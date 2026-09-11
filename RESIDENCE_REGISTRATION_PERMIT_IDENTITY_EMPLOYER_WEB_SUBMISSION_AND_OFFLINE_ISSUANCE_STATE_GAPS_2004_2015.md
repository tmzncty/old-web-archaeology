# 居住登记、居住证、身份证、单位网报与线下发证状态差（2004–2015）

> Scope：本 note 只研究约 2004–2015 中文互联网中与“人已经住在异地，但行政身份/居住记录怎样跟过去”直接相关的 Web / Web-adjacent 对象：二代身份证照片与异地办证过渡方案、深圳 2008 居住证/就业登记网上申报、2015 深圳经济特区居住证服务平台，以及这些前台与派出所、单位、房东/申报义务人、纸表、后台人口系统和实体证件之间的状态差。1980s 暂住登记只作为必要前史，2016 以后全国身份证异地受理和跨省户政只作为后续演变，不把本仓扩成户籍制度史。

Cross-repo：生活史解释见 `tmzncty/how-people-lived`：  
`topics/from-temporary-residence-registration-to-cross-province-services-administrative-residence-portability-and-return-burden-china-1985-2026.zh-CN.md`

## 0. 为什么这个对象值得单独建 note

本仓已经有公务员网报、高考志愿、兵役登记、社保查询、医疗问答、网银、铁路票务等事务状态专题，但此前没有拆开一个非常基础的“行政居住”问题：

> **一个网页说某人可以申报居住登记、申请居住证或上传身份证照片，究竟能证明现实中的什么？**

这个对象特别容易出现三种后见之明误读：

1. “2008 已经网上办居住证，所以劳动者本人可以在家独立在线办完”；
2. “2006 可以网上传二代证照片，所以身份证已经可以全国异地办理”；
3. “2015 网站显示居住登记成功，所以实际住址、居住连续性和最终公共服务资格都已经确定”。

真实链条往往是混合的：

```text
physical person lives at address
→ landlord / employer / person records facts
→ Web account authenticates
→ data entered
→ saved
→ submitted
→ list/form printed
→ paper/material bundle reaches office
→ office accepts
→ backend verifies identity/address/employment
→ permit/card production
→ credential issued
→ later endorsement / continuity check
→ another agency decides whether credential satisfies its own service rule
```

因此本 note 的核心合同是：

> **public Web shell != private residence record != accepted application != issued credential != current entitlement != actual residence.**

---

## 1. 研究单位必须拆开

至少区分：

1. **physical person**：现实中的人；
2. **actual dwelling / stay**：现实居住地点与时间；
3. **household registration / hukou**：户籍登记状态；
4. **resident ID credential**：居民身份证及其签发状态；
5. **temporary/residence registration**：现居住地登记记录；
6. **residence permit**：居住证证件/使用功能；
7. **employer / school / landlord / declarant**：现实申报义务主体；
8. **operator**：实际操作键盘/网页的人；
9. **Web account**：单位或个人平台账号；
10. **authentication state**：单位代码、密码、个人实名、验证码等；
11. **application form**：纸面/电子申请表；
12. **saved draft**：系统保存但未上报状态；
13. **submitted record**：已上报状态；
14. **printed roster / form**：系统生成的纸质名单/材料；
15. **receiving office**：居住证/劳动/公安实体受理窗口；
16. **accepted application**：材料齐备、正式受理；
17. **backend verification**：公安/就业/社保/地址等后台核验；
18. **card production**：制证；
19. **credential issuance**：正式签发/发放；
20. **endorsement / validity**：签注、延期、有效期；
21. **service eligibility**：教育、证件、交通、住房等另一个部门的资格判断；
22. **archive capture**：公开网页被档案保存的一份表示。

永久保持：

```text
person != Web account
credential subject != keyboard operator
actual residence != registered residence
residence registration != residence permit
residence permit != local hukou
resident ID != residence permit
saved != submitted
submitted != accepted
accepted != approved
approved != card physically received
permit valid != every downstream service approved
photo uploaded != identity credential issued
archive capture != authenticated backend state
```

---

## 2. 前史边界：行政居住登记早于 Web，而且从一开始就可能由代理人操作

北京 1985 年暂住人口规定要求外地来京人员进行暂住登记，部分长期暂住者申领暂住证；住在单位、工地、旅店等处者往往由留住单位指定人员统一申报。

- **A / official historical regulation republished by Beijing government**  
  https://www.beijing.gov.cn/zhengce/zfwj/zfwj/szfwj/201905/t20190523_70923.html

对 old-Web 的关键启示不是制度评价，而是：

> **“某人的行政记录存在”从来不等于“这个人亲自填写了每一个字段”。**

这个代理结构后来进入 Web 后不会自动消失；它只是从“单位户籍管理员拿纸表去派出所”变成“单位管理员登录账号批量录入”。

