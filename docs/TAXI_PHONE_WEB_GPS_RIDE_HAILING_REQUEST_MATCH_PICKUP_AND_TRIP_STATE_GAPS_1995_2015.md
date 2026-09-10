# Taxi phone/Web/GPS/ride-hailing request, match, pickup and trip state gaps, 1995–2015

## Scope

This note is a Chinese old-Web / early mobile-Internet archaeology package, not a general history of taxis or a global ride-hailing history.

Main period: **1995–2015 Chinese Internet**.

Pre-1995 taxi/radio/telephone dispatch appears only as boundary context. Post-2015 regulation and mature ride-hailing are out of scope except where needed to explain why an earlier state must not be collapsed.

The central archival problem is simple:

> A historical page can show “叫车成功”, a car icon, a driver name, a fare estimate or a taxi-booking form without proving that a specific passenger physically entered the displayed vehicle.

Therefore this subject needs a state model at least as strict as online ticketing, hotel booking, marketplace settlement and instant-messaging presence.

---

## 1. Object separation

Do not use “taxi website”, “taxi app” or “ride-hailing platform” as if each were one recoverable object.

At minimum distinguish:

1. **regulated taxi / vehicle** — physical licensed vehicle;
2. **driver** — physical person operating a vehicle at a given time;
3. **taxi company / fleet operator**;
4. **dispatch centre** — human/technical organisation receiving requests;
5. **dispatch network** — radio, PSTN, SMS, CDMA/GPRS or other transport;
6. **vehicle terminal** — radio/GPS/data terminal mounted in taxi;
7. **vehicle telemetry** — coordinate, heading, occupancy/vacancy and timestamp;
8. **public phone number** — e.g. city/company booking line;
9. **Web site / booking page**;
10. **Web booking form**;
11. **SMS/WAP/mobile-Web entry point**;
12. **passenger smartphone client**;
13. **driver smartphone client**;
14. **passenger account / phone identity**;
15. **driver account**;
16. **vehicle record bound to driver/account**;
17. **pickup location record**;
18. **destination record**;
19. **ride request**;
20. **dispatch/broadcast event**;
21. **candidate-driver set**;
22. **driver response / acceptance**;
23. **match assignment**;
24. **ETA / route estimate**;
25. **physical approach to pickup point**;
26. **pickup / passenger boarding**;
27. **meter or platform trip-start state**;
28. **route actually driven**;
29. **fare estimate**;
30. **metered/platform final fare**;
31. **payment instruction**;
32. **payment settlement**;
33. **cancellation**;
34. **complaint / safety case**;
35. **trip-history record**;
36. **historical Web/app capture**.

A source that proves one must not silently prove the others.

---

## 2. Core state machine

A useful generic reconstruction is:

```text
passenger has transport need
-> passenger chooses entry point
   [street hail | taxi rank | phone | SMS | Web | WAP | app]
-> pickup description / coordinate created
-> request submitted
-> dispatch system accepts request
-> candidate vehicle set generated
-> request offered/broadcast/assigned
-> driver receives request
-> driver accepts
-> passenger receives car/driver confirmation
-> driver travels toward pickup
-> driver reaches a physically usable pickup point
-> passenger and driver identify each other
-> passenger boards
-> trip is started in meter/platform
-> vehicle travels
-> destination reached
-> fare finalised
-> payment completed
-> order/trip closed
-> complaint/refund/safety process, if any
```

Every arrow is a possible historical state gap.

---

## 3. The most important gaps

### 3.1 physical-taxi / digital-record gap

A vehicle can physically exist without being represented in a dispatch network.

Conversely, an old database record can persist after a vehicle is retired, reassigned or offline.

So:

```text
vehicle exists != vehicle represented in platform
```

### 3.2 registered-vehicle / operational-vehicle gap

```text
registered in fleet
!= currently roadworthy
!= currently on shift
!= currently connected
!= currently accepting passengers
```

Historical fleet size cannot be used as executable supply.

