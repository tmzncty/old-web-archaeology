# ONLINE INSURANCE QUOTE / APPLICATION / UNDERWRITING / POLICY / PAYMENT / CLAIM STATE GAPS, 2000–2015

Status: research note / state-gap model  
Scope: 约 2000–2015 中文 Web 中商业保险产品页、在线投保、电子签名/数字证书、在线支付、电子保单、WAP 理赔查询、跨地域互联网保险与售后服务状态；**不把本仓扩展成中国商业保险通史，也不研究 2015 年以后 App/小程序保险的完整历史。**  
Cross-repo companion: `tmzncty/how-people-lived/topics/commercial-insurance-risk-pooling-shock-absorption-and-life-course-optionality-china-1979-2026.zh-CN.md`  
Last research pass: 2026-09-05

---

## 0. Why an insurance Web page is not a policy

本仓已经分别研究过网上银行、信用申请、电子商务 checkout、远程文书和长期账户状态。保险把这些状态叠在一起，但又多了一层关键差异：

> 用户不是只买一个商品，而是在今天建立一个未来条件事件发生时才可能兑现的合同关系。

因此：

```text
product page
≠ quote
≠ application
≠ underwriting acceptance
≠ payment
≠ policy issuance
≠ policy in force
≠ claimable event
≠ claim accepted
≠ indemnity paid
```

一个 archive capture 最容易保存的是“立即投保”“最高保额”“在线购买”这类公开销售壳层；真正决定普通人的风险有没有被转移的健康/职业/财产告知、核保结论、保单版本、续费、报案材料、拒赔理由和赔款流水，往往在认证后的私有状态中。

核心原则：

> **marketing shell survives far better than insured state.**

---

## 1. Evidence contract

遵循 `docs/METHOD.md`。

### 1.1 Research units

必须把以下对象分别记录：

- `insurer`
- `public_site_or_host`
- `product_page`
- `quote_surface`
- `application_form`
- `identity_or_certificate_state`
- `risk_disclosure_state`
- `application_request`
- `application_record`
- `underwriting_state`
- `premium_quote_state`
- `payment_state`
- `policy_generation_state`
- `policy_delivery_state`
- `coverage_effective_state`
- `renewal_state`
- `claim_report`
- `claim_evidence_state`
- `claim_liability_state`
- `claim_payment_state`
- `claim_status_query`
- `capture`
- `claim`

不能把：

```text
“2005 年页面显示可以在线购买旅行险”
```

和：

```text
“某个自然人已完成真实告知、通过核保、支付保费，电子保单已签发且保障已生效”
```

写成同一个状态。

### 1.2 Evidence grades used here

- **A**：监管规则、保险公司当年的产品/服务公告、历史帮助文本；
- **B**：同期媒体实际操作、同期消费者第一人称、同期行业报道；
- **C**：后来机构史/品牌回顾；
- **D**：本 note 根据 A/B/C 明确画出的状态机、archive-gap 与 browser-gap 推断。

当前机构站上仍可访问、带旧发布日期的文本可以证明“机构今天保存了这份旧公告文本”，但**不是自动成为历史 memento**；它不能证明当年 DOM、HTTP headers、charset、JS、CSS、证书插件或真实 transaction。

### 1.3 Privacy stop condition

不得为了重建保险交易：

- 测试真实身份证号、保单号、银行卡或健康告知；
- 尝试登录旧客户账号；
- 使用泄露保单、理赔材料、病历、电话、cookie 或支付凭证；
- 重新识别报道里匿名投保人或被保险人；
- 用今天的在线投保表单提交虚假风险信息去猜 2000s 后台逻辑；
- 把私人保单、拒保/加费原因或赔款记录做成公开“样本库”。

本题中大量 transaction darkness 是正确的隐私边界，而不是应被攻破的考古缺页。

---

## 2. 2004：产品发现和自助组合先上 Web，但不等于完整交易闭环

2004-12-14 的同期报道记录，人保财险在 `www.e-picc.com.cn` 推出第二代 e 系列网上专用产品，消费者可以对旅行意外、医疗、家庭财产、境外救援等保障内容和期限进行自助选择、组合。

