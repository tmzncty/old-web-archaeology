# 公用事业账单查询、网上缴费、预付费表计、销账、停供与复供之间的状态缺口（中国，1996—2015）

> Scope：本文严格服务于 `old-web-archaeology` 的约 1995–2015 中文旧网主范围。它不是中国电力工业史，也不把 2015 年后的智能电表 App、远程复电、家庭人口电价优惠扩写成本仓主线。更长的生活史、海外预付费前史与 2020s 防守型基础设施比较见：
> https://github.com/tmzncty/how-people-lived/blob/main/topics/from-meter-reader-and-paper-bill-to-remote-reconnection-utility-accounts-electricity-payment-and-household-infrastructure-continuity-china-1992-2026.zh-CN.md
>
> 核心考古问题：一张历史网页如果写着“电费查询”“水电煤缴费”“支付成功”“实时销账”，研究者究竟能证明到哪一层？公开网页、户号、表计读数、账单、支付平台订单、银行扣款、公用事业账务系统、预付费卡/表计、欠费状态、停复供命令和一个真实家庭是否仍有电，并不是同一个对象。

本文与仓库已有专题分工：

- `docs/ONLINE_BANKING_REMITTANCE_TRANSFER_PAYEE_AUTHENTICATION_CLEARING_AND_RECIPIENT_STATE_GAPS_1999_2015.md`：银行资金转账；
- `docs/MOBILE_PREPAID_RECHARGE_CARD_ONLINE_TOPUP_BALANCE_AND_SERVICE_CONTINUITY_STATE_GAPS_1999_2015.md`：手机话费充值与通信连续性；
- `docs/PUBLIC_TRANSIT_SMART_CARD_WEB_TOPUP_NFC_WRITEBACK_INTEROPERABILITY_AND_RIDE_AUTHORIZATION_STATE_GAPS_1999_2015.md`：交通卡写卡与实际乘车；
- 本文：**家庭水、电、燃气等持续性基础设施账单如何从表计/账单进入 Web，再经支付和公用事业后台改变账户与服务状态。**

---

## 1. 为什么“网上缴费页”是特别危险的历史对象

一个 archive 里很容易留下：

- “电费查询”链接；
- 户号/客户号输入框；
- 城市/缴费项目下拉框；
- 支付方式列表；
- “立即缴费”按钮；
- 结果页模板；
- “实时到账”“实时销账”等宣传文字；
- 客服电话、营业厅和合作银行列表。

这些 artifact 很容易诱导后来研究者写出：

> 2008 年用户打开这个页面，输入户号，钱就直接进入电力公司，然后家里一定保持供电。

但真实系统至少应拆成：

`physical service address`
`meter / measurement point`
`meter reading`
`utility customer account / 户号`
`tariff state`
`bill / receivable`
`public Web shell`
`bill-query service`
`payment instruction`
`payment processor / bank transaction`
`utility ledger posting / 销账`
`delinquency state`
`disconnect authorization`
`physical disconnect`
`reconnect authorization`
`physical service restoration`

若涉及 IC 卡预付费，还必须再加入：

`vending transaction`
`IC card / token value`
`meter write/load`
`local remaining credit`
`meter relay / load switch`。

任何一步都不能从前一步自动推出。

---

## 2. 对象模型

### 2.1 Utility / billing institution

例如地方供电公司、自来水公司、燃气公司、物业代收机构。

同一城市同一时期可能同时存在：

- 供电企业直接抄表收费；
- 物业/单位转供或代收；
- 银行代扣/代收；
- 第三方公共缴费平台；
- 便利店/邮局/自助设备。

所以“某市可以网上缴电费”不能直接覆盖该市所有住房类型。

### 2.2 Service address / premises

真实物理住宅。

它和 Web 账户不是同一个对象。

### 2.3 Meter / measurement point

记录消耗的物理设备。

必须区分：

- 机械/机电表；
- 电子表；
- 预付费表；
- 远程抄表设备；
- 后来的智能费控表。

“电子”不自动等于“远程”。

