# BlogCN：中国博客网托管、个性网址与免费数据失踪链（2002—2013）

> 状态：**bounded research note；不是 M1 complete case。**  
> 研究对象：`blogcn.com` / 中国博客网（2008 年后中文品牌更名为“博尚网”）的博客托管结构、个性网址、2004 临时停服、2008 品牌改名，以及 2012—2013 免费服务退出与数据清除语义。  
> 本文只写本轮能够由公开、合法来源定位的证据；没有直接打开核验的 Wayback / Common Crawl 历史 capture，不写成 A 级 archived-page evidence。

## 0. 为什么现在做 BlogCN

仓库已经有个人主页、论坛、QQ 空间、百度空间等 bounded note，但 Phase 2 / M1 仍要求三个不同类型的完整案例，其中“博客 / SNS / 平台案例”尚未形成完整 case。README 也把 BlogCN、博客大巴、MSN Spaces、门户博客列为博客时代的优先对象。

BlogCN 适合现在推进，原因不是“它很有名”，而是这轮能够得到几条互相独立、且直接碰到本仓核心问题的证据链：

1. 2004 年临时停服时，存在同时代截图记录与独立网络测量；
2. 2005 年横向评测留下了托管功能、模板编辑、图片额度和个性 URL 的操作级信息；
3. 个性二级域名与实际服务路径并不相同，可以直接讨论 URL ownership / vanity URL / served path；
4. 2008 年发生中文品牌更名，但没有证据显示 `blogcn.com` 同时迁移；
5. 2012—2013 年免费服务退出留下“公告截止时间”和“实际数据清除时间”互相冲突的同期报道，能够证明**政策截止日期不能自动等同于删除事件**。

这一对象因此同时推进：

- 托管环境；
- 页面 / URL 谱系；
- 平台形态时间线；
- 失踪链条；
- “公告 ≠ 实际状态”的证据方法。

但本轮仍缺历史响应 header、charset、DOM、子资源树与 archive capture，所以不能升格为 M1 complete case。

---

## 1. 先拆研究对象

不要把“中国博客网”“BlogCN”“博尚网”“blogcn.com”“某个用户博客”当成同一个永恒对象。

本轮至少区分：

```text
operator / service family
  BlogCN 中文博客托管服务

brand label
  中国博客网
  ↓ 2008-12 报道确认更名
  博尚网

domain / service host
  blogcn.com
  www.blogcn.com

vanity identity URL
  <user>.blogcn.com

observed served / redirected path pattern（2005 测评）
  www.blogcn.com/userNN/<user>/index.html

account/service tier
  free blog
  VIP / paid service

content state
  normal
  temporarily suspended / tombstone
  exportable
  no-longer-exportable（公告计划）
  retained / deletion deferred
  actually deleted（本轮未证实）
```

因此以下等式都不能默认成立：

```text
brand rename = domain migration
vanity URL = physical/canonical storage path
shutdown notice = network blocking
free-service cutoff = account deletion
export deadline = actual data deletion time
announced purge date = verified purge event
```

---

## 2. 证据表

