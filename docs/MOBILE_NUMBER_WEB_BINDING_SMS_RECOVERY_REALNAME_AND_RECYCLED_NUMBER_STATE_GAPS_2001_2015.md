# MOBILE_NUMBER_WEB_BINDING_SMS_RECOVERY_REALNAME_AND_RECYCLED_NUMBER_STATE_GAPS_2001_2015

## 0. Scope

本研究包只处理 **约 2001—2015 中文 Web / IM / 网游 / 互联网账号与手机号码之间的绑定、短信验证、账号恢复、实名与二次放号状态缺口**。

它不是：

- 中国移动通信通史；
- 手机硬件史；
- 短信文化史；
- 2015 年以后的 App/移动互联网治理总史；
- 全球 phone-number identity 总史。

1987—2000 的移动电话/寻呼前史以及 2019—2026 的携号转网、一证通查、二次号码焕新等长期后果，主要写入 companion：

`tmzncty/how-people-lived/topics/PHONE_NUMBER_REACHABILITY_PORTABILITY_ACCOUNT_BINDING_AND_NUMBER_RECYCLING_1987_2026.md`

本仓真正要解决的是：

> **当中文旧网开始把一个电信号码当作注册、付费、密保、验证码、通知或身份恢复入口以后，“一个网页说这个号码已经绑定”到底跨越了哪些系统；而当号码销号并重新分配时，为什么第三方账号不会自动知道电信侧已经换了一个人。**

---

## 1. Research unit

严格按照 `docs/METHOD.md`，本专题必须把以下对象分开：

```text
mobile operator network
SIM / subscriber account
phone number (MSISDN-like public identifier)
SMS gateway / billing interface
Internet platform
Web account / IM account / game account
binding record
browser page / client UI
SMS message
historical capture
research claim
```

不能把“手机号码”“手机”“SIM”“手机号当前使用者”“手机号实名人”“Web 账号本人”视为同一个对象。

---

## 2. Claim list before narrative

本轮能够达到证据门槛的最小 claims：

1. **2001 前后，手机号码已经与 QQ 等互联网服务发生付费/绑定关系。**
2. **2005 年，中文网游明确提供手机绑定和短信指令式账号/角色保护。**
3. **手机绑定至少跨越 Web/客户端、平台账号数据库、电信网络和短信/计费通道，不是一个网页字段。**
4. **2013 年 9 月 1 日起，中国电话用户真实身份信息登记有明确制度规则。**
5. **电信实名关系不能自动推出第三方互联网账号已经完成同等身份核验。**
6. **2014 年已有同期用户案例证明：注销并重新放出的手机号码，可以继续碰到前任用户未清理的支付宝、淘宝、银行通知等绑定。**
7. **因此 `current number holder != original account owner` 必须成为旧网账号研究的硬状态边界。**
8. **公开 Web archive 最容易保存帮助页/绑定表单，最难保存真实 SMS transaction、账号私有状态和运营商内部号码生命周期。**

本轮没有足够证据写成：

- “手机绑定在 2001 年已经普及”；
- “手机验证码让账号更安全”；
- “2014 年二次号码问题非常普遍”；
- “Wayback 没有保存早期 QQ 手机绑定页”。

这些都需要更多规模数据或 verified capture。

---

## 3. 互联网前史边界：移动号码早于大众 Web，但本仓不无限前移

1987 年广州已经开通 TACS 模拟蜂窝移动电话系统，1993 年嘉兴开通数字移动电话网，1995 年多个省市建设 GSM，1996 年实现全国漫游；这些都是理解“手机号码先作为电信地址存在”的必要前史。

Source:
- 中国经济网，《藏区牧民用上移动电话》，2008-11-10: https://www.ce.cn/cysc/ztpd/08/txsh/ly/200811/10/t20081110_17327366.shtml
- 中国经济网，《农村信息网开通》，2008-11-10: https://www.ce.cn/cysc/ztpd/08/txsh/ly/200811/10/t20081110_17327144.shtml

**Evidence grade:** B/C institutional retrospective chronology.

但这些材料不进入本仓主对象。它们只用于说明：

```text
mobile number exists as telecom address
BEFORE
mobile number becomes Web account credential
```

同样，1994 年中国实现与国际 Internet 全功能连接，也不能被写成“1994 年以后普通人立刻用 Web 管理手机号”。

