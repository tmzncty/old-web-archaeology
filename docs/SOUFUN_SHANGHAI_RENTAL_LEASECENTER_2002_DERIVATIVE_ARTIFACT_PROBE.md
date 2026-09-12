# SouFun Shanghai Rental Lease Center, 2002 — derivative-artifact probe

Status: artifact-focused research note  
Scope: one historical Chinese rental-Web object, `http://sh.soufun.com/asp/rnl/leasecenter`, observed in 2002 through a near-contemporary scholarly extraction.  
Companion state model: `RENTAL_LISTING_ROOMMATE_AND_OCCUPANCY_STATE_GAPS_1998_2015.md`  
Cross-repo companion: `tmzncty/how-people-lived/places/china/urban-young-adult-life-horizons-2005.zh-CN.md`  
Last research pass: 2026-09-12

---

## 0. Why this note exists

The repository already has a mature rental-listing state-gap model. It does **not** need another generic note saying:

```text
listing visible
!=
unit vacant
!=
lease signed
!=
occupancy
```

This probe is justified by a different archaeological result.

A 2004 scholarly book records that its example case base was extracted from a specific SouFun Shanghai rental URL on **2002-08-27**, with **251 cases**, and reproduces a 20-record sample plus field semantics.

The original historical Web interface has not been verified in this run. But some of its **data schema and sampled records survived inside a scholarly derivative artifact**.

That creates a preservation mechanism not yet formalized in the repository:

## **derivative-data survival / 衍生数据存活**

```text
historical Web page/interface may be missing
!=
historical Web data left no trace
```

A contemporary or near-contemporary paper, book, benchmark corpus, crawler output, search-engine cache, tutorial, screenshot, or software test fixture can preserve structured material copied from a historical site even when the original capture is unavailable.

This derivative evidence is valuable, but it is **not equivalent to a historical capture**.

---

## 1. Historical object

### 1.1 Claimed original URL

The 2004 book *Foundations of Soft Case-Based Reasoning* states that its rental-information example case base was taken from:

```text
http://sh.soufun.com/asp/rnl/leasecenter
```

on:

```text
2002-08-27
```

and consisted of:

```text
251 cases
```

Source:

- Sankar K. Pal and Simon C. K. Shiu, *Foundations of Soft Case-Based Reasoning*, Wiley, 2004, Chapter 1. DOI landing page:  
  https://onlinelibrary.wiley.com/doi/10.1002/0471644676.ch1
- Searchable chapter/PDF text preserving the relevant passage and Table 1.1:  
  https://citeseerx.ist.psu.edu/document?doi=fd1e6eeb9fb877907983bfcca910274951cab911&repid=rep1&type=pdf

Publication metadata:

- first published 2004-03-12 according to Wiley;
- authors affiliated with the Indian Statistical Institute and Hong Kong Polytechnic University.

Evidence grade:

- **B+ derivative artifact** for the claim that the authors obtained a 251-record rental case base from that URL on 2002-08-27;
- **not A archived-page evidence**, because this is an extraction/republication, not the original SouFun response or WARC.

Confidence: **high** for the narrow extraction claim; **unknown** for the historical HTML/UI details.

---

## 2. What the derivative artifact actually preserves

The book says 20 cases were randomly selected from the 251-case base for its worked example. The reproduced table preserves at least these fields:

```text
city district
address of apartment
apartment type
source of information
rental cost (yuan/month)
```

It also explains coding semantics. For example:

- one district abbreviation maps to Minhang;
- apartment-type codes encode room/sitting-room structure;
- `indi` means an individual landlord source;
- values marked with `*` indicate real-estate-agent sources.

The twenty displayed examples include multiple Shanghai districts and monthly asking rents spanning a wide range.

Evidence grade:

- **B+** for field existence in the authors' extracted case representation;
- **B**, not A, for treating these fields as a proxy for what SouFun exposed to users, because the authors may have normalized, recoded or selected fields during extraction.

### Important boundary

Do **not** write:

> `The 2002 SouFun HTML form contained exactly these five fields.`

The evidence only supports:

> `A 2004 scholarly work says it extracted a 251-case rental dataset from this exact SouFun URL on 2002-08-27 and represented the records using these fields.`

The distinction matters because:

```text
source-page field
!= crawler/parser output field
!= researcher-normalized field
!= published table field
```

Without the original HTML or crawler code, we do not know which transformations occurred between them.

---

## 3. Why this matters for ordinary-life history

The companion life-history question is not “was SouFun famous?” It is narrower:

> **Could a person trying to stay in a city before the mature platform era already use the Web to compare rental possibilities across location, dwelling type, source and price?**

