# 自学考试网上报名：银行插件、混合身份校验与长期考籍状态——2004–2008

> scope: 中文旧网约 1995–2015；本 note 只研究自考服务怎样进入 Web，以及历史页面能够/不能证明什么。  
> cross-repo: `tmzncty/how-people-lived/sources/self-study-exams-second-chance-higher-education-and-credential-time-china-1981-2025.zh-CN.md`  
> status: research note；尚未达到 M1 historical Web case 门槛。

## 0. 去重与研究问题

仓库已有公务员在线报名、校园一卡通、声讯查分等 state-gap 专题。本轮不再泛泛重复“页面存在不等于事务完成”。

自学考试给出三个新的、可单独考古的问题：

1. **长期状态**：一个考生可能跨几年累积单科成绩，中断后再回来；Web 不只是一次报名界面，而是长期考籍的观察窗口。
2. **客户端依赖**：所谓“网上报名”可能硬依赖 Windows / IE / 银行安全插件 / 特定银行卡。
3. **混合身份完成**：网上注册后，新生仍可能必须在线下摄像、出示身份证，才能真正生成可考试的身份。

核心不等式：

```text
online registration page exists
!= any browser can use it
!= payment can complete
!= candidate identity is complete
!= candidate can sit the exam
!= past course credits are preserved
!= graduation eligibility is satisfied
```

## 1. 可确认的同时代事务变化

### 1.1 2004 杭州：电话、Web、银行系统叠在同一报名路径中

《杭州日报》2004-11-19 报道，2004 年 10 月自考成绩可通过声讯电话或浙江自考网查询；2005 年 1 月考试报名则同时提供电话与网上报名。

但网上报名不是只打开一个网页：报道专门提醒工商银行网银升级，并区分已经办理电话/网上报名手续、持灵通卡、只有存折等不同用户状态；部分用户需要先到银行重新注册，再通过工商银行站点完成自考报名。

来源：

- 《10月自考成绩明天公布》，搜狐保存的《杭州日报》稿，2004-11-19：<https://news.sohu.com/20041119/n223064993.shtml>（B）

这说明事务至少横跨：

```text
exam authority identity/state
+ telecom / Web access
+ bank account state
+ bank authentication state
+ payment confirmation
```

Web 页面只是其中一层。

### 1.2 2004/2005 北京：新生“只能网上报考”，却仍必须到线下摄像

《北京晚报》2004-11-25 报道，北京从 2005 年 4 月考试开始，课程报考采用网上、电话、邮储营业网点三种方式；新生注册和报考“只能网上办理”。但同一流程又规定新生在之后的固定日期到注册区县自考办摄像。

来源：

- 《2005年自考下月开始报名》，搜狐，2004-11-25：<https://news.sohu.com/20041125/n223178411.shtml>（B）

所以“online-only registration”并不等于“remote-only enrollment”。

更准确的历史事务是：

```text
online data entry
→ online/other-channel course registration
→ payment state
→ assigned candidate identifier
→ physical identity / photo capture
→ usable exam credential
```

### 1.3 2006 海南：Web + 银行 + 线下照片是明确的混合流程

海南 2006 年首次实行网上付考试费。报道要求考生先办理工商银行卡并开通网上支付，再进入海南省考试局自考报名系统；新生报名成功后三天内仍须到报名点照相，照片用于准考证和毕业证。

来源：

- 海南新闻网/新浪，《海南省自考报名3月1日开始 首次实行网上付费》，2006-03-01：<https://edu.sina.com.cn/exam/2006-03-01/103129555.html>（B）

因此新增一个 archaeology unit：

**`hybrid enrollment state / 混合报名状态`**。

历史用户可能已经完成网页中的“报名成功”，但制度上仍处于“照片未采集，因此不能形成完整考试身份”的中间态。

## 2. 2006 天津：浏览器环境本身就是制度接口

现存于自考365的 2006-11-28 天津报名通知，保存了非常罕见的客户端要求：

- Windows 2000 或以上；
- 浏览器至少 IE 6.0；
- 浏览器密钥长度 128 位；
- 必须安装工商银行安全插件；
- 必须持指定工商银行卡之一；
- 必须开通个人网上银行；
- 第一次支付前还要设置网银登录/支付密码。

