# 在线地图、路线规划、地图瓦片与路由状态缺口，1999—2015

## 定位

本笔记属于中文旧网的 **dynamic map / query-state / runtime research note**，不是 M1 完整案例。

本轮研究的问题不是“某个地图网站首页长什么样”，而是：

> **一个 1999—2015 年中文在线地图页面，到底依赖哪些页面之外的数据和计算，为什么 archive 保存了 HTML 仍可能没有保存历史地图体验？**

与 `how-people-lived` 的生活史交叉研究见：

- <https://github.com/tmzncty/how-people-lived/blob/main/sources/from-paper-traffic-maps-to-mobile-navigation-route-executability-and-local-spatial-knowledge-china-1978-2026.zh-CN.md>

本仓 scope 仍保持约 1995—2015 中文互联网。美国 MapQuest、CD-ROM 旅行软件等跨国比较放在 HPL；这里只在必要处作为方法参照。

---

## 一、开工去重

仓库已经有：

- 机票搜索 / 预订状态；
- 铁路票和其他事务接口研究；
- 114 / 网上黄页的 query / ranking state；
- 医院预约号源 state；
- EMS tracking event stream；
- 网吧 runtime context；
- classifieds listing lifecycle；
- 多种登录、支付、凭证、关系状态缺口。

但仓内搜索 `地图 / 导航 / Mapbar / Go2Map / 公交查询 / 路线规划` 没有发现独立专题。

地图站与上述 transaction site 又有明显不同：

```text
用户请求不是只返回一条数据库记录
而是：
输入位置 / 起终点
→ 地理编码
→ 读取某一版空间数据
→ 选择交通模式
→ 运行路由算法
→ 生成路径
→ 请求多个地图图块 / 图层
→ 叠加 POI / 路线 / 文字说明
→ 用户继续 pan / zoom / 改条件
```

所以需要独立建模。

---

## 二、历史 identity：Go2Map 最迟 1999 已属于中文 Web 地图前史

2005 年 SOHU 向美国 SEC 公开的收购公告提供了一个高质量 A 级 identity anchor：

- 公司：Go2Map Inc. / 北京图行天下；
- historical URL：`http://www.go2map.com`；
- 服务：online mapping；
- 通过 Internet/Intranet、mobile phone、call center、PDA 等多个终端提供地图能力；
- 数据库声称覆盖约 200 个城市 POI；
- 其中 14 个城市向 Web surfers 提供免费在线地图查询。

来源：

- SOHU / SEC，2005-04-12：
  - https://www.sec.gov/Archives/edgar/data/1104188/000119312505075385/dex991.htm
  - **A：同时代正式公司披露。**

2007 年近同时代行业回顾将 Go2Map 公开服务起点追溯到 1999 年 5 月：

- https://www.eeo.com.cn/2007/0604/67899.shtml
- **B/C：近同时代行业回顾，不作为精确页面结构证据。**

因此 OWA 的中文地图谱系不能从 2005 年 Google / 百度开始。

---

## 三、不要把“地图网站”当成一张大图片

一个静态旧网页通常可以粗略分成：

```text
HTML
CSS
JS
images
```

在线地图更接近：

```text
page shell
+
place / POI database
+
geocoder
+
road / transit graph
+
routing engine
+
map tile or rendered-map service
+
overlay / marker state
+
query parameters
+
user interaction state
```

因此需要一个更严格的 research unit。

本笔记建议把一次历史在线地图体验至少拆成：

1. `platform` — Go2Map / Mapbar / 搜狗地图 / 谷歌地图等；
2. `page shell` — 首页 / 搜索页 / 路线页；
3. `map data version` — 当时的道路、POI、公交数据；
4. `geocoder state` — 字符串如何被解析成坐标 / POI；
5. `route engine state` — 当时算法和约束；
6. `tile/render layer` — 地图图块或服务端生成图；
7. `query state` — 起点、终点、模式、过滤条件；
8. `viewport state` — center / zoom / pan；
9. `result state` — 路线、换乘、距离、排序；
10. `capture` — archive 实际保存了其中哪些表示。

