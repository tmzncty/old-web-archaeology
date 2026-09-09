# WITKEY_TASK_MARKET_BOUNTY_SUBMISSION_SELECTION_PAYMENT_REPUTATION_AND_WORK_OUTCOME_STATE_GAPS_2004_2015.md

> 范围：约 2004–2015 中文旧网中的“威客”/任务市场、悬赏、竞标、交稿、选稿、结算、评价与工作结果状态
>
> 状态：research note / execution-state model
>
> 日期：2026-09-09
>
> 关联生活史：`tmzncty/how-people-lived/topics/from-second-work-to-witkey-task-markets-digital-piecework-and-modular-livelihood-china-1988-2026.zh-CN.md`

## 0. 为什么这不是再写一遍“网上兼职”

本仓已经有两条很接近、但研究单位不同的旧网劳动线：

- `docs/CAMPUS_PARTTIME_BBS_SHORT_GIGS_SCHEDULE_PAYMENT_AND_OUTCOME_GAPS_2005_2009.md`
- `docs/PART_TIME_JOB_POSTS_BBS_MEDIATION_AND_OFFLINE_EXECUTION_2006_2009.md`

它们已经很好地处理了：

```text
BBS/论坛上看到兼职
→ 电话/QQ/面试
→ 到商场/培训班/家庭/外地现场
→ 实际劳动
→ 现金/转账/纠纷
```

本条目只补其中此前没有单独拆开的另一种拓扑：

> **工作本身能够在 Web 上被编码为一个 task，由陌生劳动者竞标/交稿，客户在线选择结果，平台参与托管支付和声誉记录。**

因此研究单位不是“副业”或“大学生兼职”，而是 **task-market transaction**。

硬边界：

> `online discovery ≠ online execution`
>
> `web task exists ≠ labor was performed ≠ worker was paid`

本条目严格留在约 2004–2015 中文旧网，不扩写 2020s 平台劳动史。后来的劳动条件、社保、风险缓冲和跨国比较主要写入 `how-people-lived`。

---

## 1. Evidence contract

沿用 `docs/METHOD.md`：

- **A**：原始/同时代历史网页、官方帮助页、平台规则、原始软件/接口文档、可验证 archive capture；
- **B**：同期新闻、媒体页面观察、用户教程、记者对任务/平台的操作记录；
- **C**：后来回忆、平台史叙事；
- **D**：研究者状态机、保存偏差、机制推断与复原。

必须继续保持：

```text
platform
≠ site/host
≠ task account
≠ task URL
≠ submission
≠ archive capture
≠ claim
```

平台今天仍有同名帮助页，也不能自动证明 2006 年页面结构、域名、结算规则、浏览器环境或字段完全相同。

---

## 2. 核心对象：一个 task 并不是一张静态招聘广告

普通旧网页很容易让人把任务页理解成：

```text
标题
+ 一段要求
+ 一个价格
```

实际上完整事务至少需要更多对象：

```yaml
client_account:
  identity_state: unknown | weakly_verified | verified
worker_account:
  identity_state: unknown | weakly_verified | verified
  reputation_state: unknown | visible | hidden

task:
  task_id: unknown
  title: unknown
  category: unknown
  budget_or_bounty: unknown
  fee_rule_version: unknown
  published_at: unknown
  deadline: unknown
  task_state: draft | funded | published | judging | awarded | closed | cancelled | disputed | unknown

submission:
  submission_id: unknown
  worker_id: minimized
  submitted_at: unknown
  payload_type: text | image | archive | link | other | unknown
  visibility: public | client_only | unknown
  selection_state: pending | shortlisted | winner | rejected | unknown

payment:
  funding_state: unknown | promised | prepaid | escrowed
  release_state: unknown | released | withheld | disputed
  receipt_state: unknown | worker_received | not_received | unknown

reputation:
  before: unknown
  update_event: unknown
  after: unknown
```

所以一个历史任务页面被 archive 抓到，只能恢复其中一部分。

---

## 3. 2004–2006：K68 把“工作”编码成可公开竞标的数字任务

### Claim OWR-WITKEY-2006-01

**2006-01-02 的同期专业媒体报道直接观察 K68，并把它描述为一种面向数字化工作的悬赏/竞标平台：客户预先付款，发布任务，多人竞标，中标者获得客户出资的一部分，平台抽取佣金。**

来源：

