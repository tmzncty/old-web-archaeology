# SEARCH / DIRECTORY / QUERY / RANKING / INDEX STATE GAPS, 1997–2015

Status: research note / state-gap model  
Scope: 约 1997–2015 中文 Web 中分类目录、门户搜索、网页搜索、站内/频道搜索、查询 URL、索引状态、排名/广告层与 archive blind spots；**不把本仓扩展为全球搜索史，也不把 2015 年后的平台/AI 搜索当成主对象**。  
Cross-repo companion: `tmzncty/how-people-lived/topics/from-knowing-where-to-look-to-typing-a-question-directories-search-engines-and-retrieval-labor-china-1980-2026.zh-CN.md`  
Last research pass: 2026-09-05

---

## 0. Why search is a special old-Web object

搜索页面看起来往往比论坛、网银、Webmail 简单：

```text
<input>
<button>
results
```

但一个历史搜索结果实际上依赖一条很长、且绝大部分不在公开 HTML 中的状态链：

```text
source page published
→ crawl allowed
→ crawler reached page
→ bytes fetched
→ charset decoded
→ document parsed
→ links/text extracted
→ document admitted to index
→ index snapshot activated
→ query submitted
→ query decoded/tokenized
→ candidate retrieval
→ ranking rules
→ paid/ad layer
→ geographic/device/session modifiers
→ result page rendered
→ user sees result
→ user clicks
→ destination still loads
→ information is still current
→ real-world action
```

公共 Web archive 最容易保存：

- 首页；
- 搜索框；
- 帮助页；
- 产品新闻；
- 某些带 query 的 SERP；
- 查询参数痕迹。

但最难保存：

- 当时完整 crawler frontier；
- 私有 index snapshot；
- ranking model/config；
- paid-placement state；
- 个性化/session；
- autocomplete；
- 用户失败的 query reformulation；
- click log；
- 用户最后是否相信/行动。

因此本 note 的核心命题是：

> **search interface survives far better than search state.**

一张 2003 年搜索页保存完整，并不等于我们已经复原“2003 年搜索某词会看到什么”。

---

## 1. Evidence contract

遵循 `docs/METHOD.md`。

### 1.1 Research units

必须分别记录：

- `search_platform`
- `host`
- `directory_taxonomy`
- `category_page`
- `search_form`
- `query_string`
- `query_url`
- `query_encoding`
- `result_page`
- `result_entry`
- `destination_url`
- `crawl_state`
- `index_snapshot`
- `ranking_rule`
- `paid_placement_state`
- `session_or_personalization_state`
- `capture`
- `claim`

不能把：

```text
“百度在 2001 年提供网页搜索”
```

和：

```text
“2001-09-20 14:03 一名北京网吧用户在 IE5.5 输入某个 GB2312 query 后看到了 A/B/C 三个结果且 A 是自然结果”
```

写成同一层事实。

### 1.2 Evidence grades used here

- **A**：历史 capture/WARC、同期产品/help/技术文档、当年 query URL/截图；
- **B**：同期媒体实测、教程、用户问题帖；
- **C**：后来公司史/怀旧回忆/现代镜像；
- **D**：根据参数、截图、后续产品行为推断的历史状态。

公司当前保留、标明 2001 日期的旧新闻可以证明“公司现在保存了这份同期文本”，但不自动等于 2001 年原 URL/HTML capture。

### 1.3 Privacy boundary

搜索 query 可以非常敏感。

本仓不得：

- 重新识别匿名用户的历史 query；
- 把可关联到具体普通人的 query log 批量发布；
- 从泄露日志重建个人疾病、性、财务、政治、家庭等敏感兴趣；
- 用 archive 重放会触发现代真实搜索账户/广告账户的操作。

优先研究公开界面、公开 SERP、产品规则与匿名化结构。

---

## 2. 目录页不是“低级搜索引擎”，而是另一种检索状态机

1990s 中文 Web 早期，人工分类/网站目录很重要。

当前可访问的 `sohuitc.cn` 页面保留了 1997–1998 风格内容，并称 1998 年搜狐推出大型分类查询搜索引擎、使用“出门靠地图，上网找搜狐”的口号。

