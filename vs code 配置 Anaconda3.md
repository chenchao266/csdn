# 历史版本
[~~Anaconda3~~ ](https://repo.anaconda.com/archive/)
[Miniconda3](https://repo.anaconda.com/miniconda/)
[Miniforge](https://conda-forge.org/miniforge/#history/)
[Miniforge镜像](https://mirrors.tuna.tsinghua.edu.cn/github-release/conda-forge/miniforge/)
## conda
.condarc
```css
channels:
  - https://mirrors.bfsu.edu.cn/anaconda/cloud/
  - https://mirrors.bfsu.edu.cn/anaconda/cloud/pytorch/
  - https://mirrors.bfsu.edu.cn/anaconda/cloud/menpo/
  - https://mirrors.bfsu.edu.cn/anaconda/cloud/bioconda/
  - https://mirrors.bfsu.edu.cn/anaconda/cloud/msys2/
  - https://mirrors.bfsu.edu.cn/anaconda/cloud/conda-forge/
  - https://mirrors.bfsu.edu.cn/anaconda/pkgs/free/
  - https://mirrors.bfsu.edu.cn/anaconda/pkgs/main/
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/pytorch/
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
  - defaults

```
pip\pip.ini

```bash
[global]
index-url = https://pypi.tuna.tsinghua.edu.cn/simple
[install]
trusted-host = pypi.tuna.tsinghua.edu.cn
```

python3.9 兼容性好
```bash
conda install python=3.9
conda create --name py39 python=3.9 anaconda
conda activate py39
```

## vs code

vs2019_light.json

```css
"editor.background": "#FFFFFF",
```
改为
```css
"editor.background": "#CCE8CF",
```
settings.json
参考https://blog.csdn.net/shaooping/article/details/122392978
```css
 {
    "workbench.colorTheme": "Visual Studio 2019 Light",
    "python.analysis.extraPaths": [
        "C:\\ProgramData\\Anaconda3\\Lib\\site-packages",
        "C:\\Users\\cc\\AppData\\Roaming\\Python\\Python39\\site-packages"
    ],
    "workbench.iconTheme": "material-icon-theme",
    "python.autoComplete.extraPaths": [
    
    ],

    "terminal.integrated.profiles.windows": {
        "PowerShell": {
            "source": "PowerShell",
            "icon": "terminal-powershell"
        },
 
        "conda powershell terminal":{
            "path": "C:\\Windows\\System32\\WindowsPowerShell\\v1.0\\powershell.exe",
            "args": [
          "-ExecutionPolicy" ,"ByPass", "-NoExit", "-Command","& 'C:\\ProgramData\\Anaconda3\\shell\\condabin\\conda-hook.ps1'; conda activate 'C:\\ProgramData\\Anaconda3' "
            ],
            "title":"conda powershell terminal",
        },
           
        "conda powershell 1.13":{
            "path": "C:\\Windows\\System32\\WindowsPowerShell\\v1.0\\powershell.exe",
            "args": [
          "-ExecutionPolicy" ,"ByPass", "-NoExit", "-Command","& 'C:\\ProgramData\\Anaconda3\\shell\\condabin\\conda-hook.ps1'; conda activate 'C:\\Users\\cc\\.conda\\envs\\pytorch1.13' "
            ],
            "title":"conda powershell 1.13",
        }
    },
    "terminal.integrated.defaultProfile.windows": "conda powershell terminal",
    "python.terminal.activateEnvironment": true,
    "python.pythonPath": "C:\\ProgramData\\Anaconda3\\python.exe"
    //"python.pythonPath": "C:\\Users\\cc\\.conda\\envs\\pytorch1.13\\python.exe",
    "python.envFile": "${workspaceFolder}/.vscode/.env",
 
}

```

调试py文件时，launch.json例子

```css
{
    "version": "0.2.0",
    "configurations": [
        {
            "name": "Python: Current File",
            "type": "python",
            "request": "launch",
            "program": "${file}",
            "console": "integratedTerminal",
            "justMyCode": true,
            //"args": ["--weights", "yolov5s.pt", "--include", "torchscript", "onnx" ]
            "args": ["--data", "data/coco128.yaml", "--weights", "yolov5s.pt","--img", "640", "--device", "0", "--batch-size", "1", "--workers", "1" ]
        }
    ]
}
```
如果 训练时候提示 页面文件太小
修改 yolov5 utils\general.py
```python
NUM_THREADS = 1 #min(8, max(1, os.cpu_count() - 1)) 
```
减小`--batch-size`的值
减小`--workers`的值