# ONLINE_DATING_PROFILES_VERIFICATION_SEARCH_MESSAGING_AND_OFFLINE_OUTCOME_STATE_GAPS_2003_2012.md

> Status: methodology / research note  
> Scope: Chinese online dating / marriage-oriented platforms, approximately 2003–2012.  
> Cross-repository context: `tmzncty/how-people-lived/topics/matchmaking-personal-ads-searchable-mates-and-marriage-route-executability-china-1981-2025.zh-CN.md`  
> Core boundary: this note studies the **old-Web state machine between a public dating profile and an actual offline relationship outcome**. It does not attempt to republish historical personal profiles or prove individual marriages.

## 0. Why dating sites are unusually dangerous historical objects

Dating platforms look easy to archive because many visible pages resemble ordinary profiles:

```text
photo
age
city
height
education
occupation
income
self-description
partner requirements
```

But the visible profile is only one state in a much larger, mostly private system:

```text
registration
→ profile creation
→ profile moderation / verification
→ indexing / search visibility
→ ranking
→ profile view
→ initial message
→ message becomes readable
→ reply
→ off-platform contact exchange
→ offline meeting
→ relationship status change
→ account inactivity / deletion / success-story publication
```

A historical capture may preserve only one public projection while almost every state that determines whether the route worked is missing.

Therefore the hard rule is:

> **profile archived ≠ relationship reconstructed**

And for privacy:

> **historical visibility ≠ permission to reaggregate intimate personal data today**

---

## 1. Research units

Keep the following units separate:

- **platform** — e.g. a dating/marriage service brand;
- **host / product surface** — desktop Web, WAP/mobile Web, later app;
- **account** — login credential / platform account;
- **profile subject** — the person described by the profile;
- **account operator** — the person actually editing/searching/messaging through the account;
- **profile version** — fields and values at a specific time;
- **verification state** — what evidence, if any, the platform says has been submitted/checked;
- **search-index state** — whether and how the profile is discoverable;
- **message thread** — private contact state;
- **offline handoff** — exchange of phone/QQ/email or meeting details;
- **offline encounter** — whether a meeting actually happened;
- **relationship outcome** — none / continued dating / marriage / other;
- **public success story** — a platform-published claim about an outcome;
- **capture** — archive representation of any public resource;
- **claim** — the narrow historical proposition supported by evidence.

Never assume:

`account operator = profile subject = message author = person who later met someone offline`.

The 2009 contemporary press already records parents browsing dating profiles together with adult children, and later reports explicitly describe parents operating online matchmaking on behalf of children. The operator/person split is not an edge case invented by modern apps.

---

## 2. Evidence grades used here

Follow `docs/METHOD.md` A/B/C/D.

Important examples:

### A

- 2011 Jiayuan SEC F-1/A regulatory filing describing product mechanics;
- verified historical official help/product pages if a capture is actually opened and inspected;
- historical WARC/capture of a platform page with original URL and datetime.

### B

- 2006 First Financial Daily report describing a Jiayuan offline event;
- 2009 China Youth Daily report describing how users and parents browsed profiles;
- contemporary tutorials/reviews explaining site use.

### C

- later recollections of early dating-site interfaces;
- retrospective founder histories;
- current official milestone pages describing earlier product history.

### D

- inferred field schema from screenshots;
- guessed browser/charset requirements;
- reconstructed ranking logic;
- guessed profile-to-user identity linkage.

No D claim should be written as an original interface fact.

---

## 3. The 2006 online→offline handoff is already visible in contemporary reporting

A First Financial Daily report dated 2006-02-14 described more than 200 Jiayuan members attending an offline Lantern Festival event in Shanghai. Participants wore heart-shaped labels with member number and age and carried paper slips containing contact information.

Source (contemporary article, Sina mirror):
https://finance.sina.com.cn/chanjing/b/20060214/01402338668.shtml

Evidence grade: B.

This one event establishes a narrow but useful state transition:

```text
online membership identity
→ platform-organized physical gathering
→ membership number remains a lookup key
→ paper contact endpoint
→ possible later private communication
```

It does **not** establish:

- that every attendee had a verified identity;
- that the membership number mapped one-to-one to a real person;
- that exchanged contacts were later used;
- that any particular attendee formed a relationship;
- platform-wide success rate.

Old-Web implication:

> an archived event page can prove an event was announced or a participant list was displayed; it cannot prove the private handoff that followed.

---

## 4. 2009: public profile abundance and household co-browsing

China Youth Daily on 2009-12-24 described a young man whose mother pushed him to register across multiple dating websites after numerous introductions and large matchmaking events. On Jiayuan-like profile pages the reporter observed photos, region and monthly income fields; the young man browsed large numbers of candidates while his parents helped compare them.

Source:
https://zqb.cyol.com/content/2009-12/24/content_2997776.htm

Evidence grade: B.

This establishes several historically important states:

- structured personal fields were used for fast candidate comparison;
- a public profile could be browsed by people other than the future dater;
- the practical user could be a **household**, not an isolated individual;
- candidate abundance created a filtering workload.

It does not establish the exact 2009 DOM, field order, CSS, search query parameters or browser environment.

The article's visible registered-user counter is also a classic measurement warning:

> **displayed registered-account count ≠ active people ≠ unique people ≠ marriage-seeking people ≠ successful users**.

---

## 5. 2011 Jiayuan F-1/A: a rare primary description of the hidden state machine

The strongest source in this note is Jiayuan.com International Ltd.'s Form F-1/A filed with the U.S. SEC on 2011-05-11:

https://www.sec.gov/Archives/edgar/data/1511683/000104746911004910/a2203664zf-1a.htm

Evidence grade: A for what the company disclosed at filing time. Company statements about effectiveness, trust or market leadership remain issuer claims.

### 5.1 Registration and search

The filing says registration and immediate full search access were offered free.

That supports:

```text
registered
→ searchable database access available
```

It does not prove a specific profile was indexed immediately, nor that every profile had equal search visibility.

### 5.2 Sent message vs readable message

The filing states that users were not required to pay merely to send an initial message, but either sender or recipient had to purchase a RMB2 virtual stamp for the initial message to be readable. After the initial message was read, subsequent communication between the same two users could be free.

Therefore:

> **message sent ≠ message readable**

This is one of the most important old-Web execution gaps in the whole platform category.

A server or archive that preserved a “message sent” confirmation would still not prove the recipient ever gained access to the content.

### 5.3 Public profile vs search visibility

The filing describes paid services including:

- improving search ranking;
- priority ranking for sent messages;
- premium display of pictures/profile;
- virtual gifts;
- online chatting;
- advanced memberships.

Therefore:

> **profile exists ≠ profile receives equal discovery probability**

Search ranking is part of the historical interface, not neutral plumbing.

### 5.4 Profile claim vs proof-submission state

The filing says users could submit proof of information such as age, income and education. Users who submitted proof and paid a fee received a higher database rating. It also says some basic information such as height, salary and education could not later be improved without verification.

This establishes a distinct state:

```text
field self-declared
→ proof submitted
→ platform records a verification/rating state
```

It does not establish:

- that every displayed field was verified;
- that submitted documents remained current;
- that the platform independently verified every claim with an issuing authority;
- that marital status could never change after verification;
- that the operator remained the original person.

Use the narrow term **proof-submission / platform verification state**, not “real-name truth.”

### 5.5 Online conversation vs off-platform handoff

The filing says historical data showed the average exchange between two users on the site lasted about 3.5 days, and the company believed users interested in further interaction exchanged personal contact information and communicated directly.

This supports a platform design expectation:

```text
site discovery
→ initial paid-readable connection
→ short internal conversation
→ contact moves outside platform
```

It does not let an archaeologist reconstruct what happened after the handoff.

This is a major preservation asymmetry: the platform may preserve discovery metadata while the socially important relationship moves to phone, QQ, SMS, email or physical meetings.

### 5.6 Mobile Web boundary

The filing says certain dating features had been accessible through mobile browsers since June 2010, including sending/reading messages, viewing/modifying profiles and purchasing some value-added services.

This supports:

- mobile-browser access existed by that date;
- desktop Web was no longer the only execution surface.

It does **not** establish:

