# Graduate employment agreement, dispatch, report-card, archive and destination state gaps, China 2004–2015

## Scope

This is a **Chinese old-Web companion**, not a general history of Chinese graduate employment.

The primary window is c. 2004–2015, when university and provincial employment websites increasingly mediated:

- authenticated graduate identity;
- electronic recommendation forms and résumés;
- employer qualification/registration;
- online recruitment;
- employment agreements / `三方协议`;
- dispatch (`派遣`);
- reassignment (`改派`);
- temporary holding states such as `暂缓就业`;
- archive (`人事档案`) routing;
- hukou-routing information;
- report-card (`就业报到证`) processing.

Pre-2004 institutional background and post-2015 electronic-report-card / national destination-registration developments are boundary context only. They belong primarily in `how-people-lived` rather than expanding this repository indefinitely.

Cross-project companion:

- `tmzncty/how-people-lived/topics/graduation-routing-three-party-agreements-report-cards-archives-and-status-windows-china-1997-2026.zh-CN.md`

## Why this belongs in old-Web archaeology

A historical graduate-employment website is easy to misread as an ordinary information site.

In practice, by the mid-2000s some such systems were **transactional control planes** connecting student records, employers, universities and provincial employment authorities. A page could be only the visible layer of a much larger state machine whose consequences happened later through printers, sealed archives, confidential post, police registration, employer HR offices and physical report-in.

Therefore:

> `historical page survives != historical transaction survives`

and:

> `student clicked submit != graduate's life-course route completed`

This case is useful because it makes several archive gaps unusually explicit.

---

## 1. Evidence contract

Repository method applies without exception:

- platform / host / account / page / capture / claim remain distinct;
- `exists`, `available`, `used`, `popular` and `caused` must not be collapsed;
- a current official page carrying 2008-dated text is **not automatically a verified 2008 capture**;
- an old URL mentioned by a notice is a locator, not proof that the original endpoint has been inspected;
- an administrative record is evidence of a recorded state, not automatically evidence of actual employment.

### Grades used here

- **A-content**: official/institutional historical-dated content whose current provenance is clear, but whose historical Web capture has not been verified in this slice.
- **A**: contemporaneous official announcement/text where the artifact itself is sufficiently identifiable.
- **B**: contemporaneous or near-contemporaneous media/technical observation.
- **C**: later recollection; not used for precise UI claims here.
- **D**: researcher state-machine reconstruction; always explicit.

---

## 2. Baseline: the Web can expose an institution-bound student identity

### Beijing online graduate job fairs, 2004

A contemporaneous report about Beijing's 2005-graduate online job fairs described a verification path:

1. graduate-school-status data were imported into the employment site;
2. a student activated the record;
3. the student completed an electronic recommendation form consistent with the paper recommendation form;
4. the university verified the electronic form.

Evidence:

- 2004-11-23, contemporaneous media report:
  https://edu.sina.com.cn/l/2004-11-23/92301.html

**Grade: B.**

Supported narrow claim:

> By late 2004, at least one Beijing graduate-employment Web workflow linked online job-fair participation to pre-existing student-status data and university verification.

Not supported:

- that all Beijing graduates used it;
- that the historical site UI is recoverable from this article;
- that the electronic record by itself created a legal employment relationship.

### State gap introduced

`person is a graduating student`

is not the same as

`person possesses an activated employment-system identity`.

Call this the **student-status / Web-account gap**.

---

## 3. Shandong 2005–2006: employment transaction moves onto the Web

On 2005-10-21/22 the Shandong graduate employment information network (`www.sdbys.cn`) was announced as operational. Contemporaneous reporting said that from 2006, graduates employed within the province would cease using paper employment-agreement forms and would process agreement signing, dispatch and reassignment online. The network was described as spanning 17 cities, 140 counties/districts and roughly 270 colleges, with recruitment and remote-interview functions as well.

Evidence:

- 2005-10-22, Qilu Evening News / Sina:
  https://news.sina.com.cn/c/2005-10-22/07457234216s.shtml
- 2005-10-22, Life Daily / Sina:
  https://news.sina.com.cn/c/2005-10-22/09087234857s.shtml
- 2005-08-15, CERNET reporting on the planned launch:
  https://www.edu.cn/xxh/fei/xin_xi_zi_xun/200603/t20060323_135329.shtml

**Grade: B, two closely related media families plus an education-network report.**

