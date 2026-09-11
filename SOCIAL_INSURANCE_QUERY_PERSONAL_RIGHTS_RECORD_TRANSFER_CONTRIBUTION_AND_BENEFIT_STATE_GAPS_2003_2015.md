# 社会保险网上查询、个人权益记录、转移接续与待遇状态差（2003–2015）

> Scope：本 note 只研究约 2003–2015 中文互联网中的劳动/社会保障公共服务入口、个人社保查询、个人权益记录、缴费证明与养老保险关系转移，以及这些 Web 页面与电话、自助终端、纸质对账单、地方经办数据库之间的边界。1990s 制度和第一张社保卡只作为理解 Web 前史的必要背景；2016 以后全国统一平台只用于说明后续演变，不把本仓扩成社会保障制度史。

Cross-repo：生活史解释见 `tmzncty/how-people-lived`：  
`topics/from-work-unit-retirement-records-to-online-social-insurance-portability-benefit-continuity-and-future-rights-visibility-china-1991-2026.zh-CN.md`

## 0. 为什么这个对象值得单独建 note

本仓已经有网银转账、信用报告、公务员网报、消费者投诉、法律援助、医疗、校园一卡通等事务状态专题，但此前没有把“社保网页里显示的一条记录”与现实参保、缴费、转移和未来待遇拆成独立对象。

这种历史页面特别容易产生两种误读：

> “2011 年网上已经能查社保，所以当时每个人都可以随时确认自己的全部社保。”

以及：

> “网页里显示了某月缴费，所以这条养老权益已经全国可携带、未来退休时一定有效。”

现实至少可能经过：

```text
worker enters job
→ employer registers worker
→ employer declares contribution base
→ contribution is paid
→ local social-insurance database records month
→ worker obtains/query identity
→ worker authenticates
→ web/phone/terminal returns record
→ worker notices discrepancy
→ correction request
→ local agency verifies/corrects
→ worker changes job/city
→ transfer request
→ destination agency accepts
→ source agency transfers record/funds
→ destination agency merges years/account
→ later retirement eligibility check
→ benefit calculation
→ actual benefit payment
```

因此本 note 的核心合同是：

> **public Web shell != authenticated personal record != authoritative legal record != successful transfer != future benefit entitlement**

---

## 1. 研究单位必须拆开

至少区分：

1. **physical worker / insured person**：现实劳动者/参保人；
2. **employment spell**：现实某段工作经历；
3. **employer registration**：用人单位参保登记；
4. **contribution declaration**：单位申报的缴费基数与月份；
5. **actual contribution payment**：真实缴费到账；
6. **local social-insurance record**：地方经办系统内的参保/缴费记录；
7. **social-security number / card**：身份与服务凭证；
8. **Web account / personal user**：网上平台个人账号；
9. **authentication state**：身份证号、社保卡号、密码、验证码/数字证书等身份校验；
10. **query request**：用户发起的查询；
11. **query result**：网页/电话/终端返回的数据；
12. **annual statement / personal-rights record**：年度对账单/个人权益记录；
13. **printed proof**：打印的制式社保证明；
14. **verification serial / code**：证明真伪校验状态；
15. **correction request**：对错误记录提出的核查/变更申请；
16. **transfer application**：养老保险关系转移申请；
17. **source-agency processing**：原参保地转出；
18. **destination-agency acceptance**：新参保地接收；
19. **merged contribution years/account**：年限与账户最终合并；
20. **retirement eligibility**：未来待遇领取资格；
21. **benefit calculation**：待遇核定；
22. **actual payment**：现实养老金/待遇到账；
23. **12333 call state**：电话自助/人工查询状态；
24. **self-service terminal session**：线下自助终端会话；
25. **mailed paper statement**：邮寄纸质对账单；
26. **archive capture**：档案保存的公开网页表示。

永久保持：

```text
worker != Web account
Web account != social-insurance relationship
employer declaration != money actually paid
query result != guaranteed-correct legal record
paper printout != future benefit entitlement
verification code valid != document remains verifiable forever
transfer application != transfer completed
source marked transferred-out != destination successfully received
multi-location display != merged account
social-security card != nationwide seamless portability
archive capture != private authenticated session
```

---

## 2. 前史边界：Web 没有发明社会保险记录，数字化先发生在后台

1997 年国务院《关于建立统一的企业职工基本养老保险制度的决定》已经要求建立企业职工基本养老保险个人账户。这个制度层显然早于大规模个人 Web 查询。

