# 1999–2009：网上查号、搜索与问答——query state、ranking state 与 answer-production gaps

> Scope：本文件只处理约 1999–2009 中文旧网中“网上查号 / 搜索框 / 搜索结果 / 知识问答页面”作为 Web artifact 时的证据合同。
>
> 更长的普通生活史、1989 年电话信息服务、1994 前后中国联网阶段、2021 动态防疫政策查询、2025 生成式 AI 与 Usenet/Minitel 海外对照写在：
> <https://github.com/tmzncty/how-people-lived/blob/main/topics/procedural-knowledge-option-discoverability-and-everyday-search-china-1989-2025.zh-CN.md>
>
> 本文件不写“中国搜索引擎通史”，也不假定今天向一个仍存活的搜索框提交查询，就能复现 2003、2005 或 2008 年真实用户看到的结果。目标是回答：**旧网档案留下一个搜索/问答页面时，它究竟保存了信息发现过程的哪一层，又系统性看不见哪些状态？**

---

## 1. 为什么这是一个新的旧网研究单位

仓库已经处理过：

- job board 中的职位、简历、投递与 attention gap；
- 婚恋/住房的 search filters 与现实 outcome gap；
- 学历查询的 authoritative database read surface；
- 网银的 transaction execution gap；
- 同学录的 mutable profile / roster state；
- BBS 兼职与现实执行；
- pager gateway 的跨网投递。

搜索/问答与它们不同。

这里最容易被错误保存的是：

> **interface survived, information state did not.**

一个 2005 年的搜索首页 HTML 可以完好存在，却不意味着：

- 2005 年的索引还在；
- 某个 query 当时返回什么还在；
- 当时结果的排序还在；
- 广告/推广位状态还在；
- 用户点了哪个结果还在；
- 结果页指向的目的页面还在；
- 用户最后是否据此采取行动还在。

对问答页面又相反：

- 某个公开 question/answer 可能长期存活；
- 但大量只在搜索框里输入、从未公开成页面的问题没有 URL；
- 站内搜索、推荐、投票、采纳、编辑与 moderation state 仍可能消失。

因此本文件新增两个核心 archive units：

> **query state** 与 **ranking/answer state**。

---

# 2. 两条基础执行链

## 2.1 搜索 / 查号链

最小链条应拆成：

```text
public search page
→ input controls / query syntax
→ submitted query
→ server-side parser
→ index/database snapshot at that time
→ filtering / ranking / paid-placement policy
→ result set
→ rendered result page
→ user reads / skips / clicks
→ destination resource
→ downstream action
```

不能把任何相邻两层默认合并。

尤其：

```text
search form exists
≠ query was submitted
≠ historical index survives
≠ historical result survives
≠ result was read
≠ result was trusted
≠ result caused action
```

## 2.2 问答链

Q&A 至少拆成：

```text
user need
→ account/session
→ question submission
→ question page created
→ category/tags
→ visibility/search exposure
→ answers arrive
→ votes/comments/points
→ accepted/best-answer state
→ later edits/moderation/deletion
→ later searchers discover page
→ later reader acts or ignores
```

因此：

```text
question answered
≠ answer correct
≠ accepted answer objectively correct
≠ later reader saw it
≠ later reader followed it
```

---

# 3. C1 — 1999 年网上 114 是“旧数据库的新 Web read surface”

来源：1999-09-15《北京晨报》同期报道（新浪存续页）：
<https://news.sina.com.cn/society/1999-9-15/14567.html>

报道描述“网上 114”试运行，并明确说服务建立在 114 原有数据库基础上。

可观察的 query affordances 包括：

- 已知单位名称查询；
- 单位名拼音首字母查询；
- 按行业类别查询；
- 电话号码反查单位；
- 旧号/旧名查新号/新名；
- 国内国际区号；
- 常用电话。

报道还说：

