# CHILDLESS / DINK / DELAYED PARENTING / REPRODUCTIVE-INTENTION STATE GAPS, 1999–2015

Status: research note / state-gap model  
Scope: 约 1999–2015 中文论坛、贴吧、博客、门户转载与社区页面中围绕“丁克 / 不生 / 暂时不生 / 被丁克 / 什么时候生”的公开状态；不把仓库扩展成生育史或全球 Internet 史  
Cross-repo companion: `tmzncty/how-people-lived/topics/from-when-to-have-children-to-whether-to-have-them-parenthood-optionality-childlessness-and-reproductive-intention-china-1997-2026.zh-CN.md`

## 0. Why this belongs in old-web archaeology

旧网里看到一个标题：

```text
“我不想生孩子”
“丁克家庭”
“我现在适合生孩子吗？”
```

最危险的研究错误，是直接把页面上的一句自述转换成整个人生的最终状态。

对于这种材料，至少存在：

```text
现实家庭状态
→ 当时本人的生育意向
→ 伴侣的意向
→ 账号选择公开的叙述
→ 标题/标签
→ 回复与争论
→ 媒体摘引与再命名
→ 后续生活变化
```

因此本 note 研究的不是“谁最终生没生”，而是：

> **中文旧网怎样把某一时点的家庭/生育意向变成可搜索、可回复、可转载的页面状态；档案今天又能证明到哪一步。**

---

## 1. Research units

依照 `docs/METHOD.md`，必须拆开：

- `platform`
- `host`
- `board_or_group`
- `thread`
- `post`
- `reply`
- `account`
- `self_label`
- `media_label`
- `reproductive_intention_at_time_t`
- `observed_family_state_at_time_t`
- `later_outcome`（通常 unknown）
- `historical_locator`
- `capture`
- `claim`

尤其禁止：

```text
account == person == household == couple
```

一个账号发帖最多直接证明这个账号在该时点公开了某种叙述。

---

## 2. The primary state distinction

旧网页里的“无孩”至少拆成：

```text
observed_no_child_state
├── intention_unknown
├── assumed_future_parenthood
├── deliberate_delay
├── uncertain_or_ambivalent
├── voluntarily_childfree_at_t
├── partner_mismatch
└── wants_parenthood_but_not_realized
```

因此固定：

```text
childless_now ≠ childfree_by_choice
childfree_label ≠ permanent lifetime outcome
post at t1 ≠ intention at t2
one partner's post ≠ couple consensus
```

本文称为：

**life-course label / outcome gap — 生命历程标签 / 最终结果缺口。**

---

## 3. 1999：门户/报纸已经把“丁克”变成可索引公共对象，但这仍不是论坛 transaction

1999 年《生活时报》刊载《中国大城市出现“丁克族”》，采访北京几对长期没有孩子的夫妻，记录他们关于竞争、事业、夫妻关系与抚养成本的解释。

Current surviving news page:

- https://www.gmw.cn/01shsb/1999-10/05/GB/shsb%5E1122%5E0%5ESH5-509.htm

Evidence grade: **B：同时代报纸内容的当前 Web survivor。**

这能证明：

- 1999 年相关家庭形态已经进入大众媒体公共叙述；
- Web 今天还能寻址这篇同期文章；
- 当时普通读者不需要先进入一个专门论坛，已经可能通过报纸接触这种标签。

但不能证明：

- 这就是 1999 年用户看到的原始 Web DOM；
- 页面今天的 charset/模板与当时完全相同；
- 被采访家庭后来一直无孩；
- 这些受访者代表城市夫妻总体。

这属于：

**news-survivor / original-render gap。**

---

## 4. 2010：一个非常具体的 Chinese old-Web locator——但不是 verified capture

2010-07-16 的报道记录：记者在百度贴吧“哈尔滨吧”看到帖子：

```text
我现在的情况适合生孩子吗？
```

并称随后联系到发帖者“小燕”（化名）。报道里的她结婚三年、夫妻租房、收入较低，明确表达：希望经济和住房条件改善后再考虑孩子；亲友把他们称作“丁克”，她则用“被丁克”解释自己的状态。

Near-contemporary media survivor:

- Sina / 国际在线：https://news.sina.com.cn/o/2010-07-16/160517817925s.shtml
- Sohu / 新华转载链：https://news.sohu.com/20100716/n273547343.shtml

Evidence grade: **B + 同期第一人称（媒体中介）。**

### 4.1 Multiple URLs do not equal independent evidence

新浪、搜狐等版本明显属于同一报道传播链。

所以：

```text
3 repost URLs
≠ 3 independent evidence families
```

