# ONLINE_FOOD_ORDERING_MENUS_SERVICE_AREAS_AND_DELIVERY_OUTCOME_GAPS_2004_2010.md

> 状态：研究笔记 / evidence contract extension  
> 主体范围：**2004–2010 中文 Web 上的网上订餐、外卖菜单、服务区域查询、购物车 / 表单、即时通信订餐与线下配送 handoff。**  
> 1993 年电话送餐只作为必要前史边界；2014 年饭统网失联只作为平台消失 / archive lifecycle 的后端观察，不把本仓改成全球餐饮互联网史。

---

## 0. 为什么这是旧网考古问题，而不是餐饮史

网上订餐很适合检验本仓的方法，因为它把一个公共 Web artifact 与一个几乎完全发生在私有 / 线下空间里的执行结果连在一起。

一个旧网页今天可能还留下：

- 餐厅名称；
- 菜单；
- 价格；
- 配送区域；
- 订餐按钮；
- 登录框；
- 购物车；
- 地址输入框；
- “30 分钟送达”承诺。

但用户真正经历的是：

```text
看到页面
→ 判断能不能送到自己这里
→ 选菜
→ 提交订单 / 转电话 / MSN
→ 商家有没有收到
→ 菜有没有货
→ 商家是否接受
→ 厨房制作
→ 配送员出发
→ 找到地址 / 通过门禁
→ 交付
→ 支付
→ 吃到
→ 可能投诉 / 退款 / 再订
```

公共 Web archive 通常只保存左半边。

所以本篇的核心边界是：

> **ordering interface ≠ order execution ≠ delivery outcome**。

---

## 1. 研究单位

按照 `docs/METHOD.md`，不要把下列对象混成一个“订餐网站”：

- **platform / brand**：例如某订餐品牌；
- **host / domain**：具体网站域名；
- **restaurant / merchant record**：平台中的餐馆记录；
- **menu page**：某商家公开菜单；
- **service-area query**：按写字楼、小区、地址或区域返回结果的动态查询；
- **order form / cart**：具体下单入口；
- **IM endpoint**：MSN / QQ 等即时通信订餐账号；
- **order record**：一次私有交易记录；
- **delivery run**：一次真实配送；
- **capture**：某历史时点保存下来的页面表示；
- **claim**：依据证据作出的最小结论。

尤其不能把：

> `brand existed in 2006`

直接写成：

> `the currently reachable domain reproduces the 2006 service`。

---

# 第一部分：前史边界——Web 没有发明送餐

## 2. 1993 电话送餐只作为 boundary condition

2003 年同期采访回顾，丽华快餐创始人蒋建平 1993 年在常州以少量资金起步，早期自己骑摩托送餐，并较早采用“一份起送、随叫随到”等方式。

来源：

- 《创业故事：“丽华”叫板洋快餐》，2003-10-12：<https://news.sina.com.cn/c/2003-10-12/1019903029s.shtml>
- 《送餐业的领跑者：专访丽华快餐董事长蒋建平》，2003-07-25：<https://finance.sina.com.cn/crz/20030725/1534382256.shtml>

### 证据等级

- 2003 企业状态：B；
- 1993 创业细节：十年后当事人口述，经同期媒体交叉，按 C/B 混合使用。

### 本仓只保留的结论

**已证实 / 高概率：**

> 中文 Web 网上订餐出现以前，中国城市里已经存在电话接单 + 人工配送的专业送餐模式。

**不得扩写成：**

- 1993 普通家庭已经普遍叫外卖；
- 当时全国送餐方式都相同；
- Web 只是把电话“换了个皮肤”。

Web 后来的查询、菜单、购物车和可索引商家列表仍是新的技术层。

---

# 第二部分：2004——公开菜单与网页下单进入既有配送链

## 3. 2004 丽华北京网上订餐：目前是 B 级记者页面观察

2004 年 8 月《新京报》报道丽华在北京推出网上订餐。记者说自己查看了订购网站，看到 6–20 元不同档次菜谱，并描述网页订餐与“半个小时内送到”的承诺。

来源：

- 《中外快餐连锁争抢京城市场》，《新京报》，2004-08-05：<https://news.sina.com.cn/o/2004-08-05/09023299815s.shtml>

### 证据等级

**B：同期媒体中的记者页面观察 + 企业陈述。**

