# ABANDONED_APPLICATIONS_AND_NEGATIVE_STATE_SURVIVAL_2007_2015

## Scope

本说明研究约 2007–2015 中文互联网中招生、招考、资格考试和公共招聘系统里一类特别容易被旧网考古误读的对象：**没有走到最后的申请状态**。

仓库已经有：

- `APPLICATION_STATE_ELIGIBILITY_AND_ROUTE_PORTFOLIO_2003_2015.md`：申请、资格审核、确认、准考证等状态链；
- `TRANSACTIONAL_TRAVEL_WEB_AND_REVOCABLE_BOOKING_ARTIFACTS_2011_2015.md`：订单、支付、库存与撤销；

本文件不重复“系统有状态”。它进一步问：

> **当一条申请路线终止时，旧网页究竟保存的是系统状态、机构判断、用户行为，还是用户动机？**

尤其关注：

- 未确认；
- 未缴费；
- 未上传照片；
- incomplete application；
- 缺考/no-show；
- 主动撤回；
- 资格过期；
- 进入面试后放弃；
- 因另一条路线成功而停止当前申请。

本仓仍保持约 1995–2015 中文旧网 scope。2017、2019、2022、2023 的生活史比较放在 `tmzncty/how-people-lived`，这里只在结论处交叉链接。

---

## 1. 第一条硬规则：`system abandonment label ≠ human intention`

2007 年浙江省 2008 年公务员招考的同期说明明确提醒，通过资格初审后仍需上传照片、完成缴费确认；未按时完成者，制度上“视为自动放弃报考”。

这是一个非常重要的旧网语义问题。

系统可以观察到：

```text
eligibility_passed
→ confirmation_deadline_passed
→ photo/payment incomplete
→ application invalid / deemed abandoned
```

但系统通常看不到：

```text
why?
```

可能的真实原因包括：

- 本人主动改变主意；
- 已找到工作；
- 转去考研；
- 竞争太激烈；
- 忘记截止时间；
- 不会网上支付；
- 银行卡/网银失败；
- 照片规格错误；
- 网络故障；
- 交通/住宿成本太高；
- 家庭突发事件。

因此数据库或公告中的 `自动放弃` 首先是一个**流程归类**，不是一条心理自述。

### 证据

- **B/A-near-primary（同期报考提醒，转述官方公告）**：杭州日报/新浪教育，2007-11-13，《08年浙江省公务员报考工作11月15日结束》。文中明确说明资格初审通过后仍须上传照片、缴费确认，未按时完成“视为自动放弃报考”。  
  <https://edu.sina.com.cn/official/2007-11-13/1110107824.shtml>
- **A/B（同期政府/组织部门公告保存）**：温州 2008 年公务员招考公告，包含报名、资格、后续体检/考察/报到等状态及逾期取消资格规则。  
  <https://www.wzdj.gov.cn/system/2007/11/02/100431672.shtml>

### 推荐写法

可以写：

> `未按期完成缴费确认者在该年度规则下被系统/制度视为放弃报考。`

不能只依据系统状态写：

> `该用户不想考公务员了。`

---

## 2. “弃考率”至少有三个不同分母

旧报刊和培训页面经常出现“报名人数”“弃考率”“参考率”，但它们可能对应不同节点：

```text
registered
→ passed_preliminary_review
→ confirmed / paid
→ printed_ticket
→ physically_attended
```

2007 年浙江材料是一个很清楚的例子：第一阶段注册 25.7 万余人；缴费确认 18.3 万余人；同期报道又说，到了真正笔试仍可能继续出现已确认者缺考。

同一篇文章如果说“弃考 22%”，读者很容易把它理解为：

```text
22% of everyone who once clicked register consciously decided not to take the exam
```

实际并不能这样推。

### 证据

- **B（同期新闻，引用省公务员考试录用系统统计）**：《浙江日报》，2007-12-06，《浙江公务员弃考率达22% 报考热中有“虚火”》。  
  <https://edu.sina.cn/sa/2007-12-06/detail-ikftssap7780897.d.html>

