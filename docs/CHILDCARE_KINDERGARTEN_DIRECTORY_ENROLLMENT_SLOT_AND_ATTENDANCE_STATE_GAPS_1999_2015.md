# 中文旧网托幼目录、幼儿园报名、名额分配与实际入园状态缺口（1999–2015）

## 0. Scope

本说明只处理约 1999–2015 中文 Web 里与托幼/幼儿园有关的以下对象：

- 学前教育信息门户；
- 幼儿园目录与园所主页；
- 招生简章；
- 家长信息采集；
- 网上报名；
- 网上报名顺序；
- 电脑派位/摇号结果；
- 网上状态查询；
- 线上登记与线下材料核验之间的状态转换。

它**不是**一篇中国托育史，也不把仓库 scope 扩展到 1995 年以前或全球托育史。更长时段的生活史、前互联网托儿组织、海外比较与 2016 年以后变化写在：

- `tmzncty/how-people-lived/topics/childcare-slots-care-time-compatibility-and-parental-work-executability-china-1952-2026.zh-CN.md`

它也不重复：

- `docs/LIFE_STAGE_ROUTING_LURKER_VISIBILITY_AND_PARENTING_COMMUNITY_ARTIFACTS_1999_2003.md`：后者研究育儿社区、同阶段路由、潜水者与社区 artifact；
- domestic-service 相关说明：后者研究家政/保姆 profile、matching、预约与入户服务；
- higher-education / school application 相关研究：本说明只关心托幼/幼儿园服务。

核心问题是：

> **旧网页能证明一个幼儿园、报名系统或录取结果“存在”到什么程度？从页面存在到一个孩子真正每天进入园所，中间有哪些不能跨越的状态？**

---

## 1. Minimum state model

托幼 Web artifact 至少要拆成下面这条链：

```text
real institution exists
→ institution is legally/operationally active
→ public directory entry / homepage exists
→ institution is accepting this age/cohort
→ household is within eligibility rules
→ application window is open
→ parent discovers the page
→ client/browser can load the page
→ account / child record can be created
→ form fields are completed
→ submit request is sent
→ server acknowledges request
→ application record is committed
→ eligibility/material review
→ applicant enters allocation pool
→ order / lottery / discretionary allocation
→ result is produced
→ result is published / delivered
→ parent notices result
→ parent accepts / completes offline verification
→ fees / health / document requirements are completed
→ child is formally enrolled
→ child actually attends
→ attendance continues over time
```

任何历史叙述都不能无证据地跨越这些节点。

因此必须固定以下硬规则：

```text
kindergarten homepage exists
≠ institution has an available place

institution is listed
≠ institution is recruiting now

online information collection
≠ application

application submitted
≠ database committed

application stored
≠ eligible

eligible
≠ admitted

admitted
≠ accepted by family

accepted
≠ documents verified

enrolled
≠ actually attended

attendance on one date
≠ stable care arrangement
```

---

## 2. Why this object matters to old-Web archaeology

幼儿园报名页和普通内容页不一样。

普通新闻或个人主页主要面临：HTML、图片、链接、字符集和动态资源能否保存。

托幼报名系统还额外依赖：

- 特定日期/时刻是否开放；
- 年龄和出生日期规则；
- 户籍/居住地/单位等资格；
- 登录、账号、家长与儿童关联；
- 私人身份字段；
- 服务端写入；
- 审核队列；
- 名额上限；
- 随机派位或报名时序；
- 线下原件核验；
- 私人录取结果。

所以一张 archive screenshot 最多能证明某个前台状态，不能自动恢复整个招生过程。

---

## 3. 1999–2002: information Web before allocation Web

上海学前教育网自己在 2005 年保存的建设史称：

- 1998 年成立上海学前教育信息部；
- 1999 年推出第一版上海学前教育网，域名 `www.xq.shec.edu.cn`，起初仅教育系统内部访问；
- 2000 年面向幼儿家长和公众推出社会化入口；
- 2002 年向幼儿园和家长推出会员制“园园通管理平台”。

Source:

- Shanghai Preschool Education Network, 2005-12-27:  
  <https://age06.edu.sh.cn/age06web/home/content/2005/7376821742871777280.html>
- Current institutional “About Us”:  
  <https://age06.edu.sh.cn/age06web/government/AboutUs.html>

Evidence class: **A/B-near-primary institutional self-history**.

### What this proves

可以安全写：

- 1999–2002 上海学前教育领域已经存在制度性 Web 信息平台；
- 服务对象从内部系统扩到公众/家长；
- 后续出现面向园所与家庭的管理平台。

不能写：

