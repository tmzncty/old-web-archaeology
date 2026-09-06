# Online Banking / Postal Remittance / Money-Transfer State Gaps, 2005–2015

## Scope

本笔记研究约 2005–2015 中文旧 Web 中，普通人的异地转账、网上银行、邮政电子汇兑/网上支付入口怎样被页面、线下身份核验、银行卡网络、邮政柜台与私有账务后台共同拼出来。

它**不是**中国金融史，也不把全球 Minitel、美国 home banking 等前史扩进本仓。跨国前史、家庭汇款、迁移与代际资金流的生活史比较见 sister repository：

`tmzncty/how-people-lived/topics/from-money-orders-to-mobile-transfers-family-remittance-executability-and-distributed-household-finance-china-1980-2026.zh-CN.md`

本仓只问 old-Web archaeological questions：

- 历史 host / URL / product page 到底是什么；
- 页面能证明“存在”到哪一步；
- 哪些动作还需要柜台签约、证书、U 盾、口令卡或邮局现金入口；
- 公开 Web 壳与私有账本/清算状态之间在哪一步失联；
- 哪些 locator 可以登记为 candidate capture，哪些真正被打开验证过；
- archive 最容易让后来的研究者误判什么。

按照仓库方法：

> `bank/product ≠ site ≠ login page ≠ authenticated session ≠ submitted transfer ≠ settlement ≠ recipient usable balance`。

---

## 1. Evidence status and M1 boundary

本轮有多组 2005–2008 同时代银行功能说明、记者操作/安全报道、邮政支付工作流，以及若干明确 historical locators。

另外发现一个**候选 Wayback locator**：第三方 archive index 指向 2007-07-20 的中国工商银行英文网上银行页面：

- original URL: `https://mybank.icbc.com.cn/icbc/enperbank/index.jsp`
- candidate Wayback datetime: `20070720202123`

但本轮尝试实际打开该 Wayback replay 时遭遇 `429 Too Many Requests`，并没有成功检查 memento body、header、DOM 或子资源。

因此它只能登记为：

> **candidate capture, not verified capture**。

本轮**没有完成一份满足 M1 的 2005–2010 中文网上银行/邮政支付 transaction capture 验证**。

仍为 unknown 的包括：

- historical response headers / charset；
- login form `action`；
- GET/POST 细节；
- cookie / session；
- ActiveX / security control 的具体版本；
- certificate / U 盾 challenge-response；
- recipient validation；
- transfer submit response；
- sender debit state；
- interbank clearing / postal backend state；
- recipient credit/cash-out state；
- historical browser compatibility。

这符合本仓 `docs/METHOD.md`：搜索结果里出现 Wayback 链接，不等于已经验证 capture。

---

## 2. Historical locator families

### 2.1 招商银行：`www.cmbchina.com`

2005 年同期招商银行/媒体材料已经把个人网上银行分成“大众版”和“专业版”。

同期功能说明中：

- 大众版可进行账户/工资、汇款到账等查询；
- 专业版可执行转账汇款；
- 专业版需要申请，并到银行网点办理/确认数字证书等认证步骤；
- 专业版可向国内不同地区、不同银行账户汇款。

Sources:
- 生活日报/新浪，2005-03-08，`https://finance.sina.com.cn/roll/20050308/08431411415.shtml`
- 招行内容经搜狐转载，2005-05-10，`https://business.sohu.com/20050510/n225500337.shtml`

证据等级：**B：同期产品/功能材料**。

2006 年多篇同期安全报道又用 `www.cmbchina.com` 作为真实招商银行域名，与仿冒域名对照。

证据等级：**B：同期安全报道，可支持 domain provenance，不支持具体 transaction backend**。

Important：

> `www.cmbchina.com` 可确认是当时正式银行 Web 身份的一部分，但不能由今天仍存在同域名推出 2005 年所有路径、页面、账号体系和静态资源连续。

### 2.2 中国工商银行个人网银：`mybank.icbc.com.cn`

2006 年同期安全材料给出真实个人网银 locator：

