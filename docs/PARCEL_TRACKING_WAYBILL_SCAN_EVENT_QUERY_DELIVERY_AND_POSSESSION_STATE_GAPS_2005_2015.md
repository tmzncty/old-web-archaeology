# 中文旧网包裹 tracking、运单、扫描事件、妥投与占有状态缺口（2005–2015）

> Status: incremental archaeology note
>
> Parent: [`../ECOMMERCE_CHECKOUT_DELIVERY_ADDRESS_PICKUP_AND_FULFILLMENT_STATE_GAPS_1999_2015.md`](../ECOMMERCE_CHECKOUT_DELIVERY_ADDRESS_PICKUP_AND_FULFILLMENT_STATE_GAPS_1999_2015.md)
>
> Life-history companion: `tmzncty/how-people-lived/topics/from-postal-inquiry-to-parcel-tracking-delivery-state-legibility-and-waiting-uncertainty-china-1980-2026.zh-CN.md`

## 0. Scope：不再写第二篇“电商履约史”

父稿已经完整区分 product page、cart、checkout、order、payment、shipment、delivery attempt、pickup endpoint、possession 与 return/refund，并已用 2010 当当 SEC F-1 证明当时账号自助系统可以查询 order/shipment status 和预计送达日期。

本稿只补父稿中仍然太粗的一段：

> **一个 physical parcel 怎样被运单号和扫描事件表示成 Web 上可查询的 tracking state；历史研究者怎样避免把“查询页显示某状态”误写成物体连续位置、现实签收或本人占有。**

时间范围严格保持在约 2005–2015 中文 Web。1994 EMS “跟踪查询网”只作为直接必要的边界前史，不把本仓扩成全球物流史；FedEx 等全球对照放在 `how-people-lived`。

---

## 1. 研究单位：必须再拆一层

父稿的 `shipment` 对 tracking archaeology 仍然太大。至少应区分：

- **order**：商家/平台接受的一次购买或寄递请求；
- **shipment**：与现实物流对应的一次运输对象；
- **parcel / mail item**：实际移动的物体；
- **waybill / tracking number**：系统赋予运输对象的一串标识；
- **barcode / machine-readable identifier**：供节点设备扫描的机器可读表示；
- **scan event**：某设备/工作人员在某节点记录的一次事件；
- **carrier event record**：承运商后台持久化的事件；
- **normalized tracking event**：聚合器把不同承运商状态映射后的表示；
- **tracking query**：用户输入单号/账号发起的一次查询；
- **tracking result page / component**：某次查询生成的网页表示；
- **notification**：SMS、站内、邮件/App 等推送；
- **delivery attempt**：现实末端的一次尝试；
- **proof of delivery / POD**：系统认为交付完成的证据/状态；
- **proxy recipient**：门卫、前台、家人、同事、代收点、快递柜等；
- **named recipient possession**：指定收件人本人实际取得；
- **archive capture**：档案服务在某时刻保存的页面/子资源。

不能把任何两个层级默认合并。

---

## 2. 最小 tracking 状态链

```text
order / shipment request
→ waybill number allocated
→ label generated
→ physical parcel prepared
→ carrier actually accepts parcel
→ first physical scan
→ scan event stored in carrier backend
→ tracking backend exposes event
→ user query returns result
→ user actually sees result
→ origin processing
→ line-haul / transfer
→ destination processing
→ out for delivery
→ delivery attempt
→ POD / delivered / 妥投 / signed state
→ proxy or named recipient access
→ named recipient possession
→ possible loss/dispute/return
→ record eventually expires / becomes unavailable
```

必须固定以下硬边界：

> **waybill exists ≠ carrier physically has parcel**
>
> **seller says “shipped” ≠ first carrier acceptance scan exists**
>
> **scan event exists ≠ parcel is continuously located**
>
> **destination-center scan ≠ out for delivery**
>
> **out for delivery ≠ delivered**
>
> **delivered / 妥投 / signed ≠ named recipient possession**
>
> **tracking result visible now ≠ historical user saw the same result at the same time**

---

## 3. 中国边界前史：1994 “跟踪查询网”不能偷换成 public Web

后来的 EMS 历史资料普遍记载，1994-01-18 开通“邮政特快专递跟踪查询网”，实现快件“网上跟踪查询”。