- **A / contemporaneous regulation**  
  https://www.nmg.gov.cn/zwgk/zfgb/1997n_5293/199709/199707/t19970716_309391.html

1999 年上海发出全国第一张社会保障卡。人社部后来的官方回顾特别值得 old-Web 研究注意：筹备过程中，不同部门需要整理积累多年的数据疏漏，并改造各自系统以支持卡片。

- **B / official retrospective**  
  https://chinajob.mohrss.gov.cn/c/2022-06-10/352279.shtml

因此前史边界是：

```text
paper/work-unit record
→ local administrative database
→ IC card / local information integration
→ telephone / self-service query
→ Web query
→ later national Web aggregation
```

不能把“个人能在网页上查”当成数字社保的起点。

---

## 3. 2003：12333 是一个与 Web 并行、而且长期保留的重要入口

2003 年 5 月 27 日，劳动和社会保障部发布劳社部函〔2003〕84号，规定全国统一劳动保障电话咨询服务号码为 **12333**，要求各地整合原有咨询系统，逐步以一个号码对外服务。

- **A / contemporaneous official notice**  
  https://www.mohrss.gov.cn/xxgk2020/fdzdgknr/zhgl/rlzyshbzxxh/202010/t20201031_394105.html

这个对象对 old-Web 的意义非常大：

> **Web archive 天生更容易留下网页，却会系统性低估电话作为同一公共服务系统的重要性。**

2003–2015 的社会保障数字服务不能只写成网站史，而应写成 channel stack：

```text
窗口
+ 电话 12333
+ 邮寄纸质记录
+ 自助终端
+ Web
+ 单位人事
+ 后期手机 APP / 微信
```

任何只依赖网页 archive 的历史，都可能把当时大量不经过 Web 的真实查询行为直接删掉。

---

## 4. 2011：exact historical original URL 已知，但历史 DOM 仍未核验

2011 年一个同时代个人博客明确记录北京市社会保险网上办事大厅：

```text
http://www.bjld.gov.cn/csibiz/home/
```

并说明可以查询个人社会保险缴费情况。

- **B / contemporaneous user documentation**  
  https://blog.sina.com.cn/s/blog_561be372010114tn.html

另有同时期/后来沿用资料进一步保留 `cardbiz` 等旧路径，但目前不能仅靠二手说明重建网页形态。

### 当前可支持

- 2011 年该 original URL 已被普通用户当作北京社保网上办事大厅入口；
- 个人缴费查询能力在当时至少已经实际进入用户操作说明；
- 北京劳保/人社旧域名体系中 `csibiz` 是社会保险事务入口的一部分。

### 当前不能支持

- 2011 首页的准确 DOM、栏目顺序或 CSS；
- 登录表单真实 `action`；
- 当时使用什么 server-side framework；
- charset；
- 是否要求 IE-only、ActiveX 或特定控件；
- 个人登录后所有查询字段；
- 同一 URL 在 2010、2011、2013 是否使用同一实现。

### M1 capture 状态

本轮按 exact original URL 尝试定位 Wayback/CDX：

```text
http://www.bjld.gov.cn/csibiz/home/
```

但当前可用检索路径没有取得一份实际打开后可同时核验以下字段的 historical capture：

- `archive_source`
- `capture_url`
- `original_url`
- `capture_datetime`
- HTTP/replay state
- `Content-Type / charset`
- DOM/form action
- scripts/iframe/subresources
- second historical time point

因此严格记录：

> **M1 verified historical Beijing social-insurance Web capture: NOT ACHIEVED IN THIS SLICE.**

这不等于“Wayback 没保存”。只是当前 locator / replay 尚未达到本仓 METHOD 的 capture 验证门槛。

---

## 5. 2011：个人权益记录本身已经被定义成纸质 + 电子的长期事务对象

2011 年 7 月 1 日实施的《社会保险个人权益记录管理办法》明确：个人权益记录可以以纸质材料和电子数据等载体存在，内容包括登记、缴费、待遇资格/领取、缴费年限和个人账户等。

- **A / regulation**：人社部令第14号  
  https://www.moj.gov.cn/pub/sfbgw/flfggz/flfggzbmgz/201109/t20110920_145073.html

这给旧网研究一个关键边界：

> **网页只是个人权益记录的一种读取接口，不是记录本身。**

所以：

```text
HTML page disappears
!= social-insurance record disappears
HTML page survives
!= historical personal record survives in archive
```

真正长期存在的 authoritative state 位于社会保险经办系统，而不是公共网页 HTML。

---