| ID | 时间 | 证据 | 等级 | 独立证据家族 | 本轮用途 |
|---|---|---|---|---|---|
| A1 | 2004-03-13 21:32 左右 | Jian Shuo Wang 同时代文章保存其对 `blogcn.com` 的截图，并明确标注截图时间 | **A**（同时代截图 / contemporaneous publication） | Wang personal observation | 证明该时点 BlogCN 公开页面呈现停服状态；不能证明隐藏 DOM、header 或停服原因 |
| A2 | 2004-03-18 | OpenNet Initiative Bulletin 001：实际测试显示 BlogCN 网络层可访问，但正常内容被临时停服信息替代 | **A**（直接测试部分） / 原因转述为 B | ONI measurement | 区分“网络可达”与“平台内容可用” |
| A3 | 2004 年后续 | OpenNet Initiative Bulletin 008：记录 3 月临时停服后恢复 | **A/B**，与 A2 同家族 | ONI follow-up | 后续状态；不作为第二个独立家族重复计数 |
| B1 | 2005-03-31 | ChinaByte 经新浪保存的六家中文 BSP 横向测评 | **B** | hands-on technical review | 托管功能、模板编辑、图片额度、个性 URL → 实际路径跳转 |
| B2 | 2005-06-16 | 新浪科技报道 BlogCN 推出 M-RABO / RABO 收费服务 | **B**（用户数为运营方 claim） | business/product report | 免费托管之外的付费分层；不能把 225 万用户当独立测量 |
| B3 | 2008-12-30 | 新浪科技：《中国博客网更名为博尚网》 | **B** | rename/business report | 品牌变化与域名持续存在 |
| B4 | 2012-12-13 | 卢松松博客及 cnBeta/搜狐 IT 转述 BlogCN 停止免费服务公告 | **B**（公告二手转述） | near-contemporary web report | 提供公告文本与 2013-03-31 截止线索；未恢复 BlogCN 原公告 |
| B5 | 2013-04-01 | 中国互联网协会转述 BlogCN 免费服务公告，称公告日期为 2012-12-19 | **B** | industry-association report | 证明二手来源对原公告日期存在 12/13 vs 12/19 冲突 |
| B6 | 2013-03-31 | 中国广播网报道“今日将关闭所有免费博客并清除数据” | **B** | radio/news report | 证明媒体在截止日前如何理解公告；不是删除完成的技术证据 |
| B7 | 2013-04-02 | 第一财经日报：记者在 4 月 1 日看到 BlogCN 登录首页显示数据清除可延后至 7 月 1 日 | **B，direct observation embedded in report** | independent newspaper observation | 直接反驳“3 月 31 日 / 4 月 1 日已完成全部数据删除”的确定叙事 |
| C1 | 后来回忆 | 后来用户回忆 BlogCN 二级域名、页面个性化、Flash 等体验 | **C** | retrospective memory | 只用于与 2005 同期测评比较，不决定技术事实 |
| D1 | 本文 | 将 free cutoff / export cutoff / deletion / URL disappearance 拆成不同状态 | **D** | researcher model | 明确是解释模型，不伪装成历史原件 |

---

## 3. 2004：停服页存在，但“网站关了”不是一个足够精确的状态

### A1 — 2004-03-13 的同时代截图

Jian Shuo Wang 在 2004-03-13 当晚发布文章 `Blogcn & BlogDriver Shut Down`，并标注一张自己截取的 `blogcn.com` 屏幕截图时间为当晚 9:32。

Source:

- Jian Shuo Wang, `Blogcn & BlogDriver Shut Down`, 2004-03-13.  
  <https://home.wangjianshuo.com/20040313_blogcn_blogdriver_shut_down.htm>  
  Accessed 2026-09-17. Evidence: **A for the contemporaneous screenshot/publication**.

安全 claim：

> 2004-03-13 晚间，一个同时代可定位的访问者记录到 `blogcn.com` 正显示停服状态。

这条证据不能单独证明：

- 服务器完全离线；
- DNS 失效；
- 全国所有网络都无法访问；
- 用户数据已经删除；
- 停服原因；
- 当时页面的 charset / HTTP header / DOM。

截图能证明的是**可见页面状态**，不是整个系统状态。

### A2 — OpenNet：站点可达，但内容被 tombstone / suspension message 替换

OpenNet Initiative 在 2004-03-18 的 Bulletin 001 中记录：BlogBus 与 BlogCN 并非在技术网络层面被过滤到不可访问；测试时这些网站仍可访问，但正常内容被移除并替换为“临时关闭”类信息。

Source:

- OpenNet Initiative, `Bulletin 001`, 2004-03-18.  
  <https://opennet.net/bulletins/001/>  
  Accessed 2026-09-17. Evidence: **A for ONI's direct reachability/testing observation**; explanations attributed to third parties remain B.

这条证据和 A1 来自不同 evidence family，组合后能够把“关闭”拆成更具体的状态：

```text
DNS / network path
  apparently reachable

HTTP / site entry
  reachable enough to return a page

normal hosted-blog content
  unavailable / removed from normal presentation

replacement page
  temporary shutdown / suspension message
```

因此本案可以留下一个方法结论：

> **“网站关闭”在旧网考古中必须继续拆分。网络可达、入口页返回、正常内容可见、用户后台可用、数据仍保存在后端，完全可能是不同状态。**

