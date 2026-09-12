# IP telephone cards, 201 campus phones, public phone bars, and the cross-protocol service topology — 1999–2008

> Status: research checkpoint, not an M1 complete archaeological case.
>
> Scope: Chinese Internet / old-Web boundary, 1999–2008. The object is not “telephone history in general.” It is a historically important service in which **IP network transport, telephone terminals, DTMF/IVR account control, retail prepaid cards, public phone shops, and sometimes Web marketing/support were one service stack**. This matters to old-Web archaeology because a browser-centered archive can preserve only a small part of what ordinary users actually executed.

## 0. Why this is not another generic `page != transaction` note

The repository's 2026-09-12 de-duplication audit says a new domain note should normally add at least one of:

- a verified artifact;
- a new transaction architecture;
- a new ordinary-life pathway;
- a new preservation failure mode;
- or a cross-time transition.

This slice qualifies mainly on **new transaction architecture + new ordinary-life pathway**.

The relevant historical transaction is not:

```text
Web page -> form -> private Web state -> offline completion
```

It is closer to:

```text
retail / institutional acquisition of a card or account
-> access to some telephone terminal
-> dial service access code
-> DTMF / IVR account authentication
-> enter destination number
-> carrier IP transport / gateway
-> destination telephone network
-> metering / balance decrement
```

For public phone bars, the shape can instead be:

```text
walk-in user
-> operator-owned shared telephone terminal
-> direct dial or simplified front end
-> computer / operator metering
-> carrier long-distance / IP service
-> cash settlement at the shop
```

The exact gateway and billing topology varied by operator, city and product. The diagrams above are **research abstractions**, not claims that every 179xx card or every phone bar used identical equipment.

The central archaeological distinction is:

```text
Internet/IP transport exists
!=
Web browser is the execution interface
!=
end user is an Internet subscriber
```

---

## 1. 1999 contemporaneous boundary: IP telephone service was authorized as a telephone-access service

On 1999-04-27 China's Ministry of Information Industry approved trial IP telephone services by China Telecom, China Unicom and Jitong. A contemporaneous *People's Daily* report gives:

- China Telecom access code `17900`;
- China Unicom `17910`;
- Jitong `17920`;
- trial domestic long-distance tariff: RMB 0.30/minute;
- the IP telephone tariff excluded the local telephone access charge.

Source:

- *People's Daily*, 1999-04-28, “IP电话试验正式获准　试验期间国内长途每分钟仅0.3元”: https://cn.govopendata.com/renminribao/1999/04/28/2/

Evidence grade: **B**, contemporaneous press report of the regulator's announcement.

A 2000 contemporaneous user instruction for China Unicom makes the non-Web interaction explicit. Fixed-line callers could buy an IP telephone card, dial `17910`, then follow voice prompts to enter the card number, password and destination number.

Source:

- ZOL / *Beijing Youth Daily*, 2000-06-12, “联通IP又开通哪些城市”: https://news.zol.com.cn/2000/0612/5333.shtml

Evidence grade: **B**.

This is enough to reject a common hindsight shortcut:

```text
IP service = user opened the Internet / Web
```

The user-facing endpoint could simply be an ordinary DTMF telephone.

---

## 2. New state model: the account could move while the terminal stayed shared

Early-2000s reports show a market in prepaid IP telephone cards sold at substantial discounts. The user carried a card/account/PIN and could invoke the long-distance service from an eligible telephone.

Examples:

- Shenzhen market report, 2000-12-08: https://finance.sina.cn/sa/2000-12-08/detail-ikftpnnx6095431.d.html
- Nanjing IP-card discount report, 2001-10-29: https://tech.sina.com.cn/it/t/2001-10-29/89668.shtml
- Beijing card comparison, 2002-03-22: https://news.zol.com.cn/2002/0322/37934.shtml

Evidence grade: **B**.

For old-Web / infrastructure archaeology, the relevant states are therefore not simply `phone owner / non-owner`.

A more useful decomposition is:

```text
TERMINAL_AVAILABLE
CARD_OR_ACCOUNT_OBTAINED
ACCESS_NUMBER_REACHABLE
ACCOUNT_ACCEPTED
DESTINATION_REACHABLE
CALL_CONNECTED
BALANCE_DECREMENTED
CALL_COMPLETED
```

The physical terminal, access line, prepaid identity and long-distance network may belong to different actors.

This is a historically distinctive form of **terminal–service decoupling**.

---

## 3. 2003 Beijing university evidence: users stacked 201 and IP systems

