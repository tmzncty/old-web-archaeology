# 中文旧网远程教育、学习平台、课程作业与学生状态缺口（1999–2015）

## 0. Scope

本说明只处理约 1999–2015 中文 Web 中与现代远程教育 / 网络教育有关的以下对象：

- 网络教育学院与招生页面；
- 校外学习中心 / 教学点信息；
- 学生账号与登录入口；
- 选课、费用、课程开通；
- 课程资源与客户端依赖；
- 论坛、答疑、消息与学习安排；
- 作业发布、提交、补交、反馈；
- 考试预约、成绩查询和学籍状态；
- demo / production 平台状态；
- 当前存活机构页面与历史原页面之间的证据边界。

它**不是**中国成人教育通史，也不把本仓 scope 扩展到 1979 年广播电视大学、1981 年自学考试或 2016 年以后移动学习。更长时段的普通人生活史、互联网前史、海外比较与 2023–2026 青年夜校写在：

- `tmzncty/how-people-lived/topics/education-reentry-adult-continuing-learning-and-recursive-life-courses-china-1979-2026.zh-CN.md`

它也不重复：

- `EDUCATION_CREDENTIAL_QUERY_REGISTRY_VERIFICATION_AND_RESULT_STATE_GAPS_2001_2015.md`：后者研究学历证书、电子注册与在线验证；
- 招生/考试相关 state-gap notes：本说明关注**已经进入或正在进入远程学习体系以后，学生怎样取得课程与完成学习**；
- 通用论坛/社区研究：这里的论坛只在它作为教学平台的课程/答疑组件时讨论。

核心问题是：

> **一个 2005 年网页写着“网络教育”“学习平台”“网上作业”，究竟能证明学生的哪一层学习状态？从招生、缴费、登录到真正获得学分，中间有哪些不能凭静态页面跨越的状态？**

---

## 1. Why distance education is a useful old-Web object

网络教育页面不是普通内容页。

一个新闻页如果成功回放，主要问题通常是：HTML、CSS、图片、脚本、字符集和链接是否保存。

一个网络教育学生平台还依赖：

- 真实学生身份；
- 学籍；
- 费用状态；
- 选课记录；
- 课程授权；
- 登录/session；
- 教材与线下学习中心；
- 课件格式和插件；
- 作业截止时间；
- 服务端提交；
- 教师批改；
- 考试资格和预约；
- 线下考试 / 身份核验；
- 成绩入账；
- 私人学生数据库。

因此 archive 最容易保存的是：

```text
招生介绍
公告
帮助文字
某个公开 demo 说明
课程宣传
```

最难保存的是：

```text
一个真实学生在某一秒的登录态
实际已选课程
缴费是否到账
私有作业正文
提交 transaction
教师批改状态
真实成绩
学分入账
```

这形成一种结构性保存偏差：

**public-learning-shell / private-student-state asymmetry（公开学习壳 / 私人学生状态不对称）**。

---

## 2. Minimum state model

至少拆成：

```text
real person wants to study
→ program actually exists
→ program is authorized / admitting
→ local learning center or enrollment route exists
→ person discovers the route
→ application is submitted
→ prior qualification / identity is checked
→ admission state is created
→ fees are due
→ payment is sent
→ institution confirms payment
→ student record exists
→ credentials are generated / delivered
→ student can authenticate
→ login session is established
→ course selection is available
→ course is selected / assigned
→ course fee is satisfied if required
→ course entitlement is opened
→ course appears in account
→ content can actually load in historical client environment
→ schedule / forum / guidance becomes visible
→ assignment is released
→ student prepares work
→ upload / submit request is sent
→ server acknowledges submission
→ submission is durably stored
→ instructor / grader receives it
→ feedback / grade is produced
→ grade is posted to student state
→ exam may be booked
→ identity / attendance / exam conditions are satisfied
→ exam result is recorded
→ credits accumulate
→ graduation requirements are satisfied
→ credential is issued / registered
```

任何历史叙述都不能无证据地跨越这些节点。

固定以下硬规则：

