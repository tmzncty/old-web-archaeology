# RAIL_TICKET_QUERY_PORTALS_BROWSER_PAYMENT_AND_BOOKING_STATE_GAPS_2010_2012.md

> 状态：研究笔记 / evidence contract extension  
> 主体范围：**2010–2012 中文 Web 中铁路余票查询、12306 初代互联网售票、账户 / 身份 / 浏览器 / 支付 / 取票状态，以及这些动态状态的 archive gap。**  
> 2000 年铁路后端票务联网与 2009–2010 电话订票只作为必要前史边界；2019 以后候补系统只用于解释后续 state model，不把本仓扩成当代交通平台史。  
> 生活史交叉：`tmzncty/how-people-lived/topics/ticketability-railway-booking-labor-and-mobility-calendar-china-2000-2025.zh-CN.md`

---

## 0. 为什么铁路购票是旧网考古问题

今天看到一个 2011 年的“网上购票”新闻，很容易把当时的网页想成今天 12306 的早期皮肤。

这是危险的。

初代铁路互联网购票真正包含的是一串分布式状态：

```text
用户打开网站
→ 浏览器能否正常工作
→ 注册
→ 邮箱 / 身份信息
→ 查询日期、车次
→ 后端当时是否有库存
→ 尝试下单
→ 席位是否临时锁定
→ 跳转网上银行 / 银联
→ 银行侧是否付款
→ 支付结果是否返回铁路系统
→ 订单是否确认
→ 是否需要换纸票
→ 证件 / 票能否通过进站核验
→ 旅客是否真正上车
```

Web archive 最可能保存的是：

- 首页；
- 帮助页；
- 公告；
- 静态购票规则；
- 某些表单壳；

最难保存的恰好是：

- 某一秒的余票；
- 登录后的账号状态；
- 席位锁定；
- 银行跳转；
- 支付回调；
- 订单确认；
- 历史候补 / 排队位置；
- 某个普通人的真实乘车结果。

所以本篇的核心边界是：

> **page survived ≠ historical inventory survived ≠ transaction executed ≠ journey happened**。

---

## 1. 研究单位

按照 `docs/METHOD.md`，本案例至少拆成：

- **rail ticketing backend**：铁路客票库存与发售系统；
- **public information site**：公众时刻 / 票价 / 余票查询站点；
- **ticket-sale scope**：某一历史日期实际开放互联网售票的车种 / 路线范围；
- **account**：一个注册用户；
- **traveler identity**：订单内实际乘车人的证件身份；
- **query**：出发站、到达站、日期等一次查询；
- **inventory result**：该次查询在该秒返回的余票状态；
- **order attempt**：用户提交的订单动作；
- **seat lock**：系统暂时保留的席位状态；
- **payment session**：铁路站点与银行 / 支付系统之间的一次支付链；
- **ticket contract / confirmed order**：铁路系统确认的有效购票结果；
- **pickup / gate mode**：纸票换取、二代身份证直接检票等不同执行方式；
- **capture**：档案在某时刻保存的一份页面表示；
- **claim**：依据证据作出的最小陈述。

必须避免把：

> `www.12306.cn existed`

直接写成：

> `all Chinese railway tickets were purchasable online at that date`。

2011 年互联网售票是分车种、分阶段扩展的。

---

# 第一部分：必要前史——后端联网不等于公众 Web 售票

## 2. 2000：跨站票务联网先发生在铁路内部

2000 年 9 月同期报道说，全国铁路首批 44 个火车站将实行联网售票，联网车站之间可以办理返程票、连程票与异地车票。

来源：

- 《全国铁路首批44个大站票务将联网》，2000-09-07：<https://news.sina.com.cn/china/2000-09-07/124805.html>

### 证据等级

**B：同期媒体报道。**

### 本仓保留的边界

这证明：

> **铁路座位库存可以在公众 Internet 售票之前通过内部计算机系统实现跨站处理。**

不能写：

- 2000 普通家庭已经在网上买全国火车票；
- 44 站联网等于全国所有车站实时互售；
- 今天 12306 的页面 / API 可以直接代表当时后台结构。

旧网考古需要区分：

```text
backend network
public Web information layer
public Web transaction layer
```

它们有不同的起始时间。

---

## 3. 2010 电话订票：另一套非 Web 的远程交易接口

2010 年《中国青年报》对春运实名制与电话订票的同期调查记录：成都电话订票试运行时，短时间内涌入大量呼叫；实名制需要输入身份证号码，又延长了单次电话处理时间。

