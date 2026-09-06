# 集邮论坛、缺项清单、扫描图、联系方式与实物交换：从 Web 可见状态到真实邮品的状态缺口（2005—2015）

> Scope：只研究约 2005—2015 年中文 Web 中，集邮论坛/专题站怎样表示邮票、封片戳、会刊、want list、求购交换、图片附件、价格和用户身份，以及这些公开页面状态与真实联系、付款、邮寄、验收、更新收藏之间的缺口。
>
> 不把本文件扩成 1980s 中国集邮史、1997 邮市史或全球 philately 史；这些进入 `tmzncty/how-people-lived/topics/stamp-collecting-postal-artifacts-open-ended-completion-and-hybrid-exchange-china-1980-2026.zh-CN.md`。

本题不是“老集邮网站怀旧”。它要回答的是：今天看到一条 2008 年的“缺第 82、87、102 期”“出某邮品”“求交换”帖子，究竟能证明历史交易到哪一步？

---

## 1. 研究单位：论坛帖子不是邮册，也不是成交凭证

至少区分：

- platform / forum brand；
- host / domain；
- board / section；
- thread；
- post / reply；
- current account state；
- post-time account state（若可恢复）；
- image / scan / attachment；
- want list / 缺项清单；
- offer / sale / exchange listing；
- quoted catalog number / condition / price；
- PM / e-mail / phone handoff；
- bank remittance / payment；
- postal / courier shipment；
- physical inspection；
- acceptance / dispute / return；
- collection update；
- current live legacy page；
- verified historical capture。

最小状态机：

```text
收藏者发现缺项
→ 在论坛检索 / 发 want list
→ 陌生人看到帖子
→ 回复“我有” / 提供线索
→ 转 PM / e-mail / 电话
→ 确认品种、品相、价格/交换条件
→ 汇款或约面交
→ 邮政/快递寄出
→ 收件
→ 实物鉴别
→ 接受 / 争议 / 退回
→ 放入邮册 / 更新缺项
```

因此固定：

```text
thread exists ≠ matching item existed in counterparty possession
reply “有” ≠ item still available
want list ≠ transaction
listed price ≠ paid price
bank account posted ≠ remittance occurred
shipping discussion ≠ parcel delivered
scan visible ≠ physical item condition fully represented
“已出 / 已换” ≠ payment-shipping-inspection chain verified
current user rank ≠ historical user rank
current post count ≠ post-time post count
current renderer ≠ historical DOM/CSS/charset
```

---

## 2. 为什么集邮论坛特别适合 old-Web state-gap 研究

它把 Web 接到一个高度物理化的收藏系统：

```text
Web 文本 / 图片
→ 私下联系
→ 钱
→ 邮政 / 快递
→ 一张具体纸片
→ 放进一个真实邮册
```

这使至少五个现实状态必须单独验证：

- **item existence state / 实物存在状态**；
- **condition state / 品相状态**；
- **contact state / 联系状态**；
- **fulfillment state / 履约状态**；
- **collection incorporation state / 入藏状态**。

即使 HTML 保存完整，也不能自己证明邮品最后进入了谁的邮册。

---

## 3. 2008—2009 普邮网 current legacy pages：历史内容活着，但多个时间层被压在一起

本轮找到的最有价值对象是 `puu.cn` 当前仍在线的一批旧帖。

### 3.1 缺项清单

当前页面：

- <https://www.puu.cn/thread-17099-1-1.html>

页面承载标注 **2009-02-07** 的“看看谁能帮助我（1）”，正文逐项列出作者缺少的地方集邮会刊和总期号。

它可以窄地支持：

- 当前 `puu.cn` 保存了一条带 2009 日期的历史正文；
- 论坛被用于公开发布非常细粒度的集邮文献 want list；
- 缺项可以以期号/范围方式标准化表达。

它不能支持：

- 2009 页面 DOM 与今天相同；
- 当前显示的用户积分、签到等级、头像、今日心情是 2009 状态；
- 当时已有当前全部 JavaScript / CSS / 导航；
- 有回复即完成了交换；
- 没有公开回复就表示没有人私下联系。

### 3.2 技术性图片帖

当前页面：

- <https://www.puu.cn/thread-9651-1-1.html>

一个标注 **2008-03-14** 的帖子今天仍显示 `股1.jpg`、`股2.jpg`、`股3.jpg` 等图片占位/附件提示，并出现“登录后才能下载或查看”等当前界面文本。

这说明必须拆开：

```text
thread text survival
attachment metadata survival
thumbnail survival
full image bytes survival
login authorization state
historical access rule
```

不能因为当前 renderer 写着“需要登录”就断言 2008 当天访问规则完全一样。

---

## 4. legacy-rendering temporal collapse：一个 2008 帖子里能同时出现 2026 账号状态

普邮网旧帖页面今天经常显示：

- 2008/2009 的发帖日期；
- 用户当前累计积分；
- 2020s 的签到天数；
- 当前每日心情；
- 当前站点“登录/注册”提示；
- 当前版权/举报声明。

