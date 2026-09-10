# Online-game portals, clients, patches, accounts, real-name gates, servers, characters, guilds and world-state gaps, 1999–2015

> Scope: Chinese-language old Web and adjacent client/server infrastructure, approximately 1999–2015.  
> Cross-repository life-history package:  
> https://github.com/tmzncty/how-people-lived/blob/main/topics/networked-games-persistent-worlds-guild-schedules-character-continuity-and-life-course-china-1995-2026.zh-CN.md

## 0. Research boundary

This note is **not** a general history of Chinese online games, a catalog of MMORPGs, or a commercial history of Shanda / The9 / NetEase / Tencent. It treats the online game as an archaeological object whose public Web shell, local executable client, authentication account, real-name record, payment entitlement, server realm, character database, guild/social graph and live world state have different authorities and different survival histories.

It keeps the repository's main object inside the Chinese old-Web period. Pre-Web MUD material is used only to clarify the technical genealogy; broad global comparison belongs in `how-people-lived`.

The central warning is:

`archived game website != preserved game service != preserved player world`.

A researcher may recover a 2007 official home page, a patch download and a guild forum while still being unable to determine whether a particular realm was reachable, whether a character existed, whether a prepaid entitlement was valid, or what players were doing inside the world at that moment.

---

## 1. Object ontology: “the game” is many independently versioned authorities

At minimum, separate:

1. **game title / product identity** — the continuing commercial/cultural name;
2. **operator / publisher** — the entity currently authorized to run the service in a territory;
3. **official portal** — public Web pages for news, account links, support and marketing;
4. **download page** — Web record advertising a client or patch;
5. **installer / client build** — exact executable bytes and installed files;
6. **patcher / launcher** — client-side component that may contact dynamic endpoints before login;
7. **patch manifest / CDN object** — version-specific remote dependency;
8. **game account** — authentication namespace, not identical to a human;
9. **real-name / identity record** — identity authority used for age, security or policy enforcement;
10. **phone/email binding** — recovery/contact credential, potentially changed independently of character state;
11. **prepaid card / point code** — physical or digital credential representing payment value;
12. **billing account / entitlement** — server-side authoritative playable time/value;
13. **authentication service**;
14. **realm / shard / server group** — a named world/service partition;
15. **realm status** — online, maintenance, closed, queueing, transfer-only, etc.;
16. **character record** — identity, level, inventory, achievements/progress and other game-specific fields;
17. **guild membership record**;
18. **friend/social graph record**;
19. **instance/raid state** — short-lived cooperative world copy/state;
20. **in-game chat / mail**;
21. **guild Web/forum identity** — may use character names but is not the authoritative game database;
22. **external IM/voice layer** — QQ, YY, TeamSpeak and similar systems used to coordinate play;
23. **world rules/content version** — what NPCs, maps, balance and quests exist at time T;
24. **operator migration/archive artifact** — exported or transferred data during service handoff;
25. **actual human presence** — a person at a keyboard/device, not derivable from account metrics alone.

Do not collapse these into “game X was online.”

---

## 2. Core state machines

### 2.1 Access path

`game known`
→ `client source discovered`
→ `correct installer obtained`
→ `client installed`
→ `required patch/build reached`
→ `account authenticated`
→ `identity/age gate passed`
→ `billing entitlement accepted`
→ `realm reachable`
→ `character list loaded`
→ `character entered world`
→ `other players/social state reachable`
→ `actual session took place`.

Each arrow can fail independently.

Preserve at least:

- `game-title / current-operator gap`
- `portal-live / game-service-live gap`
- `download-page / client-binary gap`
- `client-installed / patch-compatible gap`
- `patch-compatible / authentication-success gap`
- `account-exists / account-usable gap`
- `account / real-person gap`
- `submitted-realname / verified-realname gap`
- `verified-identity / current-operator-recognition gap`
- `authenticated / entitlement-valid gap`
- `entitlement-valid / realm-online gap`
- `realm-online / character-load gap`
- `character-load / actual-human-play gap`
- `server-online / desired-realm-online gap`
- `desired-realm-online / queue-cleared gap`
- `world-access / guild-availability gap`.

### 2.2 Prepaid/payment path

`physical/digital card purchased`
→ `code exposed/entered`
→ `code accepted`
→ `account credited`
→ `playtime/points available`
→ `playtime consumed`
→ `remaining balance`.

Therefore:

`card sold != code redeemed != account credited != time consumed`.

