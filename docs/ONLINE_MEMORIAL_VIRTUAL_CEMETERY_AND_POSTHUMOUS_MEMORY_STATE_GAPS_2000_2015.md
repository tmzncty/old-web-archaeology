# ONLINE MEMORIAL / VIRTUAL CEMETERY / POSTHUMOUS MEMORY STATE GAPS, 2000–2015

## Scope

本笔记只研究约 2000—2015 年中文 Web 中的：

- 网上纪念馆 / 虚拟墓地；
- 陵园或殡葬机构提供的在线祭奠入口；
- 纪念页、相册、留言、虚拟供品等页面对象；
- 普通账号在用户死亡后逐渐显现出的 posthumous-memory 问题；
- 这些对象的 URL、账号、收费、动态交互、存档与消失机制。

它**不是**中国丧葬史，也不把本仓 scope 扩展到全球死亡文化。

全球 Web 前史、The WELL、英语 virtual cemetery 与跨国生活史比较主要写入 companion note：

- `tmzncty/how-people-lived/topics/from-graves-to-digital-afterlives-mourning-addressability-memorial-persistence-and-posthumous-account-governance-china-1980-2026.zh-CN.md`

本仓的问题更窄：

> **当中文旧网中的一个“网上纪念馆”看起来像一座可以永久访问的数字墓地时，我们究竟能从今天留下的页面证明到哪一层？**

---

## 1. 先不要把“网上纪念馆”当成一个页面

对一个普通 memorial object，最少要拆成：

```text
现实中的逝者
→ 某个亲友 / 管理员决定建馆
→ 找到 provider / 陵园站点
→ 注册或取得管理凭据
→ 创建 memorial namespace / 馆号 / URL
→ 输入姓名、日期、简介
→ 上传照片 / 文章 / 音视频
→ provider 接受并持久化
→ 公开页面生成
→ 搜索 / 直接链接 / 家属分享使访客找到
→ 访客进入页面
→ 选择献花 / 点烛 / 上香 / 点歌 / 祭酒 / 留言
→ submit attempt
→ server acceptance
→ 可能经过 moderation / payment
→ public display / effect
→ 家属或其他访客实际看到
→ 纪念馆续费 / 管理员继续存在
→ 域名、数据库、媒体文件和 provider 继续存在
→ 数年后仍可找到
→ archive 可能捕获其中一部分公开 shell
```

任何一步都不能由下一步反推。

特别固定：

```text
memorial page exists ≠ deceased/family approval verified
memorial named for X ≠ identity of X verified
public offering button exists ≠ offering transaction accepted
message submit ≠ message published
message published ≠ family encountered it
visitor counter ≠ unique mourners
page visible today ≠ page continuously survived since creation
“永久纪念” marketing claim ≠ durable preservation
archive capture ≠ backend/session/payment/media captured
```

---

# 2. Evidence families found this round

## E1 — 2004 重庆：功能存在，但采用极低

《重庆晚报》2004-03-25 报道：

- 南山龙园前一年清明开设“网上纪念”；
- 安放 4000 余具骨灰的园区里，至报道时只有 12 名普通人建立网络纪念馆；
- 江南殡仪馆 2001 年已尝试类似业务，但没有用户，亏损后取消；
- 页面被描述为可献花、点歌、点烛、上香、祭酒、留言、看相册。

Source:

- <https://news.sohu.com/2004/03/25/99/news219599967.shtml>

Grade: **B — 同时代地方媒体。**

What it proves:

- 2001—2004 至少已有地方殡葬机构实际推出网络纪念服务；
- 虚拟供品/留言/相册类交互在同期报道中已经存在；
- `exists / available` 与 `used / normalized` 必须分离。

What it does **not** prove:

- 原站 URL；
- 页面 DOM；
- 页面是否动态生成；
- visitor counter 的统计方式；
- 12 个 memorial 是否都持续到下一年；
- 后台是否存在审核或收费。

---

## E2 — 2004 合肥：具体 historical locator

同期报道留下：

```text
http://www.dashushan.netor.com
http://www.netor.com
```

并描述按逝者姓名建立纪念空间、点烛点歌、献花祭酒、相册与纪念文章等功能。

Source:

- 江淮晨报 / 新浪，2004-03-30：<https://news.sina.com.cn/c/2004-03-30/02152172262s.shtml>

