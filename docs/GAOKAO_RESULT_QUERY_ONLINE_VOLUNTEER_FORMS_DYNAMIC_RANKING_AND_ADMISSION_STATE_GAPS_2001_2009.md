# Gaokao Result Queries, Online Volunteer Forms, Dynamic Ranking, and Admission-State Gaps, 2001–2009

> Scope: 约 2001–2009 年中文互联网中的高考成绩/录取查询页、招生信息服务、网上填报志愿、动态排名、征集志愿与线上—线下确认流程。研究对象不是“中国高考史”，也不是今天的志愿填报 App，而是一个旧网执行问题：**当历史页面上出现“查询”“保存”“提交”“确认”时，究竟证明到哪一个状态？一个网页 capture 能不能证明某个考生的志愿真正生效、被投档、录取并最终报到？**

普通生活、考试日历、“上岸”与四种未来时间感另见 `tmzncty/how-people-lived`：

- `topics/education-application-portals-admission-calendars-and-exam-route-loops-china-1999-2024.zh-CN.md`

本文件遵守 `docs/METHOD.md`：platform / query page / form / candidate account / backend record / rank snapshot / admission decision / notification / capture / claim 不混写；`exists / available / submitted / effective / admitted / enrolled` 不互相替代。

---

## 1. 为什么招生 Web 是一种典型的“公开壳留下，决定人生的状态消失”系统

旧网档案较容易保存：

- 招生政策页；
- 学校/专业计划；
- 成绩查询入口；
- 录取查询入口；
- 网上志愿操作说明；
- 登录页；
- 表单字段与按钮；
- 历年分数/排名查询工具；
- 招生咨询公告。

但一个真实考生经历的是：

```text
取得报名资格
→ 获得考生号/密码/证件
→ 考试
→ 成绩形成
→ 通过纸/电话/Web 得知成绩
→ 理解自己所在排名和可选学校
→ 填志愿草表
→ 登录
→ 输入志愿
→ 保存
→ 查询是否保存
→ 修改
→ 最终确认
→ 可能打印/签名
→ 截止时间到达
→ 招生后台读取有效志愿
→ 投档
→ 学校阅档/录退
→ 征集志愿（若需要）
→ 正式录取
→ 通知书送达
→ 本人决定报到或放弃
→ 实际入学
```

公共 Web 只覆盖其中一部分。

因此必须固定：

```text
query page exists != historical backend reachable
form rendered != candidate eligible
fields filled != saved
saved != confirmed
confirmed online != effective where offline signature required
rank snapshot != cutoff rank
投档 != admission
admission query result != official notice
admission != enrollment
```

---

## 2. 研究单位必须拆开

### 2.1 admissions backend

省级招办、高校之间传输考生电子档案、计划、投档和录退状态的内部系统。

它可以早于普通考生的 Web 自助界面。

### 2.2 public information page

政策、计划、学校/专业介绍、录取日程等公开页面。

只证明信息被公开，不证明考生看到。

### 2.3 result-query form

输入考生号/准考证号后查询成绩或录取结果的公共入口。

页面壳可以长期存活，但查询数据库可能早已关闭。

### 2.4 volunteer / preference form

用于填报学校与专业志愿的交互页面。

应继续拆分：

```text
draft
saved
reloaded
modified
final-confirmed
locked
expired
```

### 2.5 dynamic rank state

某个历史时刻的报考人数、本人位次、专业/院校排名、预计线等。

这是**时间状态**，不是一个静态页面属性。

### 2.6 offline confirmation artifact

打印志愿表、签名、报名点确认等。

不能因为网络表单已提交就省略。

### 2.7 admission decision

投档、预录取、院校在阅、录取、退档等后台状态。

### 2.8 official notification / enrollment

录取通知书、报到与注册。

它们属于 Web 之后的现实结果。

---

## 3. 最小 execution state machine

以后遇到“2008 年某考生网上填了某大学”的 claim，至少尝试区分：

```text
A0 route / school / major exists
A1 candidate is eligible for this batch/category
A2 candidate obtains credentials/password
A3 public information is reachable
A4 historical client can render login/form
A5 candidate logs in
A6 current backend session is valid
A7 volunteer fields are entered
A8 data are saved
A9 candidate re-queries and verifies saved state
A10 data may be modified before lock/cutoff
A11 candidate performs final confirmation if required
A12 offline print/signature/registration-point confirmation completes if required
A13 deadline passes and effective record is frozen
A14 admissions backend accepts the effective preference record
A15 candidate is ranked /投档
A16 institution reads file
A17 institution admits/rejects/requests adjustment
A18 candidate receives query result
A19 official admission notice is produced/delivered
A20 candidate accepts in practice and enrolls
```

