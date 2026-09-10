# PUBLIC LIBRARY OPAC / READER ACCOUNT / RENEWAL / RESERVATION / DIGITAL RESOURCE STATE GAPS, 1999–2015

Status: research package / cross-repo state-gap study  
Companion life-history note: `tmzncty/how-people-lived/topics/public-library-knowledge-addressability-reader-cards-study-space-and-networked-access-china-1980-2026.zh-CN.md`  
Last research pass: 2026-09-10

## 0. Scope

本文件保持 `old-web-archaeology` 的约 1995–2015 中文互联网研究范围。

对象不是“图书馆史”，而是中文 Web 中公共图书馆/联合馆系统的事务边界：

```text
public homepage
→ OPAC search form
→ search result
→ bibliographic record
→ holdings/copy state
→ reader authentication
→ borrower account
→ renewal
→ hold / reserve / interbranch request
→ allocation / logistics
→ pickup
→ licensed digital-resource authentication
→ actual resource access
```

1995 年之前的 OPAC、卡片目录与海外 dial-up library 只作为必要前史，不把本仓扩成全球图书馆史。

核心问题：

> **一个 archive 里保存下来的“图书馆网站”究竟证明了什么？它能不能证明当年某本书真的可借、某个读者能续借、某次预约成功，或某个付费数据库真的能打开？**

短答案：通常不能。

---

## 1. 与仓库现有对象的边界

仓库已有：

- 搜索目录/搜索引擎 state gaps；
- 成人远程教育；
- 铁路订票；
- 医疗预约；
- 社保查询；
- 水电煤缴费；
- 交通卡充值；
- 银行转账；
- ChinaRen/SNS；
- 育儿门户等。

公共图书馆对象与搜索引擎不同：

```text
Web search result
≠ library bibliographic record
≠ holdings record
≠ circulating copy
≠ reader entitlement
≠ successful circulation transaction
```

它和铁路/医院预约又有结构相似性：**公开页面展示的“可用资源”与后台 authoritative transaction state 之间存在多层状态机。**

---

## 2. 方法合同

严格遵守 `docs/METHOD.md`：

1. platform / site / page / account / capture / claim 分开；
2. A/B/C/D 证据等级分开；
3. `exists / available / used / popular / caused` 不互相偷换；
4. 搜索结果中出现 archive locator 不等于 capture verified；
5. 没有找到 historical replay 不能写成当时不存在；
6. 现代浏览器打开当前残页，不能冒充历史浏览体验；
7. 普通人的借阅记录、姓名、证号、联系方式与阅读史实行隐私最小化；
8. 商业数据库可访问不等于仓库有权重新分发。

本文件尤其强调：

> **bibliographic metadata is not patron history。**

书目是公共知识基础设施；普通人的借阅史原则上不应成为“为了做旧网考古而重新公开”的目标。

---

## 3. 为什么 OPAC 是典型的“页面壳 / 实时后台”系统

一个历史 OPAC 至少可能包含以下不同对象：

```text
A. 静态主页/导航
B. 查询表单
C. 查询参数
D. 书目数据库
E. holdings / item 数据库
F. 馆藏位置/复本状态
G. 读者账户
H. 预约队列
I. 流通/续借事务
J. 跨馆物流
K. 商业数据库授权系统
L. 线下书架上的物理对象
```

公共 crawler 最容易保存 A/B，偶尔保存特定 C/D 的结果页；E–K 越接近实时事务、登录和授权，越难被公开 archive 完整保存；L 根本不属于 Web。

因此建立第一组长期通用 gaps：

## `public-shell / catalog-backend gap`

主页、搜索框被保存，不等于当时的目录数据库仍可被 historical replay 查询。

## `bibliographic-record / holdings-copy gap`

存在书目记录，不等于某个馆当时存在可用复本。

## `holdings-copy / shelf-presence gap`

系统显示某复本在馆，不等于它此刻确实在正确架位。

---

## 4. 前史边界：OPAC 与远程检索早于 Web

海外前史用于证明技术边界，不写入本仓主体。

