# SELF_STUDY_EXAM_REGISTRATION_PAYMENT_EXAM_RECORD_AND_GRADUATION_STATE_GAPS_2005_2010.md

Status: research note / state-gap model  
Scope: Chinese old Web, c. 2005–2010, using higher-education self-study examination portals as the primary object.  
Cross-link: `tmzncty/how-people-lived/topics/education-reentry-self-study-exams-open-university-and-life-course-reopenability-china-1981-2026.zh-CN.md`

This note asks a narrow old-Web question:

> When an adult learner's education route moved from a counter/telephone/postal process into Web portals, what did the Web page actually prove about the exam state — and what remained outside the page?

The object is not “online education.” Most self-study examination learning and testing remained materially separate from the registration portal. The Web primarily became an **administrative control plane** for a long-lived educational identity.

---

## 1. Research units

Keep these units separate:

- **exam system** — provincial/national self-study examination administration;
- **portal host** — e.g. an education examination authority host;
- **registration account / candidate identity**;
- **provisional registration record**;
- **admission-ticket / candidate number (准考证号)**;
- **course offering / exam session**;
- **course-selection request**;
- **payment transaction**;
- **paid/unpaid state shown by portal**;
- **offline photo/identity confirmation**;
- **exam notice / seat information**;
- **physical exam attendance**;
- **score record**;
- **cumulative exam record (考籍)**;
- **transfer/exemption/substitution state**;
- **graduation application**;
- **graduation audit**;
- **physical/digital certificate record**;
- **archive capture**;
- **claim**.

A surviving registration page cannot collapse all of these into “the person was a student.”

---

## 2. Minimal state machine

A more realistic self-study-exam state machine for the mid/late-2000s is:

```text
candidate decides to re-enter education
→ opens current exam-session notice
→ confirms eligible major/course
→ new-user registration OR existing-candidate login
→ submits identity/basic data
→ receives provisional registration state
→ selects course(s)
→ invokes bank/postal payment gateway
→ payment requested
→ payment accepted by bank
→ payment state returned to exam portal
→ portal marks course as paid
→ new candidate receives/derives formal candidate number
→ prints registration result / exam notice
→ completes required offline identity/photo capture
→ admission ticket / exam qualification becomes usable
→ attends physical exam
→ score published
→ score enters cumulative exam record
→ later session repeats course-selection cycle
→ transfer / exemption / course-plan migration if needed
→ graduation conditions appear satisfied
→ graduation application submitted
→ identity / previous education / historical credits checked
→ local/provincial confirmation and audit
→ certificate approved/issued
```

Hard boundaries:

- `form submitted ≠ registered`
- `registration number ≠ exam eligibility`
- `bank debited ≠ exam portal marked paid`
- `portal marked paid ≠ candidate attended`
- `score displayed ≠ score safely incorporated into long-term exam record`
- `all visible scores passed ≠ graduation approved`
- `online graduation application ≠ certificate issued`

---

## 3. 2005–2006 Beijing: Web registration already depended on historical browser/payment conditions

A 2005 Beijing Examination News FAQ preserved by Sina described concrete online-payment failures.

It stated that some Windows 98 / Windows 2000 environments could have an IE browser with insufficient cipher/key length for the Beijing Bank payment page; the bank required 128-bit browser key length. The postal payment gateway could also fail when the browser version was too old.

Source (B, contemporaneous newspaper technical guidance):

<https://edu.sina.com.cn/exam/2005-12-19/155624543.html>

This supports narrow claims:

- online exam registration/payment was operational enough to generate support documentation;
- browser version/security capability could affect payment executability;
- successful access to the exam portal did not imply access to the payment gateway.

It does **not** prove the exact historical DOM/CSS/JS of the registration portal.

---

## 4. 2006 Tianjin: the browser, bank plugin and bank account were part of exam eligibility in practice

A contemporaneous 2006 notice for the January 2007 Tianjin self-study exam described a more explicit prerequisite stack:

- Windows 2000 or later;
- browser at least IE 6.0 class;
- 128-bit key length;
- ICBC security plugin installed;
- qualifying ICBC card/account;
- personal online banking activated;
- online payment passwords configured.

Source (B, contemporaneous notice reproduced by Zikao365):

<https://www.zikao365.com/html/3_7/2006_11_28_wa13771652488211600214392_0.htm>

The notice also says that exam-score query, score-review application and cross-province score-transfer application were opened through the same candidate-service system.

This is important for old-Web archaeology because the page was not merely an information site. It was part of a **stateful administrative workflow**.

A static capture of its front page would miss most of the historically important state.

---

## 5. 2006 Shanghai: existing candidates could transact remotely while new candidates still required physical enrollment

A Shanghai Education Examination Authority notice for the October 2006 self-study examination said existing candidates holding the required self-study-exam ICBC card could register online through the bank site.

New candidates, however, still had to appear at designated registration points to complete registration and digital-photograph collection.

Source (B/A-family official notice preserved by Zikao365):

<https://www.zikao365.com/html/2006/8/wa3621139486002115.html>

Narrow conclusion:

> **digital re-enrollment for an already known candidate can precede digital first-time identity establishment.**

This distinction matters when interpreting old portals.

---

## 6. 2007 Beijing: three channels coexisted, but new identity creation became Web-first

A May 2007 *Beijing News* report described the October 2007 self-study exam registration process.

For existing course registration, three channels coexisted:

1. Web;
2. telephone (11185);
3. postal-savings business outlets.

But first-time registration was Web-only. A new candidate had to:

- enter personal information online;
- select major and course;
- complete payment;
- log in again to obtain the formal admission-ticket/candidate number;
- print the successful-registration information sheet;
- later visit the district/county self-study office for photography and related procedures.

Source (B, contemporaneous reporting of authority notice):

<https://news.sina.com.cn/s/2007-05-25/035411888853s.shtml>

This supports a useful transition model:

```text
old candidate: web | phone | postal outlet
new candidate: web → payment → candidate number → paper printout → offline photo/identity step
```

The Web did not eliminate the institutional counter; it changed which stage required the body to appear.

---

## 7. Identity-binding gap

The 2007 Beijing workflow creates several distinct identity states:

```text
typed personal data
→ provisional Web registration
→ payment success
→ formal candidate number
→ offline photograph/identity binding
→ usable exam credential
```

A historical registration page can prove only the state it actually displays.

Do not infer:

- that a typed name was verified;
- that the candidate completed photography;
- that the candidate received the physical admission ticket;
- that the person who operated the browser was necessarily the eventual exam taker.

Recommended gap name:

> **identity-binding gap**

---

## 8. Payment-callback gap

Several contemporaneous notices define registration success by the portal showing the course payment state as **“已缴费”**.

For example, a 2009 Beijing practical-course notice said registration success was represented by the course payment status being “paid”; the online payment system at that time supported Beijing Bank.

Source:

<https://www.zikao365.com/new/1_15/2009_3_9_li82783214119390024853.shtml>

The important chain is:

```text
exam portal creates order/request
→ bank page accepts payment attempt
→ bank settles/debits
→ callback/return reaches exam service
→ exam portal updates course state to paid
```

Without historical backend logs, a bank-side event and an exam-side registration state cannot be assumed identical.

Recommended gap name:

> **payment-callback gap**

---

## 9. 2008 Beijing: the portal was becoming a persistent candidate-state surface

In April 2008 Beijing opened a “Higher Education Self-study Examination Comprehensive Information Query System.” Contemporary reporting said self-study exam services had progressively moved online, including:

- exam registration;
- payment;
- score/query services;
- exam-record handling;
- graduation application;
- thesis application;
- certificate query;
- online learning services.

Source (B, *Beijing Examination News*):

<https://edu.sina.com.cn/zikao/2008-04-02/1417131748.shtml>

This is a major old-Web transition.

The portal was no longer merely an announcement board. It was becoming a **longitudinal institutional identity surface**.

For an adult learner who studied over several years, the historically important object is therefore not one page but a persistent state relation:

```text
candidate identity
↔ accumulated course results
↔ current course-plan version
↔ transfer/exemption state
↔ graduation eligibility
```

---

## 10. Exam-record persistence gap

Self-study examination is especially sensitive to archival misunderstanding because completion is modular.

One candidate can have:

- course A passed in 2006;
- course B failed in 2007;
- no exam in 2008;
- course B passed in 2009;
- cross-province transfer in 2010;
- a changed course plan in 2011.

A capture from one year can never be treated as the complete educational record.

Recommended gap name:

> **exam-record persistence gap**

Questions to preserve:

- Was a score only displayed or committed into exam records?
- Did the course code later change?
- Was the result transferred between provinces?
- Was it substituted or exempted?
- Was a previous result still valid under the graduation plan used later?

---

## 11. Course-plan version gap

A self-study programme can change required course codes, names, practice components or substitution rules.

Therefore:

> `candidate passed every course visible in a historical page ≠ candidate satisfied a later graduation plan`.

For reconstruction, preserve where possible:

- programme/major code;
- exam session;
- course code;
- course title;
- theory/practical classification;
- plan/version date;
- substitution rule;
- exemption rule;
- effective period.

Recommended gap name:

> **course-plan version gap**

---

## 12. 2009 Tibet: online registration still ended in physical confirmation, payment and photo collection

A 2009 Tibet Education Examination Authority notice, preserved on the Tibet government site, said candidates could complete online registration through the examination-authority website during June 25–30 and edit submitted information during that period.

Then, during July 1–5, the candidate had to appear personally at the local education/sports bureau self-study office to:

- confirm registration information;
- pay fees;
- collect a photograph.

Source (A/B government publication):

<https://www.xizang.gov.cn/zwgk/xxfb/gsgg_428/201902/t20190223_61084.html>

This is another reminder that “online registration” is a stage, not a full transaction.

---

## 13. 2010 Hubei: online graduation application exposed the final credential state machine

Hubei Provincial Education Examination Authority published a detailed 2010 online graduation procedure.

The process included:

- online applicant registration;
- later information confirmation;
- provincial online audit/validation;
- valid ID original/copy;
- candidate/admission-ticket card;
- course pass certificates;
- completion of required thesis/practical work;
- correct transfer/exemption status;
- previous higher-education credential for undergraduate graduation applicants;
- additional proof for name changes.

Source (A, provincial examination authority):

<https://www.hbea.edu.cn/html/2010-05/3123.shtml>

This produces another hard boundary:

> **graduation-eligible in the candidate's own view ≠ graduation approved by the authority.**

Recommended gap name:

> **credential-closure gap**

---

## 14. 2010 Heilongjiang: score query, real-name Web account, graduation application and online payment were linked

A May 2010 notice from the Heilongjiang self-study examination office said April exam results were available online; candidates already registered online could query directly, while others had to complete real-name registration first.

The same notice said graduation applications continued online during a fixed window and included online payment.

Preserved contemporary copy:

<https://heilongjiang.eol.cn/hljkaoshi/201005/t20100512_474200.shtml>

The later certificate notice said successful graduation applicants still had to collect certificates through the relevant examination office.

Preserved notice:

<https://www.zikao365.com/new/1_9/2010_7_5_li1372517115701024890.shtml>

Again:

```text
online graduation application
→ audit/validation
→ certificate issuance
→ physical collection
```

The Web did not make the credential purely virtual.

---

## 15. Browser-environment evidence boundary

The 2005–2007 material is unusually valuable because it gives explicit historical browser assumptions:

- IE version constraints;
- Windows version constraints;
- 128-bit key-length requirement;
- bank security plugin requirement;
- specific bank/card prerequisites.

These are stronger than a modern Wayback replay.

However, they still do not prove:

- exact page rendering;
- historical viewport;
- charset;
- CSS layout;
- client-side JavaScript implementation;
- whether a payment popup used ActiveX or another mechanism unless explicitly documented;
- server software.

Do not reconstruct those from the support text alone.

---

## 16. Archive survival bias

Public archives are more likely to preserve:

- examination notices;
- public schedules;
- help/FAQ pages;
- newspaper tutorials;
- course tables;
- generic login entry pages.

They are much less likely to preserve:

- authenticated candidate dashboards;
- historical score ledgers;
- payment state;
- identity/photo bindings;
- transfer records;
- exemption decisions;
- graduation audit outcomes.

This creates a systematic bias:

> **the public instruction layer survives better than the educational state layer.**

A future historian can easily learn “how a candidate was told to apply” while being unable to prove what happened to an ordinary candidate after clicking submit.

---

## 17. Privacy stop condition

Historical self-study exam accounts may contain:

- name;
- identity-card number;
- photograph;
- admission-ticket/candidate number;
- home/work contact data;
- education history;
- scores and failures;
- graduation status.

Therefore:

- do not compile old candidate-number lists;
- do not attempt password recovery;
- do not cross-match historical candidates to current accounts;
- do not republish score pages containing unnecessary personal data;
- prefer public official notices and abstracted state models.

The state machine can be studied without reconstructing a private person's transcript.

---

## 18. What is verified in this note

### High confidence

- mid/late-2000s Chinese self-study exam administration used Web registration/payment/query functions in multiple provinces;
- online processes often coexisted with telephone, postal-bank or physical-counter channels;
- first-time candidates could still need offline photo/identity confirmation after Web registration;
- historically documented browser/payment prerequisites could materially affect registration;
- by 2008 Beijing publicly described a broad integrated online self-study exam service surface;
- by 2010 Hubei/Heilongjiang had online graduation application processes with additional identity/qualification audit.

### Medium confidence / locality-bound

- specific browser, bank and payment requirements should be treated as **local and session-specific**, not national rules;
- the degree of end-to-end digitalization varied substantially between provinces and exam sessions.

---

## 19. What this note does not claim

It does not claim:

- every province had online registration by 2005;
- all candidates owned a home PC or bank card;
- Internet registration replaced physical self-study offices;
- the candidate dashboards are recoverable today;
- the historical sites used any particular backend stack;
- browser support was identical across years;
- an archived score page proves final graduation;
- a successful online application proves the candidate sat the exam.

---

## 20. Failed/negative evidence in this run

This run located strong contemporaneous notices and technical guidance but did **not** obtain and inspect a complete authenticated 2005–2010 candidate-session capture containing:

- login;
- registration form;
- course selection;
- bank return;
- paid-state update;
- score ledger;
- graduation workflow;
- certificate outcome.

No claim is made that such a complete capture is publicly recoverable.

The exact historical DOM/CSS/charset/browser rendering of the main registration systems therefore remains **unknown unless separately verified**.

---

## 21. Suggested evidence fields for future captures

```yaml
system_name:
province:
exam_session:
portal_host:
page_url:
capture_url:
capture_datetime:
page_role: notice|registration|login|course-select|payment-return|score|record|graduation
candidate_state_authenticated: false
candidate_identifier_visible: false
new_or_existing_candidate:
registration_state:
course_selection_state:
payment_state:
offline_confirmation_required:
photo_capture_required:
exam_notice_available:
score_state:
record_transfer_state:
exemption_state:
graduation_application_state:
graduation_audit_state:
certificate_state:
browser_requirement:
os_requirement:
bank_requirement:
plugin_requirement:
charset_verified: false
source_grade:
claim_supported:
claim_not_supported:
privacy_redactions:
unknowns:
```

---

## 22. Why this changes old-Web archaeology

A self-study exam portal is a good counterexample to treating the old Web primarily as pages and communities.

For an adult learner, the valuable thing was not the page design. It was whether the page could move a long-lived institutional state forward:

```text
not registered
→ registered
→ paid
→ exam-qualified
→ passed course
→ accumulated credit
→ eligible for graduation
→ certified
```

The archaeology therefore needs to preserve a distinction between:

> **Web artifact survival**

and

> **administrative state survival**.

A perfectly archived public registration page may tell us almost nothing about whether one ordinary person's interrupted education was successfully reopened, continued and finally closed into a credential.
