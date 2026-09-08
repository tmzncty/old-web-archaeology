# AGRICULTURAL_INFORMATION_12316_SMS_WEB_MARKET_PRICE_AND_OFFLINE_SALE_STATE_GAPS_2003_2015

## 0. Scope

本 note 研究约 2003—2015 中文互联网中的一个事务型缺口：**农业信息网站、短信、热线、村级信息站与农产品供求平台究竟怎样进入普通农户的生产/销售事务，以及 Web 上的“信息可见”“供货发布”“购销对接”与现实成交之间存在哪些状态缺口。**

它不是全球农业信息史；1910s—1920s 美国 Market News、1980s 中国农业广播教育只作为必要前史边界。2018—2026 的直播、电商、AI 12316 只作 afterlife 检验，不扩张本仓约 1995—2015 中文旧网 scope。

本轮首先查重了仓库现有 recruitment、day-labor、domestic-service、classifieds、online-banking、remittance、mobile-number、photo-album 等专题；未发现独立的 agricultural market information / 12316 / rural information service state-gap note。

检索日期：2026-09-08。

---

## 1. Claim list before narrative

本轮只把以下窄 claim 写到较高确定度：

1. **A / high**：2006 年农业部同时代通知明确把“中国农业信息网”的 locator 写为 `www.agri.gov.cn`。
2. **A / high**：2006 年邢台农业价格信息体系实际把网站、短信、免费电话、广播、电视、报纸和基层信息员并列使用；Web 并不是唯一 farmer-facing channel。
3. **A/B / high**：2006 年以后“电话、电视、电脑三电合一”的设计明确针对不同农户可接受渠道，并建设乡镇/村级信息服务点。
4. **A / high**：农业部 2006 年开通 12316 电话专用号码、2009 年开通短信号码；2011 年官方文件仍要求各地继续建设 12316 综合信息服务平台。
5. **B / high**：2008 年“网上农产品购销对接”实际仍通过电话、email、传真、短信帮助买卖双方联系；名称中的“网上”不能直接解释为农户浏览器自助交易。
6. **A/B / high**：2008 年 CNNIC 农村调查显示行政村 Internet 可接入率已经很高，但农村居民 Internet 普及率只有 11.7%；`village connected != household/user adoption`。
7. **B / medium-high**：2006—2010 已有具体农户/经纪人通过农民信箱、地方农业网站、网吧等寻找买家和市场信息的同期人物材料。
8. **B / high**：2008 年柑橘短信传言造成销售冲击，证明 `faster information != verified information`，农业数字信息渠道也有负外部性。
9. **D / high as model, not historical fact**：历史 Web 研究必须把 `price/listing visible`、`buyer contact`、`order/intent`、`offline pickup`、`inspection`、`settlement` 分开。

---

## 2. Prehistory boundary: “数字农业信息”不能从 WWW 起算

中国普通农户在大众 Internet 以前并非处于“无信息”状态。现实渠道至少包括广播、电视、报刊、基层农技站、价格部门、供销/批发市场、电话、驻村干部、经纪人和种养大户。

1980 年成立的中央农业广播学校/后来的中央农业广播电视学校，是明确的远程农业教育前史；地方志还能看到县级分校按照广播播出时间组织农民和农村干部听课、再由地方辅导员辅导。

这些材料写入本 note 只为了设边界：

> **Internet 的到来不是从 0 到 1 地发明“远程农业信息”，而是把既有广播、电话、人际中介和市场报道重新接入数据库与双向网络。**

因此 1994 年前的科研网络/邮件与“普通农户实际使用网络获取市场信息”也必须拆开。前者存在，不能据此推出后者。

---

## 3. Historical locators

### 3.1 中国农业信息网

2006-06-15 的农业部通知（湖南省农业农村厅现存转载）明确要求相关人员关注：

```text
中国农业信息网：www.agri.gov.cn
```

Source:
https://agri.hunan.gov.cn/agri/xxgk/tzgg/200606/t20060619_3370430.html

Evidence grade: **A**（同时代农业部通知）  
Confidence: **high** for locator existence/name.

