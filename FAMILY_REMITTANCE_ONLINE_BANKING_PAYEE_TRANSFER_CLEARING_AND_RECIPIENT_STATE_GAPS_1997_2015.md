# Family remittance / online banking / payee / transfer / clearing / recipient state gaps（中文 Web，1997—2015）

## 0. Scope

本 note 只研究约 1997—2015 中文 Web 中与个人转账、汇款和家庭资金移动直接相关的 **Web 可观察层**：银行门户、个人网银、功能说明、历史登录入口、证书/控件、跨行清算说明、用户教程和同时代安全报道。

它不把“中国家庭汇款史”整体搬进本仓。邮政汇兑、农民工携现返乡、农村金融网络、2015 年后的手机支付和 2020s 家庭资金流，主要写入：

- `tmzncty/how-people-lived/topics/from-postal-remittances-to-instant-family-transfers-remittance-executability-intergenerational-money-flows-and-family-money-portability-china-1995-2026.zh-CN.md`

本仓要回答的是更窄的问题：

> 二十年后，我们如果只找到一个银行网站、一张“转账汇款”帮助页或一份登录截图，到底能够证明普通用户当时完成了哪一步？哪些关键状态天然不会进入公共 Web archive？

遵守 `docs/METHOD.md`：platform / site / page / account / capture / claim 分离；archive locator 未实际打开核验前不算 verified capture；现代浏览器成功打开今天仍存活的旧路径，不等于历史浏览体验。

---

## 1. 研究对象必须拆开

至少区分以下对象：

1. **bank / legal institution**：现实中的银行机构；
2. **public portal host**：如 `www.icbc.com.cn`；
3. **personal online-banking host**：如 `mybank.icbc.com.cn`；
4. **public product/help page**：转账、汇款、U 盾、费率、公告等公开页面；
5. **login page**：认证入口；
6. **customer**：银行真实客户；
7. **Web account / online-banking entitlement**：是否已经注册/开通网银；
8. **credential**：用户名、卡号、密码；
9. **hardware/software credential**：U 盾、数字证书、口令卡、客户端控件等；
10. **browser environment**：IE/其他浏览器、ActiveX、OS、证书链、编码；
11. **payee record**：收款人姓名、卡号/账号、开户行等；
12. **transfer form**：用户填写的汇款指令；
13. **submitted request**：浏览器已把请求提交给银行；
14. **bank accepted instruction**：银行系统已受理；
15. **risk/authentication result**：认证、风控、限额检查通过；
16. **bank ledger debit**：付款账户实际扣账；
17. **interbank clearing message**：跨行清算请求进入底层系统；
18. **recipient-bank credit**：收款行记账；
19. **recipient notification**：短信/页面/其他通知；
20. **recipient access**：收款人真的能登录、取现或支付；
21. **household outcome**：这笔钱真正被家人拿去交学费、看病、日常消费等。

这些对象不能合并。

---

## 2. 最小状态链

### 2.1 “网站有转账功能”不等于“这个人能转账”

`bank has public website`
`!= bank offers personal online banking`
`!= this customer has bank account`
`!= this customer has online-banking entitlement`
`!= this customer has required certificate/token`
`!= historical browser/client can execute the page`
`!= customer can authenticate`
`!= customer has usable balance`
`!= customer can add/use payee`
`!= transfer is within channel limit`
`!= transfer request accepted`。

### 2.2 “提交成功”不等于“家里钱到了”

`form submitted`
`!= bank accepted`
`!= payer debited`
`!= interbank rail available`
`!= recipient bank received clearing message`
`!= recipient account credited`
`!= recipient knows it arrived`
`!= recipient can withdraw/use it`
`!= household actually receives benefit`。

### 2.3 页面与底层轨道属于不同层

尤其跨行交易：

`front-end page reachable`
`!= clearing system running`。

2011 年工商银行公开通告就明确记录：人民银行支付清算系统进入维护窗口时，工行将暂停受理网上支付跨行清算等业务。公开 Web 页面仍可能正常存在，但资金通道本身不可用。

