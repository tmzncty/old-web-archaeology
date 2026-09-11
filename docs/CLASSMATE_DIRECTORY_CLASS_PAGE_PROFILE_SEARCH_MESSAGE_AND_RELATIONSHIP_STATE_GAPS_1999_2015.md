# 中文校友录 / 同学录：学校索引、班级页、实名 Profile、搜索、消息与现实关系状态差（1999–2015）

## 0. Scope

本 note 研究 **1999–2015 中文互联网中的校友录、同学录、校园实名 SNS 及其与 IM / 私域联络的接口**。

重点不是写 ChinaRen、5460、校内网 / 人人网的品牌史，而是回答：

> 当旧网页显示“某人属于这个班级”“某人是我的同学”“可以找同学”“班级有 50 名成员”“好友关系仍存在”时，这些 Web 状态距离现实中的两个人仍然互相认识、仍能联系、仍愿意联系，还有多少没有被网页保存的中间状态？

本对象与 `how-people-lived` 的交叉专题：

- `topics/from-paper-alumni-directories-to-classmate-platforms-and-public-social-search-relationship-recoverability-china-1985-2026.zh-CN.md`

**本仓 scope 保持约 1995–2015 中文互联网。** 纸质校友录、美国 Classmates.com、2020s 微信 / 公开社交寻人只用于解释边界与后续结果，不把本仓扩成全球关系史。

---

## 1. Claim list first

本轮只建立以下窄 claim：

1. 1999–2000 已存在以学校 / 校友 / 年轻人社区为核心定位的 ChinaRen，并在 2000 年被搜狐收购；企业用户规模只按公司口径处理。
2. 2005 年同期媒体已观察到真实班级在 ChinaRen / 5460 建立线上班级，用于跨地实习、毕业后的留言、聊天、照片和活动协调。
3. 2005 年搜狐同期产品文章可验证 ChinaRen 校友录与搜Q 3.0 的整合路径：已有班级、找同学、找班级、加入班级、管理员审批、留言 / 图片 / IM 等状态并非一个动作。
4. 同期产品文章还显示，直接 ChinaRen 校友录的同学搜索与搜Q整合入口可能具有不同的手机绑定要求，因此 `feature exists` 不等于所有客户端 / 身份状态都获得相同 permission。
5. 2005 年已有利用校友录联系方式、账号和班级关系进行骚扰 / 诈骗的报道，因此“关系可寻址性”与隐私暴露从早期就并存。
6. 2011 年 Renren F-1 可验证实名 profile 包括学校 / 大学、就业、地点等字段，并且公司自己把已建立的朋友连接和内容描述为迁移成本；这是公司 A 级陈述，不等于独立验证的社会科学结论。
7. 2014 年 Renren 年报明确提到部分用户向 social messaging services 迁移，说明公开 SNS profile 仍存在时，现实活跃关系也可能已离开该平台。
8. 1999–2015 的中文校友 / SNS 对象必须永久区分 `school/class membership`、`platform account`、`friend edge`、`message`、`off-platform contact` 与 `real relationship`。
9. 当前没有取得一个按 METHOD 实际打开并检查、同时满足 exact original URL / capture datetime / replay state / charset / DOM / subresources / second time point 的合格 ChinaRen / 5460 早期班级页 M1 capture。

---

## 2. Research units

### 2.1 Real-world people / relations

- `person_a`；
- `person_b`；
- `historical_school_membership`；
- `historical_class_membership`；
- `past_friendship/acquaintance`；
- `current_relationship_state`；
- `current_contact_channel`；
- `willingness_to_reconnect`；
- `offline_meeting/reunion`。

### 2.2 Platform states

- `platform/site`；
- `school record`；
- `class record`；
- `class page`；
- `account`；
- `profile`；
- `name field`；
- `school/year/class field`；
- `phone-binding/authentication state`；
- `class join request`；
- `class membership approval`；
- `class administrator/moderator`；
- `member roster`；
- `friend edge`；
- `search query`；
- `search result`；
- `profile view`；
- `message/comment`；
- `photo album`；
- `class notice`；
- `IM contact`；
- `off-platform phone / QQ / later WeChat handoff`；
- `account recovery state`；
- `account deletion / platform shutdown state`。

