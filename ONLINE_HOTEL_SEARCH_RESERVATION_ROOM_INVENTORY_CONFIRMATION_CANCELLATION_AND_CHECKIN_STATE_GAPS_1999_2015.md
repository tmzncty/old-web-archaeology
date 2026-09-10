# Online Hotel Search, Reservation, Room Inventory, Confirmation, Cancellation and Check-in State Gaps（中国中文 Web，1999—2015）

> **范围声明**：本文只研究约 1999—2015 中文互联网里的酒店/住宿搜索与预订接口及其历史可见性。1960s Holidex、1980s 北京住宿短缺、2020s 退改与长住酒店只作为边界比较，主体仍留在本仓的中文旧网 scope。

交叉生活史研究见：

- `tmzncty/how-people-lived/topics/temporary-lodging-hotel-booking-mobility-buffers-and-reversible-stays-china-1980-2026.zh-CN.md`

本文不回答“旅游业发展得多快”，而回答一个更窄的 old-Web 问题：

> **当历史网页显示“酒店、价格、可订、预订成功”时，我们究竟能证明哪一层状态？**

---

## 1. 开工查重与研究边界

本仓已有：

- 电商下单/配送；
- 餐馆目录/评分/到店；
- 铁路票务；
- 网上银行；
- 地图与路径规划；
- 房屋租赁、求职、身份、投诉等事务 state-gap。

酒店预订与普通电商不同的关键在于：

1. **库存天然带日期**：卖的是某晚的 room-night，不是长期库存物品；
2. **同一房间可以有多个 rate plan**：价格与取消规则绑定；
3. **OTA 可能没有最终房间分配权**：有些订单只是 request，需要酒店再次确认；
4. **完成态发生在线下**：真正完成不是“页面显示成功”，而是人到店、身份通过、酒店分房并入住；
5. **历史网页最容易保存的是壳，最难保存的是真实库存和履约事实。**

所以本文不能被 `ECOMMERCE_CHECKOUT...` 吞并。

---

## 2. 研究单位

按本仓 `docs/METHOD.md`，不把 platform/site/page/account/capture/claim 混在一起。

本专题至少区分：

### Platform

例如携程、艺龙、去哪儿等在线旅行服务平台。

### Site / host

例如 2003 年 SEC 文件明确确认的：

- `www.ctrip.com`
- 当时英文站 `www.gotochina.com`

### Page / interface

可能包括：

- destination guide；
- hotel search result；
- hotel detail；
- room/rate result；
- booking form；
- confirmation page；
- help/cancellation policy；
- member order page。

### Transaction state

真正的 reservation / supplier confirmation / payment / cancellation / check-in。

### Capture

某个 archive 保存的历史页面表示。

### Claim

例如：

> “2003 年携程公司披露其中文网站可以让客户查看酒店价格和可用性，并预订酒店。”

这是公司原始监管文件可支持的 claim。

而：

> “某个 2003 年 8 月 16 日普通用户在网页看到的 288 元房价当时真的可售并最终入住。”

则完全需要另一套事务证据，不能由 SEC 文件或今天的 archive shell 推出。

---

## 3. 核心状态机

### 3.1 Discovery state

```text
hotel exists in physical world
→ hotel is known to OTA
→ hotel has a listing
→ listing appears for a destination/query
→ user can reach listing
```

边界：

```text
real hotel != platform listing
platform listing != search visibility
search visibility != current operation
```

### 3.2 Inventory state

```text
hotel listing
→ date selected
→ room type selected
→ rate plan selected
→ room-night appears available
```

边界：

```text
hotel has rooms
!= requested date has inventory
!= requested room type has inventory
!= requested rate plan has inventory
```

### 3.3 Reservation state

```text
user inquiry
→ booking request
→ OTA accepts input
→ instant confirm OR supplier request pending
→ supplier confirmation
→ customer notified
```

### 3.4 Financial / guarantee state

```text
reservation confirmed
→ guarantee/prepay required?
→ payment/credit-card guarantee succeeds
→ cancellation/refund rules attach
```

### 3.5 Physical fulfillment state

```text
reservation exists
→ guest arrives
→ name/ID/guest conditions verified
→ front desk/PMS locates reservation
→ room is assigned
→ key/card issued
→ actual stay
```

因此至少需要长期保存以下硬边界：

```text
search result != inventory
inventory display != booking request
booking request != reservation confirmation
OTA confirmation != hotel operational recognition
reservation confirmation != payment/guarantee
payment != refundable
reservation != check-in
check-in != actual completed stay
```

