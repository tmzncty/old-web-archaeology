# Dial-up metered sessions, phone-line contention, and access-context loss, 1997–2003

> Scope: 中文 Web 约 1997—2003 年的**访问环境考古**。本文件不再增加一个近义 `page visible != transaction complete` state-gap，而回答另一个此前没有单独建模的问题：即使历史 HTML 被完整保存，今天的 replay 仍可能把当年最重要的一部分 Web 体验抹掉——**拨号、计时、电话线争用、双重资费、慢速渐进加载、Cache/离线浏览和家庭共享账号。**
>
> Companion ordinary-life file: `tmzncty/how-people-lived/sources/contemporaneous-dial-up-household-time-bills-and-phone-line-decoupling-china-1997-2003.zh-CN.md`.

本文件遵守 `docs/METHOD.md` 和 `docs/RESEARCH_SATURATION_DEDUP_AND_ARTIFACT_PRIORITY_AUDIT_2026-09-12.md` 的去重门禁。它提供的是一个新的**preservation / reconstruction failure mode**，而不是更多状态不等式：

> **A verified historical page capture can still fail to reconstruct the historical access experience if the access contract has disappeared.**

本文把这种缺失暂称为：

> **access-context loss（访问语境损失）**。

---

## 1. Why access itself must become an archaeological object

Old-Web reconstruction usually asks:

```text
What URL existed?
What capture datetime?
What HTTP response?
What charset?
What HTML / frames / CSS / JavaScript?
Which subresources survived?
Which browser assumptions were required?
```

For Chinese household Web around 1997–2003, this is necessary but not sufficient.

A user often also needed:

```text
computer
+ modem / ISDN / early broadband terminal
+ physical telephone line or other access circuit
+ dial number
+ ISP account / prepaid card / credential
+ network-use tariff
+ telephone-call tariff
+ available household line time
+ successful dial / handshake / port availability
+ enough connected minutes to load the page
```

Therefore a historically faithful access model is closer to:

```text
page artifact
+ access topology
+ tariff clock
+ household resource topology
+ client strategy
```

not page artifact alone.

---

## 2. Strong contemporary evidence: waiting was literally billable

A 1999 *Computer News* commentary gives a first-person description of self-paid Internet access. The author compared browsing to sitting in a taxi stuck in traffic while the meter keeps moving. After several months online, he complained that his scarce Internet budget was consumed by `wait`, while a sharply larger telephone bill triggered family criticism.

Source:

- 《电脑报》/新浪科技, 1999-10-13, 《评论：话说中国电信，一张网住网络的“网”》: https://tech.sina.com.cn/news/review/1999-10-13/8550.shtml

Evidence grade: **B** — contemporaneous first-person commentary, not population-representative.

This gives a reconstruction rule:

> **render latency could be monetary latency.**

A slow image, frame, Java component, redirect, DNS lookup or failed download could consume not only patience but metered access time.

An archive replay that renders the same page instantly in 2026 therefore risks converting:

```text
historical economic/temporal friction
```

into:

```text
apparently frictionless visual content
```

---

## 3. The meter was not necessarily one meter

The 1999 national tariff change for China Telecom dial-up access set the network-use basic fee at RMB 4/hour for the first 60 hours per month and RMB 8/hour above 60 hours. Local telephone charges for Internet sessions existed alongside network-use charges and were adjusted separately.

Sources:

- 国家计委, 计价格〔1999〕134号, 1999-02-10, 《关于调整邮政电信资费的通知》 reprint: https://law1.110.com/law_28485.html
- 湖北省实施通知, 1999-02-26: https://law1.110.com/law_232798.html

Evidence grade: **A-ish regulatory text reprints**; exact local implementation must still be checked by jurisdiction.

A Beijing report later that year stated that from 1999-12-01 the Internet call charge for China Telecom 163 dial-up users would fall from RMB 0.18 per three minutes to RMB 0.09 per three minutes, while 169, 263 and other ISP users would temporarily continue under the old call-charge rate.

Source:

- 《北京晚报》/新浪, 1999-11-30, 《上网话费明起减半 优惠只限163》: https://news.sina.com.cn/china/1999-11-30/36695.html

Evidence grade: **B** — contemporary implementation report.

This means that a historical Web reconstruction may need at least two cost states:

```text
ISP / network-use clock
+
PSTN local-call clock
```