### 本轮没有取得的证据

- 可验证的 2004 Wayback / WARC 原始页面；
- 原始 HTML / CSS / JS；
- Content-Type / charset；
- 浏览器要求；
- 表单 action；
- 历史订单后台；
- 当日实际配送时间数据。

所以目前只能写：

> **记者在 2004 年观察到该服务公开展示菜单并提供网页订餐。**

不能写：

> **“已复原 2004 丽华在线订餐网站”。**

---

## 4. 第一组 gap：menu-state gap

一张菜单页面可能同时包含多个时间层：

```text
页面模板时间
商家信息更新时间
菜品更新时间
价格更新时间
库存 / 售罄状态
配送费 / 起送价规则
当前营业状态
```

历史 capture 即使完整，也往往只冻结其中一部分。

因此固定：

> `menu page survived ≠ every item was actually orderable at capture time`

以及：

> `displayed price ≠ executed transaction price`

后者尤其可能受：

- 电话确认；
- 临时涨价；
- 配送费；
- 最低起送；
- 套餐替换；
- 优惠；

影响。

---

# 第三部分：2006——地址 / 楼宇开始成为 Web 查询键

## 5. “3797 想吃就吃”：同期报道保存了操作序列

2006 年《每日经济新闻》报道 3797 时，记者描述的流程是：

```text
访问网站
→ 输入写字楼或小区名称
→ 返回外卖店列表
→ 点击餐馆
→ 浏览带价格菜单
→ 点击加入购物车
→ 输入具体送餐地址
→ 等待配送
```

来源：

- 《网上订餐市场瓶颈渐现》，《每日经济新闻》，2006-08-15：<https://tech.sina.com.cn/i/2006-08-15/09581086122.shtml>

### 证据等级

**B：同期媒体对用户流程的近距离描述。**

平台规模、商家数量等数字大多来自公司，因此需要另标 **vendor claim**，不能因为记者转述就升级为独立统计。

---

## 6. 新研究单位：delivery-zone state

这是普通静态目录没有的关键状态。

用户输入“某写字楼 / 某小区”，系统返回“哪些店可送”。

至少可能涉及：

- 建筑 / 小区规范化名称；
- 商家配送半径；
- 分店归属；
- 营业时间；
- 当时是否暂停配送；
- 最低订单；
- 路线 / 区域规则。

因此一个 archive capture 中的搜索框只能证明：

> **存在一个地点查询接口。**

如果没有同时保存后台索引 / query result，不能证明：

> **某个具体地址在 2006-08-15 真的能看到某家店。**

这叫 **delivery-zone state gap（配送区域状态缺口）**。

---

## 7. query form survival 与 query-state survival 必须拆开

继承仓库已有 search archaeology 规则：

```text
form survived
≠ historical query executed
≠ historical result set survived
≠ user saw those results
```

网上订餐还要再加一层：

```text
result listed restaurant
≠ restaurant accepting orders
≠ item in stock
≠ address executable
```

---

# 第四部分：online listing 并不总是 online transaction

## 8. 2000 年代中期的“网上订餐”可能在电话处结束

同期报道经常把多种形态都称作“网上订餐”：

1. 只提供餐馆 / 菜单信息，用户最后打电话；
2. 网站提交订单，但商家再电话确认；
3. 完整表单 / 购物车下单；
4. 即时通信工具中下单；
5. 平台只做预订 / 导流，不承担配送。

所以以后看到一个旧站点自称 `网上订餐`，必须先问：

> **哪一步真的在线完成？**

不能把 marketing category 当成 transaction topology。

---

## 9. phone-handoff gap

如果网页最终显示一个电话：

```text
用户看页面
→ 拨号
→ 电话里问库存 / 价格
→ 报地址
→ 商家人工登记
```

那么 archive 能证明的只是：

- 页面提供了一个联系入口；
- 可能展示菜单 / 商家信息。

无法证明：

- 电话是否打通；
- 谁接了；
- 菜是否有；
- 最终价格；
- 是否下单。

这类历史缺口应标为 **phone-handoff gap**，而不是用页面内容推定电话后的结果。

---

# 第五部分：2007 MSN 订餐——旧网执行链越过了浏览器

## 10. 丽华“MSN 订餐机器人”

