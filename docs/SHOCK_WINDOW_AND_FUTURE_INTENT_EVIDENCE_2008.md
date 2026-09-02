# 冲击窗口与“未来打算”证据：以 2008 年就业网页为例

> 旧网里保存下来的“我以后想做什么”，只能证明这个人在**那个时间点**怎样想未来，不能被后来发生的事情改写。

本说明补充 `docs/METHOD.md`，处理一类很容易在旧网页研究中被写错的证据：

- 求职调查；
- 论坛里的“毕业后去哪”；
- 博客里的职业计划；
- 招聘会采访；
- “五年后我想……”；
- “如果找不到工作我就……”；
- 金融危机、裁员、灾害、政策变化前后的计划。

核心问题不是“这段话后来实现了吗”，而是：

> **这条未来想象是在什么信息条件下产生的？**

---

## 1. 同一个年份，不一定属于同一个期待环境

2008 年提供了一个很强的例子。

中国青年报社调查中心与 Universum 在 **2008 年 1—4 月**调查 70 所高校 16,815 名大学生。当时报道的毕业去向偏好中，42.4% 希望进入外企，19.2% 希望去国企，13.4% 希望去政府部门，6.3% 希望自主创业。

来源：

- 中国新闻网转载《中国青年报》，2008-09-11：<https://www.chinanews.com.cn/edu/kong/news/2008/09-11/1378309.shtml>
- 中国青年报后续对比稿，2008-12-11：<https://zqb.cyol.com/content/2008-12/11/content_2466836.htm>

到 **2008 年 11 月下旬**，中国青年报社调查中心通过腾讯教育频道对 1,641 名即将毕业的 2009 届学生调查时，报道的偏好已明显不同：政府 20.8%、国企 20.3%、外企 18%、自主创业 21.6%。原报道也明确提醒，两次调查平台不同，因此不能把差异全部机械解释为金融危机造成。

同年 12 月 6 日南昌一场招聘会的同期采访中，面对约 3,000 个岗位和约 30,000 名求职学生，一名计算机专业毕业生已经把短期目标明确压缩成“先养活自己”，并暂时降低对专业对口和长期发展的要求。

来源：

- 中国青年报 / 新浪转载，2008-12-10：<https://news.sina.com.cn/o/2008-12-10/064014856658s.shtml>

### 方法结论

因此不能建立一个字段：

```yaml
year: 2008
future_expectation: optimistic
```

或：

```yaml
year: 2008
future_expectation: defensive
```

这两种都太粗。

更合理的是记录**statement/capture 所处的冲击窗口**。

---

## 2. 必须拆开四种时间

一条旧网页中的“未来打算”至少可能有四个时间：

1. **experience_time**：当事人真正经历或形成想法的时间；
2. **fieldwork_time**：调查、采访、问卷实际发生的时间；
3. **publication_time**：文章首次发布的时间；
4. **capture_time**：档案系统保存该网页的时间。

例如，2008 年 9 月发布的大学生职业倾向报道，核心调查发生在 **1—4 月**。

如果只按页面发布时间把它标成“2008 年 9 月青年就业心态”，研究者就可能错误地把**危机前完成的问卷**放进**危机后信息环境**。

建议字段：

```yaml
subject: graduate-employment-expectation
experience_time: null
fieldwork_start: 2008-01
fieldwork_end: 2008-04
publication_time: 2008-09-11
capture_time: null
shock_context:
  event: global-financial-crisis
  relation: fieldwork-precedes-major-late-2008-labor-market-shock
source_population: university-students
sampling_frame: 70-universities
sample_size: 16815
```

`capture_time` 如果来自 Wayback 等档案，必须继续按 `METHOD.md` 区分 Original Resource 与 Memento。

---

## 3. “后来证明错了”不等于当时证据失效

假设找到一个 2008 年 3 月博客：

> “毕业以后我想进外企，三年后去上海。”

而这个人 2009 年最终进入国企。

正确结论是：

- 2008 年 3 月时，这个人公开表达过一种职业未来想象；
- 2009 年实际轨迹后来发生变化（若另有证据）。

错误结论包括：

- “他其实一直更想去国企”；
- “他的 2008 年博客判断是假的”；
- “金融危机导致他改变计划”（除非存在直接证据）。

未来意向是一种**当时状态（historical state）**，不是对最终人生轨迹的预测模型。

建议把：

```yaml
future_intent: foreign-firm
```

和：

```yaml
realized_outcome: state-owned-enterprise
```

放在不同字段、不同证据链中。

---

## 4. 同时代第一人称比“后来回忆当时怎么想”更适合研究未来地平线

研究“2008 年的人当时相信什么”时，优先级通常应是：

1. 当时写下的博客 / BBS 帖 / 日记 / 问卷开放题；
2. 当时媒体采访中的直接引语；
3. 当时群体调查；
4. 多年后回忆“我那时其实……”；
5. 研究者根据后来轨迹反推当时动机。

这不是说后来回忆没有价值。

后来回忆适合研究：

- 人怎样重新解释过去；
- 哪些事件后来被视为转折；
- 记忆怎样把多个阶段压缩成一个故事。

但不能用 2025 年回忆自动覆盖 2008 年留下的同时代自述。

---

## 5. 调查平台变化本身是证据边界

2008 年初与年末两项调查并不是严格面板：

- 调查对象届别不同；
- 平台不同；
- 招募方式不同；
- 样本构成可能不同。

因此旧网页考古中如果看到两个百分比发生巨大变化，必须先检查：

