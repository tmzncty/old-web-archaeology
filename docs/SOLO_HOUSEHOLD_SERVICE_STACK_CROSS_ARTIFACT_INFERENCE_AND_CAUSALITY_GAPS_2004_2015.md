# SOLO_HOUSEHOLD_SERVICE_STACK_CROSS_ARTIFACT_INFERENCE_AND_CAUSALITY_GAPS_2004_2015

> Scope: 约 2004–2015 中文 Web。不是“独居史”，也不是再写一遍租房、外卖、家政、电商或缴费史；本 note 研究的是：当多个旧网页分别显示这些家庭服务已经在线化时，我们能够、以及不能够怎样据此推断一个普通人的私人家庭已经可以独立运行。

Status: method / cross-artifact state-model note  
Last research pass: 2026-09-06  
Companion life-history study: `tmzncty/how-people-lived/topics/living-alone-one-person-households-solo-household-executability-and-service-rebundling-china-1977-2026.zh-CN.md`

## 0. 为什么需要这份交叉 note

本仓已经分别有：

- `ONLINE_RENTAL_LISTINGS_SUBLETS_ROOMMATES_VIEWING_CONTRACT_AND_OCCUPANCY_STATE_GAPS_2005_2015.md`
- `ONLINE_FOOD_ORDERING_MENUS_SERVICE_AREAS_AND_DELIVERY_OUTCOME_GAPS_2004_2010.md`
- `ECOMMERCE_CHECKOUT_DELIVERY_ADDRESS_PICKUP_AND_FULFILLMENT_STATE_GAPS_1999_2015.md`
- `UTILITY_BILL_ACCOUNT_BINDING_PAYMENT_AND_SERVICE_CONTINUITY_STATE_GAPS_2003_2015.md`
- `DOMESTIC_SERVICE_PROFILE_MATCHING_BOOKING_CREDENTIAL_AND_IN_HOME_SERVICE_STATE_GAPS_2008_2015.md`
- `SUPPORT_PAGES_DOWNLOAD_ARTIFACTS_REPAIR_REQUESTS_AND_OUTCOME_GAPS_2005_2015.md`
- `ONLINE_BANKING_REMITTANCE_AND_PAYMENT_STATE_GAPS_1997_2015.md`

每一篇都已经把单项交易拆得很细。真正还缺的是**跨页面推断纪律**：如果 2008 年一座城市同时有网上租房、订餐、购物和缴费页面，研究者很容易从“网页世界越来越完整”跳到“一个人已经可以靠 Internet 独立生活”。这个跳跃没有证据保障。

本 note 因此只做两件事：

1. 把家庭服务组合成一个 cross-artifact state model；
2. 规定哪些生活史因果结论不能从旧网页直接推出。

## 1. 关键区分：service-component existence ≠ solo-household executability

对于一个只有一名常住者的私人住宅，支持栈可能包括：

```text
住房找到并实际入住
+ 餐食获得
+ 日用品补给
+ 水电燃气/通信维持
+ 支付
+ 清洁/家政
+ 维修
+ 生病或异常时 fallback
+ 社交/联络
```

旧 Web 往往只能保存其中每一项的公共壳层。

因此：

```text
rental listing exists
+ food-ordering page exists
+ e-commerce checkout exists
+ utility-payment page exists
+ domestic-service directory exists
≠
同一个现实用户同时能执行这些路线
≠
该用户是一人户
≠
这些 Web 服务导致该用户开始独居
```

这是本 note 的第一条硬规则。

## 2. 为什么 2004–2010 网上订餐仍值得作为“家庭服务栈”部件，而不是独居证据

既有 `ONLINE_FOOD_ORDERING...` note 已记录：2004 年丽华等网络订餐、2006 年 3797 按办公区/住宅区检索餐馆与菜单、2007 年 MSN 机器人订餐、2008 年校园订餐等路径，并已拆开菜单、配送区、订单接收、厨房库存、派送与现实交付。

这类页面能够证明一件生活史上很重要的事：**获得一顿饭逐渐不要求本人做饭，也不要求固定同住者做饭。**

但它不能证明：

- 下单者独居；
- 下单地址是长期住宅；
- 下单者不会做饭；
- 下单者没有家人/室友；
- 网上订餐是其选择一人居住的原因。

