# Driver-license Web appointment, exam, and credential state gaps, China 1996–2015

## Scope

本笔记研究约 1996–2015 中文 Web 中与机动车驾驶资格有关的网页与事务状态，重点不是写一部驾考制度史，而是回答：

> **当“车管所”开始出现于中文 Web 上以后，archive 能看到的页面，究竟离一个普通人真正拿到驾驶证还有多远？**

对象包括：

- 交管局/车管所官方网站；
- 驾驶证业务指南；
- 表格下载；
- 驾考报名、预录入；
- 网上考试预约；
- 预约审核和结果查询；
- 驾驶人信息查询；
- 网上补换证/约办；
- 网上选号等相邻车管事务；
- 2015 年开始出现的全国互联网交通安全综合服务管理平台。

不把本仓扩成全球驾驶史，也不把 2016 年以后移动 App 作为主要对象。2016 年以后的 `交管12123` 只在解释 1996–2015 中文旧网的迁移边界时出现。

对应生活史专题：

- `tmzncty/how-people-lived/topics/drivers-license-mobility-skill-and-life-course-optionality-china-1985-2026.zh-CN.md`

---

## 1. 最低证据合同

继续遵守仓库既有原则：

```text
platform / institution
≠ site
≠ page
≠ form
≠ submitted transaction
≠ accepted transaction
≠ exam capacity
≠ physical exam
≠ licence issuance
≠ later real-world driving
```

### 1.1 `official website exists ≠ online driving-license transaction exists`

交管部门有网站，可能只提供：

- 地址；
- 电话；
- 办事指南；
- 法规；
- 表格下载；
- 公告；
- 驾驶人/车辆信息查询。

不能因此说“可以网上考驾照”或“可以网上办驾驶证”。

### 1.2 `online appointment ≠ exam accepted`

至少需要区分：

```text
candidate sees appointment page
→ identity entered
→ eligibility data resolved
→ candidate sees available session
→ session selected
→ initial booking recorded
→ authority reviews eligibility
→ booking approved
→ candidate receives/queries confirmation
→ candidate appears physically
→ identity verified at exam site
→ exam actually starts
```

重庆 2010 年材料明确保存了“初预约成功之后还要审核，考试前两日再查是否通过”的状态，因此不能把预约按钮当作最终考试资格。

### 1.3 `exam digitized ≠ exam remote`

理论题可以计算机化；科目二、科目三可以使用传感器、摄像头、GPS 和自动评判；预约可以经 Web 完成。

但实际驾驶技能考试仍然要求：

- 身体到场；
- 考试车辆；
- 场地/道路；
- 考生本人；
- 身份确认；
- 可用考场时段。

### 1.4 `locator ≠ verified capture`

本轮定位到：

- `www.cqjg.gov.cn`
- `www.czcgs.gov.cn`
- `www.czcgs.gov.cn/default.php?mod=c&s=ss1571a90`
- `jtgl.beijing.gov.cn`

以及 2015 年全国平台试点背景。

但没有成功打开并验证一个满足 M1 条件的 2009–2014 驾考预约 transaction memento。

因此这些均只能作为 **historical locator**，不是 archive-confirmed DOM。

---

## 2. 前史边界：1996 的驾驶资格状态机已经很清楚，但还不是 Web workflow

1996 年《中华人民共和国机动车驾驶员考试办法》明确把驾驶考试拆成：

```text
科目一：法规与相关知识
→ 合格
→ 科目二：场地驾驶
→ 合格
→ 科目三：道路驾驶
→ 合格
```

考试必须在车辆管理所设定的考试场、道路或场所进行，并事先约定考试日期和时间。

Source:
- 《中华人民共和国机动车驾驶员考试办法》，公安部令第29号，1996：https://zh.wikisource.org/wiki/中华人民共和国机动车驾驶员考试办法

Evidence grade: **A，部门规章文本。**

