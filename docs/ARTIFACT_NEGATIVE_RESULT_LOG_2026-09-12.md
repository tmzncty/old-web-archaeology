# Artifact Negative-Result Log — 2026-09-12

> Scope: implementation of the structured negative-artifact record proposed in `RESEARCH_SATURATION_DEDUP_AND_ARTIFACT_PRIORITY_AUDIT_2026-09-12.md`.
>
> This file does **not** treat a failed replay as evidence that the historical page never existed or that Internet Archive lacks a capture. It records only what this research run could and could not verify.

## Why record negative artifact work separately

Recent domain notes repeatedly reached the same state:

```text
period-correct host / URL locator found
!=
archive capture actually opened and inspected
```

Repeating that sentence inside another `*_STATE_GAPS_*.md` file creates topic proliferation without moving M1 forward.

A structured negative-result log is more useful because it preserves:

- the exact historical object attempted;
- where the candidate locator came from;
- which replay / archive path was tried;
- whether the main document actually opened;
- what remains unknown;
- what a later researcher should try next.

This directly follows `docs/METHOD.md`:

> A search result containing a Wayback link is not a verified capture; an un-opened locator remains only a candidate capture.

---

# Record 1 — CSDN IT job-hunting portal, 2005 candidate capture

```yaml
object: CSDN IT job-hunting portal
research_unit: site/page candidate, not yet a verified capture
platform_or_site: CSDN
original_host: www.csdn.net
original_url: http://www.csdn.net/job/
period_claimed: 2005
candidate_capture:
  archive_source: Internet Archive Wayback Machine
  locator: https://web.archive.org/web/20050408034818/http://www.csdn.net/job/
  timestamp_string: "20050408034818"
opened_capture: false
failure_class:
  - candidate_not_opened
  - replay_or_fetch_cache_miss_in_current_research_environment
evidence_grade_for_locator: C/D boundary for the locator itself; later secondary pages point to it, but the historical artifact was not inspected
m1_status: NOT ACHIEVED
```

## 1. Locator provenance

A current English Wikipedia entry for CSDN lists an `IT job hunting` service and points to this exact Wayback locator:

- `https://web.archive.org/web/20050408034818/http://www.csdn.net/job/`

Source:

- https://en.wikipedia.org/wiki/Chinese_Software_Developer_Network

DBpedia exposes the same archived URL as an external link derived from the Wikipedia entity:

- https://dbpedia.org/page/Chinese_Software_Developer_Network

These are **later secondary locator sources**, not historical proof of the page's contents.

The locator is useful because it gives a concrete original URL and candidate timestamp, but by the repository's evidence contract it remains only a **candidate capture** until the actual replay is opened and checked.

## 2. Period-near evidence that a CSDN talent service did exist

The research run also found evidence independent of the current Wikipedia description that CSDN operated a talent / recruitment service in the 2000s.

### 2.1 51CTO blog copy of CSDN talent-service material

A 51CTO blog page preserved material headed `关于CSDN 人才服务业务`. The page states that the CSDN talent service was intended for IT professionals and IT enterprises, and describes a workflow in which enterprise members could publish recruitment information and query / download résumés from a CSDN technical-talent database.

Source:

- https://blog.51cto.com/lewis/61736

Evidence class: **B / near-period secondary or copied business material.**

What it can support:

- a CSDN talent-service business existed by the period represented by the page;
- employer-side job posting and résumé-database access were part of the described service model.

What it cannot support:

- the exact 2005 HTML / DOM of `www.csdn.net/job/`;
- whether every described service was available on that exact date;
- the search fields, application button, login boundary, charset, browser requirements, or transaction path visible to an ordinary user.

### 2.2 2007 report of CSDN talent-channel career discussion

A 2007 article reports that CSDN's management channel and talent channel hosted an online discussion about job-hopping, career transition, promotion and entrepreneurship, including developers who had moved to Baidu.

Source:

- https://www.admin5.com/article/20070127/34873.shtml

Evidence class: **B, near-period secondary report.**

This supports the existence of a career-oriented CSDN channel and career-information use. It does not by itself reconstruct the recruitment transaction interface.

## 3. Archive replay attempted in this run

The exact candidate link above was followed from the DBpedia / Wikipedia locator.

Result in the current research environment:

```text
replay fetch -> cache miss / main document not returned
```

Therefore the following fields remain **unverified**:

