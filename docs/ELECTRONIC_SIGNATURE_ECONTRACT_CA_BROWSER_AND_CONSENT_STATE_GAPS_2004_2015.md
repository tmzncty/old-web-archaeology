# 电子签名、电子合同、CA、浏览器与合意状态缺口（中文旧网，2004—2015）

> Cross-repo companion: `tmzncty/how-people-lived/topics/ELECTRONIC_SIGNATURE_REMOTE_CONTRACT_AND_COMMITMENT_EXECUTABILITY_1994_2026.md`

## 0. Scope

本专题严格留在本仓约 1995—2015 中文互联网 scope 内，重点研究 2004—2015 年中文 Web 中“电子签名 / 电子合同 / 网上签约”怎样被呈现、执行和保存。

1994 年 NIST 数字签名标准、1996 年 UNCITRAL 电子商务示范法等全球前史只在 companion life-history 文档中用于跨国比较；本文件不把 `old-web-archaeology` 扩张成全球电子签名史。

这里尤其需要防止四种混淆：

```text
电子签名 ≠ 扫描签名图片
电子合同 ≠ 一份 PDF 文件
网上签约 / 网签 ≠ 密码学数字签名
历史网页 capture ≠ 历史签约 transaction
```

研究目标不是证明“电子签名技术很先进”，而是把普通用户在旧 Web 上完成一次正式承诺所依赖的状态链拆开。

---

## 1. Research units

按照 `docs/METHOD.md`，本专题至少区分以下研究单位：

### platform
电子签约平台、CA 服务、政务/行业签约平台、企业内部人事平台。

### site / host
例如 2004—2005 同期媒体提到的 `www.esca.cn`，以及后来第三方电子签平台 host。

### account
用户账号、企业账号、证书主体、签名人身份。

### page
合同展示页、签署页、证书下载页、帮助页、验证页、合同查询/下载页。

### artifact
- HTML/CSS/JS；
- ActiveX/插件；
- 证书/USBKey 驱动；
- PDF/数据电文；
- 签名值；
- 时间戳；
- 审计日志；
- SMS/邮件通知；
- CA 证书链。

### claim
每条 claim 必须明确是功能存在、普通用户可用、有人实际使用、规模普及还是现实后果。

---

## 2. Evidence contract

本专题沿用仓库 A/B/C/D：

- **A**：法律、规章、同期官方产品文档、真正历史 capture、原始软件/证书/手册；
- **B**：同期媒体、教程、用户操作说明、企业/行业采访；
- **C**：后来回忆；
- **D**：研究者状态机、协议/页面复原。

特别说明：

- 今天仍托管的 2004/2005 法律文本，是 A 级**历史内容证据**，但不是 2004/2005 Web UI capture；
- 今天微软支持站仍托管的 InfoPath 2007 说明，可证明 legacy product 的技术要求，但不能当成 2007 年 Microsoft 页面形态的 capture；
- 同期厂商/创业者“首个”“第一份”“零风险”等宣传，只能证明其当时这样宣称。

---

## 3. 必须拆开的签署功能

旧 Web 页面常把“电子签名”表现成一个按钮，但背后至少有七个问题：

```text
IDENTITY       谁？
INTENT         是否同意？
CONTENT        同意哪一版？
INTEGRITY      签后有没有改？
TIME           何时签？
DELIVERY       对方是否收到？
CUSTODY        双方以后还能否调取？
```

因此：

**`SIGN button clicked != all signature functions satisfied`**。

---

## 4. 基础 transaction state machine

### 4.1 合同展示与签署

```text
CONTRACT_DRAFT_EXISTS
→ CONTRACT_VERSION_FROZEN?
→ PAGE/CLIENT_LOADS
→ USER_AUTHENTICATED
→ SIGNING_CREDENTIAL_AVAILABLE
→ USER_SHOWN_CONTRACT
→ USER_EXPRESSES_INTENT
→ SIGNATURE_GENERATED
→ SIGNED_DATA_SUBMITTED
→ SERVER_RECEIVES
→ SIGNATURE_VALIDATED
→ COUNTERPARTY_ACCEPTS / SIGNS
→ COMPLETED_CONTRACT_STORED
→ PARTY_NOTIFIED
→ PARTY_CAN_RETRIEVE
→ REAL-WORLD PERFORMANCE
```

每个箭头都可能失败。

### 4.2 CA / certificate chain

