# Matchmaking profile schemas, searchable life fields, and form-survival gaps (China, 2003–2011)

> Status: research note / evidence checkpoint. This is **not** an M1 complete case and does not claim to reconstruct an original Jiayuan / Baihe registration or search interface.
>
> Scope: the repository remains centered on the roughly 1995–2015 Chinese Web. Earlier newspaper personal ads, marriage-agency cards, and the 1991 `电脑红娘` are used only as boundary history to show that structured partner data predates the Web; the archaeological object here is the old Chinese Web's profile / search / verification architecture.
>
> Cross-research context: this note complements `tmzncty/how-people-lived/sources/personal-ads-computer-matchmaking-searchable-profiles-and-partner-market-legibility-china-1981-2024.zh-CN.md`.

## 0. Why this note is not another generic `page != transaction` memo

The distinct old-Web issue is that a matchmaking service does not merely expose pages. It defines a **schema for a person** and then makes selected attributes searchable, rankable, visible, hidden, editable, or verifiable.

A historical homepage can survive while the socially consequential parts disappear:

```text
homepage survives
!=
registration form survives
!=
profile field schema survives
!=
search filters survive
!=
verification rules survive
!=
ranking / recommendation logic survives
!=
historical candidate database survives
```

For ordinary-life history this matters because a field such as `学历`, `收入`, `婚姻状况`, `身高`, `所在地`, or `住房` is not just interface chrome. Once the service lets users filter or rank by it, that field becomes part of how strangers are made legible to one another.

This note calls that object a **`profile schema`**.

---

## 1. Boundary history: structured matchmaking predates public Web dating

Chinese partner-search media were already structured before mass Internet access.

- 1980s newspaper / magazine personal ads compressed people into short packets of age, occupation, income, height, housing, education, family responsibility and desired-partner criteria.
- Guangzhou's early-1980s marriage agency used cards that visitors could inspect and staff could match.
- In 1991, *China Women* / 《中国妇女》 announced a `电脑红娘` service operated with research organizations; a 1992 follow-up discussed applicants who set conditions such as doctorate, high income, or overseas status too narrowly.

Current institutional retrospective:

- China Women / 婚姻与家庭, 2024-09-30, `“鹊桥”栏目创办40周年，《中国妇女》记录下的大龄青年婚恋变迁`  
  https://www.womenofchina.com/jiatin/2024/0930/15704.html

This boundary prevents a serious chronology error:

```text
computer matchmaking
!=
Internet dating
```

The 1991 user-facing process may have involved paper forms, mail, telephone, institution staff and a backend computer. No TCP/IP user access, browser, public search interface or online profile should be inferred from the phrase `电脑红娘`.

For OWA, this prehistory is useful only because it tells us what the Web later changed: not the first appearance of fields, but the ability of ordinary users themselves to repeatedly enter, edit, search and compare a large profile database.

---

## 2. 2008 contemporaneous functional evidence: the service was already a hybrid online/offline route

A 2008-08-19 *New Century Weekly* article currently preserved by Sina follows a 30-year-old Beijing civil servant who had gone through years of family-arranged dates before trying Baihe. The report describes paid service, a `婚恋类型测试`, online interaction with a platform worker, and rapid movement into an offline meeting and marriage.

Current representation:

- Sina / 新世纪周刊, 2008-08-19, `甜蜜的对抗：婚恋网站的模式之争`  
  https://news.sina.com.cn/c/2008-08-19/115016140459.shtml

**Evidence grade: B — contemporaneous media description of service use.**

It supports claims such as:

```text
by 2008:
professional matchmaking websites were an executable alternative route
+ paid service existed
+ a psychological / matchmaking test was user-visible
+ online discovery could hand off to offline meeting
```

It does **not** establish:

- the historical registration DOM;
- the exact field list;
- which fields were required;
- the exact option values;
- client-side validation;
- whether all profile claims were verified;
- historical ranking logic;
- a byte-identical 2008 page representation.

A newspaper description of `婚恋类型测试` is not the test artifact itself.

---

## 3. 2011 Jiayuan SEC filing: first-party evidence for transaction architecture

Jiayuan.com's 2011 U.S. SEC F-1 is a much stronger source for service architecture than a later retrospective or current page.

Source:

- U.S. SEC, Jiayuan.com International Ltd., Registration Statement on Form F-1, filed 2011  
  https://www.sec.gov/Archives/edgar/data/1511683/000104746911003874/a2203517zf-1.htm

The filing describes a system in which:

1. users could register for free and then immediately search the full database;
2. the first message could be sent without charge, but either sender or recipient had to spend the equivalent of RMB 2 in virtual stamps for that first message to be readable;
3. after the first message was read, subsequent site communication between the pair was free;
4. value-added services included refined search, higher search ranking / visibility, priority messages, online chat, and premium profile display;
5. some service had been available through mobile browsers since June 2010;
6. the company encouraged users to submit evidence for attributes including age, income and education; after proof and a small fee, the profile could obtain a higher rating;
7. after registration, some basic personal information such as height, salary and education could not simply be changed in a more favorable direction without verification.

