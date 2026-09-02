# OPPORTUNITY_VERIFICATION_AND_REPUTATION_WARNING_2004_2008.md

## 目的

本文件配套 `how-people-lived` 的生活史专题：

- <https://github.com/tmzncty/how-people-lived/blob/main/topics/verify-before-travel-and-opportunity-trust-infrastructure-2004-2008.zh-CN.md>

本仓保持约 1995–2015 中文互联网考古 scope。本文件不把招聘诈骗史扩张成一般社会史，而只处理一个旧网证据问题：

> 当 2000 年代招聘信息、公司口碑、求职警告和“黑名单”进入网站、校园 BBS 与论坛以后，今天的研究者怎样区分“当时存在一个信誉信号”与“该指控已经被证明为真”？

前两份招聘方法文档已经建立：

- [RECRUITMENT_LISTING_AND_RESUME_LIFECYCLE_1999_2004.md](RECRUITMENT_LISTING_AND_RESUME_LIFECYCLE_1999_2004.md)
- [RECRUITMENT_PROCESS_STAGE_AND_CHANNEL_SWITCHING_2003_2006.md](RECRUITMENT_PROCESS_STAGE_AND_CHANNEL_SWITCHING_2003_2006.md)

本文件在 process graph 中增加一个经常被忽略的阶段：

```text
discovery
→ employer research
→ opportunity verification
→ application / screening
→ travel / onsite verification
→ offer / contract / onboarding
```

`opportunity verification` 可以发生在申请前、申请后或收到邀约以后；它不是固定单点，而是“在支付更高现实成本以前，尝试确认远方机会是否值得继续”。

---

## 1. 第一条硬规则：archived listing ≠ verified opportunity

旧招聘页被 archive 保存，只能证明某个历史时点存在一条公开信息。

它不能自动证明：

- 招聘单位是页面声称的主体；
- 招聘会取得了当时所需审批；
- 联系邮箱/电话确属该企业；
- 岗位当时确实空缺；
- 薪资和条件真实；
- 后续面试、录用或劳动关系真的发生。

2006 年武汉一场毕业生招聘会提供了明确反例：同期报道称约 6000 名学生通过网络获知活动并到场，其中不少人从外地赶来；事后有关部门调查称活动未登记、未获审批，现场实际招聘单位与此前宣传严重不符。

来源：

- 中国教育和科研计算机网，2006-03-17，《警惕非法招聘诈骗大学生钱财》：<https://www.edu.cn/jiao_yu_ping_lun_1070/20060317/t20060317_167661.shtml>

证据等级：**B — 同时代 institution-hosted 报道，含部门调查结果。**

因此 archive 中“有职位页 / 有招聘会专题”首先是 **publication evidence**，不是 **opportunity validation evidence**。

---

## 2. 第二条硬规则：archived blacklist entry ≠ verified misconduct

2006 年同期报道记录，湖南、上海等地高校 BBS 和独立网站已经出现求职“黑名单”、受骗帖和公司风险询问；部分帖子被跨校转载、长期置顶或由版主汇总。

来源：

- 当代商报 / 红网 / 新浪，2006-03-20，《公司招聘黑名单惊现网络 长沙四公司榜上有名》：<https://news.sina.com.cn/c/edu/2006-03-20/08498481759s.shtml>
- 新华视点 / 四川在线 / 新浪，2006-03-22，《“实战”暗藏玄机 求职遭遇“忽悠”》：<https://news.sina.com.cn/c/edu/2006-03-22/13338502496s.shtml>
- 新闻晚报 / 新浪科技，2006-12-05，《大学生网上讨伐黑公司》：<https://tech.sina.com.cn/i/2006-12-05/13121272392.shtml>

证据等级：**B。**

这些材料非常适合研究：

- 当时求职者如何判断陌生企业；
- 校园 BBS 是否承担同伴预警；
- 风险经验怎样跨年级、跨学校传播；
- 某个企业在某一时点是否已经出现负面声誉信号。

但它们不能单独证明对应指控为真。

必须固定以下关系：

> **warning exists ≠ allegation is true**

同样：

> **subject rebuttal exists ≠ allegation is false**

