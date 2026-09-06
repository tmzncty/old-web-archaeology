# Hospital appointment Web registration and remote-care state gaps, 1999–2015

## Scope

本 note 研究约 1999–2015 中文 Web 中**医院预约挂号、实名注册、统一预约平台、移动入口与早期远程医疗前台**留下了什么，以及 archive 能证明什么、不能证明什么。

它不是中国医疗服务史，也不研究 2015 年后的互联网医院全史。1999 以前的电话预约只作为理解旧 Web 的前史边界；2015 以后的 App / 互联网医院主要由 companion `how-people-lived` 承接。

研究单位严格按本仓 METHOD 分开：

- hospital / institution；
- official site / host；
- appointment page；
- third-party booking platform；
- unified public booking platform；
- user account / patient identity；
- dynamic slot inventory；
- one booking transaction；
- one confirmation / SMS / e-mail；
- physical check-in and encounter；
- archive capture；
- claim。

不能把它们合成一句“某医院 2009 年可以网上挂号”。

Companion ordinary-life note：

- <https://github.com/tmzncty/how-people-lived/blob/main/topics/from-window-queue-to-remote-follow-up-healthcare-entry-appointment-executability-and-care-continuity-china-1980s-2026.zh-CN.md>

---

## 1. Claim contract

本题最容易发生的是 **shell-to-outcome leap**：档案留下一个“网上预约”按钮，研究者就写成“患者当时已经能顺利预约并看上医生”。

至少必须固定以下边界：

`hospital site exists ≠ appointment page exists`

`appointment link exists ≠ endpoint responds`

`endpoint responds ≠ registration works`

`registration works ≠ identity verification succeeds`

`doctor shown ≠ slot currently available`

`slot shown ≠ slot reserved`

`form submitted ≠ server accepted`

`booking accepted ≠ confirmation received`

`confirmation received ≠ patient collected ticket / checked in`

`check-in ≠ doctor actually encountered`

`online consultation link exists ≠ legally / clinically valid first diagnosis`

`current legacy page carrying a 2009 date ≠ verified 2009 memento`

对于 archive，动态号源尤其危险。一个 capture 最多证明：

> 某个时刻，档案抓到了某个页面状态。

它不能自动证明：

- 其他时间也有相同号源；
- submit POST 被档案保存；
- 后台真正锁定号源；
- SMS / email 已送达；
- 患者最后来院；
- 医生实际接诊。

---

## 2. 前史边界：电话预约先于普通 Web，但旧 Web 继承了同一套 credential / inventory 问题

2009 年北京医院预约方式调查回顾，北京大学人民医院从 1996 年已使用电话预约磁卡：患者购卡、预存金额，再用固定电话预约；北医三院也有预约卡体系。

来源：

- 北京晚报 / 新浪，2009-08-31，B/C：<https://news.sina.com.cn/h/2009-08-31/113318547636.shtml>

这不属于本仓核心年代中的“网页对象”，但它解释了为什么后来的 Web 预约并不是从零开始。电话时代已经有：

```text
patient identity / card
→ stored balance
→ appointment service
→ hospital slot inventory
→ confirmation
→ physical attendance
```

Web 把其中一些入口和展示状态搬到浏览器，但没有消灭后台号源、实名、医院卡和到院报到。

因此本仓不使用“window → Web”这种过度线性的谱系；更准确是：

```text
window / queue
+ telephone/card booking
+ hospital Web frontends
+ third-party booking sites
+ unified booking platform
+ mobile / WeChat / App
```

多套入口长期并存。

---

## 3. 1999 early Web：存在历史 locator，但还没有本轮核验的 transaction capture

2006 年《人民日报》对北京预约挂号历史的调查回顾，北京市卫生部门 1999 年已推动预约挂号卡，覆盖五十多家医院，并可通过电话或 Internet 使用。

来源：

- 人民日报 / 新浪，2006-01-19，B：<https://finance.sina.com.cn/xiaofei/consume/20060119/07102288409.shtml>

2009 年另一篇同期调查将北京卫生部门预约网络的起点同样追到 1999 年前后，并说明十年间网上/电话预约仍只是整体门诊中的一部分。

来源：

- 人民日报 / 新浪，2009-08-20，B：<https://news.sina.com.cn/h/2009-08-20/110918475562.shtml>

