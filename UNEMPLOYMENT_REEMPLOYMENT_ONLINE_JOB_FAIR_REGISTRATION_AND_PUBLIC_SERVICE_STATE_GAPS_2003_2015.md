# Unemployment / Reemployment Online Job Fair, Registration and Public-Service State Gaps, China 2003–2015

## Scope

本研究包聚焦 **2003–2015 中文 Web 与公共就业 / 再就业服务的交界**：

- 网上招聘会；
- 公共就业网站；
- 劳动力市场信息系统；
- `12333` 电话服务；
- 《再就业优惠证》等纸质身份接口与后台数据库；
- 失业 / 再就业状态如何从线下柜台逐步进入可联网管理的公共服务系统。

1998–2002 的再就业服务中心、下岗与失业保险并轨只作为理解 2003 年 Web 状态机的必要前史，不把本仓 scope 扩成完整劳动制度史。跨国公共就业系统前史与 2020 年以后的生活史比较主要写入 companion：

- `tmzncty/how-people-lived/topics/from-xiagang-to-registered-unemployment-reemployment-and-digital-public-employment-services-china-1998-2026.zh-CN.md`

本文件遵守 `docs/METHOD.md`：

> site / page / account / backend record / paper credential / archive capture / lived outcome 必须分开。

---

# 1. Why this belongs in old-Web archaeology

就业 Web 很容易被保存成一张“岗位页面”的历史，但普通人的真实事务并不是：

```text
看到网页 → 找到工作
```

更接近：

```text
现实工作中断
→ 行政身份被认定
→ 取得/验证证件
→ 获得公共服务资格
→ 找到可访问的终端
→ 打开网站 / 拨打热线 / 到窗口
→ 看见职位
→ 提交信息
→ 用人单位收到
→ 达成初步意向
→ 面试 / 核验 / 录用
→ 实际到岗
→ 新劳动关系和社保记录建立
```

其中很多关键状态根本不在公开 Web 页面里。

因此这里研究的是 **state gaps**，不是“最早网上招聘”竞赛。

---

# 2. Necessary prehistory: 1998–2002 public-employment state machine

## 2.1 `xiagang` was not identical to registered unemployment

1998 年深圳正式文件说明，再就业服务中心可以：

- 发放基本生活费；
- 代缴养老、失业、医疗保险；
- 提供培训和就业指导；
- 托管部分下岗职工，期限原则上不超过 3 年。

Original/current carrier of historical official text:
- https://www.sz.gov.cn/zfgb/1998/gb143/content/post_10123116.html
- https://www.sz.gov.cn/zfgb/1998/gb145/content/post_10124194.html

Evidence: **A for the historical regulation text; current government HTML is the present carrier, not a verified 1998 Web capture.**

2001 年辽宁并轨文件又明确规定，新减员原则上不再进入再就业服务中心，而是解除劳动关系后衔接失业保险和劳动力市场。

Source:
- https://www.ln.gov.cn/web/zwgkx/zfwj/szfwj/6D69769EF6384624B98CF5E8A65A12F1/index.shtml

Evidence: **A for the dated regulation; current carrier is not assumed to reproduce original 2001 DOM.**

### State gap 01 — `lived-no-job / administrative-label gap`

```text
not doing original job
≠ xiagang
≠ registered unemployed
≠ internal retirement
≠ policy-eligible reemployment target
```

A future archive that preserves only the label “下岗失业人员” can therefore flatten several legally different states.

---

# 3. 2003 paper credential + networked backend: the Web-visible world was only one layer

The Guangdong 2003 `再就业优惠证` rules are unusually valuable because they describe both the **paper credential** and the **information system behind it**.

The rules distinguish eligible categories including:

- SOE laid-off workers;
- SOE unemployed workers;
- persons requiring placement after SOE closure/bankruptcy;
- certain long-term urban unemployed receiving minimum-living support.

Applicants had to provide different proofs depending on state: `下岗职工证`, employer proof that the labor relationship had not been terminated, `失业证`, social-insurance booklet, low-income-support evidence, etc.

