# CLASSIFIED LISTING / CITY / CATEGORY / CONTACT / RANKING / VERIFICATION / REAL-WORLD OUTCOME STATE GAPS（2005–2015）

> Scope：中文互联网约 2005–2015 年的生活分类信息、招聘/家政/搬家等本地 listing 界面，以及这些公开页面与现实交易/劳动之间的状态差。
>
> 本文件**不是** 58 同城或赶集网的公司史，也不把全球 Craigslist / Minitel 写进本仓主对象。海外材料仅作为比较机制；前互联网与跨国生活史详见 `tmzncty/how-people-lived` 配套专题。

## 0. 为什么这个对象值得单独做 old-web archaeology

旧网研究很容易保存“内容页”，却忽略一种更短命、更高度依赖现实状态的页面：**classified listing**。

一条 2009 年的帖子可能只在几小时或几天内有价值：

- 房间已经租掉；
- 临时工已经招满；
- 搬家车今天有空、明天没有；
- 电话号码换了；
- 发布者删帖；
- 商户重新 refresh；
- 付费排序改变位置；
- 平台判断它重复、过期或违规；
- 用户从页面跳到电话/QQ，真实交易从此离开 Web。

因此 classifieds 的核心历史对象不是“一张页面截图”，而是：

> **某个时刻，一个本地需求怎样被编码成可搜索记录，又怎样（或没有怎样）进入现实生活。**

## 1. 研究对象必须拆开

不要把以下对象合并：

1. `platform` — 生活分类信息平台；
2. `host / city site` — 某一城市入口；
3. `neighborhood / locality selector` — 区域过滤；
4. `category` — 房屋、招聘、二手、黄页、本地服务等；
5. `subcategory` — 合租、兼职、搬家、保洁等；
6. `user account`；
7. `merchant account`；
8. `merchant certification state`；
9. `listing record`；
10. `listing revision`；
11. `listing status` — active / expired / removed / filled / unknown；
12. `listing rank / placement`；
13. `priority placement purchase`；
14. `realtime-bid state`；
15. `search query`；
16. `search result page`；
17. `listing landing page`；
18. `phone number / SMS endpoint`；
19. `platform IM identity`；
20. `off-platform QQ / later WeChat contact`；
21. `physical address`；
22. `interview / service appointment`；
23. `contracting entity`；
24. `payment recipient`；
25. `actual labor demander / service consumer`；
26. `real-world outcome`；
27. `complaint / moderation record`；
28. `archive capture`。

即使一个 capture 同时显示其中若干层，也不能把它们视为同一权威状态。

## 2. 核心 state gaps

### 2.1 existence gaps

```text
real-world need exists
!= listing drafted
!= listing submitted
!= platform accepted
!= listing publicly visible
!= listing indexed in category/search
```

### 2.2 freshness gaps

```text
listing publicly visible
!= opportunity still open
!= phone still reachable
!= price/wage still current
!= quantity/slots still available
```

一条 archive capture 最多能证明“该页面在 capture 时返回了某种表示”，不能证明现实需求仍有效。

### 2.3 locality gaps

```text
city selected
!= poster physically in that city
!= employer/service provider registered in that city
!= work/service performed there
```

2013 年 58.com F-1 明确说明平台以约 380 个 city websites 为入口，并可继续筛选 neighborhood；但 2024 年调查又能看到“上海岗位”由外省注册主体发布。

因此“城市站”首先是**信息组织字段**，不能自动等于法律主体所在地或现实服务地点。

### 2.4 identity gaps

```text
registered account
!= verified individual
!= verified merchant
!= actual contact person
!= actual employer / service provider
```

### 2.5 certification gaps

```text
merchant passed platform certification
!= every listing is accurate
!= contact person is authorized
!= future transaction is guaranteed
```

认证本身是历史对象，不能被研究者升级为结果担保。

### 2.6 contact gaps

```text
phone shown
!= call placed
!= call answered
!= same person answered
!= terms confirmed
!= appointment made
```

移动 Web/App 的 direct-dial 功能进一步压缩了 page → phone 的步骤，但也让真实执行更快离开可公开保存的 Web 层。

### 2.7 job gaps

