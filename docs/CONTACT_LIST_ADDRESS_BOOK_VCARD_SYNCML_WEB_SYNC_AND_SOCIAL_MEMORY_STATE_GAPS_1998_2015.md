# CONTACT LIST / ADDRESS BOOK / VCARD / SYNCML / WEB SYNC STATE GAPS (1998—2015)

> Scope: **约 1998—2015 中文旧网中的个人通讯录、Web 地址簿、联系人导入/导出与跨终端同步状态。**
>
> 本稿不是全球联系人协议史，也不是现代移动隐私综述。1998 vCard、2000 SyncML 只作为理解中文旧网 artifact 的必要技术前史；2015 以后“联系人权限治理”的长期生活史比较主要放在 sibling repository `tmzncty/how-people-lived`。

Cross-link:

- <https://github.com/tmzncty/how-people-lived/blob/main/topics/from-paper-address-books-to-cloud-contacts-social-memory-portability-china-1980s-2026.zh-CN.md>

---

## 1. 为什么这是一个 old-Web 问题，而不只是“手机换机教程”

2000s 中国用户的联系人并不天然属于一个现代 OS account。

同一个人的联系资料可能同时散落在：

- SIM；
- 手机机身电话簿；
- PC/PDA 本地通讯簿；
- 厂商 PC Suite；
- 运营商 PIM / “号簿管家”；
- QQ 同步助手账号；
- QQ 邮箱/PC QQ 可管理的联系人；
- Web 端 `pim.qq.com`；
- 导出的 CSV / vCard / 私有备份文件；
- 后来的智能手机系统联系人数据库。

因此旧网页中一个“导入联系人”“同步成功”“云备份”的按钮，其背后通常不是一个页面状态，而是一条跨手机、浏览器、账号、网关、同步协议和远端数据库的事务链。

按照本仓 METHOD，本切片严格区分：

```text
platform
!= web host
!= account
!= contact row
!= export artifact
!= sync transaction
!= archive capture
!= researcher claim
```

同时继续坚持：

```text
exists != available != used != popular != caused
```

---

## 2. 研究问题

本切片回答六个具体问题：

1. 中文旧网什么时候出现“联系人不只属于本机，也可以由 Web/账号保管”的可核验路径？
2. 一个历史页面里看到“备份/同步/导入/导出”时，究竟还缺哪些状态才能证明事务真的发生？
3. vCard、SyncML、PC Suite、运营商 PIM、QQ 同步之间是什么关系，哪些不能合并成“云同步”？
4. archive 保存一个 Web 地址簿外壳时，为什么通常仍然无法恢复真实联系人状态？
5. 同步系统的错误、冲突、覆盖和号码陈旧怎样影响历史解释？
6. 在不重新公开普通人的私人关系图的前提下，怎样做合格的 old-Web reconstruction？

---

## 3. Claim list

### C1 — 1998 年 vCard 已把个人联系信息定义成可跨系统交换的结构化对象

RFC 2426（September 1998）定义 vCard 3.0，可表示姓名、地址、电话、Email、照片等个人目录字段；RFC 还明确提醒联系人信息会变旧，并提供 `REV` 等机制表达更新时间。

Evidence:

- **A / high** — RFC 2426: <https://www.rfc-editor.org/info/rfc2426/>

What this proves:

- 1998 年存在标准化联系人交换对象；
- `TEL`、`EMAIL`、`ADR` 等字段具有明确定义。

What this does **not** prove:

- 中国普通用户 1998 年普遍使用 vCard；
- 某一个国产手机/网页兼容全部字段；
- `.vcf` 能无损穿过所有系统。

### C2 — 2000 年 SyncML 把“个人信息跨设备保持一致”明确做成开放同步问题

SyncML Initiative 2000 年同期公告称，该组织由 Ericsson、IBM、Lotus、Motorola、Nokia、Palm、Psion、Starfish 等推动，目标是让 remote data 与 personal information 跨网络、平台、设备进行 universal synchronization。

Evidence:

- **A/B / high for announcement** — 2000-05-10 SyncML Initiative announcement: <https://www.globenewswire.com/fr/news-release/2000/05/10/1845116/0/en/SyncML-Initiative-Announces-Wide-Support-and-New-Aggressive-Development-Schedule.html>

Boundary:

```text
standard specified != handset implements != operator enables != user configures != successful sync
```

### C3 — 2008 年中国移动“号簿管家”已留下 Web ↔ 手机 ↔ 本地文件的普通用户操作证据

2008-09-07 的 TM700 同期技术记录描述：手机自带 PC 助手形成数据闭环，不能方便批量导入已有电话簿；作者转而使用中国移动“号簿管家”，将其描述为基于 Web 的联系人管理系统，手机可以与其同步，Web 端可以导出电脑本地文件，也可以反向导入。

Evidence:

- **B / high for described user path** — 3533 手机世界，2008-09-07，《给飞利浦TM700导入电话薄》：<https://www.3533.com/news/2008/9/7/85679.htm>
- **A/B / medium for product architecture, date unclear on current page** — 中国移动宁夏现存“号簿管家”说明：<https://www.nx.10086.cn/support/brand/gotone/vipclub/hyfw/110000004662.html>

The operator page says the service can involve Web、WAP、SMS、SyncML、manual management and terminal synchronization.

This is enough to establish a **historical architecture family**. It is not enough to reconstruct the exact 2008 national hostname, login flow or server transaction.

### C4 — 2010—2011 QQ 同步助手把 QQ account 变成跨手机平台联系人同步主体

2010-11-17 手机中国/搜狐同期报道 says QQ 同步助手 PPC version completed coverage of several mainstream smartphone systems; users could log in with QQ number and perform cross-platform contact import/export, alongside SMS/call-record backup.

Evidence:

- **B / high** — 搜狐数码/手机中国：<https://digi.it.sohu.com/20101117/n277693943.shtml>

2011 sources further describe cloud backup / cross-brand synchronization. A 2011-12-07 source explicitly states that users could manage contacts and important SMS through PC at `pim.qq.com`.

Evidence:

- **B / medium-high** — cnBeta, 2011-07-14: <https://www.cnbeta.com.tw/articles/soft/148779.htm>
- **B / high for hostname claim** — 电脑商情在线, 2011-12-07: <https://www.cbinews.com/desktop/0RCMO1>

Boundary:

```text
pim.qq.com mentioned in contemporary source
!= a verified 2011 archive capture of pim.qq.com
```

### C5 — By 2015, `pim.qq.com` was still referenced as a Web management/export surface

A 2015 tutorial on migrating Android SMS to iPhone tells users to log into QQ Sync Assistant Web at `http://pim.qq.com/`, find cloud data and export SMS.

Evidence:

- **B / medium** — 2015-11-04 tutorial: <https://www.duote.com/tech/android/93887.html>

This supports continuity of the Web-management idea into the end of this repository’s primary period. It does not by itself identify the precise 2010 UI or prove unchanged backend semantics.

---

## 4. Object model: “一个联系人”到底是什么

历史 reconstruction 不应把一行“张三 138…”当作唯一对象。

最低限度要区分：

```text
PERSON
  ├─ name(s)
  ├─ phone number(s)
  ├─ email(s)
  ├─ organization/title
  └─ other identifiers

CONTACT RECORD
  ├─ record id
  ├─ fields
  ├─ local storage owner
  ├─ source
  ├─ last modified
  └─ sync metadata

ADDRESS-BOOK CONTAINER
  ├─ SIM
  ├─ handset-local store
  ├─ desktop/PDA store
  ├─ operator PIM account
  ├─ QQ/cloud account
  └─ exported artifact
```

关键硬边界：

```text
same display name != same person
same phone number != same person across time
same person != same contact record
same contact record != same field set after import/export
```

手机号二次放号尤其意味着：

```text
old contact row survives
!= current number holder is the historical person
```

因此联系人研究必须与 sibling 的 phone-number lifecycle 研究相互引用，但不能合并。

