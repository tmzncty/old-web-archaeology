# Online matchmaking profile, filter, identity-verification and offline-relationship state gaps, China 2003–2015

## Scope

This is a **Chinese old-Web companion**, not a general history of courtship or marriage.

Primary scope: approximately **2003–2015**, when Chinese dating/matchmaking sites increasingly exposed:

- structured personal profiles;
- candidate search/filtering;
- internal messages and paid communication;
- optional or mandatory identity verification;
- online/offline matchmaking events;
- public success narratives;
- cross-city partner discovery.

Earlier newspaper personal ads, marriage agencies and overseas pre-Web systems are boundary context only. Post-2015 mobile apps, WeChat mini-programs and the 2025 nationwide marriage-registration reform belong mainly in the companion `how-people-lived` topic.

Cross-project companion:

- `tmzncty/how-people-lived/topics/matchmaking-personal-ads-searchable-mates-and-marriage-executability-china-1981-2026.zh-CN.md`

## Why this belongs in old-Web archaeology

A historical matchmaking page looks deceptively legible.

A surviving page may show:

- a profile;
- a user count;
- a search form;
- a verification badge;
- a message button;
- a platform claim that a couple succeeded.

None of those states automatically proves that two people actually formed a relationship.

A useful minimum rule is:

> `profile visible != person available != message received != mutual interest != offline meeting != relationship != marriage`

Online matchmaking is therefore a strong case for separating a **browser-visible control plane** from a largely unarchived private/offline relationship process.

---

## 1. Evidence contract

Repository method applies without exception:

- platform / host / account / page / capture / claim are distinct;
- `exists`, `available`, `used`, `popular` and `caused` must not be collapsed;
- platform registration counts are platform claims unless independently audited;
- a historical URL in a contemporaneous article is a locator, not a verified capture;
- a verified legal identity does not make every profile field true;
- a platform success story is not automatically independent evidence of marriage;
- ordinary historical dating profiles carry unusually high privacy risk and should not be republished simply because an archive exposes them.

### Grades used in this note

- **A**: contemporaneous official/legal text or a sufficiently identifiable original technical artifact.
- **A-content**: official/institutional historical-dated content still hosted today, where original historical Web rendering has not been verified.
- **B**: contemporaneous media observation, interview or user-operation description.
- **C**: later recollection.
- **D**: researcher state-machine reconstruction.

No source in this slice licenses reconstruction of private user messages or missing profile pages.

---

## 2. Pre-Web boundary: personal ads already separated public profile from private communication

A 2009 retrospective interview with Ding Naijun describes a 1981 `市场报` personal advertisement followed by hundreds of postal responses and private correspondence.

Evidence:

- 2009 retrospective interview preserved by Sina:
  https://style.sina.com.cn/news/2009-10-10/101649707_2.shtml

**Grade: C.**

This is useful only as boundary context.

It establishes an older state machine:

```text
person wants partner
  -> public ad submitted
  -> newspaper prints compressed profile
  -> reader sees ad
  -> reader sends private letter
  -> advertiser receives letter
  -> advertiser chooses whether to answer
  -> correspondence continues
  -> possible meeting
```

The Web did not invent the distinction between a **public matching surface** and **private relationship communication**.

It changed latency, indexing, filtering and scale.

Do not expand this repository into a 1980s newspaper history; that belongs in the cross-project life-history note.

---

## 3. 2003–2006: historical locators and the emergence of a searchable matchmaking database

A 2006-01-23 Sina Tech interview with Jiayuan founder Gong Haiyan explicitly identifies the service and links the historical locator:

- `www.love21cn.com`

The interview describes the site as a serious marriage-oriented dating service and discusses user-provided proof such as identity and education credentials.

Evidence:

- https://tech.sina.com.cn/it/2006-01-23/1115827191.shtml

**Grade: B.**

Supported narrow claims:

1. By January 2006, `love21cn.com` was publicly identified as a Jiayuan matchmaking-site locator.
2. The platform publicly described identity/education proof as part of profile trust-building.
3. Structured online profiles and partner discovery were part of its stated service.

Not supported:

- exact historical HTML or CSS;
- the precise registration form schema;
- the real share of users who uploaded verification materials;
- whether a verification badge mapped one-to-one to a valid document at every historical date;
- the site's exact browser or charset requirements;
- the ranking logic behind search results.

### New state gap: profile record / truthful person

A profile can exist while:

- the person has stopped using the account;
- some fields are stale;
- some fields are strategically presented;
- a photograph no longer represents the current user;
- identity credentials are valid but lifestyle claims are not independently verified.

Therefore:

`profile record exists`

