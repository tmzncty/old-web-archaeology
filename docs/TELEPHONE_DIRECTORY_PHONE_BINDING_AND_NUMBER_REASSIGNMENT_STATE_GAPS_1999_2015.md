# Telephone directories, phone-number binding, and number-reassignment state gaps, 1999–2015

## Scope

This note models a specific Chinese old-web boundary:

> **What does a telephone number on a historical webpage actually prove?**

The main research object remains the Chinese Web, approximately 1995–2015.

This is not a general global telephone history. Pre-Web telephone directories and post-2015 number-reassignment evidence appear only when they are necessary to interpret Chinese historical web artifacts.

Cross-repository companion note:

- `tmzncty/how-people-lived/topics/telephone-household-reachability-number-identity-and-contact-state-china-1980-2026.zh-CN.md`

Central archaeological warning:

> **A phone number in a capture is a time-bounded contact field, not a permanent person identifier. A directory hit is not proof that the number was current, a successful bind is not proof of enduring identity, and a number that works today may belong to someone unrelated to the historical page.**

This topic has a strong privacy stop condition: do not call old personal numbers simply to identify their present holder.

---

## 1. Why phone-number state needs its own model

Historical Chinese pages often contain phone numbers in:

- personal homepages;
- company contact pages;
- forum signatures;
- classified advertisements;
- rental/job listings;
- dating profiles;
- school pages;
- service directories;
- online Yellow Pages / 114;
- account-security and mobile-binding help pages.

A web archive makes these fields look unusually precise: a number is a string of digits, often next to a name and address.

But that precision is deceptive.

The historical relationship may be:

```text
page subject
→ contact number displayed
→ number assigned to a line/subscriber at that datetime
→ caller dials
→ network routes call
→ someone answers
→ caller reaches intended person/organization
```

Every arrow can fail.

Later, when phone numbers became internet-account keys, a second state chain appeared:

```text
internet account
→ phone submitted
→ SMS/telecom possession test
→ platform binding stored
→ number later canceled
→ carrier eventually reassigns number
→ historical platform binding may remain
→ new subscriber receives old platform state
```

A public web capture can preserve only fragments of these chains.

---

## 2. Minimum object decomposition

Do not merge the following objects.

### 2.1 Telephone number string

Example shape only:

```text
010-xxxxxxxx
13xxxxxxxxx
```

The digits are not a person.

### 2.2 Numbering-plan state

The rules that make a number valid at a historical datetime:

- local number length;
- area code;
- mobile prefix;
- special-service number;
- number-upgrade mapping.

### 2.3 Telecom subscriber / line assignment

The carrier-side assignment of a number to a line/SIM/account.

Usually not public-web evidence.

### 2.4 Physical endpoint

A fixed line, public telephone, mobile handset/SIM, office PBX, household telephone or other endpoint.

### 2.5 Directory record

A searchable database record maintained by 114, Yellow Pages or another directory service.

It can be stale even if the number itself is valid.

### 2.6 Directory query result

A dynamically generated response for a query at a particular time.

This is not the same object as the underlying subscriber record.

### 2.7 Historical web contact field

A number displayed on a page.

It can remain online after the organization moves, a listing expires or the number changes.

### 2.8 Internet-platform account

QQ, email, forum, dating, e-commerce or another account.

### 2.9 Phone-binding edge

A platform-database relationship such as:

```text
account A ↔ phone number N
```

This edge has its own creation, update and deletion lifecycle.

### 2.10 SMS verification event

Evidence that a verification message/code was sent and/or received at one moment.

It does not prove permanent ownership or every identity claim attached to the account.

### 2.11 Current number holder

The present-day subscriber.

Never infer that this person is the historical page subject.

### 2.12 Capture

One archived representation at one datetime.

The capture freezes a field; it does not freeze the telecom network or subscriber database.

---

## 3. Core state models

### 3.1 Directory lookup chain

```text
114 / directory service exists
→ web front end exists
→ query interface loads
→ user submits name/category/number
→ backend accepts query
→ directory database contains a matching record
→ result is returned
→ displayed number is current for that record
→ telecom network still routes that number
→ intended organization/person answers
```

Do not infer the last steps from an archived search form.

### 3.2 Historical contact-page chain

```text
page published
→ phone field entered
→ page remains reachable
→ phone assignment remains unchanged
→ organization/person remains at same place
→ caller dials
→ intended subject answers
```

A page can survive for years after the number becomes wrong.

