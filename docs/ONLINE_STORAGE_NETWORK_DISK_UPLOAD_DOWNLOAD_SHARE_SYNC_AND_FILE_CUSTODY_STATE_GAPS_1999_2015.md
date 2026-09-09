# Online storage, network disks, upload/download, sharing, sync and file-custody state gaps · 1999–2015

> Status: research note / evidence contract.
>
> Scope: **约 1999–2015 中文 Web 中的网络硬盘、网络 U 盘、个人网盘、临时文件中转、公开/私密分享、客户端同步与相关 archive state gaps**。
>
> This is not a global history of cloud computing, FTP, enterprise storage, or post-2015 personal cloud markets.
>
> Cross-repo life-history note:
> `tmzncty/how-people-lived/topics/from-floppy-disks-to-cloud-sync-personal-file-portability-digital-baggage-and-working-memory-china-1980s-2026.zh-CN.md`

---

## 0. Why this belongs in old-web-archaeology

旧网研究很容易把“网络硬盘”写成一个网页产品：

```text
有首页
+ 有“上传”按钮
+ 有“下载”按钮
= 网盘已经被复原
```

这是不够的。

一个普通用户在 2005 年把 `paper.doc` 从网吧电脑送到 Mofile，第二天再从学校机房取回，背后至少经过：

```text
现实中的人
→ 浏览器 / QQ 客户端
→ 登录账号 / session
→ 本地文件选择
→ upload request
→ Web / application server
→ storage object
→ metadata / quota row
→ private box or relay semantics
→ later login / share URL
→ policy / expiry / ACL check
→ download response
→ local filesystem write
→ user opens the file
```

所以本篇第一条硬规则是：

```text
network-disk page survives
!= account survives
!= file-list survives
!= payload survives
!= share token survives
!= download succeeded historically
!= local copy survived
```

---

# 1. Scope boundary

## 1.1 In scope

约 1999–2015 中文互联网中的：

- “网络硬盘 / 网络 U 盘 / 网盘 / 云盘”页面；
- QQ 网络硬盘、网易网盘、Mofile 等 ordinary-Web / client-facing surfaces；
- 上传、下载、删除、重命名、文件夹等文件操作；
- quota / single-file limit；
- 私人保管与临时中转；
- share link / public file / password / expiry；
- browser 与专用客户端混合事务；
- Windows shell / QQ client / ActiveX / Java / browser upload 等历史客户端依赖；
- 2012–2015 同步盘与跨终端访问；
- historical captures 中页面壳、列表、payload、token、session 的分离；
- 停服、缩容、删除与数据导出对应的状态问题。

## 1.2 Out of scope

本篇不做：

- 全球 cloud computing 通史；
- 2020s NAS / personal cloud 市场；
- 企业对象存储；
- 恢复或闯入真实私人账号；
- 下载私人、侵权或敏感文件；
- 批量重新发布普通用户旧网盘内容；
- 把 FTP / ARPANET 全史塞进本仓；
- 把 2016 以后个人云盘调整写成仓库主体。

2016 停服潮、2020 远程协作、2025 混合备份主要属于 `how-people-lived` 的跨时期生活史；本仓只在必要处作为 later consequence 提及。

---

# 2. Prehistory boundary：FTP 很早，但本仓不是 FTP 全球史

1980 RFC 765 已经定义远程文件存储和取回、用户认证、存储分配等机制。

Source:

- RFC Editor, RFC 765, 1980: <https://www.rfc-editor.org/info/rfc765/>

这只用于边界说明：

```text
remote file transfer existed before the Web
!= public consumer Web storage existed
!= ordinary Chinese users had remote storage access
```

中国 1994 年前已经有科研网络、远程登录和电子邮件实验；1994-04-20 才是全功能接入国际 Internet 的明确节点。

Sources:

- 中国科学院档案馆：<https://www.acas.ac.cn/byyxc/bydt/202404/t20240422_7174874.html>
- CNNIC 大事记：<https://www3.cnnic.cn/n4/2022/0401/c87-912.html>

