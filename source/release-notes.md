---
date: 2022-12-09
ref_url: https://developer.work.weixin.qq.com/document/path/93262
---

# 更新日志

## 2022-12-01

### 办公能力

#### 概要

- 支持新建文档和表格，可将项目进展、业务数据等通知给成员，提高信息流转效率 详情
- 支持新建收集表，方便收集员工信息 详情
- 支持预约会议和修改会议信息，例如周期性的小组周会、部门例会 详情
- 支持新建日程，可用于面试安排、预约线下会议、项目计划等场景 详情
- 支持唤起日程闲忙视图，方便确定约会时间 详情
- 支持发送普通邮件、日程邮件及会议邮件，用于企业招聘、通知公告等场景 详情
- 支持新建微盘共享空间，可用于企业内资料共享、文件公示等场景 详情

### 邮件

#### 服务端 API

- 变更接口 支持自建应用、代开发应用、第三方应用调用邮箱相关接口 详情
- 新增接口 支持发送普通、日程、会议邮件 详情
- 新增接口 支持分页获取收件箱下，指定时间范围内的邮件 id 列表 详情
- 新增接口 支持指定单个邮件 id，获取邮件 eml 数据 详情
- 新增接口 支持更新应用邮箱帐号 详情
- 新增接口 支持查询应用邮箱帐号 详情

#### 服务端回调

- 新增事件 应用邮箱接收邮件事件 详情

### 文档

#### 服务端 API

- 新增接口 支持新建文档 详情
- 新增接口 支持对指定文档、收集表进行重命名 详情
- 新增接口 支持删除指定文档、收集表 详情
- 新增接口 支持获取指定文档的基础信息 详情
- 新增接口 支持获取文档的分享链接 详情
- 新增接口 支持获取文档权限信息 详情
- 新增接口 支持修改文档查看规则 详情
- 新增接口 支持修改文档通知范围及权限 详情
- 新增接口 支持修改文档安全设置 详情
- 新增接口 支持创建收集表 详情
- 新增接口 支持编辑收集表 详情
- 新增接口 支持读取收集表的信息 详情
- 新增接口 支持获取收集表的统计信息、已回答成员列表和未回答成员列表 详情
- 新增接口 支持读取收集表答案 详情

#### 服务端回调

- 新增事件 修改文档成员事件 详情
- 新增事件 删除文档事件 详情
- 新增事件 收集表完成事件 详情

### 日程

#### 服务端 API

- 变更接口 新增日历管理员，不再支持组织者相关字段 详情
- 变更接口 新增日程管理员，不再支持组织者相关字段，不再支持发起群聊、非参与者主动加入日程 详情

#### JS-SDK

- 新增接口 查看其他成员日程中指定时间段内的闲忙状态 详情

#### 小程序

- 新增接口 查看其他成员日程中指定时间段内的闲忙状态 详情

### 会议

#### 服务端 API

- 变更接口 支持代开发应用配置会议接口权限 详情
- 变更接口 创建会议可指定会议所属日历，新增管理员字段，不再支持发起者字段，不再支持外部联系人相关字段，不可设置主动加入 详情
- 变更接口 会议支持修改所属日历，不再支持外部联系人相关字段，不可设置主动加入 详情
- 变更接口 不再支持获取通过企业微信客户端和腾讯会议 APP 创建的会议列表 详情
- 变更接口 不再支持获取通过企业微信客户端和腾讯会议 APP 创建的会议列表。新增管理员字段，不再支持发起者字段，外部联系人相关字段发生变更 详情

#### 服务端回调

- 新增事件 修改会议事件 详情
- 新增事件 取消会议事件 详情

#### JS-SDK

- 变更接口 不再返回 meetingId 字段 详情

#### 小程序

- 变更接口 不再返回 meetingId 字段 详情
  微盘

#### 服务端 API

- 变更接口 微盘接口操作维度由成员变更为应用，无需再指定 userid，支持自建应用调用微盘相关接口 详情
- 变更接口 空间不再支持相册类型，不再支持配置权限自定义组合 详情
- 变更接口 不再支持配置权限自定义组合，不再支持成员邀请和修改文件分享设置 详情

- 新增接口 支持获取空间信息 详情

- 变更接口 文件权限不再支持配置权限自定义组合 详情

- 新增接口 支持获取文件的权限信息 详情

- 新增接口 支持修改文件安全设置，水印相关设置 详情

#### 服务端回调

- 新增事件 解散空间事件 详情
- 新增事件 修改空间成员事件 详情
- 新增事件 修改空间安全设置事件 详情

### 审批

#### 服务端 API

- 新增接口 支持创建审批模板 详情
- 新增接口 支持更新审批模版 详情

### 基础能力

#### JS-SDK

- 变更接口 分享接口支持 ID 转译功能 详情

- 新增接口 支持屏幕保持常亮 详情

- 新增接口 支持从会话选择文件 详情

### 上下游

#### 服务端 API

- 变更接口 获取企业详情列表接口，支持分页查询，支持查询未加入的企业 详情
- 变更接口 获取企业信息接口，支持查询未加入的企业 详情

### 客户联系

#### 服务端 API

- 新增接口 支持终止尚未发送的朋友圈发表任务 详情

- 变更接口 增加 allow_select 参数，允许成员在待发送客户列表中重新选择发送客户 详情

- 新增接口 重新触发群发通知，提醒成员完成群发任务 详情

- 新增接口 支持取消尚未发送给客户的群发任务 详情

### 微信客服

### 服务端 API

- 变更接口 获取客服帐号列表接口，支持查看账号管理权限 详情
- 变更接口 读取消息接口，支持指定拉取某个客服账号的消息，支持视频号小店订单、商品类型消息 详情
- 变更接口 进入会话事件，客户从视频号小店和视频号进入时，返回更详细的来源信息 详情
- 变更接口 获取客户基础信息，支持客户从视频号小店和视频号进入时，查看更详细的来源信息 详情

#### 服务端回调

变更事件 新增 OpenKfId 字段 详情

- 新增事件 客服账号授权变更事件 详情
  第三方应用

#### 服务端回调

- 新增事件 授权组织架构权限通知事件 详情
  智慧硬件

#### JS-SDK

- 新增接口 支持发起文件打印 详情

#### 小程序

- 新增接口 支持发起文件打印 详情

## 2022-10-09

### 基础能力

#### 服务端 API

- 新增接口 支持异步上传 200M 的视频，用于客户群的入群欢迎语素材 详情

### 效率工具

日程

#### 服务端 API

- 变更接口 支持创建公共日历与全员日历 详情
- 变更接口 支持使用 op_mode 和 op_start_time 来更新和修改重复日程 详情
- 变更接口 支持设置仅日程组织人可创建群聊，从而避免参与人误操作创建群聊 详情

### 微盘

#### 服务端 API

- 变更接口 第三方与代开发应用也可以调用空间管理的相关接口 详情
- 变更接口 第三方与代开发应用也可以移动文件与获取文件信息 详情
- 变更接口 第三方与代开发应用也可以调用文件权限的相关接口，包括新增成员、删除成员、分享设置 详情

#### 服务端回调

- 新增事件 当企业授权安装了具有微盘权限的第三方或代开发应用，企业微信会向应用回调通知特定的事件，包括容量不足事件、空间变更事件、文件变更事件 详情

### OA

### 审批

#### JS-SDK

- 新增接口 审批控件支持配置为应用的页面，由应用提供单选或多选，用户操作后再调用 jsapi 将结果保存到审批中 详情

### 上下游

#### JS-SDK

- 变更接口 创建上下游会话，支持下游企业成员邀请其他下游企业的成员 详情
- 变更接口 变更上下游会话，支持下游企业成员邀请其他下游企业的成员 详情

### 小程序

- 变更接口 创建上下游会话，支持下游企业成员邀请其他下游企业的成员 详情
- 变更接口 变更上下游会话，支持下游企业成员邀请其他下游企业的成员 详情
  家校沟通
  学生支持手机号

