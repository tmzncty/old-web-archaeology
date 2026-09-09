# Online banking, remittance, transfer, payee, authentication, clearing and recipient state gaps, 1999–2015

> Scope: 中文旧网约 1999–2015。研究个人网上银行、Web 转账/汇款、收款人管理、跨行转账、支付清算前端、第三方支付转账以及亲密付等“远程给别人钱”的页面、状态机和保存缺口。
>
> 不做全球汇款史，不把 1980s 邮政汇兑、2007 Kenya M-Pesa 或 2020s 家庭钱包无限写进本仓。更长的普通生活史、跨国对照和 2020–2026 家庭财政变化写入 `tmzncty/how-people-lived` 配套专题。

核心问题不是：

> “旧网页上有没有一个‘转账汇款’按钮？”

而是：

> **某一历史时点，一个普通用户从这个中文 Web 入口发起的钱，究竟走到了哪一个 authoritative state；收款人最后是否真的获得了可用资金？**

网上转账尤其容易被历史页面误导，因为它横跨：

```text
public bank site
→ authenticated session
→ payee / beneficiary
→ transfer form
→ security credential
→ bank ledger
→ payment / clearing rail
→ recipient bank ledger
→ notification
→ cash-out / spending
```

archive 通常只容易保存最外层页面。

---

## 0. 本轮结论摘要

本轮可以确认的历史基线：

1. **1999 年**建设银行已经推出个人网上银行，官方后期发展历程明确列出查询、转账、代理缴费、挂失等功能；1999 年 8 月北京、广州个人网银正式上线。
2. **2004 年**同期材料已经同时出现两件事：网上银行个人客户快速增长，以及用户对安全的显著顾虑；同年存在真实“木马窃取网银凭证 → 远程转走资金”的刑事案件。
3. **2006 年**建设银行官方历史记录全国个人跨行转账上线；这证明 Web 用户侧跨行汇款已进入产品能力，但不能从产品存在直接推出所有银行/所有用户都能实时到账。
4. **2010-08-30**，人民银行网上支付跨行清算系统（俗称“超级网银”）上线，把多家商业银行网银端口与跨行查询/转账进一步连接；同期测试报道出现几秒至几十秒的到账体验。
5. **2014-09**，支付宝“亲密付”把“转一笔钱给对方”变成“给亲属/伴侣一个月度代付额度”；这是 Web/移动支付史中值得和普通 bank transfer 分开的 authorization state。
6. **2015-06/10**，微信转账进入联系人关系图，10 月同期材料又保存了按实名身份共享月度免费额度和超额手续费规则。
7. historical transaction 最容易缺失：公开 archive 可以保存首页、帮助、费率、输入框甚至成功样式，却通常保存不了登录 session、证书、一次性验证码、实际扣账、跨行清算返回和收款行入账。
8. 本轮尝试直接打开约 2005 年 `www.ccb.com` 的 Wayback replay URL；当前访问链拒绝未经搜索结果建立 provenance 的构造 archive URL。搜索引擎也未返回可实际核验的对应历史 memento。因此 **M1 verified historical online-banking transaction capture: NOT ACHIEVED IN THIS SLICE**。

---

## 1. 开工前查重与范围边界

本仓已有：

- 在线记账 / financial-memory state gaps；
- 信用申请 / credit-report state gaps；
- 电商 checkout / payment / fulfillment；
- 手机预付费充值；
- 校园一卡通余额与挂失；
- 其他多种事务型 Web state-gap。

本稿不重复它们。

真正新增的是：

> **payer 的钱从一个远程 Web/session 发出以后，怎样穿过银行/支付机构/清算网络，最终成为 recipient 可支配的资金。**

因此：

- `bookkeeping record` 不是 authoritative bank ledger；
- `e-commerce checkout payment` 不是一般 person-to-person transfer；
- `mobile top-up` 的收款对象是运营商服务余额，不是另一个普通人的一般资金账户；
- `credit application` 是未来资金资格，不是当前存量资金移动。

---