来源（A）：
- ICBC, 2011-07-01, “关于暂停受理跨行小额支付业务、网上支付跨行清算业务……”：
  https://www.icbc.com.cn/icbc/%E9%87%8D%E8%A6%81%E5%85%AC%E5%91%8A/%E5%85%B3%E4%BA%8E%E6%9A%82%E5%81%9C%E5%8F%97%E7%90%86%E8%B7%A8%E8%A1%8C%E5%B0%8F%E9%A2%9D%E6%94%AF%E4%BB%98%E4%B8%9A%E5%8A%A1%E7%BD%91%E4%B8%8A%E6%94%AF%E4%BB%98%E8%B7%A8%E8%A1%8C%E6%B8%85%E7%AE%97%E4%B8%9A%E5%8A%A1%E5%85%A8%E5%9B%BD%E6%94%AF%E7%A5%A8%E5%BD%B1%E5%83%8F%E4%BA%A4%E6%8D%A2%E4%B8%9A%E5%8A%A1%E7%94%B5%E5%AD%90%E5%95%86%E4%B8%9A%E6%B1%87%E7%A5%A8%E4%B8%9A%E5%8A%A1%E7%9A%84%E9%80%9A%E5%91%8A.htm

这应长期作为 `page state / rail state gap` 的标准反例。

---

## 3. 1997—2000：先证明“银行上 Web”和“个人可以远程办银行”是两件事

招商银行现行机构史把 1997 年“一网通”作为个人客户网上银行/网上支付的重要起点；工商银行官方电子银行史明确记录 `www.icbc.com.cn` 于 1997 年 12 月开通，1999 年推出统一号码电话银行 95588，2000 年 2 月企业网上银行在四城开通，2000 年 8 月个人网上银行在北京、浙江试点。

来源（A，机构自述，需和同期材料交叉）：
- 招行官网历史页：https://www.cmbchina.com/
- 工行电子银行发展史：https://www.icbc.com.cn/icbc/%E5%8C%97%E4%BA%AC%E5%88%86%E8%A1%8C/%E5%88%86%E8%A1%8C%E5%8A%A8%E6%80%81/%E5%B7%A5%E5%95%86%E9%93%B6%E8%A1%8C%E7%94%B5%E5%AD%90%E9%93%B6%E8%A1%8C%E5%BC%95%E9%A2%86%E9%87%91%E8%9E%8D%E6%9C%8D%E5%8A%A1%E8%B5%B0%E8%BF%9Be%E6%97%B6%E4%BB%A3.htm
- 工行版本史：https://www.icbc.com.cn/icbc/html/wangyin/version/banben.files/version.htm

### 可证实

- 工商银行公共网站 host `www.icbc.com.cn` 至少在其机构史中明确追溯到 1997 年；
- 工行个人网银并非与公共网站同日出现，其机构史把个人业务试点放在 2000-08-28；
- 电话银行、手机银行、网上银行曾经并行，而不是 Web 一出现就替代所有远程金融渠道。

### 不能由这些材料直接证明

- 1997 年公共网站首页具体 DOM/CSS/charset；
- 1997 年普通个人能否通过该网站完成汇款；
- 2000 年个人网银所有地区都可用；
- 某个历史页面使用 IE/ActiveX 的具体版本条件。

因此：

`public site launch date != personal transfer availability date`。

---

## 4. 2003—2005：“金融@家”把转账汇款写进 Web 产品，但安全令牌让数字事务继续保留物理尾巴

工行官方版本史记录：2003-11-23 推出“金融@家”新一代个人网上银行，产品体系明确包括“转账汇款”。2005 年官方/同期媒体又反复把 7×24 小时汇款列为个人网银功能。

来源：
- ICBC version history（A）：https://www.icbc.com.cn/icbc/html/wangyin/version/banben.files/version.htm
- 工行“金融@家”2005 年业务介绍（A）：https://www.icbc-us.com/icbc/%E5%A4%A9%E6%B4%A5%E5%88%86%E8%A1%8C/%E5%88%86%E8%A1%8C%E5%8A%A8%E6%80%81/%E5%B7%A5%E8%A1%8C%E9%87%91%E8%9E%8D%E5%AE%B6%E7%AC%AC%E4%B8%89%E6%AC%A1%E8%8D%A3%E8%86%BA%E4%B8%AD%E5%9B%BD%E6%9C%80%E4%BD%B3%E4%B8%AA%E4%BA%BA%E7%BD%91%E4%B8%8A%E9%93%B6%E8%A1%8C%E7%A7%B0%E5%8F%B7_1.htm

2005 年工行推广 U 盾时的同期说明则保留了非常重要的物理/浏览器边界：客户证书放在 USBKey 中，使用时需要把硬件插入电脑；证书下载失败还可能必须去柜台处理。

