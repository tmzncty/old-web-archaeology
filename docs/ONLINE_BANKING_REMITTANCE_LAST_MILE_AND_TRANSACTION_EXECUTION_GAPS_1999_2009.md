# ONLINE_BANKING_REMITTANCE_LAST_MILE_AND_TRANSACTION_EXECUTION_GAPS_1999_2009

> 适用范围：约 1999–2009 年中文旧网中的个人网上银行、网上转账/汇款、数字证书、USBKey/U盾、安全控件、公开帮助页，以及这些 Web artifact 与银行核心系统、跨行清算、农村取现之间的关系。
>
> 跨仓生活史主文档：
> <https://github.com/tmzncty/how-people-lived/blob/main/topics/money-over-distance-remittance-latency-and-financial-copresence-china-1986-2023.zh-CN.md>
>
> 本说明不写“中国支付史总论”，也不把 2010 年后的移动支付平台扩进来。研究问题只有一个：
>
> **当一个旧网页开始允许用户移动真钱时，今天保存下来的页面究竟能证明交易链的哪一段？**

---

## 0. 与既有文档的边界

本仓已经有：

- `TRANSACTIONAL_TRAVEL_WEB_AND_REVOCABLE_BOOKING_ARTIFACTS_2011_2015.md`：12306 的实名、库存、订单、支付与线下核验；
- `PAGER_GATEWAYS_ONLINE_PAGING_AND_CROSS_NETWORK_DELIVERY_GAPS_1998_2002.md`：Web/Email 到寻呼/SMS 的跨网络投递；
- `CONTACT_STACK_AND_CHANNEL_HANDOFF_1998_2002.md`：不同通信通道之间的 handoff；
- `DOCUMENT_GATED_SHARED_ACCESS_AND_IDENTITY_BINDING_2001_2005.md`：证件、共享终端和身份绑定；
- `JOB_BOARD_ADDRESSABILITY_RESUME_DATABASE_GAPS_AND_APPLICATION_ATTENTION_1999_2009.md`：登录后简历库与申请事件的不可见性。

本篇不重复这些模型。

新增研究单位是：

> **stateful money transaction + authentication environment + clearing backend + recipient last mile**。

其特殊之处在于：

1. 页面不是只在“提交一个申请”，而是在授权不可随意复制的账户状态变化；
2. 浏览器之外还可能有数字证书、USB Key、密码、控件和本地驱动；
3. 同一笔钱可能跨出当前银行进入人民银行支付系统、银联或另一家金融机构；
4. 收款人真正使用这笔钱，仍可能发生在完全离线的农村信用社柜台或 ATM。

因此它值得独立建模。

---

## 1. 研究单位：不要把“转账页面”当成一笔转账

一次 2000s 个人网上银行汇款至少可能包含：

```text
public bank homepage
→ login entry
→ customer entitlement / signed service
→ browser + OS compatibility
→ local security control / client software
→ password / certificate / USBKey
→ authenticated session
→ source account state
→ payee/account input
→ transaction confirmation
→ digital signature / authorization
→ bank application server
→ bank core ledger
→ intrabank or interbank clearing
→ receiving-bank ledger
→ recipient notification
→ recipient branch / ATM / card acceptance
→ cash-out or spending
```

建议以后至少拆以下对象：

```yaml
public_page:
login_endpoint:
auth_method:
local_client_dependency:
source_account:
payee_record:
transaction_request:
authorization_event:
bank_ledger_event:
clearing_event:
receiving_account_event:
recipient_access_event:
cash_out_event:
```

核心边界：

> **archived transfer form ≠ archived transfer**

> **successful login ≠ authorized transfer**

> **authorized transfer ≠ receiving account credited**

> **receiving account credited ≠ recipient obtained usable cash**

---

## 2. 1999：个人网上银行“有转账”应先记录为机构沿革 claim，而不是伪造历史页面

中国建设银行当前仍有官方“发展历程”页面，称：

- 1999 年推出个人网上银行；
- 当时可提供网上查询、转账、代理缴费、挂失等；
- 2003 年个人简易版可以办理账户查询、个人名下转账、代理缴费和网上购物支付；
- 2006 年才面向全国推出个人跨行转账。

