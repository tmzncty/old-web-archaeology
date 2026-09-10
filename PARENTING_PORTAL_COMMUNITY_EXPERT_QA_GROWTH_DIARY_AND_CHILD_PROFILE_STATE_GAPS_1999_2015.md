# PARENTING PORTAL / COMMUNITY / EXPERT-QA / GROWTH-DIARY / CHILD-PROFILE STATE GAPS, 1999–2015

Status: research note / state-gap model / case-candidate support  
Scope: 约 1999–2015 中文 Web 中育儿门户、专家问答、论坛/圈子、博客/成长日记、宝宝相册、按孕周/月龄组织的内容与工具，以及这些对象的 archive blind spots；**不把本仓扩展为全球育儿史，也不把 2015 年后的移动 App / 微信 / AI 当成主对象**。  
Cross-repo companion: `tmzncty/how-people-lived/topics/networked-parenting-knowledge-peer-support-growth-diaries-and-digital-care-delegation-china-1980-2026.zh-CN.md`  
Last research pass: 2026-09-10

---

## 0. Why parenting is a special old-Web object

旧网育儿页面表面上可能只是“文章 + 论坛 + 相册”，但它实际上把五类不同的状态塞进同一站点：

1. **editorial / expert knowledge**：编辑文章、医院/专家内容、在线问答；
2. **peer community**：普通父母发帖、回复、圈子、同龄/同城交流；
3. **family memory**：成长日记、照片、视频、里程碑；
4. **developmental routing**：用预产期、生日、年龄/月龄决定栏目、提醒或推荐；
5. **commerce**：用品库、推荐、团购、广告、电商入口。

它们的页面风格可能极其相似，但证据责任完全不同。

一个旧页面写着“专家指导”不能自动证明当前显示的具体建议由哪位专家审阅；一个论坛“经验帖”不能升级成医学事实；一个成长日记能证明某位父母当时这样记录，却不能升级成孩子的临床发育记录。

因此本 note 的核心命题是：

> **parenting portal shell survives more easily than the relationship between advice, profile state, community context and real care.**

Web archive 最容易保存：

- 首页；
- 阶段栏目；
- 公共文章；
- 专家列表/问答入口；
- 论坛板块首页；
- 某些公开博客/成长日记；
- 宝宝相册壳；
- 商品/广告位；
- 帮助页。

最难保存：

- 登录态；
- 父母账号与孩子档案的绑定；
- 生日/预产期驱动的个性化页面；
- 私密/半私密成长记录；
- 私信和群组上下文；
- 动态回复计数、推荐排序；
- 专家问答的完整提交/审核链；
- 当时用户究竟读了什么、相信什么、做了什么；
- 图片/CDN/头像/相册原图；
- 被删除或后来改成私密的儿童资料。

这类对象因此特别适合用来检验本仓 `page != account != backend state != real-world action` 的方法合同。

---

## 1. Evidence contract

遵循 `docs/METHOD.md`。

### 1.1 Research units

不得把“宝宝树/摇篮网/新浪亲子”整个品牌写成一个对象。至少分别记录：

- `platform`
- `host`
- `portal_homepage`
- `stage_taxonomy`
- `article_page`
- `expert_profile`
- `expert_qa_entry`
- `question_submission`
- `question_publication`
- `forum_board`
- `thread`
- `reply`
- `parent_account`
- `child_profile`
- `pregnancy_due_date`
- `child_birthdate_or_age_field`
- `growth_diary`
- `album`
- `media_asset`
- `privacy_state`
- `friend/follow/group_relation`
- `recommendation_slot`
- `commerce_slot`
- `archive_capture`
- `claim`

### 1.2 Evidence grades in this note

- **A**：当时官方页面/帮助页、仍可验证的同期原始页面、当时发布的产品公告；
- **B**：同期媒体、操作教程、用户采访、第三方报道；
- **C**：多年后的公司史、怀旧、后来用户回忆；
- **D**：根据残存导航/截图/报道推断的页面结构或状态机。

