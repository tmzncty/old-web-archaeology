# SMS × Web：短信网关、订阅、SP 计费、投递与控制层状态缺口（中文互联网，2000—2015）

> Cross-repo life-history companion: `tmzncty/how-people-lived/topics/from-text-me-when-you-arrive-to-verification-codes-sms-micro-coordination-and-channel-role-inversion-china-1998-2026.zh-CN.md`

## 0. Scope：这不是“短信发展史”

本仓 scope 仍然保持约 1995—2015 中文旧网。本专题不把蜂窝短信史无限前移，也不把全球 SMS 史塞进中文旧网仓。

研究对象是 **2000—2015 中文 Web 与 SMS 之间的接口**：

- 门户网站怎样让用户在 Web/WAP 上订短信；
- SP、门户、运营商、短信网关、SMSC、计费系统之间有哪些不同状态；
- 一个网页上的“订阅成功”与手机真正收到消息之间隔了什么；
- 退订、投诉、代收费为什么必须保留独立状态；
- 后来 OTP、账号恢复、交易通知出现以后，SMS 怎样从“内容服务”逐渐变成 Web/App 的控制通道；
- 公共 archive 能保存哪些 HTML/帮助页，却为什么几乎不可能单靠这些页面复原一条真实历史短信事务。

中国 2000 年以前的移动通信和寻呼只作为必要前史边界；全球第一条 SMS、海外 adoption 等放到 `how-people-lived` companion 中处理。

---

## 1. 研究单位：不能把“短信服务”当成一个对象

按本仓 `METHOD.md`，至少拆成以下研究单位：

### platform / service

例如某门户“奥运快讯”、天气订阅、邮件提醒、短信密保、验证码服务。

### site / host

例如：

- `tech.sina.com.cn` 的业务说明；
- 门户短信频道；
- SP 订阅/退订帮助页；
- 运营商网上营业厅。

### account / subscriber relation

某一手机号与某一 SP/门户业务之间是否存在订阅、绑定、计费或通知关系。

### page / URL

介绍页、订阅页、确认页、退订帮助页、资费页、验证码请求页。

### backend transaction

订阅请求、确认、网关提交、SMSC 接收、网间路由、投递、计费、退订、投诉处理。

### handset-side artifact

手机中实际出现的一条短信、发件代码、时间、分段状态、用户是否阅读。

### capture

archive 对上述**网页表层**在某一时刻的保存；通常不等于后台 transaction。

---

## 2. 最小 claim list

本专题当前只推进以下窄 claim：

1. **2000 年 8 月，新浪同期页面明确描述了 PC/WAP Web 订阅 → Internet 网站 → SMS 中心 → 手机收取的跨网络服务链。**
2. **2000—2002，短信服务从运营商内部开通、预付费扩展到移动/联通网间互通，不能把三个状态压成“2000 年短信已全面普及”。**
3. **2004 年信息产业部监管文件证明，订阅确认、资费、退订、代收费、原始计费记录和投诉处理已经是独立事务状态。**
4. **一个 Web 页面显示“已提交/已订阅”不能证明 SMS 已被运营商接受、手机已收到、用户已看到或采取行动。**
5. **2010s 的 OTP/登录验证使 SMS 越来越承担 Internet account/control-plane 功能，但短信总量不能直接解释为人际短信使用。**
6. **历史 Web capture 即使保存了订阅表单，也通常无法复原真实 subscriber state、billing state 与 delivery state。**

后续若不能取得更强 capture，不把这些 claim 扩写成完整的平台技术史。

---

## 3. 2000：一个非常清楚的 Web → SMS handoff

2000 年 8 月 30 日新浪科技发布《新浪网推出奥运短信息手机点播服务》，说明 8 月 25 日新浪与中国移动推出“全球通奥运快讯”。页面明确写到：

- 面向支持中文 SMS 的全球通手机用户；
- “将短信中心与互联网连接”；
- 用户可以通过 PC 或 WAP 手机登录网站订购信息；
- Internet 网站根据用户要求把信息以短消息形式发送到手机。

Source:
- 新浪科技，2000-08-30: https://tech.sina.com.cn/internet/china/2000-08-30/35284.shtml

