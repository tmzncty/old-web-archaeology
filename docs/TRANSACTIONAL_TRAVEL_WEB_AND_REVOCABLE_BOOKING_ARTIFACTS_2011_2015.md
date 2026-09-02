# TRANSACTIONAL_TRAVEL_WEB_AND_REVOCABLE_BOOKING_ARTIFACTS_2011_2015

## Scope

本说明研究 2011–2015 年中文旧网中的一个此前未单独建模的对象：**公共服务型交易网站（transactional public-service web）**，以中国铁路 12306 的网络售票为主要案例。

本仓 scope 仍保持约 1995–2015 中文互联网。本说明不把 2020–2022 疫情出行史纳入旧网研究对象；后期材料只在 `tmzncty/how-people-lived` 中用于说明这种交易基础设施后来如何承载退票、停运和旅行资格变化。

核心问题不是“12306 当年好不好用”，而是：

> 当一个旧网页不只是展示信息，而是在实名、实时库存、支付和线下核验之间推进一笔交易时，今天的 archive 到底还能保存多少历史过程？

---

## 1. 研究单位：不要把“购票页面”当成完整购票系统

2011 年铁路互联网售票的同期规则已经表明，一次完整交易横跨多个对象：

```text
公开首页 / 查询页
→ 用户账户
→ 实名乘车人信息
→ 实时余票与席位锁定
→ 订单状态
→ 外部支付渠道
→ 短信 / Email 通知
→ 纸质车票或电子客票状态
→ 车站身份 / 票证核验
```

因此考古单位必须至少区分：

- **public page**：任何人可访问的说明、查询或入口；
- **authenticated account state**：登录后的用户状态；
- **passenger identity record**：乘车人实名信息；
- **inventory state**：某一时刻的余票；
- **order state**：已锁席、待支付、已支付、已取消、已改签等；
- **payment handoff**：跳转到银行、银联、支付宝等外部支付系统；
- **confirmation artifact**：订单号、短信、Email、电子票信息；
- **physical handoff**：换取纸质票、刷身份证进站、窗口改签等。

**同一个 host 上的一组页面 ≠ 完整服务系统。**

---

## 2. 2011：Web 交易从页面直接跨进身份证、银行和车站

2011 年 6 月京津城际率先开通网络售票，随后逐步扩展到高铁、动车和更多普速列车。同期操作说明要求：

- 用户先在 12306 注册；
- 填写真实姓名、身份证件类型/号码、手机号、电子邮箱等；
- 一张有效身份证件通常只能注册一个用户；
- 查询并预订后必须在规定时间内在线支付；
- 交易成功后通过手机/邮箱得到信息；
- 在不少车站仍需携证件和订单信息换取纸质车票；
- 少数具备二代身份证检票条件的线路可以直接以购票所用身份证通过自动检票。

因此必须写出：

> **electronic purchase ≠ paperless boarding**

以及：

> **web transaction ≠ web-contained transaction**

### 证据族

**Family A — 铁路规则/官方操作信息的同期转述**

- 中新网转述铁路客户服务中心《京沪高速和京津城际铁路互联网售票暂行办法》，2011-06-24：  
  <https://www.chinanews.com.cn/cj/2011/06-24/3134489.shtml>
- 中新网/新华网，2011-09-30，注册字段、证件、支付与通知流程：  
  <https://www.chinanews.com/gn/2011/09-30/3364951.shtml>
- 北京晨报经搜狐，2011-11-19，《旅客列车互联网售票暂行办法》、电子客票状态、改签/退票与纸票转换：  
  <https://news.sohu.com/20111119/n326137863.shtml>

**Family B — 同期地方现场/操作报道**

- 燕赵都市报经新浪，2011-09-30：石家庄当时网上购票后仍需到指定窗口换纸质票。  
  <https://news.sina.com.cn/o/2011-09-30/070023242267.shtml>

证据等级：主要为 **B（近同时代二手）**，其中直接转述官方规则的窄 claim 可视为 A-near-primary，但在未取得原始 2011 规则页面 capture 前不升级为完整 A artifact。

---

## 3. Archive 最难保存的不是页面，而是“状态”

传统 Wayback 式页面考古最容易保存：

- 首页 HTML；
- 帮助页；
- 静态操作说明；
- 新闻公告；
- 某时刻的 CSS/图片（若子资源成功保存）。

但一次铁路购票真正决定结果的部分大量属于**短寿命状态**：

- 当秒余票；
- 某用户是否已经锁定席位；
- 订单还有多少支付时间；
- CAPTCHA 的具体挑战；
- 用户 cookie / session；
- 支付跳转后的银行状态；
- 短信是否送达；
- 纸票是否已换取；
- 该电子票是否已失效；
- 车站当时是否具备身份证直接检票能力。

因此：

> **archived form ≠ archived transaction**

> **archived availability query ≠ historical inventory snapshot**

> **HTML capture success ≠ order workflow reconstructable**

---

