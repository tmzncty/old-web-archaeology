# SECONDHAND MARKET / BBS / C2C：listing、担保支付、验货、物流与成交状态缺口（中文旧网，1999—2015）

> Scope：本笔记只研究约 1999—2015 中文互联网中的个人交易/二手交易页面、校园 BBS secondhand 版、早期 C2C、担保支付与线上发现—线下成交的技术/事务状态。1990s 以前的旧货市场与海外 BBS 只作为前史边界；2018—2026 的移动二手平台只作为 afterlife，不把本仓扩成全球二手经济史。
>
> Cross-repo companion：`tmzncty/how-people-lived/topics/from-flea-market-to-resale-platform-secondhand-goods-asset-liquidity-and-reversible-consumption-china-1990s-2026.zh-CN.md`
>
> 检索日期：2026-09-08。
>
> M1 status：**NOT ACHIEVED IN THIS SLICE**。本轮取得多个同期 historical locator 和事务描述，但未取得一份可按 `docs/METHOD.md` 检查 capture datetime、HTTP、charset、DOM、脚本、session、图片子资源与历史浏览器行为的合格 historical replay。

---

## 1. 研究单位：不要把“二手交易网站”当成一个状态

旧网里的“二手交易”至少包含以下不同研究单位：

1. **platform**：例如 Eachnet / eBay 易趣、淘宝；
2. **host/site**：例如 `eachnet.com`、`www.alipay.com`；
3. **BBS service**：例如水木清华类校内 BBS；
4. **board**：例如 secondhand / 二手市场版；
5. **account**：卖家、买家、校园账号；
6. **listing/post**：一件物品的一次出售帖；
7. **message/contact**：站内信、QQ、电话、邮件；
8. **offer/bid**：报价或竞价状态；
9. **payment instruction**：汇款/担保支付指令；
10. **escrow ledger**：第三方是否实际收到钱；
11. **delivery**：面交、邮寄、快递；
12. **inspection/acceptance**：买家是否认可成色与功能；
13. **settlement**：卖家最终是否拿到钱；
14. **archive artifact**：后来档案服务保存了哪一层。

这些单位不能互换。

所以以后看到一句“2004 年已经可以网上买二手”，必须继续问：

```text
在哪里看到？
谁能登录？
能不能发帖？
联系方式怎样交换？
钱在网页里付还是银行/邮局付？
货是快递还是面交？
有没有验货？
平台有没有确认成交？
今天 archive 保存的是 listing、首页，还是只有新闻报道？
```

---

## 2. 前 Web 边界：旧货市场已经有“信息—估价—结算—运输”栈

1998 年 3 月 9 日施行的《旧货流通管理办法（试行）》定义“旧货”为已经进入生产或生活消费、处于储备/使用/闲置状态、仍有部分或全部使用价值的物品，并把旧货市场定义为可以提供信息、评估、结算、加工翻新、保管、运输等配套服务的场所。

Source:
https://www.hengqin.gov.cn/lab/flfg/bmgz/content/post_3727256.html

Evidence grade: **A**（1998 部门规章文本的政府站点转载）  
Confidence: **high**.

这条边界的意义是：

> **Web 没有发明信任、估价、结算和运输问题。**

实体旧货市场已经把它们组合在一起。

中文旧网后来做的事情，是把其中“信息聚合、身份、评价、支付指令和部分争议处理”数字化，同时让真实物品继续留在物理世界。

---

## 3. 海外 pre-Web 对照：BBS 可以先做 marketplace discovery，成交仍走电话

1990 年《Washington Post》的二手电脑购买指南已经建议读者使用本地/全国 BBS 查找二手 PC，并点名 CompuServe、MCI Mail、Delphi 上的 Boston Computer Exchange；文章同时强调二手设备的保修与故障风险。

Source:
https://www.washingtonpost.com/archive/business/1990/09/24/used-equipment-market-is-haphazard-but-bargains-can-be-found/3749531f-bfe4-4144-a4e1-7e7566a244c4/

Evidence grade: **B**（1990 同期媒体）  
Confidence: **high**.

1991 年《Christian Science Monitor》又记录 Boston Computer Exchange 从 1982 年开始经营旧电脑交易，到 1991 年已是规模化经纪市场。

Source:
https://www.csmonitor.com/layout/set/amphtml/1991/1029/29141.html

Evidence grade: **B**  
Confidence: **high**.

