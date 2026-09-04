# ONLINE BANKING / REMITTANCE / PAYMENT STATE GAPS, 1997–2015

Status: research note / state-gap model  
Scope: 约 1997–2015 中文 Web 中个人网银、网上汇款、跨行账户管理与支付控制面的技术状态、授权状态、浏览器/安全介质依赖、后台清算与 archive blind spots；**不把本仓扩展成全球支付史或 2015 年后的移动支付史**。  
Cross-repo companion: `tmzncty/how-people-lived/topics/money-across-distance-remittance-family-support-and-financial-reachability-china-1980-2026.zh-CN.md`  
Last research pass: 2026-09-05

---

## 0. Why payment pages are a special old-web object

一个普通旧网页常常可以近似成：

```text
URL
→ HTML
→ CSS / images / JS
→ rendered page
```

个人网银与网上支付完全不能这样处理。

一个“转账汇款”页面背后至少可能有：

```text
public bank site
→ customer identity
→ bank account
→ e-banking enrollment
→ signed / non-signed customer state
→ security mode
→ certificate / U盾 / token
→ browser + OS + driver
→ login session
→ payee / recipient
→ amount / fee / limit
→ transfer form
→ signature / OTP
→ bank acceptance
→ interbank clearing
→ recipient-bank posting
→ recipient account usable
→ cash-out / spending
→ human confirmation
```

公共 Web 档案最容易保存的，恰恰主要是这个链条最外侧的：

- 产品介绍；
- 登录页；
- 安全说明；
- 驱动下载页；
- 公告；
- 帮助文档。

最重要的生活状态——谁转给谁、转了多少、银行是否真正受理、对方是否到账、钱后来是否被取出——本来就应被身份验证与金融隐私挡在公共 archive 之外。

因此本 note 的核心命题是：

> **control surface survives far better than transaction state.**

这和 companion life-history note 的发现直接对应：

> 普通人的资金越来越能跨距离流动，但 archive 通常保存“如何操作”的外壳，无法直接保存一个家庭真实的钱路。

---

## 1. Evidence contract

遵循 `docs/METHOD.md`。

### 1.1 Research units

必须分别记录：

- `bank_or_payment_platform`
- `public_site_or_host`
- `product_page`
- `help_page`
- `login_page`
- `customer_account_state`
- `security_credential_state`
- `browser_environment`
- `private_session`
- `transfer_request`
- `clearing_state`
- `recipient_posting_state`
- `capture`
- `claim`

不能把：

```text
“工行网银存在”
```

和：

```text
“某用户在某台 Windows XP + IE6 机器上持有效 U盾，并在当晚成功把 500 元转到另一银行、收款人当天能取现”
```

写成同一层事实。

### 1.2 Evidence grades in this note

- **A**：银行/监管机构当年官方公告、帮助页、业务规则；
- **B**：同期媒体实测、用户教程、技术问题帖；
- **C**：后来回忆/企业历史；
- **D**：研究者根据残存资料推断的状态链。

Current live official page carrying an old publication date can be strong evidence for the text the institution currently preserves, but it is **not automatically a historical memento**.

### 1.3 Privacy stop condition

不得为了 old-web 考古：

- 测试历史银行卡号；
- 尝试登录旧账户；
- 复用泄露 cookie/session；
- 重放真实转账；
- 重新公开普通人的交易流水、收款人、余额或身份证件信息；
- 把私人银行截图当作公共数据集批量收集。

本仓研究产品和页面结构，不研究普通人的可识别金融隐私。

---

## 2. 1997–1998：银行网站先从“看账户”走向“动账户”

2000 年《人民日报》回顾当时近年的网上银行发展时记录：

- 招商银行 1997 年网站已经提供“一卡通”账务查询等功能；
- 1998 年“一网通”进一步支持网上支付。

Near-contemporary source:
- 《人民日报》2000-11-21，《网上银行“轻骑兵”》：
  https://cn.govopendata.com/renminribao/2000/11/21/11/

Evidence grade:
- B+：近同时代国家报纸回顾；用于功能时间线，不用于猜具体 DOM。

这一步最需要避免的错误是：

```text
account information visible on Web
≠
funds movable on Web
```

因此增加：

## **query / transaction capability gap**

一个银行 Web 系统可以先支持：

- 余额；
- 明细；
- 利率/产品信息；

却仍不允许该用户从浏览器发起高风险资金转移。

