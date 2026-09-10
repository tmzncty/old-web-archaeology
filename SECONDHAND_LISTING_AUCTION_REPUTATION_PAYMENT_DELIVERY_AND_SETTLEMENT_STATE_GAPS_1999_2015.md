# SECONDHAND_LISTING_AUCTION_REPUTATION_PAYMENT_DELIVERY_AND_SETTLEMENT_STATE_GAPS_1999_2015

> 类型：research note / transaction-state-gap package
>
> 主体 scope：约 1999–2015 中文互联网中的个人二手/闲置物交易、校园 BBS 跳蚤板、早期 C2C 拍卖/交易平台及其支付、评价、交付接口。
>
> 本文件**不是**易趣/淘宝/闲鱼通史，也不是完整 M1 case。当前证据足以建立 transaction model 与 archive-risk model，但尚未取得并核验一个满足本仓 METHOD 最低字段要求的 1999–2005 EachNet historical Memento。
>
> 生活史交叉笔记：`tmzncty/how-people-lived/topics/secondhand-goods-household-liquidity-reversible-ownership-and-informal-selling-china-1979-2026.zh-CN.md`

## 0. 为什么这个对象值得进入 old-web-archaeology

旧网中的“二手交易”不是一个页面类别，而是一组经常横跨网页、BBS、电话、线下见面、银行/邮局、快递和后来担保支付系统的事务。

它特别容易被后来的完整电商体验倒灌：今天看到一个“商品详情页”，研究者很容易自动补全“下单—在线付款—快递—确认收货—退款”。但 2000 年中国 C2C 的同期材料明确显示，网页可以只负责**把陌生买卖双方找出来**，验货、付款和交付仍在线下完成。

因此，本专题的考古单位必须从“页面是否存在”改成：

> **哪一个状态由哪一个系统权威决定，哪个页面只是在显示或建议这个状态。**

---

## 1. 开工前查重与仓库边界

本轮在两仓搜索 `二手 / 闲置 / 跳蚤 / 易趣 / marketplace / auction / classified / resale` 等组合，没有发现现成的独立二手 C2C transaction-state note。

本仓 README/ROADMAP/METHOD 的约束继续适用：

- platform / site / account / page / capture / claim 不得混写；
- exists / available / used / popular / caused 分开；
- historical locator 不是 verified capture；
- 当前服务器仍能返回一个旧 URL，不等于返回字节就是当年的历史原件；
- 浏览器、charset、脚本、表单 endpoint 未验证时必须保留 unknown；
- 私人卖家的姓名、电话、地址、聊天和交易细节实行研究必要最小化；
- 无法可靠复原是允许的正式结论。

本轮没有复制私人 listing、照片、联系电话或历史账号数据库。

---

## 2. 先拆研究单位：一个“二手商品”至少涉及 12 类对象

1. **physical item**：现实世界中那一件具体物；
2. **seller person / organization**：现实出售方；
3. **platform account**：用于发布的账号；
4. **listing record**：平台数据库中的出售信息；
5. **listing page / post URL**：用户可访问的页面表示；
6. **search/category index**：让 listing 可被发现的索引状态；
7. **offer/bid record**：报价、出价或议价状态；
8. **agreement/order record**：双方是否已经形成交易约定；
9. **payment record**：银行、邮局、平台托管或现金的资金状态；
10. **shipment/handoff record**：快递、邮寄、校园面交等交付状态；
11. **receipt/acceptance/dispute record**：收货、确认、争议、退款；
12. **reputation record**：双方交易后的评价/信用累计。

它们的生命周期并不相同。

一件货可以已经卖掉，但搜索引擎里旧 listing 仍存在；也可以 listing 已删除，但快递/支付记录仍存在；更可以页面显示“交易成功”，现实买家却从未拿到符合描述的物品。

---

## 3. 最小状态机：不能把“页面上有一件商品”写成“交易发生”

### 3.1 listing publication

```text
physical item exists
→ seller controls/possesses item
→ seller decides to offer
→ account exists
→ listing draft created
→ listing submitted
→ platform accepts
→ listing published
→ listing indexed/discoverable
→ prospective buyer actually sees it
```

必须保留：

- `item-exists / seller-authority gap`
- `draft / submitted gap`
- `submitted / published gap`
- `published / indexed gap`
- `indexed / seen gap`

### 3.2 bargaining / auction

