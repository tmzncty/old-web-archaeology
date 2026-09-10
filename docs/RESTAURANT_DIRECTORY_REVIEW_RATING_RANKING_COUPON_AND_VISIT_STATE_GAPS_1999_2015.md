# Restaurant directory / review / rating / ranking / coupon / visit state gaps（1999–2015）

> Status: research package / archaeology candidate.
>
> Scope: **约 1999–2015 中文互联网中的餐馆目录、城市生活指南、用户点评、评分、榜单、优惠券与从页面到实体到店之间的状态边界。**
>
> This is **not** another online-food-ordering history. The repository already has `ONLINE_FOOD_ORDERING_MENUS_SERVICE_AREAS_AND_DELIVERY_OUTCOME_GAPS_2004_2010.md`. That package studies ordering and delivery execution. This package studies a different state machine: **how a real-world restaurant becomes an addressable, reviewable and rankable Web object, and how a page view becomes — or fails to become — a physical visit.**

---

## 0. Why this object belongs in old-web-archaeology

Restaurant-review sites sit at an unusually revealing boundary between old Web and physical city life.

A surviving page may contain:

- restaurant name;
- branch name;
- address;
- telephone number;
- cuisine;
- price band;
- user reviews;
- food / environment / service scores;
- popularity;
- ranking position;
- coupon;
- map link;
- reviewer profile;
- publication timestamp.

But none of those fields automatically proves what happened in the restaurant itself.

The minimum state chain is:

```text
real venue exists
→ platform learns about venue
→ listing/entity created
→ metadata populated
→ reviewer claims a visit
→ review submitted
→ review accepted/published
→ scores aggregated
→ ranking/search result computed
→ page rendered to a user
→ user chooses venue
→ user calls / downloads coupon / navigates
→ venue is actually open
→ user reaches the correct branch
→ table is actually available
→ meal actually occurs
```

Therefore old-Web reconstruction must never collapse:

```text
listing
review
rating
ranking
coupon
visit
meal
```

into one event.

---

# 1. Research-unit separation

Following `docs/METHOD.md`, the following units must stay separate.

## 1.1 Platform

Examples:

- Dianping / 大众点评;
- Koubei / 口碑网;
- portal food channels;
- city-guide sites;
- telecom information services such as Web 114 / 号码百事通;
- later mobile/local-search clients.

A platform can survive while individual restaurant pages, ranking logic or account systems change completely.

---

## 1.2 Site / host

Potential historical hosts include:

```text
www.dianping.com
possibly older zsurvey.com lineage
city-specific or mobile/WAP hosts
partner portal pages carrying Dianping-derived content
```

A host string is not sufficient identity evidence for a historical service state.

---

## 1.3 Restaurant entity

A real restaurant needs its own temporal identity model.

At minimum:

```text
brand
branch
address
telephone
operator / owner if known
opening date if known
closure / relocation if known
```

Do not assume:

`same restaurant name == same historical venue`.

---

## 1.4 Listing page

A restaurant listing is a platform object.

It may outlive:

- a branch closure;
- a move;
- a change of operator;
- a concept change;
- a phone-number reassignment.

So:

> **restaurant listing identity != restaurant business continuity.**

---

## 1.5 User account / reviewer profile

A reviewer account may contain:

- nickname;
- rank / badge;
- total review count;
- personal restaurant history;
- city;
- social relationships;
- avatar/profile fields.

A public nickname is not proof of legal identity.

---

## 1.6 Review

A review requires at least three distinct times whenever evidence permits:

```text
claimed dining/event time
submission time
publication/render time
```

Old pages often expose only one.

---

## 1.7 Rating snapshot

A rendered score is a **time-dependent aggregate**, not a timeless property of a restaurant.

A historical page needs:

```text
capture datetime
score shown
review count shown
ranking context if any
algorithm/version if known
```

Without those, writing “the restaurant had 4.7 stars in 2008” may be an anachronism.

---

