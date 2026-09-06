# Consumer complaint Web submission / routing / remedy state gaps, 2004–2015

## Scope

本文严格留在本仓约 1995–2015 中文 Web 的研究边界内。它不是中国消费者权益保护史，也不把 1980s 消费者协会、1999 年 12315 电话网络、2017 年以后全国 12315 互联网平台、2018 年后的黑猫投诉或 2020s ODR 体系扩进本仓主体。

更长的 ordinary-life companion note 见：

- `tmzncty/how-people-lived/topics/consumer-redress-complaint-executability-and-failure-reversibility-china-1984-2026.zh-CN.md`

这里问一个更窄的 old-Web 问题：

> 当 2004–2015 中文 Web 上出现“我要投诉”、公开投诉记录、投诉编号、处理状态和企业回复时，一个历史页面究竟能证明到哪一步？“页面上有投诉”与“消费者已经获得退款/维修/补偿”之间，隔着多少不可见状态？

沿用 `docs/METHOD.md`：

`platform ≠ site/host ≠ account ≠ page/URL ≠ capture ≠ claim`

本题再增加：

`complaint expression ≠ submission ≠ server acceptance ≠ publication ≠ routing ≠ response ≠ remedy ≠ consumer satisfaction`。

---

## 1. 最小状态机：投诉页不是一篇普通文章，而是一笔持续变化的事务

一个 online complaint 至少可能经过：

```text
consumer experiences problem
→ identifies target merchant/service
→ opens complaint entry page
→ account/identity/contact fields
→ category + narrative + requested remedy
→ evidence attachment / external evidence
→ submit attempt
→ server acceptance
→ complaint ID assigned
→ moderation / validity check
→ public OR private state
→ routed to enterprise / authority / mediator
→ enterprise response
→ consumer follow-up
→ negotiation / mediation
→ refund / repair / replacement / rejection / no response
→ status closed / stale / deleted
→ page survives OR disappears
```

从 archive 角度，每一步都可能断裂。

因此历史研究至少要分别记录：

- `entry_page_exists`
- `submission_endpoint_known`
- `submission_success_evidence`
- `complaint_id_known`
- `publication_state`
- `routing_state`
- `merchant_response_state`
- `consumer_followup_state`
- `remedy_state`
- `closure_state`
- `capture_state`

不知道时写 `unknown`。

---

## 2. 2006：`www.caqp.org.cn` 的“我要投诉”证明 Web 入口存在，但不能替后台 transaction 作证

2006-03-03，《法制晚报》经新浪保存的同期报道写明，中国质量万里行促进会在 3·15 期间接受家装消费举报，消费者可以拨打电话，也可以登录：

- `www.caqp.org.cn`
- 点击“我要投诉”

来源，B 级同期媒体：
<https://finance.sina.com.cn/xiaofei/consume/20060303/16012389834.shtml>

2008 年《北京晚报》仍记录该 host 作为质量举报投诉网站：
<https://news.sina.com.cn/c/2008-10-26/181014632361s.shtml>

这两个 evidence family 至少支持一个窄结论：

> 2006–2008 年间，公开材料把 `www.caqp.org.cn` 描述为可通过 Web 进入投诉/举报流程的历史 host。

它们**不能**直接证明：

- 2006 的“我要投诉”按钮具体 URL；
- form 是 GET 还是 POST；
- 是否必须注册；
- 是否需要真实姓名、电话、身份证；
- 是否能上传图片；
- submit 后有没有 receipt / complaint ID；
- 数据是否进入内部工单系统；
- 是否向企业转发；
- 每个提交是否都被工作人员看到；
- 历史服务器是否在夜间同样接受 transaction。

这就是 **public-entry / private-workflow gap**。

---

## 3. 2008：315ts 留下了罕见的“普通用户说自己已提交，并给出具体投诉 URL”

2008-05-24，博客园用户 dudu 在追踪一起快递运输损坏争议时记录自己的行动：

1. 在“315消费电子投诉网”提交投诉；
2. 声称投诉已经被受理；
3. 给出一个 `http://www.315ts.net/ts/viewtousu.asp?id=<numeric-id>` 格式的具体投诉页 locator；
4. 同时继续拨打快递分公司电话和企业投诉电话。

来源：同时代个人 Web 日记，A/B 之间的操作证据：
<https://www.cnblogs.com/dudu/archive/2008/05/24/1206329.html>

这条证据很有价值，因为它让我们观察到一个具体历史 URL pattern：

