# ONLINE DATING / PROFILE / SEARCH / MESSAGE / VERIFICATION / OFFLINE MEETING STATE GAPS, 2003–2015

## Scope

本笔记只处理约 2003–2015 中文旧网中的婚恋/征友平台考古：世纪佳缘、百合网及同时期的严肃婚恋、征友、论坛征婚等界面怎样把现实中的择偶与相亲拆成 profile、search、message、verification、payment 与 offline meeting 等数字状态。

本文件**不**把仓库扩展成全球婚恋史，也不试图判断某个平台“真的帮多少人结婚”。前互联网报纸征婚、法国 Minitel，以及 2020s 移动婚恋主要放在 `how-people-lived` 的跨时期比较中。

交叉研究包：`how-people-lived/topics/from-newspaper-personals-to-online-dating-romantic-addressability-matchmaking-infrastructure-and-partnership-optionality-china-1981-2026.zh-CN.md`。

---

## 1. Minimum state model

对一个中文旧婚恋站，至少拆开：

1. **physical person**：现实中的人；
2. **relationship intention**：现实中是否确实希望交友/恋爱/结婚；
3. **platform account**：平台注册账号；
4. **profile**：公开/半公开个人资料页；
5. **profile field**：年龄、性别、城市、学历、职业、收入、婚姻状态、兴趣等字段；
6. **self-asserted field**：用户自行填写但未被平台核实的信息；
7. **submitted proof**：用户向平台提交的证明材料；
8. **verification badge/state**：平台展示的“已提交/已验证”类状态；
9. **active status / last login**：账号是否近期仍使用；
10. **search query**：用户设置的筛选条件；
11. **search result**：该次查询返回的候选集合；
12. **ranking/exposure**：自然或付费排序/突出展示；
13. **initial message**：首次站内联系；
14. **delivery/moderation state**：消息是否通过过滤并真正送达；
15. **read state**：收件人是否实际读取；
16. **reply / exchange**：站内持续通信；
17. **off-platform contact exchange**：QQ、电话、邮箱等站外联系方式交换；
18. **offline event registration**：线下活动报名；
19. **offline attendance**：实际到场；
20. **face-to-face meeting**：两人现实见面；
21. **relationship state**：约会、恋爱、结束关系等现实状态；
22. **marriage registration**：法律意义上的婚姻登记；
23. **payment state**：邮票/会员/VIP/线下活动等付费；
24. **moderation/blacklist state**：举报、观察名单、黑名单；
25. **archive capture**：今天档案机构保存的页面表示。

### 必须永久保留的状态差

```text
account exists
!= profile complete
!= profile truthful
!= profile proof submitted
!= claim independently true
!= account currently active
!= search result displayed
!= profile actually viewed
!= initial message submitted
!= message delivered
!= message read
!= reply received
!= off-platform contact exchanged
!= offline meeting occurred
!= relationship formed
!= marriage occurred
```

另一个非常重要的状态差是：

```text
registered user accounts
!= unique physical people
!= active user accounts
!= paying user accounts
!= people currently seeking a partner
!= successful relationships
!= marriages
```

---

## 2. 2003–2005: platform existence is not yet historical interface reconstruction

本轮可以可靠确认：

- 世纪佳缘的公司文件把平台起点追溯到 2003，并长期使用 `http://www.jiayuan.com`；
- 百合网当前仍保存的公司历史说明其于 2005 年 5 月正式发布 `www.baihe.com`，核心模式包括心理测试、推荐与搜索。

来源：

- Jiayuan 2011 SEC F-1：<https://www.sec.gov/Archives/edgar/data/1511683/000104746911003874/a2203517zf-1.htm>
- 百合网公司历史页：<https://news.baihe.com/gybh/438.htm>

但这些来源只能证明**平台和某些服务设计存在**，不能直接告诉我们：

- 2003/2005 首版首页实际长什么样；
- 当时的 profile 字段顺序；
- 搜索表单有哪些下拉项；
- 是否要求 IE/特定脚本；
- charset；
- 注册/登录 form action；
- 用户页面是否需要登录；
- 动态搜索结果 URL pattern；
- 婚恋资料是否被 robots、session、验证码或 POST 挡住 archive。

这些都必须等 capture/原始页面证据。

---

## 3. 2008–2011: Jiayuan F-1 gives an unusually detailed transaction-state map

