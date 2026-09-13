# 12306 早期网络售票：IE-only、15 分钟席位锁、银行支付、纸票桥接与事务状态丢失，2011–2012

> Scope：中文旧网约 1995–2015 范围内的铁路 12306 早期 Web 事务层，重点研究 **2011 年从“查询站”转向大规模在线购票时，普通用户实际需要跨过哪些浏览器、身份、支付与线下终端边界**。  
> 交叉生活史包：`tmzncty/how-people-lived/sources/railway-ticket-access-queues-reservation-infrastructure-and-mobility-commitment-china-2005-2025.zh-CN.md`。  
> 本文不是 12306 技术发展史，也不宣称已经复原 2011 年网站。当前价值是建立可复核的 transaction-state model、historical locator、客户端约束和 archive gap。

---

## 0. 去重：不再重复“页面不等于事务”，而是把一次铁路购票的具体状态拆出来

仓库已经反复建立：

```text
page != account
page != transaction
locator != verified capture
current live legacy page != historical memento
```

所以本轮不再换词重造一个一般性“状态缺口”。

只回答更具体的七个问题：

1. 2011 年 12306 网络售票的 historical locator 和公开页面结构可以确认到什么程度？
2. 当时“查询余票”和“真正持有一个席位”之间有哪些状态？
3. 为什么 **15 分钟**是一个关键历史事务时钟？
4. 网站为什么不能脱离银行支付、短信 / 邮件、身份证和车站闸机单独理解？
5. 当时 IE / 根证书 / SSL / JavaScript 条件怎样影响可执行性？
6. 为什么网上买到票以后，很多车站仍必须换纸质票？
7. Web archive 即使保存页面，哪些真正决定“票是不是你的”的状态仍然会消失？

---

## 1. Historical identity 与 locator

### 1.1 当前能够确认的 2011 historical locator

多份 2011 同期材料都直接给出：

```text
http://www.12306.cn/
http://www.12306.cn/mormhweb/kyfw/
http://www.12306.cn/mormhweb/kyfw/ypcx/
```

其中：

- `mormhweb/kyfw/` 被同期博客直接称为 12306 购票 / 客运服务入口；
- `mormhweb/kyfw/ypcx/` 在 2011 年旅行计划、博客和铁路报道中作为余票 / 时刻查询入口出现。

### 1.2 当前访问状态不能冒充 2011 页面

本轮直接检查：

```text
https://www.12306.cn/mormhweb/
```

现在会导向现代 `https://www.12306.cn/index/`。

而：

```text
https://www.12306.cn/mormhweb/kyfw/
```

目前仍返回一个非常简化的“铁路客户服务中心--客运服务”legacy shell，页脚显示：

```text
版权所有 © 2008-2018 中国铁路信息技术中心 中国铁道科学研究院
```

但这只能证明**当前服务器仍保留该历史路径族的某种 live representation**。

不能写成：

> 这就是 2011 年用户看到的页面。

因为我们没有：

- 2011 capture datetime；
- 2011 HTTP headers；
- 当年完整 DOM；
- 当年 CSS / JS / 图片资源；
- 当年登录态；
- 当年购票子系统真实返回。

### 当前 live locator

- https://www.12306.cn/mormhweb/
- https://www.12306.cn/mormhweb/kyfw/

### 证据等级

- **A（当前 live artifact，仅证明 2026 当前响应）**；
- 对 2011 UI 只能作为 historical locator continuity，不能作为历史 capture。

---

## 2. 2011 以前的 12306 信息层：事务上线以前，查询已经进入旅行计划

一个 2011 年 3 月 6 日的普通 WordPress 旅行计划非常适合作为平台用途边界证据。

作者组织 8 人从上海去武汉，列出备选车次和价格，并明确让同行者使用铁路官方系统：

```text
http://www.12306.cn/mormhweb/kyfw/ypcx/
```

查询车票。

当时计划中的 6 张票仍由一名成员统一购买。

这说明：

```text
web information access
can precede
web transaction access
```

12306 在大规模网上售票之前，已经可以进入普通人的：

- 选车次；
- 比较时间；
- 协调同行人；
- 决定谁负责买票

这些日常动作。

### 证据