!=

`all profile claims are true now`.

Call this the **profile-record / person-state gap**.

---

## 4. 2008: an observed search action turns life attributes into query parameters

A China Youth Daily report republished by China News on 2008-03-03 contains a concrete contemporaneous usage observation.

A pseudonymous user called `小周` enters criteria including:

- age;
- education;
- monthly salary;

into Jiayuan's search interface and receives dozens of candidates. The user explains the attraction in terms of self-directed search, anytime access and more choice.

Evidence:

- https://www.chinanews.com.cn/sh/news/2008/03-03/1179413.shtml

**Grade: B.**

This source supports an unusually specific interface-level claim:

> By early 2008, at least one major Chinese matchmaking workflow exposed life-course attributes as selectable/filterable candidate-search criteria.

The same article says reporters saw matchmaking search forms with more than ten possible conditions on several sites.

### New state gap: query matches / socially executable match

If the SQL/search layer returns a person, all it proves is that the indexed profile satisfies some stored criteria.

It does not prove:

- the account is active;
- the person will see the initiating user;
- the person will like the initiating user's profile;
- the person is geographically available to meet;
- the two schedules overlap;
- housing/work/family circumstances permit a relationship;
- either person actually wants marriage at the same time.

Therefore:

`search result match`

!=

`mutual match`

!=

`executable relationship`.

Call this the **query-match / mutuality gap**.

---

## 5. 2008–2010: abundance, paywalls and family proxy browsing

Contemporaneous reports show that more candidates did not eliminate search labor.

A 2009 China Youth Daily report describes large volumes of profile browsing and family members helping a young person screen candidates.

Evidence:

- https://zqb.cyol.com/content/2009-12/24/content_2997776.htm

A 2010 report on the annual marriage/dating survey explicitly says some parents had moved onto matchmaking websites to search for partners for their children.

Evidence:

- https://zqb.cyol.com/content/2010-01/09/content_3029736.htm

**Grade: B.**

### New state gap: account user / decision-maker

A historical account does not always reveal who is doing the searching.

Possible paths include:

```text
child owns account -> child searches
child owns account -> parent sits beside child and screens
parent registers/searches -> child later reviews candidates
parent passes profile/phone information offline -> child decides whether to contact
```

Thus:

`account belongs to person X`

!=

`all search decisions were made by person X`.

Call this the **account / proxy-operator gap**.

### Paywall state must also remain explicit

Period business reporting describes matchmaking sites using different monetization models, including paid messages, subscriptions, value-added verification or offline services.

That means a visible message button may still hide additional states:

`button visible`

`user entitled to use feature`

`user paid / possessed virtual currency`

`message transaction accepted`

`message actually delivered`

These cannot be compressed.

---

## 6. 2011: identity verification creates a backstage legal-identity layer

On 2011-12-15 Caixin reported Baihe's announcement of a site-wide real-name policy.

The report says:

- new users would have to register under a real identity;
- old users had a transition period;
- after the transition only verified users could use the matchmaking service;
- the company said identity data would be sent to a national citizen identity information system and a verification result returned to the user's phone;
- the company said it would not retain the identity-card number;
- users could exchange verified identity information with one another through authorization.

Evidence:

- https://companies.caixin.com/2011-12-15/100338598.html

**Grade: B, with implementation details attributed to platform statements.**

A later 2012 China News report confirms that the 2011 policy had become a major public issue in discussions of matchmaking-site trust and fraud.

Evidence:

- https://www.chinanews.com/sh/2012/11-29/4367041.shtml

### New identity model

At minimum, distinguish:

```text
legal person
  |
  v
backstage verified platform identity
  |
  v
public-facing nickname/profile
  |
  v
selectively disclosed information to another user
  |
  v
off-platform identity in QQ/phone/email
  |
  v
person encountered in an offline meeting
```

These layers can diverge.

### New state gaps

**verification-request / verification-success gap**

Submitting an ID is not the same as successful validation.

**verified-person / verified-profile-claim gap**

A legal identity match does not verify salary, property, relationship history or intent.

**backstage-real / frontstage-alias gap**

Mandatory backend verification does not imply public display of a legal name.

**verified-account / current-controller gap**

A verified account could later be shared, compromised or abandoned unless ongoing controls are known.

Historical archaeology must not infer more than the evidence supports.

---

## 7. Browser-visible site vs private/off-platform communication

Chinese matchmaking in this period commonly overlapped with:

- internal site messages;
- email;
- QQ;
- telephone/SMS;
- offline matchmaking events;
- direct meetings.

The Web page could therefore function as a **discovery and coordination control plane**, while the relationship's highest-value interactions moved outside the web host.

