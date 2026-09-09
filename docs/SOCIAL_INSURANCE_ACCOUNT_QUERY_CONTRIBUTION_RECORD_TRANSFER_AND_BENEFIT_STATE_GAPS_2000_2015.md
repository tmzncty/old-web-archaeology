# 社保账户查询、缴费记录、关系转移、权益认定与待遇之间的状态缺口（中国，2000—2015）

> Scope：本文严格服务于 `old-web-archaeology` 的约 1995–2015 中文互联网主范围。它不是中国养老保险制度通史，也不把 2020s 全国社保平台或平台骑手保障扩成本文主对象。更长的前互联网制度背景、2008 农民工退保生活史、2019—2026 life-horizon 比较及美国 Social Security 前史见：
> https://github.com/tmzncty/how-people-lived/blob/main/topics/from-work-unit-seniority-to-portable-contribution-ledger-pension-insurance-migration-and-institutional-memory-china-1986-2026.zh-CN.md
>
> 核心考古问题：一张旧网页如果写着“养老保险个人账户查询”“单位缴费查询”“转移接续”“个人权益记录”，研究者究竟能证明到哪一层？公开查询入口、登录成功、页面显示某月缴费、单位已经申报、经办机构权威账本已经入账、跨省转移已经完成、年限最终被待遇领取地承认，以及退休时真正按此计算养老金，并不是同一个对象。

本文与仓库已有专题分工：

- 在线简历 state-gap 研究职业市场怎样读取候选人；
- 网上银行 state-gap 研究资金转账与清算；
- 公用事业账户 state-gap 研究住宅基础设施账本；
- 本文研究**普通人的工作生命怎样被社会保险 Web 入口部分显影，以及页面可见状态与权威长期权益之间的缺口。**

---

## 1. 为什么社保旧网页是一种特别危险的历史对象

公开 Web 很容易保存：

- 人社/劳动保障网站首页；
- “养老保险个人账户查询”链接；
- 身份证号/用户名输入框；
- 密码说明；
- 业务指南；
- 转移接续说明；
- 社保政策问答；
- 缴费基数和费率表；
- “查询成功”“申请成功”的前端模板。

真正决定一个人几十年后待遇的状态，却主要存在于：

- 用人单位申报系统；
- 社会保险征缴/经办数据库；
- 历史纸质档案；
- 个人权益账本；
- 地方之间的转移消息和资金关系；
- 视同缴费年限认定；
- 补缴/更正审批；
- 最终待遇核定。

因此：

`public query shell != authoritative life-course ledger`。

---

## 2. 对象模型

### 2.1 Public information site

政策、办事指南、费率、经办机构地址、热线、新闻。

可以证明服务信息被公开，不证明某项私人事务已经可在线执行。

### 2.2 Query entry

“养老保险个人账户查询”“社保个人信息查询”等入口。

可能只是：

- 表单壳；
- iframe；
- 跳转到另一个 host；
- 依赖登录密码；
- 依赖证书/控件；
- 只在特定时间开放；
- 后端已经下线的历史页面。

### 2.3 Person match

身份证号、社保编号、密码等输入以后，系统把查询请求绑定到某个参保人。

因此：

`ID field accepted != authoritative person matched`。

### 2.4 Employer declaration

用人单位向征缴/经办机构申报某人某月工资基数与参保状态。

这是 Web 个人查询页之外的另一条事务链。

### 2.5 Contribution posting

应缴、已扣、单位申报、资金实际到账、社保账本记账必须拆开。

至少有：

`employment exists`
→ `employer should insure`
→ `employer declaration`
→ `premium collection`
→ `agency posting`
→ `personal-rights record visible`。

任何一步都不能从前一步自动推出。

### 2.6 Personal rights record

经办机构对个人登记、缴费、待遇等权益信息的制度性记录。

页面显示是它的一个展示层，不是记录本体。

### 2.7 Transfer application

劳动者跨统筹地区就业后发起养老保险关系转移接续。

