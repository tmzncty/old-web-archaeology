# LIFE_STAGE_ROUTING_LURKER_VISIBILITY_AND_PARENTING_COMMUNITY_ARTIFACTS_1999_2003.md

## 目的与 scope

本笔记研究 **1999–2003 中文旧网中的亲子/育儿社区对象**，重点不是写“中国网络育儿史”，而是建立旧网考古时需要额外处理的一组证据边界：

- 平台按怀孕/孩子年龄划分的社区，究竟能证明什么；
- 宝宝主页是谁的身份对象；
- 论坛发帖者与真正阅读者之间有多大可见性差异；
- 平台把原始网友讨论整理成“亲子杂志/网友讨论”页面以后，哪些上下文已经改变；
- 专家聊天室、论坛、短信、地域俱乐部和线下聚会怎样形成一个跨媒介系统；
- 今天还能打开的 2000–2003 页面，怎样与当时真正的 HTML/capture 区分。

仓库仍保持约 **1995–2015 中文互联网**的主 scope。美国 Usenet 的比较证据放在配套生活史研究中，不把本仓扩张成全球旧网史：

- <https://github.com/tmzncty/how-people-lived/blob/main/topics/care-cohorting-life-stage-routing-and-parenting-advice-stacks-china-1980-2003.zh-CN.md>

本笔记与既有文档的区别：

- `QUOTATION_SURVIVAL_AND_MEDIA_RECONTEXTUALIZATION_2009_2010.md` 主要研究论坛内容被新闻媒体摘引以后怎样存续；
- `CONTACT_STACK_AND_CHANNEL_HANDOFF_1998_2002.md` 主要研究电话/BP/Email/IM 等联系渠道之间的 handoff；
- 本笔记关注的是 **life-stage taxonomy、parent-authored child identity、lurker invisibility 和 parenting-community participation funnel**。

---

## 1. 研究对象不能只写成“育儿网站”

新浪亲子中心当前仍可访问的“社区大事记”自述显示，1999–2003 期间同一个门户体系里至少出现过：

- `SinaBaby / 新浪宝贝` 栏目；
- 宝宝个人主页；
- 育儿论坛；
- 按年龄划分的俱乐部；
- 按地域划分的俱乐部与论坛；
- 专家在线答疑/聊天室；
- 育儿短信；
- 网上亲子调查；
- “亲子杂志”式网友整理页；
- 线下妈妈宝宝聚会。

来源：

- 新浪亲子中心“社区大事记”：<https://baby.sina.com.cn/article/65_1554.shtml>

证据性质：**A/B-near-primary, surviving platform self-history**。它能够证明平台今天把这些里程碑写进自身历史；会员数、主页数属于平台自报，不能自动视作独立审计后的活跃人数。

因此考古单位至少应拆成：

```yaml
platform
section
age_club
regional_club
forum
thread
post
curated_discussion_page
expert_chat_transcript
baby_homepage
parent_account
survey
sms_service
meetup_plan
meetup_report
capture
claim
```

不能把这些统称为一个“网站页面”。

---

## 2. 新对象：life-stage taxonomy

2000-10-12，新浪亲子中心的历史页自述推出五个年龄俱乐部：

- 准妈妈；
- 0—1 岁；
- 1—2 岁；
- 2—3 岁；
- 小小少年。

2003-03-11 又增加“未准妈妈”“小学生”论坛。

来源同上。

这类结构应记录为 **life-stage taxonomy（人生阶段分类体系）**，而不只是普通 forum category。

建议字段：

```yaml
community_taxonomy:
  dimension: child_life_stage
  labels:
    - pregnant
    - age_0_1
    - age_1_2
    - age_2_3
    - older_child
  first_observed_or_claimed_date:
  source_type:
  taxonomy_version_confidence:
```

### 最低推理边界

必须明确：

> **category label ≠ verified user life stage**

一个账号进入“0—1 岁俱乐部”，不能自动证明：

