# Nursing-Home Directory, Bed Availability, Assessment, Waitlist, Admission and Occupancy State Gaps, 2007–2015

## Scope

本笔记研究约 2007–2015 中文旧 Web 及其相邻电话、短信、桌面软件和线下养老机构流程中，一个“养老院可以查到”究竟距离“某位老人真正住进去”还有多少状态。

本仓已有：

`docs/ELDERCARE_HOTLINE_ONE_BUTTON_TELECARE_REMOTE_MONITORING_AND_RESPONSE_STATE_GAPS_2007_2015.md`

它研究的是居家老人如何通过热线、一键呼叫、远程监测和社区服务获得响应。

**本文不重复 telecare。**

本文只问另一条事务链：

> **养老机构怎样被公开发现、比较；床位怎样被显示、评估、轮候、分配；老人怎样从一个 Web/电话目录里的“候选机构”变成真实住户。**

跨国养老服务信息前史、1980s—2026 晚年生命历程比较及疫情/旅居养老后续，见 sister repository：

`tmzncty/how-people-lived/topics/institutional-eldercare-bed-addressability-admission-autonomy-and-later-life-branching-china-1981-2026.zh-CN.md`

本仓严格保持中文旧网约 1995–2015 scope，不扩写成全球养老史。

按仓库 METHOD：

`platform ≠ site ≠ page ≠ capture ≠ institution ≠ vacancy ≠ application ≠ admission ≠ occupancy`。

---

## 1. Evidence contract and this slice's limit

证据分级沿用仓库标准：

- **A**：同期官方政策、政府服务说明、原始软件/产品材料、已核验 historical capture；
- **B**：同期媒体调查、用户/老人/家属/工作人员采访、操作教程；
- **C**：多年后回忆；
- **D**：研究者状态模型或复原。

本轮取得：

- 2009 北京 96156 的具体 Web locator：`www.bjcs.gov.cn`；
- 2009 深圳“统一养老院信息平台”需求的同期调查；
- 2009 养老机构内部管理软件的同时代软件目录证据；
- 2013 广州公办床位“申请—评估—轮候—入住”统一平台政策；
- 2013 无子女老人通过 96156 找到机构、但在 admission gate 被挡住的同期人物材料；
- 2014 公办床位公开轮候、护理型/休养型供需错配证据；
- 2016 沈阳统一养老平台作为超出本仓主体 scope 的 after-boundary 验证，用于证明后来公开前台与内部入住系统确实可以进一步合并。

但本轮**没有取得并实际打开一份满足 M1 合同的 2009 `www.bjcs.gov.cn` 养老机构查询 historical Memento/WARC**。

尝试直接请求：

- `https://web.archive.org/web/20090901000000/http://www.bjcs.gov.cn/`
- 对 `www.bjcs.gov.cn/*` 的 2009–2010 CDX-style query

当前工具访问链因 archive URL provenance 安全限制拒绝直接打开构造 URL。

因此只能记录：

> **M1 verified historical nursing-home directory Memento: NOT ACHIEVED IN THIS SLICE.**

这不等于：

- Wayback 没保存；
- `bjcs.gov.cn` 当时不存在；
- 养老院查询页一定不可回放。

以下仍为 `unknown`：

- 2009 页面 exact URL；
- HTTP status / redirect chain；
- charset；
- DOM / frames / tables / CSS；
- 浏览器兼容要求；
- 查询字段；
- form GET/POST；
- 结果页 URL pattern；
- 是否存在登录/session；
- 机构信息更新频率；
- 床位字段是否存在；
- 若存在床位字段，它是否实时；
- public front end 是否连接机构内部 occupancy database。

---

## 2. Object model：不要把“养老院网页”当成一张床

至少拆成这些对象：

```text
real-world eldercare institution
public institution record
public directory / portal
institution detail page
telephone directory record
internal institution management system
bed / room inventory
care-level capability
applicant record
elder assessment
waitlist position
admission offer
service contract
assigned bed
resident record
actual occupancy
care episode
```

它们可以完全分离。

