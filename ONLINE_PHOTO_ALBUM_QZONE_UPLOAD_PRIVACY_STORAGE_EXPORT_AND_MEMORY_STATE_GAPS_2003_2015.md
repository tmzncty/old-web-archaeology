# 中文旧网网络相册、QQ 空间图片与“记忆还在不在”状态缺口（2003–2015）

> Scope：本研究严格保持 `old-web-archaeology` 的约 1995–2015 中文互联网范围。重点对象是 2003–2015 网络相册、QQ 空间相册、校园 BBS 图片帖、图片 host 与相关上传/浏览/权限/导出事务。1990s 海外数字影像与 2019/2020/2025/2026 的后续材料只作为前史或 afterlife 对照，不把仓库改成全球照片史。
>
> 核心问题：一个旧网页里“有一张照片”，到底能证明什么？主 HTML、相册索引、缩略图、原图、EXIF、访问权限、上传账号、评论、下载能力和平台数据库是完全不同的状态。**历史页面仍有 `<img>` 标签，不等于历史照片文件仍在；今天还能登录一个旧账号，也不等于 2006 年的浏览器体验被复原。**

对应 how-people-lived companion：

- `topics/from-film-rolls-to-cloud-albums-photo-memory-recoverability-china-1980-2026.zh-CN.md`

---

## 0. 本轮为什么是独立缺口

仓库已经有：

- 个人主页/自出版；
- 博客/SNS；
- BBS/论坛；
- 同学录；
- 电商、租房、医院、铁路、物流等事务状态。

但“照片”不能只作为这些页面上的一种普通附件处理。

它有自己独立的后台事务：

- 上传是否成功；
- 是否生成缩略图；
- 原图是否保留；
- 相册目录是否更新；
- 图片 host 是否还在；
- 权限是否允许当前 viewer；
- 是否允许外链；
- 下载拿到的是原图还是压缩图；
- 平台停服前能否批量导出。

而且照片恰好是旧网 archive 最容易产生**“页面看起来还在，核心生活证据其实已经断掉”**的资源类型之一。

---

## 1. 研究单位必须分开

按 `docs/METHOD.md`，本专题至少拆成：

### platform

例如：

- 网易相册；
- QQ 空间；
- 又拍/巴巴变等独立相册；
- 校园 BBS 的贴图系统。

### site / host

例如：

- `photo.163.com`；
- `qzone.qq.com`；
- `imgcache.qq.com`；
- 图片可能使用的独立 static/image host。

### account / album

一个用户账号下的相册集合，可能有：

- public；
- friends-only；
- password；
- private；
- platform-default visibility。

### page

可能是：

- 相册列表页；
- 某个 album 页面；
- 单张图片 detail 页；
- 上传页；
- 帮助页；
- 下载/导出页；
- QQ 空间中的相册 module。

### image object

必须独立于 page：

- thumbnail；
- medium/rendered version；
- original；
- avatar/cover；
- externally hotlinked copy。

### transaction

- upload；
- album creation；
- privacy change；
- view；
- download；
- delete；
- export；
- migration；
- shutdown recovery。

### capture

Wayback/Common Crawl/其他 archive 保存的一次表示。

**同一相册页的 capture 与其中图片文件的 capture 不是同一个 artifact。**

---

## 2. 两套状态机：照片对象和页面必须分开

### 2.1 上传事务

建议状态：

```text
LOCAL_FILE_EXISTS
→ USER_SELECTS_FILE
→ CLIENT_VALIDATES_FORMAT/SIZE
→ UPLOAD_REQUEST_STARTED
→ BYTES_RECEIVED_BY_PLATFORM
→ OBJECT_PERSISTED
→ THUMBNAIL_DERIVED
→ ALBUM_INDEX_UPDATED
→ ACL_ATTACHED
→ USER_SEES_SUCCESS
```

可能分叉：

```text
UPLOAD_REQUEST_STARTED
→ NETWORK_FAIL
→ RETRY / PARTIAL / DUPLICATE
```

或：

```text
OBJECT_PERSISTED
→ THUMBNAIL_FAIL
→ album shell shows placeholder/red X
```

