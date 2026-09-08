# SCHOOL_HOME_SMS_XIAOXUNTONG_ATTENDANCE_PARENT_PORTAL_GROUP_CHAT_AND_ACTION_STATE_GAPS_2003_2015

> 中文旧网交叉切片：2003—2015 年家校通信中的“校讯通/家校通”、短信、WAP、网站、语音、学生卡、成绩/作业状态与现实行动之间的状态缺口。
>
> 主 scope：约 2003—2015 中文互联网与其短信/移动通信交界。1980s—1999 海外 homework hotline / parent portal 只作前史比较；2018—2026 家长群、专用 App、大学家长群只作 earlier-state 的 afterlife 校验，不把本仓扩成当代教育平台史。
>
> 检索日期：2026-09-08。
>
> life-history companion：`tmzncty/how-people-lived/topics/from-parent-meeting-to-real-time-school-observability-home-school-communication-and-parental-monitoring-china-1980-2026.zh-CN.md`

---

## 0. 为什么这是旧网考古，而不是教育技术产品史

“校讯通”很容易被一句话写成：

> 学校通过互联网和短信把作业、成绩、考勤发给家长。

但这句话把至少六层状态压扁了：

```text
学校真实发生的事件
→ 教师/设备是否记录
→ 记录是否进入后台数据库
→ 是否生成一条可发送信息
→ 短信/WAP/Web/语音渠道是否成功
→ 家长是否真正收到、看到、理解
→ 家长是否有能力行动
→ 现实行动是否改变学生处境
```

所以本切片研究的不是“某产品有哪些功能”，而是：

1. 一个 2003—2015 的家校通信事务实际跨过哪些系统；
2. SMS、WAP、Web、voice、IC card 为什么不能合并成一个“网站”；
3. “实时”在哪一层成立，在哪一层可能延迟；
4. 家长号码、学生身份、考勤记录、成绩、消息如何被绑定；
5. archive 为什么最容易留下产品宣传，却最难留下普通家庭真正收到的消息；
6. 为什么今天仍能看到 2007 年新闻页，仍然不等于我们已经复原 2007 年校讯通服务。

必须遵守 `docs/METHOD.md`：

```text
exists
!= available
!= used
!= popular
!= caused
```

并进一步固定：

```text
feature advertised
!= feature enabled at a school
!= student enrolled
!= guardian number correctly bound
!= event recorded
!= message generated
!= message delivered
!= guardian noticed
!= guardian acted
```

---

## 1. 研究单位：不要把“校讯通”当成一个统一网站

2003—2015 的中文材料里，“校讯通”“家校通”“家校亲情卡”“校信通”等名称可能对应：

- 地方教育局 + 中国移动/联通等运营商合作；
- 第三方服务商提供的软件/托管中心；
- 学校本地读卡器与后台；
- 运营商 SMS gateway；
- WAP 页面；
- PC Web 管理后台；
- 家长登录门户；
- 12580/其他语音入口；
- IC/智能卡；
- 亲情电话终端；
- 学校内部成绩/学籍/考勤系统。

所以一次研究至少要区分：

```text
brand
service provider
carrier
school deployment
backend host
teacher interface
guardian interface
student card/terminal
message route
account/identity binding
```

即使两个城市都把服务称为“校讯通”，也不能默认：

- 数据库 schema 相同；
- 域名相同；
- 收费方式相同；
- 支持相同运营商；
- WAP/Web 页面相同；
- 学生卡协议相同；
- “已到校”触发逻辑相同。

---

## 2. 海外前史边界：家校远程信息早于 Web，本仓只把它当比较参照

### 2.1 1981 homework hotline：电话已经能把“家庭必须去学校”拆开

1981 年《Christian Science Monitor》报道，加州 Porterville 学区让 1—12 年级学生每周四晚通过电话联系值班教师处理作业问题，部分时段提供西班牙语支持。

Locator:
https://www.csmonitor.com/1981/1113/111301.html

Evidence grade: **B contemporaneous media**.

1990 年《Washington Post》又报道巴尔的摩使用计算机驱动的电话录音系统，家庭可 24 小时拨学校号码听当天作业。

