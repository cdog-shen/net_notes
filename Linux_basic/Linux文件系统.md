由于多用户操作系统的特性，盘符式的分区方式不再适用

Linux下并没有盘符的概念存在，只有一个顶级目录---根目录(/)，其余的文件都存放于根目录及其子目录，并根据用户来区分，用户只能在自己权限范围内读写

但是对于系统存储硬件来说，对于硬盘的分区和修改都是一样的，只是调用的方法不一样

Windows通常会采用直接分配盘符的方式，直接管理

Linux中每个磁盘分区必须被挂载到相应的目录才能操作，一个磁盘只能保存一份数据，但其挂载的位置可能会有不同

制定磁盘分区是有一定好处的，并不是Linux的文件系统只有一个根目录作为主体所以就认为磁盘分区毫无必要，分区有诸多好处

​	可以把不同资料，分别放入不同分区中管理，降低风险。

​	大硬盘搜索范围大，效率低

​	磁盘配合只能对分区做设定

​	/home /var /usr /local 经常是单独分区，因为经常会操作，容易产生碎片

对于新手来说，最好还是将整个文件系统都设置在 / 挂载点下，这样遇到的问题更少

## 不同分区 不同功能

​	分区的名字都是其功能的缩写

​		/bin 		系统基础的命令存放处(cd ls cp mv mkdir)，普通用户也可以执行

​		/boot		Linux的内核及引导系统程序所需要的文件，一般是一个独立的分区，内含有grub kernels initrd等等

​		/dev		 一些必要的设备,声卡、磁盘等

​		/etc 		系统配置文件存放处，比如账号密码

​			opt目录：opt对应配置文件

​			X11目录：XWindows系统配置文件

​			xml目录：xml配置

​		/home	用户工作目录，home下的每一个文件夹都代表了一个用户，内包含个人环境变量，通常为单个分区

​		/lib		 库文件存放区（bin和sbin所需的动态链接库）

​		/media	可移动媒体挂载分区，系统默认挂载到此处

​		/mnt		 临时挂载文件系统。这个目录一般是用于存放挂载储存设备的挂载目录的，比如有cdrom 等目录

​		/opt		 自选安装的应用程序包

​		/proc		操作系统运行时，进程（正在运行中的程序）信息及内核信息（比如cpu、硬盘分区、内存信息等）存放在这里

​		/root		root用户的工作目录（通常没有子目录）

​		/sbin		super bin文件，管理员用户所使用的bin文件

​		/tmp		 系统临时文件，一般重启后不会被保存

​		/usr		 包含了系统和用户工具和程序

​			/usr/bin	普通用户非必须可执行命令

​			/usr/include	标准头文件

​			/usr/lib	用户的库文件

​			/usr/src	内核源码

​			/usr/X11R6	X Window System, Version 11, Release 6

​		/srv		该目录存放一些服务启动之后需要提取的数据

