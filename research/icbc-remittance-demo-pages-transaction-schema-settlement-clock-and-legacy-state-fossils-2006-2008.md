# ICBC 汇款演示页：交易 schema、清算时钟与 legacy state fossil（2006–2008）

## Scope / 为什么这个案例属于 old-web-archaeology

本仓库不研究一般金融史。本 note 研究一个非常 old-Web 的问题：

> 当 2000s 的银行事务已经进入 Web 后，今天究竟还能恢复什么？

本轮与 `how-people-lived` 的资金传输专题交叉。HPL 讨论普通家庭怎样把工资跨距离送回家；这里专门处理 2006–2008 中国个人网银如何把“汇款”编码成网页字段、身份权限、服务时钟和交易状态。

核心对象是中国工商银行当前仍在线的一组 legacy demonstration pages / rules pages。它们的路径包含 `yanshichengxu`、`dongtaiyanshi` 等演示目录，页面内嵌 2006、2007、2008 的示例日期和交易数据。

**重要 provenance 限制：**

这些是**今天仍在线的官方 legacy demo artifacts**，不是本轮已经核验过 capture timestamp 的 2006/2008 Wayback memento，也不是私人用户真实账户记录。它们非常适合恢复 transaction schema、字段、说明文字和当时产品逻辑；不适合证明某一具体用户真的完成过页面中的示例交易，也不能仅凭嵌入日期断定 HTML 文件在那个日期已经以完全相同形态公开上线。

---

## 1. 新的 artifact 类型：public demo state 可以比 private account state 活得更久

旧网交易系统有一个保存悖论：

- 真正重要的私人交易记录受认证、隐私和数据保留规则保护，几乎不会进入公共 Web archive；
- 银行为了教学而制作的**演示程序**却可能把完整页面结构、字段、示例账号、状态和提示公开在静态目录里；
- 多年以后，真正账户状态消失，演示页反而继续活着。

本轮把这类材料暂定为：

### `transaction-schema fossil / 交易模式化石`

以及更具体的：

### `legacy demo-state fossil / 遗留演示状态化石`

它不是“真实历史交易数据库”的替代物，却能保存：

- 字段名称；
- 字段顺序；
- 状态 vocabulary；
- 收款人数据模型；
- 手续费显示；
- 隐私选项；
- 渠道边界；
- 认证等级与交易限额；
- 跨行结算时钟提示。

这对 M1/M2 以后恢复事务型旧站非常有价值。

---

## 2. Artifact A：2006 示例交易查询页

当前仍可被搜索引擎读取的工行官方页面：

`/icbc/html/download/yanshichengxu/personalbank/icbc/perbank/remit/remitexc_icbc_query_1.htm`

公开标题：`个人网上银行-行内汇款查询`

当前 URL：
https://icbc.com.cn/icbc/html/download/yanshichengxu/personalbank/icbc/perbank/remit/remitexc_icbc_query_1.htm

页面中的示例交易日期为 **2006-06-01 14:33:34**，并展示：

- 指令序号；
- 付款账号；
- 收款人；
- 收款账号；
- 金额；
- “钞汇标志”；
- 手续费；
- 交易日期；
- 交易时间；
- 交易状态；
- 回单 / 详细信息。

示例状态写为：

`支付成功已经清算`

这说明对于当时的网银 UI，用户看到的并不只是“转账成功/失败”布尔值；至少演示逻辑已经把 transaction id、支付动作和“清算”状态作为可见信息。

来源：
- 官方 legacy demo page（当前 live representation）：https://icbc.com.cn/icbc/html/download/yanshichengxu/personalbank/icbc/perbank/remit/remitexc_icbc_query_1.htm

证据等级：**A for schema / B for exact historical runtime**。

原因：官方页面当前真实存在且字段可读；但没有独立 capture timestamp 证明它在 2006-06-01 已以完全相同 HTML 上线。

---

## 3. 一个很重要的渠道边界：online history != all money history

同一页面明确提示：

