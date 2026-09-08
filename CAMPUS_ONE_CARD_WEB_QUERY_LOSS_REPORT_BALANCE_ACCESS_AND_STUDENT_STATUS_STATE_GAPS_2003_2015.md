# Campus One Card / Web Query / Loss Report / Balance / Access / Student-Status State Gaps, 2003–2015

> Scope: Chinese old Web and Internet-backed campus systems, approximately 2003–2015.
>
> Companion life-history note: `tmzncty/how-people-lived/topics/from-separate-meal-library-and-access-cards-to-one-campus-credential-student-status-and-everyday-life-china-1980-2026.zh-CN.md`
>
> Research question: when a Chinese university said “校园一卡通”, what exactly existed on the Web, what existed only on campus LAN/bank/private networks, what state did a browser query actually expose, and what real-world action followed? How should an archaeologist distinguish a surviving help page from the historical transaction system that once decided whether a student could eat, enter a dormitory, borrow a book, or use a remaining balance?

This is **not** a general smart-card history and not a global campus-card history. The repository scope remains the Chinese Internet/old-Web environment of roughly 1995–2015. Pre-Web and overseas history belongs mainly in `how-people-lived`; it appears here only where needed to prevent a false claim that the public Web created campus credentials.

---

## 0. Why this is an old-Web archaeology problem

A campus-card page can look deceptively simple:

- “余额查询”;
- “交易明细”;
- “网上挂失”;
- “圈存/转账”;
- “修改密码”;
- “校园卡服务”.

But the page is only the visible edge of a much larger transaction path:

`student/person registry`
`→ campus-card account`
`→ physical/virtual credential`
`→ entitlement / wallet state`
`→ reader / POS / gate`
`→ local or central transaction state`
`→ campus network / private network sync`
`→ database`
`→ Web / touchscreen / IVR presentation`
`→ user interpretation`
`→ real-world action`.

Therefore:

**campus-card Web archaeology cannot stop at HTML.**

A preserved login box or balance-query shell does not prove that the historical database can still answer a query, and a successful account login would not by itself prove that a door reader or dining POS had synchronized the same state.

---

## 1. Research-unit separation

Following `docs/METHOD.md`, keep at least these units separate.

### 1.1 Platform / service family

Examples:

- a university “校园一卡通” system;
- a vendor-built card platform;
- a university-wide identity/account system;
- a mobile/virtual-card extension.

### 1.2 Site / host

Possible historical or current examples include:

- dedicated `ecard.*.edu.cn` host;
- university IT center site;
- integrated portal;
- B/S self-service host;
- bank-side recharge/payment host.

A brand can persist while the host changes.

### 1.3 Account

A student’s campus-card account is not the same object as:

- the plastic card serial number;
- student number;
- bank account;
- unified-identity account;
- mobile-phone credential;
- alumni identity.

### 1.4 Credential

Possible media:

- contactless IC card;
- magnetic-stripe card;
- CPU card;
- SIM/mobile card;
- QR virtual card;
- NFC phone credential.

The same account can outlive one credential medium.

### 1.5 Subsystem

At minimum distinguish:

- dining POS;
- library;
- dorm gate;
- campus gate;
- computer room;
- bathing/water control;
- school bus;
- clinic;
- registration/迎新;
- Web self-service;
- bank-transfer/recharge subsystem.

“Campus card works” is meaningless unless the subsystem is named.

### 1.6 Page / URL

Examples:

- public help page;
- login page;
- balance page;
- transaction-history page;
- loss-report form;
- recharge page;
- admin page.

### 1.7 Capture

An Internet Archive capture of a public help page is a capture of **that page**, not of:

- the historical student account;
- the wallet ledger;
- the door-control database;
- the bank-network transaction;
- the POS offline state.

### 1.8 Claim

Every claim should identify which of the above objects it actually concerns.

---

## 2. Core state models

## 2.1 Credential provisioning

Do not compress issuance into `CARD_EXISTS=true`.

A more useful model is:

`PERSON_RECORD_EXISTS`
`→ STUDENT/STAFF STATUS CONFIRMED`
`→ CARD_ACCOUNT_CREATED`
`→ CARD MEDIA PERSONALIZED`
`→ CARD_ID ↔ PERSON_ID BOUND`
`→ INITIAL ENTITLEMENTS ASSIGNED`
`→ WALLET / SUBSYSTEMS INITIALIZED`
`→ CARD DISTRIBUTED`
`→ USER FIRST SUCCESSFUL USE`.