来源（B，同期媒体转载工行说明）：
- 搜狐，2005-10-10：https://news.sohu.com/20051010/n227157027.shtml

因此历史事务链不是：

`Web exists → user transfers money`。

而可能是：

`bank account exists`
→ `customer obtains online-banking entitlement`
→ `customer obtains USBKey / certificate`
→ `client driver/control installed`
→ `browser reaches authentic host`
→ `certificate recognized`
→ `login succeeds`
→ `payee/amount entered`
→ `transaction authenticated`
→ `bank accepts`
→ `clearing/credit occurs`。

### 新状态差：`remote transaction / physical credential gap`

用户已经不必为了每笔汇款去柜台，但“远程”仍可能依赖一枚在手里的 U 盾、已安装的驱动和一台兼容电脑。

这类物理尾巴在今天的网页 archive 中尤其容易消失。

---

## 5. 2005—2007：安全报道给了 exact transaction host，但不能用今天的残存页面替代历史 capture

2006 年一次假冒工行网银的同期用户安全报道明确对比了假网址和真实登录地址，并留下：

`https://mybank.icbc.com.cn/icbc/perbank/index.jsp`

来源（B，2006 同期安全报道）：
- cnBeta, 2006-12-06：https://www.cnbeta.com.tw/articles/19028.htm

2007 年一篇 IE7 操作文章又记录：进入工行个人网上银行时可能遇到 ActiveX 控件安装问题，用户被建议把 `*.icbc.com.cn` 加入可信站点并按提示安装控件。

来源（B，同期技术教程/后续转载）：
- 51CTO 记录页：https://blog.51cto.com/u_15127629/3918259

### 这里可以确认什么

- `mybank.icbc.com.cn` 是至少在 2006 年被同期材料识别为工行真实个人网银 host；
- `/icbc/perbank/index.jsp` 是一条有同期出处的历史登录路径；
- 至少部分 2007 用户环境遇到 IE7 / ActiveX 兼容问题。

### 不能确认什么

- 所有 2006/2007 用户都必须 ActiveX 才能使用所有功能；
- 所有转账页面都在同一路径；
- 今天访问同一路径所得 DOM、脚本、跳转就是 2006 页面；
- 银行后台的汇款请求和清算状态可以从登录页 capture 推导出来。

---

## 6. Archive locator 检查：得到一个 2007 英文网银快照线索，但尚不足以完成 M1

本轮实际检查 `archive.is` 对 `mybank.icbc.com.cn` 的索引。索引页列出了：

- 2007-07-20 20:21 的 `https://mybank.icbc.com.cn/icbc/enperbank/index.jsp`
- 并标注其 archival source 为 Wayback：
  `http://web.archive.org/web/20070720202123/https://mybank.icbc.com.cn/icbc/enperbank/index.jsp`

本轮能实际打开并检查的是 **archive.is 的索引页面**；继续跟入 Wayback capture 时收到 HTTP 429 / rate-limit 类错误，未取得主文档内容。因此：

### Candidate capture

- original URL: `https://mybank.icbc.com.cn/icbc/enperbank/index.jsp`
- candidate datetime: `2007-07-20T20:21:23`（来自索引展示）
- candidate archive source: Internet Archive / Wayback
- locator source: `https://archive.is/mybank.icbc.com.cn`
- verification status: **candidate only**

### 未取得

- capture 主 HTML；
- historical HTTP/replay status；
- Content-Type / charset；
- DOM；
- JS / CSS / image subresources；
- login form action；
- certificate/control behavior；
- Chinese-language transaction page；
- 第二个可比较历史时点。

因此严格记录：

> **M1 verified historical Chinese online-banking/remittance transaction capture: NOT ACHIEVED IN THIS SLICE.**

这不是“Wayback 没保存”。这里只能说：本轮没有成功打开并验证满足 `docs/METHOD.md` 最低字段合同的 historical capture。

---

## 7. 2005 年网上汇款增长可以证明“used”，但不能告诉我们是谁把钱汇给了谁

工行 2005 年官方材料称，截至 2005 年 8 月个人网银客户规模已很大，且 1—8 月“网上汇款”交易额显著增长。

