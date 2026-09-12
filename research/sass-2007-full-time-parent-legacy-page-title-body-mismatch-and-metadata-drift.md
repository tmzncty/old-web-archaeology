# SASS 2007 全职父母旧内容页：title/body mismatch、机构站点迁移后的元数据漂移与来源恢复

> 状态：artifact/provenance research note
>
> 建立日期：2026-09-13
>
> Scope：中文机构网站旧内容的当前存活形态；不把 current live page 冒充 historical capture。

## 1. 为什么写这一条，而不是再加一个抽象 state-gap

本仓已经高度饱和。此 note 不再制造新的“页面 ≠ 真实状态”同义结论，而记录一个已经实际观察到、会直接影响历史研究结论的具体 artifact failure mode：

**一个机构网站当前仍能访问的 2007 年旧内容页，页面标题与正文属于完全不同的主题。**

这种错配会同时影响：

- 搜索发现；
- 引文元数据；
- 机器抓取；
- URL → 题名映射；
- 研究者对作者/文献身份的判断；
- 后续把旧网页转成结构化证据时的去重与 provenance。

这里把它暂称为：

**`metadata–body desynchronization / 元数据—正文失同步`**。

名称只服务于检查，不主张这是新理论。

## 2. 当前可观察 artifact

### URL

`https://www.sass.org.cn/_t31/2007/0308/c1201a25372/page.htm`

当前页面可公开访问。

### 页面当前显示的题名

页面 H1/搜索结果题名为：

> （女学者专辑）林荫茂：信访工作责任追究制若干问题思考

页面显示日期：

> 2007/03/08

### 但正文实际内容

正文从“一、国内外研究述评”开始，主题是**全职父母**，包括：

- 中国儿童中心“十大城市 0—6 岁儿童家庭调查”的背景；
- “全职父母”概念及主动/被动选择型区分；
- 上海家庭数据；
- 742 户拥有 0—18 岁子女完整家庭的量化数据说明；
- 5 位 0—6 岁儿童全职父母的质性访谈说明；
- 其中一名访谈对象为 34 岁男性、博士在读；
- 对竞争压力、失业、下岗、自愿生活方式选择等进入路径的讨论。

这些正文和“信访工作责任追究制”没有可见主题联系。

当前搜索引擎同样以错误/不匹配的 H1 题名返回这个 URL，但摘要抽取的是“全职父母”正文。

## 3. 当前可验证、不可验证的东西必须分开

### VERIFIED NOW

截至本轮检查，可以验证：

- URL 当前可访问；
- 当前页面显示日期 `2007/03/08`；
- 当前 H1 是“林荫茂：信访工作责任追究制……”；
- 当前正文主题是全职父母研究；
- 正文包含具体研究定义、样本与方法信息；
- 搜索引擎可以通过正文把它召回，同时仍展示不匹配题名。

### NOT VERIFIED

本轮**不能**验证：

- 2007-03-08 当天这个 URL 的实际 H1 是什么；
- 2007 原始页面是否已经存在当前这段正文；
- 当前 URL 是否等同于 2007 原始 URL；
- 错配究竟由 CMS 迁移、数据库 article-id 冲突、模板重建、人工覆盖、抓取错误还是其他原因造成；
- 正文在 2007 以后有没有被截断、转码、拼接或重写；
- 页面最初作者究竟是谁；
- 2007 原始 charset、HTTP response、DOM、附件、图片、导航和站点结构。

因此最准确的 artifact label 是：

**`current-live legacy representation carrying 2007-dated content, with verified title/body mismatch`**

而不是：

**`2007 historical webpage capture`**。

## 4. 为什么这会改变研究结果

### 4.1 只按 title 建索引，会把这份材料放错主题

题名检索会把它放进“信访/行政责任”主题，正文检索却会把它召回“全职父母/家庭社会学”。

因此：

`surviving URL != correctly surviving bibliographic identity`

网页还“活着”，不等于它的文献身份仍然完整。

### 4.2 只引用页面 H1，会产生严重误引

如果自动文献工具做：

`URL → <title/H1> → citation`

它很可能把全职父母研究正文引用成“信访工作责任追究制”。

对于旧中文机构站点，应增加至少一种校验：

`title semantic topic vs body semantic topic`

当两者完全不相干时，citation metadata 必须降级为 uncertain。

### 4.3 页面正文反而能纠正同期新闻摘要中的一个 denominator 风险

2007-03-29 东方早报/新浪报道同一研究时，一处称“对沪上 742 户全职父母家庭进行调查”，后文又说研究者分析的是“742 户拥有 0—18 岁子女的完整家庭”。

当前 SASS 正文明确写的是：

> 量化数据主要来自前期大型家庭问卷调查，对 742 户拥有 0—18 岁子女的完整家庭数据进行分析。

所以新闻开头的“742 户全职父母家庭”至少不能不加审查地作为 sampling frame 使用。

来源：
- SASS 当前 legacy representation：
  https://www.sass.org.cn/_t31/2007/0308/c1201a25372/page.htm
- 东方早报/新浪 2007-03-29：
  https://news.sina.com.cn/c/2007-03-29/044311520672s.shtml

这说明旧网页 archaeology 不只是“怀旧复原 UI”；它可以直接改变社会史统计材料的解释。

## 5. 同期资料生态：同一个数字如何在门户转载中继续存活

2007—2008 多个门户仍保存相关报道：

