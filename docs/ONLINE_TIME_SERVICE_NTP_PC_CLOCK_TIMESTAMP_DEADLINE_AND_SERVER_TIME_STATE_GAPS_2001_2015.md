# ONLINE_TIME_SERVICE_NTP_PC_CLOCK_TIMESTAMP_DEADLINE_AND_SERVER_TIME_STATE_GAPS_2001_2015

## 0. Scope

本 note 研究约 2001—2015 中文互联网中的一个此前未独立建模的基础设施对象：**网络授时、PC 校时、页面显示时间、服务器权威时间、时间戳与“某时某分开放/截止”的 Web 事务之间究竟有什么状态缺口。**

它不是国家授时工程通史，也不是钟表史。1970s–1980s 的广播/电话/长短波授时只作为必要前史边界；2019–2026 的抢票、候补、毫秒悬浮时钟只作 afterlife 校验，不扩张本仓约 1995–2015 中文旧网 scope。

Life-history companion：

`tmzncty/how-people-lived/topics/from-calling-117-to-millisecond-countdowns-public-time-network-synchronization-and-executable-deadlines-china-1970-2026.zh-CN.md`

检索日期：2026-09-09。

本轮已先检查当前树中的：

- `SHIFT_WORK_JOB_LISTINGS_ROSTERS_AND_ACTUAL_CLOCK_STATE_GAPS_2005_2015.md`；
- railway ticketing / appointment / exam result / web form / transaction deadline 等事务专题；
- `PREHISTORY_BOUNDARY.md`；
- `METHOD.md`。

未发现独立的 public time / NTP / PC clock / server-time / timestamp / deadline state note。

---

## 1. Claim list before narrative

本轮只把以下 claim 写到较高确定度：

1. **B / high**：2003 年新华社报道显示，117 电话报时是公众熟知的服务之一，并在电信网编号调整中改为 12117；这证明 Web 以前/之外已有面向普通人的公共时间接口。
2. **官方机构回顾 + 同期机构材料 / high**：国家授时中心 2001 年创建 `www.time.ac.cn`“时间科普”网站并提供公益网络授时；2004-05-01 发布“时间精灵”网络校时组件。
3. **A / high**：2009-01-01 闰秒调整时，国家授时中心短波、低频时码、Internet、电话和时间戳等不同服务同时进行相应调整；这些是不同服务栈，不应混成一个“北京时间网页”。
4. **A / high**：时间戳服务在闰秒附近主动暂停，说明 `wall-clock display` 与 `trusted timestamp service` 是不同事务。
5. **B + 同时代用户材料 / high**：2009 年电商秒杀已让普通用户围绕精确开售时刻守候，并出现自动“秒杀器”；但现有材料不能证明淘宝当时具体服务器时钟实现。
6. **D / high as model**：必须拆开 `standard time generated -> signal/service published -> client receives -> local clock adjusted -> browser renders -> request sent -> server receives -> server evaluates deadline -> DB commits -> user sees result`。
7. **D / high as preservation rule**：`page shows 20:00 != server opened exactly when the browser clock showed 20:00`；`archived timestamp != proof of historical server clock accuracy`。
8. **D / high as preservation rule**：历史 Web archive 即使完整保存 countdown HTML/JS，也通常没有保存生产服务器的 NTP source、系统时钟偏差、请求队列、数据库 commit time 与用户本地钟。
9. **M1 partial only**：本轮找到一条指向 2013-01-10 `time.ac.cn/serve/BPL.htm` 的 Wayback locator，但当前工具回放返回 cache miss，不能升级为 verified capture。

---

## 2. Prehistory boundary：Web 没有发明公共标准时间

2003 年新华社报道，在电信网编号计划调整时直接写道：“许多百姓都知道，想了解时间可以打电话 117”，并说明 117 将调整为 12117。

Source:

https://news.sohu.com/13/81/news208738113.shtml

Evidence grade: **B / high**。

这条材料不是用来证明 1980s/1990s 的拨打率，而是限定 claim：

> **ordinary-user public time existed outside the Web.**

因此旧网研究必须避免：

```text
pre-Web = no remote standard time
```

更准确的是：

```text
radio / shortwave / telephone
  -> public or professional time access

later:
Internet time / PC synchronization / web display
  -> another delivery + execution layer
```