Locator:
https://www.washingtonpost.com/archive/local/1990/01/11/homework-hot-line-helps-students-parents/bf304ff7-1160-43d0-9f64-81eae96072b8/

Evidence grade: **B contemporaneous media**.

对本仓的意义只是边界：

> `remote school-home communication` 早于 WWW；Web/SMS 后来改变的是数据来源、自动触发、粒度和反馈周期。

### 2.2 1999 parent portal：Web 把“季度成绩单”压缩成滚动数据库视图

1999 年旧金山湾区 Antioch High 已有 Internet 家长入口查看 attendance、grades 等；同期 PowerSchool 产品材料明确强调实时查看成绩、考勤与作业，反衬季度/学期反馈的迟缓。

Locators:
- https://www.sfgate.com/education/article/Parents-Can-Track-Students-On-Internet-New-2910341.php
- https://librarytechnology.org/document/22624
- https://librarytechnology.org/document/22625

Evidence grade: **B contemporaneous media/vendor documents**.

跨国共同变化是：

```text
periodic report
→ database-backed query
→ event-level visibility
```

中国 2003—2015 的特殊路线则更多经过运营商短信、WAP、托管中心和智能卡，而不是只靠家庭 PC portal。

---

## 3. 中文旧网强锚点 A：2004 武汉“互联网 + 固话 + 手机”

2004 年湖北日报/搜狐现存同期报道描述武汉十余所学校使用“家校通”，并明确说系统利用 Internet、固定电话、移动电话实现家校互动；家长可以用短信询问，教师在网络端发布信息。

Locator:
https://news.sohu.com/2004/05/31/67/news220326799.shtml

Evidence grade: **B contemporaneous media**.

这条来源能证明：

- 至迟 2004 年武汉已有 multi-channel 家校通信部署个案；
- Internet 可能处在教师/后台侧，家长只使用 SMS/phone；
- “家长上网”不是这种基础设施影响家庭生活的必要条件。

不能证明：

- 十余所学校代表武汉普及；
- 所有功能都由一个 Web host 提供；
- 当前搜狐转载页面就是 2004 服务页面；
- 家长短信全部成功送达。

---

## 4. 中文旧网强锚点 B：2005—2006 学生卡把物理动作接进消息系统

### 4.1 泉州“家校亲情卡”

2005 年 CERNET 的同期材料描述：学生刷卡出入学校后可以触发家长短信；系统也含亲情电话、网站查询成绩/评语等，突发天气时学校可用短信发停课通知。

Locator:
https://www.edu.cn/xxh/xy/200510/t20051017_143387.shtml

Evidence grade: **B contemporaneous education/IT media**.

### 4.2 广州越秀区“校讯通”

2006 年广州日报/新浪报道，越秀区 110 所中小学开始部署校讯通。记者现场描述学生刷卡后到校/离校信息自动进入家长手机，教师可以批量发送通知、作业和测验成绩；广州市七中首批使用者约占学生三分之一，报道明确当时并非硬性要求。

Locator:
https://news.sina.com.cn/o/2006-09-25/061210099682s.shtml

Evidence grade: **B contemporaneous media**.

这两条材料支持下面的 attendance transaction model。

---

## 5. Attendance state machine：`刷卡` 不是一个布尔值

```text
CARD_ISSUED
→ CARD_BOUND_TO_STUDENT_ID
→ GUARDIAN_NUMBER_BOUND
→ READER_ONLINE
→ CARD_PRESENTED
→ READER_ACCEPTED_TOKEN
→ LOCAL_EVENT_WRITTEN
→ EVENT_SYNCED_TO_BACKEND
→ RULE_EVALUATED (ARRIVAL/DEPARTURE)
→ MESSAGE_COMPOSED
→ SMS_GATEWAY_ACCEPTED
→ CARRIER_ROUTED
→ HANDSET_RECEIVED
→ GUARDIAN_NOTICED
→ GUARDIAN_INTERPRETED
```

必须固定：

- `card issued != card carried that day`
- `card presented != student identity independently verified`
- `reader beep != backend sync complete`
- `backend record != SMS generated`
- `SMS generated != carrier accepted`
- `carrier accepted != handset received`
- `handset received != guardian saw it`
- `“17:45离校” != student safely arrived home`

