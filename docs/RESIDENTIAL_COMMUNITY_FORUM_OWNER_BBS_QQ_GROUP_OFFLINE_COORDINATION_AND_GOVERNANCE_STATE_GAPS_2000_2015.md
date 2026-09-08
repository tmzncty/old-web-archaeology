# 中文住宅社区论坛、业主 BBS、QQ群与线下协调状态缺口（2000–2015）

## Scope

本专题只研究约 2000–2015 中文互联网中的住宅社区/楼盘/业主论坛及其与 QQ 群、早期微信群、线下业主行动之间的接口。

它不是中国社区治理通史，也不把 `old-web-archaeology` 扩展成全球社区网络史。1989 Santa Monica PEN、1993 Blacksburg Electronic Village 等海外对象只在 companion `how-people-lived` 中作为前史/比较；本文件主体保持中文旧网 scope。

本轮研究对象包括：

- 搜房/房天下式楼盘业主论坛；
- 独立住宅社区网站，如“家住天通苑”相关谱系；
- 房产门户里的小区板块；
- 论坛向 QQ 群、微信群和线下活动的 handoff；
- 帖子、账号、楼盘名、业主身份、业委会权限、物业响应和现实执行之间的状态缺口；
- 旧论坛消失、当前 legacy page 与历史 capture 的差异。

核心提醒：

> `forum visible != resident verified != homeowner verified != collective decision != offline execution`。

---

## 1. Why this is an old-Web object, not merely a housing topic

2000s 中文商品房小区非常适合旧网考古，因为论坛页面把多个原本分离的层叠到一起：

```text
楼盘/小区名称
→ 房产门户中的固定板块
→ 用户名/版主
→ 帖子与回复
→ QQ/MSN/电话等站外联系方式
→ 线下见面、团购、班车、签名、业委会、物业交涉
```

网页只是链条的一段。

同期材料已经显示，论坛会用于装修团购、停车费比较、物业打分、维权基金、社区活动、交通组织、媒体报料；但这些行为的最终状态通常不在同一个数据库里。

因此这个 case 的主要价值不是“证明中国曾经有业主论坛”，而是建立一套以后能复核的 **residential coordination transaction model**。

---

## 2. 同时代锚点：2006–2009 业主论坛已经是新建小区的重要电子入口

### 2.1 大连：论坛首页同时承担通知、征集、物业意见和活动

2006 年《半岛晨报》报道，大连当时已有 200 多个网上业主论坛，页面常见物业通知、足球队征集、物业满意度调查等内容。报道同时提醒，论坛增进邻里联系但也带来争吵等问题。

Source family B：
- 《论坛大开骂戒 众声怒讨物业》，2006-12-20，搜狐转载《半岛晨报》
- https://news.sohu.com/20061220/n247150685.shtml

能支持：
- 2006 年同期媒体确实观察到多个大连小区论坛；
- 论坛用于多种住宅事务；
- 冲突与邻里联系同时存在。

不能支持：
- “大连几乎所有业主都使用论坛”；
- “200 多个”都是活跃、独立或身份核验严格的社区；
- 论坛导致物业问题解决。

### 2.2 上海：2007 年公共机构开始把业主论坛视为可观察民意来源

2007 年上海一项政协提案的同期报道指出，越来越多新建小区居民使用以小区命名的业主论坛；提案调研特别提到搜房网和上海热线房产频道。报道转述的访问量与论坛数量属于调研/平台尺度数据，需要作为一个 evidence family 使用，不能当独立 census。

Sources B：
- 《小区“版主”应优先进入业委会》，2007-01-28
  https://news.sohu.com/20070128/n247886063.shtml
- 《“业主论坛”渴望倾听》，2007-04-08
  https://news.sohu.com/20070408/n249279417.shtml

这组材料的历史意义在于：论坛的角色已从“居民自己聊”扩展到“政府/媒体考虑是否应该听”。

但必须固定：

> `forum traffic != representative public opinion`。

版主也不能因为拥有线上声望就自动取得法定业委会权力。

---

## 3. Account state：论坛账号不是“业主”布尔值

住宅论坛最危险的历史误读之一，是把发帖账号自动解释为该小区产权人。

至少应拆成：