```text
program page exists
≠ program was still admitting

student account exists
≠ credentials reached the student

credentials exist
≠ login succeeded

login succeeds
≠ all course content loads

course listed
≠ student is enrolled in it

course selected
≠ fee confirmed

fee sent
≠ institution confirmed payment

payment confirmed
≠ course entitlement already opened

course page renders
≠ historical media/plugin plays

assignment page exists
≠ student saw it

student clicked submit
≠ server persisted the assignment

submission persisted
≠ instructor graded it

grade shown
≠ graduation conditions completed

online education
≠ no offline dependency
```

---

## 3. 1999–2008: existence and scale are supported, but not a single universal platform architecture

教育部 2008 年总结称，自 1999 年起分 5 批批准 68 所普通高校和中央广播电视大学开展现代远程教育试点。截至 2007 年底，学历教育累计注册学生 670 万；中央电大开放教育学生 458 万；在职人员占 86.5%；普通高校及公共服务体系有 5935 个校外学习中心，中央电大有 3292 个教学点。

Sources:

- Ministry of Education, 2008, `积极推进高校现代远程教育试点工作`:  
  <https://www.moe.gov.cn/jyb_xwfb/xw_zt/moe_357/s3580/moe_2448/moe_2450/moe_2456/tnull_39524.html>
- Ministry of Education, 2008, `发展远程教育和继续教育，建设全民学习、终身学习的学习型社会`:  
  <https://www.moe.gov.cn/jyb_xwfb/xw_zt/moe_357/s3580/moe_2448/moe_2450/moe_2456/tnull_40508.html>

Evidence class: **A — contemporaneous official summary/statistics**.

### What this proves

可以安全写：

- 到 2007 年，中国高校现代远程教育已经是大规模制度性系统；
- 在职学生占该系统学生的很大比例；
- “网络教育”仍依赖大量地方学习中心/教学点，不是纯粹 browser-only 服务。

不能写：

- 68 所试点高校使用同一个软件栈；
- 每个学生都从家庭宽带访问；
- 所有课程都完全在线；
- 学习中心只是招生点而不承担线下教学/考试；
- 一个平台截图足以代表全国网络教育。

### New gap: system existence / local execution gap

```text
national distance-education system exists
≠
a given worker in a given city has a usable local learning route
```

一个学生还可能受：当地学习中心、招生专业、网络条件、纸教材、考试地点和工作时间限制。

---

## 4. 2005 Beiwaionline: course access was explicitly conditional on payment state

北外网络教育学院今天仍保存带 2005 年发布时间的公开公告。`2005春季学期选课缴费须知` 描述了清晰链路：

```text
student logs into learning platform
→ 学籍管理
→ 年度课程申请
→ 选取课程
→ 费用查询 / 所有费用清单
→ remittance/payment
→ institution receives payment
→ courseware/resources are opened
```

公告还明确写到：在课件开通前，学生先利用课本学习，并与学习中心确认面授辅导；若未在截止日前汇款，学习平台不能如期开通并影响学业进程。

Source:

- Beiwaionline, 2005-01-31, `2005春季学期选课缴费须知`:  
  <https://www.beiwaionline.com/aboutbeiwai/gonggao/webinfo/2005/01/1272264151168775.htm>

Evidence class: **A/B-near-primary — surviving contemporaneous institutional page**.

### New gap: payment-sent / payment-confirmed / entitlement-open

必须至少区分：

```text
student sends payment
→ bank/postal channel processes payment
→ institution receives / reconciles payment
→ student financial state changes
→ course entitlement job runs
→ learning resources become available
```

因此：

```text
remittance receipt
≠ platform entitlement
```

也不能因为某个学生账号能登录，就推断该学期课程都已经开通。

### Hybrid learning evidence

同一公告明确保留：

- 纸质课本；
- 学习中心；
- 面授辅导。

所以本仓以后遇到“网络教育”必须先问：

> Web 是全部教学系统，还是仅承担一部分课程、教务、沟通与状态显示？

`online` 不是一个足以描述整个学习行为的标签。

---

## 5. 2005 forum and assignment deadlines: public notices survive, actual reading/submission states do not

北外网院 2005 年 3 月公告写到：

- “新生三周拓展训练论坛”将在规定日期关闭；
- 之后不同层次学生进入不同课程论坛；
- 两项作业分别有首次提交截止与补交截止日期；
- 问卷发布在学习平台首页公告中。

