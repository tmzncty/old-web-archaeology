# 法律援助热线、Web 问答、视频咨询、证据与现实救济状态差（1999–2015）

## 0. 范围

本 note 只研究约 1999–2015 年中文互联网环境里，与公共法律服务/法律援助直接相邻的 Web 接口、在线问答、视频咨询、律师/法援入口及其与现实程序之间的状态差。

它**不是**中国法律援助制度史，也不是全球 legal-tech 史。

1999 年以前的法律援助试点、148 电话前史仅作为理解中文 Web 服务为什么以“热线 + 网站”混合形态出现的必要边界；2016 年以后的微信、App、全国中国法律服务网和正式在线诉讼，只用于说明 2015 年以前哪些接口后来被重新整合，不改变本仓 1995–2015 中文旧网的主 scope。

本 note 的核心问题是：

> **旧网页面上出现“在线咨询”“申请法律援助”“律师回复”，究竟能证明现实中的法律救济走到了哪一步？**

---

## 1. 为什么这个对象适合旧网考古

公共法律服务是一类很容易产生“页面看起来比现实事务完整”的对象。

Crawler 可能保存：

- 网站首页；
- “在线咨询”栏目；
- 一条公开问题；
- 一条律师回复；
- 法律援助申请说明；
- 律师/机构名录；
- 业务统计新闻。

但真正决定一个人的问题有没有解决的状态往往在公开 Web 之外：

- 电话是否真正接通；
- 问题有没有通过管理员审核；
- 律师是否看见；
- 当事人是否读到回复；
- 是否转为线下会见；
- 是否提交正式法援申请；
- 是否通过经济困难/事项范围审查；
- 是否指定承办律师；
- 证据是否补齐；
- 是否进入调解、仲裁或法院；
- 最终裁决有没有执行。

因此：

```text
public advice page
!=
real-world remedy state
```

这是本 note 的最低解释边界。

---

## 2. 对象模型：不要把“一个法律网站”当成一个状态

至少拆成以下对象：

```text
physical person / party
legal problem / dispute
legal right / rule in force at historical time
telephone number
hotline queue / call
operator / lawyer / legal-aid worker
website / host
user account (if any)
public question
private question
moderation state
lawyer / adviser profile
answer draft
published answer
video consultation session
uploaded document / evidence image
legal-aid eligibility rule
legal-aid application
application review
assignment to lawyer
mediation / arbitration / litigation filing
accepted case / docket
award / judgment / settlement
execution / payment / reinstatement
archive capture
```

### 永久状态差

- `law in force != law shown on current page`
- `hotline number published != call connected`
- `call connected != professional advice completed`
- `question submitted != moderation passed`
- `moderation passed != lawyer viewed`
- `lawyer viewed != answer published`
- `answer published != questioner read`
- `online answer != lawyer-client relationship`
- `online answer != formal diagnosis of legal facts`
- `lawyer profile exists != lawyer available at that moment`
- `legal-aid information page != legal-aid application submitted`
- `application submitted != eligibility established`
- `eligibility established != lawyer assigned`
- `document uploaded != evidence authenticated`
- `evidence displayed over video != evidence admitted in later procedure`
- `mediation / arbitration / lawsuit filed != accepted`
- `accepted != claimant wins`
- `award / judgment != actual payment / performance`

---

## 3. 1999–2003：热线先构成事务骨架，Web 是后来叠加层

### Claim 3.1 — 148/12348 首先是电话与组织路由，不是 Web 产品

1999 年《光明日报》的同期报道记录：山东东明县 1998 年 3 月 16 日开通 148 法律服务专用电话；到 1999 年中，地、县级建制平均开通率分别约 39.1% 与 64.6%，仍有明显地区空白。

这对 old-Web 的意义不是写电话史，而是确定后来的网页并非从零开始：

```text
司法行政内部资源
→ 148/12348 电话统一入口
→ Web 在线咨询
→ 视频 / 文件传输
→ 后来的多终端平台
```

所以历史网页上出现 `12348`，不能自动解释为“此时 12348 已经是今天意义上的全国 Web 平台”。

**Evidence**

- **B / contemporary news** — 光明日报 1999-06-22（新浪保留）：148 起源、推广与地区开通率。  
  <https://news.sina.com.cn/china/9906/062213.html>

### Claim 3.2 — 同一个“12348”号码在地方上的启用时间与后台组织状态不同

