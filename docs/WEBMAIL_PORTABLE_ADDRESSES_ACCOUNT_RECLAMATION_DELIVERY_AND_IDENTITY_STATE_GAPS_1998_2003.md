# Webmail、可携带个人地址、账号回收与投递状态缺口（1998–2003）

> Scope：1998–2003 中文旧网中的免费 Webmail / 门户邮箱及其与移动通知、即时通信的早期衔接。
>
> 本文不是“中国电子邮件通史”，也不把科研网早期邮件扩进本仓主 scope。1980s–1994 只作为必要前史边界；全球比较写入 `tmzncty/how-people-lived`。

交叉生活史笔记：

- `tmzncty/how-people-lived/topics/personal-addressability-portable-reachability-and-the-right-to-be-unreachable-china-1952-2024.zh-CN.md`

本切片研究的对象不是“某邮箱页面长什么样”，而是：

> **一个旧网页上的邮箱地址，究竟经过多少个私有后台状态，才能真正成为某个人可长期使用的通信身份？**

---

## 1. 为什么 Webmail 是旧网考古的高价值对象

公开 Web 很容易留下：

- 首页；
- 注册入口；
- 登录框；
- 产品广告；
- 邮箱容量说明；
- 帮助页；
- 服务迁移/收费公告。

但真正决定“这个人还能不能收到信”的状态几乎全部在公开 Web 之外：

```text
用户名是否仍可注册
→ 账号是否真的创建
→ 邮箱空间是否成功初始化
→ 密码是否仍有效
→ 发件是否被本地系统接受
→ SMTP/网关是否投递
→ 对端是否接受/退信
→ 用户何时重新登录
→ 是否真的看到
→ 是否回复
→ 账号是否因闲置被回收
→ 域名/服务是否易主
```

因此 Webmail 是典型的 **public shell / private execution system（公开壳—私人执行系统）**。

必须固定：

- `registration page exists ≠ username available`
- `account created ≠ mailbox remains active`
- `send button clicked ≠ message accepted by server`
- `server accepted ≠ recipient mailbox accepted`
- `mailbox accepted ≠ user read`
- `user read ≠ user replied`
- `address printed in an old page ≠ safe or useful to republish today`

---

## 2. 前史边界：1980s 中国已有电子邮件，不等于 1998 年免费 Webmail 的社会条件已经存在

CNNIC 的网络大事记记录，中国科研教育机构在 1980 年代已经通过国际链路交换电子邮件；1994-04-20 NCFC 才通过 64K 国际专线实现 Internet 全功能连接。[1][2]

因此：

```text
科研节点能发国际 E-mail
≠ 中国已经有面向大众的 Webmail
≠ 普通家庭已经有浏览器/拨号账号
≠ 普通人已经有稳定私人邮箱
```

本仓不把 1987 邮件节点写成中文大众 Web 起点，只把它作为技术谱系边界。

到 1997 年 CNNIC 第一次调查时，中国互联网用户仍只有约 62 万，且主要通过拨号上网；1998–2003 免费邮箱的意义恰恰是在一个仍高度有限的联网人群中，让个人第一次较容易取得一个不直接绑定单位局域网或学校主机的数字地址。[3]

---

## 3. 163.net：同一个公开地址体系内部已经存在“账号死亡”

### 3.1 可证实的同时代事实

1999-12-24《南方周末》关于 163.net 电子邮局出售的同期报道提供了几条非常适合状态考古的事实：[4]

- 1998-01-24 飞华向网易洽购大容量邮件系统，初始设计容量约 30 万用户；
- 163 电子邮局开通约 8 个月后登记用户已超过设计容量；
- 1999-06-14 登记用户突破 100 万；
- 1999-10-07 登记用户约 150 万；
- 期间系统多次清理废旧账号，报道明确称“三个月无信件往来的邮箱”会被收回；
- 1999 年服务出售后，Web 收发界面发生变化，邮箱容量从 2MB 增加到 5MB；
- 163.net 电子邮局与 Supercool 免费个人主页、PCICQ 等资产被一并出售。

这组材料是 **B：同期独立媒体报道**，并且包含对原经营者的采访。它不是服务器日志，不能证明每一个具体账号都严格按同一秒表执行回收。

但它足以支持一个重要结论：

> 早期免费 Webmail 的“地址”不是永久财产；服务商可以按照活动状态回收 namespace。

可以称为 **account-reclamation gap（账号回收缺口）**。

### 3.2 `account exists at t1 ≠ same person controls address at t2`