`https://mybank.icbc.com.cn/icbc/perbank/index.jsp`

同时可观察到一个非常重要的旧 Web 问题：仿冒页面会复制银行外观并诱导用户输入凭据，因此“页面看起来像银行”不是 institutional authenticity 的充分条件。

证据等级：**B：同期安全材料**。

2007 candidate capture 的英文入口为：

`https://mybank.icbc.com.cn/icbc/enperbank/index.jsp`

但如上所述，Wayback replay 本轮没有验证成功。

### 2.3 邮政网上支付：`www.udpay.com.cn`

2005 年“网汇通”同期报道明确给出：

`www.udpay.com.cn`

并描述一种很典型的 hybrid workflow：

1. 用户在 Web 注册并取得“汇户号”；
2. 资金可以通过邮政柜台或预付式网汇通卡进入账户；
3. Web 账户可用于网上支付/转账等；
4. 余额还可生成一笔 24 小时取款汇款，再到邮政联网网点兑取现金。

Source:
- 每日新报/新浪，2005-08-10，`https://news.sina.com.cn/c/2005-08-10/08526654252s.shtml`

证据等级：**B：同期业务报道**。

这个案例特别重要，因为它直接否定：

> `online payment = all-online money path`。

真实路径可以是：

```text
cash
→ post-office counter
→ Web-account value
→ online transaction
→ optional postal cash-out
```

### 2.4 “网汇 e”：邮局现金柜台 → 支付宝 Web

2007 年同期材料描述“网汇 e”：没有银行卡或网上银行的人，可以先在邮政柜台交现金/使用绿卡并设置密码，取得汇票号；之后在支付宝网页输入汇票号与密码完成充值。

Sources:
- 长江商报/新浪，2007-04-15，`https://news.sina.com.cn/c/2007-04-15/060711641728s.shtml`
- 中国经济网，2007-03-23，`https://finance.ce.cn/bank/yhsy/jsz/200703/23/t20070323_10796984.shtml`

证据等级：**B：同期业务说明**。

这类系统非常适合 old-Web archaeology，因为“网页上的充值成功”前面其实已经发生了一次完全离线的现金 transaction。

---

## 3. Do not collapse interface families

### Family A — Bank Web transfer

研究者重建状态模型（**D**，不是任何一家银行原始 schema）：

```text
official product/help page discovered
│
├─ account exists
│
├─ account eligible for online banking?
│
├─ online registration / branch activation
│   ├─ identity checked
│   ├─ service agreement
│   ├─ certificate / UShield / password card issued
│   └─ activation succeeds?
│
├─ login page reachable
│
├─ browser/security-control compatible
│
├─ authenticated session established
│
├─ recipient entered
│   ├─ name/account
│   ├─ destination bank/region
│   └─ validation succeeds?
│
├─ amount / fee / limit shown
│
├─ transaction authenticated
│
├─ submit accepted by server
│
├─ sender account debited
│
├─ clearing/routing
│
├─ recipient account credited
│
└─ recipient can withdraw/spend
```

Archive 通常最多只能保存最上游的 public shell。

### Family B — Postal cash → Web payment

研究者重建状态模型（**D**）：

```text
Web service discovered
→ Web account / identifier registration
→ user goes to post-office counter
→ cash / postal card accepted
→ remittance number / password issued
→ user returns to Web
→ number + password entered
→ backend verifies postal value
→ online balance credited
→ payment / transfer initiated
→ merchant/platform accepts
→ possible unused balance
→ optional postal cash-out
```

这里的关键是：

> **Web archaeology 只抓到中间的页面时，极容易把前后两个线下柜台状态删掉。**

---

## 4. Hard state boundaries

### 4.1 `product page exists ≠ user account eligible`

银行宣传“可网上转账”，不能证明一个普通存款账户已经开通该权限。

### 4.2 `大众版 exists ≠ third-party transfer available`

2005 年招商、浦发等产品本身就区分查询型/低权限入口与需要额外签约的专业版。

### 4.3 `online application ≠ transfer permission activated`

