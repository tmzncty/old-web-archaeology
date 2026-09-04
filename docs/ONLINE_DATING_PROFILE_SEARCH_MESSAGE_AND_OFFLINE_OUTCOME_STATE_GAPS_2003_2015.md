# Online dating profiles, search, messages, and offline relationship state gaps, 2003–2015

## Scope

This note models Chinese old-web dating / marriage-search platforms as **stateful systems whose public pages are only the front edge of a much longer relationship chain**.

Main research object remains the Chinese Web, approximately 1995–2015.

Pre-Web personals and overseas computer matching appear only as boundary/comparison material in the companion `how-people-lived` note. This repository does **not** become a global history of dating technology.

Cross-repository companion note:

- `tmzncty/how-people-lived/topics/mediated-partner-search-personals-online-dating-and-searchable-intimacy-china-1981-2026.zh-CN.md`

Central archaeological warning:

> **An archived dating profile is not a verified person, a search hit is not a mutual match, a readable message is not a reply, and a platform “success” state is not evidence that a relationship or marriage occurred.**

Because dating profiles contain unusually sensitive personal information, this topic also requires stricter privacy minimization than ordinary portal archaeology.

---

## 1. Why dating platforms need a separate state model

A historical dating interaction may depend on:

- registration state;
- account identity;
- profile completion;
- profile moderation;
- self-reported attributes;
- optional documentary proof;
- search-index inclusion;
- ranking / promoted visibility;
- query filters;
- login state;
- message composition;
- moderation or anti-spam rules;
- payment / virtual-stamp state;
- recipient login;
- message readability;
- reply;
- off-platform contact exchange;
- telephone / QQ / later WeChat contact;
- in-person meeting;
- relationship formation;
- relationship-status update;
- hiding/deleting the account.

A web archive can preserve the landing page or profile shell while losing nearly every state that determines the real outcome.

---

## 2. Minimum object decomposition

Do not merge the following objects.

### 2.1 Platform / brand

Examples may include Jiayuan, Baihe, Zhenai and earlier dating/community services.

A brand name is not a stable technical system across years.

### 2.2 Registered account

An account identifier in the platform database.

Do not assume:

`one account = one unique person`.

### 2.3 Profile

A representation attached to an account, potentially including:

- age;
- sex/gender field as defined by the historical platform;
- location;
- height;
- education;
- income;
- relationship/marital status;
- photographs;
- self-description;
- desired-partner filters;
- verification markers.

A profile is a historical artifact of **claims and platform fields**, not a census record.

### 2.4 Search index entry

The platform's searchable representation of a profile.

A profile can exist but be excluded, hidden, stale, demoted or promoted in search.

### 2.5 Search result page

A dynamic result generated from query filters, index state, ranking rules and possibly payment/promotional state.

### 2.6 Message object

A platform communication record. It may have separate states for sent, accepted, moderated, paid/unlocked, delivered, read and replied.

### 2.7 Verification artifact

Platform state indicating that some attribute was checked or a proof was submitted.

This is not equivalent to proving every statement in the profile.

### 2.8 Relationship-status field

A user/platform account field such as “currently dating someone” or “in a relationship.”

Treat it as an account state unless independent evidence supports the real-world relationship.

### 2.9 Offline interaction

Telephone, QQ, meeting, family introduction, cohabitation, marriage or any other state outside the platform.

Normally invisible to a public web archive.

### 2.10 Capture

One archived representation at one datetime.

The capture is not the live platform database.

---

## 3. Core state chain

A dating-platform path should be modeled as:

```text
public landing page exists
→ registration endpoint available
→ account created
→ profile fields submitted
→ profile accepted/moderated
→ profile included in search index
→ query submitted
→ search backend executes
→ candidate appears in result set
→ candidate profile viewed
→ initial message composed
→ platform accepts message
→ moderation/anti-spam state passes
→ payment/unlock condition satisfied if required
→ recipient logs in
→ recipient can read message
→ recipient replies
→ repeated exchange occurs
→ private contact information exchanged
→ communication leaves the platform
→ meeting proposed
→ meeting actually occurs
→ further meetings / relationship may occur
→ account relationship status may change
→ profile may be hidden, stale or deleted
```