海外边界也一样。NIST 官方史记录 WWV 1950 年开始语音标准时间、1971 年提供电话 time-of-day service；RFC 958 则在 1985 年定义早期 NTP。

Sources:

- https://www.nist.gov/blogs/taking-measure/nist-radio-station-wwv-celebrates-century-service
- https://www.rfc-editor.org/rfc/rfc958.html

Evidence grade: **A/C boundary** for institutional history; **A** for RFC.

全球前史的完整讨论归 Life Horizons companion，本仓只用来限制“中文 Web 发明了校时”的叙述。

---

## 3. 2001：`time.ac.cn` 把标准时间变成普通 Internet 用户可直接访问的服务

国家授时中心 2009 年机构发展纪实记录：

- 2001 年创建“时间科普”网站；
- 网站提供公益网络授时服务和专家互动平台；
- 网络授时软件从 `CSAOtime 1.20` 起发展；
- 2004 年 5 月推出“时间精灵”。

Source:

https://lssf01.cas.cn/lssf/xwhd/cmsm/200910/t20091026_4508645.html

Evidence grade: **C/A boundary / high**。

这只能支持机构所述的服务发展，不自动证明：

- 2001 年页面具体 DOM；
- 每个版本的下载 URL；
- 用户实际浏览器；
- 是否必须 ActiveX/插件/管理员权限；
- 独立用户量；
- 每次校时是否成功。

本仓的研究单位至少要拆成：

```text
PLATFORM/INSTITUTION = 国家授时中心时间服务
HOST = www.time.ac.cn
PAGE = 时间显示/服务说明/下载/时间精灵页面
SOFTWARE = CSAOtime / 时间精灵
TIME SOURCE = backend/network timing source
CLIENT STATE = local Windows clock
```

不能把它们写成一个对象。

---

## 4. 2004—2005：“时间精灵”说明旧 Web 可以直接修改现实设备状态

中国科学院基础设施平台的 2005 年同期报道写道，国家授时中心从 2004-05-01 起通过“时间网站”发布“时间精灵”；到 2005 年日访问量近 4000，总访问量突破百万，并称软件被电信、金融、证券期货等行业采用。

Source:

https://lssf01.cas.cn/lssf/cdbssxt/xwdt/200512/t20051203_4511285.html

Evidence grade: **A/B boundary / high**。

这类页面在 old-Web 中很容易被误读成普通资讯页。实际上如果组件/软件能够修改 PC 系统时钟，它属于一种**现实状态执行接口**。

最低 state machine 应是：

```text
TIME_PAGE_VISIBLE
  -> COMPONENT/SOFTWARE_DISCOVERED
  -> DOWNLOAD_REQUESTED
  -> BYTES_RECEIVED
  -> SOFTWARE_INSTALLED/LOADED
  -> NETWORK_TIME_REQUEST_SENT
  -> RESPONSE_RECEIVED
  -> RESPONSE_VALIDATED/ACCEPTED
  -> CLOCK_ADJUSTMENT_ATTEMPTED
  -> OS CLOCK CHANGED
  -> USER OBSERVES NEW TIME
```

必须坚持：

```text
下载成功 != 安装成功
安装成功 != 可联网取时
网络响应到达 != 响应被接受
响应被接受 != OS 时钟已经改动
页面显示标准时间 != 本机系统时钟已同步
```

---

## 5. browser assumption：早期“网页校时”可能不是纯 HTML

后来的教程材料把“时间精灵”描述为首次需要下载小组件，以后进入特定网页点击“校准”即可；还提到 Windows 98/XP、代理和防火墙兼容性。

Source（2011 后续用户教程，仅作实现 locator，不用于锁定 2004 原始 UI）：

https://www.micoder.cc/blog/30.html

Evidence grade: **C/B boundary / medium**。

因此如果未来取得 2004–2006 historical capture，必须专门检查：

- HTML 中是否有 `<object>` / ActiveX；
- 是否下载 EXE/DLL/CAB；
- MIME type；
- IE security zone；
- Windows 权限；
- script 语言；
- proxy/firewall handling；
- 编码（GB2312/GBK）；
- 页面时间是服务器渲染、JS 本地递增还是组件读取；
- “校准”按钮到底调用浏览器脚本还是外部程序。

在没有原始 capture 与二进制前，不应重建一个“2004 时间精灵网页”截图然后当原件展示。

---

