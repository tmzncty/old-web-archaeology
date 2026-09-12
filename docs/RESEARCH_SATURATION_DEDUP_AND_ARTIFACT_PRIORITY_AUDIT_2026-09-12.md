# Research Saturation, De-duplication, and Artifact Priority Audit — 2026-09-12

> Scope: process audit for the `how-people-lived` × `old-web-archaeology` cross-research line.
>
> This is **not** a closure document and does not move the repository beyond its stated 1995–2015 Chinese-Web scope.

## 0. Why this audit is necessary now

This run re-read:

- current `main` and recent commits;
- `ROADMAP.md`;
- `RESEARCH_PLAN.md`;
- `docs/METHOD.md`;
- the current file/topic inventory;
- the companion Life Horizons ROADMAP / INDEX / methodology and topic tree.

The repository has accumulated a large number of useful transaction-state notes. That work has made a recurring point very clear:

```text
public page state
!=
private account state
!=
live inventory / queue / workflow state
!=
offline completion
```

The new risk is different: repeating the same epistemic warning under another domain-specific filename without materially improving the historical evidence base.

The repository's own roadmap still defines M1 / Phase 2 around **three complete archaeological cases** with identity confirmation, at least two historical time points, multiple evidence sources where possible, resource-loss lists, browser / encoding / plugin assumptions, and explicit confirmed / probable / unknown columns.

Therefore the next unit of progress should increasingly be measured by **artifact quality and cross-time verification**, not by the count of additional `*_STATE_GAPS_*.md` files.

---

## 1. Candidate probes rejected as duplicate expansion

### 1.1 Deaf / disability accessibility

A new broad “Web accessibility changed ordinary life” note would duplicate existing work.

Already present:

- `docs/DEAF_COMMUNICATION_SMS_CHAT_FORUM_SIGN_VIDEO_CAPTION_AND_ACCESSIBILITY_STATE_GAPS_2002_2015.md`
- companion Life Horizons work on deaf communication independence;
- companion Life Horizons work on visual impairment and screen-reader independence.

The deaf note already covers:

- pre-Web TTY as an overseas boundary condition;
- Chinese fixed-line/mobile SMS accessibility in 2002;
- “聋人在线” in 2005;
- QQ / SMS / relay-service evidence in 2007;
- modality-specific executability;
- public-Web versus private-communication archive gaps.

**Decision:** no new general accessibility file.

Useful future increment would require one of:

- an actual historical Chinese deaf-community capture;
- a browser / screen-reader compatibility artifact;
- a contemporaneous blind-user report tied to a specific host and interface;
- a comparison showing a genuinely different transaction state model.

### 1.2 Part-time / odd jobs / gig work

Already covered by domain notes around:

- campus part-time job boards;
- day-labor / odd-job boards;
- witkey task markets;
- recruitment listings and employment-state gaps.

**Decision:** do not open another generic “online gig platform” state-gap note unless the evidence introduces a new historical object or transaction architecture.

### 1.3 Searchable past / reputation / context collapse

This run checked the overseas Deja News / Google Groups transition as a comparative object.

In February 2001 Google announced acquisition of Deja's Usenet archive, then expanded Google Groups later that year into a searchable archive reaching back to 1981. Contemporary users and press immediately noticed that old posts could become much easier to retrieve than when originally written.

Sources checked:

- contemporaneous Google announcement text preserved in Usenet / Google Groups: https://groups.google.com/g/news.admin.net-abuse.usenet/c/Ep2SvF48aEw/m/fEPNnyyEylEJ
- WIRED, April 2001, contemporary interviews on unexpectedly retrievable old posts: https://www.wired.com/2001/04/google-restores-deja-view/
- contemporaneous December 2001 Google Groups archive announcement text: https://groups.google.com/g/alt.music.j-s-bach/c/1ljVLPaYn7M

This supports a real archaeological distinction:

```text
PUBLIC_WHEN_POSTED
!=
GLOBALLY_SEARCHABLE_BY_AUTHOR_OR_KEYWORD_YEARS_LATER
```

But that mechanism is already substantially represented in the companion life-history repository through searchable-past, alumni / re-contact, public identity, pseudonym / identity-portfolio, resume / candidate legibility, and search-engine topics.

For the Chinese old-Web repository, a new file is **not yet justified** without a period-correct Chinese artifact or contemporaneous user account demonstrating that an old BBS / blog / homepage became newly searchable and materially affected employment, family, courtship, or another offline relation.

**Decision:** comparative evidence retained here; no new state-gap topic.

---

## 2. What the roadmap says versus what the repository has been doing

`ROADMAP.md` and `RESEARCH_PLAN.md` still prioritize:

1. method / data contracts;
2. a candidate survey;
3. three complete archaeological cases;
4. platform genealogy;
5. browser-environment experiment;
6. archive-gap model.

The current corpus, however, contains many conceptual transaction notes for specific domains.

Those notes are useful research scaffolding, but they must not silently substitute for the M1 / Phase 2 acceptance criteria.

A domain note that says:

```text
form visible
!=
submission accepted
!=
backend action completed
```

is methodologically correct, but it is not itself a complete archaeological case unless the relevant historical page, capture time, replay state, resource dependencies, and cross-time comparison are actually verified.

---

## 3. De-duplication gate for future new files

From this point, a new domain-specific old-Web note should normally require at least **one** of the following that is not already present in nearby work:

1. **Verified historical artifact**
   - an opened capture, not a search-result locator;
   - original URL + capture URL + timestamp + replay/HTTP state;
   - main-document versus subresource distinction;
   - charset / Content-Type where reliable.

2. **New transaction architecture**
   - not merely another version of `page -> form -> private state -> offline completion`;
   - for example, a historically distinctive relay, store-and-forward, offline-reader, batch-sync, or multi-operator workflow.

3. **New ordinary-life pathway**
   - evidence that the interface enabled or blocked a life route not already modeled in the companion repository.

4. **New preservation mechanism / failure mode**
   - e.g. a platform-specific URL architecture, dynamic resource dependency, login boundary, plugin requirement, or charset failure demonstrated by artifact evidence.

5. **Cross-time change on the same site / platform**
   - at least two historical points showing an actual interface or ownership / identity / workflow transition.

If none applies, the preferred action is:

- append evidence to an existing canonical note;
- update a synthesis / genealogy;
- or record the negative search in a research audit.

---

## 4. Artifact priorities: existing domains where state models are mature but M1 remains weak

The cross-research line has repeatedly reached the same boundary: historical hosts / locators are known, but the transaction page itself has not been verified to the repository's minimum capture contract.

High-value candidates for the next runs include:

### A. Early online recruitment

Known period-correct recruitment hosts and campus links already exist in notes.

Need:

- one actual 1999–2005 capture;
- original URL and exact timestamp;
- form / link structure;
- charset;
- whether application was on-site, email-based, downloadable, or redirected;
- second time point if possible.

Life-history payoff: separates “jobs became visible at distance” from “applications became executable at distance.”

### B. Dating / matchmaking

Existing notes already model profile / search / message / offline-meeting state gaps.

Need:

- actual historical Jiayuan / Baihe profile-search or help capture;
- evidence for search fields and message boundary;
- membership / payment interface at a historical time point;
- explicit distinction between public profile and private relationship outcome.

Life-history payoff: no need for another partner-addressability theory; the next gain is knowing what a 2000s user could literally see and click.

### C. Railway / 12306

Multiple notes already model query, inventory, payment, ticketing, identity and boarding gaps.

Need:

- verified early `12306.cn` / `dynamic.12306.cn` capture;
- period-specific DOM / forms / redirects;
- subresource and certificate / client assumptions only where evidenced;
- comparison across at least two early moments.

Life-history payoff: converts a mature mobility-slot theory into reproducible Web archaeology.