### 2.4 Customer account / 户号

供电/水务后台用于识别应收关系的账户标识。

它可能：

- 印在纸账单上；
- 与地址相关；
- 与产权人/合同户名相关；
- 由物业掌握；
- 在搬家/过户后改变关系。

### 2.5 Bill / receivable

某一计费周期依据读数、费率、历史余额等形成的应收记录。

页面上“查询到金额”不等于该金额对应的读表时刻就是页面访问时刻。

### 2.6 Public Web shell

公众能够看到的网页：查询入口、说明页、合作机构、收费渠道、FAQ。

它最容易被 archive 保存，也最容易被误当成整个交易系统。

### 2.7 Bill-query backend

真正接受户号并返回账单的后台。

它可能：

- 要求登录；
- 使用动态请求；
- 调用另一机构的 EBPP 平台；
- 只返回最近一期；
- 在今天仍活着但调用的是现代数据库。

### 2.8 Payment processor / bank

银行卡、网银、付费通、支付宝、快钱、财付通等资金处理层。

### 2.9 Utility ledger

真正决定“这笔应收是否已经销账”的权威公用事业账本。

支付平台订单成功不是该账本状态的同义词。

### 2.10 Service-control state

欠费、提醒、停供、复供等状态。

2015 年以前很多地区的停复供仍包含人工环节，不能把后来智能表远程控制倒投回来。

---

## 3. 基本状态链

### 3.1 后付费账单链

`表计记录消耗`
→ `人工/设备取得读数`
→ `后台形成账单`
→ `账单/通知送达用户`
→ `用户识别户号和金额`
→ `在柜台/银行/Web 提交支付`
→ `支付机构扣款/授权`
→ `缴费信息进入公用事业后台`
→ `权威账本销账`
→ `欠费状态解除/未触发停供`
→ `家庭持续获得服务`

### 3.2 欠费—停供—复供链

`账单到期`
→ `账户进入欠费状态`
→ `提醒/催缴`
→ `满足当时停供规则`
→ `停供动作被授权`
→ `现场或设备执行`
→ `用户补缴`
→ `支付到账`
→ `公用事业账本销账`
→ `生成复供条件/工单`
→ `现实基础设施恢复`

### 3.3 预付费 IC 卡链

`用户购买电量/金额`
→ `售电系统生成记录`
→ `价值/授权写入 IC 卡`
→ `用户把卡带到表计`
→ `表计读取并增加本地可用余额`
→ `持续扣减`
→ `低余额提醒`
→ `达到阈值`
→ `表计可能切断负荷`

因此：

`payment success ≠ card value written ≠ meter credit loaded ≠ electricity available`。

---

## 4. 1996—2002：预付费售电已经是数字状态机，但不是公众 Web 故事

### 4.1 1996 行业标准说明预付费电表已成为明确技术对象

`JB/T 8382-1996《预付费电度表》` 于 1996 年发布、实施，适用于固定安装、对交流有功电能进行本地测量、管理和监控的预付费电度表。

题录来源（B，标准题录；本轮未取得机械行业官方历史数据库的原始标准页）：
https://www.biaozhun.org/hangye/180225.html

这条证据只能证明标准化技术对象存在，不证明 1996 年普通城市家庭的安装比例。

### 4.2 2001 国家标准把 IC 卡售电、卡管理和预付费电表拆成明确系统

国家标准全文公开系统可核验：

- `GB/T 18460.1-2001 IC卡预付费售电系统 第1部分：总则`；
- `GB/T 18460.2-2001 第2部分：IC卡及其管理`；
- `GB/T 18460.3-2001 第3部分：预付费电度表`；
- 发布 2001-10-08，实施 2002-05-01。

来源（A，国家标准）：
https://openstd.samr.gov.cn/bzgk/gb/newGbInfo?hcno=E461098D9DE45BAD33A17A816D7E654F
https://openstd.samr.gov.cn/bzgk/gb/newGbInfo?hcno=0F9D152CD572ADEAF4B20171D1A5E820
https://openstd.samr.gov.cn/bzgk/std/newGbInfo?hcno=31976D3866C066362CE73696D4392583