后来的 BCE 创办人回访材料描述了一种很值得和中国早期 Eachnet 对照的状态：商品数据库可以经 Delphi 等在线服务远程查询，但交易仍可能通过电话与线下付款/寄送完成。

Source:
https://www.ecommercetimes.com/story/online-pioneer-marks-silver-anniversary-of-e-commerce-61952.html

Evidence grade: **C/B boundary**（2008 回访）  
Confidence: **medium-high** for mechanism.

因此以下结构并非中国特有：

```text
NETWORK_DISCOVERY
→ OFF_NETWORK_CONTACT
→ OFF_NETWORK_PAYMENT
→ PHYSICAL_DELIVERY
```

这也是研究中文 1999—2005 C2C 时必须避免后见之明的原因。

---

## 4. 1999—2000 Eachnet：Web 把陌生人介绍给彼此，上海街头才真正完成交易

### 4.1 historical locator

2000 年《Washington Post》同期报道直接使用：

```text
Eachnet.com
```

并称其为上海的个人交易 World Wide Web 站点。

Source:
https://www.washingtonpost.com/archive/business/2000/03/26/dot-comrades-start-small/949819e5-2900-452e-bb2a-d1966a57c3b2/

Evidence grade: **B**（2000 同期现场报道）  
Confidence: **high** for host identity and observed use.

这是一条 **historical locator**，不是本仓已验证的 archive capture。

### 4.2 普通用户使用：浏览器里的交易仍然回到公交车、校门口与现金

报道中的 25 岁上海公务员高晓怡从报纸广告知道 Eachnet，为寻找一只波斯猫配偶而进入网站。更关键的是记者对平台实际交易结构的观察：

- 交易很少超出上海市区；
- 支付与配送基础设施不足；
- 买家倾向亲自验货；
- 卖家收现金；
- 双方会在人民广场大屏幕下或复旦大学校门口等公共地点见面。

同一报道列出的常见小额 listing 包括家电、钥匙扣、CD、手机、部分使用过的电话卡等。

Evidence grade: **B**  
Confidence: **high** for observed pattern; 平台声明的用户数/日交易量只证明“平台当时如此宣称”。

这使 2000 Eachnet 的最低事务模型应写成：

```text
LISTING_CREATED
→ LISTING_VISIBLE
→ BUYER_DISCOVERS
→ CONTACT/BID
→ MEETING_ARRANGED
→ PHYSICAL_INSPECTION
→ CASH_EXCHANGED
→ ITEM_HANDED_OVER
```

而不是现代人默认的：

```text
LISTING
→ ONLINE_PAYMENT
→ SHIPPING
→ RECEIPT_CONFIRMATION
→ PLATFORM_SETTLEMENT
```

### 4.3 每个箭头都可能失败

例如：

- 帖子存在，但买家没看到；
- 买家出价，但双方没约成；
- 约好见面，但有人爽约；
- 见面后发现成色不符；
- 买家现金不足；
- 大件无法搬运；
- 双方完成交易，但平台没有完整“成交事件”记录。

所以：

> **Web-visible intent != completed resale.**

---

## 5. 2004 实体校园跳蚤市场：旧网并没有自动替代“手递手”

北京交通大学 2004 年同期校内报道记录一次 160 多个摊位的毕业跳蚤市场。原因是毕业生物品不便携带，低年级学生需要低价学习/生活用品；商品包括书籍音像、日用品、文体用品、小家电。

Source:
https://news.bjtu.edu.cn/info/1044/13458.htm

Evidence grade: **A/B boundary**（校方同期记录）  
Confidence: **high**.

报道还记录校外人员混入并使用假钞。

这个案例对旧网考古很重要，因为它说明即使 Web/BBS 已存在：

- 当面验货仍有价值；
- 现金仍然需要真伪验证；
- 同校空间本身是一种 market infrastructure；
- 卖自行车、被褥、小家电的最佳界面可能仍是操场/小树林，而不是网页。

因此不能从 `BBS secondhand board exists` 推出 `physical flea market obsolete`。

---

## 6. 2005 水木清华类 BBS：同一个市场可能同时属于 Telnet 和 Web，而不是“一个网页”

CERNET 2005 年同期报道明确写道，用户可使用 Sterm 或 Cterm 等终端客户端连接：

```text
166.111.8.238
```

进入“BBS 水木清华站”；报道列出的 600 多个版面中包括二手市场、兼职、career、选课、考研、交友等生活版面。

