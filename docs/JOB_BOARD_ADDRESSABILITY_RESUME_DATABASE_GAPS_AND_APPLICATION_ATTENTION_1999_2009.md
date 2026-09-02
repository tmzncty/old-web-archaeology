# JOB_BOARD_ADDRESSABILITY_RESUME_DATABASE_GAPS_AND_APPLICATION_ATTENTION_1999_2009

## 研究问题

1999—2009 年中文旧网中，“招聘”不是一种单一页面形态。

同一个求职流程里可能同时出现：

- 门户求职频道；
- 专业人才网站；
- 高校就业信息网；
- 校园 BBS 招聘版；
- 企业招聘页；
- 电子简历数据库；
- 在线双选会；
- 网上洽谈室；
- Email；
- 手机 / 短信；
- 现场宣讲会和招聘会；
- 学校就业推荐表和学籍信息；
- 主管部门核准。

如果只保存一张“职位详情页”截图，很容易误以为自己已经保存了历史招聘市场。

实际上真正决定求职体验的是一套动态状态系统：

```text
岗位是否仍开放？
求职者能否找到它？
简历是否公开？
企业能否搜索到这份简历？
投递是否被系统接受？
是否通过字段过滤？
有没有人真正阅读？
面试通知通过什么渠道到达？
最终是否线下面试、签约、核准并到岗？
```

本文件提出两个核心概念：

1. **job-board addressability（招聘市场可寻址性）**：岗位与求职者不只被“发布”，还可以进入索引、数据库和查询接口，被远方陌生人搜索；
2. **application-attention gap（申请—注意力缺口）**：Web archive 容易保存“一个人可以点击投递”的界面，却极难证明简历后来是否被检索、打开、筛选、回复或转化为面试。

它与已有文档的边界如下：

- `APPLICATION_STATE_ELIGIBILITY_AND_ROUTE_PORTFOLIO_2003_2015.md` 主要处理考试 / 正式申请工作流和资格状态；
- `ABANDONED_APPLICATIONS_AND_NEGATIVE_STATE_SURVIVAL_2007_2015.md` 主要处理放弃、缺席等负状态；
- 本文专门处理**劳动市场中的岗位索引、简历数据库、职位搜索、电子投递、雇主筛选和回应不可见性**。

研究主体严格停留在约 1995—2015 中文旧网 scope；本文核心证据集中在 1999—2009。

---

## 1. 研究单位：不要把“招聘网站”当成一个对象

沿用 `docs/METHOD.md`，至少拆开下面这些对象：

```text
platform
site / host
employer account
job-seeker account
vacancy record
vacancy detail page
search query
search-result page
candidate profile
resume version
resume visibility state
application event
employer search / view event
screening rule
interview invitation
email / SMS notification
online chat / negotiation event
offline interview
employment agreement
institutional approval
hire / arrival
archive capture
claim
```

### 为什么必须拆

同一条历史 URL 可以证明：

- 某个岗位当时曾被页面表示；
- 某字段曾出现在申请表里；
- 平台宣称允许企业检索简历；

却通常不能证明：

- 岗位在 capture 当天仍然开放；
- 搜索结果完整；
- 某简历对企业可见；
- 企业真的搜到某个人；
- 投递真的进入招聘方队列；
- HR 打开过；
- 系统为什么淘汰；
- 面试通知是否到达；
- 用户是否参加面试；
- 最终是否入职。

所以：

> **archived recruitment page ≠ archived recruitment process**

---

## 2. 两条独立生命周期：岗位状态和求职者状态

### 2.1 Vacancy lifecycle

建议最低拆成：

```text
draft
→ published
→ indexed
→ searchable
→ applications accepted
→ paused
→ filled / withdrawn / expired
→ page retained / removed
```

页面还在，不表示状态仍停留在 `applications accepted`。

必须固定：

> **vacancy URL present ≠ position open**

以及：

> **posting date ≠ availability interval**

### 2.2 Candidate / resume lifecycle

```text
account created
→ profile created
→ resume uploaded / entered
→ visibility configured
→ searchable by employer
→ application sent
→ employer viewed / not viewed
→ filtered / shortlisted
→ interview invitation
→ interview
→ offer
→ accepted / declined
→ hired
→ resume hidden / stale / deleted
```

