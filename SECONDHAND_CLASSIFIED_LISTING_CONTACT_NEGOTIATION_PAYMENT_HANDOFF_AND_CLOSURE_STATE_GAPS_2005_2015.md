# Secondhand classifieds, listing, contact, negotiation, payment, handoff and closure state gaps, 2005–2015

> Scope: 中文旧网约 2005–2015。研究校园 BBS、分类信息网站、移动分类信息、淘宝二手/闲鱼等二手交易入口中，一件普通闲置物从“有人想卖”到“另一个人真正拿到”的页面、状态机与保存缺口。
>
> 不做全球二手市场史，也不把 1980s–1990s 旧货市场、Boston Computer Exchange、eBay 或 2016–2026 移动二手平台无限写进本仓。更长的生活史、跨国对照与 2020s “可逆生活”写入 `tmzncty/how-people-lived` 配套专题：`topics/from-buying-things-to-being-able-to-exit-them-secondhand-markets-resale-liquidity-and-material-reversibility-china-1979-2026.zh-CN.md`。

核心问题不是：

> “旧网页上有没有一个‘二手转让’栏目？”

而是：

> **某一历史时点，一条中文旧网二手信息究竟推进到了哪个 authoritative state；它最后是否真的对应一次物品所有/占有关系的改变？**

二手交易尤其容易被 archive 误导，因为它天然跨越：

```text
public board / category
→ listing
→ seller identity / contact endpoint
→ search / browse exposure
→ inquiry
→ phone / QQ / site message
→ negotiation
→ agreement
→ payment / escrow / cash plan
→ meeting / pickup / shipment
→ inspection / acceptance
→ fund release
→ listing close / delete / expire
```

archive 最容易保存前半段，最难保存真正让物品换主的后半段。

---

## 0. 本轮结论摘要

本轮可以确认的历史基线：

1. **2008 年**广州高校同期报道已经把校园 BBS 记录为毕业生处理带不走物品的优先渠道；受访学生明确说“E时代我们都是网上甩卖”。网页让出售从“本人站在地摊旁”变成可以异步等待联系，但真正议价、看货和交付仍大量回到宿舍、电话和现实空间。
2. **2009 年**北京高校同期报道继续记录清华、北大、人大等校园 BBS 二手板活跃，毕业季大量旧书、自行车、小家电和生活用品进入跨届流通。
3. **2010 年**分类信息行业报道已把“二手物品转让”列为从报纸分类广告迁移到 58 同城、赶集网等城市化可搜索列表的典型业务；同年赶集移动端已支持附近信息、搜索、发布、点击电话和短信分享。
4. **2011 年**同期报道中的“跳蚤族”已经在论坛、58、赶集、社区二手等多渠道之间处理婴儿车、豆浆机、风扇等家庭闲置，说明二手 Web 不只服务毕业/搬家这种年度节点。
5. **2013 年**淘宝二手“一键转卖”把既有购买记录直接转成新的二手 listing 输入；同一账户里的商品第一次更明确地形成 `buy → use/idle → relist` 的可见生命周期。
6. **2014 年**闲鱼上线时，同期报道明确把它与 58/赶集式“信息发布后再线下沟通”区分：淘宝账号可登录、个人无需开店即可发布、支付宝可进入交易链、买家收货后再确认付款。
7. 因此 2005–2015 的中文旧网二手交易不是一条简单的“线下 → 线上”替代史，而是从 **Web 发现 + off-Web 成交**，逐渐出现 **listing + identity + message + escrow/payment + shipping + acceptance** 的更多站内状态。
8. 二手交易存在强烈的历史可见性反转：**最容易保存的是“有人曾经想卖”，最不容易保存的是“是否卖成、成交价多少、谁拿走、为什么关闭”。**
9. 本轮尝试直接验证约 2009–2011 年 `58.com` 二手分类的 Wayback replay；当前访问链拒绝未经可追溯搜索结果建立 provenance 的构造 archive URL，未取得可逐项核验 `capture_datetime / HTTP / charset / DOM / form / contact / historical listing state` 的合格 memento。因此：**M1 verified 2009–2011 58.com secondhand historical capture: NOT ACHIEVED IN THIS SLICE**。

---

## 1. 开工前查重与范围边界

本仓已有大量 transaction/state-gap 研究，包括：

