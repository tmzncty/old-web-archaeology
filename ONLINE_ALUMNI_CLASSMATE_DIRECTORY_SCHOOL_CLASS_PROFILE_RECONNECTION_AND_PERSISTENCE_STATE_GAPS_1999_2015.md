# Online alumni / classmate directory: school, class, profile, reconnection and persistence state gaps, 1999–2015

## Scope

This note studies a specific Chinese old-Web transaction family:

> **How did a user turn “we once went to school together” into an online route for finding, contacting and continuing to recognize another person?**

Primary scope stays within the repository boundary of roughly **1995–2015 Chinese Internet**. The main objects are:

- ChinaRen 校友录;
- 5460 中国同学录;
- school/class directory pages;
- class homepages;
- address books, guestbooks and class albums;
- login/account reuse;
- search/create-school/create-class flows;
- class membership and administrator roles;
- the transition from class-centric alumni directories to person-centric campus SNS;
- privacy leakage, impersonation and account-control gaps;
- page/service disappearance and the archiveability of relationship state.

Pre-Web paper alumni directories and overseas services belong mainly in the cross-repo life-history note and are used here only as boundary context.

Cross-repo companion:

- [`tmzncty/how-people-lived/topics/from-paper-classmate-books-to-searchable-past-alumni-directories-sns-and-social-recoverability-china-1955-2026.zh-CN.md`](https://github.com/tmzncty/how-people-lived/blob/main/topics/from-paper-classmate-books-to-searchable-past-alumni-directories-sns-and-social-recoverability-china-1955-2026.zh-CN.md)

---

## 1. Why “the alumni page existed” is not enough

For this object, the minimum state distinction is:

```text
PLATFORM_EXISTS
!=
SCHOOL_RECORD_EXISTS
!=
CLASS_RECORD_EXISTS
!=
PERSON_ACCOUNT_EXISTS
!=
PERSON_JOINED_CLASS
!=
PROFILE_DISCOVERABLE
!=
CONTACT_FIELD_VISIBLE
!=
MESSAGE_SENT
!=
MESSAGE_DELIVERED
!=
MESSAGE_READ
!=
PERSON_REPLIED
!=
RELATIONSHIP_REACTIVATED
```

A historical article saying “ChinaRen had a classmate directory” proves a much narrower fact than a historical class page proving one class existed.

A class page proves something narrower than a logged-in member directory.

A member directory proves something narrower than a successful message.

A successful message proves something narrower than an offline reunion.

Therefore this note explicitly forbids shortcuts such as:

> `class page exists -> old classmates were reunited`

or:

> `registered users -> active relationships`.

---

## 2. Research units

Following `docs/METHOD.md`, this topic uses separate units.

### platform

Examples:

- ChinaRen 校友录;
- 5460 中国同学录;
- 校内网 / 人人网 when used as the successor relation model.

### host / service surface

Known historical locators include:

- `www.chinaren.com`;
- `alumni.chinaren.com`;
- class subdomain patterns under `alumni.chinaren.com` described in a 2000 tutorial;
- `www.5460.net`.

A brand is not assumed to map to one stable host or one stable implementation across all years.

### school record

A platform object representing one school. It may be created by a user rather than imported from an authoritative education registry.

### class record

A platform object representing one cohort/class under a school.

### user account

A platform account or an account reused from another service, such as a Sohu/ChinaRen mail account in a 2004 tutorial.

### class membership edge

A relation between account and class. Its approval/verification semantics must not be guessed.

### person identity claim

The proposition that an account actually belongs to the former classmate the searcher remembers.

### contact field

Telephone, email, QQ, address or other field that may have its own visibility and freshness state.

### relationship outcome

A reply, later QQ/MSN/telephone contact, offline meeting, renewed friendship or no response.

### capture

A historical archived representation of any of the above page surfaces. It is not the same as the live backend state at capture time.

---

## 3. Evidence ledger

### E-01 — 2000 ChinaRen operational walkthrough

**Source:** 《生活时报》, 2000-07-21, “寻找回来的世界”.  
<https://www.gmw.cn/01shsb/2000-07/21/GB/07%5E1411%5E0%5ESH7-2123.htm>

**Grade:** B — contemporaneous media/tutorial evidence.  
**Confidence:** high for described user-visible functions; lower for adoption/popularity claims.

The article describes:

- entry from `www.chinaren.com`;
- region/country navigation;
- school keyword/category search;
- selecting an existing school and class;
- creating a school if absent;
- creating a class;
- assigning an English class name;
- a resulting class subdomain pattern under `alumni.chinaren.com`;
- platform registration and an ID;
- group mail;
- class guestbook;
- class album;
- class address book;
- class discussion area;
- class chat room;
- common links.

**What it proves:** a detailed 2000-era user-facing model existed and was publicly explained.

**What it does not prove:** historical HTML/DOM, charset, cookies, scripts, exact authorization checks, every class’s activity, or national adoption.

---

### E-02 — 2003 first-person reaction to a 5460 redesign

**Source:** CFC 中文网 forum thread, 2003-06-06.  
<https://bbs.comefromchina.com/threads/115276/>

**Grade:** A/B boundary — contemporaneous user post on a third-party forum.  
**Confidence:** high for that poster’s experience; not representative.

A user reports that the new `www.5460.net` interface felt faster and photo management easier, but also says the redesign felt emotionally like moving from a long-inhabited place into a new place and needing to rebuild a sense of “home.”

This is useful because it proves that **interface continuity itself could become part of social continuity**.

It does not prove the underlying database or user counts.

---

### E-03 — 2004 tutorial comparing online classmate directories

**Source:** PChome, 2004-06-23, “百花争艳网上同学录”.  
<https://m.pchome.net/article/content-17875-all.html>

**Grade:** B — contemporaneous tutorial.  
**Confidence:** high for basic visible navigation.

The tutorial gives `http://alumni.chinaren.com`, describes registration/login, notes Sohu or ChinaRen mail credentials could be reused, and describes searching/creating “我的大学 / 我的中学 / 我的小学.”

This supports a state distinction between:

```text
PLATFORM_ACCOUNT_CREATED
and
EXISTING_CREDENTIAL_REUSED
```

It still does not reveal backend identity verification.

---

### E-04 — 2004 public forum preserves a class URL pattern

**Source:** CFC 中文网 forum thread, 2004-09-05.  
<https://bbs.comefromchina.com/threads/278456/>

**Grade:** A/B boundary — contemporaneous user post containing a live-at-the-time locator.

The post preserves a ChinaRen class URL form resembling:

```text
alumni.chinaren.com/class/class_index.jsp?classuuid=<numeric-id>
```

For privacy minimization, this research note does **not** reproduce the ordinary class UUID.

**What this proves:** a JSP/class-UUID URL shape was publicly used in 2004.

**What it does not prove:** that the URL still resolves, its historical DOM, whether the class was public, or whether all member data was visible without authentication.

---

### E-05 — 2005 online classes during internship and post-graduation dispersal

**Source:** 《解放日报》 via Sina, 2005-03-18, “‘我的大学’虚拟化”.  
<https://news.sina.com.cn/s/2005-03-18/09105394097s.shtml>

**Grade:** B — contemporaneous reporting with interviews and reporter observation.  
**Confidence:** high for reported cases; not population-wide.

The article describes:

- a Fudan master’s class whose members dispersed to internships nationwide and used a ChinaRen classmate record for notices, messages and chat;
- other university online classes with administrators;
- a Wuhan University alumnus working in Jiuquan who said the online class continued to connect classmates distributed around the country;
- a counterexample: online expressions of interest did not necessarily produce actual offline activities because people still lacked time.

This is strong evidence that:

> `ONLINE_CLASS_CONTINUITY != OFFLINE_CO-PRESENCE`.

---

### E-06 — 2005 privacy boundary conflict involving 5460-derived data

**Source:** 《长沙晚报》 via Sina, 2005-12-27.  
<https://news.sina.com.cn/c/2005-12-27/11207830273s.shtml>

**Grade:** B — contemporaneous dispute report.  
**Confidence:** medium-high for the reported user complaint; the precise technical acquisition chain remains unresolved.

A user reported that school history, home address/telephone, email and QQ information originally entered on 5460 under an expected classmate-only context was exposed through a third-party people-search service.

This supports a privacy state model:

```text
USER_ENTERS_DATA
→ PLATFORM_STORES_DATA
→ PLATFORM_VISIBILITY_RULE
→ DATA_COPIED / EXPORTED / ACQUIRED ?
→ THIRD_PARTY_INDEX
→ THIRD_PARTY_ACCESS_RULE
```

The `?` is important: the exact extraction, transfer or authorization mechanism must not be inferred from the user complaint alone.

---

### E-07 — 2007 transition from class-centric directory to person-centric SNS

**Source:** Sina Tech, 2007-04-19.  
<https://tech.sina.com.cn/other/2007-04-19/14131474024.shtml>

**Grade:** B + platform claims.  
**Confidence:** high for announced product direction; user-count claims remain platform-supplied.

校内网 described its planned alumni product as more “user-centered” than traditional ChinaRen/5460 classmate directories, with custom pages, aggregation of classmates’ blogs/photos and subscription to friend information.

The critical structural transition is:

```text
CLASS-CENTRIC
school → class → address book / guestbook

becomes

PERSON-CENTRIC
profile → friend edge → content stream → subscription / ambient updates
```

This is not merely a visual redesign; it changes what relationship persistence means.

---

### E-08 — 2008 first-person search and relation-recovery evidence

**Source:** 中青在线 / 中国青年报 via China News, 2008-10-13.  
<https://www.chinanews.com.cn/edu/dxxy/news/2008/10-13/1409431.shtml>

**Grade:** B with contemporaneous first-person testimony.  
**Confidence:** high for the described individuals; non-representative.

Key observations:

- one user worried about missing the appearance of old classmates;
- another received a message from a former high-school classmate, then used names from a graduation photograph to search more than 60 former classmates and found nearly 30 accounts in about half an hour;
- users described searching for former/current overseas upperclassmen to ask about universities and study abroad;
- one interviewee re-evaluated and renewed contact with a previously disliked schoolmate after reading that person’s posts;
- the same article preserves a strong attention-cost counterexample: users repeatedly checking pages, messages and comments even after entering work.

This is direct evidence for:

```text
PROFILE_DISCOVERY
!=
RELATIONSHIP_REACTIVATION
```

but it also proves some cases crossed that boundary.

---

### E-09 — 2010 social graph used for job information

**Source:** 《光明日报》, 2010-04-04.  
<https://epaper.gmw.cn/gmrb/html/2010-04/04/nw.D110000gmrb_20100404_10-05.htm>

**Grade:** B with contemporaneous first-person interview.  
**Confidence:** high for the reported use case.

A graduating student described using the former 校内网 / 人人 relation network for classmates to share, discuss and recommend job information.

Therefore:

> `SOCIAL_EDGE_EXISTS` can become `LABOR-MARKET_INFORMATION_ROUTE`, but the latter still does not imply successful employment.

---

### E-10 — 2019 group persistence without active relationship

**Source:** 人民网《讽刺与幽默》, 2019-11-08.  
<https://paper.people.com.cn/fcyym/html/2019-11/08/content_1955509.htm>

**Grade:** B / contemporaneous first-person commentary.  
**Confidence:** high for the author’s own group behavior; not a national activity rate.

The author describes dozens of WeChat groups, including classmate groups, with most becoming long-term “deep lurk” spaces: users neither speak nor leave.

This provides a successor-state counterexample:

> `GROUP_MEMBERSHIP_PERSISTS != ACTIVE_RELATIONSHIP_PERSISTS`.

It should not be retroactively projected onto 2000-era class pages.

---

## 4. State model A — school and class resolution

A 2000 ChinaRen-style path should be represented as:

```text
SERVICE_ENTRY
→ REGION_SELECTED ?
→ SCHOOL_QUERY
→ SCHOOL_RESULT_SET
→ SCHOOL_RESOLVED
   OR
   SCHOOL_CREATE_REQUEST
→ SCHOOL_RECORD_CREATED ?
→ CLASS_QUERY
→ CLASS_RESULT_SET
→ CLASS_RESOLVED
   OR
   CLASS_CREATE_REQUEST
→ CLASS_RECORD_CREATED ?
→ CLASS_HOME_REQUEST
→ CLASS_HOME_RENDERED
```

Questions that remain independent:

- Was school creation immediate or moderated?
- Could duplicate school records coexist?
- Were class names normalized?
- Did a user have to prove school attendance?
- Could anyone create a class?
- Could class administrators remove members?
- Did school/class identifiers survive platform migrations?

A newspaper walkthrough cannot answer all of these.

---

## 5. State model B — account and class membership

```text
ACCOUNT_ABSENT
→ REGISTRATION_FORM
→ CREDENTIAL_SUBMISSION
→ ACCOUNT_CREATED
→ LOGIN
→ CLASS_FOUND
→ JOIN_REQUEST
→ MEMBERSHIP_PENDING ?
→ MEMBERSHIP_ACCEPTED ?
→ MEMBER_VIEW
```

Possible alternate path, documented in the 2004 PChome tutorial:

```text
EXISTING_SOHU_OR_CHINAREN_MAIL_ACCOUNT
→ CREDENTIAL_REUSE
→ ALUMNI_SERVICE_LOGIN
```

Do not assume:

> `ACCOUNT_CREATED == CLASSMATE_VERIFIED`.

A platform may know only that an account claims a school/class affiliation.

---

## 6. State model C — finding one remembered person

```text
MEMORY_OF_PERSON
→ SEARCH_KEY_AVAILABLE
   [name / school / class / region]
→ QUERY
→ CANDIDATE_ACCOUNTS
→ NAME_MATCH
→ SCHOOL_MATCH
→ CLASS_MATCH
→ PROFILE_OPENED
→ CONTACT_OR_MESSAGE_ROUTE_AVAILABLE
```

Identity still remains unresolved:

```text
NAME_MATCH
!=
SAME_HISTORICAL_PERSON
```

Even stronger tuple:

```text
NAME + SCHOOL + CLASS
!=
ACCOUNT_CONTROLLED_BY_THAT_PERSON_NOW
```

The 2020s fraud cases in the life-history companion demonstrate why this state gap matters, but those later cases are **afterlife evidence**, not part of this repository’s primary old-Web scope.

---

## 7. State model D — contact and actual reconnection

```text
PROFILE_FOUND
→ CONTACT_FIELD_VISIBLE
   OR
   PLATFORM_MESSAGE_ROUTE
→ MESSAGE_COMPOSED
→ MESSAGE_SUBMITTED
→ PLATFORM_ACCEPTED
→ DELIVERY_ATTEMPT
→ INBOX / EMAIL / NOTIFICATION
→ RECIPIENT_NOTICES
→ RECIPIENT_RECOGNIZES_SENDER
→ RECIPIENT_REPLIES
→ OTHER_CHANNEL_EXCHANGED ?
→ OFFLINE_MEETING ?
→ RELATIONSHIP_REACTIVATED ?
```

The historical archive is most likely to preserve the early steps and least likely to preserve the later ones.

Therefore:

> `historical profile capture != evidence of successful reunion`.

---

## 8. State model E — class guestbook, album and address book

A class page could bundle several transaction families that must be separated.

### guestbook

```text
GUESTBOOK_LINK_VISIBLE
→ ENTRY_FORM_OPEN
→ TEXT_ENTERED
→ SUBMIT
→ SERVER_ACCEPTS
→ ENTRY_STORED
→ ENTRY_RENDERED_TO_OTHER_MEMBER
```

### album

```text
ALBUM_LINK_VISIBLE
→ UPLOAD_FORM
→ FILE_SELECTED
→ UPLOAD_ACCEPTED
→ IMAGE_STORED
→ THUMBNAIL_GENERATED ?
→ IMAGE_VISIBLE
→ CAPTION / COMMENT ?
```

### class address book

```text
MEMBER_PROFILE_EXISTS
→ CONTACT_FIELDS_EXIST
→ VISIBILITY_RULE
→ REQUESTER_AUTHORIZED
→ FIELD_RENDERED
→ FIELD_CURRENT ?
```

The final `FIELD_CURRENT` must stay separate. A ten-year-old telephone field can be historically authentic and operationally useless.

---

## 9. State model F — privacy scope and secondary indexing

The 2005 privacy dispute requires a model that does not assume one technical explanation:

```text
USER_SUBMITS_CONTACT_DATA
→ PLATFORM_DATABASE
→ EXPECTED_VISIBILITY_SCOPE
→ ACTUAL_VISIBILITY_SCOPE
→ DATA_ACCESS_BY_OTHER_PARTY
→ COPY / EXPORT / SCRAPE / LICENSE / OTHER ?
→ THIRD_PARTY_DATABASE
→ THIRD_PARTY_SEARCH_RESULT
→ THIRD_PARTY_PAYMENT / ACCESS ?
```

The unresolved transfer edge is historically important.

A later investigator must not rewrite:

> “the user believed the field was classmate-only and later saw it on a third-party search service”

as:

> “5460 sold the field.”

The latter requires independent evidence.

---

## 10. State model G — class-centric directory to ambient SNS

Traditional alumni directory:

```text
USER DECIDES TO VISIT CLASS PAGE
→ CLASS PAGE
→ CHECK GUESTBOOK / ALBUM / ADDRESS BOOK
→ LEARN UPDATE
```

SNS successor:

```text
FRIEND EDGE EXISTS
→ OTHER USER POSTS
→ FEED / NEW-FEED PIPELINE
→ ITEM ELIGIBLE
→ ITEM DELIVERED / RANKED
→ USER NOTICES
→ PASSIVE UPDATE ABOUT OLD CLASSMATE
```

This changes the temporal contract:

- alumni directory is usually **destination pull**;
- social feed is increasingly **ambient push / ranked exposure**.

Do not infer that every friend update was shown or noticed.

`friend edge exists` is not equivalent to `user continuously knows friend’s life`.

---

## 11. URL and implementation locators worth preserving

### ChinaRen 2000

From E-01:

- root: `www.chinaren.com`;
- class subdomain described as `<class-name>.alumni.chinaren.com`.

### ChinaRen 2004

From E-03:

- `alumni.chinaren.com`.

From E-04:

- observed public URL shape: `.../class/class_index.jsp?classuuid=<numeric-id>`.

### 5460 2003

From E-02:

- `www.5460.net`.

These are **historical locators**, not verified archive captures.

No claim should be made yet about:

- server software;
- database vendor;
- exact session cookie names;
- GET vs POST semantics beyond visible URL patterns;
- encoding;
- browser-specific JavaScript;
- image host topology;
- authentication headers.

---

## 12. Browser and page-shape questions still requiring historical capture

For a verified 2000–2005 capture, inspect at minimum:

- HTTP status and redirects;
- `Content-Type` and charset;
- declared vs actual GB2312 / GBK / UTF-8 behavior;
- frameset or iframe use;
- table layout;
- image navigation;
- form method and action;
- hidden school/class IDs;
- JSP/ASP/static URL mix;
- cookies and login redirects;
- whether class subdomain hostnames are real hosts, redirects or virtual-host routing;
- whether album images use a separate asset host;
- whether guestbooks require JavaScript;
- whether “chat room” uses Java Applet, ActiveX, iframe, polling or another mechanism;
- IE-specific assumptions;
- whether archive rewriting breaks forms or script-generated URLs.

Until this is inspected, modern browser behavior cannot be described as historical user experience.

---

## 13. Historical visibility bias

Online classmate services are especially vulnerable to **selective preservation**.

### likely visible today

- public platform descriptions;
- media tutorials;
- public class URL patterns;
- front pages;
- public forum posts about the service;
- press descriptions of user counts;
- redesign announcements.

### likely missing today

- logged-in address books;
- private telephone/email fields;
- member approval history;
- rejected join requests;
- group mail delivery results;
- who read a message but did not answer;
- private chat logs;
- old passwords and account recovery paths;
- QQ/MSN conversations after the initial alumni-site contact;
- actual offline reunions;
- users who never registered;
- people who intentionally did not want to be found.

Therefore:

> **archive-visible class != historical class.**

A saved public shell can overrepresent the platform and underrepresent the actual human network.

---

## 14. Archive/privacy tension

This topic has an unusually strong ethical conflict:

> the historical function depended on making ordinary people findable, while responsible archaeology should not recreate a public directory of their old contact details.

Repository policy should therefore prefer preserving:

- host/path patterns;
- UI structure;
- form fields as field names, not personal values;
- screenshots only when rights/privacy allow;
- synthetic examples for reconstruction;
- claim-level summaries;
- archive metadata.

Avoid republishing:

- old home addresses;
- telephone numbers;
- emails;
- QQ numbers;
- private messages;
- ordinary users’ class UUIDs where unnecessary;
- deleted personal profiles.

The fact that an archive can technically expose an old address does not automatically make redistribution appropriate.

---

## 15. Platform persistence state

A relationship platform can decay in several distinct ways:

```text
DOMAIN_RESOLVES
→ HOMEPAGE_LOADS
→ LOGIN_WORKS
→ ACCOUNT_RECOVERABLE
→ SCHOOL_INDEX_WORKS
→ CLASS_PAGE_WORKS
→ MEMBER_DIRECTORY_WORKS
→ OLD_MESSAGES_WORK
→ OLD_PHOTOS_WORK
→ EXPORT_AVAILABLE
```

These states can fail independently.

Therefore:

> `homepage alive != class archive alive`.

and:

> `domain dead != people/relationships dead`.

The latter is crucial: users may already have moved to QQ, MSN, phone, Renren or WeChat while the old platform disappears.

Historical platform death is partly a **memory-access event**, not necessarily a relationship-death event.

---

## 16. Redesign as a historical event, not cosmetic noise

The 2003 5460 forum post is valuable because it captures an ordinary user treating interface change as a change of social place.

A redesign can alter:

- page URL;
- where photos live;
- navigation hierarchy;
- search behavior;
- class-home affordances;
- habitual checking path;
- emotional familiarity;
- archiveability.

So archaeology should record redesigns as possible **social-continuity breaks**, not only CSS differences.

---

## 17. Counterexamples

### CEX-1 — easy online contact does not create offline time

The 2005 Fudan/Tongji reporting includes students who could coordinate online but still could not make a football match happen because schedules did not align.

### CEX-2 — a class can stay active while people are geographically dispersed

The Wuhan University graduate in Jiuquan demonstrates the opposite of the simple “migration destroys class ties” story.

### CEX-3 — a profile can be findable while contact data is unsafe

The 2005 privacy dispute shows that findability and privacy are not monotonic public goods.

### CEX-4 — redesign can improve technical usability and still feel like social loss

The 2003 5460 user explicitly reports this split.

### CEX-5 — newer SNS does not necessarily preserve the old archive

A successor social graph can maintain people while old guestbooks/photos/class pages disappear.

---

## 18. Hindsight risks

### H-01 Do not call ChinaRen “an early WeChat”

It was organized around Web-era school/class pages, destination visits, guestbooks, albums and address books. Modern always-on messaging semantics must not be projected backwards.

### H-02 Do not treat 2008 users as if they already knew Renren would decline

Their contemporaneous experience was rapid expansion of a new social graph. Later nostalgia is a different evidence layer.

### H-03 Do not equate “real-name campus network” with verified legal identity

A school/name tuple, a platform account and legal person verification are separate states.

### H-04 Do not convert platform-supplied user counts into active-person counts

Registered accounts, active users, class memberships and active relationships are different denominators.

### H-05 Do not infer causality from sequence

A user finding a job after receiving information from classmates does not prove the platform caused employment without stronger evidence.

---

## 19. Historical capture attempt in this slice

Targets attempted:

- `alumni.chinaren.com` for 2000–2001;
- `5460.net` for 2000–2004.

Method attempted:

- public Web search for archived Wayback locators;
- direct CDX URL attempts.

Result:

- no search result produced a replay that could be opened and inspected in this run;
- direct constructed CDX URLs were rejected by the current Web access layer because the exact URL had not first appeared as a safe searchable result;
- therefore no capture datetime, replay HTTP state, charset, DOM, cookie/session behavior or subresource completeness was verified.

### M1 status

> **NOT ACHIEVED IN THIS SLICE.**

This means only:

> **this run did not verify a qualifying historical capture.**

It does **not** mean:

> “Wayback did not preserve ChinaRen/5460.”

That stronger negative claim is prohibited by `docs/METHOD.md`.

---

## 20. Next capture priorities

If this object is revisited, highest-value archive work is:

1. find one verifiable ChinaRen capture around 2000–2001;
2. record original URL, capture URL and Memento datetime;
3. inspect charset and page structure;
4. determine whether school/class search is replayable or only shell HTML survives;
5. locate one public class page without republishing member contact data;
6. test class subdomain vs `classuuid` URL generations;
7. locate one 5460 capture before/after the 2003 redesign;
8. compare photo asset survival;
9. record login boundary without attempting to recover private member data;
10. then decide whether this topic can graduate from research note to an M1-grade forum/community case.

---

## 21. Minimum claims safe to reuse now

### Confirmed / high confidence

- A 2000 contemporaneous tutorial described ChinaRen school/class search, school/class creation, class URL naming and class communication features.
- A 2003 contemporaneous user post identifies `www.5460.net` and reacts to a redesign, including photo-management changes.
- A 2004 contemporaneous tutorial identifies `alumni.chinaren.com` and describes registration plus school-stage search/create functions.
- A 2004 public user post preserves a `class_index.jsp?classuuid=...` locator pattern.
- 2005 contemporaneous reporting documents geographically dispersed students/alumni using online class pages for coordination and continued contact.
- 2005 contemporaneous reporting documents a dispute over 5460-origin personal information appearing in a third-party people-search service.
- 2007 contemporaneous reporting documents the announced transition toward profile/feed-centered alumni SNS features.
- 2008 contemporaneous interviews document users searching old classmates by name, using the social graph for study-abroad information and in some cases reactivating a relationship.

### High probability but still incomplete

- ChinaRen/5460 implemented multiple backend membership/authorization states not visible in press tutorials.
- redesigns likely changed URL, rendering and asset topology across years.
- a meaningful share of relationship continuation moved off-platform into QQ/MSN/phone, making the alumni site only the discovery layer.

### Unknown in this slice

- exact historical charset and browser assumptions for the key 2000 ChinaRen class page;
- exact membership verification rules;
- exact privacy permission implementation;
- exact data path in the 2005 third-party privacy dispute;
- message delivery/read semantics;
- one fully verified historical replay meeting M1 requirements.

---

## 22. What this changes about Chinese old-Web archaeology

The online classmate directory is a particularly useful reminder that an old Web page can be **social infrastructure rather than merely content**.

A class homepage did not matter only because it displayed text and images. It mattered because a user could attempt to move through a hidden transaction chain:

```text
remember a person
→ remember a school/class
→ locate a class page
→ locate an account
→ expose or request a contact route
→ send a message
→ wait for another human to recognize the message
→ continue elsewhere
```

Almost every state after `PAGE_RENDERED` is poorly preserved by conventional Web archives.

That means a perfectly replayed screenshot of an old class page could still miss the most historically important thing the service did.

The archaeology problem is therefore not just:

> “What did ChinaRen look like?”

but:

> **“Which parts of the ordinary act of finding an old classmate survive as Web evidence, and which parts disappeared because they lived in authentication, databases, private fields, external messengers and human recognition?”**

That distinction should carry forward into future forum/SNS cases.
