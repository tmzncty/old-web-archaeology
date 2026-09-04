# FORUM / THREAD / GROUP LIFE-SCRIPT VISIBILITY AND TEMPORAL STATE GAPS, 1995–2015

Status: research note / state-gap model  
Scope: 约 1995–2015 中文 BBS、论坛、小组页面中“人生经验帖”的页面状态、线程时间、回复、编辑、成员、传播与线下结果；不把仓库扩展成全球网络史  
Cross-repo companion: `tmzncty/how-people-lived/topics/stranger-life-scripts-forums-peer-advice-and-alternative-life-course-visibility-china-1980-2026.zh-CN.md`

## 0. Why this object matters for old-web archaeology

论坛/BBS/小组不是普通文章页。

一个新闻页面常常可以简化为：

```text
URL
→ HTML
→ assets
→ rendered article
```

一个论坛人生帖至少可能涉及：

```text
platform
→ board/group
→ thread
→ original post
→ edits
→ replies
→ pagination
→ bump/order state
→ quotes
→ deleted replies
→ account profiles
→ attachments/images
→ outbound links
→ cross-posts
→ readers/lurkers
→ private messages
→ offline action
```

因此，旧网档案保存一个“帖子页面”时，最危险的错误是把：

> **页面上今天还能看到的文本**

直接当成：

> **帖子刚发布时的完整历史状态。**

本 note 用两个当前仍存的中文平台 survivor 作为核心例子：

1. 豆瓣“七十年代”小组：页面显示创建于 2005-08-15，但今天同页同时混有 2022 更新的规则和当前讨论；
2. 磨房《迟到的间隔年》：线程显示创建于 2008-01-22，但当前第一帖顶部包含 2009 年出版和 2010 年媒体采访链接。

它们都非常适合说明：

> **live survivor ≠ historical capture**

以及：

> **thread timestamp ≠ page-state timestamp**

---

## 1. Evidence contract

This note follows `docs/METHOD.md`.

### 1.1 Research units

必须分别记录：

- `platform`
- `host`
- `group_or_board`
- `thread`
- `post`
- `reply`
- `account`
- `page_url`
- `capture`
- `current_live_survivor`
- `claim`

不能把“豆瓣”“某小组”“一个帖子”和“今天抓到的一页 HTML”混成同一个对象。

### 1.2 A current live page is evidence of current state

当前可访问页面可以作为：

- current platform artifact；
- 当前页面显示的 metadata；
- 当前仍能跟随的链接；
- 当前 DOM/资源状态；

的高强度证据。

但它**不是**自动的 historical A-grade capture。

例如当前页面显示：

```text
创建于 2005-08-15
```

只能直接证明：

> 2026 当前 survivor page 声称/显示该 group creation metadata。

若没有历史 memento 或同时代独立证据，就不能自动推出：

- 2005 页面也长这样；
- 当前简介文本就是 2005 原文；
- 当前 group type/tag 是 2005 分类；
- 当前成员数是历史成员数；
- 当前热门话题排列是历史排列。

### 1.3 Candidate archive locator is not verified capture

本轮没有取得并实际验证一个足以重建 2005 豆瓣小组首页或 2008 磨房线程原始 DOM 的 Wayback/WARC capture。

因此：

- historical charset；
- original DOM；
- CSS；
- JS；
- form action；
- cookie/session；
- page size；
- browser-specific behavior；
- original image host mapping；

保持 unknown。

这不是缺陷掩盖，而是本仓允许的负结果。

---

## 2. Case A — Douban “七十年代” group as a mixed-time live survivor

Current live URL:
- https://www.douban.com/group/10422/

### 2.1 What the current page visibly contains

当前页面可观察到：

- title: `七十年代`
- group creation metadata: `2005-08-15`
- group type shown today: `生活`
- current description text；
- a list labelled as historical/popular topics, including questions around maturity, single women at age thirty, marriage, etc.;
- community rules explicitly labelled `2022-01-24 更新`；
- current/recent discussion table；
- current member count and current related groups；
- current site navigation, app promotion and modern footer.

Current platform artifact:
- https://www.douban.com/group/10422/

### 2.2 The page contains multiple clocks at once

It must not be assigned one date.

A useful decomposition is:

```text
group_created_at = 2005-08-15 (displayed metadata)

description_state_at = unknown

historical_topic_created_at = per-thread state, not group homepage state

rules_updated_at = 2022-01-24

recent_discussion_state_at = current render time

current_member_count_at = current render time

page_rendered_at = current access time
```

This is **page-time stratification**.

### 2.3 creation metadata gap

`group_created_at` does not establish:

- exact public launch datetime;
- whether group was immediately visible to all users;
- whether current group title was unchanged;
- whether current description existed at creation;
- whether current URL pattern existed exactly in current form.

### 2.4 description-edit gap

A current description can contain old-looking prose without an exposed edit timestamp.

Therefore:

```text
current description text
≠
2005 original description text
```

unless archive evidence independently establishes continuity.

### 2.5 topic-list curation gap

A group homepage can show “热门话题” links that were selected or edited later.

The list proves current curation state, not historical ranking state.

### 2.6 rules-time gap

The 2022 rules on a group created in 2005 are an unusually clear demonstration:

> **the current page is a composite of historical identity metadata and later governance state.**

Any screenshot labelled simply “2005 Douban group page” would be false if made from today’s live page.

---

## 3. Case B — Mofang “迟到的间隔年” as a surviving edited thread

Current live URL:
- https://www.doyouhike.net/topic/279778

Independent near-contemporary report:
- https://www.chinadaily.com.cn/hqpl/2010-03/30/content_9675381.htm

Later 2013 media ecology report:
- https://zqb.cyol.com/html/2013-05/28/nw.D110000zgqnb_20130528_7-03.htm

### 3.1 What the current live page visibly establishes

Current page shows:

- forum/category `异域之旅`；
- displayed topic datetime `2008-01-22 01:57`；
- original author account label；
- many follow-up posts carrying granular 2008 timestamps；
- a long travel narrative；
- images now served through current CDN and, in some positions, links associated with `laiba.tianya.cn`；
- current site navigation/footer.

### 3.2 The first post proves that displayed creation time is not enough

Current first-post area also contains links to:

- the later book page；
- later book-sale pages；
- media reviews/interviews dated 2009；
- a China Radio International interview dated 2010.

Therefore the current first-post text cannot be treated as a byte-equivalent 2008-01-22 original.

This is one of the strongest concrete examples of:

> **post-created-at / post-edited-at divergence.**

### 3.3 Thread-time stratification

A thread should carry at least these clocks when evidence permits:

```text
thread_created_at
post_created_at
post_last_edited_at
reply_created_at
reply_last_edited_at
thread_last_bumped_at
page_archive_capture_at
current_page_render_at
resource_fetch_at
```

If `post_last_edited_at` is unavailable, do not silently set it equal to `post_created_at`.

### 3.4 Current survivor claim boundary

The current live survivor supports:

- the platform currently presents the thread as originating in Jan 2008；
- granular historical-looking post timestamps survive；
- the narrative currently contains later-added reference links；
- some historical resource lineage crosses host boundaries.

It does **not** by itself establish:

- 2008 DOM；
- 2008 page order exactly；
- 2008 images exactly；
- 2008 charset；
- whether every surviving sentence was present in 2008；
- deleted posts/replies；
- 2008 read count；
- 2008 ranking position；
- the exact Tianya cross-post state.

---

## 4. Core state chain for forum life-story research

For a thread about a life choice, use this chain:

```text
platform exists
→ board/group exists
→ thread URL exists
→ author account exists
→ original post submitted
→ post accepted/published
→ post enters list/ranking state
→ readers can access page
→ reader actually opens
→ reader interprets
→ reader replies / bookmarks / cross-posts / sends PM / does nothing
→ thread is edited or bumped
→ derivative copies appear elsewhere
→ reader may act offline
→ offline outcome may later be reported
```

The public page is mostly evidence around the middle of this chain.

The two ends are often darkest:

- exact author/account/private state before publishing；
- actual reader life outcome after reading.

---

## 5. New archive/state gaps

### 5.1 live-survivor / historical-capture gap

A current page that displays a 2005 or 2008 date is not the same thing as a capture made in 2005 or 2008.

Record separately:

```yaml
artifact_type: current_live_survivor | historical_capture | screenshot | derivative_copy
page_displayed_historical_datetime:
artifact_observed_datetime:
archive_capture_datetime:
```