None of these arrows is safe to infer automatically.

---

## 4. Evidence anchor: 2008 Chinese users were already performing structured partner search

A China Youth Daily report dated 2008-03-03 described a user entering age, education and monthly salary into Jiayuan's search interface and receiving dozens of candidate profiles. The user valued self-directed search, login-time flexibility and a larger range of options.

Source:

- https://www.dzwww.com/xinwen/guoneixinwen/200803/t20080303_3228860.htm

Evidence grade: **B — contemporaneous media observation and user statement**.

The same report said the reporter observed search criteria extending across more than ten fields, including age, sex, height, credit rating and test type.

What this supports:

- structured profile fields were part of the user-facing search logic by 2008;
- search could expose many candidate profiles quickly;
- platform use could be scheduled around work time.

What it does not support:

- exact historical DOM;
- exact query parameter names;
- the truth of profile fields;
- search-ranking algorithm details;
- a national adoption rate;
- offline relationship outcomes.

---

## 5. Life-script serialization gap

Dating search creates an unusually consequential database problem: social expectations about adulthood are converted into queryable fields.

A historical platform may expose fields for:

```text
age
education
income
location
height
relationship status
personality/test label
partner preference
```

But the following must remain separate:

```text
field exists
≠ field required
≠ user filled field
≠ value truthful
≠ value verified
≠ searcher used field
≠ field influenced ranking
≠ field mattered after meeting
```

When reconstructing a historical search form, record the **actual visible field set for that capture**, not a later platform's schema.

---

## 6. Strong platform document: Jiayuan 2011 F-1

Jiayuan.com International Ltd. filed an F-1 with the U.S. SEC on 2011-04-20.

Source:

- https://www.sec.gov/Archives/edgar/data/1511683/000104746911003874/a2203517zf-1.htm

Evidence grade: **A for contemporaneous formal company claims, product definitions and business metrics.**

It is not independent evidence that the company's claimed matching effectiveness was true.

The filing documents a platform state machine much richer than a static profile directory.

It says users could:

- register for free;
- search the database;
- send an initial message without a sending fee;
- require either sender or recipient to purchase a RMB2 virtual stamp before that initial message became readable;
- communicate freely on-platform after the first message was read;
- purchase services including improved search ranking, priority messaging, online chat and premium display;
- submit proof for profile information;
- participate in offline gatherings and VIP services.

This means historical archaeology must separately model **visibility, readability and payment state**.

---

## 7. Registration/account multiplicity gap

The 2011 F-1 reported 40.2 million registered user accounts as of 2011-03-31 and separately defined active user accounts.

The filing also warns in its definitions that registered account counts can include multiple accounts associated with one registered user.

Therefore never convert:

```text
40.2 million registered accounts
```

into:

```text
40.2 million people
```

Recommended fields:

```yaml
metric_name:
metric_date:
unit: account|user|visitor|paying_account|active_account
platform_definition:
multiple_accounts_possible:
source:
```

---

## 8. Profile-subject identity gap

A profile can be:

- created by the subject;
- partly assisted by staff;
- stale;
- duplicated;
- maliciously impersonating someone;
- filled with inaccurate values;
- abandoned while remaining visible.

Archive-safe statement:

> “This capture displays a profile claiming X.”

Unsafe statement without independent evidence:

> “This person was X.”

This distinction is especially important for income, marital status, age and employment.

---

## 9. Verification-state gap

The Jiayuan F-1 says the platform encouraged users to provide proof of age, income and education, and offered rating/verification-related mechanisms.

That produces a state chain:

```text
self-reported value
→ proof submission option exists
→ user submits material
→ platform receives material
→ platform review occurs
→ verification marker/rating changes
→ future searcher sees marker
```

