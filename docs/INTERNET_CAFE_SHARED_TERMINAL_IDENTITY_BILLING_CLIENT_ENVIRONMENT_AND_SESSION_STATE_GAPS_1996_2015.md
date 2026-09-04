# Internet-café shared-terminal, identity, billing, client-environment and session-state gaps, 1996–2015

Status: research note / evidence-model extension  
Repository scope: **Chinese Web / Chinese Internet access environment, approximately 1995–2015**  
Cross-project companion: `tmzncty/how-people-lived/topics/shared-terminal-internet-access-place-bound-connectivity-and-device-optionality-china-1987-2023.zh-CN.md`

## Why this belongs in Old Web Archaeology

A historical webpage does not tell us **where or on what machine it was actually seen**.

For a large part of the Chinese old-Web period, some users accessed QQ, portals, forums, blogs, email, games and search engines from shared Internet-café computers rather than from a stable personal PC.

That creates an archaeological problem different from ordinary page preservation:

> **page survival ≠ historical access-environment survival.**

A Wayback capture may preserve HTML from 2005 while losing almost everything about the ordinary user's real access stack:

- which café;
- which terminal;
- which Windows build;
- which IE version;
- which Chinese IME and fonts;
- Flash / ActiveX / Java state;
- local proxy/cache;
- LAN topology;
- diskless vs local-disk client;
- restore-card behavior;
- billing session;
- identity-card / membership-card state;
- whether there was a queue for a machine;
- whether a user left files or credentials on the terminal.

This note therefore models the **shared-terminal access state** rather than attempting to reconstruct a specific person's browsing history.

Privacy rule: do **not** seek, publish, correlate or reconstruct historical identity-registration logs, real ID numbers, exact user session histories, account passwords, private chat logs or deleted personal files.

---

# 1. Scope boundary

This repository remains focused on the Chinese Web and access environment around **1995–2015**.

The global prehistory of public network access, ARPANET, Minitel, British cybercafés and the ordinary-life comparison belong mainly in `how-people-lived`. They can be linked here when they clarify a mechanism, but they do not expand this repository into a world cybercafé history.

Likewise, China's pre-1994 research/academic networking is relevant only as a boundary condition:

> limited research / mail connectivity before 1994 must not be mistaken for ordinary public café access.

The shared-terminal archaeology begins where public/commercial Internet use becomes observable in the Chinese Web era.

---

# 2. Minimal state machine

A usable Internet-café access session should not be compressed into `user enters café → online`.

A more defensible state chain is:

```text
venue exists
→ venue is legally/operationally open
→ user reaches venue
→ seat/terminal is available
→ identity / membership / temporary-card requirement is satisfied
→ money / balance / prepaid state permits access
→ terminal is assigned
→ local management client unlocks terminal
→ terminal boots into a specific local image
→ LAN is up
→ upstream Internet access is up
→ browser / IM / game / other client is usable
→ user logs into a platform account
→ activity occurs
→ local/downloaded/uploaded state may be created
→ platform logout may or may not occur
→ venue billing session ends
→ terminal may be restored / rebooted / reimaged
→ local traces may persist, be centralized, or disappear
```

Each arrow is a potential historical gap.

A page capture proves almost none of the later states.

---

# 3. Evidence baseline

## 3.1 Shanghai, 1998: public access was already a distinct business category

A contemporaneous *China Reading Weekly / 中华读书报* report dated **1998-08-26** described approximately 400 registered Internet cafés in Shanghai after local normalization measures. It described the early Shanghai venue “威盖特,” falling hourly prices, membership-card practices and household-computer ownership as a competitive pressure.

Source:
- https://www.gmw.cn/01ds/1998-08/26/GB/213%5EDS3505.htm

Evidence grade: **A/B contemporary press**.  
What it proves: public Internet-access venues and a paid-hour access market were socially observable in 1998 Shanghai.  
What it does not prove: exact nationwide first-café chronology, any particular venue's HTML, client OS, browser version, billing software or LAN architecture.

### Archaeology consequence

The historical object is already two-layered:

1. the **public Web** being accessed;
2. the **local access service** mediating the user to that Web.

Only the first layer is routinely captured by web archives.

---

# 4. Regulation makes the physical terminal part of the digital record