---

## 4. 2003 携程 SEC 文件：罕见的原始交易状态说明

携程 2004 年 Form 20-F 对 2003 年酒店预订流程给出了非常适合 old-Web 考古的原始系统说明。

来源：

- **A（公司原始监管文件，证明公司当时如何正式披露自己的系统；不能单独证明任一用户订单）**：Ctrip.com International, Ltd., Form 20-F, filed 2004: <https://www.sec.gov/Archives/edgar/data/1269238/000119312504084450/d20f.htm>

文件把典型酒店交易分成三步。

### 4.1 Inquiry

客户可以：

- 在网站搜索；
- 或拨打客服中心；

来了解目的地酒店。

这已经说明：

```text
web interface
```

和：

```text
human call-center interface
```

共享的是同一个旅行服务系统，而不是两个互斥时代。

### 4.2 Reservation

客户通过网站或电话选择酒店，携程替客户建立 reservation。

但这一状态仍不是最终确认。

### 4.3 Confirmation 分成两种供应关系

SEC 文件明确区分：

#### guaranteed allotment

携程拥有保证配额时，可以给客户即时确认，再通知酒店。

#### on-request

如果是 request 模式：

```text
客户提出请求
→ 携程把请求交给酒店
→ 酒店确认
→ 携程再通过电话 / email / SMS 告知客户
```

因此：

## booking-request / supplier-confirmation gap

是 2000s 酒店 Web 最关键的事务边界之一。

即使我们未来取得一张历史页面，上面出现：

> “您的预订申请已提交”

也不能把它复原成：

> “房间已确认”。

---

## 5. 2003：网站已经能查价与“availability”，但大多数交易仍由人操作数字后台

同一 Form 20-F 披露：

- 2003 年总交易中，约 70% 经客服中心执行，约 30% 经网站执行；
- 当时约 800 名客服代表；
- 客服代表会代表客户访问内部信息系统，查看酒店、价格、可用性并执行预订；
- 中文网站 `www.ctrip.com` 的 booking software 与网站集成，可以查看酒店/航班价格和可用性并预订；
- 网站同时提供目的地指南、用户游记/图片、公告板、旅伴与旅行建议等内容。

这形成一个本仓非常值得长期使用的概念：

## human-mediated Web-era backend

早期“在线旅游”可以是：

```text
用户不碰 Web
→ 打 800 电话
→ 客服操作联网数据库
→ 客服代查库存/价格
→ 建单
→ 供应商/后台处理
→ 电话/SMS/邮件回传结果
```

所以以后研究旧网 adoption 时必须区分：

```text
platform is digitally networked
!= final user operates a browser
```

这也说明仅统计历史网站 PV，无法还原整个平台的数字化事务量。

---

## 6. 2009：电话中心仍约占 2/3 交易

携程 2010 年 Form 20-F（2009 财年）继续披露：

- 2009 年约 2/3 交易通过客服中心、约 1/3 通过网站；
- 这一结构与 2008 年大体一致；
- 客服中心 24×7 运行；
- 客服可提供实时酒店、航班与度假信息并进行预订；
- 网站也能在数分钟内完成 booking；
- 参与其 electronic confirmation system 的酒店可通过在线接口收取并确认客户 reservation 信息。

来源：

- **A（公司原始监管文件）**：Ctrip.com International, Ltd., Form 20-F, fiscal year 2009: <https://www.sec.gov/Archives/edgar/data/1269238/000095012310008368/c95193e20vf.htm>

这再次固定：

## website-share / digital-system-share gap

如果 2009 年网站只占约 1/3 交易，不能反推出“只有 1/3 交易数字化”。

因为客服中心本身也在高度依赖数字系统。

反过来也不能说：

> “携程是互联网公司，所以普通客户已经普遍自助下单。”

两种说法都把 front-end 与 backend 混了。

---

## 7. 一份 2007 同期用户材料：Web discovery 与电话 booking 可以属于同一个人

2007 年《深圳特区报》报道中的苏小姐，在科技园公司工作。她说：

- 休闲旅行会先上携程看目的地指南；
- 比较酒店；
- 再预订机票和酒店；
- 出差时也会用 800 电话。

来源：

- **B（同期媒体第一人称；文章具有明显企业宣传色彩，只用于支持窄操作事实）**：<https://news.sohu.com/20070419/n249535319.shtml>

