# Compulsory-education enrollment, migrant-child eligibility, student records, and placement state gaps, 2003–2015

## Scope

This note stays inside the repository’s Chinese old-Web scope. It does **not** turn `old-web-archaeology` into a general history of hukou, migrant labor, or compulsory education.

The narrow object is the transition from Web pages that merely published school-admission policy toward Web systems that participated in compulsory-education enrollment, especially for migrant / non-local-hukou children, while the decisive transaction still crossed:

- parent and child identity;
- hukou and residence records;
- employment / temporary-residence evidence;
- local street or township review;
- education-administration approval;
- school-seat allocation;
- student-record creation or transfer;
- paper printout and signature;
- actual school attendance.

The paired life-history research is in:

`tmzncty/how-people-lived/topics/from-borrowed-school-place-to-portable-student-records-migrant-child-schooling-family-co-residence-and-education-portability-china-1996-2026.zh-CN.md`

The pre-Web 1996–1998 migrant-child policy history belongs primarily in that repository. Here it appears only where needed to explain what a 2014–2015 Web form was actually formalizing.

---

## Research question

When an archived page says “义务教育入学服务平台”, what historical event does that actually prove?

At minimum, the following states must remain separate:

`physical child`
→ `legal guardian`
→ `local-residence claim`
→ `hukou / residence / employment evidence`
→ `Web registration`
→ `information submitted`
→ `cross-system identity validation`
→ `local eligibility review`
→ `proof of local-school eligibility issued`
→ `Web confirmation`
→ `school-seat allocation / contact`
→ `school-side verification`
→ `parent signature / paper retention`
→ `formal enrollment`
→ `student record created or transferred`
→ `actual attendance`
→ `later progression / transfer`.

No archived shell, screenshot, policy page, or surviving form is sufficient to collapse this chain.

---

## 1. What existed before transactional Web enrollment

The 1998 `流动儿童少年就学暂行办法` required migrant children seeking education in the destination locality to navigate approval and application across home and destination jurisdictions. The policy permitted public-school “借读”, private schools, affiliated classes, and schools specifically serving migrant children. It also established temporary student records in receiving schools.

Contemporary-policy text preserved by CERNET:
https://cernet.edu.cn/zhong_guo_jiao_yu/zheng_ce_gs_gui/bu_men_gui_zhang/200603/t20060323_113067.shtml

For this repository the important point is architectural:

**The Web did not invent the enrollment workflow.** It inherited an already multi-actor paper-and-office workflow in which eligibility and student records crossed home locality, destination locality, family, school, and public-security / residence administration.

That makes later Web enrollment a case of **workflow digitization**, not a clean migration from “nothing online” to “everything online”.

---

## 2. 2003–2008: policy information became searchable before the admission transaction became a unified Web state machine

The 2003 State Council General Office document on migrant workers’ children assigned primary responsibility to destination governments and public schools and called for integration into local education planning.

Official text:
https://www.moe.gov.cn/jyb_xxgk/gk_gbgg/moe_0/moe_9/moe_40/tnull_147.html

By 2007, the Ministry of Education website was publishing direct public Q&A from migrant parents asking why children following parents into cities still had to pay “借读费”. The page preserved both the household’s contemporary question and an official policy answer.

Examples:
https://www.moe.gov.cn/moe_879/moe_1252/s8447/201412/t20141204_180172.html
https://www.moe.gov.cn/moe_879/moe_1252/s8447/201412/t20141204_180171.html

This is already a significant old-Web state transition:

`private household uncertainty`
→ `question entered into public Web channel`
→ `question selected / published`
→ `official response published`
→ `policy information becomes searchable by later users`.

But it is **not** an enrollment transaction.

`public Q&A answer != local eligibility determination != school seat`.

### Archive warning: answered-question survival bias

Public government Q&A preserves questions selected for response. It does not preserve:

- every household that had the same problem;
- people who did not know the website existed;
- telephone / office inquiries;
- questions not selected for publication;
- whether the household later succeeded in enrolling the child.

A well-preserved policy Q&A page can therefore exaggerate how much of enrollment was actually Web-mediated.

---

## 3. Student-record portability and admissions eligibility are different system layers

In January 2014, the national primary-and-secondary student-record system began nationwide trial operation for cross-province transfers. Official descriptions say a family could apply to the receiving school and the remaining transfer-approval steps could proceed online.

Official sources:
https://www.moe.gov.cn/jyb_xwfb/gzdt_gzdt/s5987/201401/t20140107_162019.html
https://www.moe.gov.cn/s78/A06/gongzuo/s8252/s8271/201408/t20140808_173985.html

This establishes an important state separation for old-Web archaeology:

`school-admission eligibility`
!= `student-record transfer eligibility`
!= `student-record transfer request`
!= `source school / authority approval`
!= `destination acceptance`
!= `record data correctly synchronized`.

A child can have a legitimate receiving-school path while records fail to transfer. Conversely, a technically transferable record does not create a local school seat.

The Ministry’s 2014 implementation reports are unusually valuable because they document data-interface problems among national and provincial systems. One report notes mismatches in self-built provincial systems, including Shanghai fields such as migrant-child status and other student attributes.

Source:
https://www.moe.gov.cn/s78/A06/tongzhi/201409/t20140930_183158.html

Thus:

`database field exists != source and national systems map it identically`.

### Old-Web implication

A surviving front-end transfer page would tell us little about whether:

- the student had a duplicate / temporary / formal record number;
- identity data matched public-security records;
- destination and source systems agreed on field values;
- a province used the national system directly or a local system bridged to it;
- the transfer completed before the child’s real school transition.

Those are backend transaction states and should remain UNKNOWN unless separately evidenced.

---

## 4. Beijing 2014 is the strongest M1 target: first unified compulsory-education entry service

Contemporary April 2014 reporting identifies the original public host:

`http://yjrx.bjedu.cn`

and states that Beijing’s unified compulsory-education admission service would open on 1 May 2014. This was described as the first year Beijing used a unified system covering both primary and junior-secondary entry, connected to the electronic student-record system.

Contemporary sources:
- China Education / Beijing Daily report: https://www.edu.cn/edu/ji_chu/ji_jiao_news/201404/t20140430_1106973.shtml
- People’s Daily education channel: https://edu.people.com.cn/n/2014/0430/c1053-24959606.html
- China News Service: https://www.chinanews.com/edu/2014/04-29/6120015.shtml

The contemporaneous claims support:

- a public portal existed at that host;
- it exposed city / district policy and school information;
- primary-school-age population information collection was mandatory for ordinary admission;
- the service connected admission workflow with electronic student-record administration.

They do **not** by themselves establish the exact 2014 DOM, JavaScript implementation, form endpoints, charset, browser constraints, session design, CAPTCHA design, or backend topology.

Those remain UNKNOWN.

---

## 5. For non-Beijing-hukou children, “online enrollment” was a hybrid workflow, not a Web-only transaction

Contemporary 2014–2015 instructions show a multi-stage workflow for non-local-hukou families.

A 2014 Shijingshan instruction describes parents first visiting `http://yjrx.bjedu.cn`, entering a specific non-local-hukou eligibility-review entrance, then taking the required evidence to the local street office for review, and finally returning to the platform to confirm information after approval.

Contemporary description:
https://www.ysxiao.cn/c/201404/545.html

A 2015 East District parent letter again gives the exact host and explicitly says the online operation is only information collection. Parents still had to take employment, residence, temporary-residence, household-register and home-locality guardianship evidence to street-level review. After cross-department review, they queried the result and printed the local-school eligibility proof and child information-collection form.

Contemporary description:
https://www.ysxiao.cn/c/201504/3728.html

