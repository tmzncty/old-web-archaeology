# ONLINE RECRUITMENT / JOB AD / ACCOMMODATION / APPLICATION / EMPLOYMENT STATE GAPS, 1999–2015

Status: research note / cross-repo slice  
Scope: Chinese Web and Web-adjacent recruitment systems, c. 1999–2015  
Companion ordinary-life note: `tmzncty/how-people-lived/topics/from-food-and-lodging-jobs-to-youth-inns-arrival-accommodation-job-housing-bundling-and-city-trial-optionality-china-1980-2026.zh-CN.md`

## 0. Why this belongs in old-web archaeology

Old recruitment pages look deceptively easy to interpret. A surviving page may show:

```text
岗位名称
工资
工作地点
包吃住
立即申请
```

It is tempting to read the page as if it were a stable database record of a real job and a real dormitory.

That is unsafe.

For ordinary-life history, a recruitment page sits between at least three different systems:

1. **public information system** — what job/ad/profile the Web exposed;
2. **private transaction system** — résumé submission, recruiter review, phone calls, interview and offer;
3. **physical employment / accommodation system** — whether the vacancy, workplace, dorm bed and promised benefit actually existed when the applicant arrived.

This note therefore does not attempt to write a general history of Chinese online recruitment. It establishes archaeological boundaries for a narrower but consequential question:

> **When a historical Chinese recruitment page said that a distant job existed — especially a “包吃住 / 包住” job — what exactly can the archived Web prove, and what remains outside the archive?**

The repository's normal METHOD contract applies: platform/site/page/account/capture/claim remain separate, a locator is not a verified capture, and `exists != available != used != popular != caused`.

---

## 1. Research-unit graph

Do not collapse the following objects:

```text
physical employer
actual establishment / factory / store
actual vacancy
employer HR department
labor agency / intermediary
individual recruiter
poster identity
recruitment platform
platform employer account
employer profile page
job listing
listing revision
print advertisement
BBS / campus repost
search-results page
job seeker
job-seeker account
résumé
application event
platform delivery state
recruiter inbox / ATS state
shortlist state
phone/SMS/email contact
interview appointment
actual interview
offer
acceptance
physical arrival
employment start
wage/payroll state
accommodation promise
actual dormitory
bed inventory
bed assignment
room condition
housing deductions / deposit
continued occupancy
employment end
dorm exit
archive capture
research claim
```

A Web archive can preserve some of these very well and be almost silent about the others.

---

## 2. Minimum state distinctions

### 2.1 Listing / vacancy

```text
job listing exists
!= listing is current
!= employer is still recruiting
!= number of openings remains positive
!= displayed location is actual work location
!= listing was posted directly by employer
!= poster was authorized by employer
```

### 2.2 Application / recruitment outcome

```text
account created
!= résumé completed
!= résumé made searchable
!= application submitted
!= platform accepted submission
!= recruiter received it
!= recruiter opened it
!= applicant shortlisted
!= applicant contacted
!= interview scheduled
!= interview attended
!= offer issued
!= offer accepted
!= actual start of employment
```

### 2.3 “包住 / 包食宿”

```text
listing text says “包住”
!= physical dormitory exists
!= bed available on applicant's arrival date
!= bed is free
!= utilities are free
!= no deposit or payroll deduction exists
!= room occupancy matches wording or expectation
!= dorm is near workplace
!= transport between dorm and workplace is provided
!= spouse / child can co-reside
!= worker receives a bed after actual hiring
!= bed remains available after transfer / resignation / layoff
```

For archaeological writing, **accommodation language in a job ad is a claim about the advertised compensation bundle**, not proof of the physical dormitory outcome.

---

## 3. 1999–2004: print and Web recruitment were one hybrid publication system

### 3.1 51job's 2004 F-1 is unusually useful primary evidence

51job, Inc.'s 2004 SEC filings describe a deliberately hybrid recruitment system.

The company stated that:

- `www.51job.com` had operated since 1999;
- *Career Post Weekly* was a city-specific print recruitment publication;
- all recruitment advertisements appearing in *Career Post Weekly* were also posted to `www.51job.com`;
- the website also carried online-only advertisements;
- Web recruitment advertisements were updated hourly;
- job seekers could post résumés;
- employers could manage résumé/candidate review through Web-based eHire tools;
- as of 2004-06-30 the company reported approximately 6.9 million user accounts created since site launch and about 4.6 million online résumés.

Primary sources:

- 51job, Inc., Form F-1, filed 2004-07-07:  
  https://www.sec.gov/Archives/edgar/data/1295484/000114554904000896/u99016fv1.htm
- later 2004 filing with service description:  
  https://www.sec.gov/Archives/edgar/data/1295484/000114554904001289/u99016a6e424b4.htm

Evidence grade:
- **A** for “the company stated that its service worked this way at filing time.”
- Company-reported scale is not independent audience measurement.

### 3.2 Archaeological consequence: print and Web copies may be one evidence family

Because 51job explicitly says print ads were mirrored online, the following cannot automatically be counted as two independent confirmations:

```text
Career Post Weekly advertisement
+ same 51job Web advertisement
```

They can independently preserve different artifacts, but the factual job claim may originate from one employer submission / one platform publishing workflow.

This is a **print–Web duplication bias**.

An archived Web copy can still be valuable because it may preserve:

- exact wording;
- structured fields;
- original URL shape;
- publication/update timestamps;
- platform navigation;
- application link;
- employer-profile relationship.

It does not become a second independent witness that the job actually existed.

---

## 4. 2004–2005 campus BBS as recruitment-navigation infrastructure

The old Chinese Web did not consist only of recruitment portals. Campus BBS users actively maintained lists of recruitment URLs and application deadlines.

### 4.1 2005 Little Lily artifact: exact historical recruitment URLs

A Google Groups-preserved message identifies itself as originating from Nanjing University's Little Lily BBS and gives a 2005 campus-recruitment navigation list including:

```text
http://campus.chinahr.com/
http://graduate.zhaopin.com/campus/company-m.jsp
http://www.51job.com/default-xs.php
```

It also listed company-specific online application routes and deadlines.

Source:
- message preserved by Google Groups, posted 2005-11-04, carrying an original Little Lily timestamp of 2005-09-07:  
  https://groups.google.com/g/cn.bbs.campus.job.northeast/c/WNPANVAA37w

Evidence grade:
- **A-/B+ contemporary community artifact** for the fact that these URL strings were circulating as recruitment navigation in 2005.
- It is **not** itself an opened archive capture of those target URLs.

Important representation gap:

> **Google Groups-preserved message content != original campus-BBS DOM / charset / thread context / board ranking / login state.**

The text helps recover an address graph while losing much of the original browsing environment.

### 4.2 2004 Shenzhen job-search guide: Web guidance and physical arrival coexisted

A 2004 campus-BBS-circulated “深圳求职指南（2004版）” describes its target job seeker as a young person with some education/experience, little money, and limited first-hand knowledge of Shenzhen. It explicitly treats online material and offline books/guides as parallel sources.

Source:
- Google Groups-preserved BBS post, 2004-10-05:  
  https://groups.google.com/g/cn.bbs.campus.job/c/74T0OBfEfcY

Evidence grade:
- **B contemporary/near-contemporary individual guidance**.

This matters archaeologically because a recruitment URL by itself can overstate how self-contained the Web was. The user still needed:

- cash;
- a bed;
- public transport knowledge;
- phone/email access;
- physical recruitment markets/interviews;
- local verification.

A preserved recruitment site captures only one layer of the execution stack.

---

## 5. 2005 Jobar: the missing archaeology of “arrival infrastructure”

A particularly useful 2005 campus-BBS artifact advertises `http://www.jobar.com.cn/` as “众博学生公寓 / Jobar”, aimed at students traveling for job search, exams and travel.

The post's service bundle included:

- low-price beds with nightly / longer-stay pricing;
- free broadband for online job search;
- cheap résumé printing/binding;
- buses reaching talent markets;
- weekly job-fair information;
- maps and local transport/life information;
- local Xiaolingtong rental to reduce nonlocal communication cost;
- a resident population described as other job seekers.

