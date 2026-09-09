# ONLINE DICTIONARY / WEB TRANSLATION / MACHINE TRANSLATION / SEMANTIC ACCESS STATE GAPS (2003—2015)

> Status: research package / state-gap note
>
> Scope: 中文旧网约 1995—2015。全球机器翻译前史只作为解释中文 Web artifact 的边界材料，不把本仓扩成全球 MT 史。
>
> Life-history companion: `tmzncty/how-people-lived/topics/from-paper-dictionary-to-ambient-translation-semantic-access-language-gates-and-cross-border-optionality-china-1995-2026.zh-CN.md`

## 0. 研究问题

旧 Web 中的在线词典和机器翻译很容易产生一种危险错觉：

> archive 里还看得见一个输入框、语言下拉框、`translate` 按钮，于是研究者以为“当年的翻译功能已经被保存”。

实际上，一个历史翻译页面至少可能包含：

```text
HTML shell
+ input form
+ source-language selector
+ target-language selector
+ charset assumptions
+ JS event handler
+ AJAX/POST endpoint
+ dictionary/MT backend
+ model / lexicon version
+ result renderer
+ follow-up webpage proxy
+ user-local browser/client integration
```

其中任何一层都可能没有被 archive 保存。

本稿集中处理：

- 在线词典 query；
- 网络释义 / 例句；
- 文本机器翻译；
- 整页 Web translation；
- 桌面词典 / 浏览器划词与 Web backend 的桥接；
- URL translation proxy；
- 2003—2015 中文互联网中的 service migration 与 backend drift；
- historical shell 与 current backend 混合形成的伪“回放”。

核心目标不是复原某个用户当年的私人查询历史，而是复原**一个普通中文 Web 用户当时怎样把“看不懂”转换成一次可执行的 query transaction**。

---

## 1. 与仓库 METHOD 对齐

本稿遵守 `docs/METHOD.md`：

- platform / host / page / capture / claim 分开；
- A/B/C/D 分级；
- 搜索结果里的 Wayback locator 不是 verified capture；
- `exists != available != used != popular != caused`；
- modern browser 成功渲染不等于 historical browser experience；
- `没有找到 != 当时不存在`；
- 不为了考古完整而公开真实个人的私人查询、翻译记录、聊天内容或敏感文本。

尤其固定：

```text
translation form captured
!= translation backend captured
!= historical result reproducible
!= historical model/lexicon preserved
!= historical user obtained same output
```

---

## 2. 研究对象必须拆层

### 2.1 platform

例：

- 海词 / Dict.cn；
- 金山词霸 / 爱词霸；
- 有道词典 / 有道搜索；
- Google Translate 中国入口；
- Yahoo!/Babel Fish 或 Bing Translator（仅海外对照/迁移背景）。

品牌连续不等于 backend 连续。

### 2.2 host

历史上可能出现：

- `dict.cn`；
- `www.iciba.com`；
- `dict.youdao.com` / 早期 `yodao.com` 相关入口；
- `translate.google.cn`；
- 其他 API / AJAX / static / CDN host。

同品牌 host 的变化应单独记录。

### 2.3 page

至少区分：

- dictionary home/search form；
- word entry；
- sentence/paragraph translation page；
- webpage URL translation form；
- help/download page；
- browser toolbar/plugin page；
- API/JS endpoint；
- user wordbook / history page；
- error/rate-limit page。

### 2.4 capture

一个 2008 年的首页 capture 可能只有 HTML 壳；另一个 2009 年 capture 才保存 CSS；结果页甚至可能完全没有进入 archive。

### 2.5 claim

优先窄写：

- `2007-09-19 网易官方稿宣布有道桌面词典测试版支持网页取词。`
- `2009-06 的用户工具清单列出沪江小D的 Firefox/QQ/MSN 等入口。`

不要写：

- `2008 年中国网民已经普遍通过在线翻译阅读英文网站。`

---

## 3. 前史边界：1995—2002 主要作为“为什么 Web 不是起点”

