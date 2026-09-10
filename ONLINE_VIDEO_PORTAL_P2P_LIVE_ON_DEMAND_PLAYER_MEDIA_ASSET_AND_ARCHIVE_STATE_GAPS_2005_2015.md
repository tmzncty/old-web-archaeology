# Online Video Portal, P2P Live, On-Demand, Player, Media Asset and Archive State Gaps（中文 Web，2005—2015）

> **范围声明**：本文只研究约 2005—2015 中文互联网里的网络电视、视频门户、点播页面、播放器、媒体对象、上传/发布与历史保存状态。1980s 录像机、海外 time-shifting 和 2020s 推荐/短视频只作边界比较，主体不离开本仓的中文旧网 scope。

交叉生活史研究见：

- `tmzncty/how-people-lived/topics/broadcast-schedules-time-shifting-online-video-and-viewing-time-sovereignty-china-1980-2026.zh-CN.md`

本文不回答“网络视频行业什么时候崛起”，而回答一个 old-Web 更具体的问题：

> **当一个历史页面写着“直播”“点播”“播放”“视频已发布”“播放 XX 次”时，我们究竟能证明到哪一层？**

---

## 1. 开工查重与研究边界

本仓已经覆盖：

- 家庭宽带与拨号/ADSL；
- 网吧共享终端；
- 搜索与目录；
- 个人主页和公开自我；
- 在线存储；
- RSS；
- 摄影/音乐/兴趣论坛；
- 旧浏览器与插件环境的一般方法问题。

但没有独立拆解网络视频这一类特别容易被 archive 误读的复合对象。

网络视频和普通静态网页不同，因为“页面存在”只是观看事务中很薄的一层。真正播放往往还依赖：

- 播放器脚本或 SWF；
- Flash / Windows Media / 其他 runtime；
- P2P 客户端；
- 视频 ID 到真实媒体对象的映射；
- API / manifest / stream URL；
- CDN 边缘节点；
- 转码版本；
- 版权和审核状态；
- 实时直播源；
- 用户带宽、编解码器和本机环境。

因此：

```text
historical video page survives
!= historical player survives
!= stream endpoint survives
!= media bytes survive
!= clip was playable at capture time
!= clip is playable today
!= a historical user actually watched it
```

这也是为什么“看到一个旧播放页截图”绝不能自动升级成“历史视频已经复原”。

---

## 2. 研究单位：不要把站点、页面、媒体和观看混成同一个对象

按 `docs/METHOD.md`，至少区分以下层次。

### Platform

例如：

- PPLive；
- PPStream；
- 土豆；
- 优酷；
- 其他中文网络电视/视频门户。

### Site / host

例如主站、播放器域名、静态资源域名、CDN host、接口 host。

### Page / interface

可能包括：

- 首页；
- 频道页；
- 节目表；
- 搜索结果；
- 视频详情/播放页；
- 上传页；
- 播放列表；
- 评论页；
- 客户端下载页；
- 插件升级提示；
- 版权/下架提示。

### Media object

不是 HTML 页面，而是实际被播放器取用的：

- FLV / MP4 / WMV 等视频对象；
- 分片；
- manifest；
- 实时流；
- 转码版本；
- P2P 分发对象。

### Player/runtime

例如：

- Flash Player；
- Windows Media Player；
- 独立 P2P 客户端；
- JavaScript + SWF 壳；
- 浏览器插件。

### Transaction / viewing state

- 用户连接；
- 首帧开始；
- 缓冲；
- 中断；
- seek；
- 完播；
- 评论/评分/收藏。

### Capture

某个 archive 在某个时点保存的页面、脚本、SWF 或媒体对象。

### Claim

例如：

> “2007 年 11 月发布的 PPLive 1.9.15 版本说明明确列出增加点播功能。”

同期版本报道可以支持。

而：

> “某个普通用户 2007 年 12 月 5 日 20:13 在 PPLive 完整看完一集电视剧。”

