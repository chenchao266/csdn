
# 安装d2l pytorch 版本
Anaconda3 python 3.9 pytorch 1.9/1.12 
d2l-0.17.6-py3-none-any.whl安装失败
[Anaconda3 配置](https://blog.csdn.net/chencao100/article/details/127986052)
[github](https://github.com/d2l-ai/d2l-en) 或[gitcode](https://gitcode.net/mirrors/d2l-ai/d2l-en)下载d2l-en-v0.17.6.zip

 

 
```bash
pip install pytz
pip install albumentations opencv_python_headless
pip install wandb
pip install ruamel.yaml
pip install numba==0.56
pip install ogb pykeops ray einops
```

修改 setup.py和安装的版本一致

```python
'jupyter==1.0.0',
'numpy==1.21.5',
'matplotlib==3.5.1',
'requests==2.27.1',
'pandas==1.4.2'
```

管理员权限 运行Anaconda3
安装pytorch 、 mmcv
pytorch 1.9  **python 3.9**
[cuda 11.1.1](https://developer.download.nvidia.com/compute/cuda/11.1.1/local_installers/cuda_11.1.1_456.81_win10.exe)
[libtorch 1.9.1](https://download.pytorch.org/libtorch/cu111/libtorch-win-shared-with-deps-1.9.1%2Bcu111.zip)
```bash
pip install torch==1.9.1+cu111 torchvision==0.10.1+cu111 torchaudio==0.9.1 numpy<2 -f https://download.pytorch.org/whl/torch_stable.html

pip install mmcv-full==1.4.8 -f https://download.openmmlab.com/mmcv/dist/cu111/torch1.9.0/index.html

pip install mmdet==2.23.0 
pip install mmsegmentation==0.29.1 
pip install mmcls==0.23.2
pip install mmdet3d==0.18.1
pip install mmrotate==0.2.0

pip install torch-scatter torch-sparse torch-cluster torch-spline-conv -f https://pytorch-geometric.com/whl/torch-1.9.1+cu111.html

pip install torchdiffeq torch-geometric
 
python setup.py install
```
pytorch1.12  **python 3.10**
[cuda 11.6.2](https://developer.download.nvidia.com/compute/cuda/11.6.2/local_installers/cuda_11.6.2_511.65_windows.exe)
[libtorch 1.12.1](https://download.pytorch.org/libtorch/cu116/libtorch-win-shared-with-deps-1.12.1%2Bcu116.zip)
```bash

pip install torch==1.12.1+cu116 torchvision==0.13.1+cu116 torchaudio==0.12.1 numpy<2 -f https://download.pytorch.org/whl/torch_stable.html
 
pip install mmcv-full==1.7.1 -f https://download.openmmlab.com/mmcv/dist/cu116/torch1.12.0/index.html

pip install mmdet==2.28.2 
pip install mmsegmentation==0.30.0 
pip install mmcls==0.25.0
pip install mmdet3d==1.0.0rc6
pip install mmrotate==0.3.4

pip install torch-scatter torch-sparse torch-cluster torch-spline-conv -f https://pytorch-geometric.com/whl/torch-1.12.1+cu116.html

pip install torchdiffeq torch-geometric
 
python setup.py install
```

pytorch2.7   **python 3.13**
[cuda 12.6.3](https://developer.download.nvidia.com/compute/cuda/12.6.3/local_installers/cuda_12.6.3_561.17_windows.exe)
[libtorch 2.7.1](https://download.pytorch.org/libtorch/cu126/libtorch-win-shared-with-deps-2.7.1%2Bcu126.zip)
```bash
pip install torch==2.7.1 torchvision==0.22.1 torchaudio==2.7.1 --index-url https://download.pytorch.org/whl/cu126
```

--------------------------
```bash

jupyter notebook
```

运行时如果出现

 -  Error #15: Initializing libiomp5md.dll, but found libiomp5md.dll already initialized.

```bash
Anaconda3\Library\bin\
site-packages\torch\
```

目录下都有 libiomp5md.dll，删除Anaconda3\Library\bin\目录下的

 -  OSError: [WinError 1455]页面文件太小，无法完成操作。
 
修改pytorch所在盘的虚拟内存大小