### 3.1 本地电子词典 / PC 软件先存在

中文旧网范围之外但直接相关的背景：

- 1995：文曲星等便携电子词典进入市场；
- 1997：同期媒体后来把金山词霸产品线起点记为 1997；
- 1999：金山词霸/快译等 PC 本地软件参与低价正版软件竞争。

来源：

- 新浪科技 2004 对词霸2005的同期评测，回述“金山词霸97年诞生”：<https://tech.sina.com.cn/s/n/2004-05-28/1821368709.shtml>
- 中关村在线，1999-10-26：<https://news.zol.com.cn/1999/1026/671.shtml>

证据边界：

- 1999 新闻可作 **B contemporaneous**；
- 2004 对 1997 的产品回顾只能作 **B/C**；
- 本轮未取得 1997 原始安装介质/手册，因此不把具体版本 UI 升为 A。

这段前史只为了说明：

> 中文 Web 在线词典出现时，用户已经熟悉“数字查词”，Web 新增的是远端更新、跨机器访问和网络语境，不是从零发明查词。

### 3.2 海外 Web 前史：Babel Fish 证明“整页翻译”不是 2008 才出现

SYSTRAN 公司历史把 1997 年 AltaVista Babel Fish 记为首个免费在线翻译服务；Microsoft 2012 年官方迁移公告证明 Yahoo Babel Fish 用户随后被迁往 Bing Translator，并说明当时仍支持 text/webpage translation。

来源：

- <https://www.systransoft.com/systran/>
- <https://www.microsoft.com/en-us/translator/blog/2012/05/30/welcoming-yahoo-babel-fish-users/>

用途：**全球技术前史 / cross-national comparison only**。

不要因此把 old-web-archaeology 主体扩到 AltaVista/Yahoo。

---

## 4. 2003—2007 中文 Web：online dictionary 的 artifact family

### 4.1 Dict.cn / 海词

当前 Dict.cn 页脚自述：

> 自 2003 年 11 月 27 日开始服务。

当前页：<https://sh.dict.cn/>

证据等级：

- 当前站对自身历史的声明：**A-current / C-history**；
- 不能据此描述 2003 年首页布局；
- 需要 historical capture 才能证明当年 form、charset、query URL 与 result DOM。

### 4.2 2006—2007 有道：dictionary 与 search engine 数据开始交叠

2006-12-15 新浪科技观察网易测试 `yodao.com`，列出网页搜索、博客搜索和词典；2007-09-19 网易官方发布桌面词典测试版，强调“网络释义”、网页取词与 Internet 词库；2007-12-11 正式版发布时继续列出海量词典/桌面词典。

来源：

- <https://tech.sina.com.cn/i/2006-12-15/13341290786.shtml>
- <https://www.prnasia.com/story/5436-1.shtml>
- <https://www.prnasia.com/story/7350-1.shtml>

证据：

- 新浪：**B contemporaneous independent media observation**；
- 网易 PR：**A contemporaneous vendor claim**。

可以支持：

```text
dictionary service existed
network-derived definitions were an explicit product feature
browser/page word-capture was advertised
```

不能直接支持：

```text
all definitions were generated live
all users saw identical results
market penetration
translation quality
```

---

## 5. Dictionary query state machine

一个最小 dictionary transaction 应拆成：

```text
D0 page shell loaded
D1 input focused
D2 query text entered
D3 encoding / normalization applied
D4 request issued (GET / POST / JS / AJAX)
D5 backend resolves query
D6 exact / fuzzy / derived entry selected
D7 result payload returned
D8 result DOM rendered
D9 pronunciation / example / related links optionally loaded
D10 user saves / copies / follows / adds to wordbook
```

### 必须避免的错误

`D0 survives != D4 endpoint survives`

`D4 endpoint responds today != historical backend reproduced`

`same query string != same historical result`

`word entry title survives != all examples/audio survive`

`HTTP 200 != semantically valid dictionary result`

---

