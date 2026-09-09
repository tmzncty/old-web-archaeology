# QQ Web Presence、在线/离开/隐身、动态状态按钮与可联系性证据缺口（2000—2015）

## 目的与 scope

本文件补充：

- `docs/METHOD.md`；
- `docs/CONTACT_STACK_AND_CHANNEL_HANDOFF_1998_2002.md`；
- `docs/CONTACT_ENDPOINT_LIFECYCLE_1997_2003.md`；
- `docs/SOCIAL_STATUS_VISIBILITY_AND_CONSUMER_ACCOUNT_IDENTITY_2008_2010.md`。

普通生活史主文档：

- https://github.com/tmzncty/how-people-lived/blob/main/topics/from-online-icons-to-right-to-disconnect-presence-availability-and-offline-time-china-1999-2026.zh-CN.md

本文件只处理约 2000—2015 中文旧 Web 中与即时通信 presence 直接相交的对象：

- QQ/TM 在线、离开、隐身、忙碌等状态；
- QQ Web Presence / QQ 在线状态；
- 网页、论坛、博客、邮件签名中的状态按钮；
- `is.qq.com/webpresence/` / `code.shtml`；
- `wpa.qq.com/pa?...` 等状态图像请求；
- `tencent://message/...` URL protocol handoff；
- 陌生人临时会话；
- 状态的隐私、安全与访问规则；
- archive 保存动态状态时产生的认识论陷阱。

本仓**不会**因此扩成 2020s 工作群/离线权史。后者写入 `how-people-lived`。

核心问题：

> **一个 archive 里保存下来的“QQ在线”图标，究竟证明了什么？**

最重要的结论先写在前面：

```text
account exists
!= client connected
!= user-declared status says online
!= a particular watcher is allowed to see online
!= web badge rendered online
!= human is at keyboard
!= human saw visitor/message
!= human is available
!= human replied
```

因此：

> **presence representation != lived availability**

---

# 1. 研究单位：不要把“在线”当成一个布尔字段

建议把一个旧 IM/Web presence 案例至少拆成以下对象。

## 1.1 `account / presentity`

被描述状态的 QQ/TM 账号。

```yaml
presentity:
  platform: qq
  identifier_observed: true
  identifier_republished: false
  ownership_verified: false
```

对普通人账号默认不重新发布 QQ 号。

---

## 1.2 `client_session`

某个 QQ/TM/移动桥接客户端与服务端之间的已认证会话。

可能状态：

```text
not_connected
connecting
authenticated
reconnecting
disconnected
unknown
```

注意：

```text
client_session = authenticated
!= user is physically present
```

---

## 1.3 `declared_presence`

用户或客户端声明的可联系性状态，例如：

```text
online
away
busy
do_not_disturb
invisible
offline
custom_status
unknown
```

具体 QQ 版本的状态集合必须按同期版本证据填写，不能把今天的状态词反投到旧版本。

---

## 1.4 `presence_service_state`

服务端保存/分发的状态。

这与客户端 UI 不应默认等同。

需要问：

- 状态更新是否已抵达服务端？
- 是否存在缓存？
- 自动离开/超时是否改变状态？
- 多端登录时哪个状态优先？
- 移动 OICQ / WebQQ 是否使用相同状态模型？

没有同期协议/客户端证据时，这些保持 unknown。

---

## 1.5 `watcher_view`

某个具体观察者实际被允许看到的状态。

可能观察者：

```text
friend
stranger
blocked_user
web_page_visitor
archive_crawler
search_engine
```

presence 从一开始就可能有权限差异。

因此：

```text
server knows user connected
!= every watcher sees user online
```

---

## 1.6 `web_badge`

网页中的在线状态图片/按钮。

历史代码可能包含：

```html
<img src="http://wpa.qq.com/pa?p=...">
```

它可能是：

- 动态请求；
- 跳转后图片；
- 在线/离线二值图；
- 经过缓存或代理的结果；
- 被 archive 单独抓取的子资源。

只有拿到具体版本和响应才能判断。

---

## 1.7 `protocol_handoff`

点击网页以后，从浏览器交给本地 QQ 客户端的 URL scheme，例如：

```text
tencent://message/?uin=...&Site=...&Menu=yes
```

这是**浏览器 → 操作系统 → 本地客户端**的 handoff，不是纯 Web 事务。

---

## 1.8 `conversation_state`

即使按钮可点击，也要继续拆：

```text
click
→ local protocol handler invoked
→ QQ client present
→ client opens temporary-session request
→ platform policy allows request
→ recipient receives request/message
→ recipient notices it
→ recipient accepts/responds
```