### Important narrow conclusion

This is stronger than evidence for a job-board feature.

The contemporaneous descriptions explicitly place **agreement, dispatch and reassignment** in an online workflow. Therefore the Chinese Web by 2006 could participate directly in a state transition that later affected offline employment-administration routes.

But the following remain distinct:

`online agreement created`

`graduate accepted it`

`employer status validated`

`university accepted it`

`provincial dispatch state updated`

`report-card state created`

`archive route created`

`archive physically sent`

`archive physically received`

`graduate actually reported to employer`

`graduate actually worked there`

No source in this slice justifies compressing these into one Boolean `employed=true`.

---

## 4. 2008 university notices expose the hidden state machine

Current official university pages carrying historical-dated content are exceptionally useful here. They preserve procedural language, deadlines, legacy URLs and sometimes authenticated-system locators.

They **do not** by themselves prove how the entire page rendered in 2008.

### 4.1 Sun Yat-sen University: an online choice can have a default physical route

A chemistry-school notice dated 2008-05-25 said graduates in specified states could apply for `暂缓就业` through the university employment-management system at:

`http://202.116.65.110/employ/login_student.aspx`

The notice further said the university would begin arranging archives and printing hukou-migration documents in early June. If a graduate had not registered `暂缓就业`, further study, overseas study or return-to-source status by the deadline, the archive would by default be sent to the home-source personnel bureau and a return-to-source hukou migration document would be printed.

Evidence:

- https://ce.sysu.edu.cn/zh-hans/article/1586

**Grade: A-content / historical capture unverified.**

This gives a particularly clear **default-route gap**:

`student has not selected a visible option`

!=

`system does nothing`

The institution may require a routable state and therefore execute a default branch.

### Privacy note

The current page contains names and student information for individuals who were difficult to contact. Those names are not needed for the historical claim and should not be reproduced in this repository.

### 4.2 Xiamen University: browser account + report card + confidential post + police office

A finance-department notice dated 2008-05-16 describes the employment report card as an important credential for employer report-in, personnel archive reception and hukou handling.

Evidence:

- https://finance.xmu.edu.cn/info/1007/1447.htm

A journalism-school notice dated 2008-06-20 says:

- graduate archives would be sent through the postal confidential-document channel (`机要文件通信站`);
- graduates should track whether the receiving institution got the archive;
- a postal trace was possible within one year;
- hukou migration had its own time requirement;
- the graduate could keep using the original account/password for the university graduate-employment website for one year after graduation.

Evidence:

- https://comm.xmu.edu.cn/info/1048/35032.htm

**Grade: A-content / historical capture unverified.**

The notice exposes at least four independent persistence domains:

1. employment Web account;
2. printed report/hukou papers;
3. sealed personnel archive;
4. postal transfer record.

A future historian can recover one while losing all the others.

---

## 5. Proposed transaction model (D reconstruction)

The model below is analytical. It must not be mistaken for the exact implementation of any single provincial system.

```text
student record exists in school SIS
        |
        v
employment-platform identity provisioned
        |
        v
account activated / authenticated
        |
        +-----------------------------+
        |                             |
        v                             v
search / recruitment              no confirmed job
        |                             |
        v                             +--> temporary-holding route
employer contact                        (`暂缓就业`, where available)
        |                             |
        v                             +--> further study / abroad
agreement proposed                   |
        |                             +--> return-to-source / second distribution
        v
student confirmation
        |
        v
employer sign / stamp / online acceptance
        |
        v
university verification
        |
        v
higher-level / provincial routing state
        |
        +--> dispatch / report-card state
        +--> archive destination
        +--> hukou destination / migration-paper state
        |
        v
papers / database record / route generated
        |
        v
archive physically sealed and sent
        |
        v
receiving institution accepts archive
        |
        v
graduate reports in
        |
        v
employment actually begins
        |
        v
possible later reassignment / job change
```

Every arrow is a potential evidence gap.

---

## 6. Named state gaps

### G1 — student-status / Web-account gap

A university has a record for a graduate, but the graduate may not have activated or successfully authenticated the employment account.

### G2 — account / usable-interface gap

Credentials can exist while the required browser, network, JavaScript, encoding, or endpoint is unavailable.

### G3 — opportunity / executable-employer gap

A company can offer work while lacking the required personnel/hukou/archive reception route for a particular graduate.

### G4 — online-intent / validated-agreement gap

