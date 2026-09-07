# 公务员网上报名：职位表、资格审查、支付、准考证与最终录用之间的状态缺口（2004—2015）

> Scope：本 note 只研究约 2004—2015 中文 Web 与公务员招考事务的交界：职位公告、网上报名、资格审查、报名确认、支付、照片、准考证、成绩/面试名单与公示。1994 年考试录用制度建立属于理解这一 Web 事务的前史，放在 `how-people-lived`；本仓不扩成公务员制度史。

## 1. 为什么它值得 old-web archaeology 单独处理

公务员招考网页不是普通“信息页”。

它至少混合了三类不同对象：

1. **public information surface**：公告、职位表、报考指南、考试大纲、咨询电话；
2. **authenticated transaction surface**：注册、报名、选择职位、查询资格审查、报名确认、上传照片、缴费、准考证；
3. **downstream offline/institutional state**：真实到场考试、资格复审、面试、体检、考察、公示、录用和到岗。

因此一个保存完整的招考公告，只能证明“当时公开了这些规则/locator”，不能证明真实报名后台仍可复原，更不能证明某个报名记录最后变成一份工作。

本 note 的核心状态链是：

`announcement published`

→ `position table available`

→ `candidate can access registration host`

→ `account/application created`

→ `one position submitted`

→ `recruiting agency receives application`

→ `qualification review passed`

→ `registration number available`

→ `confirmation required`

→ `photo accepted`

→ `payment gateway success`

→ `exam-system payment state reconciled`

→ `admit card printable`

→ `candidate actually attends`

→ `written score`

→ `interview shortlist`

→ `candidate confirms interview`

→ `original documents rechecked`

→ `interview / professional test`

→ `physical examination / inspection`

→ `proposed-hire list`

→ `formal employment / actual reporting for duty`。

每个箭头都可能断。

---

## 2. 2004：网上报名已经存在，但确认仍然需要身体到场

2004 年 10 月的人事部 2005 年度中央、国家机关招考流程已经要求考生通过人事部网站提交报名。

但网上申请之后，通过报名的考生仍须在 11 月 5—6 日到所选省会/直辖市的指定地点办理确认。同期说明要求本人携带：

- 身份证、学生证等有效证件；
- 两张一寸照片；
- 考务费用；
- 领取准考证主证；
- 填写寄送公共科目笔试成绩的信封。

本人无法到场时还可以委托他人，但代办人要同时携带双方证件。

历史 locator：

`www.mop.gov.cn/2005gwy/default.asp`

因此 2004 年不能写成：

> “中央公务员考试已经实现网上报名，所以报名流程已经数字化。”

更准确是：

`Web application → offline confirmation → physical ID/photo/payment → paper/mail artifacts`。

### 新 gap：application / confirmation gap

`报名表已经在 Web 提交`

不等于：

`报名资格已经最终确认`。

来源：

- 中新网同期稿，新浪转载，2004-10-29：https://finance.sina.com.cn/towork/20041029/10301118469.shtml
- 2005 年度招考公告同期全文：https://www.chinanews.com.cn/news/2004/2004-10-14/26/494049.shtml

**Evidence：A-content / B；confidence: high。**

---

## 3. 2005—2006：网络报名统一了，确认却按地区分裂成 online/offline 两种路径

2006 年度中央、国家机关招考公告明确：

- 报名全部采取网络报名，不设现场报名；
- 报考者只能选择一个部门或单位中的一个职位；
- 新旧两个身份证号码不能同时报名；
- 资格审查合格后不能再改报其他职位；
- “报名序号”是报名确认、准考证下载和成绩查询的重要 key；
- 报名推荐表、报名登记表仍从网站下载并打印。

但报名确认并未全国统一为在线事务。

北京、上海、天津、吉林、河北、山西、江苏、浙江、江西、福建、陕西等 11 个省市可在 `www.cpta.com.cn` 网上确认：上传电子照片、网上缴费；其他考区仍需现场确认和缴费。

历史报名 host 又包括：

`gwy2006.mop.gov.cn`

这说明同一年度、同一个国家级招考，可以同时存在两种完全不同的末端操作路径。

### 新 gap：national-process / regional-execution gap

不能从一个北京考生的操作教程外推全国。

同一制度 label 下至少要记录：

- 年度；
- 考区；
- 是否网上确认；
- 支付渠道；
- 照片要求；
- 现场证件要求。

### 新 gap：registration-number / person-memory gap

报名序号变成跨多个页面/阶段引用同一申请的事务键。

如果历史档案只保存公开公告，却没有保存用户本地抄写的报名序号、cookie/session 或认证后台，就不可能重放完整个人流程。