A particularly strong contemporaneous behavioral trace appears when Beijing Communications disabled 201-card “nested dialing” into other operators' IP telephone cards in July 2003.

*Beijing Times* reported that some university students said most students used a 201 card and then dialed an IP card, because this could avoid the local-call component and leave only the RMB 0.30/minute IP long-distance charge. After the interconnection was disabled, customer-service complaints increased sharply.

Source:

- *Beijing Times*, 2003-07-23, Sina preservation, “不准用201卡套拨IP电话”: https://news.sina.cn/sa/2003-07-23/detail-ikkntiak7674806.d.html

Evidence grade: **B**, contemporaneous journalist report containing user-group testimony.

This adds a transaction architecture that a page-only archaeology would easily miss:

```text
campus/shared telephone
-> 201 account/card layer
-> second IP-card layer
-> long-distance network
```

The ordinary user was actively optimizing across **two account systems and their settlement boundary**.

That gives a useful preservation warning:

```text
published tariff table
!=
actual effective calling route used by students
```

because real behavior depended on nesting, interconnection and operator policy.

---

## 4. Public phone bars were a physical front end to an IP-era service stack

A July 2003 Nanjing report says Jiangsu Unicom had begun laying out long-distance phone bars in 2001 and located them especially in urban-edge areas, construction sites and places dense with migrant population. The operator explained that fixed telephones at worksites or temporary residences could not satisfy everyone, while mobile phones were still not universal and were expensive; the phone bar let migrant workers call home from a shared commercial facility.

Source:

- *Yangtze Evening Post*, 2003-07-11, Sina preservation, “城市话吧上演‘三国大战’”: https://news.sina.com.cn/s/2003-07-11/0811360267s.shtml

A December 2003 investigation describes these phone bars as operator-authorized businesses concentrated around residents, students and migrant workers, and notes that some mobile public-phone businesses used carrier IP circuits.

Source:

- ChinaByte / Sina, 2003-12-02, “移动‘话吧’调查：低价长途背后的灰色陷阱”: https://tech.sina.com.cn/it/t/2003-12-02/1526262920.shtml

Evidence grade: **B**.

Archaeologically this matters because the service's visible “UI” could be:

- a shop sign;
- a paper price table;
- a telephone handset;
- a card;
- an IVR prompt;
- a small local billing computer visible only to the operator;
- and cash payment after the call.

A Web crawl could preserve none of those states even though the underlying long-distance transport was IP-based.

---

## 5. A surviving 2003 institutional content artifact: CERNET / campus VoIP without browser execution

Henan Normal University's current site still serves a legacy page dated **2003-06-17**, titled “校园网IP电话长途开通说明”. The page says the campus-network IP telephone system had interconnected with the CERNET / CERNET service company's IP telephone system and could place long-distance calls.

The page preserves period-specific operational details:

- an institutional unit had to apply for long-distance activation;
- charges were transferred through the university's finance office;
- internal network calls and external calls had different tariffs;
- users dialed fixed or mobile destination numbers directly from an IP telephone, ending with `#`;
- the page includes a sample application form with unit name, phone location, international-long-distance flag, contact name, phone, mobile and email.

Source:

- Henan Normal University, page carrying publication date 2003-06-17, “网络中心：校园网IP电话长途开通说明”: https://www.htu.edu.cn/2010/1019/c8955a64103/page.htm

Evidence handling:

- **A-ish institutional content / current live legacy representation**, because it is an institutional page carrying dated operational material;
- **NOT a verified 2003 Web capture**;
- current DOM, current CMS wrapper, current HTTP headers, current charset and current URL path must not be back-projected to 2003.

The narrow claim is only:

> the university currently preserves institutional content dated 2003-06-17 that describes an operational campus/CERNET IP-telephone workflow.

This is useful because it demonstrates a historically real IP service whose execution interface was a telephone and institutional application process, not a browser transaction.

---

## 6. Web could be marketing / procurement while execution remained cross-protocol

A different 2002 report describes inexpensive “network phone cards” purchasable through sites such as 21CN and 163, then used from a PC with sound card, microphone/headset and Internet connection.

Source:

- *New Express*, 2002-07-05, Sina preservation, “国际长途0.32元/分钟 网络电话卡在广州受欢迎”: https://tech.sina.com.cn/it/t/2002-07-05/124415.shtml

Evidence grade: **B**.

This warns against collapsing all “IP telephone cards” into one endpoint model.

At least two user-facing topologies coexisted:

```text
ordinary telephone -> IVR / DTMF -> IP carrier network -> telephone
```

and

```text
Web purchase / PC audio client -> Internet -> telephone network
```

The brand term or article category `IP电话` is therefore insufficient to infer terminal, protocol, browser requirement or account state.

Rule:

```text
terminology continuity != endpoint/protocol identity
```

---

## 7. Cross-protocol service decomposition: a new archive-gap model

This slice introduces a preservation distinction more specific than the generic statement “the Web page is not the transaction.”

### 7.1 The same service could have several independently preservable planes

```text
retail / advertising plane
Web help / marketing plane
telephone access plane
IVR / DTMF control plane
private account / balance plane
carrier routing / IP transport plane
PSTN destination plane
shop-local billing plane
```

Each can survive or disappear independently.

A historical Web help page might survive while:

- the access number no longer routes;
- IVR audio is lost;
- the card account database is gone;
- the carrier gateway implementation is undocumented;
- the shop billing software is lost;
- no record of the completed call exists.

So the reusable inequality is:

```text
verified historical Web help page
!=
verified historical IVR behavior
!=
verified private account validity
!=
verified carrier routing path
!=
verified completed call
```

This is **cross-protocol service decomposition**.

### 7.2 Why this differs from the previous teletext boundary slice

The teletext slice demonstrated a **signal-layer archive gap**: machine-readable digital content could enter a PC through broadcast signals that URL archives never saw.

This IP-telephone slice is different:

- the service itself could include ordinary Web marketing/support;
- but execution crossed from Web/retail into telephone DTMF/IVR and carrier networks;
- private prepaid balance and routing state were essential to success;
- the user may never have touched a browser.

The missing artifact is therefore not merely “a non-Web signal.” It is the **cross-protocol workflow between several systems**.

---

## 8. Cross-time change: from cards and booths toward direct dialing and personal mobile endpoints

A 2008 Guangzhou report records that IC-card public booths had declined sharply while public phone bars still had customers, especially for cheap long-distance calls or emergency backup. The same report retrospectively notes that 2003-era phone bars increasingly used computer metering and direct dialing, removing the long sequences of card numbers and passwords required by older card workflows.

Source:

- *Information Times*, 2008-10-16, Sina preservation, “过气电话亭成了都市‘鸡肋’”: https://news.sina.com.cn/o/2008-10-16/040714580738s.shtml

Evidence grade:

- 2008 observation: **B**;
- retrospective description of earlier popularity: **C/B mixed** and should not establish precise launch dates by itself.

This supports a real interface transition:

```text
user carries card + manually enters credentials on shared terminal
->
shop abstracts card/account complexity and exposes direct dialing + computer metering
->
increasingly, user carries their own mobile endpoint and subscriber identity
```

The important dimension is not only device miniaturization. It is **where account state and interaction complexity live**.

---

## 9. Overseas comparison: prepaid phone cards were also a portable communication identity

The U.S. Federal Trade Commission wrote in 1997 that prepaid phone cards had become important for households without telephones, students, travelers and people without long-distance service. In the specific enforcement case, sellers targeted Indian-American users making calls to India and neighboring countries, using ethnic newspapers, retail displays and a World Wide Web home page.

Source:

- U.S. FTC, 1997-08, “FTC Charges Seller of Prepaid Phone Cards with Deception…”: https://search.ftc.gov/news-events/news/press-releases/1997/08/ftc-charges-seller-prepaid-phone-cards-deception-causing-substantial-losses-consumer

Evidence grade: **A**, contemporaneous regulator record; allegations remain allegations rather than adjudicated facts.

A 2001 *Washington Post* field report observed immigrants using prepaid cards at public telephones. One Sri Lankan caller said repeated failed calls to his wife and children still consumed small amounts of card balance.

Source:

- *The Washington Post*, 2001-09-02, “Hearing the Call”: https://www.washingtonpost.com/archive/lifestyle/magazine/2001/09/02/hearing-the-call/ee726499-68f7-4fb3-a3f0-6e29811ea3d9/

Evidence grade: **B**, contemporaneous observation + first-person testimony.

Cross-national common mechanism:

```text
personal prepaid credential + temporary/shared telephone
```

allowed long-distance communication without owning the line or subscribing that line to long-distance service.

The China-specific evidence in this slice adds especially visible:

- 179xx IP-access codes;
- 201-campus-card nesting;
- operator/merchant public phone bars near migrant and student concentrations;
- coexistence with rapidly expanding mobile telephony.

Current evidence does **not** justify calling those features globally unique.