#### 服务端 API

- 变更接口 创建学生支持添加手机号 详情
- 变更接口 更新学生支持修改手机号 详情
- 变更接口 批量创建学生支持添加手机号 详情
- 变更接口 批量更新学生支持修改手机号 详情
  第三方应用
  通讯录展示组件
  通讯录展示组件支持展示成员的别名 详情

#### 服务端 API

- 变更接口 文件中的通讯录 ID 转译，支持 userid 转译为成员别名，以及跨企业的转译 详情
- 变更接口 通讯录 userid 排序接口，支持按别名进行排序 详情
- 变更接口 发送应用消息接口，支持将 userid 转译为别名 详情
- 变更接口 通讯录搜索接口，支持搜索出已离职的成员 详情
  ID 转换

#### 服务端 API

- 新增接口 客户标签 ID 的转换接口，可将客户联系中的客户标签 ID 转换成服务商主体下的 ID 详情
- 新增接口 微信客服 ID 的转换接口，可将微信客服 ID 转换成服务商主体下的 ID 详情
  智慧硬件

#### 服务端 API

- 新增接口 第三方应用可获取企业授权的硬件设备列表 详情
- 新增接口 第三方应用可获取设备的考勤打卡原始数据 详情
- 新增接口 第三方应用可获取设备的温度检测记录 详情
- 新增接口 第三方应用可获取设备的门禁设备通行记录 详情
- 新增接口 第三方应用可获取企业已设置的门禁规则 详情
- 新增接口 第三方应用可向企业微信写入企业的门禁规则 详情
- 新增接口 第三方应用可修改企业已有的门禁规则 详情
- 新增接口 第三方应用可删除企业已有的门禁规则 详情

#### 服务端回调

- 新增事件 企业对设备数据的授权发生变更时，回调通知对应的第三方应用 详情

## 2022-08-11

通讯录管理

#### 服务端 API

通讯录同步接口调整，以加固企业通讯录安全 详情

### 微信客服

#### 服务端 API

- 新增接口 支持知识库分组管理 详情
- 新增接口 支持知识库问答管理 详情

- 变更接口 支持菜单消息插入换行和文本 详情

#### 服务端回调

- 新增事件 微信用户撤回消息事件 详情
- 新增事件 接待人员撤回消息事件 详情

### OA

#### 服务端 API

- 变更接口 获取企业假期管理配置，新增返回额度计算规则与假期过期规则 详情
- 变更接口 获取成员假期余额，新增返回假期的实际发放时长 详情

- 新增接口 支持企业为打卡人员补卡 详情

### 效率工具

#### 服务端 API

- 新增接口 支持将文件分块上传到微盘 详情

#### JS-SDK

- 新增接口 第三方应用可调起微盘和文档选择器，以完成上传、下载与分享功能 详情

### 小程序

- 新增接口 第三方应用可调起微盘和文档选择器，以完成上传、下载与分享功能 详情
  企业支付

#### 服务端 API

- 新增接口 可获取对外收款项目中每笔收款的商户单号 详情

#### JS-SDK

- 新增接口 可在应用页面中发起对外收款 详情
- 新增接口 可在应用页面中发起退款 详情

### 小程序

- 新增接口 可在应用页面中发起对外收款 详情
- 新增接口 可在应用页面中发起退款 详情
  上下游

#### 服务端 API

- 变更接口 支持获取企业的认证与验证状态 详情

#### JS-SDK

- 新增接口 上下游聊天工具栏可获取当前互联群的群 ID 详情

### 小程序

- 新增接口 上下游聊天工具栏可获取当前互联群的群 ID 详情

## 2022-06-21

基础能力

#### 服务端 API

- 新增事件 设置工作台自定义展示的 webview 类型，支持指定 webview 内可点击跳转等 详情
  客户联系

#### 服务端 API

- 新增接口 支持分配在职成员的客户群 详情
  上下游

#### 服务端 API

- 新增接口 支持批量导入上下游联系人 详情
- 新增接口 支持将企业从上下游中移除 详情
- 新增接口 支持获取上下游中指定企业的分组与自定义 ID 详情

- 变更接口 获取上下游通讯录分组接口，支持获取某个指定的分组 详情

#### 服务端回调

- 新增事件 创建上下游空间事件 详情
- 新增事件 更新上下游空间事件 详情
- 新增事件 删除上下游空间事件 详情
- 新增事件 新增上下游分组事件 详情
- 新增事件 更新上下游分组事件 详情
- 新增事件 删除上下游分组事件 详情
- 新增事件 企业加入上下游事件 详情
- 新增事件 将企业更新分组事件 详情
- 新增事件 移除企业事件 详情

#### JS-SDK

- 变更接口 上下游聊天工具栏可获取当前联系人 userid 详情
- 变更接口 上下游聊天工具栏可分享消息到当前会话 详情

### 小程序

- 变更接口 上下游聊天工具栏可获取当前联系人 userid 详情
- 变更接口 上下游聊天工具栏可分享消息到当前会话 详情
  家校沟通

#### 服务端 API

- 变更接口 发送「学校通知」支持发送给学生 详情

- 新增接口 家校 oauth2 接口，专用于家长与学生在微信端访问 oauth2 链接时获取身份信息 详情

- 新增接口 获取观看直播统计，支持学生的统计 详情

- 新增接口 获取未观看直播统计，支持学生的统计 详情

#### JS-SDK

- 变更接口 获取当前客户群的群 ID 接口，支持在学生群工具栏中的调用 详情
- 变更接口 分享消息到当前会话接口，支持在学生群工具栏中的调用 详情

### 小程序

- 变更接口 获取当前客户群的群 ID 接口，支持在学生群工具栏中的调用 详情
- 变更接口 分享消息到当前会话接口，支持在学生群工具栏中的调用 详情

## 2022-04-29

### 客户联系

#### 服务端 API

- 变更接口 获取客户详情接口：若客户来源于视频号，则返回视频号添加场景（主页或直播间） 详情
- 变更接口 批量获取客户详情接口：若客户来源于视频号，则返回视频号添加场景（主页或直播间） 详情

### 微信客服

#### 服务端 API

- 变更接口 获取客服帐号列表接口支持分页拉取 详情
- 变更接口 添加接待人员接口支持按部门配置接待人员 详情
- 变更接口 删除接待人员接口支持按部门删除接待人员 详情
- 变更接口 获取接待人员列表接口返回接待人员部门的 id 详情
  上下游

#### 服务端 API

- 变更接口 获取上下游列表接口支持上下游系统应用调用 详情
- 变更接口 获取上下游通讯录分组接口支持上下游系统应用调用 详情
- 变更接口 获取企业上下游通讯录分组下的企业详情列表接口支持上下游系统应用调用 详情

- 新增接口 获取上下游对接规则 id 列表 详情

- 新增接口 新增上下游对接规则 详情

- 新增接口 删除上下游对接规则 详情

- 新增接口 更新上下游对接规则 详情

- 新增接口 获取上下游对接规则详情 详情

第三方应用

#### 服务端 API

- 变更接口 获取企业永久授权码接口不返回企业主体名称 详情
- 变更接口 获取企业授权信息接口不返回企业主体名称 详情

## 2022-03-12

基础能力

#### JS-SDK

- 变更接口 打开已有群聊并发送消息接口，桌面端也支持发送消息 详情
  客户联系

#### 服务端 API

- 变更接口 获取客户详情接口，若客户来源于视频号，则返回视频号名称 详情
- 变更接口 批量获取客户详情接口，若客户来源于视频号，则返回视频号名称 详情
- 变更接口 代开发应用转换 external_userid 接口，支持客户群成员的转换 详情

### 微信客服

#### 服务端 API

- 新增接口 可获取「客户数据统计」企业汇总数据 详情
- 新增接口 可获取「客户数据统计」接待人员明细数据 详情