“网上银行”这个品牌名本身不能作为统一 capability label。

---

## 3. 2003–2008：远程转账建立在一串本地授权与客户端状态上

### 3.1 U盾：Web page is only one component

中国工商银行 2007 年官方 U盾材料明确描述 U盾作为网上银行数字认证/电子签名安全介质，并提供不同厂商型号与价格；同一时期官方操作说明把申请、证书与客户端环境连接到网银转账流程。

Official source:
- 中国工商银行，2007 年 U盾官方说明：
  https://www.icbc.com.cn/icbc/html/guanggao/2007nian/0801Udunjgqmxt/sy_Udunjgqmxt_070801.htm

Evidence grade:
- A：current official host preserves a page explicitly dated/structured as a 2007 document；不是本轮实际验证过的 2007 archive capture。

对于 old-web 考古，最重要的不是 U盾用了哪种算法，而是页面行为依赖：

```text
physical enrollment
→ security medium issued
→ correct driver installed
→ certificate provisioned
→ browser can call component
→ private login session
→ signing action
```

因此增加：

## **branch-enrollment gap**

`online feature exists` 不证明用户可以不去实体营业网点就获得资格。

以及：

## **credential-medium gap**

`customer has online-banking account` 不证明：

- 已领取 U盾；
- U盾仍在本人手中；
- PIN 未锁；
- 证书仍有效；
- 当前交易必须/允许使用这一介质。

### 3.2 Driver/browser/OS is part of transaction history

2007 年同期技术博客留下了 Vista / IE7 与工行华虹 U盾兼容问题：用户描述拿到 U盾后长时间无法正常安装使用，并提到支持建议仍可能要求 XP / IE6。

Contemporary user technical evidence:
- 博客园，2007-08-11，《工行华虹U盾在Vista和IE7下的解决方案》：
  https://www.cnblogs.com/xdotnet/archive/2007/08/11/icbc_u.html

Evidence grade:
- B：同时代用户操作/技术问题；不能代表所有 U盾型号与用户。

这给 M3 浏览环境路线增加一个非常强的对象：

## **security-device / browser-environment gap**

现代浏览器打开 2007 的银行帮助页成功，完全不能证明 2007 的真实高风险交易控件能在现代环境中工作；反过来，历史用户看到同一个“登录/转账”入口，也不代表其 OS、浏览器、ActiveX/驱动组合能够通过签名步骤。

建议未来浏览器实验把这类页面列入候选，但**绝不进行真实交易**。

---

## 4. 2008：安全政策升级会让“昨天还能转”的账户今天突然只能看

中国建设银行上海市分行 2008-06-05 公告明确说，从 2008-06-14 起：

- 停止软文件证书客户的转账汇款；
- 停止软文件证书客户的网上支付；
- 停止非签约客户的网上支付；
- 同时提供动态口令卡/UKey 升级路径。

Official contemporary source:
- 中国建设银行上海市分行，2008-06-05：
  https://ccb.com/chn/2008-06/05/article_2021122311295217225.shtml

Evidence grade:
- A：官方公告，明确发布日期与生效日期。

这是一条非常重要的 old-web state rule：

> **account existence ≠ authorization continuity**

同一用户、同一账号、同一站点 URL，交易 capability 可以因安全政策切换而变化。

因此新增：

## **security-policy-version gap**

必须记录：

```yaml
policy_effective_from:
customer_security_mode:
signed_state:
transaction_type:
limit_state:
```

不能把 2008-06-13 和 2008-06-14 当成同一 capability state。

---

## 5. A transaction page needs more clocks than a normal article page

银行页面至少可能涉及：

```text
page_published_at
policy_effective_at
security_certificate_issued_at
certificate_expires_at
login_session_started_at
transfer_submitted_at
bank_accepted_at
clearing_at
recipient_posted_at
capture_at
current_live_render_at
```

因此一个 2008 公告页面今天仍活着，不意味着：

- 当年同一个 host/path 一直不变；
- 当年 CSS/JS/charset 与今天相同；
- 相关登录 endpoint 仍存在；
- 旧证书/控件还能执行；
- 当前银行规则可倒推回 2008。

新增：

## **policy-time / interface-time divergence**

政策文本可以保存得非常好，而执行该政策的登录页与安全组件已经完全换代。

---

## 6. 2010 “超级网银”：统一后台并不等于用户看到一个真正统一的网站

