# Eldercare Hotline, One-Button Telecare, Remote Monitoring and Response State Gaps, 2007–2015

## Scope

本笔记研究约 2007–2015 中文旧 Web 及其相邻通信基础设施中，居家养老/空巢老人服务怎样被拆成：

- 电话热线；
- Web 查询；
- 短信 / email；
- 一键呼叫器；
- CDMA/GPS 老人手机；
- 视频/摄像头；
- 呼叫中心与服务商调度；
- 社区、助老员、亲属和急救人员的线下响应。

它**不是**中国养老政策史，也不把 2016 年以后 App、IoT、智能门磁、AI 养老平台无限塞入本仓。

跨国前史、2018–2026 后续和普通家庭生活史见 sister repository：

`tmzncty/how-people-lived/topics/from-phone-check-ins-to-one-button-telecare-empty-nest-ageing-in-place-and-care-radius-china-2007-2026.zh-CN.md`

本仓只问 old-Web archaeological questions：

> 当同期报道说“网上可查”“一键可呼”“远程可看”时，历史研究者究竟能够证明哪个 state？

按仓库 METHOD：

`platform ≠ site ≠ page ≠ capture ≠ transaction ≠ offline response`。

---

## 1. Evidence grade and this slice's boundary

沿用本仓 A/B/C/D：

- **A**：原始/同时代官方页面、公告、技术资料、可验证 archive capture；
- **B**：同期新闻、记者操作、用户/服务人员采访；
- **C**：多年后的回忆；
- **D**：研究者状态模型或复原。

本轮取得：

- 2007–2011 多份同期热线/服务平台报道；
- 北京 96156 的具体历史 host / subdomain locator；
- 杭州 2009 远程摄像头 + CDMA/GPS + 呼叫平台的同期 workflow；
- 杭州 2011 一键终端的按钮语义；
- 北京 2011 Web 志愿服务供需对接 locator；
- 2018 对 2008–2015 济南一键通使用结果的反向核查。

但本轮**没有实际取得并检查满足 M1 合同的 2007–2015 Wayback/WARC replay**。

因此以下继续为 `unknown`：

- 历史 HTTP headers / charset；
- `www.bjcs.gov.cn` 2009 DOM / frames / JS；
- 表单 `action`、GET/POST；
- session / cookie；
- 96156 Web 端是否支持真实 service request 还是只查信息；
- call-center internal queue / dispatch backend；
- 一键通终端 protocol；
- CDMA/GPS device-server protocol；
- camera stream transport / authentication；
- service completion callback；
- error/timeout/retry UI。

因此本笔记的 M1 状态是：

> **NOT ACHIEVED IN THIS SLICE.**

“本轮未验证到 capture”不得改写成“Wayback 没有保存”。

---

## 2. Historical locator family: Beijing 96156 was not one page and not one channel

### 2.1 2007–2008: telephone-first service

2007 年同期报道记录“96156亲情服务卡”：符合条件的老人可以拨 96156，就近获得家务、陪同、代办、维修等政府购买服务。[S1]

2008 年又加入“亲情倾听”和热线购药；空巢老人可以申请陪聊或定期问候。[S2]

这两个时点能证明：

```text
96156 service family exists
+ telephone intake exists
+ some requests route toward human/community service
```

它们**不能**证明 2007/2008 同时存在可完成同类事务的公开 Web application。

### 2.2 2009: concrete multi-channel locator

2009-09-01《新京报》同期说明给出：

- telephone: `96156`
- website: `www.bjcs.gov.cn`
- SMS: `1069031596156`
- email: `bjcs@bjcs.gov.cn`

并说明老人可查养老院、居家养老及社区生活服务信息。[S3]

这是一个很重要的 historical locator，但必须最小化解释：

> 它证明 2009 年报道把 `www.bjcs.gov.cn` 作为 96156 四种服务入口之一。

它**不自动证明**：

