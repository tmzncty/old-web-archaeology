# 中文旧网同学录：班级目录、找同学、身份确认、IM 联动与平台记忆状态缺口（1998—2015）

## Scope

本笔记只研究约 **1998—2015 中文旧网中的网上同学录 / 校友录 / 早期校园关系网络**，重点对象包括：

- 5460 中国同学录；
- ChinaRen 校友录；
- 校内 / 人人式校园实名关系网络；
- 与 QQ / 搜Q 等 IM 的联动；
- 班级、学校、成员、留言、相册等页面与事务状态；
- 改版、平台迁移和服务衰退以后，关系记录与用户内容如何变得难以访问。

不把本仓扩成全球 SNS 史。法国 Minitel、美国 Classmates.com / Facebook 等前史和跨国比较放在 `tmzncty/how-people-lived`：

- `topics/from-paper-address-books-to-searchable-classmates-social-tie-reconnectability-and-platform-memory-china-1990-2026.zh-CN.md`

2018、2019、2024 的人人网材料只作为 **afterlife / preservation consequence**，帮助解释 1998—2015 的旧网对象后来发生了什么，不改变本仓主 scope。

---

## 一、研究单位：不要把“同学录”写成一个页面

一次网上“找老同学”至少涉及：

```text
platform / brand
→ host
→ account
→ school record
→ class record
→ class membership
→ profile
→ search index
→ contact channel
→ message / IM delivery
→ photo / guestbook / forum content
→ later migration or deletion
```

因此以下对象必须分开：

- **platform brand**：例如 ChinaRen；
- **service**：ChinaRen 校友录；
- **host**：如 `alumni.chinaren.com`；
- **school record**：一个平台里的“某学校”；
- **class record**：某学校下的“某年级某班”；
- **account**：登录账户；
- **member/profile**：班级中的一个用户资料；
- **relationship edge**：班级成员、好友、管理员等关系；
- **content**：留言、照片、日志、讨论；
- **search result**：用户通过姓名/学校搜索得到的候选；
- **capture**：档案服务在某时刻保存的一份页面表示。

同一个品牌不等于同一个 host；同一个 host 的 2001、2007、2013 页面也不能默认同一技术栈。

---

## 二、已确认的历史 locator 与窄 claim

### 1. 2001：ChinaRen 与 5460 已经作为网上校友录被同期媒体识别

2001-01-10《中华读书报》同期观察把网上校友录单列为“精神家园”，明确写到：

- ChinaRen：`www.chinaren.com`；
- 中国同学录：`www.5460.com`。

报道还观察到 5460 中同一学校可能被重复创建许多次，导致首次访问用户难以找到正确班级。[S1]

**证据等级：B。**

可支持：

- 2001 年这两个 locator / 品牌在同期中文 Web 语境中与“校友录/同学录”关联；
- 重复 school/class record 是实际可观察的目录问题。

不能支持：

- 全国大学生普及率；
- 精确注册量；
- 原始 HTML / charset / browser requirement；
- `www.chinaren.com` 首页与校友录具体 path 在全部 2001 年份保持不变。

---

### 2. 2004：ChinaRen 校友录有明确的独立 host 与可描述操作路径

PChome 2004-06-23 的同期用户教程给出：

```text
http://alumni.chinaren.com
```

并描述：

- 点击“注册”；
- Sohu / ChinaRen 邮箱用户可复用用户名密码；
- 进入后可以按“我的大学 / 我的中学 / 我的小学”搜索或创建班级。[S2]

**证据等级：B。**

这使我们可以把早期 ChinaRen 校友录至少拆成：

```text
account identity
→ school-level directory
→ class search/create
→ class membership
```

但仍不知道 2004 原始页面的：

- HTTP headers；
- charset；
- frames / table / DOM；
- JS；
- cookie/session 行为；
- 是否存在 browser sniffing；
- 搜索请求是否 GET/POST；
- classuuid 如何生成；
- 未登录搜索与登录后搜索的精确差异。

---

### 3. 2004：一个真实 class URL pattern 被论坛用户留下

2004-09-05 CFC 中文论坛的一名用户发布 ChinaRen 校友录班级链接：

```text
http://alumni.chinaren.com/class/class_index.jsp?classuuid=...
```

另一名用户回复自己两年前就开过班级但“没人去”。[S3]

**证据等级：B（同期论坛操作痕迹）。**

