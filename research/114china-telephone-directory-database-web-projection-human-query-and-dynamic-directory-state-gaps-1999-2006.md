# 114china：电话号簿数据库向 Web 的投影、人工查询与动态目录状态缺口（1999—2006）

> 类型：research note / artifact-escalation note。不是 M1 complete case。
>
> 范围：只研究与约 1995—2015 中文 Web 直接相关的 114 / 网上 114 / 号码百事通投影问题。纸质电话簿、160/168、法国 Minitel 等更长的生活史与跨国比较主要放在 `how-people-lived`。

## 0. 本轮为什么值得写，而不是再造一个 `STATE_GAPS`

仓库已经有大量交易、账号、动态页面 state-gap 研究，因此“搜索框背后有数据库”本身不够构成新专题。

本对象真正新增的是一个中文旧网考古问题：

> **1999 年的 `114china.com` 并不是从零建立一套 Web 数据，而是把已有电话查号数据库的一部分投影到 Web。人工接线员、内部数据库、公开 Web、广告信息和隐私过滤之间不是同一个状态空间。**

这使它同时具有：

- 中文 Web 早期公共服务史价值；
- 电话基础设施 → Web 的直接谱系价值；
- 动态查询页面的 archive-gap 价值；
- privacy/filtering state 的考古价值；
- 人工解释层无法被网页 capture 保存的特殊缺口。

它不是把 OWA scope 推到 1980s，而是在解释 **1999 年中文 Web 页面到底从什么旧系统长出来。**

---

## 1. 研究单位必须拆开

本 note 至少区分以下对象：

```text
114 service
≠ operator workstation
≠ underlying telephone-directory database
≠ Web-exposed directory subset
≠ http://www.114china.com page shell
≠ one submitted query
≠ one historical result set
≠ merchant-added advertisement/details
≠ a Wayback capture
```

如果不拆开，很容易出现这种错误：

> “1999 年网上 114 有 230 多万条 Web 可搜记录。”

目前证据并不支持这种写法。1999-09 报道说的是 **114 查号台共有 230 多万个号码资源**，同时说 Web 建立在原数据库基础上；1999-12 报道又说网上 114 **已收录 20 多万条信息**。二者可能是：

- underlying number resources vs richer Web records；
- 试运行数据库 vs 正式开放数据库；
- 不同口径；
- 媒体写作误差；
- 系统在三个月内发生变化。

在没有历史 artifact 的情况下，不能自行选一个解释。

---

## 2. 已确认的 historical identity

### Claim 2.1 — 1999-09-15 之前/当日，北京已有“网上 114”试运行报道

《北京晨报》经新浪保留的 1999-09-15 报道称，记者前一天从北京 114 查号台获悉，“网上 114 台开始试运行”；历史 URL 明确给出：

```text
http://www.114china.com
```

报道描述的查询能力包括：

- 电话号码查询；
- 号码反查单位；
- 国内/国际区号；
- 旧号旧名查新号新名；
- 常用电话；
- 按单位名称；
- 按名称拼音首字母；
- 按行业类别。

同时明确说，网上 114 是在“查号台原有的数据库基础上”建立的。

来源：

- 北京晨报 / 新浪，1999-09-15，`https://news.sina.com.cn/society/1999-9-15/14567.html`

**Evidence grade: B**（同时代媒体，URL 与功能描述清晰；不是 archived-page artifact）

**Confidence: high**

### Claim 2.2 — 1999-09 报道明确存在 Web privacy projection

同一报道说，114 查询台有 230 多万个号码资源，但“此次 114 上网”基本不提供私宅电话，愿意将私宅电话用于商业活动者可另行联系。

这直接证明：

```text
underlying directory scope
!= Web-visible directory scope
```

**Evidence grade: B**

**Confidence: high**

### Claim 2.3 — 1999-12-27 报道再次记录 `114china.com` / `.net`，但 launch state 与记录数不同

另一篇《北京晨报》经新浪保存的 1999-12-27 报道称，网上 114 自助查询系统“将于近日开通”，并给出：

```text
http://www.114china.com
http://www.114china.net
```

报道说系统当时收录 20 多万条信息，除了电话号码，还包含地址、下属部门、业务内容、广告等；并存在“热线查询”、关键词/业务性质/产品名称等模糊搜索和号码反查，同时明确私宅电话不能查询。

