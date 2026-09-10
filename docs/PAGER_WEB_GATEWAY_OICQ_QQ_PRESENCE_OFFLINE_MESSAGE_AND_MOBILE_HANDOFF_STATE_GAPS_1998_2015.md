# Pager / Web gateway / OICQ-QQ presence / offline-message / mobile-handoff state gaps（1998—2015）

## 0. Scope guard

本文件研究的是 **1998—2015 中文互联网中，OICQ/QQ 及与其相连的 Web、SMS/WAP、移动终端、在线状态与离线消息接口怎样形成一套“人可被找到”的数字基础设施**。

它不是：

- 一部完整 QQ 产品史；
- 一部中国寻呼史；
- 一部全球 ICQ 史；
- 一部 2015 年以后的微信/移动社交史。

1998 年以前的寻呼机、公用电话，以及海外 ICQ，只作为前史和比较边界。完整的普通生活史、跨国比较与 2020s “离线权”讨论，写在 `how-people-lived`：

`topics/from-please-page-me-to-why-didnt-you-reply-reachability-pagers-mobile-phones-and-presence-states-china-1984-2026.zh-CN.md`

本仓仍遵守 `docs/METHOD.md`：platform、site/host、account、client、session、page、capture 与 claim 必须分开；搜索结果里的 archive locator 不是 verified Memento。

---

## 1. 为什么这是 old-Web 问题，而不只是“聊天软件史”

OICQ/QQ 的核心互动长期发生在客户端和服务器，而不是普通 HTML 页面里。

但用户能否真正使用这套系统，又依赖大量 Web 和非 Web 边界：

```text
软件下载页 / 帮助页 / 注册页
→ 安装客户端
→ 建立账号
→ 客户端登录服务器
→ presence 状态发布
→ 好友端渲染状态
→ 消息提交
→ 在线直达或服务器暂存
→ 客户端取回
→ 用户实际注意
→ 回复
```

到 2000s 又加入：

```text
PC QQ
↔ SMS / WAP / 运营商网关
↔ GSM 手机
```

因此，只保存 `qq.com` 或 `tencent.com` 的网页壳，无法复原一个人当年“头像亮着”“隐身”“离线收到消息”到底如何工作。

这个对象特别适合用于提醒：

> **旧网考古不能把 Web archive 等同于 Internet archive。**

网页只是入口、说明和一部分控制面；真正的状态可能在 proprietary client、即时通信服务器、运营商 SMS 网关和瞬时 presence 数据里。

---

## 2. 研究单位：先把“一个 QQ 用户”拆开

至少要区分：

- **person**：现实中的人；
- **QQ/OICQ account / UIN**：账号标识；
- **credential**：密码、令牌等认证材料；
- **client installation**：某台 PC / 手机上的某版本客户端；
- **session**：一次已认证连接；
- **device**：PC、GSM 手机等；
- **presence state**：online / away / busy / DND / invisible / offline 等；
- **contact-list rendering**：好友端实际看到的状态；
- **message object**：某条文本、图片等消息；
- **server receipt state**：服务器是否接受；
- **recipient delivery state**：目标客户端是否取到；
- **human attention state**：人是否看见；
- **reply state**：人是否回复；
- **Web help/download/binding page**：公开 Web 表示；
- **carrier gateway**：SMS/WAP 与 OICQ/QQ 的桥接；
- **archive capture**：后来保存的一份历史表示。

这些不能互相替换。

---

## 3. 第一组 state gaps：账号、会话与 presence

### 3.1 `account-exists / session gap`

```text
账号存在
!=
当前有一个客户端成功登录
```

一个长期不用的 QQ 号仍可能存在，但没有 session。

### 3.2 `session / presence-publication gap`

```text
客户端连接成功
!=
presence 已向所有联系人正确发布
```

网络故障、协议状态、服务器延迟、客户端 bug 都可能造成偏差。

### 3.3 `presence-authority / contact-render gap`

```text
服务器权威状态
!=
某个好友客户端此刻显示的状态
```