- Web 上所有电话服务都可直接下单；
- 老人本人是主要 Web 用户；
- Web 与热线共用同一数据库；
- 查询结果实时；
- service-provider availability 实时；
- Web 上提交的事务能直达线下服务人员。

### 2.3 2010–2011: 96156 becomes a domain/service family

2010 年同期报道记录“96156首都殡葬公益服务网站”，使用 `binzang.96156.org.cn`，并继续与电话、短信、邮件并列。[S4]

2011 年北京开通“首都社区志愿服务网” `zyz.96156.org.cn`，用户可查询项目、在线报名、请求志愿援助，也可拨 96156 咨询。[S5]

同年“北京家政服务网”给出 `www.bj5800.com` / `www.96156.net.cn`，仍采用统一的 96156 热线。[S6]

这说明：

### `service brand ≠ one host`

“96156”不能被考古者当成一个固定网站。

至少在 2009–2011 证据中，它更像：

```text
telephone service number
+ bjcs.gov.cn information portal
+ 96156.org.cn sub-services
+ 96156.net.cn / bj5800.com service portal
+ SMS
+ email
+ offline community/service-provider network
```

后续应按 host + date + function 单独建证据对象。

---

## 3. 2009 Hangzhou: `remote visibility` and `emergency summon` are different state machines

2009 年中国新闻网/CCTV 对杭州拱墅区的同期报道记录：[S7]

- 2007 起为部分老人安装“电子保姆”呼叫器；
- 2009 安装“全球眼”摄像头；
- 配发有 GPS 和“一键通”功能的 CDMA 手机；
- 与社区居家养老中心和 96345 便民平台相连；
- 摄像头安装强调征得老人本人同意。

至少有两条事务链。

### 3.1 Active emergency / service request

```text
terminal/device assigned
→ device powered
→ elder has device nearby
→ elder presses button
→ wireless/telephone network accepts signal
→ service platform receives
→ resident identity/address resolved
→ operator interprets request
→ emergency/community/service resource chosen
→ local responder dispatched
→ responder arrives
→ issue resolved / escalated
```

### 3.2 Remote camera monitoring

```text
camera installed
→ consent obtained
→ camera powered/networked
→ stream reaches platform
→ authorized staff can view
→ staff actually observes relevant period
→ anomaly recognized
→ response initiated
→ local responder arrives
```

二者不能合并成“平台实时监护”。

尤其：

`camera stream exists ≠ someone is watching exactly when an accident happens`。

---

## 4. 2010–2011: the “virtual nursing home” was a dispatch system, not a virtual building

### 4.1 Lanzhou: phone request → service order → embodied worker

2010 年《光明日报》报道兰州城关区虚拟养老院：老人仍在自己家，通过服务网络获得社区医疗、送餐、上门服务等。[S8]

同期报道强调老人“拨通服务电话”即可提出需求。

从 old-Web 角度，不能因为名称里有“虚拟”就假定核心前端是浏览器。

更谨慎的模型是：

```text
service catalog
+ customer/resident registry
+ phone intake
+ staff dispatch
+ provider network
+ order/subsidy logic
+ offline service completion
```

后台是否为 Web application，需要独立证据。

### 4.2 Hangzhou 2011: one box, multiple semantic buttons

2011 年《钱江晚报》记录杭州上城区“一键通”终端：红、黄、绿按钮分别对应紧急救助、社区服务和生活服务。[S9]

这说明 terminal input 本身已经有 route semantics：

```text
button colour/type
→ request class
→ routing logic
```

但同期新闻不能告诉我们：

- request code 编码；
- terminal ID 格式；
- PSTN/GSM/CDMA/专网实际 transport；
- call center software；
- 地址/老人档案如何查出；
- 多次误按如何处理；
- 没有接通时是否自动重拨；
- 服务商拒单如何重派。

这些继续标 unknown。

---

## 5. Reconstructed state model

以下为 **D 级研究者状态模型**，不是任何一个历史平台的原始 schema。