### 3.3 Internet phone-binding chain

```text
account logged in
→ user submits phone number
→ platform accepts format
→ verification / SMS condition satisfied if required
→ binding record created
→ account-security state changes
→ number remains assigned to same person
→ binding remains maintained
```

Historical documentation may prove only that the feature or endpoint existed.

### 3.4 Reassignment chain

```text
old holder stops using number
→ carrier cancels assignment
→ cooling/freeze period
→ number returned to pool
→ new holder receives number
```

This telecom chain is separate from:

```text
old internet account
→ old binding remains / is removed / is stale
```

That separation is the source of later “secondary-number” problems.

---

## 4. 1999 Beijing online 114: a telephone database became a web search system

A Beijing Morning Post report dated 1999-09-15 said Beijing 114's online self-service query had begun trial operation at:

- `http://www.114china.com`

The contemporaneous report described functions including:

- query by unit name;
- query by initial/pinyin clue or industry category;
- reverse lookup from number to organization;
- area-code lookup;
- old-number / old-name to new-number / new-name lookup;
- common-service-number lookup.

Source:

- https://news.sina.com.cn/society/1999-9-15/14567.html

Evidence grade: **B — contemporaneous media report describing a live service.**

A second report dated 1999-12-27 said the service held more than 200,000 web-visible information records and could search by product/business category even when a user did not know the exact unit name.

Source:

- https://tech.sina.com.cn/news/internet/1999-12-27/14203.shtml

Evidence grade: **B — independent-ish contemporaneous media report from the same local-news environment; useful for function claims, not a substitute for an actual capture.**

### What this proves

- by late 1999, Beijing 114 directory data had a public Web query layer;
- search could be field/category driven, not just exact telephone-number lookup;
- reverse lookup existed for eligible organizational records;
- the Web interface extended a pre-existing telephone information service rather than creating the directory from scratch.

### What it does not prove

- exact HTML/DOM;
- charset;
- form method;
- CGI/ASP endpoint;
- query parameter names;
- ranking/order;
- latency;
- browser requirements;
- whether a particular historical result was returned on a particular day.

This run did **not** obtain and verify an archive capture of `114china.com` from 1999–2001.

Per `docs/METHOD.md`, a search-engine locator or remembered URL is not a verified capture.

---

## 5. Privacy was already built into the online-directory boundary

The 1999 reports explicitly say the online 114 system largely excluded private residential telephone numbers for privacy reasons.

That means a future reconstruction must not treat the service as:

```text
complete copy of all 114 data
```

The likely architecture had at least a policy/filter boundary between:

```text
telecom / directory records
and
web-publishable records
```

The exact implementation remains unknown.

A contemporaneous 2000 report on Jinan said private-home 114 lookup was being stopped after a survey in which more than two-thirds of respondents reportedly did not want residential phone numbers publicly queryable; the report also noted similar restrictions in other cities.

Evidence grade: **B — contemporaneous media; should be used as policy/social evidence, not as a nationwide uniform rule.**

Archaeological consequence:

> **Failure to find a residential number in an online directory is not evidence that the household lacked a telephone. It may be a publication/privacy state.**

---

## 6. Directory completeness gap after telecom restructuring

In 2003, Xinhua reported a practical failure in 114 lookup after telecom restructuring: a reporter using one operator's 114 service could not directly obtain information for a China Tietong office and had to route through other agencies.

Source:

- contemporaneous Xinhua report (archived media copies; record exact stable URL when adding a case fixture).

Evidence grade: **B — contemporaneous operational observation.**

This creates a key state distinction:

```text
telephone number exists
≠ local 114 database contains it
≠ this operator's 114 can query it
≠ web-114 contains it
```

Recommended fields:

```yaml
directory_operator:
record_operator:
query_scope:
cross_operator_supported:
database_sync_claimed:
observed_lookup_result:
lookup_datetime:
```

Never describe “114” as one timeless national database unless the evidence supports that exact scope.

---

## 7. Number-version gap: a historically correct phone number can become invalid without the page changing

Nanjing changed fixed telephone numbers from seven to eight digits on 2003-12-06.

Contemporaneous sources:

- Yangtze Evening News, 2003-08-27: https://news.sina.com.cn/c/2003-08-27/1222645241s.shtml
- Xinhua / Xinhua Daily, 2003-12-05: https://news.sina.com.cn/c/2003-12-05/13491267145s.shtml