Do not collapse it into “verified profile.”

Questions for a future historical capture:

```yaml
verification_type:
verification_badge_text:
proof_required_or_optional:
verification_scope:
verification_date_visible:
expiry_or_recheck_known:
manual_review_claimed:
```

If the evidence does not reveal what the badge actually verified, keep scope unknown.

---

## 10. Search-index inclusion gap

A profile's existence does not guarantee it can be found.

Possible states:

1. profile exists but not yet indexed;
2. profile hidden by user;
3. profile excluded by moderation;
4. profile visible only to certain account classes;
5. profile appears only under some filters;
6. profile is demoted;
7. profile is promoted by paid visibility;
8. profile remains indexed after the user has stopped searching.

Therefore:

```text
profile URL survives
≠ profile was discoverable in ordinary search at that datetime
```

---

## 11. Ranking / visibility monetization gap

The 2011 F-1 documents value-added services including improved search ranking and premium display.

This is a key old-web state gap:

```text
profile meets query filters
≠ profile receives same visibility as another matching profile
```

A historical result page can be shaped by:

- match criteria;
- recency;
- activity state;
- paid promotion;
- platform ranking rules;
- moderation;
- geography;
- login/account class.

Without evidence, do not reconstruct “natural” ranking from visible fields alone.

---

## 12. Initial-message / readable-message gap

Jiayuan's 2011 F-1 gives a concrete example where message states differ.

A simplified chain is:

```text
sender clicks send
→ message accepted
→ initial message exists
→ RMB2 virtual-stamp condition satisfied by sender or recipient
→ message becomes readable
→ recipient logs in
→ recipient opens/reads
→ recipient replies
```

Therefore an interface message such as “sent successfully” cannot prove that the recipient ever read the content.

Archive fields should distinguish:

```yaml
message_sent_ui:
message_object_confirmed:
payment_required:
payment_satisfied:
readability_confirmed:
read_receipt_feature:
reply_confirmed:
```

Most public archives will only have the first one or two.

---

## 13. Moderation / delivery gap

The 2011 filing describes keyword screening/manual review and user-reporting/blacklist mechanisms.

That creates another hidden state:

```text
user submits message/profile text
≠ platform accepts it unchanged
≠ recipient receives it
```

Potential transformations include:

- rejection;
- delayed review;
- keyword blocking;
- text removal;
- account restriction;
- user blacklist effects.

A capture of a composition form does not prove the historical moderation result.

---

## 14. Off-platform handoff gap

The F-1 states that, based on company historical data, the average exchange between two users on Jiayuan lasted 3.5 days, and the company believed interested users then exchanged personal contact information to communicate directly.

This is one of the most important archaeological facts in this topic.

The intended path often became:

```text
site search
→ site message
→ limited site exchange
→ telephone / QQ / other private channel
→ possible meeting
```

So a platform can be most effective precisely when the relation disappears from its public/archive-visible space.

Call this **successful disappearance bias**.

The absence of long on-platform message histories is not evidence that no relationship continued.

---

## 15. Platform status / real relationship gap

The F-1 reports an operational metric based on users changing relationship status to states such as “currently dating someone” or “in a relationship.”

That supports:

```text
account field changed
```

It does not independently establish:

```text
verified romantic relationship
cohabitation
engagement
legal marriage
relationship duration
```

Suggested field:

```yaml
relationship_state_source: self_reported_account_field|platform_claim|independent_record
```

Never silently upgrade self-reported platform status to demographic marriage data.

---

## 16. 2019 counterexample: online discovery often stops before meeting

A 2019 China Youth Daily report provides contemporaneous individual evidence that users combined family introductions, alumni activities, matchmaking corners, dating platforms and platform-hosted offline events.

Source:

- https://news.cctv.com/2019/09/19/ARTIQcf3Z3b8CgW5Ga4UmfT4190919.shtml

This is outside the core old-web period but useful as a boundary check on outcome inference.