**Evidence grade: A for first-party description of 2011 business and service rules, with normal issuer-bias caution for competitive / market-quality claims.**

### 3.1 Transaction architecture

The old-Web transaction can therefore be modeled more precisely than `profile page -> message`:

```text
register
→ profile enters searchable database
→ search / browse candidate profiles
→ send initial message
→ virtual-stamp payment state determines readability
→ first message read
→ subsequent communication unlocks
→ optional paid visibility / refined search / ranking
→ offline meeting / VIP / event may follow
```

This is a genuinely distinct architecture for OWA because **visibility and communication are partially monetized state transitions inside the social graph**.

The archaeological target is not just a pretty homepage; it includes profile creation, result sets, communication state, payment gates and verification state.

---

## 4. New object: `profile-schema artifact`

A historical matchmaking form should be treated as a structured artifact, not merely a screenshot.

For each field, record if recoverable:

| Field | Meaning |
|---|---|
| `display_label` | what the user saw, e.g. 学历 / 身高 |
| `field_name` | HTML / request parameter name |
| `input_type` | text, radio, select, checkbox, date, etc. |
| `option_list` | exact categories available at that historical time |
| `required` | whether completion was mandatory |
| `default` | preselected value / placeholder |
| `validation` | client or server validation actually evidenced |
| `editable_after_registration` | whether users could later change it |
| `profile_visibility` | whether others could see it |
| `searchable` | whether it could be used as a search predicate |
| `sortable` | whether result ranking could use it |
| `verification_state` | self-asserted / document-submitted / verified / unknown |
| `proof_type` | ID / diploma / income evidence / unknown |
| `ranking_effect` | whether verification or paid state affected order / rating |
| `price_effect` | whether access to field/search/filter required payment |

This makes the historical option list itself an archaeological source. For example, a platform that offers only `未婚 / 离婚 / 丧偶` is not merely storing text: it has chosen a finite vocabulary through which users must represent marital history.

### 4.1 Claim boundary

```text
field exists
!=
field is searchable
!=
field is used in ranking
!=
field is independently verified
```

Do not collapse these states.

---

## 5. `profile-schema salience`: interface categories can become social categories in use

The cross-repository life-history package contains a particularly useful 2024 first-person interview: a 27-year-old woman said that in ordinary offline socializing she might not especially care about some “hardware conditions”, but once the matchmaking app required many attributes to be filled in, she began hoping for someone whose conditions were somewhat better or at least similar.

Current source:

- Beijing Daily, 2024-04-09, `调查｜从“下一个更好”，到“把握好现在”，相亲者正在变化`  
  https://news.bjd.com.cn/2024/04/09/10742288.shtml

This is outside OWA's core period and is therefore **not** used to reconstruct a 2008 form. It is methodological evidence for why old profile forms matter.

A platform can make an attribute salient through:

```text
required field
+ fixed option list
+ search filter
+ result summary card
+ verification badge
+ ranking / recommendation use
```

Therefore later historians should preserve old form controls and option values, not only textual page copy.

---

## 6. `verification-state ambiguity`

The SEC filing makes an especially important distinction available:

```text
user asserted a value
!=
user uploaded / submitted evidence
!=
platform accepted that evidence
!=
platform marked the attribute as verified
!=
the person's broader profile is trustworthy
```

This matters because current or archived profile pages may visually display values without preserving how those values entered the system.

For a historical profile artifact, record verification at the **field** level if possible.

Avoid claims such as:

> “The site verified its users' education.”

Prefer:

> “The 2011 filing states that users could submit proof for attributes including education and receive higher profile rating after verification; this does not establish that every displayed education claim was verified.”

---

## 7. `current schema != historical schema`

The current live Jiayuan interface can still expose structured partner-search controls such as marital status, height and education.

That current page is useful only as a **locator / descendant representation**. It does not prove that:

- the same fields existed in 2003, 2005, 2008 or 2011;
- labels were identical;
- option categories were identical;
- fields had the same required / optional status;
- search ranking used them in the same way;
- the same verification rules applied.

Therefore:

```text
current field list
!=
historical field list
```

and:

```text
same label across years
!=
same semantics / validation / visibility / ranking role
```

A future M1 case should prefer cross-time field diffs over a single present-day screenshot.

---

## 8. Preservation failure mode: `form survival gap`

Matchmaking services expose several surfaces with very different archive probabilities:

```text
public homepage
public marketing article
press release
registration form
logged-in profile editor
search-result page
candidate profile
message inbox
payment / virtual-stamp dialog
verification upload flow
rank / recommendation output
historical database rows
```