如果研究者在 1999 年论坛里看到：

```text
someone@163.net
```

它只能证明：

> 某页面在那个历史时点把该字符串作为联系方式展示。

它不能自动证明：

- 这个地址当时一定已成功注册；
- 1999 年页面发布数月后仍有效；
- 2000 年仍由同一个人控制；
- 后来重新注册同名地址的人与原作者是同一人；
- 今天向这个地址发信可以验证历史身份。

因此旧网页中的邮箱地址不能被当成稳定的跨时 identity key。

### 3.3 这也是隐私边界，不是鼓励“测试旧邮箱活没活”

本仓不应：

- 批量向历史私人邮箱发送探测邮件；
- 尝试密码找回；
- 根据退信/未退信推断普通人的现状；
- 重新整理大规模旧邮箱地址目录。

“地址的历史连续性无法验证”应当被保留为结论。

---

## 4. 一个非常容易出现的后见之明错误：`163.net` 不应自动等同于后来熟悉的网易 `163.com` 邮箱

1999《南方周末》材料写得很清楚：当时的 `163.net` 电子邮局由广州飞华经营，其邮件系统与网易有技术采购关系；随后 `163.net` 服务与相关资产又出售给深圳新飞网。[4]

2001 年网易自己的官方公告则在另一个企业/产品上下文中宣布推出收费高级邮箱服务，并称网易网站当时有超过 3600 万注册用户，同时保留免费邮箱服务。[5]

因此旧网研究必须把下列对象分开：

```text
163.net 历史电子邮局
网易提供/销售的邮件系统技术
网易门户账号
后来熟悉的 mail.163.com / 163 邮箱品牌
```

相似的数字品牌、技术供应关系和后来的市场记忆，很容易把几条企业/域名谱系压成一条。

本文件把这称为 **brand/domain genealogy hazard（品牌—域名谱系混淆）**。

除非取得更细的公司公告、DNS/WHOIS、历史页面或服务迁移文档，不写：

> “1998 年今天的网易 163 邮箱直接以完全相同账号体系上线。”

---

## 5. 2000–2002：一个网民可能同时有很多邮箱，地址稳定性是后来逐渐形成的

CNNIC 2002-07 发布的第十次《中国互联网络发展状况统计报告》提供了很好的 denominator：[6]

- 截至 2002-06-30，上网用户约 4580 万，只占总人口约 3.6%；
- 人均 E-mail 账号数在 2000 年 1 月曾达到约 4 个；
- 免费 E-mail 账号在 2000 年 7 月达到人均约 3.3 个；
- 到 2002 年，CNNIC 观察到用户逐渐集中到常用的 1–2 个邮箱；
- 受访网民平均每周收到约 6.5 封非垃圾邮件、6.9 封垃圾邮件，发出约 5.3 封；
- CNNIC 将邮件发送量下降的一种可能解释指向手机、短消息、网络寻呼等通信方式的流行。

这说明早期 Webmail 不宜用今天的“一个长期主邮箱”模型反推。

更合理的状态是：

```text
用户在门户 A 注册一个免费邮箱
+ 在门户 B 再注册一个
+ 为某论坛/主页再留一个
+ 有的只使用几次
+ 有的忘密/闲置
+ 有的因规则变更或收费放弃
+ 少数逐渐成为长期主地址
```

于是 archive 中“出现过的邮箱地址数量”可能系统性高估**真正长期维持的个人地址数量**。

这可以称为 **address-survival bias（地址幸存偏差）**。

---

## 6. 2001：免费与收费邮箱并存，不等于免费用户自动迁移

网易 2001-11-15 的官方新闻稿宣布面向个人和企业推出高级收费邮箱，并明确提到线上与线下支付方式，同时说明既有免费邮箱继续提供服务。[5]

这条 **A：平台官方公告** 能证明产品存在和厂商设计，但不能证明：

- 哪个具体免费用户转成收费用户；
- 免费/收费账号是否共享完全相同 backend；
- 每种账号的真实留存率；
- 付费后是否更长期稳定；
- 页面上出现的价格在所有渠道是否完全一致。

对旧 Web 来说，这会产生：

- `plan-version gap`
- `account-entitlement gap`
- `payment-completion gap`
- `free-to-paid migration gap`

Web 产品页只告诉我们“有哪些计划可选择”，不告诉我们一个具体人的账号后来走了哪条路线。

---

## 7. Webmail 与手机/QQ 的衔接：账号开始脱离“坐在电脑前才存在”的状态

