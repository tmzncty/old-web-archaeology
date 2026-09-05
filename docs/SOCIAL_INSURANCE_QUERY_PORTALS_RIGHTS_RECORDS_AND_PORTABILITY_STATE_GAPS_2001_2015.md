# Social-insurance query portals, rights records, and portability state gaps, 2001–2015

## Scope

This note stays inside the repository's Chinese old-Web scope. It does **not** attempt to write a global welfare-state history or extend the repository into present-day government apps.

The object is narrower:

> How did Chinese Web interfaces begin to expose social-insurance / medical-insurance records to individuals, and what can an archived query page actually prove about the underlying administrative state?

The life-history interpretation lives mainly in:

- `tmzncty/how-people-lived/topics/social-insurance-portability-record-continuity-and-protection-across-mobility-china-1995-2026.zh-CN.md`

This file focuses on interface, backend-state, temporal, identity, portability, and archive gaps.

## Why this belongs in old-web archaeology

A social-insurance website is not merely a page carrying information. It is a **control / observation surface over a private administrative database**.

That makes it unusually easy to overclaim from an archive.

An archived page can preserve:

- agency branding;
- help text;
- login fields;
- query categories;
- password instructions;
- links to policy documents;
- maybe a rendered account result if it was public/cached accidentally.

It usually cannot preserve:

- the authenticated citizen account;
- the exact database snapshot queried at that moment;
- employer contribution reports not yet posted;
- fund-accounting state;
- inter-agency transfer messages;
- a later correction;
- the person's real eligibility for benefits at the moment of use.

Therefore the central rule is:

> **query surface survives much more easily than rights state.**

## Historical anchors

### 2001: Shanghai social-security card and citizen-service information system

Shanghai's 2001 `社会保障卡管理办法` defined the social-security card as an IC card used for personal social affairs including employment, social insurance, social assistance, preferential treatment, and provident-fund loan matters.

A related municipal rule described a unified `社会保障和市民服务信息系统` supporting those affairs.

This provides A-grade evidence for an important precondition of later Web service:

- a machine-readable personal identifier / card;
- administrative systems capable of associating multiple public-service records with an individual;
- a municipal information infrastructure that existed independently of any particular Web front end.

It does **not** prove that all those records were already queryable over the public Web in 2001.

Sources:

- Shanghai municipal government, 2001 social-security card rule: <https://www.shanghai.gov.cn/nw26170/20200820/0001-26170_27370.html>
- Shanghai municipal government, 2001 citizen-service information-system rule: <https://www.shanghai.gov.cn/nw4093/20200813/0001-4093_21.html>

## 2005 account-query incident: an unusually strong ordinary-user trace

A 2006 *Southern Weekly* investigation preserved a detailed account of retired Shanghai accountant Zhang Tiebiao's use of the Shanghai Medical Insurance Bureau's Web service.

The report states that on **2005-05-24** he logged into the bureau-run medical-insurance site and inspected his personal medical-insurance account. He compared the displayed monthly contribution information with his retirement date and wage records and found a missing final pre-retirement contribution.

The same report says that when he returned to the account two days later, some displayed monthly figures had shifted.

Source:

- *Southern Weekly*, mirrored by Sina, 2006-11-02: <https://finance.sina.com.cn/g/20061102/10583043325.shtml>

This is valuable because it gives more than a generic statement that "online query existed". It preserves:

- a user;
- a query date;
- a purpose;
- a named account section (`个人账户清算信息` in the report);
- an observed discrepancy;
- repeat access;
- changed display state;
- offline cross-checking against wage records and regulations;
- subsequent telephone / administrative escalation.

### What it proves

It is strong B+/near-contemporaneous evidence that by 2005 a Shanghai insured person could use a bureau-run Web interface to inspect individual medical-insurance account information.

It also proves that displayed administrative data could be **contested and revised**.

### What it does not prove

It does not by itself reveal:

- original URL;
- charset;
- DOM;
- form method/action;
- password/cookie/session implementation;
- whether the account page was rendered server-side or through client script;
- database schema;
- whether a displayed month's number represented contribution month, posting month, accounting month, or a later normalization layer;
- whether the changed display reflected database repair, presentation remapping, or another backend process.

## Core state chain

For an authenticated social-insurance query, preserve at least the following independent states:

```text
real person
  -> administrative identity
  -> local social-insurance identifier / card
  -> insurance enrollment
  -> employer / individual declaration
  -> contribution paid
  -> contribution accepted by collection system
  -> contribution posted to rights record
  -> accounting / fund state
  -> Web account entitlement
  -> credential / password state
  -> login session
  -> query request
  -> backend dataset snapshot
  -> rendered query result
  -> citizen interpretation
  -> offline proof / dispute
  -> later correction or transfer
```

Never collapse this into:

```text
website says X -> X was unquestionably the legal/financial state
```

## State gaps

### 1. enrollment / contribution gap

A person can be enrolled while the current month's contribution has not yet been paid or posted.