### Proposed state machine (D reconstruction)

```text
profile account created
        |
        v
profile approved / indexed
        |
        v
candidate appears in search result
        |
        v
candidate profile actually viewed
        |
        v
contact/message feature available
        |
        v
required payment/entitlement satisfied (if any)
        |
        v
message/contact request accepted by platform
        |
        v
message reaches recipient inbox
        |
        v
recipient logs in and reads
        |
        v
recipient responds
        |
        v
conversation continues
        |
        +--> stays on platform
        |
        +--> moves to email / QQ / SMS / phone
        |
        v
offline meeting arranged
        |
        v
meeting actually occurs
        |
        v
repeated relationship develops
        |
        v
marriage intention develops
        |
        v
legal registration / household life
```

This model is analytical. It is **not** a reconstruction of the exact Jiayuan/Baihe server implementation.

### Important gaps introduced

- **message-sent / delivered gap**;
- **delivered / read gap**;
- **read / reciprocal-response gap**;
- **online-conversation / offline-meeting gap**;
- **meeting / repeated-relationship gap**;
- **relationship / marriage gap**;
- **marriage-story / independently verified marriage gap**.

---

## 8. Search form survival can overstate historical visibility

A future historian may successfully recover:

- the homepage;
- registration instructions;
- screenshots of a search form;
- a list of selectable partner criteria;
- a public profile;
- a verification-policy announcement.

But fail to recover:

- server-side search index state;
- result ordering;
- whether a candidate profile was active;
- internal mailbox data;
- message delivery status;
- deleted messages;
- QQ/phone conversations;
- offline meetings;
- relationship outcomes.

This creates a particularly severe **interface / transaction dark-matter gap**.

The search UI is precisely the part most likely to be described publicly; the private interaction state is precisely the part most likely to be absent from Web archives.

---

## 9. Success counters and user counts require separate evidence families

Dating sites often publicly report:

- registered-user counts;
- active-user counts;
- successful couples;
- marriages;
- events held;
- verification rates.

These are not interchangeable.

At minimum distinguish:

`registered account`

`non-duplicate account`

`active account in stated period`

`profile viewed`

`contact initiated`

`offline meeting`

`self-reported couple`

`platform-classified successful couple`

`legally registered marriage`

`long-term continuing household`

A platform press release can be strong evidence that **the platform made a claim on that date**, while remaining weak evidence that every underlying case was independently validated.

---

## 10. Chinese Web matching can be geographically wide while legal marriage remained territorially routed

The 2003 Marriage Registration Regulations required mainland couples to jointly register at the marriage-registration authority of either party's permanent hukou location and to present household registration and identity documents.

Official text:

- https://www.nhc.gov.cn/wjw/flfg/200308/e2813d5724c44fe7bff26cdf9f28945d.shtml

**Grade: A.**

This produces a useful state boundary:

`online profile visible nationally`

!=

`marriage can be legally registered at the location where the couple currently met/lived`.

Call this the **match-geography / registration-geography gap**.

The later 2025 nationwide-registration reform is outside the primary old-Web period, but it helps expose the historical constraint by contrast. It should remain boundary context only.

---

## 11. Privacy and ethics are first-order technical constraints in this case

Historical dating profiles may expose:

- photographs;
- birth year/age;
- city;
- education;
- employer/occupation;
- income;
- housing/property claims;
- marriage history;
- contact details;
- intimate preferences.

A profile being technically retrievable from an archive does **not** make wholesale republication appropriate.

### Rules for this research line

Prefer:

1. platform help/official pages;
2. search-form schemas without ordinary-user identifiers;
3. contemporaneous media observations using existing pseudonyms;
4. aggregate statistics with sampling caveats;
5. minimally necessary profile-field examples.

Avoid:

- bulk extraction of ordinary-person profiles;
- re-publishing phone numbers/email/QQ numbers;
- face-photo galleries;
- exposing an archived dating profile of a person who later removed it;
- attempting to connect a historical dating profile to a current real-world identity unless a compelling public-interest reason exists.

The object of study is the **platform state machine and lived interface**, not the rediscovery of individual private lives.

---

## 12. Archive gap in this slice

### M1 status

**NOT ACHIEVED IN THIS SLICE.**

This research round identified:

- contemporaneous media reports;
- historical host/brand locators such as `love21cn.com`;
- contemporaneous user-operation descriptions;
- contemporaneous identity-verification policy descriptions;
- official marriage-registration rules.

It did **not** obtain and inspect a qualifying verified Wayback/WARC capture of a 2003–2011 Chinese matchmaking site.

