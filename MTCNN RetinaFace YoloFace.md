
[MTCNN](https://github.com/imistyrain/MTCNN)
Fast-MTCNN /mtcnn_opencv.cpp
bug:
 line 174             `faceBox.score = confidence_data[i];`
should be :  `faceBox.score = 1.0f - confidence_data[i];`

------

## RetinaFace-Cpp
[retinaface](https://github.com/deepinsight/insightface/tree/master/detection/retinaface)
[RetinaFace-Cpp](https://github.com/Charrin/RetinaFace-Cpp)
[retinaface_caffe](https://github.com/wzj5133329/retinaface_caffe)
[Retinaface-caffe](https://github.com/cholihao/Retinaface-caffe)

------
## scrfd

[scrfd](https://github.com/deepinsight/insightface/tree/master/detection/scrfd)

修改`mmdet\__init__.py`
 
```python
mmcv_minimum_version = '1.1.5'
mmcv_maximum_version = '1.4.8'
```
安装mmdet 
```powershell
python setup.py develop
```
导出onnx
```powershell
python tools/scrfd2onnx.py configs/scrfd/scrfd_34g.py model.pth --shape 640 640 --input-img t2.jpg
```
训练 修改 configs/scrfd/scrfd_34g.py
```python
	total_epochs = 10*lr_mult 	#80
	checkpoint_config = dict(interval=10)	#80
	evaluation = dict(interval=10, metric='mAP')	#80
    samples_per_gpu=1, 	#8
    workers_per_gpu=1, 	#3
```
  修改 mmdet\models\dense_heads\scrfd_head.py
  
```python
        avg_factor = sum(avg_factor)
        avg_factor = reduce_mean(avg_factor).item()
        if  avg_factor != 0:	#+++
            losses_bbox = list(map(lambda x: x / avg_factor, losses_bbox))
        losses = dict(loss_cls=losses_cls, loss_bbox=losses_bbox)
        if self.use_kps:
            if  avg_factor != 0:	#+++
                losses_kps = list(map(lambda x: x / avg_factor, losses_kps))
            losses['loss_kps'] = losses_kps
        if self.use_dfl:
            if  avg_factor != 0:	#+++
                losses_dfl = list(map(lambda x: x / avg_factor, losses_dfl))
            losses['loss_dfl'] = losses_dfl
        return losses
```

 
```powershell
python tools/train.py configs/scrfd/scrfd_34g.py  --gpus 1
```

[scrfd-opencv](https://github.com/hpc203/scrfd-opencv)




------
## YoloFace
[yolov5](https://github.com/hpc203/yolov5-face-landmarks-opencv-v2)
[yolov5-face](https://github.com/deepcam-cn/yolov5-face)
[yolov7](https://github.com/hpc203/yolov7-detect-face-onnxrun-cpp-py)
[yolov7-face](https://github.com/derronqi/yolov7-face)
[opencv Support for YOLOv7 ONNX](https://github.com/opencv/opencv/pull/22290)
修改 dnn\src\layers\fast_convolution\fast_convolution.cpp 

```cpp
        int k = 0, nbias = K + 32;
        conv->biasBuf.resize(nbias);//reserve //20221125 opencv-4.x
```