这遵守 `docs/METHOD.md` 的独立来源规则。

### 4.2 Historical locator state

本轮获得的 locator 是：

```text
platform = 百度贴吧
board = 哈尔滨吧
thread_title = 我现在的情况适合生孩子吗？
reported_at = 2010-07
```

但**没有取得原帖 URL，也没有实际打开并检查一份 Wayback/WARC memento**。

因此以下全部保持 unknown：

- exact thread id / URL；
- original post datetime；
- original charset / HTTP Content-Type；
- DOM；
- pagination；
- whether title/body was later edited；
- reply count at the reporter's encounter time；
- deleted replies；
- cookie/session state；
- author profile metadata；
- whether current/replayed page would match 2010 browser behavior。

Candidate locator ≠ verified capture。

---

## 5. Media relabeling gap

2010 案例特别适合说明：

```text
poster: “条件改善后再考虑孩子”
relatives/media shorthand: “丁克 / 被丁克”
```

标签可能由：

- 本人；
- 伴侣；
- 亲友；
- 论坛回复者；
- 记者；
- 编辑标题；
- 后来的研究者；

分别赋予。

必须记录：

```text
label_actor
label_time
label_text
```

而不是只存一个 `dink=true`。

本文称为：

**media-relabeling gap — 媒体再标签缺口。**

同一家庭可能在不同页面被写成：

- 丁克；
- 被丁克；
- 暂缓生育；
- 经济压力家庭；
- 年轻夫妻。

这些不是可互换的数据库值。

---

## 6. Thread title is not full intention state

一个标题为了获得回复，经常把复杂问题压缩成一句：

```text
“我该不该生？”
“我不想生，我错了吗？”
```

因此：

```text
thread_title
≠ complete_post_position
≠ later clarification in replies
≠ offline decision
```

如果只剩搜索结果或媒体标题，研究者尤其容易误把标题当成作者最终立场。

这叫：

**title / deliberation gap — 标题 / 决策过程缺口。**

---

## 7. Reply-state gaps

人生决策帖至少需要拆：

```text
post submitted
→ server persisted
→ thread publicly visible
→ indexed / surfaced
→ other user encountered
→ reply submitted
→ author later returned
→ author actually read reply
→ reply affected deliberation?
→ offline conversation with partner/family
→ later decision
```

因此固定：

```text
reply exists ≠ poster saw it
poster saw it ≠ believed it
many replies ≠ consensus
forum consensus ≠ population norm
online support/opposition ≠ offline outcome
```

档案通常最多证明其中前半段。

---

## 8. Account identity and couple-state gaps

生育意向属于高度私人状态。

旧论坛账号可能：

- 纯昵称；
- 一次性账号；
- 借用账号；
- 夫妻其中一方；
- 为保护隐私而改写年龄、收入、城市；
- 被媒体进一步化名。

所以：

```text
account profile
≠ verified civil identity
```

更不能：

```text
one poster's intention
→ infer spouse's private intention
```

即使媒体后来声称“联系到本人”，也只提高那个**媒体访谈 claim** 的置信度，不把论坛账号变成一个可供研究者重新识别的现实档案。

### Privacy stop condition

不要为了确认“后来有没有孩子”而：

- 用旧用户名 + 城市 + 工作单位做人肉搜索；
- 拼接手机号/QQ/真实姓名；
- 尝试登录旧账号；
- 使用泄露数据库；
- 重新公开生殖健康、医疗或家庭冲突隐私。

**later outcome unknown** 是允许、而且在这里通常应当保留的状态。

---

## 9. “丁克吧”与专题社区：存在标签空间，不等于成员共享一种固定人生

2018 年同期采访中，一名受访者提到自己有时会去“丁克吧”浏览；这超出本文核心 1999–2015 artifact 的直接证据期，只作为平台连续性边界提示。

对应 how-people-lived source:

- https://www.chinanews.com.cn/m/sh/2018/04-13/8489926.shtml

这里不能反推：

- 2010 年“丁克吧”的具体页面结构；
- 某用户实际发过帖；
- 吧内用户全是终身自愿无孩；
- 浏览者一定加入社区身份。

因此：

```text
group/topic label exists
≠ membership identity
≠ stable lifetime intention
```

这与仓库已有论坛研究的 `group state ≠ member state` 原则一致。

---

## 10. Old-Web-specific temporal state model

建议对这类页面至少保存以下字段：

