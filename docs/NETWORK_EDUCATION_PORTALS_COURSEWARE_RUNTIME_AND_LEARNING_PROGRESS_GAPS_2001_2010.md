# Network-education portals, courseware runtimes, and learning-progress gaps, 2001–2010

> 研究范围：约 2001–2010 年中文互联网中的高校网络教育 / 现代远程教育 student portal、学习平台、课程资源与校外学习中心的 Web 痕迹。
>
> 本文不是“中国远程教育通史”，也不把广播、电视、函授、自考全部纳入 old-web 主体。1995 年以前的远程教育前史只作为边界说明；全球对照放在 `how-people-lived`。本仓真正关心的是：**一个历史网络教育页面能证明什么，不能证明什么；学生真正完成学习所依赖的账号、软件、后台状态和线下节点又为什么特别难存下来。**

跨仓对应：

- `tmzncty/how-people-lived/topics/educational-reentry-second-chance-routes-and-learning-location-detachment-china-1980-2025.zh-CN.md`

---

## 1. 开工前查重结论

仓库已有大量与动态状态、私有执行和历史页面时间层有关的研究：

- job board / resume database；
- part-time job execution；
- SOHO / intranet shadow；
- remittance transaction backend；
- dating profile / relationship outcome；
- alumni roster / mutable profile；
- credential query / personnel record；
- query/ranking state；
- live legacy rendering；
- roommate listing / cohabitation outcome。

但没有专门处理：

- 网络教育 student portal；
- 历史 courseware runtime；
- 学习进度数据库；
- 作业/考试状态；
- “公共招生页存在”与“某个已注册学生真的能完成课程”之间的证据链。

因此本轮不是重复“登录墙会丢失”这一已有结论，而是把旧网研究对象推进到一个新的状态机：**learning execution**。

---

## 2. 研究单位：不要把“网络学院网站”当成一个页面

对 2001–2010 网络教育，至少拆成以下单位：

1. **institution / programme** — 某高校网络教育学院或远程教育项目；
2. **public site** — 招生、简介、专业、学习中心、政策、软件下载等公开站点；
3. **learning centre** — 某地实体校外学习中心；
4. **student account** — 与入学批次、身份、层次、中心等绑定的账号；
5. **student portal / LMS** — 登录后的课程、通知、进度、作业、考试入口；
6. **course / courseware** — 某门课程和其 HTML、视频、音频、文档、下载包；
7. **support channel** — BBS、聊天室、在线答疑、电话、Call Center、Email、QQ 等；
8. **assessment state** — 作业、在线测试、预约、统考、课程考试、论文等状态；
9. **credential state** — 学籍、毕业、电子注册、学历/学位授予；
10. **capture** — archive 实际保存到的某一次公开响应。

这些不能互换。

尤其禁止：

```text
network college homepage survived
→ student platform survived
→ courseware worked
→ student actually studied
→ student passed
```

---

## 3. 一个更接近真实生活的 state machine

网络教育实际执行链可以暂时建模为：

```text
programme exists
→ public recruitment information visible
→ applicant understands credential type
→ applicant is eligible
→ admission / registration
→ learning-centre assignment or support relationship
→ student account created
→ login succeeds
→ course entitlement appears
→ course material can be opened
→ local software/runtime works
→ learner allocates study time
→ progress is recorded
→ questions/support are exchanged
→ assignment is submitted
→ assessment is completed
→ required offline / unified exam is completed
→ thesis/practicum where applicable
→ graduation audit
→ credential / degree registration
```

档案研究里应该默认：**每个箭头都可能断。**

---

## 4. 2004–2007：网络教育已经是大系统，但仍明显依赖实体服务节点

### Evidence E-01 — 2004 同期行业/教育网络报道

中国教育和科研计算机网 2004 年的高校远程教育招生问答称，当时教育部批准的远程教育试点高校已达 68 所，全国已有 2000 多个学习中心，在册学生超过 200 万。