另有 2001 年 CCTV 财经页面把“中国农业信息网”列为：

```text
http://www.agri.gov.cn
http://www.agri.org.cn
```

Source:
https://finance.cctv.com/financial/jintudi/20010924/hangqing/9.htm

Evidence grade: **B**（同时代第三方 locator）  
Confidence: **medium-high**。

目前不能由这些 locator 推出：

- 2006 首页真实 HTML 结构；
- charset；
- 是否 frameset；
- 某价格/供求栏目具体 path；
- 是否要求 IE；
- form 是否真正可提交；
- session/cookie 语义；
- 普通农户是否直接访问。

### 3.2 其他 locator / product names worth pursuing

同时代来源明确出现但本轮未验证 historical capture 的对象：

- “邢台三农价格信息监测网”；
- “农价直通车”短信平台；
- “浙江农民信箱”；
- “新农村商网”；
- 12316 电话/短信农业服务；
- 地方“农民一点通”/村级信息服务点。

注意：产品名/平台名 ≠ 已知 host/path。

---

## 4. 2006 邢台：Web 在后台，但 farmer-facing interface 是一个 multimodal stack

2006 年国家发改委保存的邢台物价局同期工作材料，是本轮最强的一份事务合同。

Source:
https://www.ndrc.gov.cn/xwdt/gdzt/newcountry/xiagexiazai/200607/t20060705_75412.html

Evidence grade: **A**  
Confidence: **high** for described institutional design; **medium** for program self-reported impact.

材料把发布平台概括为“讯、网、栏、台、话、报”，其中包括：

- Web：三农价格信息监测网；
- SMS：“农价直通车”；
- 电话：8008037185 免费咨询；
- 电视；
- 广播；
- 报纸；
- 驻村干部、价格监测员、村干部、种养大户等人工信息节点。

因此不要把这个系统画成：

```text
farmer -> browser -> website -> decision
```

更接近现实的 topology 可能是：

```text
national / regional price sources
        |
        v
local price database / agricultural websites
        |
        +----> web page --------> PC user
        +----> SMS -------------> handset user
        +----> 800 phone --------> caller
        +----> radio / TV -------> household audience
        +----> newspaper --------> reader
        +----> village cadre / information agent -> non-user household
```

这意味着一个从未亲自打开网站的农户，仍然可能使用**由 Web/数据库参与生产的信息**。

新增状态边界：

```text
BACKEND_DIGITIZED
!= FARMER_WEB_USER
!= FARMER_INFORMATION_REACHED
!= FARMER_DECISION_CHANGED
```

---

## 5. “三电合一”不能复原成“农村网站普及”

2008 年《农民日报》同期材料回顾 2006 年农业部门推进“三电合一”，明确写的是电话、电视、电脑的组合，并强调通过用户能够接受、愿意接受的渠道提供服务；同时建设乡镇农业信息网站、村级信息服务点。

Source:
https://www.chinacoop.gov.cn/HTML/2008/12/15/19505.html

Evidence grade: **B**  
Confidence: **high** for contemporary program framing.

2008 年门头沟区政府的工作总结也把“三电合一”描述为电话语音、电脑网络和电视节目三种载体的有机结合。

Source:
https://www.bjmtg.gov.cn/11J000/gzzj53/200804/fc53fb84223f4b3d957a94f737cc9954.shtml

Evidence grade: **A**  
Confidence: **high**.

### Archaeological implication

如果未来找到一个 2007 年县农业局网站 capture，不能从“网站上有市场行情”推断：

1. 本村家庭有电脑；
2. 农户亲自打开该页；
3. 农户知道这个 URL；
4. 页面是主要渠道；
5. 信息没有同时通过电话/电视/短信再分发。

旧网历史的研究单位必须至少分：

- data source;
- Web publication;
- downstream re-publication;
- village service station;
- human intermediary;
- end household.

---

## 6. 12316：电话先成为入口，Web/短信/广播再层叠上去

2011 年农业部关于延长 12316 公益服务号码使用期限的通知明确记载：

