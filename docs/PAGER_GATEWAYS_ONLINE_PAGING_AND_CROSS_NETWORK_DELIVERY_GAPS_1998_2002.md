# PAGER_GATEWAYS_ONLINE_PAGING_AND_CROSS_NETWORK_DELIVERY_GAPS_1998_2002

## 研究问题

1998—2002 年中文旧网里经常出现今天已经很陌生的一组词：

- 网上寻呼；
- 网络寻呼机；
- Email 到达寻呼；
- 电子邮件增值服务；
- 寻呼台；
- GSM 短消息；
- Web 规则设置；
- 通过传真取信。

如果只从今天的浏览器和产品分类出发，很容易把它们都理解成“早期即时通信”。

这是危险的。

在这一时期，至少存在两类完全不同的系统：

1. **Internet / Email → 物理寻呼网络 → 随身 pager**；
2. **Internet → 桌面客户端 / 在线账号 → 屏幕上的消息提醒**。

两者都可能使用“寻呼”这个词，但它们的：

- endpoint；
- 用户是否必须在线；
- 传输网络；
- 是否依赖电信运营商；
- 是否需要另外找电话回复；
- archive 能保存的证据层；

完全不同。

本文件建立一套针对这类跨网络旧网对象的 evidence contract，并提出一个新的 archive-gap 概念：

> **cross-network delivery gap（跨网络投递缺口）**：Web archive 往往能保存 HTTP 入口、帮助页和设置页，却无法证明消息后来是否穿过后台网关、寻呼运营网和无线链路真正到达用户终端。

本文只处理与约 1995–2015 中文旧网直接相关的 1998—2002 Web / Email / pager 交叉层，不把仓库扩展成完整电信史。更早的中国寻呼史、全球 pager 前史和普通生活影响放在 `tmzncty/how-people-lived`。

---

## 1. 开始前先固定研究单位

沿用 `docs/METHOD.md`，不要把品牌词当研究单位。

针对“网上寻呼”至少拆成：

```text
service / product
web page / form
user account
email mailbox
web-configured routing rule
server-side gateway
paging operator network
physical pager endpoint
SMS endpoint
fax endpoint
desktop IM endpoint
individual delivery event
callback / reply event
archive capture
claim
```

### 为什么必须这样拆

同一张网页可以证明：

- 当时有一个输入框；
- 当时平台宣称可以发到 pager；
- 当时允许用户设置转发规则；

却通常不能证明：

- 后台规则真的被保存；
- 某封邮件被网关解析；
- 寻呼台真的接受了投递；
- 无线网络真的把它发出；
- 用户的 pager 在覆盖区且有电；
- 用户真的读到了；
- 用户随后真的回电。

因此这类对象比普通静态网页更需要 **state / layer discipline**。

---

## 2. 最低术语区分：同一个“寻呼”不是同一种系统

建议为证据记录增加 `delivery_endpoint_type`。

### A. `physical-pager`

Internet 或 Email 只是消息来源，最终端是真实无线寻呼机。

典型链：

```text
web form / email
→ Internet-side server
→ gateway
→ paging operator
→ radio paging network
→ physical pager
```

### B. `mobile-sms`

Internet / Email 消息经过网关送到 GSM 短消息终端。

```text
email
→ gateway
→ mobile carrier SMS
→ mobile handset
```

### C. `fax`

Web / Email 侧通过后台服务把内容转成传真获取。

```text
mailbox
→ gateway
→ PSTN / fax service
→ fax machine
```

### D. `desktop-im`

所谓“网络寻呼机”实际是需要电脑 / 客户端在线或可连接服务器的桌面即时通信系统。

```text
desktop client
→ Internet service
→ account / presence / queue
→ another desktop client
```

这一类与 `physical-pager` 的差别尤其大。

因此必须固定：

> **same historical label ≠ same delivery graph**

以及：

> **“网络寻呼机”这个产品名称本身，不能证明物理寻呼网络参与。**

---

## 3. Evidence family A：1999 年国信网上寻呼

一份同期通信行业统计 / 业务总结资料在回顾 1999 年寻呼业时写到：

- 国信寻呼的 198 / 199 网络覆盖大量城市；
- “国信网源”提供网上寻呼；
- Internet 网上寻呼已经与全国 198 / 199 网络以及多个省级网络相连；
- 22 个省级寻呼网络已经开通“电子邮件到达寻呼”等业务。

