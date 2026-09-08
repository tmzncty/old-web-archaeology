# PASSWORD_LOGIN_RECOVERY_QUESTION_EMAIL_SMS_SESSION_AND_ACCOUNT_CONTROL_STATE_GAPS_1998_2015

## 0. Scope

本研究包只处理 **约 1998—2015 中文旧 Web / IM / 网游环境中的密码登录、密码保护、找回问题、恢复邮箱、手机绑定、验证码、session 与“账号真正控制权”之间的状态缺口**。

它不是：

- 中国密码学史；
- 计算机安全技术通史；
- 2015 年以后 App / passkey 全史；
- 所有账号盗窃案件的犯罪史；
- 教普通用户如何设置密码的安全指南。

长期生活后果主要写入 companion：

`tmzncty/how-people-lived/topics/PASSWORD_ACCOUNT_RECOVERY_AND_AUTHENTICATION_MAINTENANCE_1995_2026.md`

本仓真正要回答的是：

> **当一个旧网页出现“用户名 / 密码 / 忘记密码 / 密码保护 / 绑定手机 / 找回密码”时，我们究竟能证明哪一层状态；为什么保存了登录页，并不等于保存了当年的身份验证系统，更不等于能够证明某个历史用户当时真正控制账号。**

---

## 1. Research units

按照 `docs/METHOD.md`，本专题必须把以下对象分开：

```text
platform / service
host / site
account identifier
browser login page
PC / IM / game client
password field
password verifier / account database
recovery-question record
recovery email endpoint
mobile binding record
SMS gateway / telecom endpoint
session cookie / token
authenticated account state
user-visible private data
historical capture
research claim
```

这些对象不能压成一个“账号密码”。

尤其必须固定：

```text
login page exists
!= backend authentication survives

password accepted
!= current human is historical account creator

password reset completed
!= historical social/content state restored
```

---

## 2. Claim list before narrative

本轮达到证据门槛的最小 claims：

1. **1990s—2000s 的中文网络服务逐渐把个人账号和秘密口令变成普通用户进入 IM、邮箱、网游等服务的基础接口。**
2. **2004 年网游注册已经使用邮件验证码等外部通道，证明 authentication/recovery 很早就是跨系统事务。**
3. **2005 年网游服务已经同时出现密码、手机绑定、安全卡、软键盘等多种账号保护/恢复机制。**
4. **2006 年普通 QQ 用户个案证明：密码控制权可以直接控制客户关系、个人资料和长期积累的社会网络。**
5. **2006 年大型盗号案件材料证明，木马可从终端窃取账号密码并通过邮件或 HTTP POST 外传；因此“用户设置了密码”不能推出秘密只存在用户脑中。**
6. **2009 年钓鱼案例证明，仿真页面可诱导用户主动把账号/支付凭证提交给错误服务。**
7. **2013—2015 前后，账号体系已越来越依赖邮箱、手机、统一通行证和多种恢复资料；研究必须把各个验证信号拆开。**
8. **公开 Web archive 通常只能保存 login/recovery shell，无法自然保存密码数据库、私有 session、真实 SMS delivery 和历史账号控制状态。**
9. **因此 `archived login form != reproducible historical authentication transaction` 必须成为硬边界。**

本轮没有足够证据写成：

- “2005 年普通中国网民已经普遍使用多因素认证”；
- “某种手机密保一定降低了盗号率”；
- “某个历史 QQ 密保页面已经被 Wayback 完整保存”；
- “知道密码的人就是账号法律/历史所有者”；
- “忘记密码是当时用户退出互联网服务的主要原因”。

---

## 3. 互联网前史边界：password 早于 Web，本仓只保留必要前史

MIT CTSS 在 1961 年已经展示多用户 time-sharing，并被 MIT CSAIL 后来的机构史称为广泛认为最早使用个人账号密码的计算机系统之一。

Source:
- MIT CSAIL, `Fernando "Corby" Corbató (1926-2019)`, 2019-07-13: https://www.csail.mit.edu/news/fernando-corby-corbato-1926-2019

**Grade:** B/C institutional retrospective history.

这条前史只用于建立概念边界：

```text
shared computer
→ separate user account
→ personal password
```