来源（A，机构自报）：
- https://www.icbc-us.com/icbc/%E5%A4%A9%E6%B4%A5%E5%88%86%E8%A1%8C/%E5%88%86%E8%A1%8C%E5%8A%A8%E6%80%81/%E5%B7%A5%E8%A1%8C%E9%87%91%E8%9E%8D%E5%AE%B6%E7%AC%AC%E4%B8%89%E6%AC%A1%E8%8D%A3%E8%86%BA%E4%B8%AD%E5%9B%BD%E6%9C%80%E4%BD%B3%E4%B8%AA%E4%BA%BA%E7%BD%91%E4%B8%8A%E9%93%B6%E8%A1%8C%E7%A7%B0%E5%8F%B7_1.htm

它最多支持：

- personal online banking existed；
- transfer/remittance existed as product；
- bank reported substantial usage/growth。

它**不能**支持：

- 这些汇款主要是农民工给父母；
- 用户年龄、城乡、收入结构；
- 收款人的现实身份；
- 一笔汇款最后用于什么。

这是 `bank-transaction aggregate / household-meaning gap`。

Web 和机构业务统计很容易保存“有多少交易”，却几乎不保存“为什么这 500 元今天必须到家”。

---

## 8. 2008：公共 Web 已经把汇款渠道做成可比较对象，但“价格表”仍不是一次成功事务

2008 年天津日报同期文章已经把个人异地汇款方式并列为：

- 网上银行；
- 自助设备；
- 柜面；
- 邮政汇款。

并比较不同渠道手续费。

来源（B）：
- 《天津日报》，2008-01-16：https://news.sina.com.cn/c/2008-01-16/100713269910s.shtml

这类页面是 old-Web 很容易残存的材料：费率表、帮助文档、渠道说明。

但应保留状态差：

`fee schedule says online transfer available`
`!= user has online banking`
`!= browser works`
`!= recipient bank supported`
`!= actual fee for this account/tier/region matches summary`
`!= transfer succeeded`。

### 新 archive bias：`guidance survival / transaction-state loss`

公开帮助材料的保存概率远高于任何一名普通人的：

- 登录成功/失败；
- 收款人填错；
- U 盾识别错误；
- 当日限额；
- 银行后台拒绝；
- 收款到账；
- 家里是否真正取出现金。

因此历史研究不能因为帮助页保存得好，就把业务执行写得过于顺滑。

---

## 9. 2010：跨行网上支付清算系统把“银行网站”后面又显露出一层公共基础设施

2010-08-30，人民银行网上支付跨行清算系统开始上线。同期新华社报道明确说明，其目标是连接相关商业银行网银端口，使用户最终可以进行跨行账户管理和资金汇划。

来源（B+，新华社同期稿转载）：
- https://news.sina.com.cn/o/2010-08-31/051018043272s.shtml

但同期报道同时说明：系统上线不等于所有个人客户当天就能使用，各行还需要通过验收、接入和开通。

来源（B）：
- 《法制晚报》，2010-08-30：https://news.sina.com.cn/c/2010-08-30/141218041124s.shtml
- 《经济参考报》，2010-09-03：https://finance.sina.com.cn/money/bank/ywycp/20100903/09418597859.shtml

因此：

`PBOC rail live`
`!= bank connected`
`!= bank customer-facing service enabled`
`!= customer signed agreement`
`!= transfer within 50k/other applicable limit`
`!= transfer accepted at this moment`。

这条链对于 Web archaeology 很重要，因为一个历史银行 portal 可以“看起来”提供跨行转账按钮，但按钮后面依赖的系统可能：

- 尚未接入；
- 正在维护；
- 仅部分地区/客户开放；
- 要先签约；
- 有额度边界。

---

## 10. Web 页面与收款端之间还隔着一个常被 archive 擦掉的世界

即使找到完整历史网银转账页，也只能恢复发送端的一小部分体验。

家庭汇款的真正状态还包括：

`payee account legally exists`
`→ recipient can access it`
`→ recipient knows transfer arrived`
`→ local ATM/branch can pay cash if needed`
`→ recipient can authenticate`
`→ recipient trusts SMS/page`
`→ recipient uses funds`。

尤其 2000s 农村汇款场景中，发送者已经可以通过 Web 网银操作，并不意味着父母/配偶收款端已经全面数字化。收款端可能仍然是：

- 农村信用社柜台；
- 邮政储蓄；
- ATM；
- 存折；
- 他人协助查询；
- 现金消费。

因此新增：

### `sender-Web / recipient-offline asymmetry`