“提交申请”只表示一个事务开始。

### 2.8 Source-side release

原参保地核验并发送关系/信息/资金。

### 2.9 Destination receipt / merge

新参保地收到并按规则接续，缴费年限进入未来的累计计算。

因此：

`transfer application submitted != source released != destination received != entitlement merged`。

### 2.10 Benefit calculation

退休时按法律、历史缴费、视同缴费、待遇领取地等规则进行正式核定。

今天保存一张 2009 年个人账户页面，不能直接计算或证明 2026 年实际养老金。

---

## 3. 基本状态链

### 3.1 在职缴费链

`real work`
→ `formal employment relationship`
→ `social-insurance registration`
→ `employer monthly declaration`
→ `collection/payment`
→ `agency ledger posting`
→ `personal-rights record`
→ `Web display / paper statement`
→ `worker notices / does not notice`。

### 3.2 跨地区转移链

`old local record`
→ `employment moves`
→ `new local enrollment`
→ `transfer eligibility`
→ `application`
→ `source verification`
→ `source information/fund transfer`
→ `destination receipt`
→ `local merge`
→ `years accumulated`
→ `future benefit-location decision`。

### 3.3 记录纠错链

`Web/paper record shows missing month`
→ `person checks contract/pay evidence`
→ `asks employer / agency`
→ `agency investigates`
→ `supplementary declaration/payment/correction`
→ `authoritative ledger changes`
→ `display eventually refreshes`。

### 3.4 退休待遇链

`historical records`
+ `recognized deemed-contribution years`
+ `actual contribution years`
+ `personal-account information`
+ `benefit-location rules`
→ `retirement application`
→ `agency review`
→ `formal benefit decision`
→ `payment`。

---

## 4. 早期中文 Web：先保存的是“入口”，不是人的整条工作史

### 4.1 2006 上海劳动保障服务网已经是公共服务入口

上海市劳动和社会保障局 2006 年政府信息公开年报明确称，网站是政府信息公开主渠道，并在改版后形成“办事大厅”“新闻中心”“资讯服务”“互动社区”四大模块；“办事大厅”已经包含社会保险办事功能。

证据等级：**A（同时期官方年报）**。

可证明：

- 2006 年上海劳动保障 Web 公共服务存在；
- 社会保险已进入网站办事结构。

不能证明：

- 所有社保事务都可在线完成；
- 每个参保人都使用网站；
- 公开 archive 可以看到真实个人权益记录。

### 4.2 2008 年官方年报进一步确认 host 与网站规模

2008 年原上海市劳动和社会保障局年报把政府网站写为：

`http://www.12333sh.gov.cn`

并记录当年网站持续整合改版，便民服务、信息公开与在线互动具有很大访问量。

证据等级：**A（同期官方年报）**。

这给旧网考古提供了一个可靠的 host anchor。

### 4.3 同期媒体确认 12333sh.gov.cn 的服务语义

2008 年《新民晚报》同期报道把 `www.12333sh.gov.cn` 描述为“上海劳动保障网”，并称其向市民提供浏览、查询、办事、咨询、评议、投诉举报等一门式网上便民服务。

证据等级：**B+（同期高质量媒体）**。

因此至少可以建立：

`2008 public host verified by official/media evidence`。

### 4.4 2009：社保记录开始被其他人生接口直接调用

2009 年上海“居转户”网上申报上线时，同期报道明确指出，申请人可以通过 `www.12333sh.gov.cn/index.shtml` 查询在沪缴纳社会保险费情况及累计缴纳时间。

这非常关键，因为它证明 Web 社保查询不只是“看看养老账户余额”，而已经成为另一套城市身份事务的前置核验工具。

这里需要分开：

`social-insurance record exists`
与
`residence-to-household-registration application accepts that record`。

### 4.5 一个可疑但有价值的历史 endpoint locator

后来的保险资讯页面给出了上海个人社保查询历史地址：