The same regulation says issuance, use, annual review and cancellation were to be entered into the provincial labor-market information system and a `下岗失业人员再就业扶持管理系统`.

Source:
- Shenzhen government gazette carrying Guangdong regulation, dated 2003-07-03:
  https://www.sz.gov.cn/zfgb/2003/gb350/content/post_4976320.html

Evidence: **A — contemporary formal regulation text.**

### State gap 02 — `paper-credential / backend-record gap`

```text
paper certificate physically exists
≠ backend record exists correctly
≠ certificate is current after annual review
≠ another department has queried/accepted it
≠ benefit has actually been granted
```

### State gap 03 — `lived-unemployment / credential-eligibility gap`

Someone can be genuinely without stable work but fall outside the certificate categories.

The archive-friendly object — a certificate form or help page — is not the same as the lived population.

### Historical visibility asymmetry

The regulation and backend field structure can survive while the daily experience does not:

- who filled the form for a low-literacy applicant;
- how many trips were required;
- whether a local office had working terminals;
- whether the database was online that day;
- how long corrections took;
- whether the holder actually obtained a job.

Those remain unknown in this slice.

---

# 4. January 2003: a national online job fair for laid-off and unemployed youth

A Xinhua report dated 2003-01-27 describes the first national online recruitment fair for laid-off / unemployed youth and gives the historical public locator:

```text
http://www.chinajc.com/
```

Reported event facts:

- the online “recruitment hall” received about 1.659 million visits/clicks (`人次`);
- 1,874 enterprises offered 41,376 positions;
- 7,209 people reached **preliminary employment intentions** online;
- the organizer explicitly used Youth League work sites/facilities to create conditions for laid-off and unemployed youth to log onto the site.

Contemporary user case:

- Shanxi youth Wang Zhigang said previous Internet and talent-market searches often exposed him to high education requirements;
- he found the targeted service-sector / front-line positions more compatible with his situation;
- the report says he found a security-guard position at a Beijing construction company through the site.

Source:
- Xinhua, 2003-01-27, preserved by Sina:
  https://news.sina.com.cn/s/2003-01-27/203340616s.shtml

Evidence: **B — contemporary news report with a user interview and operation-level observations.**

## 4.1 Do not repeat the headline's stronger inference

The headline says the event “helped seven thousand find new jobs,” but the quantitative body text is narrower:

```text
7,209 preliminary online employment intentions
```

Therefore the repository records:

### State gap 04 — `online-intent / actual-employment gap`

```text
job visible
→ expression/application
→ preliminary intent
→ interview/contact
→ offer
→ actual start
→ sustained employment
```

No source obtained in this slice gives a complete conversion funnel from 7,209 preliminary intentions to actual starts and retention.

**Do not rewrite 7,209 as verified stable jobs.**

---

# 5. Public Web access without private Internet ownership

The same 2003 report says local Youth League organizations used their work facilities to provide necessary conditions for unemployed youth to **log onto the site**.

This is technically and socially important.

A public employment Web service could reach a person through:

```text
organization office / shared PC / public terminal
→ browser
→ chinajc.com
```

without requiring:

```text
home PC + home dial-up/broadband ownership
```

### State gap 05 — `service-online / private-terminal gap`

```text
online service exists
≠ target person owns a connected computer
≠ target person cannot use the service
```

Institutional/shared terminals create a third state.

This directly cross-links with the repository's existing work on Internet cafes and shared-terminal digital life: **access is a separate clock from ownership.**

### Unknown in this slice

We do not know the 2003 fair's access distribution among:

- home computers;
- Internet cafes;
- Youth League facilities;
- public labor-market terminals;
- friends/workplaces/schools.

Do not infer proportions.

---

# 6. The same year: `12333` shows that public-service interfaces were multi-channel

On 2003-05-27, the Ministry of Labour and Social Security formally issued the national public-service telephone number `12333`.

