# WEATHER_FORECAST_WARNING_SMS_WAP_WEB_AND_ACTION_STATE_GAPS_2001_2015

## 0. Scope

本 note 研究约 2001—2015 中文互联网中的一个事务型对象：**天气预报、灾害预警、短信、WAP、气象门户与网络媒体联动究竟怎样把“未来几小时/几天的天气”送到普通人手里，以及页面上可见的预报/预警和现实中的接收、理解、行动之间存在哪些状态缺口。**

它不是中国气象事业通史，也不是全球天气传播史。1980 年电视天气预报、19 世纪电报气象网络、1960s NOAA Weather Radio 只作为必要前史边界；2021—2026 的短临预警/叫应只作 afterlife 校验，不扩张本仓约 1995—2015 中文旧网 scope。

本轮首先检查了仓库现有 school website、ambient information、travel booking、mobile number、agricultural information 等专题；未发现独立的 weather forecast / warning / 12121 / SMS / WAP / China Weather transaction-state note。

检索日期：2026-09-08。

Life-history companion：`tmzncty/how-people-lived/topics/weather-forecast-warning-near-future-executability-china-1980-2026.zh-CN.md`

---

## 1. Claim list before narrative

本轮只把以下 claim 写到较高确定度：

1. **B/C + B / high**：广东气象部门 2001 年已经开展手机天气短信服务；2004 年同期报道显示该服务已形成大规模订阅，但订阅量不能外推全国人口。
2. **B / high**：2008 年雨雪冰冻期间，武汉、广州已经通过手机短信把天气、道路/客运/铁路状态和行动建议组合后主动送给市民；部分发送具有地理定向/组织定向特征。
3. **B / high**：`www.weather.com.cn` 于 2008-07-28 正式上线，提供天气预报、灾害预警、旅游天气等栏目；这是强 historical locator，不是 historical capture。
4. **A / high**：2009-07-16 中国气象局启动气象预警信息共享服务平台，与人民网、新华网、新浪网等十多家网络媒体建立预警联动播发机制。
5. **A / high**：2009—2010 同期中国天气网站点材料明确出现 WAP 气象服务，且 Web 页面同时继续提示 12121/96121 电话查询。
6. **A / high**：2014 中国天气网改版把预报时效延长到 15 天，增加未来三天逐 3 小时预报，并明确说明预报越远不确定性越大、会滚动订正。
7. **A/B / high**：当前 `weather.com.cn` live host 上仍可访问带 2009—2010 发布时间的预警/视频内容，并暴露出 `.shtml`、iframe、打印/收藏、Flash player 提示等旧形态痕迹；但 current live page **不是** verified 2009/2010 capture。
8. **D / high as model**：必须把 `forecast generated`、`page published`、`SMS queued/sent/delivered`、`user noticed`、`understood`、`believed`、`action possible`、`action taken` 分开。
9. **D / high as preservation rule**：`historical timestamp on live page != historical capture`，`video page displays Flash warning today != historical Flash asset preserved`。

---

## 2. Prehistory boundary：Internet 没有发明“远程天气未来”

中国 1994 年正式全功能接入全球 Internet 以前，普通人的天气信息已经通过广播、报纸、电视、电话等远程传播。2010 年宋英杰等人的气象节目史回顾记录，20 世纪 80 年代以前广播/报纸已承担公众天气预报，央视电视天气预报于 1980-07-07 开播。

Source:
https://www.gmw.cn/02sz/2010-01/01/content_1070928.htm

Evidence grade: **C/B boundary**  
Confidence: **high** for program history.

海外也一样。美国 National Weather Service 的官方历史资料显示，19 世纪中叶电报已经用于集中不同地点的天气观测；1870 年 Army Signal Service 建立国家级 weather observation/warning 体系。NOAA Weather Radio 又在 1960s 发展为连续天气广播，后来的警报功能可直接进入私人住宅。

Sources:
https://www.weather.gov/timeline/radarfaq
https://www.weather.gov/gid/ouroffice
https://www.weather.gov/lch/noaa

这些前史只用于限制 claim：

> **Web 是天气传播栈的新层，而不是远程预报/预警的起点。**