- 操作者是母亲；
- 操作者本人刚生育；
- 孩子与操作者同住；
- 操作者是主要照护者；
- 孩子的实际年龄已被平台核验；
- 用户之后必然迁移到下一年龄俱乐部。

平台 taxonomy 是**界面和社区组织事实**；真实 household/life-course 状态需要独立证据。

---

## 3. 新对象：life-stage routing 不能由一张 capture 推断

如果平台提供 `准妈妈 → 0—1 → 1—2 → 2—3` 的连续分组，很容易产生一个诱人的历史叙述：

> “用户随着孩子长大自动从一个社区迁移到下一个社区。”

除非找到同一账号在多个时点的可验证记录，否则这仍是 **D — plausible reconstruction**，不能直接写成 A/B 事实。

真正要验证 life-stage routing，应尽量建立纵向链：

```yaml
actor_or_account:
observations:
  - date:
    observed_section:
    claimed_child_age:
    artifact_url:
    evidence_grade:
  - date:
    observed_section:
    claimed_child_age:
    artifact_url:
    evidence_grade:
```

### 必须区分两种“迁移”

1. **platform-routed migration**：平台 UI/规则主动推荐或自动进入下一阶段；
2. **user-chosen migration**：用户自己阅读/发帖到新的年龄社区。

目前本轮只证明平台存在年龄分组；未证明自动路由逻辑。

---

## 4. 宝宝主页不是“儿童用户主页”

平台历史页自报：

- 2000-01-07：开始网上“安家立页”；
- 2000-05-21：已有 5,000 个宝贝定制个人主页；
- 2001-02-28：18,000 个；
- 2001-12-31：40,000 个；
- 2003-07-10：80,000 个。

此外，2000-03-28 当前仍可访问的“月宝贝”页面展示了孩子姓名/小名、生日、出生体重、城市、网号等字段。

来源：

- 平台时间线：<https://baby.sina.com.cn/article/65_1554.shtml>
- 2000-03-28 月宝贝页面：<https://baby.sina.com.cn/2000-03-28/26/88.shtml>

### 关键身份边界

必须写：

> **baby homepage ≠ child-authored identity**

早期“宝宝主页”通常更应先按 **parent/guardian-authored representation of a child** 处理，除非有证据证明孩子本人在操作。

因此至少拆分：

```yaml
represented_person: child
probable_or_claimed_operator: parent_or_guardian_or_unknown
account_holder: unknown
page_author: unknown
subject_identity: child
operator_identity: unknown
```

不能因为页面标题是孩子名字，就把其行为、文体和账号活动全归给儿童本人。

### 隐私规则

这些历史页面常暴露未成年人的：

- 姓名；
- 生日；
- 城市；
- 照片；
- 早期账号/网号；
- 家庭关系。

本仓研究平台结构时不批量复制这些字段，不建立可搜索的普通儿童身份索引。只保留支持页面结构 claim 所需的最少示例信息。

---

## 5. 新的参与可见性模型：participation funnel

论坛/社区档案容易让研究者产生一种错觉：

> 看得到谁发帖，就知道谁在使用这个社区。

但在线社区至少应拆成下面的参与漏斗：

```text
可以接入平台
→ 看过栏目/帖子
→ 长期只读 / lurk
→ 注册账号
→ 加入某俱乐部
→ 发过帖
→ 被其他用户回复
→ 被编辑选入整理页
→ 参加线下活动
```

这些层不能互相替代。

建议字段：

```yaml
participation_state:
  reachable: unknown
  reader: unknown
  recurring_reader: unknown
  registered: unknown
  club_member: unknown
  poster: unknown
  curated_or_featured: unknown
  offline_participant: unknown
```

### 新的硬规则

> **poster population ≠ reader population**

> **registered population ≠ active population**

> **club member count ≠ unique household count**

> **featured user ≠ representative user**

> **offline attendee ≠ ordinary online member**