- 2006 年申请开通 `12316` 专用电话号码；
- 2009 年申请开通短信息号码；
- 到 2011 年继续要求完善 12316 综合信息服务平台。

Source:
https://scs.moa.gov.cn/zcjd/201904/t20190418_6183307.htm

Evidence grade: **A**  
Confidence: **high**.

吉林后来的官方回顾称其 2006 年 5 月开通 12316、2008 年建 12582 短信平台，2014 年整合成覆盖语音、短信、广播电视、新媒体等的综合平台。

Source:
https://www.ndrc.gov.cn/fzggw/jgsj/gjss/sjdt/201709/t20170901_1154820_ext.html

Evidence grade: **B/C boundary**（官方 retrospective）  
Confidence: **medium-high** for milestones, lower for impact claims.

### Critical old-Web state gap

`12316 exists` 不等于 `12316 is a website`。

在很多时期，真正 farmer-facing 的入口首先是电话号码。Web 可能主要存在于：

- 坐席后台；
- 专家知识库；
- 行情数据库；
- 供求信息录入；
- 政策信息发布；
- later web portal / app。

因此旧网研究不能只寻找“12316 首页截图”，还应寻找：

- 坐席软件截图/手册；
- 专家登录界面；
- 短信网关说明；
- 话务工单状态；
- 供求信息如何从电话转成网页/短信；
- callback / three-way-call / dispatch 机制。

---

## 7. 2008 rural Internet denominator：村里能接入，不能替代 household/user evidence

CNNIC 2008—2009 农村调查给出一个非常必要的 denominator：

- 2008 年底农村网民约 8460 万；
- 农村居民 Internet 普及率约 11.7%，城镇约 35.2%；
- 89% 行政村能上网；
- 网吧仍是农村网民的重要接入点；
- 手机上网快速扩张。

Source:
https://www2.cnnic.cn/n4/2022/0401/c117-827.html

Evidence grade: **A**  
Confidence: **high**.

必须固定：

```text
VILLAGE_NETWORK_AVAILABLE
!= HOUSEHOLD_CONNECTION_AVAILABLE
!= PERSON_IS_NETIZEN
!= PERSON_USES_WEB_FOR_AGRICULTURE
```

2009 年张家口同期材料甚至给出更具体的地方对照：100 多万农户中 Internet 用户约 11 万，报道说农村经纪人和农业生产经营大户的上网率也仍然很低；当地因此把 Internet、短信、12316 电话、信息服务站和服务大厅继续捆在一起。

Source:
https://news.sohu.com/20090516/n263994454.shtml

Evidence grade: **B**  
Confidence: **medium-high**.

因此“农业网站在 2008 年已经存在”和“多数农户直接使用 Web”之间有明确证据断层。

---

## 8. First-person / user-adjacent evidence: platform use can change market radius

### 8.1 浙江农民信箱，2006

同期浙江日报材料记载，海宁姚季良在“浙江农民信箱”发布水果网套供货信息，杭州外贸公司看到后联系，之后签订供需合同并实体交货。

Source:
https://finance.sina.com.cn/roll/20060904/0329901513.shtml

Evidence grade: **B**  
Confidence: **medium-high**.

事务链应记录为：

```text
ACCOUNT/ACCESS
→ LISTING CREATED
→ LISTING VISIBLE TO UNKNOWN BUYER
→ BUYER CONTACT
→ OFFLINE NEGOTIATION
→ PAPER/OFFLINE CONTRACT
→ PRODUCTION
→ DELIVERY
→ SETTLEMENT (not technically reconstructed here)
```

不能缩成一个 `ONLINE_SALE_SUCCESS`。

### 8.2 余姚网吧/家庭 PC，2006

同期材料记录农户进网吧查俏销品种，也有少数较早购买家庭 PC、参加培训后自己查技术和行情的用户。

Source:
https://finance.sina.com.cn/roll/20060303/0545578023.shtml

Evidence grade: **B**  
Confidence: **medium**.

这里新增一个 access state：

```text
WEB_USE_LOCATION = {home_pc, internet_cafe, village_station, operator-mediated, unknown}
```

