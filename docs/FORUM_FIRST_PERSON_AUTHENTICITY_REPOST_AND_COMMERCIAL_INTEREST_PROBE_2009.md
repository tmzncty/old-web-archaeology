# FORUM FIRST-PERSON AUTHENTICITY / REPOST / COMMERCIAL-INTEREST PROBE, 2009

Status: narrow evidence-method / artifact probe  
Scope: 2009 年成都论坛中传播的“AA 拼房结婚”帖及其同时代媒体查证；用于 ordinary-life / life-history 项目的第一人称证据真实性边界，不扩展成房地产营销史，也不把一个可疑帖子写成“2009 青年婚姻观”总体结论。  
Cross-repo companion: `tmzncty/how-people-lived/topics/what-made-marriage-economically-possible-china-1998-2024.zh-CN.md`

## 0. Why this probe exists

旧论坛、博客和个人主页最有价值的一类材料，是同时代第一人称。

但一个非常危险的捷径是：

```text
first-person grammar
+
contemporaneous publication
=
authentic ordinary-life autobiography
```

这条等式不成立。

2009 年成都论坛中传播的一则“AA 拼房结婚”帖提供了一个很好的反例，因为**同期记者在帖子仍然活跃传播时就对其真实性和商业动机提出了明确质疑**。

因此本 note 不是为了证明帖子一定是房地产公司策划。

它要证明的是一个更窄、但对整个仓库非常重要的方法结论：

> **同时代、第一人称、细节丰富、跨多个论坛传播，仍然不足以证明叙述者就是那个真实生活事件的当事人。**

---

## 1. Research unit

至少拆成：

```text
underlying real person / event (if any)
→ original composition of text (unknown)
→ first known forum post (unknown)
→ reposting account(s)
→ local forum page(s)
→ cross-forum copies
→ property name embedded in text
→ reader comments / attention
→ reporter contact with one poster
→ reporter identity check
→ newspaper article
→ Sina republication / current live survivor
→ modern search result
→ research claim
```

这些对象绝不能合并。

特别要保留：

```text
poster
!=
author
!=
person described in post
!=
commercial beneficiary
```

以及：

```text
same text on many forums
!=
many independent ordinary-life cases
```

---

## 2. Current surviving evidence

当前可检索、可阅读的新浪页面：

- headline: `网友发帖寻女友拼房结婚被疑炒作`
- current URL: https://news.sina.com.cn/s/2009-02-24/020917273220.shtml
- displayed datetime: 2009-02-24 02:09
- source line: 扬子晚报

当前页面保存的报道内容包括：

1. 一个“80后男”寻找女性共同首付、共同月供、同时解决买房和结婚问题的帖子；
2. 对女性年龄、学历、存款等条件的要求；
3. 一个具体楼盘名称；
4. 报道称该帖在成都多个本地论坛传播并形成热门讨论；
5. 记者通过帖子留下的邮箱联系到一个自称相关发帖人的人；
6. 对方告诉记者，这个主意并非自己原创，只是转帖；
7. 对方自己又表示怀疑这是某房地产公司的炒作；
8. 对方随后声称自己是成都某网络媒体记者并提供姓名；
9. 报道称记者在该网站工作人员中未查到此人；
10. 记者此后无法进一步核验其身份 / 背景。

证据等级：

- 扬子晚报同期记者调查，经新浪当前存活页保存：**B / T1**；
- 页面当前显示的 2009 日期、来源行、正文：可观察；
- 2009 新浪历史 DOM / template / charset：**未验证**；
- 原论坛贴：**未验证**；
- 房地产公司实际参与：**未证实**。

---

## 3. What the post appeared to prove — and why that proof fails

如果只读帖子叙事，它看起来是异常理想的 life-history evidence：

```text
25-year-old man
+ bachelor degree
+ two years in Chengdu
+ wants to settle
+ no existing partner
+ exact desired partner profile
+ exact savings threshold
+ exact shared down payment
+ exact monthly mortgage
+ exact housing development
+ explicit marriage plan
```

这样的材料很容易诱使研究者写：

> “2009 年有年轻男性开始通过网络寻找陌生女性，以 AA 首付方式解决买房和婚姻。”

