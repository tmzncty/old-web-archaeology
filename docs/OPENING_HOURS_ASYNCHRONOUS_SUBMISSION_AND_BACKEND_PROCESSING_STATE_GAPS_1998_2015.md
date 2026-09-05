# OPENING_HOURS_ASYNCHRONOUS_SUBMISSION_AND_BACKEND_PROCESSING_STATE_GAPS_1998_2015

## Scope

本说明研究约 1998–2015 中文互联网里一个很容易被“网上办理”“24 小时”“不打烊”这些词抹平的技术—制度问题：

> **一个 Web 入口什么时候真的开放？用户什么时候能提交？服务器什么时候确认收件？后台什么时候处理？现实状态什么时候改变？**

它不是一般的在线报名史，也不是政务服务史。

已有 companion notes 已经分别研究：

- application / eligibility state；
- online banking transaction state；
- rail-ticket queue and payment；
- recruitment / résumé / career state；
- public-library remote-resource state；
- remote-work state。

本说明横向抽取它们共有的 **temporal state（时间状态）**，专门防止把一个历史网页上的“网上”“全天候”“24 小时”直接解释成完整事务在任意时刻都可完成。

生活史 companion：

- <https://github.com/tmzncty/how-people-lived/blob/main/topics/opening-hours-temporal-executability-and-asynchronous-life-administration-china-1987-2026.zh-CN.md>

仓库 scope 仍保持约 1995–2015 中文旧网。ATM、ARPANET email、Minitel 等前史只在生活史 companion 中作为机制比较，不把本仓扩成全球网络史。

---

## 1. 研究单位：历史站点不只有 page state，还有 clock state

一个交易/申请系统至少同时存在：

```text
public notice
→ advertised availability window
→ DNS/network/host reachable
→ application route reachable
→ authentication/session ready
→ client form usable
→ submit attempt
→ server receives bytes
→ durable application record
→ acknowledgement / registration number
→ queue
→ automated or human review
→ status publication
→ payment / confirmation / physical follow-up
→ real-world effect
```

每一层都有自己的时钟。

### 必须固定的硬规则

> **online ≠ 24-hour**

> **24-hour front-end ≠ 24-hour backend**

> **submit click ≠ durable record**

> **durable record ≠ accepted application**

> **reservation available anytime ≠ service performed anytime**

> **page reachable in archive ≠ historical transaction endpoint was open at that capture time**

> **24-hour in a notice ≠ every function was continuously available**

---

## 2. 四种容易混淆的“开放”

### 2.1 Information availability

公告、帮助页、职位表、材料清单可以随时读取。

这只证明：

```text
information page reachable
```

不能证明：

```text
transaction route reachable
```

### 2.2 Submission availability

表单允许提交。

但提交可能只是：

```text
front-end accepted input
```

还不能证明服务端已生成 durable application ID。

### 2.3 Processing availability

后台自动程序或工作人员实际开始审核、核验、结算。

这可能只发生于工作时间或批处理窗口。

### 2.4 Completion availability

最终结果已经产生，而且用户可以取得、下载、领取或使现实登记生效。

因此“24 小时网上受理”最常见的精确解释可能只是：

```text
24h submission
→ business-hours processing
→ later result
```

而不是：

```text
24h instant completion
```

---

## 3. 1998–2003：自助银行提供一个 Web 以前已经成熟的模板

本仓不研究 ATM 前史本身，但 1990s 后期中文 Web 的“24 小时服务”语义需要一个边界说明。

1999 年同期媒体已经报道招商银行北京独立式自助银行，以 ATM、存款机和查询终端提供全天候存取、查询、转账。

对旧网考古的意义不是“证明 Web 已经 24 小时”，而是说明当时用户对“全天候”的理解已经可以来自：

```text
branch counter closed
+ machine still performs selected states
```

早期网上银行继承的正是这种 **selected-state continuity**，而不是整个银行后台全部实时运行。

### Evidence

- **B（同期媒体）**：1999 年招商银行独立式自助银行报道。历史页面 locator 应进一步做 archive 验证；当前研究只用其同期文本证明“24h self-service”作为当时公开概念存在。

### Archaeology rule

如果历史网银产品页写“24 小时”，必须继续寻找：

- 哪些功能是余额查询；
- 哪些是行内转账；
- 哪些涉及跨行清算；
- 哪些只是提交指令，次工作日才处理；
- 系统维护窗口；
- 证书/ActiveX/浏览器要求。

不能把一个 slogan 直接映射到所有 transaction states。

---

## 4. 2007–2009：同一时代的“网上报名”具有不同 daily window

这是本轮最重要的 old-Web 反例。

### 4.1 2008 广州经济资格考试：明确写 24 小时不间断接收