则需要完全不同的私人日志或事务证据，不能从产品说明推出。

---

## 3. 先拆三种不同的网络视频状态机

## 3.1 Live / P2P network-TV state

```text
现实频道/赛事/节目存在
→ 上游信号在该时刻实际播出
→ 网络电视平台为该频道建立入口
→ 节目表/频道列表向用户显示
→ 用户客户端/浏览器成功连接
→ 中继/P2P peers/服务器可用
→ 解码器与播放器工作
→ 首帧出现
→ 缓冲维持在可接受范围
→ 播放持续
```

必须保持：

```text
channel listed
!= upstream source live
!= stream reachable
!= player starts
!= playback remains continuous
```

直播还天然拥有 **stream-state volatility / 流状态波动**：同一个 URL 在不同分钟可能指向不同节目、不同码率、甚至无信号。

所以 archive 以后保存“频道入口”并不能恢复某个具体时刻的实际直播内容。

## 3.2 On-demand state

```text
视频标题/条目存在
→ video ID 可解析
→ 当前版权/审核状态允许播放
→ 播放页可加载
→ player runtime 可执行
→ API / manifest / stream URL 返回
→ CDN / 媒体对象仍存在
→ 浏览器/插件/codec 可解码
→ 首帧开始
→ 用户可 seek / pause / continue
→ 完播或中途退出
```

核心边界：

```text
page exists
!= video ID resolves
!= rights permit playback
!= player works
!= stream endpoint resolves
!= media bytes exist
!= first frame starts
!= completion occurs
```

## 3.3 UGC upload/publish state

```text
用户选择本地文件
→ upload request 提交
→ bytes 到达平台
→ 文件完整性检查
→ 转码
→ 自动/人工审核
→ publish state
→ 播放页生成
→ CDN/P2P 分发
→ 搜索/首页/相关推荐可发现
→ 实际观看
```

因此：

```text
upload submitted
!= upload completed
!= transcode succeeded
!= moderation passed
!= page published
!= media playable
!= video discovered
!= video watched
```

这条链对于 archive 尤其重要：一个后来还能找到的播放页不能证明原始上传文件仍在，也不能证明历史上所有转码版本都曾同时存在。

---

## 4. 2006：PPLive 显示“网络电视”首先可能只是把电视终端搬到电脑

2006 年对 PPLive 创始人姚欣的同期采访记录：他还是华中科技大学学生时，因为喜欢看足球、寝室里却没有电视，于是开始写 P2P 网络电视软件，让宿舍电脑能够接收电视内容。

来源：

- **A/B（2006 同期创始人采访）**：太平洋电脑网/新浪科技，2006-03-27，《独家专访PPLive创始人姚欣：为看球而生的软件》：<https://tech.sina.com.cn/roll/2006-03-27/1422878883.shtml>

2006 年底 PPLive 的版本报道则明确提到：

- 软件面向 Windows；
- 支持 Windows Media Player 11；
- 使用 P2P；
- 针对 512K ADSL 做过播放优化。

来源：

- **B（2006 同期软件版本报道）**：太平洋电脑网/新浪科技，2006-12-09，《修正卡巴斯基误报：PPLive新版发布》：<https://tech.sina.com.cn/s/s/2006-12-09/1008184600.shtml>

这里需要固定两个 state gap：

```text
broadband subscription exists
!= P2P video is smooth
```

以及：

```text
PC can run client
!= upstream live source exists
!= requested program is available
```

这不是“视频网站已经成熟点播”的证据，而是网络先替代一部分电视接收终端。

---

## 5. 2007：网络电视、循环轮播和真正点播不能混成同一个词

2007 年 6 月《北京青年报》报道住在北京朝阳区出租屋的李非：她头一天晚上错过湖南卫视“快乐男生”直播，第二天下午登录 P2P 视频直播网站，在 PPStream 的循环节目里补看；同一场比赛当天安排了多次重复播出。

