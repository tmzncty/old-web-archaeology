# Cohabitation, “fact marriage,” and legal-vocabulary drift on the Chinese old Web, 2001–2007

> Status: research checkpoint. This note does **not** reconstruct an early marriage/legal-advice Web application. It isolates a different old-Web problem: a page can survive perfectly as text while the meaning and legal validity of its relationship labels change underneath it.
>
> Companion life-history slice: [`tmzncty/how-people-lived/sources/unregistered-cohabitation-fact-marriage-shared-home-and-relationship-credentials-china-1989-2023.zh-CN.md`](https://github.com/tmzncty/how-people-lived/blob/main/sources/unregistered-cohabitation-fact-marriage-shared-home-and-relationship-credentials-china-1989-2023.zh-CN.md)
>
> M1 historical Web artifact status: **NOT ACHIEVED IN THIS SLICE**. The pages below are current live legacy representations carrying 2005–2007-dated text, not verified replay captures of their original DOM/HTTP/charset state.

## 0. Why this note clears the repository’s de-duplication threshold

The repository already has many variants of:

```text
page exists != transaction succeeds
current shell != historical artifact
label exists != status confirmed
```

A generic “legal Web pages can be outdated” note would be duplicate expansion.

This checkpoint is narrower and adds a preservation / interpretation failure mode not yet separately modeled:

> **semantic survival without normative validity**.

The page body, URL, date and title may all survive, yet a legal/social label on the page may no longer mean what a modern reader thinks it means—or may already have been disputed on the very day the page was published.

The concrete case is the post-2001 Chinese Web vocabulary around:

- `非法同居`;
- `同居关系`;
- `事实婚姻`;
- `有配偶者与他人同居`;
- media vernacular `试婚`.

This matters because old-Web corpus search is unusually vulnerable to treating words as stable categories across time.

---

## 1. Legal chronology needed before reading the Web corpus

### A. 2021 court-system retrospective explanation

Shandong courts host a page attributed to the Supreme People’s Court Civil Adjudication No. 1 Tribunal and sourced to its commentary on the Civil Code marriage-family judicial interpretation:

- 2021-11-10, 《事实婚姻的效力》
- <https://www.sdcourt.gov.cn/jningweisfy/385991/385992/7914350/index.html>

Evidence class: **A-/B+ for legal-history interpretation**, not an original 1994 Web artifact.

It records a changing regime:

- the 1989 judicial opinion used `非法同居关系` for certain unregistered unions;
- the 1994-02-01 Marriage Registration Administration Regulation treated unregistered people living publicly as husband and wife as lacking valid marital status;
- later Marriage Law / judicial-interpretation rules used a conditional approach for pre-1994 relationships and emphasized registration / supplementary registration.

The important archaeological point is not to rewrite all legal detail here. It is to establish that:

```text
term meaning at 1989
!=
term meaning at 1994
!=
term usage after 2001
```

### B. 2006 Jiangsu court article

Jiangsu Court Network, 2006-04-25, 《同居与重婚界定标准概论》:

- <https://www.jsfy.gov.cn/article/86101.html>

Evidence class: **B+ — contemporaneous court-system legal discussion**.

It explicitly says that after the Marriage Law judicial interpretation (II), from 2004-04-01 ordinary requests merely to dissolve a cohabitation relationship were generally no longer accepted by courts, except specified married-person-with-another cases; disputes over property / children remained a different matter.

This is enough to establish that a 2006 page containing `同居` cannot be interpreted by importing the 1989 `非法同居` category wholesale.

---

## 2. Concrete old-Web evidence: the obsolete label was still alive on the Web

### A. 2005 Guangzhou Daily / Sina: the Web itself is named as a carrier of the old term

Current live legacy representation:

- Sina News, displayed date 2005-10-12;
- source shown as 大洋网-广州日报;
- title: 《“同居”何来“非法”？》;
- <https://news.sina.com.cn/o/2005-10-12/10467148472s.shtml>

Evidence class:

- **A for the current observable legacy page state**;
- **B+ for the 2005-dated contemporaneous argument carried by that text**;
- **not A-grade evidence for the original 2005 HTML/HTTP/charset/browser state**.

The article argues that `非法同居` had an older legal basis in the 1989 judicial opinion, but that the 2001 and 2003/2004 judicial interpretations had shifted wording to `同居关系` and stopped treating ordinary unmarried cohabitation as a relation courts simply dissolve on request.

Most valuable for old-Web method: the 2005 writer explicitly comments that entering `非法同居` into an Internet search engine still produced “thousands” of related URLs.

The exact search engine, date/time, query syntax and result count were not preserved in this slice, so **do not quote that as a reproducible corpus measurement**.

But as a contemporaneous observation it establishes a historically important phenomenon:

```text
legal vocabulary changes
→
older wording remains abundant and searchable online
```

Working term:

> **lexical fossilization / 词汇化石化**

### B. 2006 dated Sina page still uses the old umbrella label as if current

Current live legacy representation:

- Sina mobile, displayed date 2006-08-29;
- source displayed as 大众网-农村大众;
- title: 《非法同居与重婚之法律相关》;
- <https://news.sina.cn/sa/2006-08-29/detail-ikknscsk0868514.d.html>

Evidence class: **A for current page state; B for period-dated legal/media discourse**.

The article continues to classify unregistered cohabitation through `非法同居` vocabulary and mixes this with valid statutory discussion of `有配偶者与他人同居`.

For archaeology, that is more important than deciding whether the journalist’s doctrinal summary was perfect:

> **different surviving 2005–2007 pages did not converge on one synchronized vocabulary after the legal-language shift.**

### C. 2007 Sohu page performs the contradiction inside one document

Current live legacy representation:

- Sohu News, displayed date 2007-03-23;
- title: 《不卖淫 不嫖娼 未婚同居合法？非法？》;
- <https://news.sohu.com/20070323/n248910703.shtml>

Evidence class: **A for current legacy page state; B for contemporaneous media/legal discourse**.

The article says a lawyer explained that the word `非法` was no longer used from the 2001 judicial interpretation onward. Yet the same article still contains older/casual expressions such as `解除非法同居` when narrating a case.

This is a useful warning:

```text
one page
can contain
multiple semantic vintages
```

A bag-of-words corpus model will flatten them into one category.

---

## 3. New preservation mechanism: semantic survival without normative validity

Old-Web preservation is usually discussed as loss:

- URL dies;
- body disappears;
- image breaks;
- script no longer runs;
- charset corrupts.

This case shows the reverse problem:

> **the text survives too well.**

A 2005 or 2007 article can remain fully indexable in 2026. A searcher asking a current legal question may land directly on it.

So:

```text
page still accessible today
!=
page is current advice

historical term survives in title
!=
term remains a valid current legal category

text preservation success
!=
semantic-currentness success
```

Working term:

> **normative-version drift / 规范版本漂移**

The object has been preserved, but its interpretation requires a date-aware legal/social vocabulary layer that an ordinary archive replay does not automatically provide.

---

## 4. New archaeological failure mode: search-result anachronism

Search engines intentionally surface relevant old pages without requiring the user to think historically.

A modern query such as:

```text
非法同居
事实婚姻
同居八年算夫妻吗
```

may return:

- a 2005 opinion arguing the term is obsolete;
- a 2006 article still using it as a broad category;
- a 2007 legal Q&A mixing new and old terms;
- a modern court explanation of the 1994 cutoff.

All four can appear on one modern result page.

Therefore:

> **SERP adjacency != semantic contemporaneity**.

Suggested field for future evidence records:

```yaml
semantic_version:
  term_as_printed: "非法同居"
  page_display_date: 2005-10-12
  speaker/source: "commentary/article/title/quoted law"
  legal_regime_referred_to: "1989 opinion / 2001 interpretation / unknown"
  term_status_on_page_date: "contested/legacy/current/unknown"
  current_term_status: "historical/limited/context-dependent/unknown"
```

This must remain separate from artifact fields such as capture datetime, Content-Type and charset.

---

## 5. Historical word frequency is not historical behavior frequency

The 2005 article’s “thousands of URLs” observation is tempting for digital history, but unsafe.

A large number of pages matching `非法同居` could include:

- old law reproduced verbatim;
- news about a university rule;
- pages criticizing the phrase;
- lawyer explanations saying the phrase is outdated;
- duplicate portal syndication;
- court cases involving a married person and another partner;
- unrelated moral commentary;
- scraped copies created years later.

Therefore:

```text
URL count containing “非法同居”
!=
number of cohabiting couples
!=
number of unlawful relationships
!=
number of pages endorsing the category
```

Working term:

> **lexical prevalence / behavioral prevalence split**.

A historical search-frequency project must sample and classify **usage function**, not just term presence.

Suggested `usage_function` values:

```yaml
usage_function:
  - governing_rule_quote
  - obsolete_rule_quote
  - page_author_category
  - headline_hook
  - quoted_speaker
  - critique_of_term
  - search_query_or_question
  - navigation_taxonomy
  - unknown
```

---

## 6. Title vocabulary is not body legal conclusion

The 2007 Sohu case is especially useful because its title deliberately stages `合法？非法？`, while the body explains that the simple `非法同居` label had already been challenged / dropped in judicial wording.

This yields a rule different from the repository’s earlier accidental metadata/body mismatch case:

> **headline vocabulary may be rhetorically historical even when the body’s legal conclusion rejects it.**

So:

```text
H1/token hit
!=
author conclusion
```

This is not page corruption. It is a genuine feature of journalism and legal popularization.

For corpus work, store separately:

```yaml
term_location:
  title: true
  deck: false
  body_author_voice: true
  quoted_law: true
  quoted_interviewee: false
```

Without location and speaker attribution, historical NLP will turn debate into consensus.

---

## 7. “事实婚姻” is a time-indexed status, not a plain synonym for cohabitation

Modern ordinary-language pages often use `事实婚姻` to mean “they lived like husband and wife for a long time.”

But court-system explanations make the 1994-02-01 cutoff central to civil recognition.

Therefore old-Web extraction needs this hard boundary:

```text
text says “事实婚姻”
!=
relationship legally recognized as fact marriage
```

A claim record should ideally include:

```yaml
relationship_claim:
  cohabitation_start_date: known/unknown
  registration_exists: yes/no/unknown
  public_spouse_presentation: yes/no/unknown
  substantive_marriage_conditions: confirmed/probable/unknown
  legal_status_claimed_by_page: fact_marriage/cohabitation/unknown
  legal_status_independently_verified: confirmed/probable/unknown
```

For life history, this is a major difference: two couples with almost identical households can have different institutional exit, property and status procedures because one relationship began before a legal cutoff and another after it.

---

## 8. Another boundary: actor language is evidence even when doctrine is wrong

The goal is **not** to normalize every old page into modern terminology and erase the old wording.

A 2006 reporter using `非法同居` may be doctrinally imprecise, but the mistake is itself historically valuable evidence of:

- ordinary legal vocabulary;
- moral stigma;
- lag between judicial language and mass-media language;
- how a user in 2006 would phrase a search query.

Thus retain both:

```yaml
actor_term: "非法同居"
normalized_research_category: "unregistered cohabitation; exact legal status unresolved"
```

Do **not** silently replace the historical actor’s word with the modern category.

---

## 9. Cross-source chronology table

| Date | Surviving source | What the page says / demonstrates | Safe archaeological use |
|---|---|---|---|
| 2005-10-12 | Guangzhou Daily text on Sina | argues `非法同居` is obsolete as a general label; says search engines still return many such pages | contemporaneous evidence of lexical lag; current legacy representation |
| 2006-04-25 | Jiangsu Court Network | explains post-2004 handling of ordinary cohabitation cases | contemporaneous court-side semantic/legal context |
| 2006-08-29 | Sina / Rural Masses | still uses `非法同居` as broad organizing term | evidence of unsynchronized mass-media vocabulary |
| 2007-03-23 | Sohu legal report | title asks legal/illegal; body says `非法` wording had been dropped, while still reusing old phrase in case narration | within-document mixed semantic vintages |
| 2021-11-10 | Shandong court / SPC Civil I commentary | reconstructs legal treatment of fact marriage and 1994 cutoff | current authoritative-ish retrospective normalization, not historical Web state |

This is a **semantic chronology**, not a capture chronology.

---

## 10. Current artifact-state observations and their limits

In this run, the following dated articles were directly recoverable as current live pages through search/open:

- 2005 Sina;
- 2006 Jiangsu court;
- 2006 Sina mobile;
- 2007 Sohu.

What this establishes:

```yaml
current_live_legacy_representation: true
period_date_displayed: true
text_body_accessible_now: true
```

What it does **not** establish:

```yaml
historical_capture_opened: false
original_2005_2007_dom_verified: false
original_http_status_verified: false
original_content_type_verified: false
original_charset_verified: false
original_css_js_verified: false
original_link_graph_verified: false
second_historical_timepoint_verified: false
```

Do not infer IE requirements, GB2312/GBK, frames, table layout, portal navigation or ad scripts from era stereotypes.

---

## 11. M1 status

```yaml
object: Chinese Web cohabitation / fact-marriage legal-language pages
period_target: 2001-2007
current_live_legacy_pages_opened: true
verified_timestamped_historical_archive_capture_opened: false
second_verified_historical_timepoint: false
m1_status: NOT ACHIEVED
```

This result must **not** be rewritten as:

> “Wayback did not preserve these pages.”

The archive-discovery question remains open.

---

## 12. Why this matters to ordinary-life history

The companion HPL slice shows that ordinary life could contain:

```text
shared home
+
shared expenses
+
family recognition
+
possibly children
-
marriage registration
```

The old Web then adds another layer: the words a person used to understand that life were themselves changing.

A 2005 user might search `非法同居`; a 2010 lawyer might prefer `同居关系`; a family might call two people `夫妻`; a court might ask whether the relation began before 1994 and whether marriage conditions were satisfied.

So:

> **historical relationship status is not recoverable from a single keyword.**

This is exactly the kind of life-history / interface intersection the two repositories need to preserve.

---

## 13. Suggested method addition for future old-Web cases

For legal, welfare, household, employment and credential pages, add a **semantic validity window** next to artifact provenance:

```yaml
semantic_context:
  printed_term: ""
  term_location: title/body/navigation/form/quoted_text
  actor_using_term: ""
  page_date: ""
  rule_effective_date_referenced: ""
  governing_rule_at_page_date: confirmed/probable/unknown
  term_was_current_at_page_date: confirmed/probable/unknown
  term_is_current_today: confirmed/probable/unknown
  research_normalization: ""
```

This prevents two opposite mistakes:

1. **presentism** — erasing historical actor language because it sounds wrong today;
2. **archive literalism** — treating every preserved historical label as a timeless legal fact.

---

## 14. Counterexamples and caution

### 14.1 Old terminology does not automatically mean the page was “wrong”

A page may quote an old rule for history, discuss a specific earlier relationship, or use a provocative headline. Classification requires local reading.

### 14.2 New terminology does not guarantee doctrinal accuracy

A page saying merely `同居关系` can still misstate property, child or marriage rules.

### 14.3 Legal-status research must not collapse civil and criminal contexts

`事实婚姻`, `有配偶者与他人同居`, and possible bigamy questions have different elements. The same colloquial phrase can behave differently across legal domains.

### 14.4 Syndication is not independent corroboration

If one Guangzhou Daily article appears on five portals, that is one evidence family unless independent reporting is demonstrated.

---

## 15. What would count as the next artifact advance

High-value next steps:

1. open a verified 2001–2007 historical archive capture of one legal-advice or marriage portal page;
2. record capture datetime, historical URL, response/replay state, Content-Type, charset and DOM;
3. recover a historical navigation taxonomy showing whether `非法同居`, `事实婚姻` or `同居关系` was used as a site category rather than merely article text;
4. find the same page/site at a second time point to test whether labels changed after 2001/2004 legal-language shifts;
5. compare historical search-engine or portal index snippets if trustworthy captures survive.

A particularly valuable case would be a legal portal that changes its navigation/category label over time while retaining old article bodies.

---

## 16. Saturation status

This slice adds a new preservation/interpretation mechanism:

- **lexical fossilization**;
- **normative-version drift**;
- **search-result anachronism**;
- **lexical prevalence ≠ behavioral prevalence**;
- **mixed semantic vintages inside one surviving page**.

It also supports a newly identified ordinary-life pathway in HPL: shared household without the standard marriage credential.

Therefore this run is **not** a no-new-mechanism run. Cross-project saturation remains **0/3**.
