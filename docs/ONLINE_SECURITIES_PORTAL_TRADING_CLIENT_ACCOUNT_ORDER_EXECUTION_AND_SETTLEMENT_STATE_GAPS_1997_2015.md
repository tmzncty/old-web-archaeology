# Online securities portal / trading client / account / order / execution / settlement state gaps（1997—2015）

## 0. Scope

本 note 研究约 1997—2015 年中文 Web 中券商网站、网上委托入口、客户端软件下载、行情、账户权限、委托与成交确认的历史可见性。

它不写“中国证券市场史”，也不把 1980s—1990s 的证券营业厅和电话委托无限扩进本仓；这些前史及 2016—2026 移动券商、家庭资产配置、青年未来预期，主要写入交叉专题：

- `how-people-lived/topics/from-securities-halls-and-radio-quotes-to-mobile-brokerage-retail-investing-market-time-and-self-provisioned-futures-china-1986-2026.zh-CN.md`

本仓范围仍保持在约 1995—2015 中文互联网，重点回答：

> **当券商把行情、风险提示、软件、网上委托和客户服务放进中文 Web 后，一张历史网页到底能证明一次真实证券交易的哪一段？为什么 public page、installed client、broker gateway、exchange order state、bank custody 与最终 settlement 必须拆开？**

---

## 1. Research unit：不能把“券商网站可打开”写成“投资者已经成交”

至少拆开以下对象：

1. **physical investor**：现实投资者；
2. **securities account**：证券账户；
3. **broker capital account / 资金台账**：券商侧交易资金账户；
4. **custody bank account**：第三方存管银行账户；
5. **online-trading entitlement**：客户是否已申请/获得网上委托权限；
6. **broker public site / host**：券商公开网站；
7. **online-trading entrance**：监管意义上的固定 Internet 入口；
8. **download page**：客户端/安全组件/升级包的公开下载页面；
9. **installer / executable**：历史软件二进制本身；
10. **runtime dependencies**：操作系统、浏览器、运行库、证书、加密组件、防火墙等环境；
11. **login session**：一次真实认证会话；
12. **quote feed**：行情数据流；
13. **displayed quote state**：某一终端显示的价格、时间戳、延迟状态；
14. **order ticket/form**：用户填写的委托界面；
15. **order submission**：本地终端发起委托；
16. **broker gateway receipt**：券商系统是否收到；
17. **exchange acceptance**：交易所是否接受；
18. **order state**：未报、已报、部分成交、全部成交、已撤、废单等；
19. **fill / execution**：真实成交；
20. **clearing / settlement**：清算交收；
21. **bank-securities transfer**：第三方存管下的资金划转；
22. **withdrawable-funds state**：资金最终是否可转出/使用；
23. **paper/phone fallback**：柜台、电话、自助终端等替代渠道。

最低状态链：

`broker site exists` ≠ `broker licensed for Internet entrustment` ≠ `branch enabled` ≠ `investor has entitlement` ≠ `client/browser can run` ≠ `login succeeds` ≠ `quote is timely` ≠ `order submitted locally` ≠ `broker received order` ≠ `exchange accepted order` ≠ `order filled` ≠ `cancel succeeded` ≠ `settlement completed` ≠ `funds withdrawable`。

还必须保留几条 old-Web 特有边界：

`historical download page survives` ≠ `binary survives` ≠ `binary can still run` ≠ `backend still exists`。

`historical quote page survives` ≠ `historical live quote feed survives`。

`account owner` ≠ `person who physically operated keyboard that day`。

---

## 2. Evidence baseline

沿用 `docs/METHOD.md`：

- **A**：历史 capture、同时代监管文件、券商公告、软件手册、原始技术资料；
- **B**：同期新闻、教程、安全事件、用户操作说明；
- **C**：后来回忆；
- **D**：研究者复原。

本轮尤其强调：**监管文件可以证明系统应当有什么边界，不等于某一家券商每个历史版本都严格按相同界面实现。**

### 当前得到的 historical original hosts / locators

本轮取得一个很强的同时代券商 host：

- `http://www.sw2000.com.cn/` — 2004 年上市公司/基金等同时期资料把它列为申银万国证券网站，并记录公司公告在该站披露。

示例来源：
- 2004 年公司资料的当前保存页中保留主办券商申银万国网址：
  https://m.cj.sina.cn/page/aHR0cDovL2ZpbmFuY2Uuc2luYS5jb20uY24vc3RvY2svY29tcGFueS9zaC85MDA5MzEvOV8xNC5zaHRtbA?from=redirect