---

## 四、`map shell survival != map survival`

在线地图尤其容易出现一种错觉：

> archive 打开一个历史地图 URL，搜索框和 logo 都在，所以“历史地图保存下来了”。

这可能完全不成立。

页面 shell 可以存活，但：

- 图块 host 已死；
- JavaScript API 已变；
- route endpoint 已死；
- POI backend 已换库；
- token / key 已失效；
- archive rewrite 破坏相对 URL；
- 旧 HTTP 子资源被现代 HTTPS 环境阻断；
- query 依赖 POST / XHR，crawler 没保存响应；
- 同一 URL 今天返回的是另一代地图数据。

因此增加：

## `map-runtime survival gap / 地图运行时存活缺口`

历史地图是一个运行系统，不是一张截图。

---

## 五、2004：预生成地图说明“地图版本”本身就是 artifact

2006 年 3sNews 对 Go2Map 创始人的近同时代访谈回顾称：

- 早期 Go2Map 访问速度较慢；
- 2004 年采用“预先生成地图”的技术路线；
- 目的是减少服务器计算压力、提高访问速度；
- 但预生成也会限制某些信息源的动态显示。

来源：

- 3sNews / 泰伯网，2006-09-11：
  - https://www.taibo.cn/p/1598
  - **B/C：2006 年对 2004 架构的企业/行业回顾。**

这个信息非常重要，因为它说明不能只研究 HTML。

如果某一代地图是预先生成的，那么历史地图可能存在一批真正的图像 artifact：

```text
map version N
→ render / pre-generate
→ many image chunks
→ browser requests relevant chunks
```

archive 若只抓到 page shell，却没有把这些 chunk / tile 保存下来，空间内容就会大面积丢失。

---

## 六、`map-tile state loss / 地图图块状态丢失`

到 2010s，中文地图站的图块依赖已经非常明确。

2013 年一篇同时代开发者博客用浏览器开发工具观察搜狗地图，记录到当时的 tile 请求类似：

`http://p2.go2map.com/seamless1/.../744_212.png`

并尝试解释 zoom、x、y 等参数的构造方式。

来源：

- 博客园，2013-01-29：
  - https://www.cnblogs.com/enjoyeclipse/archive/2013/01/29/2880791.html
  - **B：同时代开发者技术观察，不是平台官方协议。**

另一篇 2013 年技术笔记还横向记录了 Google、SoSo、Baidu、Sogou、Nokia、Bing 等多个图块 URL，并指出不同服务有加密/偏移/尺寸差异；其中 Sogou 仍出现 `go2map.com` 图块 host。

- 博客园，2013-04-25：
  - https://www.cnblogs.com/hyb1/archive/2013/04/25/3042475.html
  - **B：同时代开发者观察。**

因此恢复一张历史地图时至少要问：

```text
主 HTML 保存了吗？
JS 保存了吗？
tile host 保存了吗？
这一 zoom 的所有可见 tile 保存了吗？
marker / label 是否独立图层？
archive replay 是否仍向 live host 取 tile？
```

如果最后一种情况发生，现代截图可能出现危险的混合：

> **historical shell + present-day map data**

这不能叫历史原件。

---

## 七、`map-version drift / 地图版本漂移`

地图数据是会变的。

2007 年一次 Google 中国相关访谈中，现场用户直接提出地图数据“陈旧”的问题；李开复的回答也承认地图服务需要持续改善数据，并讨论中美用户交通方式差异。

来源：

- CNET / ZOL 访谈存续页，2007-08-29：
  - **B：同期公开交流；本轮保留为地图更新问题 evidence family。**

2006 年中国移动 / 联通定位业务报道也明确把“地图、公交线路、餐馆位置等信息需要经常更新”列为移动位置服务瓶颈之一；报道还称某导航地图供应方会定期进行数据更新。

- 《新经济导刊》/ 新浪科技，2006-03-14：
  - https://tech.sina.com.cn/t/2006-03-14/1547867045.shtml
  - **B：同期产业报道。**

