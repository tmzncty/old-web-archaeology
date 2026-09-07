# C2C marketplace listing, identity, escrow, reputation and transaction state gaps, 1999–2015

## Scope

This companion stays inside the repository's main scope: **Chinese Internet / old-Web systems, approximately 1999–2015**.

It is not a general history of e-commerce, and it does not treat Taobao, EachNet/eBay EachNet, Paipai, Alipay or Tenpay as stable single technical objects across all years. The research unit is the transaction surface and its observable states at a particular time.

The corresponding ordinary-life synthesis is maintained in `tmzncty/how-people-lived`:

- https://github.com/tmzncty/how-people-lived/blob/main/topics/from-old-goods-to-platform-selling-c2c-escrow-reputation-and-light-entrepreneurship-china-1987-2026.zh-CN.md

The pre-1999 history of trust shops, flea markets, newspaper classifieds and other non-Web channels belongs primarily in that repository. It is used here only as a boundary condition: **online C2C did not invent personal resale; it changed how a private seller, a listing and an unknown buyer could become mutually addressable.**

---

## 1. Research unit: do not collapse page, user, seller, payment and transaction

For a C2C marketplace, at least the following objects must be separated:

- **platform / brand** — e.g. EachNet, Taobao, Paipai;
- **host** — e.g. `www.eachnet.com`, `www.taobao.com`, `www.paipai.com`;
- **account** — a persistent platform login or nickname;
- **seller certification state** — whether the platform accepts the account as eligible to sell;
- **item listing** — one product record, with title, description, price, images and validity period;
- **storefront** — a seller-facing public aggregation of listings;
- **order / bid** — an expressed transaction commitment;
- **payment object** — bank/payment-platform transaction;
- **escrow object** — money held by a third party pending delivery/acceptance;
- **shipment** — logistics record;
- **receipt / confirmation** — buyer-side acceptance state;
- **feedback / reputation** — platform-generated record after a transaction;
- **dispute / return** — a post-order state that may reopen an apparently completed transaction;
- **archive capture** — a historical representation of one public surface, not the underlying live state machine.

A historical shop page can survive while the payment, private chat, logistics, dispute record and even the account database have vanished.

---

## 2. Minimal transaction state machine

A reasonable working model for early Chinese C2C systems is:

```text
account created
→ identity / seller certification
→ listing drafted
→ listing published
→ listing indexed / searchable
→ buyer discovers listing
→ inquiry / chat
→ bid or order committed
→ buyer payment initiated
→ bank/payment platform accepts money
→ escrow/payment status reflected to marketplace
→ seller ships
→ carrier accepts parcel
→ carrier delivers
→ buyer confirms / timeout / dispute
→ escrow releases money
→ seller balance becomes available
→ withdrawal / settlement
→ feedback created
→ seller reputation recalculated
→ after-sales / return / dispute may still reopen the case
```

This is a **research state machine**, not a claim that every platform or year used exactly this implementation.

Its purpose is to prevent archive evidence from collapsing several statuses into one sentence such as “the item was sold.”

---

## 3. Historical hosts and brand boundaries

Useful historical locators confirmed by contemporary material include:

- `www.eachnet.com` — EachNet / later eBay EachNet;
- `www.taobao.com` — Taobao;
- `www.alipay.com` — Alipay, formally launched as a separate site in February 2005;
- `www.paipai.com` — Paipai.

These locators are **not verified archive captures in this slice**.

The METHOD rule applies strictly:

> same brand ≠ same host ≠ same codebase ≠ same database ≠ same user experience across years.

A 2003 Taobao item page, a 2006 Taobao seller center and a 2013 Taobao shop page should not be treated as one technical system merely because the host label remains familiar.

---

## 4. 1999–2004: listing visibility and market radius

Contemporary 2002 reporting described EachNet as founded in Shanghai in August 1999 and already offering auctions, buy-it-now and fixed-price transactions for individuals and merchants. Company-reported scale figures were large enough to show that individual C2C listing was no longer merely experimental.

