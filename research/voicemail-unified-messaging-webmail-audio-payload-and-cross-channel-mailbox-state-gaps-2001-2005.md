# Voicemail, unified messaging, WebMail and cross-channel mailbox state gaps, 2001–2005

> Status: research / state-gap note, **not an M1 complete archaeology case**.  
> Primary old-Web scope: Chinese telecom unified-messaging systems whose mailbox state could be reached through WebMail as well as telephone / POP / IMAP / fax paths.  
> Companion life-history note: `tmzncty/how-people-lived/sources/from-missed-calls-to-stored-voice-answering-machines-voicemail-and-unified-messaging-china-1991-2005.zh-CN.md`.

## 0. Why this belongs in old-web-archaeology without turning the repository into a telephone-history project

The companion repository handles answering machines, fixed/mobile voicemail and asynchronous voice as ordinary-life communication history.

This repository only takes the slice where those older communication systems intersect the Chinese Web directly:

> **A voice / fax / email mailbox could have a Web representation, while the actual message state lived outside the captured HTML and could also be changed through non-Web channels.**

The anchor case is a China Telecom IDC UMS project signed in 2001 and described in a 2005 technical/vendor case. The system reportedly let users access voice mail through:

- telephone;
- WebMail;
- POP/IMAP mail clients;
- text-to-speech pathways;

and also supported fax-to-mail / mail-to-fax.

That is squarely an old-Web archaeology problem because a historical browser capture, even if perfect, may preserve only one interface onto a mailbox whose state was shared across several protocols.

The note therefore does **not** attempt a general history of answering machines. A 1980 household answering machine is useful comparative prehistory for `how-people-lived`, but it is outside this repository's primary 1995–2015 Chinese-Web scope unless it directly explains a Web-era interface.

---

## 1. Evidence contract

`docs/METHOD.md` applies without exception.

Research units remain distinct:

- **service / product**: operator voicemail, voice-SMS, UMS;
- **telephone number / mailbox account**: one provisioned mailbox identity;
- **Web front end**: e.g. a WebMail representation, if a historical public front end can be verified;
- **mail protocol access**: POP / IMAP;
- **telephone access path**: IVR / voicemail retrieval number;
- **notification path**: e.g. SMS informing the user that audio exists;
- **audio object**: one stored voice message;
- **greeting object**: owner-recorded or system greeting;
- **mailbox state**: message list, unread/listened/deleted state, quota/retention;
- **billing/provisioning state**: whether service is enabled and what retrieval/send path costs;
- **capture**: one archived representation at a verifiable time;
- **claim**: a narrow statement supported by one or more evidence objects.

Minimum rule:

```text
WebMail page survives
!= mailbox survives
!= audio survives
!= notification survives
!= telephone path survives
!= same mailbox state survives
!= user listened
```

---

## 2. 2001 China Telecom UMS: one mailbox, several access protocols

A DOIT case study published 2005-04-05 describes a China Telecom IDC project whose contract date is given as **May 2001** and installation locations as Beijing, Shanghai, Guangzhou and Xi'an.

The case says the UMS (Unified Message Service) layer was built on a large-capacity email system and offered:

- mail management;
- voice mail;
- fax mail;
- mail notification.

For voice mail specifically it says users could access messages through:

- telephone;
- WebMail;
- POP/IMAP mail clients;
- TTS (text-to-speech) access.

It also describes mail-to-fax and fax-to-mail functions.

Source:

- DOIT, 2005-04-05, `中国电信IDC项目UMS统一消息服务系统案例分析`  
  https://www.doit.com.cn/p/17152.html

**Evidence grade: B/C boundary.** It is a technical/vendor case published four years after the stated contract, useful for architecture and deployment claims but not equivalent to a 2001 live front-end artifact or independent adoption measurement.

### Archaeological consequence: `cross-channel mailbox state`

The same logical mailbox could be mutated through several interfaces.

For a hypothetical stored message `M`:

```text
M arrives
  -> user listens by telephone
  -> state may become listened/read
  -> later WebMail representation may differ
```

or:

```text
M arrives
  -> WebMail deletes M
  -> later telephone IVR no longer announces M
```

Whether those exact semantics held for this deployment still requires product/manual evidence. The important confirmed architectural point is that several access channels were advertised for one messaging service.

Therefore a historical Web capture is not a self-contained state object.

