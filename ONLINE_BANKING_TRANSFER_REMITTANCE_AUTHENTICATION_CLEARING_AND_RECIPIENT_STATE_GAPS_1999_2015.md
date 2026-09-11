# 网上银行转账、汇款、认证、清算与收款状态差（1999–2015）

## 0. 范围

本 note 只研究约 1999–2015 年中文互联网环境中，与个人网上银行、在线转账、跨行汇划和远距离家庭资金支持直接有关的 Web 接口与后台状态。

它**不是**中国银行业史、支付宝史、移动支付史或整个支付系统史。

1999 年以前的邮政汇兑、银行卡联网与银行柜台，仅作为理解 Web 转账为什么出现、它替代了哪些动作的必要边界；2016 年以后的 App、二维码、亲属卡、医保钱包等只用于说明旧 Web 状态模型后来如何被重新封装，不改变本仓约 1995–2015 中文旧网的主 scope。

核心问题是：

> **旧网页面上出现“转账成功”“网上汇款”“跨行转账”，究竟能证明现实中的钱走到了哪一步？**

最低解释边界：

```text
public Web page
!= authenticated banking session
!= accepted payment instruction
!= interbank clearing
!= recipient account credit
!= recipient's real-world ability to use the funds
```

---

## 1. 为什么网上银行是一个特别困难、也特别适合旧网考古的对象

普通旧网页面希望被公开访问，网银恰恰相反：它最重要的状态从设计上就不应该被公共 crawler 保存。

公开 Web 可能留下：

- 银行门户首页；
- “个人网上银行登录”入口；
- 安全提示；
- 帮助文档；
- 转账业务介绍；
- 手续费/限额说明；
- 浏览器控件说明；
- 反钓鱼公告；
- 同期新闻或用户教程。

真正决定一笔钱是否到达的部分则通常在：

- HTTPS 认证会话；
- 登录后的账户列表；
- 收款人列表；
- U 盾/数字证书/动态口令等安全验证；
- 银行核心系统；
- 跨行清算系统；
- 收款行入账状态；
- 短信/站内回执；
- 后续冲正、退回、撤销；
- 普通个人银行流水。

这些东西既难以归档，很多也**不应该**为了历史研究重新公开。

因此网上银行尤其容易产生一种档案错觉：

> **页面壳保存得越好，越容易误以为交易本身也被保存了。**

---

## 2. 对象模型：不要把“转账”当成一个状态

至少拆成：

```text
physical sender
legal account holder identity
cash / deposit balance
bank account
bank / branch
online-banking enrollment
Web portal / host
login page
browser / device
session
password / credential
certificate / USB token / OTP / security control
payee / recipient
payee name
account number
recipient bank / branch
saved payee record
transfer instruction
amount
fee
transaction limit
bank-side acceptance
same-bank core processing
interbank clearing rail
clearing message
settlement
recipient-bank posting
recipient account credit
transaction reference / receipt
SMS / notification
reversal / refund / failure
cash withdrawal / merchant spending
archive capture
```

### 永久状态差

- `bank account exists != online banking enrolled`
- `online banking enrolled != transfer function activated`
- `login page reachable != user authenticated`
- `user authenticated != transfer-capable credential present`
- `saved payee != payee data still current`
- `recipient name entered != physical person uniquely identified`
- `instruction submitted != bank accepted`
- `bank accepted != clearing completed`
- `clearing completed != recipient bank posted funds`
- `success page != recipient account credited`
- `recipient account credited != recipient noticed`
- `recipient noticed != funds locally usable`
- `same-bank transfer != interbank transfer`
- `real-time rail exists != every bank exposes it to every customer`
- `online-transfer feature exists != user knows it`
- `user knows it != user trusts it`
- `user trusts it != user prefers it over counter / ATM / postal remittance`
- `public help page archived != authenticated transaction path archived`

---

## 3. 与前 Internet 汇款的边界：Web 没有发明“钱先于身体到达”

邮政汇兑、银行汇款、亲友携带和银行卡网络早已允许异地资金流动。本仓不把它们写成旧网对象，但需要保留这一边界，因为否则很容易把网银错误解释成“第一次能远程汇款”。

2001 年中国邮政电子汇兑尤其是一个重要反例：普通人仍可站在实体柜台办理汇款，但后台纸质汇票传递逐渐被电子信息替代，汇款时间已经显著缩短。

对 old-Web archaeology 的启示是：

```text
backend digitization
!=
Web interface
```

反过来也成立：

```text
Web interface
!=
all backend states visible on Web
```