### D. Hospital appointment portals

Existing notes already model patient / operator / proxy / slot / visit distinctions.

Need:

- actual historical portal artifact from a known hospital or city platform;
- account / real-name boundary;
- whether live slot data was server-rendered, session-bound, or otherwise unavailable to archive;
- explicit failure record where private state cannot be recovered.

Life-history payoff: strengthens the claim about body-queue displacement without pretending archive pages preserve historical slot inventory.

### E. Online banking / remittance

Existing notes already model account / authentication / payee / transfer / clearing / recipient gaps.

Need:

- verified period capture of a public help or transaction shell;
- evidence for USBKey / certificate / browser requirements at a specific date;
- no inference from contemporary security articles to all banks or all users.

Life-history payoff: distinguishes institutional electronic rails from consumer Internet self-service.

### F. E-commerce / escrow

Latest cross-research work already models listing / inventory / order / escrow / shipment / delivery / refund state separation.

Need:

- actual early item / help / escrow flow capture;
- second time point;
- platform-state versus courier-state boundary;
- archived public rules versus missing private order outcome.

Life-history payoff: turns “remote goods addressability” into a concrete historical interface sequence.

---

## 5. Archive-negative results should become first-class evidence

A repeated phrase across recent notes is effectively:

> period-correct host / locator found; M1 verified transaction capture not achieved in this slice.

That is useful, but future runs should normalize this into a small structured negative-result record rather than repeatedly opening another conceptual document.

Suggested minimum negative-artifact record:

```yaml
object:
original_host:
period_claimed:
locator_sources:
archive_sources_checked:
opened_capture: false
failure_class:
  - no_candidate
  - candidate_not_opened
  - replay_error
  - redirect_only
  - robots_or_access_boundary
  - login_or_session_boundary
  - dynamic_state_missing
  - subresources_missing
unknowns:
next_action:
```

This would directly support the roadmap's future archive-gap model.

---

## 6. Cross-repo coverage assessment

The companion life-history repository now has strong or very strong coverage in:

- education and re-entry;
- job search, job change, informal / multiple work;
- housing and non-kin households;
- marriage / partner search / family formation;
- migration and return travel;
- caregiving and care access;
- identity documents and record portability;
- communication channels and reachability;
- public Internet / home Internet / shared terminals;
- information search and procedural knowledge;
- social ties / re-contact / identity portfolios;
- future expectations / fallback portfolios;
- platform disappearance / memory and archive bias.

Accordingly, old-Web should increasingly provide **artifact depth** for these already-developed mechanisms, rather than generating a parallel set of almost synonymous conceptual categories.

---

## 7. Saturation status for this run

After targeted probes, this run did **not** identify a genuinely new:

- ordinary-life pathway;
- institutional interface;
- period-time mechanism;
- communication / Internet transition mechanism;
- cross-national structural difference;
- or first-hand source that materially overturns an existing conclusion.

The Deja / Usenet comparison strengthens an existing historical-visibility mechanism, but does not currently justify a new Chinese old-Web research object.

Therefore the cross-research saturation counter should be recorded as:

**1 / 3 consecutive runs without substantive new mechanism.**

This is not closure. No research task should be disabled yet.

The next run should first attempt **artifact verification or synthesis**, and only reset the saturation counter if it uncovers a genuinely new mechanism or conclusion-changing evidence.

---

## 8. Practical next-run order

1. Re-read current HEADs and this audit.
2. Do not choose a topic only because a keyword is absent from GitHub code search; inspect the file tree and synonyms first.
3. Pick one existing high-value M1-not-achieved domain.
4. Attempt an actual historical capture / artifact verification.
5. In parallel, look for one contemporaneous first-person life-history source that changes interpretation rather than merely illustrates it.
6. Check one overseas comparison, but do not create a new cross-national topic unless the difference is structural.
7. If no substantive increment again, update saturation to `2 / 3` rather than inventing another micro-topic.
