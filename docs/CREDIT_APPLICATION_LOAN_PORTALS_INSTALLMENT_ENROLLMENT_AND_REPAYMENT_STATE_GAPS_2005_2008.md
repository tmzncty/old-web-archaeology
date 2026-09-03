# Credit Applications, Loan Portals, Installment Enrollment, and Repayment-State Gaps, 2005–2008

> Scope: 约 2005–2008 年中文互联网中的个人贷款、信用卡网上申请、信用卡分期与网上银行相关页面。研究对象不是“中国消费金融史”，也不是今天 App 借贷产品，而是一个旧网执行问题：**当一个历史网页写着“在线申请”“网上贷款”“分期付款”时，这个页面究竟能证明到哪一步？哪些真正决定借款、额度、分期、账单与还款结果的状态今天天然不可见？**

普通生活、住房/教育信贷、四种未来时间感和跨国前史另见 `tmzncty/how-people-lived`：

- `topics/credit-debt-future-income-and-repayment-calendars-china-1998-2023.zh-CN.md`

本文件遵守 `docs/METHOD.md`：platform / product page / application form / account / backend decision / transaction / statement / capture / claim 不混写；`exists / available / applied / approved / borrowed / repaid` 不互相替代。

---

## 1. 为什么信贷 Web 是一种典型的“页面比结果更容易留下”的旧网

传统网页档案最容易保存：

- 某贷款产品介绍；
- 利率/手续费说明；
- 信用卡宣传页；
- 在线申请入口；
- FAQ；
- 网上银行交易规则；
- 贷款计算器的页面壳。

但一个用户真实经历的可能是：

```text
看见产品
→ 判断自己是否符合资格
→ 填申请
→ 提交身份/单位/收入/联系方式
→ 银行后台收到
→ 征信/内部规则审核
→ 电话/短信/网点联系
→ 补纸质材料
→ 批准或拒绝
→ 核定额度/利率/期限
→ 签约或发卡
→ 激活
→ 消费/提款/放款
→ 申请分期（若有）
→ 分期审核/入账
→ 生成账单
→ 到期还款
→ 银行入账
→ 逾期/正常状态与征信更新
```

服务器端公共 Web 只覆盖其中少量步骤。

因此必须固定：

> `historical credit page capture ≠ historical credit decision`

以及：

> `loan calculator result ≠ loan offer`

> `online application submitted ≠ approved`

> `card issued ≠ credit available at a specific historical moment`

> `installment advertised ≠ transaction enrolled`

> `payment initiated ≠ account settled`

---

## 2. 研究单位必须拆开

### 2.1 product / campaign

一种信用卡、个人住房贷款、汽车贷款、消费分期或校园联名卡产品。

“建行信用卡”“中行个人贷款”都太粗；同一品牌下不同年份、地区、客群和产品规则可能完全不同。

### 2.2 public product page

公开介绍：

- 资格；
- 额度；
- 期限；
- 费率；
- 优惠；
- 申请入口。

页面存在只能证明银行当时公开提供/宣传某种路径，不能证明某人通过。

### 2.3 public application form

浏览器中可见的申请字段或提交入口。

它与后台审批数据库不是一个对象。

### 2.4 applicant identity / documents

姓名、身份证、住址、工作单位、收入、学校、联系人、资产/抵押等。

这些通常属于私人数据；旧网考古原则上不应重建普通个人完整申请档案。

### 2.5 backend application state

可能包括：

```text
created
submitted
received
duplicate
incomplete
pending review
need documents
credit checked
approved
rejected
expired
cancelled
```

这类状态很少进入公开 archive。

### 2.6 credit account / limit

获批后的账户、额度、可用额度、账单周期、还款日、利率等。

“申请成功”仍不等于某次消费时额度可用。

### 2.7 purchase / loan disbursement

信用实际进入现实生活的时点：

- 信用卡某笔消费授权；
- 房贷/车贷实际放款；
- 现金贷款到账。

### 2.8 installment enrollment

不是产品页上的“支持分期”，而是某笔已发生交易真正被纳入 3/6/12 期等计划。

### 2.9 statement / repayment state

每期账单、最低还款、全额还款、手续费、利息、逾期、银行入账与征信更新。

这些是生活后果最强、同时也是最不适合公开恢复的私人状态。

---

## 3. 最小 execution state machine

以后凡涉及“某人在 2006 年通过网页申请了一张信用卡/一笔贷款”的 claim，至少应尝试区分：

