# Dating / Matchmaking Profile Search, Message and Offline-Meeting State Gaps, 2003–2015

## Scope

本笔记研究约 2003–2015 中文旧 Web 中的婚恋/交友站点如何把“寻找伴侣”拆成一组网页与后台状态：注册、profile、搜索、认证、发信、线下活动和真实见面。

它**不是**中国婚姻史，也不把全球 Minitel / CompuServe 等前史塞进本仓；跨国前史和 1981–2026 普通生活变化见 sister repository：

`tmzncty/how-people-lived/topics/from-newspaper-personals-to-platform-matchmaking-partner-addressability-and-mate-search-executability-china-1981-2026.zh-CN.md`

本仓只问 old-Web archaeological questions：

- historical site / host / URL 到底是什么；
- 哪些流程有同时代操作证据；
- 哪些只是平台宣传；
- 哪些 transaction state 只存在于动态 backend，archive 很可能看不到；
- 页面留下以后，我们最容易误判什么。

按照仓库方法：

> `platform ≠ site ≠ page ≠ capture ≠ transaction ≠ offline outcome`。

---

## 1. 证据等级

沿用本仓 A/B/C/D：

- **A**：原始/同时代页面、WARC、操作痕迹、同时代手册等；
- **B**：近同时代新闻、记者操作、平台负责人访谈；
- **C**：后来回忆；
- **D**：研究者复原/推断。

本轮有多个非常具体的 historical locator 和同时代 workflow 报道，但**没有成功打开并验证一份满足 M1 条件的 2003–2010 婚恋网站完整 Wayback/WARC transaction capture**。

因此：

- historical DOM：unknown；
- HTTP charset / response header：unknown；
- form `action` / GET vs POST：unknown；
- cookie / session：unknown；
- 搜索 ranking：unknown；
- 私信 backend：unknown；
- 身份/学历认证 backend：unknown；
- profile 删除/婚恋状态关闭逻辑：unknown。

发现 locator 不能升级成 verified capture。

---

## 2. Historical locators and platform families

### 2.1 世纪佳缘早期 host：`www.love21cn.com`

2006 年新浪科技对创办人的同期访谈明确给出：

- platform：世纪佳缘；
- host：`www.love21cn.com`；
- 创办时间陈述：2003-10-08；
- 平台当时把身份证明、学历证明等作为真实性机制的一部分进行宣传。

证据等级：**B：同期平台负责人访谈**。

Source:
- 新浪科技，2006-01-23，https://tech.sina.com.cn/it/2006-01-23/1115827191.shtml

2007 年《北京日报》又记录其初期技术形态：一台普通 PC、FrontPage 做的简单网页和 `www.love21cn.com` 域名。

证据等级：**B/C：近时回顾**。

Source:
- 《北京日报》/搜狐，2007-05-18，https://business.sohu.com/20070518/n250102769.shtml

### 2.2 一个罕见的具体 transaction locator：`/xiangqin/index.html`

2007 年《京华时报》在地坛春节相亲活动报道中明确给出：

`http://www.love21cn.com/xiangqin/index.html`

报道描述：

1. 用户访问页面；
2. 填写个人信息；
3. 相关征友信息很快在网页上显示；
4. 线下活动把这些资料再次悬挂到现场；
5. 感兴趣者向资料下的小信封投入纸条；
6. 工作人员转交；
7. 部分参与者现场面对面互动。

证据等级：**A/B：同期具体 locator + workflow description**。

Source:
- 《京华时报》/新浪，2007-02-13，https://news.sina.com.cn/c/2007-02-13/035311227831s.shtml
- 同一活动后续，2007-02-20，https://news.sina.com.cn/s/2007-02-20/011912348522.shtml

Important：

> 这证明该 URL 在同期报道中被作为报名入口引用，并证明报道所描述的 hybrid workflow；它**不是**本轮已验证的 archived page capture。

### 2.3 `jiayuan.com` domain migration

2011 年 TechNode 对创办人和公司历史的近时报道说，`love21cn.com` 在 2007 年更换为 `jiayuan.com`。

