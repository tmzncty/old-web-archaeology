# Part-time job posts, BBS mediation, and offline execution gaps, 2006–2009

## Scope

本笔记只处理约 2006–2009 中文旧网中的一个窄问题：**校园 BBS / 网站 / 任务平台怎样参与兼职和短工的发现、联系、信任、执行与纠纷传播，以及 Web archive 为什么特别容易只留下工作链的一小截。**

它不是“大学生兼职史”，也不把本仓 scope 扩成劳动史。1980s 的业余兼职制度、2010s 以后移动平台、副业与当代职业时间感主要属于 `how-people-lived`；本文件只把与 1995–2015 中文旧网直接相关的平台 artifact 和证据边界写清楚。

交叉链接：

- `tmzncty/how-people-lived/topics/secondary-work-gig-routes-and-enacted-job-portfolios-china-1982-2026.zh-CN.md`
- `docs/JOB_BOARD_ADDRESSABILITY_RESUME_DATABASE_GAPS_AND_APPLICATION_ATTENTION_1999_2009.md`
- `docs/ROOMMATE_CLASSIFIEDS_LISTING_LIFECYCLE_AND_HOUSEHOLD_OUTCOME_GAPS_2003_2011.md`

本文件新增的不是 full-time job board 的 resume database 模型，而是 **short-gig execution chain**：许多兼职信息从 BBS 开始，却在电话、办公室、纸面合同、铁路、临时住宿和现金/转账中完成；档案保存的不完整性因此与普通招聘网站不同。

---

## 1. Core distinction: online discovery ≠ online execution

旧网材料里“网上兼职”至少有两种不同拓扑：

### A. Online-discovered, offline-executed

```text
BBS / web listing
→ phone / QQ / email contact
→ offline interview
→ contract / verbal agreement
→ travel
→ physical work
→ cash / transfer / dispute
```

例如：家教、促销、讲课、展会、派单、校园代理。

### B. Online-discovered, online-executed

```text
BBS / task marketplace
→ contact / bid
→ digital task
→ upload / electronic delivery
→ online reputation / payment
```

例如：程序、网站、设计、文案、论坛管理、网络记者、部分游戏劳动。

研究时必须记录：

```yaml
discovery_medium: bbs | website | task-marketplace | portal | other
contact_channel: phone | sms | qq | email | web-form | unknown
interview_mode: offline | online | none | unknown
contract_mode: paper | digital | verbal | unknown
execution_location: employer-site | client-home | remote | cross-city | mixed | unknown
delivery_channel: physical | web | email | ftp | qq | unknown
payment_channel: cash | bank | platform | unknown
```

硬边界：

> `online discovery ≠ online labor`
>
> `web listing ≠ web transaction`

---

## 2. 2006 cross-city tutoring case: an unusually complete execution chain

### 2.1 What survives

2006-08-24，《华夏时报》刊发一篇调查报道，新浪至今保留全文。报道追踪了当年 7–8 月间几名北京高校学生赴湖北黄石做暑期讲课兼职的过程，并明确说明最初机会来自清华“水木社区”中的招聘帖。

当前可核的存续页面：

- 新浪转载《华夏时报》，2006-08-24，《清华北大高考状元暑假打工被骗夜宿街头》：
  <https://news.sina.com.cn/s/2006-08-24/00589829746s.shtml>

证据等级：**B（近同时代新闻调查）**。

重要说明：本文目前没有取得原始水木招聘帖、最初投诉帖或北大未名长帖的可验证 archive capture。因此不能因为 2006 新闻逐字描述了帖子，就把今天的新浪页面标成 A 级 BBS 原件。

### 2.2 Reported chain

报道所重建的链条大致为：

```text
mid-Jul 2006
SMTH recruitment post
→ next-day Beijing office interview
→ Jul 17 phone call / paper contract
→ Jul 20 Beijing West → Wuchang train
→ pickup / Huangshi accommodation
→ lectures / planned classes
→ employer proposes lower pay
→ negotiation
→ dismissal / loss of accommodation
→ self-funded return
→ Aug 9 SMTH complaint post
→ complaint removed after hours
→ blank replacement post with “misunderstanding” title
→ ~23:00 long PKU Weiming BBS complaint
→ repost back to SMTH
→ Aug 16+ reporter interviews
→ Aug 24 press reconstruction
```

