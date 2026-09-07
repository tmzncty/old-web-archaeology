# 中文旧网高考志愿：网上咨询、志愿填报、确认、录取与未来选择状态缺口（2003—2015）

## Scope

本笔记只研究约 **2003—2015 中文旧网中与普通高考志愿直接相关的 Web / 网络事务**，重点包括：

- 高考成绩、位次与往年录取资料查询；
- 全国/高校网上招生咨询；
- 省级网上志愿填报；
- 学校/报名点工作站；
- 考生账号、密码、验证码/证书等身份状态；
- 志愿草稿、保存、提交、确认、打印、签名、上传/生效；
- 网上录取后台与候选人前台的区别；
- SMS / 声讯电话与 Web 的并行；
- 历史页面、动态事务状态和 archive preservation 的差异。

不把本仓扩成整个中国高考史，也不把 1990s 招生信息化前史变成本仓主对象。1996—2002 的网上录取只作为理解 2003—2015 中文旧网的边界：**招生后台联网早于普通考生全面网上填志愿。**

普通生命历程、四种未来时间感、家长/老师/考生决策权与法国 Minitel RAVEL 对照，放在 `tmzncty/how-people-lived`：

- `topics/from-paper-volunteer-forms-to-digital-future-menus-gaokao-choice-major-city-and-life-branching-china-1999-2026.zh-CN.md`

---

## 一、研究单位：不要把“高考网站”当成一个页面

一次普通高考志愿至少可能跨越：

```text
招生计划/专业目录发布
→ 考生成绩/位次发布
→ 信息查询
→ 招生咨询
→ 考生身份与账号
→ 志愿草稿
→ 在线输入
→ 逻辑校验
→ 保存
→ 提交
→ 最终确认
→ SMS/页面反馈
→ 学校下载/打印
→ 本人纸上签名（部分省份/年份）
→ 报名点/学校上报
→ 志愿最终生效
→ 省级投档后台
→ 高校审阅电子档案
→ 预录/退档
→ 省级审核
→ 正式录取
→ 结果查询
```

这些对象必须分开：

- **information platform**：例如“阳光高考”；
- **provincial exam authority site**：省级考试机构网站；
- **volunteer transaction system**：正式志愿填报系统；
- **admission backend**：省招办—高校网上录取后台；
- **candidate account**：考生登录身份；
- **paper artifact**：专业目录、草表、打印确认表；
- **telephone/SMS channel**：与 Web 并行的查询或确认通道；
- **page / URL**：静态公告、帮助页、登录页、结果页；
- **transaction state**：草稿、保存、确认、生效等；
- **capture**：档案服务保存的某一历史表示。

尤其禁止：

> `网上录取 = 网上填志愿 = 在线咨询 = 考生家庭已经普遍联网`

这四个等号都不成立。

---

## 二、前史边界：招生后台联网早于候选人 Web 前台

教育部 2001 年官方通知要求全国各省级区域普通高校招生实行网上录取，并明确区分现场局域网录取和远程广域网录取；2002 年招生文件进一步要求计算机网上录取并尽量采用远程异地方式。[S1][S2]

2003 年 CERNet 的技术回顾记录，从 1996 广西试点到 1999 年 10 个省市、478 所高校，再到 2002 年近 1600 所高校/全国 31 个省级区域，考生报名、体检、成绩、志愿已被制作成电子档案供网络录取后台使用。[S3]

这说明一个非常重要的技术边界：

### `candidate-data-digitized / candidate-Web-submission gap`

```text
志愿已经进入电子档案
≠
考生本人通过浏览器提交志愿
```

所以本仓遇到 2000—2002 的“网上录取”材料时，只能证明录取工作流数字化，不能把它写成普通家庭 Web adoption。

---

## 三、2003：Web 先承载查询，电话、短信和拨号网络并行存在

北京 2003 年“高考录取资料网上查询系统”的同期材料给出了一组很珍贵的 locator：[S4]

```text
www.bbn.com.cn
www.bjeea.edu.cn
```