Contemporaneous report (B):  
https://business.sohu.com/20041214/n223488912.shtml

这能支持：

```text
product discoverability existed
+ user-configurable coverage choices existed
+ www.e-picc.com.cn is a historical locator
```

不能自动支持：

```text
quote == final premium
application == accepted risk
product visible == available to every visitor
coverage selected == policy issued
```

因此必须固定：

> **coverage selection ≠ contractual coverage.**

同一张页面可能只是把若干保障选项展示给用户；真正的承保边界仍取决于后续身份、告知、核保、支付和合同签发状态。

---

## 3. 2005-02：一个很重要的反例——“网上投保已开通”不等于用户已经把它当成普通生活渠道

2005-02-08《南京日报》同期报道，一家保险公司网上保险业务半年只卖出 10 单；报道同时指出，当时一些保险网站仍以公司/产品介绍为主，网上可选品种有限，实际可操作性不一。

Contemporaneous local report (B):  
https://news.sina.com.cn/s/2005-02-08/06125087693s.shtml

它特别适合 old-Web 的 `exists / available / used / popular` 四分法：

```text
website exists
≠ transaction route usable
≠ users know the route
≠ users trust the route
≠ route is common
```

因此不能从“2004/2005 已有网上保险产品”直接写成“2005 普通家庭已经习惯网上买保险”。

这一材料也提醒 archive 研究者：产品页的幸存概率通常远高于“半年只卖十单”这种失败或低使用度状态。如果只看幸存页面，很容易把早期 Web 保险重建得比当年真实生活更成熟。

---

## 4. 2005-04：电子保单把身份、证书、支付、核保和合同生成绑成一条数字状态链

2005-04-01《电子签名法》实施当天，人保财险宣布推出电子保单。同期报道把流程描述为：登录 e-PICC、选择产品、在线支付保费、生成/接收电子保单；另一个同期报道明确说，个人需要先在北京数字证书认证中心或北京银行网点申请个人数字证书，电子保单当时支持多家银行的网上支付。

Contemporaneous reports (B+):  
https://finance.sina.com.cn/money/insurance/bxyx/20050404/10131485019.shtml  
https://finance.sina.com.cn/roll/20050404/00031483552.shtml

这至少说明 2005 的完整数字保险交易不能简化成：

```text
browser -> click buy -> done
```

更保守的状态机是：

```text
browser/network ready
→ personal digital certificate ready
→ product selected
→ application/risk data entered
→ request sent
→ server accepts request
→ underwriting path
→ premium/payment authorization
→ payment result
→ policy contract generation
→ electronic signature/seal state
→ electronic policy delivery
→ coverage effective state
```

### 4.1 certificate-readiness gap

当时的个人数字证书需要另外取得。因此：

```text
user has Internet
≠ user has required certificate
≠ browser can use certificate correctly
```

本轮没有 verified historical capture，也没有验证 2005 e-PICC 对 IE、ActiveX、特定 CSP/控件或 TLS 版本的精确要求，因此**不得**从“需要数字证书”继续脑补成某个具体浏览器依赖。

### 4.2 payment / policy gap

同期新闻把“网上支付”和“发送电子保单”写成连续流程，但 archive 研究必须把它们分开：

```text
payment page rendered
≠ payment request sent
≠ bank authorization success
≠ insurer received settlement/reference
≠ underwriting accepted
≠ policy generated
≠ policy delivered
≠ coverage in force
```

即使今天找到一张“支付成功”截图，也不能单凭截图证明保险后台已经创建有效保单。

### 4.3 electronic-policy / historical-rendering gap

电子保单具有法律意义，不代表今天 archive 回放出来的 PDF/HTML 就一定是当年原文件。必须分别记录：

- 原始保单文件是否存在；
- 是否由平台后来重新生成；
- 是否有签章/证书对象；
- archive 是否保存二进制子资源；
- 当前渲染是否仍能验证历史签名。

