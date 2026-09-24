# BlogBus：二级域名、迁移与 DNS 级失踪链（2004—2013）

> 状态：**bounded research note；不是 M1 complete case。**  
> 研究对象：`blogbus.com` / 博客大巴在 2004—2013 年间的托管博客形态、二级域名、迁移导致的 URL 断裂、VIP 独立域名，以及 2010 年 DNS 解析中断所造成的“页面消失但数据未必消失”。  
> 本文只写本轮能够由公开、合法来源定位的证据。没有直接核验的 Wayback / Common Crawl capture，不写成 archived-page A 级证据。

## 0. 为什么现在做 BlogBus

仓库已经有 BlogCN、网易个人主页、百度空间、QQ 空间、西祠和 Discuz! 等 bounded note，但 Phase 2 / M1 仍没有正式完成任何一个 `cases/<slug>/` 案例。BlogBus 值得在此时单独做一刀，不是因为“又一个老博客平台”，而是因为它恰好留下了一组能够把**URL、托管状态、DNS 与内容存续拆开**的同时代证据。

本轮至少可以推进四个仓库当前仍未完全解决的问题：

1. 托管博客的用户身份 URL 如何从旧路径迁移到二级域名；
2. “平台为用户提供独立域名”如何改变 URL ownership；
3. 2010 年站点不可访问如何具体拆成首页/IP、域名解析、内容数据等不同层；
4. 一个域名短期停止解析后重新恢复，为什么不能简单写成“网站在 2010 年关闭”。

BlogBus 还提供一个很有价值的编码旁证：2005 年一位同时代用户在迁移后遇到找回密码邮件乱码。但这个证据只能证明**邮件/账户恢复链上存在编码失败**，不能直接推出 BlogBus 页面本身当时使用哪种 charset。

因此本轮的核心不是补一段平台史，而是建立一个更严格的失踪链模型：

```text
用户看不到页面
    ≠ DNS 一定失效
    ≠ origin 一定离线
    ≠ HTTP 一定没有响应
    ≠ 正常内容一定删除
    ≠ 后端数据一定删除
    ≠ 用户 URL 永久消失
```

本轮仍缺历史响应 header、原始 HTML、charset、redirect、DNS 记录、页面资源树与直接 archive capture，所以不能升格为完整 case。

---

## 1. 先拆研究对象

不要把“BlogBus”“博客大巴”“blogbus.com”“某个二级域名博客”“后台数据库”和“域名解析状态”视为一个永恒对象。

本轮至少区分：

```text
service / operator family
  BlogBus / 博客大巴

public service domain
  blogbus.com
  www.blogbus.com

hosted-blog identity locator
  <name>.blogbus.com

possible historical legacy URL
  old platform path / old account URL
  （2005 用户记录表明迁移后原网址可能失效；本轮未恢复具体 pattern）

paid / VIP URL option
  custom independent domain
  （2005 同期报道确认 BlogBus VIP 提供独立域名）

content state
  normal
  migrated
  normal content unavailable / replacement notice
  retained but user-inaccessible
  restored

name-resolution state
  resolving
  homepage/IP issue
  domain resolution suspended
  restored

backend-data state
  present
  backup claimed by operator
  actually deleted / corrupted
  （后两项本轮没有直接存储层证据）
```

因此下列等式都不能默认成立：

```text
homepage down = whole service down
domain unresolvable = origin deleted
user URL broken = user data deleted
platform migration = successful redirect
second-level domain = canonical storage path
custom domain = user owns platform content
operator says data safe = independently verified backup
service restored = all historical links restored
```

---

## 2. 证据表