上海 1999 年初运行 16000148，2002 年 1 月切换到全国统一号码 12348；广州则在 1999 年 6 月开热线、2003 年 12 月切换 12348。

因此：

```text
national number standard
!=
local number activated
!=
local service staffed
!=
local web service available
```

这与本仓已有 emergency-hotline 研究中的“号码标准 ≠ 地方服务已启动”相似，但这里要再增加**咨询、法援、律师、公证等后台法律服务资源的路由**。

**Evidence**

- **A/B** — 上海律师协会转载同期文件，2002-01-09。  
  <https://www.lawyers.org.cn/info/b315d368a80d4f2283a0cb882c397f90>
- **B** — 南方日报 2003-12-01（新浪保留），广州改用 12348。  
  <https://news.sina.com.cn/c/2003-12-01/10121224642s.shtml>

---

## 4. 2003–2007：北京市法律援助网说明“Web 提交”本身已经是多阶段事务

### Claim 4.1 — 2003/2004 左右北京已形成热线 + 网络 + 现场并行

北京市司法局后来的 25 年工作史记录：1999 年设 148 办公室；2003 年以后群众可通过网络、法援电话和现场咨询。

2016 年央广报道则明确写到：**2004 年北京市法律援助网开通并设“在线咨询”栏目**。另有中央财经大学法学院 2007 年的机构页面称，北京市法律援助网自 2003 年 12 月 3 日设立，设有“法援在线”和“法律援助登记申请”等频道；2006 年起，该校法律援助中心参与在线答疑。

这里存在一个需要保留的时间差：

- later institutional summary：2004 年开通；
- 2007 partner institution page：2003-12-03 设立。

两者并不一定冲突，可能涉及“设立 / 上线 / 正式开通”的口径，但在找到历史 capture 或原始公告以前，**不要把具体日写成绝对 launch date**。

**Evidence**

- **B/C** — 北京市司法局 25 年回顾。  
  <https://sfj.beijing.gov.cn/sfj/sfdt/ywdt82/flfw93/325875591/index.html>
- **B** — 央广 2016 对 2004 网站节点的回顾。  
  <https://china.cnr.cn/gdgg/20160523/t20160523_522216867.shtml>
- **B / partner institution contemporaneous-near** — 中央财经大学法学院，2007-09-30，描述 2006 合作和网站频道。  
  <https://law.cufe.edu.cn/info/1152/24348.htm>

### Claim 4.2 — “在线咨询”很可能不是用户提交后立即公开的同步聊天

2015 年一篇对北京市 12348 的产品说明保留了一条很有价值的流程描述：

```text
网友提问
→ 管理员审核
→ 律师回复
→ 管理员发布
```

这是一条后来的 B/C 级说明，不能直接替代 2006 DOM 或后台手册；但它提示 archive 研究必须为 **moderation state** 留字段。

一条公开问答能证明的只是：某条经过筛选的提问和答复最终公开过。

它不能证明：

- 同期一共有多少未通过审核的问题；
- 等待了多久；
- 提问者是否仍在等待；
- 是否收到私下补充答复；
- 是否后来进入正式案件。

**Evidence**

- **B/C** — 2015 对北京 12348 / 法援网咨询流程的产品说明。  
  <https://www.sohu.com/a/21530352_201718>

---

## 5. 2004–2009：音视频与文件传输让“证据”第一次更容易进入远程法律咨询

### Claim 5.1 — 2004 已有商业法律网站演示音频/视频咨询

2004 年《大连晚报》报道“中国法律顾问网”现场演示：用户可以通过网络与律师进行音频、视频交流，还可以邀请多名律师参与。

这只能证明功能被同期展示/宣传，不能证明：

- 用户规模；
- 浏览器/插件兼容性；
- 实际连接成功率；
- 费用；
- 是否形成正式委托关系。

**Evidence**

- **B** — 大连晚报 2004-12-27（新浪保留）。  
  <https://news.sina.com.cn/s/2004-12-27/01534634193s.shtml>

### Claim 5.2 — 2009 北京 148 视频咨询的关键不是“视频”，而是 document-bearing consultation

2009 年中国广播网记者在北京宣武区司法局现场记录网络视频咨询。同期报道明确提到：

- 咨询者可与律师视频交流；
- 系统有文件传输；
- 律师可向咨询者发送法律规定和文书格式；
- 咨询者可展示证据材料；
- 律师可对证据“有没有用、还缺什么”作初步判断。

这产生一个新的 transaction state：

