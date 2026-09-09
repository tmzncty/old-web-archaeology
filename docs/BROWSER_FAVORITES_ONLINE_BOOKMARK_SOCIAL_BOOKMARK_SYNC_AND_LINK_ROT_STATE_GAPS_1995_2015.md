# BROWSER FAVORITES / ONLINE BOOKMARK / SOCIAL BOOKMARK / SYNC / LINK-ROT STATE GAPS, 1995–2015

Status: research note / state-gap model  
Scope: 约 1995–2015 中文 Web 中浏览器收藏夹、网络收藏夹、网摘/社会化书签、浏览器账号同步、导入导出、全文/快照收藏及其 archive blind spots；**不把本仓扩展成全球 bookmark 史或 2015 年后的通用知识管理史**。  
Cross-repo companion: `tmzncty/how-people-lived/topics/from-favorites-to-retrieval-memory-bookmarks-online-collections-and-link-rot-china-1994-2026.zh-CN.md`  
Last research pass: 2026-09-09

---

## 0. Why bookmarks are a special old-Web object

旧网页考古很容易把 bookmark 当成“小功能”：一个标题 + 一个 URL。

实际上，一条收藏记录至少可能位于以下不同系统：

```text
browser local profile
Windows Favorites folder
exported HTML file
browser toolbar
browser account
online-bookmark website
social-bookmark account
mobile browser
cloud/sync backend
snapshot/full-text preservation backend
```

并且它指向的目标网页又是另一个独立、会继续变化的对象。

因此必须先固定最重要的边界：

> **bookmark survives != bookmarked page survives**

以及：

> **bookmark URL resolves today != same content that user bookmarked historically**

一个 2006 年用户的 bookmark 可能完整保存到今天，但：

- 域名换了主体；
- URL 被 301 到首页；
- 页面内容重写；
- charset/资源失效；
- 页面只对登录用户开放；
- 原站死亡后域名被重新注册；
- archive 保存的是另一时点。

所以 bookmark 是 old Web 的**路径 artifact**，不是自动的 historical content capture。

---

## 1. Evidence contract

遵循 `docs/METHOD.md`。

### 1.1 Research units

至少分别记录：

- `browser_or_client`
- `browser_profile`
- `local_bookmark_store`
- `favorites_folder`
- `bookmark_entry`
- `bookmark_folder`
- `bookmark_title`
- `target_url`
- `target_page_state`
- `export_file`
- `import_process`
- `online_bookmark_platform`
- `online_account`
- `remote_collection`
- `tag`
- `public_private_state`
- `sync_backend`
- `sync_revision`
- `snapshot_or_fulltext_copy`
- `capture`
- `claim`

不能把：

```text
“QQ书签在 2007 年存在”
```

和：

```text
“某具体用户 2007-07-26 的第 83 条私人书签是什么”
```

当成同一层研究对象。

### 1.2 Evidence grades used here

- **A**：同期浏览器/平台官方文档、安装包/帮助页、历史 HTML/capture、用户自己导出的 contemporaneous bookmark file；
- **B**：同期媒体教程、产品评测、站长插件日志、普通用户操作帖；
- **C**：后来回忆、当前百科/产品史；
- **D**：根据残存字段/URL/截图复原历史事务。

公司或平台今天保存一篇标注 2006 的旧新闻，可以证明“今天保留了这份同期文本”，不能自动证明当年的 HTML/DOM/URL routing 与今天页面一致。

### 1.3 Privacy boundary

私人 bookmark collection 可以暴露：

- 医疗/疾病；
- 财务；
- 性与亲密关系；
- 宗教；
- 工作求职；
- 家庭成员；
- 具体兴趣和社交关系；
- 过去访问过但后来删除的页面。

因此本仓不得为了“完整复原”而批量重新公开普通人的私人收藏集合。

优先研究：

