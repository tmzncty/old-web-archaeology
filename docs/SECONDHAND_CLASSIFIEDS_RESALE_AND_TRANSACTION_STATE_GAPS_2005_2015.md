# Secondhand classifieds / resale / transaction state gaps, 2005–2015

## Scope

本文严格留在本仓约 1995–2015 中文 Web 的研究边界内。它不是中国旧货业史，也不把 1980s 信托商店、流动收购、2015 年后的移动二手平台、2020s 青年消费文化扩进本仓；这些更长的普通生活史放在 companion note：

- `tmzncty/how-people-lived/topics/secondhand-circulation-possession-liquidity-and-household-reversibility-china-1987-2026.zh-CN.md`

这里问一个更窄的旧网问题：

> 当 2005–2015 中文 Web 上出现“出售二手显示器”“毕业甩卖”“闲置转让”这样的页面时，我们到底能够从一个历史页面证明到哪一步？页面上的“出售”状态，与真实物品是否仍存在、卖家是否可联系、双方是否见面、是否付款、是否交付、后来有没有纠纷之间隔着多少层？

沿用 `docs/METHOD.md`：

`platform ≠ site/host ≠ account ≠ page/URL ≠ capture ≠ claim`

本题再增加：

`listing state ≠ transaction state ≠ object state ≠ household outcome`。

---

## 1. 为什么二手分类页是一个典型的“时态页面”

二手 listing 和宠物领养、招聘、租房一样，不是普通静态文章。它表达的往往是一个**短期现实状态**：

- 物品还在不在；
- 价格有没有变；
- 卖家是否仍想出售；
- 是否已经有人预订；
- 是否已经成交；
- 交易是不是取消；
- 物品有没有损坏；
- 卖家是不是已经毕业/搬家/换城市；
- 页面是否忘记关闭。

因此一个 2007 年标题写“出售显示器”的页面今天仍在线，只能可靠证明：

> 在能够确认的历史时点，有人/媒体/平台留下了这样一条出售表达。

它不能自动证明：

> 该物品在 capture 以后仍可买，或最终一定成交。

必须分别记录：

- `listing_state_at_page_time`
- `object_state_at_page_time`
- `contact_state`
- `transaction_state`
- `listing_state_afterward`
- `real_world_outcome`

不知道时就写 `unknown`。

---

## 2. 2005：赶集的“线上二手货、线下就近交易”把旧网与现实交付的边界说得非常清楚

2005-06-02，《新京报》经新浪科技保存的一篇同期报道介绍赶集网，标题直接写作“线上二手货线下就近交易”。报道把它定位成按城市组织的本地分类信息服务，普通人可以在网上免费发布，再就近完成现实交易。

来源，B 级同期媒体：
<https://tech.sina.com.cn/i/2005-06-02/0941624627.shtml>

这是一个很好的最低状态模型：

```text
seller has object
→ listing authored
→ platform accepts/publishes
→ listing indexed in city/category
→ viewer encounters
→ viewer contacts seller
→ parties negotiate
→ place/time arranged
→ physical meeting
→ inspection
→ payment
→ handoff
→ listing closed OR left stale
```

因此：

`listing published ≠ contact happened`

`contact happened ≠ meeting happened`

`meeting happened ≠ buyer accepted object`

`price displayed ≠ realized price`

`listing disappears ≠ successful sale`

最后一条尤其重要：页面消失也可能来自过期、用户删除、平台清理、账号失效或站点迁移。

### 2.1 local-radius gap

赶集早期叙述非常强调“就近”。这说明 Internet 当时首先扩大的未必是全国物流交易，而是**同一城市里陌生人的发现半径**。

一个 listing 的真实可执行性仍取决于：

- 城市是否相同；
- 距离；
- 公交/地铁；
- 大件能否搬运；
- 双方是否有共同空闲时间；
- 是否愿意见陌生人。

所以 `same city website ≠ locally executable transaction`。

---

## 3. 2005–2006：分类信息的结构化，不等于交易已经平台化

### 3.1 58.com：发布、分类、搜索和用户评价进入页面层

2005 年底的同期报道说，58 同城把分类信息发布流程简化，并加入结构化分类搜索；用户评价可以影响信息排名、暂停和发布者信用。2006 年报道又记录 58 于 2005 年 7 月上线，主要提供二手商品、招聘、交友等用户发布的分类信息。

来源：