来源：

- 2006 年度招考公告同期转载：https://business.sohu.com/20051012/n240528095.shtml
- 新华社/中国青年报，2005-10-12：https://news.sina.com.cn/o/2005-10-12/05017144359s.shtml

**Evidence：A-content / B；confidence: high。**

---

## 4. 一条值得保留的 URL/locator 转换

这一时期至少出现过以下 locator：

- `www.mop.gov.cn/2005gwy/default.asp`
- `gwy2006.mop.gov.cn`
- `www.cpta.com.cn`
- 各省人事考试网站

因此“公务员网上报名系统”不是一个稳定 URL。

站点品牌/制度连续，并不意味着：

`host continuity`

或：

`application continuity`。

### 新 gap：annual-host / institutional-continuity gap

年度专题 host 非常容易在当年事务结束后失效、改版或被新系统替代。

后来的当前站点即使保存历年公告，也不应被误认为原始报名 backend。

---

## 5. 2006—2008：电子照片与网上支付把客户端环境、银行和招考后台接进同一事务

2007 年安徽考区的 2007 年度网上确认说明要求考生已经通过人事部/海关报名资格审查，并准备：

- JPG 电子照片；
- 特定尺寸/大小范围；
- 工商银行或建设银行的可网上支付银行卡。

2007 年江苏的 2008 年度确认说明更明确：

- 2 寸电子证件照；
- JPG；
- 20KB 以下；
- 银行卡需开通网上支付。

这意味着一个“符合公务员报考资格”的人，在网上确认阶段还要额外满足：

`有可用电脑/浏览器 + 有符合规范的照片文件 + 会处理图片 + 有可在线支付银行卡 + 银行支付页面可用 + 招考系统能接收回执`。

不能从法律/职位资格直接跳到数字事务可执行性。

### 新 gap：policy-eligible / client-executable gap

“可以报考”与“这台机器现在能完成确认”是两个状态。

来源：

- 安徽 2007 年度确认说明：https://www.eol.cn/gongwuyuan/guojia/200610/t20061010_199562.shtml
- 江苏 2008 年度确认报道：https://edu.sina.com.cn/official/2007-11-08/1345107319.shtml

**Evidence：B，来源内容来自地方考试中心/考务说明；confidence: high。**

---

## 6. 最有价值的 old-Web 状态缺口之一：银行已经成功，报名系统还不知道

江苏 2008 年度网上确认同期说明保存了一个很具体的异常：

如果支付页面提示支付成功，但报名确认系统显示缴费不成功，考生不应再次支付，而要等待当天晚上系统“同步对账”；对账后报名系统状态才会更新。

这是一条非常强的技术—生活证据，因为它证明：

`bank payment state = success`

与：

`exam registration state = paid`

在现实中可以短时间不一致。

### 新 gap：payment-gateway / exam-ledger reconciliation gap

旧网事务考古不能看到一个“支付成功”截图就宣布报名完成。

至少要区分：

- 用户浏览器看到的银行返回页；
- 银行账务状态；
- 支付接口返回；
- 招考系统本地缴费字段；
- 夜间或批次对账后的最终状态。

这与电商、网银、考试报名等其他中文旧网事务具有很强的可比较性。

来源：

- 江苏 2008 年度国考网上确认同期报道：https://edu.sina.com.cn/official/2007-11-08/1345107319.shtml

**Evidence：B；confidence: high。**

---

## 7. 2008—2009：资格审查通过 ≠ 参加考试

2009 年度招考约有 77.5 万名考生获得参加笔试的资格，但现场仍出现明显缺考。

因此任何历史数据集如果只保存：

`application record`

或：

`qualification-approved record`

都不能自动写成“此人参加了公务员考试”。

### 新 gap：qualified / confirmed / attended gap

真实分母至少可以包括：

1. 报名申请；
2. 通过资格审查；
3. 完成报名确认/缴费；
4. 实际到达考场。

这些值的差异本身就是生活选择：有人临时找到别的工作，有人放弃，有人无法出行，有人只是把报名当一个备选项。但具体原因通常不会进入官方公开记录。

来源：

- 2009 年度国考河南考区同期报道：https://edu.sina.com.cn/official/2008-12-05/1628177666.shtml

**Evidence：B；individual reasons mostly unknown。**

---

## 8. 面试阶段再次从 Web 退回电话和纸证

国家统计局 2008 年公务员面试公告提供了一个非常清楚的后半段事务：进入面试名单的考生，需要在 2 月 14—15 日之间通过电话确认；逾期不确认视为自动放弃，后续考生按成绩递补。

