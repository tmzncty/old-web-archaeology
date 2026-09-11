# 兵役登记、网上应征、学籍校验、筛选与批准入伍的状态差（2010–2015）

> Scope：本 note 只研究约 2010–2015 中文互联网中的大学生网上预征、全国征兵网与相关 Web 流程。它不是中国征兵史，也不讨论军队作战、装备或宏观军事政策。1985–2009 的基层兵役登记与纸面流程只作为理解 Web 接口的前史边界；2016 以后只在必要时用于说明后续状态，不扩展成本仓主体。

Cross-repo：生活史解释见 `tmzncty/how-people-lived`：  
`topics/from-local-military-registration-to-online-enlistment-institutionalized-interruption-and-life-course-reentry-china-1985-2026.zh-CN.md`

## 0. 本轮为什么值得单独建 note

本仓已有公务员网报、学历查询、毕业派遣、医院挂号、网银、12306 等状态机专题，但此前没有征兵 Web。

征兵平台对旧网考古很有价值，因为它把几个不同制度对象压进一个界面：

```text
兵役登记
大学生预征
学籍 / 高考数据校验
应征报名
初选
打印纸表
线下初检 / 体检 / 政治考核
批准入伍
学费补偿 / 贷款代偿
```

如果未来只剩一张“报名成功”截图，最容易发生的错误就是把它写成“此人当兵了”。

因此本 note 的核心不是复原视觉，而是固定：

> **public Web state != administrative state != physical screening state != actual service state**

---

## 1. 前史边界：Web 以前，兵役登记已经是分布式基层事务

1985 年发布、2001 年修订的《征兵工作条例》规定，县市兵役机关组织基层单位办理兵役登记；机关、团体、企事业单位、乡镇政府与街道办事处负责本单位/地区的适龄男性登记、填写兵役登记表并上报。本人特殊情况下不能到场时，还可书面委托亲属或所在单位办理。

来源：

- **A / official legal text, official republication**：国防部，《征兵工作条例》。  
  https://www.mod.gov.cn/gfbw/fgwx/flfg/16216170.html
- **A / official historical-text republication**：全国征兵网文本经中国雄安留存。  
  https://www.xiongan.gov.cn/2017-12/19/c_129770192.htm

这个前史只用于界定 Web 改变了什么：

- Web **没有发明兵役登记**；
- Web **没有发明基层审核**；
- Web 新增的是全国统一的信息入口、本人可直接填写的数据对象，以及教育记录与征集系统之间更自动化的比对。

不要把此段扩成 1980s–1990s 网站史。

---

## 2. 研究单位必须拆开

至少区分以下对象：

1. **physical person**：现实青年；
2. **legal military-service-registration subject**：依法需要兵役登记的主体；
3. **military-service registration record**：兵役登记记录；
4. **enlistment intention**：本人表达的应征意愿；
5. **Web account**：用于登录报名系统的网络账号；
6. **education identity**：学籍 / 学历 / 高考相关记录；
7. **pre-enlistment application**：大学生预征报名记录；
8. **general enlistment application**：应征报名记录；
9. **online preliminary-review state**：系统预审 / 初选状态；
10. **printed form artifact**：下载打印的登记表、审核表、学费补偿/贷款代偿申请表；
11. **local confirmation**：乡镇、街道、学校等线下确认；
12. **preliminary inspection**：初审初检；
13. **physical examination state**：体检状态；
14. **political / statutory assessment state**：政治考核等法定审核状态；
15. **selection / pre-assignment state**：预定 / 定兵前状态；
16. **formal approval of enlistment**：批准入伍；
17. **actual reporting / service**：现实报到并服役；
18. **school-status preservation**：保留学籍/入学资格；
19. **tuition / loan benefit record**：学费补偿、助学贷款代偿状态；
20. **archive capture**：档案保存的页面或资源。

永久保持：