1999-04-07 腾讯官方历史公告称，它与深圳联通合作提供“Mobile Email”，可以让移动电话通过短信查询、收发或回复邮件，并在新邮件到来后提供通知。[7]

2000-06-21 腾讯又宣布 Mobile QQ 进入深圳联通 STK 服务，功能包括发送/查询消息、查询好友状态与 QQ 用户信息；无 STK 卡也有命令式使用方式。[8]

这些都是 **A：平台官方功能宣称**。它们不能证明全国普通人实际覆盖，更不能把深圳联通试点直接外推成全国体验。

但对 Webmail archaeology 很重要，因为它说明“邮箱网页”逐渐不再是唯一的可观察入口：

```text
同一邮箱/QQ identity
可能被：
Web 页面访问
+ 手机短信网关通知
+ 移动终端命令访问
+ 后来的客户端/POP/SMTP 访问
```

于是：

> **page capture completeness ≠ service-experience completeness。**

即使完整保存了一个 2000 年 Webmail 首页，也可能完全漏掉同一账号体系的移动通知、短信网关或客户端使用方式。

---

## 8. Webmail execution state machine

建议后续所有旧邮箱案例至少按下列状态机审查：

```text
服务/域名存在
→ 注册页在目标时点可访问
→ 用户名此刻可用
→ 注册请求被接受
→ 账号创建
→ mailbox storage/quota 初始化
→ 用户能完成认证
→ compose/send 页面可使用
→ 本地邮件系统接受发件
→ relay / SMTP 尝试投递
→ 目标域接受或退信
→ 目标邮箱仍有效且未超额
→ 接收者在之后某个时点登录/得到通知
→ 接收者实际阅读
→ 接收者回复
→ 双方地址在下次通信时仍有效
```

长期状态还要继续：

```text
账户有活动
→ 长期未登录/无信件
→ 触发 inactivity rule（若有）
→ suspended / reclaimed / migrated / charged / closed
→ 原地址是否再次开放注册（未知时保持未知）
```

---

## 9. 新增 archive / execution gaps

### 9.1 registration-form version gap

今天找到“注册免费邮箱”的介绍，不等于知道 1999-03、1999-10、2000-02 的字段完全相同。

可能变化：

- 用户名长度；
- 密码规则；
- 密保问题；
- 真实姓名/地区字段；
- 服务协议；
- 验证方式。

### 9.2 username-namespace gap

注册页面存在，不说明一个具体用户名当时可用。

### 9.3 account-entitlement gap

页面允许登录，不说明任何普通访客都有已开通的邮箱、POP/SMTP 或移动功能权限。

### 9.4 quota-state gap

产品页写 2MB/5MB，只能证明公开计划或当时宣传；不能恢复某账户在某天已占用多少空间、是否超额。

### 9.5 authentication / recovery gap

公开 archive 通常不会也不应保存密码、密保答案、恢复邮箱、手机绑定等私人状态。

### 9.6 SMTP / delivery gap

Web 页面显示“发送”，不证明：

```text
本地 MTA 接受
→ 路由成功
→ 对端接受
→ 未被过滤
→ 未进入垃圾箱
```

### 9.7 bounce-state gap

退信往往进入私人收件箱。公开网页通常无法证明某封历史邮件最后是否 bounce。

### 9.8 read / reply gap

邮件到达服务器和人真正读到之间仍有不可见状态。

### 9.9 inactivity-reclamation gap

163.net 同期资料证明存在闲置账号清理，但公开 Web 很难恢复某个具体账号何时满足规则、何时被回收、是否重新放号。[4]

### 9.10 service-ownership transfer gap

服务易主时，公开首页/品牌变化可能保存下来；账号数据库、后台迁移、密码兼容、历史邮件迁移是否逐项成功则通常不可见。

### 9.11 cross-channel notification gap

手机邮件/短信通知/QQ 网关等功能让同一 identity 的执行路径超出 Web 页面；只看 HTTP capture 会低估真实系统。

### 9.12 address-continuity gap

某个地址在两个年份都出现在公开页面里，不能自动证明中间始终由同一人控制。

### 9.13 brand/domain genealogy gap

相似品牌、域名数字和技术供应关系容易被后来叙述压成一个连续服务。必须按 host、operator、date 分开。

---

## 10. 一个更严格的对象模型

不要把“网易/163 邮箱”作为一个不分时期的自然对象。

建议证据至少记录：