## 2. 研究单位：不要把“网银”当成一个页面

### 2.1 institution

例如：

- 建设银行；
- 工商银行；
- 招商银行；
- 中国人民银行；
- 支付宝/支付机构；
- 腾讯/微信支付。

### 2.2 public host / site

例如历史上的：

- `www.ccb.com`；
- 某银行电子银行子域；
- 支付宝 Web 前端；
- 微信支付帮助/规则页面。

### 2.3 authenticated bank session

它与公开站点不是一个对象。

登录后可能包含：

- 账户列表；
- 余额；
- 收款人；
- 转账页面；
- 历史交易；
- 安全中心；
- 限额设置。

这部分涉及高度敏感个人数据，研究不应追求真实普通用户账号复原。

### 2.4 payee / beneficiary record

至少包含：

- 收款人姓名；
- 账号/卡号；
- 开户行；
- 地区/分支行；
- 可能的备注或联系人名。

“收款人保存成功”本身也是一个独立状态。

### 2.5 transfer instruction

一次指令可能包含：

- source account；
- payee；
- amount；
- currency；
- fee mode；
- execution time；
- memo；
- security confirmation。

### 2.6 payer bank ledger

真正决定付款方余额是否变化的 authoritative ledger。

### 2.7 clearing / payment rail

跨行时还可能经过：

- 大额/小额支付系统；
- 网上支付跨行清算系统；
- 第三方支付机构内部/银行通道；
- 其他当时支付路由。

不能从某银行前端 UI 直接推断内部 rail。

### 2.8 recipient bank/payment ledger

最终收款方是否入账是另一个 authoritative state。

### 2.9 notification

可能是：

- Web 成功页；
- 站内消息；
- SMS；
- email；
- 对方 App/账户提醒。

通知不是 ledger。

### 2.10 cash-out / spending

即使 recipient ledger 已入账，用户还可能需要：

- ATM；
- 银行柜台；
- 商户受理环境；
- 绑定银行卡；
- 支付密码/证件。

所以：

`recipient credited != recipient can immediately use in desired form`

---

## 3. 最小 transaction state machine

### 3.1 discovery / provenance

```text
bank exists
→ official historical host identified
→ online-banking entry identified
→ HTTPS / certificate / security guidance identifiable
```

硬边界：

`page looks like bank != page is bank`

2000s 网银木马/钓鱼环境使 provenance 本身成为 transaction safety 的一部分。

### 3.2 authentication

```text
public page
→ login entry
→ account/user identifier
→ password / certificate / token / USB key / other credential
→ authenticated session established
```

硬边界：

`login form captured != authentication backend captured`

`historical password rules known != historical session reproducible`

### 3.3 payee state

```text
payee identity entered
→ bank/account info entered
→ possible validation
→ beneficiary saved or one-time selected
```

硬边界：

`payee text accepted by browser != receiving bank/account validated`

### 3.4 transfer-request state

```text
source account selected
→ payee selected
→ amount entered
→ fee / timing / memo selected
→ user confirms
→ security credential accepted
→ request reaches payer bank
```

硬边界：

`confirm button clicked != payer bank accepted request`

### 3.5 debit / acceptance state

```text
request accepted
→ payer bank validates balance/limit/risk
→ payer ledger debit or hold
→ transfer instruction created
```

硬边界：

`UI success != payer ledger debit`

也存在反方向：

`UI error/timeout != no debit happened`

网络中断后最危险的问题之一正是前端不知道 authoritative commit 是否已经发生。

### 3.6 interbank clearing state

```text
payer bank instruction
→ rail submission
→ rail accepted/queued/rejected
→ recipient bank receives
```

硬边界：

`payer debited != interbank rail accepted`

`rail accepted != recipient bank credited`

### 3.7 recipient credit

```text
recipient bank receives
→ account/name/rule validation
→ recipient ledger credit
→ funds available or pending
```

硬边界：

`recipient bank message received != funds immediately spendable`

### 3.8 notification / observation