### 3.3 GPS-coordinate / live-telemetry gap

A vehicle having GPS hardware does not prove that a dispatch centre receives timely coordinates.

Separate:

```text
GPS device installed
-> coordinate acquired
-> coordinate transmitted
-> server receives it
-> timestamp remains fresh
-> occupancy/vacancy state is accurate
```

A 2007 Wuxi driver saying his GPS was “basically used as a car phone” is exactly the kind of evidence that blocks `installed hardware = working dispatch infrastructure`.

Source:
https://news.sina.com.cn/c/2007-11-27/090012976371s.shtml

### 3.4 vacant-light / dispatch-availability gap

A taxi may show “空车” on the street but already be travelling to a digital booking.

The inverse is also possible: a platform may regard a driver as online, while the driver is not willing to take the next request.

```text
street vacancy != platform availability
platform online != street vacancy
```

This became socially visible during the 2013–14 taxi-app transition.

### 3.5 phone-connected / booking-created gap

Calling a dispatch number is not proof that a valid booking exists.

Human dispatch may fail to find a vehicle, misunderstand an address, or leave the request unmatched.

### 3.6 Web-form-render / executable-booking gap

A preserved form proves only that the site presented an interface.

It does not prove:

- the form action still worked;
- the dispatch backend was reachable;
- the address parser recognised the input;
- candidate vehicles existed;
- a vehicle accepted;
- the taxi arrived.

### 3.7 address-string / pickup-coordinate gap

The 2006 Shanghai Qiangsheng Web-booking workflow required users to enter road name, house number and waiting place. Contemporary reporting warned that spelling/address errors could make GPS search fail.

Source:
https://news.sina.com.cn/o/2006-04-10/12518659970s.shtml

Therefore:

```text
human-readable pickup description
!= geocoder-recognised location
```

### 3.8 map-coordinate / legal-pickup-point gap

A precise point can still be unusable because of:

- road barriers;
- one-way traffic;
- elevated roads;
- gated compounds;
- taxi stopping restrictions;
- airport/rail-station pickup rules;
- opposite carriageways;
- mall entrances with identical names.

So better GPS does not eliminate pickup-location ambiguity.

### 3.9 request-submitted / system-accepted gap

Network failure, account state, malformed address, throttling, app/server incompatibility or unsupported geography can prevent a client-side submission from becoming a server-side request.

### 3.10 system-accepted / driver-notified gap

A request stored in the server does not prove that any driver terminal received it.

### 3.11 driver-notified / driver-accepted gap

A driver can hear/see the request and ignore it.

The 2013 Beijing day-in-the-life report is unusually valuable: driver Dong received multiple official dispatch requests and simply declined them because pickup deadheading, direction or destination made them economically unattractive.

Source:
https://news.sina.com.cn/c/2013-06-06/000027326134.shtml

### 3.12 accepted / approaching gap

A driver may accept and then remain stationary, take another task, call the passenger, cancel, or become unreachable.

Later user reports make this gap explicit; older archives should not assume it away merely because the interface says “司机已接单”.

### 3.13 matched / pickup gap

This is the central operational boundary:

```text
match record != passenger physically picked up
```

The match can fail through no-show, wrong entrance, cancellation, vehicle mismatch, traffic, phone failure or driver/passenger misunderstanding.

### 3.14 profile-driver / physical-driver gap

Do not assume the person behind the wheel is necessarily the account/profile owner.

2018 investigations of “马甲网约车” are post-core-period but prove why this distinction must be preserved when reading 2012–15 platform records.

### 3.15 profile-vehicle / physical-vehicle gap

Same logic for licence plate/model/vehicle binding.

### 3.16 ETA-render / arrival-time gap

An ETA is a forecast generated from a particular network state and model.

Archive screenshots of “3分钟到达” do not prove actual arrival in three minutes.

### 3.17 fare-estimate / final-fare gap

