# PARCEL_EXPRESS_TRACKING_WAYBILL_SCAN_DELIVERY_AND_MATERIAL_MOBILITY_STATE_GAPS_2004_2015

> 研究对象：2004—2015 中文旧网中的快递/邮政查询页面、运单号、扫描事件、客服/短信/Web 多通道查询，以及这些页面与现实包裹运输之间的状态缺口。
>
> 本文不是“中国快递业史”，也不把 1994 年以前的邮政数字化扩成 old-web 主体。1994 年前后的 EMS 跟踪网络只作为理解 2004—2015 公共 Web 查询为何可能存在的前史边界；全球物流史与跨国生活史主要放在 `tmzncty/how-people-lived` companion。
>
> Life-history companion：`tmzncty/how-people-lived/topics/from-carrying-everything-yourself-to-sending-luggage-ahead-parcel-tracking-and-material-portability-china-1980-2026.zh-CN.md`
>
> 检索日期：2026-09-08。

---

## 1. 为什么快递查询页是旧网考古对象

一个历史快递查询页面看起来很简单：

```text
输入运单号
→ 点击查询
→ 看见“已收寄 / 转运 / 派送 / 签收”
```

但真正事务至少跨过：

```text
实物被收寄
→ 运单建立
→ 网点扫描
→ 分拣/运输
→ 运输系统写入状态
→ 查询数据库可读
→ Web/SMS/客服接口取回
→ 用户得到文本
→ 用户理解
→ 现实包裹继续移动
→ 末端交付
→ 收件人真正拿到物品
```

因此不能把：

- `tracking page exists`
- `tracking form submits`
- `backend returns a record`
- `record says delivered`
- `recipient actually has parcel`

写成同一个状态。

本专题增加七个旧网状态变量：

1. **waybill-state separation / 运单—实物状态分离**：数据库里的事件与现实物体之间不是一一实时映射；
2. **scan-event latency / 扫描事件时延**：扫描发生时间、同步时间和用户查询时间可以不同；
3. **query-channel divergence / 查询通道分歧**：网站、短信、11185/客服可能从不同缓存、接口或更新周期得到信息；
4. **tracking-shell vs logistics-backend / 查询壳与物流后台分离**：archive 可能保存表单 HTML，却保存不了动态查询结果与内部业务系统；
5. **last-mile handoff gap / 末端交付缺口**：派送、签收、本人持有必须拆开；
6. **trust-interface layer / 信任界面层**：用户把域名、品牌、查询结果当作“这个包裹是真的在走”的证据，仿冒站也会复制这种外观；
7. **aggregator-normalization gap / 聚合器标准化缺口**：第三方多快递查询页把不同承运商状态归一化以后，显示文本不必等于承运商原始状态字段。

---

## 2. 前史边界：1994 EMS 跟踪查询网不能自动写成 public Web

后来的 EMS 企业史材料常记录 **1994 年 1 月 18 日**开通邮政特快专递跟踪查询网。

Source:
https://wapbaike.baidu.com/item/中国邮政速递物流股份有限公司/6597081

Evidence grade: **C/B mixed later corporate-history relay**.  
Confidence: **medium**.

这个节点值得保留，但它早于中国 **1994 年 4 月 20 日**实现与国际 Internet 的全功能连接。中国在此以前已有科研网络、电子邮件和其他前互联网/专线数字通信，因此不能说“1994 年前完全没有网络”；同样，也不能反过来把一个业务查询网写成普通家庭已经能在 Netscape/IE 中打开的公共 WWW 页面。

Institutional historical sources:
- https://www.cac.gov.cn/2024-04/20/c_1715291120716362.htm
- https://www3.cnnic.cn/n4/2022/0401/c87-912.html

Evidence grade: **A/B institutional history**.

old-web 的边界写法应是：

```text
1994-01：EMS 有“跟踪查询网”历史记录
    ↓ 技术入口、用户对象、网络层未知
1994-04-20：中国实现全功能 Internet 连接
    ↓
1995+：公共 Web 逐步发展
    ↓
2004—2005：同期媒体明确证明普通用户可用网站查询 EMS 状态
```

