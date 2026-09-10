# NEWS REPOST / SOURCE LINEAGE / PUBLICATION TIME / CONTEMPORARY VOICE GAPS, 1998–2015

Status: method note / cross-repo evidence protocol  
Scope: 约 1998–2015 中文新闻门户、媒体网站、转载页、移动版 survivor 在普通生活史第一人称材料中的证据边界；不扩展成新闻业史  
Cross-repo companion: `tmzncty/how-people-lived/sources/contemporary-future-imagination-lock-in-optionality-samples-2006-2025.zh-CN.md`

## 0. Why this note exists

`how-people-lived` 需要大量 2007–2010 同时代普通人自述。

现实中，很多早期报刊/杂志采访今天不是通过原始媒体站点存活，而是以：

```text
original newspaper/magazine
→ portal republication
→ mobile rewrite
→ search index
→ current live survivor
```

的形式留下。

如果不单独建模 source lineage，就很容易出现两个相反错误：

1. 因为原始 URL 已失效，就把仍然很有价值的同期采访全部降成“后来回忆”；
2. 因为新浪/搜狐/凤凰今天还能打开一个 2008 页面，就把它误称为“2008 年已核验历史网页快照”。

本 note 的核心目标是把：

- **话是什么时候说的**；
- **记者什么时候写的**；
- **原媒体什么时候发布**；
- **门户什么时候转载**；
- **页面今天什么时候被观察**；
- **archive 什么时候真正抓取**；

分开。

---

## 1. Research unit

至少拆成：

```text
real-world interview/event
→ reporter notes / recording
→ editorial article version
→ original publisher
→ syndication / licensed republication
→ portal article record
→ desktop URL
→ mobile URL
→ later template migration
→ current live survivor
→ search-engine copy/snippet
→ historical archive capture (if any)
→ research claim
```

这些对象不能合并。

特别是：

```text
original publisher
≠ current surviving host
```

以及：

```text
article publication time
≠ page observation time
≠ archive capture time
≠ interview/event time
```

---

## 2. Minimum time provenance fields

使用一条新闻转载材料时，建议至少记录：

```yaml
claimed_original_publisher:
current_surviving_host:
current_url:
headline_current:
byline_current:
source_line_current:
page_displayed_publication_datetime:
interview_or_event_datetime:
  value:
  precision: exact | day | month | inferred-range | unknown
original_url:
  value:
  status: verified | candidate | unknown
republication_datetime:
  value:
  status: explicit | inferred | unknown
current_observed_datetime:
historical_capture:
  url:
  capture_datetime:
  status: verified | locator-only | not-checked | blocked
article_version_relation:
  exact-copy | near-copy | edited-repost | mobile-render | unknown
```

如果页面没有给出某个字段，写 `unknown`，不要把另一个时间填进去。

---

## 3. Core state gaps

### 3.1 interview-time / publication-time gap

一个 2008-05-09 发布的采访，谈话可能发生在几天或数周以前。

因此：

```text
published_at = 2008-05-09
```

不能自动变成：

```text
speaker said this exactly on 2008-05-09
```

如果正文只给“4 月 26 日下午”这种事件锚点，可以把部分现场采访时间缩窄；其余仍保持未知。

### 3.2 original-publication / portal-republication gap

新浪、凤凰、搜狐等门户长期承载报刊和杂志内容。

当前 portal survivor 可以很好地支持：

- 当前页面显示的来源行；
- 当前保存的正文；
- 当前显示的历史发布时间；

但不能仅凭它证明：

- 原媒体当日网页 DOM；
- 原媒体精确发布时间；
- 原媒体标题完全相同；
- 原媒体分页、图片、评论、相关链接完全相同。

### 3.3 republication-time / original-publication-time gap

门户可能：

- 同日转载；
- 次日转载；
- 延迟转载；
- 重新编辑旧稿；
- 在数据库迁移时重建页面。

如果只有当前门户页的 timestamp，应称：

> `page-displayed publication datetime`

而不是在没有来源链证据时直接称 `original publication datetime`。

### 3.4 current-live-survivor / historical-capture gap

一个今天仍能打开、页面上写着 `2008年01月11日` 的 URL：

```text
current live survivor displaying a historical publication date
```

不等于：

```text
capture made on 2008-01-11
```

历史 DOM、charset、CSS、广告、分页、图片 host、脚本和导航都需要 historical capture 才能重建。

### 3.5 displayed-timestamp / record-creation-time gap

CMS 迁移可能保留旧日期，也可能重新生成：

- mobile page；
- AMP-like page；
- print page；
- app share page；
- structured-data timestamp。

因此一个旧 timestamp 是**内容时间线线索**，不是自动的服务器对象出生证明。

### 3.6 quote-survival / recording-survival gap

新闻正文中的直接引语是同期文本证据，但通常不是原始音频逐字稿。

应写：

```text
article attributes this statement to speaker X
```

而不是：

```text
the surviving webpage proves every spoken word byte-for-byte
```

除非原始录音/采访实录另外存在。

### 3.7 same-copy / independent-evidence gap

