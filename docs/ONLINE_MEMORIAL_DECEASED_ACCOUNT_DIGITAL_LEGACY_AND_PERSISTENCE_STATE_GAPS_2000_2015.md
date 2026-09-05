# Online memorials, deceased accounts, digital legacy, and persistence state gaps on the Chinese old Web (2000–2015)

Status: research note, **not** an M1 complete reconstruction case.

Cross-repository context:

- life-history synthesis: `tmzncty/how-people-lived/topics/posthumous-administrative-closure-digital-remains-and-memory-persistence-china-1958-2026.zh-CN.md`

This note stays inside the repository's approximately 1995–2015 Chinese-Web scope. It does not turn the repository into a global digital-death history. Later platform policies such as 2020 Weibo/Bilibili deceased-account states belong in the cross-repository life-history synthesis, not as old-Web artifact evidence here.

---

## 1. Research question

Death creates an unusually difficult old-Web archaeology problem because a surviving page can describe several different states that must not be collapsed:

```text
real person
→ real death
→ someone knows / reports the death
→ memorial page or existing account remains online
→ platform may or may not know the user is deceased
→ family may or may not control credentials
→ public content may remain visible
→ service may migrate / close / expire
→ archive capture
```

Hard rules:

- `real death ≠ platform-verified death`
- `memorial page exists ≠ deceased consented to it`
- `memorial creator ≠ legal next of kin`
- `account inactive ≠ account holder deceased`
- `last login ≠ date of death`
- `relative ≠ authenticated account holder`
- `death certificate ≠ password entitlement`
- `content value ≠ transferable account control`
- `service promise of permanence ≠ durable preservation`
- `public memorial ≠ permission to republish sensitive family material`
- `archive capture ≠ the live platform state at that date`

The archaeological question is therefore not simply “did Chinese people mourn online?” It is:

> **Which state did a page represent, which states were private or off-platform, and what exactly survives when the platform itself becomes an archaeological object?**

---

## 2. Two objects that must not be merged

There are at least two different old-Web systems.

### Object A — purpose-built online memorial

```text
death
→ relative/friend chooses memorial service
→ registers / pays / enters deceased metadata
→ memorial page created
→ photos/text/virtual offerings added
→ visitors encounter page
→ comments/tributes accumulate
→ subscription/domain/platform continues or fails
→ archive capture
```

### Object B — an ordinary account whose user later dies

```text
user creates QQ/email/blog/forum account while alive
→ account accumulates content and relationships
→ user dies
→ credentials remain as they were
→ family wants access / preservation / deletion
→ platform terms and authentication rules apply
→ account remains, freezes, expires, is recovered, or is lost
→ public surface may continue independently
```

A 2004 Netor memorial page and a 2011 deceased user's QQ account are **not the same class of artifact**.

The first was created after death for memorialization. The second was a living person's private/public communication environment that unexpectedly became a posthumous object.

---

## 3. 2003: online memorialization was already a visible Chinese-Web practice

A 2003 *Beijing Evening News* report preserved by Sina described “digital memorial” practices around Qingming. It reported that a worker in Fuzhou used SMS to send virtual flowers to a memorial page, and that the memorial provider Netor/“网同” said its service had operated for more than three years. The provider claimed about 20,000 memorial halls for ordinary people and more than 100,000 average daily visits. The report also described the trial “八宝山在线” service and server-capacity pressure.[1]

Evidence role:

- strong contemporaneous secondary evidence that such services and routines existed;
- participant/vendor claims for scale;
- **not** evidence for unique-user counts;
- **not** a verified capture of Netor's 2003 DOM;
- **not** evidence that online memorialization was socially normal across China.

Minimum reconstruction:

```text
Chinese Web memorial services existed by 2003
ordinary-person memorial pages were a product category
SMS/Web could be linked to virtual offerings
server capacity mattered to the user-visible service
```

Not allowed:

```text
20,000 memorial pages = 20,000 independent deceased people
100,000 visits = 100,000 unique mourners
reported feature X = verified historical DOM element
```

---

## 4. 2004 Netor / Dashushan: a useful candidate locator, not yet a verified M1 capture

A 2004 *Jianghuai Morning News* report preserved by Sina gave explicit candidate URLs for the Dashushan memorial park and Netor. It described functions including candles/music, virtual flowers/wine, photo albums and memorial writings. It also used marketing language promising “permanent preservation” and effectively unlimited expansion.[2]

Candidate original URLs from the contemporaneous report include:

```text
http://www.dashushan.netor.com
http://www.netor.com
```

These are valuable **locators**.

They are not automatically historical captures.

A future M1-level investigation must obtain and actually inspect an archive object with, where available:

- archive provider;
- archive URL;
- original URL;
- capture datetime;
- HTTP status;
- content type;
- charset;
- DOM/form structure;
- referenced image/media assets;
- login/payment dependencies;
- whether the page is a live memorial, landing page, or later redirect.

Until then:

`contemporaneous URL citation ≠ verified archived page`.

---

## 5. “Permanent” is a platform state claim, not an archaeological fact

Online memorial products are especially prone to a semantic trap.

A service can advertise:

```text
permanent memorial
permanent storage
unlimited expansion
365-day access
```

But technical persistence requires a chain:

```text
company/institution survives
→ domain remains controlled
→ DNS resolves
→ hosting continues
→ database remains intact
→ storage remains intact
→ application still runs or data is migrated
→ account/payment state still authorizes access
→ old URLs redirect or remain stable
```

Therefore:

> **“永久保存” in a 2004 article is evidence of a historical service promise and future imagination, not proof that the user's data actually persisted permanently.**

Call this the **platform-mortality gap**.

It is particularly important for memorial sites because the product itself asks users to trust the platform with a time horizon potentially longer than the customer, the creator, or the original software stack.

---

## 6. 2008: contemporaneous users explicitly worried about platform disappearance

A 2008 *China Youth Daily* report on online grave-sweeping recorded a consumer concern that can be paraphrased as: after paying, what happens if the webpage suddenly disappears and there is nobody to pursue?[3]

The same report said online memorial services were not yet the mainstream Qingming route and discussed annual fees, maintenance fees and virtual-offering charges.

This is unusually valuable because it supplies a **contemporaneous user-side durability model**:

```text
payment
→ memorial page exists today
→ expected future access
→ platform/provider persistence
→ consumer remedy if service disappears
```

The user was already reasoning about a state gap that Web archaeology later encounters directly:

`paid memorial ≠ durable memorial`.

Do not turn this into a universal attitude. The report gives a real contemporary concern, not a nationally representative survey.

---

## 7. Memorial-page creation has identity gaps of its own

A memorial service may ask for the deceased person's:

- name;
- dates;
- biography;
- photograph;
- relationship to creator;
- cemetery/plot information;
- creator account;
- payment.

But without a verified historical form and validation policy, do not infer what was required in a particular year.

Possible states:

```text
real death
→ creator assertion
→ memorial service accepts metadata
→ public page appears
```

This does **not** necessarily imply:

```text
civil death certificate checked
kinship checked
deceased identity uniquely resolved
creator had exclusive right to publish the material
```

Hard boundaries:

- `page says person P died ≠ civil registry verification`
- `creator says “father/mother/spouse” ≠ relationship independently verified`
- `photo uploaded ≠ copyright/privacy clearance established`
- `memorial page created ≠ deceased had requested memorialization`

This is the **memorial-assertion / civil-state gap**.

---

## 8. Virtual offering state must not be confused with ritual outcome

A memorial page might show actions such as:

```text
献花
点烛
上香
祭酒
留言
点歌
```

For archaeology, record the platform state precisely.

Potentially observable:

```text
button/link existed
page displayed offering O
visible counter changed
transaction confirmation page existed
```

Usually not observable from a static capture:

```text
who actually clicked
whether payment cleared
whether one person clicked repeatedly
whether the family considered the action meaningful
whether the user also visited a physical grave
```

Thus:

`virtual offering visible ≠ physical ritual replaced`.

`online memorial use ≠ abandonment of offline mourning`.

---

## 9. 2011 QQ dispute: deceased-account archaeology is a credential problem

A 2011 *News Evening* report preserved by Sina described a dispute in which a widow wanted access to her deceased husband's QQ because it contained photographs and messages from their life together. The report contrasted her claim with Tencent's service terms concerning the QQ number and user rights.[4]

For old-Web archaeology, this is much more than a legal-interest story. It reveals a state chain:

```text
real person
→ QQ identifier
→ authentication secret
→ mailbox/messages/photos
→ real death
→ spouse knows death and relationship
→ spouse does not necessarily know credential
→ platform has account record
→ platform terms govern recovery/control
```

At least four objects must stay separate:

```text
identifier
credential
content
property/economic value
```

Hard rules:

- `QQ number ≠ password`
- `password ≠ ownership of all content`
- `spousal relationship ≠ successful account authentication`
- `death certificate ≠ automatic credential disclosure`
- `content of emotional value ≠ transferable platform identity`
- `platform says number is not user-owned ≠ every digital item in account has identical legal status`

Call this the **account / content / credential split**.

---

## 10. An account can outlive the person without becoming a memorial

In old-Web captures a profile may remain publicly reachable after the user has died.

Possible explanations include:

- platform did not know;
- nobody requested closure;
- account was intentionally preserved;
- account became inaccessible but public profile remained;
- login credentials remained with a family member;
- the user was not actually deceased and the inference is wrong;
- the captured page predates the death;
- a later archive replay gives a misleading impression of continuity.

Therefore:

`public profile after date D ≠ user was alive after D`.

and:

`no later posts ≠ user died at last-post date`.

This is the **last-activity / life-status gap**.

A user's death date should never be inferred solely from platform silence.

---

## 11. Family access leaves very little public evidence

The most important posthumous operations are commonly private:

```text
password search
phone/SIM recovery
email password reset
platform support ticket
death certificate submission
relationship proof
export/download
private message access
account deletion request
billing cancellation
```

These are exactly the states a public web archive is least likely to preserve.

Call this **public-memorial-shell / private-credential-state asymmetry**.

The archive may keep:

- a memorial homepage;
- a public profile;
- a news report about account inheritance;
- terms of service;
- public condolences.

It will usually not keep:

- help-desk correspondence;
- uploaded death certificate;
- recovery answers;
- private mailbox state;
- login cookies;
- family authorization documents;
- deletion logs.

Do not fill the private half with inference.

---

## 12. Platform terms are versioned historical artifacts

The 2011 QQ dispute also warns against citing a current user agreement to prove a 2005 account rule.

A platform term can change independently of the interface.

Future archaeology should record:

```text
terms URL
visible revision date
capture datetime
account-registration date if independently known
relevant clause
whether acceptance was clickwrap/browsewrap/unknown
```

Hard rule:

`current Tencent/Netor terms ≠ 2003/2011 terms`.

A contemporaneous newspaper quoting a term is useful evidence of what was being publicly asserted then, but is not a substitute for a captured full agreement if the exact legal state matters.

---

## 13. Memorial pages produce a distinctive archive survival bias

Death-related pages are unusually likely to be:

- linked by news stories;
- shared by many mourners;
- copied into other sites;
- revisited annually around Qingming/anniversaries;
- treated as culturally important by the platform.

This can create **memorial survival bias**.

A researcher may find many pages about deaths but very little about the same person's ordinary years.

Therefore:

> **The death page can become more archivally visible than the life it claims to summarize.**

Do not infer social importance from HTML survival.

Similarly:

- a heavily linked memorial may reflect a school/community/public event;
- an ordinary person's family may mourn intensely but never create a public URL;
- a private memorial may be blocked from crawling;
- a memorial may survive only as a media quotation.

---

## 14. Platform death creates a second-order archive problem

Online memorial systems are unusual because the service itself can die.

State chain:

```text
memorial created on platform A
→ platform A changes software/domain
→ content migrated / partly migrated / not migrated
→ old URL dies
→ current platform may re-render old data
→ archive captures only some versions
```

A present-day page containing a memorial created in 2004 may be:

- the original HTML preserved continuously;
- a later template rendering of old database records;
- a migrated page with new IDs;
- a manually recreated memorial;
- a redirect from an old URL;
- a third-party copy.

These are not equivalent.

For any candidate case record:

```text
record creation date
page template date
current rendering date
archive capture date
```

as separate clocks.

This is the **memorial-record / rendering-version gap**.

---

## 15. Search-engine discovery can re-contextualize grief

A memorial page may contain full names, dates, photographs, workplace/school information and relatives' messages.

At time t, family members may have expected the page to be found mainly by people who knew the URL.

At time t+10, search engines or archives can make fragments independently discoverable.

Thus:

`public at creation ≠ intended for unlimited future aggregation`.

Do not concatenate old memorial metadata to reconstruct private family networks unless the historical mechanism cannot be established otherwise.

Particularly avoid:

- home addresses;
- phone numbers;
- medical details;
- children's identities;
- private relationship conflicts;
- cross-platform re-identification.

---

## 16. “Digital legacy” should not be retroactively imposed on all old-Web behavior

Contemporaneous 2003–2008 Chinese sources usually used terms such as:

- 网上祭奠;
- 网上纪念馆;
- 数字化祭奠;
- 网上墓地.

The 2011 QQ dispute was framed as “网络遗产” in media discussion.

Do not rewrite 2003 users as if they were already operating with the 2020s conceptual bundle of:

```text
digital assets
digital estate
digital afterlife
digital immortality
```

Modern analytical terms are allowed, but original vocabulary should be retained near the evidence.

---

## 17. What a future M1 case would need

A robust online-memorial M1 case should ideally include at least two historical timepoints and two independent sources.

Minimum artifact set:

1. verified historical archive capture of landing/index page;
2. verified historical memorial-page capture;
3. contemporaneous press/service documentation;
4. where possible, terms/pricing/help page;
5. asset manifest for images/JS/CSS/media;
6. encoding/browser assumptions;
7. explicit unknowns for login/payment/private state.

Fields:

```text
archive_provider
archive_url
original_url
capture_datetime
http_status
content_type
charset
page_title
platform_name
memorial_id/url_shape
creator_auth_required = yes/no/unknown
payment_required = yes/no/unknown
relationship_verification = yes/no/unknown
death_verification = yes/no/unknown
media_dependencies
broken_assets
later_migration_evidence
```

An ordinary-profile-after-death case would need a different schema and must not rely on death inference from silence.

---

## 18. Negative result from this run

This run found strong contemporaneous **locators and descriptions**, especially:

```text
http://www.netor.com
http://www.dashushan.netor.com
```

but it did **not** obtain and actually inspect a Wayback/WARC object that satisfies the repository's M1 evidence contract for a 2000–2011 Chinese online memorial or deceased-account transaction.

Therefore the following remain **unknown** for the candidate historical pages unless a later verified capture establishes them:

- exact historical URL canonicalization;
- archive capture datetime;
- HTTP headers;
- charset;
- DOM;
- form action;
- login/session model;
- cookie behavior;
- payment callback state;
- memorial database schema;
- creator/death/kinship verification policy;
- deletion/export behavior;
- historical backup and migration implementation.

Do **not** mark M1 complete from the press reports alone.

---

## 19. Privacy and stop conditions

For deceased/private-user cases, stop if completing the reconstruction would require:

- password reset attempts;
- login attempts to an old account;
- using leaked credentials/databases;
- obtaining private messages without clear authorization;
- re-identifying a private person from old phone/email/school fragments;
- republishing sensitive grief, health or child information merely because a page once exposed it.

Death does not turn private data into unrestricted research material.

This repository should prefer platform-level mechanics and already-public institutional/journalistic descriptions over invasive reconstruction of a particular family's private account state.

---

## 20. Cross-repository consequence

The life-history repository asks how many practical life routes ordinary people possessed.

This old-Web case adds a final boundary:

> **A Web identity can remain technically present after the real person has died, while the family lacks the credentials, rights, or platform state needed to control it.**

For history, that means the Web does not merely preserve people. It preserves **partial states** of people.

Sometimes the visible page is a deliberate memorial.

Sometimes it is an abandoned living-person profile.

Sometimes it is a migrated database rendering.

Sometimes it is an archive copy of a service that promised permanence and later vanished.

Old-Web archaeology must determine which one it is before saying what survived.

---

## Sources

1. *北京晚报*, “短信、上网寄托哀思 今年流行‘数字化祭奠’”, 2003-04-04, preserved by Sina. https://tech.sina.com.cn/i/c/2003-04-04/1633175845.shtml
2. *江淮晨报*, “祭奠亲友可到网上纪念馆”, 2004-03-30, preserved by Sina. https://news.sina.com.cn/c/2004-03-30/02152172262s.shtml
3. *中国青年报*, “网上祭扫：说起来容易做起来难”, 2008-04-07. https://zqb.cyol.com/content/2008-04/07/content_2132646.htm
4. *新闻晚报*, “谁动了我的网络遗产”, 2011-10-21, preserved by Sina. https://tech.sina.com.cn/i/2011-10-21/13406211146.shtml

Later comparator, outside this note's archaeological time scope:

- Weibo deceased-account protection announcement, 2020-09-17, contemporaneous transcription: https://www.thepaper.cn/newsDetail_forward_9216910
- Bilibili memorial-account announcement, 2020-12-24, contemporaneous transcription: https://fashion.chinadaily.com.cn/a/202012/24/WS5fe4689fa3101e7ce973753c.html