来源：

- 新浪科技保存的 1999 年通信业统计资料，2000-06-14：<https://tech.sina.com.cn/it/2000-06-14/28155.shtml>

证据等级：**A/B：同期行业统计与运营业务说明**。

### 这个来源可以支持什么

可以支持：

> 1999 年中国物理寻呼网络已经存在 Internet-facing gateway，并提供 Web / Email 与 pager 网络之间的桥接服务。

### 不可以支持什么

不能单独支持：

- “网上寻呼”用户规模；
- 某个普通用户实际收过多少条；
- 一个历史网页表单的每次提交都成功送达；
- 1999 年所有“网络寻呼机”都属于国信物理寻呼系统。

### 需要继续寻找的原始 artifact

优先级较高：

- `国信网源` 历史 URL / capture；
- 网上寻呼输入页；
- 用户帮助页；
- 寻呼号码格式说明；
- 错误返回页；
- 是否需要登录；
- 浏览器 / 编码要求；
- 网关业务协议或用户手册。

本轮尚未验证这些具体 capture，因此不能把行业总结中的功能说明升级成已复原 Web UI。

---

## 4. Evidence family B：1999 年 Tencent Email → pager / SMS / fax

腾讯官方保留的一条 1999 年历史产品记录提供了更具体的后台流程。

1999 年 7 月 11 日，腾讯与深圳龙脉公司合作推出电子邮件增值服务系统，目标用户包括 ISP 拨号用户。

文章描述：

- 新邮件到达时系统可抽取发信人、主题和正文；
- 用户通过 Web 设置过滤规则、关键词和时间范围；
- 匹配后可以把邮件内容 / 提示送往寻呼台；
- 也可以送往 GSM 短消息；
- 还可以用传真取得信息。

来源：

- 腾讯官方历史文章，1999-07-11：<https://www.tencent.com/zh-cn/articles/80260.html>

证据等级：**A：公司同期产品记录 / 官方历史页**。

### 关键 archaeology 含义

这里的 Web 页只是一个**控制平面**。

真正的数据路径发生在后台：

```text
user opens web settings
→ rule saved on server

later:
new email arrives
→ server parses message
→ applies rule
→ dispatches to paging / GSM / fax system
→ external network handles delivery
```

这意味着：

> **archived configuration surface ≠ archived runtime execution**

即使未来取得 1999 年完整设置页 HTML，也仍然无法仅靠该 HTML 证明某封具体邮件曾经成功投递。

---

## 5. 这类 Web 不是“浏览网页”，而是控制另一个网络

旧网研究经常把页面作为最终对象。

pager gateway 提醒我们：某些页面真正重要的功能发生在页面之外。

建议区分：

| Layer | 例子 | Archive 常见可见性 |
|---|---|---|
| presentation | HTML 表单、帮助文字、图片 | 中—高 |
| user configuration | 转发规则、关键词、时间段 | 低；常需登录 |
| application server | rule engine、mail parser | 极低 |
| gateway | paging / SMS / fax connector | 极低 |
| carrier network | 寻呼运营网、GSM、PSTN | Web archive 几乎不可见 |
| radio / last mile | pager 是否收到 | 不可见 |
| human action | 看见、回电、忽略 | 不可见，除非另有个人史料 |

因此这类案例的核心问题应该是：

> **这个页面控制了什么？它控制的系统有没有留下独立证据？**

而不是只问“页面长什么样”。

---

## 6. 最小状态机：从网页到人的身体，中间至少有十几步

对 `web/email-to-physical-pager`，建议按以下状态记录：

```text
S0 service advertised
S1 web endpoint reachable
S2 user authenticated / permitted
S3 recipient identifier syntactically valid
S4 form submitted / mail received
S5 server accepted request
S6 routing/filter rule matched
S7 gateway created downstream dispatch
S8 paging operator accepted dispatch
S9 radio transmission attempted
S10 pager in coverage / powered
S11 message displayed on device
S12 user noticed message
S13 user understood required action
S14 user found reply channel if necessary
S15 reply completed
```

一个 archive capture 最多通常能支持 S0–S3 的部分信息。

服务器日志或运营商记录才可能支持 S4–S9。

个人同期日记 / BBS 才可能支持 S11–S15。

因此硬规则：

> **form displayed ≠ request accepted**

> **request accepted ≠ downstream dispatch**

