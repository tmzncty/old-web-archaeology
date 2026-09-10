# Software-download portals, mirrors, binaries, installers, versions and bundling state gaps, 1997–2015

> Scope: Chinese-language old Web, approximately 1997–2015.  
> Cross-repository life-history package:  
> https://github.com/tmzncty/how-people-lived/blob/main/topics/software-acquisition-shareware-self-provisioning-and-toolchain-portability-china-1995-2026.zh-CN.md

## 0. Research boundary

This note is **not** a commercial history of Huajun, Skycn, Xunlei, FlashGet or all Chinese software portals. It treats software distribution as an archaeological object whose visible Web page, downloadable file, executable installer, installed runtime and license state may all have different authorities and different survival histories.

It also does not move this repository into a global shareware-history project. Pre-Web overseas material belongs mainly in `how-people-lived`; here it is used only where it clarifies why a Chinese old-Web download portal should not be treated as a self-contained invention.

The central warning is:

`download-page survival != binary survival != historical artifact identity != installability today`.

A researcher may recover a 2005 software description page and still know almost nothing about the exact bytes a user received in 2005.

---

## 1. Object ontology: what exactly are we trying to recover?

At minimum, separate these objects:

1. **software product** — e.g. a named program as a continuing project;
2. **version record** — a portal/database claim that version X existed;
3. **vendor/author origin page** — page controlled by the developer/publisher, if any;
4. **aggregator listing** — Huajun/Skycn/PConline/ZOL-style catalog record;
5. **download detail page** — page containing one or more visible download actions;
6. **mirror endpoint** — concrete HTTP/FTP server/path used to retrieve bytes;
7. **redirector / anti-hotlink layer** — intermediate request logic that can reject or rewrite the fetch;
8. **download-manager protocol/link** — e.g. a link handed to FlashGet/Xunlei rather than directly to the browser;
9. **binary artifact** — exact `.exe`, `.zip`, `.rar`, `.msi`, etc. bytes;
10. **wrapper/downloader** — small executable whose job is to obtain/install another program;
11. **intended installer** — installer for the product the user believes they selected;
12. **optional/advertised bundled components**;
13. **silent/undesired bundled components**;
14. **installed program state**;
15. **registration/license state**;
16. **update channel**;
17. **runtime dependencies** — OS, DLL/runtime, driver, browser integration, service, codec, Java/Flash/etc.;
18. **user-visible launch result**.

Do not collapse them into “software X was downloadable.”

---

## 2. Core state machine

A minimal acquisition path is:

`product known`
→ `listing discovered`
→ `detail page rendered`
→ `download action selected`
→ `endpoint resolved`
→ `transfer started`
→ `transfer completed`
→ `artifact identity checked/assumed`
→ `installer launched`
→ `installation completed`
→ `program launched`
→ `registration/activation completed (if required)`
→ `task actually performed`.

Each arrow can fail independently.

For old-Web claims, preserve at least these state gaps:

- `software-product / listing-record gap`
- `listing-record / current-version gap`
- `version-label / served-binary gap`
- `download-page / binary-object gap`
- `download-link / retrievable-object gap`
- `mirror-listed / mirror-operational gap`
- `browser-click / download-manager-dispatch gap`
- `download-manager-dispatch / server-permission gap`
- `transfer-start / transfer-complete gap`
- `complete-file / authentic-file gap`
- `authentic-file / safe-file gap`
- `downloaded-file / install-success gap`
- `install-success / runnable-runtime gap`
- `launch / task-success gap`
- `trial-installed / registered-license gap`
- `registered-license / future-activation-survival gap`
- `update-advertised / update-endpoint-survival gap`
- `visible-download-button / intended-target gap`
- `wrapper-downloaded / intended-software-installed gap`
- `current-version-page / historical-page gap`
- `historical-page / historical-served-bytes gap`
- `archived-binary / safe-to-execute-today gap`.

---

## 3. Why the Chinese download portal mattered

### 3.1 Early software discovery was not yet equivalent to “go to the official site”

A 2004 contemporaneous report on the “中文上网官方版” said the software was distributed not only from CNNIC’s own home page but also through 63 named/unnamed domestic download sites, including Huajun Software Garden, PConline and Skycn. The number and claimed download popularity are promotional-source data and must not be treated as audited market share. What it does establish is that **a publisher deliberately used aggregator sites as distribution infrastructure**.