---

## 3. State gap 1: `mailbox-provisioning state`

A user-facing page can exist even when a particular telephone account has not enabled voicemail, or the reverse: the backend can provision a mailbox without the user having intentionally activated it.

The latter is not hypothetical. A 2004 Beijing Youth Daily report describes Xi'an Telecom enabling a “free” voicemail function across household fixed lines / Xiaolingtong after a system upgrade. Some users reported learning of the service only after calls began being diverted after several rings.

Source:

- 北京青年报 / 新浪新闻, 2004-04-28, `“免费”语音信箱 暗设收费陷阱`  
  https://news.sina.com.cn/c/2004-04-28/06502419649s.shtml

**Evidence grade: B.** Contemporaneous consumer reporting with reporter testing, user complaints and operator response.

This yields an old-Web rule:

```text
service advertised
!= mailbox provisioned for account X

mailbox provisioned
!= user knowingly activated it

Web login exists
!= voice feature enabled
```

If a future archived WebMail UI contains a “voice mail” tab, that proves interface capability, not the historical provisioning state of any ordinary subscriber.

---

## 4. State gap 2: `audio-payload survival gap`

HTML may preserve:

- a mailbox row;
- sender/caller metadata;
- timestamp;
- play/download control;
- duration field;

while the actual voice object is missing.

Potential audio storage could have lived in:

- a separate media server;
- an authenticated attachment endpoint;
- a generated streaming URL;
- a mailbox backend never exposed to crawler access.

Until a historical implementation is directly inspected, those are only possible architectures, not claims about the China Telecom deployment.

The minimum archaeology distinction is:

```text
voice-message metadata survives
!= voice-message audio survives
```

This matters more than for ordinary text email because the semantic content may exist only in the missing audio payload.

---

## 5. State gap 3: `notification-state loss`

China Unicom's 2003 `10158 短信听` is useful comparative evidence because its workflow explicitly separated voice content from the notification channel:

1. sender dials 10158;
2. records up to 30 seconds;
3. enters recipient mobile number;
4. recipient receives a text SMS saying a voice message is waiting;
5. recipient calls 10158 to hear it.

The report gives a sender price of 0.1 RMB/message and says receipt of the notification and listening were free. It also says earlier mobile voicemail offerings had weak market response in part because sender and recipient were both charged by time.

Source:

- 北京现代商报 / 新浪科技, 2003-07-01, `联通开通“语音短信” 语音服务瞄准手机终端`  
  https://tech.sina.com.cn/it/t/2003-07-01/1322204317.shtml

**Evidence grade: B.**

For Web archaeology the important state chain is:

```text
message exists in voice backend
!= notification generated
!= SMS delivered
!= user noticed notification
!= user retrieved audio
```

A preserved Web page from the same product family would normally expose at most one part of this chain.

---

## 6. State gap 4: `read/listened-state ambiguity`

Email/WebMail uses concepts such as read/unread. Voice systems can have analogous but not necessarily identical states:

- new;
- announced;
- listened;
- replayed;
- saved;
- deleted;
- expired.

The exact state machine of the 2001 China Telecom UMS deployment has **not** been recovered in this run.

Therefore a future reconstruction must not invent familiar modern voicemail semantics merely because they seem plausible.

Required evidence before claiming state behavior:

- contemporaneous user manual;
- operator help page;
- protocol/product documentation;
- directly inspectable historical UI / API behavior.

### Cross-channel warning

Even if a 2002 WebMail capture displays `unread`, the historian must ask:

- could listening by telephone clear this flag?
- did POP download alter state?
- did IMAP preserve it?
- did deleting by telephone remove the Web row immediately or after synchronization?

These are empirical questions.

---

## 7. State gap 5: `greeting-state gap`

A voicemail service often has an outgoing greeting or system announcement.

The 2004 Xi'an report records callers being diverted after a few rings to a system voice prompt. The available report does not establish whether individual household users could record a personal greeting in that implementation.

Therefore preserve:

```text
system prompt observed/reported
```

separately from:

```text
personal greeting supported
```

and separately from:

```text
specific user's historical greeting recovered
```

The last category would also raise strong privacy issues and usually should not be sought for ordinary users.

---

## 8. State gap 6: `billing-route invisibility`

Telecom messaging behavior depended on who paid and at which step.

