# ELICITED_FUTURES_CURATED_COURSE_BLOG_AND_TEMPORAL_COMPOSITES_2007_2010

## Scope

本说明研究 2007–2010 中文旧网中一种与普通人生活史高度相关、但很容易被误判的文物：**课程/论坛征集后由公共博客整理发布的个人未来规划文本**。

它与本仓已有的：

- `APPLICATION_STATE_ELIGIBILITY_AND_ROUTE_PORTFOLIO_2003_2015.md`；
- `ABANDONED_APPLICATIONS_AND_NEGATIVE_STATE_SURVIVAL_2007_2015.md`；

研究对象不同。前两者主要处理申请系统状态、资格、确认、缺考和负状态。本文件研究的是：

> **一段“我以后要怎样生活”的第一人称文本，究竟是谁写的、谁发布的、在什么提示下产生、今天又以哪一层网页外壳幸存？**

本仓仍严格保持约 1995–2015 中文互联网 scope。中国高等教育制度环境和英国 PDP 对照的生活史解释主要放在 `tmzncty/how-people-lived`；这里仅处理中文旧网页文物、provenance、展示层与推理边界。

---

## 1. 当前可观察对象：一个仍存活的新浪“职业生涯规划”博客出版层

当前访问新浪博客目录：

<https://blog.sina.com.cn/s/articlelist_1456022085_0_1.html>

可以观察到：

- 页面标题/博客名显示为“职业生涯规划”；
- 当前目录显示“全部博文(9358)”；
- 当前分类包括职业生涯规划与生涯教育、大学生活、职业素质、求职策略、就业指导与考研规划、创业与留学、自我探索与职业选择等；
- 目录仍列出大量内部日期为 2007–2013 的文章；
- 若干文章标题带 `[原创]我的职业生涯规划……`；
- 具体正文常以 `文/某学生（年级/专业）` 署名，并在文末标示“出处：大学生职业生涯规划论坛”。

当前“关于我”页：

<https://blog.sina.com.cn/s/profile_1456022085.html>

则显示：

- 基本信息、个人经历、个人简介均“暂未添加”；
- “暂未认证”。

因此本轮只能确认：**新浪当前仍提供一个以“职业生涯规划”为名的账号/博客展示层，其中保存了大量历史日期正文和学生署名。**

不能从当前 profile 独立确认：

- 账号现实运营者是谁；
- 是否由某位教师、学校部门、论坛编辑或多人共同维护；
- 学生是否亲自登录该新浪账号发布；
- 页面署名是否经过独立身份核验。

---

## 2. 第一条硬规则：`displayed student byline ≠ platform account owner`

以 2007-12-27、2008-06-04、2009-04-05、2010-12-05 的几篇规划为例，正文都出现学生年级/专业式署名，同时位于同一个新浪博客账号下，并在文末指向“大学生职业生涯规划论坛”。

最安全的文物模型是：

```text
student-attributed text
→ course / forum / editorial collection layer ?
→ Sina blog account publication layer
→ current surviving Sina rendering
```

中间关系尚未完全核实，因此不能写成：

```text
该学生的个人新浪博客
```

除非有独立证据证明账号归该学生所有。

推荐字段：

```yaml
platform: sina-blog
platform_account: "1456022085"
account_display_name: "职业生涯规划"
displayed_post_author: "student byline present"
author_identity_basis: page_byline
account_owner_verified: false
publisher_relation: unknown_or_collective
source_attribution_in_body: "大学生职业生涯规划论坛"
```

隐私上，仓库正文优先使用“某法学大二学生”“某管理学院大三学生”等角色描述，而不是建立普通学生姓名索引。

---

## 3. `[原创]` 是页面标签，不是独立作者认证

新浪标题里的 `[原创]` 可以作为**平台/编辑展示事实**记录：

```yaml
platform_originality_label: "原创"
```

但它不能自动升级成：

```yaml
authorship_independently_verified: true
```

原因很简单：

- 账号可能是转载/汇编层；
- 正文作者与发布账号并非同一主体；
- “原创”可能表示相对博客内容库的编辑分类，而非法律意义或身份验证意义上的作者认证；
- 本轮没有找到原始课程提交系统或作者本人独立账号作交叉核验。

因此：

> **platform originality label ≠ verified authorship**

这条规则也适用于旧博客中的“原创”“转载”“荐”“精华”等平台标签。