- 变更接口 读取消息接口，可按需选择返回 amr 或 silk 格式的语音消息 详情
- 变更接口 用户进入会话事件，若微信客户从视频号进入，则返回视频号名称 详情
- 变更接口 获取客户基础信息，返回 48 小时内最后一次进入会话的来源信息 详情

### OA

#### 服务端 API

- 变更接口 更新日程接口，支持传入 skip_attendees 参数，以避免覆盖参与者列表 详情
- 变更接口 会议室预定信息增加预定状态 status 字段 详情
  效率工具
  企业微信邮件 API 开始灰度测试，企业可以通过接口更加高效地管理邮件群组、业务邮箱等功能。

#### 服务端 API

- 新增接口 管理邮件群组相关的接口，可以创建、更新、删除、获取邮件群组等 详情
- 新增接口 管理业务邮箱相关的接口，可以创建、更新、删除、获取业务邮箱等 详情
- 新增接口 禁用/启用邮箱，可以操作成员邮箱和业务邮箱 详情
- 新增接口 可获取与更改用户功能属性 详情
- 新增接口 可获取指定成员邮箱当前未读邮件数量 详情

### 家校应用

#### 服务端 API

- 变更接口 健康上报获取用户填写答案，新增返回填写时间与行程卡类型 详情
  政民沟通
  新增防疫场所码接口

#### 服务端 API

- 新增接口 可获取场所码列表 详情
- 新增接口 可获取场所码的上报问卷 详情
- 新增接口 可获取场所码的上报明细 详情
  第三方应用

#### JS-SDK

- 新增接口 可让管理员打开应用管理页面，快速进行修改可见范围等操作 详情
- 新增接口 可让用户可快速打开应用评价页面 详情

### 小程序

- 新增接口 可让管理员打开应用管理页面，快速进行修改可见范围等操作 详情
- 新增接口 可让用户可快速打开应用评价页面 详情

## 2022-01-10

企业通讯录

#### 服务端 API

- 新增接口 第三方应用新增组织架构信息权限，可以获取部门组织架构以及上级身份 详情
- 新增接口 可获取指定部门的全部子部门 ID 列表 详情
- 新增接口 可获取单个部门详情，包括部门负责人 详情

- 变更接口 创建成员接口，可以指定企业邮箱 biz_mail 详情
- 变更接口 更新成员接口，可以指定企业邮箱 biz_mail 详情
- 变更接口 读取成员接口，新增返回企业邮箱 biz_mail 详情
- 变更接口 获取部门成员详情，新增返回企业邮箱 biz_mail 详情
- 变更接口 异步导出成员详情接口，新增返回企业邮箱 biz_mail 详情
- 变更接口 增量更新成员接口，可以指定企业邮箱 详情
- 变更接口 全量覆盖成员接口，可以指定企业邮箱 详情

#### 服务端回调

变更事件 新增和变更成员事件，增加企业邮箱 BizMail 字段 详情
客户联系

#### 服务端 API

- 新增接口 企业可通过接口配置客户群「加入群聊」的方式 详情
  自建应用代开发

#### 服务端 API

- 新增接口 可以通过接口获取代开发应用的带参授权链接 详情

- 变更接口 企业管理员通过带参链接授权代开发应用之后，获取企业永久授权码时返回 state 值 详情
- 变更接口 获取指定的应用详情接口，新增返回代开发应用的发布状态 customized_publish_status 详情

#### 服务端回调

变更事件 企业管理员通过带参链接授权代开发应用之后，授权通知事件返回 State 字段 详情
第三方应用

#### 服务端 API

- 新增接口 获取带参的应用二维码 详情

- 变更接口 企业用户通过带参的应用二维码安装应用之后，获取企业永久授权码时返回 state 值 详情

#### 服务端回调

变更事件 企业用户通过带参的应用二维码安装应用之后，授权通知事件返回 State 字段 详情
上下游
企业微信针对多个企业之间的协作场景推出「上下游」功能，上下游之间的企业可以共享自建应用和第三方应用 详情
效率工具

#### 服务端 API

- 新增接口 可以增加日程的参与者 详情
- 新增接口 可以删除日程的部分参与者 详情

## 2021-12-17

企业通讯录
第三方应用获取成员性别需要本人授权

#### 服务端 API

- 变更接口 读取成员接口，对第三方应用返回的 gender 为 0，即未定义 详情
- 变更接口 获取部门成员详情，对第三方应用返回的 gender 为 0，即未定义 详情
- 变更接口 第三方异步导出通讯录时，导出结果里的 gender 为 0，即未定义 详情
- 变更接口 第三方应用需要先申请“性别”敏感字段权限，且 oauth2 链接的 scope 值为 snsapi_privateinfo，才能获取到成员的性别 详情

#### 服务端回调

变更事件 成员新增与变更回调事件，第三方应用得到的 Gender 为 0，即未定义 详情

### 小程序

- 变更接口 第三方应用需要先申请“性别”敏感字段权限，且成员同意授权才能获取到成员性别 详情
  客户联系

#### 服务端 API

- 变更接口 获取客户详情接口，对第三方应用返回的 gender 为 0，即未定义 详情

- 新增接口 批量获取客户详情接口，对第三方应用返回的 gender 为 0，即未定义 详情

### 微信客服

#### 服务端 API

- 变更接口 获取客户基础信息接口，对第三方应用返回的 gender 为 0，即未定义 详情

### OA

#### 服务端 API

- 新增接口 可根据会议 ID 查询会议室预订详情 详情

#### 服务端回调

- 新增事件 会议室预定事件 详情
- 新增事件 会议室取消事件 详情

### 基础能力

### 小程序

支持更多微信### 小程序 API 详情
支持更多微信### 小程序组件 详情

## 2021-11-19

基础能力
企业微信帐号 ID 安全性全面升级 详情

#### 服务端 API

- 变更接口 临时素材接口支持上传 10M 的图片 详情
- 变更接口 支持所有第三方应用设置工作台自定义展示 详情
- 变更接口 第三方应用模板卡片消息支持 id 转译 详情

#### JS-SDK

- 变更接口 第三方应用分享消息到当前会话，支持分享企业已关联的### 小程序 详情

### 小程序

- 变更接口 第三方应用分享消息到当前会话，支持分享企业已关联的### 小程序 详情
- 变更接口 ### 小程序的内嵌 webview 支持调用 jssdk 录音接口 详情

### 企业通讯录

通讯录成员可指定直属上级

#### 服务端 API

- 变更接口 创建成员可指定直属上级 详情
- 变更接口 读取成员接口，返回“直属上级” 详情
- 变更接口 更新成员可指定直属上级 详情
- 变更接口 获取部门成员详情接口，返回“直属上级” 详情
- 变更接口 获取部门列表接口，返回“部门负责人” 详情

#### JS-SDK

- 变更接口 返回 ticket 的选人接口，可传入不在应用可见范围的 selectedOpenUserIds 详情

### 小程序

- 变更接口 返回 ticket 的选人接口，可传入不在应用可见范围的 selectedOpenUserIds 详情
  客户联系

#### 服务端 API

- 变更接口 支持发表纯文本的朋友圈 详情

- 新增接口 支持代开发应用的 external_userid 换为第三方应用的 external_userid 详情

### 微信客服

#### 服务端 API

- 变更接口 接待人员重新接入已结束/已转接会话，返回新的会话事件变更类型 详情

#### JS-SDK

- 变更接口 分享消息到当前会话接口，桌面端支持分享菜单消息 详情

### 小程序

- 变更接口 分享消息到当前会话接口，桌面端支持分享菜单消息 详情

## 2021-09-29

### 客户联系

#### JS-SDK

- 新增接口 支持企业发表内容到客户的朋友圈 详情
- 新增接口 企业与第三方应用可通过接口管理商品图册 详情
- 新增接口 企业与第三方应用可通过接口管理聊天敏感词 详情

### 微信客服

#### 服务端 API

