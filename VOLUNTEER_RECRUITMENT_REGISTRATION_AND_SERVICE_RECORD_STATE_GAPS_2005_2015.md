# Volunteer recruitment, registration and service-record state gaps, 2005–2015

## Scope

本 note 研究约 2005–2015 中文 Web 中**志愿者招募、实名注册、项目报名、筛选培训、服务时长与证书记录**留下了什么，以及 archive 可以证明什么、不能证明什么。

它不是中国志愿服务史。1990s 的学校、单位、团组织和地方协会只作为理解旧 Web 的前史边界；2015 年之后移动端平台、疫情应急动员、线上陪伴与时长交易问题主要由 companion `how-people-lived` 承接。

Companion ordinary-life note：

- <https://github.com/tmzncty/how-people-lived/blob/main/topics/volunteer-service-addressability-civic-role-and-recorded-altruism-china-1993-2026.zh-CN.md>

本题尤其容易发生 **public-shell-to-real-service leap**：研究者看到一个“我要报名”按钮、一串申请人数、一个志愿者证书，就把它写成“这些人已经完成了真实服务”。本仓继续按 METHOD 把 platform、host、page、account、transaction、record 与 claim 分开。

---

## 1. Claim contract

至少固定以下状态边界：

`recruitment page exists ≠ application form exists`

`form visible ≠ submit endpoint works`

`form submitted ≠ server accepted`

`application accepted ≠ selected`

`selected ≠ assigned`

`assigned ≠ trained`

`trained ≠ actually attended`

`attended ≠ completed the assigned task`

`task completed ≠ service recipient actually benefited`

`hours recorded ≠ hours independently verified`

`hours verified ≠ service quality`

`certificate exists ≠ underlying service record authentic`

`current page carrying a 2007 date ≠ verified 2007 memento`

对 archive，公开招募页最容易保存；真正决定一个志愿者有没有上岗的身份证明、面试结果、内部名单、排班、签到、退岗、服务对象反馈和时长更正，几乎都更靠近认证后的后台或线下组织过程。

因此：

> **旧网页上的“志愿者”首先是一个平台状态，不是自动等价于现实里完成过服务的人。**

---

## 2. 前史边界：Internet 没有发明志愿者匹配

1994 年《人民日报》同期材料已经记录青年志愿者行动、“一助一”长期服务和通过学校、单位、团组织进入项目的路径。

来源：

- <https://cn.govopendata.com/renminribao/1994/10/7/9/>
- <https://cn.govopendata.com/renminribao/1994/3/7/4/>
- <https://cn.govopendata.com/renminribao/1994/04/19/3/>

这不属于本仓核心 Web 年代，但它解释了 later Web 的真正增量。前 Web 的典型路由更像：

```text
school / work unit / association / local organizer
→ organizer knows a need
→ organizer recruits or mobilizes people
→ service team is formed
→ physical service occurs
```

旧 Web 增加的不是第一次“陌生人帮助陌生人”，而是把：

- 项目名称；
- 服务地点；
- 时间；
- 技能要求；
- 申请资格；
- 联系方式；
- 报名入口

逐渐变成普通浏览器可以发现和提交的对象。

---

## 3. 2006 北京奥运：一个典型的 distributed-Web recruitment cross section

### 3.1 Web、热线和纸表并存

2006 年 8 月北京奥运会、残奥会志愿者招募启动时，北京地区同时存在：

- 区县网络报名系统；
- 12308 咨询热线；
- 街道 / 乡镇团委纸质报名表；
- 高校和相关组织的线下招募点。

来源：

- 新京报 / 新浪，2006-08-29：<https://news.sina.com.cn/c/2006-08-29/00459871729s.shtml>
- 北京奥运会官方网站历史内容 / 新浪，2006-08-28：<https://sports.sina.com.cn/o/2006-08-28/16062424298.shtml>

这对旧网考古很重要，因为“奥运志愿者网上报名”并不对应一个单一 host。

