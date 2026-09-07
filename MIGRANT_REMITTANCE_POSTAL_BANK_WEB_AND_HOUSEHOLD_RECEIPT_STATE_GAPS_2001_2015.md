# MIGRANT_REMITTANCE_POSTAL_BANK_WEB_AND_HOUSEHOLD_RECEIPT_STATE_GAPS_2001_2015

## Scope

本说明研究约 **2001–2015 中文互联网与邮政/银行支付网络交界**中的一个此前没有单独建模的对象：

> 外出务工者怎样把工作地收入送到另一个地方的家庭；银行/邮政网站、网银、电话、实体网点、银行卡和跨行清算分别承担什么状态；以及“网上能汇”“银行已受理”“钱已到账”“家里拿到钱”为什么不能互相替代。

本仓仍然只研究中文旧网及其技术/事务边界。1990s 的迁移与邮政汇款前史、2015 以后移动支付与家庭迁移变化主要写入生活史 companion：

- `tmzncty/how-people-lived/topics/remitting-home-split-household-finance-migration-and-payment-rails-china-1995-2026.zh-CN.md`

海外 migrant remittance 比较也留在 `how-people-lived`，不把本仓扩成全球支付史。

---

# 1. 研究单位：不要把“汇款”当成一次网页提交

至少区分以下 state：

1. **income available**：工资是否真正支付给劳动者；
2. **sender funding state**：现金/账户余额是否可用于汇款；
3. **channel selected**：随身现金、邮政、银行柜台、银行卡、电话、Web 等；
4. **sender identity executable**：证件、银行卡、网银签约、证书/密码等是否可完成；
5. **instruction submitted**：柜台/网站是否接受汇款指令；
6. **payment rail accepted**：银行/邮政后台是否接纳交易；
7. **settlement/availability**：资金是否真正进入可兑付状态；
8. **receiver notified**：收款人是否知道钱可取、金额、汇款号/密码等；
9. **receiver identity executable**：证件、密码、卡、网点等条件是否满足；
10. **cash-out / account credit**：收款人是否真正拿到可用资金；
11. **household allocation**：资金是否用于学费、医疗、生活、建房、债务等；
12. **reversal/dispute state**：密码遗忘、退汇、错汇、未到账、投诉等是否解决。

核心规则：

```text
wage earned
≠ wage paid
≠ remittance instruction submitted
≠ transaction accepted
≠ funds settled
≠ receiver notified
≠ receiver can authenticate
≠ receiver obtained cash
≠ household expense was actually paid
```

旧 Web 页面最多经常只能保存其中一两个 surface。

---

# 2. 2001 边界：邮政电子汇款可以是“联网后台 + 线下现金”，不需要用户拥有 Internet

2001 年中国邮政推出电子汇款时，公开流程仍是普通人到邮局交现金，由邮政联网后台完成 24 小时兑付。同期报道说首批 20 个城市、106 个联网网点，资费仍为汇款额 1%，最低 2 元、最高 50 元。

Source:
- 中国青年报，《中国邮政开通电子汇款 现金汇款24小时可兑付》，2001-06-29：
  https://zqb.cyol.com/content/2001-06/29/content_250595.htm

Evidence grade: **B — contemporaneous press describing official service launch**.

### 对 old-web 的意义

这条材料要求我们在中文互联网史里区分：

```text
networked transaction backend
≠ Web frontend
≠ household Internet access
```

一个数字化程度很高的汇款系统完全可以没有给普通用户提供网页表单。

新增：

**backend-network / user-Web gap — 后台联网 / 用户 Web 缺口。**

不要因为 2001 已经“电子汇款”就推断当时存在可供普通用户浏览器执行的汇款页面。

---

# 3. 2005：服务存在也不等于用户会选择它

人民银行 2005 年农民工金融需求材料及 2006 年同期报道指出：由于成本、保密和便利等原因，很多农民工仍选择携带现金回家；即使汇款，也主要通过邮政汇款和邮政绿卡，银行卡汇款比例较低。

Sources:
- 中国青年报，《央行：农民工去年人均收入8520元》，2006-05-26：
  https://zqb.cyol.com/content/2006-05/26/content_1396641.htm
- 中国人民银行历史 PDF：
  https://www.pbc.gov.cn/eportal/fileDir/history_file/files/att_12732_1.pdf

Evidence grade: **A/B institutional + contemporaneous press**.

这给旧网研究增加一条 adoption rule：

```text
bank website advertises transfer
≠ worker has bank account/card
≠ worker signed up for e-banking
≠ worker trusts the channel
≠ home village has practical cash-out
≠ worker chooses it over carrying cash
```

因此页面的 `exists`、服务的 `available`、个人的 `executable` 和实际 `used` 必须继续分层。