这条链对旧网考古的价值在于：**只有最前端的发现和后端的纠纷传播属于公开网络；真正的劳动关系主体大部分发生在网外。**

### 2.3 Listing → embodied commitment

报道记载，招聘帖给出的工作条件包括赴黄石讲课、每天约 5 小时、每日约 200 元；当事人随后到北京办公室面试。签约时，广告中的 5 小时在合同里变为 8 小时，当事人提出疑问但仍签约，并得到火车票。

这里至少要分开三个 state：

```text
advertised_state
contracted_state
performed_state
```

硬规则：

> `advertised hours ≠ contracted hours`
>
> `contracted hours ≠ performed hours`
>
> `advertised pay ≠ paid amount`

如果 archive 只保存招聘帖，只能证明 `advertised_state`。

---

## 3. Platform-affiliation trust is not verification

2006 报道中的当事人显然把高校社区、校友身份、教育机构名称等作为信任判断的一部分。这种现象可称为：

**platform-affiliation trust export**

即：一个工作机会出现在熟悉/高声誉社区中，或招聘者声称拥有某学校/校友身份时，平台与机构的声誉会被心理上带入下一阶段交易。

但考古记录必须保持以下边界：

```text
posted_on_university_bbs != endorsed_by_university
claims_alumni_identity != verified_employer_identity
recognized_school_name != verified_contract_performance
bbs_account_exists != real-world legal identity proven
```

若以后能恢复原始帖子，应单独记录：

```yaml
board:
poster_handle:
poster_affiliation_claim:
platform_verified_affiliation: yes | no | unknown
employer_name_claim:
external_legal_entity_match: yes | no | unknown
contact_info_present:
university_endorsement_evidence: none | present | unknown
```

尤其不要在仓库里把普通学生账号和今天的现实身份做不必要的重新绑定。

---

## 4. Complaint-state mutation: post → deletion/replacement → repost → press

2006 报道保存了一个很少见的内容生命周期：

1. 8 月 9 日中午，SMTH 出现题为《我在黄石带班的痛苦经历》的帖子；
2. 几小时后该帖撤下；
3. 被题为《我在黄石完全是一场误会》的新帖取代，但报道说该帖没有正文；
4. 当晚约 23 时，北大未名 BBS 出现约 4000 多字的《黄石带班遇险受骗记》；
5. 后一帖很快被转载回水木；
6. 随后记者采访不同发帖者/当事人，形成新闻重建。

这可建模为 **complaint-state mutation（投诉内容状态变异）**：

```text
original complaint
→ unavailable / removed
→ replacement shell
→ alternate-platform long post
→ cross-post
→ media reconstruction
```

但必须避免两个常见误判。

### 4.1 deletion ≠ recantation

原帖被撤、随后出现“误会”标题，**不能单凭页面变化推断原作者主动撤回指控、遭到施压或事实已经反转**。原因未知就必须写 unknown。

```text
post_removed != claim_retracted
replacement_title != verified_resolution
```

### 4.2 many surviving copies ≠ many independent witnesses

一个 BBS 帖被另一个站转载，再被门户和新闻网站转载，可以形成很多 URL，却可能只来自同一信息链。

```text
10 repost URLs != 10 independent sources
```

建议每条材料增加：

```yaml
content_origin_id:
source_role: original | crosspost | quote | press-reconstruction | later-retrospective
copy_relationship:
independent_observation: true | false | unknown
```

这和普通“引用幸存”不同：这里同时发生了**原内容消失 + 替代版本出现 + 跨平台迁移 + 新闻二次调查**。

---

## 5. Repost rescue is evidence survival, not original preservation

这组材料提醒：一个被删除的旧网事件，有时不是完全消失，而是以较低等级的证据在别处存活。

可以把存续层写为：

| 层 | 能证明什么 | 不能证明什么 |
|---|---|---|
| 原始 BBS capture（若取得） | 某时点服务器返回的帖子、标题、作者句柄、版面等 | 现实事件必然真实 |
| 同期 cross-post capture | 某内容被另一账号/平台重新发布 | 原帖全文完全一致；转载者独立见证 |
| 同期新闻引用/描述 | 记者当时看到或获得了相关内容；可与采访/合同交叉 | 原始 HTML、完整 thread、未删回复 |
| 后来回忆 | 事件如何被记忆 | 当时页面细节 |

所以：

