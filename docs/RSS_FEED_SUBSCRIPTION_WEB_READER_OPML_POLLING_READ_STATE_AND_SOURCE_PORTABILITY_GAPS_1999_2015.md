# RSS_FEED_SUBSCRIPTION_WEB_READER_OPML_POLLING_READ_STATE_AND_SOURCE_PORTABILITY_GAPS_1999_2015

> Status: research note / cross-repo companion
>
> Scope: 中文 Web / Web-adjacent RSS、Atom、在线阅读器、OPML、博客订阅、reader migration，约 1999—2015
>
> Date: 2026-09-09
>
> Cross-repo life-history note: `tmzncty/how-people-lived/topics/from-periodical-subscription-to-rss-and-algorithmic-feeds-information-subscription-source-sovereignty-and-unread-debt-china-preweb-2026.zh-CN.md`

## 0. 研究问题

本稿不写一部“RSS 兴衰史”，也不把全球 feed 史无限扩进本仓库。它只研究一个 old-Web state gap：

> **一个历史页面上出现 RSS 图标、一个 feed URL 或一个在线阅读器入口以后，我们还需要哪些证据，才能证明某个来源真的可订阅、阅读器成功抓到更新、用户账号保存了订阅、未读状态在多设备间一致，并且用户在服务停服时能够把自己的订阅图迁走？**

这类对象特别容易被 archive 误读，因为公开层和私人层分得很深：

```text
public website
→ public RSS/Atom endpoint
→ private reader account
→ private subscription graph
→ reader polling backend
→ private read/unread/star/tag state
```

archive 很可能留下最外面的图标、帮助页和 feed XML，却看不见真正决定个人阅读生活的账号状态。

因此必须坚持：

```text
RSS icon exists
!= feed URL exists
!= feed returns HTTP success
!= payload is valid feed
!= reader can parse it
!= user subscribed
!= backend committed subscription
!= poller fetched later update
!= item entered user's queue
!= user saw/read it
```

---

## 1. Scope boundary

### 1.1 本仓库主对象仍是约 1995—2015 中文 Web

本稿主体只处理：

- 中文博客/新闻站点的 RSS/Atom 输出；
- RSS 图标、autodiscovery、订阅按钮；
- 抓虾、鲜果、有道阅读、Google Reader 在中文用户场景中的 Web 使用；
- OPML 导入导出；
- Web reader 的账号、文件夹、read/unread、tag/star/share 等状态；
- reader shutdown/migration；
- 中文 Web 页面怎样调用第三方订阅服务。

### 1.2 1999 以前全球历史只作为技术前史

RFC 977（1986）的 NNTP 和更早 Usenet 说明“选择持续更新的 group、询问新文章、只取需要且尚未拥有的对象”有更早网络谱系。

来源：

- RFC Editor, RFC 977, 1986
- https://www.rfc-editor.org/info/rfc977/
- grade: A

它不属于本仓库主研究期，也不能用来证明中文大众旧网已经具有 RSS 行为。

### 1.3 1999 RSS 0.90 是协议边界，不是中文采用起点

RSS Advisory Board 保存的 Netscape RSS 0.90 规范注明原发布日为 1999-03-15。

来源：

- https://www.rssboard.org/rss-0-9-0
- https://www.rssboard.org/rss-history
- grade: A

这里只用来固定 Web syndication 的协议前史。

> **specification date != Chinese service launch != user adoption.**

---

## 2. 已确认的中文历史主体与同期材料

### 2.1 抓虾 / `www.zhuaxia.com`

2007-02-12 新浪科技同期长篇访谈直接把抓虾链接指向 `www.zhuaxia.com`，并称其为在线 RSS 订阅网站；创始人徐易容在实录中说公司 2005-12 成立、产品 2006-04 上线。

来源：

- https://tech.sina.com.cn/i/2007-02-12/19041381851.shtml
- grade: A/B（同期访谈 + 页面外链；功能/时间为当事人自述）

该页还保留了：

- 实际博客用户使用抓虾的第一人称；
- 从 Bloglines 向抓虾迁移部分订阅的描述；
- 热门/推荐功能；
- 在线 reader 相对 desktop reader 的讨论；
- 多电脑与未来手持设备阅读的同期想象。

但它仍然不是抓虾本身的历史 capture。

### 2.2 2007 OPML：跨 reader 的 source graph 可携带性已明确存在

2007-07-02，月光博客公开从 Google Reader 导出的 OPML 文件，并明确说可导入 Google Reader、Bloglines、抓虾等 reader；个人样本为 150+ sources、每日约 100—300 updates。