必须固定：

```text
public page != personal state
personal state != final state
save != confirm
online confirm != offline signature
current rank != final rank
query result != legal/official artifact where page itself says so
admitted != enrolled
```

---

## 4. E1 — 2001：网上录取首先是招生后台网络化，不是“所有考生网上报名”

教育部 2001 年通知规定，全国各省区市普通高校招生实行网上录取，包括现场局域网录取和远程广域网录取，并提高远程录取比例。

Source:

- 教育部办公厅，教学厅〔2001〕1号：<https://www.moe.gov.cn/jyb_xxgk/gk_gbgg/moe_0/moe_7/moe_12/tnull_5936.html>

Grade: **A**。

Supported claims:

- 2001 年普通高校招生后台已明确进入全国性网上录取建设阶段；
- onsite LAN 与 remote WAN 是两个不同执行环境。

NOT supported:

- 普通考生当年自己在浏览器里完成全部志愿/录取流程；
- 所有学校、家庭已具有稳定 Internet access；
- 某个考生录取结果可由今天公开网页完整重放。

必须固定：

> `backend digitization != public-web transaction`

---

## 5. E2 — 2001 新浪录取查询：历史 form shell 仍活着，但它自己就声明不是最终权威记录

今天仍可打开新浪教育旧页：

- 标题为“2001年高考北京地区考生录取情况网上查询”；
- 有“请输入您的考生号”字段；
- 文字说明覆盖提前、第一批、第二批和专科录取情况；
- 页面标出数据最后更新时间为 `2001年8月27日18:31`；
- 明确声明网页信息只供参考，正式录取以考生收到的录取通知单为准。

Source:

- <https://edu.sina.com.cn/act/luqu.html>

Grade: **A/B boundary**。

这是一个很有价值的 old-web artifact，但只能支持：

> 该历史查询页面壳与当时的公开声明今天仍可观察。

本轮**没有**：

- 用真实考生号查询；
- 构造/猜测考生号测试后台；
- 证明 2001 查询数据库今天仍连接；
- 证明页面当前的 HTML、服务器端代码与 2001 完全未变；
- 复原任何普通考生的历史结果。

这产生 **form-shell survival gap**：

> 页面看起来仍“能输入”，不代表二十五年前的后台状态仍存在。

同时产生 **authority gap**：

> 页面自己已经告诉研究者，网页结果与正式录取通知书不是同一个权威层级。

---

## 6. E3 — 2003：历史数据查询已经带 paywall / login-time entitlement

2003 年北京教育考试院与通信公司合作的高考录取资料网上查询系统提供：

- 1999–2002 历年高校在京录取统计；
- 成绩分布；
- 分数与排名关系；
- 个人分数在地区及拟报学校历史录取中的排名比较。

报道还写明：

- 需购买 10 元“门票”；
- 门票当天有效；
- 有登录次数限制；
- 可通过不同拨号/ADSL/LAN 接入渠道进入服务；
- 同时仍提供 160 声讯和短信查分。

Source:

- 中国教育在线保存的同期报道：<https://gaokao.eol.cn/news/200603/t20060323_76739.shtml>

Grade: **B**。

这意味着一个旧网页即使被完整 capture，也未必能复原历史体验，因为当时还可能依赖：

```text
access-network entitlement
+ paid ticket
+ session/login counter
+ historical query database
```

新增：**entitlement-state gap**。

同时：

> `historical-data query tool != admissions decision engine`

它帮助判断，不替代正式志愿与投档。

---

## 7. E4 — 2008 广东：网上填了，但不去线下签字，志愿仍可无效

广东省考试中心 2008 年通知明确：

1. 考生先通过网上填报系统填学校和专业；
2. 再在规定时间到报名点办理签名确认；
3. 逾期未确认，网上志愿信息无效；
4. 不同分数段在不同时间窗口上网填报。

Source:

- 阳光高考保存的广东省考试中心通知：<https://gaokao.chsi.com.cn/gkxx/ss/200806/20080630/7451025.html>

Grade: **A**。

这是 old-web execution archaeology 的关键边界：

```text
browser submission
→ offline signature
→ effective preference
```

因此不能从：

> “服务器日志里出现某次保存”

直接写成：

> “该考生最终有效填报了这一志愿”。

新增：**offline-confirmation handoff gap**。

---

## 8. E5 — 2009 湖北：未来路线受 session timeout 约束

《湖北日报》2009 年同期操作指引记录：