**Evidence / boundary source**

- **B / contemporary report** — 2003 年关于邮政电子汇兑的报道，记录 2001-07-01 对外运行和 2002 年以后的电子替代。  
  https://news.sina.com.cn/c/2003-10-10/1046890772s.shtml

---

## 4. 2005–2007：精确 URL 本身成为金融安全状态的一部分

### Claim 4.1 — 2000s 中期的网银页面不能只按“长得像不像银行”来识别

2006 年多篇同期报道记录假冒工商银行网站通过邮件、近似域名和高度相似的页面诱导用户输入账户与密码。一些报道甚至明确指出，假页面外观与真正个人网上银行页面“几乎一模一样”。

这给旧网考古增加一个永久问题：

```text
visual similarity
!=
provenance
```

一张没有地址栏、证书状态、capture URL 与 original URL 的旧截图，即使视觉上完全像银行页面，也不能独立证明它是历史真站。

**Evidence**

- **B / contemporary press** — 2006-05-20，《新京报》报道假工行网银页面。  
  https://finance.sina.com.cn/xiaofei/consume/20060520/09332583478.shtml
- **B / contemporary press** — 2006-05-23，中国广播网报道。  
  https://news.sina.com.cn/s/2006-05-23/14439003751s.shtml

### Claim 4.2 — 2007 工行官方安全页给出了可定位的 personal Internet banking original URL

工商银行 2007 年官方反钓鱼页面明确要求用户手工输入正确网址，并给出：

```text
portal:
http://www.icbc.com.cn

personal internet banking login:
https://mybank.icbc.com.cn/icbc/perbank/index.jsp
```

同时页面说明个人网银和在线支付页均应以 `https://mybank.icbc.com.cn` 开头，并以 SSL/浏览器安全锁作为当时用户可观察的安全线索之一。

这是一条非常有价值的 A 级历史 Web 线索，因为它提供了：

- 精确 host；
- 精确 path；
- HTTPS；
- 官方同期 provenance；
- 当时银行希望用户检查的浏览器状态。

**Evidence**

- **A / contemporaneous official Web page** — ICBC 2007 安全提示。  
  https://www.icbc.com.cn/icbc/html/guanggao/2007nian/0118/sy_fangfan_070118.htm

### 重要限制

这份官方说明**不能**单独证明：

- 2007 登录页 DOM 长什么样；
- 所有子资源是否来自相同 host；
- 当时必须使用哪一个具体 IE 版本；
- 登录以后转账表单字段；
- U 盾/控件在每类客户上的强制程度；
- 哪些页面被 archive 保存。

“官方给出 URL”与“历史 capture 已核验”是两个不同证据状态。

---

## 5. phishing twin problem：视觉复原尤其危险

2006 年一名用户记录曾直接比较假网银与真网银，并给出真正个人网银 URL：

`https://mybank.icbc.com.cn/icbc/perbank/index.jsp`

同期材料说明假站可以把品牌、布局、输入框甚至“新一代网上银行”字样复刻得非常接近真站。

**Evidence**

- **B / contemporary user observation** — 2006-12，cnBeta 留存。  
  https://www.cnbeta.com.tw/articles/19028.htm

因此未来 reconstruction 必须保留：

```text
historical visual resemblance
!=
historical authenticity
```

任何网银复原如果只有一张无 provenance 的旧截图，都应该降级为 candidate，而不是原件。

---

## 6. 登录页面与“能转账”之间还有一整套安全状态

当前很多银行帮助页仍保留安全控件、证书、U 盾、短信验证码等说明，但本仓不能把今天的帮助文档直接倒推到 2005 或 2007。

一个较好的近历史用户证据来自 2014 年个人博客：作者使用工行网银在线缴纳电费，记录了：

```text
进入 personal Internet banking
→ 输入用户名 / 密码 / 验证码
→ 选择缴费项目
→ 输入家庭电费户号
→ 查询欠费
→ 提交
→ 插入 U 盾
→ 输入 U 盾密码
→ 在硬件上确认
→ 页面显示缴费成功
```

它不是转账案例，但对 2014 年普通个人 Web 银行认证链是很好的 B/T0 观察。

**Evidence**

- **B / T0 contemporaneous user tutorial** — 2014-05-11，个人技术博客。  
  https://www.crifan.org/use_online_back_of_icbc_to_pay_electric_fee/

永久边界：

```text
login password accepted
!=
transaction authorization completed
```

而且：

```text
software / USB token / certificate requirement observed in 2014
!=
proven requirement for 2006
```