远早于中文大众 Web。

中国 1994 年正式全功能接入全球 Internet 以前已有科研网络、电子邮件和计算机账号环境；但本仓不能因此写成“1994 前普通中国家庭已经生活在密码社会”。

`old-web-archaeology` 的主对象仍保持约 1995—2015 中文旧网。

---

## 4. 一次登录到底跨越哪些状态

最小登录状态机：

```text
ACCOUNT_EXISTS
→ LOGIN_PAGE_OR_CLIENT_AVAILABLE
→ USER_ENTERS_IDENTIFIER
→ USER_ENTERS_SECRET
→ REQUEST_SUBMITTED
→ REQUEST_REACHES_AUTH_SERVICE
→ ACCOUNT_LOOKUP_SUCCEEDS
→ SECRET_VERIFIER_MATCHES
→ POLICY_CHECKS_PASS
→ SESSION/TOKEN_CREATED
→ SESSION_DELIVERED_TO_CLIENT
→ CLIENT_STORES_SESSION
→ PROTECTED_RESOURCE_REQUESTED
→ SESSION_ACCEPTED
→ PRIVATE_RESOURCE_RENDERED
```

因此以下等式全部错误：

```text
password field rendered = account exists
HTTP 200 = login succeeded
login POST returned = password accepted
cookie exists = authenticated session
authenticated session = historical owner identity proven
private page screenshot = password itself recovered
```

### 4.1 archive 能保存什么

一个正常 archive capture 最有可能保存：

- 登录页 HTML；
- 用户名/密码 `<input>`；
- form action；
- CSS / image；
- 帮助链接；
- JS validation；
- 静态“忘记密码”说明。

它通常不能自然保存：

- 密码哈希/验证数据库；
- 历史账号的真实秘密；
- 当年 session；
- 登录后的个人好友/邮件/游戏资产；
- 手机短信真正投递结果；
- 运营商 SIM 当前持有人；
- 客服人工申诉判断。

所以本专题的旧网复原上限必须比普通静态页面更低。

---

## 5. 2004：邮箱验证码证明 authentication 早就是跨服务事务

2004 年《天堂II》公开测试相关同期材料记录：

- 官网开放公测账号注册；
- 注册后系统通过邮箱发送验证码；
- 注册高峰时邮箱系统繁忙；
- 部分玩家因此无法收到验证码。

Source:
- 新浪游戏，《〈天堂II〉近期公开测试要闻综述》，2004-08-25: https://games.sina.com.cn/newgames/2004/08/082542676.shtml

**Grade:** B — 同期运营材料 / 游戏媒体页面。

### 5.1 最小事务链

```text
GAME_REGISTRATION_FORM
→ ACCOUNT_RECORD_CREATED/PENDING?
→ VERIFICATION_TOKEN_GENERATED
→ EMAIL_MESSAGE_GENERATED
→ MAIL_SYSTEM_ACCEPTS
→ MESSAGE_DELIVERED?
→ USER OPENS MAIL
→ USER SUBMITS TOKEN/LINK
→ TOKEN VALIDATED
→ ACCOUNT ACTIVATED
```

报道能证明“部分玩家未收到邮件验证码”这一可观察后果，但不能单独判断问题发生在：

- token generation；
- SMTP queue；
- destination server；
- spam filter；
- mailbox quota；
- 用户输入错地址。

所以：

**`verification email sent/claimed sent != user received it`**。

---

## 6. 2005：一个密码开始变成多层凭证组合

### 6.1 天堂II安全卡与手机绑定

2005 年新浪游戏关于《天堂II》的同期页面说明，在“安全卡”以前，平台已经推出手机绑定账号服务，并把安全卡称为账号安全的额外一层。

Source:
- 新浪游戏，《天堂II安全卡 双因素保护游戏帐号》，2005-03-11: https://games.sina.com.cn/o/n/2005-03-11/88449.shtml

**Grade:** B — 同期运营/媒体材料。

这可以证明功能存在，不能证明使用率。

### 6.2 热血江湖：手机密码保护、软键盘、账号加锁

2005—2006 的《热血江湖》运营材料记录：

