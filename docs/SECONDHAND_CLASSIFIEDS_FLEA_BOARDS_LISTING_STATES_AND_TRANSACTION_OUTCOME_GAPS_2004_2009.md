# 二手分类信息、校园跳蚤板与交易结果缺口（2004–2009）

> 状态：bounded research note；**不是 M1 完整案例**。
>
> 主体范围：2004–2009 中文旧网中的校园 BBS 二手板、校园论坛、专门二手网站与分类信息网站。
>
> 边界：本篇不写 2014 以后移动端闲置平台史，也不把全球 Craigslist / eBay 史塞入本仓。1998 年旧货制度仅作为“Web 不是起点”的前史边界。
>
> 研究问题：**一条“二手出售”网页究竟证明了什么？从 listing 到成交之间，哪些状态存在于 Web 上，哪些会转入 QQ、电话和线下，并因此从档案中消失？**

---

## 0. 为什么现在研究它

本仓已有：

- 招聘信息与线下执行缺口；
- 婚恋 profile 与互选结果缺口；
- 租房 / roommate listing 与共同居住结果缺口；
- 搜索 query / ranking state 缺口；
- 网银交易与 backend clearing shadow；
- Qzone 的客户端 / 浏览器 / Flash / 装扮资源链。

这些材料已经证明：

> **页面存在通常只覆盖真实生活流程的一部分。**

二手交易特别适合进一步检验这一点，因为它往往经历：

```text
公开 listing
→ 私下询问
→ 议价
→ 线下看货 / 面交 / 发货
→ 付款
→ 商品离开卖家
→ listing 删除 / 标售出 / 过期
```

公开 Web 通常最容易保存第一步，最难保存最后几步。

因此本篇新增的不是“二手电商发展史”，而是一个 **listing-state archaeology**。

---

## 1. 研究单位

根据 `docs/METHOD.md`，本篇严格分开：

### platform

例如某校园 BBS、分类信息网站。

### board / category

例如：

- 二手物品；
- 跳蚤市场；
- 电脑数码；
- 图书；
- 家具家电。

### listing / post

一条具体的出售信息。

### account

发布信息的用户身份。

### contact endpoint

帖子里可能出现的：

- QQ；
- 电话；
- Email；
- 站内信。

### transaction

实际买卖过程。

### capture

档案服务保存的某个时点的页面表示。

### claim

研究者可以由一个或多个 evidence 支持的最小结论。

硬规则：

> **listing 是 artifact；transaction 是 event。两者不是同一个研究单位。**

---

## 2. 最小 claim list

| Claim | 当前等级 | 结论强度 |
|---|---|---|
| 2004 年同期报道已观察到校园 BBS 存在二手物品交易板块 | B | 已证实媒体当时如此记录 |
| 2004 年至少有学生认为“同校用户”降低了 BBS 交易的信任成本 | B | 已证实同期第一人称如此表达；不可推广至所有学生 |
| 2005 年高校二手信息同时出现于食堂 / 告示板 / 黑板 / 高校论坛，并通过 QQ / 电话等完成联系 | B | 已证实多渠道并存 |
| 2006 年 58 分类信息网把二手物品列为主要分类之一，并允许个人免费发布 | B | 已证实同期报道如此描述 |
| 2007–2008 年校园二手执行仍大量发生在线下回收者、宿舍、校园摊位 | B | 已证实同期媒体存在此类执行链 |
| 2009 年有学生专门购买域名建设面向本校的跳蚤网站，让卖家发布闲置物品信息 | B | 已证实同期报道 |
| 公开 listing 能证明交易完成 | — | **不能证明** |
| listing 消失能证明卖掉了 | — | **不能证明** |
| 当前仍可打开的旧 listing 页等于历史 listing state | — | **不能默认** |

---

## 3. 前史边界：Web 以前旧货市场已经承担“信息 + 评估 + 结算”

1998 年《旧货流通管理办法（试行）》把旧货市场定义为具有信息、评估、结算、加工翻新、保管、运输等配套服务的交易场所，并规定了来源 / 去向记录和出售者身份登记等要求。

官方保存文本：

<https://www.hengqin.gov.cn/lab/flfg/bmgz/content/post_3727256.html>

### 证据等级

**A：同时代制度文本。**

### 对本仓的边界意义

这证明：