The official consolidated text of the `互联网上网服务营业场所管理条例` states that it was promulgated in 2002 and revised in 2011. The text defines commercial public Internet-access venues and includes technical/record requirements relevant to old-Web interpretation.

Official source:
- https://www.cac.gov.cn/2011-01/09/c_133158959.htm

Evidence grade: **A normative text**, with version caveat.  
Version caveat: the accessible page is a consolidated 2011-revised text. For claims about exact 2002 wording, retrieve the 2002 gazette/original version before asserting no-change continuity.

The consolidated text states that:

- consumer computers in such venues must connect through a **LAN** rather than each directly connecting to the Internet;
- venues must implement management technical measures;
- operators must verify/register valid user identity documents and record Internet-use information;
- registration and record backups must be retained for at least 60 days.

This matters because the access venue is not merely a dumb pipe.

It is simultaneously:

- a network edge;
- a managed LAN;
- an identity interface;
- a terminal-allocation system;
- a billing system;
- a record-retention system.

---

# 5. 2004 Nanjing: identity subject, terminal subject and platform subject are not the same object

A **2004-09-30** *Yangtze Evening News* report described Nanjing's rollout of a real-name card system. Users were expected to obtain an access card using an identity document, swipe before going online, and have their identity checked. The report said the system recorded identity information, access time and the machine number.

Contemporaneous source:
- https://tech.sina.com.cn/i/2004-09-30/1119434480.shtml

Evidence grade: **B contemporaneous local reportage**.  
Scope limit: one municipal rollout; do not generalize implementation fidelity to every Chinese café.

The resulting identity stack can be modeled as:

```text
legal person
→ presented identity document
→ venue access-card / temporary-card subject
→ billing/session record
→ assigned machine number
→ platform account(s)
→ public nickname / avatar / post
```

These must never be merged.

### New gap: operator / identity / account gap

A historical forum post can tell us the username that authored a message. It does not normally prove:

- which legal person was using the machine;
- whose café access card was used;
- whether the café verified the card correctly;
- which physical machine produced the request;
- whether the platform account itself was shared.

Therefore:

> **platform identity ≠ physical-terminal operator ≠ venue-registered identity.**

This is especially important when researching old BBS / forum pseudonyms. Do not attempt to bridge the layers by deanonymizing users.

---

# 6. 2004 Nanjing: restore systems can erase one class of history while another system is required to retain it

A **2004-12-18** Nanjing report said local enforcement found cases in which installed restore cards interfered with the required retention of 60-day access records.

Source:
- https://news.sina.com.cn/c/2004-12-18/11544560191s.shtml

Evidence grade: **B contemporaneous reportage**.

This is unusually valuable technical evidence because it shows two historical state-management goals colliding:

### Goal A: ephemeral client state

A café benefits when a terminal can return to a known clean configuration after each user:

- malware and accidental changes disappear;
- software settings reset;
- local clutter is removed;
- maintenance becomes cheaper;
- the next customer receives a predictable environment.

### Goal B: persistent management / compliance state

A management system may need to preserve:

- identity registration;
- access time;
- terminal mapping;
- security / administrative logs.

These should not be treated as the same storage layer.

### New gap: local-restore / centralized-record gap

A restored local Windows desktop may erase a downloaded file or browser history while a central café server still retains some session metadata.

Conversely, a central record requirement does **not** prove the browser's local cookies, cache, passwords or downloads were preserved.

So old-Web research should avoid two opposite assumptions:

> “还原卡 erased everything.”

and

> “60-day records mean the café retained the user's full browsing contents.”

Neither follows from the evidence.

---

# 7. 2006–2008: diskless / centralized infrastructure changes what a 'historical PC' means

Contemporaneous Chinese IT industry material from 2006 discussed Internet-café diskless workstations: client machines without ordinary local disks could boot and obtain system/data state over the network from central storage or servers.

Sources / B promotional-industry evidence:
- https://tech.sina.com.cn/h/2006-03-30/1533884268.shtml
- https://tech.sina.com.cn/h/2006-08-14/092567166.shtml

A 2006 technical forum discussion also describes RPL/PXE-style network boot mechanisms in the context of diskless café machines:
- https://netpcforum.org/t/%E8%AE%A8%E8%AE%BA%E6%97%A0%E7%9B%98%E7%BD%91%E5%90%A7%E7%9A%84%E7%94%B5%E8%84%91%E6%98%AF%E6%80%8E%E4%B9%88%E5%B7%A5%E4%BD%9C%E7%9A%84/112015