### 2.1 `institution / listing gap`

现实中合法经营的机构不一定有独立网页，也不一定被某一目录收录。

反过来，历史目录里仍存在的条目也可能在后来：

- 改名；
- 搬址；
- 换运营主体；
- 停业；
- 转为护理院；
- 只保留品牌名。

所以：

`listing survival != institution continuity`。

### 2.2 `institution / bed gap`

养老机构不是一个 inventory unit。

同一家机构可能同时有：

- 自理床；
- 半自理/介助床；
- 失能护理床；
- 失智专区；
- 单间/双人间/多人间；
- 公办保障床位；
- 市场化床位。

因此：

`institution has vacancy != this elder has a suitable vacancy`。

### 2.3 `bed-count / live-vacancy gap`

页面写“床位 300 张”通常更接近 facility capacity claim，而不是 transaction-time vacancy。

必须拆：

```text
licensed / declared beds
→ physically usable beds
→ staffed beds
→ beds assigned to this care category
→ currently unoccupied beds
→ beds not already promised to waitlist applicants
→ beds available to this applicant
```

### 2.4 `directory-result / admission gap`

即使查询页显示：

```text
机构存在
+ 地址正确
+ 收费可接受
+ 离家近
```

仍可能在真实流程里遇到：

```text
护理等级不接
→ 无空床
→ 需排队
→ 需健康评估
→ 需代理/联系人/担保
→ 费用结构与页面摘要不同
→ 老人本人不愿入住
→ 看院后放弃
```

---

## 3. 2007–2009：旧网首先解决的是“我该问谁”，不是实时 bed booking

### 3.1 2009 北京：96156 同时有电话、Web、SMS、email

2009-09-01《新京报》同期报道明确给出：[S1]

- telephone: `96156`
- website: `www.bjcs.gov.cn`
- SMS: `1069031596156`
- email: `bjcs@bjcs.gov.cn`

并说明老人可查询北京市各敬老院情况。

这与现有 telecare 专题共享一个 historical locator，但这里问的 claim 不一样。

现有 telecare 文档证明：`96156` 是多通道社区/养老服务品牌，不是一个单一网站。

本文只使用其中最窄的一条：

> **2009 年同期媒体把 `www.bjcs.gov.cn` 列作可获取敬老院信息的 Web 入口之一。**

不能因此写：

- 网站可实时查询空床；
- 网站可在线签入住合同；
- 网站可上传老人健康评估；
- Web 查询与 96156 电话使用同一实时数据库；
- 老人本人而非子女/工作人员是主要 Web 操作者；
- 查询结果自动意味着机构接受该老人。

因此新增：

### `public-directory / executable-bed gap`

```text
养老院信息可查
!=
一张可被这个老人取得的床可查
```

### 3.2 2009 深圳：社会需求本身说明“有机构”不等于“可比较”

《深圳晚报》报道市老年人协会历时半年的养老院调查，并称许多老人即使详细走访，仍难在机构间选择，调研建议建立统一养老院信息平台。[S2]

这条证据很重要，因为它阻止一种 Web 后见之明：

> 不能因为 2009 年已经能 Google/Baidu 搜到若干养老院名称，就认为“找养老院的信息问题已经解决”。

老人实际需要比较的是：

- 地点；
- 价格；
- 公办/民办；
- 护理对象；
- 生活环境；
- 医疗支持；
- 是否真有床；
- 是否容易探望。

搜索引擎返回页面 ≠ 结构化选择信息。

---

## 4. 2009：养老机构内部已经可以数字化，但内部数字化 ≠ public Web

ZOL 2009-01-12 的软件目录仍保存“好来颐和养老院信息管理系统 3.0”条目。[S3]

其同期软件说明列出：

- 前台接待；
- 老人档案；
- 护理；
- 医疗；
- 库存；
- 居住管理；
- 费用结算；
- 报表等。

系统平台被列为 WinXP / Win98 / WinNT4 / Win95 / WinMe 等。

证据等级：**B：同期软件分发目录 / 产品说明。**