- 电商 checkout / delivery / fulfillment；
- 网银 / remittance；
- parcel tracking；
- rental listing / roommate；
- dating / matchmaking；
- resume / recruiter search；
- domestic service matching；
- railway ticketing；
- hospital appointment；
- campus card；
- consumer complaint。

本稿不重复这些对象。

真正新增的是：

> **普通人本人持有的一件旧物，怎样通过旧 Web 被另一个陌生人或弱关系买家发现，并最终退出原持有人的生活。**

因此必须区分：

- `merchant inventory` 与 `personal idle item`；
- `new-goods ecommerce order` 与 `used-goods person-to-person negotiation`；
- `listing existence` 与 `physical object existence`；
- `asking price` 与 `transaction price`；
- `platform account` 与现实物品权属；
- `message/contact` 与真实成交；
- `payment` 与 physical handoff；
- `listing closure` 与真正售出。

### 1.1 时间边界

本仓主对象从约 2005 年中文校园 BBS/分类信息二手场景写起，到 2015 年移动化、担保交易和专业二手服务过渡。

1998《旧货流通管理办法（试行）》只作为**前史/制度边界**：它证明互联网之前旧货市场已承担信息、评估、结算、翻新、保管、运输等功能；不把本仓改写成 1980s 旧货商业史。

### 1.2 海外对象不进入本仓主体

Boston Computer Exchange、eBay 的比较只在 `how-people-lived` 用于说明：

- online listing 早于 full online transaction；
- 买家池扩大后，陌生人信誉会成为共同基础设施问题。

本仓主体继续只讨论中文旧网。

---

## 2. 研究单位：不要把“一条二手帖”当成整笔交易

### 2.1 platform / board / category

可能是：

- 校园 BBS 二手版；
- 综合论坛跳蚤板；
- 58 同城城市二手频道；
- 赶集网二手频道；
- 社区论坛；
- 淘宝二手；
- 闲鱼。

板块存在只证明平台给了这种用途一个入口。

### 2.2 listing

listing 至少可能包含：

- 标题；
- 分类；
- 物品名称/型号；
- asking price；
- “几成新”等 condition claim；
- 地点；
- 照片；
- 发布时间；
- 联系方式或联系按钮；
- seller account；
- 状态标签。

它首先是一份**卖方声明**。

### 2.3 physical object

物体本身是独立对象。

研究时要问：

- listing 中的照片是不是该物品；
- 物品是否仍在卖方手中；
- 是否已经损坏/售出；
- 型号、配件、序列号是否一致；
- 是否存在权属或转让限制。

因此：

`listing metadata != authoritative object state`。

### 2.4 seller identity

可能是：

- BBS ID；
- 手机号；
- QQ；
- 分类信息账号；
- 淘宝账号；
- 实名支付身份；
- 校园弱实名身份。

一个“个人卖家”账号也不自动证明卖方只是偶尔处理闲置；可能存在职业倒卖、代卖或商家伪装个人。

### 2.5 contact endpoint

例如：

- BBS 站内信；
- 公开电话；
- QQ；
- 分类站联系按钮；
- App 内消息。

只要交易逃到电话/QQ，archive 对后续状态的观察能力就急剧下降。

### 2.6 inquiry / message

“还在吗？”只是 inquiry state，不是购买承诺。

私聊中可能继续确认：

- 瑕疵；
- 型号；
- 发票；
- 原价；
- 最低价；
- 自提地点；
- 运费；
- 是否先到先得。

### 2.7 negotiation

asking price 可以在私聊或面交时改变。

所以：

> **archive 中的标价不是历史成交价。**

### 2.8 agreement

双方可能已经口头/文字约定，却仍可发生：

- 买方失约；
- 卖方改卖别人；
- 到场后觉得成色不符；
- 运输太贵；
- 临时取消。

### 2.9 payment / escrow

2005–2011 很多同城分类交易可能现金面交或站外转账；2014 后担保支付更容易成为平台内状态。

必须区分：

- 未付款约定；
- 直接转账；
- 现金；
- 支付平台付款；
- escrow held；
- seller funds released；
- refund / dispute。

### 2.10 physical handoff

真正让物品改变占有关系的动作可能是：