这不是独立验证携程市场份额的材料。

但它非常适合证明：

```text
same user
→ Web for search/comparison
→ phone for another transaction context
```

因此不要设计一个虚假断代：

```text
电话时代结束
→ Web 时代开始
```

真实旧网更像多通道叠加。

---

## 8. 搜索结果页为什么是危险史料：room-night 是瞬时数据库状态

对普通旧网页，可以问：

> 2004 年 6 月 1 日这个页面是否存在？

对酒店搜索页还必须问：

> 页面里的“有房/价格”究竟针对哪一天、哪一房型、哪一 rate plan、哪一库存快照？

因此新增：

## room-night / page-time gap

历史 capture 时间例如：

```text
capture_datetime = 2006-05-10 11:03
```

页面查询条件可能是：

```text
check-in = 2006-06-01
check-out = 2006-06-02
```

这两个时间必须分开。

如果 archive rewrite 丢了 query string、cookie、POST body 或 session，现代回放甚至可能得到：

- 默认今天日期；
- 空结果；
- 错误页；
- 登录页；
- 一个由今天后端重新生成的房价。

这些都不能当成历史库存。

---

## 9. rate plan 不是“同一间房的一个价格标签”

同一房型可能同时存在：

```text
可免费取消价
不可取消价
会员价
预付价
到店付价
含早餐价
不含早餐价
促销价
```

因此新增：

## room-type / rate-plan gap

以及：

## quoted-price / executable-price gap

历史网页里出现“￥298 起”最多证明：

- 在某一页面状态里出现过这个数字；

不能自动证明：

- 任意日期都 298；
- 任意用户都能买；
- 税费/服务费已包含；
- 当时仍有库存；
- 订单最终以 298 成交。

---

## 10. 2011 求职旅社与去哪儿：平台 listing 可以收录非标准住宿形态

2011 年《新民晚报》报道上海求职旅社时明确写到，记者在 `Qunar.com` 查询到多家上海求职旅社及多人间/包间价格。

来源：

- **B（同期媒体）**：新民晚报/新浪，2011-03-04，《“求职旅社”最近有点闹猛》：<https://news.sina.com.cn/o/2011-03-04/153722053692.shtml>

这条材料对 old-Web 的意义不是证明去哪儿库存绝对准确，而是：

> 到 2011 年，中文在线旅行搜索的对象已经不只是标准星级酒店，也能把求职旅社这种夹在青年旅舍、群租和过渡住房之间的空间变成可查询 listing。

因此平台 taxonomy 本身可能影响：

- 什么住宿被看见；
- 它被归到什么类别；
- 什么价格粒度可比较。

需要新增：

## lodging-category / real-use gap

同一个现实住宿空间可以同时具有：

- 旅馆；
- 青年旅舍；
- 求职旅社；
- 床位；
- 群租；
- 月租过渡空间；

不同社会和监管含义。

平台把它归为一个“酒店/住宿 listing”，不能抹掉这些差异。

---

## 11. 酒店确认页与真实到店之间还有一整套不可见系统

即使得到历史 confirmation page，也只到这里：

```text
OTA says confirmed
```

但真实到店还可能依赖：

- OTA 与 hotel supplier 的同步；
- 酒店 PMS；
- guest name；
- 身份证/护照；
- 同住人登记；
- 押金；
- 到店时间；
- no-show 规则；
- overbooking 处理；
- 酒店当日实际营业状态。

因此新增：

## OTA-confirmation / hotel-PMS-recognition gap

和：

## reservation / check-in gap

old-Web 页面考古尤其容易高估前台网页的权威性，因为真正决定能否给房卡的后台通常根本不公开。

---

## 12. 身份是另一条状态轴：booking principal != checked-in guest

酒店预订里至少还要区分：

```text
account holder
booker
payer
named guest
actual arriving person
registered occupants
```

这些可以是同一个人，也可以不是。

所以：

```text
account authenticated
!= guest identity accepted at hotel
```

这与本仓居民身份证研究有交叉，但本文不扩写证件史。

只保留：

## booking-identity / occupancy-identity gap

历史平台页面显示“订单属于某账号”不能证明最终入住者就是账号本人。

---

## 13. 取消是一个状态机，不是页面上的一个形容词

取消至少要拆成：

```text
cancellation policy displayed
→ policy attached to selected rate plan
→ cancellation requested before/after deadline
→ OTA receives request
→ supplier accepts/rejects
→ penalty calculated
→ refund initiated
→ payment channel settles refund
→ customer actually receives money
```