Never collapse them.

### 5.2 post-edit-history gap

If a post has later material but no visible edit history:

```text
current post body
→ historical text lineage unknown
```

The exact version at any earlier date cannot be reconstructed confidently.

### 5.3 description-edit-history gap

Group descriptions are often long-lived control text but may be edited repeatedly.

Current description cannot be assigned to group creation date without evidence.

### 5.4 reply-pagination gap

A crawler/archive may save page 1 but miss:

- page 2+；
- “load more” replies；
- nested replies；
- reply API responses.

Therefore:

```text
thread capture exists
≠
full discussion captured
```

### 5.5 deleted-reply gap

A conversation can lose a reply while later replies still refer to it.

### 5.6 quote-orphan gap

A quoted fragment may survive after original content is deleted.

The quote proves somebody later displayed that fragment, not automatically the full original post state.

### 5.7 bump/order gap

Old forums often ordered visibility by:

- latest reply；
- manual top/pin；
- board rules；
- hotness；
- administrator curation.

A capture of a thread does not tell us where it ranked ten minutes earlier or how many people encountered it through board ordering.

### 5.8 board-index gap

A thread URL may survive while the board index/list state that made it discoverable is gone.

Thus:

```text
content survival
≠
discoverability survival
```

This matters directly to life-history interpretation.

### 5.9 search-index gap

A post existing on a platform does not prove it was searchable at the time.

Need separate evidence for:

- site search；
- search-engine indexing；
- tags/categories；
- internal recommendations.

### 5.10 member / reader / poster gap

A group member count is not a count of:

- active readers；
- unique humans；
- posters；
- people who agreed with group framing；
- people who acted offline.

Maintain:

```text
registered_member
≠ active_member
≠ reader
≠ poster
≠ planner
≠ offline_actor
```

### 5.11 lurker invisibility gap

Readers who never reply are usually absent from public archival traces.

A 1997 Usenet study explicitly warned about this analytical distinction; for Chinese old-web work this is a methodological comparator, not an expansion of repository scope.

Comparator:
- https://academic.oup.com/jcmc/article/2/4/JCMC242/4584382

### 5.12 bookmark/favorite gap

Favorites/bookmarks may be:

- private；
- account-only；
- deleted when service shuts down；
- not archived.

Yet long-latency influence may operate through exactly this state.

### 5.13 PM / off-platform handoff gap

Forum participants may continue through:

- private message；
- email；
- QQ；
- phone；
- later WeChat；
- offline meeting.

Public thread archives rarely preserve this handoff.

### 5.14 offline-outcome gap

A post saying “I want to resign/travel/study again” does not prove the action occurred.

Likewise a later success story may omit failed attempts or changed plans.

### 5.15 cross-post lineage gap

The same narrative may exist as:

```text
Mofang thread
→ Tianya cross-post
→ personal blog
→ book
→ media interview
→ encyclopedia entry
```

These are derivatives with different edit histories.

Do not merge them into one “original text”.

### 5.16 derivative-amplification gap

A later book or news feature can make the original thread appear historically more central than it actually was at publication time.

Record derivative success separately from original visibility.

### 5.17 resource-host gap

A thread may survive while images depend on:

- another forum；
- image host；
- CDN migration；
- rewritten asset URLs.

The current Mofang survivor visibly includes resource lineage crossing host boundaries.

Therefore main HTML survival cannot establish original image survival.

### 5.18 CDN-remapping gap

Today’s page may load a migrated image from a new CDN while giving no evidence that this was the historical 2008 delivery path.

### 5.19 account-continuity gap

Same username/avatar display does not prove:

- account has never changed owner；
- platform account IDs never migrated；
- profile fields are historical；
- account still controlled by original person.

### 5.20 moderation-state gap

Deleted, hidden, locked, moved, pinned and merged states may not be captured.

Current surviving discourse is partly the result of moderation history.

### 5.21 category-taxonomy gap

Current category names/tags can differ from historical taxonomy.

Do not backfill modern categories onto old posts without archive evidence.

### 5.22 platform-governance-time gap

Current rules can coexist on a 2005-created group page.

Rules must carry their own date/version, not inherit group creation date.

### 5.23 popularity-metric gap

Current reply/member/view counts may be cumulative, recomputed, migrated or unavailable historically.