历史研究若看到一条宣传语“实时通知家长”，最多可以先记录 **intended transaction semantics**，除非另有日志/SLA/用户材料，不能写成所有消息实际秒级送达。

2011 年南方日报调查甚至记录，有用户因为网络拥堵在半夜才集中收到此前的“校讯通”消息，这正是 `event time != delivery time` 的同期反例。

Locator:
https://tech.sina.com.cn/t/2011-10-25/08056225302.shtml

Evidence grade: **B contemporaneous media/user quote**.

---

## 6. Grade / homework state machine：页面或短信上的数字也有来源链

```text
ASSESSMENT_HAPPENED
→ SCORE_RECORDED_BY_TEACHER
→ SCORE_ENTERED/IMPORTED_TO_SYSTEM
→ STUDENT_ID_MATCHED
→ VISIBILITY_RULE_APPLIED
→ MESSAGE/PORTAL VIEW GENERATED
→ GUARDIAN AUTHORIZED
→ GUARDIAN RECEIVES/VIEWS
→ GUARDIAN INTERPRETS
→ OPTIONAL FAMILY ACTION
```

需要固定：

- `exam completed != score finalized`
- `teacher has score != score entered into platform`
- `score entered != correct student mapping`
- `portal can show grades != school enabled it`
- `school enabled it != all families subscribed`
- `grade delivered != context delivered`
- `grade visible != learning diagnosis`

2013 年南方日报调查已经直接暴露最后一层问题：教师说编一条校讯通短信往往需要斟酌，因为只发分数/表现可能伤害孩子或变成应试式通报。

Locator:
https://edu.rednet.cn/c/2013/11/11/4051033.htm

Evidence grade: **B contemporaneous media**.

---

## 7. 2005 “亲子通”：position state machine 与 consent state machine 必须分开

新华社/新浪 2005 年报道上海移动相关服务时，描述“亲子通”允许家长查询孩子位置；报道同时保留被查询者提醒、同意/关闭机制，并采访了觉得像被监视的学生。

Locator:
https://news.sina.com.cn/c/2005-08-21/11316742437s.shtml

Evidence grade: **B contemporaneous media**.

不能把这一服务抽象为：

```text
parent → gets child location
```

至少要拆：

```text
NUMBER/DEVICE ENROLLED
→ GUARDIAN RELATION/REQUEST ACCEPTED
→ LOCATION QUERY SUBMITTED
→ NETWORK PRODUCES LOCATION ESTIMATE
→ CHILD NOTIFICATION/CONSENT STATE
→ RESULT RETURNED
→ USER INTERPRETS RESULT
```

并固定：

- `phone location != child body location in all cases`
- `location available != permission valid`
- `guardian wants location != student accepts continuous visibility`
- `service technically supports off switch != child can socially use it without consequence`

这也是旧网/移动前智能机时代少见但非常重要的 **monitoring consent gap**。

---

## 8. 2007 规模化：MAS / ADC 证明“学校有没有网站”不是唯一数字化路径

2007 年教育部与中国移动合作的 CERNET 同期报道写得很具体：

- 信息化程度高的学校：部署 MAS（移动代理服务器）；
- 信息化程度低的学校：使用 ADC（应用托管中心）；
- 终端通道：短信、彩信、WAP；
- 截至 2006 年 11 月：报道口径称校讯通用户达到 1244 万。

Locator:
https://www.cernet.edu.cn/xxh/fei/xin_xi_zi_xun/importantnews/200701/t20070116_214721.shtml

Evidence grade: **A/B contemporaneous institutional media**.  
Count treatment: **provider/institutional count; do not equate to independent households or national penetration**.

这给旧网方法增加一个必须保留的 topology：

```text
LOW-IT SCHOOL
→ hosted application center (ADC)
→ carrier/network services
→ family SMS/WAP/voice
```

与：

```text
HIGHER-IT SCHOOL
→ local/server integration (MAS)
→ carrier/network services
→ family channels
```

两者都可能被媒体称作“校讯通”，但 server ownership、data custody、failure mode 不同。

所以：

**no public school website != no networked school-home service**。

---

## 9. 2007 中山：12580 + electronic display 说明“家长到学生”也不一定经过学生手机

