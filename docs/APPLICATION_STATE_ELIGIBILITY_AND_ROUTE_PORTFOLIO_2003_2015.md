# APPLICATION_STATE_ELIGIBILITY_AND_ROUTE_PORTFOLIO_2003_2015

## Scope

本说明研究约 2003–2015 中文互联网里一类容易被普通网页考古误读的对象：**招生、招考和招聘申请系统中的“申请状态（application state）”与“资格状态（eligibility state）”**。

主要例子来自：

- 硕士研究生网上报名；
- 中央/地方公务员网上招考；
- 高等教育学历电子注册/查询。

它与已有 [`TRANSACTIONAL_TRAVEL_WEB_AND_REVOCABLE_BOOKING_ARTIFACTS_2011_2015.md`](TRANSACTIONAL_TRAVEL_WEB_AND_REVOCABLE_BOOKING_ARTIFACTS_2011_2015.md) 有交叉，但研究单位不同：

- 交易考古主要问：订单、库存、支付和线下交付怎样形成一笔交易；
- 本说明主要问：**一个人怎样从“看见一条人生路线”变成“制度判断此人是否仍有资格继续走这条路线”。**

本仓 scope 仍保持约 1995–2015 中文旧网。2023–2025 的“巡考”、应届身份延长等生活史比较放在 `tmzncty/how-people-lived`，不把这里扩展成当代就业研究仓库。

---

## 1. 研究单位：不要把“报名网站”当成一个页面

一个招考系统至少可能同时存在以下对象：

```text
public notice / 招考公告
→ position catalogue / 专业目录
→ registration entry / 报名入口
→ authenticated applicant / 登录后的报考者
→ application record / 一次具体申请
→ eligibility review / 资格初审状态
→ confirmation / 缴费、照片、现场或网上确认
→ registration number / 报名序号或类似关键标识
→ admission ticket / 准考证
→ exam attendance / 实际参加考试
→ score / 成绩查询
→ interview / 复试或面试状态
→ admission / employment result
```

因此：

> **portal exists ≠ application filed**

> **application filed ≠ eligibility accepted**

> **eligibility accepted ≠ application confirmed**

> **application confirmed ≠ exam attended**

> **exam attended ≠ final admission/employment**

今天只找到一个历史报名入口截图，最多证明某个入口/表单曾存在，不能自动把一个假想用户一路推进到录取。

---

## 2. 2003–2005 研究生报名：技术接口和制度接口必须分开记录

### 2.1 2003：网上报名只是部分单位试点

教育部 2003 年对 2004 年硕士招生政策的同期说明中，同时出现：

1. 报考者不再需要所在单位同意证明、报名表不再要求单位签字盖章；
2. 部分招生单位试点网上报名，入口为 `chinayz.com.cn`。

这对旧网考古提出一个重要边界：

> **form field disappears ≠ website caused the underlying rule to disappear**。

如果 2003 和 2004 的历史表单之间真的能观察到“单位意见/盖章”字段消失，页面变化只能证明 UI/材料要求发生了变化；真正说明制度原因的证据仍来自招生政策本身。

### 证据

- **A（官方同期政策说明）**：教育部，2003-08-09，《教育部负责人详解研究生招生政策新变化》。  
  <https://www.moe.gov.cn/moe_879/moe_329/moe_296/tnull_2998.html>
- **A（官方同期简要政策页）**：教育部，2003-11-14，《2004年硕士生招生政策主要变化》。  
  <https://www.moe.gov.cn/moe_879/moe_329/moe_296/tnull_2995.html>

### 2.2 2004–2005：全国网上提交以后，仍有现场确认

教育部对 2005 年硕士招生规定考生一律网上报名，并允许在报名期内修改/校正网报信息。

但同年 11 月官方提醒又明确：网上报名后仍必须到指定报考点确认信息、缴费、照相，否则网报无效。

所以旧页面复原不能画成：

```text
提交按钮 → 报名完成
```

至少应画成：

```text
online draft/submission
→ mutable during window
→ physical confirmation
→ fee/photo
→ effective application
```

### 证据

