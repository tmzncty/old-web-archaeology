# CINEMA_SHOWTIME_ONLINE_TICKETING_SEAT_INVENTORY_REDEMPTION_AND_REFUND_STATE_GAPS_2000_2015.md

## Scope

本研究包只处理约 2000—2015 中文 Web 中与电影院影讯、在线购票、团购券、在线选座、支付、兑换码、自助取票和退改相关的状态边界。

它**不是**中国电影产业史，也不是全球电影票务史。1989 Moviefone 等海外前史只在对应 `how-people-lived` 生活史文件中作为比较；2020 后疫情与 2023—2026 退改签争议也主要留在生活史仓。

交叉文件：

- `tmzncty/how-people-lived/topics/cinema-showtimes-online-ticketing-seat-selection-and-reversible-leisure-china-1980-2026.zh-CN.md`

本仓只问：

> 当一个 2005、2010 或 2014 年的中文网页声称“电影票可查询/可预订/可选座”时，研究者究竟能从页面证明哪一层状态？哪些真正决定观众能不能坐进影厅的状态存在于影院售票系统、支付系统、短信、自助机和私人订单中，而不是 Web 页面本身？

---

## 1. Research unit decomposition

按仓库 `docs/METHOD.md`，禁止把“电影票网站”当成单一对象。至少拆成：

```text
platform
site/host
cinema record
film record
screen/auditorium
showtime
seat map schema
seat inventory snapshot
seat hold
offer/fare/price rule
coupon/voucher
order
payment transaction
ticket entitlement
SMS redemption code / QR / ticket number
kiosk redemption
paper ticket
admission scan/tear
actual screening
refund/change request
seat release
money return
```

这些对象可以属于不同主体：

- 影片/发行方决定上映与部分价格规则；
- 影院/院线决定真实影厅、排片和本地库存；
- 影院票务软件维护 seat inventory；
- 第三方平台展示并尝试锁定库存；
- 银行/第三方支付完成资金状态；
- SMS 网关发送兑换码；
- 自助取票机把数字权利转换为纸票；
- 影院检票系统决定最终入场；
- 平台、影院和支付方共同参与退款结算。

所以任何历史页面都必须先说明它只是其中哪一层。

---

## 2. 核心 state gaps

### G01 — film-page / real-release gap

一个影片页面存在，不代表该片在当前城市、当前影院、当前日期真实上映。

```text
film metadata exists
!= local theatrical release
```

### G02 — cinema-directory / operating-cinema gap

目录里有影院记录，不代表当日仍营业，也不代表该影院已接入在线售票。

### G03 — published-showtime / executable-showtime gap

网页显示一场 `19:20`，不代表影院后台此刻仍执行该场次。

排片可能因：

- 临时调整；
- 设备故障；
- 包场；
- 片方/院线调整；
- 数据同步延迟；

而改变。

### G04 — schedule-source / platform-cache gap

平台排片可以由影院系统接口、人工录入、批量导入或缓存获得。除非有证据，不应假定“页面刷新一次 = 影院实时状态”。

### G05 — seat-map geometry / seat-inventory gap

页面能画出 H8，并不意味着 H8 当前可售。

```text
seat exists in auditorium map
!= seat available for this showtime
```

### G06 — available-render / lock-acquired gap

用户看到绿色座位到点击它之间，其他用户可能已先锁定。

```text
rendered available
!= lock acquired
```

### G07 — seat-selected / seat-held gap

前端高亮一个座位，不代表服务器已经为该订单保留它。

### G08 — seat-held / payment-success gap

许多系统会用短时 seat hold 避免重复出售。支付超时后 seat 可能释放。

因此：

```text
selected/held
!= sold
```

### G09 — payment-success / ticket-entitlement-issued gap

支付渠道返回成功与票务系统完成出票之间可能存在异步失败。

### G10 — order-created / order-paid gap

历史截图里的订单页必须区分“待支付”和“已支付”。

### G11 — voucher-purchased / showtime-reserved gap