A student clicking or entering an intended employer does not prove a three-party agreement was valid across all required parties.

### G5 — agreement / dispatch gap

A signed agreement does not automatically prove a final dispatch state was produced.

### G6 — dispatch-plan / report-document gap

A school or provincial system can have a dispatch plan before the graduate receives a report card or equivalent credential.

### G7 — report-card-issued / graduate-collected gap

The document may have been produced but never collected, mailed successfully or used.

### G8 — archive-route / archive-sent gap

A destination field is not a postal event.

### G9 — archive-sent / archive-received gap

The sender can record dispatch while the receiving personnel agency has not accepted or indexed the file.

### G10 — hukou-migration-paper / completed-hukou-transfer gap

Printing a migration paper does not prove the graduate later registered at the destination police authority.

### G11 — registered destination / actual-employment gap

This is central to life-history interpretation. A graduate can be recorded as signing, dispatching or reporting to an entity without sustaining actual employment there.

### G12 — employment-statistic / lived-work gap

Administrative employment categories can include signed agreements, contracts, flexible employment, further study and other states depending on the reporting rule. A published employment percentage cannot be reverse-engineered into a uniform set of ordinary lives without its denominator and category rules.

### G13 — temporary-holding / future-route gap

`暂缓就业` or archive retention proves that a route was kept open for a period; it does not prove the graduate later used that route successfully.

### G14 — account-validity / archive-validity gap

A student Web login might expire one year after graduation while a personnel archive must remain administratively meaningful for decades.

### G15 — help-page / authenticated-backend gap

An archived or surviving instruction page does not preserve the protected transaction database that actually generated dispatch states.

### G16 — frontend-era / backend-era gap

A current page can preserve 2008 text in a modern CMS template while the original 2008 backend has disappeared.

---

## 7. A first-person life-course stress test: Shanghai, 2008

A contemporaneous investigative report about graduate employment statistics included an out-of-town Shanghai graduate (referred to as “Xiao Wang” in the article). She wanted to stay with a magazine where she had interned, but before graduation the employer could not solve the hukou/archive reception issue. Her concern was that without an appropriate pre-graduation agreement, the school would route hukou/archive back to her home region and she could lose a more advantageous fresh-graduate route for remaining in Shanghai.

Evidence:

- 2008-01-10, `青年周末` article reproduced on Sina:
  https://edu.sina.com.cn/l/2008-01-10/1442140643.shtml

**Grade: B, contemporaneous interview.**

What it proves:

- at least one graduate experienced job choice, archive/hukou routing and fresh-graduate timing as one practical constraint bundle.

What it does not prove:

- the frequency of this experience;
- the exact backend state of her university system;
- that all Shanghai employers faced the same personnel constraints;
- that every failure to sign a three-party agreement meant no employment.

### Old-Web relevance

A reconstruction based only on the employment website could miss the actual blocking condition. The user might see a recruitment opportunity and even communicate online with the employer, while the decisive state exists in personnel/hukou administration outside the public Web.

Call this **transaction-backend dark matter**.

---

## 8. Administrative record versus lived employment: 2008–2009 counterevidence

A 2009 contemporaneous report on the phrase `被就业` documented a graduate who discovered a company on an employment agreement even though he said he had not known that employer. The story emerged through a forum post and was then investigated by mainstream media.

Evidence:

- 2009-07-27, People's Daily investigation reproduced by Sina:
  https://edu.sina.com.cn/j/2009-07-27/1050175130.shtml

**Grade: B.**

This does **not** establish a national rate of false employment records.

It does establish a crucial methodological rule:

> A historical employment-system row can be a real historical artifact and still fail to describe the graduate's lived work history.

For old-Web reconstruction, therefore, even a perfectly preserved authenticated page showing “signed” or an employer name would still require separate evidence before claiming actual work.

---

## 9. Historical visibility asymmetry

Graduate employment produces several record families with different survival probabilities.

### Likely institutionally durable

- student identity;
- diploma/degree status;
- some dispatch or destination records;
- personnel archive metadata;
- official annual employment statistics.

### Potentially fragile

- student account state;
- old password recovery mechanism;
- online employer invitations;
- draft electronic agreements;
- forum threads asking how to route an archive;
- email or QQ conversations with recruiters;
- temporary Web notices;
- browser-side form validation;
- exact failure messages;
- user uncertainty before final submission.

### Potentially invisible even when administratively important

