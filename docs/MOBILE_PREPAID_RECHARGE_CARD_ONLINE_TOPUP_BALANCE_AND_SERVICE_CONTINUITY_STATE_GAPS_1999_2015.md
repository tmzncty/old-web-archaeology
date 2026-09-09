# MOBILE_PREPAID_RECHARGE_CARD_ONLINE_TOPUP_BALANCE_AND_SERVICE_CONTINUITY_STATE_GAPS_1999_2015

## 0. Scope

本研究包只处理 **约 1999—2015 中文 Web 与移动通信预付费/充值之间的网页、凭证、交易和服务状态缺口**。

它不是：

- 中国移动通信通史；
- 手机资费比较；
- 支付宝/网银通史；
- 2015 年以后 App 充值史；
- 手机号账号绑定/二次放号通史；
- 全球 prepaid mobile 通史。

长期生活史与海外比较写入 companion：

`tmzncty/how-people-lived/topics/PREPAID_MOBILE_RECHARGE_BALANCE_SERVICE_CONTINUITY_AND_NUMBER_MAINTENANCE_1984_2026.md`

手机号与互联网账号绑定另见：

`MOBILE_NUMBER_WEB_BINDING_SMS_RECOVERY_REALNAME_AND_RECYCLED_NUMBER_STATE_GAPS_2001_2015.md`

本仓真正要解决的是：

> **当一个中文旧网页写着“充值”“缴费”“充值成功”“余额”或“欠费停机”时，我们到底看见了哪一层状态？一个 Web 表单、一次第三方支付成功、一个语音/短信成功提示和运营商 authoritative balance ledger 之间为什么不能互相替代？**

---

## 1. Method contract

严格遵守 `docs/METHOD.md`：

- platform / site / page / capture / claim 分层；
- A/B/C/D evidence grade；
- `exists != available != used != popular != caused`；
- archive locator 未实际打开并检查，不叫 verified capture；
- “本轮没找到”不得写成“历史上不存在”；
- 今天仍活着的运营商页面调用今天后端，只能证明当前系统，不得当作 2009 transaction replay。

此外，本专题特别容易发生 **transaction hindsight**：

> 一个历史页面最后显示“充值成功”，并不能证明用户在点击按钮之前就已经拥有余额；一个现代帮助页仍写着“充值中心”，也不能证明它保持了十年前相同的支付渠道、字段、后台或状态语义。

---

## 2. Research unit

必须分开：

```text
mobile operator / carrier
subscriber account
phone number
SIM
prepaid balance / postpaid receivable
recharge card physical stock
recharge-card serial / PIN / secret
retailer / distributor
Web merchant / C2C seller
online business hall
bank / telephone bank / online bank
third-party payment provider
recharge order
payment transaction
carrier recharge request
carrier authoritative ledger mutation
balance query
service authorization state
SMS / IVR / Web success notification
browser page / capture
research claim
```

尤其不能把：

```text
merchant order status
third-party payment status
carrier recharge request status
carrier balance state
telecom service state
```

压成一个“充值成功”。

---

## 3. Claim list before narrative

本轮证据能够支持的最小 claims：

1. **1999 年中国联通公开推出预付费移动业务时，账户余额已经直接参与呼叫授权，并支持继续充值。**
2. **2004—2006 年实体充值卡仍是现实渠道，具有可分销、可掉包、可伪造/盗用的凭证状态。**
3. **2005 年至少一个中国联通省级网上营业厅已经把第三方网上支付嵌入手机充值/缴费页面。**
4. **2006 年电话银行充值把银行卡账户、手机号和运营商充值接口连接起来，并允许为他人号码充值。**
5. **2006—2007 年手机充值/IP 卡已经成为 C2C 平台显著商品类别之一，但平台公司数据不能等同于全国用户普及率。**
6. **2007—2010 年同期案例证明，假支付页和伪造“充值成功”反馈可能与运营商真实余额完全分离。**
7. **2010—2013 年充值进一步进入手机银行、网上营业厅、短信/WAP/电话营业厅等多渠道体系；不同渠道并存而非线性替代。**
8. **2013 年已有运营商文档明确存在延期停机/信用开机等例外，因此 `balance insufficient != service immediately terminated` 也不能作为绝对规则。**
9. **公开 Web archive 最容易保存充值入口、帮助页和营销文案，最难保存登录态、支付 callback、carrier ledger mutation、余额快照和服务授权状态。**

