# `love21cn.com` / 世纪佳缘：profile 搜索、身份验证、中继联系与关系状态缺口（2003—2011）

## Status

Research note / candidate old-Web case.

**This is not an M1 complete case.**

本轮取得了：

- 2003—2007 `www.love21cn.com` 的多条同时代 identity / locator 证据；
- 一个 2007 年具体活动页面 URL：`http://www.love21cn.com/xiangqin/index.html`；
- 同时期对 profile、条件搜索、身份 / 学历证明、手机端搜索、线下打印、匿名中继联系等操作的描述；
- 2011 年婚恋平台“前台匿名、后台实名”的身份层证据。

但本轮**没有实际打开并核验**满足仓库合同的历史 Memento：

- 没有已核验的 `capture_datetime`；
- 没有 historical HTTP / replay state；
- 没有已检查的 DOM / charset / subresources；
- 没有两个已核验历史时点。

因此不能把它写成“世纪佳缘 2007 页面已复原”。

与 `how-people-lived` 的交叉研究：

- <https://github.com/tmzncty/how-people-lived/blob/main/sources/from-newspaper-personals-to-searchable-spouse-pools-matchmaking-infrastructure-and-profiled-eligibility-china-1981-2025.zh-CN.md>

---

## 1. 本轮为什么适合 OWA

婚恋网站把 old-Web archaeology 的几个问题同时放大：

1. **页面不是人。** 一个 profile 是某时刻的平台表示，不是这个人的永久婚姻 / 关系状态。
2. **搜索结果不是静态网页集合。** 候选池由条件、排序、活跃状态、认证状态和平台规则动态决定。
3. **联系可能离开 Web。** 电话、短信、纸条、线下活动、匿名转接号码都可能成为下一跳。
4. **“成功”可能导致数字对象消失。** 找到伴侣后隐藏 / 删除 / 停止登录，本身可能是目标完成。
5. **隐私风险极高。** 历史 profile 可能包含照片、年龄、学历、婚姻史、住房、收入、电话等；archive 可访问不等于应该重新结构化发布。

因此这个 case 不应该以“恢复一个漂亮的 2007 首页”为目标，而应该先恢复它的**状态模型与跨通道动作链**。

---

## 2. Historical identity：`www.love21cn.com`

2006 年有至少两个不同类型的同期来源能确认：

- 世纪佳缘历史域名为 `www.love21cn.com`；
- 创办时间为 2003 年 10 月；
- 品牌当时已经在首页和 Google 广告语境中被使用。

### Evidence family A：创办人新浪在线访谈

- 新浪科技，2006-01-23：
  - https://tech.sina.com.cn/it/2006-01-23/1115827191.shtml
  - 明确写出 `www.love21cn.com`，并称网站创办于 2003-10-08；
  - 平台强调身份证明、学历证明等“真实性”机制。
  - **A/B：同时代平台创办人公开陈述。**

它能证明“平台当时这样描述自己的功能与定位”，不能自动证明所有 profile 都真实，也不能把平台自报规模当成独立审计数据。

### Evidence family B：品牌 / 搜索争议

- 新浪科技，2006-09-30：
  - https://tech.sina.com.cn/i/2006-09-30/11321168085.shtml
  - 平台声明再次明确 `www.love21cn.com` 是世纪佳缘网站，并称 2003 年 10 月创建、2004 年申请商标、2004 年起购买 Google 广告。
  - **A/B：同时代平台声明，经新浪发布。**

这组材料足以把 `love21cn.com` 作为 historical host candidate 锁定，但仍不是 archive capture。

---

## 3. 2007 活动页给出了一个高价值 exact locator

2007-02-13 《京华时报》报道给出一个非常具体的 URL：

`http://www.love21cn.com/xiangqin/index.html`

报道描述的动作是：

```text
用户打开活动页
→ 填写个人资料
→ 征友资料显示在网页
→ 工作人员把资料打印 / 悬挂在地坛活动现场
→ 线下参与者把纸条投入 profile 下的信封
→ 工作人员再把纸条交给征友人
→ 部分人现场见面
```

来源：

- https://news.sina.com.cn/c/2007-02-13/035311227831s.shtml
- **B：同期媒体对具体 URL 和工作流的报道。**

这条 locator 的价值高于只知道首页域名，因为它指定了：

- host；
- path；
- 功能上下文；
- 使用日期附近；
- 页面和现实活动的对应关系。

