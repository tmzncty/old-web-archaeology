# UTILITY BILL ACCOUNT BINDING, PAYMENT AND SERVICE-CONTINUITY STATE GAPS, 2003–2015

Status: research note / state-gap model  
Scope: 约 2003–2015 中文 Web 中水、电、燃气等公用事业账单查询、账户/户号绑定、第三方缴费、银行支付、电子账单与公用事业后台销账之间的技术状态；**不把本仓扩展成公用事业史，也不重复通用网上银行史，更不延伸成 2015 年后的移动 App 史**。  
Cross-repo companion: `tmzncty/how-people-lived/topics/from-shared-meters-to-household-uptime-utility-accounts-recurring-obligations-and-remote-home-maintenance-china-1998-2026.zh-CN.md`

---

## 0. Why a utility-payment page is not just another bank-transfer page

本仓已有：

- `ONLINE_BANKING_REMITTANCE_AND_PAYMENT_STATE_GAPS_1997_2015.md`：个人网银、授权介质、跨行清算；
- `ECOMMERCE_CHECKOUT_DELIVERY_ADDRESS_PICKUP_AND_FULFILLMENT_STATE_GAPS_1999_2015.md`：商品、checkout、配送；
- `HOME_BROADBAND...`：住宅宽带申请、装机、账户和销户；
- `WEB_FORM_FAX_EMAIL...`：远程提交与文书状态。

本 note 不重复“钱怎么从银行出去”，而是研究一个更窄的对象：

> **某一笔钱怎样被识别为“这间住宅、这个户号、这个账期的这张水/电/燃气账单”，并最终改变公用事业自己的账务与服务状态。**

公用事业支付链至少可以拆成：

```text
dwelling / service point
→ meter / connection
→ utility customer account / 户号
→ account-holder / occupant relation
→ meter read / usage record
→ bill generation
→ paper/electronic bill issued
→ customer encounters bill
→ payment channel supports this city + biller + account type
→ account number / barcode entered or bound
→ bill lookup
→ amount returned
→ payment instrument selected
→ payment authorization
→ bank / payment-network settlement
→ utility receives payment reference
→ utility ledger write-off
→ arrears state updates
→ physical service remains / resumes
→ receipt / history retained
```

公共 Web 档案最容易留下：

- 公共事业缴费入口；
- 帮助页；
- “生活助手”产品说明；
- 支持城市/缴费单位列表；
- 电子账单宣传页；
- 争议公告。

而最关键的私人状态通常不会、也不应该进入公共 archive：

- 真实户号；
- 水电用量；
- 欠费金额；
- 银行账户；
- 支付授权；
- 某笔钱是否已经在 utility ledger 中 durable write-off；
- 某住宅是否因欠费被停供；
- 谁实际居住在那里。

因此本 note 的核心命题是：

> **payment shell survives much better than obligation state.**

---

## 1. Evidence contract and privacy stop condition

遵循 `docs/METHOD.md`。

### 1.1 Research units

必须区分：

- `utility_company_or_biller`
- `service_point_or_dwelling`
- `meter_or_connection`
- `utility_account_number`
- `account_holder`
- `actual_occupant`
- `payer`
- `bill`
- `billing_period`
- `public_payment_page`
- `third_party_aggregator`
- `bank_or_payment_instrument`
- `private_session`
- `payment_request`
- `payment-network settlement`
- `utility_ledger_writeoff`
- `service_state`
- `capture`
- `claim`

尤其禁止把：

```text
payer = account holder = resident
```

当作默认事实。

2009 年的普通用户材料已经说明，外地成年子女完全可以替父母住宅缴账单。

### 1.2 Evidence grades

- **A**：同期公用事业、银行、平台正式规则/帮助页，或已验证的历史 capture；
- **B**：同期新闻、用户教程、记者实测、行业机构材料；
- **C**：后来回忆/机构历史；
- **D**：本仓状态链和推断。

Current live host 上保存的旧发布日期文本，可以证明“该机构今天保存了这份旧文本”，**不等于本轮已经验证其 historical DOM / HTTP headers / capture datetime**。

### 1.3 Privacy stop