同年《机动车驾驶证管理办法》规定驾驶证全国有效，并把身份证件号码、长期住址、准驾车型、初次领证日期、有效期、发证机关和档案编号等作为正式记录项目。

Source:
- 南昌市公安局保存文本：https://ncga.nc.gov.cn/ncgaj/xxgkzcwj/200804/Q24BICD9ZMCK03AM875HKJIA9DXFT5X7.shtml

Evidence grade: **A。**

对旧网考古的意义是：后来的 Web 页面不是凭空出现一套业务，而是在既有行政状态机前面增加数字前台。

因此不要写：

```text
before web = no appointment / no structured record
```

更准确的是：

```text
pre-Web appointment + paper/office record
→ Web information/query
→ Web pre-entry / appointment
→ Web transaction front end
→ later unified national service front end
```

---

## 3. 2008–2009：网站先成为“知道怎样办”的入口，数字后台开始管理考生

### 3.1 2009 烟台：网上答复先减少“为了问材料跑一趟”

2009 年暑期，烟台车管部门为学生驾考开绿色通道，同期报道明确说通过“网上答复”和电话热线向学生说明报名条件、材料和办理程序，使其尽量一次跑完现场手续。

Source:
- 齐鲁晚报/新浪，2009-07-07：https://news.sina.com.cn/c/2009-07-07/073315911123s.shtml

Evidence grade: **B，同时代操作报道。**

这不是网上报名完成，而是：

```text
website/phone information
→ candidate knows eligibility/materials
→ physical service hall
→ form / copies / photo / submission
```

所以应标为 **information-to-counter handoff**。

### 3.2 2009 西安：后台“报名系统升级”可以直接改变谁报得进去

2009 年陕西多地“申领驾照报名系统”升级后，对异地学驾照者设置比例限制。同期报道记录西安部分外地学员连续数月报不上名，驾校对外地学员额外收费。

Source:
- 三秦都市报/新浪，2009-12-20：https://news.sina.com.cn/c/2009-12-20/072016802168s.shtml

Evidence grade: **B，同时代调查报道。**

这是一个非常重要的 old-Web/数字行政反例：

> **数字化不只把旧流程变快；软件里的 eligibility / quota rule 可以成为新的制度门。**

这里无法从公开报道恢复具体软件 UI、数据库字段或 quota algorithm，但可以确认：

```text
system upgrade
→ applicant category recognized
→ quota applied
→ some applicants unable to enter normal registration flow
```

不要把“系统升级”自动写成“便民升级”。

---

## 4. 2009–2010 重庆：`www.cqjg.gov.cn` 从信息网变成事务前台

### 4.1 2008：host 已经用于驾驶/车辆状态查询

2008 年重庆公安交通管理信息网 `www.cqjg.gov.cn` 已提供到期报废车辆查询。

Source:
- 重庆商报/新浪，2008-01-19：https://news.sina.com.cn/c/2008-01-19/030113287080s.shtml

Evidence grade: **B，historical host + described function。**

这只能证明 host 在当时承载交通管理查询，不能证明 2010 年的驾考预约 endpoint 已经存在。

### 4.2 2009：网上车管所开放，出现预约驾驶考试等事务

2009 年 7 月，重庆报道明确称网上车管所地址为：

`www.cqjg.gov.cn`

并称可用于：

- 网上选号；
- 预约驾驶考试；
- 补领机动车牌证等。

Source:
- 重庆晚报/央视网，2009-07-01：https://news.cctv.com/china/20090701/100296.shtml

Evidence grade: **B。**

注意：同一篇还给出“网上车管所办公时间”。这提醒我们，所谓“online”在早期政务 Web 中也可能仍被后台人工值守时间约束；不能后见式假定 24×7 transaction backend。

### 4.3 2010：操作报道保存了一条完整的驾考预约漏斗

2010 年 12 月重庆科目三网上自主预约面向主城多区开放。报道留下：