因此：

```text
“免费取消”标签
!= current order is still within free window

cancel request submitted
!= reservation released

refund approved
!= money received
```

2000s—2015 历史页面若只保存“可免费取消”，还必须知道：

- 这个标签属于哪一房型/价型；
- 截止时间用哪一时区；
- 是否后来修改订单；
- 确认邮件/短信是否给出不同条款；
- 页面是否由动态脚本按今天状态重绘。

---

## 14. 2015 是一个合理的本仓边界，而不是“手机时代以后都不重要”

到 2015，移动 OTA、移动支付和定位已经深度改变酒店预订，但本仓的核心仍是约 1995—2015 中文旧 Web。

2015 以后更适合作为**解释旧状态机为什么重要**的对照，而不是继续无限拉长本文主体。

例如 2020 疫情暴露：

```text
预订页面中的取消窗口
```

可以在七个月后的现实计划变化时产生巨大后果。

2025 的“不可取消”纠纷又说明：

```text
digital booking convenience != future reversibility
```

这些后来的材料帮助我们理解：为什么 2000s 的 rate plan / confirmation / cancellation policy 不能只当 UI 装饰。

但它们不属于本文主要旧网证据期。

---

## 15. 旧网保存中最危险的几类“假历史”

### 15.1 current backend rehydration

历史 URL 被 archive 保存，但动态请求今天重新命中现代 API，出现现代库存/价格。

结论：

> capture shell 可以是历史的，里面的 inventory 不一定是历史的。

### 15.2 session loss

历史搜索依赖 cookie、session 或 POST 参数；archive 只保存 GET shell。

现代回放时看见“请选择日期”，不能倒推历史用户没有搜索结果。

### 15.3 rewritten query string

archive rewrite 可能破坏：

- hotel ID；
- check-in/out；
- city ID；
- campaign parameter；
- rate parameter。

### 15.4 AJAX/XHR missing

主 HTML 保存，房型库存接口没保存。

因此：

```text
page captured != inventory captured
```

### 15.5 login wall surviving better than account state

会员订单页可能只留下登录壳。

这不能证明：

- 用户没有订单；
- 订单不存在；
- 当时登录失败。

### 15.6 call-center completion invisibility

2003/2009 大量交易通过电话执行。

即使 Web archive 完美，仍然会系统性漏掉：

> **大量依赖同一数字后台、但没有由最终用户通过公开网页完成的事务。**

这是本专题对 archive bias 的最重要补充。

---

## 16. 新增 state gaps 清单

### 现实对象与平台

- `physical-hotel / platform-listing gap`
- `platform-listing / current-operation gap`
- `lodging-category / real-use gap`

### 时间与库存

- `hotel / room-night gap`
- `room-night / page-time gap`
- `room-type / rate-plan gap`
- `cached-availability / executable-inventory gap`
- `quoted-price / executable-price gap`

### 预订

- `inquiry / booking-request gap`
- `booking-request / OTA-acceptance gap`
- `booking-request / supplier-confirmation gap`
- `instant-confirm / on-request gap`
- `customer-notification / authoritative-supplier-state gap`

### 金融与退改

- `reservation-confirmed / guarantee-completed gap`
- `prepayment / refundability gap`
- `cancellation-label / order-policy gap`
- `cancel-request / inventory-release gap`
- `refund-approved / funds-received gap`

### 入住

- `OTA-confirmation / hotel-PMS-recognition gap`
- `booking-identity / occupancy-identity gap`
- `reservation / check-in gap`
- `check-in / completed-stay gap`

### 历史保存

- `historical-shell / historical-inventory gap`
- `captured-listing / captured-transaction-state gap`
- `public-Web / call-center-transaction gap`
- `static-guide / volatile-room-night gap`
- `public-booking-interface / private-stay-record gap`

---

## 17. 证据表