`http://www.12333sh.gov.cn/fwdt/grxx/grxx.jsp`

并描述通过身份证号/查询密码查看缴费和记账情况。

证据等级：**C（后来二手说明）**。

这只是一个 **candidate historical locator**，不是 verified 2008/2009 capture。

本轮尝试直接打开构造的 Wayback/CDX URL时，当前 Web 访问链拒绝未经搜索结果建立 provenance 的 archive URL，因此：

**M1 verified historical replay: NOT ACHIEVED IN THIS SLICE.**

严禁写成：

- “Wayback 没保存”；
- “该 URL 当时不存在”；
- “该 endpoint 2008 年一定就是今天二手页面描述的字段”。

---

## 5. 2009—2011：关系转移把网站状态拉向跨地区事务

### 5.1 2009 年政策问题来自真实的地方记录不兼容

2008—2009 同期报道反复记录珠三角农民工因跨城市/跨省转移困难而退保。

这使旧网中的“关系转移”不是一个纯粹的政策帮助页，而是连接两套地方权威账本的高风险事务。

### 5.2 2010 起的制度目标是“关系跟人走”，不是“一个网页改个地址”

国办发〔2009〕66号要求跨省就业时基本养老保险关系能够转移接续。

对 old-Web 考古而言，至少要保留：

`browser application state`
`source-agency state`
`destination-agency state`
`fund/information transfer state`
`final accumulated record`

五层。

### 5.3 2011《社会保险法》使“查询记录”成为法定权利

《社会保险法》第四条明确个人有权查询缴费记录、个人权益记录；第十九条规定养老保险关系随本人跨统筹地区转移，缴费年限累计计算。

这意味着旧网页上的“查询”不能只理解成便民产品功能，它已经成为本人监督单位缴费和长期权益的一部分。

---

## 6. 北京：2010s Web 服务进一步把缴费月份变成本人可查看对象

### 6.1 2010 年前后北京市社会保险网上服务平台上线

2013 年的同期/近同时期服务介绍回顾称，北京市社会保险网上服务平台 2010 年初上线，最初已包含人员增减申报、个人信息查询和报表下载，之后扩展到参保记录打印、历年对账单、个人信息变更等功能。

证据等级：**B-/C+（2013 对 2010 的近时回顾）**。

### 6.2 2011 的普通 Web 痕迹

2011 年新浪博客用户在整理北京社保缴费基数时直接留下当时网上办事大厅：

`http://www.bjld.gov.cn/csibiz/home/`

并写明可以查询个人社会保险缴费情况。

证据等级：**B-/C（同期个人博客，可作为平台可观察事实的 locator，不用作政策权威解释）**。

这种个人材料对 old-Web 很有价值：

- 它证明用户实际会把官方 host 当查询入口传播；
- 它保留了今天官网重构后很容易丢失的路径形态。

但绝不能由博客文本推出：

`所有登录流程都成功`、`所有数据都实时`、`查询页就是权威账本`。

### 6.3 对账单 vs 页面

北京后来的材料显示 2010 年及以前的历史社保年度对账单仍可由网上平台查看；2011 年以后又形成更稳定的权益记录查询。

对考古而言，纸/电子对账单是一个独立 artifact：

`screen query result`
不必等于
`official printable rights statement`。

---

## 7. 十五个必须长期保留的 state gaps

### 7.1 public-query-page / authenticated-account gap

公开查询页存在，不证明任何私人账户已登录。

### 7.2 ID-input / person-match gap

输入身份证号/社保号，不证明后台成功绑定权威人员记录。

### 7.3 employer-declaration / contribution-posting gap

单位“申报了”不等于当月缴费已进入经办账本。

### 7.4 payroll-deduction / agency-receipt gap

工资条上扣了个人部分，不足以单独证明社保机构已实际收到并记账。

### 7.5 displayed-month / authoritative-ledger gap

网页显示一个缴费月份，是查询层输出；权威状态仍在经办账本。