```text
voice-only remote advice
→
document-bearing remote advice
```

但仍必须保持：

```text
lawyer saw scan / video image
!=
evidence formally authenticated
!=
evidence admitted by arbitrator / court
```

**Evidence**

- **B / contemporary field report** — 中国广播网 2009-06-19（新浪保留）。  
  <https://news.sina.com.cn/c/2009-06-19/151115818205s.shtml>

---

## 6. 页面层与现实救济层之间的最大鸿沟：evidence-to-remedy gap

2009 年《法制日报》关于农民工讨薪的同期报道里，法律援助律师反复提醒保存欠条、工资条、工资卡、考勤记录、对工单等材料。

对 Web archaeology 而言，这意味着一条“我要工资”的公开咨询页即使完整保存，也不能告诉我们现实 claim 有没有必要材料。

### 建议对象关系

```text
public question
    ↓
answer: “保存工资条 / 考勤 / 欠条”
    ↓
private evidence bundle [normally not public]
    ↓
legal-aid / arbitration application
    ↓
case file [mostly non-Web]
    ↓
award / settlement
    ↓
payment
```

### Archive asymmetry

最容易被 crawler 保存：

- 问题正文；
- 律师公开答复；
- 法条链接；
- “申请援助”按钮。

最不容易保存：

- 身份证；
- 劳动合同；
- 欠条；
- 工资流水；
- 考勤；
- 私下补充材料；
- 仲裁/法院内部状态；
- 真正到账。

本 note 把它称为：

> **advice-text survival / remedy-state loss asymmetry**

**Evidence**

- **B/T1** — 法制日报 2009-01-15（新浪保留）。  
  <https://news.sina.com.cn/o/2009-01-15/080515037302s.shtml>

---

## 7. 2010–2015：旧网站看起来“静态”，服务状态已经越来越后台化

### Claim 7.1 — 同一个公开入口背后存在 queue / staff / availability 状态

北京市司法局 2012 年工作材料记录法律援助中心已有接待、受理、审查、指派、办案等完整质量管理链，并累计通过法律援助网解答网民问题。

旧网页往往只会留下“在线咨询”按钮，却不会把这些后台状态完整暴露出来。

因此：

```text
consult button visible
!=
consulting staff online
!=
queue short
!=
answer SLA met
```

**Evidence**

- **A/B（北京市司法局）**：  
  <https://sfj.beijing.gov.cn/sfj/sfdt/sfxzyw59/422034/index.html>

### Claim 7.2 — 后来的 2016 改造反向证明旧系统存在呼转、掉线与延时咨询问题

2016 年央广在报道北京市新 12348 综合平台时明确说，旧专线随着咨询量增加，出现呼转不成功、通话质量差、掉线等问题；旧法援网咨询通常需要约 3 个工作日答复，改造后才计划提供实时在线服务。

这类 later evidence 不应倒推每一个 2010 页面当时“都很慢”，但它证明：

> **“在线咨询”四个字并不能告诉 archive researcher 它是实时、异步、多久答、是否积压。**

**Evidence**

- **B** — 央广 2016-05-23。  
  <https://china.cnr.cn/gdgg/20160523/t20160523_522216867.shtml>
- **B** — 北京日报/人民网 2016-05-24。  
  <https://politics.people.com.cn/n1/2016/0524/c1001-28373885.html>

---

## 8. Old-Web 状态机

建议以后遇到 1999–2015 中文法律咨询/援助页面时，至少记录这些状态：

### A. Institution state

```text
institution exists
hotline office exists
local service activated
staff / lawyer roster assigned
service hours
jurisdiction / service scope
```

### B. Web state

```text
host resolves
page served
account required?
question form rendered
question submitted
submission acknowledgement
moderation pending / passed / rejected
professional assigned
answer drafted
answer published
user notified
```

### C. Evidence state

```text
document possessed by user
scanned / photographed
uploaded / transmitted
lawyer viewed
lawyer says potentially relevant
original retained
later authenticated
later admitted
```

### D. Formal remedy state

```text
consultation only
referral
legal-aid application
eligibility review
application approved / rejected
lawyer assigned
mediation
arbitration
court filing
accepted
award / judgment / settlement
execution
actual payment / performance
```

### E. Archive state

```text
original URL known
candidate capture found
capture opened
capture datetime verified
HTTP / replay state checked
charset checked
DOM inspected
form action / endpoint inspected
subresources inspected
second historical time point checked
```

