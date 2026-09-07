# 门诊挂号并不是一个按钮：网上预约、实名、114、微信与“真正看上病”之间的状态缺口（2003—2015）

> Scope：严格留在约 1995—2015 中文互联网。本文不写中国医疗史总论，而把 2003—2015 年医院网站、统一预约平台和移动端门诊前台当作旧网事务系统来研究：页面能证明什么，后台又有多少状态不会跟着页面一起被保存。

## 0. 为什么这个对象属于旧网考古

医疗网站特别容易制造一种“保存错觉”。

研究者未来可能找到：

- 一个医院首页；
- 一张“网上预约挂号”截图；
- 一篇“开通微信医院”的新闻；
- 一份医生出诊表。

但真正决定患者当天是否见到医生的往往不是这些静态页面，而是当时已经消失的动态后台：

```text
患者账号
→ 就诊卡/实名身份
→ 科室/医生排班
→ 可预约号源
→ 时段库存
→ 预约锁定
→ 预约确认
→ 当日取号/报到
→ 支付
→ 医保结算
→ 检查/检验队列
→ 处方
→ 药房状态
```

因此本专题的核心不是“医院什么时候有网站”，而是：

> **renderable page ≠ executable medical transaction**。

---

## 1. 2003 苏大附一院：Web 已经能预约，但事务仍在医院窗口完成闭环

2003 年 8 月 1 日，苏州大学附属第一医院推出网上预约挂号。同期《江南时报》给出了历史 locator：

- `www.sdfyy.cn`

并记录了实际操作：首次注册、查询科室和专家、选择日期/医生、系统返回号数、名额满时改约、查询/取消预约；预约成功后，患者 **就诊当天仍需到指定窗口付费取号**。

来源（B）：江南时报，2003-08-02，新浪存留：
https://news.sina.com.cn/o/2003-08-02/1058491035s.shtml

### 可直接支持的最小 claim

- 2003-08-01 苏大附一院已公开提供一种 Web 预约挂号服务；
- 同期报道给出 host `www.sdfyy.cn`；
- Web 前台能够表达科室、医生、日期、是否满额、预约号数和取消动作；
- 当日付费取号仍是独立线下状态。

### 不能从报道推出

- 原页面的 DOM、frameset、CSS 或 JS 结构；
- charset 是 GB2312、GBK 还是其他编码；
- 是否 IE-only；
- 账号是否与法定实名身份强绑定；
- 号源是实时数据库查询还是定时同步；
- 预约成功记录如何写入 HIS；
- “前 5 个号留给网上预约”在所有科室是否都稳定执行；
- 实际使用人数和 no-show 率。

### 新状态缺口

```text
web account created
≠ patient identity verified

slot shown
≠ slot still available at submit

reservation accepted
≠ fee paid

fee paid
≠ number collected / check-in completed

check-in completed
≠ doctor actually seen
```

---

## 2. 2009：预约政策全国推进以后，必须区分 exists / available / used

卫生部 2009 年 9 月 30 日印发《关于在公立医院施行预约诊疗服务工作的意见》，要求当年 11 月起所有公立三级医院开展预约诊疗，并要求预约和就诊使用本人有效证件实名办理。

来源（A）：卫生部，卫医管发〔2009〕95号：
https://www.nhc.gov.cn/zwgkzt/s9968/200910/43105.shtml

这可以证明 **policy-required availability**，但不能证明普通患者已经普遍采用。

同年卫生部门汇总显示，北京 9 月初诊预约率为 5.46%、复诊预约率为 20.36%，四川大学华西医院预约挂号量达到门诊量 50.10%。

来源（A/B）：中国政府网稿，2009-11-10，搜狐存留：
https://news.sohu.com/20091110/n268096207.shtml

而 2009 年 9 月 1 日北京三级医院推行预约挂号首日，媒体仍在协和医院看到百余名患者/家属守在挂号处，一名患者为专家号凌晨 3:30 到场。

来源（B）：北京晨报，2009-09-02，搜狐存留：
https://news.sohu.com/20090902/n266379669.shtml

### old-Web 解释

同一个 2009 年可以同时成立：

```text
预约功能 exists
预约渠道 available
普通患者知道该渠道 unknown / varying
预约号源 actually available varying
患者 actually used it varying
传统窗口仍 heavily used
```

因此任何未来 capture 即使显示“网上预约挂号”，也不能从 `exists` 跳到 `popular`。

---

## 3. 实名制把“账号”与“患者”拆成两个研究对象

