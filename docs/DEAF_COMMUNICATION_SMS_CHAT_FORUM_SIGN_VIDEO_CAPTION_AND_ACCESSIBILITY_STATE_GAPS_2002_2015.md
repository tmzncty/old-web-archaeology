# Deaf Communication, SMS, Chat, Forums, Sign Video, Caption, and Accessibility State Gaps (China, 2002–2015)

> Scope: Chinese Web and Web-adjacent communication systems, approximately 2002–2015, where deaf and hard-of-hearing users encountered text, SMS, forums, instant messaging, captions, relay services, sign-language video, and institution-facing interfaces.
>
> Pre-Web TTY history appears only as a boundary condition. 2018–2026 material appears only as afterlife evidence showing which early state gaps persisted.
>
> This is **not** a general disability-policy history, hearing-aid history, or a claim that one communication mode fits all deaf users.

Companion life-history package:

- <https://github.com/tmzncty/how-people-lived/blob/main/topics/from-hearing-proxy-to-text-and-video-independence-deaf-communication-accessibility-and-life-path-executability-china-2002-2026.zh-CN.md>

---

## 0. Why this belongs in old-web-archaeology

A surviving page may say:

- “在线交流”；
- “支持短信”；
- “手语视频”；
- “同步字幕”；
- “无障碍服务”。

None of those labels proves that a deaf user could actually complete the intended communication.

A usable transaction may require:

```text
page reachable
-> visual/text interface understandable
-> account/session usable
-> message accepted
-> message delivered
-> recipient understands modality
-> recipient can respond in compatible modality
-> response reaches original user
-> offline action occurs, when required
```

This topic is therefore a particularly strong example of the repository's central distinction between **visible Web state** and **actual transaction executability**.

The core warning is:

> **communication availability is modality-specific: a service can be online, staffed, and technically functional while still being unusable to a person whose usable modality is not exposed by the interface.**

---

## 1. Pre-Web boundary: text telephony predates Web accessibility

The Internet did not invent remote text communication for deaf people.

Gallaudet University Archives documents the mid-1960s development of the acoustic-coupler TTY. Ordinary teletype machines had required expensive dedicated lines; Robert Weitbrecht's adapter allowed reclaimed machines to work over ordinary telephone lines. In 1964 Weitbrecht and James Marsters made a successful long-distance TTY call between deaf users. Community organizations later distributed and adapted machines and maintained TTY-number directories.

Sources:

- Gallaudet University Archives, *The Harry G. Lang Collection on Early TTY History*: <https://gaarchives.gallaudet.edu/repositories/2/resources/211>
- National Deaf Life Museum, “Telephones and TTYs”: <https://nationaldeaflifemuseum.omeka.net/exhibits/show/history-through-deaf-eyes/exhibition/awareness--access-and-change/telephones-and-ttys>

Evidence grade: **B** for the present Web finding aids/exhibition, backed by described archival collections containing contemporaneous material.

Archaeological lesson:

```text
telephone network exists
!=
text endpoint exists
!=
user owns endpoint
!=
other party has compatible endpoint
!=
relay to ordinary voice users exists
```

No inference is made here that Chinese households followed the same TTY adoption path.

---

## 2. 2002: text grafted onto the fixed/mobile telephone network

A 2002 *People's Posts and Telecommunications* item, now preserved by the China Rehabilitation Science Institute, reported that 15 deaf residents in Shanghai Jing'an received “家家e” fixed-line SMS telephones. The report states a unit value of RMB 300 and describes a live message sent from a participant's home to the event venue and answered there.

- <https://crsi.com.cn/Html/News/Articles/18888.html>

The same institutional archive preserves 2002 items on a Shanghai mobile “爱心卡” with user-entered or preset Chinese SMS phrases:

- <https://crsi.com.cn/Html/News/Columns/58/23.html>

Evidence grade: **B** (contemporaneous trade/media reports preserved on a later institutional site).

