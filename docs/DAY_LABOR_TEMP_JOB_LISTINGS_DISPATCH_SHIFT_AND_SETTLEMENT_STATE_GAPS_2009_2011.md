# DAY_LABOR_TEMP_JOB_LISTINGS_DISPATCH_SHIFT_AND_SETTLEMENT_STATE_GAPS_2009_2011.md

> 状态：methodology / research note / execution-state model  
> 主范围：2009–2011 中文网络中的兼职、短工、本地分类信息与移动发布/查询；1990s–2008 马路劳务市场只作必要前史边界  
> 关联生活史：`tmzncty/how-people-lived/topics/day-labor-daily-reentry-income-latency-and-standby-life-china-1991-2025.zh-CN.md`  
> 与既有文件边界：`ONLINE_RECRUITMENT_RESUME_DATABASES_APPLICATION_STATES_AND_RESPONSE_GAPS_2000_2004.md` 研究持续岗位、简历数据库、投递和回复；本篇研究**有效期可能只有几个小时 / 一天的岗位，以及 Web 页面之后的派工、上车、到岗、工时和结算状态。**

---

## 0. 为什么短工需要单独的旧网状态机

普通网络招聘可以被简化为：

```text
job posted
→ resume submitted
→ employer response
→ interview
→ offer
→ employment
```

但日结、小时工、暑期兼职、活动临工、临时搬运等可能是：

```text
05:30 发布今天要 8 人
→ 05:45 有人看见
→ 电话 / QQ 联系
→ 06:00 已招满
→ 06:20 帖子仍在线
→ 工人集合
→ 车辆接走 / 自行到岗
→ 当天劳动
→ 核算工时
→ 当晚结算 / 或发生拖欠
```

因此一个保存完好的招聘页面，可能在它被 archive 捕获时已经没有现实执行价值。

本篇固定：

> **listing survived ≠ shift was still open**

> **worker contacted ≠ worker selected**

> **selected ≠ arrived on site**

> **arrived ≠ work actually started**

> **work completed ≠ hours accepted**

> **quoted day rate ≠ amount paid**

> **same-day-pay claim ≠ same-day settlement**

这组 gap 与一般求职网页明显不同，因此值得独立建模。

---

# 1. 必要前史：Internet 以前，地点本身就是“本地招聘平台”

2004 年关于沈阳鲁园劳务市场的同期报道称，这个自发形成的零工劳务市场当时已经存在 13 年；2008 年郑州二马路劳务市场每天约有一千人找工作。

来源：

- 2004-02-11《鲁园里 农民工艰难“找活儿”》：  
  <https://news.sina.cn/sa/2004-02-11/detail-ikknscsi2613320.d.html>
- 2008-08-07《新劳务市场开业求职农民工不买账》：  
  <https://news.sina.com.cn/c/2008-08-07/073414279363s.shtml>

证据角色：**B**。

这里不把 `old-web-archaeology` 扩展成 1990s 劳务市场史，只保留一个边界：

```text
fixed street / market
→ workers know where to appear
→ employers know where to drive
→ skill sign / direct question
→ immediate selection
```

Web 后的分类信息并没有发明本地匹配，而是把一部分 **place-based discoverability** 变成 **remote discoverability**。

---

# 2. 2008 郑州：physical profile 与 two-sided discoverability

2008 年郑州报道特别适合旧网方法，因为它展示了一套完全没有服务器、但状态非常明确的“现场信息系统”。

劳动者手里或脚边的纸上写着：

- 杂工；
- 烩面；
- 炒菜；
- 护理病人；
- 保姆。

这相当于一个 physical profile：

```text
skill
+ availability-now
+ physical presence
+ direct contact
```

同一天，新建的正式劳务市场虽然环境更规范，但没有雇主进来发招聘信息。劳动者于是重新回到二马路，解释说临时招工的人不知道新市场，进去“不好找活”。

来源：

- <https://news.sina.com.cn/c/2008-08-07/073414279363s.shtml>

对旧网的直接启发：

> **a better interface with no demand-side traffic is still an unusable marketplace.**