## 1.8 Search / ranking result

A search page may depend on:

- selected city;
- district;
- cuisine;
- price;
- atmosphere;
- popularity;
- current ranking algorithm;
- login state;
- device;
- location;
- personalization.

Therefore:

> **a restaurant’s existence in the database is not equivalent to its visibility in one historical result page.**

---

## 1.9 Capture

A Wayback locator, current mirror, quoted screenshot or media description is not automatically a verified historical capture.

Minimum desired capture evidence:

```text
original URL
archive URL
capture datetime
HTTP/status if observable
charset / encoding evidence
DOM / HTML evidence
subresource state
forms / scripts / links
whether backend data is historical or current
```

---

# 2. Pre-Web boundary: the Web inherited city directories instead of inventing them

## 2.1 1999 Beijing Web 114 as a boundary object

A contemporaneous *Beijing Morning Post* report dated 1999-09-15 described Beijing 114 launching an online lookup service at `www.114china.com`.

The report stated that the Web service was built on the existing 114 directory database, then containing more than 2.3 million number records, and could search by organisation name, abbreviation or industry category.

Source:

- 《北京114查号台提供网上查询服务》，北京晨报，1999-09-15：
  https://news.sina.com.cn/society/1999-9-15/14567.html

Evidence grade: **B — contemporaneous media description of the service and pre-existing database.**

### Archaeological significance

This establishes a useful boundary:

```text
telephone directory database exists
→ Web interface exposes existing directory
```

not:

```text
Web arrives
→ local-business database is invented
```

For restaurant archaeology, a Web directory can therefore inherit records whose provenance began outside the Web.

---

## 2.2 Directory state is not reputation state

114 / yellow-pages style systems primarily answer:

```text
what is the name?
what is the phone number?
which category?
```

Restaurant-review systems add:

```text
is it good?
what is it like?
how much?
which branch?
what do other diners think?
```

That is a distinct layer.

---

# 3. 2003–2006 Dianping: a restaurant becomes a persistent public reputation object

## 3.1 2003 origin and 2006 contemporaneous description

A 2006 *New Economy Guide* article described Dianping as created in April 2003 and explicitly contrasted its Internet-based collection of diner comments with the mailed-survey model associated with Zagat.

Source:

- 《大众点评网：Web2.0成熟时》，新经济导刊 / 新浪科技，2006-04-10：
  https://tech.sina.com.cn/i/2006-04-10/1421897310.shtml

The same report directly observed a public reviewer account, `Cina`, which had accumulated reviews across 191 restaurants and had a personal page.

Evidence grade: **B — contemporaneous media observation of public site behaviour.**

### New old-Web object

The important object is not “a restaurant article”.

It is a reusable database entity:

```text
restaurant entity
+ accumulated reviews
+ reviewer identities/pseudonyms
+ multiple score dimensions
+ persistent URL/page state
```

This persistence differentiates Web reputation from much ephemeral spoken word-of-mouth.

---

## 3.2 2006 filter logic

A contemporaneous 2006 article described the user flow as filtering restaurants by cuisine, district and atmosphere, then sorting/choosing according to user-review scores.

Source:

- 《大众点评网：让吃饭变得更讲究》，新经济导刊 / 新浪科技，2006-10-20：
  https://tech.sina.com.cn/i/2006-10-20/16121195439.shtml

Evidence grade: **B — contemporaneous functional description.**

This provides a historical state model:

```text
city selected
→ filter dimension selected
→ result set generated
→ order/rank applied
→ restaurant page opened
→ user reads reviews
```

A reconstruction that only rebuilds restaurant detail pages but not result-set formation misses a central part of the historical experience.

---

# 4. Review publication and merchant dispute are different states

## 4.1 Early legal disputes preserve otherwise fragile platform facts

2005–2006 press coverage of restaurant defamation/reputation disputes preserved concrete evidence that negative diner comments were public, persistent and commercially salient enough for restaurants to litigate against the platform and, in some cases, reviewers.

