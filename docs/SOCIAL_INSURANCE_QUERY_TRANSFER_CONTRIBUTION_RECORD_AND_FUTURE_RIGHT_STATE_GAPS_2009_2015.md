# SOCIAL_INSURANCE_QUERY_TRANSFER_CONTRIBUTION_RECORD_AND_FUTURE_RIGHT_STATE_GAPS_2009_2015.md

Status: research note / state-model extension  
Scope: Chinese social-insurance Web/public-service interfaces within the repository's c.1995–2015 scope, centered on **basic pension contribution records and cross-province transfer after the 2009 rules**.  
Cross-link: `tmzncty/how-people-lived/topics/retirement-as-a-life-stage.md`.

This note asks a narrow old-Web question:

> When a worker changed employer or city, what historical Web artifact could prove that years of pension contributions actually survived the move?

The answer is usually: **far less than a surviving public help page appears to prove**.

A public page can preserve rules, forms and navigation. The life-changing state — the worker's authenticated contribution ledger, transfer request, agency-to-agency information exchange, fund reconciliation and destination write — is mostly private backend state and is systematically underrepresented in public Web archives.

That makes social insurance an unusually useful case for separating:

- visible Web interface;
- authenticated user state;
- agency workflow;
- fund movement;
- durable future entitlement.

---

## 1. Research units

Do not collapse the following into one object:

- **policy document** — legal or administrative rule describing eligibility and procedure;
- **public service site / host** — local labor/social-security portal;
- **public help page** — instructions, FAQ, downloadable form or service directory;
- **login / authentication page** — entry point to personalized services;
- **personal-rights query** — authenticated display of contribution or benefit information;
- **contribution record** — backend history associated with one insured person's identity;
- **transfer certificate** — document summarizing contribution participation before a move;
- **transfer application** — request to continue the pension relationship in another locality;
- **agency contact message / letter** — destination-to-origin workflow state;
- **transfer information table** — origin agency's structured pension history for transfer;
- **fund transfer** — movement of the transferable pension funds;
- **destination account write** — contribution history and amounts entered into the new locality's record;
- **completion notification** — state exposed back to employer/worker;
- **archive capture** — a preserved public representation of any one of these objects;
- **claim** — the minimum historical conclusion supported by evidence.

A preserved login page is not a preserved contribution ledger. A preserved transfer guide is not a completed transfer.

---

## 2. Institutional prehistory: the durable record predates the Web interface

The 1997 State Council decision on a unified enterprise-worker basic pension system described a system combining social pooling and individual accounts and required personal pension accounts for covered workers.

Source (official government-gazette reproduction):

- State Council, `国发〔1997〕26号`, 1997-07-16: https://www.nmg.gov.cn/zwgk/zfgb/1997n_5293/199709/199707/t19970716_309391.html

This is **prehistory**, not evidence that ordinary workers had an Internet pension account in 1997.

The distinction is fundamental:

```text
backend administrative record exists
≠ worker can inspect it remotely
≠ worker can correct it online
≠ record can move across local systems
```

The Web entered a longer history of pension administration; it did not create the pension record itself.

---

## 3. 2009–2010 cross-province transfer created an explicit multi-system state machine

At the end of 2009, the Ministry of Human Resources and Social Security issued implementation material for the national cross-province pension transfer rules. The trial handling procedure took effect on **2010-01-01**.

Primary/official source:

- MOHRSS, `人社部发〔2009〕187号`, 2009-12-30: https://www.mohrss.gov.cn/yanglaobxs/YLBXSzhengcewenjian/201610/t20161017_257400.html

The official handling procedure is unusually valuable for Web archaeology because it exposes the hidden stages that a public "transfer pension" button would otherwise compress.

### Canonical administrative chain

```text
old locality contribution history
→ contribution certificate requested
→ certificate issued
→ worker enrolls in destination locality
→ transfer application submitted
→ destination agency checks eligibility
→ destination agency sends contact letter
→ origin agency verifies history
→ origin agency generates transfer-information table
→ origin agency transfers funds
→ origin agency sends information
→ destination agency receives information + funds
→ destination agency reconciles amount and history
→ destination account is updated
→ worker/employer is notified
```

The trial rules specify multiple 15-working-day handling windows rather than a single atomic transaction.

They also distinguish **information** from **funds**: the destination agency is to complete continuation after receiving the transfer-information table **and** the transferred fund, check both, then record the amounts and supplement the person's information.