## 6. 2009 闰秒：最适合用来证明“不是所有时间状态都一样”

国家授时中心 2009-01-01 同期材料明确记录：北京时间出现 `07:59:59 -> 07:59:60 -> 08:00:00`；短波、低频时码、Internet、电话、时间戳服务都进行了相应闰秒调整。

Sources:

- https://lssf.cas.cn/sszs/gykj/cdbssxt/kycg/200901/t20090105_5054002.html
- https://english.ntsc.cas.cn/newsroom/events/202108/t20210811_277785.html

Evidence grade: **A / high**。

另有时间戳服务公告显示，服务在闰秒附近暂停约 20 分钟以保障可靠性和安全性。

Source:

https://timefreq.ntsc.cas.cn/kyjz/201205/t20120529_409625.html

Evidence grade: **A / high**。

这迫使我们拆开至少六种时间：

```text
STANDARD_TIME
BROADCAST_TIME
NETWORK_TIME
OS_SYSTEM_TIME
TRUSTED_TIMESTAMP_TIME
APPLICATION/DATABASE_EVENT_TIME
```

页面上肉眼看到的“北京时间”只是第七层：

```text
RENDERED_DISPLAY_TIME
```

### 6.1 最低同步状态模型

```text
SOURCE_CLOCK_VALID
  -> TIME_SERVICE_AVAILABLE
  -> CLIENT_QUERY_SENT
  -> PACKET/RESPONSE_RECEIVED
  -> DELAY/OFFSET_ESTIMATED
  -> RESPONSE_ACCEPTED
  -> CLOCK_SLEW/STEP REQUESTED
  -> OS CLOCK UPDATED
  -> APPLICATION OBSERVES UPDATED CLOCK
```

反例：

```text
NTP server reachable != client clock changed
client clock changed != app immediately rereads it
app timestamp valid != database commit happened at identical instant
```

---

## 7. 2009 同时代技术讨论：几十秒的漂移在旧网里是实际故障，不只是理论问题

2009 年 Panabit BBS 的一条同期用户/管理员讨论中，用户报告系统时间错误，并手工执行 `ntpdate 210.72.145.44`；输出显示 offset 约 36 秒。开发侧随后处理与相关库缺失有关的问题。

这类材料非常有价值，因为它证明：

> **PC/server time drift was an observed operational problem, not merely a standards-document concern.**

但它属于技术用户/管理员材料，不能外推普通家庭。

Evidence class: **B + contemporaneous technical user report**。

研究时应记录：

- OS/设备；
- time server IP/host；
- reported offset；
- sync command；
- error path；
- whether the adjusted clock persisted after reboot；
- whether application timestamps changed accordingly。

这条材料的主要方法价值，是提醒我们：一张历史网页上的时间戳可能来自一个当时并不准确的服务器。

---

## 8. 2009 电商秒杀：页面“几点开售”第一次把浏览器时间差变成普通生活问题

2009 年《钱江晚报》对淘宝“秒杀器”的同期报道保存了一个普通用户案例：白领 Julia 早晨等秒杀，来不及吃早餐，差点上班迟到仍未抢到。报道把“秒杀”解释为有限商品在指定时刻开售，大量网民同一时刻等待；“秒杀器”则用软件替人自动抢购，省掉守在电脑前的人力和时间。

Source:

https://news.sina.com.cn/c/2009-07-09/051715922117s.shtml

Evidence grade: **B + contemporaneous user report / high**。

这里 old-Web 必须拒绝一个很诱人的过度复原：

> 不能因为报道写“几点开始”，就断言用户浏览器页面里存在准确倒计时，更不能断言淘宝当时 production server 使用哪一个 NTP source。

最低 transaction model：

```text
CAMPAIGN_RULE_PUBLISHED(t_release)
  -> USER_LEARNS_RELEASE_TIME
  -> USER_LOCAL_CLOCK_APPROACHES(t_release)
  -> PAGE/CLIENT READY
  -> USER/AUTOMATION SENDS REQUEST
  -> REQUEST REACHES EDGE/SERVER
  -> SERVER_TIME_EVALUATES_ELIGIBILITY
  -> INVENTORY CHECK
  -> ORDER STATE CREATED/REJECTED
  -> USER SEES RESULT
```

必须固定：