这组标准是非常好的 old-Web 边界：

> **家庭数字售电可以先以 IC 卡 + 售电设备 + 本地表计的封闭系统出现，而不是先以浏览器出现。**

所以不能把“数字化公用事业”直接等同于“Web 公用事业”。

---

## 5. 2006—2008：公开 Web、电话、银行、邮局、便利店和营业厅长期并存

### 5.1 2006 西宁：“一户一表”本身决定谁和供电企业直接结算

2006 年供电公司同期解释，“一户一表”意味着供电部门直接装表、直接供电、抄表收费和管理；报道回顾当地 1998—2003 年的一户一表改造。

来源（B）：
https://news.sina.com.cn/s/2006-05-12/10038905918s.shtml

old-Web 研究者因此不能从一个地方供电网站的“居民缴费”页推断：

`所有住在该城市的人 = 该供电网站的直接居民客户`。

物业、合表、转供电住房可能仍不在同一状态模型里。

### 5.2 2008 博客园页面保存了一个同时代“缴费渠道矩阵”

2008-06-05，博客园用户“康德”发布《上海水电煤查询大全》。当前页面仍可观察到当时列出的原始入口：

- 上海电力查询：`www.95598.sh.cn`；
- 水费/煤气查询：`online.shfft.com`；
- 付费通网上缴费：`www.shfft.com`；
- 电费电话查询：95598；
- 水费同时可通过银行、邮局、营业站点、便利店、自动转账与付费通等方式完成。

来源（B/C1，同时代用户编目）：
https://www.cnblogs.com/naotang/archive/2008/06/05/1214058.html

这条材料能够证明：

- 这些 URL/渠道在该同时代用户认知中真实存在；
- 查询与缴费可能分属不同站点；
- Web 不是唯一入口。

它不能证明：

- 每个 URL 当日的具体 DOM；
- 每个后端都能成功响应；
- 上海居民普遍使用网上缴费；
- 当前仍活着的 hostname 返回的是 2008 后端。

### 5.3 2008 北京：纸账单仍是 Web 的 credential bootstrap

北京晚报 2008-08-02 记录：用户需先有交通银行太平洋卡并在柜台开通网银缴费，再登录网银，凭《北京市自来水集团公司缴费通知单》上的**用户编号**查询和缴费。

来源（B）：
https://news.sina.com.cn/c/2008-08-02/142914256831s.shtml

因此新增：

### `paper-bootstrap gap`

`Web 表单存在`
≠ `用户可以脱离纸账单完成身份/账户定位`。

旧网页如果只保存一个“用户编号”输入框，却没有说明编号从哪里来，就会把真实生活中的纸质依赖抹掉。

### 5.4 2008 广州：Web 只是多渠道服务之一

2008 年广州供电系统同期材料同时列出营业厅、银行划账、自助服务终端和网上营业厅，并强调 24 小时自助终端解决“下班后也能交电费”的问题。

来源（B + 同期使用者）：
https://business.sohu.com/20080629/n257812452.shtml

这说明早期数字服务并非单线替换：

`柜台 → Web`

更接近：

`柜台 + 银行 + 自动扣款 + 自助终端 + 电话 + Web`。

---

## 6. 2008—2010：第三方支付把地方账单接到统一前端，但后台并没有因此统一

### 6.1 快钱/支付宝的公共事业缴费仍是一城一城对接

2009 年《第一财经周刊》记录：快钱在 2008-05-31 向上海用户推出免费公共事业缴费；支付宝 2008 年 10 月在上海推出类似服务，之后扩展杭州、北京、重庆等地。文章同时说明，地方公共事业机构接入成本很高。

来源（B）：
https://m.cj.sina.cn/page/aHR0cDovL2ZpbmFuY2Uuc2luYS5jb20uY24vbGVhZGVyc2hpcC9tcm9sbC8yMDA5MDYwNC8yMDI0NjMwNjMxNy5zaHRtbD9mcm9tPXdhcA?from=redirect

