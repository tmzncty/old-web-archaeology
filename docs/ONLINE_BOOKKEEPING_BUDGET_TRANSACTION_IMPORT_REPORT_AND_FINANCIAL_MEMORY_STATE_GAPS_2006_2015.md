# ONLINE_BOOKKEEPING_BUDGET_TRANSACTION_IMPORT_REPORT_AND_FINANCIAL_MEMORY_STATE_GAPS_2006_2015

> Status: research note / cross-repo companion
>
> Scope: 中文 Web / Web-adjacent 个人记账、预算、账单同步与财务报表，约 2006—2015
>
> Date: 2026-09-09
>
> Cross-repo life-history note: `tmzncty/how-people-lived/topics/from-paper-ledgers-to-budget-apps-cash-flow-legibility-and-financial-buffer-china-preweb-2026.zh-CN.md`

## 0. 研究问题

本稿不讨论“哪款记账软件最好”，也不把网银、支付宝、信用卡管家重新写一遍。它只研究一个 old-Web state gap：

> **历史网页证明“网上有一个账本”以后，我们究竟还需要哪些证据，才能证明一个普通人的某笔支出真的被提交、保存、分类、汇总进报表、参与预算，并在另一台设备上仍然一致？**

中文旧网已经保存了大量关于“网络记账”“账客”“网上账本”的同期报道与教程；但真正的私人账本通常在登录之后，动态地存在数据库中，既难被 archive 捕获，也不应为了考古完整而重新公开。

因此本对象天然适合仓库现行方法：

```text
platform != host != account != ledger != transaction != report != capture != claim
```

并且必须坚持：

```text
记账页存在
!= 用户创建了账本
!= 某笔流水提交成功
!= 后端持久化
!= 分类正确
!= 报表已重算
!= 预算提醒已触发
!= 用户看到并因此改变行为
```

---

## 1. 为什么这是一个独立的旧网对象

`old-web-archaeology` 已经研究过：

- 个人网银、汇款与资金可用状态；
- 信用申请与信用报告；
- 密码、手机号、账号恢复；
- 网络硬盘与个人数据保管；
- Web 日历与未来事件；
- 浏览器收藏与个人检索记忆。

个人记账却处在这些系统之间：

- 它可以手工记录现金，根本不接银行；
- 也可以维护“现金 / 储蓄卡 / 信用卡”等用户定义账户；
- 后期可以导入支付账单或同步多端；
- 报表是由原始流水和分类规则派生的二级对象；
- 预算又用过去流水去约束未来。

因此必须单独建模。

---

## 2. 已确认的历史主体与时间边界

### 2.1 2008 年“网络账本”已经是可观察的中文 Web 类型

2008-01-09 新华网/《市场报》经搜狐保存的报道直接观察多家在线记账服务，并描述当时常见功能：

- 任意联网电脑访问；
- 数据保存在服务器；
- 日常收入/支出录入；
- 分类；
- 月度比例与总额曲线；
- 固定支出自动记录；
- Excel 导出；
- 部分平台支持公开“晒账”和评论。

来源：

- https://business.sohu.com/20080109/n254544291.shtml
- grade: B（同期媒体采访 + 页面观察）

这可以支持：

> 2008 年中文 Web 上存在面向普通用户的在线个人记账/账客服务及上述功能类型。

不能支持：

> 这些服务已经成为中国年轻人的普遍日常习惯。

报道中用户数多来自平台负责人陈述，应当单独降级。

### 2.2 2008 深圳材料保存了字段层级

中国互联网协会保存的一篇同期材料描述了登录后的记账页面字段，包括：

- 日期；
- 现金金额；
- 信用卡金额；
- 储蓄卡金额；
- 收入 / 支出；
- 教育、金融、投资等用途分类；
- 自定义用途名称；
- 说明和评论；
- 月末/季末统计报表。

来源：

- https://www.isc.org.cn/article/12708.html
- grade: B（同期转载/媒体材料）

这一证据比“某网站有记账功能”更强，因为它开始支持历史 data model 的一部分字段。

