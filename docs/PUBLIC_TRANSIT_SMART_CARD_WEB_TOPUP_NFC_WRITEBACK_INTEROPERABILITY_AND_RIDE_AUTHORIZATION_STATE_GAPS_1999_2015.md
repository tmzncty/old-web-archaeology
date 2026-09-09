# 公共交通 IC 卡、Web 充值、NFC、圈存、互联互通与实际乘车之间的状态缺口（中国，1999—2015）

> Scope：本文件严格服务于 `old-web-archaeology` 的约 1995–2015 中文旧网主范围。它不是全球智能交通卡史，也不把 2015 年之后的全国交通联合、二维码乘车或银行卡直接过闸扩写成本仓主线。海外 Octopus / Oyster 与 2015 年后的跨城生活史比较放在 `tmzncty/how-people-lived`：
> https://github.com/tmzncty/how-people-lived/blob/main/topics/from-carrying-change-to-carrying-a-mobility-balance-transit-fare-media-topup-and-portability-china-1979-2026.zh-CN.md
>
> 核心考古问题：一张历史网页如果写着“交通卡查询”“在线充资”“充值成功”“手机一卡通”，研究者究竟能证明到哪一层？网页壳、支付状态、后台账户、实体卡芯片、NFC 安全元件、闸机/车载机、票价规则、中央清分与一个真实的人实际完成乘车，并不是同一个对象。

本文件也与仓库已有对象明确分工：

- `CAMPUS_ONE_CARD_WEB_QUERY_LOSS_REPORT_BALANCE_ACCESS_AND_STUDENT_STATUS_STATE_GAPS_2003_2015.md`：校园机构身份与一卡通；
- `docs/MOBILE_PREPAID_RECHARGE_CARD_ONLINE_TOPUP_BALANCE_AND_SERVICE_CONTINUITY_STATE_GAPS_1999_2015.md`：移动通信预付费余额；
- 铁路票务专题：预订特定车次/席位、订单与乘车执行；
- 本文：**城市公交/地铁的反复小额乘车权，如何在交通卡、Web 充值、写卡、NFC 与验证器之间流转。**

---

## 1. 为什么“交通卡网页”特别容易产生错误历史结论

一个最常见的历史页面可能只有：

- 卡片介绍；
- 充值网点列表；
- 余额查询入口；
- “网上充”按钮；
- 手机一卡通说明；
- 服务范围与票价优惠；
- 常见问题；
- “充值成功”/“交易成功”的结果页面样式。

这些 artifact 很容易让后来研究者产生一种错觉：

> 既然网页写着在线充值，而且结果页显示成功，那么用户的交通卡已经多了这笔钱，并且下一次上车一定可以刷。

实际上至少要拆成：

`public site`
`fare-media product`
`physical card`
`chip purse / secure element`
`backend account`
`top-up instruction`
`payment transaction`
`write-back / circle-store`
`validator transaction`
`fare-rule evaluation`
`clearing / settlement`
`actual ride`

这些对象可以部分成功、部分失败。

---

## 2. 对象模型：不要把“卡”当成一个单一状态

### 2.1 Institution / operator

例如交通卡公司、公交集团、地铁运营方、清分机构、移动运营商、银行/支付机构。

它们可以共享一个产品品牌，但不一定共享同一后台。

### 2.2 Public site / Web service

公众能在浏览器里看到的：

- 产品说明；
- 网点查询；
- 余额/交易查询；
- 在线充资入口；
- 下载/安装说明；
- 客服与退卡规则。

页面存在，只能证明某个公开入口存在。

### 2.3 Fare-media product

“上海公共交通卡”“北京市政交通一卡通”“手机一卡通”等是制度/产品层对象。

同名产品在不同年份可能经历：

- 卡片代际变化；
- 可用线路变化；
- 押金/服务费变化；
- 充值渠道变化；
- 优惠规则变化；
- 实名/匿名政策变化。

### 2.4 Physical card / secure element

真正放在乘客手里、被闸机或车载机读取的介质：

- 实体 IC 卡；
- NFC-SIM；
- 手机安全元件；
- 后来其他设备钱包。

它可能和 Web 账户完全不是同一个余额对象。

### 2.5 Backend account

网上营业厅、手机钱包或支付页面看到的后台账户。

尤其在需要“圈存”的体系中：

`backend funded` 并不意味着 `chip purse funded`。

### 2.6 Validator / gate transaction

真正决定某一次公交/地铁进站或乘车是否放行的事件。

研究者必须区分：