```text
transaction state changes
→ Web receipt / SMS / email / app notice generated
→ user receives notice
→ user reads notice
```

硬边界：

`notification sent != notification delivered/read`

### 3.9 reversal / return

错误收款信息、规则限制或后续异常可能导致：

```text
transfer initiated
→ debit
→ clearing reject / recipient reject
→ returned
→ payer ledger restored
```

所以一张历史“已提交”截图完全不足以证明最终结果。

---

## 4. 1999：个人网上银行已经可以远程移动账户资金

建设银行官方发展历程记录：

> 1999 年推出个人网上银行，为客户提供网上查询、转账、代理缴费、挂失等服务。

另一个建行官方回顾明确写：

- 1999 年 1 月 Internet 网站标志电子银行业务起步；
- 1999 年 8 月北京、广州推出个人网上银行。

来源：
- https://ccb.cn/cn/ebank/personal/detail/201306071370582541.html
- https://www.ccb.com/chn/2014-11/18/article_2022110414395277779.shtml

证据等级：**A/C-border — 银行官方后期历史页面。**

可以证明：

> **1999 年建行个人 Web banking 已存在查询与 transfer capability。**

不能证明：

- 全国所有地区同日可用；
- 普通家庭普遍拥有网银；
- 1999 的转账已经覆盖任意他行账户；
- 页面今天的展示就是 1999 DOM。

---

## 5. 2004：可执行性已经不只是“有网络”，还包括安全环境

### 5.1 同期用户规模与安全顾虑不能混为 adoption proof

2004-11 同期媒体引用新华社和 CNNIC 信息：国内网上银行个人客户数增长较快；不愿选择网上银行的受访者中，76% 将安全列为原因。

来源：
- https://finance.sina.com.cn/money/bank/bank_hydt/20041126/12121183655.shtml

证据等级：**B**。

用户/客户账户数字是银行/行业业务口径，不一定等于独立自然人，也不能直接推出日常转账使用频率。

### 5.2 木马案件证明 credential layer 是真实事务的一部分

2004 年长沙法院审理的同期案件中，被告被指通过木马窃取受害人网上银行账户和密码，再把资金远程转走/用于购物。

来源：
- 中国新闻网经搜狐保存：https://news.sohu.com/2004/07/08/69/news220916925.shtml

证据等级：**B — 同期司法新闻。**

对 old-Web 考古来说，它证明：

> **历史网银体验不能只复原 HTML。用户端 OS、浏览器、恶意软件、证书/密码和本地安全状态都会改变“这个页面能不能安全执行”。**

这与本仓 browser-environment 方法完全一致。

---

## 6. 2006：个人跨行转账上线，但“跨行”不能被写成一个瞬时状态

建设银行官方发展历程称，**2006 年面向全国推出个人跨行转账业务**。

来源：
- https://ccb.cn/cn/ebank/personal/detail/201306071370582541.html

证据等级：**A/C-border**。

旧网复原时至少需要知道：

- 哪些收款行可选；
- 是否需要开户行；
- 服务时间；
- 限额；
- 手续费；
- 大额/小额路径；
- 周末/节假日；
- 收款行入账处理。

一个“跨行转账”菜单不能替代这些 transaction semantics。

---

## 7. 2010：“超级网银”把前端银行与清算层之间的边界变得可见

2010-08-30，人民银行网上支付跨行清算系统上线。同期新华社/媒体说明：

- 相关商业银行网银端口可以连接；
- 用户最终可进行跨行账户查询/管理和资金汇划；
- 一些测试中跨行转账可在数秒到半分钟完成；
- 各银行具体开放、接入、费率仍有差异。

来源：
- https://news.sina.com.cn/o/2010-08-31/051018043272s.shtml
- https://news.sina.com.cn/c/2010-08-30/141218041124s.shtml
- https://finance.sina.com.cn/china/jrxw/20100831/11168577979.shtml

证据等级：**A/B**。

### 7.1 `real-time label / end-to-end reality gap`

“实时”至少可能指：