```text
buyer sees listing
→ asks question / bids / makes offer
→ seller receives
→ seller accepts or auction closes
→ agreement exists
```

必须保留：

- `bid / winning-bid gap`
- `winning-bid / executable-sale gap`
- `chat-agreement / platform-order gap`
- `platform-order / legally-or-practically-completed-transfer gap`

### 3.3 payment

```text
payment method chosen
→ payment initiated
→ money leaves buyer control
→ bank/platform confirms receipt
→ (optional) escrow holds funds
→ release condition reached
→ seller receives spendable funds
```

必须保留：

- `payment-instruction / payment-sent gap`
- `payment-sent / payment-cleared gap`
- `escrow-funded / seller-paid gap`
- `refund-approved / refund-received gap`

### 3.4 delivery and settlement

```text
seller packs item
→ carrier/meeting handoff
→ item in transit
→ buyer obtains package/item
→ buyer inspects
→ accepts OR disputes
→ dispute resolved
→ settlement final
```

必须保留：

- `shipment-number / carrier-possession gap`
- `carrier-delivered / buyer-possession gap`
- `buyer-possession / condition-accepted gap`
- `receipt / final-price gap`
- `platform-success-label / dispute-finality gap`

所以最重要的永久边界是：

**listed != sold != paid != delivered != accepted != finally settled**。

---

## 4. 1999—2001：EachNet 证明“Web market”可以只完成匹配层

### 4.1 2000 年同期证据：网页找人，人民广场见面，现金成交

《Washington Post》2000-03-25 对上海 EachNet 的同期报道，是本轮最重要的 transaction-boundary 证据之一。

报道中的 25 岁公务员 Gao Xiaoyi 因在线下街市长期找不到自己要的对象，转向从报纸广告得知的 EachNet。更重要的是，报道明确观察：当时 EachNet 促成的交易很少跨出上海；由于支付和配送基础设施不成熟，买家常坚持亲自看货，买卖双方在人民广场、复旦大学门口等现实地点碰面，以现金完成交易。

来源：
- Clay Chandler, “Dot-Comrades Start Small,” *The Washington Post*, 2000-03-25：<https://www.washingtonpost.com/archive/business/2000/03/26/dot-comrades-start-small/949819e5-2900-452e-bb2a-d1966a57c3b2/>

证据等级：**B（同期独立媒体，含现场/用户材料）**。

它能直接否定一个后见模板：

```text
错误：1999 C2C 网站存在
   ⇒ 用户已经在网站上完成支付和物流
```

更符合证据的是：

```text
EachNet listing/search/auction layer
→ contact / agreement
→ physical meeting
→ visual inspection
→ cash handoff
```

因此 `online marketplace` 必须拆成至少：

- online discovery；
- online negotiation/auction；
- payment rail；
- delivery rail；
- dispute authority。

五层可在不同年代、不同商品、不同用户身上分步上线。

---

## 5. 2002—2004：评价与实名不是装饰，而是把本地熟人信任翻译成账号状态

### 5.1 2002 实名卖家

2002-12-23 的同期《北京晨报》报道（新浪科技当前仍保留历史 URL）记录：易趣要求卖家身份信息接受核验，同一身份证与卖家注册相关联；交易以后买卖双方评价会累积并向后来的用户展示。

来源：
- <https://tech.sina.com.cn/i/c/2002-12-23/0724157229.shtml>

证据等级：**B（同期媒体；当前稳定历史 URL，不等同于独立 WARC/Memento）**。

这一变化应建模为：

```text
real person
→ submitted identity attributes
→ verification service returns result
→ platform account receives verification state
→ public page may render badge/state
```

而不是：

`实名认证 = 所有商品真实`。

### 5.2 2003：用户已经把“实名 + 历史评分”当作陌生交易的安全线索

2003-08-18《上海青年报》经新浪保存的同期报道采访一位网名“麻辣兔头”的余女士。她把卖家实名和买卖双方评价视为自己更敢在网络环境中交易的原因。

来源：
- <https://news.sina.com.cn/c/2003-08-18/0900585147s.shtml>

证据等级：**B（同期媒体 + 同时性用户自述）**。

同一页面今天仍能观察到大量当时新浪门户 shell 的链接结构、短信、邮箱、搜索、广告等元素。但必须记录：

