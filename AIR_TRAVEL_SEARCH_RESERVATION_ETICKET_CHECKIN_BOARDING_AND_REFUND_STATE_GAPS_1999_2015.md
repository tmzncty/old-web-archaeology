# Air-travel search, reservation, e-ticket, check-in, boarding and refund state gaps, 1999–2015

> Scope: Chinese old Web / Web-adjacent airline passenger systems, roughly 1999–2015.
>
> Cross-life-history note: `tmzncty/how-people-lived/topics/air-ticket-dematerialization-self-checkin-and-boarding-executability-china-1979-2026.zh-CN.md`
>
> This file does **not** attempt a general history of Chinese civil aviation. It asks a narrower archaeology question: when a historical page says a flight was available, booked, ticketed, checked in, or “paperless”, what exact state did the Web page know, what authority sat behind it, and what can an archive actually preserve?

## 0. Why aviation needs its own state model

Air travel is unusually dangerous for story-first reconstruction because many distinct records can look like one transaction to a passenger:

```text
schedule
→ inventory/availability
→ fare quote
→ passenger name record (PNR)
→ payment
→ ticket issuance / e-ticket coupon
→ itinerary receipt
→ check-in
→ seat assignment
→ boarding pass
→ identity/travel-document verification
→ baggage acceptance
→ security/border clearance
→ gate acceptance
→ actual boarding
→ flight operation
→ flown coupon / settlement
```

A Web page may expose only one or two layers while the authority resides in another system.

Therefore the following claims are never interchangeable:

**flight listed != flight operates**  
**seat shown != seat sellable now**  
**reservation exists != ticket issued**  
**payment submitted != ticketed**  
**e-ticket exists != itinerary receipt authentic**  
**checked in != boarding pass accepted**  
**boarding pass accepted at security != passenger boarded**  
**boarding recorded != flight departed**  
**refund requested != refund approved != money returned**.

This is the aviation version of the repository's general `platform / page / account / capture / claim` discipline.

---

## 1. Boundary prehistory: the old Web inherited a much older networked backend

The main object of this repository remains Chinese Web history around 1995–2015. A short prehistory is necessary only because the public Web did not create airline inventory from scratch.

China TravelSky's current official corporate history traces its institutional origin to the Civil Aviation Computer Information Center from 1979 and describes its long-running reservation, departure-control, distribution and settlement systems.

Source:
- TravelSky current official corporate profile: <https://www.infosky.com.cn/travelsky/xxgk/qyjbxx/A069011002Gone1.html>

Artifact status: **current corporate retrospective, not a historical Web capture**.

Claim limit: this supports a pre-Web industry-computing boundary. It does **not** prove that a household in 1985 could directly access these systems, nor does it establish exact historical UI/protocol versions.

A useful external comparator is IBM's SABRE history: airline reservation terminals were networked over telephone lines decades before ordinary customers booked on the Web; American Airlines later extended terminals to travel agents in 1976 and consumer access through online services in the 1980s.

Source:
- IBM History, “Sabre”: <https://www.ibm.com/history/sabre>

This comparator belongs mainly in the cross-life-history repo; here it protects one archaeological rule:

> **public-Web emergence must not be mistaken for backend-computerization emergence.**

---

## 2. 1999–2001: TravelSky.com exposes live industry state to the public Web

A 2001 Cathay Pacific corporate release states that TravelSky.com launched in December 1999 and could provide real-time schedules, seat availability, prices and booking for all 25 Chinese commercial airlines plus Air Macau. It also states that the Civil Aviation Computer Information Center supplied inventory-control, CRS and airport passenger-processing systems, with a network then extending across 300+ mainland cities, 80 foreign cities and 28,000+ terminals.

Source:
- Cathay Pacific, 2001-04-19: <https://news.cathaypacific.com/cathay-pacific-outlines-travelsky-cooperation>

Evidence status: **contemporary corporate source / strong locator and capability evidence**.

It establishes a critical topology:

```text
public Web browser
        ↓
TravelSky.com Web front end
        ↓
industry reservation/distribution systems
        ↓
airline inventory / fare / passenger-processing state
```

The public page therefore must not be treated as the authoritative inventory itself.