Source:

- Beiwaionline, 2005-03-15, `2005年春季“拓展后问卷”发布通知`:  
  <https://www.beiwaionline.com/aboutbeiwai/gonggao/webinfo/2005/03/1272264151063205.htm>

Evidence class: **A/B-near-primary contemporaneous institutional page**.

### New gap: announcement / encounter gap

该页面能证明机构**发布过**某个截止时间。

它不能证明：

- 某个真实学生在截止前登录；
- 学生看到首页公告；
- forum link 当时加载成功；
- 学生阅读了某帖；
- 学生知道论坛会关闭。

因此：

> **announcement published ≠ student encountered announcement**

这和普通旧网论坛的 lurker invisibility 类似，但这里后果可能直接影响成绩。

### New gap: submit / persist / grade

如果 archive 保存一个“作业提交”按钮或帮助页，仍然只能说明交互入口存在。

完整链路应是：

```text
assignment released
→ student sees it
→ file/form prepared
→ submit clicked
→ HTTP request reaches server
→ validation succeeds
→ database/file commit
→ receipt/state returned
→ grader receives
→ feedback/grade recorded
```

历史 archive 通常看不到这条链的大部分私人 transaction。

---

## 6. 2006: production platform and demo platform must be treated as different historical objects

2006 年 12 月北外网院公开邀请学生试用新版平台，给出 demo URL：

`http://demo.beiwaionline.com/newplat`

公告明确说明：

- 试营业时间仅 2006-12-15 至 2006-12-17；
- 用现有用户名/密码登录；
- 登录后看到的信息全部是**模拟信息**，与真实信息不符；
- 正式启用时会重新录入真实信息；
- 平台包含“我的日程”“我的书房”“我要交流”等组件；
- 配套“选课缴费”“成绩查询”的 Flash 动画；
- 另有 VOB/VOC 平台讲解与论坛交流。

Source:

- Beiwaionline, 2006-12-12, `欢迎大家参与新学习平台系统体验活动！`:  
  <https://www.beiwaionline.com/aboutbeiwai/gonggao/webinfo/2006/12/1272264150034298.htm>

Evidence class: **A/B-near-primary contemporaneous institutional announcement**.

### Hard rule: demo state ≠ production state

这是一条可以直接泛化到整个旧网仓的方法规则：

```text
demo account
≠ production account

demo student information
≠ real student database

demo grade
≠ actual grade

demo course enrollment
≠ actual entitlement
```

如果未来真的找到该 demo 的历史 capture，必须在 evidence metadata 明确写：

```yaml
platform_state: demo
student_data: simulated_by_official_statement
production_equivalence: unknown
```

不能因为 demo 看起来完整，就把它当作真实学生平台快照。

---

## 7. Flash/VOB/VOC evidence: client dependency exists, exact historical client remains unknown

2006 公告明确提到 Flash 动画和 VOB/VOC 节目，因此可以安全写：

> 学生支持材料中至少存在依赖当时浏览器媒体能力/插件生态的组件。

但本轮没有取得：

- 原 Flash 文件；
- SWF version；
- ActionScript；
- 当时推荐 Flash Player 版本；
- IE/Netscape/Firefox 支持矩阵；
- VOB/VOC 的底层技术说明；
- 原始 JS/browser-sniffing 代码。

因此不得从“有 Flash 动画”跳到“只能 IE6 使用”。

### New gap: page-render / pedagogical-resource gap

一个 modern browser 今天即使能显示公告 HTML，也不证明：

- 2006 的 Flash 教程可以播放；
- 实际课件加载；
- 音视频能解码；
- 原 forum/session 仍可运行。

这类页面特别适合 M3 浏览环境实验，但在拿到历史 artifact 前不应先做漂亮 reconstruction。

---

## 8. 2006 course selection notice: temporal state matters

`2006秋季学期选课缴费须知` 记录：

- 选课缴费窗口为 8 月 1 日至 8 月 27 日；
- 特定年级学生才需要自己选取课程；
- 新生课程由学院统一设置；
- 学费收到后课程资源才开通；
- 曾延修或休学、转入其他年级者要按对应规则重新办理。

