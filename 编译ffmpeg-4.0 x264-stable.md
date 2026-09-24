[https://github.com/ShiftMediaProject/x264/releases](https://github.com/ShiftMediaProject/x264/releases) 也可以直接下载编译好的
**vs2017  64位**

 1. msys2下运行

```
pacman -Syu
pacman -S make pkg-config diffutils yasm
pacman -S mingw-w64-x86_64-nasm mingw-w64-x86_64-gcc mingw-w64-x86_64-SDL2
```
usr\bin\link.exe改一下名

2. 编译x264

```
git clone git://git.videolan.org/x264.git
git checkout -b stable remotes/origin/stable
CC=cl ./configure --prefix=../build --host=x86_64-w64-mingw32 --enable-shared  --extra-ldflags=-Wl,--output-def=libx264.def 
```

如果`--enable-static` 后面config ffmpeg 时 会提示找不到x264，看config.log是一些符号未链接

```
make
make install
```

把lib目录下的 .dll.a 或 .dll.lib 重命名.lib
ffmpeg只认libx264.lib（动态库的lib）。可以编译ffmpeg时使用x264动态库lib，使用ffmpeg静态库时链接x264的静态库版本。
 

3. 编译ffmpeg

msys2目录下新建bat文件

```
set MSYS2_PATH_TYPE=inherit
call "D:\Program Files (x86)\Microsoft Visual Studio\2017\Professional\VC\Auxiliary\Build\vcvars64.bat"
msys2_shell.cmd -mingw64
```

 执行bat文件，然后

```
./configure --prefix=../build --target-os=win64 --arch=x86_64  --toolchain=msvc --enable-static    --extra-cflags='-I../build/include'  --extra-ldflags='-LIBPATH:../build/lib'  --enable-gpl --disable-everything --disable-avdevice --enable-muxer=mp4 --enable-muxer=h264 --enable-protocol=file --enable-avformat --enable-avcodec --enable-decoder=mjpeg --enable-decoder=mpeg4 --enable-decoder=h264 --enable-encoder=libx264 --enable-encoder=mjpeg --enable-encoder=mpeg4 --enable-parser=h264 --enable-libx264  --disable-network --disable-avfilter --disable-ffmpeg --disable-ffplay --disable-ffprobe --disable-symver  
```


`  --extra-cflags 加上 -MD `选项，链接时有问题。暂时不知如何搞。


 config.h 编码改为utf8带bom，否则大量warning
 config.mak
 awk新版本 需要 把`gsub(/\\/, "/")`改为`gsub("\\", "/")` 或`gsub(/\\\/, "/")`(这个折磨了好长时间)
  
```
make -j4

make install
```

把lib目录下的.a重命名.lib
链接静态库 还需要Bcrypt.lib

 4. 最后

目前 ffmpeg 2.8 + x264 148 版本可以正常写mp4文件。
其它版本还有问题。暂时不知如何搞。
 