## 4. 2012：高并发把“页面存在”与“用户能完成交易”进一步分开

2012 年春运期间，铁路方面称互联网售票已覆盖全路，但当时互联网票仍只占总售票的一部分。与此同时，大量用户遭遇页面缓慢、无法进入、扣款与出票状态不同步等问题。

这类案例必须严格区分：

- `service_exists = true`
- `route_supported = true`
- `user_reached_login = ?`
- `query_succeeded = ?`
- `seat_locked = ?`
- `payment_debited = ?`
- `ticket_issued = ?`

不能从“12306 已上线”推出“某个用户当时能够完成网上购票”。

### 证据族

- 新华社采访铁路客服专家（中新网转载），2012-01-13：网络售票逐步扩张、春运售票占比、服务链条。  
  <https://www.chinanews.com.cn/cj/2012/01-13/3603064_2.shtml>
- 《新京报》经新浪，2012-01-14：网站缓慢、扣款后未出票等同期故障经验。  
  <https://news.sina.com.cn/c/2012-01-14/023123797504.shtml>

---

## 5. 2013：同一交易系统开始跨 Web 与官方 App

2013 年 12 月官方“铁路12306”手机客户端上线试运行；同期铁路方面还表示新版网站增加了动态刷新、自动查询、自动提交等功能。手机端可以复用网站用户名/密码，并进入铁路电子支付平台完成付款。

这意味着从 2013 年起，对同一服务不能再简单使用：

`platform = website`

更准确的是：

```text
service = 12306 railway ticketing
channel ∈ {desktop web, mobile app, phone, station window, agency}
shared backend / account relationships = must be evidenced per version
```

### 考古边界

- **app available ≠ web obsolete**；
- **same account credential ≠ identical client behavior**；
- **same backend ≠ same front-end feature set**；
- **current app download page ≠ proof of exact 2013 launch UI**。

### 证据族

- 新华社/人民网，2013-12-09：官方 App 上线、新网站自动查询/自动提交等功能。  
  <https://media.people.com.cn/n/2013/1209/c40733-23790795.html>
- 新浪科技/新文化报，2013-12-09：客户端下载、Web 账号复用、支付渠道和稳定网络要求的同期实测。  
  <https://tech.sina.com.cn/i/2013-12-09/11168988455.shtml>

---

## 6. 2014–2015：CAPTCHA 是页面元素，也是竞争规则

2014 年，12306 更换动态验证码以限制抢票插件；2015 年又升级为图片点选验证码。同期媒体和用户反馈显示，这些 CAPTCHA 不只是“登录页长什么样”的视觉细节，而是直接改变：

- 第三方浏览器/插件能否自动操作；
- 人工登录需要多少时间；
- 用户在高峰放票时能否及时进入订单流程；
- 页面与自动化工具之间的竞争关系。

因此研究 CAPTCHA 时不能只保存截图。

需要记录：

- challenge 类型；
- 出现在哪个 workflow stage；
- 是否每次动态生成；
- 是否与登录、查询、提交订单绑定；
- 官方声称的目的；
- 同期用户/第三方如何实际应对；
- 是否导致第三方工具失效；
- 哪些 claim 仅来自第三方厂商。

### 证据族

- 中国广播网相关报道的英文转述，2014-01-02：动态验证码、插件浏览器受影响。  
  <https://www.ecns.cn/cns-wire/2014-01-02/95200.shtml>
- 广州日报/人民网，2015-03-17：图片点选验证码实测。  
  <https://travel.people.com.cn/n/2015/0317/c41570-26703269.html>
- 新华社/人民网，2015-12-10：铁路部门说明验证码主要用于阻止自动化异常访问，并给出网络售票量。  
  <https://politics.people.com.cn/n/2015/1210/c70731-27912601.html>

### 重要反例

2015 年关于“一次通过率”的统计口径存在明显来源差异：第三方厂商和铁路后台给出的比例不同。因此：

> **one vendor metric ≠ platform-wide historical truth**

应保存各自口径与 evidence family，不做简单平均。

---

## 7. Transaction archaeology：建议新增字段

对于 12306、网银、电商、早期政务预约、招生报名等同类中文旧网对象，建议最少记录：

```yaml
service_name:
service_version_date:
channel:
  - desktop_web
  - mobile_web
  - mobile_app
  - phone
  - physical_window
public_entry_url:
auth_required:
account_registration_required:
credential_types_accepted:
identity_binding_scope:
inventory_dynamic:
transaction_state_model:
seat_or_resource_lock_timeout:
payment_external_dependency:
notification_channels:
output_artifact:
physical_handoff_required:
anti_automation_gate:
known_browser_or_network_constraints:
archiveable_static_components:
non_archiveable_runtime_state:
observed_user_success_evidence:
observed_user_failure_evidence:
```

### `identity_binding_scope`

不要只写 `real_name = true`。应区分：