如果历史页面只留下账号内容，不能自动推断用户是在家里使用。

### 8.3 甘肃经纪人，2010

同期报道中，白银销售经纪人赵永明表示自己自 2003 年开始使用网络，通过地方农业信息网站联系外地/海外客商，并在 2010 年当下把网络销售视为长期方向。

Source:
https://news.sohu.com/20100111/n269506354.shtml

Evidence grade: **B + contemporaneous first-person**  
Confidence: **medium-high**.

这是一条 user experience 证据，但仍不能外推到“普通农民普遍如此”。

---

## 9. “网上购销”不是 browser-only transaction

商务部 2008 年第三届秋季农产品网上购销对接会的同期说明明确说，对接会通过：

- 电话；
- email；
- 传真；
- 手机短信；

帮助买卖双方互通信息、促成交易。

Source:
https://www.chinanews.com/cj/hzzx/news/2008/09-10/1377587.shtml

Evidence grade: **A/B**  
Confidence: **high**.

这条证据对旧 Web 术语尤其重要：

```text
ONLINE_MATCHMAKING
!= BROWSER_ONLY
!= SELF_SERVICE
!= PAYMENT_ONLINE
!= DELIVERY_ONLINE
```

可能存在的事务模式至少有：

```text
1. farmer self-posts listing on Web
2. local officer/agent posts on farmer's behalf
3. buyer discovers listing on Web then calls farmer
4. platform operator reads Web data and sends SMS/phone alert
5. email/fax is used between organizations while farmer remains offline
```

要重建具体案例，必须确定是哪一条，不能只看产品名称“网上购销”。

---

## 10. Negative case: faster network can spread market-destroying misinformation

2008 年柑橘大实蝇事件是本专题必须保留的反例。同年同期报道记载，关于“蛆橘”的短信快速扩散后，湖北等并无同类疫情地区也出现严重滞销和价格下降。

Sources:
- https://www.chinanews.com.cn/gn/news/2008/10-29/1428973.shtml
- https://news.sina.com.cn/c/2008-10-31/195916565325.shtml

Evidence grade: **B**  
Confidence: **high** for market disruption; **medium** for any exact causal attribution/magnitude.

新增状态：

```text
MESSAGE_CREATED
→ MESSAGE_FORWARDED
→ RECIPIENT_BELIEVES
→ CONSUMER_DEMAND_CHANGED
→ WHOLE-CATEGORY MARKET EFFECT
```

这条链说明：

```text
LOWER_INFORMATION_LATENCY
!= HIGHER_INFORMATION_QUALITY
```

所以旧网农业信息研究不能只统计“消息传播更快”作为正向现代化指标；**verification latency** 同样关键。

---

## 11. Core state machines

### 11.1 Market-information state machine

```text
SOURCE_DATA_CREATED
→ DATA_ENTERED
→ PUBLISHED_TO_WEB
→ RE-PUBLISHED_TO_SMS/PHONE/RADIO/TV/PRINT
→ FARMER_CHANNEL_AVAILABLE
→ FARMER_RECEIVES
→ FARMER_UNDERSTANDS
→ FARMER_TRUSTS
→ FARMER_DECISION_CHANGES
→ OFFLINE ACTION
```

状态缺口：

- `database row exists != public page exists`
- `page exists != farmer sees it`
- `SMS sent != delivered`
- `phone hotline exists != queue answered`
- `radio broadcast != household listening`
- `farmer receives != farmer trusts`
- `farmer trusts != action changes`

### 11.2 Supply-listing / sale state machine

```text
SELLER_IDENTIFIED
→ PRODUCT/QUANTITY/LOCATION KNOWN
→ LISTING ENTERED
→ LISTING PUBLISHED
→ BUYER DISCOVERS
→ CONTACT ESTABLISHED
→ PRICE/QUALITY NEGOTIATED
→ INTENT/ORDER
→ PACKING/GRADING
→ PICKUP/LOGISTICS
→ RECEIPT/INSPECTION
→ PAYMENT INITIATED
→ PAYMENT SETTLED
```