---

## 5. State machine A — 从手工联系人到可导出对象

```text
A0 PERSON KNOWN
  ↓
A1 CONTACT DATA ENTERED
  ↓
A2 STORED IN A LOCAL CONTAINER
  ↓
A3 FIELD MAPPING KNOWN
  ↓
A4 EXPORT REQUESTED
  ↓
A5 EXPORT GENERATED
  ↓
A6 EXPORT FILE SAVED
  ↓
A7 FILE MOVED TO ANOTHER DEVICE/SERVICE
  ↓
A8 IMPORT REQUESTED
  ↓
A9 PARSE/MAP
  ↓
A10 MERGE / CREATE / SKIP / FAIL
  ↓
A11 DESTINATION CONTACT USABLE
```

Do not collapse:

```text
Export button exists
!= export generated
!= file downloaded
!= file parseable elsewhere
!= imported fields preserved
```

Potential historical failure modes:

- GBK / UTF-8 / Unicode name corruption;
- different number formatting;
- multiple phone numbers collapsed into one;
- notes/organization fields dropped;
- unsupported photo/birthday fields;
- duplicate creation;
- SIM capacity/field limits;
- proprietary PC-suite format.

---

## 6. State machine B — Web / cloud synchronization

```text
B0 LOCAL CONTACT SET
  ↓
B1 SYNC SERVICE EXISTS
  ↓
B2 USER ACCOUNT AUTHENTICATED
  ↓
B3 DEVICE/AUTHORIZATION BOUND
  ↓
B4 LOCAL CHANGESET ENUMERATED
  ↓
B5 NETWORK REQUEST SENT
  ↓
B6 SERVER ACCEPTS DATA
  ↓
B7 REMOTE ADDRESS BOOK UPDATED
  ↓
B8 REMOTE REVISION / SERVER STATE EXISTS
  ↓
B9 SECOND DEVICE AUTHENTICATES
  ↓
B10 REMOTE CHANGESET FETCHED
  ↓
B11 CONFLICT POLICY APPLIED
  ↓
B12 SECOND LOCAL STORE UPDATED
  ↓
B13 HUMAN CAN ACTUALLY FIND/CALL THE CONTACT
```

Required boundaries:

```text
sync button clicked != request sent
request sent != server committed
server committed != all fields preserved
remote state updated != second device fetched
second device fetched != conflict resolved correctly
UI says success != every contact converged
```

---

## 7. State machine C — Merge / conflict / deletion

The most dangerous reconstruction error is assuming synchronization is simple copying.

```text
C0 SAME LOGICAL PERSON EXISTS IN TWO STORES
  ↓
C1 MATCH CANDIDATE FOUND
  ↓
C2 POLICY CHOOSES:
     - MERGE
     - KEEP BOTH
     - OVERWRITE LOCAL
     - OVERWRITE REMOTE
     - USER DECIDES
  ↓
C3 RECORD MUTATED
  ↓
C4 CHANGE PROPAGATED
```

Deletion must be modeled separately:

```text
D0 CONTACT PRESENT BOTH SIDES
  ↓
D1 DELETED LOCALLY
  ↓
D2 TOMBSTONE / CHANGE EVENT CREATED ?
  ↓
D3 SERVER RECEIVES DELETE ?
  ↓
D4 REMOTE ROW REMOVED / RECYCLE-BINNED ?
  ↓
D5 OTHER DEVICES RECEIVE DELETE ?
```

A 2017 App Store user review preserved on the current official QQ Sync Assistant listing says the user enjoyed cross-device sync but had sometimes experienced contacts disappearing and was unsure whether it came from their own operation. This is **contemporaneous user testimony, not a verified bug report**. It nevertheless proves that ordinary users could perceive synchronization itself as a possible failure domain.

Source:

- Apple App Store, official Tencent QQ同步助手 listing: <https://apps.apple.com/cn/app/id389481236>

Because 2017 is outside this repository’s central 1995—2015 scope, it is cited only as a later caution about state semantics, not as old-Web primary evidence.

