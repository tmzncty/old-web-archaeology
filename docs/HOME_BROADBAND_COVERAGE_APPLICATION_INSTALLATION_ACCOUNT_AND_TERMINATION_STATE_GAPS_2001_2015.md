# HOME_BROADBAND_COVERAGE_APPLICATION_INSTALLATION_ACCOUNT_AND_TERMINATION_STATE_GAPS_2001_2015

Status: research note / state-gap model  
Scope: approximately 2001–2015 Chinese public Web interfaces, telecom support/business-hall pages and contemporaneous technical/service reporting related to residential ADSL / community broadband / FTTH  
Companion life-history note: `tmzncty/how-people-lived/topics/home-broadband-address-bound-connectivity-installation-and-household-network-readiness-china-1999-2026.zh-CN.md`

## 0. Why this belongs in old-web archaeology

A historical ISP page can look deceptively conclusive.

It may say:

- “本市已开通 ADSL”；
- “小区已覆盖”；
- “网上申请”；
- “48 小时装机”；
- “百兆提速”；
- “点亮光小区”；
- “暂停/恢复宽带”；
- “网上营业厅”。

None of these statements, by itself, proves that a particular household had a working Internet connection.

Residential broadband is a useful old-Web case because the public Web exposes only the outer shell of a much longer operational chain. The states that matter most to ordinary users — port availability, work-order status, authentication, line sync, modem/ONT assignment, actual packet reachability, billing and later cancellation — are usually private, dynamic and poorly archived.

The core warning is therefore:

> **public service page survival ≠ subscriber service-state survival.**

This note does **not** attempt to reconstruct subscriber accounts or revive historical credentials. It models what can and cannot be inferred from public evidence.

---

# 1. Research unit and evidence contract

Per `docs/METHOD.md`, do not collapse these objects:

- telecom operator / ISP brand;
- city or regional service;
- exchange / DSLAM / PON area;
- residential compound / building;
- one physical address;
- public product page;
- public coverage/demand page;
- authenticated online business hall;
- subscriber account;
- installation/work order;
- modem / DSL line / ONT;
- PPPoE or other authentication state;
- billing record;
- one browser capture;
- researcher claim.

A 2013 public page saying “100M available in major cities” is a claim about a product/service layer.

It is **not** evidence that:

- every building in those cities had fiber;
- an apartment had an available port;
- a user had ordered it;
- the technician had visited;
- the ONT had registered successfully;
- the user’s PC/router had authenticated;
- the service actually reached websites;
- the user received contracted speed.

---

# 2. Master state machine

A residential fixed-broadband route should be modeled at least as:

```text
[PUBLIC MARKET STATE]
product announced
→ city/region served
→ plan/tariff published

[ADDRESS INFRASTRUCTURE STATE]
exchange/OLT/DSLAM capability exists
→ neighborhood/building covered
→ drop/line route physically possible
→ port/line resource currently available

[APPLICATION STATE]
user discovers channel
→ application submitted
→ identity/address accepted
→ plan selected
→ application accepted
→ work order created

[FULFILLMENT STATE]
appointment scheduled
→ technician dispatched
→ technician arrives
→ in-building / in-home work completed
→ modem/ONT/CPE assigned

[NETWORK STATE]
account provisioned
→ physical line sync / optical link succeeds
→ authentication succeeds
→ IP/DNS/routing available
→ target Internet services reachable

[HOUSEHOLD STATE]
router/LAN/Wi-Fi configured
→ household device connects
→ task/application works

[BILLING / LIFECYCLE STATE]
billing active
→ plan changed / suspend / resume / move
→ cancellation requested
→ outstanding fees settled
→ loaned equipment returned if required
→ account/service administratively closed
```

Each arrow is a possible historical evidence gap.

---

# 3. Gap taxonomy

## 3.1 market-availability gap

`product page exists ≠ ordinary subscriber can buy it at this address`