```text
ACCOUNT_CREATED
↓
EMAIL/PHONE VERIFIED?            unknown / yes / no
↓
SELF_CLAIMS_PROPERTY?            yes / no
↓
PROPERTY_UNIT DISCLOSED?         yes / no
↓
PROPERTY DOCUMENT VERIFIED?      yes / no / not supported
↓
CURRENT OCCUPANCY?               owner-occupier / landlord / tenant / pre-handover / unknown
↓
HOUSEHOLD ROLE?                  title holder / spouse / parent / child / other
```

同期反例非常强。2008 年济南一名新房主在业主论坛进入 QQ 群并登记资料后，遭大量装修营销电话；报道说有装修公司会注册论坛账号、伪装成业主获取信息。

Source B：
- 《装修电话“狂轰”新房主》，2008-01-11
  https://news.sina.com.cn/c/2008-01-11/021213236649s.shtml

因此：

> `account in owner forum != homeowner`。

历史研究中用户名、房号、产权身份必须分别记录，不允许从版块名称推身份。

---

## 4. Thread lifecycle：帖子存在，不等于它一直代表当前事实

建议把住宅论坛帖子至少拆为：

```text
THREAD_CREATED
→ MODERATED/PINNED?
→ REPLIES_ACCUMULATE
→ CONTACT_HANDOFF? (QQ/MSN/phone/email)
→ OFFLINE_ACTION?
→ OUTCOME?
→ THREAD_EDITED/DELETED/LOCKED?
→ BOARD_MIGRATED?
→ CURRENT_LEGACY_RENDERING?
→ HISTORICAL_CAPTURE?
```

特别需要防止：

- 旧帖子仍能打开，于是默认它当年的楼盘状态仍有效；
- 当前模板显示某个按钮，于是默认历史时点已有这个功能；
- 帖子里写“大家都同意”，于是默认存在有效投票；
- 帖子里写“物业答应”，于是默认维修完成。

---

## 5. 论坛 → 站外即时通信：旧 Web 的真实生活路径经常主动离开 Web

### 5.1 2008：论坛发现，MSN 报名，线下见面

2008 年上海一名即将收房业主从小区论坛看到装修“团装”信息，再通过 MSN 报名，最后乘大巴去看样板房并线下谈装修。

Source B：
- 《沪装修公司想新招 “装潢一日游”拉拢“团装”业主》，2008-02-21
  https://www.chinanews.com.cn/estate/gfzy/news/2008/02-21/1169532.shtml

所以一个可执行的 transaction 可能是：

```text
FORUM_THREAD_VISIBLE
→ USER_READS
→ CONTACT_ENDPOINT_FOUND
→ MSN CONTACT
→ OFFLINE MEETING
→ NEGOTIATION
→ CONTRACT/NO CONTRACT
```

Archive 若只保存 thread，只能证明前半段。

### 5.2 论坛 → QQ 群

2008 年个人信息泄露案例又显示，论坛可成为 QQ 群的入口。这里需要区分：

```text
forum membership
QQ group membership
real-property identity
phone/address disclosure
```

它们属于不同系统，不应合并成单一 `community_member=true`。

---

## 6. Thread → collective comparison：页面让分散经验变得可横向比对

### 6.1 停车费

2007-12-24，一名用户在搜房网建德国际公寓论坛询问停车费；其他住户由此发现，有人每月约 150 元、有人按日计费约 300 元，形成收费标准差异的公开比较。

Source B：
- 《调查12小区停车收费：有标准但有人钻空子》，2008-01-14
  https://news.sina.com.cn/o/2008-01-14/022813252848s.shtml

状态模型：

```text
INDIVIDUAL OBSERVATION
→ THREAD CLAIM
→ OTHER USERS DISCLOSE THEIR EXPERIENCE
→ APPARENT DISCREPANCY
→ MEDIA/PROPERTY ATTENTION
→ FORMAL VERIFICATION?
→ REMEDY?
```

关键缺口是 `apparent discrepancy → formal verification → remedy`。

### 6.2 物业打分

2009 年珠江峰景业主在论坛发起物业服务打分，列出卫生、停车、安全、维修、绿化等多个项目；物业称已安排人员了解评价。

