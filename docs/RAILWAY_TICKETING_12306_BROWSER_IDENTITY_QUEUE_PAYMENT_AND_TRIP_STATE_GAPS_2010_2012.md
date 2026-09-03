# 12306、实名制与“买到票以后”：2010–2012 中文旧网的 browser / identity / queue / payment / trip state gaps

> 研究对象：2010–2012 年中国铁路实名购票与 12306 互联网售票的公开 Web 执行层。本文不是铁路运输史，而是回答：**一张“有票”页面、一个订单状态或一条网购成功记录，究竟能证明现实乘车链中的哪一步？**

生活史对应研究：

- `tmzncty/how-people-lived/topics/railway-ticketing-mobility-executability-queue-virtualization-and-travel-calendars-china-1979-2026.zh-CN.md`

本文件严格保持本仓约 1995–2015 中文旧网 scope。1996 年铁路内部客票联网只作为理解 12306 的必要前史；2019、2020、2026 的生活后果不在本文主体中展开。

---

## 1. 先固定研究单位：12306 page 不是一次 train trip

铁路票务旧网至少要区分：

- **institution**：原铁道部、铁路局、车站、铁路客票系统运营单位；
- **backend reservation system**：铁路客票发售和预订系统/TRS；
- **public platform/service**：12306 互联网售票、电话订票；
- **site/host**：历史上的 `www.12306.cn`；
- **page/form**：注册、查询、车次列表、确认订单、支付跳转、未完成订单、订单查询；
- **account identity**：12306 注册账号；
- **passenger identity**：实际乘车人及其有效身份证件；
- **inventory state**：某时刻某车次/席别的可售票额；
- **order state**：查询、提交、排队、锁定、取消、失败；
- **payment state**：银行扣款、支付返回、铁路确认；
- **ticket state**：电子客票/纸质票/取票状态；
- **station state**：身份核验、检票、进站；
- **operation state**：列车是否按日运行、晚点/停运；
- **capture/artifact**：一次网页、截图、报道或系统描述；
- **claim**：研究者能安全作出的最小结论。

因此必须固定：

> **`page survived ≠ backend survived ≠ inventory was still saleable ≠ order succeeded ≠ payment settled ≠ ticket usable ≠ passenger boarded`**。

12306 是典型的 **process web（过程型 Web）**：决定现实结果的大量状态在网页之外或在服务器的极短时间窗口里变化。

---

## 2. 前史边界：1996 的“联网售票”不是 2011 的 Internet ticketing

1996-12-20《人民日报》保存的新华社报道说，铁路部门计划实现全国计算机售票联网，使一个窗口能够销售不同方向、车次的客票。[1]

2006 年铁路客票系统 5.0 升级材料又明确区分了车站计算机售票、地区联网售票、全路联网售票等阶段。[2]

这两组证据能证明：

> **铁路内部 seat inventory / ticketing network 在公众 Web 自助购票以前已经长期存在。**

它不能证明：

- 1996 年普通旅客能在家访问这个网络；
- 该系统运行在公共 Internet 上；
- 旅客自己拥有查询/锁座账号；
- 当年任何一个“联网”窗口都能取得全路所有票额。

所以研究旧网时必须把：

```text
internal railway network
≠ public Internet
≠ public Web storefront
```

分开。

否则会把铁路行业信息化错误地写成中国普通用户网络生活的提前大众化。

---

## 3. 2010：实名制先改变“ticket ↔ person”关系，Web 还不是主体

2010 年春运，广铁集团和成都铁路局部分车站试行火车票实名制；同期规则要求部分车票使用有效身份证件购买，并在进站时核对票、证、人。[3][4]

这一步本身并不是 12306 Web 功能，却直接决定后来网站数据模型中为什么不能只保存“购买者”。

至少要区分：

```text
account operator / buyer
≠ passenger
≠ identity document holder
≠ person appearing at station gate
```

当时规则还允许持他人有效身份证件原件代购车票。[5]

因此新增：

### `buyer-passenger identity gap`

网页或订单里的“账号所有者”不一定是乘车人。

### `same-person boarding gap`

真正上车时，系统/工作人员最终要验证的是票面乘车身份与现场乘车人的关系，而不是谁点击了网页。

### `credential fallback gap`

身份证遗失、忘带等情形并不必然意味着行程彻底终止。成都铁路局同期公布了到车站公安制证口办理临时身份证明的条件。[6]

因此：

`required credential exists ≠ traveler must possess that exact physical document at every moment`。

研究历史 UI 时必须寻找 fallback，而不是只看主流程。

---

