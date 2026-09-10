# ATM / bank-locator / online-banking limit / cash-dispense / settlement state gaps, 1995–2015

## Scope

This is a **Chinese old-Web / banking-interface archaeology note**, not a general history of money, banks, ATMs, UnionPay or mobile payments.

Main period: **1995–2015 Chinese Internet**.

Pre-1995 bank-network and ATM history appears only where necessary to explain why a public Web page is not the authority for a cash transaction. Post-2015 mobile-payment decline of ATM use appears only as boundary context.

The central archival problem is:

> A historical bank Web page can prove that an ATM locator, daily-withdrawal-limit control, branch query or self-service instruction existed. It cannot by itself prove that a specific ATM was physically present, online, stocked with cash, connected to the relevant card network, or that a specific withdrawal actually dispensed money and settled correctly.

This subject is therefore a strong example of why **Internet history is not identical to Web-page history**. The financially authoritative system often lived behind private bank networks decades before ordinary consumers saw a Web interface.

---

## 1. Boundary context: public Web arrived after networked cash withdrawal

Main life-history package:

- `tmzncty/how-people-lived/topics/atm-cash-access-interbank-networks-and-payment-fallback-sovereignty-china-1987-2026.zh-CN.md`

Relevant boundary facts:

- later institutional/media histories place an early mainland Chinese ATM installation at Bank of China Zhuhai in 1987;
- Shanghai began a “Gold Card Project” in 1993 and operated an ATM/POS interconnection system from 1995;
- China UnionPay was established on 2002-03-26 to operate national interbank card switching/interoperability.

Sources:

- Shanghai Municipal Government, banking-card industry plan preserving 1993/1995/2002 milestones:
  https://www.shanghai.gov.cn/nw6933/20200906/0001-6933_534.html
- 2003 contemporaneous UnionPay profile, reproduced by Sina:
  https://finance.sina.cn/sa/2003-04-14/detail-ikknscsi0750501.d.html

These facts must not be converted into a false Web-centric history. ATM transactions can be digital network transactions without HTTP, browsers, public DNS or user-facing Web pages.

---

## 2. Object separation

Do not use “ATM”, “bank website” or “online banking” as if each were one recoverable object.

At minimum distinguish:

1. **bank account** — authoritative ledger relationship;
2. **available balance** — amount potentially usable at a given time;
3. **card account / card number**;
4. **physical card**;
5. **PIN / authentication factor**;
6. **issuing bank**;
7. **acquiring ATM operator**;
8. **interbank switch / card network**;
9. **ATM physical cabinet**;
10. **ATM location record**;
11. **ATM terminal ID**;
12. **terminal software/configuration**;
13. **telecommunications link**;
14. **ATM service state** — powered, online, maintenance, out-of-service;
15. **cash cassette inventory**;
16. **denomination inventory**;
17. **withdrawal request**;
18. **authorization request**;
19. **authorization response**;
20. **dispense command**;
21. **physical note movement**;
22. **customer cash-taking event**;
23. **journal / ATM electronic log**;
24. **issuer ledger posting**;
25. **interbank clearing/settlement**;
26. **reversal / correction**;
27. **printed receipt**;
28. **public bank Web site**;
29. **branch/ATM locator page**;
30. **locator database record**;
31. **online-banking account session**;
32. **ATM/POS limit-setting Web form**;
33. **limit/configuration state stored in backend**;
34. **mobile-Web bank interface**;
35. **customer-service hotline**;
36. **complaint/fraud case**;
37. **historical Web capture**.

Evidence for one object cannot silently prove another.

---

## 3. Generic cash-withdrawal state machine

```text
customer has an account with available funds
-> customer has usable card/authentication material
-> customer locates an ATM
-> ATM is physically present
-> ATM is powered and operational
-> ATM is connected to acquirer/switch
-> card is read
-> PIN/authentication accepted
-> withdrawal amount requested
-> terminal/network sends authorization
-> issuer/account backend authorizes
-> ATM receives authorization
-> ATM verifies/assumes local dispense ability
-> cash cassette feeds notes
-> notes reach presentation slot
-> customer physically takes notes
-> terminal journals dispense outcome
-> issuer/acquirer records converge
-> interbank clearing/settlement completes
-> reversal/correction occurs if required
```

Every arrow is a possible state gap.

---

## 4. Core state gaps

### 4.1 account-balance / cash-access gap

```text
account balance > 0
!= cash can be obtained here and now
```

Possible blockers:

- no valid card;
- ATM absent;
- terminal offline;
- card/network not accepted;
- PIN/auth failure;
- daily limit exhausted;
- local ATM cash cassette empty;
- insufficient denomination mix;
- cross-bank restriction;
- risk control/fraud block.

