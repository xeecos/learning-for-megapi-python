# 配置常用工具

现在树莓派已经可以联网，我们还需要为它安装一些常用工具，比如中文显示、中文输入法、Git、Chromium浏览器等。
1. 中文显示和安装拼音输入法
```
sudo apt-get install ttf-wqy-microhei scim-pinyin
```
从```Preferences```打开```Raspberry Pi Configuration```, 点击```Set Locale```，```Language```为```zh(Chinese)```，```Country```为```CN(P.R.of China)```，```Character Set···为```UTF-8```，重启树莓派。

2.安装Git
```
sudo apt-get install git
```
3.安装Chromium浏览器
* 编辑或新增chromium.list

  ```sudo nano /etc/apt/sources.list.d/chromium.list```
* 新增一行

  ```deb http://ppa.launchpad.net/canonical-chromium-builds/stage/ubuntu vivid main```
* 保存后在终端执行
```
sudo apt-get update
sudo apt-get install chromium-browser chromium-browser-l10n
```
4.