因此 old-Web 研究不能把 TV、radio、telephone、SMS 当成“网站出来以前的无关旧媒介”；它们和 Web 长期组成同一公共信息系统。

---

## 3. 2001—2004：SMS 是独立事务，不是“手机打开天气网页”

广东省气象局现行页面回顾称，广东省气象部门 2001 年率先开展手机短信气象服务；2004 年同期财经报道把开始时间写为 2001 年 11 月，并称当时全省手机气象短信用户已超过 600 万户。

Sources:
https://gd.weather.com.cn/fwmh/05/1325562.shtml
https://finance.sina.com.cn/chanjing/b/20041231/10221264836.shtml

Evidence grade:
- official retrospective: **B/C boundary**;
- 2004 contemporary media: **B**.

这里必须至少拆三种东西：

```text
DAILY_SUBSCRIPTION_SMS
EMERGENCY_BROADCAST_SMS
MOBILE_WEB_WAP_QUERY
```

它们不能写成同一个“手机天气服务”。

### 3.1 Daily subscription state machine

```text
SERVICE_EXISTS
→ user knows service
→ subscription request sent
→ operator/service confirms subscription
→ recurring forecast generated
→ SMS queued
→ SMS sent
→ carrier accepts
→ handset reachable
→ SMS delivered
→ user notices
→ user reads
→ forecast still timely
→ user interprets
→ user changes/does not change plan
```

Critical gaps:

```text
SUBSCRIBED != MESSAGE_DELIVERED
MESSAGE_DELIVERED != MESSAGE_READ
MESSAGE_READ != FORECAST_BELIEVED
FORECAST_BELIEVED != ACTION_TAKEN
```

### 3.2 Denominator warning

“600 万用户”只能证明这一服务已达到显著规模；本轮没有证据把它换算为：

- 广东人口占比；
- 独立自然人数；
- 手机用户渗透率；
- 每日实际阅读率；
- 全国采用率。

不能用一个省的商业增值业务倒填“中国手机用户已经习惯天气短信”。

---

## 4. 2008 rain/snow emergency：SMS 把天气、交通和行动指令编成同一消息

### 4.1 Wuhan：第一次政府 SMS 的价值在“不要白跑已经停运的车站”

2008-01-16 的同期报道记载，武汉市部分市民收到署名“武汉市人民政府”的三则短信；其中一则直接告诉市民高速公路关闭、部分长途客运停驶，另外两则提供未来三日雨雪预报和咨询电话。报道称，此前长途汽车站已经停运，仍有大量不知情旅客前往车站。

Source:
https://news.sina.com.cn/c/2008-01-16/061014752884.shtml

Evidence grade: **B**  
Confidence: **high**.

这说明事件消息不是单一 `WEATHER_FORECAST`，而是 composite payload：

```text
WEATHER_STATE
+ TRANSPORT_STATE
+ CONSULTATION_ENDPOINT
+ ACTION_GUIDANCE
```

旧网/通信考古如果只保存天气文字，会漏掉它最直接改变生活的部分——交通事务状态。

### 4.2 Guangzhou：network targeting 已经让“同一事件，不同用户”收到不同消息

2008-01-31 同期报道记载，广州移动在冰冻雨雪期间通过 10086、小区短信、校讯通等渠道发送近 2300 万条定向短信。其中包括：

- 京珠高速区域：“不要驾车北上”；
- 校讯通：向学生/家长体系发送相关通知；
- 铁路相关区域：提醒不要选择铁路出行、按规定办理退票；
- 配合气象台发送天气信息。

Source:
https://news.sina.com.cn/c/2008-01-31/121314871702.shtml

Evidence grade: **B**  
Confidence: **high** for messaging design; counts = messages, not unique people.

Archaeological implication:

```text
same weather event
!= same message to everyone
```

可能的 targeting key 包括：

- cell/coverage area;
- organization membership (`校讯通`);
- government emergency list;
- subscription relation.

未来如果取得运营商侧日志，至少要区分：

```text
TARGET_SET_BUILT
→ MESSAGE_BATCH_CREATED
→ GATEWAY_ACCEPTED
→ CARRIER_SENT
→ HANDSET_DELIVERED
```