同期页面列出了多个区县报名站点，例如：

- `www.bjdch.gov.cn`
- `www.bjxch.gov.cn`
- `www.cwi.gov.cn`
- `www.bjchy.gov.cn`
- `www.bjhd.gov.cn`
- `www.bjft.gov.cn`
- `www.bjsjs.gov.cn`

以及其他区县政府或招募入口。

因此当时更可能存在一个**分布式招募拓扑**：

```text
central Olympic recruitment information
→ district / county site
→ local recruitment page
→ local form or instructions
→ local organizer database / manual workflow
→ later centralized selection state
```

不能因为今天只找到一个中央宣传页，就重建成“所有报名都通过一个统一 Web application”。

### 3.2 Archive implications

分布式拓扑会制造至少五种 capture gap：

1. 中央页面保存，但区县 target 没保存；
2. 区县首页保存，但动态报名 form 没保存；
3. form HTML 保存，但 submit endpoint / POST 没保存；
4. 页面显示“报名成功”，但后台是否真正收件不可见；
5. 区县域名后来改版或复用，使旧 URL family 难以确认。

因此应分别记录：

`central locator`

`district host`

`recruitment page`

`application form`

`submit endpoint`

`server acceptance`

而不是统称“奥运报名网站”。

---

## 4. 2007–2008：申请人数只是 funnel 的最上层

2008 年 3 月底，北京奥运会赛会志愿者申请人数达到 1,125,799 人；最终北京实际录用赛会志愿者 74,615 人，京外赛区另有 7,600 人。

来源：

- 新华社 / 新浪，2008-04-02：<https://2008.sina.com.cn/dt/other/2008-04-02/174763407.shtml>
- 法制日报 / 中国新闻网，2008-08-14：<https://www.chinanews.com.cn/olympic/news/2008/08-14/1347326.shtml>

同期招募规则还明确存在：

```text
application
→ material review
→ interview / test
→ position matching
→ background review
→ training
→ admission notice
→ actual scheduling
```

来源：

- 北京奥运会官方网站 / 搜狐，2007-03-27：<https://2008.sohu.com/20070327/n249015045_3.shtml>
- 北京奥运会官方网站 / 搜狐，2007-10-18：<https://news.sohu.com/20071018/n252727527.shtml>

因此旧 Web 中最显眼的“申请总人数”反而是最不能直接写成现实服务规模的数字。

必须区分：

`account registered`

≠ `application submitted`

≠ `application eligible`

≠ `candidate interviewed`

≠ `volunteer selected`

≠ `role assigned`

≠ `shift attended`

≠ `service completed`。

### 4.1 Skill / role matching is a separate state

志愿服务不是一个统一岗位。翻译、医疗、交通、媒体、场馆协助、秩序维护等角色对技能、时间和风险要求不同。

所以一个页面写“申请成功”最多说明候选人进入了 pipeline，不能证明：

- 某个角色有空位；
- 技能被组织认可；
- 背景审查通过；
- 候选人愿意接受最终分配；
- 排班与学习/工作时间兼容。

对 archive 来说，这些后续状态多数不会出现在公开 HTML 里。

---

## 5. `www.zgzyz.org.cn`：网上申报之后仍有属地审核和实地核验

2007 年团中央有关志愿者评选文件明确要求在中国志愿者网 `www.zgzyz.org.cn` 开设专题和网上申报系统；网上申报截止后，申报数据按属地反馈至省级组织，随后还要进行资格审查、实地考察和初评。

来源：

- 中国共青团，2007-12：<https://www.gqt.org.cn/documents/zqbf/200712/t20071204_53573.htm>

这给出一个很重要的 old-Web state chain：

```text
public Web application
→ server-side submission
→ record routed by territory
→ local organization receives record
→ qualification review
→ possible field verification
→ evaluation / selection
```

所以：

`online application exists ≠ reality is verified online`。

### 5.1 Current evidence status