另有 2007 年同时代公告保存 `www.htsc.com.cn` 等券商入口，例如华泰证券第三方存管公告：
- https://business.sohu.com/20070711/n250993645.shtml

这些都是 historical original host/URL locator，**不等于本轮已实际验证对应年份的 archive capture**。

---

## 3. 1997—2001：网上委托是已有远程交易渠道上的新层，不是第一个“电子委托”

### 3.1 2000 监管文本明确排除了专用电话拨号网

中国证监会 2000-03-30 的《网上证券委托暂行管理办法》是本专题最关键的一手规范。

它把网上委托定义为证券公司“通过互联网”向本机构已开户投资者提供下达证券交易指令、取得成交结果的服务；随后明确：这里的互联网指通用公共计算机通信网络，**不包括**证券公司租用公共通信设施、专门用于证券委托的电话拨号网或其他计算机网络。

来源：
- CERNET 保存法规全文：https://www.edu.cn/bz_6525/20060323/t20060323_83220.shtml

**证据等级：A。**

因此 old-Web 不应写：

> “1997 左右出现网上证券交易，所以此前只能到柜台。”

更准确的是：

> 电话委托、专门拨号网络、自助终端等远程/电子委托早已存在；Internet 网上委托是把交易入口进一步放到通用公共网络中的一层。

### 3.2 2000 法规本身已经要求区分 public entrance 与 internal system

同一办法要求：

- 已经合法开户的客户本人申请网上委托，办理时核验身份证明原件；
- 网上委托必须有替代交易方式；
- 客户信息、资金账户、股票账户和身份识别等核心数据系统不能任意托管在合法营业场所之外；
- 网上委托系统要与其他业务系统技术隔离；
- 禁止通过网上委托系统直接访问证券公司内部业务系统；
- Internet 传输中的敏感信息需加密；
- 券商要提供固定互联网入口站点；
- 入口站点和终端软件都必须提示传输中断、停顿、延迟、身份仿冒、行情错误等风险。

来源同上。

这几条足以建立一个 old-Web 的核心模型：

`public broker website` → `Internet-facing entrustment system` → `isolated broker internal system` → `exchange infrastructure`。

Archive 即使完整保存第一层，也不能据此声称后面三层被保存。

### 3.3 2001 的资格批复：网站存在还不够

2001-02-05，中国证监会核准 23 家证券公司开展网上证券委托，包括国泰君安、国信、中信、申银万国、海通、中国银河、平安等。

来源：
- 中国证监会：https://www.csrc.gov.cn/csrc/c101799/c1003791/content.shtml

**证据等级：A。**

批复还要求券商网站首页提示：获得证监会网上委托核准，不构成监管机关对安全和效率的保证。

因此：

`site has “网上交易” words` ≠ `regulatory qualification proven`。

对于 2000—2001 历史站点，最好把资格批复与 archive page 配对，而不是只看网页营销文案。

---

## 4. 2003：SARS 压力测试揭示 Web/电话已经是 transaction fallback，但实时交易仍依赖整套后台

2003-05-17，CCTV 同期报道 SARS 期间到营业部现场交易人数明显下降，而网上交易和电话委托上升；银河证券扩容网上交易系统，在北京、上海增加镜像点。受访券商称网上交易额占比由约 15% 上升到 60% 多。

来源：
- CCTV.com / CNTV 当前保存页：《券商争抢网上交易商机》：https://www.cntv.cn/lm/776/13/86033.html

**证据等级：B+。** 同期报道，比例是受访券商口径，不能外推全市场。

对 old-Web 最重要的不是“60%”本身，而是报道里出现的基础设施对象：

- 网站预约；
- 网上交易账户；
- 免费电话系统；
- 在线信息服务；
- 交易系统扩容；
- 镜像点；
- 并发在线容量。

这证明网页只是入口壳的一部分。一次 SARS 期间成功交易至少还需要：

`用户接入网络` → `DNS/host reachable` → `登录/认证` → `行情或委托终端` → `券商 Internet gateway` → `内部交易系统` → `交易所`。

因此 archive 里“主页能打开”无法证明当日交易能力。

---

## 5. 2004：“证券大盗”说明 endpoint software 是历史交易系统的一部分

2004 年 11—12 月，同期报道记录“证券大盗”木马可以窃取多家证券交易系统的账号、密码；《证券时报》的调查称木马利用 IE 浏览器漏洞，并记录用户键盘输入再外传。