- **A-/B+（2011 同期普通用户公开博客；证明该作者当时的计划与 URL 使用，不外推总体）**：WordPress，《3.18-3.20 武汉计划》，2011-03-06。  
  https://vivienwdd.wordpress.com/

另一个 2011 年 1 月的博客园开发者学习日志，也把同一 `ypcx` URL 当作当时可用的铁路查询入口收录。

- **B（2011 同期个人技术笔记）**：博客园 Smalltalk，2011-01-06。  
  https://www.cnblogs.com/Smalltalk/archive/2011/01/06/1927626.html

---

## 3. 2011 网络售票的最小 transaction state machine

2011 年 6–12 月大量同期报道足以恢复一个不依赖截图的最小事务模型。

```text
S0: 未登录 / 未注册
↓
S1: 网站实名注册
↓
S2: 查询日期 / 发到站 / 车次 / 席别
↓
S3: 系统发现可售库存
↓
S4: 提交订单 / seat lock
↓
S5: 15 分钟支付窗口
↓
S6a: 银行确认支付成功
S6b: 超时未支付 → seat release
↓
S7: 12306 订单确认 + SMS / email
↓
S8a: 符合条件线路可用二代身份证直接进站
S8b: 其他车站 / 证件 / 票种需要换纸质车票
↓
S9: 线下检票 / 乘车
```

这个模型比“网页上有购票按钮”重要得多。

因为用户是否真正拥有未来席位，取决于状态是不是从 `S4` 走到了 `S6a`。

---

## 4. Artifact family A：15 分钟 seat lock 是早期 12306 的核心时间状态

2011 年 9 月上海的记者实测记录，选择车次和席别以后页面提示“席位已成功锁定”，要求在 15 分钟内完成网上支付。

青岛的同期体验报道同样观察到：如果 15 分钟内不支付，系统会自动把席位释放给其他旅客。

成都铁路局同期公布的规则也明确：预订成功后须在 15 分钟内完成付款，逾期网站自动取消所预订席位。

因此：

```text
availability shown
!=
seat locked
!=
seat paid
!=
travel completed
```

本轮将这一具体历史对象记为：

**`ephemeral seat lock / 瞬时席位锁`**。

它不是一个一般性理论新词，而是 archive 需要特别处理的**计时事务状态**。

### 证据

- **B+（2011 同期记者实测）**：新闻晚报，2011-09-22，《沪宁沪杭高铁今起网上售票》。  
  https://news.sohu.com/20110922/n320218494.shtml
- **B+（2011 同期记者实测）**：半岛都市报，2011-09-24，《国庆青岛4.3万人乘火车出行 网购火车票付款慢》。  
  https://news.sina.com.cn/o/2011-09-24/042023209144.shtml
- **B+/A-（铁路局规则经同期媒体）**：成都日报，2011-09-20，《凭4种证件购票 实行网银付费》。  
  https://news.sina.com.cn/o/2011-09-20/031023182277.shtml

### Archive consequence

即使未来取得一份完整 `S4` 页面 HTML，也不意味着恢复了“这个席位”。

必须承认：

```text
seat_lock_id
lock_created_at
lock_expires_at
current_inventory
payment_callback_state
```

很可能全部只存在于服务器 / 会话 / 数据库中。

因此：

> **A page capture can preserve the sentence “席位已锁定”，但不能证明 archive 保存了当年那个锁本身。**

---

## 5. Artifact family B：IE-only 与根证书——网站存在，但并非所有联网用户都能执行事务

2011 年 6 月《新京报》记者实测 12306 京津城际网络售票：

- Chrome 无法正常订票；
- Firefox 无法正常订票；
- Safari 无法正常订票；
- Opera 无法正常订票；
- IE9 和 360 浏览器可以进入；
- 铁路客服明确表示，当时网站按 IE 标准制作，仅支持 IE6 及以上版本。

同期购票报道又记录，第一次购票需要按网页提示安装“根证书”。

因此 M3 浏览环境实验未来至少必须包含：

```yaml
browser_assumptions:
  ie6_plus_expected: true
  non_ie_failure_reported: true
  root_certificate_installation_reported: true
  ssl_behavior_version_sensitive: true
```

### 证据

- **B+（2011 同期记者测试 + 铁路客服）**：新京报，2011-06-15，《非IE用户被指无法在线订火车票》。  
  https://news.sina.com.cn/c/2011-06-15/084622643844.shtml