An official 2015 Yanshan implementation document provides an especially useful state sequence:

1. relevant departments examine different documents;
2. the street office communicates the review result;
3. eligible families receive `在京就读证明`;
4. the education authority assigns a school according to residence and capacity;
5. parents enter the Beijing compulsory-education portal and complete information collection;
6. the system generates a registration number;
7. parents take the proof package and registration number to the assigned school;
8. the school prints the student information-collection form;
9. the parent signs it;
10. the school retains the signed form and document copies.

Official source:
https://www.beijing.gov.cn/zhengce/zhengcefagui/201905/t20190522_58382.html

This gives the repository a durable state model:

`Web registration`
!= `document review initiated`
!= `document review passed`
!= `local-study certificate issued`
!= `school allocated`
!= `information collection confirmed`
!= `paper form printed`
!= `parent signed`
!= `school retained records`
!= `student record created`
!= `child attended`.

### Key archaeological lesson

Calling the system “网上报名” or “入学服务平台” must not erase the offices, paper, stamps, signatures, and school-side actions surrounding it.

This is another case of **hybrid digitality** rather than full digitization.

---

## 6. Mandatory information collection changes the evidentiary meaning of an absent record

2014 reporting states that children who did not participate in the information-collection system would not be able to proceed normally with primary-school entry.

Source:
https://www.chinanews.com/edu/2014/04-30/6123278.shtml

The 2015 Shijingshan plan similarly states that failure to complete required information collection would prevent normal admission.

Official source:
https://www.beijing.gov.cn/zhengce/gfxwj/qj/201905/t20190522_58365.html

This is not merely a “convenience website”. It is a **transactional gate**.

However, archival absence is still ambiguous:

`no surviving public page/account trace`
may mean
- the archival crawler could not see authenticated state;
- the family used a service window / late-arrival exception;
- the record existed only in protected systems;
- the child never completed the process.

Therefore public-Web absence cannot be converted directly into “child did not enroll”.

---

## 7. The Web account owner, form operator, legal guardian, and child are different entities

The enrollment object requires at least four identities:

1. **physical child** — person receiving compulsory education;
2. **legal guardian** — person legally responsible for application / signatures;
3. **Web operator** — person typing into the site, which may be a parent, relative, school staff member, service-window worker, or helper;
4. **institutional record subject** — identity represented by hukou, residence and student-record databases.

Never infer:

`child record == child Web account`

or

`guardian named on form == person at keyboard`.

In some historical workflows, school or local staff performed data entry. Even when the system was nominally “parent online”, the repository should not infer independent digital literacy from successful submission unless evidence says the parent personally operated it.

---

## 8. Enrollment state and student-record state can diverge in real life

A 2014 People’s Daily case is a useful reality check. A child who had moved from Gansu to live with his mother in Beijing had already spent a year attending a school, but the family later learned that the student record could not be transferred in a way that supported normal progression to junior secondary education.

Source:
https://edu.people.com.cn/n/2014/0807/c1006-25421226.html

For old-Web analysis this proves why the following states must not be collapsed:

`physical attendance`
!= `recognized enrollment`
!= `student record attached to destination school`
!= `progression eligibility`.

An archived school website saying a child “在校就读” would not by itself prove the student-record path was settled.

---

## 9. Shanghai 2015 provides a second platform target, but it should not be conflated with Beijing

Contemporary 2015 reporting records Shanghai’s new compulsory-education admission system at:

`http://www.shrxbm.cn`

and describes a platform through which parents could read city / district policy, query child admission information, receive public-school admission notices, and perform online private-school registration.

Source:
https://edu.people.com.cn/n/2015/0205/c1053-26511786.html

This is a second valuable historical host, but its transaction model and target population must be reconstructed separately.

Do not infer that because Beijing and Shanghai both had citywide Web admission services in 2014–2015 they shared:

- software lineage;
- browser requirements;
- field names;
- identity-verification architecture;
- school-seat allocation logic;
- migrant-child eligibility rules;
- student-record integration.

Those are jurisdiction-specific claims.

---

## 10. Public shell / private child-state asymmetry

Compulsory-school admission has an unusually strong archival asymmetry.

### Likely to survive publicly

- policy explanations;
- school lists;
- district boundaries;
- deadlines;
- screenshots in news reports;
- parent instructions;
- public portal hostname;
- user manuals;
- document checklists;
- general workflow diagrams;
- technical-support phone numbers.

### Designed not to survive publicly

- child name and identity number;
- guardian identity;
- actual residence;
- temporary / residence permit details;
- family hukou;
- employment and social-insurance evidence;
- document-review result;
- rejection reason;
- school allocation;
- student-record number;
- signed information-collection form;
- later transfer and progression state.

Therefore a Web archive can preserve the **rules of entry** far better than the **life course of any entrant**.

Call this:

**public-shell / private-child-state asymmetry**.

---

## 11. Eligibility-state / seat-state asymmetry

For migrant families, a second archival gap is especially important:

`eligible to receive local compulsory education`
!= `assigned requested school`
!= `assigned any school`
!= `school accepted child`
!= `child attended continuously`.

The 2015 Yanshan document explicitly says assignment depended on residence and school capacity; capacity exhaustion could trigger adjustment to another school.

Thus a preserved `审核通过` screenshot would still not prove which classroom the child entered.

Call this:

**eligibility-state / seat-state asymmetry**.

---

## 12. Record-portability / service-portability asymmetry

The national student-record system demonstrates another gap:

`record can move`
!= `public service entitlement moves`.

A national record identifier and online transfer workflow can reduce the burden of carrying educational records between provinces, yet destination admission remains governed by local rules, school capacity, residence and other conditions.

This distinction is essential whenever later observers read “全国联网” as if schooling itself had become nationally fungible.

Call this:

**record-portability / service-portability asymmetry**.

---

## 13. Deadline-state loss

Enrollment systems encode unusually consequential time windows.

States may include:

`registration not yet open`
→ `registration open`
→ `draft saved`
→ `submitted`
→ `eligibility review pending`
→ `supplement required`
→ `passed / failed`
→ `confirmation window`
→ `window closed`
→ `late-arrival manual route`.

A later archived snapshot may show only a closed portal or policy page. It cannot reconstruct what a family saw at 23:45 on the final day or whether the backend accepted its last submission.

This is **deadline-state loss**.

The distinction matters because contemporary 2014–2015 descriptions explicitly say missing the information-collection window can affect normal admission, while some late-arrival service-window exceptions remained.

---

## 14. Cross-system verification makes provenance harder, not easier

Digitized admission increasingly depended on other databases:

- public-security identity data;
- hukou / temporary-residence data;
- education student records;
- employment / social-insurance data in some localities;
- local housing / residence evidence;
- school capacity and assignment data.

A Web result such as `审核通过` may therefore be a **derived state**, produced from records whose own provenance is outside the admission website.

Future reconstruction should distinguish:

`field typed by guardian`
from
`field returned by external database`
from
`field manually verified by clerk`
from
`derived eligibility decision`.

Without manuals, API documents, source code, backend logs or explicit contemporary technical descriptions, do not infer which fields were authoritative or how conflicts were resolved.

---

## 15. Security and privacy boundary

Historical school-admission records contain children’s personally identifying and family information. The repository should **not** attempt to recover or republish private historical applications merely to make the transaction chain more concrete.

Appropriate objects include:

- blank forms;
- official manuals;
- publicly released screenshots;
- public workflow pages;
- public policy Q&A;
- aggregate statistics;
- redacted official cases;
- first-person materials voluntarily published by the family where necessary and proportionate.

Do not collect or expose a historical child’s identity number, private address, guardian employment evidence, phone number, or student-record identifier.

