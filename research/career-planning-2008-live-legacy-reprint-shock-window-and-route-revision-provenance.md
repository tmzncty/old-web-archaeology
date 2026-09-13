# 2008 职业规划 live-legacy 页面、路线修订与 shock-window provenance 升级

> Scope：2008 年中文 Web 中与大学职业规划、招聘反馈和金融危机相关的 **current live legacy pages / repost lineage / internal dates**。  
> 这是一份 evidence/provenance upgrade，不新造新的 `*_STATE_GAPS_*` 领域，也不宣称完成 M1。  
> 交叉生活史包：`tmzncty/how-people-lived/sources/evidence-upgrade-career-planning-market-contact-shock-and-revision-china-2008.zh-CN.md`。

## 0. 去重与本轮目标

仓库已经有：

- `docs/ELICITED_FUTURES_CURATED_COURSE_BLOG_AND_TEMPORAL_COMPOSITES_2007_2010.md`；
- `docs/SHOCK_WINDOW_AND_FUTURE_INTENT_EVIDENCE_2008.md`；
- `docs/NEWS_REPOST_SOURCE_LINEAGE_PUBLICATION_TIME_AND_CONTEMPORARY_VOICE_GAPS_1998_2015.md`。

因此本轮不再重复：

```text
internal post date != archive capture date
current legacy page != verified historical capture
reprint != independent evidence family
future plan != later outcome
```

新增价值只在三点：

1. 把一条 2008-04-11 的**计划遇到招聘市场后被明确改写**的同期采访接进现有 future-plan 证据链；
2. 记录它今天实际存活在哪个 Web 层、页面自己怎样标源；
3. 把 2008-12-31 同一新浪“职业生涯规划”出版层中的金融危机文本接进 shock-window 方法，而不把当前 live rendering 冒充 2008 capture。

---

## 1. Artifact A：CERNET 当前仍存活的 2008-04-11 新华网转载

当前 URL：

- https://cernet.edu.cn/edu/jiao_yu_yan_jiu/200804/t20080411_290253.shtml

当前可观察：

- 标题：`高校职业生涯规划课程，为何难成就业万灵丹?`
- 页面正文头部标示：`2008-04-11 新华网 曹馨月;简小娟`
- 当前 host：`cernet.edu.cn`
- 当前页面外壳明显包含今天仍在更新的 CERNET 导航、推荐和站点元素；
- 正文则保存 2008 年采访叙事与学生直接陈述。

因此最安全的对象模型是：

```yaml
artifact_type: current_live_legacy_reprint
current_host: cernet.edu.cn
internal_publication_date: 2008-04-11
body_source_label: 新华网
body_byline: 曹馨月;简小娟
original_xinhua_url: unknown
archive_capture_datetime: null
historical_capture_verified: false
retrieved_2026: true
```

### 1.1 为什么这条正文值得加入 life-history 证据链

正文记录：

- 一名化学化工学院大四学生按照课程形成了“研究部门 -> 大企业管理”的完整路线，但实际应聘不顺；
- 一名法学院大三学生原本准备“律师事务所 -> 积累经验 -> 自己开所”，在参加几次招聘会后放弃原计划，准备转向中学教师；
- 一些学生认为课程理论性太强，不能完全解决择业就业问题；
- 教师也承认“有目标”不等于能够一步步落实。

OWA 不负责证明哪个职业更好；这里的考古意义是：**同一页同时保存了 elicited plan、market contact 与 route revision 三种时间状态。**

这比只保存一篇完整规划书更接近历史中的“未来如何被改写”。

---

## 2. Source-lineage 状态：知道 body 标源，不等于已经恢复 original

当前 CERNET 页明确把来源写成“新华网”，但本轮针对标题在 `xinhuanet.com` 的精确 Web 检索没有找到可直接打开的原始页面。

因此不能写：

```text
Xinhua original recovered
```

只能写：

```text
current CERNET live legacy reprint
+ body-level attribution to Xinhua
+ original URL not recovered in this run
```

推荐字段：

```yaml
source_lineage:
  current_survivor: cernet.edu.cn
  displayed_origin_publication: 新华网
  displayed_origin_date: 2008-04-11
  origin_url: null
  origin_page_opened: false
  repost_family_counted_as_independent_evidence: false
```

这不是一个新的 preservation mechanism，只是把 `NEWS_REPOST_SOURCE_LINEAGE...` 的规则落实到一个具体 future-intent artifact。

---

## 3. Artifact B：2008-04-28 搜狐保存的新华社招聘会报道

当前 URL：

- https://business.sohu.com/20080428/n256564934.shtml

当前页面标示：

- 日期：`2008年04月28日`
- 来源：`新华网`
- 标题：`职业规划是大学生进入社会前应做的关键工作`

正文包含同期求职学生的直接引语：在工作难找的情况下，岗位“差不多”就先签，是否合适以后再说；另有软件学院毕业生在考研与工作之间长期摇摆，考研失败后决定先工作。

artifact 模型同样是：

```yaml
artifact_type: current_live_legacy_reprint
current_host: business.sohu.com
internal_publication_date: 2008-04-28
body_source_label: 新华网
historical_capture_verified: false
```

### 方法价值

这条材料发生在 2008 年 4 月，不能后见式全部归因于 2008 年晚期金融危机。它适合和现有 `SHOCK_WINDOW...` 配合：

> **短期化、satisficing 和路线切换并非只有急性宏观冲击以后才出现。**

因此未来做时间比较时，不能把：

```text
late-2008 defensive language
```

自动当作：

```text
all defensive employment behavior was created by the global financial crisis
```

---

## 4. Artifact C：2008-12-31 新浪职业规划出版层中的金融危机文本

