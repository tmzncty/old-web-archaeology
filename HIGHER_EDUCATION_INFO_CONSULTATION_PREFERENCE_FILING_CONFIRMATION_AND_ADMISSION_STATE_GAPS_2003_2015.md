# 高校招生信息、网上咨询、志愿填报、确认与录取的状态差（2003–2015）

> Scope：本 note 只研究约 2003–2015 中文互联网中的高考招生信息平台、网上咨询、网上志愿填报，以及它们与短信、纸质确认、投档/录取状态之间的边界。1980s–1990s 的纸质招生目录、报纸、邮政和声讯电话只作为理解 Web 改变了什么的前史；2016 以后只用于解释后续演变，不扩展成本仓主体。

Cross-repo：生活史解释见 `tmzncty/how-people-lived`：  
`topics/from-paper-admissions-guides-and-voice-hotlines-to-online-preference-filing-educational-choice-addressability-and-application-executability-china-1980-2026.zh-CN.md`

## 0. 为什么这个对象值得单独建 note

本仓已有学历查询、校园一卡通、公务员网报、征兵网报等状态机研究，但此前没有把“高校招生信息 → 在线咨询 → 正式志愿提交 → 招生录取”拆成独立旧网对象。

这类页面尤其容易造成后见之明错误，因为今天看到一个历史“阳光高考”页面或“网上填报志愿”截图，很容易不加区分地写成：

> 考生在网上报了大学。

现实至少可能经过：

```text
浏览院校信息
→ 注册咨询账号
→ 在线提问
→ 得到回答
→ 查省级招生计划
→ 获取报名号 / 密码
→ 登录省级志愿系统
→ 填写志愿草稿
→ 提交
→ 确认提交
→ 收到短信
→ 学校 / 报名点下载确认表
→ 本人纸面签字
→ 报名点上报
→ 志愿正式生效
→ 投档
→ 高校录取
→ 录取结果可查
→ 录取通知书送达
→ 本人报到
```

因此本 note 的核心合同是：

> **information page != consultation state != preference-filing state != admission state != real enrollment**

---

## 1. 研究单位必须拆开

至少区分：

1. **physical candidate**：现实考生；
2. **candidate registration identity**：报名号、考生号、密码等招生考试身份；
3. **household / helper**：父母、教师、同学、机房工作人员等现实协助者；
4. **school / major information page**：学校、专业、学费、奖助、办学条件等公开信息；
5. **province-major quota record**：分省分专业招生计划；
6. **admissions policy / charter**：招生政策、招生章程；
7. **consultation platform account**：阳光高考等咨询平台账号；
8. **consultation question**：考生/家长提交的问题；
9. **consultation answer**：高校/招办作出的回复；
10. **public Q&A page**：回答后公开显示的问答内容；
11. **preference-filing system**：省级正式志愿填报事务系统；
12. **preference draft**：未最终确认的志愿草稿；
13. **submitted preference**：点击提交后的记录；
14. **final-confirmed preference**：最终确认、不可再改的志愿状态；
15. **SMS notification**：跨出 Web 的短信通知；
16. **printed confirmation sheet**：学校/报名点打印的纸质确认表；
17. **candidate signature**：现实纸面签名；
18. **school / registration-site report**：报名点最终上报；
19. **effective preference record**：正式生效、可进入投档的志愿；
20. **投档 record**：省级招生系统投档状态；
21. **institution admission decision**：高校录取决定；
22. **public admission-result query**：对考生开放的录取结果查询；
23. **paper admission notice**：纸质录取通知书；
24. **real enrollment**：现实到校报到；
25. **archive capture**：档案保存的网页表示。

永久保持：

```text
candidate != Web account
Web account != person at keyboard
information page != current-year quota
consultation question submitted != answered
answered != candidate read
read != candidate follows advice
draft != submitted
submitted != final-confirmed
final-confirmed != school-side final reporting
SMS success != preference legally effective
preference effective != 投档
投档 != admission
admission-result page != paper notice delivered
paper notice delivered != actual enrollment
archive capture != private transaction state
```

---

## 2. 前史边界：Web 没有发明志愿、查询或远程信息

在大众 Web 之前，招生事务已经通过学校、纸质招生计划/简章、报纸、电话、邮政和现场咨询组织。

2002 年安徽仍可通过 168 声讯电话查询高考成绩和后续录取状态。这是一个很好的 Web-adjacent 边界：Internet 已经存在，但电话仍是个人事务状态查询接口。