## 4. 2011-06：公众 Web 售票真正出现，但并不是全路同时切换

2011-06-12，京津城际开始试行互联网售票；6 月 24 日京沪高铁跟进，9 月 30 日扩到全路动车组，11 月 20 日扩到 Z 字头，12 月 10 日扩到 T 字头，12 月中下旬再分批扩到 K 字头和其他列车。[7]

因此必须记录 **service-scope time gap**：

同一个 `12306.cn` host 在 2011 年 6 月、9 月、11 月和 12 月能买的列车范围并不相同。

> **一个 2011 年的页面 capture 不能不带日期地证明“2011 年 12306 已可购买所有火车票”。**

更不能用 2012 年帮助页反向补足 2011-06 的产品范围。

### `route-class eligibility gap`

当时能否网购取决于：

- 日期；
- 列车等级/车次前缀；
- 始发/到达站；
- 是否属于已上线线路；
- 证件类型；
- 开车前剩余时间。

“网站能打开”只是最外层条件。

---

## 5. 注册、乘车人、证件：身份不是一个 input field

2011 年的互联网购票教程和铁路解读显示，首次用户要注册账号并填写姓名、证件号码、电话、邮箱等；网上可使用的有效证件类型又少于 2010 年部分线下实名试点可接受的证件集合。[8][9]

因此新增：

### `channel-specific credential gap`

`station accepts document X ≠ website accepts document X`。

线下售票窗口、电话订票和 Web 可以拥有不同的证件集合。

### `identity-entry error gap`

同期铁路提醒，证件号码输入错误会造成取票或进站问题。[9]

一张历史表单只能证明字段存在，不能证明：

- 输入时是否实时校验；
- 姓名/证件是否与外部库在线比对；
- 错误格式在哪一步才被发现；
- 后来能否修改；
- 账户实名和乘车实名是否共享同一验证状态。

### `proxy-purchase gap`

2011 年规则明确考虑“代人购票”：购票人可替乘车人下单并把订单信息告知对方。[8]

因此旧 Web 中的一个 account session 不应自动映射为一名 traveler。

---

## 6. browser/runtime gap：网页存在，不代表每台当时电脑都能执行

2011-11-20 的记者实测明确提醒，为在 12306 顺利购票需要使用 IE6.0 及以上版本，并称部分 Firefox 等浏览器不能正常显示页面。[10]

同期用户教程还提到根证书安装等要求。[11]

这给本仓增加一个典型的 **historical runtime eligibility** 问题：

```text
HTML response exists
≠ form renders correctly
≠ JS works
≠ certificate chain accepted
≠ bank redirect works
≠ order can be submitted
```

### `browser-eligibility gap`

如果未来找到 2011 页面的 WARC，用现代 Chromium 成功打开，仍不能写成“2011 用户可以这样买票”。

至少要检查：

- IE6/IE7/IE8 DOM/JS 行为；
- TLS/证书兼容；
- 根证书要求；
- cookies/session；
- 第三方银行跳转；
- charset；
- archive rewrite 是否破坏表单 action。

本轮**没有取得 2011 购买流程的完整 HTML/CSS/JS/WARC 与旧 IE 执行证据**，所以只把浏览器要求固定为同期 B 级操作事实，不做 UI reconstruction。

---

## 7. inventory 是时间函数：截图里写“有”不能证明用户点下去仍然有

2011 同期说明中，车次列表显示“有”或具体张数时，用户可以点击预订；成功后才会进入“席位已成功锁定”的状态。[8]

因此至少有：

```text
query response inventory
→ submit request
→ reservation engine processes request
→ seat lock
```

### `inventory-snapshot gap`

一次 capture 的余票数字只能证明**该响应生成时**服务器返回了某个值。

它不能证明：

- 下一秒仍有票；
- 同一票额没有被窗口/电话/其他用户同时竞争；
- 用户提交后一定锁定；
- archive capture 时间等于 backend 查询时间。

### `cross-channel inventory gap`

2012 年前后，窗口、代售点、电话、互联网共同连接客票系统。公共报道可以证明“组成同一服务链条”，但不能从一个 Web 数字推出各渠道在那一刻看到完全相同、无延迟的库存状态。[7]

需要避免把“共享后台”简化成“每个前端完全同步”。

---

## 8. order lock 不是 payment success：30/45 分钟是一种临时权利

2011 年记者实测：用户提交后如果席位成功锁定，需要在 30 分钟内完成网上支付，否则票额自动释放。[8][10]

2012 年初高峰期，支付时限一度从 30 分钟调整到 45 分钟；同期报道出现“银行扣钱但没有出票”的情况。[12]