- 《K68让工作全球化》，2006-01-02，《中国电子商务》/新浪
- <https://tech.sina.com.cn/i/2006-01-02/1113809253.shtml>
- 等级：B（同期专业媒体页面观察 + 创办人采访）

报道还称记者在 2005-12-09 看到：

- 669 个任务；
- 悬赏金额 243042 元；
- 507 人次竞标成功；
- 发放赏金 191657 元；
- 20499 名注册工作人员。

这些只能写成“记者当日按平台页面看到/记录的数字”。

不能写成：

- 20499 个独立活跃劳动者；
- 507 个长期从业者；
- 这些人都收到完整赏金；
- K68 代表当时全部中文威客市场。

### Claim OWR-WITKEY-2006-02

**同一报道称 K68 由创办人此前经营的 BBS 社群发展而来，并把平台早期任务用于寻找数据库开发者。**

这给出一个重要的平台形态谱系：

```text
BBS / 社群聚集
→ 需求帖子
→ 规则化悬赏
→ 预付款/佣金
→ 任务平台
```

这不是“论坛自然进化成平台”的普遍规律，但至少在 K68 个案中，BBS 与任务交易层之间存在可观察的组织连续性。

---

## 4. 任务市场第一种核心事务：bounty / contest

早期威客最值得单独恢复的是“多人先做、客户再选”的悬赏/比稿结构。

### 4.1 建议状态机

```text
C0 client drafts brief
→ C1 bounty promised
→ C2 funding/prepayment accepted by platform
→ C3 task published
→ C4 worker discovers task
→ C5 worker decides eligible/worthwhile
→ C6 submission produced
→ C7 submission uploaded
→ C8 deadline reached
→ C9 client/platform judges
→ C10 shortlisted / winner / rejected
→ C11 outcome displayed
→ C12 payment released
→ C13 worker payout received
→ C14 reputation/profile updated
→ C15 possible repeat-client / off-platform continuation
```

旧网考古必须阻止以下跳跃：

> **`task page captured ≠ bounty actually funded`**
>
> **`submission displayed ≠ worker received payment`**
>
> **`winner shown ≠ transaction completed without dispute`**

### 4.2 2006 的 199 人 / 140 方案：公开 Web 容易把“很多劳动”压成一个赢家

2006-10-11《中华人民共和国企业家》经新浪保存的同期报道记录 K68 上一个婚宴小游戏任务：12 天内有 199 人参与，提供 140 种方案，最后由客户选择结果。

来源：

- 《威客网站当道：创意产品网上换现金》，2006-10-11，《中国企业家》/新浪
- <https://tech.sina.com.cn/i/2006-10-11/12131178677.shtml>
- 等级：B（同期媒体观察）

它对 archive 有一个非常重要的启示：

如果最后只剩：

```text
任务页
+ “已中标”标签
+ 一份获奖作品
```

历史就会自动把：

```text
199 人参与
140 个方案
大量未中标准备时间
```

压缩成“一个成功交易”。

新增：

## winner-survival bias / 中标者保存偏差

> **公开平台和 Web archive 系统性地更容易保存赢家、获奖案例和成功页面，而不是所有未中标劳动。**

---

## 5. 2006：注册、投稿、中标、靠平台生活是四个不同状态

### Claim OWR-WITKEY-2006-03

2006-10-27《中国新闻周刊》的同期报道写到，当时 K68 有 44226 名注册用户，但只有 1505 人/次获得收入，累计收入 531199 元；报道本身用这些数字说明竞争激烈。

更重要的是，报道采访到被称为“威客王”的陈怡。她说平台扩大了客户来源，但即使已有名气，靠悬赏平台维持生活也不现实；后来一些客户会直接找她合作。

来源：

- 《威客，能赚钱的网络新“游戏”》，2006-10-27，《中国新闻周刊》
- <https://www.chinanews.com.cn/other/news/2006/10-27/810922.shtml>
- 等级：B（同期媒体采访；平台数字仍按报道口径）

固定硬边界：

> `registered account ≠ active worker`
>
> `active worker ≠ submitted work`
>
> `submitted work ≠ winning work`
>
> `winning once ≠ viable livelihood`

### 5.1 客户可能从平台内状态跳出平台

同年《都市快报》报道设计人员赖明生利用业余时间参与悬赏任务，后来有客户绕过公开任务继续直接找他设计。

来源：