- **B+（2011 同期记者体验）**：新闻晚报，2011-09-22。  
  https://news.sohu.com/20110922/n320218494.shtml

### 方法意义

未来如果一个 archive replay 在 modern Chromium 中可以显示：

```text
查询按钮
车次列表
订单页面
```

也不能直接写：

> “2011 用户可以这样操作。”

因为历史可执行性还依赖：

- IE document mode；
- SSL / certificate trust；
- iframe mixed scheme 行为；
- JavaScript 日期控件；
- 银行支付页面兼容性。

---

## 6. Artifact family C：2011 普通开发者留下了一个非常罕见的“跨浏览器拼装事务”自述

2011 年 11 月 22 日，博客园用户 `longware` 发表一篇同期短文，直接给出：

```text
http://www.12306.cn/mormhweb/kyfw/
```

并描述自己的购票问题。

按研究必要最小化，只保留操作层结论：

- 作者认为当时 HTTP 页面嵌套 HTTPS iframe 在 IE 中经常打不开；
- IE9 下日期选择器经常失效；
- 自己采取“Firefox 中订票 → IE 中付款”的混合流程；
- 支付完成后，在另一个浏览器再次点击成功状态时又收到短信，作者因此怀疑短信发送逻辑没有正确去重；
- 订单 / 已订票查询也出现和预期不一致的行为。

### 证据

- **B（2011 同期第一人称技术博客；强在具体操作，弱在不能代表全体用户）**：博客园 longware，2011-11-22，《刚有人谈铁-道-部，一起来说说12306购票系统吧》。  
  https://www.cnblogs.com/longware/archive/2011/11/22/13382228.html

### 为什么它很值钱

官方帮助页通常给出理想流程：

```text
browser
→ order
→ bank
→ success
```

这个普通用户材料却显示真实事务可以变成：

```text
Firefox: 选日期 / 订票
→ IE: 进入支付
→ bank page
→ 回到不同浏览器确认
→ notification side effect
```

因此 historical transaction unit 不能默认等于“一个浏览器 tab 内从头到尾完成”。

这属于：

**`cross-client transaction stitching / 跨客户端拼装事务`**。

它不是说该行为普遍，而是证明**当兼容性失败时，普通用户会自己把多个客户端拼成一条可工作的事务路径。**

---

## 7. 12306 不能作为一个单域名系统考古：事务跨越银行、短信/邮件与车站终端

2011 年网络购票要求网上支付。

因此完整事务实际跨越：

```text
12306 Web
→ seat lock / order state
→ bank / UnionPay payment
→ callback to railway state
→ SMS / email notification
→ station ticket machine / window
→ ID verification / gate
```

本轮将这个具体结构记为：

**`cross-domain transaction dependency / 跨域事务依赖`**。

这里的“domain”既包括 Web 域名，也包括非 Web 系统。

### 2011 支付条件

成都铁路局同期规则称，用户需要开通网上银行业务的银行卡或相应银联支付能力；在开始支付、未完成之前，不能再次购买其他车票。

换句话说：

```text
12306 account access
!=
payment capability
```

### Archive consequence

即使 12306 HTML 保存良好，如果以下任一层缺失：

- 银行页面；
- payment token；
- callback endpoint；
- session cookie；
- SMS gateway；
- station database；

都不可能真正 replay 当年交易。

因此 M3 应明确区分：

```text
visual replay
workflow reconstruction
live transaction replay
```

后者在真实历史系统上通常既不可行也不应尝试。

---

## 8. 网上票仍然需要纸：`paper bridge / 纸质桥梁`

2011 年福州火车站、福州南站的同期说明非常清楚：车站当时不具备二代身份证直接检票条件，所以即使用户已经完成网上实名购票和支付，仍需要在开车前用证件 / 订单信息换取纸质车票。

烟台、石家庄等同期材料也留下类似要求。

与此同时，京津城际等部分线路已经允许二代身份证直接进站。

因此不能把 2011 写成一个全国同步的：

```text
paper ticket
→
e-ticket
```

更准确的结构是：

```text
Web transaction ready
+
station identity/gate infrastructure uneven
→
some journeys still require paper bridge
```

### 证据

- **B+**：福州新闻网，2011-09-29，《温福、福厦动车实行网络售票 乘车需换纸质车票》。  
  https://news.fznews.com.cn/jsxx/2011-9-29/2011929XRE2RGW9OO154816.shtml