- exact WAP/HTML implementation;
- screen layout on a specific phone;
- carrier performance;
- browser compatibility;
- that mobile access was common among all users.

The filing also notes limitations of contemporary mobile devices including lower resolution/functionality/memory. Keep those as company-described engineering constraints, not reconstructed user experience.

---

## 6. Online-dating execution state machine

A minimum historical model should be:

```text
S0  platform/service exists
S1  registration surface reachable
S2  account created
S3  profile fields submitted
S4  profile passes moderation / becomes eligible for display
S5  optional proof/verification state attached
S6  profile indexed in search
S7  profile receives a ranking / visibility state
S8  another user views profile
S9  viewer initiates message/contact
S10 initial message becomes readable
S11 recipient replies
S12 thread continues
S13 personal contact endpoint exchanged
S14 off-platform conversation occurs
S15 offline meeting planned
S16 offline meeting occurs
S17 further relationship continues / does not continue
S18 profile status changes / account becomes inactive / account deleted
S19 optional public success-story claim appears
```

No archive should silently leap from S6/S8 to S16/S17.

---

## 7. Gap taxonomy

### 7.1 profile-snapshot gap

A capture shows a profile at one moment but cannot establish earlier/later values.

Fields such as city, salary, marital status, partner requirements and photos can change.

### 7.2 operator-person gap

The account operator may be:

- profile subject;
- parent;
- friend;
- intermediary / agency staff;
- compromised account holder.

A public profile does not establish authorship of every message.

### 7.3 verification-state gap

A badge/label may mean only that a document was submitted or a certain platform procedure occurred. Exact semantics can vary by date and product surface.

### 7.4 search-index gap

A profile page can exist while being excluded from normal search due to moderation, preferences, inactivity or other system state.

### 7.5 ranking/discoverability gap

Paid ranking and premium display mean visibility is mutable and commercialized.

A capture of a profile URL cannot reconstruct its position in a user's search results.

### 7.6 message-readability gap

Jiayuan's 2011 pricing model demonstrates directly:

`initial message sent ≠ initial message readable`.

### 7.7 reply gap

Readable does not mean read; read does not mean replied.

### 7.8 off-platform handoff gap

Once phone/QQ/email is exchanged, the relationship can leave the archiveable platform.

### 7.9 meeting-plan gap

Agreeing to meet does not prove a meeting occurred.

### 7.10 offline-outcome gap

A public Web archive usually cannot establish whether two people dated, separated or married.

### 7.11 success-story selection gap

A platform success page is selected publicity evidence. It can prove the platform published the claim; it cannot supply a denominator or causal success rate without an independently defined sample.

### 7.12 account-status gap

A profile remaining reachable later does not establish the person is still single, still seeking, still operating the account or still alive.

### 7.13 deletion/privacy gap

Deleted or hidden dating profiles are not an invitation to recover and republish intimate information merely because an archive may still contain it.

---

## 8. Search fields are social-history evidence, but only if provenance is strong

Dating profile fields are historically valuable because they operationalize what a platform believed users wanted to compare.

Potential fields include:

- age;
- location;
- height;
- education;
- occupation;
- income;
- housing / property-related claims;
- marital status;
- children;
- self-description;
- partner criteria.

But a modern help page or memory cannot establish the field set for 2005.

For field genealogy, record:

```yaml
platform:
product_surface: desktop-web|mobile-web|app|offline-event
field_name:
field_label_original:
field_type: free-text|enum|numeric|boolean|unknown
required: true|false|unknown
visibility_default: public|restricted|unknown
verification_possible: true|false|unknown
source_url:
capture_datetime:
evidence_grade:
```

Do not infer a stable schema across a decade.

---

## 9. 2018–2019 retrospective relevance: trust remained an execution problem

Although outside the core 2003–2012 object window, 2018–2019 contemporary surveys help explain why the old verification state matters.

China Youth Daily 2018-01-25 reported a survey of 1,998 marriage-age single respondents in which inaccurate member information and weak review were major concerns; 69.3% of that sample said platforms should strictly check member data.

https://zqb.cyol.com/html/2018-01/25/nw.D110000zgqnb_20180125_2-07.htm