### 可证实

- 1999 前后北京存在面向公众的电话/Internet 预约服务这一制度与功能层事实。

### 尚不能证实

本轮没有取得并实际打开：

- 1999 原始预约首页的已核验 memento；
- 原始 host / URL family 的完整谱系；
- HTML / frameset / form 结构；
- HTTP charset；
- browser requirement；
- submit method；
- session / cookie；
- slot inventory request；
- payment handoff；
- confirmation page。

因此不能从 2006/2009 的回顾文字重建一个“1999 北京网上挂号界面”。

---

## 4. 2009 是一个罕见的 service-state cross section：49 家医院并没有一个统一 Web 状态

北京晚报 2009-10-29 的记者体验对当时 49 家三级医院进行了电话与网络预约测试，是本题非常有价值的 B 级近原始操作证据。

来源：

- <https://news.ifeng.com/mainland/200910/1029_17_1410577.shtml>

报道明确记录：

- 49 家医院中，23 家官网找不到网络预约链接；
- 有医院官网打不开；
- 有医院网站可打开，但预约链接失效；
- 10 家被记者实际测试的官网可通过注册进入网络预约；
- 不少官网主要只是说明电话预约；
- 有医院把网络预约导向第三方平台；
- 不同医院对身份、手机、既往就诊卡和确认方式要求差异很大。

这说明同一天、同一城市、同一级别医院仍存在完全不同的 **appointment frontend state**：

```text
A. no visible online booking link
B. link visible but endpoint broken
C. official page contains instructions only
D. official site redirects to third party
E. account registration required
F. admin/manual confirmation required
G. mobile verification required
H. e-mail booking workflow
I. functional interactive booking
```

因此 archive sampling 如果只挑“成功留下来的漂亮预约页”，会严重高估 2009 年网络预约的一致性与成熟度。

---

## 5. 2009 historical locators and transaction patterns

以下对象目前是**historical locators / contemporary described hosts**，不是本轮已核验 WARC transaction。

### 5.1 `www.ikang.com` — hospital → third-party handoff

同期记者记录，部分医院官网把网络预约导向爱康网 `www.ikang.com`，再按城市、医院、科室、医生逐级选择。

来源：

- 北京晚报 / 凤凰，2009-10-29：<https://news.ifeng.com/mainland/200910/1029_17_1410577.shtml>

潜在状态链：

```text
hospital official page
→ third-party booking host
→ city
→ hospital
→ department
→ clinician
→ slot
→ identity
→ confirmation
```

考古风险：

- hospital page capture 与 third-party capture 时间可能不同；
- redirect/link survives 并不等于 target transaction survives；
- third-party platform later redesign may erase hospital-specific historical workflow；
- 同一品牌今天仍存在也不能证明 2009 技术栈连续。

### 5.2 `iask.mtzyy.com.cn` — registration + administrator confirmation

煤炭总医院同期说明要求首次预约在 `http://iask.mtzyy.com.cn/` 注册用户名和密码，再等待管理员回复；只有特定管理员回复才算有效确认。

来源同上。

这类流程不是普通的：

`form → immediate booking success`

而更像：

```text
account creation
→ request posted
→ human administrator reviews
→ administrator reply
→ user must encounter reply
→ booking considered confirmed
```

所以一个 archive 若只保存注册页或请求页，仍然无法证明 transaction completion。

### 5.3 identity + phone verification + prior-patient binding

同期报道记录，北京回龙观医院网上预约要求姓名、年龄、性别、身份证号和手机号；复诊患者还需患者 ID / 就诊卡号，并通过手机确认身份，当时手机验证还有运营商限制。

这补出几个独立 state：

`public form exists`

≠ `user has accepted mobile carrier / number`

≠ `identity accepted`

≠ `prior patient record linked`

≠ `booking allowed`。

对 old Web 考古而言，公开页面最可能保存下来，而 SMS verification、患者 ID 匹配和医院后台则几乎天然落在 archive 黑区。

### 5.4 `www.crrc.com.cn` + e-mail booking — Web instructions, mail transaction

北京博爱医院同期页面说明 24 小时接受预约，historical locator 为 `www.crrc.com.cn`；但实际 transaction 需要把姓名、身份证号、联系电话发送到指定 e-mail，预约成功后再通过邮件通知，并要求在规定时间到挂号室领取预约号。