必须固定：

> **resume uploaded ≠ employer-searchable resume**
>
> **resume searchable ≠ resume viewed**
>
> **application sent ≠ application read**
>
> **application read ≠ shortlisted**
>
> **interview invitation ≠ interview attendance**
>
> **offer ≠ hire**

---

## 3. Evidence family A：1999 年“招聘信息不够丰富”——早期 Web 不能从存在直接跳到成熟

1999 年 10 月《生活时报》根据当年 CNNIC 报告讨论中国互联网内容供给时，明确把“求职招聘信息”列为当时相对不够丰富的类别。

来源：

- 《生活时报》，1999-10-27，《网上“求职招聘信息”不够丰富》：<https://www.gmw.cn/01shsb/1999-10/27/GB/shsb%5E1144%5E0%5ESH7-2726.htm>

证据等级：**B：同时代媒体观察**。

同一时期 CNNIC 1999 年 7 月报告称中国上网用户约 400 万，上网计算机约 146 万台；其在线问卷受访者主要在单位或家庭上网。

来源：

- CNNIC 1999 年 7 月统计报告的新浪历史页面：<https://tech.sina.com.cn/news/it/1999-12-15/13431.shtml>

证据等级：**A/B：同期统计报告网络转载**。

这两条证据共同支持一个非常窄的边界：

> 1999 年求职招聘已经进入中文 Web，但不能因为能找到招聘栏目，就重构成后来成熟招聘平台那种丰富、持续更新、广泛可及的市场。

### 旧网研究中的对应规则

```text
job channel exists
≠ rich vacancy corpus
≠ frequently updated corpus
≠ broad labor-force access
≠ primary job-search channel
```

---

## 4. 2001：在线就业系统开始把三类主体放进一个工作流

2001 年 12 月新华社报道南京推动毕业生就业网上办理，明确出现：

```text
用人单位网上招聘
+ 毕业生网上求职
+ 主管部门网上审批
```

报道记录网站开通约一个月后已有：

- 200 家招聘单位；
- 4000 多个岗位；
- 4000 多名毕业生登录求职资料；
- 近百名毕业生达成双选意向并经网站申报核准。

来源：

- 新华社 / 新浪科技，2001-12-20，《明年起南京毕业生就业工作全部网上办理》：<https://tech.sina.com.cn/i/c/2001-12-20/96819.shtml>

证据等级：**B：同时代新闻报道**。

### 这里证明的是 system topology，不是每个 outcome

可以支持：

- 求职资料数据库存在；
- 岗位数据库存在；
- 双选与行政核准在同一网络服务体系内被连接；
- 至少有一部分真实用户和用人单位使用。

不能自动支持：

- 每个岗位的历史快照都完整保存；
- 4000 份资料都同时公开可检索；
- “达成意向”后来全部实际入职；
- 网站是南京全部毕业生的唯一渠道。

因此：

> **platform-reported workflow completion ≠ independently verified employment outcome**

---

## 5. 2003：高校就业站已经不只是公告板，而是数据库 + 论坛 + 洽谈室

中南大学目前保存的一篇 2003 年《中国教育报》报道，描述其毕业生就业指导信息网包含：

- 网上快讯；
- 招聘中心；
- 求职中心；
- 就业政策与形势；
- 就业论坛；
- 网上招聘洽谈室；
- 毕业生档案馆；
- 留言 / 教师答复。

报道还列出学校自报的会员、电子简历、企业会员和招聘信息规模。

来源：

- 中南大学新闻网，保存《中国教育报》2003-03-29 报道：<https://news.csu.edu.cn/info/1143/101248.htm>

证据等级：**B：同时代媒体文本；平台规模和“求职成功”数字为校方自报**。

### 对旧网形态研究的意义

这里至少出现三类页面 / 状态：

```text
public information pages
authenticated candidate data
interactive employer-candidate spaces
```

这三类 archive 可见性极不相同。

公开新闻可能今天仍在；
真正的：

- 电子简历；
- 登录后的求职中心；
- 招聘洽谈记录；
- 雇主后台搜索；
- 个人申请状态；

却很可能已经全部消失。