- 这是**新浪当前服务器对历史 URL 的当前响应**；
- 本轮没有证明当前响应字节、广告子资源、DOM 与 2003 原响应完全相同；
- 页面本身可作为“当前保存的历史正文与部分页面结构”线索，但不能替代 2003 capture metadata。

这正是 `historical-URL / historical-capture gap`。

### 5.3 企业监管材料：平台自己如何描述交易基础设施

eBay 2002 Form 10-K 披露，2002-03-17 eBay 取得 EachNet 约 38% 普通股权益，并将 EachNet 描述为面向中国个人和商业用户的在线商品/服务交易市场。文件对 eBay 自身市场的描述列出 listing、auction/fixed price、评价、安全、验证、托管/鉴定、支付和运输等配套工具。

来源：
- SEC：<https://www.sec.gov/Archives/edgar/data/1065088/000089161803001538/f88540e10vk.htm>

证据等级：**A（监管披露；平台/公司自述不等于独立效果评估）**。

2003/2004 eBay 监管披露又记录：eBay 在 2003 年 7 月完成对 EachNet 剩余股权的收购。

来源：
- eBay 2003 Form 10-K：<https://www.sec.gov/Archives/edgar/data/1065088/000089161804000676/f96707ore10vk.htm>

证据等级：**A**。

这些材料适合确认主体关系和平台自述，不适合独立确认中国用户交易成功率、欺诈率或页面体验。

---

## 6. 信用状态本身也要拆：账号信誉不是一次交易的事实

至少需要：

```text
transaction/event exists
→ platform decides event is eligible for feedback
→ rater submits feedback
→ platform accepts feedback
→ feedback is associated with target account
→ public reputation aggregate recalculated
→ next viewer sees aggregate
```

因此：

- `real transaction / feedback-eligible event gap`
- `transaction / feedback-submitted gap`
- `feedback-submitted / feedback-published gap`
- `one-account / one-person gap`
- `historical-rating / current-behavior gap`
- `account-score / this-item-quality gap`

历史页面上的“98% 好评”最多是某一时点平台按某种规则聚合出的账号状态，不能变成研究者对现实人格的结论。

如果评价规则、撤销机制、时间窗、匿名/实名规则已经丢失，数字本身的历史含义会严重缩水。

---

## 7. 2004—2010 校园 BBS：旧网二手交易经常是“信息在线、执行线下”的混合系统

### 7.1 水木 `SecondBook`：当前渲染保留历史日期，但不是历史 capture

水木社区当前移动页 `SecondBook` 仍展示：

- 2004-03-25 “出售图书者请进”；
- 2004-06-29 “求购图书者请进”；
- 2005-06-06 版面治版方针；
- 2008-11-24 关于商业行为的通告。

来源：
- <https://m.newsmth.net/board/SecondBook>

证据等级：**B/C 边界**。

理由：这些是当前服务中带历史日期的内容记录，但本轮没有验证一个 2004/2005 Memento，因此不能用当前 mobile template 反推 2004 页面布局、URL、编码、浏览器或当时实际呈现。

可直接支持的窄 claim 是：

> 当前水木系统中保存了标记为 2004—2008 的 SecondBook 板面规则/入口记录。

不可直接支持：

> 2004 年用户看到的就是当前移动页这个界面。

### 7.2 2008 广州：BBS 发帖成为毕业清仓首选，但现实宿舍承担验货和仓储

2008-07-01 广州高校同期报道中，多名毕业生正在出售离校带不走的家电、电脑、书和生活用品。受访学生把“各校 BBS 发帖”列为最优先的甩卖路径；报道同时观察到，买家根据网上信息进入学生宿舍看货，使宿管需要额外执行证件/接人管理。

来源：
- 《广州日报》经中新网/搜狐：<https://news.sohu.com/20080701/n257861290.shtml>

证据等级：**B（同期媒体，多名学生同时性自述/观察）**。

这个案例至少有五个权威域：

1. BBS authority：帖子存在、版面分类、账号状态；
2. student authority：本人是否真的拥有物品；
3. dormitory authority：买家能否进入宿舍；
4. payment authority：现金/其他支付是否真正交付；
5. physical custody：物品最终由谁拿走。

因此，archive 如果只保存 BBS post，最多证明**有人公开提出出售意图**。

### 7.3 2010 南京大学：BBS 下载审批表 + 现实跳蚤市场