候选来源：

- 中国邮政 EMS 后期历史汇总：<https://wapbaike.baidu.com/item/%E4%B8%AD%E5%9B%BD%E9%82%AE%E6%94%BF%E9%80%9F%E9%80%92%E7%89%A9%E6%B5%81%E8%82%A1%E4%BB%BD%E6%9C%89%E9%99%90%E5%85%AC%E5%8F%B8/6597081>
- evidence: **C/B-low，后期汇总；本轮尚未取得 1994 同期网络技术说明**

由于这一日期早于中国 1994-04-20 全功能接入国际互联网节点，且现有材料没有交代终端/协议/公众访问路径，本仓只登记：

```yaml
1994-01-18:
  claim: postal express tracking-query network reported as opened
  public_world_wide_web: not established
  ordinary_household_access: not established
  terminal_and_protocol: unknown
```

这条前史只用于阻止两种错误：

1. “1994 前完全没有数字 tracking”；
2. “1994 年初普通家庭已经在 Web 浏览器里查 EMS”。

目前两者都不能成立。

---

## 4. 2005：可定位的 public-Web EMS 查询 URL

2005-11-17，博客园《在线查询大全》列出：

`http://www.ems.com.cn/ems/index.jsp`

并将它标成 EMS 全球快递邮件号查询入口。

来源：

- <https://www.cnblogs.com/Qia_sky/archive/2005/11/17/278192.html>
- evidence: **A/B，同时代公开 Web 文章；能证明 URL 被当时作者识别和传播**

2007 的 Google Groups / 51CTO 转贴继续保留相同 URL：

- <https://groups.google.com/g/zhong1985624/c/RFyCqZ1uUCM>
- <https://blog.51cto.com/zjhwin/43402>

因此可以谨慎写：

> **到 2005 年，`ems.com.cn/ems/index.jsp` 已经作为公众 Web 查件入口被普通中文网站作者公开传播。**

不能写：

- 2005 全国 EMS 用户都会查；
- 该 URL 从哪年开始上线；
- 2005 DOM/charset/form action 已被本轮验证；
- 所有邮件号都能查到完整节点。

---

## 5. 2006 同时代论坛：endpoint-known / result-confidence gap

2006-06-07 的华人论坛讨论中，一名用户问 EMS 是否有 tracking number；另一名用户贴出上述 URL，但仍表示并不确定是否真的能 track 到。

来源：

- <https://huaren.us/showtopic.html?topicid=210057>
- evidence: **A，同时代论坛即时讨论；不是普及率样本**

新增：

### **endpoint-known / result-confidence gap**

```text
user knows query URL
!= user understands which identifiers are accepted
!= query returns a record
!= returned record is timely enough to trust
```

这类材料比后来的产品史更能保存旧网用户真实的不确定性。

---

## 6. 2007 假 EMS 网站：tracking form 也是 trust artifact

2007-02-08 的同期报道对比假邮政速递网站与真实 EMS 网站。记者明确写到，假站复制了“邮件查询”等栏目；真实站点为 `ems.com.cn`，并通过 logo、新闻更新时间、客服信息、版权主体等差异进行鉴别。

来源：

- 搜狐新闻，2007-02-08：<https://news.sohu.com/20070208/n248113551.shtml>
- evidence: **B，同期独立媒体观察**

这说明旧 tracking page 研究不能只问“是否有一个输入框”。还要问：

```text
hostname
TLS/HTTP context if any
brand marks
page freshness
form action
whether query leaves the host
whether page asks for payment/account credentials
```

新增：

### **tracking-interface trust gap / 查件界面信任缺口**

> **页面长得像 EMS 查询 ≠ 查询请求真的进入 EMS tracking backend。**

旧网回放里尤其不能只凭 logo 或复制的表单就确认历史主体。

---

## 7. 2007 “雀雀•魅”：妥投终态与现实占有分离

2007-08-22 红网/新浪报道保存了一次非常有价值的同时代用户经验：

- 北京寄往长沙的 EMS 急件；
- 收件人主动上 EMS 网站查询；
- 页面显示抵达长沙处理中心和安排投递的具体时间；
- 用户又通过热线核验；
- 实际迟迟没有取得；
- 后续网页已经显示“妥投”，物件却进入同楼另一单位的收发室。

