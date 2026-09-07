# Railway ticket computer network, telephone, 12306 and return-travel state gaps (China, 1996–2015)

> Scope: 1996—2015 中文 Web / Web-adjacent 铁路客票基础设施。本文不写中国铁路运输通史，也不把全球票务系统并入本仓；1996—2010 的内部客票网络、窗口与电话只作为理解 2011 年以后 12306 中文 Web 的直接前史。

生活史 companion：

- `tmzncty/how-people-lived/topics/return-trip-executability-ticketing-infrastructure-and-reversible-migration-china-1996-2026.zh-CN.md`

本文只研究：**一张“可以回家/返岗”的火车票，在铁路后台、电话、浏览器、身份库、银行和实体检票之间究竟经历哪些不同状态，以及 old-Web 档案最容易保存错哪一层。**

---

## 1. 核心警告：铁路“联网售票”不能自动解释成 Internet 售票

1996 年《人民日报》同时代报道说，铁道部计划两年内实现计算机售票全国联网，使旅客可在任一购票窗口购买任一方向、任一车次车票。

来源：

- **A/B（同期中央报纸）**：1996-12-20：<https://cn.govopendata.com/renminribao/1996/12/20/5/>

同年北京站的现场报道则清楚显示，普通旅客仍然站在售票窗口前，由售票员在电脑上输入车次、日期、票别和数量并打印软纸票。

来源：

- **A/B（同期现场报道）**：1996-06-06：<https://cn.govopendata.com/renminribao/1996/6/6/1/>

因此本案必须至少拆成：

```text
railway internal network
!=
public remote reservation channel
!=
public Web
!=
household Internet self-service
```

这是研究中文旧网时一个特别容易被“今天一切都在网页上”的经验污染的术语陷阱。

### 新增 gap：`backend-networked / public-Web gap`

```text
窗口之间已经共享客票数据
!=
普通用户可以在浏览器里访问、锁座、支付
```

1996 的“全国联网”首先是铁路售票基础设施史，不是大众上网史。

---

## 2. 研究单位

按照 `docs/METHOD.md`，本案至少拆开：

- **core ticketing backend**：铁路客票发售和预订核心系统；
- **station terminal / window**：售票员操作终端；
- **telephone reservation service**：IVR/电话订票及其共享票额；
- **ticket pickup point / agency**：取票与代售点；
- **Web service / host**：例如 `www.12306.cn` / `kyfw.12306.cn`；
- **account**：注册用户；
- **passenger / contact record**：乘车人身份记录；
- **availability query**：一次余票查询；
- **reservation / seat lock**：暂时占用席位；
- **payment transaction**：银行/支付轨交易；
- **confirmed ticket order**：铁路订单确认；
- **paper ticket / e-ticket credential**：乘车凭证表现；
- **gate validation / boarding**：票证人与身体是否真正进入列车；
- **page / URL**：帮助、登录、查询、订单等页面；
- **capture**：档案保存的历史表示；
- **claim**：研究者依据 evidence 作出的最小结论。

不能因为这些状态都围绕“同一张火车票”就把它们合成一个对象。

---

## 3. 2008—2009 电话订票：远程事务早于全国 Web 自助

2008 年广铁春运电话订票已能预订部分返程临客；2009 年春运前，广东 9 个车站开始电话订票“通订通取”。深圳旅客可以拨广州地区电话订广州始发列车，成功后在深圳取票点取票。

来源：

- **B（同期媒体）**：2008-01-11：<https://news.sina.com.cn/c/2008-01-11/024013236900s.shtml>
- **B（同期媒体）**：2008-12-29：<https://news.sina.com.cn/c/2008-12-29/063914951398s.shtml>

这里的状态链已经是：

```text
call placed
→ IVR reachable
→ requested train/date accepted
→ quota available
→ reservation code/order generated
→ pickup deadline still valid
→ passenger reaches an enabled pickup point
→ paper ticket issued
→ passenger later boards
```

### `reservation / pickup gap`

电话里“订到了”不等于纸票已经在手。

### `channel-reachable / quota-available gap`

电话打通也不等于目标方向仍有票额。

### `reservation-location / pickup-location gap`

通订通取允许预订和取票发生在不同站点，但取票仍然是独立事务。

这些状态绝大部分不会因为某个介绍电话订票的新闻网页被 archive 保存，就自动留下历史交易证据。

---

## 4. 2011：12306 Web 出现以后，浏览器本身成为票务基础设施

2011 年 6 月铁路开始试行互联网实名售票，并逐步扩展；9 月 30 日，全国动车组进入网络售票范围。

来源：