- 新增接口 特定场景下可发送客服欢迎语、提示语和结束语等事件响应消息 详情
- 新增接口 第三方应用可获取企业的视频号绑定状态 详情
- 新增接口 在人工接待中，可通过接口将客户转接给其他接待人员 详情

#### JS-SDK

- 新增接口 打开客服会话时可指定微信客户 ID 详情

### 小程序

- 新增接口 打开客服会话时可指定微信客户 ID 详情
  消息推送

#### 服务端 API

- 变更接口 第三方应用模板消息支持打开### 小程序，并且支持仅发送给未授权的成员 详情
- 变更接口 应用模板卡片消息支持更多的特性了 详情

### 企业通讯录

#### 服务端 API

- 变更接口 通讯录成员的自定义字段、别名字段，长度限制放宽到 64 个字符了 详情

### 基础能力

### 小程序

- 新增接口 支持从企业微信客户端会话选择文件 详情

### OA

#### 服务端 API

- 变更接口 支持第三方应用获取设备打卡数据 详情
  会话内容存档

#### 服务端回调

- 新增事件 企业收到或发送新消息时回调事件到企业指定的 url 详情
  第三方应用

#### 服务端回调

- 新增事件 增加第三方应用管理员变更通知 详情

#### JS-SDK

- 新增接口 第三方可在应用页面内让用户快速打开应用客服的会话 详情

### 小程序

- 新增接口 第三方可在### 小程序应用内让用户快速打开应用客服的会话 详情
  自建应用代开发
  代开发应用增加家校沟通自定义权限 详情

#### 服务端回调

- 新增事件 通讯录变更回调 详情
- 新增事件 修改代开发应用可见范围时，企业微信会回调变更授权通知 详情

## 2021-08-18

企业通讯录

#### 服务端 API

- 新增接口 对于通讯录较大的企业，提供异步导出通讯录的解决方案 详情
- 新增接口 第三方应用获取选人 ticket 对应的用户 详情

#### JS-SDK

- 变更接口 返回 ticket 的选人接口，支持传入默认选中的人员 详情

### 小程序

- 新增接口 返回 ticket 的选人接口，可用于创建群聊或推送模板消息 详情
  客户联系
  客户管理

#### 服务端 API

- 新增接口 客户联系规则组管理接口，可以创建、编辑、删除、获取规则组 详情
- 新增接口 规则组客户标签管理接口 详情
  客户朋友圈

#### 服务端 API

- 新增接口 客户朋友圈规则组管理接口，可以创建、编辑、删除、获取规则组 详情

#### JS-SDK

- 新增接口 发表内容到客户朋友圈 详情
- 新增接口 设置朋友圈封面与签名 详情

### 小程序

- 新增接口 发表内容到客户朋友圈 详情
- 新增接口 设置朋友圈封面与签名 详情
  消息推送

#### 服务端 API

- 变更接口 创建企业群发，附件中支持文件 详情
- 变更接口 获取企业的全部群发记录 ，支持返回文件 详情

#### JS-SDK

- 变更接口 群发消息到客户，附件中支持文件 详情
- 变更接口 群发消息到客户群：附件中支持文件 详情

### 小程序

- 变更接口 群发消息到客户，附件中支持文件 详情
- 变更接口 群发消息到客户群：附件中支持文件 详情
  在职继承

#### 服务端 API

- 变更接口 在职继承频率调整 详情
  统计管理

#### 服务端 API

- 变更接口 获取「群聊数据统计」数据，新增教培群迁移数据 详情
  变更回调

#### 服务端 API

- 新增接口 客户标签顺序重排事件回调 详情
  变更事件 客户标签回调事件支持规则组标签 详情
  变更事件 删除企业客户事件，可通过 Source 区分出在职继承触发的删除事件 详情

### 微信客服

#### JS-SDK

- 变更接口 微信客服工具栏支持 msgmenu 消息（即菜单消息） 详情

- 新增接口 可从页面快速跳转到微信客服消息的界面 详情

### 小程序

- 新增接口 微信客服工具栏支持 msgmenu 消息（即菜单消息） 详情
- 新增接口 可从### 小程序快速跳转到微信客服消息的界面 详情
  消息推送

#### 服务端 API

- 变更接口 发送应用消息接口，支持五种模板卡片类型 详情

- 新增接口 五种新的模板卡片消息允许应用通过接口进行更新 详情

- 变更接口 图文消息支持打开### 小程序 详情

- 新增接口 通过接口下发的应用消息，可以通过接口撤回 详情

#### 服务端回调

- 新增事件 用户点击模板卡片消息中的按钮之后的事件 详情

- 新增接口 当应用收到模板卡片事件推送时，可立即回复模板卡片更新消息 详情

家校沟通

#### 服务端 API

- 新增接口 获取可在微信「学校通知-学校应用」使用该应用的家长范围 详情

- 变更接口 读取学生或家长，老师个人授权的应用只能获取到该老师管理的班级 详情
- 变更接口 获取部门成员详情，老师个人授权的应用只能获取到该老师管理的班级 详情
- 变更接口 获取部门家长详情，老师个人授权的应用只能获取到该老师管理的班级 详情
- 变更接口 获取部门列表，老师个人授权的应用只能获取到该老师管理的班级 详情
- 变更接口 获取外部联系人详情，老师个人授权的应用只能获取到该老师管理的班级 详情
- 变更接口 发送学校通知，老师个人授权的应用只能获取到该老师管理的班级 详情
  政民沟通

#### JS-SDK

- 新增接口 支持从微信中的网页进入居民上报### 小程序 详情

### 小程序

- 新增接口 支持从微信中的### 小程序进入居民上报### 小程序 详情
  自建应用代开发

### 企业通讯录

#### 服务端 API

- 变更接口 读取成员，增加敏感字段授权 详情
- 变更接口 获取部门成员，增加敏感字段授权 详情

- 新增接口 获取部门成员详情，增加敏感字段授权 详情

- 新增接口 获取部门列表，增加敏感字段授权 详情

- 变更接口 获取标签成员，增加敏感字段授权 详情
  客户联系

#### 服务端 API

- 变更接口 获取客户详情，敏感信息需要授权才吐出 详情
- 变更接口 批量获取客户详情，敏感信息需要授权才吐出 详情

### 基础能力

移动端 SDK 支持分享

### 小程序 详情

## 2021-07-14

### 客户联系

#### 服务端 API

- 变更接口 成员对外信息增加了微信视频号名称 详情

- 新增接口 支持将### 小程序在微信获取的 opengid 转换为客户群 ID 详情

- 变更接口 支持获取客户群中客户的名字和在群中的昵称 详情
- 变更接口 发送新客户欢迎语支持文件 详情
- 变更接口 入群欢迎语素材支持文件与视频 详情

#### JS-SDK

- 变更接口 发送消息到会话，支持定义发送后停留在工具栏还是回到会话 详情

### 小程序

- 变更接口 发送消息到会话，支持定义发送后停留在工具栏还是回到会话 详情
  家校应用

#### 服务端 API

- 变更接口 第三方应用支持在 k12 学校的工作台自定义展示 详情

- 新增接口 班级收款获取学生付款结果 详情

#### JS-SDK

- 新增接口 发起班级收款 详情

### 小程序

- 新增接口 发起班级收款 详情

### 教培行业

#### JS-SDK

- 新增接口 群发消息给学员 详情
- 新增接口 群发消息给学员群 详情

### 小程序

- 新增接口 群发消息给学员 详情
- 新增接口 群发消息给学员群 详情

## 2021-06-03

第三方应用
支持成员授权应用 详情

#### 服务端 API

- 新增接口 获取成员授权列表 详情
- 新增接口 查询成员用户是否已授权 详情

- 变更接口 获取永久授权码接口返回企业的授权模式（管理员授权或成员授权） 详情
- 变更接口 获取企业授权信息接口返回企业的授权模式（管理员授权或成员授权） 详情
- 变更接口 应用消息支持模板消息，成员授权模式下支持推送给未授权的成员 详情
- 变更接口 获取应用的管理员列表，成员授权模式下不返回系统管理员列表 详情
- 变更接口 成员授权模式下，读取成员时所属部门列表、主部门都只返回根部门 id，即 1；不返回部门内 order 详情