来源：

- <https://news.sina.com.cn/o/2007-08-22/215712431390s.shtml>
- evidence: **B，同期媒体保存用户投诉/电话采访；具体个案不可代表总体服务水平**

这条材料足以固定：

### **status–possession gap / 状态—占有缺口**

```text
carrier marks delivered / 妥投
→ physical item may be at reception/mailroom/proxy
→ named recipient may still not know or possess it
```

因此 archive 中若能找到一个显示“妥投”的历史 result page，最多证明：

> 某 backend 在 capture 时给这个 identifier 返回了某终态表示。

不能直接证明：

- 购买者本人签字；
- 指定收件人实际获得；
- 交付地点符合原约定；
- 该状态在现实交付之后才写入；
- 没有后续纠纷或改写。

---

## 8. scan-state 不是 location truth

Tracking 页面常让现代读者产生一种“包裹被连续定位”的错觉。历史上大多数 ordinary parcel tracking 更接近离散事件序列：

```text
scan at node A
[unknown physical interval]
scan at node B
[unknown interval]
out-for-delivery event
POD event
```

本稿新增：

### **scan desert / 扫描荒漠**

两个可见事件之间没有新 scan：

- 不证明包裹静止；
- 不证明包裹丢失；
- 不证明页面没有延迟；
- 也不证明它一定继续正常移动。

### **event/display/capture four-clock problem**

至少记录四个时钟：

```yaml
physical_event_time:
backend_ingest_time:
user_visible_display_time:
archive_capture_time:
```

若还有 notification，则增加：

```yaml
notification_send_time:
notification_receive_time:
user_read_time:
```

同一个“14:42 派送”的字符串，不应与 14:42 页面已可见、用户已看到、archive 当时已抓到混为一谈。

---

## 9. 2010 当当父稿证据：order tracking 与 carrier tracking 也不能合并

父稿已经依据 2010 当当 SEC F-1 记录：客户账号可 track order and shipment status、查看 estimated delivery date、修改部分尚未完成的 delivery/payment 状态。

原始来源：

- SEC F-1/A：<https://www.sec.gov/Archives/edgar/data/1499744/000095012310111515/h04369a4fv1za.htm>

新增边界：

> **merchant order status ≠ carrier event stream。**

电商平台可能显示：

```text
已确认
已出库
已交承运商
运输中
```

承运商可能同时有另一套：

```text
运单已生成
已揽收
离开处理中心
到达处理中心
派送
妥投
```

历史页面若只保存一侧，不能补出另一侧缺失状态。

---

## 10. 2010—2011 快递100：新增 aggregator-origin gap

2011-04-20 的同期行业报道观察到“快递100”已经能在一个互联网应用里查询多家快递/物流公司订单信息，并被嵌入百度开放应用场景。报道引用产品方口径称上线约八个月累计近 4,000 万次查询、约 600 家合作伙伴；规模数据应保留来源性质，不能当独立人口统计。

来源：

- DOIT，2011-04-20：<https://www.doit.com.cn/p/73407.html>
- evidence: **B，同期行业媒体；功能观察较强，规模主要为企业口径**

这里新增三个 archaeology gap。

### 10.1 **aggregator-origin gap / 聚合器来源缺口**

```text
快递100 result
!= same-instant carrier official result proven
```

必须问：

- 数据来自官方 API、页面抓取、合作接口还是缓存？
- 更新时间差多少？
- carrier 原始状态字符串是什么？
- 聚合器是否做 normalized mapping？

### 10.2 **cross-carrier semantic normalization gap / 跨承运商语义归一缺口**

不同公司历史上可能把类似现实状态命名为：

- 已收件 / 已揽收 / 收件扫描；
- 到达网点 / 到达处理中心；
- 派件中 / 正在投递；
- 签收 / 妥投 / 正常签收。

聚合器若统一成一套现代枚举，研究者必须保留 raw carrier string，否则会把不同历史制度强行压平。

### 10.3 **proxy-state drift / 代理状态漂移**

一个 2011 嵌入百度/Q+ 的查询组件，可能只是一层 UI；后端又可能来自快递100，快递100再来自 carrier。