> 此查询只针对在网上银行办理的转账汇款；柜面、ATM、POS、电话银行、多媒体自助终端等其他途径完成的交易不能在这里查询。

因此：

### `account history != channel-complete history`

至少在这个产品设计里，用户资金事务被不同 access channel 切开。

一个旧网研究者即便完全恢复“网上银行转账历史”页面，也不能据此重建一个人全部汇款活动，因为：

`web channel transaction state`

只是

`counter + ATM + POS + phone + multimedia terminal + web ...`

中的一个切片。

这对 old-Web 方法很重要：**网站数据库从来不必然等于机构的完整事务数据库。**

---

## 4. 隐私不是只有“账号可见/不可见”一个层级

2006 demo 查询页还写明：付款人在转账时可以选择不向收款人显示付款账号；如果选择隐藏，收款人在查询收款信息时看不到付款人账号。

这说明至少 UI 层存在：

### `transaction-level disclosure choice`

研究旧网金融页面时，不能只问“这个页面有没有账号字段”，还要问：

- 字段对谁可见？
- 付款人是否可控制披露？
- 收款人、付款人、银行后台看到的是不是同一 schema？
- 演示页展示的是哪个 actor 的视角？

因此 transaction schema 应增加：

`actor_view = sender | recipient | bank | public-demo`

以及：

`field_visibility_policy`。

---

## 5. Artifact B：收款人名册说明了“汇款地址簿”怎样替代重复输入

官方 legacy page：

https://icbc.com.cn/icbc/html/download/yanshichengxu/personalbank/icbc/perbank/account/account_mypayee_remitfor_acctpers.htm

标题：`个人网上银行-我的收款人`

页面把“我的收款人”直接解释成通讯录：建立后，转账时无需重复输入户名和账号。

更值得注意的是，提示文字说收款人信息可以包括：

- 有账号收款人；
- **无账号收款人**；
- 企业收款人；
- 个人外汇汇款收款人；
- 收款账号也可以属于其他银行。

另一个工行现存业务说明还写得更明确：如果不知道收款人账号，可以输入姓名、证件类型与号码，把款项汇往指定工行网点，由收款人持有效证件取款。

来源：
- legacy “我的收款人”：https://icbc.com.cn/icbc/html/download/yanshichengxu/personalbank/icbc/perbank/account/account_mypayee_remitfor_acctpers.htm
- 工行转账汇款业务说明：https://wap.icbc.com.cn/page/721855141685641260.html

这说明传统汇兑逻辑没有被“账号转账”一次性取代。Web banking 内部仍可容纳：

`person identity + designated outlet`

而不一定是：

`person = bank account number`。

因此建议 OWA 在金融 artifact 中区分 recipient-addressing mode：

- `account-addressed`；
- `identity-addressed`；
- `branch-pickup`；
- `cash-out network`。

这与 HPL 的邮政汇票—银行卡过渡直接相连。

---

## 6. Artifact C：2008 跨行汇款页保存了跨行 transaction schema

官方 legacy demo：

https://www.icbc.com.cn/icbc/html/dongtaiyanshi/personalbank/icbc/perbank/remit/remit_noicbc_pay1_1.htm

搜索引擎当前可以读取一份示例日期为 **2008-03-29** 的跨行汇款状态，字段包括：

- 汇款日期；
- 汇出注册卡（账户）；
- 收款人全称；
- 收款人开户行行别；
- 收款账户开户网点；
- 收款人账号；
- 总金额；
- 手续费；
- 用途；
- 汇款附言。

示例收款行甚至细化到具体网点。

来源：
- 工行 legacy cross-bank demo：https://www.icbc.com.cn/icbc/html/dongtaiyanshi/personalbank/icbc/perbank/remit/remit_noicbc_pay1_1.htm

证据等级：**A for visible schema / B for historical deployment date**。

这对考古特别重要，因为今天“输手机号/选常用收款人”可能让人忘记：2000s 一次跨行汇款可能要求用户明确知道：

`银行行别 + 具体开户网点 + 户名 + 账号`。