- 公共产品/help 页面；
- 公共分享按钮；
- 字段/格式；
- 导入导出；
- 匿名统计；
- 用户主动公开的少量操作经验。

---

## 2. Historical boundary: hotlist/bookmark predates the Chinese mass Web, but that does not make it a Chinese ordinary-life fact in 1994

1994 年 WIRED 对 Mosaic 的同期报道已经记录浏览器可建立 `hotlist`，把经常访问的位置保存下来。

Source:
- https://www.wired.com/1994/10/mosaic/

Evidence:
- B+ / overseas near-contemporary evidence。

这只是技术/海外使用前史。

本仓主对象仍是约 1995–2015 中文 Internet/Web。不能从：

```text
Mosaic had hotlist in 1994
```

跳成：

```text
1994 Chinese households commonly maintained Web bookmarks
```

后者需要中国公众接入、设备、浏览器发行、用户实践等独立证据。

---

## 3. State machine A — local browser favorite

最小状态链：

```text
page loaded
→ user invokes Add Favorite/Bookmark
→ browser obtains current URL/title
→ user may rename/select folder
→ entry written to local store
→ local store survives browser/session
→ user opens bookmark UI
→ entry found
→ target URL requested
→ target response returned
→ user sees usable page
```

### 3.1 Add action gap

页面里存在“加入收藏夹”按钮，不证明：

- 用户点击了；
- 浏览器允许脚本写收藏；
- 安全策略没有阻止；
- entry 最终落盘；
- 标题/URL 是作者预期的值。

因此：

```text
AddFavorite UI exists
!=
bookmark entry created
```

### 3.2 Browser/client gap

IE、Netscape、Firefox、Maxthon、腾讯 TT、360 等浏览器的 bookmark store、脚本接口、目录语义可以不同。

历史页面使用 `window.external.AddFavorite(...)` 时，应同时记录 browser assumption。现代 Chromium 打不开这条旧接口，不证明当年 IE 不能工作；现代浏览器成功执行一个替代脚本，也不证明历史行为相同。

Microsoft legacy IE 文档仍保存 `AddFavorite(URL, Title)` 方法说明，并限制 URL scheme/用户动作条件。

Source:
- Microsoft Learn, legacy `AddFavorite` documentation:  
  https://learn.microsoft.com/en-us/previous-versions//aa768521(v=vs.85)

Evidence:
- A/C：官方 legacy technical documentation；适合确认接口合同，不是某一历史网页 capture。

### 3.3 Local-write gap

即使 UI 显示“收藏成功”，还应区分：

```text
browser in-memory state
→ profile/favorites object created
→ filesystem/profile write durable
→ later session still enumerates it
```

浏览器崩溃、profile corruption、权限、漫游配置都可能影响后续可见性。

---

## 4. IE Favorites as a filesystem/profile artifact

2005 年 PCPOP/新浪的同期 Windows XP 教程明确把 IE Favorites 描述为需要备份的本地资产：重装系统可能丢失；IE 的 Import/Export Wizard 可以把 favorites 导出为 HTML，备份到 CD 或导入另一台电脑。

Source:
- https://tech.sina.com.cn/s/2005-12-06/0901783556.shtml

Evidence:
- B：同期技术媒体教程。

这使旧网考古不能只问：

> “收藏夹页面长什么样？”

还要问：

- 收藏对象存在哪里？
- 是 Windows shell Favorites、浏览器 DB、还是自有格式？
- export 是否保留 folder hierarchy？
- title 是否采用页面 `<title>` 还是用户自定义？
- created/modified time 是否进入导出格式？

### 4.1 Import/export state gap

```text
export command available
!= export completed
!= export file readable
!= export contains all metadata
!= file transferred
!= import completed
!= imported tree semantically identical
```

尤其 HTML bookmark export 通常主要保留路径和标题，不能默认保留：

- 原始访问时间；
- favicon；
- cookie/session；
- 页面正文；
- 页面历史版本；
- 登录态；
- 自定义 extension metadata。