```text
REAL PERSON / ORGANIZATION
→ IDENTITY PROOF
→ CERTIFICATE APPLICATION
→ CA / RA APPROVAL
→ CERTIFICATE ISSUED
→ PRIVATE KEY DELIVERED / GENERATED
→ PRIVATE KEY CONTROLLED BY SIGNER?
→ SIGNATURE CREATED
→ CERTIFICATE VALID AT SIGNING TIME?
→ RELYING PARTY VALIDATES
```

因此：

**`certificate issued != private key controlled by named person at the relevant moment`**。

### 4.3 合同保管

```text
SIGNED OBJECT CREATED
→ SERVER STORES
→ USER ACCOUNT LINKS TO OBJECT
→ DOWNLOAD AVAILABLE?
→ LOCAL COPY SAVED?
→ PLATFORM/ACCOUNT SURVIVES
→ YEARS LATER RETRIEVAL
→ YEARS LATER VERIFICATION
```

因此：

**`stored today != retrievable after account closure`**。

---

## 5. 2004—2005：法律与认证基础设施出现，但不能跳到大众使用

### Claim 5.1 — 2005-04-01 起，中国电子签名法正式施行

《中华人民共和国电子签名法》2004-08-28 通过，2005-04-01 施行。法律定义电子签名和数据电文，并规定当事人约定使用电子签名/数据电文的文书，不得仅因电子形式否定法律效力；可靠电子签名还要求签名制作数据专有、签署时由签名人控制、签名改动可发现、数据电文改动可发现。

Source:
- 中央网信办，《中华人民共和国电子签名法》: https://www.cac.gov.cn/2004-08/28/c_126468489.htm

**Grade:** A — 法律文本内容证据。

**Does not prove:**
- 普通用户已经有证书；
- 普通浏览器已经能签；
- 对方机构接受；
- 任意电子签名图片都可靠；
- 2005 年大众合同已无纸化。

### Claim 5.2 — 电子认证服务被作为第三方公众服务管理

2005 年《电子认证服务管理办法》把电子认证服务定义为为电子签名相关各方提供真实性、可靠性验证的公众服务，并规定第三方电子认证服务机构的管理框架。

Source:
- 司法部转载《电子认证服务管理办法》，2005-04-12: https://www.moj.gov.cn/pub/sfbgw/flfggz/flfggzbmgz/200504/t20050412_143906.html

**Grade:** A。

### Claim 5.3 — `www.esca.cn` 在同期媒体中作为安全电子印章系统地址出现

2005 年同期报道回溯称，中国电子商务协会等在 2004-11-09 推出安全电子印章系统，并给出 `www.esca.cn` 地址；同类报道还讨论了电子合同示范签署。

**Grade:** B — 同期媒体/行业报道。

**Important:**

`media mentions host != historical capture verified`。

本轮没有获得该 host 2004—2006 的可核验 memento，不能据媒体文字重建主页 DOM、charset、表单或客户端要求。

---

## 6. 2005 同期材料：最有价值的是“不确定性”，而不是“第一份”宣传

2005-04-01 生效当天，潘石屹参与了电子合同展示签署。同期《互联网周刊》报道明确承认活动存在较强展示意味，同时记录了签署者的几个问题：

- 是否可以和银行签文件；
- 密码被破解怎么办；
- 电子签章丢失怎么办；
- 未来能否和购房者、建筑商、银行普遍使用。

Source:
- 《电子签名：告别纸上谈兵》，2005-05-11: https://finance.sina.com.cn/chanjing/b/20050511/16411578910.shtml

**Grade:** B — 同期行业报道。

这比“电子签名第一人”更重要，因为它证明：

```text
LEGAL VALIDITY OPENED
but
USER TRUST / KEY CUSTODY / COUNTERPARTY ACCEPTANCE / COST
still unresolved
```

同一报道还写到部分电商企业受成本等因素影响仍在观望。

所以：

**`law effective != market normalized`**。

---

## 7. 浏览器环境：数字签名可能比普通 Web 表单更依赖本机状态

Microsoft 今天仍托管的 InfoPath Forms Server 2007 legacy 帮助页说明，浏览器中的数字签名要求支持 ActiveX，因此要使用 Windows Internet Explorer；首次签署还要安装并启用两个 ActiveX add-on，然后选择 certificate 才能签。

Source:
- Microsoft Support, `Add a digital signature to a browser-enabled form`: https://support.microsoft.com/en-US/infopath/add-a-digital-signature-to-a-browser-enabled-form