因此：

> `用户看见“上传成功” != 原图永久保存`。

### 2.2 浏览事务

```text
ALBUM_URL_REQUESTED
→ SESSION/COOKIE CHECK
→ ACCOUNT/ALBUM RESOLUTION
→ ACL CHECK
→ HTML/SHELL RETURNED
→ THUMBNAIL URLs RESOLVED
→ IMAGE HOST REQUESTED
→ IMAGE OBJECT RETURNED
→ BROWSER DECODES IMAGE
→ USER ACTUALLY SEES PHOTO
```

其中任何一层都可能失败。

所以：

- `HTTP 200 album page != photo visible`；
- `thumbnail visible != original available`；
- `original URL known != viewer authorized`；
- `archive has HTML != archive has image object`。

---

## 3. 2003–2006：网络相册作为独立服务与个人空间模块

### 3.1 相册并不是一个统一产品形态

2000s 中期中文 Web 同时存在：

- 独立网络相册；
- 博客附属相册；
- QQ 空间等个人空间内的相册模块；
- 图片外链 host；
- BBS 直接上传附件；
- 自己找免费 Web 空间放图再 `<img>` 外链。

同期资源目录可以看到非常具体的差异：

- 5MB、20MB、50MB、100MB、1GB；
- 按总容量或月上传/流量限制；
- 只接受 JPG，或接受 GIF/PNG/BMP；
- 支持/禁止外链；
- 免费用户加水印；
- 相册访问需要注册；
- 有些使用 Flash 界面。

这些不是无关紧要的套餐差异，而是决定历史页面能否长期工作的重要技术约束。

同期线索：
- `免费相册` 资源索引（2004–2006 多次更新时间）：https://digilander.libero.it/chengfrancesco/album.html

证据等级：**B（同期站长/资源目录；逐项能力仍需平台原始帮助页确认）**。

### 3.2 QQ 空间把照片嵌入一个更大的“个人网络住所”

2006-03-30 的 QQ 空间新手教程记录：

- QQ2005 Beta2 及以上版本被建议作为最佳使用环境；
- 可以从 QQ 客户端进入；
- 也可以访问 `http://qzone.qq.com`；
- 开通后可建立相册、日志等；
- 知道 QQ 号码可以按当时的空间地址模式访问他人空间。

来源：
- https://m.qqan.com/c/1038

证据等级：**B（同期教程）**。

这里要特别记录 browser/client assumption：

```text
QQ client version
IE/browser behavior
possible Flash/JS modules
login cookies
imgcache/static hosts
```

不能用 2026 的 qzone 登录页解释 2006 的实际操作路径。

### 3.3 图片可以既是“相册对象”，又是网页资源

2006 年另一个同期教程教用户把 QQ 空间皮肤图片另存后上传到自己的 QQ 相册，再通过地址用于空间装饰。

来源：
- https://www.qqan.com/article/article_1168_1.html

证据等级：**B（同期用户教程）**。

这提示一个重要旧网事实：

> **相册服务有时同时承担 personal archive 和 image hosting。**

同一图片对象可能被：

- 相册页面浏览；
- 日志引用；
- 论坛外链；
- QQ 空间皮肤/模块引用。

因此平台改变 hotlink policy、图片 URL 或流量限制时，损坏的不只是“相册”，还可能是一批其他网页。

---

## 4. 2007 故障是非常强的事务证据：登录失败、索引失败、对象丢失必须分开

### 4.1 刘大光案例：平台不可登录时，用户无法知道对象是否还在

2007-01-27《财经时报》报道：刘大光（化名）因网易相册提供无限空间与批量上传，在 2006 年 10 月把家中全部数码照片上传。元旦后相册无法登录。平台产品组曾发布致歉并承诺恢复，但到报道时仍未正常。

用户最直接的问题是：“照片能不能恢复、能恢复多少”。

来源：
- https://tech.sina.com.cn/i/2007-01-27/13231356731.shtml

证据等级：**B（同期独立媒体；含用户第一人称与平台公告转述）**。