This yields the first hard boundary:

> **transfer requested ≠ transfer accepted ≠ information sent ≠ money sent ≠ destination ledger written**

---

## 4. Networked administration and public Web service are not the same layer

The 2009 implementation notice explicitly said that local agencies already connected to the national `金保工程` should adjust systems so pension-transfer business could exchange information electronically with the ministry's inter-regional system; places not yet connected could temporarily use paper procedures while building their local systems.

This provides a useful three-layer distinction:

1. **agency network connectivity**;
2. **public Web information / service pages**;
3. **authenticated individual transaction state**.

The existence of layer 1 does not prove layer 2 or 3. A worker could be using a counter and paper certificate while agencies exchanged some state electronically behind the scenes.

Likewise, a public Web portal could explain the process while the decisive transfer still occurred through agency systems invisible to the user's browser.

---

## 5. Shanghai 2010 shows a hybrid public-service environment, not a fully Web-native pension route

Shanghai's Human Resources and Social Security Bureau's **2010 government-information disclosure annual report** is strong contemporaneous institutional evidence for the service environment.

Source:

- Shanghai Municipal Government, 2010 HRSS annual report: https://www.shanghai.gov.cn/nw25513/20200820/0001-25513_25128.html

The report says:

- the bureau published major social-insurance information on its government website;
- its portal's most popular areas included **便民服务**, **信息公开** and **办事大厅**;
- 2010 saw more than **19.87 million** calls to the 12333 telephone hotline;
- the hotline also handled email, card inquiries, loss reporting and other service tasks;
- the bureau launched a trial **12333在线智能咨询** service;
- online service pages exposed conditions, agencies, procedures, required materials and downloadable forms;
- the bureau also used in-person, telephone, email, Web, newspaper and printed channels together.

The report also says Shanghai formulated implementation opinions in 2010 for pension and medical-insurance relationship transfer for mobile workers.

This is evidence for a **hybrid service stack**:

```text
public Web information
+ downloadable forms
+ online consultation
+ telephone hotline
+ counter
+ agency backend
```

It does **not**, by itself, prove that a Shanghai worker in 2010 could complete the whole pension transfer through a browser.

### Why this matters for old-Web reconstruction

A modern observer may see a historical government portal and assume:

> "The service was online."

The historically safer question is:

> **Which stage was online?**

Possible answers include only policy lookup, only form download, only appointment/consultation, only authenticated query, only application submission, or full transaction execution. These are different claims.

---

## 6. A social-insurance record is a changing state, not a static page

A worker's pension history can be represented as:

```text
employer establishes participation
→ employer reports wage/contribution basis
→ contribution obligation generated
→ money paid
→ agency accepts payment
→ payment posts to worker identity
→ personal-rights record reflects the month
→ worker queries/receives statement
→ mismatch may be noticed
→ correction process may begin
```

Therefore a historical screenshot showing "insured" does not prove every expected month was posted correctly.

### State gaps

#### `employer-report gap`

Employer has submitted or claims to have submitted data, but agency state is unknown.

#### `payment-posting gap`

Money has been paid or deducted, but the worker's personal ledger has not yet been updated or cannot be proven updated.

#### `identity-binding gap`

A contribution exists in a system, but whether it is bound to the correct individual record is unresolved.

#### `authenticated-ledger gap`

A public portal survives, but personalized contribution rows required authentication and are absent from public archives.

#### `statement-snapshot gap`

A mailed/printed/Web statement is only a snapshot at one time; later correction or transfer may change the administrative state.

#### `record-correction gap`

A mismatch is visible, but the archive rarely preserves whether the correction request succeeded.

---

## 7. Transfer has additional state gaps

The 2009 procedure motivates a second group of explicit gaps.

### `certificate-issuance gap`

The user asks for a contribution certificate; whether the certificate was issued and what history it contained are separate facts.

### `transfer-application gap`

A transfer form exists or is submitted; eligibility and acceptance are still unknown.

### `agency-contact gap`

Destination agency accepts the application, but whether the origin agency actually receives/processes the contact request is separate.

### `information-table gap`

The origin agency has a record but may still need to create the formal transfer-information table.

### `fund-transfer gap`

Information can move without proving the associated transferable fund has arrived.

### `information/fund reconciliation gap`

The destination may possess both artifacts but still need to verify they match.

### `destination-write gap`

Reconciled state has not yet been written into the worker's destination pension account.

### `completion-notification gap`