---

## 4. 2001：QQ“手机捆绑”是一个重要交叉锚点

### 4.1 证据

2006 年重庆商报/新浪关于 QQ 号码被盗诉讼的报道，转述用户刘晓华（网名“发条”）的诉状：

- 他称自己在 **2001 年**使用“手机捆绑”；
- 每月支付 10 元；
- 并用网名注册到一个五位 QQ 号码。

Source:
- https://news.sina.com.cn/c/2006-03-10/02358404178s.shtml

**Grade:** B — 2006 年法律/媒体材料对 2001 交易的近事后重构。

### 4.2 这个来源能证明什么

可以写：

> `By 2001, at least one documented QQ user described using a paid mobile-phone binding path associated with QQ registration/service.`

不能写：

> `2001 年 QQ 用户普遍使用手机绑定。`

也不能从“手机捆绑”四个字反推当年具体是：

- WAP 页面；
- Web 表单；
- 客户端菜单；
- 短信上行；
- 运营商代收费；
- SP 计费；
- 哪个域名/接口。

这些具体技术边仍待原始帮助页、资费说明或历史 capture。

### 4.3 最小状态模型

```text
QQ_ACCOUNT_EXISTS
→ MOBILE_BINDING_OFFER_AVAILABLE
→ USER_SUBMITS/REQUESTS_BINDING
→ OPERATOR/BILLING_PATH_ACCEPTS?
→ PLATFORM_RECORDS_BINDING?
→ FEE_CHARGED?
→ USER_CAN_USE_BOUND_FEATURE?
```

报道只支持其中部分状态，不能自动补齐全过程。

---

## 5. 2005：手机密保把号码变成“账号控制信号”

### 5.1 同期服务证据

2005 年网易“大话密保”功能说明明确写到：

- 手机绑定游戏账号；
- 通过手机短信指令保护游戏角色；
- 可短信锁定/解锁角色；
- 部分操作异常时发送短信通知；
- 当时只在列出的部分省市、移动/联通用户中提供。

Source:
- 叶子猪转载官方说明，2005-08-24: https://xy2.yzz.cn/pa/htmldata/8/10/2005_08/5028_1.shtml

**Grade:** B — 同期官方功能说明镜像。

这份材料尤其适合 METHOD 的 `exists / available / used / popular` 分层：

- `exists`: yes；
- `available`: 只对列出的运营商/地区/服务器条件成立；
- `used`: 本轮尚无可靠用户规模数据；
- `popular`: unknown；
- `caused`: 不能仅凭服务存在证明盗号率因此下降。

### 5.2 身份信号的变化

传统密码验证：

```text
knows secret → account access
```

手机绑定增加了一种外部信号：

```text
controls telecom endpoint → may perform account-control action
```

但必须写成“may”，因为：

```text
SMS generated
≠ SMS delivered
≠ SIM in original user's hands
≠ current holder is historical account creator
≠ lawful account ownership proven
```

这条状态边界在 2014 的二次号码案例中会变得关键。

---

## 6. 关键事务链：一次“绑定手机号”横跨多少系统

旧网页里的一个“绑定成功”提示，背后至少可能跨越：

```text
[Browser / PC client]
        |
        v
[Web / IM / game front end]
        |
        v
[Account service]
        |
        +------> [Binding database]
        |
        +------> [Billing/SP gateway?]
        |
        +------> [SMS gateway]
                         |
                         v
                  [Mobile operator]
                         |
                         v
                    [SIM / handset]
                         |
                         v
                        [person]
```

因此 archive 研究至少要区分：

1. 页面上出现“手机号”字段；
2. 后端是否接受请求；
3. 平台是否真正写入 binding record；
4. 短信是否被网关接受；
5. 运营商是否投递；
6. 当前 SIM 是否收到；
7. 当前持有人是否是原 Web 账号本人；
8. 用户是否完成后续确认。

**`binding form captured != historical binding transaction reproduced`**。

---

## 7. 一个通用 binding state machine

```text
UNBOUND
  |
  | user enters number
  v
NUMBER_SUBMITTED
  |
  | platform normalizes / validates syntax
  v
NUMBER_ACCEPTED
  |
  | maybe challenge / SMS / billing
  v
CHALLENGE_SENT
  |
  v
CHALLENGE_DELIVERED?
  |
  | correct response / operator confirmation
  v
BINDING_CONFIRMED
  |
  v
PHONE_BOUND
  |
  +----> PASSWORD_RECOVERY_ENABLED?
  +----> SMS_ALERT_ENABLED?
  +----> BILLING_ENABLED?
  +----> LOGIN_ENABLED?
```