A national or city-level broadband announcement proves a marketed service existed.

It does not prove local infrastructure or available capacity.

## 3.2 coverage-address gap

`city/neighborhood covered ≠ specific building/apartment serviceable`

Coverage can be defined at very different granularities.

A historical page may say “XX 小区已覆盖” while:

- some buildings are not wired;
- one entrance is excluded;
- property access is unresolved;
- internal building cabling is incomplete.

Unless the historical evidence names the exact serviceable unit and the meaning of “coverage”, keep the claim narrow.

## 3.3 port/line-resource gap

`physical network nearby ≠ spare port/line exists now`

This gap is strongly evidenced by 2008 contemporaneous reporting.

A Guangzhou applicant submitted 2M broadband requests to two operators and both were rejected because local ADSL access ports were full; expansion timing was unknown. Another operator eventually pulled a line from farther away.

Source / B contemporaneous:
- https://www.c114.com.cn/market/183/a328684.html

A Beijing suburban resident similarly reported repeated inability to obtain fixed telephone/broadband because local line resources and ports were occupied.

Source / B contemporaneous:
- https://www.chinanews.com.cn/it/txxw/news/2008/12-29/1506181.shtml

Therefore:

> a saved tariff page or coverage map cannot be used as proof of installability.

## 3.4 application/order gap

`online form submitted ≠ operator work order exists`

A public Web form may successfully render and accept fields while backend processing fails, is rejected, or requires telephone/branch confirmation.

Unless there is authenticated/order evidence, claim only that an application channel existed.

## 3.5 appointment/visit gap

`appointment scheduled ≠ technician arrived`

Weather, customer absence, property access, capacity, workload or rescheduling can interrupt the route.

A historical appointment page is not proof of physical installation.

## 3.6 CPE ownership/loan gap

`device in the home ≠ device owned by subscriber`

Modem/ONT/set-top equipment may be:

- purchased;
- rented;
- loaned without a clearly remembered deposit;
- bundled in a plan;
- property of the operator pending return.

This distinction becomes especially visible at termination.

## 3.7 account-provisioning / auth gap

`wire installed ≠ subscriber account can authenticate`

Possible states include:

- account not provisioned;
- wrong username/password;
- account bound to line/device;
- authentication backend unavailable;
- account suspended;
- plan not yet activated.

Most of these states live behind private systems and are unlikely to be captured by Web archives.

## 3.8 line-sync gap

`account valid ≠ DSL/optical physical link up`

ADSL requires physical line conditions and DSL sync; FTTH requires optical link/ONT registration.

Public product pages rarely preserve the subscriber’s actual line state.

## 3.9 end-to-end reachability gap

`line/auth succeeds ≠ Internet use succeeds`

DNS, routing, upstream outage, local firewall, ISP filtering, application server failure or malware can all break actual use.

A support page describing “ADSL 正常” troubleshooting is not evidence that a particular historical session worked.

## 3.10 contracted-speed / access-speed / application-performance gap

These must not be collapsed:

```text
advertised plan rate
≠ access-line synchronization rate
≠ operator speed-test result
≠ LAN/Wi-Fi throughput
≠ application download/upload performance
```

By the FTTH era, a surviving “100M” product page says very little about a user’s bedroom Wi-Fi or a particular website’s speed.

## 3.11 local-network/Wi-Fi gap

`Internet reaches ONT/modem ≠ all household devices can use it`

The public ISP Web often stops at the CPE boundary.

But ordinary life can fail because of:

- router configuration;
- weak Wi-Fi coverage;
- old network cards;
- local cabling;
- multiple-device contention;
- user configuration errors.

The archive therefore tends to preserve the operator boundary better than the household experience boundary.

## 3.12 move/reinstall gap

`subscriber remains same person ≠ fixed connection moves with them`

Moving house may require:

- checking new-address coverage;
- submitting a move request;
- new construction/appointment;
- returning/replacing CPE;
- changing plan or operator.