CERNET 2007 年中山材料除了刷卡短信，还写到家长可拨打 12580，把留言显示在学校电子屏上；学生可借亲情电话联系绑定号码。

Locator:
https://www.edu.cn/xg_zi_xun_5782/20070605/t20070605_236172.shtml

Evidence grade: **B contemporaneous media/service case**.

这使 communication route 至少有：

```text
SCHOOL → GUARDIAN SMS
GUARDIAN → 12580 → SCHOOL DISPLAY → STUDENT
STUDENT → SCHOOL VOICE TERMINAL → BOUND FAMILY NUMBER
GUARDIAN → WEB/WAP → PLATFORM
```

所以旧网研究不能只抓一个域名，然后说已经抓到了“家校通”。

**service = distributed transaction across web, telecom, card and school hardware.**

---

## 10. 2008 同期访谈：同一功能对家长和学生是不同事务

《中国教育报》2008 年访谈里：

- 家长陆传文：工作忙、不能总去学校，孩子进入初中后也更少主动讲，希望系统把无法直接了解的信息带给自己；
- 中学生汪波：安全通知可以接受，但如果学校事无巨细把自己的校内生活发给父母，会觉得压力，希望由自己决定怎样沟通；
- 教育研究者指出不同年龄段的学生对隐私、自主空间需求不同。

Locator:
https://www.cernet.edu.cn/xxh/xy/200802/t20080219_280128.shtml

Evidence grade: **B contemporaneous structured interview**.

这要求 archive / reconstruction 不只建“消息发送状态”，还要有 `audience legitimacy state`：

```text
STATE EXISTS
→ SCHOOL MAY RECORD
→ SCHOOL MAY SHARE
→ GUARDIAN MAY RECEIVE
→ STUDENT MAY/MAY NOT CONSENT
```

也就是说：

**technically shareable != socially legitimate to share**。

---

## 11. Provider / carrier state：加入一项学校服务可能等于加入一个电信关系

### 11.1 2005 铜川：已有手机仍被迫增加终端/号码

新华社/新浪同期报道里，有家长已经有两部手机，却因为学校推广的家校通安排而认为自己还得购买/使用指定小灵通或固定通信服务。

Locator:
https://news.sina.com.cn/s/2005-09-12/09556920624s.shtml

Evidence grade: **B contemporaneous complaint/media**.

### 11.2 2009 北京：运营商不兼容

北京青年报/中新网 2009 年报道部分学校推广家校通时，有家长投诉原运营商号码不能使用，需要再办移动号码；市教委当时把具体合作称为学校/区县与商家之间的市场行为。

Locator:
https://www.chinanews.com.cn/it/it-txxw/news/2009/10-22/1924026.shtml

Evidence grade: **B contemporaneous media**.

因此 enrollment state machine 至少是：

```text
SCHOOL SELECTS SERVICE
→ FAMILY INFORMED
→ CONSENT / SOCIAL PRESSURE
→ COMPATIBLE CARRIER/NUMBER EXISTS?
→ NEW NUMBER/SERVICE MAY BE REQUIRED
→ FEE / PACKAGE ACCEPTED
→ STUDENT-GUARDIAN BINDING ENTERED
→ SERVICE ACTIVE
```

必须固定：

- `school says voluntary != family experiences choice as voluntary`
- `family owns a phone != phone carrier compatible`
- `compatible number != subscription activated`
- `service activated != guardian wants every feature`

“数字鸿沟”在这里不只是有没有设备，也包括 **carrier compatibility / operator lock-in**。

---

## 12. Message delivery state：2010—2011 同期用户材料说明“实时”会沉淀成习惯，也会出现拥堵

2010 年南方日报佛山校讯通报道保存了多名家长/教师自述。一名家长说以前了解孩子要打电话、等家长会或考后评价表，现在会及时收到信息；另一名家长说每天收短信已经成为习惯。报道中的具体文本包括 17:45 刷卡离校和当天语文作业。

Locator:
https://news.sina.com.cn/c/2010-05-28/082817575890s.shtml

Evidence grade: **B contemporaneous media / user quote**.

2011 年调查则记录网络拥堵导致半夜集中收信的用户体验。