一个办公室团体、夫妻家庭、宿舍寝室都可能使用相同订餐入口。

所以 old-Web 只能支持：`food procurement became remotely addressable for some users`，不能支持：`online food ordering created solo living`。

## 3. 2011：网上订餐从“能下单”向 tracking / multi-channel routine 扩展

中国互联网协会 2011-09-29 转载的同期行业报道记录，麦当劳在北京、上海、广州、深圳、天津、佛山、东莞七城启动网络订餐，消费者可在线跟踪订单；网络订餐与电话订餐均收每单 7 元配送费。报道还记录，肯德基网上宅急送已覆盖更多城市；丽华从更早时期开展网上订餐，但广州地区的网络订餐曾运营后取消。

Source (B+, contemporaneous industry-news reprint):  
https://www.isc.org.cn/article/16739.html

这一材料新增三个状态边界。

### 3.1 tracking display ≠ verified courier position

一个历史页面写“订单跟踪”，可能只是：

```text
received → preparing → dispatched → completed
```

的业务状态，也可能有更细信息。没有历史 DOM、脚本、接口或用户截图，不能脑补成今天地图上的实时 GPS 骑手位置。

因此：

**tracking state ≠ physical-location telemetry。**

### 3.2 same service category ≠ same geographic availability

七个城市上线，不代表全国上线；同一品牌不同城市也可能有完全不同配送时段、门店和网络渠道。

### 3.3 channel existence is reversible

丽华广州网上订餐“开过又取消”的同期记录很重要：

```text
service launched
≠ service remains available forever
```

对于一人家庭，某个日常服务如果已经被纳入习惯，渠道下线就会形成 **service-stack regression / 服务栈回退**。历史研究不能只记录 launch date，还要找 termination / city withdrawal / channel replacement。

## 4. 2011：网购已成为重要消费渠道，但“网购能买日百”仍不是家庭运行完成态

CNNIC 的《2011年中国网络购物市场研究报告》显示，截至 2011 年底网络购物用户约 1.94 亿；在网购用户中，39.3% 购买过日用百货，16.7% 购买过餐饮美食服务；网上支付和货到付款都在使用，手机网购也已出现一定规模。

Source (A/B+, CNNIC research report release):  
https://www2.cnnic.cn/n4/2022/0401/c119-1021.html

这里能支持的是：日常家庭补给逐渐拥有更多 remote procurement routes。

不能支持：

```text
网购用户 = 独居者
网购渗透率 = 一人户可执行性
购物页面存在 = 最后一公里已成功
```

既有电商 state model 仍然成立：checkout 之后还有支付识别、商家履约、物流、地址定位、签收与售后。

## 5. 2015：外卖平台化增强了“可寻址商家集合”，仍没有消灭最后一公里

中国网信网 2015-02-03 的同期行业综述把网上订餐描述为当时仍处于快速发展/竞争阶段的细分领域，并记录“饿了么”2009 年上线、2011 年 11 月上线手机网站，之后经历多轮融资。

Source (B, contemporaneous institutional media industry overview):  
https://www.cac.gov.cn/2015-02/03/c_1114223504.htm

这里真正发生的结构变化不是“第一次有人送饭”，而是：

```text
一家餐馆一个电话/网页
→ 聚合平台统一列出许多商家
→ 用户先进入平台，再按地理位置、菜单、价格等寻找供给
```

可以称为 **service discovery aggregation / 服务发现聚合**。

但平台层增加以后，状态链反而更长：

```text
平台显示商户
→ 商户此刻仍营业
→ 当前地址在配送区
→ 菜品仍有库存
→ 下单请求被平台持久化
→ 商户收到
→ 商户接受
→ 备餐
→ 配送能力可用
→ 地址被正确找到
→ 实际交付
```

因此：

**front-end platform reach ≠ last-mile capacity。**

对“一人家庭服务栈”而言，平台降低的是发现/协调成本；物理食物仍必须从厨房移动到门口。

## 6. 家庭支持栈必须按事务逐项取交集，而不是把网页数量相加

假设研究者在某城市某年找到五类页面：

```text
租房 A
订餐 B
电商 C
缴费 D
家政 E
```