2007 年《北京晚报》记者亲自按要求添加丽华 MSN 账号。报道说，对话框打开后右侧出现菜单，用户可以在即时通信环境里进行订餐；记者同时判断在线订餐尚未被白领普遍接受。

来源：

- 《网络企业争食白领午餐市场 网上订餐画饼难充饥》，《北京晚报》，2007-08-29：<https://www.chinanews.com.cn/cj/xfsh/news/2007/08-29/1013780.shtml>

### 证据等级

**B：同期记者操作体验。**

### 10.1 为什么这不能只按“网页”考古

执行链可能是：

```text
MSN 客户端
→ MSN 账号 / bot
→ 菜单资源
→ 用户输入
→ 丽华内部系统 / 人工
→ 厨房
→ 配送
```

即使订餐网站的 HTML 保存得很好，也完全不能替代：

- 历史 MSN 网络；
- 当时账号；
- bot 服务端；
- 菜单推送；
- 消息协议；
- 用户会话。

这叫 **cross-service execution gap（跨服务执行缺口）**。

---

## 11. 浏览器 / 客户端假设：目前只能写“不知道”

本轮材料没有可靠证明这些早期订餐站点：

- 是否 IE-only；
- 是否依赖 ActiveX；
- 是否特定 GB2312 / GBK；
- 是否要求 JS / cookies；
- 购物车是否 session-based；
- 是否支持 Firefox / Netscape；
- 是否有 Flash 菜单。

因此禁止为了“像 2000 年代网站”而补出这些条件。

当前只可提出待验证问题：

- 页面编码；
- form action；
- cookie / session；
- JS 购物车；
- 动态图片 / 菜单子资源；
- 登录是否必要；
- 地址检索是否 server-rendered。

---

# 第六部分：2008——小型校园网站与物理配送

## 12. “宜客网”：网站很轻，配送很重

2008 年同期报道记录中国人民大学毕业生叶路春和同学继续经营大学期间建立的订餐网站。他们用很低的网站启动资金面向学生和附近写字楼揽单，报道现场看到二百多份盒饭装入保温箱，再绑到三轮车上配送。

来源：

- 《名牌大学毕业生网上揽顾客卖盒饭》，2008-03-04：<https://language.chinadaily.com.cn/campus/2008-03/04/content_6506743.htm>

### 证据等级

**B：同期报道 + 同时性第一人称。**

### 12.1 对技术史的意义

这类案例提醒：

> **low-cost Web presence can sit on top of high-friction physical execution.**

页面或网站可能非常简单，但真实容量由：

- 厨房产能；
- 保温箱；
- 三轮车；
- 配送人员；
- 午餐时间窗；

决定。

所以不能用页面“看起来简单”推断服务规模小，也不能用订单增长推断网站技术先进。

---

# 第七部分：建立最小 execution state machine

## 13. 推荐状态链

```text
merchant / kitchen exists
→ public listing exists
→ menu published
→ service area valid
→ service time valid
→ user discovers listing
→ user selects items
→ order attempt
→ [web submit | phone handoff | IM handoff]
→ merchant receives request
→ merchant accepts / rejects
→ item inventory confirmed
→ preparation
→ courier assigned / human delivery begins
→ address found
→ building / campus access passed
→ handoff to customer
→ payment settled
→ customer accepts meal
→ complaint / refund / repeat / no repeat
```

历史证据必须注明自己停在哪一格。

---

## 14. 一组必须固定的非等价关系

### 页面层

`restaurant listed ≠ restaurant open`

`menu page survived ≠ menu current`

`item shown ≠ item available`

`displayed price ≠ executed price`

### 地址层

`city supported ≠ address supported`

`address field exists ≠ address accepted`

`delivery promise ≠ delivery radius verified`

### 下单层

`order form exists ≠ form submitted`

`form submitted ≠ merchant received`

`merchant received ≠ merchant accepted`

### 配送层

`accepted order ≠ courier dispatched`

`courier dispatched ≠ address found`

`promised 30 minutes ≠ delivered in 30 minutes`

`delivered ≠ customer accepted / ate`

### 使用层

`account exists ≠ account ordered`

`review exists ≠ reviewer consumed exactly that historical listing`

`site traffic ≠ successful meals delivered`

---

# 第八部分：新增 archive gaps