```text
C0 product exists
C1 public page is reachable
C2 applicant falls inside advertised target group
C3 application form can render in historical client
C4 required fields/documents are available
C5 application is submitted
C6 bank backend receives submission
C7 identity is matched/verified
C8 credit/internal checks run
C9 application is approved/rejected
C10 applicant is notified
C11 offline follow-up / additional documents complete
C12 contract/card/account is created
C13 card/account is activated or loan is disbursed
C14 usable limit/balance exists
C15 transaction is authorized
C16 installment is requested, if applicable
C17 installment is approved/enrolled
C18 statement is generated
C19 repayment is initiated
C20 repayment is posted
C21 overdue/normal status is resolved
C22 credit record is updated where applicable
```

必须固定：

```text
product page != eligibility
eligibility != application
application submitted != backend received
received != approved
approved != activated/disbursed
card exists != usable limit
purchase exists != installment enrollment
installment request != approved installment
statement exists != paid
payment initiated != posted
posted != every later credit-record consequence known
```

---

## 4. Evidence anchors

### E1 — 2006 中国银行：真正的“网上贷款申请”仍明确 handoff 到线下客户经理/网点

2006-11-14 的同期报道记录，中国银行在全国推出“理想之家”个人贷款网上申请服务，覆盖住房贷款、汽车消费贷款、个人投资经营贷款、抵质押信用贷款与个人信用贷款等品种。

关键操作描述是：

- 用户登录中行网站；
- 从个人金融服务/综合贷款服务进入在线申请；
- 提交贷款申请；
- 银行收到后，由最近网点的客户经理主动联系；
- 后续咨询与贷款事宜继续安排。

Source:

- 上海证券报 / 新浪财经，2006-11-14：<https://finance.sina.com.cn/money/bank/bank_opration/20061114/00003074882.shtml>

Grade: **B**（同期媒体对银行新服务的报道）。

这条证据特别适合固定：

```text
online application
!= online underwriting
!= online contract
!= online disbursement
```

Web 在这里首先是 **lead / intake interface**。

它把“必须先走进某个网点才能表达贷款需求”改成了“先远程提交，再由最近网点接手”，但真正的借款关系仍跨越 Web 与线下。

Claims supported:

- 2006 年中行确实公开推出个人贷款在线申请入口；
- 在线入口覆盖多个个人贷款品类；
- 公开流程包含网点客户经理后续 handoff。

Claims NOT supported:

- 某一历史申请表具体全部字段；
- 自动审批比例；
- 从提交到放款的平均时间；
- 当时每一种贷款是否能完全不去网点；
- 任何具体用户是否最终获贷。

### E2 — 2006 网上申请信用卡已成为被独立讨论的营销渠道

新浪财经 2006-09-27 的专题文章《网上申请信用卡：走了多久 能走多远》明确把信用卡与 Internet 的结合、网上申请信用卡作为当时已经出现的发卡/营销路径讨论，并引用 CNNIC 第 17 次调查作为潜在网络客群背景。

Source:

- 新浪财经，2006-09-27：<https://finance.sina.com.cn/money/bank/bank_card/20060927/11522951093.shtml>

Grade: **B**。

本轮没有从公开 archive 取得该文章提及的各家银行原始申请表 capture，因此只保留窄 claim：

> 2006 年，中国信用卡市场已经存在“网上申请”这一可公开辨识的渠道类别。

不据此复原任何一家银行具体的 2006 DOM、字段、JavaScript 校验或浏览器要求。

### E3 — 2006 工行个人网上银行规则：页面功能已经包括“网上贷款”，但交易资格仍被账户/注册状态约束

工商银行现仍公开一份标注 2006-08-23 更新的《个人网上银行交易规则》。其中明确：

- 特定工行账户/银行卡客户在网点注册或网站自助注册后取得网上银行交易资格；
- 不同客户类型/付费情况可获得不同交易功能；
- 功能列表包括账户查询、转账、汇款、缴费、理财、网上贷款、网上购物、银行卡服务等；
- 对外支付还可能涉及动态密码/口令卡/U盾等不同身份确认条件。

Source:

- 中国工商银行官方：<https://icbc.com.cn/icbc/html/zhangcheng/wsyh_jygz.htm>

Grade: **A**（银行官方保存、带明确 2006 更新日期的交易规则；未声称当前页面部署环境等同 2006 年服务器）。

