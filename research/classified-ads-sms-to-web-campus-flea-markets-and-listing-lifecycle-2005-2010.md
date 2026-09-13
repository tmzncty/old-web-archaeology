# 从小广告、短信到同城 listing：客齐集、58、校园跳蚤网站与分类信息的跨通道考古，2005–2010

> Scope：中文旧网约 1995–2015 范围内，聚焦 2005–2010 分类信息 / 二手发布如何把墙面广告、短信、电话、便利店信息卡、校园地摊、BBS 与 Web listing 接在一起。  
> 交叉生活史包：`tmzncty/how-people-lived/sources/from-flea-markets-to-classified-platforms-possession-exit-and-resale-optionality-china-1998-2025.zh-CN.md`。  
> 本文不是 58 / 客齐集商业史，也不宣称已经恢复它们的历史首页。目标是：**先把“Web 页面上的一条分类信息到底从哪里进入系统、最后在哪里完成交易”拆开，再记录目前能确认的 historical identity、transaction chain、privacy risk 与 archive gap。**

---

## 0. 去重：不再增加一个泛化的 `page != transaction`

本仓已有大量案例反复证明：

```text
page != account
page != transaction
locator != verified capture
current live legacy page != historical memento
```

本轮不再把同一结论改名成新的 `state-gap`。

真正新增的是两个具体考古问题：

1. **`cross-channel publication / 跨通道发布`**：历史 Web listing 不一定由浏览器里的用户自己输入；它可能来自 SMS、电话、便利店纸卡、墙面小广告的人工登记。
2. **`listing lifecycle / listing 生命周期`**：分类信息页面的意义高度依赖“此刻是否仍有效”。保存了广告正文，不等于保存了它何时卖出、撤回、过期、被电话成交或在线下交付。

这两点会直接改变我们如何解释 2005–2010 的分类信息网页。

---

## 1. 研究单位：至少要把五层分开

### Layer A — source message / 原始信息

可能是：

- 电线杆 / 墙面小广告；
- SMS；
- 电话口述；
- 便利店填写的纸卡；
- 浏览器 Web form；
- 校园 BBS 下载的表格；
- 线下摊位。

### Layer B — ingestion / 录入系统

可能由：

- 用户本人；
- 客服；
- 志愿者；
- 网站管理员；
- 校园活动组织者

完成。

### Layer C — Web representation

例如：

```text
city subdomain
→ category
→ listing title/body
→ contact field
→ timestamp
```

### Layer D — contact / negotiation

电话、短信、QQ、MSN、站内联系、当面议价等。

### Layer E — handoff / actual transaction

见面交货、现金、转账、邮寄、委托网站代卖、赠送等。

如果只恢复 Layer C，就不能宣称整套分类交易已经复原。

---

## 2. Subject A：客齐集（Kijiji China）2005 的 historical identity 可以确认，但 Web capture 尚未确认

### 2.1 可确认的 historical identity

2005-09-26 的同期媒体报道明确给出：

- 品牌：客齐集 / Kijiji；
- historical host candidate：`shanghai.kijiji.com.cn`；
- 业务定位：分类信息；
- 强调小社区 / 本地 / 邻居对邻居；
- 用户信息可以从上网、短信、电话、MSN 等途径进入；
- 平台与报纸、广播、电视、SP 等其他发布渠道建立合作设想。

### Source

- **B（同期媒体采访）**：《电子商务酝酿造村冲动 客齐集挖掘千亿市场》，每日经济新闻 / 新浪，2005-09-26。  
  https://tech.sina.com.cn/i/2005-09-26/0716728515.shtml

### 已证实

```yaml
subject: Kijiji China / 客齐集
historical_period: 2005
candidate_host: shanghai.kijiji.com.cn
service_type: local classified information
historical_identity_confidence: high
verified_historical_capture: false
```

### 不知道