它可以证明：

> 2009 年市场上已经存在面向养老机构内部业务数字化的软件产品。

它不能证明：

- 全国养老院普遍采用；
- 这套产品拥有 Web front end；
- 某个政府养老目录使用它；
- 内部床位数据自动同步到公众网站；
- 软件标称功能在任一具体机构真实使用。

这形成：

### `internal-digitization / public-visibility gap`

```text
机构内部已经有 resident / room / billing database
!=
公众能在线看到真实 occupancy
```

这一点与很多旧网事务相似：**后台数字化通常先于个人直接操作的 Web 事务。**

---

## 5. 养老床位不是酒店库存：评估和公共分配会进入状态机

### 5.1 2013 广州：统一信息平台开始要求公开“床位 + 申请 + 评估 + 轮候”

2013 年新华社报道广州市研究建立公办养老机构统一评估轮候制度。[S4]

同期方案的关键点包括：

- 市、区县两级公办养老床位纳入公开轮候；
- 建立统一信息平台；
- 床位和申请、评估、轮候情况公开；
- 在优先保障特定困难老人前提下向符合条件老人开放。

这里第一次可以明确写出：

```text
public bed
→ applicant
→ assessment
→ priority
→ waitlist
→ vacancy event
→ offer
→ admission
```

而不是：

```text
看到“有床”
→ click buy
```

因此养老床位与酒店房晚最关键的差异之一是：**公办床位可能同时是公共资源分配问题。**

### 5.2 2014：统一轮候仍不等于整个养老市场统一

2014 年新华社/经济参考报继续报道“一床难求”和床位空置并存，并指出护理型供给不足、部分休养型机构却利用不足；广州当年已推进统一公办养老床位轮候。[S5]

因此必须保留：

`public waitlist visibility != citywide market vacancy visibility`。

一个城市可以：

```text
优质低价公办床排很久
+
高价或地点差的民办床空着
+
失能老人又找不到真正护理型床
```

总床位统计无法回答任何一项具体交易。

---

## 6. 2013 无子女老人：directory success 可以在 admission gate 之后归零

### 6.1 Ding Yu case

《新京报》2013 年采访 83 岁、终身未婚的丁玉（化名）。[S6]

她的流程非常适合做 state-gap case：

```text
想考虑机构养老
→ 通过 96156 获得养老院电话号码
→ 把号码记在纸质记事本
→ 实际拨打养老院
→ 询问入住
→ 被告知需要直系亲属签字
→ 没有可满足条件的人
→ 放弃该路径
→ 继续独居
```

这里：

`directory success = TRUE`

但：

`admission success = FALSE`。

而且 failure reason 完全不在“网站能不能搜到养老院”这一层。

这新增一个 old-Web 特别容易忽略的状态：

### `search-principal / admission-principal gap`

搜索者可以是老人本人；
入住事务却可能要求另一个现实人物——代理人、送养人、担保人、紧急联系人——加入。

因此：

`one human + one browser + one phone != sufficient transaction principals`。

### 6.2 `account model / family model gap`

未来如果找到某个 2010s “养老院在线申请”页面，不应该只记录登录账户字段。

还必须问：

- applicant 是老人还是家属？
- resident 与 operator 是否同一人？
- 是否有 guardian / proxy / contact / guarantor 字段？
- 是否默认存在“子女”？
- 一个无子女老人能否提交完整表单？

**事务的数据模型可能把标准家庭脚本写进 schema。**

---

## 7. 一个更完整的 admission state machine

### 7.1 Discovery

```text
institution exists
→ directory has record
→ record indexed / reachable
→ user finds record
→ user understands record
```

失败模式：旧地址、旧电话、机构改名、页面不被搜索、老人不会操作 Web。

### 7.2 Comparison

```text
price displayed
+ location displayed
+ care scope displayed
+ bed count displayed
→ user forms shortlist
```

失败模式：价格只是起价；护理费另计；床位数非 vacancy；护理对象描述太粗。

### 7.3 Contact

```text
phone / form / email request
→ institution receives
→ staff replies
```