面试又可能要求身份证、学生证/工作证、学校盖章推荐表、单位同意报考证明、报名登记表等原件或纸件。

因此：

`名字出现在 Web 面试名单`

不等于：

`本人已经接受面试机会`。

### 新 gap：shortlist / acceptance gap

### 新 gap：online-record / original-document gap

前台数据库可以先让一个人通过资格审查；真正进入面试时，纸质/原始材料仍可能再次决定该状态是否有效。

来源：

- 国家统计局 2008 年面试公告：https://www.stats.gov.cn/fw/gwyzl/zlgg/202302/t20230215_1906158.html
- 2006 年度招考公告同期转载：https://business.sohu.com/20051012/n240528095.shtml

**Evidence：A-content。**

---

## 9. 2009：照片格式已经是可观察的客户端合同

宁夏 2009 年度考区网上确认要求上传近期免冠 2 寸证件照，JPG，20KB 以下，并在线支付考务费。

浙江同期系统进一步给出像素范围与比例：最小约 80×110、最大约 200×280，建议 100×140，20KB 以下。

这类规格不是无关紧要的页面细节。

对一个 2008 年普通用户，它可能意味着：

- 去照相馆要电子版；
- 用图片软件缩图；
- 找会处理文件的人帮忙；
- 在网吧/学校机房把照片复制到报名电脑；
- 因文件大小/尺寸不符反复上传。

但本轮没有找到足够好的同时代第一人称材料证明这些动作的频率，所以这里只能记录 **client-side requirement**，不能把推断写成普遍体验。

来源：

- 宁夏 2009 年确认说明：https://edu.sina.com.cn/official/2008-11-03/1629173130.shtml
- 浙江 2009 年确认说明：https://edu.sina.com.cn/official/2008-11-03/1600173117.shtml

**Evidence：B；behavioral inference: D。**

---

## 10. 2010s：职位表与资格条件越来越适合被结构化搜索，但“匹配”不是录用

到 2010s，国考年度专题已经形成非常稳定的逻辑结构：

- 公告；
- 招考简章/职位表；
- 报考指南；
- 考试大纲；
- 网上报名；
- 资格审查状态；
- 报名确认与缴费；
- 准考证；
- 成绩；
- 调剂；
- 面试公告；
- 拟录用公示。

职位表中的年龄、学历、学位、专业、工作经历、基层项目经历等字段，开始构成一种 **structured eligibility surface / 结构化资格表面**。

第三方教育网站也据此发展出职位筛选、报名入口聚合和考试资讯页。

但这不意味着第三方页面、职位筛选器与官方事务后台是同一个系统。

### 新 gap：third-party-discovery / official-transaction gap

用户可以在新浪、中国教育在线、培训机构等页面看职位、讨论竞争比、下载资料；真正提交申请和改变报名状态的仍是官方报名系统。

这也影响历史保存：第三方“入口页”往往比年度官方 backend 活得更久，于是后人容易高估第三方页面在事务中的权威性。

---

## 11. 公开名单的保存会制造一种历史可见性偏差

公务员招考特别容易留下：

- 招考公告；
- 职位表；
- 面试名单；
- 调剂名单；
- 拟录用公示；
- 录用政策。

却很难留下：

- 报名后为什么放弃；
- 资格审查失败者当时如何理解原因；
- 备考用了多少个月；
- 家庭是否提供生活费；
- 是否同时投企业/考研；
- 某次失败以后是否换职业；
- 考上后为什么主动不去。

### 新 gap：public-roster / lived-career gap

未来研究者如果只依赖政府 Web archive，会天然看见“成功进入下一状态的人”，却更难看见大量退出、失败、改路和从未完成 transaction 的生活。

这与 `how-people-lived` 的核心问题直接交叉：

> **制度记录特别擅长保存“一个人被系统识别成什么”，不一定保存“这个人最后怎样活”。**

---

## 12. 对 old-Web archive 的具体技术含义

要复原一个 2005—2010 的公务员报名案例，至少需要区分：

### public page

- announcement HTML；
- job list（HTML/Excel/ZIP/Word）；
- guide；
- help/FAQ；
- contact list。

### authenticated page

- registration/login form；
- one-position selection；
- qualification-review status；
- registration number；
- photo upload；
- confirmation；
- payment redirect/callback；
- admit-card page。

### external dependencies

- bank online-payment gateway；
- local provincial personnel-exam site；
- identity/document checks；
- printer/PDF/HTML print behavior；
- telephone confirmation；
- offline exam venue。

