# Hi-Fi 音响论坛、评测、DIY、二手与试听：从网页讨论到真实听音的状态缺口（2001—2015）

> Scope：只研究约 2001—2015 年中文 Web 中，音响 / 耳机 / PC Hi-Fi 社区怎样表示器材、听感、DIY、二手交易、试听和用户声望，以及这些页面状态与真实拥有、真实成交、真实听音之间的缺口。
>
> 不把本文件扩成 1990s 中国音响产业史，也不把美国/欧洲 Hi-Fi 前史写进本仓；那些进入 `tmzncty/how-people-lived/topics/audiophile-hifi-hobby-life-world-china-1980s-2026.zh-CN.md`。

本题不是“老烧论坛怀旧”。它要回答的是：今天看到一个 2003 年日期的器材帖、一个“已出”二手帖、几十页回复或一个用户器材签名，究竟能证明历史用户真实生活到哪一步？

---

## 1. 研究单位：论坛页面不是听音现场

至少区分：

- platform / forum brand；
- host / domain；
- board / subforum；
- thread；
- post / reply；
- user account；
- avatar / signature / rank；
- attachment / inline image / external image；
- quoted text；
- product page / review；
- DIY schematic / measurement / BOM；
- classified / secondhand listing；
- intermediary / escrow state；
- PM / QQ / phone handoff；
- offline audition；
- physical ownership；
- physical transaction；
- real repair / modification outcome；
- current live legacy page；
- historical archive capture。

最小状态机：

```text
用户听说某器材
→ 找到论坛/音频站
→ 浏览版块/搜索
→ 打开帖子/评测
→ 看到参数、图片、他人听感
→ 发问 / 回复 / 私信
→ 可能去店里 / 烧友家试听
→ 决定借、买、DIY 或放弃
→ 交易/制作真实发生
→ 器材进入现实系统
→ 摆位 / 搭配 / 调试 / 使用
→ 再回 Web 写听感、照片或测量
→ 升级 / 二手转卖 / 长期持有
```

固定边界：

```text
thread exists ≠ author owned device
review exists ≠ reviewer used retail sample long-term
reply count ≠ distinct listeners
view count ≠ owners
signature gear list ≠ current verified inventory
classified posted ≠ item available
“已出” ≠ transaction fully verified
PM / QQ handoff ≠ archive-visible transaction
forum recommendation ≠ user followed it
DIY schematic downloaded ≠ device built
build photo ≠ long-term successful operation
offline audition announced ≠ event occurred
current live old post ≠ verified historical capture
```

---

## 2. 为什么 Hi-Fi 论坛特别适合做 old-Web state-gap 研究

多数旧论坛研究停在：

```text
发帖 → 回复
```

Hi-Fi 把网页状态至少接到四种现实状态：

```text
讨论
→ 真实听音

讨论
→ 真实购买 / 二手交易

讨论
→ 真实 DIY / 改机

讨论
→ 线下试听 / 家访 / 聚会
```

因此 HTML 即使完整，也最多证明“平台怎样表示和讨论器材”，不能自己证明声音、拥有、成交或线下共同在场。

本题增加四个必须单独验证的状态：

- **ownership state / 拥有状态**；
- **listening state / 实际试听状态**；
- **build state / 制作与改机状态**；
- **transaction state / 二手成交状态**。

---

## 3. 2003 HIFI168 live legacy page：历史内容仍在线，但不是 2003 capture

当前非常发烧网仍可访问一个 URL：

```text
https://mail.hifi168.com/bbs/showtopic-40621.aspx
```

页面承载题为“关于 BOSE 的一些自己的看法”的帖子，页面显示首帖日期 **2003-11-23**。正文中，用户回忆约十年前在广州实体商店听过 BOSE，并提到近期去广州音响商圈试听 LINN；当前页面还展示用户名、账号等级、注册时间、帖子/积分等字段。

当前 live legacy page：

- <https://mail.hifi168.com/bbs/showtopic-40621.aspx>

### 证据等级