Source:
- 2005-06-05 BBS artifact preserved by Google Groups:  
  https://groups.google.com/g/cn.bbs.campus.job.southeast/c/Sl-I3WMkEqU

Evidence grade:
- **A-/B+** for the historical post and the service claims made by its poster.
- **UNKNOWN** for actual occupancy, service consistency, business duration and physical conditions without independent evidence.

### 5.1 Why this is an old-Web object, not merely a housing anecdote

The Jobar post demonstrates that early online job search depended on a stack that included a physical place to use the network:

```text
bed
+ shared/private PC access or broadband access
+ printing
+ local transport information
+ telephone reachability
+ job-fair calendar
+ recruitment websites
```

The old Web can preserve the URLs and advertising language while losing the **bed inventory state** that made the Web usable by a visitor with little money.

This produces a new archaeological asymmetry:

## **recruitment-page survival / arrival-infrastructure loss**

Twenty years later, a national recruitment portal may be well cited and partially archived, while cheap student lodging, public computer access, printing shops, bus routes to job fairs and short-term bed availability are far more weakly preserved.

That preservation pattern can make online recruitment history look more “fully online” than lived recruitment actually was.

---

## 6. Accommodation claims inside recruitment text

Contemporary recruitment material commonly used compact compensation phrases such as:

- 包吃住
- 包食宿
- 提供住宿
- 食宿免费 / 有扣费
- 当天/次日安排住宿

These phrases must be treated as **structured promises or ad-copy claims**, not housing observations.

A 2008 labor-market report found job seekers explicitly asking for employer accommodation because market rooms were expensive; another worker would not decide to stay only from the “工资 + 包吃住” wording but continued to inspect/discuss the actual work and accommodation conditions.

Source:
- 温州新闻网 / 新浪, 2008-02-19:  
  https://news.sina.com.cn/s/2008-02-19/142313436739s.shtml

A 2018 Beijing labor-market report similarly found surrounding-city employers highlighting food/lodging and a job seeker saying he wanted a dormitory because even a single room cost more than RMB 1,000/month.

Source:
- 北京晨报 / 新华网, 2018-03-27:  
  https://www.xinhuanet.com/politics/2018-03/27/c_1122594358.htm

These later sources are outside or at the edge of this repository's 1995–2015 primary scope, but they clarify why the older “包住” field must be modeled as consequential rather than decorative.

---

## 7. Employment bundle state: the dormitory is not independent of production state

A 2019 on-site report about Foxconn Zhengzhou recorded a worker describing cancellation of factory-to-dorm shuttle buses and dormitory laundry service; dormitory buildings were also consolidated according to employee numbers. A recruiter in Shenzhen told the reporter that successful recruits could be assigned accommodation immediately or the next day.

Source:
- 新京报 / 人民网, 2019-02-15:  
  https://it.people.com.cn/n1/2019/0215/c1009-30676805.html

Again, this is outside the old-Web core period but helps formalize a state relation that likely applies to earlier cases and must be tested, not assumed:

```text
production demand
→ headcount
→ recruitment intensity
→ dormitory occupancy / building use
→ shuttle / daily-life service provision
```

An old job ad saying “包住” does not contain this dynamic state machine.

---

## 8. Proposed evidence model for historical recruitment/accommodation pages

For any future capture or research note, record at minimum:

```yaml
platform:
site_host:
page_type:            # search / listing / employer-profile / apply / help / BBS-post
original_url:
capture_url:
capture_datetime:
accessed_at:
archive_source:
http_or_replay_state:
content_type:
charset_observed:
browser_assumption:

listing_id:
listing_created_or_updated_at:
employer_name_as_displayed:
poster_type_claimed:  # employer / agency / unknown
job_title:
job_location_as_displayed:
wage_as_displayed:
accommodation_text:
food_text:
fee_or_deduction_text:
application_endpoint:
contact_channel_types:

provenance_grade:
confidence:
independent_evidence_family:
privacy_redactions:
unknowns:
```