本轮可以把 `www.zgzyz.org.cn` 记为高置信 historical locator，因为同时代正式文件明确指向该 host 和“网上申报系统”。

但本轮**没有实际取得并打开一个 2007 年满足 M1 门槛的完整历史 transaction capture**，因此以下内容保持 unknown：

- 原始 DOM；
- charset；
- frames / table layout；
- browser requirement；
- form action；
- GET / POST；
- captcha；
- cookie / session；
- 身份字段具体格式；
- server acceptance response；
- applicant dashboard；
- region-routing implementation。

同样，今天能访问团中央 2007 文件，不等于 2007 年 `zgzyz.org.cn` 的交互技术状态已被恢复。

---

## 6. `www.bv2008.cn`：从一次报名到一个持久的 volunteer account / service ledger

2011 年底，北京宣布将“志愿北京”建设为统一志愿服务综合信息平台。同期报道说明，实名注册者填写二十余项个人信息后取得唯一志愿者编号，个人基本信息和志愿服务时间被设计为长期保存；2012 年报道继续说明，注册者可在网上申请团体、项目和培训，审核后平台记录服务经历和时间。

来源：

- 北京日报 / 新浪，2011-12-19：<https://news.sina.com.cn/c/2011-12-19/031823653117.shtml>
- 中国互联网协会转载，2012-03-07：<https://www.isc.org.cn/article/19308.html>

这里出现一个和 2006 分布式招募明显不同的对象：**persistent volunteer account / service ledger**。

状态更像：

```text
real person
→ real-name registration
→ unique volunteer number
→ profile / skills
→ organization membership
→ project application
→ accepted assignment
→ service episode
→ verified hours
→ cumulative history
→ certificate / star / later reuse
```

### 6.1 “终身保存”是设计 claim，不是 archive 已经证明的事实

同期媒体使用“终身保存”一类表述，只能证明平台当时这样设计或宣传。

它不能自动证明：

- 数据从 2011 到今天每一天都连续可用；
- 所有旧账号都能登录；
- 每一笔旧时长都没有迁移损失；
- 数据库 schema 没有改变；
- 一次平台迁移没有重新映射 account ID；
- 用户本人从未要求删除或更正记录。

所以本仓将其记为 **persistence claim**，而不是 empirically verified perpetual persistence。

### 6.2 Public shell / private service state asymmetry

公开页面可能留下：

- 注册说明；
- 项目列表；
- 招募人数；
- 项目状态；
- 培训公告；
- 证书示例；
- 星级规则。

认证后或线下状态可能包括：

- 身份证号 / 手机号；
- 审核结果；
- 内部 roster；
- 排班；
- 到场签到；
- 退岗；
- 服务对象信息；
- 负责人确认；
- 时长更正；
- 申诉；
- 被拒绝或取消的记录。

因此 archive 天然更容易保存“这个项目看起来成功地招了很多人”，而不是“谁没来、谁中途退出、谁的时长后来被纠正”。

---

## 7. 2015：service record 获得外部 credential value

教育部 2015 年《学生志愿服务管理暂行办法》要求学校建立学生志愿服务记录档案，将记录归入综合素质档案；高校将志愿服务纳入实践学分管理，并按累计时间进行星级认证。

来源：

- 教育部，2015-03-18：<https://www.moe.gov.cn/srcsite/A12/s7060/201503/t20150318_189379.html>

对 old-Web 考古而言，这意味着一个平台里的 `service hours` 不再只是内部展示字段，而可能流出平台，成为：

- 学校档案字段；
- 实践学分依据；
- 评奖 / 综评材料；
- 纸质或电子证明。

于是需要新增 **service-record provenance**：

```text
service happened
→ organizer verifies
→ platform writes hours
→ record persists
→ certificate generated
→ school / employer / other institution encounters certificate
→ external institution accepts or rejects it
```

任何一个环节都可能失败。

