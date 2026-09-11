# E-commerce item/order/escrow/shipment/tracking/delivery-confirmation/refund state gaps, 2003–2015

**Scope:** Chinese Web, c. 2003–2015  
**Cross-repo life-history package:** [`how-people-lived/topics/from-postal-parcels-to-e-commerce-and-village-delivery-goods-addressability-delivery-executability-and-remote-household-provisioning-china-1980-2026.zh-CN.md`](https://github.com/tmzncty/how-people-lived/blob/main/topics/from-postal-parcels-to-e-commerce-and-village-delivery-goods-addressability-delivery-executability-and-remote-household-provisioning-china-1980-2026.zh-CN.md)  
**Status:** research note / state-model expansion / verified-capture work still open  
**Date:** 2026-09-12

> This note does **not** treat a surviving Taobao/Alipay page as proof that a historical purchase was executable. The central object is the gap between a public catalog page and the private, time-dependent chain that turned a listing into money, a parcel, physical possession, and sometimes a refund.

## 1. Why this belongs in old-web archaeology

A large share of old-Web reconstruction is page-centered: recover a homepage, a forum thread, a product detail page, a logo, an encoding, or a navigation structure. E-commerce exposes the limit of that model unusually clearly.

A historical marketplace page can survive perfectly while almost everything that made it economically meaningful is gone:

- the seller's real stock at that moment;
- the buyer's login state;
- the negotiated terms in private IM;
- the buyer's bank or Alipay state;
- an escrow hold;
- the generated order number;
- the seller's acceptance/cancellation;
- the carrier chosen;
- the parcel tracking graph;
- delivery attempts;
- the recipient's real identity and location;
- confirmation of receipt;
- a dispute, return, or refund.

Therefore the minimum archaeological unit for Chinese e-commerce cannot be `product page`. It must be a transaction-and-logistics state model.

## 2. Repository evidence contract

Per [`docs/METHOD.md`](./METHOD.md), keep separate:

```text
platform
!= site/host
!= public page
!= account
!= transaction state
!= archive capture
!= claim
```

For this topic, add:

```text
seller
!= seller account
!= store page
!= item listing
!= physical inventory

buyer
!= buyer account
!= payer
!= recipient
!= person who confirms receipt

item listing
!= live stock
!= order
!= paid order
!= escrow-funded order
!= shipment
!= delivered parcel
!= satisfactory item
!= completed transaction

shipment
!= tracking record
!= tracking record being current
!= physical parcel location
!= successful final delivery
```

A search result, secondary screenshot, or later blog saying “this was 2005 Taobao” is only a **candidate locator** until the original archive artifact is opened and checked against the repository's M1 capture contract.

## 3. Core state graph

### 3.1 Product-discovery state

```text
marketplace host reachable
-> category/search page reachable
-> result set returned
-> item page reachable
-> seller/store page reachable
```

But:

```text
item page reachable
!= listing active at historical moment
!= item in stock
!= seller willing/able to ship to buyer region
!= displayed price was final transaction price
```

Historical search results are especially ephemeral. A capture of `www.taobao.com` does not reconstruct which items a query returned at 14:00 on a specific day, how they ranked, or whether paid promotion influenced ordering.

### 3.2 Buyer–seller communication state

2000s Chinese C2C shopping often relied on real-time buyer–seller communication before payment. Contemporary descriptions of Taobao's “旺旺” place bargaining, item questions, and seller availability inside the transaction environment.

The relevant model is:

```text
public listing
-> buyer opens contact channel
-> seller online/offline state
-> private conversation
-> negotiated price/shipping/variant
-> buyer decision
```

Archive consequence:

```text
public item page survives
!= private negotiation survives
```

The negotiated transaction may differ from the visible listing in quantity, shipping cost, variant, promised service, or even destination.

### 3.3 Payment and escrow state

A 2005 contemporary report describes Alipay as holding the buyer's money until the buyer confirms receipt, and records `www.alipay.com` as an independently accessible service host.

Source:
- 人民网/江南时报 contemporaneous report, 2005-02-03: https://finance.sina.com.cn/roll/20050203/04301343972.shtml
- 东方早报 contemporaneous report on upgraded Alipay / full-compensation promise: https://finance.sina.com.cn/roll/20050203/09561345274.shtml

This requires at least the following states:

```text
checkout initiated
!= bank payment initiated
!= bank payment successful
!= Alipay transaction created
!= funds held in escrow
!= seller notified as payable/ship-ready
!= buyer confirmation
!= funds released to seller
```

The key historical innovation is a state that is easy to erase in retrospective prose:

```text
buyer has paid
AND seller has not yet irreversibly received money
```

That state mediated trust between strangers. It cannot be reconstructed from a static item page alone.

### 3.4 Order state

Minimum order model:

```text
cart/intent
-> order creation attempt
-> platform order ID issued
-> payment pending
-> paid/escrowed
-> seller preparing
-> shipped/cancelled/refunded
```

Archive hazards:

- public pages normally do not expose the buyer's order detail;
- order URLs often require authentication/session cookies;
- order status is mutable;
- later screenshots may show only the terminal state;
- old database records may have been migrated into new interfaces, losing historical rendering and intermediate states.

Therefore:

```text
modern “已买到的宝贝” record
!= historical transaction UI
!= proof of every historical intermediate state
```

### 3.5 Logistics state

Alibaba's 2014 SEC F-1 is useful precisely because it separates marketplace transactions from third-party logistics. It states that delivery companies were independent logistics providers; sellers selected delivery providers; an information system linked buyers, sellers and delivery firms; and transactions on Alibaba's China retail marketplaces generated billions of packages handled by the partner network.

Primary company filing:
- Alibaba Group F-1, SEC, 2014: https://www.sec.gov/Archives/edgar/data/1577552/000119312514184994/d709111df1.htm

Minimum logistics chain:

```text
seller marks “shipped”
!= carrier actually accepts parcel
!= pickup scan exists
!= origin sorting complete
!= long-haul transport complete
!= destination station received
!= courier out for delivery
!= delivery attempt succeeds
!= recipient physically receives parcel
```

And:

```text
tracking status
!= physical truth with zero latency
```

A tracking database is itself an interpretation layer created by scans, imports, carrier APIs and status mappings.

### 3.6 Receipt-confirmation state

Escrow makes “receipt” a particularly dangerous ambiguous term.

Possible distinct states:

```text
carrier says delivered
recipient has parcel
buyer account sees delivered
buyer opens parcel
buyer judges item acceptable
buyer manually confirms receipt
platform auto-confirms after timeout
seller receives funds
```

A historical platform record saying “交易成功” can therefore hide several different physical histories.

### 3.7 Return/refund/dispute state

Minimum reverse-flow model:

```text
buyer requests refund
!= seller agrees
!= platform accepts dispute
!= return address valid
!= parcel returned
!= seller receives return
!= refund authorized
!= payment rail posts refund
!= buyer balance/bank actually credited
```

A surviving “七天退换” or consumer-protection page proves a rule/promise, not a successful historical refund for any user.

## 4. 2003–2005: marketplace visibility appears before the whole transaction becomes archive-visible

Taobao's public host `www.taobao.com` is a period-correct historical locator. Contemporary 2005 reporting also explicitly records `www.alipay.com` as the payment service host.

The strongest period evidence in this slice is not a Wayback capture but contemporaneous press describing the transaction logic:

- Alipay temporarily held funds until the buyer confirmed receipt;
- payment safety and after-sales uncertainty were already major consumer concerns;
- Taobao publicly promoted compensation mechanisms as a way to reduce stranger-transaction risk.

Sources:
- https://finance.sina.com.cn/roll/20050203/04301343972.shtml
- https://finance.sina.com.cn/roll/20050203/09561345274.shtml
- https://finance.sina.com.cn/roll/20050303/10081399921.shtml

This supports an architectural claim, not a DOM claim:

```text
public marketplace layer
+ payment/escrow layer
+ bank/payment rail
+ private buyer/seller state
+ later physical delivery
```

It does **not** yet prove:

- exact 2005 Taobao HTML structure;
- historical charset for a particular item page;
- exact JavaScript behavior;
- whether a specific browser/control was mandatory;
- the precise login/session flow;
- the DOM of an Alipay confirmation page.

Those remain UNKNOWN until a verified capture is opened.

## 5. 2008: one contemporary life history reveals the whole Web–parcel stack

A 2008 China News Service story about a Zhejiang University of Technology student (“小吴”) is unusually useful because it crosses both consumption and selling.

She described:

1. buying clothing on Taobao;
2. finding the size unsuitable after physical delivery;
3. relisting the unused item online;
4. successfully selling it a week later;
5. later using a relative's food-wholesale supply to open a shop;
6. building recurring customers in other regions;
7. contacting express-delivery companies to ship orders;
8. eventually treating the online shop as a post-graduation job path.

Source:
- 中国新闻网 / 今日早报 material, contemporaneous, 2008-04-15: https://business.sohu.com/20080415/n256305845.shtml

For archaeology, this single life history proves why a marketplace cannot be reconstructed only as “pages people browsed.” The actual cycle was:

```text
browse -> buy -> delivery -> inspect physical item -> relist -> new buyer
-> seller communication -> parcel shipment -> repeat customers
```

The physical object crossed the Web boundary twice.

It also creates a useful counterexample to simplistic claims that online selling eliminated work. The same report records failed/dormant student shops, the need to remain online to answer questions, sourcing problems, photography, copywriting, trust accumulation, packing and shipment.

## 6. Search/index state gaps

A historical search page is one of the least reproducible e-commerce artifacts.

Separate:

```text
query string
search backend/index at time T
seller/item eligibility at time T
ranking model at time T
paid promotion state
personalization/cookie/account state
returned result set
result order actually rendered
item clicked
```

A replayed HTML shell that contains a search box does not reconstruct any of the above.

Potential bias:

**catalog-shell survival / search-state loss asymmetry** — the visible interface survives better than the dynamic market that filled it.

## 7. Stock and price state gaps

For a product page:

```text
displayed product title
!= historical inventory quantity
!= specific SKU/variant available
!= price buyer ultimately paid
!= shipping fee after destination selection
!= coupon/promotion state
```

A product capture may be historically genuine and still be insufficient to answer “could someone in county X buy this item that day?”

This is especially important when later archive replay strips AJAX/XHR responses, region selectors, stock APIs or scripts.

## 8. Identity: one transaction can involve several people

For ordinary-life reconstruction, preserve:

```text
account owner
!= payer
!= delivery-address owner
!= named recipient
!= person answering courier call
!= actual end user
!= person confirming receipt
```

Examples include:

- an adult child buys goods for parents in another province;
- a parent pays for a student's order;
- a dorm roommate signs for a parcel;
- an office front desk accepts delivery;
- a household account is operated by more than one family member.

Therefore an archived account/order record, even if available lawfully, must not be translated directly into a one-person consumption biography.

## 9. 2013–2015: platform scale makes logistics architecture unavoidable

Alibaba's 2014 F-1 says partner delivery companies handled about 5.0 billion packages generated by its China retail marketplaces in 2013 and describes a shared logistics information system. It also says 156 million packages were generated by the 2013 Singles Day promotion, compared with an average of about 13.7 million per day.

Source:
- https://www.sec.gov/Archives/edgar/data/1577552/000119312514184994/d709111df1.htm

This evidence is useful for architecture, but it is a company regulatory filing and must not be silently converted into a national household-use statistic.

For old-Web reconstruction it proves a structural point:

> by 2013–2014, the Chinese retail Web's visible product/order layer depended on a massive, partly external physical network whose state cannot be captured by crawling marketplace HTML.

The delivery layer had its own operators, personnel, sorting centers, station networks and databases. The “site” and the “service” were physically non-coextensive.

## 10. Geography state gap: `deliverable address != doorstep delivery`

Although this repository's main period ends around 2015, later evidence is useful to identify what historical captures cannot tell us. A 2019 Beijing Consumers Association field survey found rural orders that were accepted by e-commerce systems but delivered only to pickup points, village committees or township locations, in some cases many kilometers from the written address.

Source:
- https://it.people.com.cn/n1/2019/0417/c1009-31033676.html

Do not back-project the exact 2019 geography to 2008. The methodological value is narrower:

```text
platform accepted postal address
!= historical carrier served that address to the door
```

A product/order page rarely preserves the service-area table, local franchise behavior, phone call, secondary fee, or actual pickup distance that completed the transaction.

## 11. Archive asymmetries introduced by e-commerce

### 11.1 `catalog survival / inventory-state loss`

Item description and image may survive; historical SKU stock usually does not.

### 11.2 `public listing / private negotiation asymmetry`

Price, variant, shipping promise and condition may have been negotiated in 旺旺/IM; public crawls normally miss it.

### 11.3 `transaction-guidance survival / transaction-state loss`

Help pages explaining “how to pay” may survive while the buyer's actual payment/escrow state is private and mutable.

### 11.4 `payment-page survival / bank-state loss`

A payment page can survive even when the bank gateway, certificate, account balance, risk-control decision and settlement path are absent.

### 11.5 `item-page survival / parcel-state loss`

The page can be perfect while the tracking number, scans, courier calls and failed delivery attempts disappear.

### 11.6 `delivery-status / physical-possession ambiguity`

“已签收” is a logistics/database statement, not necessarily direct observation that the intended buyer personally received and inspected the object.

### 11.7 `rule survival / remedy-outcome loss`

Consumer-protection and refund rules survive more easily than the private dispute showing whether remedy actually worked.

### 11.8 `successful-store visibility / failed-store disappearance`

Long-lived stores and high-reputation sellers leave more traces. Student sellers and small shops that died quickly can disappear, biasing later reconstructions toward success.

### 11.9 `Web survival / courier-labor invisibility`

Pages preserve products and branding much better than sorting, packing, delivery walking/driving, village pickup labor and family receipt arrangements.

### 11.10 `historical-rendering loss / database-record survival`

A modern platform account may expose a very old order record in today's interface. That record can be evidence that a transaction record survived, but it is **not** a capture of the historical Web UI.

## 12. Candidate historical original hosts and locators

### High-confidence period hosts

- `http://www.taobao.com/` — Taobao marketplace host, period-correct from 2003 onward.
- `http://www.alipay.com/` — explicitly reported in 2005 contemporary press as the payment-service site.

### Candidate historical path lead

A later secondary article about viewing 2005-era sites points to a Wayback-rendered Taobao path resembling:

- `http://www.taobao.com/new.php`

Source/locator only:
- https://segmentfault.com/a/1190000023396971

This is **D-level locator evidence**, not a verified capture. The archive URL was not recovered and validated in this slice.

### Why no path is promoted to M1 yet

A valid M1 artifact for this topic should record at minimum:

1. original URL;
2. archive capture URL;
3. capture datetime;
4. replay/HTTP status;
5. `Content-Type` and charset evidence;
6. DOM/form targets or equivalent transaction-relevant structure;
7. scripts/CSS/subresources needed for rendering or transaction UI;
8. historical browser/OS assumptions where evidenced;
9. whether login/session is required;
10. whether dynamic item/stock/order/payment state is missing;
11. a second historical time point for change comparison.

Public Web searches in this slice identified historical original hosts and a secondary Wayback locator, but direct replay of a 2005 Taobao/Alipay transaction artifact was not successfully opened and validated. Therefore:

> **M1 verified historical Chinese e-commerce item/order/escrow capture: NOT ACHIEVED IN THIS SLICE.**

This statement does **not** mean “Wayback did not save it.” It only means the evidence contract was not met here.

## 13. Technical unknowns that must remain unknown

Do **not** fill the following from era stereotypes:

- exact historical charset of a given Taobao/Alipay page;
- whether a particular action required IE;
- whether a particular page used ActiveX;
- exact JavaScript framework/library;
- exact payment-control behavior;
- session-cookie schema;
- form method/action;
- precise order API endpoint;
- exact tracking API integration;
- historical TLS/browser compatibility.

Even if some of these were common in 2000s Chinese transactional sites, the repo requires artifact-level proof.

## 14. A useful reconstruction template for any historical transaction

When a future capture is found, record:

```text
[PUBLIC DISCOVERY]
host:
page type:
original URL:
capture datetime:
charset evidence:
item/store identity:
public price:
public stock indicator:

[CLIENT]
browser evidence:
OS evidence:
JS/CSS dependencies:
login required?:
security control/certificate evidence?:

[ACCOUNT/IDENTITY]
account role:
payer role:
recipient role:
name/phone/address fields present?:

[TRANSACTION]
cart/order state:
payment rail:
escrow state:
seller acceptance state:

[LOGISTICS]
carrier selectable/selected?:
tracking-number state:
tracking UI:
service-area evidence:
delivery-confirmation semantics:

[AFTER-SALES]
refund/return entry point:
reverse-logistics requirement:
refund settlement state:

[ARCHIVE LIMIT]
what is public and captured:
what is private:
what is dynamic:
what cannot be inferred:
```

## 15. Evidence ledger

| Claim | Evidence | Grade | Limits |
|---|---|---:|---|
| Alipay's 2005 public service model held buyer funds until receipt confirmation | contemporaneous press describing service; `www.alipay.com` named | B/A-adjacent architecture evidence | does not recover DOM or a user's private payment state |
| Online-shopping safety/after-sales were explicit period concerns | 2005 contemporary report citing then-current survey | B | survey provenance should be recovered before using precise percentages as national estimates |
| A 2008 student life history crossed buy → physical receipt → relist → sell → ship → full-time shop work | contemporaneous China News Service/Today Morning Express report | B | individual case, not prevalence estimate |
| Alibaba marketplace orders depended on independent third-party logistics providers and shared information systems | 2014 SEC F-1 | A/company filing | describes Alibaba ecosystem, not all Chinese e-commerce |
| 2013 Alibaba China retail marketplace orders generated ~5b partner-delivered packages; Singles Day generated 156m | 2014 SEC F-1 | A/company filing | company scope, not national household statistic |
| A platform-accepted rural address need not mean doorstep delivery | 2019 consumer-association field survey reported by Beijing Youth Daily/People.cn | B | later than core scope; used to expose state distinction, not back-project exact 2019 conditions |
| 2005 Taobao/Alipay complete historical transaction capture recovered | none | — | **NOT ACHIEVED** |

## 16. Privacy and research ethics

Transaction archaeology is unusually likely to expose ordinary people's personal data. Historical pages may contain names, phone numbers, addresses, buyer IDs, seller IDs, order IDs, tracking numbers or dispute details.

Repository rule for this topic:

- do not republish full private addresses or phone numbers merely because an old page exposed them;
- do not build person-level purchase histories from leaked/private transaction records;
- prefer interface/state reconstruction over identifying ordinary users;
- for contemporary first-person cases, quote/paraphrase only what is necessary to establish the life-path mechanism;
- distinguish a public seller/store identity from a private buyer transaction.

“Public once” does not mean “ethically necessary to re-amplify now.”

## 17. Cross-repo implication: what a Web archive systematically misses about ordinary life

The Life Horizons package asks when distant goods became part of a person's realistic option set. Old-Web archaeology supplies the corrective:

> A page showing that the product existed is only the beginning of the life-history claim.

To say “a student in 2008 could buy this from another province,” the strongest evidence chain would ideally connect:

```text
period listing/search evidence
+ period payment/escrow evidence
+ shipping capability
+ destination serviceability
+ recipient-side executability
+ after-sales possibility
```

Conversely, the absence of a surviving item page does not prove the goods were unavailable: transactions could have been discovered through forums, IM, offline contacts, phone orders or dead platform pages.

## 18. Next targets

1. Recover a **verified 2004–2006 Taobao public item/store/search capture** with full URL, datetime, charset, DOM, dependencies and second time point.
2. Recover a **verified 2004–2006 Alipay public payment/help capture**, carefully separating help/demo UI from authenticated transaction UI.
3. Locate contemporaneous Taobao 旺旺 client/help material and determine how item identity, seller identity and IM session were linked.
4. Find early public logistics-query pages or manuals showing when a buyer could directly query carrier status rather than phone the seller/carrier.
5. Recover 2008–2012 public after-sales/refund/help flows and distinguish policy text from authenticated dispute states.
6. Compare one failed/dormant small seller with a long-lived successful store to counter survival bias.
7. Build one two-time-point capture comparison around a transaction-related page rather than another homepage-only comparison.

## 19. Bottom line

The Chinese e-commerce old Web should not be reconstructed as a gallery of shopping pages.

Its historically meaningful architecture was already distributed across:

```text
public catalog/search
+ seller presence and private IM
+ account/session
+ bank/payment/escrow
+ order database
+ third-party logistics
+ delivery phone/address
+ confirmation
+ dispute/return/refund
```

The public Web is the layer most likely to survive. Ordinary life happened when all the other layers lined up long enough for a physical object to leave one place and become usable in another.

That difference — between **“the page existed”** and **“the thing arrived”** — is the central state gap this note adds to the repository.
