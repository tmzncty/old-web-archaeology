# Early online real-estate exhibition, queue, auction, and offline conveyance, 2000–2007

> Scope: 2000–2007 年中文 Web 中，房地产网站怎样从“在线看楼盘”向网上排号、网上竞价等更深事务层推进；重点不是房地产市场史，而是**哪些购房状态真的进入浏览器、哪些资格/资金/合同/产权状态仍在 Web 外部**。
>
> Companion ordinary-life research: `tmzncty/how-people-lived/places/china/early-individual-home-buyer-life-horizons-2000-2007.zh-CN.md`.

本文件遵守 `docs/METHOD.md`，并特别响应 `docs/RESEARCH_SATURATION_DEDUP_AND_ARTIFACT_PRIORITY_AUDIT_2026-09-12.md` 的去重门禁：这里不再写一个泛化的 `housing page != transaction` state-gap，而只保留一个此前未单独建模的历史 transaction architecture：

> **房地产 Web 可以先把展示、排号或竞价搬上网，但“获得进入网上事务的资格”本身可能依赖线下/银行资金状态；最终合同与产权又继续回到 Web 之外。**

与已有文件分工：

- `docs/HOUSING_INVENTORY_ONLINE_SIGNING_FILING_AND_OCCUPANCY_STATE_GAPS_2004_2015.md`：官方/准官方库存、网签、备案、登记和入住；
- `docs/CREDIT_APPLICATION_LOAN_PORTALS_INSTALLMENT_ENROLLMENT_AND_REPAYMENT_STATE_GAPS_2005_2008.md`：银行贷款申请、审批、账户和还款；
- 本文件：**2000s 初期商业房地产门户的 exhibition / queue / auction 前台，以及其与线下资格、保证金、选房、签约的编织。**

---

## 1. 为什么这不是另一个近义 state-gap 文件

现有住房 Web 研究已经充分证明：

```text
listing visible
!= inventory live
!= contract signed
!= filing complete
!= title registered
!= household moved in
```

本轮真正新增的是一个不同的执行形态：

```text
public Web discovery
→ Web registration / queue / bid
→ non-Web identity / qualification / money gate
→ Web credential or queue state
→ Web bid / number allocation
→ offline viewing / contract / financing / conveyance
```

尤其 2007 年朝外 SOHO 网上拍卖的同期规则明确显示：

> **先有真实身份 + 拍卖公司资格 + 30 万元保证金实际到账，才会发给用户网上竞买账号和密码。**

也就是说：

```text
account credential
```

本身不是一个单纯网站注册结果，而是一个由**外部资金清算状态**触发的事务令牌。

这在现有 domain notes 中不是简单的 `form submitted != completed` 重复。

---

## 2. Evidence map

| ID | Date | Object | Evidence | Grade | Main value |
|---|---:|---|---|---|---|
| E1 | 2000, recalled 2009 | SouFun online residential exhibition | Fang/SouFun 10-year retrospective | C / platform retrospective | earliest known platform self-history of online exhibition topology |
| E2 | 2000, described 2001 | Shenzhen real-estate fair with online component | China Construction News reprint | B | near-contemporary corroboration that online/physical fair hybrid existed |
| E3 | 2000, recalled 2007/2009 | Pan Shiyi / SouFun online auction | Jinghua Times 2007 + platform retrospective | B/C | proves 2007 actors remembered a 2000 auction; exact original Web artifact still unverified |
| E4 | 2003, recalled 2009 | Chaoyang New City online queue | platform retrospective | C | ordinary-home queue architecture candidate |
| E5 | 2007 | Chaowai SOHO online auction | Jinghua Times / Sina | B | explicit identity → deposit → credential → online-bid gate |
| E6 | 1999–2000 U.S. | HomeAdvisor | Microsoft contemporaneous product material | A/B | overseas comparison: listing + mortgage transaction layers were also being integrated |

The grades are intentionally conservative.

A current Fang anniversary page saying “2000 年首创” is evidence that **Fang later represented its history that way**, not a substitute for a 2000 capture.

---

## 3. 2000: online home exhibition is best treated as a later platform-memory claim, not a verified historical page

Fang/SouFun's 2009 “中国网络房地产十年” retrospective states that on 2000-02-28 a coalition of real-estate websites in about 20 cities launched a “2000年网上住宅大联展,” with online halls for Beijing, Shanghai, Chengdu, Xi'an, Tianjin, Shenzhen, Chongqing, etc.

Source:

- Fang/SouFun 10-year retrospective, 2009: https://sh.esf.fang.com/zt/200906/10znqindex.html

Evidence grade: **C / later platform retrospective**.

The page frames the change as allowing home seekers to avoid repeatedly visiting fairs and carrying home stacks of brochures.

That retrospective supports only the narrow claim:

> By 2009, SouFun publicly represented a 2000 multi-city online residential exhibition as part of its own early product history.

It does **not** yet support:

- exact 2000 hostnames;
- exact HTML / DOM / frames / JavaScript;
- whether every named city hall was live on the same day;
- visitor counts;
- whether a visitor could reserve or buy a unit from the exhibition itself;
- browser / charset assumptions;
- a claim that most home buyers used it.

### 3.1 Life-history meaning if the retrospective is broadly accurate

The likely change is not “houses became purchasable entirely online.” It is narrower:

```text
physical housing fair / newspaper / sales office
→ candidate-set construction partly possible from a screen
```

That would compress **search** before it compresses **commitment**.

But this remains a historical hypothesis until a period-correct artifact or near-contemporary operation report is opened and verified.

---

## 4. A near-contemporary boundary: Shenzhen 2000 real-estate fair had an online component

A China Construction News retrospective of the 2000 Shenzhen property market, published/reposted in 2001, describes the city's 2000 real-estate fair as having opened an “网上交易会” alongside the physical event.

Source:

- 中国建设报 / 温州网 repost, 2001-08-13, “2000年深圳楼市回眸”：https://home.66wz.com/system/2001/08/13/002971032.shtml

Evidence grade: **B** (near-contemporary industry/media summary).

This is useful because it is a different evidence family from SouFun's 2009 anniversary page.

It still does not tell us the Web workflow in detail, but it supports a broader minimum claim:

> Around 2000, at least some Chinese property fairs were already treating an online layer as part of the event rather than as a completely separate later invention.

The hybrid topology matters:

```text
physical fair
+ media advertising
+ phone / sales office
+ online fair
```

not:

```text
physical market disappears
→ pure Web replaces it
```

---

## 5. The remembered 2000 Pan Shiyi auction: preserve the claim, not the legend

A 2007 *Jinghua Times* report about a new online auction says SouFun chairman Mo Tianquan recalled that Pan Shiyi and SouFun had already run an online auction in 2000 and that two commercial units sold above the market price.

Source:

- 京华时报 / 新浪科技, 2007-01-12: https://tech.sina.com.cn/i/2007-01-12/09251332243.shtml

Evidence grade for the **2007 statement**: **B**.

Evidence grade for the **2000 event details**: **C-like retrospective claim embedded in B reporting**.

Fang's 2009 retrospective also says Pan Shiyi sold two units through SouFun online bidding in 2000.

Source:

- Fang/SouFun, 2009 retrospective: https://sh.esf.fang.com/zt/200906/10znqindex.html

These two pages should **not** be counted as two fully independent confirmations of the 2000 event; both may rely on the same company memory.

### 5.1 Do not write “China's first online property auction” yet

Later pages repeatedly use “first” language, but this run has not opened a 2000 contemporaneous auction page, rule sheet, result page, press release, or independent newspaper story that establishes priority against every other Chinese site.

Therefore the safe claim is:

> Later SouFun/company-linked histories and a 2007 contemporary report remembered a Pan Shiyi/SouFun online property auction in 2000.

Not:

> It has been archaeologically verified as China's first online property auction.

### 5.2 Conflicting later details are a warning

Later summaries on the Web sometimes describe different counts or broader 2000 online property-sale events.

Without the original 2000 artifact, exact item counts, URLs, bid timing and price path should remain **UNKNOWN** unless supported by a clearly independent period source.

This is a classic case of:

> **retrospective milestone compression** — a later corporate timeline can preserve that “something important happened” while flattening the messy original workflow into a clean anniversary milestone.

---

## 6. 2003 Chaoyang New City: an ordinary-home queue architecture appears in later platform history

Fang's 2009 retrospective says that in May 2003 SouFun and Beijing's Chaoyang New City economic-housing project used online queuing / subscription:

- project, layout, environment and transport information were placed online;
- users filled an online subscription/queue form;
- buyers still needed identity and relevant qualification documents;
- staff pulled applicant data from the online system and filtered valid customers;
- later selection/signing remained part of the purchase workflow.

Source:

- Fang/SouFun, 2009 retrospective: https://sh.esf.fang.com/zt/200906/10znqindex.html

A 2007 media/new-media book excerpt likewise describes the general online-queue workflow as:

```text
online queue application
→ queue verification
→ on-site home selection
→ on-site contract
```

and recalls very heavy traffic for the 2003 Chaoyang New City event.

Source:

- 肖勇，《赢在新媒体》节选，新浪博客，2007: https://blog.sina.com.cn/s/blog_4bda6da101000cbt.html

Evidence grade: **C/B-secondary retrospective**, not a 2003 original artifact.

### 6.1 Why this candidate matters despite weak artifact status

This is potentially a genuinely ordinary-life transaction architecture:

> a scarce housing queue was partially moved from physical presence into a remote information-and-numbering system.

If period artifacts are recovered, it could answer:

- Did a user need an account first?
- What identity fields were entered?
- Was the queue number first-come-first-served by server timestamp?
- Was a CAPTCHA present?
- How did the site handle duplicate identity numbers?
- What exactly did “有效客户” mean?
- Was the result visible online or delivered by phone/email?
- What happened during overload?
- Were failed submissions logged?

Those questions matter to ordinary life because a queue system can change whether a worker must physically camp at a sales office, take leave from work, pay an intermediary, or rely on a relative.

### 6.2 Current stop condition

This run **did not obtain a verified 2003 historical capture** of the queue page.

Therefore do not use the retrospective's claims to reconstruct the interface.

---

## 7. 2007 Chaowai SOHO: the transaction topology is explicit enough to add a new state model

The strongest evidence in this slice is the 2007-01-12 *Jinghua Times* report on two Chaowai SOHO shops scheduled for online no-reserve auction through a SouFun auction platform supplied by Tianwen Auction.

Source:

- 京华时报 / 新浪科技, 2007-01-12: https://tech.sina.com.cn/i/2007-01-12/09251332243.shtml

Evidence grade: **B** (contemporary report quoting the announced auction rules).

The report says a bidder had to:

1. provide real name, address, phone number and email;
2. register with Tianwen Auction and obtain bidder qualification;
3. pay a **RMB 300,000 bidding deposit** to a designated bank / real-estate company account;
4. wait for the money to arrive in the account;
5. only then receive the online bidding username and password;
6. use those credentials to participate in online bidding.

This gives a much more specific architecture than “there was an online auction.”

### 7.1 New state chain

```text
A0 public auction notice visible
A1 identity information supplied
A2 auction-company registration exists
A3 bidder qualification granted
A4 deposit transfer initiated
A5 deposit actually credited to designated account
A6 online bidding credential issued
A7 bidder can authenticate
A8 bid submitted
A9 bid accepted by auction system
A10 auction closes / winner determined
A11 offline/legal transaction steps continue
A12 contract / payment / conveyance / registration complete
```

The critical new boundary is:

```text
Web account request
!= bidder credential
```

because:

```text
bidder credential
requires an external cleared-funds state
```

This can be named:

> **cleared-funds credential gate（到账资金凭证门）**

or more generally:

> **external-state-issued Web credential** — the browser credential is granted only after a non-Web institution confirms an external state.

This architecture also appears in other domains (brokerage, ticketing, wholesale marketplaces, membership), but this is a concrete Chinese old-Web real-estate example.

### 7.2 The Web does not contain the whole transaction even if bidding is genuinely online

Even a perfect auction-page capture could fail to preserve:

- whether the deposit actually arrived;
- bidder qualification documents;
- the private credential issuance event;
- full bid ledger;
- invalid/rejected bids;
- final settlement;
- sales contract;
- tax/payment status;
- property conveyance/registration;
- possession/occupancy.

Therefore a new preservation rule is justified:

> **verified online bidding interface != verified bidder eligibility != verified property conveyance**

This is not merely philosophical: the eligibility token itself depends on a bank/account state archive crawlers would not see.

---

## 8. Why “online auction” is not the same thing as e-commerce checkout

Real estate is unusually useful for old-Web archaeology because the object is:

- high value;
- legally registered;
- geographically fixed;
- often credit-financed;
- identity-heavy;
- slow to convey;
- tied to offline inspection and possession.

So a page can move unusually deep into the transaction — even accepting live bids — while the final legal state remains elsewhere.

A more accurate early-Web topology is:

```text
Web: discover / compare / queue / bid
Bank: funds / guarantee / mortgage
Auction company or developer: qualification / acceptance / contract
Property administration: filing / registration
Physical world: inspection / delivery / occupancy
```

This is **cross-institutional state assembly**, not “the house was bought on one website.”

---

## 9. Cross-channel evidence also corrects the history of user access