One interviewee said the candidates she actually met were mostly introduced by other people; platform contacts often moved only to WeChat and occasional chat.

This demonstrates why an old profile/search archive cannot imply an in-person meeting.

Use this 2019 evidence as **later boundary evidence**, not as a reason to extend the repository's main scope beyond 2015.

---

## 17. 2020 boundary evidence: family mediation can migrate online

A 2020 China News report described parents who moved matchmaking activity into online communication and brought candidates into the same WeChat group for video conversation during pandemic restrictions.

Source:

- https://www.chinanews.com/sh/2020/03-13/9123765.shtml

Again, this is post-scope comparison only.

Archaeological implication for earlier platforms:

> `digital dating` and `family-mediated dating` are not mutually exclusive categories.

A platform may supply discovery while relatives coordinate the next step elsewhere.

---

## 18. Profile staleness gap

Historical dating profiles are especially vulnerable to temporal misreading.

Possible state chain:

```text
profile created
→ user actively searching
→ user stops logging in
→ user begins relationship elsewhere
→ profile remains visible
→ search index remains stale
→ archive captures profile months/years later
```

An archive capture date is **not** necessarily the date the profile content was current.

Record separately when observable:

```yaml
profile_created_at:
profile_last_updated_at:
last_login_label:
archive_capture_datetime:
relationship_status_at_capture:
```

Do not infer missing values.

---

## 19. Dynamic-age / derived-field caution

Some dating systems may store birth year/date and render current age dynamically; others may store an age value directly.

Without a verified historical capture and code/backend evidence, do **not** assume which model a platform used.

Potential archaeology problem:

- archived HTML stores rendered age;
- JavaScript calculates age at runtime;
- archive replay executes modern date logic;
- current platform re-renders old data through new templates.

Any claim that “this archived profile showed age X to users in year Y” needs capture-specific evidence.

This is a hypothesis-driven caution, not a claim about a specific Jiayuan implementation.

---

## 20. Search URL / private-query gap

Search pages may depend on:

- POST bodies;
- authenticated cookies;
- session IDs;
- opaque user IDs;
- server-side stored preferences;
- pagination tokens;
- ranking state.

Therefore a saved URL such as:

```text
/search?...filters...
```

may not reproduce the historical result set even when HTML shell survives.

Required evidence distinction:

```text
search form capture
≠ submitted query capture
≠ result-set capture
≠ same ranking on replay
```

---

## 21. Web/mobile divergence gap

By the later part of the repository period, dating services could have:

- desktop Web;
- mobile Web;
- SMS/mobile-carrier services;
- native apps;
- public-account integrations;
- offline events.

Do not treat one interface as the platform.

If a 2013 desktop capture lacks a feature, the feature may still have existed in a mobile product—and vice versa.

Required fields:

```yaml
surface: desktop_web|mobile_web|app|sms|offline_event
account_namespace_shared:
profile_store_shared:
message_store_shared:
feature_parity_known:
```

---

## 22. Offline-event state gap

The Jiayuan F-1 says the company organized hundreds of offline social gatherings and reports 864 events in 105 cities in 2010.

This is A-grade evidence for the company's formal event claim, not for every attendee outcome.

State chain:

```text
event listing exists
→ registration opens
→ user registers
→ payment/qualification if any
→ attendance slot confirmed
→ person travels to venue
→ checks in
→ attends event
→ talks to candidate
→ contact information exchanged
→ later communication
```

An archived event listing proves almost none of the later states.

---

## 23. Success-story selection gap

Dating platforms have a structural incentive to publish successful couples.

A success-story page can prove:

- platform published the story at that date;
- the story contained particular claims;
- perhaps the named subjects consented to publicity, if documented.

It cannot establish:

- platform-wide success rate;
- typical time to relationship;
- typical user experience;
- representative demographics.

Do not use success-story archives as denominator-free outcome statistics.

---

## 24. Privacy / dignity stop condition