> 旧货交换、信息服务、身份记录和交易结算并不是 Web 才出现。

本仓从 2004–2009 切入，是为了研究 **中文旧网怎样重新组织这些已有功能的页面与账号形态**，而不是把历史起点强行设在 Web。

---

## 4. 2004：校园 BBS 二手板是一种 bounded marketplace

2004 年 2 月的同期媒体报道提到，高校 BBS 的二手物品板块原先主要供学生交换闲置物品，后来也出现了更持续的经营行为。

一名被报道的学生解释，自己之所以选择 BBS，是因为使用者主要是本校学生，因此更容易建立信任。

来源：

<https://edu.sina.cn/sa/2004-02-19/detail-ikftssap7679469.d.html>

### 证据等级

**B：同期媒体 + 同期第一人称引语。**

### 4.1 board membership 是技术 / 社会混合条件

这里的“平台身份”不是纯技术账号。

它可能同时意味着：

```text
BBS account
+ school affiliation
+ shared campus geography
+ possible offline traceability
```

因此：

> **account trust ≠ platform reputation only**。

同校这一社会边界本身就是 trust layer。

### 4.2 archive 不能自动保存这种 trust layer

如果今天只剩一条帖子 HTML：

- 用户是否当时仍是在校生？
- 账号是否需要校园网注册？
- 是否可以校外访问？
- 是否有实名 / 学号绑定？
- 买卖双方是否实际认识共同的人？

都可能无法从帖子正文恢复。

因此新增：

**membership-context gap（成员资格语境缺口）**。

---

## 5. 2005：一个商品可以同时存在于黑板、论坛、QQ 和电话

2005 年《每日商报》关于高校二手市场的同期报道记录了一个典型的混合媒介环境：

- 食堂 / 校园现场；
- 告示板；
- 宿舍黑板；
- 高校论坛；
- QQ；
- 电话。

来源：

<https://www.zafu.edu.cn/info/1012/61669.htm>

### 证据等级

**B。**

### 5.1 cross-channel listing identity

一件自行车可能同时：

```text
黑板写一次
+ BBS 发一次
+ QQ 群发一次
+ 电话联系若干次
```

所以 archive 中看到 3 个文本，不一定是 3 件商品。

新增硬边界：

> **many listings ≠ many items ≠ many sellers**。

这叫：

**cross-post duplication（跨渠道重复）**。

### 5.2 contact endpoint 只是 handoff

如果网页只留下：

```text
QQ: xxxxx
Tel: xxxxx
```

它只能证明：

> 发布者提供了某种联系路径。

它不能证明：

- 有人联系；
- 联系时间；
- 询价次数；
- 谁先联系；
- 是否见面；
- 是否成交。

因此：

> **contact info visible ≠ contact occurred**。

---

## 6. 2006：分类信息页把城市生活拆成 category

2006 年 2 月新浪科技关于 58 分类信息网的同期报道把二手物品、交友、招聘等列为主要分类信息内容，并描述个人免费发布模式。

来源：

<https://tech.sina.com.cn/i/2006-02-12/1519838495.shtml>

### 证据等级

**B。**

企业融资和用户规模数字受到公司口径影响，不作为本篇核心结论。

### 6.1 category page 不等于 market inventory

分类页最容易让研究者产生错觉：

> “我抓到了 2006 年某个二手分类页面，所以我看到当时市场。”

实际上一个 category capture 可能只保存：

- 第一页；
- 某一排序；
- 某一城市；
- 某一查询条件；
- 抓取瞬间还没过期的 listings。

因此新增：

**classified-inventory snapshot gap（分类库存快照缺口）**。

一个 capture 只能证明：

> **在这个页面状态、这个抓取时点，档案服务保存了这些可见条目。**

不能直接推当月总 listing 数。

---

## 7. city / locality 是 listing schema 的核心状态

二手交易和纯文本讨论不同。

一个商品是否现实可买，通常高度依赖：

- 城市；
- 校区；
- 区县；
- 能否自提；
- 是否包邮；
- 物品体积。

所以旧网考古若只保存标题和价格，可能丢掉最决定交易可执行性的字段。

建议 evidence schema 扩展时考虑：