同一“考生服务系统”又承载：

- 报名报考；
- 10 月考试成绩查询；
- 成绩复核网上申请；
- 跨省市成绩转移网上申请。

来源：

- 《天津市07年1月自学考试网上报名通知》，自考365现存旧内容页，2006-11-28：<https://www.zikao365.com/html/3_7/2006_11_28_wa13771652488211600214392_0.htm>（B；当前 live legacy representation，本轮未验证 2006 archive capture）

### 2.1 新机制：`client-stack eligibility / 客户端栈资格`

这类旧 Web 事务不能只记录 URL 和表单字段。

一个历史研究者还必须问：

```text
OS compatible?
browser compatible?
crypto strength sufficient?
ActiveX / bank control installed?
bank account eligible?
online banking activated?
payment password configured?
```

如果缺任何一项，“网页可访问”都可能和“事务可执行”完全不同。

因此新增：

**`interface availability != operational eligibility`**。

## 3. 2006 北京：表单状态与银行状态互相生成

2006 年的北京自考操作说明称，北京报名/报考已经完全采用网上办理；新生填写个人信息和专业课程后获得临时流水号，再进行课程选择和支付，之后取得正式准考证号。

来源：

- 四联自学网/新浪，《轻松搞定：北京自考网上报考流程、技巧全解》，2006-12-14：<https://edu.sina.com.cn/exam/2006-12-14/110064559.html>（B）

这说明候选人的标识并非静态单号，而可能经历：

```text
unregistered person
→ submitted profile
→ temporary transaction identifier
→ paid registration
→ formal candidate number
→ offline photo/identity completion
```

对 old-Web archaeology 来说，应把“账号”拆成：

- temporary registration ID；
- formal candidate ID / 准考证号；
- bank-side payment transaction；
- identity/photo completion state。

否则截图里看到一个“成功注册”页面，很容易被误写成“已经有考试资格”。

## 4. 2007 北京：Web 开始成为长期学籍记忆的观察窗

2007 年《北京考试报》报道，北京教育考试院网站可查：

- 往期成绩，最早到 2001 年 10 月；
- 最新到档信息；
- 毕业证书；
- 教材；
- 考试时间。

报道明确给出一种生活场景：有的考生一两年前甚至更早考过几门，后来中断，现在回来续考；先在网上确认旧成绩是否仍有效。跨省转考者则查看考籍档案是否到达北京，再携带证件去办理转入手续。

来源：

- 《北京市自考生遇到5类问题可在网上解决》，新浪保存《北京考试报》稿，2007-10-29：<https://edu.sina.com.cn/zikao/2007-10-29/1715105945.shtml>（B）

### 4.1 新机制：`historical state observability / 历史状态可观察性`

很多 Web archaeology 只问“当年首页是什么样”。

自考系统说明，更重要的页面可能是登录后才出现的：

- 一个人多年累积的成绩列表；
- 缺考/合格/转入状态；
- 到档时间；
- 是否满足毕业条件。

这些都是**用户特定、数据库驱动、带长期历史的状态**。

于是：

```text
public help page preserved
!= private candidate history preserved
```

并且：

```text
registration UI reconstructed
!= candidate's multi-year educational state reconstructed
```

这形成新的 archive gap：

**`longitudinal account-state loss / 纵向账号状态丢失`**。

## 5. 2007 北京：Web 事务已经存在“不可逆提交”

北京市教育考试院内容的 2007 报考说明（现通过新浪转载可见）记录：

- 首次参加者网上注册并录入个人信息；
- 选报专业、课程；
- 缴费成功后获取正式准考证号；
- 在截止日前可查询、修改和补报课程；
- 但课程付费成功后不能退报/退费；
- 截止日后只能查询报考信息。

来源：

- 《北京07年10月自考简章与考试计划安排三》，新浪，2007-07-27：<https://edu.sina.com.cn/zikao/2007-07-27/155295459.shtml>（B；署名来源为北京市教育考试院，本轮未取得原始官方 historical capture）

这提醒 archaeology 不应只保存静态表单，还应记录：

**`state transition reversibility / 状态转换可逆性`**。

一个“选课”按钮在缴费前后不是同一个制度意义；系统截止日前后也不是同一状态机。

