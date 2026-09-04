# PAGER_WEB_GATEWAY_EMAIL_TO_PAGER_AND_REACHABILITY_STATE_GAPS_1999_2007

Status: research note / state-gap model  
Scope: approximately 1999–2007 Chinese public Web evidence around 网上寻呼、电子邮件到达呼、Web-configured message forwarding and the shutdown of public paging networks  
Companion life-history note: `tmzncty/how-people-lived/topics/pagers-asymmetric-reachability-callback-labor-and-the-mobile-summons-china-1984-2026.zh-CN.md`

## 0. Why this belongs in old-web archaeology

Pager history is easy to misread as a hardware story.

For this repository, the much more useful object is the late-1990s / early-2000s **Web-to-paging gateway**.

A historical page may claim:

- “网上寻呼”；
- “电子邮件到达呼”；
- “输入寻呼号码发送”；
- “新邮件自动通知”；
- “禁呼时间”；
- “过滤关键字”；
- “已发送”。

None of those visible states proves that a specific ordinary person’s pager actually beeped, displayed the message, was noticed, or resulted in a callback.

The master warning is:

> **Web submission state ≠ paging-network delivery state ≠ human receipt ≠ real-world response.**

This is especially valuable for old-Web archaeology because the transport layer itself has largely vanished. Even if HTML survives, the carrier gateway, paging center, RF network and private subscriber records may no longer exist.

This note does not attempt to revive historical pager numbers, reconstruct subscriber accounts, or republish private messages.

---

## 1. Research units

Per `docs/METHOD.md`, keep these objects separate:

- public Web page;
- authenticated user configuration page;
- one email account;
- one Web form submission;
- pager number / subscriber record;
- Internet-to-paging gateway;
- operator paging center;
- radio network;
- one physical pager;
- device power / coverage state;
- one displayed message;
- human notice;
- callback / reply channel;
- one archive capture;
- researcher claim.

A surviving 1999 feature page can prove that a service was described.

It does **not** prove:

- a user enrolled;
- the user’s filter was saved;
- one email matched the filter;
- the gateway accepted the event;
- the paging network transmitted it;
- the pager was powered on and in range;
- the recipient read it;
- the recipient called back.

---

## 2. Evidence grades used here

### A / A-

- communications statistical bulletin / official statistical compilation where provenance is clear;
- historical technical or service documentation produced at the time.

### B / B+

- near-contemporaneous media reporting;
- current corporate archive preserving a dated historical press release, when the original 1999 capture has not been independently verified.

### C

- later personal recollections of 1990s pager routines.

### D

- the state machine and gap taxonomy below are researcher models.

---

## 3. Strong anchor: by end-1999, Chinese paging networks had explicit Internet gateways

A June 14, 2000 online reproduction of the **1999 communications development statistical bulletin** states that by the end of 1999:

- “网上寻呼” had been opened on the national 198/199 paging network, 27 provincial networks and some local networks;
- “电子邮件到达呼” had been opened in 22 provincial networks.

Source / A-/B+:
- https://tech.sina.com.cn/it/2000-06-14/28155.shtml

A scanned `通信统计资料汇编（1999）` attributed to 信息产业部综合规划司 is also available as a research lead. The scan itself should be cited only after the exact page containing the relevant statement is located and visually checked.

### Narrow claim

By the end of 1999, an Internet/paging service integration was not merely speculative: official communications reporting described online paging and email-arrival paging as deployed across national/provincial paging networks.

### Do not infer

- mass consumer adoption;
- exact UI design;
- browser requirements;
- exact delivery latency;
- whether every 198/199 user could use the service;
- whether any particular user received a specific email notification.

### Historical significance

This gives the old Chinese Web a transport relation that disappears from many later histories:

```text
Internet / email
→ gateway
→ paging system
→ RF transmission
→ portable receiver
```

The Web was already connected to a non-Internet mobile notification network.

---

