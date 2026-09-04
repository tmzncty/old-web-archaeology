# Online appointment, ticket-booking, digital-queue and offline-fulfillment state gaps, 2009–2015

Status: research note / evidence-model extension  
Repository scope: **Chinese Web / Chinese Internet service environment, approximately 1995–2015**  
Cross-project companion: `tmzncty/how-people-lived/topics/queues-waiting-release-time-synchronization-and-delegated-waiting-china-1980s-2026.zh-CN.md`

## Why this belongs in Old Web Archaeology

A historical booking page is unusually easy to over-interpret.

A preserved page may show:

- a doctor name and an “预约” button;
- a train with “有票”; 
- a form saying an order was submitted;
- a “排队处理中” message;
- an appointment confirmation page;
- a payment button;
- a booking rule explaining pickup or check-in.

None of those, by itself, proves that the historical user ultimately received the scarce service.

For appointment and ticket systems, the archaeological object is not merely a page. It is a distributed transaction spanning:

- public Web pages;
- authenticated accounts;
- identity databases;
- inventory / quota state;
- release schedules;
- backend queues;
- payment gateways;
- SMS / phone notification;
- counter or machine pickup;
- offline identity checking;
- the eventual clinic visit or railway journey.

Therefore:

> **page state ≠ transaction state ≠ entitlement state ≠ offline fulfillment.**

This note models those gaps for Chinese old-Web appointment and ticket-booking systems, using 2009 hospital booking and 2011–2015 railway online ticketing as bounded cases.

Privacy rule: do **not** retrieve, correlate, publish or reconstruct historical patients' medical-card numbers, identity numbers, real booking accounts, ticket order numbers, private appointment records, phone numbers, payment records or travel histories.

---

# 1. Scope boundary

This repository remains focused on the Chinese Web and its access environment around **1995–2015**.

The long prehistory of physical queues, telephone reservation, French Minitel and later 2020s waitlist/pre-order systems belongs mainly in `how-people-lived`. They can be referenced here to clarify mechanisms, but they do not expand this repository into a global history of queues.

Likewise, this note does not attempt a full history of:

- Chinese hospitals;
- railway ticketing as an institution;
- Spring Festival migration;
- healthcare inequality;
- transport capacity.

The narrow archaeological question is:

> **What does a surviving Web artifact actually prove about a historical reservation or ticket transaction?**

---

# 2. Minimal state machine

A defensible generic booking chain is:

```text
public information page exists
→ service / train / doctor is discoverable
→ user has a usable account or permitted anonymous route
→ required identity / card / passenger data are accepted
→ booking window is open
→ inventory / slot is displayed as available
→ user selects an item
→ request is submitted
→ backend accepts request into processing / queue
→ inventory may be temporarily held
→ order / reservation is created
→ required payment succeeds within deadline
→ system records confirmation
→ notification / order identifier is available
→ user reaches required offline location
→ pickup / check-in / identity verification succeeds
→ service is actually delivered / journey actually occurs
```

There can also be branches:

```text
request submitted
→ queue waits
→ inventory exhausted
→ request fails
→ user retries / changes channel / changes train / changes doctor
```

and:

```text
reservation created
→ payment not completed in time
→ reservation expires
→ inventory returns to pool
```

and:

```text
reservation confirmed
→ user misses pickup/check-in deadline
→ reservation is void / service not consumed
```

Each arrow is a separate evidence problem.

---

# 3. Gap taxonomy

## 3.1 availability-snapshot gap

A page saying `有票`, `可预约` or showing a selectable slot proves, at best, what the interface reported at one moment.

It does not prove:

- inventory was still available milliseconds later;
- another channel did not consume it;
- the interface was synchronized with backend inventory;
- the user's later submission received the same state.

Historical archives freeze a dynamic availability state into a misleadingly static artifact.

## 3.2 release-time gap

A help page may say inventory opens at a certain time.

That proves the stated rule, not:

- the backend actually exposed every item at exactly that second;
- all channels shared the same release time;
- the page was cached;
- the user knew the rule;
- the user was already authenticated and ready.

## 3.3 registration / account-state gap

A public booking page can survive while the authenticated registration system is gone.

The page does not prove whether a historical user had:

- a registered account;
- a valid password;
- required email/phone access;
- a verified identity;
- a usable medical card / passenger profile;
- an account not locked by prior failures.

## 3.4 identity-binding gap

Real-name systems create several linked subjects:

```text
account holder
→ presented identity record
→ patient / passenger subject
→ medical card / frequent passenger entry
→ payment subject
→ person who actually arrives
```

These may coincide, but must not be assumed to be identical.

A family member can operate an account for an older parent; one account can contain multiple passengers; a telephone booking can be collected by another person under permitted rules.

Do not collapse `operator` into `service subject`.