Source:
https://www.edu.cn/xin_xi_zi_xun_1625/20060323/t20060323_121263.shtml

Evidence grade: **B**（2005 同期报道）  
Confidence: **high** for address/access-client description and board existence.

这给旧网考古增加一个关键对象层：

> **BBS board != Web page.**

同一个 board 可能同时有：

- Telnet/terminal 客户端入口；
- Web gateway；
- 不同编码/字符终端；
- 不同登录态；
- 不同校内/校外网络策略。

因此未来即使找到一份 HTML capture，也不能自动声称复原了当时 Sterm/Cterm 用户看到的交易体验。

需要分别记录：

```text
service protocol
client software
host/IP
board name
web gateway URL (if any)
auth state
network-location restriction
encoding
post rendering
contact-field rendering
```

---

## 7. 2005—2006 高校 BBS 网络边界变化：访问控制会直接缩小/改变 marketplace graph

2006 年同期报道回顾 2005 年高校 BBS 调整访问范围时写道，在“水木清华”限制校外 IP 以后，本校学生、离校校友、社会网友的发言权限不再相同；社会用户在报道所述状态下只能在征友、二手市场等有限版面发言，校友另有院系版权限。

Source:
https://news.sina.com.cn/c/edu/2006-07-03/15389360675s.shtml

Evidence grade: **B**（2006 同期报道）  
Confidence: **medium-high** for described policy state; exact per-board technical ACL implementation仍需原始站务公告/capture.

中山大学“逸仙时空”的同期报道又保存了类似网络位置限制：2005 年 3 月关闭校外访问/发文后，到 2006 年部分校外发文权重新开放。

Source:
https://news.sina.com.cn/c/2006-10-18/100811268788.shtml

Evidence grade: **B**  
Confidence: **high** for reported chronology.

这意味着一个二手版面的市场半径可能因为技术/管理配置发生变化：

```text
同校学生可读写
校友可读但受限写
社会用户只能某些版发言
校外 IP 甚至不能登录
```

所以：

> **BOARD EXISTS != SAME AUDIENCE REACH.**

同一个 board name 在 2004、2005、2006 可能对应不同可交易人群。

旧网研究如果只保存页面截图，很容易完全漏掉这一层。

---

## 8. 2005 支付转折：从“把钱汇给陌生人”到“把钱暂存给第三方”

### 8.1 支付宝 historical locator

2005 年《江南时报》同期报道明确记录：

```text
www.alipay.com
```

并把支付宝机制描述为：买家确认收货以前，由第三方暂时保管货款。

Source:
https://finance.sina.com.cn/roll/20050203/04301343972.shtml

Evidence grade: **B**  
Confidence: **high** for product mechanism and historical host.

### 8.2 最小 escrow state machine

```text
BUYER_INITIATES_PAYMENT
→ BANK/PAYMENT_RAIL_ACCEPTS
→ ESCROW_CREDITS_ORDER
→ SELLER_SEES_PAID/SECURED
→ SELLER_SHIPS
→ BUYER_RECEIVES
→ BUYER_ACCEPTS or DISPUTES
→ ESCROW_RELEASES or HOLDS/REFUNDS
→ SELLER_BALANCE_AVAILABLE
```

因此：

- `buyer says money sent != escrow credited`
- `escrow credited != seller shipped`
- `seller shipped != buyer received`
- `buyer received != buyer accepted condition`
- `platform marks complete != no later dispute`

### 8.3 eBay 易趣“安付通”：同期投诉恰好证明 UI 状态和资金状态可以分裂

2005 年《新闻晨报》报道一名易趣注册用户胡女士第一次使用安付通时遇到：自己认为钱已经汇出，但平台仍发信提示未付款；她又一度联系不上客服，担心订单被取消。

Source:
https://tech.sina.com.cn/i/2005-01-26/0711514776.shtml

Evidence grade: **B + contemporaneous user complaint**  
Confidence: **high** for existence of this failure mode.

这是一条非常好的旧网 transaction-state 证据：

```text
USER_BANK_ACTION_COMPLETED
!= PLATFORM_ESCROW_LEDGER_CREDITED
!= ORDER_UI_MARKED_PAID
```

历史研究者如果只看到某个订单页的“未付款”，不能反推用户从未汇款。

反过来也一样：用户说“我已汇”，不能直接证明平台/银行最终结算完成。

### 8.4 安付通升级时间