考生购买 10 元、当天有效的查询“门票”后，可检索：

- 1999—2002 年全国高校在京招生录取统计；
- 本人成绩在北京市/区县中的相对位置；
- 往年报考院校录取考生成绩分布。

当时同时支持：

- 16900 主叫/注册拨号；
- ADSL；
- LAN；
- `1606789` 声讯电话查询成绩；
- 手机短信成绩服务。[S4]

### 已能证明

- 2003 年招生信息已经存在 Web + PSTN/声讯 + SMS 的多入口结构；
- Web 查询可能与电信计费耦合；
- “可获得录取数据”早于“正式选择必须在 Web 上完成”。

### 仍不知道

- 2003 原始页面 HTTP headers；
- 精确 charset；
- 登录/购票表单是 GET/POST 还是其他方式；
- session/cookie；
- 是否依赖 IE-only 脚本；
- 电信计费结果如何回写 Web 会话；
- 三次登录机会在后端怎样计数；
- 错误页和超时页具体怎样呈现。

### 状态缺口

`data-visible / transaction-authoritative gap`

看到往年数据不意味着该页面本身承载正式志愿提交。

---

## 四、2004—2005：全国咨询平台把“招生老师在线”做成旧网常见事务

### 1. 2004 网上咨询周

教育部 2004 年公告给出：[S5]

```text
www.chsi.com.cn
www.cernet.cn
www.gaokao.edu.cn
```

考生和家长可以在网上咨询周通过这些站点/BBS 向教育部、省市招办和高校人员提问。

这里应拆成：

```text
question drafted
→ submitted
→ accepted by platform
→ visible/moderated
→ answered
→ answer read
→ answer understood
→ answer affects preference
```

`question-submitted / answer-visible gap` 不能忽略。

2005 年教育部又在 `gaokao.chsi.com.cn` 开通“阳光高考”信息平台，把招生政策、计划、资格、院校介绍、章程、往年录取、奖贷学金和在线咨询等聚到同一公共入口。[S6]

这时平台主要是 **information / consultation layer**。它与各省的正式志愿交易系统不能默认是同一个后台、同一账号体系或同一 URL。

### 2. archive preservation 风险

2004–2005 的咨询页面可能包括：

- BBS 问题列表；
- 回答状态；
- 院校专区；
- 动态时间窗口；
- 管理后台设定的咨询时间；
- 登录后提问；
- 搜索/翻页；
- 高校回答正文。

即使今天还能访问官方“咨询周”公告，也不等于这些当年的事务页面、session 和动态内容还存在。

### `announcement-survives / transaction-state-survives gap`

官方静态公告的保存概率通常远高于真实用户问答和登录状态。

---

## 五、2005 广东：网上志愿是纸—网—学校工作站共同系统

广东省 2005 年普通高考网上志愿官方通知保留了一个接近完整的事务合同。[S7]

### 1. 基础设施层

通知要求建立：

```text
省
→ 市
→ 县（区）
→ 中学/报名点工作站
```

并因网络负载把 21 个地市分组、分时段进行填报。

地方可以根据网络速度：

- 让考生自行网上填报；
- 或集中到中学/指定工作站填报。

对没有 Internet 条件的考生，县级招考机构要提供上网环境。

所以：

### `service-online / household-online gap`

**正式事务已经在线，不代表每个家庭必须拥有私人 PC 和宽带。**

学校工作站本身是 Internet adoption 的重要历史节点。

### 2. 纸质目录仍是 authoritative source

考生必须先依据当年正式《招生专业目录》和补充材料，填写纸质志愿表，再把院校和专业代码录入网上系统。[S7]

因此：

```text
printed plan
→ paper draft
→ online entry
```

不是“Web 取代纸”，而是 **paper–digital braid / 纸—网编织**。

### 3. 登录状态

官方通知记录：

- 考生通过考生号和预留密码登录；
- 没有预留密码的考生使用初始密码 `a1b2c3`；
- 首次登录后必须更改；
- 机构一侧还涉及证书/工作站身份。[S7]