来源：

- **A/B（2007 同期普通用户场景）**：《北京青年报》/新浪科技，2007-06-20，《两阵营暗战网络电视 点播成杀手应用》：<https://tech.sina.com.cn/i/2007-06-20/09301572636.shtml>

这条材料说明：

```text
missed original TV broadcast
→ can catch a later network loop
```

已经是一种明显的 time-shifting，但仍不等于真正任意时刻的点播。

同年 9 月同期报道仍明确区分：PPLive 主要提供电视同步直播或电视剧/电影轮播，而 PPStream 已有点播。到 11 月底发布、12 月初报道的 PPLive 1.9.15，更新说明才明确列出“增加点播功能”。

来源：

- **B（2007 同期产品状态）**：新浪科技，2007-09-14，《PPLive获德丰杰千万美元投资》：<https://tech.sina.com.cn/i/2007-09-14/10021740000.shtml>
- **B（2007 同期版本说明）**：小熊在线/新浪科技，2007-12-03，《PPLive V1.9.15 增加点播功能》：<https://tech.sina.com.cn/s/s/2007-12-03/1620507436.shtml>

因此以后遇到 2005—2008 的“网络电视”材料时必须先问：

- 真直播？
- 平台循环轮播？
- 条目式 VOD？
- 本地下载后播放？

不能把所有带播放器的互联网视频都用今天的“点播”概念回写。

本专题把它命名为：

## network-TV / on-demand gap（网络电视 / 点播缺口）

---

## 6. 2007：播放器升级提示本身也是历史证据，但只能证明被提示的那一层

土豆 2007 年 12 月的公司发布称，网站开始使用 H.264 以提高部分视频质量；要观看新的高质量版本，用户需要升级到 Adobe Flash Player 9，未升级者仍可继续观看原有标准质量视频。

来源：

- **A（公司同期技术公告，按公司口径使用）**：Tudou.com, 2007-12-11, H.264 / Adobe Flash Player 9 announcement：<https://en.prnasia.com/releases/global/Tudou_Com_China_s_Largest_Online_Video_Sharing_Site_Brings_Better_User_Experience_To_Its_40m_Visitors_With_Better_Quality_Video_In_Large_Scale-15905.shtml>

这给出一条可以实际固定的 2007 技术状态：

```text
某些 H.264 高质量 Tudou 视频
→ 需要 Flash Player 9
```

但不能扩展成：

```text
2007 Tudou 所有页面都只能 IE 打开
```

或：

```text
整个中文视频网站都必须 Flash 9
```

同样，PPLive 1.9.15 版本说明提到增加 IE 工具栏插件，只能证明该版本包含这项功能；它不能自动证明全部播放流程只支持 IE。

因此 old-Web 中插件证据必须坚持：**exact workflow, exact date, exact product**。

---

## 7. 2005—2011 土豆：观看、注册、上传、评论和“用户数”是不同统计对象

土豆 2011 年向美国 SEC 提交的 Form 20-F 回顾，公司网站于 2005 年 4 月上线，并披露用户可以上传、分享、观看、评分和评论视频。到 2011 年，网站包含分类、关键词搜索、观看历史、Top 10、相关视频和播放列表；播放列表可以连续播放多个视频。

来源：

- **A（公司监管文件）**：Tudou Holdings Ltd., Form 20-F, fiscal year 2011：<https://www.sec.gov/Archives/edgar/data/1499599/000119312512143077/d305513d20f.htm>

同一监管文件明确说明：

- 搜索、观看视频不要求注册；
- 上传、评分、评论、推荐等交互需要注册账户；
- 平台使用 IP 等口径估算 monthly unique visitors，并承认共享 IP 可能让多个人被低估为一个访问者，而动态/变化 IP 又可能让同一个人被高估为多个访问者。

