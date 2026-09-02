# 2003—2010：平台中介不等于平台创造——旧网社交与求职关系的来源判定

本文件补充：

- `docs/METHOD.md`；
- `docs/ACCOUNT_PORTABILITY_AND_LOCAL_RESIDUE_1999_2003.md`；
- `docs/SOCIAL_STATUS_VISIBILITY_AND_CONSUMER_ACCOUNT_IDENTITY_2008_2010.md`。

前一阶段已经区分：

```text
person ≠ account ≠ terminal ≠ local files ≠ server state
```

以及：

```text
status existence ≠ status visibility ≠ status credential
```

本文再补一个在研究 QQ、论坛、博客、贴吧、SNS、招聘帖和网吧材料时非常容易犯的错误：

> **platform-mediated tie ≠ platform-originated tie**

也就是：

> **一段关系通过互联网继续运作，不等于这段关系最初由互联网创造。**

---

## 1. 为什么这个区分重要

旧网页很容易让研究者看到：

- “老乡群”；
- “同事群”；
- 招工帖；
- QQ 联系方式；
- 论坛里的“介绍工作”；
- 博客好友；
- 校友社区；
- 地方论坛里的租房/招工信息。

然后产生一个过强推断：

> “这个平台创造了新的社会网络。”

但对 2000 年代大量用户，真实链条可能是：

```text
村里亲戚
→ 先去东莞
→ 把老乡叫来
→ 两人在同一工厂成为工友
→ 之后交换手机号 / QQ
→ 换厂以后继续通过 QQ 联系
→ 再把下一份工作信息发给对方
```

在这条链里：

- QQ **中介**了关系；
- QQ 可能延长、加速、扩展了关系；
- 但关系的**起源**可能是亲属、老乡、同事或同学。

考古记录必须把这两件事分开。

---

## 2. 反技术决定论证据：迁移求职网络在大众互联网之前已经很强

1990 年代中国农村—城市劳动力迁移研究已经反复记录：亲属、朋友、老乡与先行迁移者在寻找工作、住宿和迁移信息中占重要位置。

可用来源：

- Harry X. Wu & Li Zhou, “Research on Rural-to-Urban Labour Migration in the Post-Reform China: A Survey,” 1996：<https://ideas.repec.org/p/adl/cercwp/1996-04.html>
- Yaohui Zhao, “The Role of Migrant Networks in Labor Migration: The Case of China,” 2003：<https://doi.org/10.1093/cep/byg028>

Zhao 的研究特别强调：持续参与迁移、有实际经验的迁移者会促进后来者迁移，机制主要是实际帮助。

这意味着：

> **如果 2006 年的论坛、QQ 群或博客里出现老乡介绍工作，不能把“老乡网络”本身记成平台发明。**

平台改变的可能是：

- 找到对方的速度；
- 联系成本；
- 跨厂/跨城后的持续性；
- 一条消息能同时触达多少人；
- 关系能否在换地点后继续调用；
- 原本弱联系是否更容易保持。

这些都需要单独证明。

---

## 3. 同时代移动通信研究：旧关系可以被技术重新布线

2005 年《中国日报》对东莞农民工手机田野研究的同期报道指出：

- 手机帮助 migrant workers 与亲属、朋友保持联系；
- 手机被用于获得就业信息；
- 企业经营者已经意识到，工人能够通过移动通信了解外部工作机会，会增加他们的流动能力。

来源：

- *China Daily*, “Mobiles Better Migrant Workers' Lives,” 2005-10-21，经 China.org.cn 保存：<https://www.china.org.cn/english/null/146181.htm>

2008 年 MIT Press 的相关学术章节进一步把移动网络的作用概括为：

- 延长工作场所社会网络；
- 维持分散的家庭和亲属联系；
- 帮助零工劳动者与公司保持连接并组织工作。

来源：

