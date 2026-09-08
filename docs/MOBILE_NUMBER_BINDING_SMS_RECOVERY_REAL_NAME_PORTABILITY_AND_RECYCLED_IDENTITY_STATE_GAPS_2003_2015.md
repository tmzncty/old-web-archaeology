# Mobile Number Binding, SMS Recovery, Real-Name Registration, Portability, and Recycled-Identity State Gaps (China, 2003–2015)

> Scope: Chinese Web/mobile-number interaction, approximately 2003–2015. The core archaeological target is how a telephone number moved from a contact field into account binding, password recovery, payment/security, real-name subscriber records and — in pilot regions — carrier portability.
>
> 2018–2026 material appears only as afterlife evidence to expose what early systems had already made possible and what they failed to clean up.
>
> This is **not** a general history of Chinese mobile telecommunications, SIM cards, 2G/3G/4G, or WeChat. It is a transaction-state study of the boundary between a telecom number and Web identity.

Companion life-history package:

- `tmzncty/how-people-lived/topics/from-place-bound-phone-to-portable-identity-anchor-mobile-numbers-number-portability-and-account-continuity-china-1987-2026.zh-CN.md`

---

## 0. Why this belongs in old-web-archaeology

A Web archive can preserve a page saying:

> “绑定手机后可以找回密码。”

That does **not** tell us:

- which number was actually bound;
- whether the SMS was delivered;
- whether the SIM was still controlled by the same person;
- whether the subscriber registration matched the account operator;
- whether a later recycled-number user could receive the same recovery SMS;
- whether changing carrier changed routing or third-party service behavior;
- whether the account was ultimately recovered.

This topic is therefore a strong example of why old-Web archaeology must separate **visible interface state** from **private cross-system state**.

The central warning is:

> **a phone number printed in a form is not yet an identity; it becomes identity-like only through several independently maintained databases.**

---

## 1. Core transaction model

### 1.1 Binding lifecycle

Never collapse “手机绑定成功” into one undifferentiated state.

```text
TELECOM_NUMBER_ACTIVE
  -> USER_CONTROLS_SIM
  -> PLATFORM_BINDING_PAGE_REACHABLE
  -> USER_ENTERS_NUMBER
  -> PLATFORM_CREATES_PENDING_BINDING
  -> SMS_GENERATED
  -> SMS_ROUTED
  -> SMS_DELIVERED_TO_CURRENT_SIM
  -> USER_ENTERS_CODE / SENDS COMMAND
  -> PLATFORM_ACCEPTS PROOF
  -> BINDING_COMMITTED
  -> PHONE_RECOVERY_AVAILABLE
```

Possible failure/exception branches:

```text
SMS generated
  -> not delivered / delayed / routed incorrectly

code received
  -> expired / rejected / wrong session

binding committed
  -> attacker or different person later controls SIM

number cancelled
  -> platform binding remains
```

### 1.2 Password-recovery lifecycle

```text
RECOVERY_REQUEST
  -> ACCOUNT IDENTIFIED
  -> BOUND_NUMBER LOOKUP
  -> SMS CHALLENGE GENERATED
  -> SMS DELIVERED
  -> CHALLENGE SATISFIED
  -> PASSWORD RESET AUTHORIZED
  -> NEW CREDENTIAL COMMITTED
  -> OLD SESSIONS INVALIDATED? [unknown by product]
```

Important gaps:

- `SMS sent != SMS delivered`
- `SMS delivered != correct historical account owner received it`
- `number possession != durable account ownership`
- `phone bound != account recoverable in every failure mode`
- `recovery accepted != all old sessions revoked`
- `binding page exists != ordinary users actually adopted it`

### 1.3 Telecom-number lifecycle

```text
NUMBER AVAILABLE
  -> NUMBER ASSIGNED
  -> SIM ACTIVE
  -> SUBSCRIBER REGISTERED / NOT YET FULLY VERIFIED
  -> NUMBER USED
  -> SUSPENDED
  -> CANCELLED
  -> QUARANTINE / RECYCLING PROCESS
  -> REISSUED TO NEW SUBSCRIBER
```

The Web-platform lifecycle is independent:

```text
OLD_PLATFORM_ACCOUNT
  -> number binding remains
  -> number cancelled by OLD_USER
  -> same digits later assigned to NEW_USER
  -> platform still sends SMS to same digits
```

This cross-system race produces:

> **identity residue / 号码身份残留**

---

## 2. Pre-Web boundary: personal-number continuity is older than Web identity

The mobile-number story must not begin with QQ or smartphones.

By 2000 Q1, Chinese mobile users exceeded 50 million and mobile traffic volume first surpassed fixed-phone traffic under the Ministry of Information Industry’s accounting method. By 2001 July mobile subscriptions were around 120 million; by 2005 mobile subscriptions exceeded fixed-line subscriptions nationally.

Context sources:

- 2000-05-23 contemporary report citing MII: <https://news.sina.com.cn/china/2000-05-23/91712.html>
- 2001-08-24 People’s Daily historical page: <https://cn.govopendata.com/renminribao/2001/8/24/6/>
- MII 2002-06 statistical bulletin: <https://www.miit.gov.cn/gxsj/tjfx/txy/art/2020/art_9918596d71124956b23b556ea6c370b4.html>
- National Bureau of Statistics summary through 2005: <https://www.stats.gov.cn/zt_18555/ztfx/15cj/202303/t20230301_1920491.html>

These are **context**, not evidence that every household had a phone or that mobile numbers were already identity anchors.

The relevant prehistory is simpler:

```text
fixed line: place/household/unit -> number
mobile line: person carrying handset/SIM -> number can move with person
```

The Web later reuses this already-portable address.

---

## 3. 2004 counterexample: number continuity was not yet universally “sacred”

A 2004 Harbin Daily local survey reported that 58.3% of respondents had changed mobile numbers and 47.3% said they would change operator and number for tariff reasons.

- <https://news.sohu.com/20040901/n221828125.shtml>

Evidence grade: **B**.

Limitations:

- local Harbin sample;
- methodology not sufficient for national inference;
- no claim should be made that “58.3% of Chinese mobile users changed numbers”.

Archaeological value:

This prevents a back-projection from the app era.

> `mobile number important in 2026` does not prove `mobile number was already prohibitively costly to change in 2004`.

The state history we need to reconstruct is precisely how the number accumulated additional dependencies.

---

## 4. 2005: mobile binding enters Web-account recovery

A 2005 contemporary report about the online game `热血江湖` describes a newly added mobile-password-protection function. Users could bind a mobile number, use SMS to retrieve an account password, and use a Web query path involving the phone number/member information to inspect binding-related state.

- 2005-09-05, Sina Games: <https://games.sina.com.cn/o/n/2005-09-05/1603124246.shtml>

Evidence grade: **B** — contemporary product/operation reporting.

### What this supports

By 2005, at least some Chinese Web services had explicit transaction paths in which telecom control became evidence for Web-account control:

```text
mobile number
-> SMS channel
-> recovery proof
-> account credential change/recovery
```

### What it does not support

Do not infer:

- all game accounts used mobile binding;
- SMS recovery was mandatory;
- mobile binding was free;
- the same protocol was used by QQ, banks, Taobao, etc.;
- every SMS was reliably delivered;
- the currently visible Sina article reproduces an original product help page.

### Historical capture status

This run identified the contemporary article URL but did **not** recover and inspect a qualifying 2005 historical replay of the underlying game help/binding application.

Therefore:

- original host/path of the binding application: **unknown**;
- HTML/DOM/frames: **unknown**;
- charset: **unknown**;
- session/cookie model: **unknown**;
- SMS gateway request path: **unknown**;
- POST vs GET behavior: **unknown**;
- browser requirement: **unknown**.

---

## 5. 2006–2007: QQ cases expose `phone bound / account secure` as a false equivalence

A 2006 Beijing newspaper report on QQ theft described a failure mode in which a stolen account could be associated with the thief’s mobile phone, leaving the original user to pursue an appeal/unbinding path.

- 2006-09-20, 京华时报 via Sohu: <https://news.sohu.com/20060920/n245445345.shtml>

A 2007 Chinanews case described a paying QQ user who had used the account for five to six years and had important work contacts reaching them through it. The account had mobile binding, but after theft the mobile self-service recovery path did not simply restore control.

