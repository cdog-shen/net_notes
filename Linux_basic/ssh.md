# ssh和scp

​	ssh和scp都是基于22号端口的ssh服务

## ssh的全称是secure shell---安全命令行

​	用法：ssh [参数] (user@remote)

​	user：远程用户的用户名

​	remote：远程主机，通常是地址或是主机名

​	常用参数：

​		-p	端口 port 的参数，不指定时通常为22，有些情况下服务器会指定ssh服务端口

### ssh-keygen---生成ssh公私钥

### ssh-copy-id---发配公钥给指定服务器

​	用法：ssh-copy-id [-p 22] user@remote

## scp的全称是secure copy---安全复制

​	用法：scp [参数] (user@remote:file) [local_directory]

​	user：远程用户

​	remote：远程主机

​	file：目标文件的路径（可以是相对路径也可以是绝对路径）（相对路径时是相对该用户的home文件夹下）

​	local_directory：保存位置的路径

​	常用参数：

​		-r	递归复制，复制文件夹时要用如同cp命令

​		-P	端口参数，默认22

## 配置别名

更改在 .ssh 目录下的 config 文件追加内容：

```config
Host (name)
	HostName (0.0.0.0)
	User (name)
	Port (22)
```

