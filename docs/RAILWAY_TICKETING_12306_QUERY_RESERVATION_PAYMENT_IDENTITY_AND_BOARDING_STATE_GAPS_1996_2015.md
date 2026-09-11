# 铁路客票、12306 查询、预约、支付、实名与乘车状态缺口（中文 Web，1996—2015）

## 0. 研究边界

本 note 研究约 1996—2015 年中文 Web 中与铁路客票有关的公开页面、购票入口、帮助文档、用户教程和事务状态，以及这些页面与电话订票、铁路内部联网售票、纸票、实名核验和真实乘车之间的边界。

1996 年铁路客票发售和预订系统建设属于必要前史，因为它解释 2011 年 `www.12306.cn` 为什么能够在公共 Internet 上暴露全国车次、余票和订单能力；但本仓不把中国铁路内部计算机网络史整体前移成 old-web 主对象。

跨时期普通生活、迁移、春运、返乡与“一个人在未来某天能否真正回家”的长线比较写在：

- `tmzncty/how-people-lived/topics/from-ticket-window-queues-to-pre-reservation-railway-ticketing-mobility-slots-and-return-home-optionality-china-1986-2026.zh-CN.md`

本 note 只回答：**当普通人通过中文 Web 查询和购买铁路客票时，一个页面或订单究竟证明了什么；哪些真正决定“这人后来有没有坐上那趟车”的状态，公共 Web archive 几乎天然看不见。**

---

## 1. 先拆对象：一个“12306 买票”至少包含二十个不同实体/状态

研究时必须分开：

1. **physical passenger / 现实中的乘车人**；
2. **purchaser/operator / 实际操作网站的人**；
3. **railway operator / 铁路运输与票额管理主体**；
4. **platform/site/host / 公共购票网站与主机**；
5. **Web account / 网站账号**；
6. **account identity / 账号实名状态**；
7. **passenger identity record / 乘车人身份记录**；
8. **train/service / 具体列车**；
9. **origin-destination segment / 出发—到达区间**；
10. **seat class / 席别**；
11. **inventory snapshot / 某一瞬间返回的余票状态**；
12. **query request / 查询请求**；
13. **booking/order request / 订票请求**；
14. **temporary seat lock / 临时席位锁定**；
15. **payment request / 支付请求**；
16. **bank/payment-side confirmation / 银行侧支付结果**；
17. **railway-side order confirmation / 铁路侧订单确认**；
18. **ticket issuance / 出票状态**；
19. **paper ticket / 纸质客票**；
20. **electronic order/credential / 电子订单或可用于乘车的电子状态**；
21. **pickup/exchange / 到站换票/取票**；
22. **identity verification / 实名核验**；
23. **gate check / 闸机/检票状态**；
24. **actual boarding / 实际上车**；
25. **refund/change request / 退票、改签请求**；
26. **refund settlement / 退款到账**。

因此必须长期保留下面的状态差：

`site exists`
`!= online ticketing is available for this train/date`
`!= query request reaches live inventory`
`!= displayed inventory is still current`
`!= user account is valid`
`!= passenger identity is accepted`
`!= booking request submitted`
`!= seat temporarily locked`
`!= payment completed`
`!= railway order confirmed`
`!= ticket issued`
`!= passenger possesses a usable boarding credential`
`!= paper ticket no longer required at this station`
`!= passenger passes real-name verification`
`!= passenger reaches the gate in time`
`!= passenger actually boards`
`!= trip is completed`
`!= refund request completed`
`!= refund money has returned`。

这套拆分直接沿用本仓 `docs/METHOD.md` 的原则：platform、site、account、page、capture 和 claim 不得混成一个对象。

---

## 2. 1996：铁路内部联网是 Web 购票的前史，不是公共 Internet 购票本身

1996 年 12 月《人民日报》报道铁路部门加快计算机售票网络建设，目标是在两年内实现全国联网，使旅客可以在一个购票窗口购买不同方向和车次的车票；北京站、北京西站等已经使用计算机售票软件和软纸客票。

来源：
- 《人民日报》1996-12-20，第 5 版数字转录：https://cn.govopendata.com/renminribao/1996/12/20/5/

**证据等级：A/B+。** 同时代新华社/人民日报报道的后续数字转录，可证明当时建设目标与北京部分实施情况；不能把“计划两年全国联网”直接写成“1998 所有窗口已完成”。