- 读卡成功；
- 卡片被接受；
- 扣费成功；
- 优惠规则是否应用；
- 是否形成后台上传/清算记录；
- 人是否真的完成了这次旅程。

---

## 3. 基本状态链

### 3.1 Web 充值链

`网站存在`
→ `在线充值被公开宣称可用`
→ `用户浏览器/设备满足要求`
→ `登录/识别卡片成功`
→ `支付请求提交`
→ `支付机构扣款/授权`
→ `交通后台接受充值指令`
→ `需要时完成写卡/圈存`
→ `卡片本地余额真正变化`
→ `闸机/车载机下一次读取新余额`
→ `按当时票价规则完成扣费`
→ `乘客实际完成移动`

任意一步都不能由前一步自动推出。

### 3.2 NFC 手机卡链

`手机型号支持 NFC`
→ `SIM/安全元件方案兼容`
→ `运营商/交通卡业务已开通`
→ `手机侧账户可用`
→ `后台账户有资金`
→ `圈存进入交通卡账户/安全元件`
→ `设备在当前电量/系统状态下仍可刷`
→ `目标线路验证器接受`
→ `完成扣费/乘车`

### 3.3 跨域互联链

2015 年前后各地互联互通仍处发展过程中，不能把后来“交通联合”的成熟语义倒投回早年地方卡。

真正的跨域状态至少是：

`卡片/标准理论兼容`
→ `目标城市已接入`
→ `目标运营者已接入`
→ `目标线路/设备已升级`
→ `验证器识别卡片`
→ `清分链路接受`
→ `当地票价规则可执行`
→ `是否享受本地换乘/优惠另行判断`

---

## 4. 1999 上海：公共交通数字化首先不是 Web 故事

上海公共交通卡股份有限公司官方网站记录，公司经市政府批准于 **1999 年 5 月 25 日**成立，承担上海公共交通“一卡通”工程，包括卡片制作发行以及系统的中央结算和清分。

来源（A，运营机构）：
https://www.sptcc.com/

这条证据首先说明：

> **公共交通数字化可以在普通家庭尚未通过 Web 管理卡片之前，先以卡片 + 读卡设备 + 机构后台 + 中央清分的形式进入城市日常。**

因此：

`交通卡后台联网存在 ≠ 家庭 Internet 接入 ≠ 公众 Web 自助可用`。

1999 年精确首发/试运行日期在后来的材料中常见，但本轮没有取得同等强度的首发当日一手公报。公司成立日期和职责可列 A；精确到某一天的发行节点应暂时低一级处理。

---

## 5. 2006 北京：纸月票迁移进 IC 卡，但制度迁移不能写成自然采用

中国政府网 2006 年 3 月 27 日转载同期北京日报便民问答，明确说明北京自 **2006 年 5 月 10 日**起实行刷卡乘车，并区分普通卡电子钱包储值区以及多种月票卡，纸质月票退出既有票制。

来源（A/B，政府门户 + 同期报刊）：
https://www.gov.cn/banshi/2006-03/27/content_237530.htm

这类材料的历史意义不只是“一卡通上线”：

- 原纸月票用户被迁入新的介质；
- 月票资格与电子钱包可以同时存在于卡片体系；
- 一张卡的制度状态开始决定不同线路/票种上的扣费规则。

但不能由此推断所有乘客是因为个人偏好主动转向 IC 卡。

`institutional migration` 与 `voluntary adoption` 必须分开。

---

## 6. 2008：同期用户材料暴露了充值、匿名和丢卡之间的实际权衡

新华社 2008 年的北京一卡通采访保存了很稀有的普通使用者细节：

- 业务员宋卫强充值 50 元，认为大约只够一周地铁；因卡不记名、担心丢失，不愿一次充太多；
- 王晓伟在四惠排队，一次充 100 元，希望大约一个月少排一次充值队；
- 刚下火车的张春雨带着儿子买一卡通、充 30 元，并计算公交折扣与返程前退押金的价值。

来源（B，含同期第一人称 C1）：
https://business.sohu.com/20080902/n259336986.shtml

这组材料提供的是实际使用逻辑，而不是平台宣传：

`更大充值金额 → 更少充值劳动`，

但同时：

`匿名卡余额越大 → 丢失后的不可恢复损失越大`。

哈尔滨 2008 年同期采访提供了反例：王女士给公交 IC 卡充值 100 元，用掉十几元后丢卡，因为不能挂失而无法追回余款。

来源（B + C1）：
https://news.sina.com.cn/s/2008-03-06/002113525134s.shtml