- 2005 首页 / 城市页实际 DOM；
- listing URL pattern；
- charset / Content-Type；
- 登录是否强制；
- 联系方式字段结构；
- listing 删除 / 过期按钮；
- 搜索排序；
- 图片上传流程；
- 是否存在 IE-only / JS compatibility 假设；
- archive 中哪些子资源仍存。

---

## 3. 2005-07：一条 Web listing 可以从 SMS 进入，而不是从 Web form 进入

2005-07-27 的同期报道描述客齐集短信业务：

```text
用户编辑 SMS
→ 发送到指定移动 / 联通号码
→ 客服中心接收
→ 客服把信息发布到对应城市的客齐集网站
```

如果短信内容不够详细：

```text
客服再打电话
→ 补充信息
→ 再形成 Web listing
```

报道还说：

- 用户支付的是普通短信费 0.1 元/条；
- 内容可以是租房、买卖物品、交友等；
- 平台会选部分信息再发布到平面报纸；
- 还计划通过便利店纸质信息卡收集内容后上传到 Web。

### Source

- **B（同期媒体，含平台业务陈述）**：《客齐集网站开通短信业务》，ChinaByte / 新浪，2005-07-27。  
  https://tech.sina.com.cn/i/2005-07-27/1628675321.shtml

### 事务模型

```text
S0 ordinary user has a phone, maybe no PC
↓
S1 compose classified message as SMS
↓
S2 telecom SMS transport
↓
S3 Kijiji customer-service ingestion
↓
S4 optional phone callback for missing fields
↓
S5 listing published to city site
↓
S6 optional syndication to print
↓
S7 buyer discovers listing
↓
S8 contact / negotiation / handoff outside the preserved page
```

### 考古意义

如果未来 archive 只剩 `S5` 的 HTML，研究者很容易错误推断：

> “这是用户通过 Web 页面填写的分类广告。”

但同期证据已经证明，**同一种 Web representation 可以有不同 input provenance**。

因此未来 evidence schema 对分类信息案例至少应考虑：

```yaml
content_ingestion_channel:
  - web-form
  - sms
  - phone-assisted
  - staff-digitized
  - paper-card
  - unknown
```

这是比再添加一个 “HTML != transaction” 更具体的方法改进。

---

## 4. 2005-07：甚至墙面小广告也可能被人工“迁移”进 Web

客齐集 2005 年北京“疏引合法小广告”行动的同期报道说，志愿者会：

1. 清理街头小广告；
2. 把合法广告的内容与联系方式登记下来；
3. 用手机信息告诉广告发布者怎样使用客齐集网站。

### Source

- **B（同期科技媒体）**：《客齐集北京疏引合法小广告》，新浪科技，2005-07-18。  
  https://tech.sina.com.cn/i/2005-07-18/0954665503.shtml

### 这不是一个小细节

它意味着历史分类 Web 的内容来源可能是：

```text
physical wall
→ volunteer transcription
→ database
→ website
```

因此一个 archive capture 的文本可以是原始内容的**第二次表示**，而不是用户最初发布动作的原件。

未来若恢复 listing，要区分：

- `original expression`：墙面纸张 / SMS / 电话；
- `platform representation`：网站记录；
- `archive representation`：Wayback / WARC 保存的网页。

三者不能自动当成一个对象。

---

## 5. 2005 的“同城”不是宣传词：分类信息故意把市场半径压回附近

2005-09-26 的采访中，客齐集负责人强调“小社区”“村庄”，甚至设想只向同一个居住小区发送分类广告，提高命中率并降低交易成本。

同期文章明确把它与淘宝/eBay式交易区分开，并提到专业手机论坛本来就存在活跃二手交易。

### Source

- **B**：https://tech.sina.com.cn/i/2005-09-26/0716728515.shtml

### 方法意义

不要默认：

```text
Internet adoption
=
national market radius
```

分类 Web 也可以主动把 Internet 的可搜索能力用于**强化本地匹配**：