这一材料支持：

```text
bank website reachable
!= user has transaction entitlement
```

以及：

```text
customer account exists
!= all online functions enabled
```

Archive implication:

即使今天完整保存公共规则，也没有保存某一历史账户在某一天究竟注册了什么权限、持有什么安全工具、是否有贷款资格。

### E4 — 2006 建行消费分期：分期不是购买瞬间自动发生，而是交易之后、账单之前再申请的一层状态

2006 年多家同期报道记录建设银行消费分期规则：持卡人先完成信用卡消费；消费后第 2 日至账单日前 3 个工作日之间，可向银行申请把符合起点金额的交易分 3、6、12 个月偿还；银行审核通过后才进入分期，用户按月偿还本金并支付手续费。

Sources:

- 每日经济新闻 / 新浪财经，2006-10-20：<https://finance.sina.com.cn/money/bank/bank_card/20061020/10593004910.shtml>
- 深圳商报 / 新浪财经，2006-11-15：<https://finance.sina.com.cn/money/bank/bank_card/20061115/04223078433.shtml>
- 城市快报 / 新浪财经，2006-11-15：<https://finance.sina.com.cn/roll/20061115/04421041247.shtml>

Grade: **B**（多个同期报道；部分可能共同来自银行产品信息，因此不能机械算三个完全独立 evidence family）。

这里必须区分：

```text
purchase authorized
→ transaction posts
→ installment window opens
→ user requests installment
→ bank reviews
→ installment enrolled
→ future statements generated
```

因此一张“支持 12 期分期”的历史宣传页无法证明：

- 某笔购买真的做了分期；
- 申请时仍在时间窗口；
- 银行审核通过；
- 用户后来逐期偿还完毕。

### E5 — 2006 分期“零利息”页面/宣传不能替代真实成本计算

同期《新京报》报道指出，多家银行信用卡分期宣传“零首付零利息”，但不同期限仍有手续费；文章直接比较不同手续费结构，并提醒消费者计算总成本。

Source:

- 新京报 / 新浪财经，2006-12-20：<https://finance.sina.com.cn/money/bank/bank_opration/20061220/09303180703.shtml>

Grade: **B**。

Useful boundary:

```text
headline says “interest-free”
!= zero financing cost
```

旧网页研究如果只保存营销标题、丢掉费率表或条款脚注，可能系统性高估当时产品的“免费”程度。

### E6 — 2008 大学生“卡奴”个案：账单/扣款状态甚至对当时用户本人都可能不透明

2008 年《中国青年报》采访大学生叶荟：她在办卡后发生逾期并收到银行法律投诉信，回忆自己在还清时仍没有完全弄明白资金怎样扣除；她原来计划用另一张信用卡分期购买笔记本电脑，后来因还款经历改变了想法。

Source:

- 中国青年报 / 中国新闻网，2008-12-09：<https://www.chinanews.com/cj/jrlc/news/2008/12-09/1479137.shtml>

Grade: **B**（同期第一人称经媒体采访）。

Archive relevance:

这提醒我们：

> `public terms visible ≠ user understood current account state`

真正影响体验的还有：

- 账单何时生成；
- 通知是否收到；
- 自动/主动还款路径；
- 入账顺序；
- 利息/滞纳费用；
- 当前逾期状态；
- 后续信用记录。

这些几乎都不在公共 Web archive 内。

---

## 5. 必须新增的 archive gaps

### 5.1 application-form version gap

同一“在线申请”URL 可能多年持续存在，但字段、验证逻辑、目标产品和后端接口会更新。

今天找到一个申请表，不得默认它就是 2006 年版本。

### 5.2 application-submit gap

有 form shell 不代表 submit endpoint 被 archive 捕获，更不代表当时提交成功。

```text
form rendered != POST accepted
```

### 5.3 backend-receipt gap

浏览器“提交成功”提示也未必证明银行核心系统已经形成可处理申请。

需要区分前端 acknowledgment 与后台 case creation。

### 5.4 eligibility-rule gap

公开页可能只列大类条件，真实审批还依赖：

- 年龄；
- 地区；
- 学校/单位；
- 收入；
- 资产；
- 已有负债；
- 内部策略；
- 当时征信数据。

这些动态规则通常不会完整公开。

### 5.5 credit-check gap

后台是否查询个人信用信息、查询到什么版本、评分如何，都属于不可由普通 page capture 重建的状态。