Sources:

- 《“孔家花园”再告网站 网友“老饭桶”也成被告》，东方网 / 新浪，2005-11-08：
  https://news.sina.com.cn/c/2005-11-08/01147387128s.shtml
- 《中国餐饮业网民商誉侵权第一案》，2006-01-05：
  https://finance.sina.com.cn/manage/commanage/20060105/15252251591.shtml

Evidence grade: **B — contemporaneous reporting on platform content and litigation.**

### Required separation

```text
user submitted review
≠ platform published review
≠ restaurant agreed with review
≠ review was legally defamatory
≠ review was factually false
```

A merchant lawsuit is evidence that content had social consequences, not evidence that the criticized dining experience did or did not occur.

---

## 4.2 Moderation claims are not moderation outcomes

The 2006 reporting described registration, contact details, reviewer grading and staff review/checking as platform practices.

Those are **platform claims / contemporaneous descriptions of governance**, not proof that every published review passed an effective authenticity test.

Therefore:

> `moderation mechanism described != review authenticity proven`.

---

# 5. 2007–2010: public restaurant pages become actionable city knowledge

## 5.1 2007 personal-blog counterexample

A dated 2007-12-06 BlogCN/Cnblogs page described a Shanghai resident who rarely needed to search for food because company lunches and home cooking already covered much of everyday eating; a friend, by contrast, frequently browsed food and Dianping-like sites.

Source:

- 《釜山料理吃烧烤》，博客园，2007-12-06：
  https://www.cnblogs.com/Sonne/archive/2007/12/06/984640.html

Evidence grade: **A/B boundary — dated contemporaneous personal publication currently visible; no independent historical WARC verified in this slice.**

### Significance

This is a useful adoption boundary:

> `service exists != every urban diner needs it`.

Existing institutional meal arrangements can reduce the value of local restaurant search.

---

## 5.2 2008 ranking aggregation

A 2008-01-16 Sina food article reported Dianping’s 2007 restaurant awards/list, produced from user reviews and dimensions including taste, environment and service.

Source:

- 《2007年度大众美食榜单揭晓》，新浪饮食，2008-01-16：
  https://bj.sina.com.cn/danone/art/2008-01-16/180635002.shtml

The participation counts in the story should be stored as **event/platform-reported metrics**, not converted into independent population estimates.

### State transition

```text
individual reviews
→ restaurant score
→ city-wide ranking/list
```

This matters for archive reconstruction because a ranking page is not merely a static editorial page: it may be the output of a database and aggregation logic.

---

## 5.3 2009 coupons: reputation page becomes transaction-adjacent

A 2009 Shanghai consumer report released by Dianping and republished in January 2010 described large numbers of coupon page views/downloads and restaurant listings.

Source:

- 《大众点评网发布2009年度上海生活消费报告》，PChome, 2010-01-11：
  https://article.pchome.net/content-1040396.html

Evidence grade: **B/C — contemporaneous platform-report metrics via republication.**

A restaurant page now had a transaction-adjacent branch:

```text
read reputation
→ see coupon
→ download / print coupon
→ travel to restaurant
→ merchant may or may not accept coupon under historical conditions
```

Hence:

> **coupon visible != coupon successfully redeemed.**

---

## 5.4 2010 traveller trace: page → map → physical queue

A dated 2010-06-20 51CTO personal travel blog said the writer used Dianping food reviews together with a map to find restaurants one by one in Xiamen. At a popular seafood restaurant, the group then waited about 45 minutes for a table.

Source:

- 《2010厦门之旅-美食篇》，51CTO博客，2010-06-20：
  https://blog.51cto.com/jackiechen/336161

Evidence grade: **A/B boundary — contemporaneous personal page currently visible; historical capture not independently verified.**

### Crucial state boundary

```text
restaurant highly recommended
→ user physically finds it
→ restaurant open
→ queue exists
→ table eventually obtained
```