| ID | 时间 | 证据 | 等级 | 独立证据家族 | 本轮用途 |
|---|---|---|---|---|---|
| A1 | 2004-03-12 | Jian Shuo Wang 同时代文章保存 BlogBus 停服页截图，并转述 2004-03-11 的临时关闭提示 | **A for contemporaneous screenshot/publication**；原因判断不自动升级 | contemporaneous personal observation | 证明该时点存在 replacement / shutdown 页面 |
| A2 | 2004-03-19 | OpenNet Initiative 对 BlogBus / BlogCN 做实际访问测试：网站并非网络层完全不可达，而是正常内容被移除、换成临时关闭信息 | **A for direct measurement**；原因转述为 B | independent network measurement | 区分 reachability 与 normal content availability |
| A3 | 2005-01-30 | Xu Wenhao 第一人称记录 BlogBus 数据迁移后原网址失效、只能用二级域名访问，且找回密码邮件乱码 | **A for first-person operational observation** | user observation | URL continuity、migration 失败与编码问题 |
| B1 | 2005-07-05 | 《中国计算机报》经新浪保存：BlogBus VIP 提供更大空间、远程发布、独立域名、模板定制等增值服务 | **B** | product/business report | URL ownership 与页面控制权分层 |
| A4 | 2008-09-22 | 上海博识文化传播有限公司经 PR Newswire 发布 BlogBus 活动稿，使用 `cityphoto.blogbus.com` 活动地址 | **A for operator-issued contemporaneous locator** | operator press release | 证明 `*.blogbus.com` 二级域名命名方式确实处于生产使用中；不能单独证明所有用户博客同一实现 |
| B2 | 2010-01-08 | 《京华时报》经新浪保存：域名服务商称被要求停止解析 BlogBus 域名；BlogBus 此前称由首页 IP 问题转为域名解析问题，内容不会受影响 | **B，含直接采访** | newspaper + domain provider / operator quotes | DNS 层失踪链；区分数据与可达性 |
| B3 | 2010-01-14 | 互诺转载 BlogBus 恢复公告全文：称 `blogbus.com` 域名解析已恢复、数据有双重备份 | **B / derivative operator notice** | republished operator notice | 恢复节点与“数据安全”运营方 claim |
| B4 | 2013-07-18 | 36氪报道 BlogBus 新版上线并更新 Android/iOS 客户端；同时嵌入 CEO 长微博回顾 | **B for 2013 relaunch**；对更早历史回顾只作 C/B 边界线索 | tech media | 证明 2010 并非永久关停节点；平台后来继续演化 |
| C1 | 2013 CEO 回顾中的 2002、2006、2009、2011 叙述 | 后来回顾自身早期历史 | **C unless separately corroborated** | operator retrospective memory | 只作线索，不替代当年 artifact |
| D1 | 本文 | 将 URL / DNS / content / backend / redirect 拆层 | **D** | researcher model | 明确是解释模型，不伪装成历史事实 |

### 关于“独立来源”

- A1 与 A3 都是个人用户/观察者材料，但作者、时间和观察事件不同，不能简单当成同一份转载链。
- A2 是网络研究机构直接测试，和 A1 完全不同 evidence family。
- B2 来自报纸采访域名服务商和平台，B3 是平台公告的二次保存，两者有部分事实依赖关系，因此不能机械算成两个互不相关的根来源。
- 2013 的 36氪只用于证明当年的 relaunch；其对更早年份的总结不能反向覆盖 2004/2005/2010 的同期证据。

---

## 3. 2004：所谓“关闭”，至少可以拆成网络可达与正常内容不可用

### A1 — 2004-03-11 / 12 的停服页

Jian Shuo Wang 在 2004-03-12 发布 `BlogBus.com Blocked`。他一开始用“blocked”形容事件，随后明确修正自己的措辞：这并不只是简单意义上的网络阻断，而是服务被要求停下来。

页面保存了 BlogBus 当时的停服截图，并把页面信息翻译为：因部分用户内容问题，Web server 暂时关闭，会尽快处理。

Source:

- Jian Shuo Wang, `BlogBus.com Blocked`, 2004-03-12.  
  <https://home.wangjianshuo.com/20040312_blogbuscom_blocked.htm>  
  Accessed 2026-09-24. Evidence: **A for the dated contemporaneous page and embedded shutdown screenshot; causal explanation is not independently proven by the screenshot alone.**

安全 claim：

> 2004-03-11/12 左右，BlogBus 对公开访问者呈现了一个临时停服 / replacement 页面，而不是正常托管博客内容。

这条证据不能单独证明：

- DNS 是否停止解析；
- TCP / HTTP 是否完全不可达；
- 用户博客数据库是否删除；
- 所有用户二级域名是否同样返回该页面；
- 关闭原因的完整法律 / 行政链条；
- 页面实际 HTTP status、header、charset 或 DOM。

### A2 — ONI：可达性仍存在，正常内容被替换

OpenNet Initiative 在 2004-03-19 的同时代记录中报告：BlogBus 与 BlogCN 并不是通过网络技术手段直接变成“不可访问”；测试时站点仍然能够访问，但原本内容被移除，页面被临时关闭信息取代。