中国互联网协会 2009-09-01 转载成都服务上线材料时，也明确列出水费、电费、电话费、宽带费和不同支付方式。

来源（B）：
https://www.isc.org.cn/article/8429.html

因此：

`platform supports “electricity bill” category`
≠ `全国公用事业形成一个统一账务 API`。

### 6.2 同一“生活缴费”UI 会把不同地方后台规范化成看似相同的按钮

第三方支付最容易制造一种 archive 错觉：

- 上海电费；
- 成都水费；
- 南京燃气；

都可能在平台界面中变成同一套：

`选择城市 → 选择项目 → 输入户号 → 查询 → 支付`。

但原始机构可能拥有不同：

- 户号格式；
- 账单周期；
- 销账时延；
- 是否可欠费；
- 支持银行卡；
- 退费逻辑；
- 是否需要纸质编号；
- 是否通过另一家 EBPP 平台。

新增：

### `proxy-channel normalization gap`

第三方统一 UI 只能证明**它向用户呈现了一种统一操作语义**，不能证明原公用事业后台原本就具有相同状态机。

### 6.3 2009 用户第一人称说明“平台功能存在”与“哪个流程更好用”是两层证据

2009-04-19，一名用户记录父亲让自己在网上替家里交水、电费，并逐步比较支付宝与建行网银流程；作者还说自己租房时一直使用建行网银缴费。

来源（C1，同时代用户操作记录）：
https://www.leadto.com.cn/technews/1316.html

对 old-Web 考古，这类材料特别有价值，因为它能补 archive 静态页很难回答的问题：

- 用户从哪里进入；
- 哪一步需要切换 tab；
- 不同前端流程是否冗长；
- 家庭成员怎样代办；
- 租房者如何把线上缴费纳入日常。

但用户截图/文字仍不能证明后台 authoritative ledger 的内部状态。

---

## 7. 2014：付费通—支付宝通道终止，暴露“一个按钮背后还有另一个平台”

2014-06-30/07-03 的同期报道记录，上海付费通终止为支付宝提供公共事业账单通道。双方自 2009 年合作，付费通自身运营 EBPP（电子账单呈递与支付）平台；争议中还出现大量高频账单查询造成通道拥塞/服务器故障的说法。

来源（B）：
https://business.sohu.com/20140701/n401594220.shtml
https://business.sohu.com/20140703/n401735846.shtml

这一事件非常适合 old-Web，因为它证明：

`Alipay page alive`
≠ `Shanghai utility query route alive`
≠ `PayEase/付费通 channel alive`
≠ `utility ledger endpoint alive`。

新增：

### `front-end / bill-channel gap`

一个前端品牌继续存在，不代表它当年依赖的账单通道仍存在。

### `partner-topology temporal drift`

同一个“缴电费”按钮在不同年份背后可能经过不同机构。

因此，现代页面不能用于填补历史中间件拓扑。

---

## 8. 关键 state gaps

### 8.1 `bill-shell / utility-ledger gap`

公开账单页保存下来，不等于公用事业账务数据库也被保存。

### 8.2 `meter-reading / bill-time gap`

网页访问日期、账单生成日期、实际抄表/采样日期可能不同。

一张 2009-06-01 显示“本期电费”的网页不能自动证明读数也是 6 月 1 日取得。

### 8.3 `user-number / service-address gap`

页面要求户号只证明户号是接口字段。

archive 通常无法也不应该恢复普通家庭真实“户号 ↔ 姓名 ↔ 地址”映射。

### 8.4 `paper-bootstrap gap`

网上缴费入口可能仍依赖纸账单上的客户编号、条码或通知单。

### 8.5 `payment-submit / payment-commit gap`

用户点击“支付”不等于银行/支付机构已经扣款。

### 8.6 `payment-commit / utility-posting gap`

银行扣款或第三方订单成功不等于公用事业权威账本已经销账。

### 8.7 `notification / ledger gap`

短信、网页“成功”或邮件通知只能证明某层系统发出了结果，不自动证明最终账本状态。