## 6. 2007 济南：新生与老生甚至看见不同的 Web 能力

2007 年济南自考材料称，网上报名只允许已有准考证号的老考生，新、老考生都可以现场报名；同一时期毕业申请又可先网上申报，再持打印出来的受理单去现场领取材料并本人交验。

来源：

- 舜网-济南时报/新浪，《7月自考本周六起报名》，2007-05-24：<https://news.sina.com.cn/c/2007-05-24/031611880809s.shtml>（B）

所以：

```text
same service brand
+ same year
!= same interface capability for all user classes
```

至少应区分：

- new candidate；
- existing candidate；
- transfer candidate；
- graduation applicant。

## 7. 2008 江苏：Internet 从事务层进入教学层

2007 年底的江苏报道显示，考试院除网上报名外，还与华夏大地教育网建设“在线课堂”，计划提供 38 个专业、260 余门网上助学课程，以解决地域和课程分散导致的辅导困难。

来源：

- 《08年上半年自考报名今天开始》，新浪保存《扬子晚报》稿，2007-12-01：<https://news.sina.com.cn/o/2007-12-01/011213000032s.shtml>（B）

因此 archaeological object 至少要拆成：

1. information portal；
2. registration/payment system；
3. candidate account/history system；
4. learning-content platform。

同一个“自考网站”可能只是品牌上的一体，技术上完全是多套系统。

## 8. 为什么这不是公务员网上报名专题的重复

两者都出现了报名、缴费、身份和纸面考试，但自考有几个特别结构：

### 8.1 时间跨度不同

公务员报名通常围绕一次招录周期；自考账号可能保存数年、十年的课程状态。

### 8.2 学习状态可累积

用户不是简单的 `registered / not registered`，而可能有数十门课程分别处于：

`unattempted / registered / absent / failed / passed / transferred / exempted`

最终才组合成毕业资格。

### 8.3 中断后回来是正常路径

“多年后重新登录查旧成绩”不是异常恢复，而是制度允许的真实生命路线。

因此，**长期数据库状态本身就是历史对象。**

## 9. 保存故障一：`client-environment archive gap`

就算今天找到 2006 报名页 HTML，也未必能重放事务，因为：

- IE6-specific JS 可能丢失；
- ActiveX / 银行安全插件不可用；
- HTTPS/TLS/证书环境已变化；
- 银行支付 endpoint 已消失；
- 跨域跳转可能被 archive rewrite 破坏；
- 当年 128-bit crypto 检测逻辑在现代浏览器上无意义；
- 支付成功回跳参数可能从未进入 archive。

因此：

```text
HTML preserved
!= historical client stack preserved
!= transaction replayable
```

这类案例特别适合未来 M3 浏览环境实验。

## 10. 保存故障二：`financial-side state loss`

旧网页也许告诉我们“去工商银行支付”，但历史事务真正完成还需要：

- 用户银行卡状态；
- 网银开通状态；
- 安全插件；
- 银行授权结果；
- payment callback；
- 考试系统记账。

所以：

```text
exam site captured
!= bank-side payment state captured
!= exam authority received payment
```

这与普通 static-page archaeology 不同，属于跨机构事务证据链。

## 11. 保存故障三：`identity-material split`

2005–2007 的新生流程反复出现：

`网上注册 / 获得号码 → 到现场照相 / 验证身份证 → 才形成完整考试身份`

历史 Web capture 几乎不会保存：

- 当场拍摄的照片；
- 柜台审核；
- 身份证核验结果；
- 某人是否按期限出现；
- 最终准考证是否制作。

所以“网上注册成功”与“历史中真实存在一个可参加考试的人”必须分开。

## 12. 保存故障四：`longitudinal account-state loss`

最重要的缺失可能不是页面，而是数据库随时间累积的个人状态：

```text
2001 pass A
2002 pass B
2003 interruption
2005 transfer to another province
2007 return
2008 exemption approved
2009 graduation eligibility reached
```

一个页面模板即使完整保存，也无法恢复这些状态迁移。

这和近期仓库提出的 `population-state loss` 有亲缘关系，但这里更强调**同一账户跨多年、跨地区的纵向状态链**，不是同一时间点的大规模用户集合。

## 13. 当前可证实 / 高概率 / 不知道