各平台可以只实现其中部分分支。

研究者不能因为今天某产品用短信验证码，就把这个完整模型倒灌到 2001/2005。

---

## 8. 2010 前后：号码开始成为不能轻易丢掉的长期外部凭证

虽然本仓主对象不是携号转网政策，但 2010 天津/海南试点是理解旧网手机号绑定的重要背景：手机号码已经积累了大量联系人和服务关系，以至于“换运营商必须换号码”成为可见的用户退出成本。

光明日报 2010 年 11 月 24 日解释携号转网时，用“想换 iPhone 4/运营商，却舍不得多年 139 号码”的场景说明号码沉没成本；经济观察网同月采访的用户则描述因为想用联通 3G/iPhone、又要继续保留原号码，现实方案是同时携带两部手机。

Sources:
- https://epaper.gmw.cn/gmrb/html/2010-11/24/nw.D110000gmrb_20101124_2-07.htm
- https://www.eeo.com.cn/2010/1130/187751.shtml

**Grade:** B, contemporaneous media/user material.

对旧网研究的意义是：

> 账号绑定手机号不是一次孤立设置；它开始搭在一个用户希望长期维持的社会地址上。

---

## 9. 2013：电话实名关系增强，但“号码控制权”仍不能等同“Web 账号所有权”

### 9.1 原始法规

工业和信息化部第25号令《电话用户真实身份信息登记规定》自 2013 年 9 月 1 日起施行，明确要求固定电话、移动电话等入网时登记真实身份信息。

Source:
- 工业和信息化部: https://www.miit.gov.cn/zwgk/zcwj/flfg/art/2020/art_07ad6d8e69cd4d5ba8b307b37c1aa093.html

**Grade:** A.

### 9.2 三种身份不得合并

```text
TELECOM_SUBSCRIBER_IDENTITY
≠
CURRENT_SIM_CONTROLLER
≠
WEB_ACCOUNT_OWNER
```

即使电信侧完成实名：

- 家庭成员可能代持/代操作；
- 号码会转让、过户、销号；
- 第三方 Web 服务可能只验证“能否收到短信”；
- 老账号绑定可能早于实名制度；
- 号码回收以后，新的实名订户与旧账号创建者可以完全不同。

因此不能把 `phone real-name system` 当成互联网账号实名的替代证据。

---

## 10. 2014：二次放号把最重要的跨系统缺口暴露出来

### 10.1 同期个案

2014 年北京青年报报道：市民赵女士新办理一个手机号以后，收到陌生人的银行卡扣费信息；记者还发现该号码可通过手机验证触及前任用户的支付宝/淘宝相关账号。运营商、支付宝、银行客服均指出，原因涉及号码重新放号，而原持有人未解除第三方绑定。

Source:
- 北京青年报/人民网，2014-09-15: https://politics.people.com.cn/n/2014/0915/c1001-25660141.html

**Grade:** B, contemporaneous user case with multiple service-side confirmations.

### 10.2 Telecom lifecycle

```text
NUMBER_ASSIGNED_TO_A
→ A_ACTIVE
→ A_CANCELS
→ NUMBER_QUARANTINED?
→ NUMBER_RETURNED_TO_POOL
→ NUMBER_ASSIGNED_TO_B
→ B_ACTIVE
```

### 10.3 Internet account lifecycle

```text
ACCOUNT_A_CREATED
→ NUMBER_BOUND_TO_ACCOUNT_A
→ A_STOPS_USING_NUMBER
→ BINDING_NOT_REMOVED
→ ACCOUNT_A_STILL_POINTS_TO_NUMBER
```

两个状态机随后碰撞：

```text
CURRENT_NUMBER_HOLDER = B
WEB_BINDING_OWNER = A
```

于是必须固定：

> **`current number holder != historical web-account owner`**

### 10.4 这是 identity collision，不只是“安全新闻”

本仓不把个案做成猎奇。

它的考古价值在于证明：

