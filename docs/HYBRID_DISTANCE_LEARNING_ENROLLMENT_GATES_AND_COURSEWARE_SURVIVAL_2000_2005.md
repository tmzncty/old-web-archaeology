# HYBRID_DISTANCE_LEARNING_ENROLLMENT_GATES_AND_COURSEWARE_SURVIVAL_2000_2005.md

## 目的与 scope

本笔记研究 **2000–2005 中文 Web 上的网络教育 / 现代远程教育 artifacts**。重点不是写一部“中国远程教育史”，而是回答旧网考古中的一个证据问题：

> 今天还能打开一张“网络大学”招生页、课程页、学生征文或公告时，我们究竟保存了当年的哪一层学习过程？

配套生活史专题：

- <https://github.com/tmzncty/how-people-lived/blob/main/topics/study-without-leaving-adulthood-education-reentry-and-hybrid-distance-learning-china-1979-2005.zh-CN.md>

本仓仍保持约 **1995–2015 中文互联网**的主 scope。1979–1990s 的广播电视大学、函授、夜大学和海外 Open University 比较只放在配套生活史专题；本文件仅在需要解释 2000s 网络教育继承了哪些非 Web 环节时把它们作为前史边界。

本笔记建立五个主要对象：

- **hybrid learning stack**：Web 与纸、光盘、磁带、面授、学习中心、线下考试共同组成的学习系统；
- **enrollment gate**：只有正式注册/登录后才能进入的课程、论坛、作业、成绩和进度状态；
- **courseware survival gap**：公开招生/宣传页比登录后课程运行状态更容易长期存活；
- **learner-voice curation gap**：平台公开展示的优秀学员/征文是同时代第一人称，但经过制度选择；
- **digital scheduling / physical execution**：报名、预约、查询可以在线，考试、面授和部分材料流转仍在物理世界完成。

---

## 1. 第一条硬规则：network education ≠ web-only education

2005 年北外网院当前仍可访问的一组历史公告显示，所谓“网络教育”至少可以同时包括：

- 网站和登录后的学习平台；
- 网络课程资源；
- 课程论坛；
- 在线作业；
- 实时/录播式 VOB/VOC 助学活动；
- 纸质文字教材；
- 录音磁带；
- CD-ROM 辅导课件；
- 面授辅导；
- 校外学习中心；
- 物理考场中的笔试、口试；
- 教材订购与物流。

来源：

- 北外网院，2005-05-10，《新版辅导课件又有新产品！》：<https://www.beiwaionline.com/aboutbeiwai/gonggao/webinfo/2005/05/1272264150991114.htm>
- 北外网院，2005-08-12，《2005年秋季学期教材订购提醒》：<https://www.beiwaionline.com/aboutbeiwai/gonggao/webinfo/2005/08/1272264150793292.htm>
- 北外网院，2004-07-22，《北京地区04秋新生学前讲座开讲》：<https://www.beiwaionline.com/aboutbeiwai/news/webinfo/2004/07/1272264153685194.htm>
- 北外网院，2004-01-09，课程终结考试报道：<https://www.beiwaionline.com/aboutbeiwai/news/webinfo/2004/01/1272264153859813.htm>

证据性质：**A/B-near-primary — surviving first-party historical pages carrying internal 2004–2005 publication dates**。这些 URL 当前由学校域名返回历史正文，可以证明“当前 surviving page 包含这些同期制度描述”；如果没有 WARC/历史 capture，则不能声称当前 HTML、CSS、导航和资源结构就是 2004–2005 原始字节级形态。

因此固定：

> **network education ≠ web-only education**

以及：

> **archived educational website ≠ archived educational system**。

研究单位必须从单一 `website` 扩展到跨媒介学习栈。

---

## 2. 建议对象模型：不要把“网院页面”当成一个层级

至少拆分：

```yaml
institution
program
public_site
admissions_page
learning_center
learner_account
student_record
course
courseware_package
learning_platform
forum
assignment
assignment_submission
live_session
recorded_session
study_record
exam_reservation
physical_exam
score_record
credential_record
printed_textbook
cassette_or_audio_media
cdrom_courseware
public_student_story
capture
claim
```

### 关键区别

`institution` 可以长期存在，但 `learning_platform` 可以更换。

`course` 可以长期存在，但每一学期的：

- 课件版本；
- 作业；
- 论坛；
- 直播活动；
- 考试；
- 学生进度

都可能是不同对象。