- 1999 年普通上海家庭已经普遍靠 Web 找幼儿园；
- 2000 年网站已经具有今天意义上的统一网上报名；
- “园园通”在 2002 年已经等于今天的一网通办入园系统；
- 当前站点 URL、DOM、页面风格、charset 或数据库结构与 1999/2002 相同。

### New gap: information-state / allocation-state gap

这是本说明的第一条核心缺口：

```text
service information becomes web-visible
≠
scarce care slots become web-allocatable
```

中文学前教育 Web 可以先传播政策、园所信息和育儿知识很多年，然后才逐步介入真实报名与分配。

---

## 4. Directory state is not institution state

旧网中一个幼儿园条目可能来自：

- 教育行政部门目录；
- 学前教育门户；
- 园所自己的主页；
- 搜索引擎；
- 家长社区整理；
- 商业黄页；
- 新闻稿或招生简章。

因此必须记录：

```text
institution_name_at_capture
operator/organizer_if_known
physical_address_at_capture
telephone_at_capture
source_type
directory_or_homepage
capture_datetime
page_last_updated_if_visible
recruiting_status_if_explicit
```

并固定：

> **directory entry survival ≠ institutional continuity**

机构可能改名、迁址、停办、转制，而目录仍在；反过来，机构继续存在，旧主页也可能已经死亡。

---

## 5. 2015: online registration becomes allocation-adjacent

2015 年太原同期报道已经给出非常清晰的招生链：

```text
幼儿园公布招生简章
→ 家长网上报名
→ 幼儿园审核材料
→ 公示录取名单
→ 办理入园手续
```

报道还写到，部分幼儿园按规定时间内的 **网上报名次序** 确定最终名单。

Source:

- 山西新闻网 2015-05-21，《今年，各大幼儿园招生多要求网上报名》：  
  <https://news.sina.com.cn/o/2015-05-21/021731857260.shtml>

Evidence class: **A/B-near-primary contemporaneous report**.

### New gap: client time / server order gap

一旦名额与提交顺序有关，“先到”不再只是身体排队顺序。

需要区分：

```text
user opened page at T1
user clicked submit at T2
request left client at T3
server received request at T4
validation completed at T5
record committed at T6
allocation order key = ?
```

如果历史系统没有公开排序字段，就不能从“家长说自己很早提交”推定数据库中的真实次序。

### New gap: submit / acknowledge / commit

历史页面出现：

```text
报名成功
```

最多只能证明某一前台 success state，除非有额外证据，否则不能自动推出：

- 数据库 transaction 已持久化；
- 后台审核队列已生成；
- 家长不会因重复提交/系统错误而丢失记录；
- 该记录最终进入名额分配池。

---

## 6. 2015: physical queues and Web enrollment coexist

北京 2015 年一所幼儿园公布 100 个名额后，部分家长提前五天到门口排队；正式报名时，排在 100 名后的部分家庭没有报上。

Sources:

- 北京青年报 / 人民网 2015-05-21：  
  <https://edu.people.com.cn/n/2015/0521/c1053-27036062.html>
- 北京晨报 / 人民网 follow-up 2015-05-24：  
  <https://politics.people.com.cn/n/2015/0524/c1001-27047164.html>

这证明不能写一个简单阶段论：

```text
1990s physical queue
→ 2010s online registration
```

更准确的是：

```text
physical queue
+ phone consultation
+ website notice
+ online information collection
+ online application
+ offline verification
+ lottery / discretionary allocation
```

不同城市、园所和年份长期共存。

### Hybrid-channel state gap

同一招生流程里，“网页”可能只承担其中一步：

- Web 发布规则；
- 线下报名；
- Web 采集信息；
- 线下交原件；
- Web 查询结果；
- 电话通知；
- 门口张榜。

所以 archive 不能因为捕获了一个 Web 页面，就把全过程写成“网上招生”。

---

## 7. Computer lottery: transparent allocation artifact, scarce capacity unchanged

2015 年广州教育部门办幼儿园的电脑派位提供了另一个状态模型。同期报道记载，159 个园区拿出 85% 学位参与派位，共 26,851 人报名；不同园区竞争度差异极大，最热门园区报名/录取比超过 60:1。

Source:

- 南方日报 / China Daily, 2015-04-24:  
  <https://cnews.chinadaily.com.cn/2015-04/24/content_20529414.htm>

### Lottery pipeline

至少需要拆成：

```text
published capacity
→ eligible applications
→ final lottery input set
→ randomization / allocation process
→ provisional result
→ public result
→ qualification verification
→ final enrollment
```

因此：

```text
lottery system exists
≠ every application entered the lottery

name appears in provisional result
≠ final enrollment

computer allocation
≠ more slots
```