平台公司稿可证明“平台当时/后来这样宣称”，不能直接证明注册量、活跃度、医疗质量或大众普及。

---

## 2. Historical boundary: the Web did not invent expert parenting knowledge

配套生活史已经记录：北京出版集团资料将《父母必读》的创刊时间列为 **1980 年 4 月**，内容覆盖孕产、儿童保健、喂养、疾病预防和教育心理。

Source:

- https://www.bph.com.cn/guojia/detail/1545.html

Evidence: **B-institutional retrospective**.

对 old-Web 的意义不是把 1980 年代纳入仓库主 scope，而是确定边界：

```text
expert parenting content existed before Web
```

所以 1999–2015 的问题不能写成“育儿知识第一次出现”，而应问：

- 文章怎样变成可搜索 URL；
- 生命周期栏目怎样建立；
- 专家和普通用户内容怎样并置；
- 家庭记忆怎样从纸本/相册进入账号；
- 一个孩子怎样被平台表示成 profile state；
- 社区互动怎样被 crawler 保存或漏掉。

---

## 3. 1999 Yaolan as an early boundary marker — but not yet a verified Memento

摇篮网 2014 年公司稿自述：1998 年创建，**1999-12-15 正式上线**，提供孕期与 0–6 岁育儿知识、互动产品和咨询服务；另一个 2014 公司稿描述用户登录后可进入“专家在线咨询”，选择孕产/早教等类别并进行一对一实时沟通。

Sources:

- https://www.prnasia.com/story/97380-1.shtml
- https://www.prnasia.com/story/96280-1.shtml

Evidence: **A-platform self-history in 2014; C for exact 1999 user experience**.

Narrow claims supported:

- Yaolan by 2014 consistently represented its public launch date as 1999-12-15;
- its product identity included stage-specific parenting knowledge and expert consultation;
- expert consultation by 2014 included authenticated user entry and category selection.

Not supported:

- exact 1999 homepage DOM;
- 1999 charset/browser requirements;
- 2000 registered-user count independent verification;
- whether the expert-QA workflow in 1999 matched the 2014 workflow;
- nationwide ordinary-parent adoption.

### Archive attempt this pass

Candidate replay attempts for `www.yaolan.com` could not be opened through the current archive access chain because constructed Wayback URLs require prior provenance from a returned search result.

Therefore:

```text
M1 verified 1999–2003 yaolan.com historical capture:
NOT ACHIEVED IN THIS SLICE
```

This means **capture unverified**, not `Wayback has no capture` and not `site did not exist`.

---

## 4. 2007 BabyTree: a contemporary community-use artifact

A September 2007 Economic Observer article preserves unusually useful contemporary user testimony.

Source:

- https://www.eeo.com.cn/2007/0905/82270.shtml

Observed claims (B-contemporary media + first-person):

- a working mother using the nickname “梨子妈妈” described using BabyTree daily during spare time;
- activities included photo upload, growth diary, exchanging parenting experiences, and forum moderation;
- she explicitly described the diary as memory intended for years-later recall;
- she described online interaction as reducing isolation/helplessness during parenting;
- the article identifies BabyTree as a Web 2.0 Chinese parenting community and discusses planned online-to-offline extensions.

The platform traffic figures in the same article are founder/company claims and should remain tagged as such.

### 4.1 State model

A 2007 “parenting community” should not be reconstructed as only:

```text
user -> post -> reply
```

A better minimum model is:

```text
parent creates/authenticates account
→ optionally creates child/baby representation
→ enters community or profile space
→ uploads photo / writes diary / opens thread
→ content receives visibility state
→ other accounts read/reply
→ parent interprets social response
→ possible offline care/action
→ diary remains as future memory artifact
```

### 4.2 New state gaps

#### `parent-account / child-profile gap`