当前页面：

<https://forex2.ccb.com/chn/ebank/personal/leftnav/nav2.shtml>

### 证据等级

**B/C 边界：机构 retrospective chronology。**

它能支持窄 claim：

> 建行现在把 1999 年记作个人网银服务推出年份，并称当时具有转账功能。

它不能直接升级为：

> 1999 年某个具体 HTML 页面长这样；

或者：

> 1999 年普通客户已经可以向全国任何银行账户在线汇款。

尤其要保留：

> **current institutional history page ≠ 1999 capture**

---

## 3. 2004：同期材料证明 Web 汇款已经是真实大业务，但仍不能看到单笔 transaction

2004 年 10 月同期材料称，工商银行个人网上银行已提供：

- 账户查询；
- 转账；
- 24 小时跨地区跨行汇款；
- 缴费；
- 其他投资/支付业务。

材料还称：

- 2004 年 1–9 月个人网银用户突破 1000 万；
- 个人汇款交易额约 58 亿元；
- 账户转账交易额约 1101 亿元。

来源：

<https://news.sohu.com/20041015/n222501246.shtml>

### 证据等级

**B：同期媒体 / 银行信息。**

这些数字可以证明：到 2004 年，个人网银已经不只是概念演示。

但 archive 若只留下这篇公开新闻，仍然看不见：

- 哪些具体客户发起；
- 发给谁；
- 当时具体输入界面；
- 是否出现失败；
- 何时入账；
- 收款人是否真正取到钱。

因此：

> **aggregate transaction volume ≠ recoverable transaction history**

这是金融 Web 特别强的历史可见性矛盾：交易越真实、越敏感，越不应该存在于公开 archive。

---

## 4. public shell survival vs private state disappearance

银行旧网最容易幸存的是：

- 首页；
- 产品新闻；
- 功能列表；
- FAQ；
- 安全提醒；
- 客户端下载说明；
- 获奖新闻；
- 费率公告。

最不应该公开幸存的是：

- 用户账户余额；
- 收款账号；
- 转账金额；
- session cookie；
- 数字证书私钥；
- 支付密码；
- 交易流水；
- 收款人身份证明；
- 后台风控结果。

因此需要正式命名：

## private-transaction survival inversion：私人交易存续倒置

> **越接近真正决定“钱有没有移动”的证据，越可能因为登录、隐私、安全和短寿命状态而不在公共 Web archive 中。**

这与静态个人主页不同。

旧网考古不能把“我们只保存到了帮助页”理解为当时服务只是一套帮助页；恰恰可能说明真正运行部分在 archive 的制度性盲区里。

---

## 5. 认证不是网页字段：2005 年 U盾把一块物理硬件塞进 Web transaction

2005 年 10 月新华社同期报道：工商银行把智能客户证书 USBKey 正式命名为“U盾”，并向更广泛的网银客户推广。

其操作逻辑包括：

```text
用户名 + 密码
+ 插入 USB 接口的 U盾
+ 银行端数字证书验证
→ 才允许执行网银账户操作
```

来源：

<https://tech.sina.com.cn/i/2005-10-10/1619736319.shtml>

### 证据等级

**B：新华社同期报道，经新浪保存。**

它证明硬件证书成为当时个人网银安全栈的一部分。

### 新的考古规则

如果今天只 archive 到登录页面里的：

```html
<input name="password">
```

不能推断历史用户只靠密码完成交易。

真正认证环境可能还需要：

- 柜台签约；
- 领取硬件；
- 本地驱动；
- 浏览器控件；
- 数字证书；
- USB 设备；
- 第二个 PIN；
- 银行后台证书状态。

因此：

> **HTML credential fields ≠ complete historical authentication stack**

---

## 6. 2005 招行资料：同一个“网上银行”内部已经存在不同权限层

2005 年搜狐保存的一份来自招商银行网站的功能介绍，明确把个人网银拆成“大众版”和“专业版”。

其中：

- 大众版可做查询、部分账户管理和申请；
- 若要使用专业版，需要本人持有效身份证件和银行卡到网点填写证书申请表并取得授权码；
- 专业版提供向国内不同地区、不同银行账户转账汇款等能力；
- 一些功能还必须先到柜台开通或在专业版软件里开通。