Digital identity is portable; residential line state is not.

## 3.13 termination/settlement/equipment-return gap

`user stopped using service ≠ service administratively closed`

A complete closure route can involve:

```text
cancel request
→ identity verification
→ fee settlement
→ equipment return
→ backend closure
→ removal of restrictions / account state clean
```

A 2023 Beijing Youth Daily investigation, outside this repo’s primary 1995–2015 scope but relevant as a lifecycle boundary, documented users who discovered at cancellation that optical modems had to be returned; one renter who left the device with a landlord later reported being unable to process operator services after returning from abroad.

Source / B later boundary evidence:
- https://www.chinanews.com.cn/sh/2023/07-29/10051771.shtml

This later evidence should **not** be projected backward to say every 2000s modem followed the same ownership rules. It simply demonstrates why CPE ownership and closure are separate states that a historical case must check.

---

# 4. 2001 ADSL: public tariff pages can prove a product, price and claimed access mode — not household adoption

A 2001-09-17 *People’s Daily* market report provides useful contemporaneous evidence for Beijing ADSL:

- Beijing Telecom promoted ADSL prominently;
- tariff examples included a high initial account/opening cost and time-banded plans;
- some community Ethernet alternatives were cheaper;
- staff at several offices reportedly saw few ADSL applicants;
- the technical explainer described ADSL as capable of simultaneous telephone/data use and not requiring traditional dial-up for each session.

Source / B contemporaneous national newspaper archive:
- https://cn.govopendata.com/renminribao/2001/9/17/12/

### What this evidence supports

- ADSL was a publicly marketed residential access product in Beijing by that date.
- Specific tariffs were publicly described.
- “no need to dial each visit / persistent availability” was part of the technical proposition.
- uptake at the inspected offices could be low despite product existence.

### What it does not support

- citywide building coverage;
- port availability at any address;
- actual subscriber count beyond claims in the report;
- individual line performance;
- browser/PPPoE client details;
- whether an applicant’s installation was completed.

### Browser/environment caution

If an actual 2001 operator application page is later recovered, do not assume modern Chromium replay equals historical usability.

Potential dependencies to inspect rather than guess:

- IE-specific JS;
- GB2312/GBK encoding;
- client-side validation;
- frames/table layout;
- HTTP/HTTPS support;
- downloadable dialer/PPPoE software;
- ActiveX controls.

No such dependency is asserted here without a verified capture.

---

# 5. 2005–2007: the Web starts managing the account, but private subscriber state remains hidden

## 5.1 Time-limited broadband shows that “broadband” did not immediately mean unlimited always-on use

Contemporaneous Beijing reporting in 2005–2007 documents ADSL plans with monthly included hours and per-minute excess charges.

Sources / B:
- https://finance.sina.com.cn/roll/20050802/0637243551.shtml
- https://news.sina.cn/sa/2006-08-05/detail-ikknscsk0715138.d.html
- https://news.sina.com.cn/o/2007-01-05/142810932345s.shtml

This matters for page archaeology because tariff UI may encode a real behavioral constraint.

A historical plan selector with “20 小时 / 50 小时 / 不限时” is not decorative metadata: it defines different user-time regimes.

## 5.2 2006 online self-service proves Web-mediated plan/account operations existed

Beijing Netcom contemporaneous service reporting says users could handle multiple ADSL changes and introduced online self-service for changing usage-duration plans.

Source / B:
- https://tech.sina.com.cn/t/2006-05-17/1755942442.shtml

A separate 2006 report describes a `bbn.com.cn` “宽带管家” route for enabling an ADSL online payment-related function.

Source / B:
- https://finance.sina.com.cn/roll/20060927/0519948749.shtml

### Narrow claim

By 2006, parts of Beijing ADSL subscriber administration could be initiated through public/authenticated Web interfaces.

### Do not infer