2005 年 eBay 易趣相关同期报道称，“安付通”于 2004 年 10 月推出，2005 年升级买卖双方保障；报道还称易趣更早于 2001 年推出“易付通”。

Source:
https://tech.sina.com.cn/i/2005-06-08/1620630374.shtml

Evidence grade: **B / company-announcement mediated**  
Confidence: **high** for announced dates, **lower** for vendor usage-growth claims.

---

## 9. 支付“在线化”也不能自动证明交易已经脱离邮局/银行/电话

2005 年另一篇同期报道解释为什么诚信支付工具被平台当作关键基础设施：普通银行汇款、邮局汇款可能产生手续费，跨行又增加成本，卖家甚至需要提供多张银行卡。

Source:
https://tech.sina.com.cn/i/2005-06-08/1411630177.shtml

Evidence grade: **B / company statement mediated**  
Confidence: **medium-high** for contemporary transaction friction.

所以 old-Web 的交易页面至少还要问：

- 页面只是显示卖家银行卡号吗？
- 用户需要离开电脑去 ATM/柜台吗？
- 是否支持网银？
- 需要哪个银行？
- 支付状态靠自动回调还是人工确认？
- 是否有担保账户？
- 是否有手续费？
- 订单超时多久取消？

这些都是当年的**执行条件**，不是页面美术细节。

---

## 10. 2006 校园“网络跳蚤市场”：BBS 不只有个人闲置，也开始混入校园代理与准商业卖家

2006 年《钱江晚报》报道记者查看复旦、清华、北大等高校 BBS 的“网络跳蚤市场”，发现其中活跃着校园代理，商品从电脑、MP3/U 盘到服装、化妆品等。

Source:
https://news.sina.com.cn/o/2006-12-27/042810869384s.shtml

Evidence grade: **B**（2006 同期报道）  
Confidence: **high** for observed phenomenon.

这意味着“二手版”不等于“所有 listing 都是个人旧物”。

旧网考古至少要给 seller role 留出：

```text
PERSONAL_USED_GOOD
PERSONAL_UNUSED_GOOD
CAMPUS_AGENT
SMALL_MERCHANT
PROFESSIONAL_RESELLER
UNKNOWN
```

否则研究者可能把一个学生代理的新货广告误读成“2006 大学生二手消费”。

同理：

> **board label != item provenance.**

---

## 11. 2008 毕业季：offline market 仍然给我们提供“listing 消失以后”的现实对照

2008 年中新网南昌高校报道记录，大四女生在寝室出售半新衣物和书，一次交易中低年级学生花 43 元买走一件毛衣和一本英文书；报道还指出，部分外地毕业生因为行李问题提前处理物品。

Source:
https://news.sohu.com/20081128/n260915734.shtml

Evidence grade: **B**  
Confidence: **high** for observed case.

广州同期报道的毕业清仓则包括冰箱、空调、日用品、网店库存等。

Source:
https://news.sohu.com/20080701/n257861290.shtml

Evidence grade: **B**.

这些线下材料对 old-Web 非常重要，因为网上的普通 listing 很可能已经消失，而同期记者把**为什么卖、卖什么、怎样讨价还价、最后谁买走**保存了下来。

它们可以作为 B 级 transaction-context，不应伪装成原始 BBS page。

---

## 12. 2014 华科“白云黄鹤” secondhand：线上 listing + QQ/微信/电话 + 线下验货是完整事务

2014 年荆楚网报道华中科技大学“白云黄鹤”BBS secondhand（二手版）。卖家在线发布商品文字和照片，买家再通过 QQ、微信、电话联系，最后线下验货成交。

Source:
https://edu.cnhubei.com/qczx/201404/t20140430_34000.shtml

Evidence grade: **B**（2014 同期报道）  
Confidence: **high** for described workflow.

一名毕业生的示例 listing 被报道为：原价约 2600 元的自行车，骑行约 500 公里，毕业时标价 1700 元，理由是毕业后带不走。

这让 2014 仍然可以写成：

```text
BBS_POST
→ PHOTO/TEXT_DESCRIPTION
→ BUYER_DISCOVERY
→ QQ/WECHAT/PHONE_CONTACT
→ LOCAL_MEETUP
→ INSPECTION
→ BARGAIN
→ PAYMENT
→ HANDOVER
```

因此：

> **O2O 不是移动互联网时代才出现的漂亮商业概念；在校园 BBS 里，online discovery + offline inspection 本来就是二手物的自然事务结构。**

