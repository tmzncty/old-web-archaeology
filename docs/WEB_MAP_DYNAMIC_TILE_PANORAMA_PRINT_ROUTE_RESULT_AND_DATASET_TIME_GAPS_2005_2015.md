# WEB_MAP_DYNAMIC_TILE_PANORAMA_PRINT_ROUTE_RESULT_AND_DATASET_TIME_GAPS_2005_2015

> Status: incremental archaeology package — not a second general online-map history
>
> Date: 2026-09-09
>
> Parent note: [`ONLINE_MAPS_LOCAL_SEARCH_ROUTE_PLANNERS_AND_REAL_WORLD_EXECUTION_STATE_GAPS_1999_2015.md`](ONLINE_MAPS_LOCAL_SEARCH_ROUTE_PLANNERS_AND_REAL_WORLD_EXECUTION_STATE_GAPS_1999_2015.md)
>
> Cross-repo life-history parent: `tmzncty/how-people-lived/topics/searchable-city-routefinding-local-search-and-navigation-china-1983-2026.zh-CN.md`
>
> New life-history evidence addendum: `tmzncty/how-people-lived/topics/searchable-city-operational-map-navigation-dependency-and-movement-exhaust-evidence-addendum-2026-09-09.zh-CN.md`

## 0. 查重与本稿边界

本轮重新读取 `README`/`AGENTS`/`ROADMAP`/`RESEARCH_PLAN`/`docs/METHOD.md`/`docs/PRIOR_ART.md` 和当前专题树后，确认仓库已经存在一篇较完整的：

- `ONLINE_MAPS_LOCAL_SEARCH_ROUTE_PLANNERS_AND_REAL_WORLD_EXECUTION_STATE_GAPS_1999_2015.md`

它已经覆盖：

- 1999 中文在线地图与插件依赖；
- Go2Map / local search / POI；
- geocoding；
- route planner；
- dynamic map capture；
- JavaScript；
- transit dataset；
- Web/mobile boundary；
- real-world execution gap。

因此本轮**不保留第二篇重复的 broad map note**，只处理父稿仍值得深化的四个 artifact-level gap：

1. **tile temporal mosaic / 图块时间拼贴**；
2. **panorama double-time / 实景双时间**；
3. **print-route portability / 打印路条作为动态路线的静态可携带快照**；
4. **route-result / dataset-time separation / 路线结果与数据有效时间分离**。

并记录本轮对 Mapbar / Mapabc historical replay 的实际负结果。

本稿继续遵守 `docs/METHOD.md`：

```text
platform
!= site/host
!= page/URL
!= query instance
!= backend result
!= capture/memento
!= claim
```

以及：

```text
candidate archive locator
!= verified historical capture
```

---

## 1. 新证据锚：2008 用户已经把几个地图后端当成不同能力源

2008-04-24，博客园用户 KymoWang 留下同时代记录：最早使用 668map，后来常用 Mapbar 与 Mapabc，认为公交更新不如 8684；当天查询北京酒仙桥时又发现 City8 的 360° 实景。

来源：

- <https://www.cnblogs.com/Kymo/archive/2008/04/24/1170077.html>
- grade: **A，同时代公开第一人称；单个用户，不代表总体**

对 old-Web archaeology 来说，这条材料的价值不是“哪个地图最好”，而是证明一个真实工作流可能跨多个 host：

```text
mapbar.com / mapabc.com
→ generic basemap + route

8684.cn
→ transit freshness preferred by this user

city8.com
→ panorama / visual verification
```

所以以后重建“一个人 2008 年怎样查到酒仙桥”时，不能假定全部状态都在一个平台里。

应该允许：

> **one real-world task → several Web evidence systems**

这与仓库现有 cross-platform channel-switching 方法一致。

---

## 2. Tile temporal mosaic：一张历史地图可以同时来自多个日期

父稿已经指出 dynamic-map capture 往往只保住 shell，而 tile、overlay、backend 会丢失。本轮再加一个更严格的时间模型。

假设 archive replay 看起来显示一张 2008 年地图：