2012 年铁科院对 12306 的公开释疑进一步说明，铁路客票发售和预订系统从 1996 年开始建设，此后先后完成计算机售票、区域联网、全国联网、清分清算、席位复用、实名与电子支付等功能。

来源：
- 中国网络电视台，2012-01-13，《12306互联网购票系统释疑》：https://jingji.cntv.cn/20120113/115500.shtml

**证据等级：A/B+。** 铁科院系统建设口径的同期公开说明。

这里必须避免一个 old-Web 常见误写：

> “1996 年铁路联网，所以普通旅客 1996 年已经可以上网买票。”

这是错误跳跃。

更准确的状态是：

`railway internal computerized inventory exists`
`→ station windows can query/sell a wider inventory`
`→ passenger still interacts mainly with window/telephone/agency`
`→ public Internet purchase appears later`。

也就是说，**记录先在铁路机构内部跑起来，浏览器只是多年以后才成为普通人的直接入口。**

---

## 3. 2008 电话订票作为控制组：remote transaction 早于 Web，但“订到”仍不等于“拿到票”

广铁 2008 年春运电话订票是研究 12306 的一个重要控制组。同年报道记录，旅客可通过电话预约若干天后的车票；预约成功以后，必须在规定时间前到指定地点取票，逾期则自动取消。另有报道显示，大量已经电话预约成功的票最终并未按时领取。

来源：
- 《南方都市报》/新浪，2008-01-14：https://news.sina.com.cn/c/2008-01-14/020113252059s.shtml
- 《信息时报》/搜狐，2008-01-20：https://news.sohu.com/20080120/n254766540.shtml

**证据等级：B。** 同期媒体报道。

因此电话订票必须拆成：

`phone connected`
`→ passenger/request matched`
`→ temporary reservation created`
`→ pickup deadline generated`
`→ passenger reaches pickup point`
`→ physical ticket issued`
`→ passenger boards`。

这对 old-Web 很重要，因为它证明：

**remote reservation != Web reservation**，而且 **remote reservation != transaction completed**。

如果后来的网页考古只看“预约成功”页面，会低估线下取票、身份核验、时间窗口等事务尾巴。

---

## 4. 2011：`www.12306.cn` 首次把查询、锁位、支付和订单放到公共 Web 上

### 4.1 exact historical original host

2011 年京津城际 Internet 售票的同期报道明确留下：

- `http://www.12306.cn/` / `www.12306.cn`

用户需要在站点实名注册，查询日期、车次、席别和余票，然后提交订单并在限定时间内通过网银完成支付。

来源：
- 《东方早报》/搜狐，2011-06-13：https://sh.sohu.com/20110613/n280679313.shtml
- 《燕赵都市报》/新浪，2011-09-30：https://news.sina.com.cn/o/2011-09-30/070023242267.shtml
- 福州新闻网，2011-09-29：https://news.fznews.com.cn/jsxx/2011-9-29/2011929XRE2RGW9OO154816.shtml

**证据等级：B。** 同期记者实测和铁路部门信息，可证明历史 host、用户流程与当时部分线路/车站的取票规则；不是 DOM/服务器实现的一手 artifact。

### 4.2 Web 事务链至少有五个关键断点

同期报道显示，典型流程可拆为：

1. 注册/登录；
2. 查询车次与余票；
3. 选择列车/席别并提交订单；
4. 系统在短时间内暂时锁定席位；
5. 用户在约 15 分钟内完成网银支付；
6. 铁路订单状态确认；
7. 视车站条件直接刷二代身份证进站，或到窗口换取纸票。

因此：

`inventory displayed != seat locked`

`seat locked != payment completed`

`bank says payment sent != railway order necessarily confirmed`

`order confirmed != paperless boarding supported`

`online order != passenger actually travelled`。

这些状态差是研究动态事务页时最重要的证据边界。

### 4.3 account owner 不一定等于 passenger

2011 年福州等地的购票说明已经允许一个账号为其他乘车人购买客票，只要录入相应实名信息。

这意味着：

`Web account owner != passenger`

`keyboard operator != passenger`

`payment cardholder != passenger`。

以后如果恢复到某个账号操作页面，也不能从一次 purchase event 自动推断账号主人就是最终乘车人。

---

## 5. 2011 的客户端条件：Internet 可及不等于 transaction 可执行

