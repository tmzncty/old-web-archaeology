# 中文旧网电子商务 checkout、收货地址、自提与履约状态缺口（1999–2015）

## Scope

本稿只研究约 1999–2015 中文 Web 的一个窄问题：

> **旧电商页面显示“可以买”以后，我们还需要哪些状态，才能证明一个普通人当时真的能把商品送到某个现实端点并取得它？**

这不是中国电子商务通史，也不扩张成 2020s 快递平台史。

它与 `how-people-lived` 的交叉点是 **physical delivery addressability / 物理可投递性**：稳定住宅并不是唯一的末端，单位、宿舍、邮局、自提点、代收人都可能成为现实交接端点。

本仓只处理中文旧网可观察的界面、账号、订单、配送与 archive state；全球 mail-order、邮政史与 2015 以后生活变化放在 `how-people-lived`。

---

## 1. 先定义研究单位

必须分开：

- **retail platform / site**：例如 dangdang.com；
- **product page**：某商品页面；
- **account**：某用户账号；
- **address-book entry**：账号内保存的一条收货信息；
- **cart**：尚未确认的商品集合；
- **checkout session**：一次结算状态；
- **order**：平台接受的一次购买请求；
- **payment state**：预付、货到付款、邮政汇款等；
- **delivery method**：快递、EMS、普通邮寄、自提等；
- **fulfillment record**：仓储/拣货/打包/出库状态；
- **shipment**：现实物流对象；
- **delivery attempt**：一次实际投递尝试；
- **pickup endpoint**：自提点/配送站等；
- **recipient / proxy recipient**：本人或代收者；
- **possession**：商品真正进入收件人控制；
- **return/refund state**：退货与退款闭环；
- **archive capture**：档案服务保存的某一表示。

不能把任何两个层级默认合并。

---

## 2. 最小完整状态链

```text
product exists
→ product page reachable
→ page says in stock / orderable
→ account usable
→ address/contact information available
→ cart
→ checkout session
→ delivery method available for this address
→ payment method available for this address/order
→ order submitted
→ platform accepts order
→ inventory allocated
→ warehouse picks/packs
→ carrier accepts parcel
→ shipment enters network
→ delivery/pickup endpoint reached
→ recipient or authorized proxy can receive
→ acceptance / COD / rejection
→ possession
→ possible return/refund
→ transaction closed
```

因此必须固定：

> **product page exists ≠ order could be submitted ≠ order was accepted ≠ parcel was shipped ≠ parcel reached the stated address ≠ the named person received it。**

---

## 3. 2010 当当 F-1：Web checkout 已经是一个私人状态机

### 原始证据

E-Commerce China Dangdang Inc. 2010-12-07 向 SEC 提交的 F-1/A 明确描述：

- 首次购买者需要建立账号并填写 contact information、shipping 和 payment details；
- 已有用户登录后可以调用 preferred checkout options；
- 系统会根据此前信息生成 preferred delivery address、shipping method 和 payment option；
- 账号自助功能可以 track order and shipment status、查看预计送达日期、取消未出库商品、修改 delivery information/payment options、合并订单和申请退货；
- payment options 包括 COD、在线支付、wire transfer 和 postal remittance；
- COD 下，第三方快递向客户指定地址交货并现场收款；
- 公司当时称 COD 覆盖 750 多个城市和城镇；
- delivery options 包括 courier、express courier、中国邮政普通邮件和 EMS；
- 中国邮政普通邮件/EMS 被描述为覆盖最广，包括偏远地区；
- 公司依赖大量第三方运输/快递公司，也直接监控履约表现。

来源：

- https://www.sec.gov/Archives/edgar/data/1499744/000095012310111515/h04369a4fv1za.htm

关键段落：checkout（约 L2948–2950）、Payment and Delivery（约 L3008–3018）、Customer Service（约 L3041–3055）。

### Evidence

- **Grade A**：同期公司监管申报。
- Confidence: **high** for “公司当时这样描述系统能力”；medium for 用户层面普遍体验。

### 能证明

到 2010 年，至少对当当而言：

- 收货地址不是单次网页文本，而是账号内可持久保存/调用的私人状态；
- checkout 会联合地址、配送和支付；
- shipment status 已有用户可查询表示；
- Web 订单必须落到现实物流网络才能完成。

### 不能证明

F-1 不能告诉我们：

