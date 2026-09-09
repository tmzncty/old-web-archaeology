# WEB_MAP_POI_ROUTE_QUERY_TRANSIT_DIRECTIONS_TILE_AND_NAVIGATION_STATE_GAPS_1999_2015

> Status: research note / cross-repo companion
>
> Scope: 中文 Web / Web-adjacent 电子地图、POI、公交/驾车路线、实景、打印路条、地图共享与早期移动导航，约 1999—2015
>
> Date: 2026-09-09
>
> Cross-repo life-history note: `tmzncty/how-people-lived/topics/from-asking-directions-to-live-navigation-route-executability-and-spatial-legibility-china-1979-2026.zh-CN.md`

## 0. 研究问题

本稿不是“中国电子地图产品史”，也不把全球 GIS/GPS 历史扩进本仓库。

它只研究一个 old-Web archaeology state gap：

> **当一个历史中文网页上出现地图、地点、公交查询或驾车路线以后，我们还需要哪些证据，才能证明当时的用户真的能把一个起点和终点提交给 route engine，得到与那个时点的数据相符的路线，并把它打印、记住、分享或实际用于出行？**

地图类旧网页尤其容易制造“看起来已经完整保存”的假象。

一个 archive replay 可能仍然显示：

- logo；
- 搜索框；
- “公交”“驾车”tab；
- 某个地点名称；
- 一张地图底图；

但真正决定历史行为的后端可能早已不存在：

```text
address query
→ geocoder
→ POI database
→ route graph
→ transit timetable/line database
→ route engine
→ tile/image service
→ browser JS
→ route-result renderer
```

因此必须坚持：

```text
map shell captured
!= map tiles captured
!= POI database captured
!= historical geocoder still callable
!= route engine captured
!= historical route result reproducible
!= route was correct in the street
!= user actually reached destination
```

---

## 1. Scope boundary

### 1.1 本仓主对象仍是约 1995—2015 中文互联网

主体研究：

- 1999—2015 中文在线地图入口；
- `mapbar.com`、`mapabc.com`、`668map.com`、`city8.com`、有道地图等公开 Web 形态；
- POI/address query；
- 公交换乘与驾车路线；
- route result / print view；
- 360° 实景；
- 地图共享、标注、embed/API；
- Web→desktop/mobile handoff；
- tile/image/JS/charset/browser dependency；
- historical capture 的 state gap。

### 1.2 1999 以前中国地图前史只用于解释边界

前互联网纸图、1980s “活地图”、1990s 交通指示图、CD-ROM GIS 主要写入 `how-people-lived`。

只有当它们直接解释中文 Web 地图为什么采用某种交互时，才在本稿引用。

### 1.3 全球 MapQuest / Google Maps 主要留在 how-people-lived

MapQuest printable directions、Google 2009 connected navigation 可用于证明“静态 route document → live route service”是跨国共同变化，但不是本仓主体。

---

## 2. 与仓库方法合同的对应

依据 `docs/METHOD.md`，必须把以下层级分开：

```text
platform
site / host
page / URL
query instance
route result
capture / memento
claim
```

地图还必须再加一层 **dataset version**，因为同一 URL 在不同日期可能由完全不同的 POI/道路/公交数据库生成结果。

不能写：

> “2008 年 Mapbar 页面现在能打开，所以 2008 年路线还能复原。”

应该拆成：

1. 2008 年该 host/产品是否存在；
2. 当时 route UI 是否存在；
3. original query syntax 是否可确定；
4. 当时 geocoder/route backend 是否可确定；
5. archive 是否保存一次具体 route response；
6. response 使用的道路/公交数据版本是否可确定；
7. 当时浏览器环境能否正确呈现；
8. 该路线在现实世界是否可执行。

并继续区分：

```text
exists
available
used
popular
caused
```

---

## 3. 已确认的历史主体与同时代证据

### 3.1 `www.mapbar.com` / Mapbar：2006 route query 功能存在

2006-07-20 新浪科技同期报道 Mapbar 发布 264KB、无需安装注册的“小Me”桌面地图查询工具，明确说可查询公交线路、驾车路线和其他地图信息。