一篇新闻写“发送 X 万条”通常只能证明其中某个上游状态，不能自动证明每部手机成功收到。

---

## 5. 2008 historical locator：China Weather `www.weather.com.cn`

2008-07-28 国际在线同期报道（新浪保存）明确写：

```text
中国天气网 (www.weather.com.cn)
```

当日正式上线，栏目包括天气预报、灾害预警、天气资讯、气候变化、旅游天气、气象知识等。

Source:
https://news.sina.com.cn/s/2008-07-28/144214229855s.shtml

Evidence grade: **B**  
Confidence: **high** for host/name/launch date.

2009 年中国天气网自己也回顾：2008-07-28 正式上线。

Source:
https://www.weather.com.cn/index/lssj/11/374248_4.shtml

Evidence grade: **A/B boundary**（2009 年官方站点对一年前自身历史的描述）  
Confidence: **high**.

### What this proves

- host existed;
- site name existed;
- public launch date;
- broad service categories.

### What it does NOT prove

- exact 2008 homepage path;
- HTTP status/header set;
- charset;
- table/div/frameset structure;
- JS library versions;
- browser matrix;
- cookies/sessions;
- CDN/image host topology;
- cache/refresh interval;
- how forecast data moved from internal system to web;
- user reach/adoption;
- whether a specific user saw an update before traveling.

因此：

```text
CONTEMPORARY LOCATOR
!= VERIFIED HISTORICAL CAPTURE
```

---

## 6. 2009：warning syndication——用户不必进入 weather.com.cn 才能看见气象局预警

2009-07-16，中国气象局启动气象预警信息共享服务平台，并与人民网、新华网、新浪网等十多家网络媒体签订预警信息联动播发协议。

Sources:
https://news.weather.com.cn/index/lssj/07/22356.shtml
https://www.weather.com.cn/zt/tqzt/0907qyys/07/64346.shtml
https://www.weather.com.cn/zt/tqzt/0907qyys/07/64355.shtml

Evidence grade: **A**  
Confidence: **high**.

官方同期介绍还说明，平台按地域、类型、级别、状态和发布时间整理不同气象台站的预警，供媒体快速获取和传播。

因此 2009 Web topology 至少可能是：

```text
LOCAL_MET_OFFICE
→ WARNING_SOURCE_DATA
→ CMA SHARING PLATFORM
→ PEOPLE/XINHUA/SINA/etc.
→ portal page / news page
→ reader
```

不能写成：

```text
user must visit www.weather.com.cn
```

更不能用 weather.com.cn 的 pageview 直接估算所有在线 warning reach。

### New state gap: source authority vs presentation host

```text
WARNING_ISSUED_BY_MET_OFFICE
!= WARNING_HOSTED_ON_CMA_SITE
!= WARNING_REPUBLISHED_BY_PORTAL
```

历史研究者需要同时保存：

- original issuing office;
- issuance timestamp;
- warning type/level/status;
- syndication timestamp if known;
- portal publication timestamp;
- whether later update/cancellation propagated.

否则可能拿到“红色预警”页面却漏掉几小时后的解除/降级状态。

---

## 7. 2009—2010：WAP、电话、Web、SMS 是并行 stack，不是技术世代替换

2009-10-22 青海省气象局同期页面介绍“气象 WAP 业务”，称可浏览天气预报、实况、卫星云图、多普勒雷达、天气传真图、灾害预警等信息。

Source:
https://www.weather.com.cn/qinghai/qxfwxx/10/73560.shtml

Evidence grade: **A**  
Confidence: **high** for service description.

当前中国天气网 host 上保存的 2010 年预警内容页仍展示：

- `收藏此页`；
- `打印`；
- 400-6000-121 气象服务热线；
- 12121/96121 天气电话查询；
- “通过手机登陆中国天气 WAP 版查看各地天气资讯”。

Examples:
https://gd.weather.com.cn/alarm/yjxh/03/264457.shtml
https://henan.weather.com.cn/alarm/yjxh/03/285861.shtml
https://hunan.weather.com.cn/alarm/yjxh/03/271607.shtml

Evidence grade: **historical content on current live host**  
Confidence: **high** for current rendered text and historical timestamp field; **low/unknown** for original 2010 rendering/runtime.

