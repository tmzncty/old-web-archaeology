# INTERNET CAFE / PUBLIC TERMINAL / IDENTITY / SESSION / BROWSER / SECURITY STATE GAPS, 1995–2015

## Scope

本笔记只处理约 1995–2015 中文互联网中的一个基础设施问题：

> 一个旧网页在公网存在，不等于普通人当时是在私人电脑上访问它。大量访问可能发生在网吧、公共电脑屋、学校机房、单位终端等共享机器上。

本文件不把仓库扩成全球网吧史。全球 Cyberia、Internet café 等只作为 how-people-lived 中的比较对象；这里关注中文旧网考古时，**访问环境本身如何改变页面可执行性、账号身份、安全、计费、浏览器条件以及今天的存档偏差**。

当前已有的旧网研究大多从远端对象出发：

`platform → host → page → account → capture → claim`

网吧要求补一条经常完全消失的本地链：

`physical venue → terminal/seat → venue identity record → billing session → OS/browser/client image → network path → web account/login → task → logout/local cleanup`。

如果不把两条链接起来，一个保存很好的 2006 网页仍可能让研究者误以为：用户拥有自己的电脑、可以自由安装插件、可以保存本地文件、可以安全输入银行卡密码、可以一直保持登录，甚至可以随时访问。

---

## 1. Minimum state model

研究网吧相关历史页面时，至少拆开以下对象：

1. **physical venue**：具体营业场所；
2. **venue operator / employee**：经营者或前台；
3. **terminal / seat**：用户实际使用的机器，不等于场所本身；
4. **real-world consumer**：现实中的上网者；
5. **identity document**：身份证等有效证件；
6. **venue identity record**：场所为监管/计费保存的身份记录；
7. **billing session**：某机位从何时开始、何时结束、费率为何；
8. **management client/server**：计费、实名、安全管理等场所软件；
9. **OS/browser image**：终端当时的 Windows、IE/其他浏览器、插件、输入法、证书和本地策略；
10. **installed client**：QQ、游戏客户端、下载工具等非 Web 软件；
11. **network session**：终端到公网的实际连接状态；
12. **web/platform account**：论坛、博客、QQ 空间、邮箱等远端账号；
13. **login session / cookie**：平台认证状态；
14. **page / service**：远端网页或事务；
15. **local file/cache/history**：下载文件、缓存、浏览历史、本地账号痕迹；
16. **task outcome**：发帖、聊天、付款、报名等现实事务结果；
17. **archive capture**：今天存档机构保存的远端页面表示。

### 必须保留的状态差

```text
venue exists
!= venue open at that hour
!= seat available
!= consumer admitted
!= identity accepted
!= billing session started
!= terminal has working network
!= target site reachable
!= target site renders correctly on that browser image
!= platform account can authenticate
!= authentication is safe on a shared terminal
!= task submitted
!= task completed
!= user logged out correctly
!= local traces were erased
!= later public archive captured any of the above local state
```

---

## 2. Public access is not household ownership