来源：

- https://tech.sina.com.cn/other/2006-07-20/15061047598.shtml
- grade: B（同期媒体/产品信息）

可证明：

- Mapbar 品牌/服务在 2006 年存在；
- route query 已经是明确产品能力；
- Web map 正在向 desktop shortcut/client 延伸。

不可证明：

- 当时每个城市都有同等 route coverage；
- 具体一次 route backend 如何计算；
- 用户规模；
- 今天访问 Mapbar 得到的路线等于 2006 路线。

### 3.2 `www.mapbar.com`、`www.mapabc.com`、`www.668map.com`、`www.8684.cn`、`www.city8.com`：2008 用户侧 hostname 组合

2008-04-24，一名博客园用户公开写下实际使用链：最早 668map，后来常用 Mapbar 和 Mapabc，公交更新则认为 8684 更快；当天查询北京酒仙桥时发现 City8 的 360° 实景。

来源：

- https://www.cnblogs.com/Kymo/archive/2008/04/24/1170077.html
- grade: A（同期公开用户材料）

这条材料非常适合做 old-Web hostname/provenance 证据，因为它来自产品之外，且同一时点把多个服务放进真实工作流。

它支持：

```text
one user
→ multiple map hosts
→ different data strengths
→ cross-check before travel
```

但不支持：

> “2008 年普通中国网民普遍同时使用五个地图站。”

### 3.3 2008 行业侧：地图服务已经竞争 POI、实时路况、实景和 API

2008-04-10《信息周刊》/泰伯网引用 iResearch 2007 报告，列 Mapbar、Mapabc、51ditu、搜狗/Go2Map 为当时主要在线地图竞争者，并讨论 POI、360° 实景、实时路况、开放 API 与无线导航。

来源：

- https://www.taibo.cn/p/4670
- grade: B

其中访问份额、市场规模、POI 数量含咨询机构或厂商口径，只能作为行业结构线索；不能直接升级为人口层面的 popular claim。

### 3.4 2008 有道地图：中文自然语言式起终点查询仍在被改进

2008-09-01 网易发布有道地图测试版的同期公司稿，称收录 400 多城市地图、近 100 城公交，并强调降低传统地图搜索中“先指定公交站点”的交互要求。

来源：

- https://www.prnasia.com/story/13413-1.shtml
- grade: A/B（同期企业公告）

它可以证明当时 route UX 的一个真实问题：

> 用户通常知道“我从某个地方去另一个地方”，却未必知道系统要求的规范站名、地址或 route-node 名称。

因此 geocoder / place resolution 本身就是 route transaction 的前置状态。

### 3.5 2009 MSN 地图共享：route/map 已进入 IM 协作场景

2009-05-06 中关村在线实测 Windows Live Messenger 的地图即时共享功能：聊天双方可在同一张地图上搜索、浏览、标注，并看到对方操作。作者同时自述去陌生地方前会先上网查图，但仍可能到现场找不到。

来源：

- https://soft.zol.com.cn/131/1319968_all.html
- grade: B/A（同期产品实测 + 作者第一人称）

这证明 map state 已经不只属于一个独立页面，还可以成为：

```text
IM conversation
→ shared map context
→ collaborative POI selection
→ offline meeting
```

这种跨产品 handoff 对 archive 特别脆弱：IM shell、地图 iframe/object、第三方 tile、用户会话与实时协同很可能由不同服务承担。

### 3.6 2011—2012：公共就业服务也开始地图化

2011 北京在火车站和长途站向来京务工者免费发放“北京市求职地图”，包含公共职介机构、电话、乘车路线、维权与社保信息。

来源：

- https://msn.finance.sina.com.cn/cjyw/20110210/025411055.html
- grade: B

2012 哈尔滨“就业地图”则明确同时提供 Web、公共查询机和有线电视入口，放入 8000 多信息点。

来源：

- https://www.xinhuanet.com/politics/2012-11/28/c_113828487.htm
- grade: B

这类 public-service map 提醒 old-Web 研究不要只盯商业地图首页：地图能力也可能被嵌进就业、政务、医院、旅游等专题站点。