- 约有 230 多万个号码资源；
- 企事业单位号码“随时更新”；
- 为保护隐私，私宅电话基本不进入网上查询。

## evidence

**B — 同时代新闻，能证明当时报导的公开功能和数据库关系。**

## confidence

**high for feature/existence claim**；
**unknown for exact historical backend implementation**。

## 新 evidence rule：front-end capture does not freeze the database

即使找到：

```text
1999-09-20 capture of www.114china.com
```

也最多证明当时 archive 抓到了某个 interface representation。

它不自动保存：

```text
114 database @ 1999-09-20
```

因此固定：

> **historical HTML datetime ≠ historical backend-state datetime**

若今天一个旧 URL 仍能提交查询，它可能：

- 连接今天数据库；
- 连接替换后的数据库；
- 已失效；
- 被 archive replay 拦截；
- POST 根本没有被保存。

不得将今天的 response 当历史 result。

---

# 4. C2 — 分类本身就是一种信息模型，不是中性的自然目录

1999 网上 114 已支持“所属行业类别”查询。

这意味着用户发现一个陌生服务时，可能依赖：

```text
user's mental category
↔ platform's category ontology
```

如果用户想到的词与目录使用的类别不同，他可能找不到本来存在的对象。

这种问题在海外同期 Minitel 目录也很明显，但本仓不扩写全球材料；全球比较留在 how-people-lived。

在中文旧网 case 中应新增字段：

```yaml
query_mode:
  - exact_name
  - prefix_or_initials
  - category
  - free_text
  - reverse_lookup
category_ontology_observed: true|false|unknown
category_version_known: true|false
```

不能把 category label 当成现实行业的天然边界。

---

# 5. C3 — 2004 年 114 争议说明：发现接口会路由注意力

来源：2004-02-21 新华网调查（新浪存续页）：
<https://news.sina.com.cn/c/2004-02-21/09511861933s.shtml>

以及 2004-07-02《北京晚报》关于相关诉讼的同期报道：
<https://news.sohu.com/2004/07/02/93/news220829357.shtml>

报道记录的争议对象是“开锁”类模糊查询。

部分开锁企业声称，不能说出企业全称的用户查询会被导向某个合作热线；报道还记录了合作合同、服务费/查询费等情况。

法院后来驳回了原告关于市场垄断等主张，因此本仓不能写：

> `114 legally found to monopolize locksmith discovery`

可以写的窄 claim 是：

> **2003–2004 年北京 114 的模糊查询 routing 成为公开商业与法律争议对象。**

## 为什么它属于 old-web archaeology

网上 114 与电话 114 共享/继承一种信息发现逻辑：

```text
vague user need
→ intermediary classifies need
→ intermediary selects/returns endpoint
```

因此搜索史不能从算法排名才开始研究“visibility allocation”。

### 固定边界

```text
listed in database
≠ returned for vague query
≠ equally visible
≠ neutral recommendation
```

如果历史 Web 页面显示“按行业查询”，研究者需要问：

- 返回完整列表还是部分列表？
- 顺序是什么？
- 是否有推荐/合作/推广状态？
- 是否按地理、字母、点击、付费或人工规则排序？

如果没有证据，必须写 unknown。

---

# 6. C4 — 2005 百度知道：搜索系统开始把“问题”本身变成可持久页面

来源：2005-07-07《新京报》同期报道（新浪存续页）：
<https://tech.sina.com.cn/i/2005-07-07/1005656566.shtml>

报道明确说测试版已经上线，并把其模式描述为：

- 用户提交问题；
- 其他用户回答；
- 通过悬赏/激励机制促成答案；
- 与只查询 Internet 上既有内容的搜索不同，平台会让用户创造答案。

## evidence

**B — 同时代媒体报道。**

## 新 artifact unit：answer-production object

普通网页搜索的 query 常常是短命状态：

```text
?q=怎么去除鱼腥味
```

用户关闭浏览器后，query 本身未必留下公共文档。

