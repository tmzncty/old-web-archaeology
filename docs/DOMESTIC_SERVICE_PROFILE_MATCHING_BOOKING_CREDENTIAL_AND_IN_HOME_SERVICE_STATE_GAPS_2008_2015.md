# 中文旧网中的家政人员资料、匹配、预约与上户状态缺口（2008–2015）

Status: methodology / evidence-gap note  
Scope: approximately 2008–2015 Chinese Web / mobile-Web / early app evidence related to nanny, maternity-care, cleaning and domestic-service matching  
Cross-link: `tmzncty/how-people-lived/topics/paid-domestic-service-care-time-substitution-and-cross-household-time-transfer-china-1985-2025.zh-CN.md`

## 研究问题

旧网页很容易给后人一种错觉：

> 页面上有一个保姆资料，旁边写着“待岗 / 可预约”，所以当时一个普通家庭已经可以顺利找到、验证、签约并获得这项服务。

这不成立。

家政服务特别适合检验本仓的核心原则，因为它把 **公开数字状态** 和 **私人家庭内部状态** 拉得很远。

一个可见 profile 只证明某个系统在某一时点愿意这样展示某个人或某类服务。它不自动证明：

- worker 仍然可用；
- profile 是本人创建；
- 身份 / 健康 /培训资料已被独立核验；
- 家庭成功联系到 worker；
- 双方签了合同；
- worker 实际到家；
- service 按约完成；
- 实际工时与页面一致；
- 钱真正到 worker 手里；
- 后来没有换人、投诉、续约或转为线下私下联系。

因此本文件把“网上找保姆”拆成可检验的状态机，而不是把一个搜索结果页当作完整交易史。

---

# 1. 为什么从 2008 年切入，而不把互联网写成起点

中文旧网范围内最重要的前史是：家政匹配早于 Web。

1985 年北京已有妇联 / 街道推动的家务服务公司网络；1986 年北京家庭服务员管理规则已要求身份、健康、暂住 / 居住相关材料、介绍机构和合同。

这些属于 `how-people-lived` 的互联网前史，不把 `old-web-archaeology` 主对象无限前移。

对本仓来说，它们只提供一个必要边界：

> **Web profile 是旧有 trust / intermediary / contract route 的新界面，不是家庭服务劳动的起点。**

前史 locator：

- 1985-12-22 *人民日报* 文章数字转录：
  https://cn.govopendata.com/renminribao/1985/12/22/1/
- 北京市政府保存的 `京政办发〔1986〕110号`：
  https://www.beijing.gov.cn/zhengce/zfwj/zfwj/bgtwj/201905/t20190523_73770.html

这些来源不进入 1995–2015 Web artifact 数据集；只作为边界说明。

---

# 2. 2008 广州 96909：从“公司里有谁”到“网上可以查询谁”

## 2.1 同时代证据

2008-07-29，《羊城晚报》报道一个由省家政协会指导、与 `96909` 公益家政热线相关的保姆信息登记系统已经开通，市民可登录：

`www.96909.com.cn`

查询已登记保姆基本资料。

报道说登记信息涉及：

- 年龄；
- 籍贯；
- 基本身份资料；
- 特长；
- 后续计划增加工作简历、客户评价等。

首批约有 3000 多条登记信息，其中近六成被报道为待业状态；不方便上网的市民仍可电话查询。

来源：

- *羊城晚报* 2008-07-29，新浪镜像：
  https://news.sina.com.cn/c/2008-07-29/140014235251s.shtml

Evidence: **B — 同时代媒体对系统、入口与字段的报道**。

同日《南方日报》报道也称约 3000 名家政从业人员资料进入系统，平台按小时更新员工信息，并说明可通过服务人员编号查询。

来源：

- https://news.sina.com.cn/c/2008-07-29/024414231312s.shtml

Evidence: **B**。

## 2.2 这能证明什么

可以谨慎写：

> 2008 年 7 月，广州存在一个面向公众的家政人员信息登记 / 查询 Web 入口，并与电话热线并行；同时代报道把 worker 身份、技能、就业状态和未来评价记录描述成可进入数据库的字段。

不能写：