A government-preserved 2002 report on telecom tariff liberalization explicitly lists:

- fixed-line voicemail account-opening and monthly-rental charges;
- mobile voicemail and other supplementary-service charges.

Source:

- 重庆市发展改革委存档 / 华西都市报, 2002-11-21, `四川省开始放开34类100余种电信资费`  
  https://fzggw.cq.gov.cn/zwxx/xwbd/202003/t20200319_5775331.html

**Evidence grade: A-content/B.**

The 2003 `10158` report gives a concrete redesign where sender pays 0.1 RMB and recipient notification/listening are free.

Archaeological consequence:

```text
same visible “leave message” function
!= same historical economic action
```

A Web form or help page is insufficient unless the relevant tariff period is also identified.

---

## 9. State gap 7: `cross-channel parity ambiguity`

“Accessible by phone and WebMail” does not prove the interfaces exposed identical capabilities.

Possible differences include:

- telephone can play/delete but not download;
- Web can expose metadata not spoken by IVR;
- POP/IMAP can deliver audio as attachments;
- fax mail may render as image/document rather than an equivalent message class;
- TTS may provide a one-way transform from text email to voice playback.

The 2005 UMS case confirms multiple access methods, but does not in the currently retrieved text provide enough detail to reconstruct complete capability parity.

Therefore the repository should record per-channel capabilities independently:

| capability | telephone | WebMail | POP/IMAP | fax | TTS |
|---|---:|---:|---:|---:|---:|
| list messages | unknown | probable, not yet artifact-verified | unknown | n/a | unknown |
| hear voice audio | reported | reported access, exact player unknown | reported access, encoding unknown | n/a | n/a |
| receive text email | unknown | reported email system | reported | n/a | reported through TTS |
| delete / mark state | unknown | unknown | unknown | unknown | unknown |
| send fax / convert | reported system function | unknown UI | unknown | reported | n/a |

Anything marked unknown stays unknown until artifact or manual evidence resolves it.

---

## 10. New archive mechanism: `backend continuity / interface discontinuity`

Unified messaging creates a preservation problem opposite to a static homepage.

The backend mailbox may have continued operating while:

- public WebMail URLs changed;
- login pages were redesigned;
- domains migrated;
- telephone access numbers changed;
- authentication moved behind a new portal.

Or the Web shell may survive after the messaging backend has been decommissioned.

Therefore:

```text
historical Web shell alive
!= historical mailbox backend alive
```

and:

```text
mail service continuity
!= Web interface continuity
```

A future M1 case involving messaging should treat backend era and interface era as separate timelines.

---

## 11. New archive mechanism: `cross-channel mutation invisibility`

The hardest problem is not merely that a crawler cannot authenticate.

It is that state may have changed outside the browser entirely.

Example model:

```text
12:00 message arrives
12:05 crawler captures Web mailbox row as unread
12:07 subscriber calls voicemail number and listens
12:08 backend marks message listened
```

The 12:05 capture remains historically valid for that moment, but a later researcher cannot infer from it how long the unread state persisted or which interface changed it.

Call this:

### `cross-channel mutation invisibility`

It generalizes to other old-Web services whose state could be changed via:

- telephone IVR;
- SMS;
- desktop mail client;
- fax;
- operator/customer-service action.

This is distinct from ordinary server-side dynamic content because **another communications network may be the state-changing client**.

---

## 12. Privacy boundary

Voicemail archaeology has an unusually high risk of recovering private ordinary-person content.

For this repository, useful evidence usually consists of:

- service manuals;
- field names;
- public help pages;
- login / mailbox UI schema;
- sample/demo messages;
- operator product documents;
- protocol behavior;
- public historical screenshots;
- archived code or media assets with no personal content.

Do **not** treat real ordinary-user voicemail audio, phone numbers, PINs, greetings, caller identities or private mailbox contents as desirable collection targets merely because an abandoned endpoint exposes them.

If a historical artifact contains personal message data, prefer redacted structural description over republication.

---

## 13. Overseas control: answering-machine artifacts show a different storage locus

The companion HPL note uses US Smithsonian artifacts as the cross-national control:

- 1980 `AutoMatic TelePhone`: local answering machine, about 20 minutes recording; advanced model supports remote retrieval from another telephone;
- ca. 1981 Jan Butterfield answering-machine cassette: actual ordinary historical messages survive as a physical audio artifact;
- ca. 1982 Code-a-Phone: museum history notes some callers resisted speaking to a machine.