必须考虑：

- 客户端缓存；
- 刷新延迟；
- 第三方插件；
- 版本不兼容；
- “隐身”本来就设计成向他人渲染为不可见/离线。

### 3.4 `online / attentive gap`

这是本案例最重要的历史边界之一：

```text
Online
!=
人在电脑前
!=
正在看 QQ
!=
有空
!=
愿意回复
```

2009 年以后，手机 QQ 让这一 gap 更大：客户端可以常驻，presence 指示越来越不等于身体坐在 PC 前。

### 3.5 `invisible / truly-offline gap`

好友列表上看起来离线，至少可能意味着：

- 对方真的没有 session；
- 对方隐身登录；
- 客户端/服务器状态异常；
- 第三方“查隐身”工具声称识别到另一状态。

所以 historical screenshot 上一个灰头像不能直接写成“此人当时没上网”。

---

## 4. 第二组 state gaps：一条消息从“发出去”到“人看见”

### 4.1 `compose / submit gap`

用户在输入框里打完字，不等于客户端已经把消息提交到服务器。

### 4.2 `submit / server-accept gap`

客户端点击发送，不等于服务器接受成功。

### 4.3 `server-accept / recipient-delivery gap`

服务器接受消息后，可能：

- 对方在线，直接进入其 session；
- 对方离线，由服务器暂存；
- 网关转送到另一渠道；
- 因协议/网络/账户状态失败。

### 4.4 `delivery / human-read gap`

```text
客户端已经收到
!=
通知被人注意
!=
人读懂了
```

聊天记录和服务器日志最多能证明技术状态的一部分，不能自动证明注意力。

### 4.5 `read / reply gap`

历史研究尤其不能从“22:03 收到消息，22:40 回复”反推对方故意晾了 37 分钟。

人可能：

- 离开座位；
- 在上课/上班；
- 手机没电；
- 无信号；
- 只看到通知没打开；
- 需要考虑后再回复。

`message latency` 与 `social response expectation` 是两种时间。

---

## 5. 1998 ICQ：presence 从一开始就同时包含“找到我”和“别打扰我”

### 5.1 同时代海外技术教程

1998 年 `INTERNET Watch` 的 ICQ 教程说明：

- 对方在线时消息可即时到达；
- 对方离线时，服务器可保存消息并在下次连接时呈现；
- 联系人列表显示连接/在线状态；
- 用户可设置 away 等状态。[E1]

1998 年 `CHIP` 的同期介绍进一步列出 Online、Away、N/A、Occupied、DND、Free For Chat、Invisible、Offline 等状态；文章还提醒按分钟/电话脉冲付费的拨号用户，保持长期在线本身有成本。[E2]

**证据等级：A/B（同期技术媒体/教程，海外比较）。**

这两份材料只用于建立即时通信协议/界面谱系，不证明 OICQ 在同日具有完全相同的实现。

### 5.2 重要方法结论

presence 并不是简单的一盏“人在/不在”灯。

它从早期已经承载：

```text
网络连接状态
+
用户自行声明的可用性
+
对联系人展示的社交边界
```

因此以后考古 QQ 的“在线/隐身”时，不能只问图标颜色，还要问：

- 谁设置的？
- 服务器如何解释？
- 好友端如何渲染？
- 第三方客户端是否修改？
- 当时拨号/包月环境是否允许长期在线？

---

## 6. 2001：OICQ→QQ 改名提醒我们，品牌连续性也不是协议连续性

2001 年 4 月新浪科技同期报道说，腾讯此前称 OICQ 的即时通信软件在 `2000b Build 0325` 测试版中改为“腾讯 QQ”；报道同时说腾讯网站上的 OICQ 字样也逐步改成 QQ。[E3]

同月台湾 iThome 亦有独立同期报道，记录 OICQ→QQ 的名称转换与当时腾讯自己的用户规模宣称。[E4]

**证据等级：B，两组同期媒体；用户量只按腾讯当时宣称处理。**

