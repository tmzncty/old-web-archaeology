# 兴趣圈、同城活动页与线下聚会：从发现同好到真实共同在场的状态缺口（2005—2015）

> Scope：只研究约 2005—2015 年中文 Web 中，论坛/社区/同城活动页怎样把“共同兴趣”转成“可发现的人与活动”，以及网页上可见的兴趣、报名、成员、地点、讨论、照片等状态与线下真实到场之间的缺口。
>
> 不把本文件扩成全球网络社群史，也不把 1980s 的业余无线电、The WELL 或 2020s“搭子”写进本仓主线；这些只进入 companion life-history note。
>
> Companion：[`tmzncty/how-people-lived/topics/from-hobby-networks-to-dazi-interest-addressability-activity-companionship-and-copresence-china-1980-2026.zh-CN.md`](https://github.com/tmzncty/how-people-lived/blob/main/topics/from-hobby-networks-to-dazi-interest-addressability-activity-companionship-and-copresence-china-1980-2026.zh-CN.md)

本题不是“豆瓣同城怀旧”。它要回答的是：2009 年看到一张活动页，页面上有“感兴趣”“要参加”、地址、地图、讨论和活动照片，究竟能证明普通用户真实经历到哪一步？

---

## 1. 研究单位：不要把“活动页”直接等同于“活动”

本题至少包含以下不同对象：

- forum thread / 论坛召集帖；
- group / 小组、圈子、兴趣社区；
- event index / 同城活动索引页；
- event detail page / 活动详情页；
- organizer account / 发起人或组织者账号；
- interest state / “感兴趣”等意向状态；
- RSVP state / “要参加”、报名、申请等状态；
- comment/discussion / 讨论区；
- map/address / 地点、地图、交通信息；
- ticket/payment / 票务或费用；
- off-platform handoff / QQ、电话、短信、email 等离站协调；
- physical event / 现实活动；
- post-event artifact / 照片、回顾、后续讨论；
- actual relationship outcome / 现实认识、再次见面、关系终止。

最小状态机：

```text
用户有兴趣/活动需要
→ 找到论坛/同城入口
→ 浏览活动索引
→ 过滤时间/类型/城市
→ 打开详情页
→ 理解地点、费用、条件
→ 点击“感兴趣” / “要参加” / 留言
→ 与发起人或其他成员协调
→ 必要时离站到 QQ/电话/短信
→ 当天实际出发
→ 找到地点
→ 活动真实举行
→ 用户真实进入现场
→ 与其他参与者发生共同活动
→ 活动结束
→ 照片/回顾/讨论可能回到 Web
→ 关系结束 / 继续下一次活动 / 转成朋友
```

因此固定：

```text
page exists ≠ event occurred
“感兴趣” ≠ RSVP
RSVP ≠ attendance
attendance ≠ meaningful interaction
interaction ≠ friendship
member list ≠ people physically present together
photo exists ≠ complete attendance record
map displayed ≠ venue was found successfully
forum reply ≠ organizer saw it
organizer account exists ≠ organizer was reachable
ended page ≠ reliable historical transaction capture
```

---

## 2. 为什么这一题与普通 Web 社区研究不同

论坛研究常停在：

```text
发帖 → 回复 → 社区互动
```

而同城活动把 Web 接到了一个新的现实状态：

```text
发帖 / event page
→ 人必须离开浏览器
→ 在某个具体时间到某个具体地点
→ 与其他身体共同出现
```

这让 **co-presence state / 共同在场状态** 成为必须单独验证的层级。

一份保存完整的 HTML 最多可以证明平台当时如何表示活动；它无法自己证明：

- 用户当天是否出门；
- 活动是否临时取消；
- 场地是否改变；
- “要参加”的用户是否 no-show；
- 未点 RSVP 的人是否临时到场；
- 线下是否通过 QQ/电话完成最后确认；
- 聚会以后是否真的成为朋友。

---

## 3. 2008：论坛帖子可以把文字互动导向定期聚会，但原 transaction 仍然缺失

2008 年 1 月《新快报》报道 21CN“广州人广州事”论坛的一场“80 后”故事接龙。版主“BB噶烧卖”向记者说，自己刚毕业工作，同事忙、很难结交新朋友，发帖也希望认识更多同龄人；报道称近 300 名网友加入接龙，一些网友后来彼此认识，并定期出来聚会。

B 级同期来源：

- 新快报/新浪，《故事接龙演绎“80后”生活》，2008-01-11：<https://news.sina.com.cn/c/2008-01-11/012413236036s.shtml>

这可以窄地支持：

```text
2008 年中文地方论坛
存在“线上主题互动 → 一部分参与者线下聚会”的同期案例
```

不能支持：

```text
21CN 所有参与者都见过面
论坛成员数 = 聚会人数
报道中的聚会一定能由今天 archive 独立复原
```

### Archive gap

本轮没有得到该故事接龙原帖的已验证 Wayback/WARC capture，也没有确认：

- 原帖 URL；
- 原 HTML/charset；
- 用户登录状态；
- 分页与楼层编号；
- 是否有“聚会报名”专门回复；
- 是否留下活动后的照片/名单。

因此该对象目前仍是 **B-level behavioral evidence + unverified original thread**，不能升级成 M1 capture。

---

## 4. 2008：同一人生阶段也能成为线上召集条件

2008 年 3 月《新闻晨报》报道，40 多名“80 后”年轻母亲通过网络组织，在上海长风公园带宝宝聚会。受访者朱小姐说，她从 2006 年怀孕开始就在论坛认识预产期相近的妈妈群体，“8月猪妈帮”按宝宝出生月份形成。

B 级同期来源：

- 新闻晨报/新浪，《“80后”白领妈妈群“晒”宝宝》，2008-03-17：<https://news.sina.com.cn/s/2008-03-17/031013582659s.shtml>

对 old-Web 来说，这说明 group membership 的分类键不一定只是抽象兴趣，也可能是：

```text
城市
+ 人生阶段
+ 预产月份 / 孩子年龄
+ 周末时间
```

但报道没有提供论坛 URL、注册/审核规则、群成员状态或活动报名 workflow，不能反推平台技术。

---

## 5. 豆瓣同城 2009：同时代官方文档把“活动可发现性”做成明确产品状态

豆瓣官方 2009 年 3 月的产品博客是本题目前最强的 A 级同时代平台证据之一。官方称“同城”已经上线一年，并描述新版首页将：

- 突出“一周热门”；
- 按类型展示活动，例如“音乐演出”“生活聚会”；
- 将时间筛选和内容类型筛选放在同一侧，便于交叉选择；
- 将用户创建的活动按“主题活动”聚合；
- 给已结束活动增加“精彩回顾”，利用照片和讨论保留资料价值。

A 级来源：

- 豆瓣官方博客，《同城即将上线新首页》，2009-03-04：<https://blog.douban.com/douban/2009/03/04/376/>

7 月官方博客又介绍“同城活动地图”：活动地点足够准确时可以自动生成地图，发起人也可手工标注；参加者在活动页看到地图。A 级来源：

- 豆瓣官方 2009 年归档，《同城活动地图上线》，2009-07-24：<https://blog.douban.com/douban/2009/>

这组材料可以可靠证明平台当时有意把：

```text
city + time + category + event page + location
```

组合为 event discovery interface。

但 A 级平台文档仍然只能证明 **product state**，不证明：

- 每个活动都有准确地点；
- 地图 API 对所有用户/浏览器都正常；
- “热门”意味着实际到场人数多；
- 已结束活动一定真实发生；
- 照片来自活动当天且覆盖实际参与者。

---

## 6. 一个仍在线的 2010 legacy event page：用户可见状态非常丰富，但不是历史 capture

目前仍能访问一个豆瓣 legacy event URL：

```text
https://www.douban.com/event/12171101/
```

页面标题为“中国新设计”系列活动，正文保留 2010 年 7 月的日期、地点/项目说明、免费状态、组织者、照片、讨论区，以及：

```text
84 人参加
532 人感兴趣
```

页面还保留成员级的“感兴趣”“要参加”等状态，以及平台的提示：活动信息由发起人自行发布，后续事项由发起人负责，豆瓣只提供信息展示空间，不能保证活动真实性、有效性与安全性。

当前可访问页面：

- <https://www.douban.com/event/12171101/>

### 证据等级与边界

这个对象非常有价值，但必须准确描述为：

**current live legacy page carrying historical-looking 2010 event content / 今天仍在线、承载 2010 活动内容的 legacy 页面**。

它**不是**本轮已验证的 2010 Wayback/WARC capture。

因此它可以证明：

- 当前这个 legacy URL 呈现上述字段与旧内容；
- 豆瓣的现行/遗留模板仍区分“感兴趣”“要参加”；
- 页面自己承认信息展示与现实活动安全/真实性之间有责任边界。

它不能独立证明：

- 2010 年 7 月当天 DOM 与今天完全相同；
- 当年 HTTP charset、CSS/JS 与今天相同；
- `84 / 532` 是活动发生前、发生后还是后来最终固化的数值；
- 成员状态在当年通过什么 POST endpoint 写入；
- 用户点击“要参加”后是否收到邮件/站内信；
- 84 个账号真实到场 84 人。

### 一个特别重要的 state gap

平台把至少两个意向状态显示给公众：

```text
interested
want-to-attend / RSVP-like state
```

这本身已经证明：

```text
interest ≠ intention-to-attend
```

而平台自己的安全提示又进一步说明：

```text
intention-to-attend ≠ verified real-world event
```

因此任何以后统计历史豆瓣活动的人，都不能把“感兴趣 + 要参加”当作线下客流。

---

## 7. 2009“99人书库”：平台计数、媒体观察与现实活动要分开

2009 年《南方都市报》报道豆瓣用户组织“99人书库”，并围绕书库做纪录片放映、展览、沙龙、诗歌、设计和音乐等活动。报道给出深圳 524 人“参与”、1627 人“感兴趣”、全国 4980 人“感兴趣”等数字，并采访实际参加过纪录片放映的 Nini。

B 级同期来源：

- 南方都市报/新浪，2009-11-23：<https://news.sina.com.cn/c/2009-11-23/041916650641s.shtml>

这是一个很好的三层证据组合：

```text
平台数字（报道转述）
+ 媒体对组织者/参与者采访
+ 至少一名受访者明确说参加过线下活动
```

但仍不能把这些层级合并：

- `1627 感兴趣` 不是 1627 到场；
- `524 参与` 的平台字段语义需要原页面才能确认；
- 一名 Nini 到场不能证明所有活动按计划举行；
- 媒体照片也只是被选中的活动时刻。

### Historical locator

同期独立网页曾保留一个豆瓣活动 URL locator：

```text
http://www.douban.com/event/10830731/
```

本轮没有得到并实际检查这个 URL 对应的 Wayback/WARC memento，因此它只能登记为 **candidate historical locator**，不能称为 verified capture。

---

## 8. 从“论坛帖子”到“event object”：旧网状态模型发生了什么变化

论坛召集常接近：

```text
thread title
→ post body
→ replies
→ organizer manually counts / contacts users
→ off-platform coordination
```

同城 event object 则把更多字段显式结构化：

```text
title
+ date/time
+ city/venue
+ category
+ organizer
+ fee/ticket info
+ map
+ interested state
+ attendance-intent state
+ discussion
+ photos / recap
```

这不是简单的 UI 进步。结构化以后，平台才能进一步：

- 按城市/日期/类型检索；
- 排热门；
- 做地图；
- 聚合同一主题；
- 让活动结束后进入“回顾”状态；
- 把成员意向显示成可见的社会信号。

因此一个重要 old-Web 概念是 **event objectification / 活动对象化**：现实里本来模糊的“周末有人去看展吗”，被平台压成一套可索引、可排序、可计数的字段。

但字段越漂亮，越容易诱发 **state-completeness illusion / 状态完整性幻觉**：页面看起来已经描述了整个活动，实际上最重要的现实执行状态仍然在网页之外。

---

## 9. RSVP 的历史考古：为什么“要参加”不是 attendance log

活动页面上最危险的字段就是人数。

至少需要拆成：

```text
page view
→ interest mark
→ RSVP / want-to-attend
→ organizer accepts (若有审核)
→ user still intends on event day
→ user travels to venue
→ user finds venue
→ user checks in / is observed present
→ user stays for meaningful part of event
```

历史页面通常最多保存前 2—4 层。

现实中的以下状态往往不可见：

- 临时加班；
- 天气/交通导致取消；
- 忘记；
- 约了朋友后改计划；
- 活动临时改地址；
- 未点“要参加”却直接到场；
- 一个账号带多人；
- 到门口发现不合适就离开。

因此必须固定：

```text
RSVP count is a platform-state count, not a headcount.
```

没有独立签到/现场观察时，不得把 RSVP 数作为活动规模。

---

## 10. Event discovery 也有 executability stack

即使页面是真实历史 capture，一次现实共同在场仍至少依赖：

```text
页面可访问
→ 字符集/浏览器正常
→ 用户能搜索/过滤
→ 地点能理解
→ 地图/交通信息可用
→ 时间与本人日程重叠
→ 费用可负担
→ 联系方式有效
→ 发起人仍在组织
→ 必要票务/报名成功
→ 当天交通可达
→ 现场安全和准入条件成立
```

因此：

`event discovery ≠ event executability`。

这一点尤其需要和 companion 的 `temporal executability`、`transport`、`payment`、`identity` 研究交叉，而不能只看一张活动详情页。

---

## 11. 线上身份与线下身份之间还有一个 encounter gap

论坛昵称或豆瓣账号可以在活动页上非常熟悉，但第一次见面时仍存在：

```text
account identity
≠
physical person encountered at venue
```

平台头像、昵称、发言历史可以降低完全陌生感，却不能自动完成现实身份核验和安全判断。

同样：

```text
online familiarity ≠ offline trust
```

本题不研究实名制，也不尝试重新识别历史普通用户。对于旧活动页中的普通账号，按仓库隐私原则只保留支持 state-model 所需的最少信息，不批量复制成员列表。

---

## 12. 最重要的保存偏差：public-event-shell / private-attendance-state asymmetry

旧网很容易留下：

- 活动标题；
- 时间地点；
- 发起人；
- “感兴趣 / 要参加”计数；
- 公开讨论；
- 活动照片；
- 结束后的回顾；
- 成功活动被媒体报道的故事。

但真正决定“这次社交有没有发生”的信息最容易消失：

- 私信；
- QQ/短信/电话确认；
- 临时改期；
- no-show；
- 取消；
- 现场谁真正来了；
- 谁和谁真的聊过；
- 不愉快、安全事故或提前离场；
- 活动后是否继续联系。

这构成：

**public-event-shell / private-attendance-state asymmetry / 公开活动壳层—私人到场状态不对称**。

档案保存的往往正是“看起来最像活动已经完成”的部分。

---

## 13. event survivorship bias：成功聚会比“什么也没发生”更容易进入历史

平台会保留热门活动、照片、精彩回顾；媒体会报道“网友从线上走到线下”；参与者也更可能回忆有意思的一次聚会。

而下面这些状态几乎没有纪念品：

```text
没人报名
报名两人最后都没去
发起人取消
群里约了半天没定时间
去了发现聊不来
见一次以后再无联系
```

所以不能从 archive 中“成功活动占多数”推出当年的真实成功率高。

后续若做抽样，必须主动找：

- cancelled；
- postponed；
- “没人来”；
- “鸽子”；
- “改期”；
- “活动失败”；
- 只有 announcement、没有 recap 的页面。

这类 **negative state survival / 负状态幸存** 应与仓内已有 `ABANDONED_APPLICATIONS_AND_NEGATIVE_STATE_SURVIVAL_2007_2015.md` 方法互通。

---

## 14. 浏览器、字符集和动态状态的具体未知项

对于 2008—2010 中文 event/community 页面，未来拿到真实 capture 时至少要记录：

- HTTP `Content-Type` / charset；
- GB2312/GBK/UTF-8；
- IE6/IE7 与当时主流浏览器兼容；
- event list 是否服务端渲染；
- 时间/类型筛选是 GET、POST 还是 JS；
- 地图依赖的第三方 JS/API 是否被 archive 保存；
- “感兴趣 / 要参加”按钮是否需要登录；
- 点击后的 endpoint、CSRF/session/cookie；
- 数字计数是 HTML 固化还是异步拉取；
- 讨论分页；
- 图片 CDN/相册资源；
- 已注销账号后来如何回写历史成员列表；
- 已结束状态何时产生、由什么字段决定。

现代 Chromium 今天能打开 legacy page，只能证明今天能得到这种呈现，不能证明 2010 年用户在 IE/Firefox 下看到完全相同页面。

---

## 15. 本轮证据分层

### A：同期平台原始证据

- 豆瓣官方产品博客 2009：同城首页改版、时间/类型过滤、主题索引、精彩回顾；
- 豆瓣官方产品博客 2009：同城活动地图。

这些支持产品设计/平台宣称，不自动支持实际活动效果。

### B：同期媒体与用户行为证据

- 2008 21CN 论坛故事接龙与线下聚会采访；
- 2008 年轻母亲论坛群体公园聚会；
- 2009 “99人书库”媒体采访与参加者自述。

这些支持具体行为案例，但原论坛/event transaction 多数未被本轮 archive 验证。

### 当前 legacy artifact

- `https://www.douban.com/event/12171101/`：今天仍在线、承载 2010 活动字段和成员状态的 legacy 页面。

它不升级为 2010 historical capture。

### D：研究者机制推断

- `event objectification`；
- `public-event-shell / private-attendance-state asymmetry`；
- `event survivorship bias`；
- `co-presence executability`。

这些概念必须继续由更多历史 capture 和负状态样本检验。

---

## 16. 本轮 M1 / archive 负结果

本轮没有取得并实际验证一份满足本仓 M1 门槛的 2005—2010 中文兴趣活动完整 Wayback/WARC transaction capture。

当前具体 locator 包括：

```text
21CN 广州人广州事论坛（报道可确认平台/版面，原帖 URL 未确认）
http://www.douban.com/event/10830731/   # 同期独立网页保存的 historical locator，未验证 memento
https://www.douban.com/event/12171101/  # 当前 live legacy page，不是历史 capture
```

因此以下内容继续全部是 `unknown`：

- 原活动页 capture datetime；
- 原始 HTML/charset；
- 当年 CSS/JS；
- RSVP POST endpoint；
- cookie/session；
- 计数更新机制；
- 取消/退出 RSVP 的状态；
- 私信/QQ/电话 handoff；
- 实际签到；
- no-show rate；
- “要参加”与真实到场的转换率。

这不是研究失败，而是本题最重要的考古边界之一。

---

## 17. 隐私与版权 stop condition

兴趣活动特别容易诱使研究者顺着公开旧账号去拼普通人的真实姓名、电话、QQ、学校与现实聚会轨迹。本仓不这样做。

以后取得旧活动页时：

- 优先记录字段结构、URL pattern、计数与公开状态；
- 普通用户 ID 仅在 claim 必需时最小化引用；
- 不批量重新公开成员列表；
- 不尝试把活动账号重新识别到现实个人；
- 不为了验证“后来是否成为朋友”追踪私人社交关系；
- 不复制版权不明的整页照片/相册。

`attendance unknown` 可以永久保持 unknown。

---

## 18. 下一步最有价值的证据

1. 实际打开并检查 2008—2010 豆瓣同城 event/index 的 Wayback memento，记录 original URL、capture datetime、HTTP/charset、资源完整性；
2. 找至少一份同期用户教程，确认“感兴趣/要参加/退出/发起活动”的真实操作路径；
3. 找一组有明确 `取消 / 改期 / 鸽子 / 无人参加` 的活动页，纠正成功活动幸存偏差；
4. 找 21CN、天涯地方版、豆瓣小组等论坛式召集与 event-object 式召集的同年对照；
5. 在旧浏览器环境中检查活动地图、筛选器和 RSVP 控件是否需要特定 JS/浏览器；
6. 将 event page 与 companion life-history note 的城市交通、时间、陌生人安全和活动型陪伴机制交叉，而不是从页面直接推断社会结果。

---

## 19. 本轮最重要的方法结论

旧互联网最容易给后人制造一种错觉：

> 页面写着“84 人参加”，所以 84 个人曾经在那里共同生活过两个小时。

真正能从页面直接读出的，只是平台曾保存一种 `want-to-attend / participate-like` 状态。

**从网页上的“我想去”，到现实里的“我真的去了、见到了另一个人、一起完成了那件事”，中间仍然有一整条不可见的生活链。**

中文旧网考古如果不把这条链拆开，就会把平台的社交想象误写成普通人的现实生活。