中文旧网本轮没有找到足够强的同期“长期潜水者自述”，因此这个 participation funnel 的“lurker 很重要”部分主要由配套生活史中的 1994 `misc.kids` 海外对照提供方法提醒；在本仓不能因为海外证据存在，就把中国早期亲子论坛的 lurker 比例直接填出来。

---

## 6. 2001 的网友整理页：contemporaneous material，但不是原始完整 thread

两个很有价值的新浪存续页面：

1. 2001-11-28，《南方无暖气，宝宝怎过冬》  
   <https://baby.sina.com.cn/mag/2001-11-28/60_4382.shtml>
2. 2001-12-30，《众网友讨论：当两代人育儿观念冲突时》  
   <https://baby.sina.com.cn/news/2001-12-30/5534.shtml>

都明确显示由“新浪网友”整理，并在正文中排列若干网友经验。

它们非常适合证明：

- 平台当时公开汇集此类育儿问题；
- 用户经验已经进入平台内容生产；
- 论坛/网友讨论可以被编辑成相对独立的内容页；
- 生活细节（洗澡、暖气、托儿所接送、祖辈冲突等）确实进入公开网络文本。

但必须写：

> **curated discussion page ≠ original complete thread**

整理页不能自动证明：

- 原始 thread URL；
- 原帖准确发布时间；
- 回复的原始顺序；
- 是否删除过内容；
- 哪些帖子没有被选入；
- 编辑是否改写标点、标题或长度；
- 原帖作者账号与整理页署名是否完全对应；
- 原始论坛页面的 UI、分页、签名、头像和邻接内容。

### 与 quotation survival 的区别

`QUOTATION_SURVIVAL_AND_MEDIA_RECONTEXTUALIZATION_2009_2010.md` 处理“论坛 → 新闻媒体”的跨机构再语境化；这里更多是：

```text
平台内部网友讨论
→ 同平台编辑/网友整理
→ 亲子杂志/新闻式永久页面
```

它是 **intra-platform curation**。

建议增加：

```yaml
content_origin:
  original_thread: unknown
  original_post: unknown
  curated_from_user_material: true
curation:
  editor_or_compiler_visible: true
  selection_criteria: unknown
  editing_extent: unknown
  original_context_preserved: partial_or_unknown
```

---

## 7. “讨论活着”不等于“建议被采用”

育儿材料特别容易造成因果过度推断。

例如《南方无暖气，宝宝怎过冬》可以证明用户分享“中午洗澡、利用热水器、快速包裹”等实际操作；《两代人育儿观念冲突》可以证明用户公开讨论祖辈与父母的分歧。

但不能从页面存续推出：

- 阅读者采纳了建议；
- 建议在医学上正确；
- 某种做法因此普及；
- 代际冲突因此减轻；
- 论坛比医生/纸媒/亲属更有权威。

硬规则：

> **advice visible ≠ advice adopted**

> **peer consensus ≠ expert validity**

> **thread activity ≠ behavioral diffusion**

如果要证明行为改变，需要后续帖子、日记、访谈、调查或其他独立证据。

---

## 8. 专家聊天室是另一个 artifact family

2002-04-28，新浪保存了一场儿童保健专家与家长讨论早期教育的在线访谈/答疑页面：

- <https://baby.sina.com.cn/news/2002-04-28/6650.shtml>

同一平台历史页还记载：

- 2001-02-20 专家答疑改版；
- 2001-03-09 儿科专家做客嘉宾聊天室；
- 2001-09-25 专家答疑再次改版并增加专家；
- 2001-05-15 开通育儿专家提示短信。

这表明考古“育儿社区”时，不能只搜索 `forum`。

最小 channel map：

```yaml
care_information_channels:
  peer_forum:
  curated_peer_article:
  expert_article:
  expert_live_chat:
  expert_qa:
  sms_tip:
  baby_homepage:
  regional_club:
  offline_meetup:
```

### 专家 transcript 的边界

> **expert chat transcript ≠ clinical encounter**

