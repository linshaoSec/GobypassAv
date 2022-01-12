**Golang cs上线免杀工具**
by:linshao

通过简单的免杀来学习Go，源码注释比较多，方便阅读
time: 2022-1-12日

```
需要环境:windows/ golang
下载地址https://golang.google.cn/dl/go1.17.6.windows-amd64.msi
```

```
---------------------------------------------------------------------------
使用:	1.修改mian.go 14行的shellcode(注意cs的shellcede要勾选64位否则运行不了)
	 2.cmd执行go run main.go 运行本程序生成加载器源码bypass.go
	 3.cmd执行go build -ldflags "-H windowsgui" bypass.go 生成exe可执行文件
---------------------------------------------------------------------------
原理:1.利用杀软对golang的弱检测，
	2.对shellcode和一些关键字进行随机编码来防止被抓特征码，若是被检测了请尝试重新生成
---------------------------------------------------------------------------
```

> 报错解决方案
>
> go env -w GO111MODULE=auto
>
>![image](https://user-images.githubusercontent.com/96420060/149149788-df868afc-0519-42de-9752-f4fde458cfa1.png)
>
> 
>
> 使用上的疑问或有其他好的建议请指教:
>
> 技术之路，希望能与努力的你相遇。。。
>
>正在寻求爱交流分享的小伙伴，我们的小圈子期待你的加入：
>
> 微信公众号:
>
> ![img](https://s3.bmp.ovh/imgs/2022/01/a99511042861512a.jpg)