资金的“地址”远比一个社交账号或手机号更长、更容易输入错误。

---

## 7. 24 小时网站 ≠ 24 小时跨行清算

这是本轮对 old-Web 最有实质意义的新接口边界之一。

工行 2006 年《个人网上银行交易规则》明确写：个人网上银行对外提供 **7×24 小时**服务，并提供账户转账、个人汇款等功能。

来源：
- 工行 2006-08-23 规则页：https://icbc.com.cn/icbc/html/zhangcheng/wsyh_jygz.htm

但 2008 跨行汇款 demo 的提示又写：

- 各地人民银行规定的跨行汇款服务时间不同；
- 一般为工作日 9:00–17:00；
- “加急”方式在服务时间内办理时，资金当日到达收款人银行；
- **具体到账时间仍取决于收款行系统。**

于是必须区分：

### `interface availability != settlement availability`

网页服务器可以 24 小时在线，登录也可能 24 小时可用，但一笔资金事务后面还存在：

`request accepted`

→ `bank instruction generated`

→ `interbank service window`

→ `receiving bank processing`

→ `recipient balance available`。

因此：

**“网站能点”不是“钱正在移动”的充分证据。**

这类 settlement-clock constraint 不存在于普通静态网页 DOM，却直接决定用户真实体验。

建议以后的 transaction artifact schema 增加：

- `front_end_availability_window`
- `processing_window`
- `settlement_window`
- `recipient_availability_condition`

---

## 8. 凭证等级直接决定能汇多少钱

工行 legacy “单笔转账汇款”说明页写明：

- 用户需到网点开通对外转账权限或注册约转账户；
- 无证书网银客户单笔转账限额 2,000 元、日累计 5,000 元；
- 有证书客户不受上述限额约束。

来源：
- https://www.icbc.com.cn/icbc/html/dongtaiyanshi/personalbank/icbc/intercard/remit/remitexc_infointro.htm

2006 年交易规则还列出动态口令卡、静态支付密码、U盾等不同身份确认方式。

因此：

### `login success != transaction capability`

同一个人能够登录网银，不代表他拥有同样的：

- 对外转账权限；
- 汇款限额；
- 支付凭证强度；
- 可用收款人范围。

这和仓库此前研究的 client-stack eligibility 不完全相同：那里主要是“浏览器/插件决定能不能进入事务”；这里是：

**已经进入以后，credential tier 继续决定事务边界。**

暂定：

### `credential-tier transaction boundary / 凭证等级事务边界`

---

## 9. Web 上的一次“汇款”其实是多个可失败状态的组合

从现存工行帮助/演示页看，至少可以恢复如下状态层：

1. 登录身份；
2. 是否有对外转账权限；
3. 付款账户；
4. 收款人寻址；
5. 金额；
6. 手续费；
7. 指令提交；
8. 授权 / 支付验证；
9. 银行处理；
10. 跨行清算；
11. 收款行处理；
12. 回单/历史查询。

工行企业网银遗留帮助页甚至保留更细的指令状态 vocabulary：

- 提交成功等待银行答复；
- 等待授权；
- 等待二次授权；
- 授权成功等待银行答复；
- 被主管拒绝；
- 被银行拒绝；
- 成功处理。

来源：
- https://www.icbc.com.cn/icbc/html/view/111112/html/10/04.htm

企业网银不是本 note 的主要普通生活对象，但它证明同一机构同时期的 Web transaction engine 本身就被设计成多阶段状态机。

因此 OWA 做金融 Web reconstruction 时，最危险的简化是：

`点击提交 → success`

而真实事务可能是：

`submitted != authorized != bank-accepted != cleared != recipient-available`。

---

## 10. 这类 demo artifact 为什么比“今天截一张网银图”更有历史价值

当前银行官网往往会重新设计门户，但旧演示程序目录可能长期无人删除。结果是：