所以一张 archive 中的“卡余额”如果缺乏实名/挂失语义，不能被后来的账户型钱包概念覆盖。

---

## 7. 2011 上海：“网上充”证明 online payment 与 physical write-back 是两个状态

2011 年上海“网上充”平台上线时，同期报道明确说明，用户需要登录 `www.sptcc.com`，并购买一个连接个人电脑的**网上充交易终端**，才能完成充资、移资、查询、续期等操作。

来源（B，同期报道）：
https://news.sina.com.cn/c/2011-05-03/152022399111.shtml

这留下本文件最重要的 old-Web 状态缺口之一：

> **支付或后台交易发生在 Web 上，不代表物理卡芯片中的可刷价值已经自动变化。**

至少可能存在：

`Web 支付/后台记账`
→ `本地交易终端/读写器`
→ `把新价值写回实体卡`
→ `下次验证器读到新值`

因此看到历史“充值成功”页时，必须继续问：

- 成功的是支付还是写卡？
- 页面是在写卡之前还是之后显示？
- PC 终端是否在线？
- 卡片是否一直插在/靠近读写设备？
- 写卡中断怎样恢复？
- 支付已扣款但写卡失败怎么办？

本轮来源只证明“需要 PC 交易终端”这一事实；**它没有给出精确浏览器、ActiveX、驱动版本或底层协议**。这些不能猜，应继续从安装手册、驱动包、帮助页或真实 historical capture 补证。

---

## 8. 2013 北京 NFC：后台账户、圈存、手机硬件和离线刷卡必须分开

2013 年北京移动与北京市政交通一卡通推出 NFC 手机一卡通时，人民日报同期说明非常适合建立状态模型：

- NFC-SIM 承载交通卡功能；
- 手机账户与一卡通账户是两个账户；
- 可通过银联给后台账户充值；
- 之后还要执行“圈存”，把钱转进真正刷卡使用的一卡通账户；
- 完整业务只支持特定 NFC 手机和专用 NFC-SIM；
- 手机自动关机后，依靠残余电量/NFC 仍可完成若干次刷卡。

来源（B，人民日报）：
https://cpc.people.com.cn/n/2013/0722/c83083-22273798.html

因此：

`phone account balance > 0` ≠ `transit purse balance > 0`；

`online recharge completed` ≠ `circle-store completed`；

`phone has no Internet` ≠ `ride authorization impossible`；

`phone supports NFC in generic specs` ≠ `specific transit-card emulation works`。

这也是 old-Web archaeology 特别值得保存的一点：**Web/移动网络管理层和现场离线授权层可以同时存在。**

---

## 9. 2015 作为 scope edge：移动支付入口开始靠近卡片，但兼容矩阵没有消失

2015 年北京一卡通与微信/NFC 结合的充值说明，已经把支付、贴卡读取和充值进一步压进手机。但公开材料仍要求 NFC Android 设备与特定支持条件。

来源（C，平台/自媒体转载，降级使用，仅证明功能线索）：
https://mt.sohu.com/20150927/n422187869.shtml

这条材料不承担“普及率”结论，也不用于证明 2015 年所有 Android 或所有一卡通卡种都能使用。

它只说明本仓主时间窗末端已经出现一个明确迁移方向：

`PC + Web + 外接读写终端`
→ `手机 + 支付 App + NFC 读写/安全元件`

而真正的可执行性仍由硬件、OS、卡种、支付和交通后台共同决定。

---

## 10. 本轮新增 state gaps

### 10.1 public-shell / fare-backend gap

公开网页、帮助页、充值入口存在，不等于其后端票务服务当时可用。

### 10.2 payment-commit / card-writeback gap

银行卡/支付平台扣款成功，不等于新价值已经写入物理卡或安全元件。

### 10.3 backend-account / chip-purse gap

后台账户有余额，不等于闸机读取的卡内钱包有余额。

2013 NFC-SIM 的“充值→圈存”是直接证据。

### 10.4 displayed-balance / validator-balance gap

网页/手机查询显示的余额和验证器此刻读取到的余额可能来自不同状态层或不同同步时点。

### 10.5 recharge-point / rechargeability gap

一个网站列出“充值点”，不等于某个历史日期该点仍营业、当前卡种可充、设备正常或无需排队。

### 10.6 accepted-city / accepted-line gap

“某城市支持”不能自动推出所有运营者、所有线路、所有闸机同时支持。

### 10.7 interoperability / local-discount gap

卡能跨城刷，不等于自动获得当地居民/换乘/学生/老人优惠。