为隐私最小化，本仓不复制该普通用户班级的完整 `classuuid`，只保存 URL pattern。

这个材料非常重要，因为它同时证明两件相反的事：

1. class page 的确可以被创建并公开链接；
2. **created ≠ populated ≠ active**。

所以必须增加：

### `class-created / class-used gap`

一个班级 URL 存在，不代表同学已经迁入，也不代表它承担真实关系维护。

---

### 4. 2005：校友录搜索与 IM 联动，并存在手机绑定状态差异

搜狐 2005-03-01 对搜Q 3.0 / ChinaRen 校友录整合的同期产品材料记录：

- 客户端有独立“校友录”界面；
- 两个主要按钮是“找同学”“找班级”；
- ChinaRen Web 校友录的“查找同学”当时要求手机绑定用户；
- 搜Q一侧放开了这一限制。[S4]

**证据等级：B；涉及搜狐自家产品能力时按 A/B 厂商材料看待。**

这直接要求把：

```text
profile exists
search result visible
contact permission granted
IM identity linked
message actually delivered
```

分开。

---

### 5. 2006–2007：ChinaRen 从典型旧式页面结构向 Web 2.0 技术迁移

2007-03-02 的 ChinaRen 改版材料回顾 2006 年二级产品升级时明确写到：

- 首页“摒弃 table 的页面结构”；
- 全站应用 DIV+CSS；
- 大量 AJAX；
- 2007 改版增加大容量相册、批量上传、幻灯浏览、班级动态、资料变化提醒、音乐/视频插入、隐私设置、博客互通等。[S5]

**证据等级：A/B 平台产品宣称。**

它不能证明所有用户浏览器都顺利运行这些功能，但对考古有一个关键含义：

### `static-page survivability / dynamic-state survivability gap`

早期较静态的班级页面和后期 AJAX 驱动的动态模块，其 archive 可恢复性不能默认相同。

即使主 HTML 被 capture，以下内容仍可能来自未保存的 API / JS / session：

- 班级动态；
- 相册翻页；
- 成员资料变化；
- 搜索结果；
- 私有资料；
- IM 在线状态；
- 批量上传；
- 登录后的关系图。

---

## 三、不要把“加入班级”直接当成现实身份确认

### 1. `school-record / historical-school gap`

2001 同期观察已指出 5460 中同一学校可能重复创建。[S1]

因此：

```text
platform school record exists
≠
this is the canonical historical school entity
```

学校可能：

- 重名；
- 改名；
- 合并；
- 被用户重复创建；
- 按院系/校区另建；
- 使用简称、旧称、错别字。

未来做 dataset 时，必须保留 platform-native label，而不是先强行归一化后删除历史歧义。

---

### 2. `class-page member / actual classmate gap`

2004 一则武汉同期诈骗报道记录，有人冒充“高中校友”取得信任；某同学录管理员还专门提醒班级成员谨慎验证新加入者身份。[S6]

这说明：

```text
account joined class
≠
account operator actually belonged to that class
```

平台的班级 membership 是**平台状态**，不是自动成立的现实人物史实。

如果将来 archive 到成员列表，只能写：

> 该 capture 显示账号 X 当时被平台列为该班级成员。

不能直接写：

> X 历史上确实就读该班。

除非有其他独立证据。

---

### 3. `name-match / person-match gap`

2008 校内网同期采访记录，一名大学生拿高中毕业照上的姓名逐个搜索老同学，60 多人中找到近 30 人。[S7]

这种操作本身说明搜索结果需要用户继续做**人工身份拼接**：

```text
name
+ school
+ cohort
+ photo/profile
+ mutual friends
→ probable person match
```

因此 future schema 应允许：

- `candidate_identity_match`；
- `confirmed_identity_match`；
- `match_basis`；
- `confidence`。

不要让一个搜索结果直接升级为“历史人物已确认”。

---

## 四、同学录真正是一条多系统事务链

建议至少把一次“找到并重新联系同学”写成：

```text
1. account created
2. account authenticated
3. school searched
4. school record selected
5. class searched / created
6. join request submitted
7. membership approved / auto-added
8. profile indexed
9. another user searches
10. candidate result displayed
11. identity inferred / confirmed
12. contact permission available
13. IM / message submitted
14. platform accepts message
15. recipient account remains active
16. recipient actually retrieves message
17. recipient responds
18. relationship moves to another channel or offline life
```