---

## 4. 地图页不是一个对象：最小对象模型

建议以后 `evidence.yaml` / case note 至少把以下对象分开。

### 4.1 Map shell

```text
MAP_SHELL {
  host
  page_url
  page_title
  navigation_tabs
  search_form
  visible_controls
  browser_assumption
  charset
  capture_datetime
}
```

### 4.2 POI record

```text
POI {
  poi_id?
  display_name
  aliases[]
  address_text
  coordinates?
  phone?
  category?
  source?
  valid_time?
}
```

### 4.3 Route query

```text
ROUTE_QUERY {
  origin_text
  destination_text
  origin_resolved_id?
  destination_resolved_id?
  mode
  preferences?
  request_datetime?
}
```

### 4.4 Route result

```text
ROUTE_RESULT {
  route_id?
  ordered_steps[]
  polyline_or_geometry?
  transit_lines[]
  transfers[]
  estimated_distance?
  estimated_duration?
  fare?
  generated_at?
  data_version?
}
```

### 4.5 Rendered map assets

```text
MAP_RENDER {
  base_tiles[]
  marker_assets[]
  route_overlay
  labels
  zoom
  viewport
  client_js
}
```

一个 archive capture 很可能只拥有这些对象中的一部分。

---

## 5. State machine A：POI / 地址查询

```text
RAW USER TEXT
→ REQUEST SUBMITTED
→ NORMALIZED
→ GEOCODER MATCHED / AMBIGUOUS / FAILED
→ POI RESOLVED
→ MAP CENTERED
→ USER RECOGNIZED / REJECTED
```

必须固定：

```text
search box exists
!= query submitted
!= backend responded
!= correct historical POI matched
!= user accepted the match
```

### 5.1 地址并非稳定主键

同一地点会经历：

- 改名；
- 门牌调整；
- 行政区调整；
- 商户倒闭/迁址；
- 旧地名继续口语使用；
- 同名道路/小区；
- 拼音/简繁体/错别字差异。

因此今天输入同一字符串获得一个 POI，不能证明 2008 年 geocoder 也会解析成同一对象。

### 5.2 archive 的 POI temporal drift

历史 HTML 可能保留 2008 页面外壳，却在 replay 时调用：

- 当前地图 API；
- 当前 tile；
- 当前 POI endpoint；
- 已被 archive rewrite 的 query。

于是可能出现：

> **2008 shell + 2026 place state**

这种混合不能称为 2008 historical map state。

---

## 6. State machine B：公交路线

```text
ORIGIN RESOLVED
+ DESTINATION RESOLVED
+ TRANSIT DATA AVAILABLE
→ ROUTE REQUEST
→ CANDIDATE TRANSFERS GENERATED
→ RESULT RANKED
→ USER SELECTS
→ OPTIONAL PRINT/COPY
→ REAL-WORLD TRIP
```

硬边界：

```text
bus line exists in database
!= line ran at queried date/time

route result exists
!= transfer was legal/practical

station name matches
!= station physical position matches

line geometry survives
!= timetable/frequency survives
```

旧 Web route page 往往最容易保留“乘 X 路换 Y 路”的文字结果，却完全不保留：

- 当日首末班；
- 发车间隔；
- 临时改线；
- 票价；
- 站点是否同站换乘；
- 实际步行距离。

因此 route text 只是 **plan representation**，不是完整 mobility state。

---

## 7. State machine C：驾车路线

```text
ORIGIN/DESTINATION RESOLVED
→ ROAD GRAPH LOADED
→ ROUTE COST FUNCTION APPLIED
→ RESULT GENERATED
→ MAP OVERLAY RENDERED
→ OPTIONAL PRINT
→ DRIVER EXECUTES
→ DEVIATION?
```

在早期 Web 地图中，最后一步通常发生在离开电脑以后。

这与后来的 live navigation 不同：

```text
Web route:
request once → static answer → leave computer

live nav:
location updates → route recalculated → instruction updates → repeat
```

因此不能因为 2006 有“驾车路线”，就把它写成今天意义上的实时导航。

---