- actual Wayback replay status;
- whether the response was the historical main document, redirect, error, login page or archive placeholder;
- HTTP status;
- `Content-Type`;
- charset / encoding;
- page title;
- DOM structure;
- form methods / actions;
- search parameters;
- job-list URL pattern;
- résumé / applicant login boundary;
- employer login boundary;
- whether applications were submitted on-site, by e-mail, or redirected elsewhere;
- JavaScript dependencies;
- frames / iframe use;
- CSS / image / script subresource survival;
- historical browser assumptions;
- whether an ordinary visitor could execute a complete application from this page.

No IE / ActiveX / GB2312 / GBK / ASP / JSP claim is made from period stereotype.

## 4. Second candidate time point

A current Russian Wikipedia page lists a second historical locator for the same original path with timestamp string:

- `20060207145021`

Implied candidate URL:

- `https://web.archive.org/web/20060207145021/http://www.csdn.net/job/`

Source:

- https://ru.wikipedia.org/wiki/CSDN

Status:

```yaml
second_timepoint_candidate: true
opened_capture: false
cross_time_comparison: NOT POSSIBLE YET
```

This is useful because M1 requires at least two historical time points, but it must not be promoted to a verified time point until the replay is actually opened.

## 5. Related host locators

The same later CSDN secondary page exposes candidate 2005 Wayback URLs for sibling service areas:

- `http://dev.csdn.net/`
- `http://www.csdn.net/news/`
- `http://training.csdn.net/`

These may later help with site identity, navigation topology or common layout **if** their actual captures can be opened. They were not treated as substitutes for the job portal in this run.

## 6. Why this is still useful for the life-history cross project

The companion `how-people-lived` research now has strong evidence that recruitment platforms can function in two different ways:

1. **opportunity infrastructure** — distant jobs become searchable;
2. **market-signal infrastructure** — users infer that the labor market is tightening when similar searches produce fewer responses, fewer postings or slower callbacks.

A verified 2005–2006 CSDN recruitment artifact would therefore help answer two archaeological questions:

- What could an IT worker literally see and do on a Chinese recruitment portal at that moment?
- Which parts of labor-market experience were public Web state versus private account / callback state that archives are unlikely to preserve?

The second question matters because even a perfect capture of the public job portal would still not preserve an individual's recruiter response rate.

A future case should therefore keep this distinction:

```text
public job page survives
!=
historical job inventory fully survives
!=
application submitted
!=
recruiter viewed it
!=
callback received
!=
user's perceived market probability survives
```

---

## 7. Confirmed / probable / unknown

### Confirmed in this run

- Current secondary sources expose an exact Wayback locator for `http://www.csdn.net/job/` at timestamp string `20050408034818`.
- Near-period Web material describes a CSDN talent service involving employer job postings and résumé-database access.
- A 2007 report describes a CSDN talent channel hosting career-oriented discussion.
- The candidate 2005 Wayback replay was **not successfully opened** in the current research environment.

### Probable, but not promoted to confirmed artifact claims

- The candidate locator likely corresponds to a real archived historical resource rather than an invented URL, because several later references converge on it.
- The `www.csdn.net/job/` path was plausibly part of the talent-service surface described in near-period materials.

These remain probabilistic until the capture itself is inspected.

### Unknown

- exact historical page appearance;
- charset;
- layout;
- search fields;
- account model;
- on-site application mechanics;
- e-mail / off-site handoff;
- JavaScript / plugin dependencies;
- resource loss;
- whether 2005 and 2006 captures differ;
- whether the archive captured any live job listings or only a shell.

---

## 8. Next verification actions

Priority order for a later run:

1. Open the 2005 candidate capture through an archive client that can return the actual main document and headers.
2. Open the 2006 candidate time point.
3. Record `original_url`, `capture_url`, exact capture timestamp, replay state, title, HTTP / `Content-Type`, charset when reliable.
4. Inspect DOM / link and form structure without executing private-account actions.
5. List missing subresources separately from main-document survival.
6. Search period tutorials / screenshots for the same job portal as an independent evidence family.
7. Compare 2005 and 2006 only after both artifacts are verified.
8. If both replay attempts fail, classify the exact failure (`redirect_only`, `robots`, `dynamic_state_missing`, etc.) rather than writing “Wayback did not save it.”

---

## 9. Methodological result

This run does **not** achieve M1 for CSDN recruitment.

It does achieve a smaller methodological advance requested by the previous audit: archive-negative work is now captured in a reusable structured form rather than disappearing into prose or triggering another domain note.

The result should be cited as:

> `candidate locator found; historical capture not verified in this run`

not:

> `historical page recovered`

and not:

> `historical page absent from the archive`.