- 2007-11-16, Chinanews: <https://www.chinanews.com.cn/sh/news/2007/11-16/1079503.shtml>

Evidence grade: **B** — contemporary media with user claims.

### Archaeological use

These sources prove neither platform security quality nor theft prevalence. They are useful as **state-boundary probes**:

```text
phone bound
!= only legitimate owner can ever change the binding

phone recovery feature exists
!= every stolen account can be recovered automatically

account is long-lived
-> more real-world contacts may depend on it
-> failure has larger offline consequence
```

The account itself had become an ordinary-life address; the phone number then became one of the mechanisms for preserving that address.

---

## 6. The hidden architecture: two independent identity graphs

By the mid-2000s, the user can be represented in at least two systems:

### Telecom graph

```text
number
-> SIM/USIM
-> operator account
-> subscriber registration
-> billing/service state
```

### Web graph

```text
platform account
-> username / QQ ID / member ID
-> password
-> bound mobile number
-> recovery state
-> payment / premium status
```

The same decimal phone number is the join key, but neither system owns the complete truth about the person.

Therefore the following are unsafe assumptions:

```text
telecom says NEW_USER owns number
=> platform should know old binding is invalid      [false unless synchronized]

platform says account bound to number
=> current telecom subscriber is original account owner   [false after recycling]
```

This is the basic architecture behind later recycled-number failures.

---

## 7. 2010–2013 real-name registration: `registered / authenticated / actual user` must remain separate

From 2010-09-01, new prepaid mobile subscribers were required to register real identity information. Contemporary material emphasized that prepaid cards were still widely sold through dispersed retail channels.

- 2010-08-20 policy/report relay: <https://www.edu.cn/wisafety_9958/20100820/t20100820_512090.shtml>

Contemporary reporting immediately after implementation documented that some street/retail sales did not yet consistently perform the requested identity process.

The 2013 reinforcement of phone real-name requirements again raised the distinction between merely entering subscriber information and actually authenticating identity.

- 2013-09-02, Chinanews: <https://www.chinanews.com.cn/sh/2013/09-02/5231311.shtml>

### Required role split

Never model “手机号用户” as one actor without qualification.

At minimum:

```text
REGISTERED_SUBSCRIBER
ACTUAL_SIM_USER
PLATFORM_ACCOUNT_OPERATOR
PAYER / FAMILY MEMBER / EMPLOYER [where relevant]
```

They may coincide. Historical reconstruction must not assume they do.

### State distinctions

- `subscriber data entered != identity authenticated`
- `identity authenticated != SIM never lent/transferred`
- `registered subscriber != platform-account legal/actual owner`
- `real-name rule exists != every retail transaction complied immediately`

This is precisely the kind of `exists / available / used` distinction required by the repo METHOD.

---

## 8. 2010–2014 number-portability pilots: the number begins to separate from the carrier

China’s first mobile number-portability pilots began in Tianjin and Hainan on 2010-11-22; Hainan expanded to two-way portability in 2014; Jiangxi, Hubei and Yunnan joined a second batch in September 2014.

Later official national-launch material preserves the pilot chronology:

- 2019-11-27, Xinhua via CAC: <https://www.cac.gov.cn/2019-11/27/c_1576389972372088.htm>

The later source is **A for the government’s official retrospective chronology**, but it is not a 2010 Web capture.

### State model for portability

A porting transaction should be reconstructed as something closer to:

```text
CURRENT_NUMBER_ACTIVE
  -> ELIGIBILITY CHECK
  -> CONTRACT / ACCOUNT RESTRICTIONS CHECK
  -> AUTHORIZATION TOKEN / REQUEST
  -> TARGET_CARRIER ACCEPTS REQUEST
  -> PORT ORDER CREATED
  -> CROSS-CARRIER ROUTING STATE UPDATED
  -> TARGET SIM ACTIVATED
  -> VOICE TEST
  -> SMS TEST
  -> DATA TEST
  -> THIRD-PARTY SERVICE TEST
```

Important gaps:

- `eligible != request submitted`
- `request accepted != routing updated`
- `routing updated != every service works`
- `number retained != original carrier contract/benefits retained`
- `carrier changed != third-party app binding changed`

