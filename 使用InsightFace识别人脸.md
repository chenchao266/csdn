
[Face-Recognition-with-InsightFace](https://github.com/tuna-date/Face-Recognition-with-InsightFace)
[MTCNN](https://github.com/ipazc/mtcnn)
[InsightFace](https://github.com/deepinsight/insightface)

```bash
pip install keras
pip install tensorflow==2.2
```

datasets\train里的目录名中的空格' '改成'_'
使用datasets\train里的图片生成train.lst
修改src\data\dir2lst.py
```python
import sys
import os
sys.path.append('../common')
import face_image

input_dir = sys.argv[1]

dataset = face_image.get_dataset_common(input_dir, 2)
output_filename = os.path.join(input_dir, 'train.lst')
with open(output_filename, "a") as text_file:
    for item in dataset:
      oline = "%d\t%s\t%d\n" % (1, item.image_path, int(item.classname))
      text_file.write(oline)

```


```bash
python dir2lst.py F:\insightface-master0\datasets\train
```
修改src\data\face2rec2.py

```python
#try:
    #import multiprocessing #Windows下
#except ImportError:


s = mx.recordio.pack(header, b'')#加上b
```

```bash
python face2rec2.py F:\insightface-master0\datasets\train

```
使用[generate_image_pairs.py](https://blog.csdn.net/CLOUD_J/article/details/100672392)
并修改

```python
    if len(same_list) > 10: #and len(same_list) < 13
        for j in range(0, 10, 2): #len(same_list)
```

```bash
python generate_image_pairs.py --data-dir F:\insightface-master0\datasets\train --outputtxt F:\insightface-master0\datasets\train\train.txt --num-samepairs 100
```
修改[lfw2pack.py](https://blog.csdn.net/CLOUD_J/article/details/100672392)
```bash
python lfw2pack2.py --data-dir F:\insightface-master0\datasets\train --output F:\insightface-master0\datasets\train\train.bin --num-samepairs 100
```
生成的文件放到recognition\datasets\train里
新建文件property
内容为`类别数,112,112`

recognition\ArcFace
复制sample_config.py为config.py
修改config.py

```python
dataset.emore.dataset = 'emore'
dataset.emore.dataset_path = '../datasets/train'
dataset.emore.num_classes = #类别数#
dataset.emore.image_shape = (112, 112, 3)
dataset.emore.val_targets = ['train']


default.end_epoch = 100 
default.per_batch_size = 32 #128# 显卡垃圾
```
修改verification.py

```python
    #val = float(true_accept) / float(n_same)
    #far = float(false_accept) / float(n_diff)
    #改成
    if n_same == 0:
        val = 1
    else:
        val = float(true_accept) / float(n_same)
    if n_diff == 0:
        far = 0
    else:
        far = float(false_accept) / float(n_diff)

```
修改train.py

```python
#_rescale = 1.0 / args.ctx_num
_rescale = 0.03125
```
然后训练并验证
```bash
set CUDA_VISIBLE_DEVICES='0,' 
python -u train.py --network r100 --loss arcface --dataset emore

```

-----------------------------------------------------
修改src\train_softmax.py

```python
    #print(his.history['accuracy'])

    history['acc'] += his.history['accuracy']
    history['val_acc'] += his.history['val_accuracy']
```

参考RetinaFace\test.py修改src\recognizer_image.py

```python
from retinaface import RetinaFace
...
detector = RetinaFace('../RetinaFace/model/R50', 0, gpuid, 'net3')
...
faces, landmarks = detector.detect(img, thresh, scales=scales, do_flip=flip)
...
```

```bash
python faces_embedding.py --dataset F:\insightface-master0\datasets\train 
python train_softmax.py
python recognizer_image.py --image-in ../datasets/test/005.jpg

```
-------------------
其它
下载[lfw-deepfunneled](http://vis-www.cs.umass.edu/lfw/lfw-deepfunneled.tgz)
使用src\align\align_lfw.py 生成对齐后的人脸
或参考[编译RetinaFace及使用](https://blog.csdn.net/chencao100/article/details/104058423)

```python
_paths = fimage.image_path.split('\\')#Windows下'/'改成'\\'
```

```bash
python align_lfw.py --input-dir F:\lfw-deepfunneled --output-dir F:\lfw-align
```
------------------
最终
用insightface检测[新浪微博下载的图片](https://blog.csdn.net/chencao100/article/details/115304344)并识别
```python
import cv2
import sys
import numpy as np
import datetime
import os
import glob
 
 
from skimage import transform as trans
sys.path.append('../deploy')
sys.path.append('../src/common')
sys.path.append('../RetinaFace')


from retinaface import RetinaFace
from keras.models import load_model
#from mtcnn.mtcnn import MTCNN
from imutils import paths
import face_preprocess
import numpy as np
import face_model
import argparse
import pickle
import time
import cv2
import os

ap = argparse.ArgumentParser()

ap.add_argument("--mymodel", default="outputs/my_model.h5",
    help="Path to recognizer model")
ap.add_argument("--le", default="outputs/le.pickle",
    help="Path to label encoder")
ap.add_argument("--embeddings", default="outputs/embeddings.pickle",
    help='Path to embeddings')

ap.add_argument('--image-size', default='112,112', help='')
ap.add_argument('--model', default='../models/model-y1-test2/model,0', help='path to load model.')
ap.add_argument('--ga-model', default='', help='path to load model.')
ap.add_argument('--gpu', default=0, type=int, help='gpu id')
ap.add_argument('--det', default=0, type=int, help='mtcnn option, 1 means using R+O, 0 means detect from begining')
ap.add_argument('--flip', default=0, type=int, help='whether do lr flip aug')
ap.add_argument('--threshold', default=1.24, type=float, help='ver dist threshold')

args = ap.parse_args()

# Load embeddings and labels
data = pickle.loads(open(args.embeddings, "rb").read())
le = pickle.loads(open(args.le, "rb").read())

embeddings = np.array(data['embeddings'])
labels = le.fit_transform(data['names'])
# Initialize faces embedding model
embedding_model = face_model.FaceModel(args)

# Load the classifier model
model = load_model(args.mymodel)
gpuid = -1 ###-1禁止使用GPU
detector = RetinaFace('../RetinaFace/model/R50', 0, gpuid, 'net3')
# Setup some useful arguments
cosine_threshold = 0.8
proba_threshold = 0.85
comparing_num = 5
thresh = 0.8



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


# Define distance function
def findCosineDistance(vector1, vector2):
    """
    Calculate cosine distance between two vector
    """
    vec1 = vector1.flatten()
    vec2 = vector2.flatten()

    a = np.dot(vec1.T, vec2)
    b = np.dot(vec1.T, vec1)
    c = np.dot(vec2.T, vec2)
    return 1 - (a/(np.sqrt(b)*np.sqrt(c)))

def CosineSimilarity(test_vec, source_vecs):
    """
    Verify the similarity of one vector to group vectors of one class
    """
    cos_dist = 0
    for source_vec in source_vecs:
        cos_dist += findCosineDistance(test_vec, source_vec)
    return cos_dist/len(source_vecs)


# 读取中文路径
def cv_imread(filePath):
    cv_img=cv2.imdecode(np.fromfile(filePath,dtype=np.uint8),-1)
    if cv_img is None:
        return cv_img
    if len(cv_img.shape) == 2:
        cv_img=cv2.cvtColor(cv_img,cv2.COLOR_GRAY2BGR)
    return cv_img
 
def detect(count, jpgfile, spath):
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
                crop = img[box[1]:box[3], box[0]:box[2]]
                nimg = preprocess(img, bbox=box, landmark = landmarks[i])#, image_size='112,112'
                nimg = cv2.cvtColor(nimg, cv2.COLOR_BGR2RGB)
                nimg = np.transpose(nimg, (2,0,1))
                embedding = embedding_model.get_feature(nimg).reshape(1,-1)

                text = "Unknown"

                # Predict class
                preds = model.predict(embedding)
                preds = preds.flatten()
                # Get the highest accuracy embedded vector
                j = np.argmax(preds)
                proba = preds[j]
                # Compare this vector to source class vectors to verify it is actual belong to this class
                match_class_idx = (labels == j)
                match_class_idx = np.where(match_class_idx)[0]
                selected_idx = np.random.choice(match_class_idx, comparing_num)
                compare_embeddings = embeddings[selected_idx]
                # Calculate cosine similarity
                cos_similarity = CosineSimilarity(embedding, compare_embeddings)
                if cos_similarity < cosine_threshold and proba > proba_threshold:
                    name = le.classes_[j]
                    text = "{}".format(name)
                    print("Recognized: {} <{:.2f}>".format(name, proba*100))
                    if text == 'yz':
                        target_file = os.path.join(spath, str(count)+'__'+str(i)+suf)
                        cv2.imwrite(target_file, crop)
                        #oline = '%d\t%s\t%d\n' % (1,target_file, 1)#one class
                        #text_file.write(oline)
    img = None


count=0
ppath="G:\\down\\yz"
spath="G:\\down\\detect_yz"
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
        #with open(output_filename, "a") as text_file:
        for files1 in filelist1:
            oldfile=os.path.join(Olddir, files1)
            detect(count, oldfile, npath)
            count+=1  

```