Especially after route choice, waiting, dynamic pricing, tolls, tips, booking fees or meter rules:

```text
estimated fare != final charge
```

### 3.18 payment-authorised / settlement gap

A payment UI may report initiation/authorisation while later settlement, refund or charge reversal remains unresolved.

### 3.19 order-complete / physical-trip gap

2014 subsidy gaming reports matter methodologically because platform incentives could reward the database state “completed order”.

Source:
https://finance.people.com.cn/n/2014/0127/c70846-24240560.html

Therefore a completed digital order is not by itself proof that a passenger was transported.

### 3.20 passenger-cancelled / downstream-cancelled gap

The 2013 Beijing 96106 report describes a passenger cancelling an airport booking but subsequently receiving many success messages and calls from drivers who had received copies of the request.

Source:
https://news.sina.com.cn/c/2013-06-06/000027326134.shtml

This is a direct example of distributed dispatch state becoming inconsistent.

---

## 4. Historical layers within Chinese scope

### 4.1 1995 boundary: phone dispatch already exists

A 2024 Beijing Daily report says the Beijing taxi dispatch centre was established in 1995 and provided telephone taxi matching.

Source:
https://bj.people.com.cn/n2/2024/0427/c14540-40825685.html

Evidence status: **later institutional retrospective, not a verified 1995 Web source**.

Use only to establish the pre-/early-Web boundary. Do not infer 1995 order volume, terminal technology or coverage from the present system.

### 4.2 2004 Suzhou: phone front end, GPS/computer back end

Contemporary reporting says nearly 2,000 taxis had GPS. A caller contacted the dispatch line; an operator used a computer to search nearby vacant vehicles, saw plate/driver/phone information, then connected passenger and driver to clarify location.

Source:
https://news.sohu.com/20040901/n221827977.shtml

This is an important old-Web lesson:

> **consumer Web use is not necessary for digital infrastructure to mediate an ordinary transaction.**

If archaeology studies only browser-visible pages, it will undercount digital coordination already happening behind telephone interfaces.

### 4.3 2004–05 Shanghai: city-scale dispatch platform as policy target

Contemporary reporting says Shanghai planned to bring its taxi fleet into a unified dispatch platform and allow telephone, Internet and fixed-rank access.

Sources:

- https://news.sohu.com/20041112/n222949104.shtml
- https://auto.sina.com.cn/news/2005-01-01/092393374.shtml

Do not collapse:

```text
policy target
!= installed terminal
!= connected taxi
!= responsive driver
!= successful pickup
```

### 4.4 2006 Shanghai Qiangsheng: one of the clearest Web-to-vehicle workflows

Contemporary reports identify `www.62580000.com` and describe a Web form for immediate taxi booking.

The reported chain is:

```text
public Web booking form
-> address/phone/name submission
-> GPS lookup
-> CDMA/GPRS dispatch infrastructure
-> nearby vacant vehicle terminals
-> response
-> vehicle number shown to passenger
-> physical vehicle arrival
-> driver calls passenger
```

Sources:

- https://news.sina.com.cn/o/2006-04-02/13598593326s.shtml
- https://news.sina.com.cn/o/2006-04-10/12518659970s.shtml

Important period-specific constraints from the report:

- immediate booking only, not future reservation;
- address text had to be sufficiently exact;
- system searched within a reported radius;
- Web page could return “no vehicle”; 
- fallback remained telephone contact.

This is **not** merely a primitive smartphone app. The user supplied textual place identity; the server/dispatch network tried to map it into vehicle geography.

### 4.5 2007 Wuxi: infrastructure failure through participation failure

Contemporary reporting says around 1,000 taxis had received GPS terminals in 2003, but by 2007 only around 60 remained registered for dispatch; driver Huang Lian said his GPS was effectively just a vehicle phone.

Source:
https://news.sina.com.cn/c/2007-11-27/090012976371s.shtml

This case should remain a standing counterexample against deterministic narratives:

```text
hardware installed
+ call centre exists
+ publicised service promise
!= durable dispatch market
```

The missing layer can be incentives, demand density and willingness to respond.

### 4.6 2012: smartphone two-sided matching

Contemporary Hangzhou reporting on Kuaidi shows a passenger smartphone sending a request and drivers responding, with extra payment/tip affecting response time.

Source:
https://www.chinanews.com/auto/2012/10-09/4233192.shtml

At this point the archival object becomes much more difficult than a Web form because important states move into:

- passenger app;
- driver app;
- mobile GPS;
- push/voice notification;
- server candidate set;
- driver response race;
- phone confirmation.

### 4.7 2013: official dispatch and commercial apps coexist

A June 2013 Beijing Youth Daily day-in-the-life report captures a taxi using:

- street hailing;
- 96106 official dispatch;
- an older dispatch terminal;
- Didi smartphone app.

Source:
https://news.sina.com.cn/c/2013-06-06/000027326134.shtml

This is methodologically superior to a simple company launch date because it proves **workflow coexistence inside one driver’s day**.

### 4.8 2013: location/vehicle-state quality was explicitly not solved by “having an app”

A January 2013 report says an official Beijing mobile taxi client was experimental and could not yet query nearby vacant vehicle positions. A transport-information official stated that accurate service required timely vehicle-location transmission, accurate vehicle status and appropriate management rules.

Source:
https://auto.sina.com.cn/news/2013-01-01/12231084785.shtml

This directly supports:

```text
app installed
!= accurate live dispatch state
```

### 4.9 2014: platform adoption changes street-hail semantics

Contemporary Beijing/Shanghai reporting records vacant-looking taxis passing street hailers because they were waiting for or travelling to app bookings. Shanghai temporarily restricted taxi-app use during peaks.

Sources:

- https://mobile.people.com.cn/n/2014/0123/c183175-24203793.html
- https://www.chinanews.com/df/2014/02-24/5873722.shtml
- https://politics.people.com.cn/n/2014/0226/c70731-24474876.html

This creates an important archaeological gap:

> A photo of a green “空车” roof light no longer guarantees the same social meaning it had before app dispatch.

Digital reservation can change the semantics of a physical indicator.

### 4.10 2014: payment becomes another state machine

Didi/WeChat Pay and Kuaidi/Alipay subsidy campaigns tied request/match/trip/payment states together.

Sources:

- https://finance.people.com.cn/n/2014/0127/c70846-24240560.html
- https://politics.people.com.cn/n/2014/0218/c70731-24387462.html

An old screenshot reading “支付成功” still should not be used to infer the physical trip without corroboration.

### 4.11 2015 boundary: taxi-hailing platform broadens beyond licensed-taxi matching

By 2015, Didi/Kuaidi’s service set had expanded beyond the initial taxi-hailing use case toward multiple vehicle-service categories.

For this note, do not retroactively relabel 2012–13 licensed-taxi app workflows as if they were already the mature 2016+ regulatory category “网约车”.

This is a terminology boundary as well as a product boundary.

---

## 5. Interface-specific archaeology

### 5.1 Street hail

Likely surviving evidence:

- street photography;
- regulation;
- roof-light design;
- taxi-rank maps;
- first-person waiting accounts.

Missing states:

- how long a specific person waited;
- how many empty taxis passed;
- whether a driver saw a raised hand;
- whether a car was already digitally booked.

### 5.2 Telephone dispatch

Possible surviving evidence:

- public booking numbers;
- tariff cards;
- press reports;
- dispatch manuals;
- call-centre screenshots;
- operator training documents.

Usually missing:

- audio of ordinary calls;
- complete queue state;
- rejected requests;
- driver radio/terminal response;
- actual pickup completion.

### 5.3 SMS booking

Need to distinguish:

```text
SMS sent by passenger
-> carrier accepted
-> dispatch gateway accepted
-> request parsed
-> vehicle found
-> response SMS generated
-> response delivered
```

