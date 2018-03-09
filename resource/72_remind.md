# 技能模块 Skill
## 提醒
### 1、获取提醒列表
请求获取设备上的提醒列表：

Swift:

```swift
RokidMobileSDK.skill?.remind.getList(deviceId: String,
                           completion: @escaping (_ error: RKError?, _ reminds: [RKRemind]?) -> Void)
```

RKRemind 字段说明：

| 参数 | 类型 | 必要？ | 说明 |
| --- | --- | --- | --- |
| id |  int| 是 | 闹钟Id |
| year | int | 是 | 年 |
| month | int | 是 |  月|
| day | int | 是 | 日 |
| hour | int | 是 | 小时 |
| minute | int | 是 | 分钟 |
| content | String | 是 | 提醒内容 |

---

### 2、删除提醒
删除一个提醒：

Swift:

```swift
RokidMobileSDK.skill?.remind.delete(deviceId: String, remind: RKRemind)
```

---

