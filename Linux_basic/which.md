# which

which命令用于查询可执行命令的二进制文件所在位置

用法：which (unix命令)

通常会直接返回该命令的绝对路径

但像 cd 命令这样存在于系统内核的文件是不能被查找到的

## bin和sbin

### 	/bin

​		binary，可执行二进制文件，用于具体应用

### 	/sbin

​		system binary，系统管理员专用的二进制文件，主要用于系统管理

### 	/usr/bin

​		user commands for application，后期软件的可执行文件

​	/usr/sbin

​		super user commands for applications，超级用户的管理程序