Historical writing must not say “he had money” when the evidence only establishes a ledger balance but the research question is physical cash access.

### 4.2 ATM-listing / physical-presence gap

A bank Web page or directory may list a machine after it has been moved, retired, replaced or temporarily unavailable.

```text
ATM record exists
!= machine physically exists at that location now
```

Conversely, a machine can exist without being indexed by a public Web locator.

### 4.3 physical-presence / operational-state gap

```text
machine is in the wall
!= machine powered
!= machine in service
!= communications link healthy
!= host/switch reachable
```

A historical photograph proves cabinet presence, not transaction executability.

### 4.4 operational / cash-stock gap

A terminal can accept cards and display menus while having no usable banknotes for the requested withdrawal.

```text
ATM online
!= cash cassette sufficiently stocked
```

A locator page is especially weak evidence for this state because cash stock is volatile and usually private.

### 4.5 total-cash / denomination gap

Even if the machine contains cash in aggregate, the requested amount may fail because the available cassettes cannot construct it or because a cassette is disabled.

Historical ATM limits therefore have both logical and mechanical layers.

### 4.6 authorization / dispense gap

A successful host authorization does not prove physical notes left the machine.

A 2007 Suzhou case described a customer whose ATM screen showed transaction success while the machine did not present cash.

Source:
https://news.sina.com.cn/c/2007-08-06/120813603687.shtml

Therefore:

```text
authorized
!= dispenser actuated correctly
!= notes presented
!= customer received notes
```

### 4.7 dispense / customer-possession gap

Even physical presentation is not exactly the same event as the user taking the money. Notes may be retracted after timeout; mechanical disputes can exist between terminal logs and human recollection.

Do not infer possession from dispense-journal semantics without knowing the terminal generation and journal definition.

### 4.8 screen-success / ledger-finality gap

A front-end screen may render a successful response while later reconciliation creates a correction, reversal or dispute.

```text
screen message
!= final ledger state
```

The reverse is also possible: user believes a transaction failed while a debit remains until reversal.

### 4.9 issuer-authority / acquirer-observation gap

When a cardholder uses another bank’s ATM, no single visible component necessarily owns the whole truth.

- ATM operator sees terminal events;
- switch sees messages;
- issuer owns account authorization/ledger;
- cardholder sees screen/cash/receipt;
- final clearing may occur later.

A historical source from one party must not be silently upgraded to another party’s authority.

### 4.10 daily-limit / per-transaction-limit gap

2007 Chinese reporting around ATM withdrawal-limit increases recorded cases where daily limit became RMB 20,000 while a machine still allowed only RMB 2,000 per operation, requiring repeated transactions.

Sources:
- https://zjnews.zjol.com.cn/05zjnews/system/2007/05/23/008451248.shtml
- https://www.eeo.com.cn/2007/0523/64780.shtml

Therefore:

```text
daily authorized maximum
!= maximum one dispense
```

### 4.11 limit-setting-page / backend-policy gap

A Web form can expose ATM/POS limit configuration, but the visible page is not itself the enforcement authority.

招商银行的现存 legacy update page records:

- 2009-07-09: Web banking added ATM/POS limit controls;
- 2010-07-28: mobile-Web banking added ATM/POS limit modification.

Source:
https://cmbchina.com/cmbpb/v50/gb/pb/PublicMessageMore.htm

The state model is:

```text
user submits Web setting
-> bank backend accepts change
-> policy record updates
-> later ATM authorization consults effective policy
-> withdrawal allowed/denied
```

The public HTML only proves part of that chain.

### 4.12 UI-setting / effective-time gap

Even when a Web page reports “设置成功”, archival reconstruction still needs to ask whether the backend change was immediate, delayed, channel-specific or subject to other risk controls.

Do not assume synchronous propagation without documentation.

### 4.13 domestic-ATM / overseas-ATM-policy gap

The 2009 CMB legacy record distinguishes domestic daily limits and the ability to close/open overseas UnionPay ATM/POS usage. That means “card usable at ATM” is not a unitary capability; geography can be an explicit backend policy dimension.

### 4.14 cross-bank-available / cross-bank-free gap

Interoperability does not mean zero cost.

A 2007 Zhengzhou user reported using ATMs across banks because it was convenient and later discovering through online transaction details that the cross-bank withdrawal fee had risen to RMB 4 per operation.

Source:
https://news.sohu.com/20071018/n252722252.shtml

So:

```text
interbank withdrawal technically permitted
!= financially frictionless
```

