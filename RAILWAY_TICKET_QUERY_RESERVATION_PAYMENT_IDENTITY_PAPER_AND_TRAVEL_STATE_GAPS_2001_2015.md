# Railway ticket query, reservation, payment, identity, paper and travel state gaps, 2001–2015

> Scope: Chinese old Web / Web-adjacent railway passenger systems, roughly 2001–2015.
>
> Cross-life-history note: `tmzncty/how-people-lived/topics/from-station-queue-and-telephone-booking-to-12306-rail-ticketability-return-home-executability-and-mobility-options-china-1996-2026.zh-CN.md`
>
> This file does **not** attempt a general history of Chinese railways or Spring Festival travel. It asks a narrower archaeology question: when a historical Chinese railway page says a train, seat, order, payment, ticket, identity or refund existed, what exact state did the Web page know, what authority sat behind it, and what can an archive actually preserve?

## 0. Why railway booking needs its own state model

A railway trip looks simple to a passenger, but Web ticketing crosses many distinct authorities:

```text
timetable / service plan
→ train operation plan
→ inventory pool
→ origin-destination allocation
→ public query
→ displayed availability
→ user / passenger identity state
→ reservation / order request
→ seat hold
→ payment instruction
→ bank/payment result
→ ticket issuance / transport entitlement
→ paper ticket exchange, if required
→ station identity / gate validation
→ actual boarding
→ train operation
→ connection / final arrival
```

Refund and change introduce another branch:

```text
change / refund request
→ railway order state changes
→ seat may return to inventory
→ accounting / payment instruction
→ bank settlement
→ passenger actually receives funds
```

The following claims are therefore never interchangeable:

**train listed != train operates**  
**seat displayed != seat lockable now**  
**order submitted != seat held**  
**bank debited != ticket issued**  
**Web purchase != paperless boarding**  
**ID data entered != identity verified**  
**ticket issued != passenger boarded**  
**refund shown on Web != money settled to bank account**  
**“no ticket” for one segment != physically no empty seat anywhere on the train**.

This is the rail-specific version of this repository's `platform / site / account / page / capture / claim` discipline.

---

## 1. Boundary prehistory: the public Web inherited a national ticketing backend

The repository's main scope remains Chinese Web history around 1995–2015. A short prehistory is necessary because railway computerization did not begin with 12306.

A 2012 near-contemporary account from engineers/operators of the railway ticketing system says the national passenger-ticket system was made a major “Ninth Five-Year Plan” research project from 1996. It describes version 1.0 as replacing manual hard-card ticket sales with computer ticketing, 2.0 as regional networking, 3.0 as national networked ticket sales, 4.0 as connection to clearing/settlement, 5.0 as seat reuse/shared inventory, and 5.2 as adding real-name ticketing, electronic ticket and electronic payment capabilities.

Source:
- People.cn report preserved by CNTV, 2012-01-13: <https://jingji.cntv.cn/20120113/115500.shtml>

Evidence status: **A/B — near-contemporary system/operator account**. It is strong for the system's claimed lineage and topology, but still partly self-description. It does not independently prove exact national rollout dates at every station.

The core archaeological rule is:

> **public-Web emergence != railway reservation-computing emergence.**

A passenger in the late 1990s could still stand at a physical window while that clerk was querying a networked seat database. Backend digitization may therefore be visible in transaction latency and cross-station sellability even when the household owns no computer.

### State gaps introduced before the Web

#### `window-interface / backend-network gap`
A physical paper ticket does not imply a non-digital transaction. The visible artifact may have been produced from a networked inventory system.

#### `national-system / local-capability gap`
A national system version can exist while stations, routes or equipment are rolled out unevenly.

#### `paper-artifact / inventory-authority gap`
The passenger-facing paper represents a backend entitlement; the paper alone does not reproduce the live seat-allocation state that created it.

---

## 2. Web chronology must separate information service from transactional ticketing

The same 2012 operator account says a 12306 customer-service website went online on 2010-01-30 with route-planning, timetable, train-status and remaining-ticket queries, while transactional Internet ticket sales were rolled out in stages from 2011-06-12 through the end of 2011.

Source:
- <https://jingji.cntv.cn/20120113/115500.shtml>