因此以后研究分类信息网站，不能只恢复“求职者可以发帖”这一边。

必须问：

- 雇主是否真的浏览该分类；
- 雇主是否知道该站点；
- 同城 / 区域是否准确；
- 帖子有没有被搜索收录；
- 联系入口是否可用；
- 岗位在回复前是否已经招满。

---

# 3. 2009：BBS / QQ 式“网络兼职”已经形成不同于正式简历的入口

2009 年江西日报同期报道高校“网络兼职”时，直接记录校园 BBS 上的招聘帖：

- 校园兼职记者；
- 论坛管理员；
- 通过 QQ 联系；
- 学生把这类经历理解为勤工助学、职业经验甚至未来创业的“探路石”。

来源：

- 《“网络兼职”受大学生追捧》，江西日报，2009-04-14，经新浪保存：  
  <https://news.sina.com.cn/o/2009-04-14/082815463441s.shtml>

证据等级：**B：同期媒体观察。**

这和 2001 年简历数据库非常不同。

简历数据库强调：

```text
profile fields
→ employer search
→ application
```

部分兼职帖则更接近：

```text
forum post
→ brief requirements
→ QQ contact
→ private conversation
→ ad hoc work
```

因此出现 **low-formality recruitment handoff**：

> 公开 Web 只留下帖子，真正的筛选、价格、身份确认和开工时间马上转移到即时通信。

这类岗位尤其容易在历史记录中断成两半。

---

# 4. 2009：online labor 可以完全不留下“工作地点”

2009 年《中国新闻网》报道的“网络钟点工”包括替人处理游戏 / 网络服务、代写博客、收集资讯等，报道同时讨论网络劳务中缺少传统劳动合同、发生纠纷后难以处理的问题。

来源：

- 2009-10-16《中国新闻网》报道，经搜狐保存：  
  <https://news.sohu.com/20091016/n267398755.shtml>

证据等级：**B**。

这说明短工不能只按“同城现场派工”理解。

到 2009 年至少已经同时存在：

```text
street day labor
local offline casual work
campus BBS / QQ part-time recruitment
purely online casual labor
```

旧网 archive 对最后两类尤其容易过度可见：

- 帖子更容易存下来；
- 但私聊和实际报酬更难保存。

于是必须防止：

> **web visibility bias → 误以为线上零工比街头零工更普遍。**

---

# 5. 2010：兼职页面的“高日薪”可以产生强行动，但页面并不证明岗位存在

2010 年浙江在线同期报道一批大学生看到网络兼职招聘：

> 日薪 200 元、连续 27 天的活动工作人员。

一些学生因此：

- 放弃家乡其他实习机会；
- 留在杭州；
- 租房；
- 缴纳报名费用；
- 等待上岗。

最终活动被告知取消，一名学生已经损失刚交的 1000 元房租，只能计划回家。

来源：

- 《大学生暑期打工要防“陷阱” 高薪往往是骗局》，2010-08-10：  
  <https://zjnews.zjol.com.cn/system/2010/08/10/016833240.shtml>

证据等级：**B：同期媒体 + 同期第一人称。**

这不是一个“互联网诈骗史”案例那么简单。

它提供了一条非常重要的 execution boundary：

```text
listing visible
→ applicant believes it
→ applicant pays / rents room / stays in city
→ promised activity fails to materialize
```

所以：

> **job listing can produce real-world costs even when no job ever exists.**

对于短工网页，不能只问“页面是真是假”，还必须问：

- event / project 是否真的成立；
- 招聘方是否真的取得用工资格；
- 招聘人数是否真实；
- 开工日期是否发生；
- 报名费 / 押金是否形成 sunk cost；
- 岗位取消后谁承担租房、交通和机会成本。

---

# 6. 2010：本地分类信息进入手机，岗位信息第一次能跟着人移动

赶集网 2010 年 9 月的同期报道与行业资料说明：