State gaps:

```text
fixed line installed
!=
SMS-capable terminal installed

SMS terminal installed
!=
user can afford ordinary ownership/replacement

message sent at demonstration
!=
service normalized in ordinary households

15 donated devices
!=
citywide adoption
```

This material matters to old-Web archaeology because it shows a Web-era accessibility transition that does **not require a browser at the user endpoint**. Backend/network digitization and text communication may affect ordinary life before household Web self-service becomes normal.

---

## 3. 2005 “聋人在线”: community page state versus lived community state

A 2005 contemporaneous report describes “聋人在线” as a broad deaf-community site with news, learning, career guidance, rehabilitation, psychology, forums, friend gatherings and chat use. It also records a concrete job-referral chain: a deaf woman in Nanjing asked the site for employment help; the operators referred her to an employer; she was interviewed and hired; she later emailed the site to thank them.

- <https://news.sina.com.cn/o/2005-09-09/13296903831s.shtml>

The same report states that founder Shen Gang initially lacked home broadband and had to work from an Internet café until a volunteer helped install broadband.

Evidence grade: **B**.

The report gives 23,000+ registered members and 10,000+ daily visits. These are **media-reported platform metrics**, not independently audited server logs.

### 3.1 Community-state model

```text
SITE_EXISTS
  -> SITE_REACHABLE
  -> USER_HAS_ACCESS_DEVICE
  -> USER_HAS_AFFORDABLE_CONNECTIVITY
  -> REGISTRATION_AVAILABLE
  -> ACCOUNT_CREATED
  -> FORUM/CHAT_REACHABLE
  -> POST/MESSAGE_CREATED
  -> OTHER_USER_READS
  -> RESPONSE_CREATED
  -> RELATIONSHIP / INFORMATION / JOB LEAD MAY FOLLOW
```

Never collapse:

- `site exists != household access`;
- `registered member != active user`;
- `forum post exists != useful answer received`;
- `job lead received != interview obtained`;
- `interview obtained != employment sustained`.

### 3.2 Historical identity is still incomplete

The 2005 report is strong evidence that a site called “聋人在线” operated and had the listed functional categories. In this slice, however, the exact original domain, URL hierarchy, forum software, charset, login flow and archive capture have **not** been independently verified.

Do not infer those details from later sites that reuse similar names.

---

## 4. 2007: QQ can be more communicatively available than co-presence

A 2007 contemporaneous article quotes a text message sent by a deaf university student identified as “小林” (pseudonym). After returning home for the winter holiday, he said that even family members could not understand his sign language. A classmate said his QQ account was online every day because he could not communicate well with relatives at home.

- <https://news.sina.com.cn/c/2007-02-01/032611135946s.shtml>

Evidence grade: **B+** — contemporaneous media reproducing a first-person SMS plus contemporaneous third-party observation.

This creates an important state distinction:

```text
PHYSICAL_COPRESENCE
!=
MODALITY_COMPATIBILITY

REMOTE_TEXT_SESSION
may be more communicatively usable than
PHYSICAL_COPRESENCE_WITHOUT_SHARED_SIGN/TEXT
```

For Web archaeology this means that “remote” and “socially distant” cannot be treated as synonyms. A QQ session could provide a more direct interaction than an in-person household conversation.

### 4.1 What a surviving QQ artifact would not prove

A friend-list entry or “online” icon would not prove:

- an actual conversation happened;
- the user personally controlled the account at that moment;
- messages were readable on the user's client;
- conversation frequency;
- emotional support received;
- whether the same person could communicate with a hospital, employer or government office.

Private QQ history is also a severe archive gap: public Web crawlers normally do not preserve authenticated instant-message content.

---

## 5. 2007: SMS becomes an institutional workaround

A contemporaneous 2007 report describes a court using more than 100 SMS messages while mediating a divorce involving two deaf litigants:

- <https://news.sina.com.cn/o/2007-10-22/133012768569s.shtml>