因此必须长期保存：

```text
registered account
!= viewer
!= unique person
```

以及：

```text
IP-based unique
!= human unique
```

这对历史人口推断非常重要。一个大学宿舍、网吧或单位出口后的许多人可能共享公网 IP；同一移动/拨号用户又可能在统计周期里换 IP。

同样：

```text
page view
!= video start
!= unique viewer
!= completed view
```

如果历史页面只留下一个“播放量”，而原始统计口径没有保留，就不能擅自把数字解释成“有这么多人完整看过”。

---

## 8. 播放列表和相关推荐改变观看链，但页面状态仍不能证明连续观看

土豆监管文件显示，用户可以创建播放列表，多个视频可连续播放；平台还会展示相关视频和榜单。

这使观看从：

```text
找一个视频
→ 看一个视频
```

逐渐可能变成：

```text
找一个视频
→ 播放
→ playlist / related video
→ 下一条
```

但 archive 里即使完整保存了 playlist 页面，也只能证明：

- 平台存在这种组织结构；
- 某些条目在当时页面表示中被排进列表。

它不能证明某个用户按顺序全部看完。

因此新增：

## playlist / continuous-watch gap（播放列表 / 连续观看缺口）

---

## 9. “发布一个视频”与“进入公共可见性”之间还有审核、推荐和 CDN

土豆监管文件回顾，公司最初两年几乎全部依赖 UGC；上传后平台要转换视频格式，并进行版权/内容过滤，再通过自身 CDN 与 P2P 分发。平台同时使用首页推荐、Top 10、相关视频等机制提高可发现性。

这里至少要分开：

```text
video uploaded
→ transcoded
→ approved/published
→ playable
→ indexed/searchable
→ recommended
→ viewed
```

所以一个后来在 archive 里“从未搜到”的视频不能自动解释成从未上传；一个有播放页但媒体丢失的视频也不能自动解释成从未成功播放。

### 9.1 生产者侧门：一个网络视频可以先获得观众，再反向获得传统机构机会

2010 年《中国青年报》采访 24 岁李洪绸：他 2008 年从一所民办高校编导专业毕业，自述学历背景使自己和同学在电视台等传统媒体求职时碰壁，于是 5 个年轻人自组团队，把低成本短片上传视频网站。大学时期上传的学生作品曾被推到首页并获得点击分成，后来团队持续制作网络作品，又反向得到电视台合同；2010 年他把下一阶段未来描述为带团队向专业影视公司发展。

来源：

- **A/B（2010 同期第一人称与团队报道）**：《中国青年报》/南开大学转载，2010-10-25，《草根导演将兴趣“玩”成职业》：<https://news.nankai.edu.cn/rwsd/system/2010/10/25/000034443.shtml>

对 old-Web 来说，这条材料证明的是**平台发布和推荐机制确实进入了一条具体职业路径**；它不是那个视频页面本身的 historical capture，也不能用来推断所有 UGC 作者都能职业化。

---

## 10. CDN/P2P 是“看得见的视频页”背后最容易被历史抹掉的一层

土豆 2011 年监管文件披露，公司使用自建 CDN 与 P2P 技术，部署大量服务器，并在部分较小运营商网络中缓存热门内容，以降低延迟和带宽压力；视频上传后还要转换为适合网站播放的格式。2009—2011 带宽成本持续构成平台显著成本。

这让一个 old-Web 视频页至少依赖：

```text
HTML / JS / CSS
+ player runtime
+ API
+ video metadata
+ media manifest / stream URL
+ CDN cache or origin
+ codec/plugin
```

而一般 Web archive 对这些层的保存概率完全不同。

这形成本专题最重要的保存偏差：

## shell-survival / media-asset-loss asymmetry（页面壳存活 / 媒体对象丢失不对称）

二十年后可能出现：