这里需要把订单至少拆成：

```text
inventory visible
→ submit
→ seat lock
→ unpaid order
→ bank authorization/debit
→ payment callback to railway
→ railway marks paid
→ ticket/order issued
```

由此新增：

### `seat-lock gap`

`submit clicked ≠ seat locked`。

### `payment-debit gap`

`bank debited ≠ railway received successful callback`。

### `ticket-issuance gap`

`railway received payment ≠ historical artifact proves ticket issued`。

### `timeout/release gap`

若支付时间窗口结束，席位可能回到库存；银行侧却可能仍处在扣款/退款处理状态。

这类状态尤其不能靠页面截图倒推，因为支付跳转、银行页面和铁路订单页属于不同系统。

---

## 9. paper / e-ticket / gate gap：2011 的“电子客票”不是所有线路都无纸化

2011 年同期规则说，京津城际、京沪等部分线路可以用二代身份证直接通过自动检票机；但绝大多数网购旅客仍需在开车前换取纸质车票。[8][9]

因此新增：

### `ticket-medium gap`

同一个“网上购票成功”状态可能继续走向：

```text
A. 二代身份证直接检票
B. 先到车站/代售点换纸票 → 再检票
```

### `paper-exchange gap`

网购成功仍不等于旅客完成全部购票劳动。若需要纸票，还要考虑：

- 换票窗口是否开放；
- 证件原件是否到手；
- 排队时间；
- 异地代售点费用/规则；
- 开车前是否留足时间。

因此：

> **“足不出户买票”在 2011 年经常只是“足不出户完成购买阶段”，不等于完全不去售票设施。**

---

## 10. 2012 春运：Web queue 本身成为一个新的历史对象

2012 年 1 月，12306 在高峰时出现日点击数超过 10 亿次的规模；同期铁路后台报道已经把未支付、取消、完成支付等状态分别显示在监控系统中。[13][14]

这说明 12306 不是一张“查询+购买”表单，而是大规模实时状态机。

### 10.1 `load-state gap`

一个页面在凌晨/淡季能正常打开，不证明春运放票时刻能执行。

档案回放几乎天然丢失：

- 当时并发量；
- session 建立失败；
- AJAX/请求超时；
- server-side queue length；
- 银行回调拥塞；
- 页面重试次数。

### 10.2 2012-09：显式排队把“等待”写进网页

9 月升级后的同期记者/用户材料记录，提交热门线路订单后可能进入“大于 30 分钟”的处理队列；有人等待多个 30 分钟后订单仍失败，也有人等待 1 小时 40 分钟才得到结果。[15][16]

由此新增：

### `queue-state gap`

一张“预计等待 30 分钟以上”的 screenshot 不能证明：

- 前方真的固定有多少订单；
- 预计时间单调下降；
- queue position 不会变化；
- 等完必然有票；
- 用户可以安全刷新/关闭页面；
- 系统是否在不同车次共享队列。

同期客服甚至承认部分等待时间表现难以解释。[17]

### `queue-policy version gap`

2012 年 9 月排队功能上线后很快又根据反馈调整。于是：

> **“2012 年 12306 的排队方式”不是一个全年稳定不变的 UI。**

任何 capture 必须精确到日期，最好精确到当天系统版本/新闻背景。

---

## 11. queue virtualization：旧网保存网页，却很难保存“被网页占用的那一个小时”

对生活史来说，12306 最值得研究的不只是技术故障，而是：

```text
物理售票队列
→ 浏览器刷新/登录
→ 后台排队
→ 支付窗口
```

等待从车站转移到家、宿舍、办公室和网吧。

但是 archive 对这种生活时间极不敏感：

- 一张页面只保存状态，不保存用户守了多久；
- 成功者往往没有写长帖；
- 失败和愤怒更容易生成媒体文本；
- 服务器日志和用户 session 通常不公开。

所以新增：

### `friction-retention bias`

旧网更可能留下“系统繁忙”“排了两小时”“扣钱没出票”等异常故事，而不留下几百万次普通顺利交易的主观体验。

因此**投诉材料不能用于估计失败率**，只能用于证明失败机制真实存在。

反过来，铁路公布的“成功售出多少张”也不能证明平均用户体验顺畅。

---

## 12. operation-state gap：票务 Web 的终点甚至不在票务系统里

2008 年冰雪灾害曾造成京广铁路大面积晚点和广州站大量旅客滞留。[18] 这一事件发生在 12306 互联网售票以前，但对状态机边界非常重要：

```text
valid ticket
→ traveler reaches station
→ train actually operates
→ boarding occurs
→ trip completes
```

