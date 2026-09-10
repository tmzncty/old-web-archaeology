# Online Memorial, Memorial Page, Deceased-Account Persistence and Archive State Gaps, China 1998–2015

## Scope

本笔记研究约 **1998–2015 中文旧 Web** 中“人已经死亡，但页面/账号/留言仍可能继续存在”这一类对象。

主要对象包括：

- 专门建立的网上纪念馆；
- 烈士陵园、墓园或纪念机构建立的网上纪念页面；
- 为普通逝者建立的个人纪念页；
- 原本属于活人的博客、QQ/Qzone、个人主页等，在本人去世后继续被访问、留言或保存的页面；
- 与这些页面相关的账号、认证、留言、虚拟祭奠、上传内容、保存与删除状态。

本仓**不**写一部完整中国殡葬史，也不把 2020s 微博/B站/微信的现代逝者账号规则反向投射到 2000s。跨国前史、现实生命历程、2015–2026 的数字遗产和平台治理变化见 sister repository：

- `tmzncty/how-people-lived/topics/from-visiting-a-grave-to-keeping-an-account-alive-mourning-digital-remains-and-posthumous-social-presence-china-1980-2026.zh-CN.md`

按照仓库方法，必须始终保持：

> `person != death event != memorial subject != memorial creator != account owner != page != capture != platform state != offline mourning outcome`

---

## 1. Evidence contract

沿用仓库 A/B/C/D 证据分级：

- **A**：同时代原始页面、WARC、原始政策/手册、可核验 HTML/HTTP artifact；
- **B**：同时代新闻、记者现场观察、当事人同期采访；
- **C**：后来回忆；
- **D**：研究者状态机复原或机制推断。

本轮有若干准确到 host / path 的同期 locator，并有 2007–2008 同期报道和普通人第一人称材料；但**没有成功取得一份满足 M1 条件的 1998–2010 中国网上纪念馆 historical memento/WARC**。

因此以下技术项仍是 unknown：

- historical HTTP status；
- response header / charset；
- DOM / frameset / table / CSS layout；
- form `action`、GET/POST；
- cookie / session；
- login / creator authentication；
- virtual-offering transaction backend；
- comment moderation backend；
- visitor counter implementation；
- image/audio/video hosting topology；
- page-deletion and export workflow；
- site shutdown / domain migration behavior。

**同时代文章里的 URL 是 locator，不是 verified capture。**

---

## 2. Object families must not be collapsed

### 2.1 Purpose-built memorial page

页面从建立之初就以“被纪念者已去世”为前提。

典型状态：

```text
creator account
→ deceased-person profile / memorial subject
→ biography / dates / photo
→ memorial page published
→ visitors arrive
→留言 / 献花 / 点烛 / 点歌等虚拟动作
→ moderation / maintenance
→ continued hosting / deletion / migration
```

### 2.2 Institutional memorial / cemetery page

烈士陵园、墓园、纪念机构等可以建立由组织维护的页面。它与普通家庭个人纪念页不同：

- page owner 可能是机构；
- subject identity 可能来自档案而非用户自填；
- maintenance horizon 可能依赖机构预算；
- visitor/comment permissions 可能更严格。

### 2.3 Ordinary account later used as a memorial

博客、个人主页、QQ 空间等原本不是纪念馆。主人死亡以后，页面可能继续存在并被亲友访问。

这类对象必须与 purpose-built memorial 分开：

```text
account created for living user
→ years of ordinary activity
→ user dies
→ platform may not know
→ account becomes inactive
→ friends/family may continue visiting/commenting
→ credentials / phone / email may expire
→ content may persist, be deleted, be stolen, or become unreachable
```

### 2.4 Private digital estate / non-public account state

私信、账号余额、支付信息、云文件、好友列表、登录凭证等不是“公开 memorial page”。

公共 Web archaeology 不应因为研究数字遗产，就试图恢复真实普通逝者的私聊、支付、密码或私密相册。

---

## 3. Late-1990s to 2004: a new channel existed before it was ordinary

2007 年新华社对当时行业的近时回顾称，中国较早的网上纪念馆在 1990 年代末已经出现，但早期发展受到网民规模、带宽、硬件等条件限制；该报道还提到 2004 年民政系统曾倡导互联网祭扫等新形式。[S1]

**Grade: B/C.**

这条材料只能建立边界：

```text
service existed by late 1990s
!=
ordinary households had broadband
!=
ordinary households knew the service
!=
online memorial was common
```