因此形成本文第一个重要缺失概念：

## resume-database invisibility（简历数据库不可见性）

> **the public shell of a job site can survive while the candidate market that made it useful disappears completely.**

---

## 6. 2003 SARS：高流量同时暴露服务端容量边界

新华社 2003 年报道山西毕业生网上双选活动时，记录网站能浏览招聘信息、提交电子档案、进入在线洽谈室；同时又明确记载，服务器只能允许约 7000—8000 人同时在线，不少学生和用人单位反复点击却无法注册和洽谈。

来源：

- 新华社 / 云南日报 / 新浪，2003-06-17，《网上求职显身手》：<https://news.sina.com.cn/e/2003-06-17/1159227983s.shtml>

证据等级：**B：同时代新闻报道**。

这对浏览器 / Web 考古很重要，因为历史页面截图不会告诉我们：

- 高峰时能否加载；
- session 是否建立；
- 注册 POST 是否成功；
- 数据库是否超时；
- 洽谈室是否已满；
- 某个求职者是否连续失败后放弃。

所以：

> **page renderability ≠ historical service availability**

以及：

> **successful modern replay ≠ historical peak-load experience**

---

## 7. 2003：申请—注意力缺口已经被同时代用户和雇主直接描述

### 求职者侧：投递以后“没有回音”

2003 年《中国青年报》采访中：

- 一名文秘求职者称 SARS 期间多次网上求职，但有时没有合适岗位，有时简历投出后没有回应；
- 一名英语教育从业者说三个月来网上投出的求职信一直没有回复；
- 一名毕业生制作个人求职网站，但效果不大，最终通过熟人获得工作。

来源：

- 《中国青年报》/ 新浪，2003-06-27，《非典难撼现场招聘霸主地位 网上招聘要跨的门槛还很多》：<https://news.sina.com.cn/c/2003-06-27/03421231604.shtml>

证据等级：**B，包含同期第一人称材料**。

### 雇主侧：简历池暴涨

同一报道中的 HR 认为网络招聘虽然节约发布成本，但大量不匹配简历反而消耗筛选时间。

2003 年《新京报》另一篇采访中，一名企业招聘负责人更直接表示，100 份电子简历中可能只有约 10 份基本符合要求，公司没有精力逐一回复淘汰者。

来源：

- 《新京报》/ 新浪教育，2003-11-26，《鼠标一点轻松搞定 网络招聘会今冬大行其道》：<https://edu.sina.com.cn/l/2003-11-26/57046.html>

证据等级：**B：同期采访，单个企业经验**。

这支持建立：

## application-attention gap（申请—注意力缺口）

```text
application interface visible
→ submission possible
→ employer queue grows
→ screening occurs somewhere off-page
→ many candidates receive no explicit state transition
```

Web archive 往往只能保存前两步。

因此：

> **submitted ≠ human-attended**

这一条与正式考试申请里的 `submitted ≠ eligible` 不同；这里缺失的是**注意力状态**而不是行政资格状态。

---

## 8. 2002：Email + 手机形成 off-platform notification dependency

2002 年《北京晨报》报道网上求职时，受访学生和业内人士把稳定 Email 与手机视为重要联系组合，并特别指出求职者不能只依赖当前单位的企业邮箱。

来源：

- 《北京晨报》/ 新浪科技，2002-07-15，《网上求职 带火收费邮箱》：<https://tech.sina.com.cn/i/c/2002-07-15/125931.shtml>

证据等级：**B：同时代媒体观察；商业邮箱用户数字不作总体外推**。

对 old-web-archaeology 来说，最重要的不是“收费邮箱流行”，而是招聘平台流程的一部分已经离开平台 URL：

```text
job-site application
→ employer system / mailbox
→ Email reply
→ mobile call / SMS
→ physical interview
```

因此新增：

## off-platform response gap（站外回应缺口）

一个招聘站的 WARC 即使保存得非常好，也很可能完全看不到：

- HR 发出的 Email；
- 邮件是否进垃圾箱；
- 手机电话；
- 短信；
- 双方约定的面试地点；
- 后续签约。

所以：

> **complete website capture ≠ complete recruitment transaction**

---

## 9. 2007：BBS、招聘站、Email 和状态查询已经构成混合发现栈

