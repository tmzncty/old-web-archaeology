# ONLINE_BANKING_REMITTANCE_SECURITY_TOKENS_AND_SETTLEMENT_STATE_GAPS_2004_2008

## 0. Scope

本 note 研究 **2004–2008 中文 Web 上的个人网上银行转账/汇款 artifact，及其与真实资金执行之间的缺口**。

它不是“中国银行史”，也不是“电子支付发展史”。

前互联网的邮政汇兑、银行卡网络和银行后台联网，只在解释旧网页为何具有某些功能时作为必要边界；全球比较、家庭汇款与迁移的生活史主要写入：

- `tmzncty/how-people-lived/topics/remittance-infrastructure-distributed-household-liquidity-and-distance-money-china-1986-2026.zh-CN.md`

本仓主体仍保持约 1995–2015 中文互联网 scope。

---

## 1. 为什么网上银行是特别容易“看起来保存了，其实关键状态全丢了”的旧 Web

一个 2006 年银行帮助页今天仍能显示“转账”“汇款”“7×24 小时”，并不意味着历史交易系统已经复原。

对普通论坛来说，主帖正文可能就是最关键 artifact；对网上银行来说，**公共页面往往只是最外层壳**。

真正决定一笔汇款是否发生的状态通常在：

- 登录 session；
- 客户账户权限；
- 账户余额；
- 收款人信息；
- 单笔/日累计限额；
- USBKey / 数字证书 / 口令卡状态；
- 银行后端授权；
- 跨行清算；
- 收款行入账；
- 接收人后续取现/支付。

这些状态大多：

1. 从未公开；
2. 登录后动态生成；
3. 涉及高度敏感的个人金融信息；
4. 不应为了“考古完整”而通过泄露账户或私人记录补齐。

所以网上银行是一个典型的：

> **public-shell / private-execution asymmetry（公开页面—私人执行不对称）**

---

## 2. Evidence contract

### A — 可用于证明同期功能/规则的原始官方材料

本轮找到的高价值材料包括：

1. 工行 2006-01-24 《调整U盾价格的通告》：
   - U盾用于网络环境身份识别；
   - 可办理 24 小时大额转账、汇款；
   - 2006-02-01 后不同型号价格为 60–76 元。
   - <https://www.icbc.com.cn/icbc/html/gonggao/2006nian/0124/sy_pop_udunjgtzgg0601241.html>

2. 工行 2006 年同期页面介绍个人网上银行：
   - 账户查询、转账、7×24 小时汇款等；
   - 电子银行口令卡面向对支付限额要求不高的普通客户；
   - <https://nz.icbc.com.cn/icbc/html/guanggao/2006nian/1113/sy_banner_global-finance_061113.html>

3. 工行仍在线的历史客户证书帮助页：
   - 静态密码客户对外转账/汇款存在较低限额；
   - 口令卡与 U盾对应不同限额/权限；
   - U盾客户可进行 24 小时大额转账汇款；
   - <https://icbc.com.cn/icbc/html/download/zhengshu/czzn_a1.htm>

4. 2007-08-01 U盾价格调整官方页：
   - U盾价格继续下降；
   - 对外资金转移与安全硬件绑定；
   - 截至 2007 年 6 月底，工行自报个人网上银行客户 3066 万，其中 U盾客户超过 256 万；
   - <https://www.icbc.com.cn/icbc/html/guanggao/2007nian/0801Udunjgqmxt/sy_Udunjgqmxt_070801.htm>

### B — 同期报道 / 用户说明

工行站内 2006 年用户征文页保存了一种同期使用语言：申请 U盾需要带身份证去柜台、填写申请表、付工本费，回家再按说明安装；作者同时抱怨当时汇款查询对柜台业务仍有限制。

- <https://www.icbc.com.cn/icbc/html/guanggao/2006nian/10242/taobao/taobao37.html>

该材料是银行主办活动中的用户投稿，不应当作随机样本；但可用于证明：

> **网上银行的“远程”并不意味着开户、证书领取、安装和所有查询都已经远程化。**

### 重要限定：历史内容 ≠ 历史渲染

以上多条 2006/2007 内容目前仍位于工行 live host。