- **B+**：燕赵都市报，2011-09-30，《30日起动车开始网络售票 记者网上15分钟买张票》。  
  https://news.sina.com.cn/o/2011-09-30/070023242267.shtml
- **B+**：中国经济网，2011-06-13，《京津城际今起试行网络售票 二代证直接进站上车》。  
  https://finance.sina.cn/sa/2011-06-13/detail-ikftpnnx9267642.d.html

### 考古字段建议

以后记录早期在线事务时，不能只记：

```yaml
online_purchase: true
```

至少应该加：

```yaml
online_reservation: true
online_payment: true
paper_exchange_required: route_or_station_dependent
id_direct_boarding: route_or_station_dependent
```

否则会把完全不同的历史体验压成一个布尔值。

---

## 9. 一个账号里其实有两种身份：网站账户与乘车人身份

2011 网络售票要求网站实名注册，一张有效身份证件只能注册一个用户；但账户又可以为其他乘车人购买车票，一笔订单可包含多名旅客。

因此至少有：

```text
account identity
!=
passenger identity
```

这是具体的：

**`credential-layer split / 凭证层分裂`**。

例如：

```text
A 登录自己的 12306 账户
→
为 A / B / C 查询并购买
→
每个乘车人各自对应有效身份证件
```

Web archive 即使未来保存登录页，也不会保存真实用户当时账户内的乘车人列表和订单关系。

### 证据

- **B+/A-**：中国互联网协会保存的铁路规则，2011-09-19。  
  https://www.isc.org.cn/article/16580.html
- **B+**：福州新闻网，2011-09-29。  
  https://news.fznews.com.cn/jsxx/2011-9-29/2011929XRE2RGW9OO154816.shtml

---

## 10. “余票页面”保存得再好，也恢复不了当时的市场状态

12306 的历史页面真正依赖一个高度动态的库存系统。

某一秒可能是：

```text
二等座 12
```

下一秒可能：

```text
二等座 0
```

同时还存在：

- 别人的 15 分钟未支付 seat lock；
- 刚刚取消的订单；
- 刚退回系统的席位；
- 银行支付已发生但 callback 尚未完成；
- 多用户并发提交队列。

所以本轮明确记录：

**`reservation-state loss / 预订状态丢失`**。

它具体包括：

```yaml
not_preserved_by_static_page_capture:
  - exact_inventory_snapshot
  - concurrent_orders
  - seat_lock_owner
  - seat_lock_expiry
  - order_queue_position
  - payment_pending_state
  - payment_callback_state
  - released_inventory_event
  - sms_or_email_delivery_state
```

这与“市场状态丢失”相似，但这里的研究对象更窄：**一个单一旅客事务与实时铁路库存之间的短时联动。**

---

## 11. 2012：Web 并发压力又增加了“排队页”这一新事务状态

2012 春运前后，12306 在高并发下使用排队机制，媒体报道过用户提交订单后进入系统队列、长时间等待的情况。

这意味着在线购票并不是：

```text
点击 → 成功 / 失败
```

而可以出现：

```text
查询到余票
→ 提交
→ queue state
→ 等待服务器处理
→ 再决定有没有订单 / 席位
```

这个 queue state 对 Web archaeology 很重要：

- 它可能由动态 JS / session 维持；
- 同一个 URL 对不同用户显示不同排队状态；
- archive crawler 几乎不可能拥有真实旅客会话；
- 一张排队页截图不能告诉我们用户最终是否买到票。

因此：

```text
queue UI preserved
!=
queue state reconstructed
```

---

## 12. historical locator 的“操作化石”活在第三方旧页面里

本轮找到多类 2011–2012 第三方 contemporaneous pages，仍然保存：

```text
http://www.12306.cn/mormhweb/kyfw/ypcx/
```

以及它的用途描述。

例如：

- 2011 WordPress 旅行计划要求同行者用这个 URL 查票；
- 2011 博客园技术笔记收录该 URL；
- 2011 温州交通信息把它作为铁路客服中心的车票 / 余票 / 时刻入口；
- 2012 背包客论坛用户直接贴该链接并讨论实时余票。

这说明，即使目标站点某个历史页面难以回放，**第三方普通用户页面仍能保存它的 historical address 和实际用途。**

