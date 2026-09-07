# Student-aid loan, green-channel, online-application, Alipay and repayment state gaps, China 1999–2015

## Scope

This is a **Chinese old-Web companion** for the history of higher-education financial aid interfaces.

Primary scope: approximately **1999–2015**, especially the transition from:

- paper poverty certification;
- campus green-channel registration;
- bank/campus loan handling;
- source-region student loans;
- Web application and account management;
- Alipay settlement;
- online repayment and personal-credit records.

Earlier 1998 green-channel practice is boundary context. Post-2015 mobile-app, remote co-borrower authorization and later repayment-relief policy belong mainly in the cross-project life-history note.

Cross-project companion:

- `tmzncty/how-people-lived/topics/green-channel-student-loans-tuition-liquidity-and-education-executability-china-1998-2026.zh-CN.md`

This note is **not** a general consumer-credit history. The relevant transaction is a higher-education access workflow whose browser-visible portion sits between student, household, school, county aid center, bank, payment provider and later credit reporting.

---

## Why this belongs in old-Web archaeology

A surviving student-aid page can look complete while proving only one small state.

A page may show:

- eligibility rules;
- an application button;
- a historical URL;
- a printed application form;
- a repayment instruction;
- an Alipay account explanation;
- a “loan approved” or “loan issued” instruction.

None of those automatically proves that the student:

- could run the required browser;
- had Internet access;
- printed the form;
- passed family-poverty verification;
- appeared with a co-borrower;
- signed a valid contract;
- delivered the school receipt;
- had the contract approved by the bank;
- had funds actually credited to the school;
- remained enrolled;
- later repaid without interruption.

A useful minimum rule is:

> `policy page exists != student eligible != application submitted != contract valid != receipt accepted != loan approved != school paid != student remained enrolled != loan repaid`

This is therefore a strong old-Web case where a **browser-visible control plane** sits on top of a multi-institution financial and educational state machine.

---

## 1. Evidence contract

Repository method applies without exception:

- platform / host / page / capture / claim are distinct;
- `exists`, `available`, `used`, `popular`, and `caused` must not be collapsed;
- current institutional pages carrying historical-dated instructions are not automatically verified historical renderings;
- a historical locator is not a verified capture;
- a loan instruction page cannot prove an individual loan transaction;
- a payment-provider page cannot prove that school accounting received the funds;
- a credit-record warning cannot prove that a specific historical borrower was actually reported at a particular date without account-level evidence.

### Grades used here

- **A**: contemporaneous official regulation, official product/system announcement, or identifiable original technical artifact.
- **A-content**: official/institutional historical-dated content still hosted today, where original historical Web rendering has not been verified.
- **B**: contemporaneous media observation or operational explanation.
- **C**: later recollection.
- **D**: researcher state-machine reconstruction.

No D-grade reconstruction is presented as historical UI.

---

## 2. Pre-Web/early-Web boundary: green channel separates enrollment from immediate payment

In 1998, contemporaneous reporting described Beijing universities allowing disaster-affected and economically disadvantaged students to register through fee deferral, reduction, loans, aid and work-study arrangements.

Evidence:

- `生活时报`, 1998-09-03, preserved by Guangming:
  https://www.gmw.cn/01shsb/1998-09/03/GB/726%5ESH2-307.htm

**Grade: B.**

A 2007 China Youth Daily retrospective, preserved by Tsinghua, describes Tsinghua's 1998 green-channel origin and a named former student case.

Evidence:

- https://www.tsinghua.edu.cn/info/1910/75493.htm

**Grade: A-content for institutional history; C for the retrospective life story.**

Old-Web boundary claim:

> The important precondition for later Web student-aid systems is not “paper loan form existed.” It is that university registration itself became a staged transaction where `admitted` and `fully paid` could be temporarily separated.

That yields an early state chain:

```text
admitted
  -> arrives at university
  -> hardship asserted/documented
  -> green-channel window accepts case
  -> student registered before full payment
  -> later aid/loan/waiver decision
```

This boundary remains outside the repository's main technical scope except where it explains later Web state semantics.

---