- 2005 年 4 月 29 日安全中心开放；
- 后续提供软键盘注册、手机账号加锁等服务；
- 另有手机密码保护、装备加锁等机制；
- 2006 年账号升级要求重新设置密码、超级密码，并通过邮箱或手机与账号绑定，用于以后找回。

Sources:
- 新浪游戏，《〈热血江湖〉多重措施帮你防盗号》，2005-09-05: https://games.sina.com.cn/o/n/2005-09-05/1603124246.shtml
- 新浪游戏，《热血江湖网通电信一区账号升级启动》，2006-10-30: https://games.sina.com.cn/o/n/2006-10-30/1028173133.shtml
- 新浪游戏，《〈热血江湖〉免费网游绝无外挂》，2006-02-24: https://games.sina.com.cn/o/n/2006-02-24/1835143523.shtml

**Grade:** B — 同期官方/运营稿经新浪游戏保存。

### 6.3 不能把它们压成“MFA”一个词

历史界面中可能同时存在：

```text
LOGIN_PASSWORD
SUPER_PASSWORD
RECOVERY_QUESTION
RECOVERY_ANSWER
REGISTERED_ID_INFO
EMAIL_BINDING
PHONE_BINDING
SMS_COMMAND
SOFT_KEYBOARD
SECURITY_CARD
```

它们的目的不同：

- 登录；
- 改资料；
- 找回；
- 锁定角色；
- 防键盘记录；
- 证明对外部终端的控制。

用今天的 `2FA/MFA` 总称全部历史对象，会丢失实际事务结构。

---

## 7. `account ownership` 不是一个布尔值

旧网研究尤其容易把“账号属于谁”写成简单事实。

但至少存在：

```text
REGISTERED_CREATOR
CURRENT_PASSWORD_KNOWER
CURRENT_SESSION_HOLDER
CURRENT_BOUND_PHONE_HOLDER
CURRENT_BOUND_EMAIL_CONTROLLER
PERSON NAMED IN REGISTRATION DATA
PLATFORM-RECOGNIZED OWNER AFTER APPEAL
LEGAL CLAIMANT
SOCIAL NETWORK'S RECOGNIZED PERSON
```

这些身份可能重合，也可能不重合。

因此固定：

**`knows password != historical creator != lawful owner`**。

这条边界对盗号、账号买卖、二次号码、账号申诉、遗产等研究都重要。

---

## 8. 2006：普通用户已经把 QQ 密码当成工作基础设施的一把钥匙

四川在线/华西都市报 2006 年报道网络营销从业者李先生：

- QQ 用了 7 年；
- 密码长期未变；
- 很多客户通过 QQ 联系；
- 突然登录时系统提示密码错误；
- 盗号者公开要求付费换回密码；
- 腾讯客服表示可以填写网上 QQ 号码申诉表。

Source:
- 新浪转载，《QQ号被盗 索回需付30元》，2006-07-03: https://news.sina.com.cn/c/2006-07-03/06059355251s.shtml

**Grade:** B — 同时代普通用户 + 平台客服回应。

这里可写窄 claim：

> 对这一名受访者，QQ credential loss 直接威胁其客户联系方式连续性。

不能写成：

> 2006 年中国网络营销者普遍依赖 QQ 作为唯一客户系统。

### 8.1 申诉入口本身也不是账号恢复完成

```text
appeal form exists
→ user submits
→ platform receives
→ evidence evaluated
→ claimant accepted/rejected
→ password reset
→ other security fields reset?
→ contacts/content/assets still intact?
```

所以：

**`appeal submitted != ownership adjudicated != full account restoration`**。

---

## 9. 2006：密码可以在用户不知情时离开本机

《法制日报》2006 年关于大型 QQ/Q币盗窃案的报道转述腾讯和警方材料：

- 2006 年 3 月起 QQ 盗号投诉增长；
- 5 月时每天接近 3—4 万投诉；
- 大量木马记录 QQ 号和密码；
- 早期样本通过邮件自动发送账号密码；
- 后续样本改成通过 HTTP POST 把账号密码写到目标服务器文件。

Source:
- 新浪转载《法制日报》，《全国最大规模盗窃Q币案侦破记》，2006-12-31: https://news.sina.com.cn/o/2006-12-31/083510902403s.shtml

