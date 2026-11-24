安装 [msys2-x86_64-20261120.exe](https://github.com/msys2/msys2-installer/releases/download/2026-11-20/msys2-x86_64-20261120.exe)
```
pacman -Syu
pacman -S mingw-w64-ucrt-x86_64-gtk3 \
          mingw-w64-ucrt-x86_64-python-cairo \
          mingw-w64-ucrt-x86_64-pango \
          mingw-w64-ucrt-x86_64-gcc
```          
找到你的MSYS2安装目录（默认是C:\msys64）
将以下路径添加到系统环境变量PATH中：
C:\msys64\ucrt64\bin
C:\msys64\usr\bin
```
pip install weasyprint
```
测试
```
import os,time
import subprocess
from pathlib import Path
 
os.add_dll_directory(r"C:\msys2\ucrt64\bin")
os.environ['WEASYPRINT_DLL_DIRECTORIES'] = r'C:\msys2\ucrt64\bin'
from weasyprint import HTML
```