Source:

- Beiwaionline, 2006-07-26:  
  <https://www.beiwaionline.com/aboutbeiwai/gonggao/webinfo/2006/07/1272264150232851.htm>

Evidence class: **A/B-near-primary contemporaneous institutional page**.

### New gap: interface existence / temporal permission gap

同一个选课页面可能在不同日期、不同年级、不同学籍状态下产生完全不同的能力。

```text
course-selection interface exists
≠ this student can select now
```

至少应记录：

```text
academic_term
selection_window
student_cohort
new_or_continuing
active/suspended/extended status
fee state
```

旧网截图如果没有这些上下文，很容易把“一个按钮”误写成“所有学生一直拥有这个功能”。

---

## 9. State stack for a historical learning-platform capture

如果未来取得真实 2005–2010 学习平台 capture，最小研究单位不应只写“北外网院主页”。建议拆成：

### Platform level

- public institutional site;
- enrollment portal;
- production learning platform;
- demo/test platform;
- forum/community host;
- course-content host/CDN if separate;
- payment information flow;
- exam/grade service if separate.

### Account state

- applicant;
- admitted student;
- fee unpaid / sent / confirmed;
- active student;
- suspended / extended / graduated;
- credentials issued;
- login enabled/disabled.

### Course state

- catalogued;
- assigned;
- selected;
- payable;
- payment reconciled;
- entitlement opened;
- currently active;
- assignment due;
- exam eligible;
- completed.

### Artifact state

- announcement;
- help page;
- screenshot;
- login shell;
- authenticated HTML;
- course asset;
- forum page;
- assignment form;
- grade view;
- demo content;
- reconstructed display.

不要把这些层级合成一个“网站”。

---

## 10. Historical first-person evidence belongs next to platform evidence, but cannot replace it

2009 年《北京考试报》报道自考在职学习者时，同一篇材料里同时出现：

- 一名只剩一门课的学生找到工作后利用业余时间复习，最终通过；
- 一名学生进入销售工作后因加班拖了三年；
- 另有学生因工作忙、出差而反复错过/未通过考试。

Source:

- Beijing Exam newspaper / Sina, 2009-02-21:  
  <https://edu.sina.com.cn/zikao/2009-02-21/1256188120.shtml>

Evidence class: **B — contemporaneous reported first-person**.

这类材料适合证明：

- “制度允许灵活学习”与“普通人实际能完成”不同；
- 工作时钟会直接改变教育路径。

但它不能证明某个网络教育平台的 DOM、字段、session 或数据库行为。

因此 old-Web case 应把：

```text
technical artifact evidence
```

和：

```text
lived-use evidence
```

交叉，而不是互相替代。

---

## 11. Local learning centers are part of the technical-social stack

教育部 2008 年统计同时显示数千个校外学习中心/电大教学点。这一点对 Web 考古非常重要：

> **页面里的“在线学习”不能被理解为学生与一台中央服务器之间的纯二元关系。**

现实拓扑可能是：

```text
university headquarters
→ public website
→ learning platform
→ local learning center
→ paper materials / face-to-face support
→ student home/work/shared terminal
→ centralized examination
```

因此一个历史平台即使完整回放，也只恢复了整个远程教育系统的一部分。

### New gap: platform completeness / service completeness

```text
Web artifact complete
≠ historical service complete
```

这条规则尤其适用于：

- 医院预约；
- 铁路购票；
- 银行；
- 教育；
- 政务查询。

旧网不是现实制度的全集，而常常只是 control surface。

---

## 12. Search / enrollment / learning / credential must remain separate

对一个普通成人来说：

```text
finds program on web
→ applies
→ becomes student
→ learns
→ passes courses
→ obtains credential
```

是六个不同阶段。

现有仓库已有学历验证 state-gap note，因此本说明只到“学分 / 毕业条件形成”，最终证书是否可验证仍交给：

- `EDUCATION_CREDENTIAL_QUERY_REGISTRY_VERIFICATION_AND_RESULT_STATE_GAPS_2001_2015.md`

这条边界很重要，因为：

> **一个 Web 学习平台可以真实存在、学生也真实学习过，但最终学历/证书是否形成和可验证仍是另一套制度状态。**