---

## 5. Why network favorites mattered in 2000s China: endpoint plurality

2008 年 CNNIC 第 22 次报告记录 2.53 亿网民、19.1% 普及率；同期 CNNIC 数据报道给出：74.1% 网民在家上网、39.2% 使用网吧，网吧网民约 9918 万。

Sources:
- https://www3.cnnic.cn/n4/2022/0401/c88-813.html
- https://news.sohu.com/20080724/n258354852.shtml

Evidence:
- A-/B+：调查/同期报道。

不能从这些上网场所比例直接推出 network favorite 使用率。但它们构成重要技术场景：

```text
one person
→ home PC
→ office/school PC
→ Internet cafe PC
→ later phone
```

本地 bookmark tree 与“同一个人”不天然绑定。

2008 年腾讯 TT4.3 教程正是用“公司、家里不同电脑”来解释网络收藏夹，并描述本地收藏与网络收藏之间拖动。

Source:
- https://www.duote.com/tech/1/1215.html

Evidence:
- B：同期产品教程。

加入：

## **person/profile gap**

```text
same person
!= same Windows profile
!= same browser profile
!= same bookmark store
```

网络收藏的意义之一，就是把 bookmark address 从 device/profile 提升为 account-addressed state。

---

## 6. State machine B — online bookmark / network favorite

```text
user logged in
→ current page URL/title obtained
→ save request sent
→ remote account identified
→ privacy/public state chosen/defaulted
→ tags/folder/notes optionally attached
→ backend commits bookmark object
→ later session/device authenticates
→ remote list fetched
→ entry rendered
→ target URL requested
```

### 6.1 login gap

```text
online bookmark page accessible
!= user authenticated
!= correct account selected
```

共享电脑/网吧尤其必须考虑：

- cookie 是否残留；
- 是否自动登录；
- 退出是否彻底；
- browser history 是否泄露私人收藏；
- 公共/私人 default 是否明确。

### 6.2 save-request / commit gap

```text
bookmarklet/button clicked
!= HTTP request reached service
!= backend commit succeeded
!= entry later retrievable
```

### 6.3 privacy-state gap

社会书签常同时支持公开与私人状态：

```text
remote bookmark exists
!= publicly discoverable
```

archive 看不到私人集合，不能因此推断它不存在。

这是非常重要的 **archive selection bias**。

---

## 7. 2006 Baidu 搜藏 — locator preservation begins to split from content preservation

新浪科技 2006-11-22 报道当时 `cang.baidu.com` 测试页具有：

- 全文收藏；
- 快速查找；
- 网页快照；
- 分享。

Source:
- https://tech.sina.com.cn/i/2006-11-22/09251250212.shtml

Evidence:
- B+：同期媒体对测试页的观察。

2006-11-28 的同期转稿又把传统收藏的弱点描述为：只记录 URL 时，原站失效/删 URL 后不能再打开；百度产品宣称用网页快照/全文收藏补偿。

Source:
- https://www.cnbeta.com.tw/articles/18683.htm

Evidence:
- B：同期媒体/转稿；证明产品宣称，不证明每一份快照都永久可用。

这要求旧网研究新增两个对象：

```text
bookmark_target_url
snapshot_representation
```

它们不能混成一个。

### 7.1 snapshot gap

```text
bookmark saved
!= snapshot created
!= snapshot captures same response user saw
!= snapshot remains available
```

快照还可能发生：

- crawl time 与 user save time 不同；
- JS/登录内容缺失；
- 图片/CSS 未保存；
- charset 解析不同；
- source page 在 crawl 与 save 之间改变。

所以“全文收藏”不能自动升级成 historical page preservation。

---

## 8. 2006–2008 social bookmarking — private PIM and public discovery overlap

2006 年《解放日报》/新浪科技报道国内已有 365key、新浪 VIVI、35766 等大量网络书签/网摘服务，并明确同时存在公共分享与私人收藏。