证据等级：**B/C**。

Source:
- TechNode, 2011-05-17, https://technode.com/2011/05/17/jiayuan-founder-haiyan-gong-nasdaq/

当前不能从“域名更换”自动推出：

- 两个域名所有 URL 一一重定向；
- account ID 连续；
- profile URL 连续；
- search index 连续；
- image/static host 连续；
- archive coverage 连续。

这形成一个 **domain-migration continuity gap**。

### 2.4 百合网：测试/推荐式 Web interaction

2006 年《三联生活周刊》记者实际完成百合网约 100 道恋爱测试，系统返回恋爱类型和两名候选，显示 85% / 90% 匹配度；其中一个候选的多个字段保密且没有照片。

证据等级：**A/B：同时代 reporter-operated observation**。

Source:
- 《三联生活周刊》/新浪，2006-09-29，https://news.sina.com.cn/s/2006-09-29/180011139304.shtml

这说明至少在记者当次使用路径中存在：

```text
questionnaire
→ type/result generation
→ candidate recommendation
→ profile field visibility controls
```

但它不证明：

- 算法公式；
- ranking backend；
- 候选是否在线；
- match score 是否可重复；
- score 是否预测线下结果。

### 2.5 2008 同期平台模式描述

2008 年《新世纪周刊》把三个模式并置：

- 百合：心理测试/匹配；
- 珍爱：注册 → 推荐 → 人工红娘 → 见面；
- 世纪佳缘：注册 → 搜索 → 发信 → 约会。

Source:
- 《新世纪周刊》/新浪，2008-08-19，https://news.sina.com.cn/c/2008-08-19/115016140459.shtml

证据等级：**B**。

这个材料的重要性在于：

> “婚恋网站”不能当成单一 interface family。

搜索式、推荐式、人工 redirection、心理测评、线下 event handoff 都会产生不同的 state gaps。

---

## 3. Reconstructed state model

以下是研究者状态模型，等级 **D**。它不是任何一个具体网站原始数据库 schema。

```text
Platform discovered
│
├─ landing page reachable?
│
├─ account creation
│   ├─ username / email / mobile?
│   ├─ password accepted?
│   └─ account activated?
│
├─ profile creation
│   ├─ age / sex / location / education / occupation
│   ├─ relationship / marital status
│   ├─ self-description
│   ├─ partner requirements
│   ├─ photo upload
│   └─ visibility controls
│
├─ credential / trust layer
│   ├─ identity document submitted?
│   ├─ education proof submitted?
│   ├─ platform reviewed?
│   ├─ accepted / rejected / pending?
│   └─ what badge/result is public?
│
├─ discovery
│   ├─ query filters
│   ├─ ranking / recommendation
│   ├─ profile result
│   └─ profile view
│
├─ contact
│   ├─ message / letter sent
│   ├─ paid credit / membership required?
│   ├─ delivered?
│   ├─ read?
│   ├─ replied?
│   └─ off-platform contact exchanged?
│
├─ hybrid / offline handoff
│   ├─ event signup
│   ├─ event admission / payment
│   ├─ printed profile / staff mediation
│   ├─ body actually arrives
│   ├─ introduction actually occurs
│   └─ later private contact
│
└─ outcome
    ├─ no reply
    ├─ chat only
    ├─ meeting
    ├─ repeated meetings
    ├─ relationship
    ├─ marriage
    ├─ profile remains stale
    └─ account/profile closed or deleted
```

Archive 通常只能看到其中极少的 public states。

---

## 4. Hard state boundaries

### 4.1 `registered member ≠ active member`

平台宣称的累计会员可能包括：

- 已结婚但未注销；
- 只注册未填写资料；
- 长期不登录；
- 重复账号；
- 被限制或已离开用户。

除非源明确给出 active definition，否则不能把累计注册数当 contemporaneous active dating population。

### 4.2 `profile exists ≠ subject still searching`

旧 profile 今天仍可访问，可能只是数据库遗留。页面本身不证明当事人仍单身、仍授权公开或仍使用平台。