因此它们可以高强度证明：

- 当时官方如何描述功能、价格、权限；
- 某些 URL/content family 至少被当前站点保留。

但它们**不能单独证明**：

- 2006 年当时的 HTML 与今天完全相同；
- CSS/JS/图片未迁移；
- 当年的浏览器渲染；
- 后台 endpoint 仍是原 endpoint；
- 登录后交易表单的历史 DOM；
- 某一普通用户真的成功汇过款。

记为：

```text
A for dated official claim/content
!=
A for exact historical rendering/runtime
```

---

## 3. 最小 execution state machine

网上汇款不能建模成：

```text
transfer page → success
```

最低应拆成：

```text
public service/help page exists
→ user has eligible bank account
→ user registered for online banking
→ required security method is available
→ client software / certificate / hardware works
→ user authenticates
→ transfer form is rendered
→ beneficiary information entered/selected
→ amount passes fee/limit rules
→ user submits
→ security authorization succeeds
→ sender account is debited
→ bank backend accepts instruction
→ inter/intra-bank clearing/settlement occurs
→ recipient account is credited
→ user/recipient receives confirmation
→ recipient can access/cash out/use funds
→ dispute/reversal/next transfer, if any
```

因此固定：

```text
transfer form exists ≠ user eligible
user eligible ≠ security environment works
form submitted ≠ authorization succeeded
authorized ≠ sender debited
sender debited ≠ recipient credited
recipient credited ≠ recipient can use/cash out
```

---

## 4. 新 archive gaps

### 4.1 form-shell gap

公共帮助页、产品页和入口页可能被 archive 保存，而真正转账表单需要登录后才能生成。

**结论：**

```text
public product page survived ≠ transfer UI survived
```

### 4.2 account-entitlement gap

同一个“个人网上银行”品牌下，客户可能具有不同权限：

- 仅查询；
- 静态密码低限额；
- 动态口令/口令卡；
- U盾/证书；
- 柜面签约状态。

页面写“支持大额汇款”不能外推到每一个注册账号。

### 4.3 security-token/runtime gap

2006 年 U盾不是一个抽象的“安全设置”，而是有价格、USB 物理硬件、数字证书与安装步骤的客户端组件。

于是历史执行依赖：

```text
bank account
+ online-banking registration
+ physical token
+ certificate
+ client installation
+ working computer environment
```

今天保存下来的 HTML 即使打开正常，也不能证明上述运行环境还能复现。

本轮没有足够证据确认所有具体交易页是否依赖某一版 ActiveX、特定 IE 版本或驱动，因此**不得猜测**浏览器/插件细节；需要以后逐 URL、逐时点验证。

### 4.4 beneficiary-state gap

常用收款人、历史收款账号、备注等通常属于登录后的私人可变状态。

archive 不保存它们，既是技术缺失，也是正确的隐私结果。

不得为了恢复“真实转账页面”而重新公开历史普通用户的姓名、账号、手机号或收款关系。

### 4.5 balance-snapshot gap

页面能证明“可汇款”，但某个用户当时有没有足够余额，通常不可知。

所以：

```text
service capability ≠ transaction capacity of a specific user
```

### 4.6 transfer-limit gap

同一时期不同认证方式可能有不同单笔、日累计或总限额。

历史页面若只剩产品介绍而缺失当日限额表，就不能推断某笔金额“理论上一定能汇”。

限额还可能跨版本改变，因此必须记录：

- effective date；
- authentication type；
- channel；
- amount unit；
- whether limit is per transaction / per day / cumulative。

### 4.7 fee-state gap

汇款手续费可能由：

- 本行/跨行；
- 同城/异地；
- 金额；
- 渠道；
- 优惠期；
- 客户等级

共同决定。

某一静态资费页不等于所有历史时点执行价格。

### 4.8 submission / authorization gap

网页提交事件和银行真正接受资金指令是两层。

浏览器可能已经显示“已提交”，但：

- 证书签名失败；
- 密码错误；
- token 未识别；
- 后端超时；
- 限额触发；
- 风控拒绝。

因此不能从前端 capture 推后端成功。

### 4.9 clearing / settlement gap

即使发送行已经扣款，跨行资金到达接收行仍是后端状态。