- **A**：教育部，2004-08-25，《关于做好2005年招收攻读硕士学位研究生工作的通知》。  
  <https://www.moe.gov.cn/srcsite/A15/moe_778/s3113/200408/t20040825_79970.html>
- **A**：教育部，2004-11-04，《教育部提醒报考硕士生考生勿忘按时进行现场确认》。  
  <https://www.moe.gov.cn/jyb_xwfb/gzdt_gzdt/moe_1485/tnull_4354.html>

### 新的硬规则

> **online submission ≠ effective registration**

如果现场确认状态没有证据，不得把一条保存下来的网报页面解释成“此人已经取得考试资格”。

---

## 3. 公务员招考：申请开始拥有明确的机器可观察状态

### 3.1 2003：报名人数和审核通过人数已经是两个统计对象

2003 年人事部门公布的 2004 年中央、国家机关公务员招考数据中，360,240 人通过互联网报名，181,488 人通过招考部门审核。

旧网研究最应该保存的不是“36 万人报名”这一单个数字，而是统计口径本身已经区分：

```text
submitted
!=
eligibility_passed
```

这说明“资格审查结果”并不是研究者后来加上的抽象，它已经是当时系统/行政流程真实存在的一种状态。

### 证据

- **B（同期媒体转述人事部门）**：中新网，2003-11-02。  
  <https://www.chinanews.com.cn/n/2003-11-02/26/363811.html>

### 3.2 2005：报名、资格审查、确认、照片、支付、准考证逐层分离

2005 年发布的 2006 年中央、国家机关招考公告显示：

- 报名全部通过网络进行，不设现场报名；
- 通过资格审查以后仍须完成报名确认；
- 一部分省市网上确认，需要上传电子照片并在线缴费；
- 其他地区仍进行现场确认；
- 报考者最后自行下载打印准考证。

因此同一年度甚至存在 **same service, different confirmation channel by exam region**。

不能因为一个北京考生可以网上确认，就把全国所有考生的 2005 年体验复原成全流程在线。

### 证据

- **B/A-near-primary（同期公告转载，来源标注为发改委/中央招考公告）**：搜狐，2005-10-12。  
  <https://business.sohu.com/20051012/n240528095.shtml>

### 3.3 2006 青岛：资格初审状态可以被用户主动回查

青岛 2006 年公安人民警察招考简章提供了一个保存较完整的地方工作流：

- 网上填写个人报考资料；
- 每人限报一个职位；
- 资格确认前再次提交时，后一次信息覆盖前一次；
- 用人单位网上进行资格初审；
- 报考者提交后再回到网站查询初审结果；
- 通过后打印报名登记表、诚信承诺书、准考证主证；
- 再去指定地点现场认定。

这说明旧网里的一个 `status query` 页面具有实际生活含义：用户不是只来“读信息”，而是在等待制度决定自己下一步还能不能继续。

### 证据

- **A（政府站保存的同期招考简章）**：青岛市人社相关页面，2006 年公安人民警察招考。  
  <https://hrss.qingdao.gov.cn/zxzx_47/gzdt_47/202206/t20220613_6129786.shtml>

---

## 4. Application state 不等于 transaction state

已有交易考古模型里，常见状态是：

```text
inventory queried
→ resource locked
→ awaiting payment
→ paid
→ issued
→ changed/refunded
```

而申请系统的核心状态可能是：

```text
opportunity observed
→ applicant says “I fit”
→ form submitted
→ institution checks “you fit / you do not fit”
→ applicant confirms / supplies evidence
→ exam or interview permitted
→ result adjudicated
```

差异在于：

- 订单系统主要处理资源分配和支付状态；
- 申请系统包含**制度裁决**；
- `eligibility` 不是用户自己点击一下就能完成的状态；
- 同一条公开规则落到具体申请人身上时，仍可能出现材料解释、人工审核、异议处理、线下复核。

因此建议把它单独称作：

## adjudicated state（经裁决状态）

它需要回答：

