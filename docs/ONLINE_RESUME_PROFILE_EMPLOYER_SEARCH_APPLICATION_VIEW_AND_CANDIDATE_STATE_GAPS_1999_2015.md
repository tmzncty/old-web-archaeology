# ONLINE RESUME / PROFILE / EMPLOYER SEARCH / APPLICATION / VIEW STATE GAPS (1999—2015)

> Status: research package / state-gap note  
> Scope: 中文旧网约 1999—2015。海外 Usenet / Monster 只作技术与形态前史对照，不把本仓扩成全球招聘史。  
> Life-history companion: `tmzncty/how-people-lived/topics/from-paper-resume-to-searchable-candidate-profile-candidate-legibility-and-life-course-serialization-china-1980-2026.zh-CN.md`

## 0. 研究问题

招聘网站很容易在 archive 中留下“职位搜索框”“注册简历”“投递”按钮，于是后来的研究者会产生一个危险错觉：

> 看见了招聘页面，就仿佛也看见了当时的人怎样进入候选人库、怎样被企业搜索、筛选、查看和联系。

实际上至少存在两条不同事务：

```text
求职者：
job page
→ choose/create resume
→ submit
→ server receives
→ parse/index
→ employer job inbox
→ view/filter
→ contact/interview/reject/unknown

企业：
enterprise account
→ query/filter candidate database
→ result list
→ open candidate detail
→ unlock/download/contact
→ interview/hire/ignore
```

本稿研究的不是“招聘网站历史”本身，而是旧 Web 中**候选人记录如何成为可查询对象，以及 archive 为什么特别容易保存界面却丢失真实候选人状态**。

---

## 1. 与仓库 METHOD 对齐

本稿遵守 `docs/METHOD.md`：

- platform / host / account / page / capture / claim 分开；
- A/B/C/D 分级；
- archive locator 未实际打开不得写成 verified capture；
- `exists != available != used != popular != caused`；
- modern page / current backend 不得冒充 historical transaction；
- `没有找到 != 当时不存在`；
- 不为“考古完整”重新公开真实普通人的姓名、电话、住址、工作史、求职意向等私人简历内容。

本专题固定以下边界：

```text
resume form captured
!= resume database captured

resume submitted
!= parsed
!= indexed
!= searchable
!= matched
!= viewed
!= contacted
!= interviewed
!= hired
```

---

## 2. 研究对象必须拆层

### 2.1 platform / host

例如：

- 前程无忧 / `51job.com`；
- 中华英才网 / `chinahr.com`；
- 智联招聘；
- 企业自己的招聘子站；
- 校园招聘系统。

品牌连续不等于数据库 schema、搜索逻辑、权限策略连续。

### 2.2 account

至少区分：

- job-seeker account；
- employer / recruiter account；
- platform operator account；
- delegated enterprise sub-account。

企业账号可见的候选人页面通常不是普通公众 Web 页面。

### 2.3 resume / candidate profile

一个候选人可能同时存在：

- profile metadata；
- online resume；
- uploaded Word/PDF；
- multiple resume variants；
- language variants；
- current revision；
- stale revision；
- employer-downloaded copy。

`person != candidate record != one resume revision`。

### 2.4 application

一次申请应单独视为 transaction object：

```text
candidate_id
+ resume_revision_id
+ job_id
+ submitted_at
+ platform receipt state
+ employer-side state
```

不能只凭候选人最终入职结果倒推出此前某一次 application 的内部状态。

### 2.5 search result

企业搜索结果可能依赖：

- query keywords；
- location；
- industry / position；
- education；
- experience；
- salary；
- availability；
- update time；
- visibility state；
- ranking logic；
- enterprise permissions；
- current index snapshot。

所以同一个 query 在不同时间不必得到相同结果。

---

## 3. 海外前史边界：Web 以前已经出现“格式先替机器筛一遍人”

Usenet `misc.jobs.offered` / `misc.jobs.resumes` 是本专题的前史对照，不属于本仓主体。

历史 Jobs FAQ 保存的统计称，1994 年 12 月两个星期内：

- `misc.jobs.offered`：8824 posts；
- `misc.jobs.resumes`：4286 posts。