---

## 3. 2004–2006：二代身份证变成机器可读证件，但 Internet 首先只移动了一段材料

2004 年第二代居民身份证换发启动。同期资料确认新证使用非接触式 IC 卡，具有视读和机读功能。

- **B / contemporaneous Xinhua report**  
  https://news.sina.com.cn/c/2004-03-29/23072171651s.shtml

但 2006 年长期外出务工经商人员仍遇到“必须回常住户口所在地办理”带来的现实困难。公安部当时允许若干替代安排：暂缓换证、工作人员前往流动人口集中地采集人像、亲属持户口簿代办。

- **B / contemporaneous Xinhua report**  
  https://news.sina.com.cn/c/2006-10-19/175410276619s.shtml

重庆梁平针对在深圳、东莞等地务工者的做法更适合 old-Web：劳动者在务工地数码照相，照片通过 Internet 上传到二代身份证照片检测中心检查，之后仍由原籍/亲属链继续办证。

- **B / contemporaneous regional report**  
  https://news.sina.com.cn/c/2006-09-27/080010118888s.shtml

因此必须固定：

```text
photo captured digitally
!= photo passed technical check
!= origin-side identity record verified
!= application accepted
!= resident ID produced
!= resident ID delivered
```

更不能从“照片经过 Web 上传”写成“2006 年身份证已经实现全国异地受理”。

### 对 archive 的特殊风险

未来如果只剩“二代证照片检测中心”网页：

- 它可以证明某个上传/检测入口存在；
- 不能证明某一上传者最终取得证件；
- 更不能说明制证法律权限已经从户籍地转移到务工地。

这是典型的 **material-transfer digitization / jurisdiction-still-offline gap**。

---

## 4. 2008 深圳：官方文件保存了一条非常完整的 hybrid Web workflow

2008 年 6 月，深圳公安局和劳动保障局发布《关于启用深圳市居住证/劳动就业登记网上申报系统的通知》，并规定从 8 月 1 日起实施。

- **A / contemporaneous official notice**  
  https://www.sz.gov.cn/zfgb/2008/gb604/content/post_4985042.html

这份文件比“某网站能办居住证”的概括有价值得多，因为它明确给出了状态序列：

```text
1. 用人单位线下到窗口立户
   → 提交单位证明
   → 领取系统登录密码 + 纸质《居住证申请表》

2. 被聘员工填写纸表

3. 用人单位从深圳政府在线 / 公安主页 / 劳动保障网上大厅进入系统

4. 单位录入员工：
   → 个人基本信息
   → 就业信息
   → 居住证信息

5. 点击“保存”

6. 点击“上报”

7. 系统打印就业登记资料 / 居住证人员名单

8. 单位携相关材料到实体受理机构

9. 后续受理 / 审核 / 制证
```

这条链必须永久保留：

> **online submission != paperless end-to-end service**。

而且官方文件明确把用人单位规定为办理劳动就业登记和申办居住证的责任主体之一。

因此：

> **employee = credential subject; employer staff may be the Web operator.**

任何未来统计“2008 居住证网报用户”的研究，如果把一条单位账号会话想象成一个独立劳动者自己上网，就会严重误读数字普及程度。

### 2008 制度本身已经是跨系统对象

同年的《深圳市居住证暂行办法》要求公安、劳动保障、出租屋管理等信息系统通过统一政务信息资源交换平台互联共享；条例同时允许逐步通过网络、电话、传真等方式申请居住登记。

- **A / contemporaneous official regulation**  
  https://www.sz.gov.cn/zfgb/2008/gb604/content/post_4985058.html

这说明“网站”从一开始就只是更大后台中的一个 channel，不能单独理解。

---

## 5. 2008 ordinary-user evidence：证件意义进入生活，但不能反推界面使用

2008 年 8 月实施首日，同期新华社报道中，来自湖南、2005 年来深圳工作的袁先生说，暂住证总让他觉得自己是“外”人，而居住证使他开始把自己描述为准备长期住下去的人。

- **B/T1 / contemporaneous report + first-person statement**  
  https://news.sina.com.cn/s/2008-08-01/202114253686s.shtml

《法制日报》同期还记录一名在深圳 6 年的湖南机械维修工，把新居住证与能够更方便办理赴港事务、去香港看看联系起来。

- **B/T1 / contemporaneous report + first-person statement**  
  https://news.sina.com.cn/o/2008-08-04/080414263246s.shtml

这些材料适合证明：居住证被普通人理解为一种“我能在这里继续生活/办事”的 credential。

它们**不适合**证明：

- 两名受访者本人亲自使用了 2008 Web 申报系统；
- 所有外来劳动者都认可这种制度；
- 证件所列的所有公共服务在 2008 年已经自动可用。

生活史效果和 Web 操作证据必须分开。