## 4. Tencent/SINET 1999 evidence: browser-side rules controlling mobile interruption

Tencent’s current corporate archive preserves a page dated 1999-07-11 describing an email value-added system jointly launched with SINET on Shenzhen Telecom’s network for trial operation.

The archived corporate text says that when email arrived, the system could extract:

- sender address;
- subject;
- content;

and, if user-defined rules matched, forward content to a paging station or GSM SMS system.

It also says users could authenticate with username/password and configure parameters including:

- call-barring / no-page time periods;
- mail-forwarding time periods;
- string filtering.

Source / B+:
- https://www.tencent.com/en-us/articles/80260.html

### Provenance caution

This is a current Tencent corporate-history page carrying a 1999 date.

This run did **not** verify a 1999 Web archive capture of the original page.

Therefore:

- it is strong evidence that Tencent currently preserves this dated historical claim;
- it should not be represented as a verified 1999 original HTML capture;
- the historical DOM, URL parameters, charset, forms and browser behavior remain unknown.

### Why the “禁呼时间” field matters

If authentic to the described system, it shows that reachability was already programmable in the browser:

```text
mobile notification capability
+ user-configured time boundary
```

But:

`rule UI exists ≠ rule saved ≠ rule executed ≠ social boundary respected`

A historical user could technically suppress pages during a period while an employer or family member might still expect immediate response.

---

## 5. Master state machine

A Web/email-to-pager route should be modeled as at least:

```text
[PUBLIC FEATURE STATE]
service announced
→ public page/help page reachable

[ACCOUNT / RULE STATE]
user eligible
→ account authenticated
→ pager/mobile endpoint bound
→ forwarding rule created
→ quiet-time/filter rule stored

[TRIGGER STATE]
email/message/event arrives
→ server parses event
→ rule is evaluated
→ event qualifies for forwarding

[GATEWAY STATE]
gateway job created
→ payload transformed/truncated/encoded
→ paging operator accepts submission

[RADIO DELIVERY STATE]
paging center schedules transmission
→ relevant transmitter/network available
→ pager in coverage
→ pager powered / receiving
→ message received/displayed

[HUMAN STATE]
user notices alert
→ user interprets number/text
→ user decides to act

[REPLY / OUTCOME STATE]
reply channel found
→ callback/SMS/other reply attempted
→ other party reached
→ practical action completed
```

Every arrow is a possible evidence gap.

---

## 6. Gap taxonomy

### 6.1 feature-claim gap

`service page exists ≠ ordinary user could successfully use service`

A launch article or help page proves a claim/availability layer, not end-to-end operation.

### 6.2 authentication-state gap

`login form exists ≠ historical credentials authenticated`

Public archives generally cannot and should not preserve ordinary users’ live credential state.

### 6.3 endpoint-binding gap

`account exists ≠ correct pager number was bound to it`

Pager-number bindings are private subscriber data.

Do not recover or republish them unless a public institutional case genuinely requires the minimum detail.

### 6.4 rule-persistence gap

`browser shows “设置成功” ≠ backend stored rule`

A client-side confirmation can precede or even substitute for a failed backend write.

### 6.5 filter-evaluation gap

`rule stored ≠ one historical message matched it`

A “string filter” feature cannot be used to infer what messages the user saw.

### 6.6 gateway-submission gap

`email arrived ≠ gateway submitted a paging job`

Possible interruption points include:

- mail parser failure;
- encoding failure;
- account state;
- quota;
- backend outage;
- routing configuration;
- operator interface failure.

### 6.7 payload-transformation gap

`Internet text ≠ pager display text`

The gateway may:

- truncate;
- strip characters;
- convert charset;
- retain only subject/sender;
- replace unsupported symbols;
- split a message.

A surviving Web/email text is therefore not necessarily the text displayed on the pager.

### 6.8 operator-acceptance gap

`gateway request sent ≠ paging operator accepted it`

The external network boundary is a distinct state.