**Grade:** A/B — 官方 legacy 产品技术文档；不是历史页面 capture。

这给中文旧网电子签名考古提供了一个非常重要的 browser assumption：

```text
HTML shell survives
≠ signing control survives
≠ ActiveX can install
≠ certificate store exists
≠ private key exists
≠ historical transaction can be replayed
```

### 7.1 需要记录的本机依赖

- Windows 版本；
- IE 版本；
- ActiveX 安全策略；
- trusted-site 配置；
- 插件/控件版本；
- CA 根证书；
- USBKey 驱动；
- 本地证书库；
- 私钥介质；
- 签名算法/证书有效期；
- TLS/HTTPS 兼容性。

### 7.2 旧 Web capture 最容易制造的错觉

如果 Wayback 以后能打开一个“电子合同签署页面”，现代 Chromium 看到的很可能只是：

- 表单壳；
- 已失效脚本；
- 缺失 ActiveX object；
- 已被 archive rewrite 的 URL；
- 不存在的服务端 session。

因此不能截图后写“历史签约流程已复原”。

---

## 8. “网签”必须和电子签名分离

2008 年北京存量房交易“网签”同期材料显示，服务窗口仍可帮助买卖双方办理网上签约，首日现场甚至有大量柜台等待办理。

这类材料说明：

```text
ONLINE FILING / CONTRACT GENERATION
can coexist with
PHYSICAL COUNTER + PAPER SIGNATURE
```

所以旧网页里出现“网上签约”“网签合同”，不能直接推断：

- 用户在家完成；
- 使用数字证书；
- 使用可靠电子签名；
- 签署双方不见面。

本仓已有：

- `docs/HOUSING_INVENTORY_ONLINE_SIGNING_FILING_AND_OCCUPANCY_STATE_GAPS_2004_2015.md`

本专题只把住房“网签”当概念边界，不重复住房交易研究。

---

## 9. 必须区分 visual signature、手写轨迹与可靠电子签名

旧/中期 Web 和早期移动端会出现不同形式：

1. 上传扫描签字图片；
2. 在手写板/触控屏采集笔迹轨迹；
3. 账号密码确认；
4. SMS OTP；
5. CA certificate + private key；
6. USBKey；
7. 第三方平台把实名、意愿认证、文件 hash、时间记录组合成证据链。

它们不能仅因为页面上都显示一个“签名”图像而合并。

硬边界：

**`signature image copied into document != reliable electronic signature`**。

---

## 10. 2015：第三方电子签约云开始把“证据保管”当成产品卖点

2015 年关于互联网金融的同期报道指出，一些 P2P 交易完全在平台内完成，投资人没有纸质合同，一旦平台失效或数据被毁，用户可能缺乏足够交易证据；第三方电子合同厂商因此把身份识别、合同固化和第三方保管作为价值主张。

Source:
- 人民网转载《广州日报》，2015-04-27: https://finance.people.com.cn/money/n/2015/0427/c42877-26908888.html

**Grade:** B — 同期媒体+行业人士；不能把厂商主张当司法结果统计。

这里出现一个关键 state gap：

```text
TRANSACTION EXISTS ON PLATFORM
!= PARTY POSSESSES CONTRACT
!= THIRD PARTY PRESERVES EVIDENCE
!= COURT WILL ACCEPT EVERY ARTIFACT
```

### 10.1 2015 的未来想象：在线租房合同

2015 年上上签创始人在同期采访里用“和房东在线快速签合同”作为希望实现的典型场景，并承认网上签约本身当时仍没有真正发展起来。

Source:
- 新华网转载《新京报》，2015-10-08: https://www.xinhuanet.com/politics/2015-10/08/c_128294214.htm

**Grade:** B — 创业者/产品叙事。

这只能证明 2015 年该场景被公开想象/营销，不能证明租房电子签约已经成为常态。

---

## 11. 电子合同的 archive object 不是一个文件，而是一组相互依赖的状态

### 11.1 页面层

```text
contract URL
→ HTML
→ CSS/JS
→ login/session
→ contract data loaded
→ signing widget loaded
```

### 11.2 签署层

```text
credential
→ signer action
→ exact contract bytes/hash
→ signature value
→ timestamp/log
→ server receipt
```

### 11.3 证据层