The notice required local systems to move toward one public number and specified no information-service fee beyond ordinary communication charges.

Source:
- Labour and Social Security Ministry, 劳社部函〔2003〕84号:
  https://www.mohrss.gov.cn/xxgk2020/fdzdgknr/zhgl/rlzyshbzxxh/202010/t20201031_394105.html

Evidence: **A — contemporary formal notice.**

### State gap 06 — `Web-page / public-service-channel gap`

Do not reconstruct 2003 employment service as a Web-only experience.

A more historically defensible stack is:

```text
street/community labor office
+ labor market hall
+ telephone 12333
+ paper certificate
+ backend labor-market information system
+ selected Web recruitment sites
```

A person could use one channel to learn what to do and another to execute it.

---

# 7. Backend networks preceded end-to-end personal Web transactions

Official 2001 and 2002 statistical bulletins report that public labor-market information networks were already being connected internally:

- 2001: among 100 modernization pilot cities, 64 had city-district real-time networking;
- 2002: 90 cities had city-district real-time networking.

Sources:
- 2001 bulletin:
  https://www.stats.gov.cn/sj/tjgb/qttjgb/qgqttjgb/202302/t20230218_1913248.html
- 2002 bulletin:
  https://www.stats.gov.cn/sj/tjgb/qttjgb/qgqttjgb/202302/t20230218_1913251.html

Evidence: **A — official near-contemporary annual statistical bulletins.**

### State gap 07 — `networked-backend / Web-frontend gap`

```text
employment office databases networked in real time
≠ job seeker has a Web account
≠ job seeker submits directly online
```

This is a recurring old-Web error: historians see an Internet-era date and assume the citizen-facing browser is the principal interface. Internal networks may be historically earlier and behaviorally more important.

---

# 8. 2014–2015: public recruitment Web becomes a multi-site infrastructure

By the end of the repository's main period, public/education recruitment was no longer a one-off novelty.

The 2015 national university-graduate employment network alliance recruitment weeks listed four public platforms:

```text
www.ncss.org.cn
www.chrm.gov.cn
www.chinajob.gov.cn
www.cjob.gov.cn
```

Four rounds were scheduled for spring, summer, autumn and winter.

Source:
- Ministry of Education + MOHRSS, notice dated 2015-03-11:
  https://www.moe.gov.cn/srcsite/A15/s3265/201503/t20150311_189363.html

Evidence: **A — contemporary official notice.**

A 2015 Beijing employment-service notice likewise describes an explicitly mixed model combining:

- in-person recruitment;
- campus service;
- network recruitment;
- print-media recruitment;
- policy consultation;
- real-name registration.

Source:
- Beijing Municipal HRSS, 2015-03-10/11 notice (current official carrier):
  https://rsj.beijing.gov.cn/xxgk/2024zcwj/202406/t20240617_3716918.html

Evidence: **A for the dated notice text; current publication wrapper is later.**

### State gap 08 — `national-portal / local-execution gap`

A national/public portal can expose opportunities while application, interview, identity checks and benefit execution still happen through local systems, local offices or employer channels.

### State gap 09 — `multiple-host / one-policy-event gap`

The same national recruitment event can be distributed across several hosts.

Therefore:

```text
one event name ≠ one canonical historical URL
```

Archive research must preserve the host list and not assume one surviving domain represents the whole event.

---

# 9. Candidate historical state chain

For 2003–2015 public reemployment Web, use at least the following states:

```text
A. Person's original work actually stops
B. Labor relationship retained / terminated / internally retired / other
C. Administrative unemployment/reemployment category assigned
D. Paper credential / certificate / ID exists
E. Backend record exists and is current
F. Public employment service entitlement exists
G. User can physically reach a window/phone/terminal/network
H. Public site/host is reachable
I. Job listing is visible
J. Person submits interest/application
K. Employer/service receives it
L. Preliminary employment intent exists
M. Identity/qualification/interview succeeds
N. Offer/placement exists
O. Person actually starts
P. New employment lasts long enough to become a meaningful reemployment outcome
Q. New labor/social-insurance records are established
```