and the dial number / ISP could alter which tariff applied.

### 3.1 Archaeological consequence

A page's historical access cost cannot be inferred from HTML size alone.

It may depend on:

- which ISP the user called;
- which access number was recognized by the telephone billing system;
- local tariff rules;
- time of day;
- failed or repeated dials;
- link speed and line quality;
- whether content was cached;
- whether images/Java were suppressed;
- whether the user downloaded for offline reading.

Therefore:

> **same page bytes != same historical access cost**.

---

## 4. Contemporary user guidance shows that the client was actively shaped around the meter

A 2001 popular technical guide advised users to prepare before dialing, start software and browser windows first, reduce multimedia requests, disable Java, exploit browser Cache, use offline browsers such as WebZIP, and avoid writing e-mail while connected.

Source:

- 人民网-华东新闻/新浪科技, 2001-10-10, 《上网冲浪需具备的七个好习惯》: https://tech.sina.com.cn/i/c/2001-10-10/87279.shtml

Evidence grade: **B** — contemporary technical advice.

This is important for artifact interpretation because it means the historical user may not have consumed the page as the server intended.

A nominal page might contain:

```text
text
+ GIF/JPEG images
+ Java
+ multiple linked subpages
```

while the actual user intentionally requested:

```text
text only
+ cached assets
+ no Java
+ batch download now
+ reading later offline
```

So:

> **historical server representation != historical user-consumed representation**.

That difference is not only a browser-compatibility issue; it can be a deliberate cost-control strategy.

---

## 5. The browser session could compete with the household telephone itself

Dial-up over an ordinary household telephone circuit did not merely use a familiar wire; it transformed the line into a data session while connected.

The strongest contemporary Chinese evidence for the household consequence appears at the transition to ADSL.

On 2001-07-27, *Beijing Evening News* reported that after telephone installation fees were abolished, many households that already had a telephone were ordering another line specifically for more convenient Internet access. The report noted that much residential plant had originally been planned around one line per household and that the new demand could strain line capacity.

Source:

- 《北京晚报》/新浪科技, 2001-07-27, 《北京电信7月27日开通“超级一线通”》: https://tech.sina.com.cn/it/t/2001-07-27/77899.shtml

The next day's ADSL launch report promoted one of the central advantages as simultaneous Internet and telephone use, and explicitly said ADSL Internet no longer generated an Internet call charge because the data session did not occupy the telephone line in the old way.

Source:

- 《北京晚报》/新浪科技, 2001-07-28, 《北京电信开通上网不交电话费的家庭ADSL服务》: https://tech.sina.com.cn/i/c/2001-07-28/77958.shtml

Evidence grade: **B** — contemporary service/urban reporting.

This supports a distinct historical resource state:

> **household-line contention**.

For a one-line household, “a person is online” could imply “the household's ordinary voice path is unavailable or constrained.”

That is not visible in a saved homepage.

---

## 6. ADSL changed access topology before it necessarily created unlimited access

The Beijing 2001 ADSL offer is especially useful because it prevents a simplistic transition story.

The service offered:

- 512K downstream access;
- data/voice coexistence on the same copper pair;
- no separate Internet local-call charge;
- but 40h / 100h / 200h monthly usage packages;
- excess-minute charges;
- substantial installation / equipment-related upfront costs.

Source:

- https://tech.sina.com.cn/i/c/2001-07-28/77958.shtml

A contemporaneous August report criticized the product precisely because ADSL technology could support long-lived / always-on connections while the Beijing pricing model still imposed limited-hour packages.

Source:

- 《北京晨报》/新浪科技, 2001-08-06, 《北京ADSL定位不为普通网民 一问世便遭冷遇》: https://tech.sina.com.cn/i/c/2001-08-06/79011.shtml

This yields a useful phase distinction:

```text
PSTN dial-up:
voice/data contention + network-use time + telephone-call time

Early ADSL package:
voice/data decoupled + call-fee decoupled + usage-hour limits may remain

Later flatter broadband:
voice/data decoupled + increasingly persistent connection + weaker session clock
```

Therefore:

> **broadband transition != one event**.

Speed, line decoupling, call-charge decoupling, flat-rate billing, and always-on practice can move on different dates.

---

## 7. `account != user != household` is not a theoretical warning

A 2019 *Beijing Daily* archival retrospective cites its 1997 reporting that Beijing Internet accounts/users had passed 100,000 by year end and explicitly notes that one Internet account was often used by more than one person.