### 2.3 Real-name/time-control path

`human civil identity`
→ `identity data submitted`
→ `verification authority returns status`
→ `account classified by age`
→ `current calendar time compared with rule`
→ `game server grants/reduces/denies service`.

Therefore:

`real-person age != entered ID age != verified account age != actual operator at keyboard`.

### 2.4 Operator-transfer path

`old operator service stops`
→ `account namespace mapped`
→ `unused balance mapped/refunded`
→ `character DB transferred/restored`
→ `guild/social records restored`
→ `new operator authentication works`
→ `new realm opens`
→ `player verifies continuity`.

An operator transfer can succeed at some stages and fail at others.

---

## 3. Pre-Web boundary: MUD proves the service/client split predates the browser

A 1984 contemporaneous article about the Essex University MUD, later archived by Richard Bartle, records outside players connecting after midnight to a DEC-10; players needed a computer and had to pay telephone-call costs. Up to 36 people could share the textual world simultaneously.

Source (global prehistory; A-content / later personal archive carrier):  
https://mud.co.uk/richard/wivjun84.htm

This is outside the repository's main geographic/time scope and is not evidence about Chinese mass adoption. Its narrow archaeological lesson is essential:

**networked game world != Web page**.

The service can predate HTTP and can be reached through a terminal/protocol session. Therefore a Web-first archive strategy will systematically under-represent the genealogy of persistent multiplayer worlds.

For China, the repository's existing prehistory boundary remains controlling: international e-mail/research connectivity existed before 1994; full-function Internet connection dates to April 1994; public/commercial access expanded after 1995; 1997 CNNIC still measured a relatively small national Internet population. Early Chinese MUD material should therefore be treated as a campus/early-user boundary, not proof of household-scale Internet gaming.

A 2005 retrospective interview on `侠客行` dates the overseas Chinese MUD project to 1995; later community histories place a domestic Peking University server in 1996. These are B/C sources and should not be used as precise mass-user counts.

Sources:  
https://tech.sina.com.cn/i/2005-06-25/1540645859.shtml  
https://wiki.pkuxkx.net/wiki/nianjian/1990s

---

## 4. 1999–2006: public Web was only one surface of the commercial game stack

### 4.1 Internet cafés and prepaid retail were part of the access protocol in practice

Shanda's 2004 SEC filing states that it estimated a nationwide distribution/payment network of more than 317,000 retail points, over 40% Internet cafés; it also described a server network of roughly 10,100 servers plus 2,300 annex units and a 24-hour call center. These are company claims in a regulatory filing, not independent population estimates.

Source (A/company filing):  
https://www.sec.gov/Archives/edgar/data/1278308/000114554905000033/u99471fv1.htm

A later The9 filing explains that due to limited online-payment availability, play time was distributed primarily through prepaid cards and online points, with Internet cafés acting as important resellers; customers could also play at home.

Source (A/company filing):  
https://www.sec.gov/Archives/edgar/data/1296774/000114554908001189/h02254e20vf.htm

This creates an old-Web warning:

`game portal visible on Web != transaction originated on Web`.

A historically normal workflow could be:

`portal/advertisement/friend`
→ `Internet café already has client installed`
→ `cash handed to café/retailer`
→ `prepaid code or eSales point credited`
→ `client login`
→ `server session`.

Web archive can preserve the portal while missing the most common physical payment or access step.

### 4.2 Installed-at-café availability is its own state

A game could exist commercially but not be installed on the café machine a user had access to. Game operators explicitly competed for presence on Internet-café PCs because disk space and local administration limited how many games could be featured.

Therefore add:

- `commercially-launched / café-installed gap`
- `café-installed / current-client-version gap`
- `client-present / local-user-permission gap`
- `Internet-access-available / desired-game-available gap`.

This is another reason not to reconstruct ordinary use from official site availability alone.

---

## 5. Client and patch state: the preserved installer is not the preserved service

MMORPG clients are unusually dependent on a live compatibility relation between local files and server-side version state.

Preserve:

`client binary survives != launcher can update != auth protocol accepted != world server speaks that build`.

Potential dependencies include:

- patch manifest endpoint;
- CDN paths;
- launcher self-update;
- certificate/TLS behavior;
- anti-cheat module;
- account service;
- realm list;
- region/operator-specific executable;
- registry/configuration state;
- runtime/DirectX/driver requirements.

A bit-perfect 2005 client ISO can therefore be a strong software artifact while still being unable to recreate a 2005 session.

