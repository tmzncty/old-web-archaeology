# 医疗求助旧网事务考古：论坛、博客、捐助、核验与资金使用状态缺口（中国，2000—2015）

## 0. Scope

本笔记研究 **2000—2015 中文互联网中个人/家庭大病求助如何被旧 Web 表达并执行**，重点不是“感人故事史”，而是事务状态：

- 一条求助信息在哪里出现；
- 谁发布；
- 页面怎样持续存在；
- 捐助路径是否真的在线；
- 页面显示的目标、累计数和真实到账之间有什么缺口；
- 病历、身份、家庭经济情况怎样被核验；
- 筹到的钱怎样进入患者/医院；
- 剩余款、退款和页面关闭怎样处理；
- 哪些状态今天还能被 archive 看见，哪些已经消失。

**仓库 scope 不前移。** 1990s 以前或海外的互助/telethon 只在配套生活史研究中作为前史；2016 以后水滴筹、监管和移动端众筹只作为 afterlife，用于检验早期状态机是否完整。

配套生活史：

- <https://github.com/tmzncty/how-people-lived/blob/main/topics/networked-medical-appeals-catastrophic-illness-social-capital-and-emergency-liquidity-china-1991-2026.zh-CN.md>

---

## 1. 研究单位与最小 claim

按照 `docs/METHOD.md`，以下对象不得混为一谈：

```text
platform
site/host
forum board
thread/post
personal homepage/blog
fundraising project
payment endpoint
bank/payment account
historical capture
media quotation of a page
researcher reconstruction
```

尤其禁止以下跳跃：

```text
媒体说“网上求助”
→ 推断存在专门众筹平台

页面存在
→ 推断捐款按钮可用

捐款按钮可用
→ 推断支付成功

页面显示“已筹 X 元”
→ 推断患者已收到 X 元

患者收到 X 元
→ 推断 X 元全部用于治疗
```

本笔记的基本任务不是证明“网络救了某人”，而是尽量把每个动作拆回可证实的状态。

---

## 2. 证据等级

沿用仓库 METHOD：

- **A**：历史原始页面/capture、同期官方公告、平台帮助页/产品页、支付或规则文档；
- **B**：同期媒体对页面和用户操作的现场观察、同期教程/论坛讨论；
- **C**：多年后的平台/当事人回忆；
- **D**：研究者推断与复原。

本轮最大限制是：**取得了多个强 historical locator 和同期媒体对页面行为的描述，但没有取得一个按 M1 标准逐项检查过的 historical capture。** 因此这是一份 research note，不把任何现代页面或媒体引文伪装成历史原始 HTML。

---

## 3. 状态机 A：求助页面不是“有/无”二值

建议把一次旧网医疗求助拆成：

```text
NEED_EXISTS_OFFLINE
    ↓
APPEAL_AUTHORED
    ↓
PUBLISHER_IDENTITY_DEFINED
    ↓
POST/HOMEPAGE/BLOG_CREATED
    ↓
PAGE_PUBLICLY_REACHABLE
    ↓
PAGE_INDEXED_OR_LINKED
    ↓
REPOSTED / QUOTED ELSEWHERE
    ↓
DONOR_SEES
    ↓
DONOR_BELIEVES_ENOUGH
    ↓
PAYMENT_ROUTE_DISCOVERED
    ↓
PAYMENT_ATTEMPTED
    ↓
PAYMENT_SETTLED
    ↓
BENEFICIARY/FUND ACCOUNT CREDITED
    ↓
FUNDS WITHDRAWN / TRANSFERRED
    ↓
TREATMENT OR OTHER EXPENSE PAID
```

每个箭头都可能失败。

关键 state gaps：

```text
PAGE_PUBLIC ≠ PAGE_DISCOVERABLE
VIEW ≠ TRUST
TRUST ≠ DONATION
DONATION_INTENT ≠ PAYMENT_SETTLED
PAYMENT_SETTLED ≠ BENEFICIARY_RECEIVED
BENEFICIARY_RECEIVED ≠ TREATMENT_PAID
```

---

## 4. 状态机 B：发帖人不一定是患者

早期案例反复出现代理发布：