```text
Eligibility / enrollment
│
├─ elder objectively eligible?
├─ application made?
├─ reviewed?
├─ resident/contact record created?
├─ address recorded?
└─ device/service entitlement activated?

Endpoint
│
├─ landline / mobile / terminal / web / SMS / email
├─ device physically installed?
├─ powered?
├─ network reachable?
├─ elder knows operation?
└─ elder can physically reach it?

Trigger
│
├─ call dialed
├─ button pressed
├─ SMS/email sent
├─ web request submitted
├─ camera observed
└─ sensor/absence event generated

Intake
│
├─ platform receives event?
├─ resident identity matched?
├─ address/contact data current?
├─ operator answers?
├─ request intelligible?
└─ urgency classified?

Routing
│
├─ family contact
├─ community worker / grid worker
├─ volunteer
├─ home-service provider
├─ medical / emergency
└─ multiple fallbacks

Offline execution
│
├─ responder accepts?
├─ can travel?
├─ can enter dwelling?
├─ arrives in time?
├─ service delivered?
└─ escalation needed?

Closure
│
├─ completed
├─ false alarm
├─ no-contact
├─ refused/cancelled
├─ provider unavailable
├─ duplicate request
└─ unresolved
```

Archive 最容易保存的是 public portal 和 service description；最不容易保存的是后半条状态机。

---

## 6. Hard state boundaries

### 6.1 `service advertised ≠ elder eligible`

很多政府购买服务针对特定年龄、低保、独居、失能或困难人群。

### 6.2 `elder eligible ≠ enrolled`

未申请、未建档或资格未审核都可能让“政策可用”停在纸面。

### 6.3 `enrolled ≠ terminal installed`

设备采购、安装批次和家庭条件都可能造成延迟。

### 6.4 `terminal installed ≠ terminal usable`

需要供电、通信、充值/卡、维护、老人理解操作。

### 6.5 `terminal usable ≠ terminal reachable during emergency`

2018 济南对 2012/2014 使用经历的报道是关键反例：固定设备在客厅，而老人倒在厨房，无法触及。[S10]

### 6.6 `button pressed ≠ platform connected`

中间仍有线路、网络、设备和呼叫中心状态。

### 6.7 `platform connected ≠ responder assigned`

需要理解需求、匹配服务类型和资源。

### 6.8 `responder assigned ≠ responder arrived`

交通、距离、门禁、钥匙和人手都可能造成失败。

### 6.9 `child notified ≠ child can provide immediate care`

子女可能在外地或工作中；通知本身不产生身体在场。

### 6.10 `camera online ≠ emergency observed`

“可以远程看”与“有人持续看、正好看见、正确理解”必须分开。

### 6.11 `activity data ≠ wellbeing`

红外/摄像头/电话活动只能证明某类 proxy event，不能自动等同医学健康状态。

### 6.12 `web information ≠ service-order authority`

2009 `www.bjcs.gov.cn` 被明确描述为“网站查询”；没有 transaction capture 时，不能把它写成完整在线下单系统。

### 6.13 `service completed ≠ care need solved long-term`

一次送药、陪聊、修理或送医不能证明长期照护已经稳定。

---

## 7. A crucial afterlife counterexample: 2018 Jinan audits the old promise of 2008–2015 devices

虽然 2018 超出本仓主研究时段，但它对 2008–2015 设备的 afterlife 极有价值。[S10]

报道给出：

- 济南 2008 年试运行“一键通”、2009 年正式运行；
- 到 2015 年 8 月，在网用户与活跃用户之间有明显差距；
- 一些老人多年几乎不用设备；
- 固定设备可能在事故发生位置不可触及；
- 腕表式设备也可能因字小、按键小、充电/手机卡等操作成本被闲置。

这提供一个 old-Web/transaction archaeology 常见但容易丢失的状态：

### `installed-but-dormant`

静态政府报告可能留下：

`已发放 X 台 / 已安装 X 户`

但普通生活真正需要的是：

`老人是否持续会用 + 关键时刻是否记得 + 设备是否在手边 + 后台是否仍有人值守`。

