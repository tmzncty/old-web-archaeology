# Artifact probe: `carboy.163.net` / “完全上网手册” personal homepage (1996–2000)

> Status: **artifact probe / negative verification record**, not a new domain theory note.
>
> Canonical nearby note: `docs/PERSONAL_HOMEPAGE_PUBLIC_SELF_METRICS_AND_PLATFORM_MORTALITY_1996_2015.md`
>
> Companion life-history evidence upgrade: `tmzncty/how-people-lived/sources/evidence-upgrade-carboy-personal-homepage-feedback-loop-and-client-stack-china-1996-2000.zh-CN.md`

## 0. Why this probe exists

The repository already has a mature state model for personal homepages:

```text
person
!= account
!= homepage namespace
!= page body
!= asset set
!= guestbook database
!= counter state
!= audience history
!= archive capture
!= current replay
```

The current bottleneck is not another conceptual variant. The ROADMAP / saturation audit asks for **opened, time-stamped historical artifacts**, ideally at more than one historical point.

This run therefore tried to turn the well-known early Chinese personal homepage “完全上网手册” into an actual archaeological case.

Result: **historical identity/locator evidence improved, but no qualified historical capture was opened. M1 remains not achieved.**

---

## 1. Historical identity evidence

### 1.1 Near-contemporaneous 2000 profile

Liu Ren’s 2000-11-06 profile of Yang Zhenting (`Carboy`) describes:

- his first network experience on Guangdong `视聆通`;
- a 14400 bps modem;
- a `Windows 3.1`-only client despite his machine already running Windows 95;
- later acquisition of a separate Internet account;
- creation of “carboy 的个人主页”;
- the page’s shift from automobile material toward Windows 95 dial-up / Internet-help material after repeated reader questions;
- the later disappearance / relocation of the original “完全上网手册”.

Source:

- 刘韧，《杨震霆广州网事》，《计算机世界》/ 新浪科技，2000-11-06: <https://tech.sina.com.cn/path/2000-11-06/491.shtml>

Evidence grade: **B** — near-contemporaneous press profile with participant quotations. Strong for the described sequence; not a substitute for the 1996–1999 Web artifact.

### 1.2 Near-contemporaneous 2000 homepage retrospective gives concrete historical locators

A 2000-12-14 Sina article on early “十佳个人主页” lists the Carboy site with a period locator:

- `business.gznet.com/carboy/`

and says that after the original page was removed, only fragments remained at:

- `carboy.163.net`

Source:

- 《中国最早的“十佳个人主页”流落何处》，新浪科技，2000-12-14: <https://tech.sina.com.cn/r/m/46310.shtml>

Evidence grade: **B/C** — near-contemporaneous retrospective useful for locator identity and then-current survival state; not an archived copy of either historical URL.

### 1.3 Contemporaneous demand-side context

A 1998-05-16 Usenet post preserved in Google Groups reposted a network-news item saying that NetEase’s reopened free-personal-homepage application service received more than 3,000 applications on the first day.

Source:

- `cn.bbs.comp.software`, “网络新闻(转)”, 1998-05-16: <https://groups.google.com/g/cn.bbs.comp.software/c/N-CnYVj4n8M>

Evidence grade: **B/C** — contemporaneous circulated text, original news provenance unresolved.

This is useful context for the hosting environment, but does not prove that Carboy used the same signup path or that all applicants became active pages.

---

## 2. A historical preservation clue: search identity surviving after content identity broke

The 2000 Liu Ren profile says that after the original “完全上网手册” was gone, a Yahoo! search for the name could still find a site/result, but the content was no longer Yang Zhenting’s actual “完全上网手册”.

This is a valuable period observation of:

```text
search-result identity / remembered site name
!=
current content identity at the resolved location
```

The repository already models searchable-past and identity / host drift elsewhere, so this is recorded as **supporting evidence**, not promoted into a new named preservation mechanism.

What it does show is that Web loss can be partial and misleading:

- a remembered title can survive;
- a search result can survive;
- a host/path can be reused or repointed;
- yet the page body and site identity that users remember can already be gone.

---

## 3. Artifact search performed in this run

Candidate historical URLs / identities checked:

```text
http://business.gznet.com/carboy/
http://carboy.163.net/
carboy.163.net
“完全上网手册” + Carboy / 杨震霆
```

Search paths attempted:

1. exact-host / exact-string Web searches;
2. searches scoped to `web.archive.org` / Wayback-like URLs;
3. direct Wayback calendar / CDX-style URL attempts from the available browsing runtime;
4. direct HTTPS CDX query from the execution container.

Observed result:

- no accessible search result surfaced a historical `carboy.163.net` memento that could be opened and inspected;
- direct Wayback URL opening in the Web runtime was rejected as an unsafe/unresolved URL because no prior Wayback result existed to follow;
- direct container access to `web.archive.org` failed DNS resolution in this runtime;
- therefore no capture timestamp, HTTP/replay state, DOM, charset, assets, or second time point was obtained.

Critical interpretation:

> **This does not prove that the Internet Archive has no capture. It only proves that this run did not obtain and open one through the available access paths.**