报道同时提供了一名应届毕业生主动放弃的第一人称，但这个个案只能解释**一种可能机制**，不能替 5.2 万人的聚合差值统一赋予动机。

### 建议字段

```yaml
population_stage:
  # registered | eligibility_passed | confirmed | ticket_issued | attended | finished
population_count:
denominator_stage:
transition_to_stage:
transition_count:
reported_attrition_rate:
rate_recomputed_by_researcher:
individual_motive_evidence_present:
```

核心规则：

> **count drop between states ≠ one cause**

---

## 3. `no-show` 是事件，`withdrawal` 是动作，`rejection` 是裁决

旧网页研究必须至少分开三类负状态。

### 3.1 no-show / absent

可观察事实：应该出现的人没有出现。

它可以发生在：

- 笔试；
- 面试；
- 现场确认；
- 体检；
- 报到。

没有额外证据时，只能编码：

```yaml
observed_event: no_show
motive: unknown
```

### 3.2 withdrawal / abandonment

需要有用户动作或制度明确记录，例如：

- 用户点击撤回；
- 明确来信声明放弃；
- 同期采访说本人决定不去；
- 规则把某种超时明确归为“视作放弃”。

最后一种仍然只能写 `system_classified_as_abandoned`，不能升级成 `intentional_withdrawal`。

### 3.3 rejection / ineligibility

这是机构作出的裁决，例如：

- 专业不符；
- 学历不足；
- 资格初审未通过；
- 体检不合格；
- 未被录取。

它和用户主动退出完全不同。

因此：

> **no-show ≠ withdrawn ≠ rejected**

---

## 4. 2008 四川事业单位考试：聚合缺考可以观察，但个人原因不能从空座位读出来

2008 年四川省属事业单位公开招聘中，18,441 人取得考试资格，14,394 人实际参考，4,047 人缺考，缺考率 21.9%。同期负责人认为，一部分考生同时报多个岗位/考试，权衡后会放弃某些考试集中准备更有把握的一项。

另一篇同日现场稿又记录：

- 有考试日期冲突；
- 有考生在贴吧讨论考点过远；
- 有人因为交通不便而萌生临时放弃。

这是一个很好的**多因同状态**案例：最终数据库里都可能只是 `absent`，但背后至少有策略性修枝、时间冲突和地理摩擦。

### 证据

- **B（同期现场报道）**：四川在线—天府早报，2008-12-07，《1.4万人赶考 1个饭碗10人抢》。  
  <https://news.sina.com.cn/c/2008-12-07/073914842059s.shtml>
- **B（同期独立稿件，同一考试）**：成都商报，2008-12-07，《省属事业单位公招 4000人缺考》。  
  <https://news.sina.com.cn/c/2008-12-07/040614841341s.shtml>

### 推理边界

可以说：

> `该次考试存在 4,047 个已取得资格但未实际参考的记录；同期材料显示其中至少一部分是多路线权衡或交通/日程摩擦。`

不能说：

> `4,047 人都因为觉得公务员/事业单位不值得而主动弃考。`

---

## 5. 网上支付把“是否继续一条人生路线”绑定到跨系统交易状态

2000 年代后期报名系统的一项关键变化，是申请是否继续有效越来越依赖：

```text
application system
→ photo validation
→ bank/payment gateway
→ callback/reconciliation
→ registration status update
```

这使“未缴费”变成一个尤其危险的历史标签。

安徽省自考办 2007–2008 年的同期网络报名问题解答明确记录过：

- 报名系统可能没有显示成功，但银行卡已经扣款；
- 用户需要等到次日再查询结果；
- 重复扣款或“钱已划走但报名未成功”会以后退款；
- 2008 年解答甚至明确提醒，在确认状态前不要反复刷新或重新报名。

这证明：

> **displayed state ≠ reconciled backend state**

以及：

> **money debited ≠ effective application**

这不仅是支付工程问题。它会直接决定一个人能不能坐进考场。