- 每次登录网上志愿系统，填报时间为 30 分钟；
- 超时自动退出；
- 需要继续填/改时，15 分钟后可再登录；
- 每批志愿完成后要点击“保存”；
- 离开时要“安全退出”；
- 推荐关闭页面后再次登录，通过“查询志愿”检查是否真正保存。

Source:

- 高考资讯网保存的《湖北日报》稿：<https://www.gkzxw.com/Article/200906/34145.html>

Grade: **B**。

这使历史 Web 的 runtime 条件非常具体：

```text
form visibility
!= valid authenticated session
!= save completed before timeout
```

而现代 archive 通常不会保存：

- 历史 session cookie；
- authentication backend；
- 30 分钟倒计时状态；
- 当次保存 ACK；
- “查询志愿”重新读回的个人结果。

新增：**session-runtime gap** 与 **save-ack gap**。

---

## 9. E6 — 2009 河南：同一年、同一省内也能出现纸卡与 Web 并存

河南 2009 考生指南记录：

- 普通高校招生全国统考类考生的**原始志愿**仍采取填涂志愿卡；
- 对口招生、专升本原始志愿，以及录取期间各类征集/补录志愿实行网上填报；
- 网上系统使用准考证号与初始密码；
- 正式开通前还设置了演练时间。

Source:

- <https://gaokao.chsi.com.cn/gkxx/ss/200906/20090614/25817549.html>

Grade: **B**（同期考生指南转载）。

必须固定：

> `online volunteer filling existed in a province != every volunteer stage in that province was online`

所以按年份画一条“纸质 → 网上”的单线时间轴会丢失真实混合态。

新增：**workflow-scope gap**。

---

## 10. E7 — 2008 内蒙古：动态排名是一类 archive 极难保存的“流动网页状态”

内蒙古实时网上填报志愿允许考生根据：

- 自己的实时排名；
- 院校/专业计划数；
- 当前报考人数；
- 预计分数线等；

不断修改志愿直到本人分数段截止。

教育系统保存的工作材料记录：

- 本科各批次平台累计提供 108 小时动态排名；
- 110154 人次在线填报；
- 累计修改志愿 6,441,829 次；
- 平均每人次修改约 58 次；
- 采用高分段先结束、低分段后结束的分时策略。

Source:

- 教育部旧站保存材料：<https://www.moe.gov.cn/jyb_xwfb/s6192/s222/moe_1736/201004/t20100420_85708.html>

Grade: **A/B**。

这产生本轮最重要的新 archive gap：**mutable-ranking time collapse（可变排名的时间坍缩）**。

一个静态 capture 即使抓到了：

```text
某院校 14:00 的排名页
```

也不能自动证明：

```text
14:05 的排名
15:00 分数段截止时的排名
该考生最后一次看到的排名
该考生最后一次保存的志愿
最终投档时的排序
```

尤其不能把今天残留的一张榜单截图写成“当年最终状态”。

这一类 Web 最接近：

> **历史对象不是页面，而是一个不断变动的状态流。**

传统页面 archive 对这种对象天然不完整。

---

## 11. E8 — 2009 陕西征集志愿：在线截止与线下确认是两个不同 deadline

陕西 2009 二批征集志愿材料记录：

- 网上征集志愿有明确提交截止；
- 随后考生还必须在更晚但同样严格的截止前，到县区招办或指定地点签字确认；
- 才进入后续投档流程。

Source:

- 阳光高考保存同期报道：<https://gaokao.chsi.com.cn/gkxx/ss/200907/20090724/28758260.html>

Grade: **B**。

它揭示 **multi-deadline state machine**：

```text
online deadline
!= offline confirmation deadline
!=投档 deadline
```

所以“在截止前提交了网页表单”仍可能不是最终有效状态。

---

## 12. 一组应固定进入仓库的方法术语

### 12.1 form-shell gap

表单壳存活，但历史 backend / database 不再可执行。

### 12.2 auth / entitlement gap

当时需要考生号、密码、付费门票、特定资格或账户状态；archive 不保存这些私人/动态状态。

### 12.3 save / confirm gap

保存不是最终确认。

### 12.4 offline-confirmation handoff gap

Web 成功后仍可能依赖打印、签字、报名点确认。

### 12.5 deadline-state gap

历史 deadline 一旦过去，今天回放页面不能重建“当时还剩几分钟”的制度状态。

### 12.6 session-runtime gap

登录状态、cookie、timeout、后端 session 不随静态 HTML 存活。

### 12.7 mutable-ranking time-collapse gap