**Evidence:** A/B — contemporaneous platform announcement available as a live legacy article today. It is strong evidence for the claim “Sina described such a service flow in 2000”; it is **not** a verified 2000 archive capture of the page’s historical rendering.

最小状态链：

```text
[用户知道服务存在]
        ↓
[PC/WAP 打开订阅入口]
        ↓
[选择内容 / 提交手机号]
        ↓
[门户记录 subscription request]
        ↓
[门户/互联网业务系统生成消息]
        ↓
[SMS gateway / operator interface 接受？]
        ↓
[SMSC 接受？]
        ↓
[目标网络可达？]
        ↓
[手机收到？]
        ↓
[用户看到？]
```

必须固定：

`subscription page exists != user subscribed`

`form submitted != portal subscription committed`

`portal says sent != operator gateway accepted`

`gateway accepted != handset delivered`

`handset delivered != human read`

`read != real-world action`

---

## 4. 2000—2002：网络“有短信”与社会关系“互相可达”不是同一个状态

中国电子报 2007 年整理业务节点时记录：

- 2000-05-17，中国移动正式开通 SMS；
- 2001-05-17，向神州行用户开通；
- 2002 年 5 月，中国移动、中国联通实现短信互通。

Source:
- 中国电子报 / 新浪科技，2007-04-17: https://tech.sina.com.cn/t/2007-04-17/15121469621.shtml

**Evidence:** B — industry retrospective, useful for service chronology.

因此旧网复原若看到 2000 年某门户写“手机用户均可……”，必须继续问：

- 哪家运营商；
- 哪种套餐；
- 是否支持中文；
- 是否必须是全球通而非神州行；
- 对端是不是同网；
- 网间 SMS 当时是否互通；
- 页面上的 eligibility 文案有没有随着后台业务扩展而更新。

不能从今天仍活着的同一篇新闻页面推断 2000—2002 三个年份的 eligibility 一致。

---

## 5. 2003—2004：SP 订阅把“合意”和“计费”变成需要单独保存的状态

2004 年信息产业部《关于规范短信息服务有关问题的通知》是本专题目前最强的一组状态证据。它并不只是“监管垃圾短信”，而是直接定义了一个可用于考古的 transaction contract。

Source:
- 信息产业部，2004-04-15: https://www.miit.gov.cn/jgsj/xgj/fwjd/art/2020/art_65f1dfb5208e4277979ed7f05a82ddad.html
- 信息产业部，2004-04-30 政策解读: https://www.miit.gov.cn/zwgk/zcjd/art/2020/art_23c3764afa874e24b11bf534947a6ac8.html

**Evidence:** A — contemporaneous regulatory record; current URL/CMS is not the historical 2004 Web rendering.

文件要求：

- 宣传中明示资费与退订方法；
- 包月/订阅业务先发送确认消息，确认消息必须写资费；
- 用户未反馈确认，视为撤销申请；
- 记录短信发送/接收时间与两端号码/代码，至少保存 5 个月；
- `0000` 查询某 SP 全部订阅，`00000` 一次退订全部；
- 账单展示 SP 名称、代码、代收费金额；
- 投诉无法及时确认责任时存在暂退费处理。

这意味着 2004 年不能再用二元状态：

```text
未订阅 / 已订阅
```

更准确的是：

```text
DISCOVERED
→ REQUEST_SUBMITTED
→ CONFIRMATION_SENT
→ CONFIRMATION_DELIVERED?
→ USER_CONFIRMED?
→ SUBSCRIPTION_ACTIVE
→ CONTENT_SENT
→ BILLING_EVENT_CREATED
→ CARRIER_BILLED
→ USER_RECEIVED?
→ USER_REQUESTED_CANCEL?
→ CANCEL_RECORDED?
→ BILLING_STOPPED?
→ CONTENT_STOPPED?
```

这里有至少三个不同的“退出成功”：

1. SP 数据库把订阅标为取消；
2. 不再产生后续信息费；
3. 手机不再收到内容。

它们不能被一个 Web “退订成功”页面合并。

---

## 6. 计费 evidence 与消息 content 必须拆开

2004 监管规则要求保留的核心原始数据包括发送/接收时间和双方号码/代码，主要用于计费争议和监管。

这提示 archive 工作需要区分：