因此历史地图 claim 必须带版本意识：

```text
“2008 年某站能显示北京某路”
```

不能由：

```text
“今天用历史 URL 打开后能显示这条路”
```

推出。

增加：

## `map-version provenance / 地图版本 provenance`

至少记录：

- capture datetime；
- 页面版本；
- 可观察的数据更新时间；
- tile / API endpoint；
- 是否出现 live contamination；
- 是否能证明 route result 与 capture 同时代。

---

## 八、地点搜索不是静态 lookup：`geocoder-state loss`

用户在地图站输入的通常不是坐标，而是：

- `北京站`；
- `中关村`；
- `某某饭店`；
- 一条门牌地址；
- 一个旧地名；
- 甚至拼写错误。

系统必须把字符串映射成：

```text
canonical place / POI
+
coordinate
+
possible alternatives
```

这层通常不会被 archive 保存。

因此增加：

## `geocoder-state loss / 地理编码状态丢失`

一张历史地图截图能证明“某坐标处画了一个 marker”，却不一定能证明：

- 用户当时输入了什么；
- 系统给出过几个同名候选；
- 第一候选为什么排在前；
- 旧地名是否能解析；
- 错别字是否被纠正；
- 地址数据库当时更新到哪一版。

这和黄页 research note 的 query-state gap 相邻，但对象不同：这里返回的不只是一个商家 record，而是**一个空间实体和后续路线计算的起点**。

---

## 九、路线结果是“当时算法 × 当时地图 × 当时条件”的产物

2006 年 Mapbar 同期产品报道已经出现：

- 地图查询；
- 公交驾车；
- 公交线路；
- 公交站点；
- 用户问路。

来源：

- ChinaByte / 新浪科技，2006-09-15：
  - https://tech.sina.com.cn/roll/2006-09-15/1123100442.shtml
  - **B：同期产品报道。**

2008 年 Google 中国官方博客则明确展示：

- 公交路线；
- 地铁；
- 每段站点和距离；
- “较快捷”；
- “少换乘”；
- 驾车路线；
- 跨省驾车。

来源：

- Google 中国官方博客，2008-09-01：
  - https://china.googleblog.com/2008/09/blog-post_1940.html
  - **A：同时代官方功能说明。**

这说明路线不是简单数据库字段，而是计算结果。

增加：

## `route-engine state loss / 路由引擎状态丢失`

一次 route result 至少依赖：

```text
origin
+
destination
+
transport mode
+
road / transit graph version
+
route cost function
+
transfer rules
+
possibly traffic / closure state
+
algorithm version
```

只保存结果 HTML，不足以复现当时为什么给出这条路线。

---

## 十、`result reproducibility gap / 结果可复算缺口`

对于普通静态文章，archive 最重要的是“显示了什么”。

对于路线服务，还需要区分：

### preserved result

某次用户查询的具体结果页面被保存。

### reproducible result

今天在历史环境中重新提交相同起终点，仍可由历史 backend / snapshot 数据生成同一结果。

两者通常不相等。

因为历史路由 backend 往往已经消失。

所以 OWA 将来若拿到一个 2008 route-result capture，应只声称：

> “该 capture 保存了这一时刻的一个 route-result representation。”

不能自动声称：

> “2008 路由服务已经被完整恢复。”

---

## 十一、PC Web 地图还有一个很容易被 archive 忽略的“打印态”

早期在线地图常被用来：

```text
电脑上查
→ 打印
→ 离开电脑
→ 带纸出门
```

这意味着同一服务可能至少有：

- interactive screen representation；
- print stylesheet / print page；
- route text；
- map overview；
- turn list。

海外有一份很强的实物类比：UNT Libraries 保存了 2004-04-15 一份 9 页 MapQuest Dallas→Austin 打印路线。

- https://digital.library.unt.edu/ark:/67531/metadc980091/
- **A：历史打印 artifact。**

OWA 不把这个美国对象写成中文旧网案例，但它提醒我们：

## `print-state preservation / 打印态保存`

可能比 interactive route page 更接近某些用户真正带离电脑的历史界面。