### Important topology

```text
                     +--> TV/radio
meteorological data +--> 12121/96121 telephone
                     +--> subscription SMS
                     +--> emergency SMS
                     +--> desktop Web
                     +--> WAP mobile Web
                     +--> portal syndication
```

这比线性叙述：

```text
TV -> Web -> smartphone
```

更接近现实。

---

## 8. Forecast page and warning page must not be collapsed

### Forecast

通常回答：

```text
what may happen
where
when
temperature/rain/wind/etc.
```

### Warning

至少还需要：

```text
issuer
issue time
hazard type
level/color
affected area
valid/state/update/cancel
defense guidance
```

因此 state machine 不同。

### 8.1 Forecast state machine

```text
MODEL/OBSERVATION AVAILABLE
→ FORECAST PRODUCED
→ FORECAST VERSION PUBLISHED
→ PAGE/CACHE UPDATED
→ USER LOADS PAGE
→ CORRECT LOCATION SELECTED
→ CORRECT TIME HORIZON READ
→ USER UNDERSTANDS UNCERTAINTY
→ USER ACTS / DOES NOT ACT
→ FORECAST LATER UPDATED
```

### 8.2 Warning state machine

```text
HAZARD DETECTED
→ WARNING DECISION
→ WARNING ISSUED
→ WARNING DISTRIBUTED
→ CHANNEL ACCEPTED
→ USER/ORG RECEIVED
→ USER/ORG NOTICED
→ LEVEL/AREA UNDERSTOOD
→ RESPONSE AUTHORIZED
→ RESPONSE EXECUTED
→ WARNING UPDATED / DOWNGRADED / CANCELLED
```

Critical gaps:

```text
ISSUED != DELIVERED
DELIVERED != NOTICED
NOTICED != UNDERSTOOD
UNDERSTOOD != ACTION AUTHORIZED
ACTION AUTHORIZED != ACTION EXECUTED
OLD WARNING PAGE != CURRENT WARNING STATE
```

---

## 9. 2010 preserved pages：current live content 不是 M1 capture

当前搜索可找到多条标注 2010 日期的 China Weather warning page，例如：

```text
https://gd.weather.com.cn/alarm/yjxh/03/264457.shtml
https://hunan.weather.com.cn/alarm/yjxh/03/271607.shtml
https://henan.weather.com.cn/alarm/yjxh/03/285861.shtml
```

页面呈现典型 legacy-looking 结构：

- `.shtml`；
- breadcrumb；
- historical timestamp；
- 字体切换；
- 收藏/打印；
- warning table；
- phone/WAP service footer。

另有视频页面目前明确显示：

```text
Get the Flash Player to see this player.
```

Example:
https://www.weather.com.cn/video/09/67553.shtml

当前页面还出现 `iframe` 标记/占位。

### Preservation rule

这些现象只能证明：

> **2026 年当前 live site 仍保留带旧时间戳的内容对象，并呈现某些 legacy UI/runtime 痕迹。**

不能直接证明：

- 2010 页面当年就是今天这份 DOM；
- Flash player 当年的 SWF 仍存在；
- Flash 版本要求；
- video URL；
- 当年 iframe src；
- 当年 CSS/JS；
- 当年 charset；
- 当年页面完整可执行。

`Get the Flash Player` 今天出现，甚至可能说明**当前模板仍引用一段已经失效的历史播放器链**，而不是“Flash 资产保存完好”。

所以：

```text
LIVE LEGACY PAGE
!= HISTORICAL REPLAY
!= HISTORICAL EXPERIENCE
```

---

## 10. 2014 redesign：更长 horizon 是产品功能，不是确定性保证

中国天气网六周年新版公告称：

- 预报时效延长至 15 天；
- 增加未来三天逐 3 小时预报；
- 新增/调整城市、景点、空气质量等产品；
- 提供在线问卷收集用户反馈。

公告同时明确提醒：预报不能 100% 确定，预报时效越长不确定性越大，网站会滚动订正。

Source:
https://www.weather.com.cn/wzfw/gbgg.shtml

Evidence grade: **A**  
Confidence: **high**.