### A. message-content evidence

“当时那条短信具体写了什么？”

### B. transaction/charging evidence

“何时、哪个代码向哪个号码发了多少条，产生了什么费用？”

### C. subscription-consent evidence

“用户是否明确请求/确认了这个持续服务？”

一个媒体报道可能复述 content，却没有 B/C；一张账单可能有 B，却没有 content；一个订阅网页 capture 可能只保存 UI，三者都不完整。

因此：

`message text survives != delivery transaction survives`

`billing line exists != user consent proven`

`subscription page capture != historical subscription state`

---

## 7. 从“内容服务”到“控制层”：old Web 后期必须开始分离短信的两种角色

2000s 前半，门户/SP 的短信业务常把 SMS 本身当作商品或内容终点：

- 体育比分；
- 新闻；
- 天气；
- 铃声/娱乐；
- 包月提醒。

到 2000s 后半至 2010s，SMS 越来越频繁承担另一种角色：

```text
Web/App 事务正在别处发生
→ 系统发一条 SMS
→ 用户凭 SMS 完成/恢复/确认另一项事务
```

典型包括：

- 账号绑定；
- 密码恢复；
- 一次性验证码；
- 银行风险通知；
- 票务/物流状态；
- 预约提醒。

这个阶段与本仓既有 companion 强交叉：

- `docs/MOBILE_NUMBER_BINDING_SMS_RECOVERY_REAL_NAME_PORTABILITY_AND_RECYCLED_IDENTITY_STATE_GAPS_2003_2015.md`
- `docs/PASSWORD_LOGIN_RECOVERY_QUESTION_EMAIL_SMS_SESSION_AND_ACCOUNT_CONTROL_STATE_GAPS_1998_2015.md`
- `docs/ONLINE_BANKING_*`
- `docs/PARCEL_EXPRESS_TRACKING_*`
- `docs/HOSPITAL_*`

本专题不重复这些领域的完整事务，而是提供公共 SMS handoff 模型。

---

## 8. OTP 的最小状态机

到 OTP 阶段，一个典型 Web/SMS 事务应至少拆成：

```text
[Web/App 用户请求验证码]
        ↓
[应用验证 request eligibility]
        ↓
[OTP generated]
        ↓
[OTP bound to account / number / action / expiry]
        ↓
[SMS gateway request created]
        ↓
[carrier/SMSC accepts?]
        ↓
[handset receives?]
        ↓
[user sees code?]
        ↓
[user submits code?]
        ↓
[server verifies code + expiry + context]
        ↓
[next transaction state]
```

必须固定：

`OTP generated != SMS sent`

`SMS sent != delivered`

`delivered to number != intended person received`

`OTP correct != all identity facts verified`

`OTP verified != final transaction succeeded`

`historical OTP form capture != historical account-control evidence`

---

## 9. “网页能开”仍然不能证明旧短信服务能运行

SMS × Web 案例特别容易产生一种假复原：

1. archive 保存了订阅页；
2. 表单还看得到；
3. 研究者就说“这个服务已经复原”。

实际上最关键的依赖可能都已经死了：

```text
HTML form
  ↓
form action endpoint
  ↓
portal user DB
  ↓
SP subscriber DB
  ↓
operator gateway credentials
  ↓
SMSC route
  ↓
billing relation
  ↓
historical mobile number state
```

所以：

> **`historical page replay != historical SMS transaction replay`**

哪怕 archive 保存了 HTML、CSS、JS，也不能为了“演示”向今天可能已经二次放号的手机号重新发送消息。

---

## 10. Browser / charset / WAP 条件

2000 年新浪材料明确同时提到 PC 与 WAP，因此任何具体 reconstruction 至少需要记录：

- PC Web 与 WAP 是否是同一 URL/表单；
- 当年页面 charset；
- 手机号码输入格式；
- 是否依赖登录 cookie；
- JS validation 是否影响提交；
- WAP/WML 页面是否独立存在；
- 后台是否根据运营商/号段判断 eligibility；
- 短信内容的中文编码/拆分是否改变实际消息数量。

最后一点目前**没有在本 slice 中取得足够原始实现证据**，所以不填具体 GSM 字符数/中文分段数来冒充这个历史服务的实际实现。

