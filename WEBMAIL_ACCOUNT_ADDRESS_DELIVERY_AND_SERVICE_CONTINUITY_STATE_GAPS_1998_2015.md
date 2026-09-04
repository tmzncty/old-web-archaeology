# WEBMAIL_ACCOUNT_ADDRESS_DELIVERY_AND_SERVICE_CONTINUITY_STATE_GAPS_1998_2015

Status: research note / state-gap model  
Scope: approximately 1998–2015 Chinese public-Web evidence around free Webmail, registration/login, message delivery, quota/inactivity, provider transitions, notification integration and the preservation limits of private inboxes  
Companion life-history note: `tmzncty/how-people-lived/topics/electronic-mail-portable-address-webmail-formal-inbox-and-institutional-reachability-china-1986-2026.zh-CN.md`

## 0. Why Webmail belongs in old-web archaeology

A Webmail login page is one of the most deceptive historical Web artifacts.

It can survive looking almost complete:

- logo;
- username box;
- password box;
- “注册免费邮箱”；
- “登录”；
- “收件箱”；
- “发送成功”；
- quota text;
- help links;
- brand/domain.

Yet nearly everything that mattered to an actual user may have lived somewhere the public archive did not and should not capture:

- account database;
- password verifier;
- session state;
- private inbox;
- SMTP/MTA queue;
- recipient-server reply;
- spam filtering;
- attachment store;
- quota state;
- read/unread flags;
- deletion state;
- account-recovery state;
- ownership/migration mapping after a provider sale.

The master warning is:

> **Webmail page state ≠ account state ≠ delivery state ≠ inbox state ≠ human reading ≠ real-world response.**

This note stays within the Chinese-old-Web scope. Pre-1998/global email history belongs primarily in the companion `how-people-lived` note; Hotmail appears here only as a bounded comparative precedent for Webmail portability.

---

## 1. Research units

Per `docs/METHOD.md`, keep these units separate:

- mail-service brand;
- domain / host;
- one login host;
- one public marketing/help page;
- one registration page;
- one account;
- one email address string;
- one authenticated Webmail session;
- one mailbox;
- one folder;
- one message;
- one attachment;
- one compose form;
- one send transaction;
- frontend Web application;
- outbound mail transfer agent (MTA);
- DNS/MX state;
- remote MTA;
- spam/virus/filter layer;
- quota/storage state;
- notification layer (for example QQ reminder);
- provider/company ownership;
- archive capture;
- researcher claim.

These objects can share a brand without sharing a lifecycle.

---

## 2. Evidence grades used in this note

### A / A-

- contemporaneous service/provider announcements where provenance is known;
- original contemporary institutional pages;
- verified historical archive captures, if/when actually inspected.

### B / B+

- near-contemporaneous newspaper/technology reporting;
- contemporary user tutorials/discussions for observable operation or experience;
- current corporate archive preserving a dated historical statement, if original capture is not verified.

### C

- later recollection or nostalgia.

### D

- state machines, gap taxonomy and reconstruction hypotheses below.

This run does **not** claim to have verified an actual 1998–2001 Wayback/WARC capture of `163.net` or early `163.com` Webmail.

Therefore historical DOM, charset, exact form endpoints and browser behavior remain unknown unless separately supported.

---

## 3. Strong 1999 anchor: `163.net` free mail existed at scale, but scale did not mean permanence

A 1999-12-24 *Southern Weekend* report reproduced by Sina described `163.net` as a major free-email provider. It reported:

- 1.5 million registered users by 1999-10-07;
- more than 1 million registered users by 1999-06-14;
- repeated capacity expansion after 1998;
- account cleanup under which mailboxes with no mail traffic for three months were reclaimed;
- a Web-interface change after expansion;
- mailbox capacity increasing from 2 MB to 5 MB;
- a sale/provider-ownership transition at the end of 1999.