- Pui-lam Law & Yinni Peng, “Mobile Networks: Migrant Workers in Southern China,” 2008：<https://doi.org/10.7551/mitpress/9780262113120.003.0005>

这些材料支持：

```text
existing tie
+
new communication infrastructure
→
more persistent / more reachable tie
```

但仍不能自动升级成：

```text
new infrastructure
→
created the tie
```

---

## 4. 对 QQ / 论坛 / SNS 案例建议新增四个字段

以后研究一个历史社交关系，建议至少记录：

```yaml
relation_observed:
  platform: "QQ / forum / blog / SNS"
  observed_at: "2008-xx-xx"
  relation_type_claimed: "coworker / classmate / fellow-villager / friend / unknown"

relation_origin:
  origin_context: "offline-workplace / hometown / school / platform-native / unknown"
  origin_evidence: "..."
  confidence: "high / medium / low / unknown"

platform_role:
  role: "created / mediated / maintained / reactivated / broadcast / unknown"
  evidence: "..."

mobility_role:
  cross_workplace: true|false|unknown
  cross_city: true|false|unknown
  cross_life_stage: true|false|unknown
```

### `created`

只有在证据能够支持“双方最初通过该平台认识”时使用。

例如同期自述明确说：

> “我们是在这个论坛认识的。”

### `mediated`

双方原本已经认识，只是通过平台继续交流。

### `maintained`

平台让关系在换单位、换城市、毕业等变化后继续存在。

### `reactivated`

原本失联或很少联系的旧关系，因为平台重新连接。

### `broadcast`

平台让一个已有关系网络中的信息从一对一变成一对多传播，例如群消息、论坛帖、QQ群公告。

---

## 5. “平台上的求职”也要拆成信息来源与关系来源

看到一个 2008 年招工帖时，至少存在几种不同机制：

### A. 陌生人市场

```text
陌生招聘者
→ 公开帖子
→ 陌生求职者
```

这最接近“平台替代熟人网络”。

### B. 旧关系数字化

```text
旧同事 / 老乡
→ QQ / 论坛发岗位
→ 原本认识的人响应
```

平台主要负责降低通信成本。

### C. 弱联系扩散

```text
我认识的人
→ 转发一个他朋友的岗位
→ 我第一次接触那个雇主
```

这里平台可能扩大弱联系半径。

### D. 社群型陌生关系

```text
同乡论坛 / 行业论坛 / 校友社区
→ 原本不认识
→ 因共同身份获得初步信任
→ 工作信息流动
```

这类最值得研究，因为平台既不是纯陌生市场，也不是简单复制已有强关系。

一个页面的 HTML 本身通常不能告诉我们属于哪一种。

必须找：

- 帖子上下文；
- 用户自述；
- 回帖中的关系称呼；
- 同期采访；
- 平台帮助页；
- 社群规则；
- 多个时间点的关系演化。

---

## 6. 2008 年仍大量依赖熟人求职：不要把“招聘网站存在”写成“熟人就业网络已经退出”

基于 2008 年 Rural to Urban Migration in China（RUMiC）调查的研究指出，近三分之二的农村—城市迁移劳动者通过家庭成员、亲属、朋友或熟人找到工作。

来源：

- Wenjin Long, Simon Appleton & Lina Song, “Job Contact Networks and Wages of Rural-Urban Migrants in China,” IZA Discussion Paper 7577：<https://www.iza.org/en/publications/dp/7577/job-contact-networks-and-wages-of-rural-urban-migrants-in-china>

因此旧网研究遇到：

- 招聘网站；
- 门户招聘频道；
- BBS 招工版；
- 地方论坛招聘帖；

时，必须继续遵守仓库已有的：

```text
exists ≠ available ≠ used ≠ popular ≠ caused
```

再新增：

```text
formal online channel exists
≠
informal social network displaced
```

平台可能扩展了一条新渠道，但旧渠道可以长期并存。

---