这里要长期保留：

`brand-name continuity != domain continuity != account continuity != protocol continuity`。

更名期间，旧域名、软件下载页、客户端 build、账号系统和用户口语中的“QQ/OICQ”并不会在同一秒钟同步切换。

---

## 7. 2001 “移动 OICQ”：PC 即时通信通过运营商网关伸到 GSM 手机

新浪科技 2001-03-06 的同期报道记录，北京移动正式开通“移动 OICQ”，GSM 的 SMS/WAP 系统与 OICQ 系统通过网关互联；手机用户可以给 OICQ 用户发送消息、查询好友状态，并可在 OICQ 用户不在线时留下消息。[E5]

报道还称 2001 年 1 月移动 OICQ 日消息量已超过 100 万条。

**证据等级：B，同期科技媒体；消息量为运营方/报道口径，不等于独立用户数。**

这是一条极重要的中国旧网过渡态：

```text
QQ/OICQ relationship graph on PC
+
carrier SMS/WAP gateway
+
GSM handset
```

已经可以形成移动通信链。

因此：

`mobile Internet behavior != smartphone app behavior`。

### 7.1 `QQ-account / mobile-binding gap`

一个 QQ 号存在，不等于已经正确绑定可用手机服务。

### 7.2 `gateway-enabled / SMS-delivery gap`

运营商宣布业务开通，不等于每一条消息都成功穿过：

```text
QQ/OICQ server
→ gateway
→ carrier SMSC
→ radio network
→ handset
```

### 7.3 `friend-status-query / authoritative-presence gap`

手机能查询好友状态，只证明这一功能被同期报道为可用，不代表查询结果没有刷新延迟或协议映射问题。

---

## 8. 2008：离线消息不再只是一段文字

2008-07-08 的太平洋电脑网/新浪体验文记录，QQ2008 正式版新增“离线也能发图片”等功能。[E6]

**证据等级：B，同期软件评测。**

它说明 offline-message state machine 在 2000s 后期已经不仅承载短文本。

但仍不能写成：

```text
离线图片发送按钮存在
=
任意图片在任意网络条件下都永久可取回
```

还需要确认：

- 上传对象是否先进入腾讯服务器；
- 是否有大小/格式/时效限制；
- 对方客户端版本；
- 对方实际下载；
- 图片对象是否在服务器过期。

这些本轮没有得到腾讯原始协议/帮助页，保持 unknown。

---

## 9. 2008—2009：“隐身”从软件功能变成边界争议

### 9.1 2008 同期用户采访：隐身可以被理解成“不想被打扰”

2008-11-26 齐鲁晚报/新浪关于“查隐身”功能的报道保存了同期用户观点：有人使用相关第三方功能只是想知道朋友、同事是否在线；另一位受访者则明确把好友隐身解释为“不想被打扰”，并认为用户有权保护这种状态。[E7]

**证据等级：B，同期地方媒体第一人称；不代表全体 QQ 用户。**

这给 old-Web 研究带来一个不能忽略的边界：

`presence discoverability != consent to contact`。

### 9.2 2009 同期教程：QQ2008 beta1 可在登录对话框选择“隐身登录”

中关村在线/新浪 2009-02-03 的教程以 QQ2008 beta1 为例，明确描述登录框中的“隐身登录”。[E8]

**证据等级：B，同期软件操作教程。**

它可证明这个版本/教程描述的操作路径，但不能自动外推所有 2008 build。

### 9.3 `third-party-visibility / first-party-privacy gap`

一旦“查隐身”工具出现，旧网考古还要多问：

- 客户端显示的是腾讯官方 presence 还是第三方推断？
- 插件是否通过异常协议行为探测？
- 平台后来关闭相关接口是否改变过去状态？
- 媒体截图是否来自官方客户端？

截图中的“隐身可见”标签本身不能当作服务器真实状态的最终证据。

---

## 10. 2009：手机 QQ 让“头像一直亮着”与“人一直在电脑前”彻底分开