### 5.6 approval-decision gap

```text
application exists
```

与：

```text
approved/rejected
```

之间往往没有公开 artifact。

### 5.7 offline-handoff gap

2006 中行案例明确显示，online intake 后仍由最近网点客户经理接手。

电话、面谈、复印件、签名、抵押/担保等线下环节通常完全不会进入 Web archive。

### 5.8 card-delivery / activation gap

批卡以后仍可能经历：

```text
制作
→ 邮寄/领取
→ 激活
→ 设置密码
```

公开申请页无法证明这些步骤成功。

### 5.9 historical-limit gap

信用额度与可用额度是账户私有、动态状态。

某产品“最高额度 X”不代表某用户实际额度。

### 5.10 transaction-authorization gap

卡有额度仍不保证某笔消费成功：商户、网络、风控、单笔限制等都可能影响授权。

### 5.11 installment-enrollment gap

广告支持分期不等于某笔交易被分期；2006 建行材料已经证明分期可以是购买后另行申请并审核的第二流程。

### 5.12 statement-cycle gap

账单日、还款日、已入账/未入账交易、最低还款额与费用都随具体账户和时间变化。

### 5.13 repayment-posting gap

```text
user sent money
!= bank posted payment to the intended account in time
```

公共网页很难保存这一状态。

### 5.14 delinquency / credit-record gap

逾期是否形成、何时修复、怎样进入征信，是长期人生后果的一部分，但属于最不应为了考古而公开恢复的私人数据。

### 5.15 calculator/quote gap

贷款计算器或模拟结果通常基于用户输入与公开利率。

```text
simulated monthly payment
!= approved monthly payment
```

因为真实合同还可能依赖审批金额、利率、期限、担保、费用与政策时点。

---

## 6. Web 层与真实信贷层：建议的证据合同

以后遇到旧银行页面，claim 应按层写。

### Level P — public information

可证明：

- 产品被公开宣传；
- 页面写了某资格/费率/期限；
- 某个在线入口存在。

不能证明任何普通人获贷。

### Level F — form execution

若有历史 capture/截图/教程，可证明：

- 某版表单字段；
- 某浏览器能渲染；
- 提交流程被当时材料描述。

仍不能证明后台批准。

### Level B — backend state

只有银行内部、同期用户通知或强可核验材料才能推进到：

- 收件；
- 补材料；
- 审批；
- 拒绝；
- 额度。

这类材料通常不应为普通个人重新公开。

### Level T — transaction state

需要证据才能声称：

- 实际放款；
- 实际消费；
- 实际分期；
- 真实账单。

### Level R — repayment/outcome

需要进一步证据才能声称：

- 正常还清；
- 提前结清；
- 逾期；
- 进入/修复信用记录；
- 债务如何影响后续生活。

公开 archive 通常停在 P 或 F。

---

## 7. Browser / runtime：金融网页比普通静态页更不能用现代回放替代历史执行

2005–2008 的银行 Web 可能依赖：

- IE 特定行为；
- ActiveX / 控件；
- 客户端证书；
- U盾 / USBKey；
- 口令卡；
- JavaScript 表单校验；
- HTTPS / 当时证书链；
- popup / frame；
- GBK/GB2312 编码；
- session cookie；
- 后端动态接口。

工行 2006 规则已经明确不同客户可能依赖口令卡/U盾等支付身份确认工具。

因此：

> **modern browser can display page ≠ historical user could execute transaction**

尤其不能把今天仍能访问的银行品牌站点，当作 2006 年网上银行执行环境本身。

若未来尝试复原，应至少记录：

```text
historical OS assumption
browser/version
TLS/certificate limitation
security-control requirement
hardware token requirement
encoding
original host
archive rewrite
backend dependency
```

---

## 8. 一个很重要的保存偏差：**approval invisibility / complaint visibility**

顺利完成的借款流程可能只留下：

- 一张营销页；
- 一次私密申请；
- 若干银行内部记录；
- 此后多年按月扣款。

这些都不会自动进入公共互联网。

相反，如果发生：

- 被催款；
- 逾期争议；
- 盗刷；
- 申卡纠纷；
- 手续费争议；

用户更可能写论坛帖、求助媒体或进入法律报道。

因此历史公共材料可能存在 **complaint visibility bias（投诉可见性偏差）**：

> 问题账户产生的公开文字，可能比平稳偿还十年的账户更多。

不能据此推断“当时多数信贷都会出问题”。