- historical host：`www.cqjg.gov.cn`；
- 页面入口名称：“考试预约”；
- candidate 需阅读服务约定；
- 填写/核对身份证号、姓名、驾校名称、考试车型；
- 系统按驾校可用场次显示选择；
- 名额满后界面关闭；
- 网上成功只算“初预约”；
- 车管所仍审核资格；
- 考试前两天需要重新查询审核结果；
- 预约后缺席可按考试不合格处理；
- 需要留下可联系到本人的电话号码。

Source:
- 重庆晨报/新浪，2010-12-24：https://news.sina.com.cn/o/2010-12-24/190621702317.shtml

Evidence grade: **B，极强的同期 workflow 证据，但不是直接 capture。**

可建模为：

```text
GET booking page
→ accept service terms
→ enter identity
→ backend resolves driving school / exam type
→ retrieve available sessions
→ choose session
→ initial booking
→ backend/authority eligibility review
→ applicant re-queries status
→ approved / rejected
→ physical arrival
→ exam
```

这条链非常适合防止把“预约成功”误读成“已获考试资格”。

---

## 5. 2010：网页也在做 paper-to-Web bridge，而不是马上无纸化

重庆同年便民措施允许驾驶人从公安交通管理信息网下载机动车驾驶证申请表、身体条件证明等表格；与此同时，全市交巡警平台仍提供同样的纸表。

Source:
- 重庆商报/新浪，2010-07-20：https://news.sina.com.cn/c/2010-07-20/042117831236s.shtml

Evidence grade: **B。**

另一个更重要的 hybrid：当地 70 多家体检医院可以通过 Internet 直接向车辆管理所传送机动车驾驶人身体条件证明信息，使驾驶人不用再自己到车管所递交该证明。

因此至少要拆出：

```text
form downloadable by citizen
≠ form submitted online by citizen
≠ medical evidence transmitted institution-to-institution
```

这三类都可以被媒体统称“网上办理/网络便民”，但技术和生活意义完全不同。

---

## 6. 2011 常州：网上车管所已经出现多事务状态与明确 timeout

2011 年 4 月 29 日，常州公安“网上车管所”上线：

- host：`www.czcgs.gov.cn`；
- 驾驶人考试自助预约；
- 丢失损毁驾驶证补发约办；
- 车辆/驾驶证相关信息查询；
- “车管在线”实时对话；
- 牌照自编自选。

同期报道还给出一个操作说明 locator：

`http://www.czcgs.gov.cn/default.php?mod=c&s=ss1571a90`

Source:
- 现代快报/新浪，2011-04-29：https://news.sina.com.cn/c/2011-04-29/032922378237.shtml

Evidence grade: **B，historical host + exact path + workflow description。**

同一系统的网上选号功能明确存在：

- 最大同时在线量 500；
- 单次查询次数限制；
- 系统自动退出；
- 预选号成功后只保留 5 个工作日；
- 仍需到车管所正式确认并完成后续领牌。

虽然选号不是驾考本身，但它揭示了这类早期车管 Web 的重要共同属性：

### 6.1 Web state 有 timeout

```text
temporary reservation / preselection
→ finite holding window
→ physical completion required
→ timeout
→ resource returns to pool
```

因此 archive 看见“成功页面”也不能证明后来完成线下步骤。

### 6.2 concurrent-capacity 可能进入页面行为

报道明确提到 500 个同时在线上限。这说明当时政府 transaction Web 并不一定拥有今天默认的弹性容量。

未来若获得 capture，应重点检查：

- 高并发错误页；
- session timeout；
- repeated login；
- quota full 提示；
- 是否依赖特定浏览器/脚本。

---

## 7. 2011 济南：驾考开始变成“人、图像、专网、考试车”的复合数字系统

济南 2011 年同期材料把以下模块并列为驾驶人考试“智能化”：

- 学车网上报名；
- 预录入；
- 人像采集和比对；
- 适性检测；
- 考试网上预约；
- 远程监控；
- 科目二 VPN 专网考试管理；
- 科目三智能评判；
- 考试总量控制。