- that every service change was end-to-end online;
- that the archived public shell preserved authenticated account state;
- that a click immediately changed billing/provisioning;
- that all browsers or encodings worked identically.

### New state gap: request-versus-provisioning gap

For telecom administration:

```text
user requests plan change
≠ backend billing plan changed
≠ network provisioning changed
≠ next bill reflects change
```

An authenticated screenshot of “申请成功” would still require later evidence to prove downstream completion.

---

# 6. 2008: port-full cases are direct evidence against reading operator Web as infrastructure truth

The 2008 Guangdong and Beijing cases should be treated as high-value counterexamples because they expose states usually absent from public Web archives.

## Guangdong

A business user submitted broadband requests to two operators; both rejected them because local ADSL access ports were full.

Source:
- https://www.c114.com.cn/market/183/a328684.html

## Beijing suburbs

A resident reported repeated applications over years but no fixed line/broadband because local resources and ports were occupied.

Source:
- https://www.chinanews.com.cn/it/txxw/news/2008/12-29/1506181.shtml

### Archaeological implication

Suppose a Wayback capture survives for the local operator in July 2008 and says:

> “2M ADSL，欢迎办理。”

The strongest defensible claim is:

> the operator publicly marketed that plan in the relevant period.

It is **not**:

> the applicant could have bought it at that address.

This distinction should be reused in all old-Web research on physical services:

- delivery;
- utilities;
- broadband;
- housing;
- transport;
- local medical appointments.

A Web interface can represent a service whose physical execution is capacity-constrained elsewhere.

---

# 7. 2012 FTTH: work-order timing exposes a multi-system backend

A 2012 China Economic Net report on Shanghai Telecom’s FTTH acceleration is unusually valuable because it names operational stages:

- acceptance/entry at the business hall;
- work order generated within 4 hours;
- on-site installation and activation within 48 hours in covered areas;
- average installation time about 1.72 days in pilot areas.

Source / B contemporaneous:
- https://district.ce.cn/zg/201208/28/t20120828_1298843.shtml

Another contemporaneous report states the 48-hour commitment applied to residences in optical-network-covered areas and allowed application through business halls or `10000` telephone service.

Source / B:
- https://news.cntv.cn/20120517/101405.shtml

### Why this matters to Web archaeology

A public page or form may show only:

```text
“申请光网”
```

but the operator’s actual transaction spans at least:

```text
public channel
→ CRM acceptance
→ address/resource lookup
→ dispatch/work-order system
→ technician mobile/field workflow
→ physical installation
→ network provisioning
→ billing activation
```

The public Web is only one UI into a larger sociotechnical system.

### New rule

When reconstructing a historical Web service that triggers physical work, include a **backend/field-work boundary** explicitly.

Do not imply that preserving the Web form preserves the service process.

---

# 8. 2013 “点亮光小区”: demand registration is not coverage or fulfillment

Contemporaneous 2013 reporting on China Telecom’s third broadband acceleration says:

- existing optical-broadband users could use `10000`, the online business hall or a physical business hall to handle upgrade service;
- users without installed optical broadband could visit `dlgxq.189.cn` for the “点亮光小区” activity.

Source / B contemporaneous:
- https://www.c114.com.cn/news/117/a786151.html

This gives a particularly important state distinction:

```text
user expresses demand online
→ operator aggregates demand
→ operator decides/arranges build
→ building becomes covered
→ address becomes serviceable
→ user applies
→ installation completes
```

A historical `dlgxq.189.cn` capture, if found, would therefore prove only the interface and its claims unless downstream records are available.

### demand-registration gap

`“点亮” click / registration ≠ construction promise ≠ completed fiber build`

This is a strong warning against language such as:

> “用户点击后小区就会开通光纤。”

The evidence supports a demand-collection route, not guaranteed infrastructure delivery.

---

# 9. Archival asymmetry: the more consequential the state, the less likely public Web preserves it

A broad pattern emerges:

| State | Public archive survivability | Importance to actual household |
|---|---:|---:|
| product announcement | high | medium |
| tariff page | high | high |
| FAQ / install instructions | medium-high | medium-high |
| coverage lookup shell | medium | high |
| authenticated application | low | high |
| port availability response | very low | decisive |
| work-order status | very low | decisive |
| subscriber credentials | should not be public | decisive |
| DSL/optical line state | very low | decisive |
| billing ledger | private | decisive |
| termination/equipment-return status | private | decisive |

This means the old Web systematically overrepresents **what operators advertised** and underrepresents **whether individual households successfully received service**.

That is not simply a Wayback failure.

Much of the missing state was never public HTTP content in the first place.

---

# 10. Historical browser / protocol questions to preserve for future verified captures

For a verified 2001–2015 ISP page, record rather than assume:

## Document layer

- charset (`GB2312`, `GBK`, UTF-8, Big5 if relevant);
- table/frameset layout;
- client-side validation;
- image maps;
- iframe dependencies;
- external JS/CSS survival.

## Browser layer

- IE-specific APIs;
- ActiveX controls;
- Java applets;
- Flash;
- TLS/certificate compatibility;
- cookies/session requirements;
- pop-up flows.

## Account layer

- whether login UI itself survives;
- whether it was tied to phone number/broadband account/ID;
- whether CAPTCHA or SMS existed;
- whether authentication endpoint is archived (usually it should not be usable).

## Network/service layer

- PPPoE client/software references;
- modem configuration guides;
- DNS settings;
- line indicators / error-code manuals;
- downloadable firmware or drivers.

### Important safety boundary

Do not attempt to authenticate into historical accounts, reuse leaked credentials, or reconstruct personal subscriber identifiers.

The research target is interface/state structure, not individual access.

---

# 11. Evidence grades and what each source family can prove

## A — original / institutional

Candidate evidence families to prioritize in future capture work:

- archived ISP official tariff pages;
- official online-business-hall help pages;
- official installation manuals;
- official CPE manuals;
- original software/dialer packages where redistribution permits;
- CNNIC/MIIT statistics for adoption/capacity context.

A product page proves an operator claim at a date; it does not prove fulfillment.

## B — near-contemporaneous secondary

Used in this note:

- 2001 *People’s Daily* broadband-market reporting:
  https://cn.govopendata.com/renminribao/2001/9/17/12/
- 2006 Beijing Netcom service-change reporting:
  https://tech.sina.com.cn/t/2006-05-17/1755942442.shtml
- 2008 port-full cases:
  https://www.c114.com.cn/market/183/a328684.html
  https://www.chinanews.com.cn/it/txxw/news/2008/12-29/1506181.shtml
- 2012 Shanghai FTTH work-order timing:
  https://district.ce.cn/zg/201208/28/t20120828_1298843.shtml
- 2013 `点亮光小区` / online business-hall route:
  https://www.c114.com.cn/news/117/a786151.html

These can recover operation claims, URLs, process steps and user failure states that are not otherwise visible.

## C — later recollection

Later “我家第一条 ADSL”“当年拨号声”“第一次装光纤” recollections can be useful for lived experience but should not set exact tariff dates, DOM structure or coverage without contemporaneous confirmation.

## D — reconstruction

Any recreated 2000s ISP page, old IE screenshot, dialer interface or FTTH application flow must be labeled `reconstruction` and list:

- historical originals;
- missing assets;
- substituted assets;
- modern tooling;
- assumptions;
- unresolved differences.

Generated or recreated UI must never be presented as the original historical page.

---

# 12. Confirmed / probable / unknown

## Confirmed

- Beijing residential ADSL was publicly marketed with explicit tariff structures by 2001.
- Time-limited ADSL plans remained common enough to appear in 2005–2007 contemporaneous reporting.
- By 2006, some Beijing broadband account/service operations had online self-service routes.
- In 2008, applicants could fail to obtain broadband because specific local ports/lines were exhausted despite operators selling broadband generally.
- By 2012, Shanghai FTTH provisioning exposed distinct acceptance, work-order and field-installation stages.
- By 2013, public Web demand registration (`点亮光小区`) and online-business-hall channels were part of broadband upgrade/coverage workflows.