这条材料不能写成“照片已经丢失”。当时真正可证明的是：

```text
LOGIN/ACCESS = failed or unavailable
OBJECT_RECOVERABILITY = unknown to user
PLATFORM_PROMISED_RECOVERY = yes
FINAL_OBJECT_STATE at article time = unresolved
```

这恰好展示为什么旧网研究不能把“用户打不开”直接等同于“后台对象不存在”。

### 4.2 王女士案例：album shell 与 image object 可以分离

2007-09 的同期报道记载王女士约 130 张照片一度全部显示成异常/red-X；她没有保留本地备份，相册设置为非公开，约一个月后照片又恢复。

这是非常适合作为 state-gap fixture 的个案：

```text
ALBUM_ACCOUNT exists
ALBUM_INDEX likely exists
IMAGE_RENDER failed
LOCAL_BACKUP absent
PRIVACY non-public
LATER_RECOVERY observed
```

不能根据 “red X” 判断到底是：

- image URL 404；
- image host outage；
- auth/session failure；
- database-object mapping failure；
- browser/network failure；
- actual object temporarily unavailable。

除非拿到当时 HTTP/HTML/资源请求证据，否则只能保留这些 competing explanations。

---

## 5. 2008–2010：照片从相册对象进入论坛身份与反馈回路

### 5.1 校园 BBS 图片帖：公开发布是一笔事务，不是“照片存在”

2009-07-10《中国青年报》记录武汉大学毕业生向涛把 PS 后的毕业照发布到校园论坛“珞珈山水”贴图版。

他在发布前担心：

- 不想听到的评论；
- 被熟悉同学认出后笑话；

但仍决定发布，并不断刷新页面看回复。

来源：
- https://zqb.cyol.com/content/2009-07/10/content_2750416.htm

证据等级：**B（同期媒体 + 同时代本人自述）**。

应拆成：

```text
PHOTO_LOCAL
→ EDITED
→ POST_CREATED
→ IMAGE_UPLOADED/HOTLINKED ?
→ THREAD_VISIBLE
→ VIEWERS_LOAD
→ REPLIES_CREATED
→ AUTHOR_REFRESHES
→ AUTHOR_READS_REPLY
```

其中 `IMAGE_UPLOADED/HOTLINKED` 本轮仍未知。

即使未来 archive 找到 thread HTML，也不能默认它已经保存原图。

### 5.2 照片已经参与身份治理

海外同期代表性调查可帮助理解为什么“图片页”不能只当静态内容：Pew 2010 调查显示，美国 18–29 岁 SNS 用户中 41% 曾移除照片中的姓名标签，71% 改过隐私设置。

来源：
- https://www.pewresearch.org/internet/2010/05/26/reputation-management-and-social-media/

证据等级：**A（同期代表性调查；美国对照，不外推中国比例）**。

跨国共同机制是：

```text
photo object exists
≠ user accepts current identity linkage
```

一张照片可以继续存在，但某个人要求解除 tag；或者照片仍可被朋友看到，但不再出现在本人 profile 上。

---

## 6. 2005–2015 旧网页里至少存在五种“照片还在”

为了避免后续 agent 过度陈述，建议统一使用以下层级。

### P0 — page reference survives

HTML/DB shell 中仍有：

```html
<img src="...">
```

或有一条图片记录。

只能证明**引用痕迹**。

### P1 — thumbnail survives

缩略图可以加载。

只能证明某个 derived object 尚存，不能证明原图。

### P2 — rendered/medium copy survives

平台展示尺寸的 JPEG/GIF 可打开。

仍不能证明原始上传分辨率或 EXIF 保存。

### P3 — original downloadable copy survives

需要明确证据证明下载得到 original 或平台声明保留原图。

### P4 — semantic context survives

除了像素，还知道：

- 谁上传；
- 何时；
- 哪个相册；
- 标题/说明；
- 谁在照片里；
- 评论；
- ACL/受众。

只有到这一层，才接近“历史生活记忆”而不是孤立图片文件。

**注意：P4 不代表更适合公开。它往往包含更多个人信息。**