2009-09-03 中新网/搜狐校园报道保存了一个非常具体的同期误判：一位母亲看到儿子的 QQ 头像几乎一直在线，先以为他逃课，后来才知道手机 QQ 可以让账号长时间保持在线；报道还采访到从早到晚使用手机 QQ 的大学生。[E9]

**证据等级：B，同期媒体第一人称/局部观察。**

这足以固定一个重要语义漂移：

```text
1990s 后期：Online 较强地暗示一台联网电脑当前开着客户端
2009：Online 可能只是手机端常驻 / 长连接
```

因此：

`presence icon != device type != location != attention`。

同期 CNNIC 第25次报告称，截至 2009 年底中国网民约 3.84 亿、手机网民约 2.33 亿；手机网民占网民 60.8%。[E10]

中国互联网协会同期转引 CNNIC 调研称 2009 年即时通信用户约 2.77 亿，手机即时通信用户约 9141 万。[E11]

这些数字用于大规模采用背景，不用于证明某个 QQ feature 的具体实现。

---

## 11. 一个完整的 historical QQ message state machine

以后复原任意 1999—2015 QQ/OICQ 消息功能，至少应问：

```text
person has account
→ account credential valid
→ correct client version installed
→ network path available
→ session authenticated
→ presence published
→ sender sees some rendered state
→ message composed
→ client submits
→ server accepts
→ recipient online?
    → yes: route toward active session
    → no: store offline / reject / alternate path depending on feature/version
→ recipient client obtains object
→ local notification/render succeeds
→ human notices
→ human opens/reads
→ human replies or not
```

如果经过移动网关，再加：

```text
QQ account eligible/bound
→ gateway enabled
→ message mapped to SMS/WAP format
→ carrier accepts
→ SMSC routes
→ handset reachable
→ handset receives
→ user notices
```

任意一个箭头都不能由“网页上有这个按钮”自动补齐。

---

## 12. old-Web 专用 state-gap 清单

### 身份 / 账号

- `person / QQ-UIN gap`
- `QQ-UIN / active-user gap`
- `registered-account / concurrent-session gap`
- `credential-valid / client-login-success gap`

### presence

- `session / presence-publication gap`
- `presence-authority / contact-render gap`
- `online / attentive gap`
- `online / interruptible gap`
- `invisible / truly-offline gap`
- `first-party-presence / third-party-detection gap`

### message

- `message-compose / submit gap`
- `submit / server-accept gap`
- `server-accept / recipient-delivery gap`
- `recipient-delivery / human-read gap`
- `human-read / reply gap`
- `offline-store / eventual-retrieval gap`
- `offline-image-upload / recipient-download gap`

### Web / client / gateway

- `Web-download-page / binary-installer gap`
- `installer / runnable-historical-client gap`
- `historical-client / live-server-protocol gap`
- `Web-help-page / operational-backend gap`
- `QQ-account / mobile-binding gap`
- `gateway-advertised / gateway-operational gap`
- `gateway-accept / SMS-delivery gap`
- `desktop-presence / mobile-presence-mapping gap`

### 统计

- `registered-account / unique-person gap`
- `concurrent-online-account / attentive-person gap`
- `daily-message-count / unique-sender gap`
- `daily-message-count / successful-human-conversation gap`

### archive

- `screenshot-status / authoritative-server-state gap`
- `historical-page / historical-client-state gap`
- `historical-client-shell / historical-server-protocol gap`
- `archived-help / historical-service-availability gap`

---

## 13. 浏览器、客户端和协议环境：这里不能只写 IE6 / charset

传统 Web case 常问：

- charset；
- table/CSS；
- JS；
- Flash；
- IE/Netscape。

QQ case 还必须增加：

- Windows 版本；
- QQ/OICQ exact build；
- 本地聊天记录格式；
- proprietary protocol 版本；
- 登录服务器是否仍存在；
- server-side presence authority；
- UDP/TCP 等 transport 选择（若有一手协议证据再记录）；
- SMS/WAP carrier gateway；
- 当时运营商网络；
- 手机终端和短信能力；
- 第三方插件/外挂是否介入。