Archive 保存外层 component，不代表内层数据源被同日保存。

---

## 11. tracking page 的 archive 特别难点

### 11.1 form shell survives / private query result missing

最常见保存形态可能是：

```text
logo + 单号输入框 + 查询按钮 + 帮助文字 survives
```

而真正的 result：

- 通过 GET/POST 参数动态生成；
- 依赖 cookie/session；
- 由 JavaScript/AJAX 二次请求；
- 后端只保留有限历史；
- archive 不会主动提交私人 tracking number。

因此：

> **tracking form capture ≠ tracking transaction capture。**

这不是考古失败，而是动态/private state 的正常保存边界。

### 11.2 HTTP 200 != valid tracking result

同一 URL 可能返回：

- 初始空表单；
- “号码不存在”；
- 验证码错误；
- service unavailable；
- 被 archive rewrite 的脚本错误；
- 真正 event list。

必须记录页面语义，而不是只记 HTTP status。

### 11.3 current-backend rehydration != historical replay

如果旧 URL 今天仍然活着、或 Wayback 的 shell 仍会请求今天的 API，页面显示的状态可能来自当前 backend。

必须固定：

> **historical shell + live backend ≠ historical tracking result。**

### 11.4 tracking-number reuse / privacy hazard

不要为了复原而拿公开旧网页中的普通人真实运单号去当前系统反复查询。

原因：

- 运单号可能被重新分配；
- 当前结果可能指向无关的新用户；
- tracking 结果可能泄露地点、时间、地址片段和收件关系；
- 对本研究来说，真实私人单号通常不是必要条件。

应优先寻找：

- 官方 demo；
- 帮助页截图；
- 媒体操作观察；
- 已脱敏样例；
- 文档中的字段/状态枚举。

---

## 12. terminal-state hindsight bias：archive 特别容易只留下“结局”

Tracking 是一个不断变化的页面：

```text
今天：已揽收
明天：运输中
后天：派送中
最后：已签收
```

如果 archive 只在最后抓了一次，它会让后来的研究者产生错觉：

> 这个包裹“历史上就是已签收”。

实际上前几天用户面对的可能是长时间无更新、错误节点、反复查询与客服沟通。

新增：

### **terminal-state hindsight bias / 终态后见偏差**

最终状态最稳定、最容易幸存，却恰好最容易抹去等待过程中的不确定性。

因此完整 case 最好寻找 ≥2 个时点；只有终态 capture 时，必须显式说：

```yaml
terminal_state_observed: true
prior_state_sequence_observed: false
historical_uncertainty_reconstructed_from_this_capture: prohibited
```

---

## 13. “签收”以后还存在 endpoint semantics

2018—2019 虽已超出本仓主研究窗口的晚端，但它们反过来解释 2005—2015 为什么不能把 `signed` 当“本人获得”。同期材料大量出现：

- 快递柜；
- 门卫/前台；
- 合作代收点；
- 本人未接电话却显示签收。

父稿已经研究 pickup endpoint，本稿只把对历史 tracking 的结论固定为：

```text
POD endpoint may be:
  named recipient
  household member
  colleague
  office reception
  guard
  pickup station
  parcel locker
  other proxy
```

若历史状态字符串只有“妥投/签收”，endpoint 仍是 unknown，除非另有 evidence。

---

## 14. 旧 Web 证据等级与可复原层级

建议 parcel tracking 使用 T0–T8：

| Level | 保存到什么 |
|---|---|
| T0 | 只有第三方提到某站能查询 |
| T1 | historical hostname / query URL 可定位 |
| T2 | tracking form/help page capture 已验证 |
| T3 | input fields / form action / charset / client dependencies 可确认 |
| T4 | 脱敏 historical result page 或官方样例可确认 |
| T5 | 多状态 event labels / timestamp semantics 可确认 |
| T6 | merchant/carrier/aggregator provenance 链可确认 |
| T7 | ≥2 historical timepoints，能观察 UI/state change |
| T8 | 在不暴露普通人私人运单数据的前提下，事务、浏览环境、数据来源与保存缺口都可复核 |

T8 **不要求**重新公开真实普通人的完整物流轨迹。