### 8.8 `proxy-channel normalization gap`

支付宝、快钱、财付通、付费通等可能把不同机构包装成统一的“生活缴费”，不能把统一 UI 倒推成统一原始后端。

### 8.9 `front-end / bill-channel gap`

平台前端与 EBPP/地方账单通道可以独立存活或独立失效。

### 8.10 `prepaid-vending / card-write gap`

预付费系统中：

`付款`
≠ `售电记录生成`
≠ `IC 卡写入成功`。

### 8.11 `card-write / meter-load gap`

卡里有新价值不等于用户已经把卡带回住宅并让表计读取。

### 8.12 `meter-credit / physical-service gap`

表计账户状态和现实供电状态仍可能受开关、线路、故障等影响。

### 8.13 `delinquency / disconnect gap`

账户欠费不能在所有年份、地区、用户类别上自动等同于“已经停供”。

具体停供规则需要时期和机构证据。

### 8.14 `payment / reconnection gap`

即使补缴成功，复电也可能是独立事务。

2015 年前尤其不能把后来远程自动复电语义倒投回来。

### 8.15 `direct-customer / actual-resident gap`

真实居住者可能通过物业、房东、单位或合表体系缴费，并非公用事业 Web 账户直接客户。

### 8.16 `historical-URL / current-backend rehydration gap`

旧 URL 今天若仍能打开，却调用 2026 年账务系统，只能算**当前后端重水合**，不能称历史账单回放。

---

## 9. Archive 为什么天然偏向“缴费入口”，而不是“一个家庭有没有真正交上”

### 9.1 公共 shell 最容易被抓

Crawler 容易看到：

- 首页；
- 帮助；
- 合作银行；
- 城市选择；
- 户号输入框；
- 资费说明。

### 9.2 真实 transaction 最难被抓

真正事务通常需要：

- 真实户号；
- 用户登录；
- 动态账单查询；
- 银行/第三方支付跳转；
- session/cookie；
- CAPTCHA/证书/ActiveX；
- 账务 API；
- 实时 ledger state。

这些正是 archive 最难保存的部分。

因此产生：

### `transaction-survival inversion`

> **越能证明某个普通家庭实际完成了缴费的材料，越可能因为登录、支付、隐私和动态后端而没有被公共 Web archive 保存。**

### 9.3 欠费、停供和复供更不可见

一个被保存的“在线缴费帮助页”不会告诉研究者：

- 有多少用户晚交；
- 谁真的被停过；
- 复电等了多久；
- 哪个家庭由物业代缴；
- 哪次银行扣款和公用事业销账不同步。

这些状态往往只存在于私人账单、企业业务库、客服电话记录和现实家庭经验里。

---

## 10. 浏览器与技术环境假设

2000s 公用事业缴费页可能依赖：

- IE-only 页面；
- ActiveX/网银安全控件；
- 客户端证书；
- 弹窗；
- frameset；
- GB2312/GBK；
- 跨域跳转；
- 银行支付页面；
- JS 动态提交；
- 第三方 EBPP 接口。

因此现代 Chromium 能打开一个历史 HTML，不代表：

- 当时 Firefox/Netscape/IE 都能用；
- 网银控件仍可执行；
- 支付跳转可完成；
- 后端查询与销账仍可复现。

应记录 `browser assumption`，而不是用现代截图代替历史可执行性。

---

## 11. 2008 上海候选 historical capture：本轮验证边界

同时代博客页给出了三个非常明确的 original URL 候选：

- `http://www.95598.sh.cn/` / 其电费查询入口；
- `http://online.shfft.com/`；
- `http://www.shfft.com/`。

来源定位：
https://www.cnblogs.com/naotang/archive/2008/06/05/1214058.html

本轮尝试以约 2008-06-05 时点构造 Wayback replay：

- `web.archive.org/web/20080605000000/http://www.95598.sh.cn/`
- `web.archive.org/web/20080605000000/http://www.shfft.com/`
- `web.archive.org/web/20080605000000/http://online.shfft.com/`