---

## 11. 2007—2010：为什么个人日常使用证据仍然需要离开 Web 页面找

2007 年《青年参考》转载的一组材料中，一名 20 岁房地产经纪人没有电脑，每几周才去网吧看 Email，却每天用 SMS 约朋友吃饭。

Source:
- 《青年参考》/新浪新闻，2007-11-07: https://news.sina.com.cn/c/2007-11-07/144814255660.shtml

**Evidence:** B — contemporaneous first-person.

这条材料与 portal/SP capture 的证据类型完全不同：

- 门户页可以证明“服务存在/怎样宣称操作”；
- 用户材料才可能证明“普通人怎样把 SMS 放进生活”；
- 但一个个案不能推出全国代表性。

旧网考古尤其要避免只研究那些本来就最容易被 archive 保存的 Web 页面，然后得出“当时数字生活主要发生在 Web 页面里”。

---

## 12. 2019 以后发生的角色反转，为什么仍然属于 old-Web 的解释边界

本仓不把研究对象扩张到 2020s 平台史，但需要用后来的结果帮助识别 2000—2015 哪些 state transition 值得保存。

工信部 2019 年通信业统计公报记录，全国移动短信业务量同比增长 37.5%，并明确指出网络登录和用户身份认证等安全服务推动了短信量增长。

Source:
- 工业和信息化部，《2019年通信业统计公报》: https://www.miit.gov.cn/gxsj/tjfx/txy/art/2020/art_2d61a3d279ba4d53aa944359d20b8d7f.html

**Evidence:** A2 — official statistics after this repo’s main scope.

这个后续结果反过来提醒 old-Web 研究：2000s 的短信 portal/SP 页面不能只作为“过时内容服务”收藏。它们也是后来 Web→SMS 控制链的早期基础设施前身。

但不能倒推：

`2000 年 Web→SMS existed != 2000 年已存在 2019 式 OTP 生态`

---

## 13. Archive evidence model

若后续取得一份真正历史 capture，至少记录：

```yaml
original_url:
capture_url:
capture_datetime:
archive_source:
accessed_at:
http_status:
content_type:
charset:
page_type: intro | subscribe | confirm | unsubscribe | tariff | help
browser_assumption:
requires_login:
form_action_visible:
phone_field_visible:
operator_selector_visible:
price_visible:
unsubscribe_instruction_visible:
subresources:
  css:
  js:
  images:
  wap_links:
backend_state_observable: false
sms_delivery_observable: false
billing_state_observable: false
confidence:
```

任何 `backend_state_observable: false` 的 capture，都不得用截图“补”成真实订阅成功记录。

---

## 14. 当前 historical-capture 尝试

本 slice 对新浪 2000 年奥运短信页面进行了 archive locator/replay 探索：

Original Resource candidate:
- `http://tech.sina.com.cn/internet/china/2000-08-30/35284.shtml`

目前公开 Web 搜索没有返回可直接检查的 Wayback replay；直接构造 Wayback replay/CDX 路径又被当前研究访问链的 URL 安全限制拒绝。

因此当前只能记录：

```text
live legacy article: VERIFIED
historical article content/date claim: SUPPORTED by contemporaneous article
Wayback candidate locator: NOT VERIFIED
historical replay: NOT ACHIEVED IN THIS SLICE
historical HTTP/charset/DOM/subresources: UNKNOWN
historical form action/backend transaction: UNKNOWN
```

根据 `docs/METHOD.md`：

> 搜索结果里的 locator 不等于 verified capture；“这轮没有验证到”也不能写成“Wayback 当年没有保存”。

**M1 contribution in this slice: NOT ACHIEVED.**

---

## 15. Preservation levels：短信服务不能只按“页面还在不在”分级

建议 SMS/Web 案例采用：

### S0 — citation only

只有后来的文字提及。

### S1 — service/page shell

有业务介绍/帮助页正文，但没有 historical capture 或可执行事务。

### S2 — verified historical page capture

有可检查的原始 URL、capture datetime、HTTP/charset/DOM 和资源缺失记录。

### S3 — historical UI/action semantics

能够可靠确定当时表单字段、资费、确认/退订路径、浏览器/WAP 条件。

### S4 — transaction-side evidence

