## Mirai-api-http消息类型一览

#### Source

```json5
{
    "type": "Source",
    "id": 123456,
    "time": 123456
}
```

| 名字 | 类型 | 说明                                                         |
| ---- | ---- | ------------------------------------------------------------ |
| id   | Long | 消息的识别号，用于引用回复（Source类型只在群消息中返回，且永远为chain的第一个元素） |
| time | Long | 时间戳                                                       |

#### Quote

```json5
{
    "type": "Quote",
    "id": 123456
}
```

| 名字 | 类型 | 说明                        |
| ---- | ---- | --------------------------- |
| id   | Long | 被引用回复的消息的messageId |


#### At

```json5
{
    "type": "At",
    "target": 123456,
    "display": "@Mirai"
}
```

| 名字    | 类型   | 说明                                           |
| ------- | ------ | ---------------------------------------------- |
| target  | Long   | 群员QQ号                                       |
| dispaly | String | At时显示的文字，发送消息时无效，自动使用群名片 |

#### AtAll

```json5
{
    "type": "AtAll"
}
```

| 名字    | 类型   | 说明                      |
| ------- | ------ | ------------------------- |
| -       | -      | -                         |

#### Face

```json5
{
    "type": "Face",
    "faceId": 123
}
```

| 名字   | 类型 | 说明       |
| ------ | ---- | ---------- |
| faceId | Int  | QQ表情编号 |

#### Plain

```json5
{
    "type": "Plain",
    "text": "Mirai牛逼"
}
```

| 名字 | 类型   | 说明     |
| ---- | ------ | -------- |
| text | String | 文字消息 |

#### Image

```json5
{
    "type": "Image",
    "imageId": "{01E9451B-70ED-EAE3-B37C-101F1EEBF5B5}.png",  //群图片格式
    //"imageId": "/f8f1ab55-bf8e-4236-b55e-955848d7069f"      //好友图片格式
    "url": "http://xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
}
```

| 名字    | 类型   | 说明                                                         |
| ------- | ------ | ------------------------------------------------------------ |
| imageId | String | 图片的imageId，群图片与好友图片格式不同。不为空时将忽略url属性 |
| url     | String | 图片的URL，发送时可作网络图片的链接；接收时为腾讯图片服务器的链接，可用于图片下载 |

#### Xml

```json5
{
    "type": "Xml",
    "xml": "XML"
}
```

| 名字 | 类型   | 说明    |
| ---- | ------ | ------- |
| xml  | String | XML文本 |


