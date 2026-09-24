编译[RetinaFace](https://github.com/deepinsight/insightface/tree/master/RetinaFace) 
另见 [RetinaFace-Cpp](https://github.com/Charrin/RetinaFace-Cpp)、[Retinaface-caffe](https://github.com/cholihao/Retinaface-caffe)

Anaconda下运行
```bash
pip install mxnet
或
pip install mxnet-cu101
conda install libpython m2w64-toolchain -c msys2
conda install cython
```

在Python安装路径下找到\Lib\distutils文件夹，创建distutils.cfg写入如下内容：

```
[build]
compiler=mingw32

[build_ext]
compiler=mingw32 
```
然后进入RetinaFace的目录
修改test.py

```python
gpuid = -1 ###禁止使用GPU
```

修改rcnn\cython\cpu_nms.pyx
```python
cdef np.ndarray[np.int_t, ndim=1] order = scores.argsort()[::-1]
###改成
cdef np.ndarray[np.int_t, ndim=1] order = scores.argsort()[::-1].astype(np.int32)
```
然后
```bash
cd rcnn
cd cython
python setup.py build_ext --inplace
cd ..
cd pycocotools
python setup.py build_ext --inplace
```
其它

```bash
pip install --upgrade jupyter_client
conda install spyder=4.0.1
###删除.spyder-py3
```

参考
[RetinaFace在win10+CPU版mxnet+python36下配置运行](https://blog.csdn.net/sinat_28704977/article/details/98963166)

附
用RetinaFace检测[新浪微博下载的图片](https://blog.csdn.net/chencao100/article/details/115304344)并对齐
```python
import cv2
import sys
import numpy as np
import datetime
import os
import glob
from retinaface import RetinaFace
import face_preprocess
from skimage import transform as trans

#from face_preprocess
def preprocess(img, bbox=None, landmark=None, **kwargs):

  M = None
  image_size = [112,112]
  if landmark is not None:
    assert len(image_size)==2
    src = np.array([
      [30.2946, 51.6963],
      [65.5318, 51.5014],
      [48.0252, 71.7366],
      [33.5493, 92.3655],
      [62.7299, 92.2041] ], dtype=np.float32 )
    if image_size[1]==112:
      src[:,0] += 8.0
    dst = landmark.astype(np.float32)

    tform = trans.SimilarityTransform()
    tform.estimate(dst, src)
    M = tform.params[0:2,:]
    #M = cv2.estimateRigidTransform( dst.reshape(1,5,2), src.reshape(1,5,2), False)

  if M is None:
    if bbox is None: #use center crop
      det = np.zeros(4, dtype=np.int32)
      det[0] = int(img.shape[1]*0.0625)
      det[1] = int(img.shape[0]*0.0625)
      det[2] = img.shape[1] - det[0]
      det[3] = img.shape[0] - det[1]
    else:
      det = bbox
    margin = kwargs.get('margin', 44)
    bb = np.zeros(4, dtype=np.int32)
    bb[0] = np.maximum(det[0]-margin/2, 0)
    bb[1] = np.maximum(det[1]-margin/2, 0)
    bb[2] = np.minimum(det[2]+margin/2, img.shape[1])
    bb[3] = np.minimum(det[3]+margin/2, img.shape[0])
    ret = img[bb[1]:bb[3],bb[0]:bb[2],:]
    if len(image_size)>0:
      ret = cv2.resize(ret, (image_size[1], image_size[0]))
    return ret 
  else: #do align using landmark
    assert len(image_size)==2

    #print(src.shape, dst.shape)
    #print(src)
    #print(dst)
    #print(M)
    warped = cv2.warpAffine(img,M,(image_size[1],image_size[0]), borderValue = 0.0)

    #tform3 = trans.ProjectiveTransform()
    #tform3.estimate(src, dst)
    #warped = trans.warp(img, tform3, output_shape=_shape)
    return warped


# 读取中文路径
def cv_imread(filePath):
    cv_img=cv2.imdecode(np.fromfile(filePath,dtype=np.uint8),-1)
    if cv_img is None:
        return cv_img
    if len(cv_img.shape) == 2:
        cv_img=cv2.cvtColor(cv_img,cv2.COLOR_GRAY2BGR)
    return cv_img
 
def detect(count, jpgfile, spath, detector, text_file):
    print(jpgfile)
    img = cv_imread(jpgfile)
    if img is None:
        return
    index = jpgfile.rfind('.')
    if index > 0:
        suf = jpgfile[index:]
    else:
        suf='.jpg'
    print(img.shape)
    thresh = 0.8
    scales = [1024, 1980]
    im_shape = img.shape
    target_size = scales[0]
    max_size = scales[1]
    im_size_min = np.min(im_shape[0:2])
    im_size_max = np.max(im_shape[0:2])
    #im_scale = 1.0
    #if im_size_min>target_size or im_size_max>max_size:
    im_scale = float(target_size) / float(im_size_min)
    # prevent bigger axis from being more than max_size:
    if np.round(im_scale * im_size_max) > max_size:
        im_scale = float(max_size) / float(im_size_max)
    print('im_scale', im_scale)
    scales = [im_scale]
    flip = False
    faces, landmarks = detector.detect(img, thresh, scales=scales, do_flip=flip)
    print(count, faces.shape, landmarks.shape)
    #print(type(faces))
    #print(type(landmarks))
    if faces is not None:
        print('find', faces.shape[0], 'faces')
        for i in range(faces.shape[0]):
            #print('score', faces[i][4])
            box = faces[i].astype(np.int) 
            if (box[3]-box[1]) > 100 and (box[2]-box[0]) > 100:
                #crop = img[box[1]:box[3], box[0]:box[2]]
                crop = preprocess(img, bbox=box, landmark = landmarks[i])#, image_size='112,112'
                target_file = os.path.join(spath, str(count)+'__'+str(i)+suf)
                cv2.imwrite(target_file, crop)
                oline = '%d\t%s\t%d\n' % (1,target_file, 1)#one class
                text_file.write(oline)
    img = None


gpuid = 0 ###-1禁止使用GPU
detector = RetinaFace('./model/R50', 0, gpuid, 'net3')
count=0
ppath="G:\\down\\yz"
spath="G:\\down\\detect_align"
dirlist=os.listdir(ppath)
for dirs in dirlist:
    Olddir=os.path.join(ppath, dirs)
    if os.path.isdir(Olddir):
        output_filename = os.path.join(spath, 'lst')
        npath = os.path.join(spath, dirs[0:4])
        isExists = os.path.exists(npath)
        if not isExists:
            os.makedirs(npath)
        filelist1=os.listdir(Olddir)
        with open(output_filename, "a") as text_file:
            for files1 in filelist1:
                oldfile=os.path.join(Olddir, files1)
                detect(count, oldfile, npath, detector, text_file)
                count+=1


```