- 谁作出资格判断？
- 判断依据是用户自填字段、上传材料、数据库记录还是线下证件？
- 是否人工审核？
- 是否有申辩/复核机制？
- 状态何时从 provisional 变成 final？

旧网页只保存一个“资格审查通过”模板，不等于已经保存了产生这项判断的证据链。

---

## 5. `registration number` 一类短寿命标识是工作流文物，不只是隐私字段

招考系统常需要一条用户侧短期标识，把后续动作串起来，例如：

- 报名序号；
- 准考证号；
- 订单/申请编号；
- 身份证件号与账户之间的绑定。

对考古来说，这些字段存在具有结构意义：它们说明页面之间不是独立静态文档，而是共享后台状态。

但本仓不需要、也不应重新公开普通历史用户的真实号码。

推荐记录：

```yaml
workflow_key_type: registration_number
workflow_key_required_for:
  - confirmation
  - admission_ticket
  - status_query
historical_value_preserved: false
privacy_reason: ordinary-user identifier minimized
```

即：**保存字段角色，不保存普通人的真实值。**

---

## 6. 学历电子注册：资格凭证开始具有“可查询后端”，但不要虚构系统集成

学信网 2009 年官方沿革页说明：

- 2001 年起实行高等教育学历证书电子注册；
- 2002 年回登 1991–2000 年学历证书信息；
- 2005 年学信网被指定为高等教育学历证书查询网站。

从旧网结构史看，这意味着“学历”不再只是一张用户手里的纸质证书，也存在一个可供查询/认证的网络记录体系。

### 证据

- **A（官方平台制度沿革）**：学信网，2009-02-09，《关于我们》。  
  <https://www.chsi.com.cn/about/200902/20090209/17223140.html>

### 必须禁止的推断

> **credential registry exists ≠ recruitment portal automatically verified against it**

除非拿到当年接口、后台说明、操作手册或明确官方说明，否则不能说某个 2005 年报考系统“自动连接学信网验证学历”。

允许写：

- 当时存在学历电子注册与网上查询制度；
- 某招考公告要求某种学历；

不允许无证据拼成：

- 该招考网站必然实时调用学历数据库完成资格审查。

---

## 7. “一人限报一个职位”也不等于一个人只有一条人生路线

招考公告常规定：

- 在**这一次考试**里只能报一个职位；
- 或资格确认后不能再修改该次职位。

这只定义一个 application cycle 内的约束。

不能推出：

```text
this_exam.max_positions_per_person = 1
therefore
person.total_life_routes = 1
```

一个人仍可能同时参加：

- 国家公务员考试；
- 某省公务员考试；
- 研究生考试；
- 事业单位招聘；
- 企业秋招。

这就是为什么旧网考古需要把 **application record** 和 **person-level route portfolio** 分开。

本仓通常没有足够隐私和跨站证据重建普通人的完整 portfolio，因此默认只记录前者；跨路线的生活史分析应移交 `how-people-lived`。

---

## 8. Archive asymmetry：最容易保存“机会菜单”，最难保存“谁试过哪些路”

旧招生/招考网站的保存偏差非常强。

### 容易被保存

- 招考公告；
- 职位表/专业目录；
- 报名时间；
- 资格条件；
- 操作指南；
- 公开统计；
- 首页和静态帮助页。

### 很难被保存

- 登录后的个人申请；
- 用户曾经修改过的旧版本；
- 资格初审失败页面；
- 因忘记确认/缴费而失效的申请；
- 用户主动放弃的面试；
- 现场确认实际是否完成；
- 同一个人在别的网站同时报了什么；
- 用户电脑里打印出的临时准考证/登记表；
- 失败后没有任何公开结果的人。

所以必须写：

> **archived opportunity menu ≠ historical applicant portfolio**

以及：

> **public eligibility rule ≠ applicant-specific eligibility decision**

现在搜索旧网时，我们更容易看见“制度允许哪些人报名”，而不是“某个普通人那年究竟同时试了多少条路”。

这会系统性高估清晰、完整、最终成功的人生路径，并低估大量短命的候选未来。

---

## 9. 页面回放时要特别检查的技术问题