```text
Internet-scale discovery technology
+
city / neighborhood filtering
+
face-to-face or cheap local handoff
```

对廉价、笨重、需要现场检查的二手物，这可能比跨省物流更合理。

---

## 6. Subject B：58 同城 2005–2006——“个人免费发布”可以确认，历史页面形态仍未确认

2006-02 的同期报道把 58 同城写成 2005 年上线、提供二手商品买卖、交友、招聘等分类信息，对个人用户免费，信息由用户发布。

2006-10 的同期行业文章又列出其主要分类：

- 房屋租售；
- 兼职；
- 家政；
- 跳蚤市场；
- 交友征婚等。

### Sources

- **B（同期科技新闻）**：《58分类信息网获软银亚洲500万美元风险投资》，2006-02-12。  
  https://tech.sina.com.cn/i/2006-02-12/1519838495.shtml
- **B（同期行业报道）**：《58同城：做大分类信息的价值》，2006-10-20。  
  https://news.ouc.edu.cn/2006/1020/c425a102064/page.htm
- **B（同期产品新闻）**：《58同城分类推出新版 实现分类信息互动化》，2005-12-20。  
  https://tech.sina.com.cn/roll/2005-12-20/1121797097.shtml

### 可确认

```yaml
platform: 58.com
period: 2005-2006
individual_posting: exists
used_goods_category: exists
local_classified_structure: exists
free_personal_posting: contemporaneously_reported
```

### 不能确认

- 2005/2006 首页 layout；
- “一步发布”具体 fields；
- 账号是否必需、cookie/session 结构；
- 城市 host pattern 的当时完整集合；
- listing detail page DOM；
- 联系方式暴露策略；
- 删除 / 修改 / 标记成交逻辑；
- 真实发布量和转化率。

当前 `58.com` 仍是运营中的现代站点，**今天的页面不能充当 2005/2006 capture**。

---

## 7. Subject C：2009 中国地质大学“坏坏宝宝”跳蚤网站——小范围 Web 可以故意不做支付和物流

《长江商报》2009-05-17 的同期报道由中国地质大学新闻网保存，记录了一名在校生为本校二手交易自建网站。

报道里的操作结构非常完整：

```text
校园已有：墙面求购/甩卖广告 + 地摊
↓
学生买域名，建本校跳蚤网站
↓
卖家发布闲置商品
↓
可以卖家自己交易；也可以委托网站代卖
↓
网站靠寝室楼纸广告 + QQ 签名 + 好友群推广
↓
买家在网页发现
↓
校内完成交易
```

网站作者特别说，因为在一个学校内交易：

- 不需要支付宝；
- 不需要快递；
- 不需要邮费。

### Source

- **B（同期媒体采访，由大学新闻网保存）**：《大二学生“淘宝”高校二手市场》，2009-05-17。  
  https://voice.cug.edu.cn/info/1006/7890.htm

### 重要修正

这直接反驳一种容易后见化的复原思路：

> “早期二手网站功能不完整，因为没有在线支付/物流，所以只是未成熟电商。”

在这个校园对象里，**不做支付和物流恰好是设计优势**，因为物理距离已经被校园范围压到足够小。

未来如果能找到该站 capture，应该把它作为：

**Web discovery + local handoff system**

而不是拿今天 marketplace 的支付/物流清单评判“缺功能”。

### Archive gap

同期报道只说学生花 300 元购买了一个域名，但报道正文没有提供足以可靠确认的 historical hostname。本轮不猜域名、不把搜索引擎中的同名站点硬连过去。

因此：

```yaml
historical_site_identity: partial
operator_identity: contemporaneously_reported
site_name: 坏坏宝宝（报道用名）
exact_original_url: unknown
verified_capture: false
```

---

## 8. Subject D：南京大学 2010——BBS 是线下跳蚤市场的 administrative dependency