同一个学生的 `learner_account` 也不能与 `student_record`、`credential_record` 合并：

- 平台账号存在不等于学籍当前有效；
- 学籍有效不等于本学期活跃；
- 活跃不等于课程完成；
- 课程完成不等于毕业；
- 毕业不等于取得某一学位。

---

## 3. 第二条硬规则：public page ≠ enrolled learning environment

网络教育最容易被今天搜索引擎发现的通常是：

- 招生简章；
- 学院新闻；
- 对外咨询；
- 项目介绍；
- 学生宣传文章；
- 公开公告。

但真正日常学习常发生在：

```text
登录
→ 我的课程
→ 单元课件
→ 作业
→ 论坛
→ 学习记录
→ 成绩 / 考试预约
```

这组状态通常需要：

- 账号；
- 密码；
- 学籍或课程权限；
- 有效 session/cookie；
- 当时数据库；
- 有时还需要特定插件、媒体播放器或脚本。

因此：

> **public recruitment artifact ≠ enrolled student artifact**。

### 建议字段

```yaml
access_gate:
  public_access: true | false | unknown
  account_required: true | false | unknown
  enrollment_required: true | false | unknown
  course_registration_required: true | false | unknown
  session_required: true | false | unknown
  historical_credentials_available: true | false | unknown
  archive_replay_auth_possible: true | false | unknown
  gate_evidence:
```

搜索引擎能索引到学院新闻，并不能证明历史课程论坛或个人学习记录也公开可索引。

---

## 4. 第三条硬规则：portal account ≠ active learner

北外网院 2004 年新生讲座已经讲解：

- 在线提交作业；
- 学习记录卡；
- 成绩构成；
- 课程论坛；
- 助学活动。

来源：

- <https://www.beiwaionline.com/aboutbeiwai/news/webinfo/2004/07/1272264153685194.htm>

这说明平台至少设计了多个过程状态。

研究时应避免：

```text
找到账号
→ 推断此人持续上课
→ 推断完成课程
→ 推断毕业
```

建议把学习状态拆成：

```yaml
learner_state:
  account_observed:
  enrollment_observed:
  current_course_access_observed:
  assignment_submission_observed:
  forum_participation_observed:
  exam_reservation_observed:
  exam_attendance_observed:
  score_observed:
  course_completion_observed:
  graduation_observed:
  degree_observed:
```

并固定：

> **account exists ≠ course participation**

> **course participation ≠ course completion**

> **course completion ≠ credential completion**。

这与仓库已有 application-state 方法类似，但研究单位不同：这里不是一次报名漏斗，而是可能持续数年的学习状态机。

---

## 5. 第四条硬规则：digital scheduling ≠ physical execution

### 5.1 课程终结考试：在线预约，线下完成

北外网院 2004 年 1 月报道显示，全国 44 个学习中心有近 7000 名学生参加约 2 万科次课程考试。针对学生分散、学籍状态复杂的情况，课程考试采用平台预约；但实际考试仍进入具体考场，由监考人员组织。

来源：

- <https://www.beiwaionline.com/aboutbeiwai/news/webinfo/2004/01/1272264153859813.htm>

因此：

```text
platform reservation
≠
physical attendance
```

一个 archive 如果只保存“预约成功”界面，最多能证明某次预约状态；不能自动证明考生后来真的到场。

### 5.2 入学考试：结果可在线查询，身体仍要赶路

2004 年 7 月北外网院北京地区新生入学考试包括现场笔试和口试。报道中有天津考生为避免雨天路况很早驾车到北京，也有考生带行李赶考试后续航班、火车或出差；成绩之后可通过网站或学习中心查询。

来源：

- <https://www.beiwaionline.com/aboutbeiwai/news/webinfo/2004/07/1272264153673090.htm>

因此：

> **online result query ≠ online examination**。

### 考古字段

```yaml
assessment:
  registration_channel: web | center | mixed | unknown
  reservation_channel: web | center | mixed | unknown
  execution_mode: online | physical | mixed | unknown
  execution_location:
  identity_check:
  proctoring_mode:
  result_channel: web | center | mail | mixed | unknown
  attendance_evidence:
```

不要因为系统叫“网络教育学院”就给所有 assessment 自动填 `online`。

---

## 6. 第五条硬规则：courseware exists ≠ student accessed it

2005 年北外网院公告显示：

