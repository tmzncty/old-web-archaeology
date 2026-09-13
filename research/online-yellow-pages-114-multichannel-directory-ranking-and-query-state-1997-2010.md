# 网上黄页、114 与多通道目录：记录来源、排序状态和查询结果缺口，1997–2010

> 状态：research note，不构成 M1 完整案例
>
> 范围：中文互联网约 1997–2010 的网上黄页及其与纸质黄页、114 话务台、WAP、SMS、电话转接之间的关系。
>
> 交叉主题：`how-people-lived` 中的 service addressability / discoverability，以及普通人怎样在陌生城市找到现实服务。

---

## 0. 为什么这是 old-Web archaeology，而不只是电话史/广告史

网上黄页是一个很容易被后见之明误读的旧网对象。

今天看到一个 1998 年企业 listing，很容易顺手理解成：

> 这家企业当时已经“有网站/上网了”。

但实际可能完全不是这样。

企业的 Web 可见性可能来自：

- 电信号码数据库；
- 工商/机构名录；
- 黄页公司购买/交换的数据；
- 销售人员人工“扫街”；
- 企业电话登记；
- 广告销售；
- 第三方把纸质/后台记录发布成 Web 页面。

因此网上黄页是非常好的案例，用来区分：

```text
real-world entity
!= telephone subscriber record
!= directory database record
!= Web listing
!= query result
!= ranked result
!= actual call/service event
!= archive capture
```

---

## 1. 研究单位

本条目至少区分以下 12 层：

1. **business / institution**：现实中的商家或机构；
2. **telephone endpoint**：一个真实电话号码及其运营商归属；
3. **source record**：电信/工商/人工采集等原始记录；
4. **directory corpus**：黄页或 114 后台数据库中的实体记录；
5. **channel representation**：纸本、Web、WAP、SMS、话务台等具体表示；
6. **page / listing URL**：Web 上的某一企业/分类页面；
7. **query**：用户输入/说出的检索需求；
8. **query result set**：某一时刻返回的候选集合；
9. **ranking / priority state**：结果顺序、付费优先、人工推荐规则；
10. **contact transaction**：转接电话、短信返回号码、用户自行拨号；
11. **service event**：现实世界中是否真的订票、开锁、搬家、就餐等；
12. **archive capture**：历史档案保存的页面表示。

这些层不能互相替代。

尤其：

```text
listing exists
!= business itself had a website

business exists
!= visible in this directory

visible in directory
!= returned for this query

returned first
!= objectively best

captured listing
!= preserved search ranking
```

---

## 2. 1997–1998：ChinaBIG 证明“Web presence 可以由目录替实体生成”

### 2.1 已确认 historical identity / locator

1997 年 10 月 28 日《South China Morning Post》同期报道把 ChinaBIG 描述为 Internet-based directory，并给出：

- `www.chinabig.com`

报道称目录包含大量企业的电话、地址、电子邮件等信息。

1998 年 3 月 WIRED 的同期报道再次明确链接：

- `http://www.chinabig.com/`

并称 ChinaBIG 有约 200 万 business listings。

来源：

- SCMP, 1997-10-28, *Mainland guide lists two million phone numbers, addresses and e-mails*：https://www.scmp.com/article/216823/mainland-guide-lists-two-million-phone-numbers-addresses-and-e-mails
- WIRED, 1998-03-01, *China, Big Time*：https://www.wired.com/1998/03/neweconomy-9/

证据等级：**B，高置信**。

这两组来源来自不同媒体，可作为两个 evidence family。

### 2.2 不要把 200 万 listing 误读成 200 万企业“上网”

WIRED 同期报道一边记录 ChinaBIG 的大量企业记录，一边引用公司负责人说中国当时活跃 Web sites 的数量仍很少。

因此：

**`Web-visible entity != Web-using entity`**

这可以称为：

**`registry-mediated Web presence / 目录中介的 Web 可见性`**。

它是一种旧 Web 上非常重要但容易忽略的 artifact 类型：

> 页面由聚合平台生成，页面主体并不是页面作者，也不一定知道或控制页面的存在。

因此，未来抽样中文旧网站时，不能把“某企业在 ChinaBIG 上有 listing”计为“某企业拥有网站”。

---

## 3. 1997–2001：directory corpus 的 provenance 并不单一

2001 年《经济观察报》同期行业报道回顾 ChinaBIG 的电子黄页项目：

