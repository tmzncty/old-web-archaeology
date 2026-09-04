# ONLINE_SHOP_SELLER_ONBOARDING_DISCOVERABILITY_ESCROW_RATING_AND_SETTLEMENT_STATE_GAPS_2003_2010.md

> 范围：2003–2010 中文旧网中的 C2C / 小型网店卖家端状态、页面可见性、支付担保、排序、评价、结算与现实履约  
> 状态：research note / execution-state model  
> 关联生活史：`tmzncty/how-people-lived/topics/self-employment-business-route-executability-and-platform-dependent-livelihoods-china-1979-2025.zh-CN.md`  
> 方法边界：本条目不是中国电子商务通史，也不把今天的平台界面倒推为 2000 年代页面；主体严格留在本仓约 1995–2015 中文旧网 scope 内。

## 0. 为什么“开过网店”不能从一个店铺页面直接证明

本仓已经分别研究招聘、兼职 BBS、支付/信贷、个人账号、平台关系图和影视中的旧网使用语境。网店卖家有一条独立的执行链，因为一个公开店铺页面只覆盖真实经营过程的一小部分。

卖家端更接近：

```text
platform exists
→ member registration
→ identity / verification state
→ seller entitlement
→ shop creation
→ listing creation
→ listing indexed / ranked / exposed
→ buyer inquiry / IM handoff
→ order creation
→ payment / escrow lock
→ seller notified
→ shipment
→ receipt
→ buyer confirmation
→ escrow release / settlement
→ rating / reputation update
→ refund / dispute / freeze if any
→ shop continuity / migration / closure
```

因此固定边界：

- `registration page exists ≠ account created`
- `account exists ≠ seller entitlement`
- `shop exists ≠ listing exists`
- `listing exists ≠ listing searchable`
- `listing searchable ≠ listing meaningfully exposed`
- `buyer inquiry ≠ order`
- `order created ≠ paid`
- `payment locked ≠ seller can use funds`
- `shipment ≠ receipt`
- `receipt ≠ escrow released`
- `delivered ≠ profit`
- `rating displayed ≠ reputation state immutable`
- `storefront URL survives ≠ historical order/payment backend survives`
- `GMV ≠ seller income`

这条状态机解释了为什么旧网考古如果只保存 HTML，很容易高估“店铺存在”的历史信息量。

---

## 1. Evidence contract

沿用 `docs/METHOD.md`：

- **A**：原始/同时代页面、官方公告、历史 capture、软件/服务手册；
- **B**：同期新闻、记者观察、同期用户教程；
- **C**：后来回忆或近年历史整理；
- **D**：研究者状态机、保存偏差与机制推断。

本轮使用的核心卖家操作材料以 **B** 为主，辅以近同时代回顾。需要特别说明：

> **同期报纸说“卖家这样操作” ≠ 本仓已经取得并验证当时 production seller backend 的 A 级 WARC。**

搜索结果、后来 VOD/新闻存档和历史教程只能支持其各自窄 claim，不能填补缺失的登录 session、订单数据库、支付 callback 或历史 DOM。

---

## 2. 2005：开店已经形成一套可以被公开教授的 Web 操作知识

### Claim OWR-SELLER-2005-01

2005 年《金陵晚报》刊出淘宝会员撰写的《淘宝卖家开店必修》，教程从注册、会员名等最初步骤展开，并把读者直接定位为“来开店赚钱”的卖家。

来源：

- 《淘宝卖家开店必修》，2005-07-19：https://news.sina.com.cn/s/2005-07-19/09006474272s.shtml
- 等级：B（同期用户教程 / 报纸转载）

它可以支持：

- 到 2005 年，面向普通用户的开店流程已经足够稳定，能形成逐步教程；
- “会员账号”开始承担经营入口作用；
- 网店经营需要一种新的 procedural knowledge，而不只是会浏览网页。

它不能支持：

- 教程截图/字段今天仍等同于 2005 production 页面；
- 所有注册账号都完成开店；
- 店铺创建后一定有商品、有流量或有成交；
- 浏览器、字符集、Cookie/session 机制已由本轮验证。

新增：**registration-form version gap** 与 **seller-entitlement gap**。

一个历史注册页 capture 即使恢复，也只能回答“当时要求输入什么”，未必能回答账号是否实际创建、是否完成卖家资格、是否后来失效。

---

## 3. 2003–2005：第三方担保把“支付”拆成多个状态