如果仍需本人到柜台验身份证、签约、领证书/U 盾，则网页申请只是状态链中一段。

### 4.4 `login page exists ≠ authenticated session works`

Archive 能保存登录框，不代表当年的认证服务、证书体系、ActiveX、安全控件、短信或硬件 token 还能重演。

### 4.5 `submit clicked ≠ server accepted`

没有 POST response / transaction receipt，就不能从按钮存在推断成功提交。

### 4.6 `sender debited ≠ recipient usable balance`

跨行、跨地区、邮政兑付都可能存在中间清算与到账时延。

### 4.7 `recipient credited ≠ recipient can cash out`

尤其对农村/乡镇历史场景，账户上的钱是否能在附近网点取出，是另一层 infrastructure question。

### 4.8 `fee table at time A ≠ fee at time B`

银行手续费、优惠期、同城/异地、同行/跨行、柜台/网银会变化。历史费用必须绑定日期和产品。

### 4.9 `bank claims user count ≠ household normality`

银行发布的客户数可以证明平台方口径下的规模宣称，不能直接翻译成全国成年人口、独立家庭或活跃转账人数。

### 4.10 `online payment ≠ all-online payment`

“网汇通 / 网汇 e”已经给出直接反例。

### 4.11 `official-looking page ≠ official destination`

2000s 网上银行钓鱼材料证明，视觉复制成本已经足够低。研究者必须区分：

- official bank domain；
- mirror / campaign page；
- media screenshot；
- phishing clone；
- archive replay domain。

这形成 **destination-provenance gap / 目的地来源缺口**。

---

## 5. 2005 fee pages show why Web interfaces could change household behavior

2005 年招商银行同期资费材料记录：

- 柜面异地快速汇款：5‰，最低 5 元，且不封顶；
- 网上个人银行专业版：2‰，最低 5 元、最高 50 元。

Source:
- 招行资费材料经搜狐转载，2005-01-09，`https://business.sohu.com/20050109/n223853000.shtml`

这不是“网银一定更便宜”的永久规律，而是一个特定历史时点的产品结构。

对 ordinary-life reconstruction 的意义是：

> Web 不只改变“是否要去柜台”，还可能改变一笔小额/大额异地转账的边际价格。

但只有同时知道：

- 用户是否已经开通专业版；
- 证书/U 盾成本；
- 电脑和 Internet 是否可得；
- 收款人是否能使用账户；

才有资格讨论行为变化。

---

## 6. Credential layer: the transaction is partly outside HTML

2005–2006 的个人网银材料反复出现：

- branch signing；
- digital certificate；
- U 盾；
- electronic password card；
- browser/security control。

这意味着旧网银不是一个“保存 HTML 就能复原”的对象。

即使 login page 100% 保存，真实认证链仍可能依赖：

```text
local certificate store
+ hardware token
+ browser plugin / ActiveX
+ bank-side key infrastructure
+ live account state
```

因此现代浏览器今天能打开 archive replay，只能证明 HTML shell 可显示，不能证明：

> “2006 年用户当时就是以现代浏览器看见并完成同样流程。”

旧浏览器/安全控件条件必须另外验证。

---

## 7. Security and provenance are part of ordinary executability

2006 年同期网银安全报道已经出现模仿真实招商银行、工商银行页面的钓鱼站点。

技术史上，这意味着用户必须完成一个隐藏任务：

> **在输入最高价值的账号凭据以前，先判断“我现在到的到底是不是真银行”。**

于是 online-banking executability 不只是：

`computer + Internet + account + password`。

还要加：

`destination provenance judgment`。

这与后来的搜索引擎假医院、假客服、假投诉入口属于同一类日常数字能力问题。

---

## 8. Public-Web / private-ledger asymmetry

网上银行是 archive selection bias 极强的对象。

### Public Web 比较容易留下

- 产品介绍；
- 资费表；
- “立即登录”链接；
- FAQ / 帮助；
- 安全提示；
- 客户端/控件下载说明；
- 活动宣传；
- 新闻稿。

### 真正决定钱有没有到的 private state 最难留下