- **B / contemporaneous local report**：2002-07-24  
  https://edu.sina.com.cn/l/2002-07-24/28867.html

1995 年浙江报纸曾整版刊登上线名单，后来的报纸实物与考生回忆说明公开报刊也曾承担“结果传播”的功能。但该 2025 回忆只能列为 C，并不能据此推断 1995 全国统一流程。

- **C / retrospective anchored by surviving newspaper issue**  
  https://www.sohu.com/a/887113073_121627717

这个前史只用于固定：

> **Web 到来首先新增一种渠道，而不是把既有学校、电话、纸面和邮政系统瞬间清空。**

---

## 3. 2003–2005：网上咨询先成为全国性招生信息接口

学信网机构史称，2003 年非典期间举办全国大型网上高考咨询周，2004 年继续扩大；这是一条 **B / official retrospective**，适合证明服务谱系，不用于重建 2003 页面 DOM。

- https://www.chsi.com.cn/about/ct15.shtml

2005 年 5 月 10 日，教育部正式开通“阳光高考”信息平台，官方同时代公告保存 exact original URL：

```text
http://gaokao.chsi.com.cn
```

公告称平台提供：

- 分省分专业招生来源计划；
- 招生政策；
- 具有招生资格的院校名单；
- 各类考生资格名单；
- 院系设置；
- 录取规则；
- 往年录取情况；
- 学费、奖贷学金、食宿与办学条件；
- 在线咨询。

来源：

- **A / contemporaneous official announcement**：教育部，2005-05-09  
  https://www.moe.gov.cn/jyb_xwfb/gzdt_gzdt/moe_1485/tnull_5675.html
- **A / contemporaneous official consultation notice**：2005-05-30  
  https://gaokao.chsi.com.cn/gkxx/file/200505/20050530/28062.html

同年咨询周通知还保存另一个当时入口：

```text
http://www.gaokao.edu.cn
```

- **A / official**：教育部，2005-06-08  
  https://www.moe.gov.cn/jyb_xwfb/gzdt_gzdt/moe_1485/tnull_3811.html

### 可支持的 claim

- 2005-05-10 `gaokao.chsi.com.cn` 被官方作为阳光高考公网入口；
- 平台当时已承担公开招生信息与在线咨询；
- 全国性 Web 招生信息层已经形成。

### 不能支持

- 不能从今天仍可访问的同域页面倒推 2005 首页布局；
- 不能从“点击率”直接推算独立考生人数；
- 不能从平台存在推断所有地区正式志愿都在这个平台提交；
- 不能从同一域名延续推断 2005 与 2015 使用同一后端或前端技术。

---

## 4. 2006：咨询平台本身已经存在账号与可见性状态差

2006 年同期报道明确区分：

- 未注册用户：可浏览、搜索问题；
- 注册用户：可提交问题；
- 问题并非提交后立刻公开，而是在回答后显示；
- 高校有各自设定的咨询时间。

来源：

- **B / contemporaneous report**：2006-05-12  
  https://news.sina.com.cn/c/2006-05-12/09268905275s.shtml
- **A / contemporaneous platform notice**：2006-04-24  
  https://gaokao.chsi.com.cn/gkxx/file/200604/20060424/461618.html
- **A/B / contemporaneous platform news**：2006-04-26  
  https://gaokao.chsi.com.cn/gkxx/ss/200604/20060426/464337.html

因此永久保留：

```text
platform page reachable
!= consultation account registered
!= question submitted
!= question accepted / awaiting answer
!= answer completed
!= public Q&A visible
```

这对于 archive 特别重要：如果未来只保存了公开 Q&A，我们看到的是**已经越过审核/回答门槛的子集**，不是所有当年问题。

### Archive bias：answered-question survival bias

咨询页最可能保存：

- 被回答并公开显示的问题；
- 高校介绍和公告；
- 长期稳定 URL 的政策页。

最可能消失：

- 未回答问题；
- 被拒绝/重复的问题；
- 用户私有账号状态；
- 登录后的个人页面；
- 高校后台回答队列；
- 浏览但未提问的人。

因此“archive 中某类问题很多”不能直接等于“所有考生最关心这一类问题”。

---

## 5. 同一时期的真实基础设施是 Web + 电话 + 现场

2006 年河南省招生办公室公开安排同时提供：

```text
网上咨询：gaokao.chsi.com.cn
电话咨询：移动总机号码
现场咨询：郑州大学 / 河南农业大学 / 黄河科技学院
```

来源：