南京大学 2010 年官方通知规定毕业生跳蚤市场的具体日期/时段/地点；卖家须填写审批表，审批表可以从“小百合 BBS”下载，并进行院系/保卫部门登记。现实交易又被限定为毕业生自己的学习生活用品，非毕业生和校外人员不得进入销售。

来源：
- 南京大学保卫处：<https://bwc.nju.edu.cn/1b/1c/c577a6940/page.htm>

证据等级：**A（同期高校官方页面）**。

这是一种非常清楚的 hybrid workflow：

```text
Web/BBS 获取规则和表格
→ 现实身份审核
→ 获得线下市场销售资格
→ 现场摆卖
→ 买家当面选择
→ 现场交付/结算
```

“数字化”发生在流程的一部分，不应将整条事务一律命名为 online transaction。

---

## 8. 商品状态：旧网最难保存的往往不是页面，而是“这一件东西当时到底怎么样”

二手商品和新品目录最大的差异之一是**单件异质性**。

同型号两个相机可能有不同快门次数、外观、维修史；同一本教材可能有不同笔记；同一件衣服可能有不同污渍/尺寸变化。

所以要拆：

```text
seller condition description
→ photos supplied
→ platform structured condition grade (if any)
→ buyer interpretation
→ physical item at shipment
→ physical item at receipt
→ post-receipt dispute evidence
```

至少有：

- `description / actual-condition gap`
- `photo / whole-item gap`
- `photo-time / shipment-time gap`
- `seller-grade / platform-inspection gap`
- `platform-inspection / later-damage gap`

这也是为什么二手交易历史不能只保存 listing metadata。

但隐私/版权边界又意味着：本仓不应为了“完整”而批量重新公开普通人的家庭照片、住址背景、手机号和聊天证据。

---

## 9. 2018 的后期参照：为什么早期 state model 最终需要 dispute layer

虽然本仓主体到 2015 左右，本节只作为**后期参照**，不用于倒写 2000s 功能。

2018 年同期调查记录“到手刀”等争议：买家收货后以物品状况等理由要求再次降价，卖家如果缺乏发货前状态证据会处于不利位置；另有违规 listing、骚扰、诈骗等问题。

来源：
- 中新网经人民网，2018-08-28：<https://capital.people.com.cn/n1/2018/0828/c405954-30255147.html>
- 科技日报经人民网，2018-09-11：<https://ip.people.com.cn/n1/2018/0911/c179663-30285914.html>

它提醒旧网考古：即使未来找到一个 2004 页面上写着“交易成功”，也必须问当时是否存在后续申诉/撤销/评价/退款状态，以及“成功”到底由哪个数据库字段定义。

---

## 10. Archive state model：最容易留下的是广告和 listing，最难留下的是成交事实

### 10.1 `listing-survival / settlement-loss asymmetry`

公开 listing/page 很适合 crawler：

- 标题；
- 描述；
- 图片 URL；
- 标价；
- 卖家昵称；
- 结束时间；
- 某一时点的评价数字。

而最能证明现实交易是否完成的东西往往在：

- 登录后订单页；
- 私信；
- 银行/邮政支付；
- 平台托管账本；
- 快递；
- 线下现金面交；
- 争议后台。

因此可能出现：

> **archive 保存了一座巨大的“待售商品城市”，却保存不了其中绝大多数东西最后是否真的换过主人。**

### 10.2 `public-intent / private-authority inversion`

网页上最公开的是“我想卖”；真正权威的“钱到了”“货到了”“退款完成”反而属于私人事务状态。

历史研究伦理也要求后者不能因为技术上可恢复就被批量公开。

### 10.3 `dead-listing / live-item gap`

listing 失效不等于实物消失。一件 2005 年卖掉的相机可能 2026 年仍在第三个主人手里；反过来，listing 页面可能幸存，而实物早已报废。

这类对象的 material history 与 Web history 必须分开。

### 10.4 `search-index / marketplace-database gap`

搜索引擎捕获到一个 listing URL，不等于当时平台内搜索也能找到它；平台搜索排序、类别索引、过期隐藏、反作弊都可能与公开 URL 存在不同生命周期。

---

## 11. 页面技术/浏览器条件：目前哪些可以说，哪些不能说

### 已证实