- 标题还在；
- 作者名还在；
- 评论还在；
- “播放”按钮还在；
- SWF 文件也许还在；
- 但真实 FLV/MP4/CDN 对象早已消失。

于是研究者可以非常清楚地看到“人们围绕这段视频做了什么”，却再也看不到视频本身。

这不是 archive 失败的单一异常，而是流媒体对象本来就跨越多层、动态 URL、分发节点与版权生命周期的结构性后果。

---

## 11. 当前 replay 还可能把旧页面接到新后台：不要把今天渲染出的结果倒写回历史

历史 HTML 如果包含：

- 相对 API URL；
- 动态 JavaScript；
- iframe；
- 当前域名下的播放器脚本；
- 当前推荐接口；

archive replay 就可能出现：

```text
historical shell
+ current or missing backend
```

本专题将它命名为：

## historical-page / current-backend rehydration gap

因此真正做 M1 时，不能只看浏览器里“页面能打开”，必须记录：

- original URL；
- capture datetime；
- replay URL；
- HTTP 状态；
- HTML charset；
- 脚本与 SWF 是否来自同一历史时间；
- API 请求是否也被 archive 捕获；
- stream/media URL 是否历史化；
- 当前域名是否被意外访问；
- 页面是否因为现代浏览器禁 Flash 而失真。

---

## 12. 下架与审核制造另一种 archive selection bias

2007 年围绕网络视频内容治理的同期报道已经显示，PPLive 等平台会移除部分内容、调整频道或节目。

来源：

- **B（2007 同期行业/监管报道）**：新浪科技，2007-03-19，网络电视内容整顿相关报道：<https://tech.sina.com.cn/i/2007-03-19/07331421809.shtml>

因此：

```text
video absent from later site
!= video never existed
```

也不能反向写：

```text
video survives in archive
= representative of what was most watched
```

受版权、监管、平台迁移和商业价值影响，某些最热门内容反而更可能被替换、下架或跨站迁移；大量低流量 UGC 又可能因为无人保存而消失。

本专题将它命名为：

## takedown-selection bias（下架选择偏差）

旧网残存样本不是当年内容生态的无偏抽样。

---

## 13. 网络视频已经很大，不等于普通中国家庭都完成了迁移

CNNIC 2008 年 6 月报告显示，中国网民约 2.53 亿，宽带网民约 2.14 亿，但全国 Internet 普及率仍约 19.1%。

来源：

- **A/B（CNNIC 同期统计）**：CNNIC，第22次中国互联网络发展状况统计报告：<https://www3.cnnic.cn/n4/2022/0401/c88-813.html>

这条统计对 old-Web 的用途不是证明具体站点流量，而是给任何“网络视频已经成为普通人的默认观看方式”加上人口边界。

因此：

```text
platform technically available
!= broadband household available
!= suitable PC available
!= actual viewer population universal
```

同样，土豆公司对年轻、城市、受教育用户群的描述只能作为平台自述，不能倒推全国人口结构。

---

## 14. 2008—2015 的移动端不能被倒写成“一开始就是手机视频”

土豆监管文件显示，公司 2010 年开始通过中国移动等渠道扩展移动视频业务，并逐渐把内容带到移动终端。

这至少说明：

```text
desktop web catalog
!= mobile catalog
!= same codec/runtime
!= same rights set
!= same playback success
```

未来遇到同名视频在 PC 页面和手机端都存在时，不能自动假设：

- 视频 ID 相同；
- URL 相同；
- 转码版本相同；
- 授权状态相同；
- 评论和播放量共享同一数据库。

因此新增：

## desktop-catalog / mobile-catalog gap

---

## 15. 一组可复用 state gaps

本专题建议把以下边界长期复用到其他流媒体对象：