不能写成“该城 2009 年已经具备完整数字独居生活”。至少还需要检查：

```text
A 的区域 ∩ B 的配送区 ∩ C 的物流覆盖 ∩ D 的公共事业合作范围 ∩ E 的上门范围
```

而且交集还要包含：

```text
用户的设备/浏览器
支付工具
身份/账号
时间窗口
价格承受能力
现实地址
```

这叫 **cross-service executability intersection / 跨服务可执行性交集**。

网页分别存在，只能证明集合不是空集；不能证明同一个普通人在同一时间、同一地址、同一预算下位于所有集合的交集中。

## 7. “住址”是这些旧 Web 服务之间少数真正共享、但又很难存档的 join key

租房、订餐、电商、上门家政和部分维修都围绕一个现实地址运行。对生活史研究来说，一个人开始拥有稳定私人地址后，很多服务才可能围绕住宅聚合。

但是公开档案恰恰不会、也不应该替我们保存真实用户完整地址历史。

因此存在 **address-join darkness / 地址连接黑区**：

- 公开租房页可能有小区/区域；
- 公开餐饮页可能有配送区；
- 电商页可能有城市覆盖；
- 家政页可能有服务城区；
- 真实用户收货地址、订单、物业户号则属于私人状态。

这意味着 archive 很难证明“这几个公共服务真的同时围绕同一名居民的同一间房运行过”。

禁止为了补这个 join 去使用泄露订单、身份证、电话号码、完整住址或重新识别普通人。

## 8. 一人户推断特别容易被“一个账号”误导

旧网页中看到一个账号、一个订单、一个缴费户号，不能推断现实 household size。

```text
one account ≠ one person
one payer ≠ one resident
one delivery order ≠ one eater
one utility account ≠ one-person household
one rental inquiry ≠ solo tenancy
```

既有 `LOCATION_COPRESENCE_AND_DISTRIBUTED_HOUSEHOLD_INFERENCE_1999_2015.md` 的原则应当扩展到这里：数字身份与现实共同居住关系之间没有自动一一映射。

一名在外地工作的子女可以替父母交水电费；一名室友可以替全屋下单；一个家庭可能共用账户；一个独居者也可能用单位账号或父母银行卡。

## 9. 页面越“生活化”，越容易产生错误的整体性想象

旧 Web 考古有一种特殊的 **service-catalog completeness illusion / 服务目录完整性幻觉**。

当 archive 同时保存“租房”“订餐”“购物”“缴费”“家政”“维修”栏目时，今天的研究者很容易觉得现代城市家庭服务已经完整搬上网。

但目录是商业承诺和信息架构，不是执行账本。

```text
栏目存在
≠ 商户在线
≠ 区域覆盖
≠ 价格可负担
≠ 用户成功注册
≠ 支付成功
≠ 线下履约完成
≠ 下一周仍然可用
```

因此生活史必须从“网站提供了哪些栏目”降到“哪条路线可以完成到现实状态”。

## 10. 可用性与使用密度也不能混淆

2011 CNNIC 数据说明网络购物已达到较大用户规模；2015 网上订餐又成为快速扩张领域。但即使一个服务已经拥有大量用户，也不能推出某个一人户“主要靠它活着”。

真正需要的生活史证据是 **routine integration / 日常整合**：

- 一周几顿饭依赖送餐？
- 日用品是偶尔网购还是持续补给？
- 缴费是每月在线完成还是仍去柜台？
- 家政是应急使用还是稳定替代固定家务？
- 一旦渠道失效，用户切回什么路线？

公共网页通常不保存这种跨周、跨月 routine ledger。

因此：

**service adoption ≠ household dependence。**

## 11. 服务栈的长期变化：Web 首先增加 route portfolio，平台再增加 aggregation

在 old-Web scope 内，可以谨慎提出一条技术形态变化：

### 阶段 A：电话/线下为主，Web 主要负责发现

网站提供电话、地址、菜单、分类信息；事务可能切回电话或现场。

### 阶段 B：Web 开始接收事务

在线表单、购物车、支付、订单号逐渐出现；但商家、物流、上门服务仍在线下完成。

### 阶段 C：聚合平台