---

## 7. 权限状态：private album 不等于 archive gap 可以被研究者强行填上

照片权限至少需要：

```text
PUBLIC
FRIENDS / RELATION_GRAPH
PASSWORD / SHARED_SECRET
SELECTED_USERS
PRIVATE
UNKNOWN
```

并且：

`historical ACL ≠ current replay visibility`。

Archive 可能：

- 没抓登录后页面；
- 只抓到公开 shell；
- 因 cookie 缺失显示登录页；
- 保存一个被 archive rewrite 改写过的异常页面。

研究伦理上还要再加：

> **当年 non-public 的普通个人照片，即使今天通过某种泄漏/旁路能看到，也不应为了考古批量重新公开。**

此专题优先研究：

- 结构；
- URL pattern；
- 权限模型；
- failure mode；
- 平台帮助页；

而不是重建普通用户私密相册内容。

---

## 8. 图片 host 是旧网保存中经常被忽略的独立故障域

同一页面可能是：

```text
HTML host: qzone.qq.com
image host: imgcache.qq.com / other image domain
JS/CSS host: separate static host
album API: separate endpoint
```

因此 historical capture 必须分别记录：

```text
main_document_capture
thumbnail_capture
original_image_capture
css_capture
js_capture
flash_capture
```

`main_document_capture = yes` 并不能把其他字段默认填 yes。

### 8.1 外链会把故障扩散到平台之外

2000s 免费相册资源目录经常把“是否支持外部调用”作为卖点，说明图片 host 被拿来支持论坛、博客、个人主页或网店。

于是：

```text
album provider changes URL/hotlink rule
→ unrelated historical pages lose images
```

这是一种**跨站资源死亡**，非常适合 M4 缺失地图以后专门统计。

---

## 9. 原图、压缩图、EXIF 与“看起来一样”的陷阱

即使历史图片还能打开，也要问：

1. 是否被平台 resize；
2. JPEG 是否重新编码；
3. EXIF 是否被剥离；
4. 文件名是否被重写；
5. 是否加水印；
6. 是否只剩 thumbnail；
7. 动图是否仍保留全部 frame；
8. PNG/GIF 是否被转成 JPEG；
9. historical color profile 是否还在。

因此：

> `pixels visually similar ≠ historical object bit-identical`。

对于生活史尤其重要的是 EXIF/date：

- 页面发布时间；
- 上传时间；
- 拍摄时间；
- archive capture time；

可能是四个完全不同的时间。

不能把它们合并成“照片时间”。

---

## 10. 2011–2015：从 destination album 到 SNS feed，照片的“主要入口”开始变化

本研究当前不写一条产品年表，而关注 transaction topology。

早期独立相册常是：

```text
user goes to album destination
→ browses album list
→ opens photo
```

SNS/空间 feed 越来越可能变成：

```text
photo uploaded to album/storage
→ activity generated
→ friends receive in feed/dynamic stream
→ comments/likes happen there
→ album becomes backend archive / secondary destination
```

这对考古影响很大：

一张照片的社会互动可能不发生在 photo detail page，而发生在 feed item、说说、转发或 IM 链接中。

因此：

`album capture != social reception capture`。

如果只保存相册页，研究者可能误判一张照片“没有互动”。

---

## 11. 2019 网易相册停运作为 afterlife：shutdown state 必须单独建模

虽然 2019 超出仓库主时间范围，但它直接决定 2003–2015 上传对象的后续命运，因此作为 afterlife 保留。

2019-03 起网易相册停止新注册/VIP 充值并关闭部分功能，仍允许登录、浏览、下载个人资源；公告要求用户在最终停服前保存需要的相册。最终服务器关闭后，用户无法继续使用服务，数据不再保留。

来源：
- 新浪科技，2019-05-07（含公告全文）：https://finance.sina.com.cn/chanjing/gsnews/2019-05-07/doc-ihvhiqax7160503.shtml
- 界面新闻，2019-03-07：https://www.jiemian.com/article/2930056.html

证据等级：**A/B**。

建议 shutdown state：