| gap | 含义 |
| --- | --- |
| `network-TV / on-demand gap` | 网络电视入口不等于任意时刻点播 |
| `channel-listing / live-source gap` | 频道被列出不等于上游信号此刻有效 |
| `program-schedule / actual-air gap` | 节目表写了不等于现实源按计划播出 |
| `video-page / media-object gap` | 页面存在不等于媒体对象存在 |
| `player-shell / playable-runtime gap` | 播放器壳存在不等于 runtime 可执行 |
| `SWF-player / stream-endpoint gap` | SWF 保存不等于流地址仍可解析 |
| `stream-endpoint / CDN-object gap` | endpoint 返回不等于实际媒体字节仍在 |
| `upload-request / publish gap` | 上传请求不等于公开发布 |
| `publish / rights-survival gap` | 曾发布不等于后来仍有传播权 |
| `registered-user / viewer gap` | 注册账户不是所有观看者 |
| `view-count / completed-view gap` | 播放计数不等于完播 |
| `IP-unique / person gap` | IP 统计不等于真实独立人 |
| `playlist / continuous-watch gap` | 播放列表不等于用户连续看完 |
| `historical-page / historical-stream-state gap` | 页面快照不等于当时实时流状态 |
| `current-replay / current-backend-rehydration gap` | 今天 replay 成功不等于当年后台状态 |
| `desktop-catalog / mobile-catalog gap` | PC 与手机不是天然同一目录/转码/权限 |
| `takedown / original-historical-popularity gap` | 后来缺失不等于当年不重要或不存在 |

---

## 16. 与 Life Horizons 的交叉：观看时间的变化为什么是一种生活基础设施变化

`how-people-lived` 对应专题把历史拆成：

```text
广播时间依赖
→ time shifting
→ schedule sovereignty
→ duration sovereignty
→ stop-time sovereignty
```

old-Web 这边要做的不是重复生活史叙述，而是保证每一个“我可以晚点看”“我可以点播”“我可以连续看”的结论都没有跨越技术状态：

- 2007 的循环重播不能写成成熟 VOD；
- 播放列表不能写成自动完播；
- 一个能打开的页面不能写成视频仍可播；
- 公司披露的带宽/CDN 不能证明某一个普通用户没有卡顿；
- 一个青年创作者被首页推荐不能写成平台给所有人同等曝光。

也就是说，**生活时间主权的扩张，必须落在一串具体可执行技术状态上。**

---

## 17. 证据等级

### A：原始/机构强证据

- Tudou 2011 Form 20-F：平台上线时间、网站功能、注册要求、流量统计口径、自建 CDN/P2P、转码、移动业务、带宽成本等；
- CNNIC 2008 同期统计：Internet/宽带人口边界。

### A/B：同时代人物与产品材料

- 2006 姚欣：寝室没电视，为看球开发 PPLive；
- 2007 李非：错过直播后通过 P2P 平台循环补看；
- 2007 PPLive 产品报道：直播/轮播与点播功能差异；
- 2007 Tudou Flash Player 9/H.264 技术公告；
- 2010 李洪绸：传统媒体求职碰壁后通过视频网站建立制作路径。

### 不能升级的材料

- 公司“最大/第一/年轻人不看电视”之类宣传，不外推到总体人口；
- 今天仍可打开的旧新闻页面不是原视频网站 historical capture；
- 当前视频网站残留 URL 不是 2005—2010 的 historical page state；
- 某个视频标题被搜索引擎索引不等于媒体对象仍可播放。

---

## 18. 反例

1. **Internet 网络电视不等于 VOD**：2007 PPLive 仍主要直播/轮播。
2. **VOD 不等于无需插件/客户端**：2007 高质量 Tudou 视频有明确 Flash Player 9 条件；P2P 电视也依赖本地软件/runtime。
3. **页面保存不等于视频保存**：媒体对象可在另一 host/CDN/动态 URL。
4. **账户很多不等于观看者很多**：观看无需注册；账户可闲置；一人可多账户。
5. **IP unique 不等于真实人**：宿舍/网吧共享出口与动态 IP 都会扭曲。
6. **推荐曝光不等于职业成功**：李洪绸是路径存在证据，不是成功概率估计。
7. **网络视频兴起不等于电视消失**：2008 人口普及边界仍非常明显，直播也持续保留同步价值。