```text
service_brand
operator_at_time
host/domain
observed_at
page_url
capture_url (if verified)
account_namespace (if known)
plan/free-paid tier
quota claim
login method
mobile/POP/SMTP adjacency
inactivity rule
ownership/migration event
browser/charset assumption
```

尤其是：

```text
same brand ≠ same host
same host ≠ same operator
same operator ≠ same backend
same email string ≠ same human controller across years
```

---

## 11. 保存偏差：公开帮助页会活下来，真正重要的通信状态不会

### 容易留下

- “免费邮箱”广告；
- 注册数；
- 2MB/5MB 容量；
- 服务升级新闻；
- 登录框截图；
- 门户帮助文档；
- 收费方案；
- 新闻报道中的邮箱联系方式。

### 很难、且很多情况下不应该留下

- 私人邮件正文；
- 收件箱结构；
- 地址簿；
- 密码/密保；
- 真实投递日志；
- bounce 原因；
- read state；
- 登录 IP；
- 账号找回记录；
- 私人转发规则。

因此电子邮件史有非常强的 **privacy-compatible incompleteness（与隐私兼容的不完整性）**：

> 某些关键状态没有进入公开 archive，并不是保存失败，而是通信隐私正常存在的结果。

本仓不以“补齐私人 mailbox”作为研究目标。

---

## 12. 本轮 archive 查证与负结果

本轮通过公开 Web 检索检查了 `163.net`、历史电子邮局、1998–2000 页面与 archive locator 相关线索。

### 已找到并可核验

- 1999《南方周末》同期报道及具体日期、业务状态、账号回收规则；
- 2001 网易官方收费邮箱公告；
- 2002 CNNIC 邮箱账号与互联网普及统计；
- 1999/2000 腾讯官方移动邮件 / Mobile QQ 功能公告。

### 本轮仍未取得

- 一个已经实际打开并确认内容的 1998–2000 `163.net` 注册页 Wayback capture；
- 当时 registration / login 页的原始 HTML/CSS/JS；
- 可复核的历史 charset/header；
- 服务器端注册、回收、投递日志；
- 能证明某一个普通账户从创建到回收的完整公开状态链。

因此本轮**不做**：

- 1998 页面视觉复原；
- “当时一定是 GB2312 / IE4 / 某分辨率”的猜测；
- 登录表单字段补全；
- SMTP/backend 技术实现推断；
- 普通用户邮箱内容恢复。

“Webmail 服务存在且部分规则可证，但生产交互环境无法完整复原”是目前的正式结论。

---

## 13. browser / runtime 条件：目前只能登记未知

1998–2003 邮箱很可能受当时浏览器、JS、Cookie、编码和代理环境影响，但本轮没有历史 capture 可以做旧浏览器验证。

因此：

```text
browser_assumption: unknown / not verified
charset: unknown for the missing production pages
JavaScript dependency: unknown
cookie/session behavior: unknown
POP/SMTP client configuration: partially evidenced at service level only, not reconstructed
```

不能因为同时期许多中文站点使用 GB2312、IE，就把它自动填到这个案例。

---

## 14. 海外比较只作边界，不扩本仓 scope

全球侧，ARPANET 在 1972–1973 已出现网络邮件，并形成 `user@host` 形式；法国 1980 年代 Minitel 的 messaging 也已经让大量用户通过远程数字终端通信。

这些材料说明：

> **“个人数字地址”早于 WWW，中文免费 Webmail 是这条全球谱系进入中国大众互联网的一种本地实现，而不是概念的全球起点。**

完整跨国生活史比较放在 `how-people-lived`，本仓不因此把 scope 前移到 1970s 全球网络史。

---

## 15. 对旧网研究的直接方法增量

过去很多旧网页案例把邮箱地址当成页面 metadata：

```text
作者：某人
联系：someone@example.com
```

本轮之后，应该把它视为**有时间状态的外部服务接口**：

```text
page captured at t1
→ address string observed at t1
→ provider/account lifecycle unknown
→ deliverability at t1 may still be unknown
→ controller at t2 may be unknown
```

这会改变个人主页、BBS 签名、招聘帖、租房帖、网络简历等许多已有案例的处理方式。

尤其需要新增一句默认规则：

> **历史联系方式不是永久身份标识，也不是今天可供研究者探测的 API。**

---

## 16. 已证实 / 高概率 / 不知道

### 已证实

