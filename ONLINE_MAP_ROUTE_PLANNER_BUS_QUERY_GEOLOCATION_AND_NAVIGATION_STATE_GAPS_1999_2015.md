# ONLINE MAP / ROUTE PLANNER / BUS QUERY / GEOLOCATION / NAVIGATION STATE GAPS（1999—2015）

## 0. Scope

本文件研究约 1999—2015 年中文互联网里的在线地图、公交查询、路线规划与早期移动导航，重点不是写“地图公司发展史”，而是恢复一个旧 Web 事务：

> **用户输入一个起点和终点以后，当时的系统到底做了什么，而今天的档案还能证明到哪一步？**

仓库 scope 保持不变：

- 主体仍是约 1995—2015 中文互联网；
- 1994 以前中国信息环境只作为边界说明；
- Minitel / MapQuest 等海外前史不在本仓展开，跨国生活史写入 `how-people-lived`；
- 2016 年以后只在必要时用于说明 old-Web 状态的 afterlife，不作为本文件主研究对象。

交叉生活史文件：

- `how-people-lived/topics/from-asking-directions-to-delegating-the-next-turn-maps-route-planning-and-navigational-executability-china-1980-2026.zh-CN.md`

本文件遵守 `docs/METHOD.md`：

- platform / site / page / query / capture / claim 分离；
- A/B/C/D 分级；
- `exists / available / used / popular / caused` 分离；
- 未实际打开的 archive locator 不算 verified capture；
- 当前网页、新闻截图和后来重建不能冒充历史浏览体验。

---

## 1. 为什么在线地图是特别容易被“保存错”的旧 Web 对象？

普通文章页的核心历史对象可能是 HTML 正文。

地图则往往至少有五层：

```text
页面 shell
+ 地点/道路数据库
+ 查询参数
+ 路线计算服务
+ 地图图像/tiles/Flash/JS 子资源
```

一次真实的历史查询又至少多一层用户输入：

```text
用户脑中的起点/终点
→ 文本输入
→ 地名解析
→ 路线图数据库
→ 路径计算
→ 页面渲染
→ 用户理解
→ 现实道路执行
```

所以：

> **`map-page capture != historical route transaction`。**

Archive 保存了查询框，不代表保存了 2008 年 6 月某一组起点终点返回的路线。

Archive 保存了地图图层，也不代表保存了当时路线数据库、实时交通状态或某个 POI 的历史坐标。

---

## 2. 边界：1994 全功能接入 ≠ 1994 普通人已经在 Web 上查地图