因此一份 WARC 如果只抓到公共公告，不能写“公务员报名系统已保存”。

---

## 13. 本轮明确的 state gaps

- `announcement-visible / effective-position gap`
- `position-match / applicant-eligibility gap`
- `application-submitted / qualification-passed gap`
- `qualification-passed / confirmation-completed gap`
- `national-process / regional-execution gap`
- `policy-eligible / client-executable gap`
- `photo-selected / upload-accepted gap`
- `payment-gateway / exam-ledger reconciliation gap`
- `qualified / confirmed / attended gap`
- `admit-card-generated / actually-printed gap`
- `written-pass / interview-shortlist gap`
- `shortlist / acceptance gap`
- `online-record / original-document gap`
- `interview-passed / physical-exam / inspection / final-hire gap`
- `public-roster / lived-career gap`
- `annual-host / institutional-continuity gap`
- `third-party-discovery / official-transaction gap`

---

## 14. Browser / encoding / archive assumptions

### 已证实

- 2004 年已有中央招考 Web 报名 + 现场确认混合流程；
- 2005 年为 2006 年度招考时已全部网络报名；
- 11 个省市先实行网上确认/支付，其他考区仍现场确认；
- 2007—2009 多地网上确认使用 JPG 电子照片和网上支付；
- 至少有一期明确存在“银行支付成功但报名系统待夜间对账”的异步状态；
- 年度系统使用过 `mop.gov.cn`、`gwy2006.mop.gov.cn`、`cpta.com.cn` 及地方考试站等多个 host。

### 高概率但本轮未验证原始 capture

- 年度专题与报名后台很可能存在 ASP/JSP/动态 session 等当时常见的服务端状态；
- 不同考区的页面实现、支付银行、照片验证和浏览器兼容性可能不同；
- 高峰报名期间可能存在拥堵/超时，但具体年份与技术表现不能从报名人数直接推断。

### 不知道

- `www.mop.gov.cn/2005gwy/default.asp` 原始 HTTP headers、charset、DOM、CSS、JS；
- `gwy2006.mop.gov.cn` 原始登录/报名 form 与 session/cookie；
- `www.cpta.com.cn` 当年确认/缴费 callback 的真实实现；
- 银行支付返回使用 GET/POST、服务器回调还是批处理文件；
- 夜间同步对账的协议、批次格式和数据库字段；
- 原始准考证打印页面的 HTML/PDF/ActiveX/打印 CSS；
- 是否存在 IE-only、ActiveX、特定 TLS/证书链依赖；
- 2004—2010 各时点的 GB2312/GBK/UTF-8 真实 charset；
- 认证页是否进入 Wayback/Common Crawl，以及是否因 session/robots 被系统性排除。

---

## 15. M1 状态

**M1 = NOT ACHIEVED IN THIS SLICE.**

本轮取得的是：

- 同期公告/操作说明；
- 政府/机构 current pages carrying historical-dated content；
- 同期媒体转载；
- 明确的历史 host/URL locator；
- 用户操作规则、照片格式和支付异常说明。

但本轮**没有实际取得并检查**一份满足本仓合同的 2004—2010 公务员报名系统 Wayback/WARC response。

因此不能写：

- “2006 年报名页就是今天能看到的这个样子”；
- “当年一定用 IE”；
- “某个动态 form 已被 archive 保存”；
- “Wayback 没有该系统”。

正确措辞只是：

> **本轮尚未验证历史 capture。**

---

## 16. 隐私与再发布边界

公务员面试/拟录用公示可能包含普通人的姓名、准考证号、毕业院校、单位等个人信息。

即使历史页面仍可获得，本仓也不应为了“完整复原”批量重新发布名单。

研究平台结构时优先保存：

- 字段 schema；
- 列表布局；
- 状态机；
- 公开政策；
- 必要的统计；
- 最小化、已公开且对 claim 必需的个案。

不要把一批二十年前普通考生重新变成可检索数据集。

---

## 17. 与 how-people-lived 的交叉结论

companion：

`topics/civil-service-exams-stability-option-windows-and-career-reentry-china-1994-2026.zh-CN.md`

old-Web 这一侧改变的不是“公务员为什么稳定”，而是一个更窄也更可验证的问题：

> **Web 把一条职业路线拆成了一串可查询、可提交、可支付、可打印的状态；但一个人真正得到工作，仍然要穿过电话、纸证、考场、面试、体检和现实迁移。历史档案通常保存前台规则，最容易丢掉的恰恰是那些真正决定事务有没有完成的认证后台和退出原因。**

本轮是实质新增，不计入连续无新增饱和次数。