这延续此前仓库记录的 cross-platform operational fossil，但这里对象从“同学录操作”变成了**公共事务网站的查询入口**。

### 证据

- WordPress，2011-03-06：  
  https://vivienwdd.wordpress.com/
- 博客园，2011-01-06：  
  https://www.cnblogs.com/Smalltalk/archive/2011/01/06/1927626.html
- 温州网经新浪保存，2011-07-26：  
  https://news.sina.com.cn/c/2011-07-26/161922880883.shtml
- 背包客栈，2012：  
  https://www.backpackers.com.tw/forum/showthread.php?t=719366

---

## 13. OWA M3 的直接实验价值

如果以后取得 2011 capture，本案例非常适合作为浏览器环境实验，因为已有同期证据预先给出可检验假设。

### 至少应该比较

1. modern Chromium；
2. IE6；
3. IE8 / IE9；
4. Firefox 同时代版本（若环境可得）；
5. 证书不受信状态；
6. HTTP 父页 + HTTPS iframe 条件；
7. 日期控件是否工作；
8. GBK / UTF-8 / response header；
9. 页面脚本是否依赖 `document.all` 或 IE-specific behavior；
10. bank redirect 只做离线结构分析，不尝试真实支付。

### 可验证的历史假设

同期证据已经给出：

- 非 IE 可能无法正常登录 / 订票；
- IE9 日期控件可能异常；
- SSL / iframe 可能影响加载；
- 页面要求安装根证书。

因此这个 case 未来不是“盲测各种浏览器”，而是可以直接验证 contemporaneous complaints。

---

## 14. 海外对照只写入方法背景，不扩张 OWA scope

`old-web-archaeology` 的主 scope 仍是约 1995–2015 中文互联网。

本轮不把法国 Minitel 写成仓库对象，只保留一个方法参照：法国 1988–1989 官方记录显示，TGV 柜台、旅行社、自动设备和 Minitel 可以共同接入一个中央预订服务器；Minitel / 电话占位如果不及时取票，也会重新释放。

这说明：

> **动态 seat state、远程预订、取票 deadline 和中央库存并不是 Web 特有结构。**

跨国生活史比较放在 HPL；OWA 只用它避免把 12306 的每个事务机制误判成“Web 首次发明”。

参照：

- 法国参议院，1988-12-08 / 1989-04-20：  
  https://www.senat.fr/questions/base/1988/qSEQ881202718.html

---

## 15. 本轮 artifact / evidence table

| 对象 | 日期 | 类型 | Grade | 能证明 | 不能证明 |
|---|---:|---|---|---|---|
| `12306.cn/mormhweb/kyfw/ypcx/` 第三方引用 | 2011 | contemporaneous locator | B/B+ | URL 与查询用途 | 页面长相、DOM |
| 非 IE 无法订票报道 | 2011-06 | journalist test + customer service | B+ | 浏览器门槛 | 每个用户都失败 |
| 上海网购体验 | 2011-09 | journalist workflow | B+ | 根证书、seat lock、15min、网银 | 服务器内部实现 |
| 福州铁路流程 | 2011-09 | railway rule via local media | B+ / A- | 实名、4证件、15min、SMS/email、纸票 | 全国所有站完全一致 |
| `longware` 博客 | 2011-11 | contemporaneous first-person | B | IE9/FF/SSL/短信问题的单用户操作 | 普遍故障率 |
| current `/mormhweb/kyfw/` | 2026 access | current live legacy shell | A for current state | historical path family today仍响应 | 2011 historical capture |
| French TGV/Minitel official answer | 1988–1989 | overseas comparative primary | A | central server + remote hold/release precedent | 中国 12306 行为 |

---

## 16. 已证实 / 高概率 / 不知道

### 已证实

- 2011 年 `www.12306.cn` 已提供分阶段网络售票；
- 早期网站明确存在 IE compatibility constraint；
- 网上购票需要实名注册与乘车人证件信息；
- 订单提交后存在约 15 分钟的临时席位保留 / 支付窗口；
- 逾期未支付席位会释放；
- 支付依赖银行 / 网银层；
- 成功后可通过短信 / 邮件收到信息；
- 2011 不同线路 / 车站对纸票兑换与身份证直接进站支持不一致；
- `mormhweb/kyfw/ypcx/` 是当时普通用户实际引用的查询 locator；
- 当前旧路径的服务器响应不能当成 2011 capture。