Archive 通常只能保存前两三层。

---

# 2. 协议前史：RFC 2778 给旧网考古一个非常好用的 presence vocabulary

RFC 2778（2000）把 presence service 描述成保存并分发 presence information 的系统，区分：

- PRESENTITIES；
- WATCHERS；
- PRESENCE TUPLES；
- STATUS；
- COMMUNICATION ADDRESS；
- ACCESS RULES。

STATUS 的例子包括：

```text
online
offline
busy
away
do not disturb
```

Source:

- RFC 2778, 2000-02: https://www.rfc-editor.org/info/rfc2778/

Evidence grade：**A / original standards document**。

这不是说 QQ 必然按 RFC 2778 实现。

它的价值是提供一个不依赖具体产品的研究框架：

```text
presentity state
!= watcher representation
```

以后旧网页里的“在线”图标都应先问：

> **谁是 watcher？**

而不是只问：

> “这个 QQ 当时是不是在线？”

---

# 3. 2000 QQ2000：隐身直接证明 `connected != visible`

腾讯保存的 2000-11-17 产品发布材料列出 QQ2000 新功能，其中包括：

- “隐身”；
- 多种可自定义离开留言；
- 多级保密选项；
- 黑名单；
- 从对方好友列表删除自己；
- 移动 QQ；
- Tencent Browser 的“谁与我同在”。

Source:

- 腾讯，《QQ2000版本正式发布》：https://www.tencent.com/zh-cn/articles/80254.html

Evidence grade：**A / contemporaneous official platform claim**。

### 可证明

- 2000 年该版本官方宣称存在隐身和离开留言；
- QQ 的 presence 已经允许用户主动管理可见性；
- presence 与联系人/浏览器/移动消息开始相互连接。

### 不能证明

- 后来的 Web Presence 如何映射“隐身”；
- 每个 watcher 都看到同一状态；
- 用户选择隐身时仍能正常进行所有会话；
- 用户规模与实际使用频率。

固定规则：

> **invisible state makes “offline-looking” evidence ambiguous by design.**

因此：

```text
historical screenshot shows grey/offline icon
```

最多证明：

```text
that representation was observed
```

不能升级成：

```text
the person was disconnected from QQ
```

---

# 4. 2001 移动 OICQ：presence 可以跨越 PC Internet 与 GSM SMS/WAP

2001-03-06 新浪科技的同期报道描述，北京移动 2 月 20 日开通“移动 OICQ”，将 GSM SMS/WAP 系统与腾讯 OICQ 互联。

手机用户可以：

- 与 PC OICQ 用户互发消息；
- 查询不在线时收到的信息；
- 查看好友状态；
- 按昵称/邮箱/OICQ 号查用户。

Source:

- https://tech.sina.com.cn/i/c/56518.shtml

Evidence grade：**B+ / contemporaneous service report**。

这对 old-Web scope 的意义不是展开移动通信史，而是提醒：

> **presence source terminal != watcher terminal**。

2001 年已经可能存在：

```text
QQ presentity on PC/QQ service
→ presence service
→ GSM/SMS/WAP gateway
→ mobile watcher
```

所以看到一次“好友状态查询”描述时，不要假设双方都处在浏览器或 PC 客户端里。

---

# 5. 2004：QQ Web Presence 至少已经被公开描述为“把状态发布到互联网”

Google Groups 今天仍可检索到一条内部日期为 2004-11-04 的公开帖子，链接：

```text
http://is.qq.com/webpresence/
```

并描述：

- 将 QQ/TM 在线状态发布在互联网上；
- 点击状态图标发消息；
- 不必先加好友；
- 可生成网页/论坛代码。

Source:

- https://groups.google.com/g/cn.fan/c/O7CHPNCx-Vw

Evidence grade：**A-like / surviving contemporaneous public post**。

### 限制

- 当前 Google Groups 页面不是 verified 2004 Wayback memento；
- 不能证明历史字节未被迁移/重编码；
- 不能据此确定官方首发日期；
- 帖中“最新功能”的措辞只能证明作者当时如此理解。

建议记录：

```yaml
artifact_status: surviving-contemporaneous-post
internal_date: 2004-11-04
historical_byte_identity: unverified
official_service_url_observed: true
```

---

# 6. 2006 同期教程：Web presence 已经被写进“网页/论坛/Blog 联系按钮”的普通技术实践

2006 年《电脑爱好者》一期的幸存 PDF/整理页里介绍：