Do **not** preserve ordinary historical applicants' personal phone numbers, email addresses, identity documents or résumés merely because an archive exposes them. The research question is platform and transaction structure, not re-identifying individuals.

---

## 9. Archive-gap catalogue

### 9.1 listing-text survival / vacancy-state loss

A listing can survive after its vacancy is filled, withdrawn or duplicated.

```text
archived listing at T
!= vacancy open at T
```

Unless the platform explicitly records closed/expired state, the archive only proves page representation.

### 9.2 benefit-claim survival / dormitory-reality loss

“包住” may survive permanently in HTML while the physical dormitory's:

- location;
- room size;
- number of occupants;
- fees;
- utilities;
- curfew/rules;
- bed availability;
- family eligibility;
- post-resignation grace period

remain completely invisible.

### 9.3 application-shell survival / recruiter-decision loss

A working-looking “立即申请” button in a replay cannot prove:

- the historical form submitted correctly;
- the backend accepted it;
- the résumé reached employer tools;
- a recruiter reviewed it;
- a phone/email response followed.

### 9.4 search-result survival / ranking loss

Even when a listing URL survives, the historical query that surfaced it may not.

Need separate evidence for:

```text
listing existed
!= listing was discoverable for query X
!= listing ranked on page 1
!= job seeker actually saw it
```

Dynamic ranking, paid placement, personalization and expiry can make the historical search surface unrecoverable.

### 9.5 BBS mirror / original-BBS representation gap

Google Groups currently preserves valuable content carrying provenance strings from campus BBS systems. It can recover:

- post text;
- date strings;
- URL strings;
- sometimes board/source markers.

It does not automatically recover:

- original terminal/Web layout;
- encoding path;
- board hierarchy at the time;
- edits/deletes;
- read counts;
- exact threading;
- user session context;
- whether the post was promoted/reposted elsewhere.

Thus use it as a preserved artifact with a representation caveat, not a substitute for a verified original capture.

### 9.6 cross-channel survival asymmetry

The recruitment path may continue through:

```text
Web listing
→ telephone
→ SMS
→ e-mail
→ talent market
→ agency storefront
→ factory gate
→ dorm viewing
```

The Web archive disproportionately preserves the first node.

### 9.7 print–Web duplication bias

Where a platform says it mirrors print ads online, the print issue and website may be two artifacts of one publisher workflow. Do not use them as independent factual confirmation of employer claims without checking source lineage.

---

## 10. Exact historical URLs currently identified

Contemporary evidence in this slice provides at least these candidate original URLs:

```text
http://www.51job.com/
http://www.51job.com/default-xs.php
http://campus.chinahr.com/
http://graduate.zhaopin.com/campus/company-m.jsp
http://www.jobar.com.cn/
```

They are useful locator seeds.

However:

> **A historical URL string in a 2005 BBS post is not an M1 archive capture.**

This slice has not yet produced a capture for these recruitment/accommodation objects that has been actually opened and jointly verified for:

- original URL;
- capture URL;
- capture datetime;
- replay/HTTP state;
- Content-Type and charset;
- DOM/form action;
- script/iframe/subresource survival;
- application/session boundary;
- a second historical time point.

Therefore:

## **M1 verified historical Chinese recruitment/accommodation capture: NOT ACHIEVED IN THIS SLICE.**

This is not a claim that Wayback, Common Crawl or another archive contains no relevant captures. It only records the current evidence boundary.

---

## 11. Browser / encoding / implementation status

Current status for the candidate recruitment/accommodation sites:

```text
historical IE requirement: UNKNOWN
historical Netscape/other browser behavior: UNKNOWN
ActiveX requirement: UNKNOWN
Flash/Java dependency: UNKNOWN
GB2312/GBK/UTF-8 per target historical page: UNKNOWN
ASP/JSP/PHP/server framework: UNKNOWN
historical TLS/certificate behavior: UNKNOWN
form submission method/endpoints: UNKNOWN unless original capture is verified
```

Do not infer these merely from “2005 Chinese website” stereotypes.

The SEC filings prove that 51job operated Web-based résumé/employer tools; they do not prove a specific client browser implementation.

---

## 12. Privacy boundary