This creates a basic chronology rule:

```text
railway information available on Web
!=
Web can reserve inventory
!=
Web can accept payment
!=
all trains available online
```

A historical 2010 screenshot of 12306 is not automatically evidence of online purchase capability. Likewise, a later 2011 purchase page should not be backdated to the site's information-only phase.

---

## 3. 2011: the railway transaction enters the browser — with browser-specific friction

### 3.1 Staged rollout is itself a state boundary

The railway account says online sales opened first for Beijing–Tianjin intercity trains on 2011-06-12, Beijing–Shanghai high-speed on 2011-06-24, all EMU trains by 2011-09-30, then Z/T/K and other passenger trains in stages through December.

Source:
- <https://jingji.cntv.cn/20120113/115500.shtml>

Therefore an archive from July 2011 cannot be interpreted with December 2011 product coverage.

A Web form may look generic while the transaction backend is route/product constrained.

### 3.2 Exact historical original-URL evidence

Contemporary reports and user notes expose historical public entry points including:

- `http://www.12306.cn/mormhweb/`
- `http://www.12306.cn/mormhweb/kyfw/`

A November 2011 user technical note explicitly links the passenger-service area as:

- `http://www.12306.cn/mormhweb/kyfw/`

Source:
- contemporary user technical note, 2011-11-22: <https://www.cnblogs.com/longware/archive/2011/11/22/13382228.html>

These are **candidate historical original URLs**, not verified archive captures in this research slice.

### 3.3 Browser compatibility is part of ticketability

A June 2011 *Beijing News* test reported that customer service described the site as developed around IE standards and supporting IE6+, while tests in Chrome, Firefox, Safari and Opera encountered login, garbling or purchase problems.

Source:
- *Beijing News*, preserved by Sina, 2011-06-15: <https://news.sina.com.cn/c/2011-06-15/084622643844.shtml>

Evidence status: **B — contemporaneous independent browser test**.

The contemporaneous user note cited above records additional issues involving HTTP/HTTPS framing, certificate warnings, calendar behavior and switching browsers for different stages of a booking/payment flow.

Evidence status: **T0/B — contemporaneous user report, useful for existence of one experienced failure path, not prevalence**.

Permanent state distinctions:

```text
browser can render home page
!= browser can log in
!= browser can render booking controls correctly
!= browser can submit order
!= browser can complete bank payment
```

### Browser archaeology warning

A modern browser successfully replaying the page proves almost nothing about the 2011 user experience. A proper M1 capture would need at minimum:

- original URL and archive capture URL;
- capture datetime;
- HTTP / archive replay status;
- historical charset / Content-Type where recoverable;
- DOM and form actions;
- script and iframe dependencies;
- certificate / HTTPS assumptions;
- archive URL rewriting effects;
- at least one second historical time point.

Do **not** infer ActiveX, a specific JavaScript framework, IE document mode, GB2312, or exact TLS behavior merely from the year.

---

## 4. Web purchase did not mean paperless travel

On 2011-09-30, contemporary local reporting from Shijiazhuang said nationwide EMU online sales had begun, but passengers at Shijiazhuang still needed to exchange the online/electronic purchase for a paper ticket because direct second-generation-ID gate use was not then available there.

Sources:
- China News / *Yanzhao Evening News*, 2011-09-30: <https://www.chinanews.com/cj/2011/09-30/3365703.shtml>
- Sina-preserved *Yanzhao Metropolis Daily*, 2011-09-30: <https://news.sina.com.cn/o/2011-09-30/070023242267.shtml>

This is a critical transaction-state boundary:

```text
Web ticket purchase
→ backend transport entitlement
→ [station-capability dependent]
→ direct ID entry OR paper-ticket exchange
```

Therefore:

**electronic purchase != paperless journey**.

A historical help page saying “online ticketing available” cannot be used to infer that a passenger at every station could walk directly to the gate with an ID card.

### `network-wide product / station-edge capability gap`

The transaction core and the physical station edge can be upgraded at different speeds.

This is exactly the kind of distributed system state that static Web archaeology tends to flatten.

---

## 5. Identity itself became a transaction state

Online railway purchase layered real-name passenger identity onto an account system.

By late 2015, reports about 12306 mobile “two-way verification” show that account use could depend on phone verification state as well as passenger identity data.

