# 业余无线电呼号、论坛、设台申请与真实 RF 通联：中文旧 Web 状态缺口（2000—2015）

> Scope：只研究约 2000—2015 年中文 Web 怎样承载业余无线电爱好者的呼号身份、论坛讨论、技术资料、邮件选编、设台/办证信息、设备 DIY 和活动协调，以及这些公开网页状态与**真实持证、真实架台、真实发射、真实 QSO**之间的缺口。
>
> 不把本文件扩成中国 1980s—1990s 业余无线电制度史，也不写成全球 packet-radio / amateur-radio 通史。前史、生活成本和跨国比较进入 companion：[`tmzncty/how-people-lived/topics/amateur-radio-hobby-parallel-infrastructure-callsign-identity-and-network-succession-china-1981-2026.zh-CN.md`](https://github.com/tmzncty/how-people-lived/blob/main/topics/amateur-radio-hobby-parallel-infrastructure-callsign-identity-and-network-succession-china-1981-2026.zh-CN.md)

本题不是“老火腿论坛怀旧”。它要回答：今天打开一个标注 2004 年的 HelloCQ 帖、一个 QSL.net 呼号主页、一个 2009 年办证攻略，究竟能证明当年用户真实生活到了哪一步？

---

## 1. 研究单位：呼号、论坛账号、网页和电台不是同一个东西

至少区分：

- amateur-radio service / 业余业务；
- operator qualification / 操作技术能力；
- station licence / 电台执照；
- callsign / 呼号；
- physical station / 真实电台设备；
- antenna / feedline / power / 天馈电源；
- platform / forum / email list；
- host / domain；
- user account；
- callsign field in profile；
- personal homepage / QSL page；
- thread / post / reply；
- attachment / schematic / firmware / image；
- application form / download page；
- status-query page；
- QSO / 真实双向通联；
- QSL / log / contest result；
- current live legacy page；
- historical archive capture。

固定边界：

```text
论坛账号 ≠ 持证操作员
profile 写了呼号 ≠ 身份已经独立验证
呼号曾存在 ≠ 当前电台执照一定有效
操作能力证书 ≠ 某一具体电台已经获准设置
电台执照 ≠ 用户此刻在发射
帖子说“抄收” ≠ archive 自己能验证 RF 信号
活动公告 ≠ 活动真实举行
QSO log ≠ 对方独立确认
QSL 页面存在 ≠ 实体 QSL 卡已经交换
current live old post ≠ historical Web representation
```

---

## 2. 三条不同状态机不能压成“上论坛玩无线电”

### 2.1 身份状态机

```text
产生兴趣
→ 获得操作资格（制度随年份变化）
→ 设置/使用电台获许可
→ 获得/使用呼号
→ 在论坛/主页填写呼号
→ 他人按呼号识别该用户
→ 论坛账号、主页和呼号可能持续多年
```

### 2.2 Web 行政状态机

2009 个案至少显示：

```text
找到办证说明
→ 下载表格/试题
→ 打印
→ 手写/填表
→ 邮政汇款
→ EMS 寄材料
→ 收到证件/表格
→ 本地窗口递交设台材料
→ 获得回执
→ 回家上网查进度
→ online status = success
→ 再到现场
→ 银行缴费
→ 领取电台执照
```

所以：

```text
download page exists
≠ application submitted
≠ operator qualification granted
≠ station licence granted
≠ callsign assigned
≠ station physically installed
≠ lawful transmission occurred
```

### 2.3 技术实践状态机

```text
论坛/邮件看到方案
→ 下载正文/图片/附件
→ 找零件
→ 制作/刷固件
→ 安装
→ 测试
→ 调谐
→ 接入真实电台
→ 发射/接收
→ 完成 QSO 或失败
→ 回论坛写结果
```

因此：

`thread survives ≠ attachment survives ≠ build happened ≠ build worked ≠ RF result succeeded`。

---

## 3. 2004：QSL.net + HelloCQ + 邮件选编已经形成跨平台 hobby knowledge chain

QSL.net 当前仍保存《业余电台中文邮件选编》第 195 期，页面标注 2004-08-21。目录明确写有：

- “哈罗CQ广播爱好者各 HAM/BCL 论坛”；
- 协会消息；
- “酷站链接”；
- 本选编 / ChinaHam 各讨论组订退办法；
- 并注明“感谢 http://www.hellocq.net 发行”。

其中保存一条来源定位很清楚的论坛材料：

```text
HelloCQ 火腿社区
数字和空间通信版
2004-08-15
BG4REB
“都来听听 AO51”
原帖 locator:
http://www.hellocq.net/forum/showthread.php?t=94979
```

正文说作者此前为 UO-14 做过 2 米和 70 cm 八木天线，花了几个月工作之余的时间；后来用于实际活动，并在 AO-51 可用后继续通联实验。

来源：

- current QSL.net legacy text：<https://www.qsl.net/bd7as/zazhi/195.htm>

### 证据状态

本轮可以可靠记录：

```text
current legacy page
carrying text dated 2004-08-21
which itself preserves a forum locator and post dated 2004-08-15
```

不能写：

```text
we verified the original HelloCQ 2004 HTML / DOM / CSS / charset
```

因为本轮**没有**打开并验证 `showthread.php?t=94979` 的历史 memento。

### 新的 archive 结构：republication chain

这里不是单一网页，而是：

```text
论坛原帖
→ 邮件/编辑选编
→ QSL.net legacy archive
→ 今天的搜索引擎
```

后两个节点可能在原论坛消失以后继续保存文字。

可称为：

**republication survival chain / 再发布存活链**。

它既能救回内容，也会丢失：

- 原楼层结构；
- 回复；
- 头像/签名；
- 原附件；
- 图片；
- 编辑记录；
- 登录状态；
- 原论坛模板；
- 当时的用户资料。

所以“文字幸存”不等于“论坛对象幸存”。

---

## 4. 邮件选编证明：论坛、邮件列表和 Web 在 2000s 可以并存，而不是线性替代

同一批《业余电台中文邮件选编》目录反复把：

```text
forum discussion
+ ChinaHam discussion groups
+ association information
+ useful-site links
+ email subscription instructions
```

装进一个传播包。

例如第 200 期（2004-10-11）继续列出 HelloCQ 多篇论坛话题、应急通信活动、HAM/BCL 站点链接和讨论组订退。

来源：

- <https://qsl.net/b/bd7as/zazhi/200.htm>

这对 old-Web 平台谱系是一个重要反例：

**“论坛时代”并不意味着 email-list 已经死掉。**

同一个人可能：

1. 在论坛发帖；
2. 内容被邮件选编；
3. 邮件通过 discussion group 分发；
4. 选编再以静态 HTML 挂在 QSL.net；
5. 原论坛和转存站的存活周期完全不同。

因此以后做平台 genealogy 时，不能只画：

`BBS → Web forum → SNS`。

业余无线电这种技术社群更像：

`mailing list ∥ forum ∥ personal homepage ∥ QSL archive ∥ RF network`。

---

## 5. 2009 汽车之家办证攻略：一份网页可以保存跨媒介事务链，但不能证明每一步后台状态

汽车之家当前可访问一篇页面标注 **2009-06-28 12:08:52** 的帖子：

`领航呼叫车队-申请呼号、办理电台执照完全攻略`

current locator：

<https://club.autohome.com.cn/bbs/thread/f651044e4514449a/3534641-1.html>

首帖按日期记录：

### 2009-05-14

- 从中国无线电运动协会网站下载入会申请表；
- 下载个人业余电台申请表；
- 从天津无线电运动协会网站下载四级考题；
- 打印试题，答案要求手写；
- 准备照片和身份证明复印件。

### 后续

作者继续记录邮局汇款、复印汇款单、EMS 邮寄材料、收到协会/操作证材料与呼号、本地办事窗口提交设备数据、取得回执、回家上网查进度、网上显示办理成功后再次到现场、去附近银行缴费、领取电台执照等环节。

作者称整个过程历时 30 多天，总支出 241 元。

### 证据等级

这是：

**current live platform page carrying a user post dated 2009**。

它非常适合证明：

- 这位作者当时如何理解和记录自己的办事流程；
- Web 已经承担表格下载和进度查询；
- 事务仍然跨越纸、邮政、窗口和银行。

它不能证明：

- 2009 年所有地区流程相同；
- 当前汽车之家 DOM 就是 2009 DOM；
- 当前账号等级、点赞、推荐、热帖算法字段属于 2009；
- 原图片今天仍以原文件/原压缩参数保存；
- 网上进度页的 backend response、数据库状态和鉴权机制已经被 archive 保存。

---

## 6. legacy rendering temporal collapse：今天看到的“2009 帖”可能同时含 2020s 页面状态

汽车之家当前页面在同一个画面里可能出现：

```text
2009 正文时间戳
+ 今天的平台导航
+ 当前用户状态
+ 当前推荐/热度算法
+ 当前 CSS/JS
+ 后来迁移后的图片服务
```

如果研究者整页截图并标成“2009 年汽车之家论坛长这样”，就会制造假历史。

因此增加字段：

```yaml
content_timestamp: 2009-06-28
current_renderer_observed_at: 2026-09-07
historical_renderer_verified: false
mutable_fields:
  - account_stats
  - popularity/recommendation fields
  - navigation
  - ad slots
  - image CDN path
```

可称为：

**legacy-render temporal collapse / 遗留页面时间塌缩**。

这一问题与 Hi-Fi、摄影老帖完全一致，说明它应成为 old-Web 的通用方法条目。

---

## 7. 呼号字段会制造一种特别危险的“身份自动验证”错觉

业余无线电论坛常见：

- username 本身就是呼号；
- profile 有 callsign 字段；
- signature 有呼号、设备清单；
- 个人主页以呼号为标题；
- QSL.net path 也可能围绕呼号组织。

但是历史研究必须继续拆：

```text
页面声称 callsign = X
≠
研究者已独立验证该账号控制者就是该持证人
```

还要区分：

```text
某呼号在某时期被指配
≠
同一呼号永远对应同一现实状态
```

不同制度时期的呼号回收、重新指配、执照失效和账号继承/盗用都可能改变解释。

因此推荐字段：

```yaml
claimed_callsign: BGxXXX
claim_source: username | profile | signature | post_body | external_registry
registry_verified_at: null
historical_assignment_verified: false
```

若只是论坛 profile，写 **claimed callsign**，不要直接写“该用户真实呼号”。

---

## 8. current personal homepage ≠ historical personal homepage

QSL.net 等长期托管环境非常容易产生错觉：看到一个“老派 HTML”页面，就自动认为它是 1990s/2000s 原样保留下来的网页。

必须区分：

- current URL path；
- 页面正文自述的时间；
- 文件 Last-Modified（若可靠）；
- archive capture datetime；
- 外链/图片的创建时间；
- 当前 host 迁移和重写。

即使个人主页正文说“1994 入会、1995 考证”，它首先证明的是：

`当前页面这样叙述自己的历史`。

要证明 1998 年页面已经写了这些内容，仍然需要 1998 capture 或其他同时代 evidence family。

增加：

**retro-styled page dating gap / 老式页面年代判定缺口**。

---

## 9. 技术帖子有比普通论坛更严重的 attachment survival gap

无线电 DIY 可能依赖：

- 电路图；
- PCB；
- 天线尺寸图；
- Smith chart / 测量结果；
- 固件；
- 频率表；
- 软件；
- 串口/编程工具；
- 图片托管站；
- zip/rar 附件。

因此：

```text
thread HTML preserved
→ attachment metadata preserved?
→ attachment file preserved?
→ image host alive?
→ download requires login?
→ archive saved binary?
→ version identifiable?
→ external software dependency still obtainable?
```

一篇“八木制作成功”的帖子如果只剩尺寸讨论、原图全部消失，历史学家并不能说“制作方案已经完整保存”。

可复用此前 Hi-Fi / photography 已出现的：

**technical-attachment survival gap / 技术附件存活缺口**。

但无线电还多一层：即使电路图和照片全在，**RF performance 仍然不可由 HTML 自动验证**。

---

## 10. online text / physical RF gap：网页最难保存的恰恰是核心行为

业余无线电 Web 的根本保存偏差是：

**真正的 QSO 并不发生在 Web 上。**

Web 可能留下：

- “今晚 20:00 某频率 CQ”；
- “刚才抄到 XX”；
- QSO log；
- QSL scan；
- 活动结果；
- contest score；
- 天线照片。

但现实过程是：

```text
设备上电
→ 频率/模式设置
→ 天线真实存在并工作
→ 传播条件允许
→ 发射
→ 信号跨空间
→ 对方接收
→ 对方回应
→ 本台接收
→ QSO 完成
```

普通网页 archive 通常没有：

- IQ/raw RF recording；
- 当时频谱；
- 发射功率实际值；
- 天线驻波；
- 对方台独立日志；
- 实时传播条件；
- 未成功的呼叫。

因此增加本题最重要的 hard boundary：

```text
post says QSO happened
≠ archive independently proves RF path
```

这不是说用户自述无效，而是必须把 evidence type 写清楚。

---

## 11. 2000s old-Web 的“Internet + radio”并不是二选一

业余无线电特别适合修正一种常见的技术史叙事：

```text
旧媒介
→ 被 Internet 替代
```

实际 2004—2009 可见的结构更像：

```text
RF hobby
+ email list
+ Web forum
+ QSL static site
+ postal mail
+ association website
+ government/association forms
+ phone/QQ/offline meetups
```

这些层可以同时工作。

Internet 往往负责：

- 找资料；
- 查设备；
- 讨论天线；
- 下载表格；
- 查行政状态；
- 协调活动；
- 保存通联后的文本/照片；

RF 则负责核心无线电实践。

所以 old-Web companion 不应把“HAM 上网”理解成“HAM 停止玩无线电”。

---

## 12. 海外方法对照：TAPR 的 CompuServe → email → Web/FTP 迁移证明“平台继替”可以发生在一个未消失的 hobby 上

本仓不把 TAPR 写成主研究对象；这里只借它验证一种解释框架。

TAPR 官方历史记录：

- 1982：早期 amateur packet QSO；
- mid-1980s：组织使用 CompuServe message boards；
- 1992：加入 Internet，用 email distribution 取代 CompuServe boards；
- 1993：email list 与 email 软件请求；
- 1995：第一批 Web pages；
- 1995：原先通过办公室/会议购买软盘获得的软件库迁到 FTP。

来源：

- <https://tapr.org/history/>

这说明一个 old-Web genealogy 可以是：

```text
同一个兴趣实践保持
而 coordination / distribution layer 更换
```

而不是：

```text
新网络出现
→ 旧 hobby 消失
```

对中文业余无线电，未来应特别寻找：ChinaHam / HelloCQ / 邮件列表 / QSL.net / QQ 群之间是否也有可验证的类似迁移链。

---

## 13. 本轮 archive search 状态：M1 NOT ACHIEVED

本轮已经获得：

1. current QSL.net legacy text，承载 2004 邮件选编和 HelloCQ historical locator；
2. current AutoHome legacy page，承载 2009 第一人称办证流程；
3. current HelloCQ/相关站点可见性线索；
4. 多个 contemporaneous locator、host 和 thread pattern。

但本轮**没有取得并实际检查**一份满足 M1 门槛的 2000—2010 中文业余无线电论坛/个人主页 transaction memento。

因此以下内容全部保持 `unknown / unverified`：

- 2004 HelloCQ 原 thread DOM；
- 原 charset；
- 当时论坛软件和版本；
- 原 CSS / JS；
- 登录/cookie/session；
- attachment URL pattern；
- 图片 host；
- 原帖分页和楼层结构；
- 当时 profile schema；
- 2009 申请网站 form action / GET/POST；
- 状态查询接口与 backend；
- 历史证件下载/上传流程；
- 当时是否 IE-only / ActiveX；
- historical mobile rendering。

固定措辞：

**`M1 NOT ACHIEVED IN THIS SLICE`**。

不能写“Wayback 没有”，因为本轮只证明**没有成功取得 verified capture**，不是证明 archive 中不存在任何 memento。

---

## 14. 本题新增的 archive-gap vocabulary

### callsign-account identity gap

`profile 呼号 ≠ 已验证现实持证人`。

### licence-to-air gap

`执照状态 ≠ 实际 RF 发射/通联`。

### web-to-paper/postal handoff gap

网页流程中途转到打印、手写、汇款、EMS、窗口、银行以后，Web archive 无法独立保存全事务。

### online-status/backend gap

“查询成功”页面如果没有请求/响应和账号后台，不能证明数据库如何判断、何时变更。

### republication survival chain

原论坛内容可能通过邮件选编、静态站转载而存活，但原上下文/附件/互动消失。

### technical-attachment survival gap

正文存活不等于电路图、固件、天线图、程序仍在。

### public-thread/private-QSO gap

公开讨论最容易存，真正的无线电行为和私下协调最难存。

### legacy-render temporal collapse

旧正文 + 当前模板/账号字段被错误压成一个历史时点。

### online-admin / physical-RF gap

行政层可以完全数字化，电台实践仍然是物理过程。

---

## 15. 已证实 / 高概率 / 不知道

### 已证实

- 2004 年的当前 QSL.net legacy page 保存一份标注日期明确的业余电台中文邮件选编，并给出 HelloCQ 原帖 locator、ChinaHam 讨论组和网站链接等传播结构。
- 当前汽车之家页面保留一篇标注 2009-06-28 的用户攻略，正文记录 Web 下载/查询与纸张、邮政、窗口、银行混合的办证路径。
- 这些材料足够证明 2000s 中文 Web 是业余无线电知识、办事信息和社群协调的一层基础设施。

### 高概率、仍需 capture 加强

- HelloCQ 在 2004 已承担数字/空间通信等技术版块及大量用户讨论；现有二次保存链很强，但原页面结构尚未验证。
- 早期 QSL.net / 呼号个人主页可能承担长期个人身份和资料索引，但每个具体页面需要独立年代验证。

### 不知道

- 原始 historical UI、DOM、CSS、charset、插件、cookie/session；
- 原附件的完整存活率；
- forum username 与 callsign 的身份核验率；
- 原帖中自述 QSO 与对方日志的交叉确认率；
- 论坛用户中真正持证、实际长期发射的人口比例；
- 旧论坛私信/QQ/电话 handoff 后有多少真实活动和交易。

---

## 16. 隐私与版权边界

业余无线电是公开呼号传统较强的社群，但这不取消本仓隐私原则。

- 不批量抓取呼号与现实姓名、电话、住址的映射；
- 不因旧 callbook/论坛可访问就建立普通个人身份数据库；
- 引用普通用户帖子只保留支撑机制所需的最小信息；
- 不重新分发旧论坛附件、扫描 QSL 卡、证件照片和身份证明；
- 技术附件版权不明时只保存 locator、metadata、摘要；
- 对 current profile 的可变字段不倒灌到历史时点。

---

## 17. 下一步最小考古任务

1. 对 `hellocq.net/forum/showthread.php?t=94979` 搜索并**实际打开**多个历史 memento；
2. 定位 2004 前后的 HelloCQ board index、profile、attachment URL pattern；
3. 查 ChinaHam discussion group 是否有 mbox / mailing-list archive / 同期订阅说明；
4. 选一个 QSL.net 中国呼号个人主页，建立至少两个历史 capture 时点，检查 host/path/charset/外链变化；
5. 定位 2009 中国无线电运动协会下载表格和状态查询的 historical locator；
6. 如果得到 verified capture，再进入 M1 case，而不是继续堆 current legacy screenshots。