---

## 4. 第二条硬规则：`contemporaneous text ≠ spontaneous text`

这些文章最容易被生活史研究误用的地方，是把“同时代第一人称”直接等同于“自发日记”。

2007-12-27 的一篇文章开头明确说职业生涯规划课即将结束，结尾感谢老师提供机会认真考虑未来；2009-04-05 的跨专业考研规划也明确说学习课程后，自己才把原有转专业想法变成具体实施方案；2010-12-05 的文章称要“郑重地将它提交”。

因此它们应编码为：

```yaml
contemporaneous: true
first_person: true
elicitation_context: course_or_forum_assignment_like
spontaneous: false_or_not_established
```

研究者可以据此说：

> `该学生在当时的职业规划文本中如此描述自己的未来。`

不能直接写：

> `这就是当时学生未经提示时自然想到的未来。`

核心规则：

> **contemporaneous self-description ≠ spontaneous self-description**

---

## 5. “计划”也不是“预测”：`future plan ≠ expected outcome`

职业规划作业通常要求作者产生目标、SWOT、时间表和行动计划。一个结构完整的未来文本至少可能同时包含：

- normative goal：我觉得自己应该成为谁；
- preferred route：我现在最想走哪条路；
- fallback：如果失败怎么办；
- assignment compliance：为了完成作业必须给出一个计划；
- aspiration：理想上希望几十年后如何；
- probability judgment：本人认为实际上多大概率能发生；
- later outcome：最后真的发生了什么。

这些不能互相替代。

例如 2008-06-04 的学生文本把未来串成公务员、继续读研、企业、博士、约 45 岁后大学任教的长链，同时本人又明确承认人生存在变数、可能在路口改变方向。

所以：

> **long route sequence on page ≠ belief in deterministic life course**

以及：

> **future plan ≠ expectation ≠ probability judgment ≠ later outcome**

---

## 6. 这组页面是“未来文物”，不是社会总体样本

目前幸存页面很适合研究：

- 2007–2010 年学生如何使用“职业规划”语言；
- 哪些职业、教育、资格、城市和家庭条件可以进入一个规划文本；
- SWOT、时间表、证书、实习、考研、公考、回乡等怎样被组织成计划；
- 什么样的文章会被职业教育博客整理和公开。

它不适合直接估计：

- 有多少大学生想考公务员；
- 有多少人相信五年/十年计划能够实现；
- 有多少学生支持职业规划课程；
- 2008 年大学生总体有多乐观。

因为我们没有：

```text
all students
→ all course participants
→ all submitted assignments
→ selected for forum/blog
→ successfully published
→ survived platform changes
→ currently retrievable
```

每一层的分母。

---

## 7. 新的保存偏差：`coherence survival bias`

这类 corpus 可能产生一种与 `negative-state survival gap` 不同的偏差：

**coherence survival bias（连贯性存续偏差）**。

容易被课程、论坛或编辑层选择并保留下来的文本，可能更偏向：

- 标题完整；
- 有自我分析；
- 有 SWOT；
- 有明确目标；
- 能分阶段；
- 能给出行动列表；
- 有积极结语；
- 适合作为他人参考。

而以下未来更容易不留下公开文物：

- “我不知道”；
- 只交很短的作业；
- 目标互相矛盾；
- 不愿公开家庭/感情/经济问题；
- 中途改主意但未重新投稿；
- 根本没有参加这类课程/论坛；
- 觉得“规划没用”的人；
- 计划失败后不再更新原文的人。

所以：

> **surviving polished plan ≠ typical degree of historical certainty**

这个偏差会使几十年后的研究者把过去看得比当时实际生活更加整齐、有序和可规划。

---

## 8. 第三条硬规则：`internal post datetime ≠ verified historical capture datetime`

本轮访问的是**当前仍可返回的 live Sina pages**。页面正文内部显示：

- 2007-12-27；
- 2008-06-04；
- 2009-01-28；
- 2009-04-05；
- 2010-12-05；

等博文日期。

这些日期是重要的**页面内部时间声明**，但本轮没有为每篇文章验证对应日期附近的 WARC/Wayback capture。

因此字段必须拆开：

```yaml
internal_post_datetime: "2008-06-04 07:16:49"
body_claimed_origin_time: "2008-06-04"
retrieved_at: "2026-09-03"
archive_capture_datetime: null
historical_capture_verified: false
```