这是历史 Web archive 最难保存的部分之一，因为它通常只有：

- 私人交易流水；
- 银行内部日志；
- 清算系统记录；
- 私人短信/邮件通知。

### 4.10 recipient-access gap

家庭汇款尤其不能停在“入账”。

接收方可能仍需：

- 去网点；
- 去 ATM；
- 持银行卡；
- 通过身份验证；
- 在农村地区找到受理点。

2005–2007 “农民工银行卡特色服务”之所以专门把城市存款与家乡农村信用社取款相接，就是 recipient-side access 的同时代证据。

生活史来源：

- 2005-12-29 人民银行稿：<https://finance.sina.com.cn/g/20051229/1801472429.shtml>
- 2006-07-05 人民银行答记者问：<https://finance.sina.cn/sa/2006-07-05/detail-ikkntiam0361147.d.html>

### 4.11 notification gap

短信、电话、邮件或 IM 里的“收到没有”通常不会与银行页面一起保存。

因此公共 Web 很难恢复一笔家庭汇款的最后确认步骤。

### 4.12 reversal / dispute gap

错账号、重复转账、不到账、退汇、诈骗、争议等结果往往进入客服、电话、柜台或私人沟通。

公开帮助页可能保存“如何投诉”，但实际争议处理结果仍不可见。

### 4.13 transaction-history retention gap

交易历史本来就不是公共网页资产。

这和论坛帖子不同：

> **交易记录没有被 Web archive 保存，不应默认视为需要修复的 archive failure。**

金融隐私要求我们把“看不到”保留为研究边界。

---

## 5. 2004–2008：为什么 security artifact 本身就是生活基础设施

2006-01-24 工行官方公告给出 U盾价格 60–76 元，并把它定义为用于网上银行身份识别的数字证书，可用于 24 小时大额转账、汇款。

来源：<https://www.icbc.com.cn/icbc/html/gonggao/2006nian/0124/sy_pop_udunjgtzgg0601241.html>

这意味着“从家里转大额钱”在当时至少可能需要：

```text
先去柜台
→ 证明身份/签约
→ 购买或领取安全工具
→ 把物理 USBKey 带回家
→ 在个人电脑配置
→ 登录网银
→ 才能完成某类资金转移
```

因此一个数字服务仍然有**物质依赖链**。

2007 年价格下调页又说明 U盾从此前最高 76、最低 60 元降至 60/58 元；工行同时自报个人网银客户 3066 万、U盾客户 256 万以上。

来源：<https://www.icbc.com.cn/icbc/html/guanggao/2007nian/0801Udunjgqmxt/sy_Udunjgqmxt_070801.htm>

不能从这两个数字推出“其余网银用户都无法转账”，因为还存在口令卡和不同权限；它只能证明：

> **高权限/高安全远程转账在一部分用户那里还绑定着一个需要单独取得的实体认证物。**

这与今天“手机本身同时承担设备、认证和网络终端”的体验不同。

---

## 6. 网上银行并没有把柜台一次性删除

同期用户稿件描述申请 U盾仍需带身份证到工行柜台、填表、支付工本费，然后回家安装；作者还希望未来把柜台汇款的查询也更完整地纳入网银。

来源：<https://www.icbc.com.cn/icbc/html/guanggao/2006nian/10242/taobao/taobao37.html>

该来源不能代表“普通网银用户”的平均体验，但足够证明一个结构事实：

```text
remote execution
can coexist with
physical enrollment + physical security token + branch fallback
```

所以中文旧网考古里不能把“网上银行上线”写成“银行业务从此离开网点”。

更准确的是：

### hybrid banking stack

```text
柜台开户/签约
+ 电话客服
+ Web 查询/转账
+ USBKey/口令卡
+ ATM/农村信用社现金端
```

不同用户使用不同组合。

---

## 7. 2006 的一个关键尺度问题：产品能力与社会分布

人民银行发布的 2006 年《中国支付体系发展报告》同期摘要显示：

- 到 2006 年底，借记卡发行量约 10.8 亿张；
- 银行卡受理商户、POS、ATM 快速增加；
- 网上支付、电话支付和移动支付也在增长。