- 赛迪网经新浪科技，2005-12-20，B：<https://tech.sina.com.cn/roll/2005-12-20/1121797097.shtml>
- 新浪科技，2006-02-12，B：<https://tech.sina.com.cn/i/2006-02-12/1519838495.shtml>

从 old-Web 角度看，变化至少包括：

```text
free-text notice
→ category
→ city/subsite
→ structured fields
→ search/filter
→ user feedback/ranking
→ account reputation
```

但这些都仍主要属于 **discovery / screening layer**。

报道能证明平台当时公开宣称或提供这些界面机制，不能证明：

- 每条信息都经过真实身份验证；
- 差评机制一定能识别诈骗；
- 所有已售物品都会及时下架；
- 页面点击、回复或好评对应真实线下成交。

### 3.2 263：旧“跳蚤市场”被重新组织成 Web2.0 分类信息

2006-05-15 前后，263 把 `www.263.com` / `www.263.net` 的主业务转向分类信息，公开类别包括房产、招聘、宠物和跳蚤市场。同期访谈里，经营者说改版前北京、上海跳蚤市场每天约有一两千条有效发帖，分类信息改版后发布量上升；同时强调分类信息有很强地域性。

来源：

- 新浪科技，2006-05-15，B / 平台公开状态：<https://tech.sina.com.cn/i/2006-05-15/1001937045.shtml>
- 新浪科技访谈，2006-05-24，B，经营者同时性陈述：<https://tech.sina.com.cn/i/2006-05-24/1438953632.shtml>

这里必须保留一个 **posting-volume / transaction-volume gap**：

`daily posts ↑ ≠ successful trades ↑ by the same amount`。

发帖量只能说明信息供给和发布行为，不能直接当成交量。

---

## 4. 历史 locator：中文门户分类信息不应从记忆里补 URL

本轮取得几个可以继续做 archive 定位的同时代 locator：

- `www.58.com`
- `www.ganji.com`
- `www.263.com`
- `www.263.net`
- `classadnew.sina.com.cn`

其中 `classadnew.sina.com.cn` 不只是后来 SEO 列表中的域名。新浪 2006 年一篇站内新闻已经直接链接到该 host 的城市分类信息页；2005 年新浪技术页的导航也存在“生活资讯/分类信息”指向该 host 的痕迹。

同期 locator 示例：
<https://news.sina.com.cn/s/2006-04-03/09418600514s.shtml>

注意：**locator 不是 capture。** 本轮没有因为这些 URL 还出现在旧新闻或搜索结果里，就声称已经恢复 2005/2006 的原始分类页。

---

## 5. 2007：媒体留下“卖家即将毕业、买家刚参加工作”的现实 outcome，但不能倒推出原 listing 页面

2007-01-01 的同期报道记录：一名刚毕业工作的刘先生，在某网站跳蚤市场从一名即将毕业离校的大学生手里买到 15 英寸液晶显示器和品牌 MP3，价格约为新品一半。

来源：齐鲁晚报经新浪，B：
<https://news.sina.com.cn/c/2007-01-01/032710905959s.shtml>

这条材料很有价值，因为它至少跨过了：

```text
online listing/discovery
→ buyer found item
→ seller identified as graduating student
→ transaction reported as completed
→ buyer reports use-value/price benefit
```

但 old-Web 侧仍必须克制：

- 报道没有给出原 listing URL；
- 不知道具体平台页面结构；
- 不知道双方用站内消息、QQ 还是电话联系；
- 不知道是否当面验货；
- 不知道 listing 成交后是否被标记为“已售”；
- 不知道页面是否被 archive 保存。

因此这是 **real-world outcome evidence without original transaction page**，不是完整页面考古案例。

---

## 6. 2009：同一篇同时代报道给出了极少见的 listing→offline funnel

《中国青年报》2009-03-31 报道中，北京职员文小娟发现 40 多件闲置衣物。朋友帮她在网站“个人闲置”区发帖，附照片和每件 10–20 元标价；一天内卖掉 8 件，买家都上门自取、当面交易。

来源，B，含同时性自述：
<https://zqb.cyol.com/content/2009-03/31/content_2603231.htm>

这个案例至少能观察到：

```text
idle goods identified
→ listing + image + price
→ viewers encounter
→ some contact
→ physical pickup
→ face-to-face payment/handoff
→ eight items leave household
```

但即使这样仍有未知状态：

- 有多少人浏览；
- 有多少人询价后放弃；
- 标价是否等于成交价；
- 是否一次卖给多人；
- 页面何时关闭；
- 未售物品后来怎样处理。