### What remains unknown for 2010–2014

This run did not recover verified historical user-facing portal captures for the Tianjin/Hainan or second-batch pilots.

Unknown:

- whether eligibility checking was Web, SMS, shop-counter, telephone, or mixed at each date;
- exact historical hosts and paths;
- form fields;
- browser assumptions;
- error messages;
- authentication method;
- routing-database synchronization latency;
- SMS short-code workflow;
- user-visible port-status states.

Do not reconstruct these from the 2019 national process.

---

## 9. 2014 recycled-number evidence: the strongest state-gap proof in the main scope

A 2014 Beijing Youth Daily / People’s Daily report described a user receiving a recycled mobile number and then seeing communications associated with the prior holder, including financial notifications; the report also discussed old Taobao/Alipay bindings and the possibility that SMS validation could expose old account state to the new holder.

- 2014-09-15, People.cn: <https://society.people.com.cn/n/2014/0915/c1008-25661203.html>

Evidence grade: **B**.

This is not evidence that every recycled number exposed an account. It is strong evidence for the possibility of the following cross-system state:

```text
TELECOM:
OLD_USER -> CANCELLED
NUMBER -> REISSUED
NEW_USER -> ACTIVE

PLATFORM:
OLD_ACCOUNT -> STILL_BOUND_TO_SAME_DIGITS
```

### Core archaeological distinction

> **carrier lifecycle completion != platform lifecycle completion**

A telecom operator can validly reassign a number while a Web platform still has a perfectly valid-looking database row that says:

```text
account.mobile = same_digits
```

No Web page screenshot alone can tell us which person the digits corresponded to at a later date.

---

## 10. A state variable old Web archives almost never preserve: `binding_created_at`

The recycled-number problem demonstrates why a phone-number binding should be modeled as a temporal relation, not a timeless property.

Instead of:

```text
account -> phone_number
```

historically safer reconstruction is:

```text
account
-> phone_number
-> binding_created_at
-> binding_verified_at
-> subscriber-control interval
-> last_reverified_at
-> unbound_at
```

Without time, the same digits can falsely collapse two people into one identity.

This becomes especially important after number recycling.

---

## 11. Afterlife boundary: 2018–2019 makes the hidden binding graph visible

This section is outside the repo’s main 1995–2015 scope and is used only as afterlife evidence.

### 11.1 2018: ordinary users no longer know all places where a number exists

A 2018 People.cn report about recycled numbers described a newly graduated user moving to a new city, obtaining a new number, and receiving the previous user’s financial messages. The article contrasted earlier number changes — largely an address-book notification problem — with the app era, where users may not remember how many third-party services contain the number.

- 2018-11-12: <https://society.people.com.cn/n1/2018/1112/c1008-30396405.html>

This supports:

> **binding-graph opacity / 用户无法直接观察完整绑定图**

### 11.2 2019: number continuity becomes an explicit reason for number portability

A 2019 People.cn report quoted a Beijing user describing how changing numbers in 2018 consumed substantial time and effort because so many services and contacts needed updating.

- 2019-04-03: <https://finance.people.com.cn/n1/2019/0403/c1004-31012251.html>

This afterlife evidence explains why the 2010–2014 pilot should not be read solely as tariff competition: the number had become a continuity object.

### 11.3 2019 national launch confirms portability is not application portability

The national launch report says trial users still reported failures after porting, including network access, recharge and some application services.

- <https://www.cac.gov.cn/2019-11/27/c_1576389972372088.htm>

Therefore:

```text
PORT_COMPLETE
!= THIRD_PARTY_SERVICE_GRAPH_PORTABLE
```

This is a durable state distinction that should be applied when reconstructing 2010–2014 pilots.

---

## 12. Afterlife boundary: 2020 shows a service may remember a phone number after the user considers it dead

A 2020 Beijing Health Kit case documented users who had bound phone numbers on WeChat/Alipay versions of the service; a number that the user regarded as no longer in use could still have to pass travel-history verification for a defined period after unbinding.

- 2020-11-25, Beijing Youth Daily via People.cn: <https://bj.people.com.cn/n2/2020/1125/c14540-34435865.html>

This is outside main scope and should **not** be back-projected into 2010 systems.