Source:
- https://tech.sina.com.cn/i/2006-12-01/13491267213.shtml

Evidence:
- B+。

海外 Del.icio.us 同期已经把 bookmark、tag、network、RSS 等结合起来。

Source:
- WIRED, 2006:  
  https://www.wired.com/2006/10/the-social-bookmarking-showdown-deldoticiodotus/

Evidence:
- B+ overseas comparison；只作为形态对照，不扩展本仓 scope。

加入：

## **bookmark / recommendation gap**

```text
user bookmarked URL
!= user endorses URL
!= user recommends URL to everyone
```

收藏动机可能是：

- 以后阅读；
- 工作资料；
- 批判性观察；
- 临时中转；
- 分享；
- 测试服务；
- 私人提醒。

因此社会书签的 save count 不能简单当“支持票数”。

---

## 9. 2007 QQ书签 — account and browser-toolbar handoff

2007 年 QQ 工具栏同期材料描述：用户无需再注册，可用 QQ 号码登录；QQ书签 (`shuqian.qq.com`) 是免费网络收藏夹，可从工具栏收藏当前网址、查看收藏列表、管理和分享。

Source:
- https://www.cnbeta.com.tw/articles/soft/33673.htm

Evidence:
- B：同期行业媒体/产品材料转述。

同期 QQ 实验室产品报道也已经列出 `QQ书签（shuqian.qq.com）`。

Source:
- https://www.cnbeta.com.tw/articles/soft/25271.htm

Evidence:
- B。

这要求把事务拆开：

```text
historical Web page
→ toolbar/browser extension
→ QQ account auth
→ bookmark API/backend
→ online collection page
```

archive 即使保存了 `shuqian.qq.com` 首页，也通常不会保存：

- 已登录工具栏状态；
- QQ account cookie/token；
- 私人 bookmark list；
- save request；
- backend commit；
- later cross-device fetch。

---

## 10. 2008 share-button ecology — one Web page could fan out to many bookmark backends

WPJAM 在 2008-06-16 公布 17fav WordPress 插件的同期动作统计，其中包括：

- QQ书签 1283；
- 百度搜藏 959；
- Google书签 666；
- del.icio.us 651；
- 雅虎收藏 444；
- 新浪 VIVI、365Key 等。

Source:
- https://blog.wpjam.com/2008/06/16/bookmark-and-share-stats-1/

Evidence:
- A-/B+：站长公开自身插件统计；**不是总体市场份额**。

这给旧网页面增加一个容易漏掉的对象：

## **bookmark/share fan-out state**

一个博客正文底部可能有：

```text
share/bookmark link A
share/bookmark link B
...
```

每个链接又可能依赖：

- third-party endpoint；
- encoded page URL；
- encoded title；
- charset；
- popup；
- account login；
- callback；
- remote service continued existence。

因此：

```text
share-button image survives
!= share endpoint survives
!= target parameters decoded correctly
!= bookmark created
```

旧 Web capture 经常能保存小图标，却丢掉真正的 third-party transaction。

---

## 11. State machine C — mobile bookmark handoff

2009 年 QQ 手机浏览器 beta 的同期评测写到起始页把“我的书签”和“我要搜索”放在前面。

Source:
- https://www.duote.com/tech/1/2752.html

Evidence:
- B。

这不能自动证明 desktop QQ bookmark 与 mobile bookmark 使用完全相同 backend。

必须区分：

```text
mobile local bookmarks
mobile account bookmarks
desktop online bookmarks
server-side merged view
```

如果没有同期技术/帮助证据，不能仅凭同一品牌名推断四者完全一致。

加入：

## **brand-continuity / backend-continuity gap**

```text
same product brand
!= same storage schema
!= same sync backend
!= same merge semantics
```

---

## 12. State machine D — sync and revision history

