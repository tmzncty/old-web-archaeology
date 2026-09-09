# RAILWAY TICKETING / QUERY / ORDER / PAYMENT / IDENTITY / TRAVEL-EXECUTION STATE GAPS (2005—2015)

> Status: research package / state-gap note  
> Scope: 中文旧网约 2005—2015。1960s SABRE、1999 英国 Trainline 只作 reservation / public-Web booking 的海外技术前史对照，不把本仓扩成全球票务史。  
> Life-history companion: `tmzncty/how-people-lived/topics/from-ticket-window-to-waitlist-and-reservation-rail-ticketing-booking-horizons-and-mobility-optionality-china-1980-2026.zh-CN.md`

## 0. 研究问题

旧 Web 中的铁路购票页很容易给后来研究者一种错觉：

> 看见“查询”“预订”“提交订单”“支付”按钮，就仿佛已经看见了一次真实购票。

但铁路票务是一个典型的高状态密度事务：

```text
查询页可打开
→ 日期/发到站合法
→ 该车次进入当前渠道预售期
→ inventory query 返回
→ 页面显示余票
→ 用户登录
→ 乘车人身份有效
→ 提交订单
→ 服务器排队
→ 席位锁定
→ 支付
→ 出票
→ 取票/电子客票状态
→ 进站核验
→ 实际乘车
```

任何相邻两步都不能自动互推。

本稿研究的是：

1. 2005—2015 中文 Web 中铁路查询/订票界面怎样进入日常；
2. 为什么 dynamic inventory、登录态、排队、支付和实名核验特别难被 archive 完整保存；
3. 如何避免把一张静态历史页面误当成“当时真的可以买到票”的证据。

---

## 1. 与仓库 METHOD 对齐

本稿遵守 `docs/METHOD.md`：

- platform / site / host / account / page / capture / claim 分开；
- A/B/C/D 分级；
- archive locator 未实际打开不得写成 verified capture；
- `exists != available != used != popular != caused`；
- modern page / current backend 不得冒充 historical transaction；
- `没有找到 != 当时不存在`；
- 不重新公开普通旅客真实身份证号、手机号、订单号等私人票务数据。

本专题固定：

```text
booking page captured
!= inventory captured

query result rendered
!= seat reserved

order submitted
!= queued successfully
!= seat locked
!= paid
!= ticket issued

identity form accepted
!= identity verified

payment success page
!= railway ticket-state commit proven

online ticket exists
!= gate execution succeeds under every station/credential condition
```

---

# 2. 研究对象必须拆层

## 2.1 platform / host

至少区分：

- 铁路客户服务中心官网；
- `12306.cn` / 后续具体客运服务 host；
- 铁路局/地方历史查询页；
- 第三方时刻/余票查询站；
- 第三方抢票/聚合工具；
- 支付网关；
- 电话订票系统。

同一品牌下的 host、前端和后端可能跨年份迁移。

## 2.2 account

12306 事务至少涉及：

- registered user；
- passenger / 常用联系人；
- account owner 与 passenger 可以是不同人；
- identity-verification state；
- phone / email contact；
- login/session state。

所以：

```text
account holder != passenger
```

而且：

```text
passenger stored in account
!= passenger identity verified
```

## 2.3 train / journey / segment

车票不是单纯 `train_id + seat`。

至少有：

```text
travel_date
+ train number
+ origin
+ destination
+ seat class
+ passenger type
+ sales channel
+ presale state
```

同一趟车从 A 到 D 的某席位是否可以卖给 A→B，与 B→D 的库存约束并不是一个简单静态总数可以完全描述。

本稿不根据民间逆向工程自行断言铁路内部 seat-allocation 算法；只固定：**网页上看到的余票是后端在特定时间、特定 query 条件下返回的 transaction view。**

## 2.4 query result

一条历史余票结果至少绑定：

```text
query_time
+ travel_date
+ origin/destination
+ channel
+ passenger type
+ backend inventory snapshot
+ client/session context
```

所以：

```text
“无票”
```

可能表示：

- 真正售罄；
- 尚未到起售时间；
- 当前渠道未开放；
- 当前区段被限售；
- 查询超时/错误被 UI 映射成无结果；
- 历史脚本回放失败；
- modern backend 对 historical parameters 给了现代结果。

## 2.5 order / queue / lock

订单至少要拆：

```text
order draft
→ submit request
→ queue admission
→ inventory recheck
→ seat allocation/lock
→ payment pending
→ paid
→ ticket issued
→ cancelled/expired/refunded
```