---

## 13. Archive preservation bias

### What tends to survive

- institution homepage;
- public news/announcements;
- enrollment guides;
- support email/phone;
- screenshots in manuals/news;
- demo descriptions;
- static course lists;
- policy pages.

### What tends not to survive publicly

- authenticated dashboard;
- real names/student IDs;
- fee reconciliation state;
- private forum participation;
- submitted homework;
- teacher feedback;
- exam reservations;
- grade history;
- session cookies;
- private database state.

部分“缺失”不是 archive 失败，而是**隐私和认证系统本来就应该阻止公共抓取**。

这可称为：

**privacy-preserving educational archive asymmetry（隐私保护造成的教育档案不对称）**。

研究者不应为了补齐它而：

- 尝试历史学生账号；
- 搜索泄露密码；
- 使用泄露学生数据库；
- 重新公开私人作业、成绩、联系方式。

---

## 14. Current surviving page / historical original gap

本轮最有价值的材料来自 `beiwaionline.com` 当前仍可访问、正文标注 2005/2006 发布时间的机构页面。

这些页面可以作为：

- 当时公告文本的高价值近原始/机构证据；
- 历史 URL/功能/术语 locator；
- 搜索 Wayback/Common Crawl 的入口。

但当前存活页不自动等于：

```text
2005 server response
2005 DOM
2005 CSS
2005 charset
2005 navigation shell
2005 JavaScript
2005 cookies/session
```

站点可能经历过 CMS 迁移、URL rewrite、模板替换、编码统一和数据库导入。

所以固定：

> **historical publication date on a surviving page ≠ verified historical memento**

---

## 15. Archive search result of this run

本轮已获得一个非常具体的 historical-original candidate：

- `http://demo.beiwaionline.com/newplat`
- 官方公告说其有效期为 2006-12-15 至 2006-12-17；
- 官方公告明确说其中数据是模拟信息。

但本轮**没有取得并实际打开一份达到本仓 METHOD M1 标准的 1999–2010 中文网络教育学习平台 Wayback/WARC memento**。

因此以下均保持 `unknown`：

- demo URL 是否被公开档案实际 capture；
- production platform 的真实历史 original URL；
- 2005–2006 DOM / frameset / charset；
- login form action；
- cookie/session scheme；
- password recovery flow；
- course resource URL pattern；
- assignment POST endpoint；
- grade-query endpoint；
- precise Flash Player/browser requirements；
- server-side persistence semantics；
- database schema。

按照 `docs/METHOD.md`：

> **candidate locator 不是 verified capture。**

因此本说明仍是 state-gap research note，不勾选 M1 完整案例。

---

## 16. Suggested evidence record if a verified capture is found later

```yaml
subject: distance-learning-platform
platform_operator: "..."
platform_state: production | demo | unknown
original_url: "..."
archive_source: internet-archive | common-crawl | other
capture_url: "..."
capture_datetime: "..."
accessed_at: "..."
http_replay_state: "..."
page_type: login | dashboard | announcement | course | assignment | forum | grade | demo
historical_charset: "... | unknown"
browser_assumption: "... | unknown"
plugin_dependency:
  flash: true | false | unknown
  java: true | false | unknown
student_state_real_or_simulated: real | simulated | unknown
authenticated_state: public | authenticated | unknown
subresources_complete: true | false | partial | unknown
evidence_grade: A | B | C | D
confidence: high | medium | low
privacy_action: metadata-only | redacted | public-safe
notes: "..."
```

如果是 demo，`student_state_real_or_simulated` 绝不能省略。

---

## 17. Browser / encoding experiment questions

如果未来得到足够 artifact，M3 最值得验证：

1. 2005/2006 页面真实 charset 是什么；
2. 是否使用 frames/iframes；
3. 登录和课程资源是否 browser-sniffed；
4. Flash 教程在当时哪类浏览器/插件可用；
5. modern Chromium replay 丢失哪些交互；
6. archive URL rewriting 是否破坏相对路径；
7. session/login shell 是否被误存为“课程页面”；
8. demo 和 production 是否共享模板/host/path。

在得到原始 artifact 前，不先猜答案。