原始页面：

- <https://www.edu.cn/edu/yuan_cheng/yuan_cheng_jiao_yu/200603/t20060323_89419.shtml>
- 页面正文标注原稿日期：2004-03-05。

**等级：B。**

说明：当前 URL 路径带有 `200603`，而正文标明 2004-03-05，可能经历 CMS 迁移/再发布。不能把当前 URL 结构直接投射为 2004 原始路径。

### Evidence E-02 — 教育部 2007/2008 同期统计

教育部总结称，截至 2007 年底，现代远程教育试点学历教育累计注册学生约 670 万，其中中央电大开放教育学生 458 万；在职人员占 86.5%；普通高校和公共服务体系设校外学习中心 5935 个，中央电大设开放教育教学点 3292 个。

来源：

- <https://www.moe.gov.cn/jyb_xwfb/xw_zt/moe_357/s3580/moe_2448/moe_2450/moe_2456/tnull_39524.html>

**等级：A — 教育部同期官方总结。**

### Claim C-01

**已证实：** 2000s 中后期中国网络高等学历教育已经形成由高校、公共服务系统、学习平台和大量校外学习中心共同组成的体系。

**不能推出：**

- 这些学习中心的实际服务质量相同；
- 每位学生都主要在家学习；
- 所有课程都在线完成；
- “网络教育”就是一个纯 Web 产品。

### Old-web implication

历史网络教育网站应被理解为 **hybrid institutional interface**。

Web 页面只是体系的一层，实体学习中心不是“网络不够先进的残余”，而是当时系统设计的一部分。

---

## 5. 2008 教材给出了比门户截图更有价值的客户端环境证据

### Evidence E-03 — 《网络教育学习指导》

中南大学出版社当前官网保存 2008 年 2 月出版的《网络教育学习指导》书目、前言和详细目录。

来源：

- <https://csup.csu.edu.cn/info/1030/5042.htm>

页面记录：

- 出版时间：2008-02；
- ISBN：978-7-81105-623-5；
- 书中说明中南大学网络教育学院 2001 年开始首批学生教学；
- 编者明确说，一部分网络教育学生对网络使用不熟悉，甚至可能从未上过网，所以教材需要先教授网络技能；
- 目录包含校外学习中心、学习平台、BBS、聊天室、在线辅导答疑、学习进度；
- 工具章节列有超星阅读器、PDF / PS / DVI、FlashGet、RealPlayer、Windows Media Player、QuickTime 4.1.2 等。

**等级：A-/B+。**

- 书本身是 2008 年正式出版的历史 artifact；
- 当前出版社网页是现代 institutional rendering，不是 2008 年 student portal capture；
- 因此可以把书的出版信息和目录作为历史教材证据，但不能把当前页面视觉当 2008 页面形态。

### Claim C-02 — digital literacy was part of the client stack

**已证实：** 至少该教材的设计明确预设部分网络教育学生需要先学习基本 Internet 使用，再进入正式课程。

这意味着：

```text
Internet available to programme
≠ Internet familiar to learner
```

以及：

```text
student enrolled
≠ student can immediately operate the learning environment
```

对旧网复原，这是非常重要的 browser/user assumption。

---

## 6. 不要把教材列出的所有软件误写成“强制系统需求”

历史教材目录列出了多种软件，但 evidence 只直接证明：

> 这些工具被编者认为对网络学习足够常见/有用，值得写进学习指导。

它不自动证明：

- 每门课程都需要 RealPlayer；
- 每个学生必须装 QuickTime 4.1.2；
- FlashGet 是平台自身依赖；
- BBS 和聊天室对所有专业都同样重要；
- 学校服务器在整个 2008 年都提供完全相同的格式。

因此建立规则：

> **tool documented ≠ tool mandatory**

> **format mentioned ≠ format observed in every course**