Source / B+ near-contemporaneous report:
- https://tech.sina.com.cn/news/internet/1999-12-24/14105.shtml

### Narrow claims

The source can support that:

1. a public free Webmail service under `163.net` was in operation;
2. provider-side capacity and quota policy changed over time;
3. inactivity could trigger address/mailbox reclamation;
4. corporate ownership could change while the public service brand remained visible.

### Do not infer

It does not prove:

- each registered account represented one human;
- a particular account remained active;
- all old accounts migrated intact through the sale;
- the exact private-mail storage implementation;
- the exact historical login URL/form action;
- a specific message survived or was delivered;
- a 1999 public homepage capture preserves private inbox state.

---

## 4. The first major gap: service branding is not account continuity

### 4.1 Near-name continuity trap

A common later-history error is to treat:

```text
163.net
=
163.com
```

because both are remembered as “163 邮箱/电子邮局”.

But a 2001-10-31 contemporaneous report states that NetEase had launched its own free mailbox using the `163.com` portal domain in October 2000, and expanded it to 25 MB in October 2001.

Source / B:
- https://tech.sina.com.cn/i/c/2001-10-31/90065.shtml

The historical rule must be:

> **similar brand string ≠ same domain ≠ same operator ≠ same account database ≠ same address continuity.**

### 4.2 Suggested evidence fields

For every mail service/timepoint, record separately:

```yaml
brand_name:
address_domain:
web_host:
operator:
owner:
login_host:
registration_host:
mail_backend_identity: unknown | evidenced
account_migration_claim: unknown | claimed | verified
capture_datetime:
```

### 4.3 Why this matters for ordinary-history claims

Suppose a 2000 personal homepage lists:

```text
someone@163.net
```

A later researcher must not silently “correct” that to:

```text
someone@163.com
```

Nor can a currently live `mail.163.com` page be used as evidence that the historical `163.net` address still exists.

The address string is a time-specific artifact.

---

## 5. Account lifecycle must be reconstructed as a state machine

A Webmail address can move through many states:

```text
registration page exists
→ registration request submitted
→ username available
→ account created
→ address routable
→ account activated
→ user authenticates
→ mailbox usable
→ account remains active
→ policy changes
→ dormant/inactive
→ reclaimed/disabled
→ address potentially reassigned or retired
```

### 5.1 `registration-page / account-created gap`

A saved registration form only proves that registration was presented.

It does not prove:

- backend accepted the username;
- CAPTCHA/validation passed;
- account creation transaction committed;
- welcome mail was stored;
- user ever returned.

### 5.2 `address-string / live-account gap`

A historical webpage can preserve an address long after its account died.

So:

```text
address appears in 2002 page capture
≠
address was still valid at capture time
≠
address is valid today
```

### 5.3 `inactive-policy gap`

The 1999 `163.net` report gives explicit evidence that inactivity mattered.

A researcher must distinguish:

```text
account registered
account active
mail traffic present
last login
last mail traffic
policy-defined inactive
account reclaimed
```

These clocks are not interchangeable.

### 5.4 `reassignment gap`

Unless a provider’s historical policy is documented, do not assume reclaimed usernames were:

- permanently retired;
- immediately reassignable;
- later restored to the same person.

This is particularly important for identity work: a historical address string cannot automatically be treated as a permanent person identifier.

---

## 6. Message delivery requires a much longer chain than “发送成功”

A useful minimal delivery state machine is:

```text
compose UI loads
→ recipient syntax accepted
→ send form submitted
→ Web frontend accepts request
→ message object generated
→ outbound MTA accepts
→ DNS/MX lookup succeeds
→ remote MTA reachable
→ remote MTA accepts/rejects/defers
→ spam/filter/virus policy runs
→ quota/storage permits delivery
→ message stored in recipient mailbox
→ recipient account still accessible
→ recipient logs in / receives notification
→ inbox listing displays message
→ recipient opens message
→ attachment/content renders
→ recipient acts/replies
```