来源：

- 北京晨报 / 新浪，1999-12-27，`https://tech.sina.com.cn/news/internet/1999-12-27/14203.shtml`

**Evidence grade: B**

**Confidence: high for what the report says; medium for exact launch state**

---

## 3. 一个不能被抹平的 contemporaneous contradiction

两篇 1999 年《北京晨报》材料形成了一个非常有价值的证据冲突：

| 日期 | launch wording | quantity wording | URL |
|---|---|---|---|
| 1999-09-15 | “开始试运行” | 114 查号台共有 230 多万个号码资源 | `www.114china.com` |
| 1999-12-27 | “将于近日开通” | 网上 114 已收录 20 多万条信息 | `.com` / `.net` |

### 当前允许的解释

- September = trial；December = formal public opening；
- 230 万 = 底层号码资源；20 万 = Web 上的 richer information records；
- 系统或编辑口径发生变化。

### 当前不允许写成事实的解释

不能直接写：

> “网上 114 从 230 万条缩到 20 万条。”

也不能写：

> “1999 年 9 月只是内测，12 月才第一次公开。”

除非取得页面 capture、官方公告或技术资料交叉确认。

这应登记为：

### `launch-state ambiguity`

以及：

### `database-scope ambiguity`

这类矛盾本身就是 artifact-first 继续推进的理由。

---

## 4. 这是旧电话数据库到 Web 的 projection，而不是“Web 搜索从零出现”

1999-09 报道已经给出直接 provenance：Web 服务建立在原 114 数据库基础上。

因此对象谱系至少应建模为：

```text
telephone-directory records
        ↓
114 internal database
        ↓
operator-mediated lookup
        ↓
privacy / publication / enrichment filters
        ↓
Web-visible directory subset
        ↓
114china page/query interface
        ↓
query result generated at request time
```

其中每一箭头都可能改变历史状态。

---

## 5. 新增状态缺口 1：`directory-database state`

Web shell 存在，不代表我们知道某个时点数据库里有什么。

要回答：

> “1999-12-27 搜‘地毯’会返回哪些单位？”

需要的不只是 HTML，还需要当时的：

- 条目集合；
- 单位名称；
- 分类字段；
- 电话号码；
- 地址；
- 旧名/新名映射；
- 旧号/新号映射；
- 更新时间；
- 停业/迁址状态。

Wayback 即使完整保存首页，也通常不能保存一次任意数据库查询在历史 backend 上生成的结果。

### Rule

```text
archived form != archived directory state
```

---

## 6. 新增状态缺口 2：`interface-projection state`

1999-09 已证明 Web 没有原样暴露全部底层数据：私宅号码被基本过滤。

因此每个历史时点都要问：

- 哪类记录能由人工 114 查询？
- 哪类记录能在 Web 查询？
- 哪些字段在 Web 公开？
- 哪些字段只在后台？
- reverse lookup 对哪些对象可用？
- 商业用户是否可主动 opt-in？
- 是否存在按用户/来源不同的 visibility？

这不是泛泛的“数据库动态”；它是**同一基础数据库向不同公共界面投影时形成的历史权限状态。**

---

## 7. 新增状态缺口 3：`human-interpreter loss`

电话 114 与 Web 表单的最大区别之一，是人工接线员能够承担 query normalization：

- 听到简称后猜正式名称；
- 追问城市/区县；
- 区分同音机构；
- 处理不完整记忆；
- 把自然语言映射到数据库字段。

Web 114 则要求这些能力由页面字段、模糊匹配算法和用户自己承担。

历史网页 capture 即使 100% 完整，也无法直接恢复：

- 接线员当时会问什么；
- 哪类口语表达会被成功理解；
- 哪些模糊需求人工能解决而 Web 搜不到；
- 哪些用户因为不会拼音首字母/正式名称而失败。

因此：

### `human-interpreter loss`

是本对象区别于一般动态目录页的关键 archive gap。

后续若能找到 114 接线员培训手册、操作规程、工作站截图或同期采访，应作为独立 artifact family，而不能从 Web 页面反推。

---

## 8. 新增状态缺口 4：`query-normalization state`

1999-09 报道明确提到：

- 单位完整名称；
- 名称“开口音”/拼音首字母；
- 行业类别。