## 3.5 submission / queue-admission gap

A user pressing `提交订单` proves neither that the server received the request nor that it entered the transaction queue.

A historical screenshot of “正在提交” may correspond to:

- client-side waiting;
- HTTP request in flight;
- reverse proxy overload;
- application queue admission;
- database transaction processing;
- timeout after partial work.

Without backend evidence, do not assign an internal implementation.

## 3.6 queue-position opacity gap

A digital queue message such as “预计等待 30 分钟以上” is an interface claim about processing state.

It does not necessarily expose:

- exact position;
- ordering rule;
- inventory reserved for queued users;
- queue length;
- whether estimate can increase;
- whether other channels share inventory.

## 3.7 inventory-race gap

A user may see availability but lose it between query and order creation.

Therefore:

> **inventory displayed ≠ inventory held.**

This gap is especially important for scarce railway tickets and expert appointments.

## 3.8 payment-window gap

An order may exist only as a temporary hold until payment is completed.

So:

`order created ≠ paid order`.

Historical payment pages are often external or authenticated and poorly archived; this creates systematic missingness exactly at the point where a tentative transaction becomes a paid entitlement.

## 3.9 reservation / fulfillment gap

A confirmed reservation can still require:

- physical ticket pickup;
- hospital number collection;
- identity-card verification;
- arrival before a deadline;
- check-in / report;
- final service acceptance.

Thus:

> **online success ≠ offline completion.**

## 3.10 cancellation / release gap

Inventory can re-enter the pool after:

- cancellation;
- payment timeout;
- missed pickup;
- schedule change;
- refund / rebooking.

A later user may acquire an item that did not exist when an earlier archive capture was made.

## 3.11 cross-channel inventory gap

Telephone, Web, counter, community referral, self-service machine and mobile app can coexist.

Do not assume:

- identical quotas;
- identical pre-sale windows;
- identical cancellation rules;
- identical identity requirements;
- identical pickup requirements.

A historical Web page is only one interface into a multi-channel allocation system.

## 3.12 anti-bot / throttling-state gap

Rate limiting, CAPTCHA, queueing, identity verification or risk controls may activate dynamically.

A capture made under low load cannot prove high-load behavior.

Conversely, a screenshot of a CAPTCHA or queue cannot prove every user saw it.

## 3.13 public-page / private-order gap

The public rules may be preserved for decades while the user's actual order database is inaccessible or correctly private.

That is not merely an archive failure. Some of the most important state is **supposed to be private**.

---

# 4. 2009 Beijing Chaoyang Hospital: a clean example of online reservation requiring offline closure

A Beijing Health Bureau item republished by Sina on **2009-09-07** stated that Beijing Chaoyang Hospital opened online appointment booking on September 1. It also described telephone, window, follow-up and community booking routes.

Contemporaneous source / A-B institutional content:
- https://news.sina.com.cn/c/2009-09-07/112616254859s.shtml

The page states that online booking required prior registration and real identifying information, and that an online reservation for a morning visit had to be collected at designated windows from **09:30 to 10:00**; after **10:30**, an uncollected online reservation was treated as void.

### Archaeological consequence

A preserved “预约成功” artifact would prove only an intermediate state.

The real chain was closer to:

```text
public hospital page
→ online booking platform
→ registration
→ identity / medical-card data accepted
→ 1–7 day slot selected
→ reservation recorded
→ patient travels to hospital
→ patient reaches correct window during pickup interval
→ identity/card check
→ number collected
→ clinical queue / visit
```

The source therefore directly supports:

> `online reservation recorded ≠ clinic number collected ≠ doctor actually seen`.

### Browser / Web uncertainty

The institutional text identifies the historical hospital homepage and booking function, but this run has **not verified a preserved 2009 authenticated booking session**.

Therefore this note does **not** assert:

- exact HTML form fields;
- character encoding;
- JavaScript behavior;
- browser requirements;
- session-cookie implementation;
- whether specific historical subresources survive.

Those require a verified capture.

---

# 5. 2009 Beijing system-level adoption: existence must not be collapsed into normality

Beijing health authorities later summarized that from **2009-09-01 through 2009-12-31**, the city's 49 tertiary hospitals recorded about 1.234 million appointment registrations, about 13.05% of actual registrations. Within appointment registrations, Web booking accounted for only 3.43%, while telephone and window booking were much larger shares.

Institutional source:
- https://wjw.beijing.gov.cn/xwzx_20031/wnxw/201912/t20191214_1175570.html

This is not primarily a Web-interface source, but it constrains archaeological interpretation.

A surviving 2009 booking page proves `exists` and perhaps `available`; it does not justify:

> “By 2009 Beijing hospital booking was mainly online.”

The adoption ladder remains:

```text
feature exists
→ user can reach feature
→ user can satisfy account/identity requirements
→ user actually uses it
→ booking succeeds
→ offline closure succeeds
→ feature becomes routine for a substantial population
```

---

# 6. 2011–2012 railway Web ticketing: the transaction becomes distributed across page, identity, payment and pickup

A January 2012 Xinhua Q&A republished by China News stated that 12306 began Internet ticket sales for Beijing–Tianjin intercity trains on **2011-06-12**, then expanded to additional train categories during 2011. By the 2012 Spring Festival season, Internet and telephone ticketing had expanded across the railway system.

Source / B contemporaneous explanatory report:
- https://www.chinanews.com.cn/cj/2012/01-13/3603064_2.shtml

A second contemporaneous report from **2012-01-12** preserves ordinary-user failures across channels:
- https://news.cntv.cn/20120112/102751.shtml

It records:

- a user repeatedly refreshing 12306 after “提交订单用户过多” messages until tickets sold out;
- another passenger recruiting seven relatives/colleagues to telephone-book in parallel;
- a passenger calling the booking number 27 times before succeeding;
- queues at telephone-booking ticket pickup windows.

### Archaeological consequence

A Web archive that preserves only the public booking interface misses the actual multi-channel state topology:

```text
Web query / refresh
↘
 telephone call attempts
  ↘
   station / agent counter
    → shared railway inventory
     → reservation / order
      → pickup / identity check
       → entry / travel
```

A historical person's route can cross channels mid-transaction.

Therefore do not infer a single access route from one surviving page.

---

# 7. 2012: the queue becomes an explicit backend object

In September 2012, contemporaneous reports described a new 12306 queue mechanism. Users completing the booking flow could receive messages that their submitted orders would be processed after a wait of 30 minutes or more, without a guarantee of ticket issuance.

Sources / B contemporaneous reports:
- https://www.chinanews.com/cj/2012/09-20/4198992.shtml
- https://news.sina.com.cn/o/2012-09-19/125925207377.shtml
- https://tech.sina.com.cn/i/2012-09-18/00227626106.shtml

One report described a user waiting 30 minutes only to receive an order-processing failure; another reporter recorded approximately 100 minutes of waiting before receiving a different seating outcome.

### New archaeological object: backend queue state

The visible old-Web page now contains a representation of a **server-side temporal process**.

That means a screenshot of:

```text
排队等待中
预计等待 30 分钟以上
```

is not merely “page content.”

It is a time-sensitive projection of a backend state.

### New gap: capture freezes a moving queue

If an archive captures such a page, it can misleadingly turn a transient estimate into a permanent document.

The capture proves only:

> at capture time, this rendered representation said the order was waiting.

It does not prove:

- queue position;
- final result;
- true wait duration;
- whether estimate changed;
- whether inventory remained;
- whether user stayed logged in;
- whether order was later canceled or failed.

---

# 8. 2013: the public site begins performing part of the user's waiting work

A contemporaneous 2013 report on the redesigned 12306 site described:

- automatic query;
- automatic order submission;
- ticket-availability sound notification;
- alternative dates;
- preferred trains;
- preferred seat classes.

Source / B contemporaneous report:
- https://politics.people.com.cn/n/2013/1206/c1001-23761164.html

This matters for old-Web archaeology because the interface is no longer just a static query form.

It can act as a small **user-side waiting agent**.

The state machine becomes:

```text
user stores preferences
→ page/client repeatedly queries
→ inventory appears
→ client may alert / auto-submit
→ server transaction path begins
```

### Browser-runtime consequence

A static HTML capture may preserve form labels while losing:

- JavaScript timers;
- repeated-query behavior;
- sound notification assets;
- event handlers;
- session-dependent passenger data;
- CAPTCHA state;
- backend responses.

Therefore:

> **UI text survival ≠ interactive waiting behavior survival.**

This is exactly the kind of case where modern browser replay cannot be treated as a historical interaction reconstruction without explicit evidence.

---

# 9. 2014–2015: identity state becomes more explicit and more version-sensitive

A February 2014 report on 12306's identity verification changes stated that from March 1 the site would expose different verification states such as `已通过`, `待核验`, `未通过` (with other document types having additional states).

Source / B contemporaneous report:
- https://www.chinanews.com/sh/2014/02-24/5873751.shtml

This creates a new old-Web distinction:

```text
passenger entry exists in account
≠ identity verified for online purchase
≠ order permitted
```

A profile-like passenger row can survive in a screenshot while its transactional eligibility is unknown.

### Version risk

Do not back-project 2014 identity-status labels into 2011–2013 screenshots or later rules backward into earlier years.

Booking systems are highly versioned policy interfaces.

---

# 10. Cross-channel state model

For evidence extraction, record each historical artifact against this matrix where possible:

| State family | Example observable evidence | What it does NOT prove |
|---|---|---|
| Public information | help page / booking rule | service actually reachable |
| Discovery | doctor/train listed | inventory available now |
| Account | login form | user had valid account |
| Identity | verification label | person who operated account |
| Availability | “有票” / slot shown | item held for user |
| Submit | button pressed / loading page | backend accepted request |
| Queue | waiting estimate | exact position / final success |
| Order | order number / unpaid order | payment success |
| Payment | gateway success | platform reconciled payment |
| Confirmation | success page / SMS rule | offline pickup/check-in |
| Pickup | ticket/number collection rule | user actually collected |
| Offline fulfillment | boarding / clinic visit | normally not public-Web-visible |
| Cancellation | cancel rule | actual inventory re-release timing |

The farther right the transaction moves, the less likely ordinary public Web archives are to preserve it.

---

# 11. Platform disappearance and historical visibility

Appointment/ticket systems create a characteristic preservation bias.

## Usually easier to preserve

- public help pages;
- announcement articles;
- screenshots in news reports;
- booking instructions;
- release-time rules;
- public login shells;
- error-message screenshots.

## Usually harder or inappropriate to preserve

- authenticated order history;
- identity-binding database state;
- payment callbacks;
- queue internals;
- private SMS confirmations;
- medical appointment records;
- exact passenger itinerary histories;
- server-side inventory transitions.

Therefore the public historical record systematically over-represents **rules and failure screens**, while under-preserving successful private closure.

This is not evidence that failure was more common than success.

---

# 12. Evidence grading for appointment / ticket artifacts

## A — primary / contemporaneous

Examples:

- verified archived official booking/help page;
- historical official manual;
- contemporaneous service announcement;
- original screenshot with date/provenance;
- official technical document.

Even A evidence normally proves only the state it directly exposes.

## B — near-contemporaneous secondary

Examples:

- reporter records own booking attempt;
- user process described in contemporaneous newspaper;
- technical press captures queue/error screenshots;
- official statements quoted in news.

Useful for dynamic behavior that public archives often miss.

## C — retrospective memory

Examples:

- “I remember refreshing 12306 all night in 2012.”

Good for lived experience; insufficient alone for exact UI, dates or server behavior.

## D — reconstruction

Examples:

- rebuilding a 2012 queue page from screenshots;
- simulating old JavaScript behavior;
- inferring backend queue architecture from UI messages.

Must be marked reconstruction and separated from historical originals.

---

# 13. Anti-hindsight rules

1. Do not use today's 12306 App to reconstruct the 2012 Web transaction.
2. Do not assume today's unified identity/payment rules existed in 2011.
3. Do not interpret a preserved slot list as proof of successful booking.
4. Do not interpret a success page as proof of hospital attendance or railway travel.
5. Do not infer server architecture from a client message such as “排队中”.
6. Do not assume telephone, Web and counter shared identical inventory or deadlines without evidence.
7. Do not treat the existence of online booking as population-wide adoption.
8. Do not deanonymize historical users to “complete” a transaction chain.
9. Do not republish private medical/travel/order data simply because an archive accidentally exposes it.
10. Do not treat missing authenticated pages as a failed study; private-state missingness is itself part of the evidence model.

---

# 14. Negative result for this run

This research pass verified strong contemporaneous public evidence for:

- Beijing hospital online-booking rules in 2009;
- multi-channel coexistence;
- 2011–2012 railway Internet/telephone expansion;
- ordinary user refresh/redial/pickup experiences;
- explicit 12306 backend queue messages in 2012;
- 2013 automatic query/submission UI functions;
- 2014 identity-verification states.

But it did **not** obtain and validate a privacy-safe, authenticated historical session that follows one user all the way through:

```text
login
→ availability query
→ request
→ backend queue
→ order creation
→ payment callback
→ confirmation
→ pickup/check-in
```

Therefore this note does not invent:

- exact historical DOM across the full transaction;
- cookies / session schema;
- queue implementation;
- payment callback protocol;
- database table structure;
- exact charset/browser support for authenticated pages;
- a real person's end-to-end transaction history.

This is a meaningful archive gap, not a reason to fill the missing states with modern assumptions.

---

# 15. Why this changes Chinese old-Web interpretation

Old-Web archaeology often asks:

> What did the page look like?

Booking systems force a harder question:

> **What was the page a window into, and how much of the real transaction lived somewhere else?**

For scarce appointments and tickets, the historically decisive state often sits behind the page:

- inventory;
- queue position;
- identity eligibility;
- order hold;
- payment reconciliation;
- pickup deadline;
- offline arrival.

A page can survive beautifully while the process that gave the page practical meaning is completely gone.

So the defensible conclusion is:

> **The Chinese old Web increasingly became an interface to real-world state, but the more consequential that state became, the more likely it was to be authenticated, dynamic, private and poorly archived.**