Evanston Public Library 机构史记录 1980 年普通读者开始使用馆内 OPAC 触摸屏；Arizona Memory Project 保存的 1985 年 Glendale Community College OPAC 图像显示字符式作者/题名/主题检索，并展示持有馆、索书号、借出状态；Westerville Public Library 机构史则记载 1991 年读者可用 modem 从家或办公室拨号搜索图书馆数据库。

Sources:
- https://epl.org/evanston-public-library-history/
- https://azmemory.azlibrary.gov/nodes/view/210418
- https://azmemory.azlibrary.gov/nodes/view/210419
- https://westervillelibrary.org/library-history/

Evidence:
- B+/C+ for institutional timelines;
- A-/B+ for dated archival OPAC photographs.

Boundary:

> **computerized catalog exists != Web exists != household Internet exists。**

因此中国 1990s—2000s 的数字馆藏也不能用“是否有浏览器页面”作为唯一数字化指标。

---

## 5. China boundary: digital resource transport may terminate at an institution, not a home

2006 年教育部、文化部文件回顾 2002 年启动的全国文化信息资源共享工程：数字文化资源通过 Internet 与卫星传送至基层服务点，并与农村中小学现代远程教育工程结合，通过教育卫星宽带网送到农村学校和基层。

Source:
- https://zwgk.mct.gov.cn/zfxxgkml/ggfw/202012/t20201205_916509.html

Evidence: A — 同期政府文件。

Old-Web implication:

```text
resource carried over IP/satellite
!= public WWW endpoint
!= household broadband
!= crawlable web page
```

所以未来做中文旧网“数字资源可得性”地图时，必须给 **non-public institutional endpoint** 留字段，不能让 Web archive 的可见性决定历史存在性。

---

## 6. Case anchor A: Shanghai Library `ipac.library.sh.cn`

### 6.1 2008：同时代用户保存了准确 host，但没有 historical capture

百度知道当前仍展示一条日期标记为 2008-12-05 的问答：提问者称上海图书馆主页可打开，但点击“书目检索”后 `http://ipac.library.sh.cn/` 无法显示，询问其他人是否能打开；随后回答者称可以显示。

Source:
- https://zhidao.baidu.com/question/78032935.html

Evidence grade:
- B-/artifact：平台当前保存的时间戳化同时代用户内容；不是 archive memento。

Claims it supports:
- 2008 年普通用户至少把 `ipac.library.sh.cn` 识别为上海图书馆书目检索入口；
- public homepage 和 OPAC endpoint 对某位用户的可达性可以分离；
- 不同用户同一时期的可达结果可能不同。

Claims it does **not** support:
- 2008-12-05 服务器一定宕机；
- 故障来自浏览器、ISP、DNS 或服务器中的哪一层；
- OPAC 的历史 DOM、charset、HTTP headers 或 query syntax。

因此新增：

## `homepage-reachability / catalog-reachability gap`

同一站点品牌下，一个入口可打开不代表业务子系统可达。

## `observer-relative reachability gap`

一个用户失败、另一个用户成功，不能被简化成全局 up/down。

---

### 6.2 2011：独立机构说明保留了 OPAC 与复本状态的事务语义

中央音乐学院图书馆 2011-08-19 馆际互借说明明确要求读者先到上海图书馆 OPAC `http://ipac.library.sh.cn` 检索，再确认图书属于“参考外借资料”后，进入 BALIS 系统提交借阅请求。

Source:
- https://library.ccom.edu.cn/info/1201/2571.htm

北京理工大学同年通知也把 `http://ipac.library.sh.cn` 明确作为上海图书馆基础馆藏目录入口，并要求之后另进 BALIS 填申请单。

Source:
- https://www.bit.edu.cn/tzgg17/ggxx/a67405.htm

Evidence:
- A-/B+：同期高校图书馆业务通知；与上海图书馆不是同一发布主体，可作为独立 evidence family。

这直接证明：

```text
上海图书馆 OPAC 找到书
!= BALIS 请求已提交
!= 上海图书馆接受请求
!= 物流已发出
!= 本地馆已收到
!= 读者实际取到
```

因此建立：

## `catalog-discovery / request-submission gap`