```text
job listing exists
!= vacancy exists
!= employer is poster
!= interview exists
!= interview terms match listing
!= worker starts work
!= hours match promise
!= wage owed
!= wage paid
```

### 2.8 service gaps

```text
merchant page exists
!= service available now
!= quoted price executable
!= worker arrives
!= service completed
!= consumer accepts result
```

### 2.9 ranking gaps

```text
listing exists
!= listing is visible near top
!= top position is organic
!= ranking is stable across users/time
```

2013 58.com F-1 明确记载 priority listing 与 real-time bidding；付费商户可按类别和地点竞价更显眼位置。

所以历史截图里的“第一个结果”不能默认解释为：

- 最相关；
- 最近；
- 最受欢迎；
- 真实供给最多；
- 平台自然排序。

它可能是购买的数字摊位位置。

### 2.10 archive gaps

```text
listing URL captured
!= category page captured
!= ranking context captured
!= phone/IM action captured
!= linked images captured
!= later deletion/expiry captured
!= real-world outcome captured
```

## 3. 2013 58.com F-1：一个同期的平台结构锚点

58.com 2013-09-27 向美国 SEC 提交的 Form F-1 是当前 slice 最有价值的 A 级结构材料之一。

原件：

- https://www.sec.gov/Archives/edgar/data/1525494/000104746913009364/a2216693zf-1.htm

### 3.1 A 级可直接支持的产品结构

F-1 明确说明：

- 用户可不注册直接 browse/search listing；注册后才可发布并使用更多通信工具；
- 平台内容按城市、进一步按 neighborhood、类别和子类别组织；
- 主要分类包括住房、工作、二手、汽车、宠物、票务、yellow pages 与本地服务；
- jobs 包含销售、技能工、餐饮、配送、homecare/cleaning 等；
- listing page 展示多条概要，点击后进入更详细 landing page；
- 移动入口同时包含 Android/iOS application、smartphone browser-adapted application 和功能机 WAP；
- 移动端可 direct dial listing 上的电话，也可短信或使用即时通信；
- 付费商户有 certification、online storefront、priority listing 等服务；
- real-time bidding 可以竞争特定 category + location 的显眼位置；
- 认证商户需要提交营业执照等材料，平台称会与第三方数据库核对。

### 3.2 这份材料不能支持什么

不能仅凭 F-1 写：

- “2013 年普通中国人都通过 58 找工作/房子”；
- “平台认证信息都真实”；
- “56.4 million monthly listings 就是 56.4 million 个独立真实机会”；
- “用户数/市场份额数据是独立第三方无利益关系统计”；
- “WAP 已覆盖所有功能机用户”；
- “商户说当日收到电话，所以一般商户都如此”。

公司在监管申报里对自身业务的陈述是 A 级 contemporaneous platform evidence；其中引用的委托行业报告、公司选择的 merchant examples 仍必须单独降权。

## 4. 58 的历史结构说明：Internet 没有消灭 locality

F-1 描述的典型信息路径：

```text
platform
→ select city
→ select neighborhood
→ category
→ subcategory
→ parameters/filter
→ listing page
→ landing page
→ phone / SMS / IM / later transaction
```

这是一个非常重要的 old-Web 结论：

> 分类信息并不是“无地点网络”。它把地理位置从必须身体进入的市场，转写成 URL / city selector / neighborhood field / query parameter 等数字结构。

因此未来 M1 capture 若获得，应重点保存：

- city host/path；
- city selector；
- neighborhood selector；
- category hierarchy；
- filter parameters；
- result count / pagination；
- listing timestamp；
- phone reveal/communication mechanism；
- paid/promotion markers；
- charset/content type；
- desktop/WAP differences。

## 5. WAP 不是脚注

F-1 到 2013 年仍明确写出功能机 WAP application，与 smartphone browser 和原生 App 并列。

这意味着中文旧网研究如果只保存桌面站，会系统性遗漏一种真实入口。

需要区分：

```text
desktop city site
!= smartphone browser-adapted site
!= WAP feature-phone site
!= Android/iOS app
```

未来不得根据桌面 HTML 推断 WAP：