Jiayuan.com International Ltd. 2011 年提交 SEC 的 F-1 是目前本专题最强的一组 A 级平台文件。它不是历史页面 capture，但能证明公司当时如何定义自身业务状态。

### 3.1 search access and user classes

F-1 说明平台提供免费注册并让注册用户直接搜索数据库；同时公司自己区分：

- registered user accounts；
- active user accounts；
- paying user accounts。

截至 2011-03-31，公司自报约 4020 万 registered user accounts；2011 Q1 平均月活约 474 万。

这正好规定旧网研究不能写：

> “2011 年世纪佳缘有 4020 万人在相亲。”

更窄的写法只能是：

> “公司披露截至该日累计注册账号约 4020 万，并另行报告了显著更小的月活跃和付费账号口径。”

A 级来源：<https://www.sec.gov/Archives/edgar/data/1511683/000104746911003874/a2203517zf-1.htm>

### 3.2 search result != neutral exposure

F-1 记录的付费功能包括：

- 提高 search ranking；
- priority ranking for sent messages；
- premium display of pictures/profile；
- 更精细的 profile search；
- 查看谁浏览过自己的 profile；
- 查看另一用户上次登录时间。

因此历史页面里“搜索结果第一个人”并不自动意味着“最符合条件”或“最受欢迎”。页面排序可能混合：

```text
query constraints
+ platform ranking
+ paid exposure
+ account activity
+ unknown internal rules
```

如果未来取得 capture，却没有后台排序规则，研究者只能证明**当时页面这样显示**，不能反推出完整推荐算法。

### 3.3 verification badge != independent truth

F-1 说用户可以付费“submit proof of information posted on their profiles so that other users will know they have submitted such information to us”。

因此至少拆成：

```text
user typed field
→ user submitted some proof
→ platform recorded submission/verification state
→ badge/state displayed
```

不能进一步自动写成：

```text
badge displayed → every underlying claim was independently and continuously true
```

需要具体知道平台当时验证了什么、用什么资料、是否有过期机制、页面标签具体文案。

### 3.4 message submitted != message delivered

F-1 记录：

- 初始消息发送/读取存在付费模型；
- 第一次消息被发送并读取以后，同一对用户可继续站内交流；
- 平台使用关键词软件筛查消息；
- 被标记的信息由客服人工判断是否可以送达；
- 违反规则的消息可能被删除，发送者进入 watch list 或 blacklist。

所以旧网事务模型至少必须有：

```text
sender composes
→ submit
→ automated keyword screening
→ possible human review
→ deliver OR delete
→ recipient account receives
→ recipient logs in
→ recipient reads
→ recipient replies
```

一张“已发送”截图不能证明对方读过；一份数据库里的 message row 也未必证明通过了当年的全部 moderation path。

### 3.5 website communication often intentionally exits the website

F-1 还说，公司历史数据中两名用户站内平均交流约 3.5 天，公司相信愿意继续互动者往往会交换个人联系方式，在站外继续通信。

这会产生一个强烈的 archive asymmetry：

> **平台最可能保存/公开的是关系启动，真正的关系发展却可能很快离开平台。**

因此：

`profile disappears / stops messaging != relationship failed`。

相反，长期在线也不能证明用户始终没有关系，除非有更多证据。

### 3.6 online platform already rebundled offline matchmaking

公司文件记录，自 2008 年以来长期组织线下大型活动；2010 年共称举办 864 场、覆盖 105 个城市，典型活动约 100–200 人。另有 VIP 人工搜索、背景核查、咨询、候选人预筛和线下活动。

所以“Web 婚恋”的边界不是纯 Web：

```text
web profile/search
→ message
→ platform staff
→ offline event / face-to-face interview
→ private contact
```

研究时不能因为用户从网站进入，就把后续线下人工劳动抹掉。

### 3.7 mobile browser is a separate access mode

F-1 记录自 2010-06 起部分功能可通过 mobile browser 使用，包括消息、profile 查看/修改和购买部分增值服务，同时公司承认当时手机设备的分辨率、性能和内存会使体验弱于桌面电脑。

所以：

```text
feature available on desktop web
!= same feature available on mobile web
!= same usability
```

不能拿后来的 App 体验倒推 2010 手机浏览器。

---

## 4. 2008 public-forum personals show why “dating profile” needs provenance

2008 年成都一名 37 岁男性在多个网站论坛公开征婚，并明确表达特殊择偶偏好；同期媒体之后进行了面对面采访。它可以作为 B 级证据，说明婚恋自我描述不只发生在专门婚恋平台，也会出现在通用论坛。

