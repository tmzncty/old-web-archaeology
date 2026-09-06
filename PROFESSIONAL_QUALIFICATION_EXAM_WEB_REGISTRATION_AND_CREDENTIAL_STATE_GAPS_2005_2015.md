# 职业资格考试旧 Web 报名与证书状态缺口（2005–2015）

> Scope：只研究约 2005–2015 中文 Web 中，职业资格 / 专业技术资格考试怎样被网页化、怎样跨过 Web 与现实审核边界，以及 archive 今天最容易误读哪些状态。职业资格制度的 1990 年代前史与跨国比较主要放在 `tmzncty/how-people-lived`。

Cross-reference:

- `tmzncty/how-people-lived/topics/professional-qualification-exams-credential-optionality-and-exam-executability-china-1993-2026.zh-CN.md`

## 1. 研究问题

今天看到一条 2007 年“网上报名”新闻，很容易下意识把它理解成现代意义上的：

```text
打开网站
→ 填表
→ 付款
→ 报名成功
```

同期材料显示，实际流程经常远比这复杂：

```text
announcement page
→ registration endpoint
→ account/session
→ personal data
→ photo upload
→ preliminary submit
→ print form
→ employer verification / seal
→ in-person qualification confirmation
→ online or offline payment
→ registration accepted
→ admit card
→ physical exam
→ score query
→ post-exam qualification review
→ certificate issuance
```

因此本 note 的核心边界是：

> **“网上报名”只能证明流程中至少有一个 Web state，不能自动证明整次报名 transaction 已经在线闭合。**

同样必须区分：

```text
报名页存在 ≠ 报名端点当时可用
提交表单 ≠ 服务器接受
服务器接受 ≠ 资格审核通过
资格审核通过 ≠ 缴费完成
缴费完成 ≠ 报名状态完成
打印准考证 ≠ 实际到场
成绩合格 ≠ 资格复核通过
资格复核通过 ≠ 证书已制发
证书已制发 ≠ 雇主实际认可/录用
```

## 2. 研究单位

依据 `docs/METHOD.md`，本题必须至少拆成：

- **platform / service**：某省/市人事考试平台、全国专业技术人员资格考试报名服务平台；
- **site / host**：例如 `www.21wecan.com.cn`、`www.gdkszx.com.cn`；
- **announcement page**：考试通知、报考简章、流程说明；
- **registration page**：实际表单、登录、照片上传；
- **account/session**：用户身份、登录态、报名记录；
- **transaction**：一次具体报名、审核、缴费或查询；
- **result page**：成绩、资格复核、证书状态；
- **capture**：archive 保存的一次历史表示；
- **claim**：基于上述 evidence 的最小结论。

一个官方 host 真实存在，不等于其中某个 dynamic registration endpoint 已经被 archive 保存。

## 3. 2005–2006：从“网页告诉你怎么办”到“网页先收一部分材料”

### 3.1 2005：考试计划和表格可以先进入 Web，但仍不能推导全流程在线

2005 年上海统计专业技术资格考试的同期通知已经允许考生从上海统计网、上海职业能力考试网、21 世纪人才网获取通知、附件与有关表格。

这类证据最稳妥的 claim 是：

> **考试信息与表格已经具有 Web reachability。**

它不能自动升级成：

> “2005 年该考试已经端到端网上报名。”

本仓以后遇到 `download form`、`网上下载`、`表格下载` 等词时，都应单独标记为 **document availability state**，不能与 **transaction submission state** 合并。

### 3.2 2006 卫生专业技术资格：典型的 Web-pre-registration + paper/in-person backend

2006 年 11 月广东卫生专业技术资格考试通知明确：

- 考生登录中国卫生人才网 `http://www.21wecan.com.cn`；
- 在线填写个人申报资料；
- 下载打印申报表；
- 随后在规定日期到考点/报名点办理现场确认。

Source:

- https://news.sina.com.cn/o/2006-11-09/094010452869s.shtml

另一个 2006 年考务通知进一步保存了后台现实材料：打印的申报表需要单位核实并签字、盖章，现场审核还需要身份证、毕业证/学位证、既有资格证等原件，以及多张实体照片。

Source:

- https://www.sd-eh.com/index.php/portal/article/index/id/88.html

这里至少存在四种不同状态：

```text
web application filled
printed application produced
employer verified paper
registration point confirmed
```

如果 archive 只保存第一种页面，把它回放成“报名成功页”，会严重高估旧 Web 的 transaction closure。