- 1996 年形成电子黄页构想；
- 1997 年与中国联通相关方合作并发布 `www.ChinaBIG.com`；
- 1999 年开始在北京、深圳、广州、上海运营；
- 号码资源取得并不自动，早期部分数据要由销售人员“扫街”获得。

来源：

- 《经济观察报》，2001-06-19（新浪保存）：https://tech.sina.com.cn/it/t/72064.shtml

证据等级：**B，中高置信**。

这里最值得 OWA 固化的是：

**`directory record provenance / 目录记录来源`**。

一条 listing 至少需要问：

- 是运营商用户表自动导入？
- 来自工商/政府数据？
- 商户主动登记？
- 广告客户创建？
- 销售人员人工收集？
- 从纸质黄页迁入？
- 多来源合并？

如果 provenance 不清，不能把 listing 字段当作“企业在该日期主动对公众发布的自我描述”。

---

## 4. 2001：同一 directory corpus 已经同时暴露给纸、Web、WAP、呼叫中心

2001 年《21世纪经济报道》采访上海黄页时明确称，上海黄页已经建立：

- 网上黄页；
- WAP 黄页；
- 呼叫中心；
- 传统纸本。

该报道还记录上海黄页向高校宿舍发纸本、讨论普通用户使用率，并称上海 1987 年底已开始出版黄页号簿。

来源：

- 《21世纪经济报道》，2001-06-06（新浪保存）：https://tech.sina.com.cn/it/t/69995.shtml

证据等级：**B，高置信**。

这要求 OWA 不把“网站”当成唯一研究单位。

更合适的模型是：

**`multi-channel directory corpus / 多通道目录语料库`**

```text
backend directory corpus
├─ print yellow pages
├─ telephone operator console
├─ Web search/listing
├─ WAP
└─ later SMS
```

一个 2001 Web capture 最多证明其中一个 channel representation。

它不能自动说明：

- 同时纸本里有哪些记录；
- 话务员能查到哪些字段；
- WAP 是否使用完全相同的数据库；
- 各渠道更新时间是否一致。

---

## 5. 2004：SMS 黄页进一步证明“Web 只是目录数据库的一种视图”

2004 年 7 月的同期报道记录，中国电信推出“短信版黄页”。用户把查询请求发到指定短信代码，可查询 10 个城市的公司地址、电话号码，也能通过电话号码反查公司名称；报道明确称服务依托中国电信黄页号码资源数据库。

来源：

- 《北京现代商报》，2004-07-01（新浪保存）：https://tech.sina.com.cn/it/t/2004-07-01/1514382127.shtml

证据等级：**B，高置信**。

因此一个历史 query 可能由：

```text
SMS text
→ parsing / lookup
→ backend directory corpus
→ SMS result
```

完成，而整个动作没有任何 Web 页面。

如果未来只按 URL 保存率衡量“数字黄页是否存在”，会系统性低估这类跨通道信息服务。

---

## 6. 2005–2006：`directory coverage != real-world coverage`

2006 年《齐鲁晚报》报道山东固定电话市场拆分后出现的查号问题：网通掌握的 114 无法直接提供部分铁通、电信用户号码；真实营业的酒店/公司因此可以在 114 中“查无此单位”。当地同时存在多个运营商自己的查号台。

来源：

- 《齐鲁晚报》，2006-03-20（新浪保存）：https://news.sina.com.cn/c/2006-03-20/07538480130s.shtml
- 《信息时报》，2005-08-30（新浪保存，广东跨运营商号码登记争议）：https://tech.sina.com.cn/t/2005-08-30/0717706378.shtml

证据等级：**B，高置信**。

这给 archive interpretation 增加一个关键边界：

**`absence from directory != absence from city`**。

一个 114 / 网上黄页数据库可能因为：

- 运营商边界；
- 数据交换失败；
- 商户未登记；
- 更新延迟；
- 收费策略；
- 数据采集范围；

而漏掉现实实体。

因此目录 capture 是**信息制度的可见世界**，不是现实城市实体全集。

---

## 7. 2006：从 exact lookup 到 fuzzy discovery，查询本身成为历史对象

2006 年“号码百事通”同期介绍使用一个很清楚的例子：

> 用户想吃某种饭，却不知道餐厅名字。

114 于是从“精确查号”扩展为“模糊查询”，后台按餐饮类型、价格、位置等组织信息；话务员可以给出地址、路线、候选餐馆，甚至转接/预订。

来源：