- why a graduate selected a default route;
- whether family pressure drove the choice;
- whether an employer informally promised later hukou help;
- whether a graduate planned to change jobs immediately after dispatch;
- whether the student viewed the official destination as a paperwork solution rather than a future.

This produces an **administrative-survival bias**: the more successfully an institution records a state, the more likely a future historian is to mistake that state for the whole life.

---

## 10. 2008 legacy-page temporal collapse

The Sun Yat-sen and Xiamen University pages accessed today are useful but must be described carefully.

Supported wording:

> “A current official university page carries text dated 2008-05-25 describing an employment-management URL and deadline.”

Unsupported wording without a verified capture:

> “This is what the employment website looked like on 2008-05-25.”

Current templates, navigation, CSS, analytics and CMS metadata can be much newer than the historical body text.

### Specific locator worth future archive work

From the Sun Yat-sen notice:

`http://202.116.65.110/employ/login_student.aspx`

and linked historical employment-center URL(s).

The notice proves the locator was referenced by an official page carrying a 2008 date. It does not prove that a particular Wayback capture exists or has been inspected.

---

## 11. Browser and platform questions still unknown

For provincial and university systems of c. 2005–2010, this slice has **not** established:

- exact historical `Content-Type` / charset (GB2312, GBK, UTF-8, etc.);
- browser support matrix;
- IE-only dependencies;
- ActiveX usage, if any;
- JavaScript validation rules;
- frameset/table-layout details;
- ASP / ASP.NET session behavior;
- cookie lifetime;
- whether a campus-network restriction applied;
- password reset flow;
- whether student ID, ID-card number or a generated credential was used at each site;
- whether employer acceptance generated a printable artifact or only changed backend state;
- exact electronic signature semantics in the Shandong 2006 workflow;
- how dispatch/reassignment changes propagated between university, municipal and provincial databases;
- peak-period capacity and timeout behavior.

These must remain `unknown` until technical evidence is inspected.

---

## 12. 2015 boundary: what the Web had become, and what it still had not replaced

By the first half of the 2010s, Chinese university employment websites could already combine information, authenticated student records, recruitment and administrative workflows. Yet the decisive route often still left the browser:

- archive moved physically;
- hukou procedures completed elsewhere;
- employer report-in happened offline;
- the actual labor relationship could begin later or not at all.

Therefore the archaeology object is not simply “an old graduate job site.”

It is:

> **a Web control plane attached to a distributed socio-technical transaction whose other components lived in university offices, provincial databases, employers, post, personnel archives and police-registration systems.**

That distinction should guide capture interpretation.

---

## 13. Post-scope boundary notes (not expansion of repository scope)

Later evidence helps identify which 2004–2015 states were durable and which were transitional.

### 2019 Guangdong: database becomes the primary credential surface

A provincial smart-service platform enabled electronic employment report cards, archive-destination queries and online reassignment. It also offered historical electronic report-card queries for graduates from 2006–2016.

- Ministry of Education / China Education Daily, 2019-05-29:
  https://www.moe.gov.cn/jyb_xwfb/s5147/201905/t20190529_383569.html

This is useful as **afterlife evidence** for older records, not as proof of the old site's original UI.

### 2020 pandemic: physical dependencies become visible

Jiangsu's 2020 emergency process used Web/WeChat recruitment, online interviews, express-mail paper agreements, platform approval and mailed report cards.

- https://news.jstv.com/a/20200212/1581495225897.shtml

This shows that even after years of Web employment services, paper and physical delivery remained inside the transaction.

### 2023: report card removed, destination registry remains

From 2023, the employment report card stopped being required, but the Ministry of Education established graduate-destination registration and query/verification mechanisms connected to archive and hukou transfer.

- https://app.www.gov.cn/govdata/gov/202305/13/500817/article.html
- https://www.moe.gov.cn/jyb_xwfb/xw_zt/moe_357/jjyzt_2022/2022_zt18/gzbs/202306/t20230626_1065810.html

This later development suggests a **paper-to-registry inversion**, but it should be analyzed in the life-history repository rather than extending this old-Web case beyond 2015.

---

## 14. Overseas comparator: Japan 1997–1998

The comparison is about the Web entering a synchronized graduate-employment system, **not** about equivalence of institutions.

A 1997 report described a 20-year-old Tokyo university student learning to use university Internet facilities specifically to begin job hunting; employer homepages supplied job, meeting, office-visit and interview information, and some accepted applications online.