Evidence grade: **B contemporary technical discussion**; not proof of adoption rate.

A 2008 server-solution article depicts a larger café architecture in which different servers may serve movie/VOD, game/update and other functions.

Source / B contemporary technical-industry article:
- https://news.mydrivers.com/1/115/115440.htm

### New gap: physical box / logical system image gap

When a customer sat at “machine 37,” the historical experience might have depended less on that box's local disk than on:

- central boot image;
- image version;
- server availability;
- LAN switch / topology;
- shared update cache;
- game/update server;
- local proxy or content server.

Therefore an archaeological reconstruction should not infer the historical software environment from a surviving café PC chassis alone.

A surviving terminal and a surviving server image are different evidence objects.

---

# 8. Access-place state gaps

## 8.1 Venue-exists gap

A business directory or news item can prove a café existed at a location.

It cannot prove:

- it was open on a specific day;
- the Internet uplink worked;
- a seat was available;
- the listed price was still current.

## 8.2 Legal-venue / actual-venue gap

A licensed-venue list does not prove that unlicensed venues did not operate. A report on an unlicensed café does not prove the whole sector was unlicensed.

Keep license state separate from physical operation state.

## 8.3 Queue / terminal-availability gap

A venue with 100 PCs can still be unusable to the 101st customer.

Historical opening hours and seat counts are not enough; queue and occupancy are transient states rarely archived.

## 8.4 Price / realized-cost gap

An advertised hourly price may differ from:

- member price;
- night package;
- prepaid discount;
- minimum charge;
- temporary promotion;
- actual time billed.

Do not use one surviving sign as a full price distribution.

---

# 9. Identity and billing gaps

## 9.1 ID-registration gap

`rule requires ID registration`  
≠ `venue system was installed`  
≠ `operator actually verified identity`  
≠ `presented ID belonged to operator`  
≠ `record was correctly retained`.

The 2004 Nanjing report itself includes concerns that users might use someone else's card or that some operators might ignore rules for business reasons.

Source:
- https://tech.sina.com.cn/i/2004-09-30/1119434480.shtml

So compliance state is empirical, not inferable from regulation.

## 9.2 Membership-card gap

A historical membership card proves enrollment at some time. It does not automatically prove:

- current balance;
- access on a given date;
- card ownership continuity;
- which terminal was used.

## 9.3 Billing-session gap

A café bill/session can theoretically provide:

- start time;
- stop time;
- machine number;
- price rule;
- account/card state.

Public Web archives almost never preserve authenticated billing databases. Therefore the most important ordinary-life time evidence is usually missing.

## 9.4 Payment-state gap

`user inserted/paid money`  
≠ `account balance updated`  
≠ `terminal unlocked`  
≠ `session continued for advertised duration`.

---

# 10. Client-environment gaps

A historical café session depends on a local client environment.

Record separately where evidence exists:

- OS and service pack;
- browser and version;
- default homepage;
- proxy setting;
- DNS behavior;
- screen resolution;
- fonts;
- Chinese input methods;
- Flash version;
- Java/JVM;
- ActiveX controls;
- QQ / MSN / UC / game client versions;
- antivirus / firewall;
- download manager;
- archive/unzip software;
- local drive letters / permissions;
- USB / floppy / optical-drive availability;
- diskless or local-disk architecture;
- restore system / reboot semantics.

### Browser capture gap

A Wayback page loaded in modern Chromium does not establish how it rendered in the café's historical IE environment.

Use this repository's existing browser-environment contract:

- historical browser claims require evidence;
- modern rendering is not historical proof;
- missing plugins must remain missing unless a reconstruction is explicitly labeled;
- oldweb.today / VM replay is preferred to inventing a new emulator.

---

# 11. Platform-login / local-machine gap

The user can take an online identity across physical machines, but some state stays local.

Separate:

```text
platform-side state
- account
- friends
- messages
- posts
- server-side mail
- game character / inventory

from

local-machine state
- cookies
- saved password
- browser cache
- downloaded attachment
- local chat log
- screenshots
- game patches
- temporary files
```

This distinction is crucial to ordinary old-Web use.

A QQ account might persist for ten years while every physical machine used to access it disappears.

### New concept: identity outlives terminal

> **online identity portability can precede personal-device ownership.**