2007 年《齐鲁晚报》采访一名山东大学大四学生时，报道她几乎每天上网寻找岗位，收藏夹里同时包含：

- 人才招聘网站；
- 山东大学 BBS；
- 北京大学、人民大学等高校 BBS；
- 求职状态页面；
- Email。

有时她一天投递几十份简历，同时仍参加部分现场招聘会。

来源：

- 《齐鲁晚报》/ 新浪，2007-03-29，《毕业生网上海投简历“捞”工作》：<https://news.sina.com.cn/c/2007-03-29/003211516786s.shtml>

证据等级：**B，包含同期第一人称**。

### 对页面谱系的意义

这里不能把“招聘平台”孤立出来。

岗位发现路径可能是：

```text
company page
→ professional job board
→ university BBS repost
→ another university BBS
→ email / application form
```

因此新增硬边界：

> **BBS repost ≠ canonical vacancy record**

同一个职位可能被复制、摘要、转发多次；每个页面的日期也不一定代表职位首次发布或仍然有效的日期。

建议记录：

- `canonical_employer_url`（若可确认）；
- `platform_listing_url`；
- `repost_url`；
- `repost_datetime`；
- `source_attribution`；
- `observed_expiry`；
- `confidence_same_vacancy`。

---

## 10. 2007：经认证的电子简历说明“平台身份”可能和制度身份绑定

北京市 2007 年高校毕业生网上双选会允许企业搜索毕业生简历、发送面试通知。

同时系统流程要求：

- 预先认证的学籍信息进入就业信息网；
- 学生激活学籍；
- 根据学校就业推荐表填写电子推荐表；
- 高校审核电子推荐表真实性。

来源：

- 《新京报》/ 新浪，2007-11-07，《高校毕业生首场网上双选会开始》：<https://news.sina.com.cn/c/2007-11-07/012412856610s.shtml>

证据等级：**B：同时代媒体报道**。

这要求 old-web 研究把 candidate profile 再拆层：

```text
account identity
institution-verified student record
self-entered profile fields
institution-reviewed recommendation fields
free-text resume claims
```

必须固定：

> **verified profile ≠ every field independently verified**

以及：

> **platform account identity ≠ public real-name profile**

一个系统可以在后台知道学生是谁，同时对普通 Web 访问者不公开全部身份字段。

---

## 11. 2008：“限时网投”意味着 Web 接口已经可以成为实体招聘会的必经状态机

2008 年《长江日报》报道武汉高校招聘时出现：

- 企业到校园现场宣讲；
- 现场不接受纸简历；
- 应聘者必须登录指定人才网站；
- 只在宣讲结束后的有限时间内接受投递；
- 企业按专业、学校、英语等级、实践经验、薪酬范围等字段快速分类。

其中一个报道案例的申请窗口只有 6 小时。

来源：

- 《长江日报》/ 新浪教育，2008-10-22，《现场不收简历 校园招聘会兴起“限时网投”》：<https://edu.sina.com.cn/l/2008-10-22/1127153829.shtml>

证据等级：**B：同期媒体采访**。

这里至少产生四条旧网证据规则。

### 11.1 `physical event ≠ paper application`

宣讲会是线下发生，并不表示简历收取也是线下。

### 11.2 `listing visible ≠ application window open`

页面今天还能访问，也不能推断当时任意时刻都能投递。

### 11.3 `form fields ≠ neutral metadata`

结构化字段参与快速淘汰和分类，它们本身属于招聘系统行为的一部分。

### 11.4 `deadline text ≠ server acceptance proof`

即使历史页面写“截止 18:00”，仍需区分：

- 浏览器显示；
- 客户端校验；
- server timestamp；
- 提交成功回执；
- 后台记录。

---

## 12. Job-search result page 是一种特别危险的 archive 对象

招聘站搜索页常由：

- query parameters；
- session；
- cookie；
- 地区 / 行业过滤；
- 登录身份；
- 排序；
- 后台索引；
- 数据更新时间；

共同决定。

因此一张搜索结果 capture 只能证明：

> 在特定已知 / 未知查询条件与 capture 时点，archive 得到了这一种结果表示。

不能证明：