## 8. State machine D：实景 / panorama

2008 KymoWang 对 City8 360° 实景的同期第一人称证明，实景已经进入用户查地点流程。

但 panorama 需要另外建状态：

```text
POI/coordinate
→ panorama coverage exists
→ panorama index resolves
→ image set loads
→ viewer JS/plugin runs
→ orientation control works
→ user maps image to real street
```

必须区分：

```text
panorama page shell survives
!= panorama image cube survives
!= orientation metadata survives
!= historical capture date of imagery known
```

实景影像还有“双时间”问题：

- page capture datetime；
- street imagery acquisition datetime。

二者不能混成一个日期。

---

## 9. State machine E：打印路条 / route portability

北京数字信息亭到 2004 年已经提供公交查询和“路条打印”的后来报刊数据库记录。

来源：

- 北京日报客户端历史整理：<https://xinwen.bjd.com.cn/content/s67bfa0a8e4b068c68f104f2d.html>
- grade: B/C（回引 2004-06-24 原报）

Web 地图时代，print view 是非常重要却容易被忽略的 artifact：

```text
route generated
→ PRINT VIEW
→ browser print stylesheet
→ physical paper
→ user leaves networked terminal
```

打印页在某种意义上是早期 route state 的 **portable snapshot**。

它可能比动态地图本身更容易进入 archive，因为：

- 文字更多；
- JS 少；
- tile dependency 少；
- URL 有时独立；
- 用户会保存/转发。

以后调查 Mapbar/Mapabc 时应主动寻找：

- `print`；
- `routeprint`；
- `printmap`；
- 静态图片；
- email/share route；
- 纯文字路线。

---

## 10. State machine F：地图共享 / embed / API

```text
SOURCE MAP STATE
→ SHARE ACTION
→ SERIALIZED STATE / URL
→ THIRD-PARTY OR IM HANDOFF
→ RECEIVER OPENS
→ MAP STATE REHYDRATED
```

可能被编码进 URL 的状态包括：

- center；
- zoom；
- POI ID；
- marker；
- start/end；
- route mode；
- token/session id。

硬边界：

```text
share link survives
!= serialized state still decodes
!= backend object still exists
!= receiver sees same historical map
```

2009 MSN map sharing 还增加另一层：

```text
IM session exists
!= map applet/plugin loaded
!= both peers shared same state
```

---

## 11. Tile archaeology：一张“看得见的地图”可能来自很多日期

早期在线地图常由多个静态/动态图块拼成。

一次 replay 可能出现：

```text
main HTML: 2008-04-01
JS: 2008-05-20
northwest tile: 2008-03-12
southeast tile: missing
marker icon: current live server
route overlay: not archived
```

因此需要 **tile temporal mosaic / 图块时间拼贴** 概念。

### 11.1 最低检查项

- tile URL pattern；
- zoom/x/y 参数；
- image format；
- host/CDN；
- archive capture datetime per tile；
- missing tile ratio；
- 是否被 replay rewrite；
- labels 是否 baked into tile；
- route/marker 是 server image 还是 client overlay。

### 11.2 不能从“地图看起来完整”推断底层完整

一张 screenshot 可能只是恰好 viewport 内图块都幸存。

不能推出：

- 其他 zoom 完整；
- 全国 coverage 完整；
- pan 后仍完整；
- route endpoint 完整。

---

## 12. Charset / URL encoding：中文地名是技术对象

中文地图 query 往往包含：

- GB2312 / GBK 页面；
- UTF-8 API；
- percent encoding；
- JS `escape()` / `encodeURIComponent()`；
- 拼音/汉字转换；
- IE-only form behavior。

例如同一个“酒仙桥”可能在：

```text
form charset
→ browser encoding
→ URL percent encoding
→ backend decoder
→ geocoder normalization
```

任何一层错位都可能让现代 replay “表单看起来能输入，但提交永远无结果”。

因此：

> **form visible != query historically executable.**

---

## 13. Browser/JS assumptions

调查早期地图必须记录：