没有这些证据时，只能说“当时存在电子保单服务”，不能复原具体自然人的真实保单。

---

## 5. 2006：第一人称证明“网上购买”仍可能是数字前台 + 物理交付

2006-08-23《南京日报》报道金融机构员工“小蒋”准备一家三口去黄山，夫妻通过网络购买 7 天旅行意外保险，总计 50 元；报道明确写到，他后来拿到的是保险公司**送上门的纸质保单**。

Contemporaneous first-person via newspaper (B+):  
https://news.sina.com.cn/s/2006-08-23/07089826313s.shtml

这条证据非常重要，因为它阻止我们用今天的“手机电子保单”心智回填 2006：

```text
online purchase entry
+ remote transaction convenience
+ physical policy delivery
```

可以同时存在。

因此新增：

> **front-end digitization / back-end physical delivery gap.**

一个历史页面即使明确写“网上保险”，也必须继续问：

- 合同最终以电子文件还是纸件交付？
- 是否需要快递/业务员送单？
- 签名、身份核验是否仍在线下完成？
- 发生争议时用户保存的是哪个版本？

这些问题不能用品牌名或“在线”二字代替。

---

## 6. 2007：机构自己的五年史证明“Web 销售”和线下理赔服务长期并存

人保财险 2007 年保存的 e-PICC 五年大事记回顾：2005 年推出全流程电子化投保/支付/电子保单；2006 年已有网上交强险和手机投保；2007 年北京分公司又为电子商务渠道车险客户提供送单、移动 POS 收费、事故车托管和理赔服务专员陪同等服务。

Participant history, dated 2007 (A/B for what PICC said about its own service; not independent adoption evidence):  
https://property.picc.com.cn/cx_gywm/zxzx/xwsd/200711/t20071128_71110.html

这形成一个非常重要的反例：

> **digital sales does not imply dematerialized claims.**

车险事故需要车辆查勘、维修、现场材料和人与物的移动。即使购买入口已经 Web 化，事故后的执行仍可能高度线下。

所以：

```text
sales portability
≠ service portability
≠ claims portability
```

这也是为什么 old-Web 不能只考古“Buy now”按钮。

---

## 7. 2009：WAP 把“买”和“看理赔进度”都搬到手机，但状态可见不等于状态完成

2009-12-10 中国保险行业协会同期报道，中国人保财险推出 `wap.epicc.cn`，支持手机投保、手机支付、车险理赔信息查询；车险客户可输入保单号和被保险人证件号码查看报案后理赔进展。

Contemporaneous industry record (B+):  
https://www.iachina.cn/art/2009/12/10/art_23_5988.html

这说明移动 Web 的意义不只在“销售随身化”，还出现：

> **claim-state visibility / 理赔状态可见性。**

但必须固定：

```text
claim status page visible
≠ backend claim state fully exposed
≠ liability accepted
≠ amount finalized
≠ payment initiated
≠ money received
```

### 7.1 query-input / identity gap

报道说需要保单号和被保险人证件号码。历史考古只能记录这种**字段类别**，不应搜集真实自然人的号码作为样本。

### 7.2 WAP browser gap

`wap.epicc.cn` 是有价值的 historical locator，但本轮没有取得并验证当年 WAP memento，因此以下仍为 unknown：

- WML / XHTML-MP / HTML 具体形态；
- charset；
- User-Agent 分流；
- 手机浏览器/网关要求；
- session/cookie 机制；
- 支付跳转；
- 理赔查询 endpoint；
- 页面是否按设备重写。

不能因为今天“手机网页”通常是 HTML5，就把 2009 WAP 自动重建成现代移动站。

---

## 8. 2015：监管文本把互联网保险正式写成多状态服务，而不是单纯销售页面

2015-07-22 印发、10 月 1 日起实施的《互联网保险业务监管暂行办法》明确把互联网保险定义为依托互联网和移动通信等技术订立保险合同、提供保险服务的业务，并规定销售、承保、理赔、退保、投诉处理、客户服务等核心保险经营行为由保险机构管理负责。对部分跨区域经营的险种，监管还特别强调异地售后和理赔服务能力。