同一 FAQ 明确说数量已经大到不可能合理逐条阅读，因此 Subject 应稳定包含 location 与简短 job description，让计算机先做筛选。

Sources:
- https://stason.org/TULARC/society/job-offers/1-1-What-isn-t-misc-jobs-offered.html
- https://stason.org/TULARC/society/job-offers/2-misc-jobs-offered-Why-have-posting-guidelines.html

Evidence: **B+，历史技术社区 FAQ 的公开保存；统计值在 FAQ 中归因于同期 Usenet stats。**

用途仅限证明：

> 只要职位/简历数量超过人工逐条阅读能力，格式和字段就会开始参与可见性。

不要写成：

> 1994 年美国普通人已经普遍通过网络数据库求职。

当时 Usenet 接入人群高度偏向高校、科研和技术用户。

Monster 的 1997—2003 材料又证明另一层：在线简历不只是一篇公开帖子，而可以成为受限数据库记录。1997 Microsoft 与 Monster Board 的同期合作公告已经允许申请者在线申请、建立在线简历，并接收匹配职位；2003 Monster 监管文件明确写出候选人可保存 resumes / cover letters / applications，并看到简历被潜在雇主查看的次数，付费雇主可以在 access-restricted resume database 中按关键词、地点等检索。

Sources:
- Microsoft, 1997-10-14: https://news.microsoft.com/source/1997/10/14/microsoft-and-the-monster-board-offer-exclusive-resource-to-recruit-skilled-candidates-for-41000-jobs-in-microsofts-channel/
- SEC, Monster/TMP 2003: https://www.sec.gov/Archives/edgar/data/1020416/000104746903037619/a2121724zs-3a.htm

Evidence: **A，同期公司公告 + 监管文件。**

这仍然只是跨国形态对照，不证明中国网站直接照搬某一特定系统。

---

## 4. 1999—2004：中国候选人数据库进入一个仍然高度混合的招聘世界

前程无忧 2004 年 SEC prospectus 是目前本稿最强的一手平台证据之一。

文件称：

- `51job.com` 自 1999 年建立；
- 求职者可以在网站发布简历；
- 企业通过 Web-based `eHire` 管理和组织在线简历与候选人审阅；
- 公司口径截至 2004-06-30 约有 690 万 registered job user accounts、约 460 万 posted resumes；
- 2003 年公司收入中 print advertising 仍约占 62.3%，online recruitment services 约占 26.2%。

Source:
- SEC 2004: https://www.sec.gov/Archives/edgar/data/1295484/000114554904001289/u99016a6e424b4.htm

Evidence: **A，同期监管文件；规模与市场地位是公司披露口径。**

同一份文件还明确说，中国私人部门招聘仍大量依赖 personal referrals 和 large job fairs；公司的纸质招聘刊物也被用于触达不易接入 Internet 的中低收入求职者。

因此这里必须写：

```text
online resume database exists
!= all job seekers online
!= all occupations represented equally
!= paper/job fair/referral disappeared
```

中文旧网中的候选人数据库不是从零替换现实招聘，而是在现场招聘会、介绍、报刊和电话旁边增加一层远程检索接口。

---

## 5. Candidate profile state machine

一个最小在线简历至少需要拆成：

```text
C0 account exists
C1 resume draft created
C2 fields entered
C3 uploaded document attached (optional)
C4 save request issued
C5 server accepts record
C6 parse/normalize succeeds or partially succeeds
C7 visibility policy set
C8 index updated
C9 candidate becomes searchable (if policy permits)
C10 candidate record matched by an employer query
C11 result-list row rendered
C12 recruiter opens detail
C13 recruiter downloads/unlocks/contact action
C14 candidate refreshes/edits
C15 previous revision becomes stale / replaced
C16 candidate hides/deletes/closes account
```

硬边界：

```text
C4 != C5
C5 != C6
C6 != C8
C8 != C9
C9 != C10
C10 != C12
C12 != C13
C16 on platform != every downloaded copy deleted elsewhere
```

---

## 6. Visibility policy 是独立状态，不等于“有没有一份简历”

2009 年前程无忧同期公告把简历公开状态分成至少三档：

- 完全保密；
- 对无忧公开；
- 完全公开。