A parent can have an account without creating a public child profile. A child profile can also be maintained by a parent account long before the represented child can meaningfully consent.

#### `growth-diary / complete-childhood gap`

A diary records selected moments. It does not provide a neutral or complete record of childhood.

#### `community-response / trusted-advice gap`

A reply exists because another user responded; it does not become medical/professional authority by popularity.

#### `online-support / hands-on-care gap`

A parent can feel less isolated while still lacking sleep, money, time or another adult physically present.

#### `future-memory / future-access gap`

A 2007 parent can intend to read the diary “years later”; that intention is only executable if account recovery, platform survival, media assets and export all continue to work.

This last gap is particularly important for platform archaeology:

```text
memory was created for the long term
but hosted on infrastructure with a different lifetime
```

---

## 5. 2009 Sina Parenting retained pages: portal architecture without proven byte-identical replay

Sina currently exposes URL paths titled “亲子首页往日回顾” for dated 2009 pages.

Sources:

- 2009-04-28: https://baby.sina.com.cn/head/baby20090428pm.shtml
- 2009-10-28: https://baby.sina.com.cn/head/baby20091028am.shtml

The April page is indexed with navigation including:

- 健康 / 营养 / 教育；
- 准备怀孕 / 怀孕期 / 分娩期 / 新生儿 / 婴儿期 / 幼儿期 / 学龄前；
- 专家指导；
- 论坛；
- 博客；
- 宝宝相册；
- 视频。

The October page additionally exposes a navigation cluster including:

- 专家；
- 论坛；
- 博客；
- 视频；
- 专题；
- 实用工具；
- 求医问药；
- 母婴用品库。

Evidence: **A/B first-party retained dated page**.

### Critical provenance warning

These URLs are on Sina’s live domain today and are titled as historical homepage review pages. This pass has **not** established whether each file is:

- an untouched static 2009 file;
- a server-side preserved historical snapshot;
- a later reconstruction using historical content;
- or a hybrid whose navigation/assets were modified later.

Therefore do not label them `archive capture` or `Memento` without further evidence.

A safe claim is:

> Sina currently retains dated pages representing its 2009 parenting homepage architecture, and those representations show stage taxonomy + expert + community + personal-media/tool surfaces in one portal.

### 5.1 Developmental taxonomy as platform state

The stage navigation is not merely editorial. It is a candidate routing system:

```text
pregnancy/child stage
→ relevant category
→ articles / expert material / forum topics / tools / products
```

If later logged-in features used due date or birthday to personalize content, the actual state would be:

```text
stored profile field
→ computed age/stage
→ recommendation logic
→ rendered page
```

A public archived category page can preserve the taxonomy while losing the profile-driven computation entirely.

This creates `stage-taxonomy / personalized-stage-state gap`.

---

## 6. A minimum state machine for old-Web parenting services

### S0 — public portal exists

Homepage/category can be loaded.

### S1 — editorial content exists

Article title/body/source/date can be observed.

### S2 — expert/peer provenance is distinguishable

The interface tells the user whether the material is editorial, professional Q&A, user forum or advertorial.

### S3 — account exists

A logged-in parent identity is represented.

### S4 — child/pregnancy profile exists

Due date, birth date, sex/name/nickname or other stage fields may exist.

### S5 — personal content exists

Diary, album, post, favorites or tool records are stored.

### S6 — community relation exists

Replies, friends, groups, same-age/same-city circles or messages exist.

### S7 — recommendation/commerce layer reacts

Page content may be stage-, profile-, session- or ad-driven.

### S8 — real-world care/action occurs

Parent changes feeding/sleep/activity, buys an item, phones a doctor, visits a clinic, or does nothing.

Archive generally sees S0–S2 best, fragments of S5–S7, and almost never S8.

---

## 7. Reusable state gaps

### 7.1 `portal-shell / user-state gap`

A complete homepage does not reveal a logged-in parent’s personal stage, favorites, groups, diary or messages.