这个历史事实只用于描述当时认证状态，**不能据此展开现实系统攻击、不能推断相同机制在其他年份/省份存在。**

### 4. 逻辑校验与红色错误提示

系统会根据输入的学校/专业代码做逻辑检查，无效信息以提示方式要求纠正。

因此：

`typed-code / semantically-intended-choice gap`

数字表单可以防一部分非法组合，却不能判断“这个专业真的是考生以为的那个专业”。

### 5. 截止、打印和签字

在允许修改期结束后，学校打印正式志愿表，考生核对、签名后进入档案。[S7]

所以早期广东网上志愿至少有：

```text
entered
→ server-valid
→ deadline reached
→ printed
→ checked
→ signed
→ archived
```

### `online-filled / legally-effective gap`

不能把浏览器中已经出现志愿内容直接等同于最终有效档案。

---

## 六、2006：同一制度既可以 Web，也可以电话；渠道不是整齐替换

2006 年北京同期报道记录，当年新增声讯电话填报志愿路径，固定电话拨打 `1606790`，同时仍可访问：[S8]

```text
www.bjeea.cn
gk.bbn.com.cn
```

用户需要准备：

- 考生号；
- 密码；
- 特征码；
- 学校代码；
- 专业代码。

这进一步证明：

### `channel convergence without channel death`

Web 并没有立刻杀死电话事务。

对于一些家庭，电话可能比不稳定的 PC/宽带更熟悉；对于另一些家庭，Web 可以更容易查看和修改多项志愿。

历史研究不能把“系统提供 Web”当成“所有人只用 Web”。

---

## 七、2007：页面“提交成功”以后，仍可能需要线下确认与安全补偿

2007 年北京一次网上志愿相关安全事件的同期报道中，北京教育考试院强调，网上填报后报名单位仍会组织考生签字确认。[S9]

本仓不复述攻击细节，也不把一则事故外推成整个系统“不安全”。

它的价值在于证明：

### `online-submitted / finally-confirmed gap`

某些纸质确认/报名单位流程不只是“落后的遗留”，也可能承担：

- 身份复核；
- 最终意愿确认；
- 异常发现；
- 事务恢复。

### `offline fallback as integrity layer`

旧的线下层有时是新数字层的 integrity fallback，而不是简单的冗余。

---

## 八、2008：省际异质性非常大，不能造一条全国同步迁移史

湖北省考试机构保存的 2008 招生说明显示，同一年仍存在：[S10]

- 机读志愿卡；
- 纸质志愿表；
- 网上填报；
- 不同地区采用不同方式；
- 不同批次在估分填报与知分填报之间存在不同安排；
- 网上远程录取后台已经普遍运行。

所以：

### `national-brand / provincial-execution gap`

“2008 年高考志愿”不是一个全国统一浏览器体验。

任何逐年时间线都至少需要标记：

- province；
- batch；
- candidate type；
- fill timing；
- paper/online mode；
- confirmation mode；
- system host；
- whether score/rank was known。

否则非常容易把北京、广东、湖北、陕西的流程拼成一个不存在的“全国用户”。

---

## 九、2009 陕西：把正式志愿拆成状态机

2009 年陕西的网上填报说明提供了本专题最清晰的状态边界之一。[S11]

### 1. 在线阶段

```text
login
→ fill
→ click “提交”
→ can still modify
→ click “确认提交”
→ no further modification
→ SMS confirmation
```

截止前没有“确认提交”，已填写内容仍无效。

### 2. 纸面阶段

确认提交以后：

```text
school/download
→ print confirmation form
→ candidate signs
→ school/reporting-point uploads/reports signed choice
→ final effective state
```

拒绝签字同样导致志愿无效。[S11]

由此必须拆开：

### `draft / submit / final-confirm / signed / uploaded / effective`

它们不是同义词。

### 3. 历史截图的解释规则

如果未来只找到一张：

