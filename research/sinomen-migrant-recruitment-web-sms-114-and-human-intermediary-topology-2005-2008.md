# 新农门 2005–2008：Web、短信、114 与人类中介共同组成的招聘平台拓扑

> Status: research checkpoint.
>
> Scope: 约 1995–2015 中文旧网。本文不把农民工生活史整体写入本仓；只研究一个中文 Web 服务如何与电话、短信、培训学校、政府项目和村级联系人共同工作，以及这种多端点服务给 archive interpretation 带来的新 state gaps。
>
> Companion life-history slice: `tmzncty/how-people-lived/sources/contemporaneous-migrant-job-search-hybrid-intermediation-china-2006-2009.zh-CN.md`
>
> M1 historical Web artifact status for `www.sinomen.cn`: **NOT ACHIEVED IN THIS SLICE**.

## 0. Why this checkpoint is not another generic recruitment-state-gap note

The repository already has mature notes on:

- early recruitment listing/resume lifecycle;
- 51job cross-channel registration;
- public-employment backend systems vs public Web access;
- unemployment/reemployment service state gaps.

Those already establish rules such as:

```text
web platform != web-only ingress
backend digitization != citizen Web access
listing visible != application delivered != hire
```

A new generic “农民工网上招聘” note would be duplicate expansion.

This checkpoint adds a narrower historical object with a different topology:

> **a service deliberately designed so that the Web-facing side could be used mainly by employers/institutions while many intended workers were reached through SMS, 114 operators, training schools, government offices and village-level human intermediaries.**

The archaeological problem is therefore not only `ingress channel` but **record provenance + cross-channel service topology**.

---

## 1. Identity and chronology currently supportable

### 1.1 Brand/service launch

A 2006-11-06 contemporaneous report carried by Sohu / 浙江在线—今日早报 states that:

- 杭州新农门信息技术有限公司 was founded in 2005-09;
- the 新农门 website officially launched in 2005-11;
- the reporter visited the site in 2006 and described visible sections and job-search behavior.

Current carrier:
- https://news.sohu.com/20061106/n246217039.shtml

Evidence class: **B — contemporaneous media report.**

Important chronology rule:

```text
brand/service launch date
!=
first verified date for a particular hostname
```

The 2006 article says the site launched in 2005 but does **not** provide a host in the text currently exposed by the crawler.

### 1.2 `www.sinomen.cn` is directly attested by 2007-01-07

A 2007-01-07 杭州日报 report preserved by Sohu explicitly says:

> 在网上登录“新农门网”（www.sinomen.cn）

and then describes the visible sections.

Current carrier:
- https://news.sohu.com/20070107/n247457743.shtml

Evidence class: **B — contemporaneous media report with explicit host.**

Therefore the safe chronology is:

```yaml
service_reported_online: 2005-11
host_www_sinomen_cn_explicitly_attested_by: 2007-01-07
host_used_at_initial_2005_launch: unknown
```

Do **not** silently backfill `www.sinomen.cn` into 2005 merely because later reports associate the brand with that host.

A current third-party company profile also associates the company with `www.sinomen.cn` and records later Internet/call-center business scope, but this is only a present-day secondary carrier and is not promoted to historical Web artifact evidence:
- https://www.job5156.com/comp/472519

---

## 2. What the contemporaneous reports say the Web surface contained

The 2006-11-06 reporter describes the homepage as containing sections including:

- 打工招工;
- 培训;
- 交流;
- 权益;
- 政策;
- 生活服务;
- 活动专区.

The reporter further describes:

- job information for employers in Guangdong, Zhejiang, Shanghai and elsewhere;
- a `职位搜索` function;
- links/paths from insufficient skill to vocational-school training information;
- later recommendation to jobs after training.

Source:
- https://news.sohu.com/20061106/n246217039.shtml

The 2007-01-07 report again lists:

- 打工招工;
- 培训;
- 交流;
- 权益;
- 政策资讯;
- 生活服务;

and reports that job entries could include employer/job description and pay.

Source:
- https://news.sohu.com/20070107/n247457743.shtml

Evidence status:

> **B-grade reported interface behavior, not A-grade interface artifact.**

These descriptions provide concrete fields to look for in a future capture, but cannot establish historical DOM, HTML labels, form actions, exact URL paths, JavaScript, session behavior, charset or browser assumptions.

---

## 3. The service was explicitly not “a website used only through the website”

### 3.1 SMS and telephone were part of the designed service

The 2006 report explicitly says that people who could not or did not have time to use the Web could get information by telephone or SMS.

The 2007 report repeats this and describes a “打工卡” plus telephone service.

Sources:
- https://news.sohu.com/20061106/n246217039.shtml
- https://news.sohu.com/20070107/n247457743.shtml

### 3.2 114 became a human-operated endpoint

A 2006-12-14 杭州日报 report preserved by Sina describes a collaboration with China Telecom:

- caller dials `114`;
- states that the request is job seeking or recruiting;
- is transferred to the relevant hotline;
- staff match supply/demand and later return information.