不能把：

```text
页面现在显示 2008-06-04
```

写成：

```text
我们已经验证 2008-06-04 当天新浪服务器返回的就是当前这份 HTML。
```

核心规则：

> **historical-looking live page ≠ verified historical capture**

---

## 9. 当前页面是 temporal composite，不是 2008 浏览器体验

当前目录页和正文页同时包含：

- 历史日期正文；
- 当前/后期新浪导航；
- 微博入口；
- 当前统计/关注展示；
- `Copyright © 1996 - 2022 SINA Corporation`；
- 今天仍能请求到的图片、脚本和样式资源。

因此最好把当前页面建模为：

**temporal composite page（时间复合页面）**。

至少拆成：

```yaml
content_body_time: historical_internal_date
platform_template_time: unknown_later_or_current
sidebar_state_time: current_retrieval_state
asset_versions: mixed_or_unknown
retrieval_time: current
```

尤其不能从当前目录的：

```text
全部博文(9358)
职业生涯规划与生涯教育(738)
...
```

倒推出 2008 年就已经有同样的总数、分类结构或栏目名称。

同理，当前 `关于我` 页显示“暂未认证”“暂未添加”，只能证明**当前返回的 profile 状态**，不能证明 2008 年当时 profile 一定为空。

因此：

> **current profile state ≠ historical profile state**

以及：

> **current category count ≠ historical category count**

---

## 10. 当前 live page 的 body 与 chrome 必须分层引用

建议引用时写成：

> `当前仍可访问的新浪页面中，正文内部标示发布时间为 2008-06-04，并以学生年级/专业署名；本轮未验证 2008 年同期 archive capture。`

而不是：

> `2008 年的新浪博客页面长这样。`

建议字段：

```yaml
artifact:
  platform: sina-blog
  account_id: "1456022085"
  current_url:
  retrieved_at:
  internal_post_datetime:
  displayed_title:
  displayed_byline_present: true
  body_source_attribution_present: true
  current_template_markers:
    - weibo-link
    - current-profile-module
    - sina-copyright-2022
  historical_capture_verified: false
  browser_assumption: modern-retrieval-only
```

这与 `docs/METHOD.md` 的原则一致：现代浏览器当前返回的页面不能自动当作历史浏览体验。

---

## 11. 推荐的新研究单位：`future-plan artifact`

为了让生活史研究可以安全引用旧网“未来规划”，建议新增一个逻辑研究单位，而不是把它混进普通 blog post：

```yaml
future_plan_artifact:
  platform:
  account:
  url:
  internal_post_datetime:
  retrieved_at:
  archive_capture_datetime:

  authorship:
    displayed_byline: present | absent
    identity_basis: page_byline | verified_account | unknown
    account_owner_same_as_author: true | false | unknown

  elicitation:
    context: course | contest | survey | interview | forum_prompt | spontaneous | unknown
    prompt_text_known: true | false | partial
    submission_language_present: true | false

  future_content:
    horizon_years:
    primary_route:
    fallback_routes:
    route_sequence:
    credentials_named:
    cities_named:
    family_constraints_named:
    financial_constraints_named:
    uncertainty_acknowledged: true | false
    revision_acknowledged: true | false

  publication:
    publication_layer: personal_blog | collective_blog | forum | media | school_site | unknown
    selection_mechanism: known | partial | unknown
    platform_originality_label:

  provenance:
    evidence_grade:
    historical_capture_verified:
    current_template_contamination: likely | unknown | low
```

重点是：**prompt、author、publisher、account、page、capture、future claim 七层不能压成一个对象。**

---

## 12. 样本页：只登记支持方法结论所需的最小信息

### 12.1 2007-12-27

URL：
<https://blog.sina.com.cn/s/blog_56c9224501007z9x.html>

当前可观察：

- 内部日期 2007-12-27；
- 标题带 `[原创]`；
- 正文以某法学大二学生署名；
- 明确说职业规划课程即将结束；
- 文末标“出处：大学生职业生涯规划论坛”；
- 文章承认目标仍不唯一，保留公务员/考研等备选。

证明力：

- 高：该当前页面**呈现**上述历史日期正文与课程语境；
- 中：该文本可作为同期署名第一人称未来规划使用；
- 低/未知：学生现实身份、当时发布账号控制权、2007 原始页面模板。