- 登录后的账户余额；
- 收款账户；
- 转账金额；
- 短信/硬件 token challenge；
- POST body；
- transaction ID；
- 失败原因；
- sender debit；
- clearing status；
- recipient credit；
- cash-out；
- 退款/冲正；
- 银行内部工单。

因此形成：

> **public-service-shell / private-ledger-state asymmetry**。

Web archaeology 最容易保存“这里曾经有一个转账入口”，最难保存“某个普通家庭那一次钱到底哪天到”。

---

## 9. Preservation biases specific to money-transfer Web

### 9.1 Successful-transaction survivor bias

银行新闻稿、用户教程和媒体更容易记录成功流程；失败登录、证书过期、跨行不到账等普通失败状态系统性不足。

### 9.2 Help-page survivorship bias

FAQ、功能表、资费页面可能被 archive 抓到，authenticated workflow 却因 login/cookie/POST 天然缺失。

### 9.3 Fee-schedule drift

今天还能访问的历史资费说明，不一定代表页面整个存活期都采用同一费率。

### 9.4 Credential-layer disappearance

证书签发、ActiveX、U 盾中间件、旧浏览器兼容性可能完全脱离页面 archive。

### 9.5 Rural cash-out invisibility

城市银行 Web 页很可见；收款人在县城、乡镇、农村信用社实际如何取款，往往落在另一个制度/线下网络里。

### 9.6 Phishing preservation paradox

仿冒站、新闻截图或安全报道有时反而比真正的 authenticated transaction 更容易公开保存。研究者不能因为某张“很像银行”的历史页面活着就认定其官方身份。

### 9.7 Domain/path migration gap

银行域名长期存在，也不能证明：

- login path 不变；
- account backend 不变；
- 产品权限不变；
- 安全控件不变；
- static asset host 不变；
- historical redirect 连续。

---

## 10. Why postal-Web hybrids matter to old-Web history

“网汇通 / 网汇 e”提醒我们，2000s 中文 Web 的交易页面经常处在一个更大的现实装置中。

如果只保存网页，我们可能错误重建为：

```text
user
→ Web
→ money moves
```

同期证据支持的实际路径可能是：

```text
user cash
→ postal counter
→ postal backend
→ printed/issued number + password
→ Web entry
→ payment platform
→ merchant / online balance
```

这类 **web-to-counter / counter-to-web handoff** 是旧网生活史中特别容易消失的环节。

同样地，银行网银可能是：

```text
Web product page
→ physical branch signing
→ local certificate / hardware token
→ Web authenticated transfer
```

因此：

> **2000s 的“在线服务”常常不是纯在线系统，而是 Web 前台与物理机构共同完成的一条状态机。**

---

## 11. Relation to ordinary life without leaving repository scope

本仓不推导“Internet 导致农民工迁移更多”之类宏观因果。

它能更窄地证明：

- 2005–2008 的中文 Web 已存在可查询/可操作的个人网银产品；
- 一些高权限转账功能仍要求线下签约和额外 credential；
- 邮政支付可以把现金柜台与 Web 支付接起来；
- 手续费、到账、认证、安全来源都是不同 transaction state；
- archive 最容易失去的是最后是否到账和被家人使用。

与 sister repository 的连接点是：

> **一个网页上的“转账”按钮只证明潜在入口；普通人能否用它维持异地家庭，必须继续回到账号、网点、费用、认证、到账和收款端。**

---

## 12. Evidence table