#### 服务端回调

变更事件 成员通知事件，成员授权模式下，用户所属部门或者主部门只返回根部门 id，即 1 详情
变更事件 管理员对应用的授权模式进行切换时，会触发变更授权通知的回调 详情

#### JS-SDK

- 新增接口 返回 ticket 的选人接口，可用于创建群聊或推送模板消息 详情
- 新增接口 创建群聊并发送消息 详情
- 新增接口 打开已有群聊并发送消息 详情
  会话

#### JS-SDK

- 新增接口 私密消息 详情

### 小程序

- 新增接口 私密消息 详情
  效率工具

#### 服务端 API

- 新增接口 直播观众跳转### 小程序商城时，可获取直播间、观众及观众所属邀请人信息 详情

- 变更接口 获取“推广产品”直播观看明细时，新增观众所属邀请人信息 详情
  企业互联

#### JS-SDK

- 新增接口 创建企业互联会话 详情
- 新增接口 变更互联群成员，可往指定的互联群添加成员 详情

### 小程序

- 新增接口 创建企业互联会话 详情
- 新增接口 变更互联群成员，可往指定的互联群添加成员 详情
  家校应用

#### 服务端 API

- 变更接口 家校通讯录返回班级关联的班级群 ID 和毕业班标记 详情

#### JS-SDK

- 新增接口 支持让老师跳到认领班级的界面 详情
- 新增接口 微信 H5 页面唤起填写学生资料页面 详情

### 小程序

- 新增接口 支持让老师跳到认领班级的界面 详情
- 新增接口 微信### 小程序进入填写学生资料页面 详情
  政民沟通

#### 服务端 API

- 新增接口 添加网格 详情
- 新增接口 编辑网格 详情
- 新增接口 删除网格 详情
- 新增接口 获取网格列表 详情
- 新增接口 获取用户负责及参与的网格列表 详情
- 新增接口 添加事件类别 详情
- 新增接口 修改事件类别 详情
- 新增接口 删除事件类别 详情
- 新增接口 获取事件类别列表 详情

- 变更接口 变更接口 获取巡查上报事件列表新增图片及视频字段 详情
- 变更接口 变更接口 获取巡查上报的事件详情信息新增图片及视频字段 详情
- 变更接口 变更接口 获取居民上报事件列表新增上报人、上报人手机、上报人 unionid、图片及视频字段 详情
- 变更接口 变更接口 获取居民上报的事件详情信息新增上报人、上报人手机、上报人 unionid、图片及视频字段 详情
  其他
  深色模式指引 详情

## 2021-04-02

会话

#### JS-SDK

- 新增接口 应用可隐藏聊天附件栏发送按钮 详情

- 变更接口 获取进入 H5 页面的入口环境支持聊天附件栏 详情
- 变更接口 分享消息到当前会话支持聊天附件栏 详情

### 小程序

- 变更接口 wx.qy.getContext 支持聊天附件栏 详情
- 变更接口 wx.qy.sendChatMessage 支持聊天附件栏 详情

### 客户联系

#### 服务端 API

- 变更接口 拉客户群详情新增邀请人信息 详情
- 变更接口 发送新客户欢迎语支持多附件 详情
- 变更接口 创建企业群发支持多附件 详情
- 变更接口 获取企业的群发记录时，可以导出多个附件了 详情

#### 服务端回调

变更事件 客户群变更事件，增加更详细的信息 详情

#### JS-SDK

- 变更接口 群发消息给客户时，支持传入文本内容和多个附件 详情
- 变更接口 群发消息发送给客户群时，支持传入文本内容和多个附件 详情

### 小程序

- 变更接口 wx.qy.shareToExternalContact 支持多附件 详情
- 变更接口 wx.qy.shareToExternalChat 支持多附件 详情

### 应用消息推送

#### 服务端 API

- 变更接口 任务卡片消息，支持应用回调内容展示 详情

### 效率工具

#### 服务端 API

- 变更接口 直播详情接口新增在线人数和预约人数字段 详情

#### 服务端回调

- 新增事件 新增直播状态回调事件 详情

### 家校应用

#### JS-SDK

- 新增接口 局校互联通讯录选人接口 详情

### 小程序

- 新增接口 wx.qy.selectCorpGroupContact 详情

### OA

#### 服务端 API

- 变更接口 获取员工打卡规则支持第三方 详情
- 变更接口 获取打卡记录数据支持第三方 详情
- 变更接口 获取打卡日报数据支持第三方 详情
- 变更接口 获取打卡月报数据支持第三方 详情
- 变更接口 获取打卡人员排班信息支持第三方 详情
- 变更接口 为打卡人员排班支持第三方 详情
- 变更接口 获取企业假期管理配置支持第三方 详情
- 变更接口 获取成员假期余额支持第三方 详情
- 变更接口 修改成员假期余额支持第三方 详情

基础能力

- 新增接口 打开个人聊天窗口 schema 详情

## 2021-02-04

### 客户联系

#### 1.在职继承

##### 服务端 API

- 新增接口 当成员或客户有变更时，可将在职成员的客户批量转接给其他成员，并查询转接结果 详情

#### 2.离职继承

##### 服务端 API

- 新增接口 成员离职后，可将他的客户和客户群批量转接给其他成员，并查询转接结果 详情

#### 3.消息推送

##### 服务端 API

- 变更接口 添加入群欢迎语素材时，可以通知成员将这条入群欢迎语应用到客户群中了 详情

### 应用消息推送

#### 服务端 API

- 变更接口 企业关联的### 小程序已统一为应用，支持给成员推送图文等更多类型消息等完整应用能力 详情

### 效率工具

#### JS-SDK

- 新增接口 支持获取系统剪贴板内容 详情

### 家校应用

#### 服务端 API

- 变更接口 健康上报新增“收集文件/图片”问题类型 详情

## 2020-12-21

### 客户联系

新增更多接口能力，帮助企业提升客户管理能力和客户运营能力。

1.客户联系

#### 服务端 API

- 变更接口 第三方应用也可以新增和修改企业标签库了 详情

- 新增接口 可以获取企业全部的群发记录了 详情

#### JS-SDK

- 变更接口 使用聊天工具栏时，可在 H5 中将### 小程序直接发送到会话了 详情

  2.客户群

#### 服务端 API

- 变更接口 第三方应用也可以获取客户群列表了 详情
- 变更接口 第三方应用也支持配置入群欢迎语素材了 详情
- 变更接口 第三方应用也支持分配离职成员的客户群了 详情
- 变更接口 第三方应用也支持按照成员与自然日维度获取群聊数据统计了 详情

#### 服务端回调

- 新增事件 新建客户群可以主动回调给企业了 详情
- 新增事件 新建客户群可以主动回调给服务商了 详情
- 新增事件 解散群聊可以主动回调给企业了 详情
- 新增事件 解散群聊可以主动回调给服务商了 详情
- 新增事件 修改群公告也会产生客户群变更回调给企业了 详情
- 新增事件 修改群公告也会产生客户群变更回调给服务商了 详情

  3.客户朋友圈

#### 服务端 API

- 新增接口 可以获取企业全部的客户朋友圈发表记录了 详情

### 效率工具

新增会议、直播等接口能力，帮助企业进一步提高办公效率。

1.会议

#### 服务端 API

- 新增接口 创建预约会议 详情
- 新增接口 修改预约会议 详情
- 新增接口 取消预约会议 详情
- 新增接口 获取成员会议 ID 列表 详情
- 新增接口 获取会议详情 详情

#### JS-SDK

- 新增接口 创建立即会议 详情
- 新增接口 进入会议 详情

### 小程序

- 新增接口 创建立即会议 详情
- 新增接口 进入会议 详情

  2.直播

#### 服务端 API