- Times Higher Education, 1997-11-14:
  https://www.timeshighereducation.com/news/japans-young-job-hunters-scour-the-web-for-leads/104571.article

A 1998 Japan Times report said Internet access made corporate recruitment information easier to obtain while post-recruitment-pact job hunting was beginning earlier and lasting longer; some students applied to dozens of firms.

- Japan Times, 1998-07-23:
  https://www.japantimes.co.jp/news/1998/07/23/national/end-of-recruitment-pacts-sparks-skipping-to-find-jobs/

**Grade: B contemporaneous overseas media.**

Common mechanism supported:

- university Internet infrastructure could reduce job-information/search friction inside a synchronized new-graduate labor market;
- lower search friction could coexist with more applications, earlier recruitment and greater time pressure.

Not supported:

- any Japanese equivalent of China's employment report card, hukou route or personnel-archive coupling;
- identical graduate status rules.

---

## 15. Evidence table

| Claim | Evidence | Grade | Confidence | Caveat |
|---|---|---:|---:|---|
| Beijing online graduate job fairs used imported student status + student activation + university verification by 2004 | contemporaneous report | B | high for reported workflow | UI not inspected |
| Shandong announced online agreement/dispatch/reassignment from 2006 | two contemporaneous reports | B | high | authenticated system not captured here |
| SYSU 2008 notice referenced online temporary-employment application and a default archive/hukou route | current official legacy content | A-content | high for preserved text | historical capture unverified |
| XMU 2008 notices connected report card, archive confidential post, hukou and time-limited Web account | current official legacy content | A-content | high for preserved text | historical rendering unverified |
| At least one 2008 Shanghai graduate experienced job/hukou/archive timing as a coupled constraint | contemporaneous interview | B | medium-high for existence of case | not representative |
| Administrative employment record can diverge from lived employment | 2009 investigated case | B | high for existence of divergence | no rate estimate |
| Japan 1997–1998 Web job hunting reduced information friction while recruitment timing pressure persisted/increased | contemporaneous media | B | medium-high | institutional systems differ |

---

## 16. M1 status

**M1 NOT ACHIEVED IN THIS SLICE.**

This slice inspected:

- contemporaneous media evidence;
- current official legacy pages carrying 2008-dated procedural text;
- explicit historical URLs and system names.

It did **not** obtain and inspect a qualifying verified Wayback/WARC response for a 2004–2010 authenticated Chinese graduate-employment platform.

Therefore we still do not have, for this case:

- ≥2 verified historical capture timepoints of the transactional site;
- historical HTTP headers;
- original charset confirmed from capture;
- DOM/CSS/JS inspection;
- subresource-loss map;
- browser/IE compatibility verification;
- authenticated transaction replay evidence;
- exact server-side state transitions.

Correct conclusion:

> “No qualifying capture was verified in this research slice.”

Incorrect conclusion:

> “Wayback has no copy.”

The latter has not been established.

---

## 17. High-value next archive targets

1. `www.sdbys.cn` around 2005-10 through 2007, especially public help pages explaining online agreement, dispatch and reassignment.
2. Sun Yat-sen employment-management locators referenced in the 2008 notice, including `202.116.65.110/employ/login_student.aspx`.
3. Xiamen University graduate-employment help pages around 2008, including report-card/reassignment instructions.
4. Beijing graduate employment information network around 2004–2006, especially electronic recommendation form workflows.
5. Public user guides/screenshots that reveal browser and form assumptions without exposing private student records.
6. Evidence of how a signed online agreement was converted to a printable report card / dispatch document in a specific province.

Do not attempt to access private historical student accounts or reproduce personally sensitive records.

---

## 18. What this changes in old-Web interpretation

Old Web pages did not only represent conversation, publishing and consumption.

Some pages were **state-transition interfaces** attached to life-course institutions. A graduate could click a form in June and thereby influence where a sealed archive was mailed in July, which document was printed, whether a personnel office could accept the file, and what route remained available after leaving campus.

That gives this repository a stronger archaeology rule:

> **For transactional old-Web systems, reconstruct not only what the page said, but what had to happen before and after the page for the real-world state to become true.**

Otherwise a perfectly preserved screen can produce a historically false life.

---

AI-assisted initial research note. Historical UI/capture claims intentionally remain narrower than the surviving procedural-text evidence.