```text
person != account
account != military-service registration record
registration record != enlistment application
enlistment application != preliminary selection
preliminary selection != physical examination passed
physical examination passed != final approval
final approval != actual reporting
actual reporting != later completion of service
education record matched != person fully eligible
form printed != form accepted
benefit form submitted != benefit paid
archive capture != backend administrative record
```

---

## 3. 2010：大学生预征开始全国网上报名

教育部 2013 年官方政策问答明确回顾：自 **2010 年**起，全面实施大学生入伍网上报名预征，应（往）届毕业生与在校生登录“大学生应征入伍网上报名平台”，填写、打印《登记表》和《申请表》。官方同时把优势解释为：个人可自行报名打印、可在学校完成部分初审、可进行学籍信息比对、可收到政策和应征提醒。

来源：

- **A/B / official retrospective with specific operational claim**：教育部，2013。  
  https://www.moe.gov.cn/jyb_xwfb/xw_zt/moe_357/s7093/s7407/201309/t20130903_156772.html

### 可支持的最小 claim

- `exists`：2010 起大学生网上预征制度被全面实施；
- `available`：符合该政策对象的大学生可使用网上报名平台；
- `integration`：平台与教育记录比对发生制度性连接。

### 不能支持

- 不能从该官方回顾重建 2010 首页 DOM；
- 不能确定 2010 首版 charset、浏览器要求、JS 技术栈；
- 不能确定 2010 所有报名者都完全自行操作；
- 不能把“网上报名成功”写成“入伍成功”。

---

## 4. 2011：取得 exact historical original URL

教育部 2011 年 4 月 10 日同时代公告保存了当年大学生网上预征的两个明确入口：

```text
http://zbbm.chsi.cn
http://zbbm.chsi.com.cn
```

并记录当年网上报名期为 4 月 12 日至 7 月 12 日。

来源：

- **A / contemporaneous official announcement**：教育部，2011-04-10。  
  https://www.moe.gov.cn/jyb_xwfb/gzdt_gzdt/s5987/201104/t20110410_128422.html

这是本轮 old-Web 最重要的 provenance 增量，因为它把“大学生网上预征平台”从品牌名推进到了 **可供档案检索的 exact original URL**。

但 exact URL 仍然不是 historical capture。

### M1 状态

本轮检索了：

- `zbbm.chsi.cn`
- `zbbm.chsi.com.cn`
- 2010–2013 时间窗的 archive locator / 搜索线索

当前没有取得一份已经实际打开并可同时核验以下字段的历史 capture：

- `archive_source`
- `capture_url`
- `original_url`
- `capture_datetime`
- replay / HTTP state
- charset / Content-Type
- DOM / form structure
- form action / endpoint
- scripts / iframe / image subresources
- second historical time point

因此：

**M1 verified historical `zbbm.chsi.*` application capture: NOT ACHIEVED IN THIS SLICE.**

这不等于“Wayback 当时没有保存”。

---

## 5. 2014：全国征兵网把“兵役登记”和“应征报名”做成相邻但不同事务

2014 年湖南省征兵办同期政策答问明确称，当年全面实行网上征兵，青年登录“全国征兵网”：

```text
http://www.gfbzb.gov.cn
```

男性流程被明确拆成：

1. 注册账号；
2. 兵役登记；
3. 应征报名；
4. 打印表格；
5. 到乡镇 / 街道武装部现场确认；
6. 后续体检、政治考核、审批定兵。

来源：

- **A/B / contemporaneous local official interview**：湖南省征兵办 2014 年答记者问。  
  https://www.hnrd.gov.cn/content/2014/07/21/7263842.html
- **A / contemporaneous local government notice**：内乡县 2014 年征兵公告。  
  https://www.neixiang.gov.cn/gsgg/2015-03-17/8568.html

因此本仓必须永久保留：

```text
military-service registration
!= enlistment application
```

这与美国 Selective Service 当前官网反复强调的 “registration is not the same as enlisting” 在概念上类似，但这里不要把两国制度视为同一法律结构。