- 电信数据库有自己的对象生命周期；
- Web 平台绑定表有自己的生命周期；
- 一个系统结束关系，不会自动触发另一个系统删除状态；
- 研究者如果只看到 Web 数据库里“phone=138…”这一字段，根本不能知道 2014 年此刻 SIM 归谁。

---

## 11. 二次号码状态模型

```text
T0: number belongs to person A
T1: A binds number to Web account A
T2: A cancels telecom service
T3: telecom marks number inactive
T4: third-party binding remains
T5: telecom reissues number to person B
T6: B receives SMS / recovery challenge sent to same number
T7: Web platform may infer "phone possession"
```

每一步都要分别找证据。

尤其不能写：

```text
A cancelled number
→ therefore A account was unbound
```

也不能写：

```text
B received OTP
→ therefore B owns historical account
```

---

## 12. 账号恢复状态机

```text
RECOVERY_REQUEST
→ ACCOUNT_IDENTIFIER_RESOLVED
→ BOUND_PHONE_LOOKED_UP
→ OTP_GENERATED
→ SMS_GATEWAY_ACCEPTED
→ OPERATOR_ROUTED
→ SIM_RECEIVED
→ HUMAN_READ_CODE
→ CODE_SUBMITTED
→ CODE_VALIDATED
→ RECOVERY_AUTHORIZED
→ ACCOUNT_CREDENTIAL_CHANGED
```

Archive 可能只能看到：

- “找回密码”页面；
- “发送验证码”按钮；
- 帮助文档。

它通常看不到：

- 当年的账号数据库；
- 绑定手机号；
- OTP；
- SMS 投递日志；
- SIM 实际持有人；
- 用户是否完成修改。

所以必须坚持：

> **`historical recovery page capture != historical recovery transaction evidence`**。

---

## 13. 页面层与事务层必须分离

建议以后遇到手机绑定页面时，用以下字段记录：

```yaml
page:
  original_url:
  capture_url:
  capture_datetime:
  charset:
  browser_assumption:
  login_required:
  form_fields:
  form_action:
  js_dependencies:
  image_dependencies:

binding_claim:
  function_advertised:
  phone_format_expected:
  operator_restriction:
  region_restriction:
  fee_claimed:
  sms_claimed:
  recovery_claimed:

transaction_unknowns:
  backend_endpoint_verified: false
  database_write_verified: false
  sms_delivery_verified: false
  user_identity_verified: false
```

这样可以避免“页面上有按钮”直接写成“服务完成”。

---

## 14. 手机号字段究竟代表什么：至少六种语义

旧网数据库里一个 `mobile` / `phone` 字段可能表示：

1. 联系方式；
2. 通知目的地；
3. 收费对象；
4. 密保恢复目的地；
5. 登录 identifier；
6. 某种实名/身份辅助信息。

同一个平台在不同年份还可能改变语义。

因此：

> **`phone field exists` 不等于 `phone used for authentication`。**

必须靠当年帮助页、协议、实际事务或用户材料证明具体功能。

---

## 15. 手机号码与 Web 账号的“时间错位”

旧网研究尤其容易犯一种错误：拿一个 2014 年仍然存在的账号状态去解释 2005 年的用户身份。

但真实关系可能是：

```text
2005 account created
2006 phone bound
2009 user changes city
2011 user stops old SIM
2012 number cancelled
2014 number reissued
2014 web account still stores same digits
```

同一串数字在 9 年里可以指向不同的人、不同运营商关系和不同信任语义。

因此任何手机号相关 claim 最少需要：

- **号码字段值的历史时点**；
- **Web binding 的历史时点**；
- **电信订户状态的历史时点**；
- 如果涉及身份，明确说明我们究竟知道的是哪一种状态。

---

## 16. 隐私：这类旧网考古尤其不能“复原得太完整”

手机号本来就是可联系普通个人的现实接口。

因此本仓应比一般页面考古更严格：

- 不在仓库重新公开普通用户完整历史手机号码；
- 截图/转录时对非必要号码做遮蔽；
- 不尝试通过二次放号验证某个旧账号现在是否可登录；
- 不使用验证码、找回密码等方式对历史账号做主动控制测试；
- 不把 archive 中残留的手机号批量索引成“旧网通讯录”；
- 若引用个案，以媒体已经公开、支持 claim 所需的最少信息为限。

**研究账号绑定状态，不等于重新激活历史身份。**

---