南京大学保卫处当前官网保存的 2010 同期通告写明：毕业生跳蚤市场在固定时间、固定地点开放；卖家必须先填写审批表，写身份、摆摊时间地点和拟售物品，再由院系和保卫处审批登记。

最值得 OWA 注意的一句是：

> 审批表可在小百合 BBS 下载。

### Source

- **A-/B+（当前大学官方站保存的同期正式通告）**：《关于规范2010年度“毕业生跳蚤市场”活动的通告》。  
  https://bwc.nju.edu.cn/1b/1c/c577a6940/page.htm

### 依赖链

```text
Xiaobaihe BBS / web resource
→ download approval form
→ fill identity + time + place + goods scope
→ department/security approval
→ receive registration proof
→ enter physical flea market
→ face-to-face transaction
```

如果未来只研究 BBS 页面内容而不看线下通告，就会漏掉它作为**现实制度入口**的功能。

反过来，只研究校园跳蚤市场也会漏掉“下载表格”已经被数字化。

这是一种非常典型的：

**online document dependency + offline state transition**。

---

## 9. 分类信息的核心保存问题不是“页面有没有”，而是“这条信息在什么时候仍然有效”

一条二手 listing 通常存在时间敏感状态：

```text
DRAFT
→ PUBLISHED
→ AVAILABLE
→ CONTACTED / NEGOTIATING
→ RESERVED ?
→ SOLD / GIVEN AWAY
→ REMOVED / EXPIRED
```

2005 客齐集、2006 58、2009 校园网站的同期材料都能证明 **PUBLISHED / discoverable** 这类状态存在，但目前不能恢复：

- 谁联系过；
- 是否议价；
- 实际成交价；
- 何时卖掉；
- 卖家是否主动删除；
- listing 是否自动过期；
- 是否因为手机号失效而“形式上存在、实际已死”；
- 是否在线下先成交、网页后来才消失。

因此 archive 即便保存一条广告正文，也只能说明：

> **该 representation 在某个 capture 时点可被保存。**

不能自动说明：

> **该商品在那个时点仍可购买。**

本轮不另造一个新的 `state-loss` 名词；统一记入 **listing lifecycle evidence gap**。

---

## 10. 联系方式是最容易“保存成功但研究伦理失败”的字段

2005 客齐集“疏引小广告”报道明确说，志愿者记录了广告**内容和联系方法**；早期分类信息的实际成交又高度依赖电话、短信、QQ 等外部通道。

因此未来如果真的找到 2005–2010 listing capture，可能会遇到：

- 手机号；
- 固话；
- QQ；
- email；
- 住址 / 小区；
- 姓名。

这些字段对理解历史 transaction chain 很重要，但对研究仓库而言不意味着应该原样重新发布。

### 本仓隐私处理规则

遵循 `docs/METHOD.md`：

```text
需要证明“有 phone contact field”
!=
需要把一个普通人的历史手机号提交到 GitHub
```

未来 evidence 建议：

```yaml
contact_field_present: true
contact_type: phone
contact_value_republished: false
privacy_reason: ordinary-person historical contact coordinate
```

如果旧号码今天已转分配给另一人，原样公开反而会把历史证据风险转嫁给完全无关的现代用户。

---

## 11. `cross-channel publication` 会制造 provenance ambiguity

假设未来拿到一个 2005 客齐集 listing：

```text
title: 出售二手自行车
body: ...
contact: ...
```

仅凭 HTML 不能知道它是：

1. 用户自己用 browser 发布；
2. 用户发 SMS，客服录入；
3. 用户在便利店写纸卡，工作人员录入；
4. 志愿者从街头小广告人工转录；
5. 平台从合作媒体同步。

因此分类信息的 provenance 至少应分：

```yaml
representation_source: web-page
content_origin: unknown
platform_ingestion_method: unknown
archive_source: ...
```

不要让“archive 保存的是 Web”偷偷变成“历史用户原来就是在 Web 上操作”。

---

## 12. 当前仍在线的同期媒体页也是旧网 artifact，但不是目标平台 capture