## 7. 一个重要的档案偏差：平台更容易保存“消息”，不容易保存“关系为什么可信”

例如 archive 可能保存：

> “某厂招人，联系我。”

但真正让这条消息有效的背景可能是：

- 发帖人与读帖人是同乡；
- 两人以前在同厂；
- 一个共同朋友担保；
- 群成员来自同一学校；
- 某个用户名在社区里已经积累几年信誉。

HTML capture 可以保存：

```text
message
username
time
URL
```

却可能丢失：

```text
offline trust path
prior workplace tie
hometown relation
phone calls before/after post
private QQ messages
face-to-face handoff
```

因此：

> **archived communication artifact ≠ complete social relation graph**

这是研究旧论坛招聘、二手交易、合租、聚会与迁移网络时必须显式记录的缺口。

---

## 8. 对“互联网改变生活”的安全表述梯度

### Level 1 — observed mediation

> 某关系在某时点通过平台通信。

只需直接 artifact 即可。

### Level 2 — cross-place maintenance

> 该平台被用于在换城市/换单位后维持旧关系。

需要用户自述、连续账号证据或其他材料。

### Level 3 — expanded reach

> 平台使信息到达原本不容易接触的人。

需要传播链或平台使用证据。

### Level 4 — network creation

> 平台创造了新的关系。

需要证明双方原来不认识，且关系起点来自平台。

### Level 5 — behavioral consequence

> 平台因此使某人换工作、迁移、租房、结婚或组织行动。

需要更强的因果链，不得由帖子存在直接推出。

---

## 9. 海外比较如何使用而不破坏本仓 scope

全球研究可以帮助判断机制是否普遍，但不把海外对象变成本仓主 case。

可比材料包括：

- 2008 年波兰—英国临时移民研究：社会网络影响迁移持续时间与决策；
- 2007—2008 年英国波兰移民网站研究：互联网逐渐成为 migrant network 的持续参照点；
- 2009 年新加坡外籍劳工研究：手机在高度流动、受制度约束的劳动者中维持跨地点关系。

来源：

- Anne White & Louise Ryan, 2008：<https://doi.org/10.1080/09668130802362227>
- Ian Fitzgerald, Jane Hardy & Miguel Martinez Lucio, research based on 2007–2008 Polish-administered UK websites：<https://researchportal.northumbria.ac.uk/en/publications/the-internet-employment-and-polish-migrant-workers-communication->
- Eric C. Thompson, 2009：<https://doi.org/10.1111/j.1471-0374.2009.00258.x>

这些材料用于支持一个一般问题：

> **数字平台究竟创造新关系，还是让已有迁移网络更持久、更广、更容易重复调用？**

中文旧网案例仍需用中文互联网自己的证据回答。

---

## 10. 以后做旧网 case 的最低检查表

遇到涉及“网友介绍工作”“QQ群招工”“论坛老乡会”“校友社区”“博客好友”的历史材料时，至少问：

1. 双方何时第一次认识？
2. 关系是否早于账号/平台？
3. 平台承担创建、维持、恢复还是广播功能？
4. 关系有没有跨单位、跨城市、毕业或返乡继续？
5. 公开页面之外是否存在不可见的电话、短信、私聊或线下关系？
6. archive 保存的是消息，还是也能证明信任路径？
7. 是否把平台功能存在误写成社会关系由平台造成？
8. 是否把一条在线招聘信息误写成该群体的主要就业渠道？

若无法回答，应保留：

```text
relation_origin: unknown
platform_role: observed mediation only
```

而不是补故事。

---

## 核心结论

旧网考古研究人的关系时，至少要同时保存三条时间线：

```text
关系什么时候开始
平台什么时候介入
人生地点什么时候变化
```

三者并不一定同时发生。

最重要的新规则是：

> **平台能够让一个关系跨越地点，不等于平台创造了这个关系；平台保存了一条消息，也不等于 archive 保存了让这条消息真正有效的社会信任结构。**