- 同一 listing 是否同 ID；
- 电话号码是否完整显示；
- 图片是否加载；
- 搜索参数是否一致；
- 登录/验证码是否相同；
- 是否存在独立 host；
- charset 是否一致。

没有 historical capture 就保持 unknown。

## 6. ranking-as-market-place：页面排名是一种可购买的空间

F-1 记载：

- paying member 有 preferential listing benefits；
- priority listing 可把信息放在普通付费会员 listing 之上；
- real-time bidding 可以按具体分类和地点竞价第二天的显眼 placement；
- placement duration 可以从数小时到数天或数周。

这把一个传统分类广告问题重新带回 Web：

```text
物理市场入口/报纸醒目栏位
→ 数字页面顶部
```

对历史研究尤其危险，因为 archive 常常只给一个时间点。

### 6.1 capture 必须问

- 当时是否登录？
- query/location/category 是什么？
- result order 是什么？
- 是否有“推广/置顶/竞价”标识？
- capture 是首页、分类页还是 landing page？
- listing 的发布时间与 capture 时间相差多久？
- 同一 URL 第二天排序是否变化？

### 6.2 不要把 archived rank 当长期地位

某 listing 在一个 Memento 里排第一，只能证明：

> 这个 representation 在那个 capture 时刻把它放在那里。

不能直接写“它是最受欢迎商户”。

## 7. 2010 同期用户材料：listing 可能直接改变家庭空间使用

2010-10-19 金羊网/搜狐报道记录孙小姐因为租金上涨，在 58 同城发布“出租两居室客厅一间”，并在电话采访里说此举是为了减轻租金压力。

来源：

- https://news.sohu.com/20101019/n276017211.shtml

**证据等级：B/T1。**

它对 old-Web 的意义不是证明 58 普及率，而是说明：

```text
Web listing
→ 陌生合租者可被寻找
→ 一套住房的内部空间可以重新分类
```

历史 capture 若只剩标题“客厅出租”，仍无法证明：

- 最后有没有租出去；
- 谁入住；
- 实际租金；
- 联系发生在站内还是电话；
- listing 保留了多久；
- 页面删除是因为成交、过期还是人工撤销。

这就是 `listing text survival / outcome loss`。

## 8. 2024 调查用作 later-state counterexample：公开 listing 与责任主体可以彻底分裂

虽然 2024 超出本仓主时间范围，但它可以作为**后续系统状态的反例**，帮助我们避免错误理解 2005–2015 的 archived listing。

《上观新闻》/澎湃的调查路径显示：

```text
平台兼职 listing
→ 用户留下联系方式
→ 微信联系人
→ 线下面试地址
→ 收款二维码主体 A
→ 协议签约主体 B
→ 朋友圈再次发布的下游工作
→ 另一组实际招工联系人
```

来源：

- https://www.thepaper.cn/newsDetail_forward_26882627

报道中平台发布者、通知面试者、收款方、签约方和真实下游招工者出现分离；当地执法人员也把这种主体切割描述为固定证据和认定责任的难点。

**证据等级：B/T1，作为 2024 later-state comparison，不得反投射为 2010 平台的一般状态。**

它对 old-Web 的方法意义是：

> 即使我们今天完整恢复一条 2010 recruitment listing，也不能默认页面里的公司名就是最终劳动关系、收款或工资责任主体。

## 9. contact-channel escape / 联络链逃逸

分类信息天然鼓励 Web → 非 Web 的 handoff。

2013 F-1 的产品设计本身已经支持：

- phone；
- SMS；
- instant messaging；
- mobile direct-dial。

因此 archive 保存偏差不是偶然，而是系统结构决定的：

```text
公开 listing 容易被 crawler 看见
→ 用户下一步电话最难被公共 archive 保存
→ 线下会面完全离开 Web
→ outcome 几乎天然不可见
```

这与电商订单不同：classified marketplace 很多时候只负责“让双方找到彼此”，不是 transaction authority。

## 10. listing-shell survival / market-state loss asymmetry

### 10.1 最容易存活

- platform logo；
- category name；
- listing title；
- description；
- displayed price/wage；
- displayed location；
- poster nickname/company name；
- public timestamp；
- static image（若抓到）。