- 打开 `http://is.qq.com/webpresence/code.shtml`；
- 选择显示风格；
- 填 QQ 号、网站名；
- 生成网页或论坛代码；
- 把按钮贴到页面/签名中。

Source currently surfaced as preserved magazine material:

- https://oddownload.nuduseng.com/5%E8%80%81%E5%85%89%E7%9B%98%E7%BE%A4%28%E7%BE%A4%E5%8F%B7854318908%29%E7%BE%A4%E5%8F%8B%E5%88%86%E4%BA%AB%E6%B1%87%E6%80%BB%202019%E5%B9%B46%E6%9C%881%E6%97%A5%E8%87%B320%E6%97%A5/2019-06-11/%E4%B8%81%E4%B8%81/%E7%94%B5%E8%84%91%E7%88%B1%E5%A5%BD%E8%80%85/%E3%80%8A%E7%94%B5%E8%84%91%E7%88%B1%E5%A5%BD%E8%80%85%E3%80%8B2006%E5%B9%B41-12%E6%9C%9F/%E7%94%B5%E8%84%91%E7%88%B1%E5%A5%BD%E8%80%852006%E5%B9%B4%E7%AC%AC01%E6%9C%9F.pdf

Evidence grade：**B/A-like preserved periodical artifact; provenance chain still needs independent archival verification**。

另一个 2006 技术教程也公开链接 Web Presence 并把它描述成“在线状态发布在互联网上”：

- https://www.iplaysoft.com/qq-skill.html

Evidence grade：**B / contemporaneous tutorial**。

这些材料说明：

```text
presence badge
```

已经进入个人 Blog / 论坛签名 / 小网站技术文化，而不只是 QQ 客户端内部功能。

---

# 7. 2007：幸存 HTML 把 `web_badge` 与 `tencent://message` 同时保存了下来

2007-03-09 的博客园文章给出：

```html
<a target=blank href=tencent://message/?uin=QQ号码&Site=www.cnblogs.com&Menu=yes>
  <img border="0" SRC=http://wpa.qq.com/pa?p=1:QQ号码:7 alt="点击这里给我发消息">
</a>
```

并标出官方代码生成器：

```text
http://is.qq.com/webpresence/code.shtml
```

Source:

- https://www.cnblogs.com/finejob/archive/2007/03/09/669238.html

Evidence grade：**B+ / contemporaneous technical article preserving code**。

这是非常有价值的旧网 evidence，因为它同时保存了两个完全不同的子系统：

```text
<img src=...>
→ state representation / badge retrieval

<a href=tencent://message/...>
→ browser-to-local-client handoff
```

不要把它们写成“一个 QQ 链接”。

---

# 8. 建议的 Web Presence 事务状态机

至少拆成：

```text
P0  QQ/TM account exists
P1  owner has a usable client/account session
P2  user/client declares a presence state
P3  presence service receives/stores state
P4  web-presence service is enabled for that account
P5  page HTML contains badge/link code
P6  visitor browser requests badge resource
P7  server/policy maps account state to visitor representation
P8  badge response reaches browser
P9  browser decodes/renders image
P10 visitor interprets badge as contactable/not contactable
P11 visitor clicks link
P12 OS/browser resolves tencent:// protocol handler
P13 local QQ/TM client opens
P14 temporary-session request allowed by current policy
P15 request/message reaches owner account/session
P16 human notices it
P17 human accepts/responds
```

任何 archive reconstruction 必须说明自己走到了哪一层。

例如：

```text
HTML 中有 <img src=wpa...>
```

最多可靠证明：

```text
P5
```

若 archive 还保存了一份 badge GIF：

```text
P8/P9 artifact may be available
```

仍然不能自动证明：

```text
P16/P17
```

---

# 9. 2008：同期教程明确把按钮解释成“看到你的 QQ 是否在线”

2008-09-10 博客园文章《在网页中嵌入QQ》描述 Web Presence：

- 进入 `http://is.qq.com/webpresence/`；
- 选择状态图片风格；
- 填 QQ/TM 号码和来源网站；
- 生成网页或论坛代码；
- 网页上显示 QQ 是否在线；
- 点击后发起临时会话；
- 被联系者可以拒绝或设置临时会话条件。

Source:

- https://www.cnblogs.com/onlywnan/archive/2008/09/10/1288370.html

Evidence grade：**B / contemporaneous tutorial**。

这说明 Web Presence 同时承担两种功能：

```text
presence publication
+
conversation initiation
```

这两种功能在 archive 中可能有完全不同的保存率。

---

# 10. `wpa.qq.com/pa`：动态图像不能按普通静态 GIF 理解

2007 的代码已证明页面会请求类似：