Historical locator printed in announcement:

```text
http://www.weather.com.cn/index/feedback_domestic_2014.shtml
```

Evidence: **A / high locator confidence**.

### State gap: horizon vs version

长期预报页面必须视为 versioned data：

```text
FORECAST_FOR_DATE_D generated at T1
!= FORECAST_FOR_DATE_D generated at T2
!= OBSERVED_WEATHER_AT_D
```

一个 archive 只抓到 T1，不等于抓到了“当时最终预报”。

如果未来研究 15 天预报准确率或用户决策，必须至少保存：

- forecast target date/time;
- issue/update time;
- location;
- model/product if known;
- later revision;
- actual observation;
- user action timing.

---

## 11. User evidence：forecast view 和 behavior 之间必须有独立证据

2008 北京一篇同期报道中，记者写自己和不少市民一样订阅天气短信，并描述收到次日中雨预报后降雨未出现；报道还提及此前气温预报偏差后市民抱怨穿衣受到影响。

Source:
https://news.sina.com.cn/c/2008-05-09/201113854723s.shtml

Evidence grade: **B（含 contemporaneous first-person reporter account）**.

2009 海口同期报道记录，一名市民原计划全家元旦去三亚，因阴冷潮湿天气与孩子考试临近取消；另一个受访者也称天气影响博鳌出游计划。

Source:
https://www.weather.com.cn/index/lssj/01/17323.shtml

Evidence grade: **A/B boundary**.

因此可以高置信写：

```text
FORECAST INFORMATION
can enter real household travel decisions
```

但不能从这两个个案推出：

```text
MOST USERS CHECKED WEB BEFORE TRAVEL
```

更不能由某个页面访问量推出页面造成了某个现实行为。

---

## 12. Afterlife check: 2019—2026 why old states matter

本节只用于验证 2001—2015 状态模型，不扩张仓库 scope。

### 12.1 2019: same warning, different actionability

2019-08-10 上海暴雨橙色预警期间，新华社照片同时记录虹桥机场旅客排队退改签、外卖员继续冒雨配送。

Source:
https://www.sohu.com/a/332835535_267106

这验证：

```text
WARNING_RECEIVED
!= USER_CAN_STOP_ACTIVITY
```

旧 Web 的 `防御指南` 不能被直接当作现实执行日志。

### 12.2 2021: warning existence is not the end of the causal chain

郑州市气象台 2021-07-20 上午继续发布暴雨红色预警；同期人物采访却显示个人仍可能因为没理解量级、已有事务或经验上的信任校准而继续出行/送孩子。

Sources:
https://www.cneb.gov.cn/2021/07/20/ARTI1626744367803911.shtml
https://static.nfnews.com/content/202107/22/c5552821.html

这验证老 Web 研究为什么必须拆：

```text
PAGE/SMS SAYS RED
!= SOCIAL SYSTEM PAUSED
```

### 12.3 2024—2026: modern warning systems increasingly optimize lead time and response coupling

2024 福建同期人物材料记录养殖户收到台风预警短信后撤离上岸；2025 年底中国气象局发布 2026—2030 新一代短临预警方案，强调提高提前量与预警—响应联动。

Sources:
https://hxdsb.fjdaily.com/pc/con/202410/08/content_402138.html
https://app.www.gov.cn/govdata/gov/202512/02/540711/article.html

这验证 old-Web 时代最值得保存的不只是“页面长什么样”，还有：

- issue time;
- delivery time;
- update time;
- geographic targeting;
- action rule;
- acknowledgement/response if any.

---

## 13. Browser / runtime questions for future M1 capture

如果以后拿到 2008—2014 China Weather capture，应优先记录：

### 13.1 HTTP / encoding

- capture datetime;
- final URL / redirects;
- HTTP status;
- `Content-Type` + charset;
- server/cache headers if present;
- compressed/uncompressed behavior.

### 13.2 HTML topology

- frameset / iframe;
- table layout vs CSS layout;
- page charset declaration;
- form/select used for city switching;
- warning table semantics;
- print/favorite JS;
- image map;
- province subdomain topology (`gd.weather.com.cn`, etc.).

### 13.3 Dynamic dependencies