但同期记者调查至少破坏了其中最重要的一个 link：

```text
first-person narrator
=
verified real person executing this plan
```

因为被联系到的人自己说他是转帖者，并非原创者。

所以允许的最小 claim 应改成：

> 2009 年成都多个本地论坛中传播过一则以第一人称“AA 拼房结婚”计划包装的帖子；同期扬子晚报记者联系到的一名相关发帖者称自己只是转帖，并且该报道公开质疑其与房地产营销的关系。

这句话比“有人真的这样结婚”窄很多，但证据更强。

---

## 4. Authenticity state model

普通个人材料建议以后增加以下状态：

```text
text exists
!=
text was written by account holder
!=
account holder is a real unique person
!=
account holder is the described protagonist
!=
protagonist actually intended the described action
!=
action was attempted
!=
action happened
```

进一步加入：

```text
organic post
commercially seeded post
journalist-created scenario
role-play / joke
copypasta
fiction / creative writing
real event retold by third party
```

在没有证据时都属于候选解释，而不是研究者可以自行决定的标签。

---

## 5. `first-person` 应该至少拆成三层

### 5.1 grammatical first person

文本写“我”。

只能证明：

> 页面上的文字采用第一人称语法。

### 5.2 attributed first person

可以确认某账号 / 笔名发布该文本。

只能证明：

> 该账号当时发布 / 转发过这段第一人称文本。

仍不能自动证明它在描述账号主自己的真实生活。

### 5.3 authenticated autobiographical first person

至少需要一部分独立证据把：

- 账号；
- 人；
- 事件；
- 时间；
- 后续行动

连接起来。

对普通人的隐私研究，不需要也不应该无限追实名。

所以更现实的仓库字段可以是：

```yaml
authenticity_status:
  grammatical_first_person: yes
  account_attribution: verified | probable | unknown
  authorship: verified | attributed | unknown | repost
  autobiographical_relation: verified | probable | unknown | contradicted
  commercial_interest: observed | suspected_by_source | unknown | none-observed
  event_execution: verified | reported | unknown
```

---

## 6. Repost multiplicity is a separate problem from syndication multiplicity

仓库已有新闻转载 source-lineage 规则：

```text
same newspaper article on Sina + Sohu + Phoenix
!=
three independent evidence families
```

论坛还需要多加一层：

```text
same life-story text on Forum A + Forum B + Forum C
!=
three independent people
!=
three independent experiences
```

甚至：

```text
same username on several sites
!=
verified same human
```

2009 案例中，记者联系到的人已经明确说自己“只是转帖”。

因此 cross-posting 的传播宽度反而可能**降低**我们对“帖子就是发帖者真实人生”的信心。

---

## 7. Commercial-interest layer

同期报道不能证明房地产公司真的策划了帖子。

但它足以说明三个必须保留的事实：

1. 帖子反复出现具体楼盘名称；
2. 传播获得显著点击和争论；
3. 记者和部分网友当时已经公开怀疑其商业营销属性。

因此 evidence record 应写：

```yaml
commercial_interest:
  property_name_embedded: true
  commercial_beneficiary_identifiable: true
  source_reports_contemporaneous_suspicion: true
  sponsor_verified: false
  astroturfing_proven: false
```

不要从 `suspicion` 偷换成 `proven campaign`。

---

## 8. Independent contextual family: real-estate Internet marketing did exist

为了判断“商业动机”是不是一个完全不合时宜的后见之明，本轮还检查了同期房地产网络营销材料。

2008 年一篇房地产网络营销模式文章明确把 Internet 描述成开发商与目标消费者进行双向互动的信息 / 广告 / 销售平台：

https://www.chinaacc.com/new/287/295/358/2008/8/wa664154395188002145-0.htm

2008 年《法制晚报》报道楼市转冷后，多家项目加大网络与短信广告投放预算：

https://news.sohu.com/20080311/n255646651.shtml

2009 年房地产网络广告市场本身也已达到明显规模；同期行业资料显示新浪乐居、搜房、搜狐焦点等是重要线上广告渠道。

例如：