## 3. 1999–2004: policy existence / actual loan executability gap

The national student-loan program began pilot operation in 1999 and expanded nationally in 2000. Official retrospective policy material states that by June 2004 about RMB 5.2 billion had actually been issued to roughly 800,000 students, after several years of implementation difficulty.

Evidence:

- Ministry of Education online interview, 2004:
  https://www.moe.gov.cn/jyb_xwfb/xw_zt/moe_357/s3579/moe_489/moe_490/tnull_4001.html
- 2007 official policy review:
  https://www.chsi.com.cn/gjzxdk/news/200703/20070306/756004.html

**Grade: A-content.**

A 2001 China Youth Daily field report describes a Shaanxi Normal University student whose application had been pending for more than half a year; he remained on campus during summer and took tutoring work.

Evidence:

- https://zqb.cyol.com/content/2001-09/05/content_290340.htm

**Grade: B.**

### New state gap: policy-enabled / institutionally executable

```text
national policy exists
  != local bank participates
  != school can process application
  != student application accepted
  != loan approved
  != money issued
```

Call this the **policy-enabled / institutionally executable gap**.

A historical policy page is therefore insufficient evidence that a local student's transaction path existed at the same date.

---

## 4. 2002–2005: hardship evidence / green-channel acceptance / later financing are separate states

A 2002 Nanjing University report describes a student presenting a local family-economic-condition certificate and filling out a university hardship survey before using the green channel; loan application happened later.

Evidence:

- 2002 report preserved via Sohu/People's Daily material:
  https://news.sohu.com/34/37/news202983734.shtml

**Grade: B.**

A 2003 Tsinghua report describes multiple separate channels: temporary no-interest advance, hardship subsidy, national student loan, scholarship, grant, and work-study.

Evidence:

- https://www.tsinghua.edu.cn/info/1994/77385.htm

**Grade: A-content / B.**

### New state gap: hardship document / financing outcome

A historical “poverty certificate” or hardship survey is not the final financial state.

Possible sequence:

```text
local hardship certificate exists
  -> university accepts document
  -> hardship status recorded
  -> temporary enrollment allowed
  -> one or more aid channels evaluated
  -> loan/grant/work-study outcome determined later
```

Therefore:

`hardship documented != student loan approved`.

This matters for archive interpretation because a surviving form often looks like the transaction itself when it is only an input artifact.

---

## 5. 2007–2009: source-region loans create a multi-geography transaction

The source-region credit student-loan program expanded rapidly after 2007. A 2008 official education report states that the initial five-region pilot had approved more than 110,000 applicants.

Evidence:

- Ministry of Education / China Education Daily, 2008-07-23:
  https://www.moe.gov.cn/jyb_xwfb/xw_zt/moe_357/s3579/moe_1889/moe_1890/tnull_37360.html

**Grade: A-content.**

A 2008 Hubei report gives an especially useful state distinction: students who had submitted the source-region loan receipt to the university were to be treated as having completed tuition payment even when loan funds had not yet arrived.

Evidence:

- https://www.chsi.com.cn/gjzxdk/syddk/200812/20081203/11200445.html

**Grade: B / A-content for the quoted administrative rule.**

### New state gap: receipt accepted / funds settled

```text
contract signed
  -> school receipt issued/submitted
  -> school provisionally treats fee as satisfied
  -> bank approval/funding continues
  -> actual school account credited later
```

Thus:

`school accepts receipt` != `bank funds already settled`.

Call this the **receipt / settlement gap**.

The receipt can function as a temporary trust token between education and finance systems.

---

## 6. 2009: coverage eligibility can decide whether the education route remains alive

A January 2009 Hebei Youth Daily report describes a freshman at a private college who had worried about suspension or withdrawal because his school category had not been eligible for the source-region loan; a policy expansion brought private-college students into the program.

Evidence:

- https://gaokao.chsi.com.cn/gkxx/mb/dt/200901/20090104/16013370.html

**Grade: B.**

This supports a narrow state claim:

> `person is economically needy + person is enrolled` did not necessarily imply `loan product covers this institution category`.

### New state gap: applicant condition / covered institution

