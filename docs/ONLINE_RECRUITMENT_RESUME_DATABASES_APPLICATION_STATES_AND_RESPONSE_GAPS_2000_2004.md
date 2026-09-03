# ONLINE_RECRUITMENT_RESUME_DATABASES_APPLICATION_STATES_AND_RESPONSE_GAPS_2000_2004.md

> 范围：约 2000–2004 中文网络招聘页面、简历数据库、求职流程与保存缺口
>
> 状态：research note / execution-state model
>
> 日期：2026-09-03
>
> 关联生活史：`tmzncty/how-people-lived/topics/job-search-addressability-application-labor-and-recruitment-routes-china-1993-2026.zh-CN.md`

## 0. 为什么这是一个旧网考古对象，而不只是就业史

网络招聘特别适合检验本仓的核心方法，因为它是一类典型的 **execution-state web**：

公开网页只保存流程很薄的一层，真正决定一个人是否得到工作的状态大量存在于：

- 动态职位库；
- 可修改的个人简历；
- 搜索索引；
- 雇主后台；
- 站内消息或 email；
- 电话；
- 面试安排；
- 线下办公室；
- 最后的 offer 与入职。

因此，一个保存完好的“招聘首页”或“填写简历”表单，几乎从来不能直接回答：

> 当时有哪些职位真的还有效？
>
> 某个人的简历有没有被雇主看到？
>
> 一封申请有没有收到回复？
>
> 一次回复有没有变成面试？
>
> 一次面试有没有变成工作？

本条目的核心边界是：

> **page survived ≠ backend state survived ≠ transaction executed ≠ employment outcome known**

---

## 1. Scope：严格留在中文旧网 2000–2004

本文件主体只讨论：

- 2000 年前后网络、报纸、电话、传真、email 并存的招聘入口；
- 2001 年左右可观察的求职简历字段、登录、修改与删除机制；
- 2003 年网上招聘会的申请—回复断裂；
- 页面、动态数据库、个人资料、email/电话 handoff 与后续结果的保存偏差。

不把本仓扩成全球招聘史。

1993 年大型人才市场只作为必要前史边界：它说明在中国 1994 年全功能接入国际互联网以前，职位信息集中、求职者集中和面对面筛选已经可以由线下人才市场完成。全球比较和 2008–2026 的生活史变化放在 `how-people-lived`，不写进本仓主范围。

---

## 2. Evidence contract

### 2.1 A/B/C/D

沿用 `docs/METHOD.md`：

- **A**：可定位的同时代原始页面、官方帮助、历史 capture 等；
- **B**：同期记者观察、教程、用户操作说明；
- **C**：后来回忆；
- **D**：研究者的状态机、保存偏差和机制推断。

### 2.2 本轮一个重要特殊状态：live legacy artifact

新浪目前仍可访问一组带有 2001 年内容、字段和旧路径的求职页面。

但：

> **current live response ≠ verified 2001 archive capture**

本轮没有取得并验证：

- 2001 年当日 WARC；
- 历史 HTTP headers；
- 历史浏览器 screenshot；
- 当日服务器端代码；
- 当时数据库快照。

因此这些页面只证明“一个明显带有历史内容和旧接口结构的 legacy artifact 今天仍可取得”，不能把今天的 response body 自动当成 2001 年原封不动的服务器输出。

涉及具体历史页面视觉、charset、JS 或浏览器要求时仍然必须停在“不知道”。

---

## 3. 2000：网络招聘首先嵌入多媒介体系

### Claim OWR-RECRUIT-2000-01

**2000 年 3 月的同期报道把网络、报纸和猎头组合描述为同一套招聘服务；个人求职者还可以通过来信、电话、传真、email 或直接网页注册加入。**

证据：

- 《生活时报》2000-03-06《找工作“网络、报纸、猎头”一站购齐》
- URL：https://www.gmw.cn/01shsb/2000-03/06/GB/03%5E1274%5E0%5ESH3-631.htm
- 等级：B（同期媒体；关于服务模式的描述接近平台公告，规模与效果不能据此独立验证）