本轮证据不足以支持：

- “2005 年大多数中国手机用户已经网上充值”；
- “淘宝是手机充值大众化的主要原因”；
- “一个第三方页面显示成功即可证明运营商已入账”；
- “2013 年全国所有省份所有套餐都有同一种信用开机规则”；
- “Wayback 没有保存 2005 浙江联通或 2009 10086 充值页”。

---

## 4. Necessary prehistory boundary: 1999 prepaid mobile account, not mass Web recharge

1999 年 12 月 15 日，中国联通宣布在北京、上海、广州推出“如意通”预付费业务。同期报道直接说明：呼叫建立时根据账户余额决定接受/拒绝，通话中实时扣减，用户可继续充值。

Source:
- 中新社/新浪，1999-12-16: https://news.sina.com.cn/china/1999-12-16/42641.html

**Grade:** B — contemporaneous wire report relaying an operator launch.

这个锚点的考古意义是：

```text
telecom account balance state
already existed before
ordinary Web self-service top-up became routine
```

不能因为 1999 已有预付费账户，就把它写成 1999 用户已经通过浏览器管理账户。

本仓主对象从 **中文 Web 开始成为充值/缴费界面** 时才真正展开。

---

## 5. 2004—2006: physical recharge card is a credential-bearing artifact

### 5.1 卡不是“钱的图片”，而是一段可消费 credential

2005 年法制晚报记录北京移动准备推出 30 元充值卡，此前常见最低面额为 50 元。

Source:
- https://tech.sina.com.cn/t/2005-03-10/1838547300.shtml

**Grade:** B, contemporaneous media.

2006 年上海充值系统案件材料则明确出现充值卡后台数据的字段描述，包括序列号、明码和暗码。

Sources:
- 上海青年报/新浪，2006-06-22: https://tech.sina.com.cn/t/2006-06-22/10511002972.shtml
- 东方早报/新浪，同日: https://tech.sina.com.cn/t/2006-06-22/07071002281.shtml

**Grade:** B contemporaneous legal/media. These two reports concern the same case and are one evidence family.

因此历史充值卡至少应建模为：

```text
CARD_BATCH
→ CARD_CREDENTIAL_CREATED
→ PHYSICAL_CARD_DISTRIBUTED
→ PIN/SECRET_UNREVEALED?
→ USER_ACQUIRES_CARD
→ PIN SUBMITTED TO CARRIER CHANNEL
→ CARRIER ACCEPTS / REJECTS
→ VALUE CREDITED TO TARGET ACCOUNT
→ CARD CREDENTIAL CONSUMED
```

### 5.2 `physical card survives != credit was unused`

今天收藏到一张未刮/已刮充值卡，不能从外观推出：

- 当时是否已经售出；
- PIN 是否已经被抄走；
- 是否已充值；
- 是否失效；
- 目标号码是谁；
- 运营商后台当时如何记录。

反过来，一张卡已经被使用也可能继续作为纸片幸存。

这是一种典型的 **credential / substrate gap**。

### 5.3 2005 掉包案例固定 `card possession != credential validity`

汉网 2005 年报道，一个小店老板把一批充值卡交给买家检查后又收回，随后发现多张卡不能使用；案件调查指向卡片被调包/凭证被消耗的问题。

Source:
- https://news.sina.com.cn/s/2005-10-29/10487301751s.shtml

**Grade:** B contemporaneous media.