### 4.15 fee-disclosed / fee-noticed gap

A fee can exist in tariff documentation or terminal prompts but still be noticed only after account review.

Archival tariff pages should not be treated as proof that users understood the fee before transacting.

### 4.16 branch/ATM-locator / live-executability gap

A Web locator may provide:

```text
name
address
map/text direction
service type
telephone
```

but the user’s real question may be:

```text
Can I withdraw RMB 2,000 there at 22:40 tonight with this card?
```

Those are fundamentally different claim types.

### 4.17 locator-address / geospatial-position gap

Historical banking locators often used postal addresses, road names or branch names rather than precise modern map coordinates. Even when coordinates exist, a mall, station or office building may have multiple entrances and access-hour constraints.

```text
address record
!= physically reachable machine
```

### 4.18 branch-open / ATM-accessible gap

An ATM may be:

- inside a branch lobby and inaccessible after closing;
- in a 24-hour self-service vestibule;
- on an external wall;
- inside a mall/railway station with separate opening hours.

Do not infer 24/7 access merely from the word ATM.

### 4.19 card-issued / local-acceptance gap

A person owning a bank card does not prove that local machines accept it. This was especially relevant during partial interconnection and urban-rural unevenness.

The “migrant-worker bank card” service is useful precisely because it exposes this gap: the special service joined issuing banks with rural credit cooperative/postal channels so workers could deposit at the work destination and withdraw near home.

Sources:
- https://business.sohu.com/20070912/n252093370.shtml
- https://finance.sina.cn/sa/2008-12-31/detail-ikkntiam3569793.d.html

### 4.20 coverage-statistic / individual-access gap

A province being “covered”, or tens of thousands of rural outlets supporting a service, does not prove that a particular village household had a nearby usable outlet.

Preserve the geographic denominator.

### 4.21 transaction-count / person-count gap

ATM withdrawal counts are not user counts.

```text
one person may withdraw many times
one card/account may serve household routines
one user may use several banks/machines
```

Never translate transaction volume directly into “number of people using ATM”.

### 4.22 bank-card-count / people gap

Similarly, cards per capita are not individual adoption. One person can hold multiple debit/credit cards while another holds none.

### 4.23 Web-session / person gap

Online banking account sessions do not necessarily equal unique humans; family assistance, enterprise delegation and shared machines complicate identity.

### 4.24 ATM-receipt / transaction-authority gap

A printed receipt is excellent evidence that a terminal produced a user-facing artifact, but its semantic authority depends on transaction type. A receipt saying “accepted” or showing a balance should not automatically override later bank reconciliation.

### 4.25 public-Web / private-banking-network gap

This is the major architectural gap.

```text
public Web page
!= ATM transport network
!= issuer host
!= interbank switch
!= clearing ledger
```

Bank Web pages may explain or configure an ATM transaction without carrying the cash-dispense message itself.

---

## 5. A concrete 2008–2011 Web-to-physical-terminal bridge

The still-live CMB legacy update page is particularly useful because it shows Web/mobile interfaces progressively wrapping a pre-existing physical network.

Relevant entries include:

```text
2008-06-12  online interbank transfer in selected branches/regions
2009-07-09  Web ATM/POS daily-limit controls
2010-07-28  mobile-Web ATM/POS limit controls
2010-11-03  iPhone mobile banking
2011-07-08  branch queue-information query
2011-12-10  interbank account query/transfer via “超级网银他行账户”
```

Source:
https://cmbchina.com/cmbpb/v50/gb/pb/PublicMessageMore.htm

Archive classification:

> **surviving official legacy page, not verified historical Memento**.

This distinction is essential. The page currently renders historical dated content, but without a contemporaneous capture it does not prove:

- 2009 DOM structure;
- 2009 HTTP headers;
- 2009 charset behavior;
- then-current CSS/image dependencies;
- actual login endpoint availability;
- certificate/client requirements for every workflow;
- whether linked binaries today are the historical bytes;
- whether every listed feature was globally available at the moment the dated line was added.

What it does strongly show is that by those dates the bank represented Internet/mobile interfaces as control surfaces around account and ATM/POS policy.

---

## 6. Why ATM history is an old-Web preservation problem even though ATMs are not Web pages

### 6.1 locator-page survival / operational-state loss asymmetry

The most archive-friendly object is a static or semi-static ATM locator result.

The most historically important user question is volatile:

> Was this exact machine usable, connected and stocked with the required notes at this exact time?

That state is usually absent from Web archives.

Therefore:

```text
archived locator entry
!= archived service state
```

### 6.2 public-location / private-settlement authority inversion