```text
main HTML capture:      2008-04-01
client JS capture:      2008-05-20
northwest tile:         2008-03-12
northeast tile:         2008-04-03
southwest tile:         missing
southeast tile:         2008-06-11
marker image:           live current server
route overlay:          missing
```

视觉上它可能仍像“一张地图”，但历史上其实是 **tile temporal mosaic / 图块时间拼贴**。

### 2.1 最低 tile evidence 字段

未来 map case 建议增加：

```yaml
map_shell_capture_datetime:
tile_url_pattern:
tile_scheme_known:
zoom_level:
viewport:
tiles:
  - original_url:
    capture_url:
    capture_datetime:
    http_status:
    image_format:
    archive_rewrite_observed:
missing_tile_count:
mixed_capture_times: true|false|unknown
labels_baked_into_tile: true|false|unknown
route_overlay_mode: server_image|client_vector|unknown
```

### 2.2 一张完整 screenshot 不能升级成完整 dataset

即使截图里 viewport 正常，也只能证明：

> 某一时点、某一视野里出现了这一组合。

不能推出：

- 其他 zoom 完整；
- pan 后完整；
- 全国 coverage 完整；
- route backend 完整；
- tile 与 POI 属于同一数据版本。

因此建议增加 claim：

```text
viewport visually complete
!= map service historically complete
```

---

## 3. Panorama double-time：页面时间和街景拍摄时间不是一回事

2008 KymoWang 的同期材料证明 City8 360° 实景已经进入至少一名中文用户的地点查询流程。

但 panorama artifact 至少有两种时间：

```text
viewer/page capture datetime
!= street imagery acquisition datetime
```

甚至还可能有：

```text
panorama index database update datetime
viewer JS version datetime
image cube resource capture datetime
```

### 3.1 最小状态机

```text
POI / coordinate known
→ panorama coverage exists
→ panorama index resolves
→ image set loads
→ viewer runs
→ orientation metadata loads
→ user maps imagery to physical street
```

硬边界：

```text
panorama viewer shell survives
!= panorama image set survives
!= orientation metadata survives
!= imagery acquisition date known
!= imagery represented street state at page capture date
```

### 3.2 为什么这对历史解释危险

如果 2009 的 archive 页面调用了 2007 拍摄的街景，它保存的是：

> **2009 可访问的、2007 空间表示。**

不能直接写成：

> “这就是 2009 年街道的样子。”

反过来，今天 replay 里若被 live API 污染而出现 2026 imagery，也不能把 current imagery 当历史子资源。

---

## 4. Print route：动态路线的离线快照可能比地图本身更容易保存

父稿已讨论 printable directions，但本轮将它提升为独立 preservation object。

北京日报的历史数据库整理记录：2004 年北京数字信息亭正式开通 312 个点位，可查公交并打印“路条”。

来源：

- 北京日报客户端历史整理：<https://xinwen.bjd.com.cn/content/s67bfa0a8e4b068c68f104f2d.html>
- grade: **B/C**，后来报社数据库回引 2004-06-24 原报；本轮未直接取得原版扫描

对 2005—2015 Web map，也应主动寻找：

- `print`；
- `routeprint`；
- `printmap`；
- printable text itinerary；
- static map image；
- email route；
- share route。

### 4.1 为什么 print artifact 值得优先找

典型 transaction：

```text
route query
→ route backend result
→ print view
→ browser print stylesheet / simplified HTML
→ paper
→ user leaves networked terminal
```

相比动态地图，print view 常常：

- 文字更多；
- JS 更少；
- tile dependency 更少；
- 有独立 URL；
- 更可能被邮件、论坛、博客重新链接。

因此 **print route 是 route-result preservation 的高价值旁路**。

### 4.2 仍然不能过度解释

```text
print view archived
!= user physically printed it
!= user carried it
!= route was current
!= user arrived
```

archive 能证明的是 route representation，不是现实执行。

---

## 5. Route result 的六种时间必须分开

父稿已经要求记录 map-data vintage；本轮进一步把时间拆成最小集合：

```text
T_page      = page publication / shell version time
T_capture   = archive capture time
T_query     = user query time (often unknown)
T_generate  = route engine result generation time (often unknown)
T_dataset   = road/transit/POI data valid time (often unknown)
T_travel    = user actual trip time (usually unknown)
```