同一事件也有新浪科技同期报道：

- 2000-02-28：https://tech.sina.com.cn/news/it/2000-02-28/18495.shtml
- 等级：B；与上一报道可能共享同一宣传材料，不能简单算两个完全独立 evidence family。

### 它证明什么

至少证明当时的招聘服务设计本身就是 **hybrid media stack**：

```text
paper / newspaper
phone
fax
email
Web registration
headhunter / human screening
```

所以旧网史不应写成：

> “2000 年左右招聘从报纸搬到网上。”

更准确：

> **Web 被接到原有纸媒、电话和人力中介之上。**

### 它不证明什么

它不证明：

- 2000 年所有求职者都能上网；
- 51job 已成为全国主导渠道；
- 所有发布职位都真实有效；
- 使用网络的人最终更容易就业；
- 网络已经替代人才市场、学校和熟人介绍。

---

## 4. 2001：简历数据库把普通人的经历变成结构化查询对象

### Claim OWR-RECRUIT-2001-01

新浪教育当前仍保留一份标记面向“2001 届毕业生”的求职信息表单。可观察字段包括：

- 会员 ID / 密码；
- 姓名；
- 学校；
- 专业；
- 求职地区；
- 行业；
- 职位；
- 简历摘要；
- 联系方式；
- 修改 / 删除求职信息的入口。

URL：

- https://edu.sina.com.cn/job/zhaopin/findjob.html

证据状态：**A-candidate / live legacy artifact**。

理由：字段和历史内容直接可观察，但本轮没有验证 2001 年 capture datetime，不能把今天的 live response 等同于当年 snapshot。

### Claim OWR-RECRUIT-2001-02

2001 年同期求职教程明确建议：

- 选择更新快、流量和职位信息较好的网站；
- 用户应能用 ID/密码登录修改简历；
- 系统可以把简历自动送给企业；
- 可以生成简历 URL；
- 为提高检索命中，应在字段中考虑“网页 / 主页 / 网站”等同义词。

来源：

- 新浪教育 /《生活时报》2001-01-12：https://edu.sina.com.cn/j/18760.shtml
- 等级：B（同期教程，适合证明当时被教导的操作逻辑，不等于所有网站功能一致）

### 考古意义：resume is mutable state

纸质简历可以作为一个固定 artifact 保存。

网络简历却更像状态：

```text
create profile
→ publish / searchable
→ edit
→ update expected role / city / contact
→ hide / delete
→ perhaps re-activate
```

因此某次 capture 只代表某个时点，不能把后来看到的字段倒投回更早时间。

固定规则：

> **profile page at t2 ≠ profile state at t1**

> **current surviving profile ≠ all historical versions**

> **resume URL survived ≠ profile remained intentionally public throughout the interval**

---

## 5. Machine legibility 在 2001 年已经存在，不必等到 AI 招聘

2001 年教程要求求职者考虑关键词和同义词，本身已经说明招聘数据库存在一种早期 **query-facing representation**：

求职者必须让系统能够通过字段或关键词找到自己。

这和 2020s AI 自动评分当然不是同一技术层级，不能用现代 ATS/LLM 术语倒写 2001 年系统。

但最低限度可以说：

> **数据库化招聘已经使“怎样把自己写成可被查询的记录”成为普通求职操作的一部分。**

旧网研究如果只截首页，会把这个机制漏掉。

真正重要的 artifact 常常是：

- search form；
- resume form；
- field taxonomy；
- update/delete endpoint；
- search result URL；
- query parameters；
- employer-side search / filtering documentation。

---

## 6. Privacy finding：历史简历可能比它对应的求职关系活得更久

本轮搜索过程中，搜索引擎仍能返回至少一份 2001 年左右的普通个人求职页面，其中包含直接身份与联系信息。

依照 `AGENTS.md` 与 `docs/METHOD.md` 的“研究必要最小化”原则：