Sources:

- https://americanhistory.si.edu/collections/object/nmah_1299450
- https://www.aaa.si.edu/collections/items/detail/telephone-answering-machine-messages-14295
- https://americanhistory.si.edu/collections/object/nmah_1299447

For OWA, the comparison is methodological:

```text
local answering machine
→ audio state may survive as physical tape

network voicemail / UMS
→ audio state lives in carrier/service backend
→ Web crawler may preserve only interface metadata
```

This does not prove that China lacked local answering machines or that US adoption was greater. It only demonstrates two different preservation geometries.

---

## 14. Artifact search status in this slice

### Achieved

- China Telecom UMS project identity and stated 2001 contract date: achieved through 2005 technical/vendor case.
- Reported access modes (telephone, WebMail, POP/IMAP, TTS): achieved at architecture-claim level.
- Fixed/mobile voicemail as tariff/service categories by 2002: achieved.
- 2003 China Unicom voice-SMS workflow and pricing: achieved through contemporaneous report.
- 2004 Xi'an fixed-line voicemail auto-provisioning dispute: achieved through contemporaneous report.

### Not achieved

- exact public historical China Telecom UMS WebMail hostname: **not achieved**;
- exact 2001–2005 public login URL: **not achieved**;
- inspectable Wayback capture of UMS/WebMail UI: **not achieved**;
- replay/HTTP status: **not achieved**;
- DOM / HTML: **not achieved**;
- charset / Content-Type: **not achieved**;
- historical voice-player implementation: **not achieved**;
- historical audio attachment MIME type / codec: **not achieved**;
- mailbox state machine: **not achieved**;
- second verified historical timepoint: **not achieved**.

### M1 status

**M1 COMPLETE CASE: NOT ACHIEVED.**

This note must not be cited later as if “the 2001 WebMail page has been recovered.”

At present we have a historically anchored architecture lead and state model, not a verified historical Web representation.

---

## 15. Next artifact-first probes

Priority order:

1. Search contemporaneous China Telecom IDC / UMS product brochures, manuals and operator help pages for a historical hostname or screenshots.
2. Search 2001–2005 Chinese technical magazines and vendor manuals for exact WebMail / UMS URLs.
3. Search old DNS/domain references only after obtaining an exact candidate host; do not guess a URL from later branding.
4. If a Wayback locator is found, verify:
   - capture datetime;
   - replay/HTTP state;
   - DOM / source;
   - charset / Content-Type;
   - forms and link targets;
   - scripts / media-player dependencies;
   - audio-resource URLs;
   - authentication boundary;
   - second historical timepoint.
5. Keep telephone/IVR and POP/IMAP manuals alongside Web captures, because a Web-only reconstruction cannot establish cross-channel state behavior.

---

## 16. Confirmed / probable / unknown

### Confirmed or strongly supported

- By 2002, fixed and mobile voicemail existed as tariff/service categories in China.
- A China Telecom IDC UMS project signed in 2001 was later described as supporting voice/fax/email functions with telephone, WebMail, POP/IMAP and TTS access paths.
- China Unicom's 2003 10158 product explicitly separated stored voice content, SMS notification and later telephone retrieval.
- A 2004 Xi'an case shows that provisioning can occur without user awareness or intentional adoption.

### Probable but not artifact-verified for the 2001 project

- WebMail presented voice-message metadata and some way to invoke playback or access the voice object.
- Mailbox state was shared across at least some access channels.

### Unknown

- exact public host / URL;
- exact UI;
- codec/player;
- cross-channel read/delete synchronization semantics;
- quota and retention;
- authentication model;
- ordinary-user penetration;
- how long the Web interface remained unchanged.

---

## 17. Why this changes the repository's archaeology model

Earlier dynamic cases already established:

```text
page != backend state
```

This case adds a narrower but genuinely new constraint:

> **backend state may be mutated through a non-Web network while the historical Web page is only one temporary view.**

For unified messaging, the correct research unit is closer to:

```text
mailbox
× time
× channel
× provisioning state
× notification state
× message/audio state
× tariff state
```

rather than simply:

```text
URL × capture time
```

That makes this a useful cross-repository case even before a complete M1 artifact is recovered.