因此：

**`backend tracking network exists != public Web tracking exists`。**

---

## 3. 2004：同期媒体已经明确把 Web 与 SMS、电话并列为用户查询通道

2004 年 8 月 EMS“全夜航”开通的同期《新闻晨报》报道写明，在 136 个大中城市间的 EMS“次日递”安排中，用户可以通过**网站、短信、电话**查询自己交寄快件的状态。

Source:
https://finance.sina.com.cn/b/20040819/1147960712.shtml

Evidence grade: **B contemporaneous media**.  
Confidence: **high** for advertised channel availability; **unknown** for browser implementation and household use rate.

这一材料能证明：

- 2004 年已经存在面向公众的 Web 查询路径；
- Web 并不是唯一入口；
- 同一个现实包裹的状态可能通过短信、电话和网站三套用户界面暴露。

它不能证明：

- 网站首页历史 DOM；
- 表单 `action`；
- charset；
- 是否依赖 JavaScript/cookie；
- 查询结果页面 URL 结构；
- 每个快件都按同样粒度更新；
- 用户真的更常用网站而不是电话。

---

## 4. 2005：取得精确 historical locator `www.ems.com.cn`

2005 年两组同期媒体材料明确写到：用户可以拨打 `11185`，或者访问中国邮政 EMS 网站 `www.ems.com.cn` 查询两地时限与邮件传递信息。

Sources:
- https://news.sina.com.cn/o/2005-07-26/03306526163s.shtml
- https://news.sohu.com/20050513/n225556766.shtml

Evidence grade: **B + B contemporaneous media, separate media families**.  
Confidence: **high** for hostname and advertised query function.

因此可登记：

```yaml
historical_locator:
  host: www.ems.com.cn
  observed_year: 2005
  evidence_grade: B
  proved:
    - public-facing EMS Web host existed in contemporaneous reporting
    - users were told they could query mail-transfer information there
  not_proved:
    - exact historical HTML
    - exact path/form action
    - browser requirements
    - result-page structure
    - archive capture
```

这仍然只是 locator，不是 capture。

---

## 5. 一个查询事务至少要拆成两条状态机

### 5.1 现实物流状态机

建议最低模型：

```text
WAYBILL_CREATED
→ ACCEPTED
→ ORIGIN_SCAN
→ SORTED
→ DEPARTED_ORIGIN
→ ARRIVED_TRANSIT
→ DEPARTED_TRANSIT
→ ARRIVED_DESTINATION
→ OUT_FOR_DELIVERY
→ DELIVERY_ATTEMPTED
→ DELIVERED / HELD / FAILED / RETURNED
→ RECIPIENT_ACTUAL_POSSESSION
```

不能把这些合并成：

`shipping = true`。

### 5.2 Web 查询状态机

```text
HOST_RESOLVES
→ HOMEPAGE_LOADS
→ TRACKING_FORM_VISIBLE
→ USER_HAS_VALID_WAYBILL_NUMBER
→ NUMBER_ENTERED
→ REQUEST_SUBMITTED
→ SERVER/BACKEND_ACCEPTS_QUERY
→ RECORD_FOUND / NOT_FOUND / ERROR
→ RESULT_RENDERED
→ USER_READS_RESULT
→ USER_INTERPRETS_STATUS
```

这里有至少五类 gap：

1. **页面 gap**：首页加载了，表单脚本未必能工作；
2. **session gap**：表单可能需要 cookie、验证码或动态 token；
3. **backend gap**：archive 可能回放 HTML，但历史业务数据库早已不存在；
4. **semantic gap**：显示“到达处理中心”不等于用户知道还要等多久；
5. **physical gap**：数据库事件不是 GPS 连续轨迹。

---

## 6. `event_time != sync_time != query_time`

旧快递查询尤其需要保存三个时间：

```text
physical/event time
→ scan/write time
→ backend synchronization time
→ user query time
```

例如一个包裹 14:10 离开分拨中心：

- 14:08 可能提前批量完成装车扫描；
- 14:35 扫描数据才同步到中心；
- 15:00 用户第一次刷新网站；
- 页面显示的文本未必说明这三个时间的差异。