---

## 19. 后见之明风险

### 不要写：“视频网站天生就是点播”

P2P 网络电视中的直播、轮播、点播曾长期并存。

### 不要写：“Flash 页还在，所以视频还在”

HTML、SWF、stream URL、CDN 对象是不同资源。

### 不要写：“今天浏览器打不开，说明当年也打不开”

现代浏览器禁用 Flash、TLS/JS 变化、archive rewrite 都会制造新的失败。

### 不要写：“今天 replay 能打开，说明当年页面就是这样”

必须排除当前 API/JS rehydration。

### 不要写：“播放次数就是观看人数”

计数口径必须单独确认。

### 不要写：“2008 年年轻人都从电视迁往 Internet”

站点样本、公司宣传和人口普及率不能混用。

---

## 20. 本轮 historical capture 状态

本轮围绕：

- `tudou.com`；
- `youku.com`；
- PPLive/PPTV 早期页面；

搜索了历史 locator 与 Wayback 索引线索，但当前可用检索链没有取得一份能够同时核验以下字段的合格 memento：

```text
original URL
capture datetime
HTTP state
charset
DOM
player code
script/SWF dependencies
stream/media URL
subresources
```

因此本轮只能记录：

> **M1 verified Tudou/PPLive historical video-page Memento: NOT ACHIEVED IN THIS SLICE**

这不能写成“Wayback 没有保存”。

同样，本轮没有直接验证 2005—2007 Tudou 播放页的：

- exact charset；
- exact table/div layout；
- exact browser support matrix；
- exact player SWF URL；
- exact media URL format。

这些继续保持 `unknown`。

唯一可以精确固定的是：2007 年 12 月公司公告里，对新 H.264 高质量视频有 Flash Player 9 的明确要求；不能把这一点扩张到更早年份和全部页面。

---

## 21. 下一步如果要把它升级成 M1

优先目标不是再搜十篇行业回顾，而是拿到一套真正的 capture pair：

1. 2006—2007 的 Tudou/优酷/PPLive 一个首页或频道页；
2. 同期一个具体视频/节目播放页；
3. 如果可能，再拿 2009—2011 同一平台的第二时点；
4. 逐项记录 charset、HTML、播放器技术、脚本、SWF、媒体 URL、404/redirect；
5. 至少找一份同期普通用户博客/BBS 描述真实播放环境，与平台技术材料交叉；
6. 不追求复活私人观看历史，只复原公开接口和技术状态。

如果视频字节已经不可获得，也应把“标题/评论/页面壳存活而媒体消失”本身作为 M1 结论，而不是视为案例失败。

---

## 22. 这一专题改变了我们对旧网考古的哪一点理解？

静态旧网页很容易诱导一种错误直觉：只要 HTML 被保存，历史对象就还在。

网络视频恰好把这个直觉击穿。

一个播放页二十年后可能还保存着标题、作者、评论、播放按钮、甚至当年的 Flash 壳；但真正让当年那个学生在宿舍电脑里看到一场球赛的 P2P peers、实时源、转码文件、CDN 节点、播放器 runtime 和版权状态，几乎全部是页面之外的东西。

所以网络视频的旧网史必须区分：

> **“观看这件事曾经有一个网页入口”**

与：

> **“那段影像本身今天仍然可被可靠复原”。**

二者完全不是同一个证据命题。

而这正好和生活史那边互相校正：Internet 的确逐渐让普通人不再必须按电视台节目表安排自己，但这种时间自由并不是由一个“播放”按钮神奇地产生的，而是由宽带、终端、P2P/直播源、点播数据库、播放器、转码、CDN、版权和用户自己的可用时间共同拼出来的。