2010—2012 大量“在线电影票”其实是团购兑换券：

```text
voucher purchased
!= film chosen
!= showtime chosen
!= seat assigned
```

### G12 — voucher-price / final-price gap

团购券到影院后可能遇到特殊影片、IMAX/3D、节假日或片方最低票价等补差规则。

### G13 — coupon-valid / cinema-accepts-today gap

页面写可用影院/期限不代表某日某特殊场次一定接受。

### G14 — ticket-code-generated / SMS-delivered gap

出票成功后，兑换码经短信发送；SMS 网关延迟或手机号错误都可能导致用户没有收到。

### G15 — code-delivered / code-redeemable gap

收到短信并不自动证明影院自助机能识别它。

### G16 — redeemable-code / paper-ticket-issued gap

取票机离线、缺纸、故障或影院端状态不一致，都可能使数字凭证无法立即转换为纸票。

### G17 — paper-ticket / admission gap

纸票已打印仍可能因：

- 走错影院；
- 走错日期；
- 迟到；
- 票已被异常核销；
- 场次取消；

而不能完成观影。

### G18 — admission / screening-completed gap

观众入场不代表放映最终顺利完成；设备故障、停电等可以在放映过程中触发退票或补偿。

### G19 — platform-account / moviegoer gap

一个账号可以为情侣、家庭、同事购买多张票；购票账号数不能直接当观影人数。

### G20 — ticket-count / unique-person gap

同一人可重复购票；出票数也不是独立用户数。

### G21 — online-order / online-only-workflow gap

“网上买票”可能仍依赖：

- 短信；
- 影院取票机；
- 纸质票；
- 线下补差；
- 人工客服。

禁止把它倒写成今日二维码直接进场。

### G22 — mobile-app / pure-mobile-authority gap

2012—2015 App 可以只是前端入口，真实 inventory 和 order authority 仍在影院/第三方后台。

### G23 — refund-supported / this-order-refundable gap

平台或影院“支持退票”不等于所有：

- 影片；
- 场次；
- 特价票；
- 团购券；
- 时间窗口；

都适用。

### G24 — refund-requested / seat-released gap

用户提出退票以后，影院库存何时重新开放给别人，是另一状态。

### G25 — seat-released / money-returned gap

座位重新可售也不代表资金已回到银行卡/支付账户。

### G26 — platform-rule / cinema-rule gap

第三方平台、影院、院线、票务系统可以分别拥有规则。2018 以后争议虽然超出本文件主体年代，却提醒研究 2010s 早期流程时必须检查究竟谁掌握退票 authority。

### G27 — asking/show-price / actually-paid-price gap

页面标价可能受：

- 会员卡；
- 团购；
- 银行优惠；
- 平台补贴；
- 服务费；
- 兑换券；

改变。历史页面上的“60 元”不自动等于观众实际支付 60 元。

### G28 — online-ticket-share / population-adoption gap

线上出票占比高，不意味着同等比例人口使用。高频影迷和多张订单会重复计入交易。

### G29 — listing-page / actual-transaction gap

搜索引擎或 archive 保存一个售票页，只证明公开页面存在，不能证明当天有人成功完成订单。

### G30 — archived-showtime / historical-seat-state gap

这是一条 archive-specific gap：即使 2012 年某排片页被完整保存，crawler 抓到的也只是某一次 HTTP 响应，而不是整场销售过程的动态库存时间序列。

---

## 3. 中文旧网时间线：只写目前有证据支撑的窄结论

### 3.1 2001：同期媒体仍保存“到影院再比较具体场次与票价”的流程

2001-08-12《每日新报》转载页面记录，一家人在影院现场问到晚场与特晚场票价以后才决定选择更便宜的场次。

它不能证明当时没有任何网上售票；它只证明**现场排片牌/售票窗口仍真实承担普通用户的决策入口。**

- Grade: B
- Confidence: high for this individual workflow
- URL: https://ent.sina.com.cn/m/f/2001-08-12/53522.html