Q&A 则可能把它转为：

```text
/question/<persistent-id>
```

并留下：

- title；
- question body；
- author/account；
- timestamp；
- answers；
- accepted answer；
- points；
- category；
- comments。

这使旧网 archive 对“普通人当时问什么”获得一种新的可见性。

但同时产生明显 selection bias：

> **publicly externalized question ≠ all questions users had**

大量问题可能只被：

- 输入搜索框；
- 问 QQ 好友；
- 问同事；
- 打电话；
- 自己放弃。

它们不会成为公开 URL。

---

# 7. C5 — 2007 年“知识搜索”展示问答平台的口语化查询与生活问题定位

来源：中国互联网协会 2007-07-13 同期行业报道：
<https://www.isc.org.cn/article/12411.html>

文章用以下例子解释“知识搜索”：

- 字词用法；
- 诗句出处；
- 烹饪去腥；
- 电影某一时刻的音乐；
- 日常生活、学习、专业疑问。

文章还列出多个当时的服务：

- 百度知道；
- 新浪爱问知识人；
- 腾讯问问；
- 雅虎知识堂；
- 经验搜索；
- 医疗问答等。

## evidence

**B — 同期行业媒体/协会转载。**

文中关于访问量、最大平台等数字多来自平台/行业声称，不能不加限定地当独立流量审计。

## 新的技术/页面边界：natural-language question ≠ search keyword

一个页面只有一个“搜索框”，并不能证明其语义模型。

应分别记录：

```yaml
input_expectation:
  exact_identifier: false
  keyword_query: true
  natural_language_question: true|false
  category_browse: true|false
```

问答平台还需要区分：

```text
question search
vs
question creation
```

用户输入一句话后，系统可能：

- 直接搜索相似旧问题；
- 引导新建问题；
- 两者混合。

历史页面只保存 input box 时，不能推断实际 server-side branch。

---

# 8. C6 — 2008 年同期用户材料证明“search used”，但不能复原这些人的 query log

来源：中国青年报 2008-07-15 文章的存续转载：
<https://www.guandian.cn/article/20080715/74573.html>

文章中的同期材料涉及：

- 早餐；
- 公交路线；
- 作业/文案；
- 娱乐；
- 化妆品；
- 小身体问题；
- 电影细节；
- 猫的品种；
- 网络流行语。

其中一名 1985 年出生的受访者明确描述自己遇到陌生网络符号后立刻打开百度。

## evidence

**B + contemporaneous first-person fragment**。

## 可证明

> 至少部分 2008 年年轻网民已经把搜索用于大量普通生活小问题。

## 不能证明

- 文章列出的每一个 query 都来自已保存 server log；
- 这些用户每次具体输入什么关键词；
- 当时第一页有哪些结果；
- 哪个结果被点击；
- 哪个结果导致了后续行为；
- “80 后”整体都如此。

### 新 gap：behavior described, event artifact absent

这是一类很典型的旧网证据错位：

```text
contemporaneous first-person use description survives
but actual search events do not
```

研究者必须把它标成“used evidence”，不能伪造成“query capture”。

---

# 9. query-state gap

搜索最基础、也最系统性的缺失是：

> **大多数查询从来不是公共 Web 页面。**

典型 query state 可能包含：

```yaml
query_text: ?
timestamp: ?
user_or_session: private/unknown
location_or_ip: private/unknown
input_method: typed|history|suggestion|voice|unknown
filters: ?
result_page_number: ?
```

公开 archive 通常不应、也不会系统保存私人 query logs。

所以：

> **absence of archived queries is often the correct privacy outcome, not a research defect to be “repaired” by deanonymization.**

## privacy stop condition

本仓不：

- 搜集泄露的个人搜索日志；
- 重新公开普通人的敏感健康/性/财务查询；
- 根据第三方缓存批量还原个人 query history；
- 用账号名跨站拼接私人检索行为。

---