1. 1999 年 `163.net` 是大规模免费电子邮局，并存在按闲置状态清理账号的规则报道。[4]
2. 1999 年服务易主前后，Web 界面和邮箱容量发生变化。[4]
3. 2000–2002 年许多中国网民同时持有多个 E-mail 账号，随后数量下降。[6]
4. 2001 年网易同时提供免费邮箱并推出收费高级邮箱。[5]
5. 1999–2000 年已有平台把电子邮件 / QQ 与移动网络、短信/STK 功能衔接。[7][8]

### 高概率，但本轮不升级为 A 级页面复原

1. 1998–2000 `163.net` 实际存在 Web 注册/登录/收发页面；同期报道明确写到 Web 收发，但本轮没有实际打开历史 capture。
2. 普通用户在服务易主、扩容和清理期间经历过不同页面/账户状态，但具体账户差异无法公开恢复。

### 不知道

1. 任一特定普通历史邮箱是否在某个具体日仍可投递。
2. 被清理的同名账号是否、何时重新开放给其他人。
3. 1998/1999 production 页面的精确 DOM、CSS、JS、charset 与浏览器依赖。
4. 服务出售时每个 mailbox 的后台迁移方式与失败率。
5. 历史邮件是否被某个收件人真正阅读、何时阅读、是否回复。

---

## 17. Sources / provenance

### A — original / institutional / platform

**[A1] CNNIC — 1986–1993 Internet chronology**

https://www3.cnnic.cn/n4/2022/0401/c87-911.html

用途：只作前史边界，证明中国科研网络邮件先于 1994 全功能 Internet。

**[A2] CNNIC — 1994–1996 Internet chronology**

https://www3.cnnic.cn/n4/2022/0401/c87-912.html

用途：固定 1994-04-20 全功能接入边界。

**[A3] CNNIC — 第十次《中国互联网络发展状况统计报告》发布说明，2002-07-22**

https://www3.cnnic.cn/n4/2022/0401/c155-4806.html

用途：2002 用户 denominator、E-mail 账号数、邮件使用量变化。

**[A4] NetEase — “NetEase.com Launches Paid Premium Email Service”, 2001-11-15**

https://ir.netease.com/news-releases/news-release-details/neteasecom-launches-paid-premium-email-service

用途：网易收费高级邮箱、免费邮箱继续存在、线上/线下支付等厂商宣称。

**[A5] Tencent — “Tencent launched mobile email service in cooperation with Shenzhen Unicom”, 1999-04-07**

https://www.tencent.com/en-us/articles/80261.html

用途：移动邮件/短信通知功能的厂商历史公告。只证明提供/宣称，不外推全国采用。

**[A6] Tencent — “Mobile QQ entered into China Unicom's Mobile New Life”, 2000-06-21**

https://www.tencent.com/en-us/articles/80256.html

用途：QQ identity 与移动电话/STK/命令式服务衔接。

### B — contemporary secondary

**[B1] 《南方周末》—《综述：飞华入不敷出卖掉163》，1999-12-24，新浪保存**

https://tech.sina.com.cn/news/internet/1999-12-24/14105.shtml

用途：163.net 运营主体、设计容量、用户规模、闲置账号清理、服务出售、Web 界面/容量变化。

### Comparative boundary only

**Computer History Museum — Networking & The Web timeline**

https://www.computerhistory.org/timeline/networking-the-web/

**Le Monde — “Le phénomène minitel”, 1986-04-12**

https://www.lemonde.fr/archives/article/1986/04/12/le-phenomene-minitel-en-1985-ce-n-etait-qu-un-pari-risque-en-1986-c-est-un-succes-industriel-et-commercial_3115720_1819218.html

不进入中文旧网主 case，只用于避免把 Webmail 的“个人数字地址”误写成 WWW 独创。

---

## 18. 下一步

最高价值后续不是继续搜“免费邮箱市场份额”，而是：

1. 实际定位并打开一个 1998–2000 中文免费邮箱 registration/login historical capture；
2. 记录 original URL、capture datetime、HTTP/replay state、charset、表单字段与子资源缺失；
3. 找第二个独立邮箱服务做同年对照；
4. 检查是否存在明确 inactivity / quota /收费迁移规则；
5. 不登录、不探测普通私人账号，只研究公开页面和服务规则。

真正要恢复的不是私人收件箱，而是：

> **一个 1999 年普通网民写在 BBS 签名里的邮箱地址，为什么当时可以跟着他跨宿舍、跨单位、跨城市；又为什么那个看起来比门牌号更“永久”的字符串，其实也可能在几个月不使用以后从他的人生里消失。**