### 3.2 2005：高票价与现场售票仍是重要生活条件

2005 年“周二半价”同期报道采访上海观众，显示票价、同行人数与影院小食共同进入观影预算。

这不是 Web 证据，但它提供了理解后来团购/票补的生活基线：网络票务的 adoption 不只由技术便利驱动，价格折扣也可能是关键。

- Grade: B
- URL: https://news.sina.cn/sa/2005-07-08/detail-ikkntiam4034042.d.html

### 3.3 2008：大型门户已经把“每日影讯/订票信息”列为固定 Web 导航类别

新浪娱乐 2008-06-15 的日期化历史页面当前仍可访问，导航中明确出现“每日影讯”“演出资讯”“订票信息”。

这可以证明 2008 年中文 Web 的大型娱乐门户已经把电影/演出时刻与订票信息作为可点击的日常信息类型。

但该 surviving page **不能**直接证明：

- 某一个“订票信息”链接一定支持交易；
- 用户能在线锁座；
- 所有城市都覆盖；
- 页面内容和 2008 当日子资源今天仍完整。

- Grade: A/B boundary: surviving contemporaneous page on original host
- URL: https://ent.sina.com.cn/head/ent20080615pm.shtml

### 3.4 2009—2010：格瓦拉从资讯/排片探索走向影院库存接口

2014 年对格瓦拉团队的回顾采访说，2009 年暑期其先与上海永华取得影院合作，2010 年《阿凡达》阶段继续扩张；团队面临的核心困难之一是影院售票系统此前并不愿意/习惯向第三方开放接口。

这是 C/B 边界的后来访谈，适合作为 `candidate claim`，不能代替 2009/2010 原始 API 文档或 historical capture。

可较强写成：

> 后来回顾材料把格瓦拉早期在线选座的关键瓶颈描述为第三方平台与影院/票务系统之间的库存数据接口，而非单纯网页展示。

不可直接写成：

> 2009 年全国影院已普遍开放实时接口。

- Grade: C/B
- URL: https://www.qianzhan.com/people/detail/314/140918-1d3884e0_3.html

### 3.5 2010《阿凡达》提供“远程库存不可见/不可执行”的峰值反例

多家 2010 同期报道保存上海和平影都 IMAX 排队、售罄和黄牛溢价。

这些材料不能证明“格瓦拉一定解决了所有《阿凡达》购票”，但说明：热门场次中，如果用户必须去影院才能确认库存，信息获取本身会消耗大量身体时间。

- Grade: B
- URLs:
  - https://style.sina.com.cn/news/2010-01-13/110654783.shtml
  - https://news.cntv.cn/society/20100108/102110.shtml
  - https://news.sina.com.cn/c/2010-01-08/051016897488s.shtml

### 3.6 2011：团购券与在线选座必须保持两种不同 object class

2011 年同期报道记录大量观众已在网上购买低价电影团购券，但热门影片仍可能需要提前到影院排队兑换具体场次，有的券还在现场遇到补差价。

因此仓库若以后建立 dataset，至少应让：

```text
voucher_product
seat-specific_ticket
```

成为两个不同类型。

- Grade: B
- URLs:
  - https://ent.sina.com.cn/m/f/2011-08-01/16013374380.shtml
  - https://news.sina.com.cn/o/2011-12-27/173523704358.shtml

### 3.7 2012：App Store 当前页面可提供“历史日期评论”，但不是历史 capture

格瓦拉 App Store 当前页面展示一条标记 2012-09-02 的评论，称应用让用户不再需要在售票窗口排队。

使用时必须写：

```text
current App Store rendering of a review labeled 2012-09-02
```

而不能写：

```text
verified 2012 App Store capture
```

这类材料非常适合 old-Web/early-mobile 的证据分类练习。

- Grade: B/C boundary
- URL: https://apps.apple.com/au/app/%E6%A0%BC%E7%93%A6%E6%8B%89%E7%94%9F%E6%B4%BB/id388083979

### 3.8 2013—2014：在线选座已成为可量化市场，但仍未覆盖全部影院