```text
signed document
+ signer identity evidence
+ certificate
+ validation chain
+ signing time evidence
+ audit log
+ delivery evidence
```

### 11.4 履行层

```text
contract validly formed
→ goods/service/work/money actually performed
```

因此：

**`electronic contract exists != underlying obligation performed`**。

---

## 12. Archive preservation levels

建议以后对电子签名案例使用 E0—E5：

### E0 — shell only
只保存网站/签约入口 HTML。

### E1 — contract-view UI
可看到合同展示结构，但没有真实合同实例或 session。

### E2 — signing UI artifact
签署按钮、控件引用、JS/ActiveX object 等有残留。

### E3 — signed object
存在一份真实签署后的数据电文/PDF，但不一定能验证签名。

### E4 — verification-capable evidence
证书、签名值、必要链路足够，今天仍可独立验证至少部分签名属性。

### E5 — transaction evidence bundle
进一步保留身份、意愿、版本、签署、送达、双方保管等关键证据链。

普通 Web archive 多半停在 E0—E2。

E4/E5 常涉及私人合同与敏感身份数据，本仓原则上不应为了“完整”而重新公开。

---

## 13. 证书与长期验证的时间问题

一份 2008 年当时能验证的电子签名，到 2026 年不一定能在普通现代浏览器里直接重放：

- 证书可能已过期；
- CA 根证书可能更换；
- 算法可能被淘汰；
- CRL/OCSP 历史状态不易取得；
- 时间戳服务可能停止；
- 驱动/USBKey 已不存在；
- 客户端控件不可运行。

因此：

**`cannot verify today != signature was invalid then`**，

同时也有：

**`PDF opens today != signature remains verifiable`**。

任何 D 级长期验证复原都应说明证书时间、算法、信任根与 revocation 信息假设。

---

## 14. 合意必须和身份验证分开

电子签名系统很容易留下大量“这是这个人”的证据：

- 身份证；
- 实名手机号；
- 银行卡；
- 人脸；
- 设备；
- 微信账号；
- CA certificate。

但这些不能自动回答：

> **他是否在这个时点看到并同意了这一版合同？**

所以状态机必须同时有：

```text
IDENTITY_AUTHENTICATED
```

和

```text
INTENT_CONFIRMED_FOR_VERSION_X
```

二者不可合并。

这对后来的劳动合同争议尤其重要，虽然 2020s 已超出本仓主要时间范围；life-history companion 会继续追踪。

---

## 15. 用户可见状态和后端状态

一个典型旧 Web 页面可能显示：

- “签署成功”；
- “合同已生成”；
- “已认证”；
- “已发送”；
- “已存证”。

但每个 UI label 都必须继续问：

```text
UI says signed
→ signature bytes generated?
→ server received?
→ counterparty signed?
→ final version locked?
```

```text
UI says sent
→ notification generated?
→ SMS/email delivered?
→ recipient opened?
```

```text
UI says stored
→ which backend?
→ retention period?
→ user can export?
→ survives account closure?
```

所以：

**`front-end success state != final real-world state`**。

---

## 16. 浏览器兼容与“普通用户可及”不能省略

依据仓库 METHOD，一个电子签名产品即使：

- 有官方网站；
- 有证书服务；
- 有签约按钮；

也只能先证明 `exists`。

要写 `available` 至少还要问：

- 普通用户能否申请证书；
- 价格；
- 是否需要单位统一部署；
- 是否支持家用电脑；
- 是否只能 IE；
- 是否要管理员权限安装 ActiveX；
- 是否要 USBKey；
- CA/驱动是否容易取得；
- 对方机构是否接受。

要写 `used/popular` 还需要独立采用证据。

---

## 17. 隐私边界

真实电子合同几乎天然包含：

- 姓名；
- 身份证；
- 手机；
- 地址；
- 工资/价格；
- 银行信息；
- 签名；
- 合同内容；
- 企业/个人证书标识。

因此本仓应优先保存：

- 页面结构；
- URL pattern；
- 帮助文档；
- 控件/浏览器要求；
- 公开 demo；
- 法律与机构说明；
- 抽象 transaction state。

不要为了证明 E4/E5 批量重新公开普通人的历史合同。

---

## 18. 本轮 archive attempt

### Target A
`www.esca.cn`，2004—2006。

理由：同期 2005 媒体把该 host 与 2004 年安全电子印章系统联系起来，是一个值得后续验证的 early Chinese e-signature Web artifact candidate。

