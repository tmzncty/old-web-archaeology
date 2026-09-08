# HOSPITAL REGISTRATION / APPOINTMENT / REAL-NAME / SMS / PAYMENT / VISIT STATE GAPS, 2003–2015

## Scope

本研究包只处理约 **2003–2015 中文旧网中的医院预约挂号事务**：医院官网预约、统一预约网站、电话与 Web 共存、实名注册、短信验证码、医院就诊卡/病案号、取号、支付、爽约和现场就诊之间的状态关系。

它不是“中国医疗信息化史”，也不把 2016 年以后公众号、小程序、App 作为主体。后来的移动端材料仅用于验证 earlier transaction 为什么重要、哪些状态长期延续。

Life-history companion：

- `tmzncty/how-people-lived/topics/hospital-registration-appointment-scheduling-and-care-access-executability-china-1980-2026.zh-CN.md`

核心考古问题：

> **旧网页上一个“预约挂号”按钮究竟证明了什么？**

最低边界：

```text
hospital page exists
!= doctor schedule exists
!= slot exposed to this channel
!= request accepted
!= appointment confirmed
!= registration fee paid
!= hospital number issued
!= patient checked in
!= doctor actually seen
```

---

## 1. 为什么这是旧网对象，而不只是医院管理对象

2000s 的网上挂号是一个典型的 **Web shell + hospital transaction backend + offline fulfillment** 系统。

一次看似简单的“网上挂号”可能跨越：

```text
PC browser
→ hospital / city appointment website
→ account database
→ identity fields
→ department / doctor schedule
→ slot quota
→ request state
→ SMS gateway
→ future hospital counter / kiosk
→ hospital registration system
→ real person arrival
→ consultation
```

因此 archive 即使完美保存首页、logo、科室列表和表单，也很可能完全没有保存：

- 当天真实剩余号源；
- 登录态；
- 用户实名资料；
- 动态 POST 结果；
- 短信验证码；
- 医院内部 HIS 的 slot ledger；
- 最终是否到院；
- 现场是否取号；
- 医生是否实际接诊。

这正是中文旧网考古里非常典型的 **transaction preservation gap / 事务保存缺口**。

---

## 2. Evidence contract

遵循仓库 `docs/METHOD.md`：

- **A**：历史网页 capture、同时代官方公告/医院页面/技术文档；
- **B**：同期新闻、记者实测、用户操作报道；
- **C**：多年后医院或用户回忆；
- **D**：研究者根据残存材料重建的事务状态。

本专题尤其不能把下列对象混为一体：

- platform：如“北京市预约挂号统一平台”；
- host：如 `www.bjguahao.gov.cn`；
- page：注册页、医院列表页、科室页、预约结果页；
- account：一个实名患者账户；
- slot record：某医生某日的一条号源；
- appointment record：一次预约事务；
- capture：archive 在某时点保存的一份页面表示。

`current live legacy page` 也不能自动视为 `historical capture`。

---

## 3. 2003 苏州：一个早期中文医院 Web appointment transaction 已经可以被同期文字重建

2003 年 8 月 2 日《江南时报》报道，苏州大学附属第一医院从 8 月 1 日起推出网上预约挂号，给出 historical locator：

```text
http://www.sdfyy.cn/
```

同期描述的事务流程包括：

1. 登录医院网站；
2. 第一次使用时注册；
3. 查询科室专家和科室基本情况；
4. 填写科室、就诊日期、医师；
5. 系统返回所挂号数；
6. 若预约人数超过名额，自动要求另约时间；
7. 当时实行提前两天预约；
8. 网上预约者前 5 位号有保留安排；
9. 就诊当天到医院指定窗口付费取号；
10. 已完成预约可查询和取消。

来源：