### 核心 state gaps

#### `account-created / currently-recoverable`

账号创建过，不等于多年后仍能找回密码。

#### `mobile-bound / phone-still-controlled`

2005 手机绑定可以解锁搜索权限；但绑定号码多年后可能已经换号。[S4]

#### `school-found / correct-school`

同名、重复 school record 使两者分离。[S1]

#### `class-created / populated`

同期论坛已经存在“班级开了两年但没人去”的反例。[S3]

#### `member-listed / actual-classmate`

冒名加入案例证明不能直接等同。[S6]

#### `profile-found / person-confirmed`

同名搜索仍需要照片、年级和共同好友人工确认。[S7]

#### `discoverable / contactable`

查找功能可能受手机绑定、登录、权限限制。[S4]

#### `message-submitted / platform-accepted / recipient-read`

三者都必须分开。当前没有足够原始事务日志确认历史实现细节。

#### `friend-edge / lived-relationship`

好友/同班边只证明平台关系，不证明亲密度和线下互动。

#### `photo-listed / image-object-survives`

相册页面 capture 不保证原图对象仍在 archive。

#### `platform-active / social-centrality`

一个平台还在线，不等于用户仍把它当主要社交入口。

#### `data-retained / user-accessible`

服务器可能仍保存数据，但登录/找回密码失败时用户仍然无法取回。

---

## 五、2001–2008 的页面形态：目录型 Web 怎样逐渐长成关系流

基于同期材料，可以做一个**仅到 claim 层、尚未完成 capture 验证**的形态演变假说：

### Phase A：school/class directory

2001–2004 证据最强的是：

- 找学校；
- 找班级；
- 创建班级；
- 进入班级页面；
- 留言/交流。[S1][S2][S3]

核心导航像一棵目录树：

```text
school
└── class
    ├── members
    ├── guestbook / discussion
    └── photos / notices
```

### Phase B：directory + IM

到 2005，搜 Q 联动把校友录的 class/person directory 与在线 IM 接起来。[S4]

于是：

```text
find old person
→ immediately attempt synchronous contact
```

### Phase C：directory + persistent profiles + feed-like updates

2006–2007 的 ChinaRen 改版材料增加：

- 班级动态；
- 个人资料变化；
- 大容量相册；
- 博客圈；
- 多媒体内容；
- Ajax interaction。[S5]

它意味着平台从“我需要找人时才查目录”向“我打开以后会持续看到同学变化”靠近。

### Phase D：campus real-name SNS

2008 校内网材料已经把：

- 实名 profile；
- 日志；
- 好友的好友；
- 新鲜事；
- 圈子；
- 旧同学搜索；

放在同一社会空间里。[S7]

所以旧网平台谱系不能只写：

```text
校友录 → SNS
```

更准确的是：

```text
school/class directory
+ persistent account
+ identity verification
+ content publishing
+ friend graph
+ activity update
→ campus-centered SNS
```

这是 M2 platform genealogy 很值得保留的一条桥梁。

---

## 六、用户行为证据：网上班级不是只有“找人”

2005《解放日报》同期报道显示，网上班级可以承载：

- 班会通知；
- 毕业后持续留言；
- 婚礼/生活照片；
- 专业技术讨论；
- 春游倡议；
- 异地同学持续联系。[S8]

因此 `class page` 的研究单位不应只视为“人名目录”。

它同时可能是：

- message board；
- photo album；
- lightweight forum；
- event coordination page；
- memory archive。

但同一报道也保存了用户反对意见：在校学生若过度依赖网上班级，可能弱化现实集体生活。[S8]

所以不能写成“网上同学录提高了所有同学关系质量”。

---

## 七、关系可见性也是隐私与攻击面

本对象有比普通门户页面更高的隐私风险。

2004 冒充校友诈骗材料已经证明，学校、班级和共同记忆本身可以成为社会工程素材。[S6]

因此旧网考古不应该因为历史网页公开过，就重新批量公开：

- 普通人的真实姓名 + 电话；
- 家庭住址；
- 工作地址；
- 邮箱；
- 生日；
- 个人照片；
- 家庭关系；
- 私人留言。

### 推荐保存

- host / URL pattern；
- 空白帮助页；
- 注册和找班级流程；
- classuuid 等字段结构，但对真实 ID 做最小化；
- 页面截图中的布局测量（必要时去标识化）；
- 同时代教程和媒体截图；
- schema / state model；
- 资源缺失清单。