## 6. 网络释义 / Web-extracted examples state gap

网络释义特别容易发生 historical drift，因为它可能依赖：

- search index；
- current Web corpus；
- ranking algorithm；
- spam filtering；
- current user submissions；
- editorial dictionary layer；
- cache refresh。

因此：

```text
2008 page URL opened in 2026
+ current backend returns definition
```

不能叫：

```text
2008 definition replay
```

更准确的名称：

**current-backend rehydration / 当前后端重水合。**

这和动态地图、路线、物流 tracking 等专题中的 current backend contamination 属同一大类，但这里的数据对象是“词义/例句”。

---

## 7. Text machine-translation state machine

```text
T0 translation page loaded
T1 source language selected / auto-detect enabled
T2 target language selected
T3 source text entered
T4 client normalization / length validation
T5 request issued
T6 source-language detection (if applicable)
T7 segmentation / tokenization
T8 MT backend processes
T9 translated payload returned
T10 result rendered
T11 user copies / edits / rates / searches / emails result
```

必须固定：

`form exists != T8 backend exists`

`backend exists today != same model/phrase table existed historically`

`same source text != same output across time`

`translated output fluent != output correct`

---

## 8. Webpage translation is not “text translation with a bigger box”

整页翻译至少还有：

```text
W0 user enters source URL
W1 translator fetches source page
W2 source HTTP/redirect/auth resolved
W3 source charset decoded
W4 HTML parsed
W5 translatable text extracted
W6 text translated
W7 links/resources rewritten or proxied
W8 translated wrapper rendered
W9 user clicks a link
W10 proxy decides whether/how to translate next page
```

### 8.1 必须区分 source page 与 translated representation

一个历史 translated-page capture 可能包含：

- 原站当年的内容；
- 翻译服务当年的 wrapper；
- archive rewrite；
- 今天已经失效的 proxied link。

时间至少有三层：

```text
source-content time
translator-render time
archive-capture time
```

若 source 本身来自数据库，还可能更多。

### 8.2 historical webpage translator 可能在 archive 中“看似可点击、实际上永远无法执行”

因为：

- archive 不会替用户 POST；
- translation backend 未被保存；
- 外部 source URL 后来失效；
- JS endpoint 被 robots/跨域/HTTPS 改变；
- 旧 charset 参数丢失；
- translated links 指向 live service。

因此一张漂亮的表单截图只能证明 **interface surface**。

---

## 9. 2008：Google/金山与中文 Web 翻译的扩展窗口

### 9.1 同时代第一人称：Google Translate 的语言扩展被用户立即观察

2008-05-11 博客园用户记录 Google Translate 对中文及更多语言互译的改进，并直接测试中文句子。

来源：

- <https://www.cnblogs.com/dingxue/archive/2008/05/11/1191900.html>
- evidence: **A contemporary public first-person**。

它能证明：

- `translate.google.cn` 作为用户认知中的入口存在；
- 用户会主动比较语言覆盖与输出效果；
- 翻译质量本身就是用户可观察/可嘲笑/可讨论的 Web artifact。

它不能证明：

- 2008 所有 query 都使用同一后台；
- 该 URL 的当日 DOM 已由本轮 archive 验证；
- 用户总体采用率。

### 9.2 谷歌金山词霸：local lexicon 与 remote MT 混合

2008 年同期产品资料描述联合版同时包含本地词典以及整句、全文、网页翻译等网络功能。

来源：

- <https://www.duote.com/tech/1/32.html>
- <https://www.cnblogs.com/anlyren/news/1170471.html>

这类 hybrid client 在考古时不能只抓官网：

```text
installer/package
+ local dictionaries
+ registry/config
+ browser hooks
+ remote translation endpoint
+ update service
```

才构成较完整 artifact family。

一个 2008 安装包今天即使能启动，也不保证远端 translation endpoint 仍在。

---

## 10. 2008—2010：browser/plugin/bot 让 translation transaction 离开主站首页

2009 年博客园用户整理的在线词典生态列出：