- 当天数据库只有这些岗位；
- 排名就是历史用户看到的默认顺序；
- 下一页存在 / 保存完整；
- 已登录用户和匿名用户结果相同；
- 该结果在一小时前或一天后仍一样。

必须固定：

> **search result ≠ full historical corpus**

建议 capture metadata 增加：

```text
query_terms
location_filter
category_filter
sort_order
pagination
login_state
observed_result_count
capture_datetime
known_dynamic_parameters
```

---

## 13. 简历数据库比职位页面更难保存，也更敏感

历史招聘站上的普通简历可能包含：

- 姓名；
- 性别 / 年龄；
- 手机；
- Email；
- 家庭地址；
- 学校；
- 工作经历；
- 照片；
- 薪资期待；
- 求职地点；
- 婚姻等当时常见字段。

即使 archive 偶然保存，也不应为了“完整历史”批量重新索引和公开。

沿用 `docs/METHOD.md` 的隐私最小化原则：

- 优先保存字段 schema；
- 保存平台帮助页和公开规则；
- 普通个人只保留支持 claim 所需的最少信息；
- 不批量建立“旧简历人肉数据库”；
- 不因为旧联系方式今天可能失效就视为无隐私风险。

因此：

> **resume-database invisibility is partly an archive gap and partly a boundary we should preserve deliberately.**

这不是需要“修复”的所有缺失。

---

## 14. Freshness ambiguity：岗位和简历都可能“还在页面上，但现实已经变了”

招聘系统天然有两个易腐对象：

### Vacancy freshness

职位可能已经：

- 招满；
- 暂停；
- 修改要求；
- 延长；
- 被复制到其他站；
- 页面未删除。

### Resume freshness

求职者可能已经：

- 找到工作；
- 改变城市；
- 改变薪资要求；
- 更换联系方式；
- 不再求职；
- 忘记关闭公开简历。

因此必须建立：

> **record survives ≠ labor-market state survives**

这对 archive 特别重要，因为 archive 的职责恰恰是让过期页面继续存在。

一个保存良好的旧招聘页面，其“保存成功”反而更容易诱发“岗位当时一直存在”的误读。

---

## 15. “海投”导致一个新的 historical visibility paradox

网络招聘让求职者一天投出几十份简历成为可能。

但这些事件往往没有公开 URL。

典型链条：

```text
用户登录
→ 点击申请
→ POST / AJAX
→ 后端插入 application record
→ 企业后台队列
→ 无任何回复
```

几十份申请可以真实消耗一个人的一天，却在公开 Web 上留下 **零个可引用页面**。

因此产生：

## application-event invisibility（申请事件不可见性）

公开档案会系统性偏向：

- 招聘公告；
- 企业宣传；
- 成功案例；
- 平台帮助页；
- 公开 BBS 转帖；

而低估：

- 没被看的申请；
- 没回复的申请；
- 登录后状态；
- 失败提交；
- 用户主动撤回；
- 过期后重新投递。

所以：

> **archived opportunity menu ≠ historical application workload**

---

## 16. “无回复”又是另一种不能过度解释的负状态

用户同期自述“投了很多，没有回复”非常珍贵，但仍然只能证明：

> 从用户视角没有观察到回应。

不能直接判断：

- HR 没看；
- 系统自动淘汰；
- 岗位已关闭；
- 邮件发送失败；
- 企业觉得不匹配；
- 回复被垃圾邮件过滤；
- 站内状态更新但用户没查；
- 招聘信息本身已陈旧。

因此建议字段：

```text
user_observed_response = none
system_state = unknown
employer_view_state = unknown
reason = unknown
```

而不是直接写：

```text
employer_ignored = true
```

这一纪律与已有 `negative-state archaeology` 完全一致。

---

## 17. 平台“成功就业人数”必须和因果 claim 分开

历史高校就业站、人才网站和商业招聘平台经常自报：

- 多少人“网上求职成功”；
- 多少岗位；
- 多少简历；
- 多少会员；
- 多少点击。

这些数字可以证明：

- 平台当时这样统计 / 宣称；
- 系统不是纯演示页面；
- 某种规模的活动存在。

但不能自动证明：

