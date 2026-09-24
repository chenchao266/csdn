**vs2017  64位**

 1. `git clone --recursive https://github.com/pytorch/pytorch.git`


 2. Anaconda命令行
也可以在build_windows.bat里设置
```bash
set CAFFE2_USE_MSVC_STATIC_RUNTIME=OFF
set BUILD_SHARED_LIBS=ON
set USE_CUDA=ON
set USE_NNPACK=OFF
set USE_MKL=OFF
set USE_TBB=ON
set USE_OPENMP=ON
set BUILD_CAFFE2_MOBILE=OFF
set BUILD_TEST=FALSE
set MAX_JOBS=2
set BLAS=OpenBLAS
set USE_NUMPY=FALSE
set MKL_THREADING=TBB
```
如果`BUILD_TEST=TRUE`，需要关闭杀毒软件，否则exe无法嵌入manifest导致失败。
如果不设置`MAX_JOBS`，内存会爆（内存>=16G，可以忽略）
如果`CAFFE2_USE_MSVC_STATIC_RUNTIME=ON`，生成build.ninja编译FLAGS是/MT，否则是/MD

tools\setup_helpers\cmake.py

```
elif var.startswith(('BUILD_', 'USE_', 'CMAKE_')):
改成
elif var.startswith(('BUILD_', 'USE_', 'CMAKE_', 'CAFFE2_', 'TORCH_')):
```

在cmake\Modules_CUDA_fix\FindCUDA.cmake里加上

```
SET(TORCH_CUDA_ARCH_LIST "5.0;5.2;6.0;6.1;7.0;7.5")
```

如果设置OpenBLAS，需要修改cmake\Modules\FindOpenBLAS.cmake

```
SET(OpenBLAS_INCLUDE_DIR "D:/WorkBench/.../openblas")
SET(OpenBLAS_LIB "D:/WorkBench/.../libopenblas.dll.a")
```

 

 3. scripts目录下运行
 
```
build_windows.bat
```
如果`BUILD_SHARED_LIBS=OFF`，1.3.1版本生成的lib会超过4G，结果link就失败了。
如果`BUILD_SHARED_LIBS=ON`，生成的dll会有1G多，下一步就是如何精简了。
Release模式，编译时更新torch.pdb，这一步很慢，让人受不了。。。