因此将来若发现中文地图站 `print`, `printmap`, `routeprint` 等历史 URL，应单独登记，不应只当重复页面。

---

## 十二、2006 “小Me”：地图体验不一定发生在浏览器 tab 里

2006 年 Mapbar 发布 264K 的免安装桌面地图客户端“小Me”。同期报道说：

- 下载 / 复制到桌面即可使用；
- 无须安装注册；
- 可查公交线路、驾车路线和其他地图信息。

来源：

- 新浪科技，2006-07-20：
  - https://tech.sina.com.cn/other/2006-07-20/15061047598.shtml
  - **B：同期产品报道。**

因此又出现一个 OWA 边界：

> **old Web service != browser-only experience**

一个中文在线地图平台可能同时通过：

- browser；
- small desktop client；
- WAP / mobile app；
- call center；
- PDA；

访问同一或相关地图数据库。

这与前几轮“跨通道发布 / 查询”研究相呼应。

增加：

## `client-surface plurality / 客户端表面复数性`

恢复 Web 页面并不能恢复整个历史服务。

---

## 十三、2008：同一个地图系统同时存在 PC 与手机两种时间结构

Google 中国官方博客 2008 年 9 月的一篇第一人称产品文章特别有用。

作者写到：

- 过去会问路，但仍会坐错公交或绕路；
- PC Web 地图可以先规划路线；
- 但需要一台能上网的 PC；
- 手机地图把路线规划移到“任何时间、任何地点”。

来源：

- https://china.googleblog.com/2008/09/22_2361.html
- **A-source / contemporaneous self-report：官方博客内员工自述，兼有营销选择偏差。**

这给 OWA 一个很具体的 reproduction requirement：

同一数据服务在：

```text
PC Web browser
```

和：

```text
2008 mobile client
```

上不是同一个历史体验。

要记录：

- viewport；
- input method；
- network bandwidth；
- device location availability；
- GPS / cell positioning；
- map cache；
- route display density；
- battery / data cost；
- PC 与 mobile 的功能差异。

M3 将来不应只做 desktop IE / Netscape 比较。

---

## 十四、地图 API 会让历史页面依赖另一个已经消失的平台版本

2008 年 Google 中国官方博客已经鼓励用户把春运地图通过 iframe 嵌入自己的网页 / 博客，并提供具体嵌入代码；同期还有中文地图 API 文档和开发者生态。

来源：

- Google 中国官方博客 2008 年 1 月 archive page：
  - https://china.googleblog.com/2008/01/
  - **A：同时代官方页面；能证明当时存在地图嵌入实践。**

这意味着 OWA 研究一个 2008 个人博客时，页面里即使只有一段 iframe / JS：

```text
<iframe src="http://ditu.google.cn/...">
```

真正地图内容可能全部属于外部平台。

于是出现：

## `embedded-map dependency gap / 嵌入地图依赖缺口`

主页面存活，第三方地图平台死亡后，历史页面会留下一个空洞。

这和 Flash / 图片 CDN 丢失相似，但更复杂，因为地图 iframe 后面还有动态查询和数据版本。

---

## 十五、POI 不是地点本身：`POI-to-place gap`

在线地图越来越把地图与本地生活搜索结合。

2006 Mapbar 已经有：

- 餐饮；
- 休闲；
- 医药；
- 旅游；
- 房屋租售；
- 票务；
- 用户标注 / 分享地点。

2009 Google 中国也公开把餐饮、购物、旅游、娱乐等生活信息叠加到地图平台。

这提示：

```text
POI record
!=
physical establishment
```

一个 POI 可能：

- 已倒闭但 record 仍在；
- 已搬迁；
- 电话更新；
- 名称改变；
- 坐标只是建筑中心；
- 入口在另一条路；
- 同名多店。

因此增加：

## `POI lifecycle state / POI 生命周期状态`

历史 capture 只能证明平台在该 representation 中显示了这个 POI，不能自动证明该店在 capture 当日实际营业。

与 classifieds 一样，需要避免把 representation state 当成 real-world transaction state。

