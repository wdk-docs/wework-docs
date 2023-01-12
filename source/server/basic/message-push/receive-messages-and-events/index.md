---
title: 接收消息与事件 概述
date: 2020/10/20
---

# 概述[^1]

[^1]: WW-90238

## 关于接收消息

为了能够让自建应用和企业微信进行双向通信，企业可以在应用的管理后台开启接收消息模式。
开启接收消息模式的企业，需要提供可用的接收消息服务器 URL（建议使用 https）。
开启接收消息模式后，用户在应用里发送的消息会推送给企业后台。此外，还可配置地理位置上报等事件消息，当事件触发时企业微信会把相应的数据推送到企业的后台。
企业后台接收到消息后，可在回复该消息请求的响应包里带上新消息，企业微信会将该被动回复消息推送给用户。

## 开启接收消息

### 设置接收消息的参数

在企业的管理端后台，进入需要设置接收消息的目标应用，点击“接收消息”的“设置 API 接收”按钮，进入配置页面。

![](https://wework.qpic.cn/wwpic/811920_5NH6quLcQXyXXjT_1578920675/0)

要求填写应用的 URL、Token、EncodingAESKey 三个参数

- URL 是企业后台接收企业微信推送请求的访问协议和地址，支持 http 或 https 协议（为了提高安全性，建议使用 https）。
- Token 可由企业任意填写，用于生成签名。
- EncodingAESKey 用于消息体的加密。

这三个参数的用处在 加解密方案说明 章节会介绍，此处不用细究。

### 验证 URL 有效性

当点击“保存”提交以上信息时，企业微信会发送一条验证消息到填写的 URL，发送方法为 GET。
企业的接收消息服务器接收到验证请求后，需要作出正确的响应才能通过 URL 验证。

- 企业在获取请求时需要做 Urldecode 处理，否则可能会验证不成功
- 你可以访问接口调试工具进行调试，依次选择 建立连接 > 接收消息。
- 假设接收消息地址设置为：http://api.3dept.com/，企业微信将向该地址发送如下验证请求：

**请求方式**：GET<br />
**请求地址**：http://api.3dept.com/?msg_signature=ASDFQWEXZCVAQFASDFASDFSS&timestamp=13500001234&nonce=123412323&echostr=ENCRYPT_STR

**参数说明**

| 参数          | 必须 | 说明                                                                                                                 |
| ------------- | ---- | -------------------------------------------------------------------------------------------------------------------- |
| msg_signature | 是   | 企业微信加密签名，msg_signature 结合了企业填写的 token、请求中的 timestamp、nonce 参数、加密的消息体                 |
| timestamp     | 是   | 时间戳                                                                                                               |
| nonce         | 是   | 随机数                                                                                                               |
| echostr       | 是   | 加密的字符串。需要解密得到消息内容明文，解密后有 random、msg_len、msg、receiveid 四个字段，其中 msg 即为消息内容明文 |

企业后台收到请求后，需要做如下操作：

1. 对收到的请求做 Urldecode 处理
2. 通过参数 msg_signature 对请求进行校验，确认调用者的合法性。
3. 解密 echostr 参数得到消息内容(即 msg 字段)
4. 在 1 秒内响应 GET 请求，响应内容为上一步得到的明文消息内容(不能加引号，不能带 bom 头，不能带换行符)

以上 2~3 步骤可以直接使用验证 URL 函数一步到位。
之后接入验证生效，接收消息开启成功。

<a id="使用接收消息"></a>

## 使用接收消息

开启接收消息模式后，企业微信会将消息发送给企业填写的 URL，企业后台需要做正确的响应。

### 接收消息协议的说明

- 企业微信服务器在五秒内收不到响应会断掉连接，并且重新发起请求，总共重试三次。如果企业在调试中，发现成员无法收到被动回复的消息，可以检查是否消息处理超时。
- 当接收成功后，http 头部返回 200 表示接收 ok，其他错误码企业微信后台会一律当做失败并发起重试。
- 关于重试的消息排重，有 msgid 的消息推荐使用 msgid 排重。事件类型消息推荐使用 FromUserName + CreateTime 排重。
- 假如企业无法保证在五秒内处理并回复，或者不想回复任何内容，可以直接返回 200（即以空串为返回包）。企业后续可以使用主动发消息接口进行异步回复。

### 接收消息请求的说明

假设企业的接收消息的 URL 设置为 `http://api.3dept.com`。

**请求方式**：POST<br>
**请求地址**：http://api.3dept.com/?msg_signature=ASDFQWEXZCVAQFASDFASDFSS&timestamp=13500001234&nonce=123412323

**接收数据格式**：

```xml
<xml>
   <ToUserName><![CDATA[toUser]]></ToUserName>
   <AgentID><![CDATA[toAgentID]]></AgentID>
   <Encrypt><![CDATA[msg_encrypt]]></Encrypt>
</xml>
```

**参数说明**

| 参数       | 说明                                                                 |
| ---------- | -------------------------------------------------------------------- |
| ToUserName | 企业微信的 CorpID，当为第三方套件回调事件时，CorpID 的内容为 suiteid |
| AgentID    | 接收的应用 id，可在应用的设置页面获取                                |
| Encrypt    | 消息结构体加密后的字符串                                             |

企业收到消息后，需要作如下处理：

1. 对 msg_signature 进行校验
2. 解密 Encrypt，得到明文的消息结构体（消息结构体后面章节会详说）
3. 如果需要被动回复消息，构造被动响应包
4. 正确响应本次请求

以上 1~2 步骤可以直接使用解密函数一步到位。
3 步骤其实包含加密被动回复消息、生成新签名、构造被动响应包三个步骤，可以直接使用加密函数一步到位。

被动响应包的数据格式：

```xml
<xml>
   <Encrypt><![CDATA[msg_encrypt]]></Encrypt>
   <MsgSignature><![CDATA[msg_signature]]></MsgSignature>
   <TimeStamp>timestamp</TimeStamp>
   <Nonce><![CDATA[nonce]]></Nonce>
</xml>
```

**参数说明**

| 参数         | 是否必须 | 说明                   |
| ------------ | -------- | ---------------------- |
| Encrypt      | 是       | 经过加密的消息结构体   |
| MsgSignature | 是       | 消息签名               |
| TimeStamp    | 是       | 时间戳                 |
| Nonce        | 是       | 随机数，由企业自行生成 |

### 获取企业微信服务器的 ip 段

企业微信在回调企业指定的 URL 时，是通过特定的 IP 发送出去的。如果企业需要做防火墙配置，那么可以通过这个接口获取到所有相关的 IP 段。

**请求方式**：GET（HTTPS）<br />
**请求地址**： https://qyapi.weixin.qq.com/cgi-bin/getcallbackip?access_token=ACCESS_TOKEN

**参数说明**：

| 参数         | 必须 | 说明         |
| ------------ | ---- | ------------ |
| access_token | 是   | 调用接口凭证 |

**权限说明**：

无限定。

**返回结果**：

```json
{
  "errcode": 0,
  "errmsg": "ok",
  "ip_list": ["101.226.103.*", "101.226.62.*"]
}
```

**参数说明**：

| 参数    | 说明                 |
| ------- | -------------------- |
| ip_list | 企业微信回调的 IP 段 |