### 10.8 concession-card / human-entitlement gap

卡内优惠状态存在，不等于持卡者此刻仍满足资格；反过来，人真实有资格，也可能因为卡未更新、丢失、失效而无法在机器上执行优惠。

### 10.9 phone-support / card-emulation gap

“手机有 NFC”只是硬件能力线索，不足以证明运营商 SIM、安全元件、OS、应用与交通卡方案兼容。

### 10.10 online-management / offline-authorization gap

Web/手机可以管理账户，不等于每次上车都向 Internet 在线查询；交通卡常常必须在弱网或无公网情况下快速授权。

### 10.11 tap-transaction / human-ride gap

一次刷卡日志只证明某张卡在某设备发生事件；不能单独证明持卡人身份、完整起终点、出行目的，甚至不能在所有票制下证明最终完成整段旅程。

### 10.12 loss / recoverable-value gap

物理卡丢失后能否挂失、追回余额，取决于实名/匿名、产品规则与后台账户绑定，不能按今天的实名钱包常识倒推。

### 10.13 fare-rule temporal drift

一张 2008 页面上的折扣/票价说明只能说明对应时间窗口的制度规则，不应拿现代规则重新解释历史交易。

### 10.14 recharge-network temporal drift

历史充值网点是高度动态的基础设施数据：开店、撤点、设备升级都会改变“这个地址能不能充值”。

### 10.15 service-coverage temporal drift

某卡支持公交、地铁、出租车等功能的范围会逐年变化；后来的产品总览不能倒投成首发即有完整覆盖。

### 10.16 historical-success-page / authoritative-chip-state gap

archive 若保存一张“交易成功”结果页，仍不一定保存：

- 支付流水；
- 写卡最终状态；
- 失败恢复；
- 卡内余额；
- 下一次闸机读取结果。

所以“成功页”不能被当成端到端 transaction proof。

---

## 11. Old-Web preservation bias：最容易留下的是说明，最难留下的是城市真正执行的状态

### 11.1 Public help pages survive better than private fare state

Wayback 更可能保存：

- 交通卡公司主页；
- 常见问题；
- 充值流程图；
- 网点地址；
- 票价/押金说明；
- 手机支持列表。

它天然不应该保存普通人的：

- 实时余额；
- 交易流水；
- 乘车轨迹；
- 绑定手机号；
- 支付账户；
- 实名优惠资格。

这不是“archive 不完整”这么简单，还是**隐私边界本来就把最接近真实生活执行的状态挡在公共 Web 之外**。

### 11.2 Device-mediated service cannot be reconstructed from DOM alone

2011 上海案例意味着，即使完整拿到 HTML/CSS/JS，仍可能缺少：

- USB/专用读卡终端；
- 驱动；
- 浏览器插件/控件；
- 本地服务；
- 卡片协议；
- 后端握手；
- 实体 IC 卡。

所以页面视觉复原不是事务复原。

### 11.3 Current-backend rehydration is not historical replay

如果今天打开一个旧帮助页/旧 URL，却调用当前交通卡后端、当前票价、当前充值点数据库或当前卡产品配置，只能标为：

`current-backend rehydration`

不能叫 2011 transaction replay。

### 11.4 Dynamic lists fossilize badly

充值点、支持手机型号、可用线路、票价和优惠规则都是时变数据库。一个 capture datetime 必须与其显示的数据有效期分开记录。

---

## 12. 历史 Web 验证状态

本轮针对约 2000s–early 2010s 的 `sptcc.com`、北京交通卡相关历史页面进行了 archive locator / historical replay 检索，但没有取得一份可以实际逐项核验以下字段的合格 memento：

- original URL；
- capture URL；
- capture datetime；
- HTTP status；
- charset；
- DOM；
- form action；
- 脚本/控件依赖；
- 历史余额/充值后端语义。

因此本轮状态严格记录为：

> **M1 verified historical transit-card Web capture: NOT ACHIEVED IN THIS SLICE**

这只表示“本轮没有完成验证”，**不等于 Wayback/其他 archive 没有保存**，也不等于相关历史页面当时不存在。

后续若找到候选 locator，必须实际打开并按 `docs/METHOD.md`、`docs/CITATION.md` 记录，才能升级证据状态。

---

## 13. 浏览器/运行环境：已知与未知必须分开

### 已知

- 2011 上海“网上充”明确需要连接个人电脑的交易终端；
- 2013 北京 NFC 手机一卡通明确受手机型号、NFC 与 NFC-SIM 支持范围限制。

### 未知/不得推断