## 6. 2013 北京：Web 查询已经是一个“定制—次日下载—30日验证”的事务状态机

北京市 2013 年关于统一规范个人权益记录查询的官方通知提供了非常强的 A 级状态材料。

它列出四类查询渠道：

1. 社保经办机构窗口；
2. 经办机构服务区自助终端；
3. 北京市社会保险网上服务平台；
4. 12333 热线（预计 2014 年 1 月启用个人权益查询）。

- **A / official Beijing notice, 京社保发〔2013〕45号**  
  https://rsj.beijing.gov.cn/yltc/sbzytzx/202311/t20231101_3292116.html

网上个人用户的状态链不是“打开网页 → 看到全部记录”，而是：

```text
register personal user
→ login succeeds
→ enter “个人权益记录” module
→ submit customization request
→ wait until next day in principle
→ download / print standardized record
```

通知还规定，打印出的个人权益记录可以通过查询流水号与校验码进行真伪校验，而且校验存在 **30 日**时间窗口。

这产生几个永久边界：

```text
query requested
!= record immediately generated
record downloadable
!= user actually downloaded
printout exists
!= verification window still open
verification succeeds in 2013
!= screenshot can be re-verified decades later
```

### verification-code expiry bias

如果未来 archive 保存了一张“社保证明”截图，其中带流水号和校验码，我们不能在多年后因无法校验就判断当年的证明是假的；30 日校验窗口本来就是系统状态的一部分。

反过来，即使截图视觉上非常像官方证明，也不能跳过当年的动态校验状态直接宣称其真实。

---

## 7. 2013–2014：多渠道并存，而且纸 → Web 的默认迁移改变了历史可见性

2014 年，北京仍向 823 万名参加五项社会保险的在职职工邮寄 2013 年度纸质对账单；但官方同时宣布，下一年度开始不再主动邮寄，参保人可以通过单位或社保网上平台选择获取方式，未选择者默认网上查询。

- **B / contemporaneous Beijing Morning Post report**  
  https://finance.people.com.cn/n/2014/0515/c1004-25018453.html
- **B / contemporaneous Beijing Daily report**  
  https://cpc.people.com.cn/n/2014/0515/c83084-25019369.html

这不是一个小的“无纸化”细节。它改变了记录如何进入普通人的日常：

```text
old default:
agency → mails statement → household receives paper

new default:
record exists → individual must authenticate/query/download
```

### paper-to-Web default migration bias

当制度从主动邮寄转向默认网上查询时：

- 数字技能强的人更容易持续主动核查；
- 不常登录的人可能长时间不看记录；
- archive 反而会保存更多公开“如何网上查”的教程；
- 私人对账单本身由于登录、隐私和个性化几乎不会进入 Web archive。

因此将来资料会产生一种悖论：

> **我们可能比 2014 年一个普通劳动者本人更容易看到当年的“查询说明页”，却永远看不到她当年真正看到的个人缴费记录。**

---

## 8. 2014：手机与微信进入，但不能把后来的 Web 兼容性要求投射回去

2014 年北京启动社保移动服务试运行，参保职工可以通过官方 APP / 微信服务号查询参保、缴费、社保卡进度、定点医院等信息。同期报道仍给出网上平台：

```text
http://www.bjrbj.gov.cn/csibiz/
```

- **B / contemporaneous report**  
  https://politics.people.com.cn/n/2014/0606/c1001-25111596.html

这说明服务形态已经从：

```text
Web only
```

进一步变成：

```text
Web + app + WeChat + phone + terminal + counter
```

但是今天打开现行北京社保平台，会看到 Chrome / Firefox / 360 / IE10+ 的浏览器提示：

- current site: https://rsj.beijing.gov.cn/csibiz/

**绝不能**把今天的浏览器提示倒推成 2011 或 2014 的浏览器要求。历史时期的 IE/ActiveX、charset、脚本、证书与登录实现仍必须等待真正 capture 或同时代技术文档。

---

## 9. “网页显示缴费”距离现实权益还有多远

在页面考古里，一行月份记录最容易让人产生错误确定感：

```text
2013-08  已缴
```

但真正状态至少还包括：

```text
employer declared wage base
→ agency accepted declaration
→ payment cleared
→ month stored in local record
→ query view generated
→ worker checks
→ worker disputes if wrong
→ agency reviews evidence
→ record corrected / not corrected
```

北京市 2013 规则明确规定，个人对权益记录有异议时，可以向参保地社保经办机构提出书面核查并提供证明材料；确有错误再按程序变更。