本仓因此不把 1980s 科研传输当作“中文旧 Web 网盘”。

---

# 3. Terminology contract：network disk != backup != sync != relay

## 3.1 Physical removable storage

```text
floppy / optical disc / USB drive
```

文件跟随物理介质移动。

## 3.2 Remote personal storage

```text
local file
→ explicit upload
→ remote object
→ explicit download later
```

用户主动搬运副本。

## 3.3 Temporary relay

```text
upload
→ short retention window
→ recipient / later device downloads
→ object expires
```

目标是传递，不是长期保存。

## 3.4 Synchronization

```text
local folder A
↔ sync client
↔ server state
↔ sync client
↔ local folder B
```

用户不一定逐个执行 upload/download。

## 3.5 Backup

备份强调独立恢复副本，不等于“远端还有一份”。双向同步会把删除和损坏传播到其他设备，因此：

```text
sync copy != independent backup
```

## 3.6 Share

分享不是存储本身：

```text
object exists
→ share policy created
→ token / URL generated
→ recipient opens
→ ACL / expiry / password checked
→ bytes returned
```

因此：

```text
object exists != share active
share URL exists != object exists
HTTP 200 share wrapper != file bytes returned
```

---

# 4. Evidence grades used here

沿用仓库 METHOD：

- **A**：同期官方帮助、服务公告、可验证历史 capture、原始协议/手册；
- **B**：同期技术媒体、操作实测、论坛/博客第一人称；
- **C**：后来的机构史、服务回顾；
- **D**：本篇的状态机、archive-gap reconstruction。

特别规则：

> 当前互联网上还能打开一篇 2005 年新浪技术文章，可以证明那篇文字今天仍被服务；**不能证明 2005 年的原始页面 DOM、charset、图片、下载链接和广告资源就是今天的样子。**

---

# 5. 1999–2002 overseas comparison：consumer Web storage existed before Chinese network disks matured

这部分只作可比对象，不扩写为全球仓库。

1999 年 X:drive 已经提供 Web-based hard-drive service，25MB 免费空间，可以组织、保存、发布和分享文档、表格、演示、图片、音乐和视频；2000 年 01net 的操作文章说，用户可以在任何联网电脑上通过浏览器重新访问文件。

Sources:

- InternetNews, 1999-12-01: <https://www.internetnews.com/small-business/xdrive-secures-20-million-in-funding/>
- 01net, 2000-07-03: <https://www.01net.com/actualites/sauvegarder-ses-donnees-sur-le-web-112928.html>
- WIRED, 1999-08-09, i-drive and trust: <https://www.wired.com/1999/08/file-storage-matter-of-trust/>

这提供一个海外对照：

```text
Web storage as “any browser / any computer”
```

并非中国 2004–2005 才独立出现的想法。

但 1999 年海外 consumer service ≠ 1999 年中文普通用户已经拥有同等服务可及性。

---

# 6. 2004 QQ 网络硬盘：Web / IM client mixed surface

2004-07-07 的同期报道记录 QQ 网络硬盘：

- 普通用户 16M；
- QQ 会员 128M；
- 需要 QQ2004 Beta 或更高版本；
- 宣传直接以 U 盘插拔和刻光盘作为要替代的操作。

Source:

- cnBeta, 2004-07-07，《QQ推出128M网络硬盘!》：<https://www.cnbeta.com.tw/articles/4207.htm>

Evidence grade：**B**。

这类对象对 old-Web archaeology 特别危险，因为它不是纯 browser transaction。

可能链路：

```text
QQ executable
→ authenticated QQ account
→ network-disk panel
→ service API / HTTP request
→ storage backend
```

而公开 Web 只可能留下：

- 宣传页；
- 下载 QQ 客户端页；
- 帮助页；
- 可能的 `disk.qq.com` shell。

因此固定：

```text
historical web shell
!= historical QQ client functionality
```

以及：