OpenNet 后续 Bulletin 008 又记录这些服务后来恢复，但它与 A2 属于同一组织的延续观察，不能机械地算成第二个独立来源。

### 关于原因

本轮不把“为什么停服”写成由 A1/A2 直接证明的事实。ONI 对原因的部分说明依赖其他组织的报道；Wang 的个人文章也带有当时语境下的判断。本文只需要证明页面 / 服务状态，不需要把未经同等级核验的原因扩张成确定因果结论。

---

## 4. 2005：BlogCN 是典型的托管博客平台，而不是用户自己拥有目录树的独立网站

### B1 — 同期横向测评留下操作级信息

2005-03-31，ChinaByte 的六家中文博客托管服务商横向测评经新浪保存。文章不是平台官方宣传稿，而是对 BlogCN、BlogBus 等服务的实际注册和功能评测。

Source:

- 周天舒，`综述：六个中文博客托管服务商横向测评`，ChinaByte / 新浪科技，2005-03-31.  
  <https://tech.sina.com.cn/i/2005-03-31/1021566876.shtml>  
  Accessed 2026-09-17. Evidence: **B**.

该测评对 BlogCN 留下的可用信息包括：

- 注册流程为多步骤，并要求填写较多个人资料；
- 博客提供日历、评论、归档、RSS、Trackback 等典型 BSP 功能；
- 编辑器提供 UBB / 可视化编辑等方式；
- 可使用模板，并允许懂 HTML 的用户编辑模板代码；
- 提供图片上传，但有总空间和单图大小限制；
- 有朋友、团队博客等平台关系功能；
- 提供大量页面模板；
- 提供“个性网址 / 虚拟网址”形式的用户二级域名。

这些信息能支持：

> 2005 年 BlogCN 的页面外观可以由平台模板 + 用户一定程度的 HTML 模板修改共同决定。

但不能直接支持：

- 页面使用哪种 charset；
- 所有模板共享同一 DOM；
- 所有用户都修改过模板；
- 当时依赖 IE-only / ActiveX；
- 平台支持 Java Applet；
- Flash 一定由平台原生组件托管。

没有 capture / header / 原 HTML 时，浏览器和编码仍必须写 **unknown**。

---

## 5. 个性二级域名 ≠ 实际页面路径：一个很有价值的 URL ownership 证据

B1 给出的测试实例表明，BlogCN 可以向用户展示类似：

```text
<user>.blogcn.com
```

这样的个性地址，但实际访问会进入类似：

```text
www.blogcn.com/userNN/<user>/index.html
```

的路径结构。

为避免不必要暴露普通账号，本仓只保留抽象 pattern，不复写测试文章里的账号名。

这是一个很重要的托管平台结构：

```text
user-facing identity locator
  <user>.blogcn.com
        |
        | redirect / mapping observed by tester
        v
platform-controlled served path
  www.blogcn.com/userNN/<user>/index.html
```

当前能安全声称：

> 至少在 2005 年该测评所测试的 BlogCN 账号中，用户可获得个性二级域名，而实际访问被导向平台 `www.blogcn.com` 下的分片式用户路径。

不能继续声称：

- `userNN` 一定代表数据库 shard；
- 二级域名通过 DNS CNAME 实现；
- 跳转一定是 HTTP 301/302；
- 所有账号都使用相同规则；
- `index.html` 是静态文件而非动态生成 / rewrite 的表面路径。

这些都需要历史 HTTP / DNS / capture 证据。

### 为什么它重要

博客时代的 URL 所有权比个人主页更集中。表面上用户拥有一个“像自己域名”的入口，但真正页面命名、目录结构、模板系统、数据存储和长期存续都由平台控制。

因此 M2 的 URL ownership 比较至少需要区分：

```text
vanity identity URL
canonical / served URL
operator-owned namespace
content ownership
exportability
post-shutdown redirect / tombstone
```

不能只问“用户有没有独立二级域名”。

---

## 6. 2005：从全免费托管向收费分层扩展，但不是“免费博客当年已经退出”