历史浏览器、ActiveX、安全控件和 USB 中间件必须按具体时点找证据。

---

## 7. 2010–2011：按钮背后的跨行状态机发生重要变化

### Claim 7.1 — 网上支付跨行清算系统把多个商业银行 Web 前台接到新的公共清算轨道

人民银行资料记录：网上支付跨行清算系统于 2010 年 8 月 30 日上线试运行，2011 年 1 月 24 日完成全国推广；系统采用实时传输及回应机制，支持跨行支付、跨行账户信息查询与在线签约，并可向客户反馈最终处理结果。

**Evidence**

- **A / PBOC** — 网上支付跨行清算服务。  
  https://guiyang.pbc.gov.cn/guiyang/113337/2164373/2197562/index.html
- **B / contemporary Xinhua report** — 2010-08-30 上线。  
  https://news.sina.com.cn/o/2010-08-31/051018043272s.shtml

这说明 old-Web 研究不能只看商业银行页面：

```text
bank Web page
→ bank backend
→ PBOC interbank clearing rail
→ recipient bank
→ recipient account
```

交易网页只是状态机最外层的一扇窗。

### Claim 7.2 — 系统上线并不等于所有用户第一天都可以无条件使用

2010 年同期体验报道记录，不同银行接入、签约和业务开放状态并不一致；有记者在系统上线次日尝试也未成功。

**Evidence**

- **B / contemporary press** — 新民晚报 2010-08-31。  
  https://tech.sina.com.cn/i/2010-08-31/17234606672.shtml
- **B / contemporary press** — 2010-11 对系统业务状态的说明。  
  https://money.sohu.com/20101108/n277225718.shtml

因此：

```text
clearing infrastructure live
!=
bank connected
!=
feature enabled
!=
user signed agreement
!=
user successfully transferred
```

---

## 8. confirmation-page / settlement-state gap

对普通用户而言，“转账成功”页面是最强的心理终点；对历史研究而言，它仍然只是一个前台状态。

至少要区分：

```text
browser displays success
→ bank records accepted transaction
→ clearing message sent
→ recipient bank acknowledges
→ account posting succeeds
→ funds become available
```

可能出现：

- 超时但后台已处理；
- 前台显示已受理但异步失败；
- 收款账号错误；
- 收款行维护；
- 交易被风控挂起；
- 后续冲正/退回；
- 用户关闭页面但银行账本已完成。

因此 archive 中即使真的幸运保存了一张“成功”页面，也不能单独证明某个现实收款人最终拿到钱。

这是本对象最重要的 transaction-state contract。

---

## 9. recipient addressability：Web 表单也在不断压缩“钱该发给谁”的字段

早期银行汇款常要求用户知道：

- 收款人姓名；
- 卡号/账号；
- 收款银行；
- 某些场景下开户行/地区。

到 2010s 后期，“手机号支付”可以把手机号绑定到默认银行账户，让付款人在支持银行之间用手机号发起转账。这一阶段已经接近本仓上界，主要作为 1999–2015 表单演化的后续边界，而不是把旧网研究扩到移动支付时代。

**Evidence / later boundary**

- 泰安银行 2019 业务说明：手机号与账户绑定、跨行支付、双方银行需支持。  
  https://www.taccb.com.cn/taccb/2024-04/05/article_2024040501111456003.html

这个变化提醒旧网复原者：历史表单字段本身就是生活史证据。

```text
postal address
→ bank account + branch
→ bank account with interbank lookup
→ phone-number alias
```

不要只截图“转账”按钮，而忽略一个时期普通用户究竟必须知道多少收款人信息。

---

## 10. 与农民工汇款生活史的交叉：收款端基础设施会改变 Web/银行卡功能的价值

2007 年同期农民工采访说明：在城市拥有银行卡，并不等于回乡后就能方便取现。

袁丽芳看重农民工银行卡特色服务，是因为自己曾携带一年积蓄坐火车返乡时被盗；邱洪春则已经有银行卡，但发卡行在家乡乡镇没有网点，仍要去县城取款。

**Evidence**

- **B / T1 contemporary interview**：  
  https://finance.sina.com.cn/roll/20070212/10291213725.shtml

另一名受访者刘大胜知道特色服务却不采用，因为当时每日取款限额、手续费和自己原有账户安排更不合适。

- **B / T1 contemporary interview**：  
  https://finance.sina.com.cn/roll/20070212/10291213726.shtml

对 old-Web 的意义是：

```text
Web / card function exists at sender side
!=
recipient-side real-world executability
```