A 2004 Reuters/China Daily interview with an eBay EachNet manager estimated that, around the site's early period, about 95% of physical exchanges were completed face-to-face, while by 2004 more than 70% of transactions were between users in different cities.

These are company estimates, not population measurements. They nevertheless support a useful narrow claim:

> the public listing could become geographically remote before the physical object moved.

That gives the first major state distinction:

### `listing-reach / delivery-reach gap`

A listing can be visible nationwide while practical delivery, payment or dispute resolution remains local, expensive or uncertain.

---

## 5. 2003–2005: low-cost listing does not mean low-cost transaction

Taobao's early competition emphasized free listing and transaction services. This reduced the fixed monetary cost of testing whether a product could find a buyer.

But the disappearance of a per-listing fee does **not** imply that the seller performed no labor.

A 2005 newspaper-republished seller tutorial, written under the Taobao username “猪脑子塞了”, gives a rare near-operational snapshot of what a novice seller actually had to do at the time.

The tutorial described:

- registering a member name and password;
- becoming an Alipay member;
- uploading an identity document for certification;
- using a digital camera, scanner or fax to submit the identity image;
- waiting roughly three working days for certification;
- maintaining at least ten active items before opening a shop;
- photographing products and editing images;
- writing titles with search keywords;
- constructing descriptions with fonts, tables and other page-formatting devices;
- choosing seven- or fourteen-day listing validity periods;
- designing shop logos, announcements, forum avatars and signatures;
- waiting for the Alipay payment notice before shipping;
- handling returns and after-sales communication.

This is **B-grade contemporary user-operation evidence**, not a historical Taobao HTML capture.

It proves that the lived seller workflow included much more than “click publish.” It does **not** prove the exact historical DOM, charset, CSS, browser requirement or backend implementation.

### Old-Web morphology implied by the tutorial

The material does allow narrow claims about the public presentation culture of the time:

- titles were written for marketplace search;
- item descriptions could use visible text formatting and tables;
- shops had logo/announcement-like presentation surfaces;
- seller promotion crossed between marketplace listings and community/forum identity surfaces;
- listing lifetime itself was a transaction-relevant field.

The exact HTML and rendering environment remain unknown until a verified capture is inspected.

---

## 6. Identity is layered, not binary

Early C2C transactions could involve several different identities at once:

```text
public nickname
≠ person operating the keyboard
≠ person whose ID passed seller certification
≠ payment-account legal identity
≠ bank-account holder
≠ parcel sender / recipient name
≠ formally registered business operator
```

A 2009 contemporary feature on teenage online sellers records a sixteen-year-old who could not independently register adult online banking / shop functions and therefore used her mother's identity and bank card.

This creates:

### `account-operator / legal-identity gap`

The person maintaining the shop, chatting with buyers and choosing stock can differ from the legal identity recognized by payment and certification systems.

### `seller-certified / business-registered gap`

Platform permission to sell does not automatically mean the seller has crossed the administrative boundary into a formally registered business.

Beijing's 2008 rules are useful here because they explicitly distinguished a private person disposing/exchanging personal-use goods without profit from profit-seeking online operation that fell under business-registration requirements.

The boundary between “consumer clearing an old item,” “occasional seller,” “side business” and “formal operator” is therefore a historical state transition, not a label that can be inferred from the existence of a shop page.

---

## 7. Escrow: buyer-paid is not seller-paid

In February 2005, contemporary reporting described the newly formalized `www.alipay.com` escrow mechanism in straightforward terms: the buyer's money was held by Alipay until the buyer confirmed receipt, after which it was released toward the seller.

This produces several state gaps that must never be collapsed:

### `payment-initiated / bank-accepted gap`

The buyer clicks pay, but the bank or payment provider may still reject, time out or fail.

### `bank-debited / escrow-credited gap`

A bank-side debit does not by itself prove the marketplace ledger has reconciled successfully.

### `escrow-held / seller-paid gap`