### 4.3 `profile field ≠ verified fact`

年龄、学历、住房、职业等自述字段必须与认证状态分开。

### 4.4 `verification badge ≠ all claims verified`

平台宣传“身份认证”不能自动扩展成：照片、收入、住房、婚姻状态、职业和所有学历字段均已核验。

### 4.5 `match score ≠ compatibility`

2006 reporter walkthrough 证明网页返回 match percentage；它不能证明算法预测有效。

### 4.6 `search result ≠ mutual match`

Search 是单边查询；关系需要另一人也同意。

### 4.7 `message sent ≠ received / read / replied`

Archive 可能保存“发信”按钮，却保存不了用户的 private inbox 状态。

### 4.8 `contact exchanged ≠ meeting`

QQ、电话、email、站内信转移到线下以后，Web archaeology 很容易失去 outcome。

### 4.9 `event page exists ≠ participant attended`

2007 地坛活动把 Web 页面接到线下现场；只有报名页面不能证明报名者身体到达。

### 4.10 `meeting ≠ relationship ≠ marriage`

媒体和平台更爱保存成功故事，但 failure states 才是最容易消失的普通状态。

---

## 5. 2007 地坛案例：Web data became paper and bodies

这个案例特别适合 old-Web archaeology，因为它破坏了“网页状态”和“现实状态”的简单二分。

### 同期可观察链

```text
love21cn.com activity page
→ participant enters personal info
→ profile displayed online
→ organizer reproduces profile at physical venue
→ interested visitor leaves paper note
→ staff delivers note
→ participants may meet face to face
```

### 还存在的 phone/privacy layer

同期报道还提到，提前订票者可获得一个用于联系的“佳缘通”号码，让中意者在不知道报名者常用联系方式的情况下联系。

这个事实说明 early online dating 并不是天然“把手机号公开给所有人”。平台/活动方已经在尝试把：

`reachability` 与 `direct disclosure` 分开。

### Archaeological implication

如果 archive 只留下报名 page：

- 我们可能看得到输入说明；
- 看不到当天数据库里有谁；
- 看不到谁被打印；
- 看不到纸条；
- 看不到 staff delivery；
- 看不到实际见面。

这是一种 **online-to-offline state collapse**。

---

## 6. Search / filter archaeology

2006 的媒体材料已经留下年龄、身高、地域、认证分等搜索条件的描述；2008 世纪佳缘模式也被概括为 `注册 → 搜索 → 发信 → 约会`。

但如果没有 transaction capture，以下都不能从静态页面猜：

- filter 是 `<select>`、checkbox 还是 free text；
- 是否 GET query；
- hidden field；
- charset；
- query 参数名；
- paginated result URL；
- 默认排序；
- paid member 是否影响排序；
- inactive profile 是否仍返回；
- exact-match vs range semantics；
- city code / occupation code；
- result truncation。

尤其不要用今天 `jiayuan.com` / `baihe.com` 的 DOM 去补 2006 页面。

---

## 7. Credential / trust archaeology

2006 平台方已经把身份证明、学历证明和“信用认证”作为信任机制的一部分。

历史复原至少要拆：

```text
user enters claim
→ user chooses whether to submit proof
→ proof upload / offline delivery?
→ backend receives
→ human / machine review?
→ pass / fail / pending
→ badge or score written to profile
→ search/filter may use badge?
```

### Public-credential / private-verification asymmetry

Archive 最可能保存：

- “已认证”图标；
- 信用分；
- FAQ；
- 上传说明。

Archive 最不应/最难保存：

- 身份证扫描件；
- 学历证书；
- phone verification；
- 后台审核日志；
- rejection reason。

因此：

> `public badge visible` 可以是证据；`how it was produced` 仍可能 unknown。

---

## 8. Private message preservation gap

婚恋网站的核心 transaction 往往恰恰在 archive 最难保存的位置：

```text
profile view
→ send private letter
→ inbox
→ reply
→ exchange QQ / email / phone
→ leave platform
```