要证明某门课程实际依赖某播放器，需要进一步取得：

- 历史课程页面；
- 媒体 URL / MIME；
- 软件要求页；
- 同期 student manual / FAQ；
- 或真实历史客户端错误记录。

---

## 7. 浏览器环境不能只记“IE6”三个字

2000s 网络教育复原至少应考虑：

- Windows 版本；
- Internet Explorer 版本；
- ADSL / 校园网 / 单位网络 / 拨号等接入；
- cookie / session；
- Javascript；
- 弹窗；
- 下载管理器；
- PDF/专用阅读器；
- RealPlayer / Windows Media Player / QuickTime；
- 文件压缩/解压；
- 中文编码；
- 流媒体协议/端口；
- 当时带宽；
- 浏览器安全设置；
- 登录后相对链接和动态 URL。

没有历史 courseware capture 时，不应想当然地把今天 HTML5 video 的使用经验套回去。

### Browser reconstruction rule

若未来选择某个网络学院作为 M3 浏览器实验案例，应至少比较：

```text
modern Chromium
vs.
IE6-era Windows environment
```

并明确：

- 能打开公共主页；
- 能否登录；
- 课件 URL 是否仍存在；
- 媒体是否因 plugin/protocol 缺失失败；
- archive rewrite 是否进一步破坏请求。

---

## 8. account-entitlement gap — 账号与课程授权缺口

网络教育 student portal 的关键状态通常不属于公开 URL。

一个学生看到某门课程，往往取决于：

- 账号；
- 入学批次；
- 专业；
- 层次；
- 已选课程；
- 缴费状态；
- 学习中心；
- 学期；
- 后台授权。

因此：

> **login page survived ≠ historical account survived**

> **student account existed ≠ course entitlement can be reconstructed**

这与普通公开网页的 archive gap 不同。

这里缺掉的不是一个 HTML 文件，而是一个历史授权关系。

### 隐私 stop condition

不得为了“复原”而使用泄露账号、密码、成绩数据库或私人学生信息。

对 ordinary-life research，知道“这类授权存在”已经足以建立制度模型，不需要恢复具体普通学生的私有账号。

---

## 9. courseware-runtime gap — 课件运行环境缺口

即使 archive 保存了课程 HTML，也可能没有保存：

- 流媒体文件；
- Real/Windows Media playlist；
- 外部播放器；
- ActiveX/插件；
- 下载包；
- 专用阅读器；
- 字体；
- 跨域脚本；
- 后台生成 token 的媒体 URL。

因此：

```text
course page captured
≠ courseware complete
≠ media playable
≠ historical learning experience reconstructed
```

### 保存偏差

静态目录、课程简介和帮助文档往往比大型媒体资源更容易存活。

结果是后人可能看到：

> “第 3 讲：某某主题”

却完全不知道当年学生实际观看的是：

- 15 分钟低码率 RealVideo；
- 90 分钟课堂录像；
- PPT + 音频；
- 纯文本；
- 下载后的离线包。

所以**课程目录存活率不能代理学习材料存活率**。

---

## 10. learning-progress state gap — 学习进度状态缺口

《网络教育学习指导》目录明确有“学习进度”等学生平台功能。

这类状态通常位于数据库里：

```text
student_id
course_id
unit
last_access
progress
assignment_state
quiz_state
```

但 archive 往往只能保存无身份公共页面。

于是出现旧网历史研究中一个非常大的反差：

> **平台可能保存得比人的学习过程更好。**

我们能知道学校有某门课，却不知道普通学生：

- 打开过几次；
- 学到第几章；
- 停了几个月；
- 是否重修；
- 是自己学还是只在考试前集中学习。

因此：

> **course enrolled ≠ course engaged**

> **course engaged ≠ course completed**

---

## 11. assignment / assessment gap — 作业与考核状态缺口