一个页面显示“排队中”，不能证明已经锁到席位。

## 2.6 credential / passenger identity

实名制以后，票务对象不只是 seat transaction，还绑定：

- 证件类型；
- 证件号码；
- 姓名；
- 核验状态；
- passenger/contact relationship。

2014 年网上身份核验出现多种状态后，这个层级必须独立保存。

## 2.7 travel execution

`ticket issued` 以后仍要区分：

```text
paper ticket retrieved / not retrieved
identity readable / not readable
gate supports ID direct entry / not supported
manual check / automatic gate
train actually boarded / not boarded
```

旧 Web 只看到订单，不等于历史研究已经看到完整旅行。

---

# 3. 海外技术前史边界：reservation backend 远早于 public Web

## 3.1 1964 SABRE：实时库存首先服务机构终端

Computer History Museum 记录 American Airlines / IBM SABRE 在 1964 年已通过电话线连接约 2000 个终端到中心计算机，用于实时航空订位。

Sources:
- https://www.computerhistory.org/timeline/1964/
- https://www.computerhistory.org/internethistory/1960s/

Evidence: **B+（博物馆技术史）。**

用途仅限证明：

> 多地点同时访问有限席位库存，是 public Web 以前就存在的 online transaction problem。

不要写成：

> 1964 年普通旅客已经可以自己在家操作在线订票。

## 3.2 1999 Trainline：public Web rail booking 的海外对照

Railway Gazette 1999 年同期报道英国 TheTrainLine 于 1999-02-25 上线，用户可以通过 Internet 为不同铁路运营商查询、购买车票和席位预订，并安全支付。

Source:
- https://www.railwaygazette.com/news/thetrainline-brings-online-booking-to-britain/27579.article

Evidence: **B+（同期行业媒体）。**

用途是比较形态：

```text
public query
→ reservation
→ payment
→ fulfillment
```

不证明中国铁路 1999 年已经有同等 public self-service。

---

# 4. 2005—2010 边界：中文 Web 可以查铁路信息，但真正的席位交易仍大量在线下/电话完成

本仓主体从 2005 开始观察中文 Web，但必须避免把“查车次/票价/余票”的第三方页面与“铁路官方完成售票事务”混在一起。

2008 前后，中国铁路后台已经经过计算机售票与全国联网演进；普通用户前台仍大量依靠：

- 售票窗口；
- 代售点；
- 电话；
- 铁路局本地渠道；
- Web 时刻/查询信息。

2010 年博客园公开春运电话订票指南，工作流包括：

```text
电话拨号
→ 输入乘车信息/身份证
→ 语音生成取票密码
→ 在期限内到指定点取票
```

Source:
- https://www.cnblogs.com/vaiyanzi/archive/2010/01/24/1655448.html

Evidence: **B（同期用户指南）。**

2011 年鄂州市政府公开说明 95105105 提供订票、订单查询、取消、车次、票价、余票和取票点查询。

Source:
- https://www.ezhou.gov.cn/smpd/tzgg/201101/t20110131_64718.html

Evidence: **A/B+（同期政府服务信息）。**

这说明中文旧网前史不能写成：

```text
没有 public Web checkout
= 没有远程数字票务
```

电话 IVR 已经是远程 transaction interface。

---

# 5. 2011：12306 public Web transaction state 出现

## 5.1 京津城际试行互联网售票

2011-06-12，京津城际开始试行网络售票。同期报道明确：

- 用户先注册 12306；
- 在网页完成购票；
- 成功后通过邮件/短信获得提示。

Source:
- https://www.chinadaily.com.cn/dfpd/bj/2011-06/13/content_12680031.htm

Evidence: **B+（同期媒体）。**

这足以证明：

```text
public Web booking transaction exists
```

但不能单独证明：

- 全国所有列车都已可网购；
- 所有旅客证件都可使用；
- 所有车站都支持同样取票/进站流程；
- 网站在所有高峰都可稳定完成 transaction。

## 5.2 2011-06-27：证件支持范围是 Web availability 的一部分

同期媒体实测京沪高铁网购：

- 注册；
- 查询；
- 输入有效实名证件和联系方式；
- 支付；
- 凭证件/订单号办理后续；
- 当时网购支持五类证件。

报道还记录一名 16 岁学生因为学生证不在网上购票有效证件范围，只能帮父母网购后自己到代售点购买。