- “提交成功”；
- SMS 提示；
- 志愿表打印页；

都不能单独证明最终有效。

必须问：

> 这个截图对应事务链中的哪个状态？后续状态是否有证据？

---

## 十、2009：平台能把专业展示出来，却不能保证考生理解专业

《中国青年报》2009 年在线调查和人物采访显示，一大部分受访者认为考生对高校和专业了解不足；受访者信息来源仍混合了老师、志愿指南、父母亲友、网络、高校网站和学长学姐。[S12]

对 old-Web 考古的意义不是社会心理本身，而是：

### `information-rendered / information-understood gap`

```text
school page exists
professional plan downloadable
BBS answer visible
≠
candidate understands future curriculum/job
```

所以一个 2009 年“学校介绍页面被成功 capture”只能证明历史信息对象存在，不能证明普通用户当时获得了足够理解。

---

## 十一、2015 湖北：事务 Web 已经日常化，但保存/超时/退出仍然是制度状态

2015 年湖北省网上填报说明给出正式入口：[S13]

```text
http://tbzy.hubzs.com.cn
```

操作步骤包括：

1. 依据志愿草表进入对应批次；
2. 输入学校/专业代码；
3. 系统把代码转换成名称并提示无效代码；
4. 点击“保存”；
5. 使用“查询志愿”检查；
6. “安全退出”。

同时规定/提醒：

- 单次登录操作约 30 分钟；
- 超时会退出；
- 不点击保存等于没有保存；
- 最好重新登录检查；
- 不要在截止前最后几小时集中填报，以防网络拥堵；
- 手机号被用于官方短信联系；
- 当时有效手机号范围还有地域/运营商约束。[S13]

这说明即使到 old-Web scope 的后缘，仍存在大量：

### `browser-visible / server-persisted gap`

### `session-open / session-valid gap`

### `password-known / authorized-user gap`

### `saved / deadline-valid gap`

用户错误不一定表现成“网页打不开”。

更常见的失败可能是：页面看起来填完了，但服务器没有形成最终有效状态。

---

## 十二、核心状态缺口清单

本专题以后遇到任何历史 capture、截图、报道，都优先用下面的状态表解释，而不是一句“当时可以网上报志愿”带过。

| 状态 A | 不等于 | 状态 B |
|---|---|---|
| 招生后台联网 | ≠ | 考生家庭可网上填志愿 |
| Web 页面存在 | ≠ | 普通考生可访问 |
| 普通考生可访问 | ≠ | 家庭拥有私人 Internet |
| 专业目录在线 | ≠ | 考生理解专业 |
| 学校/专业代码存在 | ≠ | 当年对该考生可报 |
| 志愿草表填写 | ≠ | 正式志愿 |
| 表单输入完成 | ≠ | 已保存 |
| 已保存 | ≠ | 已提交 |
| 已提交 | ≠ | 已最终确认 |
| 已最终确认 | ≠ | 已签字/已生效 |
| SMS 提示成功 | ≠ | 后续所有线下状态完成 |
| 志愿已生效 | ≠ | 已投档 |
| 已投档 | ≠ | 高校已录取 |
| 高校预录 | ≠ | 省级审核完成 |
| 显示“录取” | ≠ | 考生最后实际入学 |
| 网络咨询问题已发 | ≠ | 招办已回答 |
| 招办已回答 | ≠ | 用户理解并采纳 |
| historical locator known | ≠ | historical capture verified |
| old text visible on current gov site | ≠ | original 2005 page preserved |

---

## 十三、页面形态与 archive preservation：最容易保存的往往不是最关键状态

### 1. 当前政府站上的旧内容不是“原始 2005 HTML”

广东 2005、2006 的一些志愿通知今天仍可在政府站访问。

它们可以作为**官方历史文本内容**使用，但今天的页面：

- 使用现代政府 CMS；
- 可能重新排版；
- 可能迁移 URL；
- 可能统一成现代 UTF-8/响应式模板；
- 不保留当年脚本、header、cookie、表单行为。