研究单位应从“黑公司名单”改成 **reputation signal（声誉信号）**。

---

## 3. Reputation artifact 的最小字段

建议任何招聘口碑 / 警告 / 黑名单 / 回应 artifact 至少记录：

```yaml
reputation_signal:
  signal_id:
  signal_type: warning | blacklist | complaint | rebuttal | official_record | unknown
  original_url:
  capture_url:
  capture_datetime:
  assertion_time:
  platform_or_site:
  author_role: applicant | student | moderator | media | employer | regulator | unknown
  subject_name_as_displayed:
  subject_identity_status: confirmed | ambiguous | unknown
  allegation_summary:
  first_person_experience: true | false | unknown
  evidence_grade: A | B | C | D
  confidence:
```

其中 `subject_name_as_displayed` 只保留研究所需最低信息。普通企业联系人、个人手机号、QQ、住址等不应因“考古”而重新大规模公开。

---

## 4. 指控本身必须与核验状态分栏

推荐额外建立：

```yaml
verification:
  platform_review_claimed: true | false | unknown
  organizer_license_checked: true | false | unknown
  official_approval_checked: true | false | unknown
  employer_identity_cross_channel: confirmed | partial | failed | unknown
  public_phone_or_address_match: confirmed | partial | failed | unknown
  independent_evidence_families:
  official_record_found: true | false | unknown
  subject_response_found: true | false | unknown
  verification_status: confirmed | partially_confirmed | contested | unverified | unknown
```

注意：

- `platform_review_claimed: true` 只证明平台声称进行了审核；
- `official_approval_checked: true` 只证明某活动/机构在特定时间点有对应审批证据；
- 这些字段都不能升级为“未来所有招聘行为可信”。

---

## 5. “平台已审核”是一个历史 claim，不是研究者结论

2000 年代招聘网站和转载页常出现类似“已审核”“由某招聘平台审核并发布”等文字。

旧网考古必须把它拆成：

```text
historical platform claim:
  当时页面显示平台声称已审核

researcher conclusion:
  我们是否能从独立证据确认审核范围、流程与对象
```

因此：

> **review badge exists ≠ employer objectively legitimate**

只有当原始平台帮助页、企业发布规则、资质提交要求或内部流程材料可定位时，才能进一步讨论“审核”具体意味着什么。

---

## 6. 2007 官方规则提供了制度化核验基线

2007 年人事部《关于规范人才招聘会管理改进人才招聘服务的通知》要求招聘会举办方具备相应资质、依法审批，并在会前严格审查参会单位资格与招聘信息，防止“只招不聘”和虚假招聘；同时要求建立招聘广告与供求信息审查制度，公开合法中介、已审批招聘会、举办单位和举报投诉电话，并提出建立权威人才招聘信息服务平台、保证信息真实可靠。

来源：

- 人事部，国人部发〔2007〕94号，深圳市政府转载：<https://www.sz.gov.cn/cn/xxgk/zfxxgj/tzgg/content/post_1613558.html>

证据等级：**A — 同时代官方规范性文件。**

它可以作为旧网页核验字段的制度背景，但必须避免两种错误：

1. **rule exists ≠ rule fully enforced**；
2. **approved organizer ≠ every advertised job later proved genuine**。

法规最适合证明：在 2007 年，哪些主体被正式要求承担哪些审核责任。

---

## 7. 从“职位网页”到“信任路径图”

一次招聘考古不要只画 communication workflow，还应画 trust workflow。

例如：

```text
招聘网站看到岗位
↓
检查公司完整名称
↓
搜索校园 BBS / 论坛旧帖
↓
出现负面声誉信号
↓
打企业公开电话 / 问学校就业中心
↓
查招聘会批准信息
↓
决定继续 / 放弃 / 仍不确定
```

推荐结构：

```yaml
trust_path:
  - step: discovery
    channel: recruitment_site
    result: listing_found

  - step: peer_search
    channel: campus_bbs
    result: warning_found
    historical_effect: possible_deterrence

  - step: independent_confirmation
    channel: school_or_official_source
    result: confirmed | failed | unknown

  - step: decision
    result: continue | abandon | unknown
```