例如：

- <https://www.puu.cn/thread-11618-1-1.html>
- <https://www.puu.cn/thread-12365-1-1.html>

这些页面中的正文日期是 2008，而某些用户状态显示到 2026。

因此正式加入 **legacy-rendering temporal collapse / 遗留渲染时间塌缩**：

```text
historical post body
+
mutable current account fields
+
current template/navigation/legal notice
→ one present-day page
```

任何截图若不分层，都会把十几年状态伪装成一个历史时点。

推荐记录：

```yaml
post_timestamp: historical value shown by page
renderer_observed_at: current access date
mutable_fields:
  - user_points
  - total_posts
  - sign_in_days
  - mood
  - rank
  - avatar
current_host: www.puu.cn
historical_host_verified: false/unknown
```

---

## 5. want-list gap：公开“我缺什么”比“我最终补到了什么”更容易存活

2009 want-list 页面是一种典型 archive asymmetry。

公开 Web 容易保存：

```text
缺哪些期
想要什么
谁回复过
```

真正 outcome 往往转到：

```text
站内信
QQ
E-mail
电话
短信
银行转账
邮寄单
包裹
收件后的私下确认
```

因此增加 **want-list-to-collection gap / 缺项清单—真实入藏缺口**。

即使十年后这条帖子还在，我们也可能永远不知道其中哪些空格最终被填上。

这也是 `how-people-lived` 所说 open-ended completion horizon 在 old-Web 的可见性边界：archive 特别擅长保存“未来还缺什么”，不擅长保存那个未来后来是否发生。

---

## 6. 2008 混合联系方式：Web 只是交易的一层，不是整个交易系统

一个 2008 普邮网帖子转录内部交流资料时，同时留下：

- 纸质邮政地址；
- 电话 / 传真；
- 手机；
- E-mail；
- 银行账户；
- 截止日期。

当前页面：<https://www.puu.cn/thread-9052-1-1.html>

另一个 2008 帖子则具体讨论寄两本集邮书到辽宁的邮费，作者描述先尝试快递、后改到邮局寄件。

当前页面：<https://www.puu.cn/thread-13460-3-1.html>

这两组材料支持：

> 2000s 集邮 Web 交易/交换是明显的 **cross-channel handoff / 跨渠道交接**。

典型链可以是：

```text
论坛发现
→ e-mail / phone
→ bank remittance
→ postal / courier shipment
→ physical receipt
```

所以需要增加：

- `public-thread/private-contact gap`；
- `contact-to-payment gap`；
- `payment-to-shipment gap`；
- `shipment-to-receipt gap`；
- `receipt-to-condition-acceptance gap`。

Web archive 通常只覆盖第一段。

---

## 7. scan ≠ object：集邮论坛的图片有特殊证据边界

邮票/封片戳研究高度依赖图像，但扫描件不能完全替代实物。

一张论坛图最多可能帮助观察：

- 图案；
- 大体齿孔；
- 邮戳位置；
- 明显版式；
- 可见污损。

但它未必可靠呈现：

- 背胶；
- 纸张厚度；
- 荧光/水印；
- 修补；
- 揭薄；
- 细小齿孔损伤；
- 色差；
- 真伪鉴定所需微观特征。

因此：

```text
scan uploaded
≠ item authenticated
≠ item condition fully observed
≠ uploader physically possessed it at every later time
```

增加 **scan-to-object provenance gap / 扫描—实物来源缺口**。

若帖子附件丢失，又会出现第二层：

`discussion survives ≠ object image survives`。

---

## 8. 文献集邮使“附件/目录/索引”比普通聊天更关键

2008 普邮网可以看到：

- 地方会刊缺期；
- 文章索引；
- 民刊介绍；
- 邮史资料转录；
- 目录与刊期整理。

例如：

- <https://www.puu.cn/thread-11533-1-1.html>
- <https://www.puu.cn/thread-12365-1-1.html>

对这种社区，真正重要的 historical object 不只是帖子正文，还包括：

- 目录图片；
- PDF/Word/扫描附件；
- 引用来源；
- 被转贴文章的 original page；
- 会刊邮寄地址；
- 旧站外链。

因此增加 **bibliographic-object survival gap / 文献对象存活缺口**。

一条“赵某研究成果索引”还在线，不等于被索引文章也能在线取得；一条民刊介绍还在，不等于那份纸刊已经数字保存。

---

## 9. 2010s：签到、等级和游戏化字段会反过来污染历史账号解释

普邮网当前 2019 和 2024 的签到页显示自动签到帖、随机“邮品分”、等级和累计签到天数，例如：

- <https://www.puu.cn/thread-132155-2-1.html>
- <https://www.puu.cn/thread-137265-2-1.html>

这些页面说明平台后来增加/保留了明显的 **gamified persistence layer / 游戏化留存层**。

但当同一个账号出现在 2008 帖子里时，不能倒推：