一个完美保存的“跨行转账”网页也不能告诉我们农村家人是否有账户、是否知道密码、附近是否有网点、取现是否方便。

---

## 11. archive bias 1：public-shell / authenticated-state asymmetry

这是本专题最核心的保存偏差。

### 容易保存

- 门户首页；
- 网银入口链接；
- 产品宣传；
- 帮助页；
- 安全提示；
- 登录前页面；
- 费率与限额说明；
- 新闻稿。

### 很难/不应公开保存

- 账户余额；
- 收款人姓名与账号；
- 登录后的菜单；
- 单笔金额；
- 银行流水；
- 短信验证码；
- 证书私钥；
- U 盾交互；
- 真实交易回执；
- 家庭之间的资金流。

因此：

> **网银史的“最好档案”在伦理上也不应该是一个普通人的完整真实账户 session。**

研究目标应是恢复 transaction schema、公开帮助和系统边界，而不是追求泄露私人金融资料来获得“完整体验”。

---

## 12. archive bias 2：security-artifact loss

历史网上银行可能依赖：

- 特定浏览器；
- 安全控件；
- ActiveX；
- Java；
- 本地证书；
- USB token 驱动；
- 硬件确认；
- 被当时 TLS/证书链支持、今天已退出的加密环境。

即使 HTML 保存下来：

```text
HTML capture survives
!=
security middleware survives
!=
transaction can be reconstructed
```

而现代浏览器“打不开”也不能自动写成“历史页面坏了”。

需要未来 M3 浏览环境实验时单独验证。

---

## 13. archive bias 3：live-list / backend-data loss

网银页面中的很多“表单元素”并不是静态 HTML：

- 开户行列表；
- 收款人列表；
- 城市/网点；
- 单日限额；
- 手续费；
- 已签约账户；
- 银行支持状态；
- 实时可用余额。

即使 archive 保存了表单壳，也可能没有相应 API、会话和后台数据库。

因此：

```text
select element survives
!=
its historical option set survives
```

这对旧网页“复原”尤其重要，不能用今天的银行列表去填历史下拉框后伪装成原件。

---

## 14. archive bias 4：current-help / historical-interface gap

银行网站经常把旧帮助页迁移、改模板或保留旧日期。

一个今天仍然在线、页眉页脚已经现代化的“2007 安全提示”可以很好地证明当时银行曾发布这些文字，但它**不一定**证明：

- 2007 年用户看到的完整页面布局；
- 当时 CSS/图片资源；
- 当前 URL 就是当时 original URL；
- 页面的后续 footer 没有被 CMS 重渲染。

因此必须把：

```text
historical content with contemporary date
```

与：

```text
verified historical capture of that page
```

分开。

---

## 15. phishing twin problem 对 provenance 的特殊要求

普通门户页如果截图没有 URL，主要损失是站点身份不确定；网银页面如果没有 URL、证书或 provenance，甚至可能把钓鱼页当成官方页。

未来 `evidence.yaml` 对银行类页面应额外优先记录：

- visible original URL；
- HTTPS / HTTP；
- archive replay URL；
- capture datetime；
- redirect chain；
- page title；
- certificate information if source actually preserves it；
- bank official contemporaneous references to the URL；
- whether screenshot includes browser address bar；
- whether source is a phishing-warning article showing a fake page rather than the genuine service。

---

## 16. 当前 archive 核验结果：M1 未达成

本轮已经得到一个来自 2007 工行官方页面的精确历史候选 original URL：

```text
https://mybank.icbc.com.cn/icbc/perbank/index.jsp
```

并继续寻找 2000s–early 2010s 的历史 archive capture。

本轮能够找到 archive locator / snapshot index 线索，也找到 2007 英文个人网银相邻 URL 的历史线索；但实际尝试打开候选 snapshot 时遇到访问失败/限流与超时，**没有取得一份可以同时核验以下字段的 capture**：

- exact original URL；
- capture URL；
- capture datetime；
- replay / HTTP state；
- charset / Content-Type；
- DOM；
- form action / interaction endpoint；
- subresources；
- 第二历史时点。

因此严格记录：

> **M1 verified historical Chinese online-banking transfer capture: NOT ACHIEVED IN THIS SLICE.**

这不等于“Wayback 没保存”，也不等于“历史页面不存在”。

当前只能说：

- 精确 historical original URL 候选已有强同期官方来源；
- archive locator 存在；
- 本轮未能把 locator 提升为 verified capture。

后续若访问条件恢复，应继续从这个 exact URL 及其相邻 path 进入，而不是猜域名。

---

## 17. 浏览器 / 编码 / 插件状态：当前明确 UNKNOWN