- 不在仓库记录该人的姓名；
- 不抄录 email；
- 不抄录电话；
- 不给出个人页面 locator；
- 不用个人资料做 screenshot 或 fixture；
- 不因为公开搜索还能找到，就认定其继续公开符合当事人现在的意愿。

这个负结果本身值得记录：

## public-resume afterlife

网络招聘会产生一种特殊的历史残留：

> **求职目的早已结束，但为了当年被雇主联系而公开的个人资料可能继续存活。**

因此：

> **archive completeness can conflict with privacy correctness**

本仓在这种情况下应研究 URL pattern、字段结构和平台状态，而不是重新公开普通人的 PII。

---

## 7. 2003：大量投递与极少可见回复，产生 application-response gap

2003 年 SARS 期间，同期媒体对网络招聘会的调查提供了一个非常有价值的后台切口。

报道给出某网上招聘活动连续两日的粗数据：

- 一日：26,597 份简历，75 个面试通知；
- 次日：26,682 份简历，257 个面试通知。

来源：

- 2003-05-23，同期调查：https://edu.sina.cn/sa/2003-05-23/detail-ikftpnny8650557.d.html?vt=4
- 等级：B（同期记者调查；具体后台数字仍依赖主办方或平台提供）

报道还明确指出，主办方自己也难以确切知道最终通过网络招聘找到工作的总人数。

### 不能错误计算“成功率”

不能直接做：

`75 / 26597 = 网络求职成功率`

因为：

- `resume submission` 不是独立个人；
- 同一人可投多个岗位；
- `interview notice` 不是 offer；
- 一个面试可对应多人；
- 平台不知道最终线下就业结果；
- 后续可能转电话/email/线下面试。

### 真正可写的历史结论

> **平台可以观测“提交了多少简历”，却无法自动观测“最后有多少人真正就业”。**

这正是 execution-state archaeology 的核心。

---

## 8. 一个网络招聘 execution state machine

研究 2000s 招聘页面时，至少应区分以下状态：

```text
employer has a real need
        ↓
vacancy created
        ↓
vacancy published
        ↓
listing indexed / searchable
        ↓
job seeker discovers listing
        ↓
job seeker reads requirements
        ↓
resume/profile exists
        ↓
application submitted
        ↓
platform/backend receives submission
        ↓
application enters employer queue
        ↓
recruiter actually opens / screens it
        ↓
contact attempted
        ↓
email/phone/message actually reaches applicant
        ↓
interview proposed
        ↓
interview actually happens
        ↓
offer proposed
        ↓
applicant accepts / declines
        ↓
identity/credential checks if any
        ↓
actual onboarding
        ↓
continued employment
```

任何公开页面最多只证明其中少数节点。

---

## 9. 新增 archive gaps

### 9.1 vacancy-snapshot gap

某个职位列表页保存下来，不代表职位在整个页面存活期都有效。

固定：

> **listing exists in capture ≠ vacancy still open at user query time**

可能发生：

- 已招满但页面没删除；
- 招聘暂停；
- 重复发布；
- 列表缓存滞后；
- 旧页仍被搜索引擎索引。

### 9.2 search-index / ranking gap

知道职位数据库里有多少条，不等于知道某个求职者当时输入条件后看到了什么排序。

动态 query 通常依赖：

- 关键词；
- 地区；
- 行业；
- 职位分类；
- 发布日期；
- 用户 profile；
- 数据库当时状态。

历史首页不能恢复这些条件的笛卡尔积。

### 9.3 resume-version gap

网络简历可修改，所以一个 profile URL 不是一个稳定文档。

需要区分：

- account created_at；
- resume version at t1；
- resume version at t2；
- current live artifact；
- delete/hide/reactivate state。

### 9.4 application-submit gap

点击“提交”或存在投递按钮，不代表：

- 请求成功到达服务器；
- 后台建立记录；
- 企业账号能看到；
- 该职位仍接受申请。

固定：

> **form/action survived ≠ historical POST succeeded**

### 9.5 recruiter-attention gap