### 不推荐

- 把一个普通班级的全量名单搬进仓库；
- 批量抓取旧联系信息；
- 将 archive 中已经删除/遗忘的私人照片重新公开。

---

## 八、平台 afterlife：为什么“页面还在不在”不是唯一保存问题

这一节超出 2015 的部分只用于解释旧网遗产，不扩仓库 scope。

### 1. 2018：用户关心的开始从“继续用”变成“别删数据”

2018 年人人网资产出售时，采访中的一些旧用户已经多年很少登录，但明确希望照片和日志保留；有人主动先导出再删除，因为不知道数据未来会怎样被使用。[S9]

这说明：

### `active-use / preservation-value gap`

低活跃不等于低保存价值。

### 2. 2019：账号恢复本身成为产品能力

2019 年新人人 App 上线时，媒体把“原账号密码还能登录”“账号密码找回体系”作为主要卖点之一。[S10]

因此旧 Web 的长期考古需要追问：

```text
content survives
+ account mapping survives
+ recovery channel survives
```

缺任何一个，普通用户都可能无法取回自己的旧内容。

### 3. 2024：用户要求的甚至只是“让我把照片拿回来”

2024 年人人网暂停服务时，有用户在贴吧等渠道询问如何登录以保存照片；青年报采访的老用户则担忧整套“青春纪念册”失去访问能力。[S11][S12]

这里必须严格区分：

```text
service paused
≠ data destroyed
≠ data recoverable by user
≠ archive independently preserved
```

平台当时公开表示数据会被保护并准备升级，但这只是平台 claim，不可改写成“数据已经永久安全”。[S11][S12]

---

## 九、历史可见性偏差：旧网会留下“关系图”，但未必留下关系

网上同学录特别容易产生一种历史错觉。

### 容易留下

- 学校名称；
- 班级名称；
- 成员数量；
- 公开昵称/姓名；
- 公开留言；
- 相册索引；
- 平台公告；
- 帮助页；
- 产品改版新闻。

### 容易丢失

- 登录后动态页面；
- 私信；
- QQ / 搜Q 会话；
- 手机绑定状态；
- 成员审核记录；
- 搜索 ranking；
- 原图对象；
- AJAX endpoint 返回；
- 删除内容；
- 用户导出的本地副本；
- “搜到以后没有回应”的失败事务；
- 关系真正在线下恢复了多久。

因此：

### `archived-relationship-graph / lived-relationship gap`

即使未来能复原某班级 2005 年成员页面，也只能复原一种**平台可观察关系图**，不能直接复原同学之间真实亲密度。

---

## 十、浏览器与技术环境：本轮已知与未知

### 已知

- 2004 ChinaRen 校友录有 `alumni.chinaren.com`；[S2]
- 同期 class URL 至少出现 `class/class_index.jsp?classuuid=...` pattern；[S3]
- 2005 存在与搜Q 3.0 的 IM 联动；[S4]
- 2006 改版宣称从 table 首页转向 DIV+CSS，并大量使用 AJAX；[S5]
- 2007 新版包含大相册、动态、多媒体、博客互通和隐私设置。[S5]

### 仍不知道

- 1998–2001 5460 初始 charset；
- 2001 ChinaRen 校友录具体 path；
- 2004 ChinaRen 原始 Content-Type / charset；
- 是否存在 IE-only JS / `document.all` / browser sniffing；
- 登录 cookie 名称、session timeout；
- class search 请求格式；
- 2005 手机绑定接口与校友录权限判断是否同一后台；
- 2006 AJAX endpoint 的 URL、response encoding 与 archive 可保存性；
- 相册原图 host / CDN；
- Flash / ActiveX 是否参与批量上传或其他功能；
- 2009 以后人人网与旧校内关系数据迁移的精确 schema。

这些都不能从今天的回顾文补齐。

---

## 十一、Archive / M1 状态

### `M1 = NOT ACHIEVED IN THIS SLICE`

本轮已经取得多个明确 historical locator：

```text
www.chinaren.com
www.5460.com
www.5460.net
alumni.chinaren.com
alumni.chinaren.com/class/class_index.jsp?classuuid=...
```

并获得：

- 2001 同期站点观察；
- 2004 用户教程；
- 2004 真实 class URL pattern；
- 2005 产品/IM 联动说明；
- 2006–2007 页面技术改版说明；
- 2008 同期用户使用材料。