- 2001/2003/2005 页面 DOM 长什么样；
- 2010 某个具体城市的某条街能否 COD；
- address 字段如何拆分省/市/区/街道；
- 是否有邮编必填；
- 是否校验地址；
- cookie/session 名；
- charset；
- browser requirement；
- 某笔订单最终由本人还是代理收件。

---

## 4. checkout default / explicit-choice gap

当当 F-1 说系统可以依据此前信息生成 preferred delivery address、shipping method 和 payment option。

因此历史研究必须区分：

1. 系统展示的 default；
2. 用户明确重新选择；
3. 用户没有注意到而沿用；
4. 最终 order record 中的值；
5. 履约过程中后来修改的值。

> **checkout 页面上预选了某地址 ≠ 用户在本次订单中主动确认那是当前住址。**

这在研究搬家、宿舍退住和多地址用户时尤其重要。

---

## 5. address-book / current-residence gap

一条历史 address-book entry 最多证明：

> 某账号在某时点保存过一组姓名、电话/联系方式与地址数据。

不能直接证明：

- 账号本人住在那里；
- 那是户籍/法定地址；
- 当时仍有效；
- 地址中的人仍同住；
- 订单实际送往此地址；
- 收件人亲自接收。

因此新增：

### **saved-address residue / 已保存地址残留**

人已经搬走，账号仍可长期保留旧公司、旧宿舍、旧家庭地址。

对 old-Web archive 来说，这类数据又通常位于登录后私人页面，正常情况下不应进入公共 WARC。

---

## 6. city-coverage / exact-address gap

当当 2010 称 COD 覆盖 750 多个城市和城镇。

这只能证明 **service-area claim**，不能变成：

> “该城市中的所有地址都能 COD。”

真实能力可能还依赖：

- 城/郊；
- 具体街区；
- 第三方 courier coverage；
- 商品类别；
- 金额；
- 配送时间；
- 临时服务中断；
- 地址能否被系统/人工识别。

因此字段应至少区分：

```yaml
platform_claimed_city_coverage:
exact_address_serviceability:
observed_checkout_option:
observed_successful_delivery:
```

四者不能互填。

---

## 7. COD 把“支付完成”拖到物理末端

当当的 COD 模式中，快递人员把商品送到指定地址，客户可在现场检查、接受或拒绝部分/全部商品，快递再收取实际接受商品的款项。

这意味着：

```text
order accepted
≠ sale economically final
≠ payment collected
≠ all shipped items accepted
```

新增：

### **physical-settlement gap / 物理结算缺口**

在 COD 环境里，Web 数据库里的 order 不是最终交易本身；最终结算要等现实门口/取件点的交接。

这也解释为什么“网上购物”在早期中国并不要求支付过程已经完全在线化。

---

## 8. 2006 近同时代材料：线上商店与现金末端并存

2006 年《华盛顿邮报》采访当当创始人俞渝与实际消费者。文章写到，公司早期曾高估信用卡适用性，后来转向 COD 与 postal money orders；一名 27 岁上海消费者描述自己多次使用当当并以现金购买。

来源：

- Jason Dean, “Chinese Online Retailer Thrives at Home,” 2006-08-21：https://www.washingtonpost.com/archive/business/2006/08/22/chinese-online-retailer-thrives-at-home-span-classbankheaddangdangcom-uses-local-savvy-regulations-to-fend-off-giant-foreign-rivalsspan/61796645-50ae-45ab-a48d-c677b28d72c7/

Evidence:

- **Grade B**：同期独立新闻 + 用户/公司采访。

它能交叉支持“Web 购买 + 现金末端”真实存在，但不能复原 checkout 页面。

---

## 9. 2014 京东 F-1：pickup endpoint 被纳入平台履约网络

JD.com 2014-05-19 的 F-1/A 声明，截至 2014-03-31：

- 86 个仓库；
- 1,620 个 delivery stations；
- **214 个 pickup stations**；
- 网络覆盖 495 个城市；
- 超过 70% 的订单在下单当天或次日送达（按公司口径）。

来源：

- https://www.sec.gov/Archives/edgar/data/1549802/000104746914005020/a2220187zf-1a.htm

Evidence:

- **Grade A**：同期监管申报。

### 新状态：pickup selection

电子商务末端不再只有：

```text
checkout address → courier → door
```

还可以是：