因此新增：

### `train-operation gap`

即使未来 archive 完整保存一张“订单已完成”的 12306 页面，它仍不能证明：

- 列车当天未停运；
- 旅客实际到站；
- 票证核验成功；
- 旅客实际上车；
- 最终抵达。

**Web archaeology 的 claim 必须停在证据能到达的状态。**

---

## 13. 隐私边界：实名票务 Web 不应为了考古而恢复个人订单

铁路实名订单可能包含：

- 姓名；
- 身份证件号码；
- 手机号；
- 邮箱；
- 出发/到达城市；
- 旅行日期；
- 同订单乘车人；
- 支付记录；
- 订单号；
- 取票/退改记录。

这些数据组合起来可以直接恢复一个普通人的移动轨迹。

因此本仓应坚持：

1. 不用真实身份证号试探历史/残存查询接口；
2. 不重新发布旧订单截图中的完整身份证、手机号、邮箱、订单号；
3. 不批量收集可识别普通人的历史出行记录；
4. 研究页面结构时使用字段名、规则和公开示例，不需要真实旅客数据；
5. 即使 archive 或搜索引擎曾意外保存私人订单，也把它视为 privacy stop condition，而不是“珍贵数据集”。

`archive can expose ≠ research should republish`。

---

## 14. 本轮 claim / evidence matrix

| Claim | Evidence | Grade | Confidence |
|---|---|---:|---|
| 1990s 铁路内部计算机售票网络先于公众 Web 自助售票 | 1996《人民日报》同期报道 + 2006 系统升级材料 | B + B | high |
| 2010 部分车站实名制把票、证、人绑定 | 铁道部/新华社同期通报、媒体规则说明 | A/B | high |
| 临时身份证明构成实名制 fallback | 成都铁路局同期说明 | B（机构信息转引） | high |
| 12306 互联网售票从 2011-06 起分阶段扩到不同列车 | 2012 客服/铁路系统同期说明 | A/B | high |
| 2011 Web 购票要求历史浏览器/证书/网银等执行环境 | 同期记者实测/教程 | B | high |
| 2011 席位锁定后存在 30 分钟支付窗口 | 同期铁路解读与记者实测 | B | high |
| 多数线路网购后仍需纸票，部分高铁可刷二代证 | 同期铁路规则 | B | high |
| 2012 高峰出现支付扣款与铁路订单状态不同步 | 同期报道及铁路解释 | B | high |
| 2012-09 热门线路引入显式 Web 排队，等待后仍可能失败 | 多家同期记者实测/用户材料 | B | high |
| 单一页面不能证明实际乘车完成 | 状态机推论，受票务规则与运输中断反例支持 | D（显式推论） | high |

---

## 15. 已证实 / 高概率 / 不知道

### 已证实

- 铁路客票后台联网远早于公众 Internet 自助购票；
- 2011 年 12306 网络售票按列车类别分阶段扩大；
- 早期网购依赖账号、身份证件、浏览器兼容、支付和常见的线下换票；
- 席位显示、锁定、支付和出票是不同状态；
- 2012 年 Web 高峰真实出现登录/下单拥塞和显式排队；
- 实名票务允许代购，所以 buyer/account ≠ passenger；
- 票务页面本身不能证明现实上车或抵达。

### 高概率但仍需更强原件

- 2011 不同月份的前端 JS/表单结构和浏览器兼容问题应存在明显版本差异；
- 12306 与 TRS/银行之间的状态同步延迟是“扣款未出票”现象的重要技术 seam；
- 2012 排队逻辑在数日/数周内多次调整，单一 capture 很容易把短期实验当成全年规则。

### 不知道

本轮没有可靠取得：

- 2011-06-12 首日完整首页、注册页、查询页、支付页 WARC；
- 同一 2011 session 的全链网络记录；
- 当年 production JS/接口协议；
- TRS 与 12306 的具体内部 API/消息格式；
- 银行支付 callback 的历史协议实现；
- 某一普通用户从“看到余票”到“实际进站”的可公开完整 session；
- 2012 排队算法的源码或可复核服务端实现。

因此不做代码级 reconstruction，也不生成“仿 2011 12306”并冒充历史原件。

---

## 16. Archive 搜索与 stop condition

本轮公开 Web 能找到大量 2011–2012 同期报道、操作教程、记者实测和铁路说明，但**没有取得足以验证整套动态交易流程的 A 级历史 WARC/HTML + backend interaction**。

这不是一个可以靠常识补齐的空白。

尤其：