- 《今日早报》，2006-05-17（新浪保存）：https://news.sina.cn/sa/2006-05-17/detail-ikkntiam7065191.d.html
- 新华社，2006-03-06（新浪保存）：https://news.sina.com.cn/c/2006-03-07/08538379589s.shtml

证据等级：**B，高置信**。

这意味着 OWA 的单位不能停在 listing page。

至少还需要保存：

- query text / spoken intent；
- category mapping；
- location constraint；
- returned candidates；
- result order；
- operator intervention；
- whether result was read aloud, texted, or call-transferred。

本条目把这类缺失称为：

**`query-state gap / 查询状态缺口`**。

---

## 8. 人工话务员是一层无法被普通 Web archive 保存的 runtime

在“语音 Google”阶段，用户并不直接操作数据库。

真实事务链可能是：

```text
spoken request
→ human operator interprets intent
→ operator searches internal console
→ operator chooses / reads candidates
→ optional paid-priority rule
→ call transfer or SMS result
→ user contacts business
```

这个系统的关键 runtime 包含：

- 话务员培训和分类规则；
- 内部查询终端；
- 话务员看到的字段；
- 人工判断；
- 通话上下文；
- 当时的数据库状态。

即使公开网站完整保存，也不会保存这层 operator runtime。

因此可以把它记为：

**`operator-layer loss / 话务员层丢失`**。

这不是泛泛的“page != transaction”，而是明确指出历史服务的一部分从来就不在 public Web 上。

---

## 9. 2007：结果排序可以由付费优先决定，而静态 listing 无法恢复当时排名

2007 年《南方周末》调查报道记录了“优先报号权”：商户付费后，当用户做行业相关模糊查询时，114 可以优先报出其号码；多地甚至以竞拍方式出售优先位置。

报道中的一个同期第一人称案例是：一名上海上班族通过 114 找机票代理，平时使用的售票处没有被找到，话务员转接到一个被称为“号码百事通机票订购中心”的代理；后来她发现同航班邻座价格明显更低，也发现该代理与中国电信并非隶属关系，而是购买了优先报号。

来源：

- 《南方周末》，2007-11-22（搜狐保存）：https://business.sohu.com/20071122/n253422378.shtml

证据等级：**B，同时代调查报道；高置信于“这一商业机制和案例被当时媒体记录”，不外推全部查询。**

为了隐私最小化，本 note 不重复普通受访者姓名。

这给 OWA 提供了一个很具体的新状态：

**`ranking-state invisibility / 排序状态不可见`**。

一张企业 listing 的历史 capture 无法告诉我们：

- 用户搜“机票”时它排第几；
- 是否付费优先；
- 是否被话务员主动推荐；
- 同行业其他候选是否被隐藏/延后；
- 某个城市、某个日期的价格规则是什么。

因此：

**`captured listing != preserved discovery experience`**。

---

## 10. `search result` 本身比 listing 更脆弱

旧网考古经常优先寻找稳定 URL：企业详情页、帮助页、首页。

但对目录型服务而言，真正影响用户行动的可能是**瞬时查询结果页**：

```text
query + location + corpus_version + ranking_rule + paid_priority
→ result set at time t
```

这类页面往往：

- 参数化；
- 动态生成；
- 依赖后端数据库；
- 可能没有稳定 URL；
- 抓取器未必提交查询；
- capture 时后端可能已经失效；
- 同一个 URL 在不同时间返回不同结果。

因此未来做黄页/本地搜索 artifact 时，至少要分别寻找：

1. 首页/入口；
2. 分类页；
3. 企业 listing；
4. 查询表单；
5. query-result URL pattern；
6. 当时帮助页/广告说明；
7. 若可能，内部/营销材料解释排序和数据来源。

只恢复 listing page 不能叫“恢复本地搜索体验”。

---

## 11. 一个很重要的历史可见性偏差：聚合数据库可能比个人/小商家自己的 Web 留得更久

集中式目录有两个相反的保存效应。

### 11.1 它让原本没有网站的实体进入历史 Web

这是正向的 historical visibility：

- 一家没有主页的小饭馆；
- 一个只拥有固定电话的小企业；
- 一个从未自己发布网页的机构；

都可能在第三方 directory 中留下名字、地址、电话类别等痕迹。

### 11.2 但 archive 保存的是目录运营商的分类逻辑

它留下的不是商家“自己怎样描述自己”，而是：