### 6.9 radio-delivery gap

`operator accepted ≠ pager received`

Coverage, transmitter state and RF conditions matter.

### 6.10 device-state gap

`RF transmission exists ≠ physical pager was powered and functional`

Possible states:

- off;
- dead battery;
- out of range;
- broken device;
- wrong device/address;
- storage/display limitation.

### 6.11 human-notice gap

`pager displayed ≠ user noticed`

A user may be asleep, in a noisy place, have silent/vibration behavior, or ignore a low-priority message.

### 6.12 callback-channel gap

`user saw callback number ≠ user could call`

Especially for one-way numeric pagers, real response might still require:

- public telephone;
- office telephone;
- home telephone;
- telephone card / cash;
- access permission;
- time to find a phone.

This is the main bridge to ordinary-life history.

### 6.13 reply-outcome gap

`callback attempted ≠ other party reached`

A full social interaction requires another state chain after the page itself.

### 6.14 public-Web/private-message gap

The historically most important events — actual pager messages — are also the least appropriate material to mass-republish.

Public feature pages and service manuals should be preferred over private message reconstruction.

---

## 7. A 1999 “发送成功” page is especially dangerous evidence

Suppose a verified Wayback capture eventually shows:

> “您的寻呼已经发送成功。”

The strongest safe interpretation may still be only:

- the historical application reached a browser-visible success branch;
- or an archive replay has preserved text that was once used for that branch.

It does **not** automatically prove:

- an operator accepted the message;
- RF transmission occurred;
- the pager received it;
- the recipient read it;
- any callback occurred.

Therefore old-Web work on transactional communication must preserve a distinction between:

> **UI success and transport success.**

This applies beyond pagers to:

- email;
- SMS gateways;
- fax gateways;
- ticket booking;
- online payment;
- appointment systems;
- early e-commerce orders.

---

## 8. Transport-layer extinction

This case adds a particularly useful archive category:

> **transport-layer extinction**

A historical website can be perfectly preserved while the network it controlled is gone.

For a public paging gateway, missing infrastructure can include:

- paging carrier backend;
- operator-to-gateway protocol;
- subscriber database;
- numbering plan allocation;
- RF transmitter network;
- paging center software;
- proprietary message format;
- terminal hardware.

So even a complete HTML/JS recovery may be **non-executable by historical definition**.

This is stronger than ordinary link rot.

The missing object is not only a file; it is the external communication network.

---

## 9. 2007 public paging shutdown: why historical forms become semantically dead

In March 2007, contemporaneous reporting on the Ministry of Information Industry notice said China Unicom applied to discontinue 198/199, 126/127 and 128/129 wireless paging services in 30 provinces/regions/municipalities outside Shanghai, after user cleanup/transfer work.

Sources / B:
- https://tech.sina.com.cn/t/2007-03-07/07191404385.shtml
- https://tech.sina.com.cn/t/2007-03-04/08031400044.shtml

### Archaeological implication

After network shutdown, an archived “online paging” form can retain:

- labels;
- instructions;
- pager-number field;
- message field;
- submit button;

while every meaningful backend arrow is dead.

That page has become an artifact of an **extinct service contract**.

### Do not test with real numbers

Do not attempt to discover old ordinary users’ pager numbers or repurpose current numbers to “see what happens”.

The network/service no longer represents the historical subscriber relation, and personal data minimization takes priority.

---

## 10. Public paging shutdown does not prove all pager topologies ended in 2007

Contemporaneous Chongqing reporting in March 2007 still counted thousands of pager-service users and described remaining unit/special-use contexts even as the mass consumer market disappeared.

Source / B:
- https://news.sohu.com/20070306/n248531044.shtml

Therefore distinguish:

```text
public national paging service shutdown
≠ every local/private/organizational paging network shutdown
≠ all pager hardware instantly unused
```

The repo should date the exact service/network under study instead of declaring a universal pager “death date”.

---