最常见的 archive 只有 `T_capture`。

### 5.1 不允许从 T_capture 推断 T_dataset

一个 2008-04-01 capture 不代表：

> route graph 就是 2008-04-01 最新现实。

后台数据可能：

- 一周前；
- 一月前；
- 某城市更新周期更慢；
- 不同 layer 有不同版本。

2008 KymoWang 对公交更新速度差异的观察，以及后来用户对封路更新延迟的抱怨，都说明 **data freshness 是经验变量，不是常数**。

### 5.2 历史 URL + live backend 是污染，不是恢复

若一个旧 route URL 今天还能打开，但返回当前路径：

```text
historical URL
+ current POI resolver
+ current road graph
+ current renderer
```

应标：

> **live-current contamination / current backend rehydration**

绝不能叫 historical route replay。

---

## 6. Query encoding：中文地名本身就是历史协议状态

早期中文地图 query 可能经过：

```text
page charset (GB2312/GBK/UTF-8)
→ browser form encoding
→ percent encoding
→ JS escape()/encodeURIComponent()
→ backend decoder
→ geocoder normalization
```

因此一个今天仍看得到的 form 可能：

- 能输入“酒仙桥”；
- 但 archive rewrite 后提交乱码；
- 或 historical endpoint 已死；
- 或浏览器默认编码与当年不同。

应继续坚持：

```text
form visible
!= historical query executable
```

未来 case 可记录：

```yaml
page_charset:
form_accept_charset:
method:
action_url:
js_serializer:
sample_raw_query:
sample_encoded_query:
backend_decoder_known:
modern_replay_result:
historical_browser_result:
```

这类字段很适合 M3 浏览器环境实验。

---

## 7. Mapbar / Mapabc：本轮 historical replay 的实际负结果

### 7.1 已确认的 historical host evidence

2008 KymoWang 的同期第一人称明确写到：

- `mapbar.com`；
- `mapabc.com`。

2006 Mapbar 产品报道又独立证明其公交/驾车 route query 能力。

来源：

- <https://www.cnblogs.com/Kymo/archive/2008/04/24/1170077.html>
- <https://tech.sina.com.cn/other/2006-07-20/15061047598.shtml>

因此 historical主体/功能存在已有 A/B evidence family。

### 7.2 本轮尝试

本轮尝试直接打开约 2008 年的构造 Wayback replay：

```text
https://web.archive.org/web/20080401000000/http://www.mapbar.com/
https://web.archive.org/web/20080401000000/http://www.mapabc.com/
```

当前研究访问链对这些未经搜索结果产生的构造 archive URL 执行 safety restriction，未返回可实际检查的 memento。

因此严格记录：

```text
M1 verified Mapbar historical capture:
NOT ACHIEVED IN THIS SLICE

M1 verified Mapabc historical capture:
NOT ACHIEVED IN THIS SLICE
```

这只表示：

> **本轮没有获得可以逐项检查 original URL / capture URL / capture datetime / HTTP / charset / DOM / subresources 的合格历史快照。**

绝不表示：

> “Wayback 没有保存 Mapbar / Mapabc。”

这符合 `docs/METHOD.md` 的负证据规则：`没有找到 != 当时不存在`，locator 未实际检查不能升级成 capture。

### 7.3 下一步证据路径

下一轮若继续地图 case，应优先：

1. 从普通 Web 搜索先取得明确 archive locator，再 open；
2. 工具允许时查 Internet Archive CDX；
3. 查 Common Crawl index；
4. 查 2005—2010 用户教程中的 print route / screenshot / route URL；
5. 针对 City8 单独查 panorama viewer + image assets；
6. 针对 Mapbar/Mapabc 查 JS、tile host、route-result URL pattern，而不是只查首页。

---

## 8. 新增 preservation levels（作为父稿的补充，而不是替换）

父稿已经有完整 state model。本轮建议仅为动态 artifact 增加一组局部等级：

### D0 — product/host evidence only

只知道历史主体/功能曾存在。

### D1 — verified shell memento

实际检查过 original URL、capture URL、datetime、HTTP/replay 状态。

### D2 — shell + static assets