### 7.2 `article-publication / medical-authority gap`

An article is present and readable; its author, reviewer, update date and medical applicability may be unclear.

### 7.3 `expert-label / answer-review gap`

An “expert” surface can exist without preserving the credential verification or editorial review chain behind every answer.

### 7.4 `question-submission / question-publication gap`

A parent may submit a question that is never accepted, answered or publicly indexed.

### 7.5 `thread-view / user-action gap`

A thread can survive while there is no evidence that the original parent followed the advice.

### 7.6 `reply-count / reply-survival gap`

Count metadata can survive while individual replies are missing, or replies survive after count widgets change.

### 7.7 `child-profile / child-consent gap`

The represented person and the account operator are different people. A parent may have had authority to post in practice; the child’s later preference cannot be inferred.

### 7.8 `public-then / public-now gap`

A page public in 2009 may later become private/deleted. Archive accessibility does not automatically create an ethical right to republish child details.

### 7.9 `growth-diary / objective-record gap`

Diary entries are authored selection, not clinical observation and not a complete time series.

### 7.10 `photo-thumbnail / original-media gap`

HTML and thumbnail references may survive while original photos on separate image/CDN hosts disappear.

### 7.11 `stage-taxonomy / actual-development gap`

A portal category like “8-month baby” is a content taxonomy; it does not prove a child should or did meet every listed milestone.

### 7.12 `profile-age / render-time gap`

If a page computes “宝宝 X 个月” from stored birthday, archived HTML can show a value from capture time while modern replay scripts may recompute or fail.

### 7.13 `same-age-circle / same-experience gap`

Two children share a month age; household income, health, childcare, region and family support can differ substantially.

### 7.14 `community-popularity / population-representativeness gap`

A busy parenting forum overrepresents people who are online, willing to write, and sufficiently interested to join.

### 7.15 `ad-slot / historical-ad gap`

The HTML slot can survive while the ad creative is loaded dynamically from a later or missing ad host.

### 7.16 `product-recommendation / editorial-recommendation gap`

A product appears near health/education content; this does not prove independent editorial endorsement.

### 7.17 `searchable-question / prevalent-problem gap`

Questions that produce posts are not a denominator for how often the issue occurred in all households.

### 7.18 `account-survival / family-memory-survival gap`

Login may still work while old albums or diary assets are gone; the reverse can also occur through public orphan pages.

### 7.19 `platform-survival / memory-portability gap`

A platform can remain online but remove export/old features; a family’s future-memory intention can still fail.

### 7.20 `contemporary-page / current-medical-advice gap`

A perfectly preserved 2009 health article is a historical object. It must not be surfaced as current pediatric guidance without current verification.

---

## 8. 2007–2010 page-shape hypothesis

This is **D reconstruction hypothesis**, not a completed browser reconstruction.

Based on the dated Sina retained pages and contemporary BabyTree reporting, a representative Chinese parenting portal/community around 2007–2010 may need at least these surfaces in an experiment:

```text
[global portal header]
  ├─ health / nutrition / education
  ├─ pregnancy → preschool stage taxonomy
  ├─ expert / Q&A
  ├─ forum/community
  ├─ blog/growth diary
  ├─ baby album/video
  ├─ tools
  └─ product/commerce links

[logged-in personal state]
  ├─ parent account
  ├─ child/baby profile
  ├─ age or due-date
  ├─ diary / album
  ├─ groups/friends/replies
  └─ privacy settings
```

Unknown in this pass:

- exact `charset` for each historical host/time point;
- IE-only behavior or ActiveX requirements;
- JavaScript browser sniffing;
- upload controls;
- cookie/session names;
- image/CDN host graph;
- whether profile pages used frames, tables or DIV/CSS at each time point;
- whether Ajax loaded replies/recommendations;
- mobile/WAP variants.

Do **not** fill these with generic “2000s websites used GB2312 and IE6” assumptions. They must be measured per capture.