### 2.3 `caakee.com` / 财客在线：candidate host，不等于本轮已取得 memento

2008—2009 同期报道反复提到“财客在线”；融资/项目数据库后来保留 `http://www.caakee.com` 作为项目 URL，并称其 2006 年开始提供在线记账服务。

本轮只把：

`caakee.com → 财客在线 candidate historical host`

登记为可进一步核验的线索。

**没有**把当前搜索结果自动升级为 A 级历史网页 capture。

### 2.4 2010—2011 `feidee.com` / 随手记：Web + mobile 同步成为明确产品结构

2011-04 的同期行业报道明确说：

- 随手记在 2010 年 5 月发布；
- 当时支持 Web、iPhone、Android；
- 网站和手机端之间可同步；
- 不同手机端之间可同步；
- 有预算预警短信；
- 有个人财务报表。

来源：

- https://www.doit.com.cn/p/72965.html
- grade: B（同期行业媒体；规模数字主要来自企业披露）

另有 2011-12 的 Android 社区软件介绍保存 `www.feidee.com`、本地 SD 卡备份、与金蝶理财网双向同步、电脑查看报表等产品描述：

- https://apk.tw/thread-38889-1-1.html
- grade: B（同期软件分享/介绍页；可辅助功能与 hostname，不可单独证明后端事务成功）

因此 2010s 初必须把 Web 账本和 mobile client 视为同一同步系统的不同入口，而不是两个互不相关的产品页面。

---

## 3. 对象模型

一个高质量复原至少要区分以下对象。

### 3.1 Identity / account layer

```text
PERSON
→ PLATFORM ACCOUNT
→ AUTH CREDENTIAL
→ SESSION
```

需要问：

- 登录名是什么？
- 是否绑定邮箱/手机号？
- mobile 与 Web 是否同一账号？
- 是否允许离线、本地未登录账本？
- later account migration 是否改变旧数据归属？

### 3.2 Ledger container

一个账号可能拥有：

- 个人账本；
- 家庭账本；
- 工作报销账本；
- 多个独立账本；
- 示例/demo 账本。

因此：

> **account exists != one canonical ledger exists**

### 3.3 Transaction object

最小流水可能包括：

```text
transaction_id
amount
currency
date/time
direction = income / expense / transfer
account_from / account_to
category
subcategory
merchant/payee
person/project
tags
note
created_at
updated_at
source = manual/import/sync/automation
```

历史版本不一定全部存在这些字段；这里只是调查矩阵，不能倒投到 2008。

### 3.4 Account model

早期在线账本材料已经出现：

- cash；
- credit card；
- savings/debit card。

后续还可能有：

- investment；
- receivable/payable；
- liabilities；
- virtual/payment account。

关键边界：

> **ledger account balance != bank backend balance**

如果金额来自用户手工输入，它只是用户模型中的余额，而不是金融机构的权威余额。

### 3.5 Category taxonomy

类别是报告语义的一部分：

```text
transaction
→ category mapping
→ aggregation
→ chart/report
```

如果分类规则变了，同一批历史流水重新计算出的图表也可能变化。

### 3.6 Budget rule

```text
period
category/account scope
limit/target
spent_so_far
remaining
threshold
notification rule
```

预算属于未来状态，不等于历史流水。

### 3.7 Report / derived aggregate

常见派生对象：

- 月度收支；
- 分类占比；
- 趋势曲线；
- 账户余额；
- 资产/负债；
- 预算完成度。

必须固定：

> **report is a derived view, not the raw ledger.**

### 3.8 Import/export artifact

例如：

- Excel；
- CSV；
- proprietary backup；
- bank/payment bill file；
- app local backup。

导出文件是新的 artifact，有自己的时间和 schema。

### 3.9 Sync client / server state

```text
local transaction
→ local commit
→ sync queue
→ authentication
→ server commit
→ second client fetch
→ conflict / duplicate resolution
→ local materialization
```

“支持同步”不能跳过这整条链。