“完全公开”意味着企业会员和平台工作人员可以检索/查看；求职者可调整状态。

Sources:
- 51job / PR Newswire Asia, 2009-03-24: https://www.prnasia.com/story/18318-1.shtml
- 同期商业媒体转述可作为另一入口。

Evidence: **A（平台当时规则声明）+ B（同期媒体转述）。**

这支持：

```text
resume storage state
!= employer-search visibility state
```

尤其对在职求职者，保留未来跳槽选项与让陌生企业主动检索自己的职业历史，是两件不同的事。

但平台宣称“保护”并不能自动证明所有执行、第三方下载和企业账号行为都没有漏洞。

---

## 7. 2008：submission cost 降低以后，review scarcity 变得更明显

2008 年一组同期校园招聘材料已经出现明显的新状态差。

长江日报报道武汉校园招聘时，吉利在宣讲后要求应聘者只通过中华英才网、且在 6 小时内网投简历。受访学生邓同学说网上投简历方便，但见不到人，真实个性和能力难以充分展示；企业 HR 则解释，网上可以按专业、学校、英语、实践经验、薪酬范围等限制项快速分类海量简历。

Source:
- 长江日报 / 新浪教育，2008-10-22: https://edu.sina.com.cn/l/2008-10-22/1127153829.shtml

Evidence: **B，同期媒体 + 求职者/HR 同期引语。**

这条证据非常重要，因为它直接给出：

```text
human self-presentation
→ form fields
→ filter conditions
→ candidate subset
```

同一时期还有学生反映投出大量网络简历却缺乏回复。这里不能反推“ATS 自动淘汰”，只能固定：

> **submission cost下降，并没有同步消除 recruiter review scarcity。**

所以：

```text
application submitted
!= application visibly reviewed
```

---

## 8. 2009 recruiter-side first person：旧 Web 的候选人列表不是中性的“电子纸”

2009-10-30，博客园作者记录自己因公司招聘而使用中华英才网企业账号。

他描述的实际工作流包括：

```text
设置简历筛选器
→ 分页浏览候选人列表
→ 打开简历详情
→ 下载/导出
→ 转交秘书通知面试
```

可观察字段包括：

- 更新时间；
- 行业；
- 职位；
- 工作年限；
- 学历；
- 地点；
- 年龄/性别等个人属性；
- 职业目标；
- 求职意向；
- 期望薪水；
- 到岗时间；
- 工作经验；
- 教育；
- 技能。

作者还明确说企业端可以按更新时间排序，因此建议求职者经常刷新；关键词在列表中的可见程度也会影响被注意。

Source:
- 博客园，2009-10-30: https://www.cnblogs.com/over140/archive/2009/10/30/1592961.html

Evidence: **B，同期 recruiter-side 第一人称操作记录；不代表所有企业、所有年份或整个平台规则。**

它证明的是一种很具体的旧网页面形态：

> 候选人的人生不是整份 Word 文件原样进入 HR 视野，而会先经过一个带字段、列表、排序、分页和筛选器的检索界面。

---

## 9. Resume freshness / 更新时间是瞬时状态，archive 特别容易把它“石化”

如果 recruiter 可以按更新时间排序，那么 `updated_at` 至少同时具有两种语义：

1. 内容最后保存时间；
2. 在候选人搜索中的 freshness / activity signal。

这产生：

## freshness petrification / 新鲜度石化

一个 2009-10-30 capture 若显示“今日更新”，二十年后仍可能把这个标签冻结在页面里。

因此：

```text
captured 'recently updated'
!= candidate remained active after capture
```

反过来，如果今天 live backend 为一个旧账号重新计算“最后活跃”，也不能把当前值投回历史 capture。

---

## 10. Application state machine

一次“网投”至少拆成：

```text
A0 job page rendered
A1 apply action initiated
A2 resume/version selected
A3 questionnaire/cover letter completed (if any)
A4 request issued
A5 platform receives application
A6 validation passes
A7 application linked to job
A8 employer-side inbox/list includes record
A9 recruiter search/filter leaves it visible or excludes it
A10 recruiter opens candidate/application
A11 recruiter records internal disposition (optional)
A12 contact/interview invitation issued (optional)
A13 candidate receives notice (optional)
A14 process ends: hired/rejected/expired/unknown
```