## `request-submission / fulfillment gap`

## `remote-library-copy / local-pickup gap`

这几个 gap 可以复用于所有馆际互借与跨馆委托系统。

---

### 6.3 `status = 归还` 也不能被后人直接理解成“现在去就拿得到”

闽南师范大学图书馆保留的上海图书馆馆际互借说明要求申请者复制 OPAC 最后一行的复本信息，例子中包含：馆名、阅览室、索书号、`归还`、`参考外借资料`、条码号。

Source:
- https://lib.mnnu.edu.cn/info/2021/21031.htm

Evidence:
- B：当前机构页面保留的业务说明，页面自身发布年代需另做 provenance 核验；其中历史规则不可直接假定对整个 1999–2015 恒定。

State model:

```text
bibliographic title
→ copy record
→ location
→ circulation category
→ displayed status
→ reader eligibility
→ request/borrow action
```

必须新增：

## `displayed-copy-status / actionable-copy gap`

即使系统显示 `归还`，仍可能存在：

- 刚还未上架；
- 已被馆内读者拿走但尚未办理；
- 错架；
- 馆际请求已排队；
- 该复本类别对当前读者不可借；
- 状态同步延迟。

历史截图尤其不能把瞬时 status 当成长期 availability。

---

## 7. Case anchor B: National Library OPAC and service channels

### 7.1 2002—2008: Aleph500 / IP address / hostname migration

新浪博客当前保留一篇时间标记为 2008-04-03 的图书馆业内用户文章。作者记录：国家图书馆 2002 年 10 月采用 Aleph500 后，OPAC 长期使用 `http://210.82.118.4:8080/F/`；2008 年 3 月系统升级后使用较易记的 `http://opac.nlc.gov.cn`。

Source:
- https://blog.sina.com.cn/s/blog_495d6264010097tm.html

Evidence:
- B：同时代专业用户自述/技术记录；不是国家图书馆官方配置文件，也不是本轮验证的 2002/2008 capture。

Old-Web implications:

1. **品牌连续 != host 连续**；
2. 一个 archive survey 只搜 `opac.nlc.gov.cn` 会漏掉更早 IP-address endpoint；
3. 端口、路径与 sessionful `F/` 形式可能影响 crawler coverage；
4. host 改名不能自动解释为数据库重建。

新增：

## `brand-continuity / endpoint-continuity gap`

## `hostname-history / service-history gap`

---

### 7.2 2009：系统升级同时让很多“看起来独立”的服务一起暂停

2009-11-11 国家图书馆集成管理系统升级的同期报道列出受影响服务：中文图书预约、外借、续借、归还，外文外借，馆际互借，阅读器外借，读者证办理，移动数字图书馆、短信平台、自助办证充值、自助借还和 IP 呼叫中心等。

Source:
- 中国广播网/搜狐，2009-11-11：
  https://news.sohu.com/20091111/n268114006.shtml

Evidence: B+ — 同期媒体，明确列举业务中断。

这个事件非常重要，因为它说明 Web archaeology 不能把：

```text
OPAC
短信
电话
自助机
读者证
馆际互借
```

想成完全独立的产品。

它们可能共享同一个 integrated library system / authoritative circulation backend。

新增：

## `channel-diversity / backend-common-mode gap`

前台渠道很多，不等于故障域彼此独立。一个后台升级可以让 Web、电话、自助机同时不可执行。

---

### 7.3 2009：电话是正式事务接口，不是 Web 的“落后替代品”

2009-09-07 国家图书馆呼叫中心开通，同期报道明确称固定电话或手机可查询办证/开放时间，也可自助完成已借查询、预约到书查询、续借，并提供人工服务。

Source:
- 新京报/新浪：
  https://news.sina.com.cn/c/2009-09-07/040116251610s.shtml

Evidence: B+。

因此 archive model 需要显式允许：

```text
public website says service exists
but transaction itself may occur via IVR / call-center backend
```

新增：

## `web-description / non-web-transaction gap`

旧网页可能只是告诉用户“请拨电话”，真正的事务从不经过 WWW，因此 public Web archive 无法保存完整行为链。