Backend completion exists, but whether the worker knows it is separate.

The strongest old-Web claim should therefore stop at the exact preserved state.

---

## 8. Interruption is not the same as erasure

The national rules explicitly preserve an important negative state: for some migrant workers who interrupt employment or return home, the existing pension relationship and contribution record are retained rather than deleted; later contribution years can accumulate with the earlier record.

For historical-Web research, this means absence of a new contribution row during a gap should not be read as account death.

Useful states include:

- active contribution;
- inactive but retained relationship;
- temporary account;
- transfer pending;
- transferred out;
- transferred in;
- terminated under an allowed termination rule;
- unknown.

Do not collapse all non-active accounts into "closed".

---

## 9. Contemporaneous reporting shows why backend completion mattered to real mobility

A 2009 contemporaneous report described migrant worker Wang Hongfei moving from Shenyang to Suzhou in late 2008 and successfully transferring two years of prior social-insurance history to his new job.

Source:

- 2009-04-15 report: https://business.sohu.com/20090415/n263403563.shtml

This should be used as **B-grade contemporaneous personal evidence**, not proof of national prevalence. It shows that transfer was a real life-route concern before national standardization.

A 2010 CCTV investigation, reproduced by Sina, provides the opposite case: footage and reported Shenzhen bureau figures described very large numbers of migrant workers surrendering pension relationships before the national transfer rule, with transfers far rarer than surrender in the cited 2007 figures.

Source:

- 2010-01-11: https://news.sina.com.cn/c/sd/2010-01-11/233319445992_2.shtml

The historical point is not that every surrendered account represented the same motive. It is that:

> **a mobile worker's pension state could terminate as part of leaving a city.**

The 2009–2010 transfer architecture was therefore not merely a website convenience. It changed whether a future-right record could survive geographic mobility.

---

## 10. Policy completion and system completion diverge

In 2016 MOHRSS stated that the 2009 transfer system had generally operated smoothly, but also listed continuing difficulties involving historical contribution information, temporary accounts, one-off payments, duplicate pension receipt and other edge cases.

Source:

- MOHRSS, 2016-12-02: https://www.mohrss.gov.cn/wap/xw/rsxw/201612/t20161202_261000.html

This is outside the main 2009–2015 evidence window by one year, so treat it as a **near-post-period audit** of the system created during the repository's scope.

It directly blocks a common overclaim:

> `national transfer rule exists ≠ all historical records became interoperable`

---

## 11. What public archives are structurally likely to preserve

For social-insurance services, a public Web archive is relatively good at preserving:

- policy pages;
- service directories;
- public FAQs;
- downloadable forms;
- office addresses and phone numbers;
- public login shell;
- JavaScript/CSS if not blocked;
- sometimes browser requirements or help text.

It is structurally poor at preserving:

- authenticated personal contribution histories;
- identity-verification state;
- employer reporting state;
- private correction requests;
- inter-agency messages;
- transfer-information tables containing personal data;
- fund movement;
- destination-ledger writes;
- notification histories.

This is not only an accidental archive failure. Much of the missing state **should not have been public in the first place**.

Therefore social-insurance Web archaeology has a built-in privacy-shaped absence.

---

## 12. Privacy is a positive research constraint, not a gap to defeat

Do not attempt to "complete" the historical record by:

- logging into old individual accounts;
- testing historical ID numbers or social-security card numbers;
- searching leaked databases;
- correlating old contribution records with current identities;
- republishing names plus detailed contribution histories;
- recovering passwords or security answers.

Preferred evidence:

- official process documents;
- public help pages;
- anonymized or already-published contemporaneous case descriptions;
- system manuals without personal data;
- screenshots with personal fields removed, if legally available;
- aggregate reports.

The absence of authenticated ledgers should be recorded as a **privacy/architecture boundary**, not treated as a challenge to bypass.

---

## 13. Browser and authentication uncertainty

This run did **not** recover and validate a 2009–2012 authenticated historical personal-pension query session from a major locality such as Beijing, Shanghai or Shenzhen.

Therefore do not infer from current portals:

- historical URL paths;
- login identifiers;
- password rules;
- certificate/ActiveX requirements;
- IE version requirements;
- charset;
- DOM structure;
- whether contribution records were server-rendered or loaded dynamically;
- whether a query page exposed all backend state;
- whether transfer status was available to the worker online.

A current government page may help locate terminology, but it cannot substitute for a verified historical capture.