Do not execute preserved old clients on an ordinary host merely because they are historically interesting. They may contain vulnerable launchers, obsolete drivers, anti-cheat components or malicious/tampered redistribution. Prefer hashing/static inspection and isolated environments.

---

## 6. 2007: real-name information becomes executable service authority

A July 16, 2007 contemporaneous China Internet Society article reports mandatory anti-addiction rollout, including `World of Warcraft` real-name verification. It describes warnings/reduced rewards after three hours for minors and says account information was submitted for public-security verification.

Source (A/B contemporaneous implementation report):  
https://www.isc.org.cn/article/9899.html

Archaeologically, the key change is not merely a policy notice. Civil identity became part of a game-state decision path:

`ID data`
→ `verification response`
→ `age classification`
→ `server-side time/reward rule`.

Add:

- `registration-form accepted / identity-authority verified gap`
- `identity-authority verified / age-policy applied gap`
- `account-age / current-human-operator gap`
- `policy-described / client-enforced gap`
- `client-enforced / non-circumventable gap`.

A preserved 2007 anti-addiction notice proves the rule was announced/implemented; it does **not** by itself prove that a particular player's submitted identity was true or that circumvention was impossible.

---

## 7. Guild Web pages are coordination artifacts, not the authoritative guild

A 2009 contemporaneous report on a `World of Warcraft` guild reproduces a guild-Web notice left from 2007: raids every Friday/Saturday at 19:30, members asked to be online on time, and forum applicants asked to use their actual in-game character name for verification. The article also describes attendance discipline, a student player's fixed evening raid schedule and offline meetups.

Source (A/B contemporaneous media observation/interview; preserved republication):  
https://www.cnbeta.com.tw/articles/tech/91824.htm

This creates a useful identity stack:

`forum account`
↔ `declared character name`
↔ `authoritative character record`
↔ `authoritative guild membership`
↔ `actual human`.

They may be linked socially, but they are not the same object.

Preserve:

- `guild-homepage exists / guild-currently-active gap`
- `forum-ID / character-record gap`
- `character-name / unique-human gap`
- `forum-roster / live-guild-roster gap`
- `raid-notice / actual-attendance gap`
- `scheduled-start / instance-created gap`
- `guild-online-coordination / offline-friendship gap`.

This matters because old-Web archives are relatively good at preserving guild pages and forum posts. They can tempt researchers to treat those pages as a direct dump of the in-game social graph. They are not.

---

## 8. 2009 operator transfer: a natural experiment in layered authority

The 2009 mainland `World of Warcraft` operator transition provides a strong state-separation case. A contemporaneous July 31 report says the service reopened after a 53-day shutdown. A player checked both his unused prepaid balance and account continuity; customer-service statements discussed transfer/refund handling.

Source (A/B contemporaneous newspaper):  
https://mqjwb.tidenews.com.cn/epaper/article/2009-07-31/31597

The same report interviews a 28-year-old game-boosting worker who coordinated paid orders through guild members and whose income fell during the shutdown. This is evidence that server availability could affect informal labor as well as leisure; it is an individual case, not a labor-market prevalence estimate.

Archaeologically, preserve separately:

- old operator account identifier;
- unused prepaid balance;
- refund claim;
- new operator account mapping;
- character data;
- realm mapping/name;
- guild membership;
- friend/social records;
- authentication credential;
- actual successful login after reopen.

Thus:

`balance migrated != character migrated`

and

`account record present != player has verified world continuity`.

A press release saying migration is complete is evidence of operator claim/state policy; a player's successful login is a different kind of evidence.

---

## 9. Metrics: online games are hostile to “user count” shortcuts

CNNIC's 2008 online-game report says the user population under its survey definition reached 55.5 million by year end; the report also describes age, education and payment characteristics.

Source:  
https://www3.cnnic.cn/n4/2022/0401/c121-866.html

Meanwhile company filings commonly report registered accounts, activated accounts, average concurrent users and peak concurrent users. These are not interchangeable.

Always ask which metric is being observed:

- registered account count;
- activated account count;
- accounts with any play in window T;
- paying accounts;
- average concurrent users;
- peak concurrent users;
- characters created;
- clients downloaded;
- forum accounts;
- page visitors;
- unique humans.

Hard rule:

`registered accounts != unique players`.

One person can own multiple accounts; one account can be shared; inactive accounts can remain registered; Internet-café/NAT environments complicate IP-based uniqueness; one account can contain multiple characters.