所以必须区分：

### `historical-content / historical-page-artifact gap`

今天能看到 2005 文本，不能据此推断 2005 用户看到的 DOM/CSS/charset/browser experience。

### 2. 静态说明页最容易活，实时志愿状态最容易死

容易保存：

- 填报通知；
- 招生章程；
- 志愿指南；
- 新闻报道；
- 系统入口 URL；
- 操作步骤。

容易消失：

- 登录页具体版本；
- session；
- 动态学校/专业下拉；
- 用户草稿；
- 保存失败；
- 逻辑校验接口；
- 最终确认状态；
- SMS callback；
- 投档后台；
- 用户个人录取状态。

因此：

### `policy-page survival / transaction-state disappearance`

未来只读 archive 静态页，会系统性高估“制度设计”，低估普通人真正执行时的失败和恢复路径。

---

## 十四、浏览器、编码与技术假设：本轮仍不能补全

根据仓库 `docs/METHOD.md`，没有实际 historical replay/WARC 就不能把现代网页体验写成历史浏览体验。

本轮仍然不知道或未验证：

### 2003 北京查询系统

- HTTP headers；
- charset；
- IE/Netscape compatibility；
- 购票脚本；
- telco billing callback；
- session/cookie；
- proxy/cache behaviour。

### 2004–2005 全国咨询平台

- BBS 原始软件/版本；
- 登录状态；
- moderation queue；
- 页面编码；
- 问答动态 endpoint；
- 并发拥堵时的错误页。

### 2005–2009 省级志愿系统

- 具体 HTML/frames/table 结构；
- JS validation 与 server validation 分工；
- IE-only / ActiveX 与否；
- 机构证书中间件；
- cookie/session timeout 实现；
- “提交/确认提交”具体 HTTP request；
- SMS gateway 与志愿数据库的同步；
- 学校端下载/上传协议。

### 2015 湖北

- `tbzy.hubzs.com.cn` 当年页面 DOM；
- Content-Type/charset；
- session timeout 的服务端实现；
- whether historical browser sniffing existed；
- archive 是否保存动态表单资源。

任何复原都必须保持 `unknown`，直到取得可检查的历史 artifact。

---

## 十五、历史 locator 清单（candidate locators，不等于 verified captures）

| 年份 | 角色 | locator | 证据 |
|---|---|---|---|
| 2003 | 北京录取资料查询 | `www.bbn.com.cn` | 同期报道 [S4] |
| 2003 | 北京教育考试院 | `www.bjeea.edu.cn` | 同期报道 [S4] |
| 2004 | 全国网上咨询 | `www.chsi.com.cn` | 教育部公告 [S5] |
| 2004 | 全国网上咨询 | `www.cernet.cn` | 教育部公告 [S5] |
| 2004 | 咨询周 BBS | `www.gaokao.edu.cn` | 教育部公告 [S5] |
| 2005 | 阳光高考 | `gaokao.chsi.com.cn` | 教育部公告 [S6] |
| 2006 | 北京考试院 | `www.bjeea.cn` | 同期报道 [S8] |
| 2006 | 北京高考 Web | `gk.bbn.com.cn` | 同期报道 [S8] |
| 2015 | 湖北志愿系统 | `tbzy.hubzs.com.cn` | 政府存档 [S13] |

对于广东 2005，官方通知虽然说明了系统和分层工作站，但本轮没有足够证据把某一个今天已知 host 无条件回填到所有地区/所有填报阶段，因此不强行补 locator。

---

## 十六、在线/线下身份：谁在操作网页，不一定就是谁在决定未来

高考志愿特别容易让研究者把“account holder”当成唯一行动者。

实际可能是：

```text
考生本人决定 + 考生本人操作
考生本人决定 + 父母代操作
家庭共同决定 + 学校工作站老师协助操作
老师/家长强烈建议 + 考生最后确认
考生填写 + 学校打印 + 本人签字
```

所以：

### `account-operator / preference-owner gap`

以及：