The Web solved one uncertainty and exposed another.

> `high reputation != immediate service availability`.

---

# 6. 2010 mobile transition: search context begins to include the user’s location

A 2010-05-06 ZOL review of the Android Dianping client includes first-person usage: the author previously searched Web sites before dining, while the mobile client allowed more spontaneous restaurant lookup and could combine local data with Google Map; when travelling, the author also mentioned 12580 telephone information as a complementary route.

Source:

- 《美食搜罗全攻略 安卓版大众点评更新下载》，中关村在线，2010-05-06：
  https://4g.zol.com.cn/176/1768520.html

Evidence grade: **B — contemporaneous product-review / first-person usage evidence.**

### Browser-era versus mobile-era query state

PC Web commonly begins with:

```text
manually selected city / district
```

Mobile local search can begin with:

```text
device location
```

Therefore later mobile results must not be used to reconstruct earlier Web ranking contexts without qualification.

> **same platform brand != same query context.**

---

# 7. Overseas comparison: Zagat shows that crowdsourced reputation predates the Web

This material belongs primarily in `how-people-lived`, but it constrains old-Web interpretation.

## 7.1 1979–1983 paper survey

A 2009 Forbes interview with Tim and Nina Zagat recounts a 1979 restaurant survey among friends, roughly 200 diners reviewing around 100 New York restaurants, first circulated on paper and later self-published as an annual guide.

Source:

- Robert Reiss, “Turning A Hobby Into A Global Brand,” Forbes, 2009-12-31：
  https://www.forbes.com/2009/12/31/zagat-survey-crowdsourcing-leadership-careers-restaurants.html

Evidence grade: **C/B mixed retrospective first-person history.**

## 7.2 Commercial online services before the Web site

A 2000 Forbes article said Zagat data had been available via CompuServe and Prodigy from 1992 and AOL from 1996, before Zagat’s own full Web presence.

Source:

- “Zagat takes a big byte,” Forbes, 2000-02-08：
  https://www.forbes.com/2000/02/08/mu2.html

A 1999 Forbes article described the print guides as common restaurant-finding tools for locals and visitors and explained plans to place the fully cross-indexed database online, including addresses, telephone numbers, prices and online reviewing.

Source:

- “Zagat online,” Forbes, 1999-01-09：
  https://www.forbes.com/1999/01/09/feat_side.html

### Cross-national inference

Do not write:

`restaurant crowdsourcing was invented by Web 2.0`.

Safer lineage:

```text
word-of-mouth
→ structured paper survey
→ printed guide
→ commercial online service / CD-ROM
→ Web database
→ online reviewing
→ mobile location-aware discovery
```

---

# 8. 2015–2019: ranking and reputation become operational infrastructure

This package’s primary archaeology scope remains 1999–2015, but later evidence is retained only to identify which earlier states later became load-bearing.

## 8.1 2018 queue apps show the next handoff

Apple’s current App Store page for “美味不用等” still surfaces user reviews dated 2018-09/10 describing remote queueing before leaving work and restaurant recommendation rankings.

Source:

- Apple App Store, “美味不用等”：
  https://apps.apple.com/cn/app/id979857479

Evidence grade: **B/A boundary — current platform rendering of dated historical user comments; not equivalent to a verified 2018 App Store capture.**

The state chain expands:

```text
reputation choice
→ queue lookup
→ remote ticket/number
→ queue advances
→ user travels
→ table obtained
```

Again:

> `remote queue number != table already allocated` unless product evidence proves otherwise.

---

## 8.2 2019 anti-fraud reveals incentive pressure

Dianping reported in January 2020 that its 2019 anti-fraud campaign removed/handled large quantities of improper reviews, accounts and merchants, including paid/fake positive reviews, free-experience-for-review schemes, deletion pressure and harassment.

Source:

- 《大众点评：去年处理黑产、刷好评等违规商户逾3万家》，IT之家，2020-01-20：
  https://www.ithome.com/0/469/397.htm

