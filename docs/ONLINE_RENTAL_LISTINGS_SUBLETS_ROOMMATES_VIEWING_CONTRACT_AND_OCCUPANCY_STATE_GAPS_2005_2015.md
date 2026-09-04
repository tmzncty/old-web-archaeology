# ONLINE_RENTAL_LISTINGS_SUBLETS_ROOMMATES_VIEWING_CONTRACT_AND_OCCUPANCY_STATE_GAPS_2005_2015.md

Status: methodology / research note  
Scope: Chinese Web rental and roommate-listing systems, approximately 2005–2015. Pre-Internet rental matching appears only as boundary context; post-2015 platform failures appear only where needed to explain why the historical state model matters.  
Cross-link: `tmzncty/how-people-lived/topics/renting-as-waiting-room-durable-adulthood-and-nonkin-households-china-1995-2025.zh-CN.md`

This note asks a narrow old-Web archaeology question:

> **What does an archived rental listing prove — and which states between “page exists” and “someone actually lives there” remain invisible?**

The answer is more complicated than a classifieds page.

A rental system joins at least three histories:

1. Web publication and search;
2. a physical property and people claiming authority over it;
3. an offline tenancy whose decisive states are usually private and therefore poorly archived.

---

## 1. Keep the research units separate

Do not collapse the following into a single object:

- **platform** — e.g. a classified-information or SNS service;
- **host / site** — one historical hostname;
- **listing page** — one public rental/sublet/roommate advertisement;
- **poster account** — the account or identity that created the listing;
- **poster role** — landlord, agent, existing tenant, subletter, roommate seeker, unknown;
- **property** — the physical dwelling allegedly represented;
- **room / bed** — the specific occupiable unit;
- **prospective tenant** — person seeking housing;
- **prospective roommate** — person seeking a co-occupant rather than only a property;
- **contact channel** — phone, QQ, platform message, email, SMS or other;
- **viewing** — physical inspection event;
- **contract** — private legal/administrative artifact;
- **payment** — deposit/rent transfer state;
- **occupancy** — actual physical possession/use;
- **renewal / termination** — later tenancy state;
- **archive capture** — a historical representation of some public Web artifact;
- **claim** — the narrow proposition supported by the evidence.

A listing URL is not a tenancy identifier.

---

## 2. Full state machine

A useful minimum rental route is:

```text
housing need
-> listing created
-> listing indexed
-> listing visible at some rank
-> prospective tenant sees it
-> poster contacted
-> poster responds
-> vacancy still exists
-> viewing arranged
-> physical viewing occurs
-> poster authority / property facts judged acceptable
-> rent / deposit / roommate terms negotiated
-> contract or informal agreement reached
-> deposit / initial payment made
-> key / access handed over
-> occupancy begins
-> recurring rent / repairs / roommate rules continue
-> renewal OR termination
-> move-out
-> deposit return / dispute / unresolved balance
```

For shared housing add:

```text
roommate profile / description
-> mutual contact
-> compatibility screening
-> consent of existing occupants / landlord where required
-> co-residence
```

A public Web archive usually preserves only a small prefix of this chain.

---

## 3. Core state gaps

### listing-publication gap

A draft or submitted listing may not have been publicly visible.

### listing-freshness gap

A preserved listing can remain online after the room has already been rented, withdrawn or materially changed.

### poster-role gap

An account can be categorized as an individual, agent or other poster without proving the real-world relationship to the property.

### property-entitlement gap

The poster may not own the property or possess valid authority to sublet it.

### discoverability / ranking gap

A listing can exist in the database but be difficult to find because of ranking, filters, paid placement or high posting volume.

### contact-reachability gap

A visible phone/QQ/message channel does not prove the poster still answers.

### viewing-state gap

Contact does not prove a viewing was scheduled or completed.

### representation-to-room gap

Text and images do not prove that the physical room matched the listing.

### roommate-consent gap

A room may exist without all co-occupants agreeing to a new roommate.

### deposit-state gap

A person may have agreed verbally but not paid, paid but not received access, or paid into a dispute.

### contract-state gap

A contract may be proposed, signed, invalid, incomplete or privately retained; it is normally not recoverable from public Web archives.

### occupancy-state gap

Even a signed contract does not by itself establish that the tenant actually moved in.

### renewal-state gap

The archived listing says almost nothing about whether the tenancy survived the first term.

### deposit-return gap

The tenancy can end successfully while the financial closure remains disputed.

### deletion-meaning gap

A disappeared listing can mean:

- rented successfully;
- expired;
- manually deleted;
- removed by moderation;
- duplicate;
- fraudulent or suspected fraudulent;
- account deleted;
- URL scheme changed;
- archive simply missed it.

Therefore:

```text
listing disappeared != tenancy succeeded
```

---

# 4. Boundary context: matching existed before the Web

A 1995 contemporary report on Beijing's rental market described rental notices pasted in residential districts, on utility poles, under overpasses and at bus stops, alongside informal intermediaries operating with telephone access and minimal offices.

Locator used in the life-history companion note:

- 《参考消息》数字档案，1995-12-24: <https://ckxxapp.ckxx.net/pages/1995/12/24/05/>

This is outside the repository's main Web period and should remain contextual.

It demonstrates why the correct claim is not:

> the Web invented rental classifieds.

The Web inherited an existing matching function and changed its search, timing, ranking and archival properties.

---

# 5. Early Chinese-Web observable use: rental and roommate posts

## 5.1 Forum and university-board evidence

Search in this research cycle located public forum/BBS-style traces from the mid-2000s that include rental and `求合租` / shared-housing posts.

Examples include:

- Beijing-oriented forum pages with rental / roommate posts from 2006;
- university forum traces with `房屋租赁` / `求合租` in 2008.

These are useful as **platform-observable contemporaneous evidence** that housing and roommate matching occurred through ordinary Web community spaces, not only dedicated property portals.

Do not infer from them:

- platform market share;
- successful lease outcome;
- poster identity accuracy;
- population prevalence.

## 5.2 Douban as a social screening layer

A Douban note dated 2009-12-18 was located in which a user helped a female friend seek a compatible female roommate.

Use this only at the structural level.

Privacy rule:

- do not reproduce historical username, phone, QQ, exact home address or other unnecessary personal information;
- preserve the platform/date/function claim, not a redistributable dossier on the ordinary user.

The important old-Web point is that an SNS identity could help solve a different problem from a pure property listing:

```text
Who has a room?
```

and

```text
Who might be livable as a roommate?
```

are separate searches.

---

# 6. 2010 evidence: Web supply can be abundant and still operationally stale

A July 15, 2010 China Youth Daily report on young renters described multiple search channels coexisting. In a multi-response survey, respondents reported using friends/acquaintances, agencies, rental websites and community paper notices.

Source:

- <https://zqb.cyol.com/html/2010-07/15/nw.D110000zgqnb_20100715_1-07.htm>

The same report follows a graduate seeking shared housing with classmates who found many online listings already rented or controlled by intermediaries and viewed more than twenty units without securing a tenancy.

This is unusually strong evidence for a Web archaeology boundary:

> **a live listing page can already be a stale representation of the offline market.**

Thus an archive capture at `T+1 day` can preserve the HTML perfectly while preserving the housing state poorly.

### Minimum temporal fields for rental-listing evidence

When possible record:

```yaml
listing_posted_at:
listing_updated_at:
capture_datetime:
observed_available_at:
observed_rented_at:
observed_deleted_at:
```

Usually only the first three are recoverable.

Do not silently fill the others.

---

# 7. 58.com 2013 F-1/A: the listing system becomes recoverable as a platform state model

The October 28, 2013 58.com F-1/A filed with the U.S. Securities and Exchange Commission is A-grade primary evidence for the company's stated system structure at that time.

Source:

- 58.com Inc., F-1/A, filed 2013-10-28: <https://www.sec.gov/Archives/edgar/data/1525494/000104746913009985/a2217137zf-1a.htm>

As with any company filing, this establishes what the company formally represented to investors; it does not automatically prove every listing was accurate or every user experienced the platform as described.

---

## 7.1 Housing was already a structured category, not a flat message board

The filing states that housing was divided into sub-groups including:

- residential leasing;
- sub-leasing;
- secondary property sale;
- office-space leasing;
- retail-space leasing;
- factory / industrial real-estate leasing.

It further states that the platform distinguished listings uploaded by individuals from those uploaded by real-estate agents and provided tools to protect private contact information for individual users who preferred contact from individuals rather than agents.

The filing also describes search parameters in housing such as:

- price range;
- size;
- number of bedrooms;
- information source, including individuals and agents.

This yields a historical transition:

```text
paper / free-text notice
-> searchable structured local database
```

But retain the boundary:

```text
platform source_type = individual
!=
verified property owner
```

A classification field is not a title search.

---

## 7.2 Individual / agent is a platform state, not a complete identity proof