Source: Sina / 新闻晚报, 2004-08-27  
https://tech.sina.com.cn/i/w/2004-08-27/1519413752.shtml

This matters for reconstruction because an “official source” model is insufficient. The same nominal software may have existed simultaneously as:

`developer/CNNIC page`
+ `Huajun catalog record`
+ `Skycn catalog record`
+ `PConline record`
+ `multiple mirrors`
+ `download-manager indexed copy`.

A source hierarchy has to identify **which channel** a claim refers to.

### 3.2 Download managers could become discovery front ends

A 2006 FlashGet tutorial describes a search function that opened results from Huajun and Skycn, allowing software search to begin inside a download manager and then hand off into Web results/download flow.

Source: Sina / ZOL, 2006-02-17  
https://tech.sina.com.cn/s/2006-02-17/0802843838.shtml

Thus:

`user typed query in FlashGet != user began at a Web search engine`.

The browser page may be only one middle layer in a client-mediated workflow.

---

## 4. Mirror economics: a visible link is not a timeless file locator

In June 2006, Huajun and Skycn stopped offering Xunlei downloads amid a dispute framed around hotlinking/server-resource use; Xunlei issued its own statement, and Huajun/Xunlei later issued a joint statement and restored cooperation. Each party had incentives in describing the dispute, so this note does **not** decide every technical or moral claim made by either side.

What is archaeologically secure is simpler: **download behavior depended on relationships among portal servers, client software and resource-cost policy.** A link that was valid in one client/context could cease to function or be blocked in another.

Sources:  
https://tech.sina.com.cn/s/s/2006-06-02/1056971523.shtml  
https://tech.sina.com.cn/i/2006-06-02/1628972187.shtml  
https://tech.sina.com.cn/s/s/2006-06-09/0838982272.shtml  
https://tech.sina.com.cn/i/2006-06-09/1020982615.shtml

Preserve:

`page advertises mirror != server grants fetch`.

Possible hidden state includes:

- Referer / anti-hotlink checks;
- cookie/session requirements;
- User-Agent/client integration;
- temporary redirect/token;
- bandwidth throttling;
- mirror operator policy;
- source server removal;
- download-manager P2P/P2SP behavior.

Unless a historical response is actually observed, do not infer which mechanism governed a specific link.

---

## 5. Version pages: a date field is not a binary provenance chain

Current software portals often preserve records with old-looking version dates. For example, ZOL’s current Any Video Converter series page still renders entries labeled 2009/2010, including metadata such as software size and security-scan fields.

Current page:  
https://soft.zol.com.cn/series/any-video-converter/

This is useful as a **current database rendering of historical-version metadata**, not as a 2010 Memento. Therefore:

`current page says “updated 2010-02-01”`

can support

`portal database currently attributes that date/version`

but cannot support:

- the 2010 HTML layout;
- the 2010 charset;
- the exact 2010 URL path;
- the exact mirror list on that day;
- whether a download counter shown today equals a historical snapshot;
- whether the current download action serves the historical binary;
- whether security-scan status displayed now was rendered identically then.

Call this **`metadata persistence / interface contemporaneity gap`**.

---

## 6. Safety and provenance: “listed” never meant “safe”

### 6.1 2008: portal-scale scanning becomes explicit infrastructure

A July 2008 report on Skycn and Kingsoft described an automated anti-virus interface scanning software uploaded to Skycn, with detected packages to be suspended from download. The article contains promotional/security-vendor claims and large threat counts that should not be treated as neutral prevalence estimates. Still, it directly establishes that the portal considered **package scanning** necessary infrastructure.

Source: DOIT, 2008-07-30  
https://www.doit.com.cn/p/31976.html

State gap:

`portal accepted upload != package safe`.

Even a clean scan at time T does not establish safety forever:

`scan-clean at T != clean under later signatures != author authenticity != bundle desirability`.

### 6.2 2010: the problem can move from the binary to the button