当前研究环境拒绝直接打开未经搜索结果建立 provenance 的构造 archive URL；因此没有取得可以逐项核验下列字段的合格 memento：

- capture URL；
- Memento-Datetime；
- HTTP/replay status；
- historical charset；
- DOM；
- form action；
- JS/ActiveX 依赖；
- 历史账单 query endpoint；
- 支付跳转。

所以本轮只允许记录：

> **M1 verified 2008 Shanghai utility-payment historical capture: NOT ACHIEVED IN THIS SLICE.**

这绝不等于：

> `Wayback 没有保存这些页面`。

按 `docs/METHOD.md`：

`locator 未实际检查 ≠ verified capture`；

`没有找到 ≠ 当时不存在`。

---

## 12. Preservation levels

### S0 — hostname/name only

仅知道历史服务或 hostname 存在。

### S1 — contemporary external reference

同期博客/新闻明确提到 URL、功能或操作。

### S2 — public shell capture

已验证历史首页/帮助页，但没有账单查询事务。

### S3 — historical query form capture

能确认户号/项目输入字段、form/JS 等，但没有真实返回。

### S4 — sanitized/static result artifact

有同时代公开教程/截图展示查询结果结构，但不保存真实个人户号/地址。

### S5 — payment-flow artifact

能确认历史支付跳转/支付页面结构，但无真实私人交易。

### S6 — backend semantics corroborated

通过官方技术文档/同期运营材料确认支付到公用事业销账的语义。

### S7 — service-control semantics corroborated

能够确认当时欠费、停供、复供的规则和实际执行链。

### S8 — bounded reconstruction

只在证据足够时重建“一个虚构户号经过哪些界面状态”，明确标 `reconstruction`，绝不使用真实普通家庭私有账单。

---

## 13. 隐私与伦理边界

真实公用事业账单很容易泄露：

- 姓名；
- 详细住宅地址；
- 户号；
- 电话；
- 家庭能源使用模式；
- 欠费；
- 迁入迁出；
- 可能的居住/空置规律。

因此本仓不以“找到真实用户账单截图”作为高质量考古目标。

优先保存：

- 空白表单；
- 官方说明；
- 字段名；
- URL pattern；
- 同期教程中的打码截图；
- 平台拓扑；
- state transitions；
- 公开标准。

如果私人账单恰好公开可见，也只使用支持历史结构 claim 所需的最少信息，不重新扩散身份和地址。

---

## 14. 已证实 / 高概率 / 不知道

### 已证实

- 1996 年中国已有“预付费电度表”行业标准；
- 2001 年国家标准已把 IC 卡预付费售电系统、卡管理和预付费电表明确标准化；
- 2008 年上海同时代普通 Web 页面明确列出 `www.95598.sh.cn`、`online.shfft.com`、`www.shfft.com` 等查询/缴费入口；
- 2008 北京部分水费网银流程需要纸质缴费通知单上的用户编号，并需先在银行柜台开通网银；
- 2008–2009 第三方支付开始在多个城市接入公共事业缴费；
- 2009 有同时代用户记录替父亲网上缴水电费和租房时使用网银的实际操作；
- 2014 上海付费通与支付宝的公共事业账单通道合作终止，证明前端与账单中间层可独立变化。

### 高概率，但本轮不升级为完整历史 capture 结论

- `95598.sh.cn` / `shfft.com` / `online.shfft.com` 在 2008 前后存在可由普通用户访问的历史页面形态；
- 其中至少部分查询/缴费涉及动态后端而不是纯静态 HTML；
- 部分银行支付页面会受 IE/安全控件/证书环境影响。

这些都需要实际 memento / 同期手册进一步核验。

### 不知道

- 2008-06-05 三个 hostname 的确切 DOM/charset/form action；
- 当日各账单接口是否全部在线；
- 查询返回 payload 的字段结构；
- 支付平台与公用事业后台的确切销账 SLA；
- 2008–2010 普通家庭网上缴水电费的代表性采用率；
- 不同城市、不同物业/转供电住房是否能使用同一类 Web 入口；
- 历史用户发生“支付成功但未销账”的实际频率。