```text
host: www.315ts.net
path: /ts/viewtousu.asp
query: id=<numeric complaint id>
```

原博客保留了当年的完整 numeric locator；本仓只保存 URL pattern 和 source URL，不再次扩散普通投诉人的具体 complaint ID。它至少说明，当时用户能够把某个投诉记录当作**可链接的 Web 对象**在别处引用。

但这里必须保持 METHOD 门槛：

- 这是同时代外部页面给出的 **historical locator**；
- 本轮没有实际打开并验证该 URL 的 2008 Wayback/WARC memento；
- 因此不能声称我们已经看到 2008 的投诉页面原 DOM；
- 也不能从 `viewtousu.asp?id=...` 推断后台数据库字段、账户模型或工作流。

### 3.1 “被受理”这个词本身也要拆

用户写“投诉已经被受理”，可能指：

- 页面成功生成；
- 网站初审通过并公开；
- 网站工作人员确认收到；
- 已经转给企业；
- 已进入正式调解。

除非原站帮助页或 transaction state 能进一步证明，old-Web note 不能把这些含义自动合并。

因此：

`public complaint URL exists ≠ enterprise received complaint`。

---

## 4. 2007–2010：公开投诉页开始形成可搜索的“问题地图”，但 counts 不能直接当现实结果

2008 年中国电子商会公布的材料称，315消费电子投诉网 `www.315ts.net` 在 2007 年受理消费电子产品投诉 55,817 宗；2009 年上半年，该站又公开网络游戏投诉统计。

来源，B / operator-reported：

- 新华社经搜狐，2008-03-14：<https://business.sohu.com/20080314/n255716304.shtml>
- 2009 年上半年网游投诉统计，ZOL 转载：<https://game.zol.com.cn/142/1427608.html>

这些数据能证明：

- 该站自我定义为一个按投诉记录聚合行业问题的 Web 平台；
- media / industry actors 当时确实引用了该站数据；
- complaint pages 不只是给单个消费者看，也开始成为行业统计的原料。

但必须保留多个 denominator gap：

`complaint count ≠ unique consumers`

`complaint count ≠ valid complaints`

`complaint count ≠ transaction count`

`complaint count ≠ defect rate`

`complaint count ≠ unresolved cases`

一个大型品牌交易量更多、网民更多、产品更适合在线讨论，都可能导致投诉页更多，而不代表单位销量质量一定更差。

### 4.1 public complaint as cross-user coordination

同期论坛/媒体材料还能看到另一种用途：消费者会把 315ts 投诉 URL 转贴到博客、论坛、QQ群讨论中，用来告诉其他人“同型号/同商家也有人遇到类似问题”。

例如 2008 年博客园的 locator，以及同时期相机用户讨论里对 315ts complaint URL 的转引，都说明：

`individual complaint`

可以成为：

`searchable precedent / coordination artifact`。

但跨帖引用不能自动证明所有案例属于同一缺陷，也不能把转贴次数当作独立受害者数量。

---

## 5. 2008：数字消费让“证据会消失”第一次成为投诉技术的一部分

北京 2008 年网购投诉增长时，12315/消协公开提醒消费者保存：

- 电子交易单据；
- 商家以电子邮件发送的确认；
- 用户名和密码等；
- 消费记录；

并明确提醒网页更新后原记录可能无法查询。

来源：《北京日报》经搜狐，B：
<https://news.sohu.com/20080204/n255065843.shtml>

对 old-Web 考古来说，这是一份很关键的同期方法材料。它说明历史消费者当时自己已经面对：

**transaction-state ephemerality / 交易状态易逝性**。

今天 archive 能留下某个 product page，也不能自动重建消费者当时真正用于维权的 evidence bundle，因为后者可能包括：

```text
account-only order page
+ e-mail
+ payment confirmation
+ merchant chat
+ delivery record
+ screenshot
+ complaint receipt
```

这些资源大多不公开、需要认证、受隐私限制，而且 archive 本来就不应保存完整私人交易。

因此出现 **public-product-shell / private-evidence-bundle asymmetry**。

---

## 6. 2009：退款到“站内余额/积分”说明 remedy state 不能只写 solved / unsolved

2009 年北京工商/消协公布的网购投诉里：

- 一名消费者的订单被网站取消，经营者只同意把款项退到站内账户，不愿退现金；
- 另一名消费者退回有质量问题的音箱后，网站只愿给积分；
- 当时 12315 已受理，案件仍在调解。