### 高概率但本轮不升级为已证实技术细节

- 2011 页面包含显著 IE-specific JavaScript / browser assumptions；
- seat lock 与 payment callback 需要服务器 session / database state；
- archive crawler 即使抓到 HTML，也很难保存一个真实动态 seat lock。

这些从用户行为和事务逻辑高度合理，但服务器源码 / 协议没有取得，因此不写成具体内部实现。

### 不知道

- 2011 具体购票页完整 DOM / CSS / JS 版本；
- 当时 Content-Type / charset 在各子系统是否一致；
- 证书链和根证书下载包的准确版本；
- 2011 所有银行支付页的浏览器兼容矩阵；
- `kyfw/ypcx/` 是否存在本轮尚未找到的合格 historical memento；
- archive 是否保存过登录前票务页面的第二历史时点；
- 2012 queue page 的完整客户端脚本；
- 当时页面中哪些资源来自另一个 host / CDN / 内网网关。

---

## 17. Historical capture probe 与负结果

本轮完成：

- 搜索 `12306.cn/mormhweb/kyfw/` 与 `ypcx` 的历史引用；
- 检查当前 `mormhweb` / `kyfw` 响应；
- 搜索 2011 contemporaneous blog / media / user references；
- 尝试搜索公开索引中的 archive locator。

本轮**没有取得一个已经实际打开并核验以下字段的 2011 Memento**：

```yaml
archive_source: ?
capture_url: ?
original_url: http://www.12306.cn/mormhweb/kyfw/
capture_datetime: ?
http_replay_state: ?
content_type: ?
charset: ?
subresources: ?
```

因此负结果只能写：

> **no verified 2011 historical capture obtained in this run**

不能写：

> Wayback 没保存 12306。

后者超出了证据。

---

## 18. M1 状态

按 `ROADMAP.md`，完整案例至少需要两个历史时点、独立来源、资源缺失、browser/encoding/plugin assumption 和 verified historical capture。

目前：

```text
platform identity: achieved
historical locator: achieved
contemporaneous workflow evidence: achieved
browser constraint evidence: achieved
transaction-state model: achieved
current live legacy path check: achieved
verified 2011 historical memento: NOT achieved
second verified historical timepoint: NOT achieved
original DOM/CSS/JS: NOT achieved
runtime replay: NOT achieved
```

因此：

**M1 early-12306 case: NOT ACHIEVED**

不能因为证据丰富就提前翻牌。

---

## 19. 下一步最值钱的工作

1. 用 Internet Archive / Common Crawl / 其他 archive 的可检索索引继续找 `mormhweb/kyfw/` 与 `ypcx/` 的 **真实 capture**；
2. 若取得 capture，记录 exact datetime、HTTP replay、redirect、charset、主 HTML 与子资源；
3. 优先尝试获得两个时点：2011 网络售票初期 + 2012 排队机制时期；
4. 查找同期 12306 根证书下载包 / filename / certificate chain；
5. 查找 IE6/IE8/IE9 下的 contemporaneous screenshots 或官方帮助；
6. 不尝试登录历史账号、不尝试支付、不复原真实个人订单；
7. 若 M3 开始，以“非 IE 失败 / IE9 日期控件 / certificate”三个同期 complaint 作为实验假设。

---

## 20. 方法结论

这个案例最重要的考古提醒不是“12306 当年很难用”。

而是：

> **一个旧 Web 事务系统真正的历史对象，往往不是页面，而是一段带截止时间、跨多个系统、依赖客户端环境的状态迁移。**

2011 年的一张铁路票至少可能跨过：

```text
IE / Firefox
→ 12306 account
→ passenger credential
→ live inventory
→ 15-minute seat lock
→ bank payment
→ callback
→ SMS/email
→ paper ticket or ID gate
```

只保存 `12306.cn` 的一张 HTML，无法恢复其中大部分真正决定普通人能不能回家的东西。

---

## AI-assisted research note

本研究笔记初稿由 AI 辅助整理；所有历史断言均区分 current-live artifact、contemporaneous media/user evidence 与尚未取得的 archive capture。未尝试真实登录、支付或历史账号访问。