- 光盘辅导课件可以单独购买；
- 也可与文字教材、录音磁带组成套装；
- 教材订购有单独通道；
- 如果纸质教材没有及时到，学生可以暂时利用网络课件继续学习。

来源：

- <https://www.beiwaionline.com/aboutbeiwai/gonggao/webinfo/2005/05/1272264150991114.htm>
- <https://www.beiwaionline.com/aboutbeiwai/gonggao/webinfo/2005/08/1272264150793292.htm>

这组 evidence 能证明某类资源当时**存在并被提供/销售**，不能证明：

- 每名学生都购买；
- 每名学生都收到；
- 每名学生都实际播放；
- 光盘版本与在线版本完全相同；
- 当前幸存页面能复原光盘内容。

固定：

> **resource offered ≠ resource acquired ≠ resource used**。

建议字段：

```yaml
learning_resource:
  resource_type: web_courseware | print | cassette | cdrom | live_session | recording | other
  offered:
  included_by_default:
  separate_purchase:
  delivery_channel:
  version:
  access_requirement:
  student_acquisition_evidence:
  student_use_evidence:
  preserved_artifact:
```

这延续仓库 `exists ≠ available ≠ used` 的总原则，但在教育案例里必须落实到每种媒介。

---

## 7. 新对象：hybrid learning stack

对于 2000s 网络教育，不建议只记录 URL，应画出学习栈。

例如：

```yaml
hybrid_learning_stack:
  institution: Beijing Foreign Studies University Online College
  observed_period: 2004-2005
  delivery:
    web_courseware: observed
    print_textbook: observed
    audio_cassette: observed
    cdrom_courseware: observed
  interaction:
    course_forum: observed
    live_online_session: observed
    face_to_face_tutorial: observed
  administration:
    online_assignment_submission: observed
    study_record: observed
    online_exam_reservation: observed
  physical_nodes:
    learning_center: observed
    entrance_exam: observed
    end_of_course_exam: observed
```

每个 `observed` 都应链接具体 evidence，而不是从“网络学院”名称推断。

### 为什么这个模型重要

如果只看今天能抓到的 `.html`，会错误地产生一种“纯 Web 教育”的视觉印象。

而真实生活可能是：

```text
周一晚：纸书
周二通勤：磁带
周三晚：网站课件
周四：论坛问题
周末：面授
月底：邮寄/购买教材
期末：坐车去学习中心考试
```

旧网考古若只保存网页，会系统性漏掉这个人的大部分学习日常。

---

## 8. 新缺失机制：courseware survival gap

### 8.1 容易保存的东西

公开 Web 更容易留下：

- 招生新闻；
- 公开公告；
- 宣传文案；
- 学院活动；
- 学生获奖征文；
- 对外咨询页面；
- 公共课程介绍。

### 8.2 难保存的东西

更难长期保存：

- 登录后的课程页面；
- 动态课件状态；
- 私有课程论坛；
- 学生个人作业；
- 教师反馈；
- 学习记录卡；
- 分数与学籍状态；
- 实时 VOB/VOC 会话；
- 已失效的播放器依赖；
- CD-ROM 内容；
- 录音磁带；
- 纸质教材；
- 线下面授；
- 物理考场中的行为。

这构成：

> **courseware survival gap**。

今天的 archive 可能非常擅长回答：

> “这家网院当时宣称自己如何教学？”

却非常不擅长回答：

> “某个普通学生在 2004 年 11 月 17 日晚上 10 点真正打开了什么、交了什么、老师怎样回复、第二天还记得多少？”

### 建议 preservation 字段

```yaml
preservation:
  public_shell_capture:
  authenticated_course_capture:
  forum_capture:
  assignment_capture:
  live_session_capture:
  recording_capture:
  cdrom_preserved:
  print_material_identified:
  cassette_identified:
  physical_exam_record:
  capture_runtime_dependencies:
  completeness: high | medium | low | unknown
```

---

## 9. 登录门槛会产生 enrollment-gated invisibility

Web archive 的另一个结构偏差是：

```text
公开页面 → crawler 可访问 → 容易留下
登录页面 → 需要 credentials/session → 常被挡住
课程状态 → 需要数据库 + 权限 → 更难留下
```

因此形成 **enrollment-gated invisibility（注册/学籍门控不可见性）**。

它与此前 `DOCUMENT_GATED_SHARED_ACCESS...` 的“现实场所进入网吧要身份证”不同：

- 那一份方法文档研究**接入互联网之前的物理访问门槛**；
- 本笔记研究**已经在 Web 上以后，只有正式学生才能进入的应用层内容门槛**。