来源：

- 《火车票实名制解决啥问题》，2010-03-02：<https://zqb.cyol.com/content/2010-03/02/content_3107271.htm>

### 本仓为什么要记录它

因为如果只看 Web archive，会误以为：

```text
车站窗口
→ 12306 Web
```

实际上当时还存在：

```text
车站窗口
代售点
电话订票
Web 信息查询
随后才逐步出现 Web 交易
```

这些渠道可以共享或竞争同一票务库存，但它们的用户接口、故障模式和可保存性不同。

电话 busy state 几乎不会进入 Web archive。

因此新增：

### channel-state invisibility

同一历史时刻：

- Web 可能正常打开；
- 电话可能全部占线；
- 窗口可能排长队；
- 某代售点可能已经售完；

单个网页 capture 不能代表“当时买票难不难”。

---

# 第二部分：2010——查询站点与交易站点不要合并

## 4. 12306 最初的重要功能之一是“看见”

2010 年开通的铁路客户服务网站首先提供了列车时刻、票价、余票、代售点、正晚点等公开查询。

本轮能够可靠确认的是：在正式普遍互联网售票展开以前，公众 Web 已经先承担铁路信息查询层。

### 最小 claim

> **2010 年公众可以通过铁路客户服务网站获取一部分动态票务 / 运行信息。**

### 不能扩写

> **“2010 年用户已经可以在 12306 上购买所有列车车票。”**

这里必须分开：

```text
information visibility
transaction capability
```

这对 archive 也非常关键：

一个余票查询表单即使被保存，也不表示档案保存了当时后台库存数据库。

---

## 5. query-state gap

一次余票查询至少依赖：

```text
query timestamp
origin
 destination
travel date
train scope
seat class
backend inventory snapshot
cache / response timing
```

历史 HTML 常常只保存：

- 输入框；
- “查询”按钮；
- JS；
- 空表格；

而不会保存：

- 某位用户 2010-02-05 10:03 输入的具体查询；
- 服务器在那一秒返回的库存；
- 几秒后库存如何变化。

所以固定：

> `query form survived ≠ historical query survived`

以及：

> `query form survived ≠ historical inventory result survived`

---

## 6. inventory-state gap

铁路余票是一种高频可变状态。

同一个 URL 在一分钟内可能依次显示：

```text
有票
→ 无票
→ 退票释放
→ 再次无票
```

因此任何历史 capture 都只能回答：

> “这个 capture 保存时，页面呈现了什么？”

不能自动回答：

> “那一天一直有票 / 一直无票。”

更不能用今天调用到的数据库答案填补 2011 历史库存。

---

# 第三部分：2011——Internet 售票是一套逐步展开的 transaction stack

## 7. 2011-06：京津城际首先试行，不能倒推全国

2011 年 6 月 12 日，京津城际率先试行互联网售票。

同期记者的购票观察保存了当时用户侧流程：

- 注册；
- 身份信息；
- 邮箱激活；
- 查询；
- 下单；
- 网上支付；
- 在规定时间内完成付款；
- 二代身份证在满足条件时可直接检票，否则存在纸票换取路径。

来源：

- 北京晚报 / 中新网，《京津城铁网购车票仅需2分钟 持二代证可无票登车》，2011-06-12：<https://www.chinanews.com.cn/cj/2011/06-12/3105357_2.shtml>

### 证据等级

**B：同期记者操作观察 + 铁路规则说明。**

### rollout-scope gap

这一案例只证明：

> `京津城际在 2011-06-12 开放互联网售票`

不能写成：

> `2011-06-12 全国所有铁路互联网售票`

后续动车组、Z 字头、T 字头和其他列车是继续分阶段开放的。

因此历史研究必须保存：

- 日期；
- 车种；
- 路线 / 铁路局范围；
- 当日政策版本。

今天“12306 可以买全国大部分列车”的事实不能倒投回 2011-06。

---

## 8. account-state gap

一个注册页面可以被 archive 保存，但普通用户账户状态通常不会。

历史上真正决定能否继续的是：

```text
账号是否注册成功
邮箱是否激活
密码是否有效
身份证信息是否通过
联系人是否已保存
登录 session 是否仍在
```

这些状态有几个特点：

1. 通常需要登录；
2. 与个人身份相关；
3. 经常存储于后端数据库；
4. 不应为了考古完整度从泄露数据库中恢复。

所以：

> **registration page survived ≠ historical account survived**。