### State gaps introduced here

#### `schedule-page / operational-flight gap`
A timetable can list a future flight that is later cancelled, retimed or consolidated.

#### `availability-render / executable-inventory gap`
A query can render seats available at time T1 while another channel consumes inventory before the user completes booking at T2.

#### `fare-display / ticketable-fare gap`
A displayed fare may depend on booking class, passenger type, date, tax, remaining inventory or rule conditions not preserved in the search-result shell.

#### `Web-front-end / CRS-authority gap`
The browser may merely project state from a backend reservation system. Replaying the HTML shell years later does not recreate historical CRS inventory.

#### `public-query / historical-snapshot gap`
A preserved search form proves a query interface existed. It does not prove what result the same date/route query returned in 2001.

---

## 3. 2000–2006: electronic ticketing must be separated from online purchase

Contemporary industry material records China Southern introducing an electronic ticket around 2000, with Air China and China Eastern following in 2003. By 2006 the Civil Aviation Administration was pushing industry-wide e-ticketing and simplified passenger procedures.

Sources:
- China Civil Aviation News / China Eastern e-commerce manager, 2005-07-13: <https://tech.sina.com.cn/it/2005-07-13/0911661465.shtml>
- Xinhua/CAAC, 2006-05-31: <https://finance.sina.com.cn/chanjing/b/20060531/22002613730.shtml>
- China Youth Daily, 2006-06-02: <https://finance.sina.com.cn/chanjing/b/20060602/07032618565.shtml>

The archaeological rule is simple:

> **e-ticket != Web booking**.

An e-ticket is an electronic transport record. It can be created after a Web purchase, a telephone transaction, or an agent-terminal transaction.

### Core ticket-state model

```text
search result
→ booking request
→ PNR / reservation record
→ payment authorization
→ ticket issuance
→ e-ticket number + coupon status
→ itinerary receipt / invoice-like document
```

Each arrow is a possible failure or delay boundary.

### State gaps

#### `PNR / e-ticket gap`
A reservation record can exist before ticket issuance or can be cancelled if payment/ticketing time limits expire.

#### `payment-submit / payment-authorized gap`
A Web confirmation screen can reflect submission without proving settlement.

#### `payment-authorized / ticket-issued gap`
Funds movement and ticket issuance are distinct backend acts.

#### `ticket-issued / itinerary-receipt gap`
The transport entitlement can exist without the passenger currently holding a paper itinerary receipt.

#### `itinerary-receipt / ticket-authority gap`
A printed document can be forged or altered while the backend ticket record says something else.

#### `paper-lost / transport-entitlement gap`
Once e-ticketing is authoritative, loss of a paper representation need not destroy the transport right.

This last gap is historically important because it changes what an archive should consider the “ticket”: the visible paper artifact becomes evidence of a backend record, not necessarily the primary authority.

---

## 4. 2006–2010: verification sites expose authority without exposing transaction history

By late 2006, contemporary reporting says TravelSky's “信天游” site provided electronic-ticket verification in response to fake itinerary receipts and problematic agents.

Source:
- Beijing Daily via Sina, 2006-12-22: <https://news.sina.com.cn/s/2006-12-22/071210835344s.shtml>

A 2010 consumer guide still directs travelers to `www.travelsky.com` for ticket verification and describes matching passenger/ticket information against the authoritative record.

Source:
- 2010-01-26 guide syndicated by China Weather: <https://news.weather.com.cn/index/lssj/01/376565_6.shtml>

### Verification state gaps

#### `verification-form / authoritative-query gap`
A preserved form proves that fields existed. It does not prove that a particular historical ticket validated successfully.

#### `verification-response / public-archive gap`
A real response may contain passenger name, identity data, fare, ticket number or agency information. It is both transaction-authoritative and privacy-sensitive, so it is less suitable for public archival preservation than the generic form.

#### `receipt-visual / backend-match gap`
Visual similarity to an itinerary receipt is not equivalent to a matching authoritative ticket record.

This creates a recurring repository pattern:

## `public-shell / private-authority inversion`

The easiest artifact to archive is the generic public verification page; the evidence that most strongly proves a real transaction is the response that should generally **not** be republished.