- 银行前端即时受理；
- 付款行即时扣账；
- 清算系统即时转发；
- 收款行即时入账；
- 收款人即时可用。

这些不是同义词。

因此：

> `system supports real-time transfer != every historical transfer was end-to-end instant`

### 7.2 front-end / rail provenance gap

同一个银行 Web 表单，在不同年份可能调用：

- 行内系统；
- 大小额支付系统；
- 网上支付跨行清算；
- 其他接口。

研究者不能从 2026 后端或现代帮助文档倒推 2010 historical rail。

---

## 8. 2014：亲密付不是 ordinary transfer，而是 standing authorization

2014-09 同期材料记录支付宝“亲密付”：

- 可给爱人、子女、父母等开通；
- 设置月度上限；
- 对方发生消费时由开通方账户自动扣款；
- 开通人可收到扣款提醒。

来源：
- https://news.sina.com.cn/o/2014-09-25/091330912132.shtml
- https://news.sina.com.cn/o/2014-09-26/113030919216.shtml

证据等级：**B — 同期产品报道 + 用户采访。**

因此状态机必须和 P2P transfer 分开。

### 8.1 P2P transfer

```text
payer chooses recipient
→ chooses amount
→ confirms
→ recipient balance/ledger increases
```

### 8.2 delegated payment authorization

```text
sponsor chooses beneficiary
→ sets monthly limit
→ authorization remains active
→ beneficiary later initiates merchant purchase
→ sponsor account is charged
```

硬边界：

`authorization created != money already transferred`

`beneficiary sees limit != beneficiary owns that amount as cash`

`merchant payment approved != beneficiary can withdraw/transfer balance`

这类产品如果只用“转账”一个词会完全丢失语义。

---

## 9. 2015：微信把 social contact graph 变成 transfer addressing layer

2015-10 的同期报道记录：微信转账功能在当年 6 月上线；10 月进入新的手续费测试规则。陈先生给朋友转 3 万元还款时，因超过月度免费额度看到 10 元手续费提示。

来源：
- https://media.people.com.cn/n/2015/1023/c40606-27731083.html

证据等级：**B — 同期用户案例 + 平台规则。**

这里对旧网/早期移动 Web 史的意义是：

> **收款人寻址开始从 bank-account-centric 向 social-identity-centric 移动。**

用户未必先输入：

`姓名 + 卡号 + 开户行`

而可能先在已有联系人关系里选一个人。

但这又产生新的 hard boundary：

`social account identity != legally intended bank recipient identity`

联系人被盗、账号误认或同名都可能改变实际收款主体。

### 9.1 identity-linked fee state

同期规则还显示，免费额度按身份证名下相关微信支付账户合并计算。

因此：

`app account != fee-policy identity unit`

研究单个 UI account 时不能忽略背后的实名状态。

---

## 10. 本专题新增的 state gaps

### 10.1 `displayed-success / ledger-commit gap`

```text
Web says “success”
!= payer bank ledger definitely committed
!= recipient ledger credited
```

### 10.2 `UI-error / transaction-commit gap`

反方向同样重要：

```text
browser timeout/error
!= no debit
```

历史用户可能因为页面超时重复提交，研究必须保留“前端不知道 commit”的可能。

### 10.3 `sender-debit / recipient-credit gap`

```text
sender debit
!= recipient credit
```

跨行退回、信息错误、收款行处理延迟都可能介于两者之间。

### 10.4 `payee-name / account-identity gap`

```text
human-readable payee label
!= authoritative account owner
```

浏览器保存的“妈妈”“小王”可能只是用户自定义别名。

### 10.5 `same-bank / interbank semantic gap`

行内和跨行在：

- 服务时间；
- 费用；
- 速度；
- 限额；
- 收款信息字段；

上可能不同。

不能把一个 transfer help page 的规则泛化给所有 transfer types。

### 10.6 `front-end / clearing-rail gap`

```text
same transfer form
!= same historical clearing backend
```

银行可在不明显改 UI 的情况下迁移内部 rail。