A press release saying “支持短信订车” proves only advertised capability unless a transaction trace is also available.

### 5.4 Web booking

For a 2004–10 Web taxi-booking case, archive at least:

- exact original URL;
- capture datetime;
- HTTP result;
- charset evidence;
- form fields;
- form action;
- script dependencies;
- whether result/status pages are public/session-bound;
- any cross-host dispatch endpoint;
- help/documentation describing fallback behaviour.

### 5.5 Smartphone apps

By 2012–15, a browser-only archaeological method is insufficient.

Need, where legally available:

- passenger APK/IPA/version metadata;
- driver-client version metadata;
- screenshots;
- app-store descriptions;
- permissions;
- map SDK references;
- API hostnames;
- push-notification dependency;
- phone/SMS verification flow;
- payment SDK handoff;
- contemporaneous manuals/tutorials.

Never execute an untrusted historical APK on a personal device merely to “see what happens”. Use isolated analysis if binaries are studied.

---

## 6. Preservation asymmetries

### 6.1 Web-shell / geospatial-state loss asymmetry

A crawler may preserve:

- taxi-company home page;
- “网上订车” link;
- booking form;
- promotional copy;
- city list;
- pricing help.

It usually does **not** preserve:

- nearby vehicle set at 10:17:22;
- each coordinate’s freshness;
- vacant/occupied bit;
- driver response race;
- ETA recalculation;
- physical pickup.

Therefore:

> **historical booking UI != historical dispatch world state**.

### 6.2 app-binary / backend-loss asymmetry

An APK can survive while the service dies because API endpoints, certificates, map tokens, SMS gateways, authentication and driver-side peers disappear.

So:

```text
client binary survives != historical service is replayable
```

### 6.3 public-promotion / private-trip authority inversion

The most easily archived records are often weakest for proving a real trip:

- “最快3分钟叫到车” advertisement;
- screenshot of map cars;
- city-coverage claim;
- download page.

The strongest records are private and should usually remain private:

- passenger phone number;
- home/hospital/school pickup point;
- exact trip GPS trace;
- driver identity;
- payment details;
- complaint recording;
- emergency-contact data.

Do not solve the historical-visibility problem by republishing identifiable trip histories.

### 6.4 successful-mediation invisibility

A person may phone a taxi number and benefit from GPS/computer dispatch while leaving no Web trace at all.

Thus a browser archive can systematically understate the degree of digitisation in ordinary transport.

### 6.5 dramatic-failure visibility bias

News archives disproportionately preserve:

- violence;
- scams;
- refusal;
- subsidy wars;
- strikes;
- spectacular waiting queues;
- regulatory crackdowns.

The ordinary successful 14-minute ride generates little public evidence.

Do not infer failure rate from news visibility.

---

## 7. Exact negative-evidence rules for this topic

Allowed:

> No verified Memento was obtained in this slice for the 2006 `www.62580000.com` booking form.

Not allowed:

> The page was never archived.

Allowed:

> Contemporary reporting says the service used CDMA/GPRS and a Web form.

Not allowed without capture/device documentation:

> The page required IE6 / ActiveX / GB2312 / Flash.

Allowed:

> A 2013 report says the experimental Beijing mobile client could not yet query nearby vacant-vehicle positions.

Not allowed:

> No taxi app in Beijing had live vehicle data in 2013.

Allowed:

> A photographed taxi shows an “空车” sign.

Not allowed:

> The taxi was actually available to the photographer.

---

## 8. Candidate evidence table