2005-06-16 新浪科技报道 BlogCN 推出 M-RABO 与 RABO，并明确把它描述为收费服务，称这突破了平台过去一贯的免费模式。

Source:

- 新浪科技，`中国博客网发布M-RABO和RABO 面向225万用户`，2005-06-16.  
  <https://tech.sina.com.cn/i/2005-06-16/1301637805.shtml>  
  Accessed 2026-09-17. Evidence: **B**.

报道中的 225 万注册用户是平台方面的口径，本文只记为：

> **operator claim reported by media**

而不是独立测量。

更可靠的结构性结论是：

```text
free hosted-blog baseline
      +
paid / value-added service layer
```

在 2005 年已经并存。

这不能被压成“BlogCN 从 2005 年开始收费，所以免费博客结束”。2012—2013 的免费服务退出公告本身就反证了免费层仍长期存在。

---

## 7. 2008：中文品牌更名，但没有证据证明域名同时迁移

2008-12-30 新浪科技报道：中文博客托管服务商中国博客网 `Blogcn.com` 正式更名为“博尚网”，同时改版首页；报道引用其官方博客，并称公司负责人确认变化。

Source:

- 新浪科技，`中国博客网更名为博尚网`，2008-12-30.  
  <https://tech.sina.com.cn/i/2008-12-30/14502705399.shtml>  
  Accessed 2026-09-17. Evidence: **B**.

这条证据支持：

```text
brand label
  中国博客网 -> 博尚网

service/domain identity in report
  Blogcn.com remains in use
```

因此不能画成：

```text
中国博客网 -> 新品牌 -> 新域名
```

目前更稳的是：

> **品牌层变化并不自动等于域名层迁移。**

这和西祠 `.net/.com` 的案例一样，说明平台谱系至少要把 brand、domain、operator、served host 分开建模。

---

## 8. 2012—2013：免费服务退出公告存在，但“数据到底哪天被删”没有被证明

这是本轮最有价值的证据冲突。

### 8.1 公告内容：停止免费服务 + 导出期限 + 计划不再保留数据

多个 2012 年 12 月和 2013 年 3—4 月的近同时代来源转述 BlogCN 公告，核心内容一致：

- 停止免费博客服务；
- 免费用户需要在 2013-03-31 前导出 / 备份；
- 计划从 2013-04-01 起不再开放导出，并不再保留免费博客数据；
- VIP / 收费用户继续获得服务。

可定位来源包括：

- 卢松松博客，`Blogcn宣布终止免费服务`，2012-12-13.  
  <https://lusongsong.com/blog/post/523.html>  
  Evidence: **B**, near-contemporary quotation of operator notice.
- cnBeta（稿源标搜狐 IT），`博客时代已逝！Blogcn宣布终止免费服务`，2012-12-13.  
  <https://www.cnbeta.com.tw/articles/tech/217949.htm>  
  Evidence: **B**, likely same announcement family; not counted as an independent confirmation of the underlying operator event.
- 中国互联网协会，`中国博客网今日起停止免费服务 清除免费数据`，2013-04-01.  
  <https://www.isc.org.cn/article/25313.html>  
  Evidence: **B**.
- 中国广播网，`中国博客网今日将关闭所有免费博客 并将清除数据`，2013-03-31.  
  <https://china.cnr.cn/ygxw/201303/t20130331_512264298.shtml>  
  Evidence: **B**.

### 8.2 一个 provenance 小冲突：原公告日期并不一致

2012-12-13 的卢松松 / cnBeta 页面都把公告描述为当日发生；但中国互联网协会 2013-04-01 的文章明确写“2012 年 12 月 19 日”宣布停止免费博客服务。

本轮没有找到并直接核验 BlogCN 原始公告页面，因此不能擅自决定哪一个日期是原始公告的准确 publication date。

当前应写：

```text
operator notice existed by 2012-12-13 in near-contemporary circulation
exact original notice publication date = unresolved (12-13 vs 12-19 in secondary sources)
```

而不是把任意一个二手日期升级为 A。

### 8.3 3 月 31 日的新闻说“将删除”，不能证明删除已经执行

中国广播网在 2013-03-31 报道“今日将关闭所有免费博客，并将清除数据”。这能证明当时媒体根据公告预期该事件将在截止日发生。