| Claim | Evidence | Grade | What it proves | What it does not prove |
|---|---|---:|---|---|
| 2005 CMB public/professional versions had different capabilities | contemporary bank/media function pages | B | product/interface distinction | user-level adoption or success |
| Professional-version transfer required additional activation/certificate steps | contemporary product instructions | B | offline/credential handoff exists | exact backend implementation |
| `www.cmbchina.com` was treated as official CMB domain | contemporary security reports | B | destination provenance | full URL continuity |
| `mybank.icbc.com.cn/.../perbank/index.jsp` was cited as official ICBC login | contemporary security report | B | historical locator | archived DOM/session |
| 2007 ICBC English page has candidate Wayback locator | third-party archive index | candidate A locator | possible memento target | verified capture body/header |
| `www.udpay.com.cn` supported postal-counter/Web hybrid | 2005 contemporary report | B | historical host + workflow | exact HTML/POST/backend |
| “网汇 e” used postal cash/remittance number/password to load Alipay | 2007 contemporary reports | B | hybrid offline→online workflow | individual transaction outcome |
| CMB online fee differed from counter fee at a dated point | 2005 fee material | B | dated price structure | permanent/industrywide rule |

---

## 13. What is confirmed / probable / unknown

### Confirmed from contemporaneous evidence

- 2005 Chinese personal online banking already had public/professional permission tiers.
- Higher-permission transfer routes could require physical branch confirmation and cryptographic credential/security device layers.
- `www.cmbchina.com`, `mybank.icbc.com.cn`, `www.udpay.com.cn` are usable historical locator families for targeted archaeology.
- Postal-Web hybrids allowed cash to enter an online-payment chain without the user already possessing conventional online banking.
- Online and counter remittance could have different dated fees.
- Phishing made destination authenticity an actual user task.

### Reasonable inference

- For some users, Web could reduce branch-trip frequency and transfer cost after activation.
- For users without bank cards/online banking, postal hybrid systems extended online-commerce executability beyond ordinary Web-bank customers.
- Bank transaction pages are structurally underrepresented in public web archives because authentication/private state blocks crawling.

### Unknown

- exact 2005–2008 historical DOM and charset for the transaction pages discussed here;
- exact browser/plugin requirements by product/version;
- exact login and transfer form `action` endpoints;
- historical cookie/session behavior;
- how often users failed at certificate/control installation;
- success/failure rates of interbank transfers;
- how quickly rural recipients could cash out after ledger credit;
- whether the 2007 candidate ICBC Wayback page can later be replayed and validated;
- whether Common Crawl/other WARC sources contain a better public capture of these same product/help pages.

---

## 14. Next archive work

1. Re-check the 2007 ICBC candidate memento when Wayback replay is available; record original URL, memento datetime, HTTP status, charset, DOM, subresources and whether it is a login shell/error/redirect.
2. Search dated variants of `mybank.icbc.com.cn/icbc/perbank/index.jsp`, but do not automate high-volume querying.
3. Locate 2005–2008 CMB product/help URLs under `www.cmbchina.com`; prioritize public help/fee pages over authenticated user material.
4. Check Internet Archive / Common Crawl for `www.udpay.com.cn`; retain only public platform structure, not ordinary users' payment identifiers.
5. If an authentic transaction shell is recovered, document browser/IE/ActiveX/certificate assumptions before any visual reconstruction.
6. Do not attempt to reproduce live authentication or interact with real bank accounts; this project studies historical public Web evidence, not banking systems.

---

## 15. Privacy and safety boundary

Money-transfer archaeology has a stricter-than-usual private-state boundary.

Do not collect or republish:

- bank-card/account numbers;
- remittance numbers/passwords;
- transaction IDs tied to ordinary people;
- historic private balances;
- identity documents;
- private transfer screenshots;
- leaked authenticated pages.

For mechanism research, public product/help pages, dated fee schedules, official/security documentation and abstract URL patterns are sufficient.

---

## 16. Archaeological takeaway

旧 Web 里最容易保存下来的是一句：

> “网上转账”。

但普通人当年真正面对的是更长的一条链：

> **先去柜台开权限、拿证书或 U 盾，回家用对浏览器、进入真的银行域名、通过认证、填对收款信息、支付手续费、让后台真正接受，再等另一端账户到账，而且家人所在的地方还必须能把这笔钱变成可用余额。**

所以这条研究线真正给中文旧网考古增加的，不是又一个“早期网银页面”，而是一个必须长期保留的原则：

> **public Web state 能证明钱“看起来可以被移动”到哪一步，private ledger 与现实收款状态从哪一步开始彻底失联。**