A January 2010 report describes a user who downloaded nominally free software and then found the browser homepage changed; it also discusses multiple visually similar download/advertising links and bundled software. The article’s broad characterization of the whole industry is journalistic and should not be converted into a prevalence statistic. The individual case and described UI pattern are enough to establish an important state gap:

`visible button labelled like a download != button targets intended artifact`.

Source:  
https://net.zol.com.cn/161/1615721.html

This means screenshots matter. A text-only archive that records one anchor labelled “download” but loses surrounding ads, button images, JavaScript and redirects may erase the very ambiguity users had to navigate.

---

## 7. Browser / download-manager compatibility is a first-class old-Web state

A 2006 FlashGet test explicitly listed fixes such as browser monitoring, setting FlashGet as the default browser download tool, and a bug where a Web button could not invoke FlashGet. That is direct evidence that “download page” and “download client” were coupled enough for integration bugs to matter.

Source:  
https://tech.sina.com.cn/s/s/2006-12-04/1806178057.shtml

Contemporaneous Q&A from 2010 also contains users troubleshooting cases where a browser and Xunlei/Skycn workflow did not cooperate. A current Baidu rendering of a dated post is not a historical browser capture, but its content can be evidence of user-visible compatibility friction.

Therefore preserve:

`HTML link present != clicking it invokes intended client`.

Do **not** infer “IE6 required”, “ActiveX required”, a specific charset, or exact browser compatibility from generic knowledge of 2000s Chinese sites. Those claims require `exact site × exact date × exact workflow` evidence.

---

## 8. Shareware: the binary and the commercial transaction are different archaeological objects

The 2002 contemporaneous profile of 贺辉 and his shareware program 《易表》 describes network distribution, paid advertisements on download sites, registration payments, user feedback and piracy/cracking. It provides a rare bridge between the visible download ecosystem and the author’s livelihood.

Source: Sina / 电脑报, 2002-10-21  
https://tech.sina.com.cn/s/n/2002-10-21/1716145088.shtml

For archaeology, however:

`downloadable trial != registered copy`.

Registration might involve:

- remittance/bank/payment channel;
- email exchange;
- serial/key delivery;
- different registered binary;
- server-side activation;
- manual author support.

Those transaction records are normally not public Web objects and may contain personal data. A preserved shareware ZIP can show what a user could try; it does not show whether a particular person paid, received a key or obtained support.

This yields **`public-trial / private-registration authority inversion`**: the public artifact is easy to archive, while the record most authoritative for a real purchase is private and should usually remain so.

---

## 9. First-person and community evidence: what users actually worried about

### 9.1 2007–2010: “快又安全” is already a user question

Current Baidu Zhidao pages retain posts dated 2007–2010 in which users ask where software can be downloaded quickly and safely, how to reinstall software that still will not launch, and where to find learning/stock-market tools. Replies alternate among official sites, Skycn/Huajun-like portals, download managers and antivirus checks.

Example current-rendered page, dated 2008-07-03:  
https://zhidao.baidu.com/question/59104910.html

Example current-rendered page, dated 2008-06-20:  
https://zhidao.baidu.com/question/57488535.html

Use these as **platform-visible contemporaneous content**. Do not use them as proof of:

- the exact 2008 Baidu page layout;
- search ranking at the time;
- historical advertisement placement;
- historical outgoing link target;
- general population frequency.

### 9.2 Current rendering can preserve the words while destroying the workflow

This is a recurring old-Web problem. A migrated Q&A system can keep title, timestamp and answer text while replacing:

- CSS/layout;
- download URLs;
- account presentation;
- recommendation/ranking logic;
- ad slots;
- mobile/desktop rendering;
- deleted answers.

Therefore distinguish **content contemporaneity** from **interface contemporaneity**.

---

## 10. 2011–2015 boundary: terminal-software governance becomes explicit

The China Internet Association’s 2011 draft industry norm defines “Internet terminal software” broadly to include browsers, instant messaging, download sharing, image processing, media players, Internet TV clients, games and security tools. Whatever its legal force or later evolution, the document is useful as a contemporaneous institutional signal: by this point the installable client layer itself had become a recognized governance object rather than a transparent appendage to the Web.

Source:  
https://www.isc.org.cn/article/15560.html

Within this repository’s time scope, that suggests a useful terminal boundary:

`Chinese old Web != HTML pages alone`.

Many core services of the 2000s depended on locally installed executable clients. A Web archive that perfectly preserves all public HTML can still systematically omit the client/server interaction that made the service operational.

---

## 11. Archive asymmetries specific to software distribution

### 11.1 `page-survival / binary-loss asymmetry`

The description page is HTML and crawler-friendly; the artifact may be a large binary, behind redirects, mirrors or anti-hotlink logic. The page can survive while the file vanishes.

### 11.2 `binary-survival / provenance-loss asymmetry`

An `.exe` with the correct filename may survive somewhere, but without contemporaneous hashes/signatures or a capture chain we may not know whether it is exactly the file served by the historical page.

`same filename != same bytes`.

### 11.3 `binary-survival / runtime-loss asymmetry`

Even bit-perfect preservation does not recreate:

- compatible OS;
- driver;
- runtime library;
- activation server;
- obsolete TLS/root certificates;
- browser helper protocol;
- update endpoint;
- server-side service.

Thus:

`preserved artifact != preserved experience`.

### 11.4 `mirror multiplicity / artifact identity gap`

Two mirrors advertised as the same version may conceivably have different packaging, timestamps or wrappers. Without hashes, do not assume identity merely from version text.

### 11.5 `archive-presence / execution-safety gap`

Old binaries can contain historical malware, exploitable components or unsafe installers. Archaeological preservation does not imply that researchers should execute them on a normal modern host.

Treat old executable artifacts as potentially hostile. Prefer static metadata/hash extraction and isolated environments if future work requires execution.

### 11.6 Physical media can sometimes preserve software better than Web pages

A preserved magazine companion CD/ISO can have a stable image-level hash and internal directory structure. That can be a stronger artifact identity object than a dead dynamic Web link. But it still cannot prove that a same-version portal link served identical bytes without an explicit cross-hash/provenance connection.

This is a useful cross-medium lesson: **old-Web archaeology should sometimes leave the Web to identify the artifact, while keeping the claim about the historical Web transaction narrow.**

---

## 12. M1 capture attempt status

This slice searched for historical Huajun/Skycn/EachNet-style and software-download portal traces, but did **not** obtain a Chinese historical software-download page/binary pair that can be verified under the repository’s M1 contract with all needed provenance fields.

Current status:

`M1 verified historical Chinese software-download page + served-binary pair: NOT ACHIEVED IN THIS SLICE`.

This **does not mean** “Wayback did not save it.” It means only that this research slice did not acquire and validate a qualifying replay.

Still unknown for a candidate 1999–2010 Huajun/Skycn page unless separately verified:

- original URL;
- exact capture URL;
- capture datetime;
- replay HTTP status;
- charset/header/meta interaction;
- DOM/form/button structure;
- JavaScript/ActiveX/helper-protocol behavior;
- mirror endpoints;
- redirects/session/Referer requirements;
- exact served binary;
- binary size/hash;
- whether the binary itself was archived;
- whether a download manager changed the fetched source.

Do not fill these with generic “Chinese sites of the period usually used GB2312/IE6” assumptions.

---

## 13. A future M1 protocol for one download page

A useful next artifact is **not** another retrospective “Top 10 download sites” list. It is one fully reconstructed transaction candidate.

For a selected historical page:

1. record original URL exactly;
2. open a real archive replay, not a locator/index only;
3. record capture datetime and replay HTTP status;
4. preserve raw HTML if available;
5. inspect response headers and in-document charset declarations separately;
6. enumerate all visible download anchors/buttons;
7. determine whether each target is direct HTTP/FTP, redirector, JavaScript, helper protocol or client invocation;
8. record each mirror hostname and path;
9. test only archival retrieval, not unsafe execution;
10. if a binary is available, record byte size and cryptographic hashes;
11. distinguish historical file capture time from page capture time;
12. compare filename/version text with internal PE/version metadata if safely extractable;
13. do not infer identical bytes across mirrors without hashes;
14. repeat on a second date to separate stable structure from one snapshot;
15. record missing subresources and any replay rewriting.

A strong M1 case would therefore be:

`verified 200x page`
+ `verified visible download control`
+ `verified endpoint chain`
+ `archived binary or explicit proof of its absence from this replay`
+ `artifact hash if present`
+ `second timepoint`.