### 7.6 display-time / posting-time gap

后台已经入账，前端可能延迟更新；前端历史缓存也可能晚于真实状态变化。

因此：

`page timestamp != contribution effective time`。

### 7.7 screen-record / legal-evidence gap

历史截图能证明曾显示什么，不自动等于可在行政/司法事务中使用的正式个人权益证明。

### 7.8 local-record / portable-record gap

一个地方能查到记录，不等于另一统筹地区已经接受这段年限。

### 7.9 transfer-application / source-release gap

申请提交，不等于原参保地完成转出。

### 7.10 source-release / destination-receipt gap

原地已发出信息，不等于新地已经接收并记入个人记录。

### 7.11 record-transfer / entitlement gap

关系转移完成，不等于退休待遇已经核定，更不等于某个养老金金额已经确定。

### 7.12 personal-account-amount / total-benefit gap

养老保险个人账户金额只是待遇计算的一部分，不能把页面中的“个人账户储存额”直接当未来可领取养老金总额。

### 7.13 continuous-display / continuous-eligibility gap

网页看到连续若干月缴费，不足以推出所有政策中的“连续资格”；具体住房、车辆、医疗等规则必须按城市、年份、险种独立验证。

### 7.14 online-record / offline-archive gap

视同缴费年限、早期工龄、历史纸档案等可能并不完整显现在早期 Web 查询层。

### 7.15 work-performed / social-insurance-record gap

最重要的一条：

`没有社保记录 != 那段人生没有劳动`。

非正规劳动、现金工、家庭照护、未参保平台劳动、单位漏缴情形都可能造成真实工作史与制度记录不重合。

---

## 8. 历史页面还会制造哪些 preservation bias

### 8.1 institutional-memory opacity：制度记忆不透明

研究者能看到查询壳，却看不到真正决定某个人一生权益的后台账本。

这不是资料搜得不够，而是隐私与系统边界本身决定的。

### 8.2 transaction-survival inversion

越接近真实个人权益的材料：

- 登录 session；
- 身份证号；
- 缴费工资；
- 单位申报；
- 转移消息；
- 补缴附件；
- 退休待遇核定

越不应该公开存档。

所以 archive 质量不能以“是否挖出了真人社保记录”衡量。

### 8.3 historical-rule rehydration

今天打开一个旧 URL，如果后端还活着，它可能返回：

- 当前费率；
- 当前登录系统；
- 当前机构名称；
- 当前办事规则。

这只能记为：

`current-backend rehydration`，

不能叫 2009 年历史回放。

### 8.4 record-correction invisibility

一个人如果发现 2008 年缺了一个月，2012 年补正，今天的最终权益记录可能只呈现“修好以后”的状态。

因此 final ledger 可能抹掉：

`error → dispute → evidence → correction`

这整个生活过程。

### 8.5 employer-side invisibility

个人查询页可能显示“已缴/未缴”，却无法保存单位当月为什么没申报、何时补报、工资基数怎样确定。

### 8.6 closed-session bias

社保系统通常要求登录并处理高敏感数据，公共 crawler 天然只能保存未登录壳层。

这使旧网考古对社会保障这种系统比新闻站、个人主页更容易“保存得像有一整套系统，实际只剩门厅”。

---

## 9. Artifact preservation ladder

### S0：只有后来回忆/二手描述

例如现代保险资讯说旧上海查询 URL 曾经是什么。

### S1：同时代文本提到网站/服务

例如 2008《新民晚报》明确写出 `www.12333sh.gov.cn` 并描述查询办事功能。

### S2：同期官方文档确认 host / 功能

例如 2008、2009 上海人社官方年报。

### S3：verified historical public capture

实际打开历史 memento，核对：

- original URL；
- capture URL；
- capture datetime；
- HTTP status；
- charset；
- title / DOM；
- form action；
- JS/CSS 依赖。

### S4：verified historical authenticated-shell behavior without private data