### `candidate-identity / decision-authority gap`

历史截图只能告诉我们哪个账号在执行事务，除非另有证据，不能自动告诉我们谁真正拥有决定权。

---

## 十七、安全与隐私边界

高考志愿包含高价值个人数据：

- 姓名；
- 考生号；
- 身份证信息；
- 密码；
- 手机号；
- 成绩；
- 位次；
- 学校与专业意愿；
- 录取状态。

本仓以后即使找到历史：

- 登录页截图；
- 论坛求助；
- cache；
- 用户志愿表；

也应优先保存 schema、URL pattern、字段和状态模型，不重新传播普通人的完整考生号、身份证号、密码、手机号或可识别志愿记录。

2005 广东初始密码规则可以作为公开制度事实记录，但不应用于推演现实攻击，也不能假定后来系统仍沿用。

---

## 十八、对 old-Web 主线有什么贡献？

### 1. 中文旧网不仅是“发内容”，也开始承载不可随意撤回的制度事务

个人主页/论坛/博客主要研究内容发布与身份表达。

高考志愿则提醒我们，2000s Web 同时在成为：

> **一次点击会改变制度状态的 transaction surface。**

`提交`、`确认提交`、`保存`、`签字` 是历史动作，不只是 UI 文案。

### 2. 旧网的历史价值不只在视觉页面

对志愿系统，最关键的不是“按钮长什么样”，而是：

- 哪个按钮改变什么状态；
- 可以撤回到什么时候；
- 哪个状态由纸张补全；
- 哪个状态由学校/报名点接管；
- 哪个状态进入招生后台。

### 3. 公共终端是被 household-ownership statistics 忽略的 Web 历史

2005 广东明确要求没有上网条件的考生获得学校/县级机构的填报环境；2015 湖北仍强调中学组织和统一填报地点。[S7][S13]

因此旧网考古不能只问：

> “这个家庭有没有电脑？”

还要问：

> “这个人能否通过学校、网吧、单位、公共终端实际完成 Web 事务？”

### 4. “网址还在”不等于“那个系统还在”

阳光高考品牌延续多年，但不同年份的：

- 页面；
- BBS；
- CMS；
- API；
- 账号；
- 咨询时间；
- 高校后台；

不能默认相同。

同品牌、同 host 甚至同路径的不同年份，仍须按 capture 区分。

---

## 十九、M1 状态

### **NOT ACHIEVED IN THIS SLICE**

本轮取得的是：

- 官方历史通知；
- 当前政府 CMS 中保存的旧制度文本；
- 同期报刊/教育网站操作材料；
- 多个历史 locator；
- 可复核的事务状态描述。

但本轮**没有实际取得并检查**满足仓库 `docs/METHOD.md` 最低合同的 2003—2015 历史 Wayback/WARC replay。

因此本轮没有：

- verified `capture_url` + `capture_datetime`；
- historical HTTP response；
- historical Content-Type/charset；
- 原始 DOM/CSS/JS；
- 子资源缺失清单；
- 旧浏览器回放；
- historical session/error page。

所以不能写：

> “Wayback 没有保存。”

只能写：

> **“本轮尚未验证到满足 METHOD 合同的 historical capture。”**

这条边界继续保持。

---

## 二十、下一步优先级

1. 对 `www.bbn.com.cn` / `www.bjeea.edu.cn` 的 2003 查询系统寻找实际可打开 historical capture；
2. 对 `www.gaokao.edu.cn` 2004 咨询周 BBS 寻找两个历史时点，并检查 charset/论坛软件/登录与问答状态；
3. 对 `gaokao.chsi.com.cn` 2005 初期页面区分 today-preserved content 与 historical HTML；
4. 找广东 2005/2006 省级正式志愿系统的实际 host、证书/浏览器要求和工作站文档；
5. 找 2007 北京相关历史页面，但只做状态/恢复机制考古，不复原攻击；
6. 对陕西 2009 “提交→确认提交→签字→上报”尝试找到原始系统页面或操作截图；
7. 对 `tbzy.hubzs.com.cn` 2015 capture 检查 login/session/timeout/charset/browser 条件；
8. 主动寻找考生论坛/博客里的失败操作证据：没保存、密码丢失、网络拥堵、截止前掉线、学校打印发现错误；
9. 对所有普通考生资料执行隐私最小化，不批量重发可识别志愿与身份数据。