Evidence grade: **B — contemporaneous telecom/public guidance.**

Users were told to update:

- phonebooks stored in handsets;
- business cards;
- envelopes;
- hotline / abbreviated-dial settings;
- voicemail / call-forwarding settings;
- relatives and clients.

A separate contemporaneous report described companies reprinting packaging, signs, business cards and Yellow Pages entries.

Source:

- Yangtze Evening News, 2003-11-23: https://news.sina.com.cn/s/2003-11-23/11521171682s.shtml

This gives old-web archaeology a concrete **number-version gap**:

```text
page capture date
≠ date contact number was last updated
≠ numbering-plan version implied by number string
```

A 2004 capture may still contain a 2003 pre-upgrade number.

Recommended fields:

```yaml
phone_string_as_displayed:
numbering_plan_date:
known_upgrade_event:
expected_transformation:
page_last_modified_known:
contact_field_last_verified:
```

Do not silently “correct” historical phone strings in a reconstruction. Preserve the original field and annotate the historical mapping separately.

---

## 8. Web directory survival can outlast directory semantics

Telephone directories are especially vulnerable to a false precision problem.

An archived result such as:

```text
Company X
Address Y
Phone Z
```

may appear stronger than an ordinary prose statement because it is structured.

But at capture time any of the following may already have been stale:

- company name;
- company address;
- department;
- phone number;
- business category;
- operating status.

Therefore:

```text
structured field
≠ verified current field
```

If possible, cross-check with:

- a same-period official site;
- newspaper advertisement;
- company registration/official filing where appropriate;
- another independent directory;
- later number-upgrade mapping.

Do **not** use a present-day call to a personal number as the preferred verification method.

---

## 9. 2004: Yellow Pages were already multi-channel, not just a paper book

A contemporaneous 2004 report described China Telecom packaging paper Yellow Pages with an online “Star Yellow Pages” site, allowing advertisers to obtain broader exposure across regions.

Source:

- 2004-09-06：https://tech.sina.com.cn/it/t/2004-09-06/0841419126.shtml

Evidence grade: **B — contemporaneous industry/media report.**

This matters because old-web contact discovery did not follow a simple sequence:

```text
paper directory → web search replaces paper
```

Instead, the same organizational/contact database could appear through:

- paper Yellow Pages;
- human 114 operator;
- Web 114;
- SMS/“number information” services;
- company websites;
- search engines.

Treat them as separate delivery layers that may have different update cycles.

---

## 10. 2006–2008: phone numbers became account-binding objects

A Baidu Zhidao question dated 2006-03-16 asks what it means to bind a mobile phone and QQ number. Replies describe mobile/QQ integration and privacy-related behavior.

Source:

- https://zhidao.baidu.com/question/4953794

Evidence grade: **B — contemporaneous user question/answers.**

It proves users were encountering “phone ↔ QQ” binding as a real concept by 2006.

It does **not** define Tencent's authoritative security contract.

A 2008-era tutorial describes multiple binding paths, including SMS commands and a binding URL:

- `http://bd.qq.com/`

It also refers to QQ2007 Beta2 client menu paths for mobile binding.

Source:

- https://www.syue.com/edu/Tools/Chat/QQ/15377.html

Evidence grade: **B — contemporaneous/near-contemporaneous user tutorial.**

### Archive gap

This run did **not** verify a 2006–2008 archive capture of `bd.qq.com`.

Therefore unknown:

- page title;
- charset;
- form fields;
- whether password was posted in the clear or transformed client-side;
- SMS-code state;
- exact endpoint;
- cookies/session assumptions;
- browser-specific JS;
- successful/failed response wording.

A later tutorial must not be used to reconstruct those details.

---

## 11. Phone-binding object decomposition

When a historical platform says “绑定手机”, model at least:

### 11.1 Account identity

Which platform account is being modified?

### 11.2 Submitted number

What number string did the user enter or send from?

### 11.3 Telecom control evidence

Possible mechanisms:

- SMS sent from that number;
- SMS code received at that number;
- premium-SMS billing relationship;
- carrier-side service subscription;
- manual account/password entry.

Do not assume one mechanism from another era.

### 11.4 Binding state

Possible states:

```text
unbound
pending
bound
changed
suspended
removed
stale
```

### 11.5 Platform privilege

Binding may enable only some features:

- mobile messaging;
- password recovery;
- account protection;
- paid service;
- hidden-number behavior;
- later login/verification.

Do not rewrite all historical phone binding as “modern 2FA.”