来源：
- 北京娱乐信报/新浪财经，2004-11-29：https://finance.sina.com.cn/roll/20041129/04421186279.shtml
- 《证券时报》/新浪财经，2004-12-01：https://finance.sina.com.cn/roll/20041201/115345174t.shtml

**证据等级：B+。**

### 5.1 不能从这条证据推出“所有券商 IE-only”

它只能证明：至少存在一类真实攻击路径，依赖投资者终端、IE 漏洞、键盘输入和券商交易账号。

因此目前：

- `IE was part of some attack paths`：已证实；
- `all online-trading systems required IE`：未知；
- `specific ActiveX control was mandatory at sw2000.com.cn in 2004`：未知；
- `exact Windows/browser versions required`：未知。

没有历史 capture、安装包/手册前，不得用年代刻板印象补成“IE6 + ActiveX”。

### 5.2 Archive 的安全偏差

Wayback 类公共档案最可能保存：

- 风险公告；
- 软件名称；
- 下载链接；
- 帮助页。

最不可能完整保存：

- 当时实际下载的 exe/dll；
- 安装后写入的组件；
- 用户本地证书/配置；
- 恶意木马感染状态；
- 登录会话；
- 真实委托。

因此形成 **`security-warning survival / endpoint-state loss asymmetry`**。

---

## 6. 2004 historical host：`sw2000.com.cn` 能证明什么，不能证明什么

2004 年公司材料把 `www.sw2000.com.cn` 明确列为主办券商申银万国证券网站，并多次说公司公告曾刊登于该网站。

来源：
- 新浪财经当前保存的 2004 年公司资料页：
  https://m.cj.sina.cn/page/aHR0cDovL2ZpbmFuY2Uuc2luYS5jb20uY24vc3RvY2svY29tcGFueS9zaC85MDA5MzEvOV8xNC5zaHRtbA?from=redirect

**证据等级：A-/B+ historical locator。** 它是同时期文档中明确写出的 host，可证明 host 与券商的历史关联；不是 2004 页面 capture。

本轮尝试继续定位该 host 的公开历史 capture，但没有得到一份能够**实际打开并核验**以下字段的合格 M1 artifact：

- `archive_source`；
- `capture_url`；
- `original_url`；
- `capture_datetime`；
- HTTP/replay 状态；
- Content-Type / charset；
- DOM/form action；
- 历史客户端软件下载 URL；
- scripts/subresources；
- 第二历史时点。

因此：

**`M1 verified historical Chinese broker portal/trading capture: NOT ACHIEVED IN THIS SLICE`。**

这不等于“Wayback 没保存”；目前只说明本轮没有拿到一份符合 `docs/METHOD.md` 最低合同、并实际打开检查过的 capture。

---

## 7. 2007：第三方存管让“一次网上炒股”再多出一个银行状态机

2007 年证券公司大规模推进客户交易结算资金第三方存管。同期公告明确展示了一个旧网研究必须保留的账户栈。

例如东北证券公告要求个人投资者先到证券营业部办理资金台账，再签署银行存管协议、预指定存管银行；联合证券、银河证券等同期公告也都把券商资金账户与指定银行关系拆开。

来源：
- 东北证券公告/证券时报转载，2007-08-11：https://finance.sina.com.cn/stock/t/20070811/05311597858.shtml
- 中国银河证券公告，2007-09-12：https://finance.sina.com.cn/stock/t/20070912/03391661462.shtml
- 工商银行，2007 年第三方存管上线客户超过千万的官方信息：https://www.icbc.com.cn/page/721852338615910416.html

**证据等级：A-/B+。** 券商/银行同期业务公告。

国盛证券的 2007 年公告甚至同时列出资金划转可经：

- 券商电话委托；
- 钱龙自助委托；
- 网上交易系统；
- 银行电话银行；
- 网上银行；
- 自助终端。

来源：
- https://business.sohu.com/20070906/n251985728.shtml

这证明 2007 年绝不是“网页取代柜台”的单线迁移，而是**多渠道共同操作同一个账户栈**。

最低状态应再细化为：

`securities account open`

≠ `broker capital account valid`

≠ `custody bank pre-designated`

≠ `bank-side confirmation complete`

≠ `bank-securities transfer channel enabled`

≠ `cash transferred into tradable balance`

≠ `order executable`。

### `account-page survival / bank-link state loss`

几十年后券商公告可以保存“支持某银行第三方存管”，但某一个投资者究竟：

- 选择了哪家银行；
- 是否完成银行端确认；
- 当日银证转账是否成功；
- 哪一笔钱已经成为可用资金；

都属于私有事务状态，公共 Web archive 不应保存。