因此安装量不能当使用量。

---

## 8. The public Web is not necessarily the elder-facing interface

这一专题特别容易犯一个“旧网中心主义”错误：

> 找到养老服务网站以后，把 Web 当成老人日常操作的主要入口。

2007–2011 证据反而显示：

- 老人可主要拨 96156；
- Web 可供家属、志愿者、工作人员查项目/报名；
- CDMA/一键通终端可以绕过通用浏览器；
- service operator 可能在后台使用 Web/数据库，但老人本人只按一个按钮。

因此至少有三种 actor：

```text
elder / service recipient
family member
operator / community worker
```

不能因为后台是 Internet-connected，就把事务写成“老人上网办理”。

新增：

### `backend-digitized / user-interface-digital-skill gap`

一个事务可以高度数字化，却让老人只需使用最简单的电话或单键终端。

---

## 9. Archive visibility bias

### 容易留下

- 新闻报道；
- 政府政策页；
- service catalog；
- hotline number；
- public website locator；
- 宣传截图；
- terminal product photo；
- “安装多少台”的统计。

### 容易消失

- private elder records；
- family contact list；
- call audio；
- operator queue；
- dispatch status；
- provider availability；
- no-answer / busy / timeout；
- false alarm；
- abandoned device；
- incident response time；
- door-entry failure；
- elder refusing monitoring；
- family disagreement about cameras；
- service cancelled after pilot funding ends。

因此 surviving Web 会系统性偏向“服务存在”和“成功上线”，低估 ordinary failure states。

---

## 10. Browser / protocol questions for a future real capture

如果以后取得 `www.bjcs.gov.cn`、`96156.org.cn` 或相关 2007–2015 capture，应记录：

### HTTP / encoding

- Content-Type；
- charset：GB2312 / GBK / UTF-8？
- redirects；
- cookies；
- cache behavior。

### Page architecture

- frameset / table / DIV；
- IE-specific JS；
- Flash / ActiveX；
- form action；
- GET vs POST；
- hidden fields；
- CAPTCHA；
- login requirement。

### Service transaction

- query only vs request submission；
- category code；
- address/community lookup；
- service-provider ID；
- request ID；
- state labels；
- cancellation；
- callback / completion confirmation。

### Device integration

Public Web archive 大概率不能回答：

- one-button terminal signalling protocol；
- call-center CTI integration；
- CDMA/GPS device provisioning；
- camera auth/stream；
- automatic retry；
- emergency priority；
- offline cache；
- power/network failure behavior。

这些需要厂商手册、采购文件、专利、招标参数或真实设备资料。

---

## 11. Privacy boundary

本专题涉及高龄、独居、疾病、家庭联系人、家庭内部视频与精确住址，隐私风险高。

未来即使 archive 或泄漏材料能看到真实后台，也不应为了“考古完整”重新公开：

- 普通老人姓名 + 精确地址；
- 身份证/医保信息；
- 病史；
- 子女手机号；
- 家庭摄像头画面；
- call recording；
- 紧急事件详细日志。

优先保存：

- schema / field names；
- anonymized state transition；
- public help pages；
- endpoint pattern；
- aggregate counts；
- hardware/protocol evidence。

研究“平台怎样工作”不需要重新暴露某个普通人的晚年生活。

---

## 12. Established / probable / unknown

### 已证实

- 2007–2008 北京 96156 已作为社区/老人服务电话入口运行；
- 2009 同期报道明确给出 `www.bjcs.gov.cn` 与电话/SMS/email 四渠道；
- 2009 杭州同时使用呼叫器、摄像头、CDMA/GPS 手机和社区服务平台；
- 2010 兰州“虚拟养老院”把电话请求连接到上门服务；
- 2011 杭州“一键通”用不同按钮区分紧急/社区/生活服务；
- 2011 北京存在 `zyz.96156.org.cn` 志愿服务 Web 供需入口；
- 2018 afterlife 证据证明部分 2008–2015 一键设备存在“安装但不用/够不到/不会用”的真实失败状态。