但仍必须坚持：

## `historical locator != verified Memento`

本轮通过 Web 搜索和直接 URL probe 没有取得一个可以实际打开检查的历史 capture。直接对 legacy URL 的当前 open 也没有得到可解释的历史内容。

所以当前状态只能写：

```text
exact historical URL: achieved
verified historical capture: NOT achieved
```

不能写“Wayback 没有保存”。

---

## 4. Profile 不是“一个人的数字副本”：`profile-to-person state gap`

婚恋 profile 通常包含：

- 年龄 / 出生年份；
- 城市；
- 学历；
- 职业；
- 身高；
- 婚姻状态；
- 自我描述；
- 择偶条件；
- 照片；
- 认证 / 信用标记；
- 活跃 / 联系状态。

但这些字段的历史含义必须拆开。

例如：

```text
profile says “未婚” at t1
!=
person remained unmarried at capture t2
!=
person consented to have that old state republished in 2026
```

因此定义：

## `profile-to-person state gap`

archive 保存的是某个时点的**平台表示**，不是对现实人的永久事实宣告。

对于已婚 / 离异 / 丧偶、性取向、照片、收入、房产、联系方式等字段，历史复原必须实行比普通新闻页更强的研究必要最小化。

### Repo policy

若未来取得真实个人 profile capture：

- 不把姓名、照片、电话、QQ、email、详细地址重新复制进仓库；
- 不建立可搜索的普通用户婚姻史数据库；
- 优先记录字段 schema、控件类型、是否必填、是否公开、是否验证；
- 需要截图时优先做字段级 redaction；
- 若 claim 可由平台帮助页 / 媒体操作报道支持，就不以普通人的历史隐私换取重复证据。

---

## 5. Search 页面保存下来，也不等于候选池保存下来

2007 年与 2006 年材料已经证明世纪佳缘存在按条件寻找候选的产品逻辑；2007 年维信 / Widsets 的手机端合作更明确描述：用户可以按条件查询合适对象，查看个人自述、择偶要求和相册。

来源：

- CNMO 厂商稿，2007-08-16：
  - https://www.cnmo.com/news/3812.html
  - **A/B：同期厂商发布材料。**

这带出一个比 `page != transaction` 更具体的缺口：

## `candidate-pool state invisibility / 候选池状态不可见`

一个保存完整的 search form 仍然不能告诉我们：

- 某一天满足条件的 profile 有多少；
- 哪些 profile 当时已隐藏 / 删除；
- 哪些用户最近活跃；
- 搜索结果是否按更新时间、付费、活跃度或其他规则排序；
- 同一查询在不同账号下是否相同；
- 谁因 block / privacy / membership state 而不可见。

需要把历史搜索体验建模成：

```text
query parameters
+ account state
+ candidate corpus at t
+ visibility rules
+ ranking rules
→ result set
```

Web archive 往往只可能保存第一项和部分 presentation，后四项大多是后台状态。

因此：

## `captured search form != preserved candidate pool`

---

## 6. `verification-state gap`：一个“已认证”图标背后还有后台事务

2006 年平台访谈已经把身份证明和学历证明作为“真实性”卖点。

到 2011 年，百合网把这类问题推进成强制实名：同时代报道明确写出：

```text
前台匿名
后台实名
```

新用户必须实名验证；老用户有过渡期；身份信息与全国公民身份信息系统进行比对；用户之间交换实名认证信息还需要授权。

来源：

- 中国广播网，2011-12-15：
  - https://finance.cnr.cn/gs/201112/t20111215_508933705.shtml
- 财新网，2011-12-15：
  - https://companies.caixin.com/2011-12-15/100338598.html
- **B：同时代新闻；可确认平台当时的认证制度与数据流描述。**

这说明需要把 identity 拆成：

```text
account identifier
public nickname
self-claimed profile fields
phone verification
ID verification
education/property/etc. badges
backend real-name record
mutually authorized disclosure
```

定义：

## `verification-state gap / 认证状态缺口`

即使 archive 抓到了一个“已实名 / 已认证”badge，也仍然不知道：

- badge 何时产生；
- 当时依据哪套数据库；
- 后来是否过期 / 撤销；
- badge 能验证哪些字段、不能验证哪些字段；
- 用户自述的收入、人格、恋爱意图是否仍完全是 claim。

所以 archaeology 不能把：