来源：

- 人民日报海外版/搜狐，2007-04-19：<https://news.sohu.com/20070419/n249535649.shtml>
- 新华网同期报道保存页：<https://news.sohu.com/20070604/n250390241.shtml>

这些宏观量只可用于 denominator/context。

不得推出：

```text
1.08 billion debit cards ≠ 1.08 billion distinct card users
cards issued ≠ active cards
active card ≠ online-banking registration
online-banking registration ≠ transfer permission
transfer permission ≠ actual remittance use
```

旧网页“看起来现代”特别容易让研究者忽略这个分布层。

---

## 8. 一个重要 cross-repo 边界：e-commerce payment ≠ family remittance

2005–2008 中文 Web 上同时快速扩展：

- 网上银行转账；
- B2C 在线支付；
- 支付宝等第三方支付；
- 银行与第三方账户之间的充值/提现/认证。

例如工行 2006 年官方页说明 U盾可与支付宝绑定，用于登录验证、支付、提现和充值：

- <https://www.icbc.com.cn/icbc/html/guanggao/2006nian/0523/images/zfb_060522.html>

但这不能把所有这些行为合并成“汇款”。

至少区分：

```text
merchant payment
escrow payment
bank account transfer
cash remittance
person-to-person family transfer
third-party wallet balance movement
```

它们的：

- 收款主体；
- 争议机制；
- 资金冻结；
- 身份验证；
- 手续费；
- 最终到账状态

都可能不同。

**不要因为页面上都叫“支付/转账”，就把 execution state machine 合并。**

---

## 9. Archive bias：公开页面最容易留下什么，最容易丢什么

### 容易留下

- 产品介绍；
- 新闻稿；
- 资费公告；
- 安全宣传；
- U盾/口令卡说明；
- 登录入口外壳；
- 常见问题；
- 活动页；
- 媒体评测。

### 容易丢失 / 本来就不公开

- 登录后转账表单；
- 某日账户余额；
- 常用收款人；
- 历史交易流水；
- 认证过程；
- 银行内部返回码；
- 清算与入账时间；
- 短信确认；
- 收款端现金取用；
- 客服争议结果。

因此后人特别容易得到一个错误印象：

> “历史网银主要由广告、帮助页和安全警告组成。”

实际上这是**保存结构**，不是当时真实使用结构。

---

## 10. legacy live page 的时间问题

本轮多份 2006/2007 工行官方页面今天仍可访问。

对这种对象必须拆开：

- `content_date`：正文明确标示的同期日期；
- `current_host_state`：今天由哪个 host 提供；
- `historical_rendering`：未知，除非有 dated capture；
- `historical_subresources`：未知，除非逐一核验；
- `historical_backend`：通常不可恢复。

因此使用规则：

```text
current live legacy page
can support dated textual claims
but cannot by itself prove exact historical rendering/runtime
```

这和论坛的 `live legacy rendering` 问题相似，但网上银行更危险，因为用户会自然把一个仍能打开的“老帮助页”误认为旧系统仍可执行。

---

## 11. Privacy stop condition

本领域的 stop condition 必须比普通内容站更严格。

禁止为了证明“真实有人转过账”而：

- 搜索或保存泄露的银行账户数据库；
- 重新公开普通人的历史银行卡号/银行账号；
- 使用泄露的登录凭据进入旧账户；
- 保存历史收款人名单；
- 重发含真实姓名、余额、流水的私人截图；
- 通过个人金融信息交叉识别用户。

优先证据应是：

- 官方同期规则；
- 公开帮助文档；
- 去身份化的同时代用户说明；
- 同期媒体实测；
- 可公开的聚合统计；
- 不含个人账户数据的技术 artifact。

在这个案例里：

> **success-privacy gap 不是需要“修好”的洞，而是研究必须尊重的边界。**

---

## 12. Cross-country comparator boundary

全球前史不写进本仓主体，但可以用来防止把 Web 当成唯一技术起点。

1989 年 *Le Monde* 同期文章已经写到法国银行客户可在家查询账户、办理转账和订购支票簿；BNP Paribas 后来的历史档案还保存 1984 年 Minitel TeleService B 广告，其中可见转账等服务。