Locator:
- https://www.sohuitc.cn/

Evidence:
- C / locator：**不是本轮实际打开并验证过的 historical memento**；不能把页面当前呈现自动当 1998 原始 capture。

目录式检索的状态链与全文搜索不同：

```text
site submitted/discovered
→ editor/category process
→ taxonomy category assigned
→ category page published
→ user navigates category path
→ listing visible
→ user clicks target
```

增加：

## **directory-taxonomy state gap**

一个 2001 年的分类路径：

```text
首页 > 生活 > 求职 > 北京
```

不能证明：

- 1999 年 taxonomy 也一样；
- 同一站点一直被归在该类；
- 分类标题含义没有改；
- listing 顺序相同；
- 编辑规则相同。

### 2.1 Category URL survives ≠ category membership survives

即使历史 category URL 被 archive 保存，列表里某站的出现/消失仍可能由：

- 人工编辑；
- 自动生成；
- 商业推荐；
- 死链清理；
- taxonomy 重构；
- archive 子资源/分页缺失

共同决定。

所以目录研究必须按 capture datetime 保存 **membership snapshot**，不能把平台级 taxonomy 当永久属性。

---

## 3. 2001：同一个“搜索”品牌已经包含多个完全不同的 corpus

百度当前保存的 2001-01-15 公司新闻称，为 263 提供的产品组合包括：

- 网页搜索引擎；
- 网站目录系统；
- 特定网站/频道内容检索；
- “实时信息系统”。

Source:
- https://home.baidu.com/home/index/news_detail/id/16970

Evidence:
- A-/B+：公司保留的同期文本；不是本轮验证过的 historical memento。

这要求 old-Web 研究增加：

## **query-interface / corpus gap**

一个视觉上相同的 search form 可能查询：

```text
human-edited directory
OR crawled Web pages
OR news database
OR one portal's local corpus
OR one channel
OR real-time feed
```

因此：

> **search box exists ≠ corpus known**

### 3.1 “站内搜索”与“Web 搜索”不能从按钮文字推断

必须尽量查：

- form `action`；
- hidden fields；
- query parameter；
- result host；
- help text；
- product announcement；
- source/result labels。

如果这些子资源未保存，应写 unknown，而不是靠今天同品牌产品补全。

---

## 4. 搜索索引有自己的时间，和页面时间不同

历史 SERP 至少可能涉及四个时间：

```text
source_page_published_at
crawler_fetch_at
index_snapshot_at
serp_rendered_at / archive_capture_at
```

它们可以不同。

增加：

## **index-time / page-time gap**

例如：

- 页面 3 月更新；
- crawler 4 月抓取；
- 5 月页面删除；
- 搜索结果 6 月仍显示旧 snippet。

所以 6 月 SERP 能证明：

> 某 index state 当时仍返回了该结果。

它不能单独证明：

> 6 月原页面仍然存在或内容仍一样。

### 4.1 Archive capture time is yet another clock

如果 Wayback 在 6 月保存 SERP，但 destination page 只保存到 3 月：

```text
SERP capture = 2004-06
source capture = 2004-03
```

不能把两张页面拼成“同一时刻的浏览体验”。

---

## 5. Crawler visibility gap：页面存在不等于会被搜索到

增加：

## **crawler-visibility gap**

页面可能真实存在，但因为：

- robots；
- 登录；
- session URL；
- JS 动态生成；
- forms-only navigation；
- 无入链；
- charset/parse 问题；
- crawler 策略；
- crawl budget；
- spam filtering；
- index policy

而没有进入某个搜索引擎。

因此：

```text
no result
≠
page did not exist
```

这一点对 `old-web-archaeology` 尤其重要，因为今天研究者若只靠历史搜索引擎/现代搜索结果寻找站点，会系统性偏向：

- 被链接多的站；
- 被搜索引擎喜欢的站；
- 技术上容易抓的站；
- 长寿域名；
- 公开静态页。

于是产生：