Source:

- 《北京日报》/人民网, 2019-10-17, 《1996年互联网初入北京城 嘶哑拨号声链接“新世界”》: https://media.people.com.cn/n1/2019/1017/c40606-31404334.html

Evidence grade: **C+** — later newsroom archival reconstruction with dated source pointers, not a verified 1997 Web capture.

This matters to Web archaeology because an authentication trace may represent:

```text
one ISP account
→ multiple family members
→ perhaps one computer
→ perhaps more than one user persona / email account
```

The following are not interchangeable:

```text
access account count
registered site-account count
browser profile
email address
human user
household
```

A historian should not infer one person per access credential unless the source contract says so.

---

## 8. New preservation failure mode: access-context loss

### 8.1 Definition

> **access-context loss** occurs when page/content artifacts survive but the practical conditions required to reach and consume them — tariff, access line, session state, dialing friction, client suppression/caching, and household resource conflict — are absent from the archive.

A Wayback capture might preserve:

```text
HTML
images
some CSS
some scripts
URL
capture time
```

while losing:

```text
the ISP card price
local-call tariff
night discount
busy signal / failed dial attempts
negotiated modem speed
line noise
whether the family needed the phone
whether images were disabled
whether Java was disabled
whether the user used cache
whether pages were batch-downloaded for offline reading
whether one credential represented several people
```

### 8.2 Why this changes interpretation

Suppose a 2001 page is 400 KB and contains 40 images.

A modern replay might render it in a fraction of a second.

The historical questions are instead:

- Did the user load images at all?
- At what negotiated rate?
- Did one missing subresource stall the page?
- Did the user disconnect and read locally?
- Did the phone need to be freed for another household member?
- Was the user paying an ISP clock, a phone clock, or both?

Without those variables, a visually accurate reconstruction can still be socially inaccurate.

---

## 9. Suggested extension to artifact reconstruction records

`docs/METHOD.md` should remain the canonical contract; this file does **not** modify it yet. For dial-up-era investigations, however, a supplemental access-context block is worth recording when evidence exists:

```yaml
access_context:
  access_type: dialup | isdn | adsl | lan | unknown
  dial_number: known | unknown
  isp: known | unknown
  advertised_speed: value | unknown
  negotiated_speed: value | unknown
  network_use_tariff: known | unknown
  telephone_tariff: known | unknown
  time_of_day_discount: known | unknown
  line_shared_with_voice: yes | no | unknown
  account_shared: yes | no | unknown
  client_suppression:
    images: on | off | unknown
    java: on | off | unknown
  cache_or_offline_reading: yes | no | unknown
```

Important:

> Unknown values should stay `unknown`; the goal is to expose missing context, not invent a period-perfect simulation.

---

## 10. Historical user-experience reconstruction needs a different evidence bundle from interface reconstruction

For a dial-up-era Web object, there are at least three separate reconstruction targets:

### Target A — server/page artifact

- URL
- capture datetime
- HTML / headers
- charset
- frames / scripts / subresources

### Target B — access contract

- access provider / number
- account/card arrangement
- tariff
- telephone charge
- nominal/actual speed
- session limits

### Target C — ordinary use practice

- household vs workplace vs campus vs net café
- shared line or dedicated line
- shared account or individual account
- time-of-day choices
- cache/offline strategy
- family conflict or coordination

A strong historical claim should state which target has actually been reconstructed.

A capture satisfying Target A must not silently inherit Targets B and C.

---

## 11. Overseas comparison: the resource conflict is infrastructural, not uniquely Chinese

A 1998 *Washington Post* household column describes teenagers using the home computer for online chat until the household telephone became difficult to access; the parent eventually installed a second line, only to discover that a teenager could use one line for voice while using the other for online chat.

Source:

- Howard Kurtz, *The Washington Post*, 1998-07-12, “A Clique on the Line”: https://www.washingtonpost.com/archive/lifestyle/1998/07/12/a-clique-on-the-line/b17cfdb2-bcd9-4452-8b09-188694d9069c/

Evidence grade: **B**, one contemporaneous household.

NTIA's 2001 U.S. data reported that 80.0% of individuals who used the Internet at home connected via regular dial-up telephone line, versus 12.9% cable and 6.6% DSL.

Source:

- U.S. Department of Commerce, NTIA, *A Nation Online*, Chapter 4: https://www.ntia.gov/sites/default/files/data/dn/html/Chapter4.htm

Evidence grade: **A**.

So:

> `telephone line as scarce household Internet infrastructure` is not China-specific.

What may differ are the tariffs, household income, second-line affordability, local loop capacity, housing wiring, and availability of cable/DSL/other alternatives.

OWA should keep the overseas material only as a methodological comparator; global dial-up history remains outside this repository's core scope.

---

## 12. What this changes for old-Web page design interpretation

### 12.1 Lightweight pages were not merely aesthetic

When bytes map to wait time and wait time maps to money, design weight has a direct ordinary-life consequence.

This does **not** mean every small GIF or table layout was intentionally optimized for poor users. It means page weight must be interpreted inside the access environment.

### 12.2 “Broken” may have been local/session-specific

A user reporting that a page “打不开” could mean:

- server failure;
- DNS failure;
- ISP issue;
- failed modem session;
- line noise;
- timeout on a large subresource;
- Java/browser incompatibility;
- deliberate blocking of images/scripts;
- user disconnected to stop the meter.

Therefore historical usability evidence needs failure classification whenever possible.

### 12.3 Offline Web tools were part of Web use

Using WebZIP or browser Cache means that a Web page can be socially consumed **after the Internet session has ended**.

Thus:

```text
page reading time
!= connection time
```

and:

```text
online activity history
!= time spent with Web-derived information
```

This matters to any attempt to estimate “how long people were online” from access logs.

---

## 13. M1 / artifact status in this slice

This run did **not** obtain a verified historical capture satisfying the repository's M1 minimum contract for an early ChinaNet 163 enrollment page, Beijing `www.169.com` ADSL information page, or a representative dial-up ISP help page.

Specifically, this slice does not have a verified pair of historical captures with checked:

- capture datetime;
- historical main-resource response;
- charset / declared encoding;
- DOM / frame structure;
- script and image dependencies;
- second historical time point.

Therefore:

> **M1 historical access-interface capture: NOT ACHIEVED IN THIS SLICE.**

This means only that this run did not obtain and verify the artifact. It does **not** mean Internet Archive or another archive never captured the pages.

The evidence here is instead strong enough for an **access-architecture** and **preservation-loss** note because it relies on contemporaneous tariff documents, service reporting, user commentary, and technical advice.

---

## 14. High-value artifact targets for a later run

Do not create more conceptual notes before trying these:

1. 1997–1999 ChinaNet 163 access-card / onboarding instructions;
2. period ISP help pages giving dial number, modem settings and charge rules;
3. 2001 `www.169.com` ADSL service information referenced in contemporaneous Beijing reporting;
4. screenshots/manuals of “北京宽带通” or other access software;
5. period browser/ISP documentation showing image suppression, proxy/cache or offline-reading practices;
6. historical forum/BBS posts describing line contention and household phone negotiation.

The best next artifact would let us connect:

```text
verified page
+
verified access contract
+
ordinary-life use evidence
```

rather than adding another domain analogy.

---

## 15. Hindsight risks

### Risk 1 — assuming “1994 Internet connection” means household Internet

Do not conflate national network connectivity with ordinary household access.

### Risk 2 — assuming broadband immediately meant unlimited always-on

Early ADSL could decouple voice/data while retaining hour-limited pricing.

### Risk 3 — assuming one access account means one person

Period evidence explicitly warns that accounts could be shared.

### Risk 4 — replaying a page instantly and calling that the historical experience

The archive may preserve bytes while deleting the historical meter.

### Risk 5 — romanticizing dial-up scarcity

Slow, expensive access was not charming to the 1999 user paying the bill. Nostalgic modem sound should not replace evidence about exclusion, waiting and household cost.

---

## 16. The narrow synthesis

The central old-Web correction from this slice is:

```text
historical Web page
!= historical Web encounter
```

because the encounter may have required:

```text
a billable phone session
+ a billable ISP session
+ a free household line
+ a shared computer/account
+ deliberate suppression/caching/offline tactics
```

A later broadband transition then changed not only page speed but the **resource topology of access**.

For Chinese old-Web archaeology, this means a page can be perfectly archived and still be historically incomplete in one of the most important ways:

> **the archive may save what the user saw, while erasing what it cost the household to keep the page on screen long enough to see it.**