- 黄页给它分到什么行业；
- 目录收集了什么字段；
- 哪个运营商拥有号码；
- 商家是否购买广告/优先；
- 数据多久更新一次。

因此目录 artifact 更适合回答：

> 当时的信息系统怎样让城市变得可查询？

不适合未经补证就回答：

> 这家商户当时如何理解自己的身份？

---

## 12. 与 2019 以后平台本地搜索的边界

OWA 的主 scope 保持约 1995–2015，因此本 note 不把微信、大众点评、小红书、现代 AI 本地搜索扩展成新的主研究对象。

这里只保留一个边界说明：2019 年微信测试“附近的餐厅”时，已经把地址、电话、距离之外的朋友“想去/去过”、用户印象和推荐一起放进本地发现。

来源：

- 36氪，2019-01-04（搜狐保存）：https://www.sohu.com/a/286602321_114778
- IT之家，2019-01-07：https://www.ithome.com/0/404/296.htm

这说明 1997–2007 的 directory/ranking 问题后来并没有消失，而是进入更复杂的 reputation/social/recommender system。

但后续历史主要写回 `how-people-lived`，不让 OWA scope 无限向今天扩展。

---

## 13. 海外对照只作为方法参照：法国 Minitel

本仓不改成全球旧网仓库，但海外对象可以帮助判断“Web 是否唯一演化路径”。

法国 1980s 的 Minitel 特别适合做方法参照：1987 年同期学术文章记载，Ille-et-Vilaine 的主要试点最初只提供 Electronic Telephone Directory；Minitel 直接接普通电话插口。1995 年学术研究则记录 Teletel 已有约 650 万终端和大量信息/通信/商业服务。

来源：

- Jean-Marie Charon, 1987：https://journals.sagepub.com/doi/10.1177/016344387009003004
- Charles Steinfield et al., 1995：https://onlinelibrary.wiley.com/doi/full/10.1111/j.1083-6101.1995.tb00168.x

这里的用途只有一个：证明**电子目录、家庭终端和数字服务发现可以早于 Web 普及**。

全球前史和普通生活比较写入 HPL；OWA 仍以中文 1995–2015 对象为主。

---

## 14. 本轮 artifact probe

### 14.1 已确认 historical locators

两个独立同时代来源确认：

- `http://www.chinabig.com/` — 1997/1998；
- `ChinaBIG.com.cn` — 2001 同期行业报道中出现。

WIRED 1998 页面目前仍保留指向 `www.chinabig.com` 的原始外链。

### 14.2 当前 direct-fetch 状态

本轮尝试直接访问：

- `https://www.chinabig.com/`
- `https://www.chinabig.com.cn/`

当前均未取得可解释的 historical content；请求返回网关错误/无法正常取得正文。

这只能说明**当前 direct Web 入口不可用于历史核验**，不能写成“域名历史上不存在”或“archive 没保存”。

### 14.3 archive probe 负结果

本轮进行了：

- 搜索引擎中的精确域名 + Wayback 查询；
- Internet Archive / Wayback 入口检查；
- 1997–2002 `chinabig.com` / `chinabig.com.cn` capture locator 尝试；
- 执行环境中的 CDX 直接请求尝试。

结果：

- Wayback 主站入口可访问；
- 搜索没有返回一个可直接核验的 ChinaBIG historical memento；
- 本轮没有成功打开一个带明确 `capture_datetime`、historical HTTP/replay state、DOM、charset、subresources 的 ChinaBIG capture；
- CDX 直接查询在本轮执行环境中遇到 DNS 解析失败。

因此准确措辞只能是：

**`verified historical memento: NOT achieved in this run`**

不能写成：

**`Wayback did not preserve ChinaBIG`**。

---

## 15. 浏览器 / 编码 / runtime：目前知道什么，不知道什么

### 已知

- 1997–1998 已有公开 Web directory；
- 2001 上海黄页有 Web + WAP + call center；
- 2004 有 SMS query；
- 2006 114 有人工模糊查询/短信回送/电话转接等能力。

### 不知道

本轮未取得原始 historical Web capture，因此不能可靠确定：

- ChinaBIG 1997 首页的 charset；
- frames/table/CSS/JS 结构；
- 是否需要 IE/Netscape 特定行为；
- query 参数与结果 URL pattern；
- 搜索是否由 server-side CGI / ASP 等实现；
- 结果页是否被 archive 抓取；
- 图片/广告/分类图标缺失程度；
- 2001 `ChinaBIG.com.cn` 与 `.com` 的站点/系统关系在具体页面层面如何变化。