`identity verified`

扩写成：

`the whole profile was true`。

---

## 7. 2007 “佳缘通”：网页之外还有 `contact-relay layer`

地坛活动报道最有考古价值的技术细节之一，是“佳缘通”号码。

提前报名者可以取得一个中继号码；感兴趣者能够通过它联系报名者，而不知道对方常用的真实联系方式。

这意味着历史联系链可能是：

```text
Web profile
→ platform/event identifier
→ telephony relay number
→ real phone endpoint
```

这里引入：

## `contact-relay layer / 联系中继层`

即使 Web capture 完整保存：

- profile；
- “佳缘通”按钮 / 文字；
- relay number format；

也不代表 relay 的真实后台映射被保存。

真正丢失的可能是：

- temporary mapping；
- expiry；
- call routing；
- access control；
- caller / callee consent；
- event-specific validity。

因此：

## `captured relay identifier != preserved communication route`

这也是一个典型的 privacy-preserving historical function：平台在当时已经尝试把“可以联系”与“直接公开日常电话号码”拆开。

---

## 8. Web profile 可以离开 Web：`offline event projection`

2007 地坛案例证明，profile 不只是在浏览器里被读。

它可以被：

- 打印；
- 分类；
- 挂在现场；
- 附上纸信封；
- 由工作人员引导到某个专区；
- 再由纸条触发下一次联系。

定义：

## `offline event projection / 线上资料的线下投影`

这要求 OWA 不把“页面的用户体验”限制成 browser session。

一个 historical Web object 可能进入：

```text
HTML
→ printer
→ paper placard
→ physical venue
→ handwritten response
→ staff delivery
```

如果未来只恢复网页 CSS，而完全忽略它如何被打印、张贴和用于现场分类，就仍然漏掉这个页面的一项主要 historical use。

---

## 9. `relationship-state semantics`：平台里的“成功”字段不是结婚证

婚恋平台特别容易产生 metric overclaim。

同期报道里曾出现类似：

- “已找到中意人选”；
- “交友成功”；
- “牵手成功”；
- “会员成功故事”。

这些不是同一个 state。

建议建立最小状态词典：

```text
profile active
contact initiated
reply received
private contact exchanged
offline meeting
mutual interest
relationship reported
profile hidden / inactive
marriage self-reported
marriage externally confirmed
```

定义：

## `relationship-state semantics / 关系状态语义`

例如“已找到中意人选”最多表示用户 / 平台登记了一个中间状态；不能直接转换成：

- marriage count；
- durable partnership；
- platform-caused marriage。

以后任何平台自报“成功率”都必须先问：

> **成功字段究竟在产品里是什么意思？**

---

## 10. `termination success paradox`：成功可能导致最重要的账号消失

这是本轮最值得留下的 archive-bias 假设。

对于一般内容平台：

```text
持续发内容
→ 通常留下更多可观察历史
```

而对于 serious matchmaking service：

```text
找到伴侣
→ 停止搜索
→ 隐藏 profile / 停止登录 / 注销
→ 平台可观察性下降
```

因此存在：

## `termination success paradox / 退出即可能是成功`

这意味着历史 archive / 现存数据库可能系统性偏向：

- 长期未匹配者；
- 反复使用者；
- 愿意持续公开 profile 的人；
- 没有删除账号的人。

而低估：

- 快速形成关系后退出的人；
- 转入电话 / QQ / 线下的人；
- 因隐私删除的人。

这目前是**D 级方法假设**，需要未来用帮助页的 hide/delete 机制、账号生命周期说明、用户同期讨论或平台数据库文档验证。

不能因为逻辑合理就写成已测量偏差。

---

## 11. 一个低等级但有用的注销 lead

2007 年百度知道里存在“世纪佳缘注册号怎么注销”的用户提问，其中被推荐回答称需要联系客服、用户自己无法完成。

来源：

- https://zhidao.baidu.com/question/23122500
- **C / user-generated lead：不能单独当作平台正式规则。**

它至少提示未来应主动寻找：

- 2006—2008 help / FAQ；
- 注销 / 隐藏 / 暂停征友；
- “已找到对象”状态是否自动停止搜索；
- profile 是否仍被搜索引擎索引。

如果取得同时代官方帮助页，`termination success paradox` 才能从方法假设升级为具体平台机制。

---

## 12. Attention / payment state 也会改变“谁能联系谁”