Source:
- 济南日报/新浪，2011-07-26：https://news.sina.com.cn/o/2011-07-26/052022876031.shtml

Evidence grade: **B。**

这说明不能把“驾考网站”孤立成一个 HTML 站点。真正的系统边界至少可能包括：

```text
public Internet frontend
→ applicant / school account
→ vehicle-management backend
→ identity/photo subsystem
→ exam scheduling DB
→ VPN/private exam network
→ exam vehicle sensors/cameras
→ scoring backend
→ licence record
```

Archive 通常只能抓到最左侧一两层。

---

## 8. 2011：线上预约仍然无法解决物理容量

长沙 2011 年有 28 万余名学员尚未完成全部科目，其中 1.9 万余人距离当时两年有效期不足半年。同期第一人称描述：科目一已通过，却因为练车人口过多，长时间没有获得足够练车机会。

Source:
- 长沙晚报/新浪，2011-12-16：https://news.sina.com.cn/o/2011-12-16/085323642808.shtml

四川同年也有约 49 万待考人员，主管部门把驾校超培训能力招生、考试容量作为积压背景，并提出进一步推行网上约考。

Source:
- 四川在线/凤凰网，2011-07-19：https://biz.ifeng.com/city/sc/news/sichuanxinwen/detail_2011_07/19/59853_0.shtml

所以必须固定：

```text
booking visibility
≠ available seat
≠ training capacity
≠ exam vehicle capacity
```

并把“网页上没有可选时段”视为一种重要 negative state，而不是空数据。

---

## 9. 2014：自主预约与电子考官把稀缺和评判一起数字化

### 9.1 兰州：从驾校集中代约到学员网上自主约

2014 年兰州驾考网上自主预约系统上线。此前 90 多家驾校需要工作人员定期集中到考场办理预约，且存在“插队加塞”争议；系统上线后，预约流程被转到网络平台。

Source:
- 兰州日报/中新网，2014-02-11：https://www.chinanews.com/sh/2014/02-11/5823685.shtml

Evidence grade: **B。**

这里的历史变化不是简单“排队消失”，而是：

```text
opaque intermediary queue
→ visible/digital scheduling queue
```

需要进一步核验系统是否：

- 按提交时间；
- 按驾校配额；
- 按学习进度；
- 有优先级；
- 有取消/爽约惩罚。

这些都不能从“自主预约”四个字推断。

### 9.2 广州：电子评分重写了考试可执行性

2014 年广州科目三电子评判上线头两天通过率低于 10%，约一半考生取消预约；随后短期恢复人工/电子可选，再进入全面电子化。

Sources:
- 广州日报/中新网，2014-04-02：https://www.chinanews.com.cn/sh/2014/04-02/6020540.shtml
- 南方日报/中新网，2014-04-04：https://www.chinanews.com/sh/2014/04-04/6030564.shtml

Evidence grade: **B。**

这要求 archive 研究区分两类“考试页面”：

1. **scheduling state**：你有没有被安排进某场考试；
2. **evaluation state**：到了考场以后，机器/考官怎样判断你的行为。

Web capture 可能保存前者的壳，几乎不会保存后者的完整实时传感器和评分状态。

---

## 10. 2015：地方旧网开始进入统一平台迁移期

2015 年公安部建设面向公众的互联网交通安全综合服务管理平台，通过网页、手机 APP、短信、语音等方式提供驾考预约、办牌办证、审验、违法查询等 10 大类 130 余项服务；当时已在陕西、福建、广东部分地市试点，并计划全国推广。

Source:
- 重庆晨报/搜狐，2015-07-24：https://news.sohu.com/20150724/n417410923.shtml

Evidence grade: **A/B：同期公安部门发布信息经媒体报道。**

这一节点对 old-Web archaeology 很重要，因为它制造 **service-migration ambiguity**：

```text
local website disappears / becomes shell
```

可能意味着：

- 服务真的停止；
- 服务迁到统一平台；
- 旧站只保留公告；
- 旧 URL redirect；
- 后端还在但入口变了。