Source:
- Xinhua via People.cn, 2015-12-02: <https://money.people.com.cn/n/2015/1202/c42877-27882454.html>

The relevant objects must remain separate:

```text
physical person
!= Web account
!= account phone
!= passenger record
!= identity-document number
!= railway verification state
!= order passenger
!= person appearing at station
```

Permanent distinctions:

- `account registered != phone verified`
- `passenger added != passenger identity verified`
- `identity verified != ticket inventory available`
- `identity accepted by Web != physical ID accepted at station edge`

### Privacy boundary

Passenger names, ID numbers, mobile numbers, order numbers and ticket records are sensitive transactional data. Even if a historical archive happens to expose them, this repository should prefer field/schema analysis and redact ordinary-person identifiers unless strictly necessary for a narrow claim.

---

## 6. 2012 Spring Festival: payment, order and refund states become publicly visible through failure

The 2012 Spring Festival surge is unusually useful archaeologically because infrastructure stress exposed hidden state boundaries.

The railway operator account says that from January 5, page views exceeded one billion per day for five consecutive days. It explicitly acknowledges cases where the bank had successfully processed a payment but congestion prevented the railway website from receiving the complete success result, producing cases where the user had paid while the website showed that ticket purchase was unsuccessful.

It also says complaints included:

- online payment succeeded but booking did not succeed;
- refund/change had been processed on the Web or at station but money had not yet arrived.

Source:
- <https://jingji.cntv.cn/20120113/115500.shtml>

This is strong evidence for a distributed transaction model:

```text
railway order state
        ↕
payment platform / bank state
        ↕
user-visible Web state
```

These can temporarily diverge.

### Permanent 2012 state gaps

#### `submit / accept gap`
Clicking “submit order” does not prove the order service accepted and held inventory.

#### `bank debit / railway issuance gap`
Money leaving the bank account does not prove the railway issued a ticket.

#### `railway refund / bank settlement gap`
A railway order marked refunded does not prove funds have reached the passenger's account.

#### `visible error / final transaction outcome gap`
A browser error may occur while one backend subsystem has already committed state.

### Archive consequence

A screenshot of an error page is often much easier to preserve than bank settlement logs or the eventual reconciled order. Therefore a surviving complaint screenshot should be treated as evidence of a **user-visible intermediate state**, not automatically the final transaction outcome.

---

## 7. High-demand release times expose the difference between Web shell and inventory authority

The 2012 railway account says the system intentionally limited concurrent login and order submission during peaks, and that errors were especially common at major release times.

Source:
- <https://jingji.cntv.cn/20120113/115500.shtml>

This matters because the historical Web page itself was not “the ticket pool”. It was a projection and command surface over the passenger-ticket system.

A proper state topology is closer to:

```text
browser
→ Web edge / session state
→ booking service
→ passenger identity rules
→ segment inventory / allocation
→ payment rail
→ ticket issuance
```

Thus a fully preserved HTML form cannot reconstruct what inventory the backend would have returned at 08:00 on a particular 2012 sales day.

This creates the repository pattern:

## `query-shell survival / inventory-state loss`

The reusable form is public and crawlable; the historical answer to a specific origin/date/train/segment query is ephemeral, backend-derived and often lost.

---

## 8. 2013 redesign evidence must be separated from production evidence

A 2013 *Beijing News* report on a preview/redesign described a new `https://kyfw.12306.cn/` passenger-service interface and noted categories for ordinary passengers, students and migrant workers, plus mobile-app download/QR elements. The same report also described temporary access/network problems during reporter tests.

Source:
- People.cn syndication, 2013-12-01: <https://cpc.people.com.cn/n/2013/1201/c64387-23707135.html>

Evidence status: **B — contemporaneous report about a preview/redesign**.

Claim limit:

> this is evidence that such a redesign/preview was observable and that this host was associated with it at that moment.

It is **not** enough to claim:

- that every user immediately received this exact layout;
- that all mobile links worked;
- that the preview DOM equals the later stable production DOM;
- that a current page at the same host reflects the 2013 implementation.

Permanent rule:

**preview visible != production stable**.

---

## 9. 2015: human verification, automation resistance and identity verification become interface history