### 10.7 `real-time / spendable-funds gap`

```text
real-time transfer supported
!= recipient can immediately withdraw/spend in every channel
```

### 10.8 `notification / ledger gap`

```text
SMS received
!= authoritative ledger proof
```

伪造短信、延迟短信和漏发都可能存在。

### 10.9 `beneficiary-list / real-person gap`

保存的收款人昵称、历史联系人并不等于现实关系身份。

### 10.10 `authorization / ownership gap`

亲密付/亲属卡类：

```text
monthly spending authorization
!= beneficiary-owned balance
```

### 10.11 `fee-display / fee-posting gap`

页面显示手续费不等于最终账务中一定以相同方式扣收；历史规则版本也可能变化。

### 10.12 `transfer-history / bank-statement gap`

“最近转账”页面是应用层视图；正式账单/银行 ledger 才是更高层 authoritative record。

### 10.13 `online-initiation / offline-cashout gap`

Web 完成汇款以后，收款人仍可能只能：

- 去 ATM；
- 去柜台；
- 在特定商户使用；

因此不能从 sender online 推断 recipient online。

---

## 11. 历史浏览器与安全环境：Web banking 不是普通 HTML 网站

本仓 M3 特别适合选一个早期网银帮助/登录壳做环境实验，因为真实执行可能依赖：

- SSL/TLS 版本；
- certificate chain；
- browser support；
- ActiveX / security control；
- Java/插件（具体银行/年份需逐项证据）；
- USBKey 驱动；
- 本地证书；
- Windows 权限；
- 弹窗；
- 字符编码；
- 反钓鱼提示。

注意：

> 本轮没有为每家银行每个年份确认具体 ActiveX/USBKey 要求。

这些只能作为 **browser-environment checklist**，不能写成所有 2004 网银统一实现。

---

## 12. 为什么 archive 会系统性保存错东西

### 12.1 public-shell bias

最容易幸存：

- 银行 Logo；
- 首页；
- 网银入口；
- 安全提示；
- 产品介绍；
- 手续费表；
- 帮助 FAQ。

最难幸存：

- 登录后的账户；
- 真实余额；
- 收款人；
- transaction token；
- OTP；
- certificate handshake；
- bank ledger mutation；
- clearing response。

因此：

> **online-banking shell captured != online banking transaction captured。**

### 12.2 success-page hindsight bias

即便 archive 偶然保存一个“交易成功”式页面，也可能：

- 是静态示例；
- 没有真实 session；
- 是帮助文档截图；
- 是失败后跳转的通用模板；
- 与 authoritative ledger 无关。

不能用视觉语义替代事务证据。

### 12.3 private-history absence

真实普通人的长期转账记录最能回答生活史问题：

- 每月什么时候给父母钱；
- 大学生活费多久一次；
- 生病时突然多转多少；

但它同时也是高度敏感个人金融数据。

本仓不应以“考古完整”为理由重新公开这些资料。

### 12.4 fraud-report survivor bias

公开 Web 更容易保存：

- 木马盗款；
- 转错账户；
- 诈骗；
- 系统故障；

而不是数十亿次没有新闻价值的正常转账。

因此：

> `many surviving fraud reports != fraud was the dominant user experience`

### 12.5 marketing-survival bias

银行/平台发布的“最快”“最方便”“亲情”等产品稿，比普通用户一次平淡的转账更容易长期可搜索。

功能存在可用它们证明，效果和普及不能直接照抄。

---

## 13. preservation levels

### P0 — brand only

只确认某银行/平台存在。

### P1 — public transfer entry

确认历史公开页面存在“网银/转账汇款”入口。

### P2 — form/help semantics

保存字段、服务时间、限额、费率、收款行要求等公开规则。

### P3 — authentication environment

确认具体年份的 browser/security control/certificate/token 条件。

### P4 — demo transaction flow

有官方 demo、手册、教程可复原：

`login → payee → amount → confirmation → result`

但没有真实私人账务。

### P5 — network/protocol artifact