```text
http://wpa.qq.com/pa?p=1:<QQ>:<style>
```

2008/2009 的用户教程又把按钮解释为会根据在线状态显示不同结果。

因此对研究者来说，至少存在以下可能链：

```text
HTTP request
→ account identifier extracted
→ service/policy lookup
→ current/derived presence state
→ style mapping
→ GIF/image response
```

目前本轮**没有拿到同期后端协议文档**，所以上述后端细节保持 D/high-probability model，而不是 historical original。

固定规则：

> **HTTP 200 from badge endpoint != “user was online”.**

必须先知道：

- 响应 body 到底是哪一个图；
- 该图在该版本的语义；
- 是否被缓存；
- 请求者是否受到权限规则影响；
- “隐身”映射成什么；
- archive 是否返回历史 body 还是今天的 fallback/重写结果。

---

# 11. `tencent://message`：页面活着，不代表历史会话链还能执行

2009 年博客园技术文章专门分析 `tencent://message`，将其解释为浏览器 URL protocol 交给操作系统注册的本地程序处理，并用 Windows 注册表展示类似机制。

Source:

- https://www.cnblogs.com/phinecos/archive/2009/03/06/1404951.html

2010 年另一篇技术文章继续给出 QQ 在线状态代码与 `tencent://message` 形式：

- https://www.cnblogs.com/cai9911/archive/2010/07/15/1778493.html

Evidence grade：**B / contemporaneous technical explanation**。

因此：

```text
archived <a href="tencent://message/...">
```

只证明历史页面希望发起一个本地协议 handoff。

它不证明：

- 现代浏览器仍允许执行；
- 本机安装历史 QQ；
- URL protocol 注册仍存在；
- 参数语义没有变化；
- 服务端仍允许该类临时会话；
- 历史 QQ 号仍由同一人控制。

固定规则：

> **clickable historical URI != reproducible historical conversation transaction**。

---

# 12. 2010 V3.0：临时会话本身又叠加了新的授权与安全状态

2010-09-20 的同期报道描述 QQ 在线状态 V3.0：

- 代码可嵌入网站、邮箱、论坛、博客；
- 访客无需加好友即可发起临时会话；
- 可配置是否开放文件/语音/视频；
- 支持明文/密文代码；
- 账号主人需要先开通服务；
- 可配置网站黑白名单；
- 可屏蔽特定 QQ；
- 可设置临时会话安全等级。

Source:

- https://www.doit.com.cn/p/68947.html

Evidence grade：**B / contemporaneous product report**。

因此到 2010 年，状态链不能再写成：

```text
user online
→ stranger clicks
→ chat opens
```

至少应写：

```text
account state
+
service enabled
+
source website policy
+
stranger policy
+
feature capability policy
→ temporary session may open
```

这也说明：

> **presence visibility and conversation permission are separate states.**

一个人可以公开“在线”，却不必允许所有陌生来源打开完整会话能力。

---

# 13. 普通生活证据：Web Presence 确实进入了网店客服，而不只是技术 demo

同一 2010 报道中的网店经营者称，每天约有 7—8 人通过店铺页面上的 QQ 在线状态咨询业务，客户不必先加好友，他也不必一直盯着网页。

Source:

- https://www.doit.com.cn/p/68947.html

Evidence grade：**B / contemporaneous reported user statement**。

### 可以证明

- 至少存在普通小商户把 QQ presence badge 用作客户入口的同期个案；
- Web 页面与 IM presence 已经形成具体业务 handoff；
- 在线状态可以减少“守网页”的注意力劳动。

### 不能证明

- 2010 网店普遍如此；
- 每日 7—8 人有独立日志验证；
- badge status 准确反映店主注意力；
- 访客最终成交。

推荐写成：

```text
contemporaneous reported use
```

而不是：

```text
widespread adoption
```

---

# 14. `presence visibility` 必须和“现实社会身份可见性”分开

已有：

`SOCIAL_STATUS_VISIBILITY_AND_CONSUMER_ACCOUNT_IDENTITY_2008_2010.md`

讨论的是：

```text
occupation / hukou / school / employer
```

是否在消费级账号上可见。

本文件的 presence visibility 则是：

```text
online / away / busy / invisible / offline
```

两者不能混用。

一个人可能：

```text
现实身份高度匿名
+
在线状态高度可见
```

也可能：

```text
实名网店经营者
+
QQ 选择隐身
```

所以建议 schema 分开：

```yaml
social_identity_visibility: ...
presence_visibility: ...
```

---

# 15. `Invisible` 让 watcher-specific evidence 成为必要字段