---

## 9. 时间语义：今天的法律页面尤其容易污染过去

法律 Web 页面有一个比普通内容站更危险的 archive problem：**法律本身会变。**

### 永久规则

```text
article publication time
!=
law version currently linked
!=
page's current disclaimer
!=
legal rule in force when the historical question was asked
```

例如，一个 2009 年的咨询页面今天仍能打开，而站点模板在 2020s 新增了“仅供参考”“请以最新法律为准”的 footer：

- 可以说今天页面有这个 disclaimer；
- **不能说 2009 原始 DOM 当时也有相同提示**，除非 historical capture 证明。

同理，旧回复里今天点击的法条链接可能已经指向修订文本。

建议单独记录：

```yaml
question_time:
answer_time:
law_effective_time:
current_page_observed_at:
current_template_elements:
historical_template_verified: false
```

---

## 10. 公开问答的“幸存者偏差”：真正复杂的问题反而更可能消失

### 10.1 moderation survival bias

公开 Q&A 通常已经经过平台筛选。

Archive 看到的是：

```text
submitted questions
→ moderation
→ publishable subset
→ crawler-visible subset
→ archived subset
```

因此公开页面不能代表所有求助需求。

### 10.2 successful-answer bias

有完整律师答复的页面天然比：

- 无人回复；
- 被退回；
- 转电话；
- 转线下；
- 因隐私未公开

更容易进入搜索引擎和档案。

### 10.3 remedy-success visibility bias

媒体和机构网站特别喜欢保存“讨回工资”“成功法援”的完整结局。

失败、撤回、时效已过、证据不足、胜诉后未执行、当事人觉得成本太高而放弃的路径更难留下。

因此不能从 archive survivor 推断“咨询通常能解决问题”。

---

## 11. 隐私：法律咨询是高敏感公共页面

法律问题常直接携带：

- 本名 / 手机；
- 家庭关系；
- 婚姻、疾病、伤害；
- 工作单位；
- 收入与债务；
- 身份证件；
- 住址；
- 未成年人信息；
- 涉及第三人的指控。

因此必须强化本仓现有规则：

> **historically public != ethically necessary to republish now**

如果未来发现旧法律咨询 archive：

优先保存：

- URL pattern；
- 页面模板；
- 字段 schema；
- moderation / answer 状态；
- 时间戳；
- service flow；
- 已匿名化的结构统计。

不要为了“完整复原”批量重新公开普通人的旧法律纠纷和身份证明材料。

尤其不要提交原始证据附件到仓库。

---

## 12. 与其他 old-web 研究的交叉

### 与 `CONSUMER_COMPLAINT_WEB_SUBMISSION_ROUTING_AND_REMEDY_STATE_GAPS_2004_2015.md`

共同问题：提交投诉/咨询以后如何转部门、是否真的救济。

区别：本 note 聚焦法律专业意见、法援资格、证据与正式法律程序，不重复一般消费者投诉路由。

### 与 `CIVIL_SERVICE_ONLINE_REGISTRATION_QUALIFICATION_PAYMENT_ADMIT_CARD_AND_HIRING_STATE_GAPS_2004_2015.md`

共同问题：`submitted != accepted`，以及资格审核是后台状态。

区别：这里的 eligibility 是法律援助/程序资格，后续状态还包括律师指派、证据、仲裁/诉讼和执行。

### 与 emergency-hotline 研究

共同问题：短号码把机构复杂度移到后台。

区别：紧急热线强调即时调度和位置；12348 多数情形强调法律分类、异步/同步咨询、转介和长程序。

### 与 news-repost lineage 研究

许多 2000s 证据今天只残存在新浪、搜狐等转载 survivor。转载正文可以支撑狭窄的同期语义 claim，但不能冒充原始机构网站 capture。

---

## 13. Archive / M1 检查状态

本轮已经确定若干 2003–2009 候选对象：

- 北京市法律援助网（“法援在线”“法律援助登记申请”）；
- 北京 12348/148 相关在线咨询入口；
- 2009 宣武区 148 网络视频咨询；
- 2004 “中国法律顾问网”音视频法律咨询服务。

但当前公开检索获得的主要是：

- 同期新闻；
- 合作机构对页面功能的描述；
- 后来的司法行政机构史；
- 后来对旧在线咨询流程的产品说明。

**本 slice 没有获得一份已经实际打开并同时满足以下最低条件的 historical capture：**