Therefore the following remain **unknown** unless another repository artifact separately proves them:

- exact historical HTML/DOM;
- `Content-Type` and charset;
- browser compatibility / IE assumptions;
- CSS/JS implementation;
- search form field names and request method;
- server-side ranking/filter semantics;
- profile approval/moderation implementation;
- message endpoint and delivery semantics;
- payment/session-cookie behavior;
- authentication/session timeout;
- exact identity-verification API path;
- account deletion semantics;
- private mailbox retention;
- whether archived profile pages reflected live database state or cached/static renders.

Per repository method:

> failure to verify a capture in this slice is **not evidence that no capture exists**.

Historical locators should be retained as candidate investigation targets.

---

## 13. Browser and encoding questions for a future verified capture

When a real 2003–2011 capture is obtained, record at least:

- capture datetime;
- original URL and redirect chain;
- HTTP status;
- declared and detected charset (`GB2312`, `GBK`, `UTF-8`, etc.);
- table/frames layout;
- screen-width assumptions;
- IE-only JS / `document.all` / ActiveX assumptions;
- image-host survival;
- form action destinations;
- whether search POSTs were archived;
- whether login walls block profile pages;
- archive rewrite changes;
- missing JS/CSS/images;
- whether historical navigation links resolve to the same host/brand state.

A modern browser screenshot must never be labeled “what users saw in 2008” without historical-browser validation.

---

## 14. Cross-national boundary: Minitel shows that digital intimate interaction predates the Web

This repository remains Chinese-old-Web scoped, so the French case belongs only in comparative context.

Contemporaneous French scholarship in 1987–1993 studied Minitel/videotex social communication, including pseudonymous conversational and intimate interaction.

Sources:

- Jean-Marie Charon, 1987:
  https://journals.sagepub.com/doi/10.1177/016344387009003004
- Josiane Jouët, 1987:
  https://www.persee.fr/doc/colan_0336-1500_1987_num_72_1_976
- Gérard Neyrand, 1988:
  https://www.persee.fr/doc/quad_0987-1381_1988_num_5_1_1323
- Minitel conversational corpus study, 1993:
  https://www.persee.fr/doc/linx_0246-8743_1993_num_28_1_1261

Narrow comparative conclusion:

> Digitally mediated stranger sociality and intimate interaction existed before mass Web browsing; Chinese 2000s matchmaking sites should therefore be studied as one historically specific implementation of a broader communication transformation, not as the invention of digital intimacy itself.

No attempt is made here to merge Minitel history into the Chinese old-Web corpus.

---

## 15. Claim matrix

| Claim | Evidence | Grade | Confidence | Boundary |
|---|---|---:|---:|---|
| Jiayuan had a publicly identified `love21cn.com` locator by Jan 2006 | Sina Tech interview | B | high | does not reconstruct historical page |
| Some early matchmaking sites promoted identity/education proof | 2006 platform interview | B | medium-high | implementation and uptake unknown |
| A 2008 Jiayuan user searched by age, education and monthly salary | China Youth Daily / China News | B | high | individual usage, not population rate |
| Matchmaking sites exposed many structured search criteria | contemporaneous reporter observation | B | high | exact field schema by site/version unknown |
| Parents could participate in Web partner search by 2009–2010 | China Youth Daily | B | high | prevalence estimates depend on survey/sample |
| Baihe announced mandatory real-name verification in Dec 2011 | Caixin | B | high | API implementation described by company |
| 2003 legal registration remained tied to either party's permanent-hukou location | official regulation | A | high | legal state, not proof of every local practice |
| A surviving profile proves later relationship/marriage | none | — | **unsupported** | must not infer |
| A platform user count proves active unique users | none in this slice | — | **unsupported** | registration/active/unique must remain separate |

---

## 16. What this changes in old-Web archaeology

This case adds several reusable gaps to the repository:

- **profile-record / person-state gap**;
- **profile-field / truth gap**;
- **query-match / mutuality gap**;
- **account / proxy-operator gap**;
- **message-sent / delivered / read gap**;
- **read / reciprocal-response gap**;
- **backstage-real / frontstage-alias gap**;
- **verified-person / verified-profile-claim gap**;
- **website / off-platform-conversation gap**;
- **online-conversation / offline-meeting gap**;
- **meeting / relationship / marriage gap**;
- **success-story / independently verified outcome gap**;
- **match-geography / registration-geography gap**;
- **profile-archive / relationship-outcome asymmetry**.

The larger lesson is methodological:

> A dating website is not a digital archive of relationships. It is a partial control surface over discovery, filtering, trust and contact. The states that matter most to ordinary life often leave the browser entirely.