```text
USER_CLICK_TIME != SERVER_RECEIVE_TIME
SERVER_RECEIVE_TIME != DB_COMMIT_TIME
DISPLAYED_COUNTDOWN_ZERO != INVENTORY_OPEN STATE necessarily
SAME DISPLAYED SECOND != truly simultaneous physical requests
```

---

## 9. `server time` 是事务权威，而不是浏览器上的装饰

旧 Web 研究中至少有四类“时间”经常被页面混在一起：

### 9.1 内容发布时间

例如：

`2009-07-09 05:17`

可能来自 CMS 字段。

### 9.2 用户本地显示时间

可能来自：

- OS clock；
- JavaScript `Date()`；
- timezone；
- browser locale。

### 9.3 服务端业务时间

决定：

- 是否已经开售；
- 是否过截止时间；
- 优惠是否有效；
- token 是否过期；
- session 是否过期。

### 9.4 数据库/审计时间

记录：

- request creation；
- order creation；
- payment callback；
- cancellation；
- settlement。

这四类字段可以很接近，但不能默认相同。

---

## 10. 页面倒计时与动态事务的保存缺口

假设 archive 完整保存一个写着：

```text
距离开售还有 00:00:05
```

的页面，也仍然无法自动证明：

1. 当年服务器的系统时间；
2. 用户 PC 的时间；
3. JS 是否由客户端本地递减；
4. 页面初始时间是否由服务端注入；
5. 时区；
6. network delay；
7. CDN/cache delay；
8. request 在生产系统什么时候到达；
9. inventory 何时真正切换状态；
10. DB transaction 何时提交。

因此：

> **countdown capture != transaction clock reconstruction**。

---

## 11. timestamp 也不能直接当“事件真实发生时间”

论坛、博客、订单页、新闻 CMS 常给研究者一个漂亮的时间戳。

但旧网考古至少要问：

```text
TIMESTAMP_SOURCE = client? web server? DB? CMS editor? imported record?
TIMEZONE = local? UTC? unknown?
CLOCK_SYNC = known? unknown?
EDITABLE = yes/no/unknown
RENDERING = historical or current re-render?
```

尤其是 current live legacy page：

```text
old content timestamp
+ modern CMS shell
```

只能证明当前系统把某个日期字段与旧内容对象关联，不能证明当前 DOM 就是历史页面，也不能证明原系统当年使用同一时区、同一格式或同一 clock source。

---

## 12. 2004 `time.ac.cn` 的另一个 ordinary-Web 线索：网络时间站点不只报时

2004-08-31，中国科学院机构材料记录 `time.ac.cn` 上线“任意地点日出日没时刻查询服务”，用户可以输入经纬度或地点查询世界各地日出日没时间；材料列举升降国旗、路灯、港口、旅游等用途。

Source:

https://lssf.cas.cn/sszs/gykj/cdbssxt/xwdt/200412/t20041211_5053984.html

Evidence grade: **A / high**。

2009 年百度知道中还有普通用户询问“哪里可以查到日出日落时间”，被采纳答案直接给出 `time.ac.cn/serve/sunriseset/`。

Source:

https://zhidao.baidu.com/question/84913465.html

Evidence grade: **B + contemporaneous user Q&A / medium-high**。

它说明 `time.ac.cn` 不只是一个专业授时后台，也真实进入了普通搜索/问答语境。

但：

```text
someone recommends URL
!= requester successfully loaded it
!= queried value was correct for their coordinates
!= they acted on the result
```

---

## 13. 历史页面应保存哪些技术字段

未来若取得 2001–2015 `time.ac.cn`、校时组件页或交易倒计时页的 verified capture，至少登记：

```text
archive_source
capture_url
original_url
capture_datetime
HTTP status
Content-Type
charset
redirect chain
HTML form/action
script src
object/embed tags
ActiveX/CAB/EXE/DLL links
JS Date/time logic
timezone assumptions
cookie/session requirement
subresource survival
browser assumptions
```

对校时组件额外登记：

```text
binary filename
version
hash (if legally obtained)
code-signing metadata
OS compatibility
network endpoint
protocol
privilege requirement
```

对“开售/截止”事务额外登记：

```text
published release/deadline
page countdown logic
server response headers (if historical capture has them)
client-side vs server-side time source
request endpoint
historical result availability
```

---

## 14. Archive attempt this run

### 14.1 Candidate found

本轮公开搜索找到一条由 Wikipedia 条目引用的 Wayback locator：