### 10.2 最容易消失

- 当时的搜索排序；
- listing 是否已招满/已成交；
- phone reveal 行为；
- IM 对话；
- 当时真实 caller 数；
- refresh/竞价 placement history；
- 删除原因；
- 实际见面；
- 实际工作内容；
- 工时；
- 实际工资；
- 支付；
- 纠纷与退款；
- 同一个机会被几层中介转发。

因此 classifieds 比博客更强烈地存在：

> **页面内容可以存活，市场状态却已经死掉。**

## 11. freshness paradox / 新鲜度悖论

分类信息对用户最重要的属性往往正是 archive 最难表达的属性：**新鲜度**。

一个旧网页现在“还能打开”，不意味着它当年长期有效。

研究字段至少应有：

```yaml
listing_published_at: known/unknown
capture_datetime: exact/approx/unknown
listing_status_at_capture: active/expired/removed/unknown
last_refresh_visible: yes/no/unknown
paid_placement_visible: yes/no/unknown
real_world_outcome: known/unknown
```

如果只有一个 capture，不得推断有效期。

## 12. duplication / syndication gap

F-1 还说明平台在某些无需认证的分类中会从其他网站选择并复制 classified information listings。

这引出另一个 archive 风险：

```text
same wording on site A + site B
!= two independent offers
```

未来需要记录：

- 是否为原发；
- 是否平台抓取/复制；
- 是否同一中介重复发；
- 是否相同电话/地址；
- 是否只是站群/城市镜像。

否则“多个 URL 交叉确认”会虚假抬高 evidence count。

## 13. certification / trust-score gap

2013 F-1 记载 paying merchants 的 mandatory certification，以及 trust rating / user review / fraud report 等机制。

但研究上必须保留：

```text
ID/business-license verified
!= listing fact verified
!= worker identity verified
!= every future transaction verified
```

认证图标本身是重要的 interface artifact：

- 图标长什么样；
- hover/click 是否解释认证类型；
- 是否个人/企业不同；
- 认证何时失效；
- listing 是否继承账户认证；

这些必须由 historical capture/帮助页验证，不能靠现代页面回推。

## 14. 个人隐私边界

classified archaeology 比一般门户页更容易碰到私人信息：

- 手机号；
- 住址/小区/门牌；
- QQ；
- 求职简历；
- 姓名；
- 照片；
- 家庭组成；
- 工资需求。

因此本仓默认：

- 不批量重新公开 ordinary-user phone number；
- 不为了证明“帖子真实”复制完整简历；
- 房屋/合租案例只保留支持 claim 所需的最小位置粒度；
- 已删除个人 listing 即使 archive 可见，也先判断研究必要性；
- 技术研究优先抽象 URL pattern 与字段，而不是制作可反查个人的数据库。

历史完整性不高于普通人的隐私。

## 15. Browser / charset / client assumptions

当前 slice **没有获得可核验的 2005–2010 58/赶集 historical M1 capture**，因此以下均保持 unknown：

- 2006/2008 首页实际 charset；
- 是否要求 IE 特定能力；
- JS 是否用于城市选择；
- phone 是否图片/文本/点击后显示；
- city site 是 subdomain 还是 path 的具体年份变化；
- WAP host/path；
- listing form 的 method/action；
- 验证码实现；
- CSS/表格布局；
- 动态分页；
- 登录 cookie 行为。

**禁止**根据“2000s 中文网站通常如此”自动填 `GB2312 + IE6 + table layout`。

## 16. Archive attempt log（本 slice）

### 已检查

- 搜索引擎中针对 `58.com` / `ganji.com` + Wayback / 2006 / 2008 的公开 locator；
- 58.com 2013 F-1 对历史平台结构的同期描述；
- 2006、2010 的同期媒体页面；
- 当前 Web 搜索能发现的 58 页面，仅用于确认品牌/URL 当前状态，不用作旧页面证据。

### 结果

**M1 verified historical Chinese classifieds capture: NOT ACHIEVED IN THIS SLICE.**

当前没有一份已经实际检查且同时记录下列字段的 capture：