在合法、非私人环境下观察到请求/响应形态、endpoint、错误码等；不含真实账户秘密。

### P6 — cross-system semantic reconstruction

能用银行文档 + 央行支付系统资料说明：

- payer front-end；
- bank acceptance；
- clearing rail；
- recipient bank；

之间的边界。

### P7 — bounded historical execution reconstruction

在测试/模拟账户或公开测试材料中，能够高度可信地重建当年事务语义。

### P8 — research-sufficient maximum

不要求取得真实普通用户银行流水、密码、证书或私人收款人列表。

> **高等级金融 Web 考古不等于侵犯一个真实人的银行隐私。**

---

## 14. historical replay：本轮做到哪里

本轮尝试搜索约 2005 年 `www.ccb.com` 网上银行/转账的 Wayback historical capture。

结果：

- 搜索引擎没有返回一份可直接打开并验证的 2005 `www.ccb.com` 网银 transaction memento；
- 直接构造 `https://web.archive.org/web/20050101000000/http://www.ccb.com/` 时，当前访问链拒绝打开没有来自搜索结果/用户消息 provenance 的构造 URL；
- 因此没有实际取得并逐项检查：
  - capture datetime；
  - HTTP/replay status；
  - charset；
  - historical DOM；
  - login form action；
  - transfer form；
  - JS/security control；
  - authenticated state；
  - historical result page。

按 `docs/METHOD.md`，本轮只能记录：

> **M1 verified historical online-banking transaction capture: NOT ACHIEVED IN THIS SLICE.**

这不等于：

> “Wayback 没保存建行。”

也不等于：

> “2005 建行网银不可复原。”

只意味着**本轮当前访问路径没有完成合格 capture verification**。

---

## 15. claim / evidence table

| Claim | Evidence | Grade | Confidence |
|---|---|---:|---:|
| 1999 建行个人网银已提供转账等 | 建行官方发展历程 | A/C-border | high |
| 2004 网银安全是显著用户顾虑 | 同期市场报/CNNIC引用 | B | medium-high |
| 2004 已有木马盗取网银凭证转账案件 | 同期司法新闻 | B | high |
| 2006 建行全国个人跨行转账上线 | 建行官方历史 | A/C-border | high |
| 2010 网上支付跨行清算系统上线 | 人民银行口径/新华社同期报道 | A/B | high |
| 2010 测试出现秒级跨行到账 | 同期记者/银行测试 | B | medium |
| 2014 支付宝亲密付存在月度授权代付 | 同期媒体/用户采访 | B | high |
| 2015 微信联系人转账与手续费规则存在 | 同期用户案例/腾讯回应 | B | high |
| 2005 historical CCB transaction capture 已验证 | 本轮未取得 | — | **NOT ACHIEVED** |

---

## 16. 已证实 / 高概率 / 不知道

### 已证实

- 1999 建行个人网银已有 transfer capability；
- 2000s 网银 transaction 安全与 credential theft 是真实问题；
- 2006 跨行 Web transfer 已进入建行产品；
- 2010 跨行在线清算基础设施进一步整合；
- 2014 delegated payment authorization 已出现；
- 2015 social-contact transfer 已进入中文移动互联网生活。

### 高概率但需 capture/手册加强

- 具体银行在具体年份的收款人字段和转账 form layout；
- 不同年份 ActiveX/USBKey/证书要求；
- 2010 前后同一银行 Web transfer 背后的 rail 迁移；
- 某些“实时到账”在具体银行端的 end-to-end 语义。

### 不知道

- 1999 建行最初个人网银 transfer 的精确历史 DOM；
- 2005 某次真实 transfer 的 HTTP/transaction sequence；
- archive 是否完整保存过 authenticated demo/测试流；
- 早期银行后台 ledger 与 Web 前端的具体 message schema；
- 普通用户实际遇到的平均到账延迟分布。

---

## 17. browser / charset / plugin checklist for a future verified capture

一旦获得 1999–2010 合格历史 capture，应逐项记录：