- 宿舍门口面交；
- 地铁站见面；
- 上门自提；
- 快递寄送；
- 二手店上门收；
- 同学帮忙搬。

这些往往发生在 Web 之外。

### 2.11 acceptance

买方拿到物品以后仍可能发现：

- 假货；
- 隐瞒瑕疵；
- 配件缺失；
- 无法使用；
- 与照片不一致。

“拿到”与“交易最终接受”也不是同一个状态。

### 2.12 listing closure

listing 可能因为：

- 真正售出；
- 卖方放弃；
- 过期；
- 平台清理；
- 重复发布；
- 违规删除；
- 转到另一平台；
- 修改后重新上架

而关闭。

所以：

`listing disappeared != sold`。

---

## 3. 基本状态机

一个最小可用状态机：

```text
OBJECT_HELD
  ↓
LISTING_DRAFT
  ↓
LISTING_PUBLISHED
  ↓
LISTING_VISIBLE / INDEXED
  ↓
INQUIRY_RECEIVED
  ↓
NEGOTIATING
  ↓
AGREEMENT_REACHED
  ↓
PAYMENT_PENDING / CASH_PLANNED / ESCROW_FUNDED
  ↓
HANDOFF_OR_SHIPMENT
  ↓
BUYER_RECEIVED
  ↓
BUYER_ACCEPTED
  ↓
SELLER_FUNDS_AVAILABLE
  ↓
LISTING_CLOSED
```

但旧 Web 经常只留下：

```text
LISTING_PUBLISHED
```

或最多：

```text
LISTING_PUBLISHED → contact endpoint
```

因此不能从一个 archive listing 推断整个状态机后半段。

### 3.1 中途失败状态

至少还应允许：

```text
NO_INQUIRY
INQUIRY_GHOSTED
NEGOTIATION_FAILED
BUYER_NO_SHOW
SELLER_WITHDREW
OBJECT_ALREADY_SOLD_ELSEWHERE
PAYMENT_FAILED
SHIPMENT_LOST
CONDITION_DISPUTED
REFUND_REQUESTED
PLATFORM_REMOVED
LISTING_EXPIRED
RELISTED
```

这些失败状态对普通生活很重要，因为“能发布”并不等于“能及时把东西变成现金或空间”。

---

## 4. 2005–2009：校园 BBS 与分类信息——Web 先解决“谁可能要”

### 4.1 校园 BBS 的特殊优势：地方性 + 弱关系信任

2008-07-01 广州高校同期报道记录：

- 毕业生大量出售带不走的旧物；
- 受访学生把“在各校 BBS 上发帖子”列为首选渠道；
- 其次才是贴广告、跳蚤市场、内部换物和摆摊；
- 有管理人员观察到网上买家直接到宿舍看货；
- 学生直说“E时代我们都是网上甩卖”。

来源：
- 中国新闻网稿，搜狐保存：https://news.sohu.com/20080701/n257861290.shtml

证据等级：**B（同时代记者采访，含第一人称）**。

这个案例不能证明 2008 年全国高校都一样，但非常适合复原一条真实 state chain：

```text
BBS listing
→ potential buyer reads
→ contact
→ buyer enters campus/dorm area
→ inspect object
→ bargain / pay
→ carry away
```

Web 的作用首先是**把发现和人在物品旁边等待解耦**。

### 4.2 2009 北京高校：板块流量不能直接换算成交率

2009-06-29 的同期报道记录清华、北大、人大等高校 BBS 的二手市场板块在毕业季求购求售活跃，品类包括旧书、自行车和家电。

来源：
- 中国新闻网：https://www.chinanews.com/life/news/2009/06-29/1753544.shtml

证据等级：**B（同时代报道）**。

这可以证明：

- 二手板存在；
- 当时有人使用；
- 毕业季是高峰 life-event；

但不能从“帖子很多”推出：

- 平均成交率；
- 平均成交价；
- 平均多久卖掉；
- 哪类物品真正更容易成交。

### 4.3 大件物品最能揭示 `searchability != portability`

2008–2009 同期材料都提到大件家电更难处理。

这说明旧 Web 只能解决信息的一部分：

> 找到一个想要空调的人，不等于已经解决拆机、楼层、车辆、运输、新宿舍能不能装的问题。

因此二手网页研究不能从“网络扩大买家池”直接写成“搬家成本下降”。现实搬运链仍须另证。