> `press reconstruction of BBS ≠ preserved BBS`
>
> `deleted original ≠ event absent`

两句话必须同时成立。

---

## 6. The off-platform execution gap

2006 案例中，最关键的人生后果几乎都不天然属于 Web archive：

- 北京办公室面试；
- 纸面合同；
- 火车票；
- 火车和接站；
- 黄石私人住宿；
- 真实课时；
- 招生量；
- 工资协商；
- 半夜被要求离开住处；
- 自费返程；
- 电话、短信与当面对话。

这构成 **off-platform execution gap（平台外执行缺口）**。

对于这类兼职，推荐状态机：

```text
listing_visible
→ contact_attempted
→ interview_completed
→ offer_received
→ contract_signed
→ worker_travelled
→ worker_arrived
→ work_started
→ conditions_changed?
→ work_completed | quit | dismissed | failed_to_start
→ paid_full | paid_partial | unpaid | disputed
→ complaint_posted?
```

Web archive 通常只能可靠看见其中的少数状态。

因此：

> `listing survived ≠ worker existed`
>
> `worker interviewed ≠ job started`
>
> `job started ≠ job completed`
>
> `job completed ≠ paid as promised`
>
> `complaint survived ≠ dispute outcome survived`

---

## 7. 2009: the web can also become the workplace

2009-04-14《江西日报》同期报道（新浪存续页）记录了校园网络记者、论坛管理员、BBS 跳蚤市场、威客任务、设计、编程、文案、营销、游戏练级等多类网络兼职。报道中的一个软件专业学生在威客平台接下简单订单系统任务，三天后完成并交付；另有校园 BBS 招聘兼职记者/论坛管理员的帖子示例，联系方式可以直接导向 QQ。

存续页：

- 新浪转载《江西日报》，2009-04-14，《“网络兼职”受大学生追捧》：
  <https://news.sina.com.cn/o/2009-04-14/082815463441s.shtml>

证据等级：**B（同期新闻）**；报道中引用的具体 BBS 招聘语句并不等于已取得原始 thread capture。

### 7.1 A topology change

2006 黄石案例：

```text
web = discovery + complaint publication
physical world = interview + travel + work + lodging + most dispute execution
```

2009 部分威客/设计/编程案例：

```text
web = discovery + negotiation + work delivery + reputation (sometimes payment)
```

因此旧网研究不应把所有“兼职网站/帖子”放在同一类。需要字段：

```yaml
network_role:
  discovery: yes/no
  identity: yes/no
  negotiation: yes/no
  execution: yes/no/partial
  delivery: yes/no
  payment: yes/no/unknown
  reputation: yes/no/unknown
```

这能区分 **Web as noticeboard** 与 **Web as workplace**。

---

## 8. BBS / QQ / phone form a multi-system labor stack

2009 报道里，招聘文字可能出现在校园 BBS，但联系方式直接要求“加 QQ”；2006 案例则由 BBS 进入线下地址、电话、火车和纸质合同。

因此一条兼职不能用一个 `platform = BBS` 字段概括。更准确的系统是：

```text
public discovery layer: BBS / portal / task site
private coordination layer: QQ / phone / SMS / email
institutional layer: office / company / school affiliation / contract
mobility layer: bus / rail / temporary lodging
execution layer: classroom / client site / remote PC
payment layer: cash / bank / platform
memory layer: complaint post / repost / news article
```

这与 `PAGER_GATEWAYS...` 文档的跨网络思想相似，但劳动链的终点不是“人收到消息”，而是**现实劳动是否真正执行与结算**。

---

## 9. A new archive bias: successful gig legibility

兼职和零工在旧网档案中有两种相反的可见性偏差。

### 9.1 Advertised opportunity bias

招聘帖、门户专题和“高薪兼职”广告很容易被抓到；真正有多少人联系、面试、入职、拿到钱却常常不可见。

```text
archived gig menu != enacted gig population
```

### 9.2 Complaint / exception bias

另一方面，一段普通完成、正常结算的两周家教可能根本不再被发帖；被骗、争议、夜宿街头、欠薪等异常事件反而更容易变成热门帖和新闻。

```text
surviving complaint corpus != normal outcome distribution
```

研究者因此既不能因为招聘很多就说“兼职机会丰富且执行顺利”，也不能因为幸存材料大量是骗局就说“兼职通常都失败”。