它不能证明：

- 后台删除 job 已执行；
- 所有账号在同一秒变成不存在；
- 历史静态页面同时返回 404；
- vanity URL 同时失效；
- 数据库、备份、副本、搜索索引都已清除。

### 8.4 4 月 1 日 / 4 月 2 日出现了直接反证：删除被推迟

第一财经日报 2013-04-02 报道称，BlogCN 在 4 月 1 日发布声明，在回复完用户来信前“暂缓清除免费用户数据”；记者同时从 BlogCN 登录首页观察到，用户数据清除可以延后至 **7 月 1 日**。

Source:

- 第一财经日报，`中国博客网告别免费午餐 用户数据清除延至7月1日`，2013-04-02.  
  <https://www.yicai.com/news/2597436.html>  
  Accessed 2026-09-17. Evidence: **B with contemporaneous reporter observation**.

这条来源非常关键，因为它和“3 月 31 日全部删除完成”的叙述不只是语气差异，而是状态冲突。

因此本轮结论必须是：

> **免费服务的政策退出与导出截止是有证据的；但所有免费数据实际完成删除的精确日期，本轮未证实。**

至少需要拆成：

```text
T1  stop accepting / serving free entitlement
T2  announced export deadline
T3  actual export disabled
T4  deletion job scheduled
T5  deletion deferred
T6  actual account/database purge
T7  public URL stops serving historical content
T8  backup / internal residue disappears
```

目前证据只稳定覆盖其中部分状态。

### 8.5 7 月 1 日以后发生什么？本轮不知道

第一财经提供了延期至 7 月 1 日的同期观察，但本轮没有找到可靠、可定位的 2013-07-01 后续 operator notice、记者复核、Wayback tombstone 或 Common Crawl 结果来证明：

- 7 月 1 日当天是否真的执行；
- 执行是否一次完成；
- 免费用户 URL 是否统一失效；
- 是否出现 tombstone / redirect / VIP upsell；
- 是否仍有部分静态页面、RSS、图片或搜索结果残留。

所以：

> **“2013-03-31 BlogCN 删除全部免费博客数据”不能作为本仓已经证明的历史事实。**

---

## 9. “已证实 / 高概率 / 不知道”

### 已证实（在本轮证据强度范围内）

1. **2004-03-13 晚间 BlogCN 公开页面确实出现停服状态。**  
   A1 同时代截图支持。

2. **2004-03-18 前后，至少在 ONI 的测试中，BlogCN 不是简单的网络不可达，而是站点可达、正常内容被临时停服信息替代。**  
   A2 支持。

3. **2005 年 BlogCN 已经是功能较完整的 hosted-blog platform，包含 RSS、Trackback、模板、评论、归档、图片上传和一定社交 / 团队功能。**  
   B1 支持。

4. **2005 年测试中，BlogCN 的个性二级域名可以映射 / 跳转到平台 `www.blogcn.com/userNN/...` 路径。**  
   B1 支持；实现机制未知。

5. **2008-12 中国博客网中文品牌更名为博尚网；同期报道仍使用 Blogcn.com 作为服务标识。**  
   B3 支持。

6. **2012 年底 BlogCN 已公开传播停止免费服务、要求免费用户导出数据的通知。**  
   B4/B5 多个近同时代来源支持。

7. **2013-04-01 前后的实际删除状态与早先公告不一致：第一财经记者观察到删除被延期，页面给出 7 月 1 日的新期限。**  
   B7 支持。

### 高概率但仍需要 artifact 级核验

1. `blogcn.com` / `www.blogcn.com` 在多个阶段持续作为平台主域 / 服务域，而品牌名发生变化。
2. 个性二级域名主要是平台提供的身份入口而非用户独立控制的 host；但 DNS / redirect 技术细节仍缺。
3. 免费服务退出并非一个单一瞬间，而是 entitlement、export、retention、URL serving 分阶段变化。

### 不知道

