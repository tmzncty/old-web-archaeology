# Sina / Sohu 2007–2010 intergenerational-support story probe

## Why this object belongs in Old Web Archaeology

This is not a general study of elder care. The life-history synthesis belongs in `tmzncty/how-people-lived`:

- https://github.com/tmzncty/how-people-lived/blob/main/topics/intergenerational-support-overlap-flow-reversal-and-multigenerational-horizons-china-1989-2024.zh-CN.md

The old-Web question is narrower:

> **When a 2007 online discussion survives today mainly through portal-news syndication, what exactly has survived: the original user material, a contemporary journalistic reconstruction, or only a later delivery shell containing old text?**

Two currently discoverable pages are useful for this problem:

1. Sina News, 2007-12-20: `陕西80后网友晒赡养账单 六成人没钱照顾老人`
2. Sohu News, 2010-11-18: `80后赡养父母力不从心 未来中国老人赡养成难题`

The second page recirculates substantial facts and framing from the first story while combining them with newer surveys/interviews.

This produces a preservation problem that differs from a clean forum capture.

---

## 1. Object A — Sina News, 2007-12-20

### Current discoverable URL

- Original/live URL: `https://news.sina.com.cn/s/2007-12-20/093113113590s.shtml`
- Page title: `陕西80后网友晒赡养账单 六成人没钱照顾老人`
- Displayed publication time: `2007年12月20日09:31`
- Displayed upstream/source label near the top: `国际在线`
- Body ending/source note visible in indexed text: `来源：综合`
- Reporter named in body: `王晓亮`

Current indexed result:

- https://news.sina.com.cn/s/2007-12-20/093113113590s.shtml

### What the surviving text says

The article says that young adults born in the 1980s were posting and discussing estimated elder-support budgets online. It reports:

- a small online questionnaire of more than 120 `80后` respondents;
- some respondents regularly sending money home;
- some saying their income only covered themselves;
- some still receiving parental support;
- several named interviewees calculating mortgage, household, child-education and parent-support costs;
- one named young worker described as having posted online about wanting to support his parents but lacking money.

For ordinary-life history, this is valuable contemporaneous evidence that elder-support responsibility was already being **made calculable and publicly discussable online** in 2007.

But the archaeology must not silently promote it into a forum artifact.

---

## 2. The source chain is not one page

The page compresses several different evidence objects:

```text
unknown original forum/post(s)
        ↓
small online questionnaire / reporter interviews
        ↓
reporter-selected narrative and household budgets
        ↓
upstream news publication / syndication chain
        ↓
Sina portal copy at a stable-looking 2007 URL
        ↓
2026 search-index retrieval of the surviving text
```

The current page tells us that an online post existed and quotes/paraphrases it.

It does **not** currently give us, in a verified way:

- original forum/platform name;
- original thread URL;
- original post ID;
- exact posting datetime;
- whether the quoted wording is complete;
- surrounding replies;
- username/account metadata;
- edit/deletion state;
- page layout of the original post.

Therefore:

> `contemporaneous report of a forum post != preserved forum post`

This matters because later researchers can easily mistake a portal article about “网友说” for direct platform evidence.

---

## 3. Object B — Sohu News, 2010-11-18

### Current discoverable URL

- Original/live URL: `https://news.sohu.com/20101118/n277713972.shtml`
- Page title: `80后赡养父母力不从心 未来中国老人赡养成难题`
- Displayed publication time: `2010年11月18日05:28`
- Displayed source label: `人民网`

Current indexed result:

- https://news.sohu.com/20101118/n277713972.shtml

### Why this is a second preservation state, not an independent confirmation

The 2010 Sohu page includes a section reproducing the same 2007 `陕西80后网友晒赡养账单` figures and framing:

- the annual estimated elder-support bills by city;
- the 120+ respondent online questionnaire;
- four-tenths / four-tenths / two-tenths support-capacity split;
- the claim that many young adults felt unable to meet all expected support items.

It then places this older material beside newer 2010 survey/interview material.

This is historically interesting because the 2007 online story became a reusable evidence block in later portal coverage.

But it creates a classic independence error:

> `same figures on two portals in two years != two independent observations`

The 2010 page is partly a recirculation of the 2007 media story.