本对象应标记为：

**A/B-like platform-retained historical content, but not a verified 2003 memento**。

更精确地说，它可以支持：

- 当前 host 上存在一页承载 2003 日期的旧帖；
- 当前 legacy renderer 展示若干用户字段；
- 旧帖正文确实把线下试听、品牌经验与在线讨论连接起来。

它不能支持：

- 2003 年当天页面就是当前 DOM；
- 当时 host 就是 `mail.hifi168.com`；
- 当时论坛软件/版本就是当前显示的 `Discuz!NT`；
- 当前积分、帖子数、注册资料是 2003 时点值；
- 当前分页、字体、头像、签名、广告和链接结构与历史一致；
- 原图和附件今天仍完整；
- 作者当时真的拥有正文所谈每件器材。

因此固定：

```text
historical-looking live page
≠
verified historical Web representation
```

---

## 4. 长寿论坛会制造“连续性幻觉”

Hi-Fi 社区常有 20 年级别用户账号和帖子，这对生活史极有价值，但也危险。

当前页面可能把不同年份状态叠在一起：

```text
2003 帖子正文
+ 2020s 用户总帖数
+ 后来升级的论坛 rank
+ 后来迁移的模板
+ 当前广告 / 导航
```

如果研究者截图整页再标“2003 年论坛长这样”，就会把多个时间层压成一个假时点。

因此以后针对长寿论坛必须单独记录：

- post timestamp；
- account registration timestamp；
- 当前渲染时间；
- 当前 host；
- forum software 当前标识；
- 是否能找到历史 memento；
- 哪些用户字段可能是 mutable current state。

可称为 **legacy-rendering temporal collapse / 遗留渲染的时间塌缩**。

---

## 5. 2002 起的耳机大家坛：专业小众社区会成为市场与知识基础设施

Apple App Store 当前“耳机大家坛”应用介绍称论坛成立于 **2002 年**，讨论耳机、耳塞、便携播放器、耳放、电脑音频、桌面音箱和数字音频等；2016 年同期报道同样称其 2002 年成立，并指出当时已有二手交易区和中介区。

来源：

- App Store 当前开发者介绍：<https://apps.apple.com/us/app/%E8%80%B3%E6%9C%BA%E5%A4%A7%E5%AE%B6%E5%9D%9Bapp/id1446828090>
- 2016 同期媒体报道：<https://news.sina.com.cn/o/2016-07-11/doc-ifxtwitr1944012.shtml>

证据等级：

- 成立年份：**B/C，需要继续以早期 capture / WHOIS / 同期引用核验**；
- 2016 的版块和移动端迁移：**B（同期报道）**。

这说明音频论坛不仅是内容社区，还可能同时承担：

```text
器材知识
+ 用户声望
+ 二手供给
+ 交易信用 / 中介
+ 线下试听联系
```

也因此 archive 只保住公开帖子时，会丢失真正完成交易的 PM、电话、转账和物流。

---

## 6. 2004：PC Hi-Fi 让网站、评测和爱好者产品开发混在一起

2004 年中关村在线转载 Soomal 的声卡盘点，将 DiyEden 描述为“音频发烧友组织”，并介绍其 USB DAC、真空管声卡/耳放；同年多篇拆解、评测直接链接/转述 DiyEden 与 Soomal 的技术资料。

同期来源：

- <https://sound.zol.com.cn/2004/1224/138651.shtml>
- <https://diy.zol.com.cn/2004/0921/121348.shtml>
- <https://diy.zol.com.cn/2004/0914/119950.shtml>

这构成一种 old-Web 特有的身份重叠：

```text
爱好者组织
→ 产品开发者
→ 专业网站评测对象
→ 论坛讨论对象
→ 后来商业品牌
```

所以研究“发烧友帖子”时不能默认所有参与者只是消费者。

必须标记可能身份：

- consumer；
- reviewer；
- moderator；
- dealer；
- manufacturer / engineer；
- DIY organizer；
- reseller；
- unknown。