实时排名和计划状态连续变化，单个 capture 只代表一个瞬间。

### 12.8 cross-channel divergence gap

电话、短信、Web、纸通知可能同时提供相近信息，但权威性、更新时间和可执行作用不同。

### 12.9 backend投档 gap

公开志愿页不能显示完整投档、阅档、录退内部状态。

### 12.10 admission-notice authority gap

公开查询结果与正式录取通知书/注册记录可能是不同权威层级。

### 12.11 enrollment-outcome gap

被录取不代表报到。

### 12.12 candidate-privacy gap

为了证明平台结构，不需要也不应恢复普通考生完整准考证号、身份证号、历史志愿、家庭联系方式与录取轨迹。

---

## 13. 浏览器、编码与执行环境：本轮明确不猜

本轮没有可靠取得 2008 内蒙古、2008 广东或 2009 湖北志愿后台的完整 A 级 WARC / 原始 HTML + CSS + JS + 服务器交互记录。

因此不写：

- “系统一定只支持 IE6”；
- “一定使用 GBK/GB2312”；
- “某按钮一定由某段 JavaScript 实现”；
- “当前能打开的页面就是历史浏览器所见”；
- “今天页面表单仍能提交，所以历史 backend 可用”。

若未来取得原始 capture，至少应记录：

- Original URL；
- capture datetime；
- Content-Type / charset；
- form action；
- method；
- script dependencies；
- cookie/session requirement；
- timeout；
- 是否 iframe/frameset；
- 是否依赖 ActiveX/旧证书/特定浏览器；
- 后端返回是否只是 archive rewrite。

---

## 14. 负结果：本轮没有恢复什么

### 没有恢复 2008 内蒙古实时排名流

找到了官方/教育系统对运行机制和统计的同时代/近同时代记录，但没有取得一个足以重放：

```text
candidate login
→ live rank
→ repeated refresh
→ one modification
→ later rank
→ cutoff
```

的完整历史 session。

因此只能建立状态模型，不能声称复原了当年 UI/交互。

### 没有恢复普通考生完整个人志愿链

这既是证据缺失，也是隐私边界。

即使搜索引擎或旧页偶然暴露历史准考证号、姓名、联系方式，也不应为了证明状态机而重新聚合。

### 没有证明新浪 2001 查询后台仍可执行

只确认公开历史页面壳、字段、数据更新时间与“仅供参考”的声明仍可观察。

---

## 15. 保存偏差

### 15.1 instruction survival bias

官方说明、帮助页和新闻稿比真实个人 session 更容易留下。

因此 archive 容易让后人误以为“制度说明 = 每个人都按说明成功操作”。

### 15.2 static-page bias

静态招生章程和新闻页保存率高；实时排名、库存/计划、个人志愿版本、后台投档状态保存率低。

### 15.3 failure/complaint visibility

忘密码、超时、确认失败、系统拥堵更容易进入新闻和论坛；顺利填完并录取的普通人反而可能什么都不写。

不能用幸存投诉估系统失败率。

### 15.4 success-disappearance

真正成功以后，考生不会长期保留一个“我当年填了什么、改了多少次、网页返回了什么”的公开档案。

历史结果往往只剩“后来去了某大学”，中间执行链消失。

---

## 16. 与普通生活史的交叉链接

这些 Web 状态之所以值得研究，不是因为表单本身重要，而是因为它们把一个人的生活分流到：

- 不同学校；
- 不同专业；
- 不同城市；
- 不同家庭支出；
- 不同迁移路线；
- 不同毕业年份；
- 后来的考研、求职、婚恋和住房项目。

因此旧网 claim 最好始终停在它能证明的层级：

> **我们可以证明一个未来当时怎样被输入系统；除非有额外证据，不能仅凭网页证明那个未来最终被生活出来了。**

---

## 17. 下一步高价值对象

优先级最高的不是再找一个“某省首次网上填报”新闻，而是：

1. 一个 2001–2009 有明确 timestamp 的原始成绩/录取查询 capture；
2. 一个真实但经过隐私最小化的多时点志愿执行链；
3. 2008 内蒙古实时动态排名系统的历史截图/HTML/技术手册，最好能证明两个不同时间点的状态变化；
4. 2008–2009 某省完整的用户操作手册，包含 login、save、confirm、timeout、signature 和 error states；
5. 一组能区分“网上填报成功”和“最终未报到”的公开、非敏感同期材料。

若只能找到后来的怀旧回忆，不要补绘 UI；若涉及普通人的准考证号、身份证、完整志愿或录取档案，宁可保留状态缺口，也不重新公开。