- **B（同期报道）**：<https://news.sina.com.cn/o/2011-09-30/010923240998.shtml>

工商银行保存的同期业务说明给出一个重要跨系统链：

```text
12306 register/query/reserve
→ online banking payment
→ railway order
→ SMS/email information
→ paper-ticket pickup OR supported-ID direct gate
```

来源：

- **A/B（银行机构业务记录）**：<https://www.icbc.com.cn/page/721852349806313473.html>

这意味着 12306 不是一个孤立“网站”；它从一开始就是铁路核心客票系统、身份信息、银行支付、短信/邮件、窗口和闸机的组合前端。

---

## 5. `Web available / client executable gap`：2011 年非 IE 用户可能看得到站点，却买不了票

2011 年 6 月《新京报》记者分别测试 Chrome、Firefox、Safari、Opera，均无法正常进入购票功能；铁路客服当时表示网站基于 IE 标准，仅支持 IE6 及以上版本。IE9 和部分国内兼容浏览器可正常登录。

来源：

- **B（同期记者实测 + 客服说明）**：<https://news.sina.com.cn/c/2011-06-15/084622643844.shtml>

因此：

```text
URL resolves
→ homepage renders
→ user has Internet
!=
transaction UI is executable
```

### 考古意义

以后若获得 2011 年 12306 homepage 的 Wayback capture，也不能据现代 Chromium 成功显示首页就声称“当时浏览器体验已复原”。

至少还要核：

- IE6/7/8/9 差异；
- document/browser sniffing；
- HTTPS/TLS 与证书；
- 登录/session；
- 网银跳转；
- archive rewrite 是否破坏脚本；
- 查询结果是否来自历史动态接口还是今天的错误页/空壳。

---

## 6. `online ticket / paperless boarding gap`：网上买票不等于不再需要纸

2011—2012 的网上售票说明明确区分：

- 某些具备二代身份证检票条件的线路，可凭购票身份证直接过自动闸机；
- 其他大量场景，网上支付后仍需到铁路售票点换取纸质车票。

来源：

- **A/B（工商银行铁路网售支付说明）**：<https://www.icbc.com.cn/page/721852349806313473.html>

因此：

```text
online order confirmed
!=
paper ticket obtained
!=
credential accepted at gate
!=
passenger boarded
```

Web archive 最可能保存的是前端帮助页；真正的换票日志、闸机验证和身体上车行为通常在其采集面之外。

---

## 7. 2012：`payment-debited / ticket-confirmed gap`

2012 年春运同期报道记录 12306 登录缓慢、拥堵和“交了钱却拿不到票”等问题。

来源：

- **B（同期媒体）**：东方早报 / 新浪，2012-01-03：<https://news.sina.com.cn/c/2012-01-03/074223739863.shtml>

与此同时，工商银行统计称 2012 年春运 40 天仅该行就完成 412 万笔铁路互联网售票在线支付，说明支付接口已经进入大规模真实使用。

来源：

- **A/B（银行机构业务统计）**：<https://www.icbc.com.cn/page/721856222801461270.html>

因此至少要拆：

```text
availability returned
→ reservation/seat lock
→ payment page opened
→ bank debit success
→ payment callback received
→ railway order reconciled
→ ticket confirmed
```

### `seat-shown / seat-lock gap`

余票页面显示有票，不等于在用户提交时仍能锁到。

### `seat-lock / payment gap`

锁座成功，不等于用户在时限内完成支付。

### `bank-debit / railway-ledger gap`

银行侧成功，不等于铁路订单台账已经同步确认。

### archive implication

一张历史“支付成功”截图不能单独证明该乘客最终取得有效票；一张“订单成功”截图也不能证明实际乘车。

---

## 8. 2014：乘车人开始拥有公开可见的身份事务状态

2014 年 3 月起，12306 对注册用户和常用联系人实施身份信息核验。

二代身份证记录有：

- `已通过`；
- `待核验`；
- `未通过`。

护照等证件还可能出现：

- `请报验`；
- `预通过`；
- `未通过` 等。

官方须知明确规定，部分非可执行状态需要本人持证件原件到车站窗口或代售点核验。

来源：

- **A（12306 同期官方须知）**：<https://www.12306.cn/mormhweb/weixin/dtzx/wx_zxdt/201402/t20140223_38539.html>

因此新增：

### `account / passenger-identity gap`

账号存在，不等于其中每个联系人都具有可购票身份状态。

### `identity-record / online-executable gap`

身份信息已经填入系统，不等于已经通过核验。

### `online-failure / offline-recovery gap`

一个状态在网页里不能继续，并不等于整个票务制度拒绝此人；官方仍可能要求回到窗口用原件恢复可执行状态。