- exact `original_url`；
- `capture_url`；
- `capture_datetime`；
- HTTP/replay state；
- charset/content type；
- DOM / form / search result structure；
- subresource survival；
- phone/IM action；
- second historical time point。

### 这不意味着

- Wayback 没有 capture；
- 当时没有该页面；
- 页面无法恢复。

只意味着：**本 slice 没有达到仓库 METHOD 的 M1 验证门槛。**

## 17. 证据等级摘要

| Evidence | Date | Grade | Supports | Does not support |
|---|---:|---|---|---|
| 58.com SEC Form F-1 | 2013-09-27 | A | 城市/街区/分类、Web/WAP/App、注册/发布、通信、认证、排名商业机制 | 普通人口采用率、每条 listing 真实性、2005 页面外观 |
| 金羊网/搜狐 ordinary-user renting case | 2010-10-19 | B/T1 | 一个真实受访者如何把住房空间发布为 classified listing | 平台总体成交率 |
| 2006 IT时代周刊分类信息报道 | 2006 | B | 当时分类信息网站作为 Web 2.0/投资热点被讨论 | 具体用户日常采用率 |
| 2024 上观/澎湃 investigation | 2024 | B/T1 later comparison | listing→微信→线下→多主体的责任碎片化可能性 | 不可反投射为 2010 普遍状态 |
| Craigslist / Minitel comparisons | 1986–2004 | external B/C | 跨国机制比较 | 不写入中文旧网平台谱系本体 |

## 18. 与 how-people-lived 的交叉接口

配套生活史问题：

- 本地机会什么时候从“必须认识人/必须站在市场里”变成可搜索？
- 一份零工能不能成为两份长期工作之间的 holding state？
- 主业 + 零工是不是并存，而不是两个互斥身份？
- 分类信息如何让合租、搬家、家政、维修和短工成为同一种“本地匹配”基础设施？
- 信息可见后，真实性/责任/支付是否成为新的执行瓶颈？
- 为什么 2020s 又出现数字平台 + 物理零工市场的混合结构？

参见：

- https://github.com/tmzncty/how-people-lived/blob/main/topics/from-labor-service-companies-to-online-classifieds-odd-jobs-and-local-opportunity-addressability-china-1979-2026.zh-CN.md

## 19. 下一步 M1 优先对象

### Candidate A — 58 city + jobs/listing pair, c. 2008–2010

理想 evidence package：

1. city homepage capture；
2. jobs category capture；
3. one ordinary listing landing page；
4. same URL or same category second date；
5. contemporary help/tutorial page；
6. phone/IM behavior evidence；
7. browser/charset note。

### Candidate B — Ganji city classifieds, c. 2008–2010

用来避免只把 58 一个平台当中国分类信息的全部历史。

### Candidate C — WAP/mobile classifieds, c. 2010–2013

优先回答：

- 功能机是否能直接浏览/搜索；
- 联系方式如何展示；
- 是否需要登录；
- 与 desktop listing ID 是否对应；
- 图片/分页/字符集如何处理。

## 20. 本轮 old-Web 结论

生活分类信息是一个特别容易被 archive 误读的对象。

博客文章的价值通常在“正文说了什么”；classified listing 的价值却往往在：

> **它现在还有效吗？谁会先看到？这个电话还通吗？见面以后还是这个条件吗？**

这些恰恰都是动态状态。

所以几十年以后，我们可能拥有一张非常完整的“兼职招聘”HTML，却仍然不知道那份工作有没有存在过；也可能看到一条已经成交的合租信息，却因为只有一个 capture，把它误解成长期供应。

更进一步，分类网站并没有把现实市场搬进页面以后就结束了。它只完成了最前面的一步：**让陌生人的本地需求变得可寻址。**

真正的生活随后会逃出页面，进入电话、即时通信、楼下、办公室、工地和工资结算。

因此本仓未来若要复原 classifieds，不能以“页面看起来恢复了”为终点。至少要明确标出：

```text
publicly archived information state
≠ real-world market state
```

这条不等式本身，就是这个旧网对象最重要的考古结论。

---

*Initial research note prepared with AI assistance. It intentionally records capture failure and state uncertainty rather than reconstructing unverified historical interfaces.*