《新京报》2011 年 6 月对 12306 的实际测试记录，在当时的 Chrome、Firefox、Safari、Opera 等环境里出现乱码、无法登录或不受信任连接，客服称网站主要支持 IE6 及以上；同年其他购票报道还要求用户安装站点根证书，并具备可在线支付的银行卡/网银。

来源：
- 《新京报》/新浪，2011-06-15：https://news.sina.com.cn/c/2011-06-15/084622643844.shtml
- 《新闻晚报》/新浪，2011-09-22：https://news.sina.com.cn/c/2011-09-22/143823199664.shtml

**证据等级：B。** 同期记者实测与客服口径。

这里可以确认的窄 claim 是：

- 2011 年部分 12306 事务对浏览器兼容性较敏感；
- 同期媒体明确报告 IE6+ 支持口径；
- 根证书/SSL 信任问题会影响用户操作；
- 在线支付能力属于事务链的一部分。

不能从这些材料进一步推出：

- 2011 全年所有 12306 页面都 IE-only；
- 所有页面使用同一种 JS/ActiveX；
- 某个服务器框架、charset 或浏览器嗅探实现已经确定。

没有 historical capture/HTML 的部分必须保持 UNKNOWN。

### 5.1 一个 B 级 candidate locator：`dynamic.12306.cn/otsweb/main.jsp`

2012 年流传的用户购票指南中出现过：

- `https://dynamic.12306.cn/otsweb/main.jsp`

作为当时直接进入购票/登录界面的链接，并同时提到根证书、在线银行控件与夜间系统维护。

来源：
- 2012 年用户教程的后续转载：https://www.cncn.com/article/56422/

**证据等级：B-/candidate locator。** 用户操作说明可证明“当时有人以此 URL 指导操作”，不能单独证明页面完整历史形态、生命周期、后端部署结构或每个日期都有效。

本 note 将它登记为 **candidate historical original URL**，等待 archive capture 核验；不把它提升为 M1 artifact。

---

## 6. public shell / live inventory：铁路客票 Web 的核心保存不对称

铁路购票站最容易被误解的地方，是把一个保存下来的 HTML 表单当成“当时的购票能力已经被保存”。

实际上至少存在以下不对称。

### 6.1 `query-form survival / live-inventory loss`

Archive 可能保存：

- 出发地输入框；
- 到达地输入框；
- 日期选择；
- 查询按钮；
- 席别图例。

但真正的票额是瞬时后台状态：

`2012-01-10 09:00 某车次是否还有 3 张硬卧`

通常不会由公开 Web archive 稳定保存。

因此：

`query page captured != inventory state captured`。

### 6.2 `inventory-snapshot / transaction-race gap`

即使某次截图/抓包看到“有票”，下一秒也可能已经被其他请求锁定。

因此：

`displayed “有票” != this user can still purchase it`。

这是动态库存系统和普通内容页最根本的差别之一。

### 6.3 `public-help survival / private-order loss`

帮助页、新闻稿、操作指南和购票入口适合公开抓取；真实订单则包含：

- 姓名；
- 身份证件；
- 手机号；
- 行程；
- 银行支付；
- 订单号；
- 退改记录。

这些从设计上就不应该成为公共 archive 的普通历史 artifact。

所以二十年后的研究者往往会看到“怎么买”，却看不到“这个普通人那天到底买没买成”。

### 6.4 `railway-site / bank-side gap`

在线购票跨过铁路网站与银行支付系统。

Archive 即便保存 railway-side 页面，也不会自动保存同一用户的银行侧支付状态；反过来银行扣款记录也不能单独证明铁路端成功出票。

因此必须长期保留：

`bank debit != railway ticket issued`。

### 6.5 `order / boarding gap`

一个人买到票以后仍可能：

- 没去；
- 误车；
- 改签；
- 退票；
- 身份证件核验失败；
- 因天气或列车原因未成行。

所以 `ticket order exists != actual mobility occurred`。

这对 how-people-lived 尤其重要：历史研究不能因为看到一个订票记录就把它写成“这个人回家了”。

---

## 7. Web archive 会系统性高估浏览器，低估电话、代售点和实体窗口

2008 的电话订票已经说明，在公共 Web 成为主渠道以前，旅客完全可能通过电话取得远程预约能力；同时市区代售点、车站窗口、单位团体票和旅行社长期共存。

因此存在 **Web survival / non-Web channel invisibility asymmetry**：