```yaml
same_question: unknown/yes/no
same_population: no
same_sampling_frame: no
same_platform: no
same_period: no
```

只有这些边界被保存以后，才可以写：

> “同期材料显示偏好结构存在明显差异，并与金融危机冲击方向一致。”

而不应直接写：

> “金融危机使外企偏好从 42.4% 降到 18%。”

后一句暗示了超过证据能力的因果和同样本比较。

---

## 6. 网页转载链必须区分“发布日期”和“事件时间”

旧中文网页中大量历史材料通过转载存活。

例如一篇中国青年报稿可能同时存在于：

- 中青在线原始页；
- 中国新闻网转载；
- 新浪转载；
- 地方门户镜像；
- 后来的专题页。

几个 URL 不代表几个独立 evidence family。

对于未来意向材料，建议另外记录：

```yaml
origin_publication: 中国青年报
origin_publication_date: 2008-12-10
reprint_host: news.sina.com.cn
reprint_date: 2008-12-10
fieldwork_date: 2008-12-06
evidence_family: cyol-report
```

这样能避免：

- 把转载当独立交叉验证；
- 把转载页的 crawl/capture 时间当成采访发生时间；
- 把后来的存档时间误作历史时间。

---

## 7. 冲击窗口建议字段

对 1995—2015 中文旧网中涉及未来计划、职业选择、消费计划、买房、婚姻、迁移、留学、创业等材料，建议加：

```yaml
future_intent_evidence:
  statement_time: 2008-12-06
  publication_time: 2008-12-10
  capture_time: null
  evidence_kind: contemporaneous-interview
  population_scope: individual
  future_horizon: employment
  intent: accept-lower-threshold-job-first
  fallback_if_primary_fails: take-available-work
  shock_context:
    event: global-financial-crisis
    phase: acute-labor-market-reassessment
  realized_outcome_known: false
  hindsight_leakage: none-observed
  representativeness: low
```

对于调查：

```yaml
future_intent_evidence:
  fieldwork_start: 2008-01
  fieldwork_end: 2008-04
  publication_time: 2008-09-11
  evidence_kind: survey
  population_scope: multi-university-students
  sample_size: 16815
  sampling_frame: 70-universities
  platform: offline/unspecified-in-surviving-report
  realized_outcome_known: false
```

---

## 8. “未来想象”至少要区分五种 claim

同一个网页可能同时出现：

1. **aspiration**：最想要什么；
2. **expectation**：认为最可能发生什么；
3. **plan**：准备实际做什么；
4. **fallback**：首选失败以后怎么办；
5. **fear**：担心什么会阻断计划。

例如：

> “我想进外企，但如果找不到就先找份工作养活自己。”

不能压成：

```yaml
career_goal: employment
```

至少应该拆成：

```yaml
aspiration: foreign-firm
fallback: any-acceptable-income-job
fear: unemployment
```

这正是研究“人到底有多少种活法”时最有价值的部分：一个人脑中可能同时存在多个按优先级排列的未来，而不是只有一个人生目标。

---

## 9. 旧网页中的冲击并不自动创造新偏好

2008 年材料还能提醒另一件事。

即使冲击以后国企、政府、创业等选项更显眼，也不能自动推断金融危机“创造”了这些愿望。

可能的机制包括：

- 原本存在的稳定偏好权重上升；
- 公开招聘机会结构改变；
- 外企招聘减少；
- 政策宣传使创业更可见；
- 调查平台样本变化；
- 受访者把长期愿望与短期应急路线重新排序。

所以历史网页最稳妥的表达是：

> **冲击后，可观察到不同未来选项的相对显著性和排序发生变化。**

除非有独立证据，否则不要写成单一因果链。

---

## 10. 与 `how-people-lived` 的交叉接口

`old-web-archaeology` 负责回答：

- 这条 2008 年网页什么时候真正发布？
- 调查是什么时候做的？
- 原站还是转载？
- 页面/帖子是否为同时代 artifact？
- capture 是否晚于事件很多年？
- 引语是否可定位？
- 同一内容是否只是转载家族？

`how-people-lived` 则负责回答：

- 这个人当时把哪些未来列为首选、备选和失败路径？
- 冲击前后，退路组合怎样被重新加权？
- 这种变化在不同阶层、地区、教育背景中是否相同？
- 后来实际轨迹是否改变？

相关交叉研究：

- `tmzncty/how-people-lived/topics/fallback-portfolios-and-shock-reweighted-optionality-2008-2023.zh-CN.md`

---

## 11. 最低写作规则

以后使用 1995—2015 中文旧网中的“未来打算”材料时，至少遵守：

1. **写月/日，不只写年份**，只要来源允许；
2. **调查时间优先于报道发布时间解释受访者信息环境**；
3. **转载不算新的独立来源**；
4. **意向不等于后来实现的轨迹**；
5. **后来结果不能回填成当时动机**；
6. **调查样本变化不能伪装成同一群体前后变化**；
7. **冲击相关不等于冲击造成**；
8. **把 aspiration / expectation / plan / fallback / fear 分开**；
9. **第一人称同时代自述优先用于“当时怎么想”，回忆材料用于“后来怎么解释”**；
10. **保存不知道**：如果不知道当事人后来做了什么，就明确写 `realized_outcome_known: false`。

这套规则的目的不是让旧网研究变得保守到无法讲故事，而是防止最常见的后见之明错误：

> **把一个人后来走过的人生，误写成他当时已经知道自己会走的人生。**
