# 中文网上纪念、逝者身份与身后页面状态缺口（2000–2015）

Status: methodology / research note  
Scope: Chinese Web, approximately 2000–2015. This note studies online memorial / virtual-cemetery services and the archaeological problem of posthumous identity. It does **not** turn this repository into a general history of death, inheritance, or global social-media memorialization. Later platform rules are used only to expose state distinctions that earlier evidence leaves unresolved; they must not be back-projected into 2000s services.

Privacy rule: do not rediscover, aggregate, mirror, or republish ordinary deceased users' photographs, real names, family relations, contact details, guestbooks, private messages, medical histories, or memorial-page contents merely because an archive still exposes them. Prefer service-level documentation, contemporary press, institutional memorials, public figures, and abstract state models.

---

## 1. Why online memorials belong in old-Web archaeology

A historical memorial page looks deceptively simple:

```text
name
photo
biography
guestbook
virtual flower/candle/incense
```

But the page is the visible endpoint of several different systems:

- a real person's death;
- a living requester / memorial creator;
- a service account;
- claims about the deceased person's identity;
- uploaded photographs and biographical text;
- comments written by later visitors;
- virtual-offering interactions;
- moderation and permissions;
- possible payment or renewal state;
- domain, hosting, database, image and script survival;
- archive capture.

Therefore:

> **memorial page ≠ deceased person ≠ memorial creator ≠ authoritative biography ≠ preserved archive artifact.**

The purpose of this note is to prevent those layers from being collapsed.

---

# 2. 2001: Chinese Web already had a recognizable virtual-cemetery category

A 2001-03-26 *Beijing Evening News* information page, reproduced by Sina Technology, listed multiple Chinese virtual-cemetery / online memorial services, including 网同纪念、华夏宇宙祭奠园、清明网、地球村网上公墓、中华清明网 and 英特公墓.

Source family B — near-contemporary press:

- https://tech.sina.com.cn/i/c/59673.shtml

The article is useful because it describes service capabilities rather than merely saying that “online memorials existed.” It mentions combinations of:

- applying for an online grave / memorial space;
- photographs and biographical material;
- online obituaries;
- memorial articles;
- discussion / message functions;
- online ritual actions.

### Narrow claim allowed

By early 2001, a Chinese Web user could encounter a recognizable category of services that turned memorialization into a Web-addressable activity.

### Claims not allowed

This source does not establish:

- national adoption rate;
- number of active memorials on each site;
- whether free registration was actually completed successfully by ordinary users;
- historical DOM / CSS / form fields;
- browser compatibility;
- charset;
- backend database model;
- long-term survival of a created memorial.

The current run did **not** verify a surviving 2001 WARC / Wayback capture for a representative ordinary memorial page. Therefore these technical states remain unresolved.

---

# 3. The first crucial distinction: service exists ≠ ordinary families use it

A 2004 Chongqing report provides unusually valuable negative evidence. One cemetery had offered online memorial services for roughly a year but reportedly had only 12 ordinary citizens create memorials; another funeral institution had begun a similar service in 2001 but attracted almost no use and later cancelled it.

Source family B — contemporary negative evidence:

- https://news.sohu.com/2004/03/25/99/news219599967.shtml

This supports a basic archaeology / ordinary-life ladder:

```text
service advertised
→ service reachable
→ person knows service exists
→ person accepts online memorialization
→ person creates memorial
→ relatives/friends return to it
→ use becomes routine
```

Do not jump from the first node to the last.

This negative evidence is important because later nostalgia can make early Web practices look more socially established than they were.

---

# 4. 2004: online memorials can be attached to a physical cemetery relationship

A 2004 report on 合肥大蜀山文化陵园 described cooperation with 网同纪念 to provide an online memorial garden for cemetery customers. The reported functions included creating a memorial under the deceased person's name, photographs, memorial writing, flowers and candles.

Source family B:

- https://news.sina.com.cn/c/2004-03-30/02152172262s.shtml

This creates an important entity distinction:

```text
physical cemetery record
≠ online memorial service account
≠ memorial page
```

A page may be associated with a real cemetery customer without being the authoritative cemetery record.

Likewise, a virtual memorial may exist with no corresponding grave relationship at all.

Therefore a future dataset should not silently encode:

```yaml
memorial_url: ...
physical_grave_verified: true
```