来源：

<https://business.sohu.com/20050510/n225500337.shtml>

### 证据等级

**B：同期页面转存 / 来源标称招行网站。**

### 为什么重要

以后看到：

```text
bank_has_online_banking = true
```

仍然不能直接编码：

```text
user_can_transfer_to_any_bank = true
```

需要至少增加：

```yaml
service_tier:
branch_activation_required:
certificate_required:
client_software_required:
transfer_scope:
```

因此：

> **service brand availability ≠ user entitlement**

以及：

> **online function ≠ online enrollment**

用户完全可能必须先线下跑一次银行，才能在家里获得真正的转账权限。

---

## 7. “网上”并不等于 browser-only：专业版软件、控件和驱动都是历史环境的一部分

2000s 网上银行经常不是今天意义上的“一个标准浏览器网页”。

2005 招行资料已经提到“专业版软件”。

到 2009–2010，建行官方材料更清楚暴露了浏览器兼容性问题：建行后来的官方页面称，个人网银原先的安全控件基于 IE 浏览器设计；2010 年才宣布个人网银全面支持 Firefox，并把这件事表述为突破国内网银只支持 IE 的局限。

来源：

<https://www.ccb.com/cn/ccbtoday/20100208_1265610102.html>

另一个建行 FAQ 说明，在 Vista + IE7 环境下，一度无法直接下载证书，需要先在装有 Windows 2000/XP/2003 与 IE6 的另一台电脑上下载证书，再带到新环境使用。

来源：

<https://ebank.ccb.com/cn/ebank/20091119_1258643335.html>

### 证据等级

**A/B：银行官方操作/新闻页面。**

### 对浏览器考古的意义

如果现代 Chromium 可以打开一个 2006 网银入口，它几乎没有证明历史交易流程可复现。

至少还要问：

```yaml
historical_os:
historical_browser:
security_control:
client_software:
usb_driver:
certificate_store:
admin_permission:
active_session:
```

所以：

> **page renders today ≠ banking workflow executable today**

更强地说：

> **archived HTML may preserve the least important part of the original executable environment.**

---

## 8. 2004–2005 的木马/钓鱼风险说明“运行环境”会改变实际可用性

2004 年同期报道已经出现针对网银账号和密码的木马风险讨论。

来源：

<https://finance.sina.com.cn/g/20040428/0747742192.shtml>

2005 年 U盾推广又明确以假网站、网络钓鱼、木马、密码泄露等为背景。

这说明“一个功能在帮助页写着可用”之外，用户还面对：

- 是否相信当前网站是真的；
- 当前电脑是否安全；
- 公共网吧是否适合做金融操作；
- 是否愿意安装控件；
- 是否把证书放在当前机器上；
- 是否随身携带 U盾。

因此本仓应增加一个字段：

```yaml
historical_execution_trust_context:
```

并坚持：

> **technically executable ≠ subjectively safe enough to execute**

---

## 9. 一个金融 Web transaction 可以从页面直接跨出 Internet，进入全国支付系统

人民银行 2006 年官方材料称：

- 2005 年 6 月大额实时支付系统建成；
- 2006 年 6 月小额支付系统推广到全国；
- 现代化支付系统基本覆盖全国办理支付结算业务的银行业金融机构。

来源：

<https://www.gov.cn/gzdt/2006-07/26/content_345933.htm>

2007 年官方总结进一步称，大额支付系统实现全国银行跨行资金清算零在途，银行卡全国联网通用。

来源：

<https://www.gov.cn/wszb/zhibo134/content_730516.htm>

### 对旧网建模的意义

一个旧网页上写：

```text
24小时跨行汇款
```

其历史执行对象并不是：

```text
browser ↔ browser
```

而是：

```text
browser
→ bank frontend
→ bank core
→ national payment infrastructure
→ receiving bank core
→ recipient access channel
```

后半段没有理由被 Web archive 保存。

因此新增：

## clearing-backend shadow：清算后台阴影

> **公共 Web 可以证明交易入口和公开规则，但真正完成账户状态转移的清算基础设施通常完全处于 Web archive 之外。**