### 证据

- **A/B-near-primary（安徽省自考办同期问题解答，经新浪教育保存）**：2007-05-18，《安徽自考办对07年10月网络报名有关问题的解答》。  
  <https://edu.sina.com.cn/zikao/2007-05-18/121883224.html>
- **B/A-near-primary（同期报名 FAQ）**：2008-02-18，《新生报名个人信息填写错误的解决办法》。  
  <https://edu.sina.com.cn/zikao/2008-02-18/1523122818.shtml>

### 对 archive replay 的要求

今天即使能回放一个历史“支付成功”页面，也不能直接推出：

- 后台最终把此人标为报名成功；
- 银行对账已经完成；
- 用户没有随后退款；
- 最终准考证一定生成。

如果只有前端状态，应记录：

```yaml
displayed_state: payment_success
backend_finality_known: false
reconciliation_dependency: true
```

---

## 6. “报名未完成”也可能已经是一段真实生活，而不是无效噪音

传统数据清洗很容易把 incomplete application 当成垃圾：

```text
not completed
→ discard row
```

生活史和旧网考古不能这样做。

一个未完成申请可能已经包含：

- 搜索并比较职位；
- 注册账户；
- 填写身份信息；
- 上传照片；
- 联系家人确认材料；
- 购买复习资料；
- 准备数周；
- 最后因为某一环节停止。

如果研究问题是“普通人当时实际拥有多少种未来”，这些状态正是证据。

海外的 2011 年美国海军学院争议是一个可比较的统计口径反例：学校报告 19,145 份申请，但只有 5,720 份完成全部申请流程。不同学校对 incomplete application 是否进入“申请数”分母的处理并不一致。

该海外材料只用于说明**状态口径是跨国通用的考古问题**，不纳入本仓中文旧网对象库。

- Daniel de Vise, *The Washington Post*, 2011-12-27, “Naval Academy, other colleges differ on when an application counts.”  
  <https://www.washingtonpost.com/local/education/naval-academy-other-colleges-at-odds-on-when-an-application-counts/2011/12/22/gIQAB4DBLP_story.html>

因此：

> **incomplete ≠ historically irrelevant**

---

## 7. “资格通过”仍然不是“承诺继续”

已有 application-state 文档已经规定：

```text
submitted ≠ eligible
eligible ≠ confirmed
confirmed ≠ attended
attended ≠ admitted
```

本轮补充的关键是：**每一次向后转移都可能有主动性不同的死亡机制。**

建议把状态和死亡原因分两个字段，不要把它们揉成一个枚举：

```yaml
state_at_last_observation: eligibility_passed
next_expected_state: payment_confirmed
transition_observed: false
termination_classification: system_deemed_abandoned
human_motive: unknown
```

而如果同期采访明确说“因为找到工作所以不去考试”，才可以另记：

```yaml
human_motive: substituted_by_job_offer
motive_evidence_grade: B
```

这可以防止最常见的错误：从行政术语“弃考/自动放弃”直接制造一个心理故事。

---

## 8. 负状态比成功状态更容易“无页面化”

旧网 archive 对失败/撤回有一种特殊的不对称。

### 成功状态常有公开 artifact

- 公示名单；
- 录取通知；
- 成绩榜；
- 拟录用名单；
- 招生新闻；
- 用户后来在个人主页写“我考上了”。

### 路线死亡通常没有公开 artifact

- 登录后的一次“未通过”；
- 过了截止时间后状态自动失效；
- 用户不再登录；
- 没有去考场；
- 面试通知没有回应；
- 用户收到工作 offer 后再也没打开报名站；
- 支付失败后没有重新支付。

这些状态甚至可能**从来没有独立 URL**。它们存在于数据库行、session、后台任务或物理考场，而不是可被 crawler 访问的静态页面。

我把这种现象称为：

## negative-state survival gap（负状态存续缺口）

它意味着：

> **archive survival is structurally biased toward states that become public artifacts.**

并进一步造成：