### “全部网上报名”也不等于人人自己上网

2014 年湖南材料明确说，不能或不方便网上报名的青年，可到乡镇、街道武装部或县区人武部门，由工作人员协助报名。

因此：

```text
administrative record must enter Web system
!= applicant independently operates Web system
```

这是 **assisted digital compliance**，以后不能看到数据库记录就默认键盘操作者是应征者本人。

---

## 6. 2014 女兵流程：平台不只是收表，还在做自动数据筛选

全国征兵网 2014-03-17 的官方“女兵入伍流程”至今仍可由当前站点访问。页面明确区分：

```text
网上报名
→ 系统审核
→ 打印审核表
→ 初审初检
→ 体检政审 / 综合素质考评
→ 批准入伍
```

它还说明：完成报名后，系统会对学籍与高考原始总分进行自动审核，并按报名人所在省份的高考相对分数进行初选；系统审核通过后以短信通知。

来源：

- **A / original official dated content preserved on current official site**：全国征兵网，2014-03-17。  
  https://www.gfbzb.gov.cn/zbbm/nvbzj/201403/20140317/824652247.html

### 证据边界

这个页面可以证明 **2014 年该官方流程这样规定**，但它不是 2014 年 archive capture。

当前浏览器看到的：

- HTML wrapper；
- CSS；
- 页面导航；
- TLS；
- 字体；
- 当前域名响应行为；

都不能自动当作 2014 浏览环境证据。

同样，女兵的相对分数筛选也不能泛化到：

- 所有男兵；
- 所有年代；
- 所有征集类别。

---

## 7. 2014–2015 的页面状态机建议

### 7.1 注册 / 登录层

```text
anonymous visitor
→ account registration
→ identity-linked account
→ login session
```

需要以后确认：

- 是否直接复用学信网账号；
- 2014 不同入口是否发生 SSO / redirect；
- cookies 与 session 生命周期；
- 密码找回流程；
- 是否存在手机验证。

当前证据不足，不推断。

### 7.2 兵役登记层

```text
not registered
→ registration draft
→ submitted
→ local confirmation pending
→ registration state recognized
```

注意：公开报道中的“完成兵役登记”可能指 Web 提交完成，也可能指基层确认后的行政状态，必须看原文上下文。

### 7.3 应征报名层

```text
has military-service registration
→ enlistment application draft
→ submitted
→ education / identity checks
→ preliminary state
```

### 7.4 线下审批层

```text
online preliminary state
→ local preliminary inspection
→ physical exam
→ political / statutory assessment
→ selection
→ formal approval
→ reporting for service
```

这一层最容易在 Web archive 中消失，因为很多状态只对本人和行政后台可见。

---

## 8. 页面可见信息与后台不可见状态

### public / relatively archivable

可能包括：

- 报名入口；
- 政策说明；
- 时间窗口；
- 流程图；
- FAQ；
- 公开体检标准；
- 下载表格说明；
- 咨询 / 举报入口；
- 部分帮助页。

### private / ephemeral / ethically non-republishable

可能包括：

- 身份证号；
- 户籍 / 家庭资料；
- 学籍精确记录；
- 高考分数；
- 联系电话；
- 体检结果；
- 政治考核材料；
- 报名动机；
- 具体定兵状态；
- 后续服役结果。

这会产生本专题最重要的 archive asymmetry：

> **policy-shell survival / applicant-state loss asymmetry**

二十年后，我们很可能知道“2014 年网页要求用户做什么”，却无法知道某个普通用户当年到底走到了哪一步。

这不是 archive 不够努力，而是隐私与后台事务设计共同决定的。

---

## 9. 新增 archive 偏差

### 9.1 registration-shell survival / approval-state loss

网页可能保存“兵役登记/应征报名”按钮，却不保存后续批准结果。

因此：

`button exists != user submitted != application approved`。

### 9.2 education-verification result loss