但是：

> **本轮没有实际打开并检查一份满足 `docs/METHOD.md` 合同的 1998–2010 Wayback/WARC replay。**

普通 Web 搜索没有给出可直接核验的目标历史 replay；对 archive/CDX 路径的尝试也未取得一份可记录 headers / capture datetime / resource status 的合格 response。

所以正确结论只能是：

> **本轮未验证到 historical capture。**

不能写：

> “Wayback 没有保存。”

因此 M1 所要求的：

- >=2 historical timestamps；
- archive response；
- missing-resource inventory；
- charset；
- old-browser assumption；
- 主文档 / 子资源保存情况；

仍未达到。

---

## 十二、后续 capture 验证优先级

下一次若继续此对象，优先尝试以下窄目标，而不是大规模抓取：

### Target A — ChinaRen 2004

```text
original_url: http://alumni.chinaren.com/
expected era: 2004-06 around PChome tutorial
```

要记录：

- capture datetime；
- HTTP / replay status；
- charset；
- login/register entry；
- university/middle/primary navigation；
- CSS/JS 子资源；
- 是否 frameset/table；
- archive rewrite 是否破坏表单。

### Target B — ChinaRen class page 2004

只用已公开的 URL pattern，不在仓库公开普通用户完整 class ID。

要确认：

- path 是否真的 replay；
- 未登录看到什么；
- member list 是否 require session；
- guestbook/photo links 是否动态；
- privacy risk。

### Target C — ChinaRen 2006–2007

目标是验证平台宣称的：

- table → DIV+CSS；
- Ajax；
- 班级动态；
- 相册；

是否能从实际 capture 观察到，而不是只靠改版稿。

### Target D — 5460 2001 / 2004

重点检查：

- `www.5460.com` → `www.5460.net` 的精确时间与重定向关系；
- 学校重复记录怎样呈现；
- 班级 URL schema；
- charset / HTML style；
- 用户登录后的内容是否 archive-blind。

---

## 十三、对平台谱系研究的新增结论

本轮最有价值的不是补了一个“怀旧网站”，而是给 M2 增加了一条更具体的形态链：

```text
paper class contact list
→ Web school/class directory
→ persistent class page
→ directory + IM
→ directory + profile + photos + guestbook
→ AJAX / activity updates
→ campus real-name social graph
→ general SNS / feed
→ low-activity memory archive
```

这里绝不能写成技术必然进化。

真正需要研究的是每一步新增了什么状态，也丢掉了什么：

- directory 提高可发现性；
-实名/手机号提高某些身份信号，但也增加暴露；
- IM 提高即时到达性；
- feed 增加环境式更新，却可能稀释班级目录的中心性；
- 平台集中托管让关系历史更易保存，也让关站风险集中。

---

## 十四、Claim ledger

| Claim | Grade | Confidence | Boundary |
|---|---|---|---|
| 2001 同期媒体已把 ChinaRen 与 5460 作为网上校友录对象 | B | high | 只证明媒体观察到的服务存在与用途 |
| 2001 5460 出现重复学校记录、影响查找 | B | medium-high | 单篇同期观察，不做全站频率推断 |
| 2004 ChinaRen 校友录入口为 `alumni.chinaren.com` | B | high | 同期用户教程支持 |
| 2004 可搜索/创建大学、中学、小学班级 | B | high | 操作教程支持，后台实现未知 |
| 2004 ChinaRen 存在 `class_index.jsp?classuuid=` URL pattern | B | high | 同期论坛链接；完整普通用户 ID 不再发布 |
| 创建 class page 不等于形成活跃班级 | B | high | 同期论坛直接给反例 |
| 2005 校友录找同学与手机绑定条件相关 | B | medium-high | 产品报道；精确后端规则待 capture/手册 |
| 2006 ChinaRen 首页从 table 转 DIV+CSS、大量用 AJAX | A/B vendor claim | high for claim | 需要历史 capture 才能验证实际页面 |
| 2007 ChinaRen 增加相册/班级动态/多媒体/博客互通 | A/B vendor claim | high for claim | 不代表所有用户或浏览器可执行 |
| 账号加入班级不能直接证明现实同学身份 | B + inference | high | 冒名诈骗/管理员提醒支持状态分离 |
| 2008 用户会按毕业照姓名逐个搜索老同学 | B | high for interviewed user | 不能推出普遍比例 |
| 平台低活跃不等于旧数据低保存价值 | B/C | high as mechanism | 2018–2024 afterlife 材料支持 |
| 2024 人人暂停服务 = 数据已丢失 | none | **unsupported** | 平台反而宣称数据仍受保护；用户访问性与后端留存必须分开 |