---

## 13. 为什么二手物特别需要“item-state machine”

新品网页通常有相对稳定 SKU。

个人二手 listing 却描述一个唯一物件。

因此至少要区分：

```text
ITEM_EXISTS
→ ITEM_OWNED_BY_SELLER (claimed)
→ CONDITION_DESCRIBED
→ PHOTO_UPLOADED
→ DEFECT_DISCLOSED (or not)
→ RESERVED
→ INSPECTED
→ ACCEPTED / REJECTED
→ HANDED_OVER / SHIPPED
→ RECEIVED
→ DISPUTED / FINAL
```

典型缺口包括：

- “九成新”没有统一历史尺度；
- 图片可能避开瑕疵；
- 电脑/手机可能存在间歇故障；
- 自行车可能现场才发现暗伤；
- 图书可能有批注/缺页；
- 卖家声称“自用”不等于平台能验证来源；
- listing 的原价/购买时间可能只有卖家自述。

所以旧网研究不能把 listing 文案直接提升为 A 级现实物品事实。

正确写法是：

> “该 listing / 同期报道中的卖家把物品描述为……”

而不是：

> “这件物品客观上就是九成新。”

---

## 14. 另一个 state machine：marketplace reach

二手市场的“网上可见”还要拆人群边界。

```text
PAGE PUBLICLY REACHABLE
ACCOUNT CREATION AVAILABLE
LOGIN AVAILABLE
POSTING AVAILABLE
SEARCH/BROWSE AVAILABLE
CONTACT INFO VISIBLE
EXTERNAL IP ALLOWED
NON-STUDENT ACCOUNT ALLOWED
LOCAL MEETUP FEASIBLE
CROSS-CITY SHIPPING FEASIBLE
```

2005—2006 高校 BBS 的访问调整证明：

- host 仍在线；
- board 仍存在；
- 某类人却可能突然不能发帖。

这是一种 **market radius controlled by ACL**。

如果只做页面截图，几乎看不出来。

---

## 15. “成交”也必须拆成最少四种定义

历史材料中的“成交”可能指：

### A. Social agreement

双方口头/消息里说“要了”。

### B. Platform order state

平台生成订单或拍卖结束。

### C. Economic settlement

钱已经最终进入卖家可支配账户。

### D. Physical transfer

物品已经被买家实际接收并接受。

四者可能不同步。

因此 old-Web 数据抽取若未来建立 schema，建议字段至少保留：

```yaml
listing_state:
order_state:
payment_state:
delivery_state:
inspection_state:
settlement_state:
source_for_each_state:
```

不能只有：

```yaml
sold: true
```

---

## 16. 早期 C2C 的“交易半径”不是由 HTML 决定，而是由最弱的后端/线下环节决定

2000 Eachnet 的新闻现场说明：

```text
Web 可以全国访问
但
付款 + 物流 + 验货只能稳定支持同城
```

所以真实交易半径是：

```text
min(
  information reach,
  trust reach,
  payment reach,
  delivery reach,
  inspection tolerance
)
```

这是一条非常适合中文旧网考古的解释模型。

一个全国可打开的网站，实际可能只是一个**同城陌生人见面的目录**。

反过来，一个校内 BBS 的覆盖范围很小，却因为同校、可面交、距离短而拥有更高完成率。

`global page` 不一定比 `local board` 更“先进”。

---

## 17. 浏览器/客户端环境：二手 BBS 需要特别防止“Web 化后见之明”

本专题已知至少有这些历史客户端/渠道：

- Sterm；
- Cterm；
- Telnet BBS；
- Web gateway；
- 普通浏览器 C2C 页面；
- QQ；
- E-mail；
- 电话；
- 2000s 后期即时通讯与移动端。

因此未来复原一个 secondhand board 时需要记录：

### Terminal path

- terminal client name/version；
- encoding；
- ANSI color/control sequences；
- screen size；
- login prompt；
- board navigation keys；
- post quoting；
- private message behavior。

### Web path

- host/path；
- charset；
- frames/table layout；
- cookie/session；
- login gate；
- POST form/action；
- image upload；
- pagination；
- contact information rendering；
- IE-only / JS dependency if any。

现代 Chromium 能打开某个后来的 HTML 页面，不足以证明历史 terminal/Web 用户看到同样界面。

---