---

## 5. 2005–2011：城市分类信息——从“一个校园”扩到“一个城市”

### 5.1 58/赶集式分类信息首先是 discovery layer

2010 年《互联网周刊》同期报道把：

- 房屋出租；
- 二手物品转让；
- 招聘求职

列为传统报纸分类广告进入互联网分类信息平台的典型对象，并讨论 58 同城、赶集网等在多个城市扩张。

来源：
- C114 转载《互联网周刊》2010-06-21：https://www.c114.com.cn/media/532/a517084.html

证据等级：**B（同期行业媒体）**。

对考古最重要的不是公司规模，而是交互模型：

```text
city/category page
→ listing result
→ listing detail
→ seller contact
→ transaction escapes the site
```

因此必须建立 `contact-channel escape`。

### 5.2 contact-channel escape：联系后，交易从 Web 历史里逃走

分类信息站常把 Web 做到：

- 发布；
- 搜索；
- 城市筛选；
- 物品详情；
- 联系方式。

但之后可能发生在：

- 电话；
- 短信；
- QQ；
- 面交。

这些通道通常不会和公开 listing 一起被 archive 保存。

因此：

> **一个保存完整的 listing 页面，也可能只保存了整笔交易最前面的 10%。**

### 5.3 2010 移动分类信息：listing 开始跟着城市中的身体移动

2010 年赶集客户端同期报道记录移动端具有：

- 浏览；
- 搜索；
- 附近信息；
- 发布；
- 二手分类；
- 点击联系人电话；
- 短信分享。

来源：
- 投资界转腾讯科技：https://m.pedaily.cn/news/185454

证据等级：**B（同期科技媒体）**。

这一步需要与今天 App 的完整交易栈区分。

能证明的是：

> **分类信息已经从桌面查询逐渐变成“人在城市里走动时也能查附近的人和物”。**

不能自动证明：

- 当时已普遍使用 GPS 精确位置；
- 支付已站内完成；
- 所有 listing 都有现代筛选字段。

---

## 6. 2011：论坛、分类站与社区二手并存

2011 年《羊城晚报》同期报道的“小茜”会在论坛、58、赶集、社区跳蚤等多个渠道买卖家庭闲置，涉及婴儿车、豆浆机、风扇等。

来源：
- 新浪转载《羊城晚报》：https://news.sina.com.cn/o/2011-08-27/144923061171.shtml

证据等级：**B（同期媒体，含个人经验）**。

这一材料对旧网 archaeology 有两个意义：

1. **跨平台重复 listing 很可能存在。** 同一物体可在论坛和分类站同时发布。
2. “某站 listing 消失”不等于物品已经成交；卖方可能只是把主战场移到另一渠道。

因此新增：

### 6.1 cross-platform duplicate listing gap

同一物品可能存在多个 URL：

```text
forum A post
58 listing
Ganji listing
QQ group message
```

archive 如果只保存一个 URL，会误把它当作独立交易对象。

识别同一物品需要谨慎使用：

- 相同图片；
- 相同描述；
- 相同电话/QQ（隐私敏感，不应公开重聚合）；
- 相同型号与瑕疵；
- 时间和地点。

研究中不应为了“去重”而重新暴露个人联系方式。

---

## 7. 2012–2014：购买记录、支付与 escrow 进入二手状态机

### 7.1 2013 一键转卖：购买记录成为新 listing 的 provenance

2013 年浙江在线同期报道称淘宝二手提供“一键转卖”已购商品。

来源：
- 浙江在线 2013-08-30：https://biz.zjol.com.cn/system/2013/08/30/019566388.shtml

证据等级：**B（同期媒体；平台规模数字仅作企业口径）**。

这一功能改变了 listing provenance：

过去：

```text
seller manually describes object
```

现在可以是：

```text
historical purchase record
→ prefilled product identity / metadata
→ seller adds current used condition
→ secondhand listing
```

所以考古时要区分：

- 原商品 catalog metadata；
- 卖方当前物品 condition；
- 买入时间/价格（若公开）；
- 二手 asking price。

`catalog identity != current object condition`。

### 7.2 2014 闲鱼：从信息平台向 transaction state machine 延伸

2014-07-20 央广网同期报道记录：

