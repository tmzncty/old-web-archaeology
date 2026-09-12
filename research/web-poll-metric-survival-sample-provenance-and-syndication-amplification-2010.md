# Web poll metric survival, sample provenance and syndication amplification (China, 2010)

> Status: research note / evidence checkpoint. This is **not** an M1 complete case and does not claim to reconstruct an original 2010 poll interface.
>
> Scope: one narrow old-Web archive problem exposed by contemporaneous employment and housing polls: **the percentage may survive after the questionnaire, recruitment path and original poll page have disappeared from the readily inspectable record.**

## 0. Why this note exists

This repository already contains many state-gap notes about applications, profiles, payments and offline completion. Adding another `poll page != social reality` note would be redundant.

The distinct archaeological issue here is evidence survival:

```text
reported metric survives
!=
original questionnaire survives
!=
original response set survives
!=
sampling / recruitment contract survives
!=
population prevalence is known
```

A second problem is syndication:

```text
1 agency / newspaper article
→ copied by several portals
→ several surviving URLs
!=
several independent evidence families
```

This matters directly to research that uses old Web polls as contemporaneous evidence for how people imagined work, housing and the future.

---

## 1. Case A: 2010 job-hopping / “裸辞” metrics

### 1.1 What survives

A 2010-12-24 China Youth Daily article survives today through multiple portal representations. The surviving text says:

- Zhaopin / 智联招聘 ran a `2010年秋季跳槽特别调查` with more than 8,000 workplace respondents;
- 25.8% reportedly said they had already completed a job change;
- about 60% reportedly had job-changing intentions;
- a separate poll jointly run by several media outlets, including Beijing News / 新京报, reportedly found that 56.96% of participating netizens had previously “裸辞”.

Current accessible representations include:

- Sina News, dated 2010-12-24, source 中国青年报:  
  https://news.sina.com.cn/s/2010-12-24/080821699439.shtml
- Sina Education, dated 2010-12-24:  
  https://edu.sina.com.cn/j/2010-12-24/1001197837.shtml
- Dazhong / 大众网, dated 2010-12-24:  
  https://edu.dzwww.com/dzjyxw/jyzytt2/201012/t20101224_6050316.html

A separate 2010-11-02 News Evening / 新闻晚报 article, currently accessible through Sohu, describes Zhaopin’s survey as an 8,000-person, three-week investigation and gives a more detailed distribution: 25.8% completed a job change, 30.3% had already started looking, more than 30% had thoughts but had not acted, and 8.7% said they had no job-changing plans.

- Sohu News, 2010-11-02:  
  https://news.sohu.com/20101102/n276996824.shtml

### 1.2 Evidence grade

**Grade B:** contemporaneous media descriptions of a platform survey.

The current pages are useful evidence that these metrics were being publicly reported in 2010. They are **not** proof that the current DOM, template, charset, scripts or URL structure are the historical page representation seen by a 2010 reader.

The three China Youth Daily syndications above are one content lineage, not three independent confirmations of the underlying poll.

### 1.3 What has not been recovered in this slice

This run did **not** successfully recover and inspect:

- the original Zhaopin survey landing page;
- the original questionnaire;
- the exact field dates from a first-party artifact;
- recruitment / sampling method;
- login requirements or duplicate-vote controls;
- whether `8000余名` means completed questionnaires after cleaning or all submissions;
- the original Beijing News / multi-media `56.96%` poll page;
- its denominator beyond the media description of participating netizens;
- its question wording and answer options;
- an archive capture with verified `capture_datetime`, historical HTTP/replay state, charset, DOM and form behavior.

Therefore:

```text
56.96% of participating netizens in a reported poll
!=
56.96% of Chinese workers
!=
56.96% of Chinese white-collar workers
```

---

## 2. Case B: 2010 housing poll — a second domain with the same preservation asymmetry

A 2010-01-15 Chu Tian Metropolis Daily report, currently preserved by Sina, says that more than 12,000 Wuhan SouFun / 搜房网 users participated in an online poll about post-1980 home buying. The report gives several precise figures, including 56.96% saying their down payment received parental support, 10.13% saying parents supported both down payment and mortgage, and 24.05% saying funds came from their own savings / bank deposits.

Current representation:

- Sina News, dated 2010-01-15, source 楚天都市报:  
  https://news.sina.com.cn/o/2010-01-15/063716936312s.shtml

**Grade B:** contemporaneous media reporting of an online platform poll.

This source is useful because the report itself says it was an online poll and gives an approximate response count. It still does not establish a probability sample of Wuhan’s entire post-1980 cohort.

The coincidence that this housing report and the separate naked-resignation report both contain `56.96%` is **not evidence of a shared dataset, a calculation error or copying**. They concern different questions and platforms. This note records the coincidence only to prevent a future researcher from inferring a relationship without evidence.

### 2.1 What this second case adds