这与 `INTRANET_SHADOW` 类似，但对象不同：不是企业员工的内网，而是金融交易后端。

---

## 10. 收款端甚至可以完全不使用 Internet

农民工银行卡特色服务是这个问题的极好边界案例。

2006 年同期材料明确描述：

```text
工作地商业银行 / 银联卡存入现金
→ 银联 / 银行清算网络
→ 家乡县乡农村信用社柜台
→ 取出现金
```

来源：

<https://finance.sina.com.cn/g/20060215/1000551242.shtml>
<https://finance.sina.com.cn/g/20060530/1054717850.shtml>

2008 年春节前的同期报道又保留一个具体务工者案例：在天津办卡、存入打工收入，回湖南家乡后在当地开通业务的农村信用社柜台取钱。

来源：

<https://news.sina.com.cn/c/2008-01-11/113013241603s.shtml>

### 新硬边界

> **digital transfer ≠ digital recipient experience**

收款端可能只看到：

- 一张银行卡；
- 一个农村信用社柜台；
- 柜员；
- 现金。

所以如果研究者只抓网页，很可能漏掉 transaction 对生活真正最重要的最后一公里。

---

## 11. last-mile invisibility：最后一公里不可见性

建议把金融交易的 archive coverage 拆成：

```yaml
public_information_visible: yes/no
login_page_visible: yes/no
auth_client_visible: yes/no
historical_session_visible: almost_never
transaction_request_visible: almost_never
clearing_state_visible: no
receiver_balance_visible: no
cashout_outlet_documented: sometimes
actual_cashout_visible: rarely
```

这里的核心不是抱怨 Wayback “没抓全”。

很多状态本来就：

- 登录后才出现；
- 含敏感个人数据；
- 由 POST 产生；
- 依赖 cookie/session；
- 只存在几秒；
- 在银行内部系统；
- 在线下柜台完成。

因此：

> **transaction incompleteness is partly structural, not merely an archival accident.**

---

## 12. 公开成功页也不能证明钱最终可用

即使极偶然地拿到某个“交易已提交 / 成功”历史截图，也要问这个 success 表示什么。

至少可能有：

```text
request accepted
authorization passed
source account debited
clearing submitted
receiving bank accepted
receiving account credited
recipient notified
recipient cashed out
```

不同系统把“成功”放在不同阶段。

所以：

> **success label ≠ terminal settlement state**

除非对应历史操作手册或系统说明能定位状态语义，否则不要替页面补完后续。

---

## 13. Web 能保存费率，费率却不等于真实 household cost

例如：

- 2008 农民工银行卡取现费率约 0.8%，有最低/最高；
- 单卡单日取现上限 5000 元；
- 某些地区没有联网受理点，即使愿意多付钱也未必能取。

来源：

<https://news.sina.com.cn/c/2008-01-11/113013241603s.shtml>
<https://business.sohu.com/20080124/n254857102.shtml>

Web artifact 可以很好保存：

```text
fee = 0.8%
cap = 20 yuan
```

但 household cost 还可能包括：

```text
去县城车费
+ 一天中的时间
+ 排队
+ 营业时间
+ 代办风险
+ 不会操作 ATM 的帮助成本
```

因此：

> **published fee ≠ lived transaction cost**

这是旧网页和生活史仓必须交叉的地方。

---

## 14. payment-channel accumulation：支付渠道并不整齐替代

1999–2009 不应该写成：

```text
邮政汇款消失
→ 银行柜台
→ 网银
```

同期实际更可能并存：

```text
邮政汇款
银行柜台
银行卡异地存取
ATM
电话银行
个人网银
网银专业版
银联跨行网络
农村信用社现金取款
```

同一个人甚至可能：

- 工资存银行卡；
- 大额转账去柜台；
- 查余额用网银；
- 给家人送钱仍春节带现金；
- 以后才把 U盾/网银纳入日常。

因此：

> **new channel availability ≠ old channel abandonment**

这和本仓前面对 contact stack 的研究结构相同，但这里必须单独记录**资金权限和结算状态**。

---

## 15. 历史页面中的“转账”标签需要做 capability typing

建议以后遇到旧银行页面，至少给 `transfer_capability` 分类：