- 《最近流行新职业威客 每天靠上网揭榜赚钱》，2006-09-08，《都市快报》/搜狐
- <https://news.sohu.com/20060908/n245227584.shtml>
- 等级：B（同期成功个案）

这意味着事务可能产生：

```text
public task
→ first win
→ client trusts worker
→ repeat contact
→ platform direct-hire
or
→ off-platform QQ/email/phone
```

因此平台任务页不能告诉我们整个客户关系是否继续存在。

新增：**client-continuity gap**。

---

## 6. 2009：网上接单仍可能只是主业之外的一周劳动

2009-09-18《海峡导报》报道厦门两名设计人员：

- 张金在茶叶包装公司做设计，2008 年注册威客网站后尝试包装设计任务，报道时称自己投过 6 次并累计获得 7000 多元；
- 林中在传媒公司做设计，2008 年注册猪八戒网，投过两次，其中一份北京企业的 LOGO 任务中标，得到 3250 元，并明确说作品花了自己一周业余时间。

来源：

- 《厦门数万“威客”网上“淘金”》，2009-09-18，《海峡导报》/新浪
- <https://news.sina.cn/sa/2009-09-18/detail-ikkntian2022744.d.html>
- 等级：B（同期个人采访）

这组材料对旧网状态有三个价值：

1. **平台账号状态不能替代现实职业状态。** 同一个账号背后的人仍可以有正式主业；
2. **远程交付不能替代工时。** 一张网页上的“一份 LOGO”可能对应一整周晚上；
3. **成功页面天然偏向幸存者。** 报道和平台更容易找到中标设计师，不容易找到花一周后落选的人。

因此：

> `remote task ≠ low-effort task`
>
> `digital object size ≠ labor time`

---

## 7. 2012：从悬赏任务到“直接雇佣”，平台开始保存可累积工作历史

一品威客仍保留一篇内部日期为 2012-11-16 的服务商访谈。受访者“怪猫设计”自称 28 岁、主业为地产设计师，2011 年开始参加威客，第一次中标只有 100 元；后来参与更高赏金任务，并出现客户在一次悬赏合作后直接发起“直接雇佣”的路径。

来源：

- 一品威客，《努力做好作品回报顾客》，页面内部日期 2012-11-16
- <https://m.epwk.com/weike/niu_10576.html>
- 等级：A/B 边界：平台原生存续页面 + 平台筛选成功者访谈

同平台今天仍可访问的帮助内容也说明，若客户想让多人同时完成并比较结果，可使用威客任务；另有 2014-11-20 的平台原生文章讨论赏金、竞标、雇佣/直接雇佣等任务与收费规则。

来源：

- 一品威客帮助页，内部日期 2012-07-11；
- 一品威客平台文章，2014-11-20。

这些材料可以支持：

- 平台在 2012–2014 至少已经把“悬赏/多人结果”和“直接雇佣/其他交易模式”作为不同产品路径；
- 一次任务结果可以参与下一次客户筛选。

但不能直接支持：

- 今天看到的整个页面 shell 就是 2012 HTML；
- 今日导航、CSS、登录状态、推荐模块与 2012 相同；
- “优秀服务商”个案代表普通任务参与者。

新增：

## platform-held work history / 平台托管工作历史

```text
historical win
→ profile / case / reputation
→ next client observes it
→ future work probability changes
```

这是一种新的职业记录层，但它的长期可携带性取决于平台是否存活、账号是否仍可访问、评价规则是否改变。

---

## 8. 除 contest 外，还要区分至少三套不同状态机

到了 2010s，同一平台或同类平台已经不应只用“悬赏”一种模型解释。

### 8.1 project / bid

```text
P0 client publishes requirement/budget
→ P1 workers submit bids / proposals
→ P2 client chooses worker
→ P3 funding/escrow state
→ P4 worker performs work
→ P5 delivery
→ P6 client accepts / requests revision / disputes
→ P7 payment release
→ P8 payout receipt
→ P9 rating / project history
```

硬边界：

> `bid accepted ≠ work delivered`
>
> `work delivered ≠ client accepted`
>
> `client accepted ≠ payout actually received`

### 8.2 piecework / 多人计件

```text
W0 task pool published
→ W1 unit claimed/attempted
→ W2 submission
→ W3 quality review
→ W4 accepted/rejected
→ W5 per-piece settlement
```

需要恢复的不只是“这个任务有多少钱”，还要知道：