```text
client version requirement documented
!= archived executable tested
!= original backend still reachable
```

---

# 7. 2005 “网络优盘”横评：ordinary-use vocabulary and capacity constraints

2005-08-30 同期文章直接把媒介谱系写成：软盘 → U盘 → 网络优盘，并列出：

- 网易网盘 `wp.163.com`：280M 免费；
- Mofile：1024M 接力站 + 8M 保管箱；
- QQ 硬盘 `disk.qq.com`：16M 免费；
- 其他网络硬盘。

Source:

- 新浪科技 / 天极 yesky，2005-08-30：<https://tech.sina.com.cn/s/2005-08-30/0909706572.shtml>

Evidence grade：**B / contemporaneous review**。

这条 source 同时告诉我们：

```text
service listed
!= user registered
!= user uploaded
!= user trusted it with important files
```

但它很适合证明 2005 年“网络优盘”已经成为当时技术媒体可以向普通 PC 用户解释的类别。

---

# 8. Mofile 的“保管箱 / 接力站”：同一站点中的两种 retention state machine

2005-09-08 的横向评测记录：

- Mofile 8MB 保管箱：个人长期空间；
- 1024MB 接力站：适合大文件；
- 接力站文件最多存三天，之后自动删除。

Source:

- 新浪科技 / IT.COM.CN，2005-09-08：<https://tech.sina.com.cn/s/s/2005-09-08/1159715065.shtml>

Evidence grade：**B**。

因此不能画成：

```text
Mofile file = permanent remote file
```

至少应分：

### persistent-box transaction

```text
LOGIN
→ BOX_AVAILABLE
→ FILE_SELECTED
→ UPLOAD_ACCEPTED
→ OBJECT_PERSISTED
→ METADATA_VISIBLE
→ QUOTA_UPDATED
→ later retrieve/delete
```

### relay transaction

```text
FILE_SELECTED
→ RELAY_UPLOAD
→ OBJECT_PERSISTED
→ TEMP TOKEN / ACCESS ID
→ RETENTION TIMER STARTS
→ RECIPIENT DOWNLOADS ?
→ TIMER EXPIRES
→ OBJECT DELETED / UNAVAILABLE
```

硬边界：

```text
relay upload success
!= recipient downloaded before expiry
```

以及：

```text
historical share / relay URL survives in a forum post
!= historical payload survives today
```

---

# 9. Upload state machine

复原旧网“上传”必须至少考虑：

```text
U0 local file exists
U1 user selects file
U2 browser/client knows path/name
U3 authenticated session valid
U4 quota allows upload
U5 single-file-size policy allows upload
U6 request begins
U7 request body fully reaches server
U8 server accepts transfer
U9 storage backend persists bytes
U10 metadata row commits
U11 quota/index updates
U12 UI reports success
U13 later read-back succeeds
```

因此：

```text
U12 “上传成功” screenshot
!= U9 durable object independently verified
```

可能存在：

- 页面显示成功但 metadata/write 延迟；
- 字节写入但列表未更新；
- 文件列表存在但 object 丢失；
- quota 更新失败；
- 客户端断线后 partial upload；
- 服务器接受但后来因 policy 删除。

旧 Web capture 通常只能保存 U0–U3 的 UI 外壳，几乎无法证明 U7–U13。

---

# 10. Download state machine

```text
D0 object historically existed
D1 user has file entry / share URL
D2 account/session/token valid
D3 ACL permits access
D4 retention window not expired
D5 metadata lookup succeeds
D6 payload backend returns bytes
D7 HTTP/client stream completes
D8 local filesystem writes file
D9 checksum/size/content is complete
D10 application opens file
D11 user recognizes it as intended version
```

硬边界：

```text
download button captured != D6
HTTP 200 HTML wrapper != file payload
D7 network completed != D8 local disk safe
same filename != D11 same intended version
```

---

# 11. File-list state machine

历史 archive 中最容易误判的是“文件列表”。

一个列表 row 可能包含：