后台收到申请，也不等于招聘者实际阅读。

这是在线招聘最关键的不可见状态之一：

> **received ≠ opened ≠ understood ≠ shortlisted**

### 9.6 no-response ambiguity

一名求职者没有收到消息，可能因为：

- 未读；
- 系统失败；
- 联系方式失效；
- 被筛掉；
- 职位取消；
- 招聘完成；
- 雇主改走线下；
- 回复进入 spam 或错误邮箱；
- 求职者自己停止等待。

所以：

> **silence ≠ rejection unless source says so**

### 9.7 email / phone handoff gap

早期招聘网页常把执行流程交给 email 和电话。

Web archive 通常不会保存：

- 个人邮箱收件箱；
- 招聘者发出的私人邮件；
- 电话通话；
- 手机短信；
- 后续约定。

因此“网页证据链断了”不等于关系断了。

### 9.8 interview-outcome gap

即使同期报道确认收到面试通知，仍不能推断：

- 到场；
- 面试完成；
- offer；
- 接受；
- 入职。

### 9.9 offer / onboarding gap

最终就业往往发生在平台之外。

这会产生一种系统性历史偏差：

> **招聘网站最容易保存“机会存在”和“人想申请”，最难保存“一个人的生活后来真的被这次申请改变”。**

### 9.10 cross-post duplication gap

同一岗位可以同时存在于：

- 企业官网；
- 招聘网站；
- 报纸；
- 学校就业网；
- 论坛转帖；
- email list。

所以页面数量不是职位数量。

固定：

> **many listings ≠ many vacancies**

### 9.11 aggregate-metric gap

平台发布“多少职位”“多少简历”“多少访问”时，应分别问：

- 独立用户还是 pageviews？
- 活跃职位还是累计职位？
- 简历数还是投递次数？
- 是否含重复/过期？
- 是否为平台自己宣传口径？

不能把营销数字直接写成劳动力市场规模。

---

## 10. 页面保存偏差：空壳往往比结果活得久

网络招聘有一个特别明显的保存不对称：

### 容易活下来

- 首页；
- 品牌介绍；
- 填表页面；
- 使用帮助；
- 公开职位广告；
- 静态简历；
- 新闻稿。

### 很难活下来

- 某天职位库存；
- 某次查询排序；
- 某次 POST；
- 雇主后台；
- 简历阅读状态；
- email 回复；
- 电话；
- 面试；
- offer；
- 实际入职。

所以旧网 archive 天然容易形成一种错觉：

> “我们能看到很多岗位和很多求职者，所以好像能重建整个就业市场。”

实际上我们常常只保存了**交易入口**，而不是**交易结果**。

---

## 11. 浏览器、编码与运行环境：本轮明确不知道什么

对于 2001 新浪 legacy 页面，本轮可以确认的是：

- 旧路径今天仍有可解析文本；
- 页面保留明显的历史求职字段和操作入口；
- 部分旧站资源路径/统计路径仍可从页面结构中看到。

但本轮没有完成：

- 历史 IE / Netscape 回放；
- 2001 HTTP `Content-Type` / charset 验证；
- 历史 JavaScript 行为；
- form POST 目标的当时 backend；
- 动态搜索 result 的历史 snapshot；
- 图片、字体和 viewport 的历史一致性验证。

因此禁止写：

- “该页当年必须用 IE6”；
- “该页当年就是 GB2312/GBK”；
- “今天现代浏览器看到的布局就是 2001 用户看到的布局”；
- “当前表单还可以完成历史招聘流程”。

年代直觉不能替代 capture/headers/browser experiment。

---

## 12. Live legacy rendering 的时间层问题

当前仍在线的历史页面可能混合：

1. 2001 年写入的主内容；
2. 后来迁移时保留的 HTML；
3. 后来替换或失效的子资源；
4. 当前 CDN / HTTP 层；
5. 当前搜索引擎缓存或抽取结果。

因此：

> **historical content visible today ≠ historical server state reconstructed**