## 18. Archive preservation：普通 listing 是旧网里特别容易消失的一类对象

### 18.1 listing 生命周期短

一件自行车可能：

```text
上午发帖
→ 下午有人联系
→ 晚上面交
→ 第二天删帖/沉底
```

Wayback 的抓取频率即使不低，也很容易完全错过。

### 18.2 登录与动态参数

交易页可能依赖：

- 登录；
- session cookie；
- POST；
- 动态 item id；
- 图片服务器；
- 搜索结果页；
- 用户中心。

档案服务很容易只保留首页和帮助页。

### 18.3 子资源比 HTML 更脆弱

即使 listing HTML 幸存：

- 商品图片可能来自独立 host；
- 缩略图可能存在，原图丢失；
- JS 表单失效；
- 价格状态与订单状态来自后台 API/CGI；
- QQ/电话沟通完全不在 Web archive。

### 18.4 成交以后的现实状态几乎天然不可见

archive 能证明：

> 某页面某时刻写着“1700 元出售”。

通常不能证明：

> 最终是不是 1700 元成交、什么时候成交、买家验货后是否退掉。

所以：

> **listing archive != transaction archive.**

---

## 19. 隐私边界：越是“普通人的交易页”，越不能因为 archive 可访问就重新公开全部个人信息

历史二手帖常直接包含：

- 手机号；
- QQ；
- 宿舍楼；
- 真实姓名；
- 校内账号；
- 见面地点；
- 设备序列号；
- 个人照片。

本仓应坚持 `docs/METHOD.md` 的必要最小化：

- 研究版面结构时不复制普通人完整联系方式；
- 研究 URL pattern 时抽象个人 ID；
- 只有当某条个人信息本身是历史 claim 的必要证据时才考虑保留最少部分；
- 不把已经删除的普通交易帖批量再公开；
- 不上传版权不明的商品图片/页面整页镜像。

---

## 20. 2022 易趣关站：平台死亡不仅删首页，也会切断交易 ledger 与账户路径

2022 年易趣关闭公告的同期报道记录：平台计划于 2022 年 8 月 12 日 24:00 关闭商品/商铺交易、注册、登录、充值功能并关闭网站服务器；关闭前还要求用户查看账户、历史交易记录并处理余额退回。

Sources:
https://www.nbd.com.cn/articles/2022-07-23/2375724.html
https://sc.people.com.cn/n2/2022/0725/c345529-40052142.html

Evidence grade: **B + platform-announcement mediated**  
Confidence: **high** for shutdown state.

这只作为 1999—2015 系统的 afterlife，不扩大本专题主 scope。

但它给保存史留下很明确的状态：

```text
TRADING_DISABLED
REGISTRATION_DISABLED
LOGIN_DISABLED
RECHARGE_DISABLED
BALANCE_REFUND_WINDOW
SERVER_SHUTDOWN
```

因此：

- `brand remembered != service accessible`
- `homepage screenshot survives != account ledger survives`
- `press article survives != ordinary listing survives`
- `platform history page survives != user can retrieve transaction history`

对旧网研究而言，这类关站公告是理解 archive gap 的重要证据。

---

## 21. afterlife check：移动平台并没有消灭旧问题，只是把它们重新包装

2018 年《人民日报》采访 90 后职员赵琳：她在二手平台购买一条八成新的首饰链，300 元成交，两天后由卖家寄到；后来又购买包和台灯。

Source:
https://society.people.com.cn/n1/2018/0727/c1008-30173724.html

Evidence grade: **B**（afterlife only）.

2025 年商务部仍把线上二手交易不规范、实体市场发展滞后和交易信任成本较高列为堵点。

Source:
https://ltfzs.mofcom.gov.cn/gzdt/art/2025/art_5b693d5311db462bb0c9d01eba6458e9.html

Evidence grade: **A**（afterlife only）.

这说明旧网时代的三个核心难题没有消失：

1. **这件东西到底是什么状态？**
2. **这个陌生人可信到什么程度？**
3. **钱和货在不同时间、不同网络里移动时，怎样安全交换？**

新平台只是增加了实名、评分、担保、快递跟踪、验机、仲裁等更多层。

因此研究 2000s 时，不能把它们当成“还没发明现代解决方案的幼稚阶段”；应该准确记录每一代系统当时究竟把哪一个缺口收窄了。

---

## 22. Evidence ledger