Locator:
https://tech.sina.com.cn/t/2011-10-25/08056225302.shtml

Evidence grade: **B contemporaneous media / user quote**.

这两条放在一起很重要：

```text
expected latency becomes short
→ family reorganizes attention around that expectation
→ delayed delivery is experienced as system failure / intrusion
```

“实时”因此不只是技术指标，也会变成普通人的时间习惯。

---

## 13. 2013—2015：校讯通已经进入“功能够多，但商业/责任边界不清”的阶段

2013 年南方日报调查写到，校讯通面世十年后已经叠加考勤、作业、通知、成绩等功能；家长一方面抱怨短信轰炸、变相强制，教师另一方面也觉得如何写消息是一种额外劳动。

Locator:
https://edu.rednet.cn/c/2013/11/11/4051033.htm

Evidence grade: **B contemporaneous media**.

2014 年北京相关规定要求学校不得为商业机构办理“校讯通”提供便利；同年教育评论强调，即使叫停收费型产品，家校沟通本身仍然需要其他方式继续承担。

Locator:
https://edu.people.com.cn/n/2014/1014/c1053-25829348.html

Evidence grade: **A/B policy + contemporaneous commentary**.

因此到本仓主 scope 末段，不能写成：

`校讯通退出 = 家校数字通信退出`。

更准确的 transition 是：

```text
carrier-bound paid dedicated channel
→ generic QQ/WeChat groups and other apps
→ lower marginal message cost
→ much higher message volume and looser work boundaries
```

2016 以后这个 afterlife 由通用 IM 主导，本仓不展开为完整当代史。

---

## 14. Web / WAP / SMS / voice 不同通道的状态不能合并

### SMS

```text
content saved
→ gateway accepted
→ carrier routed
→ handset received
→ notification surfaced
→ guardian read
```

### WAP

```text
WAP URL known
→ mobile data service usable
→ compatible handset/browser
→ authentication succeeds
→ page rendered
→ target record available
```

### PC Web portal

```text
host resolves
→ HTTP responds
→ legacy browser compatibility
→ login/session succeeds
→ account authorized
→ data query succeeds
→ correct student record renders
```

### Voice / 12580

```text
number reachable
→ IVR/agent route works
→ identity/target info accepted
→ message/query stored
→ school terminal/display receives
→ student/family hears/sees it
```

### Card terminal

```text
reader powered/networked
→ card accepted
→ event written
→ backend sync
```

所以即使同一份宣传资料列出“短信、WAP、网站、语音、智能卡”，也只能证明 **product/service claims multi-channel support**，不能证明每个学校、每个用户、每一天都同时拥有这些通道。

---

## 15. Authentication / identity binding：谁的成绩为什么会发到这个号码？

家校平台隐藏着一条身份链：

```text
STUDENT RECORD
↔ STUDENT ID / SCHOOL ID
↔ CARD ID
↔ CLASS / TEACHER
↔ GUARDIAN RELATION
↔ GUARDIAN PHONE NUMBER
↔ SERVICE ACCOUNT
```

研究时至少要问：

- 谁录入家长号码？
- 一个学生能否绑两个/多个照护者？
- 父母换号后谁更新？
- 隔代照护者是否可以成为主要接收人？
- 号码回收后旧绑定会不会留下？
- 班级变更、转学后旧权限如何撤销？
- 兄弟姐妹在不同学校、不同运营商平台时家庭是否要维护多个账号/号码？

同期公开材料很少回答这些后台细节。因此本专题把这些列为 **unknown**, 不从“家长手机收到短信”反推一套现代 OAuth/统一账号逻辑。

---

## 16. Group-chat afterlife（2018—2019）：低成本消息把另一种状态缺口放大

这部分超出本仓主 scope，只作为 2003—2015 专用系统的 afterlife 校验。

2018 年中国新闻网/人民网对教师的同期采访中，北京班主任形容家长微信群让自己“每天都是家长会”；幼儿园教师每天要发学生吃饭、活动照片，重要通知又会被大量“收到”回复盖住。

Locator:
https://edu.people.com.cn/n1/2018/0910/c1053-30283119.html

2018 年《法制日报》还采访到一名家长因为孩子幼儿园没有微信群而产生焦虑，因为不进群可能错过重要信息。