Source:

- OpenNet Initiative, `Domestic Blogs Closed and Blogspot Blocked in China`, 2004-03-19.  
  <https://opennet.net/blog/2004/03/domestic-blogs-closed-and-blogspot-blocked-china>  
  Accessed 2026-09-24. Evidence: **A for ONI direct reachability/testing observation**.

A1 + A2 可以支持一个比“网站关了”更精确的状态：

```text
network path / name resolution
  sufficiently available for a page to be served

HTTP/site entry
  returns a response

normal hosted content
  unavailable from normal presentation

replacement state
  temporary shutdown notice
```

这也是后面 2010 事件的对照点：

- 2004：至少有证据表明**站点仍可返回 replacement page**；
- 2010：同期采访明确触及**域名解析本身被停止**。

因此两个事件即便都被后来概括成“BlogBus 被关”，技术状态并不相同。

---

## 4. 2005：迁移可以让“同一博客”继续存在，但原 URL 已经死亡

### A3 — 第一人称迁移记录

Xu Wenhao 在 2005-01-30 的同时代文章中记录：BlogBus 当时经历数据迁移；平台最初提示迁移需要 24–48 小时，但其个人体验是等待更久，迁移后仍有 bug。

更重要的是，他明确记录了两个与考古有关的现象：

1. 迁移后“只能通过二级域名访问”，原来的网址不能继续使用，导致旧链接失效；
2. 从 BlogBus 首页进行账户恢复时，找回密码邮件出现乱码，他尝试不同字符集显示也无法正常阅读。

Source:

- Xu Wenhao, `blogbus真是烂糟糟`, 2005-01-30.  
  <https://medium.com/%E7%81%B0%E8%89%B2%E7%9A%84%E7%81%B5%E9%AD%82/blogbus%E7%9C%9F%E6%98%AF%E7%83%82%E7%B3%9F%E7%B3%9F-cdefc5e3014a>  
  Accessed 2026-09-24. Evidence: **A for dated first-person operational observation; Medium is the present host, so original publication provenance should still be independently checked if a historical copy can be found.**

### 4.1 URL continuity 与 content continuity 必须分开

这个用户报告直接提示：

```text
same user/content identity
    may survive

old locator
    may break

new second-level-domain locator
    may work
```

也就是说：

```text
content survives ≠ old URL survives
```

对于旧网考古，这意味着搜索引擎、Wayback、论坛外链或个人收藏夹中出现的大量“死链”，不能自动解释为“内容当时已经删除”。它也可能是平台迁移后没有保留重定向。

### 4.2 不能从这条记录猜出旧 URL pattern

本轮没有恢复该用户迁移前的完整 BlogBus URL，因此不能写成：

```text
old URL = blogbus.com/<user>/...
```

或任何其他具体结构。

目前只能写：

> 至少有一位 2005 年同时代用户明确观察到 BlogBus 迁移造成原 URL 不再可用，而二级域名成为可访问方式。

后续 archive 工作的目标应是找到同一用户迁移前后的两个 locator，而不是从记忆中补格式。

---

## 5. 2005：VIP 独立域名让 URL ownership 变得更复杂

《中国计算机报》2005-07-05 的文章记录，BlogBus 在 2005-06-07 高调推出新版 VIP 服务，其中包括：

- 远程发布；
- 独立域名；
- 模板定制；
- 更大空间等增值服务。

Source:

- 汪蔚，`中国计算机报：看三大博客网的扭扭捏捏`，2005-07-05，经新浪科技保存。  
  <https://tech.sina.com.cn/i/2005-07-05/1538654416.shtml>  
  Accessed 2026-09-24. Evidence: **B**.

这是一个很重要的托管模型分叉：

```text
free / ordinary hosted identity
  <user>.blogbus.com

VIP identity possibility
  user-owned or custom independent domain
       |
       v
  still backed by BlogBus hosting / publishing service
```

因此，“谁拥有 URL”不能只按平台名称回答。

至少要区分：

- 域名注册权属于用户还是平台；
- DNS 由谁控制；
- HTTP 内容由谁托管；
- 页面模板由谁提供；
- 内容数据库由谁保存；
- 用户能否把同一个域名重新指向别处。

这也是 BlogBus 比纯粹 `<user>.platform.com` 模式更有研究价值的地方。

但本轮不能声称：