---

## 4. 状态机 A：手工记一笔

```text
A0 account/session ready
A1 ledger selected
A2 transaction form rendered
A3 amount entered
A4 date/account/category entered
A5 submit action issued
A6 client validation passed
A7 request reached backend
A8 backend accepted transaction
A9 transaction persisted
A10 derived balances/reports recalculated
A11 confirmation rendered
A12 later query returns same transaction
```

必须保留的断点：

```text
form exists != submit happened
submit happened != HTTP request reached backend
HTTP 200 != application commit
success message != durable persistence
transaction appears once != no duplicate exists
```

对历史 archive 来说，A2 很容易保存，A8—A12 通常最难。

---

## 5. 状态机 B：预算与预警

```text
B0 budget feature exists
B1 user creates period/category limit
B2 budget rule persisted
B3 transactions accumulate
B4 aggregation crosses threshold
B5 warning event generated
B6 SMS/push/email queued
B7 carrier/service accepts message
B8 user receives/sees warning
B9 user changes or does not change spending
```

关键边界：

```text
budget UI exists != user configured budget
configured != stored
threshold crossed != warning generated
warning generated != delivered
warning delivered != read
read != behavior changed
```

2011 随手记报道只足以证明预算预警短信被产品提供/宣称，不能证明普通用户实际收到，更不能证明它改善储蓄。

---

## 6. 状态机 C：月报/季报

```text
C0 raw transactions exist
C1 category mappings available
C2 selected time range resolved
C3 aggregation query executes
C4 derived totals generated
C5 chart/table rendered
C6 user views/exports report
```

一个历史截图如果只剩饼图，需要避免两个错误：

1. 从饼图反推出完整原始流水；
2. 默认今天重渲染出的图表就是当年的算法结果。

类别、退款规则、转账是否计入收支、信用卡还款是否重复计入等版本变化，都可能改变报表。

> **same transactions + different accounting rules = different report**

---

## 7. 状态机 D：导入外部账单

2006–2015 的具体 import 能力需要逐平台、逐版本继续核验；但为了以后研究，先固定状态机：

```text
D0 upstream bank/payment system has transactions
D1 user requests statement export
D2 file generated
D3 file downloaded
D4 bookkeeping platform recognizes format/version
D5 parser reads rows
D6 duplicate detection/matching
D7 category mapping
D8 import preview
D9 user confirms
D10 imported transactions persisted
D11 reports recomputed
```

硬边界：

```text
file accepted != every row parsed
row parsed != transaction identity matched
imported != correctly categorized
same bank format name != same schema across years
```

这在 2020s 仍然是活问题：上游微信/支付宝账单导出格式改变后，记账软件会更新 importer。这说明 format version 本身应进入 old-Web/old-app archaeology 的证据模型。

---

## 8. 状态机 E：Web ↔ 手机同步

2011 的同期材料已经足以证明“同步”是核心产品卖点，因此不能只截图一个 Web 页面。

```text
E0 same user/account intended
E1 local ledger exists on device A
E2 local change created
E3 sync initiated/automatic trigger
E4 credentials/session valid
E5 change uploaded
E6 server commit
E7 device B connects
E8 remote change downloaded
E9 conflict/duplicate policy applies
E10 device B renders same logical state
```

关键边界：

```text
sync button exists != sync succeeded
upload succeeded != second device converged
same total balance != same transaction set
same transaction count != same category semantics
```

如果历史资料只说“手机掉了也不怕”，它只能证明产品承诺，不是数据耐久性的实证。

---

## 9. 状态机 F：公开“晒账”

2008 报道里的“账客”存在公开消费、评论和陌生人监督。

可能的事务链：

```text
private transaction/summary
→ visibility policy
→ public representation generated
→ public URL / profile
→ visitor fetch
→ comments/recommendations
```

但必须特别谨慎：

- 不要主动寻找并重新公开真实普通人的完整财务记录；
- 研究平台结构优先使用同期媒体截图、官方 demo、教程、字段说明；
- 若引用公开用户个案，只保留支持 claim 所需的最少金额/字段。