---

## 5. 2008–2010: Web check-in moves one airport transaction into the old Web

Contemporary Air China material says that on the first day of its move to Beijing Capital Airport T3 in March 2008 more than a thousand travelers used online check-in. Eligible e-ticket passengers could select seats and print boarding passes before reaching the airport.

Source:
- Air China, 2008-03-27: <https://www.prnasia.com/story/9346-1.shtml>

In 2008 Air China and China Southern described A4-paper boarding passes with 2D barcodes; 2009 Shandong Airlines and China Eastern described passengers using an Internet-connected computer plus ordinary printer to check in at home/office, while checked baggage still required a counter.

Sources:
- Air China, 2008-04-23: <https://www.prnasia.com/story/9982-1.shtml>
- CAAC / China Southern, 2008-04-23: <https://www.caac.gov.cn/PHONE/XWZX/HYDT/200804/t20080423_18688.html>
- Shandong Airlines, 2009-02-26: <https://travel.sina.com.cn/air/2009-02-26/092565153.shtml>
- China Eastern, 2009-03-03: <https://travel.sina.com.cn/air/p/2009-03-03/135766484.shtml>

### Check-in must be modelled separately from ticketing

```text
valid e-ticket
→ check-in window opens
→ passenger/flight eligible
→ seat map rendered
→ seat selected
→ check-in committed
→ boarding-pass object generated
→ paper/2D representation produced
→ airport security accepts it
→ gate accepts it
```

### State gaps

#### `ticketed / check-in-eligible gap`
A valid e-ticket does not mean online check-in is currently open or permitted for that passenger/route.

#### `seat-map-render / seat-assignment gap`
A seat displayed as available is not assigned until the transaction commits.

#### `seat-assignment / boarding-pass gap`
The seat record and the passenger-facing boarding-pass representation are distinct.

#### `boarding-pass-file / successful-print gap`
An A4-era workflow can fail at the local printer even though check-in is complete.

#### `print-success / security-acceptance gap`
A visually present boarding pass still requires identity/security validation.

#### `online-check-in / baggage-acceptance gap`
Checked baggage remains a physical custody transaction even after check-in moves online.

#### `standard-passenger / special-passenger gap`
Children, infants, disabled travelers, unaccompanied passengers, international-document cases and other special-service categories often remain outside the first self-service path.

This is especially important for life-history research: **the easiest path to digitize often encodes a “standard adult traveler” model.**

---

## 6. 2008 “Fast Travel”: paperless aviation was a bundle of independent subsystems

CAAC's 2008 report on IATA/TravelSky “Fast Travel” explicitly breaks self-service into six areas: check-in, baggage, travel-document checking, flight rebooking, boarding and baggage tracing.

Source:
- CAAC, 2008-11-14: <https://www.caac.gov.cn/XWZX/HYDT/200811/t20081114_18060.html>

This is unusually useful primary-near evidence because it prevents the archaeologist from collapsing “paperless travel” into a single feature flag.

### Required distinction

**paperless ticketing**  
!= **online check-in**  
!= **self bag drop**  
!= **self document check**  
!= **electronic boarding pass**  
!= **self boarding**  
!= **baggage tracing**.

A 2008 airline could be advanced in one of these and entirely manual in another.

---

## 7. 2010: WAP/mobile check-in creates another rendering layer

In August 2010 China Eastern and Shanghai Airlines trialed mobile check-in at Shanghai Hongqiao T2. Travelers entered through a WAP page, received an SMS/link, and displayed a two-dimensional barcode on the phone. Passengers without checked baggage could go to designated security channels; passengers with baggage still used counters.

Sources:
- China National Radio via Sina, 2010-08-16: <https://news.sina.com.cn/c/2010-08-16/110820907195.shtml>
- China Eastern operations report, 2010-09-15: <https://mil.news.sina.com.cn/s/2010-09-15/1555610965.html>

Air China launched a mobile platform the same month supporting booking, payment, seat selection, mobile check-in and flight-status queries across then-common iPhone, BlackBerry, Nokia, Motorola, Samsung, LG, Sony Ericsson and Dopod platforms.