本轮操作：

1. 公开 Web 搜索 `esca.cn` + 2004/2005 + 电子印章；
2. 搜索 `site:web.archive.org` / `web.archive.org` 组合；
3. 尝试直接构造 Wayback CDX 查询 2004—2006 HTML capture。

结果：

- 同期媒体能证明 host 字符串作为服务地址被报道；
- 普通搜索没有返回可直接核验的 historical replay；
- 当前 Web 工具拒绝直接打开自行构造的 CDX URL，理由为安全 URL 限制；
- 未取得 `capture_datetime / original_url / HTTP / charset / DOM / form action / subresources / ActiveX reference`。

因此：

**`M1 verified capture: NOT ACHIEVED IN THIS SLICE`**。

这只表示本轮没有验证到，不表示 Wayback、Common Crawl 或其他档案没有保存。

---

## 19. Hard boundaries for future work

以后任何电子签名/合同案例至少保留以下边界：

```text
visual signature image != digital signature
```

```text
certificate issued != signer controlled private key at signing
```

```text
real-name authentication != informed/voluntary consent
```

```text
contract displayed != exact version signed
```

```text
sign button clicked != signature generated
```

```text
signature generated != server received
```

```text
server received != counterparty accepted
```

```text
online signing / 网签 != reliable cryptographic e-signature
```

```text
contract stored != each party can retrieve later
```

```text
PDF survives != signature remains independently verifiable
```

```text
historical signing page capture != historical signing transaction capture
```

```text
valid electronic contract != underlying real-world performance
```

---

## 20. Evidence table

| Claim | Evidence | Grade | Confidence | Boundary |
|---|---|---:|---:|---|
| 2005-04-01 电子签名法施行 | 官方法律文本 | A | high | 法律存在 ≠ 大众采用 |
| 2005 电子认证服务进入许可/监管框架 | 部门规章 | A | high | CA 制度 ≠ 用户已持证 |
| `www.esca.cn` 被同期报道为安全电子印章地址 | 同期媒体 | B | medium-high | host mention ≠ capture |
| 2005 展示签约参与者公开讨论密码/签章丢失与未来应用 | 同期行业报道 | B | high | elite demo ≠ ordinary use |
| 同期企业仍因成本等因素观望 | 同一行业报道 | B | medium | 单一行业观察 ≠ 全国规模统计 |
| InfoPath 2007 browser signing 依赖 IE/ActiveX/add-ons | Microsoft legacy 官方文档 | A/B | high | 技术要求 ≠ 中文站点都采用该栈 |
| 2015 P2P 出现电子合同/第三方存证需求 | 同期媒体/行业人士 | B | medium-high | 产品主张 ≠ 司法采信率 |
| 2015 在线租房签约被创业者作为目标场景 | 同期采访 | B | high | future imagination ≠ adoption |

---

## 21. Unknowns / next probes

1. `esca.cn` 2004—2006 是否有可核验 Wayback/Common Crawl/WARC capture？
2. 早期安全电子印章系统的真实浏览器要求、charset、控件、证书申请流程是什么？
3. 是否存在可公开、无隐私风险的 early demo signed-object，可做 E3/E4 验证？
4. 2005—2010 中国主要 CA 面向普通个人的证书费用、申请步骤与 USBKey 要求如何？
5. 哪些签约系统明确要求 IE6/ActiveX，哪些使用 Java/独立客户端？
6. 历史证书链、CRL/OCSP、时间戳能否保存到足以验证 old signed artifact？
7. 2010—2015 移动浏览器/手机签署怎样减少 PC 控件依赖？
8. 用户签完以后能否下载一份独立合同，还是只能登录平台查看？
9. “网签”这个词在住房、劳动、金融、电商中分别代表了哪些完全不同的 transaction？

---

## 22. 这改变了什么旧网理解

旧 Web 的“事务页面”通常被我们想象成：

```text
页面还在不在？
表单能不能提交？
```

电子签名证明这还不够。

一个页面即使 HTML、CSS、按钮和合同文字都被完整保存，真正让它成为“签约基础设施”的东西仍可能全部消失：

> 证书、私钥、ActiveX、CA 信任链、服务器 session、签名值、时间记录、双方账号以及最后的合同对象。

因此电子签名是中文旧网考古里最典型的一类**事务深层对象**：

**页面只是最外层壳，现实承诺发生在 archive 最难保存的状态之间。**