```text
checkout / account
→ selected or assigned pickup endpoint
→ parcel reaches station
→ user learns it is ready
→ user presents whatever retrieval credential is required
→ possession
```

因此新增：

### **pickup-station existence / user-selectability gap**

公司有 214 个 pickup stations，不等于：

- 每个用户在 checkout 都能选择；
- 每类商品支持；
- 每个站点当时开放；
- 站点地址在 archive 时点不变；
- 用户最终确实在那里取到。

---

## 10. order-status / physical-parcel gap

当当 2010 已允许用户查询 order/shipment status。

历史页面若幸存，状态可能包括类似：

- processing；
- shipped；
- delivered；
- cancelled；
- returned。

但无论具体词是什么，都必须避免：

> **UI label = 现实事件本体。**

应分别记录：

```yaml
platform_status_label:
status_observed_at:
carrier_scan_state:
recipient_report:
payment_state:
return_state:
```

尤其：

- `shipped` 不保证 carrier 已实际首扫；
- `out for delivery` 不保证收件人在场；
- `delivered` 不保证本人已取得；
- `signed` 不说明签收人身份；
- `return requested` 不保证货物已退回；
- `refund initiated` 不保证钱已到账。

---

## 11. recipient / proxy-recipient gap

中文旧网电商研究很容易把订单中的 `receiver_name` 当作“现实收到的人”。

现实末端可能由：

- 单位收发室；
- 门卫；
- 宿舍管理员；
- 同事；
- 室友；
- 家人；
- 物业；
- 自提点工作人员；
- 其他合法或非预期代理

完成交接。

因此：

> **named recipient ≠ handoff actor ≠ final possessor。**

这条 gap 应与 `how-people-lived` 的 proxy-receipt labor 交叉链接，而不在本仓扩写家庭史。

---

## 12. delivery-method display / actual-carrier gap

当当 2010 同时使用：

- 自身履约/物流组织；
- 104 家左右第三方运输/快递服务关系（公司口径）；
- China Post ordinary mail；
- EMS。

因此 checkout 中用户看见的 delivery method 未必等于最终现实执行主体。

需要区分：

```yaml
displayed_delivery_method:
platform_fulfillment_program:
actual_linehaul_provider:
actual_last_mile_provider:
```

历史材料如果只保存“快递配送”，不能擅自填实际承运商。

---

## 13. fulfillment visibility gap

公共网页通常能观察：

- 商品；
- 价格；
- 营销；
- 配送政策；
- 帮助中心。

用户登录后也许能观察：

- order status；
- shipment status；
- estimated date。

但真正决定是否成功的仓储和物流中间态大多不公开：

- 库存分配；
- 拣货；
- 打包；
- 分拨；
- carrier handoff；
- route exception；
- 地址人工修正；
- 丢件；
- 再投；
- 代收。

因此：

### **commerce control-surface / fulfillment-state asymmetry**

旧 Web 档案保存的是消费者能看到的控制面，而不是完整物流世界。

---

## 14. cookie-personalized checkout gap

当当 F-1 还明确称，其系统可以在用户登录前通过 cookie 中的浏览历史识别用户并做个性化推荐。

这提醒 old-Web replay：

同一个 URL 在 2010 年可能因：

- cookie；
- login；
- region；
- prior address；
- cart；
- account preference

而呈现不同状态。

因此即使 archive 保存了 checkout-related URL，也不能假设：

> capture = 当时所有用户的统一页面。

新增：

### **session-personalization gap / 会话个性化缺口**

公共 archive 往往没有原始用户 cookie/session，重放只能得到匿名或降级状态。

---

## 15. address-form schema 是生活史接口，但本轮不能反推

未来如果找到 1999–2010 checkout capture，应记录：

```yaml
receiver_name_field:
province_field:
city_field:
district_field:
street_field:
postal_code_field:
phone_field:
mobile_field:
company_or_school_field:
delivery_notes_field:
default_address_checkbox:
address_validation_behavior:
charset:
form_method:
form_action:
client_side_js:
login_requirement:
```

这些字段会决定平台如何把现实地点离散成数据库。

但本轮**没有取得 verified historical checkout memento**，所以以上字段全部保持 unknown。

不能从今天的当当/京东表单倒填到 2003、2006 或 2010。

---

## 16. 2008–2009 同期用户场景：页面后的现实末端确实已经进入校园