## 11. Overseas comparator: two-way paging shows the state machine was not technologically fixed

A January 1996 *WIRED* first-person review of SkyTel 2-Way describes:

- automatic receipt acknowledgement;
- retransmission until acknowledged;
- text messages;
- preset/custom short replies from the pager.

Source / B contemporaneous:
- https://www.wired.com/1996/01/paging-goes-two-ways/

Smithsonian’s Motorola BPR2000 description documents the older one-way model as a receiver that alerts a user and shows a callback number.

Source / A object evidence:
- https://americanhistory.si.edu/collections/object/nmah_1344387

### Comparative conclusion

Do not define `pager` as one immutable technical object.

At minimum distinguish:

- tone-only pager;
- numeric pager;
- alphanumeric pager;
- two-way pager;
- organization/private pager;
- Internet/email-to-pager gateway endpoint.

This matters for Web archaeology because each type implies different backend and user state chains.

---

## 12. Browser / charset / protocol questions still unresolved

The sources prove capability and some described fields, but this run did **not** verify a historical Chinese gateway capture.

Therefore these remain unknown until a capture is actually inspected:

- original URL patterns;
- HTTP method;
- CGI/ASP/JSP implementation;
- cookie/session format;
- GB2312/GBK/UTF-8 behavior;
- maximum message length;
- whether page forms required IE-specific behavior;
- JavaScript validation;
- whether login ran over HTTPS;
- whether pager-number inputs had client-side formatting;
- how Chinese text was converted for paging;
- exact browser error/success pages.

Do not fill these with period stereotypes such as “肯定是 ASP + IE5 + GB2312”.

Those are hypotheses, not evidence.

---

## 13. Capture checklist for a future verified pager gateway

If a historical capture is found, record at minimum:

### Resource identity

- original URL;
- archive URL;
- capture datetime;
- host/domain owner at that date;
- page title;
- whether the page is public/help/authenticated.

### UI state

- input fields;
- pager-number format;
- message limits;
- send/confirm actions;
- quiet-time/filter fields;
- error/success text;
- visible service restrictions.

### Technical state

- Content-Type;
- declared/inferred charset;
- forms action/method;
- JS dependencies;
- frame dependencies;
- image/CSS resource survival;
- archive rewrite behavior.

### Claim boundary

For every screenshot, write explicitly whether it proves:

- exists;
- available;
- used;
- delivered;
- noticed;
- replied.

Most captures will prove only the first one or two.

---

## 14. Archive-gap taxonomy specific to pager gateways

### 14.1 form-shell survival

HTML form survives, action endpoint dead.

### 14.2 authenticated-state loss

Public login page survives, private subscriber pages do not.

### 14.3 backend-protocol loss

The browser endpoint survives, paging API/protocol implementation does not.

### 14.4 subscriber-database loss

Historical number/account bindings unavailable or inaccessible.

### 14.5 RF-network loss

Carrier paging transmitters/service shut down.

### 14.6 dynamic-confirmation loss

Success/failure pages generated per request were never crawled.

### 14.7 personal-message privacy barrier

The most vivid evidence may exist only in private communications and should not be mass recovered/reposted.

### 14.8 corporate-archive provenance gap

A present-day corporate history page may preserve a dated press release while the original historical URL/capture is unknown.

Such evidence is useful, but should not be silently upgraded to A-grade original Web capture.

---

## 15. What this changes in old-Web interpretation

### 15.1 The Chinese Web already controlled off-Web devices

By 1999, at least in officially reported service architecture, Web/email events could enter paging networks.

So “old Web” was never only pages viewed on desktop monitors.

It could be an interface into:

- telecom networks;
- portable receivers;
- later SMS/mobile systems.

### 15.2 Web evidence can survive while the actual historical action channel disappears

This is a major archive asymmetry:

> **public interface longevity > private service-state longevity > transport-network longevity**

### 15.3 Online/offline was already porous before smartphones