---

## 8. 2013：即使“网上开户”出现，也要继续拆账户类型

2013 年券商非现场开户开始放开。同期上海证券报报道招商证券上线网上开户/见证开户，投资者可通过视频身份验证填写资料、签风险揭示书并接受回访；但报道当时特别说明，非现场方式可以开资金账户，证券账户仍需按当时规则到营业部办理。

来源：
- 上海证券报/每日经济新闻，2013-03-20：《招商证券推出非现场开立资金账户》：https://www.nbd.com.cn/articles/2013-03-20/724632.html

**证据等级：B+。** 同期报道。

因此 old-Web 不能把一个“立即开户”按钮抽象成单一状态：

`online application started` ≠ `video identity passed` ≠ `agreements signed` ≠ `broker capital account opened` ≠ `securities account opened` ≠ `custody link finished` ≠ `trading entitlement enabled`。

这也提示 archive 研究必须保留**同一年不同账户对象的监管边界**，不能用今天的一站式手机开户反推 2013。

---

## 9. 主要 archive asymmetries

### 9.1 `public-shell / transactional-state asymmetry`

最容易保存：

- 首页；
- 行情栏目；
- 风险提示；
- 帮助页；
- 软件名；
- 下载按钮。

最不可能公开保存：

- 登录后的资金余额；
- 真实持仓；
- 委托流水；
- 部分成交；
- 撤单结果；
- 清算交收；
- 银行划转。

所以一份保存完整的券商网站，仍然可能几乎没有保存最重要的真实交易状态。

### 9.2 `download-page / executable-binary asymmetry`

历史下载页可以活着，链接的 exe/cab/dll 已经消失；即使二进制还在，没有哈希、签名、发布时间和 provenance，也不能直接当成该历史页面对应版本。

### 9.3 `executable / backend asymmetry`

即使找到原客户端并在隔离 VM 里运行，原认证、行情、委托服务器可能早已停机或换协议。

`client launches today` 只能证明可执行文件在现代复原环境能启动，不证明 2004 年真实交易链可复现。

### 9.4 `quote-page / live-feed asymmetry`

历史页面可能保存某个 HTML 框架和股票代码输入框，却不会稳定保存当时由后端推送的逐时行情。

因此：

`historical quote UI verified` ≠ `historical quote value/feed verified`。

### 9.5 `order-entry / execution asymmetry`

“提交”按钮可被 capture，真实交易所撮合状态通常不可。

必须保留：

`clicked submit` ≠ `request reached broker` ≠ `broker accepted` ≠ `exchange accepted` ≠ `filled`。

### 9.6 `account-owner / operator ambiguity`

监管原则要求本人办理关键权限，不意味着每一次后续键盘操作都能由 public Web 证明是本人完成。家庭成员、同事、营业部人员协助等现实操作需要具体材料才能判断。

不得从账号归属自动推断当时键盘前是谁。

### 9.7 `Web-survival / telephone-and-terminal invisibility`

Web archive 会结构性放大浏览器的重要性，因为：

- 电话委托没有网页；
- 营业部自助终端没有公共 URL；
- 专用拨号软件和本地客户端不一定被 crawler 获取；
- 2007 第三方存管还同时通过银行柜台、电话银行、自助设备运行。

因此任何“old Web 证券史”都必须主动把非 Web 渠道重新补回。

---

## 10. Claim table

| Claim | Evidence | Grade | Confidence | Boundary |
|---|---|---:|---:|---|
| 2000 监管定义把公共 Internet 与券商专用拨号/计算机网络区分 | 《网上证券委托暂行管理办法》 | A | 高 | 规范定义，不代表此前远程交易不存在 |
| 2000 办法要求本人申请网上委托并提供替代交易方式 | 同上 | A | 高 | 是监管要求，不证明每次现实执行都无违规 |
| 2001 有 23 家券商获网上委托资格 | CSRC 批复 | A | 高 | 获资格 ≠ 所有客户立即可用 |
| SARS 期间部分券商网上交易占比大幅上升 | 2003 CCTV | B+ | 中高 | 受访券商口径，不外推全国 |
| 2004 有木马针对多家网上交易系统账号密码 | 同期媒体/安全公司采访 | B+ | 中高 | 不证明所有券商统一技术栈 |
| `sw2000.com.cn` 在 2004 被同时期资料列为申银万国网站 | 同时期香港资料 | A-/B+ | 高 | host 关联 ≠ capture 已核验 |
| 2007 第三方存管把券商资金账户与银行存管状态连接 | 多家券商/银行同期公告 | A-/B+ | 高 | 不等于每一客户同日迁移成功 |
| 2013 已出现网上/视频非现场开资金账户 | 同期证券报报道 | B+ | 中高 | 当时证券账户仍有另一制度边界 |