不得为了 old-web 考古：

- 寻找泄露的真实水、电、燃气户号；
- 测试现存或历史户号是否仍可查询；
- 输入普通人的身份证、地址、银行卡；
- 尝试重放旧支付；
- 批量保存包含居民用量、欠费、住址和身份的私人账单；
- 用仍然可工作的找回流程推断旧账户身份。

公开帮助页足以研究状态模型；私人 transaction darkness 是这个对象本身的一部分。

---

## 2. 2003：银行网站有“缴费”能力，不等于已经知道某项公用事业如何接入

中国建设银行 2003 年官方网上银行材料已经把“缴费”与查询、转账、网上购物并列为网银能力之一。

Official source:
- 中国建设银行 2003 年相关网上银行功能材料（current official archive / dated material；本轮未验证 historical memento）。

Evidence grade:
- **A/B boundary：官方保存的同期文本；用于证明产品能力声明，不恢复 DOM。**

这里必须增加：

## **generic-payment / biller-integration gap**

```text
online bank has “缴费” menu
≠
my city's water utility is connected
≠
my account type is queryable
≠
my bill can be paid today
```

一个“公共事业缴费”菜单背后仍然需要：

- 银行与具体公用事业单位的业务关系；
- 城市/地区路由；
- 户号格式；
- 账单查询接口；
- 金额与账期匹配；
- 后端销账回传。

因此品牌级 capability 不能替代 biller-level evidence。

---

## 3. 2005：纸账单条码已经可以成为 Web/自助支付与后台账务之间的桥

2005 年《新民晚报》关于上海多媒体自助缴费的同期报道描述：银行卡用户可以在居民区等地点的自助终端插卡、扫描公共事业账单条形码并付款；银联完成资金清算后，再把成功交易的条码信息传给公用事业单位用于销账。

Source:
- 《新民晚报》2005-07-14：
  https://finance.sina.com.cn/money/bank/bank_card/20050714/15331797230.shtml

Evidence grade:
- **B：同期媒体；足以证明报道所描述的操作/机构链，不用于猜具体网络协议。**

这给 old-web archaeology 增加一个重要对象：

## **barcode-to-ledger bridge**

条码把：

```text
paper bill
```

映射到：

```text
utility obligation identity
```

再让支付系统产生可回传的 reference。

但状态仍需拆开：

```text
barcode scanned
≠
correct utility account matched
≠
correct amount returned
≠
payment authorized
≠
settlement completed
≠
utility ledger written off
```

### 3.1 physical paper can remain an input to digital payment

这也是一个很重要的形态史修正：

> **digital payment ≠ paper bill disappeared。**

2000s 的电子化完全可以把纸账单当作机器可读 credential。

因此保存一个历史支付页面时，应问：

- 它要求手输户号还是扫描/输入条码？
- 账单本身是不是另一份必要 artifact？
- 用户没有纸账单时，Web 是否能主动 query amount？

---

## 4. 2005：account/bill binding can move repeated typing into persistent state

2005 年上海另一些同期报道介绍电话缴费时，已经出现把电话号码与公共事业账单绑定的机制，以免用户每次都重新输入很长的账号/条码信息。

Near-contemporary sources:
- 2005 上海公共事业电话缴费/付费通相关报道（同期新闻材料）。

Evidence grade:
- **B。**

这里增加：

## **bill-binding state**

```text
one-time input of utility identity
→ persistent mapping in payment service
→ later payment can reuse mapping
```

它与浏览器 cookie 不是同一件事。

必须区分：

- 浏览器保存表单；
- 用户支付账号保存 biller binding；
- 公用事业后台保存 account-holder；
- 电话号码作为调用入口。

一个人换电话号码、迁居或换户以后，旧 binding 可能继续存在，形成新的 stale-state risk。

---

## 5. 2009：一个真实用户流程证明“bill lookup”和“bank payment”是两段系统

2009-04-19 一篇今天由第三方技术站保存的近同时代用户文章，记录作者自己租房时一直用建行网银缴水电费，后来又替父亲处理两张欠费单。

文章保存的操作描述大致是：

### 支付宝路线