两层不能合并。

### 推理边界

> **not archived behind login ≠ did not exist**

同时：

> **login form archived ≠ authenticated state archived**。

一个保存下来的登录页只证明入口存在，不证明 archive 进入过历史账号内部。

---

## 10. learner voice 的证据等级：同期第一人称仍然可能是精选出来的

2005 年新浪教育保存了一组北外网院学生学习文章，例如：

- 《我要上学》；
- 《网院学习第一年》；
- 《网院学习生活感想点滴》；
- 更早的网院征文获奖文章。

来源：

- <https://edu.sina.com.cn/en/2005-06-30/201533753.html>
- <https://edu.sina.com.cn/en/2005-06-30/201633754.html>
- <https://edu.sina.com.cn/en/2005-06-30/195533752.html>
- <https://edu.sina.com.cn/en/2005-04-29/160533061.html>

这些页面非常有价值，因为它们是**同时代第一人称生活材料**。其中可以看到：

- 已工作后重新成为学生；
- 工作、育儿、家庭、休息与学习争夺时间；
- 使用纸书、磁带、光盘和在线资源；
- 把学习切进清晨、深夜、通勤；
- 参加面授和在线助学。

但页面语境同时显示，它们出现在北外网院活动、征文或学院推广集合里。

因此必须标：

```yaml
learner_voice:
  first_person: true
  contemporary: true
  platform_selected: true | probable | unknown
  award_or_campaign_context:
  editorial_process_known: true | false
  representativeness: not_established
```

固定：

> **contemporaneous first-person ≠ unprompted diary**。

以及：

> **published learner story ≠ typical learner experience**。

这类材料可以非常强地支持“这种生活机制真实存在”，但不能单独支持“多数学生如此”。

---

## 11. 新偏差：success-story survival bias

网络教育机构有动力长期保留：

- 优秀学员；
- 毕业典礼；
- 学习心得；
- 获奖征文；
- “如何克服困难”的故事。

相对更不容易形成公开永久页面的是：

- 半途停学；
- 忘交作业；
- 没有参加考试；
- 账号闲置；
- 因育儿退出；
- 因加班退出；
- 因费用退出；
- 因技术困难放弃；
- 对文凭认可失望后不再继续。

因此旧网保存会产生 **success-story survival bias**。

这与仓库已有 `negative-state survival gap` 相呼应，但在网络教育里还多一层制度选择：失败状态不仅不一定有 URL，平台还更可能主动把成功故事做成公共内容。

### 研究要求

任何使用学生征文的 case，至少主动寻找一类反向 evidence：

- 退学/休学规则；
- 学籍变更公告；
- 未通过考试后的处理；
- 平台技术故障投诉；
- 社会对文凭认可的同期疑问；
- 教育主管部门对违规办学/质量问题的文件。

例如教育部 2002 年关于加强网络教育学院管理的意见明确指出，当时快速扩张过程中已出现管理制度、办学条件、教学资源和违规办学等问题：

- <https://www.moe.gov.cn/s78/A07/zcs_left/moe_743/201006/t20100608_110174.html>

这类制度性反证可防止把机构成功叙事写成整个系统的完整现实。

---

## 12. 实时教学 artifact 不是普通静态页面

2005 年北外网院 VOB 作业反馈公告列出明确的实时节目时间和平台路径：进入平台社区、特定频道参加指定时段的教师反馈。

来源：

- <https://www.beiwaionline.com/aboutbeiwai/gonggao/webinfo/2005/07/1272264150871637.htm>

这类 artifact 至少拆成：

```yaml
live_session:
  announcement_page:
  scheduled_datetime:
  platform_path:
  access_gate:
  actual_stream_or_audio_artifact:
  attendance_record:
  replay_artifact:
  transcript:
  runtime_requirement:
```

公告保存只能证明“该活动被安排/宣布”。

> **session announcement ≠ session occurred exactly as announced**

更不能推出：

> **session announcement ≠ particular learner attended**。

如果回放文件、日志、教师讲稿和参与记录分别保存，才可以升级结论。

---

## 13. 历史 URL 仍在 origin host 上，不等于今天看到的是原始页面形态

北外网院的许多 2004–2005 历史文章今天仍可由学校域名返回，而且正文内部有明确的历史发布时间。

这种证据很强，但必须拆开：