All quantities are **platform-reported metrics**.

Historical implication:

> once review scores influence visibility, actors gain incentives to manipulate the review system.

This does **not** prove the percentage of fake historical reviews on any specific 2005–2015 page.

---

# 9. 2020 as a stress test of old state assumptions

A contemporaneous 2020-02-19 report found that some Haidilao delivery operations had resumed while Dianping still displayed Beijing-area dine-in stores as suspended.

Source:

- 《餐企逐渐恢复堂食业务 外卖仍是“主力军”》，中国商网 / 中国网，2020-02-19：
  https://food.china.com.cn/2020-02/19/content_75720608.htm

This sharply exposes several non-equivalences that already mattered in the old Web but were less visible:

```text
brand active
!= every branch active

restaurant page visible
!= restaurant currently open

restaurant open for delivery
!= open for dine-in

historical good reputation
!= current operational availability
```

These should be back-projected only as **state distinctions**, not as claims that 2008 restaurants had pandemic-like operating states.

---

# 10. 2024–2026: mature-rating evidence reveals why old scores need interpretation

## 10.1 2024 low-score countersearch

A 2024 *Workers’ Daily* report interviewed diners who habitually checked restaurant photos, reviews and scores before social meals but had begun treating scores less literally after disappointing experiences with high-rated venues. One interviewee also noted that when nearly all nearby restaurants appeared highly rated, the score itself became less discriminating.

Source:

- 《“勇闯”低评分餐厅，消费者为何舍高就低？》，工人日报 / 人民网，2024-01-08：
  https://finance.people.com.cn/n1/2024/0108/c1004-40154630.html

This later evidence supports an archaeology caution:

> **rating value is contextual and distribution-dependent.**

Do not interpret a historical numeric score without reconstructing its scale, distribution, review volume and aggregation rules when possible.

---

## 10.2 Offline regulars can remain digitally weak

A 2024 *People’s Weekly* report noted that some street restaurants retained stable regular customers whose patrons rarely posted online reviews, and the businesses did not depend strongly on online acquisition.

Source:

- 《“低分餐厅”迎来“反向打卡”》，人民周刊，2024-02-07：
  https://www.peopleweekly.cn/html/2024/tebieguanzhu_0207/196266.html

This yields an important preservation principle:

> **weak online reputation != weak offline embeddedness.**

---

## 10.3 2025 review-autonomy governance

In May 2025 Dianping introduced complaint/reporting mechanisms for inducement of positive reviews and harassment following negative reviews.

Source:

- 《吃饭遇到硬要好评、强删差评怎么办？大众点评推出全民监督机制》，北京商报 / 新浪财经，2025-05-14：
  https://finance.sina.com.cn/jjxw/2025-05-14/doc-inewqans0740300.shtml

This later governance history is useful because it identifies a hidden state that an old review page rarely exposes:

```text
review appears voluntary
```

is not necessarily equivalent to:

```text
review was produced without inducement / pressure
```

Historical pages usually cannot prove this either way.

---

# 11. Core reusable state gaps

## SG-01 — real-venue / listing gap

```text
restaurant exists != platform listing exists
```

A real venue may never have been listed.

---

## SG-02 — listing / current-operation gap

```text
listing exists != restaurant currently open
```

A page can outlive the business.

---

## SG-03 — restaurant-name / business-continuity gap

```text
same name != same operator / chef / concept / branch
```

Entity resolution must be temporal.

---

## SG-04 — address / physical-location gap

```text
address displayed != restaurant located there at capture time
```

Listings can lag relocation or closure.

---

## SG-05 — menu-price / live-offer gap

```text
menu/average-spend shown != exact live menu/price
```

Useful even when delivery is out of scope.

---

## SG-06 — review-submission / publication gap

```text
user submitted review != platform published review
```

Moderation may intervene.

---

## SG-07 — publication-time / dining-time gap

```text
review published at T != meal occurred at T
```