来源同上。

这是一种特别值得记录的 hybrid state：

```text
Web page = instructions / locator
email = request channel
hospital staff = booking decision
email = confirmation channel
physical window = pickup / execution
```

因此“医院有网上预约”可能根本没有一个 HTML POST form。

如果只 archive HTML，而没有私人邮箱交易，最关键的 transaction state 必然消失。

隐私规则：本 note 不重新扩散历史普通患者的预约邮件内容；即使将来 archive 偶然保存了个人资料，也按 METHOD 研究必要最小化处理。

---

## 6. 官方 Web 的另一层问题：search result ≠ official provenance

2009-11-04 北京晚报调查记录，一名患者从搜索引擎搜索“北京××医院网上挂号”后进入一个高度类似预约页的站点；填写个人信息过程中发现 URL 与医院官方预约地址不同。记者继续检查搜索结果，并通过页面留下的 QQ / 电话确认部分页面实际由号贩经营。

来源：

- 北京晚报 / 凤凰，2009-11-04，B：<https://news.ifeng.com/society/1/200911/1104_343_1420260.shtml>

这里新增一个旧网状态层：**entry provenance / 入口来源**。

```text
search query
→ ranked result
→ page visually resembles hospital booking
→ user decides whether result is official
→ identity data may be entered
→ contact moves to phone / QQ
→ physical scalper acquires ticket
```

因此：

`hospital name in page title ≠ hospital-operated host`

`doctor schedule copied correctly ≠ hospital authorization`

`search engine ranking ≠ institutional authenticity`

`form asks for real ID ≠ legitimate real-name system`。

### Archive implication

后来的 archive 很可能同时保存：

- 真医院预约说明；
- 第三方合法预约平台；
- 商业导医；
- 号贩/仿冒预约页；
- SEO 博客或聚合页。

研究者不能因为所有页面都带“网上挂号”就把它们归到一个 platform family。

至少应分别验证：

- host ownership / operator；
- official-site backlink / redirect；
- contemporaneous institutional announcement；
- page contact model；
- fee model；
- 是否需要线下代排队。

---

## 7. 2009 policy changed the expected state contract, but policy ≠ every hospital implementation

卫生部 2009-09-30 发布《关于在公立医院施行预约诊疗服务工作的意见》，要求自 11 月起三级公立医院普遍开展预约诊疗；要求公开科室、医生专业和出诊时间，推广实名预约、分时段预约，并逐步提高预约尤其专家门诊比例。

来源：

- 卫生部，2009-09-30，A：<https://www.nhc.gov.cn/bgt/s9514/200909/d5b3893fff4747cdbf91154f5bf109c8.shtml>

这个文件可以证明**国家层面的 expected service contract**，不能自动证明：

- 每家医院 2009-11-01 都有可用 Web 表单；
- 所有预约入口都 24 小时；
- 所有专家号都进入预约池；
- 所有医院都使用同一字段；
- 实名校验实现相同；
- 实际等待时间同步下降。

这一点正好被 2009 年记者对 49 家医院的实测差异反证。

---

## 8. 2011 unified platform: address unification is not backend unification

北京市卫生部门 2011 年解释建设 114 统一预约挂号平台的原因时，明确指出此前医院各有预约电话和网址，不便群众记忆使用，因此需要统一电话、网络入口和号源数据管理。

来源：

- 北京市卫生局，2011-06-21，A：<https://wjw.beijing.gov.cn/xwzx_20031/wnxw/201912/t20191214_1174492.html>

同期北京世纪坛医院资料记录统一平台网址 `www.bjguahao.gov.cn`，并把 114 电话、网络预约和院内医生工作站预约并列。

来源：

- 北京市卫生部门 / 北京世纪坛医院，2012-era institutional note：<https://wjw.beijing.gov.cn/xwzx_20031/jcdt/201912/t20191215_1229620.html>

### 新 state model

统一平台带来：

```text
one public address
→ hospital directory
→ department / doctor / slot data
→ identity
→ reservation
→ sequence number
→ hospital check-in
```

但研究上必须继续拆：

`unified URL ≠ unified hospital backend`

`slot displayed on platform ≠ hospital HIS has same state at every moment`

`reservation sequence ≠ final outpatient registration`