Grade: **B — 同时代媒体。**

Status:

- `original_url locator`: **known**
- `verified historical memento`: **not obtained this round**
- `historical DOM / charset / headers`: **unknown**
- `backend transaction`: **unknown**

这一条是很好的 M1 candidate，但不能因为 URL 很具体，就把它写成 verified capture。

---

## E3 — 2008 普通家庭实际使用：网络纪念页作为远方亲友共同入口

《南都周刊》2008 年跟访广州普通家庭：27 岁林良英为去世妹妹付费建立纪念馆，一个实际用途是让外地同学朋友也能参与。第一个清明期间，页面有节日版式，亲友献歌、点烛、留言。

Source:

- <https://news.sina.com.cn/c/2008-04-09/164415322655.shtml>

Grade: **B — 同时代深度报道，含第一人称。**

What it proves:

- 至少在一个普通家庭案例中，public / shareable memorial page 已进入真实异地关系协调；
- ritual UI 的报道层功能包括歌、烛、留言等；
- provider 存在付费建馆状态。

What it does not prove:

- 页面请求链；
- 每个外地同学是否真正到达；
- “献歌”是否调用外部媒体资源；
- 是否 Flash / JS / iframe；
- 付费 gateway；
- 纪念馆几年后的存活状态。

---

## E4 — 2008 “永久页面”的现实反例：provider survival risk

《中国青年报》2008-04-07 调查指出，多数在线祭扫服务收取建馆、维护或虚拟祭品费用；受访/报道中的消费者担心付费以后网页或经营者消失，因此不愿尝试。

Source:

- <https://zqb.cyol.com/content/2008-04/07/content_2132646.htm>

Grade: **B — 同时代调查报道。**

This is not only a consumer-history detail. For old-web archaeology it establishes a historically contemporaneous state gap:

```text
provider claims long-term / permanent memorial
≠
user can verify future provider survival
```

因此不要从 memorial page 的语义“纪念馆 / 永久 / 墓地”推断技术保存性。

---

## E5 — current live legacy shell: Netor 管理页仍可观察，但不能冒充 2004

2026-09-06 本轮检索中，`https://cn.netor.net/` 仍有可访问的 legacy-looking 页面，并可观察到形如 `m/manager/man_<id>.html` 的管理页 URL pattern。按本仓隐私最小化原则，这里只记录 host 与抽象 pattern，不保留普通纪念对象的具体 numeric ID。

当前页面层可观察到诸如：

- 管理 / 祭奠 / 留言 / 链接 / 年谱 / 相册 / 文选等 tab；
- 馆号 / 用户 / 密码 / 验证码式管理登录 shell；
- footer 中的 Netor 品牌与长期年份文字。

Grade: **A for current 2026 surface, NOT A for 2004 history.**

Strict rule:

```text
current live legacy page carrying old design/content
≠
verified historical page representation
```

当前页最多能提供：

- 今天仍存的对象命名；
- today-current navigation taxonomy；
- 一个可能追索旧 URL pattern / account model 的线索。

不能用它证明：

- 2004 的 HTML 结构；
- 2004 也有完全相同 tab；
- 2004 的 charset；
- 从 2000 到 2026 无中断运营；
- 历史数据库始终连续。

---

# 3. Proposed state model

## 3.1 Memorial creation state

```text
candidate creator
→ registration page reachable
→ account created
→ creator authenticated
→ memorial creation form reachable
→ required identity fields entered
→ memorial name accepted
→ media uploaded
→ server accepted object
→ memorial ID / URL allocated
→ public shell available
```

Unknowns likely to matter in 2000s Chinese Web:

- 是否要求真实姓名 / 身份证 / 手机 / email；
- 创建者与逝者关系是否验证；
- 姓名字段是 GB2312 / GBK / UTF-8 哪一层；
- 图片上传大小、格式、客户端插件；
- 馆号是否 numeric primary key；
- 页面是静态生成、ASP/JSP/PHP 动态模板还是混合；
- memorial object 是否免费、试用或付费后才 public。

## 3.2 Visitor / ritual state

```text
visitor has URL or search term
→ resolves host
→ page returned
→ page renders enough UI
→ visitor selects ritual object
→ JS / link / form works
→ request reaches server
→ payment requirement? (if any)
→ server stores state
→ counter / icon / message changes
→ other viewers can observe result
```