## Probable but not promoted to stronger claims here

- Many 2000s online-business-hall pages were optimized around period IE/JS environments and may replay incorrectly today.
- Subscriber provisioning involved separate CRM/billing/network-management systems that public pages did not expose fully.
- Household Wi-Fi increasingly became a major user-experience bottleneck in the fiber era.

These are technically plausible and often documented elsewhere, but each historical case still needs object/date-specific evidence.

## Unknown / negative result in this cycle

This cycle did **not** obtain and verify a privacy-safe authenticated historical subscriber capture that preserves, end to end:

```text
address/resource check
→ application
→ accepted order ID
→ field work order
→ modem/ONT assignment
→ account provisioning
→ line sync/authentication
→ first successful Internet session
→ billing
→ later move/cancellation
```

Accordingly this note does **not** guess:

- historical login field names;
- exact subscriber dashboard DOM;
- exact charset of unverified business-hall pages;
- exact CAPTCHA/SMS behavior;
- PPPoE error codes for one operator/date without source;
- private account status;
- a particular household’s final service outcome.

The absence of such a capture is itself expected: the decisive states are private operational records.

---

# 13. Privacy and copyright boundary

Do not collect or republish:

- real historical broadband usernames/passwords;
- ID-card numbers;
- full residential addresses tied to ordinary individuals;
- phone numbers used as account identifiers;
- private bills/work-order IDs;
- leaked ISP subscriber databases;
- modem serials/ONT credentials tied to identified persons.

When a contemporaneous newspaper names a user, preserve only the minimum detail needed for the claim; do not attempt to rediscover their current identity or address.

For archived ISP assets, prefer:

- URLs;
- capture metadata;
- screenshots only where copyright/archival policy permits;
- short quoted labels;
- researcher-generated state diagrams;

rather than mirroring entire copyrighted sites or software packages.

---

# 14. What this changes in the old-Web model

Older Web histories often reconstruct visible content layers:

```text
portal page
→ links
→ forum
→ personal page
```

Residential broadband adds a different kind of object:

> **a Web page that is an interface into physical infrastructure.**

The page’s meaning depends on things that are not Web documents:

- copper/fiber in the street;
- available DSLAM/PON ports;
- building access;
- technician schedules;
- a physical modem/ONT;
- account provisioning;
- billing databases;
- later equipment return.

Therefore the archaeology of Chinese broadband Web should preserve both:

1. **page morphology** — what did the 2001/2006/2013 user see?;
2. **service-state humility** — what can that page not tell us about whether the household actually got online?

This is directly reusable for other old-Web transactional interfaces.

---

# 15. Next evidence package

Highest-value next work is **not** another generic telecom chronology.

Look for one privacy-safe, legally accessible historical case with at least three adjacent layers, for example:

```text
A. archived official 2006–2013 broadband service page
B. contemporaneous user/help report describing the same operation
C. original modem/ONT/manual or operator installation guide
```

Ideal subcases:

- 2006 Beijing Netcom ADSL online self-service;
- a verified 2012 Shanghai FTTH application/installation capture;
- a verified 2013 `dlgxq.189.cn` “点亮光小区” capture;
- period screenshots/manuals of address coverage lookup and install-status pages.

For each verified capture, record:

```text
original_url
archive_source
capture_url
capture_datetime
HTTP/replay state
charset
browser assumptions
subresource survival
public/authenticated boundary
claim supported
claim NOT supported
```

The target conclusion is not “we found the old broadband website.”

It is:

> **we can now say exactly which part of a household’s path from wanting Internet to having working Internet the surviving page represents — and which parts have disappeared.**