- 2003 新浪当前历史 URL 能返回同期报道正文，并带有大量门户链接、搜索/短信/邮箱/广告等页面 shell 元素；
- 2010 南京大学官方历史 URL 当前能返回公告正文和审批附件链接；
- 当前水木移动页能显示标记为 2004—2008 的 SecondBook 历史置顶/版规记录。

### 高概率但本轮不升级为事实

- 1999—2004 C2C/BBS 页面会依赖当时常见桌面浏览器环境；
- 部分交易流程可能依赖 cookie/session、登录后表单和动态 URL；
- auction closing / reputation aggregate / account pages 很可能由后台数据库动态生成。

这些只是工程上合理的假设，当前均为 **D / unverified**。

### 不知道

对 `www.eachnet.com` 1999—2004 的目标 workflow，目前仍不知道：

- verified capture URL；
- capture datetime；
- historical HTTP status；
- Content-Type / charset；
- DOM/layout；
- 是否 frameset/table；
- JavaScript requirements；
- cookie/session requirements；
- 图片/CSS/JS 子资源完整度；
- listing/search/auction/reputation 页面 URL pattern；
- 支付/评价动作是否跨 host；
- 当年具体浏览器兼容条件。

**不得根据“2000s 中文网站一般如此”补成事实。**

---

## 12. 本轮 archive 尝试与负结果

本轮检索了 `eachnet.com` / `www.eachnet.com` 与 2000—2005、易趣、Wayback 等组合，并尝试从公开 Web 建立 Internet Archive capture locator。

公开搜索没有返回一个可直接打开、可按本仓 METHOD 核验的 1999—2005 EachNet Memento。随后尝试直接构造 Internet Archive CDX 查询 URL，当前研究访问链拒绝打开未由既有搜索结果建立 provenance 的构造 archive URL。

所以本轮只能记录：

> **M1 verified historical EachNet marketplace/listing Memento: NOT ACHIEVED IN THIS SLICE.**

这**不等于**：

- Wayback 没有保存 EachNet；
- 2000 年 EachNet 没有网页；
- archive 中不存在任何相关子页面。

下一轮若要升级，应该先取得可验证的 exact capture locator，再逐项记录：

`archive_source / capture_url / original_url / capture_datetime / replay status / charset / DOM / login state / subresources`。

---

## 13. Historical locator ledger

| Object | Historical locator / current evidence URL | Period supported | Evidence | What it proves | What it does NOT prove |
|---|---|---:|---|---|---|
| EachNet | `www.eachnet.com` | 1999–2004 | B + A corporate | 同期存在面向个人交易的 C2C marketplace；2002/03 eBay 股权关系 | 未核验历史页面形态 |
| EachNet user workflow | Washington Post 2000 | 2000 | B | Web 匹配后常同城看货、现金面交 | 全部用户/全部商品都如此 |
| 易趣实名/评价 | Sina historical URL | 2002 | B | 卖家身份核验与评价机制被同期报道 | 实名保证商品真实性 |
| 易趣信任体验 | Sina historical URL | 2003 | B | 至少一名用户把实名/评价当交易安全线索 | 全国用户普遍如此 |
| 水木 SecondBook | current `m.newsmth.net` rendering | labels 2004–2008 | B/C boundary | 当前系统保留这些历史日期/标题 | 2004 真实 UI/HTML |
| 广州校园 BBS 二手 | Sohu/Guangzhou Daily | 2008 | B | 学生把 BBS 发帖用于毕业清仓，验货/仓储仍在宿舍 | 具体 BBS 页面结构 |
| 小百合 BBS + 线下跳蚤市场 | 南京大学官方页 | 2010 | A | 表格可从 BBS 下载，销售资格与交易场所在现实校园 | BBS 交易已在线支付/交付 |

---

## 14. Evidence grades

### A — 原始/同时代机构材料

1. eBay 2002 Form 10-K；
2. eBay 2003 Form 10-K；
3. 南京大学 2010 跳蚤市场官方公告；
4. 1998《旧货流通管理办法（试行）》可作为 Web 前后制度边界的补充背景（不作为旧网页 capture）。

### B — 近同时代独立材料

1. Washington Post 2000 EachNet 现场报道；
2. 北京晨报/新浪 2002 易趣实名；
3. 上海青年报/新浪 2003 网络交易信用；
4. 广州日报/搜狐 2008 校园毕业清仓。

### C — 后来回忆/后期整理