## 17. Archive visibility bias

这一题的历史可见性偏差非常强。

### 最容易留下

- 运营商/平台帮助页；
- 手机密保宣传；
- 绑定表单 shell；
- 服务协议；
- 新闻稿；
- “找回密码”公开页面。

### 最难留下

- 登录后的实际绑定号码；
- 私人账号设置页；
- SMS 内容与投递时间；
- 运营商计费/SP 网关日志；
- 号码注销/冻结/回收状态；
- 用户纸质通讯录与换号通知；
- “没收到验证码”这种失败事务；
- 用户后来有没有真的把所有账号解绑。

因此：

> **`archive-visible mobile binding != historical mobile-binding practice`**。

公开 archive 会系统性地高估“产品定义”，低估“事务失败、旧状态残留和普通人的维护劳动”。

---

## 18. Historical capture status in this slice

本轮主动搜索了：

- `QQ 手机绑定 / 手机捆绑 2001`；
- `QQ安全中心 手机绑定 2005`；
- `手机密码保护 2005`；
- `aq.qq.com 手机绑定`；
- 搜索结果中的 Wayback locator 线索。

公开搜索没有返回一份可实际核验的 2001—2005 QQ 手机绑定历史 replay；当前研究链也没有取得同时满足以下字段的 capture：

```text
original_url
capture_datetime
HTTP replay status
historical charset
DOM/form action
JS/subresources
login/session state
SMS/backend behavior
```

因此：

> **M1: NOT ACHIEVED IN THIS SLICE.**

准确说法是：

> `No qualifying historical mobile-binding replay was verified in this slice.`

不能写：

> `Wayback did not preserve it.`

原因可能包括：

- 原页面需要登录；
- 功能主要在 QQ 客户端而不是公共 Web；
- 手机 SP/运营商页面域名尚未确定；
- URL 动态生成；
- robots / archive exclusion；
- 资源存在但搜索定位失败；
- 历史页面已捕获但未被本轮查询发现。

---

## 19. Browser / protocol assumptions

2001—2005 手机绑定不能默认等同今天 HTTPS + AJAX + JSON 的 Web 流程。

待核验的历史条件包括：

- IE 版本；
- GB2312 / GBK；
- QQ 客户端嵌入页面；
- WAP 页面；
- 运营商 SP 计费；
- 短信上行/下行短码；
- iframe / popup；
- session cookie；
- HTTP POST 目标；
- 是否依赖 ActiveX/客户端 IPC；
- 是否由 PC 页面触发、手机短信确认。

没有原始 artifact 前，不应自行选一种现代化流程补全。

---

## 20. 2001—2015 的阶段比较

### 2001—2004：号码进入互联网服务边缘

窄证据说明 QQ 已出现“手机捆绑”路径，但具体原始 UI/协议仍缺。

### 2005—2009：手机绑定变成显式账号安全产品

网游密保等服务把手机短信做成可操作的账号控制通道。

### 2010—2012：长期号码价值越来越可见

携号转网试点说明号码已经积累了足够大的社会/服务沉没成本，用户宁愿双机并用也未必愿意重置联系地址。

### 2013—2015：实名与账号绑定产生新的身份语义冲突

电信侧越来越严格地记录当前订户身份，但 2014 二次号码个案证明：第三方互联网绑定仍可能属于过去的用户。

于是旧网后期出现一个关键悖论：

> **号码对“现在是谁在用”越来越制度化，对“过去哪些账号仍把它当谁”却仍然可能高度历史化。**

---

## 21. Counterexamples

### Counterexample A — 手机号不是唯一互联网身份

QQ 号、用户名、邮箱、本地密码、密保问题、实体令牌等都可以承担账号入口。不能把旧网写成“很早就全面手机号化”。

### Counterexample B — 手机绑定不等于所有人都会绑定

2005 同期功能存在，只证明 available；没有采用率就不能写 popular。

### Counterexample C — 电信实名不等于 Internet account real-name

2013 法规约束电话入网，不自动证明第三方账号的历史创建者身份。

### Counterexample D — 二次放号个案不等于大规模风险率

2014 报道强力证明 mechanism exists，但不能用一个案例推断发生概率。

### Counterexample E — 号码仍然属于同一个人，也可能失去实际可达性

停机、欠费、无信号、SIM 损坏、漫游限制、设备丢失都可能造成：