必须固定：

```text
'已投递' UI
!= A8 employer inbox confirmed
!= A10 recruiter viewed
!= A11 recruiter decided
```

平台可能只能证明自己的 transaction 已接收，无法证明企业内部 HR、邮件、电话或线下流程发生了什么。

---

## 11. Search result state machine

企业搜索候选人也不是一个静态页面：

```text
S0 employer authenticated
S1 subscription/permission checked
S2 filters entered
S3 query normalized
S4 current resume index queried
S5 visibility policy applied
S6 ranking/sort applied
S7 result page rendered
S8 pagination / next page
S9 candidate opened
S10 download/contact quota consumed (if applicable)
```

关键 archive 风险：

### query-result orphaning / 查询—结果孤儿化

搜索表单可能保存，真正的数据库和 result payload 没保存。

### ranking-time gap / 排名时间差

同一 query 在：

- 2009-10-30 09:00；
- 2009-10-30 17:00；

就可能因为新简历和 refresh 得到不同排名。

因此：

`search URL survives != historical result set reproducible`。

---

## 12. Candidate shell bias：最容易活下来的恰恰不是普通人的真实求职记录

archive 更容易留下：

- “注册简历”首页；
- 简历模板/help；
- 企业服务介绍；
- 搜索框；
- 隐私政策；
- 新闻稿；
- demo screenshots。

最难留下：

- 私人在线简历；
- 企业登录后的搜索结果；
- application inbox；
- 谁看过我；
- 企业内部淘汰原因；
- 下载到 recruiter 本地的 Word/PDF；
- 电话联系与线下面试。

因此新增：

## candidate-shell bias / 候选人壳层偏差

历史 Web 很容易证明“这个系统提供简历功能”，却很难证明一名普通求职者的记录当时处在哪一层状态。

这不是需要被“补齐”的缺陷。私人简历本来就包含高密度个人信息：

- 姓名；
- 电话；
- Email；
- 地址；
- 教育；
- 工作史；
- 薪资；
- 求职意向；
- 家庭/年龄等可能敏感字段。

本仓的目标是复原 schema 与 transaction，不是重新公开真实人的私人求职档案。

---

## 13. Revision collapse：一个“最终简历”会遮住此前许多个自己

在线简历可反复修改：

```text
R0 first draft
→ R1 求职目标调整
→ R2 新增项目
→ R3 换城市
→ R4 薪资期望变化
→ R5 再次刷新
```

如果平台只保留 current version，archive 即使偶然保存了一份 detail 也可能只有某个时点的 snapshot。

因此：

`one captured resume != complete candidate history`

`current profile != profile used for an earlier application`

这叫：

## revision collapse / 修订折叠

尤其不能用 2012 年账号最终状态倒推 2009 年投某份工作时的简历内容。

---

## 14. Download escape：简历一旦离开平台，删除语义会断裂

企业端若支持：

- download；
- export；
- print；
- copy contact details；

则会形成：

```text
platform-controlled record
→ employer-local copy
```

从这一步开始，平台上的：

- hide；
- edit；
- delete；
- close account；

不必然能改变已经被企业保存到本地的副本。

新增概念：

## download escape / 下载逃逸

```text
resume removed from platform
!= every previously downloaded copy removed
```

这也是为什么 2019 年以后简历泄露问题能反过来帮助我们理解 2000s 的数据结构风险，但 2019 本身不属于本仓主要时段。

作为 downstream validation，2019 年中国青年报、新华社等同期调查记录了：在线投简历后出现无关骚扰电话、简历倒卖、销号困难等问题。

Sources (out-of-scope downstream evidence, not 1999—2015 artifact proof):
- https://society.people.com.cn/n1/2019/0920/c1008-31363093.html
- https://finance.people.com.cn/BIG5/n1/2019/0712/c1004-31231346.html

---

## 15. Terminal hiring hindsight bias：最终结果会抹掉早期的不确定性

如果后来材料只保存：

> “某人通过网站找到工作。”

研究者很容易把此前过程压平为顺利链条。

真实过程可能是：

```text
投 100 份
→ 80 份无可见状态
→ 15 份拒绝/过期
→ 5 次面试
→ 1 个 offer
```