- 成功完全由平台造成；
- 人没有同时通过现场 / 熟人 / 学校渠道接触该单位；
- “成功”口径等于实际到岗；
- 会员数等于活跃求职人数；
- 页面点击人次等于独立用户。

因此：

> **platform-attributed hire ≠ causal platform hire**

以及：

> **pageviews ≠ persons**

---

## 18. 在线发现和线下执行必须分别建模

2003 年多条同期材料都显示，网上招聘和现场招聘长期共存。

到 2008 年甚至出现：

```text
现场宣讲
→ 强制网投
→ 网上筛选
→ 次日笔试
→ 后日面试
```

所以招聘流程不能编码为简单：

```text
online / offline
```

应使用 step-level channel：

| step | possible channel |
|---|---|
| discovery | BBS / job board / newspaper / fair |
| company presentation | physical / webcast |
| application | Web form / Email / paper |
| screening | server / HR backend |
| notification | site / Email / SMS / phone |
| test | Web / physical |
| interview | phone / physical / video |
| agreement | physical / institutional system |
| arrival | physical |

硬边界：

> **online discovery ≠ end-to-end online recruitment**

---

## 19. 建议的 evidence schema 扩展

以后如果进入结构化数据，可以为 employment-web artifact 增加：

```yaml
artifact_type: vacancy | resume_schema | search_result | application_form | help_page | interview_notice | forum_repost
platform:
original_url:
capture_url:
capture_datetime:
page_internal_datetime:
employer_name:
job_title:
location:
posting_datetime:
observed_expiry:
application_deadline:
login_required:
resume_required:
resume_visibility:
verified_identity_layer:
searchable_by_employer:
application_channel:
notification_channel:
structured_filter_fields: []
dynamic_query_state:
server_side_state_visible:
canonical_source_known:
repost_of:
outcome_visible:
evidence_grade:
confidence:
privacy_notes:
missing_layers: []
```

特别注意：`outcome_visible` 默认应是 `false / unknown`，不能因为页面是“招聘成功案例”就反推普通 listing 的 outcome。

---

## 20. 最低 hard boundaries

以后处理招聘旧网对象，默认检查以下边界：

```text
job listing visible
≠ position open

position open
≠ applications accepted now

search result captured
≠ complete vacancy corpus

resume created
≠ resume public

resume public
≠ employer-searchable under all queries

resume searchable
≠ resume viewed

application submitted
≠ application delivered to a human

application delivered
≠ shortlisted

interview invitation sent
≠ invitation received

invitation received
≠ interview attended

interview attended
≠ offer

offer
≠ hire

online discovery
≠ online-only recruitment

verified student record
≠ every resume claim verified

BBS repost
≠ canonical vacancy

platform-reported success
≠ independently audited causal outcome

archived page
≠ historical live service state
```

---

## 21. 已证实 / 高概率 / 不知道

### 已证实

- 1999 年中文 Internet 已有求职招聘内容，但同期媒体认为信息仍不够丰富；
- 2001 年南京毕业生就业系统已经把网上招聘、网上求职与主管部门网上审批连接；
- 2003 年高校就业站已经存在电子简历数据库、招聘中心、求职中心、论坛和在线洽谈等复合功能；
- 2003 年线上双选在突发公共卫生事件中承担了更多招聘功能，同时受到服务器并发能力限制；
- 2003 年同期求职者和企业都已经记录大量投递 / 大量简历造成的无回复与筛选负担；
- 2007 年普通毕业生可以同时通过人才网站和多校 BBS 发现招聘信息并批量投递；
- 2007 年高校就业系统已经把电子简历与学籍 / 推荐表核验连接；
- 2008 年部分校园招聘已经要求在有限时间窗口内强制网投，并利用结构字段快速分类简历。

### 高概率

- 大量真正的 application event 从未拥有公开 URL，因此系统性低估；
- 登录后的 candidate / employer backend 比公开职位页更容易从 Web archive 消失；
- Email、短信、电话和现场面试造成强烈 off-platform outcome gap；
- 动态职位搜索和简历检索结果很难靠少数 capture 重建完整历史数据库；
- 招聘页面的存续时间通常长于现实岗位的有效时间。

### 不知道