Its archaeological value is conceptual:

> **user stops using number != service immediately forgets number**

A platform may intentionally retain a historical association for time-bounded logic.

Call this:

> **binding-memory latency / 绑定记忆延迟**

---

## 13. Afterlife boundary: 2022–2026 turns old bindings into an explicit cross-platform cleanup service

In June 2022, CAICT’s `一号通查` introduced phone-number account query/unbinding functions. Contemporary reporting emphasized an important boundary: the service could remove relationships registered **before the current user obtained the recycled number**, while accounts bound during current ownership were not automatically removed under the same rule.

- 2022-06-08, People.cn: <https://finance.people.com.cn/n1/2022/0608/c1004-32441591.html>

By 2025–2026, telecom regulators/operators described `二次号码焕新` as a service in which operators/CAICT coordinate with Internet platforms to clear prior-owner bindings.

- 2025-05-16, Heilongjiang Communications Administration: <https://hljca.miit.gov.cn/xwdt/gzdt/art/2025/art_68d9615319fd4df4b6be6d261e094062.html>
- 2025-10-28, MIIT service-quality bulletin: <https://www.miit.gov.cn/zwgk/zcwj/wjfb/tg/art/2025/art_30a89a6098804ec1944aeabe6a999b9e.html>
- 2026 Q1 MIIT bulletin: <https://www.miit.gov.cn/jgsj/xgj/wjfb/art/2026/art_983eaf483b80451c8b49d6b34e1ebe08.html>
- 2026 Q2 MIIT bulletin: <https://wap.miit.gov.cn/zwgk/zcwj/wjfb/tg/art/2026/art_440c2ded2ba54f0387b4cca50acf8147.html>

### Why this matters archaeologically

The cleanup service effectively asks every participating platform to respect a temporal boundary that early account databases often did not expose to users:

```text
OLD binding happened before NEW subscriber acquired number
-> eligible for cleanup path

binding happened during NEW subscriber ownership
-> different responsibility / no automatic blanket cleanup
```

This is an afterlife solution to a state gap already visible in 2014.

---

## 14. Overseas comparator: US number portability shows that the continuity problem predates app ecosystems

The US FCC’s 1996 number-portability order treated the ability to retain a number while switching carriers as necessary for meaningful provider choice and competition.

- FCC 96-286: <https://docs.fcc.gov/public/attachments/FCC-96-286A1.pdf>
- Federal Register version: <https://www.govinfo.gov/content/pkg/FR-1996-07-25/pdf/96-18477.pdf>

In 2003, just before wireless portability took effect in major US markets, the Washington Post reported that losing a mobile number had long deterred users from changing carriers; for contractors and other people whose mobile number had become part of their professional identity, retaining the number was especially valuable.

- 2003-11-04: <https://www.washingtonpost.com/archive/lifestyle/2003/11/04/for-cell-users-safety-in-numbers/3725673c-287e-463d-b8aa-0f3e13064ca3/>

Cross-country conclusion:

> `number continuity as switching cost` is not a Chinese-app-era invention.

What later becomes especially visible in China is the stacking of:

- massive mobile adoption;
- real-name subscriber rules;
- SMS account recovery;
- super-app/payment binding;
- carrier portability;
- number recycling.

---

## 15. Browser and interface questions that remain unresolved

For the 2003–2015 main scope, the following remain **unknown** unless stronger technical evidence is recovered.

### Account-binding pages

- exact QQ/Game/Taobao/Alipay binding hosts and paths by year;
- whether forms were GET/POST;
- charset (`GB2312`, `GBK`, `UTF-8`, mixed);
- frames/iframe dependencies;
- JavaScript validation;
- image CAPTCHA;
- cookie/session behavior;
- whether mobile number was stored before SMS verification;
- whether “绑定成功” reflected database commit or only front-end state;
- SMS gateway provider and callback mechanism;
- delivery receipts.

### Password recovery

- token expiry semantics;
- resend limits;
- how account/number matching was looked up;
- whether a successful reset invalidated existing sessions;
- fallback to email/security questions/manual appeal;
- whether an attacker could bind a new phone before old owner recovery.

### Real-name registration