## **search-result survival bias——搜索结果幸存偏差**

历史 Web 中“更容易被找回”的东西，不必然是当时“最普通”的东西。

---

## 6. 2001：排名不再只是技术排序，还可以直接由付费规则改变

百度当前保存的 2001-09-20 企业新闻把“竞价排名”明确描述为：客户购买关键词，搜索结果可按竞价高低排序；2001-12-17 的企业新闻又称该模式进入多个中文门户搜索系统。

Sources:
- https://home.baidu.com/home/index/news_detail/id/16984
- https://home.baidu.com/home/index/news_detail/id/16994

Evidence:
- A-/B+：同期公司规则/市场材料；覆盖范围与效果属于公司 claim，需要独立来源才能升级。

增加：

## **paid-ranking state gap**

对于一条历史结果，至少应区分：

- natural/organic result（若能确认）；
- paid placement；
- portal partnership placement；
- directory editorial placement；
- unknown。

### 6.1 Rank #1 is not a stable historical fact

即使 query 字符串完全相同：

```text
rank(q, t1) ≠ rank(q, t2)
```

原因包括：

- index update；
- paid bid change；
- ranking algorithm change；
- spam action；
- URL canonicalization；
- news freshness；
- later geography/device/personalization。

所以：

> **“某站在某年最容易搜到”必须有当时 SERP/ranking evidence，不能用今天搜索排名倒推。**

---

## 7. 2008：搜索已经是大众网络动作，但 ranking literacy 不能假设

2009-03 CNNIC《2008年中国搜索引擎用户行为研究报告》相关发布显示，近 2/3 的受访搜索用户表示不知道搜索结果排列规则。

Source:
- 中国互联网协会转载：
  https://www.isc.org.cn/article/10314.html

Evidence:
- A-/B+：CNNIC 报告的同期转载。

这意味着研究 historical UX 时，不能只复原“系统实际上怎样排序”，还要保留另一层：

## **user ranking-model gap**

```text
actual ranking rule
≠
what user believed ranking meant
```

一个用户可能把：

- 第一条；
- 带商业关系的结果；
- 编辑推荐；
- 自然排名

统统理解成“最相关”。

这会直接影响普通人的信息选择，但公共 archive 几乎无法保存这种认知状态。

---

## 8. Query 本身也是历史 artifact，但通常保存得极不完整

带 query 的历史 URL 有时会保存：

- query text；
- page number；
- charset parameter；
- category/source parameter；
- sort mode。

但不能把一个保存的 query URL 当成完整 search session。

真实 session 可能是：

```text
q1: very broad
→ no useful result
→ q2: add city
→ q3: change spelling
→ q4: quote phrase
→ click
→ back
→ q5: search company name + 骗子
```

archive 可能只保存 q4。

增加：

## **query-reformulation gap**

这对研究“检索素养”尤其重要：成功 query 幸存，失败 query 往往消失。

### 8.1 Autocomplete / suggestions are highly ephemeral

建议词可能依赖：

- 当前热门 query；
- 用户历史；
- locale；
- session；
- live backend。

普通 HTML capture 很难保存某个用户当时看到的 suggestion state。

增加：

## **suggestion-state gap**

除非有：

- 同期截图；
- JS/API capture；
- HAR/WARC；
- 用户实测记录，

否则不得复原“当年输入这几个字会自动补什么”。

---

## 9. Query encoding / charset 是中文旧网的核心变量

历史中文 search form 可能涉及：

- GB2312；
- GBK；
- Big5；
- UTF-8；
- browser URL encoding；
- server-side decode；
- search-engine internal normalization。

2013 年后公开教程能看到百度查询 URL 曾暴露诸如 `wd`、`ie=gb2312`、分页参数等结构，但：

> **2013 参数不能无证据倒推 2001。**

因此增加：

## **query-encoding gap**

一个 historical search form 若只有 screenshot，而没有 HTML/form/traffic，不能猜：

- input name；
- `GET` / `POST`；
- charset；
- server decode；
- URL escaping；
- result endpoint。

中文编码错误可能直接改变“搜不到”的历史体验，所以不是实现细节。