- 2008 年所有广州保姆都已数字化；
- 数据库里的“待业”始终实时准确；
- 页面完成了公安身份核验的全部后端流程；
- 用户能直接在网页完成雇佣；
- 网站一定支持在线合同 / 支付；
- 该域名今天的页面结构等于 2008 年结构。

---

# 3. 一个家政 worker profile 至少包含五种不同身份

不要把一个 profile 当作“这个人本身”。

至少拆成：

### 3.1 Profile subject

页面在描述谁。

### 3.2 Profile creator / registrar

谁把资料录入系统：

- worker 本人；
- 家政公司；
- 协会 / 热线；
- 门店员工；
- 其他代理人。

### 3.3 Credential issuer

身份证、健康检查、培训证书、保险分别是谁出的。

### 3.4 Credential verifier

平台 / 公司是否真的核过原件，还是仅展示了一个字段或自述。

### 3.5 Current service actor

实际进入家庭、完成服务的是不是仍然同一人，还是后来换人 / 代班 / 重新派单。

这五层必须分开。

---

# 4. Profile state machine

建议对旧家政平台的 worker 资料使用以下状态：

```text
person exists
→ person reaches agency / platform
→ identity material submitted
→ health material submitted
→ training / skill claim submitted
→ insurance / other credential state attached
→ profile created
→ profile approved / indexed
→ profile discoverable
→ availability state displayed
→ household views profile
→ household initiates contact / request
→ worker responds
→ interview / call / video interview
→ household selects worker
→ contract / agency-membership / service agreement state
→ dispatch / appointment created
→ worker remains available at scheduled time
→ worker arrives at household
→ household grants entry
→ service starts
→ actual duties / hours occur
→ service accepted or disputed
→ payment state
→ rating / complaint / replacement / renewal
→ off-platform repeat relationship or termination
```

Archive capture 经常只能看到中间的几个公开节点。

---

# 5. 必须新增的 evidence gaps

## 5.1 profile-subject gap

`页面有一个人名 / 照片 / 编号`

不等于：

`已确认页面操作者就是本人`。

## 5.2 credential-claim gap

`页面写“健康检查 / 培训 / 身份验证”`

不等于：

`历史时点上存在可复核的有效证件状态`。

需要记录：

- 谁发证；
- 哪一年；
- 是否过期；
- 平台只是展示文字还是核验原件；
- 后来重新验证没有。

## 5.3 availability-state gap

“待岗”“可预约”“在岗”属于**高时效状态**。

2008 报道甚至说平台按小时更新 worker 信息。

因此：

> capture at 14:00 showing `待岗` 不能证明 17:00 仍可雇。

这类字段应带：

- observed_at；
- capture_datetime；
- claimed update frequency；
- whether backend freshness is independently known。

## 5.4 contactability gap

profile 可见不等于：

- 电话仍有效；
- 平台消息能送达；
- worker 会回复；
- agency 仍代表该 worker。

## 5.5 interview-state gap

电话 / 视频面试按钮存在不等于面试实际发生。

## 5.6 booking-state gap

`预约提交`

不等于：

- worker 接单；
- worker 当天仍空闲；
- 平台确认；
- worker 到达。

## 5.7 contract-state gap

2017 年关于“网约家政”的同期调查已经能看到一种重要断裂：用户可以在 App 上完成预约与付款流程，但被测试的订单没有生成已签署服务协议。

虽然 2017 超出本文件主要 2008–2015 artifact 观察窗，它可以作为后续 continuation 提醒：

> **digital order state 与 legal / contractual state 必须分开。**

Locator:

- https://www.chinanews.com.cn/m/life/2017/12-25/8408265.shtml

## 5.8 arrival-state gap

这是家政服务最重要又最难被 Web 保存的一步：

> 这个人有没有真的来到这扇门前？

## 5.9 household-entry gap

到门口也不等于进入家庭。

雇主可能因为：

- 身份疑问；
- 时间不合；
- 外观 / 沟通；
- 临时取消；
- 健康担忧；
- 家庭成员反对；

而拒绝最终上户。

## 5.10 in-home-service gap

这是真正的“黑箱”。

Web 页面通常不知道：

- 实际做了哪些任务；
- 是否临时追加任务；
- 孩子 / 老人真实照护时间；
- 夜里起了几次；
- worker 休息了多久；
- 是否有 unpaid standby；
- household 是否持续监督。