### 已证实

- 2004 杭州存在电话与网上自考报名/查询并行，网银状态影响报名操作；
- 北京从 2005 年考试周期起大规模转向网上报名，新生仍需线下摄像；
- 海南 2006 年网上支付要求先开通工商银行相关能力，并保留线下照片采集；
- 天津 2006 年操作说明明确要求 Windows 2000+、IE6+、128-bit、工商银行安全插件和网银；
- 2007 北京能在线查询多年旧成绩、到档、毕业证书等；
- 2007 北京报名存在临时/正式号码、支付后不可退等状态；
- 2007 济南对新生、老生开放的网上能力不同；
- 2008 江苏已有在线助学课程体系建设。

### 高概率

- 多地报名系统存在 IE/ActiveX/银行插件式兼容问题；
- 考试院、银行与线下自考办之间存在多套后台状态同步；
- 大量真实候选人通过网吧、单位、亲友电脑等环境完成报考。

这些都需要更多同时代操作记录后再提升证据等级。

### 目前不知道

- 2004–2008 各系统原始 HTML/JS/CSS 是否还能取得；
- `zkwsbm.bjeea.cn` 等历史 host 的可验证 archive capture；
- 当年 form action、POST 字段、支付 callback 结构；
- IE6 检测脚本与工商银行安全插件具体版本；
- candidate database schema；
- course-state / exemption / transfer 的字段模型；
- payment success 与正式准考证号生成的精确事务边界；
- 照片采集后线上状态如何变化。

## 14. 建议的 artifact schema

未来若取得 historical capture，至少记录：

```yaml
service: self-study-exam
province: null
exam_cycle: null
user_class: new|existing|transfer|graduation
original_url: null
capture_url: null
capture_datetime: null
browser_requirement: null
os_requirement: null
crypto_requirement: null
plugin_requirement: null
bank_requirement: null
candidate_id_stage: temporary|formal|unknown
payment_required: null
payment_provider: null
offline_identity_step: null
photo_capture_required: null
course_state_visible: null
historical_results_range: null
transfer_state_visible: null
graduation_state_visible: null
reversible_before_deadline: null
reversible_after_payment: null
archive_grade: A|B|C|D
replay_verified: false
```

## 15. 后见之明风险

1. 不把“网上报名”翻译成今天意义的一站式远程服务。
2. 不把当前考试院站点的功能倒推到 2004–2008。
3. 不把现在能打开的新浪/搜狐/自考365旧内容页写成当年的原始页面 capture。
4. 不把新闻提到的 URL 自动当作已验证 archive locator。
5. 不用今天 Chrome 成功加载静态说明页，证明当年 IE6 + 银行插件事务可以重放。
6. 不把“网上查到成绩”写成成绩数据库已经被 archive 保存。

## 16. 与普通生活史的连接

这类旧网考古之所以重要，不只是因为 IE6 很旧。

自考是一条可以跨几年、跨工作、跨城市、跨中断继续走的教育路线。对这样的人而言，Web 服务保存的并非一次购物订单，而是：

**“我以前已经完成的人生，制度还记不记得。”**

一门多年前通过的课程若能被查回、转入、继续组合进毕业条件，它就在把过去重新接到未来；反过来，如果系统记录无法迁移、用户错过窗口、支付没完成、照片状态没闭合，同一条人生路线也会在很小的接口处被卡住。

因此本案例建议把 old Web 的研究对象从“页面长什么样”继续推进到：

> 页面背后哪些长期状态，曾经让一个人能够几年以后回来继续生活。

## 17. M1 状态

**M1 historical self-study-exam Web case: NOT ACHIEVED IN THIS SLICE.**

本轮取得的是：

- 多个 2004–2008 同时代操作说明和新闻；
- 明确历史 URL / host locator；
- 浏览器、OS、插件、银行和线下身份步骤的事务证据；
- 可用于未来 artifact 检查的 schema。

仍缺：

- 实际打开并核验的 2004–2008 archive capture；
- ≥2 个历史时点；
- historical HTTP/DOM/charset；
- JS / ActiveX / bank control；
- payment callback；
- authenticated candidate-state capture。

所以不能声称已经复原，也不能声称 Wayback 没有保存。