- **A / official rule; same evidence family as 2013 query notice**  
  https://rsj.beijing.gov.cn/yltc/sbzytzx/202311/t20231101_3292116.html

因此：

> **queryability is not correctness。**

Web 的重要贡献之一恰恰是让本人更早发现错误，而不是保证数据库不会错。

---

## 10. 跨地区转移：Web 页面只显示事务的一部分

2009 年底《城镇企业职工基本养老保险关系转移接续暂行办法》正式建立跨省关系转移规则，自 2010 年起实施。

- **A / contemporaneous rule**  
  https://www.beijing.gov.cn/zhengce/zhengcefagui/qtwj/201001/t20100101_781119.html

其事务逻辑至少包括：

```text
new-place participation established
→ transfer request
→ destination agency review
→ acceptance communication
→ source agency handles transfer
→ relationship / funds sent
→ destination receives
→ destination completes merge
→ person / employer receives confirmation
```

这意味着一个旧网页若只有“转移申请”按钮，不能支持“网上一键把养老保险转过去了”的叙述。

永久保留：

```text
application submitted
!= destination accepted
!= source record found
!= source transferred
!= destination received
!= contribution years merged
```

后来的 2022 个案甚至显示，一条十多年前的“转出”状态仍可能没有清楚接收端。这是后续生活史证据，不用于扩大本 note 的时间 scope，但它证明上述状态差并非纯工程想象。

- cross-period validation: https://sx.people.com.cn/n2/2022/0215/c189132-35134585.html

---

## 11. 第三方查询工具：`convenient interface != public-agency interface`

Web/移动查询成熟以后，还会出现第三方代查、聚合或“掌上社保”类工具。2019 年北京官方曾转发风险提示，针对第三方“社保掌上通”等应用收集用户信息、通过第三方服务器访问官方社保系统的做法，提醒用户优先使用人社部门官方网站、12333、官方微信和自助终端等渠道。

这超出本 note 主时间范围一点，只作为 2003–2015 演变后的验证：

```text
looks like social-insurance query
!= operated by social-insurance agency
third-party login screen
!= official authentication endpoint
data shown by proxy
!= proof that agency directly exposed API to user
```

旧网页/截图考古如果没有确认域名、运营主体和网络路径，很容易把第三方壳误认成公共机构原始界面。

---

## 12. Archive preservation biases

### 12.1 `public-shell / authenticated-state asymmetry`

最容易保存：

- 官网首页；
- 办事指南；
- 公开政策；
- 查询入口按钮；
- 注册说明；
- 12333 号码；
- 软件下载/二维码说明。

最不容易保存：

- 登录后的个人权益记录；
- 身份证号/社保卡号绑定；
- 每月真实缴费；
- 转移申请与审核进度；
- 纠错材料；
- 未来待遇核定。

这不是 archive 偶然失误，而是服务本身的隐私和登录结构决定的。

### 12.2 `query-interface survival / legal-record-state loss`

我们可以恢复“2013 年网页允许查什么字段”，却不能从公共 archive 重建某个普通人的 authoritative record。

### 12.3 `multi-channel survival asymmetry`

Web archive 会系统性低估：

- 12333 电话；
- 现场窗口；
- 单位人事代办；
- 自助终端；
- 纸质邮寄对账单。

如果只看网页，容易误判“互联网是唯一主渠道”。

### 12.4 `statement-shell survival / contribution-state loss`

页面也许保存了“养老保险历年对账单查询”按钮，但后台数据库、个人账号、当年月份和真实缴费基数不会随按钮一起保存。

### 12.5 `verification-window loss`

证明上的查询流水号/校验码具有时限。多年后的静态截图不能恢复当年的实时校验能力。

### 12.6 `paper-to-Web selection shift`

2014 后默认从纸质主动邮寄向网上查询迁移，会改变谁更可能实际看到并保存自己的记录。历史材料中的“数字用户”因此可能比总体参保人口更可见。

---

## 13. 浏览器、charset、后端与安全假设

### 已知

- 2011 同时代用户材料给出 exact original URL：`http://www.bjld.gov.cn/csibiz/home/`；
- 2013 北京官方文件明确网上平台存在个人注册、定制查询与验证模块；
- 2013–2014 同时代资料给出 `http://www.bjrbj.gov.cn/csibiz/`；
- 2014 官方移动服务与 Web 并存。

### UNKNOWN，禁止自行补全