- 单位任务数是否有限；
- 是否先到先得；
- 失败是否重开；
- 验收由谁完成；
- 同一个账号完成多少单；
- rejected 单是否支付。

### 8.3 direct hire / repeat client

```text
D0 client identifies worker/profile
→ D1 invitation/contact
→ D2 scope/price agreed
→ D3 funding
→ D4 work
→ D5 delivery
→ D6 acceptance
→ D7 payment
→ D8 repeat relationship
```

这套状态机尤其容易在 archive 里消失，因为：

- 消息可能在登录后；
- 合同/需求可能只对双方可见；
- 交付文件有权限；
- 历史客户关系可能迁到 QQ / Email / 电话。

---

## 9. fee-rule version gap：同一个“赏金 1000 元”在不同年份不一定意味着劳动者拿到同样金额

历史任务页面上的 `¥1000` 或“赏金 1000 元”不能脱离当时费率解释。

早期 K68 同期报道描述的是特定佣金比例；一品威客 2014 年平台文章又显示，不同交易模式和规则存在自己的收费/赏金分配方式。

因此每个任务 evidence 应增加：

```yaml
fee_rule:
  platform: unknown
  effective_date: unknown
  transaction_mode: unknown
  worker_share: unknown
  platform_fee: unknown
  client_fee: unknown
  refund_rule: unknown
  provenance: unknown
```

固定：

> **displayed bounty ≠ worker net income**

> **same platform brand ≠ same fee rule across years**

新增：**fee-rule version gap**。

---

## 10. task-status drift：回放“一个历史任务页”最危险的是把后来的最终状态倒投给更早时点

任务页天然会变化：

```text
2006-09-01：征集中
2006-09-05：87 个投稿
2006-09-10：截止
2006-09-15：评选中
2006-09-20：中标结果显示
```

如果 archive 只抓到 9 月 20 日页面，不能写成：

> “9 月 1 日用户已经能看到赢家。”

如果平台今天保留“历史任务详情”，也不能假定它是原始状态快照。它可能：

- 用当前数据库把最终状态重新渲染进旧 URL；
- 把已删除投稿数量重算；
- 用当前会员昵称/头像；
- 隐去旧联系方式；
- 重新套用今日 CSS/JS；
- 把当前 fee/服务条款链接嵌入历史内容。

新增：

## task-status drift / 任务状态漂移

因此 archive evidence 必须记录：

```yaml
capture_datetime:
observed_task_state:
state_as_rendered_by:
  historical_server | current_server | archive_replay | unknown
```

---

## 11. uploaded-work orphaning：HTML 任务壳比真正劳动产物更容易幸存

设计/程序/图片任务至少涉及：

```text
HTML task page
+ thumbnail
+ full-size image / archive attachment
+ CSS/JS viewer
+ authentication / anti-hotlink
+ object-storage payload
+ database row
```

Web archive 很可能只保存：

- 标题；
- 赏金；
- “已有 140 个方案”；
- 一两个缩略图。

却没有保存：

- 140 份原始附件；
- 被 client-only 隐藏的投稿；
- ZIP/PSD/AI 源文件；
- 私信修改记录；
- 最终交付版本。

所以：

> `submission count survives ≠ submissions survive`
>
> `thumbnail survives ≠ deliverable survives`
>
> `task HTML survives ≠ labor product survives`

新增：**submission orphaning / 投稿孤儿化**。

---

## 12. escrow-observability gap：支付是任务市场最重要、又最难从公开网页恢复的一层

早期 K68 的核心卖点之一正是客户预付款与平台分配赏金。

但对于考古来说，真正需要的状态往往在公开页之外：

```text
client payment initiated
→ platform received funds
→ task funded
→ winner selected
→ release authorized
→ platform fee applied
→ payout initiated
→ bank/payment rail completed
→ worker balance available
```

公开任务页即使写“赏金已发放”，也可能只证明平台前端显示某状态。

没有：

- 资金流水；
- 平台账本；
- 收款账户证据；
- worker 同期确认；

就不能自动升级成 `worker actually received money`。

新增：**escrow-observability gap / 托管资金可观察性缺口**。

出于隐私和金融安全，本仓也不应主动搜集/公开普通劳动者完整账户流水；通常用当事人同期自述、平台官方结算说明和聚合统计交叉确认即可。

---

## 13. reputation orphaning：任务记录幸存，不代表它今天还对劳动者有职业价值

一个威客账号的职业资产可能包括：