来源：北京青年报经搜狐，B：
<https://news.sohu.com/20090403/n263187760.shtml>

如果未来真的取得对应 old-Web 记录，不能把“商家已处理”归成一个二值字段。至少应细分：

```text
no response
explanation only
repair
replacement
platform credit
coupon / points
partial refund
cash refund
full refund + costs
rejected
unknown
```

因此：

`response state ≠ remedy type ≠ recovered value`。

平台自己的“已处理”标签若没有消费者 follow-up，不应直接翻译成“维权成功”。

---

## 7. 2011：315ts 的运营争议使“投诉是否仍公开”本身变成不可信状态

2011-03-22，民政部对中国电子商会作出行政处罚。公开调查结果称，该会主办、由企业具体运营的“315消费电子投诉网”在运营中利用投诉信息向企业强制服务、强制收费等，被责令整改。

来源：民政部消息经中新网，A/B：
<https://www.chinanews.com.cn/gn/2011/03-22/2923011.shtml>

同时期媒体进一步报道，该网站被指可因企业付费而隐藏或缩短投诉公开时间。

来源：2011-01-06 Shanghai Daily，B：
<https://archive.shine.cn/nation/Site-made-complaints-disappear/shdaily.shtml>

这个案例对 old-Web 保存方法非常重要，因为它产生了一个比普通删帖更复杂的偏差：

## operator-mediated visibility bias / 运营者介入的可见性偏差

某条投诉没有出现在后来页面或 archive 中，可能因为：

- 从未提交；
- 提交失败；
- 未通过审核；
- 用户删除；
- 已和解后正常关闭；
- 运营方下架；
- 商业关系影响展示；
- 站点迁移/数据库损坏；
- archive 没抓到。

因此：

`not visible in surviving corpus ≠ complaint never existed`。

反过来，公开投诉仍在也不等于内容已经经过事实核验。

这个案例还说明：**consumer-protection intermediary itself can be a historical actor with incentives**。研究者不能默认“投诉网站”天然是中立数据库。

---

## 8. 2010–2015：企业自有客服、平台投诉与第三方投诉并存，必须先确定 transaction family

到 2010s 初，一个网购消费者可能至少有几条不同 Web 路线：

### A. Merchant-owned support

```text
merchant site
→ customer service / after-sales form
→ internal ticket
→ merchant-only record
```

### B. Marketplace-owned dispute

```text
order page
→ refund/dispute
→ platform evidence
→ seller response
→ platform rule / escrow
→ refund or rejection
```

### C. Third-party public complaint

```text
complaint portal
→ public complaint record
→ operator moderation
→ enterprise contact / public pressure
→ response / status
```

### D. Administrative/association route

```text
12315 / consumer association
→ accepted complaint
→ jurisdiction routing
→ mediation / administrative handling
```

同一消费者可能同时走两三条路线。

因此 archive 看到一条第三方投诉页时，不能推断：

- 用户没有同时联系卖家客服；
- 平台内部没有退款工单；
- 12315 没有另一个 case；
- 所有记录的“处理完成时间”一致。

这叫 **multi-channel case identity gap / 多渠道案件同一性缺口**。

不同系统没有稳定公开 case ID 可以互相 join 时，不应只凭商品、日期和姓氏把它们强行合并成同一个现实纠纷。

---

## 9. 本题需要固定的 state gaps

### 9.1 entry / submission gap

`“我要投诉”按钮存在 ≠ form submit 成功`。

需要历史 form action、response、receipt 或用户同期成功证据。

### 9.2 submit / acceptance gap

server 收到数据不等于网站认为投诉有效。

可能还有验证码、登录、人工审核、重复投诉检测、必填字段。

### 9.3 acceptance / publication gap

投诉可私下进入工单，却不一定公开；反之，公开页面也不一定意味着正式行政受理。

### 9.4 publication / routing gap

`public page ≠ enterprise notified`。

需要转办记录、企业回复、用户跟进或官方 workflow 证据。

### 9.5 routing / response gap

企业收到不等于回复。

### 9.6 response / remedy gap

“已回复”“已处理”不能自动翻译成退款、维修或补偿。

### 9.7 remedy / satisfaction gap

一个解释、积分或部分退款可能满足平台的 closure rule，却不一定满足消费者。

### 9.8 status-staleness gap

公开投诉页的“处理中”“已解决”是时态字段。archive 抓到的是某个时点状态，不是永恒结果。