1999-12 又描述了按业务性质、产品名称等模糊信息查询。

这些是很高价值的历史交互细节，但目前仍是媒体描述，不是已经检查的 form controls。

若取得 memento，应记录：

```yaml
query_modes:
  exact_name: unknown
  pinyin_initials: reported
  industry_category: reported
  product_keyword: reported
  reverse_phone: reported
  old_name_to_new_name: reported
  old_number_to_new_number: reported
normalization:
  charset: unknown
  fullwidth_halfwidth: unknown
  simplified_traditional: unknown
  punctuation_handling: unknown
  whitespace: unknown
  fuzzy_match_algorithm: unknown
```

不要把 1999 新闻里的功能名称直接翻译成今天意义上的 fuzzy search implementation。

---

## 9. 新增状态缺口 5：`privacy-filter state`

1999 两篇报道都明确说私宅电话不对 Web 查询开放/基本不开放。

这意味着历史页面研究必须把 privacy filter 当作页面功能的一部分，而不是法律/伦理背景注脚。

需要记录：

- 是否有 privacy notice；
- 是否解释 private residential exclusions；
- 是否允许商业用途 opt-in；
- reverse lookup 是否对个人号码直接拒绝；
- 错误消息是什么；
- 过滤发生在 query endpoint、result generation 还是数据导出前。

当前全部未知。

### 研究伦理

即使未来 archive 中存在个人住宅号码，本仓也不应为了“还原完整数据库”批量重新公开普通人的历史电话号码与地址。

研究平台结构时应优先保存：

- 字段 schema；
- privacy rule；
- redacted sample；
- result-count behavior；

而不是个人记录本身。

---

## 10. 新增状态缺口 6：`advertiser-overlay state`

1999-09 报道称商家可以发布自身信息并统计访问量；1999-12 报道又描述地址、下属部门、业务内容、广告和“114 广告”。

因此 Web 114 不是单纯“电话号码数据库镜像”。至少存在：

```text
base directory record
+ merchant-supplied enrichment
+ advertising layer
+ traffic/visit measurement
```

这会制造新的考古问题：

- 哪些文字来自电话号簿数据库？
- 哪些是商户后来填写？
- 哪些是广告字段？
- 搜索排序是否受广告影响？
- traffic statistics 是全站还是 merchant-level？
- “被访问量”如何定义？

在没有页面或后台文档之前全部保持 unknown。

---

## 11. 新增状态缺口 7：`update-lag state`

至少四个对象可能使用不同更新时间：

```text
paper telephone directory
operator-side 114 database
Web-exported directory database
merchant-added details/advertising
```

所以一个单位可能发生：

- 电话 114 已经有新号，纸号簿仍是旧号；
- Web 数据尚未同步；
- 商家广告文本已经更新但基础号码没更新；
- 旧名→新名映射只在某一界面存在。

1999-09 新闻宣称单位电话号码“随时更新”，但这是服务方/媒体对系统特性的描述，不应直接解释为零延迟一致性。

以后若做两时点 case，必须把**数据版本变化**与**页面模板变化**分开。

---

## 12. 新增状态缺口 8：`dynamic-result loss`

网上 114 本质上是查询系统。

若 archive 保存：

```html
<form action="...">
  <input name="keyword">
</form>
```

我们最多知道一个入口存在。

不能自动知道：

- endpoint 当时是否被 capture；
- GET 还是 POST；
- query parameter names；
- result pagination；
- result order；
- backend 是否在 archive replay 时被 live Web 污染；
- historical query 是否会被重写到现代服务；
- archive 是否保存任何具体 result page。

因此 M1 以后必须分别登记：

```text
shell capture
query form capture
submitted-query capture
result-page capture
backend state evidence
```

---

## 13. 1999 年电话信息网说明：Web 只是更大通信基础设施的一种界面

1999-09-29 《人民日报》报道，全国电话信息服务联网工程启动，通过专线把各城市连接到北京电报局，支持 160、168、169 电话信息服务；当时北京中心平台已经与 100 多家 168 信息台实时联网。

来源：

- 《电话信息服务迈向网络化》，《人民日报》1999-09-29；当前可检索历史文本镜像：`https://www.rmrb.zhouenlai.info/人民日报（1946-2003）/1999/09/1999-09-29.htm`

