# Digital Memorial / Profile / Guestbook / Account-Death State Gaps, 1998–2015

## Scope

This package stays inside the repository's main scope: approximately 1995–2015 Chinese-language Internet.

It does **not** turn `old-web-archaeology` into a global history of mourning or a general history of Chinese funerary culture. Pre-Web and overseas material belongs primarily in the paired `how-people-lived` topic and appears here only where it clarifies a technical or archival boundary.

Paired life-history research:

- `how-people-lived/topics/death-registration-online-mourning-digital-afterlife-and-posthumous-identity-china-1956-2026.zh-CN.md`

Research question:

> What exactly did a Chinese old-Web memorial page, guestbook, personal profile or social account prove about a person's death, identity, relationships and continuing online presence — and what crucial state was never on the public Web at all?

The main methodological claim is:

> **A memorial-looking page is not a death record; an account that remains online is not evidence the user remained alive; and a crawler that preserved the HTML shell may still have lost the most important memorial state.**

---

## 1. Object model: do not collapse these into “the memorial website”

At minimum distinguish:

```text
physical person
civil / medical identity record
death event
medical death certificate
kin / authorized reporter
platform account
login credential
personal profile
memorial-site user account
memorial record
memorial page URL
subject biography
portrait / photo object
music / Flash / animation asset
virtual grave / hall skin
virtual offering object
visitor session
guestbook message
comment moderation state
view counter
payment / virtual-item balance
notification / reminder state
search index entry
archive capture
```

These objects have different authorities and lifetimes.

A death certificate is strong evidence of a death event but says nothing about whether a memorial page existed.

A memorial page proves that a platform rendered a memorial representation, not that the platform independently verified the death.

A surviving profile URL proves neither that the user is alive nor that the account can still be logged into.

---

## 2. Core state gaps

### 2.1 Person / page gap

```text
person exists
!= memorial record exists
!= memorial page published
!= page indexed by search
!= page archived
```

Most deceased people in 2000s China never received a public Web memorial.

Therefore absence from old-Web corpora is not evidence of weak social importance, unusual family structure or lack of mourning.

### 2.2 Page-created / death-verified gap

```text
memorial page created
!= subject identity verified
!= creator authorized
!= subject actually deceased
```

A 2010 contemporaneous report described a living person discovering that a friend had created an online “grave” for him as a prank; the site removed it after contact.

Source (B / contemporaneous press):

- China News Service reprint, 2010-04-06:
  https://news.sohu.com/20100406/n271327157.shtml

This is a hard warning against treating any `memorial page` as a death-registry record.

### 2.3 Biography / authoritative-life-record gap

```text
name + dates + biography rendered
!= civil identity verified
!= dates verified
!= biography complete
!= biography neutral
```

Online memorials are relationship artifacts. Their text may be written by family, friends, journalists, strangers or site operators.

That subjectivity is historically valuable, but it is not administrative authority.

### 2.4 Registered account / memorial-author gap

```text
site account username
!= real-world identity known
!= kinship known
!= authority to represent deceased known
```

Some early Chinese memorial sites encouraged real names and detailed biographies; other users remained pseudonymous.

A 2008 contemporaneous profile of one Guangzhou user reported that the memorial for his deceased sister was the only place online where he used his real name.

Source (A/B):

- Southern Metropolis Weekly reprint, 2008-04-09:
  https://news.sina.com.cn/c/2008-04-09/164415322655.shtml

This makes memorial sites a useful counterexample to a simple “old Chinese Internet = pseudonymity” story.

### 2.5 Published page / executable ritual gap

```text
memorial HTML loads
!= virtual incense / candle control loads
!= Flash / JS executes
!= music asset loads
!= virtual offering can be submitted
!= guestbook accepts posts
!= payment endpoint works
```

A screenshot or archived HTML can preserve the appearance of a ritual while the executable ritual itself is dead.

### 2.6 Offering-click / offering-record gap

```text
button clicked
!= request reached server
!= server accepted request
!= offering record persisted
!= counter incremented
!= visitor later sees it
```

A rendered flower, candle or incense icon is not evidence of a completed historical interaction unless request/response or persisted state is independently available.

### 2.7 Guestbook-form / guestbook-message gap

```text
guestbook form visible
!= submission endpoint live
!= message accepted
!= message approved
!= message remained public
```

Moderation is especially important. A 2008 public memorial linked to a contested death accumulated many hostile comments and contemporaneous users alleged message deletion by administrators.

Source (B):

- Rednet reprint, 2008-10-18:
  https://news.sina.com.cn/c/2008-10-18/110116478945.shtml

