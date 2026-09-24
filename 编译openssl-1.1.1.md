下载并安装[ ActivePerl](http://www.activestate.com/activeperl/downloads)
下载 [OpenSSL](http://www.openssl.org/)

修改ActivePerl\Config.pm
参考[Can't locate Win32/Console.pm](https://blog.csdn.net/zhangzq86/article/details/105100942
)

 
```powershell
cd E:\openssl-1.1.1j
perl Configure VC-WIN32 --prefix=E:\OpenSSL


```
定位并运行vcvars32.bat

```powershell
cd E:\openssl-1.1.1j
nmake -f makefile
```