2009 年正式文件要求预约挂号和就诊使用本人身份证等有效证件实名办理。同期武汉实名专家挂号报道还记录了患者对隐私问题的争论。

制度来源（A）：
https://www.nhc.gov.cn/zwgkzt/s9968/200910/43105.shtml

同期媒体/政府站存留（B）：
https://sbs.mof.gov.cn/gongzuodongtai/200908/t20090807_191046.htm

因此旧网研究不能把：

- Web login；
- 电话来电号码；
- 医院就诊卡；
- 身份证；
- 社保卡；
- 后来的医保电子凭证

混成同一个 identity object。

### 状态缺口

```text
account holder
≠ legal patient

legal patient verified
≠ medical-card record matched

medical-card record matched
≠ insurance identity matched

identity matched
≠ appointment entitlement available
```

尤其在父母/子女代理预约里，**operator identity 与 patient identity 必须分开**。

---

## 4. 2011 北京：114 与 Web 汇到统一前台，但“统一入口”不自动证明统一技术后台

2011 年 7 月，北京统一预约挂号平台启动试运行。同期报道给出的历史 Web locator 是：

- `www.bjguahao.gov.cn`

电话入口则是 114。报道明确说，平台之前各医院拥有不同预约号码与入口；统一平台试图让患者用同一电话/网站预约多家医院。

同期来源（B）：法制晚报，2011-07-27：
https://news.sina.com.cn/c/2011-07-27/151122886816.shtml

北京市卫生局 2013 年工作材料称，平台自 2011-07-28 启动，到 2013 年已有 146 家医院接入；当年前 11 个月三级医院投放可预约号源 3970.2 万个，占全部号源 82.3%，同时电话、网络、诊间、复诊、社区转诊、窗口、自助等渠道并存。

来源（A）：北京市卫生局，2013-12-23：
https://wjw.beijing.gov.cn/xwzx_20031/wnxw/201912/t20191214_1172797.html

### 需要避免的过度推断

可以说：

> 114 电话与 `bjguahao.gov.cn` 构成统一预约服务的两个公众入口。

不能在没有技术文档/抓包/历史页面的情况下说：

> 两者直接查询同一个单体数据库，采用某种具体 API，所有医院号源实时同步。

真实架构可能包含运营商坐席系统、卫生部门平台、医院 HIS、批量同步、缓存或各院接口。当前证据不足。

### 新状态缺口

```text
unified brand / entry point
≠ unified backend implementation

hospital connected
≠ all departments connected

slot quota uploaded
≠ real-time total hospital inventory

telephone reservation success
≠ SMS delivered

SMS delivered
≠ patient presents correct ID / security code
```

---

## 5. 2015：微信/APP 把事务进一步拆细，医院卡和医保成为新的 join keys

2015 年东莞市人民医院“掌上医院”微信/支付宝平台试运行一个月后，已有 6887 人通过微信挂号。同期报道保存了非常适合状态考古的操作路径：

1. 关注医院微信服务号；
2. 绑定个人信息；
3. 没有诊疗卡者先到窗口用身份证实名办卡；
4. 选择院区、科室、医生；
5. 完成挂号支付；
6. 收到微信预约成功信息；
7. 到护士台报到；
8. 医生开处方/检查；
9. 手机处理待缴费信息；
10. 药房、检验、功能检查仍各有自己的实体动作。

来源（B）：广州日报，2015-11-17，人民网：
https://health.people.com.cn/n/2015/1117/c398004-27822742.html

同年北京京医通微信支付试点也说明，移动支付要与医院既有卡系统、社保卡继续做身份与账务绑定。

来源（B）：新京报，2015-04-28，人民网：
https://health.people.com.cn/n/2015/0428/c14739-26915129.html

而《经济参考报》同期报道指出，多地“移动医院”已经能挂号、缴费、查报告，但移动支付与医保系统难以打通，医保实时结算是明显堵点。

来源（B）：2015-08-19，人民网：
https://finance.people.com.cn/n/2015/0819/c1004-27482801.html

### 需要固定的状态机

```text
WeChat followed
→ user profile created
→ hospital card bound
→ legal identity matched
→ appointment selected
→ slot locked
→ fee paid
→ appointment confirmed
→ hospital check-in
→ doctor encounter
→ order generated
→ payment liability generated
→ self-pay / insurance settlement
→ test / pharmacy execution
```

于是新增：

- `WeChat-account / hospital-card gap`
- `hospital-card / legal-identity gap`
- `mobile-payment / insurance-settlement gap`
- `appointment-confirmed / check-in gap`
- `doctor-order / downstream-execution gap`