- IE 版本；
- ActiveX/插件依赖（若存在）；
- `document.all` / browser sniffing；
- XMLHttpRequest 兼容层；
- iframe；
- popup blocker；
- fixed viewport assumptions；
- image preload；
- mouse drag implementation；
- CSS positioning。

现代 Chromium 成功呈现不代表 IE6 时历史体验相同；现代 Chromium 失败也不代表历史 IE 当年失败。

Map UI 是 M3 browser-environment experiment 的高价值候选，因为：

- drag/zoom 强依赖 JS；
- 资源跨 host 多；
- 浏览器差异容易改变交互；
- 中文编码直接影响 query。

---

## 14. Historical route result 的时间语义

路线至少可能有这些时间：

```text
page publication time
capture time
query time
route-generation time
road-data valid time
transit-data valid time
user travel time
```

archive 通常只明确保存 `capture time`。

这不足以推出其他时间。

### 14.1 task-status drift 的地图版本：route-state drift

一个历史 route URL 今天如果仍能调用活后端，可能显示当前路线。

于是：

```text
historical URL survives
+ current route result
```

绝不能叫“历史路线复原”。

### 14.2 POI status drift

一条 2008 商户页面今天可能：

- 店已关；
- 地址已换；
- 电话已换；
- 商圈已改名；
- 经纬度被后端修正。

所以：

```text
historical POI page
!= historical business operational state
```

---

## 15. 1999—2015 的阶段性形态

### 15.1 约 1999—2004：地图成为 Web 查询对象

本轮没有取得 1999 Go2Map 的合格 historical capture，因此不把“1999 某首页长什么样”写死。

同期/后来的行业史把 Go2Map 追溯到 1999；北京本地报刊数据库又能追到 2001 线上数字地图和 2004 公共信息亭公交查询。

当前可稳妥写：

> 2000s 初期，中文网络环境中已经存在从地名/address 查询向电子地图显示迁移的公开服务形态。

不能写：

> 1999 全国普通网民已经常态使用在线 route planner。

### 15.2 2005—2009：route engine + POI + panorama + share

同期材料已确认：

- 公交/驾车路线；
- 多地图服务交叉使用；
- 公交数据库新鲜度竞争；
- 360° 实景；
- route UX；
- IM map sharing。

这阶段是本仓最值得深挖 capture 的部分。

### 15.3 2010—2015：Web map 向移动端 handoff

随着 GPS、移动数据和 smartphone map 成为重要入口，Web 页面并未立刻消失，而逐渐承担：

- 搜地点；
- 收藏/账号同步；
- 规划后发到手机；
- 商户/POI landing page；
- API/embed；
- 公共服务专题地图。

需要避免线性叙事：

> desktop Web 没有在 smartphone 出现那天立即退出。

---

## 16. Preservation levels

建议地图类 artifact 使用 M0–M8：

### M0 — Locator only

只有站名/域名/新闻提及。

### M1 — Historical shell capture

已实际核验 historical page capture，知道 original URL、capture URL、datetime、HTTP/replay 基本状态。

### M2 — Shell + static assets

HTML/CSS/主要图标/部分地图图片可验证。

### M3 — Tile coverage partially verified

能记录 viewport 内 tile URL 与 capture time，明确 missing/mixed time。

### M4 — Query form semantics verified

确认 field、method、charset、endpoint 或 client JS serialization。

### M5 — Historical result artifact verified

至少有一次历史 POI/route result 的独立 capture，而不是调用当前 live backend。

### M6 — Client execution reconstructed

在适当 browser environment 中验证历史 HTML/JS 交互；任何补全显式标 reconstruction。

### M7 — Transaction chain partially reconstructed

能从 query → result → print/share 追踪主要状态，明确无法保存的 backend 部分。

### M8 — Cross-source historical validation

archive artifact + 同期用户/教程/新闻等独立 evidence family 互相约束。

**M8 仍然不等于证明用户现实中没有迷路。**

---

## 17. 本轮 historical replay 结果

### 17.1 Mapbar

本轮根据同期证据确认 `www.mapbar.com` 为历史主体，并尝试直接访问构造的 Wayback historical replay：

```text
https://web.archive.org/web/20080401000000/http://www.mapbar.com/
```