---

## 6. 2015：平台转向个人/申报义务人网办，但“谁负责登记”变得更复杂

2015 年《深圳经济特区居住证条例》及办理规定重构了居住登记与居住证制度。官方办理规定明确，申报义务人可通过网络或受理点查询其提供居所内人员的登记信息；非深户籍人员和持证人也可以通过网络或受理点查询本人状态。

- **A / contemporaneous official implementation rules**  
  https://www.sz.gov.cn/gkmlpt/content/7/7787/post_7787069.html
- **A / contemporaneous ordinance text**  
  https://www.sz.gov.cn/zfgb/2014/gb900/content/post_4945836.html

同期服务指南留下了一个可以继续做 archive 定位的 historical original URL：

```text
https://www.szjzz.gov.cn/
https://www.szjzz.gov.cn/p
```

- **B / contemporaneous service guide, 2015-07-08**  
  https://m.bendibao.com/bsy613845.html

这个阶段至少有三类 actor：

```text
resident / credential subject
landlord or other declarant / residence-reporting duty
Web account operator
```

三者可能是同一人，也可能完全不是。

此外，2015 年公安通知要求部分旅业/留宿场所把住（留）宿人员身份信息扫描、上传到公安治安管理信息系统。

- **A / contemporaneous Shenzhen Public Security notice**  
  https://www.sz.gov.cn/zfgb/2015/gb929/content/post_4956387.html

所以“居住数据上线”并不只意味着居民打开一个个人 portal；它还包括房东、单位、旅业经营者、社区/公安等多种数据入口。

---

## 7. 2015 forum evidence：`page reachable != transaction executable`

深圳新闻网 2015 年 9 月整理当时新版居住证舆情时，保存了一条 8 月深圳论坛用户材料。用户称自己在 `https://www.szjzz.gov.cn/index` 注册、登录、录入真实信息并申报居住登记，但系统返回审核不通过，未清楚说明原因，也未收到预期短信；电话咨询也没有立即解决。

- **B / contemporaneous media synthesis preserving forum material, 2015-09-22**  
  https://www.sznews.com/zhuanti/content/mb/2015-09/22/content_16895848_13.htm

这是本 note 很重要的一条反例：

```text
site exists
!= account registration succeeds for everyone
!= address / resident data match backend
!= submission accepted
!= user receives reason for rejection
!= SMS is delivered
!= support channel can resolve immediately
```

而且该页同时记录，当时部分申请人的问题与平台信息系统尚未完善、或新制度条件不满足有关。

不能把一条 forum complaint 外推成“平台普遍不可用”，但它证明了**事务失败状态真实存在，而且当年用户能够直接感知到后台数据匹配问题**。

---

## 8. 2015 historical URL 与 M1 capture 状态

本轮取得的 exact historical original URL 候选：

```text
https://www.szjzz.gov.cn/
https://www.szjzz.gov.cn/p
https://www.szjzz.gov.cn/index
```

其中 `/p` 与根域来自 2015-07 同期服务指南，`/index` 来自 2015-08 forum material 的当年整理。

本轮尝试继续通过公开 Wayback/CDX 路径定位 2015 capture，但当前可用访问路径没有取得一份**实际打开后**能够同时核验以下字段的历史快照：

- `archive_source`
- `capture_url`
- `original_url`
- `capture_datetime`
- HTTP / replay state
- `Content-Type / charset`
- DOM / form action
- login/register endpoints
- scripts / iframes / subresources
- second historical time point

因此严格记录：

> **M1 verified historical Shenzhen residence-service platform capture: NOT ACHIEVED IN THIS SLICE.**

这不等于“Wayback 没有保存”。这里只能说 locator / replay 在本轮没有达到 METHOD 的 capture 验证门槛。

同样，本轮不能支持以下历史技术断言：

- 2008/2015 页面必须使用 IE；
- 使用 ActiveX；
- charset 是 GB2312 / GBK / UTF-8 中的哪一个；
- server-side framework 是 ASP / JSP / PHP 中哪一种；
- 2008 系统与 2015 `szjzz.gov.cn` 是同一代码库；
- 今天还能访问的深圳公安页面可以代表当年 DOM。

全部保持 **UNKNOWN**。

---

## 9. 最重要的 archive bias

### 9.1 `public-help-page survival / private-resident-state loss`

最容易保存：

- 办理规则；
- 登录入口；
- “保存/上报/打印”的教程；
- 政策问答。

最不可能进入公共 Web archive：

- 某个普通人的身份证号；
- 真实地址；
- 什么时候入住/搬离；
- 后台审核失败原因；
- 居住连续年限；
- 是否后来真正领取证件。

所以一个保存完好的 portal 也不能恢复普通人的真实行政居住史。

### 9.2 `credential-subject / operator gap`