The correct historical object is a **syndication lineage**, not a pile of corroborating sources.

---

## 4. New preservation mechanism: `live-origin content survival`

These pages add a preservation state that does not fit a simple `Wayback capture / no capture` binary.

### Definition

`live-origin content survival` means:

> an old document's text, publication date and original-looking URL remain discoverable on the publisher/portal's live domain years later, even though the historical delivery environment has not been verified.

This can preserve useful content while destroying or replacing many interface-level properties.

### What it may preserve

For the 2007 Sina page, current discovery preserves at least:

- URL path;
- title;
- displayed publication datetime;
- source labels;
- reporter name;
- article body text as currently indexed;
- the article's claims about online posts, questionnaire results and interviews.

### What it does not prove

Current live survival does **not** by itself prove the 2007 state of:

- HTTP headers;
- Content-Type;
- charset declaration;
- HTML DOM;
- table/frame layout;
- CSS;
- JavaScript;
- image assets;
- comments;
- related-link modules;
- ad slots;
- browser assumptions;
- page width/viewport behavior;
- whether the present HTML shell is a later migration.

Therefore:

> `old text at old URL in 2026 != verified 2007 webpage interface`

This is a distinct state from a Wayback capture with an explicit 2007 capture datetime.

---

## 5. New archive asymmetry: `content continuity / interface discontinuity`

A portal can preserve the semantic payload of an article while continuously replacing the machinery around it.

That creates an asymmetry:

```text
headline / body / displayed date        may survive
historical DOM / CSS / ads / JS         may not
original comment state                  may not
upstream linked forum thread            may not
historical browser behavior             unknown
```

A modern search engine may therefore make a 2007 article look unusually complete even when only the text lineage is stable.

For Old Web Archaeology, **content survival and interface survival must be separate fields**.

Suggested future schema fields:

```yaml
content_survival: current-live-original-url
historical_interface_verified: false
historical_capture_opened: false
underlying_user_artifact_verified: false
syndication_lineage_known: partial
```

---

## 6. Another bias: `source-chain compression`

The Sina page collapses several source layers into one readable article:

- online post;
- online questionnaire;
- reporter interview;
- expert comment;
- portal syndication.

Once the raw platform artifacts disappear, a later researcher may only see the neat article.

This creates two risks.

### Risk A — false platform certainty

The article says a person “发帖”, but without the original thread we cannot infer:

- which platform;
- whether it was a BBS, forum, blog or portal comment;
- whether replies existed;
- whether the text was edited;
- how visible the post was before journalism amplified it.

### Risk B — false population coherence

The journalist can gather different people, survey answers and online posts under one label such as `80后`.

The surviving page may therefore make a dispersed set of experiences look like a single coherent online community or shared script.

This is not evidence fraud; it is normal journalistic construction. Archaeology must preserve the distinction.

---

## 7. `syndication persistence != independent corroboration`

The 2010 Sohu page demonstrates a second problem.

Portal-era Chinese news was heavily syndicated and recombined. A striking number, quote or framing could move through:

```text
local report / portal article
→ national portal copy
→ later feature or topic package
→ another portal
→ search engine
```

If later research counts each surviving URL as an independent source, it can accidentally manufacture evidence strength.

For this case:

- the 2007 Sina page is one contemporaneous media object;
- the 2010 Sohu page is a later contemporaneous media object with new material;
- but its reused 2007 section is **not independent evidence for the original 2007 questionnaire**.

The repository should therefore track `source lineage` as well as `URL count`.

---

## 8. Evidence grading

### A. 2007 Sina page as a historical claim source

**Grade: B / A-boundary, with split grading.**

Why split it:

- the article itself is contemporaneous publication text with a displayed 2007 timestamp and stable original-domain URL;
- however current retrieval is not a verified 2007 archive capture;
- the underlying online posts/questionnaire are mediated by the article and are not independently opened.

Use it confidently for:

- `this story was publicly framed this way in 2007`;
- `portal journalism reported young adults posting elder-support budgets online`;
- `these interview/self-report statements were published at the time`.

Do **not** use it as direct proof of:

- the original post UI;
- platform identity;
- thread popularity;
- national prevalence.