A separate 2007 report describes a Chengdu relay service in which deaf users could send text/SMS content that staff converted to voice for hearing recipients, with the reverse direction converted back to text:

- <https://news.sina.com.cn/s/2007-12-05/070013022765s.shtml>

Evidence grade: **B**.

### 5.1 Direct text and relay are different transaction models

Direct institutional text:

```text
DEAF_USER
  -> SMS/TEXT
  -> INSTITUTIONAL_STAFF
  -> TEXT RESPONSE
  -> DEAF_USER
```

Relay model:

```text
DEAF_USER
  -> TEXT
  -> RELAY_OPERATOR
  -> VOICE
  -> HEARING RECIPIENT
  -> VOICE
  -> RELAY_OPERATOR
  -> TEXT
  -> DEAF_USER
```

The second model introduces additional state and privacy boundaries:

- relay queue;
- operator availability;
- transcription/interpretation accuracy;
- third-party knowledge of sensitive content;
- recipient willingness to talk through relay;
- timeout/disconnect behavior.

Therefore:

> `SMS support != direct access`.

A service may still depend on a human hearing intermediary even after the user endpoint becomes digital.

---

## 6. 2007 Web captioning: a historical locator, not yet a verified capture

A February 2007 contemporaneous article described “开聪同步字幕系统”, downloadable free over the Internet, intended to provide synchronized text for live television programming including the Spring Festival Gala.

The report explicitly prints this URL:

- **historical locator:** `http://www.kaicong.com.cn`
- report: <https://news.sina.com.cn/s/2007-02-14/081812314818.shtml>

The article also describes the user-side chain as requiring Internet access and a TV card for the intended live viewing setup.

Evidence grade: **B for the report; locator candidate only for the historical site.**

State model:

```text
SITE_REACHABLE
  -> SOFTWARE_DOWNLOAD_REACHABLE
  -> DOWNLOAD_COMPLETES
  -> SOFTWARE_INSTALLS
  -> TV_INPUT / VIDEO PATH AVAILABLE
  -> LIVE TRANSCRIPTION CREATED
  -> TIMING SYNCHRONIZED
  -> CAPTION DISPLAYED
  -> USER CAN READ CAPTION
```

Do not collapse:

- `download page exists != program runs`;
- `program runs != live text arrives`;
- `caption arrives != synchronized`;
- `caption exists != complete/accurate`;
- `one live event != continuous broadcast accessibility`.

### M1 capture status

During this slice, direct attempts to open constructed Wayback replay URLs for `www.kaicong.com.cn` were not accepted by the current Web access path, and no compliant historical replay was obtained for inspection.

Therefore:

> **M1 NOT ACHIEVED IN THIS SLICE.**

This means only “no qualifying capture was verified in this run”. It does **not** mean that Internet Archive has no capture.

Unknown:

- exact capture datetimes;
- historical HTTP headers;
- charset;
- DOM/layout;
- JavaScript/plugin requirements;
- download filenames/hashes;
- server-side live-caption transport;
- failure pages;
- whether the report URL redirected to another host.

---

## 7. 2008 Web sign-language presentation: interface visible does not prove everyday adoption

Contemporaneous reporting around the Beijing Olympics described Web-based sign-language presentation/broadcast work on official online services.

- contemporary report locator: <https://news.sohu.com/20080822/n259112458.shtml>

Evidence grade: **B**.

This is useful as evidence that sign-language presentation had become a Web-interface research/deployment target by 2008. It does not establish:

- the exact original page path;
- whether every official Web page included it;
- the number of deaf users who accessed it;
- client/browser requirements;
- whether sign vocabulary matched every user's language practice;
- whether original video/3D assets survive.

In this slice the exact historical original URL and capture were not verified.

---

## 8. 2011 caption petition: “visual content exists” is not a complete accessibility model