- 账户是否实名；
- 乘车人是否实名；
- 一个账户能否替别人购票；
- 一张证件能绑定多少账户；
- 证件是否也是最终进站凭证；
- 纸票是否会改变电子票状态。

### `transaction_state_model`

至少预留：

```text
queried
→ seat_selected / seat_allocated
→ order_created
→ awaiting_payment
→ paid
→ ticket_issued
→ paper_ticket_exchanged (optional/version-specific)
→ changed / refunded / invalidated
```

不同年代/线路必须按证据修订，不能把今天的 12306 状态机倒推到 2011。

---

## 8. 新的硬规则

### 8.1 `page exists ≠ transaction succeeds`

网页可以打开，仍可能在登录、库存、验证码、支付或出票环节失败。

### 8.2 `query result ≠ stable inventory`

余票是实时数据库状态。一个静态 archive capture 即使保存了某个数字，也必须先确认它不是回放错误、模板值、JS 失败或过期响应。

### 8.3 `electronic ticket ≠ paperless travel`

2011 年许多车站仍要求换取纸质票；只有具备相应检票条件的部分线路可直接刷二代身份证。

### 8.4 `payment button ≠ payment archived`

支付通常跨到银行/银联/支付宝等第三方系统。主站 capture 无法证明支付网关当时成功、也无法保存用户银行端结果。

### 8.5 `CAPTCHA screenshot ≠ CAPTCHA distribution`

动态验证码的一张截图只能证明某个挑战实例存在，不能证明所有用户都看见同样题目或难度。

### 8.6 `plugin blocked ≠ all automation blocked`

同期浏览器、抢票工具会迅速变化。某一天某个插件失效不能推广成整个春运期间都失效。

### 8.7 `app launch ≠ website replacement`

2013 年后多个渠道并存。研究“普通人怎样买票”必须记录 channel switching。

### 8.8 `current help page ≠ historical rule`

12306 今天仍在线、URL 也可能延续，但帮助文本、证件类型、退改签规则、服务时间和页面结构会变化。必须绑定发布日期或可验证 capture datetime。

---

## 9. “可撤销预订”为什么值得在旧网仓保留为结构概念

2011–2015 的铁路 Web 已经不只是信息浏览，而是在处理：

- 实时资源分配；
- 合同生效/终止；
- 改签；
- 退票；
- 支付退款；
- 电子状态与纸质凭证之间的转换。

因此它是一个很早、规模很大的 **revocable booking system（可撤销预订系统）**。

这为后来的生活史研究提供一个重要前提：当 2020–2022 外部条件频繁变化时，人们之所以能够不断取消、重订和重新安排旅行，是因为早在旧网时代，这套“预订并撤销未来资源”的数字交易语法已经被建立起来。

但请注意：**2020–2022 的疫情政策、健康码或地方出行资格不属于本仓 1995–2015 主 scope。** 这里只保留系统谱系链接，不向后扩张研究对象。

交叉研究见：

- `tmzncty/how-people-lived/topics/bookability-travelability-and-reversible-mobility-planning-china-2011-2022.zh-CN.md`

---

## 10. 已证实 / 高概率 / 不知道

### 已证实

- 2011 年铁路互联网售票分阶段扩展，并要求账户、实名证件信息和在线支付。
- 2011 年部分车站/线路网上购票后仍需换纸质票，部分高铁/城际具备身份证直接检票。
- 2012 年春运出现过显著高并发和交易状态问题。
- 2013 年官方 12306 App 上线，Web 与 App 并存。
- 2014–2015 验证码被用于限制自动化访问，并真实影响插件/用户操作。

### 高概率但仍需更强 archive artifact

- 2011、2012、2013、2015 各版本 12306 的完整页面状态机可以通过历史 capture + 同期操作报道复原出大部分结构。
- 某些支付跳转、订单倒计时、验证码和错误页可能只能通过截图/媒体实测而无法由普通 Web archive 完整回放。

### 不知道

- 目前尚未在本轮直接核验一组覆盖 2011→2013→2015 的 Wayback/WARC 原始 capture，因此不能把今天仍存活的 12306 帮助 URL 当作原版页面。
- 不知道各时期所有浏览器/插件组合的真实兼容矩阵。
- 不知道 archive 是否保存过可验证的、含真实历史库存的查询响应；即使存在也需隐私与真实性检查。

---

## 11. 下一步最有价值的考古动作

不是再找更多“12306 很卡/验证码很难”的新闻，而是：

1. 为 2011、2013、2015 各找至少一个可实际打开的 archive capture；
2. 分别记录 homepage、login、query、order/help 页面是否能回放；
3. 检查 CSS/JS/验证码子资源是否缺失；
4. 记录页面 charset、浏览器假设和外部支付域名；
5. 尝试仅复原**workflow graph**，不模拟真实购票、不请求历史账户数据；
6. 明确标记所有实时库存、session 与订单状态为不可由静态 capture 直接复原的部分。

如果无法获得原始 capture，应保留这份方法说明为 research note，而不是用今天的网站截图伪装 2011 页面。