Hard gaps:

```text
button visible ≠ click handler works
click handler works ≠ server accepts
server accepts ≠ persistent state
persistent state ≠ public state
public state ≠ family encounter
```

If a capture replays a “鲜花”“香烛” icon but the POST endpoint is missing, the correct conclusion is **ritual control visible, transaction unknown**.

## 3.3 Message / guestbook state

```text
message form visible
→ input
→ submit
→ server acceptance
→ moderation / spam filter
→ database record
→ display ordering
→ pagination
→ eventual deletion / hiding
```

Archive risk:

- GET-visible guestbook pages may survive;
- POST action usually does not;
- moderation queues are private;
- deleted hostile/spam messages may vanish;
- page 1 may survive while older pagination disappears.

Therefore a quiet guestbook is not evidence of a quiet bereavement community.

## 3.4 Payment / renewal state

```text
free / trial object
→ fee schedule
→ payment instruction
→ payment accepted
→ entitlement period
→ renewal reminder
→ renewal paid or missed
→ memorial remains / downgraded / hidden / deleted
```

This layer is crucial because contemporary 2008 reporting explicitly shows users worried about fees and provider survival.

Archive shell often preserves **价格表** better than it preserves whether a specific memorial was actually renewed.

## 3.5 Provider survival state

```text
brand survives
host survives
DNS survives
HTTP service survives
application survives
database survives
media object store survives
user credentials survive
billing relationship survives
public URL mapping survives
```

These are separate.

A domain resolving 20 years later does not prove the original database survived. A brand continuing does not prove the same owner or application stack. A current memorial ID resolving does not prove uninterrupted public availability.

---

# 4. A posthumous account is not automatically a memorial account

By the late 2000s and early 2010s, ordinary users increasingly left QQ, blogs, SNS profiles, email, cloud files and game/payment accounts. After death, these may become memorial artifacts without ever having been designed as memorials.

This requires a second state model:

```text
person alive
→ account actively maintained
→ person dies
→ platform may not know death state
→ credential remains active
→ friends continue seeing old profile/content
→ relatives may or may not possess password/phone/email
→ login recovery may continue through old credential
→ account may remain, freeze, delete, transfer, be hacked, or become unreachable
```

Strict distinction:

```text
purpose-built memorial page
≠
ordinary account that outlives its user
```

The 2019 public discussion of QQ / WeChat / Weibo / Alipay / cloud storage as “digital legacy” is outside this file’s 2015 endpoint as a later interpretive source, but it helps identify what 2000–2015 evidence should be sought: terms of service, inactivity/deletion policy, password recovery, phone/email binding, and family requests after account-holder death.

Later-source locator:

- 中国新闻网 / 人民网，2019-05-07：<https://industry.people.com.cn/n1/2019/0507/c413883-31071387.html>

Grade here: **C relative to the 2000–2015 technical states, useful as research lead, not proof of earlier policy.**

---

# 5. Archive biases specific to online memorials

## 5.1 Public-memorial-shell / private-bereavement-state asymmetry

Archive can often see:

- memorial title;
- deceased display name;
- public biography;
- public photographs (if fetched);
- virtual offering icons;
- public guestbook;
- provider marketing / pricing;
- public counter.

Archive usually cannot or should not expose:

- creator identity verification;
- family dispute over creation/deletion;
- private contact details;
- password / recovery email / phone;
- payment records;
- moderation queue;
- private messages;
- whether relatives actually encountered a public message;
- who approved ongoing hosting.

Therefore:

> **A richly archived memorial page can tell us much more about the provider’s public shell than about the family’s full grief process.**

## 5.2 Provider-survival bias

The very providers easiest to study in 2026 are those that survived long enough to leave searchable traces.

Failed 2001—2008 experiments, abandoned domains and unpaid memorials are systematically harder to see.

The 2004 Chongqing article is important precisely because it preserves a failed/low-adoption branch that a “surviving websites only” sample would miss.

## 5.3 Qingming-season media bias

Most contemporary reporting clusters around late March / early April.

This makes it easy to overestimate:

- how much memorial pages were visited outside Qingming;
- whether they functioned as daily continuing-bond spaces;
- how much of the provider’s annual traffic depended on a short seasonal spike.

Capture density may also be higher around seasonal media attention.

## 5.4 Success-story bias

Media prefer:

- distant relative successfully participates;
- moving memorial message;
- novel virtual ritual.

Less visible:

- no one visits;
- forgotten password;
- family disagrees;
- memorial expires;
- payment fails;
- media URLs rot;
- provider closes.

Research must deliberately preserve these negative states.

## 5.5 Ritual-interface survivorship bias

Icons and labels are easy to screenshot. Their transaction logic is not.

A future researcher may see:

```text
献花  上香  点烛  祭酒
```

and mentally complete a successful ritual flow. That is precisely what this repository must not do.

---

# 6. Browser / encoding / media reconstruction risks

For 2000—2010 memorial sites, plausible historical dependencies include:

- GB2312 / GBK / early UTF-8 transitions;
- table layout;
- image maps;
- JavaScript event handlers;
- pop-up windows;
- embedded WMA/MP3/MIDI;
- Flash ritual animation;
- IE-specific DOM or ActiveX/media controls;
- iframe / frameset;
- external counters and guestbook services.

**These are hypotheses, not findings for Netor in this round.**

Until a historical capture or software/manual evidence is inspected, do not write:

> “Netor used Flash for virtual offerings”

or:

> “The site required IE6.”

Correct wording is:

> “The reported interaction model makes script/media dependencies an important M1 question; current evidence does not establish the historical implementation.”

A modern Chromium replay of a surviving page may:

- silently substitute fonts;
- decode Chinese with a guessed charset;
- block mixed content;
- fail old media plugins;
- rewrite archive URLs;
- omit cross-origin media;
- run code differently from historical IE.

So a modern screenshot cannot be labeled “what a 2004 mourner saw.”

---

# 7. Claim discipline for this case family

## Safe claims

- “A 2004 contemporary report described an online memorial service and listed specific ritual features.”
- “The report gave `www.netor.com` as a historical locator.”
- “A 2008 first-person media case described using a paid online memorial so distant classmates/friends could participate.”
- “A 2008 contemporaneous consumer report recorded fear that paid memorial pages/providers might disappear.”
- “A current 2026 Netor legacy surface exposes a management/login shell and memorial navigation categories.”

## Unsafe claims without stronger evidence

- “The 2004 Netor page looked exactly like the current page.”
- “A memorial was stored permanently.”
- “All 2008 virtual offerings were server transactions rather than visual effects.”
- “Visitor counts represent unique mourners.”
- “The family approved every public memorial.”
- “The platform’s database was continuously online from 2000 to 2026.”
- “A current footer year proves uninterrupted operation.”

---

# 8. Privacy boundary: death does not eliminate privacy

This case family has unusually high risk of turning archaeology into re-publication of intimate material.

Rules:

1. Prefer provider help pages, public product pages, generic screenshots and media-described cases.
2. If a specific ordinary-person memorial is needed, quote only the minimum fact required for the claim.
3. Do not aggregate deceased person’s full name + dates + family + address + phone + account handles merely because fragments are public.
4. Do not recover hidden media, private guestbook entries or deleted family material.
5. Do not attempt password recovery or account login.
6. Do not treat an archived public page as blanket consent to republish all photographs or grief messages.
7. Do not dox surviving relatives to answer “what happened to this memorial later?”
8. 对普通纪念页的当前 URL 只记录 host 与抽象 path pattern；除非研究对象本身是公开机构页，否则不在研究笔记中保留可直接定位普通逝者的 numeric ID。

A dead person’s page may also contain living people’s messages and contact traces. Those living persons retain ordinary privacy interests.

---

# 9. Cross-link to ordinary-life interpretation

For `how-people-lived`, the main historical transition is:

```text
physical grave / kin network
→ shareable memorial URL
→ ongoing public or semi-public memory page
→ ordinary social accounts themselves outlive the person
→ survivors inherit account / credential / deletion work
```

For this repository, the same transition is observed as a sequence of technical evidence problems:

```text
place
→ URL
→ account
→ database state
→ transaction state
→ billing state
→ provider survival
→ archive capture
```

The important shared conclusion is:

> **Digital memorialization promises persistence precisely in an environment whose hosts, URLs, scripts, credentials and business models are historically fragile.**

That contradiction makes online memorials a particularly useful old-Web case family.

---

# 10. M1 candidate package

## Candidate A — Netor / 网同纪念

Known locators:

```text
http://www.netor.com
http://www.dashushan.netor.com
```