这说明，**即使媒体已经报道“卖成功了”，页面层和现实层仍然不能完全合并。**

同一报道的腾讯网调查又说，76.5% 受访者想卖闲置却不知道怎么卖。该调查是在线样本，不能外推全国；但对 old-Web 方法很重要：

`platform exists ≠ potential seller knows route ≠ seller can successfully author/manage listing`。

---

## 7. C2C 支付把交易半径扩大，但分类信息页和平台交易页不能混成一种东西

2005 年同期报道把支付宝描述为买家付款后由平台暂存、待买家确认收货再转给卖家的信用中介。

来源：人民网-江南时报经新浪财经，2005-02-03，B：
<https://finance.sina.com.cn/roll/20050203/04301343972.shtml>

对 old-Web 考古，这意味着至少要区分两种 transaction architecture：

### A. Classified-local

```text
listing page
→ phone/QQ/message
→ meet
→ inspect
→ cash/other payment
→ handoff
```

### B. Platform-mediated C2C

```text
item page
→ account/order
→ platform payment/escrow
→ shipping
→ delivery
→ buyer confirmation/dispute
→ seller receives funds
```

历史叙述不能因为二者都叫“网上二手交易”，就把 2005 赶集式同城信息发布和淘宝式订单/支付 transaction 当成一个技术对象。

这也是以后做 M1 case 时必须先确定的 **transaction-family boundary**。

---

## 8. 2010–2015：listing 生命周期开始越来越依赖账号、移动端和平台内部状态，但历史 archive 更难看到真实成交

本轮没有试图把 2010–2015 的每个二手平台都做一遍平台史。这里先保留一个方法判断：随着 C2C、移动端和账号信用越来越深地集成，现实 transaction 的关键状态更可能位于：

- 登录后的聊天；
- 订单页；
- 支付状态；
- 物流单号；
- 确认收货；
- 退款/争议；
- 账号信用；
- 手机通知。

这些恰好也是公共 Web archive 最难保存、最不应重新公开的状态。

因此二手交易是典型的：

**public listing shell / private transaction state asymmetry**。

公开 archive 可能留下一个商品标题、一张图片和一个标价，却看不见决定结果的绝大部分链条。

---

## 9. 新增 state gaps

### 9.1 listing-status staleness gap

`page online ≠ item still available`。

历史搜索引擎或 archive 仍能显示“出售”“求购”，但现实状态可能早已结束。

### 9.2 ask-price / realized-price gap

`displayed price ≠ final agreed price`。

线下砍价、私聊改价、打包价、运费都可能改变最终金额。

### 9.3 contact-channel gap

`contact button/phone field visible ≠ parties actually communicated through that channel`。

很多旧分类页会很快把协商转移到电话、短信、QQ 或当面交流。

### 9.4 inspection gap

`description/photo ≠ physical condition`。

二手物品的成色、剩余寿命、隐藏故障往往只有见面或收货后才暴露。

### 9.5 logistics executability gap

`buyer wants item ≠ item can be moved`。

家具、家电、自行车需要额外车辆、搬运、上楼和时间；低价大件尤其可能因物流成本而失去交易意义。

### 9.6 payment-state gap

`buyer says paid ≠ platform accepted funds ≠ seller received withdrawable money`。

不同年代、不同平台的现金、银行汇款、第三方支付和站内订单必须分开建模。

### 9.7 transaction-closure gap

`listing removed ≠ sold`，同时 `listing remains ≠ unsold`。

删除可能是成交，也可能是用户放弃、过期、平台审核、账号死亡；页面一直存在也可能只是卖家忘记更新。

### 9.8 household-outcome gap

`completed transaction ≠ durable life benefit`。

买家可能很快发现故障；卖家可能成交后因运费、退货、纠纷反而损失更多。技术考古若只恢复“成交页面”仍未恢复普通生活结果。

---

## 10. 保存偏差

### 10.1 public-listing / private-negotiation asymmetry

容易保存：

- 分类栏目；
- 标题；
- 价格；
- 城市；
- 描述；
- 部分图片；
- 浏览/回复数。

难以保存：

- 电话；
- 短信；
- QQ 私聊；
- 见面；
- 现场砍价；
- 现金；
- 验货；
- 搬运；
- 后续维修；
- 退货。

因此 archive 天然会高估“页面能说明的东西”。

### 10.2 successful-listing bias

媒体更容易报道“学生网上半价淘到显示器”“一天卖掉八件衣服”，失败 listing、无人问津、临时爽约、低价不愿卖、搬不走等更难留下。