---

# 4. 2005 农民工银行卡特色服务：真正关键的是“收款地能不能兑现”

中国人民银行《2005年贵州省金融运行报告》记录，2005 年 12 月 29 日贵州开始试点农民工银行卡特色服务：农民工在打工地用银联卡存入现金后，可在家乡附近农村信用社柜台取现。报告把它直接放在“改善农民工汇款条件”和农村支付环境的语境中。

Source:
- 中国人民银行，《2005年贵州省金融运行报告》：
  https://www.pbc.gov.cn/eportal/fileDir/history_file/files/att_12716_1.pdf

Evidence grade: **A — institutional historical report**.

这里最值得 old-web 建模的不是一张银行卡图片，而是：

**bank-website / branch-network executability gap — 银行网站 / 线下网点可执行性缺口。**

网站可以说“全国/跨地可用”，真正执行仍受：

- 发卡机构是否参与；
- 收款地农信社是否已接入；
- 卡片状态；
- 柜台营业时间；
- 身份/密码；
- 单笔/日限额；
- 当日网络与清算状态。

### 证据边界

报告说“农民工在打工地存现后，可在家乡农信社取现”，但本轮没有取得当年操作手册来确认：

- 是否必须持卡人本人取现；
- 家属能否代取；
- 是否存在附属卡/授权路径；
- 具体 PIN/身份证核验组合。

所以不能为了生活史叙事方便，把“回乡地区可取”自动写成“留乡家属可直接取”。

---

# 5. 2005 “漫游汇款”：交易权限的一部分通过电话之外的秘密转移

2005 年农业银行“漫游汇款”同期报道说：汇款人无需知道收款地具体银行名称/地址，只需填写收款人姓名并预留支取密码；收款人凭有效身份证件、漫游汇款号和支取密码，可在任一联网农行机构兑付。

Source:
- 东方早报/新浪财经，《农行新推“漫游汇款”》，2005-01-25：
  https://finance.sina.com.cn/roll/20050125/09511319852.shtml

Evidence grade: **B — contemporaneous financial press**.

这里新增：

**payment-record / secret-handoff gap — 支付记录 / 秘密交接缺口。**

银行后台可能保存：

- 汇款号；
- 汇款金额；
- 汇款人/收款人；
- 兑付状态。

但真正使收款人获得取款能力的支取密码如何传递，可能发生在：

- 电话；
- 短信；
- 当面；
- 纸条；
- 后来的即时通信。

这些通常不会与银行网页一起被 Web archive 保存。

因此：

```text
transaction record survives
≠ authorization handoff survives
```

---

# 6. 2006 网上漫游汇款：Web 只是混合事务的一段

2006 年 7 月上海农行开通 95599 网上银行漫游汇款。同期报道留下非常明确的完整路径：

```text
sender logs into Web banking
→ chooses roaming remittance
→ enters receiver name + amount + withdrawal password
→ bank submits transfer
→ sender telephones receiver with remittance number + password + amount
→ receiver visits local AgBank branch
→ receiver authenticates and cashes out
```

Source:
- 新华社上海电/经济参考报/新浪财经，《上海农行新推漫游汇款业务》，2006-07-19：
  https://finance.sina.com.cn/money/bank/bank_opration/20060719/08182743841.shtml

Evidence grade: **B — contemporaneous wire/financial press**.

这构成一个非常典型的 old-Web **hybrid transaction / 混合事务**。

### 不能写成

> 2006 年农行网上银行已经让用户完全在线完成跨地汇款。

因为至少还有两段在 Web 外：

1. 汇款人把秘密告诉收款人；
2. 收款人到实体网点兑付现金。

新增：

**online-initiation / offline-completion gap — 在线发起 / 线下完成缺口。**

---

# 7. Cross-channel secret dependency：电话不是被 Web 替代，而是成为网银控制面

2006 漫游汇款的路径特别适合纠正线性媒介史：

```text
Web transfer page
+ telephone call
+ branch counter
+ ID document
+ banking backend
= one remittance transaction
```

旧网考古若只研究 `www.abchina.com` 的页面，会把电话看成“旧媒介”；但真实事务中，电话承担了**秘密交接**，是 Web 支付的必要控制面之一。

新增：

**cross-channel secret dependency — 跨渠道秘密依赖。**

这一机制也适用于：

- 网上购票后短信验证码；
- Web 注册后 email 激活；
- 电话声讯返回交易码；
- 银行 UKey/口令卡；
- 后来的手机 OTP。

因此“网页保存完整”不等于“事务可复演”。

---

# 8. Web 页面存在不等于当年普通农民工可以执行网银