- 2009 年 5 月已有 WAP 版本；
- 2010 年 9 月上线智能手机客户端；
- 支持 iPhone、BlackBerry、Nokia/Symbian 等环境；
- 客户端强调减少相对 WAP 的流量消耗，并支持本地分类信息的移动访问。

来源：

- Interfax China, 2010-09-06：  
  <https://interfax.com/newsroom/top-stories/63073/>
- 腾讯科技 2010-09-06，经投资界保存：  
  <https://m.pedaily.cn/news/185454>

证据等级：**B / platform report**。

同年行业报道把赶集网描述为覆盖招聘、住房、二手、本地服务等的本地分类信息站。

来源：

- ChinaTechNews, 2010-04-27：  
  <https://www.chinatechnews.com/2010/04/27/11962-chinas-ganji-com-dianping-com-form-strategic-alliance>

这允许一个非常窄但重要的旧网结论：

> **local listing access became portable before the full app-platform era.**

但当前证据不能证明：

- 一个 2010 日结工真的用该 app 找到工；
- 兼职分类当时的具体 UI；
- 历史定位精度；
- push notification；
- 当时用户的具体 data plan 成本。

这些仍然需要历史 capture / 用户材料。

---

# 7. 2011：分类平台明确把“学生兼职”做成独立专区

2011 年 8 月同期报道记录：赶集网推出“同城学生兼职”专区，允许本地企业快速发帖、学生查询浏览；报道提到销售、餐饮、娱乐等暑期兼职，并出现按日标价的岗位。

来源：

- 中国经济网 2011-08-09，经新浪/MSN 页面保存：  
  <https://msn.finance.sina.com.cn/gdxw/20110809/1244220096.html>

证据等级：**B：同期报道；薪酬与“海量岗位”等宣传性用语不能当独立市场统计。**

这一证据可以证明：

```text
local city
+ student status / part-time intent
+ short-duration work
+ employer self-posting
+ online browse
```

已经被平台产品化。

但它仍然不证明：

```text
post
→ successful contact
→ actual shift
→ completed hours
→ money received
```

---

# 8. 短工 Web 的核心特征：listing half-life / 岗位半衰期

普通长期岗位可能开放若干天。

短工的现实有效期可能只有：

- 今天上午；
- 今晚夜班；
- 周末两天；
- 一场活动；
- 还缺的最后 3 个人。

因此短工历史页面需要额外字段：

```yaml
posted_at:
work_date:
start_time:
expected_duration:
headcount_requested:
headcount_remaining_at_capture: unknown
application_deadline:
contact_channel:
listing_status_at_capture: unknown|open|filled|cancelled|expired
```

如果 archive 只保存：

> “招聘 10 人，日薪 200”

就不能自动解释为 capture 时还有 10 个岗位。

固定：

> **advertised headcount ≠ remaining headcount**

> **capture datetime ≠ job-validity datetime**

---

# 9. dispatch-state gap / 派工状态缺口

许多短工不需要完整线上申请，而是：

```text
post / forum / classified
→ phone / QQ / SMS
→ “明早 6 点 XX 门口集合”
→ 到场
→ 现场再挑人
→ 车辆运到工地
```

公开 Web archive 通常只保存第一格。

应区分：

1. `listing_exists`
2. `contact_initiated`
3. `contact_acknowledged`
4. `worker_preselected`
5. `meeting_point_assigned`
6. `worker_arrived`
7. `worker_selected_on_site`
8. `transport_departed`
9. `worker_arrived_at_job_site`

任何一步都不能从上一层自动推出。

---

# 10. shift-state gap / 班次状态缺口

到工地以后仍然不是“工作已经完成”。

进一步需要：

```text
check-in
→ work actually starts
→ breaks / waiting
→ hours counted
→ early dismissal / cancellation
→ task completion
→ employer accepts hours / quantity
```

短工尤其可能发生：

- 人到了但临时不用；
- 只干半天；
- 天气取消；
- 活提前做完；
- 雇主把等待时间排除在工时外。

这些几乎从不保存在公开招聘页。

---

# 11. settlement-state gap / 结算状态缺口

“日结”应该被拆成状态，而不是一个文本标签：