```yaml
transfer_capability:
  own_account_internal: true|false|unknown
  same_bank_same_city: true|false|unknown
  same_bank_intercity: true|false|unknown
  other_bank_same_city: true|false|unknown
  other_bank_intercity: true|false|unknown
  scheduled_payment: true|false|unknown
  bill_payment: true|false|unknown
  merchant_payment: true|false|unknown
  foreign_remittance: true|false|unknown
```

理由很简单：

> **“有转账功能”不是一个足够精确的历史 claim。**

2003 建行“个人名下转账”和 2004 工行“跨地区跨行汇款”并不是同一种 capability。

---

## 16. 历史登录环境建议字段

金融旧网特别需要浏览器环境元数据。

建议新增：

```yaml
execution_environment:
  os:
  browser:
  browser_version:
  admin_required:
  security_control:
  active_x_or_plugin:
  client_software:
  digital_certificate:
  certificate_location:
  hardware_token:
  hardware_driver:
  branch_activation_required:
  browser_compatibility_evidence:
```

如果只有现代页面或后来 FAQ，未知项保持 `unknown`。

不要为了“复原完整”而猜。

---

## 17. 与浏览器复原实验 M3 的直接关系

`ROADMAP.md` 的 M3 要求比较现代 Chromium 与 IE5/IE6 级环境。

网银是一个非常有价值、但安全边界很高的实验对象。

推荐的未来实验不是“尝试登录真实银行”，而是：

1. 找历史公开帮助页 / 登录壳的合法 archive capture；
2. 记录当时页面是否要求 ActiveX / 控件 / IE；
3. 在隔离环境只比较静态渲染和控件缺失提示；
4. 不输入任何真实账户、证书或个人信息；
5. 不尝试向真实金融系统发请求。

这样可以证明：

> **historical browser dependency changes interpretation**

而不越过账户安全和隐私边界。

---

## 18. Privacy / security stop condition 在金融旧网中应更严格

本仓已有的隐私规则在金融 artifact 上应强化。

如果 archive 偶然保存：

- 账户号；
- 姓名 + 银行卡号；
- 交易流水；
- 身份证号；
- 证书序列号；
- 手机号；
- 收款人信息；

不要因为“archive 公开可访问”就复制进仓库。

优先只记录：

```yaml
artifact_type: authenticated_financial_page
sensitive_fields_present: true
research_use: structural_only
redistribute_content: false
```

如果无法在不暴露个人金融信息的情况下说明 claim，应停止扩张。

---

## 19. 证据表

| Claim | Evidence | Grade | What it does not prove |
|---|---|---:|---|
| 建行把 1999 记作个人网银推出、含转账 | 当前银行沿革页 | B/C | 1999 原始 UI、普及率 |
| 2004 工行网银含跨地区跨行汇款，业务已有规模 | 同期媒体/银行信息 | B | 单笔交易执行、家庭用途 |
| 2005 U盾作为 USBKey 数字证书推广 | 新华社同期报道 | B | 每个用户都已领取/使用 |
| 2005 招行专业版需线下申请证书，含异地汇款 | 同期资料，来源标称银行网站 | B | 所有版本完全相同 |
| 2004 已出现网银木马/账号密码风险 | 同期中新网报道 | B | 具体用户损失概率 |
| 2005/06 大小额支付系统全国铺开 | 人民银行/政府网 | A/B | 所有个人客户都能跨行汇款 |
| 农民工银行卡连接工作地银行与县乡信用社 | 同期金融报道 | A/B | 每个县乡都有受理点 |
| 2009 建行证书对 Vista/IE7 有特定限制 | 银行官方 FAQ | A | 其他银行/更早版本相同 |
| 2010 建行称此前网银安全控件主要基于 IE | 银行官方新闻 | A/B | 全行业每一年都只支持 IE |

---

## 20. 新的 archive-gap taxonomy

本篇建议正式加入以下 gap：

### 20.1 private-transaction survival inversion

公开说明长存，真实交易状态因敏感性反而系统性不保存。

### 20.2 authentication-environment gap

HTML 幸存，但证书、U盾、驱动、控件、本地软件和柜台签约条件缺失。