平台可公开宣称会核验学籍 / 高考信息，但个人匹配结果不可公开。

因此：

`verification feature exists != this applicant passed verification`。

### 9.3 printed-form artifact ambiguity

一张保存下来的《登记表》或打印页面可能证明系统曾生成过文书，但：

`form generated != form submitted != form accepted != enlistment approved`。

### 9.4 SMS-notification invisibility

2014 女兵流程明确有短信通知，但短信通常不会进入 Web archive。

页面历史因此天然缺失一条关键跨渠道状态：

```text
Web backend decision
→ SMS notification
→ person sees notification
```

### 9.5 assisted-entry operator ambiguity

当基层工作人员替不便上网的青年录入时：

`account owner != keyboard operator`。

这种代理操作几乎不会在公开 HTML 里留下痕迹。

### 9.6 current-page / historical-DOM confusion

全国征兵网今天仍保存 2014 日期的官方内容，只能证明**原始官方内容的文本 provenance**；不能把当前 CMS wrapper 误当作 2014 页面原貌。

---

## 10. 浏览器、编码与技术栈：当前全部保守处理

目前没有合格 historical capture 支持以下精确结论：

- `GB2312 / GBK / UTF-8` 的具体历史页面编码；
- IE-only；
- ActiveX；
- Flash；
- frameset；
- jQuery 版本；
- ASP / JSP / PHP 服务端实现；
- 历史 TLS 行为；
- 2010–2011 表单 action；
- 验证码实现；
- SSO 细节。

即使同年代大量中国政府/教育网站使用其中某些技术，也不能据此补全本对象。

状态：**UNKNOWN until verified capture or contemporaneous technical documentation.**

---

## 11. 2015 以后仅作边界说明：系统不会止于网页提交

2018 年军队官方回顾称，2014 年全国征兵网开通后，征兵还进一步使用网络版体检信息化管理系统；2019 年报道继续强调体检过程的信息化记录与追溯。

来源：

- **B / official retrospective**：解放军报，2018-11-25。  
  https://www.mod.gov.cn/gfbw/qwfb/4830241.html
- **B / official retrospective**：2019 年大学生征兵十周年综述。  
  https://military.people.com.cn/n1/2019/0923/c1011-31367470.html

这里只用于提示一个研究方向：

> 后台状态会继续数字化，但本仓主对象仍是 1995–2015 中文 Web，不应无限扩成现代征兵 IT 系统史。

---

## 12. 海外比较：为什么“网上招募”不是中国旧网独有

美国陆军官方回顾称，1999 年 9 月开始通过 Internet 系统接触潜在招募对象，后来 cyber recruiters 在线回答资格与岗位问题；同时 USMEPCOM 的 MIRS 早在 1994 年已经开始用于申请者处理后台。

来源：

- **B / official institutional history**：USMEPCOM。  
  https://www.mepcom.army.mil/About-Us/History/
- **B / official retrospective**：U.S. Army, 2008。  
  https://www.army.mil/article/12798/cyber_recruiting_instant_expert

因此，中国 2010–2014 的变化不应写成“世界上首次把征兵搬上网”。更值得研究的是自己的组合方式：

- 学信网教育记录；
- 高校预征；
- 兵役登记；
- 全国征兵网；
- 乡镇/街道/高校工作站；
- 打印纸表与线下确认；
- 体检和后续审批。

这是一个 **Web + national education registry + local administrative network + physical screening** 的混合系统。

---

## 13. 与“普通人怎么活”的交叉解释

这套旧网状态机为什么属于生活史，而不仅是政务网站史？

因为一个页面上的状态可能改变的是：

```text
我下学期还在不在学校？
我是不是需要回户籍地？
我的学籍能不能保留？
助学贷款怎么处理？
两年后我还能不能回来？
毕业后我是去工作、继续读书还是进入另一套组织生活？
```

old-Web 里最容易幸存的是“报名入口”和“政策问答”，但真正决定生命路线的是那些后台状态以及它们与学校、家庭和现实身体的连接。