CSS/icon/主要静态图片可定位。

### D3 — tile sample with per-resource time

能记录一个 viewport 中的 tile URL 与各自 capture datetime，并明确是否 mixed-time。

### D4 — query serialization verified

能核验 form/JS/charset 如何把中文地名编码进请求。

### D5 — historical result artifact verified

有一份历史 route/POI result，而不是 current backend 重新生成。

### D6 — print/share artifact verified

历史 route 的打印/分享表示可独立核验。

### D7 — panorama artifact partially verified

viewer/index/image set 至少两层可核验，并分别记录 page/image time。

### D8 — cross-source constrained reconstruction

archive artifact + 同期用户/教程/新闻至少两个 evidence family 互相约束；任何现代补全继续显式标 reconstruction。

D8 仍不能证明现实中的用户没有迷路。

---

## 9. Archive gap 新增字段

建议父稿未来 evidence schema 增加：

```yaml
page_capture_datetime:
query_datetime:
result_generation_datetime:
dataset_valid_datetime:
travel_datetime:

map_asset_model:
  tile|server_image|vector|unknown

tile_capture_times:
mixed_tile_times:

panorama:
  viewer_capture_datetime:
  imagery_acquisition_datetime:
  index_capture_datetime:

print_route:
  available:
  url:
  capture_datetime:

live_current_contamination:
  observed:
  current_endpoint:

route_backend_archived:
geocoder_archived:
transit_dataset_archived:
```

没有证据时必须保留 `unknown`，不要用当前地图反填历史值。

---

## 10. 隐私边界

地图 artifact 的高等级 preservation 不要求恢复真实普通人的私人路线。

不应为了“完整”重新公开：

- home/work 地址；
- 医疗路线；
- 私人约会地点；
- 历史 location sharing；
- 收藏地点；
- 可识别个人的精细轨迹。

高价值 artifact 是：

- demo route；
- public-service route；
- 新闻/教程里公开的非敏感样例；
- URL pattern；
- query schema；
- print view；
- tile/charset/browser behavior；
- aggregate data。

这与 `docs/METHOD.md` 的研究必要最小化一致。

---

## 11. 已证实 / 高概率 / 不知道

### 已证实

- 2008 至少一名中文用户实际跨 Mapbar/Mapabc/8684/City8 完成不同层面的地图核验；
- 360° 实景已经进入至少一个真实查询流程；
- 2004 北京公共信息亭已经存在公交查询→打印路条这种“动态查询→离线携带表示”的制度前身；
- Mapbar/Mapabc historical host 可由同时代用户材料确认；
- 本轮没有成功验证它们的一份 Wayback memento。

### 高概率但仍需 capture

- 2005—2010 Mapbar/Mapabc 存在独立 route-result/print/share URL 或参数化结果页；
- 图块/JS/route backend 的 archive 覆盖显著不均；
- panorama viewer 与 image set 的保存状态会明显分离；
- 中文 query encoding 是现代 replay 失败的重要来源之一。

### 不知道

- Mapbar/Mapabc 2008 canonical route query schema；
- route engine 当时的数据版本；
- tile host/path 的版本变迁；
- City8 panorama imagery 的拍摄日期和 archive coverage；
- print route 的实际保存率；
- 同一个 route result 在 Wayback/Common Crawl 中是否有独立响应命中。

---

## 12. 本轮对 old-Web archaeology 的真正新增

父稿已经正确指出：

> **archived map page != archived city != archived route engine != real-world arrival.**

本轮把这条原则再往 artifact 内部拆细了一层：

> **即使“地图图像”看起来活着，它也可能是多个 capture 日期的 tile 拼贴；即使“实景”活着，页面日期与影像拍摄日期也可能不同；即使 route URL 活着，当前后端重新计算出来的路线也不是历史路线。**

最值得下一步追的因此不是更多地图品牌发布史，而是一次真正可复核的 transaction：

```text
一个 2005—2010 中文起终点 query
→ historical request encoding
→ historical geocoder result
→ historical route response
→ historical print/share representation
→ per-resource capture times
```

只要这条链能拿下一例，就会比再收集十篇“某地图上线”新闻更接近本仓 M1/M3 的研究目标。