The buyer has committed money, but the seller does not yet have final control over it.

### `seller-balance / withdrawn-cash gap`

A platform balance may still depend on bank binding, withdrawal rules, verification or later risk control.

This temporal split is one of the central technical changes that made stranger trade more executable: neither party has to trust the other with the whole transaction state at once.

But the archive consequence is severe. A preserved item page usually contains none of these money states.

---

## 8. Shipping states: “seller says shipped” is not delivery

C2C systems increasingly connected marketplace records with logistics information, but the following states remain distinct:

```text
seller marks shipped
≠ parcel physically handed to carrier
≠ carrier scan accepted
≠ parcel moving correctly
≠ delivered to correct location
≠ correct buyer actually received item
≠ buyer accepts item as described
```

The state distinction is essential even if the surviving historical page displays “已发货” or “交易成功”.

A page label is an observable platform state. It is not automatically a reconstruction of the physical history of the object.

---

## 9. Reputation: a database signal, not a universal character certificate

By 2006 Taobao was separating buyer and seller credit displays rather than showing one undifferentiated score. Contemporary reporting records users noticing that the change could alter the visible level associated with a shop and affect business.

This shows:

### `buyer-credit / seller-credit gap`

A person can behave differently, and be evaluated differently, in buyer and seller roles.

Contemporary 2006 reporting also documented services that manufactured seller credit by simulating a full transaction loop: list an item, buy it, “ship,” confirm receipt, give a positive rating, then return the money minus a service fee.

This gives one of the most important old-Web transaction gaps:

### `transaction-complete / economic-substance gap`

A platform state machine can be syntactically complete even when no meaningful commodity exchange occurred.

Therefore:

### `feedback / truth gap`

A positive feedback record proves that the platform stored that feedback event. It does not alone prove product quality, shipment authenticity or honest economic exchange.

### `reputation / portable-identity gap`

Seller reputation is platform-local capital. It depends on the platform's rules, scoring model and continued existence.

The later 2022 closure of EachNet illustrates the preservation consequence: trading, shop functions, login and other services were shut down, and users were advised to inspect old transaction records and withdraw remaining balances before closure.

The 2022 event lies outside this repo's main old-Web period and is cited only to explain **why platform-local reputation and transaction memory can disappear later**.

---

## 10. Searchability and attention are separate states

A listing can be published and still effectively invisible.

The transaction discovery chain should therefore be split:

```text
listing drafted
→ published
→ accepted by platform
→ indexed
→ eligible for query/recommendation
→ actually displayed
→ actually noticed
→ clicked
→ inquiry/order
```

The 2005 seller tutorial already advised sellers to write searchable titles and promote themselves in forum signatures. A 2009 student-seller profile provides the complementary lived result: the seller had invested family money and kept a Taobao shop for nearly a year, but daily traffic was at one point around two visitors and only eleven clothing items sold; attention increased only after a community post drew notice.

This produces:

### `market-entry / attention gap`

The Web can make entry cheap while making visibility the next scarce resource.

For old-Web archaeology, a surviving listing page proves **publication**, not that ordinary users ever encountered it in meaningful numbers.

---

## 11. Shop page / household labor gap

The public page tends to make one seller account look like one economic actor.

Contemporary 2009 profiles complicate that picture:

- one young seller used her mother's home and former bedroom as inventory space;
- another side-business seller relied on parents to help obtain stock and send parcels;
- photography, editing, customer response and packaging occurred inside domestic time and space.

Thus:

### `account / labor-unit gap`

One account can represent a small household labor collective.

### `storefront / physical-infrastructure gap`

A shop page may look “virtual” while the business still depends on bedrooms, tables, storage, bicycles, postal counters or courier pickup.

The Web page hides much of that infrastructure.

---

## 12. Paipai and identity layering: membership can be automatic while selling is not

Contemporary 2005 reporting on Paipai described a useful layered model: QQ users could already participate as marketplace members/buyers, while selling required additional seller certification; Tenpay served as the third-party payment layer.