**Grade: A text / B current carrier**

对 OWA 的直接意义不是把 scope 变成电话史，而是提醒：

> **1999 年中文 Web 的一些数据库服务，其数据生产、维护和通信基础设施可能主要在 Web 之外。**

因此 old-Web provenance 不能从 `<html>` 开始才算。

---

## 14. 2002/2007 的生活指南保存了“多接口同场”的用户侧证据

Google Groups 当前可访问的 2007-04-02 转帖明确说，其中一份“北大生存手册”来自 2002 年未名 BBS 帖子。

当前 artifact 中，同一份实际生活指南并列列出：

- `114` 查号台；
- 160 系列火车/信息电话；
- 各种电话热线；
- `http://www.114china.com`；
- 票务网站；
- 北京公交网站。

来源：

- `https://groups.google.com/g/forcode/c/mQzaCEkX51A`

**Evidence grade:**

- 2007 Google Groups message itself：A（当前可定位 artifact，时间戳明确）；
- “2002 未名原帖”这一 provenance：C/B lead，未找到原始 BBS capture，不升级。

### OWA 意义

这说明如果我们只存 `114china.com`，会误以为用户已经处在一个主要由 Web 组成的信息环境里。

真实用户 information stack 至少包含：

```text
Web URL
+ telephone hotline
+ campus notice
+ BBS repost
+ person-to-person advice
```

所以对早期公共服务网站应记录：

### `companion-channel context`

即同一服务是否同时通过电话、短信、柜台、纸张、BBS 指南等渠道执行。

---

## 15. 2006 年“语音 Google”是反向证据：Web 没有单向淘汰电话界面

2006 年多家媒体记录，114 被升级为“号码百事通”，并被运营商/媒体称为“语音 Google”，提供餐饮、订票、家政、交通等综合生活信息与电话转接。

来源：

- 新华社/新浪，2006-03-07：`https://news.sina.com.cn/c/2006-03-07/08538379589s.shtml`
- 晶报/搜狐，2006-02-22：`https://news.sohu.com/20060222/n241950752.shtml`
- 深圳特区报/新浪，2006-02-22：`https://finance.sina.cn/sa/2006-02-22/detail-ikkntiak9949842.d.html`

**Grade: B**

这里不把“Google”当技术等同性，只把它当作同时代人的产品类比。

它证明至少在 2006 年，运营商并没有把电话查询看作注定退出，而是在把 Web 时代的“搜索”概念反投影到电话接口。

因此平台谱系不是：

```text
telephone directory -> Web -> telephone dead
```

而更接近：

```text
telephone directory database
├── operator interface
├── IVR / information service
├── Web projection
└── upgraded voice-search / transfer service
```

---

## 16. 海外 comparator：Minitel 只用于方法校正，不纳入 OWA 主对象

法国 Orange 官方历史记录，Minitel 自 1982 年商业推广，早期实验就包括电子电话簿；它依托 Transpac 而非 Internet，1980s—1990s 形成大规模家庭使用。

来源：

- Orange, `https://www.orange.com/en/our-groupe/our-history`

**Grade: B/A boundary, institutional retrospective**

### 它校正什么

它说明：

```text
electronic directory
!= Web directory
!= Internet service
```

因此 OWA 在写 `114china.com` 时不能用“电话簿第一次数字化”之类措辞。

本仓只保留这条作为 comparator note；Minitel 自身的普通生活史、终端普及与法国网络史应留在 HPL 或其他跨国研究，不扩 OWA scope。

---

## 17. 当前 artifact escalation 状态

### 已达成

- [x] historical service identity：北京网上 114；
- [x] exact historical host：`www.114china.com`；
- [x] second historical host variant：`www.114china.net`；
- [x] contemporaneous 1999 function descriptions；
- [x] provenance claim：Web 建在原 114 数据库基础上；
- [x] privacy-filter evidence；
- [x] 1999-09 / 1999-12 两个同期新闻时点；
- [x] 2006 电话“搜索”反向扩展证据；
- [x] 2007 可定位用户侧转帖 artifact，其中保存 `114china.com` 作为生活信息 URL。

### 未达成