This is not a missing-evidence defect; it is a deliberate research boundary.

---

## 16. M1 capture status

### Candidate historical original hosts

Confirmed by contemporaneous sources:

- `http://yjrx.bjedu.cn` — Beijing compulsory-education admission service, publicly announced in April 2014 for opening 1 May 2014.
- `http://www.shrxbm.cn` — Shanghai compulsory-education admission system, documented in February 2015.

### Archive attempt in this slice

Searches were run for historical archive references and surviving 2014–2015 documentation around both hosts. This slice recovered strong contemporaneous URL evidence and detailed workflow descriptions, but did **not** obtain a historical replay that was actually opened and verified for all of the repository’s minimum capture dimensions:

- exact original URL;
- capture URL;
- capture datetime;
- replay / HTTP state;
- Content-Type and charset;
- DOM structure;
- form actions;
- script / iframe / subresource dependencies;
- authentication / session boundary;
- a second historical time point for comparison.

Therefore:

**M1 verified historical Chinese compulsory-education enrollment capture: NOT ACHIEVED IN THIS SLICE.**

Do **not** rewrite this as “Wayback did not preserve it.” We have only failed to establish a verified capture in this run.

### Explicit UNKNOWNs

For the 2014 Beijing portal and 2015 Shanghai portal, unless future historical capture / manual evidence resolves them, keep the following UNKNOWN:

- browser compatibility requirements;
- IE document mode;
- ActiveX use or non-use;
- exact charset;
- front-end framework;
- server-side framework;
- CAPTCHA implementation;
- authentication/session implementation;
- HTTPS availability and enforcement;
- exact form endpoint structure;
- API/database linkage details.

Do not infer these from generic 2010s Chinese government-site conventions.

---

## 17. Evidence table

| Claim | Evidence | Grade | Important boundary |
|---|---|---:|---|
| 1998 migrant-child schooling already required a cross-locality approval/application workflow | 1998 regulation text preserved by CERNET | A-/B+ | pre-Web policy, not proof of any household outcome |
| 2003 destination government/public schools became central policy responsibility | State Council / MOE text | A | implementation varied locally |
| 2007 migrant parents still publicly asked about urban borrowing fees | MOE public Q&A | A | published questions are selection-biased |
| 2014 national student-record system enabled online cross-province transfer workflow | MOE | A | record portability != admission eligibility |
| Beijing launched unified compulsory-education service at `yjrx.bjedu.cn` in 2014 | contemporaneous Beijing / national reporting | A-/B+ | exact page implementation still unknown |
| non-Beijing-hukou workflow still required offline document review | 2014–2015 instructions and official district rules | A-/B+ to A | “online” was hybrid |
| 2015 Yanshan workflow included eligibility certificate, Web collection, registration number, school printout and guardian signature | Beijing government document | A | still does not prove actual attendance |
| Shanghai used `www.shrxbm.cn` in 2015 | contemporaneous report | A-/B+ | do not infer same architecture as Beijing |
| a child could physically attend while record/progression remained unresolved | 2014 People’s Daily case | A | individual case, not prevalence estimate |

---

## 18. What this changes in the old-Web model

This research adds a missing class of Chinese Web object: **the page that does not merely represent a user, product, message, or application, but participates in deciding whether a child is institutionally legible enough to enter a local public service.**

The old Web therefore should not be reconstructed only as information publishing and community culture. By the early-to-mid 2010s it also contained transaction gates whose consequences extended across years of a person’s life.

The correct archaeological question is not:

> “Did this city have online school enrollment?”

but:

> “Which state transition did the Web perform, which remained in an office or another database, and which decisive outcome was never public Web data at all?”

For migrant children the answer is especially consequential because a failed state transition could mean more than a failed form submission: it could determine whether a child lived with parents in the destination city or returned to the registered home locality for school.

That is the direct cross-link to `how-people-lived`: **a Web eligibility state can become a family co-residence state.**