来源：

- https://www.williamlong.info/archives/954.html
- grade: A（同期公开第一人称及公开 OPML 行为）

它可以证明：

> 至少部分中文重度用户已经实际使用 OPML 做 source-list portability。

不能证明：

> OPML 迁移保留 read/unread/star/tag/share/note；
> 150+ 是普通用户的典型规模。

### 2.3 2008 Web reader：read/unread/tag 跨电脑一致成为可观察产品能力

2008-11-27 月光博客介绍 Google Reader 等 Web RSS reader 时，明确把“在不同电脑看到相同 feed、已读/未读、标签一致”列为在线 reader 的优势。

来源：

- https://www.williamlong.info/archives/1591.html
- grade: B/A（同期技术观察）

这说明在线 reader 后端已不只保存 source URL，还承担 user-state synchronization。

### 2.4 2008 反例：reader 的 unread queue 可以成为注意力负担

2008-07-31，一名博客园用户留下同期第一人称，称自己因为大量订 RSS 而陷入“阅读黑洞”，大量消耗业余时间并产生阅读焦虑，最后主动退订。

来源：

- https://www.cnblogs.com/xjb/archive/2008/07/31/exit-rss.html
- grade: A（同期个人材料；不可外推总体）

这对 state archaeology 也有意义：

> unread count 不是装饰性 UI；它可能改变用户的清理、退订和阅读行为。

### 2.5 2009 desktop reader 的 browser/client dependency

2009-03 月光博客实测“网铃阅读器”时，记录其运行于 Windows 2000+，依赖 IE6/IE7，IE6 下部分 RSS 链接不能订阅，并可通过 URL、内置 feed 库或关键词建立订阅。

来源：

- https://www.williamlong.info/archives/1733.html
- grade: A/B（同期软件实测）

这提醒 old-Web 研究：

```text
feed itself valid
!= every historical client can subscribe
```

用户实际成功还取决于：

- OS；
- embedded IE engine；
- XML parser；
- charset/content-type；
- TLS/HTTP behavior；
- client bugs。

### 2.6 2011 mobile client：Google Reader 账号成为第三方阅读器同步后端

2011-05 的中文 Reeder 介绍明确说：Reeder 使用 Google 账号登录，自动与 Google Reader 同步；用户可以先在 Google Reader 加 feed，再在 iPhone/iPad 客户端阅读。

来源：

- https://www.williamlong.info/apps/archives/93.html
- grade: B（同期应用介绍）

这意味着历史对象至少包含：

```text
publisher feed
→ Google Reader backend
→ Google account state
→ third-party mobile client
```

不能把“Reeder app survives”当成“historical Google Reader state survives”。

### 2.7 2013 Google Reader shutdown：hosted reader 被迫与开放 feed 标准拆开

Google 2013-03 宣布 7 月 1 日关闭 Reader，并允许使用 Takeout 导出订阅等数据；同期报道指出 FeedDemon、NetNewsWire、Reeder 等第三方应用依赖 Reader 的订阅/同步基础设施。

来源：

- https://tech.sina.com.cn/s/2013-03-14/08368144866.shtml
- https://tech.sina.com.cn/i/2013-03-14/09168144952.shtml
- grade: B（同期新闻，依据官方公告/开发者生态）

这强制建立一个关键边界：

> **RSS protocol survives != hosted reader backend survives.**

### 2.8 2013 migration failure：source list 导出以后仍有 operational state

2013-07-05，Flipboard 在 Google Reader 用户迁移期间出现服务中断；报道指出一次故障与把 Google Reader 迁移来的订阅源加入 Flipboard 自家服务有关。

来源：

- https://tech.sina.com.cn/i/2013-07-05/16188512133.shtml
- grade: B

所以：

```text
export bundle created
!= new service imported
!= subscriptions normalized
!= backend stable
!= user can actually read again
```

### 2.9 2015 抓虾 shutdown：中文 reader 也有 exit-state archaeology

2015-08-21 的同期行业报道说抓虾已关闭，并称抓虾在 8 月 5 日向用户发邮件，提示将在 8 月 20 日正式关闭并要求备份数据。

来源：

- https://www.sohu.com/a/28583951_114814
- grade: B（同期行业报道；本轮未取得原始群发邮件）

这可以支持：

> shutdown notice / backup window existed according to contemporaneous reporting.

不能支持：

> every user saw the notice / exported / imported successfully。

---

## 3. Object model