反过来，银行产品页又天然偏向成功/便利叙事。

最好的旧网研究应把两种偏差一起保留。

---

## 9. 隐私 stop condition：金融执行状态不是“越完整越好”

以下内容不应为了补齐 state machine 而主动寻找、聚合或重新公开普通个人历史数据：

- 完整身份证号；
- 银行卡号；
- 信用卡 CVV/有效期；
- 银行余额；
- 信用额度；
- 历史账单明细；
- 收入证明；
- 联系电话/住址；
- 原始征信报告；
- 逾期与贷款记录的可识别个人对应；
- 安全问题/密码/证书文件。

因此这里存在一种 **privacy-preserving execution gap**：

> 某些最关键的历史执行证据没有进入公共 archive，恰恰是合理的隐私结果。

“无法知道一个普通人 2007 年 12 月到底欠了多少钱”通常不应被当成需要强行修补的档案缺陷。

研究目标应是恢复**状态结构**，不是恢复私人银行账户。

---

## 10. 与 `how-people-lived` 的交叉解释

旧网侧能证明：

- 2006 前后贷款与信用卡申请正在出现明确的 Web intake；
- 银行网上银行已将贷款、查询、支付等功能放进电子渠道；
- 分期具有独立的申请窗口和审核状态；
- 网上入口仍大量 handoff 到网点/客户经理；
- 真实额度、账单、还款与信用结果不会自然留在公开页面。

生活史侧则进一步问：

- 为什么一个人需要借？
- 这笔钱打开了教育、住房、迁移还是消费路线？
- 未来几年收入被占用了多少？
- 债务是否改变换工作、婚姻、生育或迁移选择？
- 什么情况下“能借到钱”是 optionality，什么情况下它变成 lock-in？

两仓边界保持为：

```text
old-web-archaeology
= 这个信用 Web 界面/执行链怎样存在、怎样消失、今天能证明什么

how-people-lived
= 信贷能力怎样改变一个普通人的生活时间表与未来选择
```

---

## 11. 已证实 / 高概率 / 不知道

### 已证实

- 2006 年中国银行已经推出覆盖多类个人贷款的在线申请入口，且后续明确 handoff 给最近网点客户经理；
- 2006 年“网上申请信用卡”已是可被同期财经媒体独立讨论的渠道；
- 工行 2006 年官方个人网银规则明确列出网上贷款等功能，并存在注册/安全工具/客户类型造成的权限差异；
- 2006 年信用卡消费分期可以是消费后另行申请、经银行审核后才进入分期的过程；
- 2008 年同期大学生采访显示，真实账单/扣款/逾期状态对用户本人都可能不完全透明。

### 高概率但本轮不升级为事实

- 多家银行 2005–2008 的信用卡在线申请表可能存在显著的浏览器、脚本与动态后端依赖；
- 某些产品页/申请页今天即使仍有 URL，也可能已被现代模板覆盖，不能直接当历史 artifact；
- 真实审批依赖征信与内部规则的程度，在 2000 年代中期快速增加，但不同银行、客群和时间点需要逐案验证。

### 不知道

- 本轮没有可靠取得 2006 年中行“理想之家”原始在线申请页面的已验证 archive capture；
- 没有可靠取得 2006 年某家银行信用卡网上申请表的 A 级 HTML/WARC 并完成历史客户端验证；
- 没有恢复任何历史普通个人的后台审批 case，也不计划以隐私代价去恢复；
- 不知道现存公共网页中的多少贷款计算器保留了当年真实 JavaScript/利率表而非后来替换版本；
- 没有足够证据对 2005–2008 各银行“在线申请 → 最终放款/发卡”的转化率作比较。

---

## 12. 下一步最值钱的证据，不是再找一张银行广告

下一步优先寻找一个**不含普通个人敏感数据**的完整历史技术链，例如：

```text
2006 银行原始在线申请 capture
+ 同期官方帮助页
+ 同期用户教程/媒体实测
+ 浏览器/控件要求
+ 明确的线下 handoff 说明
```

如果能找到，就可以精确回答：

> 一个 2006 年网页里的“在线申请”按钮，到底只是把姓名和电话交给客户经理，还是已经能走到身份验证、审批、额度与签约中的更深层状态？

在此之前，应坚持最小结论：

> **旧网页最容易保存“你可以申请”的承诺，最难保存“银行最后是否愿意把未来的钱真的借给你”。**