This explains why a user's social graph may be historically continuous even when the access environment changes from school lab to café to workplace to home PC.

Old-Web archaeology should therefore avoid treating “user's computer” as a stable unit unless there is evidence the computer was actually personally owned and continuously used.

---

# 12. Logout and privacy gaps

Shared machines produce risks that private machines do not.

Potential states include:

- user closes browser but remains logged in;
- browser stores credentials;
- QQ/chat client stores local history;
- downloaded files remain on disk;
- restore system deletes them at reboot;
- central file server retains them;
- next user can access local remnants;
- administrative monitoring records metadata elsewhere.

### Privacy rule for this repository

Do **not** search for or reproduce abandoned café-client files, credential stores, chat logs or identifiable session records simply because they survive in an archive, disk image or leaked dataset.

The research value is the **state model and preservation bias**, not deanonymizing ordinary users.

If a historical disk image contains personal material, preserve only the minimum metadata necessary to document the environment unless explicit lawful/public archival authorization exists.

---

# 13. Restore-state gap

After a session ends, at least four different outcomes are possible:

1. local state persists unchanged;
2. selected paths are cleaned;
3. reboot restores a reference image;
4. diskless client discards local session state and reboots from server state.

A café advertisement saying “每次重启还原” is not enough to prove which data paths were actually reset.

For reconstruction, record:

- product / version if known;
- whether restore occurred on reboot or logout;
- protected partitions;
- writable partitions;
- central roaming/profile behavior;
- exceptions for downloaded files;
- evidence source.

Do not generalize one restore product across all cafés.

---

# 14. Network-edge gaps

The regulation's LAN requirement makes the café a local network environment.

Potential archaeology fields:

- ISP / uplink provider;
- fixed/dynamic public address state;
- NAT/proxy behavior;
- LAN address space;
- switch speed;
- bandwidth sharing;
- local cache;
- local game/VOD server;
- DNS server;
- upstream outage;
- traffic shaping;
- per-client restrictions.

### Public-IP / user gap

A server log may show a café's public IP, not an individual terminal. Multiple users can share the same upstream address.

Therefore:

> **server-side IP ≠ individual user identity.**

This is another reason not to retroactively identify old forum users from IP evidence without a legitimate, necessary research basis.

---

# 15. Temporal gaps

## 15.1 Capture time vs access time

A 2006 website capture says what the archive saw then. It does not prove what a café customer saw that morning.

The customer may have encountered:

- a different cached page;
- a DNS failure;
- blocked popup/ActiveX;
- a stale local proxy object;
- a different browser-specific layout.

## 15.2 Advertised opening time vs actual session time

Opening hours do not prove a venue accepted users continuously. Maintenance, power loss, full occupancy or local enforcement can interrupt access.

## 15.3 Version drift

An Internet café can update dozens or hundreds of clients centrally. A one-week image change can affect every customer at once.

This makes software-image version a meaningful historical datetime, not merely a technical detail.

---

# 16. 2008–2010 adoption shift: the same user could have several access routes

CNNIC's 2008–2009 youth report says that in 2008, 57.5% of youth Internet users had used an Internet café within the relevant six-month window; among rural youth Internet users, the share was 65.4%.

Source / A institutional survey:
- https://www.cnnic.cn/n4/2022/0401/c116-890.html

CNNIC's 2010 youth report says the café-use share fell to 48.1%, while home and school access increased and mobile access rose strongly.

Source / A institutional survey:
- https://www3.cnnic.cn/n4/2022/0401/c116-841.html

For old-Web interpretation, this means a historical user should not be assigned one fixed “access mode.”

A single person could use:

```text
home PC on Monday
school lab on Tuesday
Internet café on Friday night
mobile browser on the weekend
```

### New gap: access-route ambiguity

Public posts rarely disclose the access venue. Therefore a 2008 BBS post cannot be labeled “home Internet culture” or “Internet-café culture” unless there is independent evidence.

The platform does not encode the full access place.

---

# 17. Why archive survival is structurally biased

Public Web archives are good at preserving:

- café promotional homepage;
- price page;
- news report;
- public regulation;
- product advertisement for management software;
- public forum discussion of diskless setups.

They are much worse at preserving:

- authenticated billing UI;
- balance database;
- terminal-assignment state;
- live occupancy;
- identity-check workflow;
- local boot image;
- internal DHCP/DNS/proxy configuration;
- private logs;
- user local files;
- exact restore operation;
- real session outcome.

