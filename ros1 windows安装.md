 1. 打开 `适用于 VS 2017 的 x64 本机工具命令提示` 
 2. 运行
 

```
@"%SystemRoot%\System32\WindowsPowerShell\v1.0\powershell.exe" -NoProfile -InputFormat None -ExecutionPolicy Bypass -Command "iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))" && SET "PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin"
```

3. 安装

```
PowerShell 
set-ExecutionPolicy RemoteSigned

 choco install git -y
 choco source add -n=ros-win -s="https://roswin.azurewebsites.net/api/v2" --priority=1
 choco upgrade ros-melodic-desktop_full  --execution-timeout=0
 choco install curl
```

5. 启动

```
cd C:\opt\ros\melodic\x64
setup.bat
```
6.  还需安装

```
pip install  pyyaml
pip install  PyCrypto
pip install  PyCryptodome
把目录crypto改成Crypto
pip install  gnupg
pip install  rospkg
pip install defusedxml
pip install rosdep rosinstall_generator wstool rosinstall
```
6. 还缺少一些dll
 
```
rosdep init
rosdep update
choco install urdfdom
choco install urdfdom_headers
choco install gflags
```

~~choco install log4cxx
choco install boost
choco search  rosdep~~ 

7. fromsource

```bash
pip install -U rosdep rosinstall_generator wstool rosinstall
curl --output requirements.txt -L https://raw.githubusercontent.com/ms-iot/rosdistro-db/init_windows/rosdistro_cache/catkin-requirements.txt
pip install -U --no-deps --force-reinstall -r requirements.txt
python -m pip install -U pip setuptools

rosdep init
curl --output 10-ms-iot.list -L https://raw.githubusercontent.com/ms-iot/rosdistro-db/init_windows/rosdep/sources.list.d/10-ms-iot.list
copy 10-ms-iot.list c:\etc\ros\rosdep\sources.list.d
rosdep update
choco source add -n=ros-win -s="https://roswin.azurewebsites.net/api/v2" --priority=1
choco source disable -n=chocolatey
mkdir c:\ros_catkin_ws
cd c:\ros_catkin_ws
set ROSDISTRO_INDEX_URL=https://raw.githubusercontent.com/ms-iot/rosdistro-db/init_windows/index.yaml
rosinstall_generator ros_comm --rosdistro melodic --deps --upstream-development > melodic-ros_comm.rosinstall
wstool init src melodic-ros_comm.rosinstall
rosdep install --from-paths src --ignore-src --rosdistro melodic -r -y

退出PowerShell 然后

set PATH=c:\opt\rosdeps\x64\bin;%PATH%

copy ".\src\catkin\bin\catkin_make_isolated" ".\src\catkin\bin\catkin_make_isolated.py"
python .\src\catkin\bin\catkin_make_isolated.py --use-nmake --install ^
--install-space c:/opt/ros/melodic/x64 ^
-DCMAKE_BUILD_TYPE=Release ^
-DCMAKE_PREFIX_PATH=c:/opt/ros/melodic/x64;c:/opt/rosdeps/x64
```
最后一条命令可以加上`--pkg roscpp`编译指定包。
除了基本的库，src还要下载以下的库
  [common_msgs](https://github.com/ros/common_msgs.git)
  [geometry2](https://github.com/ros/geometry2.git)
  [actionlib](https://github.com/ros/actionlib.git)
 tf2_msgs\msg\TF2Error.msg `NO_ERROR`改一下名，以免和宏冲突，tf2用到的地方也要随之改下。
tf2_eigen\CMakeLists.txt 及tf2_sensor_msgs\CMakeLists.txt 需要设置一下 `set(EIGEN3_INCLUDE_DIRS "D:/WorkBench/eigen-3")`
 tf2_py\CMakeLists.txt 把`${CATKIN_PACKAGE_PYTHON_DESTINATION}/_tf2.pyd`改成`bin/_tf2.pyd`
修改build_isolated\各个子目录下的build.make，替换成boost的静态库。
8. 其它
 
遇到的问题是有时候网络不通，过会又能连上。奇怪了。

下载[empy](https://pypi.org/project/empy/#files) ，然后`python setup.py install`

PyCrypto需要安装[VCForPython27](https://download.microsoft.com/download/7/9/6/796EF2E4-801B-4FC4-AB28-B59FBF6D907B/VCForPython27.msi) 