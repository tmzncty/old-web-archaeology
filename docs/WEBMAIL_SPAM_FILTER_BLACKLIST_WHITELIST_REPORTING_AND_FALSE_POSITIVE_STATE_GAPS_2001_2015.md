# WEBMAIL_SPAM_FILTER_BLACKLIST_WHITELIST_REPORTING_AND_FALSE_POSITIVE_STATE_GAPS_2001_2015

Status: research note / state-gap model  
Scope: approximately 2001–2015 Chinese public-Web evidence around Webmail anti-spam controls, blacklist/whitelist infrastructure, user reporting, filtering, false positives and the preservation limits of private inbox/filter state  
Companion life-history note: `tmzncty/how-people-lived/topics/from-reachability-to-attention-perimeter-spam-harassment-filtering-and-defensive-unreachability-china-preweb-2026.zh-CN.md`

## 0. Why this is a separate old-Web object

The repository already has:

- `WEBMAIL_ACCOUNT_ADDRESS_DELIVERY_AND_SERVICE_CONTINUITY_STATE_GAPS_1998_2015.md`;
- `docs/WEBMAIL_PORTABLE_ADDRESSES_ACCOUNT_RECLAMATION_DELIVERY_AND_IDENTITY_STATE_GAPS_1998_2003.md`;
- `docs/SMS_WEB_GATEWAY_SUBSCRIPTION_SP_BILLING_DELIVERY_AND_CONTROL_PLANE_STATE_GAPS_2000_2015.md`.

Those notes correctly include spam/filtering as one layer in a longer delivery chain, but they do not yet reconstruct **filter state itself**.

This note asks a narrower archaeological question:

> When an old Chinese Webmail page says “垃圾邮件”“黑名单”“白名单”“举报垃圾邮件” or “反垃圾”，what state actually had to exist behind that control, and what can a surviving page prove about whether a historical message reached the normal inbox?

The master warning is:

> **mail accepted ≠ mail stored ≠ mail classified as legitimate ≠ mail shown in inbox ≠ human noticed ≠ human trusted ≠ real-world response.**

This matters because anti-spam systems intentionally create **negative states**: messages that are diverted, quarantined, hidden, rejected or deleted. Those are precisely the states public Web archives preserve least well.

This note stays within the approximately 1995–2015 Chinese-old-Web scope. ARPANET/Usenet/global spam prehistory belongs in the companion `how-people-lived` note. A desktop mail client such as Foxmail appears here only as a bounded adjacent artifact because it exposes local blacklist/whitelist/filter state that helps reconstruct Chinese users’ actual mail environment; this is not a scope expansion into general desktop-software history.

---

## 1. Research units

Per `docs/METHOD.md`, keep the following separate:

- mail-service brand;
- address domain;
- Webmail host;
- authenticated mailbox;
- one message;
- SMTP sender / sending IP;
- sending domain;
- receiving MTA;
- provider-wide blacklist;
- provider-wide whitelist;
- industry/shared reputation list;
- user-local blacklist;
- user-local whitelist;
- keyword/rule filter;
- Bayesian/statistical classifier;
- virus/security layer;
- spam/quarantine folder;
- “report spam” action;
- “not spam” / restore action;
- user notification;
- local mail-client filter state;
- archived public page;
- archive capture;
- researcher claim.

These objects can share a label such as “垃圾邮件” without sharing one lifecycle.

---

## 2. Evidence grades in this note

### A / A-

- original dated regulatory/institutional pages;
- original service/provider documentation with clear provenance;
- verified historical archive capture actually opened and inspected.

### B / B+

- contemporaneous newspaper/technology reporting;
- contemporaneous user tutorials for observable UI/operation;
- later institutional page preserving a dated earlier event, clearly labeled as such.

### C

- later nostalgia/recollection;
- search snippets or screenshots without sufficient provenance.

### D

- state machines, preservation levels and reconstruction hypotheses below.

This run does **not** claim a verified 2007 Wayback/WARC capture of `iscbl.anti-spam.cn`.

---

## 3. 2004 client-side anchor: filtering could be a local personal state

A 2004-04-27 *China Computer Education News* tutorial reproduced by Sina described Foxmail 5.0 anti-spam behavior in unusually concrete terms:

- a sender in the blacklist could cause a message to be classified as spam and moved to a waste/deleted area;
- Bayesian filtering followed after blacklist checks;
- Bayesian filtering required the user to train the client on spam and non-spam messages;
- the user could manually add senders to the blacklist;
- blacklist/whitelist state was associated with local client files/settings.

Contemporaneous source / B:
- https://tech.sina.com.cn/c/2004-04-27/1049355188.shtml

### What it proves

It proves that one Chinese mail environment in 2004 exposed filtering as user-maintained state, including both explicit sender lists and learned classification.

### What it does not prove