China Youth Daily 2019-09-19 reported that among a survey sample of 1,972 single young adults, 73.0% worried about information leakage and 66.7% worried about false user information.

https://zqb.cyol.com/html/2019-09/19/nw.D110000zgqnb_20190919_4-08.htm

These sources are not used to rewrite 2011 behavior. They show that **verification and privacy remained unresolved user-facing problems after the early Web period**, so archaeologists should not treat historical badges as complete identity resolution.

---

## 10. Parent-assisted search creates an archival identity hazard

A 2009 China Youth Daily article describes parents helping an adult son browse candidate profiles:
https://zqb.cyol.com/content/2009-12/24/content_2997776.htm

Another 2009 report describes parents moving online to help children seek partners:
https://zqb.cyol.com/content/2009-12/09/content_3029736.htm

For platform archaeology this creates a hard identity boundary:

```text
profile subject
≠ search operator
≠ message drafter
```

Unless a source establishes authorship, do not quote a message as the profile subject's own words merely because it came from that account.

This problem later becomes explicit in parent-oriented apps, but it already exists inside the old-Web period.

---

## 11. Offline events are not outside Web archaeology

Jiayuan's 2011 filing says the company had hosted large-scale offline social gatherings since 2008, and the 2006 First Financial Daily report already documents a site-member event.

These events should be modeled as **cross-surface execution nodes**:

```text
Web profile
→ event registration / invitation
→ physical event
→ member number or name used as lookup key
→ paper/phone contact exchange
→ later private communication
```

An event page can therefore be historically important even if no actual relationship outcome survives.

Suggested evidence fields:

```yaml
event_date:
event_city:
platform:
online_registration_proven: true|false|unknown
member_identifier_used_offline: true|false|unknown
contact_handoff_medium: paper|phone|sms|qq|email|unknown
attendance_claim_source:
attendance_observed_or_reported:
offline_outcome_known: false
```

Avoid reproducing historical participant lists.

---

## 12. Screen and television evidence: useful for cultural legibility, not backend reconstruction

This repository already defines `SF-context`, `SF-interface`, `SF-production` and `SF-reception` in:

`docs/FICTIONAL_SCREEN_WEB_USAGE_CONTEXT_CANON_AND_RECONSTRUCTION_GAPS_2004_2009.md`

Marriage/search media are an especially useful application.

The 2008 film 《非诚勿扰》 made public mate-seeking and repeated blind dates a mainstream romantic-comedy premise. A 2008 contemporary interview with director Feng Xiaogang can support cultural/narrative context:
https://news.sina.com.cn/o/2008-12-25/143214936119s.shtml

The 2010 television program of the same Chinese title triggered contemporary public disputes over guest identity and motive; a 2010 Chengdu audition report says applicants filled basic information, signed a statement guaranteeing single/non-married status and underwent further interview checks.

Sources:

- https://ent.sina.com.cn/v/m/2010-04-06/10112919592.shtml
- https://ent.sina.com.cn/v/m/2010-08-17/07593054134.shtml

Use these as representation/production/verification context only.

Do not infer dating-site backend mechanics from television staging.

---

## 13. Preservation bias: public profiles survive better than failed interactions

The archiveable object is systematically biased toward:

- public landing pages;
- search-indexable profiles;
- promotional success stories;
- event announcements;
- press coverage;
- platform corporate documents.

It is systematically weak at:

- ignored messages;
- unread messages;
- rejected invitations;
- blocked users;
- deleted profiles;
- false starts;
- private QQ/SMS/phone conversations;
- dates that never occurred;
- relationships that ended;
- people who silently stopped searching.

This produces **success visibility bias**.

A history built only from surviving public Web pages will overrepresent:

1. people willing to expose a public profile;
2. active/current profiles;
3. platform-selected success narratives;
4. interactions that generated content worth publishing.

It will underrepresent the ordinary majority of non-events.

---

## 14. Archive/privacy stop conditions specific to dating platforms

Stop or minimize when a historical resource exposes:

- real name + old phone number;
- exact employer + private contact;
- income/property details tied to an identifiable ordinary person;
- marital status or children;
- sexual/relationship preferences;
- private messages;
- ID-document indicators;
- deleted account contents.