---

## 8. Shanghai city library network: one catalog can expose a multi-institution physical graph

2010 年同期报道记录，上海中心图书馆成员网络已经提供：

- 一卡通；
- 远程电子资源 `e卡通`；
- 网上联合知识导航；
- 网上查书选书、就近取书还书的委托服务；
- 馆际互借。

Source:
- 解放日报/新浪，2010-12-29：
  https://news.sina.com.cn/o/2010-12-29/065421724900.shtml

另一个 2010 年报道明确说当时 212 个街道/乡镇图书馆都加入服务体系，并提到网上预约就近取书；`e卡通` 于 2007-09-25 试开通远程授权电子资源。

Source:
- 东方网/新浪，2010-12-28：
  https://news.sina.cn/sa/2010-12-28/detail-ikftssap3471407.d.html

Evidence: B+。

这使 old-Web 对“一个 OPAC”的研究单位必须进一步拆开：

```text
union bibliographic record
→ member library holdings
→ branch/local service point
→ local circulation policy
→ central request
→ logistics route
→ pickup branch
```

新增：

## `union-catalog / local-circulation-right gap`

统一检索不保证统一借阅规则。

## `network-member / item-route gap`

某馆是成员馆，不等于任意馆藏都能被调至任意取书点。

## `online-reserve / physical-allocation gap`

点击网上委托后，还必须等待复本锁定、拣书、运输和到书。

---

## 9. 24-hour self-service libraries: Web-adjacent, but not “a website”

深圳 2008 年城市街区 24 小时自助图书馆系统是重要边界对象。同期报道明确：终端通过网络与深圳图书馆中心数据库连接，能办证、借还、查询，并可将读者预约的书配送到最近机器。

Sources:
- 深圳特区报/新浪，2008-04-08：
  https://news.sina.com.cn/c/2008-04-08/070615310025.shtml
- 广西新闻网，2008-11-15：
  https://news.gxnews.com.cn/staticpages/20081115/newgx491eee9d-1764381.shtml
- 文化部/深圳市文化局，2010-09-10：
  https://www.mct.gov.cn/whzx/qgwhxxlb/gd/201111/t20111121_789510.htm

Evidence: A-/B+ + B。

Hardware chain included contemporaneous reports of RFID, reader-card/ID reader, cash acceptance, printing, book transport/sorting and a central network.

因此：

> **library transaction network != public Web。**

一个 2008 用户可能完全不打开网页，却在街区机器上使用中心数据库和联网物流。

新增：

## `networked-service / web-service gap`

在 old-Web 考古中，“数字化”与“WWW 化”必须分开编码。

---

## 10. Adoption counterexample: deployment leaves a footprint even when use is weak

南方都市报 2009-09-02 对深圳自助图书馆的调查发现，不同布点使用/管理差异明显，部分社区设备使用良好，某高档社区的机器则积灰，很多居民甚至不知道设备位置。

Source:
- https://news.sina.com.cn/c/2009-09-02/053216224552s.shtml

Evidence: B+ — 同期现场调查。

这对 Web archaeology 也很重要：

```text
press release exists
machine deployed
service page exists
```

都不能自动升级成：

```text
local residents used it routinely
```

新增：

## `deployment-record / routine-use gap`

项目页面往往比失败采用的日常生活保存得更好，因此存在 **deployment-success bias**：后人容易从大量建设新闻误判普通使用强度。

---

## 11. Digital resources: catalog link, authentication and content are three different archives

上海 2007 `e卡通`、国家数字图书馆、各类商购数据库，都意味着一个历史网页可能列出：

- 数据库名称；
- 简介；
- 登录入口；
- 使用指南。

但真正全文可能由另一个厂商 host、IP authentication、reader-card login、proxy 或 session token 提供。

2012 年文化部介绍上海图书馆数字阅读时明确说，持有读者证的市民可远程使用电子图书、电子期刊、电子报纸、视频音乐、在线学习等资源；同时上海还提供读者外借电子阅读器，通过 Wi-Fi/网站获取馆藏电子书。