---

## 6. 代理式数字就医：一个账号的操作者不一定是那个身体

新华网 2015 年温州医科大学附属第一医院报道记录：陈女士在单位用手机替不会使用智能手机的婆婆预约就诊；婆婆本人去医院，陈女士在远处继续接收检查时间和费用等数字状态。

来源（B）：
https://www.xinhuanet.com/health/2015-11/17/c_128434461.htm

2018 年平台侧调查又显示子女绑定父母就诊卡、远程挂号已成为可观察用法；该调查有明显网络/平台选择偏差，因此只能作为“路径存在”的材料，不用于全国比例推断。

来源（B，超出本仓主期末点，仅用于解释 2015 路径后来如何延伸）：
https://industry.people.com.cn/n1/2018/0704/c413883-30126354.html

对 2003—2015 的 old-Web 考古尤其重要的一点是：

> **account activity ≠ patient self-operation**。

如果未来 archive/日志只留下“某账号预约了一名患者”，不能自动把数字动作归给患者本人。

---

## 7. 动态号源是典型的 archive dark matter

门诊网站最有生活意义的内容恰恰通常最难保存：

- 某医生在某日 08:00 是否还有号；
- 一个时段是否从“可约”变成“已满”；
- 提交时是否发生并发抢占；
- 预约是否因医生停诊被取消；
- 付款是否成功；
- 患者是否按时签到；
- 系统是否把号源退回库存；
- 电话和 Web 是否看到同一批库存。

一个 archive 保存的静态医生列表很可能没有保存真正决定普通人行动的 live inventory backend。

因此增加 **page-survival / transactional-state loss / 页面幸存—事务状态消失**：

```text
historical HTML survives
≠ historical slot inventory survives
≠ historical transaction survives
≠ historical patient outcome survives
```

这也是为什么医疗旧网不能只做截图博物馆。

---

## 8. 浏览器与客户端条件：目前必须明确写“不知道”

### 2003 `www.sdfyy.cn`

同期报道证明 Web 服务存在，但本轮没有取得可核验的 2003—2005 原始 capture，因此不知道：

- HTTP header / Content-Type；
- charset；
- frames/table layout；
- IE-only / ActiveX / JavaScript 依赖；
- cookie/session 行为；
- 表单 method 和 endpoint；
- 预约确认页结构；
- 子资源是否来自同 host。

不能因为 2003 中文政务/医院站常见 IE 与 GB2312，就把这些常见特征填回这个具体站点。

### 2011 `www.bjguahao.gov.cn`

同期报道确认 locator 与服务存在，但本轮同样没有取得并检查满足 METHOD 合同的历史 Wayback/WARC replay，因此不能声明：

- 当年页面 charset；
- 精确 DOM/JS；
- 是否存在浏览器嗅探；
- 114 与 Web 的具体同步机制；
- 医院接口的实时性；
- 登录/session/cookie 结构。

---

## 9. Archive 调查记录（本轮）

### `www.sdfyy.cn`

已通过公开搜索查找 Wayback/历史引用。搜索结果能找到 `sdfyy.cn` 的后期子站历史 capture locator（例如 2013 年 `www3.sdfyy.cn` 科室页面），但**没有实际取得并验证 2003 网上预约页面的 replay response**。

这只能写成：

> 本轮未验证到 2003 网上预约页面的合格 archive capture。

不能写：

> Wayback 没有保存该服务。

### `www.bjguahao.gov.cn`

本轮确认了 2011 同期媒体中的 historical locator，但没有实际取得并检查一份 2011—2015 的 archive replay。

同样只能登记为 candidate locator / archive gap。

### M1 状态

**NOT ACHIEVED IN THIS SLICE.**

按照 `docs/METHOD.md` 与 `ROADMAP.md`，完整 M1 案例至少要求实际检查历史 capture、多个时点、资源缺失、浏览器/编码条件等。本轮只有同期文本证据和历史 locator，不足以把门诊预约站点宣布为“完整考古案例”。

---

## 10. Evidence list