公共 Web archive 可能只保存：

- profile shell；
- “发信”按钮；
- pricing page；
- success story。

真正决定关系是否启动的：

- letter content；
- reply；
- block / ignore；
- harassment report；
- contact exchange；
- no-show；

通常都不在 public crawl 中。

这构成：

> **public-profile / private-negotiation asymmetry**。

---

## 9. Deletion and stale-profile state

婚恋平台对历史研究有一个比普通论坛更严重的时间问题：

> profile 的事实很快会过期。

可能状态：

- user 找到伴侣但 profile 仍在线；
- user 很久不登录但仍被搜索；
- user 隐藏 profile；
- user 请求删除；
- platform 仅 deactivate，不物理删除；
- search engine/cache/archive 仍有旧版本。

本轮没有可靠恢复 2003–2010 各站点具体 deletion UI，因此不能写“用户可以/不能自行删除”。

这也形成 privacy rule：

> 不为了研究 stale-profile 机制而重新收集、索引或扩散普通用户的旧征婚资料、照片和联系方式。

---

## 10. Parent / subject ambiguity

2007 地坛活动已经明确设有父母参与区域。到了后来的平台时代，父母还可能代为浏览或操作。

因此历史 profile 的“主体”与“操作者”必须分开：

```text
profile subject
≠ account operator
≠ payer
≠ parent/relative who selected candidate
```

如果旧页面只说“为女儿征婚”或“家长代征”，不能把 parent’s preference 自动当成 subject’s own preference。

---

## 11. Platform business model is part of the interface

2008 同期报道已经显示婚恋站存在：

- free/simple registration；
- paid VIP；
- 人工红娘；
- 心理测评；
- annual membership；
- paid offline events。

因此 search / contact executability 可能依赖付费状态。

Archive 若只保存 public landing page，很容易漏掉：

- message credits；
- paywall；
- VIP search visibility；
- offline event ticket；
- staff-mediated introduction。

要固定一个 hard boundary：

> `profile searchable ≠ contact executable for a free account`。

本轮未恢复足够 transaction evidence 来比较 2005–2015 各平台具体收费限制。

---

## 12. Mobile transition is not identical to Web disappearance

到 2010s，婚恋服务逐渐进入 mobile/app 环境，但对于本仓不能简单写：

> “App 出现，所以 Web 结束。”

需要继续核：

- Web 注册是否还能用；
- mobile 是否复用同一 account database；
- message state 是否同步；
- deep link / WAP / app 与桌面 Web 如何 handoff；
- profile URL 是否继续可被搜索引擎看到；
- old host 是否只剩 landing/SEO shell。

2007 年已经存在把婚恋信息带到移动终端的尝试，但当时不是今天意义上的 smartphone-app ecosystem。不要后见性压平成一条“PC → App”直线。

---

## 13. Preservation biases

### 13.1 success-story bias

平台和媒体最爱保存：

- “在本站结婚”；
- 闪婚；
- 名人/高学历用户；
- 高匹配分。

最难留下：

- 没人回复；
- 主动退出；
- 见面失败；
- 拒绝；
- 用户认为浪费时间。

### 13.2 active-profile survivorship bias

能被 crawler 看到的 profile 不等于当时所有用户；private/hidden/deleted users 天然缺席。

### 13.3 image-dependency gap

征婚 profile 强依赖照片。如果 HTML 被保存而图片 host 丢失，页面仍“可读”，但历史用户当时做判断的核心信息可能已经消失。

### 13.4 query-result snapshot bias

搜索结果高度依赖：

- session；
- login；
- query；
- time；
- account state；
- paid privilege；
- dynamic database。

一个 archived result page 只能证明那一次 capture，不应推广成稳定 ranking。

### 13.5 public-profile / private-negotiation asymmetry

公开 profile 易保存，私信和关系结果难保存。

### 13.6 provider narrative bias

会员数、成功对数、认证率如果来自平台，应保留“平台声称”，不能无条件转为独立测量。

### 13.7 heterosexual-marriage visibility bias