In September 2011, a contemporaneous article reported that 892 deaf signatories asked the broadcasting regulator for full captions on television news. The report states that their survey found many major evening news programs lacked full captions. It also records the argument that captions may be more useful than standardized sign presentation to many hearing-disabled viewers who do not know standard sign language.

- <https://news.sina.com.cn/o/2011-09-26/044023216168.shtml>

Evidence grade: **B**.

Archaeological consequence:

Never code accessibility as a single boolean.

A more useful model is:

```text
VISUAL ACCESSIBILITY MODES:
- open captions
- closed captions
- textual transcript
- sign-language window/video
- visual alerts
- text chat

USER SIDE:
- reads written Chinese?
- uses sign language?
- which sign variety?
- can see video clearly?
- bandwidth/device sufficient?
```

Therefore:

`sign-language video present != accessible to every deaf user`

and

`caption present != complete, accurate, synchronous caption`.

---

## 9. A modality-aware Web transaction model

### 9.1 Person-to-person communication

```text
IDENTITY / CONTACT KNOWN
  -> COMMON PLATFORM EXISTS
  -> BOTH HAVE ACCOUNTS / ENDPOINTS
  -> COMMON MODALITY EXISTS
  -> MESSAGE CREATED
  -> MESSAGE SENT
  -> MESSAGE DELIVERED
  -> MESSAGE RENDERED
  -> MESSAGE UNDERSTOOD
  -> RESPONSE CREATED
  -> RESPONSE DELIVERED
```

State gaps:

- `contact listed != contact reachable`;
- `online indicator != active conversation`;
- `message sent != message delivered`;
- `text delivered != text understood`;
- `video delivered != sign visible/understood`;
- `voice call connected != deaf user can use it`.

### 9.2 Institution-facing communication

```text
SERVICE EXISTS
  -> ACCESSIBLE ENTRY POINT DISCOVERABLE
  -> USER CAN INITIATE IN USABLE MODALITY
  -> IDENTITY / CASE CONTEXT ACCEPTED
  -> STAFF OR RELAY RECEIVES
  -> MODALITY CONVERSION OCCURS IF NEEDED
  -> STAFF UNDERSTANDS REQUEST
  -> STAFF RESPONDS
  -> USER UNDERSTANDS RESPONSE
  -> OFFLINE ACTION COMPLETES
```

State gaps:

- `hotline number published != deaf user can call`;
- `Web contact form exists != emergency response exists`;
- `relay connected != institution accepts relay`;
- `interpreter connected != privacy equivalent to direct communication`;
- `case accepted != requested service delivered`.

### 9.3 Caption / media access

```text
PROGRAM EXISTS
  -> TEXT/SIGN SERVICE EXISTS
  -> SERVICE TIMED TO PROGRAM
  -> USER DISCOVERS ACCESS PATH
  -> CLIENT CAN RENDER
  -> CONTENT COMPLETE ENOUGH
  -> USER UNDERSTANDS
```

State gaps:

- `caption asset exists != synchronized`;
- `subtitle displayed != all spoken content represented`;
- `sign window displayed != readable on small/low-resolution screen`.

---

## 10. Browser, client, device and bandwidth are part of the historical interface

A modern browser opening an old information page cannot reconstruct the original communication environment.

Potential 2002–2015 dependencies include:

- fixed-line SMS terminal hardware;
- feature-phone SMS storage/input limits;
- SIM/service-plan pricing;
- QQ client version and authenticated private state;
- Internet-café access rather than household broadband;
- Windows desktop software installation;
- TV tuner/card hardware for synchronized-caption workflows;
- video codec/plugin requirements;
- low-resolution sign-language video;
- webcam availability;
- upstream bandwidth;
- room lighting and camera framing;
- whether both hands can remain visible while signing.

The archive may preserve none of these even if a text page survives.

---

## 11. Accessibility can regress when a service becomes “more digital”

Do not assume a monotonic sequence:

```text
offline -> Web -> mobile -> AI = more accessible
```