这是合理的 privacy-preserving absence，而不是 archive 应该强行补齐的“缺陷”。

---

## 9. browser/runtime gap：2011 的“网页能开”不等于“网页能买票”

2011 年 6 月《新京报》记者实际测试：Chrome、Firefox、Safari、Opera 进入购票流程时出现不能正常登录等问题，而 IE9、360 浏览器可正常购票。铁路客服当时表示，网站基于 IE 标准制作，支持 IE6 及以上版本。

来源：

- 《非IE用户被指无法在线订火车票》，2011-06-15：<https://news.sina.com.cn/c/2011-06-15/084622643844.shtml>

### 证据等级

**B：同期多浏览器记者实测 + 客服说明。**

### 不能滥用的数字

报道依据浏览器市场份额进一步推算可能受影响的用户数量。这个推算不是对“实际购票失败人数”的直接测量，本仓不采用它作为人口规模证据。

### 本仓固定边界

> `HTML loads in modern Chromium ≠ historical transaction worked in 2011 browser environment`

涉及 12306 早期页面复原时必须记录：

- IE 版本假设；
- document mode；
- JS / ActiveX / 兼容层；
- 证书要求；
- 支付跳转；
- charset；
- archive rewrite 是否改变脚本或链接。

没有旧浏览器验证，现代截图只能写：

> “modern replay / reconstruction”

不能写：

> “2011 用户当时看到的真实浏览体验”。

---

## 10. certificate / trust runtime

2011 年互联网购票报道与用户指南显示，首次使用过程还涉及安全证书、实名信息与网上支付等环境要求。

这些要素说明早期交易页的可执行性不只是 HTML / CSS 问题：

```text
浏览器
→ TLS / certificate trust
→ 网站脚本
→ 身份字段
→ 银行支付环境
```

共同构成 runtime。

本轮没有提交任何历史证书文件，也没有用今天证书链推测 2011 证书链。

因此当前只保留：

> **当时用户侧购票过程存在需要处理证书 / 信任环境的操作。**

若以后恢复 2011 原始 certificate artifact，必须单独记录：

- 证书序列号；
- issuer；
- validity；
- 原始域名；
- 浏览器信任结果；
- 是否为 archive / reconstruction 环境。

---

# 第四部分：订单与支付——最危险的“一个成功按钮”幻觉

## 11. 最小交易状态机

至少用下面的状态链理解一次 2011 网上购票：

```text
public page reachable
→ login valid
→ query submitted
→ inventory result returned
→ train/seat chosen
→ order submitted
→ seat lock acquired
→ payment session created
→ bank authorizes / debits
→ payment callback reaches railway system
→ railway order confirmed
→ confirmation delivered
→ paper-ticket / ID-gate path available
→ traveler completes station entry
```

任何一箭头都可能失败。

所以“网上购票成功率”不能由：

- 首页 uptime；
- 查询成功；
- 银行扣款；

单独代表。

---

## 12. seat-lock gap

同期报道指出，用户下单以后必须在限定时间内完成支付，否则席位会重新释放。

这说明 `有票` 与 `你的票` 之间存在临时状态：

```text
inventory visible
→ seat temporarily held
→ payment deadline
→ confirm / release
```

历史 archive 几乎不可能可靠保存某个普通人当时的 seat lock。

因此固定：

> **availability result ≠ seat lock**

以及：

> **seat lock ≠ confirmed ticket**。

---

## 13. bank-redirect gap 与 payment-confirmation gap

铁路交易需要跨站点 / 跨机构进入网上银行或支付页面。

2011 年底同期报道出现用户在网银侧发生扣款或重复操作以后，却无法立即确认铁路订单结果的问题；铁路方面解释了重复操作、支付返回与订单状态之间可能发生的异常。

来源：

- 《铁路部门称网络购票误操作可能导致重复扣款》，2011-12-30：<https://news.sina.cn/sa/2011-12-30/detail-ikftssap4343178.d.html>

### 证据等级

**B：同期用户问题 + 铁路方面解释。**

### 本仓固定

> **bank debit ≠ railway order confirmation**。

同样：

> `payment page capture ≠ payment session`

> `payment session ≠ bank authorization`

> `bank authorization ≠ callback received`

这类跨域流程也是 archive 特别容易断裂的地方：

- archive 可能不抓银行页面；
- HTTPS / session token 无法复现；
- POST body 不会成为公共 URL；
- callback 只发生在服务器之间；
- 普通人的订单与银行卡数据不应进入公开仓库。

---

## 14. success-page bias