所以：

```text
retailer physically holds a card
≠ retailer still controls its stored value
```

---

## 6. 2005: online business hall adds a Web/payment layer

2005 年 12 月的同期报道记录：浙江联通与网银在线合作，把网上支付工具嵌入浙江联通网上营业厅缴费页面；历史报道给出的 host 是：

`www.zj.chinaunicom.com`

Source:
- eNet/新浪，2005-12-13: https://tech.sina.com.cn/roll/2005-12-13/1013790358.shtml

**Grade:** B contemporaneous service report.

可以写：

> By December 2005, a Zhejiang Unicom online business-hall payment path was publicly described as supporting mobile top-up/payment via third-party online payment.

不能写：

> `www.zj.chinaunicom.com` 当前任何可打开页面就是 2005 年充值页。

也不能写：

> 2005 年浙江联通用户普遍使用此功能。

### 6.1 最小 Web 状态机

```text
PUBLIC TOP-UP/PAYMENT PAGE AVAILABLE
→ USER ENTERS TARGET NUMBER / ACCOUNT INFO
→ AMOUNT SELECTED
→ PAYMENT PROVIDER SELECTED
→ REDIRECT / FORM POST TO PAYMENT PROVIDER
→ PAYMENT AUTHORIZED?
→ CALLBACK / RETURN TO MERCHANT?
→ OPERATOR RECEIVES RECHARGE REQUEST?
→ OPERATOR LEDGER CREDITED?
→ USER RECEIVES SUCCESS UI / SMS?
→ SERVICE STATE REFRESHED?
```

任何 archive capture 都不应把这些箭头自动视为已发生。

---

## 7. 2006: telephone-bank top-up makes one account a recharge source for several numbers

北京联通、工行、易宝 2006 年合作的同期材料描述：用户先拨工行 95588，把银行账户与手机信息关联，再拨 96533 进行充值；工行一个账户最多可为多个手机号码充值。

Sources:
- 通信世界/新浪，2006-06-14: https://tech.sina.com.cn/t/2006-06-14/1615990255.shtml
- 京华时报/新浪，2006-06-16: https://tech.sina.com.cn/t/2006-06-16/0546992912.shtml
- ChinaTechNews, 2006-06-19: https://www.chinatechnews.com/2006/06/19/3901-beijing-unicom-cooperates-with-yeepay-and-icbc-on-e-payment

**Grade:** B contemporaneous; same launch event, not three independent families.

这个对象不完全属于 Web，但对旧网状态考古很重要，因为它说明充值不是“页面自己完成”的：同一 telecom balance mutation 可以由电话银行、Web、充值卡等多个入口触发。

因此历史研究不能用：

```text
this account balance increased
→ must have come from this Web page
```

反推渠道。

---

## 8. 2006—2009: C2C platform turns recharge credential into a high-frequency Web commodity

2007 年淘宝发布的 2006 年交易材料把“手机充值/IP 卡”列入平台热销类别；同期报道特别指出，原本常在报刊亭/摊点购买的充值卡已经成为网上热销商品。

Sources:
- 千龙网/搜狐，2007-02-06: https://news.sohu.com/20070206/n248072994.shtml
- 太平洋电脑网/新浪，2007-01-18: https://tech.sina.com.cn/i/2007-01-18/1005221357.shtml

**Grade:** B contemporaneous media using Taobao company figures. These are platform self-reported data, not independent population data.

2009 年扬子晚报又把“淘宝网上买手机充值卡”写成已经不新鲜的交易类型，同时重点提醒新用户不要脱离平台流程、不要因明显低价进入假支付页面。

Source:
- 扬子晚报/搜狐理财，2009-09-29: https://money.sohu.com/20090929/n267090404.shtml

**Grade:** B contemporaneous consumer guidance.

### 8.1 C2C recharge has two distinct artifact families