The meal may predate publication by days, months or longer.

---

## SG-08 — reviewer-account / diner-identity gap

```text
account nickname != verified legal diner
```

Even a registration/contact requirement does not prove public identity.

---

## SG-09 — review / verified-consumption gap

```text
review exists != independently verified meal occurred
```

Old platforms often predate modern transaction-linked verification.

---

## SG-10 — review-count / unique-diner gap

```text
review count != unique humans
```

One person can write repeatedly; accounts can be manipulated; aggregation rules vary.

---

## SG-11 — score / representative-opinion gap

```text
aggregate score != representative opinion of all diners
```

Self-selection matters.

---

## SG-12 — rating-snapshot / current-score gap

```text
historical score != current score
```

A current page must not be used as a historical rating snapshot.

---

## SG-13 — ranking-render / database-state gap

```text
rank page capture != complete underlying database
```

A rank is a projection.

---

## SG-14 — search-rank / quality gap

```text
first result != objectively best restaurant
```

Ranking may combine popularity, relevance, filters, commercial signals or unknown logic.

---

## SG-15 — filter-label / lived-attribute gap

```text
“适合约会” / “环境好” field != universal lived experience
```

Such labels may be editorial, algorithmic or user-derived.

---

## SG-16 — popularity / table-availability gap

```text
popular restaurant != immediately usable restaurant
```

The 2010 Xiamen blog gives a direct queue example.

---

## SG-17 — coupon-visible / coupon-valid gap

```text
coupon page visible != coupon valid at visit time
```

Need date, branch and terms.

---

## SG-18 — coupon-download / redemption gap

```text
coupon downloaded/printed != merchant redeemed it
```

Actual redemption is a private/offline transaction state.

---

## SG-19 — telephone-visible / call-success gap

```text
phone number shown != successful human contact
```

Numbers expire, lines busy, stores close.

---

## SG-20 — map-point / correct-entrance gap

```text
POI coordinate != user successfully reaches correct entrance/branch
```

Especially important in malls, campuses and old street numbering.

---

## SG-21 — desktop-city / mobile-location gap

```text
manual city query != GPS/local mobile query
```

Do not silently replay one interface as the other.

---

## SG-22 — platform-coverage / city-coverage gap

```text
many listed restaurants != census of all restaurants
```

Unlisted and low-review venues remain outside the projection.

---

## SG-23 — archival-visibility / historical-importance gap

```text
well-preserved page != historically most important venue
```

Web-visible restaurants are systematically easier to recover.

---

## SG-24 — public-page / private-choice gap

```text
page exists != historical user actually saw it before choosing venue
```

Without browsing history or contemporaneous first-person evidence, causal claims are unsafe.

---

## SG-25 — current-backend / historical-render gap

```text
old URL still resolves != historical data is being served
```

A surviving route may hydrate from a modern database.

---

# 12. Dynamic ranking is unusually hard to archive

Restaurant directory pages appear static, but many historically important states are dynamic:

- score aggregates;
- review counts;
- popularity indices;
- top-50/top-100 rankings;
- search-result order;
- coupon inventory;
- branch opening state;
- logged-in personalization;
- “nearby” location context.

An HTML capture may preserve labels while losing the historical database response that generated them.

Therefore a reconstruction must distinguish:

```text
shell survived
vs
historical query result survived
vs
current backend rehydrated old shell
```

---

# 13. Charset / browser / frontend assumptions

No browser/charset claim should be inferred solely from general knowledge of Chinese Web development.

For a verified 2003–2010 Dianping capture, record:

```text
HTTP Content-Type charset
HTML meta charset
actual decoded byte behaviour
DOCTYPE if present
frames/table/div layout evidence
JavaScript dependencies
cookie/session requirements
image/css hostnames
form/action endpoints
whether search uses querystring or POST
```

Do **not** write “it was GB2312/IE6” unless a capture or contemporary technical source proves it.

---

# 14. Historical capture attempt in this slice