### 9.9 evidence-attachment gap

截图、发票、照片、聊天附件可能由单独 host、登录态、Flash/JS uploader 或私有对象存储承担；主 HTML 幸存不等于证据包幸存。

### 9.10 complaint-count / affected-person gap

一个人可以多次投诉；多人也可以围绕同一产品问题提交。投诉数不能直接当受影响人数。

---

## 10. 技术/页面问题：即使取得 capture，也不能立刻宣称“完整复原了投诉流程”

### 10.1 动态 ASP URL

`315ts.net/ts/viewtousu.asp?id=<id>` 明显表现为动态 server-side 页面 URL pattern。

从这个 pattern **可以**说：

- 同时代用户把 complaint ID 放在 query parameter URL 中引用。

不能仅凭 URL 推断：

- 后端一定是某种特定数据库；
- ID 单调递增且无缺口；
- ID 等于有效投诉序号；
- 页面无需登录；
- 所有投诉使用同一模板；
- 站点没有缓存/镜像。

### 10.2 charset unknown

本轮没有取得原历史 HTTP headers 或 HTML meta，因此 `caqp.org.cn`、`315ts.net` 具体投诉页的 GB2312/GBK/UTF-8 状态继续是 `unknown`。

不能从今天搜索引擎正常显示中文，倒推历史 charset。

### 10.3 browser assumption unknown

本轮没有验证：

- IE-only JS；
- ActiveX；
- iframe；
- table layout；
- attachment uploader；
- old captcha；
- cookie requirement。

现代浏览器能打开外部转述页面，不代表历史 complaint transaction 可在现代浏览器复现。

### 10.4 archived GET page ≠ archived POST workflow

即使 Wayback 将来命中某个 `viewtousu.asp?id=...`，它通常也更容易证明：

`a public GET representation was captured`

而不是：

`the historical POST submission + moderation + routing transaction was archived`。

这条边界必须写死。

---

## 11. 历史 locator 清单（本轮只登记，不冒充 capture）

### 11.1 中国质量万里行

- host：`www.caqp.org.cn`
- 2006 同期功能描述：“我要投诉”
- 2008 同期材料继续列为投诉举报网站

证据：

- <https://finance.sina.com.cn/xiaofei/consume/20060303/16012389834.shtml>
- <https://news.sina.com.cn/c/2008-10-26/181014632361s.shtml>

### 11.2 315消费电子投诉网

- host：`www.315ts.net`
- historical complaint URL pattern：`/ts/viewtousu.asp?id=<numeric id>`
- 同时代外部博客保留过一个具体 numeric locator；本仓不重复该 ID，只保存 pattern 与 source URL。

证据：

- 2008 博客园同期外部链接：<https://www.cnblogs.com/dudu/archive/2008/05/24/1206329.html>
- 2008 站点统计经新华社/搜狐：<https://business.sohu.com/20080314/n255716304.shtml>
- 2011 行政处罚：<https://www.chinanews.com.cn/gn/2011/03-22/2923011.shtml>

### 11.3 注意：名字相近不等于同站

历史上存在多个以“315”“投诉网”“消费投诉”命名的不同主体。

因此：

`315消费电子投诉网 ≠ 所有“315投诉网” ≠ 12315 ≠ 中国消费者协会`。

做 host/主体判断时必须保存 organization、operator、domain、year，不能靠名字合并。

---

## 12. Archive / M1 本轮负结果

本轮已经得到多个具体 historical locator，但**没有实际打开并验证一份满足本仓 M1 门槛的 2004–2010 中文消费者投诉 transaction memento / WARC**。

因此以下内容继续标为 `unknown`：

- `www.caqp.org.cn` 2006 “我要投诉”原页面 URL；
- 原 DOM / CSS / JS；
- HTTP Content-Type / charset；
- form method / action；
- captcha；
- login / cookie / session；
- attachment upload；
- server-side validation；
- complaint ID assignment rule；
- moderation state；
- enterprise routing event；
- consumer follow-up；
- remedy field；
- page deletion / closure rule。

搜索结果、同期外链或今天仍可读的二手转载都只是 locator/evidence，不是已验证 memento。

本轮尝试通过 Web 搜索定位 Wayback 结果，没有取得可实际检查的对应历史 capture；这应记录为**本轮未验证成功**，而不是写成“Wayback 没有保存”。

---

## 13. 保存偏差