- 爱词霸；
- 沪江小D；
- 海词；
- 网页划词；
- Firefox 插件；
- QQ / MSN 机器人等。

来源：<https://www.cnblogs.com/yppjava/archive/2009/06/24/15690523.html>

evidence: **A/B contemporary user-curated ecosystem observation**。

这提醒 old-Web archaeology：

> 研究“一个在线词典”不能假定所有使用都发生在它的首页。

可能的 transaction origin：

```text
homepage
search-engine box
browser toolbar
context menu
mouse hover
desktop floating window
QQ/MSN bot
embedded widget on third-party blog
mobile WAP/client
```

所以 host capture coverage 与 real user entry points 并不一致。

---

## 11. Embedded dictionary widget / third-party page state gap

历史博客/个人主页可能嵌入：

- search box；
- JS dictionary widget；
- “划词翻译”脚本；
- iframe；
- external image/button；
- third-party form action。

archive 可能保存：

- widget 图标；
- `<form>`；
- JS 引用；

却丢掉：

- remote JS；
- query endpoint；
- response；
- login/cookie；
- historical result。

固定：

`embedded search box survives != embedded service transaction survives`

`button image survives != form action valid`

---

## 12. 2012 service migration：Babel Fish → Bing 作为海外对照

Microsoft Translator 2012-05-30 官方公告欢迎 Yahoo Babel Fish 用户迁往 Bing Translator，并说明 text translation、auto-detect、webpage translation 等能力。

来源：<https://www.microsoft.com/en-us/translator/blog/2012/05/30/welcoming-yahoo-babel-fish-users/>

此案例只作 comparator，但它暴露一个 old-Web 通用问题：

```text
brand A page
→ redirect/migration banner
→ brand B backend
```

若 archive 只抓到旧 URL 在迁移后的响应，研究者很容易把：

`old locator survives`

误写成：

`old service survives`。

因此新增：

**translator-service migration gap / 翻译服务迁移缺口。**

---

## 13. 2013—2015：history result vs current model drift

即使 brand 和 host 没变，翻译系统仍可能更换：

- rules；
- phrase tables；
- statistical models；
- dictionaries；
- language detection；
- ranking；
- post-processing；
- profanity/safety filters；
- segmentation。

因此对于一个 2011 query：

> 2026 年重新提交相同文本得到的译文，只能是**现代复算结果**，绝不是 historical output。

除非存在：

- 当时的 result page capture；
- screenshot；
- copied output in a contemporaneous post；
- local cache/log；
- preserved model/runtime。

否则不得宣称“复原了当年的翻译”。

---

## 14. Charset / encoding 是中文翻译服务的一级变量

1995—2010 中文 Web 常见：

- GB2312；
- GBK；
- Big5；
- UTF-8；
- form-urlencoded 参数；
- URL percent-encoding；
- JS `escape` / `encodeURIComponent` 差异。

错误 charset 可能导致：

```text
input mojibake
→ backend receives wrong text
→ translation failure / wrong output
```

因此：

`form visually readable != submitted Chinese text encoded correctly`

如果复原历史 query，必须记录：

- page `<meta charset>` / HTTP Content-Type；
- form `accept-charset`（若有）；
- request encoding；
- backend expectation；
- browser assumption。

现代浏览器自动修正不能当历史行为。

---

## 15. Language-pair availability is time-dependent state

一个服务“支持中文”不能简化成 boolean。

至少要记录：

```text
source language
source script/variant
→ target language
availability datetime
```

例如：

- Simplified Chinese → English；
- English → Simplified Chinese；
- Simplified ↔ Traditional；
- Chinese → Japanese；
- auto-detect → Chinese。

不同方向可能在不同时间上线，质量也不同。

因此新增：

**language-pair temporal drift / 语对时间漂移。**

2026 的语言下拉菜单不能倒写 2008 的支持矩阵。

---

## 16. Auto-detect creates hidden state

自动识别源语言后，UI 可能只显示“检测到英语”，却不保留：