Public homepages and portal news are relatively likely to survive. Logged-in dynamic forms, personalized result sets, message state and private candidate data are much less likely to be reproducible.

This note calls that asymmetry:

**`form survival gap / 表单存活缺口`**.

A related stronger loss is:

**`population-state loss / 人群状态丢失`**:

Even if a registration and search form survives perfectly, the historical candidate population usually does not. A 2008 user searching `北京 + 28–32 + 本科 + 未婚` saw a result set produced by the actual 2008 database, visibility rules, payment state and ranking system. Replaying the blank form today cannot recreate that social environment.

Therefore:

```text
historical search form recovered
!=
historical search results recovered
!=
historical partner market reconstructed
```

---

## 9. Minimum evidence record for a historical matchmaking form

For any future historical capture, record at least:

```text
site / platform
historical hostname
historical URL
capture_datetime
archive source
historical HTTP / replay state
charset evidence
browser / rendering notes
authentication state
page role (register / edit / search / result / profile / message / pay / verify)
form action
HTTP method
field_name
display_label
input_type
option_list
required/default
client validation
server validation if evidenced
visibility
searchability
sortability
editability
verification state / proof type
ranking effect if evidenced
price / access gate
result-page structure
dynamic requests / script dependencies
subresource completeness
unknowns
```

Unknown must remain `unknown`.

Do not infer backend ranking from visible HTML controls.

---

## 10. Hindsight risks

### Risk A: calling 1991 `电脑红娘` an Internet service

Do not. It is evidence of computerized matching before public Web dating, not evidence of browser use.

### Risk B: treating profile fields as neutral mirrors of society

A field may reflect pre-existing social categories, but making it mandatory / searchable / sortable changes its practical importance.

### Risk C: reading current UI backward

A current marital-status or education dropdown is not a 2008 artifact.

### Risk D: treating verification as binary platform-wide trust

Verification can be field-specific and optional.

### Risk E: equating registered account counts with people

Accounts can be inactive, duplicated, fake, abandoned or outside the target population.

### Risk F: assuming the archived form reconstructs the historical market

Without the historical database, results and ranking state remain missing.

---

## 11. Artifact status in this slice

### Achieved

- contemporaneous 2008 media evidence for professional matchmaking-site use, paid service and online-to-offline handoff;
- 2011 first-party SEC evidence for searchable database access, initial-message payment state, value-added ranking/search, mobile-browser access, and attribute verification rules;
- a concrete profile-schema / form evidence contract for future captures;
- explicit separation of self-asserted, submitted and verified attributes.

### Not achieved

This run did **not** obtain and inspect a qualifying historical capture of:

- Jiayuan registration / profile editor / search interface from 2003–2011;
- Baihe registration / personality test / search interface from 2005–2008;
- the 1998 `中国交友中心` early Web service;
- the same form at two historical dates for schema diff;
- a historical search-result page with verified capture time;
- historical HTML / raw bytes / charset / scripts / form actions for those cases.

Therefore:

**`M1 historical matchmaking-profile Web case: NOT ACHIEVED IN THIS SLICE`**.

This does **not** mean Wayback or another archive never captured them. It means this run has not inspected and verified such captures under `docs/METHOD.md`.

---

## 12. Next best artifact targets

The highest-value next work is not another essay about online dating. It is to obtain comparable historical interfaces:

1. Jiayuan registration + profile editor + search pages around 2003/2005/2008/2011;
2. Baihe registration / personality-test / search pages around 2005/2008;
3. `中国交友中心` around 1998–2000;
4. at least two timepoints from the same platform so field labels and option lists can be diffed;
5. if available, contemporaneous help / FAQ pages explaining verification and paid ranking;
6. raw HTML / WARC or equivalent rather than screenshots alone.

A useful future deliverable would be a machine-readable `profile_schema_diff` table:

```text
field
2005 label/options/state
2008 label/options/state
2011 label/options/state
source capture
confidence
```

That would let the repository show not just that “dating websites existed,” but **how the Web changed the set of life facts that strangers could filter each other by.**

---

## 13. What this changes about old-Web interpretation

The main conclusion is methodological:

> An old matchmaking profile form is not a disposable input page. It is a historical classification system for intimate life.

The Web did not invent status-conscious partner choice, and it did not invent structured matchmaking. What it changed was the scale and user-side executability of those categories: ordinary users could repeatedly query a large database, narrow strangers by standardized attributes, pay to alter visibility or communication state, and sometimes attach proof to selected fields.

For old-Web archaeology, the consequence is clear:

**preserve the schema, not only the page.**

If the option lists, verification states, searchability and ranking roles disappear, a visually intact homepage can still leave the most historically consequential part of the service unrecoverable.