### 13.1 public-complaint-shell / private-settlement asymmetry

最容易保存：

- 标题；
- 投诉正文；
- 产品/商家名；
- complaint ID；
- 页面状态；
- 公开企业回复。

最难、也最不应被 archive 完整公开保存：

- 手机号；
- 地址；
- 身份证；
- 订单号；
- 支付账户；
- 私聊；
- 企业内部工单；
- 银行退款；
- 电话调解；
- 最后的私人和解条件。

因此 archive 很可能留下“争议的壳”，却缺失“真正解决争议的最后一公里”。

### 13.2 unresolved-story visibility bias

长期公开的投诉可能比快速私下解决的争议更容易被抓到，因此 surviving Web 会系统性高估“冲突一直没有解决”的可见度。

### 13.3 success-story bias

相反，平台宣传页又会优先展示成功维权个案，低估石沉大海、用户放弃和不满意 closure。

两种偏差可以同时存在。

### 13.4 operator-removal bias

315ts 2011 事件说明，投诉展示状态可能被平台经营机制影响。历史缺失不能只归因于 robots 或 archive 技术问题。

### 13.5 evidence-decay bias

商品页、邮件、聊天附件、图片、发票扫描、Flash uploader 等比纯文本投诉正文更容易丢失，导致后来研究者能看到“消费者说有证据”，却看不到当年的证据本体。

### 13.6 seasonal 3·15 bias

每年 3 月媒体和平台对投诉渠道、典型案件的报道显著增加。用公开新闻做样本会高估 3 月材料、低估全年普通失败状态。

---

## 14. 隐私边界

历史投诉页常包含比普通论坛帖子更敏感的信息，因为投诉需要证明交易和身份。

本仓执行研究必要最小化：

- 不批量重新公开历史手机号、住址、身份证、订单号；
- 不为了“验证真实消费者”去反向识别普通个人；
- 技术研究优先记录 URL pattern、字段类别、状态机；
- 普通投诉人的姓名若非理解 claim 所必需，不进入数据集；
- attachment 即使 archive 可取，也先检查隐私与版权再决定是否引用。

本轮因此只保留 2008 外部博客足以证明的 host/path/query pattern，不把普通投诉人的具体 complaint ID 复制进仓库，也不据此重新拼接其私人消费史。

---

## 15. 与 ordinary-life 研究的交叉结论

old-Web 侧能提供的最重要贡献不是“网站长什么样”，而是指出数字投诉改变了哪些状态：

```text
spoken complaint
→ durable complaint object
→ URL / ID
→ searchable / linkable
→ routable
→ countable
→ publishable
→ potentially reputation-bearing
```

但现实生活真正关心的是更后的状态：

```text
Did the person get the money back?
Did the item get repaired?
How many calls/screenshots/trips did it cost?
Did they give up because the amount was too small?
```

这些状态恰恰最不容易从公开 old Web 单独恢复。

因此本题给两仓之间建立一条明确边界：

> **中文旧网可以让投诉变得更可寻址、更可链接、更可累计；它并没有自动把“投诉可见”变成“失败可逆”。**

---

## 16. 下一步

1. 用 Internet Archive / Common Crawl 精确查询 `www.caqp.org.cn` 2005–2008 URL 历史，实际打开 memento 后再登记 capture metadata。
2. 查询 `www.315ts.net/ts/viewtousu.asp?id=...` 是否有可回放的 2007–2010 GET capture；若有，记录 original URL、memento datetime、charset、子资源和状态字段。
3. 搜索 315ts 同时期帮助页/注册页/“投诉流程”说明，优先找 A 级 capture 或平台原文转载，以确定 account、审核、企业回复和 closure 字段。
4. 不做大规模枚举 complaint ID；避免重新暴露普通消费者内容。
5. 若取得历史页面，优先比较两个时点：提交后早期“处理中” vs 后来“已回复/已解决”，验证 status temporal behavior。
6. 查 Common Crawl / ArchiveTeam 是否存在该站可合法复用的公开 WARC 线索；没有就保留 archive gap，不自建抓取器。
7. 将“投诉页面的页面状态”与 companion how-people-lived 中的“现实 remedy outcome”分栏，不为了补完整故事而把媒体结果倒灌进历史 DOM。

---

*Initial draft was AI-assisted. It follows `docs/METHOD.md`: historical locator is not treated as verified capture; operator-reported counts are labeled; ordinary complainant privacy is minimized; reconstruction is not presented as original.*