Dating profiles are among the worst candidates for indiscriminate old-web republishing because they may expose:

- photographs;
- age/birth information;
- location;
- income;
- education/employer clues;
- relationship status;
- sexual/relationship preferences;
- contact information;
- family expectations.

Repository rule for this domain:

1. prefer platform help pages, SEC/company filings, manuals and contemporaneous media;
2. model URL/profile structure abstractly;
3. do not bulk republish ordinary-user profiles;
4. do not resurrect deleted contact details;
5. if a personal capture is indispensable, retain only the minimum field necessary to support a technical claim;
6. do not create a searchable dataset of historical dating identities.

A capture being publicly retrievable is not sufficient ethical justification for republishing it.

---

## 25. Archive capture target checklist

For a future verified 2003–2008 Chinese dating-site capture, record:

```yaml
platform:
original_url:
capture_url:
capture_datetime:
page_type: landing|register|profile|search_form|search_results|message_help|pricing|verification_help
login_required:
charset:
content_type:
frames_or_iframes:
javascript_dependencies:
flash_or_plugin:
form_method:
form_action:
search_field_names:
query_parameters:
profile_identifier_shape:
ranking_text_visible:
promotion_text_visible:
verification_markers_visible:
message_payment_text_visible:
subresources_missing:
archive_rewrite_effects:
privacy_redactions_required:
evidence_grade:
confidence:
```

Never guess blank fields.

---

## 26. Negative result from this round

This round found strong contemporaneous product/business evidence in the 2011 SEC filing and strong contemporaneous user-operation evidence in 2008 media reporting.

It did **not** obtain and verify a replayable 2003–2006 Jiayuan archive capture with enough preserved structure to establish:

- DOM;
- historical charset;
- exact search field names;
- query endpoint;
- message endpoint;
- login/session mechanics;
- CSS/JS dependencies.

A search-engine locator for Wayback is not treated as a verified capture under `docs/METHOD.md`.

Therefore those technical details remain unknown rather than reconstructed from later pages.

---

## 27. What is established / likely / unknown

### Established

- by 2008, contemporaneous reporting shows structured partner-search fields and user-directed filtering on a Chinese marriage/dating site;
- Jiayuan's 2011 F-1 formally documents account/search/message-readability/payment/verification/ranking/offline-event states;
- account counts and active-account counts use distinct platform definitions;
- paid visibility can alter search exposure;
- on-platform exchanges can intentionally hand off to private contact channels;
- relationship-status changes are platform account states, not independent legal relationship records.

### High probability / reasonable inference

- public archives systematically overrepresent the discover/search stage and underrepresent real-world relationship outcomes;
- archived dating profiles have high staleness risk;
- historical reconstruction needs separate account, profile, search-index and message objects.

### Unknown

- exact 2003–2006 Jiayuan interface implementation;
- exact historical search ranking algorithm;
- per-profile verification procedure at every date;
- how many search hits led to messages, meetings or relationships;
- which off-platform channel was dominant for each cohort/year without additional evidence.

---

## 28. Cross-repository interpretation

The companion `how-people-lived` note uses these state gaps to ask a life-history question:

> When did an ordinary person gain the practical ability to treat unknown people outside their inherited social circle as searchable potential partners?

This repository contributes a narrower answer:

> Chinese dating websites made that search technically legible, but the public Web preserves the candidate-discovery layer far better than the trust, private communication, meeting and relationship layers that actually changed a life.

---

## 29. Next bounded archaeology task

Do **not** collect hundreds of personal profiles.

Highest-value next target is one verified 2003–2008 public platform/help/search capture with:

- exact archive datetime;
- charset;
- form fields;
- search action;
- ranking/promotion language;
- verification language;
- message/paywall language;
- missing-resource inventory.

A second independent family should be a contemporaneous user tutorial, product review or formal platform document.

If authentication, robots or privacy boundaries prevent reliable reconstruction, record that boundary as the result instead of rebuilding a fictional interface.