> **archive availability does not cancel financial privacy.**

---

## 10. 旧网页面与真实财务状态之间的典型 gap

### 10.1 login-shell gap

archive 常能保存登录页或产品首页，但私人 ledger 在认证之后。

```text
login page survives
!= historical account can authenticate
!= ledger endpoint survives
!= ledger rows preserved
```

### 10.2 report-without-ledger gap

媒体截图可能留下一个月度饼图，却没有原始流水。

```text
chart visible
!= raw data available
!= category rule known
```

### 10.3 ledger-without-authoritative-money gap

用户手工输入“信用卡 3000 元”并不能证明银行后台余额就是 3000 元。

```text
personal bookkeeping state
!= bank authoritative state
```

### 10.4 public-sample selection gap

愿意“晒账”的人比普通用户更可见。

所以：

```text
public ledger abundance in search engines
!= ordinary users normally publicized finances
```

### 10.5 time-of-render gap

一个今天仍活着的旧 URL 可能由当前后端重新渲染，而不是当年 HTML。

必须区分：

- original historical response；
- archive memento；
- current legacy route；
- current application data。

### 10.6 account-identity gap

手机号、邮箱、第三方登录改变后，旧账本仍可能存在但失去可寻址身份。

```text
backend rows survive
!= present user can prove ownership
```

---

## 11. 浏览器 / 客户端环境问题

2006–2015 研究至少记录：

- IE / Firefox / Chrome 支持；
- charset（GBK / UTF-8）；
- AJAX/XHR；
- Flash chart 是否存在；
- JavaScript 动态表格；
- cookie/session；
- popup；
- Excel/CSV 下载响应；
- mobile browser vs native client；
- local SD-card backup；
- iPhone/Android client version。

如果报表依赖 Flash/JS，现代浏览器看到空白不能直接写成“当年报表坏了”。

---

## 12. Preservation levels

### P0 — textual mention only

只有同期文章/目录说服务存在。

### P1 — product shell

保存产品首页、登录入口、功能宣传。

可以证明产品自述，不能证明用户 ledger state。

### P2 — transaction UI structure

保存“记一笔”表单、字段、类别选择、账户类型。

可以研究 data model 的界面投影。

### P3 — report/budget UI structure

保存图表、预算栏、阈值、报表筛选，但不一定有真实数据。

### P4 — demo/sample transaction semantics

存在官方 demo、教程测试数据或可合法保存的示例账本，可以观察 transaction → report 的映射。

### P5 — import/export format

取得历史导出/导入 schema、示例 CSV/Excel、backup 格式说明。

这是研究 portable semantics 的关键层。

### P6 — sync/client protocol evidence

有客户端包、网络文档、日志或技术说明，可以确认 Web/mobile 同步字段与冲突行为。

### P7 — transaction-state reconstruction without private data

在 demo/test 环境或公开文档基础上，能复原：

```text
create → persist → aggregate → export/sync
```

且明确标 reconstruction。

**P7 不要求，也不鼓励取得真实历史普通用户私人账本。**

---

## 13. Evidence ledger

| Claim | Evidence | Grade | Confidence | What it does not prove |
|---|---|---:|---:|---|
| 2008 中文 Web 已有多家在线记账/账客服务 | 新华网/市场报经搜狐保存 | B | high | 不证明人口普及率 |
| 2008 页面可含现金/信用卡/储蓄卡、收入支出与自定义分类 | 中国互联网协会同期材料 | B | high | 不证明具体某平台所有版本字段一致 |
| 在线账本当时可提供曲线、分类占比、固定支出和 Excel 导出 | 2008 同期媒体页面观察 | B | high | 不证明每个站都有全部功能 |
| 2010/2011 随手记支持 Web/iPhone/Android 与同步、预算提醒 | 2011 DOIT 同期报道 | B | high | 下载/用户规模主要是厂商数字 |
| `www.feidee.com` 用于随手记/金蝶理财网 Web 入口 | 2011 DOIT + 2011 Android 社区介绍 | B+B | medium-high | canonical path、各年月 URL 仍需 capture |
| 财客在线与 `caakee.com` 有历史关联 | 同期媒体品牌 + 后续项目数据库 URL | B/C | medium | 本轮未验证历史 memento |
| Web 账本数据迁移可能形成锁定 | 2018 App Store 用户自述（life-history side） | A/B | medium | 单一用户，超出 old-web 核心期，仅作后果验证 |