```text
login
→ “生活助手”
→ 水 / 电 / 燃气
→ 选择服务单位
→ 输入账单/条码信息
→ 返回并核对金额
→ 再进入网银完成付款
```

### 建行路线

```text
login
→ 缴费
→ 公共事业
→ 输入条码
→ 系统返回账单金额供核对
→ 选择银行账户
→ 密码 / 授权
→ 完成
→ 可打印/下载回执
```

Source:
- 2009-04-19 dated user procedure, current preserving host:
  https://www.leadto.com.cn/technews/1316.html

Evidence grade:
- **B-：流程型近同时代用户材料；本轮没有验证原始 2009 host、memento、DOM、charset 或 endpoint。**

这条材料最重要的不是“哪个按钮叫什么”，而是状态分层：

## **bill-query / payment-authorization gap**

能根据户号/条码返回应付金额，说明系统具备某种 bill lookup；但用户之后仍然需要单独完成银行支付授权。

因此：

```text
bill amount displayed
≠
amount paid
```

同时：

```text
payer identity
≠
resident identity
```

因为作者可以替父亲的住宅付费。

---

## 6. 2009：support matrix is city × biller × account type, not a single “online payment exists” flag

2009 年中国互联网协会等同期报道记录，支付宝公共事业缴费逐步进入上海、北京、重庆、合肥、成都、宁波等城市，水、电、电话、宽带等项目分批接入。

Sources:
- 中国互联网协会，2009-09-01：
  https://www.isc.org.cn/article/8429.html
- 中国互联网协会，2009 相关材料：
  https://www.isc.org.cn/article/8463.html
- 宁波支付宝缴费同期报道，2009-12-15：
  https://business.sohu.com/20091215/n268972071.shtml

Evidence grade:
- **B/B+：同期行业机构/媒体；平台规模与效果数字保留为平台口径。**

因此旧网证据表最好记录：

```yaml
city:
biller:
service_type:
account_number_format_known: unknown|yes|no
bill_lookup_supported:
payment_supported:
payment_instrument:
real_time_writeoff_claimed:
```

新增：

## **city-biller capability gap**

不能从：

> “支付宝 2009 年可以交水电费”

推到：

> “2009 年任意城市、任意水电账户都能交”。

同一品牌、同一栏目，在不同城市可能显示完全不同的可用服务。

---

## 7. “实时销账”必须作为 claim，而不是 transaction proof

2009 年行业/平台材料把部分公用事业缴费描述为付款成功后可“实时销账”。

Source:
- 中国互联网协会相关同期平台报道：
  https://www.isc.org.cn/article/8463.html

Evidence grade:
- **B：平台/行业材料。**

本仓应把它写成：

```text
platform claimed real-time write-off
```

而不是：

```text
all successful user payments were durably written off in real time
```

因此增加：

## **front-end success / utility-ledger writeoff gap**

至少需要区分：

```text
payment platform accepted request
→ bank/network settled
→ aggregator generated reference
→ utility billing engine ingested reference
→ correct account / billing period matched
→ arrears flag updated
```

只有私人后台日志、对账或后续账单才能真正证明最后几层；公共 archive 通常没有这种证据。

---

## 8. 2012–2014：电子账单不是“没有账单”，而是 bill-delivery state 改变

2014 年上海关于电子账单公共服务平台的同期报道记录，该平台自 2012 年运行，用户可以接收水、电、燃气等电子账单，并可在申请电子账单后取消对应纸质账单。

Source:
- 2014 上海电子账单报道：
  https://finance.people.com.cn/n/2014/0321/c70846-24704406.html

Evidence grade:
- **B：同期媒体/平台材料。**

因此增加：

## **paper-bill / electronic-bill state divergence**

```text
obligation exists
≠
paper bill exists
```

以及：

```text
e-bill application submitted
≠
paper bill already cancelled
≠
e-bill successfully delivered
≠
user encountered it
```

这与 webmail / notification research 可以交叉：账单从物理信箱迁到账号后，家庭必须开始维护另一个 attention endpoint。

---

## 9. 2014：a payment entrance can vanish even when the utility account is unchanged