必须固定：

- `listing visible != buyer exists`
- `buyer contact != agreement`
- `agreement != pickup`
- `pickup != acceptance`
- `acceptance != settlement`
- `gross sale != farmer net income`

### 11.3 Intermediated-access state machine

```text
FARMER_NEED
→ HUMAN INTERMEDIARY (cadre / information agent / kiosk operator / hotline operator)
→ DIGITAL QUERY/ENTRY
→ DIGITAL RESULT
→ HUMAN EXPLANATION/RELAY
→ FARMER DECISION
```

这条线对历史解释非常关键，因为它允许：

```text
FARMER_IS_NOT_INTERNET_USER
AND
FARMER_LIFE_IS_AFFECTED_BY_INTERNET_BACKEND
```

---

## 12. Browser / technical archaeology questions

如果后续得到 `www.agri.gov.cn`、浙江农民信箱、新农村商网或县级农业信息网 capture，至少检查：

- HTTP status / redirect；
- Content-Type / charset（GB2312 / GBK / UTF-8?）；
- frameset / table layout；
- link scheme；
- form method / action；
- dynamic query parameters；
- login / cookie / session；
- 是否需要 IE-specific JS / ActiveX；
- 上传/发布 supply listing 是否有客户端控件；
- 手机短信是否由 Web UI 触发；
- public price page 与 authenticated operator console 是否不同 host；
- 图片、行情表格、JS 是否 separately captured；
- archive rewrite 是否破坏 form action / relative URL。

现代政府 CMS 保存一篇 2006 年通知，只证明**文本 today survives**，不能证明 2006 原页面形态 survives。

---

## 13. Archive status: M1 NOT ACHIEVED IN THIS SLICE

本轮确认了强 historical locator：

```text
http://www.agri.gov.cn
www.agri.gov.cn
```

也取得多个同时代官方/媒体事务描述，但没有实际取得并检查一份满足 `docs/METHOD.md` capture contract 的 2003—2010 historical replay。

本轮尝试构造 Wayback CDX 查询时，当前 Web 访问层拒绝直接打开未由搜索结果返回的 CDX URL；这属于**本轮工具访问限制**，不能写成：

- “Wayback 没有 capture”；
- “站点当年没有保存”；
- “网站无法复原”。

因此以下全部继续保持 **unknown**：

- exact capture datetime；
- original response headers；
- charset；
- historical DOM；
- JS；
- forms / endpoint；
- cookie/session；
- login state；
- IE/ActiveX requirement；
- listing publish workflow；
- price table resource dependencies。

符合 `docs/METHOD.md` 的写法只能是：

> **本轮未验证到合格 historical capture。**

---

## 14. Preservation / historical visibility bias

农业旧网有几种特别强的保存偏差：

1. **政策文本幸存，事务后台死亡**：今天还能看到“开通 12316 / 建设三电合一”，看不到坐席 queue、短信失败、村站代录过程。
2. **成功交易被新闻记录，失败交易消失**：媒体更爱写“网上卖出百万”，很少保留“买家没来、压价、拒收、欠款”。
3. **Web 用户比非 Web 用户更可见**：农民博客、网店、论坛能留下搜索痕迹；通过电话、广播、村干部获得同一条数字信息的人往往不留下页面。
4. **公开供货信息比私下成交更可见**：listing 能被 crawler 抓，电话议价、货车到村、现金结算通常没有 Web artifact。
5. **政府项目覆盖数字比 household practice 更易保存**：`覆盖 X 个村` 不等于 `X 个村每户都用`。

因此：

```text
HISTORIAN_VISIBLE_DIGITAL_FARMER
!= TYPICAL_FARMER
```

甚至有可能：**最被 Internet 改变、本人却最少留下 Web 痕迹的人，正是那些通过热线、短信和村级操作员使用数字后台的农户。**

---

## 15. Overseas comparator without expanding repo scope

### United States, 1915—1921 (pre-Web boundary only)

USDA National Agricultural Library 的历史说明显示 Federal Market News Service 1915 年已为农户提供价格和市场状况信息；1921 年 USDA 同时代刊物又记载把主要农业市场报告通过无线电发送到多个州。