# 10. index-snapshot gap

一个搜索引擎在 t1 的结果取决于当时 index。

```text
index(t1) ≠ index(t2)
```

网页可以：

- 新增；
- 删除；
- 改内容；
- 改 URL；
- 被 robots 屏蔽；
- 被重新抓取；
- 失效；
- 被平台收录或排除。

因此，即使 query 完全相同：

```text
Q("租房 北京") @ 2003
```

和：

```text
Q("租房 北京") @ 2026
```

也不是同一个研究事件。

### 固定规则

> **same query string ≠ same historical search**

### archive implication

为了真正复现旧搜索结果，理论上至少需要：

- historical index snapshot；
- historical ranking code/config；
- historical ad/promoted-content state；
- historical query normalization；
- historical destination corpus；
- relevant personalization/context。

普通 Web archive 通常没有这些。

所以本仓多数情况下只能做：

> **interface archaeology + surviving result-page evidence**

而不是完整搜索引擎重演。

---

# 11. ranking-state gap

即使知道当时 index 中有哪些 URL，也不能自动恢复顺序。

排序可能依赖：

- 文本相关性；
- link signals；
- freshness；
- category；
- geographic signals；
- commercial/promoted placement；
- product self-preference；
- moderation/policy；
- anti-spam state。

因此固定：

```text
indexed
≠ returned
≠ first page
≠ top result
≠ clicked
```

## 为什么这对普通生活很重要

用户通常不会遍历整个 corpus。

所以真正进入生活选择的不是：

> “网上存在多少信息”

而更接近：

> “在那个人那次查询里，前几屏出现了什么”。

这也是为什么 114 模糊查询的商业 routing 与搜索排名争议可以放在同一个“attention allocation”框架内比较。

---

# 12. paid-placement / intermediary-interest gap

历史页面可能没有把付费排序、合作热线、推广位的后台合同状态完整公开。

因此对于任何 directory/search artifact，应增加：

```yaml
commercial_placement_observed: true|false|unknown
placement_label_observed: true|false|unknown
ranking_rule_known: true|false
intermediary_financial_interest_known: true|false
```

### 禁止

如果一个结果排第一，但没有证据：

- 不得断言是“算法认为最好”；
- 不得断言是“广告”；
- 不得断言是“最受欢迎”；
- 不得断言是“唯一可用”。

只记录 observable state。

---

# 13. result-page survival gap

搜索首页往往比 query result 更容易被 archive 抓到。

原因可能包括：

- result URL 带 query string；
- POST submission；
- robots；
- session；
- infinite/dynamic response；
- crawler 不会主动输入关键词；
- 参数空间无限。

因此：

> **many captured homepages + few captured result pages**

不能解释成：

> “历史用户很少搜索”。

它更可能是 crawler behavior 的产物。

### evidence record

如果找到 result capture，至少记录：

```yaml
original_url:
capture_url:
capture_datetime:
query_visible_in_url: true|false
query_visible_in_page: true|false
result_count_claimed:
visible_result_count:
next_page_links:
promoted_labels:
archive_rewrite_observed:
subresources_missing:
```

---

# 14. click/action gap

搜索结果保存下来，仍然看不见：

```text
which result user chose
→ whether destination loaded
→ whether user believed it
→ whether user called / traveled / bought / applied / changed plan
```

因此固定：

> **result visibility ≠ behavioral outcome**

这与仓库既有的：

- job application outcome gap；
- household outcome gap；
- relationship outcome gap；
- transaction execution gap

是同一类“Web 把人送到下一层以后，后续行为离开公共 archive”的问题。

---

# 15. destination-rot gap

一个旧 Q&A 或搜索结果页可能长期存活，但它链接的原始资料已经死亡。

于是历史上可能出现：

```text
answer summary survives
+ cited source dies
```

研究者今天只看到二手结论，看不到当时回答者依据什么。

### 固定规则

> **surviving answer ≠ surviving provenance**