本轮大量证据来自 2005–2006 新浪科技等页面。这些页面今天仍可以直接打开，并保留：

- 历史文章日期；
- 当时 URL / host 文本；
- 当时平台功能描述；
- 相关链接结构；
- 2005 新浪门户的部分 legacy page shell。

它们对 OWA 很有价值，但研究单位必须写清：

```text
artifact = current live legacy representation of contemporaneous media article
subject described = Kijiji / 58
```

而不是：

```text
artifact = Kijiji / 58 historical platform capture
```

**第三方同时代网页可以证明历史对象的功能和 URL，不等于已经取得目标站自己的 HTML。**

---

## 13. 本轮 historical locator / access probe

### Kijiji

已从同期材料取得：

```text
www.kijiji.com.cn
shanghai.kijiji.com.cn
```

本轮从 2005 新浪文章继续点击 `www.kijiji.com.cn` 时，请求超时，未取得可解释的现站正文。

同时尝试寻找可实际打开并核验的 Wayback locator，但本轮没有取得满足以下最低字段的 capture：

- capture URL；
- original URL；
- capture datetime；
- replay HTTP state；
- redirect / error / robots 判定；
- DOM / Content-Type / charset；
- subresource state。

所以只能写：

```text
historical locator candidates: achieved
verified historical memento: NOT achieved
```

不能写：

> Wayback 没保存 Kijiji。

“本轮没有拿到”不等于“档案里不存在”。

### 58

已确认 historical host `58.com` 和 2005–2006 contemporaneous service descriptions；当前 `58.com` 是现代生产站。

本轮没有取得 2005/2006 两个已核验 historical memento，因此：

```text
current live site: exists
historical identity: achieved
verified 2005/2006 capture: NOT achieved
```

### Campus flea site

“坏坏宝宝”报道没有给出可可靠定位的 exact URL；不做名称猜测。

---

## 14. 海外对照：电子分类 / 二手匹配远早于大众 Web

为了避免把 2005 中国分类信息写成“Web2.0 突然发明个人二手发布”，本轮检查了美国更早的对象。

### 14.1 Boston Computer Exchange：1980s 已经是 electronic discovery + offline completion

1985 TIME 已经记录普通 PCjr 用户联系 Boston Computer Exchange 挂售因停产而迅速贬值的电脑。

1990 Washington Post 则明确告诉读者：可以拨号进入本地/全国 BBS，在 CompuServe、MCI Mail、Delphi 上接触 Boston Computer Exchange 的二手设备 listing；其后仍需要经纪撮合、电话/物流等现实环节。

1991 Inc. 描述交易所：买卖双方报价，由 broker 匹配；买方资金进 escrow，卖方发货，买方验证机器状态后才放款。

### Sources

- **B（1985 同期新闻）**：TIME, “Computers: A Generation of Orphans”.  
  https://time.com/archive/6710310/computers-a-generation-of-orphans/
- **B（1990 同期消费技术报道）**：Washington Post, “Used-equipment market is haphazard, but bargains can be found”.  
  https://www.washingtonpost.com/archive/business/1990/09/24/used-equipment-market-is-haphazard-but-bargains-can-be-found/3749531f-bfe4-4144-a4e1-7e7566a244c4/
- **B（1991 同期商业报道）**：Inc., “The Used-Computer Market”.  
  https://www.inc.com/magazine/19910501/4613.html

### 14.2 Craigslist：email posting 自动进入 Web，再次说明“Web content origin != Web form”

Craigslist 的第一方历史说明称，1995 年最初是旧金山事件 email list，后来人们开始贴工作、出售物品、公寓等，Craig Newmark 编写软件把 email postings 自动加到网站。

2004 BusinessWeek 同期采访中，CEO Jim Buckmaster 回忆自己 1990s 末通过 list 卖 futon、找公寓、贴简历。

### Sources