因此 old-Web 研究不能写成“1998 年中国已经普遍网络祭扫”。

同时，它也不能反过来写成“1994 年以前没有 Internet，所以死亡纪念完全没有远距离通信”：电话、邮政、亲友代祭、报刊讣告等早已可以跨距离协调；这些前史主要留给 sister life-history repository。

---

## 4. 2007: contemporaneous description of a purpose-built memorial interface

新华社 2007 年报道描述“无尽的爱纪念网”等在线纪念服务：用户可以进入 memorial environment，并执行献花、点烛、上香、敬茶、敬酒等界面动作；报道同时保存了支持者和反对者关于“便利”“环保”“庄重”“能否替代实地扫墓”的不同意见。[S1]

**Grade: B.**

它支持：

- 2007 年公开中文 Web 已有 purpose-built memorial service；
- 页面把一组现实仪式动作重新编码成 browser-visible controls；
- 网上祭奠被部分使用者理解成跨距离参与手段；
- 同期社会并没有形成“网上必然替代线下”的共识。

它不支持：

- 每个按钮对应真实物理行为；
- 所有点击都有真实亲友身份；
- 平台已经核验每一位被纪念者的死亡；
- 所有 memorial page 都由近亲属创建；
- 页面访问量等于独立祭扫人数。

由此新增：

### `visible ritual-control / social-action gap`

`献花 button visible` 只能证明 interface affordance；实际点击、实际付款、实际情感关系和线下祭扫必须分别取证。

---

## 5. 2008 ordinary-life case: a memorial page as a distance bridge

2008 年《南都周刊》同期采访中，27 岁广州人林良英在妹妹去世后建立付费网上纪念馆；一个明确目的，是让外地的同学和朋友也能方便纪念。报道说，妹妹去世后的第一个清明，已有亲友在页面点烛、留言、献歌。[S2]

**Grade: B: contemporaneous first-person / reported usage.**

这条证据非常重要，因为它不是平台宣传，而是把页面接回了真实迁移生活：

```text
逝者的亲友分散
→ 不一定都能回到同一物理墓地
→ 一个共享页面成为远程可达的纪念地址
```

但仍需保持：

`memorial page used by some relatives/friends`

!=

`physical grave visit stopped`

!=

`online memorial represented all grief activity`。

这个案例也说明 historical Web 中最容易保存的，恰恰可能是“可公开展示的悼念”；电话、家族私聊、墓前活动与沉默的悲伤则很难进入公共 archive。

---

## 6. An exact 2008 locator: `www.99jisi.com`

新华社 2008-04-01 关于大别山烈士陵园网上纪念的报道明确给出：

- site/host locator: `www.99jisi.com`
- platform/service name: 炎黄祭网；
- 页面/纪念馆可包含照片、简介、相关文献；
- browser-visible actions 包括献花、点歌、点烛、留言等。[S3]

**Grade: B for contemporaneous locator/workflow description.**

这是一条很有价值的 archaeological locator，但目前不能升级成：

- 已验证 2008 HTML；
- 已验证 charset；
- 已验证 JS/CSS；
- 已验证 historical form endpoint；
- 已验证 visitor/comment database snapshot。

因此：

### `contemporaneous locator / capture gap`

同一个 URL 在 2008 年新闻中被引用，证明它当时被当作访问入口；并不证明今天研究者已经拿到那一时刻的页面字节。

---

## 7. 2008 counterexamples: death, authorization and moderation were already problems

2008 年新华社报道同时记录了网上祭奠服务中的高额收费、恶作剧、恶意建立纪念对象、攻击性留言等争议。[S4]

**Grade: B.**

这些异常不是边角料，反而帮助我们建立几个关键 state gap。

### 7.1 `page-created / death-verified gap`

能够为某个名字建立 memorial page，不能自动证明此人真的死亡。

### 7.2 `creator / authorized-family gap`

页面创建者可能不是法定近亲属，也可能没有获得所有家属同意。

### 7.3 `comment-visible / legitimate-mourner gap`

留言者可以是亲友，也可能是陌生人、恶作剧者或攻击者。

### 7.4 `moderated-page / original-comment-stream gap`

一个今天仍整洁的纪念页，可能经历过删除、屏蔽、审核；现存评论不能自动代表当年所有输入。

这些 gap 对 archive 尤其关键：

> **保存下来的页面可能比历史现场更“干净”，也可能因为平台关闭而比历史现场更“空”。**