Do not:

- build a dataset of historical member IDs;
- probe old email/phone endpoints;
- attempt password recovery;
- cross-reference a profile with current social media to discover later marriage outcomes;
- republish full profile screenshots merely because they are technically accessible.

Research platform structure using abstract field names and aggregate counts wherever possible.

---

## 15. Browser / charset / rendering boundary

This note does **not** establish the exact 2003–2011 browser environment of Jiayuan or other dating platforms.

The SEC filing proves service mechanics and mobile-browser availability by June 2010, not:

- IE version requirements;
- GB2312/GBK/UTF-8 at a particular host/date;
- JavaScript framework;
- image upload component;
- cookie/session implementation;
- exact HTML form fields;
- WAP markup;
- historical viewport.

A current Jiayuan page or current help center must not be rendered as “the 2010 interface.”

Historical browser claims require inspected captures or contemporary technical documentation.

---

## 16. Negative result for this slice

This research pass obtained:

- a primary 2011 SEC filing with unusually detailed product-state descriptions;
- multiple 2006–2009 contemporary press descriptions of use and online→offline handoff;
- later contemporary evidence demonstrating persistence of verification/privacy problems.

It did **not** obtain and inspect a privacy-safe, ordinary-user 2003–2006 historical profile capture with enough preserved subresources to establish:

- exact profile DOM;
- field order;
- charset;
- search-result layout;
- message UI;
- verification badge rendering;
- browser compatibility.

Therefore those interface details remain **unknown**, not reconstructed.

Current/live pages that preserve an old event date are not automatically historical captures of that date.

---

## 17. Claim ledger

| Claim | Evidence | Grade | Confidence | Boundary |
|---|---|---:|---|---|
| Jiayuan members used online member IDs in a 2006 offline event | First Financial Daily contemporaneous report | B | high | one event, not all users |
| 2009 users could browse structured candidate information and parents could co-filter | China Youth Daily 2009 | B | high | reporter-observed/reported use, not exact DOM |
| Jiayuan 2011 offered free registration/search but initial-message readability could require a RMB2 virtual stamp | SEC F-1/A | A | high | issuer product disclosure |
| Search ranking/profile prominence could be paid | SEC F-1/A | A | high | proves product mechanism, not ranking algorithm |
| Users could submit proof of age/income/education and receive a higher database rating | SEC F-1/A | A | high | proof-submission state ≠ universal truth |
| Selected features were available through mobile browsers from June 2010 | SEC F-1/A | A | high | not exact device/browser experience |
| Platform expected successful contacts to move off-site after initial exchange | SEC F-1/A | A for company disclosure | medium | company interpretation of user behavior |
| Exact 2005 ordinary-user profile interface recovered | none | — | **not established** | explicit negative result |

---

## 18. What this changes in old-Web archaeology

Dating platforms force a stronger version of the repository's `exists / available / used / completed` rule.

For this domain:

```text
profile exists
≠ profile discoverable
≠ profile viewed
≠ message readable
≠ reply received
≠ person verified
≠ contact moved offline
≠ date happened
≠ relationship formed
≠ marriage occurred
```

The public Web records the **possibility surface** much better than the outcome.

That is historically useful rather than a failure: it tells us exactly where the archive ends and ordinary life begins.

---

## 19. Next high-value archaeology

Prioritize, in order:

1. find an official/historical 2004–2006 registration or help-page capture and inspect original URL, datetime, charset and field schema;
2. find a 2008–2011 search-results capture and determine which filters/ranking indicators are actually visible;
3. find a privacy-safe official message/help page documenting the virtual-stamp readable/unreadable state;
4. compare desktop and June-2010-era mobile-browser product surfaces using real captures if available;
5. document how success-story pages represent a relationship outcome without treating them as a denominator;
6. sample archive survival bias across public profiles vs help pages vs message/login surfaces without collecting personal profile content.

The main question is not “can we still see an old dating page?” It is:

> **which parts of a relationship-search state machine were public enough to survive, and which socially decisive states disappeared because they were private, off-platform, ephemeral or deliberately deleted?**