An archive snapshot of the message list is therefore only one moderation state, not a complete record of everything submitted.

### 2.8 View-counter / unique-human gap

```text
page counter = N
!= N unique people
!= N mourners
!= N successful ritual acts
```

Counters may count refreshes, bots, repeated visitors or server-side rules unknown to us.

Do not turn old view counters into population estimates.

### 2.9 Free memorial / cost-free continuity gap

```text
memorial creation free
!= all decorations free
!= storage free
!= renewal free
!= long-term hosting guaranteed
```

2008 and 2010 contemporaneous reporting records paid memorial halls, paid virtual goods and annual maintenance models on some sites.

Sources:

- Xinhua reprint, 2008-04-05:
  https://news.sina.com.cn/c/2008-04-05/073615294595.shtml
- contemporaneous report, 2010-10-20:
  https://news.sina.com.cn/o/2010-10-20/113418259489s.shtml

The presence of a “permanent memorial” label must therefore be treated as a service promise, not demonstrated preservation durability.

### 2.10 Site-online / memorial-durable gap

```text
provider online at t1
!= provider online at t2
!= database preserved
!= uploaded photos preserved
!= guestbook preserved
```

A 2010 contemporaneous report quoted a former industry worker saying that some memorial providers withdrew when business was unsustainable and users' materials disappeared with server shutdown.

This produces **memorial-host dependency**: distance from the physical grave is reduced by adding dependency on the platform operator.

### 2.11 Account inactive / person deceased gap

```text
no login for months/years
!= deceased
```

and conversely:

```text
person deceased
!= platform has been informed
!= account state changed
```

This distinction becomes structurally important once personal SNS profiles persist for years.

### 2.12 Death reported / death accepted gap

```text
relative/friend reports death
!= evidence sufficient
!= platform accepts report
!= account enters protected/memorial state
```

This turns death itself into a platform state-transition requiring evidence.

### 2.13 Protected account / inherited account gap

```text
account protected after death
!= heir can log in
!= heir receives password
!= all account data transferable
```

Memorialization, protection, deletion and inheritance are different state transitions.

### 2.14 Account / embedded third-party privacy gap

```text
account belonged to deceased user
!= every message in account belongs solely to deceased
```

Private messages contain other people's communications. Any archaeology or inheritance model that treats an account as a single inheritable object risks collapsing multiple persons' privacy states.

---

## 3. Chinese Web transition, 1998–2004: dedicated memorial space appears before SNS death-state machinery

Contemporaneous 2007 reporting said Chinese online memorials had appeared by the late 1990s, though early growth was constrained by bandwidth, hardware and the small Internet population; it also reports official encouragement of online memorial practices by 2004.

Source (B for late-1990s retrospective claims; A for 2007 observed state):

- Xinhua reprint, 2007-04-03:
  https://tech.sina.com.cn/i/2007-04-03/10221446100.shtml

For archaeology, the key distinction is between at least three site families:

1. cemetery / funeral-service sites adding a Web memorial feature;
2. dedicated national memorial platforms;
3. later general portals / news sites adding temporary Qingming memorial features.

Do not infer identical account, payment, media or moderation architecture from the shared label `网上祭祀`.

---

## 4. 2007–2010: the memorial page becomes a compound media object

### 4.1 Simulated ritual was not “just text on a webpage”

A 2007 Shenzhen report describes a memorial site using interactive representations of flowers, matches, incense, tea and alcohol, with selectable grave backgrounds and tombstones.

- Xinhua reprint, 2007-04-03:
  https://tech.sina.com.cn/i/2007-04-03/10221446100.shtml

This suggests an archaeological target broader than DOM text:

```text
HTML shell
+ images
+ script / Flash-like interaction
+ media assets
+ user/session state
+ server-side memorial record
+ optional payment state
```

Without subresource recovery, an archive may preserve only a fraction of what contemporaneous users experienced.

### 4.2 The memorial could function as a distributed family / friend address

A 2008 Guangzhou user created a paid memorial after his sister's death partly so classmates and friends living elsewhere could participate.

- Southern Metropolis Weekly reprint, 2008-04-09:
  https://news.sina.com.cn/c/2008-04-09/164415322655.shtml

A 2010 report describes a student receiving an email from former classmates telling her that they had built a memorial page for a deceased teacher.

- contemporaneous report, 2010-04-02:
  https://news.sina.com.cn/o/2010-04-02/102417314856s.shtml

Technical consequence:

> Email, IM and portal links may be part of the memorial access path even when the memorial itself is a separate site.

The archive target should therefore include referrer/discovery evidence when available, not only the final URL.