2008 年《中国青年报》报道义乌工商职业技术学院学生通过淘宝等平台经营网店，快递公司因学生接单发货需求而进入校园。

- https://zqb.cyol.com/content/2008-07/07/content_2252821.htm

2009 年《中国青年报》在大学生网购报道中写到，校园宿舍楼下中午会出现一排快递公司邮件/包裹。

- https://zqb.cyol.com/content/2009-10/31/content_2913516.htm

Evidence:

- **Grade B**：同期新闻与现场观察。

这些材料可以证明：

> 某些校园在 2008–2009 已经形成 Web order ↔ campus delivery 的真实生活整合。

它们不能证明：

- 具体 checkout 字段；
- 全国高校普及；
- 每个学生自己的订单/地址；
- 快递后台状态。

---

## 17. 一个旧网页为什么会夸大“可购买性”

### product-page survival bias

商品详情页是公开、链接密集、SEO 价值高的资源，更容易被搜索与 archive 保存。

而：

- checkout；
- address book；
- order history；
- shipment tracking；
- COD eligibility；
- pickup selection

往往需要登录、session 或实时后台。

因此 archive 会系统性制造一种错觉：

> **商品世界保存得很完整，交易世界保存得很残缺。**

看到 2006 年某本书的商品页，不应写成“2006 年任何访问者都可以成功买到并送到家”。

---

## 18. delivery-success survival bias

一次成功配送通常不会产生公开 Web 文档。

反而更可能留下公开痕迹的是：

- 平台帮助页；
- 配送政策；
- 抱怨；
- 新闻事故；
- 公司宣传；
- 上市申报。

所以历史记录会同时低估“平凡成功的千万次交接”，又高估争议案例的可见度。

这与 forum/public-page 研究中的 encounter-history darkness 类似，但对象变成：

### **delivery-outcome darkness / 配送结果黑区**

我们知道系统宣称能送，却很少知道普通某一单到底怎样到手。

---

## 19. return-path gap

当当 2010 F-1 已明确存在在线退换申请、客服审核、部分城市 courier pick-up、现金或账户/银行卡退款。

因此交易完成以后仍有第二条状态链：

```text
possession
→ defect / unwanted item
→ return eligibility
→ online request
→ approval
→ courier pickup / customer ship-back
→ warehouse receives
→ inspection
→ refund initiated
→ refund available
```

不能把 `return policy exists` 写成 `return succeeded`。

也不能把 `courier pickup offered in major cities` 外推到全国。

---

## 20. 与 1990 邮政投递结构的必要前史边界

`old-web-archaeology` 的主 scope 不前移到 1980s/1990 年邮政史。

但理解中文电商末端时，需要保留一个前史边界说明：1990 年《邮政法实施细则》已经规定多种现实投递端点：居民信报箱/收发室、单位收发室、农村固定点、邮政信箱、存局候领、代理领取。

官方数字文本：

- https://www.hengqin.gov.cn/lab/flfg/sgaflfg/xzfg/content/post_3861566.html

这只用于说明：

> **Web 电商没有发明“住宅以外的投递端点”；它把地址、配送选择、支付、状态查询和物流网络重新接进了账号与 checkout。**

前互联网普通生活变化的主体分析留在 `how-people-lived`。

---

## 21. 必须记录的 state gaps

本专题新增/固定：

1. `product-page / orderability gap`
2. `price-display / checkout-price gap`
3. `account-exists / account-usable gap`
4. `address-book / current-residence gap`
5. `saved-address / selected-address gap`
6. `selected-address / exact-serviceability gap`
7. `city-coverage / street-coverage gap`
8. `displayed-delivery-method / actual-carrier gap`
9. `COD-city / COD-order gap`
10. `checkout-default / explicit-choice gap`
11. `order-submitted / order-accepted gap`
12. `accepted-order / inventory-allocation gap`
13. `shipment-status / physical-parcel gap`
14. `out-for-delivery / recipient-reachable gap`
15. `named-recipient / handoff-actor gap`
16. `handoff-actor / final-possessor gap`
17. `delivery-scan / actual-possession gap`
18. `pickup-station-exists / user-selectable gap`
19. `pickup-selected / parcel-ready gap`
20. `parcel-ready / user-collected gap`
21. `return-policy / return-eligibility gap`
22. `return-request / return-received gap`
23. `refund-issued / funds-available gap`
24. `public-page / private-transaction-state gap`
25. `archive-capture / authenticated-session gap`
26. `anonymous-replay / personalized-checkout gap`
27. `historical-address / modern-address-label gap`
28. `platform-status / physical-world-event gap`