本轮尽量不依赖怀旧文章来确定旧网页技术。北京日报 2025 的信托商店回顾只用于 how-people-lived 的前互联网物质基线，不用于 EachNet 页面复原。

### D — 研究者模型

本文件所有 state-gap 名称、authority split 和 archive asymmetry 均为研究模型，必须继续用更多实际 capture/transaction manuals 验证。

---

## 15. 关键 state-gap 清单

### Object / authority

- `physical-item / listing-record gap`
- `seller-possession / seller-authority gap`
- `person / platform-account gap`
- `account-verified / listing-truth gap`

### Publication / discovery

- `draft / submitted gap`
- `submitted / published gap`
- `published / indexed gap`
- `indexed / seen gap`
- `historical-search-result / platform-search-state gap`

### Price / auction

- `asking-price / clearing-price gap`
- `bid / winning-bid gap`
- `winning-bid / executable-sale gap`
- `auction-closed / payment-completed gap`

### Reputation

- `transaction / feedback-submitted gap`
- `feedback-submitted / published gap`
- `account-score / this-listing-quality gap`
- `historical-score / current-person-behavior gap`

### Payment

- `agreement / payment-initiation gap`
- `payment-initiation / cleared-funds gap`
- `escrow-funded / seller-paid gap`
- `refund-approved / refund-received gap`

### Delivery

- `tracking-number / carrier-custody gap`
- `carrier-delivered / buyer-possession gap`
- `buyer-possession / buyer-acceptance gap`
- `receipt / settlement-final gap`

### Item condition

- `description / actual-condition gap`
- `photo / whole-item gap`
- `photo-time / shipment-time gap`
- `condition-at-shipment / condition-at-receipt gap`

### Hybrid old-Web workflow

- `BBS-post / physical-sale gap`
- `online-contact / offline-meeting gap`
- `online-agreement / cash-handoff gap`
- `downloaded-form / offline-approval gap`

### Archive

- `historical-URL / historical-capture gap`
- `listing-survival / settlement-loss gap`
- `public-intent / private-authority gap`
- `dead-listing / live-item gap`
- `current-rendering / historical-template gap`
- `main-document / transaction-backend gap`

---

## 16. 与 how-people-lived 的交叉解释

old-web 不应该把用户行为简化成“易趣打败谁/淘宝打败谁”的公司竞争故事。真正与普通生活相连的是：

- 一件宿舍里的旧风扇能否找到下届学生；
- 一台相机能否从陌生人手里重新流动；
- 一个准备搬走的人是否必须把全部家当一起带走；
- 网页负责哪一步，现实地点负责哪一步；
- 身份和信誉怎样让陌生交易半径扩大；
- 为什么交易越完整，越关键的证据反而越不适合公开 archive。

这也是本仓和生活史仓的分工：

- **old-web** 保存页面/平台/状态/浏览器/档案边界；
- **how-people-lived** 解释这些技术变化怎样改变毕业、迁移、家庭预算、兴趣尝试和非正规劳动。

---

## 17. Hindsight risks

1. 不把 `C2C website exists` 写成 `end-to-end e-commerce exists`。
2. 不把 `platform says transaction completed` 自动写成现实物权/收货没有争议。
3. 不把 `real-name account` 写成 `authentic item`。
4. 不把 `BBS post` 写成 `online payment`。
5. 不把当前水木 mobile 页面写成 2004 UI。
6. 不把当前 Sina 对 2003 URL 的响应写成已核验 2003 WARC。
7. 不用后来的淘宝/闲鱼 workflow 倒推 1999 EachNet。
8. 不从一个留存 listing 推断该商品当年一定卖出。
9. 不因 archive 缺少订单/私信推断用户没交易；这些状态本来就可能是 private/authenticated。
10. 不批量复活普通卖家的联系方式、住址、家庭背景照片或聊天记录。

---

## 18. What we know / infer / do not know

### 已证实

- 2000 年 EachNet 同期使用案例中，Web 匹配与线下验货/现金交付可以并存；
- 2002—2003 易趣已经把身份核验和评价作为陌生人交易的信用基础设施；
- 2008 广州高校毕业生使用校园 BBS 发布二手信息，现实宿舍仍承担仓储/看货；
- 2010 南京大学明确存在“小百合 BBS 下载表格 + 现实审批 + 实体跳蚤市场”的混合链；
- 交易平台的公开页面状态不能独立证明支付、交付、收货和争议已经完成。

