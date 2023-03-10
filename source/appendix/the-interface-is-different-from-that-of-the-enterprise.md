---
ref: https://developer.work.weixin.qq.com/document/path/90453
date: 2022/01/20
---

# 与企业号接口差异

企业号升级为企业微信后，部分原企业号接口会有变更，以下方面会有差异，请留意。

整体的差异
返回值的差异
企业微信的所有接口都会返回 errmsg 和 errcode，所以在判断是否成功时不能以判断是否存在此字段为依据。
访问凭证的差异
企业微信的访问凭证更长，请保留足够的长度，至少为 512 字节。
自建应用的 Secret 差异
企业号每个管理组一个密钥，企业微信每个自建应用对应一个密钥
接口的差异
有部分接口在细节处有所差异，详见以下部分。
管理应用
获取应用
企业号接口 企业微信接口

差异字段名 企业号 企业微信
round_logo_url √ ×
type √ ×
chat_extension_url √ ×
home_url × √
（√ 表示有，× 表示无）

设置应用
企业号接口 企业微信接口

差异字段名 企业号 企业微信
isreportuser √ ×
type √ ×
chat_extension_url √ ×
home_url × √
（√ 表示可设置，× 表示不可设置）

获取应用概况列表
企业号接口 企业微信接口

由于管理组概念的差别，企业微信侧只可获取单个应用、企业号侧可获取多个应用（第三方套件可以获取多个）。
round_logo_url：企业号有，企业微信无
管理通讯录
管理成员
企业号接口 企业微信接口

企业微信侧多了*english_name、isleader、telephone、enable* 字段，没有 weixinid
如果成员已经登录了企业微信，则 mobile 不可修改
请确保同一个部门下的成员数不超过 3 万
管理部门
企业号接口 企业微信接口

通讯录的排序，企业微信与企业号相反
管理标签
企业号接口 企业微信接口

企业号的标签有加锁/解锁的概念，解锁后其他管理组也可以编辑标签
企业微信中创建的标签属于应用，只有该应用才可以编辑标签
管理素材
企业号接口 企业微信接口

企业微信侧不支持永久素材接口
微信支付
企业号接口 企业微信接口

支付接口两侧相同，同样的接口在企业号和企业微信都可兼容
企业付款和企业红包接口完全不同，企业微信的红包仅可在企业微信 app 中接收
JS-SDK
打开企业通讯录选人
企业号接口 企业微信接口

企业微信 APP 侧不支持 openEnterpriseContact 接口，但在微信插件（原企业号）侧仍可继续使用。
企业微信侧提供了 selectEnterpriseContact 接口来替代 openEnterpriseContact 接口。
向当前企业会话发送消息
企业号接口

企业微信暂不支持
第三方授权
企业号接口 企业微信接口

第三方回调的通讯录变更事件有变更
单点登录机制有变更
获取永久授权码、获取企业授权信息，企业微信不会返回 round_logo_url
会话服务接口
企业号接口 企业微信接口

企业号的会话服务接口必须以专有的会话服务 secret 进行调用
企业微信支持任何自建应用调用，且创建的群是特殊的关联了应用的群
企业号支持会话消息的回调，企业微信暂不支持

其它企业微信侧暂不支持接口
客服接口
摇一摇周边接口
卡券接口