```text
NORMAL_OPERATION
→ NEW_REGISTRATION_CLOSED
→ FEATURE_REDUCTION
→ READ/DOWNLOAD_WINDOW
→ FINAL_SHUTDOWN
→ ACCOUNT_UNAVAILABLE
→ PLATFORM_DATA_NOT_RETAINED
```

若中间有延期，则再记录：

```text
PLANNED_SHUTDOWN_DATE
ACTUAL_SHUTDOWN_DATE
EXTENSION_REASON
```

不能只写一个 `closed_at`。

### 11.1 export window 是一种事务，不是公告一句话

用户真正完成保存至少需要：

```text
NOTICE_RECEIVED
→ USER_REMEMBERS_ACCOUNT
→ LOGIN_SUCCEEDS
→ ALBUM_LIST_COMPLETE
→ BULK/SINGLE_DOWNLOAD_AVAILABLE
→ DOWNLOAD_COMPLETES
→ LOCAL_COPY_VERIFIED
```

2019 央视财经材料中的付世凯很说明问题：他 2008 年为分享同学聚会照片注册网易相册，后来多年不再注意这个服务，直到朋友提醒才知道关停。

来源：
- https://www.nbd.com.cn/articles/2019-05-23/1335086.html

证据等级：**B（2019 同期用户对 2008 使用路径的回顾）**。

所以：

> `platform published shutdown notice ≠ every historical user received actionable notice`。

---

## 12. 2020–2026 afterlife：旧影像对象还能被重新组织成新的时间界面

2020 年云毕业材料显示，不能返校的毕业生大量使用过去的寝室、课堂、食堂照片和短视频重新制作班级毕业视频；旧文件承担了原先并未设计给它的仪式功能。

来源：
- 中国青年报，2020-06-18：https://zqb.cyol.com/html/2020-06/18/nw.D110000zgqnb_20200618_1-10.htm

2025 年 QQ 空间 20 周年活动允许用户从历史照片中选择内容生成“人生特映礼”；2026 年新版“那年今日”又会根据往年发布主动推送历史动态。

来源：
- https://ai.zol.com.cn/992/9925441.html
- https://www.ithome.com/0/960/949.htm

这些只作为 afterlife 使用，用来证明：

> **2005–2015 写入的平台对象，二十年后可能被新的 UI/算法重新排序和呈现。**

绝不能据 2026 的呈现方式推断 2006 原始页面结构。

---

## 13. 一个必须永久固定的边界：current live legacy page ≠ historical capture

如果 2026 仍能打开一个标有 `2008-06-xx` 的照片/动态页，它最多可以证明：

- 当前服务端返回一个带旧时间字段的对象；
- 某些 historical content 可能仍在平台数据库中。

不能证明：

- 2008 的 DOM 相同；
- 原始图片 URL 相同；
- 当时用的是同一压缩版本；
- 评论/ACL 相同；
- CSS/Flash/JS 相同；
- IE6 用户看到同一布局；
- 今天展示的 EXIF/metadata 当时已经展示。

这种“时间复合页”必须标记为：

```text
CURRENT_SERVICE_RENDERING_OF_HISTORICAL_CONTENT
```

而不是：

```text
HISTORICAL_CAPTURE
```

---

## 14. Archive capture 最低检查单（照片专题版）

在 `docs/METHOD.md` 通用字段外，照片案例至少再记：

```yaml
page_type: album_index | photo_detail | upload | help | feed
historical_url_pattern:
account_identifier_exposed: yes/no/unknown
album_identifier_exposed: yes/no/unknown
image_hosts:
thumbnail_url_observed:
medium_url_observed:
original_url_observed:
image_http_status:
image_mime_type:
image_dimensions:
exif_observed:
acl_visible_in_capture:
login_required:
cookie_required:
js_required:
flash_required:
uploader_plugin_required:
hotlink_behavior:
download_behavior:
archive_rewrite_observed:
```

如果 archive 只抓到 HTML shell：

```text
PHOTO_CONTENT_PRESERVED = UNKNOWN/NO
```