- 所有 VIP 用户都使用独立域名；
- 独立域名一定由用户本人持有注册权；
- BlogBus 一定提供完整 DNS 托管；
- 绑定域名后平台二级域名一定仍然存在；
- BlogBus 关闭时自定义域名一定可以无损迁出。

这些都需要具体账户或平台文档支持。

---

## 6. 2008：`*.blogbus.com` 二级域名确实处于公开生产使用

2008-09-22，上海博识文化传播有限公司经 PR Newswire 发布活动稿，明确给出活动地址：

```text
http://cityphoto.blogbus.com
```

Source:

- 上海博识文化传播有限公司，`博客大巴 BlogBus 发起《大同.视界》摄影展`，2008-09-22，PR Newswire Asia.  
  <https://www.prnasia.com/story/13954-1.shtml>  
  Accessed 2026-09-24. Evidence: **A for operator-issued contemporaneous locator**.

这条证据价值不在活动本身，而在 URL：

> 到 2008 年，`<name>.blogbus.com` 形式的二级域名确实用于公开的 BlogBus 托管内容 / 项目页面。

它和 A3 的 2005 用户观察互相补充：

```text
2005 user observation
  migration made second-level domain the working locator

2008 operator-issued URL
  a production <name>.blogbus.com locator is directly documented
```

但仍不能直接推出所有用户博客都采用相同 DNS / virtual-host 实现。

需要 archive / DNS 证据才能继续回答：

- wildcard DNS 还是逐条记录；
- wildcard virtual host 还是 application routing；
- 是否存在 canonical redirect；
- 是否同时支持 `www.blogbus.com/...` 路径；
- 自定义域名如何映射到同一内容对象。

---

## 7. 2010：一次非常适合做“域名失踪链”的事件

### B2 — 1 月 5 日起从首页/IP问题发展成域名解析问题

2010-01-08，《京华时报》报道 BlogBus 自 1 月 5 日起无法正常登录。

报道保留了几个不能被压成一个“网站挂了”的状态变化：

1. 1 月 5 日，BlogBus 公告称最初受到的是“首页 IP”层面的问题；
2. 1 月 6 日，BlogBus 又称问题属于“域名解析”；
3. 域名服务商北京新网互联工作人员向记者表示，接到通知要求停止解析 BlogBus 域名；
4. BlogBus 表示博客内容不会受影响；
5. 截至报道时，公开访问仍未恢复。

Source:

- 《京华时报》，`百万用户上不了“博客大巴”`，2010-01-08，经新浪新闻保存。  
  <https://news.sina.cn/sa/2010-01-08/detail-ikmyaawa2464891.d.html>  
  Accessed 2026-09-24. Evidence: **B, with direct interviews/quotes**.

### 7.1 这不是普通“服务器宕机”叙事

从该报道能够安全提取的最小状态模型是：

```text
T0 — normal service

T1 — homepage/IP-level failure reported by operator

T2 — domain-resolution failure reported by operator

T3 — domain provider confirms resolution suspension

T4 — public users cannot reach normal BlogBus URLs

backend content/data state
  operator claims unaffected
  independently unknown
```

因此：

```text
public URL unreachable
    does not prove
backend content deleted
```

这是本仓“页面与域名失踪链条”里非常重要的一种类型：

> **命名层消失（name-resolution disappearance）可以让大量仍然存在的服务器与数据，在用户体验中瞬间变成“整个网站消失”。**

### 7.2 站点是否可以绕过域名访问，本轮不知道

因为没有当时 origin IP、Host header、CDN / virtual-host 配置和 DNS 历史记录，本轮不能回答：

- 用户输入 origin IP 是否仍可访问；
- 站点是否要求正确 `Host: *.blogbus.com`；
- 用户博客是否和首页使用相同 IP；
- 后台、图片、静态资源是否在别的域名；
- 邮件、API、RSS 是否同样因 DNS 失效。

这些恰恰是 archive capture 无法单独替代的运行环境证据。

---

## 8. 2010-01-13/14：域名恢复，但“数据安全”仍只是运营方声明

2010-01-14 的转载页面保存了 BlogBus `再度启程` 公告全文。公告称：

- 自 1 月 5 日以来，因 `blogbus.com` 域名被服务商停止解析而大规模无法访问；
- 经过沟通后域名解析恢复；
- 各地用户将逐批恢复访问；
- 运营方称网站数据有双重备份，不会出现数据丢失。