| Evidence | Grade | 支持什么 | 不支持什么 |
|---|---|---|---|
| Ctrip 2004 Form 20-F（2003 业务） | A | `www.ctrip.com` 存在、网站与客服中心功能、70/30 交易结构、询问/预订/供应商确认流程 | 任一具体用户或任一历史房价真实成交 |
| Ctrip 2010 Form 20-F（2009 业务） | A | 2009 约 2/3 call center、1/3 website；24×7；electronic supplier confirmation | 全国 OTA 用户结构、所有酒店均实时确认 |
| 2007 苏小姐同期采访 | B | 同一用户可 Web 比较+预订，也可出差打电话 | 全国普及率；文章宣传中的市场份额 |
| 2011 求职旅社同期报道 | B | Qunar 被记者用于查询求职旅社及床位价；非标准过渡住宿被平台化 | 当时每条 listing 实时有效；全上海覆盖 |
| 1965 Holidex / 1973 法院记录 | A/B+（边界比较） | 酒店数字库存/集中预订早于 Web，且可由机构中介操作 | 中国旧网具体实现 |
| 2020/2025 取消纠纷 | B（边界比较） | 取消条款是一种未来承诺状态，不是 UI 装饰 | 2000s 同一平台具体规则 |

---

## 18. 已证实 / 高概率 / 不知道

### 已证实

1. 携程 2003 已同时以中文 Web 与 24 小时客服中心提供酒店搜索/预订。
2. 2003 公司披露交易执行约 70% 在客服中心、30% 在网站。
3. 2003 酒店确认至少存在 guaranteed allotment 与 on-request 两类不同路径。
4. on-request 路径里，客户提出预订后仍需酒店供应商确认。
5. 2009 公司披露交易仍约 2/3 通过客服中心，网站约 1/3。
6. 2009 已有酒店供应商使用 electronic confirmation interface 的公司披露。
7. 2011 同期媒体确实使用 Qunar 查询上海求职旅社 listing/价格。

### 高概率，但本轮不升级为 A

1. 2000s 携程酒店搜索/详情页大量内容由数据库动态生成；
2. 房型/库存/价格接口可能依赖 session、query、脚本或后台请求；
3. 不同年份页面可能有明显 IE/编码/JS 环境差异。

这些都符合当时技术常识，但没有历史 capture/原始前端资源就不得写成确定历史。

### 不知道

1. 1999—2002 `www.ctrip.com` 具体酒店搜索 URL pattern；
2. 2003 主站页面真实 charset、DOM、CSS/frameset 形态；
3. 2003 booking 是否依赖特定 IE/JS/cookie 设置；
4. 某一历史日期实际房晚库存与平台数据库更新延迟；
5. 酒店 supplier interface 的具体协议/前端；
6. 用户订单确认页的完整字段与历史 URL；
7. 2011 Qunar 求职旅社页面的具体 historical URL/capture；
8. 艺龙、芒果、去哪儿在同年代的确认状态机是否与携程一致。

---

## 19. Archive 检查结果与负证据合同

本轮以 `www.ctrip.com` 为核心 historical locator，尝试通过公开 Web 搜索寻找 2003—2007 的 Internet Archive/Wayback 可验证结果，并尝试搜索：

- `site:web.archive.org/web/2004 ctrip.com`
- `site:web.archive.org/web/2003 www.ctrip.com`
- `site:web.archive.org "www.ctrip.com" "2004"`

当前搜索没有返回可直接打开并核验的历史 memento。

因此本轮只能记录：

```text
M1 verified historical Ctrip hotel-search/booking Memento:
NOT ACHIEVED IN THIS SLICE
```

这**不等于**：

```text
Wayback 没有保存
```

也不等于：

```text
当时页面不存在
```

可能原因包括：

- 搜索引擎不索引 Wayback URL；
- 需要在 Internet Archive UI/CDX 内进一步定位；
- 动态路径/query 没有被当前公开搜索发现；
- 页面存在但子资源/库存接口缺失；
- robots 或 session 条件影响可见性。

按 `docs/METHOD.md`，locator 未实际打开并核验 capture datetime、HTTP 状态、original URL、主文档/子资源时，不能升级为 archive evidence。

---

## 20. 浏览器 / 编码 / 插件假设

本轮**没有**得到足够历史 capture，因此保持：

```text
charset: unknown
browser requirement: unknown
IE-only behavior: unknown
frameset/table layout: unknown
Java/ActiveX/Flash dependency: unknown
cookie/session requirement: partially likely, not verified
AJAX/XHR dependency: unknown for 2003; later years need separate evidence
viewport: unknown
```

不能因为“2003 中国网站常见 GB2312/IE6”就自动填上。

每一个 future capture 都需要单独测。

---

## 21. 后见之明风险

### 风险 A：把 Web adoption 写得太快

SEC 原始材料已经直接反驳：2003、2009 多数交易仍由电话客服执行。

### 风险 B：把“在线旅游公司”理解成“交易全在线”