```yaml
listing_location_text: null
city_host_or_subdomain: null
pickup_required: unknown
shipping_offered: unknown
contact_channel: []
price_asking: null
price_negotiable: unknown
listing_state_observed: active|sold|expired|deleted|unknown
```

这些字段不是为了重建用户私人数据，而是为了记录**页面机制**。

---

## 8. 2007：毕业回收证明 listing 之外还存在另一条 execution path

2007 年 7 月毕业季报道记录，高校周边的线下回收者在短时间内大量收购毕业生电脑、自行车和小家电；一个被报道的极端例子，是学生一年前约 4000 元购入的电脑，被回收者以 200 元收走。

来源：

<https://news.sohu.com/20070703/n250881882.shtml>

### 证据等级

**B；单一个案，不代表平均折价。**

### 对旧网考古的意义

如果研究者只抓 BBS / 分类网站，会漏掉：

```text
没发帖
→ 直接叫回收者
→ 当场估价
→ 当场搬走
```

因此：

> **Web-visible secondhand activity ≠ total secondhand activity**。

这是 **channel-selection bias（渠道选择偏差）**。

不同类型卖家可能系统性选择不同渠道：

- 很急的人 → 回收者；
- 想卖高一点的人 → BBS / classified；
- 只想送人的人 → 熟人 / 宿舍；
- 大件 → 同城；
- 小件 → 更可能跨地域。

---

## 9. 2008：宿舍货架说明“网上可发现”不是必要条件

2008 年 11 月《南昌晚报》经中国新闻网保存的报道记录，高校寒假前的跳蚤市场中，有大四学生直接把衣服、书包、首饰等挂在寝室床位下售卖；几名低年级学生现场挑选并购买。

来源：

<https://www.chinanews.com.cn/edu/dxxy/news/2008/11-28/1467177.shtml>

### 证据等级

**B。**

### 方法边界

旧网仓在研究“校园二手网站”时必须留下这个反例：

> 同一年同一类人完全可以不经过 Web 完成交易。

否则我们会把“能被 archive 看见的人”误写成“当时的人”。

---

## 10. 2009：专门网站把校园二手从板块变成独立 host

2009 年 5 月《长江商报》报道，中国地质大学（武汉）一名学生花 300 元购买域名，建立面向本校学生的跳蚤网站；学生可以发布闲置物品，其他人看到后联系购买。

来源：中国地质大学新闻网保存：

<https://voice.cug.edu.cn/info/1006/7890.htm>

### 证据等级

**B。**

### 10.1 board → standalone site 不是线性进化

这条材料只能证明：

> 至少有人尝试把校园二手的需求做成专门 Web 服务。

它不能证明：

- BBS 被替代；
- 网站成为学校主流；
- 网站长期存活；
- 一周“有生意”意味着稳定成交；
- 未来专业平台必然由它演进。

正确写法是：

```text
physical flea market
BBS board
campus forum
standalone flea site
```

可以并行存在。

---

## 11. 二手 listing 的状态机

本篇建议把一条普通二手信息拆成：

```text
1. item exists
2. seller decides to sell
3. listing drafted
4. listing published
5. listing indexed / visible
6. potential buyer views
7. buyer contacts seller
8. negotiation
9. inspection / meeting / shipping arrangement
10. payment
11. physical handoff
12. dispute / acceptance
13. listing marked sold / deleted / expires / remains stale
```

公开旧网常常只保存 4–5。

所以每一个“看起来像交易”的旧页面都应先问：

> **我们到底观察到了状态机的哪一格？**

---

## 12. listing-state gap

### 定义

**listing-state gap**：

档案只能看到某时点的 listing 表示，无法确定它在真实业务中的状态。

例如今天 archive 里有：

```text
出售自行车 100 元
QQ: ...
```

可能对应：

- 刚发布；
- 已经被人预定但没改帖；
- 已经卖掉但没删；
- 电话失效；
- 卖家已经离校；
- 自动缓存页。

因此：

> **page live ≠ item available**。

---

## 13. asking-price gap

### 定义

旧网页往往保存的是 **asking price**。

但现实里可能：

```text
标价 200
→ QQ 里还价 150
→ 见面发现磨损
→ 120 成交
```

公开 Web 最后只剩 `200`。

因此：

> **asking price ≠ transaction price**。

如果以后做历史价格数据集，必须把字段写成：

```yaml
price_type: asking|sold|reported_transaction|unknown
```