不能默认：

- 专家核验了提问者/孩子完整病史；
- 用户得到了个体化医疗诊断；
- 用户执行了建议；
- 页面中的“专家”身份在所有时间点均由平台以同一方式认证。

本仓只记录页面可证的角色、机构介绍和互动形式。

---

## 9. 地域俱乐部与线下聚会：regional label ≠ residence, meetup plan ≠ attendance

平台历史页记载 2001-03-06 开通四个地域俱乐部/论坛；2001–2003 又列出北京、南京、天津、青岛等多地妈妈宝宝聚会。

一篇 2001-02-27 的“五一大聚会”策划页甚至列出：

- 外地与北京家庭预计人数；
- 住宿；
- 交通；
- 儿童食品；
- 药箱；
- 北京网友帮助外地网友减少携带用品等安排。

来源：

- <https://baby.sina.com.cn/news/2001-02-27/1815.shtml>

这证明线上社区至少能被用来组织现实活动和资源协调。

但应严格区分：

> **regional club membership ≠ verified residence**

> **meetup proposal ≠ event occurred exactly as planned**

> **event report/photo ≠ complete attendance list**

> **offline participation ≠ representative platform use**

对普通家庭线下活动尤其不应复制名单、联系电话、孩子身份等无必要私人信息。

---

## 10. current survivor ≠ verified historical capture

本轮使用的新浪页面有一个共同特点：

- URL 今天仍能返回内容；
- 页面正文内部显示 2000–2003 日期；
- 但我们本轮并没有为每个 URL 建立 Wayback/WARC 的原始历史 capture 链。

因此必须延续仓库已有的 temporal-composite 规则：

```yaml
internal_article_date: 2001-11-28
current_observation_date: 2026-09-03
historical_capture_datetime: unknown
historical_html_verified: false
current_survivor: true
```

不能写：

> “这是 2001 年原始 HTML 的精确保存。”

只能写：

> “这是今天仍可访问、内部标有 2001 年日期的新浪历史内容页；正文历史性较强，但模板/脚本/链接/广告等是否保持原状需要 capture-level 验证。”

---

## 11. 旧网亲子社区的特殊历史可见性偏差

### 11.1 lurker visibility gap

只读用户通常没有 post URL，因此在 archive 里接近不可见。

结果：

> archived voices overrepresent people willing/able to post.

### 11.2 curation selection bias

“众网友讨论”整理页只保存被编入文章的回复。

结果：

> surviving curated voices ≠ original discussion distribution.

### 11.3 successful-community bias

大型聚会、获奖宝宝、专家活动、热门话题更容易获得独立永久 URL。

结果：

> ordinary reading day ≠ event-heavy surviving corpus.

### 11.4 child-representation bias

宝宝主页能让孩子成为极高可见度的页面 subject，但页面生产者通常是成年人。

结果：

> represented child visibility ≠ child agency.

### 11.5 problem visibility bias

“孩子哭闹怎么办”“两代育儿冲突”“冬天怎么洗澡”天然适合提问和讨论；没有出问题、照常完成的护理通常不会留下同等密度文本。

结果：

> archived care corpus may overrepresent uncertainty and conflict.

### 11.6 advice-outcome gap

平台保存建议，不保存大多数家庭后来是否执行以及结果。

结果：

> advice archive is much richer than outcome archive.

---

## 12. 建议的 parenting-community artifact schema