The public page is easy to archive but weak in transaction authority.

The strongest evidence for a completed withdrawal may exist in:

- bank ledger;
- ATM electronic journal;
- switch logs;
- settlement/reversal records;
- customer complaint files.

Those are private financial records and should generally **not** become public archaeology artifacts.

Thus the most authoritative evidence is also the least appropriate to expose.

### 6.3 machine-presence / cash-stock invisibility

Historical directories can sometimes reconstruct where machines were located. They almost never preserve cash cassette inventory minute by minute.

This makes “ATM density” useful for infrastructure distribution but weak for executable cash access.

### 6.4 screen/receipt survival / backend-state loss asymmetry

A photograph of an ATM screen or a surviving receipt may preserve the user-facing result while the host/switch state that produced it is gone.

The inverse is also possible in institutional archives: aggregate transaction logs survive while the exact UI and physical machine disappear.

### 6.5 successful-mediation invisibility

A person may never visit a bank Web site yet live inside digital banking infrastructure.

Examples:

- uses card at ATM;
- uses another bank’s ATM via interbank network;
- migrant worker deposits wages in city and withdraws near hometown;
- asks bank clerk to change a parameter later consumed by an ATM.

A Web-only history systematically undercounts this kind of digital mediation.

---

## 7. Migration and rural-network evidence: avoid Web-centric and urban-centric inference

2007–2008 “migrant-worker bank card” evidence is important for old-Web archaeology because it shows that infrastructure reach can be extended through **bank switching + physical rural financial outlets**, not necessarily consumer Web access.

2007 contemporaneous description:

```text
worker obtains/deposits into card in work city
-> interbank/card network carries account authority
-> worker returns home
-> nearby rural credit cooperative accepts card/service
-> worker withdraws cash or checks balance
```

Sources:
- https://gxt.hunan.gov.cn/xxgk_71033/gzdt/jxyw/200709/t20070912_2064612.html
- https://finance.sina.com.cn/g/20070108/14093225800.shtml
- https://news.sina.com.cn/c/2008-01-11/113013241603s.shtml

This establishes **digital financial mediation without requiring household Internet adoption**.

Do not infer:

```text
rural card service
=> rural Web banking adoption
```

They are separate infrastructures.

---

## 8. Mobile-payment boundary: why post-2015 evidence changes how we interpret 1995–2015 ATM pages

By 2018, contemporaneous reporting already described many young consumers carrying only a phone, with store revenue dropping sharply when electronic payment failed.

Source:
https://legal.people.com.cn/n1/2018/0608/c42510-30045973.html

By 2022, People’s Daily reported ATM counts had declined from 1.1108 million in 2018 to 947,800 in 2021, while arguing that machines should not simply be removed and should undergo elder-friendly adaptation.

Source:
https://finance.people.com.cn/n1/2022/0905/c1004-32519173.html

These post-scope facts must not be inserted as if they described 2008 behavior. Their archaeological use is narrower:

> they explain why a 2008 ATM-locator page represented a much more central everyday problem than an equivalent locator page might represent to many 2025 users.

Historical interface meaning depends on surrounding life infrastructure, not only HTML.

---

## 9. State gaps for future capture work

When a genuine 1998–2015 Chinese ATM/bank-locator capture is found, record separately:

### Page identity

- original URL;
- archive URL;
- capture datetime;
- HTTP status;
- redirect chain;
- page title;
- declared/detected charset;
- language;
- logged-in or public state.

### Locator semantics

- bank-owned vs third-party locator;
- branch vs ATM categories;
- province/city/district selection;
- address text;
- map dependency;
- keyword search;
- service capability fields;
- “24-hour” claim if present;
- update timestamp if present.

### Technical dependencies

- form method/action;
- server-side endpoint;
- JS files;
- iframe;
- map provider;
- image maps;
- Flash/ActiveX/Java dependency if actually evidenced;
- cookies/session;
- HTTPS/TLS behavior;
- client certificate / proprietary desktop client only where evidenced.

### Transaction boundary

State explicitly whether the captured page can:

```text
only explain ATM service
only locate ATM
change account/ATM limits
show account balance
submit money movement
or merely hand off to another client/system
```

Do not let navigation labels prove backend transaction capability.

---

## 10. Historical-capture status for this slice

This research pass found useful **current surviving legacy bank pages** and multiple contemporaneous reports but did not obtain a historical Chinese ATM-locator / online-banking Memento that was fully verified for:

- original URL;
- capture URL;
- capture datetime;
- HTTP response;
- charset;
- DOM/form structure;
- linked scripts/styles;
- result-page behavior;
- backend handoff.