## 4. 2007：照片上传、属地报名和现场确认让 state gap 更清楚

### 4.1 广东注册安全工程师

2007 年广东注册安全工程师执业资格考试通知把步骤写成：

```text
www.gdkszx.com.cn
→ 网上填表
→ 上传小于 50K 的彩色证件照
→ 选择属地报名点
→ 携带材料
→ 现场“报名确认”
```

Source:

- https://m.jianshe99.com/html/2007/3/pa715835495182370028910.html

这说明照片上传已经是报名系统内部 transaction 的一部分，但**照片成功上传仍然不是报名完成状态**。

### 4.2 浙江职称外语：online payment 是另一只钟

浙江财经大学 2007 年 12 月通知教职工参加 2008 年职称外语考试时，指向浙江人事考试网的具体 locator：

- `http://www.zjks.com/zjksweb/showInfo/Info.aspx?id=694`

并说明此次报名采用网上报名、网上交费。

Source:

- https://rsc.zufe.edu.cn/info/1068/2128.htm

这个 locator 很有研究价值，因为它保留了：

- `zjksweb` application path；
- ASP.NET 风格 `Info.aspx?id=...` dynamic URL；
- Web 信息页与实际报名/支付 endpoint 之间可能存在的进一步 handoff。

但本轮没有取得该 URL 的 verified memento，因此不能从 URL 风格推断原始 DOM、session、支付接口或浏览器要求。

## 5. 2008：旧 Web 报名已经很“复杂”，但仍然不是 today-like one-stop flow

### 5.1 广州注册结构工程师：网上预报名 / 现场确认是两个明确命名状态

2008 年广州注册结构工程师等考试规定：

- 从中国广州人事网 / 广州考试信息网进入报名系统；
- 网上填表；
- 上传小于 30K 的证件照；
- 完成“网上预报名”；
- 随后在小北路的实体报名点进行“报名确认”。

Source:

- https://www.eol.cn/hang_kao/jian_zao_di_chan/zhu_ce_jie_gou_gong_cheng_shi/kao_shi_dong_tai/200807/t20080701_305794.shtml

Historical host / locator family:

- `www.gzpi.gov.cn/gzexam`
- `www.gzexam.com.cn`

本题以后遇到 archive capture 时，必须检查页面究竟是：

- announcement；
- pre-registration form；
- confirmation instructions；
- success/receipt page。

不能只因为标题里有“网上报名”就把它们合并。

### 5.2 广州经济专业技术资格：Web transaction 会主动 hand off 到照相馆和工作单位

2008 年广州经济专业技术资格报名流程的同期保存非常适合建立状态机：

```text
联网电脑
→ 广州人事/考试网站
→ 注册 / 登录
→ “我的系统”
→ 专业技术资格考试系统
→ 个人基本信息 + 个人简历
→ 选择类别 / 地点 / 级别 / 科目
→ 打印照相凭条
→ 到指定照相馆
→ 照相馆把照片直接上传系统
→ 考生回到 Web 查询照片状态
→ 等待网上确认
→ 网上支付
→ 打印报名发证登记表
→ 工作单位审核盖章
→ 保存到未来办证
```

Source:

- https://www.chinaacc.com/new/15/22/48/2008/4/lu113513204413480024876-0.htm

这是一条非常重要的 **cross-organization transaction chain**：

Web 不只是连接用户和政府考试系统，还临时把：

- 照相馆；
- 工作单位；
- 支付；
- 未来发证

串进同一报名过程。

因此“报名系统”不能只按一个域名考古。

### 5.3 2008 厦门执业药师：网上报名、照片审核、现场资格审核、网上缴费、准考证、成绩查询彼此独立

厦门 2008 年执业药师考试简章保存了一条几乎完整的 lifecycle：

```text
www.fjpta.com 网上报名
→ 照片审核
→ 现场资格审核（新考生）
→ 网上缴费
→ 网上下载打印准考证
→ 实体考试
→ xmks.gov.cn 或 9622297799 查询成绩
```

Source:

- https://www.med66.com/html/2008/5/zh9255191239121580027562.html

Historical hosts:

- `www.fjpta.com`
- `www.xmks.gov.cn`

同时存在 Web 查询与电话信息台查询，本身就是一个重要提醒：

> **同一个考试的数字服务并不一定只有 Web 一条路径。**

## 6. 2009：成绩合格以后，Web 仍然可能把人重新送回纸面

广州市人事局 2009 年发布的 2008 年经济专业技术资格考试合格通知保存了一个后端状态：