### Claim OWR-SELLER-PAY-2003-01

近同时代电子支付史材料对 2003 年早期担保交易的描述是：买家先把款项交给第三方；卖家得到付款通知后发货；买家确认收货后，第三方再把款项交给卖家。

来源：

- 2009 年网络支付历史整理：https://www.cnblogs.com/tony-net/archive/2009/10/02/1577447.html
- 等级：B/C（近同时代回顾；用于状态机，不作为完整原交易页面证据）

这使交易至少具有：

```text
order exists
→ buyer funds submitted
→ escrow/payment state accepted
→ seller notification
→ shipment
→ buyer receipt/confirmation
→ settlement released
```

因此新增：

- **order/payment gap**；
- **escrow-lock gap**；
- **seller-notification gap**；
- **escrow-release gap**；
- **settlement-history gap**。

固定边界：

> **paid by buyer ≠ settled to seller**

> **seller notified ≠ shipment occurred**

> **shipment occurred ≠ buyer confirmed**

> **buyer confirmed ≠ historical settlement record is publicly recoverable**

这是一个典型的旧网保存偏差：最重要的状态往往都在私人后台，而不是公共商品页。

---

## 4. 2006：“店还在”但排序规则变了，现实经营能力也会变

### Claim OWR-SELLER-RANK-2006-01

2006 年 5 月，淘宝推出“招财进宝”竞价推荐服务。同期媒体报道的基本机制是：卖家可以通过付费取得推荐/更靠前的展示位置，关键词搜索中的排列与竞价等因素相关。

来源：

- 《卖家扬言集体下架 淘宝大幅降“推荐费”》，2006-05-30：https://news.sina.com.cn/c/2006-05-30/02459061654s.shtml
- 《淘宝“招财进宝”满月便夭折》，2006-06-12：https://news.sohu.com/20060612/n243677800.shtml
- 《淘宝网“招财进宝”夭折》，2006-06-13：https://business.sohu.com/20060613/n243710887.shtml
- 等级：B（同期媒体；具体参与卖家人数在不同报道间存在差异）

### Claim OWR-SELLER-RANK-2006-02

同期报道记录卖家以商品下架、停止使用旺旺、提取支付宝余额、签名/投票等方式抗议；淘宝最终取消相关服务并处理费用退还。

另一篇同期报道给出 6,000+ 卖家签名等数字；由于媒体口径不同，本条目不把任何一个参与数量当成精确平台人口。

补充来源：

- 浙江在线 2006-06-01：https://zjnews.zjol.com.cn/05zjnews/system/2006/06/01/006655604.shtml
- 2006-06-02 报道：https://news.sina.com.cn/o/2006-06-02/05499095863s.shtml

### 考古意义：platform-policy state ≠ storefront state

这里出现一个非常重要的旧网对象：**同一个店铺 URL、同一个商品页面可能没有删除，但它的被发现概率和经营价值已经发生变化。**

因此新增：

- **ranking/exposure gap**；
- **paid-placement gap**；
- **governance-state gap**；
- **seller-protest/migration gap**。

固定边界：

> **shop page unchanged ≠ commercial state unchanged**

> **search result capture at t1 ≠ ranking rule at t2**

> **listing indexed ≠ buyer would realistically encounter it**

> **platform rule announced ≠ every seller affected equally**

这类历史变化无法仅靠“有没有 Wayback 页面”恢复。排序算法、竞价状态和每次查询时的候选集本身是动态的。

---

## 5. 2008–2009：店铺背后还有货源、宿舍、快递和家庭关系

### Claim OWR-SELLER-OFFLINE-2008-01

2008 年《中国青年报》报道义乌工商职业技术学院的学生网上创业时，记录到校内已有大量网店与参与学生，快递企业进入校园，一些学生依托邻近小商品市场获得货源。

来源：

- 《义乌商职院：千余学生网上淘金年入2500万元》，2008-07-07：https://zqb.cyol.com/content/2008-07/07/content_2252821.htm
- 等级：B（同期媒体 + 学校/个案数据；义乌环境不可代表全国高校）

2009 年“自雇”报道又记录一名学生/毕业生经营网店时利用父亲已有的医药供应关系。

来源：

- 《开网店做家教 大学生兴起“自雇”就业》，2009-02-20：https://edu.sina.com.cn/j/2009-02-20/1405165415.shtml
- 等级：B（同期采访；平台卖家数字不外推）

### 考古意义：public Web 保存不了 business handoff