`account exists != current contribution settled`

### 2. employer-declaration / rights-posting gap

An employer may have submitted a declaration while the individual's rights record is not yet updated.

The exact historical posting delay must be evidenced for the city/year; do not infer it from modern systems.

### 3. payment / display gap

Money can have been deducted from payroll without appearing in the public query result at the same moment.

The 2005 Shanghai case is a warning that display chronology and payroll chronology may differ.

### 4. accounting-month / lived-month gap

A screen field labeled with a month may represent a posting/accounting period rather than the month the worker thinks the deduction belongs to.

Do not map month labels to lived employment chronology without documentation.

### 5. query-result / legal-right gap

A rendered result is evidence about what the interface returned, not automatically the final legal interpretation of the person's entitlement.

### 6. query-result / fund-state gap

The front-end record does not expose the complete underlying fund accounting.

A balance line is not a full audit trail.

### 7. current-page / historical-interface gap

A modern government page preserving an old rule is not evidence that today's page structure existed when the rule was issued.

### 8. card / Web-account gap

Possessing a social-security card does not prove Web access had been activated, a password existed, or the citizen knew how to query online.

### 9. identity / credential gap

A card number, citizen ID, social-security number, username, and Web password can be separate identifiers/credentials with different lifetimes.

Do not infer the authentication scheme from current guidance.

### 10. local-account / national-portability gap

A city can provide excellent online visibility into a local account while cross-province transfer remains procedurally difficult.

`local queryability != national portability`

### 11. legal-portability / data-portability gap

The 2009/2010 pension-transfer rules created a legal right / procedure for cross-province transfer, but this does not prove that all local systems immediately exchanged records through one national real-time network.

### 12. transfer-request / transfer-completion gap

A submitted transfer request is not proof that the outgoing record, incoming record, funds, and accumulated years were all reconciled successfully.

### 13. record-transfer / service-usability gap

Pension record transfer and the ability to use medical-insurance treatment in another place are different state machines.

Never use one as evidence for the other.

### 14. displayed-continuity / actual-continuity gap

A screen that shows many historical months does not prove there were no coverage interruptions elsewhere or in another insurance scheme.

### 15. archived-login-shell / authenticated-state gap

A Wayback capture of the login shell cannot replay the private session, account database, or legal state.

This is a hard stop condition unless an authenticated transaction was separately and lawfully preserved.

## 2009–2010: portability policy becomes an information-system problem

The State Council's 2009 temporary measures on transfer and continuation of basic pension insurance took effect on 2010-01-01. They applied to participants including migrant workers and stated that pension relationships should transfer when workers moved across provinces, while contribution years and individual-account amounts would be accumulated according to the policy.

Official / primary policy:

- Ministry of Human Resources and Social Security: <https://www.mohrss.gov.cn/yanglaobxs/YLBXSzhengcewenjian/201610/t20161017_257400.html>

A contemporaneous *China Youth Daily* survey is especially useful for Web history. One worker said he learned from a **QQ pop-up news window** that pension insurance could now be transferred. In the same 1,971-person online survey, 81.5% wanted a nationally unified electronic social-security platform.

Source:

- *China Youth Daily*, 2010-01-05: <https://zqb.cyol.com/content/2010-01/05/content_3013186.htm>

This gives us two separate Web-mediated states:

```text
policy exists
  -> news is distributed through a commercial IM/news surface
  -> worker learns policy exists
  -> worker attempts administrative action
```

and:

```text
legal transfer rule exists
  -> users perceive fragmented data/service systems
  -> demand for national electronic platform
```

Do not collapse policy publication, policy awareness, platform integration, and successful transfer.

## 2013 Beijing: multi-channel rights-record query and verification

A 2013 Beijing social-insurance notice standardized individual-rights-record queries. It listed several channels:

- social-insurance agencies;
- self-service terminals;
- Beijing Social Insurance Online Service Platform;
- 12333 telephone service (planned in the notice for 2014 use in this query context).

Registered personal Web users could request records, and printable records used serial / verification codes for later authenticity checking.

Source:

- Beijing Human Resources and Social Security Bureau, 京社保发〔2013〕45号: <https://rsj.beijing.gov.cn/yltc/sbzytzx/202311/t20231101_3292116.html>

This introduces another state chain:

```text
rights record
  -> user requests standardized representation
  -> electronic / paper representation generated
  -> serial + verification code
  -> third party checks representation
```

Therefore add:

### 16. record / representation gap

A printable rights statement is a generated representation of the administrative record, not the record itself.

### 17. representation / verification-window gap

A verification code can have its own time window and validity state. A statement can remain as a paper artifact after its online verification window expires.

### 18. third-party-verification / holder-identity gap

Successful verification of a statement proves properties of the issued representation; it does not automatically prove that the presenter is the lawful subject unless identity binding is also checked.

### 19. channel-equivalence gap

Web, self-service terminal, phone, and counter may expose different fields, refresh cycles, and authentication requirements.