2008 官方流程已经证明：

```text
worker whose permit is being processed
!= employer staff who logs into Web system
```

2015 又增加房东/申报义务人。

因此 archive / server log 中“谁发起一次请求”与现实中“谁的生活因此被登记”必须分开。

### 9.3 `save / submit / print / office-acceptance gap`

2008 系统明文把“保存”“上报”“打印”和“携资料到窗口”拆开。

未来看到截图里的“保存成功”按钮绝不能写成“申请已完成”。

### 9.4 `address-code / actual co-residence gap`

地址本身可以成为结构化数据库项，但：

```text
address exists
!= person actually slept there every day
!= registration was updated immediately after move
!= co-residents / landlord relationship can be inferred safely
```

研究平台 schema 时优先抽象字段，不重新公开普通人的历史详细住址。

### 9.5 `credential-history / downstream-service gap`

居住证页面可能显示证件有效，但教育、出入境、住房等部门仍有自己的时期性条件。

因此：

> **permit valid at time T != every advertised benefit executable at time T**。

---

## 10. 隐私边界比一般旧网页更严格

居住登记/居住证平台天然包含高敏感组合信息：

- 姓名；
- 身份证号；
- 户籍地址；
- 实际居住地址；
- 房东/同住关系；
- 就业单位；
- 入住/离开时间；
- 可能还有社保/家庭/联系方式。

即使某一旧页面或泄露数据今天仍可检索：

- 不批量重新发布；
- 不建立普通人的 residence timeline；
- 不为了“复原完整事务”搜集私人后台截图；
- 研究重点应放在 field schema、actor role、状态机、公开帮助页和匿名化失败模式。

这里的“档案不完整”部分是合理的隐私结果，不应被当成需要补齐的技术缺陷。

---

## 11. 已证实 / 高概率 / 不知道

### 已证实

- 2004–2006 二代证数字化与长期外出人员原籍办证困难同时存在；
- 2006 已有“数码照片经 Internet 上传检测、原籍继续办证”的 hybrid 工作流；
- 2008 深圳居住证/就业登记网报存在，并明确区分单位立户、纸表、录入、保存、上报、打印和线下窗口；
- 2008 用人单位可作为责任主体，`credential subject != Web operator`；
- 2015 `szjzz.gov.cn` 已作为深圳居住登记/居住证服务入口出现在同期指南；
- 2015 同期用户材料证明注册、提交之后仍可能出现审核、短信和客服状态差。

### 高概率但仍需 historical capture 加强

- 2015 服务平台存在至少根域、`/p`、`/index` 等入口/路径变体；
- 2008 “深圳市居住证综合信息网”与政府在线、公安全站、劳动保障网上大厅之间存在导航关系，但 exact original URL / 重定向关系尚未核验；
- 2008 到 2015 的居住证 Web 基础设施存在明显系统重构，而非仅页面换皮。

### 不知道

- 2008/2015 历史 DOM、charset、CSS/JS 架构；
- 是否存在浏览器限制或控件要求；
- 登录、注册真实 form action；
- 哪些页面被 iframe/JS 动态加载；
- 2008 与 2015 后台数据库迁移/兼容细节；
- 普通劳动者本人独立使用 Web 的比例；
- 2015 archive 对 authenticated pages 保存到什么程度。

---

## 12. 下一步

1. 继续以 `szjzz.gov.cn` 的 2015 exact URL 做 Wayback / Common Crawl / Archive-It locator 调查；
2. 找到至少两个 historical time points，再判断是否能进入 M1 完整案例；
3. 搜索 2008 同期报纸/用户教程，争取获得“深圳市居住证综合信息网”确切 original URL；
4. 比较 2008 employer-centric portal 与 2015 declarant/personal portal 的 actor model；
5. 若获得 capture，优先验证 charset、登录边界、保存/上报按钮和公开帮助页，不尝试访问私人账号；
6. 把“单位网报”“个人申请”“房东申报”作为三条不同事务路径，不再合并成一个“网上办证”。

---

## 13. 本 note 对中文旧网解释的修正

政务旧网最容易让后来的研究者产生一种错觉：**网页上已经有表单，就等于人已经可以独立在线完成现实事务。**

居住证案例恰好说明相反情况。2008 年最典型的“网上申办”，可以是员工写纸表、单位管理员上网录入、系统打印名单、单位再抱着材料去窗口；2006 年的“网上办身份证”可以只是照片在 Internet 上移动，而法律上的办证仍留在原籍；2015 年个人 portal 更成熟以后，后台地址记录、申报义务人和审核状态又成为新的摩擦来源。

因此研究这类旧网页，最值得保存的不是“按钮长什么样”，而是：

> **究竟是哪一段行政状态第一次能够通过网络移动；又有哪一段仍然要求一个真实的人、单位或纸件到达现实窗口。**