---

## 10. Evidence contract for short-gig artifacts

建议以后遇到中文旧网兼职/零工材料时至少记录：

```yaml
artifact_id:
platform:
board_or_section:
original_url:
capture_url:
internal_datetime:
capture_datetime:
evidence_grade: A | B | C | D

artifact_role: listing | reply | complaint | correction | repost | media_quote | platform_help
poster_handle:
poster_real_identity_verified: true | false | unknown
institution_affiliation_claim:
institution_affiliation_verified: true | false | unknown
employer_claim:
external_employer_verification: true | false | unknown

work_type:
advertised_location:
advertised_duration:
advertised_hours:
advertised_pay:
contact_channels: []

discovery_online: true | false | unknown
interview_mode:
contract_mode:
execution_mode: offline | online | hybrid | unknown
travel_required: true | false | unknown
lodging_required: true | false | unknown

outcome_observed: true | false
outcome_state:
payment_state:
complaint_state:

content_origin_id:
copy_relationship:
independent_observation:

missing_layers: []
privacy_notes:
researcher_inference:
```

---

## 11. Evidence grades for this note

### B — 2006 press reconstruction

The 2006 Sina/Huaxia Times page is near-contemporaneous reporting. It includes journalist interviews, descriptions of then-live BBS posts, a photographed paper contract and a detailed chronology. It is stronger than later nostalgia, but it is **not** the same as the missing original BBS captures.

Claims allowed:

- the press reported seeing/describing those posts at that time;
- interviewed participants described the chain;
- the press reconstructed specific dates and offline steps.

Claims not allowed without original captures:

- exact original HTML / headers / thread structure;
- every quoted/reported line is byte-identical to the source post;
- deletion cause;
- poster account ownership beyond what the report establishes.

### B — 2009 press report

The 2009 Sina/Jiangxi Daily page is contemporaneous evidence that BBS, QQ and task websites were being discussed/used for several forms of student part-time work. It does not estimate prevalence and does not authenticate each cited platform account.

### A candidate — future work

If a dated Wayback/Common Crawl capture of the original 2006 SMTH recruitment/complaint or PKU Weiming thread is found, it can be promoted to A-level artifact evidence. Until then, do not manufacture an original thread from newspaper prose.

---

## 12. Counterexamples and hindsight risks

- **BBS job post ≠ platform endorsement.**
- **University affiliation ≠ legal employer verification.**
- **Contract ≠ actual working conditions.**
- **Post deletion ≠ voluntary recantation.**
- **Cross-post ≠ independent corroboration.**
- **Online recruitment ≠ online work.**
- **Online work ≠ platform-mediated payment.**
- **Visible complaints ≠ representative outcome distribution.**
- **2009 “网络兼职” label ≠ all students already had routine access to such work.**
- Do not re-index ordinary students' names, historic contact details or other unnecessary personal data merely because a 2006 press page remains public.

---

## 13. What this changes in old-web archaeology

兼职材料迫使旧网考古把“网页是否存在”向外延伸一步：**一个页面可以只是一段现实劳动链的入口。**

对于这类 artifact，真正应研究的是：

```text
URL / post
→ trust
→ private contact
→ embodied execution
→ outcome
→ complaint / memory
```

其中绝大多数箭头都不会被传统网页快照直接保存。

所以本仓以后遇到兼职、求租、交易、报名、约见等页面，都应先问：

> **这个 Web artifact 是“行为本身”，还是只负责把人送到行为发生的地方？**

如果只是入口，那么 archive 能证明的主要是当时的**可发现性、可联系性和公开承诺**；现实结果仍需合同、新闻、当事人同期记录或其他独立证据才能补上。

---

## 14. Next high-value target

优先寻找：

1. 2006 SMTH 原招聘帖、原投诉帖、《我在黄石完全是一场误会》替换帖的历史 capture；
2. 同日晚北大未名《黄石带班遇险受骗记》的原始 capture；
3. 一个 2001–2005 中文校园 BBS 中“招聘 → 回复/更新 → 已招满/撤帖 → 后续体验”的同一 thread 多时点序列；
4. 2008–2009 威客平台中一笔公开任务从发布、接单、交付到评价的历史 artifact 链。

如果这些拿不到，**“原帖已无法可靠复原，只剩近同时代新闻重建”本身就是应记录的正式负结果。**