```text
capture_datetime candidate: 2013-01-10 21:00:25
original_url: http://www.time.ac.cn/serve/BPL.htm
archive: Internet Archive / Wayback Machine
```

Locator:

`https://web.archive.org/web/20130110210025/http://www.time.ac.cn/serve/BPL.htm`

其来源页面明确说该页面 archived from the original on 2013-01-10。

### 14.2 Replay result

本轮实际沿该 locator 请求回放，但当前访问工具返回 `cache miss`，没有取得可检查的 memento 内容。

因此当前状态只能写：

> **candidate capture found; historical replay NOT VERIFIED in this slice**。

不得写：

- Wayback 没保存；
- 页面当年打不开；
- 2013 capture 已验证；
- HTML/charset/subresources 已知。

### 14.3 Earlier-time targets still unverified

优先目标仍应包括：

```text
http://www.time.ac.cn/
http://www.time.ac.cn/stime.asp
http://www.time.ac.cn/times/timefairy.htm   # locator from later tutorial; historical form uncertain
http://www.time.ac.cn/serve/sunriseset/
```

年份优先：

```text
2001–2002
2004–2005
2008–2009
```

M1 status for this slice: **NOT ACHIEVED**。

这遵守 `METHOD.md`：locator 不冒充 capture，`没取到` 不写成 `不存在`。

---

## 15. 2015 boundary：PC 自动校时已经常态化到足以被技术教程当作系统设置讨论

2015 年技术教程已经会把国家授时中心、教育网 NTP 节点、Windows Time 服务和 Internet time synchronization 并列，说明到本仓尾端，“电脑自己从网络校准时间”已经是一种熟悉的系统管理动作。

Source:

https://www.cnblogs.com/dmcl/p/5858222.html

Evidence grade: **B / medium-high**（技术用户材料，不外推家庭总体）。

这适合作为 old-Web 终点边界：

```text
1990s/early 2000s:
manual clock + telephone/radio + dedicated client/service

2000s:
web-delivered calibration software + OS Internet Time + NTP

2010s:
accurate network-synchronized device time increasingly assumed by web/app transactions
```

---

## 16. Afterlife checks, 2019–2026：为什么这个旧网对象后来变得更重要

这些证据不扩大本仓 scope，只用来检验 2001–2015 state model 是否真的解释后来的生活。

### 16.1 2019：起售时刻成为普通人的明确操作时间

2019 春运报道：北京西站 8:00 起售，开售一分钟后就可能出现“排队人数超过余票数”；报道也记录用户提前定闹钟进入抢票模式。

Source:

https://finance.people.com.cn/n1/2019/0102/c1004-30498811.html

这验证：

> `shared clock -> public release schedule -> synchronized demand spike`

是一个真实 afterlife。

### 16.2 2024：候补把等待从人交回系统

12306 候补功能升级后，可以在多个未来日期/车次组合上持续等待，临客新增时系统可自动优先配售。

Source:

https://society.people.com.cn/n1/2024/0112/c1008-40157290.html

这验证另一个 state transition：

```text
USER_REFRESH_LOOP
-> SERVER_PERSISTENT_WAITLIST
```

### 16.3 2024：普通用户开始显式比较“不同时间源”

App Store 现行毫秒级悬浮时钟产品允许选择不同时间源、手动调节偏移；2024-01-17 一名用户报告实际秒抢会差 1–2 秒。

Source:

https://apps.apple.com/cn/app/%E6%82%AC%E6%B5%AE%E6%97%B6%E9%92%9F-%E6%8A%A2%E8%B4%AD%E7%A7%92%E6%9D%80%E5%8A%A9%E6%89%8B/id1546947240

这里再次验证本 note 的核心：

```text
DEVICE_TIME
!= SELECTED_NETWORK_TIME_SOURCE
!= PLATFORM_SERVER_TIME
!= REQUEST_ARRIVAL_TIME
```

---

## 17. Preservation bias：历史学家最容易看到的是“几点”，最难看到的是“那一秒系统发生了什么”

旧网页特别容易留下：

- `发布时间：2009-01-01 08:00`；
- `20:00 开售`；
- `报名截止 24:00`；
- 一个静态倒计时图片；
- 时间服务的宣传页；
- NTP 地址；
- 下载链接文本。

最难留下：