- detection confidence；
- alternative languages；
- mixed-language spans；
- user correction；
- model version。

固定：

`auto-detect selected != source language correctly detected`

对于短词、人名、代码、混合中英尤其重要。

---

## 17. Audio / pronunciation / OCR 是独立 artifact family

在线词典/翻译服务往往继续增加：

- TTS/audio pronunciation；
- microphone input；
- OCR screenshot；
- image translation。

这些不能从文字结果页推断。

### audio

可能是：

- static mp3；
- Flash player；
- JS generated request；
- TTS backend。

`play icon survives != historical audio survives`

### OCR

```text
image
→ OCR text
→ translation
```

如果 OCR 错了，译文即使流畅也不能证明 translation layer 错误。

因此保存时要拆：

`OCR output` 与 `translation output`。

---

## 18. User wordbook / history：最有生活史价值，也最不应该公开挖掘

账号型词典常可能保存：

- 生词本；
- 查询历史；
- 收藏例句；
- 自定义词条；
- 学习进度。

这些数据可以非常直接暴露：

- 学业；
- 工作；
- 疾病；
- 性；
- 移民/签证；
- 财务；
- 私人通信对象。

因此本仓明确：

> **private semantic history is research-sensitive by design。**

高质量考古的目标是确认 schema/state/transaction，而不是恢复某位普通用户的真实查询历史。

优先顺序：

1. 官方 demo；
2. 帮助页；
3. 公开教程截图；
4. 自己构造的现代 test fixture（必须标 reconstruction）；
5. 公开自愿分享的历史截图/博客，且最小化个人信息；
6. 不批量抓私人 wordbook/history。

---

## 19. Dictionary / translation preservation levels

建议引入 S0—S8：

### S0 — claim only

只知道品牌/服务据称存在。

### S1 — historical locator

有同时代 URL，但未验证 capture。

### S2 — verified historical shell

已实际打开 archive capture，记录 `capture_datetime / original_url / HTTP / charset`，可见主表单。

### S3 — static UI/resources

CSS/图片/JS 的一部分保存，可判断历史页面形态。

### S4 — transaction syntax

能确认 query 参数、form action、language pair、GET/POST/JS 调用方式。

### S5 — historical result artifact

至少一个当时产生的 query result 由 capture/screenshot/contemporary copy 保存。

### S6 — multi-timepoint result comparison

同一 query 或可比 query 在多个历史时点有可核验结果，可分析 backend drift。

### S7 — client integration

历史桌面词典/插件/toolbar/bot 与 Web backend 事务关系有软件包/手册/网络证据。

### S8 — executable reconstruction with boundaries

在旧浏览器/保留客户端中可执行部分流程，并明确：

- historical original；
- missing backend；
- substituted backend；
- modern proxy；
- reconstruction 标记。

**S8 不要求重新获得任何真实私人用户查询历史。**

---

## 20. 本轮 historical replay 尝试

本轮尝试直接定位/回放以下约 2008 时点：

- `http://dict.cn/`
- `http://www.iciba.com/`
- `http://dict.youdao.com/`
- `http://translate.google.cn/`

当前 Web 访问链对直接构造的 Wayback replay URL 返回安全限制，未取得可逐项核验的：

- `original_url`；
- `capture_url`；
- `capture_datetime`；
- HTTP 状态；
- charset；
- DOM；
- form action；
- JS/AJAX endpoint；
- historical result。

因此严格记录：

```text
M1 verified Dict.cn historical capture: NOT ACHIEVED IN THIS SLICE
M1 verified iciba historical capture: NOT ACHIEVED IN THIS SLICE
M1 verified Youdao Dictionary historical capture: NOT ACHIEVED IN THIS SLICE
M1 verified translate.google.cn historical capture: NOT ACHIEVED IN THIS SLICE
```

这只表示：

> **本轮未完成 verified replay。**

绝不表示：

> Wayback 没保存 / 当时没有这个页面。

### 已有同期 locator / host evidence