---

## 18. Claims table

| Claim | Evidence | Grade | Confidence | Boundary |
|---|---|---:|---:|---|
| 1999 后高校现代远程教育形成大规模制度系统 | 教育部 2008 总结 | A | high | 不证明单一统一技术栈 |
| 2007 年系统内在职人员占比很高 | 教育部 2008 | A | high | 仅限该统计口径 |
| 2005 北外网院学生需要登录平台选课/查费用，缴费确认后开课程资源 | 同期机构公告 | A/B | high | 当前存活页非 verified historical memento |
| 2005 平台具有课程论坛、首页公告和作业截止/补交机制 | 同期机构公告 | A/B | high | 不证明某学生实际阅读/提交 |
| 2006 存在为期三天的新版 demo，且模拟数据与真实学生信息明确区分 | 同期机构公告 | A/B | high | demo 本体未取得 capture |
| 2006 平台使用 Flash 教程及 VOB/VOC 支持内容 | 同期机构公告 | A/B | high | 精确客户端/协议 unknown |
| 网络教育仍依赖学习中心/纸教材/面授 | 教育部统计 + 北外公告 | A/B | high | 各校比例不同 |
| 真实作业提交、成绩、学生 session 被公共 archive 系统性低保存 | 状态模型/隐私机制 | D | medium-high | 需未来样本量化 |

---

## 19. What is known / probable / unknown

### 已证实

- 2000s 中期中文网络教育平台已真实承担选课、费用、课程开通、论坛、作业截止等学生事务；
- 至少北外网院 2005–2006 的公开制度文本把 Web 与纸教材、学习中心、面授并置；
- 2006 公开 demo 明确区分模拟数据与真实学生数据；
- Flash 等客户端资源确实进入过学生支持栈；
- 学生能否学习与费用、学籍、时间窗口等状态有关。

### 高概率但仍需 capture / technical evidence

- production platform 有独立于公开官网的认证/session/学生数据库；
- 部分课程资源存在明显的历史浏览器/插件复现问题；
- CMS 迁移已经改变当前页面模板，与 2005 原始响应不同。

这些都不能在拿到原 artifact 前提升为 A 级技术事实。

### 不知道

- 2005/2006 production URL；
- 精确 DOM、charset 和浏览器要求；
- demo capture 是否幸存；
- assignment/grade backend 语义；
- 真实用户端设备分布；
- 在家、单位、学习中心、网吧接入比例；
- archive 对该类认证平台的保存率。

---

## 20. How this changes old-Web archaeology

这类对象迫使旧网研究从：

> “这个网页当年长什么样？”

继续推进到：

> **“这个网页当年只是一个信息页面，还是一个能改变真实学生制度状态的 control surface？它显示出来的状态，和后台真实状态之间还隔着什么？”**

网络教育是非常好的交叉案例，因为同一 browser window 里可以同时出现：

- 信息；
- 身份；
- 费用；
- 授权；
- 教学资源；
- 社区；
- 截止时间；
- 私人提交；
- 成绩。

而公共 archive 恰恰会系统性地只保存其中最公开、最静态的一层。

---

## 21. Next concrete tasks

优先级：

1. 对 `demo.beiwaionline.com/newplat` 做 Wayback CDX / Memento locator 调查并**实际打开**任何命中；
2. 从 2005–2006 北外公开公告继续提取 production platform 的 host/path 线索；
3. 查 Common Crawl 是否保存 `demo.beiwaionline.com` 或早期 learning-platform 子域；
4. 找同期学生教程/截图，交叉核对菜单名、浏览器、插件和 URL；
5. 若拿到 ≥2 时点 + ≥2 evidence family，再考虑升级为正式 case；
6. 对任何真实学生姓名、成绩、作业和账号字段只做最小必要描述，不复制私人内容。

---

## 22. Research saturation status

本轮新增了此前旧网仓未单独建模的 **authenticated learning-platform state**：payment-confirmed/course-entitlement、announcement/encounter、assignment submit/persist/grade、demo/production、page-render/pedagogical-resource、temporal permission 以及 public-shell/private-student-state archive asymmetry。

因此不是无新增轮次，不满足阶段 closure 条件。