Do not convert this into “Wayback 没保存”.

---

## 4. Structured negative-result record

```yaml
object: Carboy / 完全上网手册 personal homepage
original_host_candidates:
  - business.gznet.com
  - carboy.163.net
period_claimed: 1996-2000
locator_sources:
  - https://tech.sina.com.cn/path/2000-11-06/491.shtml
  - https://tech.sina.com.cn/r/m/46310.shtml
archive_sources_checked:
  - general Web search for exact historical host/path
  - web.archive.org-scoped search queries
  - Wayback calendar/CDX URL attempts from Web runtime
  - direct CDX request from container runtime
opened_capture: false
failure_class:
  - no_accessible_candidate_returned
  - archive_query_transport_failure
  - candidate_not_opened
unknowns:
  - whether Wayback contains captures inaccessible to the current search/runtime path
  - exact earliest page URL and URL migrations
  - capture datetime(s)
  - original HTTP status / redirect chain
  - DOM / markup
  - charset / Content-Type
  - image and download subresources
  - counter / guestbook backing state
  - when the automobile-to-Internet-help transition occurred in page content
next_action:
  - retry via a working CDX/Wayback access path
  - query business.gznet.com/carboy/ and carboy.163.net separately with exact and prefix matching
  - if captures exist, open at least two distinct historical timepoints
  - record capture URL, timestamp, replay state, charset, DOM, subresource failures, and visible links
```

The `failure_class` values `no_accessible_candidate_returned` and `archive_query_transport_failure` are deliberately more precise than pretending a repository-wide `no_candidate` result. The current runtime itself is part of the uncertainty.

---

## 5. What can be reconstructed without pretending it is the page

From contemporaneous descriptions we can responsibly say:

- Carboy maintained a personal homepage in the 1990s;
- an early locator was reported as `business.gznet.com/carboy/`;
- later fragments were reported at `carboy.163.net`;
- the content included Internet / software / homepage-making help and automobile material;
- reader questions materially influenced what he kept adding;
- by late 2000, contemporaries already described the original site as partly or largely lost / displaced.

We **cannot** currently claim:

- the page’s exact HTML structure;
- exact charset;
- whether a given logo / counter / guestbook rendered at a historical timestamp;
- what its navigation looked like in 1996, 1997, 1998 or 1999;
- that a surviving current page is byte-identical to any historical version;
- that Yahoo’s 2000 result can presently be replayed;
- the exact redirect / ownership transition that produced the search/content mismatch.

Therefore this probe remains a **locator-and-contemporaneous-description case**, not a capture case.

---

## 6. Overseas comparator: GeoCities confirms the general platform transition, not a China-only phenomenon

Yahoo’s 1999-01-28 acquisition announcement described GeoCities as hosting more than 3.5 million user-authored sites and emphasized tools allowing non-technical users to create, publish and update Web content. WIRED’s same-day coverage described GeoCities as the largest personal-homepage provider and a major audience property.

Sources:

- Yahoo!, `Yahoo! To Acquire Geocities`, 1999-01-28 (preserved by NewMediaWire): <https://www.newmediawire.com/news/yahoo-to-acquire-geocities-3064119>
- WIRED, `Yahoo Gobbles Up GeoCities`, 1999-01-28: <https://www.wired.com/1999/01/yahoo-gobbles-up-geocities-2/>

Evidence grade: **B** for contemporaneous corporate self-description / media reporting.

Comparison:

```text
GeoCities / global Web:
low-cost hosted personal publishing + community/audience aggregation

Carboy / Guangzhou:
personal publishing emerges while users may still be crossing
local-network -> full-Internet and client-configuration barriers
```

The broad personal-publishing transition is not China-specific. The Chinese case is useful because it shows that **publishing layer, access layer, and client stack could move at different speeds**.

No genuinely new cross-national structural difference is claimed from this run.

---

## 7. M1 assessment

Required for a strong M1 personal-homepage case:

- [x] historical entity / page identity has period evidence;
- [x] concrete historical locator candidates identified;
- [x] multiple source types / dates available for context;
- [ ] at least one historical capture actually opened and inspected;
- [ ] second historical time point;
- [ ] capture datetime and replay/HTTP state;
- [ ] DOM / charset inspection;
- [ ] subresource-loss inventory;
- [ ] counter / guestbook / private backing-state boundary grounded in the artifact;
- [ ] browser-era replay comparison.

Result:

**`M1 personal-homepage case: NOT ACHIEVED IN THIS RUN.`**

---

## 8. Saturation / de-duplication consequence

This run strengthens existing personal-homepage and historical-visibility conclusions, but it did **not** produce:

- a new ordinary-life pathway;
- a new institutional interface;
- a new period-time mechanism;
- a new communication / Internet transition mechanism;
- a new cross-national structural difference;
- or a verified historical artifact that materially changes the existing conclusion.

The earlier Internet-café run had produced genuine new mechanisms and therefore reset the sequence. This run should now count as:

**1 / 3 consecutive runs without substantive new mechanism.**

No closure is justified. The next run should continue with artifact verification / same-person longitudinal evidence before considering another domain-specific concept note.