教育部 2007 年关于网络高等学历教育证书和学位管理的通知明确要求试点高校在招生简章和学生手册中说明网络教育统考、学历文凭、学位授予、电子注册等政策。

来源：

- <https://www.moe.gov.cn/srcsite/A07/moe_743/200704/t20070410_110179.html>

**等级：A。**

这证明网络教育的真实 credential chain 远不止“看完网页”。

需要区分：

```text
course content
→ assignment
→ course assessment
→ required unified examination where applicable
→ graduation audit
→ diploma
→ degree conditions
→ electronic registration
```

### Archive implication

这些结果越来越接近个人受保护教育记录，越不可能被公开 Web archive 完整保存。

所以本仓应把这种缺失记为：

**privacy-compatible absence**，而不是“Wayback 抓得不好”。

---

## 12. support-channel handoff gap — 学习支持跨渠道缺口

2008 教材目录同时记录 BBS、聊天室和在线答疑。

教育部关于公共服务体系的总结还提到 Call Center。

真实学生遇到问题时可能使用：

```text
student portal notice
→ BBS
→ live chat
→ phone / Call Center
→ email
→ QQ
→ local learning-centre staff
```

网络教育因此具有和本仓前面研究的招聘、婚恋、合租类似的 handoff：

> **public/archivable interface → private or off-platform execution**

但这里有一个教育特有区别：

handoff 不只是社交便利，它可能决定一个学生能不能完成作业、修改选课、解决考试预约或恢复账号。

因此：

> **support option listed ≠ support interaction preserved**

---

## 13. centre/offline-execution gap — 校外学习中心与线下执行缺口

教育部统计中的数千个学习中心意味着：

即使课程主要在 Internet 上，普通学生的完整路线仍可能包括：

- 到本地中心咨询；
- 报名/身份核验；
- 面授或辅导；
- 领取/购买教材；
- 计算机机房；
- 考试；
- 现场处理学籍问题。

旧网页可能保存“某市学习中心地址”，却几乎不保存：

- 学生实际去过几次；
- 排队多久；
- 机房电脑是什么配置；
- 当地带宽怎样；
- 工作日晚间是否开放；
- 某年是否搬址；
- 电话是否有人接；
- 某个中心是否实际停办但页面未更新。

因此建立：

> **centre listed ≠ centre operational at every point in the page’s apparent lifetime**

这也是一个 dynamic institutional state。

---

## 14. historical-centre-topology gap — 学习中心网络的时点拓扑缺口

普通旧网研究经常把“友情链接”当图网络；网络教育还存在另一种网络：**机构服务拓扑**。

例如：

```text
university
├── Beijing centre
├── Shenzhen centre
├── Urumqi centre
└── county-level service point
```

这个树会变化：

- 新设；
- 撤销；
- 更名；
- 地址迁移；
- 合作机构更换；
- 招生权限改变。

如果只读取今天的机构历史页，很容易把最后状态倒投到 2005。

未来证据采集应把：

```text
centre_name
city
address
phone
valid_from
valid_to
observed_at
source
```

作为时点字段，而不是静态“校外学习中心列表”。

---

## 15. 2008–2009 handbook pages 的一个额外用途：恢复当时的普通操作词汇

北京中医药大学继续教育学院当前站点保存一篇题为“2008中国大学网络教育学生手册（节选）”的页面，当前页面显示发布时间 2009-11-17，正文把现代远程教育定义为使用计算机网络、多媒体、卫星和电子通信技术连接分离状态的教师与学生，并特别强调这种形式适合在职从业人员的业余学习。

来源：

- <https://jxjyxb.bucm.edu.cn/xwdt/zsdt/2020/08/03/42.html>

**等级：B。**

这里的证据价值不是“今天某大学如何描述网络教育”，而是保留下来的旧 handbook 语言。

但仍需标明：

- 当前 CMS 页面路径/模板明显不是 2009 原始视觉形态；
- 标题说“2008 手册”，当前页面 timestamp 是 2009；
- 本轮没有证实它在 2008 年原来位于哪个 URL。

