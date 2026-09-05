# Web Form / Fax / E-mail Hybrid Application and Document-Receipt State Gaps, 2003–2010

## Scope

This note stays inside the repository's Chinese old-Web scope. It does **not** attempt to write a global history of facsimile or electronic government.

The archaeology target is a common but poorly preserved 2000s Chinese workflow:

> a public Web page begins an application, but the application only becomes valid after a form is printed, faxed, mailed, e-mailed, manually matched, checked, and sometimes reconfirmed in person.

This matters because a surviving old page may say `网上报名`, `下载报名表`, `传真`, `E-mail`, or `资格查询`, while none of those phrases alone tells us what state the applicant actually reached.

Cross-repository context:

- `tmzncty/how-people-lived/topics/from-fax-to-data-reuse-documentary-reachability-remote-submission-and-proof-mobility-china-1985-2026.zh-CN.md`

The life-history repository handles the longer pre-Web and post-2015 comparison. This file only defines old-Web technical/evidentiary boundaries and state gaps.

---

## 1. Why this is a distinct old-Web object

A 2000s institutional Web application often was not a self-contained Web transaction.

It could instead be:

`public instructions page`
→ `Web registration`
→ `generated form`
→ `local print`
→ `handwritten completion/signature`
→ `fax or post`
→ `staff receipt`
→ `manual match with Web record`
→ `eligibility review`
→ `Web result page`
→ `in-person original-document check`.

The Web page was therefore one control surface inside a **multi-channel transaction**.

A historically accurate reconstruction must preserve the handoffs between:

- HTTP;
- browser rendering;
- local printer;
- paper document;
- public switched telephone network / fax;
- e-mail;
- postal delivery;
- office staff;
- private institutional database;
- public result page;
- physical counter or exam room.

Calling the whole thing simply “online registration” collapses the most important state transitions.

---

## 2. Strong contemporaneous cases

### 2.1 Hohai University, 2008: online registration produced a form that still had to return by fax/post

Hohai University's official 2008 broadcasting-and-hosting arts admissions brochure required applicants to:

1. register on the university admissions Web site during a specified window;
2. download and print the generated registration-information form;
3. complete it;
4. deliver, mail, **or fax** it to the admissions office before a second deadline;
5. visit the admissions Web site several days later to check qualification;
6. appear in person with identification, photograph, qualification notice and examination fee.

Sources:

- official admissions brochure: https://zsw.hhu.edu.cn/zskx/471.html
- official university news item: https://www.hhu.edu.cn/_t128/2008/0307/c187a145085/page.htm

Evidence class: **A — contemporaneous institutional instructions**.

This is a canonical hybrid chain:

`Web account/form state`
→ `paper-image transmission state`
→ `staff review state`
→ `public qualification state`
→ `physical identity/original state`.

### 2.2 Zhengzhou University Third Affiliated Hospital, 2007: letter / fax / e-mail were parallel submission routes

The hospital's official recruitment notice allowed applicants to register by letter, fax, or e-mail and submit a résumé. Candidates later had to bring original and copied identity, degree and language-certification documents to the interview.

Source:
https://www.zzu.edu.cn/info/1442/60061.htm

Evidence class: **A — contemporaneous institutional recruitment notice**.

The page proves that a Web-published recruitment notice could route the applicant **off the Web** for the actual submission.

`recruitment page visible` therefore does not imply:

`application stored in Web application database`.

There may have been no public applicant database at all for that workflow.

### 2.3 Guangxi inspection/quarantine recruitment, 2008: fax receipt, e-mail feedback, then on-site confirmation

A preserved contemporary recruitment copy says out-of-province applicants could download a form and fax it with required materials; qualification feedback would be returned by e-mail; successful fax applicants still had to attend on-site confirmation, pay and collect an admission ticket.

Preserved source:
https://www.job910.com/jobs/zhaopin-146161.html

Evidence class: **B — contemporaneous secondary preservation of an institutional notice**. The original agency page remains to be located and verified.

This case is especially useful because the channels are sequential rather than interchangeable:

`fax submission`
→ `e-mail review result`
→ `physical confirmation`.

A single applicant therefore had to maintain several reachable endpoints at once.

### 2.4 National postgraduate registration, 2008: “online” still required a physical confirmation phase

The Ministry of Education's September 2008 notice says national postgraduate registration used online registration plus on-site confirmation; applicants had to present identity and graduation documents, pay and be photographed. It also warned users to disable pop-up blockers and stated that certain key fields could not be changed after a registration number was generated.

Source:
https://www.moe.gov.cn/moe_879/moe_329/moe_1798/tnull_39054.html

Evidence class: **A — contemporaneous central-government instructions**.

This is not primarily a fax case, but it is important as the control: even a national-scale Web registration system could deliberately stop short of full remote completion.

---

## 3. Legal transition: data messages could become documents, but workflow adoption lagged

China's Electronic Signature Law was adopted on 28 August 2004 and took effect on 1 April 2005. It established legal conditions under which a data message could satisfy written/original-form requirements and electronic signatures could have legal effect.