`certificate page exists` 更不能证明 underlying service happened exactly as claimed。

---

## 8. Assisted registration / human proxy state

数字系统不应被假设为人人独立操作。大型赛事、学生项目和社区服务中，可能存在：

- 学校统一收集报名信息；
- 班级 / 团组织代为录入；
- 线下纸表后由工作人员写入数据库；
- 工作人员帮助不会使用网站的人创建账号；
- 组织负责人批量确认时长。

因此：

`record exists in Web system ≠ volunteer personally completed the Web interface`。

这和其他数字公共服务中的 human proxy 问题相同：一个机会在网上存在，不等于每一个现实使用者都直接经过网页。

未来如果获得历史操作手册，应特别寻找：

- 批量导入；
- admin account；
- organization leader confirmation；
- CSV / Excel import；
- paper-to-digital migration；
- offline registration reconciliation。

---

## 9. Full state machine

本题建议后续所有案例至少按以下状态拆分：

```text
real social need
→ organizer creates project
→ public recruitment page
→ user discovers project
→ user account / identity
→ application form
→ submit attempt
→ server acceptance
→ applicant record
→ eligibility review
→ interview / test / background review
→ selected
→ role assigned
→ training
→ schedule / shift
→ actual attendance
→ check-in / organizer observation
→ real task performed
→ service recipient interaction
→ organizer verification
→ hours written
→ correction / dispute
→ certificate / star / school-credit handoff
→ repeat service or exit
```

### 9.1 Negative states must be preserved

尤其不能只保存 happy path。需要主动寻找：

- recruitment page expired；
- application deadline passed；
- form broken；
- duplicate application；
- ineligible；
- interview failed；
- background review failed；
- no suitable role；
- user withdrew；
- training not completed；
- schedule conflict；
- no-show；
- event cancelled；
- service suspended；
- volunteer left early；
- organizer refused to verify hours；
- hours missing；
- hours disputed；
- record corrected；
- certificate rejected externally。

如果档案只留下成功招募新闻，研究结果会系统性高估服务顺滑程度。

---

## 10. Archive biases specific to volunteer Web

### 10.1 Public-recruitment-shell / private-service-state asymmetry

最容易保存：

- 招募公告；
- 项目介绍；
- 资格要求；
- 申请总数；
- 成功典型；
- 证书 / 星级规则。

最难保存：

- rejected applicant；
- private roster；
- shift scheduling；
- attendance；
- no-show；
- recipient feedback；
- internal quality judgment；
- correction / dispute；
- why someone stopped serving。

因此公开壳层会天然比真实服务状态完整。

### 10.2 Successful-participation bias

平台新闻和媒体更愿意报道：

`报名踊跃 → 培训 → 成功上岗 → 感人故事`

失败状态通常没有独立 URL，甚至只存在于内部表格。

所以未来研究应主动搜：

`落选 / 退选 / 未通过 / 缺席 / 鸽子 / 取消 / 补录 / 时长错误 / 漏记 / 申诉 / 退岗`

等 contemporaneous traces。

### 10.3 Applicant-count survivorship bias

“申请超过 100 万”是新闻价值很高、保存概率很高的数字；“其中多少人完成了多少小时、多少人临时退出”更难保存。

因此大数字优先留存，会诱使后人把 recruitment attention 写成 deployed capacity。

### 10.4 Credential visibility bias

当志愿时长能生成证书、星级、学分以后，**record itself** 比服务中的细节更容易存档。

这可能让未来研究者看到大量“X 小时”“五星志愿者”，却看不到：

- 同样一小时包含多少实际劳动；
- 是否只是培训 / 值守 / 待命；
- 服务对象是否真正接触；
- 组织如何评估质量。

---

## 11. Privacy boundary

志愿平台很容易留下普通人的：

- 真实姓名；
- 学校 / 单位；
- 手机号；
- 身份证字段；
- 项目 roster；
- 服务对象地址；
- 未成年人信息；
- 困难家庭 / 病患信息。