2008 年广州市经济专业技术资格考试通知的同期转载写明：报名期间，网上报名系统“24小时不间断接收”报名。

但同一流程继续要求：

```text
online profile
→ print photo slip
→ designated photo studio
→ wait for photo upload (up to about 24h)
→ online confirmation by registration point
→ payment
→ print registration form
→ employer review/stamp
→ keep document for later certificate handling
```

这说明一个“24h”网页入口可以嵌在高度非 24h 的完整事务链中。

### Evidence

- **B/A-near-primary（同期转载官方通知）**：广州市人事考试中心，穗人考中心函〔2008〕52号，2008-03-28 / 2008-04-03 转载。  
  <https://www.chinaacc.com/new/15/22/48/2008/4/lu113513204413480024876-0.htm>

### New gap

**submission-window / completion-window gap**

```text
24h input window
≠
24h complete registration
```

### 4.2 2008/2009 研究生网报：官方 Web 系统每天只开 9:00–22:00

教育部同期公告明确：

- 2008 年硕士网上报名每天 9:00–22:00；
- 2009 年仍是每天 9:00–22:00；
- 网上报名之后必须在固定日期现场确认、缴费、照相，否则报名无效。

因此必须禁止：

> “Web form existed, therefore users could submit at any hour.”

### Evidence

- **A（官方同期）**：教育部，2007-09-10。  
  <https://www.moe.gov.cn/jyb_xwfb/gzdt_gzdt/moe_1485/tnull_26364.html>
- **A（官方同期）**：教育部，2008-09-17。  
  <https://www.moe.gov.cn/moe_879/moe_329/moe_1798/tnull_39054.html>

### New gap

**Web-presence / daily-opening-window gap**

一个历史报名主页 capture 即使凌晨仍能回放，也不能证明 2008 年凌晨真实报名 endpoint 接受 POST。

---

## 5. 2008 公务员报名：系统负载本身会重新分配用户时间

2008 年国考网报首日，同期记者在 8:00 后实际遇到：

- 保存注册信息缓慢；
- “系统忙，请重新登录”；
- 页面十分钟无响应；
- 网站一度难以登录。

技术人员建议报考者在晚上、清晨错峰。

这使“网上报名”出现一个非常重要的 **capacity-time coupling（容量—时间耦合）**：

```text
nominal opening window is wide
but
successful submission probability varies by hour
```

因此用户可能主动把报名劳动移到凌晨。

### Evidence

- **B（同期媒体，现场操作）**：沈阳今报 / 新浪，2008-10-16，《公务员报名系统拥堵建议报考者错峰上网》。  
  <https://news.sina.com.cn/o/2008-10-16/032914580484s.shtml>

### New gaps

**advertised-open / practically-usable gap**

**submit-click / server-acceptance gap**

**nominal-deadline / effective-safe-deadline gap**

如果最后一天 24:00 截止，而高峰时持续超时，那么“截止到 24:00”并不意味着 23:59 才开始填写仍具有同等可执行性。

---

## 6. 2008 网申：异步并不等于低成本

同期校园招聘材料记录：

- 有毕业生从 9 月开始投几十份网络申请却没有反馈；
- 一些网申有 4–5 页甚至十多页；
- 一份网申可能耗时 3–4 小时。

从 old-Web 考古角度，这增加了两个必须分开的状态：

```text
application form reachable
→ user completes client-side labor
→ submit
→ company system durably receives
→ screening
→ human/recruiter encounter
→ response / silence
```

因此：

> **submitted ≠ encountered by recruiter**

> **no response ≠ no durable submission**

> **form accessible after hours ≠ application is cheap to maintain**

### Evidence

- **B（同期媒体，第一人称）**：信息时报 / 新浪，2008-10-30。  
  <https://edu.sina.com.cn/l/2008-10-30/1406154992.shtml>
- **B（同期媒体）**：长沙晚报 / 新浪，2008-11-06。  
  <https://edu.sina.com.cn/l/2008-11-06/1057155891.shtml>

### Archive implication

Archive 很容易保存招聘主页和表单字段，却几乎不会保存：

- 普通申请者的草稿；
- timeout；
- recruiter queue；
- 是否打开过某份申请；
- 何时被筛掉；
- 沉默究竟发生在哪一层。

这产生 **public-form / private-review-state asymmetry**。

---

## 7. 预约系统：anytime reservation ≠ anytime real-world act

婚姻登记、医院挂号、政务预约、办证预约都具有类似结构：

```text
calendar visible
→ slot visible
→ slot selected
→ reservation durable
→ confirmation generated
→ person arrives during assigned office time
→ identity/material verification
→ real-world act
```

因此一个 24h 预约系统最重要的考古边界是：

