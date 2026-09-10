# MP3 Search, Audio Result, Target File, Player Library and Playlist State Gaps, 2002–2015

## Scope

本文件研究约 2002–2015 中文旧网中的一个具体对象链：

> **用户在网页或播放器中输入一个歌名以后，屏幕上的“搜索结果”怎样（或怎样没有）变成一份真正可播放、可保存、以后还能找回的音频。**

它不是全球数字音乐史，也不把 1980s 磁带、Napster、2020s 流媒体作为本仓主对象。那些跨国前史与 life-history 比较写入 `tmzncty/how-people-lived`；这里仅保留理解中文旧网技术形态所需的边界。

本文件与 `ONLINE_VIDEO_PORTAL_P2P_LIVE_ON_DEMAND_PLAYER_MEDIA_ASSET_AND_ARCHIVE_STATE_GAPS_2005_2015.md` 的区别：视频文件关注 portal/player/live/on-demand 链；这里重点是 **song-level search index、第三方 MP3 URL、榜单、文件身份、本地播放器库与早期在线音乐聚合**。

## 1. 研究单位必须分开

不要把“百度 MP3”“一个搜索结果”“一首歌”“一个 URL”“下载下来的文件”“播放器里的一行”混成同一对象。

至少拆成：

1. **work / composition**：作品；
2. **recording**：某一具体录音；
3. **release/version**：专辑版、现场版、翻唱版、剪辑版等；
4. **metadata record**：歌名、艺人、专辑、时长、码率等；
5. **query**：用户输入；
6. **search index snapshot**：某时刻索引状态；
7. **result item**：结果页中的一行；
8. **target URL**：结果链接指向的地址；
9. **target host/site**：第三方主机；
10. **HTTP retrieval event**：某时刻真正发起的获取；
11. **media bytes**：返回的音频字节；
12. **local file**：保存到用户磁盘的副本；
13. **player library entry**：本地播放器索引记录；
14. **online catalog record**：在线曲库中的歌曲记录；
15. **playlist entry**：账号/播放器内的选择关系；
16. **entitlement/license state**：此用户、此时、此设备是否有权播放；
17. **archive capture**：档案服务保存的一次页面/资源表示；
18. **claim**：研究者据此作出的最小陈述。

## 2. 最小状态链

典型 2000s Web MP3 路径可写成：

`query typed`
→ `search request accepted`
→ `index returns result item`
→ `user selects result`
→ `intermediate/result page loads`
→ `target URL is exposed or invoked`
→ `third-party host resolves`
→ `HTTP request succeeds`
→ `bytes transfer completes`
→ `file is actually audio`
→ `recording matches metadata`
→ `codec/player can decode`
→ `file saved locally`
→ `player scans/imports it`
→ `user renames/tags/sorts it`
→ `file copied to portable device`
→ `later retrieval still possible`。

任何一步都不能由相邻一步自动推出。

## 3. 必须永久保留的 state gaps

### 3.1 `song work != recording`

同一作品可以有：

- 原唱；
- 翻唱；
- live；
- remix；
- demo；
- 剪辑版；
- 错标文件。

历史结果页出现一个歌名，不足以确认具体音频身份。

### 3.2 `metadata label != returned media identity`

文件名和结果标题都可能错误。只有真正检查音频指纹、时长、标签或可核对内容以后，才可把 URL 与具体录音绑定。

### 3.3 `search result indexed != target currently reachable`

搜索引擎索引有时间滞后。结果页可以还显示一个 URL，而第三方文件已经：

- 删除；
- 迁移；
- 403；
- 需要 Referer；
- 域名失效；
- 返回 HTML 错误页；
- 被替换成另一个文件。

### 3.4 `target reachable != transfer complete`

2000s 拨号/ADSL 环境下，连接建立不等于整首歌下载完成。断线、超时和限速都可能产生不完整 artifact。

### 3.5 `HTTP 200 != MP3`

服务器可能用 200 返回：

- 错误 HTML；
- 防盗链页；
- 登录页；
- 重定向脚本；
- 广告页；
- 与文件名无关的内容。

### 3.6 `MP3 extension != valid decodable audio`

扩展名不是 codec 证明，也不是文件完整性证明。

### 3.7 `playable != authentic/correct version`

能播放只证明播放器理解字节；不证明艺人、版本、来源或版权状态。