---

## 10. Ordinary-life payoff for the companion repository

The companion `how-people-lived` research question is not “when was VoIP invented?” It is:

> what had to be true for a student, migrant worker or traveler to live far from family without owning a home telephone or personal mobile phone?

This topology added a middle state between no real-time contact and personal-mobile reachability:

```text
I do not own the terminal
but I can carry the right to use a long-distance service
```

That is a genuine life-route change because it reduces the communications cost of:

- studying in another city;
- living in collective accommodation;
- temporary migrant work;
- traveling without a household subscription;
- maintaining family ties before universal personal mobile access.

But it also preserves an asymmetry:

```text
cheap outbound contact
!=
personally addressable inbound reachability
```

A walk-in caller can contact family without automatically becoming continuously reachable by family.

---

## 11. Evidence table

| Claim | Evidence | Grade | Confidence | Boundary |
|---|---|---:|---:|---|
| 1999 IP-phone trials used 17900/17910/17920 and RMB 0.30/min domestic long distance | *People's Daily* 1999-04-28 | B | high | regulator announcement via press |
| Unicom fixed-line users could dial 17910 then card no./password/destination | ZOL / BYD 2000-06-12 | B | high | product instructions, not packet capture |
| students used 201-card + IP-card nested dialing to lower cost | *Beijing Times* 2003-07-23 | B | medium-high | interview-based, not survey |
| operator phone bars targeted migrant / student dense areas and construction sites | *Yangtze Evening Post* 2003-07-11; ChinaByte 2003-12-02 | B | high for existence / targeting | no national usage denominator |
| a university preserved 2003-dated CERNET/IP-phone operational instructions | current HTU legacy page | A-ish content / current representation | high for content existence | not verified 2003 capture |
| some network phone cards used Web purchase + PC audio endpoint | *New Express* 2002-07-05 | B | high | do not generalize to all IP cards |
| by 2008 IC booths had declined while phone bars retained some use | *Information Times* 2008-10-16 | B | medium-high | Guangzhou local slice |
| U.S. prepaid cards similarly served users lacking own line/long-distance subscription | FTC 1997; WP 2001 | A/B | high | overseas comparison, not China evidence |

---

## 12. Hindsight risks

Do **not** write:

- “1999 Chinese consumers were already making Internet calls from PCs”;
- “IP phone user = Internet user”;
- “IP phone card = Web account”;
- “phone bar = Internet cafe”;
- “public phone availability = personal inbound reachability”;
- “all 179xx products used the same gateway or authentication architecture”;
- “current 2003-dated university page = original 2003 HTML/DOM/charset.”

The safest formulation is:

> IP-based carrier transport entered ordinary long-distance communication through several user-facing surfaces, including ordinary telephones, prepaid cards, campus systems, public phone shops and, in some products, PCs/Web distribution. Browser use was neither necessary nor universal.

---

## 13. Artifact status and negative result

### Verified in this slice

- multiple contemporaneous media descriptions of access numbers, tariffs and user workflows;
- a current institutional legacy page carrying dated 2003 campus IP-phone operating instructions;
- contemporaneous evidence of a distinct 201-card/IP-card nested workflow;
- contemporaneous evidence of public phone bars as a migrant/student communication interface.

### NOT achieved

This slice did **not** obtain:

- a verified 1999–2003 Wayback capture of China Telecom `17900`, China Unicom `17910`, or Jitong `17920` help pages;
- capture datetime + historical HTTP status + original charset + period DOM for an operator card page;
- original IVR audio/prompts;
- a physical card scan with readable period instructions and provenance;
- public-phone-bar billing client software / screenshots;
- gateway configuration or packet-level evidence tying a specific user session to a specific IP transport implementation;
- two historical captures of the same operator service page.

Therefore:

**M1 historical IP-telephone service capture: NOT ACHIEVED IN THIS SLICE.**

This does not mean no capture exists. It records only the current verification boundary.

---

## 14. Highest-value next artifacts

1. China Telecom / Unicom / Jitong period IP-card scans and envelopes;
2. original 17900 / 17910 / 17920 user manuals or operator help captures;
3. university 201 telephone handbooks and student BBS instructions;
4. phone-bar billing software manuals/screenshots;
5. historical IVR prompt recordings;
6. two time points on one operator's public help pages showing transition from card/PIN to direct-dial account binding;
7. evidence for whether and how public phone-bar users could receive callbacks or messages.

The last item is especially important for life history, because it tests the distinction between **being able to call home** and **being personally reachable from home**.