```text
filename
size
upload time
file type
object id
folder id
owner id
share flag
```

但列表是 metadata，并不是 payload。

固定：

```text
file-list row survives
!= payload survives
```

反过来也可能：

```text
payload survives in cache
!= original metadata/context survives
```

如果只有裸文件，没有 owner / folder / date / description，不能声称“完整恢复了某人的网盘”。

---

# 12. Quota is a state, not just a marketing number

2004–2005 资料里 16MB、128MB、280MB、1024MB 等数字经常出现。

必须拆开：

```text
advertised plan quota
!= account-specific quota
!= free space remaining
!= maximum single-file size
!= temporary relay allowance
!= actual stored bytes
```

例如 Mofile 的 1024MB 接力站不能和 8MB 保管箱直接相加写成“用户有 1032MB 永久空间”。

同理，QQ 会员 128M ≠ 普通账号 128M。

---

# 13. Browser, client and plugin archaeology

历史在线存储可能依赖：

- plain HTML file input；
- JavaScript；
- ActiveX / upload control；
- Java applet；
- proprietary QQ client；
- Windows shell integration；
- local sync client。

因此 preservation 不能只问“网页在不在”。

需要记录：

```text
browser requirement
OS requirement
client version
plugin/control requirement
form action / endpoint
cookie/session dependency
upload mechanism
subresources
```

尤其当页面说“请安装最新版客户端”时：

```text
page rendered
!= transaction executable
```

---

# 14. 2008 ordinary Web trace：网络硬盘已经变成可整理的 service ecosystem

2008-01-30 的新浪博客文章整理多个“免费网络硬盘 / 网络 U 盘”，并描述 Yahoo 公文包、永硕等服务的容量和分享方式。

Source:

- 新浪博客，2008-01-30：<https://blog.sina.com.cn/s/blog_4b02f08c01008fko.html>

Evidence grade：**B/C / contemporaneous user-curated page**。

这条材料的价值不是平台数字一定完全准确，而是它显示：

> 当时普通 Web 内容已经会把多个在线存储服务当成可以选择、比较、收藏的一类工具。

但：

```text
blogger listed service
!= blogger verified every backend state
```

遇到容量、期限或功能数字时仍应与同期官方/媒体交叉核对。

---

# 15. 2008 overseas comparison：Dropbox moves the archaeology target from “Web disk” to “sync state”

Dropbox 2008-09-11 public launch 的创始人第一人称材料，以忘带 U 盘导致无法继续工作为起点。

Source:

- <https://blog.dropbox.com/topics/company/dropbox-launches-to-the-public>

同期报道又记录免费 2GB、Windows/Mac/Linux client 和 Web access。

Source:

- ＠IT, 2008-09-12：<https://atmarkit.itmedia.co.jp/news/200809/12/dropbox.html>

这不属于中文旧网本体，但它给中文 2012–2015 sync products 一个非常清晰的比较框架：

```text
Web disk archaeology asks:
was file uploaded and later downloaded?

sync archaeology must additionally ask:
which local version became server version, and when did device B converge?
```

---

# 16. Sync state machine

```text
S0 local file A exists
S1 watcher notices change
S2 client authenticates
S3 local version/hash determined
S4 server compares remote state
S5 upload begins
S6 server commits version V2
S7 device B polls / receives notification
S8 B downloads V2
S9 B writes local version
S10 local indexes agree
```

Conflict path：

```text
A edits V1 → V2a
B edits V1 → V2b
before convergence
→ conflict / overwrite / duplicate / merge
```

所以固定：

```text
sync enabled != all devices converged
same filename != same bytes
same modified time != same causal history
```

历史 screenshot 显示绿色勾号也只证明某个 UI 状态，不足以证明远端和所有设备的一致性。

---

# 17. 2012 Baidu Netdisk：cross-device language becomes explicit

2012-03-23 百度网盘公测：