Candidate historical object:

```text
http://www.dianping.com/
```

Desired period:

```text
2005–2007
```

This run attempted direct Wayback replay / CDX-style URLs for the host, including a dated replay and a 2005–2007 CDX query.

The current research environment rejected the constructed archive URLs because provenance for the exact archive URL had not first been established through a retrievable search result.

Therefore the correct result is:

> **M1 verified historical Dianping Web capture: NOT ACHIEVED IN THIS SLICE.**

Do **not** rewrite this as:

- “Wayback has no Dianping captures”; or
- “Dianping was not archived”; or
- “the historical homepage cannot be recovered.”

Those claims are not supported.

This is a locator/replay limitation, not archive absence evidence.

---

# 15. Candidate M1 object after capture is obtained

Dianping is a strong future M1 candidate because independent evidence already supports multiple historical states:

## Timepoint candidate A — 2003–2006

Evidence families already available:

- contemporaneous media descriptions;
- contemporaneous legal disputes quoting/displaying platform content;
- user/reviewer profile observations;
- printed restaurant guide lineage.

Need:

- verified historical HTML/WARC;
- URL structure;
- charset;
- result/list/detail page relationship;
- static assets;
- account/login boundary.

## Timepoint candidate B — 2007–2010

Evidence families already available:

- dated user blogs;
- media-published restaurant ranking pages;
- coupon/report material;
- mobile-client review;
- travel-blog handoff from online review to physical visit.

Need:

- verified historical restaurant detail and/or search result capture;
- rating algorithm/version evidence;
- mobile/WAP/desktop split;
- exact coupon workflow evidence.

## Timepoint candidate C — 2011–2015

Future work:

- mobile/desktop coexistence;
- group-buying / booking adjacency;
- map/local-position integration;
- transition toward transaction-heavy O2O.

This package does not yet close M1 because the archive-capture contract is not met.

---

# 16. Archive bias specific to restaurant-review systems

## 16.1 Platform-visible-city bias

A successful platform can make later researchers mistake:

```text
restaurants visible on platform
```

for:

```text
restaurants important in the real city
```

That is unsafe.

Low-tech, regular-customer and neighbourhood venues may leave far less recoverable Web evidence.

---

## 16.2 Review-survival / meal-disappearance inversion

The public review can survive for decades while the meal itself leaves almost no durable evidence.

So:

```text
review survives
!= meal details independently recoverable
```

The most recoverable item may be the representation, not the event.

---

## 16.3 Failure amplification

Extreme negative experiences, lawsuits and merchant-review conflicts are disproportionately newsworthy and archivable.

Therefore:

> many archived disputes do not imply most historical restaurant visits ended in conflict.

---

## 16.4 Popularity amplification

Highly reviewed venues create more pages, mentions, reposts and ranking records.

Their historical visibility is mechanically higher than quiet local venues.

---

# 17. Privacy and research ethics

Restaurant reviews are public-facing, but old reviewer pages can expose:

- long-term movement patterns;
- workplace/home-area inference;
- real names or pseudonyms linked across sites;
- dates and social relationships;
- photographs of companions;
- phone/contact metadata.

A historical reconstruction does not require deanonymising ordinary reviewers.

Prefer:

- page schema;
- aggregate field structure;
- pseudonym only when already central to a public contemporaneous source;
- quoted content only when analytically necessary;
- no mass reconstruction of individual dining histories.

---

# 18. Cross-link to how-people-lived

Companion life-history package:

`tmzncty/how-people-lived/topics/restaurant-reputation-local-knowledge-portability-and-city-legibility-china-1982-2026.zh-CN.md`

The life-history side introduces:

- `local-knowledge portability`;
- `dining-place addressability`;
- `weak-tie reputation infrastructure`;
- `city legibility`;
- `reputation-verification labor`;
- `venue-state volatility`;
- `defensive interpretation`.

Old-Web archaeology should keep the technical/state evidence here and leave global Zagat prehistory and post-2015 life-course comparison primarily to `how-people-lived`.