- exact original URL；
- archive capture URL；
- capture datetime；
- HTTP / replay state；
- charset / Content-Type；
- DOM / form structure；
- question submission endpoint 或 video/file interaction endpoint；
- subresources；
- second historical time point。

因此：

> **M1 verified historical Chinese legal-aid Web Q&A / video-consultation capture: NOT ACHIEVED IN THIS SLICE.**

这不等于“Wayback 没保存”。

更准确地说，本轮连部分早期服务的 **exact historical original URL** 都没有从高质量证据中可靠解析出来，因此不能用猜测域名去制造 archive negative。

---

## 14. 浏览器、编码和插件：目前必须保持 UNKNOWN

2003–2009 中文法律网站很可能处于 IE/GBK/Flash/ActiveX/插件高度常见的时代，但**年代常识不是页面证据**。

在没有 historical HTML / headers / manuals 的情况下，不得写：

- “必须 IE6”；
- “使用 GB2312”；
- “视频通过 ActiveX”；
- “页面采用 table layout”；
- “后台是 ASP/JSP/PHP”；
- “文件上传使用某特定插件”。

尤其 2009 视频咨询报道只证明“有视频和文件传输”，不能据此推断其客户端协议和插件栈。

---

## 15. 目前可以确认 / 可以合理推断 / 不知道

### 已确认

1. 148/12348 电话入口在 Web 法律服务之前已经形成，并存在明显地方 rollout 差异；
2. 北京在 2003/2004 左右已有法律援助 Web 在线咨询体系；
3. 2006 前后高校法律援助中心已经参与北京法援网在线答疑；
4. 2009 宣武区 148 视频咨询支持文件传送和证据初步展示；
5. 2010s 前期 Web 在线咨询与电话、现场服务并存，而不是替代关系；
6. 后来的系统改造记录反向证明，旧热线存在呼转/掉线、旧 Web 咨询存在延时答复等 backend constraints。

### 可以合理推断，但仍要降级

1. 在线公开问题只是全部求助的一部分；
2. 大量真实案件状态离开公开 Web 以后进入电话、面谈、法援内部系统、仲裁或法院；
3. 页面保存质量会系统性高估“咨询文本”，低估证据与执行链。

### 不知道

1. 2003/2004 北京法律援助网最初 exact URL、HTML、charset 和 browser assumptions；
2. 2006 “法援在线”具体表单字段、账号要求、审核状态码和通知机制；
3. 2009 视频咨询具体传输协议、客户端软件和附件格式；
4. 公开 Q&A 有多少比例转成正式法援申请；
5. 旧问题删除/匿名化规则如何演变；
6. 同一用户能否跨电话、Web、现场共享 case state；
7. 2015 以前不同地区 12348 网站的互操作程度。

---

## 16. 下一步

优先级从高到低：

1. 从 2006–2009 同期页面/新闻中的链接文本、网页源代码、引用页继续解析北京市法律援助网 exact historical URL；
2. 一旦 exact URL 可靠，查 Wayback / Common Crawl / 其他 archive locator，并**实际打开** candidate capture；
3. 若拿到 capture，记录 charset、form action、隐藏字段、是否需账号、question ID pattern；
4. 寻找第二历史时点，比较 2006 文本问答与 2009 视频/文件咨询是否属于同一平台或不同系统；
5. 只在证据满足 M1 后，再做浏览器复原；
6. 对普通咨询者内容坚持数据最小化，不重发身份和纠纷细节。

---

## 17. 这改变了我们怎样理解旧网

法律网站特别适合纠正一种“网页即事务”的错觉。

一张保存完好的 2007 页面可能有：

```text
在线咨询
律师回复
法律援助申请
```

二十年后看起来像一个完整服务。

但当年的普通人真正经历的可能是：

```text
先拨 12348
→ 被告知上网或带材料来
→ 在网吧 / 单位电脑提交
→ 等管理员审核
→ 三天后得到回复
→ 再去窗口
→ 补身份证和工资证据
→ 等资格审查
→ 指派律师
→ 仲裁
→ 法院
→ 执行
→ 半年以后才真正拿到钱
```

Web 只保存了这条生命路径里最公开、最容易抓的一小段。

所以对旧网考古而言，真正需要恢复的不是一句“当年已经能网上咨询法律”，而是：

> **页面上的按钮属于哪一个事务状态；它前面还要求什么，后面又必须发生什么，才会真正改变一个人的现实。**