招生/招考系统比普通内容页更容易出现“看起来有页面，但工作流已经死了”的情况。

### 9.1 动态表单

历史 HTML 可能只保存表单外壳，提交目标 CGI/JSP/ASP 已不存在。

### 9.2 Session / Cookie

登录后页面依赖 session，archive 回放无法复现真实用户状态。

### 9.3 数据库查询

资格审查、成绩、报名状态来自后台数据库；静态 capture 不能证明当时某个具体值。

### 9.4 跨域/跨系统

确认、缴费、照片上传、准考证下载可能在不同 host 或地方考试机构完成。

### 9.5 时间窗

页面只有在报名期间可提交；今天回放一个表单不能证明历史上任意日期都可使用。

### 9.6 浏览器/编码

2000 年代早期政务/教育站常见 GB2312/GBK、IE 假设、JS 表单校验等。现代浏览器能显示正文，不代表历史提交逻辑可工作。

因此：

> **form renders ≠ form was operational at capture time**

如果无法实际验证后台、时间窗和状态响应，应把“可提交”降级为推断。

---

## 10. Evidence family 示例

### Family A — 官方招生政策/规则

- 教育部 2003 年硕士招生政策变化：  
  <https://www.moe.gov.cn/moe_879/moe_329/moe_296/tnull_2998.html>
- 教育部 2004 年关于 2005 年硕士招生网上报名通知：  
  <https://www.moe.gov.cn/srcsite/A15/moe_778/s3113/200408/t20040825_79970.html>
- 教育部 2004 年现场确认提醒：  
  <https://www.moe.gov.cn/jyb_xwfb/gzdt_gzdt/moe_1485/tnull_4354.html>

### Family B — 公务员招考同期规则/统计

- 中新网 2003 年转述人事部门网络报名与审核数字：  
  <https://www.chinanews.com.cn/n/2003-11-02/26/363811.html>
- 2005 年中央招考公告同期转载：  
  <https://business.sohu.com/20051012/n240528095.shtml>
- 青岛政府/人社系统保留的 2006 年招考简章：  
  <https://hrss.qingdao.gov.cn/zxzx_47/gzdt_47/202206/t20220613_6129786.shtml>

### Family C — 学历电子注册体系

- 学信网官方沿革，2009：  
  <https://www.chsi.com.cn/about/200902/20090209/17223140.html>

注意：两个转载同一公告的新闻 URL 仍然只算一个 evidence family。

---

## 11. 建议字段

对于 2003–2015 的招生/招考/公共招聘站点，可以扩展如下字段：

```yaml
service_name:
application_cycle:
service_version_date:
public_notice_url:
application_entry_url:
application_window:
position_or_program_catalogue:
account_required:
identity_fields:
credential_fields:
max_choices_within_cycle:
application_editable_until:
submission_state:
eligibility_review_actor:
eligibility_review_input:
eligibility_state_values:
eligibility_query_method:
registration_number_type:
confirmation_required:
confirmation_channel:
photo_required:
payment_required:
physical_handoff_required:
admission_ticket_delivery:
score_query_channel:
appeal_or_objection_channel:
credential_registry_dependency_evidenced:
archiveable_public_components:
non_archiveable_private_state:
known_browser_encoding_constraints:
observed_success_evidence:
observed_failure_evidence:
```

### `eligibility_state_values`

只能记录证据真实支持的状态，例如：

```text
submitted
under_review
passed_preliminary_review
failed_preliminary_review
confirmed
invalid_due_to_no_confirmation
```

不要把今天系统中的状态名倒推给 2004 年。

### `credential_registry_dependency_evidenced`

建议值：

```text
none_observed
manual_document_check
public_query_available_but_integration_unknown
explicit_system_integration
```

没有接口证据时默认不要写 `explicit_system_integration`。

---

## 12. 新的硬规则

### 12.1 `public rule ≠ applicant-specific adjudication`

公告说“符合 X 条件可以报考”，不证明某个具体报考者被系统/审核员判为符合。

### 12.2 `submitted ≠ eligible`

2003 年中央招考统计本身已经把网上报名与通过审核分开。