---

## 14. 本轮 archive replay 尝试与负结果

### 14.1 `caakee.com`

本轮尝试直接构造约 2009 年 Wayback replay：

`https://web.archive.org/web/20090101000000/http://www.caakee.com/`

当前检索/访问链因 URL safety 限制拒绝直接打开该构造 URL，没有得到可检查的 memento response。

因此只能记录：

> **M1 verified `caakee.com` historical capture: NOT ACHIEVED IN THIS SLICE.**

这不等于：

> Wayback 没有保存 `caakee.com`。

### 14.2 `feidee.com`

本轮同样尝试构造约 2011 年 replay：

`https://web.archive.org/web/20110101000000/http://www.feidee.com/`

访问链同样因安全 URL 限制没有取得可核验回放。

因此：

> **M1 verified `feidee.com` 2010/2011 capture: NOT ACHIEVED IN THIS SLICE.**

同期独立材料足以把 `www.feidee.com` 作为 strong historical host candidate，但还不能填写：

- `capture_datetime`；
- historical HTTP status；
- charset；
- DOM；
- JS bundle；
- login form action；
- report endpoint；
- import/export path。

### 14.3 下一轮 capture 优先级

如果能获得 archive-friendly 路径，优先顺序：

1. `caakee.com` 2007–2009 首页/帮助/注册；
2. `feidee.com` 2010–2012 首页、理财网、帮助页；
3. 同期搜索缓存/软件截图中的 canonical path；
4. 官方 demo/sample ledger；
5. 历史客户端下载包及版本说明；
6. Excel/backup 样例格式。

避免把真实用户私人 ledger 作为目标。

---

## 15. 关键 archive biases

### 15.1 public-finance visibility bias

搜索引擎与 archive 更容易留下“晒账”页面、媒体引用和公开昵称；纯私人账本最不可见。

因此：

> **archive-visible bookkeeping culture != ordinary bookkeeping practice**

### 15.2 successful-render bias

保存下来的漂亮饼图比失败的 AJAX、超时、空 session 更容易被二次传播，可能夸大历史系统的稳定性。

### 15.3 current-product contamination

`feidee.com` 今天仍可能存在并重定向到新产品。当前 SEO metadata、2026 页脚、现代 App 下载入口不能用于填补 2011 页面结构。

### 15.4 schema survival bias

导出的 CSV/Excel 如果幸存，研究者容易把它当完整账本；但预算、账户层级、标签、退款关联、共享权限、操作日志等可能根本没有进入导出文件。

---

## 16. 与平台生命周期的交叉

在线记账把一个非常私密、长期的对象交给 SaaS 后端。

海外 2010 年 Wesabe 停服提供一个早期对照：用户被要求在指定期限前下载账户信息，随后功能下线、数据删除。

来源：

- https://techcrunch.com/2010/06/30/wesabe-shuts-down/
- grade: B（同期媒体记录停服页面）

因此中文旧网调查未来需要特别寻找：

```text
shutdown notice
→ export offered?
→ export schema?
→ deadline?
→ account login still works?
→ data removed?
→ successor/import path?
```

这和网络硬盘的 `archive-exit labor` 类似，但个人财务数据更敏感，而且语义更复杂。

---

## 17. 与 life-history 的交叉结论

旧网侧能可靠支撑的最小生活史结论是：