网络招聘尤其要防止把“今天还能搜到的一个旧简历页面”当成“2001 年完整招聘数据库快照”。

一个个案 profile 只证明一个 profile 曾以某种形式存在，无法回答：

- 当时同时有多少 profile；
- 哪些可被企业搜索；
- 排名；
- 活跃状态；
- 更新频率；
- 是否已经完成就业后忘记删除。

---

## 13. “成功退出”与招聘网站的反直觉保存偏差

招聘平台可能存在与婚恋、二手交易相似但不完全相同的 **success-exit bias**：

一个人找到工作后，可能：

- 删除简历；
- 隐藏简历；
- 不再登录；
- 忘记删除，让旧简历继续公开；
- 几年后再激活。

所以今天残留的旧简历集合不能解释成：

- “当时真正活跃的求职者”；
- “当时找不到工作的人”；
- “成功找到工作的人”；
- “平台历史成功率”。

成功和失败都可能导致不同的页面消失/保留行为。

---

## 14. 与个人通信身份的交叉：contact continuity

早期求职页面通常要求联系方式。

这提示一个值得跨仓继续研究的问题：当个人 email、手机号逐步成为稳定个人标识后，求职联系可以更少依赖：

- 学校办公室；
- 当前单位电话；
- 家庭固定电话；
- 固定地址。

这可能提高换工作和跨城市求职的联系连续性。

但本轮没有足够定量材料确认影响大小，所以只登记为研究问题，不写成已证实因果。

---

## 15. 2003 的线下反证：Web 没有消灭招聘大厅

2003 年同期报道还记录，在实体招聘活动恢复以后，一部分求职者仍明确偏好面对面交流，网络则被用于先看信息。

同一份调查里，一个 23 人班级已就业者的渠道分布也显示：传统招聘会、熟人和学校信息仍然重要，而通过当次网上招聘会就业者只有一人。

这是一个非常小的班级样本，不能统计外推。

它的考古价值是：

> **历史页面里的“网上招聘会”不能被自动解释为整个招聘行为已经 Web 化。**

旧网研究需要恢复 handoff：

```text
Web discovers opening
→ phone/email contact
→ physical fair / office interview
→ offline decision
```

而不是把用户停在浏览器里。

来源：

- 2003-05-23：https://edu.sina.cn/sa/2003-05-23/detail-ikftpnny8650557.d.html?vt=4

---

## 16. 推荐的数据模型

以后如果进入 schema，可为招聘 artifact 增加：

```yaml
artifact_type: recruitment_page
platform:
host:
original_url:
capture_url:
capture_datetime:
observed_today:
evidence_grade:

page_role:
  # vacancy_list | vacancy_detail | resume_form | resume_profile |
  # search_form | search_result | help | employer_form | news

historical_time_claim:
current_response_time:

requires_account: unknown
profile_mutable: unknown
listing_mutable: unknown
backend_required: unknown

fields_observed: []
query_dimensions_observed: []

handoff_channels:
  - web
  - email
  - phone
  - fax
  - offline

browser_assumption: unknown
charset_historical: unknown

pii_present: false
pii_republication_allowed: false

known_gaps:
  - vacancy_snapshot
  - search_index_state
  - resume_version
  - application_receipt
  - recruiter_attention
  - offplatform_contact
  - interview_outcome
  - offer_outcome
```

重点不是把 schema 填满，而是强迫研究者不要把一个 page 当成一次完整就业关系。

---

## 17. 已证实 / 高概率 / 不知道

### 已证实

- 2000 年同期招聘服务明确把 Web 与报纸、电话、传真、email、猎头组合使用；
- 2001 年同期教程已经把可编辑网络简历、自动投递、个人简历 URL 和关键词检索作为求职操作；
- 新浪当前仍可取得带有 2001 届求职字段和修改/删除入口的 legacy 页面；
- 2003 年网上招聘活动能记录大量简历提交和少量面试通知，而主办方并不能据此准确知道最终就业人数；
- 早期网络招聘的关键后续步骤大量会转到 email、电话和线下。