- production server 实际系统时钟；
- NTP peer/source；
- clock offset/drift；
- leap-second handling；
- user's PC clock；
- network latency；
- queue entry time；
- database commit timestamp source；
- rejected request logs；
- automation vs human click；
- edge/CDN cache state。

因此：

> **historian-visible timestamp != historical transaction time**。

这会造成一种很强的“精确性幻觉”：档案给研究者一个精确到秒的数字，看起来比口述史可靠得多，但它可能只是某个数据库字段的渲染，不足以证明现实事件恰好在那个物理秒发生。

---

## 18. A/B/C/D evidence map

| Claim | Evidence | Grade | Confidence | Boundary |
|---|---|---:|---:|---|
| 117 是公众报时接口 | 2003 新华社 | B | high | 不外推拨打率 |
| 2001 time.ac.cn 提供网络授时 | NTSC 2009 机构史 | C/A boundary | high | 页面形态未验证 |
| 2004-05-01 时间精灵发布 | 2005 CAS 同期机构材料 | A/B | high | 实际独立用户不明 |
| 2009 闰秒同步影响 Internet/电话/时间戳 | NTSC/CAS 同期材料 | A | high | 不等于所有终端成功同步 |
| timestamp 服务闰秒期间暂停 | 官方公告存档 | A | high | 只证明该服务政策 |
| 2009 用户守候秒杀、秒杀器替人等待 | 钱江晚报 | B | high | 不证明淘宝 server implementation |
| time.ac.cn 2013 BPL Wayback locator | third-party locator | candidate only | low-medium | replay 未取到 |
| PC clock / server / DB / browser time 必须拆开 | researcher model | D | high | method model, not historical claim |

---

## 19. 反例与后见之明风险

### 19.1 不要把今天自动同步的手机经验投回 2001

今天用户通常不主动“对表”，会让研究者误以为 PC/手机时间天然就准。

早期环境里需要考虑：

- CMOS/RTC 漂移；
- Windows Time 是否启用；
- dial-up/offline；
- proxy/firewall；
- 手动修改；
- 时间软件权限；
- timezone 设置错误；
- 网络服务不可用。

### 19.2 不要从标准服务存在推出普通人关心毫秒

2004 普通用户可能只需要让电脑不要差几分钟；证券、电信等行业才可能需要更高精度。

“毫秒级抢购”是后来的平台稀缺事务把这种精度需求向普通消费者下沉。

### 19.3 不要把同步精度写成事务公平

即使双方都同步到同一标准时间：

```text
client network delay
server queue
CAPTCHA
bot traffic
DB locks
inventory policy
```

仍然会造成不同结果。

---

## 20. 下一步可以怎样推进

优先级：

### P0 — verified historical capture

真正取得并记录 `time.ac.cn` 2001–2005 的 memento：

- homepage；
- standard time display；
- download page；
- 时间精灵页面；
- sunriseset page。

### P1 — original software artifact

合法可得时定位：

- CSAOtime；
- 时间精灵；
- version / binary hash / OS requirements；
- network endpoint/protocol。

只登记元数据与研究结果，版权不明时不重新分发二进制。

### P2 — transaction clock case

选一个 2009–2012 的限时事务，寻找：

- official rule；
- archived HTML/JS；
- user report；
- server-side implementation evidence；
- failure/late-request evidence。

不要只凭宣传页复原服务器状态。

### P3 — timestamp provenance audit

抽取旧网中同一内容的：

- current live legacy page；
- archive capture；
- search index snippet；
- repost；

比较 timestamp/timezone/rendering，建立“时间戳也需要 provenance”的完整案例。

---

## 21. 本轮改变了什么

中文旧网通常被写成“人获得了更多页面、信息和账号”。本 note 补了一层更底的基础设施：

> **这些页面和事务还必须共享一个足够一致的“现在”。**

网络时间最初看起来只是让 Windows 右下角不再慢几分钟；可一旦报名、购票、支付和秒杀开始围绕精确截止时刻执行，时钟就从背景设置变成制度接口。

因此 old-Web 以后遇到任何精确日期/时间事务，都应追加一个问题：

> **这个时间是谁的时间？用户本地钟、浏览器显示、服务器判断、数据库写入和 archive 保存的时间，是否真的是同一个状态？**

如果答不出来，页面上再精确的 `20:00:00` 也不能自动升级成现实世界的 `20:00:00`。