## 5.11 wage / settlement gap

广告价格 ≠ worker 实收。

要区分：

- household paid；
- agency fee；
- platform fee；
- insurance / membership；
- worker gross pay；
- worker net receipt；
- paid date；
- refund / deduction。

## 5.12 replacement gap

“雇到一名保姆”不等于关系持续。

2009 同时代报道中，一些家庭反复更换 worker。

因此必须有：

`selected → first day → retained → replaced / quit / renewed`

而不是只有 `hired=true`。

## 5.13 off-platform relationship gap

worker 与 household 建立信任以后，后续关系可能：

- 继续通过平台；
- 改走电话；
- 微信 / QQ；
- 私下续约；
- 熟人转介绍。

平台记录终止不等于劳动关系终止。

---

# 6. 2009：论坛、媒体与家政平台不是同一种证据

2009 年《中国青年报》关于保姆市场的调查说明，当时 Internet 已经进入家政劳动的**信息环境**，但不应把所有网络讨论都称为“在线家政平台”。

文章里的家庭会：

- 访问多个家政机构；
- 判断“金牌 / 星级”称号；
- 使用互联网讨论 / 论坛获取经验；
- 反复更换实际服务人员。

来源镜像：

- https://www.chinanews.com.cn/life/news/2009/03-02/1583787.shtml

Evidence: B — contemporaneous reporting.

必须区分：

### forum advice

用户讨论“怎样找保姆 / 这个公司靠谱吗”。

### directory / registration system

worker profile 可查询。

### transaction platform

能够真正预约 / 下单 / 支付 / 管理履约。

### agency's own website

只是一个传统中介的数字展示页。

同样叫“网上找保姆”，其 backend state 完全不同。

---

# 7. 2015：移动 App 可以证明哪些状态已经进入界面

一个第三方软件下载页面在 **2015-10-12** 保存了 `无忧月嫂 app 1.0` 的产品信息，描述功能包括：

- 浏览月嫂详细信息；
- 一键预约 / 咨询；
- 查看预约；
- 收藏候选 worker；
- worker 状态实时更新（产品声明）；
- 网上预约；
- 视频面试；
- 身份、健康、保险、培训等保障声明。

Source:

- https://www.cr173.com/soft/170542.html

Evidence: **B — 2015 第三方软件目录对当时 app 的描述**。

这足以证明：

> 至少到 2015 年，家政匹配中的 profile、availability、booking 和 remote interview 已经可以作为移动软件的产品状态被公开宣传。

但不能证明：

- 每个字段都实时；
- 身份验证后端具体如何运行；
- 每个 worker 都有完整证件；
- 视频面试一定通过该 app 自有实时视频技术完成；
- 预约一定形成合同；
- 所有城市功能一致。

---

# 8. Retrospective-product-copy trap

当前 App Store 的“无忧保姆”介绍写称：

> 平台 / 公司于 2008 年 5 月建立，并具有在线支付、在线面试、实时 worker 状态等功能。

Current locator:

- https://apps.apple.com/cn/app/id711993906

这类信息的证据角色必须拆开。

### 可以登记为 C / later company claim

- 公司今天怎样讲自己的历史；
- 它声称起点为 2008 年。

### 不能直接升级为 A

不能从 2020s 的 App Store copy 推出：

- `51baomu.cn` 在 2008-05 的具体页面已上线；
- 2008 年就已经支持今天列出的所有功能；
- 当时网站使用今天的数据库 / UI / verification pipeline。

正确工作流是：

> later corporate chronology → historical URL candidate → Wayback / Common Crawl / contemporary press verification → only then historical Web claim

本轮没有取得并实际核验一个 2008 年 `51baomu.cn` historical capture，因此不写 2008 UI 结论。

---

# 9. Worker availability 是一种典型的 archive-hostile state

家政资料页可能有：

```text
待岗
已约
在户
可立即上户
本周可约
下月有档期
```

这类状态的历史价值很高，因为它们直接决定一个普通家庭当时能不能执行照护计划。

但它们也是最难保存的状态之一：