Archive-visible pages usually cover only H–I and sometimes J.

The lived outcome is O–Q.

---

# 10. State-gap catalog

## 10.1 `lived-no-job / administrative-label gap`

Not working does not by itself tell us whether the person was legally/administratively `下岗`, `失业`, `内退`, or outside the recognized categories.

## 10.2 `administrative-label / credential gap`

A person in a qualifying category may not yet have obtained the paper credential required for some benefits.

## 10.3 `paper-credential / backend-record gap`

Paper and database can disagree, lag, or have different renewal/cancellation states.

## 10.4 `credential / actual-benefit gap`

Certificate eligibility does not prove a specific subsidy, tax preference, training placement or job was actually received.

## 10.5 `online-service / terminal-access gap`

Service availability does not imply household device ownership.

## 10.6 `terminal-access / browser-executability gap`

A shared terminal may still fail because of browser, network, account, encoding, script, plugin or site availability.

## 10.7 `job-visible / person-eligible gap`

A listing can be real but unusable because of education, age, city, skill, wage or schedule.

## 10.8 `application / employer-receipt gap`

Submission success must not be inferred from seeing a form.

## 10.9 `employer-receipt / preliminary-intent gap`

A received application is not a match.

## 10.10 `preliminary-intent / actual-start gap`

This gap is directly demonstrated by the wording of the 2003 online recruitment statistics.

## 10.11 `actual-start / sustained-reemployment gap`

Starting a job does not prove it lasted or restored previous income/security.

## 10.12 `Web-help / public-service-backend gap`

A Web page can describe an entitlement while the authoritative record remains in a non-public labor/social-security system.

## 10.13 `hotline-guidance / transaction-completion gap`

12333 can explain a procedure without itself being the backend that changes the employment/benefit state.

## 10.14 `national-event / local-process gap`

National branding can conceal different provincial/city systems and offline requirements.

## 10.15 `public-record / lived-income gap`

The system may know someone was placed or registered but not reconstruct informal side work, family support, debt, or actual household cash flow.

---

# 11. What the Web archive is likely to over-preserve

Public-employment Web has a strong **institutional-survivor bias**.

Likely to survive:

- official notices;
- event names/dates;
- host/domain locators;
- job counts;
- help text;
- policy eligibility;
- some public listings;
- press reports of successful cases.

Likely to disappear or never have been public:

- individual application payloads;
- rejected applications;
- telephone consultations;
- local-office notes;
- backend status transitions;
- internal reason codes;
- employer follow-up;
- informal work during unemployment;
- whether a person actually started and stayed;
- household financial coping during the gap.

This creates **public-record / ordinary-life asymmetry**.

A future researcher may see an immaculate 2003 policy page and conclude that a clean reemployment workflow existed. The person's actual life could still contain repeated trips, incomplete documents, borrowed terminal access and jobs that never progressed beyond an initial contact.

---

# 12. Historical locator notes

## 12.1 `www.chinajc.com`

Supported by 2003 Xinhua report as the China Youth Entrepreneurship Web locator used for the national online recruitment fair.

Evidence type: **B historical locator from contemporary report.**

Current status / domain continuity: **not established in this slice.**

Verified Wayback capture: **not achieved in this slice.**

Do not infer:

- original title string;
- exact homepage layout;
- charset;
- form action;
- account/login system;
- cookies/session behavior;
- whether the recruitment hall was static HTML, ASP/JSP/PHP, frames or another stack;
- browser requirement.

## 12.2 `www.ncss.org.cn`, `www.chrm.gov.cn`, `www.chinajob.gov.cn`, `www.cjob.gov.cn`

Supported by 2015 official recruitment-week notice.

Evidence type: **A for event/host association.**

That notice does not itself establish the exact 2015 HTML presentation of every host.

---

# 13. Browser / encoding / client assumptions — currently unknown