- Original URL；
- Memento URL；
- capture datetime；
- Content-Type；
- charset（GB2312/GBK/UTF-8 等）；
- frameset / table layout；
- HTTPS 是否可 replay；
- browser sniffing；
- JS errors；
- security control/ActiveX（若证据明确）；
- certificate/USBKey instructions；
- form action；
- hidden fields/token；
- 子资源缺失；
- archive rewrite；
- modern browser 与 IE-era 环境差异。

现代页面成功打开不能写成历史 transaction 可执行。

---

## 18. privacy / ethics

金融事务属于本仓最需要克制的一类对象。

禁止为了“复原完整”去公开：

- 普通个人银行卡号；
- 姓名 + 账号组合；
- 登录凭证；
- 身份证号码；
- 手机验证码；
- 私人收款人列表；
- 完整银行流水；
- 家庭医疗/赡养等敏感转账记录。

优先使用：

- 官方 demo；
- 操作手册；
- 帮助页；
- 同期教程；
- 费率表；
- 测试环境；
- 去标识化学术数据；
- 同期公开自述中的最小必要信息。

---

## 19. 对配套生活史的贡献

这个 old-Web state model 改变了一个很容易写错的生活史句子：

> “网上银行出现以后，人们可以在家给远方家人转钱。”

真正应该拆成：

```text
remote transfer UI exists
→ user can access compatible device/network
→ authentication works
→ payee can be represented
→ payer bank accepts
→ clearing succeeds
→ recipient bank credits
→ recipient can observe/use money
```

任何一层都可能失败。

同时，2014 以后还必须加入另一条状态机：

```text
family relationship represented in platform
→ spending authorization granted
→ beneficiary makes purchase
→ sponsor account charged
```

这说明中文旧网/早期移动互联网留下的不只是“支付更方便”的历史，而是：

> **家庭关系本身逐渐被平台表示成可计算的付款权限。**

---

## 20. 下一步最小可做任务

### N1 — verified 1999–2004 bank shell capture

优先寻找：

- 建行；
- 工行；
- 招行；

至少一份有明确 capture datetime 的历史 public online-banking entry/help page。

### N2 — one contemporaneous bank manual

优先找完整官方 PDF/HTML 手册，记录：

- transfer types；
- payee fields；
- fee；
- time；
- limit；
- security control；
- result/status semantics。

若为 PDF，后续分析应同时检查页面图像，不只读文本提取。

### N3 — browser environment

对一个明确 IE-era 网银壳，在旧浏览器/modern browser 中比较：

- layout；
- JS；
- control install prompt；
- HTTPS/cert；
- charset。

### N4 — clearing provenance

把 2010 超级网银前后的前端帮助页与人民银行公开支付系统说明对齐，避免只从 UI 推断 rail。

### N5 — delegated-payment artifact

找 2014 亲密付的官方帮助/规则 capture，确认：

- beneficiary roles；
- monthly limit；
- supported transaction types；
- cancel/revoke；
- notification；
- Web/mobile boundary。

---

## 21. 本轮 research value

本轮不是新增一个“银行网站案例”，而是给事务型中文旧网补了一条此前缺失的状态链：

> **钱从屏幕上的指令变成另一个普通人真正可用的资金，中间经过哪些不可见系统？**

新增可复用 gap：

- `displayed-success / ledger-commit gap`；
- `UI-error / transaction-commit gap`；
- `sender-debit / recipient-credit gap`；
- `payee-name / account-identity gap`；
- `same-bank / interbank semantic gap`；
- `front-end / clearing-rail gap`；
- `real-time / spendable-funds gap`；
- `notification / ledger gap`；
- `authorization / ownership gap`；
- `transfer-history / bank-statement gap`；
- `online-initiation / offline-cashout gap`。

它同时强化了一条 archive 方法结论：

> **在 transaction-heavy old Web 中，最容易幸存的往往是最不 authoritative 的那层 UI；真正决定生活结果的 ledger 和 clearing state 恰恰最难保存。**