Regulator text / Q&A (A):  
https://www.cac.gov.cn/2015-07/27/c_1116055547.htm  
https://www.cac.gov.cn/2015-07/28/c_1116058148.htm  
https://www.cac.gov.cn/2015-07/31/c_1116135318.htm

这给 old-Web 一个很强的历史边界：到 2015，监管已经不接受把“互联网保险”理解成一个孤立 marketing lead 页面；至少规范意义上的业务生命周期包括：

```text
sales
→ underwriting
→ policy/service
→ claim
→ surrender
→ complaint
→ customer service
```

同时监管要求页面披露保险产品、免责、理赔、退保等重要信息。这说明面对面代理减少后，**解释劳动没有消失，而是部分搬到页面、链接、确认框和用户自己的阅读上。**

因此新增：

> **agent-mediated interpretation -> self-service contract reading.**

但 `disclosure displayed ≠ disclosure read ≠ disclosure understood`。

---

## 9. Full state model

### 9.1 Product / quote / application

```text
product exists
→ public page exists
→ user discovers page
→ page renders in historical client
→ user selects product/coverage
→ quote inputs entered
→ quote calculated/displayed
→ user decides to apply
→ identity/risk-disclosure fields completed
→ legal/disclosure confirmation
→ request sent
→ server receipt
→ durable application record
```

状态缺口：

- `product-exists / public-page gap`
- `page-visible / historically-renders gap`
- `coverage-selected / contractual-coverage gap`
- `quote-displayed / final-premium gap`
- `submit-clicked / server-receipt gap`
- `server-receipt / durable-record gap`

### 9.2 Identity / certificate / underwriting

```text
identity asserted
→ certificate/identity mechanism available
→ certificate accepted
→ risk disclosure accepted as complete
→ underwriting begins
→ automated/manual review
→ standard / surcharge / exclusion / reject / supplement-needed
→ final underwriting decision
```

状态缺口：

- `Internet-access / certificate-readiness gap`
- `identity-field / identity-verified gap`
- `disclosure-sent / disclosure-complete gap`
- `application / underwriting-decision gap`
- `public-eligibility / actual-insurability gap`
- `standard-product / individual-exclusion gap`

### 9.3 Payment / policy / effective coverage

```text
premium amount determined
→ payment method selected
→ bank/payment request
→ payment authorization
→ insurer recognizes payment
→ policy generated
→ electronic/physical policy delivered
→ policy accepted/received by user
→ effective date/time reached
→ coverage in force
→ renewal/premium calendar maintained
```

状态缺口：

- `payment-button / bank-authorization gap`
- `bank-success / insurer-recognition gap`
- `premium-paid / policy-issued gap`
- `policy-issued / policy-delivered gap`
- `policy-delivered / effective-coverage gap`
- `policy-exists / renewal-current gap`

### 9.4 Claim

```text
loss/event occurs
→ user recognizes possible covered event
→ claim reported
→ insurer creates claim record
→ evidence requested
→ evidence submitted
→ completeness checked
→ supplement request if needed
→ liability reviewed
→ covered / denied / partially covered
→ amount determined
→ payment initiated
→ settlement received
→ repair/treatment/family liquidity effect
```

状态缺口：

- `event / claim-recognition gap`
- `report-made / claim-record gap`
- `claim-record / evidence-complete gap`
- `evidence-complete / liability-decision gap`
- `liability-accepted / amount-finalized gap`
- `amount-finalized / payment-received gap`
- `payment-received / loss-fully-absorbed gap`

### 9.5 Service portability

```text
online sale available in region A
→ policy sold to resident/traveler
→ event occurs in region B
→ local reporting route exists
→ survey/medical/repair evidence obtainable
→ insurer service network can act
→ claim continues without forced return to region A
```

状态缺口：

- `sales-geography / claims-geography gap`
- `online-contract / offline-service gap`
- `cross-region-eligibility / cross-region-executability gap`

---