- 新增接口 创建预约直播 详情
- 新增接口 修改预约直播 详情
- 新增接口 取消预约直播 详情
- 新增接口 删除直播回放 详情
- 新增接口 在微信中观看直播或直播回放 详情
- 新增接口 获取成员直播 ID 列表 详情
- 新增接口 获取直播详情 详情
- 新增接口 获取直播观看明细 详情

#### JS-SDK

- 新增接口 创建立即直播 详情
- 新增接口 观看直播 详情
- 新增接口 观看直播回放 详情
- 新增接口 下载直播回放 详情

### 小程序

- 新增接口 创建立即直播 详情
- 新增接口 观看直播 详情
- 新增接口 观看直播回放 详情
- 新增接口 下载直播回放 详情

  3.日程

#### 服务端 API

- 变更接口 日程相关接口支持自定义重复了 详情
- 变更接口 日程相关接口第三方应用也可以调用了 详情

  4.微盘/微文档

#### 服务端 API

- 新增接口 支持新建文件/微文档了 详情

### OA

新增汇报接口能力，完善打卡、审批的接口能力，助力企业提高 OA 流程效率和管理能力。

1.打卡

#### 服务端 API

- 新增接口 获取企业所有打卡规则 详情

- 变更接口 获取员工打卡规则接口新增排班信息相关字段 详情
- 变更接口 获取打卡记录数据接口新增标准上班/下班打卡时间、假勤状态、规则 id、班次 id、时段 id 等字段 详情

- 新增接口 获取打卡日报数据 详情

- 新增接口 获取打卡月报数据 详情

- 新增接口 获取打卡人员排班信息 详情

- 新增接口 为打卡人员排班 详情

- 新增接口 录入打卡人员人脸信息 详情

  2.审批

#### 服务端 API

- 变更接口 提交审批申请接口新增“申请人所在部门”字段，且控件类型新增位置、关联申请单、公式、时长等类型 详情
- 变更接口 获取审批申请详情接口新增位置、关联申请单、公式、时长等控件类型的数据结构说明 详情

- 新增接口 获取企业假期管理配置 详情

- 新增接口 获取成员假期余额 详情

- 新增接口 修改成员假期余额 详情

  3.汇报

#### 服务端 API

- 新增接口 批量获取汇报记录单号 详情
- 新增接口 获取汇报记录详情 详情
- 新增接口 获取汇报统计详情 详情

### 企业支付

支持对外收款相关接口能力。

#### 服务端 API

- 新增接口 可批量添加多个收款账户了 详情
- 新增接口 可以获取企业全部的收款记录了 详情

### 政民沟通

新增巡查上报、居民上报接口能力，可以帮助政府更好的做事件上报的数据分析和沉淀。

1.巡查上报

#### 服务端 API

- 新增接口 支持拉取巡查上报中配置的网格及网格负责人 详情
- 新增接口 支持拉取单位整体的巡查上报数据概况 详情
- 新增接口 支持拉取个人的巡查上报数据概况 详情
- 新增接口 支持拉取上报事件的分类统计 详情
- 新增接口 支持拉取巡查上报的事件列表 详情
- 新增接口 支持拉取巡查上报的事件详情信息 详情

  2.居民上报

#### 服务端 API

- 新增接口 支持拉取居民上报中配置的网格及网格负责人 详情
- 新增接口 支持拉取单位整体的居民上报数据概况 详情
- 新增接口 支持拉取个人的居民上报数据概况 详情
- 新增接口 支持拉取上报事件的分类统计 详情
- 新增接口 支持拉取居民上报的事件列表 详情
- 新增接口 支持拉取居民上报的事件详情信息 详情

### 企业互联

- 新增接口能力，可以让企业和第三方服务商，基于企业互联开发应用，以供互联企业共同使用。

#### 服务端 API

- 新增接口 获取应用共享信息接口，获取到企业自建应用和第三方应用在企业互联中共享的范围和覆盖的企业 详情
- 新增接口 获取下级企业的 access_token 接口，用于调用应用共享范围内，下级企业通迅录的读取权限 详情
- 新增接口 获取下级企业的### 小程序 session 接口，实现### 小程序应用跨局校使用 详情
- 新增接口 获取下级企业付费版本信息接口，第三方付费应用可通过此接口得知由上级企业统一付费的应用信息 详情

#### 服务端回调

- 新增事件 企业互联自建应用共享关系变动后，支持回调共享应用事件给企业 详情
- 新增事件 企业互联第三方应用共享关系变动后，回调共享应用事件给服务商 详情

## 2020-11-05

- 【### 小程序】新增接口：快速跳转到添加客户的界面 wx.qy.navigateToAddCustomer。详情
- 【### 小程序】新增接口：变更群成员接口 wx.qy.updateEnterpriseChat，可往指定客户群添加成员。详情
- 【### 小程序】变更接口：wx.qy.openEnterpriseChat，可返回 chatId，且支持按指定 chatid 打开已有的客户群。详情
- 【### 小程序】变更接口：wx.qy.getContext 支持家校应用调用。详情
- 【### 小程序】变更接口：wx.qy.getCurExternalChat 支持家校应用调用。详情
- 【### 小程序】变更接口：wx.qy.sendChatMessage 支持家校应用调用。详情

- 【JS-SDK】新增接口：快速跳转到添加客户的界面 navigateToAddCustomer。详情
- 【JS-SDK】新增接口：变更群成员接口 updateEnterpriseChat，可往指定客户群添加成员。详情
- 【JS-SDK】新增接口：跳转到### 小程序接口 launchMiniprogram。详情
- 【JS-SDK】变更接口：openEnterpriseChat，可返回 chatId，且支持按指定 chatid 打开已有的会话。详情
- 【JS-SDK】变更接口：getContext 支持家校应用调用。详情
- 【JS-SDK】变更接口：getCurExternalChat 支持家校应用调用。详情
- 【JS-SDK】变更接口：sendChatMessage 支持家校应用调用。详情

- 【服务端 API】新增接口：互联企业应用相关接口，应用可获取可见范围内其他互联企业的通讯录。详情
- 【服务端 API】变更接口：第三方服务商获取企业永久授权码，无论企业是否新注册，通过扫推广二维码安装的，都返回注册码相关信息。详情

## 2020-09-27

- 【服务端 API】获取客户群统计数据接口，添加支持一次性拉取多个自然日的数据。详情
- 【服务端 API】新增接口：获取客户群统计数据并按自然日聚合。详情

## 2020-09-21

- 【服务端 API】新增“批量获取客户详情”，可根据成员 userid 批量获取客户的详情。详情

## 2020-09-18

- 【服务端 API】原“离职成员的外部联系人再分配”接口，调整为支持在职成员的客户分配。详情

## 2020-09-14

- 【服务端 API】新增“微盘接口”，企业可以通过微盘相关接口，对微盘的文件进行操作和设置权限。详情

## 2020-09-02

- 【服务端 API】“创建日历”接口，增加 readonly 参数，可以允许员工在上面进行修改/创建日程等操作；增加 set_as_default 参数，可以将日历设置为员工的默认日历。详情
- 【服务端 API】“更新日历”接口，增加 readonly 参数，可以允许员工在上面进行修改/创建日程等操作。详情
  【服务端回调】新增“日历与日程变更事件”的回调（仅通过 api 创建的日历有回调事件）。详情

## 2020-08-25

【服务端回调】新增“客户接替失败事件”回调。详情

- 【服务端 API】增加“查询客户接替结果”接口，详情

## 2020-07-27

- 【服务端 API】“获取客户群详情”接口返回 unionid 字段，详情
- 【服务端 API】增加“会议室管理”与“会议室预订管理”接口，详情
- 【JS-SDK】chooseImage 接口可以通过 defaultCameraMode 参数指定默认使用前置摄像头，详情
- 【JS-SDK】「监听地理位置变化」接口当用户关闭了 GPS 时，返回 auto:location:report:fail, gps closed.详情