- 登录后页面通常不易被公共 archive 保存；
- 余票是高频动态状态；
- 支付页跨域到银行；
- 实名订单含私人数据；
- session/cookie/验证码/排队状态天然难以回放；
- archive rewrite 会破坏表单、JS 和跳转。

因此本文件的考古结论应停在：

> **我们可以相当可靠地恢复“公开规则、用户看到的状态类别、部分操作路径和失败机制”，但不能把今天可打开的页面壳当成 2011–2012 的完整交易系统。**

---

## 17. 为什么这改变了中文旧网研究

12306 说明中文旧网不只是内容网页、论坛和 SNS。

大量真正改变生活的 Web 是**状态型基础设施**：

- 高考志愿；
- 求职投递；
- 医院挂号；
- 网银转账；
- 火车票；
- 后来的政务/缴费。

它们的公共 HTML 往往是最容易保存、也最不重要的一层。

真正决定生活结果的是：

```text
identity
+ entitlement
+ dynamic inventory
+ deadline
+ backend lock
+ payment
+ cross-system confirmation
+ offline handoff
```

因此旧网考古若只问“这个页面长什么样”，会系统性高估 archive 对普通生活的可见度。

对火车票来说，最精确的一句边界是：

> **一张幸存的余票页最多证明服务器曾经返回某个可见状态；它不能证明后来有哪个具体的人因此回到了家。**

---

## 18. 来源

1. 《人民日报》1996-12-20 第5版，新华社《铁路部门加紧建设计算机售票网络 两年内将实现全国联网》（开放历史文本镜像）：https://cn.govopendata.com/renminribao/1996/12/20/5/
2. 中国新闻网/新浪，2006-08-28，《中国铁路客票系统升级 有座无票不会再现》：https://news.sina.com.cn/c/2006-08-28/125610849796.shtml
3. 中国青年报，2010-01-09，《今年春运试点火车票实名制》：https://zqb.cyol.com/content/2010-01/09/content_3029696.htm
4. 中国新闻网，2010-01-09，《今年春运试点火车票实名制 可凭20种证件购票》：https://www.chinanews.com.cn/gn/news/2010/01-09/2062947.shtml
5. 广州日报/搜狐，2010-01-10，《广铁集团公布实名制火车票购票进站流程》：https://news.sohu.com/20100110/n269474850.shtml
6. 中国交通广播网/凤凰网，2010-01-18，《成都铁路局：7类情况可现场办理临时身份证明》：https://news.ifeng.com/mainland/special/2010chunyun/ziliao/201001/0118_9288_1515575.shtml
7. 新华网材料转引于中国青年报，2012-01-14，《网络订票为何这么难》：https://zqb.cyol.com/html/2012-01/14/nw.D110000zgqnb_20120114_3-01.htm
8. 重庆晚报/新浪，2011-11-22，《教你一招：如何购票取票改签退票》：https://news.sina.com.cn/o/2011-11-22/052023503122.shtml
9. 中国新闻网，2011-12-07，《“T字头”特快列车实现网络售票 认4种证件》：https://www.chinanews.com/cj/2011/12-07/3514576.shtml
10. 法制晚报/新浪，2011-11-20，《网购火车票 7分钟搞定》：https://news.sina.com.cn/c/2011-11-20/132623495226.shtml
11. 2011-11-18 同期网购教程，保留 IE6+/根证书要求：https://lxs.cncn.com/43987/n172794
12. 东方早报/新浪，2012-01-03，《网购时限导致“吞钱 不吐票” 已延长至45分钟》：https://news.sina.com.cn/c/2012-01-03/074223739863.shtml
13. 中国广播网/中新网，2012-01-13，《12306网站订票和支付系统或将分开运行》：https://www.chinanews.com.cn/cj/2012/01-13/3604380.shtml
14. 中国网络电视台，2012-01-16，《12306订票和支付系统或分开运行 避免网络拥堵》：https://news.cntv.cn/20120116/103423.shtml
15. 新浪科技，2012-09-18，《12306订票排队系统效率低下 被指存多处漏洞》：https://tech.sina.com.cn/i/2012-09-18/00227626106.shtml
16. 新闻晚报/新浪，2012-09-19，《网上排100分钟，等来一张无座票》：https://news.sina.com.cn/o/2012-09-19/125925207377.shtml
17. 扬子晚报/新浪，2012-09-20，《铁道部否认12306网站订票难因方便内部留票》：https://news.sina.com.cn/c/2012-09-20/035825211571.shtml
18. 中国青年报，2008-01-29，《紧急动员：为国为己，今年过年不回家》：https://zqb.cyol.com/content/2008-01/29/content_2050366.htm