### 2.3 Archive states

- original URL；
- currently surviving historical article / help page；
- Memento / archive capture；
- replayed main HTML；
- login wall；
- class/member backend state；
- dynamic search result；
- image / CSS / JS / iframe subresources；
- private message / IM logs；
- later repost / memory article；
- research claim。

这些对象不得混写。

---

## 3. Permanent state gaps

### 3.1 现实同学关系与平台成员关系

```text
same school
!= same cohort
!= same class
!= knew each other
!= were friends
!= are friends now
```

旧站的学校 / 班级字段首先是 **索引关系**，不是情感强度证明。

### 3.2 班级页与真实班级

```text
class page exists
!= official school record
!= every real classmate joined
!= every joined account is correctly identified
!= every member remained active
```

某学校下出现一个“2001级3班”页面，只能证明平台数据库里有这个 class record。

不能自动证明：

- 学校官方创建；
- 班名与教务系统完全一致；
- 班里全部真人都在；
- 列表里每个账号都是真人本人。

### 3.3 找到同名 profile 与找到正确的人

```text
name query
!= unique person
!= correct school match
!= correct profile
!= profile still controlled by that person
```

2005 搜Q / ChinaRen 操作说明自己就把重名当作普通问题，因此提供按学校和班级进一步查找。

### 3.4 加入班级

```text
class found
!= join request submitted
!= moderator saw request
!= moderator recognized applicant
!= membership approved
!= applicant gained identical access to all class data
```

“找到班级”与“成为班级成员”必须拆开。

### 3.5 功能存在与权限存在

```text
“找同学” feature exists
!= user authenticated enough to use it
!= same permission in Web and IM client
```

2005 年搜狐同期文章称，ChinaRen 校友录直接查找同学需要手机绑定，而搜Q整合入口当时不要求相同条件。

这不是小产品细节，而是旧网考古必须记录的 **client / authentication path dependency**。

### 3.6 friend edge 与现实联系

```text
friend edge exists
!= either user still logs in
!= either user remembers the other
!= message can reach recipient
!= current phone/QQ known
!= ongoing friendship
```

社会图谱是一种平台状态，不是现实关系传感器。

### 3.7 消息与恢复关系

```text
message sent
!= delivered
!= visible
!= read
!= recognized
!= replied
!= off-platform contact exchanged
!= relationship reactivated
```

尤其当账号多年未登录时，historical message 只能证明平台记录过一次发送 / 留言状态。

### 3.8 内容备份与图谱迁移

```text
photos exported
!= comments exported
!= friend list exported
!= class membership migrated
!= active contact channel migrated
```

平台关停时的“请下载照片、留言板”不应改写成“用户可以完整迁走自己的社会关系”。

---

## 4. 前史边界：纸质通讯录只用于解释 Web 做了什么，不进入本仓主对象

南开大学档案馆后来记录的《旅美南开校友录（1990）》和《旅美南开校友通讯录（1996）》说明：Web 以前，校友组织已经用纸质名录维护分散人口的地址 / 联系方式。

来源：

- <https://archives.nankai.edu.cn/info/1060/1677.htm>

本仓只保留一个技术边界：

> **Web 校友录不是从“完全没有校友索引”开始，而是把一次性印刷 snapshot 变成可搜索、可由用户更新、可持续增加留言和成员状态的在线数据库。**

纸质内容的具体历史进入 `how-people-lived`，本文件不继续前移 scope。

---

## 5. Case slice A — ChinaRen 的平台谱系边界（1999–2000）

搜狐 2000 年收购完成公告称，ChinaRen 是面向年轻人的 community web site；交易完成后 ChinaRen 与搜狐继续作为相关但可区分的网站 / 产品存在。

来源：

- SOHU company release, 2000-10-31：<https://investors.sohu.com/static-files/e5aead3b-87a8-4865-ace5-f570b312b8e7>