A headline saying “X million players” must be traced to the actual metric before reuse.

---

## 10. 2011–2015: client/server/platform boundaries become even more important

By this period, Chinese online-game life increasingly mixed:

- official Web portal;
- locally installed PC/mobile client;
- platform account;
- real-name service;
- payment SDK/provider;
- launcher/patcher;
- voice/IM;
- guild forum/QQ group;
- streaming/video site;
- secondary virtual-item/boosting market.

A perfect Web capture of the public portal can therefore miss almost every state needed to reconstruct actual play.

For this repository, the relevant end-state is not “the game industry became mobile.” It is methodological: **the old Chinese Internet cannot be reconstructed as HTML alone.** Network games make this especially obvious because the public Web is often only a shell around a private client/server world.

---

## 11. State gaps to preserve as first-class fields

### 11.1 Product / operator / portal

- `game-title / territorial-license gap`
- `license-holder / actual-current-operator gap`
- `operator-announcement / service-execution gap`
- `official-domain / live-game-service gap`
- `current-official-page / historical-operator gap`

### 11.2 Client / patch

- `download-page / exact-client-binary gap`
- `client-version-label / exact-bytes gap`
- `installed-client / patch-current gap`
- `patch-current / auth-protocol-compatible gap`
- `launcher-open / patch-endpoint-live gap`
- `archived-client / safe-execution-today gap`

### 11.3 Account / identity

- `account-record / human-person gap`
- `account-login / current-controller gap`
- `submitted-ID / verified-ID gap`
- `verified-ID / real-current-player gap`
- `phone-binding / civil-identity gap`
- `old-operator-login / new-operator-login gap`

### 11.4 Billing

- `prepaid-card-sold / code-redeemed gap`
- `code-redeemed / account-credited gap`
- `account-credited / playable-entitlement gap`
- `playable-entitlement / time-consumed gap`
- `unused-balance / refundable-balance gap`
- `refund-approved / money-received gap`

### 11.5 Server / world

- `service-brand-online / desired-realm-online gap`
- `realm-online / queue-cleared gap`
- `queue-cleared / character-loaded gap`
- `character-loaded / historical-world-state gap`
- `world-running / desired-instance-available gap`
- `instance-created / raid-completed gap`

### 11.6 Social layer

- `guild-page / guild-record gap`
- `forum-ID / character-ID gap`
- `character-ID / human-person gap`
- `guild-roster / actual-active-members gap`
- `friend-list / ongoing-relationship gap`
- `scheduled-raid / actual-attendance gap`
- `in-game-chat / QQ-or-voice-coordination gap`

### 11.7 Transfer / shutdown

- `service-shutdown / data-deletion gap`
- `data-export / authoritative-backup gap`
- `authoritative-backup / future-importability gap`
- `account-migrated / character-migrated gap`
- `character-migrated / guild-social-continuity gap`
- `provider-restored / player-life-course-restored gap`.

---

## 12. Archive asymmetries specific to network games

### 12.1 `Web-shell survival / world-state loss asymmetry`

HTML pages, news and guides are crawler-friendly. The live realm is a server-side mutable database/protocol state. A preserved home page can survive after every realm, character and chat record is gone.

`homepage captured != world captured`.

### 12.2 `client survival / server loss asymmetry`

Old installers and CDs may survive, sometimes bit-perfectly. Without compatible authentication, realm-list, patch and world servers, the executable cannot recreate the historical multiplayer experience.

`client preserved != service preserved`.

### 12.3 `character-description / character-authority gap`

A forum signature, screenshot or ranking page may say a character had a level/item/rank. The authoritative server database may no longer exist or may have changed immediately after the capture.

### 12.4 `public-guild / private-co-presence asymmetry`

Guild recruitment pages and schedules are public and archivable. What made the guild socially real—voice chat, whispers, attendance, conflict, joking, waiting for late members—is largely ephemeral/private.

Thus archives over-preserve **declared organization** and under-preserve **lived coordination**.

### 12.5 `static guide / volatile rule-state asymmetry`

A guide saying “boss X drops item Y” can survive while the game has already patched drop tables, class balance, raid size or server behavior. Always bind gameplay claims to version/build/date.

### 12.6 `shutdown-news / ordinary-continuity bias`

A 53-day outage, spectacular virtual-item sale or esports retirement is highly newsworthy. An office worker playing two ordinary evenings a week leaves far fewer searchable traces. Media-based reconstruction therefore risks exaggerating extreme intensity and crisis.