所以不能把 2015 以后地方网上车管所页面消失直接写成“网上驾考取消”。

---

## 11. 推荐状态机

### 11.1 初次申领/考试

```text
information page
→ eligibility read
→ school/training registration
→ identity / residence data entered
→ health check
→ study/training state
→ subject eligibility
→ appointment page
→ available-slot query
→ booking request
→ initial success
→ authority review
→ confirmed appointment
→ physical check-in
→ identity verification
→ exam starts
→ score generated
→ pass/fail recorded
→ next subject unlocked
→ all subjects passed
→ licence record issued
→ physical licence produced/delivered
```

### 11.2 补换证/约办

```text
service page
→ applicant identified
→ licence record resolved
→ eligibility checked
→ request submitted
→ backend accepts
→ fee/payment if required
→ production
→ pickup/mail
→ old credential invalidated / new credential active
```

### 11.3 Web 自主预约

```text
page visible
→ login/identity accepted
→ training/exam prerequisites resolved
→ slot visible
→ slot selected
→ booking request stored
→ review/queue
→ confirmation
→ no-show / cancel / attend
```

---

## 12. 需要长期保留的 state gaps

### 12.1 information-to-transaction gap

页面告诉你“可预约”，不代表当前有事务 endpoint 可用。

### 12.2 appointment-to-approval gap

重庆 2010 年已经证明“初预约成功”与“审核通过”是两个状态。

### 12.3 slot-visibility gap

页面存在但所有场次已满，是一种非常重要的 negative state。

### 12.4 training-to-exam gap

完成报名或科目一，不代表获得足够练车资源，也不代表下一个科目有名额。

### 12.5 digital-to-physical gap

Web 可以调度科目三，但科目三仍依赖道路、车辆、考场和身体到场。

### 12.6 evaluation-mode gap

人工评判、电子评判、人工+电子过渡不能混为同一考试状态。

### 12.7 address/eligibility gap

身份证、居住地、异地申请类别可能改变后台是否允许进入报名流程。

### 12.8 licence-record / plastic-card gap

数据库已经写入合格或发证状态，不一定等于实体证已经领取。

### 12.9 local-site / national-platform migration gap

地方 URL 消失不等于服务消失。

---

## 13. Archive 保存偏差

### 13.1 public-service-shell / private-credential-state asymmetry

最容易留下：

- 办事指南；
- 新闻稿；
- “考试预约”按钮；
- 登录页；
- 申请表下载；
- 考试计划；
- FAQ；
- 联系电话。

最难留下：

- 身份证号；
- 照片/人像比对；
- 体检数据；
- 驾校培训记录；
- session cookie；
- POST；
- 实时考试名额；
- 审核失败原因；
- 考试车传感器数据；
- VPN 专网；
- 实际考试录像；
- 分数写回；
- 驾驶证后台记录。

所以 archive 天然会让历史看起来像：

```text
“大家都能打开一个办事网页”
```

而真实生活里更关键的可能是：

```text
“这个人当时到底约没约上、排了多久、有没有被审核拒绝、何时真正考完”
```

### 13.2 success-page survivorship bias

报道和政府网页更愿意解释“新系统开通”“预约更方便”，失败页、超时、满额、重复登录和现场被退回更难进入长期档案。

### 13.3 exam-result privacy bias

个人驾考进度本来就不应被公开 archive；缺乏真实个人 transaction 不代表系统没有运行。

### 13.4 browser/plugin invisibility

2009–2014 政务 Web 是否要求：

- IE；
- ActiveX；
- 特定脚本；
- 弹窗；
- 短信验证码；
- 客户端控件

必须依赖 capture/操作文档验证，不能凭同时期其他政务站类推。

---

## 14. M1 capture status

### 已定位 historical locator