### 高概率，但还需要 archive/技术证据加强

- 早期求职数据库存在明显的动态 state，今天无法靠静态页面恢复历史完整索引；
- 同一 profile/职位 URL 在不同时间可能对应不同状态；
- 当前仍在线的历史页面可能经历服务器迁移或资源替换；
- 个人 email/手机号可能提高跨单位求职联系连续性。

### 不知道

- 当前 Sina legacy 页与 2001 年原 HTML 是否字节级一致；
- 2001 年具体 charset/header；
- 2001 年典型浏览器兼容范围；
- 某个历史 query 在某天返回的完整结果；
- 某个具体普通人投出的申请是否到达雇主；
- 某次面试通知是否最后导致入职；
- 公开 legacy profile 的历史所有版本；
- 被删除的个人简历为何删除。

---

## 18. Stop conditions / 隐私与复原边界

遇到以下情况，不为了“完整链条”继续追：

- 只能通过重新公开普通人的邮箱、电话、住址来证明字段存在；
- 只能依赖泄露数据库或历史账号登录；
- 个人简历已删除但第三方缓存还可找到敏感内容；
- 没有历史 capture，却准备把当前 live legacy page 当 2001 原件；
- 不知道历史 charset/browser，却准备凭年代猜；
- 雇主后台和私人邮件不可见，却准备补写“这个人后来被拒绝/录取”。

**无法恢复一次求职的最终结果，是允许且重要的考古结论。**

---

## 19. 本轮对中文旧网理解的增量

此前旧网往往容易按“内容平台”想象：主页写什么、论坛讨论什么、博客怎样排版。

网络招聘提醒我们，中文旧网还有一大类更难保存的 **process web / 过程型 Web**：

- 页面只是入口；
- 数据库状态决定当下有什么；
- 账号决定用户能做什么；
- 私人通信决定下一步；
- 真实后果在线下发生。

因此，本轮最重要的结论不是“2000 年代有招聘网站”，而是：

> **旧网 archive 会系统性过度保存广告、表单和公开简历，同时系统性低估搜索排序、后台阅读、私人回复、面试与实际入职。**

如果不把这些 gap 显式写出来，研究者很容易把“平台能够提供什么”误写成“普通人真的经历了什么”。

---

## 20. 下一步最高价值证据

最值得找的不是更多品牌介绍，而是一条不侵犯隐私的、多时点普通求职执行链：

```text
2000–2004 某同期公开日记/论坛求职记录
→ 看到职位
→ 修改简历
→ 投递
→ email/电话收到回应
→ 面试
→ 明确记录 offer / 未录取
→ 数周或数月后更新是否入职
```

优先选择：

- 当事人已经公开发表的同期叙述；
- 报刊跟踪采访；
- 高校公开就业案例；
- 不需要重新暴露姓名、电话、地址的材料。

如果只能通过挖掘已删除私人简历或个人邮箱来补链，则应停止。

---

## Sources

1. 《生活时报》，2000-03-06，《找工作“网络、报纸、猎头”一站购齐》：https://www.gmw.cn/01shsb/2000-03/06/GB/03%5E1274%5E0%5ESH3-631.htm
2. 新浪科技，2000-02-28，《财富》500 强企业与“前程无忧联盟”签约：https://tech.sina.com.cn/news/it/2000-02-28/18495.shtml
3. 新浪教育 /《生活时报》，2001-01-12，网络求职教程：https://edu.sina.com.cn/j/18760.shtml
4. 新浪教育，2001 届求职信息 legacy 表单：https://edu.sina.com.cn/job/zhaopin/findjob.html
5. 2003-05-23，同期网上招聘调查：https://edu.sina.cn/sa/2003-05-23/detail-ikftpnny8650557.d.html?vt=4
6. 关联中国互联网全功能接入边界（只用于前史说明）：https://www.cac.gov.cn/2024-04/20/c_1715291120716362.htm

访问日期：2026-09-03。