一张商品页通常不保存：

- 商品从哪个批发市场/家庭关系进入卖家手里；
- 谁负责拍照、打包；
- 宿舍是否兼作库存；
- 快递何时取件；
- 家庭是否垫资；
- 线下退货/换货如何处理；
- 经营者是否同时仍是学生。

新增：

- **inventory/source gap**；
- **offline-supply handoff gap**；
- **packing/shipping labor gap**；
- **household-capital gap**；
- **seller-life-stage gap**。

所以：

> **Web storefront ≠ complete business organization**

旧网可以保存商品和店铺，但经常保存不了让那个页面持续有货可卖的现实基础设施。

---

## 6. Search / ranking / IM / payment 是一组跨服务 transaction stack

一笔典型早期网购并不一定完全发生在单一页面：

```text
platform search/category page
→ product detail
→ seller profile/reputation
→ Wangwang / other IM inquiry
→ order page
→ payment/escrow service
→ seller backend
→ courier / physical parcel
→ buyer confirmation
→ rating/review page
→ seller settlement account
```

这些层的保存概率极不相同。

公共档案更容易保存：

- 商品页；
- 店铺首页；
- 帮助页；
- 新闻/公告。

更容易丢失或不应公开的则是：

- 登录后的订单；
- 真实买卖双方 IM；
- 地址/电话；
- 身份认证；
- 银行和支付记录；
- escrow 状态；
- 退款争议；
- 账户冻结；
- 私人评价申诉。

因此新增一个总括概念：

> **transaction-state invisibility / 交易状态不可见性**：历史上最决定“这家店真的完成了交易吗”的状态，恰恰最不容易成为公共 Web artifact。

---

## 7. Rating / reputation 也不是一个静态数字

早期 C2C 的陌生人交易高度依赖卖家信誉、评价和历史交易信息。但历史 capture 看到一个信誉值，只能证明某个时点页面显示了某个状态。

完整链条可能包括：

```text
transaction completion
→ buyer eligible to rate
→ rating submitted
→ score/reputation changes
→ seller responds
→ dispute / deletion / policy adjustment if any
→ future search/trust effects
```

因此新增：

- **rating-eligibility gap**；
- **rating-mutation gap**；
- **reputation-policy gap**；
- **review-to-future-discoverability gap**。

固定边界：

> **rating shown ≠ rating history complete**

> **high score ≠ all transactions visible**

> **review exists ≠ buyer identity should be republished**

本轮没有取得足够一手材料去精确复原 2003–2010 每一版评价算法，因此只保留状态模型，不猜分值公式。

---

## 8. Cross-platform migration：关店不一定等于退出经营

2006 年争议中已经出现卖家威胁或讨论迁往其他平台。对生活史来说，这意味着店铺死亡和生计死亡必须分开：

```text
platform A account/shop closes
→ seller retains goods / customers / phone / IM / supplier relations
→ seller recreates storefront on platform B or offline
```

也可能相反：

```text
storefront remains technically accessible
→ seller stops updating
→ stock unavailable
→ contact dead
→ no orders fulfilled
```

新增：

- **cross-platform migration gap**；
- **merchant-contact continuity gap**；
- **dormant-store gap**。

因此：

> **shop disappeared ≠ merchant disappeared**

> **shop survived ≠ merchant still trading**

这与本仓已有的校友录、Webmail、联系人生命周期研究形成同构关系：URL 的连续性、账号的连续性和现实人的连续性是三种不同对象。

---

## 9. 与影视证据的边界：《家有儿女》的购物网站只能作为 usage-context

本仓已有 `FICTIONAL_SCREEN_WEB_USAGE_CONTEXT_CANON_AND_RECONSTRUCTION_GAPS_2004_2009.md`。其中《家有儿女》第一季“雪儿网站”情节把“借启动钱、建购物网站、没有买家、网站被黑”等概念放进家庭情景喜剧。

这可以作为 **SF-context**：说明这些网络经营概念在当时已经具有文化可读性。

但必须固定：

> **fictional shopping site ≠ historical C2C platform artifact**

> **plot says no buyers ≠ real traffic analytics**

> **fictional hack ≠ historical vulnerability evidence**

> **on-screen interface ≠ verified production Taobao/EachNet UI**

影视材料帮助恢复“普通家庭如何理解网店”，真正的页面、账号、排序、支付与交易状态仍需旧网证据。

---