1. 2004 tombstone 的 HTTP status、`Content-Type`、charset、HTML/frameset、缓存策略。
2. 2005 BlogCN 页面实际 charset；是否 GB2312 / GBK / UTF-8。
3. 个性二级域名是 DNS wildcard、server rewrite、HTTP redirect、meta refresh 还是 JS 跳转。
4. `userNN` 的技术含义。
5. BlogCN 是否存在 IE-only、ActiveX、Java Applet 的平台级依赖。
6. 用户模板中的 Flash 等内容是平台功能还是用户自行嵌入；本轮没有 artifact 级证明。
7. 2012 停止免费服务原公告的精确首次发布日期（12-13 与 12-19 二手记录冲突）。
8. 2013-07-01 是否实际完成了所有免费数据清除。
9. 免费博客 URL 在退出后具体返回 404、redirect、VIP 提示还是其他 tombstone。
10. 历史图片、RSS、评论、Trackback、附件等子资源比主 HTML 多存活了多久。

---

## 10. 后来回忆 vs 同时代证据

后来用户回忆中，BlogCN 常被记作：

- 每个用户有显眼的二级域名；
- 页面可高度自定义；
- 可以折腾 HTML / Flash 等视觉元素。

这些属于 **C 级经验记忆**，本身不能决定 2005 年技术实现。

但这一次有一个很好的交叉核验：

- C 级记忆说“有个性二级域名、可改页面”；
- 2005 年 B1 hands-on review 独立记录了个性网址、模板代码编辑，并观察到二级域名访问进入平台路径。

因此可以把较窄的 claim 提升为：

> **“BlogCN 在 2005 年确实向用户提供个性 URL 与模板级自定义能力。”**

但不能因为后来有人记得 Flash，就进一步写：

> “BlogCN 平台的标准页面依赖 Flash / ActiveX。”

那仍需要历史页面 artifact。

---

## 11. 可复原到什么程度

### 当前可以复原

- 2004 temporary shutdown 的**状态模型**：网络可达与内容不可用分离；
- 2005 hosted-blog 的主要功能层；
- 个性 URL 与平台路径的二层 locator 结构；
- 2005 免费 + 收费服务分层；
- 2008 brand rename 但域名没有已证实迁移的谱系；
- 2012—2013 free-service exit 的 policy / export / retention deadline；
- “公告删除日期”与“实际延期”之间的证据冲突。

### 当前不能复原

- 任何一个具体普通用户博客的完整历史页面；
- 2004 / 2005 / 2008 / 2013 的 DOM 与 CSS 级页面形态；
- 所有模板；
- 图片、音乐、Flash、评论等资源的完整性；
- 真实浏览器渲染；
- 精确 charset；
- 2013 删除 job 的后台执行过程。

因此本轮结果仍然是**平台结构与失踪链研究包**，不是视觉复原。

---

## 12. Browser / encoding / plugin assumptions

当前状态必须明确写为：

```text
historical charset        = unknown
HTTP Content-Type         = unknown
IE-only requirement       = not proven
ActiveX dependency        = not proven
Java Applet dependency    = not proven
Flash platform dependency = not proven
frameset usage            = not verified
historical viewport       = unknown
```

B1 能证明模板代码可编辑，所以未来浏览器实验尤其需要注意：

> **一个用户 BlogCN capture 的浏览器行为，不一定代表 BlogCN 平台的标准模板行为。**

用户模板、用户插入对象、平台默认代码、archive rewrite 必须分层记录。

---

## 13. Archive gap 与下一轮 bounded retrieval

本轮没有直接打开并核验目标年份的 Internet Archive / Common Crawl capture，因此不制造“已经看过 Wayback”的假象。

下一轮如果继续 BlogCN，只做以下 bounded artifact work，不继续泛搜怀旧文章：

1. **2004-03-13 / 03-18 tombstone**  
   - `http://www.blogcn.com/`  
   - `http://blogcn.com/`  
   目标：HTTP status、title、charset、页面文本、主文档与图片资源是否同 capture。

2. **2005-03 / 06 托管结构**  
   - homepage / registration / help 页面；
   - 只选评测作者自有测试账号或平台公开 demo，不批量打开普通用户博客；
   - 验证 `<user>.blogcn.com` → `www.blogcn.com/userNN/...` 到底是 30x、HTML、meta refresh 还是 JS。