```yaml
surviving_historical_page:
  current_url:
  internal_publication_date:
  current_fetch_date:
  historical_capture_verified: true | false
  historical_html_verified: true | false
  current_template_date_known: true | false
  embedded_media_survives: true | false | partial
```

固定：

> **historical article date ≠ verified historical page rendering**。

正文可能是当年内容持续迁移到后来 CMS 的结果；当前导航、页脚、CSS、图片地址、脚本和字符集都可能经过后续重构。

这不是新的 `temporal composite` 定义，相关概念已经在仓库 `ELICITED_FUTURES...` 文档中建立；本案例只调用那条规则，不重复扩张。

---

## 14. 网络课程的浏览器/插件依赖必须单独登记

2004–2005 网络教育可能涉及：

- Flash 导航或入口；
- 嵌入式音视频；
- 特定媒体播放器；
- 旧版浏览器脚本；
- 专有格式的语音/直播组件；
- CD-ROM 本地执行环境；
- 弹窗和 frame；
- 依赖服务器数据库的动态课程页面。

北外网院 2004 年“新生网院一周通”当前历史页就明确提到首页曾有 `FLASH` 闪动标题：

- <https://www.beiwaionline.com/aboutbeiwai/news/webinfo/2004/06/1272264153715552.htm>

因此后续若进入 M3 浏览环境复原，不能只测试今天的静态正文。

### 建议字段

```yaml
runtime:
  browser_requirement:
  plugin_requirement:
  media_codec:
  flash_dependency:
  javascript_dependency:
  local_cdrom_dependency:
  server_side_dependency:
  modern_replay_result:
  historical_environment_tested:
```

在没有旧环境复核前，不得把“现代浏览器能打开学院新闻”写成“2004 学生课件环境已成功复原”。

---

## 15. 教材物流也是网络教育 artifact 的一部分

2005 年教材订购公告说明，课程材料仍需要单独订购、销售和配送；如果教材未及时送达，才建议先使用网络课件继续学习。

这说明 `distance learning` 还有一个经常被 Web archive 遗漏的物流层：

```text
课程选择
→ 教材订单
→ 付款
→ 仓储/邮寄/现场购买
→ 学生收到纸书/磁带/光盘
→ 与网站并行使用
```

如果后续找到历史订单系统，应独立处理：

```yaml
material_fulfillment:
  order_channel:
  payment_channel:
  shipping_or_pickup:
  inventory_state:
  shipment_state:
  receipt_evidence:
```

但不要从“教材订购通道存在”推断具体某个学生已经收到教材。

---

## 16. 网络教育考古的最小 artifact graph

建议一条完整 case 至少画：

```text
public admissions page
        ↓
application / eligibility
        ↓
learner identity + enrollment
        ↓
learning platform account
        ↓
course registration
        ↓
┌──────────┬───────────┬───────────┐
│ web       │ physical   │ offline   │
│ courseware│ tutorial   │ print/CD  │
│ forum     │ center     │ cassette │
│ assignment│ exam       │          │
└──────────┴───────────┴───────────┘
        ↓
assessment state
        ↓
course completion
        ↓
credential state
```

每一条箭头都需要证据。

一张首页 capture 不能自动填完整张图。

---

## 17. 与生活史交叉时，建议使用的字段

为了让旧网页与 `how-people-lived` 的普通生活研究真正挂钩，可额外记录：

```yaml
lived_learning:
  employment_status:
  household_role:
  caregiving_role:
  study_location:
  study_times:
  commute_use:
  weekly_face_to_face_requirement:
  exam_travel_requirement:
  equipment_required:
  network_access_required:
  material_delivery_required:
  credential_goal:
  reported_time_conflict:
  reported_cost_conflict:
```

注意：这些字段不能由平台设计直接自动填写。

例如“系统支持随时学习”只证明功能；只有学生同期材料或时间使用资料才能填写 `study_times`。

---

## 18. 证据表

| Artifact | 证据级别 | 可以证明 | 不能证明 |
|---|---:|---|---|
| 教育部 1999–2002 现代远程教育政策 | A | 制度授权、试点范围 | 普通学生实际体验 |
| 教育部 2002–2003 信息化统计 | A/B | 学生量级、在职比例、学习中心规模 | 每个网院具体媒介组合 |
| 北外网院 2004–2005 current surviving historical pages | A/B-near-primary | 当时制度/资源被第一方历史正文描述 | 当前 HTML 等于历史原始 HTML |
| 2004 入学考试/期末考试报道 | A/B-near-primary | 物理考试与在线查询/预约并存 | 每一名网生都按相同流程 |
| 2005 教材/光盘公告 | A/B-near-primary | 多媒介资源提供 | 每名学生实际购买/使用 |
| 2005 新浪学生第一人称文章 | A/B first-person curated | 具体个人同时代体验 | 代表全部学生 |
| 当前静态登录页 | 取决于 provenance | 入口形态某个当前状态 | 历史账户内部状态 |
| Wayback 的公共学院首页 | A capture | 某时点公开页面 | 登录后课程、物理课堂、CD/纸书体验 |