另有同时代订阅/计费/投诉/日志证据，能证明至少一段后台状态变化。

### S5 — delivery/outcome evidence

有最小化、合法且隐私合规的证据证明某消息实际到达并进入真实生活行动。

绝大多数公共 archive 最多达到 S2/S3；S4/S5 不应靠 reconstruction 伪造。

---

## 16. Privacy：不要为了证明“短信真的用过”而重新公开私人短信

短信恰好是 ordinary digital life 中最私密、最不适合批量再发布的一层。

本仓应优先保存：

- 平台/运营商公开规则；
- 公开帮助页；
- URL 与 capture metadata；
- 去身份化 state model；
- 同期媒体中已经公开、只保留支持 claim 所需的最少个人信息。

不要：

- 批量收集二手手机里的私人 SMS；
- 重新公开手机号；
- 因为旧号码看似失效就尝试发送测试短信；
- 用今天的手机号去验证历史 subscription endpoint；
- 把短信内容与真实姓名重新拼接成可搜索档案。

---

## 17. 证据表

| Claim | Source | Grade | Supports | Does not support |
|---|---|---:|---|---|
| 2000 新浪描述 Web/WAP→SMS 奥运服务 | 新浪科技 2000-08-30 | A/B | contemporaneous announced flow | historical rendering / actual delivery rate |
| 2000/2001/2002 开通、预付费、网间互通节点 | 中国电子报 2007 | B | service chronology | mass adoption by each population |
| 2004 短信订阅确认、退订、计费记录有正式规范 | 信息产业部 2004 | A | state/rights requirements | every SP actually complied |
| 2007 无电脑年轻人日常使用 SMS | 青年参考同期个案 | B | lived-use possibility | national representativeness |
| 2019 SMS 量增长与登录/身份认证有关 | 工信部 2019 统计公报 | A2 | later channel-role inversion | exact 2000s causal pathway |

---

## 18. 后见之明风险

### 风险 1：把短信写成“微信前的落后 IM”

错。它首先是蜂窝网络里的 store-and-forward channel，终端门槛、计费、覆盖和可达方式都不同。

### 风险 2：把今天的 OTP 用途投射回 2000

错。2000 新浪案例证明的是内容订阅 Web→SMS handoff，不是今天的身份认证生态。

### 风险 3：从发送量推导个人行为

错。门户批量推送、SP 内容、验证码等都会改变总量。

### 风险 4：把监管文本当成实际合规证明

错。2004 文件证明“规则要求什么、当时投诉什么”，不证明每家 SP 每次都按规则执行。

### 风险 5：把 current live legacy page 当历史页面

错。今天 `tech.sina.com.cn` 还能返回 2000 正文，只能证明这份历史内容对象被现有服务保存；当前 HTML/CSS/广告/HTTPS/DOM 包装不是 2000 浏览体验。

---

## 19. 下一步真正值得做什么

按仓库 ROADMAP，下一步价值最高的不是继续写更多 narrative，而是取得一份可核验 historical capture，最好来自以下对象之一：

1. 2000—2002 门户短信订阅页；
2. 2003—2004 SP 资费/退订页；
3. 同一业务至少两个历史时点，观察字段、运营商选择和退订说明变化；
4. 若有合法公开数据，再把一份 UI capture 与一份同时代计费/投诉 evidence family 对齐。

如果 archive 只剩业务介绍正文、订阅 endpoint 和子资源全部丢失，应把“不可可靠复原真实事务”作为结论，而不是填充 mock backend。

---

## 20. 这份 companion 改变了什么

旧中文 Web 不只是页面、BBS 和个人主页。

从很早开始，它就能把一项事务**交给另一个网络继续执行**：用户在浏览器里点一次订阅，后面的内容可能连续几天从蜂窝网络抵达手机；用户甚至不必再次打开那个网站。

因此考古对象不能停在 HTML：

```text
old Web page
→ subscriber state
→ SP / portal backend
→ operator gateway
→ SMSC
→ handset
→ human action
```

**页面最容易被保存，却只是这条链里最表面的一层。真正改变普通生活的，往往恰恰发生在 archive 最难看到的那一段：页面已经关掉以后，手机口袋里有没有真的响一声。**