- 2011/2013 exact charset；
- 是否 IE-only；
- 是否 ActiveX；
- 登录控件具体实现；
- server-side framework；
- Session/cookie 机制；
- HTTPS/TLS 历史状态；
- 验证码实现；
- 2011 与 2013 是否同一代码库；
- archive rewrite 是否会破坏登录/JS。

现行网站的 Chrome/Firefox/IE10+ 提示只能证明**今天**的兼容性说明，不得作为历史证据。

---

## 14. Evidence table

| Claim | Evidence | Grade | Confidence |
|---|---|---:|---:|
| 12333 在 2003 被确立为全国劳动保障咨询统一号码 | 人社部劳社部函〔2003〕84号 | A | high |
| 2011 北京旧域名 `bjld.gov.cn/csibiz/home/` 被用户用于个人社保查询 | 同时代新浪博客 | B | medium-high |
| 个人权益记录法定包含纸质/电子登记、缴费、待遇、年限、个人账户 | 人社部令第14号 | A | high |
| 2013 北京存在窗口/终端/Web/12333 多渠道查询 | 北京官方经办通知 | A | high |
| Web 查询采用“定制—次日下载”且证明可限时校验 | 同上 | A | high |
| 2014 北京仍大规模邮寄纸账单，次年默认转网上 | 同时代北京晨报/北京日报 | B | high |
| 2014 APP/微信已加入个人社保查询栈 | 同时代新京报 | B | high |
| 2010 起跨省养老保险关系有正式转移接续程序 | 国办发〔2009〕66号 | A | high |
| 2011–2014 历史 DOM / charset / IE requirement | 未取得合格 capture | — | unknown |

---

## 15. 已证实 / 高概率 / 不知道

### 已证实

- 2003 后 12333 构成 Web 之外的重要统一公共入口；
- 2011 同时代资料已经给出北京社会保险网上办事大厅 exact original URL；
- 2011 法规正式把纸质与电子数据共同定义为个人权益记录载体；
- 2013 北京网上个人权益记录并非静态页面，而有账号、定制、等待、下载、打印、校验等状态；
- 2013–2014 Web、电话、自助终端、窗口和纸质对账单并存；
- 2014 前后纸质默认获取方式开始明显向电子渠道迁移；
- 养老保险跨省转移的真实状态远多于一个“提交”按钮。

### 高概率但仍需历史 capture/更多原始材料

- 2010–2013 `csibiz` 页面形态、栏目与登录逻辑经历过多次调整；
- 登录后的个性化页面比公开说明页更难被公共 archive 保存；
- 早期用户对社保 Web 的真实使用强烈受单位人事、城市、年龄和数字技能影响。

### 不知道

- 2011 首页/登录页精确 DOM；
- charset 与浏览器依赖；
- 哪些 JS/iframe/子资源能在 archive 完整回放；
- 2011–2014 各类用户 Web 查询占全部社保查询的比例；
- 普通参保人发现错误后实际纠错成功率；
- 当年动态 transfer/account state 是否存在任何可合法公开的匿名历史样本。

---

## 16. 隐私与版权边界

社保历史页面尤其需要严格最小化。

不要重新公开：

- 姓名 + 身份证号；
- 社会保障号/卡号；
- 个人缴费明细；
- 医保待遇信息；
- 地址/单位与完整身份组合；
- 可用于登录/验证的密码、流水号、校验码；
- 私人历史 PDF/截图中的敏感字段。

研究重点应放在：

- URL pattern；
- 页面/流程 schema；
- 登录前公开帮助；
- 字段类型；
- 状态机；
- archive gap；
- 渠道关系；
- 同时代公开制度说明。

**historically public or leaked != ethically necessary to republish now**。

---

## 17. 与 how-people-lived 的交叉解释

旧网这一侧最重要的生活史含义不是“北京 2011 年已经有一个社保网站”，而是：

> **一个人的福利历史逐渐从单位和经办柜台里的不可见后台，变成本人可以主动核查的长期记录。**

这会改变换工作的风险感知：

- 以前更依赖单位人事告诉你“交了”；
- 后来本人可以查到月份和对账单；
- 再后来跨地区关系可以在线申请转移并查看进度；
- 但 Web 始终只是一层接口，真实权益仍取决于后台记录是否完整、跨地是否接上、错误能否纠正。

这正是为什么旧网页考古必须拒绝：

```text
button survived
therefore transaction succeeded
```

更准确的结论是：

> **公开 Web 留下了“普通人当年可以怎样尝试理解自己的社会保险”的外壳；真正决定几十年后生活的那份个人制度记忆，大部分从一开始就不属于公开 Web。**