当前 URL：

- https://blog.sina.com.cn/s/blog_56c922450100buz9.html

当前可观察：

- 标题：`[原创]在金融危机的当下 为了将来我们应该做些什么`
- 内部博文时间：`2008-12-31 08:50:59`
- 分类：`自我探索与职业选择`
- 正文署名：一名 `06级大三 国际贸易` 学生；
- 正文直接把全球金融危机、出口企业倒闭、失业增加和大学生就业困难放进“为了将来应该做些什么”的问题框架。

按照现有 `ELICITED_FUTURES...` 的规则，这个页面必须拆成：

```yaml
platform: sina-blog
platform_account: "1456022085 / blog_56c92245... publication layer"
internal_post_datetime: 2008-12-31T08:50:59
student_byline_present: true
account_owner_equals_student: not_established
platform_originality_label: 原创
authorship_independently_verified: false
current_live_rendering: true
archive_capture_datetime: null
historical_capture_verified: false
```

### 为什么它与 shock-window note 相接

现有 shock-window note 已经有年初调查、年末调查和 12 月招聘会中的未来偏好变化；这条新 artifact 增加的是**同一个职业规划 publication layer 自己吸收了冲击语言**。

因此可以把 2008 年内部时间进一步拆成：

```text
课程要求“管理未来”
+
急性经济冲击改变就业信息环境
→
同一套规划语法开始把风险本身当成规划对象
```

但仍不能推断该学生代表全体，也不能从当前 live 页恢复当时博客模板、评论、阅读量或互动。

---

## 5. 一个很重要的证据组合：三页都“像 2008”，但不是三份已验证 2008 capture

本轮三个对象今天都能直接打开，并且正文/页面内部都携带 2008 年日期。

但证据状态仍然是：

```text
2008 internal date / body provenance
+
2026 current live retrieval
!=
verified 2008 archive capture
```

因此本轮**没有**把以下字段填成已确认：

- 2008 当时的 HTTP status；
- Content-Type / charset header；
- 当时 DOM；
- CSS / JS / 图片资源完整性；
- 评论区是否存在、是否完整；
- 当时页面模板；
- 当时站内链接结构；
- Xinhua 原始 URL；
- 同一页面第二历史时点的变化。

这三页的价值首先是**文本与来源线索的 live-legacy survival**，不是 Memento replay。

---

## 6. 与现有 OWA 方法文档的关系

### `ELICITED_FUTURES...`

本轮补入一种比“完整计划书”更有价值的文本状态：

```text
plan already formulated
→ labour-market encounter
→ explicit revision
```

这说明 future-plan artifact 的理想研究单位不应永远停在单篇文章；更高价值的是能连接 revision chain 的同一人 / 同一时段材料。

### `SHOCK_WINDOW...`

本轮把 2008-04 和 2008-12 放在同一年内对照，进一步说明：

- 4 月已存在就业困难与短期 fallback；
- 12 月金融危机已经直接进入职业规划文本；
- 因此 year-level label 仍然过粗。

### `NEWS_REPOST_SOURCE_LINEAGE...`

CERNET 与搜狐两页都把“新华网”作为 body-level source attribution，但这不等于已经取得两个独立来源，也不等于原始 Xinhua 页面已经恢复。

---

## 7. 海外对照只放证据边界，不扩仓 scope

本轮同时检查了 2008 年苏格兰高校 PDP 研究。研究项目自 2006 年起在四所大学展开，21 名实际经历 PDP 的学生对其学业/职业关联帮助评价并不高，批评集中于 ownership、relevance、staff engagement 和真实就业连接不足；没有 PDP 经验的学生反而普遍更乐观。

来源：

- https://www.tandfonline.com/doi/full/10.11120/elss.2008.01020002

这只作为 how-people-lived 的跨国比较。OWA 不把它纳入中文旧网主 scope。

它的考古启发只有一条：**制度说明页表达“PDP 应当怎样运作”，学生同期材料表达“它实际怎样被体验”，两类 artifact 不能互相替代。**

---

## 8. M1 状态

本轮没有获得一个满足 `docs/METHOD.md` 的历史 capture pair。

```yaml
current_live_legacy_pages_opened: 3
period_internal_dates_present: true
body_source_lineage_present: true
original_xinhua_url_recovered: false
verified_historical_memento: false
second_historical_timepoint: false
runtime_replay: false
m1_complete: false
```

所以准确表述是：

> `2008-dated live legacy text and source-lineage evidence strengthened; historical capture not verified in this run.`

不是：

> `2008 页面已经复原。`

---

## 9. 下一步最高价值动作

这条线以后若继续，优先级应是：

1. 为新浪同一职业规划账号找到并实际打开 2007–2010 至少两个 historical mementos；
2. 比较历史目录、页面模板、评论/互动与今天的 temporal composite；
3. 追原始新华网 URL，而不是把 CERNET / 搜狐转载重复计数；
4. 如果能找到同一学生相隔数月/一年发布的计划与修订，建立真正的 revision chain；
5. 优先保存公开结构和 provenance，不为了追踪“后来过得怎样”去识别普通学生现实身份。

---

## 10. 本轮结论

这轮没有产生新的 OWA state-gap 理论，价值是把现有方法推进到更好的**时间链证据**：

```text
被制度要求表达未来
→ 形成公开计划文本
→ 接触招聘市场
→ 路线被改写
→ 宏观冲击进入新的未来文本
```

而旧网保存的三个层次必须继续分开：

```text
当时的未来状态
!=
页面内部写着的历史日期
!=
今天还能打开的 legacy rendering
!=
真正核验过的 historical capture
```

这条区分比再新增一个“职业规划 state gap”文件更有价值。