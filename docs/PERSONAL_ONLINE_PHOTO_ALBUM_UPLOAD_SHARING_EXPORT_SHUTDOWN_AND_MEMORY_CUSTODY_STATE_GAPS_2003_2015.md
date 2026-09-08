# 个人网络相册、上传、分享、导出、停运与记忆保管权的状态缺口（2003—2015）

> Scope：只研究约 2003—2015 年中文旧网里，普通个人/家庭照片怎样进入网络相册、怎样通过 URL/账号/相册权限被分享、怎样跨 Web 与移动端备份，以及历史页面、图片字节、原图、相册元数据、导出和平台停运之间的状态缺口。
>
> 本文件不是摄影器材/作品论坛史。摄影论坛、EXIF、器材与二手交易已有 companion：[`PHOTOGRAPHY_FORUM_IMAGE_EXIF_CLASSIFIED_AND_ARCHIVE_STATE_GAPS_2000_2015.md`](./PHOTOGRAPHY_FORUM_IMAGE_EXIF_CLASSIFIED_AND_ARCHIVE_STATE_GAPS_2000_2015.md)。本题关心的是普通人的家庭、同学、旅行、恋爱、孩子与生活照片怎样被平台保管。
>
> life-history companion：[`tmzncty/how-people-lived/topics/from-paper-albums-to-platform-memory-photo-archives-sharing-and-memory-custody-china-1980s-2026.zh-CN.md`](https://github.com/tmzncty/how-people-lived/blob/main/topics/from-paper-albums-to-platform-memory-photo-archives-sharing-and-memory-custody-china-1980s-2026.zh-CN.md)。

---

## 1. 研究单位：相册页面、图片字节、原图和人的记忆不是同一个对象

至少区分：

- platform / 产品品牌；
- host / domain；
- account；
- album；
- album entry / photo entry；
- title / caption / comment；
- upload timestamp / capture timestamp；
- album order；
- public / private / password visibility state；
- share URL；
- viewer page / HTML；
- thumbnail；
- forum/blog resized image；
- uploaded original；
- EXIF / metadata；
- local source file；
- browser upload page；
- uploader control / client；
- mobile application；
- image host / CDN；
- authentication / passport / session；
- export package；
- migration target；
- shutdown notice；
- current live legacy page；
- historical archive capture；
- personally important memory represented by these artifacts。

最小状态机：

```text
PHOTO_CAPTURED
→ LOCAL_FILE_EXISTS
→ SELECTED_FOR_UPLOAD
→ UPLOAD_UI_OR_CLIENT_READY
→ TRANSFER_STARTED
→ SERVER_ACCEPTED
→ THUMBNAIL_OR_RESIZED_CREATED
→ ORIGINAL_STORED ?
→ ALBUM_ENTRY_CREATED
→ VISIBILITY_SET
→ SHARE_URL_CREATED (optional)
→ VIEWER_HTML_FETCHED
→ IMAGE_BYTES_FETCHED
→ ORIGINAL_DOWNLOADABLE ?
→ LOCAL_COPY_RETAINED ?

later:
→ MOBILE_BACKUP_ENABLED ?
→ PLATFORM_STILL_MAINTAINED
→ SHUTDOWN_ANNOUNCED ?
→ NOTICE_DELIVERED ?
→ NOTICE_NOTICED ?
→ EXPORT_OR_MIGRATION_INITIATED ?
→ PHOTO_BYTES_DOWNLOADED_OR_COPIED ?
→ ALBUM_CONTEXT_PRESERVED ?
→ POST_SHUTDOWN_RETRIEVABLE ?
```

固定：

```text
album page exists ≠ image bytes survived
thumbnail survived ≠ original survived
upload succeeded ≠ user retained local copy
share URL exists ≠ historical privacy state known
“无限” ≠ permanent-storage guarantee
platform account exists ≠ photo service still maintained
shutdown notice published ≠ user received it
notice received ≠ user noticed in time
export option exists ≠ export completed
photo migrated ≠ album hierarchy / caption / EXIF / privacy / timestamp migrated
public archive capture ≠ private family memory preserved
current page carrying a 2003/2008 timestamp ≠ verified historical DOM
```

本题把个人对自己历史影像仍然拥有定位、访问、复制、导出和迁移能力的状态称为 **memory custody / 记忆保管权**。

---

## 2. 与摄影论坛专题的边界

摄影论坛 companion 的主要研究单位是：

```text
thread / post / image / EXIF / equipment / classified / transaction
```

本题的主要研究单位是：

```text
account / personal album / family photo / upload workflow / visibility / long-term storage / export / shutdown
```

两者会在图片字节、缩略图、外链和 archive failure 上相交，但不能合并。

例如，一个 2008 年论坛帖子说“更多图片请看我的网易相册”，论坛专题研究的是帖子怎样把讨论指向外部图像对象；本题研究的则是：

- 这个 album URL 当时怎样组织图片；
- 用户是否保留原图；
- public/private 状态如何表达；
- 平台后来消失时，个人是否还能把这些照片带走。

---

## 3. 2003：`photo.163.com` 已被普通中文技术社区当作大量照片的在线存储/分享工具

HPE Community 当前仍有一条页面承载 **2003-10-31** 的用户帖子，标题为《给大家推荐一个好东西！无限量的网易相册》。帖子直接写出：

- `http://photo.163.com/`；
- “无容量限制”；
- 单张上传；
- “打包上传”多张图片；
- 打包下载；
- 网易通行证注册；
- 推广期免费。

来源：

- <https://community.hpe.com/t5/%E7%81%8C%E6%B0%B4%E5%8C%BA/%E5%88%86%E4%BA%AB%E6%88%91%E7%9A%84%E6%8A%80%E5%B7%A7-%E7%BB%99%E5%A4%A7%E5%AE%B6%E6%8E%A8%E8%8D%90%E4%B8%80%E4%B8%AA%E5%A5%BD%E4%B8%9C%E8%A5%BF-%E6%97%A0%E9%99%90%E9%87%8F%E7%9A%84%E7%BD%91%E6%98%93%E7%9B%B8%E5%86%8C/td-p/1587243>
- 证据等级：**B / current legacy page carrying contemporaneous user post**。

它可以支持：

- 2003 年用户已经把 `photo.163.com` 当作实际可用服务讨论；
- “无容量限制”、批量上传/下载等功能至少在用户说明中存在；
- 网易通行证是访问该服务的重要账号接口。

它不能支持：

- 2003 年网页 DOM、HTML、CSS、charset、session 与今天页面任何相似性；
- “打包上传”使用 ActiveX、Java Applet、Flash 或其他哪一种具体客户端技术；
- “无容量限制”构成永久保存承诺；
- 用户上传的图片今天仍在网易服务器。

因此本轮登记：

```text
historical locator: http://photo.163.com/
status: strong contemporaneous locator
historical capture: NOT VERIFIED IN THIS SLICE
```

---

## 4. 2007–2008：用户开始把“保存时间无限”与“把相册地址给别人”当作正常功能

2007 年一篇个人博客整理图片空间时，对网易相册写出：

- 空间：无限；
- 下载次数：无限；
- 保存时间限制：无限；
- 需要网易 ID；
- 支持密码。

来源：

- <https://filiron.blogspot.com/2007/01/blog-post_1540.html>
- 证据等级：**B（同时代用户整理）**。

这不是平台合同，却是很有价值的 user-expectation evidence：普通用户当时会把网络相册的未来寿命理解成产品选择条件。

固定：

```text
user describes “保存时间无限”
≠
service has archival permanence contract
```

2008 年 Oh My Media 作者则直接自述自己从 2005 年开始使用 Flickr、长期使用又拍网，照片达到数千张；文章把网络相册常见用途概括为：

- 与亲朋分享；
- 记录生活点滴；
- 公开展示。

来源：

- <https://ohmymedia.com/2008/06/02/792/>
- 证据等级：**B / contemporaneous first-person user account**。

这个个案可以证明“长期把大量生活图片交给网络相册”已经是现实可执行路径，但不能证明全国普及。

同年 KeyFansClub 一条仍在线的帖子把“更多图片请到相册地址看吧”指向：

```text
http://photo.163.com/photos/<user>/<album-id>/
```

来源：

- <https://keyfc.com/bbs/showtopic.aspx?forumid=2&forumpage=1&go=next&topicid=28193>
- 证据等级：**B / current legacy forum carrying contemporaneous platform-use evidence**。

2008 年另一份服务整理还记录过类似个人入口：

```text
http://photo.163.com/photos/<user>/
http://<qq-number>.photo.qq.com
```

这些都只能登记为 historical locator / URL pattern，不得因为当前网页或二手转载而推定 URL 在所有年份稳定。

---

## 5. 2009：上传页面存在，不等于家庭用户手里的原图可直接完成事务

2009 年太平洋电脑网网络相册评测记录：

- QQ 相册普通用户当时约有 200MB 空间；
- 单张图片存在约 2MB 限制；
- 许多数码相机原图需要预先处理；
- 作者专门提醒家庭用户未必熟悉图片处理；
- 网易相册提供上传控件，并区分快速上传自动压缩与保留原图用途的上传方式。

来源：

- <https://pcedu.pconline.com.cn/soft/wl/assist/0910/1852900_all.html>
- 证据等级：**B（同期产品评测）**。

这使上传状态至少需要拆成：

```text
local file exists
→ file dimensions / byte size acceptable ?
→ upload method available ?
→ browser / client compatible ?
→ upload accepted
→ server compressed / retained original ?
```

因此：

```text
site supports upload
≠
household user can upload current camera file without preprocessing
```

而且“上传控件”这个词本身不足以推断具体实现。没有历史 HTML、安装包或 contemporaneous manual，就不能把它写成 ActiveX。

---

## 6. 2011：移动端把“主动上传一批文件”推进成“长期自动把生活交给平台”

2011 年同期行业报道介绍网易“云相册”移动应用第三版，描述：

- Android / iOS；
- 选择或增量备份手机照片；
- 自动进入私密相册；
- 电脑与手机照片统一管理；
- 多人相册；
- 聚会、旅行、婚礼、家庭影集等协作场景；
- 没安装客户端的人仍可从网页加入多人相册。

来源：

- <https://www.doit.com.cn/p/94677.html>
- 证据等级：**B（同期行业报道，包含产品方信息）**。

这标志着 Web 相册与移动云备份开始衔接：

```text
manual Web upload:
拍照 → 导入电脑 → 选择 → 打开 Web → 上传

mobile backup:
拍照 → app 识别新增照片 → 备份
```

这里的 archaeological implication 很重要：

**用户越不需要主动进入 Web 上传页，未来 archive 越可能只保存服务的 public Web shell，而看不到真正承载私人记忆的数据流。**

所以：

```text
public Web significance may decline
while backend / private-account significance rises
```

这不是 Web 消失，而是事务向 authenticated mobile/backend state 移动。

---

## 7. 图片旧网必须把“HTML 存活”与“图像身体存活”分开

个人网络相册比普通文字博客至少多依赖四层：

```text
album HTML
+ thumbnail / resized image
+ original image
+ metadata / ordering / privacy state
```

可能出现：

1. 相册目录页还在，所有图片 404；
2. 缩略图在，原图链接失效；
3. 图片在，caption / album name / order 消失；
4. public landing page 在，登录后 private album 全不可见；
5. archive 保存图片字节，但无法知道原隐私状态；
6. 当前站点重新渲染旧数据，造成“旧正文 + 新模板 + 新账号状态”的 temporal collapse。

所以本仓未来任何网络相册 capture 都应分别记录：

- album HTML capture；
- thumbnail request；
- displayed/resized image request；
- original-image request；
- image host / CDN；
- Content-Type；
- dimensions；
- redirect/error/login state；
- known privacy state；
- whether bytes are archive replay or current live resource。

---

## 8. public/private 是最重要的历史可见性偏差之一

普通人的最重要照片往往并不是最公开的照片。

可能长期保存在：

- private album；
- password album；
- 只有好友可见的相册；
- 需要登录的手机云备份；
- 孩子/亲属照片；
- 病痛、葬礼、家庭内部照片。

公开 Web / 搜索引擎 / archive 更容易保存的却是：

- public album；
- 被论坛外链的图；
- 热门照片；
- public profile；
- 可匿名访问的 thumbnail。

因此固定：

```text
historian-visible photo archive
≠
ordinary person's personally-important photo archive
```

不能因为今天还能抓到一批 2008 年公开旅行图，就推断用户真正最在乎的家庭相册也同样被保存。

隐私规则：本仓研究普通个人相册时，优先记录 URL pattern、功能、状态和最小必要 evidence；不得批量重新发布普通人的家庭照片、儿童照片、联系方式或已经不再公开的私人内容。

---

## 9. 2019 网易相册关停作为 2003—2015 状态机的 afterlife 验证

2019 已超出本仓主时间范围，因此这里只把关停当作 earlier system 的 **afterlife / preservation consequence**，不扩成当代云存储史。

红星新闻 2019 年调查报道保存了最终关停公告文本：

- 最初原计划 2019-05-08 全面停止；
- 因部分用户反馈尚未下载，延期两周；
- 最终至 **2019-05-24 00:00**；
- 此后关闭服务器，用户无法登录、浏览、使用，数据不再保留。

来源：

- <https://static.cdsb.com/micropub/Articles/201906/c0ca9c68aab6dd135ef96b184206d61d.html>
- 证据等级：**B（同期调查 + 公告文本复录 + 同期第一人称）**。

它证明 earlier albums 的一个关键 state 不是永久的：

```text
ALBUM_AVAILABLE
→ SHUTDOWN_ANNOUNCED
→ DOWNLOAD_WINDOW
→ SERVER_CLOSED
→ DATA_NO_LONGER_RETAINED
```

### 9.1 dormant archive paradox / 休眠档案悖论

同一报道中的用户案例显示，一些人多年不再把网易相册当日常社交工具，却仍把学生时代、恋爱、孩子成长、去世亲人的照片留在里面；有人没有其他备份。

因此：

```text
low login frequency
≠
low archive value
```

旧平台越不再进入日常使用，用户越容易错过通知；但里面的内容反而可能越老、越不可替代。

### 9.2 notice-delivery gap / 公告—到达缺口

2019 同期报道还记录：

- 有用户长期主要使用手机 App，不常访问 Web；
- 有人称直到关停后才发现；
- 一名用户在 5 月中旬仍上传过照片；
- 部分邮件通知送达很晚；
- 用户认为网站公告并没有等于自己真正收到通知。

因此必须拆开：

```text
NOTICE_PUBLISHED
≠ NOTICE_DELIVERED
≠ NOTICE_NOTICED
≠ USER_HAS_STORAGE_TO_EXPORT
≠ USER_HAS_BANDWIDTH_TO_EXPORT
≠ EXPORT_STARTED
≠ EXPORT_COMPLETED
```

这对 old-Web archaeology 很关键：后来的“为什么用户没有及时下载”不能仅从公告发布日期反推用户已知情。

---

## 10. 2019 “一键搬家”只证明图片迁移描述，不能自动证明完整相册语义迁移

2019-04-28，科技媒体报道腾讯提供网易相册“一键搬家”到 QQ 空间，称用户登录 QQ 后可把网易相册图片同步到 QQ 空间。

来源：

- <https://www.ithome.com/0/421/306.htm>
- 证据等级：**B（同期科技媒体）**。

当前证据不足以证明以下字段一起迁移：

- 原始图像字节；
- EXIF；
- album hierarchy；
- 相册标题；
- caption；
- 评论；
- privacy；
- password semantics；
- original upload timestamp；
- capture timestamp；
- share URL。

所以固定：

```text
PHOTO_BYTES_MIGRATED
≠
MEMORY_CONTEXT_MIGRATED
```

以后如果获得历史迁移帮助页或样本，应逐字段验证，不应把“一键搬家”写成完整档案移植。

---

## 11. 海外 comparison boundary：平台停运与限时迁移并非中文互联网独有

全球对照主要写入 how-people-lived，本仓只保留边界结论。

2007 年 Yahoo Photos 关闭时，用户可以：

- 迁往 Flickr、Kodak Gallery、Shutterfly、Snapfish、Photobucket 等；
- 下载 full-resolution 图片；
- 部分情形购买 archive CD；
- 截止日前不处理则图片删除、无法再访问。

来源：

- <https://www.macworld.com/article/187070/yahoophotos-2.html>
- 证据等级：**B（同期报道）**。

这说明：

```text
shutdown deadline
+ export / migration route
+ post-deadline deletion
```

属于平台化照片存储的跨国共同问题，不应被解释成网易或中国互联网的独有现象。

但具体平台的：

- notice method；
- export completeness；
- original resolution；
- metadata preservation；
- private album handling；

必须逐平台核验。

---

## 12. 历史 locator 与本轮 M1 状态

### 12.1 当前可登记的 locator / pattern

```text
2003:
http://photo.163.com/

2008:
http://photo.163.com/photos/<user>/
http://photo.163.com/photos/<user>/<album-id>/

QQ-era example pattern reported in contemporary service lists:
http://<qq-number>.photo.qq.com
```

这些 locator 来自同时代用户帖子/服务整理，可以进入 candidate list。

### 12.2 本轮 historical capture 结果

本轮尝试继续向 `photo.163.com` 及相关历史相册 URL 的 archive / replay 方向推进，但**没有取得一份能按照本仓 METHOD 实际检查的 2003–2011 historical capture**。

因此本轮：

**M1 = NOT ACHIEVED IN THIS SLICE**。

未知项继续保持 unknown：

- historical response status；
- HTTP headers；
- `Content-Type`；
- charset；
- DOM；
- frameset / table layout；
- JS；
- cookie/session；
- NetEase Passport redirect；
- upload control implementation；
- browser requirement；
- original-image host / CDN；
- thumbnail/original relation；
- password/private album behavior；
- image download headers；
- archive rewrite effects。

按照 METHOD：

```text
this run did not verify a compliant historical capture
≠
Wayback / another archive has no capture
```

不得把负搜索结果写成历史不存在。

---

## 13. 浏览器与客户端考古要求

后续如取得 2003–2011 upload/help capture，优先检查：

1. form `enctype`；
2. file input 是否原生；
3. “打包上传 / 批量上传”是否调用独立客户端或插件；
4. uploader 是否要求 IE；
5. 是否出现 `ActiveXObject`、CAB、OCX、Java、Flash；
6. browser sniffing；
7. GB2312 / GBK / UTF-8；
8. upload limit 文案与客户端实际 limit 是否一致；
9. server-side resizing；
10. original/download endpoint；
11. image host 是否 cross-domain；
12. auth cookie 与 Passport host；
13. privacy/password check 在 HTML 层还是 image-byte request 层生效。

在取得 artifact 以前，禁止仅凭“上传控件”推断 ActiveX。

---

## 14. archive preservation matrix

| artifact | 可能存活 | 常见失败 | 能证明什么 |
| --- | --- | --- | --- |
| public album HTML | 是 | robots、动态 URL、login | 当时/后来存在相册表示 |
| thumbnail | 有时 | CDN/外链未抓 | 曾有图像对象，不等于原图 |
| resized image | 有时 | image host 与 HTML 分离 | 展示字节，不等于 original |
| original file | 较不确定 | 需权限/独立 endpoint/大文件 | 若验证可研究像素/metadata |
| private album | 较难 | login / robots / authorization | 缺失不能推出当时不存在 |
| captions/comments | 取决于页面 | AJAX/API 未抓 | 社交语境的一部分 |
| album order | 取决于 HTML/API | pagination / JS | 不能从散落 image bytes 自动恢复 |
| EXIF | 取决于原图/显示页 | strip / compression | 需要逐对象核验 |
| upload client | 较难 | 下载包消失 | 决定真实 browser executability |
| shutdown notice | 较易 | notice replaced | 证明平台发布，不证明用户收到 |
| export package | 极难 | private authenticated transaction | 是否真正把记忆迁出需要用户证据 |

---

## 15. 为什么这一题属于 old-Web archaeology，而不只是“云盘史”

网络相册在 2000s 中文 Web 中承担的不是今天单一“云备份”功能，而是同时兼具：

- 个人主页的图片身体；
- 论坛/博客外链图源；
- 家庭与同学共享；
- 旅行/聚会照片入口；
- 个人公开展示；
- 密码/私密相册；
- 后来的手机备份落点。

它处在一个非常典型的旧网转换带：

```text
HTML 页面
→ authenticated account
→ image storage
→ browser upload control
→ public URL
→ mobile app
→ backend cloud
```

因此，网络相册是研究“Web 页面如何逐渐让位给账户化、私有化、后台化数据”的理想对象。

---

## 16. 反例与后见之明风险

### 16.1 不把 2019 停运焦虑倒灌回 2003/2008

2007–2008 同期用户材料常明确把“无限”“保存无限”当作优点。不能写成早期用户普遍已经知道平台一定会死亡。

### 16.2 不把停运用户个案外推成全部用户

有人没有备份，也有人长期做多副本。停运报道可证明两种策略都存在，不能把一方写成普遍人格。

### 16.3 不把 public album 等同于 household archive

公开相册还包括网店商品、摄影作品、壁纸、论坛图床。判断 ordinary-life memory 必须看内容语境，不能只看“相册”标签。

### 16.4 不把当前 legacy page 冒充历史 capture

HPE、KeyFansClub 等今天仍能显示旧时间戳，只能作为 current rendering carrying old content；没有 memento datetime/HTTP/DOM 检查，不得写成原页面快照。

### 16.5 不把 archive absence 写成 historical absence

private/login/image-CDN 特别容易产生 preservation bias。

### 16.6 不重新公开私人家庭影像

研究功能与状态优先于重新展示普通人的照片内容。

---

## 17. 尚未确定

1. 2003–2006 `photo.163.com` 首页、帮助页、上传页的合格 WARC/Memento；
2. 2003 所谓“打包上传”的真实实现；
3. NetEase Passport 认证与 photo host 的 cookie/session 边界；
4. 2007–2011 original image / resized image / thumbnail URL schema；
5. 不同年代是否 strip/retain EXIF；
6. password/private album 是否在 image-byte 层真正阻止匿名请求；
7. QQ 相册早期 host / album hierarchy 的年代变体；
8. mobile cloud album 对 Web 旧相册是同库、迁移还是独立系统；
9. 2019 download/export package 的字段结构；
10. QQ 一键搬家是否保留 caption、album order、original timestamp、EXIF、privacy；
11. shutdown notice 是否通过站内、email、SMS、App push 分渠道发送，以及各自实际到达率。

---

## 18. 下一轮最值钱的 artifact

1. `photo.163.com` 2003–2006 homepage/help/upload historical capture；
2. 2007–2010 公开普通相册的最小化样本：只记录页面结构、图片 host 与 URL pattern，不批量下载/重发私人照片；
3. 2009 uploader/browser artifacts，确认压缩与 original-preserving path；
4. 2011 mobile cloud album help / client manual；
5. 2019 shutdown/download/export page；
6. 腾讯“一键搬家”帮助/字段说明；
7. 一个 HTML survives but image bytes missing 的实证样本；
8. 一个 thumbnail survives but original missing 的实证样本。

---

## 19. 本轮证据强度摘要

| Claim | Evidence | Grade | Confidence |
| --- | --- | --- | --- |
| 2003 年 `photo.163.com` 被用户作为无容量限制、批量上传/下载的相册推荐 | HPE 当前遗留页承载 2003 用户帖 | B / legacy contemporaneous | medium-high |
| 2007 用户把“保存时间无限”当作服务属性 | 同期个人博客整理 | B | medium |
| 2008 用户实际以网络相册记录生活、分享亲友并累计数千张照片 | Oh My Media 同期第一人称 | B | high for case |
| 2008 论坛帖外链网易个人相册 | KeyFansClub legacy page | B | high for use existence |
| 2009 upload size/compression/original path 对家庭用户构成真实门槛 | PConline 同期产品评测 | B | medium-high |
| 2011 手机增量备份与多人相册把 private backend importance 提高 | DOIT 同期报道 | B | medium-high |
| 2019 earlier albums 确实进入限时导出后停止保留 | 红星新闻公告复录 | B | high |
| 2019 公告发布与用户实际知情存在缺口 | 同期第一人称采访 | B | high for cases |
| 一键搬家至少被描述为可把图片同步到 QQ 空间 | IT之家同期报道 | B | medium-high |
| 海外也存在 deadline + migration + deletion 的照片平台退出 | Yahoo Photos 2007 | B | high for mechanism |

---

## 20. 饱和判断

本轮出现新的、此前仓库未独立建模的 old-Web 状态问题：

- **memory custody / 记忆保管权**；
- **dormant archive paradox / 休眠档案悖论**；
- **notice-delivery gap / 停运公告—实际到达缺口**；
- **public archive / private memory visibility bias**；
- **photo-byte migration / memory-context migration gap**。

并取得 2003、2007、2008、2009、2011 的同时代 old-Web 证据和 2019 afterlife 反证。

因此本阶段连续“无实质新增”计数：**0**。

不进入 closure。

---

## 21. 本题改变了旧网考古的哪一点

旧网页考古很容易天然偏向“还能看到的页面”。网络相册提醒我们，普通人真正重要的历史对象可能恰恰最不容易被 Web archive 看见：

- 登录后的私密相册；
- 孩子照片；
- 已去世亲属照片；
- 手机自动备份；
- 只有家庭知道密码的相册；
- 原图；
- 停运前一次性导出的压缩包。

所以，一个平台今天留下了很多 public HTML，并不等于这个平台成功保存了它最重要的普通生活史。

甚至可以出现相反情况：

**公开 Web 作为“网站”保存得还不错，而真正寄存在那个网站里的人的生活，已经没有了。**