公开教程和媒体报道天然喜欢保存“购买成功”的演示：

```text
注册
→ 查询
→ 付款
→ 成功
```

但真实用户更常产生的边缘状态可能是：

- 页面超时；
- 重复点击；
- 银行扣款但返回失败；
- 订单仍显示处理中；
- 席位释放；
- 邮件 / 短信没收到；
- 换浏览器重来。

这产生 **success-page bias**：

> 保存得最清楚的“标准成功流程”，未必是历史上最常见的失败边界。

所以旧网案例需要主动找：

- 同期求助帖；
- 客服问答；
- 错误截图；
- 媒体故障报道；

而不能只用官方教程复原用户经验。

---

# 第五部分：身份、纸票与车站——交易网页后面还有一段物理执行

## 15. confirmed order ≠ journey

2011 各线路规则并不完全相同。一部分二代身份证用户在具备设备的车站 / 线路可以直接凭证件进站；另一些情况仍需要换取纸质车票。

例如 2011 年 9 月武广高铁互联网售票同期报道明确要求网上成功后按规定换取纸质车票，再凭纸票检票。

来源：

- 《今起可网上购买武广高铁车票 车票预售期为10天》，2011-09-20：<https://news.sohu.com/20110920/n319917026.shtml>

所以：

> **online purchase capability ≠ paperless travel capability**。

历史复原需要单独记录：

- route / station；
- ticket rule version；
- traveler document type；
- gate equipment availability；
- 是否换纸票；
- 是否有时间窗口。

---

## 16. identity-verification gap

互联网售票将账户、订单与乘车人证件字段连接起来。

但公开 Web archive 最多保存规则，通常不会保存：

- 某人的身份证号；
- 某次实名核验结果；
- 临时身份证明；
- 车站闸机日志；
- 真实乘车记录。

这类缺失必须视为隐私边界。

### 禁止

不得为了“还原完整交易”而：

- 搜索泄露的 12306 用户数据库；
- 公开历史普通用户身份证号码；
- 拼接银行卡 / 电话 / 邮箱；
- 重放普通人的历史登录凭据。

平台结构研究不需要重新暴露个人身份。

---

# 第六部分：为什么今天看到 12306 不能代表 2011 12306

## 17. 同一域名包含多代系统

`12306.cn` 是长期存续域名，但它背后的：

- 页面布局；
- JS；
- 查询接口；
- 登录系统；
- 支付渠道；
- 证件规则；
- 预售期；
- 售票车种范围；
- 候补；
- 手机端；
- 自动提交；

都在持续变化。

因此同一 domain 不能被当作一个静态历史对象。

必须至少写：

```text
host + capture datetime + page function + rollout scope
```

而不是只写：

> “12306 页面”。

---

## 18. mutable backend / stable URL problem

铁路查询 URL 或页面入口可以多年不变，但后台数据库状态每秒变化。

这是一类典型：

> **stable public locator + mutable private state**

的旧网对象。

类似问题也会出现在：

- 医院号源；
- 求职职位；
- 二手 listing；
- 房源；
- 餐馆库存；

但铁路席位的变化速度更快，且同一席位具有非常强的排他性。

所以 railway inventory archaeology 不能只靠页面 URL。

---

# 第七部分：2019 以后只作为 state-model 后续边界

## 19. 候补把“用户刷新行为”变成服务器状态

2019 以后正式候补逐步把一部分“不断刷新余票”的行为变成：

```text
用户提交可接受需求
→ 服务端保存 waitlist state
→ 座位释放 / 新增运力
→ 自动兑现或失败
```

2024 年候补进一步允许最多 60 个“日期 + 车次”组合，并可接受新增列车。

来源：

- 人民日报，2024-01-12：<https://society.people.com.cn/n1/2024/0112/c1008-40157290.html>

本仓不继续研究 2020s 产品史，只保留一个对旧网方法很重要的比较：

### query-state → queue-state

2011 主要需要捕获“这一秒查询到了什么”；

后来的候补还需要理解：

- 你进入了哪个队列；
- 什么时候提交；
- 有哪些备选；
- 什么时候兑现；
- 为什么失败。

这种状态同样几乎全部在登录后的数据库里。

---

## 20. waitlist-outcome gap

即使公开页面保存了“候补功能说明”，也不能据此知道：

- 某用户是否提交候补；
- 排在什么位置；
- 哪个组合兑现；
- 是退票释放还是新增列车；
- 最后是否实际乘车。

因此：