Loan eligibility can depend on both the person and the institution record.

```text
student eligible by household condition
  + institution category covered
  + school present in authoritative list
  + source-region rules satisfied
  -> application path can proceed
```

A historical eligibility page should therefore be read for the exact covered school types and date.

---

## 7. 2010: the Student Online Service System moves application entry onto the Web

Contemporaneous reporting in Shandong states that 2010 source-region student-loan applications were moved to an online process using the China Development Bank Student Online System at historical locator:

- `http://www.csls.cdb.com.cn`

Evidence:

- Dazhong Daily, 2010-07-16, preserved by Sina:
  https://news.sina.com.cn/o/2010-07-16/040117813240s.shtml
- Qilu Evening News, 2010-07-12, preserved by Sina:
  https://news.sina.com.cn/c/2010-07-12/111017791458s.shtml

**Grade: B.**

A contemporaneous/institutional workflow description says students would:

1. register with real identity in the online system;
2. complete and submit the loan application;
3. export and print the application form;
4. take paper material to the county aid center;
5. undergo on-site review;
6. sign the contract with a co-borrower;
7. carry the acceptance certificate to the university.

Evidence:

- Xi'an Peihua University, 2010-07-22:
  https://www.peihua.edu.cn/zhaosheng/info/1028/1735.htm

**Grade: A-content / B.**

The Ministry of Education's 2010 notice confirms the wider source-region-loan management system and university participation.

Evidence:

- https://www.moe.gov.cn/srcsite/A05/s7052/201008/t20100813_181272.html

**Grade: A.**

### New state gap: Web application / legally completed loan

The 2010 chain is not:

`click submit -> money arrives`.

It is:

```text
Web account created
  -> form submitted online
  -> form exported/printed
  -> paper/application evidence carried offline
  -> county center review
  -> student + co-borrower physically sign
  -> university receipt state
  -> bank review/funding
```

Call this the **Web-front-end / legal-completion gap**.

This is a central old-Web finding: digitization can move data entry and status management online long before signatures, co-borrower presence and institutional verification become remote.

---

## 8. 2010 system environment: browser compatibility was part of aid executability

A preserved copy of the China Development Bank `生源地助学贷款学生在线系统使用手册`, dated June 2010, describes the system as moving tasks previously handled at bank counters onto network access.

Its stated user-computer requirements include:

- Windows;
- Internet Explorer 6.0 or 7.0;
- a host capable of connecting to the Internet.

Evidence:

- current Qingdao University page preserving the 2010 manual text:
  https://history.qdu.edu.cn/info/1075/1338.htm

**Grade: A-content, not a verified 2010 browser capture.**

### New state gap: policy eligibility / client-environment executability

A student might be fully eligible under policy but still need an executable client environment.

Potential prerequisites included:

```text
access to Windows computer
  -> working Internet connection
  -> compatible IE version
  -> ability to register/login
  -> printer access for exported form
```

The source proves requirements, not exclusion rates.

Do **not** infer that economically disadvantaged students were therefore systematically unable to apply. They may have used:

- school computer rooms;
- Internet cafes;
- county aid-center computers;
- relatives' or friends' computers;
- other compatible shared terminals.

This slice has not established the distribution of actual access points.

Call this the **client-environment executability gap**.

---

## 9. 2010: Shanghai shows another historical Web locator and still requires physical completion

A July 2010 Shanghai report identifies another historical student-loan locator:

- `http://www.loan.edu.sh.cn`

Applicants were to fill in personal/family information online, receive a registration number, then appear at the Shanghai Student Affairs Center on specified dates with application material to formally apply.

Evidence:

- Wenhui / Eastday report preserved by Sina, 2010-07-23:
  https://edu.sina.com.cn/gaokao/2010-07-23/1451260146.shtml

**Grade: B.**

Supported narrow claim:

> In at least one 2010 municipal workflow, Web registration produced an identifier for a later physical application appointment rather than replacing the office visit.

### New state gap: online registration / in-person acceptance

`registration number generated` != `loan application accepted`.

A historical Web archive preserving a registration form could therefore miss the actual transaction-acceptance step entirely.