高质量复原至少要区分以下对象。

### 3.1 Publisher/site layer

```text
SITE
PAGE
FEED_ENDPOINT
FEED_FORMAT = RSS / Atom / RDF variants
AUTODISCOVERY_LINK
VISIBLE_RSS_ICON
```

必须问：

- feed URL 是否和 page URL 同 host？
- 是否经 FeedBurner/Feedsky/第三方代理？
- 是否全文或摘要？
- 是否只有某栏目 feed？
- 一个 page 是否声明多个 feed？

### 3.2 Feed document layer

最小调查字段：

```text
feed_url
http_status
content_type
charset/xml_encoding
format/version
channel/feed title
site link
self link if any
entry/item identifier
entry link
published
updated
summary/content
author/category
```

历史版本不一定具备所有字段，不能把现代 Atom/RSS 语义倒投。

### 3.3 Reader account layer

```text
PERSON
→ READER ACCOUNT
→ SESSION
→ SUBSCRIPTION GRAPH
```

subscription record 至少可能有：

```text
feed_url
canonical_feed_id
folder/category
custom_title
added_at
polling metadata
last_success
last_error
```

### 3.4 Item cache/state layer

Reader 可能为一个 entry 另外维护：

```text
reader_item_id
source_feed_id
source_entry_id/guid/link
fetched_at
content_snapshot/cache
read/unread
starred
shared
tags
note
```

这些状态大多不是 feed 标准本身的一部分。

### 3.5 Client layer

可能包括：

- Web browser；
- desktop reader；
- browser sidebar/plugin；
- mobile Web；
- native mobile client；
- third-party app using hosted backend API。

### 3.6 Migration/export layer

```text
OPML source graph
JSON state export
ZIP/Takeout bundle
reader-specific backup
```

必须把不同导出对象分开。

---

## 4. State machine A：Feed discovery / autodiscovery

```text
PUBLISHER PAGE EXISTS
→ page contains visible RSS link/icon?
→ page contains <link rel="alternate" ...> autodiscovery?
→ browser/reader sees declaration
→ user invokes subscribe action
→ target feed URL resolved
→ HTTP request succeeds
→ feed parser accepts payload
```

### 4.1 关键边界

```text
RSS icon survives != link target survives
visible link survives != autodiscovery survives
autodiscovery survives != historical browser exposed it
feed URL returns 200 != valid feed
valid feed now != valid in historical client
```

### 4.2 Archive 风险

Wayback 可能重写 `href`，导致：

- feed URL 指向 archive wrapper；
- browser extension 无法识别；
- current browser 误解释 content-type；
- archived page and feed 来自不同 capture dates。

因此必须记录：

```text
page_capture_datetime
feed_capture_datetime
original_href
rewritten_href
content_type
encoding
```

---

## 5. State machine B：Subscribe transaction

```text
USER chooses feed
→ READER ACCOUNT authenticated
→ SUBSCRIBE request issued
→ reader normalizes URL / redirects
→ feed fetched
→ format parsed
→ subscription record committed
→ folder/category assigned
→ polling schedule created
→ initial items indexed
→ UI reports success
```

### 5.1 不能从 UI success 直接跳到 durable subscription

```text
click subscribe
!= backend commit
!= scheduled polling
!= future update observed
```

### 5.2 Redirect/canonicalization

同一站点可能有：

```text
/feed
/rss.xml
atom.xml
FeedBurner/Feedsky proxy
301 redirect
```

reader 可能保存原始 URL，也可能保存重定向后的 canonical URL。

因此：

> **same publication != same stored feed URL.**

---

## 6. State machine C：Poll → new item → unread

```text
publisher publishes page
→ feed generator emits/updates entry
→ reader polling job runs
→ HTTP request
→ response parsed
→ deduplication by GUID/link/content/etc.
→ new item inserted or existing item updated
→ unread count changes
→ user loads UI
→ item rendered
→ item marked read manually/automatically
```

### 6.1 时间至少有四种

必须区分：

```text
page published_at
feed entry published/updated
reader first_fetched_at
archive capture_datetime
```

不能因为 archive 在 2008-07-03 抓到一个 item，就写“用户于 7 月 3 日看到”。

### 6.2 更新和新建不是同一件事

Atom/RSS entry 可能更新；reader 可能：

- 改写原 item；
- 产生新 item；
- 不重新标 unread；
- 重新标 unread；
- 保留旧缓存。

历史版本需要具体证据。

### 6.3 `1000+ unread` 之类显示可能是 cap