---

## 9. Browser / encoding experiment plan

If a verified capture becomes available, compare at minimum:

1. modern Chromium replay;
2. IE6-grade environment;
3. optional IE8/compat mode if the capture is late-2000s;
4. JavaScript disabled;
5. missing cross-host images/CSS.

Record:

- declared/meta charset and HTTP charset separately;
- mojibake behavior;
- document mode / quirks triggers;
- table/DIV layout differences;
- popup/login behavior;
- upload widgets;
- form action destination;
- script errors;
- image host failures;
- dynamic recommendation gaps;
- login redirect loops.

A minimum successful M3-style micro-experiment should list at least five interpretation differences, not merely visual differences.

---

## 10. 2015 boundary: why the repo should stop before the full mobile-parenting ecosystem

By the mid-2010s, parenting support increasingly moved into:

- native apps;
- WeChat groups/public accounts;
- mobile notification/reminder systems;
- short video/live stream;
- platform SDK login/payment;
- later AI assistants and smart devices.

These are important for the companion life-history topic but should not silently pull this repository beyond its ~1995–2015 Chinese old-Web scope.

The old-Web contribution should instead preserve the Web genealogy that those apps inherited:

```text
stage taxonomy
+ searchable expert content
+ peer discussion
+ personal child profile
+ growth diary/album
+ tools/reminders
+ commerce
```

That stack is already visible in late-2000s portal/community form.

---

## 11. Archive visibility biases specific to parenting sites

### 11.1 `problem-post overrepresentation`

Parents post when confused, worried, in conflict or seeking reassurance. Routine successful care often produces no public artifact.

Therefore:

```text
archived question volume != incidence/prevalence
```

### 11.2 `active-mother overrepresentation`

Contemporary BabyTree and later app materials often foreground mothers. This may reflect actual gendered care work, platform branding and/or sampling. It cannot automatically erase fathers, grandparents, nannies and other carers from historical reconstruction.

### 11.3 `silent-reader invisibility`

A large share of online community value can come from reading without posting. Public archives preserve writers much better than readers.

### 11.4 `private-support invisibility`

Private messages, closed groups and semi-private baby spaces may contain the strongest emotional support but are least appropriate and least technically likely to survive publicly.

### 11.5 `child-privacy inversion`

The more detailed a growth diary is, the more historically rich it looks — and the stronger the reason **not** to republish it wholesale.

For ordinary children, repository output should prefer:

- URL patterns;
- field schema;
- privacy-state description;
- aggregate layout;
- minimal quoted metadata when essential;

rather than names, faces, exact birth dates, health histories or family addresses.

### 11.6 `dynamic-commerce survival bias`

Editorial pages may survive while ad targeting, product availability, affiliate rules and recommendation ranking disappear. A modern replay can make a historical page look less commercial—or differently commercial—than it was.

### 11.7 `medical-update drift`

A historical health URL may remain live but have content revised. Stable URL != stable historical advice.

---

## 12. Contemporary evidence versus later nostalgia

The 2007 BabyTree report is especially valuable because the user testimony is **contemporary**, not a 2026 memory of “the warm old Internet.” It already contains:

- work-time scarcity;
- daily use;
- growth-diary future orientation;
- peer experience exchange;
- isolation reduction;
- forum labor;
- online-to-offline commercial plans.

This prevents a later nostalgic reconstruction such as:

> “old parenting communities were pure mutual aid before commercialization.”

Commercialization was already openly discussed in 2007, and product information/commerce were part of the platform’s planned future.

Likewise, community support did not mean every answer was reliable or every user representative.

---

## 13. Cross-national comparison boundary: WELL is evidence for mechanism, not part of this repo’s object corpus

Howard Rheingold’s account of the WELL Parenting conference records a 1986 incident in which he obtained advice from the online community while his household was waiting for a pediatrician’s callback, and describes a small core of geographically dispersed participants who exchanged parenting information and emotional support.