- retail-terminal software;
- offline/online identity validation;
- retry and failure states;
- how old non-real-name numbers were migrated;
- relationship between operator CRM and public-security verification at each date.

### Portability pilot

- exact user-facing portals in Tianjin/Hainan/Jiangxi/Hubei/Yunnan;
- eligibility-query channel;
- authorization-code semantics before the 2019 standardized process;
- routing database architecture and update latency;
- SMS/MMS/value-added-service compatibility;
- failure and rollback screens.

Do not fill these gaps from modern help pages.

---

## 16. Historical locator / capture ledger

### Confirmed contemporary locators/articles

| Date | Locator | What it can support | Grade |
|---|---|---|---|
| 2004-09-01 | `news.sohu.com/20040901/n221828125.shtml` | local survey on switching numbers for tariffs | B |
| 2005-09-05 | `games.sina.com.cn/o/n/2005-09-05/1603124246.shtml` | contemporary description of mobile password protection | B |
| 2006-09-20 | `news.sohu.com/20060920/n245445345.shtml` | QQ theft/binding/recovery failure case | B |
| 2007-11-16 | `chinanews.com.cn/.../1079503.shtml` | long-lived QQ account + phone recovery failure | B |
| 2014-09-15 | `society.people.com.cn/n/2014/0915/c1008-25661203.html` | recycled-number / old-binding state gap | B |

### Capture status

This run attempted to advance archive checking for the 2005 Sina Games and 2006 Sohu URLs. The current access path did **not** yield a historical replay that could be opened and inspected under the repository’s `docs/METHOD.md` contract.

Therefore:

> **M1: NOT ACHIEVED IN THIS SLICE.**

Do not rewrite this as “Wayback has no copy”.

The correct negative result is:

> `qualifying historical replay not verified in this run`.

---

## 17. Why a modern-hosted old article is not a historical capture

Several useful 2004–2007 pages remain accessible today at Sina/Sohu/Chinanews URLs. That is valuable contemporary textual evidence, but it does not prove:

- the current HTTP response is the 2005 response;
- current HTML is original HTML;
- original charset is preserved;
- images/scripts are original;
- cookies/session behavior survives;
- article URLs were rendered with the same template;
- underlying linked service pages remain reachable.

Label these as:

> **currently accessible contemporary text**

not automatically:

> **verified historical Web capture**.

This distinction follows `docs/METHOD.md` directly.

---

## 18. Privacy rule: never preserve phone numbers merely because old pages exposed them

This topic is unusually privacy-sensitive.

Do not copy into the repository:

- historical ordinary users’ full mobile numbers;
- phone-number/QQ/account binding pairs;
- SMS codes;
- account-recovery screenshots containing real identifiers;
- lists of recycled numbers that reveal prior holders;
- private contact books.

For structural evidence, use placeholders:

```text
139XXXXXXXX
ACCOUNT_A
OLD_SUBSCRIBER
NEW_SUBSCRIBER
```

If a public help page includes example digits, preserve only what is necessary to understand the schema.

A historical archive’s accessibility is not consent for republishing account-recovery identifiers.

---

## 19. Evidence grades

### A — official/original administrative evidence

- MII/MIIT and National Bureau of Statistics telecom statistics;
- official 2019 portability launch/chronology;
- 2025–2026 MIIT `二次号码焕新` service bulletins;
- FCC 1996 portability order (overseas comparison).

### B — contemporary secondary/operational evidence

- 2004 Harbin local survey;
- 2005 Sina Games mobile-password-protection description;
- 2006–2007 QQ theft/recovery cases;
- 2014 recycled-number account-binding report;
- 2018–2019 afterlife user cases;
- 2020 Health Kit number-binding incident.

### C — later recollection

Not needed for the main claims in this slice. If later oral histories about first mobile phones/number changes are added, they must not be used to reconstruct precise Web UI or feature launch dates.

### D — reconstruction/inference

State diagrams in this note are analytical reconstructions. They are **not** recovered database schemas.

---

## 20. Known / probable / unknown

### Known