Source:

- `博客大巴关闭数日 今日公告称网站恢复访问`，2010-01-14，互诺科技转载 BlogBus 公告。  
  <https://www.hunuo.com/News/hangyemenhu/12528.html>  
  Accessed 2026-09-24. Evidence: **B / derivative operator notice**.

安全 claim：

> 到 2010-01-13/14，BlogBus 对外宣告 `blogbus.com` 域名解析已恢复，公开访问开始逐步恢复。

不能进一步写成：

- 所有用户博客当时立刻恢复；
- 所有历史 URL 都恢复；
- 双重备份已经被外部审计；
- 期间绝无数据损失；
- 缓存、RSS、图片、评论、后台状态全部与中断前一致。

运营方“数据双重备份、不会丢失”的话是重要史料，但仍然是**operator claim**，不是存储系统取证。

---

## 9. 2013：2010 不是永久死亡节点

2013-07-18，36氪报道 BlogBus 新版上线，同时更新 Android、iOS 客户端，并称桌面新版使用新的聚合首页形态。

Source:

- 36氪，`11岁的大巴重新出发，Blogbus新版上线，更新iOS、Android客户端`，2013-07-18.  
  <https://www.36kr.com/p/1641754279937>  
  Accessed 2026-09-24. Evidence: **B for the 2013 relaunch state**.

这条证据的作用是排除一种常见后见之明错误：

```text
2010 大规模不可访问
    ≠
2010 永久关站
```

从 2013 同期报道至少可以确认：

- BlogBus 作为产品仍然存在；
- 平台仍能推出新版 Web 产品；
- 同时提供移动客户端；
- 2010 的事件必须建模为一次服务 / 域名中断，而不是最终关闭。

36氪还引用 / 展示了 CEO 对 2002—2013 的长篇回顾。该回顾可以作为后续线索，但其中“2002 开始”“2009/2010 高峰”“2011 被黑”等早期事件不能仅因 CEO 自述而全部升级成 A。需要独立同期证据再逐项核验。

---

## 10. 一个可复用的“BlogBus 失踪层级”模型

### Level 0 — content object

```text
post / comment / image / template / account metadata
```

这些内容是否仍存在于数据库或对象存储中。

### Level 1 — application mapping

```text
account id
  -> hosted blog
  -> route / template / permission
```

迁移后映射变化可以让旧 URL 死亡，但内容仍存在。

### Level 2 — HTTP serving host

```text
www.blogbus.com
<name>.blogbus.com
custom-domain.example
```

同一内容可能有多个入口，也可能只有一个入口。

### Level 3 — DNS/name resolution

```text
blogbus.com / *.blogbus.com
    -> address / CDN / service
```

2010 事件说明这一层失效可以造成几乎全站的用户侧“消失”。

### Level 4 — archive visibility

```text
Internet Archive / Common Crawl / search cache
```

archive 能否看到页面，还取决于：

- crawler 当时是否解析得到域名；
- crawler 是否命中正确 hostname；
- 是否抓到用户二级域名；
- 是否记录跳转；
- 是否保存图片 / CSS / JS；
- 是否抓到 replacement / outage page；
- 是否在 outage window 中把临时状态误当长期状态。

因此未来的 capture 取证应该把“页面不存在”至少拆成：

```text
no capture found
capture says DNS failure
capture has tombstone
capture has redirect
capture has HTML but assets missing
capture has old locator after migration
capture has new locator only
```

---

## 11. 与 BlogCN 的差异：不要把两个 2000s BSP 写成同一种死亡模型

仓库已有 BlogCN note。两者都属于中国早期 BSP，但已经可以看到不同的失踪机制：

### BlogCN（已有 note）

```text
free-service cutoff
export deadline
planned purge
later deletion deferral
```

核心问题是：

> 公告日期、导出截止和实际删除不能混在一起。

### BlogBus（本 note）

```text
migration URL breakage
second-level domain identity
custom-domain option
DNS resolution suspension
service restoration
```

核心问题是：

> 用户 URL 不可达、域名解析失效和后台数据删除不能混在一起。

因此“BSP 消失”至少已经出现两种完全不同的机制：

```text
content lifecycle / purge policy
vs.
name-resolution / routing failure
```

这正是 Phase 3 platform genealogy 应该保留的结构差异，而不是把所有老博客平台统一画成“兴起 → 衰落 → 关闭”。