但 `historical_effect` 只有在用户同期材料明确说明“因为看见警告所以没去 / 改变决定”时才能写 `confirmed`。否则最多是 `possible`。

---

## 8. 多个 URL 不等于多个独立信誉来源

黑名单和求职警告特别容易形成转载链：

```text
原始 BBS 帖
→ 另一学校 BBS 转载
→ 新闻报道摘录
→ 门户再转载
→ 后来怀旧文章引用新闻
```

五个 URL 可能只有一个原始 assertion。

因此每条声誉信号应记录：

```yaml
provenance:
  probable_origin:
  repost_of:
  same_evidence_family_as:
  independent_confirmation:
```

如果无法找到原帖，只能说明“同期媒体记录当时存在该帖/名单”，不能重建其全部原始内容。

---

## 9. Archive 的特殊偏差：指控与反驳可能不对称保存

声誉材料有一种比普通网页更危险的 archive bias。

可能出现：

```text
2006-03-01 指控帖被抓到
2006-03-03 企业回应没有被抓到
2006-03-05 版主修正标题没有被抓到
2006-03-08 原帖删除
```

今天打开 archive，只会看见第一状态。

反方向也可能发生：

```text
原始投诉已删
→ 新闻只剩“某公司回应”
```

因此推荐：

```yaml
preservation:
  accusation_capture: present | absent | unknown
  rebuttal_capture: present | absent | unknown
  moderator_update_capture: present | absent | unknown
  deletion_observed: true | false | unknown
  capture_sequence_complete: true | false | unknown
  archive_asymmetry: low | medium | high | unknown
```

并固定规则：

> **one surviving state ≠ final historical state**

---

## 10. 不能把今天仍能搜索到的黑名单做成“历史坏公司数据库”

这既是证据问题，也是隐私/名誉风险。

本仓若研究 2000 年代 BBS 求职警告，应优先保存：

- 平台/版面名称；
- 日期；
- URL/capture；
- 信号类型；
- 抽象后的风险类别；
- 是否出现反驳或独立确认；
- 对当时用户判断流程的意义。

通常不需要：

- 把几十家历史被指控企业重新列成名单；
- 重新公开普通发帖者昵称、QQ、手机号；
- 复制完整指控文本；
- 从 archive 页面直接给今天仍存在的主体贴永久标签。

研究目标是重建 **how trust was assessed**，不是替历史论坛继续执行惩罚。

---

## 11. 同伴预警可以证明平台功能被“生活化”，但不能证明代表性

2006 年多篇同期报道记录学生会：

- 在校园 BBS 求职版询问某单位；
- 查“黑名单”；
- 补充自己的经历；
- 把名单转到其他学校；
- 由版主汇总、置顶。

这足以支持：

> 校园 BBS 在至少一些毕业生群体中被用作招聘信誉查询与风险传播工具。

但不能推出：

- 所有学生都会查；
- 非大学生求职者拥有同样渠道；
- BBS 用户代表全部青年劳动者；
- 被频繁讨论的企业就是最常见风险来源。

这里存在强烈的 **visibility bias**：大学生、互联网用户、愿意发帖者和冲突性经历更容易留下记录。

---

## 12. 新增 process stage：opportunity_verification

在 [RECRUITMENT_PROCESS_STAGE_AND_CHANNEL_SWITCHING_2003_2006.md](RECRUITMENT_PROCESS_STAGE_AND_CHANNEL_SWITCHING_2003_2006.md) 的 schema 基础上，建议加：

```yaml
recruitment_process:
  discovery:
  employer_research:
  opportunity_verification:
    source_provenance_check:
    employer_identity_check:
    organizer_authorization_check:
    peer_reputation_check:
    cross_channel_confirmation:
    verification_result:
  application:
  initial_screening:
  test:
  interview_1:
  physical_travel:
  credential_verification:
  offer:
  contract:
  onboarding:
```

这个阶段可以循环发生。例如收到一封陌生公司的面试邮件后，求职者才去 BBS 搜公司名。

---

## 13. 对 archive claim language 的推荐措辞

### 可以写