| Claim | Source | Grade | Confidence | What it proves | What it does **not** prove |
|---|---|---|---|---|---|
| 1998 旧货市场定义已包含信息、评估、结算、运输等 | 旧货流通管理办法 | A | high | pre-Web institutional stack | 普通家庭使用率 |
| 2000 Eachnet.com 被普通上海用户使用 | Washington Post 2000 | B | high | platform/host/use case | 全国普及 |
| Eachnet 大量交易仍同城验货、现金 | Washington Post 2000 | B | high | online-discovery/offline-completion | 所有订单都如此 |
| 2004 北交大 160+ 摊位毕业跳蚤市场 | 校方同期新闻 | A/B | high | physical market coexistence | BBS 使用率 |
| 水木可用 Sterm/Cterm 连接 166.111.8.238，含二手版 | CERNET 2005 | B | high | terminal access + board existence | Web DOM/charset |
| BBS 外网权限调整改变可发帖人群 | 2006 同期报道 | B | medium-high | market reach can depend on ACL | 精确服务器规则实现 |
| `www.alipay.com` 2005 同期存在并被描述为担保型支付 | 江南时报 2005 | B | high | host + escrow model | 某一笔交易完成 |
| 安付通用户出现“钱已汇出但订单仍提示未付” | 新闻晨报 2005 | B | high | payment-state divergence | 银行最终结算状态 |
| 2014 白云黄鹤 secondhand 采用线上帖+线下验货 | 荆楚网 2014 | B | high | late old-Web O2O pattern | board 的历史 DOM/capture |
| 易趣 2022 关闭交易、登录、服务器 | 关闭公告同期报道 | B | high | platform afterlife | archive 是否保有普通 listing |

---

## 23. 已证实 / 高概率 / 不知道

### 已证实

1. 2000 年 `Eachnet.com` 已被普通上海用户用于个人交易发现；
2. 当时支付、配送和验货仍使大量交易回到同城面交/现金；
3. 2004 年高校实体跳蚤市场仍有很强现实功能；
4. 2005 年校园 BBS 已有二手市场版，且可通过 terminal 客户端访问；
5. 2005 年担保支付已经尝试把钱—货异步交换制度化；
6. 2005 年同期投诉证明用户银行动作、平台到账状态与 UI 订单状态可能不同步；
7. 2014 年高校 BBS 二手交易仍明确采用线上发布、线下验货成交；
8. 2022 易趣服务器关闭使账号、交易与历史记录面临新的保存边界。

### 高概率，但仍需原始 capture/手册进一步证明

1. 不同高校 BBS 的 Web gateway 与 terminal interface 在字段、导航、登录上存在明显差异；
2. 早期个人交易 listing 很多依赖动态 URL、登录或独立图片 host，因此 archive 保存率低于门户静态文章；
3. 支付状态、商品状态和订单状态往往由多个后台系统维护，不是单一 HTML 状态；
4. 2000s 二手平台的页面结构会因浏览器、编码和脚本环境而改变。

### 不知道

1. 1999—2001 Eachnet 的完整 listing URL pattern；
2. 2000 年 Eachnet 页面原始 Content-Type/charset；
3. 2000 年首页/商品页是否依赖特定 JS、frames 或浏览器行为；
4. 水木清华二手市场版在 2005 年的 Web gateway 原始 URL 与 DOM；
5. 2005 安付通/支付宝交易页的完整状态文案和 session/cookie 行为；
6. 白云黄鹤 2014 secondhand 版具体 Web/Telnet 双栈实现；
7. 普通 listing 的 Wayback/Common Crawl 命中率；
8. 图片、成交标记、私信和支付回调在 archive 中各自保存到什么程度。

---

## 24. Historical locator registry（本轮只登记，不冒充 capture）

### Locator 1 — Eachnet

```text
historical host: eachnet.com
period evidenced: 2000
source: Washington Post, 2000-03-26
status: historical locator only
verified replay this run: no
```

### Locator 2 — 水木清华 BBS terminal address

```text
host/IP: 166.111.8.238
client examples: Sterm / Cterm
period evidenced: 2005
source: CERNET contemporaneous report
status: service locator / terminal access evidence
verified historical session this run: no
```

### Locator 3 — 支付宝

```text
historical host: www.alipay.com
period evidenced: 2005
source: contemporaneous press report
status: historical host locator
verified historical replay this run: no
```

### Locator 4 — 白云黄鹤 secondhand board