It does not prove:

- Foxmail usage prevalence among Chinese Internet users;
- that a particular historical Webmail provider used the same classifier;
- that all installations had identical default rules;
- that a message classified as spam was actually unwanted;
- that blacklist/whitelist files survived a reinstall or machine change.

### Archaeological consequence: `local-filter portability gap`

A mailbox address might be portable while its learned attention boundary was not:

```text
same email address on new PC
+
old local filter files absent
→
old blacklist/whitelist/Bayesian state not necessarily present
```

Therefore “user still had the same email address” cannot prove “user still experienced the same filtering environment.”

---

## 4. 2007 shared anti-spam infrastructure: the filter boundary moved above one mailbox

On 2007-06-18, the China Internet Association anti-spam integrated processing platform opened. Contemporaneous Xinhua-derived reports preserve the historical host `iscbl.anti-spam.cn` and describe:

- data sharing among telecom operators and mail service providers;
- real-time/regular publication of spam-server IP blacklists;
- a mail-service whitelist;
- ten large mail operators connected to the whitelist platform, including Sina, NetEase, TOM, 263, Wanwang, Sohu, Yahoo, Suntek/Shangyi, 21CN and Tencent.

Contemporaneous sources / B+:
- https://tech.sina.com.cn/i/2007-06-19/09201570210.shtml
- https://news.sina.com.cn/c/2007-06-19/094212050640s.shtml

The contemporary report’s market/user-share statement is a provider/association claim and must not be silently converted into independently verified national adoption.

### 4.1 New research unit: shared reputation state

The relevant state chain is no longer only:

```text
user adds sender to personal blacklist
```

but potentially:

```text
reports / observed sending behavior
→ shared server/IP reputation record
→ provider consults shared record
→ receiving decision affected
→ message accepted / rejected / diverted
```

A historical recipient may never know which layer caused the decision.

### 4.2 `global/provider/user filter gap`

Always separate:

```text
industry shared list
provider-wide rule
account-level rule
local-client rule
```

A message that disappears before Webmail storage cannot be inferred from a user’s later spam-folder contents.

---

## 5. Why whitelist evidence is as important as blacklist evidence

The 2007 platform did not only advertise blacklists; it also built a whitelist.

That is important because anti-spam archaeology can otherwise fall into a simplistic model:

```text
bad mail exists
→ filter catches it
→ problem solved
```

The existence of whitelist infrastructure demonstrates the opposite engineering constraint:

> **blocking unwanted traffic can disrupt legitimate mail traffic, so anti-spam systems also need explicit paths for trusted senders.**

A later China Internet Association page describing the 2007 platform similarly states that the whitelist was meant to reduce normal-mail communication problems caused by relying on blacklist blocking alone. Institutional later-preserved evidence / B:
- https://www.isc.org.cn/article/15536.html

### `false-positive invisibility`

False positives are unusually hard to archive.

Suppose a 2008 graduate waited for an interview email that never appeared in the normal inbox. Possible states include:

```text
employer never sent
sent but local MTA rejected
remote MTA rejected/deferred
provider blacklist blocked
provider classifier quarantined
user rule moved it
local client filtered it
mail stored in spam folder but never noticed
auto-deleted before inspection
```

A public archive normally cannot distinguish them.

This means old-Web evidence structurally over-preserves **successful visible communication** and under-preserves legitimate messages that disappeared inside filtering.

---

## 6. The key message-classification state machine

For a single historical email, use at least:

```text
sender composes
→ send transaction accepted
→ outbound MTA accepts
→ DNS/MX route succeeds
→ receiving MTA accepts/defer/reject
→ shared reputation check
→ provider policy check
→ spam/virus classifier
→ user rules
→ stored in inbox/spam/quarantine/other folder OR dropped/rejected
→ Webmail folder listing exposes message
→ notification generated or not
→ user logs in
→ user notices message
→ user trusts sender/content
→ user opens/replies/acts
```

Do not collapse these into `sent → received`.

### 6.1 `SMTP-accepted / mailbox-stored gap`

A receiving server may accept a transaction before later policy handling; a sending-side success indication is not proof of inbox storage.

### 6.2 `stored / inbox gap`

A message can exist in the mailbox but not the inbox.

### 6.3 `spam-folder / noticed gap`

A spam folder is not equivalent to user attention. The user may never open it.

### 6.4 `not-spam click / backend-learning gap`

A surviving UI control labeled “不是垃圾邮件” can prove that such an action was presented. It does not by itself prove:

- the request completed;
- a global reputation database changed;
- a sender entered a persistent whitelist;
- future messages were guaranteed inbox placement.

### 6.5 `whitelist / guaranteed-delivery gap`

Whitelisting can bypass one decision layer while later layers still fail because of:

- quota;
- account disabled;
- malformed message;
- virus policy;
- downstream client rule;
- provider outage.

