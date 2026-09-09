# 高考志愿咨询、纸卡/网报、保存、确认、投档、录取与结果查询之间的状态缺口（中国，2002—2015）

> Scope：本文严格服务于 `old-web-archaeology` 的约 1995–2015 中文旧网主范围。它不是中国高考制度通史，也不把 2020s AI 志愿工具扩写成本仓主线。更长的前互联网生活史、1960s 英国 UCCA 对照、2019 与 2020–2026 的 life-horizon 比较见：
> https://github.com/tmzncty/how-people-lived/blob/main/topics/from-paper-preference-card-to-algorithmic-future-rehearsal-gaokao-choice-interfaces-and-admission-futures-china-1980-2026.zh-CN.md
>
> 核心考古问题：一张历史网页如果写着“网上填报志愿”“提交成功”“录取查询”“征集志愿”，研究者究竟能证明到哪一层？招生咨询页、正式填报 host、登录 session、页面里已经输入的字段、保存记录、确认记录、省级招生数据库、投档、院校审阅、预录取、退档、正式录取与一个考生最终是否去那所大学，并不是同一个对象。

本文与仓库已有专题分工：

- `CIVIL_SERVICE_ONLINE_REGISTRATION_QUALIFICATION_PAYMENT_ADMIT_CARD_AND_HIRING_STATE_GAPS_2004_2015.md`：公务员考试报名与任用；
- `docs/ONLINE_RESUME_PROFILE_EMPLOYER_SEARCH_APPLICATION_VIEW_AND_CANDIDATE_STATE_GAPS_1999_2015.md`：求职简历与招聘流程；
- `CREDIT_APPLICATION_REPORT_QUERY_AND_UNDERWRITING_STATE_GAPS_2000_2015.md`：信用申请与审批；
- 本文：**高考志愿从信息获取、纸卡/网上填报进入省级权威记录，再经投档和高校审阅变成录取结果的状态链。**

---

## 1. 为什么“高考网报页面”是特别危险的历史对象

一张 archive 很容易留下：

- “高考志愿填报”标题；
- 用户名/报名号输入框；
- 学校、专业代码输入栏；
- “保存”“提交”“确认”“安全退出”按钮；
- 一张招生计划或院校列表；
- “录取查询”入口；
- “征集志愿”公告；
- 一段“提交成功”的前端提示。

但真实事务至少应拆成：

`candidate identity`
`exam score / rank`
`public information / consultation page`
`official filing host`
`authenticated session`
`local browser form state`
`draft preference`
`saved server-side preference`
`submitted preference`
`confirmed / frozen preference`
`paper confirmation (where required)`
`authoritative provincial admissions record`
`current admissions-plan snapshot`
`filing deadline state`
`投档 / matching`
`institution review`
`预录取 / 预退档 / 退档`
`formal admission`
`征集/征求志愿 eligibility`
`result-query response`
`actual enrolment / registration`。

任何一步都不能从前一步自动推出。

---

## 2. 对象模型

### 2.1 Public information / consultation site

招生政策、院校介绍、在线答疑、BBS、招生章程、计划查询。

它可以帮助考生理解选择，但未必拥有正式提交志愿的事务权限。

因此：

`official-looking consultation page ≠ official filing endpoint`。

### 2.2 Candidate identity

可能由：

- 报名号；
- 准考证号；
- 身份证号；
- 密码；
- 后来的手机号/短信验证码；
- 线下准考证/身份证恢复流程

共同构成。

身份凭据属于高敏感数据，历史考古不应追求复原普通人的真实账号。

### 2.3 Draft / local form state

浏览器里已经显示的院校、专业字段。

如果尚未保存或提交，它甚至可能只存在于当前 DOM / 表单控件里。

### 2.4 Saved preference

服务器端已经收到但仍可能修改的志愿。

页面“看得到”与服务端“保存成功”应分开。

### 2.5 Submitted / confirmed preference