A modern metric cannot be inserted into a historical 2008 snapshot narrative without its measurement date.

### 5.24 group-label / social-prevalence gap

The existence of a group named around an unusual life choice proves that the label/platform object existed.

It does not prove the behavior was socially common.

### 5.25 story / representativeness gap

The most memorable long-form thread may be exceptional precisely because it is unusually coherent, dramatic or successful.

### 5.26 visibility / feasibility gap

A user can read a detailed life story while lacking:

- money；
- housing；
- job fallback；
- passport/visa；
- family support；
- time；
- health；
- institutional eligibility.

A thread increases visibility, not automatically feasibility.

---

## 6. State model for life-script discoverability

To reconstruct whether an old thread could plausibly function as a discoverable “life script”, ask:

```text
thread existed
→ board/group was accessible to this user class
→ user had Internet/terminal/account access
→ thread was visible in board/search/link graph
→ page rendered in historical browser environment
→ user could read text/encoding/assets
→ user actually encountered it
→ user understood the category/label
→ user could access replies or follow-ups
→ user could distinguish current vs outdated advice
→ user had resources to evaluate/act
```

Archive evidence typically proves only some left-hand states.

It almost never proves the right-hand behavioral sequence.

---

## 7. Why forum archaeology matters to “ordinary life” history

A public forum page can preserve something newspapers often do not:

- uncertainty before action；
- first plan；
- objections from strangers；
- failed steps；
- corrections；
- costs；
- later update；
- disagreement among peers.

That makes threads unusually valuable life-history sources.

But exactly because the record is interactive, it is also unusually vulnerable to state loss.

The archaeologist should not ask only:

> “Did the HTML survive?”

Also ask:

> “Did the conversation topology survive?”

---

## 8. Current survivor examples and what each actually proves

| Artifact | Strong claim supported | Claim not supported |
|---|---|---|
| Current Douban “七十年代” group | current page displays creation date 2005-08-15 and old-topic links alongside later rules/current discussion | 2005 homepage looked like current page |
| Current Mofang “迟到的间隔年” | current survivor displays Jan 2008 thread/post timestamps and later-added links | current post body is exact Jan 2008 version |
| 2010 China Daily report | by 2010 the 2008 post was remembered/reported as hot on Mofang/Tianya and linked to later book diffusion | exact 2008 view count or ranking |
| 2013 China Youth report | by 2013 gap-year groups/threads were a visible online ecology | members all practiced gap years |
| 1995 CERNET history | campus BBS infrastructure began emerging in 1995 | mass Chinese youth forum adoption in 1995 |

Sources:
- https://www.douban.com/group/10422/
- https://www.doyouhike.net/topic/279778
- https://www.chinadaily.com.cn/hqpl/2010-03/30/content_9675381.htm
- https://zqb.cyol.com/html/2013-05/28/nw.D110000zgqnb_20130528_7-03.htm
- https://www.edu.cn/tsfzlc_12719/20141105/t20141105_1199004.shtml

---

## 9. Evidence grades for this note

### A-current / current platform artifact

Current live Douban and Mofang pages.

Use them for:

- current survivor state；
- visible metadata；
- current link/resource topology；
- proof that multiple historical clocks coexist on one current page.

Do **not** relabel them A-historical capture.

### A/B institutional or contemporary historical evidence

- CERNET institutional chronology for 1995 BBS infrastructure;
- 2010 contemporaneous-ish independent media confirming diffusion of the 2008 Mofang/Tianya story;
- 2013 China Youth reporting for then-current group ecology.

### D

All named gap categories and state chains in this document are researcher abstractions.

---

## 10. What is specifically unknown

For Douban 2005 group:

- original 2005 homepage HTML；
- original charset/header behavior；
- historical member count；
- historical description version；
- historical topic order；
- old CSS/JS/browser assumptions；
- whether current old-topic links were already curated in 2005.

For Mofang 2008 thread:

- original Jan 2008 first-post byte sequence；
- original first-post edit timestamps；
- historical view/rank trajectory；
- original image availability；
- deleted replies；
- exact Tianya cross-post chronology；
- whether current CDN assets are faithful migrations；
- original page DOM/browser behavior.

These unknowns should stay visible in future case work.

---

## 11. Privacy boundary

This object is especially likely to involve ordinary people describing:

- relationships；
- family conflict；
- unemployment；
- income；
- health；
- migration；
- identity details.

Repository rule:

> **study platform structure and thread state with minimum personal re-publication.**

Therefore:

- do not bulk copy old user profiles；
- do not republish deleted posts simply because an archive has them；
- avoid unnecessary names/user IDs；
- prefer abstract URL patterns and aggregate state；
- do not infer today’s identity from old usernames/contact data；
- do not contact ordinary users merely to verify an old page.

---

## 12. Browser / encoding boundary

The current survivor proves nothing about historical browser fidelity.

Potential historical variables include:

- GB2312 / GBK / UTF-8；
- IE-specific JS/layout；
- table layout；
- image hotlink behavior；
- login/session gates；
- pagination forms；
- AJAX introduced later；
- archive URL rewriting.

Until a verified historical capture is obtained and tested, keep these unknown.

---

## 13. Cross-repo interpretation boundary

This repository should not answer the full question:

> “How did strangers’ stories change Chinese life choices from 1980 to 2026?”

That belongs to `how-people-lived`.

This repository’s narrower contribution is:

> **When a life story appears to survive on the old Web, which technical and temporal states actually survive, and which parts of its social influence are invisible?**

That preserves the old-web scope.

---

## 14. New methodological conclusion: pages preserve stories better than encounter history

A forum thread may preserve a narrative for twenty years.

But the archive often cannot reconstruct:

- who saw it at the time；
- through which board/index/search route；
- whether it was on page 1 or page 200；
- which replies had already appeared；
- whether author edited it after publicity；
- which reader bookmarked it；
- who later acted because of it.

Therefore:

> **story survival ≠ encounter-history survival**

This is a new archive-gap class that should later feed Phase 5 archive-gap modeling.

---

## 15. Another methodological conclusion: the more successful the story, the more version control matters

A thread that becomes:

```text
hot post
→ cross-post
→ blog
→ newspaper feature
→ book
→ encyclopedia entry
```

is not easier to reconstruct just because more copies exist.

It may become harder, because later copies:

- edit chronology；
- compress failures；
- add retrospective meaning；
- append purchase/interview links；
- merge variants；
- change image hosting.

So derivative abundance can produce **version ambiguity**.

For historically influential forum narratives, version provenance should be treated almost like software history.

---

## 16. Proposed evidence fields for future schema work

This note suggests adding/retaining fields such as:

```yaml
artifact_type:
platform:
host:
group_or_board:
thread_url:
post_id:
account_id_or_minimized_label:
page_displayed_created_at:
page_displayed_edited_at:
archive_capture_datetime:
current_observed_at:
current_live_survivor: true|false
historical_capture_verified: true|false
pagination_state:
reply_count_observed:
member_count_observed:
member_count_as_of:
resource_hosts:
cross_post_candidates:
current_description_state:
moderation_state:
known_deleted_state:
browser_assumption:
charset_observed:
lineage_notes:
privacy_minimization:
claim_scope:
evidence_grade:
confidence:
```

Important: fields such as `member_count_observed` need their own `as_of` date.

---

## 17. Stop condition for this slice

Do not attempt a “pixel-perfect 2005 Douban” or “pixel-perfect Jan 2008 Mofang” reconstruction until a verified historical capture is available.

Current evidence is sufficient for a strong **state-gap research note**, but not for historical browser reconstruction.

A future upgrade should require at least one of:

1. verified Wayback/WARC capture from the relevant historical window;
2. independently preserved original HTML/screenshots with provenance;
3. platform documentation identifying edit timestamps/legacy rendering;
4. a second archival family confirming the same page state.

Until then:

> **unknown stays unknown.**

---

## 18. What this changes in old-web archaeology

This slice adds a category that earlier page-centric notes do not fully capture:

> **a surviving old thread is a time-layered social object, not a static document.**

The central preservation questions become:

```text
Which version of the post survived?
Which replies survived?
Which ordering state survived?
Which resource hosts survived?
Which governance layer is historical?
Which metadata is current?
Which readers never left a trace?
Which offline outcomes happened outside the platform?
```

That is the technical counterpart to the life-history finding in `how-people-lived`:

> strangers’ life stories can expand the visible future set, while the archive preserves the story far better than it preserves who encountered it or what they eventually did.
