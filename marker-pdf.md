安装 [msys2-x86_64-20261120.exe](https://github.com/msys2/msys2-installer/releases/download/2026-11-20/msys2-x86_64-20261120.exe)
```powershell
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
```powershell
# Linux/Mac
export HF_ENDPOINT=https://hf-mirror.com
 
# Windows (CMD)
set HF_ENDPOINT=https://hf-mirror.com
 
# Windows (PowerShell)
$env:HF_ENDPOINT="https://hf-mirror.com"

pip install weasyprint
pip install marker-pdf
# 安装/更新最新版 huggingface-hub（必须）
pip install -U huggingface-hub
```
测试
```python
import os,time
import subprocess
from pathlib import Path
 
os.add_dll_directory(r"C:\msys2\ucrt64\bin")
os.environ['WEASYPRINT_DLL_DIRECTORIES'] = r'C:\msys2\ucrt64\bin'
from weasyprint import HTML
```

\site-packages\weasyprint\text\ffi.py
```python
##添加
os.add_dll_directory(r"C:\msys2\ucrt64\bin")

```
\site-packages\indra_ocr\math.py
```python
meta = json.loads((onnx_dir / "math_meta.json").read_text()
##修改为
meta = json.loads((onnx_dir / "math_meta.json").read_text(encoding="utf-8"))
```