不能因为页面布局完整就打 `yes`。

---

## 15. 浏览器环境：2005–2010 相册尤其不能只用现代 Chromium

需要重点检查：

- IE-specific JS；
- ActiveX/上传插件；
- Flash album/slideshow；
- QQ client 调起；
- GB2312/GBK/UTF-8；
- frameset/table layout；
- 图片预加载脚本；
- `document.all`；
- popup/窗口策略；
- archive rewrite 对 JS 拼 URL 的破坏。

2006 QQ 空间教程明确建议 QQ2005 Beta2 及以上版本，已经足以证明客户端/浏览器环境是研究对象的一部分。

因此现代浏览器里“按钮点不了”不等于历史按钮本来就坏。

---

## 16. 历史可见性偏差：照片越私人，越可能从公共档案中消失

### 16.1 public-Web bias

最容易保存：

- 平台首页；
- 帮助文档；
- 公开明星/摄影账号；
- 被大量外链的图片；
- 热门帖子。

最难保存：

- 私密家庭相册；
- 只给好友的相册；
- 登录后列表；
- 批量上传器；
- 原图下载接口；
- 相册后台排序；
- 被删的普通照片；
- 账号间私下分享。

于是：

> **archive-visible photo culture != ordinary photo culture。**

### 16.2 success bias

今天还能在旧页看到的图片，本来就是存活者。

大量失败状态——red X、404、权限错误、热链失效、数据库错位——反而可能没有被 archive 记录。

因此不能从 surviving pages 推断“当年网络相册一般都很稳定”。

### 16.3 public-person bias

名人、摄影师、媒体图片往往保存更完整；普通宿舍、家庭、恋爱、儿童成长照片更隐私，也更不适合重新公开。

研究应优先抽象技术状态，而不是为了样本量侵犯历史普通用户。

---

## 17. 平台观察事实 / 同时性自述 / 回顾性自述要分栏

| 材料 | 可证明 | 不可直接证明 |
|---|---|---|
| 2006 QQ 空间教程 | 当时教程描述的入口、版本建议、相册功能 | 全国普及率、实际成功率 |
| 2007 网易故障报道 | 用户当时无法正常访问、平台曾公告修复、用户担忧恢复 | 后台究竟丢了多少 object |
| 2009 校园论坛采访 | 某毕业生确实把照片发到论坛并读回复 | 全体大学生都这样 |
| 2019 停服公告 | 平台关闭步骤、下载窗口、数据不再保留的政策 | 每个用户都完成导出 |
| 2025/2026 QQ 空间怀旧功能 | 当前平台如何重新呈现旧数据 | 2005 原始页面就是这种形态 |

---

## 18. Evidence ledger

### A — 原始/同时代平台或研究材料

1. 网易相册 2019 停服公告（超出主 scope，但用于 historical objects afterlife）：
   - https://finance.sina.com.cn/chanjing/gsnews/2019-05-07/doc-ihvhiqax7160503.shtml
2. Pew 2010 网络声誉调查（海外比较）：
   - https://www.pewresearch.org/internet/2010/05/26/reputation-management-and-social-media/

说明：当前仍缺 2003–2010 相册平台原始帮助页的 **verified archive capture**，因此平台早期部分尚未达到 A 级 capture 门槛。

### B — 同期媒体/教程/用户观察

1. QQ 空间教程，2006-03-30：
   - https://m.qqan.com/c/1038
2. QQ 相册作为图片外链/空间资源的教程，2006-04-13：
   - https://www.qqan.com/article/article_1168_1.html
3. 网易相册故障用户，2007-01-27：
   - https://tech.sina.com.cn/i/2007-01-27/13231356731.shtml
4. 武汉大学毕业生 BBS 图片帖采访，2009-07-10：
   - https://zqb.cyol.com/content/2009-07/10/content_2750416.htm
5. 教师 4000 张照片/电子相册，2009-10-16：
   - https://news.sina.com.cn/c/2009-10-16/022616444465s.shtml

### C — 后来回忆/afterlife