---

## 8. Proposed state machine for a purpose-built memorial (D reconstruction)

以下仅为研究者状态模型，不声称对应 `99jisi.com` 或其他站点实际数据库 schema。

```text
creator reaches service
        |
        v
creator account / identity state
        |
        v
memorial subject entered
        |
        +--> subject identity unverified?
        +--> death evidence required?
        +--> relationship evidence required?
        |
        v
page created / pending / published
        |
        v
biography / photo / dates / media uploaded
        |
        v
visitor reaches public page
        |
        +--> anonymous?
        +--> logged in?
        |
        v
virtual offering / message submitted
        |
        v
accepted by backend
        |
        v
moderation / filtering
        |
        v
public rendering
        |
        v
page remains hosted
        |
        +--> renewed / paid?
        +--> free?
        +--> migrated?
        +--> frozen?
        +--> deleted?
        +--> site/domain disappears?
```

Archive 通常只能观察其中少量 public render states。

---

## 9. Hard state boundaries for purpose-built memorials

### 9.1 `memorial subject != verified legal person`

页面名字、照片、生卒年月可能来自创建者输入。除非有明确身份/死亡核验机制，不能当 authoritative civil record。

### 9.2 `death event != platform death state`

现实死亡发生以后，平台是否知道、何时知道、凭什么知道，是另一笔事务。

### 9.3 `page owner != memorial subject`

账号操作者常常是家属、朋友、机构或站方，不是被纪念者。

### 9.4 `page creator != family consensus`

一位亲属创建页面，不等于所有近亲属都同意公开姓名、照片、疾病经过或留言。

### 9.5 `page exists != page used`

纪念馆可以建立后长期无人访问。

### 9.6 `visitor count != unique mourners`

可能涉及重复刷新、爬虫、匿名访问、计数规则变化。没有实现证据时，不能把 counter 直接解释成独立人数。

### 9.7 `virtual action accepted != offline ritual performed`

点烛/献花/上香等 browser action 是一种数字社会动作，不等于物理世界执行了同名动作。

### 9.8 `payment success != memorial permanence`

付费建立“永久馆”一类商业承诺，仍依赖公司、域名、服务器、数据库和持续维护。

---

## 10. Ordinary social accounts: a different and harder old-Web object

2003–2015 也是中文 Web 从博客、QQ 空间、个人主页走向长期 social profile 的时期。这里必须避免一个严重后见错误：

> 不能因为 2020s 平台已经有“逝者账号保护/纪念账号”规则，就假定 2005 年 QQ 空间、2008 年博客已经有相同状态机。

本轮尚未取得足够强的 2000s—early-2010s 中国平台原始死亡账号政策。

因此目前只能建立对象边界和待查问题，而不能写出虚构的 historical workflow。

### Proposed ordinary-account states (D)

```text
living user / account active
→ user dies in real world
→ platform may remain unaware
→ account inactivity grows
→ credential/device/phone/email state changes
→ page may remain public
→ friends/family may continue visiting/commenting
→ possible credential loss / theft / number recycling
→ possible deletion / reclamation / preservation
```

关键是：

`account liveness` 与 `person liveness` 已经脱钩。

---

## 11. Hard state boundaries for deceased ordinary accounts

### 11.1 `inactivity != death`

长期不登录可以由离网、换平台、丢密码、换手机号、入伍、住院、监禁、死亡等许多原因造成。不能从 inactivity 推断死亡。

### 11.2 `death known to family != death known to platform`

现实世界已经完成葬礼，平台仍可能把账号当普通 inactive account。

### 11.3 `page public != authorized family access`

家属能打开公开主页，不等于能登录后台、看私信或下载全部数据。

### 11.4 `credentials known != ethically transferable control`

家属知道密码，不等于可以无条件以逝者身份继续发消息或读取第三人私信。

### 11.5 `posthumous comments != account-owner activity`

逝者页面后来有新留言，不代表账号主人重新登录。

### 11.6 `account survives != account controllable`

页面长期存在，但用于找回密码的手机号、邮箱、安全问题可能已经失效。

### 11.7 `content survives != social context survives`

一张照片还在，不等于原相册顺序、评论、好友权限、转载关系和 contemporaneous audience 仍可恢复。

---

## 12. Archive-specific failure modes

### 12.1 `public memorial visibility / private grief invisibility gap`

公开纪念页最适合 crawler；电话、私聊、家族群、墓前活动、纸信和没有被说出的悲伤最难保存。