unless independent evidence actually verifies that relation.

---

# 5. 2007: the memorial page becomes a multi-author memory container

Contemporary reporting in 2007 described online memorial services with interactive ritual actions such as flowers, candles, incense, tea or wine.

Source family B:

- Xinhua / Sina Technology, 2007-04-03:
  https://tech.sina.com.cn/i/2007-04-03/10221446100.shtml

Another 2007 report described memorial pages carrying photographs, life stories, audio/video, lists or networks of relatives/friends, messages and memorial writing.

- Hainan Daily / Sohu, 2007-04-06:
  https://news.sohu.com/20070406/n249239764.shtml

These sources motivate a stronger state model than “static obituary page.”

A memorial page may contain contributions from:

- the person who created the memorial;
- family members;
- friends;
- classmates / colleagues;
- anonymous visitors;
- platform templates or automatically generated content.

Thus:

> **content displayed under the deceased person's page is not automatically authored by, approved by, or historically known to the deceased person.**

This is the **visitor-authorship gap**.

---

# 6. 2008: a memorial URL can coordinate geographically dispersed grief

A 2008 *Nandu Weekly* report described a 27-year-old Guangzhou man who created an online memorial after his younger sister died of cancer. The account is useful because it records a concrete use rather than service marketing: classmates and friends living elsewhere could participate remotely; the report also notes that the memorial was an unusual online context in which he was willing to use real names rather than his normal pseudonymous style.

Source family B + contemporaneous testimony:

- https://news.sina.com.cn/c/2008-04-09/164415322655.shtml

### What this may support

- online memorials could reduce geographic coordination cost;
- a memorial URL could become a shared address for dispersed relations;
- memorial contexts could encourage different identity practices from ordinary pseudonymous Web participation.

### What it cannot support

- general prevalence;
- authenticity of every contributor identity;
- actual return frequency of all friends;
- platform retention guarantees;
- whether the memorial still survives today.

For ordinary-life work this is useful as **grief coordination infrastructure**; for this repository it is a reminder that a page can be socially active without exposing the full relationship graph to archives.

---

# 7. Two different posthumous-Web architectures must not be mixed

## Architecture A — memorial created after death

Typical early virtual-cemetery pattern:

```text
person dies
→ living requester chooses memorial service
→ requester opens account / submits material
→ memorial page created
→ other visitors discover page
→ messages / virtual offerings / edits accumulate
```

## Architecture B — a pre-existing living-person account survives the person

Later SNS problem:

```text
living user already has account + content + social graph
→ person dies
→ platform may not know
→ account continues under normal state
→ someone reports death
→ platform verifies or rejects claim
→ account becomes protected / memorialized / frozen / removed / unchanged
```

Architecture B is conceptually important to understand posthumous identity, but this note does **not** use post-2015 platform policies to claim that early Chinese memorial services had equivalent states.

The two architectures preserve different things:

| Created memorial | Pre-existing account |
|---|---|
| posthumous biography assembled by survivors | person's own pre-death activity residue |
| creator chooses what enters page | pre-existing private/public visibility rules |
| memorial identity begins after death | account identity predates death |
| visitors are expected to post memorial content | ordinary social interactions may continue accidentally |
| subject and account operator are normally different | subject and operator were originally same person |

---

# 8. Core state machine for early Chinese online memorials

A useful minimum model is:

```text
real-world death
→ requester discovers service
→ requester registers / contacts service
→ requester supplies deceased identity claim
→ service accepts / does not verify / verifies some fields
→ memorial object created
→ public URL assigned
→ biography/media uploaded
→ visibility/search state
→ visitor arrives
→ visitor identity / anonymous state
→ message or virtual offering submitted
→ moderation / display state
→ optional payment / renewal / premium state
→ ongoing editing / caretaker state
→ inactive / abandoned / deleted / migrated state
→ platform/domain/backend survival
→ archive capture or non-capture
```

Every arrow can fail independently.

A historical screenshot of the final page does not prove the earlier states.

---

# 9. Deceased-identity verification gap

Early press descriptions frequently talk about creating a memorial under a deceased person's name, but the current evidence does not establish one uniform historical identity-verification contract.

Possible states include:

```text
free-text name only
family assertion
cemetery-linked customer relation
submission of documents
manual moderation
no meaningful verification
unknown
```

Therefore:

> **a memorial page claiming to represent person X is evidence that the page made that claim, not automatically proof of X's legal identity, dates, kin relations, employment history, or cause of death.**

For historical research, biography text inside an ordinary memorial page should usually be treated as family/community testimony unless independently corroborated.

---

# 10. Memorial-subject / creator gap

The central identity relation is:

```text
memorial subject ≠ memorial creator
```

A creator may be:

- spouse;
- parent;
- child;
- sibling;
- classmate;
- colleague;
- cemetery operator;
- organization;
- fan / admirer;
- unknown platform user.

This matters because permissions and historical claims depend on who created the page.

A memorial for a public figure created by an admirer is not equivalent to a family-authorized archive.

A cemetery-created page may reflect customer data but not family-authored biography.

The repository should record `creator_relation_status` separately from `subject_identity_status` whenever evidence supports it.

---

# 11. Requester-authority gap

A memorial service can technically allow a page to be created without resolving who has social, family or legal authority to represent the deceased.

Possible questions:

- Can two relatives create competing memorials?
- Can a classmate create a page before the family?
- Who can delete it?
- Who can edit biography fields?
- Who can remove an offensive message?
- What happens if family members disagree?

Current sources do not fully resolve these states for early services.

Do not infer a modern “legacy contact” model backward.

---

# 12. Virtual-offering transaction gap

Contemporary sources describe interactions such as:

- flowers;
- candles;
- incense;
- tea;
- wine;
- other ritual animations.

But a screenshot of a flower icon does not tell us whether the historical action was:

- free;
- rate-limited;
- account-gated;
- paid;
- recorded permanently;
- recorded only as a counter;
- rendered with image / JavaScript / Flash;
- later migrated to another implementation.

Thus:

> **visible offering ≠ known transaction state.**

Where money was involved, price/payment/renewal must be independently sourced.

---

# 13. “Permanent memorial” is a service claim, not an archival fact

Online memorial services often market themselves using concepts such as permanent remembrance or memory that will not be erased.

For Web archaeology this language must be normalized as:

```text
service promised persistence
```

not:

```text
artifact has permanent persistence
```

Actual persistence depends on:

- domain ownership;
- company survival;
- database migration;
- hosting bills;
- image storage;
- script/runtime compatibility;
- account/payment status;
- moderation policy;
- family deletion requests;
- archive crawling.

This creates a **posthumous persistence gap**.

A person can die once biologically and then effectively “disappear again” when the memorial platform or database disappears.

---

# 14. HTML survival is not memorial survival

A historical memorial service can fail in several distinct ways:

```text
host survives, individual page 404s
HTML survives, images missing
page shell survives, database content missing
page survives, guestbook endpoint dead
page survives, JavaScript/Flash ritual controls dead
main document archived, forms/POST actions unavailable
search index survives, destination page missing
page copied to archive, later edits absent
```

Therefore a future capture record should distinguish:

```yaml
main_html_survives:
profile_text_survives:
images_survive:
media_survives:
guestbook_entries_survive:
interactive_offerings_survive:
form_submission_replayable:
search_discoverability_survives:
```

Do not call a memorial “preserved” merely because its shell loads.

---

# 15. Search and discoverability matter for posthumous identity

A memorial URL can exist without being easily discoverable.

Possible discovery routes include:

- direct link sent by family;
- platform search by deceased name;
- cemetery index;
- search-engine indexing;
- category / recent memorial listing;
- external blog/forum links.

Each route creates a different historical visibility pattern.

A public search result may preserve only:

```text
name + title + snippet + URL
```

while the page itself is already gone.

This produces a **posthumous discoverability gap**: the archive may preserve evidence that a memorial once existed without preserving the memorial itself.

---

# 16. Visitor identity is especially fragile historical evidence

Guestbooks and memorial messages are tempting life-history sources because they can reveal:

- kinship;
- school/work relations;
- nicknames;
- migration;
- shared experiences;
- anniversaries;
- later family events.

But they are also among the most ethically sensitive ordinary-person materials.

A historical visitor name may be:

- real name;
- pseudonym;
- relation label (“姐姐”, “同学”);
- shared account;
- anonymous guest;
- platform display name changed later.

Therefore:

> **display name ≠ verified historical person.**

Do not use memorial guestbooks as a convenient dataset for rebuilding private social graphs.

---