> **success has URLs; quiet abandonment often does not.**

---

## 9. 意向文物可以比改主意的那一刻活得更久

另一种偏差来自个人主页、博客、BBS。

一个用户可能在 9 月写：

```text
“今年准备考研。”
```

这篇文章被 archive 抓到。

11 月他因为找到工作而放弃，但这个决定可能：

- 只发生在 QQ 私聊；
- 只告诉室友；
- 根本没有发帖；
- 发过，但那一页没有被抓到；
- 原帖后来删除。

几十年后，研究者只看到“我要考研”，就很容易把它写成一个持续到考试的稳定意向。

因此新增：

## intention–revision survival asymmetry（意向—修正存续不对称）

硬规则：

> **surviving intention artifact ≠ intention remained unchanged until outcome**

如果只有一篇早期计划帖，应写：

```yaml
intention_observed_at: 2008-09-xx
later_revision_evidence: none_found
outcome: unknown
```

不能写成：

```yaml
route: graduate_school
final_decision: graduate_school
```

---

## 10. 负状态的 provenance 要比正状态更细

建议把终止类 evidence 分为：

### A1 — 官方规则定义

例如：公告明确规定未缴费“视为自动放弃”。

它证明**规则如何分类**，不证明某个用户为什么没缴费。

### A2 — 系统/后台状态

例如可验证的历史状态截图、导出记录或原始数据库文档。

它证明**系统记了什么**，仍未必证明心理动机。

### B1 — 同期个人自述

例如受访者说“我找到工作，所以决定不参加考研”。

它是较强的 motive evidence，但仍是个人材料。

### B2 — 同期现场观察

例如记者看到一个考场大量空位，或某贴吧有人讨论“考点太远不想去了”。

它能证明现象/可能机制，但不能把单条帖子推给所有缺考者。

### C — 后来回忆

多年后说“当年其实没想考”，适合研究记忆，不应覆盖当时已有的报名、缴费和备考事实。

### D — 研究者推断

例如：

```text
no exam result found
→ probably did not attend
```

如果没有更直接证据，只能显式标 D，且必须保留其他解释。

---

## 11. 推荐数据结构

```yaml
service_name:
application_cycle:
artifact_date:
applicant_scope: aggregate | individual_anonymized

state_at_observation:
state_definition_source:
state_actor: applicant | institution | system | unknown
state_public_or_authenticated:
state_url_archivable:

previous_state:
next_expected_state:
transition_observed:
transition_timestamp:

termination_observed:
termination_system_label:
termination_class:
  # rejected | no_show | withdrawn | expired | incomplete | unknown
human_motive:
human_motive_evidence_grade:
substitute_route_observed:

population_count:
population_stage:
denominator_stage:
reported_attrition_rate:

payment_dependency:
external_gateway_dependency:
reconciliation_dependency:
displayed_state:
backend_finality_known:

intention_artifact_date:
revision_artifact_found:
outcome_artifact_found:

archive_source:
original_url:
capture_datetime:
archive_gap:
privacy_minimized: true
```

### 不要保存普通人的真实报名号/证件号

本仓需要的是字段角色和状态语义，不需要复原某个普通历史考生的身份证号、报名序号、手机号或银行卡信息。

---

## 12. 新的硬规则

### 12.1 `system-classified abandonment ≠ intentional abandonment`

“未按时缴费视为自动放弃”是系统/制度分类，不是用户心理材料。

### 12.2 `no-show ≠ rejection`

缺考的人可能已经完全符合资格，只是没有到场。

### 12.3 `withdrawn ≠ ineligible`

主动撤回不代表制度不允许继续。

### 12.4 `not confirmed ≠ never intended`

一个人可能认真报名、备考，最后才在确认环节退出。

### 12.5 `qualified ≠ committed`

资格审查通过只说明制度暂时允许继续，不说明本人把这条路线列为第一选择。

### 12.6 `count drop ≠ one cause`

两个状态之间少了多少人，不能只用一个采访个案解释。