## 10. Archive biases specific to insurance

### 10.1 Sales-page survival bias

最容易幸存：

- 产品名；
- 最高保额；
- 保费示例；
- “在线投保”入口；
- 宣传活动；
- FAQ。

最难、也通常不应公开幸存：

- 个人风险告知；
- 身份证/银行卡；
- 健康信息；
- 加费/除外/拒保原因；
- 真实保单正文版本；
- 理赔材料；
- 拒赔理由；
- 赔款流水；
- 客服与投诉工单。

因此：

> **public-product-shell / private-risk-state asymmetry.**

### 10.2 Success-story bias

保险公司历史页和品牌稿更容易保存“国内首张”“全流程电子化”“成功理赔”等节点；失败支付、证书不能用、拒保、加费、续期失败、理赔补材料等负状态更少被公开保存。

所以：

```text
published success case
≠ ordinary transaction distribution
```

### 10.3 Current-preservation / historical-page gap

今天仍能打开一篇标注 2007 的公司新闻，只证明该机构现在保存了该文本。它不能证明：

- 2007 的 URL/path 与今天相同；
- 当年页面模板相同；
- 当年 charset 相同；
- 当年站内链接仍可点击；
- 当前 HTML 就是历史原文件。

必须把 `publication date`、`current rendering date`、`archive capture date` 分开。

### 10.4 Dynamic transaction darkness

在线投保、支付、理赔查询本身就是高动态、高隐私、高 session 依赖对象。Wayback 即使保存公共页，也很可能无法保存：

- 登录态；
- 证书选择；
- 银行支付 callback；
- 服务器端核保；
- 私有保单；
- 理赔进度 JSON/HTML；
- 已登录账户的续期与退保状态。

因此“没有在 archive 中看到交易结果”绝不等于当年交易失败。

---

## 11. Browser / certificate / encoding questions still open

### 11.1 e-PICC, 2004–2006

已知：

- historical locator: `www.e-picc.com.cn`；
- 2005 电子保单需要个人数字证书；
- 支持网上支付；
- 同期新闻称可网上智能/在线核保。

未知：

- exact historical URL structure；
- charset；
- DOM/form action；
- HTTPS/TLS 与证书部署；
- 浏览器白名单；
- ActiveX/CSP/插件要求；
- 数字证书调用方式；
- bank redirect/callback；
- 电子保单文件格式；
- session/cookie semantics。

在取得 verified capture 或当时客户端文档前，不得填这些空白。

### 11.2 `wap.epicc.cn`, 2009

已知：

- historical locator: `wap.epicc.cn`；
- 同期行业报道说明可以手机投保、支付、查询车险理赔进度。

未知：

- WML/XHTML/HTML 实际格式；
- charset；
- UA detection；
- gateway/browser assumptions；
- payment handoff；
- session management；
- claim query endpoint。

---

## 12. Candidate capture queue — locator only, NOT verified M1 evidence

本轮记录以下历史定位线索：

| Approx. date | Candidate locator | Why useful | Current status |
|---|---|---|---|
| 2004–2007 | `http://www.e-picc.com.cn/` | 产品、自助组合、电子保单、在线支付 | **locator only; not opened as verified historical memento this run** |
| 2005 | e-PICC 电子保单 transaction surfaces | 证书、支付、合同签发状态 | **unknown exact path; not verified** |
| 2009 | `http://wap.epicc.cn/` | WAP 投保、支付、理赔状态查询 | **locator only; not verified historical memento** |
| 2015 | 各保险机构互联网保险销售/服务页 | 免责、理赔、退保、客户服务披露 | **too broad; needs named-case capture before M1 use** |

候选 locator 不能写成“已经有 archive capture”。

---

## 13. Claims we can make now

### 已证实 / 高置信