---

## 10. Search result page ≠ destination page ≠ information outcome

完整状态链：

```text
query submitted
→ result returned
→ result visible in viewport
→ user notices result
→ click
→ target request
→ target loads
→ target content legible
→ user trusts it
→ user acts
→ real-world outcome
```

增加：

## **SERP / click / outcome gap**

一个 archive 保存了 query 和结果，只能证明：

- 某个结果页曾被保存；
- 在该表示中某条结果可见。

不能自动证明：

- 当时普通用户都看见；
- 用户点击；
- destination 正常加载；
- 用户相信；
- 信息改变了行动。

### 10.1 Viewport matters

2000s 低分辨率屏幕、工具栏、IE chrome、门户 banner 可能让“首屏”与现代浏览器完全不同。

因此历史 ranking 研究应尽量记录：

- viewport；
- browser chrome；
- ad/banner 高度；
- page zoom（若有）；
- pagination。

`rank 8` 在 1024×768 中很可能意味着需要滚动。

---

## 11. 站内搜索、垂直搜索与 open-Web search 的边界

2001 百度企业新闻已经显示搜索服务可以被门户作为后台嵌入；同年另一份企业新闻称其“网事通”用于网站内部全文检索和垂直搜索。

Source:
- https://home.baidu.com/home/index/news_detail/id/16998

Evidence:
- A-/B+：公司同期材料。

这产生：

## **front-end brand / back-end provider gap**

一个 2002 门户用户可能认为自己“在 A 网站搜索”，实际后端由 B 公司提供。

反过来，同一 provider 可以给多个门户提供不同：

- corpus；
- ranking；
- skin；
- paid placement；
- result URL。

所以平台史不能只按 logo 归档搜索系统。

---

## 12. 2010s：open-Web index 与平台内部 corpus 开始重新分裂

到 2010s，普通人越来越多地在：

- 电商；
- 微博；
- 微信；
- 问答；
- 招聘；
- 本地生活

等平台内部检索。

对于本仓 1995–2015 scope，关键不是追到 2026 小红书，而是记录一个边界变化：

> **external search no longer has a plausible claim to a unified searchable public experience.**

增加：

## **open-Web / platform-search gap**

一个信息对象可能：

```text
exists inside platform
AND is searchable inside platform
BUT is absent from external Web search
```

因此：

```text
Google/Baidu historical no-result
≠
Chinese online users could not discover it by any search route
```

尤其是登录墙、App 化、robots、动态页面出现以后。

本仓在 2015 左右停止扩展这条线；2015 之后平台搜索、推荐与生活决策的演变主要交给 companion `how-people-lived` note。

---

## 13. 一个最小 historical search evidence record

建议后续 schema 至少支持：

```yaml
search_event:
  platform: null
  host: null
  interface_url: null
  query_url: null
  query_text: null
  query_encoding: unknown
  corpus_type: unknown # directory/web/site/news/vertical/platform
  capture:
    archive_source: null
    capture_url: null
    original_url: null
    capture_datetime: null
  environment:
    browser: unknown
    os: unknown
    viewport: unknown
  index:
    crawl_datetime: unknown
    snapshot_datetime: unknown
  ranking:
    rule: unknown
    paid_placement: unknown
    personalization: unknown
  results:
    - rank: null
      title: null
      destination_url: null
      snippet: null
      placement_type: unknown
      destination_capture: null
  confidence: null
  known: []
  inferred: []
  unknown: []
```

重点是让 `unknown` 成为合法结果。

---

## 14. Archive blind spots specific to search

### 14.1 Interface survives, index dies

最常见：

```text
/search.html survives
search backend dead
```

页面看起来“可以输入”，但 replay 只剩 UI。

### 14.2 SERP survives, source dies

结果条目和 snippet 在 archive 里，却没有对应 destination capture。

这时可以证明 index 曾“记得”某页，不能复原完整页面。

### 14.3 Source survives, SERP dies

一个网站保存很好，但没有任何证据说明当年什么 query 能找到它。

不能从今天 SEO/标题推断历史 discoverability。