2009 年搜狐数码介绍 Maxthon 收藏恢复：浏览器可在本地和在线状态中建立恢复点，用于处理误删或导入覆盖。

Source:
- https://digi.it.sohu.com/20090716/n265266624.shtml

Evidence:
- B：同期产品教程/媒体稿。

因此 bookmark sync 不能只有：

```text
local → server → device B
```

至少还要建模：

```text
local revision A
server revision S
remote device revision B
merge/overwrite policy
backup point
rollback target
```

### 12.1 sync gap

```text
sync enabled
!= sync request sent
!= server commit
!= second device fetched
!= both sides converged
```

### 12.2 merge gap

“merge” 不是一个自然唯一操作。

可能涉及：

- same URL dedupe；
- same title/different URL；
- same URL/different title；
- folder moved；
- duplicate IDs；
- delete tombstone；
- concurrent edits。

没有 backend contract 时，不能从 UI 上一个“同步成功”推出所有设备拥有同一语义树。

### 12.3 deletion-propagation gap

同步系统最危险的情况之一：

```text
accidental local deletion
→ valid sync event
→ server records deletion
→ other devices fetch deletion
```

所以“云端有备份”和“云端保存历史版本”不是同一件事。

---

## 13. Bookmark title and folder are historical metadata, not just cosmetics

历史 bookmark entry 可能包含：

- URL；
- title；
- folder path；
- tag；
- note；
- creation/update time；
- favicon；
- visibility；
- source/import provenance。

其中 title 尤其危险。

### 13.1 page-title gap

```text
bookmark_title
!= historical <title> bytes
```

因为：

- 用户可以改名；
- browser 可能截断/清洗字符；
- import/export 可能转义；
- later migration 可能改编码。

### 13.2 folder-taxonomy gap

用户自己的 folder hierarchy 可以表达当时的个人分类，但不能当网站官方 taxonomy。

例如：

```text
“工作 > 北京 > 以后再说”
```

只能证明这个收藏集合在某时点这样分类，不证明目标站点属于这一正式类别，也不证明用户真的采取过对应行动。

---

## 14. Link rot — address preservation and Web preservation diverge

一个 bookmark 的历史链条至少有两个时钟：

```text
bookmark_created_at
page_state_at_visit
```

之后目标站还会不断变化：

```text
t0 bookmark created
→ t1 page updated
→ t2 URL redirects
→ t3 domain/site closes
→ t4 domain re-registered
→ t5 archive replay accessed
```

因此研究必须避免：

## **live-target substitution**

即：拿今天打开的目标 URL 内容，直接填进 2008 年 bookmark 的历史语义。

正确表述应类似：

> “2008 年公开 bookmark artifact 记录了 URL X；本轮 2026 访问 URL X 返回当前页面 Y。没有 2008 capture 时，X 当时的正文状态保持 unknown。”

### 14.1 HTTP 200 gap

```text
HTTP 200
!= same historical resource
```

可能是：

- soft 404；
- parked domain；
- generic homepage；
- login shell；
- anti-bot page；
- archive wrapper；
- newly assigned content。

### 14.2 redirect gap

301/302 只证明当前 routing，不证明历史语义连续。

---

## 15. Archive interaction: bookmarks can preserve dead URLs better than archives preserve private bookmark state

这是一个有用的非对称性：

```text
public old page → may be captured by Web archive
private bookmark list → usually not captured
```

但私人 bookmark list 反过来可能保存一批已经死亡的旧 URL。

所以 bookmark 对旧网考古的价值通常不是“它替我们保存了网页”，而是：

> **它给出 candidate original resources。**

后续仍要分别搜索 Wayback/Common Crawl/其他档案，并核 capture datetime。

### 15.1 Candidate URL is not candidate page content

从旧书签拿到：

```text
http://example.cn/foo/bar.html
```

只能升级：

```text
historical URL lead
```

不能直接升级：

```text
historical content established
```

---

## 16. Historical replay attempt in this slice