因此：

> **historical text preserved in current CMS ≠ historical page capture**

该规则与 live-legacy rendering 研究相容，但这里重点是 **manual migration provenance**。

---

## 16. current publisher page ≠ historical student portal

中南大学出版社的书目页今天仍可访问，并保存丰富 2008 内容。

但是：

- 它证明教材存在；
- 它不证明 2008 学生从这个 URL 获取教材；
- 它不证明当前 HTML/CSS 是 2008 设计；
- 它更不能代替当时网络教育学院 student portal。

因此至少区分：

```text
historical printed artifact
current institutional metadata page
historical student-facing website
historical authenticated LMS
```

四者不是同一 evidence object。

---

## 17. 一个建议的 evidence schema 扩展

未来如果 `schemas/evidence.schema.json` 增加教育平台案例，可考虑以下可选字段：

```yaml
subject_type: courseware | student_portal | public_site | learning_centre | handbook
access_scope: public | authenticated | role_restricted | unknown
student_state_required: true
batch_or_term: 2008-spring
course_id: null
runtime:
  browser: ie6-assumed
  plugins:
    - realplayer
  helper_apps:
    - flashget
  evidence_for_requirement: handbook
media_preservation:
  html: unknown
  audio_video: unknown
  downloads: unknown
backend_state:
  progress: not_public
  assignment: not_public
  grades: not_public
offline_dependency:
  learning_centre: documented
  exam_site: documented
confidence: medium
```

这里只是 research note 建议，不替代正式 schema 设计。

---

## 18. 证据分层表

| ID | 时点 | 证据 | 等级 | 可支持 | 不可支持 |
|---|---|---|---|---|---|
| E-01 | 2004 | edu.cn 网络教育招生问答 | B | 试点规模、学习中心存在、当时公开话语 | 所有中心实际运行质量 |
| E-02 | 2007 | 教育部远程教育体系统计 | A | 注册规模、学习中心/教学点、在职比例 | 单个学生的使用方式 |
| E-03 | 2008 | 中南大学《网络教育学习指导》 | A-/B+ | 当时教学工具、部分学生数字技能前提 | 每门课程的强制软件需求 |
| E-04 | 2007 | 教育部证书/学位管理通知 | A | 统考、学历学位、电子注册属于 credential chain | 某学生是否毕业 |
| E-05 | 2008/2009 | 网络教育学生手册节选 | B | 同期/近同期对远程学习方式的制度说明 | 原始页面视觉、个人学习结果 |

---

## 19. Known / probable / unknown

### 已证实

- 2000s 中国高校网络教育已经达到大型制度化规模；
- 网络教育并非纯线上体系，而有大量实体学习中心/教学点；
- 2008 年正式学习指导材料仍需要教授部分学生 Internet 基础；
- 当时学习工具生态包括 BBS、聊天室、在线答疑、专用阅读器和多种流媒体/下载工具；
- 学历教育还有考试、证书、学位、电子注册等独立制度接口。

### 高概率但尚需具体站点验证

- 大量历史 courseware 在现代浏览器/现代网络环境中无法原样运行；
- archived public pages 会系统性高估“公开说明”的保存，低估实际 authenticated learning execution；
- 历史学习中心列表存在较大时间状态变异；
- LMS 的 progress / assignment / grade 状态几乎不会进入公开 Web archive。

### 不知道

本轮仍不知道：

- 中南大学 2008 某门实际课程的原始 courseware URL；
- 当时 student portal 的 HTML/JS 结构和 session 机制；
- 哪些课程实际强依赖 RealPlayer / QuickTime / Windows Media；
- 某个普通学生一次完整学习流程的 clickstream；
- 某学习中心 2005/2008/2010 三个时点的地址与设备变化；
- BBS/聊天室是否有可公开、非敏感的 archive capture。

---