---

## Sources

- [S1] 教育部办公厅，教学厅〔2001〕1号，《关于做好2001年全国普通高等学校招生网上录取工作的通知》：https://www.moe.gov.cn/jyb_xxgk/gk_gbgg/moe_0/moe_7/moe_12/tnull_5936.html — A，官方历史文件内容。
- [S2] 教育部，2002，《关于做好2002年普通高等学校招生工作的通知》：https://www.moe.gov.cn/jyb_xxgk/gk_gbgg/moe_0/moe_8/moe_22/tnull_179.html — A。
- [S3] CERNet，2003-04-03，《网上录取——尽显招生改革成效》：https://www.cernet.edu.cn/edu/yuan_cheng/yuan_cheng_jiao_yu/200603/t20060323_71542.shtml — B，接近部署时期的技术回顾。
- [S4] 教育在线，2003-06-18，《北京：高考查分三种方式 花十元钱自查排名》：https://gaokao.eol.cn/news/200603/t20060323_76739.shtml — B，同期操作报道。
- [S5] 教育部，2004，《教育部将举办“2004年普通高校招生网上咨询周”活动》：https://www.moe.gov.cn/moe_879/moe_329/moe_297/tnull_3003.html — A，官方历史公告内容；不等于历史 BBS capture。
- [S6] 教育部，2005-04-18，《教育部将开通“阳光高考”信息平台，咨询周6月10日开幕》：https://www.moe.gov.cn/jyb_xwfb/gzdt_gzdt/moe_1485/tnull_7019.html — A，官方历史公告内容。
- [S7] 广州市招考办保存的广东省 2005 年普通高考网上志愿官方通知，2005-05-09：https://gzzk.gz.gov.cn/gkck/gkckxx/wjtz/content/post_5082257.html — A，官方制度文本；当前 CMS 页面不视为 2005 原始 HTML artifact。
- [S8] 北京 2006 年 Web/声讯电话志愿操作同期报道：https://news.sina.com.cn/c/2006-05-09/15158878272s.shtml；广东同年网上填报报道可作并行参考：https://news.sina.com.cn/c/edu/2006-05-15/10008928803s.shtml — B，同期媒体操作材料。
- [S9] 北京晚报/新浪，2007-05-13，高考网上志愿安全事件与线下签字确认报道：https://news.sina.com.cn/c/2007-05-13/130611809412s.shtml — B，只用于证明当时的确认 fallback，不复原攻击。
- [S10] 湖北省教育考试院，2008 年普通高校招生/志愿说明存档：https://www.hbea.edu.cn/html/2009-03/560.shtml — A，省级考试机构材料。
- [S11] 2009 年陕西省高考网上填报志愿说明（同期高校招生网转载）：https://www.peihua.edu.cn/zhaosheng/info/1028/1796.htm；陕西招生考试信息网三本/高职通告：https://www.sneac.com/info/1019/12408.htm — A/B。
- [S12] 中国青年报，2009-06-09，《86.7％的人赞同中学普及高考志愿指导中心》：https://zqb.cyol.com/content/2009-06/09/content_2701211.htm — B，同期用户/家庭与专业理解证据。
- [S13] 湖北省 2015 年普通高校招生网上填报志愿必读，潜江市政府存档：https://www.hbqj.gov.cn/xxgk/xxgkml/szfxxgkml/qtzdgknr/gxxx/201507/t20150727_2124208.html — A/B，政府存档的省招办操作说明。

> 本文件目前是 **research companion / state-gap map**，不是 M1 完整 archaeology case。所有 historical locator 都保持 candidate 状态，直到实际检查 archive artifact。