Source B：
- 《业主自发打分点评物业》，2009-12-26
  https://news.sina.com.cn/c/2009-12-26/014516834422s.shtml

因此：

> `thread scoring != representative survey != property KPI != remediation`。

论坛可以产生一个可见评价对象，但不能跳过抽样、身份和执行。

---

## 7. Thread → media：旧网本地帖子可以进入报刊，但媒体再传播会重构证据

2007 年天津《每日新报》与搜房网业主论坛开设“新社区新新闻”板块，记者成为版主，业主可把环境、路灯、人行天桥等问题提交给媒体；还设有“新报信箱”用于不公开的信息。

Source B：
- 《“新社区新新闻”迎来开门红》，2007-01-30
  https://news.sina.com.cn/c/2007-01-30/085611120539s.shtml

这里需要区分：

```text
ORIGINAL FORUM POST
→ JOURNALIST SEES POST
→ JOURNALIST CONTACTS USER?
→ NEWS STORY
→ AGENCY/PORTAL REPRINT
→ TODAY'S SEARCH RESULT
```

今天搜索到的新闻可以证明媒体当时这样报道了论坛，但不是论坛原 HTML。

同一帖被多个门户转载，也不能自动算多个独立 evidence family。

---

## 8. Thread → offline organization：天通苑是强案例，也最容易被因果叙事夸大

### 8.1 社区网站谱系

2006 年同期报道说，天通苑社区网站从 2001 年的一家发展到十余家，“家住天通苑”及其他社区网站间存在人员和版主迁移。

Source B：
- 《天通苑社区网“群雄逐鹿”》，2006-06-27
  https://news.sohu.com/20060627/n243971274.shtml

这意味着“天通苑论坛”不能当作一个长期稳定 platform identity。研究时至少要区分：

- host / domain；
- site title；
- board；
- operator；
- moderator group；
- fork / migration / merger；
- historical period。

### 8.2 业主班车

2009 年同期回顾记录，从 2002 年起居民在社区论坛发帖组织班车；2004 年一条去 CBD 的班车由业主招募固定乘客、分摊包车费、轮值做班车长，并通过 email 发送月度财务明细。

Source B：
- 《北京天通苑10年成长记》，2009-07-01
  https://news.sina.com.cn/c/sd/2009-07-01/091918130581.shtml

建议 state machine：

```text
NEED POSTED
→ ROUTE DISCUSSED
→ RIDERS PLEDGE INTEREST
→ VEHICLE CONTRACTED
→ MONEY COLLECTED
→ FIRST RUN
→ REPEATED SERVICE
→ MONTHLY SETTLEMENT
→ SAFETY/LEGAL ISSUE
→ CONTINUE / HANDOFF / STOP
```

网页通常只会保存“招募”和“讨论”，最有历史意义的 `FIRST RUN / repeated service / settlement` 反而需要新闻、邮件、当事人记录等其他来源。

### 8.3 论坛共识与制度决策

天通苑、其他商品房小区大量论坛材料涉及物业、业委会、停车、公共收益和维权。

必须固定：

> `thread majority != owners' meeting quorum`。

尤其：

- 匿名账号无法等同产权份额；
- 一户多人可能多账号；
- 租户、潜在买家、外部人员也可能发言；
- “版主”没有天然法定授权。

2007 年天通苑维权基金因账目透明度遭部分捐款者质疑，正好显示线上声望与财务受托责任是两套状态。

Source B：
- 《业主捐款设维权基金 天通苑维权基金被指不透明》，2007-04-05
  https://news.sohu.com/20070405/n249214420.shtml

---

## 9. Forum → government / property response：收到，不等于办结

社区论坛常把现实机构拉入线程，但需要独立状态：

```text
POST EXISTS
→ INSTITUTION NOTICES
→ ACKNOWLEDGEMENT
→ CASE/WORK ORDER CREATED?
→ AUTHORITY IDENTIFIED?
→ SITE INSPECTION?
→ DECISION?
→ PHYSICAL WORK?
→ RESIDENT CONFIRMS OUTCOME?
```

2007 年上海政协提案讨论“有关部门是否应该多倾听业主论坛”，2009 年物业表示安排专人看论坛评价，都只支持 `institution notices` 或 `acknowledgement`，不能直接写 `problem solved`。