2010-08-30，人民银行网上支付跨行清算系统上线。同期报道描述其目标是把不同商业银行网银端口连接起来，让个人/企业通过既有网银界面进行跨行账户查询和资金汇划。

Sources:
- 2010-08-31 新华社稿转载：
  https://news.sina.com.cn/o/2010-08-31/051018043272s.shtml
- 中国互联网协会，2010-09-13，《“超级网银”11月全线运行手把手教你使用》：
  https://www.isc.org.cn/article/9093.html

Evidence grade:
- B+：同期机构/新闻材料。

### 6.1 “one entrance” still depended on bank-side consent/enrollment

中国互联网协会同期操作稿明确说：

- 用户只登录一家网银即可进行跨行查询/转账；
- 但跨行账户查询等服务仍需先到相关银行网点签订协议；
- 设计目标之一是减少多家银行 U盾和客户端软件的重复安装。

因此增加：

## **cross-bank consent gap**

```text
central clearing system online
≠
my other bank account has been authorized for this portal
```

### 6.2 unified backend ≠ unified discoverability

2010-12-21《上海青年报》调查发现：

- 很多用户不知道“超级网银”是什么、从哪里登录；
- 并没有一个面向个人的统一“超级网银官网入口”；
- 不同银行把它叫作“互联账户管理”“他行账户服务”“网银互联账户”等不同名字。

Source:
- 中新网转载《上海青年报》，2010-12-21：
  https://www.chinanews.com/fortune/2010/12-21/2734954.shtml

Evidence grade:
- B：同期用户/页面体验调查。

因此增加：

## **backend-unification / front-end-fragmentation gap**

后端基础设施可以统一，而 Web 导航、品牌命名和用户入口仍高度碎片化。

这也是 old-web archaeology 很容易误判的地方：

> 搜不到一张标题叫“超级网银”的统一首页，不等于 2010 年没有超级网银系统。

反过来，银行页面出现“互联账户管理”也需要独立证据才能确认它具体接入哪一代后台与哪些功能。

### 6.3 launch ≠ stable availability

2010-09-03 同期记者实测又发现，多家银行上线初期规则不同，部分签约页面无法正常跳转，客服甚至建议暂时不要使用。

Source:
- 中国新闻网稿转载，2010-09-03：
  https://news.sohu.com/20100903/n274684313.shtml

Evidence grade:
- B：同期操作实测。

因此：

## **system-launch / user-executable gap**

一个支付清算系统在官方层面“上线”不等于所有接入银行、所有客户、所有浏览器路径当天都实际可执行。

---

## 7. Core transfer state machine

研究 1997–2015 网上银行/汇款页面时，至少使用以下链：

```text
bank public site exists
→ online-banking product exists
→ customer has bank account
→ customer is eligible for online banking
→ enrollment completed
→ signed / non-signed state established
→ security credential issued
→ required driver/control installed
→ credential valid
→ login succeeds
→ session remains valid
→ recipient/payee entered
→ bank/branch/account identifiers validate
→ amount entered
→ fee/limit calculated
→ transfer request submitted
→ password/OTP/signature validates
→ bank accepts request
→ sending balance debited/held
→ interbank clearing succeeds
→ recipient bank posts funds
→ funds are actually available
→ recipient notices
→ recipient withdraws/spends
→ intended offline purpose occurs
```

Public Web artifacts overwhelmingly document only some arrows before `bank accepts request`.

---

## 8. New state gaps

### 8.1 product-page / eligibility gap

Public page advertising transfer capability does not prove this account type/customer was eligible.

### 8.2 branch-enrollment gap

Remote execution can depend on one-time or repeated physical branch enrollment.

### 8.3 signed / non-signed customer gap

A single bank can expose different capabilities based on whether the customer completed additional signing/verification.

### 8.4 credential-medium gap

Soft certificate, dynamic-password card, UKey/U盾 and later SMS/OTP are distinct authorization states.

### 8.5 driver/browser/OS gap

A security device may require a specific driver, browser or control; modern rendering does not reconstruct historical executability.

### 8.6 certificate-provisioning gap

A device being present does not prove certificate download/issuance completed.

### 8.7 certificate-validity gap

A historical screenshot of “certificate installed” does not establish certificate validity at another date.

### 8.8 security-policy-version gap

The same credential can lose transaction privileges after a policy cutover.