大型婚恋站的公开材料强烈偏向异性婚姻和“严肃婚恋”。不要因此推断其他亲密关系、同性/酷儿社群或非婚关系在旧中文 Internet 中不存在。

---

## 14. Cross-source evidence table

| Date | Object | Evidence | Grade | Proves | Does not prove |
|---|---|---|---|---|---|
| 2003/2007 | `www.love21cn.com` | 2007 北京日报回顾 FrontPage + domain | B/C | early site family / rough tech origin | original DOM, host stack, account backend |
| 2006 | `www.love21cn.com` | 新浪对创办人同期访谈 | B | host, platform identity, verification claims | verification coverage / backend |
| 2006 | 百合网 | 三联记者亲自做约 100 题测试 | A/B | questionnaire + result + recommended profiles existed in observed session | algorithm validity / stable ranking |
| 2007 | `/xiangqin/index.html` | 京华时报具体报名 locator | A/B | event locator + online profile → offline event workflow | archived DOM / actual every submit |
| 2007 | 地坛现场 | 京华时报后续 | B | physical attendance, eight-minute event, contact exchange occurred | all online registrants attended |
| 2008 | 世纪佳缘 / 百合 / 珍爱 | 新世纪周刊 | B | three distinct workflow models described contemporaneously | platform-wide conversion rates |
| 2011 | domain history | TechNode | B/C | reported love21cn → jiayuan change in 2007 | URL/account continuity |

---

## 15. M1 capture status

### Historical locators now available

- `www.love21cn.com`
- `http://www.love21cn.com/xiangqin/index.html`
- `jiayuan.com`
- `baihe.com`

### What this run did not verify

本轮没有取得并打开一份足以满足 M1 的 2003–2010 婚恋 transaction WARC/Wayback capture。

因此以下全部保持 `unknown`：

- original response headers；
- charset；
- DOM / table / frame layout；
- account registration form；
- form action；
- GET/POST；
- captcha；
- cookie/session；
- photo upload；
- search query parameters；
- result paging/ranking；
- private-message request；
- payment handoff；
- credential upload/review；
- profile hide/delete；
- dynamic relationship-status update。

正确结论是：

> **本轮未验证成功，不是 archive 一定不存在。**

后续最优先 locator 是 `love21cn.com/xiangqin/index.html`，因为我们已经有一个精确到路径、日期和同期 workflow 的入口。

---

## 16. Future archive-research checklist

若后续能找到 memento：

1. 先保存 capture URL、original URL、datetime；
2. 查 response headers 和 charset；
3. 只观察公开 HTML，不提交普通用户旧隐私；
4. 记录 form method/action；
5. 记录 external JS/CSS/image host；
6. 查是否依赖 login/cookie；
7. 不真正向历史/当前 endpoint 提交测试 profile；
8. 若有 search page，只记录公开参数结构，不重新收集普通人 profile 数据；
9. 明确 page shell 与 dynamic database state 的差异；
10. 若图片/JS 丢失，按 missing resource 记录，不生成补图。

---

## 17. What this changes in old-Web archaeology

婚恋站很好地证明：

> **旧 Web 最重要的历史对象常常不是页面本身，而是页面试图打开的一段私人现实过程。**

一个 profile 页面可以存二十年，真正的关系链却可能完全消失：

```text
谁搜索到谁
→ 谁发了第一封信
→ 谁没有回复
→ 谁把 QQ / 电话给了对方
→ 谁真的坐车去见面
→ 谁见完以后不再联系
→ 谁后来关掉 profile
```

因此婚恋旧网不能写成“有多少会员、页面长什么样”的平台史。更稳妥的考古单位是：

> **public Web state 能证明到哪一步，private transaction 与 offline outcome 从哪一步开始彻底失联。**

这也与 sister repository 的生活史结论衔接：Internet 扩大了普通人原有社交圈之外的 partner addressability，但 archive 最容易保存的恰恰是“可被看见的人”，而不是那些没有回复、没有见面、退出平台、改变主意或从未愿意公开自己的人。