---

## 十五、为什么这对“普通人怎样活”重要

旧网考古通常容易盯着首页颜色、导航栏和 Flash。

网上同学录提醒我们：**有些旧网页真正改变的不是“人看了什么页面”，而是一个多年以前认识的人，是否还具有机器可检索的地址。**

它把“班级”从一次性的物理共同体变成一个长期数据库坐标，也把“同学”从记忆里的姓名变成可以被搜索、验证、留言、加好友、再次联系的账号。

但这也意味着，一整代人的部分关系史后来被交给：

```text
domain
+ account database
+ password recovery
+ relation graph
+ photo storage
+ access-control code
```

共同托管。

所以当我们今天考古 `alumni.chinaren.com` 或 5460 时，真正丢失的可能不只是某张 800×600 的旧网页截图，而是：

> **“毕业以后我们到底怎样没有彻底失去彼此”这套普通生活基础设施。**

---

## Sources

- [S1] 《中华读书报》，2001-01-10，《家园与梦想之间》：https://www.gmw.cn/01ds/2001-01/10/GB/2001%5E334%5E0%5EDS919.htm — B，同期网站观察。
- [S2] PChome，2004-06-23，《百花争艳网上同学录》：https://m.pchome.net/article/content-17875-all.html — B，同期用户教程。
- [S3] CFC 中文网论坛，2004-09-05，《开了个校友路!大家有兴趣进来吧!》：https://bbs.comefromchina.com/threads/278456/ — B，同期用户 URL/使用痕迹；隐私最小化处理，不复制完整班级 ID。
- [S4] 搜狐，2005-03-01，《Chinaren校友录搜Q版 真正意义上实现了IM与校友录的互通》：https://news.sohu.com/20050301/n224481302.shtml — B / vendor-product material。
- [S5] 搜狐，2007-03-02，《ChinaRen校友录全新改版 四大产品构架中国最大的年轻人社区》：https://www.sohu.com/a/307988831_120136162 — A/B，平台技术与产品宣称；规模数字不当作独立统计。
- [S6] 东方网 / 新浪，2004-07-18，《大学同学录暴露身份 “高中校友”来行骗》：https://news.sina.com.cn/s/2004-07-18/11503119822s.shtml — B，同期身份风险个案。
- [S7] 中国青年报 / 中新网，2008-10-13，《虚拟网络交友成为过去 实名制网站火爆大学校园》：https://www.chinanews.com.cn/edu/dxxy/news/2008/10-13/1409431.shtml — B，同期用户采访。
- [S8] 《解放日报》/ 新浪，2005-03-18，《“我的大学”虚拟化》：https://news.sina.com.cn/s/2005-03-18/09105394097s.shtml — B，同期网上班级使用材料。
- [S9] 《长春晚报》/ 新华网，2018-11-19，《人人网被卖出网络上很平静 还有多少人去“找同学”》：https://www.xinhuanet.com/politics/2018-11/19/c_1123731824.htm — C/B，旧用户回顾与当时数据保存态度。
- [S10] 扬子晚报 / 人民网，2019-10-28，《人人网归来，你找回旧密码没？》：https://media.people.com.cn/n1/2019/1028/c14677-31424126.html；北京日报 / 人民网，2019-12-31，《人人网推新APP回归社交市场》：https://media.people.com.cn/n1/2019/1231/c40606-31529296.html — B，afterlife / account recovery。
- [S11] 青年报·青春上海，2024-12-03，《人人网暂停服务，在“建群成风”的时代，社群网站走向何方？》：https://www.why.com.cn/wx/article/2024/12/03/17332055881316521739.html — B，afterlife / user memory value + platform claim。
- [S12] 扬子晚报 / 新浪，2024-12-03，《人人网疑停止服务，团队回应：正在升级请等待》：https://finance.sina.com.cn/jjxw/2024-12-03/doc-incyekxt4849167.shtml — B，afterlife / backup attempts + platform response。

> 本笔记是 research companion，不是 M1 完整 case。任何未来 reconstruction 必须另行标记 `reconstruction`，并以实际 archive capture 为依据。