没有 exact-version evidence 时，不要因为“QQ2008 有隐身”就给 1999 OICQ 补同样 UI。

---

## 14. Archive bias 1：`client/server split loss`

QQ 是典型的客户端—服务器系统。

二十年后可能保存：

- 安装包；
- 软件截图；
- 下载页；
- 教程；
- 帮助文章；
- 本地聊天数据库；

但缺失：

- 原登录服务器；
- presence 服务；
- 在线好友列表权威状态；
- 离线消息队列；
- SMS 网关；
- 当时运营商接口。

因此一个旧客户端能够在虚拟机启动，只能证明 **client shell survives**，不能证明历史网络体验已经复原。

---

## 15. Archive bias 2：`presence ephemerality`

在线、away、busy、invisible 是高度瞬时状态。

Web crawler 即使保存了帮助页，也几乎不会保存：

> 2008-11-26 22:03 某普通用户此刻到底是什么 presence。

偶尔留下的截图又有严重选择偏差，常来自：

- 教程作者；
- 软件评测；
- 争议事件；
- bug/外挂演示。

所以截图里的状态不代表平均日常。

---

## 16. Archive bias 3：`private-message invisibility`

QQ 真正最庞大的生活史材料——朋友、恋人、家人、同学、同事之间的普通聊天——多数本来就不是公共 Web。

这也是一个**伦理上不应以“尽量恢复”为目标**的对象。

研究平台结构时优先保存：

- 客户端状态机；
- URL/host；
- 软件版本；
- 官方帮助/媒体教程；
- 协议/网关存在证据；
- 匿名化后的行为研究；

而不是把普通人的私人聊天记录集中重新公开。

因此：

`public-Web survivability != everyday-communication importance`。

---

## 17. Archive bias 4：`message-survival / attention-loss asymmetry`

即使某条消息真的保存下来，最关键的生活状态仍然常常消失：

```text
22:03 message timestamp survives
```

却不知道：

```text
人是否在上课
是否已经睡着
设备是否在包里
是否有网络
是否看到了弹窗
是否故意晚回
```

因此 old-Web/IM 研究不能把服务器时间戳直接写成“社会互动发生时间”。

---

## 18. 反例与后见之明风险

### 18.1 不把 OICQ/QQ 写成“Web 服务”

Web 是注册、下载、帮助和部分移动绑定的入口之一；核心 IM 长期主要是客户端/服务器系统。

### 18.2 不把手机 QQ 倒写进 1999

2009 的 always-on 语义不能用于解释拨号 Internet 时期的 online。

### 18.3 不把“隐身”浪漫化成完整 privacy control

隐身只管理一类 presence 呈现，不等于阻止消息发送、IP/插件探测、其他渠道联系或现实工作要求。

### 18.4 不把消息量当人数

2001 “移动 OICQ 日消息超百万”只能证明平台/运营商当时报告的流量规模。

`1 million messages != 1 million users`。

### 18.5 不从今天服务器行为补历史协议

今天 QQ 的登录、离线消息、已读/未读、设备同步行为，不能反推 2001/2008 exact behavior。

---

## 19. 已证实 / 高概率 / 不知道

### 已证实

- 1998 海外 ICQ 同期资料明确存在 online/away/DND/invisible/offline 等 presence 概念与离线消息；
- 2001 中国同期媒体记录移动 OICQ 通过 SMS/WAP/运营商网关与 PC 即时通信互联；
- 2001 年 OICQ→QQ 的名称转换有两组同期媒体记录；
- 2008 QQ2008 同期评测记录离线图片发送；
- 2008 同期用户已经把“隐身”解释为一种“不想被打扰”的边界；
- 2009 同期教程明确展示 QQ2008 beta1 的“隐身登录”；
- 2009 同期生活材料显示手机 QQ 会造成“头像一直在线，但人不在电脑前”的误解；
- 2009 年手机 Internet / 手机 IM 已经是大规模现象。