只在合法、无私人账号的情况下复原登录壳、控件依赖或错误路径。

不追求真人数据。

### S5：contemporaneous transaction documentation

官方手册/截图说明当时单位申报、个人查询或转移流程。

### S6：authoritative private transaction state

真实个人社保记录、申报、转移、补缴、待遇核定。

**默认不作为公开考古目标。**

---

## 10. 本轮历史 replay 尝试

### M1：`www.12333sh.gov.cn`

同期官方材料确认：**host 存在，且承担劳动保障网上公共服务。**

### M2：candidate query endpoint

后来二手材料提供：

`http://www.12333sh.gov.cn/fwdt/grxx/grxx.jsp`

当前证据等级：**locator only**。

### M3：Wayback/CDX

本轮尝试直接访问构造的 CDX / Wayback replay URL，当前访问链返回非重试型 provenance 安全限制：只能打开此前搜索结果中出现的精确 URL。

所以：

`verified historical social-insurance query capture: NOT ACHIEVED IN THIS SLICE`。

这只代表本轮工具链未取得可核验 memento。

绝不表示：

- archive 不存在；
- Wayback 未保存；
- 页面当年不存在。

---

## 11. 与普通生活史交叉以后，旧网页需要重新解释

### 11.1 一张“已缴费”页面实际上是一个人未来的碎片

它不是普通账户余额。

该月份未来可能参与：

- 养老累计；
- 医疗/失业等其他险种资格；
- 某些地方特定时期的住房、车辆、入学、积分等资格证明。

因此一个字段的法律语义随政策上下文变化。

### 11.2 “断缴”不是页面里的布尔值

研究者看到某月空白时必须继续问：

- 当月没有工作？
- 有工作但单位未参保？
- 已扣未入账？
- 系统延迟？
- 后来补缴？
- 这是一种允许中断、仍累计的养老关系？
- 还是另一个政策要求连续月份？

### 11.3 多地记录的历史重要性

一个人的生活可能跨：

`东莞 → 深圳 → 上海 → 家乡`。

早期地方查询页若分别保存，研究者不应把它们当四个人或四段互不相干的制度历史。

国家平台后来做“多地参保、集中展现”，反过来提醒旧网考古：

**同一人的制度身份曾被分散在多个地方 Web / 后台边界中。**

---

## 12. 证据等级

### A：同期官方/法律

- 2008、2009 上海劳动保障/人社政府信息公开年报；
- 国办发〔2009〕66号；
- 2010《社会保险法》；
- 1997 企业职工基本养老保险统一制度文件。

### B：同期高质量媒体

- 2008 上海劳动保障网服务介绍；
- 2009 上海居转户网上申报与社保查询；
- 2008—2010 农民工退保/转移接续报道。

### B-/C：同期个人网页

- 2011 博客中保存的北京社保网上办事大厅 URL 与个人使用提示。

可用于平台可观察事实和用户侧路径，不用于单独证明政策规则。

### C：后来二手技术说明

- 后来页面保存的旧上海个人查询 endpoint。

只能作为 archive locator 候选。

### D：本轮分析概念

`institutional-memory opacity`、`record-correction invisibility`、`local-record / portable-record gap` 等。

---

## 13. 反例与禁止性推断

### 13.1 禁止：页面有“查询”按钮 → 普通家庭普遍网上查社保

服务存在、家庭 Internet 可及、实际使用率完全不同。

### 13.2 禁止：显示“已缴” → 单位所有义务都已正确履行

工资基数、险种、月份、补缴情形仍需权威记录。

### 13.3 禁止：显示“转移申请成功” → 年限已在新地累计

至少还缺 source release 与 destination receipt。

### 13.4 禁止：个人账户余额 → 未来养老金总额

基本养老金的制度结构远比一个账户数字复杂。

### 13.5 禁止：某月空白 → 那个月没工作

这会系统性抹掉非正规劳动、照护、漏缴情形。