---

## 8. Web surface model — what a surviving page can and cannot show

A 2008—2012 Web contact service may expose some combination of:

- login page;
- contact list shell;
- search box;
- create/edit form;
- import link;
- export link;
- synchronization instructions;
- download client link;
- quota/count display;
- duplicate merge UI;
- restore/recycle-bin UI;
- help documentation.

But the actual contact rows are usually:

- behind authentication;
- generated dynamically;
- fetched by XHR/JS;
- stored in private account databases;
- explicitly inappropriate to republish.

Therefore:

```text
Web address-book shell captured
!= private contact dataset captured
```

and also:

```text
empty contact-list template captured
!= historical user had zero contacts
```

An archive replay of the public shell can still be valuable if it preserves:

- field names;
- import/export formats;
- client downloads;
- supported browsers;
- sync terminology;
- public API/help URLs;
- charset;
- request/form structure that does not expose private rows.

---

## 9. Permission is a separate state from synchronization

For late-period smartphone clients, access to the local contacts store must be modeled separately:

```text
APP INSTALLED
  ↓
CONTACT PERMISSION REQUESTED
  ↓
GRANTED / DENIED
  ↓
LOCAL STORE READABLE ?
  ↓
CONTACTS ENUMERATED ?
  ↓
DATA UPLOADED ?
  ↓
REMOTE STORED ?
```

Hard rule:

```text
READ_CONTACTS permission declared
!= permission granted
!= contacts actually read
!= contacts uploaded
!= contacts retained server-side
```

2019 regulatory/testing material is outside this doc’s core time window, but it is a useful methodological warning: China’s App governance work explicitly treated `READ_CONTACTS` as a capability to read the address book and found contact-access code in many tested APKs. Do not project that later Android permission model backward onto a 2008 WAP/PIM website.

Method reference only:

- CAC 2019: <https://www.cac.gov.cn/2019-05/24/c_1124538535.htm>

---

## 10. Preservation levels

### P0 — Brand/name only

We know a service such as “号簿管家” or “QQ同步助手” existed.

Not enough to claim any specific Web UI.

### P1 — Contemporary public description

A contemporary manual/news/tutorial describes Web management, import/export or synchronization.

Useful for claims about feature existence and workflow family.

### P2 — Verified public Web capture

Must record:

- archive source;
- original URL;
- capture URL;
- capture datetime;
- HTTP/replay state;
- Content-Type/charset where visible;
- whether page is login/error/redirect;
- main resource vs missing subresources.

### P3 — Interaction shell preserved

Login/import/export/edit UI, forms, JS and resource dependencies can be inspected.

Still does **not** prove live private account state.

### P4 — Synthetic/research transaction reconstruction

Using only lawful, researcher-owned/synthetic data, a compatible client/server or archived documentation can reconstruct field transformations.

Must be clearly labeled `reconstruction`.

### P5 — Format-level portability evidence

Historical export artifact specification/sample with no private ordinary-person data shows actual schema/encoding and can be parsed.

### P6 — Full historical private contact graph

**Not a preservation target.**

A real user’s address book may contain sensitive personal data about many non-consenting people. Even if a historical leak/archive exists, this repository should not copy or republish it merely to achieve “completeness”.

---

## 11. Archive bias: private social memory is anti-archive by design

This slice has a structural preservation asymmetry.

Easy to preserve publicly:

- product announcement;
- “如何同步联系人” tutorial;
- download link;
- login shell;
- feature list;
- supported device list;
- vCard/SyncML standards;
- import/export button labels.

Hard or inappropriate to preserve:

- real contact rows;
- private notes;
- phone numbers tied to ordinary people;
- relationship labels;
- sync history;
- deleted contacts;
- conflict/tombstone records;
- SMS/phonebook relationship data.

Therefore:

> **archive-visible address-book infrastructure != historical social graph**

A high-quality archaeological result may be able to reconstruct the schema and state machine while intentionally *not* reconstructing the actual social network.