- **C/B（平台后来的历史说明）**：https://www.craigslist.org/about/mission_and_history
- **B（2004 BusinessWeek 采访，由 Craigslist 保存）**：https://www.craigslist.org/about/press/craigslist.keeper

### 对中国材料的帮助

这说明中国 2005 的 SMS→Web 并不是某种孤立“土办法”。分类信息系统长期存在一种结构：

```text
non-Web input
→ structured / searchable electronic representation
→ contact
→ offline completion
```

中国比较有特色的是当时同时叠加：

- SMS 大众化；
- 网民仍未覆盖所有普通消费者；
- 墙面小广告、报纸、便利店卡片仍活跃；
- 同城平台主动把这些媒介桥到 Web 上。

---

## 15. 对浏览器复原的假设

如果以后取得 2005–2010 capture，M3 不应只看“页面视觉是否像当年”。需要至少检查：

1. **charset**：GB2312 / GBK / UTF-8？
2. **表单**：发布流程是否依赖旧 JS / popup / iframe？
3. **城市切换**：host/subdomain、cookie 还是 query 参数？
4. **contact field**：明文写在 DOM、图片化、登录后显示，还是 JS 注入？
5. **时间语义**：发布时间、更新时间、有效期是否存在？
6. **图片**：主文档与用户上传图是否分别保存？
7. **登录**：cookie/session 失效以后 archive 是否只回登录页？
8. **搜索**：结果是否 server-side dynamic，archive 只能保孤立 detail pages？
9. **SMS/电话 ingestion**：Web UI 即使完全 replay，也不能复原这些外部输入通道。

目前没有历史 capture，不先猜 IE6 必需性。

---

## 16. 已证实 / 高概率 / 不知道

### 已证实

- 2005 客齐集存在 `www.kijiji.com.cn` / `shanghai.kijiji.com.cn` historical locators；
- 2005 客齐集明确存在 SMS→客服→对应城市 Web listing 的发布路径；
- 墙面合法小广告的内容和联系方式曾被人工登记并导向 Web；
- 平台曾同时设想/使用短信、电话、MSN、便利店卡片、报纸等跨媒介路径；
- 2005–2006 58 同城存在个人免费发布、本地分类和二手商品/跳蚤市场类别；
- 2009 中国地质大学有一个针对校内二手交易的学生自建网站，且明确不依赖支付宝/快递；
- 2010 南京大学毕业跳蚤市场审批表可从小百合 BBS 下载，实际审批与交易在线下完成。

### 高概率但尚未核验到目标 artifact

- 早期分类 listing detail page 很可能暴露某种电话/IM 联系字段；同期材料支持“联系方式”是核心，但字段结构未知；
- 城市/社区分层很可能体现在 URL、站点切换或数据库查询中，但具体 pattern 需 capture；
- 已成交 listing 可能被删除或过期，导致 archive 对“活市场”产生系统性偏差，但具体策略未知。

### 不知道

- 客齐集 2005 首页/发布页的 DOM 和 charset；
- 58 2005/2006 “一步发布”的字段；
- 两个平台是否有明确“已售”状态；
- 用户上传图片实际保存率；
- listing 生命周期；
- 搜索结果的 archive 保存偏差；
- 历史手机号/QQ 显示策略；
- “坏坏宝宝”精确 historical URL；
- 本轮 candidate locators 在 Internet Archive / Common Crawl 中是否存在可用的多个时点。

---

## 17. Evidence table

