# MacOS-Windows

有些政府机构或金融机构的网站或应用必须在Windows系统中使用，因此考虑在MacOS上再装一个备用的Windows。  

采用的方案是先用BootCamp安装Win10，再使用Parallels Desktop从BootCamp分区虚拟。  
这样的好处是只需要安装一份Windows，就可以通过两种方式使用Win。  
从BootCamp启动Win需要关闭MacOS，重启电脑。另外MacBook的TrackPad在Win系统下的驱动不完善，使用体验较差。  
从Parallels启动Win是直接在MacOS中虚拟的，可以随时在两个系统是切换，利用Parallels Tools共享复制粘贴，文本和文件都能够在两个系统中来回传递。但毕竟相当于开着两个系统，电脑的发热量会明显提升。  

使用MacOS自带的BootCamp来安装Windows。
原本自己下载了Win10_1909的镜像，但是BootCamp说无法打开，于是只能从BootCamp的帮助里面，通过其提供的链接到下载最新版本的镜像Win10_2004。  
安装好Win系统后，安装Windows下的BootCamp，一般会在系统安装好后自动弹出安装提示。  
如果没有，可以在文件资源管理器中找到"OSXRESERVED"分区，打开"BootCamp"文件夹中的"Setup"安装BootCamp。  
安装Windows下的BootCamp过程中硬件驱动也会自动安装。可以通过桌面右下角BootCamp图标来设置TrackPad以及鼠标等操作。    
不过默认的TrackPad驱动不太好用，有些手势不支持，即便是支持的手势例如双指滑动来上下滚动页面，方向是跟MacOS上面的相反的。  
于是我安装了第三方驱动[mac-precision-touchpad](https://github.com/imbushuo/mac-precision-touchpad)  
这个驱动几乎完美支持所有手势，手势的效果也跟MacOS上面的一样。可惜的是不知道怎么调节箭头移动的速度，太慢了。  
另外，即便使用了第三方驱动，箭头还是会有粘滞感，反应不够迅速，容易引起误操作。  

此时默认的启动系统是Windows，通过桌面右下角的BootCamp图标可以选择默认从MacOS启动。  
在MacOS中也可以点击左上角苹果图标，在"系统偏好设置"里面点按"启动磁盘"来更改默认启动系统。(不过我的只有MacOS是可选的，不知道为什么)    
另外，也可以重启电脑时按住option键直到出现选项给你选择进入哪个系统。  
建议先在Windows中安装好必要的软件后，再重启到MacOS安装Parallels。  

重启到MacOS，安装Parallels Desktop 15.1.2，选择从BootCamp中读取。  
安装完后，如果发现两个系统的复制粘贴没有共享，很可能是Paralles Tools没有自动安装。  
Parallels启动Windows后，窗口的右上角有个黄色感叹号，提示安装Parallels Tools，按提示安装就行。  
接着可以在Parallels的"配置"中选择共享文件和剪贴板，默认都是共享的。  
安装Parallels Tools后，Windows窗口也可以自适应MacBook的屏幕了，并且可以进入全屏模式，表面上就像是从BootCamp启动一样。  

如果觉得Parallels发热很严重，可以尝试更改虚拟机监控程序。  
关闭Windows后，在Parallels的"配置"中"CPU与内存"里面，"虚拟机监控程序"从默认的"Parallels"改为"Apple"。  