```text
PATIENT
├─ self-post
├─ parent/relative
├─ classmate/student
├─ teacher/school
├─ government/work-unit official
├─ journalist/media
└─ unrelated netizen who learned the case offline
```

所以：

> **account holder ≠ patient ≠ legal beneficiary ≠ payment account holder。**

这对旧网考古尤其关键。一个 2001 年页面的站长可能只是热心网友；网页标题写患者姓名，不代表患者控制账号、密码、更新权或捐款账户。

---

## 5. 2000：东方网论坛 → 网易免费个人主页 → 线下病房

### 5.1 同期材料支持的窄 claim

2001 年 1 月《文汇报》稿件的在线转载描述：江西女孩吴梦颖因白血病在上海治疗，家庭资金已不足；**2000-10-25**，一名女大学生在东方网论坛发布求助；一名上海工作的外地网友看到后探视患者，并为她制作名为“梦颖之家”的个人主页，报道把该页放在网易免费主页 host `go7.163.com` 下。报道还记录了网友探视、提供住宿和为医院费用垫款等后续行动。

来源：

- <https://www.epochtimes.com/b5/1/1/18/n36606.htm>

证据等级：**B- / contemporaneous newspaper reprint**。

### 5.2 可登记的 historical locator

- platform family：网易免费个人主页；
- host：`go7.163.com`；
- title：`梦颖之家`；
- 原报道打印的完整 URL 已出现字符损坏，**不把损坏文本当精确 endpoint**；
- 东方网论坛原帖 URL：**unknown**。

### 5.3 已证实 / 高概率 / 不知道

**已证实（B）**

- 当时有东方网论坛求助；
- 有以该患者为对象的网易免费个人主页；
- 网页可把陌生网友带入后续线下探视与资助关系。

**高概率（D，需 capture 验证）**

- 页面可能包含病情说明、联系方式或捐助信息；
- 页面可能由热心网友而非患者本人维护。

**不知道**

- 原始 HTML；
- charset；
- frames/table 布局；
- 图片 host；
- 是否有留言簿；
- 是否有在线支付；
- 银行/邮政/现金中哪种是主要捐助路径；
- 更新频率；
- 最后存活时间；
- 是否存在 Wayback/Common Crawl 可验证 capture。

### 5.4 机制

这个案例最适合证明：

```text
forum = discovery / coordination
personal homepage = persistent address
money/care = largely offline handoff
```

所以不能把 2000 年“网上救助”直接等同于 2010s crowdfunding transaction。

---

## 6. 2000—2001：西祠胡同 SOS → 多站讨论 → 线下慈善演出

2001-02-12 的同期报道记载，南京学生孙婷患白血病，学校和区教委先组织了线下捐款；**2000 年 9 月**网名“氧气”的网友在西祠胡同发布 SOS。随后多家网站和网友社群围绕事件讨论，2001 年 2 月又组织线下演唱会，1000 多名网友到场并捐款。

来源：

- <https://www.epochtimes.com/gb/1/2/12/n46193.htm>（转引《扬子晚报》）

证据等级：**B- / contemporaneous newspaper reprint**。

### 6.1 不能从“数千帖”推出什么

报道说相关帖子/讨论很多，只能证明事件产生明显在线讨论。不能推出：

- 数千名独立用户；
- 数千名捐助者；
- 所有帖子都独立原创；
- 流量直接转化为医疗费。

### 6.2 这个案例的事务形态

```text
OFFLINE SCHOOL DONATION
→ BBS SOS
→ REPOST/DISCUSSION
→ VOLUNTEER COORDINATION
→ OFFLINE VENUE
→ CASH DONATION
```

这是早期中文旧网一个很重要的 hybrid state：**Internet 聚合关系，现实场所完成仪式和资金交接。**

---

## 7. 2007：SMS → 单位募捐 → 政府人员论坛帖

2007-04-18 同期报道观察到深圳新闻网“我说深圳事”论坛的一条公开求助。患癌外来女工此前向深圳劳动保障部门发出短信；部门内部先募得 6 万多元交给家属，随后局长在论坛发帖号召公众每人捐 10 元，并在同一帖中强调医疗/工伤保险和建立大病基金。

来源：

- <https://news.sina.com.cn/s/2007-04-18/100311664987s.shtml>

证据等级：**B / contemporaneous media observation quoting a forum post**。

