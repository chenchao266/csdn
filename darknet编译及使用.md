 
 cuda 9.2/10.1 vs2017 编译[darknet](https://github.com/AlexeyAB/darknet)
 不能预定义 `_CRTDBG_MAP_ALLOC`
 

 - darknet  
 - darknet_no_gpu 
 -  yolo_cpp_dll 
 -  yolo_cpp_dll_no_gpu

 这几个项目的中间目录不能相同。
 
 AlexeyAB版本的darknet，C++中调用(静态库)，需要改一些函数，把返回值/参数`network`的改成返回`network*`
如果用gpu 需预定义

```
#define  _TIMESPEC_DEFINED
#define GPU
#define CUDNN
#define CUDNN_HALF
然后
#include "darknet.h"
```

 