`central identity accepted ≠ local medical-record linkage complete`。

### Archive implication

统一平台会让 Web 更容易保存一个稳定 shell，却可能让真实 hospital-specific state 更不透明：

- 前台 HTML 只是一层；
- 号源数据可能来自 API / backend；
- patient authentication 在 session 内；
- real-time inventory 变化太快；
- check-in 在医院本地系统完成。

因此 unified platform archive 不能被误读成“完整保存了当时北京挂号系统”。

---

## 9. 2014–2015：旧 Web 的末端不是消失，而是成为 QR code / mobile service 的跳板

### 9.1 WeChat added another frontend, not a replacement of every older channel

2014 年北京多家医院开始推进微信预约。同期报道明确说电话、网络、自助机、窗口仍并存，并且中老年患者使用微信可能存在障碍。

来源：

- 中国广播网 / 人民网，2014-11-25，B：<https://politics.people.com.cn/n/2014/1125/c70731-26089420.html>

2015 年 114 统一预约平台的微信公众号进入测试，仍要求真实姓名和有效证件信息。

来源：

- 京华时报 / 人民网，2015-02-03，B：<https://politics.people.com.cn/n/2015/0203/c70731-26495015.html>

这意味着旧 Web 页可能逐渐承担：

```text
institution identity
+ service instructions
+ QR code
+ App download link
+ account migration notice
```

真实 transaction 则转移到微信 / App。

### 9.2 2015 Beijing Children’s Hospital App exposes a new reservation-lock state

2015 新京报记者体验北京儿童医院 App 时记录：绑定患儿/监护人身份和就诊卡后选号，预约后必须在 10 分钟内支付，否则号源自动释放；紧俏科室一周内仍可能只剩少量号。

来源：

- 新京报 / 人民网，2015-04-07，B：<https://health.people.com.cn/n/2015/0407/c14739-26804767.html>

这里出现旧 Web 末期/移动时代非常重要的状态：

```text
slot visible
→ user selects slot
→ temporary hold / payment window
→ payment succeeds in time
→ booking confirmed
OR
→ timeout
→ slot released back to inventory
```

所以：

`click reserve ≠ final reservation`。

### Archive implication

一个静态截图几乎无法恢复这种 **time-sensitive reservation lock**。需要 transaction log / client state / backend response，而这恰好通常不会进入公开 Web archive。

---

## 10. State machine for archaeology

对约 1999–2015 的医院预约对象，建议至少使用以下状态机：

```text
patient needs care
→ discovers hospital
→ discovers official or third-party appointment entry
→ verifies entry provenance
→ chooses department / clinician
→ observes schedule / slot inventory
→ creates account or provides identity
→ credential / phone / patient-card validation
→ selects slot
→ [optional temporary lock]
→ submits request
→ server / staff accepts request
→ payment if required
→ confirmation generated
→ confirmation encountered by patient
→ patient travels to hospital
→ physical ID / card verified
→ ticket / check-in completed
→ patient enters clinical queue
→ doctor encounter occurs
→ follow-up state is created
```

### 强制分离的 gap

#### 10.1 `site / booking-link gap`
官网存在，但没有预约入口。

#### 10.2 `link / endpoint gap`
页面有链接，但 target 已失效。

#### 10.3 `official / third-party provenance gap`
预约发生在医院外部平台，必须证明授权关系。

#### 10.4 `search / authenticity gap`
搜索结果可见，但可能是仿冒、号贩或聚合页。

#### 10.5 `registration / verification gap`
账号创建成功，不等于身份证、手机号、就诊卡验证成功。

#### 10.6 `doctor-directory / inventory gap`
医生姓名、出诊表存在，不等于当前有可预约号源。

#### 10.7 `visible-slot / lock gap`
号源可见，不等于已为当前用户锁定。

#### 10.8 `submit / acceptance gap`
表单提交动作不等于后台真正接受。

#### 10.9 `acceptance / encounter gap`
预约成功不等于患者按时到院，也不等于医生实际接诊。

#### 10.10 `booking / clinical-routing gap`
系统可以正确完成预约，但患者可能挂错专业；这属于现实任务失败，不是 Web transaction 失败。

---

## 11. What archives are structurally likely to preserve — and what they are likely to lose

### 容易保存