2014 年《南方日报》/人民网同期报道明确区分：

- 团购：通常购买电子兑换券，到影院再换票；
- 在线选座：查看场次座位状态，选座下单，凭兑换码到取票机取票。

报道引用艺恩口径称 2013 年在线选座市场约 12 亿元、约占总票房 5%，开通在线选座的影院比例仍是部分而非全部。

这条来源对 state model 很有价值，因为它直接证实当时完整常见 workflow 仍包含 `redemption code -> kiosk -> paper ticket`。

- Grade: B
- URL: https://media.people.com.cn/n/2014/1127/c14677-26107956.html

### 3.9 2014 乐影 App 版本材料：订单中断与实时座位同步已经进入产品语义

Apple App Store 当前乐影页面保存版本历史：

- 当前产品说明写“座位图与影院同步更新”；
- 2014-10-15 的 3.0.0 版本历史写新增“待支付订单”，用来避免支付意外中断后重新选座；
- 2014 其他版本记录会员卡支付、第三方账号登录等变化。

这类 current version-history page 不能替代 2014 IPA、API 抓包或当年页面 capture，但非常适合建立：

```text
seat-selection
→ pending-order
→ payment continuation
```

的 candidate state chain。

- Grade: B/C boundary, current store page preserving dated version history
- URL: https://apps.apple.com/cn/app/%E4%B9%90%E5%BD%B1%E7%BD%91-%E7%9C%8B%E7%94%B5%E5%BD%B1-%E4%BB%8E%E4%B9%90%E5%BD%B1%E5%BC%80%E5%A7%8B/id417621131

### 3.10 2014—2015：Web/App 已成为主入口，但不要把行业比例倒成浏览器形态

2014—2015 多份行业咨询数据显示在线购票和在线选座快速上升，到 2015 年线上出票量已经超过线下。

这只能证明交易渠道变化，不能据此猜：

- 用户使用 desktop Web 还是 mobile App；
- HTTP/API 结构；
- 影院端软件；
- 页面 charset；
- 取票是否无纸化。

- Grade: B
- URLs:
  - https://www.chinawriter.com.cn/2014/2014-08-07/213973.html
  - https://www.analysys.cn/article/detail/16977
  - https://www.chyxx.com/industry/201511/357025.html

---

## 4. Three ticket classes that must not be collapsed

### Class A — information-only / reservation-lead

页面只提供：

- 影讯；
- 影院电话；
- “订票信息”；
- 跳转链接。

它可以降低 information latency，但不一定触碰影院库存。

### Class B — voucher / group-buy

用户在线购买的是一种未来兑换资格。

Authority chain:

```text
platform voucher ledger
→ cinema accepts voucher?
→ showtime inventory at redemption time
→ possible surcharge
→ physical ticket
```

### Class C — real-time seat-specific order

Authority chain:

```text
cinema showtime inventory
→ seat availability
→ temporary hold
→ platform order
→ payment
→ issue entitlement
→ code
→ kiosk/box office
→ admission
```

同一句“网上买电影票”，在 2011 年可能指 A/B/C 中完全不同的事务。

---

## 5. Suggested minimal historical data model

```yaml
platform:
  name: null
  host: null
  date_observed: null

cinema:
  cinema_id_as_rendered: null
  name_as_rendered: null
  city: null
  address_as_rendered: null

showtime:
  film_title_as_rendered: null
  date: null
  time: null
  auditorium: null
  format: null   # 2D / 3D / IMAX etc, only if explicit
  price_as_rendered: null

transaction_capability:
  info_only: unknown
  voucher_purchase: unknown
  seat_map_visible: unknown
  seat_specific_purchase: unknown
  payment_online: unknown
  sms_code: unknown
  kiosk_redemption: unknown
  direct_mobile_entry: unknown
  refund: unknown
  change: unknown

archive:
  archive_source: null
  original_url: null
  capture_url: null
  capture_datetime: null
  http_status: null
  content_type: null
  charset: null
  main_html_saved: unknown
  css_saved: unknown
  js_saved: unknown
  images_saved: unknown
  seat_api_saved: unknown
  payment_endpoint_saved: unknown

browser_assumption:
  browser: unknown
  javascript_required: unknown
  flash_required: unknown
  activex_required: unknown
  cookies_required: unknown
```