因此不能从 archive corpus 中网上悼念材料很多，推出当时多数悼念都在线完成。

### 12.2 `page survival / family authorization gap`

今天还能打开，不代表家属今天仍希望普通人的姓名、照片、疾病史被重新扩散。

### 12.3 `current host / historical service gap`

域名今天仍在线，也可能已经：

- 换公司；
- 换程序；
- 换数据库；
- 只保留品牌壳；
- 把旧 URL 接到新 backend。

当前页面绝不能自动作为 2008 服务状态证据。

### 12.4 `historical shell / current-backend rehydration gap`

即使 Wayback 保存 HTML shell，其中动态 memorial records、visitor counters、留言、JS API 或图片可能从当前服务器加载，形成时间混合。

### 12.5 `comment survival / historical discussion gap`

评论可能经历 moderation、删除、账号注销、编码损坏、分页丢失，存活 comment stream 不是原始完整讨论。

### 12.6 `crawler capture / ordinary-use gap`

一个页面被抓取很多次，只能证明 crawler activity/visibility；不等于普通用户访问密度。

### 12.7 `successful preservation / news-visibility inversion`

顺利保存、顺利导出、顺利由家庭内部处理的数字遗存，可能从不成为新闻；账号丢失、盗号、争议、继承受阻则更易留下媒体材料。

所以失败案例在历史资料里更醒目，不能据此估计总体失败率。

---

## 13. Privacy and ethics boundary

网上纪念页涉及：

- 已故普通人的姓名、照片、疾病、死因；
- 活着的配偶、父母、子女、同学；
- 留言者账号与关系；
- 家庭冲突；
- 可能仍活着的第三人私信、照片。

本仓的 preservation goal 应优先是：

- site/host/URL 谱系；
- 页面字段和 interface structure；
- browser / encoding / media dependencies；
- public policy / FAQ；
- anonymized state-machine evidence；
- 公开机构纪念页面；
- 得到伦理上合理处理的普通人案例。

不把“重新公开普通逝者私人材料”当作 archaeological success。

尤其不能因为 crawler 曾经抓到，就把页面中可识别的家庭健康/死亡细节再次集中传播。

---

## 14. M1 target: what a real historical memorial capture would require

要把这条线升级为真正 M1，至少需要一份 1998–2010 的历史 capture，记录：

1. `original_url`
2. `capture_url`
3. `capture_datetime`
4. HTTP status / redirect
5. charset / encoding evidence
6. DOM / frames / layout
7. CSS / JS / image subresources
8. memorial creation/login controls（如存在）
9. public page field structure
10. virtual offering / message controls
11. form endpoint / method（如果 capture 支持观察）
12. dynamic state missing list
13. browser hypothesis
14. privacy-risk review

如果只有首页，也只能证明首页；不能自动升级到 user memorial page、留言 backend 或 account state。

### Current status

```text
M1 verified historical Chinese online-memorial capture:
NOT ACHIEVED IN THIS SLICE
```

本轮只找到了 contemporaneous locators 和 workflow descriptions。

**这不等于 Wayback 没保存，也不等于页面当年不存在。**

---

## 15. Browser and encoding hypotheses: intentionally left open

2000s 中文 memorial site 很容易诱发“肯定 IE6 + GB2312 + table”式想象。

本轮不做这种无 capture 推断。

目前必须保持：

- `charset`: unknown until header/meta/binary evidence；
- IE-only dependency: unknown；
- ActiveX/Flash dependency: unknown；
- table/div layout: unknown；
- image hotlink/static host: unknown；
- guestbook submission protocol: unknown；
- virtual incense/flower animation implementation: unknown。

后续一旦取得 capture，再建立 browser fixture。

---

## 16. Evidence ledger

### E1 — late-1990s Chinese online memorial genealogy

Source: 新华社/新浪，2007-04-03。[S1]

Grade: **B/C**.

Supports:
- late 1990s already had early Chinese online memorial services according to near-contemporaneous industry review；
- early growth constrained by access/technical conditions；
- by 2007 virtual offering interfaces were publicly described.

Does not support:
- exact first site/date；
- adoption rate；
- historical HTML.

### E2 — ordinary family use, 2008

Source: 《南都周刊》/新浪，2008-04-09。[S2]

Grade: **B**.

Supports:
- one identified ordinary family created a paid memorial page；
- distance to classmates/friends was an explicit reason；
- relatives/friends used page actions around first Qingming.