The platform's distinction is historically important because users explicitly cared about whether a listing came from an individual or agent.

But an old-Web researcher must not translate:

```text
individual
```

into:

```text
landlord
```

without independent evidence.

Possible real-world roles include:

- owner-landlord;
- family member of owner;
- existing tenant seeking roommate;
- authorized subletter;
- unauthorized subletter;
- intermediary posing as individual;
- stale account / reused listing;
- unknown.

Therefore store `poster_role_claimed` separately from `poster_role_verified`.

---

# 8. Discoverability was already monetized

The same filing describes online marketing services including:

- real-time bidding;
- priority listing.

It says merchants could bid for prominent placement within categories and locations, while priority listings were placed below real-time-bidding listings and above ordinary paying-member listings.

The company states that trial operation of real-time bidding began in selected categories/locations in the third quarter of 2012 and that nationwide launch occurred in the first quarter of 2013.

This matters archaeologically because a page list is not a neutral cross-section of supply.

By this period:

```text
listing exists
!=
listing appears prominently
```

and:

```text
search-result order
can contain commercial state
```

### New field recommendation

```yaml
placement_state:
  organic: unknown
  merchant_member: unknown
  priority_listing: unknown
  realtime_bid: unknown
  other_paid_placement: unknown
```

Unless the capture or platform metadata establishes placement state, leave it unknown.

Do not infer popularity from top position.

---

# 9. Real-time indexing narrows one delay but not the offline gap

58.com stated in the filing that newly posted data were typically searchable within about three seconds.

This is useful A-grade evidence about the company's claimed indexing objective/system behavior in 2013.

It does **not** mean the represented room was still vacant three seconds later, or that duplicate/stale/fraudulent supply disappeared.

The correct decomposition is:

```text
publication latency
search-index latency
market-state latency
```

These are different clocks.

A fast index can make a stale or false statement discoverable faster.

---

# 10. Mobile transition changes the temporal geography of rental search

The 2013 filing states that 58.com offered three forms of mobile access:

1. downloadable Android / iOS applications;
2. browser-adapted applications for smartphone browsers;
3. WAP applications for feature phones.

It describes location/category selection and listing results, and elsewhere describes real-time merchant/user communication in mobile applications.

This supports a narrow system claim:

> by 2013, rental/classified search could be integrated into mobile access modes rather than requiring a desktop session.

It does not establish:

- what proportion of rental seekers used each mode;
- exact 2006/2009 WAP HTML;
- device/browser compatibility for a specific historical user;
- whether every desktop field/function existed in each mobile mode.

### Archaeological implication

A housing-search session can now move with the person:

```text
see listing on commute
-> call / message immediately
-> travel to viewing
-> continue searching between viewings
```

This can make listing freshness more consequential, not less.

---

# 11. A local real-estate agency example shows channel migration, not complete replacement

58.com's filing gives an internal merchant example of a suburban Beijing real-estate agency that began using 58.com through paid membership in 2011 after relying primarily on flyers, exhibition booths and free online marketing channels.

The filing says the agency began receiving responses to listings, often on the same day, and later made the platform a principal marketing channel.

This company-provided example is not an independent effectiveness study.

Its historical value is the **channel stack**:

```text
flyers
+ booths
+ free online channels
+ paid classified platform
```

Old and new discovery infrastructures coexist.

---

# 12. Suggested rental-listing evidence schema

```yaml
platform:
host:
listing_url:
archive_source:
capture_url:
capture_datetime:
original_url:

listing:
  posted_at:
  updated_at:
  category:
  subcategory: residential_lease|sublease|roommate|unknown
  city:
  district:
  price_claim:
  deposit_claim:
  room_count_claim:
  area_claim:
  image_count:
  source_type_claim: individual|agent|unknown

poster:
  account_id_retained: false
  claimed_role:
  verified_role: unknown
  contact_method_types: []
  contact_details_redacted: true

platform_state:
  indexed: unknown
  rank_position:
  placement_state: unknown
  paid_visibility: unknown
  moderation_state: unknown

physical_state:
  still_available_at_capture: unknown
  viewing_arranged: unknown
  viewing_completed: unknown
  property_matches_listing: unknown
  poster_authorized: unknown

agreement_state:
  terms_agreed: unknown
  deposit_paid: unknown
  contract_signed: unknown
  key_handoff: unknown
  occupancy_started: unknown
  renewal: unknown
  deposit_returned: unknown

roommate_state:
  roommate_search: false
  compatibility_screening_observed: unknown
  existing_occupants_consented: unknown

claim_supported:
claim_not_supported:
evidence_grade:
unknowns:
```