### New gap: allocation transparency / capacity scarcity

数字派位可以改变名额如何分，而不改变名额总量。

旧网研究特别容易因为系统页面、名单、流程图保存得比家庭失败经历更好，而错误形成“制度已经数字化，所以问题已解决”的视觉印象。

---

## 8. Online information collection is not the same as admission

2015 年北京已经出现区县级幼儿信息采集入口整理；同期页面列出朝阳、西城、顺义、海淀等不同系统，并说明部分系统只在规定日期开放。

Source:

- 中国教育在线转载整理 / 幼教网 2015-04-16：  
  <https://www.youjiao.com/e/20150416/552f13aac1619.shtml>

Evidence class: **B/C locator-level secondary page**. It is useful for identifying likely historical system URLs and workflow clues, but not enough to declare those URLs as verified historical captures or reconstruct backend behavior.

2015 年青岛李沧区公开招生信息则明确呈现“网上报名，现场确认”的混合流程。

Source:

- 青岛日报官网 2015-06-02：  
  <https://www.dailyqd.com/2015-06/02/content_251317.htm>

### Information collection / application gap

必须区分：

```text
child record exists in district information system
≠ parent applied to a specific kindergarten
```

### Online registration / offline verification gap

还必须区分：

```text
online form accepted
≠ original documents verified
```

这类系统通常会收集高度私人的未成年人信息。公开 archive 没有保存个人记录，很多时候是正常的 privacy boundary，不应被误写成 archive failure。

---

## 9. Eligibility is a separate state machine

幼儿园报名可能涉及：

- 出生日期/年龄；
- 户籍；
- 实际居住地；
- 小区/片区；
- 父母单位关系；
- 特定机构教职工子女资格；
- 证件材料；
- 健康和其他入园要求。

因此一个系统即使“正常运行”，某个家庭仍可能因为资格状态无法进入下一步。

状态至少要分：

```text
rule published
→ household thinks eligible
→ system accepts entered data
→ institution reviews evidence
→ institution confirms eligible
```

### Eligibility text / adjudicated eligibility gap

网页写“符合 X 条件可报名”只能证明规则文本；不能证明一个具体家庭的边界案例最终怎样被裁定。

---

## 10. Browser and client environment can affect access to a scarce window

如果历史系统只在短时间窗口开放，并且报名顺序与录取有关，那么 browser compatibility 就不再是纯展示问题，而可能成为 allocation access 的一部分。

对任何 verified capture，应记录：

```text
browser requirements if stated
JavaScript requirement
ActiveX / plugin if any
cookie/session requirement
encoding
form method/action
opening / closing datetime
client-side validation
server-side validation evidence
```

但本轮**没有**获得足够原始证据证明 1999–2015 某个具体核心幼儿园报名系统必须依赖 ActiveX、特定 IE 版本或某一 CGI/ASP endpoint。因此这些项不能按“那个年代大概如此”补写。

后来的招生页面出现浏览器建议，只能作为后续演化线索，不能倒填到 2010 或 2005。

---

## 11. Public shell / private child-state asymmetry

托幼报名系统有非常强的公共/私人不对称：

### Public artifacts more likely to survive

- 招生简章；
- 首页；
- 报名入口；
- 用户说明；
- 截止时间；
- 公开录取名单（若当年确实公开）；
- 新闻截图；
- 政策公告。

### Private states less likely — and often should not — survive publicly

- 家长姓名；
- 儿童姓名；
- 出生日期；
- 身份证/户籍字段；
- 家庭住址；
- 电话；
- 登录 session；
- 志愿列表；
- 审核备注；
- 健康信息；
- 个体后台录取状态。

### Privacy stop condition

不得为了复原旧系统：

- 测试历史泄露的儿童身份数据；
- 尝试登录真实旧账号；
- 使用现役政府系统枚举未成年人信息；
- 将泄露数据库当作“珍贵历史档案”纳入仓库。

历史可见性不足在这里有一部分恰恰是正确隐私保护的结果。

---

## 12. Admission is not attendance

即使获得正式录取结果，仍然存在：

```text
offer issued
→ family receives/notices it
→ accepts
→ verifies documents
→ pays required fees if any
→ child completes health/admission requirements
→ first day attends
→ remains enrolled
```

历史 Web 很少能告诉我们：

- 家庭是否最终放弃；
- 是否转去另一所园；
- 孩子是否因健康、搬家或家庭安排未入园；
- 实际每天几点入园离园；
- 祖辈是否仍承担接送；
- 一次停课是否迫使父母请假。

因此新增：

**admission / attendance gap** 与 **Web enrollment / lived-care gap**。

---