### Evidence grade

- **A：同期公司资料**；
- 公司关于“leading / largest”等市场地位和用户数属于自报；
- 能证明公司当时如何定义产品和交易，不能单独证明普通用户体验。

### Important unit boundary

```text
ChinaRen brand
!= www.chinaren.com homepage
!= alumni-directory subsystem
!= one class page
!= one user account
```

后续若取得历史 capture，必须继续追具体 host / URL，而不能只登记品牌首页。

---

## 6. Case slice B — 2005 年“网上班级”是现实班级的延伸，但不是替代品

2005-03-18《解放日报》报道当前由新浪 survivor 保留。它记录：

- 复旦新闻学院一个硕士班因学生分散全国实习，于 2004 年末在 ChinaRen 建同学录；
- 班级管理员承担通知和线上组织角色；
- 同济一个博士班上传结婚照、活动通知、专业讨论和春游倡议；
- 武汉大学 1996 级广电班毕业后跨地域继续使用网上同学录；
- 同期也有人批评在校同学过分依赖线上联系，线下活动反而难落实。

来源：

- <https://news.sina.com.cn/s/2005-03-18/09105394097s.shtml>

### Evidence grade

- **B / T1，同期媒体现场与采访**；
- 当前 URL 是新浪保存至今的历史文章 survivor，不是已经核验的 2005 Memento；
- 页面今天能打开，只支持文章语义仍可读取，不支持“今天的 CSS / iframe / 广告布局 = 2005 render”。

### What it supports

窄 claim：

> 至少在这些具体班级中，真实班级成员把线下已有的关系和组织角色延伸到了公开互联网平台，并用于跨地协调和毕业后的持续联系。

### What it does NOT support

- 不证明 2005 全国大学生普遍拥有网上同学录；
- 不证明文中平台展示的班级数量等于真实独立活跃班级数量；
- 不证明一个班级页面的存在意味着成员日常活跃；
- 不证明线上联系提高了线下亲密程度。

---

## 7. Case slice C — 2005 ChinaRen / 搜Q：搜索、班级加入与 IM 不是一个状态

搜狐 2005-03-01 的两篇同期产品文章保存了比回忆文章更细的操作路径。

来源：

- <https://news.sohu.com/20050301/n224481435.shtml>
- <https://news.sohu.com/20050301/n224481302.shtml>

### 7.1 已有班级同步到 IM 客户端

文章描述用 ChinaRen 账号登录搜Q 3.0 后，可进入“校友录”标签看到已有班级。

应记录为：

```text
same credential accepted
→ client displays linked class records
```

不能进一步推断后台具体 SSO / API / cookie 实现，除非未来取得技术文档或抓包。

### 7.2 “找同学”与“找班级”是两种查询

当姓名重名时，产品文章建议先查学校、再查班级。

说明当时至少存在两个不同的 lookup namespace：

- person/name oriented；
- school/class oriented。

这对后续复原 search form schema 很重要。

### 7.3 班级加入需要审批

找到班级后还要发出加入请求，并等待管理员识别和批准。

所以 historical screenshot 即使出现“加入”按钮，也只能说明 **可发起 membership transition**，不能推出用户最终进入班级。

### 7.4 authentication path 不一致

另一篇同期产品文章称：

- ChinaRen 校友录的查找同学当时要求手机绑定；
- 搜Q 3.0 整合入口则“不需要”。

因此如果未来抓到两个看似相同的“找同学”界面，必须记录：

- client；
- account state；
- phone-binding state；
- date；
- actual query result。

不能用一个入口推断另一个入口。

### Evidence grade

- **A/B 边界**：搜狐同期产品页 / 产品宣传语，适合证明“搜狐当时公开描述此功能”；
- 未独立实测 historical client，因此实际服务器行为仍需历史 capture / 软件包 / 手册复核。

---

## 8. Case slice D — 2005 隐私事件：关系索引本身也可以成为攻击面

2005-05-09《金陵晚报》报道若干利用网络校友录资料、电话号码、账号 / 密码和班级成员关系实施骚扰、诈骗的案例。