- 等级；
- 中标次数；
- 评价；
- 历史案例；
- 客户回评；
- 认证；
- 累计金额。

但当：

- 平台关闭；
- 账号无法恢复；
- 产品改版；
- 旧等级体系废除；
- 页面只剩 SEO 历史壳；

这些记录即使部分仍能被 archive 看见，也不等于今天还能被本人用于接单。

> **archive-visible reputation ≠ portable career credential**

新增：**reputation orphaning / 声誉孤儿化**。

---

## 14. 2019 劳动调查只能作为后来的机制研究，不能倒装成 2006 页面证据

国际劳工组织 2021 年工作论文研究中国在线数字劳工平台，调查覆盖时间财富、一品威客、猪八戒等平台，并观察到：

- 多平台工作；
- 设计、IT、写作、问卷、微任务等不同工作；
- 计件、报名等待甄选、直接竞标等不同任务分配方式；
- 把寻找、准备等无薪时间计入后，劳动收益评价会下降；
- 一些劳动者会在普通工作时间以外继续服务客户；
- 有受访者报告完成并提交工作却未得到报酬。

来源：

- ILO Working Paper 24, *Online digital labour platforms in China: Working conditions, policy issues and prospects*, 2021
- <https://webapps.ilo.org/static/chinese/intserv/working-papers/wp024/index.html>
- 等级：B/A（高质量机构研究；样本来自平台相关招募，不具中国劳动人口代表性）

本仓使用它只做两件事：

1. 帮助确认到 2010s 后期任务分配机制已经高度多样；
2. 提醒考古人员，公开页面缺失的未支付时间和拒付状态是真实研究对象。

它**不能**证明：

- 2006 K68 已经有 2019 的所有任务类型；
- 2006 工人的收益/风险分布与 2019 相同；
- 当前平台工作条件可以倒投给旧页面。

---

## 15. Browser / runtime / Web 技术假设

一份 2004–2015 任务页可能依赖：

- GB2312 / GBK / UTF-8；
- table layout；
- IE-specific JS；
- iframe；
- popup；
- 登录 cookie；
- AJAX 动态投稿计数；
- JavaScript deadline countdown；
- Flash/ActiveX 上传器；
- 图片缩略图服务；
- anti-hotlink；
- 登录后私信/附件权限；
- 独立的对象存储/附件域名。

因此：

> **modern Chromium renders a page ≠ historical worker could complete the transaction in that environment**

如果历史任务上传依赖旧 Flash/ActiveX/IE 插件，现代回放很可能只能显示“上传按钮壳”。

以后取得真实 capture 时必须记录：

```yaml
browser_assumption:
charset:
script_dependencies:
upload_mechanism:
authentication_required:
attachment_hosts:
archive_rewrite_effect:
```

---

## 16. Preservation levels：保存到哪一层，才算真的理解一个旧任务市场

### W0 — locator only

只有域名/任务 URL/搜索结果，没有实际打开历史 capture。

### W1 — task shell

能够确认任务标题、品牌/站点壳，但关键动态状态未知。

### W2 — task metadata

可核：

- 赏金/预算；
- 截止时间；
- 分类；
- task state；
- 规则文本。

### W3 — participation layer

能观察：

- 投稿/投标计数；
- 部分匿名化 participant state；
- submission visibility；
- deadline/judging 状态。

不要求重新公开所有作品。

### W4 — outcome layer

能确认：

- winner / selected worker；
- 结果发布时间；
- task final state；
- 规则版本。

### W5 — settlement/reputation evidence

有足够、隐私最小化的证据支持：

- payment release state；
- platform fee rule；
- reputation/profile update。

不要求保存银行账户或个人敏感流水。

### W6 — multi-state transaction evidence

同一 task 至少跨两个以上历史时点，能够区分：

`open → judging → awarded/closed`

并有来自不同 evidence family 的 outcome/settlement 支持。

### W7 — historical runtime reconstruction

在明确 reconstruction 标识下，用历史浏览器/插件/编码条件验证：

- 页面如何渲染；
- 投稿/上传入口是否存在；
- 脚本/倒计时/附件如何失败；
- archive rewrite 与原始行为有何差异。

不能把 reconstruction 当 historical original。

---

## 17. 隐私与版权：任务市场比普通论坛更容易带有第三方作品和商业材料

威客任务特别容易涉及：