因此历史页面中的一个时间戳只能先按**页面字段本身**记录，不能自动解释成“包裹在这一秒物理上位于这里”。

固定：

**`scan timestamp != continuous physical location truth`。**

---

## 7. 2007：仿冒 EMS 网站证明查询页已经成为“真实性界面”

2007 年宁波《现代金报》报道，一名网名“狷人”的用户在论坛求购一本书后，被引向一个仿冒“中国邮政速递”网站。记者当时实际把假站与真正的 `https://www.ems.com.cn` 比较，指出假站模仿 EMS 标志，以及“邮件查询、公司简介、资费”等栏目，还伪造了所谓“在线支付”功能。

Source:
https://news.sohu.com/20070208/n248113551.shtml

Evidence grade: **B contemporaneous media + contemporaneous user report**.

个人材料分类：

- **contemporaneous self-report**：用户描述论坛求购、进入网站和识别骗局的过程；
- **platform/page observable**：记者当时观察真假站的栏目与功能差异；
- **media reconstruction**：完整事件顺序经记者整理；
- **not independently logged**：没有用户 HAR、浏览器历史或原始 HTTP 记录。

这个事件说明：

```text
品牌标志
+ 看起来像官网的页面
+ 可输入单号的查询框
+ 看似正规的状态/资费说明
```

已经足以构成交易信任的一部分。

因此：

**`tracking result appears plausible != site is authentic`。**

旧网复原如果只追求“看起来像当年”，反而可能错过最重要的历史事实：当时人已经需要判断“这个看起来像官网的页面究竟是不是真的”。

---

## 8. 域名、HTTPS 与当前站点不能倒灌历史实现

2007 报道使用 `https://www.ems.com.cn` 表述真实站点，但这不等于我们已经验证：

- 当时用户默认入口一定是 HTTPS；
- 当时 TLS 版本、证书链与今天一致；
- 所有查询流程全程 HTTPS；
- 2004/2005 同样使用 HTTPS；
- 当前同域名页面与当年系统同构。

历史重建必须按时点分别证明：

```text
host
scheme
path
redirect
certificate/TLS if observable
charset
DOM
form action
subresources
session/cookie
```

同一个 host 十年后仍活着，只能证明**域名连续性的一部分**，不能证明页面或后台连续性。

---

## 9. 电话 / SMS / Web 不是三份独立“真相”

2004—2005 的同期材料反复把网站、短信和 `11185` 并列。

可能的抽象结构是：

```text
物流业务数据库
├─ staff/customer-service terminal → 11185 人工/语音答复
├─ SMS gateway → 短信结果
└─ Web query frontend → 浏览器结果
```

这是 **engineering reconstruction / D**，不是当前已经证实的 2005 EMS 架构。

必须保留替代解释：

- 三个渠道可能调用不同中间系统；
- 缓存刷新周期可能不同；
- 客服人员可能看到比 Web 更多字段；
- SMS 可能只返回最后一条摘要；
- Web 可能显示完整事件列表。

因此：

**`same waybill number != identical state visibility across channels`。**

下一步应寻找内部技术手册、通信接口论文或同期用户对比记录，而不是直接把现代 API 思维塞回 2005。

---

## 10. 2010：多承运商查询开始增加一层“聚合器”

快递100 当前官方 About 页面称平台于 **2010 年 6 月 22 日**上线，定位于多家快递公司的智能查询、状态推送等服务。

Source:
https://www.kuaidi100.com/about/

Evidence grade: **C/A-current corporate retrospective**.  
Confidence: **medium-high** for company-stated launch date; **not a historical capture**.

这为 2010—2015 中文旧网增加了一层新状态：

```text
用户输入单号
→ 聚合器判断/选择承运商
→ 聚合器向承运商数据源查询
→ 承运商返回原始状态
→ 聚合器映射/标准化
→ 用户看到统一界面
```

建议状态机：

```text
WAYBILL_INPUT
→ CARRIER_SELECTED / AUTO-DETECTED
→ UPSTREAM_REQUEST
→ UPSTREAM_RESPONSE
→ NORMALIZATION
→ DISPLAY
```