```text
A. card/PIN sale
merchant delivers recharge credential
→ buyer later submits credential to carrier

B. direct top-up
buyer supplies target phone number
→ merchant/system submits recharge request
→ buyer expects carrier balance to change
```

历史页面如果只写“手机充值”，不能无证据决定属于哪一种。

### 8.2 `order completed != carrier credited`

C2C 订单可以在平台层结束，但 carrier ledger 是另一个系统。

研究时必须拆：

```text
ORDER_PAID
ORDER_FULFILLED_BY_SELLER
RECHARGE_CREDENTIAL_DELIVERED
or
RECHARGE_REQUEST_SENT
CARRIER_ACCEPTED
BALANCE_CREDITED
```

旧页面往往只保存前两层。

---

## 9. Fraud exposes the authoritative-ledger boundary

### 9.1 2007/08: fake low-price top-up page steals bank credentials

2008 年新京报报道，张小姐在 2007 年 12 月看到低价手机充值卡信息，被要求去卖家提供的页面支付 1 元；多次显示“系统故障”，实际银行卡却迅速发生多笔网上消费。

Source:
- https://news.sina.com.cn/c/2008-01-11/014313236252s.shtml

**Grade:** B contemporaneous police/media case.

考古边界：

```text
browser displays PAYMENT ERROR
≠ no financial transaction happened
```

和下一案例正好镜像。

### 9.2 2010: fake “recharge success” voice prompt, then service stops

2010 年白女士因营业厅已经关闭而急于充值，在路边摊付款后收到电话语音，提示“充值成功、当前余额 100 元”；第二天手机仍停机。

Source:
- 河北青年报/新浪，2010-08-16: https://news.sina.com.cn/c/2010-08-16/070117970386s.shtml

**Grade:** B contemporaneous first-person complaint.

考古边界：

```text
SUCCESS MESSAGE OBSERVED
≠ AUTHORITATIVE CARRIER BALANCE MUTATED
```

这个 state gap 应当成为所有支付/充值历史复原的强制检查项。

---

## 10. 2010—2013: multi-channel self-service and channel convergence

### 10.1 2010: mobile banking can top up self or another number

建设银行 2010 年服务文档写明，手机银行新增全国手机话费充值：可选本机或其他号码、选固定充值金额，成功后显示凭证号与缴费日期。

Source:
- 中国建设银行，2010-07-28: https://www2.ccb.com/chn/2010-07/28/article_2021122410374130178.shtml

**Grade:** A contemporaneous bank service documentation.

这一对象再次说明：

```text
TARGET MOBILE NUMBER
can be credited by
ANOTHER PERSON'S BANK SESSION
```

因此目标号码本人登录运营商网站不是充值成立的必要条件。

### 10.2 2011—2012: electronic channels coexist

中国移动 2012 年公开材料把网上营业厅、WAP 营业厅、短信营业厅、电话营业厅、自助终端作为并行电子渠道，并给出其公司口径的月度使用量与缴费金额。

Source:
- 中国网络电视台/搜狐IT，2012-01-23: https://news.cntv.cn/20120123/110860.shtml

**Grade:** B contemporaneous report relaying operator figures.

不能把此材料写成：

> “实体营业厅已经退出。”

恰恰相反，多渠道长期共存意味着不同群体仍面对不同的：

- 银行账户条件；
- 网络接入；
- 手机终端能力；
- WAP/短信技能；
- 信任与认证路径。

---

## 11. 2013: balance insufficiency no longer maps one-to-one onto immediate disconnection

浙江移动 2013 年春节服务说明记录：部分地区/用户有延期停机；某些在网时间达到条件的用户在余额不足、无法及时充值时，可以申请“信用开机”。材料还描述实体营业厅、自助终端、网站、充值卡和短信等并行渠道。

Source:
- 浙江移动，2013-02-09: https://www.zj.10086.cn/aboutus/xwdt/200000876227.html

**Grade:** A/B operator contemporaneous documentation.