不同省份/年份语义不同：

- 有的“提交”后仍可有限次数修改；
- 有的还有“确认提交”；
- 有的以最后一次成功提交为有效志愿；
- 有的曾在线填完后再由学校打印、本人签字；
- 后来一些地区改为短信验证码/人脸等纯在线确认。

所以不能创建一个跨省、跨十年的统一 `submitted=true` 字段来替代历史语义。

### 2.6 Authoritative admissions record

省级招办/考试院用于投档的权威志愿记录。

这是考古链上最关键、却几乎最不可能进入公共 Web archive 的状态。

### 2.7 Plan / code snapshot

同一个院校代码、专业代码、计划数、选科/身体条件，在不同年度可以变化。

今天打开一个仍然存活的“院校专业库”，若后端返回 2026 数据，不等于历史 2009 页面当时可见的数据。

### 2.8 Admission state

至少需要区分：

`未投档`
`已投档`
`院校在阅`
`预录取`
`预退档/退档`
`正式录取`
`未录取但可参加征集`
`录取后未报到`。

历史“录取查询”页面的模板存在，不证明某个考生曾得到其中任何具体状态。

---

## 3. 基本状态链

### 3.1 纸卡—电子档案混合链

`咨询/招生材料`
→ `考生写草卡`
→ `填涂正式志愿卡`
→ `学校/招办验收`
→ `机读/人工采集`
→ `形成电子志愿档案`
→ `考生校对/签字`
→ `省级权威记录`
→ `投档`
→ `院校审阅`
→ `录取结果`。

### 3.2 典型 Web 填报链

`找到官方 host`
→ `输入报名号/密码`
→ `建立登录 session`
→ `读取当年计划/填报说明`
→ `输入院校/专业`
→ `保存/提交`
→ `查看是否成功`
→ `在截止前修改`
→ `最终确认/最后一次有效提交`
→ `权威记录冻结`
→ `投档`。

### 3.3 征集志愿链

`上一轮未被正式录取`
→ `招生机构公布剩余计划`
→ `考生确认自己有资格`
→ `在很短窗口重新填报`
→ `成功提交`
→ `再次投档/审阅`
→ `结果查询`。

因此：

`第一次志愿未兑现 ≠ 当年招生流程已经终止`。

---

## 4. 2002—2004：后台已经联网，考生端仍可主要依赖纸

### 4.1 2002 广东：remote online admission 不是 candidate online filing

2002 年广东第二批 223 所招生院校中，195 所采用远程网上录取，另外 28 所因网络条件不具备而在现场局域网录取。

同期来源（B）：
https://news.sina.cn/sa/2002-08-21/detail-ikknscsi0214704.d.html

CERNET 2003 年的近同时代总结还指出，网上录取要求省级招办先把报名、体检、成绩、志愿等制作成电子档案。

来源（B）：
https://www.cernet.edu.cn/edu/yuan_cheng/yuan_cheng_jiao_yu/200603/t20060323_71542.shtml

因此 old-Web 研究必须拒绝：

`universities admitted online in 2002`
→ `ordinary candidates filled preferences online in 2002`。

这两个对象可以相差多年。

### 4.2 2004 重庆：同一年同时存在在线咨询、纸卡和电子档案

2004 年同期招生报道记录：考生先参加网上咨询；随后试填“志愿草卡”、填涂《志愿卡》；学校验收，区县招办集中把卡制成电子档案；考生通过校对册签字认可后再统一上报。

来源（B）：
https://edu.sina.cn/sa/2004-05-09/detail-ikftpnny8666886.d.html

这个案例至少要拆成：

`consultation website`
≠ `paper preference card`
≠ `digitized preference record`
≠ `candidate-approved electronic record`。

它也是本专题最清楚的 `consultation / transaction gap`。

---

## 5. 2008：网上填报成为用户事务，但执行环境仍然混合

### 5.1 学校计算机房是执行基础设施的一部分