3. **2008-12-30 rename anchor**  
   - 检查首页 title / logo / brand；
   - 验证 `blogcn.com` 是否仍直接 serving，是否发生 host redirect。

4. **2012-12 / 2013-03 / 2013-04 / 2013-07 service notice**  
   - 找原始“停止免费服务”公告 capture；
   - 找 4 月延期公告 / 登录首页；
   - 找 7 月 1 日之后的 tombstone 或 surviving free-blog sample；
   - 将 announcement time、capture time、actual page state 分开。

5. **Common Crawl 交叉核验**  
   - 只检索上述 host / anchor date；
   - 不做大规模用户 URL 枚举；
   - 用于验证 URL 是否仍被抓到以及响应 metadata，不把 Common Crawl hit 当视觉完整性证明。

---

## 14. 不能声称已经证明的内容

本轮禁止写成确定事实的句子包括：

- “BlogCN 在 2004 年被整个互联网层面封锁，所以完全无法访问。”
- “2004 停服时用户数据已经被删除。”
- “BlogCN 的用户二级域名就是独立虚拟主机。”
- “`userNN` 就是数据库分片编号。”
- “BlogCN 当年必须使用 IE / ActiveX。”
- “BlogCN 标准模板依赖 Flash。”
- “中国博客网在 2008 年换了新域名。”
- “2012-12-19 是原始公告无争议的准确首次发布日期。”
- “2013-03-31 / 04-01 所有免费博客数据已经实际删除。”
- “2013-07-01 已经确认执行全部清除。”

其中最后三项尤其重要：旧网失踪研究最容易把**公告日期**错当成**artifact disappearance date**。

---

## 15. 隐私与版权边界

### 隐私

- 不批量枚举历史 BlogCN 用户二级域名；
- 不重新公开已删除的普通用户博客正文、联系方式、照片或评论；
- 为证明 URL pattern，只保留 `<user>` 抽象形式；
- 未来 archive sample 优先使用平台官方、帮助页、测试者自有账号或已经公开用于技术说明的页面。

### 版权

- 不把 Wang 的 2004 截图复制进仓库，只引用原页面；
- 不复制 ChinaByte / 新浪整篇评测；
- 不镜像 BlogCN 历史图片、模板、音乐、Flash；
- archive 可访问不等于可以重新分发；
- 优先保存 URL、capture metadata、摘要和研究者测量结果。

---

## 16. 建议写入位置

当前只新增本 research note，不提前修改 M1 checklist。

后续 artifact 证据足够后，可拆成：

```text
cases/blogcn/
├── README.md
├── evidence.yaml
├── timeline.md
└── reconstruction.md
```

并可向 M2 `studies/platform-genealogy.md` 提供至少三个结构节点：

```text
2004  reachable host + replacement tombstone
2005  vanity subdomain + platform-controlled served path
2008  brand rename without proven domain migration
2012-2013  free entitlement/export/deletion states diverge
```

---

## 17. 本轮最小结论

BlogCN 的历史不是一句“2002 开站，2013 免费博客被删”可以概括的。

更符合现有证据的结构是：

```text
2002+ hosted blogging service
   |
2004 temporary suspension
   |-- host/network can remain reachable
   |-- normal content can be replaced by tombstone
   |
2005 mature BSP
   |-- platform templates / RSS / Trackback / comments / images
   |-- vanity <user>.blogcn.com
   |-- platform path www.blogcn.com/userNN/<user>/...
   |-- paid layer added alongside free service
   |
2008 brand rename: 中国博客网 -> 博尚网
   |-- no proven simultaneous domain migration
   |
2012 late: free-service exit notice circulates
   |-- secondary sources disagree on exact original notice date
   |
2013-03-31 announced export/deletion cutoff
   |
2013-04-01 deletion deferred in contemporaneous observation
   |
2013-07-01 later deadline
   |
actual final purge / URL disappearance = not yet verified
```

对旧网考古而言，本轮最可复用的结论不是“BlogCN 最后衰落了”，而是：

> **站点可达性、页面可见性、用户 URL、服务资格、数据导出、数据保留和实际删除必须作为不同历史状态记录。一个公告里的截止日期，不能自动替代真正的 artifact disappearance evidence。**