# 17. Later deceased-account rules expose an important state distinction, but cannot be back-projected

In 2020, Weibo publicly described a deceased-account protection mechanism and explicitly distinguished a confirmed deceased account from an account that was merely long inactive. The platform said it had been building such mechanisms since 2017 and used news, relatives' feedback and manual identification rather than treating inactivity itself as death.

After-scope methodological source:

- CNR, 2020-09-18:
  https://china.cnr.cn/xwygd/20200918/t20200918_525267714.shtml

This later source is valuable only for the following general distinction:

```text
inactive account
≠ deceased account
```

and:

```text
owner deceased
≠ platform aware of death
```

It must **not** be cited as evidence that 2000–2015 memorial sites or SNS products had the same workflow.

For in-scope 2009–2015 SNS archaeology, the correct next task is to find contemporaneous Chinese platform help pages / terms / reports describing what actually happened to deceased users' existing accounts.

---

# 18. Algorithmic afterlife is a later problem that old-Web archaeology should anticipate carefully

Once platforms generate:

- birthday reminders;
- “people you may know”;
- reconnect prompts;
- game invitations;
- anniversary resurfacing;
- automated photo memories;

an unrecorded death can make the platform continue treating a person as alive.

Facebook's 2009 memorialization change is a useful overseas contemporary comparison because reports explicitly connected memorialization to preventing deceased users from being surfaced in ordinary social prompts.

Overseas comparison, not part of Chinese-site scope:

- *The Guardian*, 2009-10-27:
  https://www.theguardian.com/technology/2009/oct/27/facebook-user-memorials
- AP / MPR, 2009-10-27:
  https://www.mprnews.org/story/2009/10/27/facebook-dead-user-profiles

This proves that the **pre-existing account after death** problem was technically real by 2009 outside China.

It does not prove equivalent Chinese product behavior.

---

# 19. Relationship to ordinary-life history

This repository should not become a general sociology-of-death project, but these Web states matter because they change what survives of an ordinary life.

A person who left little public record before death may acquire, after death:

- a biography page;
- photographs;
- family-written chronology;
- classmates' messages;
- work memories;
- a publicly searchable name.

This is **posthumous addressability**.

But archive ethics require restraint:

> The fact that death made someone historically visible does not grant historians unlimited permission to re-publish them.

The correct contribution to `how-people-lived` is the social mechanism; the correct contribution here is the platform/provenance/state model.

---

# 20. Evidence grades for this slice

## B — contemporary / near-contemporary press

- 2001 virtual-cemetery service list and function descriptions;
- 2004 physical cemetery + online memorial cooperation;
- 2004 low-adoption counterexample;
- 2007 interactive memorial service descriptions;
- 2008 first-person use case.

These support service existence, represented features and some use practices.

## C — later service self-history

Current services describing their own early founding/history can generate leads but should not independently establish exact historical implementation.

## D — research state model

Terms such as:

- `posthumous addressability`;
- `memorial-subject / creator gap`;
- `requester-authority gap`;
- `posthumous persistence gap`;
- `algorithmic afterlife`;

are analytical constructs, not historical terminology used by early sites.

---

# 21. Negative result from this run

The current run found strong contemporaneous service-level and press evidence but did **not** obtain and verify a privacy-safe, technically complete ordinary-user historical capture from 2001–2008 showing all of the following:

- original URL;
- capture datetime;
- historical HTML;
- charset / Content-Type;
- browser requirements;
- account state;
- memorial creator state;
- moderation state;
- uploaded image/resource survival;
- guestbook backend;
- virtual-offering submission behavior;
- payment/renewal state.

Therefore this note does not reconstruct early Netor or other memorial-site DOM/CSS/UI and does not claim a particular IE/GBK/Flash environment without direct evidence.

“Unable to recover the authenticated / database state” is the correct result for now.

---

# 22. Privacy and dignity stop conditions

Stop investigation when progress would require:

- bulk harvesting ordinary deceased people's names/photos;
- redisclosing family members' contact details;
- reconstructing medical or cause-of-death details not necessary to the Web claim;
- linking memorial identities to modern private social-media accounts;
- contacting surviving relatives;
- bypassing access controls;
- reproducing full copyrighted photo/video collections;
- using a still-indexed deleted memorial as justification to republish it.

For a browser/charset/capture study, prefer:

1. platform help pages;
2. institutional memorials;
3. public figures where privacy risk is low;
4. synthetic fixtures derived from documented historical structure, clearly labelled reconstruction.

---

# 23. Suggested archaeology state schema

```yaml
object_type: online_memorial
service:
original_url:
capture_url:
capture_datetime:
memorial_subject:
  identity_status: unknown|asserted|institutionally-linked|verified
creator:
  identity_status: unknown|account-visible|verified
  relation_to_subject: unknown
creation_time_known: false
physical_cemetery_link:
  status: none|claimed|verified|unknown
visibility:
  public: unknown
  searchable_by_name: unknown
  external_search_indexed: unknown
content:
  biography: unknown
  images: unknown
  audio_video: unknown
  guestbook: unknown
  virtual_offerings: unknown
interaction:
  login_required: unknown
  moderation_known: false
  payment_known: false
persistence:
  main_html: unknown
  database_fields: unknown
  images: unknown
  guestbook: unknown
  scripts_plugins: unknown
  current_service_continuity: unknown
browser_assumptions:
charset:
privacy_risk:
claim_supported:
claim_not_supported:
unknowns:
```

---

# 24. New state gaps established in this slice

- **deceased-identity verification gap** — a page's named subject is not automatically a legally verified person;
- **memorial-subject / creator gap** — the person represented is not the person operating the page;
- **requester-authority gap** — technical ability to create/edit does not establish family/legal authority;
- **physical-grave relation gap** — memorial URL and physical burial record are separate objects;
- **visitor-authorship gap** — content on the page can come from many contributors;
- **virtual-offering transaction gap** — visible ritual action does not reveal payment or persistence state;
- **moderation gap** — surviving comments do not reveal removed/rejected content;
- **discoverability gap** — page existence does not establish that a visitor could find it;
- **renewal/payment gap** — service promises of long-term persistence may depend on unpreserved account/payment state;
- **backend-survival gap** — HTML shell can outlive database content;
- **resource-survival gap** — images/video/scripts can disappear independently;
- **account-death-state gap** — a pre-existing account's owner can be dead while platform state remains “ordinary account”;
- **archive-capture gap** — a capture preserves one representation, not the full memorial lifecycle;
- **privacy redisclosure gap** — archival accessibility does not imply ethical republication.

---

# 25. Highest-value next step

Do not collect more lists of virtual-cemetery brands.

The highest-value bounded archaeology target is:

> **one privacy-safe, verifiable Chinese memorial-service case across at least two historical timepoints.**

Prefer an institutional/public-figure memorial or a platform help/demo page rather than an ordinary family memorial.

For that case, verify:

1. original URL and capture datetime;
2. historical charset and Content-Type;
3. browser/JS/Flash assumptions;
4. whether image resources survive;
5. whether guestbook / offerings were separate endpoints;
6. whether search/index pages can still reach the memorial;
7. whether current service continuity represents migration or a new implementation;
8. which states remain fundamentally unrecoverable.

That would turn this state model into a real old-Web archaeological case without violating the dignity of ordinary deceased users.

---

## Sources consulted in this slice

- 北京晚报 / 新浪，2001-03-26，国内虚拟墓地资料：https://tech.sina.com.cn/i/c/59673.shtml
- 重庆晚报 / 搜狐，2004-03-25，低采用负例：https://news.sohu.com/2004/03/25/99/news219599967.shtml
- 江淮晨报 / 新浪，2004-03-30，实体陵园与网上纪念合作：https://news.sina.com.cn/c/2004-03-30/02152172262s.shtml
- 新华 / 新浪科技，2007-04-03，网上祭奠交互：https://tech.sina.com.cn/i/2007-04-03/10221446100.shtml
- 海南日报 / 搜狐，2007-04-06，网上纪念内容形态：https://news.sohu.com/20070406/n249239764.shtml
- 南都周刊 / 新浪，2008-04-09，第一人称使用：https://news.sina.com.cn/c/2008-04-09/164415322655.shtml
- 央广网，2020-09-18，微博逝者账号保护（仅作 after-scope 状态边界）：https://china.cnr.cn/xwygd/20200918/t20200918_525267714.shtml
- Guardian, 2009-10-27, Facebook memorialization overseas comparison：https://www.theguardian.com/technology/2009/oct/27/facebook-user-memorials