Do not assume they were interchangeable because one policy document lists them together.

## Public Web archive asymmetry

Social-insurance portals create an extreme preservation asymmetry:

### Likely to survive publicly

- policy pages;
- agency homepages;
- login shells;
- help pages;
- password instructions;
- public service catalogues;
- screenshots in newspapers;
- notices describing query fields;
- downloadable blank forms.

### Unlikely / improper to survive publicly

- identifiable individual account pages;
- contribution histories;
- medical-treatment records;
- authenticated session cookies;
- identity numbers;
- transfer transaction logs;
- backend reconciliation records.

This is not merely an archival failure. Much of the missing material **should have been private**.

Therefore:

> **privacy-protecting systems naturally produce a public archive with strong control-surface bias.**

A responsible archaeology must not compensate for that bias by exposing surviving personal identifiers.

## Privacy and safety stop conditions

1. Do not publish full identity-card numbers, social-security numbers, card numbers, passwords, verification codes, medical details, or account balances tied to an identifiable ordinary person.
2. Do not attempt login or password recovery against historical accounts.
3. Do not test whether old credentials or identity-number patterns still work on current government systems.
4. Do not treat leaked/private account screenshots as preferred evidence when public policy/interface documentation suffices.
5. If a historical screenshot contains personal identifiers, redact them in derived artifacts unless the identifier is already a clearly public official/test value and preservation is necessary.

## Capture status in this research pass

### Verified historical capture

None acquired to the repository's M1 standard in this pass.

### What was acquired instead

- A-grade municipal and national policy texts describing card/information-system and query arrangements.
- Near-contemporaneous reporting describing an actual 2005 authenticated Shanghai user session and named query fields.
- 2010 contemporaneous reporting connecting a portability-policy announcement to QQ news delivery and user demand for a national electronic platform.
- 2013 official Beijing documentation of Web / terminal / phone / paper rights-record query channels and verification.

### Therefore still unknown

For the 2001–2006 Shanghai public Web interface:

- original URL(s);
- historical DNS/host ownership at specific dates;
- charset;
- browser requirements;
- frames / tables / script structure;
- login form fields;
- password initialization flow;
- cookies / session mechanism;
- query endpoint;
- result-page DOM;
- refresh schedule;
- exact database relationship between displayed medical-account entries and fund accounting.

A search-engine locator or a modern page mentioning an old hostname is **not** enough to mark these as known.

## Archaeological experiment plan

When a candidate memento is obtained, record at minimum:

1. original URL;
2. archive URL;
3. capture datetime;
4. redirect chain;
5. HTTP status where available;
6. declared / detected charset;
7. title and agency branding;
8. form fields without submitting real credentials;
9. method/action if visible in preserved HTML;
10. JavaScript / ActiveX / applet / plugin dependencies;
11. missing images / CSS / script resources;
12. whether login points to live or archived backend;
13. whether any query action would require private credentials (stop rather than test);
14. contemporaneous independent evidence that the hostname belonged to the agency at that date.

The experiment's success criterion is **interface reconstruction**, not transaction replay.

## Evidence grading

### A — official / primary administrative text

- 2001 Shanghai social-security card rule.
- 2001 Shanghai citizen-service information-system rule.
- 2009 pension-transfer policy and implementation documents.
- 2013 Beijing rights-record query notice.

### B+ — contemporaneous / near-contemporaneous user-operation evidence

- 2006 *Southern Weekly* investigation reconstructing Zhang Tiebiao's 2005 online medical-account inspection with dates, field names, repeated access, and offline corroboration.
- 2010 *China Youth Daily* contemporaneous survey / named worker describing policy discovery through a QQ news pop-up.

### C / locator evidence

- modern insurance-help pages or search results that repeat historical hostnames without a validated historical capture.

These can guide archive searching but cannot establish historical DOM or behavior.

## Hindsight risks

- Do not call a 2001 IC-card system a modern “app account.”
- Do not infer nationwide data integration from a city portal.
- Do not infer real-time posting from the ability to query online.
- Do not infer that a policy-effective date equals software deployment date.
- Do not infer that today's password / face-recognition / mobile authentication existed on the old site.
- Do not treat a corrected later screen as evidence that the earlier display “never existed.” Both can be historically real interface states.
- Do not infer pension portability from medical-insurance UI, or vice versa.

## What this changes about Chinese old-Web history

Government and public-service Web history is not only about putting forms and regulations online.

By the mid-2000s, at least some ordinary users could use a Web interface to inspect a private administrative record and challenge the institution by comparing that record with payroll and law.

That creates a historically important new relation:

> **the citizen is no longer only the object recorded by the database; the citizen can become a reader and auditor of the database's representation of them.**

At the same time, the archive preserves this relation very unevenly. We can often recover the shell that said “个人账户查询,” while the personal record, database version, reconciliation transaction, and downstream real-world result remain correctly inaccessible.

That asymmetry must be treated as part of the history, not patched over with speculation.