这些都不能靠“1990s 中文网站大概是 GB2312 + table”来补。

---

## 16. 证据等级

### A

本轮没有拿到 ChinaBIG 原始 WARC/HTML，也没有取得 1997–2001 已核验 memento。

可作为实体前史辅助的机构书目：日本国立国会图书馆保存《中国电话号簿 / 中国大黄页》1996 起的书目记录，但它证明的是纸质出版物存在，不是 Web runtime。

### B

- 1997 SCMP；
- 1998 WIRED；
- 2001《21世纪经济报道》；
- 2001《经济观察报》；
- 2004 短信黄页同期报道；
- 2005–2007 114 数据覆盖、模糊查询、优先报号的同期报道。

### C

- 后来的 114 周年史只用于 1980s/1990s chronology lead；
- 不用它替代 1997–2007 的同期材料。

### D

以下是本研究包提出的分析概念：

- `registry-mediated Web presence`；
- `multi-channel directory corpus`；
- `query-state gap`；
- `operator-layer loss`；
- `ranking-state invisibility`。

它们不是历史行动者原词。

---

## 17. 反例与后见之明风险

### 17.1 不要把 directory record 当 homepage

企业 listing 的主体未必参与页面制作。

### 17.2 不要把 large listing count 当 Internet adoption count

200 万企业 listing 和 200 万企业主动联网完全不是一个指标。

### 17.3 不要把“114 查不到”写成实体不存在

运营商数据库分裂提供了明确反例。

### 17.4 不要把排序理解成自然质量排序

2007 的优先报号表明结果第一名可能是商业规则产物。

### 17.5 不要用今天搜索引擎概念覆盖人工话务员

话务员确实完成 intent interpretation，但人类中介、电话交互、数据库权限和付费规则都不同于现代算法搜索。

### 17.6 不要把 current live page 当 historical page

本轮甚至没有取得一个可用 current ChinaBIG page，更不能以今天页面形态替 1997/2001 页面。

---

## 18. 下一步最值得做什么

1. 从 Internet Archive、Common Crawl、其他 web archive 重新取得并实际打开 ≥2 个 ChinaBIG historical captures；
2. 对每个 capture 记录 original URL / capture URL / datetime / HTTP / charset / DOM / subresources；
3. 寻找历史 ChinaBIG 查询 URL pattern，而不是只找首页；
4. 找 1999–2004 上海网上黄页 / 中国电信黄页的实际页面 artifact；
5. 找 WAP 黄页或 SMS 黄页的用户说明、操作手册、短信格式；
6. 找 114 话务员内部终端截图/培训资料/业务手册，恢复 operator-layer schema；
7. 找“优先报号”合同/资费/排序规则原件，确认 ranking state 的可观察字段；
8. 建立一个小型 schema，允许同一 directory record 关联 print/Web/WAP/SMS/voice 多个 representations。

---

## 19. 对 M1 / ROADMAP 的状态

这份 note **不是** ROADMAP M1 的三个完整案例之一。

它没有：

- ≥2 个已打开核验的历史 timepoint；
- 完整资源缺失清单基于真实 capture；
- 浏览器/编码验证；
- historical runtime replay。

因此不应升级成“完整考古案例”。

它当前的价值主要是：

1. 为 M2 平台形态谱系补一个“目录/数据库型 Web presence”边界对象；
2. 给后续 M3/M4 提供 query-result、operator layer、ranking state 这些普通静态网页研究容易遗漏的缺失维度。

当前准确状态：

```text
historical entity identity: achieved
historical locators: achieved
contemporaneous workflow evidence: achieved
cross-channel evidence: achieved
query/ranking-state model: achieved
verified historical memento: NOT achieved
second verified historical timepoint: NOT achieved
runtime replay: NOT achieved
```

---

## 20. 与 how-people-lived 的交叉

对应 HPL 研究包：

`tmzncty/how-people-lived/sources/from-114-directory-assistance-to-local-platform-search-service-addressability-and-discoverability-china-1982-2025.zh-CN.md`

HPL 的结论是：服务存在不等于普通人能发现它；从 114 到本地平台，信息基础设施不断改变“城市里有哪些机会真正进入一个人的可行动范围”。

OWA 的结论则更窄：**旧 Web 上的一张企业页面只是一层 representation；真正塑造发现过程的 corpus、query、operator、ranking 和 channel state 往往没有被页面一起保存。**