**Grade:** B — 同期案件材料。

### 9.1 browser form capture 无法代表终端安全

一个 archive 即使完整保存：

```html
<input type="password">
```

也不能证明当年用户输入秘密时：

- 电脑没有木马；
- 网吧没有键盘记录器；
- 浏览器没有恶意插件；
- DNS/hosts 没被篡改；
- 用户真的在官方站点；
- 密码没有被别的客户端读取。

这也是旧网体验复原和事务复原的根本差异。

---

## 10. 2009：钓鱼页面证明“长得一样”与“制度主体一样”必须分开

大学生肖曦的同期个案中，他通过 QQ 与假客服交互，对方发送仿淘宝链接；他后来才发现域名是 `taobao.con` 而非 `taobao.com`，已经造成 2256 元损失。

Source:
- 凤凰网，《遭“钓鱼”网站骗光生活费 大学生发帖人肉骗子》，2009-10-13: https://news.ifeng.com/society/2/200910/1013_344_1385831.shtml

**Grade:** B — 同时代普通用户个案。

### 10.1 对旧网考古的直接意义

```text
VISUAL_SIMILARITY
!= DOMAIN_IDENTITY
!= BACKEND_IDENTITY
!= PAYMENT_DESTINATION
```

因此复原一个旧登录页时，不能只看：

- logo；
- table layout；
- 输入框；
- CSS。

还必须记录：

- original URL；
- form action；
- redirects；
- iframe；
- external JS；
- HTTPS/HTTP 条件；
- certificate evidence（若时代适用）；
- backend endpoint（若可证明）。

一个漂亮的 reconstruction 若把历史 form action 换成现代本地 mock，必须明确标 `reconstruction`。

---

## 11. 2007—2010：恢复资料逐渐变成“过去的自己留给未来的证明”

账号找回系统常要求用户提供：

- 注册时间；
- 早期密码；
- 密保问题；
- 历史好友；
- 绑定邮箱/手机；
- 充值/购买证据；
- 身份资料。

这产生一个独特的时间结构：

> **用户注册账号那天随手填的字段，可能多年以后突然变成判断“今天这个人是不是昨天那个自己”的证据。**

### 11.1 2009 QQ靓号案例：用户开始主动留下凭证档案

2009 年京华时报/新浪关于 198 个 QQ 靓号被冻结的报道中，收藏者肖承超称自己保存了购买相关证据；平台要求原始购买人提交证明并走申诉程序。

Source:
- 新浪科技，《腾讯暂封198个QQ靓号》，2009-04-14: https://tech.sina.com.cn/i/2009-04-14/07312999311.shtml

**Grade:** B — 同时代特殊用户/平台争议案例。

该用户并不代表普通网民，但适合证明一种机制：

```text
account has enough value
→ user begins archiving purchase/registration evidence
→ recovery becomes documentary practice
```

不能把 198 个靓号收藏者的行为推广成一般用户习惯。

---

## 12. local password 与 server password 必须分开

旧 PC 软件里常有“密码”按钮，但它未必是远端服务器身份验证。

例如 2000s 邮件客户端、压缩软件、聊天记录、个人文件加密，都可能把密码只作为本地应用层门锁。

研究单位必须区分：

```text
LOCAL_UI_PASSWORD
LOCAL_ENCRYPTION_KEY?
LOCAL_CONFIG_GUARD
REMOTE_ACCOUNT_PASSWORD
SERVER-SIDE AUTHENTICATION
```

只看到一个密码框，不能推出存在服务器账号验证。

同理，一些所谓“本地密码保护”如果能通过替换配置文件绕过，它也不能和服务器密码的安全属性等同。

---

## 13. session 是另一个经常被 archive 忽略的账号控制层

用户成功登录以后，后续页面通常不是每一次都重新发送密码，而是使用某种 session 状态。

最小模型：

```text
PASSWORD VERIFIED
→ SESSION_ID/TOKEN CREATED
→ SET-COOKIE / client storage
→ browser sends session
→ server resolves session to account
→ protected page returned
```

因此：

```text
attacker has valid session
```

与：

```text
attacker knows password
```

不是同一个 claim。