This illustrates:

### `platform-membership / seller-authority gap`

A pre-existing social/IM identity can lower the cost of entering a marketplace without automatically granting money-moving or seller privileges.

### `chat-identity / transaction-identity gap`

The account used for conversation and discovery need not be the final legal/payment identity used for settlement.

This matters for archive reconstruction because public nicknames are often much easier to preserve than the private authentication relationship behind them.

---

## 13. Core state-gap catalogue

For future captures, screenshots or manuals, use the following distinctions explicitly:

```text
account created                ≠ legal person verified
account operator               ≠ certified ID holder
platform member                ≠ seller-authorized account
seller-certified               ≠ formally registered business
listing drafted                ≠ listing published
listing published              ≠ listing indexed
listing indexed                ≠ listing displayed to a user
listing displayed              ≠ item actually available
inquiry/chat                   ≠ binding order
bid/order committed            ≠ payment initiated
payment initiated              ≠ bank accepted
bank debited                   ≠ escrow credited
escrow credited                ≠ seller can use money
seller marks shipped           ≠ carrier accepted parcel
carrier delivered              ≠ buyer actually accepted goods
buyer confirmed                ≠ transaction economically genuine
transaction complete           ≠ no later return/dispute
positive feedback              ≠ objective truth
seller reputation              ≠ portable reputation elsewhere
public shop account            ≠ one-person labor unit
store page                     ≠ physical inventory/warehouse state
historical HTML                ≠ live transaction backend
same brand                     ≠ same implementation across years
```

These are the principal old-Web conclusions of this slice.

---

## 14. What survives, and what usually disappears

### Relatively archive-friendly

- shop home pages;
- item titles and descriptions;
- public images, when subresources were captured;
- seller nicknames;
- public credit/reputation indicators;
- category pages;
- help pages;
- platform announcements;
- some public feedback.

### Archive-hostile / transaction dark matter

- private WangWang/QQ negotiations;
- identity-document uploads;
- bank authentication;
- payment callbacks;
- escrow reconciliation;
- risk-control events;
- private addresses and phone numbers;
- courier pickup details;
- failed orders;
- cancelled orders;
- refunds and disputes;
- domestic packing labor;
- attempts by sellers who listed once and quit;
- reputation computation internals.

This creates an important historical visibility bias:

> **the old Web preserves “things that were displayed” much better than “transactions that were successfully executed.”**

A future historian who counts surviving listings may badly overestimate successful trade.

---

## 15. Privacy and redistribution boundary

C2C archaeology can easily expose ordinary people's:

- old phone numbers;
- home addresses;
- ID information;
- bank/payment traces;
- legal names;
- private chat;
- long-abandoned seller identities.

Even if an archive technically exposes these fields, this repository should prefer:

- URL patterns;
- field schemas;
- public help/tutorial pages;
- anonymized transaction-state examples;
- minimal screenshots needed to support a technical claim;
- metadata and analysis rather than republishing personal records.

Do not recreate a long-dead ordinary user's transactional dossier merely because pieces survive.

---

## 16. Evidence used in this slice

Evidence grading follows `docs/METHOD.md`.

### B — contemporary reporting / user operation material