The companion life-history file notes that in Shanghai in 2000 individual purchasers already accounted for 93% of commodity-house sales while the official bulletin reported 882,400 Internet-user households/accounts under its period statistical wording.

Source:

- Shanghai Municipal Government, 2000 statistical bulletin: https://www.shanghai.gov.cn/nw3994/20200813/0001-3994_88.html

Evidence grade: **A**.

This provides a vital boundary for any old-Web narrative:

> **market housing adoption was already much broader than direct household Web use.**

Therefore early real-estate sites should not be treated as the universal transaction substrate of the 2000 housing market.

They were an emerging layer used by some developers, intermediaries and consumers while newspaper ads, phone calls, fairs, sales offices, banks and face-to-face signing remained central.

---

## 10. Overseas comparison: U.S. online real estate in 1999–2000 also bundled listings and mortgage decisions

Microsoft's contemporaneous HomeAdvisor material offers a useful comparison.

### 10.1 1999: listing aggregation was already large-scale

Microsoft said in August 1999 that HomeAdvisor had signed access to more than 750,000 U.S. listings through brokers and MLS partners.

Source:

- Microsoft, 1999-08-09: https://news.microsoft.com/source/1999/08/09/msn-homeadvisor-signs-extensive-new-listing-agreements/

Evidence grade: **A/B** (contemporary company statement about its own service).

### 10.2 2000: the site claimed deeper mortgage execution

In May 2000 Microsoft/HomeAdvisor announced MortgageDirect, describing real-time risk-based pricing, automated credit checks, appraisal/underwriting steps and online rate locking.

Source:

- Microsoft, 2000-05-30: https://news.microsoft.com/source/2000/05/30/homeadvisor-com-guarantees-lowest-priced-loan-for-every-home-buyer/

Evidence grade: **A/B**.

By October 2000 the service claimed about 850,000 property listings updated daily plus valuation and mortgage tools.

Source:

- Microsoft, 2000-10-17: https://news.microsoft.com/source/2000/10/17/for-second-consecutive-time-gomez-crowns-homeadvisor-com-best-online-home-buying-site/

Evidence grade: **A/B**.

### 10.3 But deeper Web execution created new hidden-state risks

A 2000 *Washington Post* report followed a user who repeatedly submitted identifying information to online lenders while comparing refinance terms; those actions triggered credit inquiries, and subsequent offers changed.

Source:

- Caroline E. Mayer, “No Credit for Web Surfing,” *Washington Post*, 2000-04-26: https://www.washingtonpost.com/archive/business/2000/04/26/no-credit-for-web-surfing/a5b1631f-6aea-429c-9d60-2f6eb413709c/

Evidence grade: **B**.

This produces a useful cross-country comparison:

```text
China early real-estate Web:
public discovery / exhibition / queue / auction partly digitized,
while qualification, money and conveyance remained strongly braided with offline institutions.

U.S. 1999–2000 HomeAdvisor/lenders:
listing and mortgage decision layers could be more tightly integrated,
but “just browsing” could unexpectedly cross into a private credit-state transition.
```

The shared phenomenon is not “the Internet eliminated intermediaries.” It is:

> **ordinary users had to learn which screen actions were informational and which actions mutated institutional state.**

---

## 11. Preservation mechanism: service topology survives more poorly than marketing milestones

This slice reveals a specific preservation asymmetry.

What survives well today:

- anniversary timelines;
- “first online exhibition” / “first auction” milestone stories;
- media reports announcing a 2007 auction;
- platform corporate memory;
- project names.

What remains unverified or likely missing from ordinary public archive replay:

- 2000 exhibition DOM and city-hall navigation;
- 2000 auction page and bid ledger;
- 2003 queue form and result page;
- exact validation rules;
- session/login state;
- private applicant records;
- bank deposit clearing;
- credential issuance;
- final legal conveyance.

This can be called:

> **milestone-survival / workflow-loss asymmetry**.

It differs from simple `index-shell survival`: here the historical story that “we launched X” survives, while the stateful workflow that made X executable is what disappears.

### 11.1 Important limitation

This run has **not** yet demonstrated the loss mode with a verified pair of historical captures. It is therefore a research observation / hypothesis grounded in the source set, not an M1 artifact result.

---

## 12. Artifact status: M1 NOT ACHIEVED in this slice

This run did not open and verify a period-correct 2000–2003 SouFun page satisfying the repository's M1 minimum contract.

Specifically missing:

- verified original URL;
- archive capture URL;
- capture datetime;
- replay/HTTP status;
- historical Content-Type / charset where available;
- main document vs subresources;
- form action / session behavior;
- at least a second historical time point.

The 2009 Fang pages are **later retrospective pages**, not captures from 2000 or 2003.

The current Sina-hosted 2007 *Jinghua Times* article is a contemporaneous text source, but it is **not the 2007 auction interface**.

Therefore:

```text
M1 verified historical real-estate transaction capture: NOT ACHIEVED
```

This means only “not verified in this slice.” It does **not** mean Wayback or another archive never captured the resources.

---

## 13. Claim ledger

### Confirmed / directly supported

1. In 2007 a contemporaneous report announced a Chaowai SOHO online auction through a SouFun/Tianwen platform.
2. The announced 2007 rules required real identity information, auction-company registration/qualification, a RMB 300,000 deposit, confirmed arrival of funds, and only then an online bidding username/password.
3. A near-contemporary 2001 account of Shenzhen's 2000 property market says a major real-estate fair included an online trading/fair component.
4. In 2000 Shanghai's official bulletin reports individual purchasers already accounted for 93% of commodity-house sales while Internet use was much narrower than universal household access.
5. U.S. HomeAdvisor contemporaneously advertised very large listing inventories and mortgage transaction tools in 1999–2000.

### Probable / useful but dependent on later retrospective evidence

1. SouFun operated a multi-city online residential exhibition in February 2000 broadly resembling the later company description.
2. Pan Shiyi/SouFun ran an online property auction in 2000 involving two units.
3. Chaoyang New City used a Web queue/subscription workflow in 2003 that handed off to identity/qualification checks and offline selection/signing.

### Unknown

1. Exact 2000/2003 original URLs and hosts.
2. Exact DOM/layout/charset/browser requirements.
3. Whether auction/queue state was server-rendered, session-bound, JS-driven or otherwise difficult for archives.
4. Exact 2000 bid count, timing and complete result ledger.
5. Exact 2003 queue ordering and duplicate-prevention logic.
6. What proportion of ordinary home buyers used these online routes.
7. Whether users primarily accessed them from home, office, school, cybercafe, or through another person.

---

## 14. Hindsight risks

### 14.1 Do not turn a later corporate “first” into historical fact

Anniversary histories simplify.

Use them to locate candidates; do not let them settle priority claims without period evidence.

### 14.2 Do not equate “online bidding” with “online home purchase”

The 2007 source itself disproves that simplification: bidder eligibility depends on external identity and money states before the Web credential exists.

### 14.3 Do not assume early users owned Internet-connected home PCs

A housing seeker could access a site at:

- work;
- a cybercafe;
- a friend's computer;
- an intermediary's terminal;
- a sales office.

Direct Web use is not identical to household Internet ownership.

### 14.4 Do not infer ordinary-life prevalence from memorable experiments

Online auction events are unusually newsworthy and therefore unusually preservable.

A routine phone call + sales-office visit may have been far more common while leaving much weaker Web traces.

---

## 15. Next artifact targets

Priority order:

1. **2003 Chaoyang New City queue page**
   - ordinary-life payoff is highest;
   - try project URL variants, SouFun Beijing subdomains, archived press links and contemporary forum backlinks.

2. **2000 online residential exhibition**
   - identify exact alliance/host structure and city hall URLs;
   - verify whether it was static brochure aggregation or had inquiry/registration actions.

3. **2000 Pan/SouFun auction**
   - find period auction rule/result page or independent newspaper report;
   - reconcile item-count differences in later retellings.

4. **2007 Chaowai SOHO auction interface**
   - current media gives rules; next gain would be actual interface/capture;
   - check whether login, bidding ledger and result state are separately archived.

For any candidate capture, record the complete METHOD fields rather than only a screenshot.

---

## 16. Cross-research payoff

This slice changes the ordinary-life interpretation in one precise way.

It is too simple to describe the early Web as merely “letting people see houses online.”

By the 2000s, parts of the housing path were already being moved into distinct digital states:

```text
browse
→ register
→ queue / qualify
→ deposit clears
→ receive transaction credential
→ bid
```

But the household still had to assemble the rest through banks, developers, auction firms, contracts, registration offices and physical possession.

So the useful historical question is not:

> **When could people buy a house online?**

It is:

> **Which parts of buying a house became executable at distance first, and what new institutional state did a person have to satisfy before the next screen became available?**

That is a transaction architecture worth preserving separately from both generic housing listings and later official online-signing systems.