- 15GB 初始空间；
- 1GB 单文件上传；
- Windows / Android；
- Web access；
- 跨平台同步；
- 链接、短信/邮件等分享路径。

Sources:

- IT之家，2012-03-23：<https://www.ithome.com/0/013/422.htm>
- 中新网 / CNTV，2012-05-07：<https://news.cntv.cn/20120507/111385.shtml>
- 第一财经转载同期报道：<https://www.yicai.com/news/1559633.html>

Evidence grade：**B**。

这里的 archaeology target 已经至少有三类 surface：

```text
Web UI
Windows sync client
mobile client
```

同一个账号看见“同一文件”，不意味着三个 surface 的功能、权限和缓存行为相同。

---

# 18. 2013 storage-space war：quota abundance creates a later archaeology trap

2013 年技术媒体记录国内云盘大量免费空间竞争，从 100GB 到 1TB、2TB、10TB 等宣传不断出现。

Sources:

- 快科技，2013-09-02：<https://news.mydrivers.com/1/274/274622.htm>
- 同期个人教程：<https://albertblog.tw/641/%E3%80%90app%E8%BB%9F%E9%AB%94%E3%80%91%E5%85%8D%E8%B2%BB%E9%9B%B2%E7%AB%AF%E7%A9%BA%E9%96%93%EF%BC%8E%E7%99%BE%E5%BA%A6%E9%9B%B2>

Evidence grade：**B**。

历史研究必须抵抗这种推断：

```text
2TB promotion
→ every user had 2TB
→ every user filled 2TB
→ every file survived
```

四步都不成立。

需要分别记录：

```text
campaign eligibility
claim / activation state
account quota after activation
used bytes
later policy changes
```

---

# 19. Share state machine

```text
H0 object exists privately
H1 user selects share
H2 public/private/password policy selected
H3 token / URL generated
H4 expiration recorded
H5 recipient obtains link
H6 link request reaches service
H7 token resolves
H8 ACL/password passes
H9 object still exists
H10 bytes rendered/downloaded
H11 recipient saves local copy
```

硬边界：

```text
forum preserves H5 URL
!= H7 today
!= H9 today
```

因此旧论坛中大量 `mofile.com/...`、网盘链接本身是**事务残骸**，不是仍可访问内容的证据。

---

# 20. Link rot has two layers

普通网页链接失效通常可以画成：

```text
page URL → page gone
```

网盘分享链接至少有：

```text
share wrapper URL
→ token resolution
→ metadata
→ object payload
```

所以可能出现：

- wrapper 活着，payload 死了；
- wrapper 重定向到新服务；
- token 失效；
- payload 因期限自动删除；
- owner 删除；
- account 注销；
- policy 禁止分享；
- 页面仍显示文件名但不再提供下载。

这也是为什么 old-Web archaeology 不能只以 HTTP status 判断网盘资源保存状态。

---

# 21. Shutdown / export transaction: a service can remain readable after it stops being writable

虽然本仓主体截止约 2015，2016 个人网盘退出潮是理解 1999–2015 accumulation model 的直接 consequence，因此只保留状态边界。

360 云盘后续停服策略曾先关闭上传、分享、预览等写入/表现功能，只保留下载；因集中迁移，又按用户数据量延长下载期限。

Sources:

- 360 社区公告：<https://bbs.360.cn/thread-14620422-1-1.html>
- 人民网关于多家网盘调整：<https://it.people.com.cn/n1/2016/0507/c1009-28332179.html>

这说明服务生命周期不是：

```text
LIVE → DEAD
```

而更像：

```text
FULL SERVICE
→ SHARE DISABLED
→ PREVIEW DISABLED
→ WRITE DISABLED
→ DOWNLOAD-ONLY
→ DEADLINE EXTENDED ?
→ ACCOUNT / OBJECT DELETION
```

所以 historical capture 必须标注具体日期和当时 capability，而不能简单说“2016 年某盘关闭”。

---

# 22. Exit state machine