Therefore the correct status is:

> **M1 verified historical Chinese ATM-locator / online-banking-limit Memento: NOT ACHIEVED IN THIS SLICE.**

This must **not** be rewritten as:

- “Wayback did not preserve Chinese ATM locators”;
- “Chinese banks did not provide ATM locators”; or
- “the old page used IE6/GB2312/ActiveX”.

Those claims require evidence not obtained here.

---

## 11. Counterexamples and failure modes

### Counterexample A: “ATM = 24-hour banking”

False as a universal claim. ATM access can still depend on building opening hours, maintenance, communications and cash stock.

### Counterexample B: “cross-bank network = same experience everywhere”

False. Fees, limits, success rates, geography and card compatibility differ.

### Counterexample C: “Web banking replaced ATM”

False in this period. Web/mobile banking could alter ATM/POS permissions while physical cash still required an ATM or teller.

### Counterexample D: “card ownership = cash portability”

False if the destination lacks accepting terminals/outlets. Migrant-worker service existed because the acceptance network was uneven.

### Counterexample E: “transaction success screen = cash obtained”

False. Contemporaneous failure/fraud cases show a visible success state can diverge from physical outcome.

### Counterexample F: “ATM decline proves cash is obsolete”

False. Later policy explicitly treats cash as a fallback and protects payment choice, particularly for users and situations poorly served by digital-only interfaces.

---

## 12. Hindsight-risk register

1. Do not describe 1980s ATMs with modern browser/app language.
2. Do not infer public Internet from private banking network connectivity.
3. Do not infer mass household adoption from machine installation.
4. Do not infer rural Internet access from rural card withdrawal capability.
5. Do not treat a current legacy page as a contemporaneous capture.
6. Do not infer historical DOM/charset/browser requirements from present rendering.
7. Do not infer real-time ATM status from static locator pages.
8. Do not use transaction volume as person count.
9. Do not use issued-card count as unique user count.
10. Do not treat ATM/POS daily limit as per-transaction physical dispense capability.
11. Do not treat mobile-payment dominance after 2015 as if it already governed 2005 user expectations.
12. Do not expose private financial records merely because they would be stronger transaction evidence.

---

## 13. Evidence grades in this package

### A / strong contemporaneous or institutional

- Shanghai 2002 banking-card industry plan and 1990s interconnection milestones;
- 2003 contemporaneous UnionPay profile;
- 2007 ATM limit/fee/failure reports;
- 2007–2008 migrant-worker card reports and payment statistics;
- CMB surviving official legacy update page with dated 2008–2012 records, with capture caveat.

### B

- later institutional/technical histories used only for boundary context.

### C

- retrospective “first ATM” narratives where no contemporaneous 1987 technical/user document was obtained.

### D / reconstruction

- generic state machine and archival asymmetry concepts in this note; these are analytical reconstruction and must not be mistaken for a single vendor’s documented implementation.

---

## 14. New archival concepts from this slice

### 14.1 `locator-page survival / operational-state loss asymmetry`

Static locations survive; minute-level machine readiness usually does not.

### 14.2 `public-location / private-settlement authority inversion`

The easiest material to archive is the least authoritative for completed transactions. The strongest evidence is often private bank state.

### 14.3 `Web-control / non-Web-execution split`

The Web may configure an ATM limit while the later transaction runs on a separate private terminal/switch network.

### 14.4 `cash-stock invisibility`

Archive can preserve machine existence but not its cash cassette inventory at the user’s moment of need.

### 14.5 `successful-mediation invisibility`

A user can be deeply affected by digital networks without leaving a Web trace at all.

### 14.6 `physical-digital reconciliation gap`

ATM archaeology must model both sides of the transaction:

```text
digital debit/authorization
<->
physical banknotes
```

Any divergence between them is historically meaningful and cannot be collapsed into one “transaction” flag.

---

## 15. What this changes for the repository

ATM history adds an important correction to a Web-centered account of Chinese Internet life:

> **Digital infrastructure entered ordinary financial life not only through screens people consciously called “the Internet,” but through terminals and private networks that converted an invisible database balance into physical money.**

The later Web layer did not replace this immediately. It first made the surrounding state more visible/configurable: locate branches, inspect accounts, alter ATM/POS limits, manage interbank relations. Much of the transaction authority remained elsewhere.

For old-Web archaeology, the key lesson is therefore not “save the bank homepage.” It is:

**separate the page that tells a person where to go, the page that changes a policy, the private network that authorizes money movement, the machine that physically dispenses notes, and the ledger that later decides what finally happened.**