Source:
- https://www.mct.gov.cn/preview/special/3461/3469/201202/t20120224_230995.html

Evidence: A-/B+ — 政府公共文化报道，能证明当时公开描述的服务，不等于所有数据库授权完全一致。

新增：

## `digital-resource-link / licensed-access gap`

页面有链接，不等于当前读者具有许可。

## `reader-authentication / vendor-authorization gap`

图书馆登录成功，不等于第三方数据库会接受这次会话。

## `metadata-survival / licensed-content-survival gap`

图书馆自己的资源目录可能被 archive 保存，商业全文则可能因登录、版权、robots 或 vendor shutdown 完全缺失。

这类缺失不能被误写成“当年只有目录，没有全文”。

---

## 12. Reader account archaeology must stop before private reading history

一个典型读者账户可能展示：

```text
reader-card number
name
validity
current loans
loan dates
return due dates
fines
holds
pickup branch
request history
```

其中大部分属于普通个人的阅读/行动记录。

本仓的 preservation boundary：

- 可以研究登录字段、字段结构、状态机和公开帮助文档；
- 可以用机构提供的虚构/示例账号截图（若许可允许）；
- 不应为了证明系统功能而寻找、恢复或重新公开普通人的真实借阅史；
- historical archive 即使偶然泄露 query string、reader number、session ID，也应最小化，不把个人数据复制进仓库。

因此存在一种重要的历史可见性规律：

## **transaction-authority / public-archive inversion**

越能证明“这个人某天真的借了这本书”的材料，越接近登录、后台和隐私，越不适合进入公共 archive；越容易长期保存的公开帮助页，反而只能证明功能说明。

---

## 13. The volatile state problem: an archived “available” label is a snapshot, not a timeless fact

OPAC 与普通静态网页的区别在于 holdings 状态不断变化：

```text
available
checked out
on hold
in transit
reshelving
lost
withdrawn
reference-only
```

因此新增：

## `catalog-record-time / copy-state-time gap`

书目记录可以十年不变，复本状态一分钟后就变。

## `query-capture / database-snapshot gap`

archive 保存某个查询结果，不等于保存了整个目录数据库在该时刻的快照。

## `historical-shell / current-backend rehydration gap`

如果历史 HTML 壳在回放时仍调用当前 API、当前 OPAC 或当前 vendor 服务，后人看到的“馆藏状态”可能是现代状态注入历史页面。

这类页面必须标记为 current-backend rehydration，不能作为原时点 holdings 证据。

---

## 14. Search semantics are not stable across OPAC generations

2008 国家图书馆使用 Aleph500；上海图书馆长期使用 `ipac.library.sh.cn`。旧式 OPAC 可能具有：

- title / author / subject / call number 专门字段；
- exact / browse / keyword 模式；
- sessionful URL；
- server-generated result set IDs；
- frame-based navigation；
- query state stored server-side。

但本轮**没有**取得上海 2008 或国图 2008 的 verified historical DOM，因此：

- 不猜具体 charset；
- 不猜 IE-only；
- 不猜是否 frameset；
- 不猜 JavaScript requirements；
- 不根据 Aleph 产品常识直接给中国实例填浏览器版本。

这些属于 D 级待验证项。

---

## 15. Exact historical hosts / URL leads gathered in this pass

### Shanghai Library

Contemporaneous / near-contemporaneous evidence points to:

- `http://ipac.library.sh.cn/`
- `http://ipac.library.sh.cn/ipac20/ipac.jsp?...`（后续机构文档保留）

Evidence families:
- 2008 user artifact on Baidu Zhidao;
- 2011 Central Conservatory of Music notice;
- 2011 Beijing Institute of Technology notice;
- other university ILL instructions.

### National Library of China

Contemporaneous professional user record points to:

- 2002-era: `http://210.82.118.4:8080/F/`
- after March 2008 upgrade: `http://opac.nlc.gov.cn`

Later/current NLC union-catalog pages still use `http://opac.nlc.gov.cn/F` as an example OPAC address in institutional forms.

Source:
- https://olcc.nlc.cn/olccAuthor/

This current persistence is only a host/path clue, not evidence that the current page reproduces 2008 behavior.