---

## 十六、2019/2024 的生活证据告诉 OWA：地图最难保存的是“规则和熟路”

虽然 OWA scope 的主对象到约 2015，但后来的生活材料可以反向暴露旧网档案缺什么。

2019 年望京外卖骑手同期报道记录，熟练骑手知道：

- 哪些门禁坏；
- 哪些小路和夜路更快；
- 哪些地方导航不如长期经验精确。

2024 年北京“骑手友好社区”又通过：

- 小区路线图；
- 出入口标识；
- 物业通行机制；
- 平台端出入口更新；

解决最后几百米问题。

来源见 HPL 交叉笔记。

这说明历史 Web 地图就算完整，也可能从未包含：

- 门禁；
- 临时封路；
- 园区内部权限；
- 建筑真实入口；
- local shortcut；
- security enforcement。

因此增加：

## `access-rule invisibility / 进入规则不可见`

地图 archive 天生更擅长保存 formal geography，而不是 operational geography。

---

## 十七、建议的历史地图 evidence object

以后若取得真实历史地图 capture，不应只写一条 URL。

建议 evidence 记录：

```yaml
platform: go2map|mapbar|sogou-map|google-cn-map|other
page_type: home|poi|route|transit|print|embed|api-demo
original_url:
capture_url:
capture_datetime:
accessed_at:
http_replay_state:
content_type:
charset:

query:
  raw_text:
  origin:
  destination:
  mode: transit|drive|walk|unknown
  options:

viewport:
  center:
  zoom:
  dimensions:

map_data:
  visible_version_marker:
  provider:
  tile_hosts: []
  tiles_verified: []
  live_contamination: unknown

routing:
  result_visible: false
  result_text_preserved: false
  route_overlay_preserved: false
  backend_reproducible: unknown

runtime:
  js_preserved: false
  api_dependency:
  plugin_dependency:
  browser_assumption:

missing:
  - ...

evidence_grade:
confidence:
```

这里的重点是明确区分：

- shell；
- data；
- computation；
- interaction state。

---

## 十八、reconstruction 的最低边界

地图 reproduction 特别容易制造“看起来很真”的伪历史页面。

例如：

1. 拿到 2006 Mapbar screenshot；
2. 今天用 OpenStreetMap / 当前道路数据做一张相似底图；
3. 套上旧 logo 和搜索框；
4. 页面视觉上很像。

这种东西最多是 **D 级 reconstruction**。

必须显式写：

```text
historical shell basis
historical map-data basis
modern substituted basemap
modern route engine
modern POI data
missing original tiles
missing original JS
```

绝不能称作“2006 Mapbar 已恢复”。

---

## 十九、隐私边界：路线查询也可能是个人位置数据

历史地图看起来不像婚恋或邮件那样敏感，但 route query 可能暴露：

- 家庭地址；
- 工作地点；
- 医院；
- 学校；
- 规律路线；
- 某人在某天准备去哪里。

因此：

- 不批量收集普通用户历史路线 URL；
- 不因 query string 可见就重新结构化个人住址；
- 做 reproduction 优先使用 synthetic origin / destination；
- 使用公开机构、车站、地标作为路线测试点；
- 用户自述只保留支持研究 claim 的最小必要信息。

---

## 二十、当前 artifact / locator 状态

### Go2Map

已确认：

- historical entity identity；
- `http://www.go2map.com` historical locator；
- 2005 SEC A 级官方说明；
- 2004 预生成地图技术的近同时代回顾。

本轮没有取得：

- 一个实际打开并检查过的 1999—2004 Memento；
- 可验证 capture datetime；
- historical HTTP / replay state；
- DOM / charset；
- 完整 tile / rendered-map subresources。

### Mapbar

已确认：

- 2006 contemporaneous `www.mapbar.com` locator；
- 同期首页功能结构；
- 公交 / 驾车 / local search / community 问路存在；
- 2006 desktop client“小Me”存在。

未取得：

- verified 2004—2008 historical Memento；
- historical API / tile manifest；
- browser/JS requirements 的第一方历史文档。