### 12.2 2008-06-04

URL：
<https://blog.sina.com.cn/s/blog_56c9224501009pkc.html>

当前可观察：

- 内部日期 2008-06-04；
- 学生署名与年级/学院；
- 助学贷款、稳定收入、继续教育进入同一计划；
- 存在跨数十年的 route sequence；
- 本人同时明确承认未来可能改变。

方法意义：

> `long coherent plan` 与 `acknowledged uncertainty` 可以同时存在。

### 12.3 2009-04-05

URL：
<https://blog.sina.com.cn/s/blog_56c922450100d0e9.html>

当前可观察：

- 内部日期 2009-04-05；
- 文本把原专业不适配转化为跨专业考研的新目标；
- 使用 SWOT；
- 把任务排到年度、学期、寒暑假；
- 明确写出任务列表与时间平衡策略；
- 结尾把具体方案与所学职业规划课程连接起来。

方法意义：

> 旧网页可以保存一种“把未来写成 project plan”的文本实践，但不能据此证明计划最终执行。

### 12.4 2010-12-05

URL：
<https://blog.sina.com.cn/s/blog_56c922450100ndxb.html>

当前可观察：

- 内部日期 2010-12-05；
- 文本使用“郑重提交”语言；
- 明确不准备考研；
- 同时保留企业生物信息、回乡中学教师、回乡公务员三条方向；
- 把计算机、英语、实践、支教、公考准备排入未来三学年。

方法意义：

> 同一职业规划格式可以容纳不同生活路线，不能从文类本身推出“所有规划都朝更高学历/大城市集中”。

---

## 13. 证据等级

### A — 当前原始平台 artifact

本轮直接访问的新浪页面可作为 A 级证据证明：

- 当前 URL 返回什么；
- 当前页面显示什么博客名、内部日期、标题、正文、署名、分类和文末归属；
- 当前 profile 是否认证/填写；
- 当前目录结构和数量。

但 A 级只对**当前观察**成立。

### A/B 边界 — 历史正文内容

页面内部日期与正文构成强历史线索，而且内容高度具体、连续；但在没有同期 WARC/capture 的情况下，若 claim 涉及“2008 年服务器实际返回的精确 HTML/模板”，证据不足。

因此生活史可谨慎写：

> `当前仍存页面保存一篇内部日期为 2008-06-04 的署名职业规划文本。`

旧网技术史则不能仅据此重建：

> `2008-06-04 的新浪模板、DOM、sidebar、CSS 和资源请求链。`

### B — 制度/课程环境

中国教育和科研计算机网保存的 2008 年《大学生职业发展与就业指导课程教学要求》可以解释同期职业规划教育语境，但不能自动证明该博客作者所属具体课程采用了同一模板。

<https://www.cernet.edu.cn/edu/cooperate/crct/apr08/zcxx/200804/t20080403_289048.shtml>

---

## 14. 与媒体转载保存不同：这里是 `curation survival`

本仓其他研究已经注意到论坛帖子可能通过新闻转载幸存。这个 Sina corpus 的机制不同：

```text
individual text
→ assignment/forum collection
→ curated blog publication
→ platform survival
```

它不是记者抽取一句话重新写成新闻，而更接近 **curation survival（策展/汇编式存续）**：一批文本因为被某个职业教育出版层收集，获得统一 URL、分类和长期可搜索性。

因此：

> **survival through curation ≠ survival in original author context**

即使正文大体完整，作者自己的个人主页、同学评论、作业要求、课堂上下文和后续修改也可能完全不在同一 artifact 中。

---

## 15. 新的 archive missingness：prompt 往往比 answer 更容易消失

现在我们能看到很多“答案”——学生写好的规划；但最需要的“题目”未必同样容易找到：

- 老师到底要求写几年？
- 必须做 SWOT 吗？
- 是否有固定模板？
- 是否要求必须给出一个职业目标？
- 是否鼓励写 fallback？
- 哪些文章被选进博客？
- 是否经过教师修改？

这形成新的：

**prompt–response survival asymmetry（提示—回答存续不对称）**。

如果 prompt 消失，后来的研究者容易把受作业格式塑形的答案误读成当事人自发的叙述结构。

因此对任何课程作业、征文、问卷、论坛主题帖、博客接龙都应主动找：

```text
prompt / rubric / contest notice / syllabus / assignment instruction
```