---

## 12. 浏览器、编码与插件：本轮能说什么，不能说什么

### 12.1 页面 charset：unknown

本轮没有直接取得历史 BlogBus HTML、HTTP header 或 WARC payload，因此不能声称：

- 页面是 GB2312；
- 页面是 GBK；
- 页面是 UTF-8；
- 浏览器必须手工切换编码。

### 12.2 2005 密码邮件乱码：是独立值得保留的证据

A3 用户记录显示找回密码邮件无法正常显示，并尝试多种字符集仍未解决。

这只能安全写成：

> 2005 年 BlogBus 某次迁移后，一名用户在账户恢复邮件链上遇到严重乱码。

不能写成：

> BlogBus 2005 年网页编码错误。

邮件的 MIME header、body charset、transfer encoding 与 Web 页面完全可能是两套机制。

后续若能找到原邮件样本或完整 header，可以把它单独做成“旧互联网账户恢复邮件编码”小案例；在没有原始邮件的情况下，只保留用户观察。

### 12.3 IE / ActiveX / Flash：unknown

本轮没有找到足够强的证据证明 BlogBus 本体依赖：

- IE-only；
- ActiveX；
- Java Applet；
- Flash 作为核心渲染依赖。

即使 2000s 博客模板常嵌入 Flash / 音乐，也不能把行业习惯自动外推为平台依赖。

---

## 13. 已证实 / 高概率 / 不知道

| 状态 | 结论 | 依据 |
|---|---|---|
| **已证实** | 2004-03-11/12 左右 BlogBus 对公开访问者呈现临时停服 replacement page | A1 |
| **已证实** | 2004-03-19 ONI 测试时 BlogBus 并非简单网络不可达，而是正常内容被替换为停服信息 | A2 |
| **已证实** | 2005 年至少一名同时代用户观察到迁移后原 URL 失效、二级域名成为可访问入口 | A3 |
| **已证实** | 2005 年 BlogBus VIP 服务提供独立域名与模板定制等增值能力 | B1 |
| **已证实** | 2008 年 `cityphoto.blogbus.com` 是 BlogBus 运营方公开发布的生产 URL | A4 |
| **已证实** | 2010-01 上旬存在被域名服务商停止解析 `blogbus.com` 的同期采访证据 | B2 |
| **已证实** | 2010-01-13/14 BlogBus 宣布域名解析恢复 | B3 |
| **已证实** | 2013-07 BlogBus 仍在运营并发布新版与移动客户端 | B4 |
| **高概率** | 2005 前后平台经历过 URL namespace 重构，至少部分 legacy locator 没有保持兼容 | A3，但缺 old/new URL pair artifact |
| **高概率** | BlogBus 同时存在平台二级域名与 VIP 自定义域名两种用户侧 locator 模式 | A3 + B1 + A4 |
| **不知道** | 2005 用户迁移前具体 URL pattern | 未恢复 artifact |
| **不知道** | `*.blogbus.com` 是否 wildcard DNS / wildcard vhost | 无 DNS / server config |
| **不知道** | 2010 DNS suspension 的精确 DNS record / EPP / registry 状态 | 无原始 DNS / registry artifact |
| **不知道** | 2010 中断期间 origin IP 是否持续提供服务 | 无 origin/Host 测量 |
| **不知道** | 2010 所谓双重备份是否完整、是否通过恢复演练 | 只有 operator claim |
| **不知道** | 历史 BlogBus 页面 charset | 无 header/raw HTML |
| **不知道** | IE / ActiveX / Flash 是否为平台核心依赖 | 无足够证据 |

---

## 14. 缺失证据清单

要把此 note 升格为 M1 case，至少还缺：

### archive / HTTP

- 2004-03-11/12 `blogbus.com` replacement page 的直接 archive capture；
- 2005-01 迁移前后同一账户 old/new URL pair；
- 2005-06/07 VIP 服务说明原页；
- 2008 `cityphoto.blogbus.com` capture；
- 2010-01-04—01-15 `www.blogbus.com` 与若干非私人测试二级域名 capture；
- 2013-07 新版首页 capture；
- 原始 HTTP status；
- `Content-Type` / charset；
- redirect chain；
- page title / canonical / meta refresh；
- CSS / JS / image 子资源状态。

### DNS / domain