### 7.1 historical locator

- host/site：深圳新闻网；
- board/column：`我说深圳事`；
- exact historical thread URL：**not yet verified**。

### 7.2 新状态：public authority amplification

早期网络医疗求助并不只来自匿名患者。这里是：

```text
PATIENT SMS
→ PUBLIC AGENCY RECEIVES
→ WORK-UNIT DONATION
→ OFFICIAL FORUM AMPLIFICATION
```

因此“谁的社会资本”也需要拆开。患者自己的社交关系、单位组织能力、官员账号的公共可信度不是同一种资源。

---

## 8. 2007：病历公开争议说明“真实性核验”在专门平台之前就存在

CCTV.com 2007 年转引的调查报道记载，一名女孩在天涯、西祠等网站发布卖长发救重病母亲的求助。部分网友要求查看病历等材料；求助方以涉及私密病情为由拒绝部分披露，随后出现激烈争论。

来源：

- <https://news.cctv.com/society/20070510/100090.shtml>

证据等级：**B / contemporaneous media observation**。

这说明下面这组矛盾并不是 2016 年以后平台审核才出现：

```text
DONOR WANTS MORE PROOF
↕
PATIENT WANTS LESS DISCLOSURE
```

旧网 artifact 研究必须注意：媒体后来最容易保存的，往往正是被公开、争议和截图放大的病历材料；这会制造**privacy-driven archive bias**。

---

## 9. 2008：博客把一次 SOS 变成“疾病过程的持续页面”

2008-09-04 《新京报》报道一名白血病儿童家庭以博客持续记录治疗并筹集移植费用。父母长期陪护、停止工作，家庭依赖亲友支持。

来源：

- <https://www.chinanews.com.cn/jk/ysbb/news/2008/09-04/1370688.shtml>

证据等级：**B / contemporaneous report quoting an active blog**。

### 9.1 forum thread 与 blog 的 state difference

论坛 thread 更接近：

```text
one SOS event
+ replies
+ bump/repost dynamics
```

博客允许：

```text
persistent account
+ chronological updates
+ archives
+ comments
+ backlinks/reposts
+ potentially repeated donation reminders
```

因此研究医疗求助时，不应把论坛、个人主页、博客全部抽象成“页面”。它们的**持续更新能力、URL 稳定性和社交传播结构**不同。

### 9.2 仍未知的技术细节

- 当事博客具体 provider/URL；
- 是否使用平台模板；
- 是否启用评论审核；
- 是否公开账户信息；
- 图片是否为外链；
- 是否存在独立捐款组件；
- 文章修改史。

没有 capture 不补全。

---

## 10. 2008：支付基础设施开始让“看见求助”与“完成捐助”距离大幅缩短

医疗个案本身的早期页面常常依赖线下/银行汇款，但 2008 年汶川地震的大规模网络捐助展示了另一个基础设施转折：支付宝等在线支付工具已经可以把门户/电商中的注意直接转成在线小额支付。

本笔记不把灾害捐助等同于个人医疗求助；它只作为支付层的 capability evidence：

> 到 2008 年前后，中文互联网已经越来越具备“网页看到 → 在线支付”连续路径，后来个人大病社交筹款可以直接复用这层基础设施。

医疗求助从此不再必然要求捐赠人记下银行卡号、去柜台/ATM 或参加线下活动。

注：本轮没有把该灾害事件作为主要个案写入 life-history companion，以免混淆公共募捐与个人求助的制度边界。

---

## 11. 2009：`donation received by organizer ≠ beneficiary received`

旧 Web 时代的另一个必须保留的状态缺口，是发起页面/组织账户收钱以后，资金可能长期没有继续移动到实际受助者。

同一类早期网络募款的媒体调查曾出现：网站/组织者账户已经收到捐款，但一年以后部分款项仍停留在管理者账户的情况。

本笔记暂不把该媒体线索升级为核心 case，因为仍需更稳定的一手/同期 source family；但它已经足以提示数据模型必须保留：

```text
DONATION_SETTLED_TO_ORGANIZER
≠ BENEFICIARY_TRANSFER_COMPLETED
```

后续若取得原项目/银行或组织公告，再升级证据等级。

---

## 12. 2010：新浪博客中的“网络自救”