```text
rate advertised
→ rate verbally confirmed
→ hours / pieces accepted
→ gross amount calculated
→ intermediary deduction
→ payment promised
→ cash / transfer initiated
→ worker actually receives usable funds
→ dispute closed / unresolved
```

因此：

> **日结 is a promised settlement schedule, not evidence of settlement.**

这与卖家平台的 `delivered ≠ settled` 有相似结构，但对象不同：这里是劳动关系与工资，而不是商品交易。

---

# 12. 2019 材料帮助我们理解 2009–2011 缺的到底是什么

虽然 2019 超出本篇旧网主时段，但可以作为后续机制校验。

工人日报对马驹桥的同期报道记录：

- 工人仍在街头聚集；
- 雇主车辆直接来“拉人”；
- 手机微信群同时发布招工消息；
- 有人把临工当作寻找下一份长期工的桥接。

来源：

- <https://www.chinanews.com/sh/2019/07-18/8898589.shtml>

这里不能拿 2019 微信群倒写 2010 QQ/WAP 的具体行为。

但它验证了本篇状态模型中的基本事实：

> **digital listing and physical hiring can coexist in the same labor market.**

因此不能把 2010 分类网站的出现写成“马路劳务市场终结”。

---

# 13. 与既有招聘旧网研究的区别

已有：

`ONLINE_RECRUITMENT_RESUME_DATABASES_APPLICATION_STATES_AND_RESPONSE_GAPS_2000_2004.md`

重点是：

```text
resume database
application
employer response
interview
employment outcome
```

本篇重点是：

```text
listing freshness
remaining headcount
same-day contact
meeting point
physical dispatch
shift completion
same-day settlement
```

两者共享：

> page survived ≠ employment outcome survived

但短工再多出两个特殊历史难点：

1. **岗位有效期极短**；
2. **实际工资状态发生在页面之外，而且可能当天就全部结束。**

---

# 14. 58 / 赶集的后续资料能证明什么、不能证明什么

58 同城 2013 年提交给美国 SEC 的上市文件描述其在线 marketplace 覆盖约 380 个城市，主要类别包含 Jobs；Jobs 下当时覆盖销售、技能工人、餐饮人员、配送、家政清洁等，并提供简历搜索、候选人管理等招聘工具。

来源：

- 58.com F-1, 2013：  
  <https://www.sec.gov/Archives/edgar/data/1525494/000104746913009985/a2217137zf-1a.htm>

证据等级：**A for 2013 company disclosure**。

但必须限定：

- 它是 2013 年文件，不证明 2009 页面字段完全相同；
- 它描述 jobs category，不证明“日结”是核心产品形态；
- 简历工具存在，不代表临工必须走完整简历流程；
- 公司声称自动 / 人工筛查信息，不代表每条岗位真实、仍有效或实际支付。

这一材料适合建立平台后来的 formal endpoint，而不能用来填补 2009–2011 历史 UI 空白。

---

# 15. 本轮 archive negative result

本轮公开搜索能够核验：

- 2009 校园 BBS / QQ 兼职场景；
- 2009 网络劳务报道；
- 2010 线上兼职产生的现实行动与岗位取消案例；
- 赶集 2009 WAP、2010 手机客户端；
- 2011 赶集“同城学生兼职”专区的同期报道；
- 2013 58 正式 Jobs 产品结构。

但**没有取得并实际验证一个 2009–2011 赶集 / 58 “兼职 / 临时工 / 日结”分类页的完整历史 capture（HTML + capture datetime + 子资源 + 历史移动状态）**。

因此本篇明确不声称已经恢复：

- 2009/2010 兼职分类 exact URL taxonomy；
- 当年 DOM / CSS；
- GBK / UTF-8 实际 response；
- IE / WAP / Symbian 页面视觉；
- 历史筛选字段；
- 岗位置顶 / 排名算法；
- 联系信息隐藏策略；
- 具体“日结”标签是否为产品级字段还是自由文本。

当前 58.com 的“临时工兼职”页面虽然今天可访问，**不得拿它作为 2010 页面证据。**