- 高频变化；
- 可能来自私有后台；
- 搜索页会排序；
- worker 可能被多个门店 / 平台重复登记；
- capture 保存的是显示状态，不是 backend transaction log。

因此 schema 应避免只有：

```yaml
available: true
```

而应类似：

```yaml
availability_claim:
  displayed_value: "待岗"
  observed_at: "capture timestamp"
  source_page: "..."
  freshness_claim: "hourly / real-time / unknown"
  backend_verified: false
```

---

# 10. Search ranking and visibility

如果平台支持：

- 默认推荐；
- 星级排序；
- 好评排序；
- 最近可用；
- 附近 worker；
- 付费推荐；

则 profile 存在不等于 profile 获得相同曝光。

应增加：

`profile-index gap`

和：

`ranking / discoverability gap`

本轮没有取得可可靠说明 2008–2015 具体家政平台排序算法的历史 source，因此不推断排序逻辑。

---

# 11. Credential display schema

家政 profile 可能列出多类高敏感 credential。

建议不保存真实个人字段，而保存字段类型与验证语义：

```yaml
credential_field:
  type: identity|health|training|insurance|residence|work-history|other
  displayed: true
  issuer_named: true|false
  issue_date_visible: true|false
  expiry_visible: true|false
  verification_claimed_by_platform: true|false
  verification_method_known: false
  historical_validity_at_capture: confirmed|claimed|unknown
```

不要在公开 dataset 中复制：

- 身份证号；
- 详细户籍 / 家庭地址；
- 健康检查具体隐私结果；
- 电话；
- 私人照片；
- 家庭成员信息。

---

# 12. Household-side identity is also hidden

平台考古经常只盯 worker profile，忘记雇主一侧也有身份状态。

必须区分：

- account owner；
- person who searches；
- payer；
- household head；
- care recipient；
- person who interviews worker；
- person who supervises worker；
- person physically present at home。

例如：

> 女儿在网上替父母找护工

时：

`account user ≠ household resident ≠ care recipient`

这和本仓在婚恋 / alumni / care navigation 中已经发现的代理操作问题同构。

---

# 13. A complete household-service transaction model

建议以双边状态记录，而不是单一 order。

## Worker lane

```text
worker enters labor market
→ agency/platform registration
→ credentials submitted
→ profile indexed
→ availability state
→ contacted
→ interview
→ selected
→ contract / membership state
→ dispatched
→ arrival
→ household entry
→ service
→ payment
→ rating / repeat-client / replacement state
```

## Household lane

```text
care need appears
→ source/channel search
→ candidate list
→ profile view
→ trust assessment
→ contact
→ interview
→ selection
→ price agreement
→ contract / booking
→ waiting for arrival
→ worker arrives
→ household grants entry
→ service observed
→ accepts / disputes
→ pays
→ renews / replaces / exits platform
```

只有两条 lane 都闭合，才可以声称：

> “this online match became an actual in-home service relationship.”

---

# 14. 公开 Web 最容易保存什么、最难保存什么

## High survival probability

- platform landing page；
- agency directory；
- generic worker-list template；
- public service categories；
- advertised price；
- app feature description；
- help / terms pages；
- press launch report。

## Medium

- worker profile；
- availability label；
- public rating；
- public job/request listing。

## Low

- contact response；
- interview；
- signed contract；
- booking backend；
- household address；
- actual arrival；
- private messages；
- payment settlement；
- complaint handling；
- replacement event。

## Extremely low / should often remain private

- actual in-home labor day；
- infant / elder care details；
- household conflict；
- worker sleep / food / bathroom access；
- keys / medication handling；
- health information；
- worker's own family arrangements。

因此：

> **数字市场越公开，真正劳动过程仍可能越私人。**

---

# 15. 2017 and 2020 are continuation evidence, not excuses to expand scope

本仓主 scope 仍是约 1995–2015 中文互联网。

2017 App 预约调查和 2020 pandemic 平台案例只用于验证 2008–2015 已经出现的状态后来如何继续发展：

- booking / contract separation；
- profile / credential verification；
- online match / physical arrival separation。

它们不应把本文件扩成 2020s 家政平台史。

后续生活史主要写入 `how-people-lived`。

---

# 16. Privacy / dignity boundary

家政旧 profile 比普通论坛用户名更敏感，因为它可能把：