不能把挂牌价批量当成交价。

---

## 14. contact-handoff gap

校园 BBS / classifieds 很多时候只是 contact router。

典型：

```text
Web post
→ QQ
→ 电话
→ 宿舍 / 校门见面
```

真正的：

- 对话；
- 议价；
- 预约；
- 取消；
- 交易结果；

全部离开公共 Web。

这叫：

**contact-handoff gap（联系转场缺口）**。

本仓应避免为了补这个 gap 去搜集或重新公开普通人的历史私人聊天记录。

---

## 15. transaction-outcome gap

### 定义

即使知道双方联系过，也不能自动知道：

- 是否成交；
- 谁买；
- 最终多少钱；
- 商品是否符合描述；
- 后来是否退货；
- 是否发生纠纷。

因此：

> **reply ≠ transaction**

> **meeting ≠ sale**

> **payment ≠ durable acceptance**

这与招聘、婚恋和租房研究里已经出现的 execution/outcome gap 方向一致，但二手交易有自己的商品状态与物理交付问题。

---

## 16. success-deletion bias：卖成了，页面反而更容易消失

二手交易有一个很强的档案悖论：

卖家交易成功后，最合理的动作往往是：

- 删帖；
- 编辑成“已出”；
- 删除电话；
- 让 listing 自动过期。

因此：

> **成功交易可能降低页面未来的存活概率。**

这叫：

**success-deletion bias（成功删除偏差）**。

### 后果

今天 archive 中长期幸存的 listing，可能系统性偏向：

- 没卖掉；
- 忘了删；
- 被第三方转载；
- 静态页面；
- 搜索引擎缓存。

所以：

> **surviving listing distribution ≠ historical transaction distribution**。

---

## 17. stale-listing bias：没删也不等于仍有效

与 success-deletion bias 相反，还有：

**stale-listing bias（僵尸挂牌偏差）**。

很多旧论坛不会强制：

- 标已售；
- 自动下架；
- 更新联系方式。

因此一个 capture 抓到旧帖，不能知道其业务有效期。

建议未来 evidence 记录：

```yaml
post_datetime: ...
capture_datetime: ...
last_edit_datetime: unknown
explicit_status: unknown
contact_validity: unknown
```

---

## 18. mutable-listing time collapse

一条 listing 可能多次编辑：

```text
原价 300
→ 250
→ 200 急出
→ 已出
```

如果 archive 只抓到最后一次：

> 价格变化和卖家的 deadline 都会消失。

如果只抓到第一次：

> 成交结果又会消失。

这叫：

**mutable-listing time collapse（可变挂牌时间塌缩）**。

它与本仓已有 mutable profile 问题相似，但 listing 变化更直接对应交易过程。

---

## 19. inventory-snapshot gap

一个分类页面通常依赖：

- 数据库；
- 查询；
- 时间排序；
- 城市；
- category；
- 是否登录；
- 翻页；
- 搜索关键字。

所以即使 category HTML 被保存，也不代表：

> 当时所有 listings 已经被保存。

这叫：

**inventory-snapshot gap（库存快照缺口）**。

### 特别注意 pagination

如果 archive 只保存第一页：

- 老帖可能完全消失；
- 热门排序会扭曲样本；
- 城市 / 子分类可能没抓；
- 下一页链接可能依赖 POST / JS。

因此不能用“抓到第一页有 30 条”推导整个站点规模。

---

## 20. photo / condition gap

二手商品比招聘和征友多一个特殊维度：**物理成色**。

列表文字可能保留：

- “九成新”；
- “无拆修”；
- “轻微划痕”。

但：

- 商品图片可能在独立图片 host；
- 缩略图保留，原图丢失；
- 外链相册失效；
- 图片后来被覆盖；
- archive 没抓到 JS gallery。

因此：

> **description survived ≠ condition evidence survived**。

旧网 reconstruction 不应根据文字自动生成 / 补画商品图。

---

## 21. seller-state mutation

账号旁边今天显示的：

- 发帖数；
- 级别；
- 在线 / 离线；
- 注册天数；
- 头像；

不一定是 listing 发布时的状态。

这与本仓 `live legacy rendering` 已建立的规则一致：

> **current account state ≠ historical account state**。

二手页面尤其要避免从“今天账号等级高”倒推出“当时卖家就是职业卖家”。