### 3.8 `search engine result != hosted-by-search-engine`

百度 2006 年 20-F 把 MP3 Search 描述为指向第三方 Internet content provider 文件的 algorithm-generated links。研究写作必须保留 `index authority / media-host authority split`。

### 3.9 `ranking page != stable cultural chart`

百度同期公司文件称热门歌曲和艺人列表可按点击自动更新。某天榜单是一种动态平台状态，不是永恒的“2007 年榜单”。

### 3.10 `right-click/download affordance != same target semantics across dates`

2005 年同期报道记录百度 MP3 页调整：从原先右键下载，变为先打开页面、再点击歌曲链接或来源链接。即使品牌、host 和歌曲名相同，操作链在不同月份也可能不是同一对象。

### 3.11 `search result count != unique recordings`

多个 URL 可能只是同一文件镜像；一个 URL 也可能后来换内容。

### 3.12 `local file != player-library entry`

文件成功落盘后，播放器仍可能需要扫描、导入、读取标签或人工整理。

### 3.13 `player-library entry != file still present`

数据库/播放列表可以保留已经被移动、删除、盘符改变的路径。

### 3.14 `playlist entry != playable item`

进入在线音乐平台阶段以后，歌单里的一行只是关系记录。版权到期、地区限制、会员层级变化、歌曲 ID 合并/拆分都可让它变灰。

### 3.15 `subscription != per-device entitlement`

后来的智能终端可以进一步按设备/渠道拆分权利。这个状态主要作为 2015 以后边界，不用它倒推 2000s Web。

### 3.16 `playlist migration != byte migration`

跨平台迁移通常是 metadata matching：

`source song ID/title/artist`
→ `target catalog search`
→ `candidate match`
→ `new target playlist entry`。

它不是把源平台音频复制到目标平台。

## 4. 同时代证据锚点

### 4.1 2005–2006：百度自己怎样定义 MP3 Search

Baidu 2006 Form 20-F：

- MP3 Search 提供 algorithm-generated links；
- 目标歌曲/多媒体由 Internet content providers 提供；
- 可按 top songs / artists 等分类；
- 这些榜单根据点击自动更新；
- 公司在风险披露中明确担忧第三方 MP3 网站可用性下降会影响该服务。

证据等级：A（公司同期监管文件）。

来源：https://www.sec.gov/Archives/edgar/data/1329099/000119312506133151/d20f.htm

可支持：产品当时如何宣称自己的索引/链接角色。

不可直接支持：每条搜索结果实际合法、准确、可下载；所有用户看到完全同样的页面。

### 4.2 2005：页面操作链发生变化

《新闻晨报》2005-10-26 经搜狐转载的同期报道说，从 10 月 24 日起百度 MP3 搜索网页改变，不再维持此前的直接右键下载路径，而要求在弹出页中点击歌曲/来源链接继续。

证据等级：B。

来源：https://news.sohu.com/20051026/n227310559.shtml

这条材料主要证明：**URL/host 不变时，交互状态机也会改。**

### 4.3 2008：用户工具直接依赖百度 Top500

多特 2008-09-11 教程介绍第三方“百度 MP3 批量下载”软件，目标是一次取得百度排行榜 Top500，并按“歌手-歌曲名”自动重命名。

证据等级：B（同期教程；第三方软件宣称需降权）。

来源：https://www.duote.com/tech/1/600.html

这个 artifact 对 old-Web 很有价值，因为它说明网页榜单不仅被人阅读，还可能成为**机器可消费的上游状态**。页面结构/API 一旦改变，这类工具即可失效。

### 4.4 2008：本地播放器开始把在线推荐嵌进去

cnBeta 2008-05-28 对千千静听 5.2 beta 的试用记录：首次运行会出现每周歌曲推荐，新版加入“音乐窗”，并能把正在播放的歌曲信息发到百度 Hi。

证据等级：B（同期软件评测/用户操作观察）。

来源：https://www.cnbeta.com.tw/articles/soft/56654.htm

这提示研究单位开始从：

`browser search page + external player`

逐步变成：

`player UI + online catalog/recommendation + social status`。

不能因为今天它们都叫“音乐 App”就抹平这次整合。

### 4.5 2009：Google China 的另一种 Web 音乐搜索模型