Google Reader 等 reader 历史上可能对大数字进行 UI 截断/显示上限。

因此：

> **displayed unread count != exact backend unread cardinality unless verified.**

---

## 7. State machine D：Read/unread/star/tag/share/note

```text
item indexed
→ unread
→ UI displayed
→ read state may auto-change on scroll/open
→ user can star/tag/share/add note
→ backend commit
→ second client fetches state
→ state converges or conflicts
```

### 7.1 read != actually comprehended

旧网考古只能证明应用状态，不能证明人的认知：

> **item state = read != human read every word.**

### 7.2 cross-device state 需要 backend，不只是 feed

2008 同期材料明确强调 Web reader 可以让不同电脑保持相同已读/未读/标签。

所以 archive 中如果只保存 publisher feed：

> 它无法恢复某个用户“读到哪儿”。

---

## 8. State machine E：OPML export/import

### 8.1 Export

```text
USER requests export
→ backend enumerates subscriptions
→ folders/categories serialized
→ OPML generated
→ HTTP download starts
→ file reaches user
→ user preserves file
```

### 8.2 Import

```text
OPML file selected
→ parser accepts XML
→ outline hierarchy parsed
→ feed URLs extracted
→ URLs normalized
→ duplicates resolved
→ feeds fetched
→ dead feeds rejected/retained
→ subscription records committed
→ folders reconstructed if supported
```

### 8.3 最重要边界

```text
OPML exported
!= file reached user
!= file preserved
!= import accepted
!= folder semantics preserved
!= every feed still live
```

以及：

> **OPML source list != read/unread/star/tag/share/note state.**

这条必须作为以后所有 Reader migration 研究的默认门禁。

---

## 9. State machine F：Hosted-reader shutdown / migration

```text
SERVICE plans shutdown
→ notice published/emailed
→ user becomes aware
→ export available
→ user initiates export
→ bundle generated
→ user downloads
→ target reader chosen
→ source graph imported
→ feeds refetched
→ private states partially/fully migrated?
→ old backend disabled
→ old private state deleted/unreachable
```

### 9.1 Google Reader 2013 是典型案例

需要分开：

- public announcement；
- Takeout export；
- OPML subscriptions；
- richer JSON/state objects；
- third-party API dependencies；
- target reader capacity；
- target migration outages。

### 9.2 抓虾 2015 是中文本土案例

本轮只有同期行业报道证明：

- 关闭；
- 提前邮件通知；
- 提醒备份。

仍未知：

- export UI 长什么样；
- export 格式；
- 是否含 folder；
- 是否含收藏/评论/分享；
- 多少用户完成撤离；
- 关闭后多长时间数据仍可恢复。

---

## 10. State machine G：Third-party reader/backend dependency

2011 Reeder + Google Reader 这类架构应拆成：

```text
PUBLISHER FEED
→ GOOGLE READER POLLER/CACHE
→ GOOGLE ACCOUNT SUBSCRIPTION/STATE
→ GOOGLE READER API
→ THIRD-PARTY APP
→ LOCAL CACHE
→ USER INTERACTION
→ state sync back to Google Reader
```

所以 2013 Reader 停止不只是“网页入口没了”，还会影响多个 app 的 backend assumptions。

> **client binary survives != backend survives != historical reading workflow executable.**

---

## 11. Feed full text vs linked page：两种保存对象

历史 feed 可能包含：

- title + link only；
- summary；
- full text；
- embedded HTML；
- image enclosure/media；
- comments feed。

因此可能出现：

### Scenario A

```text
page gone
feed capture survives with full text
```

### Scenario B

```text
page survives
feed endpoint gone
```

### Scenario C

```text
both survive but dates differ
```

必须固定：

> **feed payload capture is not automatically the same artifact as the original page capture.**

如果 feed 保存了原页面全文，它可以作为文本证据，但要明确 provenance 与 capture context，不能伪装成原页面 DOM。

---

## 12. Charset / XML / HTTP compatibility

中文 RSS 历史复原特别容易碰到：

- GB2312/GBK 页面 + UTF-8 feed；
- XML declaration 与 HTTP header 冲突；
- HTML entity 未转义导致 parser failure；
- malformed XML；
- feed MIME type 错误；
- relative URL；
- Blogger/WordPress/国产博客模板差异；
- redirect chain；
- gzip；
- HTTPS/TLS later incompatibility。

因此不能只做：

`curl returns body → historical RSS worked`。

至少要记录：