本轮不能因为 2007 官方页提到 IE 收藏夹、安全锁，就自动写：

- “必须 IE6”；
- “必须 ActiveX”；
- “页面是 GB2312”；
- “必须某版 U 盾驱动”；
- “登录表单使用某种 JS”；
- “转账页是 frameset / table layout”。

这些都需要 historical capture、当时用户手册或软件包证据。

当前可以说的只有：

- 2007 官方安全提示使用 IE 地址栏/安全锁语境；
- 2014 用户教程实际观察到 U 盾硬件确认；
- 不同年代与客户类型的认证栈仍待细分。

---

## 18. 与后来的移动支付/家庭代付的边界

2018 年微信亲属卡、2019 以后手机号支付、2020s 手机银行和医保钱包说明，旧 Web 上已经存在的对象后来被重新组合：

- recipient identifier 变短；
- authentication 从 PC 浏览器迁移到手机设备、生物识别和 App；
- family relation 本身进入授权模型；
- general cash transfer 与 bounded-purpose spending 分开。

但这些内容主要属于 `how-people-lived` 的跨时期生活史，本仓只保留它们作为边界，不把 `old-web-archaeology` 扩成 2020s 金融 App 史。

---

## 19. 已证实 / 高概率 / 不知道

### 已证实

- 2006 年存在大量同期假冒银行网页报道，假页可以高度模仿真页；
- 2007 工行官方安全页明确公布个人网银登录 URL 为 `https://mybank.icbc.com.cn/icbc/perbank/index.jsp`；
- 工行同期要求用户检查 HTTPS、正确域名和浏览器安全锁；
- 2010-08-30 人民银行网上支付跨行清算系统上线试运行，2011-01-24 完成全国推广；
- 该系统支持实时传输/回应、跨行支付、账户信息查询和在线签约；
- 2014 至少有普通用户留下使用工行 Web 网银、U 盾完成在线支付的同时代操作记录；
- 发送端网银能力不等于收款端现实取现/使用能力，2007 农民工采访直接展示了这一差异。

### 高概率但需更强原始证据

- 2000s 中期不同客户的网银转账权限受不同安全认证方式影响；
- 许多历史 authenticated 页面从未被公共 Web archive 保存；
- 动态收款行列表、账户列表和交易结果比公开帮助页更容易丢失。

这些推断与系统设计高度一致，但具体站点/年份仍需逐页验证。

### 仍不知道

- 2005、2007、2010 各历史时点工行个人网银登录页的 exact DOM / charset / CSS / JS；
- 早期转账表单的字段、action 与前后页面路径；
- 不同用户类型在各年份的 U 盾/口令卡/证书强制规则；
- archive 是否保存过可公开研究且不含私人信息的 post-login demo / training transaction；
- 不同银行之间的浏览器要求如何分化；
- authenticated Web 会话在 Internet Archive / Common Crawl 中系统性缺失到什么程度。

---

## 20. 下一步

优先顺序：

1. 重试 exact ICBC URL 的 Wayback / Memento / Common Crawl 历史时点；
2. 找 2005–2010 银行官方《个人网上银行使用指南》、安装包、U 盾说明和 PDF；
3. 寻找银行公开 demo / 操作演示，而不是私人真实账户 capture；
4. 比较至少两家银行同年登录和转账字段，避免把工行当全行业；
5. 建立 `authentication_state`、`instruction_state`、`clearing_state`、`recipient_state` 字段；
6. 若取得两个可打开历史时点，再按 METHOD 进入 M1 capture 级分析；
7. M3 浏览器实验中只用合法公开 demo 或无私人信息的历史页面，不尝试恢复真实个人交易。

---

## 21. 这个专题对旧网史的意义

网银把中文旧网考古推到一个很重要的边界：

> **最改变普通生活的网页，不一定是最适合被公共档案完整保存的网页。**

论坛、博客、门户频道希望陌生人阅读；网银最有价值的页面恰恰要求“只有这个账户持有人在这一分钟能看见”。

所以二十年以后，我们可能保存了登录按钮、安全提示和“足不出户转账”的广告，却几乎永远看不到那笔真正让一个在广州打工的人把钱送回江西家庭的交易。

这不是档案工作单纯失败。

它是对象本身的结构：

```text
public Web explains the capability;
private authenticated systems execute the life event.
```

因此恢复中文旧网不能只问“这个页面长什么样”，还要问：

> **页面背后有哪些不可见状态，才让这一个按钮最后真的变成了另一座城市里可以使用的钱？**