Source:
- Air China, 2010-08-17: <https://www.prnasia.com/story/35032-1.shtml>

### Mobile-specific gaps

#### `WAP-page / device-compatibility gap`
A preserved WAP URL does not establish that every handset could render or execute it.

#### `check-in-committed / SMS-delivered gap`
The server can complete check-in while the confirmation SMS/link fails to reach the device.

#### `SMS-delivered / barcode-renderable gap`
Delivery does not guarantee the browser can retrieve/render the barcode.

#### `barcode-renderable / scanner-readable gap`
A visible barcode is not necessarily readable at the airport device.

#### `mobile-boarding-pass / phone-operational gap`
Battery, screen damage and local device state become part of boarding executability.

This is an example of `failure-mode migration`: paper-loss risk decreases while device/runtime dependencies increase.

---

## 8. 2011–2015: what should a historical airline capture actually prove?

The minimum useful old-Web object is not a screenshot saying “online booking”. A strong case should try to preserve one complete historical workflow slice.

### M1 — historical public shell

For one airline/TravelSky historical date, verify:

- original URL;
- archive URL;
- capture datetime;
- HTTP status;
- declared/observed charset;
- DOM/page structure;
- form action;
- script/CSS/image dependencies;
- whether results require live backend state.

### M2 — transaction boundary

For the same workflow, identify which step crosses into another authority:

- TravelSky CRS/GDS;
- airline host;
- payment gateway/bank;
- e-ticket database;
- airport departure-control system;
- SMS gateway;
- identity/document verification;
- refund/settlement system.

### M3 — second historical timepoint

Compare another capture after a feature transition such as:

- paper/e-ticket coexistence → e-ticket default;
- Web booking → Web check-in;
- A4 boarding pass → mobile barcode;
- static schedule → dynamic booking engine;
- airline-hosted front end → cross-host TravelSky service.

Only then should a case claim a concrete interface transition.

---

## 9. Archive failure modes specific to airline Web systems

### 9.1 `shell-survival / inventory-loss asymmetry`

A crawler can preserve logos, fare-search fields and “立即预订” buttons while the historical seat inventory is gone. Replaying the form against today's backend is **not** evidence of 2008 availability.

### 9.2 `static-timetable / operational-state gap`

A preserved scheduled flight can later have been delayed, cancelled or retimed. Timetable archaeology is not flight-operation archaeology.

### 9.3 `public-page / private-PNR asymmetry`

The public sales shell is highly archivable; real PNRs are private and usually inaccessible. This means archive evidence systematically overrepresents intended workflows and underrepresents transaction failures.

### 9.4 `ticket-record / itinerary-receipt asymmetry`

The durable authority at travel time may be a backend e-ticket coupon, while the archive is more likely to preserve a photographed/scanned itinerary receipt or generic instructions. The more visible artifact can be the less authoritative one.

### 9.5 `client-side / host-system dependency`

Historical JavaScript, applets, WAP pages or form actions can survive while the host system/API no longer understands them.

### 9.6 `cross-host transaction loss`

A single booking path can traverse airline domain → TravelSky → bank/payment host → airline confirmation → SMS. Single-host crawling can leave a false impression of an incomplete or nonfunctional site even when the original transaction succeeded across hosts.

### 9.7 `successful-telephone-transaction invisibility`

E-ticketing and computerized reservation systems also supported telephone and agent-assisted transactions. A traveler can be fully mediated by digital infrastructure and leave **no consumer Web trace at all**.

This is `transactional invisibility by mediation`, already observed in hotel-booking archaeology and especially important in aviation.

---

## 10. Page-state contract for future cases

For every historical airline page, record at least:

| Field | Required note |
|---|---|
| `artifact_kind` | current page / contemporary article / screenshot / verified capture / manual / company filing |
| `capture_datetime` | exact if verified; otherwise unknown |
| `original_url` | exact historical locator if known |
| `displayed_date` | page/article date; not automatically capture date |
| `workflow_role` | schedule / search / fare / booking / payment / ticket / verify / check-in / boarding / refund |
| `authority_system` | Web front end / TravelSky / airline host / DCS / bank / airport / unknown |
| `state_claim` | what the page actually demonstrates |
| `state_not_proved` | next transaction step not demonstrated |
| `privacy_risk` | PNR/name/ID/ticket number/boarding barcode/payment etc. |
| `runtime_dependency` | browser/JS/WAP/printer/barcode scanner/live backend/etc. |
| `date_confidence` | high / medium / low |