Source:
- https://finance.sina.com.cn/roll/20061214/05551098410.shtml

This supports:

```text
service endpoint = telephone operator
```

not merely:

```text
telephone points user to website
```

The operator is an active transaction/intermediation node.

---

## 4. 2007 evidence: the Web audience and the service audience were intentionally different

The strongest topology evidence is a 2007-07-04 新京报 report preserved by Sina.

It states that 新农门 did not primarily expect valuable site traffic to come from migrant workers. Instead, employers were an important Web-facing user group.

The report describes worker records entering the broader system through several institutional channels:

- vocational training schools sending graduate records;
- local `阳光工程办公室` contributing registered labour records;
- SMS links to more than ten thousand natural-village heads;
- village heads becoming local recruiting intermediaries when employers needed workers.

Source:
- https://tech.sina.com.cn/i/2007-07-04/03501596638.shtml

Evidence class: **B — contemporaneous business-model reporting.**

Platform scale figures in the article are attributed claims and must not be treated as audited coverage.

This topology can be represented as:

```text
[employer Web endpoint]
          |
          v
[platform/database]
   |      |       |        |
   v      v       v        v
school  gov office  SMS  114/operator
   |      |       |        |
   +------+-------+--------+
                  |
                  v
               worker
```

The diagram is a research abstraction, not a claim that all flows used one literal technical backend.

What is historically important is that the contemporaneous service description itself treats the platform as **multi-channel and human-mediated**.

---

## 5. New state gaps: record provenance must be separate from display surface

The earlier 51job checkpoint already established:

```text
web platform != web-only ingress
```

新农门 requires a stronger provenance model because a worker record may be supplied by an institution or intermediary while being searchable on a Web-facing system used by an employer.

### State gap A — `web-visible record / worker-authored record`

```text
worker record visible in Web/database system
!=
worker personally created Web account
!=
worker typed the record
!=
worker personally browsed the record
```

### State gap B — `worker known to platform / worker is Web user`

```text
platform possesses worker information
!=
worker has Internet access
!=
worker can independently operate site
```

### State gap C — `digital match / digital interaction by both parties`

```text
match produced by digital database
!=
worker used digital endpoint
```

An employer may search online while the worker receives the result through a village intermediary, telephone call or SMS.

### State gap D — `record presence / provenance known`

If a future historical capture reveals a worker profile, we still need to know whether its origin was:

```yaml
record_provenance:
  self_web_form: confirmed/probable/unknown
  school_submission: confirmed/probable/unknown
  public_program_submission: confirmed/probable/unknown
  village_intermediary: confirmed/probable/unknown
  phone_operator: confirmed/probable/unknown
  sms: confirmed/probable/unknown
  imported_batch: confirmed/probable/unknown
```

A screenshot cannot answer these fields by itself.

---

## 6. New archaeological rule: a verified homepage would still not verify the platform

This case adds a preservation problem distinct from prior `index-shell survival`, `live-origin body survival`, or `syndication persistence`.

Working term:

> **cross-channel service decomposition / 跨渠道服务分解**

Even a perfect 2007 homepage capture could recover only one surface of the lived service.

Potentially missing objects include:

- telephone IVR/transfer rules;
- operator scripts;
- internal matching console;
- SMS command syntax and outbound templates;
- `打工卡` physical fields and identifier semantics;
- school batch-submission format;
- government-office submission workflow;
- village-head SMS workflow;
- call-back timing;
- data synchronization between channels.

Therefore:

```text
verified historical homepage capture
!=
verified historical service topology
```

and:

```text
Web archive completeness
!=
service-history completeness
```

This matters for old-Web archaeology because a platform can be historically important precisely through the users who **did not operate its Web UI**.

---

## 7. “Direct Web user” did exist — but is not the only user state

A Google Groups post dated 2006-10-22 preserves a contemporaneous media text attributed to 第一财经日报 and points to an old ChinaUnix thread. It quotes a 24-year-old Anhui migrant worker, 王新胜, described as someone who regularly used the Internet and who positively evaluated 新农门's recruitment/training/rights content.

Current derivative carrier:
- https://groups.google.com/g/jusocn/c/_xob-bzL_js

Evidence class: **B/C boundary — derivative survival of contemporaneous media text.**

This supports the existence of:

```text
worker -> Web -> site
```

but cannot be generalized to the whole intended audience.

The same text explicitly says that Internet-using migrant workers were still a minority and identifies the service's “最后一公里” as a problem to be addressed through Web + local offices + SMS + 114.

Thus the historically accurate state model needs at least:

```text
direct Web worker
human-mediated worker
SMS/phone worker
institutionally imported worker record
employer Web user
```

rather than a single binary `online/offline` field.

---

## 8. Adoption evidence: online job search appears but does not replace social recruitment

A 2008-01-16 contemporaneous report summarizing the `2007中国农民工（蓝领）报告` states that in its sample:

- 朋友介绍: 41.9%;
- 老乡介绍: 32%;
- 上网找工作: 7.9% in 2006 -> 9.9% in 2007.