- 2008 年已经在广州人事/考试网站网上报名；
- 成绩已经达到合格标准；
- 但仍须提交单位盖章的报名发证登记表、身份证、学历/学位、已有资格证和照片；
- 资格复核完成后才办理资格证书。

Source:

- https://rsj.gz.gov.cn/ywzt/rcgz/gzzc/tzgg/tzgg/content/post_2418023.html

因此 old-Web capture 若只保存：

- 报名成功页；
- 成绩查询页；
- 合格名单；

都不能直接证明某位考生最后取得证书。

这条状态必须拆成：

```text
exam_passed
post_exam_review_pending
post_exam_review_passed
certificate_pending
certificate_issued
```

## 7. 2014–2015：地方入口开始向全国统一报名平台汇聚，但现场审核没有立即消失

2014 年吉林多类专业技术资格考试已经使用全国专业技术人员资格考试报名服务平台：

- `http://zg.cpta.com.cn/examfront`

报名时仍涉及注册、照片上传、考区和考试选择；完成网上报名以后，考生仍须在指定日期去考试机构做资格审核确认。

Source:

- https://www.eol.cn/hang_kao/jian_zao_di_chan/zhu_ce_jian_zhu_shi/kaoshi_dongtai/201402/t20140210_1070972.shtml

该材料还明确要求某类省级报名系统使用 IE6 或 IE8，说明这一时期的 browser assumption 不能留空。

2015 年乌兰察布部分职业资格考试已经统一通过中国人事考试网 / 全国专业技术人员资格考试报名服务平台进行网上报名与网上交费，但资格审查仍在市人社局服务大厅完成。

Source:

- https://inews.nmgnews.com.cn/system/2015/07/09/011722641.shtml

由此出现一个新的考古问题：

> **旧地方考试站点被“统一平台”替代以后，地方 Web 留下的可能只剩公告壳，而动态 transaction 被迁入一个全国 host。**

如果只按地方域名统计 capture，会误以为“报名功能消失”；实际可能是功能被 centralize 了。

## 8. 状态机

### 8.1 Information state

```text
exam exists
announcement published
announcement indexed/searchable
eligibility rules available
registration dates visible
```

### 8.2 Account / identity state

```text
account not created
account created
identity submitted
identity accepted/rejected
old candidate / new candidate distinction
```

### 8.3 Application state

```text
form opened
form partially completed
photo absent
photo uploaded
photo rejected/accepted
application submitted
application editable/locked
```

### 8.4 Eligibility state

```text
web pre-check unknown
online review pending
online review passed
in-person review required
employer seal required
review failed / supplementary material required
```

### 8.5 Payment state

```text
not payable yet
payment initiated
bank/payment handoff
money deducted
platform confirmation pending
payment confirmed
registration complete
```

### 8.6 Examination state

```text
admit card unavailable
admit card printable
physical arrival required
identity checked
exam attended / absent
score pending
score published
```

### 8.7 Credential state

```text
score passed
post-exam review pending
review passed
certificate production pending
certificate issued
certificate collected/downloaded
credential queryable
```

### 8.8 Labor-market state — usually outside old-Web proof

```text
credential listed on CV
employer checked / did not check
credential required / preferred / irrelevant
job obtained / not obtained
```

最后这一层通常应由 `how-people-lived` 的劳动市场材料完成，不能由报名站点自己宣称。

## 9. 本题最重要的 state gaps

### 9.1 information-to-transaction gap

考试通知和“报名入口”链接存在，不代表服务器端 transaction 被 archive 捕获。

### 9.2 download-to-submission gap

下载报名表、打印申请表，只是 document state，不是提交成功。

### 9.3 pre-registration-to-confirmation gap

2006–2008 多个系统直接把两者命名成不同步骤。旧网页只留下 pre-registration 时，不能补写 confirmation outcome。

### 9.4 photo-upload gap

小于 30K / 50K 的照片要求说明 image upload 是 transaction 依赖；主 HTML 被保存并不代表上传 endpoint、照片处理或用户照片被保存。

### 9.5 web-to-offline-handoff gap

报名可能跳到：

- 单位人事部门；
- 照相馆；
- 人事考试中心；
- 现场审核点；
- 银行/支付系统；
- 电话信息台。

archive 如果只看 Web 会系统性低估这些外部节点。

### 9.6 score-to-certificate gap

成绩合格可能只是办证前一状态。广州 2008/2009 证据明确显示还有资格复核。