- [ ] verified Wayback/Common Crawl historical page capture；
- [ ] capture datetime；
- [ ] historical replay HTTP status；
- [ ] historical DOM；
- [ ] Content-Type / charset；
- [ ] CSS / image / JS subresource inventory；
- [ ] query form field names；
- [ ] GET/POST behavior；
- [ ] result endpoint；
- [ ] a preserved historical result page；
- [ ] browser assumption；
- [ ] second verified Web artifact datetime；
- [ ] M1 complete case。

### 结论

```text
historical identity: ACHIEVED
historical exact URL: ACHIEVED
contemporaneous functionality: ACHIEVED
cross-channel provenance: ACHIEVED
verified historical Web memento: NOT ACHIEVED
M1 complete case: NOT ACHIEVED
```

---

## 18. Archive probe 的负结果应该怎样写

本轮没有获得一个可以实际检查的 1999—2001 archive replay。

正确写法：

> `Exact historical original URLs are known, but no historical memento was opened and verified in this run.`

错误写法：

> `Wayback 没有保存 114china.com。`

我们没有足够证据做后一个判断。

可能原因包括：

- 当前研究通路未命中；
- URL variant 不完整；
- archive index / replay 限制；
- robots；
- dynamic endpoint；
- capture 存在但没有被本轮发现。

按 `docs/METHOD.md`，`没有打开` 不能写成 `不存在`。

---

## 19. 若下轮取得 memento，最低记录模板

```yaml
subject: Beijing Online 114
site_host: www.114china.com
page_url: null
original_url: null
archive_source: null
capture_url: null
capture_datetime: null
accessed_at: null
http_replay_status: null
content_type: null
charset_header: null
charset_meta: null
page_title: null
browser_assumption: null

page_unit:
  shell: unknown
  query_form: unknown
  result_page: unknown

query_modes:
  exact_name: reported-not-verified-in-artifact
  pinyin_initials: reported-not-verified-in-artifact
  industry_category: reported-not-verified-in-artifact
  product_keyword: reported-not-verified-in-artifact
  reverse_phone: reported-not-verified-in-artifact
  old_name_mapping: reported-not-verified-in-artifact

privacy:
  private_residential_numbers_web_excluded: reported
  exact_ui_notice: unknown

subresources:
  css: unknown
  js: unknown
  images: unknown
  server_side_query_dependency: probable

state_gaps:
  directory_database_state: unresolved
  interface_projection_state: unresolved
  query_normalization_state: unresolved
  privacy_filter_state: partially evidenced
  advertiser_overlay_state: unresolved
  update_lag_state: unresolved
  dynamic_result_state: unresolved
  operator_interpretation_state: not recoverable from page alone
```

---

## 20. M1 适用性判断

`114china.com` **不是当前最优先的 M1 三类对象之一**，因为 ROADMAP 的 M1 明确要求：

1. 个人主页/主页托管；
2. 论坛/BBS/社区；
3. 博客/SNS/平台。

网上 114 更像 early public-service database / directory system。

因此即使之后 artifact 很丰富，也不应擅自拿它替换三类 M1 case；它更适合作为：

- dynamic-state method note；
- platform/database projection precedent；
- 后续 archive-gap model 的典型样本。

这避免仓库被大量事务/公共服务 state-gap note 反客为主。

---

## 21. 对 `datasets/sites.csv` / evidence schema 的启发

未来 schema 如果只记录：

```text
host
capture_datetime
html_saved
```

不足以描述这类对象。

建议至少预留：

```text
service_backend_family
public_interface_type
companion_channels
query_is_dynamic
result_state_archived
privacy_projection
human_intermediary_layer
historical_database_state_known
```

其中 `human_intermediary_layer` 很重要：一些早期中文 Web 服务不是替代原人工服务，而是从人工服务的数据库上长出第二个界面。

---

## 22. 已证实 / 高概率 / 不知道

### 已证实

- 1999-09 同期新闻记录北京网上 114 开始试运行；
- 历史 URL `www.114china.com` 明确；
- 新闻明确说系统建立在原 114 数据库基础上；
- 新闻描述按名称首字母、行业类别、号码反查、旧号旧名映射等能力；
- Web 投影明确过滤绝大多数私宅号码；
- 1999-12 又有同期报道记录 `.com` / `.net`、20 多万条信息与模糊查询；
- 2006 年 114 仍被扩展成综合生活信息电话服务；
- 2007 可定位转帖 artifact 把 `114china.com` 与电话热线并列进城市生活指南。