### 6.1 `web-success / MTA-acceptance gap`

A historical `发送成功` page or screenshot may prove only that the Web application entered a success branch.

It does not by itself prove the outbound MTA accepted the mail.

### 6.2 `MTA-acceptance / remote-delivery gap`

Even if the local system queued a message:

- DNS may fail;
- MX may be unreachable;
- remote server may defer;
- recipient quota may be full;
- spam policy may reject/quarantine.

### 6.3 `stored / noticed gap`

A mail can be successfully stored without being noticed.

This distinction becomes particularly important in the companion life-history note: later job seekers actively poll the inbox because **delivery is not the same as attention**.

### 6.4 `noticed / outcome gap`

A person may read a message and still not:

- reply;
- submit required material;
- attend the interview;
- accept the job;
- continue the relationship.

Old-Web evidence should stop at the narrowest supported state.

---

## 7. Quota and storage: mailbox size is historical state, not a timeless product attribute

The 1999 `163.net` report describes a move from 2 MB to 5 MB. The 2001 NetEase report describes `@163.com` expansion to 25 MB.

These values must be attached to exact service/timepoints.

### 7.1 `quota-version gap`

Do not write:

> “163 邮箱容量是 25MB。”

Prefer:

> “A 2001-10-31 report said NetEase’s `@163.com` free mailbox was being expanded to 25 MB.”

because:

```text
service name
+ date
+ account tier
+ rollout state
```

all matter.

### 7.2 `quota / stored-content gap`

Quota shows a maximum policy state, not actual contents.

A 5 MB account could hold:

- almost nothing;
- thousands of tiny text messages;
- a few large attachments.

### 7.3 `message-survival gap`

A message could disappear because of:

- user deletion;
- empty-trash policy;
- account reclamation;
- corruption/migration;
- provider closure;
- quota cleanup;
- local-only download followed by server deletion.

A public archive normally cannot tell which happened.

---

## 8. Provider sale, rebranding and service migration create continuity illusions

`163.net` is useful because the public brand continued across an ownership transition.

Later 2001 reporting described `163.net` being folded into Tom.com’s mail/channel strategy and changing free-registration/fee policy.

Near-contemporary sources:
- https://tech.sina.com.cn/i/c/73314.shtml
- https://tech.sina.com.cn/i/c/74470.shtml

### 8.1 `brand-survival / backend-survival gap`

A page can preserve the same logo/name while:

- owner changes;
- server cluster changes;
- account database migrates;
- password system changes;
- quota changes;
- registration closes;
- free/paid tier changes.

### 8.2 `corporate-sale / personal-account gap`

A report that “service sale did not affect users” is a provider/media claim unless account-level evidence is available.

Do not upgrade it to:

> “Every historical mailbox migrated without loss.”

### 8.3 Archaeological consequence

For a service transition, build a table like:

| Date | public brand | address domain | operator/owner | registration | quota | known backend | archive evidence |
|---|---|---|---|---|---|---|---|

Do not compress the table into a single “founded/closed” date.

---

## 9. Authentication: the public login shell is not the private Webmail application

Historical Web archives often preserve the most public part of Webmail:

```text
login page
logo
help
marketing text
```

The inbox requires:

- valid account;
- password state;
- cookies/session;
- possibly JavaScript/frame navigation;
- private backend requests;
- personalized mailbox state.

### 9.1 `login-page / authenticated-session gap`

A replayable login page does not prove a historical login can be executed now.

### 9.2 `credential-form / auth-backend gap`

Even if username/password controls survive:

- form endpoint may be dead;
- archive rewrite may alter action URL;
- server may require hidden tokens;
- cookie domain may no longer exist;
- HTTPS/TLS assumptions may differ;
- auth database is private and gone.

### 9.3 `session / inbox gap`

A session token existing in an old client artifact would not justify attempting to access or republish private historical messages.

Privacy stop condition applies.