### 4.3 Search changed the route into mourning

A 2010 interview describes an out-of-town student discovering an online memorial site through Web search, registering a free memorial, uploading photos and returning frequently.

- contemporaneous report, 2010-10-20:
  https://news.sina.com.cn/o/2010-10-20/113418259489s.shtml

This creates another state chain:

```text
need to mourn remotely
→ search query
→ result indexed
→ site reached
→ registration
→ memorial creation
→ media upload
→ repeat visit
```

A surviving memorial page cannot reconstruct the search engine rank or query that originally made it discoverable.

### 4.4 “Almost 100,000 visits” and “1,500 memorials” are event metrics, not adoption rates

A 2010 Rednet Qingming feature reported about 100,000 visits and more than 1,500 new memorials during a three-day event.

- Rednet reprint, 2010-04-06:
  https://news.sina.com.cn/o/2010-04-06/142717330845s.shtml

These numbers are platform-reported event counts. They do not establish:

- unique users;
- household adoption;
- substitution for cemetery visits;
- persistent use after Qingming;
- population share.

Keep them as platform-observable scale, not social prevalence.

---

## 5. Moderation, abuse and authenticity are first-class state

Dedicated memorial sites could be emotionally consequential precisely because pages looked authoritative and persistent.

Two contemporaneous failure modes are especially useful:

1. **unauthorized memorial creation** — a living person was given a prank “online grave” in 2010;
2. **hostile / contested guestbook content** — a 2008 memorial around a public controversy accumulated hostile comments and moderation disputes.

Therefore a historical memorial database should never be modeled as a neutral death registry.

Recommended fields for a reconstruction dataset:

```text
subject_claimed_name
subject_claimed_dates
creator_account
creator_real_identity_verified: yes/no/unknown
creator_relationship_claim
relationship_verified: yes/no/unknown
death_evidence_required: yes/no/unknown
death_evidence_type
moderation_model
comment_preapproval: yes/no/unknown
comment_delete_capability
memorial_delete/appeal process
```

Do not fill unknown fields from later site policies.

---

## 6. SNS transition: the old problem reverses

Dedicated memorial sites asked:

> “Who will create a page for the deceased?”

SNS later asks:

> “A page already exists. What happens to it after the person dies?”

This inversion is technically important.

A general SNS profile may already contain:

- years of posts;
- comments and replies;
- friend graph;
- private messages;
- tagged photos;
- birthday metadata;
- recommendation eligibility;
- login/recovery phone or email;
- third-party app links.

The death transition can therefore modify some state while preserving other state.

Overseas comparison is useful only as a model boundary: Facebook's 2009 memorialization policy required death evidence, disabled future login and retained a memorial profile for friends. It was partly motivated by algorithms recommending that users reconnect with deceased friends.

- The Guardian, 2009-10-27:
  https://www.theguardian.com/technology/2009/oct/27/facebook-user-memorials

This is **not** evidence that Chinese SNS had the same feature at the same date. It demonstrates a common platform-class problem once social graphs persist beyond biological death.

---

## 7. What belongs in 2010–2015 Chinese old-Web follow-up

The current slice did not yet establish a full M1 chain for Chinese SNS death handling before 2015.

Priority targets:

1. Sina blog / Sina Weibo historical help or community-rule pages concerning deceased accounts;
2. Tencent QQ / Qzone historical account-retention and recovery rules;
3. Renren or Kaixin profile persistence after death, if primary contemporaneous documentation can be located;
4. dedicated memorial-site terms describing death verification, creator authority and deletion appeals;
5. memorial sites' media stacks: charset, JS, Flash, background music and upload endpoints;
6. payment / virtual-offering flow if it can be verified without exposing user financial records.

Do not use the 2020 Weibo deceased-account policy to backfill 2012 rules.

---

## 8. Archive-specific preservation asymmetries

### 8.1 Memorial-shell / interaction-loss asymmetry

Likely to survive:

- title;
- subject name;
- biography text;
- static CSS;
- some image URLs;
- navigation labels.

Likely to disappear or become unreplayable:

- virtual incense / candles;
- Flash objects;
- background audio;
- dynamic guestbook pagination;
- counters;
- AJAX submissions;
- paid virtual offerings;
- login/session state.

### 8.2 Biography-survival / relationship-loss asymmetry

A memorial biography may remain while the visitor network disappears.

The archive can then make remembrance look like a single author's static text even if contemporaneous meaning depended on many people returning, posting and interacting.

### 8.3 Public-memorial / private-message authority inversion

The most archive-friendly artifacts are public memorial pages.