> `waitlist feature exists ≠ a particular user was waitlisted`

> `waitlist submitted ≠ ticket fulfilled`

> `ticket fulfilled ≠ journey completed`

---

# 第八部分：证据表

## 21. 当前关键证据

| 日期 | 对象 | 可支持的窄 claim | 等级 | 当前缺口 |
|---|---|---|---|---|
| 2000-09 | 44 站票务联网 | 内部票务联网可支持部分返程 / 连程 / 异地票 | B | 缺系统原始技术文档 / 客户端 |
| 2010-03 | 电话订票 + 实名试点 | 电话渠道存在高并发占线、证件输入与取票流程 | B | 缺 IVR 原始录音 / 完整系统说明 |
| 2010 | 12306 信息查询 | Web 查询层先于普遍 Web 交易层 | B/待补 A | 缺已验证早期 capture |
| 2011-06 | 京津城际网售 | 注册、实名、邮箱、查询、支付、身份证 / 取票形成交易栈 | B | 缺初代原始 HTML/JS |
| 2011-06 | 浏览器兼容 | 同期记者测试非 IE 浏览器出现购票障碍 | B | 缺历史 VM 重放 |
| 2011-09 | 武广高铁网售 | 当时该线路成功网购后仍需按规则换纸票 | B | 缺线路规则原文 capture |
| 2011-12 | 支付异常 | 网银扣款与铁路订单确认可出现不同步 / 用户困惑 | B | 私有订单不可复原 |
| 2024 | 候补升级 | 后来的服务端 queue state 可保存多日期 / 多车次偏好 | A/B | 不属于本仓主体年代，仅作比较 |

---

# 第九部分：需要在 capture 层记录什么

## 22. 对铁路查询 / 购票页的 capture checklist

若以后取得 2010–2012 archive capture，至少记录：

### Resource

- `original_url`
- `capture_url`
- `capture_datetime`
- `archive_source`
- HTTP status
- redirect chain

### Page role

- 首页；
- 查询页；
- 注册页；
- 登录页；
- 购票页；
- 支付说明；
- 取票规则；
- 公告；
- 错误页。

### Runtime

- Content-Type；
- charset；
- CSS / JS 是否完整；
- frames / iframe；
- 是否 IE-only；
- 是否有浏览器嗅探；
- certificate / HTTPS 状态；
- 表单 method；
- action URL；
- archive rewrite 是否破坏脚本；
- POST 是否不可重放。

### Historical scope

- 当日开放哪些车种；
- 服务时间；
- 预售期；
- 支持证件；
- 支付渠道；
- 取票 / 身份证直接进站条件。

### Explicit unknowns

- 当秒真实余票；
- 私有账户；
- 订单；
- 支付；
- 最终乘车。

---

# 第十部分：新的 archive-gap 分类

## 23. `query-state gap`

表单存在，但历史查询参数 / 响应没有保存。

## 24. `inventory-state gap`

页面存在，但高频变化的席位库存没有可靠历史快照。

## 25. `rollout-scope gap`

今天同一功能覆盖全国，但历史日期只开放部分线路 / 车种。

## 26. `browser-runtime gap`

现代浏览器回放成功，不能证明 2011 历史浏览器交易成功；反之现代回放失败，也不能证明当年失败。

## 27. `certificate-runtime gap`

页面 HTML 幸存，但历史信任链 / 安全证书 / 浏览器证书处理环境缺失。

## 28. `account-state gap`

注册 / 登录页幸存，普通人的实际账号状态不应公开恢复。

## 29. `seat-lock gap`

查询结果与最终订单之间的临时席位保留状态不可见。

## 30. `bank-redirect gap`

支付跳转跨域、带 session 与 POST，普通 Web archive 通常无法完整复现。

## 31. `payment-confirmation gap`

银行侧扣款和铁路侧订单确认是两个状态，单边 artifact 不能代表另一边。

## 32. `pickup/gate gap`

网上买票成功以后，纸票 / 身份证 / 车站设备是否真正完成下一步通常不在 Web artifact 中。

## 33. `journey-outcome gap`

车票确认不等于旅客最终上车、到达或完成中转。

## 34. `channel-state gap`

同一时刻电话、窗口、代售点与 Web 的可用性可能完全不同，Web capture 不能代表整个购票生态。

---

# 第十一部分：最重要的“不要写”

## 35. 不要把 feature existence 写成 population adoption

错误：

> “2011 年中国人已经开始网上买火车票。”

更好：