---

## 22. Evidence register

| Claim | Evidence | Grade | Confidence | Boundary |
|---|---|---:|---|---|
| 2010 当当账号保存 shipping/payment preference | Dangdang SEC F-1/A | A | high | 公司申报，不是历史页面 capture |
| 2010 当当 COD 覆盖 750+ 城镇 | Dangdang SEC F-1/A | A | high for claim | 不等于精确地址全覆盖 |
| 2010 用户可跟踪 order/shipment status、修改 delivery info | Dangdang SEC F-1/A | A | high | 不知道 UI/字段/charset |
| 2006 当当真实用户使用现金购买 | Washington Post 同期采访 | B | medium-high | 单个/少量用户不能代表总体 |
| 2008 校园网店与快递入校 | China Youth Daily | B | high for case | 不外推全国 |
| 2009 宿舍楼下形成快递交接场景 | China Youth Daily | B | high for observed scene | 不证明每校/每天 |
| 2014 京东 214 pickup stations / 495 城 | JD SEC F-1/A | A | high for company claim | 不等于每用户可选择 |
| 1990 中国已有多类型现实投递端点 | 国务院实施细则 | A | high | 仅作必要前史，不扩仓 scope |

---

## 23. 本轮 negative result

### 未取得 verified historical checkout capture

本轮搜索了：

- early Dangdang checkout / 收货地址 / COD 线索；
- 2000s 中文报道与公司申报；
- 2010 Dangdang SEC F-1；
- 2014 JD F-1。

但没有取得一份能够实际打开并核验以下字段的 **1999–2010 中文电商 checkout Wayback/WARC memento**：

- original URL；
- capture datetime；
- HTTP/replay state；
- charset；
- DOM；
- form method/action；
- address field names；
- login/session requirement；
- JS；
- cookie；
- delivery option control；
- COD eligibility UI；
- order-status endpoint。

因此本稿只是 **state-gap research note**，不是 M1 完整 archaeological case。

这符合 `docs/METHOD.md`：搜索/二手证据证明功能存在，不等于 verified capture。

---

## 24. Privacy stop condition

checkout、地址簿、订单历史、收件电话本来就是私人状态。

后续考古必须遵守：

- 不尝试登录历史普通用户账号；
- 不公布残存普通用户真实收货地址/电话；
- archive 偶然保存含个人地址页面时，优先记录结构而非重新发布值；
- 不用现代泄露数据库补“历史 checkout”；
- 不把隐私数据缺失当成需要修复的 archive failure。

### **privacy-protecting archive asymmetry**

对电子商务而言，公共档案保存商品页而不保存私人地址/订单，很多时候恰恰是正常且应当的。

---

## 25. 下一步最值钱的 M1 候选工作

目标不是再找公司规模数字，而是找到一份**可以实际验证的中文电商历史 checkout capture**，最好满足：

1. 2003–2010；
2. original URL 可确认；
3. 至少两个 capture datetime；
4. 能观察 charset / form / JS / address controls 中至少若干项；
5. 不含普通个人敏感数据；
6. 有同期官方帮助页或用户教程作为第二 evidence family。

候选方向：

- 当当公开帮助/配送说明页，而不是私人订单页；
- 卓越/亚马逊中国公开 checkout help；
- 京东早期公开购物流程/帮助页；
- 淘宝公开买家帮助页中的收货地址/确认收货流程。

如果只能找到 locator、截图或后来教程，应继续保持 `candidate / unknown`，不升级成 capture。

---

## 26. Cross-repo conclusion

`how-people-lived` 关心的是：

> 一个没有稳定住房、频繁换宿舍/单位/城市的人，怎样仍然让现实物品找到自己。

`old-web-archaeology` 在这里能贡献的不是“电商发展很快”，而是指出 Web 能留下什么、不能留下什么：

> **公开商品页面幸存得最好；决定普通人是否真正收到东西的地址、session、配送资格、物流中间态和门口交接，恰好最容易消失。**

所以研究旧电商时，最危险的捷径是把“可浏览”直接写成“可购买”，再把“可购买”写成“已送达”。