- LOGO / 插画 / 文案的版权；
- 客户尚未公开的品牌名称；
- 联系方式；
- 商业需求书；
- PSD/AI/源代码附件；
- 普通劳动者姓名/账号；
- 支付信息。

因此本仓默认：

1. 不批量重新发布全部历史投稿；
2. 不因 archive 可访问就复制完整作品集；
3. 研究任务状态优先保存 URL、日期、字段、哈希/摘要、计数和结果关系；
4. 普通劳动者账号最小化引用；
5. 若失败稿/未中标稿涉及可识别个人或已删除内容，不为“补全历史”而重新公开。

**历史可见性研究不应反过来成为重新暴露普通人劳动失败的工具。**

---

## 18. 本轮历史 replay 状态

### K68

同期媒体已经独立确认 `www.k68.cn` 在 2006 年作为 K68 任务平台 hostname 使用。

本轮尝试继续定位/打开约 2005–2006 的 Wayback historical replay，但当前访问链对构造的历史 replay URL 触发 URL 安全限制，未取得能够逐项核验：

```text
original_url
capture_url
capture_datetime
HTTP status
Content-Type / charset
DOM
JS
historical task state
submission payload
payment state
```

的合格 memento。

因此严格记录：

> **M1 verified K68 historical capture: NOT ACHIEVED IN THIS SLICE**

这只表示本轮没有完成验证，**不表示 Wayback 没有保存**。

### 猪八戒

本轮同样尝试构造约 2006 的历史 replay，受到相同 URL 安全限制。

此外，早期猪八戒的 canonical hostname / 域名变体仍需要历史 capture 或同期一手页面进一步确认，不能因为今天主域名是 `zhubajie.com` 就倒推 2006 的每个历史 URL。

因此严格记录：

> **M1 verified Zhubajie historical capture: NOT ACHIEVED IN THIS SLICE**

以及：

> **historical canonical-host state: unresolved in this slice**

---

## 19. 本轮新增的 old-Web 硬边界

1. `task page captured ≠ bounty actually funded`
2. `task published ≠ worker saw it`
3. `submission count ≠ unique workers`
4. `submission uploaded ≠ client reviewed it`
5. `submission produced ≠ labor paid`
6. `winner displayed ≠ payment received`
7. `displayed bounty ≠ worker net income`
8. `aggregate reward issued ≠ worker livelihood`
9. `registered member ≠ active worker`
10. `profile level ≠ skill alone`
11. `closed task today ≠ task was closed at earlier capture datetime`
12. `HTML task shell ≠ uploaded-work payload`
13. `thumbnail survives ≠ deliverable survives`
14. `payment UI ≠ escrow ledger`
15. `success story survives ≠ typical participant outcome`
16. `archive-visible reputation ≠ portable career credential`
17. `same brand ≠ same fee rule across years`

---

## 20. 它改变了我们怎样理解旧 Web

旧 Web 不只是“人们在网页上聊了什么”。

到 2000s 中期，一部分中文网页已经开始直接承载**劳动市场事务**：

```text
一家公司把需求写成一个 task
→ 一个陌生人看到
→ 花几个晚上做一份东西
→ 上传
→ 等待陌生客户选择
→ 可能拿到钱
→ 可能得到一条新的职业记录
→ 也可能什么都没有留下
```

这带来一个非常重要的档案学反转：

> **Web archive 往往最容易保存“有人发出了一份工作需求”，却最难保存“到底有多少普通人为它劳动、谁没有中标、谁真的拿到钱、这次经历是否改变了后来的人生”。**

任务标题、赏金数字和“已中标”标签是最显眼的网页遗物；真正构成普通人生活的却是投稿前的一周晚上、失败的方案、私信修改、提现、下一位客户和第二天仍要去上的主班。

因此威客考古不能停在“2006 年已经有悬赏网站”。

真正需要复原的是：

```text
call for labor
→ performed labor
→ selected labor
→ paid labor
→ remembered/reputable labor
```

这五层并不等价。

而对于“普通人有多少种活法”，它给出了一个非常具体的新答案：**互联网不只是让工作机会传播得更远，还让一份工作本身可以被切成一个网页对象。** 这种模块化让一个有主业的人也能在晚上把一部分技能卖给远处的陌生客户，却同时把未中标劳动、找单、排名和平台规则塞进了同一段生活。旧网页保存得越漂亮，我们反而越要提醒自己：看得见的那一单，可能只是大量不可见劳动里最后被选中的那一块。