https://blog.sina.com.cn/s/blog_5d14cc3b0100f9ir.html

这些是**独立的行业语境证据**。

它们只证明：

> 当时房地产业使用 Internet 营销完全属于现实商业环境。

它们仍然**不能证明**具体“AA 拼房结婚”帖由某开发商制作。

---

## 9. Historical visibility bias: dramatic pseudo-life can survive better than ordinary life

这个案例还提示一种 archive / search 偏差：

### ordinary life

一个真实年轻人可能只是：

- 和伴侣讨论首付；
- 向父母借钱；
- 看几个楼盘；
- 最终没买。

这类生活可能没有公开页面。

### viral pseudo-life

一个带有：

- 陌生人征婚；
- AA 首付；
- 具体楼盘；
- “80后”；
- 强争议标题

的帖子更容易：

- 被多论坛转载；
- 上热门；
- 被记者写成新闻；
- 被门户继续转载；
- 二十年后仍能被搜索。

于是产生：

**`narrative virality / ordinary-life representativeness gap`**。

搜索存活概率可能和故事戏剧性、营销价值、争议性正相关，而不是和现实中这种生活路线的普遍程度正相关。

所以：

```text
high archival visibility
!=
high historical prevalence
```

---

## 10. Platform-observable fact / contemporaneous self-report / media reconstruction

这个案例按用户要求可以这样分类：

### Platform-observable fact

目前没有已打开的 2009 原论坛 capture，因此**不能**直接观察：

- 原论坛 host；
- thread ID；
- 发帖账号页面；
- 回复结构；
- 楼层；
- 浏览量的历史页面字段；
- 删除 / 编辑状态；
- charset / DOM / CSS / JS。

### Contemporaneous self-report

新闻报道保存了一个自称相关发帖人的同期说法：

> 自己只是转帖，而不是原创。

这是 **T1 attributed statement**，不是原论坛 T0 artifact。

### Cross-confirmation

记者对其自称的网络媒体记者身份进行了当时查证，并报道称未在工作人员中找到该人。

这不证明其所有身份信息均为虚假；它只使 self-identification 的可信度下降。

### Media reconstruction

扬子晚报把多个论坛传播、帖子内容、记者联系、网友质疑重组成了一篇新闻。

我们今天看到的是这一媒体 reconstruction 的新浪 survivor。

因此：

```text
current Sina article
!=
original forum thread
```

---

## 11. Current survivor / historical capture boundary

当前可观察：

```yaml
current_surviving_host: news.sina.com.cn
current_url: https://news.sina.com.cn/s/2009-02-24/020917273220.shtml
headline_current: 网友发帖寻女友拼房结婚被疑炒作
source_line_current: 扬子晚报
page_displayed_publication_datetime: 2009-02-24 02:09
displayed_body: substantial article text survives
```

本轮没有取得：

```yaml
verified_historical_capture_opened: false
original_forum_url: unknown
original_forum_host: unknown
first_post_datetime: unknown
historical_sina_capture_datetime: unknown
historical_content_type: unknown
historical_charset: unknown
historical_dom: unknown
historical_scripts: unknown
```

本轮尝试：

- 按精确新浪 URL 搜索公开 Wayback locator；
- 按标题与 URL 组合搜索；
- 检查公开搜索结果中是否能直接取得 original forum permalink。

结果：没有拿到可实际打开、满足 `docs/METHOD.md` 最低合同的历史 capture。

因此：

**M1 verified historical forum / Sina capture: NOT ACHIEVED IN THIS SLICE.**

这不等于：

> Internet Archive 没有保存。

更不等于：

> 原论坛页面从未存在。

---

## 12. Claim ledger