---

## 15. 本轮 historical replay 尝试与负结果

本轮已经通过 2005 同期博客和 2007 多个同时代页面确认历史查询 URL：

`http://www.ems.com.cn/ems/index.jsp`

随后尝试直接构造 Internet Archive 对该 URL 的 2007 historical replay。当前研究访问链拒绝打开未经已有搜索结果产生的构造 Wayback URL，因此没有取得一份能够逐项核验以下字段的 memento：

```yaml
archive_source: Internet Archive
original_url: http://www.ems.com.cn/ems/index.jsp
capture_url: NOT VERIFIED
capture_datetime: NOT VERIFIED
http_status: NOT VERIFIED
charset: NOT VERIFIED
form_action: NOT VERIFIED
javascript_dependencies: NOT VERIFIED
result_semantics: NOT VERIFIED
```

所以本轮结论只能写：

> **M1 verified EMS historical tracking capture: NOT ACHIEVED IN THIS SLICE.**

绝不能写：

> “Wayback 没保存 EMS tracking。”

`not verified in this run != absent from archive`。

这与 `docs/METHOD.md` 的负证据规则一致。

---

## 16. 已证实 / 高概率 / 不知道

### 已证实

- 到 2005 年，`ems.com.cn/ems/index.jsp` 已被同时代中文 Web 作者公开传播为 EMS 邮件号查询入口；
- 2006 同时代论坛用户知道该入口，但有人仍不确定 tracking 实际可用性；
- 2007 同期媒体确认真实 EMS 网站拥有“邮件查询”栏目，并记录假站复制类似界面；
- 2007 有用户实际通过 EMS Web 查看节点状态，并出现“妥投”与本人实际取得分离的案例；
- 2010 当当向 SEC 描述的 Web 账号系统支持 order/shipment status tracking；
- 2011 快递100 已作为跨承运商查询应用被同期媒体实际观察。

### 高概率但本轮未完整复原

- 2005—2007 EMS Web result 很可能由动态 backend 返回，不是纯静态 HTML；
- 部分 tracking 页面依赖用户输入单号、session、脚本或后台保留期，因此公共 archive 更容易保存 shell 而不是私人 result；
- 2011 聚合查询存在 carrier→aggregator→outer platform 多层 provenance，但具体每一家承运商的接口方式可能不同。

### 不知道

- 1994 跟踪查询网的协议、终端、访问权限与 public-Web 关系；
- `ems/index.jsp` 最早上线时间；
- 2005 具体 charset、DOM、form method、验证码、result URL；
- 2005—2010 EMS 普通用户 query frequency；
- 早期民营快递各家的第一批 Web tracking 页面和 backend 语义；
- 快递100 2010—2011 每一家 carrier 的 raw mapping 和缓存/刷新策略。

---

## 17. 后见之明风险

- 不把今天 App 里的地图式物流轨迹倒投到 2005 的离散扫描事件；
- 不把“1994 网上查询”自动解释成 public Internet；
- 不从 query URL exists 跳到 popular；
- 不把秒级 event timestamp 当连续定位精度；
- 不把最终“妥投”倒写成历史过程一直顺利；
- 不把现代聚合器统一状态枚举用于解释历史 carrier 原始语义；
- 不拿当前 API 对旧号码返回的结果冒充历史记录；
- 不为了完整而重新暴露普通人的真实运单轨迹。

---

## 18. 对 `how-people-lived` 的交叉结论

旧 Web tracking 不是只有一个“方便查物流”的功能点。它把一件现实物体变成了一串可公开查询/私下查询的中间状态，从而改变普通人的等待：

```text
纯等待
→ 打电话/窗口查询
→ 主动 Web 查询
→ 购物平台内置物流
→ SMS/App 主动通知
→ 末端位置/取件码/交付方式也成为状态
```

但旧网考古同时证明：

> **Web 最擅长保存的是状态文字，最不擅长保存的是那段文字与现实物体之间真正发生了什么。**

一个 `已签收` 字符串可以幸存很多年；谁搬了最后五十米、谁去柜子取、谁白等了一下午、谁打了三次客服电话，往往更容易消失。

这正是把旧 Web 技术状态写回普通生活史时必须保留的历史可见性偏差。