### 9.7 unified-platform migration gap

地方站点的报名功能迁到 `zg.cpta.com.cn/examfront` 后，本地页面可能从 transaction endpoint 退化为 announcement/router。

## 10. Archive preservation biases

### 10.1 public-announcement / private-application asymmetry

最容易保存：

- 报考通知；
- 考试时间；
- 条件；
- host / URL；
- 操作说明。

最难、也通常不应公开保存：

- 姓名与身份证号；
- 工作单位；
- 工作年限；
- 用户照片；
- 学历与既有证书；
- 登录 session；
- 付款信息；
- 个体审核结果。

因此 **public shell survives while private eligibility state disappears** 是这个题的结构性保存不对称。

### 10.2 success-state survivorship bias

“报名成功”“合格名单”“领证通知”比：

- 照片失败；
- 资格不符；
- 未缴费；
- 超时；
- 缺考；
- 资格复核失败

更容易进入公开页面。

如果只研究可见网页，会让旧考试系统看起来远比真实流程顺畅。

### 10.3 deadline-state collapse

报名系统强烈依赖时间窗。

同一个 URL 在：

- 报名前；
- 报名中；
- 截止后；
- 缴费期；
- 准考证期

可能呈现完全不同状态。

一份无日期或抓取时间不明的 archive replay 很难证明 historical usability。

### 10.4 browser-dependency bias

2014 吉林材料仍明确要求 IE6/IE8 处理部分报名流程。更早的 2005–2010 报名站点可能存在：

- IE-only JavaScript；
- ActiveX / local upload assumptions；
- GB2312/GBK；
- frameset / table layout；
- bank plugin；
- pop-up window；
- captcha/image dependencies。

在未验证旧浏览器前，现代浏览器打开一个历史 URL 不等于“当年页面就是这样”。

### 10.5 URL / domain continuity bias

品牌、主管机构、域名与系统后端可能分别迁移。

例如：

- `www.gzpi.gov.cn/gzexam`
- `www.gzexam.com.cn`
- `www.fjpta.com`
- `www.xmks.gov.cn`
- `www.gdkszx.com.cn`
- `www.21wecan.com.cn`
- `zg.cpta.com.cn/examfront`

这些字符串只证明具体时期有相关 locator；不能因为今天仍存在同品牌/相近域名，就自动认定 2008 后端连续运行至今。

## 11. Evidence table

| Evidence | Grade | Claim supported | Not supported |
|---|---|---|---|
| 2006 卫生资格网报通知 | A/B，同期官方通知经媒体/机构保存 | `21wecan.com.cn`、在线填表、打印、现场确认 | historical DOM、真实提交结果 |
| 2007 广东安全工程师通知 | B，同期考务材料保存 | `gdkszx.com.cn`、照片 <50K、现场确认 | 上传 endpoint、session、审核 backend |
| 2007 浙江职称外语通知 | A/B，机构同期通知 | `zjks.com/...Info.aspx?id=694`、网上报名/缴费 | 实际 payment transaction |
| 2008 广州结构工程师 | B，同期教育媒体保存 | 网上预报名、照片 <30K、现场确认 | 单个考生完成状态 |
| 2008 广州经济资格流程 | B，同期流程保存 | 登录、我的系统、照相馆上传、网上支付、单位盖章 | 原 DOM / HTTP / script behavior |
| 2008 厦门执业药师 | B，同期流程保存 | 网报、照片审核、现场资格、网付、准考证、Web/电话成绩查询 | 后端数据库与个体结果 |
| 2009 广州市人事局资格复核 | A，官方同期/近同期文件 | 成绩合格后仍需资格复核才能办证 | 每位合格者最终领证 |
| 2014 吉林报名通知 | B，同期官方材料转载 | 全国报名平台 + 现场确认、IE6/IE8 browser assumption | 全国所有考试同样要求 |
| 2015 乌兰察布公告 | B，同期地方公告 | 全国平台报名/网付 + 本地资格审查 | 全国所有地区完全统一 |

## 12. M1 状态：本轮仍然是明确的负结果

本轮已经定位到多组 historical host / path：

- `www.21wecan.com.cn`
- `www.gdkszx.com.cn`
- `www.zjks.com/zjksweb/showInfo/Info.aspx?id=694`
- `www.gzpi.gov.cn/gzexam`
- `www.gzexam.com.cn`
- `www.fjpta.com`
- `www.xmks.gov.cn`
- `zg.cpta.com.cn/examfront`