### 11.6 Holder/subject identity

Even if the number was controlled by the user at the time, that does not prove every account profile field referred to the telecom subscriber's legal identity.

---

## 12. Core binding gaps

### 12.1 submitted-number / controlled-number gap

```text
number entered
≠ number under user control
```

unless the platform verifies it.

### 12.2 controlled-number / subscriber-identity gap

```text
SMS received
≠ legal subscriber identity independently established by the platform
```

unless additional evidence exists.

### 12.3 binding-created / binding-maintained gap

A successful historical binding can later become stale.

### 12.4 number-valid / account-valid gap

The phone number can still route while the internet account is deleted, or vice versa.

### 12.5 one-number / one-person gap

A number may be:

- family shared;
- employer-issued;
- temporarily borrowed;
- reassigned;
- associated with more than one platform account under historical rules.

### 12.6 binding / login gap

Some historical services used phone binding for mobile messaging or paid services without allowing the phone number to replace the platform username.

Do not impose today's login semantics on 2006.

---

## 13. Later boundary evidence: number reassignment makes historical phone fields dangerous

This section is outside the repository's core 1995–2015 period. It is included only to define a **stop condition for interpreting old captures**.

A 2024 investigation documented users receiving reissued mobile numbers that were still connected to the previous holder's platform state. One new user logged into a ride-hailing service and saw a 2019 Shanghai unpaid order despite never having lived there.

Source:

- New Beijing News / China News mirror, 2024-04-02: https://www.chinanews.com.cn/cj/2024/04-02/10191825.shtml

Evidence grade: **B — later contemporaneous reporting on current reassignment cases.**

By 2025–2026, Chinese telecom regulators and platforms were explicitly building a cross-industry “secondary-number refresh” mechanism to remove historical internet-account bindings from reissued numbers.

The MIIT 2026 Q2 service-quality notice, published 2026-08-13, reports:

- 258 supported common internet applications;
- more than 14.35 million users served;
- more than 850 million application-unbinding requests.

Source:

- https://wap.miit.gov.cn/zwgk/zcwj/wjfb/tg/art/2026/art_440c2ded2ba54f0387b4cca50acf8147.html

Evidence grade: **A — official later boundary evidence.**

Archaeological implication:

> **Do not call a phone number found in a 2003 personal homepage and treat the present answer as identity confirmation. The number may have been reassigned multiple times.**

This is now a hard privacy/method rule.

---

## 14. Number-reassignment state gap

Model separately:

```text
historical subscriber A has number N
→ historical webpage displays N
→ A stops service
→ carrier deassigns N
→ N enters holding period
→ carrier assigns N to subscriber B
```

and:

```text
historical platform account A
→ binding to N
→ binding removed / not removed / unknown
```

These chains can diverge.

Suggested evidence object:

```yaml
phone_number_redacted: true
historical_display_format:
historical_capture_datetime:
historical_page_subject:
numbering_plan_valid_at_capture:
telecom_assignment_known: false
platform_binding_known:
current_holder_checked: false
reassignment_possible: true
privacy_action: do_not_contact
```

Default for ordinary personal pages should be `do_not_contact`.

---

## 15. Directory-state gaps

### 15.1 database inclusion gap

```text
subscriber exists
≠ directory record exists
```

### 15.2 web-publication gap

```text
directory record exists
≠ record published to Web 114
```

Residential privacy policy can produce this gap.

### 15.3 freshness gap

```text
record displayed
≠ record current
```

### 15.4 carrier-fragmentation gap

```text
number exists in carrier B
≠ carrier A's directory can resolve it
```

### 15.5 reverse-lookup gap

A service may allow reverse lookup only for organizations, not private subscribers.

### 15.6 category-index gap

A unit can exist but be classified under an unexpected industry/category and therefore not appear for a user's search.

### 15.7 query-result / call-outcome gap

```text
result returned
≠ call connects
≠ intended subject answers
```

---

## 16. Historical phone fields and page staleness

Old-web researchers should distinguish at least four clocks:

1. `capture_datetime` — when the archive stored the page;
2. `page_publish/update_datetime` — when the page content was changed;
3. `phone_assignment_datetime` — when the telecom number assignment was valid;
4. `numbering-plan_datetime` — which digit/area-code rules applied.

A page can be captured in 2005 while containing a contact block last updated in 2001.

Recommended statement:

> “The 2005 capture displays the number string X; current assignment at the capture datetime has not been independently verified.”