## 20. Archive gaps specific to network education

本轮建议正式加入缺失地图词汇：

### 20.1 account-entitlement gap

账号和课程授权关系消失。

### 20.2 courseware-runtime gap

HTML 存活，但媒体、插件、客户端软件、协议或动态 token 消失。

### 20.3 learning-progress state gap

个人学习进度位于私有数据库，公开 archive 看不见。

### 20.4 assessment-state gap

作业、测验、考试预约、成绩和毕业审核属于受保护业务状态。

### 20.5 student-support handoff gap

BBS / chat / phone / email / QQ / 本地中心之间的支持链断裂。

### 20.6 centre/offline-execution gap

网页保存课程，真实报名、面授、考试或身份处理却在线下执行。

### 20.7 historical-centre-topology gap

今天看到的校外学习中心列表不能自动代表历史时点。

### 20.8 manual-migration provenance gap

旧手册文本可能被迁移到现代 CMS，却失去原始 URL、页面结构和发布时间语境。

---

## 21. 重要硬边界

今后研究 2001–2010 中文网络教育站点，默认写入：

```text
public recruitment page ≠ enrollment
```

```text
login page ≠ working historical account
```

```text
account ≠ course entitlement
```

```text
course listing ≠ courseware preserved
```

```text
courseware preserved ≠ runtime works
```

```text
runtime works ≠ student actually studied
```

```text
progress shown ≠ assignment passed
```

```text
online learning ≠ fully online credential chain
```

```text
learning centre listed ≠ centre operational at that exact historical time
```

```text
historical text in current CMS ≠ historical page rendering
```

---

## 22. 隐私与伦理边界

网络教育 archive 特别容易诱导研究者寻找个人成绩、作业或学生账号。

本仓停止条件应比普通公开网页更严格：

- 不使用泄露数据库；
- 不测试历史账号密码；
- 不公开普通学生姓名 + 成绩 + 学号；
- 不从搜索引擎缓存拼接私人学习记录；
- 不恢复已删除私人 BBS/QQ 对话；
- 公开案例优先使用 institutional manual、公开帮助页、匿名化统计和公开人物报道。

**个人学习进度不可见通常是正确的隐私结果，不是需要被“修复”的 archive failure。**

---

## 23. 它改变了我们对中文旧网的哪一点理解

以前容易把中文旧网考古想成：

```text
主页 / 论坛 / 博客 / SNS
```

网络教育平台提醒我们，还有大量非常普通、但不适合“怀旧截图”的 Web：

```text
student portal
enterprise OA
banking portal
job backend
government query system
```

这些系统对普通人的人生后果很大，却恰恰因为：

- 登录；
- 私有状态；
- 动态数据库；
- 插件；
- 大媒体；
- 线下制度接口

而极难被公共 Web archive 完整保存。

所以 old-web archaeology 的历史可见性不能只问：

> “当年网页长什么样？”

还必须问：

> **“当年网页只是一个信息表面，还是一个真正改变个人资格和生活进度的业务接口？”**

网络教育就是后一种典型对象。

---

## 24. 下一步最有价值的窄任务

不要继续收集“某大学网院有多少学生”。

最高价值下一步是选择 **一个 2004–2009 高校网络教育平台**，尽量获得至少两个历史时点，并恢复：

1. public homepage；
2. 学习中心列表；
3. student login；
4. 一门课程的 courseware locator；
5. 同期 student manual / FAQ；
6. 浏览器/播放器要求；
7. Wayback 对主 HTML 和媒体的保存差异；
8. 绝对不触碰个人账号的前提下，说明哪些 authenticated states 已永久不可见。

如果能找到同一课程在 2005 与 2009 的两个时点，尤其值得比较：

```text
Real/WM/下载式课件
→ 后来的 Flash/网页化课件
```

但只有实际 archive evidence 支持时才能写这种技术迁移，不能按常识补线性进化。