如果问答页面给出来源链接，应分别记录：

- original destination URL；
- 是否有 contemporaneous capture；
- 今天是否 redirect/domain-reuse；
- answer 是否只是复制；
- 是否还能验证 source family。

---

# 16. answer-state mutation gap

Q&A 页面不是一次写完的静态文档。

状态可能经历：

```text
question posted
→ first answer
→ more answers
→ voting
→ accepted/best answer
→ comment/dispute
→ edit
→ moderation
→ answer deletion
→ question closure
```

某个 2008 capture 和某个 2012 capture 可能显示不同“最佳答案”。

因此：

> **one capture of a Q&A URL ≠ complete answer history**

### evidence fields

```yaml
question_posted_at:
capture_datetime:
answer_count_visible:
accepted_answer_observed:
accepted_state_timestamp_known: false
edit_markers:
deleted_answer_markers:
moderation_markers:
points_or_votes_visible:
```

如果接受答案状态的发生时间未知，不能写成“从提问当天起就是最佳答案”。

---

# 17. accepted-answer correctness gap

Q&A 特别容易产生一个错误推断：

```text
platform says "最佳答案"
→ historian writes "correct answer"
```

这是不允许的。

“最佳/采纳”最多是一个 **platform state**。

它可能说明：

- 提问者选择；
- 规则自动选择；
- 投票；
- 运营机制；
- 积分逻辑。

除非另外核验，不能说明：

- 医疗上正确；
- 法律上正确；
- 当时政策上正确；
- 今天仍正确。

因此：

> **accepted answer ≠ verified truth**

---

# 18. historical-answer expiry

程序性答案有强烈时间属性。

例如：

- 电话号码；
- 报名流程；
- 软件版本；
- 浏览器菜单；
- 火车/公交路线；
- 证件要求；
- 资费；
- 店铺地址。

2006 年正确答案可能在 2009 年已经错误。

问答 archive 必须至少分：

```text
answer was posted at t1
vs
claim was valid at t1
vs
claim remains valid at capture t2
vs
claim remains valid today
```

四者不能混为一谈。

---

# 19. mirror / scrape provenance collapse

问答内容非常容易被：

- 自动采集站；
- SEO 镜像；
- 论坛转载；
- 博客复制；
- 搜索 snippet

重复保存。

所以：

> **ten URLs with same answer ≠ ten witnesses**

应先做 evidence-family dedup。

### 最低检查

- 文本是否逐字相同；
- 原作者/提问者是否相同；
- 时间戳是否继承；
- 是否保留 canonical link；
- 是否只是搜索缓存；
- 是否有独立评论/验证。

---

# 20. 2008 用户第一人称为何不能替代 query capture

同期采访和博客摘录非常有价值，因为它们证明 **used**。

但旧网仓仍要保留研究单位：

```text
contemporaneous statement about search behavior
≠ archived search request
```

例如有人说：

> 遇到不懂的网络词立刻打开百度。

可以证明一个行为模式。

不能因此生成一个虚构的：

```text
2008-07-xx 22:13:41 query="俯卧撑什么意思"
```

并写成历史记录。

这种 reconstruction 即使“很合理”，仍属于 D，而且没有必要。

---

# 21. 搜索/问答的 A/B/C/D 证据等级具体化

## A — 原始/同时代 artifact

优先：

- 1999–2009 历史搜索首页 capture；
- 历史 query result capture；
- 历史 Q&A question/answer capture；
- 当时官方帮助页、query syntax、FAQ；
- 当时浏览器/软件手册；
- 原始 HTML/JS/CSS；
- 当时公开的接口/产品说明。

### 注意

一个历史 result capture 只能证明：

> archive 在该时间抓到这个 representation

不能自动证明所有用户都看到相同结果。

## B — 同期报道/教程/用户说明

例如：

- 1999 北京晨报网上 114；
- 2005 新京报百度知道；
- 2007 知识搜索行业报道；
- 2008 用户搜索习惯采访。