2006 年商业银行已经有规模化网银。工商银行 2006 年年报材料显示网上银行、电话银行、自助银行同时发展；但电子银行通常还涉及签约、账户、密码、证书/U盾/口令卡、安全控件以及特定浏览器环境。

Source:
- 工商银行 2006 年年度报告（现有在线再发布/证券资料页可观察电子银行说明）：
  https://finance.sina.com.cn/stock/company/sh/601398/9_1.shtml

Evidence grade: **A-adjacent corporate annual-report content via current host; historical page appearance not verified**.

对本仓的规则：

```text
historical bank says “网上汇款”
≠ anonymous browser can execute it
```

至少要继续查：

- 是否必须先去柜台签约；
- 证书/U盾/口令卡；
- ActiveX 或 IE 依赖；
- SSL/TLS 与根证书；
- 登录/交易密码；
- 单笔/日限额；
- 交易后回执；
- 超时与失败重试。

因此任何复原都必须把 **public instruction page** 与 **authenticated transaction application** 分成两个研究单位。

新增：

**instruction-page / authenticated-app gap — 说明页 / 认证交易应用缺口。**

---

# 9. 2007–2015 的页面若只剩“手续费说明”，不能据此恢复过去的真实费用

银行电子渠道往往以优惠费率推广，例如网上汇款可能低于柜台；同一银行还会按时间、地区、用户类型和活动调整资费。

所以旧页面中一个费率表必须绑定：

```yaml
bank:
channel:
transaction_type:
region:
effective_from:
effective_to:
customer_type:
amount_bracket:
min_fee:
max_fee:
source_date:
```

新增：

**tariff temporal gap — 资费时态缺口。**

不要拿今天农业银行当前“漫游汇款”页面上的规则反推 2005/2006，也不要拿 2006 上海网上费率推断全国全年。

Current product description may be useful only for continuity comparison:
- 中国农业银行当前“汇兑/漫游汇款”说明：
  https://www.abchina.com.cn/cn/businesses/payment/exchange/

Evidence grade for historical claims: **not A for 2005/2006 UI; current product continuity only**.

---

# 10. Payment settlement 本身是 Web archive 的“暗物质”

一个银行网页可以被 Wayback 保存，但真正的支付结果通常不可能由公共 archive 保存，因为它依赖：

- 用户私有登录态；
- 银行核心系统；
- 银联/跨行支付清算；
- 农信社/邮政受理网络；
- 实际账户余额；
- 后台时间戳；
- 风控与身份核验。

因此本专题加入：

**transaction-backend dark matter — 事务后台暗物质。**

即使拿到完整历史 HTML，也最多能确认：

- 入口存在；
- 字段形态；
- 前端验证；
- 浏览器要求；
- 当时声明的流程。

不能确认一个具体普通人在当日：

- 成功登录；
- 成功汇出；
- 对方成功取现。

---

# 11. 旧网“到账”至少有四个不同含义

建议以后所有支付/汇款 case 固定拆：

```text
submitted
→ bank accepted
→ settlement completed
→ receiver funds available
→ receiver knows
→ receiver withdrew/used
```

所以：

### remittance-submitted / settled gap
网页回执“已提交”不等于跨行清算已完成。

### settled / receiver-notified gap
钱已可取，不等于收款人已经知道。

### notified / cash-out gap
电话收到汇款号，不等于收款人有证件、有网点、有时间去兑付。

### cash-out / household-use gap
现金拿到，不等于我们知道它最终被用于学费、医疗还是其他项目。

这四个 gap 都不能靠网页截图直接补全。

---

# 12. 2018 以后的移动支付只能作为本仓边界，不能拿来倒推 2000s Web

人民银行公布的 2018 年农村支付数据表明，农村地区移动支付已经成为网络支付主导方式，手机银行、非银行移动支付规模巨大，电话银行则明显萎缩。

Source:
- 人民网转人民银行数据，《2018年农村地区移动支付业务继续高速发展》，2019-04-02：
  https://finance.people.com.cn/n1/2019/0402/c1004-31009686.html

Evidence grade: **A/B institutional-data relay**.

它对本仓的作用只是标记边界：

```text
2001 postal electronic backend
→ 2005 card / bank-network experiments
→ 2006 Web + phone + branch hybrid transaction
→ 2010s mobile/payment-app dominance
```

不要因为 2018 的农村支付非常成熟，就把 2006 的网银体验想象成今天手机 App 的早期皮肤。

---

# 13. Archive survival asymmetry：说明页往往比真正决定家庭结果的 state 更容易活下来

汇款史有一个非常明显的保存不对称：

**更容易保存：**
- 新闻稿；
- 产品说明；
- 费率表；
- 银行首页；
- 网银帮助页；
- 营业网点列表。