CNNIC 历史记录把 1994 年 4 月 20 日 NCFC 的 64K 国际专线作为中国与 Internet 全功能连接节点；同一历史序列同时说明此前后已有科研联网、电子邮件、`.CN`、高校网络和 BBS 等发展。[CNNIC](https://www3.cnnic.cn/n4/2022/0401/c87-912.html)。

对本仓的意义不是继续前移 scope，而是避免两个错误：

```text
1994 以前
!=
中国完全没有数字通信
```

以及：

```text
1994 全功能接入
!=
1994 普通家庭已经能够在线路线规划
```

中文在线地图真正进入本文件的可核验时间带，主要从 1999—2000 开始。

---

## 3. 1999—2000：Go2Map 是目前本轮最强的早期 Web 锚点之一

### 3.1 同时代报道能够证明什么？

2000 年 8 月《中华读书报》介绍早期网上电子地图时称：

- 图行天下成立于 1999 年 5 月；
- 以 Go2Map 提供在线电子地图服务；
- 已向新浪、114China 等站点提供地图嵌入服务；
- 数据调查涉及政府机关、企业、景点、写字楼、高校、医院、影剧院；
- 服务维度包括位置、街区、公交换乘和门牌号码；
- 到 2000 年 6 月已开通 50 多个城市地图服务；
- 同期报道又明确指出在线地图速度不快、上网费较贵，对许多网民而言在线查地图仍“有些奢侈”。

来源：[光明网《数字时代的网上电子地图》，2000-08-02](https://www.gmw.cn/01ds/2000-08/02/GB/2000%5E311%5E0%5EDS1704.htm)。

证据等级：**B，near-contemporary secondary**。

可以支持：

- 2000 年中文 Web 已有在线地图服务；
- Go2Map 已有跨站嵌入/ASP 服务形态；
- 城市 POI、公交换乘和门牌号是当时产品目标；
- 使用体验受速度与接入成本约束。

不能支持：

- “Go2Map 是所有意义上的中国第一张网络地图”的绝对唯一性；
- 50 多个城市每个都有相同数据质量；
- 普通家庭普遍使用；
- 用户每次查询都能成功返回路线。

### 3.2 2005 SEC 文件提供第二个独立 evidence family

搜狐 2005 年收购 Go2Map 的 SEC 公告称，Go2Map 的平台可通过 Internet/Intranet、手机、call center、PDA 提供位置服务，并称 POI 数据覆盖约 200 个城市。[SEC filing，2005-04-12](https://www.sec.gov/Archives/edgar/data/1104188/000119312505075385/dex991.htm)。

证据等级：**A（公司同期正式文件）**。

它证明的是公司在交易时对技术与业务能力作出的正式陈述，不自动证明使用效果或覆盖质量。

这两个 evidence family 组合后可以较稳地写：

> 1999—2005 年间，Go2Map 已把在线地图从一个独立 Web 页面扩展成可被门户、电话中心和移动终端调用的空间数据服务。

仍不能写：

> 中国普通人到 2005 年已经普遍依赖 Go2Map 找路。

---

## 4. 2004—2005：搜索门户开始把“地图”纳入通用搜索入口

### 4.1 搜狐收购 Go2Map

2005 年搜狐的 SEC 文件本身已经说明收购意图：把专业 location-based information 与搜狐搜索及内容结合。

### 4.2 百度地图搜索 2005 年上线

2005 年同期行业报道记录，百度地图搜索于 2005 年 9 月上线；同一时期搜狐已通过 Go2Map/搜狗进入地图搜索竞争。[21世纪经济报道/新浪，2005-10-15](https://tech.sina.com.cn/i/2005-10-15/0924741626.shtml)。

证据等级：**B**。

这可以支持“地图成为通用搜索产品的一部分”，不能支持“百度地图当年已经具备今天的导航功能”。

这一时期研究时要把：

```text
map search
```

和：

```text
turn-by-turn navigation
```

分开。

---

## 5. 查询状态机一：地点搜索 / geocoding

历史在线地图最容易被现代语感压平的是“搜一个地点”。

建议至少拆成：

```text
USER_HAS_INTENDED_PLACE
    ↓
TEXT_QUERY_TYPED
    ↓
REQUEST_SENT
    ↓
GEOCODER_RETURNS_CANDIDATES
    ↓
USER_SELECTS_CANDIDATE
    ↓
COORDINATE / POI RESOLVED
    ↓
MAP CENTERS / MARKER RENDERS
    ↓
REAL_WORLD_PLACE_MATCHES_INTENT ?
```

关键否定式：

- `文字匹配 != 地理身份确认`
- `POI 存在 != POI 仍营业`
- `坐标正确 != 入口正确`
- `小区中心点 != 某栋楼门口`
- `同名地点候选出现 != 用户选对`
- `地图 marker 可见 != 现实标识可见`

这类状态今天仍会失效，因此不能用现代地图成功率倒推旧 Web。

---

## 6. 查询状态机二：路线规划

建议至少拆成：

```text
MAP_DATA_VERSION
    ↓
ORIGIN_RESOLVED
    ↓
DESTINATION_RESOLVED
    ↓
MODE / TACTIC SELECTED
    ↓
ROUTE_GRAPH AVAILABLE
    ↓
ROUTE COMPUTED
    ↓
RESULT HTML / MAP GENERATED
    ↓
SUBRESOURCES LOADED
    ↓
USER READS / PRINTS / COPIES
    ↓
REAL-WORLD ROUTE STILL OPEN
    ↓
USER FOLLOWS
    ↓
ARRIVAL
```

任何研究结论都不能把其中相邻状态默认合并。

特别是：

> **`route computed != route still executable in the physical world`。**

---

## 7. 查询状态机三：公交换乘

公交比道路导航多出至少四层时间状态：

```text
线路存在
→ 今天运营
→ 站点仍在原位置
→ 时刻/班次与用户到站时间匹配
```

所以：

- `route listed != bus currently running`；
- `stop name match != same physical stop`；
- `transfer graph valid != service frequency sufficient`；
- `recommended route != fastest in lived time`。

对 old-Web 考古尤其要避免把一个保存下来的“公交路线结果”当作连续多年有效的事实。

---

## 8. 2008 北京公交网：目前本轮最有价值的真实旧 Web 技术切片

2008 年 6 月 26 日一篇安全报道留下了一段罕见的操作路径：

1. 进入“北京公交网”主页；
2. 在右侧“公交换乘”输入起点、终点；
3. 点击查询；
4. 弹出动态查询页面；
5. 报道记录了 URL 形态：

```text
www.bjbus.com/busmap/map.jsp
?moduel=busrute
&Start=***
&End=***
&BusTactic=64
```

6. 当时 Symantec Antivirus 报警；报道指向一个 `ie[1].swf`，并提到此前用户反映 IE 漏洞/Flash 下载器问题；当天 11:10 左右报道更新称疑似病毒文件已清除。

来源：[DOIT，2008-06-26](https://www.doit.com.cn/p/29306.html)。

证据等级：**B，同期技术观察**。

这一条材料同时证明了三件不同的事：

### 8.1 页面事务

`Start`、`End` 与 `BusTactic` 至少在该报道观察到的 URL 中参与路线查询。

### 8.2 服务端依赖

`map.jsp` 表明结果并非一张纯静态地图；它至少需要服务端动态处理。

### 8.3 浏览器/安全环境属于历史体验的一部分

当时的 IE、Flash/SWF 和安全软件共同决定“能不能查一条公交路线”。

所以即使今天 archive 保存了 HTML：

```text
HTML preserved
!=
JSP backend preserved
!=
historical route DB preserved
!=
SWF behavior preserved
!=
same IE security behavior preserved
```

这应当成为未来 M3 浏览器差异实验的优先候选之一。

---

## 9. 2008 广州：纸、电话、Web 是并行渠道，不是简单替代链

2008 年广州同期报道显示，公交信息服务同时包括：

- 向市民家庭发放大批免费乘车手册；
- 通过“坐车网”查询路线；
- 免费电话 `96900` 咨询。

来源：[信息时报/新浪，2008-05-09](https://news.sina.com.cn/c/2008-05-09/040313850719s.shtml)。

证据等级：**B**。

这对 old-Web scope 很重要，因为它提示：

> **Web 只是当时 route-information stack 的一个入口。**

研究一个 2008 年公交网站时，如果只看网页，就会系统性漏掉同时存在的纸质指南和电话通道。

因此建议写成：

```text
route information ecosystem
= paper + hotline + Web + human help
```

而不是：

```text
paper → Web
```

---

## 10. 2008 的人类 fallback：“公交活地图”

《新京报》2008 年报道一名 28 岁北京居民穆青，周围人会给他打电话问公交路线；他还花数月调查站名/路线问题并制作公交导航图。[新京报/新浪，2008-12-29](https://news.sina.com.cn/c/2008-12-29/025914950121s.shtml)。

证据等级：**B，含同期人物自述**。

对本仓最重要的不是人物故事本身，而是状态边界：

```text
online route planner exists
+
human route expert remains useful
```

原因可能包括：

- 数据有错；
- 用户不会使用；
- 用户没有网络；
- 具体上下车点难以解释；
- 临时交通变化；
- 本地经验无法完整编码。

因此不能把一个地图网站的上线日期写成“问路行为消失日期”。

---

## 11. 2009 百度地图：Flash 是地图体验的一部分

2009 年百度地图升级报道提到：

- 搜索建议；
- 道路与地点地图搜索；
- Flash 形式的地铁线路展示等。

来源：[每日经济新闻，2009-08-25](https://www.nbd.com.cn/articles/2009-08-25/238063.html)。

证据等级：**B**。

这意味着 historical replay 至少要记录：

- 当时是否要求 Flash；
- SWF 是否被 archive 保存；
- SWF 是否请求外部数据；
- modern Chromium 下是否直接缺失；
- Ruffle 重放是否属于 reconstruction；
- 若使用 IE6/Flash Player，版本差异是否改变行为。

不能把现代浏览器中一个空白区域解释成“2009 年页面本来就是空白”。

---

## 12. 2010 GPS 数据滞后：数字地图不是现实道路的即时镜像

2010 年高速公路编号调整后，浙江在线/《今日早报》报道多款 GPS 地图未及时识别新的高速编号；其中一名论坛用户描述自己在路上看到新编号、导航无法识别，一度以为走错，只能再问朋友。[浙江在线/搜狐汽车，2010-04-14](https://auto.sohu.com/20100414/n271495216.shtml)。

证据等级：**B，媒体引用同期论坛自述**。

这里至少有四个独立状态：

```text
GPS FIX OK
ROAD PHYSICALLY EXISTS
ROAD SIGN RENAMED
MAP DB OLD
```

因此：

> **`GPS position valid != map semantics current`。**

以后研究任何“导航成功”都不能只检查定位。

---

## 13. 从 desktop Web 到 mobile：不能用今天的 turn-by-turn 体验倒灌 2000s 网页地图

2007 年对 Mapbar 的同期行业报道已经讨论在线地图向移动服务延伸；2005 年 Sohu/Go2Map 文件也把手机与 PDA 列入渠道。[泰伯网转载新浪科技，2007-09-19](https://www.taibo.cn/p/4043)。

但至少要拆：

```text
desktop map search
→ WAP/mobile map page
→ device positioning
→ GPS-assisted navigation
→ continuously recalculated turn-by-turn route
```

这些不是一个功能。

对 2005 年网页地图写“导航”时，必须说明它到底是：

- 显示地图；
- 搜 POI；
- 公交换乘；
- 生成文字路线；
- 还是随用户移动持续导航。

---

## 14. 页面保存状态机

### 14.1 地图 shell

```text
HOST_RESOLVES
→ HTML_CAPTURED
→ CSS_CAPTURED
→ JS_CAPTURED
→ TILE/SWF/IMAGE_CAPTURED
→ PAGE_VISUALLY_REPLAYS
```

任何一步都可能失败。

### 14.2 事务回放

```text
FORM_VISIBLE
→ FORM_ACTION_KNOWN
→ QUERY_ENDPOINT_REPLAYS
→ HISTORICAL DB AVAILABLE
→ RESULT GENERATED
→ RESULT SUBRESOURCES LOAD
```

即使 14.1 全部成功，14.2 仍可能完全失败。

### 14.3 动态 tile 问题

旧地图常把地图切成大量小图片或通过脚本按视窗请求资源。

因此 archive 可能出现：

- 中央几块 tile 有、周边没有；
- HTML 有、tile host 没抓；
- JS 被 rewrite 后失效；
- zoom level 变化后请求不存在；
- 路线 overlay 丢失；
- marker icon 丢失。

截图只能证明一个历史时刻**曾经被拍到的视觉状态**，不能独立证明请求链。

---

## 15. 用户事务状态与 archive 事务状态必须分开

用户侧：

```text
USER INTENDS PLACE A
→ TYPES "A"
→ SELECTS RESULT
→ READS ROUTE
→ PRINTS / REMEMBERS
→ LEAVES COMPUTER
→ TRAVELS
→ ARRIVES / GETS LOST
```

Archive 侧：

```text
CRAWLER REQUESTS URL
→ SERVER RETURNS REPRESENTATION
→ ARCHIVE STORES MAIN RESOURCE
→ SOME SUBRESOURCES STORED
→ MODERN REPLAY REWRITES URLS
```

两条链只有很小的交集。

所以：

> **`archived route page != evidence that a historical user followed that route`。**

---

## 16. Browser / runtime matrix

旧地图案例至少应检查：

| 层 | 可能问题 |
|---|---|
| IE5/IE6 | `document.all`、ActiveX、旧事件模型、漏洞/挂马风险 |
| Flash | 地铁图、交互图层、动画、SWF 数据加载 |
| JavaScript | 动态请求、地图移动、表单校验、overlay |
| charset | GB2312/GBK 地名参数编码 |
| URL rewrite | 中文起终点在 archive 重写后是否仍可复现 |
| cookies/session | 个性化、历史查询、登录状态 |
| viewport | 800×600 / 1024×768 下侧栏与地图区域是否不同 |
| image/tile hosts | 主域保存但资源域失踪 |

2008 北京公交网案例还增加一个研究提醒：**安全状态属于浏览器史的一部分。**

一个历史用户可能因为杀毒软件弹窗、IE 漏洞或 Flash 风险而无法继续完成“查路线”。

---

## 17. Place identity state machine

地图研究不能把“地名”当唯一键。

至少应记录：

```text
DISPLAY NAME
ADMINISTRATIVE AREA
ADDRESS STRING
POI ID
COORDINATE
ENTRANCE / GATE
VALIDITY PERIOD
```

同名地点尤其危险。

因此：

```text
NAME MATCH
!=
POI ID MATCH
!=
COORDINATE MATCH
!=
HISTORICAL SAME PLACE
```

一个学校、医院、公司或公交站可能：

- 改名；
- 搬迁；
- 新增分院/分店；
- 合并；
- 撤销；
- 保留旧 POI；
- 在不同地图平台使用不同 ID。

这会直接污染历史 route reconstruction。

---

## 18. Map–world lag state machine

建议对每个重要路线结论单独记录：

```text
PHYSICAL CHANGE DATE
MAP DATA UPDATE DATE ?
WEB DISPLAY UPDATE DATE ?
USER DEVICE DATA VERSION ?
```

2010 高速编号案例已经证明这些时间可以不同。

不能从：

> “2010 年道路已改名”

直接推：

> “2010 年 4 月所有在线地图都显示新名”。

也不能从今天的历史道路数据库反向修改当年屏幕状态。

---

## 19. 旧 Web 与现实行为的因果边界

### 可以较稳地写

- Web 地图降低了部分联网用户主动查地点和路线的查询成本；
- 动态路线规划让起点/终点可以成为表单参数；
- 打印/抄写后离线执行是 desktop Web 时期合理的事务路径；
- 与纸质指南、电话、人工问路长期并行；
- 数据更新、浏览器、插件、网络速度会影响可执行性。

### 不能直接写

- Web 地图导致中国城市迁移增加；
- 地图 App 导致年轻人更愿意换工作；
- 2000 年网上地图让普通家庭不再买纸地图；
- 2008 年公交查询页面存在就代表路线信息准确；
- 2010 年有 GPS 的司机都不再问路。

这些都需要独立因果证据。

---

## 20. Archive / preservation bias

### 最容易留下

- 公司新闻稿；
- 地图网站首页；
- 功能介绍；
- 城市覆盖列表；
- 静态帮助页；
- 媒体截图；
- 一部分查询 shell。

### 最容易消失

- route DB；
- geocoder DB；
- 动态 JSP 返回；
- tile server；
- Flash 内加载的数据；
- 登录后历史记录；
- 用户真实起点终点；
- 打印/手抄路线；
- 电话问路；
- 现实临时封路；
- 用户发现错误后怎样纠正。

因此：

> **`historian-visible map != historical navigational system`。**

此外，用户起终点、家庭住址和历史移动轨迹本身具有隐私属性；缺乏公共 archive 不应被当作必须“补齐”的缺陷。

---

## 21. 本轮 historical capture 检索结果

本轮尝试围绕：

- `go2map.com` 2000—2002；
- `www.bjbus.com/busmap/map.jsp` 2007—2009；
- Mapbar / 百度早期地图的相关 locator；

寻找可实际验证的 historical replay。

当前 Web 访问链对直接构造的 Wayback CDX URL 返回安全限制，未取得可按照 `docs/METHOD.md` 实际检查的：

- `capture_datetime`；
- original URL；
- HTTP/replay state；
- charset；
- DOM；
- form action；
- SWF/JS/tile subresources；
- cookie/session；
- historical query result。

因此本轮结论严格是：

> **M1: NOT ACHIEVED IN THIS SLICE.**

只表示：

> 本轮没有验证到合格 historical capture。

不表示：

> Wayback 没有保存。

也不表示：

> 历史页面不存在。

这符合 METHOD 的负证据规则。

---

## 22. 候选 capture / locator 清单（未验证）

以下只登记为后续调查对象，不升级为 A：

- `http://www.go2map.com/`
- `http://www.go2map.com.cn/`
- `http://www.bjbus.com/`
- `http://www.bjbus.com/busmap/map.jsp`
- 2005 前后百度地图搜索入口
- 2004—2007 Mapbar / 图吧入口
- 早期坐车网公交查询入口

后续若工具链可访问 CDX/WARC，应优先：

1. 先取 capture index；
2. 记录时间点；
3. 分别保存 main document 与子资源状态；
4. 检查参数 URL 是否被 crawl；
5. 不用现代地图 API 补历史缺失结果。

---

## 23. 一个最小完整 case 应该怎样做？

优先候选：**2008 北京公交网公交换乘查询**。

原因：

- 有同期实际操作描述；
- 有动态 URL pattern；
- 有查询参数；
- 有 Flash/SWF；
- 有 IE/安全环境；
- 有明确日期；
- 有人类公交导航 fallback 可形成生活史对照。

如果取得 capture，至少记录：

```yaml
subject: Beijing bus route query
site: www.bjbus.com
page_pattern: /busmap/map.jsp
observed_historical_claim_date: 2008-06-26
archive_source: ?
capture_datetime: ?
original_url: ?
query_parameters:
  Start: yes
  End: yes
  BusTactic: observed value 64
runtime:
  javascript: ?
  flash: observed in contemporary security report
  browser_assumption: IE-era environment relevant
charset: ?
backend_replayable: ?
result_tiles_or_images: ?
confidence: pending capture
```

这比“找一张旧截图”更接近本仓真正需要的案例。

---

## 24. 与普通生活史的交叉矩阵

| 生活问题 | 旧网对象 | 必须证明的状态 |
|---|---|---|
| 去陌生公司面试 | 地点搜索 / 公交查询 | 地址解析、路线结果、现实可达 |
| 异地看病 | 医院 POI / 公交 / 院内地图 | 分院/入口、路线、院内 fallback |
| 看房 | 小区 POI / 地图嵌入 | 小区定位、公交、现实入口 |
| 通勤 | 公交换乘 / 路况 | 路线存在、班次、当日拥堵 |
| 探亲 | 地址查询 / 路线 | 老地址是否仍有效 |
| 旅游 | 景点地图 | POI、开放状态、入口 |
| 夜间出行 | 路线 + 实际服务时间 | 夜班服务、末班时间 |
| 独自迁移 | 地图 + 电话/搜索 | 是否无需本地熟人即可继续下一步 |

这个矩阵的核心不是证明“互联网更方便”，而是定位：

> **哪一层过去必须由本地人解释，后来被数据库和界面接管？**

---

## 25. Evidence ledger

### E1 — 2000 online map landscape

- URL: https://www.gmw.cn/01ds/2000-08/02/GB/2000%5E311%5E0%5EDS1704.htm
- type: contemporary press
- grade: B
- proves: Go2Map service claims, embedded-map ecosystem, cost/speed constraint
- does not prove: household prevalence

### E2 — 2005 Go2Map acquisition

- URL: https://www.sec.gov/Archives/edgar/data/1104188/000119312505075385/dex991.htm
- type: corporate filing/press release in SEC archive
- grade: A
- proves: company-reported platform/channel/POI scope at acquisition
- does not prove: successful use by all users

### E3 — 2008 Beijing bus query

- URL: https://www.doit.com.cn/p/29306.html
- type: contemporary technical/security report
- grade: B
- proves: observed form workflow, query URL pattern, SWF/security environment
- does not prove: every historical request infected or every route result accurate

### E4 — 2008 Guangzhou channel stack

- URL: https://news.sina.com.cn/c/2008-05-09/040313850719s.shtml
- type: contemporary press
- grade: B
- proves: paper + Web + phone coexistence
- does not prove: usage share by channel

### E5 — 2008 human fallback

- URL: https://news.sina.com.cn/c/2008-12-29/025914950121s.shtml
- type: contemporary profile
- grade: B
- proves: one person acted as route-information helper and correction source
- does not prove: representative frequency

### E6 — 2009 Baidu map / Flash

- URL: https://www.nbd.com.cn/articles/2009-08-25/238063.html
- type: contemporary technology press
- grade: B
- proves: product features described at that time, including Flash subway presentation
- does not prove: same render in all browsers

### E7 — 2010 GPS/map lag

- URL: https://auto.sohu.com/20100414/n271495216.shtml
- type: contemporary press quoting user/forum experience
- grade: B
- proves: map DB lag could conflict with newly renamed physical roads
- does not prove: all GPS products failed identically

---

## 26. Hindsight risks

### Risk A — “网上地图出现 = 纸地图退出”

2008 的广州 channel stack 直接否定这种写法。

### Risk B — “网页地图 = 手机导航”

desktop route planner、WAP、GPS 定位和 turn-by-turn 是不同阶段。

### Risk C — “地图上有 = 现实里有”

POI、站点、道路和营业状态都有时间差。

### Risk D — “archive 有页面 = 当年查询可重现”

路线计算依赖后端历史数据库，静态 capture 通常不足。

### Risk E — “现代浏览器能打开 = 当年用户看到这样”

Flash、IE、charset、viewport 和 tile 加载都可能改变呈现。

### Risk F — “用户最后到了 = 推荐路线正确”

用户可能途中问路、改道、打车或靠熟人纠错。

---

## 27. What we know / infer / do not know

### 已证实

- 2000 年已有中文网上电子地图服务与 Go2Map 嵌入式地图生态的同期报道；
- 同期报道明确记录了速度与上网费用障碍；
- 2005 年 Go2Map 公司材料把 Internet、手机、call center、PDA 列为渠道；
- 2008 北京公交网的同期技术报道留下动态 route-query URL pattern 与 Flash/IE 安全环境；
- 2008 广州纸质乘车手册、Web 与电话查询并行；
- 2009 百度地图至少有 Flash 地铁图等旧运行时对象；
- 2010 有同期用户材料证明 GPS/map data 与新道路编号之间存在更新时差。

### 可合理推断

- 2000s desktop Web route planning 经常是“联网计算 → 打印/抄写/记住 → 离线执行”；
- 普通人的路线可执行性由地图数据库、网络、浏览器、人类帮助和真实道路共同组成，而不是一个页面独立决定；
- 地图 archive 的系统性缺口比普通文章页更严重，因为大量关键状态位于服务端数据库和动态资源。

### 仍不知道

- 2000—2004 Go2Map 普通用户真实操作界面各年份到底怎样变化；
- 早期地图服务具体 charset、JS 框架、tile 切分和缓存策略；
- `BusTactic=64` 在 2008 北京公交系统中的完整枚举语义；
- 查询结果是否使用独立地图 tile host；
- 2005—2010 普通用户打印、抄写、短信转发路线的频率；
- 早期 WAP 地图资费和兼容性对实际使用的阻碍程度；
- 是否能在 Wayback/Common Crawl/其他馆藏中恢复一条完整的历史动态路线事务。

---

## 28. 下一步

如果下一轮继续本对象，优先级应是：

1. 获取 `bjbus.com/busmap/map.jsp` 2008 前后的 verified capture；
2. 获取 `go2map.com` 2000—2002 两个以上时点；
3. 检查 HTML charset、form method/action、query parameter encoding；
4. 检查 SWF/JS/tile 子资源；
5. 设计 IE6 + historical Flash 的最小重放实验，但所有现代补全明确标 `reconstruction`；
6. 与同时期纸质公交指南做同一路线的结果差异实验；
7. 不记录或重新公开普通人的具体家庭起终点、历史移动轨迹。

---

## 29. 这一 slice 改变了什么？

地图网站不是“把纸地图搬到屏幕上”。

真正的旧 Web 转折是：

> **城市空间第一次变成一个可以向服务器提交问题的数据库。**

用户不再只看一张图，而是可以说：

```text
我在这里
我要去那里
请算一条路
```

但那条路并不生活在 HTML 里。

它生活在当时的地名数据库、公交线路表、道路图、服务器程序、Flash/JavaScript、浏览器版本和现实街道共同组成的事务里。

这也是为什么在线地图特别适合作为旧网考古对象：

> **今天最容易保存下来的是“查询框曾经存在”，最容易消失的却是“2008 年那个人按下查询以后，系统究竟告诉他怎么走”。**

> 初稿由 AI 辅助形成；后续必须以 verified capture / WARC / historical browser experiment 提升技术结论，当前未取得的状态保持为未知。