---

## 6. Browser / protocol questions for future M1 work

不要因为对象是 2009—2012 中文网站就默认 IE6、GB2312、Flash。

每个具体 capture 应实测：

1. HTTP response `Content-Type`；
2. HTML `<meta charset>` 或 http-equiv；
3. 是否 table/frameset/div 不是核心 claim，除非实际查看 HTML；
4. seat map 是静态 HTML、图片 map、Flash、JS canvas 还是 DOM；
5. 座位状态通过页面内嵌 JSON、XHR、iframe 还是服务端刷新；
6. 登录是否依赖 cookie；
7. 支付是否跳第三方 host；
8. 是否弹窗；
9. 短信码生成是在支付前还是支付后；
10. 取票机/影院系统是否使用与 public Web 不同的私有接口。

任何未验证项继续写 `unknown`。

---

## 7. Archive asymmetries

### 7.1 showtime-shell / inventory-loss asymmetry

Crawler 很容易留下：

- 影片名；
- 影院名；
- 场次时间；
- 标价；
- “立即购票”按钮。

但真正最重要的“那个瞬间还有几个座位”通常是 API/数据库的瞬时状态。

所以历史页面越完整，越容易诱导研究者产生一种错误确定感：看见 19:20，并不等于知道 18:03 时还能买到 19:20。

### 7.2 seat-map-survival / seat-state-loss asymmetry

甚至可能完整保存空影厅座位图，却没有保存红/绿/灰状态的动态 endpoint。

```text
geometry survives
!= inventory survives
```

### 7.3 public-catalog / private-order authority inversion

最容易进入 archive 的是公开 catalog；最能证明一个普通人真正成功购票的是：

- order id；
- 手机号；
- 支付交易；
- 兑换码；
- 退款流水；

这些恰好属于私人数据或后台状态，不应为了考古重新公开。

### 7.4 redemption-chain loss

HTML 和 App 产品页可能还在，但影院里的自助取票机、短信短码、专线接口、旧票务软件已经退役。

于是一个今天看起来“页面齐全”的服务，真实 transaction chain 仍可能无法复原。

### 7.5 successful-use invisibility

绝大多数成功流程不会产生新闻：用户买票、取票、看完、回家。

新闻 archive 更倾向保存：

- 一票难求；
- 黄牛；
- 支付故障；
- 退票争议；
- 团购加价；
- 平台战争。

必须把 `failure visibility bias` 写在任何生活史解释旁边。

---

## 8. Hindsight risks

### H1 — 把 2010 在线选座想成今天扫码进场

不允许。2014 同期资料明确仍大量存在兑换码 + 自助取票机 + 纸票。

### H2 — 把“团购电影票”当成 seat reservation

不允许。很多团购只是券。

### H3 — 把网页显示座位当成实时数据库真值

必须先确定数据来源与刷新语义。

### H4 — 从在线票务份额推算人口普及率

交易不是人。

### H5 — 把当前 App Store 页面当成旧版 UI capture

当前页面可保存历史版本说明/日期评论，但它是 current rendering。

### H6 — 因为今天平台支持退款，就向 2012 倒推相同规则

退款能力、规则与 authority 必须按时点取证。

### H7 — 把“Web 不可见”写成“当时没有数字化”

影院售票后台、局域网和第三方接口可以高度数字化，却不一定被 crawler 看见。

---

## 9. Evidence table