2014 年上海“付费通”与支付宝之间的公共事业缴费合作中止，提供了一个非常强的 platform-state example。

同期报道中：

- 付费通方面称，支付宝为了判断账单是否生成而进行高频查询，给其 EBPP / 下游公用事业计费系统带来压力并出现拥堵/宕机；
- 支付宝方面对原因与利益关系提出不同解释；
- 对普通用户来说，结果首先表现为：原来熟悉的第三方缴费入口不可继续使用。

Sources:
- 人民网财经，2014-03-21：
  https://finance.people.com.cn/n/2014/0321/c70846-24704406.html
- 中国新闻网，2014-07-01：
  https://www.chinanews.com/cj/2014/07-01/6336169.shtml
- 中国新闻网，2014-08-20，付费通微信等渠道：
  https://www.chinanews.com.cn/sh/2014/08-20/6513373.shtml

Evidence grade:
- **B：同期争议材料；具体技术因果存在争议。**

这里需要明确记录两条状态。

### **channel-contract dependency**

```text
utility account active
≠
third-party entrance available
```

### **query-load externality — contested**

第三方前端为了提供“账单是否已出”的体验，可能向下游 billing engine 产生额外 query load。

但本轮只能写：

> 一方当时如此解释，并存在争议。

不能把它升级成独立验证过的 outage root cause。

这也是 old-Web archaeology 的重要提醒：

> 一个今天消失的“生活缴费”入口，可能不是因为公用事业平台死亡，而是合作协议、API、流量策略或聚合商发生变化。

---

## 10. 2014：mobile/WeChat front end can reuse the same obligation identity

2014 年付费通微信服务的同期报道描述：用户注册/登录以后输入水电煤账户号，可以查询近期账单和支付状态，再通过绑定银行卡付款；为了安全，首次使用仍可能要求完整输入，后续则减少重复步骤。

Source:
- 中国新闻网，2014-08-20：
  https://www.chinanews.com.cn/sh/2014/08-20/6513373.shtml

Evidence grade:
- **B。**

这说明从 Web 到移动前端时，真正连续的对象不一定是 URL，而可能是：

- utility account number；
- billing backend；
- aggregator account；
- bank payment relationship。

新增：

## **front-end migration / obligation-identity continuity gap**

一个品牌从 Web 搬到微信，不代表：

- 旧 Web 账户完全继承；
- 所有 bill binding 一并迁移；
- session / password model 相同；
- 当年的 Web 页面可以用今天微信流程倒推。

---

## 11. Full state model

### 11.1 Stable service identity

```text
physical dwelling
→ service connection
→ meter
→ utility account number
→ account-holder relation
```

Gaps:

- `meter ≠ household`
- `submeter ≠ direct utility account`
- `account holder ≠ actual occupant`
- `account number exists ≠ account currently active`

### 11.2 Bill creation

```text
meter read / usage event
→ bill calculation
→ billing-period record
→ bill issued
→ paper / e-bill / queryable state
```

Gaps:

- `usage occurred ≠ bill issued`
- `bill issued ≠ user notified`
- `paper bill cancelled ≠ obligation disappeared`
- `bill visible in one channel ≠ all channels synchronized`

### 11.3 Discovery / binding

```text
user reaches payment channel
→ channel supports city + biller
→ utility account entered / barcode scanned / binding reused
→ bill lookup
→ amount shown
```

Gaps:

- `payment brand supports utilities ≠ my biller supported`
- `account string entered ≠ correct account matched`
- `binding exists ≠ binding still current after move`
- `bill query success ≠ payment capability`

### 11.4 Payment execution

```text
amount confirmed
→ instrument selected
→ payment authorized
→ bank/payment network accepted
→ settlement
→ reference sent downstream
```

Gaps:

- `user clicked pay ≠ request accepted`
- `platform success ≠ bank settlement final`
- `bank debit ≠ utility ledger updated`

### 11.5 Obligation closure

```text
utility ingests payment
→ correct bill matched
→ ledger write-off
→ arrears updated
→ next bill reflects state
```

Gaps:

- `payment reference received ≠ correct bill matched`
- `ledger paid ≠ receipt delivered`
- `ledger arrears ≠ physical service immediately cut`