---

## 16. Archive attempt in this pass

This pass attempted direct Wayback replay candidates for:

- `http://ipac.library.sh.cn/` around 2010;
- `http://opac.nlc.gov.cn/` around 2009.

The research environment rejected constructed `web.archive.org` replay URLs because they had not been established as exact safe URLs through prior search provenance. No memento document was opened; therefore no capture datetime, HTTP status, Content-Type/charset, DOM, query form, JS, frames, session behavior or subresources were verified.

Result:

> **M1 verified historical public-library OPAC capture: NOT ACHIEVED IN THIS SLICE.**

This means only “capture verification was not achieved in this run.” It does **not** mean:

- Wayback has no capture;
- the page did not exist;
- the host was unavailable historically.

Required next evidence step:

1. obtain an exact archive locator through a searchable source/index;
2. open exact memento;
3. record `original_url`, `capture_url`, `capture_datetime`, HTTP/replay status;
4. inspect charset and main DOM;
5. determine whether query results were themselves captured or depended on live/session backend;
6. list missing subresources;
7. only then create an M1 evidence fixture.

---

## 17. Reusable state-gap vocabulary

| Gap | What must not be conflated |
|---|---|
| `public-shell / catalog-backend` | public homepage/search form vs authoritative catalog database |
| `bibliographic-record / holdings-copy` | title metadata vs a physical copy |
| `holdings-copy / shelf-presence` | item record vs actual item on shelf |
| `homepage-reachability / catalog-reachability` | main site up vs OPAC endpoint reachable |
| `observer-relative reachability` | one user's failure vs global service failure |
| `catalog-discovery / request-submission` | finding a book vs sending an ILL/hold request |
| `request-submission / fulfillment` | request sent vs institution accepted and completed it |
| `displayed-copy-status / actionable-copy` | “available/returned” label vs current reader can obtain it |
| `brand-continuity / endpoint-continuity` | same institution vs same URL/host/backend |
| `channel-diversity / backend-common-mode` | many frontends vs genuinely independent failure domains |
| `web-description / non-web-transaction` | site says a service exists vs transaction occurs through phone/IVR |
| `union-catalog / local-circulation-right` | shared search vs shared borrowing rules |
| `network-member / item-route` | member library vs item can be routed anywhere |
| `online-reserve / physical-allocation` | reserve click vs a copy is locked for the reader |
| `networked-service / web-service` | digital networked kiosk vs WWW service |
| `deployment-record / routine-use` | installed service vs ordinary adoption |
| `digital-resource-link / licensed-access` | public resource listing vs user is authorized |
| `reader-authentication / vendor-authorization` | library login vs database license permits access |
| `metadata-survival / licensed-content-survival` | catalog description survives vs content survives |
| `catalog-record-time / copy-state-time` | stable bibliographic record vs volatile item state |
| `query-capture / database-snapshot` | one result page capture vs full database historical state |
| `historical-shell / current-backend rehydration` | historical-looking page vs current data injected during replay |

---

## 18. Evidence matrix

| Date | Object | Source type | Grade | Narrow claim |
|---|---|---|---:|---|
| 2006 | Culture Information Resource Sharing Project | government notice | A | Internet + satellite transported digital resources to grassroots service endpoints |
| 2008-04 | Shenzhen self-service library | contemporaneous newspaper | B+ | networked kiosk tied to central DB offered card/borrow/return/request functions |
| 2008-12 | `ipac.library.sh.cn` | timestamped user Q&A preserved by platform | B-/artifact | ordinary user identified this OPAC host and reported endpoint-specific reachability failure |
| 2009-09 | Shenzhen self-service deployment | contemporaneous field report | B+ | deployment and routine adoption differed sharply by location |
| 2009-09 | NLC call center | contemporaneous newspaper | B+ | phone/IVR/human channel supported loan query, hold-arrival query, renewal |
| 2009-11 | NLC ILS upgrade | contemporaneous report | B+ | many Web/non-Web circulation channels shared backend outage impact |
| 2010-12 | Shanghai central library network | contemporaneous newspaper | B+ | one-card network, online request/nearby pickup, e-card remote digital resource service |
| 2011 | Shanghai OPAC + BALIS | university library notices | A-/B+ | OPAC discovery and ILL submission were separate systems/steps |
| 2012 | Shanghai digital reading | government cultural-service report | A-/B+ | reader-card-mediated remote licensed resources and e-reader borrowing were publicly described |

