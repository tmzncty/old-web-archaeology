# CREDIT APPLICATION / REPORT QUERY / UNDERWRITING STATE GAPS, 2000–2015

Status: research note / state-gap model  
Scope: 约 2000–2015 中文 Web 中信用卡网申、个人征信网上查询、身份验证、授信审批和信用记录自查的页面/状态链；**不把本仓扩展成全球信用史，也不研究 2015 年以后移动消费贷产品的完整历史**。  
Cross-repo companion: `tmzncty/how-people-lived/topics/credit-history-borrowing-future-income-and-financial-legibility-china-1985-2026.zh-CN.md`  
Last research pass: 2026-09-05

---

## 0. Why credit Web pages are not ordinary forms

本仓已有 `ONLINE_BANKING_REMITTANCE_AND_PAYMENT_STATE_GAPS_1997_2015.md`，研究的是：

```text
已有账户 / 已有资金或额度
→ 授权
→ 支付/转账
→ 清算
→ 到账
```

本 note 研究的是更靠前的一层：

```text
一个人还没有这笔信用
→ 她提交关于自己的材料
→ 某个机构判断是否相信她的未来偿还能力
→ 才决定要不要创建额度 / 贷款 / 卡
```

因此信用卡网申页面不是简单的：

```text
form → submit → done
```

完整链至少可能是：

```text
public product page
→ eligibility wording
→ application entry
→ applicant identity fields
→ employment / income / residence fields
→ consent / authorization
→ browser-side validation
→ request sent
→ server receipt
→ application persistence
→ duplicate / fraud / identity checks
→ credit-report query authorization
→ bureau data retrieval
→ bank internal underwriting
→ approve / reject / manual review
→ credit line
→ card production
→ physical delivery / branch pickup
→ original-ID or signature verification
→ activation
→ actually usable credit
```

一个 archive capture 最容易保存的是前面 3–5 层；真正决定“这个人后来有没有一张能刷的卡”的状态，大多在认证后的银行后台。

核心原则：

> **application surface survives far better than underwriting state.**

---

## 1. Evidence contract

遵循 `docs/METHOD.md`。

### 1.1 Research units

必须把以下对象分别记录：

- `bank_or_credit_provider`
- `public_site_or_host`
- `product_page`
- `application_form`
- `applicant_identity_state`
- `consent_state`
- `application_request`
- `application_record`
- `credit_report_query`
- `underwriting_state`
- `credit_limit_state`
- `card_production_state`
- `delivery_or_pickup_state`
- `activation_state`
- `personal_credit_report_platform`
- `identity_verification_state`
- `report_request`
- `report_release_state`
- `capture`
- `claim`

不能把：

```text
“页面上可以填写信用卡申请”
```

和：

```text
“银行已经批准该自然人 10,000 元额度，卡片已制卡、已送达并激活”
```

写成同一个状态。

### 1.2 Evidence grades used here

- **A**：人民银行/征信中心/银行当年的公告、帮助、规则、产品发布文本；
- **B**：同期记者实际操作、用户教程、媒体对具体流程的测试；
- **C**：后来机构回顾；
- **D**：本 note 根据 A/B 证据明确画出的状态机和 archive-gap 推断。

Current institution pages carrying an old publication date can strongly support **the text currently preserved by that institution**. They are not automatically historical mementos and cannot prove historical DOM, headers, charset or browser rendering.

### 1.3 Privacy stop condition

不得为了重建信用申请或征信查询：

- 测试真实身份证号；
- 尝试登录旧个人信用报告账号；
- 使用泄露信用报告、银行卡资料、手机号或 cookie；
- 重新识别新闻里已匿名的借款人；
- 收集普通人的历史信用记录作为“样本库”；
- 通过今天的表单提交虚假申请去猜 2000s 后台逻辑。

本题中相当一部分 archive darkness 是**正确的隐私边界**，不是需要被攻破的缺页。

---

## 2. 2000：地方联合征信已经存在，但不是公众 Web 自助查询

2000 年 6 月《上海青年报》报道，上海个人信用联合征信体系准备于 7 月投入使用，数据库已经汇集银行信用卡和借贷等信息。

Contemporary report (B):  
https://news.sina.com.cn/china/2000-06-13/97034.html

它能支持：

```text
institutional shared credit record existed in Shanghai
```

不能支持：

```text
ordinary resident could log into a website in 2000 and inspect the full record
```

这给 old-Web 留下一个很重要的前史边界：

> **backend networked record ≠ person-facing Web control surface.**