它们能补功能与使用场景，但不是 server log。

## C — 后来回忆

例如：

- “我 2003 年每天都用某搜索”；
- “当年首页就是这样的”；
- “某平台以前结果更好”。

适合体验史，不独立确定算法、版本和具体结果。

## D — 研究者重建

包括：

- 根据截图手工重建搜索首页；
- 用现代 index 模拟历史结果；
- 根据旧文章猜测 query；
- 用今天算法生成“可能的 2005 搜索结果”。

必须标 reconstruction，且不得冒充 historical result。

---

# 22. 浏览器、编码与页面形态也会改变“能不能搜”

1999–2009 中文搜索页面还必须记录：

- GB2312 / GBK / UTF-8；
- GET / POST；
- form encoding；
- JS 是否必需；
- frameset；
- cookies/session；
- IE 特定脚本；
- autocomplete/suggestion 是否服务端；
- archive rewrite 是否破坏 query URL。

### 特别注意中文 query encoding

如果 archive 中 URL 出现：

- percent-encoded bytes；
- mojibake；
- 被 rewrite 的参数；

不要在不知道历史 charset 的情况下直接“修正”为现代 UTF-8，再声称原 query 如此。

应同时保留：

```yaml
raw_query_bytes_if_known:
decoded_query_candidate:
charset_assumption:
confidence:
```

---

# 23. 搜索首页的“极简”不等于系统简单

一个只剩：

```text
logo + input + submit
```

的旧首页，可能背后依赖：

- crawler/indexer；
- distributed storage；
- ranking；
- anti-spam；
- commercial placement；
- query logs；
- caching；
- content policy。

所以：

> **simple page surface ≠ simple historical system**

反过来，一个复杂门户首页也不证明搜索 backend 更复杂。

页面考古和系统考古必须分开。

---

# 24. 与 2019 平台围墙争议的关系：只作为 out-of-scope downstream boundary

2019 年移动平台自我导流、App 内容不能被第三方搜索完整抓取等问题，是这条谱系的后续结果，但已经超出本文件 1999–2009 主 scope。

因此这里只登记边界：

```text
open-ish Web corpus search
→ platform-owned knowledge pages
→ increasingly closed app ecosystems
```

具体 2019 证据与生活史解释放在 how-people-lived，不向本仓主研究对象无限后移。

---

# 25. 与 1989 电话查号/信息台的关系：只作为前史边界

1989 济南“114 微机查号台”和电话信息服务说明：

- 数据库/微机化可以先发生在 Web 前；
- 普通人仍通过电话和人类服务层取信息。

这个前史对理解 1999 网上 114 为什么是“read-surface migration”直接必要，因此可以保留一段 boundary note。

但本仓不扩成中国电话信息服务史。

前史完整解释见 how-people-lived。

---

# 26. archive gap taxonomy

本文件新增以下 gap labels。

## Q1 — query-state gap

用户实际输入的 query 和 session 不公开/不存档。

## Q2 — index-snapshot gap

当时可搜索 corpus 的完整状态不存在。

## Q3 — ranking-state gap

即使 corpus 可部分恢复，当时排序/推广/过滤逻辑不可恢复。

## Q4 — result-page survival gap

首页 capture 多，但具体参数结果页少。

## Q5 — click/action gap

结果页存在，不知道用户点什么、做什么。

## Q6 — destination-rot gap

结果/回答活着，目标来源已死。

## Q7 — answer-state mutation gap

答案、采纳、投票和 moderation 状态随时间变化。

## Q8 — answer-correctness gap

平台采纳状态不是事实核验。

## Q9 — query-to-public-question selection gap

只有一部分需求会从私人 query 变成公开问答 URL。

## Q10 — interface/backend time split

历史 HTML 与实际 backend state 的时间可能不一致。

## Q11 — commercial-routing opacity