```yaml
object_type: parenting_community_artifact
platform:
section:
original_url:
capture_url:
capture_datetime:
current_survivor: false
current_observed_at:
internal_date:

artifact_subtype:
  forum_thread: false
  post: false
  curated_discussion: false
  expert_chat: false
  age_club: false
  regional_club: false
  baby_homepage: false
  survey: false
  meetup_plan: false
  meetup_report: false

life_stage_taxonomy:
  visible: false
  label:
  user_stage_verified: false

identity_model:
  account_operator: unknown
  represented_person: unknown
  author_claimed_role: unknown
  identity_verified: false
  minor_data_present: false

participation:
  registered: unknown
  club_member: unknown
  poster: unknown
  reader_or_lurker: unknown
  curated_or_featured: unknown
  offline_attendee: unknown

curation:
  curated_from_user_material: unknown
  compiler_visible: unknown
  original_thread_known: unknown
  selection_process_known: unknown

channel_handoff:
  forum_to_expert: unknown
  forum_to_sms: unknown
  online_to_offline: unknown
  offline_to_web_report: unknown

behavioral_outcome_known: false
medical_or_safety_claim_present: false
privacy_risk:
evidence_grade:
confidence:
notes:
```

---

## 13. Claim checklist

研究中文旧网育儿/家庭社区时，每条 claim 至少问：

1. 我说的是平台、栏目、club、thread、整理页还是主页？
2. 日期是正文内部日期、平台自报里程碑还是 archive capture datetime？
3. “宝宝主页”是谁写的？谁只是被表示？
4. 年龄分组是 UI taxonomy 还是现实身份核验？
5. 会员数是累计注册、活跃用户、账号还是家庭？
6. 看到的是原 thread 还是整理后的精选回复？
7. 发帖者之外，有没有无法观察的长期读者？
8. 专家回答是一般教育信息还是个体医疗建议？
9. 建议被看到，是否有独立证据证明被执行？
10. 地域 club 是否真的验证居住地？
11. 线下活动是计划、报告还是实际名单？
12. 页面今天可访问，是否已验证历史 capture？
13. 是否正在不必要地重新公开儿童姓名、生日、照片或旧账号？

---

## 14. 已证实 / 高概率 / 不知道

### 已证实

- 新浪亲子当前历史页明确声称 1999 开始 SinaBaby/新浪宝贝，2000 年扩展论坛与按年龄俱乐部，2001 年增加地域社区、专家答疑和短信等功能；
- 2001–2002 当前存续页保存了网友育儿讨论整理和专家在线交流文本；
- 2001 年已有公开的线上网友线下聚会策划材料；
- 2000 年当前存续页面证明“宝宝”可以作为页面 subject 并显示生日、城市等结构化字段。

### 高概率但仍需 capture-level 复核

- 这些页面的正文主体确实源自其内部标注的 2000–2002 时期；
- 论坛、主页、年龄俱乐部构成了一套相互链接的亲子社区结构。

### 不知道

- 每个页面当年最初上线的 exact HTML/CSS/JS；
- 每个年龄 club 的真实活跃用户数；
- 普通用户中只读者比例；
- 同一账号是否按孩子年龄连续迁移社区；
- 被整理页遗漏的原始回复；
- 多少在线建议真正改变家庭行为；
- 当前幸存页面与当年页面外壳之间具体改动多少。

---

## 15. 下一步考古任务

优先级最高的不是再找更多今天能打开的新浪文章，而是：

1. 为 `2000-10-12` 年龄俱乐部、`2001-03-06` 地域论坛和 2001–2002 整理页定位可实际打开的 archive captures；
2. 查找原始 thread URL pattern，判断“亲子杂志/网友整理”从哪里取材；
3. 找同一普通账号跨两年以上的主页/论坛记录，测试 life-stage routing；
4. 找中文同期 lurker / “只看不发”自述，建立本土 participation visibility 证据；
5. 建一个宝宝主页 privacy-safe schema，只记录字段结构，不批量保存个人身份；
6. 比较 2000、2003、2006、2009 的亲子首页，观察生命周期分类、论坛、博客、相册、WAP/手机入口如何改变；
7. 对专家聊天室与普通论坛分别记录 archive completeness，避免把公开 transcript 的高存续率误当作普通用户互动的高存续率。

本轮新增的是 **life-stage taxonomy、participation funnel、lurker visibility gap、parent-authored child representation 与 parenting-specific curation boundary**，不属于既有文档的重复补例。