Web archive 对发送者界面高度可见，对收款者线下兑现过程高度不可见。

如果只考古网站，历史会被误写成“家庭汇款在 2005 已经端到端在线化”。

---

## 11. Browser / security environment：只写有证据的条件

### 已有证据

- 2005 工行 U 盾说明明确存在 USBKey / 客户证书这一物理认证层；
- 2006 同期安全报道明确留下 `mybank.icbc.com.cn/icbc/perbank/index.jsp`；
- 2007 技术文章记录至少部分 IE7 用户遇到 ActiveX 安装/可信站点问题。

### 不写成历史事实的推断

本轮**没有**足够证据统一宣称：

- “所有工行网银必须 IE6”；
- “所有汇款都依赖 ActiveX”；
- “页面一定是 GB2312/GBK”；
- “所有用户都使用 Windows XP”；
- “所有银行都要求 U 盾”；
- “每个历史版本的 `/perbank/index.jsp` DOM 相同”。

这些必须等待 verified capture + historical environment test。

---

## 12. Identity：聊天关系、家庭关系、银行收款人不是同一个对象

家庭汇款尤其容易被今天的“联系人转账”体验倒推。

在 Web 网银时代，常见状态更像：

`现实中的母亲`
`!= 地址簿中的“妈妈”`
`!= 银行 payee record`
`!= payee account legal holder`
`!= 操作取款的人`。

即使页面保存了“收款人姓名/账号/开户行”字段，也不能从字段推断：

- 两人现实亲属关系；
- 收款账号由谁日常控制；
- 汇款是否为赠与、赡养、借款、工资转交或代购；
- 资金是否后来又被转回。

这与 `how-people-lived` 中“代际资金流并非单向”必须保持联动。

---

## 13. Archive asymmetries introduced by this case

### 13.1 `public-shell / private-balance asymmetry`

公开 portal、帮助页、费率表可保存；客户余额、历史收款人和真实转账状态本来就在认证后，不应进入公共 archive。

### 13.2 `form-survival / clearing-state loss`

即使表单完整保存，也无法从静态 capture 恢复当时的清算轨、余额、限额、风险决策和收款行状态。

### 13.3 `sender-interface / recipient-life asymmetry`

发送端页面可能保存；父母在乡镇信用社排队取钱、不会操作 ATM 或拿到钱后付学费的真实过程不在 Web 页面里。

### 13.4 `security-warning survival / endpoint-state loss`

反钓鱼公告、U 盾帮助页很容易保存；真实用户电脑上的恶意软件、驱动版本、证书状态和是否误入假站不保存。

### 13.5 `transaction-aggregate / household-meaning gap`

银行能留下“网上汇款交易额”，却不会在公共网页告诉研究者这些钱是赡养、教育、医疗、还债还是朋友间转账。

### 13.6 `successful-guidance / failed-attempt invisibility`

一份“如何转账”的教程可以存活二十年；那些因为控件、限额、账号、网络、收款信息错误而失败的无数尝试往往没有公共记录。

---

## 14. Evidence matrix

| Claim | Evidence | Grade | Confidence | Boundary |
| --- | --- | --- | --- | --- |
| `www.icbc.com.cn` 被工行机构史追溯到 1997-12 | 工行电子银行发展史 | A (official retrospective) | high for institutional claim | 非 1997 capture |
| 工行个人网银 2000-08 在北京/浙江试点 | 工行版本史 | A (official retrospective) | high for institutional claim | 不等于全国可用 |
| 2003 新一代“金融@家”含转账汇款 | 工行版本史/产品说明 | A | high | 不证明单个客户可执行 |
| 2005 U 盾是 USBKey 客户证书并与网银安全相关 | 工行说明的同期媒体转载 | B/A-derived | high | 不外推所有银行/用户 |
| 2006 同期材料给出真实工行登录 URL `/icbc/perbank/index.jsp` | cnBeta 安全报道 | B | medium-high | 不是 archive capture |
| 2007 至少部分 IE7 用户遇到 ActiveX 问题 | 同期技术文章 | B | medium | 不外推所有版本/功能 |
| 2010 跨行网上支付清算系统上线 | 新华社等同期报道 | B+/A-derived | high | 用户侧需银行接入/签约 |
| 2011 清算维护时工行暂停相关跨行业务 | 工行正式公告 | A | high | 证明 rail state 独立于 page state |
| 存在 2007 ICBC English online-banking candidate Wayback locator | archive.is index | locator only | medium | 未成功打开主 capture |