---

## 10. 2013–2015：论坛并没有瞬间消失，而开始与微信群形成 temporal overlap

2013 年上海中远两湾城报道里，八旬居民自管小组负责人已经持续通过微信群参与群租整治讨论。

Source B：
- 《业委会缺位，自管小组来自治》，2013-11-03
  https://cpc.people.com.cn/big5/n/2013/1103/c87228-23412977.html

而当前房天下仍有标记为 2014 年的旧论坛内容对象。搜索结果中一条哈尔滨“紫金城”2014-05-08 帖子今天仍展示发帖时间、用户名、回复，并在当前页面表层出现“进微信群讨论”。

Current legacy locator：
- https://hrb.esf.fang.com/loupan/1910385825/bbs/177243298_177243298.htm

另一条天津 2014-11-17 帖子也呈现类似旧帖 + 当前论坛 shell：
- https://tj.esf.fang.com/loupan/1110778823/bbs/185212081_185212081.htm

### 重要：这里不能推出什么

本轮能证明：

- 2026 访问环境中的 Fang legacy endpoint 仍对搜索系统暴露带 2014 时间戳的旧内容；
- 当前渲染结果包含微信讨论 CTA 等元素。

本轮**不能**证明：

- “进微信群讨论”在 2014-05-08 原始页面上已经存在；
- 当前 HTML/CSS/导航与 2014 相同；
- 当前 host path 就是历史 original URL；
- 旧帖的全部图片、签名、回复、用户资料都完整保存。

因此应标记为：

> `CURRENT_LEGACY_RENDERING / temporal composite candidate`，不是 `HISTORICAL_CAPTURE`。

这个对象非常适合作为以后“历史内容 + 现代平台壳”实验样本。

---

## 11. Browser / runtime assumptions

住宅论坛常见的历史运行时风险包括：

- GB2312 / GBK 页面与后来的 UTF-8 wrapper；
- frames / table layout；
- image host 分离；
- 登录后才能发帖或查看部分资料；
- JavaScript 翻页、弹窗、站内短信；
- QQ/MSN 链接依赖本地客户端；
- 用户签名和头像来自独立 CDN；
- 后期站点迁移导致旧 URL rewrite；
- 当前模板将现代 CTA 注入旧内容对象。

因此 modern browser 成功打开旧帖，只说明现代服务端可以生成一种当前表示。

必须保留：

`current rendering != original response bytes != historical browser experience`。

---

## 12. Archive preservation model

住宅社区论坛的保存至少有六层：

```text
1. board index survived?
2. thread HTML survived?
3. pagination/replies survived?
4. images/avatar/signature survived?
5. account/profile metadata survived?
6. linked QQ/MSN/email/offline outcome survived?
```

即使前五层都完整，第六层也通常最弱，而恰恰第六层决定这条帖子是否真正改变了生活。

### 本轮 archive 状态

本轮对 `soufun.com` / Fang 旧论坛相关对象、天通苑社区网相关关键词和公开 archive locator 进行了搜索，但没有取得一份可以按本仓 METHOD 实际检查以下字段的 verified replay：

- `archive_source`；
- `capture_url`；
- `original_url`；
- `capture_datetime`；
- historical HTTP status / headers；
- charset；
- DOM / frames；
- subresources；
- login/session behavior。

搜索到 archive.ph 上 `blog.soufun.com` 的快照索引，可以证明第三方档案服务曾索引搜房博客 host 的若干 2013–2015 资源，但它不是本专题业主论坛 case 的已验证 capture：
- https://archive.ph/blog.soufun.com

结论：

> **M1: NOT ACHIEVED IN THIS SLICE.**

严格表述只能是“本轮未验证到适用的 historical capture”，不能写成“Wayback 没有保存这些论坛”。

---

## 13. Historical visibility bias

### 13.1 Homeowner bias

“业主论坛”天然把资料组织在楼盘/产权话语周围，容易让后来的研究者误以为住宅生活主体都是产权人。

被低估的群体包括：

- 租户；
- 与产权人同住但不持证的家庭成员；
- 老年人；
- 没有固定宽带/PC 的住户；
- 只看不发的 lurkers；
- 不愿公开楼栋/房号的人；
- 被版主封禁或从群里移除的人。