Possible gaps:

- card printed but account not activated;
- right person receives wrong card;
- card valid for dining but not library;
- new student exists in admissions database but not yet in card database;
- card account exists but door entitlement has not propagated.

Therefore:

**card issued ≠ every subsystem usable**.

---

## 2.2 Web login / query

A historical “校园卡网上查询” page should be modeled as:

`HOST_RESOLVES`
`→ PAGE/LOGIN FORM LOADS`
`→ AUTHENTICATION REQUEST SUBMITTED`
`→ SESSION CREATED`
`→ ACCOUNT RESOLVED`
`→ QUERY ENDPOINT REACHED`
`→ BACKEND LEDGER READ`
`→ RESULT RENDERED`
`→ USER CORRECTLY INTERPRETS RESULT`.

Archive replay may stop at the first or second state.

Thus:

**login shell captured ≠ historical account query reproduced**.

---

## 2.3 Balance

“Balance” may refer to different things depending on architecture:

- value physically stored on card;
- central campus-wallet balance;
- bank-side balance;
- pending transfer;
- subsidy bucket;
- meal-plan entitlement rather than currency.

Do not assume one universal architecture.

Useful generic states:

`BANK/USER FUNDING SOURCE`
`→ TOP-UP INITIATED`
`→ FUNDING AUTHORIZED`
`→ CAMPUS ACCOUNT CREDITED`
`→ OPTIONAL CARD/TERMINAL WRITE OR SYNC`
`→ BALANCE VISIBLE TO USER`
`→ BALANCE SPENDABLE AT TARGET TERMINAL`.

Therefore:

**money debited from bank ≠ campus wallet spendable immediately**.

And:

**Web balance displayed ≠ every offline reader has the same state**.

---

## 2.4 POS consumption

A minimal consumption state machine:

`CARD/CREDENTIAL PRESENTED`
`→ READER RECOGNIZES MEDIA`
`→ ID / WALLET RESOLVED`
`→ LIMIT/PASSWORD RULE CHECKED`
`→ AMOUNT ACCEPTED`
`→ LOCAL/ONLINE DEBIT COMMITTED`
`→ RECEIPT/BEEP/DISPLAY`
`→ CENTRAL LEDGER UPDATED OR LATER SYNCHRONIZED`
`→ USER SEES TRANSACTION IN QUERY HISTORY`.

The exact order differs between online, offline and hybrid systems.

Do not infer architecture from the word “一卡通”.

---

## 2.5 Loss report / blacklist

This is one of the most important old-Web state gaps.

`USER REALIZES CARD LOST`
`→ USER AUTHENTICATES TO WEB/IVR/TERMINAL/COUNTER`
`→ LOSS-REPORT REQUEST ACCEPTED`
`→ CENTRAL CARD STATUS=LOST`
`→ BLACKLIST / DENY STATE GENERATED`
`→ SUBSYSTEMS/READERS RECEIVE UPDATE`
`→ OLD CARD REJECTED EVERYWHERE`
`→ REPLACEMENT CREDENTIAL ISSUED`
`→ ACCOUNT / ENTITLEMENT MIGRATED`.

Critical distinction:

**Web says “挂失成功” ≠ every offline terminal already rejects the old card**.

Without propagation logs or system documentation, blacklist timing is unknown.

---

## 2.6 Door access

`PERSON HAS STUDENT STATUS`
`→ BUILDING ENTITLEMENT ASSIGNED`
`→ CARD PRESENTED`
`→ READER READS CREDENTIAL`
`→ LOCAL/CENTRAL RULE EVALUATED`
`→ DOOR UNLOCKS OR DENIES`
`→ ACCESS EVENT LOGGED`
`→ EVENT MAY SYNC TO CENTRAL DATABASE`.

Therefore:

**reader beep ≠ door opened**.

And:

**card valid somewhere ≠ card has permission for this building**.

---

## 2.7 Student-status lifecycle

One of the most historically important models:

`ADMITTED`
`→ REGISTERED/ENROLLED`
`→ ACTIVE STUDENT`
`→ LEAVE / SUSPENSION / EXCHANGE / DELAYED GRADUATION?`
`→ GRADUATED / WITHDRAWN`
`→ ALUMNI / STAFF / TEMPORARY ROLE?`

Each transition can map differently onto:

- library entitlement;
- dorm access;
- campus-gate access;
- student-price dining;
- wallet balance;
- transport benefit;
- Web account validity.

Thus:

**person continuity ≠ account continuity ≠ entitlement continuity**.

---

## 3. 2003–2005 evidence: Web query appears inside a non-Web infrastructure

### 3.1 2003 Lanzhou University: multi-service campus IC system

A 2003 Sina Technology case report says Lanzhou University had begun planning a campus IC system roughly two years earlier, including:

- bus;
- dining;
- shopping;
- medical treatment;
- access control;
- library borrowing;
- bathing;
- computer/network use;
- bank-linked payment/financial services.

Evidence grade: **B**.

Why only B:

- contemporary;
- useful for function existence;
- but written as a vendor/implementation case and has promotional incentives.

What it proves narrowly:

> By 2003, at least some Chinese universities were implementing integrated campus-card systems spanning multiple ordinary-life and identity services.

What it does **not** prove:

- national adoption;
- household Internet access;
- a specific historical Web UI;
- exact backend architecture.

Source:
https://tech.sina.com.cn/it2/2003-09-17/1732235079.shtml

---

### 3.2 2004 Quanzhou Normal University: the best current anchor for Web-state separation

The university’s 2004 management rules describe the system as using:

- contactless IC cards;
- electronic technology;
- computer-network technology;
- database technology;
- campus-network-connected subsystems;
- shared data.

It explicitly enumerates thirteen subsystems including:

- fee/payment;
- dining;
- library borrowing/access;
- computer-room charging;
- student-record connection;
- transfer/top-up;
- **WEB online query (and touchscreen)**;
- telephone voice service;
- bus charging;
- dorm access;
- campus-gate access;
- hot-water/bathing charging.

Evidence grade: **A-source / current-host caveat**.

Why not call this a verified 2004 Web capture:

- the document is an official dated 2004 institutional record;
- but it is being served now from a current university host/template;
- current DOM/CSS/headers/encoding are not evidence of the 2004 browser experience.

This distinction is essential:

**historical document content survives ≠ historical page presentation survives**.

Source:
https://www.qztc.edu.cn/cwc/2004/0409/c1127a41058/pagem.htm

---

### 3.3 2004–2005 Peking University: library credential migration

The library announced in December 2004 that from March 1, 2005 campus cards would be used for entrance and borrowing, replacing the former borrowing card.

The March 2005 university report then observed the access-gate system in use and explicitly noted:

- detecting invalid/lost credentials;
- recording exact entrance times;
- limited incompatibilities with some alumni/interlibrary credentials during trial operation.

Evidence grade: **A / official contemporary page content, current-host caveat for HTML form**.

This is strong evidence for a state transition:

`OLD_LIBRARY_CARD VALID`
`→ CAMPUS_CARD ACTIVATED FOR LIBRARY`
`→ OLD_CARD RETIRED`

but also for incomplete migration:

`main student/staff credential works`
`≠ every legacy visitor credential works`.

Sources:
https://www.lib.pku.edu.cn/portal/cn/news/0000000066
https://news.pku.edu.cn/xwzh/129-74710.htm

---

## 4. 2007–2010: user-facing routines become visible

### 4.1 2007 technical design: identity + bank + family remittance

A CERNET technical article on campus-card design states that campus cards could hold or reference identity information used for:

- library;
- access control;
- computer rooms;
- other management functions.

It also describes bank-card integration allowing parents to deposit money remotely through bank networks.

Evidence grade: **B / near-contemporary technical description**.

Important boundary:

**bank-network integration ≠ public Internet transaction**.

Parents could participate in a digital funds path even if neither side used a Web campus-card page.

Source:
https://www.edu.cn/ykt_6495/20070730/t20070730_246419_2.shtml

---

### 4.2 2008 student account: “one card” becomes daily dependence

A CERNET report includes a student describing the pre-one-card state as carrying:

- meal card;
- student/library card;
- computer-room card;
- bank card;
- cash.