**更难/几乎不会公开保存：**
- 具体工人的工资是否到账；
- 私人账户；
- 真实交易回执；
- 汇款号/密码；
- 电话告知；
- 柜台取款；
- 家庭最后把钱花在哪里；
- 某次失败或退汇的完整状态机。

新增：

**payment-archive / family-outcome asymmetry — 支付档案 / 家庭结果保存不对称。**

这意味着 old-Web 很容易让后人高估“金融产品页面”，低估真正维持家庭的电话、现金、柜台和亲属协调。

---

# 14. 隐私：支付考古必须比普通页面更严格最小化

本专题涉及天然高敏感数据。

即使 archive 偶然保存了：

- 卡号；
- 账户；
- 身份证号；
- 汇款号；
- 取款密码；
- 手机号；
- 姓名与金额组合；

也不得因为“历史页面可访问”就在仓库重新分发。

研究重点应是：

- field schema；
- 认证机制；
- 状态转换；
- URL pattern；
- 公开帮助文档；
- 资费与浏览器条件；

而不是恢复普通个人的交易明细。

---

# 15. Evidence table

| Claim | Evidence | Grade | Confidence | Limits |
|---|---|---:|---:|---|
| 2001 邮政电子汇款首批联网，现金汇款可 24h 兑付 | 中国青年报 2001 | B | high | 不能复原后台/网页；本身并非 Web 用户界面 |
| 2005 很多农民工仍携现，汇款主要邮政/绿卡 | PBC + 中青报 | A/B | high | 调查口径需按报告，不外推每个地区 |
| 2005 贵州试点银行卡特色服务 | PBC 2005 贵州报告 | A | high | 家属代取权限未验证 |
| 2005 漫游汇款可凭姓名、密码、汇款号跨地兑付 | 同期财经报道 | B | high | 未取得 2005 原始银行操作手册 |
| 2006 上海 95599 网银漫游汇款需电话通知收款人后到网点取现 | 新华/经济参考报 | B | high | 未验证历史网银 DOM/安全控件 |
| 2018 农村移动支付已成为网络支付主导 | PBC data relay | A/B | high | 不能倒推到 migrant-specific adoption |

---

# 16. 本轮没有做到什么：M1 仍未达到

本轮实际取得/检查的是：

- 同期报刊页面；
- 中国人民银行历史 PDF；
- 今天仍在线的银行产品说明；
- 现有历史日期的公司/媒体材料。

**本轮没有实际取得并检查一份 2001–2010 中文银行/邮政汇款页面的 verified Wayback/WARC response。**

因此以下项目继续标 `unknown`：

- 2001 邮政电子汇款是否有公开 Web 操作页；
- 2005/2006 农行漫游汇款原始页面 URL 与 DOM；
- 原始 HTTP headers；
- charset；
- IE/ActiveX 要求；
- 证书/U盾/口令卡依赖；
- form action；
- session/cookie；
- transaction confirmation page；
- error/timeout/retry UI；
- 子资源保存；
- 当年银行在线帮助页与实际 authenticated app 是否同 host。

按照 `docs/METHOD.md`：

> 搜索到一个 archive locator 也不算验证 capture；本轮更不能因为未取得 capture 就写“Wayback 没有”。

所以本专题只是 **state-gap / evidence package**，不是 M1 完整历史页面复原。

---

# 17. 下一步最值得做的 Web 考古目标

1. 找 2005–2007 农行 `95599` / 漫游汇款历史 URL，实际打开两个以上时点的 archive capture。
2. 查原始帮助页是否记录 IE、ActiveX、证书、U盾/口令卡和安全控件。
3. 查中国邮政 2001–2005 电子汇款是否存在可验证旧页面及 Web 查询功能。
4. 找农民工银行卡特色服务的原始操作规程，区分持卡人本人取现与家属实际收款路径。
5. 记录当年费率页面的有效期，不把 later page 当 earlier tariff。
6. 若能找到错误/退汇/密码遗忘的同期用户操作说明，可补 `failure-state`；不要用后来的客服 FAQ 直接倒推。
7. 对任何包含普通个人账户/手机号/汇款编号的 archive 只做结构记录，不重新公开敏感值。

---

# 18. 对中文旧网史的增量结论

这一专题最重要的不是“银行什么时候上线网银”，而是：

> **Web 事务可以非常现代，却仍然依赖电话、身份证、实体网点和一个远方家庭成员。**

2006 年一个人能在网页上发起漫游汇款，但她仍要打电话把支取秘密告诉家人；家人仍要走到当地银行、拿出证件、完成兑付。历史页面即使完整保存，也看不到这笔钱最后有没有真正进入那个家庭。

因此，中文旧网的事务考古不能停在浏览器：

**page state ≠ payment state ≠ household state。**