### 14.4 Current mirror is not historical capture

本轮找到 `sohuitc.cn` 这类当前可访问的早期风格镜像/页面线索，但没有把它升级为 1998 historical memento。

需要实际拿到：

- archive source；
- original URL；
- capture datetime；
- replay status；
- resource completeness；
- charset，

才能用于页面复原。

### 14.5 Corporate dated archive page is not original DOM

百度当前企业站保存很多标明 2001 日期的新闻稿。

它们是强文本 provenance，但只能证明：

> 当前企业历史库保存了这份同期文本。

不能据此猜 2001 原站：

- CSS；
- charset；
- URL；
- frames；
- search form；
- query endpoint。

---

## 15. New state gaps introduced in this pass

本轮新增：

- `directory-taxonomy state gap`
- `category-membership gap`
- `query-interface / corpus gap`
- `index-time / page-time gap`
- `crawler-visibility gap`
- `search-result survival bias`
- `paid-ranking state gap`
- `ranking-version gap`
- `user ranking-model gap`
- `query-reformulation gap`
- `suggestion-state gap`
- `query-encoding gap`
- `SERP / click / outcome gap`
- `front-end brand / back-end provider gap`
- `open-Web / platform-search gap`
- `interface-survival / index-loss gap`

这些 gap 共同指出：

> **搜索引擎不是一张“关于当时 Web 的客观目录”。它是某一时刻 crawler、index、taxonomy、ranking、商业规则与用户 query 共同生成的一次视图。**

---

## 16. Known / probable / unknown

### Confirmed enough for this note

- 1990s 末中文 Web 已有大型分类目录/查询型入口；
- 2001 百度同期企业材料明确区分网页搜索、网站目录、站内/频道检索等产品；
- 2001 百度企业材料明确描述按关键词竞价影响排序的排名模式；
- 2008 CNNIC 用户研究显示大量用户并不理解结果排序规则；
- 2010s 平台内部搜索与 open-Web search 并存，使可检索 corpus 更碎片化。

### Probable / needs stronger capture evidence

- 早期搜狐具体 taxonomy、search form 与原始 query URL pattern；
- 2001 百度/263 门户皮肤与后端参数的逐字段关系；
- 不同门户使用百度后端时是否共享完全相同 ranking/index snapshot。

### Unknown / intentionally not reconstructed

- 1998 搜狐原 DOM / charset / form action；
- 2001 百度某一历史 query 的完整 index snapshot；
- 某个普通用户当时看到的 autocomplete；
- paid ranking 与自然结果的所有历史视觉标记版本；
- 个别历史 query 是否真正导致现实行为。

---

## 17. Negative result of this pass

本轮**没有取得并实际打开、检查一份足够复原 1998–2001 搜狐/百度核心 search flow 的 verified Wayback/WARC capture**。

因此没有把：

- 搜索引擎检索结果里的 locator；
- 当前公司历史页；
- 当前镜像；
- 2013 参数教程

伪装成 1998–2001 原始页面。

下一步最有价值的旧网证据是：

1. 一份 1998–2001 分类目录 capture；
2. 一份实际带 query 的 SERP capture；
3. 对应 destination capture；
4. 原始 charset/form action/query encoding；
5. 至少两个时间点比较 taxonomy/ranking/interface 变化。

如果只剩首页和公司回忆，就停在 state-gap note，不宣称“搜索体验复原完成”。

---

## 18. What this changes about old-Web archaeology

以后不能再把“我今天搜到了这个历史页面”理解为对历史代表性的证明。

应额外问：

```text
当年它能被搜到吗？
用什么词？
在哪个引擎/目录？
是否需要知道分类路径？
是否付费排名？
当时 index 多新？
没有被搜到的页面去哪了？
```

这使搜索引擎本身从“研究旧 Web 的工具”变成“需要被考古的历史中介”。

最关键的结论是：

> **old Web 的历史可见性至少经过两次选择：当年的搜索/目录先选择什么容易被人看见，今天的 archive 与现代搜索又选择什么容易被研究者重新看见。**