---

## 10. 2010: Alipay becomes a payment rail, but account state and loan state remain separate

In February 2010, China Development Bank and Alipay announced a student-loan payment-settlement partnership. By the 2010 loan cycle, institutional instructions describe the loan system automatically generating Alipay accounts and using them for disbursement and repayment.

Evidence:

- Internet Society of China, contemporaneous industry report, 2010-02-02:
  https://www.isc.org.cn/article/8650.html
- Nanjing Tech student-aid instructions, 2010-09-17:
  https://xszz.njtech.edu.cn/info/1004/1364.htm
- institutional Alipay usage instructions, 2010-09-07:
  https://www.acdt.edu.cn/xsc/info/1149/1341.htm

**Grade: B / A-content.**

One preserved workflow is:

```text
student selects/receives Alipay settlement account
  -> loan contract records account
  -> account becomes usable after system provisioning
  -> student performs Alipay authentication
  -> CDB loan approved
  -> funds sent to Alipay account
  -> tuition/accommodation amount transferred to university
  -> excess amount remains for student withdrawal/use
```

### New state gap: generated account / usable payment identity

A generated Alipay account can exist before:

- it is login-ready;
- password has been changed;
- real-name authentication is complete;
- loan funds have arrived.

Thus:

`Alipay account generated` != `payment identity executable`.

Call this the **generated-account / executable-payment-identity gap**.

---

## 11. 2010–2011: payment-provider integration creates cross-platform transaction dark matter

A CDB source-region loan transaction can cross at least these system boundaries:

```text
CDB student online system
  -> county aid management system
  -> loan contract
  -> school receipt/aid-office system
  -> CDB approval backend
  -> Alipay settlement account
  -> university billing/accounting system
  -> student bank withdrawal / later repayment
```

An archive of only `csls.cdb.com.cn` would not prove the Alipay transfer.

An archive of only `alipay.com` would not prove the university received tuition.

A university instruction page would not prove a specific CDB contract was approved.

Call this **cross-platform transaction dark matter**.

This is analogous to other old-Web state-gap cases in the repository: the visible Web page is often only a control surface for private databases, financial settlement, mailed documents and institutional actions outside the archive.

---

## 12. 2011: loan data becomes more explicitly linked to long-lived credit identity

A China Development Bank Jiangsu branch notice states that source-region student-loan data would be connected to the People's Bank personal credit system, and asks borrowers to keep contact, enrollment and later employment information updated in the Student Online Service System.

The same notice says 2008–2010 borrowers could shift to Alipay repayment and view account information online.

Evidence:

- CDB Jiangsu branch notice, dated 2011-05-03, preserved on Nanjing University of Posts and Telecommunications:
  https://iam.njupt.edu.cn/_t417/2018/1021/c6442a135863/page.htm

**Grade: A-content.**

### New state gap: online profile / reachable borrower

A borrower record can remain in the loan database after:

- the student graduates;
- moves city;
- changes phone number;
- changes email;
- changes employer.

Hence the system asks borrowers to update contact and school/employment information.

`borrower record exists` != `borrower can still be contacted`.

Call this the **borrower-record / reachable-person gap**.

This is a long-horizon archive problem: the transaction may last far longer than the original university Web account or student email.

---

## 13. 2010 repayment workflow: “apply to repay” and “money actually deducted” are distinct

A 2010 university repayment instruction for CDB loans describes a monthly state sequence:

- borrower submits an early-repayment request in the online system;
- borrower moves sufficient funds into the required account by a deadline;
- deduction occurs on a later fixed date.

Evidence:

- Zhongkai University of Agriculture and Engineering, 2010-10-28:
  https://xsc.zhku.edu.cn/info/1132/3313.htm

**Grade: A-content.**

### New state gap: repayment request / repayment completion

```text
repayment request submitted
  -> request accepted for cycle
  -> sufficient balance present
  -> payment provider/bank debit occurs
  -> CDB ledger posts repayment
  -> borrower sees updated balance
```

`repayment request submitted` != `loan repaid`.

Call this the **repayment-request / settlement gap**.