失败模式：旧电话、邮箱无人值守、Web form 只发普通邮件、机构无法回答实时床位。

### 7.4 Eligibility / assessment

```text
elder identity
→ health / ADL information
→ care-level assessment
→ institution decides fit
```

失败模式：不接失智、不接重度失能、医疗需求超能力、公共政策资格不符。

### 7.5 Family / legal interface

```text
elder consents
→ proxy/contact/guarantor available if required
→ responsibility fields complete
```

失败模式：无子女、子女异地、家庭意见冲突、老人本人愿意但第三方字段缺失。

### 7.6 Public allocation, if applicable

```text
assessment
→ priority score/category
→ waitlist entry
→ waitlist position changes
→ vacancy appears
→ offer issued
```

失败模式：长期无腾退；不同 care class 队列不同；申请人情况在等待期间变化。

### 7.7 Contract and bed assignment

```text
offer
→ fee schedule understood
→ deposit/payment
→ contract signed
→ specific room/bed assigned
```

失败模式：页面价格和最终费用不一致；目标房型无床；护理费因新评估改变。

### 7.8 Physical admission

```text
elder arrives
→ identity checked
→ belongings / medication transferred
→ resident record activated
→ bed physically occupied
→ care plan starts
```

所以：

`contract signed != elder physically living there`。

### 7.9 Continuation / exit

```text
resident stays
→ care level may change
→ room/fee may change
→ hospitalization / leave may occur
→ resident continues / transfers / exits
```

“成功入住”也不是永久终态。

---

## 8. Public Web 与机构内部系统之间至少需要一个同步层

如果历史页面真的出现：

`剩余床位：12`

研究者至少要问：

1. 12 是哪个时间点？
2. 谁录入？
3. 人工日报、定时批处理还是实时接口？
4. 是全部空床还是只对外床位？
5. 是否含已承诺给轮候者但未入住的床？
6. 是否按护理等级分？
7. 机构内部转房是否及时回写？
8. archive capture 保存的是生成时页面还是缓存？

因此新增：

### `occupancy-ledger / directory-render gap`

```text
internal authoritative occupancy state
!=
public page rendered vacancy state
```

即便两者来自同一个数据库，也可能因缓存、同步周期和事务未提交而不同。

---

## 9. 2016 沈阳是 after-boundary，不纳入主体，却能验证前期 state gaps 的方向

2016 年辽宁日报/中央网信办报道沈阳建设统一养老服务信息管理平台。[S7]

报道明确把：

- 老年人口数据库；
- 养老机构数据库；
- 服务人员数据库；
- 互联网 / 电子政务外网 / 广电网 / 电话网 / 移动网络；
- 机构比较筛选；
- 机构内部老人档案、接待、订房、入住、收费、结算

放进同一体系描述。

这超出本文 2015 主 scope，因此不当成 old-Web 主案例。

但它可以反向证明一个方法论判断是合理的：

> **2009 的“公众养老院信息查询”与 2009 的“机构内部入住管理软件”是两个可分离技术层；后来才有明确系统试图把公开发现、政府数据与机构业务进一步统一。**

绝不能把 2016 的架构倒写成 2009 已经存在。

---

## 10. Generic state gaps to reuse across old-Web service archaeology

### 10.1 `real-institution / directory-record gap`

现实机构存在 ≠ 某目录有条目。

### 10.2 `directory-record / current-operation gap`

条目存在 ≠ 当时仍营业。

### 10.3 `institution / legal-operator gap`

同一品牌/地址 ≠ 同一运营主体。

### 10.4 `declared-bed-count / usable-bed-count gap`

标称床位 ≠ 可实际使用床位。

### 10.5 `usable-bed / staffed-bed gap`

床架可用 ≠ 有足够护理人员服务。

### 10.6 `staffed-bed / care-fit gap`

有护理床 ≠ 接受这个老人的失能/失智/医疗状态。

### 10.7 `bed-count / live-vacancy gap`

总床位 ≠ 当前空床。