`subscriber relationship active != user reachable now`。

---

## 22. Hindsight risks

### 风险 1：用今天“短信验证码”的固定想象倒推 2001

早期手机捆绑可能包含 SP 计费、上行短信、QQ 客户端和特定运营商接口，流程待证。

### 风险 2：认为手机绑定天然是“安全升级”

本仓只能证明功能与状态变化；安全效果需要独立攻击/事故数据。

### 风险 3：用实名制度覆盖所有历史号码

2013 前大量号码已有长期历史，后续补登记也经历过渡期。

### 风险 4：把 2014 二次放号解释成用户个人疏忽

个案当然包含旧用户未解绑，但更深的技术事实是：第三方账号状态与电信号码回收没有统一生命周期。

### 风险 5：从 current live help page 复原 historical UI

今天仍在线的帮助内容可以证明当前遗留文本或平台自述，不能证明 2005 年 HTML、DOM、CSS、JS、短信网关与浏览器体验。

---

## 23. Evidence table

| Claim | Source | Type | Grade | Confidence |
|---|---|---|---:|---:|
| 2001 用户描述 QQ 手机捆绑并按月付费 | 2006 重庆商报/新浪诉讼报道 | near-contemporary legal/media reconstruction | B | medium-high |
| 2005 大话密保提供手机绑定、短信锁定/解锁 | 同期官方说明镜像 | contemporaneous service doc | B | high |
| 2010 携号转网试点启动 | 光明日报 / 新华社 | contemporaneous policy/media | A/B | high |
| 2010 有用户因保留旧号码双机并用 | 经济观察网同期采访 | contemporaneous first-person | B | high for case |
| 2013 电话实名规定 9 月 1 日施行 | 工信部第25号令 | primary regulation | A | high |
| 2014 回收号与旧支付宝/淘宝/银行绑定发生冲突 | 北青报/人民网，含多方客服确认 | contemporaneous case | B | high for mechanism |
| 早期 QQ 手机绑定 historical replay | 本轮未验证 | archive gap | — | unknown |

---

## 24. Research unknowns / next capture targets

### P0 — 原始页面定位

优先查找：

- 2001 QQ 手机捆绑资费/注册说明；
- 2002—2004 移动梦网/腾讯合作页；
- 2004—2006 QQ 手机密保页面；
- 2005 网游手机密保原站说明；
- 早期 `aq.qq.com` / `service.qq.com` / 运营商 SP 帮助页。

### P1 — 事务路径

需要确定：

- 是 PC Web 还是 QQ client；
- 谁生成挑战码；
- SMS shortcode；
- 上行还是下行；
- 是否需要运营商代收费；
- 绑定成功状态存在哪里；
- 解绑需要什么旧凭证。

### P2 — 用户证据

寻找 2003—2009 同时代论坛/博客中的：

- 换号后忘记解绑；
- 收不到密保短信；
- 手机丢失后账号恢复；
- 运营商切换导致密保失效；
- 手机号被回收前后的第一人称经历。

### P3 — 规模

本轮没有可靠数据说明：

- QQ 手机绑定采用率；
- 手机密保采用率；
- 二次号码碰撞发生率；
- 每位网民平均绑定多少网站。

这些都必须保持 unknown。

---

## 25. Cross-repo conclusion

`how-people-lived` 关心的是：长期手机号怎样让一个人离开原来的家庭、城市、学校或运营商以后仍能被过去关系找到，以及为什么多年以后换号反而越来越难。

`old-web-archaeology` 在这一题里的任务更窄：

> **证明“号码”怎样从一个电信地址逐渐进入 Web 账号状态机，并保留每一层不能互相替代的证据。**

这次最重要的技术史结论不是“验证码出现了”，而是：

```text
A telecom number has one lifecycle.
A Web account has another lifecycle.
A binding table creates a cross-system edge.
The edge does not necessarily die when either endpoint changes owner/state.
```

因此一个旧网页中的电话号码不是静态个人属性，而是一个**带历史时点、运营商状态、账号状态和潜在所有权漂移的跨系统关系**。

对中文旧网考古来说，这会直接改变我们如何解释：

- 老账号；
- 密码找回；
- 手机绑定；
- 实名；
- 支付；
- 论坛/IM 身份；
- 以及任何 archive 中幸存下来的历史手机号字段。