A historical screenshot showing a repayment-request page would not prove completed payment.

---

## 14. 2009 labour-market stress shows why repayment state cannot be moralized from logs alone

A 2009 Xinhua investigation reported that some graduates had no fixed job and failed to deposit required interest by a fixed repayment date.

Evidence:

- Xinhua report preserved by Sina:
  https://news.sina.com.cn/o/2009-12-11/065316754526s.shtml

**Grade: B.**

This is important for old-Web interpretation of delinquency records.

A delinquency state can be real while the causal explanation remains unknown.

Possible causes include:

- unemployment or irregular income;
- address/contact changes;
- misunderstanding of repayment schedule;
- transfer failure;
- insufficient balance;
- deliberate nonpayment;
- other personal circumstances.

Therefore:

`ledger shows overdue` != `archive can infer motive`.

Call this the **delinquency-state / causal-explanation gap**.

---

## 15. Overseas comparison: FAFSA on the Web shows the same front-end/signature lag in a different institutional system

This repository remains focused on the Chinese old Web, so the U.S. case is comparison only.

The U.S. Department of Education launched FAFSA on the Web on June 30, 1997.

Primary technical/operational notices state that the early Web system:

- accepted financial-aid application data over the Internet;
- used SSL 3.0;
- initially required compatible browsers;
- in 1997 was designed for Netscape Navigator 3.0/3.01;
- still required an original paper signature page or later signed SAR to complete the application.

Evidence:

- 1997 development announcement:
  https://fsapartners.ed.gov/knowledge-center/library/electronic-announcements/1999-08-17/fasfa-web
- 1997 launch announcement:
  https://fsapartners.ed.gov/knowledge-center/library/electronic-announcements/1999-08-17/fasfa-live-web
- 1998 browser/encryption notice:
  https://fsapartners.ed.gov/knowledge-center/library/electronic-announcements/1999-08-17/fafsa-web-httpwwwfafsaedgov

**Grade: A.**

By 1999–2000, the Department used mailed PINs/EACs to enable online corrections and then electronic signatures, with identity matching tied to Social Security Administration records.

Evidence:

- 1999 Corrections on the Web:
  https://fsapartners.ed.gov/knowledge-center/library/electronic-announcements/1999-09-21/corrections-web
- 2000 ED PIN Mailer:
  https://fsapartners.ed.gov/knowledge-center/library/electronic-announcements/2000-01-07/ed-pin-mailer

**Grade: A.**

Comparative lesson:

> The hybrid sequence `Web data entry -> offline/legal identity completion -> later digital signature` is not unique to China.

The institutional details differ strongly:

- U.S.: SSN/SSA match, federal PIN, mailed signature/PIN state;
- China: source-region aid center, student + co-borrower, university receipt, CDB system and Alipay settlement.

The common historical rule is:

`form is online` != `transaction is end-to-end digital`.

---

## 16. Browser and infrastructure evidence

The 2010 CDB manual copy is unusually valuable because it provides environment requirements rather than only policy claims.

Observed from preserved manual text:

- Windows requirement;
- IE6/IE7 requirement;
- Internet connectivity requirement.

Not yet established in this slice:

- exact HTTP response headers from `csls.cdb.com.cn` in 2010;
- original page charset;
- whether HTTPS was used for every historical login step;
- TLS/certificate behavior;
- document mode / compatibility-view assumptions;
- ActiveX dependencies, if any;
- JavaScript framework/version;
- cookie/session lifetime;
- accessibility behavior;
- historical screen resolution assumptions;
- print CSS / exported form generation implementation;
- timeout/error pages;
- CAPTCHA behavior;
- actual browser differences between IE6 and IE7.

Do not convert the manual requirements into a reconstructed screenshot.

---

## 17. Candidate historical locators

The following locators are evidenced by contemporaneous/institutional material but are **not verified captures in this slice**:

### China Development Bank Student Online Service System

- `http://www.csls.cdb.com.cn`
- later/current service lineage includes `https://sls.cdb.com.cn`

Evidence families:

- 2010 Shandong contemporary reporting;
- 2010 student manual preserved by university;
- 2011 CDB Jiangsu notice.

### Shanghai student-loan site

- `http://www.loan.edu.sh.cn`

Evidence family:

- 2010 Wenhui/Eastday report preserved by Sina.

### Alipay

- `http://www.alipay.com`

Evidence families:

- 2010 CDB/Alipay partnership report;
- university student-aid operating instructions.

These are **historical locators**, not statements about current ownership, current page content, or archive availability.

---

## 18. State machine for archaeology

A conservative reconstructed state model is:

```text
[education opportunity]
student admitted
  -> tuition/liquidity gap exists
  -> hardship/eligibility evidence prepared
  -> green-channel or aid information reached

[application control plane]
student Web account created
  -> personal/family data entered
  -> application submitted
  -> application form exported/printed

[offline/legal layer]
county aid center receives student
  -> documents reviewed
  -> co-borrower present/accepted
  -> contract signed
  -> acceptance certificate issued

[university layer]
student arrives at university
  -> school receives certificate/receipt
  -> school records receipt
  -> student may be treated as fee-compliant before settlement

[bank/payment layer]
CDB reviews contract/receipt
  -> loan approved
  -> Alipay/payment account generated/provisioned
  -> funds sent
  -> university fee account credited
  -> excess funds available to student where applicable

[long-horizon account layer]
student remains enrolled
  -> graduates
  -> contact/employment information updated
  -> repayment request / scheduled payment
  -> funds actually debited
  -> credit/loan ledger updated
  -> eventual loan closure
```

Every arrow is a possible archival gap.

---

## 19. Named state gaps introduced in this slice

1. **policy-enabled / institutionally executable gap**  
   Policy exists, but local bank/school workflow may not be operational.

2. **hardship-document / financing-outcome gap**  
   A family-poverty certificate does not prove loan approval.

3. **applicant-condition / covered-institution gap**  
   A student may be needy while their institution/category is outside coverage.

4. **receipt / settlement gap**  
   University may accept a loan receipt before funds reach its account.

5. **Web-front-end / legal-completion gap**  
   Online submission may still require printed documents, co-borrower and physical signature.

6. **client-environment executability gap**  
   Policy eligibility does not prove Windows/IE/Internet/printer access.

7. **online-registration / in-person-acceptance gap**  
   A Web registration number can precede a separate physical acceptance appointment.

8. **generated-account / executable-payment-identity gap**  
   Auto-created Alipay account is not necessarily login-ready/authenticated/funded.

9. **cross-platform transaction dark matter**  
   CDB, county center, university and payment-provider states cannot be reconstructed from one site's archive.

10. **borrower-record / reachable-person gap**  
    Long-lived loan record can outlast student email, phone, school account or city.

11. **repayment-request / settlement gap**  
    Online request is not the completed debit or ledger posting.

12. **delinquency-state / causal-explanation gap**  
    Overdue record does not reveal why the person missed the payment.

These are technical-archival distinctions, not claims about borrower character or policy success.

---

## 20. Archive asymmetry

Student-aid history has a strong preservation asymmetry.

Likely to survive publicly:

- policy announcements;
- university instructions;
- help pages;
- historical URLs;
- browser requirements;
- repayment schedules;
- generic screenshots/manuals.

Likely not to survive publicly:

- student's actual application form;
- family income certificate;
- co-borrower identity and signature;
- county review decision details;
- individual CDB loan ledger;
- Alipay transaction history;
- university billing record;
- private SMS/email reminders;
- later employer/contact updates;
- reasons for missed repayment.

This means the archive may overrepresent **the institution's intended workflow** and underrepresent **the user's actual failure/recovery path**.

A historical help page should therefore never be treated as empirical proof that most users completed the process exactly as designed.

---

## 21. Privacy boundary

Student-aid records can contain unusually sensitive ordinary-person data:

- family economic hardship;
- ID numbers;
- home address;
- parent/guardian identity;
- phone numbers;
- school and major;
- loan amount;
- repayment status;
- credit status.

Even if an archive exposes an old application or borrower list, this repository should not republish ordinary borrowers' personal data merely for completeness.