也有足够的同时代官方/媒体材料证明这些 locator 与对应报名流程曾经存在。

但是：

> **本轮没有实际打开并验证一份满足 M1 门槛的 2005–2010 中文职业资格考试报名 transaction Wayback/WARC capture。**

因此以下内容继续保持 `unknown`：

- historical HTML / DOM；
- HTTP Content-Type / charset；
- GET / POST；
- form action；
- account/session/cookie；
- captcha；
- photo upload endpoint 与返回状态；
- online payment handoff / callback；
- browser sniffing / ActiveX / plugin；
- qualification review backend；
- admit-card generation；
- score-query backend；
- certificate database handoff。

正确写法是：

> **candidate locator + contemporaneous workflow evidence, no verified transaction capture in this run**

而不是：

> “Wayback 没有保存这些系统。”

## 13. 隐私与研究边界

资格考试交易包含高敏感身份材料。本仓不因为 archive 或旧网页可能可访问就重新公开：

- 普通考生姓名；
- 身份证号；
- 报名号；
- 工作单位与履历；
- 照片；
- 成绩与资格审核状态；
- 联系方式。

技术研究优先保留 institution-level host、abstract URL pattern、form/state model 和公开操作说明。

## 14. 下一步最值钱的考古动作

1. 针对 `www.21wecan.com.cn` 2006 年卫生资格报名，寻找至少一个真实 registration memento，并验证主 HTML、charset、表单 action 和子资源。
2. 对 `www.gzexam.com.cn` / `www.gzpi.gov.cn/gzexam` 做 2008 年报名期与截止后两个时点对照，测试 deadline-state collapse。
3. 对 `www.zjks.com/zjksweb/showInfo/Info.aspx?id=694` 查找 original announcement capture，再追页面内实际报名链接，避免把 information page 当 transaction page。
4. 若取得报名页，只记录公共字段结构，不复制普通考生实例数据。
5. 选择 2014 `zg.cpta.com.cn/examfront` 作为“统一平台迁移”较晚时点，比较地方页面从 transaction owner 变成 router 后的保存结构。

## 15. 对旧 Web 史的意义

职业资格考试提醒我们，旧 Web 的一个重要历史不是“人们开始在网上看信息”，而是：

> **网页开始插进那些本来需要单位、人事部门、窗口、照片、纸表和银行共同完成的制度流程。**

但它通常不是一次性替代所有旧环节，而是先形成奇怪的混合系统：

```text
在家填表
→ 去照相馆
→ 回家等照片
→ 去单位盖章
→ 网上付钱
→ 去窗口审核
→ 再回网页打印
→ 去实体考场
→ 网上/电话查成绩
→ 再去做资格复核
```

这种“半线上”不是不成熟的笑话，而是理解 2005–2015 中文 Web 如何真正嵌入普通制度生活的关键历史对象。

---

## Sources

- 2006 卫生专业技术资格考试网上报名：https://news.sina.com.cn/o/2006-11-09/094010452869s.shtml
- 2006 卫生资格报名材料与现场确认：https://www.sd-eh.com/index.php/portal/article/index/id/88.html
- 2007 广东注册安全工程师报名：https://m.jianshe99.com/html/2007/3/pa715835495182370028910.html
- 2007 浙江职称外语网报/网付：https://rsc.zufe.edu.cn/info/1068/2128.htm
- 2008 广州注册结构工程师：https://www.eol.cn/hang_kao/jian_zao_di_chan/zhu_ce_jie_gou_gong_cheng_shi/kao_shi_dong_tai/200807/t20080701_305794.shtml
- 2008 广州经济专业技术资格报名流程：https://www.chinaacc.com/new/15/22/48/2008/4/lu113513204413480024876-0.htm
- 2008 厦门执业药师报考流程：https://www.med66.com/html/2008/5/zh9255191239121580027562.html
- 广州市人事局 2009 年资格复核：https://rsj.gz.gov.cn/ywzt/rcgz/gzzc/tzgg/tzgg/content/post_2418023.html
- 2014 吉林专业技术资格考试报名：https://www.eol.cn/hang_kao/jian_zao_di_chan/zhu_ce_jian_zhu_shi/kaoshi_dongtai/201402/t20140210_1070972.shtml
- 2015 乌兰察布全国平台报名公告：https://inews.nmgnews.com.cn/system/2015/07/09/011722641.shtml

*Initial research note assembled with AI assistance; all reconstruction claims remain explicitly separated from historical evidence.*