- [《“网上预约挂号”给患者“减负”》，2003-08-02，人民网-江南时报转载](https://news.sina.com.cn/o/2003-08-02/1058491035s.shtml) — **B / 同期媒体，high confidence for described workflow; not a capture**。

这足以证明 2003 年当时有人公开提供、描述和操作这类 Web transaction，但仍不能证明原始 HTML、表单 action、JS、charset 或浏览器要求。

### 3.1 最小状态机

```text
UNKNOWN_USER
  ↓ first registration
REGISTERED_PATIENT
  ↓ choose department/date/doctor
REQUEST_COMPOSED
  ↓ submit
CAPACITY_CHECK
  ├─ full → REJECTED_FULL / TRY_OTHER_DATE
  └─ available → RESERVED
                ↓ future arrival
            COUNTER_PAYMENT
                ↓
             NUMBER_ISSUED
                ↓
              WAITING
                ↓
               SEEN
```

### 3.2 关键 gap

**预约成功 != 正式挂号完成。**

2003 材料明确说明预约成功后仍需当日到指定窗口“付费取号”。因此不能把历史页面上的 `预约成功` 解释为患者已经完成整个 registration transaction。

---

## 4. 2003 的“前 5 位网上号”揭示 channel quota 不能和 doctor capacity 混在一起

苏大附一材料说“前5位号留给网上挂号者”。这意味着至少存在两个不同概念：

- physician/session total capacity；
- Web channel reserved quota。

因此应把 slot 拆成：

```text
DOCTOR_SESSION_CAPACITY
→ CHANNEL_ALLOCATION
   ├─ web quota
   ├─ counter quota
   ├─ phone / other quota (if any, must prove)
   └─ reserved / follow-up / special channel (must prove)
```

所以 archive 中如果看到网页写“无号”，只能首先解释为：

> **这个时间点，这个页面/渠道没有可显示或可预约的号。**

不能自动写成：

> “这个医生当天完全没有任何号源。”

---

## 5. 2005：医院官网与电话可以同时存在，不能用 Web 取代整个服务界面

杭州市第三人民医院官方内容记录，2005 年 8 月 30 日起启用免费预约挂号系统，同时提供电话和网站预约，historical locator 包括：

```text
www.hz3yy.com
```

本专题将这种系统记为 **multi-channel appointment front end**：

```text
phone caller ─┐
              ├→ appointment staff/backend → future clinic slot
web user ─────┘
```

必须进一步验证的问题是：

- 电话与 Web 是否实时共享同一号源池？
- 是否预先按渠道分配不同 quota？
- 电话坐席能否看到 Web 用户看不到的内部号？
- Web 满号时电话是否仍可能预约成功？

在没有后台文档前，不能从“同时提供电话和网站”推出“共享同一实时数据库”。

---

## 6. 2009：全国推广以前，中文挂号 Web 是高度异构的

2009 年 9 月，北京三级医院全面推广预约首日的记者实测很适合作为 B 级 transaction survey。

记者在 14:30–15:00 逐一拨打 49 家三级医院预约电话：

- 3 家仍在筹备；
- 30 家可接通；
- 16 家无人接听或长时间占线；
- 有些医院可直接人工电话预约；
- 有些需要预约卡或其他前置状态。

来源：

- [《北京部分医院预约电话无人接听》，2009-09-02](https://news.sina.com.cn/h/2009-09-02/142818565101.shtml) — **B / contemporaneous reporter test**。

这说明“预约挂号上线”在当时不能被建模为一个布尔变量。

更合理的是：

```text
SERVICE_DECLARED
→ CHANNEL_PUBLISHED
→ CHANNEL_REACHABLE_NOW
→ USER_ELIGIBLE_FOR_CHANNEL
→ SLOT_VISIBLE
→ REQUEST_ACCEPTED
→ CONFIRMED
```

`SERVICE_DECLARED = true` 时，其余任何状态仍可能为 false。

---

## 7. 2009 国家制度：Web page 开始和实名身份、病案连续性绑定

2009 年 9 月 30 日卫生部发布《关于在公立医院施行预约诊疗服务工作的意见》，要求从 11 月起公立三级医院开展预约诊疗，并要求：

- 定期更新科室、医师专业和出诊时间；
- 逐步运用信息技术；
- 提高预约尤其是专家号比例；
- 提倡分时预约；
- 预约优先；
- 预约挂号和就诊使用本人有效身份证件实名办理；
- 将预约服务与病案管理、连续医疗逐步连接。

来源：

- [卫生部关于在公立医院施行预约诊疗服务工作的意见，2009-09-30](https://www.nhc.gov.cn/bgt/s9514/200909/d5b3893fff4747cdbf91154f5bf109c8.shtml) — **A / contemporaneous official**。

于是旧网挂号系统不再只是：

```text
anonymous browser → reserve number
```

而越来越接近：

```text
person
↕
legal identity
↕
account / patient record
↕
appointment record
↕
future clinical encounter
```

这是一个重要的 **identity-to-care interface**。

---

## 8. 2009 的反例：预约号总体未用完，热门专家仍然“秒缺”

2009 年 9 月 1—13 日，北京部分三级医院投放预约号源 215860 个，占同期全部号源 14.8%；实际预约 56734 个，占投放预约号 26.3%。同一报道又记录大型知名医院热门专家“一号难求”。

来源：

- [新华社，《北京医院超70%预约号没挂出 大医院仍一号难求》，2009-09-16](https://news.sohu.com/20090916/n266757884.shtml) — **B / contemporaneous survey + official statistics**。

旧网分析中必须因此区分：

```text
TOTAL_APPOINTMENT_SLOT_UTILIZATION
!= HOSPITAL-SPECIFIC SCARCITY
!= DEPARTMENT-SPECIFIC SCARCITY
!= DOCTOR-SPECIFIC SCARCITY
!= CHANNEL-SPECIFIC AVAILABILITY
```

一个页面上看到“剩余号 0”，不能用全市预约率解释；全市大量号没约出，也不能反推热门专家容易预约。

---

## 9. 2011 北京统一平台：旧 Web 已经形成明确可观察的 transaction grammar

2011 年 7 月 28 日，北京市预约挂号统一平台试运行。官方材料给出：

```text
phone: 114 / 010-114
web: www.bjguahao.gov.cn
```

首批 30 家三级医院接入，原则上预约周期 3 个月，预约服务零收费，并实行实名注册。

来源：

- [北京市卫生局，《北京市预约挂号统一平台启动试运行》，2011-07-28](https://wjw.beijing.gov.cn/xwzx_20031/wnxw/201912/t20191214_1174401.html) — **A / contemporaneous official**；
- [《北京市114统一预约挂号平台今启用》，北京日报，2011-07-28](https://www.chinadaily.com.cn/dfpd/bj/2011-07/28/content_13000741.htm) — **B / contemporaneous reporter walkthrough**；
- [中国医学科学院肿瘤医院，《我院预约挂号纳入北京市预约挂号统一平台》，2011-08-25](https://www.cicams.ac.cn/dzb/news/dong/detail/2569.html) — **A/B boundary: original hospital notice hosted by the institution**。

### 9.1 同期记者留下的 Web flow

报道中的浏览器操作为：

```text
REGISTER
  fields:
    real name
    sex
    document type
    document number
    mobile number

→ SELECT HOSPITAL
→ SELECT DEPARTMENT
→ VIEW DOCTOR / FEE / BOOKABLE COUNT / REMAINING COUNT
→ CLICK APPOINTMENT
→ FILL:
    medical record number
    visit card number
    insurance card number
    reimbursement type
    SMS verification code
→ CONFIRM
→ RECEIVE SMS:
    department
    appointment identifier
    visit date
    pickup time
```

这是非常强的 **B-level contemporaneous operation trace**，但仍不是 DOM/capture。

---

## 10. 2011 的实名账户本身已经成为长期事务状态

统一平台同期规则包括：

- 预约前实名注册；
- 一个手机号与有限数量身份证绑定；
- 同一患者在同日/同院/同科限制重复预约；
- 一段时间内预约总量有限制；
- 多次无故爽约可能进入爽约名单；
- 用户需要保管实名身份，避免被号贩使用。

因此历史账户模型至少应包含：

```text
ACCOUNT_CREATED
→ IDENTITY_BOUND
→ PHONE_BOUND
→ PATIENT_PROFILE_ACTIVE
→ APPOINTMENT_HISTORY
→ CANCELLATION_HISTORY
→ NO_SHOW_HISTORY
→ POSSIBLE_RESTRICTION
```

这意味着一次旧网页预约不只是 ephemeral form submit；它可能改变账户以后数月的资格。

---

## 11. “电话 + Web 一个统一平台”也不能草率写成所有状态完全相同

2011 年材料清楚证明 114 电话和 Web 都属于北京统一平台。但具体到某一时点，仍要区分：

- two front ends 是否调用同一 backend；
- 是否看到同一 doctor list；
- 是否共享同一 quota；
- 新号源是否同一秒对两个渠道释放；
- telephone waiting queue 是否在放号时提供另一种先后顺序；
- 网络提交失败后 slot 是否立即释放；
- SMS confirmation 是否两边完全一致。

同期材料中，北京卫生部门曾说明电话预约和网上预约会接入统一号源逻辑，但若研究具体事务，仍应优先寻找平台技术文档或 capture/请求证据，而不是由品牌统一性推断数据库一致性。

---

## 12. Web appointment 的状态不能压成 `booked=true`

建议 old-Web 数据结构把一次挂号拆为：

```text
DOCTOR_SCHEDULE_PUBLISHED
→ SESSION_EXISTS
→ CAPACITY_ALLOCATED
→ CHANNEL_QUOTA_AVAILABLE
→ USER_AUTHENTICATED
→ PATIENT_IDENTITY_VERIFIED
→ REQUEST_SUBMITTED
→ SLOT_TEMPORARILY_HELD?          # unknown unless proved
→ APPOINTMENT_CONFIRMED
→ CONFIRMATION_DELIVERED
→ REGISTRATION_FEE_STATUS
→ ARRIVAL / CHECK-IN
→ NUMBER_ISSUED
→ QUEUE_POSITION
→ CALLED
→ CLINICAL_ENCOUNTER
→ COMPLETED / FOLLOW_UP
```

任何两个箭头之间都可能失败。

### 12.1 一些必须明确写成“不等于”的状态

```text
doctor profile page exists
!= doctor will actually sit clinic that day

schedule published
!= slot currently bookable

request submitted
!= reservation confirmed

reservation confirmed
!= SMS delivered

SMS delivered
!= patient noticed it

appointment confirmed
!= registration fee paid

registration paid
!= patient arrived

patient arrived
!= checked in successfully

checked in
!= doctor seen on time

appointment cancelled
!= slot immediately re-released to all channels
```

---

## 13. Payment state：2003 与 2011 不能用今天的移动支付逻辑倒灌

2003 苏州材料明确是：

```text
online reservation
→ future arrival
→ designated counter
→ payment
→ pickup number
```

2011 北京平台在很多医院也仍涉及到院取号、识别码、就诊卡等流程；不同医院的挂号费结算方式并不完全相同。

所以不能看到今天 App 里 `支付成功` 的模型，就倒推早期 Web 也有：

```text
web reservation → online payment → digital ticket
```

历史 transaction 必须按医院、年份分别证明。

---

## 14. Real-name state：姓名字段存在不等于身份已经核验

旧网页里出现：

```text
姓名
身份证号
手机号
医保卡号
病案号
```

并不能自动证明后台已经完成强身份校验。

应区分：

```text
IDENTITY_TEXT_ENTERED
→ FORMAT_ACCEPTED
→ ID_NUMBER_BOUND
→ PHONE_VERIFIED
→ HOSPITAL_RECORD_MATCHED
→ REAL_PERSON_VERIFIED_AT_VISIT
```

2009–2011 实名制政策能证明制度要求，但某个历史页面到底只做格式校验、数据库校验还是到院二次核验，需要系统级证据。

---

## 15. SMS state：验证码、确认短信和提醒短信是三种不同事务

2011 统一平台报道同时出现短信验证码和预约成功通知。旧网考古中应至少分开：

```text
SMS_OTP_REQUESTED
SMS_OTP_SENT
SMS_OTP_DELIVERED
SMS_OTP_ENTERED
SMS_OTP_ACCEPTED

APPOINTMENT_CONFIRMED_IN_BACKEND
CONFIRMATION_SMS_GENERATED
CONFIRMATION_SMS_GATEWAY_ACCEPTED
CONFIRMATION_SMS_DELIVERED
USER_NOTICED_CONFIRMATION
```

archive 几乎不可能保存最后一段用户手机收件箱。

因此页面 capture 可能证明“系统宣称会发短信”，却通常不能证明某次个人事务的短信真的到达。

---

## 16. No-show / cancellation：用户没来也是数据库事件，而不是“什么都没发生”

统一预约出现以后，取消与爽约逐渐成为系统治理的一部分。

应建模：

```text
CONFIRMED_APPOINTMENT
  ├─ user cancels before deadline
  │      → CANCEL_ACCEPTED
  │      → SLOT_RECLAIMED?       # must prove
  │      → SLOT_REPUBLISHED?     # must prove channel/time
  │
  └─ no check-in by cutoff
         → NO_SHOW_RECORDED
         → ACCOUNT_HISTORY_CHANGED
         → POSSIBLE_RESTRICTION
```

重要：

> `cancelled != automatically visible to next Web user`。

很多现代“候补挂号”机制之所以有意义，正因为退号重新分配本身也是一套状态机。

---

## 17. 2015 boundary：Web 并没有突然被 App 替掉，而是前端越来越多

到约 2015，医院常见前端已经可能包括：

- 医院官网；
- 城市统一预约平台；
- 电话；
- 自助机；
- 现场窗口；
- 银行/电信等合作渠道；
- 微信/支付宝/医院 App；
- 复诊医生工作站。

本仓 scope 在 2015 附近收束时，应避免画成简单谱系：

```text
Web → App
```

更准确的历史是：

```text
one hospital backend / multiple overlapping front ends
```

某些老人继续电话预约；某些年轻人移动端预约；同一个家庭甚至由外地子女通过移动前端替父母操作，而父母本人只在医院现场出现。

---

## 18. Later validation only：2018–2026 说明 earlier state gaps 为什么没有消失

以下不是本仓主体，只用于验证 2003–2015 state model 的持续性。

### 18.1 2018：Web/mobile efficiency 可以把稀缺提前到老人看不见的渠道

70 岁糖尿病患者赵慧茹仍在 6:30 出门去医院排号，但同期报道指出部分专家号在她到现场以前已被网络预约完。[浙江在线，2018-01-18](https://zjnews.zjol.com.cn/zjnews/zjxw/201801/t20180118_6398110.shtml)。

这说明：

```text
physical registration available
!= same opportunity set as online reservation
```

### 18.2 2018：代理人可以和患者身体分离

武汉胡大爷夫妇的女儿在北京，通过支付宝绑定父母就诊信息，远程完成挂号和缴费；父母本人在武汉到院看病。[荆楚网，2018-06-12](https://www.cnhubei.com/xw/jk/201806/t4123360.shtml)。

这验证了 earlier identity model 必须允许：

```text
ACCOUNT OPERATOR != PATIENT BODY
```

### 18.3 2020：digital-primary route 迫使制度重新确认 fallback

2020 年国家卫健委明确要求医院为不会智能技术的老人保留现场挂号、缴费、报告打印等人工窗口，并畅通家人、亲友、家庭医生代预约渠道。[中国政府网，2020-11-26](https://www.gov.cn/xinwen/2020-11/26/content_5565203.htm)。

这验证了早期 phone/window 并不是“应该被 Web 消灭的旧接口”，而可以成为系统 resilience。

### 18.4 2025–2026：候补只是给旧 slot lifecycle 增加新的自动化状态

现代候补挂号把：

```text
CANCELLED SLOT
→ RE-RELEASE
→ WAITLIST MATCH
→ NOTIFY
→ PAYMENT DEADLINE
→ CONFIRMED
```

自动化。它并没有改变本专题最基本的判断：**号源是动态 transaction state，不是静态页面文本。**

---

## 19. Browser / Web environment questions

2003–2011 医院预约页如果取得 capture，应记录：

### Browser assumption

- IE5 / IE6 / IE7 / IE8 是否为主要支持目标；
- 是否使用 ActiveX、弹窗、frameset、`window.open`、document.all；
- JS 关闭后能否提交；
- 是否依赖 HTTPS/TLS，而旧 TLS 今天能否正常回放。

### Charset

重点检查：

- GB2312；
- GBK；
- UTF-8；
- HTTP header 与 `<meta charset>` 是否冲突；
- archive rewrite 是否改写了 form/action 或编码。

### Form / session

- GET vs POST；
- action URL；
- hidden fields；
- ASP/JSP/PHP/session identifier；
- cookie domain/path；
- CAPTCHA；
- SMS OTP；
- 登录是否跨子域；
- doctor/slot 是否 AJAX 动态加载。

### Subresources

- 科室树；
- doctor portrait；
- date picker；
- validation JS；
- CSS；
- image buttons；
- help/manual page；
- error message assets。

没有这些验证时，不应把现代浏览器显示的一张网页写成“当年预约体验”。

---

## 20. Archive preservation model

### 20.1 最容易保存

- 首页；
- 医院介绍；
- “网上预约挂号已开通”的新闻；
- 静态使用帮助；
- 科室/专家公开介绍；
- 注册入口壳。

### 20.2 最容易丢失

- 登录后页面；
- 真实剩余号；
- POST response；
- session cookie；
- CAPTCHA；
- SMS；
- 用户病案号/身份证绑定；
- 取消结果；
- 爽约状态；
- HIS 内部实际 appointment ledger；
- 到院后的取号和叫号记录。

### 20.3 因此

> **archive-visible appointment system ≠ historically executable appointment transaction。**

一个回放页即使仍显示“预约挂号”，如果后台数据库早已死亡，今天点击失败不证明历史上也失败；反过来，今天某个 legacy endpoint 偶然仍能返回内容，也不证明 2005 年原样如此。

---

## 21. Current archive investigation in this slice

### Locators checked

重点历史 locator：

```text
www.sdfyy.cn            # 2003 苏大附一网上预约同期报道
www.hz3yy.com            # 2005 杭州市第三人民医院电话/Web预约
www.bjguahao.gov.cn      # 2011 北京统一预约平台
www.114yygh.com          # 2011 肿瘤医院同期公告使用的统一平台域名
```

### What was attempted

- Web search for archived `sdfyy.cn` and `bjguahao.gov.cn` locators；
- direct Internet Archive CDX URL construction for `www.sdfyy.cn` 2003–2004；
- searches for historical pages under `sdfyy.cn` that might establish host continuity。

### Result

本轮搜索发现后来的 `www3.sdfyy.cn` 页面存在公开 Wayback locator（例如 2013 年科室页面），这可说明该域名体系后来确有 archived material，但**不能证明 2003 网上预约页面已被找到或验证**。

对 `www.sdfyy.cn` 2003–2004 构造的 CDX 请求在当前访问工具中被安全 URL 限制拒绝，未实际取得 response；`bjguahao.gov.cn` 也未取得本轮可实际打开检查的 historical replay。

因此：

> **M1 status: NOT ACHIEVED IN THIS SLICE.**

准确负结论只能是：

> “本轮没有验证到符合 METHOD 最低记录要求的预约挂号 historical capture。”

不能写：

> “Wayback 没有保存这些网站。”

### Missing before M1 use

至少仍需要：

- archive source；
- exact capture URL；
- original URL；
- capture datetime；
- HTTP replay state；
- charset；
- main HTML；
- form action；
- JS/subresource status；
- login/session boundary；
- browser assumption。

---

## 22. Claim ledger

| Claim | Evidence | Grade | Confidence | Boundary |
|---|---|---:|---|---|
| 2003-08-01 苏大附一推出网上预约 | 同期江南时报 | B | high | 功能/URL存在；非capture |
| 2003 流程含注册、科室/医师/日期、容量判断、取消 | 同期流程描述 | B | high | 不证明DOM/JS |
| 2003 预约后仍需现场付费取号 | 同期流程描述 | B | high | 证明reservation != final registration |
| 2009-11 起三级公立医院开展预约诊疗 | 卫生部正式意见 | A | high | 制度要求；不等于所有医院同日成熟 |
| 2009 北京预约渠道实际可达性差异很大 | 记者逐院电话实测 | B | high | 只代表测试时段/样本 |
| 2009 预约总体未充分使用与热门专家稀缺并存 | 北京统计+同期调查 | B | high | 不外推全国 |
| 2011 北京统一平台通过 114 + Web 对公众服务 | 北京卫生部门 | A | high | 不等于每一医院所有号源都在平台 |
| 2011 Web 注册/选院/科/医师/SMS 的操作链存在 | 同期记者实测 | B | high | 非DOM capture |
| 2011 预约事务进入实名账户/爽约治理 | 官方规则+同期报道 | A/B | high | 具体后台实现仍需技术证据 |
| 2003/2011 历史页面原始浏览体验 | 未验证capture | — | unknown | 不应复原为确定历史原件 |

---

## 23. Hindsight risks

### Risk A：把今天的一键移动支付倒灌到 2003 Web

错误。2003 的同期流程明确仍有“到院指定窗口付费取号”。

### Risk B：把“网上预约系统存在”写成当地普通人已经普遍网上挂号

错误。当前证据主要证明 exists / available / some use，缺少 2003 苏州普通患者使用率分母。

### Risk C：把预约成功写成看诊完成

错误。预约只是获得未来 slot；患者还可能未到院、未取号、爽约、医生停诊。

### Risk D：把网页显示无号写成医生没有任何剩余能力

错误。Web quota、窗口、复诊、转诊等渠道可能独立分配。

### Risk E：把实名字段写成强实名核验已完成

错误。需要进一步证明后台验证方式和现场二次核验。

### Risk F：把今天能打开的医院旧内容页当成当年 DOM

错误。`content publication date`、`current server representation`、`archive capture datetime` 必须分开。

---

## 24. Research next steps

下一轮若继续这个专题，优先级应是：

1. 通过可访问的 Internet Archive UI / Common Crawl / Archive-It 等寻找 `sdfyy.cn` 2003–2004 candidate capture；
2. 对 `bjguahao.gov.cn` 2011–2012 找至少两个时点；
3. 若取得 replay，记录 charset、form action、URL pattern、cookie/session、验证码与子资源缺失；
4. 查 2003–2010 同期用户论坛/博客中真实预约成功、失败、满号、取消经验；
5. 分辨医院自营 Web 与第三方预约站的 URL/品牌混淆；
6. 只在有足够 capture 时把这一专题升级为 M1 case candidate。

---

## 25. 这项旧网考古改变了什么

旧网页最容易诱导研究者相信“屏幕上有什么，人就已经拥有什么”。挂号系统恰好证明相反。

一张 2011 年页面可以完整显示医院、科室、医生和“剩余号”，但一个普通患者真正获得诊疗资格，还要穿过实名、短信、号源、取消、取号、缴费、到院、叫号等多个状态。archive 保存得最漂亮的往往只是这条事务链最外面的一层壳。

这也解释了为什么旧 Web 研究必须和生活史交叉：

> **页面的历史意义不在于它第一次出现了“预约”两个字，而在于它是否真的让一个尚未到医院的人，可以把未来某一天的一小段医生时间先锁进自己的生活日历。**

只有把页面状态和现实事务状态分开，我们才知道 Internet 究竟改变了什么，也才知道 archive 丢掉了什么。
