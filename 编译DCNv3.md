# 编译DCNv3
[INTERN-2.5](https://github.com/opengvlab/internimage)

windows vs2017 cuda 11.6.2 pytorch 1.12.1+cu116

```cpp
//修改 dcnv3_cuda.cu
//#include <torch/torch.h> //注释掉
torch:: 改成at::
//修改 dcnv3_cuda.h
#include <tuple>	//添加
```
管理员权限打开Anaconda Prompt
```bash
cd InternImage-master\detection\ops_dcnv3
"C:\Program Files (x86)\Microsoft Visual Studio\2017\Professional\VC\Auxiliary\Build\vcvars64.bat"

set DISTUTILS_USE_SDK=1
python setup.py build install
```