| Date | Object | Evidence class | Proven | Still unknown |
|---|---|---|---|---|
| 1995 (reported 2024) | Beijing taxi dispatch centre | C/B | telephone matching organisation existed | contemporary interface, call volume, exact terminal system |
| 2004 | Suzhou GPS phone dispatch | B+ | operator searched nearby vacant taxis on computer | exact protocol, update rate, full success rate |
| 2004 | Shanghai unified dispatch plan | B | policy/technical integration target | actual 2007 completion |
| 2005 | Shanghai 96965 | B+ | unified number launched, initial dispatchable fleet | real pickup completion rate |
| 2006 | `62580000.com` Web taxi booking | B+ | reported form fields and Web→CDMA/GPS workflow; reporter test | verified historical DOM/charset/form action/capture |
| 2007 | Wuxi GPS dispatch | B+ | hardware existed but driver participation collapsed | exact reasons by driver distribution |
| 2007 | Beijing wheelchair passenger | B+ | booking channel could address home pickup; vehicle accessibility still constrained | population prevalence |
| 2012 | Kuaidi early app | B+ | smartphone request/driver response and tip-linked response | exact client binary/API protocol |
| 2013 | Beijing official mobile taxi client | B+ | app availability did not imply accurate vacant-vehicle query | exact version/network architecture |
| 2013 | Didi + 96106 + street hail in one taxi | A/B | simultaneous workflow coexistence and driver selection | aggregate driver distribution |
| 2014 | taxi-app subsidy/payment | B | payment incentives attached to digital order states | physical truth of any uncorroborated order |
| 2014 | Shanghai peak restriction | A/B | regulator treated app orders and street service as interacting markets | long-term causal size |
| 2015 | platform service broadening | B | taxonomy changed beyond taxi-only matching | exact per-city availability by date |

---

## 9. M1 historical-capture status

**M1 verified historical Chinese taxi-booking / taxi-app capture: NOT ACHIEVED IN THIS SLICE.**

Search leads now include:

- `www.62580000.com` explicitly named in April 2006 contemporary reports;
- early 2012–14 Didi/Kuaidi app references;
- current/reprinted pages describing old workflows.

What is still required before upgrading an early Web case to M1:

1. exact original URL;
2. archive capture URL;
3. capture datetime;
4. HTTP/result metadata where available;
5. charset evidence from header/meta/raw bytes;
6. DOM/form-field recovery;
7. form action / endpoint chain;
8. script/image dependencies;
9. status/result-page behaviour where recoverable;
10. a second historical time point if making change-over-time claims.

Do **not** write “Wayback did not save it” from failure to obtain it in this run.

---

## 10. Next retrieval priorities

### Priority A — 2006 Qiangsheng Web booking

Try to recover a genuine `62580000.com` 2006–08 Memento and determine:

- whether the booking form itself was crawlable;
- charset;
- field names;
- form action;
- JS validation;
- CAPTCHA implementation;
- status lookup URL;
- whether submitted data crossed hosts;
- whether result pages were session/private.

### Priority B — early passenger/driver app pair

Find a precisely dated 2012–13 passenger client and driver client for Didi/Kuaidi/other major taxi app.

Record version separately for each side. A passenger screenshot alone cannot reconstruct dispatch behaviour.

### Priority C — vehicle terminal documentation

Seek Shanghai/Suzhou/Wuxi taxi-terminal technical manuals or procurement specifications showing:

- GPS update interval;
- vacant/occupied state source;
- GPRS/CDMA message transport;
- dispatch acknowledgement;
- text/voice payload;
- loss-of-signal behaviour.

### Priority D — street-hail semantics after app adoption

Use contemporaneous 2013–15 photos/reports to document when “空车” ceased to be sufficient evidence of immediate street availability because a taxi might already be committed to an app booking.

---

## 11. Cross-link to `how-people-lived`

The life-history package should carry the broader question:

> **When did an ordinary person stop needing a vacant taxi to physically pass in front of them before they could begin arranging a ride?**

This old-Web note contributes the technical answer: the transition was not one jump from street hail to app. It passed through telephone, human dispatch, radio/data terminals, GPS, SMS, Web forms and finally portable two-sided clients.

The key historical caution is equally important:

> **Digitising the request does not digitise the pickup itself. The archive can preserve a request, a map and a “matched” status while losing the one fact ordinary life actually depended on: did the car come?**