---

## 22. trust stack：线下旧货登记、校园身份与开放平台不是一个东西

可以暂时比较三种 trust stack：

### 22.1 旧货市场

```text
经营主体
+ 身份登记
+ 票据
+ 估价 / 检修 / 市场管理
```

### 22.2 校园 BBS

```text
学校共同体
+ BBS account
+ 校园地理
+ 线下面交
```

### 22.3 开放 classifieds

```text
platform account / listing
+ 电话 / QQ
+ 陌生人判断
+ 自行验货 / 面交
```

到更晚的平台，才会进一步增加：

- 支付担保；
- 评价；
- 鉴定；
- 仲裁。

本仓 2004–2009 的重点就是第二与第三种之间的变化。

---

## 23. “Web 交易”至少要分三层

### Level 1 — online discovery

网上看见信息。

### Level 2 — online negotiation / coordination

站内信、QQ、Email 等完成部分沟通。

### Level 3 — online transaction execution

付款、订单、物流状态、争议等真正被平台系统执行 / 记录。

2004–2009 很多校园二手和 classifieds 只能被可靠证明到 Level 1 或 2。

所以不能把：

> “网上看到二手信息”

直接改写成：

> “在线二手交易已经完成”。

---

## 24. 浏览器 / 编码条件

本篇目前没有足够原始 HTML capture 支持某个具体站点的浏览器 exclusivity 结论。

但后续若进入完整 case，应至少检查：

- GB2312 / GBK / UTF-8；
- IE6 下表格 / CSS；
- BBS 的 Web / Telnet 双入口；
- 图片 host；
- JavaScript 翻页 / 搜索；
- 登录 cookie；
- POST query；
- 联系方式是否用图片 / JS 隐藏；
- 城市子域名 / URL path。

硬边界：

> **modern Chromium renders page ≠ historical trading workflow reconstructed**。

---

## 25. 对 Wayback / Common Crawl 的具体查验建议

若下一轮追具体站点，建议先做最小化查验：

1. original host identity；
2. category URL pattern；
3. 至少两个 datetime；
4. 是否保存翻页；
5. listing detail 是否与 category 同时保存；
6. 图片 host 是否独立；
7. 联系方式是否可见；
8. listing 在后续 capture 是否变化 / 删除；
9. robots / login 是否造成系统性 gap；
10. 不访问 / 不公开不必要的普通个人敏感信息。

这比批量抓 listing 更符合本仓方法。

---

## 26. 隐私 stop condition

二手旧帖常包含：

- 手机号码；
- QQ 号；
- 宿舍楼；
- 姓名；
- 学校 / 班级；
- 面交地点。

即使 archive 仍可访问，本仓也不应批量重新公开。

本篇只研究：

- 页面结构；
- 渠道；
- 状态机；
- 公开同期报道中已经必要披露的抽象流程。

### 明确不做

- 不整理历史手机号数据集；
- 不批量提取普通学生 QQ；
- 不重新发布删除过的私人 listing；
- 不为了证明成交去寻找私人聊天记录；
- 不用泄露数据库补 account / transaction state。

---

## 27. 与 `how-people-lived` 的交叉接口

对应研究包：

`topics/secondhand-circulation-asset-reversibility-and-household-reset-china-1998-2025.zh-CN.md`

生活史侧关心：

- 毕业时为什么必须急卖；
- 一件物品能否重新变成现金；
- 搬家前能否快速腾空间；
- 失败项目的设备能否退出；
- 二手是否降低试一次新爱好的进入成本。

本仓只回答其中的旧网部分：

> **什么 artifact 能证明一个普通人当时拥有怎样的发布 / 搜索 / 联系界面，以及 archive 为什么看不到后面的真实交易。**

---

## 28. 已证实

1. 2004 同期媒体已记录高校 BBS 二手板的实际使用。
2. 至少一名同期学生明确把“多数用户来自本校”视为 BBS 交易信任优势。
3. 2005 高校二手流通真实地跨实体告示板、论坛、QQ、电话等渠道。
4. 2006 分类信息网站已经把二手物品作为普通城市生活分类之一。
5. 2007–2008 即使网络渠道存在，毕业清仓 / 宿舍面交 / 回收者仍继续承担实际交易。
6. 2009 有面向单一高校的专门跳蚤网站尝试。