这可称为 **participant-role ambiguity / 参与者角色歧义**。

---

## 7. 技术帖子比普通聊天更容易产生“附件坟场”

音频 DIY 常依赖：

- 电路图；
- PCB 图；
- 元件表；
- 测量截图；
- 拆机照片；
- 固件/驱动；
- 外链图片；
- 压缩附件。

因此一个正文仍完整的旧帖可能已经失去真正最关键的证据。

状态应拆成：

```text
thread HTML preserved
→ inline image preserved?
→ external image host alive?
→ attachment metadata visible?
→ attachment bytes accessible?
→ login required?
→ file type still readable?
→ schematic version identifiable?
```

不能从“帖子还在”直接写“DIY 方案已保存”。

增加 **technical-attachment survival gap / 技术附件存活缺口**。

---

## 8. “听感帖”有一种特殊的 provenance 问题

一条器材听感可能来自：

1. 自己长期拥有；
2. 店铺试听十分钟；
3. 去烧友家听；
4. 展会试听；
5. 厂商送测；
6. 借机；
7. 转述别人的判断；
8. 仅根据参数/品牌发表评论。

这些状态对历史解释差别极大。

因此若帖子正文没有明确说明，不要给作者补上“拥有者”身份。

推荐抽取字段：

```yaml
claimed_listening_context:
  value: owner / dealer_demo / friend_home / show / loaner / unknown
  evidence: explicit_text / inference
claimed_duration:
  value: ...
  confidence: ...
ownership_claim:
  value: yes / no / unclear
```

这能防止把论坛文本自动转成“用户拥有数据库”。

---

## 9. 二手版块：listing state 与成交 state 必须分开

Hi-Fi 器材价格高、升级频繁、型号寿命长，因此二手流通对 hobby executability 很重要。

但 old-Web 页面常最多留下：

```text
标题：出某器材
价格
成色
地点
联系方式
照片
回复
```

现实状态却至少有：

```text
想出售
→ listing published
→ potential buyer sees
→ asks question
→ PM / QQ / phone
→ price negotiation
→ payment / intermediary
→ shipment / face-to-face handoff
→ buyer inspects
→ accepted / dispute / return
→ seller marks “已出”（可选）
```

因此：

```text
“已出”文本
```

也只能证明页面/作者后来如此表示，不一定证明支付、物流和验收链每一步都可独立核验。

若论坛提供中介/担保版，应继续区分：

- request submitted；
- intermediary accepted；
- funds held；
- shipment；
- release；
- dispute；
- final closure。

---

## 10. Forum reputation 可能成为一种 hobby credential，但不是现实身份认证

老论坛常显示：

- 注册时间；
- 发帖数；
- 积分；
- 头衔；
- 精华；
- 版主身份；
- 交易评价。

这些字段可以降低陌生人交流和交易的不确定性，但不能自动解释为：

```text
高积分 = 技术正确
老账号 = 真人身份已认证
版主 = 无商业利益
发帖多 = 器材经验多
```

更准确的说法是：论坛产生了 **platform-native hobby reputation / 平台原生兴趣声望**。

这种声望高度依赖平台连续性。一旦论坛关闭、数据库损坏或账号迁移失败，十几年累积的“老烧是谁”可能瞬间失去可读性。

---

## 11. 论坛搜索是 hobby memory 的关键基础设施

音响器材生命周期往往远长于手机 App：一台 1990s 功放、2000s CD 机到 2020s 仍可能流通。

因此老帖的价值会反复回来：

```text
十年前的拆机图
旧型号故障
停产元件替代
搭配经验
二手参考
```

这意味着论坛 search/index 本身也是历史对象。

要区分：

- URL 仍存在；
- Google/Baidu 可搜到；
- 论坛内部索引可搜到；
- 登录后才可搜索；
- 索引重建后早期帖子丢失；
- 搜索只返回标题不返回旧正文。

一个论坛“在线”并不等于其过去仍然 **queryable / 可查询**。

---