2011 年《经济观察报》报道世纪佳缘以“邮票”为核心盈利模式，每张约 2 元，追求者写信需要消耗邮票；相较之下百合网使用时段会员包。

来源：

- https://www.eeo.com.cn/2011/1226/218762.shtml
- **B：同期财经媒体。**

这又带出：

## `contact-entitlement state / 联系权限状态`

一个 profile “可以看到”并不等于：

- 可以给它写信；
- 收件者一定能免费阅读；
- 两人拥有相同权限；
- entitlement 在 capture 时仍有效。

历史 contact experience 可能依赖：

```text
account type
+ payment state
+ virtual stamp balance
+ sender-paid / recipient-paid rule
+ anti-spam / blocking state
```

这些几乎都不会随着 public HTML 一起进入普通 crawler。

---

## 13. Mobile Web / client 是同一候选池的另一层 representation

2007 年 Widsets 与世纪佳缘合作的厂商材料称，手机端可以：

- 按条件搜索候选；
- 查看自我介绍；
- 查看择偶要求；
- 查看相册；
- 快速注册；
- 后续计划加入站内收信和聊天。

来源：

- https://www.cnmo.com/news/3812.html

这说明历史平台研究单位不能只写：

`love21cn.com = desktop website`

还应至少预留：

```text
desktop Web corpus
mobile widget/client representation
shared account/profile database?
shared search rules?
message state synchronization?
```

本轮没有取得 Widsets 客户端、JAR / widget binary 或协议文档，因此这些共享关系只能作为后续问题，不能推定。

---

## 14. Browser / charset / runtime 假设

本轮没有 historical capture，因此**不猜**当时页面一定使用何种：

- IE-only JS；
- frames；
- GB2312 / GBK；
- CSS layout；
- image map；
- login cookies；
- form POST endpoint。

但未来若找到 capture，应优先检查：

1. 首页和活动页的 declared charset；
2. profile/search form 是否 GET / POST；
3. URL 是否携带 user ID / search parameters；
4. 登录态与 anonymous browsing 差异；
5. 验证 badge 是否 image resource / server-rendered text；
6. 站内信是否 frame / popup；
7. 图片是否 hotlink / separate host；
8. crawler 是否被 session redirect 到首页。

在这些条件未验证前，现代 Chromium 的当前渲染不应被称为 historical experience。

---

## 15. Archive / locator 状态

本轮确认的 historical locators：

- `http://www.love21cn.com/`
- `http://www.love21cn.com/xiangqin/index.html`

同时代 provenance：

- 2006 新浪科技创办人访谈；
- 2006 新浪科技品牌声明；
- 2007 《京华时报》活动操作报道；
- 2007 北京日报 / 搜狐关于 `love21cn.com` 早期网站的报道；
- 2007 Widsets / CNMO 手机服务材料。

本轮 archive probe 结果：

```text
historical site identity: ACHIEVED
exact historical locator: ACHIEVED
contemporaneous workflow evidence: ACHIEVED
profile/search/verification/contact model: ACHIEVED
verified historical Memento: NOT ACHIEVED
second verified historical timepoint: NOT ACHIEVED
M1 complete case: NOT ACHIEVED
```

重要：

> **“本轮没实际打开核验 capture”不等于“archive 没保存”。**

下一轮可继续从 CDX / Memento API / Common Crawl / 搜索引擎残留 locator 推进，但只有实际取得并检查 capture 才能升级。

---

## 16. Privacy boundary：婚恋旧站是高风险 artifact family

婚恋 profile 比普通个人主页更容易包含：

- 照片；
- 年龄 / 出生日期；
- 婚姻史；
- 子女状态；
- 教育；
- 工作单位；
- 收入；
- 房产；
- 电话 / QQ / email；
- 对伴侣的私人条件；
- 身份认证标记。

所以本仓对此类 artifact 采用比一般旧站更严格的最小化：

### 可以保存 / 提交

- platform-level URL；
- capture metadata；
- field names；
- form structure；
- anonymous / required / optional state；
- synthetic example；
- redacted screenshot；
- aggregate counts；
- public founder / corporate statements。

### 默认不重新发布

- 普通人的完整 profile；
- 历史照片集合；
- 电话 / email / QQ；
- 精确工作单位 + 年龄 + 婚姻状态组合；
- 身份证 / 学历证明材料；
- 已删除用户的可识别婚恋史。