Locator:
https://legal.people.com.cn/n1/2018/1030/c42510-30370925.html

Evidence grade: **B contemporaneous media**.

这验证 early dedicated system 的一个 afterlife：

> 专用 SMS 时代主要担心“能不能送到”；通用群聊时代又增加“送到以后是否被几十条无关消息淹没”。

因此：

`delivery success != information salience`。

---

## 17. 2025 afterlife：read receipt 把“是否看到”重新变成平台字段

2025 年人民网报道浙江一所学校“嗨家校”个案：教师回忆微信群里通知常被连续“收到”盖住；专用平台会显示已读/未读家长，并可一键提醒未读，同时承载请假、电子签名、学情等结构化流程。

Locator:
https://zj.people.com.cn/n2/2025/0720/c186327-41296690.html

Evidence grade: **B contemporaneous institutional case**.

这条 afterlife 很有方法意义：

早期 SMS archive 最难证明的是：

```text
sent → delivered → read?
```

二十年后的专用平台开始把 `read` 变成显式数据库状态。但即使这样：

`marked read != understood != acted`。

事务状态只是在继续向后延伸。

---

## 18. 2024—2026 afterlife：技术可见性延伸以后，开始反向治理“谁不应该一直看”

2024 年《中国青年报》关于大学家长群的报道里，有大学生对父亲从家长群转来班级六级排名表示反感；教育评论把问题指向成年学生自主权。

Locators:
- https://yn.people.com.cn/n2/2024/0323/c378440-40785753.html
- https://dxs.moe.gov.cn/zx/a/jj/240301/1879367.shtml

2026 年人民日报社《讽刺与幽默》评论辽宁葫芦岛市要求班主任/任课教师退出家长群、由学校统一管理，理由包括教师“24 小时隐形办公桌”、家长焦虑和学生自主性。

Locator:
https://paper.people.com.cn/fcyym/pc/content/202603/13/content_30155389.html

Evidence grade: **B contemporaneous reporting/commentary**.

这些 afterlife 不用于把本仓写到 2026，而用于验证 2005—2008 已经出现的 privacy/monitoring state gap 确实没有自然消失。

---

## 19. Archive / preservation：最关键的家庭状态天然最不容易进入公共 Web 档案

### 19.1 容易保存

- 媒体报道；
- 产品宣传；
- 运营商社会责任报告；
- 教育信息化会议报道；
- 公开产品说明；
- 公开投诉/政策。

### 19.2 很难保存

- 真实 SMS payload；
- 手机收件箱时间戳；
- 网关重试/失败日志；
- 登录后的成绩/评语；
- 学生卡绑定；
- 读卡器本地日志；
- 家长电话号码；
- 教师后台草稿；
- 私有 WAP 页面；
- QQ/微信群；
- 学生与父母回家后的争论；
- 错绑/换号/欠费/退订记录。

因此一个很强的历史偏差是：

**archive preserves what the service said it could do more easily than what an ordinary family actually experienced.**

### 19.3 Public article surviving today != 2007 service capture

CERNET、Sina、人民网等今天仍能提供标注 2005—2011 日期的新闻/专题正文。它们是很有价值的 surviving publisher objects / contemporaneous texts，但不是校讯通服务本身的 historical replay。

尤其不能因为 2007 新闻写“网站 + 短信”，就说已经抓到了：

- 当时登录页；
- 当时 HTML/charset；
- 当时 WAP markup；
- 当时 cookie/session；
- 当时家长查询页面；
- 当时学校管理员后台。

---

## 20. Historical locator candidates 与本轮 replay 状态

### 20.1 可登记 locator

本轮可登记但未验证为 2003—2015 capture 的对象：

- `xxt.cn`：当前第三方 WHOIS/站点索引显示域名注册于 2005-04-02，现已离线，并把注册主体指向河南校信通教育科技有限公司；该信息只能作为 **D / current third-party locator lead**，不能单独证明 2005 页面内容。
  - locator evidence: https://webrate.org/site/xxt.cn/
- `www.lexue.cn`：当前 36Kr 项目信息把它列为河南校讯通相关企业的官方网址；也是 **D / current project metadata lead**，不能反推 2007 的 host 内容。
  - locator evidence: https://pitchhub.36kr.com/project/2074526182981896