> **dispatch ≠ pager receipt**

> **pager receipt ≠ human notice**

> **human notice ≠ callback / response**

---

## 7. CNNIC 1999 的“网上寻呼机”是使用证据，但不是产品识别证据

CNNIC 1999 年 7 月《中国 Internet 网络发展状况统计报告》在“用户通常使用哪些网络服务”的调查题中列出：

- 电子邮件 90.9%；
- 聊天 29.2%；
- BBS 28.0%；
- 个人主页 21.6%；
- 新闻组 21.4%；
- 网上寻呼机 14.8%；
- Internet 电话 8.4%。

来源：

- CNNIC 1999-07 PDF：<https://www.cnnic.cn/NMediaFile/old_attach/P020120612485127164902.pdf>

证据等级：**A：同期调查，但 selection-limited**。

### 代表性限制

报告自己说明，问卷主要通过当时多个网站在线征集，共获得 5 万余份有效答卷。

因此：

> `14.8% of survey respondents ≠ 14.8% of all Chinese residents`

甚至也不应未经抽样修正直接写成严格的“中国网民总体比例”。

### 语义限制

更重要的是，该统计项叫“网上寻呼机”，但调查表本身并未在当前定位材料中进一步拆出：

- Web→物理 pager；
- OICQ / desktop network pager；
- 其他即时消息服务。

因此：

> **survey category ≠ delivery endpoint classification**

CNNIC 数据可以证明“寻呼”作为一种网络服务范畴在 1999 在线用户语汇中可见，并且不是只有极少数人才认识；不能单独用来判定背后的物理网络。

---

## 8. 词汇考古：`寻呼` 从电信功能变成软件隐喻

1990 年代末“寻呼”已经是普通用户容易理解的概念：

> 我不要求对方正在和我通话，只需要把“有人找你 / 有消息”推到对方那里。

因此早期即时通信软件使用“网络寻呼机”之类命名并不奇怪。

但在考古上必须拒绝词源捷径：

```text
产品叫“网络寻呼机”
≠ 使用无线 pager 网络
≠ 与 198 / 199 寻呼台相连
```

如果一个 artifact 只有“寻呼”名称而没有 network path 证据，应该标记：

```yaml
historical_label: 网络寻呼机
physical_paging_network: unknown
endpoint_type: unknown_or_desktop_if_independently_verified
```

不能从名称自动补后端。

---

## 9. `requires_user_online` 是旧网服务的重要字段

同样叫“消息服务”，对普通生活的含义可能完全不同。

建议新增：

```yaml
requires_sender_online: true|false|unknown
requires_recipient_online: true|false|unknown
server_can_buffer: true|false|unknown
out_of_band_notification: pager|sms|phone|fax|none|unknown
```

### 物理 Email→pager gateway

收信人通常**不需要电脑此刻在线**。

消息先到服务器，再跨网络追到 pager。

### 桌面 IM

是否必须在线，要看具体版本是否支持离线消息 / server queue。

### 这对历史解释为什么重要

如果一个 1999 用户只有晚上回家拨号两小时：

- `has_email=true`；
- `Internet identity exists=true`；
- `continuously online=false`。

如果他又开了 Email→pager：

- `Internet-originating notification can reach mobile person=true`。

所以：

> **online identity ≠ online presence**

以及：

> **out-of-band notification can increase Internet reachability without increasing Internet connection time.**

---

## 10. 新 archive-gap：cross-network delivery gap

Wayback / Common Crawl 等 Web archive 的保存边界大致停在 HTTP(S) 可抓取对象。

但 pager gateway 的完整服务跨越：

```text
HTTP
→ application backend
→ mail system
→ proprietary / telecom gateway
→ paging carrier
→ radio network
→ physical device
```

因此哪怕网页保存完好，最后几层仍可能完全失踪。

定义：

> **cross-network delivery gap**：历史 Web artifact 能证明入口与宣称能力，却因为 downstream network 不属于 Web capture 边界，不能直接证明具体消息的后续投递与人类接收结果。

这个 gap 与普通“图片 404”不同。

它不是网页资源漏抓，而是**功能结果发生在另一个档案体系里**。

### 可能需要的其他证据源

- 电信运营商业务手册；
- paging gateway protocol 文档；
- 软件安装介质 / 客户端；
- 资费说明；
- 用户账单；
- 企业邮件系统说明；
- 同期 BBS 使用经验；
- 系统日志 / 测试记录（若公开保存）；
- 电信设备博物馆 / 档案。