A dial-up user did not have to remain logged into email to be notified of an arriving message if an email-to-pager gateway was configured.

That creates an early form of asynchronous ambient notification.

But it is not the same as full smartphone ambient Internet: the pager had much less content, interaction and reply capability.

### 15.4 Boundary controls are part of old-Web UI history

Fields such as `禁呼时间` deserve preservation alongside page layout and graphics because they encode social assumptions about when a person should be reachable.

---

## 16. Evidence table

| Claim | Evidence | Grade | What it proves | What it does not prove |
|---|---|---:|---|---|
| end-1999 online paging across 198/199 national + many provincial networks | 1999 communication bulletin excerpt | A-/B+ | feature/network deployment claim | actual subscriber adoption |
| email-arrival paging in 22 provincial networks | same | A-/B+ | gateway capability claim | individual email delivery |
| 1999 Web-configurable quiet/filter periods in Tencent/SINET system | Tencent dated corporate archive | B+ | preserved historical system description | verified original 1999 DOM/capture |
| public paging network shutdown process in 2007 | MII-notice-based contemporary reports | B | network/service lifecycle boundary | every private pager network ended |
| one-way pager typically requires callback infrastructure | Smithsonian device description + personal accounts | A+B/C | device topology | every later pager remained one-way |
| two-way paging existed in 1996 US market | WIRED contemporary review | B | technical counterexample | mass adoption |

---

## 17. Hindsight risks

### Risk 1: “1999 email-to-pager was basically push notification”

Too strong.

It is a useful structural precursor, but message volume, UI, interaction, pricing, coverage and social expectation were radically different.

### Risk 2: “online paging existed, therefore normal users used it”

No.

Exists/available/used/popular remain separate.

### Risk 3: treating a current Tencent archive page as a 1999 capture

Do not.

The date and corporate provenance are useful, but the original Web artifact still needs independent archive verification.

### Risk 4: recovering personal pager numbers to make the archaeology feel concrete

Usually unnecessary and privacy-invasive.

Study the service contract and state machine instead.

### Risk 5: treating 2007 as the universal end of paging

Public Unicom network closure is not identical to all private/organizational use.

---

## 18. What we know / infer / do not know

### What we know

- Official communications reporting described online paging and email-arrival paging deployed by end-1999.
- A dated Tencent corporate archive describes Web-configured forwarding/quiet/filter rules in a 1999 trial system.
- Public national paging services were being formally closed in most of China in 2007.
- One-way and two-way pager architectures both existed internationally.

### What we can reasonably infer

- The Chinese old Web briefly formed part of a hybrid Internet→telecom→RF→human notification stack.
- A page archive cannot capture most of the transaction states that mattered to users.
- Shutdown of paging transport makes surviving forms especially misleading if interpreted as executable historical systems.

### What we do not yet know

- Exact original URLs for many national/provincial online-paging forms.
- Exact 1999–2001 DOM, charset and browser assumptions.
- Subscriber counts for 网上寻呼 / 邮件到达呼.
- Actual delivery success rates.
- How often ordinary users enabled quiet/filter rules.
- Whether archived dynamic confirmation pages survive in Wayback or other collections.

---

## 19. Next research packet

The next high-value old-Web evidence is not another retrospective article.

Find one **verified 1999–2003 Chinese online-paging or email-arrival-paging capture** and record:

1. original/capture URL;
2. capture datetime;
3. operator/site identity;
4. charset;
5. browser/form dependencies;
6. visible fields;
7. message limits;
8. authentication assumptions;
9. any `禁呼时间` / filter / forwarding controls;
10. exact success/error wording;
11. which subresources are missing;
12. whether the form action points to a dead backend;
13. whether any external telecom gateway protocol is documented elsewhere.

Then stop at the strongest claim the capture supports.

The key archaeological question is:

> **When the HTML survives but the radio network no longer exists, what exactly has the archive preserved: a page, a service description, or an executable communication system?**