- Sina Tech, 2002-03-18, contemporary report on EachNet scale and transaction forms: https://tech.sina.com.cn/i/c/2002-03-18/107177.shtml
- China Daily / Reuters, 2004-09-17, `EBay's China site to join global network`: https://www.chinadaily.com.cn/english/doc/2004-09/17/content_375458.htm
- 文汇报/新浪, 2003-07-08, early Taobao report: https://tech.sina.com.cn/i/c/2003-07-08/1244206917.shtml
- China Daily, 2005-05-09, C2C listing/transaction-fee competition: https://www.chinadaily.com.cn/english/doc/2005-05/09/content_440384.htm
- 人民网-江南时报/新浪财经, 2005-02-03, Alipay escrow mechanism and `www.alipay.com`: https://finance.sina.com.cn/roll/20050203/04301343972.shtml
- 金陵晚报/新浪, 2005-07-19, contemporary Taobao seller tutorial: https://news.sina.com.cn/s/2005-07-19/09006474272s.shtml
- contemporary 2005 Paipai reporting, membership/seller-certification/Tenpay model (located in this research slice; exact archived page still to be captured)
- 东方网/新浪, 2006-01-23, buyer/seller credit separation: https://news.sina.com.cn/o/2006-01-23/08358056859s.shtml
- 上海青年报/新浪, 2006-10-31, manufactured seller-credit transactions: https://news.sina.com.cn/c/2006-10-31/085010367546s.shtml
- 北京晨报/新浪, 2008-07-03, distinction between non-profit disposal of personal goods and profit-seeking online business registration: https://news.sina.com.cn/s/2008-07-03/200314112007s.shtml
- 南都周刊/新浪, 2009-06-23, teenage/student seller cases including identity proxy and low-traffic shop: https://news.sina.com.cn/s/2009-06-23/144618077473_6.shtml
- 中国新闻网转《联合早报》/新浪, 2009-09-01, side-business/full-time seller and household support cases: https://news.sina.com.cn/o/2009-09-01/164716222022s.shtml

### Later evidence used only for preservation consequence

- 2022 EachNet closure announcement as contemporaneously reported: https://finance.sina.com.cn/tech/internet/2022-07-23/doc-imizmscv3212476.shtml

This source lies outside 1995–2015 and does **not** extend the repository's object scope. It is used only to explain how platform-local transaction/reputation records later become inaccessible.

---

## 17. Archive / browser / encoding status

### M1 status: **NOT ACHIEVED IN THIS SLICE**

This run identified historical hosts and detailed contemporary operating evidence, but it did **not** successfully open and inspect a qualifying Wayback/WARC replay for the relevant 1999–2010 marketplace pages.

Therefore the following remain `unknown` rather than inferred:

- historical HTTP headers;
- charset and Content-Type of target pages;
- exact DOM / frames / table structure;
- CSS and JavaScript behavior;
- browser sniffing or IE-specific code;
- cookies and session behavior;
- exact login / seller-certification endpoint flow;
- exact dynamic search and ranking requests;
- payment callback implementation;
- escrow reconciliation protocol;
- historical error pages;
- image/subresource completeness;
- whether a candidate archive page can actually execute any stateful action in replay.

The correct negative claim is:

> **No verified historical replay was obtained in this slice.**

It is **not**:

> “Wayback has no captures.”

A historical locator is not a verified capture under this repository's METHOD contract.

---

## 18. Next bounded archaeology targets

1. Obtain and inspect at least two captures of one public Taobao/EachNet item or help-page surface from different dates.
2. Capture a contemporary help/manual page that defines seller certification and compare it to the newspaper user tutorial.
3. Recover evidence for exact historical `charset`, browser assumptions and table/frames layout.
4. Find an archiveable public transaction-status explanation for “买家已付款 / 卖家已发货 / 交易成功 / 退款” and map labels to backend meaning.
5. Compare Taobao and Paipai identity layering: nickname, platform membership, seller certification, payment identity.
6. Track when marketplace chat moved among forum/private-message/QQ/WangWang-like channels and what portion remains archivally invisible.
7. Compare reputation rules before and after the 2006 buyer/seller credit split.
8. Document how platform shutdown or domain repurposing changes the recoverability of a seller's historical reputation.

---

## Slice conclusion

This slice adds a new old-Web object class to the repository: **the C2C transaction as a multi-system state machine rather than a static shop page.**

The central archaeological correction is:

> **A listing that survives is evidence that an item was displayed. It is not, by itself, evidence that an unknown buyer saw it, that money reconciled, that a parcel moved, that the buyer accepted it, or that the seller ever received spendable funds.**

Because this is a substantive new mechanism and evidence domain, the cross-project saturation counter remains **0**.