同一篇稿件同时出现在：

- 新浪；
- 凤凰；
- 搜狐；
- 地方门户；

不构成四个独立 evidence families。

若来源行、记者、段落顺序和关键文本相同，应先按一个 syndication family 处理。

### 3.8 headline / body lineage gap

转载门户经常重写标题。

因此：

```text
same article body
≠ same headline framing
```

标题适合研究门户如何包装内容；正文更适合研究原采访事实。二者需要分别定来源。

### 3.9 desktop / mobile page gap

老门户今天可能只剩：

- 桌面旧 URL；
- 移动重写 URL；
- 两者之一；
- 自动跳转后的现代模板。

`desktop survivor` 与 `mobile survivor` 应视为不同 page objects，即使共用 article ID。

### 3.10 pagination gap

旧长文可能拆成多页。

只保存第一页可能丢掉：

- 后续人物；
- 结论；
- 数据来源；
- 专家评论；
- 反例。

因此：

```text
article URL survives
≠ full article state survives
```

### 3.11 image/caption gap

今天正文文字仍在，不代表：

- 原照片仍在；
- 原图注仍在；
- 图序未变化；
- 图片是当年同一个 asset。

图片/CDN 必须另建 lineage。

### 3.12 source-line / rights-line gap

当前页面标注“来源：中国青年报”“来源：中国新闻周刊”等，是重要 lineage evidence。

但来源行也属于当前 survivor state；如要证明 2006/2008 当日门户就以同样方式展示，仍需 historical capture。

### 3.13 comment-time gap

今天看到的评论区：

- 可能已经关闭；
- 可能迁移；
- 可能只剩计数；
- 可能混入多年后的评论。

不能把 article publication time 继承给所有评论。

### 3.14 search-snippet / page-state gap

搜索引擎 snippet 只能证明索引系统当前显示某段文本。

它不能证明：

- 完整页面正文；
- 原页面 DOM；
- 发布时间字段可靠性；
- 转载关系；
- 历史可见性。

---

## 4. Case A — 2006 China Youth Daily anxiety article surviving on Sina mobile

Current survivor:

- https://news.sina.cn/sa/2006-12-04/detail-ikknscsk1400390.d.html

Current observable metadata includes:

- headline: `相比五年前47.8％的人“更焦虑了”`；
- displayed date: 2006-12-04；
- source/identity display pointing to《中国青年报》；
- reporter name；
- survey method paragraph；
- several attributed contemporary first-person statements。

For life-history research this is valuable because one respondent explicitly converts buying a home into a five-year job-mobility tradeoff.

Correct evidence statement:

> A currently surviving Sina mobile page preserves a China Youth Daily-attributed article displaying a 2006-12-04 publication date and contemporary attributed interview material.

Do **not** silently upgrade it to:

> verified 2006 China Youth Daily Web capture.

Unknown without further archive work:

- original CYOL URL；
- original CYOL DOM/template；
- original charset；
- whether Sina desktop and mobile variants existed in current form in 2006；
- exact interview date for every quoted respondent；
- historical reader comments / rankings / inbound links。

Evidence family: **one journalistic/survey family**, not independent proof from every later repost.

---

## 5. Case B — 2008 China Newsweek housing interview surviving on Sina

Current survivor:

- https://news.sina.com.cn/c/2008-01-11/115914721370.shtml

Current observable metadata includes:

- displayed date: 2008-01-11；
- source line naming《中国新闻周刊》；
- reporter attribution；
- detailed contemporary interview with a 26-year-old Beijing IT worker；
- mortgage amount, income, monthly payment, parental down-payment support and then-current expectations about housing prices。

This is strong **contemporary first-person evidence of perceived constraints**.

It is not by itself evidence that:

- every Beijing 26-year-old shared the view；
- the prediction about future prices was objectively correct；
- the surviving Sina HTML equals the byte-level 2008 render；
- the article’s quoted speech is an untouched audio transcript。

This distinction is especially important for “future imagination” research: what matters is what the speaker **could reasonably believe then**, not whether later history vindicated the belief.

---

## 6. Case C — one 2008 Nanfeng Chuang story, multiple surviving carriers

Current Sina survivor:

- https://news.sina.com.cn/c/2008-05-09/173015508922.shtml

Current Phoenix derivative/survivor:

- https://news.ifeng.com/society/5/200805/0511_2579_532965_1.shtml

Both preserve material from the same Nanfeng Chuang reporting around young university graduates returning to rural posts.

The Sina text contains a very useful explicit temporal decision: one graduate treats the three-year post as a bounded experiment and accepts leaving afterward if it does not fit.

But the existence of Sina + Phoenix copies does **not** mean two independent field interviews confirm the same quote.

Record as:

```yaml
evidence_family: Nanfeng Chuang original reporting
carrier_1: Sina survivor
carrier_2: Phoenix survivor/derivative
independent_confirmation_count: 1 unless another reporting family is found
```

This is the **syndication multiplicity trap**.

---

## 7. Contemporary voice protocol for `how-people-lived`

For every candidate “2008 people thought X” claim, record a row like:

| field | value |
|---|---|
| speaker / population | named, pseudonymous, anonymous, survey sample |
| life stage | student, graduate, worker, parent, retiree, etc. |
| statement type | current state / explicit future plan / fear / aspiration / retrospective account |
| spoken/event time | exact / bounded / unknown |
| publication time | explicit / inferred |
| current carrier | URL + host |
| original publisher | verified / attributed / unknown |
| original URL | verified / candidate / unknown |
| archive status | M1 verified / locator-only / current survivor only |
| later edit risk | low / medium / high / unknown |
| representativeness | case / convenience survey / probability survey / unknown |
| independent confirmation | yes / no / derivative only |
| claim allowed | narrow sentence only |

This prevents a very common collapse:

```text
one dramatic 2008 story
→ “2008 youth believed ...”
```

The correct chain is:

```text
this person said / was reported as saying X at this time
→ similar claims appear across independent people / sources
→ distribution evidence supports wider prevalence
→ only then consider period-level synthesis
```

---

## 8. A dedicated `contemporaneity` grade

Evidence grade A/B/C/D in this repository describes source relationship and reconstruction strength. For life-history work it is useful to add a separate orthogonal time label:

```text
T0 = direct artifact created by speaker at the time (post/blog/profile/letter)
T1 = same-period interview/report quoting speaker
T2 = near-period retrospective account (months to a few years)
T3 = late retrospective memory
TX = temporal relation unclear
```

Examples:

- a 2008 first-person blog post about plans: `T0`；
- a 2008 magazine interview asking plans: `T1`；
- a 2010 interview about a 2008 decision: `T2`；
- a 2025 nostalgia article recalling 2008: `T3`。

Do not collapse `T0/T1` into “more true” and `T3` into “false”.

They answer different questions:

- `T0/T1` are strongest for **what future was imaginable then**；
- `T2/T3` can be strong for **what actually happened later and how memory reorganized the past**。

---

## 9. First-person / platform-fact / media-reconstruction separation

A single current news page can support three different claim types:

### P — attributed person statement

Example form:

> the article reports that interviewee X planned / feared / preferred Y.

### O — observable page fact

Example form:

> the current survivor displays date D and source line S.

### M — media framing

Example form:

> the article headline/editorial framing groups these cases as “80后房奴”, “返乡知识青年”, etc.

These must not be merged.

In particular:

```text
media label
≠ self-identity
```

and:

```text
headline theme
≠ frequency in population
```

---

## 10. Archive-specific bias in future-imagination research

### 10.1 dramatic-future survival bias

A person saying:

> “I will quit, travel around Asia, start a company, buy a house immediately.”

is more likely to become a feature story than someone saying:

> “I expect to keep my current job and maybe save a little more.”

Thus archive survival will overrepresent unusual plans.

### 10.2 fulfilled-dream recirculation bias

If someone later became famous or succeeded, old statements are more likely to be rediscovered and republished.

This makes the past appear more full of people who “already knew where they were going”.

### 10.3 failed-plan disappearance bias

A plan that quietly failed may leave only:

- an old post；
- no follow-up；
- dead images；
- deleted account。

The successful path often has many later derivatives.

### 10.4 editorial-cohort bias

Media series titled around “80后”“90后” actively select people who fit or challenge a cohort frame.

This is useful evidence of **what the media thought was generationally legible**, not an unbiased sample of the cohort.

### 10.5 current-search ranking bias

Searching today for `2008 梦想 未来` preferentially returns pages that:

- remain indexed；
- have strong SEO/domain authority；
- were later linked；
- contain today’s search vocabulary。

Absence from search is not absence from 2008 discourse.

---

## 11. M1 archive status in this slice

This run used current live/surviving portal pages and did **not** obtain a historical memento satisfying the repository’s M1 contract for the three cases above.

Specifically, no case in this slice was verified with the full combination of:

```text
original URL
+ capture URL
+ capture datetime
+ HTTP status
+ redirect behavior
+ historical DOM
+ charset
+ subresource notes
+ comparison to a second historical time point
```

Therefore:

**M1 verified historical capture for these news/repost cases: NOT ACHIEVED IN THIS SLICE.**

This means only “not verified here”. It does **not** mean an archive copy does not exist.

---

## 12. What this changes for old-web archaeology

The key addition is **carrier lineage**.

Old-Web work often asks whether an old page survived. For ordinary-life history, a second question is just as important:

> **Did the voice survive on its original page, or only after being carried into another platform’s database?**

A dead newspaper site plus a surviving portal repost can preserve valuable 2006/2008 testimony while destroying almost all evidence about the original reading environment.

So preservation has at least two distinct success states:

```text
semantic survival   = enough text/source/date survives to support a narrow historical claim
interface survival  = enough original page/template/assets survives to reconstruct how users encountered it
```

They can diverge sharply.

For `how-people-lived`, semantic survival may be sufficient for a carefully bounded first-person claim.

For `old-web-archaeology`, interface survival requires much more evidence.

That distinction lets the two repositories share evidence without silently lowering either repository’s standard.