> **reservation-time decoupling ≠ service-time decoupling**

用户可以凌晨预约，但婚姻登记、面签、拍照或人工核验仍然发生在另一个制度时间窗口。

2009 年“9月9日”婚登高峰材料显示，北京已经使用提前预约，把当天的材料预审/办理节奏压缩；这类材料证明预约改变队列组织，但不能证明登记机关 24h 办公。

### Evidence

- **B（同期媒体）**：经济观察网，2009-09-10，关于 9 月 9 日婚姻登记预约与高峰。  
  <https://www.eeo.com.cn/tppd/jrtt/2009/09/10/150757.shtml>

---

## 8. 2011–2015：从单一网页时间转向多层 time state

到 2010s 前半期，一个中文互联网事务可能同时拥有：

```text
public website hours
authenticated portal hours
payment gateway hours
bank settlement hours
human review hours
SMS/email notification delay
physical pickup hours
```

旧网研究不能把这些压成一个 `available=true/false`。

建议未来 evidence schema 增加：

```yaml
temporal_state:
  advertised_window: unknown
  observed_frontend_window: unknown
  transaction_window: unknown
  payment_window: unknown
  backend_processing_window: unknown
  physical_followup_window: unknown
  cutoff_timezone: unknown
  maintenance_window: unknown
```

如果只有公告，不要把 `advertised_window` 自动复制到其他字段。

---

## 9. Historical capture 的特殊陷阱：页面的“现在”不是历史系统的“现在”

### 9.1 Wayback 在凌晨回放成功，不证明原站凌晨可交易

Archive replay 发生在今天。

它可能只回放：

- 静态 HTML；
- 说明页；
- 已缓存 JS；
- 被 rewrite 的 form action。

真实 POST endpoint、数据库、认证和时间门控早已不存在。

因此：

```text
Memento rendered at 03:00 today
≠
original transaction accepted at 03:00 historically
```

### 9.2 历史页面上的倒计时可能已经失真

可能依赖：

- client clock；
- server clock；
- JavaScript `Date()`；
- dynamic response；
- cookie/session age；
- timezone；
- archive rewrite。

现代回放中的“还有 2 天”不能直接当历史倒计时证据。

### 9.3 404 / system closed 页面反而可能比正常 transaction 更有价值

如果能取得同时代：

- “系统维护”；
- “非报名时间”；
- “报名已结束”；
- “系统忙”；
- “请稍后重试”；
- “每日 22:00 关闭”；

这些页面能够直接证明负状态。

本仓应主动保存 **negative temporal states**，而不是只保存成功首页。

---

## 10. New archive bias: announcement survival / transaction-time darkness

本题存在很强的保存偏差：

### 容易保存

- 报名通知；
- “24 小时服务”宣传；
- 首页；
- 操作指南；
- 截止日期；
- 静态材料清单。

### 难保存

- 23:57 的提交是否成功；
- 03:00 endpoint 是否真的开放；
- timeout / overloaded response；
- 用户完成到哪一步；
- 后台何时开始审查；
- 一个排队请求是否跨夜存活；
- 次日工作人员看到的 queue；
- 私人短信 / email 状态通知。

因此后世 archive 特别容易形成：

> **“页面说 24 小时，所以整个服务应该一直能办”的完整性幻觉。**

本说明把它称为 **transaction-time darkness（交易时间黑区）**。

---

## 11. 三条标准状态机

### 11.1 Online application

```text
notice
→ window begins
→ portal reachable
→ account/session
→ form
→ client validation
→ submit attempt
→ HTTP/application acceptance
→ durable application ID
→ review queue
→ eligibility decision
→ confirmation/payment
→ physical or online verification
→ effective registration
```

### 11.2 Reservation

```text
service directory
→ calendar
→ slot inventory
→ reservation request
→ durable reservation
→ confirmation
→ appointed time
→ physical/remote attendance
→ identity/material check
→ service completed
```

### 11.3 24h self-service / online government service

```text
public promise
→ machine/portal reachable after hours
→ identity authentication
→ requested function supported
→ materials digitizable
→ submission
→ receipt
→ queue
→ overnight storage
→ business-hours review or automated execution
→ result
→ pickup/download/real-world effect
```

这些 state machine 允许以后把“24 小时”精确标在某个箭头，而不是整张图染成绿色。

---

## 12. Evidence grading for this note

### A — strong contemporaneous primary / official

- 教育部 2007、2008 年研究生网报公告：明确每日 9:00–22:00 + 现场确认。
- 若未来取得原报名系统帮助页/capture，可进一步确定前端字段和时间门控。

### B — contemporaneous secondary / reproduced notice