腾讯 2000 年已确认存在隐身功能，但本轮没有找到足够强的一手材料证明 2004—2010 每个 Web Presence 版本对 invisible 的具体映射。

因此任何案例都必须避免：

```text
badge offline
→ account was disconnected
```

推荐增加：

```yaml
watcher_context:
  watcher_type: friend|stranger|web-visitor|archive-crawler|unknown
  authenticated: false|true|unknown
  relationship_to_presentity: unknown
  access_rule_observed: false

presence_representation:
  observed_value: online|offline|away|unknown
  semantic_mapping_version_verified: false
  invisible_mapping_verified: false
```

这是旧网 presence 研究最重要的新字段之一。

---

# 16. Archive 最危险的新陷阱：`presence petrification / 在线状态石化`

动态 presence 原本只想回答：

> “此刻大概能不能联系？”

Archive 却可能把它保存成：

```text
一个永远绿色的图标
```

或：

```text
一个永远灰色的图标
```

后人打开页面时，图标失去了原本的“此刻”，却还保留在线/离线的视觉语义。

这会产生 **presence petrification / 在线状态石化**：

> **瞬时通信状态被档案冻结成看似稳定的历史属性。**

必须明确：

```text
captured status badge
!= permanent account state
!= person's general availability
!= person's biography
```

---

# 17. 主 HTML 与 badge 子资源的 capture datetime 可能不一致

一个 Web archive 页面可能：

```text
HTML captured at T0
badge requested/captured at T0 + Δ
CSS/JS captured at T1
```

若 presence 在 T0 与 T0+Δ 之间改变，页面与 badge 甚至不代表同一逻辑状态。

推荐记录：

```yaml
capture_bundle:
  html_capture_datetime: ...
  badge_capture_datetime: ...
  same_memento_bundle: unknown
  datetime_delta_seconds: unknown
```

若 archive 只把 badge 热链到今天：

```text
historical HTML + live presence endpoint
```

则视觉结果更不能作为历史状态。

---

# 18. Archive crawler 不是当年的好友

RFC presence 模型强调 watcher/access rules；QQ 又有隐身、黑名单和陌生临时会话规则。

因此 archive crawler 访问一个 badge 时，可能属于：

```text
unauthenticated stranger watcher
```

而不是：

```text
friend watcher
```

即使同一历史秒：

```text
friend view
!= crawler view
```

也是完全可能的设计。

所以：

> **archive replay cannot automatically reconstruct the social viewpoint of a historical buddy list.**

---

# 19. Web archive 天然保存“发现入口”，却很难保存真正会话

最容易保存：

- `is.qq.com/webpresence/` 帮助/生成器；
- 某博客中的 QQ 按钮；
- `tencent://message` href；
- 状态图片；
- 教程；
- 静态 alt 文本。

最难保存：

- QQ 服务端 presence state；
- watcher-specific access rule；
- 本地 QQ 客户端；
- 临时会话是否弹出；
- 消息是否真正提交；
- 对方是否看到；
- 是否回复；
- 两人后来是否成为好友；
- 是否转入电话或线下关系。

因此本文件把已有 contact-stack 规则进一步扩展为：

> **archived presence surface != complete availability transaction**

以及：

> **archived web contact button != archived social interaction**。

---

# 20. “状态图标”至少有七种不同 claim，不要一次写完

看到一个绿色 QQ 图标时，逐层问：

1. `badge_markup_exists`：HTML 有这个状态图标引用吗？
2. `badge_resource_captured`：图片 body 被 archive 保存了吗？
3. `badge_semantics_verified`：该 style/version 的绿色到底是什么意思？
4. `presence_lookup_historical`：图片是历史动态查询结果还是固定/缓存/fallback？
5. `watcher_context_known`：对谁显示的状态？
6. `client_presence_inferred`：能否支持客户端/账号当时连接？
7. `human_availability_inferred`：能否支持真人愿意/能够聊天？

通常旧网 archive 最多可靠到 1—3。

第 7 层几乎不应只靠 Web artifact 推断。

---

# 21. 建议增加 `presence_evidence` schema

```yaml
presence_evidence:
  platform: qq
  artifact_type: web-presence-badge
  original_page_url: null
  badge_url_pattern: "http://wpa.qq.com/pa?p=..."

  presentity:
    account_identifier_observed: true
    account_identifier_republished: false

  watcher:
    type: archive-crawler
    relationship: unknown
    authenticated: unknown

  representation:
    badge_body_available: false
    observed_label: unknown
    visual_semantics_verified: false
    version_semantics_verified: false

  state_mapping:
    user_declared_status: unknown
    server_presence_state: unknown
    invisible_mapping: unknown
    cache_behavior: unknown

  handoff:
    tencent_uri_present: true
    historical_local_client_available: false
    historical_transaction_reproduced: false

  privacy:
    live_presence_probe_performed: false
    endpoint_republished: false
```