- weather JSON/XML endpoint;
- update interval;
- JS host;
- image/CDN host;
- Flash `.swf` URL;
- video backend;
- map/radar resources;
- WAP host;
- ad/analytics resources.

### 13.4 User state

Weather pages may not require login, but that does **not** mean state-free. Need check:

- selected city cookie;
- homepage preference;
- geolocation behavior;
- local storage (later period);
- favorites;
- subscription forms;
- SMS phone-number submission;
- feedback form session/CSRF behavior.

### 13.5 Historical browser matrix

At minimum attempt:

- IE6/IE7-era rendering for 2008–2010 captures;
- contemporary Firefox if relevant;
- feature-phone WAP separately from desktop browser;
- Flash-enabled browser for archived video assets if legally/technically possible.

Do not claim “works in IE6” until tested.

---

## 14. Warning archive state: update/cancel is part of the record

预警不是一个静态文章，它有 lifecycle。

建议未来结构化保存：

```text
warning_id (if any)
issuer
hazard
area
level
issued_at
valid_from
valid_until (if present)
state = active / updated / downgraded / cancelled / expired
supersedes
superseded_by
source_url
capture_datetime
```

原因：当前 China Weather 页面中就能看到“发布”“解除”等不同状态。只抓初始页面可能造成严重误读。

例如：

```text
RED WARNING PAGE EXISTS
```

无法单独回答：

```text
how long was it active?
was it later downgraded?
did portal mirrors update?
did SMS recipients get cancellation?
```

---

## 15. Historical visibility bias

天气旧网有一个很强的保存偏差：

### 容易保存

- official forecast page;
- warning page;
- portal repost;
- disaster article;
- page timestamp;
- warning color;
- institutional message-count report.

### 很难保存

- actual SMS body on a specific handset;
- delivery report;
- feature-phone WAP rendering;
- 12121 telephone voice tree;
- user called but line busy;
- user read warning but ignored it;
- employer refused time off;
- parent changed school plan;
- trip that never happened because forecast stopped it.

因此 historian-visible weather history 很容易变成“机构发布史”，而不是“普通人的近未来行动史”。

必须明确：

```text
PUBLICATION TRACE
!= RECEPTION TRACE
!= ACTION TRACE
```

---

## 16. Counterexamples

### Counterexample A — more channels do not mean more trust

2008 北京 weather SMS 误报抱怨说明，channel reach 与 forecast credibility 是两个变量。

### Counterexample B — warning page can be correct while user action still fails

2021 郑州说明，预警存在与组织/个人实际响应之间仍有很长链条。

### Counterexample C — same warning does not produce same action

2019 上海旅客可办理退改签、外卖员仍在街头；劳动条件改变 actionability。

### Counterexample D — current old-looking page does not prove preserved old runtime

2026 live host 上出现 2010 timestamp、Flash 提示和 `.shtml`，仍不能证明 2010 DOM/Flash/headers 已被复原。

### Counterexample E — longer horizon does not mean firmer future

2014 official redesign notice explicitly says uncertainty rises with lead time and forecasts are rolled/revised.

---

## 17. Hindsight risks

禁止：

1. 把 2008 中国天气网上线写成中国普通家庭第一次获得天气预报；
2. 把 2001 气象短信和后来全网应急广播混成一个制度；
3. 把 `sent X million messages` 写成 `X million unique people successfully received`；
4. 把 portal repost 当成 original warning issuer；
5. 把 current live legacy page 当作 Wayback capture；
6. 把 current browser 的 `Get Flash Player` 当成 2009 runtime 已经验证；
7. 把 15-day page 当成“15 天后天气已知”；
8. 把 warning level 当成现实停课/停工/停运状态；
9. 把“用户因为天气取消旅行”写成 Web 单独造成，除非来源明确说明信息来源和行动链；
10. 把 2021 极端事件反向投射成 2008 用户已经普遍不信预警。

---

## 18. Unknowns / next evidence targets

### Historical capture targets

1. `www.weather.com.cn` homepage, 2008-07-28 ± 30 days;
2. 2008 Olympic weather channel;
3. 2009 warning-sharing platform frontend if public;
4. 2009/2010 WAP weather portal;
5. a 2009–2010 warning detail page with active + cancellation pair;
6. 2014 redesign homepage + feedback form.