本轮针对两个同期已确认的 historical host 继续尝试：

- `cang.baidu.com`（2006 百度搜藏）；
- `shuqian.qq.com`（2007 QQ书签）。

公开搜索本轮没有返回可直接打开、且能够核验 capture metadata 的 Wayback memento。随后尝试构造带日期的 Wayback replay URL，但当前 Web 访问工具因 URL safety 约束拒绝了该形式的直接访问。

因此：

```text
M1 verified cang.baidu.com historical capture: NOT ACHIEVED IN THIS SLICE
M1 verified shuqian.qq.com historical capture: NOT ACHIEVED IN THIS SLICE
```

本负结果只表示：

> **本轮没有实际打开并检查一份合格 historical capture。**

它**不表示**：

- Wayback 没有保存；
- 其他 archive 没有保存；
- 当时页面不存在。

因此以下字段保持 unknown：

- `capture_datetime`；
- historical HTTP status；
- historical charset；
- DOM；
- CSS/JS；
- form action；
- popup/bookmarklet behavior；
- authentication flow；
- private collection state。

这遵循 `docs/METHOD.md` 的 archive locator / negative-evidence contract。

---

## 17. Preservation levels for bookmark archaeology

定义 B0–B8：

### B0 — mention only

只有后来回忆/品牌名，无 contemporaneous URL/功能证据。

### B1 — service existence

有同期官方/媒体证据证明收藏服务/功能存在。

### B2 — public shell

有可验证的历史首页/help/UI capture。

### B3 — interaction surface

能验证收藏按钮、参数、bookmarklet、toolbar link、login form 等公开交互表面。

### B4 — data model clues

能验证 title/url/folder/tag/privacy/snapshot 等字段或格式。

### B5 — export/import artifact

有合法可用的 contemporaneous exported bookmark file 或公开 fixture，可验证真实导入导出语义。

### B6 — transaction evidence

能验证至少一次 save/import/sync 的 request/response 或明确日志，但不要求暴露普通人私人内容。

### B7 — revision/sync evidence

能验证 revision、merge/delete/rollback 等行为。

### B8 — target-state linked evidence

在不侵犯隐私/版权前提下，bookmark object 与同一时点 target page capture 可以可靠关联，明确区分两者 datetime。

**B8 不是每个案例都需要达到的目标。** 私人收藏尤其应停在结构性证据，不以暴露私人历史为“完整”。

---

## 18. Reconstruction prohibitions

### 18.1 不用今天的 bookmark JSON 伪造 2007 私人收藏

可做 schema reconstruction，但必须标 D。

### 18.2 不把现代 favicon 补到历史收藏截图当原件

favicon 可能已更换、域名已复用。

### 18.3 不把 archive replay 的 target page 当用户当时看到的页面

除非 capture datetime 与访问链有额外证据。

### 18.4 不模拟真实账号登录

不对历史/现存普通账号做 credential stuffing、password reset 或私人 collection 探索。

### 18.5 不抓取私人 bookmark corpus 来“研究兴趣”

优先结构与匿名统计。

---

## 19. Claim table for this slice

| Claim | Evidence | Grade | Confidence | Boundary |
|---|---|---:|---:|---|
| IE/Windows XP 用户可将 Favorites 导出为 HTML 并导入另一台电脑 | 2005 PCPOP/新浪教程 | B | high | 不证明所有人会备份 |
| 2006 中文 Web 已有多种网络书签/网摘，支持公开/私人收藏 | 解放日报/新浪 | B+ | high | 规模数字不可当全国总体 |
| `cang.baidu.com` 2006 测试页宣称全文收藏/快照等 | 新浪科技同期观察 | B+ | high | 未验证 historical memento/backend |
| `shuqian.qq.com` 2007 作为 QQ书签存在并与 QQ 工具栏/账号结合 | cnBeta 同期产品转述 | B | medium-high | 不是本轮 capture |
| 2008 17fav 插件用户操作同时分布在 QQ书签、百度搜藏、Delicious 等服务 | WPJAM 自身日志 | A-/B+ | high for sample | 严禁外推市场份额 |
| 2008 TT 教程描述本地/网络收藏用于家/公司多机 | 同期教程 | B | high | 场景是产品解释，不代表渗透率 |
| 2009 QQ手机浏览器起始页突出“我的书签” | 同期评测 | B | high | backend continuity unknown |
| 2009 Maxthon 提供收藏备份/恢复路径 | 同期产品教程 | B | high | 未验证所有版本/默认配置 |
| bookmark surviving does not establish target-page historical content | state model + URL semantics | D/methodological | high | 需逐 target 查 capture |