---

## 15. Privacy / research boundary

此对象天然涉及高度敏感金融数据。本仓不得为了“还原网银历史”而：

- 搜集普通人的历史银行卡号；
- 重新发布旧论坛中泄露的卡号/身份证/交易截图；
- 尝试访问任何真实账户；
- 保存 session token、证书或可复用认证材料；
- 把钓鱼样本中的真实受害者信息重新聚合；
- 把公共 archive 中偶然泄露的余额/收款人当成研究素材扩散。

优先保存：

- public URL；
- historical host/path pattern；
- 公开产品文档；
- fee/help/security pages；
- capture metadata；
- 已匿名化的状态模型。

---

## 16. Counterexamples / hindsight risks

### 不要写：Internet 第一次让普通人远程汇钱

邮政汇兑、银行汇款、电话银行和专用金融网络早已存在。

### 不要写：银行网站一上线，普通人就可以网上转账

公共 portal、个人网银、开户、认证、地区覆盖和客户 entitlement 有不同时间线。

### 不要写：电子汇兑 = Web 网银

2001 邮政电子汇兑主要说明机构后台记录电子化，收发两端仍可以是实体网点。

### 不要写：有历史登录 URL = 已经完成页面考古

URL 只是 locator。没有 capture datetime、HTML、charset、DOM、subresources、browser condition 就不能宣称复原。

### 不要写：页面显示“汇款成功” = 收款人已拿到钱

还存在扣账、清算、收款行入账、通知、取现/支付等状态。

### 不要写：2007 IE7 ActiveX 个案 = 整个 2000s 中文网银统一 IE-only

只能保留为一个有同时代来源的 browser-condition specimen。

---

## 17. What remains unknown

1. 1997—2000 招商/工行早期个人网银的 **verified historical Chinese capture** 仍缺。
2. `mybank.icbc.com.cn/icbc/perbank/index.jsp` 在 2003、2005、2007 的 DOM/JS/charset/version evolution 未核验。
3. 转账/汇款 transaction page 的真实 URL pattern 尚未建立；目前材料主要是 login/help/marketing。
4. U 盾驱动、ActiveX 控件、浏览器和 OS 的版本矩阵未建立。
5. 招行“一网通”2000s 专业版的历史 transaction capture 值得与工行做独立对照。
6. 网上银行与电话银行、自助终端在 2000s 家庭汇款中的实际用户分工仍缺生活史材料。
7. 跨行清算页面按钮与底层报文/settlement state 的关系只能从公开制度文档抽象，不应模拟真实银行后端。
8. 至少需要第二个独立 archive source / historical time point 才可能把本 note 升级为 M1 完整案例候选。

---

## 18. Next archaeological slice

优先级建议：

1. 克制地继续查 `mybank.icbc.com.cn` 2003—2010 的 Wayback/CDX、archive.today 和 Common Crawl locator；
2. 只在能实际打开 capture 时记录 `capture_url/original_url/datetime/status/content-type/charset`；
3. 查找同期工行帮助页中“汇款/收款人/U盾/限额”的 exact URL；
4. 同样为 `www.cmbchina.com` / 一网通建立一个独立候选链，避免单银行推全国；
5. 若得到历史页面，再进入 M3 浏览器环境验证，而不是现在按年代印象猜 IE/GBK/ActiveX。

---

## 19. Why this changes old-Web interpretation

银行旧网页很容易让后人产生一种“屏幕中心主义”：看见 2005 年已经有“转账汇款”菜单，就觉得钱已经完全在 Internet 里移动。

实际上一次家庭汇款至少横跨：

`现实收入`
→ `银行账户`
→ `Web entitlement`
→ `历史浏览器/证书`
→ `转账表单`
→ `银行风控`
→ `跨行清算`
→ `收款账户`
→ `乡镇 ATM/柜台/现金`
→ `家庭消费`。

公共 Web archive 最可能保存的，只是这条链中间很薄的一层。

因此这个 case 对中文旧网考古最大的贡献不是“找到一个老网银页面”，而是建立一个更严格的解释原则：

> **金融网站的页面保存程度，天然高于真实资金状态的可保存程度。一个完整的 HTML，也只能证明一段界面存在，不能替普通人的钱证明它真的走到了家里。**