2008 年江苏模拟网上填报时，同期记者在南京大学附属中学观察到：学生吴健先接受约两小时培训，再进入计算机房打开指定网址；首次登录需要修改密码，模拟填报约 20 分钟。

来源（B，同时代现场报道）：
https://edu.sina.com.cn/gaokao/2008-06-13/1419147633.shtml

所以：

`online filing exists ≠ home broadband/device independently available to every candidate`。

一张历史网页的“在线”属性不能告诉我们考生实际是在：

- 家里；
- 学校机房；
- 县招办；
- 网吧；
- 借用亲友电脑

完成操作。

### 5.2 内蒙古：页面上的 rank 是一个会变动的动态状态

2008 年内蒙古实时网报材料中，考生李娜登录后能看到院校招生计划、调档线、当前报考人数和自己的动态位置；自治区招生系统同年还新增“平行分人数”等显示。

来源（B/A-B）：
https://news.sina.com.cn/c/2008-07-23/013514202466s.shtml
https://gaokao.chsi.com.cn/gkxx/ss/200807/20080722/7689883.html

这造成一个非常重要的保存边界：

`captured displayed rank ≠ final rank at deadline`。

如果 archive 恰好保存一张 10:30 的静态结果页，也不能把它当成 12:00 截止时的最终竞争位置。

---

## 6. 2009—2011：save / submit / confirm / final record 必须拆开

### 6.1 2009 湖北：30 分钟会话让“决策时间”和“页面时间”分离

省招办同期指引建议先在纸上填写志愿草表，进入系统后每次登录只有 30 分钟；超时自动退出，15 分钟后才能重新进入；每批次完成后必须点击“保存”；关闭浏览器后建议再次登录“查询志愿”验证是否真的保存。

来源（B）：
https://www.gkzxw.com/Article/200906/34145.html

因此可定义：

- `decision-time / session-time gap`：考生可能在纸上想几天，Web session 只有 30 分钟；
- `form-filled / saved-state gap`：控件里有内容不等于服务器有记录；
- `save-response / later-query gap`：一次成功提示最好还需重新查询确认。

### 6.2 2010 湖北：official-host provenance 直接关系未来控制权

2010 年湖北公开的正式填报 host 包括 `http://tbzy-dx.hubzs.com.cn` 等；省招办明确提醒考生必须核实指定网址，不要在非官方站点输入报名号、身份证、准考证号和分数。

来源（B，同期报道）：
https://news.sina.com.cn/c/2010-06-05/083417614103s.shtml

这构成 `official-host / search-result provenance gap`：

> 页面写着“高考志愿填报”不证明它是有权写入省级招生记录的 host。

在 old-Web capture 里，favicon、标题、页面抄袭甚至域名包含“gaokao”都不是授权证据。

### 6.3 2011 山东：最后一次成功提交才是有效志愿

山东 2011 年告知书明确记录：考生可自行选择上网地点，应届毕业生也可到原中学，其他考生可到县区招办指定地点；首次登录要修改初始密码；每批志愿必须点击“提交保存志愿”；提交后最多允许修改两次；最后一次提交成功的志愿才是该批次有效志愿；志愿必须由考生本人填报。

来源（A/B：同期学校转发省级告知书）：
https://www.sdecu.com/zsc/info/1022/1613.htm

这说明：

`first submitted state ≠ effective final state`。

archive 若保存一张早期页面或截图，也不能推断那就是截止时权威数据库里的最终志愿。

### 6.4 2011 陕西：同一年度还可能有“提交 → 确认提交”两级动作

陕西 2011 年说明列出正式 host `www.sneac.com` / `www.sneac.edu.cn`，考生用 14 位报名号或 10 位准考证号加密码登录，完成批次后点击“提交”，并继续完成确认步骤。

来源（A/B：同期高校招生网站保存的省级说明）：
https://zs.xust.edu.cn/info/1124/1973.htm