### 高概率但仍需一手客户端/协议证据加强

- 早期 OICQ/QQ 的 presence 设计深受 ICQ 类客户端谱系影响；
- 运营商网关使 PC 社交图在智能手机以前就获得移动外延；
- 手机常驻让 presence 从“连接状态”逐步漂移为“账号背景状态”；
- public Web 对 QQ 真实使用史的可见度远低于客户端/私聊实际重要性。

### 不知道

- 1999—2002 各 exact OICQ/QQ build 的完整 presence 枚举；
- exact server protocol 如何映射隐身、away、busy；
- 2001 移动 OICQ 的 SMS/WAP gateway 错误、重试和过期语义；
- 2008 离线图片 exact TTL、大小、下载和清理规则；
- 不同版本第三方“查隐身”究竟怎样探测；
- 2000s 早期多少 ordinary users 真正使用 Mobile OICQ，而不只是发送消息总量；
- 早期客户端在 modern network / emulator 中能够复原到什么程度。

---

## 20. M1 status

本轮查到：

- 2001 OICQ→QQ 与 Mobile OICQ 的明确 historical locators / 同期媒体；
- 2008 QQ2008 离线图片评测；
- 2008—2009 隐身相关同期采访/教程；
- Web Design Museum 的 `Tencent QQ in 2004` 页面可作为后续 archive locator lead。[E12]

但本轮 **没有取得并逐项核验一个满足本仓 METHOD 的 Tencent/OICQ/QQ historical Memento**：

- original URL；
- capture URL；
- capture datetime；
- HTTP/replay state；
- charset / Content-Type；
- DOM；
- JS / image / installer subresources；
- 页面是否 redirect / error / login shell。

因此结论必须写成：

> **M1 verified historical OICQ/QQ Web capture: NOT ACHIEVED IN THIS SLICE.**

不能写成：

> “Wayback 没保存。”

搜索结果中出现 archive/博物馆 locator，只能登记 candidate/lead。

---

## 21. 对平台谱系研究的意义

QQ 迫使 old-Web 的平台谱系加入一个与“个人主页→博客→SNS”不同的轴：

```text
public page graph
与
private presence/message graph
```

并行存在。

一个平台可以：

- 几乎没有公共可索引用户内容；
- 却在普通人的关系维持中比很多公开网站更重要。

因此以后 `platform-genealogy.md` 不能只比较：

- 谁拥有 URL；
- 谁控制页面布局；
- 谁控制公开内容生命周期；

还要比较：

- 谁控制联系人图；
- 谁控制 presence；
- 私人消息是否本地/服务器保存；
- 账号是否跨设备；
- 平台怎样与电话/SMS/移动网 handoff；
- 平台死亡时，私人关系图和聊天记录能否迁走。

---

## 22. 它改变了“中文旧网是什么”的哪一点？

如果只把 old Web 理解成一堆 HTML 页面，我们会漏掉 2000s 普通生活中非常大的那部分 Internet。

一个人可能每天：

- 打开 QQ；
- 看谁在线；
- 隐身；
- 留一条离线消息；
- 用手机接一条 OICQ/QQ 转来的短信；
- 再去浏览网页。

但二十年以后，最容易被 archive 保存的是最后那一步。

所以 QQ/OICQ 这一案例给仓库增加的核心方法结论是：

> **Internet 的生活史不等于 Web 的页面史；越是成功变成私人、实时、常驻基础设施的系统，反而越可能在公共 Web archive 中留下一个过小的影子。**

---

## Evidence

### [E1] A/B — 海外同期技术教程
INTERNET Watch, 1998-06-08, ICQ 使用教程。用于离线消息、online/away 等状态和同期操作语境。
<https://internet.watch.impress.co.jp/www/article/980608/special.htm>

### [E2] B — 海外同期电脑杂志
CHIP, 1998-07-01, “Sieciowe rendez-vous”. 用于 Online/Away/N/A/Occupied/DND/Free For Chat/Invisible/Offline 与拨号在线成本。
<https://www.chip.pl/1998/07/sieciowe-rendez-vous>