平台把大量分散商家、菜单、价格、评价和交易入口放在统一接口中，并逐步延伸到移动端。

对于一人家庭，三阶段都可能降低协调成本，但技术史结论只能是：

**可用路线增多、发现成本下降、部分事务状态变得可见。**

不能直接升级为：

**家庭不再需要亲属/同住者，因此独居增加。**

后一个命题需要人口、住房、收入与生命史证据共同支持。

## 12. 与四种时代未来的接口

本 note 的主体仍严格停留在 2004–2015 中文 Web，不把 2015 以后平台史扩进来。但它为 `how-people-lived` 的长期比较提供一个边界条件：

- 2005–2012 扩张型未来：支持栈部件增多，使“自己的小房子 + 外部城市服务”更容易被想象和执行；
- 2015 附近：聚合平台开始把分散服务组织到统一入口，但一人户形成不能归因于平台；
- 2020–2022 的服务网中断与 2023–2026 的 fallback/冗余问题属于 life-history companion 的后续范围，不在本仓本 note 内扩写。

## 13. Archive survival：公共服务壳层很亮，真实家庭组合很暗

这类研究存在很强的 **public-service-shell / private-household-composition asymmetry**。

最容易保存：

- 首页；
- 菜单；
- 服务区说明；
- 商户目录；
- 帮助页；
- 价格与宣传；
- 订单流程截图；
- 新闻报道。

最难且不应公开保存：

- 某人的持续收货地址；
- 同住者名单；
- 支付凭据；
- 水电户号；
- 家政进入住宅的记录；
- 医疗/紧急情况；
- 跨平台订单组合。

因此旧 Web 天然更擅长证明 **service possibilities**，不擅长证明 **whole-household routines**。

## 14. M1 / M3 状态与负结果

本轮没有取得并实际检查一份能够同时覆盖“租房 → 入住 → 订餐/购物 → 缴费/上门服务”的单一用户历史 WARC/Wayback transaction sequence。

这不是一个合理的 M1 目标：此类完整序列本来会跨越多个站点、认证账号和高度私人数据。

对 2011 麦当劳网络订餐与 2011 饿了么手机网站，目前仍只有同期/近同时期文本证据；本轮没有 verified historical memento，因此以下保持 unknown：

- original DOM / charset；
- order-tracking 实际字段；
- cookie/session；
- browser requirements；
- 手机网站是 WML、XHTML-MP 还是其他具体页面技术；
- 平台—商家订单 handoff protocol；
- 用户现实家庭构成。

所以本 note 不宣称完成新的 M1，也不把今天可访问的新闻页冒充 2011 原始交易界面。

## 15. 证据等级

| Evidence | Grade | What it supports | What it does not support |
|---|---:|---|---|
| 2011 中国互联网协会：麦当劳七城网上订餐、订单跟踪、丽华广州渠道取消 | B+ | channel scope, tracking claim, reversibility | exact DOM, GPS tracking, user household type |
| 2011 CNNIC 网购报告 | A/B+ | network shopping scale, daily-goods/service categories | solo-living causality |
| 2015 中国网信网网上订餐行业综述 | B | Ele.me launch/mobile-site timeline, platformization context | exact 2009/2011 client implementation |
| existing repo rental/food/ecommerce/utility/domestic-service notes | repo prior art | transaction-state decomposition | one user’s combined routine |

## 16. 它改变 old-Web 研究的哪一点

以前每个状态模型主要问：

> 这个网站声称能完成的单项任务，用户到底有没有走到现实结果？

这一轮增加第二层问题：

> 当很多网站都各自变得“可交易”以后，我们能不能把它们拼成一种新的普通生活？

答案是：**可以提出支持栈机制，但不能从公共网页直接推出家庭结构因果。**

Internet 和 Web 的确逐步把找房、找饭、买东西、缴费、叫服务变成可远程寻址的事务；这会降低一个私人家庭的部分协调成本。但“一人户为什么增加”仍需要人口、住房、收入、婚育、迁移与第一人称生命史证据。

因此最稳健的交叉结论是：

**old Web 能告诉我们，一个人独自维持住宅所需要的许多外部部件何时逐渐上线；它不能仅凭这些上线页面证明，人们就是因此开始一个人住。**