---

## 29. 高概率但仍需 capture 验证

1. 校园 BBS 二手板的页面 / URL 结构可能比开放交易平台简单，因此主文本更容易被 archive 保存。
2. 图片、联系方式、搜索结果和 listing 后续状态的保存率很可能显著低于帖子正文。
3. 成功卖出的帖子更可能被删除 / 修改，因此 archive survivors 可能对未成交 / 未维护条目有偏差。
4. 同一商品可能在黑板、BBS、QQ 与 classifieds 重复发布，导致基于文本的数量统计高估独立 inventory。

这些目前属于 **D：方法推断**，除非进入具体 capture 样本后测量。

---

## 30. 不知道

1. 2004–2009 任一具体校园 BBS 中，listing 到成交的转化率是多少？
2. 平均一件商品要改几次价？
3. 有多少帖子成交后删除？
4. 有多少帖子长期僵尸化？
5. 电话 / QQ handoff 后实际取消率是多少？
6. 同城 classifieds 与校内 BBS 的最终成交价是否系统不同？
7. 2009 那个校园跳蚤网站的 historical original URL、多个 capture 和长期存活情况如何？
8. 58 早期二手分类的具体 URL / city host / pagination pattern 在 archive 中保存到什么程度？

---

## 31. 下一步：一个最小可复核 case

下一轮最值得做的不是扩大平台名单，而是选一个公开、隐私风险可控的 historical listing / board，寻找至少两个时点：

```text
T1: active listing
T2: price edited / sold / deleted / stale
```

理想证据组合：

```text
Wayback capture
+ 同期媒体 / 教程
+ category page
+ listing detail
```

要回答的不是“这个网站好不好用”，而是：

> **同一件旧物从公开网页上出现以后，我们最多能追到它走到交易状态机的哪一格？**

如果只能证明 listing，正式结论就停在 listing。

---

## 32. 参考入口与证据等级

| 来源 | 年份 | 等级 | 用途 |
|---|---:|---|---|
| 《旧货流通管理办法（试行）》 | 1998 | A | 前 Web 制度边界：信息、评估、结算、登记等已经存在 |
| 新浪教育校园 BBS 报道 | 2004 | B | 校园 BBS 二手板与同校信任 |
| 浙江农林大学保存《每日商报》 | 2005 | B | 黑板 / 论坛 / QQ / 电话多渠道二手环境 |
| 新浪科技 58 分类信息报道 | 2006 | B | 开放 classified / 二手分类存在 |
| 中国新闻网 / 搜狐毕业清仓 | 2007 | B | 线下回收 execution path 与 deadline |
| 中国新闻网 / 南昌晚报 | 2008 | B | 宿舍线下跳蚤市场 |
| 中国地质大学保存《长江商报》 | 2009 | B | 专门校园跳蚤网站 |

链接：

- <https://www.hengqin.gov.cn/lab/flfg/bmgz/content/post_3727256.html>
- <https://edu.sina.cn/sa/2004-02-19/detail-ikftssap7679469.d.html>
- <https://www.zafu.edu.cn/info/1012/61669.htm>
- <https://tech.sina.com.cn/i/2006-02-12/1519838495.shtml>
- <https://news.sohu.com/20070703/n250881882.shtml>
- <https://www.chinanews.com.cn/edu/dxxy/news/2008/11-28/1467177.shtml>
- <https://voice.cug.edu.cn/info/1006/7890.htm>

---

## 33. 本轮方法结论

二手旧网最容易犯的错误，是把一页 `出售 XX` 当成一笔交易。

应该始终写成：

```text
listing observed
≠ item still available
≠ buyer contacted
≠ negotiation completed
≠ agreed price known
≠ payment completed
≠ physical handoff completed
≠ dispute absent
```

而且：

```text
listing deleted
≠ sale completed
≠ sale failed
```

它可能只是：

- 卖掉了；
- 改主意；
- 过期；
- 平台清理；
- 账号删除；
- archive 没抓到。

这套边界应作为以后中文旧网 classifieds / 二手板 / 交易帖研究的默认 evidence contract。

---

*本笔记由 AI 辅助整理。所有个人信息均按研究必要最小化处理；未尝试恢复私人聊天、手机号、QQ 号或已删除 listing。*