```text
HTTP status
Content-Type
Content-Encoding
redirects
XML declaration
parser behavior
historical client assumption
```

---

## 13. Browser/reader environment

### 13.1 Visible RSS icon

2000s 浏览器可能：

- 在地址栏显示 feed icon；
- 通过 browser sidebar 订阅；
- 交给 external reader；
- 交给 online reader bookmarklet；
- 完全不识别。

### 13.2 Desktop reader

2009 网铃的 IE6/IE7 差异证明：

> 同一 feed 在不同 historical runtime 下可能有不同 executability。

调查表应包含：

```text
OS
browser engine
reader version
XML parser/runtime
network/TLS environment
```

---

## 14. Dynamic page and archive pitfalls

### 14.1 Reader shell problem

Wayback 可能保存：

- login page；
- empty reader shell；
- JS bundles；
- icon sprites；

却不保存：

- authenticated subscription list；
- AJAX feed list response；
- private cached items；
- read state。

所以：

> **reader UI shell captured != historical reader account captured.**

### 14.2 Current backend re-rendering

如果历史入口仍指向活 backend，今天看到的 feed/search/result 可能是当前数据，而不是 capture 当时的数据。

### 14.3 Mixed-time replay

一个 replay 页面可能同时包含：

- 2008 HTML；
- 2009 CSS；
- 2026 live image fallback；
- missing JS；
- current browser XML rendering。

所以必须逐资源记录时间。

---

## 15. Public sharing ≠ private subscription graph

2007 月光博客主动公开自己的 OPML，是一个珍贵的 consented/public historical artifact。

但一般情况下，私人 subscription graph 可能暴露：

- 疾病；
- 宗教；
- 性与亲密关系；
- 求职/失业；
- 财务压力；
- 政治兴趣；
- 地理位置；
- 小众社群。

因此本仓库应固定隐私门槛：

> **不要以“复原 old Web”为理由，批量寻找、恢复或公开普通人的私人 reader account/subscription graph。**

优先使用：

- 平台 demo；
- 自愿公开 OPML；
- 帮助文档；
- 公开 feed；
- 停服通知；
- 公开第一人称；
- 软件手册。

---

## 16. Preservation levels

### F0 — no verified artifact

只有回忆、报道或 locator。

### F1 — visible subscription surface

已验证历史页面有：

- RSS icon；
- “订阅”按钮；
- reader service shell/help。

但 feed payload 未验证。

### F2 — verified feed payload

至少验证：

- capture datetime；
- original URL；
- HTTP；
- encoding；
- parseable RSS/Atom payload；
- item fields。

### F3 — longitudinal feed sequence

取得多个时间点 feed capture，可观察：

- item arrival；
- entry churn；
- update semantics；
- feed size/window。

### F4 — reader UI + public/demo state

能确认 reader 的：

- subscribe；
- folder；
- unread；
- star/tag；
- OPML import/export UI

但不需要私人账号。

### F5 — transaction semantics

通过公开 demo、手册、测试账号或合法可复现实验确认：

```text
subscribe commit
polling
item insertion
read-state update
export/import
```

### F6 — portability / shutdown evidence

能可靠解释：

- source graph 如何导出；
- 哪些 state 不在 OPML；
- target import；
- shutdown deadline；
- migration failures。

### F7 — privacy-preserving full architecture

在不暴露私人 subscription graph 的前提下，完整记录：

- protocol；
- page/feed；
- reader backend；
- client；
- state；
- export；
- shutdown。

最高等级**不要求**获得真实普通用户的私人阅读数据库。

---

## 17. Claim ladder

### 可以说

> 2007 年中文 Web 上存在抓虾等在线 RSS reader，且同期用户已经描述多电脑在线阅读和从其他 reader 迁移订阅。

### 不能说

> 2007 年中国网民普遍使用 RSS。

### 可以说

> 2007 年公开 OPML 案例证明 source graph 可以跨 Google Reader、Bloglines、抓虾等 reader 导入。

### 不能说

> 所有 reader 能无损迁移 read/unread/tag/share state。

### 可以说

> 2013 Google Reader shutdown 影响依赖其同步基础设施的第三方应用，并触发迁移。

### 不能说

> Google Reader shutdown 等于 RSS 标准死亡。

### 可以说

> 2015 同期报道记录抓虾关闭前提醒用户备份。

### 不能说

> 所有抓虾用户都成功备份。

---

## 18. 与算法 feed 的边界

本仓库到 2015 为止，只需要说明一个历史转折的边界：

RSS/source-subscription 的基本模型是：

