直接运行，依赖netcore runtime，需要.runtimeconfig.json及.deps.json

```powershell
dotnet exec ...
```
---
dotnet-warp 是一个Global .NET Core的打包工具

```powershell
dotnet tool install --global dotnet-warp
```

然后直接在项目目录下运行下面的命令就够了

```powershell
dotnet-warp
```
参考
[.NET Core的打包到一个exe程序](https://www.cnblogs.com/RainFate/p/12093851.html)

[.NET Standard](https://docs.microsoft.com/en-us/dotnet/standard/net-standard)

.NET Core 2.1 === .NET Standard 2.0

.NET Core 3.1 === .NET Standard 2.1

.NET 6

.NET 8

[.NET 升级利器：Upgrade Assistant](https://www.dongchuanmin.com/net/5285.html)

[.Net Framwork和.Net Core相互转换](https://zhuanlan.zhihu.com/p/716382147)

[.NET 6.0 vs2022 独立模式部署应用程序](https://blog.csdn.net/weixin_40671962/article/details/128372143)

-----------------------------------
查看依赖关系

 - ildasm.exe  ... \Microsoft SDKs\Windows\ ...目录下
 - [dnSpy](https://github.com/dnSpy/dnSpy) 
 - [ILSpy](https://github.com/icsharpcode/ILSpy)