对考古来说，“提交按钮截图”只能证明 UI 提供该动作，不能自动证明：

`submitted → confirmed → effective` 三者在某次真实 session 中都完成。

---

## 7. 征集志愿：录取结果也是后续事务的前置条件

### 7.1 2010 湖北：征集窗口短，host 与普通志愿共用

2010 年湖北第一批本科等征集志愿要求考生在指定日期登录 `tbzy-dx.hubzs.com.cn` 或教育网 host，截止当日下午 5 点，过时系统关闭。

来源（B）：
https://edu.sina.com.cn/gaokao/2010-07-19/0936259115.shtml

因此研究者若只保存“征集志愿页存在”，仍不知道：

- 该考生此前是否未录取；
- 是否达到本轮资格线；
- 截止时是否仍有对应计划；
- 是否真的成功提交。

### 7.2 2011 浙江：结果查询与再填报组成闭环

浙江省教育考试院第一批征求志愿公告要求考生先确认自己是尚未录取、符合条件的人；当天 8:30—17:30 网上填报；以最后一次成功提交为最终志愿；提交后还要“查看志愿”确认。

来源（A，经阳光高考保存）：
https://gaokao.chsi.com.cn/gkxx/ss/201107/20110717/221998107.html

这构成：

`admission-state query`
→ `eligibility`
→ `new plan snapshot`
→ `new preference transaction`。

所以录取查询不是只读终点，它有时决定考生能否进入下一轮写操作。

---

## 8. 主要 state gaps

### 8.1 consultation / transaction gap

招生咨询、BBS、院校问答可以是官方的，但未必具有写入正式志愿的事务权限。

2004 重庆就是典型：网上咨询真实存在，正式志愿仍由纸卡进入电子档案。

### 8.2 paper-card / electronic-record gap

纸卡上的内容、机读/人工采集后的电子记录和考生签字校对后的最终记录可能不一致。

保存纸卡模板不能证明某一考生权威电子档案是什么。

### 8.3 browser-form / authoritative-preference gap

页面控件显示已经填满，不等于服务器已保存，更不等于省级权威志愿记录已经冻结。

### 8.4 save / submit / confirm gap

不同省份、年份对“保存”“提交”“确认”定义不同。

历史复原必须引用当年说明，不能用现代站点的按钮语义倒推。

### 8.5 confirmation-message / effective-record gap

短信或页面提示“成功”通常只能证明系统返回某种确认；若没有后台记录，不能进一步推出投档数据库一定采用了该状态。

### 8.6 session-timeout / decision-time gap

2009 湖北 30 分钟 session 不代表考生只花 30 分钟做决定。大量思考可能发生在纸草表、家长/老师讨论和网页之外。

### 8.7 plan-page / plan-snapshot gap

招生计划、专业代码、缺额和限制条件是年度且可能分轮次变化的状态。

今天同 URL 返回的数据库内容不能回填成当年数据。

### 8.8 displayed-rank / deadline-rank gap

内蒙古实时网报的当前排名会随着其他人修改而变化。

一次 capture 是时间片，不是最终录取边界。

### 8.9 official-host / lookalike-site gap

相似页面、搜索结果、广告甚至假 App 不具备官方事务权威。

old-Web 证据需要当年的招生公告/机构链接来确认 host provenance。

### 8.10 password-possession / candidate-authorship gap

拿到报名号和密码的人技术上可能操作账号，但并不等于其行为代表考生本人意愿。

因此真实账号凭据和普通人的志愿历史不应被重新公开。

### 8.11 candidate-submission / admission-outcome gap

即使志愿有效提交，仍要经过成绩/位次、招生计划、投档规则、院校审阅和专业分配。

`submitted preference ≠ admission`。

### 8.12 admission-result / actual-enrolment gap

被正式录取也不等于最终到校注册。

录取后放弃、未报到、复读等属于另一个 life-course 状态。