## 15. menu-state gap

历史菜单保存了展示，不一定保存：

- 当天售罄；
- 临时价格；
- 配送费；
- 起送价；
- 套餐替换。

## 16. delivery-zone state gap

服务区通常是后台状态或动态查询结果。

静态首页不能恢复某楼宇当日是否可送。

## 17. order-receipt gap

即使能复原 POST / 表单，也通常没有：

- 商家后台订单列表；
- 丢单；
- 重复单；
- 商家拒单。

## 18. phone / IM handoff gap

执行离开公共 Web 后进入：

- 电话；
- MSN；
- QQ；
- 短信；
- 人工内部系统。

Web archive 在这里天然断裂。

## 19. kitchen-inventory gap

公开菜单不是厨房实时库存。

这是 food ordering 与普通静态内容站点最不同的状态之一。

## 20. dispatch-routing gap

实际配送涉及：

- 哪个分店接单；
- 哪个配送员；
- 路线；
- 批量拼单；
- 雨雪 / 堵车；
- 楼宇进入。

这些一般不进入公共页面。

## 21. delivery-outcome gap

“订单存在”仍无法回答：

- 是否准时；
- 是否错餐；
- 是否退款；
- 顾客是否再次下单。

## 22. time-promise gap

页面写“30 分钟”“40 分钟”是 **service promise**。

除非有实际日志 / 同期用户记录，不能写成历史实测延迟。

## 23. merchant-churn gap

同一平台中的餐馆、菜单和配送范围可能快速变化。

一个 2006 年与一个 2007 年 capture 不能直接拼成“连续存在一年”。

## 24. success-privacy gap

网上订餐的真正成功证据通常是：

- 姓名；
- 电话；
- 送餐地址；
- 订单内容；
- 支付；
- 配送轨迹。

这些恰好是最不应该公开重建的个人数据。

因此：

> **交易执行结果缺失，在很多情况下是正确的隐私边界。**

本仓不得为证明“订单真的发生”而寻找、下载或重新发布泄露订单数据库。

---

# 第九部分：平台死亡——2014 饭统网提供的不是“失败史”，而是 survival boundary

## 25. 饭统网“失联”说明品牌记忆与可执行服务可以瞬间分离

2014 年 4 月，多家同期媒体记者观察到饭统网官网无法打开、400 电话无人接听 / 无法正常提供服务，办公地点也出现异常。

来源：

- 中新网 / 北京晨报，2014-04-24：<https://www.chinanews.com.cn/cj/2014/04-24/6100345.shtml>
- 人民网 / 京华时报，2014-04-25：<https://it.people.com.cn/n/2014/0425/c1009-24940885.html>

### 证据等级

**B：2014 同期记者状态观察。**

### 25.1 这给 2004–2010 artifact 带来的提醒

一个平台可以留下：

- 新闻稿；
- 搜索结果；
- 媒体报道；
- 百度快照；
- 用户回忆；

但真正的：

- 商家库；
- 历史菜单；
- 订单；
- 评价上下文；
- 账号状态；

可能随服务器关闭一起失去。

因此：

> `brand remembered ≠ operational database survived`。

### 25.2 不做事后英雄叙事

2014 的倒闭 / 失联不能倒推出：

> “它 2004–2010 的技术路线从一开始就必然失败。”

后来的平台竞争结果不应反投成早期用户体验的解释。

---

# 第十部分：A / B / C / D 证据表

| Claim | 当前证据 | Grade | Confidence | 限制 |
|---|---|---:|---|---|
| Web 前已有专业电话送餐 | 2003 对 1993 的创始人回忆 + 媒体交叉 | C/B | medium-high | 非 1993 原始记录 |
| 2004 丽华北京提供网上菜单 / 订餐 | 《新京报》记者观察 | B | high | 未取得原始 HTML |
| 2006 3797 支持按楼宇 / 小区找外卖店、购物车、地址下单 | 《每日经济新闻》操作描述 | B | high | 商家数量多为公司 claim |
| 2007 丽华存在 MSN 订餐机器人 | 《北京晚报》记者实测 | B | high | bot / MSN 服务本身未保存 |
| 2008 宜客网以网站揽单、三轮车配送 | 同期媒体现场报道 | B | high | 原站 capture 未验证 |
| 2014 饭统网官网无法访问、电话异常 | 多家同期记者观察 | B | high | 证明 2014 状态，不证明更早 archive 完整性 |
| 精确浏览器 / charset / JS 要求 | 无 | — | unknown | 本轮必须停在“不知道” |
| 历史真实订单成功率 / 配送延迟 | 无 | — | unknown | 私有数据库与线下执行缺失 |