历史截图中“已登录的个人中心”也只能证明当时某个浏览器上下文获得过已认证页面，不能从截图直接反推出登录密码或账号所有权。

---

## 14. 手机恢复与本专题 companion 的边界

手机号码进入账号恢复以后，至少需要跨：

```text
WEB ACCOUNT
→ BINDING RECORD
→ SMS GATEWAY
→ MOBILE OPERATOR
→ CURRENT SIM / NUMBER HOLDER
```

这一部分已经在：

`docs/MOBILE_NUMBER_WEB_BINDING_SMS_RECOVERY_REALNAME_AND_RECYCLED_NUMBER_STATE_GAPS_2001_2015.md`

详细建模。

本专题只保留必要交叉结论：

**`phone can receive reset code != phone holder is historical account creator`**。

特别是在号码销号/二次放号以后，两边生命周期可能分叉。

---

## 15. 2013—2015：统一账号与移动绑定让恢复链更长，而不是更简单

到 2010s 前半，旧网与移动互联网的账号体系越来越多地同时存在：

```text
Web username/password
+ unified passport
+ recovery email
+ mobile binding
+ SMS code
+ app/session
+ real-name fields in some domains
```

例如 2013 年武汉大学学生开发的微信“武大助手”类服务，曾要求用户绑定/提交教务系统用户名和密码以代查教务信息。

Source:
- 中国广播网/相关同期报道，《武大学生微信开发“武大助手”》类材料，2013（本轮公开搜索已定位；后续应补一手页面）。

**Grade:** B — 同期媒体对第三方服务操作的描述。

这类对象尤其需要区分：

```text
university credential
→ user gives credential to third-party service
→ third party logs into university system on user's behalf?
```

与标准 OAuth / delegated authorization 完全不同。

没有原始协议/代码证据时，不能把具体后端动作写死。

---

## 16. 2018—2019 作为 scope 外延参照：旧账号的密码风险不会在旧网时代结束时自动终止

本仓主 scope 到约 2015，但为了理解旧网账号遗留状态，保留两条后续 consequence：

### 16.1 2018：半年不用 QQ，账号仍能代表旧人说话

广州白领林先生换工作后已基本不用 QQ，长期没有登录；账号被盗后，旧好友仍把来自该 QQ 的消息理解为他本人，他需要逐个解释。

Source:
- 人民网转载《新快报》，《QQ盗号诈骗 老骗术竟“重出江湖”》，2018-11-28: https://it.people.com.cn/BIG5/n1/2018/1128/c1009-30429175.html

**Grade:** B — 后续 life consequence，不用于扩张本仓时间范围。

### 16.2 2019：跨站密码复用让一个站的泄露进入另一个站

2019 年撞库案件中，攻击者使用外部泄露凭证批量尝试热门 App；抖音遭到千万级外部凭证尝试，上百万账号密码与外部泄露信息吻合。

Source:
- 人民网转载中新网，《黑客“撞库”热门APP盗密码赚百万 撞到抖音栽了》，2019-06-21: https://media.people.com.cn/n1/2019/0621/c14677-31174338.html

**Grade:** B — 后续 consequence。

它说明一个旧网时代形成的密码习惯可以跨平台长期保留：

```text
credential created on old service
→ reused elsewhere
→ old breach/new breach
→ current account compromise
```

---

## 17. Archive state model

### 17.1 页面保存层级

建议对 login/recovery artifact 使用以下层级：

```text
A0 只有搜索结果/locator
A1 登录页主 HTML 可 replay
A2 CSS/image/JS 主要子资源可 replay
A3 form action / recovery links 可解析
A4 对应 help/recovery flow 多页面可 replay
A5 historical transaction endpoint behavior 可观察（极少见）
A6 authenticated historical private state 可合法复核（通常不应追求）
```

M1 案例至少应达到 A1/A2 并有明确 capture datetime；A5/A6 不应作为一般要求。

### 17.2 `capture shell` 与 `transaction` 的边界

```text
ARCHIVED_LOGIN_PAGE
→ proves historical representation of a login UI

ARCHIVED_LOGIN_PAGE
-X-> proves historical password database
-X-> proves one user's password
-X-> proves successful login
-X-> proves recovery SMS arrived
-X-> proves historical account owner identity
```