---

## 9. 浏览器、网络和终端条件

### 9.1 网报并不自动等于“家庭 PC 自助”

需要记录：

- 学校是否提供机房；
- 县市招办是否有指定上网点；
- 是否允许网吧/家庭；
- 是否需要特定浏览器；
- 当年页面是否依赖 JS、frames、ActiveX 或特定编码；
- 高峰期是否存在拥塞/超时。

2008 江苏机房模拟和 2011 山东“可回学校/县招办上网”都说明终端环境属于历史事实的一部分。

### 9.2 charset / input / code table

志愿系统高度依赖院校、专业代码。即使页面 HTML 保存完整，若历史计划表、代码表或 JS 校验缺失，研究者也可能无法知道当时哪些值是合法输入。

### 9.3 session 与 cookie

登录后页面通常与临时 session 绑定。archive crawler 即使保存登录壳，也不应期待重放真实普通用户的认证状态。

---

## 10. Archive / preservation bias

### 10.1 public-shell survival / private-transaction disappearance

最容易保存：

- 填报说明；
- 公告；
- 登录页；
- 招生计划；
- 操作教程。

最难/不应公开保存：

- 真实报名号；
- 身份证信息；
- 分数与位次；
- 私人志愿表；
- session；
- 最终权威志愿；
- 个体投档/退档内部理由。

因此：

> **越能证明某一个具体年轻人的人生未来最终怎样被写入系统的材料，越可能天然位于公共 archive 的边界之外。**

### 10.2 successful-final-state bias

最终录取通知和学校新生名单相对更容易留下，但它们会把此前多次修改、未投档、退档、征集志愿等中间未来折叠掉。

### 10.3 instructions survive better than failures

官方操作说明会被重复转载；普通人一次“忘记点保存”“最后五分钟掉线”的失败通常只存在论坛、博客或私人记忆里。

这会系统性低估旧网事务的操作摩擦。

### 10.4 current-backend rehydration

若 2009 的旧 URL 今天仍能访问，却调用现代招生数据库/现代统一身份系统，它只能证明 `current backend` 在旧路径上重新提供内容，不能称为 2009 historical replay。

---

## 11. Preservation levels（建议）

### S0 — brand/host known

只知道某省存在一个网报系统或域名。

### S1 — public instruction page

有同期公告/教程，能证明 host、日期、基本步骤。

### S2 — login shell

保存登录页、字段、编码/浏览器条件。

### S3 — authenticated UI structure

在不暴露真实个人数据的前提下，有官方截图/手册证明登录后页面结构。

### S4 — draft/save/submit semantics

能从当年规则明确区分保存、提交、确认、修改次数、截止时间。

### S5 — plan/rule snapshot

同时保存该轮招生计划、代码和投档规则，能解释合法输入空间。

### S6 — synthetic transaction reconstruction

使用虚构/测试数据复原状态机，并清楚标 `reconstruction`；不尝试登录真实历史账号。

### S7 — cross-evidence transaction model

由官方规则 + 同期现场/用户材料 + 技术 artifact 共同证明实际操作链和主要失败点。

### S8 — historically faithful but privacy-safe environment study

在旧浏览器/旧编码假设下验证页面结构与客户端行为，同时明确后台不可复现部分；不以恢复任何真实考生志愿为目标。

---

## 12. 本轮 historical replay 尝试

本轮针对能从同期材料精确定位的历史 host 做了 archive 入口搜索，重点包括：

- `www.sneac.com` / `www.sneac.edu.cn`（陕西 2011）；
- `tbzy-dx.hubzs.com.cn`（湖北 2009–2010）；
- `zy.sdzk.gov.cn`（山东 2011）。

Web 搜索未返回可直接核验的 Wayback memento。随后尝试直接请求 Internet Archive CDX 查询 `www.sneac.com` 的 2010–2012 capture，当前研究环境因 URL provenance 安全限制拒绝打开构造的 CDX URL。

