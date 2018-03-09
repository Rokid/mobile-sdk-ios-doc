# 设备模块 Device
## 获取设备列表

**接口说明**

```
目前获取服务端masterId对应的设备列表，
注意 RKDevice此时里面只有 rokiId,rokidNick,basic_info信息，
底层会默认给用户选择一个当前设备，逻辑图如下：
```

**示例代码**

Swift:

```swift
// 设备信息 icon、name、alive
RokidMobileSDK.device.queryDeviceList(complete:(RKError?,[RKDevice])->Void)
```

```json
[
    {
        //设备昵称
        "rokidNick": "xxx",   
        //设备Id          
        "rokiId": "0011111111111111",   
        "basic_info": {
            //设备地区             
            "region": "CN",             
            "sn": "02010217020001ED",
            //系统版本号
            "ota": "2.2.2-20171027.091126",
            //mac地址
            "mac": "02:00:00:00:00:00",
            "ip": "183.129.185.66",
            //局域网IP    
            "lan_ip":"192.168.1.156",
            //自定义TTS音色
            "ttsList": "[{\"name\":\"111777\",\"vibrato\":0,\"speed\":0,\"formant\":0,\"tone\":0},{\"name\":\"234566777777\",\"vibrato\":4,\"speed\":5,\"formant\":-5,\"tone\":5},{\"name\":\"5555\",\"vibrato\":-5,\"speed\":5,\"formant\":-5,\"tone\":-5}]",
            //系统当前选择TTS音色
            "tts": "{\"formant\":-3,\"speed\":-2,\"tone\":1,\"ttsName\":\"蜡笔小新\"}"
         }
    }
]
```

---