### 关键不足

**本轮没有拿到 A 级历史原始网页 capture。**

因此本文件是：

> **基于多个 B 级同期独立媒体 observation 建立的 execution / archive-gap research note**，

不是完整页面复原案例。

这符合仓库 stop condition：证据不够时降低结论强度，而不是补造历史 HTML。

---

# 第十一部分：浏览环境 checklist

未来若取得 2004–2010 原始 capture，至少检查：

- `Content-Type`；
- `charset`：GB2312 / GBK / UTF-8；
- table / frameset；
- form `method` / `action`；
- JS 是否控制购物车；
- cookies / session；
- login requirement；
- address autocomplete / query endpoint；
- image menu 是否缺失；
- Flash / ActiveX 是否出现；
- IE-only browser sniff；
- HTTP → HTTPS 是否存在；
- archive rewrite 是否破坏 POST / JS；
- 动态结果是否被 archive 当作不可重复 URL；
- merchant detail 是否含个人手机号 / 不应重新公开的地址信息。

在验证前，一律不猜。

---

# 第十二部分：隐私 / 版权 stop conditions

## 26. 不恢复普通人的历史订单

不要为了证明交易完成而重建：

- 真实姓名；
- 手机号；
- 宿舍 / 家庭地址；
- 历史订单明细；
- 支付记录；
- 配送轨迹。

## 27. 不批量复制历史菜单图片

版权不明时优先保存：

- URL；
- capture metadata；
- 菜单字段结构；
- 价格范围的最小必要摘要；
- 页面布局与技术分析。

## 28. 不用现代网站替代旧站

今天还能打开的品牌官网只能证明当前状态。

除非有历史 capture datetime，否则不能截图现代页面并标作“2006 网上订餐”。

---

# 第十三部分：本轮能写进平台技术谱系的最小结论

中文网上订餐在 2004–2008 的可见形态至少包括：

```text
电话送餐（Web 前已有）
→ Web 公开菜单 / 表单
→ 按写字楼 / 小区查询配送商家
→ 购物车 + 地址输入
→ Web 与电话并存
→ MSN 等 IM 订餐
→ 小型校园订餐网站 + 人工三轮配送
```

这条谱系的历史意义不在于“越来越在线”。

更准确的是：

> **用户入口越来越数字化，而订单接收、厨房、调度、配送与门口交付长期保持高度物理化。**

所以网上订餐是一个典型的 **public-interface / private-execution split（公开界面 / 私有执行分裂）**。

这也解释了为什么它对普通生活影响很大，却很难被 Web archive 完整保存。

---

# 第十四部分：交叉链接到 `how-people-lived`

生活史侧另见：

`how-people-lived/topics/meal-provisioning-food-delivery-and-kitchen-optionality-china-1993-2025.zh-CN.md`

生活史文件主要讨论：

- 每日供餐拓扑；
- meal-time externalization；
- kitchen optionality；
- meal latency / delivery radius；
- 2008 毕业创业；
- 2019 骑手作为陌生城市进入桥；
- 2020 平台买菜与供餐模式切换；
- 2025 成本 / 卫生核验；
- 法国 Minitel 的 Web 前海外对照。

这些全球比较和 2019–2025 生活史材料不扩进本仓主体，以维持 `old-web-archaeology` 约 1995–2015 中文互联网 scope。

---

# 第十五部分：下一步证据目标

最高价值的下一步不是再找“某平台有多少家餐馆”，而是取得一个 **2004–2010 的原生 execution slice**：

```text
历史 menu / merchant capture
+ service-area query result
+ 同期用户教程 / 论坛帖
+ 电话 / IM handoff 的最小证据
+ 同期用户关于迟到 / 改价 / 售罄 / 成功送达的公开记录
```

理想情况下至少有两个独立历史时点。

只有拿到这些，才能进一步回答：

> **一个旧网页上的“订餐”按钮，在当年到底连接到了多长的一条真实生活链。**