### 13.6 禁止：今天旧 URL 能打开 → 今天页面就是当年的页面

必须核 capture datetime、后台数据和历史前端依赖。

### 13.7 禁止：未取得 Wayback memento → Wayback 没保存

负证据必须按 METHOD 保持边界。

---

## 14. 未来可以继续做的技术考古

1. 对 `www.12333sh.gov.cn` 2006—2010 首页、便民服务与 `fwdt/grxx` 路径做真实 Wayback memento 核验。
2. 复原历史 charset、导航层级、form action、查询密码申请说明。
3. 对 `www.bjld.gov.cn/csibiz/home/` 2010—2012 做 memento 矩阵，确认个人登录页与历年对账单路径。
4. 区分单位申报系统与个人查询系统是否位于同一 host、是否使用 ActiveX/证书/JavaScript 等历史依赖。
5. 建立 2000—2015 城市样本：上海、北京、深圳、广州，比较“个人查询什么时候出现、查询到什么粒度、如何认证”。
6. 只保存公开壳层和官方测试材料，不收集、传播真人身份证号、社保号、工资基数或账户记录。

---

## 15. 本轮改变了 old-Web 的哪一点理解

此前容易把旧政务站理解成“政策从纸搬到网页”。社保查询表明，更关键的变化是：

**Web 开始给普通人一扇窗口，让他们第一次能较低成本地检查制度到底怎样记住自己。**

但 archive 最容易留下的也恰恰只是这扇窗口。

几十年以后，我们或许还能看到“请输入身份证号”“查询个人账户”“关系转移”的页面，却看不到那个劳动者真正做过的零工、单位少缴的一个月、跨省转移卡住的两个月，或者后来拿工资条去补正记录的下午。

因此社会保险旧网考古的任务，不是从网页重新制造一个人的完整制度传记，而是反过来说明：

`可见 Web 壳层`
与
`不可见但真正决定权益的制度记忆`
之间究竟隔了多少层。

---

## 16. Sources

### 同期官方与法律

- 上海市劳动和社会保障局，2006 政府信息公开年报：https://rsj.sh.gov.cn/txxgknb_17198/20200617/t0035_1372758.html
- 原上海市劳动和社会保障局，2008 政府信息公开年报：https://www.rsj.sh.gov.cn/201712333/xxgk/xxgknb/201710/t20171026_1263532.shtml
- 上海市人力资源和社会保障局，2009 政府信息公开年报：https://www.rsj.sh.gov.cn/201712333/xxgk/xxgknb/201710/t20171026_1263533.shtml
- 国务院办公厅，国办发〔2009〕66号（北京市政府存档）：https://www.beijing.gov.cn/zhengce/zhengcefagui/qtwj/201001/t20100101_781119.html
- 中国人大网，《中华人民共和国社会保险法》：https://www.npc.gov.cn/npc/c2/c10134/201905/t20190522_175815.html

### 同时代 Web / 媒体证据

- 《新民晚报》，2008“12333”网站/热线服务：https://news.sina.com.cn/o/2008-10-24/152514625131s.shtml
- 《新闻晨报》，2009“居转户”网上申报与社保累计缴费查询：https://news.sina.com.cn/c/2009-07-11/081515936211s.shtml
- 2011 新浪博客，北京市社会保险网上办事大厅 locator：https://blog.sina.com.cn/s/blog_561be372010114tn.html
- 2008 新华网转载，农民工退保与转移困难：https://business.sohu.com/20080108/n254530408.shtml

### 近同时期服务回顾

- 2013 北京市社会保险网上服务平台介绍：https://www.kaixinbao.com/zixun/shishi/2A03G20130913051.shtml

### Candidate locator（未完成历史 capture 核验）

- 后来二手材料记录上海历史个人查询路径：https://news.vobao.com/article/1077980239151088635.shtml

### Historical replay status

- 本轮 Wayback/CDX 构造 URL 被当前访问链 provenance 安全限制拒绝；没有获得 verified historical memento。