This is a formal negative result for the present slice.

---

## 14. After-scope continuation: 2019 shows what later centralization made visible

This repository's main object remains Chinese old Web c.1995–2015. The **2019 national social-insurance public-service platform** is included only as an after-scope comparison that makes earlier missing state easier to understand.

On 2019-09-15 the national platform formally launched after trial operation. Official material said logged-in users could:

- query multi-location social-insurance contribution/benefit-rights information in a centralized display;
- estimate pension treatment from current contribution information;
- inspect transfer-service progress;
- access local service halls from the national portal.

Sources:

- https://www.cac.gov.cn/2019-09/16/c_1570162534774260.htm
- https://www.cac.gov.cn/2019-09/17/c_1570248598382143.htm
- https://chinajob.mohrss.gov.cn/h5/c/2019-09-09/127635.shtml

Do **not** use this 2019 interface to reconstruct a 2010 interface.

Its value is analytical: it demonstrates that a later system explicitly tried to expose states — multi-locality history, calculation and transfer progress — that were much harder for one worker to see as a unified ledger in the earlier period.

---

## 15. Cross-repository life-history interpretation

The `how-people-lived` side should treat pension history as a second biography running under the visible job biography:

```text
job A
→ contribution history A
→ move / interruption
→ record retained, surrendered or transferred
→ job B
→ contribution history B
→ reconciliation
→ eventual benefit eligibility
```

The old-Web side asks a narrower question:

> **Which of those states could a historical browser session actually reveal?**

This is a useful general pattern for other institutional life-course systems:

- school records;
- medical records;
- housing applications;
- public-benefit eligibility;
- tax accounts;
- professional credentials.

The visible webpage is often only a window onto a longer institutional memory.

---

## 16. Evidence grades for this note

### A — contemporaneous / official

- 2009 MOHRSS implementation notice and handling procedure;
- Shanghai HRSS 2010 government-information-disclosure report;
- official policy/process documents within the period.

### B — contemporaneous reporting

- 2009 Wang Hongfei transfer case;
- 2010 reporting on Shenzhen surrender/transfer practices.

### B/A continuation, outside main scope

- 2016 MOHRSS audit/repair of transfer rules;
- 2019 national platform announcements.

### D — researcher synthesis

- the explicit state-gap taxonomy in this note;
- interpretation of authenticated-state loss as a structural archive problem;
- `public page → private ledger → agency workflow → future right` model.

D-level terms must not be mistaken for historical administrative vocabulary.

---

## 17. Claims this note can support

- By 2009–2010, cross-province enterprise-worker pension transfer was formally modeled as a multi-step exchange of certificate, request, agency information and funds rather than one instantaneous action.
- Local public-service Web, telephone and counter channels coexisted; "government service was online" is too coarse a claim.
- Public Web archives are structurally unlikely to preserve the authenticated state required to prove a particular worker's contribution history or completed transfer.
- A transfer rule can exist while historical-data and special-account problems still impede actual execution.
- Social-insurance records are an example of institutional memory whose continuity can materially affect migration and job change.

## 18. Claims this note does **not** support

- that all workers could query complete pension histories online in 2010;
- that any specific 2010 local portal used today's authentication or UI;
- that a Web application meant the transfer completed;
- that contribution deduction guaranteed correct posting;
- that every migrant-worker surrender represented voluntary preference;
- that the 2019 national portal accurately represents 2009–2015 browser experience;
- that an archived public page can establish an individual's eventual pension entitlement.

---

## 19. Next evidence targets

Highest-value targets are deliberately narrow:

1. a verified 2009–2012 capture of a local social-security service directory that clearly distinguishes public information, authenticated query and transaction submission;
2. contemporaneous user manuals for local pension contribution-query systems;
3. historical browser/security requirements for an authenticated local social-insurance portal;
4. public documentation of contribution-statement delivery: mailed statement, self-service terminal, telephone, Web or counter;
5. anonymized contemporaneous evidence of a missing contribution month being discovered and corrected;
6. a longitudinal published case with at least two city moves showing certificate → application → destination completion.

Stop if the only way to resolve a gap would require recovering private individual account data.

---

## 20. Research takeaway

The most important archaeological distinction is:

> **a pension Web page is not a pension right.**

The right is a long-lived state distributed across identity records, contribution history, agency databases, transfer information and funds. The Web may expose one slice of that state, but a historical capture normally preserves only the slice — not the future itself.