- 关键招聘平台 1999—2005 每日职位数据库的完整快照；
- 大多数历史电子简历真实公开级别；
- 某份简历被多少企业查询、打开和筛选；
- 大量“无回复”分别对应哪种后台原因；
- 早期 BBS 招聘转载中，多少在转载时已经过期；
- 历史网站宣称的“求职成功”具体使用什么口径；
- 多少跨城求职真正由 Web 的远程发现首先触发。

---

## 22. 后见之明风险

### 风险 A：把职位页看成静态文献

招聘页是高度时效性的交易对象，不是普通文章。

### 风险 B：把现代搜索框经验套回早期网站

早期站点的检索字段、索引更新周期、分页、浏览器兼容和登录限制可能完全不同。

### 风险 C：从页面布局推断后台能力

一个 HTML 表单不能证明 server-side 数据库、过滤和邮件通知都正常工作。

### 风险 D：把“网上双选”写成纯线上生活

很多链条最终仍回到现场笔试、面试、签约和行政流程。

### 风险 E：把大学毕业生经验外推给所有劳动者

早期网络招聘明显更容易进入高校、IT / 通信行业和城市知识劳动者生活；其他劳动者可能长期主要依赖职介所、劳务市场、报纸、熟人、电话和现场招工。

### 风险 F：为了考古完整而重新暴露普通人的历史简历

不做。

---

## 23. 为什么这改变中文旧网的研究方式

招聘旧网特别适合提醒本仓：

> **old web was not only pages people read; it increasingly became interfaces through which people tried to alter their offline lives.**

一个人可以在网页上看见另一座城市的岗位、把自己的职业档案放进数据库、收到面试通知，然后搬家去那里生活。

但最关键的“生活改变”常常发生在 archive 边界外：

```text
search
→ click
→ submit
→ hidden database
→ phone call
→ train
→ interview room
→ contract
→ new city
```

如果只研究幸存 HTML，会系统性高估“看见”，低估“执行”，也会把大量失败和沉默从历史里删除。

因此本文新增的核心 archive principle 是：

> **preserve the distinction between opportunity visibility and reciprocal attention.**

中文旧网越能让普通人看到更多远方机会，研究者越需要追问：

- 对方有没有看到他；
- 他有没有收到回应；
- 这条线上联系有没有变成一次真实的线下迁移和工作。

---

## 24. 与 `how-people-lived` 的交叉链接

对应生活史专题：

- `topics/job-market-addressability-search-radius-and-attention-bottlenecks-china-1984-2024.zh-CN.md`

生活史仓负责：

- 1980 年代人才交流和就业制度前史；
- 普通人的工作搜索半径；
- 2005—2012 / 2015—2019 / 2023—2026 时间感比较；
- 美国 Monster 等海外比较；
- 求职如何连接迁移、住房和生命历程。

本仓只负责：

- 1995—2015 中文 Web / BBS / 招聘平台 artifact；
- 页面、数据库、搜索、账号、简历和状态边界；
- archive gap；
- 浏览器 / 动态查询 / 登录条件；
- 隐私和 provenance。

---

## 25. 下一步最值得寻找的原始 artifact

按优先级：

1. **1999—2004 中文人才网站原始帮助页**：职位有效期、简历公开级别、企业搜索规则、Email 通知；
2. **同一职位两个以上历史时点**：发布 → 更新 → 已招满 / 过期，建立真实 vacancy lifecycle；
3. **同一 BBS 招聘帖及后续“已找到人 / 截止 / 撤帖”**，验证转载与状态变化；
4. **旧招聘站搜索结果 + 详情页组合**，记录 query / pagination / ranking，不把结果页当完整 corpus；
5. **公开且非敏感的平台 demo / 手册中的雇主后台**，确认企业怎样检索和过滤简历；
6. **同期用户自述完整链**：网投 → 没回复 / 收到 Email → 电话 → 面试 → 最终结果；
7. **浏览器条件**：早期招聘表单是否有 IE-only JavaScript、frame、编码、ActiveX / 上传控件问题。

如果能找到第 2 或第 6 类连续证据，下一轮就能从“招聘系统提供了哪些接口”真正推进到**一条历史求职状态怎样在 Web 与现实之间来回穿越**。