《北京晚报》2009-03-31 同期报道 Google 中国上线正版免费音乐搜索，初期 35 万首、计划全曲库 110 万首，以广告收入向版权方分成。

证据等级：B（同期新闻，对曲库规模仍是发布方口径）。

来源：https://ent.sina.com.cn/c/2009-03-31/10552448258.shtml

它说明“音乐搜索”这个表面相似的页面类别底层可能完全不同：

- 搜第三方公网 MP3 URL；
- 搜合作版权库；
- 返回可试听对象；
- 返回可合法下载对象。

研究者必须针对具体日期和具体 service model 判断。

## 5. 旧网考古特别容易犯的错误

### 错误 A：从一张百度 MP3 首页截图推断歌曲可下载

首页/搜索框只能证明入口存在。

要证明可下载至少还需要：

- query/result page；
- target URL；
- 当时 target 的响应；
- 最好有 media artifact 或同期用户操作证据。

### 错误 B：archive 里出现 `.mp3` URL 就把它当历史原音频

需要检查：

- archive 是否真的 capture 了 media response；
- replay 是否从现代 origin 补取；
- MIME/Content-Type；
- 长度；
- 重定向；
- 是否为错误页；
- 是否是同一具体录音。

### 错误 C：把今天仍活着的转载页当作 2005 页面界面证据

同期新闻 survivor 可以证明当时有人报道某操作，但当前渲染的 CSS、导航、广告和移动模板属于今天/后来，不得回写成 2005 UI。

### 错误 D：把“Top500”当成一个固定文件

动态榜单是：

`ranking algorithm + query/click log + cutoff time + current catalog/index`。

只保存 HTML 可能只保存某一瞬间结果。

### 错误 E：把一个歌单链接当作文化对象本身已经保存

歌单页面可能还在，但：

- 曲目 ID 已变；
- 部分曲目下架；
- 评论删除；
- 用户私有化；
- 原顺序丢失；
- 页面动态 API 不回旧状态。

## 6. Archive asymmetries

### 6.1 `search-shell survival / target-audio loss asymmetry`

最容易被 crawler 保存的是：

- Logo；
- 搜索框；
- 帮助文字；
- 结果页 HTML；
- 热榜标题。

最容易丢的是：

- 第三方 MP3 原始 bytes；
- 临时/动态 URL；
- Referer/cookie 条件；
- 当时 DNS 与 host 配置；
- 播放器内部在线接口。

因此历史页面可以“看起来完好”，实际最重要的可听对象已经全死。

### 6.2 `ranking capture / ranking process loss asymmetry`

某天榜单快照可以保存；产生榜单的点击日志、去重规则、反作弊和更新周期通常不保存。

历史学家可以说“这个 capture 当时显示 X”，不能由此直接说“X 是全国第 N 热门歌曲”。

### 6.3 `metadata survival / media-identity loss asymmetry`

文本歌名、艺人名特别容易被索引和存档；真正证明是哪个录音版本的音频本体、hash/指纹却更容易丢。

### 6.4 `player-binary survival / service-backend loss asymmetry`

千千静听、酷狗、酷我等某个旧安装包即使幸存，也不保证：

- 原域名仍解析；
- 推荐/搜索 API 存在；
- TLS/证书兼容；
- 登录可用；
- 远程歌词/榜单仍返回历史格式。

“旧客户端能启动”不等于“旧在线音乐世界可复原”。

### 6.5 `playlist-shell survival / entitlement-state loss asymmetry`

平台页面可以留下歌名列表，但历史授权状态往往没有独立 capture。一个 2015 歌单今天变灰，不足以证明 2015 当时也不可播；反过来也一样。

## 7. 建议 evidence record

对历史 MP3 搜索结果至少记录：

```yaml
platform:
host:
original_url:
capture_url:
capture_datetime:
query:
result_rank:
displayed_title:
displayed_artist:
displayed_format:
displayed_size_or_bitrate:
target_url:
target_host:
intermediate_page: true|false|unknown
archive_retrieved_target: true|false|unknown
http_status:
content_type:
content_length:
media_hash:
audio_identity_verified: true|false|unknown
identity_method:
rights_claim_visible:
page_charset:
client_or_browser_assumption:
evidence_grade:
confidence:
notes:
```

对播放器/在线曲库再增加：