Source:
- https://www.chinadaily.com.cn/dfpd/sh/2011-06/27/content_12785072.htm

Evidence: **B（同期记者实测 + 同期用户发言）。**

因此：

```text
Web transaction exists
!= Web transaction available to every credential state
```

这是 old-Web 研究必须保存的 interface boundary。

---

# 6. Query state machine

一个最小余票查询应拆成：

```text
Q0 query page requested
Q1 main HTML returned
Q2 JS / station-code resources loaded
Q3 user chooses date/from/to
Q4 client validation passes
Q5 query request sent
Q6 backend accepts query
Q7 backend inventory snapshot resolved
Q8 payload returned
Q9 client parses payload
Q10 result table rendered
Q11 user reads result
```

硬边界：

```text
Q1 != Q5
Q5 != Q8
Q8 != Q10
Q10 != historical inventory reproducibility
```

### Archive implication

一份 capture 如果只有 Q1/Q2：

- 可以证明查询 UI / form shape；
- 不能证明某日期某车次当时的真实余票。

如果 archive replay 在 2026 年重新执行一个仍存活 endpoint：

> 这叫 **current-backend rehydration**，不是 historical inventory replay。

---

# 7. Presale-state gap：无票不一定是 sold out

铁路售票具有强时间窗。

2011—2013 同期材料显示不同渠道的预售期与起售时间可以不同；例如部分地区电话/互联网渠道可以早于窗口，学生票/春运又可能有特殊安排。

Sources:
- https://www.chinadaily.com.cn/dfpd/2011-12/30/content_14357835.htm
- https://www.chengde.gov.cn/art/2011/12/25/art_360_72785.html
- https://edu.people.com.cn/GB/8216/354282/index.html

Evidence: **B+/A-like（同期服务规则）。**

因此历史结果里的：

```text
“--”
“无”
“无票”
```

必须先排除：

- not yet on sale；
- channel not yet open；
- current interval restriction；
- query error；
- timeout。

推荐 artifact 字段：

```text
observed_at
travel_date
channel
known_presale_rule_version
known_sale_start_time
ui_value
interpretation_confidence
```

---

# 8. Order / queue state machine：2012 春运以后绝不能把“提交”当“出票”

一个最小 Web 购票流程：

```text
O0 train selected
O1 passenger(s) selected
O2 order form initialized
O3 identity/contact fields valid
O4 submit clicked
O5 request reaches server
O6 duplicate/session/token checks pass
O7 request admitted to order queue
O8 inventory rechecked
O9 seat allocation/lock succeeds
O10 order record created
O11 payment requested
O12 payment confirmed
O13 railway backend records paid state
O14 ticket issued
O15 confirmation rendered/notification sent
```

硬边界：

```text
O4 != O7
O7 != O9
O9 != O12
O12 != O14
O14 != actual travel
```

2012 春运高峰时期，12306 出现难登录、排队、失败与系统压力。2013 年技术负责人接受新华社采访时回顾，2012 春运第一次大规模实战中高峰点击接近 15 亿次。

Sources:
- https://politics.people.com.cn/n/2013/0116/c70731-20225837.html
- https://finance.people.com.cn/n/2012/1227/c1004-20034695.html

Evidence: **B（同期/近同期报道 + 系统负责人采访）。**

因此 archive 看到一张“提交订单”页，只能支持 O2/O3 附近的存在，不能支持 O14。

---

# 9. 2012 技术用户材料：旧 Web 的真实 transaction seam 往往藏在 JS/token/重试里

2012-01-10，博客园程序员公开记录 12306 订票助手的重试逻辑，并讨论验证码、重复提交等问题。

Source:
- https://www.cnblogs.com/studyzy/archive/2012/01/10/2318400.html

Evidence: **B（同时代技术用户观察；不是铁路官方实现文档）。**

这类材料的价值：

- 能证明当时用户实际遇到 client/server transaction friction；
- 能提供历史 UI/API 线索；
- 能解释为什么浏览器插件成为购票实践的一部分。

不能用来：

- 断言铁路内部完整架构；
- 证明某个 reverse-engineered endpoint 的语义在所有日期稳定不变；
- 把民间所谓“Bug”直接当官方根因分析。

Evidence grade 只能停在 **B/D-supporting**。

---

# 10. Identity state machine

2011 动车实名制、2012 更广泛实名制以后，Web 票务必须增加 identity state。

2014-03-01 起，12306 对互联网购票身份信息实施进一步核验。