### [E3] B — 中国同期科技媒体
新浪科技，2001-04-06，《为避免知识产权纠纷 腾讯OICQ无奈变脸QQ》。用于 `2000b Build 0325` 更名和网站名称迁移。
<https://tech.sina.com.cn/i/c/61663.shtml>

### [E4] B — 海外华文同期科技媒体
台湾 iThome，2001-04-05，《中國著名即時傳呼軟體OICQ藉最新測試版改名，以避侵權之嫌》。用于独立确认 OICQ→QQ 名称转换；平台用户量只作为腾讯当时宣称。
<https://www.ithome.com.tw/news/12315>

### [E5] B — 中国同期科技媒体
新浪科技，2001-03-06，《北京地区正式开通“移动OICQ”服务》。用于 SMS/WAP/OICQ 网关、好友状态查询、离线消息与业务消息量口径。
<https://tech.sina.com.cn/i/c/56518.shtml>

### [E6] B — 同期软件评测
太平洋电脑网/新浪科技，2008-07-08，《离线图片任你发！QQ2008正式版体验》。用于 QQ2008 正式版离线图片功能存在。
<https://tech.sina.com.cn/s/2008-07-08/0920723724.shtml>

### [E7] B — 同期第一人称采访
齐鲁晚报/新浪，2008-11-26，《腾讯关闭查隐身功能》。用于普通用户对“隐身/查隐身/不被打扰”的不同理解。
<https://news.sina.com.cn/c/2008-11-26/081714787612s.shtml>

### [E8] B — 同期软件操作教程
中关村在线/新浪科技，2009-02-03，《做真正的“隐身侠” QQ技巧之终极隐藏》。用于 QQ2008 beta1 登录框“隐身登录”操作路径。
<https://tech.sina.com.cn/s/2009-02-03/09272788053.shtml>

### [E9] B — 同期第一人称/校园报道
中新网/搜狐，2009-09-03，《大学生手机QQ聊上瘾》。用于“头像一直在线”与手机 QQ 常驻造成的现实语义误判。
<https://news.sohu.com/20090903/n266428905.shtml>

### [E10] A — 机构统计
CNNIC，第25次《中国互联网络发展状况统计报告》，2010-01-15。用于 2009 年末网民与手机网民规模。
<https://www.cnnic.cn/n4/2022/0401/c88-808.html>

### [E11] B — 机构行业报道
中国互联网协会，2010-01-04，《即时通信经济价值凸显》。用于 2009 即时通信和手机即时通信用户量的同期转引口径。
<https://www.isc.org.cn/article/10727.html>

### [E12] C/D locator lead — 后来 Web 设计档案索引
Web Design Museum, “Tencent QQ in 2004”. 当前页面声明关联 Internet Archive，但本轮未把其链接升级为 verified capture。
<https://www.webdesignmuseum.org/gallery/tencent-qq-2004>

---

## 下一步

1. 从 `Tencent QQ in 2004` locator 或独立 archive index 出发，取得一个真正可打开并核验的 2004 QQ 页面 Memento。
2. 寻找 1999—2002 OICQ/QQ historical installers / CHM help / readme，按 exact build 记录 presence 与 offline-message 状态。
3. 如果有合法可访问的历史客户端，在隔离环境中做 reconstruction，明确标注 server unavailable / emulated 部分。
4. 找 2001 Mobile OICQ 的运营商用户手册、资费表或绑定帮助页，补 `QQ account → mobile binding → SMS gateway` 状态机。
5. 找 2008 QQ2008 官方帮助或客户端资源，核离线图片大小、时效、接收版本条件。
6. 以后若写 WebQQ，单独建 case，不把 WebQQ 的 AJAX/浏览器状态倒写回 desktop QQ。

> AI-assisted research note. 该文件刻意把客户端状态、服务器状态、人类注意力和 Web archive 分开；未知项保持 unknown。