2010-07-09，17 岁白血病患者方肇新开设新浪博客。2011-01-12 的近同时期调查报道回顾，家庭此前向亲友借款仍只有不足 5 万元，博客传播后累计获得 27 万多元捐助。

来源：

- <https://news.sina.com.cn/c/2011-01-12/052621800845.shtml>

证据等级：**B / near-contemporaneous investigation of a 2010 blog campaign**。

### 12.1 强 historical locator

- platform：Sina Blog；
- campaign/blog title：`请阳光照亮这一片血色`；
- launch date reported：2010-07-09；
- exact blog URL：本轮搜索结果未给出可验证历史 endpoint；
- historical capture：**not verified**。

### 12.2 新状态：patient-authored campaign

早期案例里经常是老师、网友、媒体帮患者写；这里报道把病床上的患者本人描述为博主。

但仍要区分：

```text
BLOG AUTHOR DISPLAYED AS PATIENT
≠ account credentials definitely controlled only by patient
≠ every update personally typed without assistance
```

没有原页面/账号证据，不对创作流程做更强推断。

---

## 13. 2014—2015：专门社交众筹把求助事务封装成产品

轻松筹 2014 年出现并很快将项目传播接入微信、微博和 QQ。后来的行业报道回顾，2015 年医疗救助板块已上线约 2.3 万项目、筹款约 1.8 亿元、数百万人次参与。

来源：

- 界面新闻 2020 对早期产品的回顾：<https://www.jiemian.com/article/4612894.html>
- 2016 年中国青年报对 2015 年具体项目和剩余善款争议的近同时期调查：<https://zqb.cyol.com/html/2016-03/20/nw.D110000zgqnb_20160320_2-01.htm>

证据等级：前者 **C/B — later industry reconstruction**；后者 **B — near-contemporaneous investigation**。

### 13.1 2015 应视为旧 Web scope 的边缘，而不是强行归入“纯网页时代”

这时用户路径已经明显移动化：

```text
project page
→ social share card
→ WeChat/QQ/Weibo
→ mobile login
→ online payment
```

因此本仓只研究其**与旧 Web 事务状态的接续关系**，不把 2016 以后移动众筹扩成仓库主体。

### 13.2 平台化以后必须新增的 state fields

```text
PROJECT_CREATED
IDENTITY_SUBMITTED
MEDICAL_DOC_SUBMITTED
PLATFORM_REVIEW_PENDING
PROJECT_APPROVED
SHARE_CARD_GENERATED
CAMPAIGN_OPEN
GOAL_VISIBLE
AMOUNT_RAISED_VISIBLE
WITHDRAWAL_REQUESTED
WITHDRAWAL_REVIEWED
FUNDS_DISBURSED
CAMPAIGN_CLOSED
SURPLUS/REFUND_STATE
```

这已经和 2000 年“网页 + 银行账号”是明显不同的事务系统。

---

## 14. 状态机 C：真实性不是一个 boolean

建议数据库不要使用单一：

```text
verified=true/false
```

至少拆为：

```text
PATIENT_IDENTITY_VERIFIED
FUNDRAISER_IDENTITY_VERIFIED
RELATIONSHIP_VERIFIED
DIAGNOSIS_DOCUMENT_PRESENT
DIAGNOSIS_SOURCE_VERIFIED
HOSPITAL/TREATMENT_VERIFIED
COST_INCURRED_VERIFIED
FUTURE_COST_ESTIMATE_SOURCE
INSURANCE_STATUS_DECLARED/VERIFIED
HOUSEHOLD_ASSETS_DECLARED/VERIFIED
OTHER_AID_DECLARED/VERIFIED
PAYMENT_ACCOUNT_OWNERSHIP_VERIFIED
FUND_USE_UPDATED/VERIFIED
```

原因是旧网争议经常出现：

- 病是真的，但金额是估计；
- 患者是真的，但发帖人关系不清；
- 病历是真的，但家庭资产没有独立核验；
- 捐款到账了，但最后用途无法核实。

所以：

> **one true fact does not verify the whole campaign.**

---

## 15. 状态机 D：`goal / raised / settled / withdrawn / used / refunded` 必须分开

建议任何金额字段都带 state：