---

## 10. Browser/encoding state: do not infer the 1998 UI from a later screenshot

Early Chinese Webmail likely encountered historically specific combinations of:

- GB2312 / GBK;
- frames;
- tables;
- old JavaScript;
- IE/Netscape differences;
- dial-up latency;
- image-based buttons;
- cookies;
- multipart/form uploads.

But “likely” is not evidence.

### Current negative result

This research pass did **not** obtain and actually verify a 1998–2001 `163.net` / early `163.com` historical capture sufficient to establish:

- exact charset;
- DOM structure;
- frameset layout;
- form `method`;
- form `action`;
- input names;
- cookie names;
- CGI/ASP endpoint;
- attachment uploader behavior;
- browser requirements.

A search-engine image or a later historical screenshot is only a lead.

Per `docs/METHOD.md`:

> **archive locator / screenshot lead ≠ verified capture.**

Do not reconstruct those fields from memory.

---

## 11. 2008 QQ Mail evidence: notification is another layer, not proof of reading

A public July 2008 Usenet discussion preserved by Google Groups contains contemporary users discussing QQ Mail. One participant notes that when mail arrives, QQ can automatically notify the user; participants also discuss POP3, forwarding and file-transfer features.

Source / B/C contemporary user discourse:
- https://groups.google.com/g/cn.fan/c/O1vEHiOns1A

This is useful for a state distinction:

```text
mail stored
→ QQ notification generated
→ QQ client receives notification
→ user notices notification
→ user opens mailbox
→ user opens message
```

### 11.1 `notification-generated / notification-seen gap`

A notification feature existing does not prove:

- client was running;
- user was online;
- notification was delivered;
- user noticed it.

### 11.2 `notification-seen / message-read gap`

Seeing “new mail” is not the same as opening or understanding the mail.

### 11.3 Archaeological significance

Webmail is no longer always a self-contained website.

By the late 2000s its user-visible state can be distributed across:

- mail Web app;
- QQ/IM client;
- POP3 client;
- forwarding target;
- mobile device.

A single preserved page can therefore under-represent the historical system.

---

## 12. Email use-rate decline does not equal service death

A 2008 article by a CNNIC researcher, citing CNNIC survey data, reports:

- email use rate fell from 64.7% at end-2005 to 56.5% at end-2007;
- instant messaging rose from 41.9% to 81.4%.

Source / B+:
- https://www.cnbeta.com.tw/articles/tech/56921.htm

For old-Web archaeology this creates a methodological warning:

> **declining application share ≠ platform disappearance ≠ historical irrelevance.**

A service can become less central to casual communication while remaining crucial for:

- job applications;
- submissions;
- school/institution messages;
- account recovery;
- cross-organization communication.

Do not use popularity curves as a shortcut for service-state inference.

---

## 13. 2013 job-search evidence: address presentation is not delivery state

A 2013 contemporaneous report investigated the rumor that QQ-mail résumés were automatically rejected by HR departments.

The report found that interviewed HR staff largely denied such a blanket rule, though some mentioned:

- strange QQ display nicknames as unprofessional presentation;
- possible spam/advertising filtering;
- the importance of a clear sender name/contact identity.

Source / B:
- https://www.chinanews.com.cn/edu/2013/10-29/5435325.shtml

This requires several separate state layers:

```text
mail technically delivered
recipient spam/filter placement
sender display-name rendering
recipient sees sender/domain
recipient social interpretation
recipient opens attachment
recruitment decision
```

### 13.1 `delivery / presentation gap`

A technically successful message can still be poorly presented.

### 13.2 `presentation / decision gap`

A strange nickname does not prove rejection.

### 13.3 `rumor / organizational-policy gap`

A widely shared forum claim is not evidence of a universal HR rule.

This is a useful counterexample to over-reading contemporary user folklore.

---

## 14. Public Web archive vs private-mail archive: a structural asymmetry