而不是只保存回答。

---

## 16. 海外比较只作为方法对照，不扩张本仓 scope

英国高等教育在 2000 年代同期推进 Personal Development Planning / Progress File。2003 年的系统综述把 PDP 定义为结构化、受支持的个人反思与未来教育/职业规划过程：

<https://discovery.ucl.ac.uk/id/eprint/10174646/>

这个海外材料主要说明：**被高等教育制度要求记录、反思和规划未来，并非中文互联网特有现象。**

但本仓不因此扩张成英国旧网史。这里真正关心的比较只是：

- 英国很多 PDP artifact 位于内部 progress file / portfolio；
- 本轮中国样本通过公开新浪博客长期存活；
- 不同制度的发布层会改变几十年后的历史可见性。

全球生活史比较留给 `how-people-lived`。

---

## 17. 最低推理合同

处理这类页面时至少坚持：

```text
displayed student byline ≠ platform account owner
platform originality label ≠ verified authorship
contemporaneous self-description ≠ spontaneous self-description
future plan ≠ expected outcome
long route sequence ≠ deterministic belief
surviving polished plan ≠ representative future belief
internal post datetime ≠ verified capture datetime
historical-looking live page ≠ historical original bytes
current profile state ≠ historical profile state
current category count ≠ historical category count
current browser rendering ≠ historical browser experience
survival through curation ≠ survival in original author context
answer survives ≠ prompt survives
```

---

## 18. 已知 / 高概率 / 不知道

### 已知

- 当前新浪 URL 可访问；
- 当前账号展示名为“职业生涯规划”；
- 当前目录显示数千篇文章和多个职业教育分类；
- 多篇页面正文内部日期落在 2007–2010；
- 多篇文章带学生式署名、`[原创]` 标签和“大学生职业生涯规划论坛”归属；
- 当前 profile 未认证且无已填个人资料；
- 当前页面明显包含后期/当前平台 chrome。

### 高概率但仍需进一步验证

- 这是一个汇编/策展性质的职业教育发布账号，而非所有署名学生共同拥有的个人博客；
- 文本在发布时经过某种课程/论坛选择与编辑流程；
- 当前页面 body 的大部分文字来自历史期内容，而 chrome 经平台后续更新。

### 不知道

- 具体运营者和学校归属；
- 学生投稿原件；
- 课程 prompt/rubric；
- 选稿分母和拒稿比例；
- 每篇文章最早可验证的 archive capture；
- 原始 2007–2010 DOM/CSS/评论/访问统计；
- 是否发生过后期正文编辑；
- 署名学生后来的实际职业路径。

最后一项原则上也不应通过不必要的个人身份追踪来补齐。

---

## 19. 下一步

最高价值的下一步不是批量下载 9358 篇文章，而是做一个**小规模 provenance 样本**：

1. 选 5–10 篇 2007–2010 规划文本；
2. 查各自最早 archive capture；
3. 比较 live body 与最早 capture 是否一致；
4. 查“大学生职业生涯规划论坛”原始 URL/页面谱系；
5. 尝试定位课程/作业 prompt，而不是追踪普通学生现实身份；
6. 记录历史 template 与当前 template 的差异；
7. 统计样本中 fallback、时间表、SWOT、家庭/经济约束、revision acknowledgement 是否出现；
8. 明确这只是**文本类型样本**，不是学生总体比例。

如果原始论坛、prompt 或早期 capture 无法取得，应按 `docs/METHOD.md` 保存 archive gap，而不是用当前 live page 自动补成 2008 原貌。

---

## 20. 对旧网考古的新增理解

旧网页保存的不只是“当年人说过什么”，还保存了**谁有权要求别人说什么、哪些回答值得被公开、哪些页面结构帮助这些回答活下来**。

这组职业规划博客因此提供了一个新的历史可见性模型：

```text
institution elicits a future
→ person turns future into an assignment
→ editor/platform selects and publishes
→ public URL makes it searchable
→ platform survives while original classroom disappears
→ decades later researcher sees a coherent future plan
```

如果不恢复这条链，研究者很容易犯一个严重错误：

> 把“被制度要求写得像计划书、又被平台选择保存下来的未来”，误当成“那个年代的人本来就这样确定、连续、乐观地想象人生”。

因此，对生活史与旧网考古都应把 **elicitation context** 和 **publication context** 当作一等 provenance 字段。