- 12580：2007 中山同期报道明确将其作为家长留言入口，但它是语音 service number，不是 Web host。
- CERNET/Sina 的同期文章 URL：它们是 evidence pages，不是 transaction service endpoints。

### 20.2 本轮 archive 尝试

本轮尝试直接访问：

- `https://web.archive.org/web/20090101000000/http://xxt.cn/`
- `https://web.archive.org/web/20100101000000/http://xxt.cn/`
- CDX query for `xxt.cn`, 2005—2015

当前 Web 访问工具因安全 URL 解析限制拒绝了构造 replay/CDX URL，未取得可检查的 capture。

因此：

**M1: NOT ACHIEVED IN THIS SLICE.**

准确表述只能是：

> 本轮没有验证到一份可按 `docs/METHOD.md` 检查 capture datetime、HTTP headers、charset、DOM、WAP/JS/subresources、login/session 的 historical replay。

绝不能写：

> “Wayback 没有保存校讯通。”

没有成功查询 != archive 不存在。

---

## 21. 建议未来 historical replay 一旦取得，必须检查什么

### HTTP / encoding

- status code；
- `Content-Type`；
- declared charset；
- GB2312/GBK/UTF-8 实际字节一致性；
- redirect chain；
- HTTP vs HTTPS。

### browser / layout

- table / frame / iframe；
- IE-only control；
- ActiveX / plugin；
- JavaScript errors；
- WAP/WML/CHTML 等移动页面；
- image/JS host 是否同域。

### session

- anonymous landing vs login-only；
- student/guardian account type；
- captcha；
- SMS verification if any；
- cookies/session IDs；
- school/region selector。

### transaction

- attendance query；
- grade query；
- homework/notice；
- message compose/send；
- phone-number binding；
- unsubscribe；
- card ID state；
- WAP route；
- error messages。

### privacy

- whether student/guardian data leaked into URLs/query strings；
- whether search engines could index private pages；
- whether cached pages expose names/scores；
- whether public archives preserved PII accidentally。

若以后取得涉及未成年人真实个人数据的 capture，应优先记录结构，不在仓库复刻敏感数据。

---

## 22. Evidence matrix

| Claim | Source type | Grade | What it proves | What it does not prove |
|---|---|---:|---|---|
| 2004 武汉存在多通道家校通个案 | contemporaneous media | B | internet/phone/SMS service existed in some schools | citywide adoption |
| 2005 上海位置查询已有隐私争议 | contemporaneous media + student quote | B | monitoring concern existed contemporaneously | prevalence/accuracy |
| 2005—06 卡片可触发到离校短信 | education/media reports | B | intended workflow + deployed cases | every swipe/delivery success |
| 2007 MAS/ADC + SMS/MMS/WAP | institutional media | A/B | provider deployment architecture | all regions same stack |
| 2008 parent/student conflict | structured contemporaneous interview | B | competing needs were articulated then | national attitude distribution |
| 2009 carrier lock-in complaint | contemporaneous media | B | participation could require compatible number | all schools coerced families |
| 2010 parent habitual SMS use | contemporaneous media quote | B | some users integrated service into daily routine | general adoption |
| 2011 delayed night messages | contemporaneous media quote | B | delivery latency could diverge from event time | systematic SLA |
| 2013 message-authoring burden | contemporaneous media | B | teacher communication was labor | all teachers same burden |
| 2014 policy pushback | policy/media | A/B | commercial school facilitation was contested/restricted | digital communication ended |
| 2018 group-chat overload | contemporaneous interviews | B | generic IM created attention/work-boundary issues | all classes use WeChat |
| 2025 read-receipt platform | contemporaneous case | B | structured notification can explicitly model read state | nationwide trend |

---

## 23. 关键 state gaps 清单

### Event / attendance

- `physical event != recorded event`
- `reader beep != backend event persisted`
- `event persisted != timestamp perfectly accurate`
- `card swipe != body location`

### Message

- `teacher clicks send != server accepted`
- `server accepted != SMS gateway accepted`
- `gateway accepted != delivered`
- `delivered != read`
- `read != understood`
- `understood != action possible`

