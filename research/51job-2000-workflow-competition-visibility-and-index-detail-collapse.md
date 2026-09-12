# 51job 2000 recruitment workflow checkpoint: competition visibility and index/detail preservation asymmetry

> Status: research checkpoint, intended to fold into the canonical recruitment note after a verified historical 51job capture is recovered.
>
> Canonical related note: [`docs/RECRUITMENT_LISTING_AND_RESUME_LIFECYCLE_1999_2004.md`](../docs/RECRUITMENT_LISTING_AND_RESUME_LIFECYCLE_1999_2004.md)
>
> Companion life-history slice: [`tmzncty/how-people-lived`](https://github.com/tmzncty/how-people-lived)
>
> M1 status for 51job historical Web artifact: **NOT ACHIEVED IN THIS SLICE**.

## 0. Why this checkpoint is justified despite the de-duplication audit

The repository already has a mature state model for early recruitment sites:

```text
listing exists
!=
listing is live
!=
user can apply
!=
application reaches employer
!=
interview
!=
hire
```

A new generic “online recruitment state gap” note would therefore be duplicate expansion.

This checkpoint is narrower and adds two things not previously established in the canonical note:

1. a **contemporaneous participant-observation trace** from 2000 showing an actual user filtering jobs, seeing a visible applicant count, abandoning one crowded vacancy, submitting online résumés, configuring e-mail matching, and observing next-day partial feedback;
2. a **current preservation asymmetry** in 51job's own media-history section: dated index rows for 2000 survive, while the item-level route exposed through the current page does not recover the corresponding article body through the observed link path.

The first adds a historically distinctive interface behavior; the second adds a preservation mechanism.

---

## 1. Evidence inventory

### A. 2000-08-05 contemporaneous participant-observation article

Current live-origin URL carrying period-dated content:

- <https://edu.sina.com.cn/guide/2000-08-05/9462.shtml>
- displayed date: 2000-08-05 12:16
- displayed source: 《精品购物指南》

Evidence class:

- **B+ — contemporaneous media participant observation** for user behavior and reported interface fields;
- **not an A-grade historical capture of 51job itself**.

The article reports that the journalist:

- searched for job sites and compared five;
- selected 51job;
- searched for “编辑” and saw 522 effective job entries;
- refined by Beijing / website editor / negotiable salary / last week and received 75 results;
- inspected one vacancy and saw a platform record showing 685 online résumé submissions;
- interpreted that count as high competition and abandoned the vacancy;
- selected 12 employers and submitted résumés online;
- stored an online résumé containing profile information, a photo and work samples;
- configured e-mail matching fields including job type, salary, place, send time, frequency and result-count limit;
- spent a little over one hour on the process;
- saw 23 matching-job notices that evening and, by the next day, 3 interview invitations and 2 job-search replies, while other applications were silent.

This is much stronger than a generic product-description page because it records a sequential interaction and a decision changed by visible interface state.

### B. 2000-02-28 contemporaneous report on cross-channel registration

- Sina Tech, 2000-02-28, 《〈财富〉500强企业与“前程无忧联盟”签约》
- <https://tech.sina.com.cn/news/it/2000-02-28/18495.shtml>

Evidence class: **B — contemporaneous industry report**, with service claims largely attributed to the alliance/platform.

The report describes 51job, the print publication 《前程周刊》 and a human-resources consultancy as an integrated recruitment alliance and states that individual job seekers could become users through:

- postal correspondence;
- telephone;
- fax;
- e-mail;
- direct Web registration at `51job.com`.

This supports:

```text
web platform != web-only ingress
```

It does **not** prove that a person registered by telephone or fax could independently execute every later Web interaction.

### C. 51job's current media-history index

Current URL:

- <https://media.51job.com/index2.php>

Observed current page state includes a 2000 media chronology with date, title and publication, including entries such as:

- 2000-11 — `JUDY网上求职记` — 《世界时装之苑》;
- 2000-05-29 — `测试网上找工作` — 《北京青年报》;
- 2000-04-10 — `亲历网上求职` — 《北京晨报》;
- 2000-03-29 — `网上应聘为什么总是没回音` — 《申江服务导报》;
- 2000-02-28 — `网上招聘与传统招聘方式携手 北京成立全方位人事招聘战略联盟` — 《南方都市报》.

Evidence class for the present page: **A for current observable artifact state; C/D boundary if used to infer historical publication metadata without independent period confirmation.**

Important present-day observation:

- the crawler exposes many article titles as the same current link target/id;
- following the observed title link returns the same index-level page rather than an item body.

Therefore this route currently gives us a surviving catalogue but not the corresponding article object.

This supports a preservation category introduced below, but it **does not prove** that the historical 51job media archive originally used the same routing or that no body exists elsewhere on the site.

### D. 2004 51job SEC F-1

- 51job, Inc., Form F-1, filed 2004-07-07
- <https://www.sec.gov/Archives/edgar/data/1295484/000114554904000896/u99016fv1.htm>

Evidence class: **A — contemporaneous corporate regulatory filing.**

This source is already used by the canonical recruitment note and is not a new discovery. It remains the strongest original institutional evidence for:

- website launch in 1999;
- job search and filtering;
- user accounts and online résumés;
- employer résumé-database access;
- e-mail matching;
- direct résumé submission;
- application tracking;
- print/Web integration.

It should continue to anchor platform-capability claims while the 2000 media trace anchors observed user behavior.

---

## 2. New interface mechanism: competition visibility

The 2000 participant-observation article records a user seeing a numeric count of online résumé submissions for a vacancy and then deciding not to apply.

This is archaeologically important because the visible state is not merely:

```text
job listing exists
```

but something closer to:

```text
job listing exists
+
platform exposes a crowding signal about other applicants
→
user changes selection behavior
```

Working term:

> **competition visibility / 竞争可见性**

An early recruitment interface could make some part of the rival-candidate field visible before an application was submitted.

### What the evidence supports

- a displayed count existed in the user's observed workflow;
- the user read it as a competition signal;
- the signal materially changed the user's action.

### What remains unknown

The historical semantics of `685` are not reconstructed.

Unknowns include:

- unique people vs submissions;
- cumulative vs active-window count;
- duplicate applications;
- whether withdrawn or expired applications remained counted;
- whether the number was generated dynamically;
- whether every vacancy displayed the field;
- whether the count was exact or rounded;
- employer-side visibility of the same statistic.

Therefore the safe claim is behavioral, not statistical:

> a period user saw a platform-provided applicant-count signal and acted on it.

Do **not** convert `685` into a historical application-to-hire ratio.

---

## 3. Reconstructable workflow from the media trace — and its limits

The participant-observation article supports this **reported workflow**:

```text
find recruitment sites
→ compare several sites
→ choose 51job
→ keyword search
→ structured filtering
→ inspect job rows/details
→ inspect applicant-count signal
→ abandon one crowded opportunity
→ select other opportunities
→ online résumé submission
→ create/store résumé
→ configure matching/subscription
→ receive e-mail notices
→ receive some interview/reply messages
```

This is useful for future artifact verification because it gives concrete things to look for in a genuine historical capture:

- keyword search box;
- advanced/full search;
- location field;
- job category field;
- salary field;
- posting-time filter;
- result count;
- listing columns;
- applicant/submission count;
- résumé center;
- stored résumé form;
- club/member registration;
- e-mail matching controls;
- online submission action.

But the media article is **not itself the interface artifact**.

It cannot establish:

- exact labels or field order beyond what the journalist reports;
- form method/action;
- URL structure;
- CGI/ASP/JSP/PHP implementation;
- historical HTTP status;
- DOM;
- frames;
- JavaScript;
- cookies/session behavior;
- `Content-Type`;
- charset;
- browser assumptions;
- which actions were server-side versus e-mail handoff;
- visual layout.

No IE / ActiveX / GB2312 / GBK claim is inferred from period stereotype.

---

## 4. New preservation mechanism: index-shell survival / detail collapse

The present 51job media-history page preserves a dense list of old media metadata:

```text
date
+
title
+
publication
```

Yet following the observed title link path returns the index-level page rather than the corresponding article body.

Working terms:

- **index-shell survival**;
- **catalog-survival / detail-collapse**.

Core rule:

```text
index row survives
!=
item body survives
!=
historical item permalink survives
!=
historical link routing survives
```

This is a distinct archive/preservation failure mode from:

- a dead domain;
- a missing Wayback snapshot;
- a live-origin article whose old body still survives;
- a syndicated copy surviving after the origin disappears.

A current site may preserve enough metadata to tell us that an object once belonged to a collection while no longer exposing the object itself through the current route.

### Why it matters

If research relies only on full-text search, item-body loss may make the historical corpus look much smaller than the surviving catalogue says it was.

If research relies only on the catalogue, the opposite error becomes possible: treating a title/date row as if the article body had been recovered.

Therefore old-Web evidence should distinguish:

```yaml
catalog_entry_observed: true
item_body_opened: false
historical_permalink_verified: false
historical_capture_opened: false
```

### Independent survival can partially repair the gap

For at least one early recruitment workflow, the contemporaneous body is independently accessible today on Sina.

This demonstrates another useful chain:

```text
origin/platform catalogue survives
+
independent portal copy survives
→
content can sometimes be reconstructed across hosts
```

But:

```text
independent copied text
!=
original 51job article page
!=
original 51job recruitment interface
```

The two objects must not be collapsed.

---

## 5. Cross-channel ingress is part of site archaeology

The 2000 alliance report shows that users could apparently enter the 51job service system through letter, telephone, fax, e-mail or Web registration.

This means a Web archaeology case should not assume that all database records originated from Web forms.

Suggested future field:

```yaml
record_ingress:
  web_form: confirmed/probable/unknown
  email: confirmed/probable/unknown
  phone_operator: confirmed/probable/unknown
  fax_operator: confirmed/probable/unknown
  postal_operator: confirmed/probable/unknown
  print_syndication: confirmed/probable/unknown
```

This extends the canonical note's `channel_relationship` model.

Potentially, the visible Web database was only one surface of a larger human-and-media workflow.

That has an archaeological consequence:

> **a surviving Web record may have been born outside the Web.**

Without this distinction, researchers can accidentally infer user Web adoption from the presence of records inside a Web platform.

---

## 6. Relation to the companion life-history interpretation

The companion research already models:

- `search-before-travel`;
- `passive findability`;
- access intermediation;
- print/Web hybrid recruitment.

This checkpoint adds a concrete behavioral layer:

> early online recruitment could expose not only opportunities but also a platform-generated estimate of how crowded an opportunity looked.

That changes the life-history question from:

```text
Can I see a distant job before travelling?
```

to:

```text
Can I compare several distant jobs and decide which one seems worth spending an application on?
```

In other words, the interface starts mediating **allocation of attention under uncertainty**.

---

## 7. Overseas comparison boundary

Pew Internet Project, 2002, reported rapid U.S. growth in online job searching and large résumé databases, with strong demographic and socioeconomic differences in use:

- <https://www.pewresearch.org/internet/2002/07/17/online-job-hunting/>

Evidence class: **B — contemporaneous institutional survey.**

This makes the broad transition to searchable jobs, résumé databases and access inequality cross-nationally comparable.

It does **not** establish that U.S. recruitment sites exposed the same applicant-count field, so `competition visibility` should currently remain a **verified Chinese instance**, not a universal early-Web design claim.

---

## 8. Historical capture attempt status

This run searched for a directly usable historical 51job recruitment capture and followed an available current link toward the Wayback Machine.

Result in the current research environment:

```yaml
object: 51job early recruitment interface
period_target: 1999-2004
exact_historical_capture_opened: false
m1_status: NOT ACHIEVED
failure_class:
  - no_verified_timestamped_capture_opened_in_this_slice
  - archive_replay_or_discovery_path_not_returned_as_inspectable_historical_document
```

This must **not** be rewritten as:

> Internet Archive did not save 51job.

It means only:

> this research slice did not open and verify a historical 51job capture to the repository's minimum contract.

Still unknown:

- original URL for the exact search/results page observed in August 2000;
- capture datetime;
- historical HTTP/replay state;
- main document vs redirect;
- Content-Type;
- charset;
- DOM;
- forms/actions;
- cookie/session requirements;
- subresource survival;
- second verified historical time point.

---

## 9. Confirmed / probable / unknown

### Confirmed in this run

- A current 51job media-history index exposes many 2000 date/title/publication rows.
- Following the observed current title-link route returned the index page rather than an item body.
- A Sina page with displayed date 2000-08-05 preserves a contemporaneous participant-observation account of 51job search/filter/submission/matching behavior.
- In that account, a visible count of 685 online résumé submissions changed the user's choice: the user abandoned that vacancy.
- A separate 2000-02-28 Sina report states that users could enter the 51job alliance through letter, telephone, fax, e-mail or direct Web registration.

### Probable / strong but not promoted to artifact claims

- The current 51job media index is likely a later retained or migrated catalogue of period coverage, but its own historical construction date and migration history are not established here.
- The 2000 participant-observation account likely reflects real 51job functions because its behavior aligns with capabilities later described in 51job's 2004 SEC filing; however, alignment is not a substitute for the missing historical site capture.

### Unknown

- historical semantics of the applicant-count field;
- historical permalink architecture of 51job's media archive;
- whether article bodies still exist under hidden/current routes;
- 2000 HTML, charset, DOM, scripts and browser requirements;
- exact registration/operator workflow for telephone/fax/post users;
- whether non-Web-entered records were later editable by users online;
- whether historical 51job search/results pages survive in public archives.

---

## 10. What this changes in old-Web method

Two reusable rules should be retained:

### Rule A — visible competition state is a historical interface object

For recruitment sites, record not only fields describing jobs and applicants but also **relational metadata** that could change user strategy:

```yaml
competition_signal:
  applicant_count_visible: true/false/unknown
  count_label:
  count_semantics: unknown/...
  user_behavior_response_evidence:
```

### Rule B — catalog survival must be separated from item survival

For any portal archive, media archive, blog index, download center or BBS topic list:

```text
catalog metadata survives
!=
item content survives
!=
item link remains resolvable
!=
historical capture exists
```

This should become part of future archive-gap modeling.

---

## 11. Next artifact actions

Priority order:

1. Find an exact timestamped historical 51job home/search/recruitment capture and actually open it.
2. Search for archived `search` / job-detail / résumé-center paths, not only the home page.
3. Look for a second verified time point, ideally 1999/2000 and 2003/2004.
4. Record URL patterns, HTTP/replay state, charset and form structure only after direct artifact inspection.
5. Search period screenshots/tutorials for the applicant-count field as an independent evidence family.
6. Search current 51job media-site source/route structure for whether item bodies are still reachable through another parameterized path; do not infer deletion from the current index-loop alone.
7. Compare the independently surviving Sina text against any later recovered origin article only after both are verified.

---

## 12. Saturation impact

This slice should reset/keep the cross-research “no substantive increment” counter at **0 / 3** because it adds:

- a contemporaneous behavior trace that materially changes the interpretation of early online job search (`competition visibility`);
- a new preservation failure mode (`index-shell survival / detail collapse`);
- direct cross-channel ingress evidence showing that a Web platform's records need not originate from Web-native user actions.

It does **not** achieve M1.

The correct status is therefore:

> **substantive interpretive increment achieved; historical 51job artifact verification still pending.**

---

*AI-assisted research checkpoint. Historical-interface claims remain bounded by the evidence classes and explicit unknowns above.*