Source:
- https://business.sohu.com/20080116/n254693642.shtml

Evidence class: **B — contemporaneous report of a platform-associated survey.**

The sample is not treated as a nationally representative probability sample because the current report does not expose a sufficiently complete sampling/weighting contract.

Archaeological implication:

> a new Web route can coexist with much larger offline/social routes for years.

Therefore a site's apparent sophistication must not be used to infer population-level adoption.

---

## 9. Host chronology: do not fuse brand history and hostname history

Current evidence supports:

- service/company origin around 2005;
- site reported online 2005-11;
- `www.sinomen.cn` explicitly attested in a period newspaper report by 2007-01-07.

What remains unknown:

- whether `www.sinomen.cn` was the initial 2005 host;
- whether another domain/subdomain preceded it;
- whether the hostname redirected among multiple hosts;
- exact historical IPs;
- whether `sinomen.cn` and `www.sinomen.cn` served identical content;
- when any later repurposing or shutdown occurred.

Rule:

```text
brand launch
!= hostname launch
!= first archive capture
!= first period citation of hostname
```

This distinction is especially important when later secondary pages compress all dates into a single company history.

---

## 10. Historical capture attempt status

This research slice searched for a directly usable Wayback/archival path for `www.sinomen.cn` and attempted direct archive discovery.

In the current research environment no inspectable historical document was returned that satisfied the repository's minimum capture contract.

Record:

```yaml
object: 新农门 Web surface
known_host: www.sinomen.cn
period_target: 2006-2008
historical_capture_opened: false
m1_status: NOT ACHIEVED
```

This means only:

> this slice did not open and verify a historical capture.

It **does not** mean:

> Internet Archive never stored the site.

Still unknown:

- capture datetime;
- replay/original URL relationship;
- HTTP status / redirect chain;
- Content-Type;
- charset;
- DOM;
- frame use;
- JavaScript;
- cookies/session;
- browser requirements;
- forms/actions;
- job-detail URL structure;
- forum path;
- subresource survival;
- second verified historical time point.

No IE6 / ActiveX / GB2312 stereotype is filled in without artifact evidence.

---

## 11. Privacy boundary

A future capture may contain worker profiles, telephone numbers, village-level identities, school records or other personal data.

Repository rule for this object should be stricter than “publicly archived = safe to republish”.

Do not bulk republish:

- personal names tied to phone numbers;
- ID-like identifiers;
- detailed worker dossiers;
- private contact information;
- sensitive migration/family data.

For interface archaeology, field names, redacted examples and aggregate state transitions are normally enough.

---

## 12. Confirmed / probable / unknown

### Confirmed from contemporaneous reports

- 新农门 was reported online by late 2005.
- By 2006 reporters described a Web surface with recruitment/training/rights/policy/life-service sections.
- Telephone and SMS were explicitly offered for people unable/unwilling to use the Web.
- By 2006-12 a 114-to-human-operator job-matching route was reported.
- By 2007-01 `www.sinomen.cn` was explicitly published as the service host.
- By 2007-07 a period report described employer-side database use plus records sourced via schools, public training offices and village-level SMS contacts.
- At least one contemporaneous worker interview describes direct Web use.

### Strongly suggested but not artifact-verified

- the service likely relied on a shared or coordinated information backend across several channels;
- employer-facing digital search and worker-facing human/telecom relay were intentionally complementary;
- the Web UI represented only part of the historically operative platform.

### Unknown

- initial 2005 hostname;
- exact technical architecture tying Web/SMS/114/operator/database together;
- worker consent/edit semantics for institutionally sourced records;
- historical UI/DOM/charset/browser stack;
- data refresh/expiry rules;
- duplicate-record handling;
- whether worker records carried provenance fields internally;
- exact shutdown/transition date;
- verified historical capture timeline.

---

## 13. What this changes in old-Web method

This case adds two reusable rules.

### Rule A — archive the service topology, not only the site

For a multi-channel platform, record:

```yaml
service_endpoints:
  web:
  sms:
  telephone:
  call_center:
  physical_card:
  institutional_office:
  local_human_intermediary:
```

A homepage is not the whole service.

### Rule B — preserve record provenance separately from record display

For a profile/listing/database object, ask:

```text
Who created this record?
Who could edit it?
Who could see it?
Through which channel did it enter?
Through which channel did the affected person receive its result?
```

Without this, Web archaeology can accidentally transform:

> “an employer saw a worker record on the Web”

into the much stronger and potentially false claim:

> “the worker used the Web to create and manage that record.”

---

## 14. Why this matters beyond recruitment

The same pattern may apply to:

- ticketing systems with station clerks using networked inventory;
- banking where branch staff use online backends for non-Internet customers;
- social security with digital records but paper/desk interfaces;
- hospital registration mediated by staff;
- logistics systems where senders use counters and staff use networked software;
- early e-government where a public Web page is only one of several transaction endpoints.

Therefore a central old-Web question should sometimes be:

> **Who actually touched the browser?**

A person can live inside a digitally coordinated institution without personally becoming a Web user.