```text
goal_amount
pledged_or_displayed_amount
payment_settled_amount
platform_account_balance
withdrawal_requested_amount
withdrawal_approved_amount
beneficiary_received_amount
hospital_paid_amount
other_expense_amount
remaining_amount
refunded_amount
unresolved_amount
```

### 为什么必须这样拆

2019 以后的平台争议和 2024 年监管规则都明确证明，`筹得` 与 `提现`、`使用`、`退回` 是不同事务。

作为 afterlife verification：2019 年一例平台官方声明直接出现“已筹 147,959 元但尚未申请提现”。

来源：

- <https://www.ce.cn/xwzx/shgj/gdxw/201905/06/t20190506_32003575.shtml>

2024 年五部门《个人求助网络服务平台管理办法》更把筹集、拨付、使用和退回分别规定。

来源：

- <https://wap.miit.gov.cn/zcfg/qtl/art/2025/art_2d6278e7dd114c979879c7bf667d42f3.html>

这些 afterlife evidence 不是用来把 2024 规则倒套到 2001，而是确认我们的 state model 必须从一开始就防止“页面数字 = 患者已可用资金”的偷换。

---

## 16. 状态机 E：公开病历同时是 evidence 和 privacy artifact

医疗求助旧网和一般论坛最大的不同之一，是页面可能含：

- 姓名；
- 年龄；
- 病种；
- 医院；
- 病历照片；
- 身份证信息；
- 电话；
- 家庭住址；
- 银行账号；
- 未成年人照片；
- 家庭收入/资产；
- 生殖、精神健康或其他高度敏感病情。

按照仓库 METHOD：

1. 不为了“考古完整”重新批量公开今天已难访问的普通人敏感资料；
2. 研究页面结构时优先记录字段类型，而不是复制具体号码；
3. 历史页面若包含未成年人病历，不把图片重新分发到 repo；
4. archive 可访问不等于伦理上应该再次传播。

这类案例中，**privacy preservation can legitimately limit reconstruction completeness**。

---

## 17. 支付路径：早期求助页的真正 transaction layer 仍是高优先级未知项

2000—2010 很多媒体只写“网友捐款”，却没有完整说明：

```text
cash?
postal remittance?
bank transfer?
ATM?
Alipay?
platform wallet?
organized offline collection?
```

这不是小技术细节。不同支付方式决定：

- 是否需要捐助人离开电脑；
- 是否需要知道真实姓名；
- 是否有手续费；
- 到账多快；
- 是否可退款；
- 是否留下平台日志；
- 是否容易被诈骗账号替换。

因此旧网页中出现银行账号时，研究单位至少应记录：

```text
payment_instruction_visible
account_type
account_holder_relationship_claim
online_payment_endpoint_present
payment_confirmation_present
refund_capability_known/unknown
```

而不是简单写 `donation_supported=true`。

---

## 18. 页面状态与现实医疗状态必须分开

推荐并行保存两条时钟。

### Web clock

```text
post created
→ page updated
→ repost wave
→ donation counter changes
→ campaign closed
→ page deleted / host dies
```

### medical/life clock

```text
diagnosis
→ hospitalization
→ treatment decision
→ deposit/payment deadline
→ surgery/chemotherapy/transplant
→ discharge/relapse
→ return to school/work / long interruption
```

Web clock 和 medical clock 不同步时，才会产生真正重要的解释：

- 页面传播很快，但手术窗口仍错过；
- 病情已改变，旧求助页仍在传播；
- 页面已关闭，家庭还在承担后续费用；
- 患者康复多年，历史页面仍永久暴露最私密阶段。

所以：

> **campaign success is not the same research unit as medical outcome.**

---

## 19. Afterlife：2019—2026 为什么反过来帮助我们理解 2000—2015

### 19.1 2019：家庭资产进入公众核验

2019 的平台争议显示，平台开始要求公开疾病、治疗费、家庭经济情况、医保/商业保险等；但平台当时也公开承认部分资产难以统一核实。

这反证 2000s 论坛求助不能被研究者用今天的审核框架倒推成“平台已验证”。

### 19.2 2022：注意力可以被灰色商业化

2022 年患者家属自述第一天筹得 8,000 多元、一周后增速下降，随后收到高抽成推广者联系。

来源：