- 2008 广州经济资格考试官方通知的同期转载：24h submission + 照相/审核/缴费/单位盖章链。
- 2008 国考首日媒体实际操作：系统忙、超时、建议夜间/清晨错峰。
- 2008 校招网申体验：无反馈、3–4 小时表单。
- 2009 婚登高峰预约报道。

### C — retrospective

本轮没有用后来的“当年网申多方便/多痛苦”回忆去确定技术字段。若以后使用，仅能补主观经验。

### D — reconstruction / inference

本说明中的 state machine、gap names 和 archive-bias 模型均为研究者抽象，不是历史平台自己的术语。

---

## 13. 已证实 / 高概率 / 不知道

### 已证实

- 2008 前后不同中国网上报名系统存在不同 daily opening window；“在线”不能直接推出“全天”。
- 24h 网上提交可以与线下照相、单位盖章、人工确认同时存在。
- 高峰拥堵可以迫使申请者选择夜间/清晨错峰。
- 同期求职网申可能耗费数小时，且提交后无反馈并不少见于报道样本。
- 网上预约可以改变排队/预审，但最终现场制度动作仍有自己的时间窗口。

### 高概率但仍需 capture 验证

- 2008 广州报名入口在宣传所述报名期内确有夜间 POST 接受能力。
- 当年部分系统在截止后/每日关闭后会返回专门的 closed-state 页面或屏蔽 transaction route。
- 招聘表单的 session timeout / popup / JS 行为会显著影响长表单的夜间完成率。

### 不知道

- 2008 广州原 `gzexam` 页面具体 URL、DOM、HTTP charset、form action、cookie/session、服务器时区和维护窗口。
- 2008 国考真实 transaction endpoint 的原始错误页、HTTP status、session expiration 和 queue implementation。
- 研究生网报每日 22:00 后是关闭 form、拒绝 POST、登出 session，还是由后端时间检查拒绝；目前官方文本只证明 policy window。
- 历史第三方支付/网银在这些报名链中何时 settlement，以及跨午夜的 transaction 语义。
- 2009 婚登预约系统原页面和预约状态是否有 timeout / slot locking。

---

## 14. M1 status：本轮仍未越过 capture 门槛

本轮获得了具体 historical locators / candidate targets，包括：

- `yz.chsi.com.cn` / `yz.chsi.cn` — 2007–2009 研究生报名；
- 广州考试信息网 / 中国广州人事网 — 2008 经济资格考试；
- 2008 国考人力资源和社会保障部报名系统；
- 2009 婚姻登记预约相关入口。

但本轮**没有实际取得并检查一份满足本仓 M1 门槛的完整历史 transaction capture**，尤其没有验证：

- original URL + capture datetime；
- original HTML/charset；
- POST endpoint；
- closed-hours response；
- session/cookie；
- durable application response；
- backend review state。

因此这些只作为 candidate locator / contemporaneous documentation，不宣称已经完成页面复原。

这符合 `docs/METHOD.md`：

> 搜索结果或历史 URL 的存在，不等于已经验证 capture。

---

## 15. Privacy / stop conditions

研究“夜间提交是否成功”很容易诱导研究者去寻找真实申请者账户、报名号、身份证、求职后台或泄露数据库。

本仓明确禁止：

- 用泄露的普通人账户验证旧系统；
- 拼接身份证、手机号、报名号去重建私人申请；
- 公开普通求职者的历史私密申请；
- 为了证明后台状态而重新识别个人。

研究目标是平台结构和时间状态，不是追踪某个普通人究竟在凌晨几点提交了哪份私人申请。

---

## 16. 对旧网解释规则的新增

以后遇到任何历史页面包含：

- `24小时`；
- `全天候`；
- `随时`；
- `网上办理`；
- `不打烊`；
- `截止24时`；

至少追加六个问题：

1. 这句话修饰的是 information、submission、processing 还是 completion？
2. daily window 是多少？
3. deadline 使用哪一时区/服务器时钟？
4. submit 后是否有 durable receipt / number？
5. 后台是否要等工作时间？
6. 是否仍有必须在固定时段完成的 physical handoff？

如果这六项没有证据，就不要把“网上”画成一个瞬时、无时钟的按钮。

---

## 17. Core insight

旧网把很多事务从“必须在窗口打开时本人到场”改变成“可以先把请求交给机器”。

但历史真实状态更接近：

```text
synchronous office encounter
→ longer digital submission window
→ asynchronous queue
→ mixed automated/human backend
→ later status/result
```

而不是：

```text
paper → Web → instant 24/7 completion
```

因此在中文旧网考古中，**时间本身必须成为 transaction state 的一部分**。

一个网页入口存在，只说明门牌还在；要知道普通人当年能不能在下班后真正把事情办进去，还必须追到那扇门背后的时钟。