---

## 18. Browser / encoding / plugin assumptions

1998—2010 的中文登录、密码保护和网游官网可能受以下条件影响：

- IE / document.all；
- ActiveX；
- JavaScript browser sniffing；
- popup；
- frameset；
- Flash；
- GB2312 / GBK；
- 客户端内嵌浏览器；
- HTTPS 支持范围；
- 网吧安全控件；
- 软键盘控件；
- 登录客户端而非 public Web。

因此现代 Chromium 打开一份 archive capture 成功，只能证明现代 replay 能得到某种页面，不证明历史用户当时获得相同 login/recovery experience。

---

## 19. 历史可见性偏差

### 19.1 最容易幸存的

- 帮助中心“忘记密码”文章；
- 注册/登录 shell；
- 媒体防盗号教程；
- 平台安全公告；
- 被盗大案报道；
- 游戏运营的账号保护宣传。

### 19.2 最难幸存的

- 一个普通用户当年的真实密码；
- 密保问题答案；
- 登录后的好友/邮件/资产；
- 找回申诉里提交的个人资料；
- 客服内部审核；
- 短信是否真正送达；
- session cookie；
- 网吧客户端本地环境；
- 用户写在纸本上的密码清单；
- “忘了以后就算了、再也没有回来”的沉默案例。

因此：

**`archive-visible security discourse != ordinary credential practice`**。

安全新闻天然更容易记录出问题的人，而顺利多年使用、从不思考密码的人更难进入历史。

---

## 20. 隐私边界

密码、密保答案、历史手机号、邮箱、真实身份资料本来就是高敏感对象。

本仓原则：

- 不搜集或重新发布仍可用的真实密码；
- 不尝试利用历史泄露数据登录账号；
- 不保存普通人的密保答案；
- 不为“证明恢复流程”而触发真实用户短信；
- 普通个人账号只保留支持 claim 所需的最少公开信息；
- 若 archive 中意外保存私有/敏感数据，不把它重新镜像进仓库。

旧网考古目标是恢复**系统结构**，不是恢复普通人的秘密。

---

## 21. Evidence table

| Claim | Source | Grade | Confidence |
|---|---|---:|---:|
| CTSS 1961 已有个人账号密码 | MIT CSAIL institutional history | B/C | high |
| 2004 天堂II 注册使用邮件验证码且存在未收到情况 | 新浪游戏同期材料 | B | high |
| 2005 天堂II 安全卡、手机绑定已存在 | 同期运营材料 | B | high for exists |
| 2005–06 热血江湖有手机密码保护/超级密码/邮箱手机绑定 | 同期运营材料 | B | high for exists |
| 2006 QQ 被盗影响网络营销客户联系 | 同期普通用户采访 | B | high for case |
| 2006 木马通过邮件/POST 外传 QQ 密码 | 法制日报/警方案件材料 | B | medium-high |
| 2009 钓鱼页面可让普通大学生把交易凭证提交给错误站点 | 同期个案 | B | high for case |
| 2009 高价值账号用户会保存购买/申诉证明 | 特殊收藏用户个案 | B | medium for mechanism |
| archived login page 无法证明 backend/auth transaction | METHOD + systems inference | D | high |

---

## 22. 反例与 alternative explanations

### 22.1 登录失败不一定是密码错

可能是：

- 账号被冻结；
- 服务停机；
- 客户端版本不兼容；
- DNS/网络问题；
- 验证服务器故障；
- 密码真的被改；
- 用户输错用户名；
- 编码/输入法问题。

历史报道里出现“密码错误”只能证明界面这样报告，不能自动定位 root cause。

### 22.2 密保绑定存在不等于用户开启

平台公告只能证明 `exists/available`，不能直接写 `used/popular`。

### 22.3 账号找回不一定靠密码

人工申诉、购买记录、注册资料、好友关系、身份证、邮箱、手机都可能参与。

### 22.4 被盗后社交损失不一定来自密码本身

可能来自木马、session、社工或申诉机制。

### 22.5 历史网页今天仍可打开，不等于历史 DOM/后端仍然相同