- 网站帮助页很容易留下；
- 一通电话几乎不会进入 public Web archive；
- 代售点窗口屏幕不会被 Wayback 抓；
- 单位团购、亲友代买、线下排队很少留下结构化事务记录。

如果未来只根据残存网页重建 2008—2012 购票史，很容易把浏览器写得比实际日常更重要。

应始终保留：

`Web existed != Web was dominant channel`。

---

## 8. 2012—2015：网站越重要，故障、性能与“民间攻略”越成为历史对象

12306 在 2012 春运进入大规模高并发后，大量媒体、博客、论坛和技术社区开始讨论登录、排队、验证码、浏览器、直达 URL、刷新方式和所谓“抢票技巧”。

这些材料对 old-Web 很珍贵，但证据等级要拆开：

- 官方/铁科院说明可以证明系统公开承认的架构、容量或规则；
- 同期记者实测可以证明某个时点用户看到的现象；
- 用户教程可以证明当时流传什么 workaround；
- 论坛猜测“某 URL 绕过排队”“某节点更快”只能证明用户这样相信，不能自动证明后端机制确实如此。

因此：

`folk workaround circulated != workaround technically bypassed official queue`。

这里尤其需要避免把今天熟悉的现代 CDN、微服务、JS SPA 架构术语倒投进 2012，除非有当时文档/抓包/代码证据。

---

## 9. 原始 URL 与 M1 capture 状态

### 9.1 当前已经得到的 historical original locators

本轮可确认的历史入口包括：

- `http://www.12306.cn/` / `www.12306.cn` —— 2011 同期媒体明确用于铁路 Internet 售票；
- `https://dynamic.12306.cn/otsweb/main.jsp` —— 2012 用户教程留下的 candidate direct-login/transaction locator。

### 9.2 M1：本轮仍未取得合格 historical capture

本轮继续尝试公开 archive 定位，但没有取得一份**实际打开并同时核验**以下字段的完整事务 artifact：

- `archive_source`；
- `capture_url`；
- `original_url`；
- `capture_datetime`；
- replay/HTTP 状态；
- `Content-Type` / charset；
- 主文档 DOM；
- form action；
- login/session boundary；
- historical script/subresource；
- live query/booking request shape；
- 第二历史时点用于比较。

因此本轮状态严格记录为：

> **M1 verified historical Chinese railway/12306 transaction capture: NOT ACHIEVED IN THIS SLICE.**

这不等于“Wayback 没有保存”。

按照 `docs/METHOD.md`，搜索到 locator 或知道历史 URL，都不能替代 actual capture inspection。

### 9.3 当前可以确认/不能确认的客户端条件

**可以确认：**

- 2011 同期记者曾报告 IE6+ 支持口径；
- 同期存在根证书/信任问题；
- 在线银行/支付环境属于购票链的一部分；
- 某些车站仍需要换纸票，另一些已能刷二代身份证。

**仍然不知道：**

- 2011 某一具体日期首页与交易页的 charset；
- 具体 DOM、frameset/table layout；
- 是否/何处使用 ActiveX；
- JS/browser-sniffing 细节；
- 2011—2015 同一 host 页面架构如何逐版本变化；
- 动态余票接口在 archive rewrite 下能否可靠复现。

这些未知不得由现代浏览器回放或年代印象补全。

---

## 10. 隐私与伦理边界

铁路交易数据天然涉及普通人的高敏感行程信息。

未来即便获得历史页面/缓存，也不应为了“完整复原”重新公开：

- 乘车人姓名；
- 身份证号/证件号；
- 手机号码；
- 具体订单号；
- 银行/支付信息；
- 普通个人完整历史出行轨迹。

如果研究账号—乘车人—操作人关系，应优先使用：

- 官方帮助页；
- 媒体公开测试账号的抽象流程；
- 自己的 reconstruction；
- 已匿名化的状态模型。

不要把 archive 可访问误当成可以重新传播私人行程。

---

## 11. Claim table