For `chinajc.com` 2003 recruitment pages, the following remain **unknown** because no verified historical capture was inspected:

- `Content-Type`;
- GB2312 / GBK / UTF-8 behavior;
- IE-version dependencies;
- screen-size assumptions;
- form controls and client-side validation;
- JS/browser sniffing;
- frameset/table layout;
- image/CSS completeness;
- login/session cookies;
- HTTPS or lack thereof;
- downloadable attachments;
- printer workflow.

Do not reconstruct these from generic “2003 Chinese Web” expectations.

---

# 14. Archive search status

This slice searched current Web indexes for the 2003 historical host and attempted Wayback candidate resolution, but **did not obtain and inspect a replay response that satisfies this repository's capture contract**.

Accordingly:

```text
candidate historical locator: YES
verified Wayback/WARC capture: NO, not in this slice
claim that Wayback has no capture: NOT MADE
```

Possible reasons for unresolved capture availability include:

- indexing/search limitations;
- host variation (`chinajc.com` vs `www.chinajc.com`);
- dynamic paths;
- archive access/replay restrictions;
- domain migration.

Next archive work should enumerate URL variants and record candidate capture metadata before attempting any browser reconstruction.

---

# 15. M1 status

**M1 — NOT ACHIEVED IN THIS SLICE.**

This file is a research companion / state-gap model, not one of the required three complete archaeology cases.

Why:

- no verified historical capture was inspected;
- no two historical Web timepoints were reconstructed;
- no historical browser/encoding comparison was executed;
- no resource-loss inventory exists for `chinajc.com`;
- transaction backend remains mostly non-public.

This is an acceptable stop condition under `docs/METHOD.md`.

---

# 16. Privacy / ethics boundary

Employment and unemployment systems contain highly sensitive ordinary-person data:

- legal names;
- ID numbers;
- addresses;
- phone numbers;
- employment history;
- household/low-income status;
- social-insurance records;
- application and rejection history.

Even if an old public page or archive exposes such material, this repository should **not bulk republish personal applicant records**.

For research into workflow, prefer:

- schema and field names;
- official help pages;
- anonymized/press-reported cases;
- state diagrams;
- public aggregate counts;
- minimal necessary excerpts.

---

# 17. Overseas comparator: U.S. public employment infrastructure before mass household Web

This belongs mainly in `how-people-lived`, but one technical comparison is useful here.

A U.S. Department of Labor directive issued 1996-11-01 documents America's Job Bank as a mixed public-employment infrastructure:

- Internet job search;
- Internet employer direct entry;
- state employment-security-agency validation;
- Internet FTP exchange of job files;
- mainframe and PC systems;
- digital touch-screen ALEX terminals.

Source:
- https://www.dol.gov/sites/dolgov/files/ETA/advisories/ESPL/1997/ESPL03-97.html

Evidence: **A — contemporary official technical/business directive.**

The important comparison is not “America was earlier.” It is the shared architecture:

> **public employment digitization was multi-interface and backend-heavy before it became a private-home-Web story.**

China's specific state machine around `下岗`, enterprise reemployment centers and `再就业优惠证` remains historically distinct.

---

# 18. Claims ledger

| Claim | Evidence | Grade | Confidence | Boundary |
|---|---|---:|---:|---|
| 1998 reemployment centers could issue living allowances, pay social insurance and provide training | Shenzhen official gazette | A | high | Shenzhen implementation; not every locality identical |
| 2001 Liaoning began closing centers and routing new reductions toward contract termination + unemployment insurance | Liaoning regulation | A | high | provincial pilot/implementation |
| 2003 Guangdong reemployment certificate distinguished categories and used a provincial information system | Guangdong regulation via Shenzhen gazette | A | high | Guangdong |
| `chinajc.com` hosted/was used for the 2003 national online recruitment fair | Xinhua contemporary report | B | high | historical host association; no verified capture |
| 7,209 people reached preliminary employment intentions | Xinhua report | B | high | NOT equivalent to actual starts |
| organizers provided access conditions for unemployed youth to log onto Web | Xinhua report | B | high | access distribution unknown |
| `12333` was designated national public labor/social-security consultation number in 2003 | ministry notice | A | high | phone interface, not Web transaction proof |
| 2015 national graduate recruitment week used four listed public Web platforms | MOE/MOHRSS notice | A | high | host/event association, not exact page reconstruction |
| original 2003 DOM/browser/charset for `chinajc.com` | none | — | unknown | do not reconstruct |