> “2011 年互联网售票从部分线路 / 车种逐步扩大；同期记者已经记录到真实 Web 购票流程和浏览器兼容障碍。”

前者会把 rollout 和 population adoption 混在一起。

---

## 36. 不要把今天页面反投回历史

错误：

> “12306 现在这样，所以 2011 也这样。”

必须检查：

- 历史 capture；
- 当年帮助页；
- 同期教程；
- 浏览器环境；
- 当时车种范围。

---

## 37. 不要用历史失败状态去猎奇普通用户

用户支付异常、证件困难、抢票失败是研究制度和技术接口的证据，不是重新曝光个人身份的理由。

引用普通人时：

- 只保留支持 claim 的最小信息；
- 不重新传播身份证、银行卡、手机号、邮箱；
- 不抓泄露数据库；
- 不复原私人订单。

---

# 第十二部分：跨国前史只做边界，不扩 scope

## 38. 法国 Minitel 证明“远程铁路交易”不是 WWW 专属

1990 年《世界报》同期报道：法国部分地区用户已经可以通过 Minitel 查询 SNCF 时刻、预订座位，并通过带安全支付条件的终端完成付款；同年 SNCF 新的 SOCRATE 预订中心计划向车站、旅行社、自动机和 Minitel 提供统一的时刻、票价、预订和出票能力。

来源：

- Le Monde, 1990-02-21：<https://www.lemonde.fr/archives/article/1990/02/21/monetique-les-dispositifs-anti-fraudeurs-se-multiplient-pour-payer-par-minitel-en-toute-securite_3957116_1819218.html>
- Le Monde, 1990-07-12：<https://www.lemonde.fr/archives/article/1990/07/12/la-sncf-inaugure-un-nouveau-systeme-de-reservation_3991275_1819218.html>

这两条只作为比较边界，主要分析写在 `how-people-lived`。

本仓不把 Minitel 纳入中文旧网主体案例。

它只帮助固定：

> **remote self-service ticketing can be built on networks other than the WWW**。

因此中国 12306 的历史特殊性不能写成“人类第一次远程买火车票”，而要具体研究中国铁路内部票务系统、中文 Web、实名证件、IE 环境、网银和高峰售票如何组合。

---

# 第十三部分：当前结论

## 39. 已证实

- 中国铁路后端跨站票务联网早于公众 12306 Internet 售票；
- 2010 前后电话订票、窗口、代售点与 Web 信息查询并存；
- 2011 年互联网售票分阶段展开，不应把单条线路开通日当成全国统一状态；
- 同期记者明确观察到初代购票流程包含注册、身份、查询、支付等多个状态；
- 同期多浏览器实测证明 2011 初代系统存在明显 browser compatibility boundary；
- 同期报道证明银行支付侧状态与铁路订单侧状态不能简单视为同一个成功状态；
- 部分线路在网购成功以后仍需要纸票执行；
- 大量关键状态位于登录后数据库、支付系统与车站执行层，公共 Web archive 不可能完整覆盖。

## 40. 高概率 / 可继续验证

- 若取得 2010–2012 原始 capture，可进一步恢复查询表单、JS、charset、浏览器嗅探、支付入口与历史帮助页；
- IE-only / certificate 环境很可能使现代 archive replay 与历史真实执行出现明显差异；
- 不同铁路局 / 线路的 rollout 细节可能比全国性新闻摘要更复杂，应逐日期核验。

## 41. 不知道

本轮仍不知道：

- 某个 2011 普通用户在特定秒实际看见了什么余票；
- 初代全部交易 JS / 后端 API 的完整版本历史；
- 一次支付异常的内部服务器事件链；
- 新闻报道中的每个成功 / 失败用户最终是否乘车；
- 多少用户因浏览器兼容问题最终放弃或转窗口。

这些不知道是正式结论，不用猜测补齐。

---

# 42. 下一步最有价值的 archaeological target

最值得找的不是又一篇“12306 正式上线”报道，而是一个 **2011–2012 多时点原生执行链**：

```text
用户在论坛 / 博客说准备网上买票
→ 具体浏览器 / 证书问题
→ 查询结果
→ 下单
→ 支付成功 / 异常
→ 订单确认
→ 取纸票 / 身份证进站
→ 回来报告是否真正上车
```

如果能找到，并且个人隐私边界允许最小引用，它可以把旧网考古从：

> “这个购票页面存在过”

推进到：

> **“这个页面后面的跨系统状态，怎样真实决定了一个普通人那天能不能离开一座城市。”**