Do not populate private real-person fields merely because an old page exposes them.

---

# 13. Claim templates

### Good

> A 2009 Douban post shows the platform being used to seek a roommate.

### Bad

> Douban became a major Chinese rental platform in 2009.

---

### Good

> 58.com's 2013 SEC filing states that its housing category distinguished residential leasing and sub-leasing, and listings from individuals and real-estate agents.

### Bad

> 58 verified whether every “individual” rental listing came from the owner.

---

### Good

> Contemporary 2010 reporting documents rental seekers encountering listings that had already been rented.

### Bad

> Most 2010 online rental listings were fake or stale.

---

### Good

> By 2012–2013, 58.com offered paid priority/real-time-bid placement that could affect listing prominence.

### Bad

> The highest historical search result was the most popular or best apartment.

---

# 14. Roommate matching requires a separate social-state model

A roommate listing is not only a housing object.

The actual object can be:

```text
person A
+ current tenancy
+ one empty bed/room
+ desired person type
+ household norms
+ landlord / co-tenant permission
```

Relevant states include:

- current tenant is authorized to add someone;
- room is actually empty;
- rent split is accepted;
- deposit split is accepted;
- gender preference;
- work / sleep schedule;
- smoking / pets;
- visitor rules;
- cleaning expectations;
- duration;
- moving date;
- identity trust.

An archive can preserve the desired roommate profile while completely losing whether two strangers ever co-resided.

This is a particularly strong example of:

> **public Web visibility is inverse to lived outcome visibility.**

The advertisement survives; the household does not.

---

# 15. Physical viewing remains a hard boundary

The 2021 post-scope evidence in the companion life-history note is used only to illustrate why this state separation matters: renters still reported online descriptions differing from real properties and emphasized the importance of physical viewing.

For this repository's 2005–2015 scope, do not back-project later platform UI or fraud patterns into an earlier year without evidence.

The general state rule is timeless enough to retain:

```text
screen representation != physical inspection
```

but the prevalence and mechanism of mismatch must be period-specific.

---

# 16. Contract and occupancy are systematically under-archived

Public Web archives are structurally biased toward:

- listing title;
- advertised price;
- photographs;
- neighborhood claims;
- poster category;
- visible contact UI;
- search/category pages.

They are structurally weak for:

- negotiated final rent;
- deposit receipt;
- identity / ownership documents;
- signed contract;
- key handoff;
- roommate agreement;
- repair requests;
- landlord messages;
- eviction notices;
- renewal negotiation;
- deposit return.

This is not just an archive failure.

Many of these artifacts are correctly private.

Therefore the project should not attempt to “complete” a tenancy by deanonymizing an old poster or correlating historical phone numbers with current accounts.

---

# 17. Later long-rental-platform failure as a boundary lesson, not a scope expansion

The 2020 DanKe crisis lies outside this repository's main period, so it belongs primarily in `how-people-lived`.

It is useful here only as a conceptual stress test:

```text
tenant paid intermediary
!=
landlord received rent
```

and:

```text
private contract exists
!=
occupancy remains executable
```

Do not turn this note into a history of post-2015 long-rental apps.

Its value is to show why the state machine must not stop at `contract_signed`.

---

# 18. Archive and browser boundaries

This research cycle did **not** verify a complete historical 2005–2011 rental transaction path from:

```text
search results
-> listing page
-> contact
-> viewing
-> contract
-> occupancy
```

Nor did it verify a complete historical authenticated user session on 58.com or Ganji for this purpose.

Therefore this note does **not** claim:

- exact historical DOM/CSS for a 2006 rental listing;
- exact charset for a specific unverified page;
- exact IE/browser requirements;
- exact WAP field parity;
- exact contact-hiding implementation in earlier years;
- that a modern replay reproduces the historical user experience.

The 2013 SEC filing gives strong system-description evidence but is not a Web capture of every earlier version.

“Not yet verified” is the correct result.

---

# 19. Privacy rules for rental archaeology

Rental archives are unusually sensitive because an old listing may combine:

- precise home address;
- phone number;
- QQ / email;
- sex / age / occupation preferences;
- photographs of private interiors;
- roommate identity details;
- move dates;
- daily schedule clues.

Default handling:

- preserve URL/capture metadata where legitimate;
- redact ordinary-person contact details from research notes;
- abstract address to district/neighborhood unless exact location is indispensable;
- do not attempt to contact historical posters;
- do not cross-match old phone/QQ/email against current identities;
- do not publish a dataset of ordinary historical renters/roommates;
- avoid redistributing copyrighted listing photographs.

The object is the platform and state transition, not the private person.

---

# 20. What old-Web rental pages can reveal especially well

Despite their limitations, rental listings can preserve things other records miss:

### search vocabulary

What categories existed — `整租`, `合租`, `求合租`, `转租`, `个人`, `中介` — and when platforms formalized them.

### housing segmentation

Which location, price, room count and size fields were expected to matter.

### platform intermediation

How individual / agent distinctions, privacy controls and ranking were encoded.

### mobile transition

When searching a city no longer required a fixed desktop session.

### information-market competition

How agents/merchants paid for visibility.

### social matching

How general forums/SNS became places to assemble households, not merely discuss housing.

These are legitimate old-Web archaeology questions even when the eventual lease is unknowable.

---

# 21. What this note adds to the repository's platform genealogy

Rental classifieds expose a useful intermediate platform form between hand-maintained classifieds and later transaction platforms.

A rough functional genealogy is:

```text
paper notice / newspaper classified
-> BBS / forum free-text post
-> structured classified database
-> category/filter/ranking system
-> mobile location-aware classified access
-> later platform-managed tenancy / payment systems
```

Do not interpret this as a universal linear replacement.

The 2010 evidence explicitly shows older channels continuing alongside Web listings.

The genealogy is about **which state the platform begins to own**, not simply which medium is newest.

A forum may own only the post.

A classified platform may own:

- indexing;
- filtering;
- poster type;
- paid placement;
- contact routing.

A later managed-rental platform may also own payment and service states.

That is a major difference in failure domain.

---

# 22. Suggested lineage edges

Potential future `platform-genealogy` edges, once the repository's dataset/schema work is ready:

```text
physical / newspaper rental classified
  -> BBS/forum housing post
  confidence: high as functional lineage, not direct product inheritance
```

```text
BBS/forum free-text rental post
  -> structured classified rental category
  confidence: medium-high functional lineage
```

```text
structured classified rental category
  -> mobile/WAP local rental search
  confidence: high for 58.com by 2013 filing
```

```text
organic listing order
  -> paid priority / bid-based discoverability
  confidence: high for 58.com 2012–2013 platform system
```

Do not claim direct technical code inheritance without source evidence.

---

# 23. Research gaps

1. Verify at least two real historical rental listing captures from different years between 2005 and 2011, with original URL, capture datetime and page/subresource status.
2. Recover a privacy-safe historical 58.com or Ganji category/search page and document exact source-type filters.
3. Verify a WAP/mobile rental page from before 2012 rather than relying only on later corporate description.
4. Determine when `个人` / `中介` / `合租` / `转租` became explicit structured fields on each major platform.
5. Compare one general BBS/SNS roommate workflow with one dedicated classified platform workflow.
6. Look for contemporary user tutorials describing the full path from listing search to phone call and viewing.
7. Search for contemporaneous reports on listing expiration/deletion behavior.
8. Determine whether platforms exposed `已租` / inactive states or merely removed listings in particular years.
9. Study archive survival bias between search-result pages, listing detail pages and contact information.
10. Add a copyright/privacy-safe reconstruction experiment only if enough original HTML/CSS/browser evidence is actually recovered.

---

# 24. Stop conditions for this object

Stop claiming more certainty when:

- only search-engine snippets remain;
- listing URLs are known but captures cannot be opened;
- private contact details are the only route to outcome verification;
- current platform pages would need to be back-projected into older years;
- poster role cannot be distinguished from property authority;
- a later fan/blog recollection is being used to infer exact old UI;
- archived image/text is insufficient to identify whether the page was listing, error page, expired page or redirect;
- transaction outcome requires accessing private messages/contracts.

A valid final archaeological conclusion may be:

> **the listing state is recoverable; the tenancy state is not.**

---

# 25. Main conclusion

Rental Web archaeology reveals an especially sharp version of the repository's general evidence problem:

> **The page most likely to survive is the page created before the important event happened.**

The historical listing tells us that a room, sublet or roommate was offered or sought.

The consequential life event — finding a person, seeing the room, paying the deposit, receiving the key, living together, moving again — happens mostly off-page.

Therefore the correct state boundary is:

```text
public listing history
!=
private housing history
```

and the correct research ambition is not to erase that gap, but to model it precisely.