---

# 19. Evidence matrix

| Evidence | Date | Type | What it can establish | What it cannot establish |
|---|---:|---|---|---|
| Beijing online 114 report | 1999 | B contemporaneous media | Web interface built over prior telephone-directory database; category search | restaurant-review adoption |
| Dianping Web2.0 report | 2006 | B contemporaneous media | public user reviews, reviewer page, restaurant database model | every review authentic; population representativeness |
| restaurant-review litigation reports | 2005–2006 | B contemporaneous media/legal-event reporting | review publication had real merchant consequences | reviewed statements true/false by themselves |
| Dianping search/filter report | 2006 | B contemporaneous media | cuisine/district/atmosphere + score-based discovery | exact HTML/algorithm |
| Cnblogs dining post | 2007 | A/B dated personal trace | differential real-life adoption | citywide adoption rate |
| Sina annual food ranking | 2008 | B | aggregation into rankings | independent population estimate |
| platform consumer report | 2009/2010 | B/C | coupon/listing use by platform metrics | all offline redemption outcomes |
| 51CTO Xiamen travel post | 2010 | A/B dated personal trace | review+map → physical venue and queue | platform-caused restaurant quality |
| ZOL Android review | 2010 | B first-person product use | PC→mobile/location-aware shift | all user behaviour |
| Zagat Forbes material | 1979–2000 described in 1999/2000/2009 | B/C | pre-Web crowd-review lineage and commercial-online transition | Chinese adoption |
| Dianping 2019 anti-fraud report | 2020 report of 2019 | B platform metrics | existence of manipulation/governance problem | historical fake-review rate |
| 2020 restaurant-status reporting | 2020 | B | operation-mode volatility | 2000s normal operation pattern |
| 2024 low-score interviews | 2024 | B | contemporary defensive rating interpretation | all young consumers |
| 2025 induced-review reporting | 2025 | B | review-autonomy governance | historical prevalence |

---

# 20. Unknowns / next evidence requests

1. Obtain at least one verified 2003–2006 Dianping/zsurvey historical capture.
2. Obtain a second verified 2007–2010 Dianping capture with a different page type/timepoint.
3. Resolve early URL/host lineage (`zsurvey.com` → `dianping.com`) with primary DNS/archive/company evidence rather than later retellings.
4. Recover exact old search-result/filter parameter structure.
5. Recover historical score labels, scales and aggregation explanations.
6. Determine when restaurant branch entities became explicit rather than text-only location variants.
7. Determine early login/cookie requirements for posting reviews.
8. Recover at least one historical reviewer profile and one restaurant detail page without deanonymising unnecessary personal data.
9. Recover old electronic coupon terms and branch-validity logic.
10. Compare same restaurant entity across two capture dates to test stale address/phone/review continuity.
11. Find stronger contemporaneous evidence for 1990s Chinese paper restaurant guides / yellow-pages use in actual restaurant selection.
12. Find a low-online-visibility neighbourhood restaurant life history as a counterexample to platform-visible-city bias.

---

# 21. What this package changes

The central old-Web question is no longer merely:

> “What did Dianping look like?”

It becomes:

> **Which layer of the physical city did a historical page actually encode, and which parts of the real dining event remained outside the Web?**

A restaurant page can survive while the restaurant dies.
A score can survive while the aggregation logic disappears.
A review can survive while the actual meal becomes unverifiable.
A city ranking can survive while thousands of unlisted neighbourhood venues vanish from the historical record.

The reconstruction target is therefore not a decorative screenshot of “an old restaurant-review website”.

The stronger target is a state-separated model of:

```text
city directory
+ restaurant entity
+ public reputation
+ ranking/query projection
+ user decision
+ offline handoff
+ archival loss
```

Only then can a restored old Web page be connected safely to the harder historical question: **how did ordinary people learn enough about an unfamiliar city to decide where to go next?**