### 8.9 private-session gap

The authenticated session is usually inaccessible to public web archives by design.

### 8.10 transaction-form gap

Public help pages may show fields while the real private form, validation rules and server response remain unarchived.

### 8.11 transfer-submit / bank-acceptance gap

Client-side success or form submission is not the same as bank acceptance.

### 8.12 acceptance / clearing gap

Sending bank acceptance does not prove cross-bank settlement completed.

### 8.13 clearing / recipient-posting gap

Clearing-system completion does not automatically prove the recipient account has posted usable funds at the observed instant.

### 8.14 posting / cash-out gap

A balance can be credited while recipient still lacks immediate cash access because of branch hours, card/account state or withdrawal constraints.

### 8.15 receipt / human-notice gap

SMS/page confirmation does not prove the intended recipient noticed the payment.

### 8.16 human-notice / offline-purpose gap

Receiving money does not prove it was used for school fees, medical care, rent, family support or any claimed life outcome.

### 8.17 fee-version gap

Transfer fees can depend on date, channel, customer grade, amount and bank pair. A later fee table cannot be applied retroactively.

### 8.18 limit-version gap

Daily/single-transfer limits are policy state, not timeless product attributes.

### 8.19 payee-identity gap

The account number/name on a form is not necessarily evidence of who ultimately controlled the funds in household practice.

### 8.20 cross-bank-consent gap

Backend connectivity does not establish that a particular customer authorized account linkage.

### 8.21 backend-unification / front-end-fragmentation gap

One clearing platform can appear under many bank-specific UI labels.

### 8.22 system-launch / user-executable gap

Official launch date and successful ordinary-user execution date need not match.

### 8.23 control-surface / private-state asymmetry

Public archive survival is structurally biased toward:

```text
brand
help
FAQ
login shell
security manual
product announcement
```

and away from:

```text
customer state
balance
payee list
transaction
clearing state
recipient outcome
```

### 8.24 current-official-page / historical-capture gap

A current bank host that preserves a 2007 or 2008 document is valuable evidence of institutional memory, but it does not establish original 2007 HTML/CSS/headers/subresources.

### 8.25 branded-portal continuity gap

A bank may preserve brand names while changing:

- hostname;
- path;
- JSP/ASP structure;
- login architecture;
- authentication product;
- browser support;
- backend payment rail.

Brand continuity is not technical continuity.

---

## 9. Archive reconnaissance: candidate ICBC 2007 locator found, but not verified as a replayable capture

本轮检查 `mybank.icbc.com.cn` 的 archive locator。

Archive.is 的 host index currently lists an entry labelled:

```text
20 Jul 2007 20:21
ICBC New Generation of Internet Banking
https://mybank.icbc.com.cn/icbc/enperbank/index.jsp
archived via:
http://web.archive.org/web/20070720202123/https://mybank.icbc.com.cn/icbc/enperbank/index.jsp
```

Locator:
- https://archive.is/mybank.icbc.com.cn

This is useful evidence that a historical capture candidate exists.

However, in this research pass, attempts to actually open and inspect the referenced Wayback memento did **not** yield a verified replayable artifact.

Therefore, per `docs/METHOD.md`:

```text
archive locator found
≠
verified capture
```

Status:

```yaml
candidate_original_url: https://mybank.icbc.com.cn/icbc/enperbank/index.jsp
candidate_capture_datetime: 2007-07-20T20:21:23
archive_locator_seen: true
memento_opened_and_inspected: false
historical_dom_verified: false
historical_charset_verified: false
subresources_verified: false
login_endpoint_verified: false
```

此外，这个 locator 标题是英文 `ICBC New Generation of Internet Banking`；即使未来 capture 能打开，也不能单独替代对中文个人网银入口的研究。

### Negative result

本轮因此**没有**声称恢复：

- 2007 中文工行网银原始 DOM；
- charset；
- frameset；
- login form method/action；
- cookie/session names；
- ActiveX object IDs；
- U盾控件调用路径；
- transaction endpoint；
- 真实账户后的页面。

这些保持 unknown。

---

## 10. Why historical screenshots of “success” are dangerous

支付页面特别容易产生过度推断。

一个截图如果写：

```text
交易提交成功
```

最多证明：

> 某个页面/客户端当时呈现了一个 success-looking state。

它不自动证明：