这个例子非常适合阻止“线上失败 = 现实资格不存在”的误读。

---

## 9. 一张旧网页里最危险的词：`余票`

对 12306 之类动态事务系统，archive 研究不能把“页面被抓到”与“历史余票状态被抓到”混为一谈。

至少存在：

```text
historical HTML shell
!=
historical query request
!=
historical backend response
!=
historical inventory state
```

即使 Wayback 保存了：

- 首页；
- 登录页；
- 帮助页；
- JavaScript/CSS；

也可能完全没有保存：

- 当天某车次真正返回的余票；
- 用户提交时的锁座状态；
- 支付回调；
- 订单数据库；
- 短信；
- 电话 IVR；
- 取票机/窗口交易；
- 闸机扫描；
- 实际乘车。

这可以称为：

## live-inventory transaction dark matter（实时库存事务暗物质）

它不是 archive “坏了”，而是这类系统最重要的生活状态本来就大量发生在可公开抓取网页之外。

---

## 10. 2014—2015：Web 成为主要渠道，也不等于其他渠道死亡

2014 春运同期报道已经把网络购票称为首选方式，同时仍记录站前、窗口和不同人群的购买经验。

来源：

- **B（同期报道）**：<https://news.12371.cn/2014/01/16/ARTI1389838811604930.shtml>

这段时期应避免写成：

```text
window → telephone → Web
```

更接近：

```text
window
+ agency
+ telephone
+ Web
+ later mobile client
```

不同渠道共享或竞争同一底层库存，却有不同：

- 开放时段；
- 预售期；
- 身份要求；
- 支付方式；
- 设备/浏览器要求；
- 失败后的恢复方式。

因此新增：

## channel-specific transaction horizon（渠道特定事务地平线）

“这张票现在能不能买”必须加上“通过哪个渠道、在什么时点、用什么身份与设备”。

---

## 11. old-Web state machine

本案建议以后所有 12306 / 电话订票 claim 至少定位到以下状态之一：

```text
train/service exists
→ quota loaded into ticketing backend
→ channel opens for this date/train
→ query returns candidate
→ seat shown
→ passenger identity executable
→ reservation/seat locked
→ payment initiated
→ bank/payment side succeeds
→ railway ledger reconciles
→ ticket/order confirmed
→ paper credential exchanged if required
→ ticket/ID accepted at gate
→ passenger boards
→ journey completes
→ refund/rebooking/return journey if needed
```

### 当前已明确命名的 gaps

- `backend-networked / public-Web gap`
- `channel-reachable / quota-available gap`
- `reservation / pickup gap`
- `Web-available / client-executable gap`
- `seat-shown / seat-lock gap`
- `seat-lock / payment gap`
- `payment-debited / ticket-confirmed gap`
- `online-ticket / paperless-boarding gap`
- `account / passenger-identity gap`
- `identity-record / online-executable gap`
- `online-failure / offline-recovery gap`
- `ticket-confirmed / gate-accepted gap`
- `gate-accepted / actually-boarded gap`
- `ticket-record / lived-movement gap`
- `historical-page / live-inventory-backend gap`

---

## 12. 历史可见性偏差

### 12.1 帮助页会比真实失败更容易保存

平台官方说明通常公开、静态、可抓取；真实交易失败多发生在：

- session；
- POST；
- 登录后页面；
- 动态查询；
- 银行跳转；
- 私有订单；
- 电话；
- 窗口。

因此未来 archive 很可能系统性高估“规范流程”，低估真实用户卡在哪一步。

### 12.2 Web 会高估个人独立执行

一个订单属于某个账号，并不自动证明乘车人自己操作了账号。

后续生活史已有 2019 年工地同事代买的第一人称案例，说明“常用联系人”可以代表真实代理关系：

- <https://www.chinanews.com/gn/2019/01-21/8734553.shtml>

该材料超出本文 2015 主 scope，只作为**边界验证**：研究 2011—2015 账号/联系人时，不得默认 `account operator == passenger`。

### 12.3 ticket record 不是 body trace 的完美代理

```text
ordered
!=
paid
!=
issued
!=
boarded
!=
arrived
```

尤其在退票、改签、错过列车、代购或多人订单场景中，数据库记录与身体移动可能明显脱耦。

---

## 13. 海外前史只作为 companion 边界，不扩仓库 scope

法国 SNCF 在 WWW 以前就已通过 Minitel 提供铁路预订。1988/1989 法国参议院答复明确说，TGV 可以经窗口、旅行社、自动设备和 Minitel 预约，而且这些入口连接同一个中心服务器：

- <https://www.senat.fr/questions/base/1988/qSEQ881202718.html>