Avoid:

> “In 2005, this was definitely the subject's working phone.”

unless independent evidence supports it.

---

## 17. Contact-field survival can create false identity continuity

A special old-web bias appears when:

- a homepage survives;
- the displayed name survives;
- the phone string survives;
- the same digits are still routable today.

This visual continuity tempts a researcher to assume one continuous identity.

But the correct model is:

```text
historical page identity
≠ historical telecom subscriber (unless verified)
≠ present telecom subscriber
```

Call this **contact-field continuity bias**.

It is analogous to domain reuse:

> a domain string can survive while ownership changes; a phone-number string can also survive while the person changes.

---

## 18. Privacy rule for ordinary-person archaeology

Phone numbers are unusually risky because an archived field can still reach a real person.

For ordinary personal pages:

- redact full mobile numbers in repository prose unless the exact digits are necessary to the technical claim;
- do not mass-test whether archived numbers still connect;
- do not reverse-search current identity to “complete” a historical profile;
- do not expose a present subscriber merely because they inherited an old number;
- record numbering pattern/prefix only when sufficient;
- prefer organizational/public-service numbers for protocol/interface experiments.

If a historical personal number is necessary to prove a URL/form/capture structure, keep it in restricted evidence notes or hash/redact it.

This extends `docs/METHOD.md` privacy minimum.

---

## 19. Evidence table

| Claim | Source family | Grade | Supports | Does not support |
|---|---|---:|---|---|
| Beijing online 114 trial existed by 1999-09 | contemporaneous Beijing Morning Post/Sina preservation | B | service/URL/function existence | exact historical DOM/backend |
| online 114 largely excluded private-home numbers | contemporaneous 1999 reports | B | web-publication privacy boundary | exact database filtering implementation |
| number upgrades required users to update stored contacts/materials | 2003 Nanjing telecom/media | B | contact-maintenance labor | every site's update timing |
| Yellow Pages had a Web companion by 2004 | contemporaneous industry report | B | multi-channel directory layer | exact site behavior/capture |
| phone↔QQ binding was a user-visible concept by 2006 | contemporaneous Baidu user question | B | user-facing concept | authoritative Tencent security contract |
| `bd.qq.com` was cited as a binding route in 2008-era tutorials | user tutorial | B | historical locator/function lead | verified capture/DOM |
| reissued numbers can retain old app relationships | 2024 investigation | B, later boundary | reassignment risk | prevalence in 2000s |
| cross-platform unbinding exists at large scale by 2026 | MIIT | A, later boundary | present lifecycle mismatch | exact history of each old platform |

---

## 20. Known / probable / unknown

### Known

- by 1999, a public Beijing Web interface existed over 114-style directory data;
- private residential numbers were already treated differently from organizational directory records;
- numbering changes could invalidate contact fields without changing the page;
- 2000s Chinese Internet services were already binding phone numbers to online accounts;
- current number reassignment proves that phone strings cannot be treated as permanent identity keys.

### Probable

- many old-web contact pages became stale before disappearing;
- online directories, telephone operator databases and paper directories had different refresh cycles;
- phone-binding endpoints created hidden platform state that ordinary archive captures rarely preserve.

### Unknown

- a verified 1999–2001 `114china.com` capture and its exact technical stack;
- a verified 2006–2008 `bd.qq.com` binding capture;
- exact retention/cleanup rules for early platform phone bindings;
- how often old personal pages today point to reassigned numbers;
- whether specific surviving 114 query results reflected real-time, daily or slower directory synchronization.

---

## 21. Next bounded archaeology target

The next valuable step is **not** to scrape thousands of historical phone numbers.

Find one privacy-safe, preferably organizational, verified capture from 1999–2005 of:

- `114china.com` / `114china.net`; or
- a telecom Yellow Pages search page; or
- an early phone-binding help/entry page.

Record:

```yaml
original_url:
archive_source:
capture_url:
capture_datetime:
http_status:
charset:
page_title:
form_method:
form_action:
query_fields:
reverse_lookup_option:
industry/category_fields:
phone_display_format:
residential_privacy_text:
js_dependencies:
missing_assets:
backend_endpoint_alive_in_capture:
result_page_captured:
```

Then test one **historical organizational/public-service record**, not an ordinary person's current number, to understand the interface state safely.

The central question for this repository is now:

> **When a web archive preserves a telephone number perfectly, how much of the historical communication path has actually survived?**