### 12.3 `eligible ≠ confirmed`

一些历史流程在资格审查通过以后仍要求缴费、照片、网上或现场确认。

### 12.4 `online registration ≠ end-to-end online process`

2005 年硕士招生全国网报以后仍有现场确认；2005 年中央公务员考试也因地区不同同时存在网上和现场确认。

### 12.5 `one-position rule ≠ one-life-route rule`

“一次招考限报一个职位”不能推断报考者没有参加其他考试/招聘。

### 12.6 `credential database exists ≠ automatic backend verification`

学历可网上查询不证明具体报名系统调用了该库。

### 12.7 `current help page ≠ historical workflow`

今天的研招网、人事考试网操作步骤不能倒推 2004/2005 版本。必须按年度找同期规则或 capture。

### 12.8 `archived success path ≠ ordinary user completion rate`

官方说明往往只画顺利完成路径；失败、忘记确认、系统打不开、材料被退回等需要独立用户/运维证据。

---

## 13. 与 `how-people-lived` 的交叉链接

本说明提供的是旧网证据边界。

生活史侧对应的新问题是：

> 当网上报名、状态查询和电子记录降低了一部分申请摩擦以后，一个普通毕业生是否开始更容易同时维持考研、公考、事业单位、企业招聘等多个候选未来？

对应研究包：

`tmzncty/how-people-lived/topics/application-portfolios-eligibility-horizons-and-route-multiplexing-china-2003-2025.zh-CN.md`

这里不把 2023–2025 当作旧网 scope，只把 2003–2015 的技术/制度 artifact 提供给生活史使用。

---

## 14. 已证实 / 高概率 / 不知道

### 已证实

- 2003–2005 年硕士研究生报名经历了部分单位网报试点到全国网报的快速变化，同时至少在 2005 年招生中仍保留现场确认。
- 2003 年中央公务员招考已经区分“互联网报名”和“审核通过”人数。
- 2005–2006 年的公务员招考材料显示网上提交、资格审查、确认、照片/缴费、准考证等是分离步骤。
- 2001 年后中国存在高等教育学历电子注册与网上查询制度。

### 高概率但必须逐案验证

- 大量真实申请状态只存在于数据库/session/用户账号中，传统 Web archive 很难完整保存。
- 早期报名系统往往跨多个 host、地方考试机构和线下确认点，单一 host 的 capture 不足以重建完整体验。
- 旧网保存因此更容易留下“机会结构”，不容易留下普通人的完整申请组合。

### 不知道

- 2003–2006 若干原始报名 CGI/JSP/ASP 页目前还能否获得可验证 capture；本轮没有用可提交的历史 session 实际重放。
- 具体年份各系统浏览器版本、JS 校验、编码和上传控件的完整兼容要求。
- 哪些招考后台当时已经与学历电子注册数据建立自动接口。
- 普通用户在失败、资格被拒、忘记确认时实际看见的错误页/状态页长什么样。
- 不同 archive 对登录前表单、公开职位表、JS/CSS 和下载文件的保存差异有多大。

---

## 15. 下一步考古任务

后续如果继续这一对象，不应再增加泛泛的“某年开始网上报名”新闻，而应优先寻找：

1. 2003–2006 `chinayz.com.cn` / 早期研招网的实际 Wayback capture；
2. 2004–2006 中央公务员报名入口、资格查询、确认、准考证说明页的历史 capture；
3. 同期考生教程/论坛帖，用于还原失败路径、浏览器要求和现场/网上切换；
4. 至少一个年度的 public notice → form → confirmation instruction → result query URL 关系图；
5. 明确记录哪些页面只剩媒体截图/转述，不能假装已经拿到原始页面。

如果只能找到公告而无法找到申请表/状态页面，应把它记录成 **application-state archive gap**，而不是用今天的界面补图。

---

## AI-assisted research note

本说明初稿由 OpenAI GPT-5.6 Sol 辅助整理。所有关键 claim 依据上列同期官方或近同时代来源；D 级推断均以边界规则形式显式标出，不把现代复原当作 historical original。