```text
platform/board: 华中科技大学“白云黄鹤” BBS / secondhand（二手版）
period evidenced: 2014
source: 荆楚网 contemporaneous report
status: platform/board identity; exact historical URL not established in this slice
verified replay this run: no
```

---

## 25. Archive attempt / M1 negative result

本轮按照 `docs/METHOD.md` 尝试继续向 historical capture 推进，重点对象包括：

- `eachnet.com` 1999—2005；
- `166.111.8.238` 2004—2006；
- 早期支付宝/担保支付 historical host。

当前 Web 访问工具对构造的 Internet Archive CDX 查询拒绝直接打开，未返回可实际检查的 capture 列表。因此本轮没有取得以下最低字段：

```text
capture_url
capture_datetime
original_url at capture
HTTP status
Content-Type
charset
DOM
script/subresource completeness
cookie/session behavior
historical browser rendering
```

所以：

> **M1 = NOT ACHIEVED IN THIS SLICE.**

严格按照仓库 METHOD：

- 只能写“本轮未验证到合格 historical capture”；
- **不能写“Wayback 没有保存”**；
- 搜索结果中的 host/URL 只能登记为 locator/candidate；
- 在实际打开并检查 replay 前，不进入完整 case 的 A 级 archive 结论。

---

## 26. 下一步最值得做的旧网考古切片

### A. Eachnet 1999—2002

目标：找到至少两个时点的首页 + item/listing 页。

优先检查：

- original URL patterns；
- user/item id 形式；
- listing expiration；
- bid/offer UI；
- contact method；
- seller reputation；
- image host；
- charset；
- payment instructions；
- offline-meetup guidance。

### B. 2005 campus BBS secondhand

目标：同一 board 比较 terminal 与 Web gateway。

优先检查：

- Sterm/Cterm terminal capture/截图/手册；
- Web gateway；
- 校内/校外 ACL；
- 发帖权限；
- 联系信息；
- board archive/精华区是否保留 sold posts。

### C. 支付 transaction page

目标：证明 2004—2006 至少一个真实支付流程的页面状态。

优先检查：

```text
UNPAID
PAYMENT_PENDING
ESCROW_CREDITED
SELLER_SHIP
BUYER_CONFIRM
DISPUTE
REFUND
SETTLED
```

### D. Archive-gap sampling

取 20 条同期新闻明确提到的二手 listing/board/platform，记录：

- 主站是否 capture；
- 商品页是否 capture；
- 图片是否 capture；
- 登录是否阻断；
- 动态参数是否阻断；
- contact/transaction state 是否可见。

这会比继续写平台史更接近本仓 M4 的“缺失地图”。

---

## 27. 对“中文旧网是什么”的修正

二手交易让我们看到一种很容易被首页截图掩盖的旧网结构。

1999—2000 的 Web 已经可以把两个陌生人介绍给彼此，但真正的交易可能在人民广场大屏幕下完成；2005 的 BBS 可以让学生每天浏览 secondhand 版，但一次自行车交易最可靠的结尾仍然是楼下见面、看车、给钱；担保支付再把“谁先相信谁”变成数据库状态；快递把市场半径推得更远，但物品的真假、暗病和成色始终留在物理世界。

因此中文旧网不是一个纯粹“在线”的世界。

它更像：

```text
HTML / terminal / BBS
+ QQ / phone / email
+ bank / post / escrow
+ campus gate / metro station / dorm
+ bicycle / parcel / courier
```

共同组成的一次事务。

**如果只保存网页，我们可能保存了“有人想卖一辆车”；只有把状态链补回去，才知道这个网页有没有真正让一个毕业生少带一件行李、让另一个学生第二天骑上那辆车。**

---

## 28. 本轮饱和判断

本轮发现了新的旧网事务机制：

- `online discovery != online completion`；
- `market radius controlled by weakest transaction layer`；
- `BBS board != Web page`；
- `ACL can reshape marketplace population`；
- `user remittance != escrow credit != UI paid state`；
- `listing archive != transaction archive`。

并取得 2000 Eachnet、2005 水木/支付、2006 BBS、2014 白云黄鹤等同期证据。

因此本轮不计入“连续无实质新增”次数；cross-research 当前仍为 **0/3**，不进入 closure。

---

> AI-assisted research note. 本文件不重新公开普通历史用户的电话号码、宿舍、QQ 等不必要个人信息；所有 locator 在获得 verified capture 前均保持 locator/candidate 状态。