### 13.2 Activity bias

最活跃的帖子通常来自：

- 物业纠纷；
- 装修；
- 停车；
- 交通；
- 房价；
- 维权；
- 活动召集。

沉默、满意、没有时间上网的人更难进入 archive。

### 13.3 Publicness bias

公开论坛更可能进入搜索引擎和 Web archive；QQ 群、站内信、电话、短信、楼道口谈话和线下会议更容易消失。

于是：

> `historian-visible coordination != total residential coordination`。

### 13.4 Outcome bias

发起帖比“事情最后怎样了”更容易留下。

例如：

- “周日集合团购”可被抓取；
- 谁最后真的买了、价格是否兑现，未必留下；
- “准备组班车”可能存活；
- 三个月后是否停运，可能只能靠另一篇报道；
- “物业答复”可能存活；
- 维修现场和之后是否复发，通常不在 Web。

---

## 14. Platform disappearance and temporal composites

2009 年关于天通苑十年发展的同期报道记载，“家住天通苑”在当年 7 月 12 日被关闭，到报道时仍未恢复。

Source B：
- 《天通苑：十年造“亚洲社区”》，2009-12-07
  https://news.focus.cn/bj/2009-12-07/810897.html

这里必须把四件事分开：

```text
community still exists
site temporarily/offline
forum database survives?
domain/URL survives?
```

一个几十万人的现实社区当然不会随着一个 host 下线而消失，但它过去十年的公开讨论记录可能因此变得极难复原。

反过来，Fang 当前 legacy page 又展示另一种情况：**内容对象可能幸存，平台壳却已经是后来的。**

所以本专题加入两个互补保存状态：

- `SOCIAL COMMUNITY SURVIVES / WEB ARTIFACT DIES`；
- `WEB CONTENT SURVIVES / HISTORICAL RUNTIME DIES`。

---

## 15. State-gap checklist for future cases

### Identity

- [ ] forum account 是否经过 email/phone verification？
- [ ] 是否有产权/房号核验？
- [ ] 是购房者、已入住业主、房东、租户还是外部人？
- [ ] username 是否能安全地与现实身份关联？
- [ ] 是否涉及不应重新公开的个人地址/电话？

### Page

- [ ] original host / URL？
- [ ] board index？
- [ ] thread URL pattern？
- [ ] pagination？
- [ ] charset？
- [ ] image/attachment host？
- [ ] guest posting / login requirement？
- [ ] moderator/版主状态？
- [ ] current shell 是否向旧帖注入新 UI？

### Cross-channel handoff

- [ ] QQ 群？
- [ ] MSN？
- [ ] email？
- [ ] phone/SMS？
- [ ] physical meeting？
- [ ] 业主大会/签名/投票？

### Outcome

- [ ] 只是发帖？
- [ ] 形成共识？
- [ ] 有现实组织者？
- [ ] 有资金？
- [ ] 有合法授权？
- [ ] 有机构 acknowledgment？
- [ ] 有实际执行？
- [ ] 有后续验收？

### Preservation

- [ ] current live legacy page？
- [ ] verified historical capture？
- [ ] ≥2 historical timepoints？
- [ ] subresources？
- [ ] forum database dynamic state？
- [ ] account/profile pages？
- [ ] private channel outcome irrecoverable？

---

## 16. Evidence ledger

| Claim | Evidence | Grade | Confidence | Boundary |
|---|---|---:|---|---|
| 2006 大连已有大量小区业主论坛且用于通知/活动/物业讨论 | 半岛晨报同期报道 | B | medium-high | 规模为媒体调查，不等于活跃用户人口 |
| 2007 上海公共讨论已把业主论坛视为社区民意入口 | 东方早报/文汇报同期报道 | B | high | 提案不是制度采纳结果 |
| 2007–08 小区论坛可支持团购、停车费比对和邻居发现 | 同期人物/调查报道 | B | high | 使用案例不能外推普及率 |
| 外部营销者会伪装为业主获取资料 | 2008 济南同期案例 | B | high | 证明身份边界破裂，不证明普遍发生 |
| 天通苑社区网站可召集真实班车等线下项目 | 2009 同期回顾 | B | medium-high | 论坛是多因素之一，不能作单因果 |
| 论坛声望与受托/法定权力不同 | 2007 维权基金争议 + 制度结构 | B/D | high | 不对具体个人作超出来源的道德判断 |
| 2013 微信群已进入部分小区自管 | 解放日报同期报道 | B | high | 个案，不代表论坛已被取代 |
| 当前 Fang 可提供带 2014 时间戳的旧帖对象 | current search/live legacy result | A-current | high | 只能证明当前表示，不是 2014 capture |
| 当前旧帖 shell 出现微信 CTA | current legacy rendering | A-current | high | 不能证明 2014 原 UI 已有 CTA |
| 本轮没有验证到合格 historical replay | research process | D/negative | high | 不是 archive absence claim |