以后必须主动寻找：

- 挂很久卖不掉；
- 询价后消失；
- 交易取消；
- 货不对板；
- 退款失败；
- 运费高于物品价值。

### 10.3 image survival bias

二手商品的判断高度依赖照片。如果 archive 只留下 HTML、图片丢失：

`page readable ≠ condition-inspection affordance survived`。

### 10.4 stale-contact privacy debt

2000s 分类页可能长期暴露普通人的手机、QQ、邮箱、姓名或住址片段。即使原页今天仍公开，本仓也不应把这些字段重新复制进研究文件。

**historical availability ≠ research necessity**。

---

## 11. 与平台消失的关系

二手 listing 特别能提醒 M2/M4：旧网死亡不只意味着“文章少了一页”，还意味着很多现实 transaction 的索引消失。

平台关闭或改版后，可能丢失：

- 用户历史 listing；
- 售出/下架标记；
- 信用评价；
- 城市分类树；
- 图片；
- 站内消息；
- 收藏；
- 价格变化；
- 订单/支付跳转信息。

因此今天只剩门户新闻报道时，我们很容易知道“某平台声称每天有几千条信息”，却不知道一条真实普通用户 listing 当时到底长什么样、经过了哪些状态。

这可以称为 **transactional-darkness after platform death / 平台死亡后的交易黑区**。

---

## 12. M1 状态：本轮明确保持 negative

本轮已经取得并核对的主要 original-resource locator / platform-family 包括：

- `www.ganji.com`
- `www.58.com`
- `www.263.com`
- `www.263.net`
- `classadnew.sina.com.cn`

并取得 2005–2009 的多组同时代 B 级来源，能支持：

- 分类信息平台存在；
- 二手/跳蚤市场是明确类别；
- 城市/地域分类；
- 信息发布与搜索；
- 用户评价等公开机制；
- 至少若干线上发现、线下成交的普通用户案例。

但是，**本轮没有实际打开并验证一份满足本仓 M1 门槛的 2005–2010 中文二手分类信息 Wayback/WARC transaction capture。**

因此以下内容全部继续是 `unknown` 或未验证：

- 2005/2006 原始 listing DOM；
- HTTP charset / Content-Type；
- 发帖 form action；
- 城市/category query 参数；
- cookie/session；
- 登录与匿名发布边界；
- 图片上传与子资源 capture；
- QQ/电话字段是否经过 JS/登录保护；
- 已售/关闭状态怎样编码；
- 搜索结果排序真实行为；
- 评论/私信 endpoint；
- 支付或物流 handoff；
- 一条 listing 的完整 create→contact→close transaction。

这不是说 Internet Archive 一定没有相应 capture，而是：**本轮没有取得并实际检查它，所以不能升级证据等级。**

---

## 13. 下一步最值钱的 M1 任务

如果下一轮专门推进这一题，优先级应是：

1. 从 2005/2006 同期报道中抽取精确栏目/页面 URL，而不只用 host；
2. 对 `58.com`、`ganji.com`、`263.com`、`classadnew.sina.com.cn` 查 CDX / Wayback 时间点；
3. 实际打开一个 listing/category memento；
4. 记录 original URL、capture datetime、HTTP/回放状态、charset、主 HTML 与图片子资源；
5. 找至少两个时点，比较分类树、城市字段、联系字段、发布/关闭机制；
6. 若表单只能回放壳层，明确写 `UI survived / transaction backend unknown`；
7. 不尝试联系历史卖家，不重新传播旧手机号、QQ、邮箱或地址。

一个好的完整 case 不需要证明“全国人都怎样买二手”，只需要把一条历史 listing 的**页面状态和它不能证明的现实状态**界定清楚。

---

## 14. 对 ordinary-life companion 的贡献

从技术史角度，本轮最重要的结论是：中文旧 Web 把原来依赖信托商店、旧货市场、纸质广告和熟人的旧物，逐渐变成了**个人可发布、按城市和类别检索的网络对象**；随后账号信用、支付和物流又把更多 transaction 状态装进平台。

但 archive 的可见性恰恰朝相反方向发展：

**越接近真实交易结果的状态，往往越私人、越动态、越依赖账号和后端，也越难被公共档案保存。**

所以研究“Internet 是否让普通人的物品更容易退出家庭”时，不能用页面数量或 listing 数量作答案。真正的生活变化发生在最后几步：有人联系、有人验货、有人付款、有人搬走那张桌子，而卖家终于能关门离开原来的房间。
