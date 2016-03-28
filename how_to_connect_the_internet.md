# 如何联网

最新的树莓派3已经集成了WiFi模块，用户只需要在WiFi面板中搜索附近的WiFi路由器输入正确的密码即可。
而没有自带WiFi模块的树莓派2，我们可以通过有线连接路由器或者外接USB WiFi模块联网。

对于外接的USB WiFi模块可能还需要安装驱动。以Realtek品牌的WiFi模块为例。

1.查看Wifi网卡是否为Realtek：
以下指令在终端里执行，
```
dmesg | grep usb
```
2.如果已经通过有线联网，可以搜索一下Realtek驱动：
```
apt-cache search realtek
```
3.安装驱动：
```
sudo apt-get install firmware-realtek
```
4.如果不能联网，可以先在已联网的电脑下载deb安装包：```http://mirrors.aliyun.com/raspbian/raspbian/pool/non-free/f/firmware-nonfree firmware-realtek_0.43_all.deb```

5.通过U盘拷贝到树莓派上，执行
```
sudo dpkg -i path/firmware-realtek_0.43_all.deb```
剩下的工作就是在网络里设置WiFi了。
已经联网的树莓派除了通过外接屏幕和键盘鼠标操作，也可以远程SSH登录，ssh账号为```pi```，默认密码为```raspberry```