Sources:
- https://www.nal.usda.gov/collections/special-collections/usda-tobacco-market-news-service-records
- https://earlyradiohistory.us/1921extd.htm

这说明：

- “远方价格更快到农场”不是 Internet 时代才出现的问题；
- 网络媒介更替可以从 telegraph → radio → telephone → Web/mobile 来观察；
- 每一次媒介更替都要重新问 receiving equipment / literacy / intermediary / timeliness，而不能只记发送端技术存在。

### India e-Choupal, 2000s (comparison only)

World Bank 2005 年介绍的 e-Choupal 通过村级 Internet kiosk 和操作员让农户查价格、技术和销售渠道，说明 `intermediated digital access` 也不是中国特有现象。

Source:
https://blogs.worldbank.org/en/psd/echoupal-empowering-the-links-in-the-value-chain

本仓不扩写印度平台史；比较结果写回 `how-people-lived`。

---

## 16. Evidence register

| Claim | Evidence | Grade | Confidence | Caveat |
|---|---|---:|---:|---|
| 2006 中国农业信息网 locator `www.agri.gov.cn` | 农业部同期通知 | A | high | 不是 capture |
| 邢台网站+短信+800电话+广播电视+报纸+人工节点 | 2006 NDRC 收录工作材料 | A | high | impact 数字为项目自报 |
| 三电合一明确采用多渠道 | 2008 同期报道 + 区政府总结 | A/B | high | 地方实施程度不一 |
| 12316 phone 2006 / SMS 2009 | 农业部 2011 通知 | A | high | 各省上线时间不同 |
| 农村互联网普及率 2008 约 11.7% | CNNIC | A | high | 网民定义依 CNNIC 调查口径 |
| 农民信箱促成具体联系/合同 | 2006 浙江日报人物材料 | B | medium-high | success story selection bias |
| 2010 经纪人把网络视为长期销售方向 | 同期新华社/媒体人物材料 | B + 1P | medium-high | 经纪人不是普通农户均值 |
| 网上购销实际混合电话/email/fax/SMS | 2008 商务部信息 | A/B | high | 精确 Web workflow unknown |
| 2008 SMS 谣言扰动柑橘市场 | 同期报道 + 农业部门说法 | B | high | 精确损失/因果幅度慎用 |
| historical DOM / form / browser requirements | 未验证 | — | unknown | M1 not achieved |

---

## 17. Hindsight risks

- 不把 1994 前写成“中国农村完全没有远程信息系统”。
- 不把科研联网/国家农业网站存在写成普通农户已经 Internet-enabled。
- 不把“村村能上网”写成“户户上网”。
- 不把“网上购销”写成 browser-only/self-service/e-payment。
- 不把政府项目 self-reported transaction amount 当作独立审计结果。
- 不把少数数字农民/经纪人成功故事写成全国普及。
- 不把 2020s 对平台风险的认知倒灌给 2006 用户。
- 不把 modern CMS 中的旧通知页面截图当作 historical original。

---

## 18. Next archaeological targets

优先级从高到低：

1. **中国农业信息网 `www.agri.gov.cn` 2003—2010 verified captures**：首页 + 行情/供求入口至少两个时点；
2. **浙江农民信箱 early captures/help pages**：注册、供求发布、短信触达、账号/实名条件；
3. **新农村商网 2006—2009**：供货录入究竟由谁操作，在线“对接”之后如何转线下；
4. **12316 operator-side artifact**：坐席软件、知识库、工单、短信 gateway、专家状态；
5. **县级农业网站 + village service station**：页面与线下代操作之间的具体 handoff；
6. **失败案例**：买家毁约、物流失败、拒收、价格过时、短信没到、热线排队、错误行情。

最值得证明的新问题不是“农村互联网什么时候出现”，而是：

> **哪一个时刻，Internet 已经足以改变一个非网民农户的生产/销售决策？**

这可能比“第一位上网农民”更接近中文互联网真正进入普通生活的历史。