| Claim | Evidence | Grade | Confidence | Limit |
|---|---|---:|---|---|
| 1996 铁路正在建设全国计算机售票网络 | 《人民日报》同期报道 | A/B+ | high | 计划目标不等于所有站完成 |
| 1996 起客票发售预订系统逐步演化至全国联网/实名/电子支付 | 铁科院 2012 公开释疑 | A/B+ | high | 属机构自述建设史 |
| 2008 广铁可电话订票，成功后仍需限时取票 | 同期媒体 | B | high | 地区性案例 |
| 2011 `www.12306.cn` 已用于 Internet 售票 | 多家同期媒体 | B | high | 仍缺 actual historical capture |
| 2011 订单需短时支付，部分站需纸票、部分支持刷证 | 同期记者/铁路说明 | B | high | 线路/站点差异 |
| 2011 同期存在 IE/证书兼容问题 | 《新京报》等实测 | B | medium-high | 不能外推所有页面/日期 |
| `dynamic.12306.cn/otsweb/main.jsp` 被 2012 用户教程用作购票入口 | 用户教程转载 | B- | medium | candidate locator，非 M1 |
| public archive 很难证明实时余票和私人订单最终状态 | 系统性质 + METHOD 推理 | D | high | 属研究方法结论，不是单一历史事实 |

---

## 12. 本轮新增的 archive/state-gap 模型

### `query-form survival / live-inventory loss`

表单能活，某一秒的余票活不下来。

### `inventory-snapshot / transaction-race gap`

看见“有票”不等于轮到你提交时仍有票。

### `public-guidance / private-order asymmetry`

公开教程能保存，私人订单天然不可公开。

### `account / operator / passenger ambiguity`

账号主人、键盘操作人、付款人和最终乘客可能是不同人。

### `railway-side / bank-side settlement gap`

银行扣款和铁路出票必须分别证明。

### `online-order / boarding gap`

订单存在不能证明实际移动发生。

### `Web survival / telephone invisibility bias`

Web archive 会系统性高估网页渠道，低估电话、代售点和实体窗口。

### `historical-rendering / modern-replay gap`

现代浏览器今天能打开某个页面，不证明 2011 年用户也能以相同方式完成事务。

---

## 13. 下一步

### M1 优先目标

优先实际打开并核验：

1. `www.12306.cn` 2011 年 6—12 月的首页/注册/查询 artifact；
2. `dynamic.12306.cn/otsweb/main.jsp` 2011—2012 capture；
3. 同期根证书下载页；
4. 用户帮助/支付银行列表；
5. 一份含 charset、DOM/form action 和历史 JS 子资源的事务页面；
6. 第二历史时点（例如 2012 或 2013）用于比较页面和流程变化。

### 如果 M1 成功，建议记录

- original/capture URL；
- datetime；
- charset；
- title/viewport/frameset；
- form action；
- method GET/POST；
- cookies/session observable boundary；
- browser-specific JS/CSS；
- certificate-related resource；
- query endpoint 是否能被 archive 安全回放；
- 子资源缺失；
- modern replay 与 historical-browser assumption 的区别。

### 生活史交叉线

旧网侧一旦恢复了 2011—2013 事务页面，应回链 how-people-lived 的问题：

> **Internet 到底减少了返乡中的哪一种劳动——去窗口的身体移动、等待、信息不确定、支付，还是纸票本身？哪些劳动只是被重新分配到浏览器、网银、验证码和服务器队列？**

---

## 14. 本轮结论

12306 很容易被后来的记忆压缩成一句“以前排队买票，后来网上买票”。从 old-Web 的角度看，这个叙事过于平滑。

在 public Web 出现以前，铁路内部计算机网络、电话订票、市区售票和代售已经在减少“必须去总站窗口”的劳动；2011 年以后，浏览器进一步把**实时查询、临时锁位、在线支付和订单**放到普通人的电脑前。但这同时新增了一整套此前不存在的事务状态：账号实名、浏览器兼容、根证书、网银、短时支付、订单确认、纸票兑换和实名检票。

因此真正的技术变化不是：

> `offline → online`

而是：

> `身体去寻找票额`
> `→ 铁路内部记录先联网`
> `→ 旅客通过电话/窗口远程调用这套记录`
> `→ 公共 Web 让旅客自己查询、锁位和支付`
> `→ 真实移动仍必须经过身份、车站和列车`。

而从 archive 角度，最需要警惕的是：**我们最容易保存下来的恰恰是“怎样点”的网页，最难保存的是“那一秒到底有没有票”和“这个人后来到底有没有上车”。**

---

## AI-assisted research note

本稿初稿由 AI 协助整理。历史技术条件只写到现有同时代证据能够支持的程度；未取得 actual capture 的 URL 仅登记为 locator，不把现代回放、论坛猜测或后来的印象冒充历史原件。