This creates a predictable distortion:

> **the public story of the café survives better than the user's actual café session.**

A future historian can easily find “this café had 200 machines and offered QQ/game access” while being unable to answer “did user X actually get a seat, log in successfully and carry their file home?”

---

# 18. Archaeology checklist for a historical Internet-café object

When a café/site/software artifact is studied, capture the following without overclaiming.

## Venue identity

- name;
- address if already public and historically necessary;
- active dates;
- license/public-registration evidence if relevant;
- whether source is contemporary or retrospective.

## Public Web surface

- original URL;
- capture URL;
- capture datetime;
- page title;
- charset;
- linked assets;
- missing resources;
- declared browser/plugin assumptions.

## Access model

- hourly / package / membership price evidence;
- business hours evidence;
- identity requirement evidence;
- age/access restriction evidence;
- terminal count evidence;
- queue evidence, if contemporaneous and explicit.

## Network / terminal environment

- OS/browser if known;
- local disk / diskless;
- restore technology;
- LAN / server architecture;
- management/billing software;
- locally hosted VOD/game/update services;
- upstream provider.

## State gaps

Always state what is **not** known:

- actual occupancy;
- actual session;
- actual user identity;
- exact balance/payment;
- exact client image;
- whether logout occurred;
- whether local files survived.

---

# 19. Evidence-grade examples

### A — original / contemporaneous primary

- original regulation/gazette;
- contemporaneous software manual;
- archived venue page;
- original client/server configuration document;
- historical software installer with verifiable provenance.

### B — near-contemporary secondary / technical reporting

- newspaper visit to a café;
- IT press description of diskless architecture;
- local report on real-name access-card deployment.

### C — later recollection

- “2008 年大学旁边周末一定要占座” remembered in a 2013 article;
- oral history of using QQ in an Internet café.

Useful for lived routine, not enough to establish exact configuration or adoption rates.

### D — reconstruction / inference

- recreating a likely Windows XP + IE6 café client image;
- inferring LAN topology from a later product diagram;
- estimating software versions from screenshots.

Must be explicitly labeled reconstruction.

---

# 20. Negative result in this research slice

This round **did not obtain and verify**:

- a privacy-safe authenticated billing/session capture from a specific 1998–2010 café;
- a complete historical café client disk/server image with clear provenance and dates;
- a full dated mapping of OS + IE + IME + Flash + QQ/game versions for an ordinary venue;
- a continuous occupancy / queue log;
- a public, ethically usable person-level session ledger.

Therefore this note does **not** claim to reconstruct a representative 2005 Internet-café desktop.

It also does not infer exact HTML/DOM of café management software from current vendor pages.

“Cannot reliably recover the actual session” is a valid archaeology conclusion.

---

# 21. New reusable state gaps

Add the following to the repository's general gap vocabulary:

- `venue-exists gap`
- `legal-operation gap`
- `queue / terminal-availability gap`
- `identity-registration gap`
- `membership-card gap`
- `billing-session gap`
- `payment / balance-posting gap`
- `terminal-assignment gap`
- `client-unlock gap`
- `boot-image version gap`
- `diskless / local-disk gap`
- `LAN / upstream-connectivity gap`
- `browser / plugin / IME version gap`
- `platform-login gap`
- `local-file persistence gap`
- `logout gap`
- `restore-state gap`
- `central-record / local-state gap`
- `shared-terminal privacy gap`
- `access-route ambiguity gap`

These are useful beyond Internet cafés. They apply to school computer rooms, library terminals, hotel business centers and other shared-computing environments, but this repository should only extend to those objects when they materially illuminate the 1995–2015 Chinese Web.

---

# 22. What this changes about Old Web Archaeology

The old Web was not experienced only through old websites.

For many users, the historical Web arrived through **temporary machines**.

That changes the archaeological unit from:

> `URL + capture datetime`

into, when evidence allows:

> `URL + capture datetime + browser/client image + access place + session state + preservation boundary`

The new rule is:

> **Do not reconstruct an ordinary user's old-Web experience from the archived page alone when the access environment was a managed shared terminal.**

A page can survive while the whole local world that made it usable—IE version, font, QQ client, restore card, diskless image, billing session, LAN and physical place—has disappeared.