After integration, dining, library use, computer access and small purchases depended on the campus card.

The report also describes:

- query password;
- consumption password;
- no-password spending limit;
- transaction records stored in databases;
- touchscreen self-query.

Evidence grade: **B**, with valuable **contemporary first-person** fragments.

This evidence is stronger for ordinary use than a vendor feature list, but it still describes one campus environment, not all Chinese universities.

Source:
https://www.edu.cn/ykt_6495/20080724/t20080724_311426.shtml

---

### 4.3 2008 Xiamen University: graduation as permission remapping

The university’s 2008 graduate card notice states that after graduation:

- the student campus card automatically changes into an alumni card;
- library/access-control identity functions expire;
- consumption function can remain;
- remaining wallet balance is not automatically seized/frozen.

Evidence grade: **A / official contemporary administrative notice**.

This is one of the clearest old-Web-era examples that:

**same physical card != same institutional role**.

State model:

`ROLE=STUDENT`
`→ GRADUATION EVENT`
`→ ROLE=ALUMNI`
`→ ACCESS ENTITLEMENTS REMOVED`
`→ WALLET/CONSUMPTION MAY PERSIST`.

Source:
https://xsc.xmu.edu.cn/info/1017/41181.htm

---

### 4.4 2009 Nankai University: real-time database + deliberate dual-running

Nankai’s official 2009 launch report says the new system served over 20,000 students and included:

- card;
- consumption;
- query;
- self-service;
- data center;
- integrated business systems;
- dining;
- bathing/water control;
- student arrival/registration;
- transfer/recharge terminals;
- city-card functions.

The report says each transaction/operation entered the database in real time and could be queried.

It also says the university did **not** immediately remove old dining/bathing systems; a period of dual operation was retained to reduce rollout risk.

Evidence grade: **A / official contemporary institutional report**.

This gives an important infrastructure principle:

**migration completeness is itself a historical state**.

Possible states:

`LEGACY_ONLY`
`→ DUAL_RUNNING`
`→ NEW_PRIMARY_WITH_FALLBACK`
`→ LEGACY_RETIRED`.

Never infer the last state merely because a launch article exists.

Source:
https://news.nankai.edu.cn/zhxw/system/2009/09/23/000025625.shtml

---

### 4.5 2010 mobile-one-card controversies: integration can create lock-in

Contemporary reports describe some universities combining campus-card functions with designated telecom operator/device plans. Students complained that campus access, dining, bathing or other ordinary services could become entangled with a particular phone service.

Evidence grade: **B / contemporary investigative reporting**.

This is important because it stops a teleological reading:

`more integration ≠ more user freedom`.

The technical state should be separated into:

`CAMPUS_ID ACCOUNT`
`↔ MOBILE/SIM CREDENTIAL`
`↔ TELECOM SUBSCRIPTION`
`↔ DEVICE COMPATIBILITY`.

If any of these are contractually coupled, a student’s access problem may originate outside the campus-card core.

Source:
https://tech.sina.com.cn/t/2010-09-06/11434624851.shtml

---

## 5. 2011–2015: B/S, mobile and portal layers thicken

### 5.1 2011 C/S → B/S language matters

A 2011 campus-card upgrade case for Shandong Jiaotong University contrasts an older C/S environment with a newer B/S system and explicitly notes that the older system made customer queries less convenient.

Evidence grade: **B / technical case**.

This is useful for old-Web archaeology because “online query” may refer to substantially different environments:

- dedicated client;
- campus-only Web app;
- public Web login;
- touchscreen running a Web front end;
- WAP/mobile page;
- native mobile client.

Do not collapse all of these into “website”.

Source:
https://www.asmag.com.cn/solution/201101/39459.html

### 5.2 2013 Dalian University of Technology: current page preserves a service constellation

The university’s 2013 “玉兰卡” material records:

- dedicated campus-card site references (`ecard` service family);
- 24-hour voice service;
- bank-to-campus transfer through self-service terminals;
- online transfer through China Construction Bank’s “悦生活”, followed by terminal confirmation;
- ATM transfer as another route;
- cash counter fallback;
- campus unified database and identity infrastructure.

Evidence grade: **A/B mix**.

The university page is official and dated, but again the currently served HTML is not a 2013 capture.

The top-up path is particularly useful:

`ONLINE BANK TRANSFER SUCCESS`
`→ TERMINAL CONFIRMATION / RECEIVE`
`→ CAMPUS WALLET USABLE`.

Therefore:

**online payment success ≠ campus value already available at POS**.

Source:
https://ecard.dlut.edu.cn/info/1011/1028.htm

---

## 6. The Web page is not the transaction

## 6.1 Balance-query shell gap

Historical archive may preserve:

```text
[学号/卡号]
[密码]
[登录]
```

but not:

- authentication service;
- session cookie logic;
- database endpoint;
- account ledger;
- user-specific result;
- historical transaction table.

So the highest safe claim from a shell capture may be:

> “A Web interface for account query existed at this URL/time.”

It is **not**:

> “This user had 32.50 yuan on that date.”

---

## 6.2 Help-page survival gap

Current university sites often still serve old announcements dated 2004–2013.

These are valuable historical documents, but they can be wrapped in:

- a modern CMS;
- UTF-8 instead of original GB2312/GBK;
- responsive CSS;
- rewritten image URLs;
- new navigation;
- modern analytics;
- HTTPS redirects.

Therefore:

**current live legacy article != historical capture != historical browser experience**.

---

## 6.3 Logged-in page gap

A public archive usually cannot preserve:

- private student balance;
- personal transaction history;
- personal access log;
- student record;
- bank-linked recharge account;
- session-only loss-report result.

That is not merely a technical failure; it is also an appropriate privacy boundary.

The repository should not attempt to reconstruct real historical student financial/access records from leaked or private data.

---

## 6.4 Dynamic state gap

Even if a Web response is archived, it may capture only one transient state:

- maintenance page;
- login timeout;
- zero-result query;
- error message;
- generic demo account.

One capture cannot be generalized to system behavior across the year.

---

## 7. Identity-state gaps

## 7.1 `student number != current entitlement`

A student number can remain known for decades.

It does not prove current:

- enrollment;
- meal subsidy;
- dorm access;
- library privilege;
- active campus-card wallet.

## 7.2 `card photo/name != account controller`

A physical card may be:

- lost;
- lent;
- rented;
- stolen;
- retained after graduation;
- held as a souvenir.

2008 reports of rented Peking University meal cards are direct evidence that physical possession can diverge from institutional ownership/eligibility.

Source:
https://www.chinanews.com.cn/edu/xyztc/news/2008/11-28/1466464.shtml

Thus:

**CARD_PRESENTED != RIGHTFUL_CARDHOLDER_PRESENT**.

## 7.3 `graduation != immediate database convergence`

Graduation can involve separate schedules for:

- academic record;
- card freeze;
- door access;
- wallet refund;
- bank refund;
- alumni-role creation.

Do not assume a single midnight transition unless the institution explicitly documents one.

---

## 8. Transaction-time gaps

Useful timestamps must be named.

For a dining transaction, possible times include:

- card presented;
- terminal approved;
- local record created;
- central database received;
- Web history updated.

For a door event:

- credential read;
- access decision;
- physical unlock;
- log persisted;
- log synchronized.

For loss report:

- request submitted;
- central status changed;
- blacklist exported;
- remote/offline reader updated.

So:

**database timestamp != necessarily physical event timestamp**.

And:

**Web history ordering != necessarily exact real-world ordering**.

---

## 9. Internet boundary: do not rewrite campus networking as public-Web history

### 9.1 Before full public Internet access

Chinese universities could already have:

- internal databases;
- library automation;
- campus networks;
- bank/private networks;
- electronic meal/payment systems;
- research-network connectivity.

This is not evidence that ordinary students had public Internet access to self-service accounts.

### 9.2 After 1994

Full-function Internet connectivity in China does not imply immediate campus-card Web adoption.

The relevant ladder is:

`institution backend exists`
`→ campus network exists`
`→ card system integrates`
`→ Web/self-service exists`
`→ ordinary students can reach it`
`→ students actually use it routinely`
`→ mobile/virtual credential becomes normal`.

Each rung needs its own evidence.

---

## 10. 2015 boundary: why this file stops here

Later mobile/NFC developments matter for life-history comparison but should not pull this repository’s core scope indefinitely forward.

For orientation only:

- 2018 Zhejiang University reporting shows virtual cards/mobile applications becoming important;
- 2020–2021 many campuses added QR/NFC/mobile credentials;
- 2020 pandemic access rules reused campus credentials alongside health-state systems;
- 2019 onward campus transaction data was increasingly used for student aid;
- 2025 university notices show explicit digital deprovisioning at graduation.

Those later developments belong primarily in the companion `how-people-lived` note.

This old-Web file uses them only to clarify which earlier state boundaries survived.

---

## 11. Archive visibility bias

Campus-card history has a particularly severe archive asymmetry.

### 11.1 What is likely to survive publicly

- implementation announcement;
- IT-center help page;
- card-office hours;
- public user guide;
- FAQ;
- vendor case study;
- system architecture diagram;
- public login shell;
- graduate card notice.

### 11.2 What is likely to disappear

- authenticated balance;
- consumption ledger;
- access history;
- blacklist propagation log;
- POS outage log;
- one student’s failed top-up;
- wrong identity binding;
- dorm reader offline period;
- bank-side reconciliation state;
- terminal firmware;
- private support ticket.

Therefore:

**archive-visible campus card = mostly institutional description, not ordinary transaction history**.

### 11.3 A success bias

Official news tends to preserve launches and successful transaction counts.

Users’ failures are more likely to survive only if they became:

- complaints;
- newspaper stories;
- forum posts;
- support notices.

So the archive will tend to overrepresent both “successful rollout” and “spectacular problem”, while underrepresenting mundane intermittent friction.

---

## 12. Browser / protocol assumptions to record in future captures

For every historical campus-card Web object, record when possible:

- original URL;
- capture datetime;
- HTTP/HTTPS;
- charset (`GB2312`, `GBK`, `UTF-8`, unknown);
- frameset/table layout;
- form action;
- GET/POST;
- cookie/session dependence;
- JavaScript requirement;
- ActiveX/Java dependency, if any;
- bank plug-in/certificate dependency;
- Internet Explorer compatibility claim;
- whether page is public, campus-only, VPN-only or login-only;
- whether balance/result endpoint is a separate host;
- whether images/CSS/JS survive;
- whether archive rewrite changes form behavior.

Do not infer IE-only behavior unless a historical manual/page states it or an old-browser replay demonstrates it.

---

## 13. Evidence table

| Date | Object | Evidence | Grade | Narrow claim | Important limit |
|---|---|---|---|---|---|
| 2003-09 | Lanzhou University campus IC case | Sina Technology | B | multi-service card integration existed at at least one major university | vendor/case framing; no exact Web UI |
| 2004-04 | Quanzhou Normal University management rules | university official | A-source/current-host caveat | campus-network/database system explicitly included Web query, IVR, gates, dining, transfer | current HTML is not 2004 capture |
| 2004-12 | Peking University library migration notice | university official | A | campus card scheduled to replace borrowing card | does not prove all readers worked that day |
| 2005-03 | PKU library gate report | university official | A | card used for access; lost-card invalidation and time logging described | some legacy card types still problematic |
| 2007 | campus-card design description | CERNET | B | identity + bank/network integration and family remote funds path | not a national adoption measure |
| 2008-06 | Xiamen graduate card rules | university official | A | student card could transition to alumni role with selective entitlement loss | one university policy |
| 2008 | student one-card use | CERNET | B + contemporary self-report | ordinary student described multi-card→one-card daily use | campus-specific |
| 2008-11 | PKU meal-card rental | Beijing Morning Post/China News | B | physical card possession diverged from authorized user | reports informal behavior, not prevalence |
| 2009-09 | Nankai launch | university official | A | real-time transaction DB, 20k+ students, dual-running migration | official success report; no raw logs |
| 2010 | mobile-one-card bundling dispute | Computer News/Sina | B | some schools coupled credential to telecom/device choice | cannot generalize nationally |
| 2011 | C/S vs B/S upgrade case | technical case source | B | query convenience and architecture transition documented | vendor/implementation framing |
| 2013 | Dalian “Yulan Card” | university official | A/B | Web/voice/terminal/bank paths coexisted | current server is not historical capture |

---

## 14. Confirmed / probable / unknown

### Confirmed in this slice