A new digital layer may create new failure modes:

- voice-only phone verification;
- audio-only CAPTCHA or customer support;
- video without captions;
- tiny sign window on mobile;
- inaccessible registration flow before an accessible chat feature;
- app-only service incompatible with an older device;
- automatic speech recognition errors on names, medicine, law or dialect;
- loss of human interpreter fallback.

This is a D-level general reconstruction unless a specific product/time is sourced. It is included here as an archaeological checklist, not as a claim that every listed failure occurred on every Chinese platform.

---

## 12. Afterlife checks, 2018–2026

These later materials are **not** part of the repository's main chronological target. They are used to test what state gaps from 2002–2015 remained unresolved.

### 12.1 2019 employment still requires modality support

A 2019 Beijing deaf-employment fair offered 600+ positions across software, editing, administration, finance, customer service and other roles. The venue still assigned sign-language interpreters to employers.

- <https://news.cnr.cn/dj/20190908/t20190908_524768406.shtml>

Afterlife inference:

> broader occupational menus did not eliminate the interview/meeting modality boundary.

### 12.2 2020 crisis: information latency becomes safety-relevant

A 2020 Wuhan report describes delayed epidemic information and difficult help-seeking among deaf residents, alongside deaf volunteers using video communication to coordinate support.

- <https://www.chinanews.com.cn/sh/2020/02-20/9097753.shtml>

Afterlife inference:

> a communication state gap that looks like inconvenience in ordinary time can become an emergency-state gap during crisis.

### 12.3 2024–2026: modern services still keep human relay/interpreter layers

Hebei added sign-language video service to the 12345 WeChat mini-program in 2024; a reported user carried the live interpreter into a hospital consultation through her phone screen.

- <https://www.xiongan.gov.cn/2024-09/26/c_1212400232.htm>
- <https://politics.people.com.cn/n1/2024/1031/c458474-40351190.html>

Zhuzhou's 2026 trial platform combines emergency-call relay, online sign interpretation and service routing:

- <https://zz.voc.com.cn/news/202606/32799545.html>

Qinghai 2026 public-service pilots likewise use remote human interpreters plus speech-to-text and text/voice conversion:

- <https://www.qhnews.com/newscenter/system/2026/03/30/030535730.shtml>

Afterlife inference:

> even with AI-assisted conversion, a human interpreter/relay layer remains institutionally valuable in high-context transactions.

---

## 13. Archive visibility bias

This topic has an unusually strong preservation bias.

### More likely to survive

- public news articles;
- public forum pages;
- software download descriptions;
- platform help pages;
- public petitions;
- government service descriptions;
- screenshots of visible interfaces.

### Much less likely to survive

- SMS content;
- QQ private chat;
- logged-in chatrooms;
- live interpreter sessions;
- phone-relay queue/voice state;
- sign-language video calls;
- family paper-and-gesture communication;
- failed attempts before successful service;
- a user who could not register at all.

This creates **text-preservation bias**:

> historical Web evidence may overrepresent deaf people who were literate in written Chinese, owned usable devices, had connectivity, and participated in public text spaces.

A future researcher could incorrectly infer that “deaf Internet life was naturally text-first” simply because text is what the archive preserves best.

---

## 14. Evidence register

| Date | Evidence | Grade | What it establishes | Main limitation |
|---|---|---:|---|---|
| 1964+ US | Gallaudet/NDLM TTY history | B | pre-Web text telephony and adoption constraints | overseas comparison, not China |
| 2002 | Shanghai fixed-line SMS report | B | bounded text-over-phone deployment | 15 donated devices, no prevalence |
| 2005 | “聋人在线” profile | B | forum/chat/info/job-referral functions; home-broadband barrier | exact original URL/stack not verified |
| 2007 | Xiao Lin SMS/QQ account | B+ | contemporaneous remote-modality advantage | one student/family |
| 2007 | court SMS mediation | B | institutional SMS workaround | single case |
| 2007 | Chengdu relay | B | human text/voice relay model | adoption/queue details unknown |
| 2007 | `kaicong.com.cn` report | B + locator | synchronized-caption software advertised and distributed | historical capture unverified |
| 2008 | Olympic Web sign report | B | sign presentation as Web target | exact page/client state unknown |
| 2011 | caption petition | B | persistent broadcast-access gap; modality heterogeneity | signatories not population sample |
| 2019+ | employment/health/12345 afterlife | B/A-B | early state gaps persist in later systems | outside main chronology |