### 12.7 `displayed payment state ≠ reconciled final state`

银行/支付网关、报名系统与后台对账可能短暂不一致。

### 12.8 `surviving intention ≠ unchanged intention`

一篇“我要考研/我要考公”的旧博客不能自动代表最终决策。

### 12.9 `final public list ≠ complete historical choice set`

最终录取/录用名单只保存实现路线，不能用于反推普通人的完整申请组合。

---

## 13. 与现有文档的关系

### 对 `APPLICATION_STATE_ELIGIBILITY_AND_ROUTE_PORTFOLIO_2003_2015.md`

原文回答：申请系统有哪些状态，资格如何被制度裁决。

本文件回答：**状态怎样终止，终止标签怎样被误读成人的动机。**

### 对 `TRANSACTIONAL_TRAVEL_WEB_AND_REVOCABLE_BOOKING_ARTIFACTS_2011_2015.md`

原文回答：交易、支付、库存和撤销如何组成动态 Web 工作流。

本文件补充：**报名/资格系统中的支付失败不仅是 transaction failure，也可能直接使一条教育/就业未来失效。**

### 对 `QUOTATION_SURVIVAL_AND_MEDIA_RECONTEXTUALIZATION_2009_2010.md`

原文回答：论坛内容怎样因媒体引用而存活，却失去原平台语境。

本文件补充：**人的最初意向也可能被保存，而后来改主意的那一步没有进入 archive。**

---

## 14. 对“历史可见性”的新结论

旧网考古过去很容易围绕“留下了什么页面”展开。本轮进一步表明，有些最重要的生活事实恰恰是**没有产生页面的状态转换**：

```text
报名了
→ 没再缴费

确认了
→ 没去考试

通过笔试
→ 没去面试

拿到 offer
→ 没去报到
```

如果只看幸存网页，历史会自动变得比真实生活更线性、更确定，也更像“计划—成功/失败”的二分。

实际的人生工作流更像：

```text
create candidate route
→ spend some cost
→ learn new information
→ compare with other routes
→ continue / defer / silently drop / be rejected / fail to execute
```

因此 `old-web-archaeology` 在研究报名、招考、招聘、教育平台时，应把**终止状态和没有 URL 的状态转换**作为一等研究对象。

---

## 15. 尚未确定

- 2007–2015 是否能找到可公开、可复核、又不侵犯普通用户隐私的登录后“撤回/放弃”历史页面 capture；
- 各年度系统是否真的存在显式 `withdraw` 按钮，还是大多数放弃只能通过“不完成下一步”实现；
- 不同招考系统对 `报名人数`、`确认人数`、`有效报名人数`、`参考人数` 的统计口径是否有稳定 schema；
- 旧 BBS/博客中“先宣布报考、后来宣布放弃”的成对 capture 仍然很少，尚不足以测量 intention–revision survival asymmetry 的规模；
- 支付失败、浏览器兼容、网络拥堵等技术因素在实际路径耗损中占多大比例，目前只有局部 FAQ 和个案，不能量化推广。

---

## 16. 交叉链接

- `APPLICATION_STATE_ELIGIBILITY_AND_ROUTE_PORTFOLIO_2003_2015.md`
- `TRANSACTIONAL_TRAVEL_WEB_AND_REVOCABLE_BOOKING_ARTIFACTS_2011_2015.md`
- `QUOTATION_SURVIVAL_AND_MEDIA_RECONTEXTUALIZATION_2009_2010.md`
- `tmzncty/how-people-lived/topics/application-portfolios-eligibility-horizons-and-route-multiplexing-china-2003-2025.zh-CN.md`
- `tmzncty/how-people-lived/topics/route-attrition-substitution-and-the-lives-not-taken-china-2007-2023.zh-CN.md`

## 本轮结论

最需要写进后续数据合同的一句话是：

> **The last visible state is not the reason the future ended.**

旧网保存下来的最后一个状态，只告诉我们“流程停在哪里”；要解释“为什么这条人生路线停止”，还需要另一条来源链。