当前研究访问链拒绝打开未经搜索结果直接产生的构造 archive URL，并返回 URL safety 限制。

因此：

```text
M1 verified Mapbar historical capture: NOT ACHIEVED IN THIS SLICE
```

这只表示：

> **本轮没有取得一份可实际检查 original URL / capture URL / capture datetime / HTTP / charset / DOM / subresources 的合格 memento。**

绝不表示：

> “Wayback 没保存 Mapbar。”

### 17.2 Mapabc

同样尝试：

```text
https://web.archive.org/web/20080401000000/http://www.mapabc.com/
```

得到同类 URL safety 限制。

因此：

```text
M1 verified Mapabc historical capture: NOT ACHIEVED IN THIS SLICE
```

### 17.3 下一次更合适的路线

- 先通过 web search 得到 archive locator，再实际 open；
- 查询 Internet Archive CDX（工具允许时）；
- 检查 Common Crawl index；
- 搜索用户保存的 print route / screenshot / tutorial；
- 查 ArchiveTeam 是否有相关集合；
- 针对 City8 panorama 另查 image/cube asset preservation。

遵守 `docs/METHOD.md`：locator 未实际检查不能升级成 capture。

---

## 18. Archive gaps 特别清单

### G1 — Dynamic route backend gap

HTML 保存，route CGI/API 不保存。

### G2 — Tile gap

主页面保存，地图图块残缺。

### G3 — Dataset-version gap

不知道 capture 时 route engine 使用哪一版道路/公交/POI 数据。

### G4 — Query-encoding gap

表单存在，但 charset/JS serialization 无法确认。

### G5 — Panorama gap

viewer shell 存在，实景图片/索引缺失。

### G6 — Live-current contamination

历史壳仍调用今天的 endpoint，产生当前地图。

### G7 — Account-state gap

收藏地点、home/work、自定义标记、历史路线在登录后，archive 不应也通常不能观察。

### G8 — Real-world execution gap

即使 route result 完整，也通常不知道用户最终是否按路线走、是否问路、是否到达。

---

## 19. 隐私边界

地图旧网考古很容易从“页面结构”滑向“个人行动轨迹”。

本仓应坚持研究必要最小化。

不应为了完整性批量恢复或公开：

- 真实普通用户 home/work；
- 私人收藏点；
- 医院/疾病相关路线；
- 约会地点；
- 家庭住址；
- 细粒度历史轨迹；
- 位置共享会话。

高质量 preservation 的目标是：

- URL pattern；
- field schema；
- route/query state；
- demo/sample；
- public service map；
- aggregate behavior；

而不是私人 mobility graph。

---

## 20. 已证实 / 高概率 / 不知道

### 已证实

- 2006 Mapbar 已明确提供公交/驾车路线查询能力；
- 2008 至少一名中文用户实际交叉使用 668map、Mapbar、Mapabc、8684、City8，并关注公交更新与实景；
- 2008 在线地图竞争已覆盖 POI、实景、实时路况、API 等维度；
- 2009 地图已能嵌入/接入 IM 共享协作场景；
- 2011—2012 公共就业服务开始出现地图化的纸/Web 多入口对象；
- 历史地图页面必须拆成 shell、query、dataset、result、tiles 等多个状态。

### 高概率但仍需 capture

- 2005—2009 Mapbar/Mapabc 的主要 route UI 存在多个历史页面版本；
- 早期 route result 很可能有独立 print/share URL；
- JS/charset/browser dependency 会显著影响现代 replay；
- route result archive 覆盖率显著低于静态首页/帮助页。

### 仍不知道

- 2008 Mapbar/Mapabc 一次具体 route transaction 的 canonical URL 与完整参数；
- route backend 是否 server-rendered、XHR 还是混合；
- 具体 tile CDN/URL pattern 在各版本怎样变化；
- historical route dataset version；
- Wayback/Common Crawl 对 route result 的实际覆盖率；
- 哪些城市/县在什么时间具有可执行公交路线查询，而不是仅地图浏览；
- mobile handoff 的早期协议与账号状态是否还能复原。