### 搜狗 / Go2Map tile layer

已确认：

- 2013 contemporaneous developer observation 中仍可见 `go2map.com` tile host；
- tile URL 与 zoom/x/y 相关。

未取得：

- 原官方 tile protocol 文档；
- 1999/2004 同一机制的连续证据；
- 已验证 archive tile sample。

因此当前只能写：

```text
historical service identity: ACHIEVED
historical locators: ACHIEVED
contemporaneous workflow/function evidence: ACHIEVED
later-in-scope tile architecture evidence: ACHIEVED
verified 1999-2008 historical map memento: NOT ACHIEVED
verified two historical timepoints for one map site: NOT ACHIEVED
historical route backend reproduction: NOT ACHIEVED
M1 complete case: NOT ACHIEVED
```

**没有取得 validated capture，不等于 archive 当时一定没有保存。**

---

## 二十一、已证实 / 高概率 / 不知道

### 已证实

- 2005 官方资料确认 Go2Map historical URL、在线地图业务及多终端地图平台定位；
- 2006 Mapbar 同期报道确认地图、公交、驾车、本地搜索、站点/线路和问路功能；
- 2008 Google 中国官方资料确认公交/驾车路线计算、少换乘/较快捷等结果形态；
- 2008 同期官方博客确认 PC 路线规划与移动路线规划在历史使用情境上的区别；
- 2013 同时代开发者材料证明搜狗地图当时依赖独立 map tile 请求，且 host 与 URL 结构可以被客户端观察。

### 高概率

- 早期地图站 archive 很可能系统性丢失部分 tile / route backend / query state；
- 同一 historical shell 可能在今天被现代 live map data 污染；
- print page 是早期路线服务重要但容易被研究忽略的页面类型。

这些需要具体 capture 才能升级为个案结论。

### 不知道

- Go2Map 1999 首页真实 DOM、charset、浏览器要求；
- 2004 预生成地图具体 chunk 规格；
- 2005 搜狗地图早期 route endpoint；
- Mapbar 2006 “公交驾车”具体 query URL / method；
- 每代地图实际使用哪些数据版本；
- historical map tile 在 Wayback / Common Crawl 的真实保存率；
- 同一查询跨 2005 / 2008 / 2013 是否能获得可比较结果。

---

## 二十二、下一步最值钱的实验

### Experiment A — 两时点 map shell + tiles

找一个 Go2Map / Mapbar / 搜狗地图 URL，至少两个历史时点：

- 验证 main HTML；
- enumerate visible subresources；
- 标出 map image/tile host；
- 统计 visible viewport 缺失多少 tile；
- 检查 archive replay 是否向 live host 请求。

### Experiment B — historical query preservation

寻找一个当年媒体 / 博客明确链接到的 route / POI query：

- URL 是否携带 query；
- capture 是否保存结果；
- today replay 是否还能显示；
- 是否发生 modern-data contamination。

### Experiment C — print state

搜索：

- `printmap`；
- `print_map`；
- `routeprint`；
- `printRoute`；
- 中文“打印地图 / 打印路线”历史帮助页。

优先找一份中文 Web→纸张的实际 artifact。

### Experiment D — browser/runtime

若取得 2006—2008 map capture，M3 比较：

- modern Chromium；
- IE6 级环境；
- JS enabled/disabled；
- historical screen size；
- HTTP mixed-content assumptions；
- missing tile host。

不要在没有 historical tile/data 的情况下先做“漂亮复原”。

---

## 二十三、这一 note 改变了 OWA 什么

此前动态站研究多集中于：

```text
account
inventory
transaction
payment
relationship
```

在线地图增加了一种不同的旧 Web 对象：

> **页面是一个临时窗口，真正的历史对象是“某版空间数据库 + 某版计算服务 + 某次查询 + 某个 viewport”共同生成的瞬时表示。**

因此以后看到一张保存完好的历史地图首页，不能再问：

> “页面是不是完整？”

而要继续问：

> **“当时那座城市、那条路线、那组公交数据和那次查询，还在不在？”**