archive 和成功案例最容易留下最后一条。

新增：

## terminal hiring hindsight bias / 录用终态后见偏差

`final hire evidence != earlier application certainty`。

---

## 16. Schema hindsight：不能拿今天的招聘字段倒写 2008

现代招聘系统可能有：

- 技能图谱；
- AI 匹配；
- video interview score；
- project portfolio；
- GitHub / social link；
- auto-parsed PDF；
- model-derived candidate tag。

2008 recruiter first-person 可以证明当时某平台/账号看到了更新时间、学历、工作年限、地点、期望薪资等字段；它不能证明今天每一个字段当年都存在。

同理：

```text
current platform help page
!= historical schema documentation
```

如果今天 live eHire 有 retention、download quota 等规则，只能作为 current rule，除非找到同期历史材料，否则不得回填 2004/2009。

---

## 17. 2008 artifact family：限时网投把“提交窗口”本身变成动态 Web 状态

2008 武汉校园招聘材料还有一个 old-Web 特有问题：企业宣讲结束后只开放 6 小时网投。

这意味着一个历史职位页面可能存在：

```text
before window opens
→ accepting applications
→ deadline passes
→ job page remains visible
→ application endpoint rejects
```

因此：

`job page visible != application currently executable`。

一个 archive capture 若只保存宣讲/职位说明，却没有同时保存 submission window 和 backend response，不能证明当时该时刻仍可投。

这可以命名为：

## application-window drift / 投递窗口漂移

---

## 18. Browser / charset / upload conditions

1999—2015 在线简历还可能受到：

- GB2312 / GBK / UTF-8；
- IE-only form/JS；
- popup；
- old file upload restrictions；
- Word `.doc` / `.docx` / PDF 支持差异；
- ActiveX/editor components；
- session/cookie；
- captcha；
- cross-domain enterprise login；
- HTTPS migration；
- email activation。

因此 modern Chromium 能打开一个 old form，不等于历史浏览器下完整 transaction 可执行。

尤其中文姓名、学校、公司和职位关键词若发生编码错误，会直接改变搜索可见性。

---

## 19. Preservation levels

### P0 — mention only
只知道平台/功能被同期材料提及。

### P1 — public shell
保存公开首页、职位页、简历注册/help 等壳层。

### P2 — schema surface
能确认历史字段、下拉项、visibility 规则或帮助文档。

### P3 — candidate transaction surface
能确认 save/submit/upload 等请求结构，但不需要真实私人数据。

### P4 — employer search surface
能确认筛选器、排序、结果列表 schema 或官方 demo。

### P5 — state transition evidence
能确认某些 historical transaction state，例如 submit success / visibility change / view counter 语义。

### P6 — historical browser reconstruction
在旧浏览器/编码条件下验证公开 demo 或非敏感 fixture，明确标 reconstruction。

### P7 — privacy-safe semantic reconstruction
可用合成测试记录重建：candidate → index → query → view → application 的状态模型；仍不要求取得真实普通人的私人简历或企业后台数据。

**最高 preservation level 不等于把私人 candidate database 公开。**

---

## 20. 本轮 historical replay 尝试与负结果

本轮已实际尝试直接打开：

- 约 2009 的 `chinahr.com` Wayback replay；
- 约 2009 的 `51job.com` Wayback replay。

当前访问链拒绝未经搜索结果产生的构造 Wayback URL，因此没有获得可逐项检查：

- `original_url`；
- `capture_url`；
- `capture_datetime`；
- HTTP；
- charset；
- DOM；
- form action；
- enterprise search / resume state

的合格 memento。

所以本轮严格记录：

```text
M1 verified 51job historical resume/search capture:
NOT ACHIEVED IN THIS SLICE

M1 verified ChinaHR historical resume/search capture:
NOT ACHIEVED IN THIS SLICE
```

这**不等于 Wayback 没有保存**。

后续可以从 archive search result、CDX、已知历史深层 URL 或可访问 WARC 再继续定位。

---

## 21. 证据强度总表