新增边界：

- `aggregator result != carrier primary record`
- `carrier auto-detected != correct carrier`
- `normalized “in transit” != upstream status vocabulary preserved`
- `aggregator page archived != upstream API archived`

第三方聚合器反而更容易在 archive 里留下“页面壳”，却更难留下当年真实的动态结果。

---

## 11. Archive 最可能保存壳，最容易丢掉事务

快递查询属于典型的 **dynamic database artifact**。

一个 archive 即使完整保存：

- logo；
- 导航；
- 查询输入框；
- CSS；
- 帮助页；

也可能完全没有保存：

- 查询提交 endpoint；
- 历史业务数据库；
- 某个真实运单号的事件链；
- 验证码；
- AJAX/XHR；
- session；
- 上游承运商接口；
- 查询结果动态 HTML。

所以必须固定：

**`tracking-shell capture != tracking-transaction capture`。**

反过来也一样：今天如果向当前 EMS/聚合器后台提交一个旧单号并得到“无记录”，不能据此证明 2005 年当时没有记录。

**`current backend miss != historical backend miss`。**

---

## 12. 末端状态必须继续拆：`delivered != recipient possession`

用户真正关心的不是数据库状态，而是东西有没有进入生活。

最低末端模型：

```text
ARRIVED_DESTINATION_CITY
→ ARRIVED_DELIVERY_STATION
→ OUT_FOR_DELIVERY
→ COURIER_CONTACTED_RECIPIENT
→ DELIVERY_ATTEMPT
→ HANDED_TO_RECIPIENT / PROXY / DOORMAN / DORM / PICKUP_POINT
→ SYSTEM_MARKED_SIGNED
→ RECIPIENT_NOTIFIED
→ RECIPIENT_ACTUALLY_POSSESSES_PARCEL
```

因此：

- `arrived city != available for pickup`
- `out for delivery != delivery attempt completed`
- `signed != signed by recipient`
- `signed != recipient has opened/checked contents`
- `recipient has parcel != contents intact`

2010s 后校园驿站、代收点和快递柜会进一步把“系统签收”和“本人拿到”拆开；这些 afterlife 可用于校验 earlier state model，但不应把 old-web scope 无限后移。

---

## 13. 一次“查询不到”也不是一个简单负状态

历史 Web 查询可能返回：

```text
NO_RECORD
INVALID_NUMBER
NOT_YET_SYNCED
EXPIRED_RECORD
WRONG_CARRIER
BACKEND_TIMEOUT
MAINTENANCE
SESSION/VALIDATION_ERROR
NETWORK_ERROR
HTML/JS_FAILURE
```

对 2004—2015 旧网考古来说尤其重要，因为：

- 用户可能把“还没同步”理解成“快件没收寄”；
- archive 可能把后端错误页保存成普通页面；
- 今天重放旧表单时得到 404/空结果，可能只是 endpoint 已消失；
- 同一个单号多年以后可能已经被系统清理或循环使用。

因此：

**`no visible tracking result != parcel did not exist`。**

---

## 14. 用户真正执行的不是“看网页”，而是降低等待中的不确定性

旧网页面的生活价值来自它与现实物品绑定：

```text
毕业生把一箱书寄回家
→ 得到运单号
→ 晚上在宿舍/网吧/家里输入
→ 看见已经离开发件城市
→ 决定不用明早去网点问
```

因此 old-web 不能只保存页面美术风格。

至少要问：

- 查询是否真的可提交？
- 用户需要什么单号格式？
- 结果按事件列表还是最后状态显示？
- 是否有时间和地点字段？
- 是否解释异常状态？
- 查询失败后提示用户打什么电话？
- 用户是否需要 IE/特定编码？
- 状态变化多久刷新？

页面只是**把现实物流系统的一部分状态暴露给普通人**的窗口。

---

## 15. 浏览器与编码：现阶段必须明确保持 unknown

当前证据能够证明 2004—2005 Web 查询存在，却不足以证明历史前端技术细节。

现阶段不得直接写：