- hospital homepage；
- “预约挂号”说明；
- doctor directory；
- static schedule；
- third-party booking link；
- terms / notice；
- registration shell；
- FAQ；
- public unified-platform shell；
- later migration notice；
- QR code / App promotion page。

### 难保存或不应公开

- real-time slot inventory；
- user session；
- identity document values；
- phone verification code；
- patient ID / hospital card mapping；
- POST transaction；
- temporary reservation lock；
- payment state；
- SMS / private email confirmation；
- hospital-side manual confirmation；
- local HIS synchronization；
- no-show；
- actual doctor encounter；
- patient diagnosis / medical record。

由此出现 **public-booking-shell / private-clinical-state asymmetry**：

> 历史上最容易留下来的，是“看起来已经很数字化”的页面；最难留下来的，却是决定一个病人有没有真正看上医生的那些状态。

---

## 12. Archive biases specific to appointment systems

### 12.1 success-shell bias

成功上线过的预约页面比“电话一直占线、链接长期坏掉、管理员没回复”更容易成为可展示档案。

### 12.2 static-schedule bias

医生出诊表是静态内容，容易抓；真实号源库存变化是动态状态，难抓。后人因此会高估“看到医生列表”与“能挂到医生”之间的一致性。

### 12.3 official-site bias

研究者天然偏向医院官网，但 2009 患者真实发现路径经常从百度 / Google 开始；搜索排序、SEO 和仿冒站点也是历史 experience 的一部分。

### 12.4 frontend-survival bias

统一平台 shell 幸存，不代表各医院后台、短信网关、支付接口、HIS 和线下取号过程同时幸存。

### 12.5 mobile-handoff gap

2014–2015 后，Web 可能只留下二维码和 App 下载页；真正 transaction 转入微信 / native app，传统 Web archive 的可见性反而下降。

### 12.6 privacy-shaped absence

预约系统天然包含身份证号、手机号、病历/就诊卡号等敏感信息。它们没有进入公共 archive 并不是单纯“保存失败”；很多时候这是合理且应被继续维护的隐私边界。

---

## 13. Browser / encoding / client assumptions

本轮尚未取得足够 M1 capture，因此以下全部保持 unknown：

- 1999 北京预约站是否依赖 IE-only；
- 2009 各医院表单的原始 charset（GB2312 / GBK / UTF-8）；
- 是否使用 iframe / frameset；
- 是否依赖 ActiveX；
- JS 是否进行身份证格式校验；
- 手机验证码是否由 AJAX / full-page POST 触发；
- `iask.mtzyy.com.cn` 的论坛/问答系统具体产品和版本；
- `www.crrc.com.cn` 当时预约说明是否由静态 HTML、CMS 或动态模板生成；
- third-party platform handoff 是否使用 query parameters 传递医院/医生 ID；
- 统一平台 `www.bjguahao.gov.cn` 早期 slot data 的 endpoint / refresh model。

没有旧浏览器/capture 验证前，不应从今天还能打开的新闻描述推断这些实现细节。

---

## 14. M1 evidence status for this run

### A/B evidence obtained

1. 2009 卫生部正式预约诊疗意见（A）；
2. 2009 北京晚报对 49 家医院电话/Web 预约的同期实际测试（B）；
3. 2009 北京晚报对搜索引擎仿冒/号贩挂号页的同期调查（B）；
4. 2011 北京卫生部门关于统一 114 平台原因与设计目标的官方说明（A）；
5. 2014–2015 微信/App 预约的同期服务说明与记者操作测试（B）。

### Historical locators obtained

- `www.ikang.com`
- `iask.mtzyy.com.cn`
- `www.crrc.com.cn`
- `www.bjguahao.gov.cn`

这些 locator 均来自可定位的同时代/近同时代材料。

### M1 negative result

**本轮没有实际打开并检查一份满足 M1 条件的 1999–2011 中文医院网络预约 Wayback/WARC transaction capture。**

尝试进一步定位时，当前可用的普通 Web 检索能确认历史 host 与报道，但没有在本轮形成可实际检查的 memento transaction。因此以下不能写成“已恢复”：

- historical DOM；
- HTTP charset；
- JS validation；
- form action / method；
- cookie / session；
- dynamic slot response；
- identity verification；
- SMS/e-mail delivery；
- booking acceptance；
- payment；
- hospital HIS handoff；
- physical encounter state。