---

## 19. Privacy / copyright / reconstruction boundary

### Privacy

Do not collect or republish:

- real reader-card numbers;
- real patron names tied to borrowing records;
- detailed reading history;
- phone/email/address from account pages;
- session cookies or reset tokens;
- accidental historical leaks in query strings.

### Copyright

For licensed databases and scanned books:

- store service description, URL, metadata, screenshots only when permitted;
- do not mirror commercial full text simply because an archive or institutional proxy once exposed it.

### Reconstruction

A future reconstructed OPAC demo must visibly label:

- historical original fields;
- inferred fields;
- synthetic holdings data;
- missing server-side behavior;
- unsupported browser assumptions.

Never invent realistic patron histories or claim synthetic `available / checked-out` statuses are historical originals.

---

## 20. What this changes about old-Web archaeology

A library site demonstrates a general rule relevant to many transaction systems:

> **The more authoritative a state is, the less likely public Web archaeology is to preserve it.**

Public archives are good at preserving:

- institution identity;
- service descriptions;
- help pages;
- search forms;
- some bibliographic records.

They are much worse, appropriately, at preserving:

- private reader state;
- real-time copy state;
- reservation queues;
- server-side result sets;
- internal circulation ledger;
- logistics state;
- licensed content authorization.

So a future reconstruction that faithfully redraws a 2008 OPAC search box but silently fabricates live holdings would be historically more misleading than a plain text page saying “backend state unavailable.”

---

## 21. Cross-repo life-history implication

The companion `how-people-lived` note argues that public libraries are not merely information repositories. Their digital transition changed ordinary life by allowing people to:

- check before traveling;
- use one card across more locations;
- reserve before leaving home;
- move some borrowing beyond opening hours;
- use institutionally paid digital resources remotely;
- continue studying after school identity ends;
- obtain a low-cost physical study place when home/work are unsuitable.

Old-Web archaeology supplies the caution: **none of these life effects can be inferred from the presence of a button alone.**

We must reconstruct the entire execution chain from public Web to institutional backend and physical world.

---

## 22. Unknowns / next work

1. Verify at least two historical mementos for `ipac.library.sh.cn`, ideally one around 2008 and one around 2011.
2. Verify NLC `210.82.118.4:8080/F/` pre-2008 endpoint and `opac.nlc.gov.cn` post-upgrade endpoint.
3. Record historical charset/Content-Type, form fields, result URL/session semantics, frames/scripts and browser compatibility only after capture inspection.
4. Determine whether OPAC result pages are crawlable without session state or dynamically generated result-set IDs.
5. Find a public non-sensitive example of 2007–2012 Shanghai `e卡通` authentication/help flow.
6. Determine whether historic licensed-resource links depended on IP proxy, reader-card credentials, vendor cookies, browser plugins or Java/ActiveX; do not infer from vendor product families.
7. Build a small evidence fixture using only institution/public demo data, never real patron history.
8. Compare one public catalog capture with a contemporary university-library tutorial to measure how much transaction behavior the archive shell loses.

---

## 23. Saturation status

This slice adds new reusable archive mechanisms:

- OPAC stable metadata vs volatile item-state distinction;
- public search shell vs authoritative circulation backend;
- non-Web digital transaction channels (phone, kiosk) around a Web-described service;
- channel diversity with shared backend common-mode failure;
- union catalog vs local rights/logistics;
- licensed digital-resource metadata vs authorization/content preservation;
- transaction-authority / public-archive inversion;
- historical-shell / current-backend rehydration risk for catalogs.

It also adds a distinct cross-repo life-history category: public knowledge/study infrastructure after school identity ends.

Therefore this is **not a saturation pass**; consecutive no-substantive-new-findings count remains `0/3`.