## 2020-06-15

- 【服务端 API】新增“健康上报”接口，详情
- 【服务端 API】新增“企业直播”接口，详情
- 【服务端 API】新增“设置工作台自定义展示”接口，详情
- 【服务端 API】群机器人接口支持发送文件类型消息，详情
- 【服务端 API】“添加企业群发消息任务”接口，图片类型支持通过“上传图片”接口得到的 url，详情
- 【服务端 API】“发送新客户欢迎语”接口，图片类型支持通过“上传图片”接口得到的 url，详情
- 【服务端 API】“群欢迎语素材管理”接口，图片类型支持通过“上传图片”接口得到的 url，详情
- 【服务端 API】“获取客户详情”接口，新增添加来源字段的返回，详情
- 【JS-SDK】新增 getContext 接口，可用于获取进入 H5 页面的入口环境，详情
- 【JS-SDK】创建会话接口 wx.openEnterpriseChat，包含微信联系人的外部群最多支持 40 人，详情
- 【### 小程序】新增 wx.qy.getContext 接口，可用于获取进入### 小程序的入口环境，详情
- 【### 小程序】创建会话接口 wx.qy.openEnterpriseChat，包含微信联系人的外部群最多支持 40 人，详情

## 2020-03-31

- 【服务端 API】“修改客户备注信息”接口，现在已支持第三方调用。详情
- 【服务端 API】“编辑客户企业标签”接口，现在已支持第三方调用。详情
- 【服务端 API】“添加企业群发消息任务”接口，现在已支持第三方调用。详情
- 【服务端 API】“配置客户联系「联系我」方式”接口，单个企业创建数量限制现已提升至 50 万个。详情
- 【服务端回调】新增“编辑企业客户事件”回调。详情
- 【JS-SDK】增加“将 H5 页面通过群发助手发送给客户群”接口。详情
- 【JS-SDK】“获取当前外部联系人 userid”接口，现在已支持第三方调用。详情
- 【JS-SDK】“获取当前客户群的群 ID”接口，现在已支持第三方调用。详情
- 【JS-SDK】“通过聊天工具栏向用户发送消息”接口，现在已支持第三方调用。详情
- 【### 小程序】增加“将### 小程序通过群发助手发送给客户群”接口。详情
- 【### 小程序】增加“获取当前客户群的群 ID”接口。详情
- 【### 小程序】增加“通过聊天工具栏向用户发送消息”接口。详情
- 【### 小程序】“获取当前外部联系人 userid”接口，现在已支持第三方调用。详情

## 2020-03-14

- 【服务端 API】“配置客户联系「联系我」方式”相关接口，新增支持配置临时会话模式。详情

## 2020-01-15

- 【服务端 API】“日程”接口，新增支持日历本。详情

## 2019-12-23

- 【服务端 API】新增“获取客户群列表”接口，详情
- 【服务端 API】新增“获取客户群详情”接口，详情
- 【服务端 API】新增“群欢迎语素材管理”接口，详情
- 【服务端 API】新增“离职成员的群再分配”接口，详情
- 【服务端 API】新增“获取客户群统计数据”接口，详情
- 【服务端回调】新增“客户群变更事件”回调，详情
- 【服务端 API】新增“日程接口”，详情

## 2019-10-23

- 【服务端 API】企业微信打卡，新增“获取打卡数据”接口返回值新增经纬度信息，详情
- 【服务端 API】企业微信审批，新增概述文档，新增“获取审批模板详情”、“提交审批申请”、“审批申请状态变化回调通知”、“分类获取审批编号”、“获取审批申请详情”等接口，详情

## 2019-10-15

- 【服务端 API】为方便开发者查阅文档，对外部联系人管理相关接口的文案做了调整，将部分“外部联系人”修改为“客户”，详情
- 【服务端回调】新增“外部联系人免验证添加成员”事件，详情
- 【服务端回调】向第三方回调“添加企业客户”和“外部联系人免验证添加成员”时，增加“欢迎语 code”字段，详情
- 【服务端 API】“发送新客户欢迎语”接口支持第三方调用，详情
- 【服务端 API】新增“管理企业客户标签”接口，详情

## 2019-08-01

- 【服务端 API】变更“添加企业群发消息模板”接口，取消了 “无法向未回复消息的客户发送企业群发消息” 的限制，详情
  【服务端回调】外部联系人管理增加“删除跟进成员事件”回调，详情
  【JS-SDK】增加“聊天工具栏分享消息到会话”接口，详情
  【JS-SDK】“获取当前外部联系人 userid”支持在聊天工具栏进入页面时调用，详情

## 2019-06-28

- 【服务端 API】新增“获取企业标签库”接口，详情
- 【服务端 API】新增“编辑外部联系人企业标签”接口，详情
- 【服务端 API】新增“获取加入企业二维码”接口，详情
- 【服务端 API】新增“手机号获取 userid”接口，详情
- 【服务端 API】### 小程序通知消息，不再通过统一会话【### 小程序通知】发给用户，用户将在各个独立的### 小程序应用中收到消息，详情
- 【服务端 API】新增群机器人消息接口，详情
  【JS-SDK】新增“将 H5 页面通过个人群发发送给客户”接口，详情
  【### 小程序】新增“群发助手接口”接口，详情

## 2019-06-17

- 【服务端 API】支持自建应用调用外部联系人管理接口，详情

## 2019-05-23

- 【服务端 API】增加“发送新客户欢迎语”接口，详情
- 【服务端 API】“添加企业群发消息模板”接口支持指定一个发送人 sender，详情
- 【服务端 API】对外部联系人相关的接口调用 URL 进行了调整，详情
  【服务端回调】添加外部联系人事件增加“欢迎语 code”字段，详情
  【### 小程序】增加“转发成功回调”接口，详情

## 2019-04-24

- 【服务端 API】增加“获取员工对外联系的行为数据”接口，详情
- 【服务端 API】“发送应用消息”接口增加“任务卡片消息”类型，详情

## 2019-03-18

- 【服务端 API】“添加企业群发消息模板”接口现在支持第三方调用，详情
- 【服务端 API】增加“获取企业群发消息发送结果”接口，详情
- 【服务端 API】增加“获取离职成员的客户列表”接口，详情

## 2019-03-11

- 【服务端 API】通讯录接口支持设置地址，详情
- 【服务端 API】获取外部联系人详情接口增加以下信息：备注企业名、备注手机号、标签，详情
- 【服务端 API】增加“配置客户联系「联系我」方式”相关接口，详情
- 【服务端 API】增加“添加企业群发消息模板”接口，详情
- 【服务端 API】增加“获取配置了客户联系功能的成员列表”接口，详情
  【服务端回调】通讯录变更事件增加“地址”字段，详情
  【服务端回调】### 小程序应用支持关注与取消关注事件的回调，详情
  【JS-SDK】更新 chooseImage 接口，增加 isSaveToAlbum 参数，控制拍照时是否自动保存到系统相册，详情
  【JS-SDK】增加“语音转文字接口”接口，详情
  【### 小程序】增加“语音转文字接口”接口，详情
  【### 小程序】支持“微信运动”接口，详情

## 2019-01-07

- 第三方服务商获取企业永久授权码与获取企业授权信息，支持返回代理商信息

## 2018-12-21

- 应用消息支持 markdown 类型，详情
- 通讯录接口支持设置企业对外简称，详情
- 通讯录接口支持设置成员所在部门内是否为上级，以及网页类型的自定义字段，详情
- 通讯录变更事件增加“所在部门内是否为上级”字段，以及网页类型的自定义字段，详情
- 增加“获取外部联系人列表”接口，详情
- 增加“外部联系人变更回调”， 查看企业回调事件， 查看第三方回调事件

- 小程序，增加“视频会议”接口，详情

- 小程序，增加“无线投屏”接口，详情

变更“读取成员”接口，返回的 department 仅包含有查看权限的部门 id，详情

## 2018-11-01