- mobile-phone adoption grew rapidly during 2000–2005;
- by 2005 at least some Web services used SMS/mobile binding for credential recovery;
- mobile binding did not guarantee recovery in every account-theft case;
- real-name subscriber rules tightened during 2010–2013;
- number-portability pilots operated in selected provinces/municipalities from 2010/2014;
- recycled numbers could remain linked to previous users’ Internet accounts by 2014;
- national portability in 2019 still encountered third-party/application compatibility problems;
- later `二次号码焕新` explicitly targets pre-current-owner bindings.

### Probable

- as account binding accumulated, changing numbers became more laborious for many users;
- Web platforms generally treated SMS reception as a strong, though not perfect, proxy for current number control;
- historical platform databases frequently lacked direct knowledge of telecom reassignment events.

These should remain analytic claims, not be presented as universal system architecture without source code/technical documentation.

### Unknown

- exact architecture of 2005–2007 binding services;
- original browser/charset requirements;
- SMS gateway implementations;
- historical bind/unbind database schemas;
- cancellation-to-reissue intervals by operator/year;
- early portability portal state machines;
- prevalence of recycled-number account exposure in 2014;
- exact fraction of ordinary users whose number-change decision was dominated by digital-account costs before 2015.

---

## 21. Hindsight risks

1. **Do not back-project app-era lock-in to 2004.** A local contemporary survey shows number changing could still be common.
2. **Do not equate real-name policy with perfect enforcement.** Retail execution and authentication mattered.
3. **Do not equate possession of digits with ownership of old platform accounts.** Recycled numbers prove why.
4. **Do not equate portability with complete service portability.** Carrier routing and app/service state are separate.
5. **Do not infer Web self-service from backend digitization.** Telecom/CRM/SMS infrastructure can be digital while the user interacts by shop/SMS/telephone.
6. **Do not call a currently reachable 2005 article a verified 2005 replay without archive metadata.**
7. **Do not generalize rare account-theft/recycled-number cases into prevalence claims.** Use them to prove possible state gaps.

---

## 22. What this changes in old-Web archaeology

This slice adds an object that is neither simply “a website” nor simply “a telecom service”:

> **a cross-platform identifier whose meaning changes over time.**

It forces the repository to preserve three clocks simultaneously:

```text
telecom ownership clock
platform binding clock
human relationship/account clock
```

The same digits can remain constant while the person, carrier, platform account, or legal subscriber changes.

That means old-Web identity reconstruction must stop treating a phone number as a timeless key.

A surviving 2005 account page saying `绑定手机：139...` does not prove who controlled that number in 2014, and a 2014 SMS delivered to those digits does not prove the recipient was the 2005 account owner.

---

## 23. Next evidence targets

High-value next steps:

1. find a verified 2005–2007 historical capture of a QQ/game mobile-binding or password-recovery page;
2. recover contemporary operator manuals for 2010 Tianjin/Hainan portability pilots;
3. identify first-party telecom documentation on cancellation/quarantine/reissue intervals before 2015;
4. find Taobao/Alipay/QQ first-party help pages that explicitly instruct users to unbind before number cancellation;
5. compare email/security-question recovery with SMS recovery in the same account product over time;
6. look for archived browser requirements, charset and form submission behavior;
7. preserve error/negative states where legally and ethically possible, not only success pages.

---

## 24. Research-saturation status

This run found several mechanisms not previously isolated in the two-repository cross-study:

- phone number as a **portable personal address**;
- **identity accretion** from contact endpoint to Web-account control endpoint;
- **carrier portability vs application portability**;
- **telecom lifecycle vs platform-binding lifecycle**;
- **recycled-number identity residue**;
- **binding-memory latency**;
- the need for **temporal ownership boundaries** in identity archaeology.

Therefore this is a substantive new category and the no-new-findings saturation count remains/reset to **0**.

---

## Conclusion

The early Chinese Web did not merely “add phone numbers to forms”. It gradually made the phone number a bridge between two independently evolving systems:

```text
telecom network
<-> mobile number
<-> Web account
```

That bridge was useful precisely because the number could follow a person across places. It later became fragile precisely because the number could also be cancelled, reassigned, or moved between carriers while Web databases remembered older associations.

For old-Web archaeology, this means the most important artifact is often not the surviving binding page. It is the **missing relation state** behind the page.

> **The page can survive while the identity relation that once made it true has already moved to another person.**