- “必须 IE6”；
- “使用 ActiveX”；
- “页面是 GB2312”；
- “表单使用某个 CGI/JSP/ASP endpoint”；
- “必须开启 JavaScript”；
- “结果用 frameset/iframe”；
- “验证码从某年已经存在”。

这些都需要 capture、手册、同期教程或源码级 evidence。

建议下一轮优先寻找：

1. 2004—2007 `ems.com.cn` 历史 capture；
2. 同期浏览器操作教程；
3. 查询页面截图；
4. HTML/JS/CSS；
5. 缓存或搜索引擎保存的 URL pattern；
6. 当时用户投诉中的错误信息。

---

## 16. 隐私：运单号不是无害的“旧网页测试数据”

历史运单可能与：

- 姓名；
- 电话；
- 地址；
- 物品；
- 时间；
- 工作/学校地点；

形成关联。

即使某个旧单号今天仍能查询，也不应为了复原页面批量重新公开普通人的物流轨迹。

仓库应优先保存：

- form pattern；
- endpoint metadata；
- 空白/无敏感信息的测试状态；
- 同期官方截图；
- 研究者自己构造的 reconstruction（明确标识）；

而不是把偶然找到的普通个人运单记录当 fixture。

---

## 17. 历史可见性偏差：数据库越丰富，公共 archive 反而越贫

物流系统会产生极高密度的数字记录，但这些记录通常是：

- 私有业务数据；
- 动态查询；
- 短期留存；
- 需要单号才可访问；
- 不被搜索引擎索引；
- 不适合 archive crawler 穷举。

所以几十年后研究者看到的可能主要是：

```text
官网首页
帮助页
新闻稿
媒体截图
资费说明
```

而普通人真正反复刷新的：

```text
2005-07-26 18:32 发件局收寄
2005-07-27 xx:xx 到达处理中心
...
```

却全部消失。

这形成一个重要偏差：

**`archive-visible parcel Web != lived parcel Web`。**

旧网的事务性日常，可能恰恰比公开内容页更难保存。

---

## 18. 与仓库已有专题的边界

本专题不重复：

- `ECOMMERCE_CHECKOUT_DELIVERY_ADDRESS_PICKUP_AND_FULFILLMENT_STATE_GAPS_1999_2015.md`：后者从商品订单看履约；本专题从**已有实物/个人包裹 + 运单查询**看运输状态；
- `SECONDHAND_*`：后者研究所有权转移；本专题允许物主不变；
- `RAILWAY_TICKET_*`：后者研究人的席位与出行资格；本专题研究物不占乘客席位时怎样走；
- `ONLINE_BANKING_*`：后者研究钱的 clearing/availability；本专题研究物的 custody/scan/delivery。

跨仓 synthesis 可把一个迁移者的基础设施拆成：

```text
人：ticket / ID / transport
钱：remittance / bank / payment
关系：phone / IM / video
物：parcel / express / storage / tracking
```

---

## 19. Claim list 与证据等级

| Claim | Evidence | Grade | Confidence |
|---|---|---:|---:|
| 1994-01 EMS 有“跟踪查询网”历史记录 | 后来企业史整理 | C/B | medium |
| 1994-04-20 中国实现全功能 Internet 连接 | CNNIC / CAC | A/B | high |
| 2004 EMS 用户可通过网站/SMS/电话查询状态 | 同期新闻晨报 | B | high |
| 2005 `www.ems.com.cn` 提供邮件传递查询 | 两个同期媒体家族 | B+B | high |
| 2007 真/假 EMS 网站已围绕查询功能争夺信任 | 现代金报同期调查 | B | medium-high |
| 2010 快递100上线 | 当前官方公司史 | C/A-current | medium-high |
| 历史 EMS 查询 form action / charset / JS | 未验证 | unknown | low |
| 历史查询结果页 DOM / API | 未验证 | unknown | low |
| 网站/SMS/11185 是否同一实时数据源 | 仅工程假设 | D | low |

---

## 20. 本轮 archive / M1 状态

### 已得到的 locator

- `www.ems.com.cn` — 2005 同期媒体直接给出；
- `https://www.ems.com.cn` — 2007 同期媒体用于指认真实 EMS 站；
- `www.kuaidi100.com` — 当前官方公司史用于 2010 上线线索。