---

## 21. 后见之明风险

### 风险 1：把 Web 驾车路线写成实时 GPS 导航

早期 Web route 通常是一次生成的行前文档；没有持续 location loop。

### 风险 2：把当前地图覆盖倒投回 2008

今天一个村庄的小路存在于数据库，不能证明 2008 同样存在。

### 风险 3：把 screenshot 当成完整地图系统

一张静态截图只能证明那个画面，不证明查询、拖拽、缩放、route backend。

### 风险 4：把行业流量份额当人口普及率

iResearch/CCID 等市场数据要保留口径。

### 风险 5：把平台声称“实时”当真实世界无延迟

2018 用户对封路数据延迟的评论正好是反例：实时是系统目标，不是零延迟保证。

### 风险 6：把历史 POI 存在写成商户当时营业

地图记录、企业存在、开门营业、用户到店是不同状态。

---

## 22. 与 how-people-lived 的交叉解释

old-Web 状态机最终服务于一个生活史问题：

```text
information about opportunity
→ spatially locate opportunity
→ generate route
→ carry route outside terminal
→ execute trip
```

Web map 的历史意义不是“网页上多了一张漂亮地图”，而是让一部分陌生城市知识从必须向熟人/售票员调用，转成可由公开系统按需生成。

但 archive 最容易保存的是：

```text
map logo
search box
static POI page
```

最难保存的恰恰是：

```text
那个人输入了什么
→ 后端当时返回哪条路线
→ 他带着什么信息离开电脑
→ 路上哪里失效
→ 最后有没有到
```

所以地图也是一个典型例子：

> **platform-visible geography != lived route.**

---

## 23. Sources

### 方法

- `docs/METHOD.md`
- RFC 7089 / Memento: <https://www.rfc-editor.org/rfc/rfc7089.html>

### 中文旧网/地图

- Mapbar 小Me, 新浪科技, 2006-07-20: <https://tech.sina.com.cn/other/2006-07-20/15061047598.shtml>
- 在线地图发展新趋势, 信息周刊/泰伯网, 2008-04-10: <https://www.taibo.cn/p/4670>
- KymoWang, 实景电子地图, 2008-04-24: <https://www.cnblogs.com/Kymo/archive/2008/04/24/1170077.html>
- 网易有道地图测试版, 2008-09-01: <https://www.prnasia.com/story/13413-1.shtml>
- MSN 地图共享实测, 中关村在线, 2009-05-06: <https://soft.zol.com.cn/131/1319968_all.html>
- 北京求职地图, 新京报, 2011-02-10: <https://msn.finance.sina.com.cn/cjyw/20110210/025411055.html>
- 哈尔滨就业地图, 新华网, 2012-11-28: <https://www.xinhuanet.com/politics/2012-11/28/c_113828487.htm>
- 北京日报旧报地图专题整理: <https://xinwen.bjd.com.cn/content/s67bfa0a8e4b068c68f104f2d.html>

### 跨国技术前史（仅边界参考）

- Google Maps Navigation official blog, 2009-10-28: <https://maps.googleblog.com/2009/10/google-maps-navigation-comes-to-android.html>
- MapQuest official retrospective: <https://platform.mapquest.com/about>

---

## 24. 本轮结论

对中文旧网考古而言，地图提供了一个特别适合检验仓库方法合同的对象，因为它把几乎所有保存困难集中在一起：

- 动态后端；
- 多 host；
- 图片切片；
- JS；
- 中文编码；
- dataset 随时间变化；
- 登录后私人状态；
- 页面 capture 与现实执行之间的大状态缝隙。

以后看到一个 2008 年地图首页，最危险的说法是：

> “这个地图网站当年已经能把人带到目的地。”

更可复核的写法应该是：

> “同期证据证明该服务当时提供路线查询；某一历史 capture 若能进一步验证，只能证明页面/事务的特定状态。route engine 是否被 archive 保存、当时数据版本如何、用户是否实际抵达，仍需分别取证。”

地图的 old-Web artifact 保存的是**可计算的城市的一部分**，不是那个普通人真正走过的全部城市。