### Technical targets

- original charset;
- iframe/frameset usage;
- original `.shtml` generation/staticization behavior;
- province subdomain relation to central host;
- actual warning feed format;
- WAP markup (`WML` vs mobile HTML) and host;
- SMS subscription endpoint / short code by region;
- Flash SWF paths and required player version;
- desktop browser support statements;
- page cache/update latency.

### Life-use targets

- 2007—2010 BBS/blog posts saying “because forecast I changed/cancelled X”;
- commuters’ use of SMS vs Web;
- feature-phone WAP data-cost concerns;
- 12121 call volume and busy/failure behavior;
- weather information use among outdoor workers vs office workers;
- whether users cross-checked multiple providers after forecast misses.

---

## 19. Historical capture attempt / M1 status

本轮已经取得：

- strong contemporary locator: `www.weather.com.cn`；
- 2008 launch report；
- 2009 official warning-sharing platform pages；
- current live host 上多条 2009—2010 historical-content pages；
- current legacy video page 的 Flash-player failure marker；
- 2014 official redesign announcement + feedback locator。

本轮也尝试通过 Web 工具访问 Internet Archive CDX：

```text
https://web.archive.org/cdx/search/cdx?url=www.weather.com.cn/*&from=2008&to=2010&output=json...
```

以及 `www.weather.com.cn/index.shtml` 的 2008—2010 CDX 查询，但当前访问环境将构造的 CDX URL 拒绝为不可直接打开的 URL，没有返回 capture 列表。

因此只能写：

> **本轮没有验证到一份可以按照 METHOD 检查 capture datetime、HTTP headers、charset、DOM、JS、Flash/WAP subresources 与历史浏览器行为的合格 historical capture。**

不能写：

> “Wayback 没有保存中国天气网。”

也不能把当前 live legacy page 降格/升级成 archive capture。

### M1

**NOT ACHIEVED IN THIS SLICE**

原因：有 locator、有 contemporaneous content、有 current live legacy surface，但没有 verified historical replay/capture contract。

---

## 20. State-gap summary

```text
FORECAST_PRODUCED
!= FORECAST_PUBLISHED
!= PAGE_UPDATED
!= USER_FETCHED
!= USER_READ
!= USER_BELIEVED
!= USER_ACTED
```

```text
WARNING_ISSUED
!= PORTAL_REPUBLISHED
!= SMS_SENT
!= SMS_DELIVERED
!= USER_NOTICED
!= USER_UNDERSTOOD
!= ORGANIZATION_RESPONDED
!= USER_COULD_STOP
!= HARM_AVOIDED
```

```text
WEATHER.COM.CN EXISTS IN 2008
!= 2008 HOMEPAGE CAPTURE VERIFIED
!= 2008 RUNTIME RECONSTRUCTED
```

```text
CURRENT PAGE HAS 2010 TIMESTAMP
!= ORIGINAL 2010 DOM
!= ORIGINAL 2010 HTTP RESPONSE
!= ORIGINAL 2010 FLASH/WAP DEPENDENCIES
```

```text
15-DAY FORECAST VISIBLE
!= 15-DAY FUTURE CERTAIN
```

这些 gap 正是此专题进入 old-web-archaeology 的理由。

---

## 21. What this changes about old-Web archaeology

天气网站提醒我们：旧 Web 最值得复原的往往不是“这一页长什么样”，而是**这一页在一个不断变化的现实世界中究竟代表哪个时刻的未来。**

普通文章的旧版本主要是内容差异；天气页面的旧版本却可能直接对应不同的行动窗口：上午说晚上有雨，下午改成暴雨，傍晚升级红色预警，夜里解除。只保存最后一页，就会把一段原本不断修订的未来压扁成一个静态结论。

因此，气象旧网的核心考古单位不应只是 page，而应该是：

> **versioned forecast / warning event + delivery channel + user action window。**

这也把中文旧网和普通人生活真正接了起来：网页不是在那里“显示天气”，而是在不断重新告诉人——**你还有多少时间改变今天。**