- 小程序，增加 wx.qy.canIUse 接口，用于判断企业微信专有接口在当前版本是否可用，详情

- 小程序，增加 NFC 相关的接口，详情

## 2018-09-25

- JS-SDK，更新“通讯录选人接口”，支持 fromDepartmentId 传某个部门 id，以从指定部门开始展示，详情

- JS-SDK，增加“获取当前外部联系人 userid”（内测），详情

- JS-SDK，增加硬件接口-添加设备，详情

- JS-SDK，增加硬件接口-视频会议-查询当前是否在视频会议详情

- JS-SDK，增加硬件接口-视频会议-加入视频会议详情

- 小程序，增加“获取当前外部联系人 userid”（内测），详情

- 小程序，支持更多的接口与组件，详情

增加“离职成员的外部联系人再分配”接口（内测），详情
增加“获取公费电话拨打记录”接口，详情
增加“互联企业应用发送消息”接口，详情
增加“互联企业应用接口消息与事件”的回调，详情
变更“成员管理”相关接口，支持设置“对外职务”字段，查看接口详情：创建成员、读取成员、更新成员、获取部门成员详情
增加自建应用、第三方应用“审批流程引擎”相关能力，详情：自建应用审批流程引擎、第三方应用审批流程引擎

## 2018-09-11

- JS-SDK，增加硬件接口-发起无线投屏，详情

## 2018-09-03

- JS-SDK，增加蓝牙/低功耗蓝牙/iBeacon 接口，详情

## 2018-08-31

更新“发送应用消息”接口，mpnews 消息的 safe 参数可设值为 2，表示仅限在企业内分享，详情
更新“通讯录管理”接口，english_name 字段调整为 alias(旧企业仍然兼容 english_name 字段)，可传中文字符，详情

## 2018-08-29

- JS-SDK，增加“agentConfig”接口，用于注入第三方应用的权限，详情
- JS-SDK，增加“用户截屏事件”接口，详情

## 2018-08-27

- 第三方应用授权，变更“获取永久授权码”接口，新增 location 返回字段，详情
- 第三方应用授权，变更“获取企业授权信息”接口，新增 location 返回字段，详情

## 2018-08-15

- 小程序通知消息支持批量发送，详情

## 2018-07-19

- 小程序，wx.login、wx.checkSession 与 wx.getUserInfo 有变更，详情
- 小程序，增加“获取企业成员头像”接口，详情
- 小程序，增加“获取企业成员个人二维码”接口，详情
- 小程序，增加“获取企业成员手机号”接口，详情
- 小程序，增加“获取企业成员邮箱地址”接口，详情
- 小程序，增加“打开通讯录选人”接口，详情
- 小程序，增加“创建会话”接口，详情
- 小程序，增加“打开外部联系人列表选人”接口，详情
- 小程序，增加“打开个人信息页”接口，详情

发送应用消息，支持“### 小程序通知消息”类型，详情
第三方服务商支持关联### 小程序，详情

## 2018-06-25

- JS-SDK，变更“外部联系人选人接口”，增加参数 filterType，可控制仅展示未选择过的联系人，详情

## 2018-06-07

注册定制化，查询注册状态，注册完成回调事件不返回管理员手机号和邮箱。

## 2018-06-01

- JS-SDK，增加“打开持续定位接口”，详情
- JS-SDK，增加“停止持续定位接口”，详情
- JS-SDK，增加“监听地理位置变化”接口，详情
- JS-SDK，变更“拍照或从手机相册中选图接口”，可选择进入拍照界面时默认的拍照模式（单拍或连拍），详情
- JS-SDK，变更“标记为企业客户接口”，接口名改为 selectExternalContact，接口返回 userIds，详情
- JS-SDK，增加“打开个人信息页接口”，详情
- JS-SDK，变更“创建会话接口”，参数 openIds 改名为 externalUserIds，详情

增加“获取外部联系人详情”接口，详情
废弃“获取企业客户列表”接口，查看调整详情
废弃“关联企业客户库-获取外部联系人信息”接口，查看调整详情

## 2018-05-07

- JS-SDK，增加“监听网络状态变化”接口，详情
- JS-SDK，变更“创建会话”接口，支持传入外部联系人，详情

增加“企业客户变更事件”的回调，详情
支持第三方调用“获取企业客户列表”接口，详情

## 2018-05-03

更新：审批 API 单次拉取上限修改为 100 条，可以通过多次拉取的方式来满足需求。详情

## 2018-04-25

网页授权登录之后使用 user_ticket 获取成员详情，增加个人二维码字段，详情
网页授权登录第三方之后使用 user_ticket 获取成员详情，增加个人二维码字段，详情

## 2018-04-11

增加应用群聊会话接口（暂不支持第三方），应用可创建群聊、修改群聊、推送消息到群，详情
增加外部联系人管理接口（暂不支持第三方），详情

- JS-SDK，增加将外部联系人标记为企业客户接口，详情

增加上传图片接口，可上传图片得到永久有效的 url，详情

- JS-SDK，增加 Wi-Fi 接口，详情

- JS-SDK，增加剪贴板接口，详情

## 2018-04-08

获取永久授权码接口不再返回授权管理员的手机号码和邮箱信息。详情

## 2018-03-30

读取成员信息接口增加员工个人二维码。 详情
获取部门成员详情接口增加员工个人二维码。 详情

## 2018-03-28

第三方开放接口，注册定制化，获取注册码接口支持自定义 State 参数。详情

## 2018-03-22

第三方应用接口，获取企业永久授权码接口及获取企业授权信息接口，返回信息增加企业规模及所属行业。详情

## 2018-03-09

创建成员接口增加 to_invite 参数。详情
增量更新成员接口增加 to_invite 参数。详情
全量覆盖成员接口增加 to_invite 参数。详情

## 2018-02-06

- JS-SDK，增加分享到朋友圈接口。详情

## 2018-01-02

通讯录管理，增加邀请成员接口。详情

## 2017-12-29

- JS-SDK，增加自定义转发到会话。详情
- JS-SDK，增加自定义转发到微信。详情
- JS-SDK，Windows/Mac 支持监听页面返回事件。详情

## 2017-12-06

- OA 数据接口，增加获取打卡规则接口。详情

## 2017-11-30

- 关于第三方套件到单应用的调整。详情
- 第三方单应用支持新的 oauth2 授权方式。详情
- 素材管理，增加获取高清语音素材接口。详情

## 2017-11-15

第三方应用接口, 新增获取应用管理员接口。详情
注册定制化，可指定注册的企业信息。详情

## 2017-11-07

- JS-SDK, chooseImage 支持相机连拍。详情
- JS-SDK, 增加打开系统默认浏览器接口。详情

## 2017-11-01

资源下载，增加样式库 WeUI for Work。详情

## 2017-09-25

- JS-SDK，增加监听页面返回事件接口。详情

## 2017-09-18

电子发票新增批量查询电子发票接口。详情

## 2017-09-01

第三方开放接口，注册定制化新增设置授权应用可见范围接口。详情

## 2017-08-16

第三方开放接口，新增注册定制化能力。详情

## 2017-08-08

新增电子发票报销能力。详情

## 2017-07-21

新增企业支付能力。详情

## 2017-07-18

第三方读取成员、获取部门成员详情以及更新成员接口，增加 english_name、telephone、isleader、order 四个字段。详情

## 2017-07-04

第三方开放接口，设计资源优化。详情

## 2017-07-03

成员管理，读取成员接口去除 enable 字段。详情
通讯录修改权限，增加通讯录全部信息的读取能力。详情
通讯录管理，异步任务接口支持扩展属性。详情

## 2017-06-29

成员管理，增加二次验证接口。详情

- JS-SDK，增加创建会话接口。详情

## 2017-06-22

开发前必读，增加与企业号接口差异的说明。详情

## 2017-06-20

- JS-SDK，增加通讯录选人接口。详情

## 2017-06-19

第三方开放接口，单点登录支持成员登录。详情