因此本轮正式记录：

`M1 verified historical gaokao preference-filing capture: NOT ACHIEVED IN THIS SLICE`。

这只表示：

- 本轮没有实际打开并验证一份满足仓库 METHOD 的 historical memento；
- **不能**推出 Wayback 当时没有保存；
- **不能**把搜索结果里的候选 locator 升级成 capture；
- 同期官方/媒体材料仍足以证明这些 host 与操作规则在当时存在。

下一轮若取得 archive provenance，应至少记录：

`archive_source / capture_url / original_url / capture_datetime / accessed_at / HTTP state / redirect / charset / DOM / form action / JS dependencies / login or error shell / subresource gaps`。

---

## 13. 已证实 / 高概率 / 不知道

### 已证实

- 2002 广东高校端已经大规模远程网上录取；
- 2004 重庆存在“网上咨询 + 纸质志愿卡 + 制作电子档案 + 考生校对”的混合流程；
- 2008 江苏有学校机房组织网上模拟填报；
- 2008 内蒙古动态网报能向考生显示当前报考/排名信息；
- 2009—2011 多省正式网报说明明确存在登录、密码、保存、提交、查看、修改、截止时间等事务语义；
- 2011 山东/陕西有可定位的正式 host 和详细操作步骤；
- 征集志愿要求把前一轮录取状态作为下一轮事务资格的前置条件。

### 高概率但仍需更多技术 artifact

- 这些系统普遍依赖 cookie/session 与动态后台；
- 大量历史操作失败、拥塞和局部浏览器兼容问题不会被公开 archive 系统性保存；
- 普通考生真实 transaction state 远比公开说明页更难保存。

### 不知道

- 本轮未验证 2009–2011 上述 host 的真实 Wayback DOM/charset/form action；
- 未验证各 host 在不同批次是否使用完全相同前端；
- 未验证具体省份当年对浏览器版本、控件或网速的最低要求；
- 无法从公共证据恢复任何普通考生真实的最终志愿，这也不应成为研究目标。

---

## 14. 后见之明风险

### 风险 1：把“网上录取”写成“网上填志愿”

这是最需要避免的概念滑移。后台先联网完全可能发生在考生端 Web 自助之前。

### 风险 2：用今天统一的 UI 心智模型理解 2000s 省级系统

各省对提交、确认、修改次数、纸质签名的定义不同，必须按年份/地区读取规则。

### 风险 3：把 modern live URL 当 historical capture

旧 host 若被复用或重定向，今天的结果不是当年数据。

### 风险 4：把页面保存成功当志愿事务保存成功

HTML archive 和招生权威数据库是不同证据层。

### 风险 5：为追求“完整体验”而恢复普通人的隐私

分数、身份证、报名号、志愿和录取内部状态属于高度敏感的教育档案。本仓应保存结构与规则，而不是重新公开真实私人 transaction history。

---

## 15. 本专题改变的 old-Web 认识

高考志愿系统是一个很强的反例，说明中文旧网不能只按“页面形态”写历史。

一个 2009 年页面也许看起来极其朴素：几个文本框、下拉框、保存按钮。可它背后连接的是：

`一个十七八岁的人对未来四年的选择`
→ `省级招生数据库`
→ `数百万竞争者和有限计划`
→ `高校审阅`
→ `最终教育迁移`。

因此历史网页的意义有时不在视觉复杂度，而在 **state transition authority / 状态转换权威**：这个页面上的一次正确确认，真的有能力改变一个人下一年住在哪座城市、进入什么专业。

旧网考古如果只保存 HTML，就最容易保存“界面曾经存在”；真正困难的是承认——**那个界面当时之所以重要，是因为它后面连着一个我们今天既无法、也不应该完整重放的权威人生分配系统。**

AI-assisted initial research draft; factual claims are linked to auditable contemporary/institutional evidence, and reconstruction boundaries are explicit.