- 2008-05-11 博客直接给出 `http://translate.google.cn`：<https://www.cnblogs.com/dingxue/archive/2008/05/11/1191900.html>
- 2009 用户工具清单给出 `http://www.iciba.com/`、`http://www.dict.cn/`：<https://www.cnblogs.com/yppjava/archive/2009/06/24/15690523.html>
- 2006/2007 有道同期官方/媒体材料证明词典产品存在，但历史 canonical query host 仍需 archive 进一步核验：<https://tech.sina.com.cn/i/2006-12-15/13341290786.shtml>

它们是 **historical locator / contemporaneous host evidence**，不是 capture。

---

## 21. Evidence matrix

| 对象 | 时间 | evidence | grade | 当前能证明 | 仍缺 |
|---|---:|---|---|---|---|
| 金山词霸/快译 | 1999 | 中关村在线同期报道 | B | PC 本地翻译软件、价格事件 | 安装介质/运行截图 |
| Dict.cn | 2003 | current self-history | A-current/C-history | 自述服务起点 | 2003 capture |
| 有道 | 2006 | 新浪同期观察 | B | 测试版含词典 | DOM/query syntax |
| 有道 | 2007 | 网易 PR | A-vendor | 网络释义/网页取词 advertised | verified capture/backend |
| Google Translate CN | 2008 | 博客园第一人称 | A-user | locator、用户试用与功能观察 | verified page/result capture |
| Google/Kingsoft Ciba | 2008 | 同期试用/媒体 | B | local+network translation hybrid | package/backend artifact |
| online dictionary ecosystem | 2009 | 博客园用户清单 | A/B | plugin/bot/widget entry points | 各入口 transaction capture |
| Babel Fish→Bing | 2012 | Microsoft official | A | service migration & features | 中文 Web scope 外，仅 comparator |

---

## 22. 核心 state gaps

### G1. shell/backend gap

`历史 UI 还在 ≠ 历史翻译能力还在`

### G2. query/result gap

`query 可以重放 ≠ 得到历史结果`

### G3. source-page/proxy gap

`translated wrapper capture != source page capture`

### G4. model-version gap

`same brand/URL != same MT model`

### G5. lexicon-corpus drift

`同一词条今天的网络释义 != 2008 网络释义`

### G6. language-pair temporal drift

`2026 支持的语言对 != 2008 支持矩阵`

### G7. charset/query gap

`页面中文正常显示 != 提交参数编码正确`

### G8. browser-hook gap

`desktop client launches != hover/page-capture hook works`

### G9. embedded-widget gap

`第三方博客按钮还在 != 翻译事务还活着`

### G10. service-migration gap

`old URL redirects != old service survives`

### G11. private-history gap

`wordbook UI survives != user's historical wordbook observable`

### G12. translation/action gap

`译文看起来可懂 != 用户可安全执行后续事务`

---

## 23. 对旧网页面形态的具体研究价值

在线词典/翻译服务是旧 Web 中很值得保留的一类**动作页面**，因为它不是单纯展示内容，而是把：

```text
form
→ request
→ backend computation
→ result
```

暴露给普通用户。

它可以帮助研究：

- 早期中文 form design；
- select/options 语言列表；
- GBK/UTF-8 转换；
- popup/result frame；
- frameset；
- JS/AJAX 迁移；
- browser toolbar；
- desktop-to-Web protocol；
- portal/search/dictionary 产品融合；
- third-party widget/bot；
- 服务停服/改名/redirect。

这类页面还特别适合证明：

> **旧 Web 的动态性并不只在 Flash 和 SNS。一个看起来很朴素的词典输入框，背后也可能依赖一个完全没有被 archive 保存的计算系统。**

---

## 24. Hindsight risks

### H1. 用今天结果重做旧 query

禁止写“2008 Google Translate 把 X 翻成 Y”，除非 Y 有同时代 artifact。

现代复算只能写：

> 2026 current service returns Y for the same source string.