- 2009-12 与 2010-01 的 DNS 历史；
- nameserver 变化；
- A/CNAME 记录变化；
- 2010 事件期间是否出现 `SERVFAIL` / `NXDOMAIN` / withheld answer；
- registrar / registry status 的原始历史；
- 是否存在 wildcard `*.blogbus.com`。

### hosting / account

- 2005 迁移公告原文；
- VIP 独立域名绑定说明；
- 旧 URL → 新 URL 是否有 301/302；
- 用户导出能力；
- 自定义模板可编辑范围；
- 静态资源 host；
- 图片空间 host 与防盗链规则；
- RSS / Trackback URL pattern。

### browser / encoding

- historical HTML bytes；
- mail recovery sample/header；
- IE/Firefox 兼容说明；
- JavaScript errors；
- Flash / Java / ActiveX 是否存在平台级依赖。

---

## 15. 下一轮 bounded archive 工作

不要继续搜“博客大巴为什么衰落”的回忆文章。下一轮应直接追 artifact。

### Slice 1 — 2004 replacement page

目标 URL：

```text
http://www.blogbus.com/
http://blogbus.com/
```

目标窗口：

```text
2004-03-10 .. 2004-03-25
```

记录：

- capture datetime；
- HTTP status；
- raw `Content-Type`；
- page title；
- shutdown text；
- linked assets；
- whether individual subdomains were separately captured。

### Slice 2 — 2005 migration URL pair

先不枚举普通用户。

优先寻找：

- 同时代公开技术博客、媒体测试账号或作者本人明确公开的 locator；
- 可以证明迁移前后地址变化的同一内容对象；
- old locator 的 archived redirect / 404 / dead-link state；
- new `<name>.blogbus.com` 对应 capture。

### Slice 3 — 2010 DNS window

目标窗口：

```text
2010-01-04 .. 2010-01-15
```

目标不是“抓网页”，而是确认：

- archive crawler 在域名停止解析期间是否仍有 capture；
- 是否出现 timeout / DNS failure metadata；
- 恢复后第一批 capture 的时间；
- 是否有搜索缓存 / 独立监测记录可以和 Wayback 对齐。

### Slice 4 — custom-domain ownership

选择一个**机构 / 活动 / 项目**而非私人博客作为样本，确认：

- independent domain 是否 CNAME / A 到 BlogBus；
- 页面是否同时有 `*.blogbus.com` mirror；
- 站点停止后用户是否能把自有域名重新指向别处。

优先使用公开机构对象，避免翻个人旧博客。

---

## 16. 可以写入未来 platform genealogy 的最小结论

BlogBus 至少支持以下结构比较：

| 维度 | BlogBus 2005–2010 可安全写法 |
|---|---|
| URL ownership | 普通托管形态可使用 `*.blogbus.com`；VIP 同期报道显示可提供独立域名 |
| Layout control | 平台提供模板；VIP 报道显示可提供模板定制，但具体可编辑范围仍需原文 / capture |
| Hosting control | 内容主要由 BlogBus 托管；自定义域名不等于自托管 |
| Link continuity | 2005 有第一人称证据表明迁移使旧 URL 失效 |
| Failure mode | 2010 至少存在 DNS 解析停止导致大规模 URL 不可达 |
| Data continuity | 运营方称内容未受影响、数据有双重备份；无独立存储层验证 |
| Exit / portability | 独立域名理论上提供更强 URL portability，但本轮无具体迁出案例，不能直接声称 |

这个对象提醒我们：

> **“URL ownership”至少有域名注册权、DNS 控制权、页面路由权、内容数据库控制权四层。**

仅仅看到一个用户用了自定义域名，并不能说明她拥有页面基础设施；同样，平台域名短时停止解析，也不能说明内容本身消失。

---

## 17. 后来回忆与同时代证据比较

### 后来叙述常见压缩

2013 的平台回顾与后来关于 BlogBus 的历史介绍，很容易把 2002—2013 压缩成：

```text
创办
→ 做大
→ 多次被关
→ 衰落
→ 重启
```

这个叙述作为概览没有问题，但对考古证据太粗。

### 同时代证据显示的是多个完全不同的技术状态

```text
2004
  replacement shutdown page
  site still reachable enough to return that page

2005
  migration
  old URL breakage
  second-level-domain identity
  mail-recovery encoding failure

2005 VIP
  custom domain / template control as paid feature

2010
  name-resolution suspension
  service URLs broadly unreachable
  operator claims content/data intact

2010-01-13/14
  resolution restored

2013
  product relaunch + mobile clients
```