合作/付费/推广关系可能不在页面 surface 上。

## Q12 — mirror provenance collapse

多个副本可能来自同一原始问答，不能计为独立证据。

---

# 27. 对 capture 的最小检查表

遇到旧搜索/问答 capture 时至少记录：

```yaml
artifact_type: search_home|search_result|directory|question|answer|help|tutorial
platform:
host:
original_url:
capture_url:
capture_datetime:
page_reported_datetime:
charset:
content_type:
query_method: GET|POST|unknown
query_visible:
query_text_if_public:
category_state:
result_count_visible:
visible_result_count:
ranking_labels:
ad_or_promotion_labels:
account_required:
session_required:
answer_count:
accepted_answer_visible:
edit_or_moderation_markers:
external_destination_links:
missing_subresources:
archive_rewrite_risk:
backend_state_historical: proven|unknown|no
privacy_risk:
evidence_grade:
confidence:
```

---

# 28. Claim 写法示例

## 好

> `1999-09-15 的同期报道说，北京网上 114 试运行，支持单位名、拼音首字母和行业类别等查询，并基于原有 114 数据库。`

## 差

> `1999 年北京人都开始网上查电话。`

---

## 好

> `2005-07-07 的同期报道将百度知道描述为用户提出问题、其他用户创造答案的互动问答平台。`

## 差

> `2005 年以后中国人遇到问题都改问百度知道。`

---

## 好

> `2008 年的同期媒体采访保存了若干年轻网民将搜索用于日常小问题的第一人称描述。`

## 差

> `这证明 80 后已经不再向人提问。`

---

## 好

> `某 archive capture 保存了 query X 的一页结果，capture datetime 为 T。`

## 差

> `搜索引擎在整个 2006 年都把这个 URL 排第一。`

---

# 29. 反例与 stop conditions

## 反例 1：当前站点仍能搜

不能因此使用今天结果回填旧结果。

## 反例 2：Wayback 保存了首页

不能因此宣称“搜索功能复原完成”。

## 反例 3：找到一个 question URL

不能因此推断其作者后来执行了答案。

## 反例 4：找到“最佳答案”

不能因此用作权威事实来源，除非另行核验。

## 反例 5：几十个镜像都复制同一答案

只计一个 evidence family。

## Stop

以下情况应停止增加确定性：

- 只有今天的查询结果，没有历史 result capture；
- 只有后来 SEO 文章描述算法；
- query 涉及不应重新公开的私人敏感信息；
- 历史域名已复用；
- 乱码/charset 使 query 无法可靠还原；
- 无法判断结果是 archive replay、live backend 还是 modern redirect；
- 只有一张截图但没有 URL/datetime/provenance。

---

# 30. 本轮改变了旧网考古的哪一点

此前 old-web archaeology 很容易把“保存页面”理解成保存信息。

搜索系统迫使我们承认：

> **很多最重要的旧网生活状态从来不属于静态页面。**

搜索真正发生在：

```text
query
× historical index
× ranking policy
× time
× user context
```

而 Web archive 通常只能保存这个乘积偶然产生的少量表面结果。

问答平台则形成相反的保存偏差：

> 私人查询不留下公共痕迹，但一旦问题被外化成公共 Q&A 页面，它又可能比提问者之后的真实生活保存得更久。

所以以后研究“普通人当时怎样找答案”不能只数还活着多少搜索首页、百度知道页或门户目录。

必须同时问：

1. 当时用户通过什么 input model 提问？
2. 当时系统能看到什么 corpus？
3. 哪些选项被排序到前面？
4. 哪些需求被变成公共页面，哪些永远是私人 query？
5. 答案是否有时间有效期？
6. 页面活着时，它的来源还活着吗？
7. 用户最后有没有据此行动？

这就是本文件的核心 evidence boundary：

> **archived discovery interface ≠ archived discovery event ≠ archived knowledge state ≠ archived lived outcome.**