- By 2003–2004, at least some Chinese universities had integrated campus-card systems linking multiple identity, payment and access functions.
- A 2004 official university regulation explicitly listed Web online query alongside touchscreen and telephone voice service.
- Campus-card infrastructure relied on campus networks, databases and private/bank networks; public Web was only one interface.
- By 2005 at PKU, campus card use included library access and logging of entry time.
- By 2008, contemporary students could describe one card replacing multiple daily cards/cash.
- By 2009, Nankai documented real-time transaction/operation data and a deliberate dual-run migration period.
- Graduation could remap rights without replacing the physical card, as Xiamen’s 2008 student→alumni card rule shows.
- Integration could create provider lock-in, as 2010 mobile-card controversies show.

### High probability, but still architecture-specific

- Many systems used a central account/identity layer plus multiple readers/POS subsystems.
- Web self-service increasingly exposed balance, transaction, loss-report and recharge functions during the 2000s–2010s.
- Offline/online synchronization timing was a meaningful operational issue in some implementations.

Do not turn these into universal claims without institution-specific manuals.

### Unknown / not established here

- Which Chinese university had the first true campus-wide one-card system under a strict definition.
- Exact historical HTML/DOM/browser appearance of the 2004 Quanzhou Web query page.
- Historical URLs for many authenticated account endpoints.
- Whether specific early systems stored value on-card, centrally, or in hybrid form.
- Blacklist propagation latency after Web loss-report in individual systems.
- Exact bank-settlement/ledger consistency guarantees.
- How frequently ordinary users chose Web vs touchscreen vs IVR vs counter.
- Failure rates and accessibility for disabled users.

---

## 15. Historical capture work in this slice

### Targets attempted

Candidate old-Web target families included:

- early university `ecard` hosts;
- `card.tsinghua.edu.cn` service family;
- public campus-card help/query locators;
- 2003–2009 university campus-card documentation.

Direct CDX requests were attempted for examples including `ecard.dlut.edu.cn` and `card.tsinghua.edu.cn` with historical-year filters.

### Result

The current Web-access tool rejected direct constructed CDX URLs as unsafe unless the exact URL had first appeared in a search result. Search did not surface an exact replay that could be opened and inspected.

Therefore this slice did **not** obtain a capture for which all of the following could be verified:

- archive source;
- capture URL;
- original URL;
- capture datetime;
- HTTP state;
- charset;
- historical DOM;
- form action;
- cookie/session behavior;
- CSS/JS/subresources;
- authenticated result behavior.

### M1 status

**M1: NOT ACHIEVED IN THIS SLICE.**

Correct negative wording:

> “This research run did not verify a qualifying historical campus-card Web capture.”

Incorrect wording:

> “Wayback did not preserve campus-card sites.”

The latter is not supported.

---

## 16. Candidate future archaeology targets

If the repository later revisits this topic, high-value targets are:

1. a 2003–2006 public campus-card login/query page with ≥2 historical captures;
2. a user manual showing exact historical URL patterns and browser requirements;
3. an archived loss-report form plus contemporary manual explaining propagation timing;
4. a campus-card bank-transfer page showing bank plug-in/certificate requirements;
5. a B/S self-service page that can be compared with a prior C/S client manual;
6. a historical screenshot/capture of touchscreen Web UI;
7. a campus forum thread reporting a real failed top-up or lost-card timing, with privacy minimized;
8. a university migration notice documenting old/new system overlap.

Do not collect real student account identifiers or private financial/access records merely to make the reconstruction look more complete.

---

## 17. Cross-link back to ordinary life

The old-Web archaeological lesson changes the life-history interpretation in one important way.

A student in 2008 could say “我每天都离不开校园卡”, but the object he or she touched was only the last few centimeters of a large institutional stack:

`student registry`
`+ bank network`
`+ campus database`
`+ POS/gate readers`
`+ campus network`
`+ query/voice/terminal/Web interfaces`
`+ card-office fallback`.

The Web made some of those hidden states directly visible and actionable to ordinary users—query, loss report, recharge, records—but it did not create the underlying system.

That distinction is exactly why Chinese pre-1994 and early-Internet history must not be flattened into “before Internet / after Internet”.

The better historical question is:

> **Which part of an already-digital institutional system became directly addressable by an ordinary student, through which interface, at what time, and what real-world permission changed after the click?**

That is the old-Web object here.