Webmail produces two radically different kinds of historical material.

### Public control surface

Likely to be crawlable:

- homepage;
- help;
- feature pages;
- login form;
- registration page;
- quota announcement;
- pricing;
- provider news.

### Private state

Normally unavailable, access-controlled or ethically inappropriate to recover:

- inbox listing;
- message bodies;
- attachments;
- address book;
- drafts;
- read/unread flags;
- passwords;
- recovery questions;
- spam decisions;
- message-delivery logs.

This is **control-surface / private-state asymmetry**.

The better a service did its job protecting private mail, the worse public Web archaeology may be at reconstructing actual lived correspondence.

That is not archive failure in the simple sense; it is partly the expected result of authentication/privacy architecture.

---

## 15. Historical visibility bias: the most consequential message may be the least visible artifact

A public archived page can prove:

- “submit résumé by email”; or
- “contact us at this mailbox”.

But the consequential state may be:

```text
one private message arrives
→ one person reads it
→ buys a train ticket
→ attends an interview
→ relocates
```

The companion life-history note includes a 2020 graduate who saw interview notices in her inbox in Henan and then flew to Shanghai for interviews.

For old-Web work, the important principle is:

> **historical consequence is often inversely correlated with public archival visibility.**

The UI announcing the channel is public and easy to save.

The single private message that changed a life is private and usually absent.

---

## 16. Recommended Webmail state-gap taxonomy

### Service identity

- `brand/domain gap`
- `near-name continuity gap`
- `operator/owner gap`
- `brand-survival/backend-survival gap`
- `corporate-sale/account-migration gap`

### Registration/account

- `registration-page/account-created gap`
- `username-available/account-created gap`
- `address-string/live-account gap`
- `active/dormant gap`
- `inactive/reclaimed gap`
- `reclaimed/reassigned gap`

### Authentication

- `login-page/auth-backend gap`
- `credential-form/session gap`
- `session/inbox gap`
- `cookie-domain gap`

### Message delivery

- `compose/send-submit gap`
- `web-success/MTA-acceptance gap`
- `local-MTA/remote-MTA gap`
- `remote-acceptance/inbox-storage gap`
- `stored/noticed gap`
- `noticed/read gap`
- `read/reply gap`
- `reply/real-world-outcome gap`

### Storage/content

- `quota-version gap`
- `quota/actual-storage gap`
- `message/attachment gap`
- `server-copy/local-copy gap`
- `message-present/message-survival gap`

### Notification/integration

- `mail-arrival/notification-generated gap`
- `notification-generated/client-delivery gap`
- `notification-delivered/human-notice gap`
- `human-notice/message-open gap`

### Archive/replay

- `public-shell/private-state gap`
- `main-document/subresource gap`
- `historical-charset/modern-decoding gap`
- `historical-JS/archive-rewrite gap`
- `login-form/dead-endpoint gap`
- `screenshot/verified-capture gap`

---

## 17. Minimal claim ladder for a historical Webmail artifact

Use the narrowest supported claim.

### Level 1 — public service described

> A contemporary page described a free Webmail service under domain X.

### Level 2 — public operation documented

> Contemporary reporting/users documented registration/login/Web mail use.

### Level 3 — account existence

Requires evidence tied to an account, without exposing unnecessary personal data.

### Level 4 — message transaction

Requires actual transaction/log/message evidence.

### Level 5 — message delivery

Requires remote acceptance/storage or recipient-side evidence.

### Level 6 — human reading

Requires recipient testimony/client state.

### Level 7 — real-world consequence

Requires independent evidence linking the message to action.

Do not jump from Level 1/2 to Level 5–7.

---

## 18. Capture checklist for a future 1998–2005 Webmail find

When an actual archive capture is located, record at least:

```yaml
archive_source:
capture_url:
original_url:
capture_datetime:
accessed_at:
http_replay_state:
redirect_or_error:
host:
brand:
operator_at_time:
address_domain:
content_type:
charset:
frameset:
forms:
  method:
  action:
  input_names:
js_resources:
image_resources:
cookies_observable:
login_endpoint_replayable:
registration_endpoint_replayable:
subresources_missing:
archive_rewrite_observed:
browser_assumption:
evidence_grade:
confidence:
```

If an item is not observable, write `unknown` rather than reconstructing it from a later product.

---

## 19. Privacy stop conditions specific to Webmail

Historical email is unusually privacy-sensitive because messages can contain:

- private correspondence;
- job/education records;
- account recovery links;
- address books;
- attachments;
- health/family details;
- passwords or secrets in old mail;
- identity connections not otherwise public.

Therefore:

1. do not attempt to authenticate into historical private accounts;
2. do not reuse leaked credential dumps as an archaeology source;
3. do not bulk-publish historical personal email addresses;
4. when a public page lists a normal person’s address, quote only if necessary for the claim and minimize it otherwise;
5. do not test whether a historical address is currently controlled by the same person;
6. do not send mail to old addresses merely to test liveness;
7. provider/domain-level structure is normally sufficient for this repository.

---

## 20. Hindsight risks

### Risk A — “email existed” becomes “ordinary people used it”

A product/service page proves availability, not social distribution.

### Risk B — current `163.com` is projected backward into `163.net`

Keep historical domains/operators separate.

### Risk C — current Webmail UI is used to reconstruct 1999

Do not infer modern fields, CAPTCHA, HTTPS, AJAX or mobile integration backward.

### Risk D — provider account count becomes population count

Use the provider’s original unit (`registered accounts`, `members`, etc.).

### Risk E — `发送成功` becomes delivery/read proof

Keep message states separate.

### Risk F — declining email-use share becomes “email died”

Later formal/high-consequence uses contradict a simple extinction model.

### Risk G — public archive absence becomes “feature did not exist”

Authentication, dynamic URLs, robots or private state may explain absence.

---

## 21. What is established

- By 1999, `163.net` free Webmail was a real public Chinese Internet service with substantial reported registrations, capacity expansion, inactivity cleanup and small quotas.
- `163.net` and later NetEase `@163.com` must be treated as different historical service/domain objects unless a specific continuity claim is independently demonstrated.
- Webmail account life involved provider policy, quota, inactivity and corporate/service transitions.
- By 2008, QQ could function as a notification layer around email for at least some contemporary users.
- Declining email-use rate during the rise of IM does not prove Webmail services vanished or stopped carrying high-consequence tasks.
- Public archive preservation is structurally much better for login/help/marketing pages than for private inbox and delivery state.

## 22. What remains uncertain

This pass still lacks a verified early capture sufficient to answer:

- exact `163.net` login URL in a specific 1998/1999 month;
- exact charset and historical browser rendering;
- form endpoints;
- cookie/session names;
- Webmail folder URLs;
- exact attachment upload mechanism;
- whether a specific provider sale migrated all mail contents/account passwords unchanged;
- message-level delivery statistics;
- how often ordinary users in different social groups checked mail.

These unknowns should remain visible.

---

## 23. Why this changes old-Web interpretation

Webmail demonstrates a particularly severe archival mismatch:

> **The public Web preserves the doorway much better than the room behind it.**

For a personal homepage, the page itself may be the historical action.

For Webmail, the page is often only a control surface into a private distributed system.

The actual historical event may have crossed:

```text
browser
→ session
→ mailbox database
→ MTA
→ DNS
→ another provider
→ private inbox
→ human attention
→ offline life
```

Almost none of that chain is guaranteed to survive in a Web archive.

Therefore a surviving Webmail login screen should be treated not as a preserved mailbox, but as evidence that **a much larger, mostly invisible communication infrastructure once sat behind that page**.

---

Initial state-gap model drafted with AI assistance. Preserve the evidence grades, privacy limits and explicit unknowns in later revisions.
