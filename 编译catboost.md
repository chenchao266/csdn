运行ya.bat，提示找不到cl.exe
(我用的是vs2017)

msvs\Projects 目录下的.vcxproj 
"python" 替换成python.exe的路径

生成的 f2c.exe 和 ragel6.exe 不能用
这里下载，替换
[f2c](http://www.netlib.org/f2c/mswin/)
[ragel](https://github.com/eloraiby/ragel-windows)


.vcxproj 里的 protoc.exe 参数
去掉 "-I=" "$(SolutionDir)../contrib/libs/protobuf/src"

把"\$(VC_ExecutablePath_x64_x64)\ml64.exe"之前的
"python" "$(SolutionDir)../build/scripts/fix_msvc_output.py" "ml" 去掉

还有其它的问题
PYTHONHASHSEED是什么？

把\library\cpp\tokenizer目录下的.rl文件
放到\msvs目录下

我用的python是3.6的版本，要改以下几个.py

py_compile.py

```python
open(in_fname, 'r') 改成 
open(in_fname, 'r', encoding='UTF-8')
```

configure_file.py

```python
print 后面的参数加上()
```

f2c.py

```python
open(args.input, 'r') 改成
open(args.input, 'rb')

print >> ... 改成
sys.stderr.write('f2c failed: %s, %s' % (stderr, ret))
sys.stderr.write(stderr)

'Error'改成
b'Error'

f.write(stdout)改成
f.write(str(stdout, encoding = "utf8"))
```

subprocess32.py
```python
except 后面的,e 改成 as e
0x80000000L 改成 0x80000000
```