---

# 19. Negative evidence / unresolved questions

1. No verified Wayback/WARC response for `chinajc.com` was inspected this slice.
2. The exact recruitment-hall URL/path is unknown.
3. Account creation and login requirements are unknown.
4. Browser and charset requirements are unknown.
5. The 7,209-intent cohort's actual employment conversion is unknown.
6. The share of access from home PC, Internet cafe, public office or other shared terminal is unknown.
7. Backend protocol/database implementation of the Guangdong reemployment-support system is unknown.
8. Whether different departments queried the same live backend or exchanged batch records is unknown.
9. 2003–2015 local employment portals likely had substantial regional diversity not captured here.
10. Public job-listing persistence should not be mistaken for preservation of unemployment itself.

---

# 20. What this changes in old-Web interpretation

A public-employment website is not merely another page category.

It sits at the boundary between:

```text
browser-visible information
and
authoritative life-course state
```

The old Web may show a person a job, explain a policy or accept an expression of interest. But the historically decisive events — losing an old labor relationship, being recognized as eligible, receiving a paper credential, getting a benefit, being accepted by an employer and actually starting work — frequently happened in **other systems**.

Therefore the central rule for this object is:

> **Never let the surviving page impersonate the surviving life.**

---

## Sources consulted in this slice (accessed 2026-09-07)

### A — original / contemporary institutional evidence

- Shenzhen 1998 reemployment/basic-living-support regulation:
  https://www.sz.gov.cn/zfgb/1998/gb143/content/post_10123116.html
- Shenzhen 1998 reemployment-service-center notice:
  https://www.sz.gov.cn/zfgb/1998/gb145/content/post_10124194.html
- Liaoning 2001 xiagang-to-unemployment-insurance transition:
  https://www.ln.gov.cn/web/zwgkx/zfwj/szfwj/6D69769EF6384624B98CF5E8A65A12F1/index.shtml
- 2001 labor/social-security statistical bulletin:
  https://www.stats.gov.cn/sj/tjgb/qttjgb/qgqttjgb/202302/t20230218_1913248.html
- 2002 labor/social-security statistical bulletin:
  https://www.stats.gov.cn/sj/tjgb/qttjgb/qgqttjgb/202302/t20230218_1913251.html
- Guangdong 2003 reemployment preferential certificate rules:
  https://www.sz.gov.cn/zfgb/2003/gb350/content/post_4976320.html
- Ministry 2003 `12333` notice:
  https://www.mohrss.gov.cn/xxgk2020/fdzdgknr/zhgl/rlzyshbzxxh/202010/t20201031_394105.html
- MOE/MOHRSS 2015 national online recruitment weeks:
  https://www.moe.gov.cn/srcsite/A15/s3265/201503/t20150311_189363.html
- Beijing 2015 mixed public-employment service month:
  https://rsj.beijing.gov.cn/xxgk/2024zcwj/202406/t20240617_3716918.html
- U.S. Department of Labor, America's Job Bank directive, 1996:
  https://www.dol.gov/sites/dolgov/files/ETA/advisories/ESPL/1997/ESPL03-97.html

### B — contemporary secondary / user-operation evidence

- Xinhua, 2003 national online recruitment fair for laid-off/unemployed youth:
  https://news.sina.com.cn/s/2003-01-27/203340616s.shtml

---

*Research note assembled with AI assistance. Claims are deliberately narrower than the narrative implied by some contemporary headlines; archive reconstruction remains pending.*