这也是为什么本仓不能用 Web archive 单独宣布“服务复原完成”。

---

## 11. 新 outcome gap：notification outcome 也极难保存

即使 downstream 网络成功，普通人的动作仍然通常没有页面。

例如：

```text
Email arrives at 14:03
pager vibrates at 14:04
user sees subject at 14:07
finds a public phone at 14:18
calls office at 14:20
```

前两步也许在系统日志里；最后几步一般只存在于：

- 记忆；
- 日记；
- 聊天记录；
- 工作记录；
- 偶然的 BBS / 博客自述。

因此：

> **archived service capability ≠ historical behavioral integration**

这条规则正好与 how-people-lived 的采用阶梯对齐。

---

## 12. 1999 Tencent 页面还暴露了一种“配置页偏差”

Web archive 很可能更容易保存：

- 产品介绍；
- 新闻稿；
- 公共帮助页。

最难保存：

- 需要登录的个人过滤规则；
- 某个邮箱绑定哪个 pager；
- 哪些关键词会推送；
- 用户何时关闭服务；
- 失败重试；
- 账单和资费状态。

因此可以定义：

**configuration-survival gap（配置存续缺口）**。

公开页面告诉我们“系统允许怎样配置”；私人配置决定“这个人的实际系统怎样运行”。

后者不仅难保存，也涉及明显隐私问题，不应因技术上偶然可访问就批量重索引。

---

## 13. 联系信息本身也有隐私风险

1998—2002 年旧网页、个人主页、黄页和论坛签名里常直接出现：

- 寻呼号码；
- 手机号码；
- 家庭电话；
- Email；
- 单位；
- 真实姓名。

几十年后，这些普通人的号码和身份关系可能仍然具有隐私含义。

本仓遵循 `AGENTS.md` 和 `docs/METHOD.md`：

- 研究号码格式时优先抽象 pattern；
- 不批量重新公开历史普通用户联系表；
- 不因为 archive 可访问就建立“姓名 → pager → 手机 → Email”个人索引；
- 个案需要引用时只保留支持 claim 的最小信息；
- 不尝试联系历史账号本人进行身份确认，除非另有明确研究伦理设计。

---

## 14. 建议证据字段

未来 `evidence.schema` 若覆盖 transaction / gateway artifact，可考虑：

```yaml
subject: historical-service-or-page
observed_at: 1999-07-11

web_layer:
  original_url: null
  capture_url: null
  page_type: product-description
  auth_required: unknown

messaging_origin:
  channel: email
  mailbox_provider: isp

routing:
  user_configurable: true
  configuration_surface: web
  filter_fields:
    - sender
    - subject
    - body
    - time_window

delivery:
  endpoint_type:
    - physical_pager
    - gsm_sms
    - fax
  gateway_operator: unknown
  downstream_network: external
  acknowledgement_visible_to_user: unknown

presence:
  recipient_internet_online_required: false
  physical_device_required: true

reply:
  same_endpoint_reply_supported: unknown
  external_callback_possible: true

archive_gap:
  backend_state_preserved: false
  downstream_delivery_preserved: false
  user_notice_preserved: false

confidence: high_for_advertised_capability
```

字段的目的不是把史料伪装成完整 telemetry，而是强迫研究者明确：**我们究竟看见哪一层。**

---

## 15. 最小 claim templates

### 可以写

> 1999 年的同期行业资料记载，国信系统已经提供 Internet 网上寻呼，并在多个省级寻呼网络开通电子邮件到达寻呼。

### 不可以直接写

> 1999 年中国网民普遍通过 Internet 给 BP 机发消息。

---

### 可以写

> 腾讯 1999 年产品资料描述了一套面向拨号用户的电子邮件增值系统，用户可在 Web 设置规则，把匹配邮件通知转发到寻呼、GSM 短消息或传真通道。

### 不可以直接写

> 该系统的历史 Web 页面已被完整复原，且所有消息当时都可靠送达。

---

### 可以写

> CNNIC 1999 年在线调查的有效受访者中，14.8% 勾选了“网上寻呼机”。

### 不可以直接写

> 1999 年全国 14.8% 网民使用国信物理 pager gateway。

---

## 16. `exists / available / used / popular / caused` 的应用

### exists

同期资料证明服务被推出或功能被描述。