来源：

- <https://news.sina.com.cn/o/2005-05-09/10135836958s.shtml>

### Evidence grade

- **B / T1，同期新闻**；
- 个案不能换算平台风险率；
- 也不能从报道自动证明漏洞属于平台端、用户密码复用或社会工程中的哪一层。

### Archaeological implication

早期校友录页面如果保存了：

- 真人姓名；
- 电话；
- 邮箱；
- 具体班级；
- 家庭 / 单位地址；

即使这些当年公开，也不应因为 archive 可访问就批量重新发布。

本仓应优先恢复：

- 字段 schema；
- 权限结构；
- 页面状态；
- search / join workflow；

而不是建立“2005 普通学生电话数据库”。

---

## 9. Case slice E — 2011 Renren：学校字段从“班级目录”进入持续实名 profile

Renren 2011 F-1 描述：用户建立免费个人 profile，可包含姓名、照片、学校 / 大学、就业、当前地点、年龄、兴趣等，并用于同朋友、同学、家人和同事保持联系。

来源：

- Renren Inc. F-1/A：<https://www.sec.gov/Archives/edgar/data/1509223/000119312511099693/df1a.htm>

### Evidence grade

- **A：SEC 同期公司文件**；
- 可证明公司当时产品 schema 与自述业务逻辑；
- 用户规模、覆盖率、关系“真实性”等属于公司 assertion，需独立来源复核。

### State change

早期同学录更接近：

```text
school/class page → member roster → message board
```

实名 SNS 更接近：

```text
person profile
├── school history
├── employment
├── current location
├── friend edges
├── photos/content
└── newsfeed interaction
```

学校关系从独立“校友录应用”变成了用户长期身份图谱的一部分。

### Company-described switching cost

F-1 明确称，用户已经建立朋友连接、上传照片等以后，迁移到另一个 SNS 需要重新投入时间，并且朋友也要一起迁移。

本仓只登记为：

> **公司在 2011 年已经把 social graph / content accumulation 视为 retention mechanism。**

不要改写成“用户实际上无法离开”或“人人网关系一定比别的平台更真实”。

---

## 10. Case slice F — 2014：profile 仍在，不代表 active relationship 仍在这里

Renren 2014 年 20-F 称，自 2013 年末起，部分白领用户因竞争而向 social messaging services 迁移，公司重新聚焦更年轻的用户群。

来源：

- <https://www.sec.gov/Archives/edgar/data/1509223/000114420415023129/v403466_20f.htm>

这给 old-Web 提供一个永久边界：

```text
historical profile survives on SNS
!= person still uses SNS as primary communication channel
```

一个 2014 profile 页面即使完整可回放，也不能说明：

- 该用户仍每天登录；
- 好友边仍对应活跃联络；
- 班级活动仍在该站发生；
- 实际关系没有迁移到 QQ / 微信等 private messaging。

### `graph-presence / communication-presence gap`

这是从旧 Web 进入移动私域时最重要的不可见状态之一。

---

## 11. 2015 作为本仓 scope 的边界：为什么不能用后来的停服直接改写早期体验

2017 年朋友网（原 QQ 校友）停服时，官方公告建议用户备份照片和留言板。

来源：

- 澎湃新闻，2017：<https://www.thepaper.cn/newsDetail_forward_1733683>

本 note 使用它只解释 1999–2015 研究对象的长期 preservation outcome：

- 平台可以消失；
- 用户内容可能提供有限导出；
- friend graph / class membership / active contact 不必随导出迁移。

但 **不能因为知道 2017 会关闭，就把 2009 用户写成“当时其实已经活在一个注定消失的平台上”。**

这是典型 hindsight risk。

---

## 12. Archive asymmetries

### 12.1 `school-index survival / relationship-state loss asymmetry`

最容易长期保存：

- 学校名；
- 年级 / 班级名；
- 平台帮助页；
- 搜索入口；
- 某个 public profile shell。

最难保存：

- 两个人当时到底熟不熟；
- 后来有没有互留电话 / QQ；
- 是否真实见面；
- 是否多年不再联系。