```text
server accepted exactly one request
→ amount debited
→ interbank clearing completed
→ recipient account credited
→ recipient had access
→ intended person controlled account
→ cash was withdrawn
→ offline purpose happened
```

而 screenshot 本身还可能缺：

- URL；
- capture time；
- account masking rules；
- preceding request；
- whether it is demo/training environment；
- whether user later reversed/cancelled transaction。

因此 payment archaeology 应比普通页面更谨慎地使用“成功”一词。

---

## 11. Browser reconstruction boundaries

一个未来可做的安全实验可以比较：

- modern Chromium；
- Windows XP + IE6 级环境；
- Vista + IE7 级环境；
- 不安装历史银行控件；
- 只使用公开帮助页/静态 artifact。

实验问题：

1. 旧帮助页是否仍完整渲染？
2. 驱动下载 URL 是否存活？
3. JS/browser sniffing 是否阻止现代环境？
4. 是否残留 ActiveX/Object 标签？
5. encoding 是否因 archive rewrite 改变？
6. 公共页面中有哪些链接一点击就进入不应重放的 authenticated area？

### Hard stop

实验不得：

- 使用真实历史账号；
- 导入真实证书；
- 尝试绕过登录；
- 提交转账；
- 请求真实余额；
- 利用失效安全组件漏洞。

我们的目标是复原**界面依赖与解释差异**，不是复活金融授权。

---

## 12. Historical-visibility model

网上银行与支付是一个特别典型的 “public shell / private life” 系统。

### Public and relatively archivable

- bank homepage；
- product introduction；
- fees；
- security announcement；
- U盾 advertisement/manual；
- driver-download catalog；
- outage notice；
- cross-bank service introduction。

### Private and structurally dark

- whether a particular migrant worker enrolled；
- who in a household held the U盾；
- whether sister managed brothers' wages；
- saved payees；
- actual transfer frequency；
- failed attempts；
- balance；
- refund/reversal；
- recipient posting latency；
- whether money paid tuition/medical bills；
- whether a parent still relied on cash withdrawal。

因此 old-web 的 archive record 会系统性地夸大：

> **what the service could theoretically do**

相对于：

> **what ordinary households actually managed to do.**

这不是 archive 的失败，而是金融隐私与认证设计的必然结果。

---

## 13. Cross-repo interpretation boundary

`old-web-archaeology` 只负责 1997–2015 中文 Web 技术与保存问题：

- 银行网站；
- 登录/帮助/公告；
- 浏览器；
- 安全介质；
- archive；
- 后台/前台状态边界。

以下内容主要留在 `how-people-lived` companion：

- 1980s 邮政/银行汇兑前史；
- 2001 电子邮政汇款；
- 农民工银行卡与农村最后一公里；
- 家庭谁负责汇款；
- 父母对子女反向支持；
- 2018+ 亲属卡；
- 2019 农村小店移动支付代理；
- 2020+ payment fallback；
- 2023+ 应急现金缓冲；
- M-PESA 全球比较。

这样可以避免把本仓从“中文旧网考古”无限扩成通用金融史。

---

## 14. Confirmed / probable / unknown

### Confirmed

- 1997–1998 前后中国商业银行 Web 已从账户查询向网上支付扩展（近同时代报道）；
- 2007 工行公开推广 U盾作为网银安全认证/签名介质；
- 2007 同期用户遇到 Vista/IE7 与特定 U盾环境兼容问题；
- 2008 建行上海明确切断软文件证书客户的转账/网上支付能力；
- 2010 网上支付跨行清算系统上线；
- 2010 同期资料仍要求部分跨行服务先到银行签约；
- 2010 各行 UI 名称/入口并不统一；
- 2010 上线初期存在普通用户无法稳定执行某些签约路径的同期实测；
- archive locator currently exposes a candidate ICBC 2007 memento reference。

### Probable / strongly inferred

- 一名 ordinary user 的远程汇款 capability 经常是 `bank account + enrollment + security device + local software + browser + current policy + session` 的组合状态；
- payment old-web preservation 比普通论坛/文章更偏向 control surface；
- historical transaction outcome requires non-Web evidence such as statements, receipts, diary/interview or institution logs。

### Unknown this pass

- 2007 中文工行个人网银的可验证历史 DOM；
- exact charset / frameset / object IDs；
- historical login form action；
- original driver binaries and hashes；
- whether archive captured authenticated post-login resources at all；
- exact per-bank U盾/security-policy transitions across all years；
- exact public URL lineage for CMB 1997/1998 online-payment entry；
- transaction-level settlement latency for ordinary family remittance cases。