Prefer:

- generic schema;
- policy forms without personal data;
- official manuals;
- contemporaneous pseudonymized media cases;
- field names and workflow reconstruction;
- aggregate statistics.

Do not publish historical ID numbers, phone numbers, personal loan account details or family hardship forms.

---

## 22. What is proved / probable / unknown

### Proved at narrow claim level

- National student loans existed from the 1999 pilot period and expanded nationally after 2000.
- Green-channel enrollment and later financing were separate states by the early 2000s.
- Source-region student loans were operating at large scale by 2008.
- A 2008 Hubei administrative statement treated an accepted loan receipt as tuition completion before funds had necessarily arrived.
- In 2010, `csls.cdb.com.cn` was publicly identified as the CDB student online system locator in Shandong loan application instructions.
- The 2010 workflow still included printing, county review, co-borrower signing and university receipt.
- A preserved 2010 CDB manual states Windows + IE6/7 + Internet requirements.
- In 2010, Alipay became part of CDB student-loan disbursement/repayment workflow.
- By 2011, CDB instructions connected online borrower information maintenance with credit/repayment management.

### Probable, with caution

- Web application reduced some repetitive local data-entry and query friction.
- Alipay reduced some geographic friction in loan repayment.
- Online account management increased the importance of persistent digital identity and contact-data maintenance over the loan's multi-year lifetime.

These are mechanism-level interpretations; this slice does not quantify user-level time savings.

### Unknown

- A verified 2010 capture of the CDB student login/application page has not been inspected in this slice.
- Original HTML/CSS/JS, charset and HTTP headers are unknown.
- Exact TLS/certificate implementation is unknown.
- Actual rate of student access through home PC vs school lab vs Internet cafe vs aid-center terminal is unknown.
- Historical error/timeout/CAPTCHA states are unknown.
- Exact data exchange schema among CDB, local aid offices, universities and Alipay is unknown.
- Real historical account-provisioning failure rates are unknown.
- The share of transactions that followed the documented happy path is unknown.

---

## 23. M1 status

**M1 is NOT ACHIEVED IN THIS SLICE.**

This note contains strong A/A-content/B evidence for workflow and historical locators, but it does **not** contain a fully verified archaeological case with:

- at least two inspected historical captures of the same Chinese student-aid site;
- original/memento metadata;
- historical response headers;
- resource-missing inventory;
- verified charset/browser behavior;
- historical DOM/subresource inspection.

No Wayback/WARC response for `csls.cdb.com.cn` or `loan.edu.sh.cn` was successfully opened and inspected in this research slice.

Correct wording:

> `No verified capture was inspected in this slice.`

Incorrect wording:

> `Wayback has no capture.`

The latter has not been established.

---

## 24. Next verification targets

1. Find and actually open a 2010–2011 capture of `csls.cdb.com.cn`.
2. Record original URL, archive source, capture datetime, HTTP/replay status and charset.
3. Check whether login page, registration page and downloadable/export form were separately captured.
4. Compare capture with the June 2010 manual's IE6/IE7 assumptions.
5. Search the Shanghai `loan.edu.sh.cn` 2010 locator for at least two historical timestamps.
6. Check whether Alipay's public student-loan instructions had a distinct historical endpoint and whether it survived as HTML or only screenshots/third-party copies.
7. Search university IT/help archives for real user reports of IE compatibility, printing failures, password provisioning, or account activation.
8. Preserve only generic error/interface evidence; do not recover or republish private borrower records.

---

## 25. Why this changes old-Web interpretation

A financial-aid website is not merely an information page.

For a student who could not immediately pay tuition, a browser session could sit inside a chain that determined whether a university life remained executable.

The historically important object is therefore not just:

`What did the 2010 page look like?`

It is:

> **Which state could the page actually change, which states still required paper or a nearby adult body, which institution held the authoritative record, and at what moment did an admission offer become a funded place in a classroom?**

That is the old-Web archaeology of student aid.

---

## Research note

Initial synthesis is AI-assisted. Evidence grades follow repository method. Personal borrower data is deliberately minimized.