| Claim | Evidence | Grade | Boundary |
|---|---|---:|---|
| 1990s 海外网络已经遇到职位/简历规模过大、需要机器预筛格式的问题 | Usenet Jobs FAQ | B+ | 不代表普通人口普及 |
| 1997–2003 Monster 已把在线简历做成 persistent/searchable restricted DB | Microsoft + SEC | A | 海外形态对照，不证明中国直接复制 |
| 2004 51job 已有 online resume + eHire 候选人管理 | SEC | A | 用户/简历规模为公司口径 |
| 2004 招聘仍大量与 referral / job fair / print 并存 | 51job SEC 自述 | A | 描述公司所处市场，非全行业精确份额 |
| 2008 校园招聘企业使用字段限制项快速分类网投简历 | 长江日报同期采访 | B | 单一招聘案例 |
| 2008 求职者觉得网投方便但难充分展示个人 | 同一同期第一人称 | B | 不代表全部学生 |
| 2009 51job 有三档简历可见性状态 | 平台同期公告 | A | 规则声明不等于零执行漏洞 |
| 2009 recruiter 可按字段、更新时间等筛选候选人 | 博客园 recruiter 第一人称 | B | 单一企业账号/平台使用经验 |
| 历史 search/result 无法从当前 live backend 自动重现 | 状态模型 + METHOD | D/Method | 需具体 capture 验证每个站点 |
| 平台删除不等于企业下载副本被删除 | 系统边界推断 | D-high | 需要历史条款/客户端证据进一步实证 |

---

## 22. 已证实 / 高概率 / 不知道

### 已证实

- 2004 51job 的 Web 招聘明确包含求职者发布简历与企业 eHire 候选人管理；
- 当时 print、招聘会、个人介绍仍与在线系统并行；
- 2008 至少有企业把校园招聘申请强制放进网上字段筛选；
- 2009 至少一名真实 recruiter 记录了筛选器、列表、更新时间排序、详情与下载工作流；
- 2009 前程无忧明确提供不同简历可见性状态。

### 高概率但仍需更强 artifact

- 2000s 主流招聘站候选人检索普遍依赖动态/private backend；
- “刷新简历”在多个平台被作为提高 candidate recency 的操作；
- 许多 employer search query/result 页面不会被 public Web archive 正常保存。

### 本轮不知道

- 2000、2003、2006、2009 各平台具体 resume schema 的逐年字段差异；
- 中华英才网 2009 企业 search form 的 canonical URL 与参数；
- 51job 2009 某一 search query 的 historical result list；
- 每个平台何时开始保存/展示“谁看过我”；
- candidate delete 对 employer-downloaded copies 当年的正式 retention 规则；
- 某一名 2008 学生的申请究竟在哪个 state 被丢弃。

---

## 23. 对 old-Web 保存机制的新认识

本专题把中文旧网的“人”进一步拆成两类完全不同的可见对象：

```text
public self-publishing identity
vs
private/semi-private candidate identity
```

个人主页、博客、论坛账号希望被公众看见，因此 archive 相对容易获得公开 representation。

在线简历则相反：它希望**被一个受限职业市场看见，但不希望被所有人看见**。

所以它是一种特殊历史对象：

> **越接近普通人真实人生路径的数据，越可能因为登录、权限、隐私和动态数据库而天然抗公开归档。**

这不是 archive 做得“不够好”这么简单，而是对象的访问控制本来就是历史的一部分。

---

## 24. 它改变了我们怎样理解中文旧网？

1990s–2000s 中文 Web 不只是让普通人“找到更多招聘广告”。更深的一层是：人的学校、工作年限、城市、薪资预期、到岗时间和更新时间开始进入一个企业可以主动查询的数据库。

这意味着 Web 同时做了两件方向相反的事：

```text
求职者可以搜索职位
+
职位背后的企业也可以搜索求职者
```

一旦这两条搜索线同时成立，“找工作”就不再只是一次人去找机会的行动，而变成**人必须维持一个能够长期被职业系统读取的版本自己**。

从考古角度看，这一版本的“自己”又恰恰最容易消失：公共首页还活着，真正决定谁被看见的候选人索引、筛选器结果、更新时间、申请状态和企业下载副本却可能已经全部不可见。

因此研究旧招聘 Web，最重要的不是把某个私人简历挖回来，而是把这些**可见性状态、权限边界与事务缺口**保存下来。