- 淘宝账号可以登录；
- 普通个人无需开店即可发布闲置；
- 支付宝可进入交易；
- 买家收货满意后再确认付款；
- 平台负责人把这种个人闲置发布与传统开网店区分；
- 报道同时把 58/赶集描述为更偏信息发布、用户常在线下继续沟通。

来源：
- 央广网：https://finance.cnr.cn/gs/201407/t20140720_515982995.shtml

证据等级：**B（同期报道 + 平台负责人原话）**。

这里可以正式把状态扩展为：

```text
listing
→ contact/message
→ order/agreement
→ payment enters escrow-like state
→ shipment / handoff
→ buyer confirms
→ seller receives funds
```

即使如此，仍不能把“平台支持这种流程”写成“每一笔交易都经过完整流程”；面交、取消、站外沟通仍可能存在。

---

## 8. 关键 state gaps

### 8.1 listing-draft / published gap

卖方写完并点击发布，可能因为：

- 审核；
- 分类错误；
- 账号限制；
- 内容违规；
- 网络失败

而没有真正进入公开列表。

### 8.2 published / indexed gap

详情 URL 可访问，不等于它已经进入：

- 类目列表；
- 搜索索引；
- 推荐；
- 同城筛选。

### 8.3 listing-staleness gap

页面仍显示“在售”，物品可能已经：

- 卖给线下买家；
- 卖到另一个平台；
- 被送人；
- 损坏；
- 卖方忘记删除。

因此 historical listing timestamp 不能当 authoritative availability timestamp。

### 8.4 asking-price / transaction-price gap

网页保存的是标价。

真正成交价可能在：

- 电话议价；
- QQ 聊天；
- 面交；
- 组合购买；
- 包邮谈判

中改变。

所以不要从 archive listing 直接构建“真实二手成交价格指数”，除非另有 transaction evidence。

### 8.5 condition-description / object-state gap

“九成新”“全新未拆”“自用”“无维修”等均是 seller claim。

2018 同时代材料中已经有页面称“全新未拆”，实物却被拆开且一件验出假货的案例。

因此：

`condition text != inspected condition`。

### 8.6 seller-location / object-location gap

页面上的城市/地区可能是：

- seller 注册地；
- 发布选择地；
- 物品所在地；
- 预期交易地。

这些不必相同。

### 8.7 contact-channel escape

一旦用户点击电话/抄走 QQ，后续：

- 谁联系谁；
- 谁先答应；
- 价格；
- 见面；
- 是否成交

都可能从 Web 档案中消失。

### 8.8 negotiation invisibility

即使平台存在站内消息，消息通常需要登录且涉及私人通信，public archive 不应该也往往不能保存。

这意味着研究者最缺的恰恰是决定交易是否成立的那段对话。

### 8.9 agreement / payment gap

双方说“要了”不等于已付款。

### 8.10 payment / handoff gap

钱已转出，物品可能尚未交付；面交反过来也可能先拿货再给现金。

### 8.11 escrow / seller-funds gap

担保支付中：

`buyer paid != seller has spendable funds`。

中间还存在收货、确认、争议、退款。

### 8.12 shipment / possession gap

快递已发出，不等于买方已经拿到。

配套 parcel tracking 状态请参照本仓现有包裹追踪专题，不在此重复。

### 8.13 possession / acceptance gap

买方已经签收仍可能因为瑕疵/假货发起争议。

### 8.14 listing-closure gap

“下架/删除/已结束”并不告诉研究者：

- 成交；
- 放弃；
- 违规；
- 过期；
- 迁移；
- 重发

中的哪一种发生。

### 8.15 relist / revision collapse

卖方可能反复：

- 降价；
- 改标题；
- 换照片；
- 重发；
- 删除旧帖。

archive 只保留一个时点时，会把多轮失败出售压成一次静态 listing。

### 8.16 moderation / deletion invisibility

诈骗、违禁商品、假货 listing 可能正因为平台治理而快速消失。

因此 archive 中“没看到很多违规二手”不能证明当时没有。

### 8.17 photo-host / thumbnail gap

旧论坛和分类站常把图片放在：

- 外链图床；
- 动态缩略图；
- CDN；
- 登录后资源。

主 HTML 幸存不等于物品图像幸存。

### 8.18 seller identity / merchant status gap