- 2007-03-29 新浪/东方早报：
  https://news.sina.com.cn/c/2007-03-29/044311520672s.shtml
- 2007-03-29 搜狐/东方网：
  https://news.sohu.com/20070329/n249058757.shtml
- 2008-08-26 新浪城市/文汇报：
  https://vic.sina.com.cn/20080826/10536396.shtml

这些 current-live legacy pages 仍保存 14%、42.5%、35.7%、21.4% 等数字及访谈片段。

但它们不能机械地被当成多个独立证据：

- 部分是同一研究的不同媒体摘要；
- 部分稿件可能互相转载；
- 分母描述并不总一致；
- 2008 报道是否完全使用 2007 同一数据，本轮未验证。

这与仓库已有 `syndication amplification` / denominator provenance 原则一致，本 note 不另造概念。

## 6. 新增的考古检查：legacy page 的“文献身份完整性”

建议对这种 current-live old-content page 加一个轻量检查块：

```yaml
legacy_page_identity:
  current_url: ...
  displayed_date: ...
  current_h1: ...
  current_html_title: unknown|...
  body_topic: ...
  title_body_match: yes|no|uncertain
  named_author_in_body: ...
  body_has_internal_title: yes|no|uncertain
  original_url_verified: yes|no
  historical_capture_verified: yes|no
  migration_or_rebuild_date: unknown|...
  suspected_failure_mode: unknown|metadata-body-desynchronization|...
  search_engine_title_matches_h1: yes|no|unknown
  citation_identity_status: verified|partial|unsafe
```

关键规则：

**不要根据当前 URL 路径中的年份，自动把当前 DOM 当作该年份的 DOM。**

**不要根据机构域名，自动认为当前题名—作者—正文绑定仍然可靠。**

## 7. 与 METHOD 的关系

这次没有改动 `docs/METHOD.md`，因为单一案例还不足以升级主规范。

但它补充了 M1 以外的一种常见来源：

`current live legacy representation`

这类来源可以非常有价值，尤其当正文保存了同期研究文本；但必须和：

- historical capture；
- original source file；
- contemporary mirror；
- later institutional reconstruction

分开标记。

## 8. 为什么“标题错了但正文还在”特别值得保留

旧网消失不只有 404。

还有一种更隐蔽的消失：

**正文仍在服务器上，但它和自己的名字失散了。**

对人类研究者来说，这意味着：

- 知道原题的人可能永远搜不到；
- 搜到 URL 的人可能因为标题不相关而直接跳过；
- 自动抓取系统可能把正文错误归类；
- 后来的引文可能继续复制错误元数据；
- 一份“没有丢失”的文献，在知识层面却已经半失踪。

这可以称作**bibliographic partial loss / 书目身份部分丢失**，但目前只作为描述性风险使用。

## 9. HPL 交叉意义

该页面正文让 `how-people-lived` 能够把 2006—2008 的“全职父亲”从媒体奇观进一步拆成真实路径：

- 主动选择；
- 找工作困难；
- 失业/下岗；
- 配偶职业更强；
- 为教育孩子退出；
- 家庭经济允许的自愿退出。

对应研究包：

`tmzncty/how-people-lived/sources/contemporaneous-full-time-fathers-care-role-reversal-and-household-care-allocation-china-2006-2025.zh-CN.md`

所以这一 artifact case 不是独立的站点 bug 收藏，而是**直接影响普通生活史解释**。

## 10. 海外比较放在哪里

本仓 scope 不扩成全球旧网页仓库。

跨国层面的 stay-at-home father 数据与美国 Great Recession 对照写在 HPL；OWA 只保留这个中国机构旧内容页的 provenance / preservation 问题。

## 11. M1 状态

### Achieved this slice

- 检查到一个当前可访问、标注 2007 日期的中国机构 legacy page；
- 验证当前 title/body mismatch；
- 用同期门户文本做了主题与 sampling-frame 交叉确认；
- 形成可复用的 legacy-page identity 检查字段。

### NOT achieved

本轮未取得该 SASS 页面在 2007 年的合格 historical capture，因此：

**`M1 historical SASS full-time-parent Web case: NOT ACHIEVED IN THIS SLICE`**

缺少：

- capture datetime；
- 2007 original URL verification；
- historical HTTP/replay status；
- historical charset；
- 2007 DOM/source；
- 页面资源与附件；
- 至少第二个历史时点。

不能把“现在显示日期 2007”替代这些字段。

## 12. 下一步最值钱的动作

1. 用原文短句、作者名、可能的研究题名继续定位这篇全职父母研究的正式论文/会议稿；
2. 查 Internet Archive / Common Crawl 是否存在该 SASS 内容或更早域名下的版本；
3. 找到站点历史 sitemap、CMS 迁移说明或旧链接表，判断 title/body mismatch 是何时形成；
4. 如果能找到历史 capture，对比：H1、author、date、正文首段、charset、URL 与当前版本；
5. 不优先再收集十个类似“网页旧了”的案例，除非它们能证明一种系统性迁移模式。

## 13. 本轮对仓库的新增价值

本轮不是又一个事务 state-gap，而是一个**已验证的来源完整性故障**：

`page survives` 但 `bibliographic identity partially fails`。

它要求旧网研究在“URL 还活着吗”之外，再问一句：

> **这个还活着的页面，仍然知道自己是谁吗？**