### 高概率但需进一步验证

- 这些系统普遍依赖 resident/contact/address registry；
- call center 需要内部 dispatch/order states；
- 多服务商场景需要某种 provider availability / assignment 机制；
- public Web 和电话后台至少共享部分服务目录数据。

### 不知道

- 2009 `www.bjcs.gov.cn` 精确页面结构；
- Web 端是否能直接提交养老服务订单；
- 历史 charset / browser requirements；
- 一键通/电子保姆设备协议；
- 呼叫中心具体软件；
- GPS、视频和老人档案怎样绑定；
- pilot termination / platform migration 的具体数据迁移；
- failed call / timeout / no responder 的真实比例。

---

## 13. What this changes about old-Web interpretation

这一专题说明中文旧网不能只研究“用户面对浏览器时做了什么”。

2000s 的一个重要数字生活形态是：

```text
老人只拨电话或按按钮
→ Internet / database / CTI 在后台运作
→ operator 使用数字系统
→ 社区或服务商接单
→ 一个真人上门
```

如果只保存网页，就会错过真正决定生活结果的后半段；如果只看设备宣传，又会错过“装了六年没用过”的普通状态。

因此这条线给仓库增加一个长期需要复用的判断：

> **界面越简单，不代表系统越不数字化；系统越数字化，也不代表最终结果越能在线完成。**

在养老服务里，真正有意义的 transaction 终点通常不是 `HTTP 200`，而是**某个本地的人真的到达了老人身边。**

---

## Sources

- **[S1] B — 《京华时报》, 2007-01-09, “政府为孤寡老人买服务”**. https://news.sohu.com/20070109/n247498682.shtml
- **[S2] B — 《新京报》, 2008-05-08, “96156热线征集陪聊志愿者”**. https://news.sina.com.cn/c/2008-05-08/034513845359s.shtml
- **[S3] B/A-locator — 《新京报》, 2009-09-01, “96156可查养老院信息”**, 给出 `www.bjcs.gov.cn`、96156、SMS、email。https://news.sina.com.cn/c/2009-09-01/051016217455s.shtml
- **[S4] B/A-locator — 新京报/搜狐, 2010-03-28**, 给出 `binzang.96156.org.cn` 及多渠道体系。https://news.sohu.com/20100328/n271147769.shtml
- **[S5] B/A-locator — 《新京报》, 2011-08-12**, `zyz.96156.org.cn` 首都社区志愿服务网。https://news.sina.com.cn/o/2011-08-12/040022977046.shtml
- **[S6] B/A-locator — 《京华时报》, 2011-01-01**, 北京家政服务网 `www.bj5800.com` / `www.96156.net.cn`。https://news.sina.com.cn/c/2011-01-01/021521743528.shtml
- **[S7] B — 中国新闻网/CCTV, 2009-04-28, 杭州“全球眼”看护空巢老人**, 电子保姆、CDMA/GPS、一键通、96345。https://news.cctv.com/society/20090428/111150.shtml
- **[S8] B — 《光明日报》, 2010-12-20, “四万老人入住虚拟养老院”**. https://epaper.gmw.cn/gmrb/html/2010-12/20/nw.D110000gmrb_20101220_6-07.htm
- **[S9] B — 《钱江晚报》, 2011-11-25, “一个按键，连起没有围墙的养老院”**. https://news.sina.com.cn/c/2011-11-25/063023522522.shtml
- **[S10] B/C-afterlife — 《齐鲁晚报·齐鲁壹点》, 2018-09-10**, 对济南 2008–2015 一键通覆盖、活跃度和老人实际操作失败的回访。https://isd.ifeng.com/6869347/news.shtml

## M1 status

**NOT ACHIEVED IN THIS SLICE.**

本轮实际尝试了 `www.bjcs.gov.cn` 的 Wayback/CDX 路径，但当前 Web 访问环境不允许直接打开该查询 URL；这只说明**本轮无法验证 capture**，不构成档案缺失证据。