Source:

- https://www.rheingold.com/vc/book/1.html

This belongs primarily in `how-people-lived`, not in this repository’s Chinese-site corpus.

Its methodological use here is narrow:

- `24/7 peer/expert latency reduction` predates the Web;
- `topic-thread memory` predates Chinese parenting portals;
- online parenting communities can lead to offline relationships;
- small technically privileged communities must not be confused with mass adoption.

So the Chinese late-1990s/2000s material should be compared as one local trajectory of a broader networked-parenting mechanism, not as the global origin.

---

## 14. Candidate claim list for future M1 case work

### Yaolan case candidate

Need to verify:

- original launch host and ownership;
- 1999–2003 at least two captures;
- homepage/category URL structure;
- charset/content-type;
- expert content/Q&A entry;
- community/account surfaces;
- browser assumptions;
- subresource hosts;
- later recollection vs contemporary artifact.

Current status: **identity/history lead exists; verified capture absent in this pass**.

### BabyTree 2007 case candidate

Need to verify:

- March/September 2007 host/URL and platform title;
- homepage vs community vs personal diary URL pattern;
- account/child-profile separation;
- public/private defaults;
- photo host/CDN;
- reply/community structure;
- 2007 and 2009/2010 captures;
- export/memory persistence evidence.

Current status: **strong contemporary use evidence; verified archive capture absent in this pass**.

### Sina Parenting 2009 portal candidate

Need to verify:

- provenance of retained `head/babyYYYYMMDD*.shtml` pages;
- whether they are byte-identical historical files or retrospective renderings;
- historical HTTP/meta charset;
- CSS/JS/image host graph;
- how “往日回顾” selector is generated;
- difference between public portal and logged-in blog/album surfaces.

Current status: **first-party retained dated representation available; Memento status not established**.

---

## 15. Archive attempts and negative evidence log, 2026-09-10

Attempted candidate Wayback replay URLs for:

- `www.babytree.com` around 2007;
- `baby.sina.com.cn` around 2009;
- `www.yaolan.com` around 2001.

The current browser tooling rejected directly constructed `web.archive.org/web/<timestamp>/<original>` URLs as unsafe because the exact archive URLs had not first appeared in search results. No historical response bytes, Memento-Datetime, HTTP status, charset or subresource graph were obtained.

Therefore:

```text
verified historical parenting-site Memento:
NOT ACHIEVED IN THIS SLICE
```

Negative inference prohibited:

- not `Wayback has no snapshot`;
- not `robots blocked it`;
- not `site absent`;
- not `page was static/dynamic`;
- not `charset was GB2312`.

Next pass should first obtain an exact candidate archive locator through an allowed archive index/search path, then open that exact locator and record METHOD §4 fields.

---

## 16. “Verified / probable / unknown” checkpoint

### Verified / directly evidenced enough for narrow claims

- 《父母必读》 institutionally dates its launch to 1980-04 and describes 0–6/pregnancy/health/education scope.
- Yaolan’s later company materials consistently date public launch to 1999-12-15 and describe stage-specific parenting/expert services.
- 2007 Economic Observer preserves contemporary BabyTree user testimony about diary/photo/forum/peer-support use.
- Sina currently retains dated 2009 parenting homepage-review URLs showing stage taxonomy plus expert/forum/blog/album/tool surfaces.

### Probable / strong but not closed

- Chinese parenting Web around 2007–2010 increasingly bundled expert content, peer community, personal memory and commerce.
- child age/pregnancy stage functioned not only as editorial taxonomy but, on some services, likely as account-level routing state.
- platform-hosted family memory created a long-horizon dependence on account and media persistence.

### Unknown / must not be filled by reconstruction