The archive problem is not specific to career polls. Old portal news can preserve:

- a platform name;
- a poll date or publication date;
- a response count;
- exact percentages;
- journalist interpretation;

while the original interactive instrument is much harder to inspect years later.

That produces **`metric survival / instrument loss`** across domains.

---

## 3. Proposed terminology

### 3.1 `metric survival / instrument loss`

A numeric result survives in a report or syndicated article, while the original questionnaire / poll form / recruitment context is unavailable or unverified.

### 3.2 `syndication amplification`

The same article is copied to several portals, producing several searchable URLs and making a claim look more independently corroborated than it is.

### 3.3 `denominator opacity`

The surviving result states a percentage but does not preserve enough information to reconstruct the target population or the exact respondent eligibility / completion rules.

### 3.4 `interface-loss bias`

Later researchers see the final number but not what a participant actually saw: question order, answer choices, default selections, login requirements, anti-duplicate logic, surrounding editorial framing and poll placement.

---

## 4. Minimum evidence fields for historical Web polls

When a future case uses a historical Web poll, record at least:

| Field | Meaning |
|---|---|
| `poll_platform` | site / host that actually collected responses |
| `poll_title` | original title if verified |
| `question_text` | exact question only if artifact verifies it |
| `answer_options` | full answer set if verified |
| `field_start` / `field_end` | response period, not article publication date |
| `reported_n` | response count and whether approximate |
| `target_population_claimed` | who the article says the poll is about |
| `recruitment_method` | homepage opt-in, registered users, email invite, etc. |
| `eligibility_rule` | who was allowed to respond |
| `duplicate_control` | cookies, account, IP, none, unknown |
| `original_url` | original poll / result URL |
| `archive_source` | Wayback, WARC, current legacy page, media report, etc. |
| `capture_datetime` | only when actually verified |
| `syndication_family` | which surviving pages copy the same source text |
| `metric_definition` | what numerator / denominator actually mean |
| `unknowns` | explicit missing fields |

Unknown must remain `unknown`; do not infer a questionnaire from a journalist’s prose summary.

---

## 5. Claim rules for old-Web poll evidence

Prefer:

> A 2010 contemporaneous article reported that more than 8,000 respondents participated in a Zhaopin job-hopping survey and that 25.8% said they had already changed jobs.

Avoid:

> In 2010, 25.8% of Chinese white-collar workers changed jobs.

Prefer:

> A Wuhan SouFun online poll reported parental down-payment support among its participating users.

Avoid:

> 56.96% of Wuhan’s entire post-1980 generation relied on parents for down payments.

The distinction is not pedantry. It separates **platform-observable sentiment** from **population prevalence**.

---

## 6. Historical visibility consequence

Old Web research has a structural temptation:

```text
searchable percentage
> searchable methodology
```

Numbers are copied into headlines, year-end roundups and later retrospective articles. Poll widgets, result endpoints and interactive forms are more likely to disappear, move behind scripts, or depend on backend state that was never archived.

As a result, the historical record can become **more numerically precise while becoming methodologically less reconstructable**.

This is a useful warning for life-history research: a very precise old percentage may deserve *less* confidence than a less precise but well-provenanced first-person account, depending on the claim being made.

---

## 7. Relationship to `how-people-lived`

Cross-research package:

- `tmzncty/how-people-lived/sources/contemporaneous-job-exit-runway-naked-resignation-and-cash-buffer-optionality-china-2007-2024.zh-CN.md`

The HPL package uses the 2010 survey only to show that job-changing / naked-resignation discourse and platform polling were publicly visible. It does **not** use the poll share as a national prevalence estimate.

This OWA note explains why that evidence discipline is necessary.

---

## 8. Negative result / M1 status

This slice did not obtain a verified historical capture of the original Zhaopin 2010 survey interface or the original multi-media naked-resignation poll.

Therefore:

**M1 historical poll-interface capture: NOT ACHIEVED IN THIS SLICE.**

This means only that the present research run did not successfully open and validate such a capture. It does **not** mean that Internet Archive, another archive, a private collection or an old browser cache contains no copy.

A future successful artifact probe should inspect at minimum:

- original host and URL;
- capture datetime;
- HTTP / replay status;
- charset and Content-Type;
- question text and answer options;
- form action / script endpoint if preserved;
- login / cookie / duplicate-control clues;
- result page behavior;
- at least a second historical timepoint if the case is to count toward M1.

---

## 9. What this changes in old-Web archaeology

The missing thing is sometimes not a page image or CSS file. It can be the **measurement contract** behind a number that survives everywhere.

A historical Web poll leaves at least four separable artifacts:

```text
poll interface
→ response database
→ result summary
→ syndicated media number
```

The last object may survive after the first three are gone.

For research on ordinary life, that means a surviving percentage must be treated as an artifact with its own provenance, not as a transparent window onto an entire generation.