- **A/B / contemporaneous provincial admissions-office page**  
  https://gaokao.haedu.cn/145/369/2006/0523/79339.html

这条材料防止把 Web 写成孤立替代物。对于旧网考古应记录为 **channel stack**，而不是技术代际：

```text
Web does not imply phone removed
phone does not imply in-person removed
in-person does not imply Web unused
```

---

## 6. 2008–2009：正式志愿开始明显 Web 化，但省际流程不同

2008 年陕西首次网上填报志愿；同期报道仍要求考生结合纸质《招生考试特刊》中的学校/专业名称和代码，以及网上招生章程完成填报。

- **B / contemporaneous report**  
  https://news.sina.com.cn/o/2008-05-05/053713830335s.shtml

同一年，全国各省志愿制度并不统一：有考前填、估分填、知分填；填报渠道也存在地方差异。不能把某省第一次网上填报日期写成全国 Web adoption date。

- **B / contemporaneous comparison**  
  https://edu.sina.com.cn/gaokao/2008-03-20/1214129295.shtml

### 2008 内蒙古：同一个系统也可以有不同物理终端

同期报道里，一名考生在县中学电脑机房登录实时在线志愿系统；另一名城市考生则在家和父母操作。

- **B/T1 / contemporaneous observed use**  
  https://news.sina.com.cn/c/2008-07-23/013514202466s.shtml

因此：

```text
online filing mandated / available
!= home Internet access
!= candidate owns the terminal
!= candidate operates without assistance
```

archive 里即使看见一次成功登录，也无法知道现实键盘旁边是否还有老师、父母或同学。

---

## 7. 2009 陕西：取得一条非常清楚的事务状态链

陕西省教育考试院 2009 年官方说明是本 note 最重要的事务证据之一。

当时流程包括：

1. 考生用报名号和密码登录；
2. 填写志愿；
3. 点击“提交”；
4. 再进行“确认提交”；
5. 确认前可不限次数修改；
6. 确认后不可修改；
7. 确认提交后手机短信提示；
8. 中学/报名点下载并打印志愿确认表；
9. 考生纸面签字；
10. 中学/报名点上报；
11. 志愿最终生效。

来源：

- **A / contemporaneous provincial examination authority**：2009-06-01  
  https://www.sneea.cn/info/1027/2044.htm
- **A / contemporaneous three-year / vocational batch notice**：2009-07-01  
  https://www.sneac.com/info/1019/12408.htm

这要求旧网研究永久拆开：

```text
form page rendered
!= fields filled
draft saved
!= submit
submit
!= final confirm
final confirm
!= SMS delivered
SMS delivered
!= paper confirmation printed
paper confirmation printed
!= candidate signed
candidate signed
!= registration site uploaded final state
final state effective
!= later投档
```

### 一个非常重要的 archive 边界

Web archive 最有机会保存的是：

- 说明页；
- 公告；
- 登录页外壳；
- 静态 JS/CSS（若抓到）；
- 公开政策。

它几乎不可能合法、完整保存：

- 某个考生的报名号；
- 志愿草稿；
- 最终确认状态；
- 手机短信；
- 纸面签名；
- 招生后台投档/录取决定。

这可以命名为 **public-shell / private-admission-state asymmetry**。

---

## 8. `page != transaction`：正式填报不是阳光高考平台的同义词

2005–2009 同期资料常把 `gaokao.chsi.com.cn` 写成全国“阳光高考”咨询和信息平台；正式高考志愿则由各省级考试/招生系统按本地规则组织。

因此不要把以下对象合并：

```text
national admissions information platform
!= provincial preference-filing system
!= provincial投档 backend
!= institution admissions backend
```

如果一个历史截图同时出现“高考”“志愿”，也必须先确认 original URL 与主管单位，再判断它属于信息、模拟、正式填报还是结果查询。

---

## 9. 2009：纸质手册与 Web 正式事务并存

陕西已经网上填报时，《华商报》仍推出 48 版志愿填报手册，并增加外地零售量，内容包括招生政策、助学政策、网上填报技巧与高校资料。

- **B / contemporaneous newspaper**：2009-06-09  
  https://news.sina.com.cn/c/2009-06-09/022615756150s.shtml

旧网研究不应把纸面材料当“落后残余”。它可能承担：

- 离线比较；
- 家庭共同阅读；
- 代码抄写；
- 在正式登录前预先形成志愿表；
- 网络不可用时的参考。

Web archive 只保存线上层，会系统性低估这些纸面信息中介。

---