来源：<https://news.sohu.com/20081130/n260930770.shtml>

同年另一个“煤老板替女招婿”的热门帖子随后被识别为戏谑/虚假事件。它提供了非常重要的反例：

```text
public post has photo + biography + stated intention
!= described person exists as claimed
!= poster has authority to represent that person
!= marriage intent is genuine
```

来源：<https://news.ifeng.com/society/2/200810/1022_344_841795.shtml>

因此未来 archive 到任何普通用户征婚页面，都必须把**页面可观察事实**与**现实身份真实性**分开，且遵守隐私最小化，不重新公开普通人的历史联系方式。

---

## 5. 2009–2011: online and family-mediated matchmaking coexist

2009 年《中国青年报》报道中，一位母亲在传统介绍和大型相亲会没有结果后，让儿子注册多个婚恋网站。这类材料不能估算人口比例，但能证明：

```text
family broker
+ offline matchmaking event
+ online profile/search
```

可以同时出现在一个家庭里，而不是“旧式媒人退出 → 年轻人完全个人化”的线性替代。

来源：<https://tech.sina.com.cn/i/2009-12-24/08273706239.shtml>

这也提示旧网 capture 不能只研究个人页面。平台 FAQ、父母代注册、客服协助、线下活动报名等材料可能更能恢复实际使用环境。

---

## 6. 2015 boundary: registered-user milestones still do not solve outcome state

Jiayuan 2015 年公司公告称其多平台注册账号达到 1.5 亿，并给出“successful matches”等公司自定义指标。

来源：<https://www.prnewswire.com/news-releases/jiayuan-surpasses-150-million-registered-user-accounts-300104737.html>

本仓只能把它记成：

- A（公司当时这样公告）；
- 必须保存公司自己的 metric 定义；
- 不把 `successful match` 自动翻译成 marriage；
- 不把累计注册账号当活跃人口；
- 不用 2015 数字反推 2008 页面采用率。

2015 又是本仓 scope 的后边界附近：后续 App、短视频/直播相亲可以在 how-people-lived 延续，但不应该让 old-web 主体无限向 2020s 扩张。

---

## 7. Archive biases specific to online dating

### 7.1 profile-survival / relationship-outcome loss asymmetry

最容易被 archive 保存：

- 首页；
- 帮助页；
- 搜索壳；
- 公司公告；
- 公开 profile（若未被登录/robots 阻止）。

最难保存：

- 双方私信；
- 已读状态；
- QQ/电话交换；
- 真实线下见面；
- 分手/恋爱/结婚结果。

所以保存很好的站点仍然可能对“关系成功”几乎无证据。

### 7.2 active-account / dormant-profile ambiguity

一个历史 profile capture 证明该页在 capture 时可取，不证明本人当时仍活跃。需要 last-login、平台状态、其他证据才能进一步判断。

### 7.3 field survival can exaggerate historical importance

结构化字段比聊天、犹豫、父母意见更容易保存。后人容易因此误以为学历、工资、身高、城市等字段就是当事人完整的择偶逻辑。页面字段只能证明**平台要求/允许用户把自己这样表达**，不等于用户现实决策完全按字段执行。

### 7.4 paid-ranking opacity

即使搜索结果 HTML 被保存，也未必知道哪些位置是付费排名、临时 boost、VIP 曝光或算法排序。没有当时帮助文档/后台规则时，不得把页面顺序解释为“最佳匹配”。

### 7.5 deleted-user / success-selection ambiguity

找到伴侣的人可能主动删除/停用账号；也可能继续保留账号。失败的人同样可能删除。因而“今天 archive 找不到 profile”不能用于推断成功/失败。

### 7.6 private-intimacy boundary

婚恋档案特别容易包含：

- 真实姓名；
- 手机/QQ/邮箱；
- 住址；
- 精确生日；
- 收入、婚史、健康等敏感信息；
- 私信和照片。

本仓研究平台结构时优先记录 field schema、URL pattern、帮助页与匿名化状态机，不批量重新公开已删除的普通用户资料。

---

## 8. Historical browser / encoding questions still open

本轮拿到了明确 original host：

- `http://www.jiayuan.com`
- `http://www.baihe.com`