- exact historical DOM and charset of Yaolan 1999–2003;
- exact 2007 BabyTree personal-space privacy defaults;
- proportion of fathers/grandparents vs mothers among active community users;
- whether Sina dated “往日回顾” pages are byte-identical historical originals;
- actual historical recommendation algorithms;
- number of users who read but did not post;
- whether a given archived advice item changed real care behavior;
- export success rate when platforms later changed features;
- amount of child-profile material that remains publicly exposed today.

---

## 17. What this changes about old-Web archaeology

Parenting sites force the repository to distinguish **two different archival ethics** at once:

1. public portal/editorial architecture is a normal historical Web object worth preserving and reconstructing;
2. ordinary children’s growth records are unusually sensitive historical material because the represented person often did not choose publication.

They also expose a preservation inversion:

> **the most socially meaningful thing may be the least archivable thing.**

A parent could receive crucial reassurance in a closed group, then close the browser and never create a public page. Another parent could spend years building a public-looking growth diary whose images later vanish from a CDN. The surviving homepage can therefore tell us what the platform offered, but not how much care actually passed through it.

For the repository’s platform genealogy, this object also connects several forms often treated separately:

```text
portal/editorial taxonomy
→ forum community
→ hosted blog/personal space
→ profile-based social graph
→ lifecycle recommendation
→ commerce
```

A parenting portal is useful precisely because all five can coexist in one late-2000s service rather than appearing as a clean linear evolution.

---

## 18. Source register

### Chinese pre-Web boundary / institutional history

- Beijing Publishing Group, 《父母必读》: https://www.bph.com.cn/guojia/detail/1545.html
  - grade: B institutional retrospective
  - supports: 1980 launch and publication scope

### Yaolan platform history / service self-description

- PR Newswire / Yaolan, 2014: https://www.prnasia.com/story/97380-1.shtml
  - grade: A platform claim at publication time / C for 1999 experience
- PR Newswire / Yaolan expert consultation, 2014: https://www.prnasia.com/story/96280-1.shtml
  - grade: A platform product claim

### BabyTree contemporary evidence

- Economic Observer, 2007-09-05: https://www.eeo.com.cn/2007/0905/82270.shtml
  - grade: B contemporary report + user testimony
  - supports: diary/photo/forum/peer-support practices; founder’s business plans separately tagged as company claims
- Zhejiang Online, 2007-03-13: https://zjnews.zjol.com.cn/system/2007/03/13/008242849.shtml
  - grade: B contemporary feature
  - supports: multiple young mothers using forums for pregnancy/parenting exchange; nonrepresentative sample

### Sina retained historical representations

- 2009-04-28: https://baby.sina.com.cn/head/baby20090428pm.shtml
- 2009-10-28: https://baby.sina.com.cn/head/baby20091028am.shtml
  - grade: A/B first-party retained dated pages
  - supports: observed portal taxonomy/navigation
  - warning: not yet proven Mementos or byte-identical originals

### Overseas mechanism comparator (not corpus item)

- Howard Rheingold, *The Virtual Community*, Chapter 1: https://www.rheingold.com/vc/book/1.html
  - grade: primary retrospective participant account
  - use: network-parenting mechanism before Web; do not generalize to mass U.S. adoption

### Later comparator for information-trust mechanism (outside old-Web main scope)

- Moon et al., JMIR 2019: https://www.jmir.org/2019/7/e14289
  - grade: academic qualitative study
  - use: supports cross-national comparison about immediacy, peer support, information abundance and source verification

---

## 19. Next actionable slice

Highest-value next step is **not** another narrative history. It is capture verification:

1. obtain one exact Yaolan/BabyTree/Sina archive locator through a searchable archive index;
2. record `archive_source`, `capture_url`, `original_url`, `capture_datetime`, HTTP/replay state;
3. inspect charset, title, form actions, scripts and cross-host media;
4. inventory missing subresources;
5. build one minimal historical browser fixture;
6. compare with the 2007/2009 contemporary media representation;
7. keep ordinary child identities out of the fixture.

Until that is achieved, this file remains a research note/state-gap model rather than a completed M1 reconstruction.