同期规则中：

- 二代居民身份证用户/常用联系人可能显示“已通过 / 待核验 / 未通过”；
- 护照等证件还可能出现“请报验 / 预通过”等状态；
- 不是所有状态都能正常完成网络购票。

Source:
- https://politics.people.com.cn/n/2014/0223/c70731-24440092.html

Evidence: **A/B+（铁路总公司信息经新华社）。**

最小状态：

```text
I0 passenger record created
I1 credential fields entered
I2 submitted for verification
I3 pending / report-needed / pre-approved / failed / passed
I4 passenger usable in online transaction
I5 credential presented at offline checkpoint if required
```

硬边界：

```text
record saved != verified
verified online != every offline gate supports same credential path
```

---

# 11. Payment state machine：银行成功页不是 railway transaction 的唯一事实来源

铁路网购至少涉及两个系统边界：

```text
railway order backend
↔ payment gateway / bank
```

最小支付状态：

```text
P0 order created unpaid
P1 payment page/request created
P2 user authenticates at bank/gateway
P3 gateway says payment success
P4 callback/return reaches railway backend
P5 railway backend matches payment to order
P6 order marked paid
P7 ticket issued
```

因此：

```text
P3 != P6
P6 != P7
```

archive 尤其容易只保存：

- redirect URL；
- gateway shell；
- “已支付”截图；

但没有两边的 commit correlation。

old-Web 复原不得因为看到 bank success page 就写“票已成功出票”。

---

# 12. Ticket retrieval / e-ticket / gate execution 也必须拆开

2011 同期报道已经出现：部分条件下，网购后可凭二代身份证直接办理进出站，也可凭订单号/证件到窗口或代售点换票。

Source:
- https://www.chinadaily.com.cn/dfpd/sh/2011-06/27/content_12785072.htm

所以：

```text
online purchase
→ paper retrieval path
OR
→ identity-direct gate path (only where supported)
```

不能把 2020s “刷身份证就是票”的常态倒写进 2011 所有车站。

推荐状态：

```text
T0 ticket issued
T1 paper ticket required / optional / not required under local rules
T2 retrieval attempted
T3 paper issued
T4 passenger arrives station
T5 credential/ticket accepted at gate
T6 boarded
```

---

# 13. 2013—2015：booking horizon 与 page meaning 会随规则版本漂移

2013 春运，媒体已把 Web/电话预售 20 天作为重要优势。

Source:
- https://edu.people.com.cn/GB/8216/354282/index.html

2014 年底，2015 春运预售期又被延长到 60 天，同期媒体提醒过早预订可能导致“囤票”和后续集中退票。

Source:
- https://politics.people.com.cn/n/2014/1222/c70731-26248191.html

因此同一个页面组件：

```text
date picker
```

在 2012、2013、2015 具有不同有效未来范围。

这产生：

### `rule-version drift`

```text
same UI shape
!= same presale semantics
```

archive 如果没有规则版本与 capture_datetime，就可能错误解释某个日期为什么不可选。

---

# 14. 2015 抢票/自动化工具：第三方 client 不是铁路官方页面，但属于真实旧网使用环境

2015—2016 前后大量技术文章公开分析 12306 登录、联系人、查询、订单 endpoint 与 token；其中一类文章直接展示：

- 登录；
- 常用联系人；
- 查询余票；
- 提交订单；
- `REPEAT_SUBMIT_TOKEN` 等 client state。

Example source:
- https://www.cnblogs.com/russellwang/p/4174886.html

Evidence: **B（同时代技术用户逆向观察）。**

这种材料只能用于：

- 确认旧 Web transaction 不是一个单页 POST；
- 发现 endpoint / JS / token artifact 候选；
- 解释 browser automation 的状态依赖。

不能：

- 证明官方内部实现；
- 保证 endpoint 在整个 2015 年稳定；
- 把作者的模拟客户端结果当官方客户端等价物。

---

# 15. Queue observability gap：用户看到的“排队”不是服务器内部队列的完整镜像

历史 UI 可能显示：

- “正在排队”；
- “订单处理中”；
- “提交失败”；
- “余票 1 张”；

但实际系统里可能同时存在：

- Web request queue；
- inventory lock queue；
- payment timeout；
- order deduplication；
- anti-automation controls；
- distributed replication lag。

因此：

> **UI queue state 只能作为 user-observable state，不得直接命名内部 queue implementation。**

这是本专题的 `queue-observability gap`。