- 2019 用户回忆 2008 年用网易相册分享聚会照片：
  - https://www.nbd.com.cn/articles/2019-05-23/1335086.html
- 2025/2026 QQ 空间周年怀旧材料，只用于 current afterlife。

### D — 研究者模型

- P0–P4 photo-survival ladder；
- upload/view/shutdown state machine；
- `current live legacy page` 标记；
- `album capture != image-object capture`。

---

## 19. 本轮 archive 尝试与负结果

本轮实际尝试搜索/定位：

- `qzone.qq.com` / QQ 空间 2006–2010；
- `qzone.qq.com/helpcenter/index.html`；
- `photo.163.com` 2006–2008；
- 相关 Wayback/CDX locator。

公开搜索没有返回一份可直接按本仓 METHOD 检查的目标历史 replay。

进一步尝试直接访问：

- `https://web.archive.org/cdx/search/cdx?url=qzone.qq.com/helpcenter/index.html&from=2006&to=2010...`
- `https://web.archive.org/cdx/search/cdx?url=photo.163.com&from=2006&to=2008...`

当前访问工具因 URL 安全规则拒绝构造后的 CDX 地址，因此**没有取得 capture list，更没有实际打开一份历史快照**。

这只能记作：

```text
M1_CAPTURE_STATUS = NOT ACHIEVED IN THIS SLICE
```

不能写成：

```text
Wayback has no capture
```

也不能把搜索结果、教程截图或今天的 qzone 页面冒充 historical capture。

下一轮若继续 M1，优先尝试：

1. 从公开搜索结果中先获得 exact Wayback URL，再打开；
2. Internet Archive 可公开枚举的 collection/index 入口；
3. Common Crawl index；
4. ArchiveTeam/其他已打包数据集；
5. 从同期媒体页面中的 `imgcache.qq.com` 静态 URL 反查历史资源。

---

## 20. 反例、替代解释与 stop conditions

### 反例：red X 不等于 object deleted

2007 王女士照片后来恢复，本身就反驳这个偷换。

### 反例：平台停运不等于所有用户照片都永久丢失

用户可能：

- 已保存本地；
- 在别的平台有副本；
- 关停前完成导出；
- 亲友保存了副本。

平台数据删除只能证明平台不再提供该副本。

### 替代解释：相册访问失败

至少可能来自：

- 登录服务；
- 相册 DB；
- 图片 object store；
- image CDN；
- DNS；
- 浏览器插件；
- 客户端版本；
- 用户网络；
- ACL/session。

没有 packet/HTTP/log/HTML 时不能挑一个写成事实。

### Stop conditions

若只能得到：

- 后来怀旧文章；
- 一个当代 qzone 页面；
- 没打开的 archive locator；
- 需要重新公开普通私人照片的路径；

则停止提高结论置信度，保留缺失即可。

---

## 21. 本轮改变了什么

这个专题给旧网考古增加了一个以后可反复复用的原则：

> **“页面保存”与“生活记忆保存”不是同一层。**

一个 2008 年相册页面可能仍在 archive 里，但里面只剩缩略图；也可能原图 CDN 还活着，账号和相册目录却已经消失；甚至可能图片本身完整，却已经不知道是谁、什么时候、为什么上传。

相反，一个没有被 public Web archive 抓到的私人相册，也可能一直完整地保存在一个家庭自己的硬盘里。

因此旧网对普通生活的历史可见性不只是“哪个网页被保存了”，还必须问：

**哪一种过去被设计成公开页面，哪一种过去被锁在账号里，哪一种过去只存在于图片服务器，而平台死亡时又是哪一层先断。**

---

## 22. 饱和判断

本轮产生了新的：

- artifact/state distinction：`album shell / thumbnail / rendered image / original / semantic context`；
- transaction model：upload/view/shutdown/export；
- archive gap：`album capture != image-object capture`；
- historical visibility mechanism：private-memory archive bias；
- 2007 同时代故障证据；
- 2009 校园 BBS 普通用户照片发布证据；
- 2019 afterlife shutdown evidence。

因此不计入连续无实质新增轮次；当前阶段饱和计数仍为 **0/3**。