```yaml
client_name:
client_version:
local_file_path_semantics:
online_catalog_entry:
playlist_storage_local_or_account:
login_required:
recommendation_surface:
remote_api_host:
remote_api_observed_or_inferred:
```

## 8. 与 `how-people-lived` 的交叉接口

生活史仓库关心：

- 广播/磁带时代怎样发现音乐；
- 2000s 搜索怎样降低歌曲寻址成本；
- 校园/网吧/家庭带宽差异；
- 本地音乐收藏怎样跟着一个人迁移；
- 2010s 版权分片怎样造成平台锁定；
- 2020s 歌单迁移为何成为“退出成本”问题。

本仓只提供中文旧网的技术证据边界：

> **页面显示什么、目标对象在哪里、哪一步需要第三方服务、哪些状态 crawler 根本看不到。**

交叉专题：
- `tmzncty/how-people-lived/topics/from-radio-request-and-mp3-search-to-playlist-portability-music-addressability-and-cultural-exit-china-1980-2026.zh-CN.md`

## 9. 本轮 archive 检查与负结果

本轮通过公开搜索尝试寻找：

- `mp3.baidu.com` 2005–2009 historical capture；
- Google China 音乐搜索历史 capture；
- 能同时连到历史 target audio 的搜索结果页。

当前检索没有返回一个可实际核验、并同时满足以下最低条件的 M1 artifact：

- exact original URL；
- exact capture URL；
- capture datetime；
- replay/HTTP 状态；
- charset；
- DOM/结果字段；
- target URL；
- target/subresource 是否独立保存；
- 第二历史时点可比较。

对 Wayback CDX 的直接打开在当前检索环境中未形成可核验结果。这是**工具/检索路径上的负结果**，不是 archive coverage 的实体断言。

因此本轮结论为：

> **M1 verified historical Chinese MP3-search result + target-audio capture pair: NOT ACHIEVED IN THIS SLICE.**

不得改写成“Wayback 没保存百度 MP3”。

## 10. 下一步最值钱的 M1 case

优先不是再写一篇百度音乐史，而是取得一个**可重放的事务对**：

1. 2005–2009 某次百度/Google 音乐 query page；
2. 精确 result row；
3. 精确 third-party target；
4. 同日/近时 media capture 或明确缺失；
5. 第二时点再次查询同一歌曲；
6. 比较：result rank、URL、host、文件身份、页面 charset、浏览器要求和 target 可用性。

如果能再配一个同期教程/论坛帖子，就能第一次把：

`页面宣称`
→ `用户实际点击`
→ `网络返回`
→ `本地文件`

连成完整证据链。

## 11. 已证实 / 高概率 / 不知道

### 已证实

- 2006 年百度监管文件将 MP3 Search 描述为算法生成的第三方音频链接，并有点击驱动的热门歌曲/艺人列表。
- 2005 年同期媒体记录过百度 MP3 下载交互链的页面调整。
- 2008 年存在依赖百度 Top500 的第三方批量下载工具教程。
- 2008 年千千静听评测已出现播放器内在线推荐/音乐窗。
- 2009 年 Google China 存在以版权合作为基础的免费音乐搜索服务。

### 高概率但本文件不升级为 A

- 普通用户经常把搜索结果下载到本地播放器/MP3 设备；已有大量同期教程支撑，但不同人口与场景分布仍需定量/生命史材料。
- 许多第三方音频 target 随站点关闭和 URL 变化已经失效；这是合理机制判断，但必须逐 URL 核验。

### 仍不知道

- 某一历史日期一个具体百度 MP3 query 的完整 DOM、charset 与结果排序；
- 某个结果实际返回的具体音频 hash；
- archive 对目标 MP3 bytes 的系统性保存率；
- 搜索页调整在不同浏览器/地区/登录状态下是否完全一致；
- 2002–2004 早期 MP3 搜索页面的稳定 URL pattern。

## 12. 核心方法结论

MP3 搜索是一个极好的旧网陷阱：

> **最容易保存的是“这里曾经有一首歌”的文字，最难保存的是当年点击那一刻真正传过来的那串声音。**

页面、索引、第三方主机、文件、本地播放器和后来歌单属于不同状态域。只有把它们分开，才能避免把一个幸存的搜索结果页误写成“历史音频仍然存在”，也避免把今天还能找到的同名 MP3 冒充二十年前那个 URL 实际发出的原始字节。