写法必须是：

> `candidate historical locator found; transaction capture not verified in this research slice`。

不能写成：

> `Wayback 没有保存`。

---

## 15. Next M1 work

最值得继续的不是再搜一批“医院开通网上挂号”的新闻，而是对少量高价值 locator 做 capture-level 检查：

1. `www.crrc.com.cn` 2009 前后的预约说明页：检查主 HTML、charset、邮件 workflow 和静态/动态页面形态；
2. `iask.mtzyy.com.cn`：确认当时产品类型、注册/回复页面与 administrator-confirmation 状态是否有 memento；
3. `www.bjguahao.gov.cn` 2011–2012：至少取得两个历史时点，检查 unified shell、医院/科室目录与动态 slot 子资源缺失；
4. 搜索 2009 医院官网到 `www.ikang.com` 的真实 historical outbound link capture，确认 handoff provenance；
5. 对一个 2014–2015 微信/App 迁移页做 Web→QR/App handoff case，明确传统 Web archive 在移动 transaction 前的断点。

完成其中任一个时，都必须记录：

- original URL；
- capture URL；
- capture datetime；
- HTTP/replay state；
- missing subresources；
- charset；
- browser assumption；
- whether transaction itself can be tested；
- privacy boundary。

---

## 16. What this changes about Chinese old-Web history

医院预约是一个很好的提醒：**旧 Web 的历史不能只研究页面“长什么样”，还要研究页面是不是一个真实世界稀缺资源的入口。**

同样一个“预约挂号”按钮，背后可能分别是：

- 纯说明页；
- 电话预约指南；
- 第三方商业平台；
- 人工管理员回复；
- e-mail 请求；
- 手机实名验证；
- 统一实时号源；
- 甚至仿冒/号贩页面。

网页视觉相似，现实 state machine 却完全不同。

这类对象也暴露出旧网考古最典型的历史可见性倒置：

> **最公开、最容易被保存的是入口；最私人、最短暂、最决定现实结果的是交易。**

如果不把两层拆开，后人会很容易从一张幸存的网页截图误以为，当年的普通患者已经拥有一个完整、稳定、低摩擦的数字医疗系统。

---

## Sources

- 卫生部，2009-09-30：《关于在公立医院施行预约诊疗服务工作的意见》：<https://www.nhc.gov.cn/bgt/s9514/200909/d5b3893fff4747cdbf91154f5bf109c8.shtml>
- 北京晚报 / 凤凰，2009-10-29，49 家医院预约体验：<https://news.ifeng.com/mainland/200910/1029_17_1410577.shtml>
- 北京晚报 / 凤凰，2009-11-04，搜索引擎仿冒预约页调查：<https://news.ifeng.com/society/1/200911/1104_343_1420260.shtml>
- 人民日报 / 新浪，2006-01-19，北京预约挂号早期状态：<https://finance.sina.com.cn/xiaofei/consume/20060119/07102288409.shtml>
- 人民日报 / 新浪，2009-08-20，患者排队与预约制度调查：<https://news.sina.com.cn/h/2009-08-20/110918475562.shtml>
- 北京晚报 / 新浪，2009-08-31，各医院预约方式：<https://news.sina.com.cn/h/2009-08-31/113318547636.shtml>
- 北京市卫生局，2011-06-21，114 统一预约平台：<https://wjw.beijing.gov.cn/xwzx_20031/wnxw/201912/t20191214_1174492.html>
- 北京妇产医院 / 北京市卫生部门，2011-07-20：<https://wjw.beijing.gov.cn/xwzx_20031/jcdt/201912/t20191215_1229292.html>
- 中国广播网 / 人民网，2014-11-25，北京医院微信预约：<https://politics.people.com.cn/n/2014/1125/c70731-26089420.html>
- 京华时报 / 人民网，2015-02-03，114 微信版：<https://politics.people.com.cn/n/2015/0203/c70731-26495015.html>
- 新京报 / 人民网，2015-04-07，北京儿童医院 App transaction：<https://health.people.com.cn/n/2015/0407/c14739-26804767.html>

---

*Initial draft was AI-assisted. Historical locators are not promoted to verified captures; patient identity and medical-state data are intentionally excluded except where a published contemporary source is minimally necessary to support a mechanism claim.*