## 12. 从论坛到现实试听：co-presence gap 再次出现

Hi-Fi 圈常见：

```text
论坛讨论
→ “来我家听” / 店铺试听 / 展会 / 同城活动
→ 私信或电话确定地点
→ 现实共同在场
```

网页可见的邀请无法证明：

- 对方真实到场；
- 当天器材配置与帖中一致；
- 试听持续多久；
- 音响店是否临时换机；
- 线下意见与回帖是否一致。

因此本题与 `INTEREST_GROUP_EVENT_PAGES_OFFLINE_MEETUPS_AND_COPRESENCE_STATE_GAPS_2005_2015.md` 相连，但更强调器材与试听 provenance。

---

## 13. 2008—2015：Web 音频媒体与论坛的边界变得越来越模糊

同期科技媒体已经大量使用：

- 产品数据库；
- 评论；
- 论坛链接；
- 用户点击/查询排名；
- 拆机文章；
- 转载专业小站文章。

例如 2004 ZOL 的多媒体音箱文章直接讨论网站数据库查询排名和器材文章点击；同年的 Soomal 文章又通过 ZOL 等大站转载传播。

来源：

- <https://sound.zol.com.cn/2004/1224/138662.shtml>
- <https://sound.zol.com.cn/2004/1201/133505.shtml>

因此 historical page type 不能只分“媒体 / 论坛”二元：

```text
editorial review
community comment
forum thread
product database
manufacturer material
syndicated repost
```

同一段文字可能在多个 host 重复出现，不能把多个转载 URL 当多个独立 evidence family。

---

## 14. 论坛迁移动端以后，公开可保存知识可能变薄

2016 年报道耳机大家坛重新制作移动客户端，原因之一是旧客户端在论坛升级后无法同步。

来源：<https://news.sina.com.cn/o/2016-07-11/doc-ifxtwitr1944012.shtml>

虽然 2016 超出本题主时段一点，但它是理解 2002—2015 遗产的重要边界：

```text
论坛数据库
→ 论坛升级
→ 客户端兼容失效
→ 新移动入口
```

如果同一群体后来转向：

- App；
- 微信群；
- 私域群；
- 视频平台评论；

那么 2000s 公开长帖时代可能比后来的 hobby 生活更容易被公开 archive 保存。

不要因此误判：

```text
old Web 资料多
→ 当时讨论一定比后来更多
```

这可能只是 **public-archive visibility shift / 公开档案可见度迁移**。

---

## 15. 一个可复用的 Hi-Fi forum state model

```text
[discovery]
search engine / bookmark / link
→ forum landing
→ board
→ thread list
→ thread

[reading]
text
+ quoted posts
+ images
+ attachments
+ signature
+ product links

[participation]
register/login
→ reply / new thread
→ PM
→ reputation / rank

[hobby execution]
research product
→ audition / borrow / buy / build
→ install / pair / tune
→ long-term use

[secondary market]
classified
→ contact
→ negotiation
→ payment/intermediary
→ delivery
→ acceptance/dispute

[return to web]
listening impression
→ measurement / photo / DIY log
→ later search and citation

[archive]
page captured?
→ images?
→ attachments?
→ user mutable fields?
→ search index?
→ private handoff invisible
```

---

## 16. 主要 archive bias

### 16.1 public-thread / private-transaction asymmetry

公开讨论容易保存，PM、QQ、电话、转账和收货最难保存。

### 16.2 expert-survival bias

精华帖、版主帖、经典长文最容易被引用和迁移，普通失败经验容易沉没。

### 16.3 owner-attribution bias

研究者容易把写过器材的人自动当拥有者。

### 16.4 mutable-profile bias

旧帖旁边展示的是今天累计后的账号资料，而不是帖子当日状态。

### 16.5 attachment mortality

正文仍活着，技术图和照片可能已经死掉。

### 16.6 commercial-role opacity

商家、厂商、媒体、普通用户可能使用相似论坛身份，历史页面未必充分披露利益关系。