| ID | Minimal claim | Grade | Confidence | Evidence family |
|---|---|---:|---|---|
| E01 | 2001 同期报道保存现场比较具体场次/价格的观影决策 | B | high for case | contemporaneous press |
| E02 | 2008 新浪娱乐日期页把“每日影讯/订票信息”作为栏目 | A/B | high for page | surviving contemporaneous Web |
| E03 | 2010《阿凡达》上海 IMAX 出现极端线下排队与售罄 | B | high | multiple contemporaneous press |
| E04 | 后来格瓦拉团队回顾把影院系统接口描述为在线选座早期瓶颈 | C/B | medium | retrospective founder interview |
| E05 | 2011 团购观影券可能仍需提前现场兑换 | B | high | contemporaneous press |
| E06 | 2011 团购券可能发生现场补差价争议 | B | high for case | contemporaneous press |
| E07 | 2014 报道明确区分团购券与实时在线选座 workflow | B | high | contemporaneous press |
| E08 | 当前 App Store 保存带 2012 日期格瓦拉用户评论 | B/C | medium | current rendering/historical date |
| E09 | 当前 App Store 乐影版本史保存 2014 “待支付订单”等产品语义 | B/C | medium-high | current store version history |
| E10 | 2013—2015 在线购票/选座份额快速上升 | B | medium-high | industry-research families |

---

## 10. M1 archive attempt status

### Goal

取得至少一个 2009—2014 中文电影票务对象的 verified historical capture，并核：

- `original_url`
- `capture_url`
- `capture_datetime`
- HTTP replay 状态
- charset
- DOM
- form/action 或 JS endpoint
- seat-map dependency
- payment handoff
- subresource completeness

候选：

- `gewara.com`
- `hipiao.com`
- 当时影院自有 Web 售票页
- 新浪等影讯聚合页

### This slice

本轮通过公开 Web 搜索取得：

- 2008 新浪娱乐 surviving dated page；
- 多个 2010—2014 同期媒体/产品 workflow 证据；
- current App Store dated version/review evidence；
- 若干 `gewara.com` / `hipiao.com` original-host leads。

但**没有实际打开并检查到**一个同时满足 METHOD §4 最低 capture 字段的 Wayback/其他 archive Memento。

因此：

```text
M1 verified historical Chinese cinema-ticketing/seat-selection Memento:
NOT ACHIEVED IN THIS SLICE
```

这**不等于**：

```text
Wayback did not preserve Gewara/Hipiao.
```

也不等于：

```text
historical page did not exist.
```

只表示本轮没有取得可按仓库证据合同升级的 capture。

---

## 11. Next high-value archaeology work

下一轮若继续这个对象，不应该再堆行业回顾，而应优先完成一个窄 M1：

### Candidate A — 2010—2012 格瓦拉选座页

目标拿到：

1. 首页/影院页一个 historical capture；
2. 影片场次页；
3. seat map；
4. 一个 payment/confirmation help page；
5. 取票机/短信码说明；
6. 第二历史时点。

### Candidate B — 2011 团购券 vs 在线选座对照

选同一影院，比较：

- 团购券页面；
- seat-specific ticket page；
- 使用限制；
- 到店兑换要求。

这样可以把 `voucher != reservation` 做成可复核案例。

### Candidate C — 2014 mobile handoff

将：

- App Store 版本说明；
- 公开 Web；
- 影院取票机说明；
- contemporaneous review/tutorial

串成“App 前端—影院库存—短信—取票机”证据链。

---

## 12. 对旧网史解释的新增结论

在线电影票务是一个非常好的旧网提醒：**Web 页面经常不是事务发生的地方，只是事务跨系统移动时人能看见的一层。**

2008 的“影讯”页可以让人提前知道有什么；2011 的团购页可以买到一个低价兑换资格；2014 的在线选座页可以触摸影院实时库存；但最终观众是否坐在 H8 上，还要经过支付、短信、取票机、检票和真实放映。

于是最应该避免的旧网幻觉是：

> 因为 archive 保存了一个“立即购票”按钮，我们就已经保存了当年的购票体验。

实际上，真正短命的恰恰是按钮背后的状态：**那一秒的座位、那一笔锁定、那条短信、那台取票机与那个最终被撕掉的纸票。**