## 10. 2010–2015：信息更多，不意味着选择状态更容易解释

2010 年考生/家长调查报告显示，在其网络样本中，农民与农民工家庭考生到 4 月仍缺少明确志愿计划的比例较高。此材料不能用于全国总体估计，也不能证明 Web 造成或解决了阶层差异；它只提示：**正式界面统一后，解释规则与理解专业仍然不统一。**

- **B / contemporaneous survey report**  
  https://edu.sina.com.cn/gaokao/2010-04-14/1451242938.shtml

从旧网角度，这意味着未来如果找到一个“人人都能打开”的志愿页面，不应推断用户拥有同等的：

- 学校/专业知识；
- 家庭经验；
- 网络设备；
- 师资咨询；
- 对位次与往年线的解释能力；
- 出错后的恢复能力。

`same form != same navigational capacity`。

---

## 11. 搜索结果页、模拟志愿与正式志愿必须分开

2000s 后期开始出现大量教育门户、高考频道、论坛、博客与“志愿参考/模拟填报”内容。它们对历史研究很有价值，但必须先问：

1. 这是**官方招生数据**还是媒体整理？
2. 是**查询/模拟**还是正式事务入口？
3. 用户输入的数据是否只保存在该商业站点？
4. 推荐结果是否会进入省级招生系统？
5. 页面上“提交”是提交模拟方案，还是提交正式志愿？

永久写成：

```text
admissions-information page
!= preference-simulation page
!= official preference-filing page
```

界面文字相似不能抵消 provenance 差异。

---

## 12. Admission-result query 也不能和录取本身合并

个人结果状态同样需要拆开：

```text
institution makes admission decision
!= provincial system records decision
!= public query endpoint updates
!= candidate successfully queries
!= candidate believes result
!= paper notice generated
!= paper notice delivered
!= candidate enrolls
```

声讯电话、Web 和短信都可能只是**通知层**。一个“恭喜您已录取”的历史页面或截图可以支持当时某通知状态，却不能单独证明通知书送达、学费缴纳和真实报到。

---

## 13. Archive 偏差清单

### 13.1 information-page survival / personal-decision loss

最容易保存：

- 招生章程；
- 院校介绍；
- 专业介绍；
- 公开问答；
- 填报说明。

最难保存：

- 某考生实际考虑过哪些方案；
- 哪次修改是最后一次；
- 家庭争论；
- 老师代为解释；
- 最终为什么换专业/学校。

### 13.2 public-Q&A / unanswered-question bias

如果问题只有回答后才公开，那么 archive 天生看不到未回答问题和咨询队列。

### 13.3 HTML-form / backend-state gap

即使完整保存 `<form>`：

- 后端数据库不存在；
- 身份验证不可重放；
- 当年招生计划快照可能缺失；
- CSRF/session/cookie 状态不可恢复；
- “提交成功”无法从静态 DOM 推导。

### 13.4 Web / SMS / paper split

2009 陕西正式流程跨：

```text
Web → SMS → school printout → handwritten signature → school reporting
```

任何单一 archive 都只能看到其中一部分。

### 13.5 current page / historical UI gap

今天 `gaokao.chsi.com.cn` 仍是官方平台，且域名连续性很强；这反而增加误判风险：

> current content under historical host != historical page form

不能拿 2026 的 DOM、UTF-8、HTTPS、移动端样式或 JS 框架反推 2005/2009。

---

## 14. exact historical original URLs：本轮取得了什么

同时代官方材料明确保存：

```text
http://gaokao.chsi.com.cn
http://gaokao.chsi.cn
http://www.gaokao.edu.cn   # 2005 consultation-week announcement
```

来源：

- 教育部 2005-05-09  
  https://www.moe.gov.cn/jyb_xwfb/gzdt_gzdt/moe_1485/tnull_5675.html
- 教育部 2008-05-09  
  https://www.moe.gov.cn/jyb_xwfb/gzdt_gzdt/moe_1485/tnull_34254.html
- 教育部 2009-05-05  
  https://www.moe.gov.cn/jyb_xwfb/gzdt_gzdt/moe_1485/tnull_47120.html

这是 archive 定位的高价值 provenance。

### M1 capture 状态

本轮对上述域名/时间窗进行了公开 archive locator 检索尝试，但没有取得一份已经实际打开并能同时核验下列字段的历史 capture：

- `archive_source`
- `capture_url`
- `original_url`
- `capture_datetime`
- replay / HTTP state
- `Content-Type` / charset
- DOM / form structure
- form action / endpoint
- JS / iframe / image subresources
- second historical time point