账号显示“个人”不等于经济角色一定是普通家庭闲置卖家。

尤其到后期，职业倒卖、二手商、代卖可能使用相似界面。

### 8.19 cross-platform duplicate gap

同一物体可能在多个平台同时存在。

### 8.20 search-result temporal drift

今天打开一个仍存活的旧 listing URL 或搜索入口，如果它调用的是今天的索引/推荐后端，只能算：

> **current-backend rehydration**

不能当成 2010 年用户当时看到的搜索结果。

---

## 9. Archive 为什么特别容易误判二手交易

二手 listing 是一种典型的**短命事务对象**：

- 它的目标本来就是一旦成交就不再需要；
- 卖方可能主动删除；
- 平台可能让过期信息沉底；
- 搜索索引不断更新；
- 电话/QQ/私信是主要后续通道；
- 图片和动态字段比静态文字更易丢。

因此存在一个总的保存偏差：

> **listing survival / transaction disappearance：想卖的声明比卖成的事实更容易幸存。**

### 9.1 sold-out hindsight bias

如果 archive 恰好只抓到最终“已售/下架”页，会抹掉此前：

- 多久无人问；
- 降过几次价；
- 有多少人爽约；
- 卖方是否急着搬家。

### 9.2 unsold-survivor bias

反过来，长期没卖掉的 listing 因为活得更久，可能比很快成交、迅速删除的信息更容易被 crawl 捕获。

这意味着 archive 样本甚至可能**系统性高估难卖的物品**。

这是本轮很重要的新 archive-bias 假设，未来应做抽样验证，不能直接当已证明统计规律。

---

## 10. 浏览器、页面与技术环境

研究 2005–2015 二手 Web 时至少记录：

- charset：GB2312 / GBK / UTF-8；
- 表格布局、frames、旧式分页；
- 城市子域与 category URL；
- 发布表单是否 POST；
- 登录 cookie/session；
- 图片上传与缩略图路径；
- 外链图床；
- JS/AJAX；
- 动态电话号码展示；
- 搜索/排序参数；
- 页面是否手机 WAP/HTML5/App 落地页；
- 是否调用地图/定位；
- 支付是否跳转支付宝等外部域；
- archive rewrite 是否破坏 form action / JS / image URL。

### 10.1 当前 58 字段不能倒写回 2008

今天的 58 二手频道仍可看到城市、分类、成色等丰富筛选，但这只能证明**当前页面状态**。

不得用今天的字段集合推断 2008–2010 的历史 schema。

历史字段必须由：

- verified capture；
- 同期截图；
- 同期教程；
- 官方帮助/产品文档

逐项确认。

---

## 11. Historical replay 本轮结果

### 11.1 尝试对象

本轮尝试构造并访问约：

- 2009 年 `bj.58.com/sale/`；
- 2011 年 `www.58.com/sale/`

的 Wayback replay。

### 11.2 当前结果

当前访问链对未经搜索结果/已打开来源建立 provenance 的构造 archive URL 返回安全限制，未取得可实际检查的 memento。

因此本轮只能记录：

> **M1 verified 2009–2011 58.com secondhand historical capture: NOT ACHIEVED IN THIS SLICE.**

这不等于：

> “Wayback 没保存 58 二手页面。”

也不等于：

> “2009 年页面不存在。”

同期媒体已经独立证明当时分类信息平台与二手业务存在；只是本轮没有拿到满足仓库 METHOD 的 archive capture。

### 11.3 下一次 replay 应记录

若未来成功取得 memento，至少记录：

- archive source；
- original URL；
- capture URL；
- capture datetime；
- accessed_at；
- HTTP/replay status；
- charset/Content-Type；
- 页面是否是分类首页、搜索页、listing 详情或错误页；
- 城市；
- 类目；
- listing metadata；
- 图片是否保存；
- 联系方式是否静态/脚本生成；
- JS/AJAX 子资源；
- form action；
- login requirement；
- archive rewrite effects。

---

## 12. Preservation levels

为避免“保存了一张网页”被误写成“复原了二手交易”，建议使用以下层级：

### S0 — platform identity

只确认品牌、域名、活跃期。

### S1 — board/category shell

确认二手类目/板块存在以及导航形态。

### S2 — listing shell