---

## 17. Afterlife checks outside repo scope（只用于校验 earlier state）

这些材料不扩展 old-web 主 scope，只用来验证 2000–2015 建立的状态为何后来变重要。

### 2018：假业主群二维码

厦门反诈骗部门发现有人在小区张贴假的业主群二维码，并要求“楼栋+房号+姓名”格式，提醒存在信息套取风险。

- https://www.nbd.com.cn/articles/2018-04-27/1212499.html

它验证：早期论坛已经出现的 `local identity ↔ privacy` tradeoff 在群聊时代继续存在。

### 2019：常在线公共事务劳动

人民日报记录一名业委会主任从 2016 年建群开始持续协调小区事务，2018 年底在朋友圈描述自己“没日没夜地加班”。

- https://society.people.com.cn/n1/2019/1203/c1008-31486187.html

它验证：旧论坛的 volunteer moderation/coordination 可以在推送式群聊中演变为持续在线劳动。

### 2020：业主群成为应急基础设施

武汉、重庆同期报道显示，业主微信群被用于团购买菜、通知、排查和社区—物业协同。

- https://www.nbd.com.cn/articles/2020-02-10/1406821.html
- https://www.cac.gov.cn/2020-02/11/c_1582962734897490.htm

它验证：旧论坛时代形成的“在线发现本地陌生人并协调现实事务”机制，在 crisis state 下会承担更强职责。

### 2023–2024：群边界本身进入法律与治理问题

- 物业泄露业主单元信息案件：
  https://www.fj.chinanews.com.cn/news/2023/2023-07-05/527924.html
- 被踢出业主群后起诉案件：
  https://society.people.com.cn/n1/2024/0419/c1008-40219685.html

它验证：`group membership / admin authority / legal owner identity / privacy` 必须分别建模。

---

## 18. Cross-repo interpretation

与 `tmzncty/how-people-lived` 的 companion 专题交叉时，应保持分工：

- 本仓负责：页面、账号、论坛板块、站外 handoff、current legacy rendering、archive gap、身份/事务 state；
- Life Horizons 负责：搬入新社区后的社会网络重建、邻居发现、通勤/育儿/团购/公共事务如何改变可执行生活路线、2005–2026 的时代时间感。

跨仓共同结论可以是：

> 旧 Web 给新建住宅社区增加了一个电子“门厅”，让原本只有空间地址的一群陌生人获得了彼此可搜索的社会地址；但这个门厅从来不等于整栋楼，也不等于合法业主大会，更不等于事情最后在现实里办成了。

---

## 19. 本轮 stop condition 与下一步

本轮已经达到“可提交 research package”门槛，因为存在多个同时代 evidence family、清晰的 transaction gaps 和独立于现有租房/二手/业委会制度专题的新解释层。

但没有达到 M1 complete case 门槛。

下一步优先级：

1. 找到一个 2005–2009 搜房/独立社区站点的 verified Wayback/Common Crawl/其他 WARC capture；
2. 至少比较两个历史时点，确认 board index、thread URL、charset、登录、版主标识和外链；
3. 对 current Fang 2014 legacy page 做“historical content / modern shell”字段级拆分；
4. 找一个论坛 → QQ 群 → 线下活动有同一事件证据链的 bounded case；
5. 保存明确负结果，不因搜不到 replay 推断 archive 中不存在。

**M1 status for this slice: NOT ACHIEVED IN THIS SLICE.**