因此严格记录：

**M1 verified historical `gaokao.chsi.*` 2005–2009 platform capture: NOT ACHIEVED IN THIS SLICE.**

这不等于“Wayback 当时没有保存”。

同样保持 UNKNOWN：

- 2005 首版 charset；
- IE / Netscape / Firefox 兼容要求；
- 是否存在特定 ActiveX/插件依赖；
- 2005 首页布局与 viewport；
- 2009 各省正式志愿系统的具体前端栈。

不要用“那个年代中文网站大概都……”补齐这些字段。

---

## 15. Provenance 风险：招生季存在大量相似页面

以后做 capture 调查时必须警惕：

- 教育部门官网；
- 省考试院；
- 高校招生网；
- 新闻门户转载；
- 商业教育门户；
- “模拟志愿”工具；
- 域名相似的非官方页面；
- 今天回填了旧文章日期的 CMS 页面。

一条历史页面至少记录：

```text
original URL
host owner / institutional provenance
publication datetime
capture datetime
page function
whether login is required
whether it is information / consultation / simulation / official filing / result query
```

“看起来像官方”不是 provenance。

---

## 16. 隐私边界

高考事务可能包含：

- 姓名；
- 身份证号；
- 考生号；
- 报名号；
- 手机号；
- 分数；
- 位次；
- 家庭地址；
- 志愿列表；
- 录取结果。

即使历史 archive 或截图偶然保留，不应为了复原界面而批量重新公开普通考生的可识别信息。

优先保存：

- 字段 schema；
- 流程与状态；
- URL pattern；
- 公共说明；
- 已脱敏截图/描述。

不要把“当年公开过”直接等同于“今天研究有必要再传播”。

---

## 17. 下一步最值得做的 old-Web 小任务

1. 以 `http://gaokao.chsi.com.cn/` 为 exact original URL，检查 2005、2006、2008、2009 的可回放 capture；
2. 每个时点至少记录 charset、title、导航、登录/注册入口、咨询入口、静态资源缺失；
3. 尝试找到 2006 “未注册可浏览 / 注册才可提问”的页面结构证据；
4. 选择一个省（陕西很合适）定位 2008–2009 正式志愿系统 exact original URL；
5. 明确区分阳光高考全国信息平台与省级正式填报平台；
6. 若能取得两时点再考虑进入完整 case；
7. 不追普通考生个人账号、志愿记录或敏感数据。

---

## 18. 已证实 / 高概率 / 不知道

### 已证实

- 2005-05-10 教育部开通 `gaokao.chsi.com.cn` 阳光高考信息平台；
- 2005–2006 平台已提供全国招生信息与在线咨询；
- 2006 同期材料明确存在“未注册浏览 / 注册提问 / 回答后显示”的状态差；
- 2008 陕西首次网上填报，且纸质招生材料与 Web 同时使用；
- 2009 陕西正式志愿流程包含登录、提交、确认提交、短信、纸质确认和报名点上报；
- 各省制度/时点不同，不能用一个省代表全国。

### 高概率但本轮不写成硬事实

- 学校机房在家庭无电脑/宽带时是重要的数字事务代理基础设施；有同期个案支持，但缺全国采用率；
- 2000s 后期 Web 信息增加使“解释信息”比“获取信息”更重要；有调查与个案支持，仍需更系统数据。

### 不知道

- 2005 阳光高考首版 DOM / charset / 浏览器兼容矩阵；
- 2005–2009 历史首页是否有可完整复核的两时点 capture；
- 全国各省正式网上志愿系统首次上线的完整年表；
- 普通家庭、学校机房、网吧三种终端在正式填报中的比例；
- 未回答咨询问题的规模与内容分布。

---

## 19. 本 note 改变了什么

旧网页考古很容易喜欢“可见的页面”，而高考志愿提醒我们：**真正重要的历史状态经常恰恰不在公开页面里。**

一个被完整保存的 2009 志愿说明页可以告诉后人按钮应该怎么按，却不能告诉我们某个考生最后按了什么；一张“提交成功”截图也不能证明学校端完成最终上报；一个录取查询页更不能证明这个人后来真的去报到。

因此招生 Web 的研究单位不应是“某年高考网站长什么样”，而应是：

> **哪些人生决定第一次被写进网页字段，哪些状态必须跨出 Web 才生效，而 archive 又系统性保存了哪一层、丢掉了哪一层。**

这也是中文旧网与普通生活史真正能够互相校正的地方。