### 10.8 `live-vacancy / uncommitted-vacancy gap`

空着 ≠ 没有已经承诺给轮候者。

### 10.9 `directory-query / contact-success gap`

搜到 ≠ 电话/邮件/表单有人回应。

### 10.10 `contact-success / assessment gap`

有人接电话 ≠ 开始正式健康/能力评估。

### 10.11 `assessment / eligibility gap`

完成评估 ≠ 符合该床位规则。

### 10.12 `elder-consent / family-interface gap`

老人愿意 ≠ 代理/担保/紧急联系人手续可完成。

### 10.13 `application / waitlist-entry gap`

申请 ≠ 已进入有效队列。

### 10.14 `waitlist-entry / current-position gap`

历史登记 ≠ 当前排序状态。

### 10.15 `waitlist-position / admission-offer gap`

排第一 ≠ 今日已有适合床位腾退。

### 10.16 `admission-offer / contract gap`

通知可入住 ≠ 双方已签服务合同。

### 10.17 `contract / physical-occupancy gap`

签约 ≠ 老人已搬入。

### 10.18 `occupancy / care-delivery gap`

人在床上 ≠ 宣传/合同中的护理逐项执行。

### 10.19 `public-price / payable-price gap`

网页基础床位价 ≠ 膳食、护理、医疗、耗材、代办等实际月总额。

### 10.20 `public-Web / telephone-transaction gap`

Web 是入口之一 ≠ 实际老人主要通过 Web 完成事务。

### 10.21 `internal-database / public-directory gap`

机构内部数字化 ≠ 实时公开。

### 10.22 `current-page / historical-vacancy gap`

今天仍能打开的机构页 ≠ 能复原历史某日床位状态。

---

## 11. Browser / charset / runtime: this slice must not guess

目前没有 verified 2009 `bjcs.gov.cn` nursing-home detail/query capture。

因此不得写：

- IE6 required；
- GB2312；
- table layout；
- frameset；
- ActiveX；
- ASP/JSP；
- JS popup；
- specific viewport；
- cookies/session requirement。

以上都可能符合时代常识，但 METHOD 明确禁止把常识冒充 exact historical evidence。

2009 养老院内部管理软件目录列出的 Win95/98/NT/XP 环境，只能用于那个**桌面软件产品**，不能拿来推断 `bjcs.gov.cn` 浏览器需求。[S3]

---

## 12. Archive bias：为什么我们可能保存了“哪儿有养老院”，却保存不了“这个老人为什么没进去”

### 12.1 `public-directory / private-admission-authority inversion`

最容易进入公共 archive 的：

- 地址；
- 电话；
- 机构简介；
- 价格宣传；
- 床位总量；
- 服务项目；
- 政府政策；
- 新闻报道。

最权威却最不应公开保存的：

- 申请人身份证；
- 健康史；
- ADL / 失能评估；
- 子女/监护人/担保联系人；
- 排队位置变化；
- 真实合同；
- 支付记录；
- 入住/转床/离院；
- 医疗与护理记录。

因此一张公开养老院目录永远不能完整复原 transaction truth。

### 12.2 `marketing-survival / weak-provider disappearance bias`

有专门网站、媒体报道和长期品牌的机构更容易留下痕迹。

缺乏网站、短期经营、改名、关闭、违规或只靠社区口碑获客的机构更容易在旧网史中消失。

最终 archive 可能把当年的养老服务市场保存得比现实更：

- 大型；
- 正规；
- 稳定；
- 品牌化；
- Web 化。

### 12.3 `capacity-survival / vacancy-loss asymmetry`

床位总数适合写进静态介绍页，因此容易保存。

空床数却可能按小时/天变化，依赖后台数据，最难被 crawler 有意义地保存。

于是二十年后研究者最容易回答：

> “这家机构宣称有 300 张床。”

最难回答：

> “2009-09-01 下午，一个需要半护理的老人打电话过去，究竟有没有一张能立即入住的床？”

### 12.4 `successful-offline-completion invisibility`