本仓继续执行 METHOD 的研究必要最小化：

- 研究平台结构时优先记录 host、URL pattern、字段类型和状态机；
- 不批量复制普通志愿者 ID；
- 不重发旧手机号、身份证、家庭住址；
- 不为验证服务关系重新定位服务对象；
- 即使 archive 偶然保存认证后页面，也先判断是否应该引用，而不是“能看见就能公开”。

---

## 12. M1 status: explicit negative result for this run

### Historical locators found

本轮有较强同时代证据支持的 locator / host family 包括：

- 2006 北京奥运多个区县报名 host；
- `www.zgzyz.org.cn`；
- `www.bv2008.cn`；
- 北京奥运中央招募说明页及其区县跳转结构。

这些足以支持：

- Web 招募入口真实存在；
- 分布式区县报名体系真实存在；
- 网上申报后仍有线下/属地审核；
- 2011–2012 已出现实名唯一编号和累计服务时长的持久账号设计。

### Not verified in this run

本轮**没有实际打开并检查一份满足 M1 门槛的 2006–2012 中文志愿报名 / 服务记录完整 Wayback/WARC transaction capture**。

因此以下仍为 unknown：

- historical DOM；
- HTTP charset；
- CSS / JS；
- IE / ActiveX / browser assumptions；
- form action；
- GET / POST；
- captcha；
- cookie / session；
- real-name verification implementation；
- application server response；
- applicant dashboard；
- roster / assignment API；
- check-in mechanism；
- service-time entry endpoint；
- correction workflow；
- authenticated personal service record。

这个负结果的正确写法是：

> **本轮没有验证成功。**

而不是：

> `Wayback 一定没有这些页面。`

后续需要直接检查具体 memento、original URL family 和子资源，才能把 historical locator 升级为 verified capture。

---

## 13. Evidence table

| Evidence | Grade | Supports | Does not support |
|---|---|---|---|
| 1994 人民日报志愿材料 | A | pre-Web organizational routing existed | public searchable Web matching |
| 2006 Olympic recruitment notices | A/B | Web + hotline + paper multi-channel recruitment | every district form technically worked |
| 2007 Olympic selection rules | A/B | screening / testing / assignment pipeline | every applicant was processed identically |
| 2008 application/final volunteer counts | B | application funnel is much larger than final roster | final shift attendance for every selected person |
| 2007 `zgzyz.org.cn` official notice | A | online application + regional routing + later verification | original interactive form technical state |
| 2011–12 `bv2008.cn` reporting | B | real-name account, unique number, service-time ledger design | every legacy record is correct or continuously preserved |
| 2015 MoE rule | A | service records gain external credential value | every school implements it identically |
| 2019 contemporary reporting | B | no-show, travel, continuity and record friction exist | nationwide exact rates |

---

## 14. What this changes for old-Web archaeology

志愿者网站是一个非常好的反例，可以防止旧网研究过度迷恋“页面长什么样”。

即使完整恢复：

- 首页；
- 项目详情；
- 招募人数；
- 报名按钮；
- 个人资料页；
- 志愿时长；

仍然可能不知道现实中的关键事实：

- 谁真正来到现场；
- 谁只签到没服务；
- 谁因为工作 / 家庭临时退出；
- 谁的技能不匹配；
- 谁需要重复培训；
- 服务对象是否觉得有帮助；
- 时长是谁确认、怎样更正；
- 一张证书是否后来被学校认可。

因此本题补出的核心方法论是：

> **archive 可以很好地保存“公共参与被怎样界面化”，却很难完整保存“公共参与到底怎样发生”。**

而这正是两个仓库的交叉点：how-people-lived 追问一个普通人是否真的获得了工作与家庭之外的公共角色；old-web-archaeology 则追问，当这个角色被压成账号、项目、按钮和时长以后，哪些只是 Web shell，哪些状态还能被历史证据重新连接回真实生活。