```text
user selects source
→ source publishes
→ reader fetches
```

后来的 algorithmic feed 更可能是：

```text
platform has candidate corpus
→ user behavior/profile/social graph
→ ranking/recommendation
→ platform selects next item/source
```

这两套系统可以混合；抓虾本身已有热门/推荐。

所以 old-Web 文档不能写成：

> RSS = 无算法。

正确边界是：

> **source-selection layer、ranking layer、state-custody layer 可以由不同主体控制。**

---

## 19. 本轮 historical replay 尝试

### 19.1 抓虾 candidate host 已由同期链接确认

2007 新浪实录中，抓虾超链接明确指向：

`www.zhuaxia.com`

这足以把 hostname 登记为 **candidate historical host**。

但不等于已经拿到抓虾 2007 首页/reader 的历史 memento。

### 19.2 Wayback replay 尝试

本轮先成功打开 `https://web.archive.org/` 的 Wayback Machine 当前入口，然后尝试直接构造：

```text
https://web.archive.org/web/20070215000000/http://www.zhuaxia.com/
https://web.archive.org/web/20070701000000/http://www.feedsky.com/
```

当前 Web 访问链拒绝这两个构造 replay URL，原因是安全 URL 规则要求目标 URL 必须来自先前搜索结果或用户原文；因此未得到历史响应本身。

所以本轮必须记：

```text
M1 verified zhuaxia.com historical capture: NOT ACHIEVED IN THIS SLICE
M1 verified feedsky.com historical capture: NOT ACHIEVED IN THIS SLICE
```

这**绝不等于**：

```text
Wayback has no capture
site was not archived
site did not exist
```

本轮已经完成的是：

- Wayback 服务当前入口可访问；
- `www.zhuaxia.com` 的同期 hostname 可由 2007 新浪外链独立确认；
- historical replay 本轮未通过工具安全 URL 约束。

这符合 `METHOD.md` 的负证据门禁。

---

## 20. 以后取得 memento 后的检查清单

每个 capture 至少记录：

```text
original_url
capture_url
capture_datetime
HTTP status
MIME type
charset/XML encoding
redirect chain
DOM / raw XML
RSS/Atom version
autodiscovery tag
visible RSS icon/link
item GUID/link/title/date
script/client dependencies
whether resource is replayed or live
```

对 reader 页面额外检查：

```text
login shell
subscription UI
OPML import/export
folder/category model
read/unread UI
star/tag/share/note
AJAX/API references
polling hints
mobile/third-party-client references
```

---

## 21. 下一轮优先证据包

1. 用真正可打开的 Wayback result 取得 `zhuaxia.com` 2006—2009 capture，而不是手工猜 timestamp；
2. 找到抓虾公开 help/FAQ，可核验 OPML、folder、read state、收藏/分享字段；
3. 找到鲜果/有道 reader 的同期公开页面，比较各家 source graph 与状态模型；
4. 寻找 Feedsky 中文博客上的 feed proxy/统计/广告状态，区分 publisher-side service 与 reader-side service；
5. 获取 2013 Google Reader Takeout 数据模型的原始/高质量技术文档，拆 `subscriptions.xml` 与 JSON state；
6. 获取 2015 抓虾原始停服邮件/notice capture；
7. 对同一中文博客尝试 `HTML page capture + RSS feed capture` 成对复原，实证 page/feed 时间与内容差异；
8. 建立一个不含私人账号的 RSS replay fixture，用历史 charset、broken XML、redirect、full-text/summary cases 验证 state machine。

---

## 22. 本轮对 old-Web 方法的新增结论

这一对象补出了几条可复用的方法边界：

```text
RSS icon survives != feed survives
feed survives != linked page survives
page survives != feed survives
HTTP 200 XML != historical client parse success
feed item published != reader first fetched != archive captured
reader shell survives != private subscription graph survives
OPML survives != reader state survives
subscription export succeeds != target migration succeeds
Google Reader dies != RSS protocol dies
shutdown notice exists != user noticed/exported
```

还补出一个重要档案偏差：

> **旧 Web 最容易保存的是公开“订阅入口”，最难保存的却是一个普通人多年建立的私人 source graph 与 read state。**

而后者不仅难保存，也不应该因为历史研究而被无差别重新公开。

因此 RSS 是一个很典型的 old-Web 深层对象：页面表面只是一枚橙色图标；真正决定一个人未来每天会看到什么的，是图标后面那条长期运行的订阅、轮询、缓存、状态和迁移链。