## 13. A complete childcare enrollment artifact should record

当未来找到一个真正可验证的 1999–2015 中文托幼报名 capture 时，至少记录：

```yaml
artifact:
  service_or_institution:
  original_url:
  archive_url:
  capture_datetime:
  page_role: directory|notice|info_collection|application|result|help
  source_type:
  evidence_class:

rendering:
  declared_charset:
  observed_charset:
  frames:
  javascript:
  css:
  images:
  missing_subresources:

form:
  form_method:
  form_action:
  visible_fields:
  required_fields:
  child_age_fields:
  parent_fields:
  residence_or_hukou_fields:
  kindergarten_choice_fields:
  validation_messages:
  submit_button_text:

state:
  opening_datetime:
  closing_datetime:
  account_required:
  login_required:
  acknowledgment_state:
  offline_verification_required:
  result_channel:

allocation:
  capacity_if_explicit:
  first_come_if_explicit:
  lottery_if_explicit:
  priority_rules_if_explicit:
  ordering_key_known: false

unknowns:
  - server transaction semantics
  - database schema
  - queue ordering implementation
  - exact applicant pool
  - private review state
  - final attendance
```

---

## 14. Evidence table for this note

| Evidence | Date | What it supports | Grade | What it does NOT support |
|---|---:|---|---|---|
| Shanghai Preschool Education Network self-history | 2005, describing 1999/2000/2002 | institutional Web timeline and audience expansion | A/B-near-primary | original 1999 DOM/capture, public usage rate |
| Taiyuan kindergarten online-registration report | 2015 | application → review → admission flow; some order-based admission | A/B-near-primary | server timestamp semantics, fairness |
| Beijing five-day physical queue | 2015 | physical first-come scarcity coexisting with Web era | A/B-near-primary | citywide prevalence |
| Guangzhou computer lottery | 2015 | digital allocation of scarce public slots | A/B-near-primary | every applicant’s eligibility/final attendance |
| Beijing district system URL compilation | 2015 | locator for fragmented district information systems | B/C | verified archive capture or backend implementation |
| Qingdao online registration + onsite confirmation | 2015 | hybrid Web/offline flow | A/B-near-primary | actual private child records |

---

## 15. Negative result: still no M1-grade verified enrollment capture

This research round searched for early Shanghai preschool portals and 2010s kindergarten enrollment systems, but did **not** obtain and inspect a verified Wayback/WARC memento sufficient to satisfy the repository’s M1 artifact contract for an actual 1999–2015 childcare enrollment transaction.

Therefore the following remain **unknown unless a later capture supplies evidence**:

- original DOM of the 1999 Shanghai preschool site;
- original charset and subresource graph for its earliest public version;
- exact 2002 `园园通` parent login/session behavior;
- exact historical form actions and endpoints for 2015 district enrollment systems;
- queue data structures;
- whether “提交成功” corresponded to durable DB commit;
- server/client timestamp arbitration;
- private applicant review state;
- allocation implementation beyond publicly described rules.

A modern surviving page that says “1999 年上线” is **history evidence**, not an archived 1999 page.

A search result exposing an old URL is a **locator**, not a verified capture.

A newspaper screenshot is **interface evidence**, not a WARC.

Do not check off ROADMAP M1 on the basis of this note.

---

## 16. New state gaps added by this object

This case adds or sharpens the following gaps:

1. **information-state / allocation-state gap** — institution can be Web-visible before slots are Web-allocatable;
2. **directory-entry / operational-institution gap**;
3. **homepage / recruitment-open gap**;
4. **age-rule / actual-eligibility gap**;
5. **information-collection / application gap**;
6. **client-time / server-order gap**;
7. **submit / acknowledge / durable-commit gap**;
8. **application / allocation-pool gap**;
9. **online-order / fair-order gap**;
10. **lottery-input / published-result gap**;
11. **published-result / final-enrollment gap**;
12. **online-registration / offline-verification gap**;
13. **public-shell / private-child-state asymmetry**;
14. **admission / attendance gap**;
15. **Web-enrollment / lived-care gap**;
16. **historical-self-description / verified-capture gap**.

---

## 17. Why this matters beyond kindergarten history

This object changes how old-Web archaeology should treat any Web interface that allocates a scarce real-world service.

A page can be fully preserved while the historically decisive state is gone:

- who reached the page before closing time;
- whose POST arrived first;
- whose record survived validation;
- who entered the lottery pool;
- who was rejected after offline document review;
- who finally used the service.

For ordinary-life history, the decisive question is rarely only:

> “What did the old website look like?”

It is also:

> **“At what exact point did this page stop being information and begin participating in the distribution of a scarce piece of real life?”**