本轮尚未找到足够强的一手手册来证明 2011 上海具体使用：

- IE 哪一版本；
- 是否 ActiveX；
- 何种 USB 驱动；
- Windows 哪一版本；
- 是否需要管理员权限；
- 写卡失败后的事务恢复协议。

这些都应保持 `unknown`，不能因为 2011 年许多金融/政务服务常用 IE/ActiveX 就类推。

---

## 14. Evidence grading

| 事实 | 来源 | 等级 | 可证明 | 不可证明 |
|---|---|---:|---|---|
| 上海交通卡公司 1999-05-25 成立并承担中央清分 | 公司官网 | A | 机构、项目与后台职责 | 首日乘客规模、家庭 Web 使用 |
| 北京 2006-05-10 刷卡票制与纸月票迁移 | 中国政府网/同期北京日报 | A/B | 制度切换、卡种与时间 | 所有人自愿选择 |
| 北京 2008 充值/丢卡/游客经验 | 新华社转载 + 同期受访者 | B/C1 | 若干真实用户操作逻辑 | 全国平均充值额或心理 |
| 哈尔滨 2008 丢卡不可挂失 | 同期媒体 + 第一人称 | B/C1 | 一条真实损失路径 | 所有城市所有卡规则 |
| 上海 2011 网上充需 PC 交易终端 | 同期媒体 | B | Web 与物理写卡并存 | 精确浏览器/控件协议 |
| 北京 2013 NFC-SIM、后台账户、圈存、设备限制 | 人民日报 | B | 明确状态机与支持边界 | 大众普及率 |
| 2015 NFC/微信贴卡充值 | 平台/自媒体转载 | C | 功能线索 | 完整支持矩阵、采用率 |

---

## 15. 反例与后见之明风险

### 15.1 不要把 closed-loop digital transit 写成 public Internet adoption

交通卡可以高度数字化，同时完全不要求乘客当时拥有家庭互联网。

### 15.2 不要把 stored value 写成 bank account

早期匿名交通卡的余额、挂失和退款语义与实名银行/支付账户不同。

### 15.3 不要把 Web top-up 写成 server-only transaction

2011 上海案例直接证明物理写卡设备仍可能是端到端链条的一部分。

### 15.4 不要把 NFC 写成 generic phone capability

交通卡可执行性依赖完整兼容矩阵，而不是规格表上一个“NFC=true”。

### 15.5 不要用今日覆盖范围重建过去

今天一个品牌可能支持多城市、多线路、多支付方式；历史时点必须按当时产品、线路和票制分别核验。

### 15.6 不要以“页面无历史余额”推断无人使用

真实余额和乘车流水本来就是私有状态，公共 archive 不应该能看见。

---

## 16. 下一步最高价值证据

1. 找到 1999–2001 上海交通卡同期技术/运营文档，确认首发线路、读写器、离线交易与中央清分流程。
2. 找 2006 北京一卡通技术手册，区分公交车载机离线记录、上传周期、地铁闸机与后台结算。
3. 找 2011 上海网上充客户端/交易终端安装说明、驱动包、帮助页或 archived download；特别核验浏览器和本地控件，而不是猜 ActiveX。
4. 找 2013 北京 NFC-SIM 用户手册或 FAQ，补圈存失败、换机、SIM 损坏、余额迁移与挂失语义。
5. 找 2014–2015 跨城市互联的同期线路/卡种清单，建立“标准宣称—城市接入—具体线路—优惠规则”四层矩阵。
6. 尝试通过 Wayback、Common Crawl、ArchiveTeam 等获取一份真正可验证的 `sptcc.com` 历史 Web capture；优先保存 original URL / capture datetime / charset / form action / script and download dependencies。

---

## 17. 本轮改变了什么

此前很多 old-Web state-gap 都围绕“表单提交以后，后台到底有没有完成事务”。交通卡增加了一类更特殊的历史对象：

> **Web 事务结束以后，结果还必须重新落回一块真实物理介质，才可能在街上的闸机或公交车上被执行。**

因此它把 old-Web archaeology 从 `browser → server` 再向现实世界推进了一步：

`browser/payment`
→ `backend`
→ `physical card / secure element`
→ `offline validator`
→ `clearing system`
→ `actual human movement`

一张保存得非常完整的“网上充”页面，仍然可能离“这个人第二天早晨真的刷卡上班”隔着四五个完全不可见的系统。

这正是为什么中文旧网研究不能只问页面长什么样，还必须问**页面之外的机器和制度怎样把它变成生活。**
