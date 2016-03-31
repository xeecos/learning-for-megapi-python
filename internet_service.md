# 使用网络服务

###Http请求
当我们需要把采集的数据存储到互联网上，或者从互联网服务获取数据时，我们就要使用一些网络服务。以https://data.sparkfun.com提供的物联网数据服务为例，我们可以很快实现采集本地温度上传到data.sparkfun.com的服务器。
```
from megapi import *
import requests
reqURL = 'https://data.sparkfun.com/input/Jxyjr7DmxwTD5dG1D1Kv?private_key=gzgnB4VazkIg7GN1g1qA&brewTemp='
def onRead(v):
    result = requests.get(reqURL+str( v ))
    print result.text    
port = 6
bot = MegaPi()
bot.start()
while True:
    bot.humitureSensorRead(port, 1, onRead)
    sleep(5)
```
在https://data.sparkfun.com/streams/Jxyjr7DmxwTD5dG1D1Kv 可以访问已上报的数据。