来源：

- <https://www.lemonde.fr/archives/article/1989/03/18/le-palais-brongniart-en-direct_4109404_1819218.html>
- <https://histoire.bnpparibas/images/teleservice-b-la-bnp-comme-si-vous-y-etiez/>

这里只用于一条边界说明：

> **remote banking / remote transfer predates the Web.**

法国 Minitel 的家庭生活史、终端分布与使用成本应写在 `how-people-lived`，不把 `old-web-archaeology` 扩成全球 videotex 仓库。

---

## 13. 本轮可复用字段

今后若登记一条中文旧网转账/汇款 artifact，建议至少记录：

```yaml
platform_or_bank:
service_name:
page_url:
content_date:
observed_date:
page_type: [product, help, fee, login-shell, announcement, user-guide, media-test]
public_or_authenticated:
authentication_type:
security_hardware:
registration_requires_branch:
transfer_scope:
limit_type:
fee_basis:
recipient_channel:
known_browser_or_os_requirement:
historical_capture_verified:
historical_runtime_verified:
backend_state_known:
settlement_state_known:
recipient_access_known:
evidence_grade:
privacy_risk:
notes:
```

尤其不要把 `historical_capture_verified` 和 `historical_runtime_verified` 合并。

---

## 14. 当前已证实 / 高概率 / 不知道

### 已证实

- 2006–2007 工行官方公开页面明确提供/宣传个人网上银行转账、7×24 小时汇款等能力；
- U盾是有实体价格的 USBKey/数字证书安全工具，并与较高权限资金转移关联；
- 同期存在不同认证方式与支付/转账限额分层；
- 网银使用可以与柜台注册、实体安全工具、ATM/收款端网点并存；
- 2005–2007 农民工银行卡服务专门处理务工地存款与家乡农村网点取现的接口。

### 高概率，但还需要 artifact 级验证

- 不同历史版本的网银转账页在浏览器、证书控件、驱动和系统要求上存在具体差异；
- 部分交易 UI 与确认页可能曾被用户截图、教程或媒体评测保存；
- 某些公开帮助页可能经过 CMS 搬迁而保留正文、改变外层模板。

### 不知道

- 本轮没有可靠恢复 2004–2008 某普通用户一次完整的 logged-in transfer flow；
- 没有足够证据恢复某一具体日期的历史转账 DOM、JS、TLS/证书运行链；
- 没有验证一笔公开可追踪的“提交 → 扣款 → 入账 → 家庭收款”完整历史链；
- 也不计划通过私人金融记录强行补齐这一缺口。

---

## 15. 这改变了我们对中文旧网的哪一点理解？

网上银行提醒我们：中文旧网不只是一堆“页面”和“社区”。

2000 年代中期已经存在越来越多**流程型 Web（process Web）**：页面的意义不在页面本身，而在它能否触发数据库、认证、支付、清算和线下动作。

因此旧网保存不能只问：

> 页面还在吗？

还要问：

> **页面当年连接的是哪一套状态机？今天保存下来的 artifact 还能证明其中哪一步？**

对网上汇款而言，最谨慎也最有价值的结论是：

> **一个“转账”按钮的历史存在，只证明用户曾被提供一个发起资金移动的界面；它不证明某个账号有权限、不证明认证成功、不证明银行扣款、不证明收款行入账，更不证明远方家庭最后真的拿到了这笔钱。**

这条边界应复用于所有涉及动态账户与现实执行结果的中文旧网研究。

---

## 16. 下一步

优先寻找 2004–2008 的**公开、去身份化、非敏感** execution evidence：

1. 同期媒体对网上汇款全流程的逐步实测；
2. 银行官方操作手册/截图中的确认页状态名称；
3. 安全工具的旧安装包、驱动说明与 browser/OS requirement；
4. 不含真实账户信息的用户教程截图；
5. 同一服务两个以上历史时点的 fee / limit / auth-method 变化。

高价值目标不是拿到一笔私人流水，而是能回答：

> **2006 年一个普通用户坐在家用电脑前，从“打开银行网页”到“远方家人真的可用这笔钱”，中间究竟有多少个今天的 archive 再也看不见的状态？**