---

## 12. Historical-visibility trap: a contact record can outlive the relationship and the number

Three clocks diverge:

```text
PERSON / RELATIONSHIP LIFETIME
PHONE-NUMBER ASSIGNMENT LIFETIME
CONTACT-ROW LIFETIME
```

Example:

```text
2008: user saves “同事小李 → number X”
2010: colleague changes number
2012: number X is reassigned
2014: old contact row still exists in cloud backup
```

In 2014 the row is a valid historical artifact of what the user once saved, but it is not reliable evidence that the same person still owns X.

Thus:

```text
contact row timestamped 2014
!= relationship created in 2014
!= number-person binding valid in 2014
```

This is a key bridge to this repository’s existing mobile-number lifecycle research.

---

## 13. Browser / client assumptions

A historical contact system can depend on more than the browser.

Record where possible:

- desktop browser / WAP browser;
- charset and form encoding;
- mobile client version;
- handset OS;
- PC Suite version;
- USB/serial/Bluetooth/IR transport;
- SyncML support;
- server endpoint;
- QQ/operator account authentication;
- Java/J2ME/Symbian/WM client package;
- local OS contact database permissions.

Do not write:

> “The 2008 website synchronized the phonebook.”

Prefer:

> “A 2008 contemporary user report describes a TM700 handset synchronizing its local phonebook with China Mobile’s Web-based 号簿管家; this slice has not independently reconstructed the handset-to-server protocol or a verified Web memento.”

---

## 14. Source register

| Source | Date | Grade | Supports | Limits |
|---|---:|---|---|---|
| RFC 2426 | 1998-09 | A | vCard field/exchange model | not China adoption |
| SyncML Initiative announcement | 2000-05-10 | A/B | universal personal-data sync goal | announcement, not household use |
| 3533 TM700/号簿管家 tutorial | 2008-09-07 | B | user-described Web sync/export/import path | one handset/user path |
| 中国移动宁夏 号簿管家 page | date unclear current page | A/B | product architecture: WEB/WAP/SMS/SyncML | unsuitable alone for launch date |
| 手机中国/搜狐 QQ同步助手 PPC | 2010-11-17 | B | QQ-account cross-platform sync | media/product report |
| cnBeta QQ通讯录云备份 | 2011-07-14 | B | cross-brand/cloud-backup claim | “永不丢失” is marketing claim |
| 电脑商情在线 QQ通讯录 3.1 | 2011-12-07 | B | `pim.qq.com` Web management hostname | not a capture itself |
| 2015 migration tutorial | 2015-11-04 | B | `pim.qq.com` still referenced for Web export | tutorial, not backend proof |

URLs:

- <https://www.rfc-editor.org/info/rfc2426/>
- <https://www.globenewswire.com/fr/news-release/2000/05/10/1845116/0/en/SyncML-Initiative-Announces-Wide-Support-and-New-Aggressive-Development-Schedule.html>
- <https://www.3533.com/news/2008/9/7/85679.htm>
- <https://www.nx.10086.cn/support/brand/gotone/vipclub/hyfw/110000004662.html>
- <https://digi.it.sohu.com/20101117/n277693943.shtml>
- <https://www.cnbeta.com.tw/articles/soft/148779.htm>
- <https://www.cbinews.com/desktop/0RCMO1>
- <https://www.duote.com/tech/android/93887.html>

---

## 15. Historical replay attempt in this slice

Candidate historical hosts/objects searched:

- `pim.qq.com` (contemporaneously documented in 2011);
- China Mobile “号簿管家” / PIM public Web surfaces;
- contemporary help/tutorial references around 2008—2012.

This run did **not** obtain a verified memento satisfying the repository’s minimum archive contract (`original_url + capture_url + capture_datetime + replay/HTTP state + charset/DOM inspection`). Attempts to construct Wayback CDX/replay URLs through the current research access path were rejected by the environment’s safe-URL restriction before a historical response could be inspected.

Therefore:

**M1 verified historical contact-Web capture: NOT ACHIEVED IN THIS SLICE.**

This means only:

> “No qualifying capture was verified in this research run.”

It does **not** mean:

> “Wayback did not preserve `pim.qq.com` / 号簿管家.”

Next run should search known archive indices through a permitted locator path, then actually inspect the returned memento before upgrading any claim.

---

## 16. What is confirmed / probable / unknown

### Confirmed

- vCard standardized a structured contact exchange format by 1998.
- SyncML proponents were explicitly working on cross-device personal-information synchronization in 2000.
- A 2008 Chinese user-facing source describes China Mobile 号簿管家 as a Web-based contact-management/sync bridge for TM700.
- 2010 media documentation describes QQ-account-based cross-platform contact synchronization.
- 2011 contemporary documentation names `pim.qq.com` as a PC Web surface to manage cloud contacts/data.

### High probability but not fully reconstructed

- 2008—2012 Chinese users could encounter hybrid workflows combining handset-local contacts, Web account, client software and export files.
- Different clients almost certainly had field/encoding/capability differences; exact matrix remains unbuilt.
- Dynamic/private contact rows are less likely to survive public Web archives than public help/login shells.

### Unknown in this slice

- precise first-launch date and national rollout of 号簿管家;
- exact 2008 national hostname(s), authentication and SyncML endpoints;
- exact 2010/2011 `pim.qq.com` DOM, charset, form/action and JS dependencies;
- server conflict/deletion/tombstone semantics of early QQ sync;
- actual adoption rates among ordinary handset owners;
- proportion of users relying on SIM, PC Suite, operator PIM or QQ sync in each year.

---

## 17. Counterexamples and hindsight risks

1. **Do not write a linear “paper → SIM → cloud” replacement story.** These storage layers coexisted, and many users continued manual copying/PC backup after cloud tools appeared.
2. **Do not equate Web management with mass use.** A service can exist for compatible phones and still be niche.
3. **Do not infer backend behavior from a marketing page.** “同步成功”“永不丢失” are claims, not transaction evidence.
4. **Do not treat all `.vcf` imports as lossless.** Field and encoding mappings vary.
5. **Do not treat a preserved contact row as a durable identity binding.** Phone numbers and relationships change.
6. **Do not republish private address books to make archaeology look complete.** A privacy gap can be the correct end state.
7. **Do not project Android-era permissions backward onto WAP/SyncML/Web systems.** Different trust boundaries applied.
8. **Do not call a search-engine result containing a Wayback URL a capture.** It remains a candidate until opened and inspected.

---

## 18. What this adds to old-Web archaeology

Old-Web preservation often assumes the important historical object is “the page”. Personal address books show a class of system where the page is only the thinnest public shell.

The real historical object is distributed:

```text
private local data
+ account identity
+ format mapping
+ browser/WAP/client UI
+ sync protocol
+ remote database
+ merge/deletion policy
+ another device
+ human relationship that may already have changed
```

So a screenshot of a 2011 “联系人云备份” page can establish the existence and rhetoric of the feature, but it cannot establish that a particular user’s 372 contacts were complete, current, synchronized or recoverable.

That distinction is not a nuisance. It is exactly the archaeological result.

---

## 19. Next research tasks

1. Obtain and inspect at least one verified 2008—2012 memento for `pim.qq.com` or a documented 号簿管家 public host.
2. Locate contemporary downloadable client packages/manuals for one supported platform (Symbian/WM/J2ME) and record protocol/configuration dependencies without redistributing proprietary binaries.
3. Find a non-sensitive historical vCard/CSV template or official sample to test charset/field round-tripping.
4. Build a small synthetic reconstruction: `GBK Chinese name + two phone fields + email + organization → export/import`, clearly labeled `reconstruction`.
5. Search ArchiveTeam/Common Crawl for public help pages, not private user data.
6. Cross-link with mobile-number recycling, password/account recovery and personal-file portability companions.

Initial draft AI-assisted; factual claims should continue to be checked against located evidence under `docs/METHOD.md`.