```text
E0 shutdown/policy notice published
E1 user receives or notices notice
E2 user remembers credentials
E3 authentication succeeds
E4 account inventory loads
E5 user selects files
E6 download begins
E7 all intended bytes arrive locally
E8 local copy is verified
E9 user knows backup location
E10 remote service finally removes objects
```

硬边界：

```text
export offered != user noticed
user noticed != login succeeded
login succeeded != all files downloaded
all files downloaded != integrity verified
```

所以“给了几个月迁移期”不能直接写成“用户数据已经安全迁走”。

---

# 23. Historical archive attempt in this slice

本轮针对以下历史对象进行了 locator / replay 探索：

- `disk.qq.com`，约 2004–2005；
- `wp.163.com`，约 2005；
- `www.mofile.com`，约 2005。

公开搜索没有返回一条能直接作为本轮 verified memento 使用的对应 capture。

随后尝试直接请求类似：

```text
https://web.archive.org/web/20050901000000/http://disk.qq.com/
https://web.archive.org/web/20050901000000/http://wp.163.com/
https://web.archive.org/web/20050901000000/http://www.mofile.com/
```

当前访问链因 URL safety / replay restriction 拒绝构造的 historical URL，没有取得：

- capture datetime；
- original URL；
- historical HTTP status；
- charset；
- DOM；
- form action；
- JS / ActiveX / client references；
- subresources；
- authenticated file list；
- historical file payload。

因此本轮结论严格写为：

> **M1 verified capture: NOT ACHIEVED IN THIS SLICE.**

它只表示：

> 当前这一轮没有验证到合格 replay。

绝不能改写成：

> Wayback 没有保存这些站点。

这符合仓库 `docs/METHOD.md` 的 negative-evidence contract。

---

# 24. Preservation levels for online-storage archaeology

建议以后采用 S0–S5：

## S0 — locator / mention only

只有同期文章、域名、服务名或搜索 locator。

不能声称 capture verified。

## S1 — public shell capture

可验证历史首页 / 帮助 / 登录 / 上传 UI。

可研究：

- charset；
- layout；
- browser/client requirement；
- public copy；
- form structure。

不能研究真实私人文件状态。

## S2 — public metadata capture

合法公开的历史分享页中可验证：

- filename；
- size；
- date；
- owner/pseudonym where ethically safe；
- expiry language；
- share mode。

payload 不一定存在。

## S3 — permitted public payload capture

合法公开、非敏感、版权允许研究的文件 payload 与 metadata 同时存在。

仍不代表 owner 的其他私人目录。

## S4 — transaction semantics reconstructed

通过同期手册、页面、日志/截图等能较强重建：

- quota；
- upload/download stages；
- ACL；
- expiry；
- client/browser dependencies；
- share-token semantics。

无需、也不应暴露私人文件内容。

## S5 — bounded public replay

在合法公开的 historical artifact 上，可以验证：

```text
historical page
→ historical public metadata
→ historical permitted payload / resource
```

并记录所有缺失子资源与不可复原后台。

私人账号不应成为追求 S5 的对象。

---

# 25. Privacy / ethics boundary

网盘 archaeology 比普通网页更需要克制。

一个旧 share link 可能包含：

- 个人身份证扫描；
- 简历；
- 家庭照片；
- 工作文件；
- 学生作业；
- 财务资料；
- 私人聊天导出；
- 软件、书、影视等版权内容。

因此：

> **historical availability does not create a research entitlement to republish personal files.**

优先保存：

- 服务结构；
- UI；
- 公开帮助；
- 状态语义；
- 非敏感公开示例；
- file lifecycle。

不要把“文件真实内容”当成网盘 archaeology 完成度的唯一标准。

---

# 26. Archive visibility bias

公共 archive 最容易保存：

- landing page；
- promotion；
- help；
- signup；
- client download page；
- service notice。

最难保存：

- authenticated account state；
- private directory tree；
- payload bytes；
- quota remaining；
- ACL；
- token secret；
- temporary relay object；
- local sync database；
- final user-side file write。