## 10. 本轮没有可靠复原的东西

本轮**没有**取得并逐项验证以下整套 A 级 production artifacts：

- 2003–2006 淘宝普通卖家完整注册/开店 WARC；
- 实际 seller onboarding session；
- 历史订单后台；
- 支付 callback / escrow backend；
- 买家确认后的结算数据库；
- 每一版历史搜索排序算法；
- 历史旺旺私聊记录；
- 真实评价申诉后台。

因此没有猜：

- 具体 DOM/CSS；
- GB2312/GBK/UTF-8 的每页配置；
- 必须使用的 IE 版本；
- Cookie/session 字段；
- 内部 API；
- Alipay 与 Taobao 后端接口；
- 排名算法权重；
- 已丢失的用户订单状态。

**媒体教程/同期报道是 B，不应伪装成已经验证的 A 级历史 capture。**

“无法仅靠公共页面可靠复原交易”是本轮的正式结论之一。

---

## 11. 隐私和版权 stop condition

在线交易史天然包含高敏感私人数据：

- 姓名；
- 手机；
- 地址；
- 身份证/认证状态；
- 银行账户；
- 支付余额；
- 订单；
- 物流轨迹；
- 私聊；
- 退款/纠纷。

即使某份历史数据因旧配置曾经公开，本仓也不应为了“补完整状态机”批量重新发布。

本轮不做：

- 尝试登录旧卖家账号；
- 找回普通用户密码；
- 向旧联系方式发测试消息；
- 用私人订单号探测后端；
- 批量保存可识别普通人的评价/地址。

研究平台结构时优先保存字段、状态关系和最小必要证据。

---

## 12. 本轮新增 gap 汇总

- `registration-form version gap`
- `identity-approval gap`
- `seller-entitlement gap`
- `listing/inventory gap`
- `ranking/exposure gap`
- `paid-placement gap`
- `IM-handoff gap`
- `order/payment gap`
- `escrow-lock/release gap`
- `seller-notification gap`
- `shipment/delivery gap`
- `rating-eligibility gap`
- `rating-mutation gap`
- `reputation-policy gap`
- `governance/freeze gap`
- `settlement-history gap`
- `offline-supply handoff gap`
- `cross-platform migration gap`
- `dormant-store gap`
- `private-backend archive gap`
- `GMV-to-income gap`

其中最值得跨案例复用的是三条：

1. **public storefront state ≠ private transaction state**；
2. **URL survival ≠ livelihood survival**；
3. **platform-policy state can change real life without changing the page artifact itself**。

---

## 13. 与 how-people-lived 的交叉结论

旧网侧能告诉我们：普通网店经营的关键对象不是“一张商城网页”，而是一个会变化的交易状态机。

生活史侧则继续追问：

- 谁有资格和资本成为卖家；
- 谁提供货源；
- 一天多少时间花在客服、打包和发货；
- 经营收入何时真的能变成家庭现金；
- 平台规则变化是否迫使人换工作/换平台；
- 网店是学生时代试验、主要生计、家庭副业，还是危机时期备用路线。

两边合起来，可以避免两个常见错误：

> “旧网上有这个店，所以这个人当时经营得很好。”

以及：

> “后来店铺 URL 消失，所以这个人的生意也在那天结束了。”

这两种结论都必须经过现实执行状态和跨平台/线下证据才能成立。

---

## 14. 下一步

1. 尝试合法恢复一个 2004–2006 普通卖家**公开**店铺的至少两个历史时点，优先记录公开字段、URL、商品数、信誉显示和 archive 子资源缺失，不触碰私人后台。
2. 寻找同期官方卖家帮助页，确认每个历史时点的注册、开店、支付和评价规则；帮助页与用户教程分开计 evidence family。
3. 找一个失败/长期低活跃店铺作为反例，避免只研究明星卖家。
4. 比较淘宝、易趣/EachNet 等至少两个平台的卖家迁移成本：账号、信誉、商品数据、客户联系能否带走。
5. 研究 2006 排名争议前后搜索结果 capture 是否可得；如果没有动态候选集/算法证据，就明确停在“规则被同期报道存在”的层级。
6. 与 `how-people-lived` 做一个“网店卖家的一天”life slice：进货、拍照、上线、客服、打包、快递、结算、照护和睡眠。

本轮新增了此前仓库没有独立展开的**卖家 transaction-state invisibility、ranking/exposure 生计接口和 settlement gap**，因此不是饱和轮。