A historical screenshot should never silently substitute for a transaction record.

---

## 11. Evidence ledger

| Date | Source | Evidence class | Supports | Does not support |
|---|---|---|---|---|
| 1979→current retrospective | TravelSky official profile | C/B | pre-Web institutional computing boundary | exact old client/protocol or household access |
| 1999/2001 | Cathay Pacific / TravelSky cooperation release | A/B contemporary | live public scheduling/availability/fare/booking capability; backend terminal network | mass consumer adoption; preserved 1999 UI |
| 2005 | China Civil Aviation News / MU e-commerce | B contemporary | early airline e-ticket rollout chronology | all-airline penetration at every date |
| 2006 | CAAC/Xinhua/China Youth Daily | A/B | e-ticket simplification and rapid industry adoption | online-purchase share |
| 2006 | Beijing Daily | B | TravelSky verification service as anti-fraud layer | specific ticket validity |
| 2008 | Air China / CAAC | A-near-primary/B | online/A4 self check-in and six-part Fast Travel model | universal passenger eligibility |
| 2009 | airline operation reports | B | home/office/Web check-in; baggage remains physical | historical DOM/runtime |
| 2010 | China Eastern/Air China | A-near-primary/B | WAP/SMS barcode and mobile service transition | every handset/scanner success |

---

## 12. Current historical-capture status

This slice found strong contemporary locators and workflow descriptions for:

- `travelsky.com` / “信天游”;
- `airchina.com.cn` online check-in;
- airline B2C e-ticket sales;
- 2008–2009 A4 boarding-pass flows;
- 2010 China Eastern WAP/mobile check-in.

However, this run did **not** obtain a historical Memento that was opened and verified end-to-end with original URL, capture datetime, HTTP status, charset, DOM, form action and dependent resources.

Therefore:

## `M1 verified historical Chinese airline booking/check-in Memento: NOT ACHIEVED IN THIS SLICE`

This statement means only “not verified in this slice”. It does **not** mean Internet Archive has no capture.

Do not infer from period convention that the historical pages used IE6, GB2312, tables, frames, ActiveX or any particular JavaScript library. Those remain `unknown` until artifact evidence is obtained.

---

## 13. Counterexamples and anti-hindsight rules

1. **Electronic ticket share is not online-booking share.** Telephone and agent channels can create e-tickets.
2. **Website availability is not household accessibility.** A 1999 booking site existed before Chinese mass household Internet access.
3. **“Paperless” is not end-to-end paperless.** Different airports/routes/passenger types moved at different speeds.
4. **Self-service often excludes non-standard cases first.** Special assistance, children, international documents and checked baggage may retain staffed interfaces.
5. **A valid historical page cannot recreate historical inventory.** Never submit a historical date to a current backend and call the result a historical state.
6. **Do not publish real private passenger records merely because they survive.** PNRs, ID numbers, ticket numbers, boarding barcodes and detailed itineraries can be sensitive.
7. **Flight-status text is a time-bound claim.** Scheduled, estimated, cancelled, departed and arrived must not be collapsed.
8. **Archive silence is weak negative evidence.** No located capture != no historical service.

---

## 14. What this adds to old-Web archaeology

The main new conclusion is that airline Web archaeology requires a stronger distinction between **visible page state** and **authoritative operational state** than many ordinary content sites.

A news portal's old article can often be reconstructed from its HTML. An airline site's most important fact—whether one particular seat could really be sold to one particular person at one particular price—may have existed only for seconds inside an industry host system.

The old Web therefore leaves us a peculiar record:

> We can often recover the interface through which people were invited to plan a journey, while the exact inventory, passenger record and settlement state that made one person's journey real have disappeared or properly remain private.

That is not a defect to be papered over with reconstruction. It is itself a historical finding about how public Web interfaces sat on top of older, private, real-time transaction networks.