### 高概率

- 1999-09 “试运行”与 1999-12 “近日开通”可能对应 trial → formal opening，而不是完全矛盾；
- 230 多万“号码资源”与 20 多万“信息”很可能是不同数据粒度/公开范围；
- Web 114 的查询结果高度依赖服务器端数据库，因此单独 HTML shell 不足以重建历史行为。

这些仍然是 inference，不能写成事实。

### 不知道

- 第一个真正公开可用日；
- 首版首页长什么样；
- charset；
- form 字段；
- query endpoint；
- 1999 浏览器兼容要求；
- 是否有 frames/JS/ActiveX；
- result 排序逻辑；
- 广告是否影响排序；
- 数据同步周期；
- 人工 114 与 Web 114 具体记录数差异；
- 是否有可用 Wayback/Common Crawl artifact；
- 历史 query results 是否有任何保存。

---

## 23. 隐私与版权边界

本对象天然涉及普通个人电话号码与地址，因此后续 artifact 工作必须比普通门户首页更谨慎。

### 不做

- 不批量导出历史住宅电话号码；
- 不建立可搜索的个人 reverse-lookup 数据集；
- 不重新发布已从 Web 过滤掉的普通个人数据；
- 不因为 archive 可访问就镜像整个查询数据库。

### 可以做

- 保存 platform URL、capture metadata；
- 保存字段名、查询模式与 privacy notice；
- 用机构/公共服务号码作 redacted demonstration；
- 记录 result template，而不是个人记录全集；
- 比较记录数量、字段范围和过滤规则。

---

## 24. 后见之明风险

1. 不写“114 是百度/Google 的前身”。它们的数据库边界、索引对象与商业逻辑不同。
2. 不写“1999 年普通人已经普遍网上查号”。目前只有服务存在和可用性的证据，没有大众普及证据。
3. 不写“Web 淘汰了人工查号”。2006 的语音搜索扩展直接反驳这种线性叙事。
4. 不把电话后台数字化写成 Internet 普及。
5. 不把新闻描述的 fuzzy search 直接当成现代模糊搜索算法实现。
6. 不把 2007 转帖中的“2002 未名原帖”当成已经验证的 2002 BBS artifact。
7. 不根据今天 `114china` 品牌或域名状态反推 1999 技术系统。

---

## 25. 下一步精确任务

优先顺序：

### A. Artifact discovery

搜索并实际打开：

```text
http://www.114china.com/
http://114china.com/
http://www.114china.net/
http://114china.net/
```

时间优先：

```text
1999-09
1999-12
2000
2001
2002
```

### B. Capture verification

一旦命中，必须记录：

- original/capture URL；
- capture datetime；
- HTTP/replay 状态；
- title；
- charset；
- DOM；
- form method/action；
- subresources；
- error/login/redirect；
- 是否混入 live backend。

### C. Dynamic-result probe

只使用公共机构或无隐私风险的历史查询对象，不试探个人号码。

### D. Independent evidence family

继续找：

- 北京电信/北京电报局官方资料；
- 网站帮助页/FAQ；
- 1999—2001 用户教程；
- 报刊截图；
- 软件/系统集成商资料；
- Internet Archive / Common Crawl index metadata。

### E. Two-timepoint comparison

如果能取得 1999 + 2001/2002 两个时点，再比较：

- page layout；
- query modes；
- privacy notice；
- merchant fields；
- browser assumptions；
- URL structure；
- 数据/模板更新是否同步。

---

## 26. 本轮结论

`114china.com` 的考古价值，不在于证明“中国 1999 年已经有一个搜索网站”。更重要的是，它把一个**原本由接线员进入的电话目录数据库**部分投影到了公开 Web。

因此，一个真正可靠的复原不能只问：

> “1999 年首页是什么颜色？”

还必须问：

> “这个页面究竟暴露了后台数据库的哪一部分？哪些记录因隐私被排除？一次查询的结果是静态页面还是当时生成的状态？接线员原本承担的模糊理解和追问工作，Web 界面用什么字段或算法替代？今天的 archive 又保存了其中哪一层？”

如果这些问题没有答案，一个漂亮的 `114china.com` 首页截图仍然只是一个壳。