如果老人通过电话获知机构、子女带去实地看院、现场签约并入住，整个成功事务可能几乎不留下公开 Web trail。

因此：

`public archive transaction count != real-world admission count`。

---

## 13. A/B/C/D evidence matrix

| Claim | Evidence | Grade | Confidence | Limit |
|---|---|---:|---:|---|
| 2009 北京报道列出 `www.bjcs.gov.cn` 为 96156 四种入口之一，并可查敬老院信息 | 新京报同期报道 | B | high | 未验证历史页面/capture |
| 2009 深圳老人调研认为养老机构难比较并建议统一信息平台 | 深圳晚报同期报道 | B | high | 地方调查，不外推全国 |
| 2009 市场上有养老机构内部管理软件，含老人档案/居住/收费等模块 | ZOL 软件目录 | B | medium-high | 不能证明实际部署率 |
| 2013 广州计划用统一平台公开公办床位、申请、评估和轮候 | 新华社同期报道 | B | high | 政策计划 ≠ 所有功能当日上线 |
| 2013 丁玉从 96156 找到电话但因现实担保/签字要求无法入住 | 新京报同期采访 | B | high | 多家机构调查，不等于全国统一法定规则 |
| 2014 公办床位排队与部分民办/休养型床位空置可以并存 | 新华社/经济参考报 | B | high | 不能据此计算全国 vacancy rate |
| 2016 沈阳把机构查询与内部接待/订房/入住系统纳入统一平台描述 | 辽宁日报/网信办 | A/B | high | after-boundary，只作后续验证 |
| 2009 `bjcs.gov.cn` 具体 DOM/charset/form/runtime | none verified | — | unknown | 不猜 |
| 2009 查询结果是否含实时 vacancy | none verified | — | unknown | 不猜 |

---

## 14. Known / probable / unknown

### 已证实

- 2009 年北京存在可查询养老院信息的多通道服务体系，其中报道明确包含 Web locator；
- 2009 年深圳同期调查已经把养老机构信息难比较当作实际问题；
- 同时期养老机构内部业务已经存在商业信息管理软件；
- 2013 广州政策设计明确需要把床位、申请、评估、轮候公开到统一信息平台；
- 现实入住可以在“机构已经找到”以后因为护理、轮候、担保等问题失败；
- 2014 的公开材料表明“优质公办床位紧”和“部分床位空置”可以同时存在。

### 高概率，但本轮仍不能升级

- 2009 前台养老院目录的信息更新高度依赖人工/机构填报，而非今天式 transaction-time vacancy API；
- 老人本人和成年子女可能共同使用电话/Web/实地探院，Web operator 不必等于最终 resident；
- 内部 resident/room database 与政府 public directory 在 2009 多数情况下不是一个自动实时系统。

这些都符合证据方向，但缺 exact technical artifacts，不写成硬事实。

### 不知道

- `www.bjcs.gov.cn` 敬老院结果页 exact path；
- 2009 有多少养老院记录；
- 字段 schema；
- bed count 是否公开；
- vacancy 是否公开；
- 更新周期；
- 查询是否需要 IE-specific behavior；
- charset；
- page layout；
- 是否有在线申请；
- 是否能查 waitlist；
- 公众 Web 是否能进入内部 admission workflow。

---

## 15. Next archaeological steps

如果下一轮继续这一对象，优先级不是再找更多“养老难”报道，而是补技术证据。

### P0 — verified capture

寻找并实际核验：

- `http://www.bjcs.gov.cn/`
- `http://bjcs.gov.cn/`
- 2009 新闻中可能链接的养老/敬老院栏目 URL；
- `bjcs.org.cn` 历史 host/subdomain 谱系；
- ArchiveTeam / Common Crawl / national web archive 等替代来源。

必须记录：

```yaml
original_url:
capture_url:
capture_datetime:
http_status:
content_type:
charset:
redirect_chain:
page_role:
subresources:
login_required:
notes:
```

### P1 — exact schema

如取得页面，优先记录字段而不是截图审美：