| claim | evidence | grade | confidence | allowed wording |
|---|---|---|---|---|
| 2009 年有“AA 拼房结婚”文本在成都论坛传播 | 扬子晚报同期报道 / 新浪 survivor | B/T1 | high for reported propagation | `同期报道记录该文本在多个成都论坛传播` |
| 文本使用第一人称、提供具体首付 / 月供 / 楼盘 | 同上 | B/T1 | high for text as reported | `报道保存了这些文本内容` |
| 联系到的人是帖子原创作者 | 对方自己否认 | B/T1 | contradicted | 不得写 |
| 联系到的人只是转帖者 | 同期记者引述 | B/T1 | medium-high | `报道引述其称自己只是转帖` |
| 某房地产公司策划帖子 | 只有怀疑，无直接证据 | B + inference | low / unverified | `当时记者 / 网友公开怀疑`，不得写成事实 |
| 真实青年通过 AA 拼房与陌生人结婚 | 无执行证据 | none | unknown | 不得写 |
| 房地产行业当时使用 Internet 营销 | 同期行业 / 媒体材料 | B | high | 可写行业语境 |
| 原论坛页面可以复原 | 无 capture | none | unknown | 不得写 |

---

## 13. Minimum protocol for future first-person old-Web material

在把一个旧论坛 / 博客帖子送进 `how-people-lived` 当“这个人当时怎么想未来”的证据以前，至少问：

1. **页面存在吗？**
   - historical capture / live legacy / only media quotation?
2. **谁发布？**
   - account known / unknown / repost?
3. **谁写？**
   - account holder / copied text / unknown?
4. **是不是自己的生活？**
   - autobiographical / role-play / advice / fiction / ad copy / unknown?
5. **当时有没有商业或组织利益？**
   - embedded product / property / employer / campaign?
6. **行动发生了吗？**
   - plan / attempt / completed event / unknown?
7. **多平台是不是同一源？**
   - independent people or repost chain?
8. **为什么今天还能搜到？**
   - ordinary archival survival / media pickup / controversy / marketing virality?

建议给 ordinary-life source ledger 增加：

```yaml
voice_authenticity:
  grammatical_person:
  account_attribution:
  authorship_relation:
  autobiographical_relation:
  repost_status:
  commercial_interest:
  execution_status:
  independent_identity_confirmation:
```

---

## 14. Hindsight risks

### Risk A — “记者怀疑”写成“后来证实”

禁止。

本轮没有证明幕后主体。

### Risk B — 把文本真实性问题变成对普通用户的无限实名追踪

也禁止。

研究需要的是 evidence status，不是重新暴露普通人的身份证明。

### Risk C — 因为一个帖子可疑，就贬低整个论坛资料

同样错误。

论坛仍然可以提供极高价值的 T0 evidence；只是每条材料需要做最小 provenance / authenticity 检查。

### Risk D — 把传播量当现实比例

病毒传播反而意味着 sampling bias 更强。

### Risk E — 现代“水军 / astroturf”概念直接套回 2009

可以使用分析术语，但必须保留当时证据：本案当时自己的报道只说“被疑炒作”，没有完成 sponsor attribution。

---

## 15. What this changes in `old-web-archaeology`

此前仓库已经很好地区分：

```text
platform
site
page
account
capture
claim
```

这个案例说明 ordinary-life archaeology 还需要在 `account` 与 `claim` 之间再插入：

```text
text authorship
narrator identity
repost relation
autobiographical relation
execution relation
commercial-interest relation
```

否则一个保存得非常好的页面仍然可能产生一个非常坏的 life-history inference。

最重要的一句方法结论是：

> **“找到当年的原帖”解决的是 contemporaneity 和 page provenance；它并不会自动解决作者是谁、叙述是否自传、行动是否真的发生。**

这意味着 M1 artifact work 与 life-history authenticity work 是互补的，不是谁替代谁。

---

## 16. Next useful work

优先级：

1. 找到至少一个 2009 原始成都论坛 permalink / archive locator；
2. 若找到，实际打开并记录 original URL、capture datetime、host、thread/account relation；
3. 检查是否能找到两个历史时点（初帖 / 后续编辑或讨论）；
4. 检查 property name 是否出现在原文、签名、广告位还是媒体重述；
5. 寻找当时独立论坛用户是否指出 repost 源头；
6. 不重新聚合普通用户邮箱、真实姓名或其他非必要个人信息；
7. 若原帖永远不可得，把“媒体调查保存了真实性争议”作为最终边界，而不是补写一个 imagined original page。

在这些条件满足以前，本 note 保持 **artifact probe / method evidence** 状态，不升级为完整 M1 case。