- <https://finance.sina.com.cn/chanjing/cyxw/2022-07-07/doc-imizmscv0490858.shtml>

这帮助我们重新读旧 BBS 的“顶帖”“转帖”“门户转载”：它们也是 attention routing，只是当时尚未被如此成熟地商业化。

### 19.3 2024：监管把“平台应保存哪些状态”正式写清

2024 规则要求：

- 身份/求助材料；
- 真实性查验；
- 专用存款账户；
- 资金拨付审核；
- 使用更新；
- 目标完成后关闭；
- 尚未支出资金退回；
- 公开筹集、拨付、使用、退回；
- 求助信息完成后至少保存一定期限；
- 防止推广抽成。

来源：

- <https://wap.miit.gov.cn/zcfg/qtl/art/2025/art_2d6278e7dd114c979879c7bf667d42f3.html>

这份规则不能作为旧网行为证据，却是一个极好的 **state-model completeness check**。

### 19.4 2024：大规模退款证明 donation ledger 可以拥有长期可逆性

2019—2020 一名患者家庭通过平台收到 28,689 名捐助人的近 59 万元，2024 年平台核验后把资金退回原捐助人。

来源：

- <https://www.chinanews.com.cn/sh/2024/11-24/10324796.shtml>

对 old-Web 考古的意义不是道德评价，而是：现代平台保存了 `donor → campaign → transaction` 关系，可以多年后执行 reverse routing；早期论坛 + 银行转账通常没有同等级的事务可逆性。

---

## 20. 海外对照仅作方法边界，不扩仓库 scope

GiveForward 2008 年在美国上线，2009 年已经出现个人为家人医疗费用建立在线筹款页、经 Facebook 扩散并在线收款的案例；2011 年 TechCrunch 将其明确描述为面向医疗费用的在线筹款工具。

来源：

- <https://www.chicagobooth.edu/careercast/grassroots-social-entrepreneurship-with-desiree-vargas-wrigley>
- <https://techcrunch.com/2011/02/14/giveforward-raises-500k-to-be-the-kickstarter-for-medical-expenses/>

这只用于确认一个跨国共同 state transition：

```text
personal story
+ social network
+ online payment
```

可以共同形成个人医疗筹款产品。

**不把 GiveForward 写入本仓平台谱系主体。** 全球前史和跨国生活史留给 `how-people-lived`。

---

## 21. Preservation matrix

| artifact | 当年可能存在 | 今天典型保存状况 | 研究风险 |
|---|---:|---:|---|
| 论坛主题 HTML | 是 | 部分可能保存 | dynamic thread pagination / login / charset |
| 回复列表 | 是 | 常不完整 | 删除、分页、动态加载 |
| 个人主页 HTML | 是 | host 常死亡 | 子资源和图片缺失 |
| 博客文章 | 是 | 有的平台仍有 legacy render | 当前页面不等于历史 DOM |
| 病历图片 | 是 | 可能失链/被删除 | 高敏感，不应为完整性重新散布 |
| 银行账号文字 | 是 | 可能仍在旧快照 | 今天可能已复用/失效，隐私风险 |
| 捐款计数器 | 可能 | dynamic state 常丢失 | archived HTML 可能只留脚本壳 |
| 在线支付 endpoint | 后期更多 | 常失效 | 不能用现代 endpoint 证明历史成功 |
| 支付成功页 | 有 | 极难公开 archive | session/private state |
| 提现后台 | 平台化后 | 基本不可公开获得 | public page 无法证明 ledger |
| 退款 ledger | 现代平台有 | 私有事务数据 | 媒体/监管只能侧证 |
| QQ/短信传播 | 是 | 几乎不系统保存 | public Web 高估公开论坛的重要性 |
| 线下演出/募捐 | 是 | 靠新闻/照片保存 | Web archive 本身看不见最终交接 |

---

## 22. Historical visibility bias

医疗求助是旧网档案偏差最严重的对象之一。

今天最容易搜索到的往往是：

- 被门户转载的高关注个案；
- 有争议、需要“打假”的个案；
- 有明确数字的成功筹款；
- 有媒体持续跟踪的患者；
- 平台自己当作成功案例宣传的项目。

最难看见的是：