### 11.6 Moving / service succession

Although the companion life-history note carries the post-2015 integration history, old-Web reconstruction should already distinguish:

```text
residence / ownership change
→ final bill / meter state
→ old account closure / transfer
→ new account-holder proof
→ new billing address
→ new payment mandate / binding
```

Gaps:

- `property transferred ≠ utilities transferred`
- `old resident moved ≠ old direct-debit mandate closed`
- `new resident occupies dwelling ≠ new account-holder state completed`

---

## 12. A utility page needs several clocks

At minimum:

```text
meter_read_at
billing_period
bill_generated_at
bill_published_to_channel_at
paper_bill_sent_at
user_encountered_at
payment_submitted_at
bank_debited_at
settlement_at
utility_writeoff_at
arrears_state_changed_at
service_cut_or_restored_at
capture_at
```

Therefore:

> A screenshot showing “已缴” at time T cannot by itself reveal which earlier clock produced that state.

And an archived public help page from the same day does not contain private per-household ledger state.

---

## 13. Archive asymmetry

Public archives are structurally biased toward:

- product pages;
- help text;
- supported-biller lists;
- public login shells;
- announcements;
- press disputes;
- screenshots in tutorials.

They are structurally bad at preserving:

- authentication sessions;
- account numbers;
- private bills;
- meter readings;
- bank authorizations;
- per-transaction settlement;
- utility write-off records;
- arrears corrections;
- household move/transfer status.

This is not merely an archival failure.

Much of this material **should never have been publicly crawlable in the first place**.

Therefore introduce:

## **public-shell / private-obligation asymmetry**

A very complete archived public shell may coexist with near-total darkness about whether any given household successfully paid a bill.

---

## 14. Historical browser / client cautions

Future verified cases should record:

- IE / other browser compatibility;
- ActiveX / certificate / bank plugin dependencies inherited from payment step;
- charset and form encoding;
- whether utility selector/options are server-generated;
- whether city selection is cookie/session/account based;
- whether bill query uses full page refresh, frame, AJAX-like request, plugin or external redirect;
- bank-payment handoff method;
- whether return URL can be replayed without private session;
- whether today’s archived page is an archive rewrite rather than original response.

The 2009 user tutorial demonstrates a workflow, **not** a verified browser environment.

---

## 15. Negative result: no M1-grade utility transaction capture in this pass

本轮没有取得并实际打开、核验一份满足 `ROADMAP.md` M1 标准的 2003–2015 中文公共事业缴费完整 Wayback/WARC transaction capture。

因此以下内容继续保持 `unknown`：

- 2005/2009 具体缴费页 original URL；
- capture datetime；
- historical HTTP headers；
- charset；
- DOM；
- `form action`；
- cookie / session model；
- city/biller selector 的真实实现；
- 户号/条码字段规则；
- bill-query endpoint；
- bank/payment redirect details；
- private utility ledger schema；
- write-off transaction semantics。

当前保存的同期新闻、机构页和用户流程足以形成 **state-gap research note**，但不能冒充 historical original。

M1 不应因此被勾选。

---

## 16. Next high-value evidence

下一步优先寻找：

1. 一份实际可打开、可记录 `original_url + capture_datetime` 的 2005–2010 公共事业缴费页面；
2. 最好能有同期用户教程/截图作为第二 evidence family；
3. 记录其支持城市/缴费单位，而不是只存品牌首页；
4. 若存在支付跳转，只记录公开 control surface，不尝试进入私人 transaction；
5. 检查同一服务在 Web → WAP/手机 → 微信前端迁移时，哪些账号/户号关系保持，哪些重新绑定；
6. 把 2014 合作中断前后的公开页面做时点比较，观察“功能消失”与“站点死亡”之间的区别。

最值得验证的旧网问题不是“支付宝当年长什么样”，而是：

> **当一张家庭账单从纸、电话、自助机进入 Web 时，究竟是哪一个字符串、哪一个后台关系让远处的付款人能够准确地把钱落到那间住宅的那一次义务上；而档案今天又能证明这条链走到哪一步。**