因此固定：

```text
archive-visible network-disk culture
!= ordinary personal file practice
```

更进一步：

> 最容易保存的恰恰是“服务商说自己能做什么”，最难保存的是“普通人那天到底成功把哪个文件带到了下一台机器”。

---

# 27. Evidence matrix

| Claim | Best evidence | Current grade | Do not overclaim |
|---|---|---:|---|
| QQ 2004 有网络硬盘、普通 16M / 会员 128M | 同期技术报道 | B | 不等于每个 QQ 用户都使用 |
| 2005 网络优盘作为类别存在 | 同期横评 | B | 不等于家庭普及 |
| Mofile 有保管箱与三天接力站 | 同期横评 | B | 不等于所有账号策略永久一致 |
| 2008 普通 Web 内容整理多个网盘 | 同期博客 | B/C | 不等于作者验证全部服务 |
| 2012 百度网盘提供跨端同步 | 同期报道 | B | 宣传支持 != 所有设备稳定同步 |
| 2013 空间大战 | 同期技术媒体 | B | advertised quota != used bytes |
| historical QQ/Mofile capture | 本轮未验证 | — | locator/replay failure 不能当无存档证据 |

---

# 28. What this changes in old-Web archaeology

此前很多旧网对象可以主要围绕“页面是否存在”展开。

网络硬盘迫使研究单位继续下潜：

```text
page
→ account
→ session
→ metadata
→ payload
→ policy
→ retention timer
→ client
→ local filesystem
```

它是一个典型的 **transaction-deep Web object**：

> 页面往往是最容易保存的部分，却不是决定普通用户能不能继续生活/工作最重要的部分。

真正改变人的，是那份文件能不能在另一台机器上重新成为可用对象。

---

# 29. Counterexamples and hindsight risks

## 29.1 “network disk existed” != “USB became obsolete”

同期宣传常这么写，但后续长期是混用状态。

## 29.2 “large quota” != “durable custody”

免费 TB 空间和平台长期持续是不同变量。

## 29.3 “share page captured” != “file captured”

wrapper 和 payload 必须分开。

## 29.4 “sync client existed” != “users stopped making manual copies”

实际生活中往往仍有本地文件、聊天附件、U盘、邮件和多个云盘并行。

## 29.5 “service closed later” != “earlier service was useless”

停服风险是历史后果，不能用后见之明抹掉 2005 年一个人当时真实获得的异地文件可达性。

---

# 30. Next research targets

1. 取得 `disk.qq.com` 2004–2006 verified capture；
2. 取得 `wp.163.com` 2004–2006 verified capture；
3. 取得 Mofile 2005–2008 public shell / help / share capture；
4. 找到 QQ 客户端网络硬盘原始帮助、截图或 executable/manual evidence；
5. 进一步核 Mofile “保管箱 / 接力站”的官方期限与 token semantics；
6. 找合法公开、非敏感的 old share artifact，验证 wrapper → metadata → payload 的保存层级；
7. 核查 2012–2015 同步客户端 conflict / version behavior；
8. 研究旧网盘链接在 BBS / 博客中的 link rot，而不重新分发其内容。

---

# 31. Cross-repo synthesis

Life-history repo 的问题是：

> **一个人换一台机器、一个宿舍、一个办公室或一座城市以后，未完成的事情能不能继续。**

本仓的问题是：

> **那份文件从浏览器/客户端进入远端以后，究竟经过了哪些今天最难被 archive 保存的状态。**

两边合起来以后，不能再把“网盘”写成一个抽象产品类别。

它是一条真实生活链：

```text
person
→ local machine
→ file
→ client / browser
→ account
→ network
→ remote object
→ metadata / policy
→ later device
→ local file again
→ unfinished life continues
```

而 old-Web archaeology 的职责，就是明确指出这条链里哪些环节真的有证据，哪些今天只剩页面壳，哪些从来不应该为了“完整复原”而去侵犯普通人的私人数字行李。