并尝试通过公开 Web/Wayback 搜索入口寻找 2005–2011 可核验 capture；当前检索没有取得一份已经实际打开、且能同时核验以下字段的历史页面：

```text
archive_source
capture_url
original_url
capture_datetime
HTTP/replay state
Content-Type / charset
DOM/form action
search/result URL pattern
login/session boundary
JS/CSS/image subresources
browser/plugin assumptions
second historical time point
```

因此当前正式结论是：

> **M1 verified historical Chinese online-dating profile/search/message capture: NOT ACHIEVED IN THIS SLICE.**

这不等于“Wayback 没有保存”。本轮没有足够证据判断失败来自索引、robots、动态 URL、登录、session、POST 搜索、JS 或本次检索路径本身。

同样，以下全部保持 UNKNOWN，直到历史 capture/手册能够核验：

- IE-only 与否；
- ActiveX；
- GB2312/GBK/UTF-8；
- frameset/table layout；
- profile/search endpoint；
- 历史验证码；
- 2005→2011 是否沿用同一代码系统。

不得用“2000s 中国网站一般怎样”填补这些空白。

---

## 9. Evidence table

| Claim | Evidence | Grade | Confidence / limit |
|---|---|---|---|
| Jiayuan 2011 已区分注册/月活/付费账号 | SEC F-1 | A | high；公司披露口径 |
| 搜索排名、消息优先级、profile 展示可付费 | SEC F-1 | A | high；具体 UI 尚无 capture |
| 平台存在“提交 profile 信息证明”的服务 | SEC F-1 | A | high；不等于每个事实独立真实 |
| 消息可能经自动关键词筛查与人工 review | SEC F-1 | A | high；内部规则/误判率未知 |
| 站内联系常转移到站外联系方式 | SEC F-1 | A（公司历史数据/解释） | medium-high；公司解释不能证明每一对用户 |
| 平台同时经营大规模线下活动/VIP 搜索 | SEC F-1 | A | high |
| 论坛公开征婚可表达非常具体的个人偏好 | 2008 同期报道 | B | 个案不可外推 |
| 公开征婚帖可能是虚假/戏谑表演 | 2008 同期核查报道 | B | high for case, not prevalence |
| 家庭媒介、相亲会、婚恋网站可以叠加 | 2009 同期报道 | B | 个案/报道不能估人口比例 |
| 合格历史页面 capture 已完成 | 本轮 archive search | — | **NO** |

---

## 10. 已证实 / 高概率 / 不知道

### 已证实

- 2008–2011 的中国专业婚恋平台已经把个人资料、搜索、消息、付费曝光、某些资料证明、人工审核与线下活动组合在同一商业系统；
- 平台自身明确区分注册、活跃和付费账号；
- Web 联系可以很快转移到平台外，因此 archive 天然更擅长保存“相遇入口”而不是“关系结果”；
- 同期通用论坛也存在公开征婚，但帖子内容本身不足以证明身份和动机真实。

### 高概率但仍待 capture 加强

- profile/search 字段把择偶条件进一步结构化，使学历、城市、职业等更容易成为第一轮筛选条件；
- 付费排序与突出展示意味着“搜索页面可见性”已经商品化；
- Web 与线下红娘/活动是长期混合，而不是纯线上替代线下。

### 不知道

- 2003/2005 初版页面精确 UI、编码、浏览器要求；
- 2007–2010 profile/search 字段的逐年变化；
- 具体 verification badge 的历史文案与每项验证范围；
- 搜索结果的算法/付费排序比例；
- 有多少站内消息真正走到线下见面；
- profile 删除与婚恋成功/失败之间的选择偏差。

---

## 11. Next research slice

优先级：

1. 以 `www.jiayuan.com`、`www.baihe.com` 为 original host，定位 2005–2011 至少两个时间点的可实际打开 capture；
2. 优先抓**公开帮助页/搜索说明**而不是普通用户 profile，以降低隐私风险；
3. 记录 profile field schema、search controls、message fee wording、verification label；
4. 若能取得同年用户教程/博客截图，用作第二 evidence family；
5. 单独记录登录、POST、动态结果页或 robots 导致的 archive gap；
6. 不以平台“成功故事”栏目估计真实婚恋成功率。

如果下一轮仍只能找到后来回忆或 archive locator 而不能实际打开，不应把 M1 写得更确定。

---

初稿由 AI 辅助形成；所有历史 claim 以列出的来源和本仓 METHOD 的 evidence contract 为准。