- 首页是 2020s UI；
- 深层 `/html/download/yanshichengxu/...` 却仍保留 2000s 的字段语言；
- 搜索引擎还能索引这些深层静态页；
- 私人账户页面当然无法公开访问。

因此建立一个新的 artifact hunting 策略：

### `demo-directory archaeology`

优先搜：

- `yanshi`
- `yanshichengxu`
- `demo`
- `help`
- `guide`
- `download`
- `personalbank`
- `transaction query`
- 产品名 + `演示`

旧银行、政务、教育系统尤其值得这样找。

这类目录有可能比主页 archive 更完整地保存事务页面结构。

---

## 11. 但 demo page 也有非常明确的证据天花板

### 能证明

- 官方至少制作过这类 UI / product demonstration；
- 某些字段、状态 vocabulary 和帮助逻辑真实存在于官方遗留页面；
- 示例数据内部标示 2006/2008 等日期；
- 当前官方域名仍在提供这些文件。

### 不能仅凭它证明

- HTML 文件第一次上线的精确日期；
- 2006 年普通用户实际看到的 CSS/JS/浏览器渲染效果；
- 当时生产系统和 demo 100% 字段一致；
- 示例账号对应真人；
- 示例交易真的发生；
- 银行后端按示例页状态机完整执行；
- 2006 与 2008 页面之间的差异一定代表生产系统版本差异。

所以当前 evidence label 应写：

`official current-live legacy demo carrying period-coded transaction schema`

而不是：

`verified 2006 live customer page`。

---

## 12. 页面存活仍然不等于历史事务可重放

即使今天保存完整 HTML，真实 replay 还缺：

- 2006 的网银账户；
- 当时银行卡/存折注册状态；
- 对外转账权限；
- 口令卡/U盾/证书；
- 当时客户端安全控件；
- 历史 TLS/证书兼容；
- 后端账户数据库；
- 人民银行跨行清算窗口；
- 收款银行系统；
- 真正可动用余额。

所以：

### `transaction UI preservation != transaction replayability`

而且比一般表单更严格：钱的事务需要多个独立机构状态共同成立。

---

## 13. 与 HPL 的交叉：资金“瞬间到账”的日常感，是被很多隐藏状态制造出来的

HPL companion：

`../how-people-lived/sources/from-postal-money-orders-to-account-transfer-remittances-and-spatially-split-household-finance-china-1986-2025.zh-CN.md`

（仓库间相对链接实际不可直接跳转，保留路径作为检索 locator。）

HPL 说明，从纸汇票到电子汇兑、银行卡、网银，家庭逐渐可以让收入和人的身体分开移动。

OWA 这里补上：

所谓“网上汇款”并不是把旧流程变成一个按钮，而是重新编码了：

- 收款人是谁；
- 地址是什么；
- 谁能看到什么字段；
- 需要哪种凭证；
- 每次能汇多少；
- 什么时候可以提交；
- 什么时候真正清算；
- 失败以后状态叫什么；
- 用户在哪里查询回单。

也就是说，普通人的“钱到没到”感觉背后是一整套不可见状态机。

---

## 14. 与邮政/第三方支付的过渡对照

2005–2007 的“网汇通 / 网汇e”很适合作为旁证：没有银行卡或没有网银的人，可以：

`邮政柜台交现金`

→ `得到汇兑号/密码`

→ `在 Web 上把这张线下凭证兑换成网上账户余额`。

同期材料：
- 2005-08-10：https://news.sina.com.cn/c/2005-08-10/08526654252s.shtml
- 2006-12-30：https://news.sina.com.cn/o/2006-12-30/104110898847s.shtml
- 2007-04-15：https://news.sina.com.cn/c/2007-04-15/060711641728s.shtml

这再次说明：

`Web transaction` 不必等于 `all-Web transaction`。

一个历史用户可能在：

`cash counter`

和

`browser account`

之间来回切换。

---

## 15. M1 状态

本轮确实得到了一组比新闻 locator 更强的官方 artifact：