By 2015, image-based CAPTCHA and account/phone/identity verification were visible parts of the railway Web transaction.

Contemporary reporting on mobile two-way verification confirms that a user could move into a state where further purchase required completing phone verification.

Source:
- <https://money.people.com.cn/n/2015/1202/c42877-27882454.html>

Other 2015 reporting documented user complaints that image CAPTCHA could consume enough time for scarce inventory to change before order submission.

This is important archaeologically because a CAPTCHA is not merely decoration. It is a transaction gate:

```text
inventory visible at T1
→ user solves challenge
→ order reaches backend at T2
```

If inventory is scarce, T1 and T2 can produce different availability.

### `human-verification / inventory-latency coupling`

The user-interface burden itself can alter whether a displayed opportunity remains executable.

A screenshot preserving a CAPTCHA challenge but not its backend validity window or order timestamp cannot reconstruct the transaction.

---

## 10. Railway “availability” is not a simple physical-seat fact

Later evidence falls outside this file's main Web-era scope but clarifies a state distinction that must also govern interpretation of old pages.

In 2026 the railway's 12306 technical center publicly explained cases where a long route shows tickets while a shorter segment of the same train shows “no ticket”: long-distance trains use an allocation strategy described as “long-distance priority, while also considering medium/short distance”, with segment quotas preallocated and dynamically adjusted.

Source:
- Xinhua carried by CCTV, 2026-02-15: <https://news.cctv.cn/2026/02/15/ARTIgCDtEGPKJFGxhnY9tMic260215.shtml>

This modern explanation should **not** be backdated as proof of the exact 2011 allocation algorithm. It does, however, protect a general archaeology rule:

> **a Web result saying “no tickets” is a sellability state for a specific segment/query/rule set, not necessarily a statement about every physical seat on the full train.**

For historical pages, avoid phrases like “the train was full” unless evidence actually establishes occupancy rather than sales status.

---

## 11. Archive survival asymmetries

Railway ticketing creates several recurring archival inversions.

### 11.1 `query-shell survival / inventory-state loss`

Likely to survive:
- origin/destination fields;
- date selector;
- train list shell;
- help text;
- button labels.

Likely to be lost:
- the exact inventory snapshot returned at that second;
- segment allocation state;
- concurrent holds by other users;
- release/reallocation events.

### 11.2 `order-page survival / seat-hold loss`

A screenshot may show an order page, but not whether its hold was still valid five seconds later.

### 11.3 `payment-page survival / settlement-state loss`

A page can show “payment submitted” while the bank and railway later reconcile differently. Public archive replay cannot recreate settlement authority.

### 11.4 `ticket-artifact survival / boarding-state loss`

A paper/e-ticket artifact proves a transport entitlement existed, but usually not whether the passenger reached the station or boarded.

### 11.5 `refund-page survival / bank-return loss`

A historical Web record may say “refunded”; the actual bank credit is private and normally absent from public archives.

### 11.6 `Web-session survival / identity-state loss`

Generic pages may survive while the account's real-name verification, phone binding and passenger-record state are intentionally inaccessible.

### 11.7 `browser-replay / historical-execution gap`

Archive rewriting, current TLS policies, missing scripts, expired certificates and modern JavaScript behavior can make an old page look broken in ways that differ from 2011 — or make a page render now that was unusable in a period browser.

---

## 12. Browser / encoding / implementation assumptions: keep UNKNOWN where evidence is insufficient

Contemporary reporting supports an **IE preference/dependency claim** for early Internet ticketing, but this research slice does **not** yet possess a verified historical 12306 DOM capture sufficient to assert:

- exact document mode;
- ActiveX dependence;
- exact charset on each transaction page;
- exact JavaScript libraries;
- exact form actions;
- session-cookie structure;
- precise certificate chain;
- whether specific HTTP/HTTPS behavior observed by one user was universal.

Therefore these remain **UNKNOWN pending M1 capture**.

The correct repository posture is to preserve the browser-compatibility evidence without reconstructing a technical stack from cultural memory of “IE-era Chinese websites”.

---

## 13. Archive reconnaissance in this slice

Historical original-URL candidates identified from contemporary sources include:

- `http://www.12306.cn/mormhweb/`
- `http://www.12306.cn/mormhweb/kyfw/`
- `https://kyfw.12306.cn/` (2013 redesign/preview period)

A direct historical-archive/CDX attempt was made for the 2011 passenger-service URL, but this research slice did not obtain and inspect a capture satisfying the repository's minimum M1 contract.

### Current status

**M1 verified historical 12306 booking/search/payment capture: NOT ACHIEVED IN THIS SLICE.**

This means only:

> no capture has yet been opened and verified here with sufficient provenance and technical detail.

It does **not** mean:

> Wayback / another archive has no relevant capture.

### Required next verification

For each candidate capture, record:

1. archive source;
2. capture URL;
3. exact original URL;
4. capture datetime;
5. access date;
6. HTTP/replay status;
7. whether it is a redirect/error/login/robots placeholder;
8. Content-Type and charset where reliably observable;
9. DOM/form structure;
10. scripts, iframes, styles and other subresources;
11. archive-rewrite effects;
12. second historical time point for comparison.

Priority targets:

- 2011 passenger-service landing page;
- remaining-ticket query page;
- registration / certificate instructions;
- order/payment help pages from 2011–2012;
- 2013 `kyfw.12306.cn` redesign.

---

## 14. Evidence ledger

| Claim | Evidence | Grade | Confidence / limit |
|---|---|---:|---|
| Passenger ticketing backend predates public Web sales | 2012 operator/system account | A/B | high for stated lineage; station-by-station rollout not independently verified here |
| 12306 initially served info/query before transactional rollout | 2012 operator account | A/B | high for platform-stated chronology |
| Internet ticket sales expanded in stages during 2011 | 2012 operator account + contemporaneous local reports | A/B | high |
| Early purchase could be browser-dependent | 2011 *Beijing News* test + user technical note | B + T0/B | high for existence; prevalence unknown |
| Web purchase could still require paper exchange | 2011 Shijiazhuang reports | B | high locally; not national uniformity |
| Payment/order/refund states could diverge under 2012 congestion | operator account + contemporaneous complaints | A/B | high for existence |
| Phone/account/identity verification later affected purchase state | 2015 reporting | B | high for feature existence |
| Generic old Web page cannot reproduce historical inventory | system topology + archive method | D grounded in A/B evidence | high as reconstruction constraint |
| Exact old DOM/charset/scripts | no M1 capture yet | — | UNKNOWN |

---

## 15. Cross-national comparator belongs mainly in `how-people-lived`

For archaeology method, one overseas comparator is useful. French Senate records from 1988/1989 say TGV reservation could be made at station windows, travel agents, rapid distributors or Minitel while all channels queried one central reservation server. Remote reservations could be released if not collected in time.

Source:
- <https://www.senat.fr/questions/base/1988/qSEQ881202718.html>

A 1990 *Le Monde* report describes a limited experiment adding Minitel payment, requiring chip-card hardware and still allowing ticket collection or mailing.

Source:
- <https://www.lemonde.fr/archives/article/1990/02/21/monetique-les-dispositifs-anti-fraudeurs-se-multiplient-pour-payer-par-minitel-en-toute-securite_3957116_1819218.html>

The comparator is not evidence about Chinese implementation. It supports two general reconstruction cautions:

1. **remote reservation can predate the Web**;
2. **multiple user-facing channels can share one authoritative inventory backend**.

That topology is exactly why an archived public page is not the inventory itself.

---

## 16. What this changes in old-Web archaeology

Railway ticketing is a useful corrective to screenshot-centered old-Web history.

A preserved 2011 12306 page might tell us:

- which fields a traveler saw;
- which browser assumptions were published;
- what words were used for orders, payment and identity;
- which actions were exposed to the public Web.

But the parts that actually decided whether someone went home — live segment inventory, seat holds, bank settlement, identity verification, station edge capability, train operation and final boarding — mostly lived **outside the HTML**.

So the key lesson is:

> **a historically accurate railway page reconstruction can still be an inaccurate reconstruction of the historical journey.**

For this object, the Web shell is only one layer in a transaction distributed across reservation, identity, payment and physical transport systems. Old-Web archaeology should preserve the shell, but it must also preserve the gaps between what the shell displayed and what the passenger could actually do.