- region；
- institution type；
- address；
- phone；
- bed capacity；
- price；
- care level；
- vacancy；
- admission conditions；
- update time。

### P2 — compare two historical points

理想时间点：

- 2009：96156 / `bjcs.gov.cn` directory；
- 2013/2014：广州统一评估轮候平台。

对比：

`information directory → public resource allocation state`。

### P3 — backend artifact

寻找养老机构内部管理软件原始安装包、截图、手册或数据库字段说明。

重点确认：

`room / bed / resident / admission / discharge / billing`

怎样建模，而不是运行现代仿制品。

---

## 16. Cross-repository conclusion

旧 Web 在这个对象上真正改变的不是“老人终于可以网上买一个养老院床位”。

更准确的是：

```text
养老机构最初只是线下福利/服务场所
→ 电话和政府目录先让它可被远程找到
→ Web 开始让多个机构可比较
→ 机构内部 resident / room / billing 也数字化
→ 公共床位又需要 assessment + waitlist
→ 后来系统才逐步尝试把公开发现、床位状态、评估、预约与入住连接起来
```

所以对于 old-Web archaeology，最危险的后见之明是：看到一个养老院详情页，就把今天的 OTA / 外卖平台交易逻辑投射回去。

养老床位从来不是简单 SKU。

它同时是：

- 居住空间；
- 长期照护资源；
- 可能需要公共分配的稀缺资源；
- 依赖护理等级的匹配对象；
- 与家庭责任接口相连的事务；
- 一个真实老人可能住几年的生活地点。

**目录页面只证明“这个选择进入了信息空间”；真正的生活分支要等到老人跨过 assessment、waitlist、family/legal interface 和 physical admission，才真正发生。**

---

## Sources

### [S1] B — 《新京报》，2009-09-01
《“96156”可查养老院信息》
https://news.sina.com.cn/c/2009-09-01/051016217455s.shtml

Historical locator：`www.bjcs.gov.cn`。
注意：locator ≠ verified archive capture。

### [S2] B — 《深圳晚报》，2009-09-01
《养老院现状：公办太挤私立太贵 不能自理者居多》
https://news.sohu.com/20090901/n266367389.shtml

支持：同期老人/协会调查、机构难比较、统一信息平台需求。

### [S3] B — ZOL 软件目录，更新时间 2009-01-12
《好来颐和养老院信息管理系统 3.0》
https://xiazai.zol.com.cn/detail/35/341504.shtml

支持：养老机构内部接待、老人档案、护理、医疗、居住、费用等数字管理软件的产品存在；不证明部署率。

### [S4] B — 新华社，2013-09-23
《广州争取年内出台公办养老床位评估轮候制度》
https://politics.people.com.cn/n/2013/0923/c70731-23002519.html

支持：统一信息平台公开床位、申请、评估、轮候的制度设计。

### [S5] B — 新华社/经济参考报，2014-09-12/15
《养老机构冷热不均加剧 一床难求与床位空置并存》
https://politics.people.com.cn/n/2014/0912/c70731-25646106.html
https://www.cnfin.com/news-xh08/a/20140915/1385544.shtml

同一新华社 evidence family，只计一组，不因两个 URL 假装两份独立来源。

### [S6] B — 《新京报》，2013-10-12
《孤寡老人有钱难进敬老院 “以房养老”难适应》
https://finance.people.com.cn/n/2013/1012/c1004-23173194.html

支持：丁玉从 96156 获得号码、实际拨打、在现实 admission gate 失败；以及多家机构当时的“送养人/担保人”实践。

### [S7] A/B — 辽宁日报，经中央网信办，2016-02-03
《沈阳采集157万老人信息建大数据平台》
https://www.cac.gov.cn/2016-02/03/c_1117984337.htm

仅作 **after-boundary**：证明后来公开机构比较与内部接待/订房/入住/结算可被放入统一平台设计。不得倒推 2009 架构。

### [S8] Method anchor — repo local
`docs/METHOD.md`

用于 archive locator、evidence grade、negative evidence、browser assumption 和 privacy/copyright 约束。