The strongest evidence of an actual relationship may be private email, QQ messages or direct correspondence — exactly the materials that should **not** be recovered or republished merely because they would strengthen historical interpretation.

Privacy minimization therefore reduces evidentiary completeness by design. That is acceptable.

### 8.4 Page-survival / provider-database-loss asymmetry

A crawler may save one public page even after the original provider database later disappears; conversely, a provider may retain a database while robots/session restrictions prevent archive access.

Therefore:

```text
Wayback page absent
!= provider had no data
```

and:

```text
one archived page survives
!= memorial service as a whole survives
```

### 8.5 Account-presence / login-authority-loss asymmetry

A profile page can remain publicly visible after login credentials, recovery phone numbers, authentication hosts or account-owner status have changed or disappeared.

Do not interpret `profile URL still renders` as `account is still operational`.

---

## 9. Recommended state machine

For a dedicated memorial site:

```text
UNSEEN
  → SITE_DISCOVERED
  → ACCOUNT_CREATED
  → MEMORIAL_DRAFTED
  → SUBJECT_DATA_SUBMITTED
  → [DEATH_EVIDENCE_REQUIRED?]
  → PUBLISHED
  → INDEXED
  → VISITED
  → OFFERING_SUBMITTED / GUESTBOOK_SUBMITTED
  → [MODERATION_PENDING]
  → PUBLIC_INTERACTION_VISIBLE
  → UPDATED / RENEWED
  → SUSPENDED / DELETED / PROVIDER_OFFLINE
```

For a pre-existing SNS profile:

```text
ACTIVE_USER
  → PERSON_DIES
  → ACCOUNT_UNCHANGED
  → DEATH_REPORTED
  → EVIDENCE_PENDING
  → DEATH_CONFIRMED_BY_PLATFORM
  → PROTECTED / MEMORIALIZED / DELETED
  → LONG_TERM_RETENTION / EVENTUAL_REMOVAL
```

These two state machines should not be collapsed.

---

## 10. Evidence table for this slice

| Claim | Evidence | Grade | Limits |
|---|---|---:|---|
| Chinese online memorials existed by late 1990s and were still constrained by network/hardware conditions | 2007 Xinhua retrospective | B/C | not an M1 capture |
| 2007 Shenzhen memorial service exposed interactive virtual ritual objects | 2007 Xinhua report | A/B | platform claims about visitor counts need caution |
| A 2008 user used a memorial to connect geographically dispersed friends/classmates | 2008 Southern Metropolis Weekly interview | A/B | individual path, not prevalence |
| Some services charged for memorial creation, decoration or maintenance | 2008/2010 contemporaneous reports | A/B | site-specific prices |
| A living person could be memorialized without adequate verification | 2010 China News Service report | A/B | failure case, not normal frequency |
| Provider shutdown could destroy user memorial material | 2010 report quoting former worker | B | needs primary shutdown case for stronger chain |
| SNS class of service eventually requires death-specific account state | Facebook 2009 comparison | A/B overseas | not Chinese-platform evidence |

---

## 11. Memento / archive status

This run searched for leads around late-1990s–2010 Chinese memorial platforms and contemporaneous news references.

However, it did **not** obtain a historical capture that can satisfy the repository's M1 contract across:

- original URL;
- capture URL;
- capture datetime;
- HTTP status;
- charset;
- DOM;
- major media/script dependencies;
- guestbook or ritual endpoint behavior;
- a second time point for state comparison.

Therefore record exactly:

> **M1 verified historical Chinese online-memorial capture: NOT ACHIEVED IN THIS SLICE.**

Do not rewrite this as “Wayback did not preserve it.”

Do not infer IE version, GB2312/GBK, Flash usage, form action or database technology merely from the year or visual descriptions in press reports.

---

## 12. What this changes in old-Web archaeology

Old-Web preservation often privileges pages that appear self-contained.

Online memorials show why that is dangerous.

A static page can look unusually durable — name, dates, portrait, biography — while the historically important state may have been elsewhere:

- who had authority to create it;
- whether death was verified;
- how remote friends discovered it;
- whether virtual ritual controls actually worked;
- which guestbook messages were moderated away;
- whether paid renewal kept the page alive;
- whether the provider database later disappeared;
- whether the deceased's ordinary SNS profile remained active somewhere else.

The archival lesson is therefore:

> **The Web can preserve a representation of death while losing the transaction, moderation, relationship and identity states that made that representation socially meaningful.**

And for life history:

> **Digital life does not end at logout. Once a person's ordinary identity is distributed across sites and accounts, death becomes a cross-system state transition that may never complete everywhere at the same time.**