所以本对象提供了一个很强的总原则：

> **网页考古如果只恢复界面，会把“人生分叉”误恢复成“一个表单”。**

---

## 14. Evidence ledger

| Claim | Evidence | Grade | Confidence | Boundary |
|---|---|---|---|---|
| Web 前由基层单位组织兵役登记 | 1985/2001《征兵工作条例》官方文本 | A | high | 法律结构，不等于各地执行完全一致 |
| 2010 起全面实施大学生网上预征 | 教育部 2013 官方问答 | A/B | high | 官方回顾，不提供 2010 DOM |
| 2011 入口为 `zbbm.chsi.cn` / `zbbm.chsi.com.cn` | 教育部 2011 同时代公告 | A | high | exact URL，不等于 archive capture |
| 2014 全国征兵网全面网报 | 2014 地方征兵办 / 政府公告 | A/B | high | 仍保留线下确认与协助 |
| 兵役登记与应征报名是不同步骤 | 2014 同期官方流程 | A/B | high | 男兵流程语境 |
| 2014 女兵系统使用学籍/高考数据自动初选 | 全国征兵网 2014 官方页 | A | high | 不能泛化所有类别/年份 |
| 不便上网者可由基层协助网报 | 湖南 2014 征兵办答问 | A/B | high | 地方执行证据，未证明全国每地完全同样 |
| 2014 当前官方页不是 2014 DOM capture | METHOD + 页面 provenance 区分 | D/method | high | 研究方法判断 |
| M1 historical capture 已完成 | — | — | false | 本轮未达到 |

---

## 15. 下一步取证清单

### P0：真正拿到 M1 capture

优先目标：

```text
http://zbbm.chsi.cn/
http://zbbm.chsi.com.cn/
```

时间窗：2010–2013。

拿到后必须记录：

- original URL；
- capture URL；
- capture datetime；
- redirect chain；
- HTTP / replay state；
- Content-Type / charset；
- title；
- form fields；
- form action；
- images / CSS / JS / iframe 保存状态；
- archive rewrite；
- browser assumption。

### P1：全国征兵网 2014 双时点

目标：`http://www.gfbzb.gov.cn/` 2014 至少两个不同时间点，验证：

- 首页结构；
- 兵役登记 / 应征报名入口；
- 登录跳转；
- 学信网账号关系；
- 男女兵入口差异；
- 帮助 / FAQ；
- 子资源完整度。

### P2：用户操作材料

寻找 2010–2015 同时代：

- 高校“网上预征报名操作指南”；
- 浏览器兼容性提示；
- 截图教程；
- 学生论坛故障讨论；
- “报名成功但无法打印 / 学籍校验异常 / 登录失败”等具体事务材料。

这些材料特别适合补 official page 不会写出的 failure modes。

### P3：隐私边界

即使 archive 中意外保存了个人报名页，也不要重新公开：

- 身份证号；
- 家庭信息；
- 学籍详情；
- 高考成绩；
- 医疗 / 体检；
- 政治考核；
- 电话、地址。

优先记录 schema、字段名、状态转换，不复制普通人的敏感数据。

---

## 16. 本轮结论

当前证据已经足以确认 2010–2014 的制度与 URL 谱系：

```text
基层 / 学校组织的纸面登记与预征
→ 2010 大学生网上预征全面实施
→ 2011 可定位 zbbm.chsi.cn / zbbm.chsi.com.cn
→ 2014 全国征兵网统一入口
→ 兵役登记 + 应征报名 + 教育记录校验 + 纸表 + 线下审核并行
```

但还不足以完成一个可复核的历史页面 case：

**M1 verified historical Chinese enlistment application capture: NOT ACHIEVED IN THIS SLICE.**

这个负结果本身值得保留，因为它阻止我们用今天的全国征兵网页面外观、当前 CMS 或对 2010s 政务网站的印象，去伪造当年的浏览体验。