不要因为后来出现 `ipcrs.pbccrc.org.cn`，就把 2000 年的联合征信系统想象成一个早期个人门户。

---

## 3. 2006：信用卡“网上申请”出现，但“在线填写”不是完整授信

### 3.1 兴业银行 × 我爱卡：明确可定位的 2006 online application launch

兴业银行目前保存的一篇发布日期为 2006-08-21 的官方文本称，2006-08-01 与“我爱卡” `www.51credit.com` 合作推出“加菲猫信用卡网上申请服务”；申请者“只需花费几分钟在线填写申请表”，随后由处理中心继续服务。

Official contemporaneous text preserved by bank (A for announcement; **not verified historical capture**):  
https://www.cib.com.cn/cn/aboutCIB/about/news/2006/20060821_01.html

这条证据最多证明：

- 银行当时公开宣布存在网络申请渠道；
- `www.51credit.com` 是有价值的 historical locator；
- 用户可以在线填写信用卡申请信息；
- 银行/合作方仍存在后续处理中心。

不能证明：

- 2006 年表单的 original DOM；
- exact form action；
- 请求是否 HTTPS；
- 后台怎样持久化；
- 是否实时查征信；
- 是否自动审批；
- 填表以后无需线下验证；
- 某一个申请者实际获批。

所以必须固定：

> **online form completion ≠ completed credit issuance.**

### 3.2 这个页面本身已经透露了“Web 是获客入口，不一定是完整制度接口”

官方文本使用的是“网上营销”“网上申请渠道”“处理中心”等语言，而不是“实时授信、即时可用”。

因此最保守的状态模型是：

```text
marketing page
→ web form
→ application lead / application record ?
→ processing center
→ unknown underwriting path
→ unknown verification path
→ unknown approval state
```

问号不能被现代信用卡“秒批”经验自动补上。

---

## 4. 2006 征信手册：信用报告进入审批链，但报告不是审批结果

中国人民银行 2006 年《百姓征信宣传手册》明确：

- 全国个人信用信息基础数据库 2006 年 1 月正式运行；
- 银行经授权后可查询申请人的信用报告；
- 报告包括贷款、信用卡、担保等历史；
- 决定是否给贷款的是具体信贷机构；
- 银行还会看工作性质、居住、财务状况、当前负债和自己的信贷政策；
- 数据库不是“黑名单”。

Official handbook reproduced by CCB (A):  
https://m3.ccb.cn/chn/2006-07/06/article_2022110414390174529.shtml

所以 old-Web 必须拒绝以下常见压缩：

```text
credit report says X
→ therefore system decision = reject
```

正确状态至少是：

```text
report query authorized
→ report returned
→ report incorporated into bank decision process
+ current application data
+ bank policy
+ income / residence / debt / other checks
→ approve / reject / manual review
```

这叫 **report / decision gap**。

### 4.1 还要拆 `report` 与 `score`

2006 手册把信用报告描述成历史记录，并明确说征信中心不决定是否贷款。

因此没有明确产品证据时，不得把：

```text
个人信用报告
```

写成：

```text
一个全国统一、直接决定所有生活机会的个人分数
```

也不得把“黑名单”当成数据库的官方技术模型。

---

## 5. 2009：申请者的身份可以是一个人，偿还能力却来自第二个人

2009 年信用卡监管收紧后，同期报道记录：对已满 18 岁但没有固定工作、稳定收入来源的学生发卡时，需要落实“第二还款来源”，并确认该来源方书面同意承担相应责任。

Contemporary report citing CBRC rule (B/A-dependent):  
https://money.sohu.com/20090721/n265363349.shtml

对 Web 状态模型来说，这增加一个经常被表单截图遗漏的事实：

```text
applicant identity
≠ repayment-capacity identity
```

完整申请可能存在：

```text
student applicant
→ parent / guardian / other second repayment source
→ consent document
→ ability check
→ application eligible to proceed
```

所以旧网页即使只显示“申请人姓名”，也不能推出信用风险只绑定这个人。

这可以叫 **front-end individual / back-end household gap**。

---

## 6. 2013：个人信用报告第一次形成明确的公众 Internet 状态机

### 6.1 试点地理边界

2013 年 3 月开始，江苏、四川、重庆试点通过互联网查询本人信用报告；10 月 28 日扩大到北京、山东、辽宁、湖南、广西、广东，共 9 个省区市范围。