---

## 19. 已证实 / 高概率 / 不知道

### 已证实

- 2000s 中国网络教育并非纯 Web；至少在北外网院案例中，纸质教材、录音磁带、CD、在线课件、论坛、面授、学习中心和物理考试共同存在。
- 在线考试预约/成绩查询与线下考试可以同时存在。
- 登录后的课程状态和公开学院页面属于不同访问层。
- 2005 年公开学生第一人称材料显示学习可以叠加在工作、育儿和日常生活之上。

### 高概率但仍需 archive 级验证

- 许多今天还在 origin host 上的 2004–2005 正文经过了后续 CMS/template 迁移，而不是当年 HTML 原封不动保存。
- 登录后的论坛、作业和个人进度比公开招生/宣传页存在更严重的 archive gap。
- 非 Web 资源（CD、磁带、教材）会导致仅靠 Web archive 的研究系统性低估混合教学比例。

### 不知道

- 2004 北外学习平台每一课程页面的真实历史 DOM/CSS/浏览器要求；
- VOB/VOC 使用的完整协议、播放器和服务器依赖；
- 历史论坛、作业、个人学习记录还有多少经过合法公开授权的完整 capture；
- 同一学生从注册到毕业的完整纵向 Web 状态链是否仍可复核；
- 退学/休学学生在公开 Web 中留下多少同期第一人称材料。

---

## 20. 后见之明与 reconstruction 风险

### 不要把今天的 LMS 结构倒灌到 2004

不能因为今天 Moodle/Canvas 常见，就假设当时也有相同：

- course dashboard；
- progress bar；
- responsive player；
- 标准化论坛；
- 浏览器内视频。

必须从当年帮助页、截图、课件、安装要求或真实 capture 证明。

### 不要用“现在能打开”证明“当年这样显示”

当前 origin 页面是重要 locator，不是自动的 historical rendering proof。

### 不要重建普通学生私有学习记录

- 作业；
- 成绩；
- 论坛私密讨论；
- 身份信息；
- 账号；

如涉及普通个人，应按研究必要最小化，不为了完整 state machine 去恢复已删除或未公开的私人信息。

### 不要把 CD/磁带缺失用生成内容补齐

如果原课件不可得，记录 `missing artifact` 即可；生成式“复原课程”只能做明确标记的 reconstruction，不能伪装 historical original。

---

## 21. 对 M4 缺失地图的意义

网络教育是非常适合做 archive-gap 抽样的一类中文旧网站，因为同一个制度天然包含：

```text
public static pages
+ authenticated pages
+ database states
+ streaming/live media
+ downloadable courseware
+ physical media
+ local centres
+ offline exams
```

未来可选择 3–5 个 2000–2005 试点网院，对每个对象测：

- public page capture rate；
- login-page survival；
- authenticated-course survival；
- media subresource survival；
- help/tutorial page survival；
- courseware download survival；
- non-Web material locator survival。

这比只统计“首页是否被 Wayback 抓到”更能说明中文旧网真实保存边界。

---

## 22. 这改变了旧网考古的哪一点

此前很容易把一个旧网对象理解成“网页上的生活”。网络教育案例迫使研究单位再向外扩一层：

> **历史 Web 有时只是一个更大生活系统的控制面板，而不是生活本身。**

在网院里，Web 可以负责：

- 找资源；
- 交作业；
- 查通知；
- 约考试；
- 参加论坛；
- 看回放。

但人的生活仍同时发生在：

- 单位；
- 家；
- 通勤路上；
- 学习中心；
- 考场；
- 纸书；
- 磁带；
- CD-ROM。

因此以后研究招聘、政务、银行、教育、旅行等 transactional old web 时都应追加一个问题：

> **这个页面是完整过程，还是一个跨媒介生活流程中的控制接口？**

本轮对网络教育给出的答案非常明确：它往往只是接口之一。