---

## 15. Evidence table

| Object / time | Evidence | Grade | What it supports | What it does not support |
|---|---|---:|---|---|
| CMB 1997–1998 | People’s Daily 2000 retrospective | B+ | query → online-payment early timeline | original DOM/URL/charset |
| ICBC U盾 2007 | ICBC official dated page | A | security medium existed, promoted, technical role | original 2007 HTTP/capture state |
| Vista/IE7 U盾 2007 | contemporaneous user blog | B | real compatibility friction existed for one setup | prevalence across all users/models |
| CCB soft-cert cutoff 2008 | CCB Shanghai official notice | A | policy changed transaction capability on exact date | every user’s migration success |
| cross-bank clearing 2010 | PBOC/Xinhua/ISC reporting | B+/A-adjacent | system launch and intended function | universal user availability on launch day |
| bank agreement requirement 2010 | ISC operation article | B+ | some services still required branch agreement | every bank identical |
| fragmented UI 2010 | Shanghai Youth / CNS | B | users faced naming/discoverability fragmentation | backend absence |
| unstable initial use 2010 | CNS contemporaneous test | B | launch did not guarantee stable user execution | permanent failure |
| ICBC 2007 archive locator | archive.is index referencing Wayback | locator only | candidate capture metadata | verified historical capture |

---

## 16. New vocabulary for the repository

### query / transaction capability gap
能看账户不等于能动账户。

### branch-enrollment gap
Web 远程操作可能依赖先在线下建立授权。

### credential-medium gap
账户存在不等于当前持有可用安全介质。

### security-device / browser-environment gap
网页与安全控件可能依赖不同历史客户端环境。

### security-policy-version gap
同一账户/介质的权限会随政策日期变化。

### policy-time / interface-time divergence
政策文本状态与可执行 UI/组件状态拥有不同时间线。

### cross-bank consent gap
后台已互联不等于用户已授权跨行账户关系。

### backend-unification / front-end-fragmentation gap
统一清算层可以呈现为许多不统一的银行 UI。

### system-launch / user-executable gap
“正式上线”不是每个普通用户“当天可用”的同义词。

### transfer-submit / bank-acceptance gap
浏览器提交不是银行最终受理。

### acceptance / clearing / posting / usability gaps
一次转账的银行后端结果必须拆成多个状态。

### control-surface / private-state asymmetry
公共控制面容易保存，私人金融状态系统性不可见。

### current-official-page / historical-capture gap
官方当前站保留旧文档不等于有历史时点 memento。

---

## 17. What this changes in old-web archaeology

此前旧网研究很容易把金融页面当成：

> “又一种老网站/老 Web UI”。

本轮以后应把它视为一种特殊对象：

> **一个公开 HTML 控制面只露出一小部分状态，而真正改变现实世界的钱流隐藏在认证、客户端安全介质、银行后台与清算网络中。**

这意味着：

1. HTML 保存得非常完整，也可能仍无法复原“能不能转账”；
2. browser environment 不再只是视觉问题，还可能决定安全控件能不能执行；
3. policy date 必须和 page/capture date 分开；
4. “成功页”比普通文章页更不能被当成现实结果；
5. 交易层不可保存并不等于历史研究失败——需要与报纸、账单、用户访谈、制度材料交叉；
6. 金融隐私正是 archive blank spot 的合理原因之一。

---

## 18. Next high-value artifact

下一步最值得找的是一份**可实际打开验证**的 1998–2008 中文个人网银 public capture，最好能同时保存：

```text
homepage / product page
login shell
security help
browser requirement
U盾/证书 instructions
driver download page
fee / limit table
```

并且记录：

- original URL；
- archive source；
- capture datetime；
- charset；
- frameset/DOM；
- JS；
- ActiveX/Object dependency；
- resource failures；
- redirect chain；
- browser assumptions。

目标仍然不是进入真实账户。

最理想的成果是复原：

> **2007 年一个普通人坐在家里的 Windows XP/IE 电脑前，理论上要具备哪些本地条件，才能从一个公开银行网站走到“可以发起转账”的门口；而从那个门口以后，哪些私人状态我们原则上就不应该、也几乎不可能从公共 Web archive 恢复。**