> “2006 年某高校 BBS 的同期报道记录，学生曾用该版面询问某些招聘单位并交换风险经验。”

> “该 capture 证明当时页面存在一条针对某主体的负面声誉信号；本轮未找到独立材料确认指控本身。”

> “2007 年官方文件要求招聘会举办方审查参会单位资格与招聘信息。”

### 不应写

> “某公司 2006 年就是骗子。”

> “这个名单证明这些公司都有问题。”

> “招聘网站写了审核，所以这个职位一定真实。”

> “政府规定要求审核，所以虚假招聘从此得到解决。”

---

## 14. 证据等级建议

| artifact | 默认等级 | 可证明 | 不可自动证明 |
|---|---|---|---|
| 同时代 BBS 原帖/capture | A | 当时该 assertion 存在 | assertion 为真 |
| 同时代媒体观察 BBS 黑名单 | B | 当时媒体观察到相关使用模式 | 原帖全部细节、代表性 |
| 平台“已审核”标签/帮助页 | A（平台自身陈述） | 平台当时这样标注/声明 | 审核有效性 |
| 政府批准名单/规范文件 | A | 制度要求或某次批准状态 | 实际执行完整、后续无风险 |
| 企业同期回应 | A/B（按来源） | 企业当时提出反驳/说明 | 自动推翻原指控 |
| 多年后“十大黑公司回忆” | C | 后来的记忆/叙事 | 2006 年精确事实 |
| 研究者按旧帖重建公司风险 | D | 研究者推断 | historical verdict |

---

## 15. 海外比较放在 how-people-lived，本仓只保留方法链接

配套生活史专题比较了 2003 年美国 Monster.com 对虚假职位收集求职者个人信息的安全警告，以及 FTC 要求通过官方渠道核实工作机会的消费者保护材料。

这些海外材料说明“远程陌生机会需要核验”不是中国独有机制。但本仓主对象仍是 1995–2015 中文旧网，因此：

- 全球互联网史与跨国生活史解释放在 `how-people-lived`；
- 本仓只借此验证方法具有可迁移性；
- 不把 `old-web-archaeology` 扩成全球招聘网站史。

---

## 16. 已证实 / 高概率 / 不知道

### 已证实

- 2006 年同期报道记录多个高校 BBS 与独立站存在求职警告、“黑名单”和公司询问。
- 这些名单存在转载、汇总、置顶和用户补充。
- 同期报道同时记录企业反驳、法律风险和信息真实性争议。
- 2007 年官方文件明确要求招聘会主办方审查单位资格和招聘信息，并公开合法机构、批准活动与举报渠道。
- 网络发布的招聘信息可以触发真实跨城移动，因此网页可信度与现实成本直接相关。

### 高概率

- BBS 的可搜索性让上一届/陌生同学的经验能够成为下一位求职者的弱关系风险信息。
- 公开 archive 对职位页、新闻和公开投诉的保存远强于电话确认、学校内部核验、私信以及“我看完后决定不去”的无事件结果。

### 不知道

- 当时普通求职者实际有多大比例会先搜企业口碑。
- 民间黑名单中具体 allegation 的准确率。
- 大型招聘平台对企业审核的实际工作流及平台间差异。
- 一条警告被看到后实际改变了多少人的出行/求职决定。
- 非大学生群体怎样通过网吧、地方论坛、老乡网络或电话完成类似核验。

---

## 17. 本轮方法增量

此前招聘考古重点回答：

> 页面上有什么职位？简历怎样提交？流程怎样跨 Web、电话、QQ 和现场？

本文件增加：

> **一个历史用户凭什么相信这条机会值得继续？**

因此今后的招聘/求职旧网页案例，需要至少同时建两张图：

```text
process graph：事情怎样发生
trust graph：为什么当时的人愿意继续相信并付出下一阶段成本
```

最重要的三条边界是：

> **archived listing ≠ verified opportunity**

> **warning exists ≠ allegation is true**

> **one surviving archive state ≠ final historical state**

这三条如果不固定下来，旧网考古很容易把一个 2006 年保存下来的帖子，从“当时有人这样说”错误升级成“历史已经证明事实如此”。