确认历史 listing 详情页的布局与主要字段。

### S3 — listing + item metadata

确认某一历史时点的标题、asking price、condition claim、location、photo availability 等。

仍然不证明物体真实状态。

### S4 — contact/interaction UI

确认历史页面怎样让用户：

- 打电话；
- 发站内信；
- QQ；
- 留言；
- 下单。

仍然不获得真实私人通信。

### S5 — historically documented workflow

由同期帮助、教程、报道等确认：

`listing → contact → negotiate → pay/handoff`

的操作结构。

### S6 — synthetic representative transaction reconstruction

用虚构账户/物品重建状态机，用于展示交互逻辑；必须显式标 `reconstruction`。

### S7 — verified historical backend/artifact replay

只有实际得到历史后端响应、WARC/WACZ 或可验证事务 artifact 时才能进入。

### S8 — real private transaction history

包括普通人的私聊、电话、真实支付、地址、物流、身份证明。

**不作为本仓追求的 preservation 目标。**

它涉及隐私，而且研究平台结构并不需要重新公开普通人的私人交易。

---

## 13. 隐私与伦理边界

二手旧网页特别容易保存：

- 手机号；
- QQ；
- 宿舍楼；
- 小区；
- 家庭内部照片；
- 物品序列号；
- 学生身份线索。

即使 archive 仍公开，仓库也不应机械重新聚合。

### 13.1 最小化原则

研究时优先保存：

- URL pattern；
- 字段结构；
- 类目；
- 匿名化价格/物品类型；
- contact mechanism；
- archive metadata；
- state transition。

不需要复刻普通人的真实联系电话和住址。

### 13.2 照片尤其敏感

旧物照片可能无意中包含：

- 宿舍环境；
- 家中布局；
- 证件；
- 快递单；
- 人脸；
- 儿童；
- 序列号。

研究“照片字段存在”通常不要求重新分发原图。

---

## 14. 证据表

| Claim | Evidence | Grade | Confidence | Limits |
|---|---|---:|---:|---|
| 2008 广州高校毕业生优先用 BBS 甩卖带不走物品 | 中国新闻网同期采访（搜狐保存） | B | high | 个案/校园样本，不能外推全国 |
| 2009 北京高校 BBS 二手板毕业季活跃 | 中国新闻网 | B | high | 不能推出成交率 |
| 2010 分类信息网站承接二手转让等小广告功能 | 《互联网周刊》同期行业报道 | B | medium-high | 公司规模数字不可当人口采用率 |
| 2010 赶集移动端可浏览/搜索/附近/发布/点击电话 | 同期科技媒体 | B | high | 不等于 full mobile transaction |
| 2011 用户跨论坛、58、赶集等处理闲置 | 《羊城晚报》同期人物报道 | B | medium-high | 单个人物不代表总体 |
| 2013 淘宝二手存在一键转卖 | 浙江在线同期报道 | B | high | 平台规模数据按企业口径 |
| 2014 闲鱼允许个人发布、支付宝进入交易链 | 央广网同期报道 | B | high | 支持流程 != 每笔都完成全链 |
| 1998 旧货市场已有信息/评估/结算/运输等功能 | 《旧货流通管理办法（试行）》 | A | high | 只作前史边界，不扩仓库 scope |
| 2009–2011 58 二手历史 DOM/字段 | 本轮未取得 verified memento | — | unknown | 不得用现代页面倒写 |

---

## 15. “已证实 / 高概率 / 不知道”

### 已证实

- 2008–2009 校园 BBS 已是高校毕业生二手信息的重要线上入口之一。
- 2010 年分类信息平台已经明确经营二手物品转让，并开始进入移动端。
- 2011 年普通用户可以在论坛、分类站等多个渠道之间处理闲置。
- 2013–2014 二手交易开始与既有购买记录、支付宝/担保式支付更紧地连接。
- 线上 listing 与现实成交必须拆成不同 state。

### 高概率但需更多 artifact

- 2008–2011 58/赶集的历史 listing 字段、城市 URL、联系按钮在不同年份发生过显著 schema 变化。
- 同一物品跨多个平台重复发布并不少见。
- 很快成交后删除的 listing 可能比长期卖不掉的 listing 更难进入 archive，从而造成 survivor bias。

### 不知道