---

# 22. Preservation levels：presence artifact 不能只分“有/无”

建议使用：

## P0 — textual mention only

只剩“QQ在线”“点击和我聊天”等文字。

## P1 — HTML reference survives

保存 `<img>` / `<a>` 引用，但子资源缺失。

## P2 — badge image survives

至少有一份当时或 archive 保存的状态图像 body。

仍不代表状态查询可验证。

## P3 — badge semantics/version survives

能用同期文档确认 style 与 online/offline/other mapping。

## P4 — generator/help configuration survives

能验证当时如何选择样式、QQ 号、来源站点、隐私/安全设置。

## P5 — protocol handoff environment understood

能验证 `tencent://` 当时如何交给本地 QQ，以及必要客户端/OS 条件。

## P6 — historical dynamic transaction evidence

存在足以说明某一历史请求怎样映射到状态表示的 contemporaneous technical evidence。

这不要求、也不鼓励去探测普通个人账号。

## P7 — privacy-safe complete architecture case

把页面、badge、状态服务、权限和本地 handoff 关系都解释清楚，同时不公开普通人的私人会话或联系方式。

本轮没有达到 P6/P7。

---

# 23. 浏览器/操作系统环境：历史页面回放不是只有 IE/CSS 问题

QQ Web Presence 还有一个 old-Web 常见却容易漏掉的依赖：

```text
custom URL protocol handler
```

即便 HTML 在 modern Chromium 中完全呈现：

- `tencent://` 可能没有处理器；
- 现代安全策略可能弹额外确认；
- 历史 QQ 客户端可能无法登录；
- 参数可能已废弃；
- 临时会话服务端策略已变；
- 账号已回收/换主。

因此：

> **modern page renders correctly != historical interaction path works**。

M3 浏览器复原实验以后可以把这个对象纳入：

```text
IE6/QQ2008-era environment
vs modern Chromium without QQ protocol handler
```

比较至少：

- 页面是否显示；
- 动态图片是否加载；
- 点击是否调用本地客户端；
- 安全提示差异；
- 失败路径。

但任何实验必须标 reconstruction。

---

# 24. 隐私：不要为了验证“在线状态”去探测历史普通人账号

presence 研究天然诱惑研究者做：

```text
把旧 QQ 号塞进今天的状态接口
→ 看看还在线不在线
```

本仓默认禁止这种做法，除非对象是明确的测试账号/研究者自己控制账号，并且不涉及普通人。

原因：

- 号码可能已换主；
- 可能重新激活仍由真实个人使用；
- live probe 会产生新的观测，不是历史证据；
- 可能重新暴露一个已沉睡的个人联系端点。

默认字段：

```yaml
live_probe:
  performed: false
  reason: privacy-and-historical-validity
```

研究目标是恢复**状态机制**，不是恢复“谁在几点在线”的个人监控数据库。

---

# 25. 一个重要的新历史偏差：公开 Web 更容易保存“愿意被陌生人找到”的人

Web Presence 天然偏向：

- 网店；
- 个人站长；
- 博客作者；
- 论坛签名；
- 客服；
- 希望扩大社交/业务联系的人。

而最依赖：

- 隐身；
- 好友可见；
- 黑名单；
- 私人好友列表；

的人，反而更少留下公开状态表面。

于是 archive 容易产生：

> “旧网用户都愿意公开 QQ、随时聊天”的错觉。

准确规则：

> **archive-visible presence culture != ordinary presence practice**。

公开 badge 样本对“愿意被联系的人”存在结构性过采样。

---

# 26. 同时代第一人称材料也要按 artifact 状态降级

今天仍可见的 WordPress 个人博客中，有一篇内部日期标为 2008-08-18 的《状态》，作者说别人常问为什么不见自己上 MSN，自己实际选择隐身；同时回忆早期 QQ 一上线多个好友头像闪动、同时开多窗口聊天。

Source:

- https://fanbst.wordpress.com/

建议证据标记：

```yaml
evidence_grade: A-like/C-sensitive
artifact_status: surviving-page-with-contemporaneous-internal-date
historical_hosting_verified: false
byte_identity_verified: false
personal_identity_reconstruction: prohibited
```

用途仅限：