Thus:

```text
whitelisted ≠ delivered ≠ noticed
```

---

## 7. Spam reporting is a transaction, not a static button

A historical “举报垃圾邮件” button can correspond to several possible workflows:

```text
user selects message
→ clicks report
→ browser sends message ID / sender / headers / category
→ provider accepts report
→ message moved/deleted locally
→ provider aggregates signal
→ sender/IP/domain reputation may change
→ future traffic may be treated differently
```

### `report-control / report-commit gap`

A captured button proves the control existed, not that a historical report transaction succeeded.

### `report / reputation-update gap`

Even successful reporting need not mean one report immediately changed global reputation.

### `cross-user state gap`

A sender reported by account A may still be treated differently for account B because:

- user-local lists differ;
- account history differs;
- provider tier differs;
- classifier version differs;
- rollout differs by cluster/time.

A single inbox screenshot cannot establish provider-wide classification behavior.

---

## 8. Spam folder retention creates a preservation paradox

Spam systems are often designed to make unwanted content disappear.

Possible policies include:

```text
move to spam
→ retain N days
→ purge automatically
```

or:

```text
reject before mailbox storage
```

or:

```text
quarantine outside normal mailbox UI
```

Therefore old-Web historical corpora are biased in a special way:

> **the more successfully a system treated something as disposable, the less likely the message is to survive as a user-visible artifact.**

Call this `filter-success / archive-survival inversion`.

A researcher must not reason:

```text
I found few preserved spam messages
→ the historical user received little spam
```

The evidence may be missing precisely because the system was built to erase it.

---

## 9. Reputation has time: never replay today’s classification as historical fact

A sender/IP/domain reputation can change across hours, days or years.

Define:

- **reputation temporal drift**: today’s spam reputation is not historical reputation;
- **classifier-version drift**: same message body can receive different classifications after model/rule updates;
- **list membership drift**: an IP/domain can enter/leave blacklists and whitelists;
- **service-topology drift**: the same domain may later send from different infrastructure.

Therefore:

```text
same historical message submitted to a modern spam filter
≠ historical classification replay
```

At best it is a modern experiment.

Likewise:

```text
modern Webmail shows sender as “trusted”
≠ sender was trusted in 2007
```

---

## 10. Address exposure is not spam-delivery proof

Chinese old Web pages often expose email addresses in:

- personal homepages;
- BBS signatures;
- guestbooks;
- contact pages;
- software README files;
- mailing-list archives.

These are valuable evidence that an address string was public, but the correct boundary is:

```text
public address visible
≠ automated harvester fetched it
≠ spammer obtained it from that page
≠ spam was sent
≠ spam was delivered
≠ user saw it
```

Call this `address-exposure / harvesting gap`.

Do not turn the survival of an old email address into a causal story about where harassment came from without an independent chain.

---

## 11. From email spam to cross-channel contamination: keep channels separate

By the late 2000s, Chinese anti-spam reporting increasingly discussed unsolicited information across email, SMS, telephone/fax and instant messaging. For life history this is a major convergence: one stable person can be reached through several channels.

But old-Web archaeology must not merge them into one “spam event.”

For each item record:

```yaml
channel: email | sms | phone | im | fax
sender_identifier:
recipient_identifier:
carrier_or_provider:
classification_layer:
user_action:
backend_action:
evidence_type:
capture_time:
```

A phone-number blacklist is not an email-IP blacklist; an SMS report is not an SMTP reputation event.

The companion `how-people-lived` note handles the cross-channel social consequence. This file stays focused on Webmail/anti-spam state and uses other channels only to mark the boundary.

---

## 12. Public page survival vs authenticated filter state

A public anti-spam/help page may preserve:

- “垃圾邮件” menu label;
- help article;
- blacklist/whitelist descriptions;
- screenshots;
- report address/hostname;
- product claims.

It normally cannot preserve:

- a real account’s inbox/spam folder;
- private sender lists;
- message headers;
- provider reputation DB;
- Bayesian/model training state;
- user report history;
- server-side ruleset version;
- authentication/session state.

Therefore establish these explicit gaps:

### `spam-folder-shell / spam-content gap`

A folder named “垃圾邮件” does not prove any particular message was inside.

### `filter-UI / filter-backend gap`

A rule configuration page does not prove the historical filtering backend survived.

### `help-text / actual-policy gap`

Help text can lag rollout or account tier. It proves documentation, not necessarily every account’s actual state.

### `screenshot / operational-state gap`

A screenshot can show controls but cannot prove requests worked.

### `archive-capture / authenticated-state gap`

A public capture cannot stand in for private mailbox state.

---

## 13. Privacy stop conditions

Private inbox/spam-folder history is unusually sensitive. It may expose:

- illness;
- job search;
- finances/debt;
- sexuality/intimate relationships;
- private purchases;
- account recovery links;
- addresses/phone numbers;
- third-party identities.

Therefore highest-quality archaeology does **not** require obtaining a real person’s private spam archive.

Prefer:

- public help pages;
- vendor documentation;
- screenshots already intentionally published by the historical user;
- synthetic/test messages;
- sample headers with personal data removed;
- software configuration format without republishing actual private sender lists;
- institutional blacklist/whitelist policy documents.

Do not republish historical private inboxes simply because credentials/data happen to survive.

---

## 14. Suggested preservation levels

Use a bounded ladder:

### S0 — mention only
A dated source says anti-spam/filtering existed.

### S1 — public documentation preserved
Help/tutorial describes controls or policy.

### S2 — UI artifact preserved
Screenshot/page exposes blacklist/whitelist/spam/report controls.

### S3 — local filter artifact/schema preserved
Configuration/file format is known, but private entries are redacted or synthetic.

### S4 — verified historical public capture
Exact URL/capture datetime/HTTP/charset/DOM inspected.

### S5 — privacy-safe message/header + historical classification metadata
Enough to distinguish inbox/spam/reject state for a demo/test case.

### S6 — dated rules/reputation policy version preserved
Provider/industry decision layer documented.

### S7 — end-to-end historical behavior reproducible
Rare: sender path, receiver path, ruleset and classification behavior all evidenced without violating privacy.

Do not invent S7 from a replayable UI shell.

---

## 15. Historical replay attempt in this slice

The contemporaneous 2007 sources provide a concrete archive target:

```text
iscbl.anti-spam.cn
```

This run attempted direct Wayback replay/CDX access for approximately 2007–2008. The current research access path rejected the constructed archive URLs before a memento/CDX result could be inspected.

Therefore:

```text
M1 verified iscbl.anti-spam.cn historical capture: NOT ACHIEVED IN THIS SLICE
```

This means only:

> no qualifying capture was opened and inspected in this run.

It does **not** mean:

- Wayback has no capture;
- the hostname did not exist;
- the public platform did not operate.

The hostname and 2007 launch are independently supported by contemporaneous reporting.

Per `docs/METHOD.md`, keep:

```text
archive locator / candidate URL ≠ verified capture
no verified capture in this run ≠ historical nonexistence
```

---

## 16. What this changes for Chinese old-Web archaeology

Spam filtering adds a new class of preservation problem: **historical invisibility can itself be a product feature.**

For normal Web archaeology, absence often comes from broken links, lost databases or missing media. In anti-spam systems, absence can instead mean:

```text
rejected correctly
moved correctly
auto-deleted correctly
hidden correctly
```

That creates a special hindsight risk. A preserved normal inbox or public screenshot tends to show what successfully crossed the filter, while messages that shaped the user’s distrust, blocking habits and missed opportunities may be disproportionately absent.

So a serious reconstruction must preserve both sides:

```text
reachability infrastructure
+
attention-boundary infrastructure
```

Otherwise a history of Webmail will overstate “message delivery” and understate the daily work required to decide which delivered messages deserved attention.

---

## 17. Bounded source ledger

1. 2004 Foxmail 5.0 blacklist/whitelist/Bayesian tutorial, *China Computer Education News* via Sina:  
   https://tech.sina.com.cn/c/2004-04-27/1049355188.shtml

2. 2007 anti-spam integrated processing platform launch, Xinhua-derived report via Sina, preserving `iscbl.anti-spam.cn`:  
   https://tech.sina.com.cn/i/2007-06-19/09201570210.shtml

3. Second contemporaneous Xinhua-derived launch report:  
   https://news.sina.com.cn/c/2007-06-19/094212050640s.shtml

4. China Internet Association later-preserved institutional discussion of whitelist/false-positive problem:  
   https://www.isc.org.cn/article/15536.html

5. Cross-channel companion evidence only: 2008 ordinary-user SMS opt-out experience, *Market News* via China News Service:  
   https://www.chinanews.com.cn/it/txxw/news/2008/05-12/1245741.shtml

6. Companion life-history institutional endpoint: MIIT 2025 Q2 telecom-service notice and “来电来信免打扰”:  
   https://www.miit.gov.cn/zwgk/zcwj/wjfb/tg/art/2025/art_e279d1f22f6a4f7d9ced09a8e6ed289d.html

7. Companion life-history current endpoint: MIIT 2026 Q2 telecom-service notice:  
   https://wap.miit.gov.cn/zwgk/zcwj/wjfb/tg/art/2026/art_440c2ded2ba54f0387b4cca50acf8147.html

---

Initial draft AI-assisted. All historical interface/backend claims must remain bounded to the cited evidence and `docs/METHOD.md`; inferred state machines are D-grade reconstruction models, not claims that every provider implemented the same backend.