### available

需要进一步证明：

- 哪些 ISP / pager 网络；
- 哪些地区；
- 是否收费；
- 是否需要特定号码 / 账号；
- 是否对普通个人开放。

### used

CNNIC 分类、用户教程、同期用户自述可提供使用证据。

### popular

需要可靠 denominator，不能只拿网站宣传数字或在线问卷推总体。

### caused

要证明 gateway 改变工作 / 家庭行为，需要个体或组织行为材料，不能从产品出现直接推因果。

---

## 17. 与 OICQ / IM 谱系研究的边界

本文件不是 OICQ 技术史。

这里只建立一个必要的考古防错规则：

> **早期即时通信产品采用“网络寻呼机”语言时，不能因为词汇相同就与物理 pager gateway 合并。**

若后续专门研究 OICQ，应另做：

- 客户端版本；
- server architecture；
- offline message；
- presence；
- numeric ID；
- contact discovery；
- ICQ / pager metaphor；
- browser vs native client。

不要把本文件变成该专题的替代品。

---

## 18. 浏览器与编码问题

如果后续找到原始 `国信网源` / 邮件增值服务 capture，应记录：

- GB2312 / GBK / UTF-8；
- form action 是否被 archive rewrite；
- POST 是否可回放；
- 是否依赖 cookie；
- 是否依赖 JS；
- 是否有 frame / table layout；
- 是否 IE-specific；
- 号码输入框的 maxlength / validation；
- 原始 endpoint 是否已被域名复用；
- 是否要求登录后才能进入规则设置。

尤其注意：

> **archive 中表单“可以点击”不代表历史 backend 被回放。**

Wayback rewrite 后的提交行为不能当成 1999 服务行为。

---

## 19. 负证据与本轮未完成项

本轮已经确认：

- 1999 行业资料中存在国信 Internet→pager bridge；
- 1999 Tencent 产品记录存在 Email→pager/SMS/fax bridge；
- CNNIC 1999 在线用户调查里存在“网上寻呼机”服务类别。

本轮没有可靠取得并验证：

- 1999 `国信网源` 具体 Web capture；
- 具体 pager-send form 的原始 HTML；
- 一次真实跨网络投递日志；
- 普通用户的原始 BBS / 日记，能把 Email 到达、pager 提醒、回拨 / 上线处理串成同一事件；
- “网上寻呼机”问卷项到底如何定义每一种产品。

因此这些地方必须继续写 `unknown`。

> **没有找到历史 form capture ≠ 该 form 当时不存在。**

也不应使用现代重建页面填补。

---

## 20. 这改变了对中文旧网保存的哪一点理解？

传统网页考古很容易默认：

> 用户看到一个网页，页面本身就是主要历史对象。

跨网络 pager gateway 说明，早期中文 Internet 里有一批非常重要的页面其实只是**其他基础设施的控制面板或入口**。

它们的意义发生在页面之外：

```text
网页
→ 邮件服务器
→ 后台过滤规则
→ 电信网关
→ 寻呼 / GSM / 传真
→ 人
```

因此一个保存得非常漂亮的 HTML 页面，仍然可能只留下整个历史服务最表层的 10%。

这产生三条可复用的方法结论：

1. **archived interface ≠ archived execution**；
2. **same vocabulary ≠ same network topology**；
3. **Web preservation systematically under-preserves cross-network outcome.**

这套规则以后同样可以用于：

- Web→SMS；
- Web→fax；
- Email→voice notification；
- 早期网上银行→电话确认；
- 招聘网站→短信通知；
- 订票网站→线下取票 / 电话通知；
- 其他“网页只是入口”的混合系统。

但每个专题都必须另证，不能仅凭类比写成事实。

---

## 21. 与 `how-people-lived` 的交叉链接

普通生活层面的通信结构、寻呼与公用电话、拨号时代的间歇在线、青田果农联系栈以及美国 email-to-pager 对照，写入：

- `tmzncty/how-people-lived/topics/reachability-bridges-pagers-public-phones-and-intermittent-internet-china-1983-2002.zh-CN.md`

本仓只保留：

- 中文旧网侧的服务形态；
- Web / Email / pager 的证据边界；
- archive 能看到 / 看不到的层；
- 术语歧义；
- browser / endpoint / provenance contract。

这样可以避免把 `old-web-archaeology` 的 scope 无限前移成全球通信史。