- 女性 worker 的照片；
- 年龄；
- 籍贯；
- 身份资料；
- 健康状态；
- 工作经历；
- 雇主评价；
- 电话；
- 当前“待岗”状态；

绑在同一个页面。

因此：

1. 不因 Wayback 可访问就批量重新公开 worker profiles；
2. 优先保存 schema、字段类型、页面结构和去标识统计；
3. 研究平台搜索机制时不需要重发真实姓名 / 电话；
4. 健康信息只记录“存在 health credential 字段”，除非有极强研究必要性，不复制检查内容；
5. 不把旧 worker profile 与今天社交账号做人肉式关联；
6. 不联系历史 worker / household 来验证 archive claim，除非未来有独立伦理审查和明确同意流程。

---

# 17. Evidence table

| Claim | Time | Source role | Grade | What it supports | Does not support |
|---|---:|---|---|---|---|
| Guangzhou `96909` Web worker-registration/query system launched | 2008-07 | contemporaneous press | B | public worker database/query existed | exact DOM/backend |
| about 3,000 registered workers, many marked waiting for work | 2008-07 | contemporaneous press | B | availability status was represented | exact real-time truth |
| identity/origin/skills and planned work-history/reviews | 2008-07 | contemporaneous press | B | profile-field concept | completeness of each profile |
| `无忧月嫂 app 1.0` listed profile/booking/video-interview/status claims | 2015-10 | software directory | B | those features were advertised for a 2015 app | implementation correctness / 2008 features |
| current App Store says platform began 2008 | retrospective | company product copy | C | candidate chronology | verified 2008 website state |
| app booking can exist without signed service agreement | 2017 | contemporaneous investigation | B, continuation | later order-contract gap | 2015 exact workflow |
| online match can fail because worker cannot physically reach home | 2020 | contemporaneous reporting | B, continuation | arrival / physical-access gap | 2008–2015 pandemic-like behavior |

---

# 18. What this changes in old-Web archaeology

家政平台要求我们给“交易型 Web”再加一条此前容易忽略的原则：

> **网页不是最终行为发生的场所，而是把两个陌生人送到同一扇门前的协调层。**

这意味着 Web artifact 的历史价值非常大，但 claim 必须停在它能证明的层级。

一个页面可以很好地证明：

- 哪种 worker identity 当时可以被搜索；
- 哪些技能被商品化；
- 哪些信任字段被展示；
- 哪些 availability 状态进入 UI；
- 用户被要求经过什么页面路径。

它通常不能证明：

- worker 当晚睡了几小时；
- household 最后有没有续约；
- 孩子实际由谁照护；
- worker 自己的孩子由谁照护；
- 这份 profile 最终有没有变成一段真实劳动关系。

这正是 old-Web 与 ordinary-life history 的接口位置。

---

# 19. Research gaps

1. 找到并实际验证 `www.96909.com.cn` 在 2008–2010 的 historical captures，记录 original URL、capture datetime、charset、页面结构和资源缺失。
2. 验证是否有 worker list / profile capture；若涉及真实普通人，先做 privacy minimization，不直接提交个人信息。
3. 查 `51baomu.cn` 最早可验证 historical capture，不把当前 App Store 的 2008 founding claim 当成 first-Web date。
4. 恢复 2010–2015 不同平台的 availability / booking / interview 字段差异。
5. 区分网站、WAP、iOS / Android app 与门店 backend，避免把多 surface 合成一个系统。
6. 查早期 Terms / contract help pages，确认平台到底是 employer、agency、membership intermediary 还是 information marketplace。
7. 寻找 contemporaneous browser / mobile requirements；本轮没有证据，不猜 IE 版本、ActiveX 或 charset。
8. 只在非识别化前提下研究 profile 半衰期：一个 `待岗` worker 状态平均多久失效。

---

## Final boundary

本文件允许的最强结论是：

> **2008–2015 中文网络逐渐把家政 worker 的身份、技能、可用状态、预约和远程筛选变成数字可见状态；但真正的合同、到家、劳动、休息、支付和长期关系大多留在公共 Web 之外。**

因此不要把一张历史 profile 写成一个普通人的完整工作史，也不要把 booking button 写成已经发生的照护。