---

# 16. Inventory snapshot ephemerality：余票页是特别短命的历史对象

余票值可能在秒级变化。

一份 archive capture 的时间戳即使精确到秒，也仍可能无法回答：

- 查询请求何时发出；
- response 何时产生；
- HTML 主文档何时被 archive；
- XHR payload 是否被单独捕获；
- archive rewrite 后页面是否重新发起了现代请求。

因此：

```text
capture_datetime(page shell)
!= inventory_snapshot_time
```

如果没有历史 payload，就不要把 replay 页面里的余票值写成历史事实。

---

# 17. `sold-out hindsight bias`：最终“无票”会抹掉中间多次释放与回流

票额并不是只在起售时一次性固定后永不变化。

退票、改签、临时增开、分阶段放票都可能让 inventory 重新出现。

因此一个后来保存的“无票”页面，不能代表：

> 从起售到开车全过程始终没有任何可购买时刻。

这叫：

**`sold-out hindsight bias / 售罄后见偏差`**。

同理，一张最终成功订单也会抹掉此前：

- 多少次查询；
- 多少次失败；
- 是否使用第三方工具；
- 是否先买了替代车次再改签。

---

# 18. `sale-channel asymmetry`：窗口、电话、Web 不一定拥有相同时间语义

同期规则多次出现：

- 电话/互联网预售期不同于窗口；
- 起售时刻不同；
- 学生票、春运等有特殊窗口；
- 部分票种不能由某一渠道完成。

因此：

```text
ticket available in system
!= ticket available through this channel now
```

历史研究必须记录 `channel`。

否则很容易出现错误结论：

> “某人网上没买到，所以当时铁路完全没票。”

实际上可能只是当前 Web/channel state 不允许该票种或该时间段。

---

# 19. `credential-interface gap`：真实乘车资格与 Web 可表达证件集合不同

2011 京沪高铁同期实测显示，现场有效证件集合与 Web 当时支持的证件类型并不完全相同。

这产生：

```text
person legally eligible to travel
!= person representable by current Web form
```

对旧网考古特别重要，因为网页下拉菜单本身就是历史制度接口。

应该保存：

- `<select>` options；
- help page credential list；
- validation JS；
- server error strings；
- offline fallback instructions。

而不是只保存一个空表单截图。

---

# 20. 旧 Web artifact 应该怎样分级

建议本专题使用以下保存等级：

### R0 — mention only

只有“网上可订票”文字记载。

### R1 — hostname / canonical entry

确认历史 official host/URL。

### R2 — static booking/query shell

HTML/form/help page 可验证。

### R3 — client resources

历史 JS、station codes、validation、CSS 等可验证。

### R4 — historical dynamic result payload

至少一份同 capture 时段的查询/订单 response 可验证。

### R5 — transaction transition evidence

可证明 query → order 或 order → payment 等至少一段真实历史状态变化。

### R6 — end-to-end historical transaction artifact

拥有可验证的 historical：

```text
query
→ order
→ payment
→ issued ticket state
```

注意隐私去标识。

### R7 — executable reconstruction

在明确历史浏览器/协议/服务替代条件下复原 transaction logic；必须标 `reconstruction`，不得冒充原系统。

---

# 21. Archive replay 本轮结果

本轮已通过同期来源确认：

- `www.12306.cn` 在 2011 年作为中国铁路客户服务中心 Internet 购票入口实际存在；
- 2011-06 起存在真实 public Web purchase workflow；
- 2012—2015 页面/客户端存在强动态 transaction state。

本轮尝试直接打开 Internet Archive CDX：

```text
https://web.archive.org/cdx/search/cdx?url=www.12306.cn&from=2011&to=2012&output=json&filter=statuscode:200&limit=5
```

当前研究访问链拒绝未经搜索结果安全确认的构造 Wayback URL，因此没有得到可逐项核验的 historical memento。

所以严格记录：

```text
M1 verified 2011–2012 12306 historical Web capture:
NOT ACHIEVED IN THIS SLICE
```

这**不等于**：

```text
Wayback did not preserve 12306
```

也不等于：

```text
historical page did not exist
```

下一轮如果能通过合法 locator 进入，应记录：

```text
archive_source
capture_url
original_url
capture_datetime
HTTP/replay state
Content-Type / charset
main HTML
JS/subresources
form action
XHR endpoint
login redirect
whether dynamic result is historical or live-backend rehydration
```

---