### 20.3 clearing-backend shadow

网页请求后的银行核心系统、人民银行支付系统、银联/跨行清算不属于 Web capture。

### 20.4 recipient-last-mile gap

收款账户入账以后，县乡网点、柜台、ATM、排队和实际取现通常不在旧网页里。

### 20.5 entitlement-state gap

页面写着“可转账”，但某历史用户是否已经签约、开通、获得证书、具备该等级权限不可知。

### 20.6 security-trust gap

技术可以执行，不代表当事人愿意在当时那台机器/网吧/网络环境上执行。

---

## 21. 最小 claim 合同

以后写网上银行旧网材料，推荐使用：

```yaml
claim:
  subject: personal_online_banking_service
  date:
  institution:
  public_page_claim:
  transfer_scope:
  enrollment_mode:
  auth_method:
  local_software_dependency:
  browser_dependency:
  backend_dependency:
  recipient_endpoint:
  evidence_grade:
  contemporaneous: true|false
  archived_original_checked: true|false
  execution_observed: true|false
  privacy_risk:
  unknowns: []
```

尤其要让：

```yaml
execution_observed: false
```

成为正常、允许的结果。

---

## 22. 后见之明风险

### 风险 A：把当前网银习惯投射到 2004

今天“浏览器/手机打开银行→转账”的操作直觉，不能替代当时的柜台签约、证书、专业客户端和 IE 控件环境。

### 风险 B：从宣传功能直接推用户能力

`跨行汇款 available` 不等于某个用户账户已经获得该权限。

### 风险 C：把网银和现代支付系统混成一个系统

Web 是前端渠道；支付清算是不同基础设施。

### 风险 D：只看发款端

家庭生活的终点是收款人真正能买东西，而不是网页显示“提交成功”。

### 风险 E：把“电子化”都算作互联网

邮政电子汇兑、银行后台计算机网络、银联系统可以深度数字化，却不要求普通用户自己使用 Web。

---

## 23. 尚未确定之处

### 23.1 1999–2002 原始登录页 capture

目前机构沿革和同期媒体能确认功能存在，但还缺：

- 1999/2000 个人网银原始登录壳；
- URL pattern；
- Content-Type / charset；
- 当时浏览器要求；
- 是否 iframe / Java / ActiveX / 独立客户端 handoff。

### 23.2 一笔失败交易的历史状态链

如果能找到同期用户材料，最好不是“网银真方便”，而是：

```text
登录
→ 输入收款人
→ 提交
→ 失败 / 扣款未到账
→ 客服
→ 最终冲正 / 到账
```

这会比成功宣传页更能说明状态边界。

### 23.3 普通人的机器环境

银行官方说明能告诉我们“支持什么”，但还缺普通人当时：

- 在家用 Windows 98/XP 还是单位电脑；
- 是否能安装控件；
- 是否有管理员权限；
- 是否敢在网吧做网银；
- U盾是否随身带。

### 23.4 收款端现场

最需要和 `how-people-lived` 合作追：

- 某县乡受理点位置；
- 柜台营业时间；
- 排队；
- 身份核验；
- 老人/留守配偶怎样取钱；
- 网络故障时怎么办。

---

## 24. 它改变了我们对“旧网”的哪一点理解

旧网不只是内容空间。

到 2000s 中期，一部分网页已经成为：

> **真实账户状态变化的授权界面。**

但这种 Web 恰恰是传统页面 archive 最难完整保存的对象。

一个银行品牌首页可能活二十年；
一份“网上汇款功能介绍”也可能完整存在；
而某个普通人在 2006 年晚上 10:37 给家里汇 800 元所经历的真正历史过程——

```text
那台 Windows 电脑
那版 IE
那个安全控件
那枚证书 / U盾
那个 session
那次 POST
银行核心账务
跨行清算
家乡信用社柜台
第二天家人拿到的现金
```

几乎没有任何一层会被同一个 Web archive 保存下来。

因此本专题的最重要结论不是“网银改变了汇款”，而是：

> **当 Web 开始控制现实资源时，页面保存与行为保存之间的距离反而可能扩大。**

这应当成为 `old-web-archaeology` 以后研究所有交易型网站时的一条通用警告。