- 发帖后无人回复；
- 只有几十元/几百元帮助；
- 只在 QQ 群和短信里传播；
- 家庭主动删掉病历保护隐私；
- 患者没有写作/上网能力；
- 没有老师、同学、记者或网友代理发帖；
- 项目失败后页面很快消失。

所以：

```text
SURVIVING APPEAL CORPUS
≠ ALL MEDICAL APPEALS
≠ ALL FAMILIES WITH MEDICAL NEED
```

进一步说，**传播成功本身会提高被 archive 看见的概率**，历史样本因此天然向成功/争议项目偏斜。

---

## 23. 浏览器、编码和页面实现：目前全部不得补猜

2000—2010 中文站点可能涉及：

- GB2312 / GBK；
- table layout；
- frames；
- legacy JS；
- IE-specific behavior；
- popup；
- guestbook CGI；
- 免费主页广告框架；
- 外链图片；
- Flash / media；
- 登录态评论；
- 动态论坛 URL。

本轮没有取得原始 capture，因此不能根据今天的新闻截图或现代页面想象：

- “梦颖之家”长什么样；
- 西祠 SOS 的 exact thread skin；
- 2007 深圳论坛的 reply UI；
- 2010 新浪博客当日模板；
- 轻松筹 2014 第一版移动分享页。

这些一律 `unknown`。

---

## 24. Archive work in this slice

本轮对以下 locator 进行了 Web/Archive 搜索尝试：

- `go7.163.com` + `wumengying` / “梦颖之家”；
- `请阳光照亮这一片血色` + Sina Blog；
- `qingsongchou.com` 早期 2014 页面；
- 深圳新闻网“我说深圳事” + 2007 患癌女工求助。

通过当前搜索访问链，没有得到一个可以实际打开并按 METHOD 记录以下字段的 historical replay：

```text
archive_source
capture_url
original_url
capture_datetime
HTTP status
Content-Type / charset
main document
subresources
DOM/JS/session behavior
```

因此：

> **M1 = NOT ACHIEVED IN THIS SLICE**

严格含义只是：**本轮没有验证到合格 capture。**

它绝不等于：

> Wayback 没保存 / 页面当时不存在 / 无法在其他档案找到。

后续应继续尝试：

- Internet Archive CDX/Wayback；
- Common Crawl 索引；
- 搜索引擎缓存/引用；
- 同期教程、站长文、页面截图；
- ArchiveTeam 或平台遗留备份；
- 论坛 URL pattern 反推（只作为 candidate，不能直接变 historical original）。

---

## 25. 下一步 artifact hunt

优先级：

1. **2000 `go7.163.com` 免费主页**：寻找网易免费主页 host 结构、charset、广告框架和该页 candidate capture；
2. **西祠胡同 2000 SOS**：定位 board/thread ID 或同期引用；
3. **深圳新闻网 2007 “我说深圳事”**：定位 exact thread URL 和论坛模板；
4. **2008 白血病儿童博客**：定位 provider + article URL；
5. **2010 新浪博客**：定位 `请阳光照亮这一片血色` 原 blog URL、首篇文章和 2 个时间点；
6. **2014—2015 轻松筹**：寻找第一代 `微爱通道` 项目页、share card、支付入口和提现帮助文档。

每找到一个 capture，都先按 METHOD 做最小证据记录，不直接扩写叙事。

---

## 26. 本笔记改变的旧网理解

医疗求助把一个很容易被忽略的旧网事实暴露得特别清楚：

> **“网页把一个人救了”通常不是一个真实事务。**

更接近历史现场的是：

```text
有人在线下生病
→ 另一个人把这件事写进论坛
→ 陌生人看见
→ 有人做个人主页
→ 有人顶帖/转帖
→ 有人去医院
→ 有人线下捐现金
→ 有人后来通过银行/在线支付转钱
→ 家庭再拿钱进入医院
```

到 2014—2015，平台才开始把其中越来越多步骤封装到同一套账户、分享卡片和资金系统里。

因此中文旧网的价值不只是保存“早期网民的文字”，还在于它曾经是一个**把现实世界里原本彼此不认识的人临时组织起来的协调层**。而真正改变一个病人能不能继续治疗的最后几步，长期都发生在网页之外：银行账户、单位、病房、手术押金、照护者的时间和现实里的钱。