1990 年《世界报》又记录 SOCRATE 系统将连接车站、旅行社、自动设备和 Minitel：

- <https://www.lemonde.fr/archives/article/1990/07/12/la-sncf-inaugure-un-nouveau-systeme-de-reservation_3991275_1819218.html>

这部分**不作为 old-web 的全球案例展开**，只用于限定一个历史解释：

> “家庭远程数字订铁路票”并不是 WWW 独有能力；本仓真正研究的是中文旧网里 12306 如何叠在中国既有铁路客票网络之上，以及它留下了什么独特证据缺口。

全球比较和生活后果应写回 `how-people-lived`。

---

## 14. Archive / replay 当前状态

### 已取得

本轮取得并核验的是：

- 1996 同期报纸中的窗口电脑售票和全国联网描述；
- 2008—2009 电话订票 / 通订通取的同期报道；
- 2011 网上售票范围与浏览器兼容的同期报道；
- 银行机构保存的支付/出票业务说明；
- 2012 支付与出票异常的同期报道；
- 2014 12306 官方身份核验须知；
- 明确的历史 host/locator：`www.12306.cn` 等。

### 本轮没有取得

**没有实际取得并检查一份满足本仓证据合同的 2011—2015 12306 Wayback/WARC replay response。**

因此以下内容继续写作 `unknown`：

- 2011 首页/登录/购票页的原始 HTTP headers；
- 当时 Content-Type / charset；
- DOM、frames、JS 具体版本；
- 浏览器嗅探实现；
- 根证书/HTTPS 的实际请求链；
- session/cookie；
- 历史查询 endpoint；
- 银行 callback；
- 某时点余票 API response；
- 错误页面和超时页面的可复核 capture。

正确措辞是：

> **本轮尚未验证到合格 capture。**

不得写成：

> **Wayback 没有保存 12306。**

---

## 15. M1 status

**M1 — NOT ACHIEVED IN THIS SLICE.**

原因：

- 有多个同时代 evidence family；
- 有历史 host、功能和浏览器条件；
- 但没有实际验证 ≥2 个历史 Web capture 时点；
- 没有完成资源缺失、DOM/编码、旧浏览器 replay 的 capture-level 记录；
- 因此本文仍是 **research companion / state-gap note**，不是完整考古 case。

---

## 16. 已证实 / 高概率 / 不知道

### 已证实

- 1996 中国铁路已经在推进计算机售票和跨窗口联网；这不是公众 Internet 自助。
- 2008—2009 广东已有电话订票和通订通取。
- 2011 12306 互联网实名售票逐步进入实际运营。
- 2011 存在明确 IE 浏览器兼容限制。
- 网上支付、短信/邮件、纸票换取和部分身份证直刷属于不同事务环节。
- 2012 出现支付后未成功出票的同期报道。
- 2014 互联网乘车人身份核验成为显式状态机。

### 高概率但需 capture/更多技术材料确认

- 2011—2012 大量真实失败发生在前台 HTML 之外的 session、核心库存和支付同步层。
- 历史 Web archive 即使保存 12306 页面，也很可能无法直接保存某时刻的完整实时库存和个体订单路径。

### 不知道

- 2011 具体 production 页面在不同月份的 HTML/JS 差异；
- 早期 12306 所有浏览器/OS/TLS 组合的真实兼容矩阵；
- 2011—2013 各失败状态的发生率；
- Wayback/Common Crawl 对登录前动态查询接口实际保存到什么程度；
- 电话 IVR 的完整历史 prompt、超时和取票码格式；
- 早期 Web 用户中有多少订单实际由代理人替乘车者完成。

---

## 17. 它对中文旧网考古的意义

12306 是一个很好的反例：**历史上最重要的 Web 服务，未必最适合用“页面截图”研究。**

它真正改变普通生活的部分，是一个跨系统状态机：

- 核心票额数据库；
- 浏览器；
- 身份库；
- 银行；
- 短信；
- 纸票；
- 窗口；
- 闸机；
- 最后才是人的身体。

Web 页面只是其中一个控制面。

所以 future archaeology 如果只问“2012 年 12306 长什么样”，会漏掉更重要的问题：

> **这个页面在当时究竟能不能把一个普通人的回家计划，从“我想走”推进到“铁路系统真的为我保留了一张可使用的票”？**

---

## Research note

本研究包为 AI 辅助初稿。未复制历史页面、车票、个人账户或敏感交易数据；普通个人材料只保留支持结构性 claim 所需的最小信息。后续若进入完整 M1 case，应优先取得可验证 capture metadata 与旧浏览器 replay，而不是凭今天的 12306 页面补画历史界面。