### H2. 用 today language list 倒写旧支持矩阵

必须找 dated product/help/capture。

### H3. 把“网页翻译按钮存在”写成用户能够完成翻译

还需要 backend 与 source fetching。

### H4. 把词典例句当稳定出版物

network examples / user contributions 可能持续变化。

### H5. 把机器翻译“可用”写成“可靠”

历史用户经常把错误本身当趣味内容；可靠性必须另评。

### H6. 把中国正式接入 Internet 日期与在线翻译大众使用混成一条线

1994 full Internet connection、商业接入、家庭可及、2000s 在线词典是不同层级。

---

## 25. Privacy / copyright

### Privacy

不收集或重新公开：

- 普通用户私人 wordbook；
- 搜索/翻译历史；
- 私人聊天翻译；
- 医疗/法律/性/财务文本；
- 账号 cookie/token。

公开博客中用户自愿贴出的单句测试，也只保留支持 claim 所需的最少内容。

### Copyright

不把商业词典整库、历史词条全文、声音文件、软件光盘整体复制进仓库。

优先保存：

- URL；
- capture metadata；
- 字段与 query syntax；
- 自己的 state diagram；
- 小段必要截图/摘要（许可允许时）；
- 软件 hash/版本信息；
- 版权清晰的 fixture。

---

## 26. 下一步最有价值的 bounded tasks

1. 在可直接访问 Wayback/CDX 的环境中定位 `dict.cn` 2003—2005 的首批 capture；
2. 找 `iciba.com` 2004—2009 的 form action 与 charset 演化；
3. 找有道 2006 测试版 / 2007 桌面词典的 installer 或帮助文档，确认网络释义 endpoint；
4. 找 `translate.google.cn` 2008 的至少两个 capture，记录 language list 与 result UI；
5. 对同一个公开、非敏感、短字符串寻找 2008/2010 同期 pasted output，建立 result-drift fixture；
6. 找一个 2008 网页划词/toolbar artifact，确认 IE/Firefox/browser hook 条件；
7. 检查 QQ/MSN dictionary bot 的账号/协议/返回格式，但不要抓私人聊天；
8. 找一个中文博客嵌入在线词典 widget 的 verified capture，研究 third-party dependency；
9. 设计 `translation-evidence.yaml` 最小字段，与仓库 future evidence schema 对齐。

建议字段：

```yaml
platform:
host:
page_url:
capture_url:
capture_datetime:
charset:
client_environment:
transaction_origin: homepage|toolbar|plugin|bot|embedded|desktop
query_transport: GET|POST|AJAX|unknown
source_language:
target_language:
query_fixture:
result_artifact:
backend_historical: verified|probable|unknown|current-only
model_or_lexicon_version:
evidence_grade:
confidence:
privacy_notes:
reconstruction_notes:
```

---

## 27. 本轮结论

这一对象改变了中文旧网 archaeology 的一个默认假设：

> **“页面保存下来”并不等于“当年的意思生成机制保存下来”。**

在线词典和网页翻译恰恰是典型反例。archive 最容易保存：

- Logo；
- 输入框；
- 下拉菜单；
- 帮助文案；
- 下载按钮。

最容易丢失的却是：

- query backend；
- 当时词库；
- 当时语言识别；
- 当时机器翻译模型；
- 动态例句；
- 用户词本；
- 真正产生过的 historical result。

因此研究一个 2008 在线词典的正确问题不是：

> “这个网页今天还能不能打开？”

而是：

> **“2008 年一个中文用户在这个页面输入一个词或一个 URL 后，哪些状态发生在浏览器，哪些发生在远端，哪些被 archive 留下，哪些已经永远不能从页面壳里推回来？”**

这也是 old-Web 与 ordinary-life 交叉研究最有价值的地方：普通人的一项生活能力——“我不懂这句话，但我还可以继续往前走”——曾经依赖一整套看不见的 Web 后端；今天我们若只保存那只输入框，就很容易把当年的可执行生活误认成一张静态截图。