- 证明“隐身作为主动社交策略”至少存在同期个人自述；
- 不证明群体普遍性；
- 不用于确定具体 QQ/MSN 技术版本。

这延续本仓已有 sickbaby guestbook 的处理原则：

> surviving contemporaneous content 很有价值，但不是 verified historical capture。

---

# 27. 2008—2010 Web Presence 还改变了网页“营业状态”的表达

2010 的网店经营者材料提示：

```text
static business page
+
current IM presence badge
```

会产生一种旧网页以前不容易拥有的属性：

> **页面本身虽然是静态的，但其中一个小图标告诉访客“现在大概有人能接待”。**

这类似后来：

- 在线客服绿点；
- chat widget；
- support agent available；
- live chat opening hours。

因此 Web Presence 可以被视为一种早期：

**`human availability embedded in page / 页面嵌入的人类可用性`**。

它值得和普通“联系我们”页面分开建模。

---

# 28. 不能把 presence 当成“实时”而不检查延迟

即使服务设计目标是即时状态，也可能存在：

- 客户端上报延迟；
- 服务端传播延迟；
- badge cache；
- 浏览器 cache；
- archive proxy；
- 网络失败；
- 用户空闲自动切换延迟。

因此最好写：

```text
near-real-time presence representation
```

而不是无条件写：

```text
real-time human status
```

对具体 artifact，若没有时序证据，不推断秒级准确性。

---

# 29. 2010 后的 V3.0 证明“更多可达”与“更多防骚扰”同步增长

QQ 在线状态 V3.0 同时提高：

- 陌生人发起临时会话能力；
- 文件/音视频能力；

又增加：

- 主人先开通；
- 黑白名单；
- 屏蔽来源；
- 安全等级；
- 隐藏 QQ 号等。

这很适合旧网平台史的一个更普遍判断：

> **availability expansion tends to create a parallel boundary-management layer.**

也就是：

```text
more ways to reach me
→ more reasons to build filters
```

这条规律以后可以与：

- Email spam filter；
- forum private-message permissions；
- blog comment moderation；
- SMS anti-spam；
- work-group mute；

做跨专题比较。

---

# 30. 本轮 archive 探索与负证据

本轮围绕以下历史对象进行了公开检索和 replay 尝试：

```text
http://is.qq.com/webpresence/
http://is.qq.com/webpresence/code.shtml
http://wpa.qq.com/pa
```

并寻找 2004—2010 的 Wayback locator / memento。

结果：

- 公开搜索找到大量同期教程、代码和服务 URL；
- 本轮没有得到一份可以实际核验的 historical memento；
- 直接构造特定 Wayback replay URL 时，当前访问链的 URL 安全限制阻止继续打开；
- 因而没有取得可可靠记录的 `capture_datetime / HTTP / charset / DOM / form action / JS / badge body / subresource capture datetime`。

按照 `docs/METHOD.md`：

```text
candidate historical URL / service locator
!= verified archive capture
```

因此本轮结论为：

> **M1 verified Web Presence capture: NOT ACHIEVED IN THIS SLICE.**

不能写：

> “Wayback 没保存。”

准确写法只能是：

> “本轮在当前访问链下尚未验证到。”

下一轮若有可访问 archive，应优先从 2004/2006/2007 同期文章中已经保存的 exact original URL 继续定位。

---

# 31. Evidence table

| Evidence | Date | Grade | Supports | Does not support |
|---|---:|---:|---|---|
| Tencent QQ2000 release | 2000-11-17 | A | invisible, away message, privacy features exist as official claims | later Web Presence mapping |
| RFC 2778 | 2000-02 | A | presentity/watcher/status/access-rule conceptual model | QQ implementation details |
| Sina Mobile OICQ report | 2001-03-06 | B+ | PC IM ↔ SMS/WAP gateway and friend-status querying | every region/user access |
| Google Groups surviving post | 2004-11-04 | A-like | Web Presence URL and function publicly described | official launch date / historical bytes |
| 2006 tutorial/periodical | 2006 | B/A-like | status-code generation entered web-authoring practice | backend semantics |
| Blog园 preserved code | 2007-03-09 | B+ | `wpa.qq.com/pa` + `tencent://message` exact code form | actual message transaction |
| Blog园 Web Presence tutorial | 2008-09-10 | B | button shown as online state + temporary chat | exact invisible mapping |
| surviving first-person blog | 2008-08-18 | A-like/C-sensitive | one user intentionally used invisible mode | population pattern |
| Blog园 protocol explanation | 2009-03-06 | B | `tencent://` local protocol-handler mechanism | QQ server internals |
| DOIT QQ status V3.0 | 2010-09-20 | B | temporary-session/security settings + shopkeeper use | nationwide prevalence |