PBOC announcement reported by China Economic Net / People’s Daily (A/B):  
https://finance.ce.cn/rolling/201310/22/t20131022_1650337.shtml  
https://www.people.com.cn/24hour/n/2013/1024/c25408-23306996.html

因此一个 2013 页面存在并不等于“全国任何身份证都能用”。

必须保留：

> **page globally reachable ≠ service geographically eligible.**

### 6.2 注册不是一个状态，而是一段状态机

2013 同期记者实测保存了非常细的路径：

```text
visit ipcrs.pbccrc.org.cn
→ read agreement
→ submit name / certificate type / ID number
→ choose identity-verification method
→ identity verification
→ wait for registration result
→ receive activation code by SMS
→ activate within 7 days
→ choose credit-information product
→ submit query request
→ wait about 24 hours
→ retrieve result
```

Sources (B, contemporary operational reports):  
https://finance.people.com.cn/n/2013/1029/c1004-23356298.html  
https://www.chinanews.com/gn/2013/10-29/5435866.shtml

所以：

```text
account registration request
≠ identity verified
≠ account activated
≠ credit-report query submitted
≠ report generated
≠ report retrieved by user
```

任何一张“注册成功”截图都不能跨过后面这些状态。

### 6.3 `identity verification failed ≠ identity false`

当时提供数字证书验证和私密性问题验证等方式。中国金融信息网的同期报道明确说，如果问题验证答案与征信系统记录不一致，用户会验证失败；用户可以改用数字证书或线下查询。

Source (B, 2013 Xinhua financial information reporting):  
https://www.cnfin.com/rmb-xh08/a/20130503/1166038.shtml

北京商报记者随后实际遇到的问题更能说明这一点：验证问题可能要求回忆几年前在哪家银行贷款、月供和频率，记者和同事都曾答错/未通过。

Source (B, contemporary user-operation report):  
https://www.zghnzx.com/news/SkNiWTJxRy9Za08vQWVQTElrdXREdz09

因此：

> **knowledge-based authentication failure is not evidence that the real-world identity is false.**

它只证明该次验证没有满足系统条件。

这是 old-Web 考古非常重要的状态缺口，因为历史截图里一个红色“验证未通过”提示几乎无法告诉我们真实原因。

### 6.4 `query submitted ≠ report current at that second`

2013/2014 同期报道说明，Internet 查询不是实时返回：提交后通常需等待约 24 小时；2014 浙江上线报道还明确说查询结果只在平台保留 7 天。

Source (B, 2014 contemporary report):  
https://www.chinanews.com/sh/2014/03-28/6003484.shtml

所以必须拆开：

```text
source banks furnish data
→ credit bureau receives / processes
→ credit file state at some reporting time
→ user submits report request
→ report product generated
→ report released
→ user retrieves within availability window
```

页面里的“当前信用报告”不等于现实世界每个银行账户这一秒钟的状态。

---

## 7. 2014：Web 网申越来越像完整入口，但公开表单仍然看不到 underwriting

2014 年《京华时报》报道，当时工行、建行、农行、招行、交行、光大、广发等多家银行都已支持网站申请信用卡；记者观察到一些银行官网会要求姓名、身份证、家庭情况、工作情况等资料，并可在线查看办卡进度。

Source (B, contemporary reporting):  
https://finance.people.com.cn/money/n/2014/0515/c42877-25019120.html

这比 2006 “网上营销 + 处理中心”的外壳更接近一个持续的数字申请过程，但仍然不能把 progress UI 当成真实后台状态本身。

至少需要区分：

```text
front-end status label
≠ internal underwriting substate
```

例如一个页面可能只显示：

```text
审核中
```

后台实际可能分别处于：

- identity review；
- manual telephone verification；
- credit-report retrieval；
- anti-fraud check；
- duplicate application check；
- limit decision；
- card production queue。

没有系统文档时，不能从一个中文状态词反推完整内部工作流。

---

## 8. Two state machines that must never be collapsed

### 8.1 Credit-card application state machine

```text
product exists
→ product page reachable
→ applicant sees page
→ applicant appears eligible under public wording
→ form can render
→ applicant fills required fields
→ consent/authorization given
→ client validation passes
→ request sent
→ server accepts transport
→ application durable record created
→ identity verified
→ credit-report access permitted / performed
→ internal underwriting
→ manual review if needed
→ decision produced
→ credit line assigned
→ card produced
→ card delivered / picked up
→ final identity/signature check if required
→ card activated
→ usable credit exists
→ first transaction authorized
```

Hard gaps:

- `eligible wording / actual approval gap`
- `submit click / server receipt gap`
- `server receipt / durable application gap`
- `application record / identity verification gap`
- `identity verification / underwriting gap`
- `credit report / bank decision gap`
- `approval / limit gap`
- `approval / physical-card gap`
- `physical-card / activation gap`
- `activation / first-transaction gap`

### 8.2 Personal-credit-report query state machine

```text
public platform exists
→ user geographically eligible
→ registration page renders
→ registration request sent
→ identity-verification method selected
→ verification attempt
→ verification pass
→ registration accepted
→ activation code issued
→ SMS actually received
→ activation before deadline
→ user session authenticated
→ report product selected
→ query request sent
→ query accepted
→ backend report generation
→ result released
→ user retrieves before expiry
→ user reads / understands
→ user notices possible error
→ dispute submitted if needed
→ furnisher / bureau investigates
→ record corrected if justified
→ later report reflects correction
```

Hard gaps:

- `page reachable / geographic eligibility gap`
- `registration / identity-auth gap`
- `identity-auth fail / real-identity gap`
- `activation-code issue / SMS receipt gap`
- `activated account / report-request gap`
- `report request / report generation gap`
- `report release / human encounter gap`
- `report content / real-time source state gap`
- `error noticed / dispute submitted gap`
- `dispute / correction gap`

---

## 9. Archive asymmetry: why the most consequential state is usually missing

公开 Web archive 很容易保存：

- 银行信用卡产品介绍；
- “立即申请”按钮；
- 申请条件；
- 费用说明；
- 征信中心公告；
- 注册帮助；
- 查询教程；
- FAQ；
- 浏览器外壳与公共 CSS/images。

最不应该公开、因此也最难进入 public archive 的是：

- 真实身份证号；
- 工作单位、收入、家庭状态；
- 信用报告正文；
- 某银行对某人的内部评分/审批意见；
- 信贷员电话核验记录；
- 被拒原因；
- 分配的额度；
- 手机激活码；
- session / cookie；
- 异议申请；
- 银行内部 anti-fraud flags。

所以本题存在非常强的：

> **public application shell / private financial-judgment asymmetry**

历史网页会让后人觉得“办信用卡就是填这张表”，恰恰因为真正的判断从来不在公开 HTML 里。

---

## 10. A second archive bias: approval stories survive better than abandoned states

平台和银行官方新闻最爱保存：

- 新渠道上线；
- “几分钟填完”；
- 更快、更方便；
- 成功获批；
- 产品创新。

普通失败状态则更容易消失：

```text
打开表单但没填完
验证码没收到
身份问题忘了答案
申请被拒但不知道为什么
电话核验没接到
申请人后来不想办了
卡寄到旧地址
卡拿到后从未激活
```

因此不能从 archive 中大量存在的 launch announcement 推出“实际申请完成率很高”。

这是 **success-surface / abandonment-darkness gap**。

---

## 11. Browser / transport / encoding uncertainties

本轮没有实际取得 2006 `www.51credit.com` 或 2013 `ipcrs.pbccrc.org.cn` 的 verified historical memento，因此以下全部保持 unknown：

- 2006 historical page charset；
- historical TLS/HTTP behavior；
- original DOM；
- form action；
- JavaScript validation；
- IE-only / ActiveX requirement if any；
- CAPTCHA implementation；
- cookie/session lifetime；
- upload or attachment behavior；
- post-submit redirect；
- precise historic application-status vocabulary；
- 2013 exact public-shell DOM / CSS；
- 2013 certificate-component/browser dependency；
- mobile-SMS backend relationship；
- backend report-generation protocol。

现代浏览器今天能打开一个机构保存的“2006 新闻稿”，不能证明当年的申请表也能被现代浏览器重放。

---

## 12. Candidate locators — useful, but **not verified captures**

### 12.1 2006 credit-card application

Historical locator from Xingye Bank announcement:

```text
www.51credit.com
```

Current preserved announcement:

```text
https://www.cib.com.cn/cn/aboutCIB/about/news/2006/20060821_01.html
```

Candidate research questions for archive work:

- Was the Garfield-card form on `www.51credit.com` or another host/path?
- Does Wayback contain main HTML at ≥2 dates?
- Were form targets excluded from capture?
- Did the page use GB2312 / GBK / UTF-8?
- Were images/scripts on separate subdomains?
- Was HTTPS available/archived?

### 12.2 2013 credit-report platform

Historical locator repeatedly published by PBOC-related contemporary reporting:

```text
https://ipcrs.pbccrc.org.cn
```

Known contemporary help/manual locator reported by a 2013 tutorial:

```text
https://ipcrs.pbccrc.org.cn/html/czsc.html
```

This is a particularly good future M1-adjacent target because one can research the **public shell and manual without logging in or touching private credit data**.

---

## 13. Claims we can make now

### High confidence

1. **2006-08:** Xingye Bank publicly announced an online credit-card application route with `51credit.com` and described applicants filling a form online.  
2. **2006:** PBOC’s personal-credit handbook explicitly distinguished credit report from the lender’s final decision.  
3. **2009:** student-card rules required a second repayment source for adult students lacking stable work/income.  
4. **2013-03 onward:** `ipcrs.pbccrc.org.cn` was used for a staged pilot of Internet access to personal credit information.  
5. **2013:** registration, identity verification, SMS activation and later report request were distinct states; report retrieval was not instant.  
6. **2014:** multiple banks publicly supported website credit-card application, and contemporary reporting described identity/work/family fields and progress tracking.

### Medium confidence / careful wording

1. Internet credit application gradually moved more application labor away from branch counters.  
2. Personal online credit-report query gave users a new control surface for inspecting a financial record previously much more institution-facing.  
3. Public Web artifacts systematically underrepresent real underwriting, rejection and abandoned applications.

### Unknown

1. Exact 2006 `51credit.com` form DOM and HTTP transaction.  
2. Whether a specific 2006 online applicant could finish the entire process without physical verification.  
3. Exact algorithms used by individual banks to turn report + application into approval/limit.  
4. Historic server-side state names.  
5. Historic 2013 session/certificate implementation.  
6. True completion/abandonment rates for early Web applications.

---

## 14. Hindsight risks

### Risk 1 — imagining 2006 as today’s “秒批”

A few minutes to fill a form is not a few minutes to create usable credit.

### Risk 2 — treating a credit report as a universal score

The 2006 official handbook explicitly says lenders make the decision and the database is not a blacklist.

### Risk 3 — treating current preserved pages as historical mementos

Publication date belongs to the institution’s content record; historical HTML needs archive evidence.

### Risk 4 — equating auth failure with false identity

2013 knowledge-based questions could fail because the real person did not remember old loan details.

### Risk 5 — equating platform state with reality

`申请中`、`审核中`、`已通过` are front-end labels unless backend semantics are independently documented.

### Risk 6 — using leaked private financial data because the public archive is incomplete

That would violate both research ethics and this repo’s privacy boundary. The private state is allowed to remain dark.

---

## 15. Cross-repo meaning

The companion life-history note asks:

> **When could a person pull future income into the present, and how did past repayment become part of future opportunity?**

This old-Web note adds the technical caution:

> **The page through which a person asks for credit is only the outer control surface of that temporal bargain.**

The historically decisive state usually lives elsewhere:

```text
private identity
+ prior financial history
+ current income/debt
+ lender policy
→ invisible underwriting
→ future obligation
```

The public Web may preserve the button that said “立即申请”.

It rarely preserves whether that button changed this person’s life.

---

## 16. Next bounded tasks

1. Use Wayback / Memento to search `www.51credit.com` around 2005–2007 and locate a Garfield-card application artifact; record `capture_url`, `original_url`, `capture_datetime`, HTTP replay status, charset and missing subresources.  
2. Search the public, non-authenticated portions of `ipcrs.pbccrc.org.cn` around 2013–2014; prioritize user manuals/help pages over login transactions.  
3. Compare at least two dates of the same public application/help page to see how identity and browser requirements changed.  
4. If a form capture exists, inspect structure only; **do not submit it**.  
5. Continue to record rejection/abandonment as legitimate states rather than treating them as missing success data.

---

## 17. Negative result of this pass

**No 2000–2015 Chinese credit-card application or personal-credit-query historical Wayback/WARC memento was actually opened and verified to the repository’s M1 capture standard during this pass.**

Therefore this file is a **state-gap research note, not a completed archaeological case**.

In particular, the following remain unverified:

- original historical HTML;
- capture datetime;
- HTTP headers;
- charset;
- browser requirements;
- form target;
- client/server validation contract;
- private session semantics;
- underwriting implementation;
- credit-report backend protocol.

The right next step is to verify a public artifact, not to manufacture the missing transaction.

---

Initial draft: AI-assisted. Claims are intentionally scoped to source strength; private financial states remain outside the reconstruction target.