| Claim | Evidence | Grade | Confidence | Caveat |
|---|---|---:|---:|---|
| 客齐集 2005 存在同城分类业务 | 2005-09 同期采访 | B | high | 未取得平台 historical capture |
| SMS 可直接进入 Web listing | 2005-07 同期业务报道 | B | high | 业务规模主要来自平台陈述 |
| 小广告被人工登记并导入网络 | 2005-07 同期活动报道 | B | high | 不知导入多少条、保存多久 |
| 58 有个人免费发布和二手分类 | 2005–06 同期媒体 | B | high | 当前 58 页面不能代替旧页面 |
| 校园 Web 二手站不需要支付宝/快递 | 2009 同期学生采访 | B | high | 单校案例，不外推全国 |
| 小百合 BBS 提供线下市场审批表 | 2010 南大正式通告 | A-/B+ | high | 当前官方 legacy representation，不是 2010 memento |
| Kijiji / 58 historical DOM/charset | — | — | unknown | 需要 verified memento |
| listing sold/removed lifecycle | — | — | unknown | 静态媒体报道无法恢复 |

---

## 18. 后见之明风险

### 风险 A：把分类网站写成“不成熟淘宝”

分类信息的目标可以只是 local matching；没有支付、物流不一定是缺陷。

### 风险 B：看到 Web HTML，就默认历史用户通过 Web 输入

2005 客齐集已经直接否定这个假设。

### 风险 C：把现在仍在线的新浪 2005 文章当成 Kijiji capture

它只是**描述 Kijiji 的同期媒体 artifact**。

### 风险 D：为了“复原真实”而重新公开普通人的历史联系方式

这违反本仓隐私最小化原则，而且旧手机号今天可能已经属于另一个人。

### 风险 E：把 archive 中仍存在的 listing 当作当时仍 available

分类信息的有效期高度短暂。archive capture time 与商品可售状态不能自动等同。

---

## 19. M1 判断

这一组对象目前对 M1 的贡献是：

```text
historical identity: achieved for Kijiji / 58
contemporaneous operation evidence: achieved
cross-channel ingestion evidence: achieved
ordinary-use / campus hybrid evidence: achieved
privacy risk identified: achieved
verified historical platform capture: NOT achieved
second verified historical timepoint: NOT achieved
browser / charset verification: NOT achieved
```

所以：

**`M1 classified/community case: NOT ACHIEVED`**。

并且严格说，分类信息平台本身也不一定是 ROADMAP 中最优先的“论坛/BBS/社区”完整案例，因此本轮保持 research note，不把它强塞进三类 M1 之一。

---

## 20. 下一步高价值动作

1. 围绕 `shanghai.kijiji.com.cn`、`www.kijiji.com.cn` 做克制的 Internet Archive / Common Crawl candidate survey；
2. 对 `58.com` 2005–2007 首页、发布页、二手 detail page 找 ≥2 个实际可打开 capture；
3. 如果 capture 含普通个人联系方式，只记录字段存在性和结构，不提交原值；
4. 寻找客齐集 SMS 服务的帮助页/资费页/运营商文档，区分媒体宣传与真正执行流程；
5. 寻找“小百合 BBS 2010 跳蚤市场审批表”历史页面/附件 capture，验证 Web/BBS→线下审批依赖；
6. 寻找 2005–2010 分类 listing 的修改、删除、过期帮助文档，恢复生命周期，而不是只收首页截图；
7. 如果能取得一个 listing detail capture，M3 应比较 modern Chromium 与 IE6 级环境中的编码、表单、脚本和联系字段显示差异。

---

## 21. 本轮最重要的方法结论

分类信息让我们看到一个很容易被 Web archive 误导的事实：

> **网页上的内容，不一定是从网页里出生的。**

一张 2005 年的 listing，可能先是一张贴在墙上的纸，也可能先是一条短信；有人把它录入数据库，它才获得 URL。后来 Web archive 如果只保存 URL，就保存了这条信息的**最后一种公开表示**，却没有自动保存它最初来自哪里，也没有保存它最后是通过电话、见面还是赠送结束。

因此旧网考古不只要问：

**“这页还在不在？”**

还要问：

**“这页在整个生活动作里，到底处在第几步？”**

---

*研究说明：本 research note 由 AI 辅助初稿整理。当前没有将 current live page、媒体 legacy page 或 archive locator 冒充 historical memento；没有重新公开任何普通人的历史联系字段。*