This derivative artifact provides stronger evidence than a later corporate history for at least one narrow point:

- by 2002, a SouFun Shanghai rental endpoint contained enough structured rental records for researchers to extract **251 cases** at one date;
- the extracted records differentiated district/location, dwelling configuration, source type and asking rent;
- therefore a structured online rental-information corpus existed before the 2005 graduate life slice examined in the companion repository.

It does **not** prove:

- how many Shanghai renters used it;
- whether the records were current;
- whether individual-landlord labels were truthful;
- whether contact details worked;
- whether a displayed unit was still vacant;
- whether an actual lease resulted;
- whether the site was accessible from every network/browser;
- whether a typical 2002 young renter had convenient Internet access.

The old-Web payoff is therefore **historical addressability evidence**, not transaction-outcome evidence.

---

## 4. Relation to the existing 2010 SouFun F-1 evidence

The existing canonical rental note already uses SouFun Holdings' 2010 SEC F-1 as A-level evidence. That filing says the company then maintained a very large database of secondary and rental residential listings and offered structured search/filter functions across many cities. It also admits problems such as duplicate listings, false properties/prices and agents posing as individual owners.

Source:

- SouFun Holdings Limited, Form F-1, filed 2010-09-02:  
  https://www.sec.gov/Archives/edgar/data/1294404/000095012310083390/h04135fv1.htm

The 2002 scholarly extraction and the 2010 F-1 should **not** be collapsed into a continuous unchanged interface history.

They support two separate moments:

```text
2002-08-27
specific Shanghai rental endpoint
→ derivative extraction says 251 records available to researchers

2010
company-wide filing
→ large multi-city structured listing/search business + explicit data-quality problems
```

What they jointly improve is the timeline:

> structured online rental information in SouFun's Shanghai environment is evidenced materially earlier than the 2010 filing.

What remains missing is a same-page/interface comparison.

---

## 5. New archaeological category: derivative-data survival

### 5.1 Why ordinary Web archives are not the only survival channel

A historical website can enter later evidence through several derivative routes:

```text
historical page
→ academic crawler / benchmark dataset
→ book table

historical page
→ search-engine index/cache

historical page
→ user screenshot/tutorial

historical page
→ software test fixture / saved HTML fragment

historical page
→ quoted forum/blog post
```

These routes can preserve content that a conventional replay system no longer exposes.

But every transformation may remove or alter context.

### 5.2 Minimum provenance fields for a derivative Web artifact

This probe proposes adding the following fields when future cases use such evidence:

```yaml
evidence_type: derivative-web-extraction
claimed_original_url:
claimed_observation_date:
derivative_created_at:
derivative_author:
derivative_purpose:
claimed_record_count:
preserved_fields:
selection_method:
transformation_or_recoding:
original_capture_available: false|true|unknown
original_parser_or_crawler_available: false|true|unknown
confidence:
```

For this object:

```yaml
evidence_type: derivative-web-extraction
claimed_original_url: http://sh.soufun.com/asp/rnl/leasecenter
claimed_observation_date: 2002-08-27
derivative_created_at: 2004 publication
claimed_record_count: 251
preserved_fields:
  - city district
  - address
  - apartment type
  - information source
  - monthly rental cost
selection_method: 20 cases described as randomly selected from 251 for the published sample
original_capture_available_in_this_run: false
original_parser_or_crawler_available_in_this_run: false
confidence: high for extraction claim; low/unknown for historical UI reconstruction
```

---

## 6. What derivative data can and cannot prove

### It can help prove

- an exact historical URL was used;
- a researcher accessed/extracted data at a claimed date;
- a corpus of at least the claimed scale was represented;
- certain information categories survived extraction;
- selected historical asking-rent records existed in the derivative corpus.

### It cannot by itself prove

- HTTP status;
- Content-Type;
- charset;
- HTML/DOM structure;
- frameset/table/CSS layout;
- JavaScript behavior;
- form action;
- URL parameters;
- cookies/session boundary;
- login requirements;
- image/subresource survival;
- browser requirements;
- what the original user literally saw;
- whether each record was genuine or current;
- whether a lease occurred.

Therefore:

```text
derivative dataset
!=
verified capture
```

and:

```text
published table
!=
historical screenshot
```

---

## 7. Archive probe in this run

Searches were run for the exact historical endpoint and Wayback/Internet Archive locators, including variants around:

```text
sh.soufun.com/asp/rnl/leasecenter
rent.soufun.com/asp/rnl/
```

This run did **not** obtain a search-result locator that could be opened and checked under `docs/METHOD.md`.

Structured negative result:

```yaml
object: SouFun Shanghai rental lease center
original_host: sh.soufun.com
original_url: http://sh.soufun.com/asp/rnl/leasecenter
period_claimed: 2002-08-27
locator_sources:
  - Pal & Shiu 2004 derivative extraction
archive_sources_checked:
  - public Web search for Wayback/Internet Archive locator
opened_capture: false
failure_class:
  - no_candidate_from_search_in_this_run
unknowns:
  - whether Internet Archive or another archive holds captures not surfaced by current search
  - historical Content-Type/charset
  - HTML/DOM
  - search form and URL parameters
  - scripts/subresources
  - browser assumptions
  - session/login boundary
next_action:
  - query archive indexes/CDX directly when a compatible archive-access route is available
  - test historical host/path variants
  - seek crawler/parser code or additional 2002-era tutorials/screenshots
```

Per repository method:

> `没有找到` **不得**写成 `当时不存在` 或 `Internet Archive 没保存`。

M1 status:

**NOT ACHIEVED IN THIS SLICE.**

---

## 8. Preservation bias introduced by scholarly extraction

Derivative survival creates a different bias from Wayback survival.

Researchers often extract only the variables useful to their own problem. In this case the CBR example preserved structured housing attributes and rent, because those were useful for similarity matching.

It may systematically discard things that matter for social history:

- page hierarchy;
- photographs;
- phone/email contact;
- posting date;
- descriptive prose;
- poster identity/account;
- neighborhood narrative;
- sorting/ranking;
- ads and paid placement;
- stale/removed state;
- platform warnings;
- comments or private messages.

Call this:

## **research-purpose selection bias / 研究用途选择偏差**

```text
what later research preserved
!=
what historical users considered important
```

The derivative artifact is valuable precisely because it preserves otherwise fragile data, but its preservation pattern was shaped by a machine-learning example, not by a historian trying to reconstruct renting.

---

## 9. Cross-national boundary

The companion life-history research checked Craigslist as an overseas comparison. A 2004 BusinessWeek interview with Jim Buckmaster records that in the late 1990s he used Craigslist to sell a futon, find apartments and post a résumé before Craig Newmark contacted him about work.

Source:

- BusinessWeek, 2004-09-08, preserved by Craigslist:  
  https://www.craigslist.org/about/press/craigslist.keeper

The comparison supports a shared Internet-era mechanism:

```text
classified/portal infrastructure
→ distant or stranger housing becomes searchable before offline contact
```

But platform architecture differs. Craigslist's broad classified categories and SouFun's vertical real-estate corpus should not be treated as the same product form.

For `old-web-archaeology`, the overseas object is boundary evidence only; it does not expand this repository beyond Chinese Web scope.

---

## 10. Claims ledger

| Claim | Evidence | Grade | Confidence |
|---|---|---:|---:|
| Pal & Shiu say they extracted 251 cases from the exact SouFun Shanghai URL on 2002-08-27 | 2004 Wiley book/chapter | B+ derivative | high |
| Their published sample preserves district/address/type/source/rent variables | reproduced Table 1.1 + explanation | B+ derivative | high |
| The original SouFun HTML had exactly those fields in exactly that structure | not available | — | unknown |
| SouFun's 2010 business had structured multi-city rental/secondary listings and known false/duplicate data problems | 2010 SEC F-1 | A | high |
| A verified 2002 archive capture was opened in this run | no | — | false |
| Internet Archive has no 2002 capture | not established | — | unknown |

---

## 11. Hindsight and reconstruction risks

Do not infer from the 2004 table that the 2002 page was:

- a modern searchable card UI;
- UTF-8;
- GBK/GB2312;
- IE-only;
- ASP in any specific server implementation beyond the URL string;
- a form with the same labels as the book's normalized columns;
- free of paid ranking;
- composed only of individual landlords and agents;
- accurate inventory.

The URL suffix `/asp/` is not enough to reconstruct application architecture.

Do not generate a “2002 SouFun screenshot” from the table and label it historical. Any future visual reconstruction must be explicitly marked `reconstruction` and keep the original interface unknown.

---

## 12. What this changes in the repository

Before this probe, the rental domain's strongest structured platform evidence in the canonical note was concentrated around SouFun's 2010 F-1 plus later/supplementary reporting.

This derivative artifact moves one part of the evidence chain earlier:

> **a specific Shanghai rental endpoint is tied to a dated 2002 extraction, an exact URL, a 251-record corpus claim, and preserved sample field data.**

More importantly, it changes the archaeological method itself:

> **When the original old-Web page is gone or unreplayable, the next question should not only be “is there another archive capture?” It should also be “did another contemporary system copy, index, measure, quote or transform this page?”**

That is a genuine preservation path — but it must remain a derivative artifact, never silently promoted into the historical original.