| ID | Grade | Date | Subject | What it proves |
|---|---|---:|---|---|
| MED-01 | B | 2003-08-02 | 苏大附一院网上预约 | `www.sdfyy.cn` locator；注册/预约/取消/当日付费取号流程 |
| MED-02 | B | 2004-12-01 | 北京凌晨排队 | 预约前时代的实体队列劳动与家庭代理 |
| MED-03 | A | 2009-09-30 | 卫生部预约诊疗意见 | 三级医院推行预约、实名、更新出诊信息 |
| MED-04 | A/B | 2009-11-10 | 预约使用进展 | 不同医院预约率明显不同，exists 不等于 used |
| MED-05 | B | 2009-09-02 | 协和排队 | 新预约渠道出现后窗口排队仍同时存在 |
| MED-06 | B | 2011-07-27 | 北京统一平台 | `bjguahao.gov.cn` + 114 同期入口 |
| MED-07 | A | 2013-12-23 | 北京平台运行 | 146 家医院、多渠道并存、号源投放量 |
| MED-08 | B | 2015-04-28 | 京医通微信 | 微信挂号/支付与社保卡/医院系统绑定 |
| MED-09 | B | 2015-08-19 | 移动医院与医保 | 手机支付可用而医保实时结算仍可能不可用 |
| MED-10 | B | 2015-11-17 | 东莞掌上医院 | 绑卡、挂号支付、报到、检查、药房多状态事务 |
| MED-11 | B | 2015-11-17 | 温州代理就医 | 数字操作者与患者身体可以分离 |

核心 URL：

- https://news.sina.com.cn/o/2003-08-02/1058491035s.shtml
- https://finance.sina.com.cn/money/x/20041201/11461194069.shtml
- https://www.nhc.gov.cn/zwgkzt/s9968/200910/43105.shtml
- https://news.sohu.com/20091110/n268096207.shtml
- https://news.sohu.com/20090902/n266379669.shtml
- https://news.sina.com.cn/c/2011-07-27/151122886816.shtml
- https://wjw.beijing.gov.cn/xwzx_20031/wnxw/201912/t20191214_1172797.html
- https://health.people.com.cn/n/2015/0428/c14739-26915129.html
- https://finance.people.com.cn/n/2015/0819/c1004-27482801.html
- https://health.people.com.cn/n/2015/1117/c398004-27822742.html
- https://www.xinhuanet.com/health/2015-11/17/c_128434461.htm

---

## 11. 已证实 / 高概率 / 不知道

### 已证实

- 2003 苏大附一院公开提供 Web 预约，且预约后仍需到院付费取号；
- 2009 卫生部把实名预约诊疗推广到公立三级医院；
- 2011 北京启动 114 + Web 统一预约平台；
- 2015 一些医院已经把微信/APP 接入挂号、支付、报告等门诊状态；
- 同一时期医保结算、医院卡绑定、检查/药房等仍可能要求独立接口或实体动作。

### 高概率，但仍需 capture/技术文档

- 这些预约系统背后依赖医院 HIS 与号源数据库，并需要把多个前端事务同步回院内系统；
- 2003—2011 的页面很可能受当时浏览器、编码和 session 条件影响。

第二条只能保留为工程常识驱动的假设，不能指定具体 IE/编码实现。

### 不知道

- 2003 预约页面原始 HTML/charset/browser dependency；
- 2011 北京统一平台前台与 114 坐席的精确接口；
- 动态号源的同步频率与锁定事务；
- 支付失败/重复提交/停诊取消的历史错误页；
- 被 archive 保存的页面是否曾经能够在 replay 中真正提交事务；
- 普通患者、代办亲属、号贩子和第三方平台在后台日志里如何被区分。

---

## 12. 隐私与版权

医疗事务可能包含高度敏感的个人信息。后续若取得历史预约页面、日志、截图或缓存：

- 不重新公开普通患者姓名、身份证、手机号、诊疗卡号、疾病、预约记录；
- 只保留支持平台结构 claim 所需的最少字段；
- 动态接口若返回个人数据，不因 archive 可访问就批量镜像；
- 研究表单 schema 时优先抽象字段名和状态转换，不复制真实患者值。

---

## 13. 对 `how-people-lived` 的交叉解释

这条 old-Web 证据改变普通生活史的一点是：

> **网页把“排队”从一条可见的人群，拆成了一堆不可见的数据库状态。**

凌晨大厅里的人、矿泉水瓶和报纸很容易被记者拍下来；2003 年以后，等待越来越可能发生在“号源未放出”“已满”“预约成功待取号”“支付成功待同步”“实名未匹配”“已预约待签到”这些后台状态里。

所以网络时代并没有让等待消失。它让等待的一部分从医院门口迁入了数据库，而数据库恰恰比医院门口更容易在二十年后只剩一个空壳前端。

---

*AI-assisted research note. No reconstructed page is presented as historical original.*