Call this **dramatic-case visibility bias**.

### 12.7 `metric survival / denominator loss`

A press release may preserve “38 million activated accounts” while the original methodology explaining activation, duplicate accounts, inactivity and measurement window disappears. Never retain the number without retaining the metric definition if possible.

---

## 13. Browser/client compatibility: do not invent a Web-only workflow

For any future historical capture, record separately:

- HTTP response / charset;
- HTML/JS/CSS dependencies;
- visible client download target;
- whether registration occurred on Web or in client;
- whether launcher used embedded browser/ActiveX/other helper;
- exact client build/date;
- patch endpoint and response, if recoverable;
- realm-list/auth endpoint, if legally and safely recoverable;
- whether the Web page was merely marketing/support.

Do **not** infer “IE6 required,” “ActiveX required,” `GB2312`, a particular launcher flow or an exact executable URL from generic knowledge of 2000s Chinese game sites. Evidence must be `exact product × exact date × exact workflow`.

---

## 14. Privacy and ethics

Game archaeology is unusually likely to expose persistent pseudonyms that can be linked back to real people. Do not unnecessarily republish:

- real names behind handles;
- ID-card numbers;
- phone/email recovery data;
- account credentials;
- private guild chat/whispers;
- IP/login logs;
- transaction histories;
- minors' identity data;
- private relationship or health information revealed in guild archives.

A public 2009 guild page may be technically crawlable today; that does not automatically justify re-aggregating every ordinary member's handle, old contact detail and offline identity.

Prefer reconstructing **state machines, page forms, public policies, client artifacts and anonymized life-history mechanisms** over deanonymizing players.

---

## 15. Evidence ledger for this slice

| Claim | Evidence type | Strength / caveat |
|---|---|---|
| Pre-Web multiplayer worlds depended on terminals, phone calls and scheduled host availability | 1984 contemporaneous MUD article in later Bartle archive | A-content/B-carrier; global prehistory only |
| Chinese early MUD existed in narrow early-Internet/campus contexts | 2005 retrospective creator interview + current community chronology | B/C; do not infer mass adoption or precise user counts |
| Commercial game access relied on Internet cafés, prepaid retail and large server networks | Shanda/The9 SEC filings | A company filings; scale values are operator claims |
| 2007 real-name/anti-addiction linked ID data to play rules | contemporaneous implementation report | A/B; rule presence does not prove non-circumvention |
| Guild Web pages coordinated fixed raid schedules and character-name identity mapping | 2009 contemporaneous interview/observed guild notice | A/B; one guild, not representative of all players |
| 2009 operator transition interrupted service for 53 days and required balance/account continuity | contemporaneous newspaper | A/B; good transaction-state case |
| Game skills could support informal boosting/equipment income | 2009 direct individual interview | A/B case; not prevalence estimate |
| 2008 game-user scale and characteristics | CNNIC specialized survey | institutional survey; keep population definition |

---

## 16. M1 / historical capture status

This slice identified strong contemporaneous locator leads and public sources for Chinese game portals, guild pages and operator notices, but it did **not** complete a verified historical Memento with all of:

- original URL;
- archive capture URL;
- capture datetime;
- HTTP status;
- charset/encoding;
- DOM/page structure;
- client/download link target;
- script/subresource dependencies;
- and a second comparison time where needed.

Therefore:

**M1 verified historical Chinese MMORPG portal/client/guild page Memento: NOT ACHIEVED IN THIS SLICE.**

This must **not** be rewritten as “the Wayback Machine did not preserve it.” `not found/verified in this run != did not exist/is not archived`.

A particularly valuable future M1 target would be one 2005–2009 game portal for which we can recover:

`historical portal page + exact client/patch locator + account/charge instructions + realm/server notice + second capture after a version/operator change`.

---

## 17. What this changes for old-Web archaeology

Network games make one methodological point unusually hard to ignore:

**the history of the Chinese Internet is not the history of Chinese Web pages.**

A player in 2007 might discover a game through a portal, buy time in a physical Internet café, launch a locally installed executable, authenticate through a private account service, have civil identity checked by another authority, enter a mutable realm, coordinate through a guild forum and QQ, talk over voice chat, then leave almost no public Web record of the actual evening.

The crawler is best at preserving the **door**. The socially important object was often the **room behind the door**, and that room existed only while a set of servers, databases, protocols and other people remained jointly available.

That is the central archaeological state gap of networked games.