- 2008–2011 典型二手 listing 的平均成交率。
- 标价与成交价的平均差距。
- 平均多久出售。
- 校园 BBS 到电话/面交的真实转化率。
- 当前 archive 样本对“难卖物品”的偏高程度。
- 2009–2011 58 具体历史页面字段与浏览器行为，本轮未完成 M1 capture。

---

## 16. 后见之明风险

### 16.1 把闲鱼状态机倒写进 BBS

2008 BBS 帖没有今天统一的：

- 担保支付；
- 推荐；
- 物流；
- 平台信用；
- 争议处理。

它更接近：

`public notice → private contact → local handoff`。

### 16.2 把现代 58 字段倒写回 2010

今天的“成色/区域/推荐/认证”等 UI 不能证明历史页面也一样。

### 16.3 把 listing 当成交数据库

这是本专题最大的错误源。

### 16.4 把平台账号当现实权属

卖方可能代卖、转卖、职业倒货；买方支付也不自动证明合法取得所有附着权利。

### 16.5 把平台关闭页面当作物品生命周期终点

页面消失可能与物品无关。

### 16.6 把今天的“回血/断舍离/循环消费”语言投射到 2008

2008 的同期材料更直接的是毕业倒计时、带不走、宿舍清空和省时间；今天的消费价值观必须用今天的一手材料另证。

---

## 17. 对中文旧网考古方法的新贡献

本专题增加了几种可以复用于其他 transaction-heavy 对象的缺口：

1. **listing survival / transaction disappearance**：公开意图比完成事实更易保存。
2. **contact-channel escape**：一旦电话/QQ接管，Web evidence chain 断裂。
3. **asking-price / transaction-price gap**：公开报价不等于结算值。
4. **condition-description / object-state gap**：文本声明不等于现实物体。
5. **listing-staleness gap**：页面在 ≠ 物品还在卖。
6. **relist/revision collapse**：一次静态 capture 可能压掉多次失败出售。
7. **cross-platform duplicate gap**：多个 URL 可能只对应一个现实物体。
8. **unsold-survivor bias**：卖得慢的页面可能因为活得久而更易被档案抓到；目前是待验证假设。

其中最后一点尤其值得进入以后 M4 archive-gap 抽样：

> **旧网档案保存概率可能与事务是否迅速完成有关。**

如果成立，archive 不是随机抽样，而会系统性偏向“没有很快完成使命的页面”。

---

## 18. 对 `how-people-lived` 的交叉链接

配套生活史研究已经把二手市场解释为：

- `possession exit liquidity`；
- `material reversibility`；
- `temporary-life material stack`；
- `resale horizon`；
- `exit-price feedback`。

旧网仓不承担这些跨 1979–2026 的宏观生活结论。

它只负责提供更严格的技术/证据边界：

> **一个人“可以把物品挂到网上”，究竟在历史页面层面能证明到哪一步。**

两仓的连接点是：

`life transition needs material exit`

与

`old Web creates a partially observable listing/transaction state machine`。

---

## 19. 下一步可复核实验

以后如果 archive 访问条件允许，可以选取一个明确城市、明确日期窗口做小样本：

1. 抽取某历史二手类目的连续 listing；
2. 记录 capture 间隔；
3. 检查 listing 是否持续/删除/降价/重发；
4. 对图片、联系电话显示方式、城市字段、成色字段做 schema 编目；
5. 不重新公开个人联系方式；
6. 比较“短命 listing”和“长寿 listing”的 archive 捕获率；
7. 如果有同期帮助页，复原发布表单与关闭流程；
8. 用 synthetic item 做 reconstruction，不伪装真实历史交易。

若能完成，可以第一次实证检验 `unsold-survivor bias`。

---

## 20. 本轮饱和判断

本轮出现了新的 old-Web 状态机制与历史可见性偏差：

- `listing-staleness gap`；
- `contact-channel escape`；
- `asking-price / transaction-price gap`；
- `condition-description / object-state gap`；
- `listing-closure gap`；
- `relist/revision collapse`；
- `cross-platform duplicate gap`；
- `unsold-survivor bias`。

同时与 `how-people-lived` 新增的 `material reversibility / possession exit liquidity` 形成直接交叉。

因此本阶段连续“无实质新增”仍为 **0/3**，不触发 closure。