### 可以合理推断，但需要更强 capture/手册才能升级

- 早期 C2C 的动态 listing、auction、account、reputation 很可能严重依赖后台数据库与 session；
- 这类页面比静态新闻/帮助页更难被高保真长期保存；
- 订单、私信、支付和争议历史具有系统性 archive invisibility。

### 不知道

- 1999—2004 EachNet exact HTML/charset/browser/plugin requirements；
- 早期 EachNet listing/search/auction URL patterns；
- 某个具体时点平台内 search 与公网搜索引擎的覆盖差异；
- 早期 transaction 的同城面交/邮寄比例；
- 评价修改、删除、争议对 aggregate 的精确规则；
- 2004—2015 不同平台从 listing 到 payment/delivery 的具体迁移时间链，需要逐平台另做 case。

---

## 19. 下一步最有价值的 M1 升级路径

不要再堆十篇平台兴衰回顾。真正有价值的是拿到一套**可以复核的历史 transaction surface**：

1. 一个 2000—2004 EachNet homepage/category/listing capture；
2. 同一时期一个 search/result 或 auction/listing page；
3. 一个官方 help/manual，解释 bid/transaction/reputation/payment workflow；
4. 第二历史时点（例如 2003/2004）；
5. 完整记录 original URL、capture URL、datetime、HTTP、charset、DOM、subresources；
6. 若能安全取得，再做 old browser replay；
7. 明确哪些 transaction state 永远只能由私有后台决定，不能靠 public archive 复原。

如果只拿到 locator 而无法实际 replay，应继续保持 research note，不升级 M1 complete case。

---

## 20. 本轮结论

二手交易是一个非常适合提醒旧网研究者“网页不是现实事务”的案例。

1999—2000 年的 Web 已经足以让陌生人手里的一件物品变得可寻址，但用户仍可能必须在同一座城市见面、看货、付现金；2002—2003 年平台开始让身份和历史评价跟着账号走；校园 BBS 又证明，数字信息层可以和极其传统的宿舍验货、纸质审批、实体摊位长期共存。

因此最应保存的历史不是一张“古早电商首页”截图，而是这条边界：

**Web 先改变了谁能找到谁；支付、物流、信誉、争议和现实物品随后才一层层追上。**

而 archive 最容易保存的，恰好是“有人想卖什么”；最难、也最不应该公开重建的，是“这个具体人最终把钱给了谁、货到了哪里、双方后来为什么吵起来”。

这不是证据不足的偶然，而是事务型旧网的结构性保存偏差。

---

## Sources

1. Washington Post, 2000 EachNet contemporary report: <https://www.washingtonpost.com/archive/business/2000/03/26/dot-comrades-start-small/949819e5-2900-452e-bb2a-d1966a57c3b2/>
2. Sina/Beijing Morning Post, 2002 EachNet identity verification: <https://tech.sina.com.cn/i/c/2002-12-23/0724157229.shtml>
3. Sina/Shanghai Youth Daily, 2003 online-trading trust: <https://news.sina.com.cn/c/2003-08-18/0900585147s.shtml>
4. eBay Inc. 2002 Form 10-K: <https://www.sec.gov/Archives/edgar/data/1065088/000089161803001538/f88540e10vk.htm>
5. eBay Inc. 2003 Form 10-K: <https://www.sec.gov/Archives/edgar/data/1065088/000089161804000676/f96707ore10vk.htm>
6. Guangzhou Daily / Sohu, 2008 graduate resale/BBS workflow: <https://news.sohu.com/20080701/n257861290.shtml>
7. Nanjing University, 2010 graduate flea-market notice: <https://bwc.nju.edu.cn/1b/1c/c577a6940/page.htm>
8. Waterwood current SecondBook rendering: <https://m.newsmth.net/board/SecondBook>
9. 1998 Used Goods Circulation Rules (institutional background): <https://www.hengqin.gov.cn/lab/flfg/bmgz/content/post_3727256.html>
10. 2018 later-period dispute reference: <https://capital.people.com.cn/n1/2018/0828/c405954-30255147.html>
11. 2018 later-period platform-rights reference: <https://ip.people.com.cn/n1/2018/0911/c179663-30285914.html>

---

*Initial research synthesis AI-assisted. No private listing archive or personal contact dataset was copied into this repository.*