这说明不能用一个简化状态机：

```text
balance <= 0 → service OFF
```

更准确地应允许：

```text
BALANCE LOW/INSUFFICIENT
→ account/product/region policy checked
→ grace / credit / delayed suspension possible?
→ service partially or fully remains
→ later recharge / settlement required
```

历史“余额截图”因此不能单独推出当时的呼叫权限。

---

## 12. State-gap catalogue

### G1. `displayed-success / ledger-commit gap`

页面、短信或 IVR 说成功，不等于运营商 authoritative ledger 已经 credit。

### G2. `payment-success / recharge-success gap`

银行卡/第三方支付已经扣款，不等于 carrier recharge request 已经成功处理。

### G3. `merchant-order / carrier-state gap`

淘宝/商户订单完成，不等于 telecom account 已更新。

### G4. `card-substrate / card-value gap`

实体卡还在，不等于 stored value 还可用；凭证可能已被消耗、复制、掉包或失效。

### G5. `balance / service-authorization gap`

余额数字不等于真实通信权限；套餐、信用开机、停机状态、风控、SIM 状态都可能介入。

### G6. `service-authorization / actual-connectivity gap`

后台允许服务，也不等于现场一定有覆盖、设备正常、漫游可用。

### G7. `channel-origin gap`

一次余额增加可能来自营业厅、充值卡、电话银行、Web、WAP、短信、第三方支付、他人代充；不能从最终余额反推某个网页路径。

### G8. `target-number ownership gap`

充值目标号码不必是付款者本人号码；手机号、银行账户持有人、Web 登录者可能是三个人。

### G9. `amount-selection / amount-credited gap`

用户选择/支付的金额和运营商最终到账金额需要分别核验，尤其涉及折扣、赠送、促销、延迟到账时。

### G10. `recharge-time / service-restoration-time gap`

充值提交时间、支付时间、carrier 入账时间、服务恢复时间可能不同。

### G11. `online-shell / payment-backend gap`

archive 保存网上营业厅 HTML，不等于第三方支付 endpoint、callback、登录态和 operator backend 一起被保存。

### G12. `current-help / historical-workflow gap`

今天 10086 帮助页仍写“网上营业厅/充值中心”，不能证明 2009 使用相同 URL、字段、支付方式或状态机。

---

## 13. Preservation levels

### R0 — mention only

同期新闻只说某平台/服务支持手机充值。

### R1 — public shell

保存首页/栏目页，可以确认存在“充值/缴费”入口。

### R2 — form semantics

保存目标号码、金额、充值方式等表单字段及 charset/browser assumption。

### R3 — payment handoff

可验证向哪个银行/第三方支付 endpoint handoff，参数 schema 可见。

### R4 — return/callback shell

保存支付返回/“处理中/成功/失败”页面，但尚不能证明 carrier ledger mutation。

### R5 — carrier-side confirmation artifact

有同期 SMS/余额查询/运营商订单记录，能够与 Web transaction 对应，但仍可能缺内部日志。

### R6 — controlled transaction reconstruction

在合法测试/模拟条件下，复原完整状态机，并明确 historical original 与 modern reconstruction 的差别。

`R6` 也不应要求取得真实历史普通用户的私人号码、银行卡、充值历史。

---

## 14. Browser / charset / implementation risks

2005—2012 的充值页很可能涉及：

- GB2312 / GBK / UTF-8；
- IE-focused JS；
- popup / redirect；
- frames；
- bank plugin / ActiveX / security control；
- session cookie；
- form POST；
- hidden fields；
- cross-domain return URL；
- AJAX/XHR；
- image captcha；
- SMS verification；
- WAP sibling flow。

因此：

```text
modern browser renders form
≠ historical browser could complete payment
```

尤其是历史银行控件/ActiveX 缺失时，archive 重放可能看起来“页面完整”，实际交易路径在当年依赖的客户端组件完全没有保存。

---