- 2008 已经有签到系统；
- 2008 用户等级算法和今天相同；
- 当前 3000+ 天签到是一个从账号注册日起连续、不间断、历史可验证的活动序列。

这要求对跨十几年论坛账号建立：

```text
content-time fields
current mutable fields
feature-introduction time
```

三层分离。

---

## 10. 海外对照只作为 method comparator，不扩本仓 scope

1994 的 Computer Aided Philately FAQ 记录，StampLine 已把 `rec.collecting.stamps` Usenet 流量通过每日 mailrun 接入自己的商业联机服务；用户回复还能再送回 Internet。

来源：<https://www.geocities.ws/stamplink/StampsFAQ/ch06.html>

1996 `rec.collecting.stamps` 也已有公开出售旧邮册的帖子：

- <https://groups.google.com/g/rec.collecting.stamps/c/xQJTfGKhxIg>

这里只用来确认一个跨国共同机制：

> collector community 很早就会把**公开文本发现**与**离线实物履约**叠在一起。

全球 philately 网络史写入 `how-people-lived`，本仓不向 1990s 海外扩张。

---

## 11. 本题新增的 old-Web state gaps

固定以下术语，供以后收藏类论坛复用：

1. **want-list-to-collection gap**：发缺项 ≠ 最终补齐；
2. **public-thread/private-contact gap**：公开帖子 ≠ 私聊/电话过程；
3. **contact-to-payment gap**：联系 ≠ 汇款；
4. **payment-to-shipment gap**：付款 ≠ 发货；
5. **shipment-to-receipt gap**：寄出 ≠ 收到；
6. **receipt-to-condition-acceptance gap**：收到 ≠ 品相接受；
7. **scan-to-object provenance gap**：图片 ≠ 实物真实性/品相；
8. **attachment-survival gap**：正文在 ≠ 扫描/附件在；
9. **bibliographic-object survival gap**：索引在 ≠ 原文/纸刊已保存；
10. **legacy-rendering temporal collapse**：历史正文 + 当前账号字段/模板混合；
11. **gamified-account-state contamination**：后来的签到/等级字段污染早期账号解释。

这些同样适用于钱币、卡片、模型、旧电脑、唱片等收藏论坛。

---

## 12. M1 状态

**M1 NOT ACHIEVED IN THIS SLICE。**

本轮得到的是：

- 多条当前仍在线、承载 2008–2009 历史正文的 `puu.cn` legacy pages；
- 精确 thread URL；
- 当前 renderer 可见的附件/登录/账号字段；
- 同期第一人称的邮寄与联系方式文本；
- 若干独立的机构/媒体集邮史入口。

但本轮**没有取得并实际检查一份 2005–2010 `puu.cn` 或其他中文集邮论坛的 verified Wayback/WARC capture**。

因此目前不知道：

- 2008/2009 的 historical host 是否与当前完全一致；
- 当时论坛软件和版本；
- historical charset / Content-Type；
- 当时 DOM / CSS / JS；
- attachment URL schema；
- 图片是否由论坛本地托管还是外链；
- PM / login / cookie/session 行为；
- 用户等级、积分、签到功能何时加入；
- old thread URL 是否经历 rewrite / migration。

不能因为 current legacy page 能打开就写“2008 普邮网页面已复原”。

---

## 13. 已证实 / 高概率 / 不知道

### 已证实（当前证据允许的窄结论）

- 当前 `puu.cn` 存在承载 2008–2009 日期历史正文的旧帖；
- 这些正文显示论坛被用于缺项清单、文献交流、图片展示、邮寄讨论和跨渠道联系；
- 当前页面会把历史正文与 2020s/2026 的账号状态、签到、模板字段一起呈现；
- Web 可见交换链明显不覆盖全部现实履约过程。

### 高概率

- 论坛显著降低异地收藏者发布 want list 和发现陌生持有者的成本；
- 大量实际成交/交换在 PM、电话、Email、银行和邮政链路中完成，公开 archive 只能看到前后碎片；
- 附件、扫描和旧外链是收藏论坛系统性保存弱点。

### 不知道

- `puu.cn` 2005–2010 的完整页面形态与浏览器环境；
- 当时各版块访问控制；
- 每条 want list 的真实成功率；
- 公开“已出/已换”与真实成交的一致率；
- 论坛用户规模与普通集邮人口之间的关系。

---

## 14. 对历史可见性的结论

集邮论坛出现一种很反直觉的保存关系：

> 一枚纸质邮票可能比买到它的论坛页面、图片附件、QQ 对话、汇款记录和快递单活得更久。

因此数字化并没有让收藏史自动更完整。

今天我们可能仍握着那枚 2008 年交换来的邮票，却已经不知道：

- 是谁先在论坛看见谁；
- 价格怎么谈；
- 谁替谁付了邮费；
- 中途是否丢件；
- 收到以后是否发现品相不同；
- 那条“还缺第 87 期”的清单最后有没有真正补上。

这正是本仓应保存的 state gap，而不是用一个仍在线的老帖子把整个现实交易故事补完。