### Identity

- `student name != verified student ID`
- `guardian number != current caregiver`
- `number bound != same owner forever`
- `one guardian != whole household`

### Grade / homework

- `score entered != final score`
- `score visible != context visible`
- `homework sent to parent != homework communicated to student`
- `parent informed != parent responsible for execution`

### Consent / privacy

- `guardian entitled to some information != entitled to all school life`
- `student is minor != zero autonomy interest`
- `location technically queryable != continuous monitoring legitimate`

### Commercial access

- `school adopts service != household freely opted in`
- `family has phone != compatible carrier`
- `service advertised free != all associated telecom cost zero`

### Archive

- `news article survives != service survives`
- `service landing page survives != login transaction replayable`
- `HTML captured != SMS/voice/card backend captured`
- `product feature list != user outcome`

---

## 24. 这条 old-Web 切片改变了什么

中文旧网的“普通生活事务”不应该只研究发生在浏览器里面的动作。

校讯通尤其清楚地证明：

```text
学校读卡器
→ 本地/托管数据库
→ Internet/专网
→ 运营商短信网关
→ GSM/CDMA handset
→ 家庭注意力
```

可能是一条完整的数字事务，而家庭从头到尾一次网页都没打开。

所以 1995—2015 中文互联网史如果只按“哪些网站出现了”来写，会漏掉一整类 **Internet-backed but non-Web-facing ordinary life**。

更深一层是，系统真正改变的不是“家长有了一个网站”，而是一个过去很厚的信息空白被拆成越来越细的事件：

```text
期中才知道成绩
→ 当天短信知道作业
→ 刷卡几秒后知道离校
→ 后来群里不断看到照片
```

到了这一步，历史研究的问题也必须跟着变化：

> 页面能不能打开已经不够。我们还要知道谁被记录、谁被通知、谁能拒绝、消息什么时候到、谁必须回应，以及一个系统把“关心”变成“持续可见”以后，普通家庭和学生究竟得到什么、又失去什么。

---

## Sources / locators

Contemporaneous China core:
- https://news.sohu.com/2004/05/31/67/news220326799.shtml
- https://news.sina.com.cn/c/2005-08-21/11316742437s.shtml
- https://www.edu.cn/xxh/xy/200510/t20051017_143387.shtml
- https://news.sina.com.cn/o/2006-09-25/061210099682s.shtml
- https://www.cernet.edu.cn/xxh/fei/xin_xi_zi_xun/importantnews/200701/t20070116_214721.shtml
- https://www.edu.cn/xg_zi_xun_5782/20070605/t20070605_236172.shtml
- https://www.cernet.edu.cn/xxh/xy/200802/t20080219_280128.shtml
- https://www.chinanews.com.cn/it/it-txxw/news/2009/10-22/1924026.shtml
- https://news.sina.com.cn/c/2010-05-28/082817575890s.shtml
- https://tech.sina.com.cn/t/2011-10-25/08056225302.shtml
- https://edu.rednet.cn/c/2013/11/11/4051033.htm
- https://edu.people.com.cn/n/2014/1014/c1053-25829348.html

Overseas prehistory:
- https://www.csmonitor.com/1981/1113/111301.html
- https://www.washingtonpost.com/archive/local/1990/01/11/homework-hot-line-helps-students-parents/bf304ff7-1160-43d0-9f64-81eae96072b8/
- https://www.sfgate.com/education/article/Parents-Can-Track-Students-On-Internet-New-2910341.php
- https://librarytechnology.org/document/22624
- https://librarytechnology.org/document/22625

Afterlife only:
- https://edu.people.com.cn/n1/2018/0910/c1053-30283119.html
- https://legal.people.com.cn/n1/2018/1030/c42510-30370925.html
- https://yn.people.com.cn/n2/2024/0323/c378440-40785753.html
- https://dxs.moe.gov.cn/zx/a/jj/240301/1879367.shtml
- https://zj.people.com.cn/n2/2025/0720/c186327-41296690.html
- https://paper.people.com.cn/fcyym/pc/content_30155389.html

Locator leads, not verified captures:
- https://webrate.org/site/xxt.cn/
- https://pitchhub.36kr.com/project/2074526182981896