---

## 14. Claim discipline for download counts and rankings

Historical/current portal pages may show “downloads”, popularity, rankings or stars. Do not translate them into unique people without knowing counter semantics.

Potential unknowns include:

- click vs transfer-start vs transfer-complete;
- mirror-level vs aggregated count;
- repeated download by same person;
- automated fetch;
- counter reset/migration;
- historical snapshot vs current accumulated total.

Therefore:

`download count != completed downloads != installs != active users != unique humans`.

Similarly, a current page that still displays an old version plus a very large download total may be accumulating across years or versions. Treat counter semantics as unknown unless documented.

---

## 15. Evidence ledger

| Evidence | Date | Class | Supports | Does not support |
|---|---:|---|---|---|
| POPSOFT republication of 1995 reader article | 1995 content / modern carrier | A-content / B-carrier | companion disk as software-acquisition channel | 1995 Web UI |
| CNNIC software distributed via 63 sites report | 2004 | A/B contemporaneous industry news | aggregators used as deliberate distribution channels | audited market share |
| FlashGet search tutorial | 2006 | A/B contemporaneous technical media | download manager → Huajun/Skycn search handoff | all-user behavior |
| Huajun/Xunlei dispute and joint statement | 2006 | A/B interested-party + media | server/client resource relationship could alter availability | full truth of either party’s accusations |
| FlashGet 1.80 beta2 test | 2006 | A/B technical media | browser integration/button invocation bugs were real workflow states | universal browser requirements |
| Skycn/Kingsoft scan cooperation | 2008 | B contemporaneous vendor/industry report | portal package scanning existed | neutral malware prevalence |
| Baidu Zhidao dated software questions | 2008–2010 | B current-rendered contemporaneous content | user troubleshooting/source-selection vocabulary | historical page rendering |
| 2010 deceptive-download-button report | 2010 | B media investigation/case | button-target/bundling ambiguity | sector-wide rate |
| China Internet Association terminal-software draft | 2011 | A/B formal industry document | installed client layer recognized as governance object | compliance by every firm |
| current ZOL old-version listing | current rendering of old metadata | C for old-interface claim | current database preserves version/date fields | historical DOM/binary identity |
| Tucows transfer to Internet Archive | 2021 retrospective | B | intentional binary-library preservation is possible | Chinese portal preservation state |

---

## 16. Cross-repository interpretation

The technical state gaps here change a life-history claim in `how-people-lived`.

A generic PC becomes socially important as a **reconfigurable household machine** only when ordinary people can repeatedly acquire tools after purchase. But each apparent increase in freedom produces another infrastructure layer:

`software scarcity`
→ `directory/mirror abundance`
→ `download acceleration`
→ `source ambiguity`
→ `package scanning / reputation`
→ `bundling and wrapper risk`
→ `curated stores / package managers / official-origin preference`.

Thus old-Web software portals should not be remembered simply as “sites we used before app stores.” They were a historically specific answer to a real problem: **how to make millions of heterogeneous executable artifacts findable and retrievable under slow links and fragmented author distribution.** Their later trust and bundling problems were partly second-order effects of succeeding at that first task.

---

## 17. What this adds to the repository method

This slice adds several archive rules worth reusing beyond software portals:

1. **Content object vs executable object**: Web page and payload may require different preservation strategies.
2. **Metadata persistence is not interface contemporaneity**: a current catalog can preserve old dates without preserving the old page.
3. **Mirror topology is historical evidence**: availability may depend on endpoint relationships, not just visible anchors.
4. **Client-side helper software belongs in Web archaeology when it mediates Web actions**: FlashGet/Xunlei/browser integration can be part of the historical page workflow.
5. **A preserved executable is evidence, not an invitation to run it.**
6. **Private registration/payment records can be more authoritative than public download pages, but privacy limits are part of the source model.**

---

## 18. Saturation status

This is a substantive new state-gap family for the project: software download portal → mirror → binary → installer → runtime → registration, plus binary/page survival asymmetry and browser/download-manager handoff.

Accordingly this run is **not** a no-new-mechanism run. Cross-project saturation count remains **0/3**.