这遵守 `docs/METHOD.md`：

> current page ≠ historical capture。

---

# 16. 新增 gap taxonomy

## listing-freshness gap

页面存在，但不知道岗位是否还有效。

## remaining-headcount gap

知道原计划招多少，不知道 capture 时还缺几人。

## contact-channel gap

公开页保存，但电话 / QQ / SMS 私下状态消失。

## dispatch-state gap

不知道联系后是否给出集合地点、是否被挑中、是否被车接走。

## arrival-state gap

不知道人是否实际到岗。

## shift-state gap

不知道是否开工、实际干了多久、是否提前取消。

## rate-confirmation gap

页面工价和现场口头工价可能不同。

## hours-acceptance gap

劳动者认为自己干了 N 小时，不代表雇主最终认可 N 小时。

## settlement-state gap

“日结”文本不能证明钱已经到账。

## cancellation-externality gap

岗位取消以后，求职者为租房、交通、留城和放弃其他机会支付的成本不在页面里。

## physical-market coexistence gap

Web 有兼职信息，不证明街头 / 市场 / 熟人中介停止工作。

## mobile-portability gap

WAP / app 存在，不证明目标群体拥有兼容终端、数据资费可承担或真的用移动端找短工。

---

# 17. 建议 evidence record 字段

```yaml
object_type: temp_job_listing
platform:
city:
category:
original_url:
capture_url:
capture_datetime:
posted_at:
work_date:
work_start_time:
expected_duration:
advertised_headcount:
remaining_headcount_at_capture:
advertised_rate:
settlement_claim: same_day|weekly|monthly|unknown
contact_channel: web_form|phone|sms|qq|other
listing_status_at_capture: open|filled|cancelled|expired|unknown
historical_browser_verified: false
historical_mobile_client_verified: false
archive_grade:

execution_state:
  contact_known: unknown
  selected_known: unknown
  meeting_point_known: unknown
  arrived_known: unknown
  work_started_known: unknown
  hours_worked_known: unknown
  amount_due_known: unknown
  amount_paid_known: unknown
  paid_at_known: unknown

privacy_notes:
unknowns:
claim_supported:
claim_not_supported:
```

---

# 18. 隐私与版权边界

短工旧帖很容易包含：

- 手机号；
- QQ 号；
- 集合地点；
- 私人姓名；
- 身份证要求；
- 雇主个人联系方式。

研究时应：

- 优先记录字段结构、URL pattern 与流程；
- 不批量复制普通人的旧联系方式；
- 不尝试联系历史手机号 / QQ 来“验证”；
- 不因号码今天仍有效就继续追踪个人；
- 招聘骗局案例只保留支持机制所需的最少人物信息。

对历史页面 / 截图同样遵守版权最小化，不为“复原兼职首页”而复制整站资源。

---

# 19. 这改变了旧网考古的哪一点？

普通内容页可以近似问：

> 这份文字在这个时间点有没有存在？

短工页却必须多问：

> **这份文字在这个时间点还来得及改变一个人的今天吗？**

这是一个真正的 **temporal execution web**。

岗位页面的意义随小时衰减；

页面之外的电话、QQ、集合、上车、开工和工资状态才决定：

> 一个网页里的“200 元 / 天”，最后有没有变成一个普通人今晚手里的 200 元。

---

# 20. 下一步

下一轮旧网侧最高价值证据不是更多今天的 58 页面，而是：

1. 实际验证一个 2009–2011 兼职分类历史 capture；
2. 记录 original URL、capture datetime、category taxonomy；
3. 检查历史子资源和 charset；
4. 尝试找到一组同一天多个 capture，观察一个短工帖是否出现 / 删除 / 过期；
5. 找同期用户材料确认 `Web → QQ/电话 → 集合 → 上工` 的 handoff；
6. 不追踪私人联系方式，不把无法恢复的 backend / settlement 状态补成故事。

如果这些证据仍然不存在，`短时招聘交易状态几乎没有进入公共 Web 档案` 本身就应成为正式考古结论。