| 年代 | locator | 同时代证据支持的功能 | 当前状态 |
|---|---|---|---|
| 2008–2015 | `www.cqjg.gov.cn` | 查询、网上车管所、驾考预约、表格等 | locator only |
| 2011 | `www.czcgs.gov.cn` | 网上车管所、驾考预约、补换证约办 | locator only |
| 2011 | `www.czcgs.gov.cn/default.php?mod=c&s=ss1571a90` | 选号操作说明 | exact path locator only |
| 2009–2010 | `jtgl.beijing.gov.cn` | 北京交管信息/网上选号等相邻事务 | live institutional descendant / locator |

### 本轮 Wayback 尝试

本轮针对 `www.cqjg.gov.cn` 与 `www.czcgs.gov.cn` 搜索历史 Wayback locator，并尝试直接打开时间化 memento URL；没有取得能够实际检查 response body、headers、DOM 和 subresources 的 verified capture。

因此结论必须写成：

> **本轮未验证成功。**

不能写成：

> “Wayback 没有保存这些网站。”

### 仍为 unknown

- historical charset；
- DOCTYPE / HTML version；
- frame/iframe 结构；
- login method；
- form action；
- GET/POST；
- cookie/session；
- captcha；
- 短信验证；
- 身份字段是否明文出现在 query string；
- available-slot API；
- booking confirmation page；
- review status endpoint；
- cancellation/no-show state；
- ActiveX/IE 依赖；
- 驾校后台与公网前台的协议边界；
- 考试 VPN/专网与公网是否共享任何可抓取 endpoint。

---

## 15. 下一轮高价值 capture 任务

### A. 重庆 2009–2011

目标：`www.cqjg.gov.cn`

优先寻找：

- “考试预约”页面；
- 服务约定；
- 身份录入页；
- 可选场次页；
- 审核查询页；
- 失败/名额已满状态。

至少保存：

```text
memento timestamp
original URL
final URL
status
headers
raw bytes
render screenshot
charset evidence
subresource list
```

### B. 常州 2011

目标：

- `www.czcgs.gov.cn`
- `www.czcgs.gov.cn/default.php?mod=c&s=ss1571a90`

重点核验：

- PHP query 参数是否真来自历史页面；
- 页面编码；
- 自助预约与选号是否共享账号/session；
- 500 concurrent limit 是否在页面上有可见错误状态；
- 5 日 timeout 是否由前台或后台显示。

### C. 2015 统一平台迁移

不要从今天的 `122.gov.cn` 页面倒推 2015。

需要找到试点城市当时的：

- 原 local-site announcement；
- redirect；
- platform landing page；
- login/account registration；
- 地方旧入口停用或并存证据。

---

## 16. 对 `how-people-lived` 的贡献

这个旧网对象能改变普通生活史的地方，不是“车管所有网站了”，而是四个机制：

1. **scheduler agency**：学员从等驾校安排，部分转为自己选择考试时间；
2. **queue visibility**：考试场次与满额状态开始能被用户直接看到；
3. **administrative portability**：表格、咨询、预约和后来的全国平台逐步减少为了资格管理而跨城跑腿；
4. **digital-front-end / physical-execution split**：即使管理层高度数字化，驾驶仍是一种必须由身体在真实车辆、道路和考场里证明的能力。

因此旧 Web 在这里既不是“虚拟世界”，也不是现实车管所的镜像。它更像一层不断变厚的 **transaction front end**，把一部分信息、排队和审核状态搬到网页上，而把最难 archive 的身体技能与行政后台留在网页之外。

---

## 17. 本轮结论与饱和判断

本轮新增了此前仓库没有独立建模的旧网对象：**驾驶证报名/预约/考试/发证事务链**。

它新增的技术史机制包括：

- appointment-to-approval gap；
- information-to-counter handoff；
- online form / institution-to-institution transmission distinction；
- slot visibility and capacity gap；
- digital scheduling / physical exam split；
- electronic-evaluation transition；
- local-site / national-platform migration ambiguity；
- public-service-shell / private-credential-state asymmetry。

因此本轮属于**实质新增**，不进入连续三次“无新增”饱和计数。