1. 2008 年中国普通商业 Web 已经可以把个人小额日常消费转成可分类、可统计、可跨电脑访问的数字对象；
2. 2010s 初移动客户端与 Web 同步把记账进一步从“晚上回家补录”推向随身记录；
3. 预算和预警意味着系统不只描述过去，还开始维护 future-facing financial state；
4. 多年记录越完整，平台退出、账号恢复和数据迁移的成本越高；
5. archive 最容易保存的是产品壳、功能描述和愿意公开的“晒账”，最难保存的是普通人的真实私人财务历史。

但 old-web 证据本身不能推出：

- 网络记账提高全国储蓄率；
- 某代年轻人普遍更节俭；
- 使用 App 就能避免债务/失业冲击；
- 某历史平台规模宣传是真实活跃人数。

---

## 18. 下一步最值钱的证据

1. 一份 2006–2009 `caakee.com` verified memento；
2. 一份 2010–2012 `feidee.com` verified memento；
3. 早期“记一笔”真实表单字段与 charset；
4. 官方 demo/sample ledger，不触及个人隐私；
5. 早期 Excel export schema；
6. Web/mobile sync 的技术或帮助文档；
7. 预算短信的实际配置界面；
8. 平台停服/迁移公告；
9. 旧版客户端包与本地 backup 格式；
10. 同一流水在不同版本 report rule 下是否产生不同结果的 reconstruction experiment。

---

## 19. 已证实 / 高概率 / 不知道

### 已证实

- 2008 同期中文 Web 材料明确存在网络记账、分类、报表、导出和“晒账”实践。
- 2008 同期材料明确出现现金、信用卡、储蓄卡等账户/字段层级。
- 2010–2011 随手记同期报道明确支持 Web/iPhone/Android、多端同步、预算预警和报表。
- `www.feidee.com` 被 2011 同期材料作为相关 Web 入口提及。

### 高概率

- 早期 Web 记账的大量核心状态在登录后动态数据库中，因此公共 Web archive 对真实 ledger state 的覆盖远低于产品壳。
- 多端同步存在冲突、重复、延迟和版本差异问题，但具体历史算法仍需证据。
- Excel/CSV 导出通常不足以表达平台全部语义，但需要逐平台 schema 验证。

### 不知道

- 本轮 `caakee.com` 和 `feidee.com` 的具体 verified memento 情况；
- 2008 各平台真实活跃用户与地域分布；
- 具体平台 2006–2015 各版本的 transaction schema；
- 历史退款、转账、信用卡还款是否如何计入报表；
- 早期同步冲突策略；
- 历史 export 是否包含账户层级、分类自定义、预算和备注；
- 平台停服或产品迁移时用户实际带走多少财务语义。

---

## 20. 主要来源

### Chinese contemporary / near-contemporary

- 新华网/《市场报》经搜狐保存，2008-01-09，《“账客”网上晒消费 年轻人重拾记账理财》  
  https://business.sohu.com/20080109/n254544291.shtml
- 中国互联网协会，2008-01-16，《深圳白领流行网络记帐》  
  https://www.isc.org.cn/article/12708.html
- DOIT，2011-04-16，《随手记：金蝶友商网个人理财业务步入快车道》  
  https://www.doit.com.cn/p/72965.html
- Android 台湾中文网，2011-12-19，金蝶随手记 V5.2.0 软件介绍  
  https://apk.tw/thread-38889-1-1.html
- 博客园，2014-11，随手记界面/预算/流水字段用户评测（B，单一用户教程/评测）  
  https://www.cnblogs.com/PhiloSky/p/4114836.html

### Overseas comparison

- TechCrunch, 2010-06-30, Wesabe shutdown / user data download deadline  
  https://techcrunch.com/2010/06/30/wesabe-shuts-down/
- Intuit, Mint background, 2011  
  https://investors.intuit.com/news-events/press-releases/detail/865/financial-fun-mint-com-launches-quest-for-money

### Method boundary

本稿遵守 `docs/METHOD.md`：archive locator 未实际打开检查时不算 verified capture；`没有验证到` 不写成 `当时不存在`；涉及私人财务数据时执行研究必要最小化。