所以 archive 更容易恢复**关系索引**，而不是**关系状态**。

### 12.2 `member-roster / active-presence gap`

```text
account listed in class roster
!= account active on capture date
!= user read class messages
```

成员列表不能直接当 MAU。

### 12.3 `public-class-page / private-handoff inversion`

真正成功的 re-contact 往往会迅速离开可抓取页面：

```text
class page / profile search
→ site message
→ QQ / phone / email
→ offline meeting
```

因此 crawler 保存越完整，反而越可能只保存“关系恢复的前半段”。

### 12.4 `profile-content survival / credential-access gap`

旧 profile 仍可见，不等于原用户还能登录。

密码、旧邮箱、旧手机号、手机绑定状态通常不会公开保存。

所以：

```text
account exists
!= account recoverable by original user
```

### 12.5 `social-graph persistence / present-consent gap`

历史 friend edge、照片和留言曾经公开，不等于用户今天仍同意继续被过去的同学定位和查看。

2019 年人人重启时“旧内容 / 黑历史”争议属于 scope 外后续结果，但它提醒本仓：

> archive preservation 不应被等同于用户对当代再曝光的授权。

### 12.6 `platform-migration / archive fragmentation`

同一现实班级可能按年代依次把活跃通信迁到：

- ChinaRen / 5460；
- QQ；
- 人人；
- QQ 群；
- 微信群。

没有任何单一 archive 自动拥有完整 longitudinal social graph。

未来研究需要把不同 platform record **并置**，而不是假设它们是同一个图谱的连续数据库。

---

## 13. 页面 / 浏览器环境：本轮确认与禁止推断

### 已确认

- 当前仍可访问的 2005 搜狐 / 新浪历史文章保留文本语义；
- 2011 SEC filing 保存了产品 schema 与公司陈述；
- 文章明确提到 2005 搜Q 3.0 与 ChinaRen 的产品整合。

### 本轮没有确认

- ChinaRen 班级页 exact original URL pattern；
- ChinaRen 2005 charset；
- 是否必须 IE；
- 是否使用 frameset；
- 搜索表单 GET / POST；
- 班级成员动态加载机制；
- 搜Q 3.0 客户端与服务器协议；
- 5460 班级页的 DOM / CSS / JS；
- 任何 historical cookie / session / phone-binding enforcement 的实际响应。

因此严禁为了“符合年代感”写：

> “典型 IE6 + GB2312 + table / frameset 页面。”

除非未来拿到实际 artifact。

---

## 14. Archive search result and negative evidence

本轮检查：

- ChinaRen / 校友录 / 找同学 / 搜Q 3.0 的同期搜狐 survivor；
- 2005 新浪同期媒体 survivor；
- Renren 2011 SEC F-1；
- Renren 2014 SEC 20-F；
- 搜索引擎中的 `web.archive.org + chinaren.com / 5460` locator 线索；
- 尝试通过当前 Web 工具直接访问 Wayback CDX 查询，但该访问路径未得到可核验结果。

### Result

**`M1 verified historical ChinaRen / 5460 class-page capture: NOT ACHIEVED IN THIS SLICE`**

这只表示：本轮没有实际打开并核验到满足 METHOD 最低字段要求的 capture。

**不表示：**

- Wayback 没有任何 capture；
- ArchiveTeam / Common Crawl 没有资源；
- 原页面当年不存在。

### 下一次 M1 应至少记录

```yaml
archive_source:
capture_url:
original_url:
capture_datetime:
accessed_at:
http_or_replay_state:
redirect_or_error_state:
content_type:
charset:
main_html_preserved:
subresources:
login_required:
client_assumption:
class_or_profile_schema:
second_capture_datetime:
evidence_grade:
confidence:
```

---

## 15. Privacy / ethics

校友录是旧网隐私风险特别高的对象，因为它天然把：

- 真人姓名；
- 学校；
- 年级；
- 班级；
- 同学关系；
- 可能还有电话、邮箱、地址和照片；

聚合在一起。