Current legacy host lead:

```text
https://cn.netor.net/
```

High-value historical questions:

- earliest valid capture datetime;
- redirect chain among `netor.com`, subdomains and later `cn.netor.net`;
- HTTP Content-Type / charset;
- memorial URL / ID pattern;
- create form;
- login form;
- offering / guestbook endpoints;
- fee/renewal pages;
- media dependencies;
- browser assumptions;
- multiple captures of one public memorial over several years, without expanding private data.

## Candidate B — cemetery-hosted Netor subdomain

`dashushan.netor.com` is particularly useful because it may show the relationship between:

```text
physical cemetery institution
+
hosted virtual memorial platform
+
subdomain ownership / branding
```

Questions:

- was it a true hosted tenant or simple redirect?
- did cemetery branding wrap Netor’s application?
- did user credentials live at cemetery or provider level?
- did public memorial URLs remain stable after institutional changes?

## Candidate C — failed / disappeared local service

The 2004 Chongqing cases should be preserved as **negative candidates**, even if no capture is found.

A well-documented “service existed in media but no reliable Web artifact survives” is valuable for Phase 5 archive-gap modeling.

---

# 11. M1 result this round: locator obtained, transaction capture not verified

This round **did not obtain and inspect a historical Wayback/WARC memento** for the 2004—2010 ordinary Chinese online memorial flow.

Therefore these remain unknown:

- historical main-document HTTP headers;
- historical charset;
- DOM structure;
- JS / Flash / media requirements;
- GET/POST form actions;
- cookie / session behavior;
- creator verification;
- moderation;
- billing gateway;
- renewal / expiry backend;
- visitor-counter semantics;
- real no-show / failed-submit rate;
- whether current Netor legacy structures match 2004.

This is an explicit METHOD stop condition, not an invitation to infer the missing states.

Current evidence status:

```text
historical locator: YES
contemporary functionality description: YES
contemporary ordinary-user use case: YES
contemporary counterexample / durability concern: YES
current legacy shell: YES
verified historical transaction capture: NO
historical browser reconstruction: NO
```

---

# 12. Evidence table

| ID | Date | Object | Type | Grade | What it supports |
|---|---|---|---|---|---|
| E1 | 2004-03-25 | 重庆地方网上纪念服务 | contemporary news | B | exists vs low adoption; failed provider branch |
| E2 | 2004-03-30 | `netor.com`, `dashushan.netor.com` | contemporary news / locator | B | domain locator; reported ritual features |
| E3 | 2008-04-09 | ordinary family paid memorial | contemporary first-person media | B | distant-friend use; shared memorial address |
| E4 | 2008-04-07 | paid online memorial consumer risk | contemporary investigation | B | permanence/provider-survival gap |
| E5 | 2026-09-06 | `cn.netor.net` live legacy surface | current Web observation | A-current only | current taxonomy/login shell, not historical DOM |
| E6 | 2019-05-07 | ordinary accounts as digital legacy | later contemporaneous social/legal discussion | C for 2000–15 technical claims | research lead for posthumous ordinary accounts |

---

# 13. What this adds to old-Web archaeology

This slice adds four archive mechanisms not yet isolated elsewhere in the repo:

### 13.1 Public memorial shell / private bereavement state asymmetry

Public pages may survive while the decisive family/credential/payment states remain invisible.

### 13.2 Promise-of-permanence / infrastructure-mortality gap

The product is sold as “lasting memory,” while the Web substrate is unusually exposed to domain, database, business and plugin death.

### 13.3 Ritual control / transaction gap

A visible icon is not evidence that a ritual POST, media action, payment or persistent state was captured.

### 13.4 Posthumous identity / credential divergence

A user can die while the platform continues to treat account credentials as live. This becomes increasingly important when tracing 2010s social accounts, but the technical roots are already present in 2000s password/email/phone-bound accounts.

---

## Checkpoint conclusion

This is a **research note**, not an M1-complete case.

It has enough independent contemporaneous evidence to establish a historically meaningful case family and specific locators, but not enough archive transaction evidence to reconstruct the original site interaction.

The correct next step is not to build a replica. It is to find and inspect a small number of real historical captures for `netor.com` / `dashushan.netor.com`, record original URL + Memento-Datetime + charset/resource gaps, and then test whether the reported ritual operations survive as actual historical page states.