### 本轮没有验证到的内容

尝试继续向 Internet Archive / Wayback 的 `ems.com.cn` 历史 replay 推进，但当前工具链没有取得一份能实际检查以下字段的 capture：

- `capture_datetime`；
- original URL；
- HTTP status / redirect；
- Content-Type / charset；
- DOM；
- tracking form action；
- JS / cookie / session；
- result page；
- subresources。

因此：

**M1: NOT ACHIEVED IN THIS SLICE**。

按照 `docs/METHOD.md`，这里只能写“本轮没有验证到合格 historical capture”，不能写“Wayback 没保存”。locator 也不能冒充 capture。

---

## 21. 下一步优先任务

### A. 把 `ems.com.cn` 2004—2007 从 locator 推到 verified capture

每个 capture 记录：

```yaml
archive_source:
capture_url:
original_url:
capture_datetime:
http_status:
content_type:
charset:
redirect_chain:
main_document_saved:
subresources_saved:
tracking_form_present:
form_action:
method:
js_required:
cookie_required:
result_endpoint_archived:
browser_assumption:
```

### B. 找同时期用户教程/投诉

优先查：

- “EMS 单号 查询不到”；
- “邮件号码 查询”；
- “11185 和网上查询不一致”；
- “签收了但没收到”；
- “快递网站打不开”；
- 网吧/IE 环境下查询教程。

目标不是猎奇，而是取得真实 error states。

### C. 2010—2012 聚合器状态对比

如果取得快递100等早期页面：

- 比较承运商原始 status wording；
- 比较聚合器 normalized wording；
- 记录自动识别承运商的失败状态；
- 检查 AJAX/JSONP/API 是否被 archive 保存。

### D. 保存“查询壳活着、事务死了”的案例

特别寻找：

- archive 中表单仍在，但 submit 目标 404；
- JS 仍在，但 API host 消失；
- 页面能输入单号，但验证码资源缺失；
- 查询结果依赖当前后台，已经不可能重放历史数据。

这类失败本身就是 old-web preservation 的高价值证据。

---

## 22. 反例与后见之明风险

### 22.1 不要写“Internet 发明了快递追踪”

物流内部扫描、条码、业务查询网络可以早于 public Web。Web 的变化主要是让普通客户自己看见一部分后台状态。

### 22.2 不要写“2005 有网站，所以人人都网上查”

同期证据明确仍把电话和 SMS 并列。不同设备、接入费用、地点与用户习惯会决定实际渠道。

### 22.3 不要把当前 `ems.com.cn` 页面当 2005 页面

host 连续性不等于页面/后台/浏览器连续性。

### 22.4 不要用今天无记录证明历史无记录

业务数据库有 retention lifecycle；运单可能清理、迁移、格式改变。

### 22.5 不要把状态文字当物理连续定位

扫描事件只能证明某个业务节点产生过一条记录，不能自动证明物在整段间隔中的精确位置。

### 22.6 不要把“签收”当本人收到

代收和末端 handoff 会让数据库状态先于本人持有。

---

## 23. 它改变了我们怎样理解中文旧网

中文旧网不只是论坛帖子、个人主页和门户新闻。

到 2004—2005 年，一个很普通的 Web 页面已经可能和现实中一只纸箱绑定：用户输入十几位运单号，页面从一个不可见的物流后台取出几条状态，让远处的人知道自己的书、衣服或文件有没有离开发件城市。

这类页面的历史意义恰恰不在视觉设计，而在它是一个**跨物理世界的状态窗口**。

但也正因为如此，它极难保存完整：

- HTML 壳可能留下；
- CSS 可能留下；
- 查询框可能留下；
- 真正的业务数据库、运单事件和查询结果却可能全部消失。

所以以后看到一张保存完好的“快件查询”旧页面，最重要的问题不是“它长什么样”，而是：

> **当年一个普通人把单号输进去以后，哪套现实系统真的回答了他？回答的那几行字，又和那只正在几百公里外移动的箱子相差多远？**