CNNIC 的历史序列要求首先把中国网络接入阶段分开。1986–1987 已有科研远程登录与国际电子邮件节点，但 1994-04-20 才实现与 Internet 的全功能连接；1995-01 起公共电信网络开始向社会提供 Internet 接入。[CNNIC 1986–1993](https://cnnic.cn/n4/2022/0401/c87-911.html)；[CNNIC 1994–1996](https://www3.cnnic.cn/n4/2022/0401/c87-912.html)

因此本仓不能用“1994 前没有网络”这种写法，也不能反过来把科研邮件写成普通公众已经能够去网吧上网。

后来的机构回顾对“第一家网吧”也不一致：中国电信博物馆和 2014 中新网行业史把 1995 年上海“3C+T 公众电脑屋”称为早期/首家公共上网营业场所，而新华社 2014 时间线把 1996 年北京“实华开网络咖啡屋”称为首个网吧。[中国电信博物馆](https://museum.chinatelecom.com.cn/yj/txkp/202204/t20220421_69310.html)；[中新网](https://www.chinanews.com/sh/2014/12-08/6853489.shtml)；[CCTV/新华社](https://news.cntv.cn/2014/04/20/ARTI1397961300443621.shtml)

**当前 claim：** 1995–1996 年上海、北京已出现面向公众出售联网终端使用时间的早期场所。

**当前不 claim：** 哪一家在严格定义下是“中国第一家网吧”。

这应成为一个 future M1/M2 小案例：先找同时代营业执照、报刊广告、价格单、原始网页或照片，再裁定“first”标签，而不是让后来机构回顾互相投票。

---

## 3. 2002 regulation proves a separate venue identity layer

2002 年国务院第 363 号令把“通过计算机等装置向公众提供互联网上网服务的网吧、电脑休闲室等营业性场所”定义为独立对象，并把学校、图书馆内部为特定对象提供上网的场所排除在这一营业场所定义之外。原条例要求营业场所核对、登记消费者的身份证等有效证件，并记录上网信息。[中央政府门户保存的 2002 文本](https://www.gov.cn/banshi/2005-08/21/content_25106.htm)

这对旧网身份史有一个很重要的修正：

```text
venue real-name registration
!= website real-name registration
!= platform pseudonym
```

一个 2005 年论坛账号可能叫匿名昵称，但使用者进入网吧时现实身份已经被另一个系统记录。反过来也不能从场所身份证登记推出远端某个账号一定属于该身份证持有人：网页账号、机位 session、身份登记仍需证据连接。

因此不要写：

> “当时论坛用户是匿名的。”

更窄的写法应是：

> “该平台账号层面可以使用昵称；本轮没有证据证明平台页暴露现实姓名。若访问发生在实施身份证登记的网吧，场所运营层另可能存在现实身份记录，但这不是同一数据库。”

---

## 4. 2005–2006: shared terminals were increasingly software-managed terminals

### 4.1 Wuhan: venue logs, monitoring and web accounts are separate evidence systems

新华社 2005-07-28 报道武汉全市 1200 多家网吧、每日约 50 万人次进入网吧，并说 2001–2003 年当地网吧已先后安装安全管理软件和实名上网系统；2005 年又推进视频监控与系统升级。[新华社/新浪](https://tech.sina.com.cn/i/2005-07-28/1543676464.shtml)

这条 B 级同期新闻不能告诉我们具体软件版本、数据库 schema、终端镜像或网络协议；但它足以证明：

> **旧网页访问的“本地一侧”可能已经有一个网页档案完全看不见的管理软件栈。**

Web archive 可能保存某个论坛帖子，却不会保存：

- 用户在几号机；
- 实名登记是谁；
- 何时开机/结账；
- 前台管理服务器是否锁机；
- 视频监控是否覆盖该座位；
- 当时机器是否由无盘/还原系统恢复。

### 4.2 Changsha “网络110”: ID reader + keyboard input + billing software

2006-06-17 的同期报道给出了更具体的状态链：长沙要求网吧安装新版“网络 110”管理软件，与计费系统对接；实名信息可以通过键盘录入，也可以连接身份证读卡器读取；消费者经过系统验证后才能上机。[红网/新浪](https://news.sina.com.cn/o/2006-06-17/03439224242s.shtml)

因此至少需要：

```text
consumer presents ID
→ operator/system captures identity data
→ identity verification succeeds
→ billing/management session associates a machine
→ terminal is released for use
→ browser/client layer begins
```

不要把其中任意一步简化成“刷身份证上网”，除非具体场所、具体年份证据支持自动刷卡。同期报道本身已说明一代身份证信息可以键盘录入、二代证可使用读卡器，实际路径不唯一。

### 4.3 account owner != terminal owner

共享终端尤其要求固定这条边界：

```text
web account owner != terminal owner != venue operator
```

在家庭 PC 语境里，研究者很容易默认浏览器历史、下载文件、cookie、收藏夹都属于同一名长期用户；在网吧这通常不成立。同一台物理机一天可能经历很多互不认识的用户。

---

## 5. Access environment can change whether an old website was executable

现代 archive 回放最危险的一种后见之明是：

> 2026 年 Chromium 能打开 capture，因此 2005 年用户也能顺利完成页面事务。

网吧把这个问题放大，因为终端往往统一维护，用户未必有管理员权限，也未必可以自由更新浏览器、ActiveX、证书、Java、Flash、输入法或下载控件。

因此对任何涉及网吧使用的历史事务页，都应新增字段：

```yaml
access_environment:
  ownership: public_shared_terminal | school_terminal | workplace | household | unknown
  os: unknown
  browser: unknown
  browser_version: unknown
  plugin_policy: unknown
  local_admin_rights: unknown
  persistent_storage: unknown
  restore/reset_behavior: unknown
```

没有证据时全部写 `unknown`，不要用“网吧一般都是 IE6”补空白。

---

## 6. available online != safely executable from a public terminal

公共终端不仅影响兼容性，也改变事务风险。

2005 年招商银行关于网银安全的同期材料明确建议用户“不要在网吧等公共场所操作网上银行业务”，并把病毒、密码、证书等视为需要控制的风险；其移动数字证书方案的一个卖点正是私钥留在 USB Key 中，使用后取走，不必把证书留在电脑上。[新浪财经，2005-02-22](https://finance.sina.com.cn/money/bank/bank_hydt/20050222/16171374768.shtml)

2006 年媒体又报道过针对网吧电脑放置木马、窃取网银账号密码的案件风险。[中新网/搜狐，2006-08-22](https://news.sohu.com/20060822/n244925715.shtml)

所以研究 2000s 的“网上支付已经存在”时，需要至少拆开：

```text
payment page exists
!= browser can render it
!= required certificate/control can run
!= user trusts the public machine
!= credential entry is safe
!= bank transaction completes
```

这会改变旧网研究的一个常见写法。不能看到“网上银行/在线报名支持在线支付”，就默认任何能在网吧打开网页的人都具备同等 transaction executability。

---

## 7. Internet-cafe software itself became a distribution layer

到 2000s 后期，网吧终端不只是“裸 Windows + 浏览器”。计费、维护、游戏更新、桌面广告、影音和安全系统本身构成一个很重要但保存很差的平台层。

第一财经 2010 年对顺网科技招股材料的报道说，其“网维大师”是面向网吧渠道的互联网娱乐平台产品；2007–2009 年相关服务按年收费，说明这种终端管理已经形成商业软件市场。[第一财经，2010-06-29](https://www.yicai.com/news/368141.html)

17173 在 2012 年对网吧媒体的行业盘点又列出网维大师、PubWin、万象网管等计费/维护软件，并描述了游戏广告、桌面分发等场景。[17173，2012-06-20](https://news.17173.com/content/2012-06-20/20120620180010079_all.shtml)

这些 B 级行业材料不能代替历史软件包、手册和 capture，但它们指出了一个应该进入 platform genealogy 的分支：

```text
ISP / access line
→ venue LAN
→ billing / identity management
→ terminal maintenance / game-update layer
→ browser + local clients
→ remote Web platforms
```

对许多 2000s 网民来说，“互联网首页”甚至可能先由网吧统一桌面和软件分发系统决定，而不是由用户自己配置。

### Future evidence target

后续应优先找：

- PubWin 历史官方帮助/安装手册；
- 万象网管历史安装包或操作手册；
- 网维大师 2005–2010 历史页面、版本说明和终端截图；
- 网吧无盘/还原卡配置资料；
- 早期网吧主页/价目表的可核验 archive capture。

这些证据比后来“我的青春在网吧”回忆更能回答真实终端环境。

---

## 8. Public-web survival / access-environment loss asymmetry

这是本轮对 archive bias 最重要的新增。

### 容易保存

- 门户、论坛、博客、游戏和网银的公开页面；
- 网吧经营法规；
- 软件厂商公开产品页；
- 新闻报道中的网吧照片；
- 某些论坛用户发出的帖子。

### 很难保存

- 某个用户从哪家网吧访问；
- 终端号和计费时长；
- 当时真实 OS/browser image；
- 已安装插件与证书；
- 是否有管理员权限；
- 本地下载和临时文件；
- QQ/游戏客户端的本地状态；
- 关机/还原后哪些数据被清除；
- 身份证登记数据库；
- 局域网内部页面；
- 前台计费服务器；
- 远端网页是否因当时 DNS、带宽或安全软件而不可达。

于是形成：

> **page survival / access-environment loss asymmetry**

Web archive 偏向保存“远方网站长什么样”，却系统性漏掉“普通人靠什么机器到达它”。

这会产生错误的家庭化想象：后人看到一名 2007 用户连续发帖，很容易脑补成“他坐在自己的电脑前”；事实上仅凭帖子本身完全不能知道设备所有权和访问地点。

---

## 9. Real-name venue log / pseudonymous platform gap

2002 以后公共营业场所的身份证登记要求与 2005–2006 各地实名系统扩展，使另一个 archive gap 变得重要：

```text
real-world identity
↕
venue identity/session database       [usually private, not archived]
↕
terminal/IP/time
↕
platform login/account                [partly visible]
↕
public post/profile                   [most archivable]
```

今天通常只剩最下面一层。

因此不能从“公开旧帖看起来匿名”推出“当时现实访问完全匿名”；也不能反向利用后来泄漏/私密数据库去给普通旧网用户做实名追溯。本仓的隐私原则要求：**研究结构，不重新公开普通人的身份证号、历史机位日志或已删除联系方式。**

即使未来得到完整管理软件数据库样例，也应优先记录 schema、字段语义和工作流，而不是复制个人行记录。

---

## 10. Session privacy gap

共享机器带来一个家庭 PC 不明显的问题：一次数字生活可能必须在“时间到”时显式结束。

需要把以下状态分开：

```text
browser window closed
!= platform logout executed
!= cookie deleted
!= local history deleted
!= downloaded file deleted
!= IM client account removed
!= terminal reset/reimaged
```

2005–2007 网银安全材料反复强调公共机器风险，本身就说明“离开座位后本地环境还会不会留下东西”是当时真实的使用条件。

但是本轮还没有足够 A 级材料确定：

- 不同管理软件默认是否清 cookie；
- 常见网吧是否每次下机都自动还原系统；
- 无盘系统何时成为不同城市的常态；
- QQ 本地聊天记录、账号列表、下载文件如何处理。

这些都必须保持 UNKNOWN，不能用后来经验补成 2005 年全国常态。

---

## 11. 2012–2015: when the same venue stopped meaning the same thing

中新网 2014 年行业回顾说，2012 年全国网吧数量同比下降 6.9%，约 1 万家关闭；2013 年末互联网上网服务企业约 13.5 万家。该回顾同时把 1990s 末家庭电脑尚未普及时的网吧描述为主要上网场所之一。[中新网，2014-12-08](https://www.chinanews.com/sh/2014/12-08/6853489.shtml)

对于 old-web-archaeology，这意味着“网吧访问”不能在 1998–2015 之间当成同一个环境标签。

至少应该分：

- **early public-access phase**：联网本身稀缺；
- **mass netbar phase**：网吧是重要接入地点，并与 QQ、论坛、网络游戏等深度耦合；
- **home/mobile substitution phase**：基本联网逐步转向家庭和手机，网吧更偏游戏/性能/社交。

同一个平台用户在不同年份即使都写“我在网吧”，其含义可能已经变化。

---

## 12. M1 status in this slice

本轮获得了不少 A/B 级**制度和同期新闻**，但还没有获得一个满足仓库 M1 最低合同的“网吧终端/管理平台历史 capture”。

候选对象包括：

- 2005–2006 各地网吧实名/安全管理软件；
- “网络 110”网吧管理软件；
- PubWin；
- 万象网管；
- 网维大师；
- 1995–2005 早期网吧自己的主页/价目页。

目前公开新闻对“网络110”等产品并未给出足够明确的 exact historical original URL；现今顺网产品页只能证明今天品牌/产品谱系仍存在，不能反向当作 2007 产品页面。

因此严格记录：

> **M1 verified historical Chinese internet-cafe management/public-terminal capture: NOT ACHIEVED IN THIS SLICE.**

这不等于 Internet Archive 没保存，也不等于当时不存在相应网页。

未核实项继续保持：

- exact original product URL；
- capture datetime；
- historical Content-Type / charset；
- DOM / form action；
- historical browser requirement；
- ActiveX / Java / Flash dependency；
- management server/client protocol；
- local reset/reimage behavior；
- second historical time point。

---

## 13. Claim table

| Claim | Evidence | Grade | Confidence | Limits |
|---|---|---:|---|---|
| 1986–1987 中国已有科研远程登录/国际邮件，但 1994 才全功能接入 Internet | CNNIC historical chronology | A/institutional chronology | high | 不证明普通公众可用 |
| 1995–1996 已有早期公共 Internet 营业场所 | later institutional/media histories | C/B retrospective | medium-high | “第一家”来源冲突 |
| 2002 条例把营业性公共上网场所作为独立制度对象并要求身份证件核对登记 | State Council regulation | A | high | 后续修订不能自动代表 2002 所有细节，引用历史文本 |
| 武汉 2001–2003 已有安全管理/实名上网系统，2005 推进视频监控 | Xinhua contemporaneous report | B | high for Wuhan report | 不代表全国实现方式 |
| 长沙 2006 “网络110”与计费系统对接，可键盘录入/读卡器采集实名信息 | Rednet contemporaneous report | B | high for described rollout | exact software architecture unknown |
| 公共机器并非所有在线事务的安全等价替代品 | 2005 bank security guidance + later cases | A/B | high as risk guidance | 不说明所有网吧都被木马感染 |
| 网吧管理/维护软件在 2000s 后期成为重要终端分发层 | 2010 prospectus reporting + 2012 industry survey | B | medium-high | vendor market-share claims require primary filings/manuals |
| Web archives systematically preserve remote pages better than local venue sessions | evidence-model inference | D | high as methodological inference | 需要 future case quantification |

---

## 14. Hindsight risks

1. **不要把“网民”自动画成“家里有 PC 的人”。**
2. **不要把网页可访问自动等于事务可执行。** 公共机安全和插件条件会阻断高风险事务。
3. **不要把平台昵称匿名自动等于现实访问匿名。** 场所层可能另有实名日志。
4. **不要把后来流行的 IE6 / Ghost / 无盘 / 还原卡经验反投射到所有年份和城市。**
5. **不要用今天的网咖环境复原 2005 网吧。** 硬件、浏览器、身份登记和主要用途都已经变化。
6. **不要因为帖子还在，就假定访问环境也被保存。** 页面 archive 只保存 transaction 的远端一侧。
7. **不要为了证明身份链去重新公开历史实名记录。** 普通用户隐私优先于“考古完整性”。

---

## 15. Why this matters for Chinese old-Web archaeology

过去本仓常问：

> 这个页面当时长什么样？

这一轮要求再加一句：

> **一个当时没有自己电脑的人，实际上是怎样到达这个页面的？**

这会改变很多旧网判断：

- 一个论坛的活跃并不要求所有用户家庭拥有 PC；
- 一个网页登录功能存在，不代表共享终端上的用户愿意安全输入敏感凭证；
- 一个账号的连续在线痕迹可能来自多台完全不同的机器；
- 网吧管理软件、浏览器镜像和客户端预装会影响普通人看到哪些入口；
- 旧网页保存得再好，也很可能已经失去当时最重要的“入口环境”。

所以中文旧网不是只有服务器端遗址，也有大量已经消失的**客户端公共基础设施**。网吧是其中最值得单独建立证据模型的一类。

---

## Next research slice

优先顺序：

1. 找到一个 2003–2010 网吧管理软件的 exact historical original URL；
2. 实际打开 ≥2 个 historical capture，核验 URL、datetime、replay、charset、DOM、资源与浏览器条件；
3. 找一份同期安装手册/软件包说明做第二 evidence family；
4. 对比同一软件两个版本，观察身份证、计费、桌面分发、浏览器/客户端控制如何变化；
5. 再选一个真实旧网页，分别重建“家庭 PC 访问”和“统一网吧终端访问”可能存在的操作差异。