---

# 32. 已证实 / 高概率 / 不知道

## 已证实

- QQ2000 官方已经有隐身和离开留言；
- 2004 年已有公开同期材料传播 QQ Web Presence URL；
- 2007 年同期网页代码包含 `wpa.qq.com/pa` 图片和 `tencent://message`；
- 2008 年教程把 Web Presence 描述为网页/论坛中的在线状态与临时会话入口；
- 2010 V3.0 叠加了临时会话、来源/黑白名单和安全策略；
- 至少存在一个同期网店经营者把该入口用于业务咨询的报道个案。

## 高概率但仍需更强技术证据

- `wpa.qq.com/pa` 在服务端依据账号状态动态生成/返回不同状态表示；
- badge 可能受缓存、权限和用户状态影响；
- archive 抓取 HTML 与动态 badge 可能存在时间错位。

这些是合理技术重建，暂属 D/high-probability，不冒充 original implementation。

## 不知道

- 2004—2010 每个版本对 `Invisible / Away / Busy` 的 web badge 映射；
- stranger visitor 与 buddy watcher 是否总看见相同状态；
- badge 的具体缓存策略；
- 某个普通人的 capture 里绿色图标是否真的来自历史动态查询；
- 本轮未取得 verified memento，因此不能确认原页面 DOM/charset/子资源完整性。

---

# 33. 后见之明风险

1. 不把今天的微信“在线/已读”争论倒投到 QQ2000；
2. 不把 `Invisible` 简化成“隐私模式 = 完全离线”；
3. 不把 Web Presence 的存在写成所有个人主页都公开 QQ；
4. 不把网店案例写成 C2C 全行业标准；
5. 不把 today-live `wpa.qq.com` 行为当成 2007 行为；
6. 不把今天的 QQ 号控制者当成历史控制者；
7. 不用 live probe 补历史状态；
8. 不把 search-result snippet 或 surviving tutorial 当成 Wayback capture；
9. 不把 archive 图标颜色写成人真实注意力；
10. 不把 modern browser 能启动某个 URL scheme 当成历史 IE/QQ 环境已复原。

---

# 34. 下一步 bounded tasks

## A. 找 verified memento

优先 URL：

```text
http://is.qq.com/webpresence/
http://is.qq.com/webpresence/code.shtml
```

目标年份：

```text
2004
2006
2007
2008
2010
```

记录：

- exact original URL；
- capture datetime；
- HTTP/replay state；
- charset；
- DOM；
- form fields；
- generated-code pattern；
- JS；
- badge subresource URL；
- badge capture datetime。

## B. 钉 badge semantics

寻找同期官方帮助/客户端 help/教程，确认：

- online/offline 图片 style mapping；
- invisible behavior；
- away/busy 是否折叠成 online/offline；
- stranger watcher policy。

## C. 做 privacy-safe reconstruction

只用：

- 自己控制的测试账号；或
- 完全离线模拟 state service。

不得探测历史普通人 QQ。

## D. 浏览器差异实验

比较：

- IE6-era + registered custom URL protocol；
- modern Chromium without handler；
- archived HTML with missing badge；
- archived HTML with frozen badge。

所有输出标 reconstruction。

## E. 比较其他中文旧网 presence

可选：

- MSN 网页在线状态；
- 阿里旺旺在线客服；
- Skype status button；
- 百度 Hi；

但只在能取得同期中文 Web 证据时做，不把本仓扩成全球 IM 史。

---

# 35. 本轮改变了什么

此前旧网页中的 QQ 按钮很容易被当成一种普通“联系方式图标”。

本轮以后，应把它看成一个**跨越至少三个系统的瞬时事务**：

```text
Web page
→ presence service
→ human availability representation

and

Web page
→ custom URL protocol
→ local QQ client
→ IM service
→ another human
```

这也解释了为什么这种 artifact 比普通静态链接难保存得多。

网页可以活着，图标可以活着，甚至 `tencent://` 字符串也可以活着；可真正让它有意义的那一刻——对方是否连着、对谁隐身、有没有在电脑旁、愿不愿被打扰——几乎都在 archive 之外。

所以旧网考古在这里必须学会承认一个看似反常的结论：

> **我们有时能把“在线”那个绿色小人保存二十年，却无法据此知道，那个人在那一分钟究竟有没有空。**

这不是材料不足的偶然，而是 presence 这种历史对象本身的结构：它生来就是短暂、关系依赖、可隐藏、可自动改变，并且主要服务于“现在”。