因此“多次被关”不是一个单一事件类型，而至少包含：

- content replacement；
- URL namespace migration；
- DNS suspension；
- temporary service outage；
- later product relaunch。

这正是本仓需要保存的“同时代证据纠正后来概括”的案例。

---

## 18. 隐私与版权边界

### 不做

- 不批量枚举历史 `*.blogbus.com` 个人博客；
- 不重新公开已删除的私人日志、照片、联系方式、评论；
- 不把普通用户的旧二级域名做成可搜索名录；
- 不把仍受版权保护的博客页面 / 图片整包提交仓库；
- 不把历史数据库、备份、导出包作为研究附件；
- 不因 archive 可访问就默认允许重新发布。

### 可以做

- 引用公开新闻 / 研究机构 / 官方公告；
- 记录少量公开 URL pattern；
- 对公开机构/活动子域名做 DNS / archive 元数据研究；
- 保存 header、hash、capture datetime、redirect metadata；
- 对历史页面做最小必要截图（若后续确有研究必要，并注明来源和版权）；
- 对普通用户案例优先抽象成 `<user>.blogbus.com`。

A3 的个人用户文章之所以可以使用，是因为本轮只引用其公开的**平台故障观察**，不重新分发其私人博客内容。

---

## 19. 本轮不能声称已经证明的内容

本轮**不能**写：

- “BlogBus 2004 年被墙所以完全无法访问”；
- “BlogBus 2004 年服务器彻底下线”；
- “BlogBus 2005 年所有用户都被迁移到统一二级域名”；
- “BlogBus 旧 URL 一律没有重定向”；
- “BlogBus 二级域名一定由 wildcard DNS 实现”；
- “2010 年 BlogBus 数据中心断电 / 服务器关闭”；
- “2010 年 BlogBus 数据被删除”；
- “运营方双重备份已经独立验证”；
- “BlogBus 历史页面采用 GBK / UTF-8 中某一种”；
- “BlogBus 依赖 IE / ActiveX / Java Applet / Flash”；
- “2010 是 BlogBus 关站年份”；
- “2013 新版与 2005 老系统共享同一内容数据库或 URL 架构”。

---

## 20. 建议写入位置

当前最合适的是保留为：

```text
research/blogbus-subdomain-dns-disappearance-chain-2004-2013.md
```

获得直接 archive artifact 后，可以考虑建立：

```text
cases/blogbus/
├── README.md
├── evidence.yaml
├── timeline.md
└── reconstruction.md
```

其中 `evidence.yaml` 至少应分别记录：

- 2004 replacement page；
- 2005 old/new URL migration pair；
- 2008 public subdomain locator；
- 2010 DNS suspension / restoration evidence；
- 2013 relaunch point。

### 对 M1 的状态

**仍未完成。**

当前已有：

- identity / platform family：有；
- ≥2 历史时点：有；
- ≥2 独立证据源：有；
- later-memory vs contemporaneous evidence 比较：有；
- resource-missing list：有；
- browser / encoding / plugin assumptions：已明确 unknown；
- confirmed / likely / unknown：有。

但仍缺：

- 可直接定位的 archive capture；
- raw HTTP / charset；
- subresource inventory；
- redirect / DNS artifact；
- 标准 `cases/blogbus/evidence.yaml`。

所以不应提前勾选 M1。

---

## 21. 本轮结论

本轮最重要的新结论不是“BlogBus 很早、很有名、曾经停站”，而是：

> **旧网里的“消失”必须按命名层、路由层、页面呈现层和数据层分别记录。**

BlogBus 提供了同一个平台内的三个很不同的消失机制：

```text
2004
  normal content disappears
  but a shutdown page still answers

2005
  content/account can survive migration
  while old locator dies

2010
  domain resolution can disappear
  while operator claims content/data remain intact
```

这三种状态如果都被写成“网站挂了”，就会把最有价值的技术史证据抹掉。

下一步不应继续搜更多回忆，而应直接验证：

1. 2004 replacement page archive；
2. 2005 同一内容 old/new locator pair；
3. 2010 DNS outage window 的 capture / DNS metadata；
4. 一个公开机构型自定义域名样本的控制权与跳转链。

只有这些 artifact 到位后，BlogBus 才值得从 bounded note 升格成正式 M1 case。