---

## 15. 对中文旧网考古方法的新增意义

### 15.1 “线上办事史”不能只看页面有没有按钮

真正的研究单位应是：

`public interface + credential bootstrap + transaction + institutional backend + real-world execution`。

### 15.2 旧 Web 经常是纸张和现实机构的增量层，而不是替代层

2008 北京水费案例特别典型：用户仍要从纸账单取得编号、在银行线下开通网银，然后才回家“网上办”。

### 15.3 聚合平台会抹平地方差异

现代研究者看到支付宝统一“水电煤”页面，很容易误以为当时全国已经有统一生活缴费系统。

实际上，平台仍需逐个接地方机构和中间件。

### 15.4 最关键的历史状态往往天然不适合被 archive 保存

账务 ledger、户号—地址映射、支付授权、欠费和停供都既动态又敏感。

所以“无法复原一个真实家庭的完整交易”不是考古失败，而是这个对象的结构性边界。

---

## 16. 下一步

1. 通过可建立 provenance 的 archive 搜索结果取得 `www.95598.sh.cn`、`shfft.com`、`online.shfft.com` 的真实 memento，再记录 capture datetime / HTTP / charset / DOM。
2. 寻找 2008–2010 上海付费通/电力官方帮助页或银行网银缴费操作手册，补全 form/query/payment handoff。
3. 搜索 IE/ActiveX/银行证书依赖，建立一个最小 browser assumption 表。
4. 调查是否有 Common Crawl/WARC 能独立验证这些历史 host，而不是只依赖 Wayback。
5. 分离“供电企业直接客户”与“物业/房东/单位代收”页面语义，避免把城市级入口外推到所有住宅。
6. 若能取得不涉及私人数据的历史预付费 IC 卡售电说明，补 `payment → card write → meter load` 的 A/B 级流程证据。

---

## 主要来源

- `docs/METHOD.md`（本仓证据合同）
- 国家标准 GB/T 18460.1-2001：https://openstd.samr.gov.cn/bzgk/gb/newGbInfo?hcno=E461098D9DE45BAD33A17A816D7E654F
- 国家标准 GB/T 18460.2-2001：https://openstd.samr.gov.cn/bzgk/gb/newGbInfo?hcno=0F9D152CD572ADEAF4B20171D1A5E820
- 国家标准 GB/T 18460.3-2001：https://openstd.samr.gov.cn/bzgk/std/newGbInfo?hcno=31976D3866C066362CE73696D4392583
- 2006 西宁一户一表：https://news.sina.com.cn/s/2006-05-12/10038905918s.shtml
- 2008 上海水电煤查询大全：https://www.cnblogs.com/naotang/archive/2008/06/05/1214058.html
- 2008 北京交行网银缴水费：https://news.sina.com.cn/c/2008-08-02/142914256831s.shtml
- 2008 广州电力自助营业厅：https://business.sohu.com/20080629/n257812452.shtml
- 2009 用户支付宝/建行网银水电煤流程比较：https://www.leadto.com.cn/technews/1316.html
- 2009 第一财经周刊《快钱如何快跑》：https://m.cj.sina.cn/page/aHR0cDovL2ZpbmFuY2Uuc2luYS5jb20uY24vbGVhZGVyc2hpcC9tcm9sbC8yMDA5MDYwNC8yMDI0NjMwNjMxNy5zaHRtbD9mcm9tPXdhcA?from=redirect
- 2009 中国互联网协会成都公共事业缴费：https://www.isc.org.cn/article/8429.html
- 2014 付费通—支付宝通道终止：https://business.sohu.com/20140701/n401594220.shtml
- 2014 新华网转载后续争议：https://business.sohu.com/20140703/n401735846.shtml

> 本文件是 research/state-gap note，不是历史页面 reconstruction。未取得 verified memento 的部分明确停在 locator / contemporary-reference 层，不使用生成内容补历史 DOM、账单或交易结果。