Does not support:
- population prevalence；
- replacement of physical mourning.

### E3 — `www.99jisi.com` exact locator

Source: 新华社/搜狐，2008-04-01。[S3]

Grade: **B**.

Supports:
- exact contemporaneous host locator；
- described memorial page content and virtual actions.

Does not support:
- verified historical capture / DOM / charset / backend.

### E4 — abuse and moderation counterevidence

Source: 新华社/新浪，2008-04-05。[S4]

Grade: **B**.

Supports:
- contemporaneous concern about commercial pricing, malicious page creation and hostile behavior；
- need to model authorization/moderation states.

Does not support:
- rate/prevalence of abuse.

---

## 17. Forward boundary after 2015: evidence of a later state machine, not proof of an earlier one

Post-2015 developments belong mainly to `how-people-lived`, but they are useful as a warning against backward projection.

By 2020, contemporaneous reporting on Weibo's deceased-account protection says a claimant must provide identity, relationship and death documents before an account enters protected status; Bilibili also introduced memorial-account protection after family confirmation.[S5][S6]

These later policies prove that platforms eventually formalized:

```text
real-world death
→ documentary claim
→ platform review
→ special deceased-account state
```

They do **not** prove that 2005 or 2010 Chinese social sites already had the same workflow.

This is precisely why the 1998–2015 old-Web question remains archaeologically valuable.

---

## 18. What this changes in old-Web archaeology

Online memorials expose a strong preservation paradox:

> **A page can survive precisely because the person cannot update it anymore, while the meaning, authorization and surrounding relationship context continue changing for years.**

Most old-Web pages are treated as snapshots of past active users. Memorial pages and deceased-user pages require a different model:

- the subject may already be dead when page is created；
- creator and subject are different people；
- visitors can continue producing new content for years；
- page “staleness” can be intentional preservation, not abandonment；
- absence of login is not necessarily service failure；
- continued hosting may have intense family meaning even when platform metrics call the account inactive.

因此新增一个可复用概念：

### `intentional stasis / lifecycle-staleness gap / 有意静止—生命周期陈旧缺口`

对于普通 active profile，十年不更新通常意味着 stale。

对于 memorial page，十年不改变姓名、生卒信息和主体内容，可能恰恰意味着它仍在按照设计工作。

这会改变我们以后判断 old-Web “dead page”的方式：

> **页面死了，和页面在纪念一个死人，是两个完全不同的状态。**

---

## 19. Open questions

下一轮若深化这个对象，优先寻找：

- `99jisi.com` 2008 前后可验证 memento/WARC；
- “无尽的爱纪念网”的准确历史 host 与 page schema；
- 1998–2003 中国普通 online memorial 的 contemporaneous original artifact；
- 2003–2015 QQ/Qzone/blog 对用户死亡、账号继承、号码回收、内容删除的同期服务条款；
- memorial page 收费、续费、导出、关闭和 domain migration 规则；
- visitor counter / guestbook / virtual offering 的真实技术实现；
- 普通用户 memorial page 与公共人物/烈士 memorial 的结构差异；
- 站点关闭以后是否存在家属主动迁移/导出 memorial contents 的案例。

---

## Sources

[S1] 新华社，`中国网上祭奠先祖的人越来越多`，2007-04-03，新浪转载。
https://news.sina.com.cn/c/2007-04-03/101711557810s.shtml

[S2] 《南都周刊》，`虚拟祭祖：市场经济进驻虚拟墓地`，2008-04-09，新浪转载。
https://news.sina.com.cn/c/2008-04-09/164415322655.shtml

[S3] 新华社，`大别山烈士陵园整体“上网” 学生网上“扫墓”`，2008-04-01，搜狐转载；同期 locator `www.99jisi.com`。
https://news.sohu.com/20080401/n256025252.shtml

[S4] 新华社，`网上祭祀遭遇现实尴尬：出现高额收费与恶作剧`，2008-04-05，新浪转载。
https://news.sina.com.cn/c/2008-04-05/073615294595.shtml

[S5] 微博管理员 2020-09-17 逝者账号保护公告的同期报道转录（仅作 post-2015 forward boundary）。
https://www.thepaper.cn/newsDetail_forward_9213387

[S6] 哔哩哔哩 2020-12-24 逝者纪念账号机制的同期报道（仅作 post-2015 forward boundary）。
https://www.jiemian.com/article/5449048.html