---

## 15. Known / reasonable inference / unknown

### What we know

- text telephony predates the Web internationally;
- a bounded Shanghai fixed-line SMS deployment existed in 2002;
- a Chinese deaf-community site described as “聋人在线” was operating by 2005 with forum/chat/information functions and at least one reported job-referral outcome;
- a 2007 deaf student used SMS/QQ while reporting poor sign-language communication with family at home;
- SMS was used in at least one 2007 court case and in relay-service experiments;
- `http://www.kaicong.com.cn` was printed as a 2007 synchronized-caption download locator;
- full television caption access was still contested in 2011.

### What we can reasonably infer (D, explicitly marked)

- mainstream text platforms can reduce dependence on hearing intermediaries when both sides read/write the same language;
- private digital communication may be more accessible than physical co-presence when the household lacks shared sign language;
- archive survival will systematically privilege public text over private sign/video communication.

### What we do not yet know

- original “聋人在线” domain and page hierarchy;
- whether a compliant archived capture of that site survives;
- the original DOM/charset/forum engine/browser assumptions;
- historical QQ client/version accessibility details for these users;
- exact architecture and network protocol of the 2007 synchronous-caption system;
- exact official 2008 Olympic sign-language page URL and historical asset completeness;
- actual user counts for the specialized relay/caption systems;
- affordability and household adoption by class/region;
- how deafblind users and people with weak written-Chinese literacy experienced the same systems.

---

## 16. M1 / capture checkpoint

**M1: NOT ACHIEVED IN THIS SLICE.**

Candidate historical locator:

```text
http://www.kaicong.com.cn
```

Other historical identities/functions are supported by contemporaneous reporting, but exact original page locators remain incomplete.

Attempted in this slice:

- direct constructed Wayback replay paths for `www.kaicong.com.cn` through the available Web access route.

Result:

- current access path rejected/failed to provide a replay suitable for METHOD inspection;
- no capture datetime, HTTP headers, charset, DOM, script, download artifact, or browser behavior was verified.

Correct wording:

> “No qualifying historical capture was verified during this slice.”

Incorrect wording:

> “Wayback did not save it.”

---

## 17. What this changes in old-Web interpretation

Old-Web histories often treat a forum, chat client, subtitle download, or “contact us” page as a visible feature list. For deaf users, those visible features can be the difference between two entirely different social realities.

A telephone can be physically present but unusable. A QQ window can make a remote classmate easier to communicate with than a parent in the same room. A hotline can be fully operational but inaccessible until SMS, relay, or video interpretation is inserted. A Web page can say “字幕” while the live text stream is late, incomplete or impossible to install.

So this topic adds a stricter archaeological question:

> **When we say an old Internet service was “available”, available in which sensory and linguistic modality, to which user, on which device, and through how many human intermediaries?**

Without that state separation, a surviving page can make a historically inaccessible service look deceptively complete.

---

## Sources / provenance

Research/retrieval date: 2026-09-08.

Privacy note: only public, already published historical materials are cited; no private QQ/SMS identities or deleted personal records are republished. The pseudonym used in a 2007 contemporaneous article is retained only as the published pseudonym.

Copyright note: this file records links, metadata, transaction analysis and short paraphrases; no historical media binaries are copied.

AI-assisted initial synthesis; D-level inferences are explicitly marked and unknown capture state is preserved.