1. 2004 年同期报道已记录 e-PICC 网上专用、自助组合保险产品。  
2. 2005 年同期报道已记录人保电子保单、个人数字证书、网上支付和电子保单交付链。  
3. 同期媒体也记录，2005 年部分网上保险业务使用度仍很低，因此“开通”不能等于“普及”。  
4. 2006 年同期第一人称证明，网上购买与纸质保单送上门可以同时存在。  
5. 2009 年同期行业报道记录 `wap.epicc.cn` 可手机投保、支付并查询理赔进度。  
6. 2015 年监管已把销售、承保、理赔、退保、投诉和客户服务明确看作互联网保险生命周期的一部分。  
7. 公开销售页面不能证明任何具体自然人的真实核保、保单生效或理赔结果。

### 高概率，但仍需历史 artifact

1. 2005 e-PICC 完整流程对当时浏览器/证书组件存在具体客户端兼容性要求；  
2. 当时在线支付存在银行页面/保险后台之间的 callback 或对账状态；  
3. 2009 WAP 页面按设备或协议条件提供过不同呈现。  

这些都不能在缺少 capture/manual 的情况下写成具体技术实现。

### 仍不知道

1. 2004–2006 e-PICC 的 original DOM、charset、JS、form action、证书调用方式；  
2. 2005 第一代电子保单历史文件格式与今天是否仍可验证签名；  
3. 2009 WAP 的 WML/XHTML/HTML 形态和 endpoint；  
4. 一次真实自然人 transaction 中 `submit -> payment -> underwriting -> policy` 的后台持久化顺序；  
5. 真实拒保、加费、除外和理赔补材料在 Web 界面里的历史状态表达；  
6. 2015 前跨区域销售后，异地理赔到底怎样落到不同公司/险种的具体执行路径。

---

## 14. Negative result / M1 boundary

本轮**没有取得并实际打开一份满足 M1 要求的 2000–2015 中文互联网保险完整 Wayback/WARC transaction capture**。

特别是：

- `www.e-picc.com.cn` 目前只是高价值 historical locator；
- `wap.epicc.cn` 目前只是高价值 historical locator；
- 今天可访问的 2005/2007 机构新闻页是保存文本，不是自动等于当年原 DOM；
- 同期媒体能证明功能、操作路径和用户体验，但不能替代 authenticated transaction；
- 保险私人状态涉及身份、健康和财务数据，本就不应通过重新识别或泄露数据来补齐。

因此本 note 是 **state-gap research note**，不是 M1 完整考古案例，也不勾选 `ROADMAP.md` 的 M1。

---

## 15. Cross-repo interpretation

与 `how-people-lived` 的 companion 合起来，可以得到一个很重要的生活史判断：

> Internet 并没有发明保险。它先把风险产品变得更容易发现和购买，再把保单、续费、理赔进度逐渐变成账户状态；但真正决定家庭有没有被一次冲击托住的核心状态，恰恰是最难被公开 Web 档案保存的那一部分。

这让旧网页留下一个系统性错觉：

```text
产品世界保存得很亮
真实保障结果保存得很暗
```

而对“普通人到底有多少种活法”来说，关键也不是一个页面上出现多少险种，而是：

> **事故或疾病真的发生以后，那份此前在网页上买到的承诺，是否能够在家庭最缺现金、最缺时间的时候变成可执行的赔付。**

---

## 16. Next evidence to seek

优先级从高到低：

1. 一份实际打开并记录 original URL / capture datetime / charset / DOM 的 2004–2006 e-PICC 产品或投保页面；
2. 一份同期客户端手册或帮助页，确认数字证书、浏览器和支付兼容性；
3. 一份 2009 `wap.epicc.cn` verified capture，确认 WAP 技术栈与理赔查询字段；
4. 一份非销售型同期用户记录，完整经历 `投保 -> 续期 -> 出险 -> 报案 -> 补材料 -> 赔付/拒赔`；
5. 一个跨地域投保后异地理赔的具体 2010–2015 案例，用于检验 `sales portability ≠ claims portability`；
6. 拒保/加费/除外状态的同期公开帮助文本，而不是私人保单数据。

Stop condition 保持不变：如果只能靠私人身份材料、泄露数据库或无法区分 historical original 与后来渲染，停止扩张并记录 unknown。