今天的帮助中心可能经过 CMS 迁移、HTTPS 包装、模板替换、编码转换和链接重写。

---

## 23. 后见之明风险

1. **不要用今天的 NIST/FIDO 密码规范审判 2005 用户。** 本仓研究当时行为与系统，不做道德化评分。
2. **不要把所有“账号安全”翻译成 MFA。** 当时机制可能完全不同。
3. **不要把 QQ 盗号新闻当成全体中文互联网。** QQ 是高可见平台，有选择偏差。
4. **不要把手机验证写成实名。** `controls number` 与 `legal identity` 不同。
5. **不要把 Wayback locator 当成 verified capture。**
6. **不要把密码表单复原成“成功登录演示”并冒充历史事务。**

---

## 24. Archive work this slice

本轮针对以下对象进行了 historical locator / replay 搜索：

- `service.qq.com` 2004—2007 密码/号码申诉路径；
- `aq.qq.com` 2007—2010 密保/找回路径；
- 同期 QQ “忘记密码 / 密码保护 / 号码申诉”关键词；
- 2004—2006 网游注册、手机绑定、安全卡相关页面。

### 24.1 得到的结果

公开搜索能够定位大量**同期新闻/运营内容**，并出现 `service.qq.com` 作为当年用户回答/媒体指向的找回入口。

但本轮没有取得一份可以按 METHOD 检查以下字段的合格历史 capture：

```text
capture_datetime
original_url
HTTP replay status
Content-Type / charset
DOM
form action
JS / ActiveX / subresources
cookie/session behavior
historical recovery result
```

### 24.2 CDX 限制

本轮尝试直接查询 Internet Archive CDX：

- `service.qq.com/*`, 2004—2007；
- `aq.qq.com/*`, 2007—2010。

当前访问工具因 URL 安全限制拒绝了这些构造查询，不能把这种工具侧失败写成 archive absence。

因此结论严格为：

> **`candidate/locator research performed; verified historical login/recovery replay NOT ACHIEVED IN THIS SLICE.`**

不是：

> `Wayback did not save it.`

### 24.3 M1 状态

**M1: NOT ACHIEVED IN THIS SLICE.**

本专题当前是证据充分的 research package / state-gap note，不是“完整复原的历史登录案例”。

---

## 25. 下一步最值钱的证据

优先级从高到低：

1. 1999—2003 OICQ/QQ 原始帮助页或安装手册中的 password/recovery 说明；
2. 2004—2008 `service.qq.com` / `aq.qq.com` 的 verified capture；
3. 同期登录页的 form action、charset、JS、browser assumption；
4. 早期邮箱“忘记密码”原始帮助页；
5. 2000s 网吧用户关于“记密码/不保存密码/盗号”的同期论坛材料；
6. 同一平台至少两个历史时点，观察 recovery architecture 从问题/邮箱到手机/多工具的变化；
7. 账号申诉结果页面与帮助页之间的状态差异，但避免任何真实个人敏感数据。

---

## 26. 本轮对 old-web 方法的新增结论

这次最重要的不是再补一个 QQ 安全史，而是给旧 Web archaeology 加了一条可以跨很多专题复用的硬规则：

> **一个“登录页”不是一个账号系统。**

真正的历史对象至少包括：

```text
page shell
+ credential submission path
+ authentication service
+ verifier/account database
+ session issuance
+ recovery channels
+ human/customer-service fallback
+ historical user control state
```

archive 往往只保存第一层和一小部分帮助文档。

因此当我们未来研究邮箱、论坛、SNS、网游、银行、校园系统时，都应该把：

**`page survived`**

与：

**`identity transaction survived`**

严格分开。

---

## 27. Cross-repo understanding

这个 old-Web 状态缺口改变 how-people-lived 的地方在于：

普通人得到越来越多远程生活入口以后，并不是只获得“自由”。每个入口还需要一个长期可恢复的身份状态。

旧网帮助页里不起眼的“忘记密码”四个字，其实暴露了一项非常普通又非常长期的数字劳动：

> **让未来的自己还有办法回到过去建立的账号里。**

这项劳动不会随着浏览器关闭而结束；它会穿过换工作、换号码、换电脑、平台改版，甚至穿过十几年的人生阶段。