- 当前仍 live 的 ICBC legacy demo pages；
- 2006 example transaction schema；
- 2008 cross-bank schema；
- recipient-book / no-account recipient help；
- dated 2006 transaction rules；
- credential / limit / settlement-window documentation。

但按 ROADMAP 的严格标准，**M1 仍不能宣布完成**。

缺少：

- 至少两个已经实际核验 capture timestamp 的 historical mementos；
- 当时 HTTP / headers；
- 当时 DOM 与 charset；
- CSS / JS / image dependency 状态；
- 同一 case 两个历史时间点的真正 replay 对比；
- IE/安全控件/U盾环境中的实机渲染与行为。

准确写法：

```text
legacy official demo artifacts: achieved
period-coded transaction schema: achieved
historical memento verification: not achieved
runtime replay: not achieved

M1 online-banking remittance case: NOT ACHIEVED
```

---

## 16. 下一步 artifact probe

优先目标：

1. 对以下 URL 做 Wayback/CDX probe，必须取得可打开 timestamp 才计入：
   - `.../remitexc_icbc_query_1.htm`
   - `.../remit_noicbc_pay1_1.htm`
   - `.../account_mypayee_remitfor_acctpers.htm`
2. 找 2003 “金融@家”刚推出时的个人汇款演示页，和 2008 页面做真正 schema diff。
3. 找同时期安全控件/证书安装说明，记录 IE、ActiveX、操作系统要求。
4. 记录 demo page 的响应 header、charset、残缺图片和 JS 依赖。
5. 检查 `icbc-us.com` 等镜像/海外站为何也保留一组相似 demo；区分同步镜像和独立历史版本。
6. 寻找 contemporaneous screenshots/manual PDF，不只依赖今天仍在线的 legacy HTML。

---

## 17. 本轮对 OWA 方法论的新增

本轮不只是重复 `page != transaction`。它实际补了四个以后可复用的考古点：

1. **`legacy demo-state fossil`**：公开教学状态可能比私人 transaction state 活得更久；
2. **`interface availability != settlement availability`**：网页在线时钟和资金清算时钟要分开；
3. **`credential-tier transaction boundary`**：同样能登录的人，因凭证等级不同可执行金额/事务不同；
4. **`channel-incomplete history`**：Web history 只覆盖某个服务渠道，不能重建机构全渠道生活史。

这些机制直接影响普通人当时“钱能不能在这一刻真的过去”，因此也能改变 HPL 的跨地家庭解释。

---

## 18. Evidence register

| artifact/source | observed fact | grade | caveat |
|---|---|---:|---|
| ICBC `remitexc_icbc_query_1.htm` | 2006-coded transaction query fields/status/privacy note | A/B | current-live legacy demo, not verified 2006 memento |
| ICBC `account_mypayee...` | payee address book, account/no-account payee distinction | A/B | exact production deployment date unresolved |
| ICBC `remit_noicbc_pay1_1.htm` | 2008-coded cross-bank fields + settlement-time warning | A/B | current URL may differ from historical delivery path |
| ICBC 2006 transaction rules | 24h front-end, credential/password types, service functions | A- | live legacy rules page; historical capture not checked |
| ICBC remit intro | no-cert limits, certificate/permission distinctions | A/B | need historical capture/version diff |
| 2005–07 postal e-commerce reports | cash→counter→voucher→Web account path | B | press/product reports, not HTML transaction artifact |

---

## 19. 结论

旧网里的“汇款页面”不能只当一张表单看。

它其实暴露了一个普通人和金融网络之间的完整接口：

`谁是我`

→ `我有什么凭证`

→ `我最多能动多少钱`

→ `钱要发给哪个身份/账号/支行`

→ `什么时候银行真的处理`

→ `什么时候对方银行承认`

→ `最终状态怎样反馈给我`。

而最值得 old-Web archaeology 珍惜的，往往不是已经永远无法公开的私人账户本身，而是这些被银行当年做来“教用户怎么用”的演示页。它们今天看起来像网站深处没人清理的旧文件，却可能正是**已经消失的交易状态机留下来的公开化石**。