### 16.7 successful-upgrade bias

“终于升级成功”的帖子比买错、退货、坏机、不了了之更容易被记住。

---

## 17. M1 archive status — 本轮仍未达到

本轮已确定的 historical locator / candidate object 包括：

```text
hifi168.com / HIFI168 / 非常发烧论坛
mail.hifi168.com/bbs/showtopic-40621.aspx
erji.net / 耳机大家坛
DiyEden / diyeden.com
Soomal early audio pages
```

并实际尝试追 HIFI168 与 `erji.net` 的早期 Wayback locator，但本轮没有取得一份能够实际检查以下内容的 **2001—2005 verified memento**：

- response body；
- HTTP headers；
- capture datetime；
- original host/URL；
- DOM；
- charset；
- forum software/version；
- images/attachments；
- form action；
- cookie/session；
- search behavior。

因此：

**M1 = NOT ACHIEVED**。

正确结论是：

> 本轮已有 live legacy historical content 与同期媒体证据，但仍没有验证足以重建早期论坛页面/transaction 的 archive capture。

不能写成：

> Wayback 没有 HIFI168 / erji.net。

---

## 18. 已证实 / 高概率 / 不知道

### 已证实

- 当前 HIFI168 host 有承载 2003 日期内容的 legacy thread；
- 当前页面显示帖子、用户和论坛字段，但这些字段不能自动归到 2003 时点；
- 2004 同期科技媒体已经把 PC Hi-Fi、DiyEden、USB DAC/胆声卡等作为明确发烧/音频对象；
- 2002 起的耳机大家坛成立时间有当前开发者与 2016 同期报道相互支持；
- 2016 报道明确提到耳机大家坛二手交易区、中介区及移动端迁移。

### 高概率

- 2000s 中文 Hi-Fi 论坛已经是器材比较、听感、DIY 和二手流通的重要知识接口；
- 公开论坛帖子与线下试听、实体交易之间大量依赖 PM/QQ/电话等 archive 不可见 handoff；
- 论坛升级与平台迁移造成一部分历史附件、客户端和页面状态损失。

### 不知道

- HIFI168 2001—2003 原始首页/帖页的历史 DOM 与编码；
- `mail.hifi168.com` 是否对应早期同一 host 结构；
- 2002—2005 耳机大家坛具体 forum software 和版块结构；
- 早期用户等级、积分和签名字段何时加入；
- 论坛二手帖真实成交率；
- 多少 DIY 图纸/附件今天仍可取得；
- 早期论坛搜索索引是否经历重建和丢失；
- 论坛公开讨论转入 QQ 群/微信群后的知识损失量。

---

## 19. 后见之明风险

1. 不把今天的 legacy renderer 当历史截图。
2. 不把“老账号”理解成二十年持续活跃。
3. 不把论坛帖子自动转成器材拥有记录。
4. 不把“听过”理解成长时间家庭使用。
5. 不把二手“出”帖直接转成成交数据库。
6. 不把论坛热度直接转成发烧友人口规模。
7. 不用现代“客观测量 vs 玄学”争论替历史参与者统一分类；先保存他们当时怎样说。
8. 不因为 2000s 公开论坛今天保存得较多，就假定后来移动私域兴趣生活变少。

---

## 20. 下一步

1. 通过 Internet Archive / Common Crawl / 搜索引擎残存 locator 继续核验 HIFI168 2001—2005；
2. 核验 `erji.net` 2002—2005 首页、版块、用户页和二手区；
3. 找一个带图片/附件的 DIY thread 做 attachment-survival audit；
4. 找一个二手帖，追公开状态直到 PM/QQ handoff 边界，明确哪里开始不可见；
5. 比较当前 live legacy page 与 historical capture，检查 mutable user fields 和 template migration；
6. 追 DiyEden / Soomal / ZOL 之间转载链，区分 original article 与 syndicated copies；
7. 与 `how-people-lived` 的 price-to-wage / housing-space 研究交叉，但不要把生活史内容全部复制进本仓。