## 15. Archive replay attempt and negative evidence

本轮基于同期文献得到至少两个重要历史目标：

```text
www.zj.chinaunicom.com     # 2005 浙江联通网上营业厅报道给出的 host
www.10086.cn               # 2010s 中国移动统一门户/网上营业厅
```

随后尝试直接构造 Internet Archive replay：

```text
https://web.archive.org/web/20061201000000/http://www.zj.chinaunicom.com/
https://web.archive.org/web/20091201000000/http://www.10086.cn/
```

当前研究环境拒绝打开这些未经搜索结果建立 provenance 的构造 URL，返回 URL-safety 限制；因此没有实际取得/检查 memento。

本轮状态严格记为：

```text
M1 verified 2005–2006 Zhejiang Unicom online-hall capture: NOT ACHIEVED IN THIS SLICE
M1 verified 2009 China Mobile unified-portal recharge capture: NOT ACHIEVED IN THIS SLICE
```

这**不表示** Internet Archive 没有保存，也不表示当年页面不存在。

下一轮若继续，应：

1. 从 archive 搜索/索引先获得可追溯 locator；
2. 实际打开 memento；
3. 记录 original URL、capture URL、capture datetime；
4. 核验 HTTP / charset / redirect / login shell；
5. 检查 form action、银行/支付 handoff、JS/ActiveX；
6. 不尝试真实支付；
7. 不把现代运营商 backend rehydration 当历史交易结果。

---

## 16. Privacy and safety boundary

充值考古特别容易碰到：

- 完整手机号；
- 银行卡/支付账户；
- 充值 PIN；
- 交易流水号；
- 余额；
- 真实姓名；
- 登录 cookies/session；
- 第三方为谁充值的关系。

仓库只应保存支持状态模型所需的最少结构信息。

不要：

- 重新公开历史普通人的完整手机号；
- 保存仍可能有效的 PIN/密钥；
- 尝试历史支付 endpoint；
- 使用泄露账号复原私人充值记录；
- 把犯罪报道里的具体方法写成可复用攻击教程。

---

## 17. Cross-repo life-history interpretation

本仓只保留与旧 Web artifact/state 直接相关的解释：

```text
physical recharge card
→ telephone-bank / Web recharge
→ C2C digital commodity
→ mobile-bank / multi-channel top-up
→ online account maintenance becomes ordinary service infrastructure
```

更长的生活史结论放在 `how-people-lived`：

- 异地迁移者为什么需要远程续费旧号码；
- 家人/朋友代充为何是一种小额远程照护；
- 2018 以后低价套餐为何越来越像号码身份的维护费；
- 2020 欠费不停机为什么说明通信已经成为危机中的基础设施；
- 2020s 为什么“账户有钱”仍不足以保证号码可用。

---

## 18. What changed in our understanding of the old Chinese Web

充值页看起来像一种非常无聊的旧 Web 表单：

```text
手机号
+ 金额
+ 支付方式
+ 提交按钮
```

但它实际上是中文 Web 最早把**浏览器里的一个动作直接变成现实通信能力变化**的典型事务之一。

用户不是在网上购买一段纯数字内容；他是在尝试改变运营商网络里的一个授权状态，使某个真实的人第二天仍然能打电话、收通知、联系家里。

也正因为如此，普通 Wayback 式页面保存对这一对象天然不完整。最容易留下来的，是“充值”两个字和漂亮的成功页；最难留下来的，却是决定这件事是否真正发生的几层状态：

```text
钱有没有被银行扣掉？
商户有没有收到？
充值请求有没有送到运营商？
运营商 ledger 有没有入账？
服务什么时候恢复？
那个号码当时到底属于谁？
```

因此本专题给仓库新增的一条通用考古原则是：

> **对于会改变现实制度/账户状态的旧 Web 页面，保存 UI 永远不能自动升级为保存 transaction。**

充值只是一个很早、很生活化、也很容易看懂的例子。