---

## 11. Browser / client / charset matrix：当前仍需 UNKNOWN

| Object | Known | Unknown |
|---|---|---|
| 2000—01 broker Internet entrance | 法规要求固定入口站点 | 具体浏览器、HTML、charset、插件 |
| 2003 online trading system | 同期报道确认存在网站/网上交易系统与镜像点 | browser-only 还是 client-heavy；具体协议 |
| 2004 endpoint security | 某木马利用 IE 漏洞、键盘记录 | 每家券商是否 IE-only；是否需要 ActiveX |
| `sw2000.com.cn` | 2004 host 关联明确 | 历史 capture DOM/charset/forms/subresources |
| 2007 online trading + bank custody | 多渠道存在 | 每一券商/银行组合的具体 UI、证书、控件 |
| 2013 online account opening | 视频验证/在线资料流程存在 |具体浏览器兼容性、插件与实现版本 |

在取得历史 capture、官方用户手册、安装包或截图前，**不填 IE6、ActiveX、GB2312/GBK、Windows XP 等“时代常识”**。

---

## 12. 隐私与安全边界

证券历史事务天然包含高敏感金融信息。本仓只研究公开页面结构、软件/制度状态机和同时代公开材料，不收集或重新公开：

- 普通人的证券账号；
- 身份证号；
- 银行卡号；
- 历史持仓/余额；
- 委托流水；
- 私有成交记录；
- 可用于登录的旧口令/证书；
- 恶意软件样本的可操作攻击细节。

如果以后找到历史客户端，只做隔离环境下的文件级/界面级考古；不得使用真实账户、真实券商后台或尝试绕过认证。

---

## 13. 本轮 M1 结论与下一步

### 已完成

- 确立 1997—2015 中文网上证券研究单位和完整状态链；
- 用 2000 监管文本严格区分 Internet 与专用拨号网络；
- 找到 2001 首批 23 家网上委托资格的 A 级监管证据；
- 找到 2003 SARS 对远程交易渠道的 contemporaneous stress test；
- 找到 2004 endpoint security 证据；
- 找到 `sw2000.com.cn` historical original host locator；
- 将 2007 第三方存管加入账户/资金状态链；
- 将 2013 非现场开户拆成资金账户、证券账户等不同状态。

### 尚未完成

**`M1 verified historical Chinese broker portal/trading capture: NOT ACHIEVED IN THIS SLICE`。**

还缺：

1. 实际打开且可复核的 2000s 券商 capture；
2. 同一 host 至少第二历史时点；
3. Content-Type / charset；
4. DOM / form action / historical URL pattern；
5. 客户端下载链接与二进制 provenance；
6. 历史 browser/OS/plugin 要求；
7. 主文档与子资源保存完整度；
8. public portal 与 transaction host 是否不同域/子域；
9. 至少一个官方/同期用户手册与 capture 的独立交叉核验。

### 下一轮可执行 archaeology

优先从 `sw2000.com.cn` 继续：

- 找 Wayback/Common Crawl candidate capture；
- 实际打开而不是只记 locator；
- 记录 Memento datetime 与 original URL；
- 找“网上交易/软件下载/风险揭示/帮助”历史 URL；
- 寻找同年代公告中直接引用的 client 文件名；
- 若找到合法可研究的 installer，记录 hash、文件时间、签名、PE metadata，但不连接真实交易服务；
- 至少比较 2004 与 2007（第三方存管以后）两个时点。

其次可用 2007 同期明确保留的 `www.htsc.com.cn` 做独立对照，避免把一家券商实现方式误写成全行业标准。

---

## 14. 对 `how-people-lived` 的交叉贡献

这个 old-Web 案例改变的不是一句“炒股从线下搬到线上”，而是把它拆成三次不同的移动：

1. **行情先离开营业厅**：报纸、广播、电话把价格送到人；
2. **委托再离开营业厅**：电话/专线、Internet、客户端让指令远程提交；
3. **账户与资金最后继续拆分**：证券账户、资金台账、银行第三方存管、远程权限分别成为不同制度状态。

因此网页只是一个表面层。真正改变普通生活的是：

> **一个原本必须把身体带到证券营业厅的人，逐渐可以只把“指令”送过去；与此同时，她也必须开始自己管理电脑、网络、账号、银行关系、延迟和安全风险。**
