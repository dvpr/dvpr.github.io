## MAC

<br /><br />

##### 系统变慢
##### Mac slowly

1.	用CleanMyMac清理系统垃圾；

2.	重置NVRAM；

	> 方法是：  
	> 1、彻底关闭电脑后连接上电源适配器；  
	> 2、开机，在显示灰屏前同时按住Command+Option+P+R 键，直到听见三次以上启动声后松开这些键。  
	> 3、电脑启动后速度就恢复了

3.	修复权限；

4.	删掉无用多余的软件，也可用CleanMyMac。

> 进到资源库→找到“Preference”→清空里面的东西。**这样做等同于重装**

<br /><br />

##### OS X：关于 OS X 恢复功能
> [链接](http://www.apple.com/cn/osx/recovery/) 只要在启动过程中按住 Command-R，OS X 恢复功能便会立即运行。它可让你从常用工具中进行选择：你可以运行磁盘工具来检查或修复硬盘，擦除硬盘并重装新的 OS X，或从 Time Machine 的备份中恢复你的 Mac。你还可使用 Safari 获得 Apple 在线技术支持。如果 OS X 恢复功能出现问题，它会自动通过互联网连接到 Apple。

<br /><br />

##### 使用U盘重装系统
##### Reinstall MacOS by usb

> 下好山狮的dmg镜像，用mac里的磁盘工具把映像恢复到U盘上
>
> 然后把U盘和移动硬盘连到电脑上，开机，用U盘启动，用里面的磁盘工具把移动硬盘重分区，选GUID分区表，类型选Mac OS日志式（以上步骤是因为我有洁癖装系统前必格盘），然后正常装系统到移动硬盘就好啦

<br /><br />

##### 使用dd命令写入U盘
##### Use dd command in MacOs
```
diskutil list
diskutil umountDisk your_usb_path
sudo dd bs=4m if=your_file_path of=your_usb_path 
diskutil eject your_usb_path
```