---

## 20. Cross-repo life-history implications

本仓只保留旧 Web 技术/档案结论；普通生活时间线写入 companion。

这里需要向 `how-people-lived` 输出的最小结构是：

```text
local favorite
→ manual export/import
→ account-addressed network favorite
→ public/private social bookmark
→ multi-device/mobile access
→ sync + rollback requirement
→ link rot / platform exit / custody problem
```

它改变的是一种很具体的生活能力：

> 人能不能把“以前找到过、以后可能还要用的信息入口”从一台机器带到下一段生活。

---

## 21. Hindsight risks

1. **不要把 1994 Mosaic hotlist 写成 1994 中国普通家庭 Web 行为。**
2. **不要把 network bookmark existence 写成 popular。**
3. **不要把 17fav 操作次数写成全国份额。**
4. **不要把 save count 写成 endorsement。**
5. **不要把 bookmark entry 当 page snapshot。**
6. **不要把 live target 当 historical target。**
7. **不要把 same brand 当 same backend。**
8. **不要把 “sync successful” 当所有设备 byte/semantic-equivalent。**
9. **不要把私人集合的 archive 缺失写成当时没人使用。**
10. **不要把今天可导出的 HTML/JSON 字段倒推为旧版本字段。**

---

## 22. Open questions / next probes

1. 实际验证 `cang.baidu.com` 2006–2008 至少两个 memento；
2. 实际验证 `shuqian.qq.com` 2007–2010 至少两个 memento；
3. 找腾讯 TT/Maxthon/360 同期安装包或官方 help，确认 local/remote bookmark store 与 sync semantics；
4. 找一份不涉及隐私的 contemporaneous IE/Netscape/Firefox exported bookmark fixture，比较字段损失；
5. 检查中文博客常见“收藏/分享”插件的 target URL encoding、GBK/UTF-8 参数以及 popup 行为；
6. 对少量公开历史 bookmark URL 做 target survival test，但必须分别标 live result 与 historical capture；
7. 查明百度“全文搜藏/快照”在具体时点的抓取/保留语义，不从营销表述猜 backend；
8. 比较 network favorite 与后来平台内收藏（微博/微信/视频平台）的 exportability，但 2015 年后主要进入 companion 或另开边界说明，不能让本仓无限后移。

---

## 23. What this adds to old-web archaeology

旧网仓之前已经研究“怎样第一次找到页面”（目录/搜索），也研究“怎样把文件本体带走”（在线存储）。本轮补上二者之间一个非常常见但保存偏差极大的对象：

> **用户自己保存的返回路径。**

它要求 archive 研究同时处理三套不同状态：

```text
bookmark object state
platform/sync state
target Web resource state
```

这三套状态即使都还“存在”，时间也不一定一致。

因此本轮最重要的方法补丁可以压缩成四条：

```text
bookmark survives != target survives
URL survives != content survives
sync exists != state converged
online collection shell survives != private retrieval memory survives
```

它也说明一种旧 Web 历史可见性的悖论：**普通人最长期、最私人、最能描绘自己如何使用 Web 的那份“个人目录”，往往正是公共 Web archive 最不应该也最难保存的东西。**