数字后台可以由客服替用户操作。

### 风险 C：把“可用”标签当作历史事实

房晚库存高度动态，而且可能是 cache 或 supplier request。

### 风险 D：把今天 Ctrip 页面结构倒写到 2003

绝对禁止。

### 风险 E：把 confirmation 当作入住

公司甚至以酒店确认真实入住作为收入确认节点之一，这恰好说明 reservation 与 stay 是不同状态。

### 风险 F：只研究标准酒店

2011 求职旅社材料提醒：平台也可能收录介于旅舍、床位、群租与过渡住房之间的空间。

### 风险 G：只保存页面，不保存渠道关系

2000s OTA 的历史如果没有 call center，就会被 archive 系统性误写。

---

## 22. 一个新的 archive-bias 概念：transactional invisibility by successful mediation

本轮建议把以下概念保留到未来 METHOD/Gap Model：

## transactional invisibility by successful mediation（成功中介造成的事务不可见）

逻辑是：

```text
后台高度数字化
+ 客服替用户操作
+ 用户只打电话
= 真实数字事务没有公开网页痕迹
```

这和“没有数字化”完全不同。

携程 2003/2009 的交易渠道数据给了一个罕见可量化锚点：

> 大量 digital backend usage 在 Web archive 中天然不可见。

因此旧网研究不能只用“用户公开网页留下多少事务页面”估计数字服务渗透。

---

## 23. 第二个 archive-bias：static-guide / volatile-inventory asymmetry

目的地指南、酒店介绍、图片、旅游文章可能很容易被 crawler 保存。

房晚库存却依赖：

- 日期；
- room type；
- rate plan；
- supplier allotment；
- session；
- 价格；
- cancellation policy；
- 用户资格。

所以未来 archive 极可能呈现：

```text
“某家酒店介绍得非常完整”
```

却完全无法回答：

```text
“2006-10-03 当晚一个普通用户到底能不能以 268 元订到它”
```

这不是偶然缺页，而是动态事务系统的结构性保存偏差。

---

## 24. 与 How People Lived 的接口

old-Web 侧只做：

- 中文平台；
- 页面/渠道；
- hotel listing；
- room-night inventory；
- request/confirm；
- cancel/refund；
- archive gap；
- browser/charset unknowns。

生活史侧负责回答：

- 为什么一张临时床能让异地求职成为可执行路径；
- 为什么毕业和就业之间可以插入短旅行；
- 为什么小时房可以成为城市家庭成员购买独处的空间；
- 为什么长住酒店能让实习生推迟签一年租约；
- 为什么“免费取消”代表未来可撤回性。

这样不会把本仓扩成全球住宿史。

---

## 25. 下一步最值得推进

1. 在 Internet Archive UI/CDX 直接定位 1999—2005 `www.ctrip.com` 的历史时点；
2. 一旦有 memento，严格记录：original URL、capture URL、datetime、HTTP、charset、重定向、子资源；
3. 优先寻找 **hotel search result / booking help / confirmation help**，而不是只找首页；
4. 检查 ArchiveTeam/Common Crawl 是否存在 Ctrip/eLong/Qunar 的可用 WARC/索引；
5. 找 2003—2009 用户教程，验证真实浏览器操作、cookie/JS/登录需求；
6. 找到至少一个“request pending → hotel confirmed → SMS/email”用户侧同时代 artifact；
7. 找一个 2011 左右 Qunar 求职旅社具体 historical listing，测试平台 taxonomy 与现实住宿类别关系；
8. 获得 capture 后再进入 IE6/modern browser 对照，不提前猜历史页面外观。

---

## 26. 本轮对 old-Web 方法论真正增加了什么

以前我们已经知道：

```text
page exists != transaction succeeded
```

酒店案例把这句话推进了一层：

> **有些数字事务甚至在成功发生时，也不一定让最终用户访问一个公开网页。**

2003 和 2009 的携程可以同时满足：

```text
用户只打电话
```

和：

```text
订单高度依赖联网数据库、实时库存、数字客服系统和供应商确认接口
```

所以旧网考古不能把“Web 页面史”等同于“Internet 进入普通生活的全部历史”。

对这个仓库尤其重要，因为用户要求我们研究的正是 1995—2015 中文旧 Web；**越把 scope 守得严，越必须明确指出 scope 外但与页面同一事务链上的电话、短信、后台和实体前台，否则 Web 会把自己在历史中的位置夸大。**