```yaml
platform: baidu-tieba
board_or_group: "哈尔滨吧"
thread_title: "我现在的情况适合生孩子吗？"
thread_url: unknown
post_datetime: unknown
media_encounter_datetime: 2010-07
poster_self_label: "被丁克"   # 仅媒体访谈中的自述
observed_child_state: no_child_at_interview
intent_state: wants_child_later_if_conditions_improve
partner_intent_state: incompletely_observed
later_outcome: unknown
evidence_grade: B
archive_capture_verified: false
privacy_reidentification_allowed: false
```

关键是：

> **不要把 `later_outcome: unknown` 擅自补成 yes/no。**

---

## 11. Archive survival biases

### 11.1 conflict-post survival bias

最容易被搜索、转载的是：

- 标题冲突强；
- 婆媳/父母压力大；
- “生 / 不生”立场鲜明；
- 房价、工资数字有新闻性；
- 回复量高。

最难留下的是：

- 夫妻平静协商后暂缓几年；
- 没发帖；
- 看帖但不回复；
- 后来慢慢改变主意；
- 没有戏剧性冲突的长期无孩生活。

因此 archive 很可能高估：

**reproductive-intention conflict visibility — 生育意向冲突的历史可见性。**

### 11.2 media-survivor / forum-loss asymmetry

2010 案例现在最稳定的可访问证据是新闻转载，而不是原贴吧 transaction。

于是很容易形成：

```text
media quotation survives
original thread lost/unknown
```

记者挑选的句子、标题和类别可能比原始讨论活得更久。

本文称为：

**media-survivor / forum-loss asymmetry。**

### 11.3 outcome silence

发帖者后来如果：

- 生了孩子；
- 坚持无孩；
- 离婚；
- 改变城市；
- 只是忘了账号；

都可能不再回来更新。

所以：

```text
no update
≠ no life change
```

---

## 12. Browser / encoding / archive boundary

本轮没有 verified historical capture，因此不猜：

- 2010 Tieba exact DOM；
- GBK / UTF-8 / response headers；
- IE6/IE8 specific behavior；
- pagination endpoint；
- login requirements；
- image host；
- JS reply behavior；
- deleted-post placeholder style。

搜索引擎今天找到一个旧标题，也只证明：

> 当前搜索系统返回了一个历史相关 locator / media survivor。

不等于：

> 我们已经拥有当年用户看到的原页面。

---

## 13. What old-Web evidence can and cannot tell life history

### Can support

- 某一时点某种生活脚本进入公共中文 Web；
- 某账号公开表达怎样的意向；
- 同时有哪些反对、支持或替代叙述；
- 平台如何组织标签、主题、回复与搜索；
- 媒体怎样从论坛选取并重命名一个故事；
- 哪些页面状态容易幸存。

### Cannot automatically support

- 全国有多少人这样生活；
- 作者现实身份；
- 伴侣真实意见；
- 作者最后是否成为父母；
- 回复造成了什么因果影响；
- 今天的页面 UI 就是历史 UI；
- 一个“丁克”标签对应单一稳定的人生类别。

---

## 14. Cross-repo significance

对于 `how-people-lived`，旧网最重要的贡献不是给“丁克人数”再添一个计数，而是提供：

**reproductive-life-script observability — 生育人生脚本可观察性。**

1990s 报刊已经能让普通人知道“不成为父母”的家庭存在；论坛/贴吧进一步让人直接看见：

- 主动不想生；
- 想晚点生；
- 条件不允许；
- 伴侣意见不一致；
- 后来改变想法；
- 成为父母以后又怎样理解代价和满足。

但 old-Web 也强迫生活史研究保留一条重要限制：

> **互联网保存的是一个人在某个时刻公开说出来的未来，不是她后来完整走完的人生。**

---

## 15. Current negative result / next M1 candidate

本轮已取得：

- 1999 同期新闻 survivor；
- 2010 百度贴吧板块 + 精确 thread title 的媒体 locator；
- 2010 同一故事的转载传播链；
- 2018 后续平台连续性线索。

但**没有取得并实际验证一份满足 M1 的 1999–2010 中文“丁克 / 暂缓生育”论坛 Wayback/WARC capture**。

因此当前状态是：

```text
historical locator: yes
verified memento: no
original DOM: unknown
original charset: unknown
thread transaction state: unknown
later life outcome: intentionally unknown
```

未来若继续 M1，优先寻找：

1. 2010 百度贴吧《我现在的情况适合生孩子吗？》可验证 memento 或原 URL；
2. 2000s 独立论坛/博客中有明确时间戳、可打开 archive capture 的“丁克 / 不生 / 晚生”讨论；
3. 同一线程至少两个时点，用来证明 edit / reply / deletion / pagination state。

若只剩媒体转述，按 METHOD stop condition 保留为 B 级 research note，不补造历史页面。