Historical recruitment material has unusually high re-identification risk because pages may combine:

- full name;
- phone;
- e-mail;
- age;
- education;
- home town;
- employer history;
- desired city;
- salary expectation;
- sometimes identity or address data.

Repository practice for this subject should be stricter than a generic portal homepage case:

- do not reproduce ordinary job seekers' résumés;
- do not copy personal phone/e-mail from old BBS recruitment posts into research notes unless essential to a claim (normally it is not);
- use historical employer/service URLs and aggregate platform structures instead;
- if a public archived personal résumé is necessary to demonstrate a feature, summarize/minimize and avoid searchable identifiers;
- “archive accessible” is not a justification for republishing deleted personal job-search data.

The Jobar BBS artifact, for example, includes historical contact details; this note intentionally preserves the service URL and service description while omitting the individual's contact fields.

---

## 13. What this changes about interpreting Chinese old Web

Recruitment sites are not merely content sites. They are **transaction-front-end ruins** for processes whose decisive states mostly lived elsewhere.

A fully preserved 2005 listing can answer:

- what the platform displayed;
- which fields were used;
- what employer/poster claimed;
- what URL and navigation model existed;
- whether “住宿” was represented as a searchable/visible benefit;
- what application action the UI offered.

It usually cannot answer on its own:

- whether the vacancy remained open;
- whether the employer authorized the post;
- how many people applied;
- whether a particular résumé was reviewed;
- whether the job seeker arrived;
- whether the promised bed existed;
- what the room looked like;
- whether fees were deducted;
- whether the worker stayed;
- what happened to the worker's housing when employment ended.

This is exactly the kind of domain where **page preservation is much stronger than life-state preservation**.

---

## 14. Cross-repo insight: the Web made distant work searchable before it made arrival cheap

The ordinary-life companion note uses this archaeology to make a larger but carefully bounded claim.

By the early 2000s, a young person could increasingly:

```text
see a distant job before leaving home
→ submit a résumé online
→ receive phone/email contact
```

But the moment the person stepped off a train, the execution problem became physical again:

```text
where to sleep
where to print
how to reach the talent market
how to receive calls cheaply
how long cash lasts before first wage
```

The 2005 Jobar BBS artifact is especially valuable because it exposes this missing middle layer. A cheap bed, broadband, résumé printing, transport information and local communication were sold as one job-search package.

Later mobile Internet can make job information nearly continuous, but the 2018 evidence still finds workers making employment decisions around employer-provided accommodation. The persistence of that condition is evidence that **information reachability and housing executability are different technological histories**.

---

## 15. Next evidence targets

High-value follow-up, without broad crawling:

1. Verify at least two historical captures of one recruitment object, preferably `www.51job.com/default-xs.php` or a 2004–2006 listing/help page.
2. Search for a historical `jobar.com.cn` capture and establish whether the service page corroborates the BBS claims.
3. Find a contemporaneous platform help/manual page defining fields for “食宿/住宿/福利” and whether they were structured or free-text.
4. Locate one 2003–2010 actual job-listing capture where accommodation language is visible, while minimizing ordinary-person contact data.
5. Compare one platform page with one BBS repost to document how structured job fields were flattened into plain text.
6. Identify whether historical online application forms exposed submission acknowledgements, application history or status pages.
7. Record a negative case where an exact original URL is known but dynamic/login/robots/subresource loss prevents transaction reconstruction.

Do not advance to a full M1 case until capture metadata and second-time-point evidence meet the repository contract.

---

## 16. Current conclusion

This slice adds a specific warning to old-Web archaeology:

> **An archived job ad is evidence that a promise was displayed, not evidence that the promised life was executable.**

For remote work migration, the largest missing state may be something as mundane as a bed.

The Chinese Web of the early 2000s made national job information increasingly searchable; campus BBS posts helped users route themselves among recruitment sites; cheap job-search lodging could bundle broadband and résumé printing around that Web. Yet the decisive transition from “I found a listing” to “I can actually stay in this city long enough to take the job” often left almost no public Web trace.

That gap should be preserved as an archaeological result, not silently filled by the surviving page.