Official text:
https://www.cac.gov.cn/2004-08/28/c_126468489.htm

Evidence class: **A — law**.

Archaeological rule:

> `electronic-document law exists != this historical Web workflow accepted an electronic document`.

The Hohai 2008 case is a direct counterexample to any simple legal/technical determinism: a Web application could coexist with printing and faxing several years after the Electronic Signature Law entered into force.

---

## 4. Required state model

For any historical Web + fax/e-mail application, use at least the following states when evidence permits.

### 4.1 Public-Web state

1. `instructions_page_existed`
2. `instructions_page_was_reachable_at_relevant_date`
3. `registration_window_was_open`
4. `browser_rendered_required_controls`
5. `user_understood_route`
6. `account_or_registration_record_created`
7. `registration_number_generated`
8. `downloadable_form_generated_or_retrieved`

### 4.2 Local-document state

9. `form_download_completed`
10. `form_rendered_correctly`
11. `form_printed`
12. `required_fields_completed`
13. `signature/photo/stamp_if_required_added`
14. `supporting_documents_assembled`

### 4.3 Fax state

15. `correct_fax_number_obtained`
16. `sender_had_access_to_fax_endpoint`
17. `dial_attempt_made`
18. `fax_handshake_completed`
19. `all_pages_transmitted`
20. `sender_received_local_success_report_if_any`
21. `receiver_terminal_received_pages`
22. `pages_printed_or_queued`
23. `pages_legible`
24. `pages_remained_grouped`
25. `pages_reached_correct staff`

### 4.4 E-mail state

26. `correct_address_obtained`
27. `message_sent`
28. `SMTP_delivery_or_provider_acceptance`
29. `mailbox_received`
30. `spam/filter did not suppress`
31. `attachment intact`
32. `attachment format readable`
33. `staff opened message`

### 4.5 Institutional matching/review state

34. `fax/email/paper matched_to_web_record`
35. `applicant_identity_match`
36. `all_required_materials_present`
37. `review_started`
38. `eligibility_result_created`
39. `result_persisted`
40. `result_published_or_notified`
41. `applicant_encountered_result`

### 4.6 Physical closure state

42. `applicant_travelled_if_required`
43. `original_documents_presented`
44. `originals_matched_remote_copies`
45. `payment/photograph/biometrics_if_required_completed`
46. `final_valid_application_or_admission_state`

A historical capture will usually expose only a small fraction of these.

---

## 5. Hard state gaps

### 5.1 Online-registration / complete-application gap

A registration number can exist while mandatory faxed/mailed documents are absent.

Therefore:

`Web registration success != application complete`.

### 5.2 Fax-send / fax-receipt gap

A local fax terminal may report successful transmission, but that does not prove that:

- the correct institutional terminal received every page;
- the printout was readable;
- the paper was not separated from other pages;
- staff attached it to the correct applicant record.

Therefore:

`sender success report != institutional receipt`.

### 5.3 Receipt / case-file gap

The receiving fax machine can physically print a page that never reaches the person performing qualification review.

`paper at fax machine != material in case file`.

### 5.4 Image / identity gap

Fax is an image-transport system. It can preserve the appearance of a signature, ID copy or stamp without inherently proving who controlled the sending endpoint.

`visible signature image != authenticated signer`.

### 5.5 Web-record / fax-page matching gap

A Web form may generate a registration number, but the fax page must still carry enough information for office staff to match it to the correct private database record.

`same name != same applicant record`.

### 5.6 Deadline-clock gap

Hybrid workflows can have several clocks:

- browser submit time;
- server record time;
- local fax send time;
- receiver fax timestamp;
- staff receipt/registration time;
- postmark;
- physical arrival time.

If a rule says “received before 17:00,” do not infer which clock controlled without the original rules/manual.

### 5.7 Generated-form / historical-rendering gap

A currently preserved HTML notice may describe a generated historical form. That does **not** reconstruct:

- the original form HTML/PDF/Word file;
- its charset;
- fonts;
- pagination;
- print CSS;
- required client software;
- whether form fields were server-populated or client-rendered.

### 5.8 E-mail accepted / attachment usable gap

A message can exist while its attachment is missing, corrupted, blocked or unreadable.

`mailbox delivery != usable application material`.

### 5.9 Qualification-page / user-encounter gap

If results were posted on a Web page rather than pushed to an applicant, public capture proves the page existed but not that a particular applicant saw it before the next deadline.

`result published != applicant knew result`.

### 5.10 Copy / original gap

A faxed or scanned copy may be accepted for preliminary review while an original remains mandatory later.

`remote copy accepted for screening != original verified`.

---

## 6. Client environment and material conversion

Hybrid application archaeology must include the applicant-side physical stack, not just the server.

Potential dependencies include:

- browser version;
- page charset;
- pop-up permissions;
- downloadable Word/PDF format;
- office suite/version;
- printer and paper;
- scanner/copier if a supporting document had to become an image;
- access to a fax terminal;
- fixed telephone line;
- long-distance dialing rules/cost;
- e-mail account and attachment size;
- local shop/campus/office opening hours.

The Ministry of Education's 2008 postgraduate-registration notice explicitly warned that pop-up blockers had to be disabled. That is sufficient to establish a client-side Web dependency for that workflow, but not enough to infer a precise IE version, JavaScript engine or DOM implementation.

Do not write “IE6 required” unless a primary historical manual/capture actually says so.

---

## 7. The archive asymmetry

This workflow produces a particularly misleading Web archive.

### What public archives are relatively likely to preserve

- recruitment/admissions notice;
- fax number;
- e-mail address;
- deadline;
- downloadable blank form;
- public qualification list;
- help/FAQ page.

### What archives are unlikely or should not preserve

- applicant identity documents;
- private résumé details;
- completed application forms;
- fax transmission logs;
- receiving-machine queue;
- staff notes;
- private applicant database;
- e-mail inbox state;
- rejection reason;
- original-document verification record.

This produces **instruction-survival / transaction-darkness asymmetry**:

> we can often reconstruct exactly what the institution told applicants to do, while remaining unable to tell whether one actual person's application ever crossed the channel handoffs successfully.

That is not merely an archive failure. Some of the missing states are properly private and should not have been public in the first place.

---

## 8. Privacy and safety stop conditions

Do not try to close the private-state gaps by:

- logging into old applicant accounts;
- testing historical identities or ID numbers;
- using leaked résumé/application databases;
- searching for unredacted faxed ID copies;
- contacting historical applicants merely to reconstruct private records;
- probing current institutional endpoints with historical forms.

A rigorous archaeology may end with:

`public instruction confirmed; private transaction state unknown`.

That is a valid result.

---

## 9. Relation to later “data reuse” — boundary note only

By 2019, Chinese e-government systems increasingly described a different model: rather than requiring the citizen to repeatedly upload copies, already-held identity and certificate data could be pre-filled or reused across government systems.

Contemporaneous example:
https://gongyi.people.com.cn/n1/2019/0522/c151132-31097542.html

That period is outside this note's main 2003–2010 case window and is covered comparatively in `how-people-lived`.

It is mentioned here only to clarify the technical transition:

`Web tells user what paper to fax`
→ `Web accepts uploaded file`
→ `electronic document/signature becomes native transaction object`
→ `institution queries already-held record`.

Do not project the last stage backward into the 2000s.

---

## 10. Evidence table

| Claim | Evidence | Grade | Boundary |
|---|---|---:|---|
| 2008 Hohai applicants registered online, printed a generated form, then mailed/delivered/faxed it and later checked qualification online | Hohai official admissions pages | A | Does not reveal original historical DOM/backend or actual applicant receipt state |
| 2007 hospital recruitment accepted letter/fax/e-mail while requiring originals at interview | Zhengzhou University official page | A | Does not prove share of applicants using each route |
| 2008 out-of-province recruitment could use fax, receive eligibility feedback by e-mail, then confirm on site | preserved contemporary recruitment notice | B | Original agency page not yet verified |
| 2008 national postgraduate registration combined Web submission and on-site confirmation | Ministry of Education | A | Not a fax workflow; used as national control case |
| Electronic Signature Law took effect in 2005 | official legal text | A | Legal availability does not establish institutional implementation |
| Fax transmission substantially predated Web and could move document images over telephone lines | telecom/museum and engineering evidence in cross-repo note | A/B | Technical capability does not establish ordinary-user access |

---

## 11. Negative result in this research pass

This pass did **not** obtain and inspect a verified 2003–2010 Wayback/WARC capture that preserves one complete Chinese hybrid application transaction from public instruction through generated form and result state.

In particular, we do not yet have a verified historical capture proving for the Hohai 2008 flow:

- original URL as served in March 2008;
- exact capture datetime;
- HTTP headers;
- charset declaration;
- original DOM;
- registration form action/method;
- session/cookie behavior;
- generated-form file format and template;
- server-side registration-number semantics;
- fax-to-record matching procedure;
- private review database schema.

The currently accessible official pages are strong **historical textual evidence**, but they must not be relabeled as the original 2008 transaction capture.

M1 should therefore remain open.

---

## 12. Future capture target

A useful verified case would ideally preserve:

1. public announcement/instructions;
2. registration entry page;
3. form fields or generated blank/template;
4. explicit fax/e-mail/post instructions;
5. deadline semantics;
6. receipt/confirmation mechanism;
7. public qualification/result page;
8. client-environment requirements;
9. archive replay behavior today.

Especially valuable candidates are 2005–2010 university admissions, public recruitment and professional-exam workflows where the same instructions explicitly name Web + fax + e-mail/post + on-site confirmation.

## Core rule

> **A surviving old Web form is not the historical application. The application existed across browser state, paper state, fax/e-mail transport, private office handling, database matching and physical verification — and the archive usually preserves only the public edges.**