# 22. Browser / charset / TLS / JS 假设

铁路网购属于高度依赖浏览器执行的事务。

历史复原应检查：

- IE / Firefox / Chrome 兼容性；
- JS 是否必需；
- HTTPS / certificate compatibility；
- cookies / session；
- popup/redirect；
- bank gateway browser requirements；
- character encoding；
- date picker；
- image captcha；
- AJAX/XHR；
- anti-automation client code。

现代浏览器能打开历史 shell，不能证明 2012 年浏览器环境当时能以同样方式执行。

---

# 23. 隐私边界

铁路票务 artifact 很容易包含：

- 姓名；
- 身份证号；
- 手机号；
- 邮箱；
- 出发/到达地；
- 出行日期；
- 订单号；
- 常用联系人；
- 家庭代购关系。

这些数据组合起来可以暴露普通人的迁移、家庭、工作与长期生活轨迹。

所以高等级考古不需要重新公开真实个人订单。

优先保存：

- public demo/help；
- 去标识 transaction shape；
- error strings；
- schema；
- state transitions；
- client code；
- 官方规则。

---

# 24. 与 life-history companion 的交叉点

旧网 artifact 研究回答：

> 一个历史铁路购票页面到底证明了哪一步？

生活史 companion 回答：

> 当远程查询、电话预订、网络下单、实名核验和后来的候补成为普通生活的一部分以后，人为什么更能把跨城读书、工作、探亲和返乡写进未来计划？

两仓必须互相约束：

```text
life history 不得从页面存在推出全民可用
old-web archaeology 不得只研究 DOM 而忘记 transaction state 对真实移动的意义
```

---

# 25. 已证实 / 高概率 / 不知道

## 已证实

- 中国铁路后台计算机化/全国联网早于大众 public-Web self-service；
- 2010 前后电话订票已形成远程预订 + 实体取票路径；
- 2011-06 京津城际及随后更多动车进入 12306 Internet ticketing；
- 2011 early Web ticketing 具有证件类型限制；
- 2012 春运出现显著并发/可用性压力；
- 2014 Internet identity verification 存在多个状态；
- 2013—2015 预售规则变化会改变同一查询页面的时间语义。

## 高概率但需更强 artifact

- 2011—2012 历史页面主 HTML 可能被 archive 保存；
- 部分 JS / station-code / help page 很可能可通过历史快照恢复；
- 部分 transaction endpoint 名称可由同期技术用户文章复原。

## 不知道

- 当前可合法取得的最早 12306 完整可验证 Wayback memento 时间；
- 哪些 2011—2012 XHR/queue/payment payload 被 archive 实际捕获；
- 早期 seat lock / queue 的内部真实实现；
- 某一具体历史“排队中”UI 与后台队列层的精确一一对应关系。

---

# 26. 本轮新增的 state-gap 概念

- `presale-state gap`：无票 vs 尚未起售/渠道未开放；
- `queue-observability gap`：用户排队提示 vs 内部队列实现；
- `inventory snapshot ephemerality`：页面时间 vs 余票快照时间；
- `sold-out hindsight bias`：最终无票抹掉中间库存回流；
- `sale-channel asymmetry`：同一票额在窗口/电话/Web 的可交易时间不同；
- `credential-interface gap`：现实有效证件 vs Web 可表达证件；
- `rule-version drift`：同一 UI 在不同年份受不同预售/退改规则控制；
- `payment-commit gap`：银行支付成功 vs 铁路订单已提交出票；
- `ticket-execution gap`：已出票 vs 实际通过闸机/完成旅行；
- `current-backend rehydration`：历史 shell 调到现代后端，不得冒充历史结果。

---

# 27. 这一轮改变了什么

旧网考古里，“买火车票”以前很容易被简写成：

```text
打开网站
→ 查票
→ 点击购买
```

现在必须改写为：

```text
历史页面壳
→ 历史规则版本
→ 历史渠道预售状态
→ 历史库存 payload
→ passenger identity state
→ order queue
→ seat lock
→ payment commit
→ ticket issue
→ retrieval/gate execution
```

真正重要的保存对象，不只是那张浅蓝/白色的网页。

> **铁路购票是旧 Web 最典型的“页面很容易保存、事务几乎无法完整保存”的系统之一。**

而正是那些 archive 最难保存的瞬间——余票从 1 变 0、订单进入排队、身份证核验失败、支付回调没回来、票终于出票——决定了一个普通人那年春节到底能不能回家。