本仓采取以下最小化原则：

1. 不批量恢复普通用户电话 / 邮箱；
2. 不发布仍可能用于账号恢复的个人字段；
3. 普通班级页面优先记录 URL pattern / schema，不建立真人关系数据库；
4. 新闻已公开的具体个人案例只保留支持 claim 所必需的事实；
5. 不把 archive 里已经删除 / 私密化的内容重新做成搜索引擎可索引的数据集；
6. “历史价值”不能自动覆盖本人今天的关系退出权。

---

## 16. Claim / evidence matrix

| Claim | Evidence | Grade | Supports | Does not support |
|---|---|---:|---|---|
| ChinaRen 在 2000 被搜狐收购并作为青年 community 定位 | SOHU 2000 release | A | 品牌 / 公司谱系 | 用户真实活跃度 |
| 2005 真实班级使用网上同学录维持跨地联系 | 解放日报同期报道 | B/T1 | 具体班级实践 | 全国普及率 |
| 搜Q 3.0 可显示已有班级、找同学 / 班级、IM | 搜狐 2005 产品文章 | A/B | 产品公开描述 | historical protocol 实测 |
| 搜索权限受 client / phone-binding path 影响 | 搜狐 2005 产品文章 | A/B | 同期权限差异描述 | 后续版本相同 |
| 校友录资料可形成骚扰 / 诈骗攻击面 | 金陵晚报 2005 | B/T1 | 风险真实发生过 | 风险率 / 平台漏洞因果 |
| Renren profile 包含学校、工作、位置等并保存 friend graph | 2011 F-1 | A | 公司产品 schema | 每字段都真实准确 |
| 公司把 friend graph + content 视为 switching cost | 2011 F-1 | A | 公司自述 retention logic | 独立用户行为因果 |
| 一部分用户迁向 social messaging | 2014 20-F | A | 公司承认迁移压力 | 每一个旧 profile 都不活跃 |

---

## 17. 下一步研究问题

### M1 capture

优先找一个具体、可重复的 2004–2006 ChinaRen 或 5460 班级页面：

- 至少两个历史时点；
- 记录主 HTML、图片、CSS、JS；
- 检查登录前 / 后差异；
- 检查班级 roster、留言、加入按钮是否来自同一个 endpoint；
- 如果只剩 shell，也明确 state loss。

### Client artifact

搜Q 3.0 如果存在合法可研究的软件包 / 手册，可建立：

- version hash；
- 安装日期线索；
- login flow；
- “校友录”入口；
- browser / embedded web control assumption；
- historical server endpoint 是否仍可解析。

不要连接真实用户账号或尝试绕过认证。

### Longitudinal graph

选择一个公开机构班级而不是私人普通班级，比较：

```text
2005 class page
→ 2010 SNS profile/group
→ 后续 institution/alumni public page
```

目标不是跟踪个人，而是研究 **同一组织关系如何跨平台换容器**。

---

## 18. 本轮对旧网考古方法的新增

这一轮最重要的不是又多了一个“消失的网站名单”，而是明确了：

> **关系是一类特别难被 Web archive 保存的历史对象。**

网页很擅长留下：

- “这里有一个班”；
- “这个账号曾属于这个学校”；
- “这里有一个好友按钮”；
- “这里有一条留言”。

网页却很难告诉后来的研究者：

- 两个人究竟熟不熟；
- 留言以后有没有换 QQ；
- 五年后是否还联系；
- 账号还在的时候本人是不是早就不用了；
- 平台关掉以后这段关系是否已经迁到别处；
- 本人今天还愿不愿意被这段旧关系重新找到。

因此中文旧网研究不能把 **social graph artifact** 直接当作 **social relationship**。

最需要保存的是状态差：

```text
past classmate
!= current contact
!= platform friend
!= active relationship
```

而最成熟的复原，也许只能可靠恢复到：

> **当时的人有哪些基础设施，可以尝试重新找到彼此。**

至于后来他们有没有真的重新成为朋友，很多时候恰恰应该留在 archive 看不见的私人生活里。