`archive accessible != ethical republication`。

---

## 17. 与海外 old-network 史的边界

本仓仍保持约 1995—2015 中文互联网 scope。

法国 Minitel 1980s 匿名 messagerie、美国 Match.com 1995 的 Web personals 非常适合作为机制比较，但不扩写为本仓全球 old-Web 主线。

跨国生活史与 Internet 前史放到 `how-people-lived`；OWA 这里只保留它们对中文案例有直接解释价值的比较：

- Web 不是第一次出现匿名远程陌生人交流；
- online personals 可以从纸质 classified 的操作逻辑演化；
- 中国婚恋网站的 profile / verification / family-proxy / offline-event 组合仍需以中文一手材料独立研究。

---

## 18. Claim table

| Claim | Evidence | Grade | Status |
|---|---|---:|---|
| 2006 年世纪佳缘使用 `www.love21cn.com` | 新浪创办人访谈 + 平台声明 | A/B | 已证实 |
| 平台称创建于 2003-10-08 / 2003-10 | 同上 | A/B | 平台自述可证 |
| 2007 地坛活动有 `love21cn.com/xiangqin/index.html` | 京华时报 | B | 已证实 locator |
| Web profile 被打印到线下活动现场 | 京华时报 | B | 已证实 |
| “佳缘通”允许不知道常用联系方式时联系报名者 | 京华时报 | B | 已证实功能描述 |
| 2007 手机端可按条件搜索、看自述/择偶要求/相册 | Widsets/CNMO 厂商稿 | A/B | 功能宣布已证实；实际使用规模未知 |
| 2011 百合实行前台匿名、后台实名 | 央广 / 财新 | B | 已证实制度描述 |
| 婚恋成功会造成系统性 archive survivorship bias | 方法推断 | D | 待验证 |
| 2007 世纪佳缘普通用户必须联系客服才能注销 | 百度知道个案 | C | 仅 lead，不作为结论 |
| 2007 活动页历史 HTML/DOM/charset 已恢复 | 无 | — | **未达到** |

---

## 19. 下一步最小任务

优先级不是继续找更多成功故事，而是提升 artifact 质量。

1. 对 `love21cn.com` 和 `/xiangqin/index.html` 做 archive index probe，实际打开可用 Memento。
2. 若有 capture，记录 capture datetime、HTTP/replay、charset、DOM、CSS/JS/image completeness。
3. 寻找 2006—2008 官方 help / FAQ：注册、搜索、隐藏、注销、“找到对象”、站内信、认证。
4. 查 `robots.txt`、历史 sitemap / search URLs，确定个人 profile 的 URL pattern，但不批量抓取普通人 profile。
5. 寻找“佳缘通”的产品说明或电信实现材料，确认 relay 是 event-only 还是站内长期能力。
6. 查 Widsets 世纪佳缘 widget 的 package / binary / screenshots，建立 desktop-Web vs mobile-client representation。
7. 若能找到两个历史时点，再考虑把该对象升级为 M1 candidate；在此之前保持 research note。

---

## 20. 本轮对 OWA 方法的新增

这不是第 N 个抽象的 `page != transaction` 变体。

它增加了几个可直接用于后续 archaeology 的具体对象：

- `profile-to-person state gap`：历史 profile 不等于现实人的永久状态；
- `candidate-pool state invisibility`：search form 不保存当时真正可搜索的候选集合；
- `verification-state gap`：badge 与后台认证事务必须分开；
- `contact-relay layer`：匿名 / 中继联系方式有独立后台状态；
- `offline event projection`：Web profile 可以打印成物理事件基础设施；
- `relationship-state semantics`：中意、联系、见面、关系、婚姻不是一个“成功”字段；
- `contact-entitlement state`：付费 / 邮票 / 权限改变谁能真正联系谁；
- `termination success paradox`：对于目标是“离开平台”的服务，成功本身可能制造保存偏差。

这些机制决定了一个旧婚恋网站即使首页恢复得很好，仍然离“恢复当时一个普通人怎样找对象”很远。

真正需要恢复的是：

```text
谁当时可见
→ 为什么出现在结果里
→ 哪些字段只是自述、哪些经过验证
→ 怎样从 profile 进入第一次联系
→ 哪些联系经过平台、电话中继或线下活动
→ 关系形成后账号怎样退出可观察系统
```

这才是这个历史平台的运行世界。