### B. 2010 Sohu page

**Grade: B.**

Use it for:

- 2010 media framing;
- evidence that 2007 figures were still being recirculated;
- new interviews/surveys explicitly contained in the 2010 article.

Do not count recycled 2007 material as a second independent 2007 observation.

---

## 9. Archive probe status

### 2007 Sina URL

Public Web searches during this slice were performed for:

- exact title + `Wayback`;
- exact URL + `web.archive.org`;
- filename `093113113590s.shtml` + archive terms.

No usable Wayback locator was returned in the search results used in this run.

This means only:

> **no verified historical capture was located and opened in this slice.**

It does **not** mean:

- Internet Archive has no capture;
- no other archive preserved it;
- the page was unavailable in 2007.

Current status:

```yaml
subject: news.sina.com.cn/s/2007-12-20/093113113590s.shtml
historical_publication_datetime: 2007-12-20T09:31:00+08:00  # displayed by page/search result
current_live_url_discoverable: true
archive_locator_found_in_this_slice: false
verified_historical_capture_opened: false
historical_content_type: unknown
historical_charset: unknown
historical_dom: unknown
historical_css_js: unknown
underlying_forum_post_url: unknown
m1_complete_case_status: NOT_ACHIEVED
```

### 2010 Sohu URL

The URL is currently discoverable in Web search with original publication date and substantial body text.

A direct historical capture was not opened in this slice.

```yaml
subject: news.sohu.com/20101118/n277713972.shtml
historical_publication_datetime: 2010-11-18T05:28:00+08:00  # displayed by search result
current_live_url_discoverable: true
verified_historical_capture_opened: false
historical_charset: unknown
historical_dom: unknown
m1_complete_case_status: NOT_ACHIEVED
```

---

## 10. Why this matters to ordinary-life research

The companion `how-people-lived` note uses the 2007 article because it preserves unusually concrete household budgeting:

- mortgage;
- current household expenses;
- savings for a child's education;
- support for two sets of parents.

Old-Web archaeology changes how that evidence should be cited.

The strongest safe formulation is:

> A 2007 portal-news article reported and quoted young adults discussing elder-support budgets online, and preserved several contemporaneous household calculations.

A weaker but tempting formulation would be:

> “A 2007 forum thread shows how 80后 users calculated elder care.”

That second wording is not currently supported because the original forum artifact has not been located and opened.

This is exactly why platform/site/page/capture/claim separation matters.

---

## 11. Counterexamples and caution

### A surviving original URL is not automatically technically original

A portal may migrate static content into a new CMS or delivery shell while keeping the old path.

Without a historical capture, do not infer:

- ASP/JSP/static-HTML implementation;
- GB2312/GBK/UTF-8;
- IE-only behavior;
- table layout;
- historical ad technology;
- comment implementation.

All remain `UNKNOWN`.

### A portal article is not a neutral window into the original forum

Journalists selected which posts and budgets to quote.

The page can prove **media visibility**, not raw forum frequency.

### A repeated number is not a new measurement

The 2010 Sohu page reuses the 2007 figures.

Count provenance chains, not pages.

---

## 12. Next artifact tasks

1. query Wayback CDX or another archive interface for the exact 2007 Sina URL;
2. if found, open at least two capture datetimes rather than storing a locator only;
3. record HTTP/replay state, original URL, capture datetime, Content-Type and charset;
4. inspect whether body text is static and whether assets resolve;
5. search the 2007 article wording for the upstream International Online/local-news version;
6. search quoted phrases from the named online post to locate the original thread/platform without republishing unnecessary personal information;
7. map the 2010 Sohu page's source lineage back to the People's Daily/People.com version if available;
8. compare the 2007 and 2010 portal pages only after distinguishing reused material from newly collected evidence.

---

## Conclusion

This slice adds two useful Old-Web distinctions:

> **`live-origin content survival != verified historical interface survival`**

and

> **`syndication persistence != independent corroboration`**.

A piece of ordinary-life evidence can survive surprisingly well as text while its original platform context, thread, browser environment and source independence become much harder to recover.

For historians of everyday life, that means the visible old Web may preserve the **story people later read** more completely than the **distributed online conversations from which the story was assembled**.
