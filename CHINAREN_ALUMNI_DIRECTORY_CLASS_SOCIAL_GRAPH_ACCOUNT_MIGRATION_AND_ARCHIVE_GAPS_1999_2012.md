# ChinaRen 校友录：班级社交图、账号迁移、离校认证与档案缺口（1999—2012）

> Scope：本文严格服务于 `old-web-archaeology` 的约 1995–2015 中文互联网主范围。
>
> 对应的普通生活史、海外 Friends Reunited 对照、2018–2026 微信群/朋友圈关系边界见：
> https://github.com/tmzncty/how-people-lived/blob/main/topics/from-paper-address-books-to-hosted-class-social-graphs-alumni-directories-relationship-portability-and-platform-memory-china-1980-2026.zh-CN.md
>
> 本文不是“中国社交网络通史”。它把 ChinaRen 校友录作为一个 **M1 platform/community case** 来处理：研究 `学校 → 班级 → 成员 → 资料/留言/相册/联系方式` 这套关系基础设施怎样存在、变形、与账号体系耦合，以及为什么今天最容易留下的是公开壳，而不是班级内部真实社会关系。

---

## 0. M1 case status

ROADMAP 对 M1 完整案例要求：

- 身份确认；
- 至少两个历史时点；
- 尽量两个独立 evidence family；
- 资源缺失清单；
- 浏览器/编码/插件假设；
- “已证实 / 高概率 / 不知道”；
- 同时代材料与后来回忆的比较。

本案当前已经达到：

- **平台身份：强**；
- **历史时点：2000 / 2001 / 2004 / 2006 / 2007 / 2009 / 2012，多时点强**；
- **独立证据 family：平台官方 + 同期教程 + 同期论坛技术 artifact + 同期个人博客 + 同期媒体，强**；
- **页面/浏览器线索：2004 HTML dump 可提供 charset、table layout、外链资源和脚本线索，中等强度**；
- **真正 archive memento：本轮仍未取得可复核 Wayback capture，因此不把 M1 标成完全闭环**；
- **登录后班级内容：因隐私和 archive 限制，不追求批量恢复普通人的留言与联系方式**。

结论：这是一个**研究包已经成立、archive replay 仍缺口明确**的 M1 候选完整案例。

---

## 1. 研究单位

按 `docs/METHOD.md`，不能把品牌、域名、账号和某次页面表示混成一个对象。

### 1.1 Platform

`ChinaRen / ChinaRen 校友录`

平台最初由 ChinaRen.com 运营，2000 年被搜狐收购后继续作为搜狐体系中的青年/校友社区产品存在。

### 1.2 Historical brands / product labels

至少见到：

- ChinaRen.com；
- ChinaRen 校友录；
- 普通校友录 / 超级校友录；
- ChinaRen 校内；
- ChinaRen 空间；
- 手机校友录；
- 班级博客圈等。

同名品牌跨年份不能默认同一技术架构。

### 1.3 Known historical hosts / URL families

从同期材料可确认或强提示：

- `chinaren.com`
- `www.chinaren.com`
- `alumni.chinaren.com`
- `class.chinaren.com`
- `mail.chinaren.com`
- `profile.chinaren.com`

其中：

`host exists at one date != same endpoint/schema at another date`。

### 1.4 Account

至少涉及：

- ChinaRen 用户；
- 搜狐/ChinaRen 邮箱账户复用；
- 登录态；
- 账号激活/身份验证；
- 后期搜狐互动产品统一账号/昵称方向。

### 1.5 School

学校是可搜索和归类的制度实体。

需要区分：

- 学校数据库中存在；
- 页面可打开；
- 有班级；
- 有成员；
- 学校名称/合并/改名后的映射是否正确。

### 1.6 Class

班级是核心关系容器。

已知功能在不同时期可能包括：

- 创建班级；
- 加入班级；
- 管理员；
- 留言；
- 班级相册；
- 成员通讯录；
- 群发邮件/短信；
- 共享资源；
- 聊天；
- 班级动态；
- 博客聚合。

### 1.7 Member profile

成员可能具有：

- 昵称/姓名；
- 学校/班级身份；
- 邮箱；
- 联系方式；
- 个人空间；
- 头像；
- 日志/博客；
- 加入班级关系。

普通人的联系方式属于本案明确的隐私最小化边界，不批量再发布。

### 1.8 Capture / artifact

必须单独记录：

- archived page；
- 同期新闻中的截图；
- 同期教程截图；
- 用户论坛粘贴的 HTML；
- 后来研究文章转载的旧图；
- 今天仍在线的历史博客正文。

这些证据强度不同。

---

## 2. 身份与时间线

### 2.1 1999：平台起点

后来的多份行业资料都把 ChinaRen 创办时间放在 1999 年；本轮不依赖单一回忆来确定精确上线日。

当前最可靠的同期锚点从 2000 年官方收购材料开始。

### 2.2 2000-09-14：搜狐官方宣布收购 ChinaRen

搜狐同期官方专题写明 2000 年 9 月 14 日正式签署收购协议，并把 ChinaRen 称为年轻人社区，强调其社区服务与用户群。

证据等级：**A（平台官方同期）**。

来源：

- https://news.sohu.com/feature/merge/merge.htm
- 同期搜狐合并新闻：
  https://www.sohu.com/a/307984376_120136162

边界：

- 能证明搜狐当时怎样描述并收购 ChinaRen；
- 不能把“780 多万注册用户”“每天 4400 万 PV”等平台数字自动当作独立审计统计。

### 2.3 2001-11：普通校友录与“超级校友录”出现状态分层

《网络报》2001 年 11 月报道搜狐推出收费“超级校友录”，普通班级可通过点数升级，报道同时记录了用户对价格的质疑。

证据等级：**B+（同期行业/媒体）**。

来源：

- https://tech.sina.com.cn/i/c/2001-11-19/92494.shtml

这说明班级并非只有：

`存在 / 不存在`

两个状态，还至少有：

`普通班级`

`升级条件满足`

`超级班级已激活`

等服务等级。

因此旧页面上出现“超级校友录”入口，不代表目标班级已经付费或处于高级状态。

### 2.4 2004-06：同期教程确认公开入口与学校/班级搜索路径

PChome 2004 年教程明确记录：

- `http://alumni.chinaren.com` 为校友录入口；
- 新用户可注册；
- 搜狐或 ChinaRen 邮件用户可复用用户名密码；
- 用户可以搜索/创建“我的大学 / 我的中学 / 我的小学”班级。

证据等级：**B+（同期用户操作教程）**。

来源：

- https://m.pchome.net/article/content-17875-all.html

这是目前非常重要的结构证据：

`mail account identity`

与

`alumni/class membership`

已经可以在一个门户账号体系中连接。

### 2.5 2004-12：LinuxSir 论坛保留了异常情况下的 ChinaRen/Sohu HTML 片段

2004 年 12 月 LinuxSir 用户讨论 Fedora Core 3 下打开搜狐/ChinaRen 页面出现异常。帖子搜索索引保留了一大段当时页面 HTML。

证据等级：**B+/artifact-like contemporary evidence**。

来源：

- https://www.linuxsir.cn/forum.php?mod=viewthread&page=1&tid=167101

当前可观察片段提示：

- 页面声明 `charset=gb2312`；
- 大量 table 布局；
- 可见约 760px 固定宽度级布局线索；
- 引用搜狐/ChinaRen 图片 host；
- 可见 `mail.chinaren.com`、`alumni.chinaren.com/mobile/sms_alumni.jsp`、收费同学搜索、校园频道等链接；
- 存在 cookie/login 相关 JavaScript 与外部 profile script；
- 页面中曾泄出类似 `sohu_cms_include` 的模板标记。

最后一项只能表述为：

> **可见服务端模板/include 标记未正常展开的迹象。**

不能仅凭论坛 HTML dump 断言具体是哪一层 CMS 故障。

同时必须注意：

`论坛粘贴的 HTML != 原站 archive capture`。

它可能被论坛编码、转义、截断或二次处理。

### 2.6 2005：网上班级已被用于实习、毕业后的持续协调

2005 年《解放日报》报道复旦、同济和武汉大学班级使用网上同学录。武汉大学 1996 级广电班毕业生去了甘肃酒泉后，仍通过网上班级与各地同学持续联系。

证据等级：**B+（同期新闻 + 第一人称）**。

来源：

- https://news.sina.com.cn/s/2005-03-18/09105394097s.shtml

对 old-Web 的意义不是证明普及率，而是证明：

`class page exists`

至少在部分真实用户那里已经变成：

`class page used after geographic dispersal`。

### 2.7 2006-09：离校后身份验证可把真实校友挡在班级外

一名 2000 年毕业的长期用户 2006 年在新浪博客记录：登录 ChinaRen 后进入班级时，被要求使用学校网络/学校邮箱激活；本人已经毕业，无法满足当前在校条件，尝试其他校友验证仍循环失败。

证据等级：**B+（同期第一人称操作记录；页面目前仍在线，但今天的新浪外壳不是 2006 年页面呈现）**。

来源：

- https://blog.sina.com.cn/s/blog_467006df0100061q.html

这个案例固定一个非常重要的 state gap：

`real-world alumnus`

`account login success`

`school affiliation proof`

`class-membership authorization`

是四个不同状态。

不能把“账号还能登录”写成“旧班级还能访问”。

### 2.8 2007：产品公开宣称 Web 2.0 化

ChinaRen 2007 年改版同期稿称：

- 2006 年过程中首页从 table 结构迁向 DIV+CSS；
- 使用 Ajax；
- 新增/强化班级相册、班级动态、隐私设置；
- 与搜狐博客/班级博客圈互通。

证据等级：**A-/B（平台体系同期产品稿；适合证明官方宣称的改版方向，不独立采信宣传规模）**。

来源：

- https://www.sohu.com/a/307988831_120136162

这给浏览器复原留下明确的跨年差异：

> 不能用 2007 的 DIV+CSS/Ajax 假设回放 2004 的 table 页面，也不能反过来。

### 2.9 2009：ChinaRen 从班级目录继续向“空间”扩展

2009 年同期记者观察到 ChinaRen 登录后增加“空间”，并把搜狐博客 feed 导入；班级管理员可添加来自开放平台的 widget。

证据等级：**B+（同期记者操作观察）**。

来源：

- https://tech.sina.com.cn/i/2009-02-24/13392853423.shtml

因此 2009 年的对象模型至少变成：

`class membership graph`

+

`person-centered space`

+

`external blog feed`

+

`widget/open-platform modules`。

这不是 2004 页面简单换皮。

### 2.10 2012：关停成为共同记忆保存问题

本轮找到 2012 年 2 月的同时代用户公开信，作者描述 ChinaRen 社区关闭决定及对多年用户内容失去归属的担忧。

该材料目前用于：

- 证明**用户当时已经把平台数据视作长期共同记忆**；
- 证明关停时存在强烈的数据连续性焦虑。

它**不能单独证明**：

- 搜狐官方最终关停时间；
- 全部服务是否同日关闭；
- 全部数据是否立即删除；
- 是否存在完整导出窗口。

后来的 MediaChina 专题把这封信与旧截图整理到一起，可作为 C 级研究汇总：

- https://mediachina.today/2022/chinaren

---

## 3. 页面与功能模型

### 3.1 Public entry

可能包括：

- ChinaRen 首页；
- 校友录首页；
- 登录/注册；
- 学校搜索；
- 学校列表；
- 产品说明；
- 收费升级说明；
- 移动/短信服务；
- 帮助和 FAQ。

### 3.2 Authenticated account

可能包括：

- 用户资料；
- 已加入班级；
- 创建/申请加入班级；
- 个人空间；
- 账号验证；
- 密码/cookie/session。

### 3.3 Class state

至少区分：

`class record exists`

`class page exists`

`class has admin`

`membership request exists`

`membership approved`

`user can enter`

`user can read member directory`

`user can post`

`user can access album`

`user can send group message`

`class upgraded / premium`

`class archived / inactive`

`class data removed`。

### 3.4 Member relationship

平台“同班”至少可能来自：

- 用户自行选择；
- 管理员审核；
- 旧数据库迁移；
- 学校邮箱/网络身份验证；
- 其他同学推荐或邀请。

因此：

`same online class != independently verified real-world classmate`

除非证据说明当时的验证强度。

### 3.5 Communication channels

同期 HTML/教程/研究线索显示，ChinaRen 生态不只依赖网页留言，还可能包括：

- mail；
- class mail/group mail；
- SMS/mobile alumni；
- chat；
- blog/feed；
- later personal space。

所以一次 class-page capture 不能代表完整通信行为。

---

## 4. 长期可复用的 state gaps

### 4.1 `school-record / real-school gap`

平台学校库里有一个名称，不等于：

- 名称在当年没有歧义；
- 合并/改名关系正确；
- 用户选的是同一所现实学校。

### 4.2 `class-record / active-class gap`

班级被创建，不等于：

- 有同学加入；
- 有管理员维护；
- 有持续内容。

2004 CFC 论坛直接留下“开了班站但没人来”的反例：

- https://bbs.comefromchina.com/threads/278456/

### 4.3 `account-login / class-access gap`

账号登录成功，不等于能进入原班级。

2006 离校用户的激活失败是明确证据。

### 4.4 `real-alumnus / platform-verifiable-alumnus gap`

一个人现实中毕业于该校，不等于平台当前认证方法还能证明这一点。

如果认证依赖：

- 校园 IP；
- 学校邮箱；
- 在校状态；

那么真正离校的人可能反而最难通过。

### 4.5 `profile-findability / authorized-contact gap`

按学校和姓名找到账号，不等于对方愿意被这个人联系。

可发现性与同意必须分开。

### 4.6 `classmate-findability / public-searchability gap`

为了让旧同学找到自己而提供学校/联系方式，不等于同意第三方搜索引擎、数据聚合者或陌生人无限索引。

2005 年 5460 资料外泄/聚合争议是同类早期风险。

### 4.7 `friend-link / active-relationship gap`

同学/好友关系仍存在，不等于持续互动。

### 4.8 `class-content / offline-relationship gap`

班级留言活跃，也不能自动证明成员在线下仍频繁见面。

反过来，网页冷清也不能证明同学失联，因为他们可能已迁到 QQ、电话或线下。

### 4.9 `premium-label / premium-state gap`

页面展示“超级校友录”产品，不等于当前班级已激活付费状态。

### 4.10 `platform-brand / technical-system gap`

2000 ChinaRen、2004 Sohu/ChinaRen、2007 Web2.0 ChinaRen、2009 ChinaRen Space 必须按时点拆开。

### 4.11 `account-migration / content-migration gap`

平台说账号或用户资料“无缝迁移”时，也不能自动推出：

- 班级留言；
- 相册；
- 私信；
- 历史时间戳；
- 权限；
- 删除状态

全部无损迁移。

### 4.12 `relationship-survival / archive-survival gap`

同学可能全部迁到 QQ/微信，关系继续；旧班级历史却消失。

反过来，一张旧班级 HTML 可能幸存，人际关系早已结束。

### 4.13 `current-page / historical-rendering gap`

今天仍能打开的 2006 新浪博客证明正文内容和平台保存状态，不等于 2006 年用户看到的页面 CSS、广告、脚本、字体和布局。

### 4.14 `HTML-dump / original-response gap`

论坛粘贴的 HTML 可以保留非常珍贵的 host、charset、链接和脚本线索，但不是原站 HTTP response 的可替代品。

---

## 5. 2004 artifact reconstruction: what can we safely say?

### 5.1 Artifact

LinuxSir 2004-12 线程保存了用户在 Fedora Core 3 环境下访问 Sohu/ChinaRen 时得到的异常页面内容。

来源：

- https://www.linuxsir.cn/forum.php?mod=viewthread&page=1&tid=167101

### 5.2 可观察技术线索

当前索引片段支持：

- GB2312 页面声明；
- table-heavy layout；
- ChinaRen/Sohu 多 host 子资源；
- 登录/cookie JavaScript；
- `mail.chinaren.com` 等统一服务入口；
- 校友录移动/SMS服务；
- 外部 profile script；
- 页面模板/include 未正常渲染的迹象。

### 5.3 不能证明

不能据此证明：

- 原服务器的完整 HTML；
- HTTP header；
- 精确响应状态；
- 正常 IE6 下视觉外观；
- CSS/JS 是否全部加载；
- 页面故障究竟发生在服务端、代理、编码还是客户端；
- 该 HTML 对所有访问者都相同。

### 5.4 Browser assumptions

2004 页面复原至少要测试：

- IE6/Windows 级环境；
- contemporaneous Gecko/Mozilla/Fedora 环境；
- GB2312 解码；
- JavaScript/cookie；
- table layout；
- 第三方图片 host；
- archive URL rewriting。

不能只在 2026 Chromium 中加载一份重建 HTML 后称“历史体验已复原”。

---

## 6. 2007 artifact boundary: Web 2.0 transition

2007 产品稿称 2006 年改版过程中：

- 首页由 table 结构迁到 DIV+CSS；
- 大量 Ajax；
- 班级动态；
- 相册增容；
- 隐私控制；
- 博客互通。

来源：

- https://www.sohu.com/a/307988831_120136162

这意味着至少应有两个 browser-era fixture：

### Fixture A — 2004 legacy alumni shell

重点：

- GB2312；
- table；
- portal navigation；
- mail / alumni / SMS service links；
- 登录 cookie。

### Fixture B — 2007 Web 2.0 alumni shell

重点：

- DIV+CSS；
- Ajax；
- dynamic class updates；
- blog integration；
- potentially richer authenticated state。

不能把两者合成一个“经典 ChinaRen 页面”。

---

## 7. 2009 transition: class-centered → person-centered

2009 ChinaRen 空间材料显示，搜狐博客内容可以进入个人空间 feed，班级管理员也能加入 widget。

来源：

- https://tech.sina.com.cn/i/2009-02-24/13392853423.shtml

与此同时，校内网/人人网正把学校关系作为个人社交图的一部分，而不是唯一容器。

来源：

- https://tech.sina.com.cn/i/2009-08-04/14523321884.shtml

对平台谱系的意义：

```text
class container
    ↓
class + member profile
    ↓
class + personal space + feed
    ↓
person-centered SNS where class is one relation source
```

这是 `ROADMAP.md` 中：

`个人主页 → BBS → 托管博客 → 平台社区 → SNS/信息流`

之外另一个非常值得保存的中文路径：

`校友录 / 同学录 → 校园实名 SNS → 泛熟人 SNS`。

---

## 8. Preservation model

### S0 — only later description

只有后来文章说 ChinaRen 曾有某功能。

### S1 — contemporary text claim

同期新闻/教程明确描述功能，但无原页面。

### S2 — URL/host evidence

同期文档保留原 URL、host、链接结构。

### S3 — screenshot or copied fragment

同期截图、HTML dump 或教程图能看到页面结构的一部分。

### S4 — public-page memento

可验证 archive capture，包括 datetime、HTTP/replay、charset 等。

### S5 — subresource-complete public replay

HTML/CSS/JS/image 足够完整，可研究视觉与交互。

### S6 — authenticated structural evidence

合法、匿名化地保存登录后界面结构或官方手册，但不重新公开普通人的私人内容。

### S7 — transaction/state fixture

用测试/自有数据复原：创建班级、加入、管理员审核、登录、验证等状态转换。

### S8 — real private class archive

本项目原则上**不以公开恢复这一层为目标**。真实普通人的通讯录、私信、联系方式、照片和半私密班级留言需要隐私最小化。

当前本案：

- S1：强；
- S2：强；
- S3：中等（同期 HTML dump、后来的截图研究）；
- S4：本轮未完成；
- S5：未完成；
- S6：只有零散同期个人截图/叙述；
- S7：未来只能用 reconstruction/test fixture；
- S8：不追求公开。

---

## 9. Archive gaps

### 9.1 Public shell survives better than class life

最可能保存：

- 首页；
- 登录；
- 学校搜索；
- 产品稿；
- 帮助页。

最不容易保存：

- 登录后成员目录；
- 班级留言；
- 相册；
- 私信；
- 管理员审核；
- 用户隐私设置；
- 群发邮件/SMS 事务。

所以：

`archive sees a nearly empty shell`

不能推出：

`historical class was nearly empty`。

### 9.2 `closed-group archive invisibility`

校友录越认真保护班级隐私，公共 crawler 越不可能抓到真正社会生活。

这不是 archive 失败的单一技术问题，而是**隐私设计与历史可见性之间的结构性张力**。

### 9.3 Session / cookie loss

即使登录页完整：

`login form preserved != historical account can be authenticated`。

Cookie domain、SSO、HTTPS、验证码、后端用户库、学校验证接口都可能早已失效。

### 9.4 Dynamic/Ajax loss after 2006–2007

动态班级 feed、相册上传、开放平台 widget 等依赖 API/JS 后端。

HTML 壳幸存时，内容可能为空。

### 9.5 Cross-host dependency

2004 artifact 已显示多 host：

- `alumni.chinaren.com`
- `mail.chinaren.com`
- `profile.chinaren.com`
- Sohu 图片 host
- campus/learning 服务

archive 若只抓主文档，很容易出现“页面看似坏掉”。

### 9.6 Shutdown burst bias

2012 关停附近产生大量怀旧/失落文章；正常运行期的普通沉默使用反而更少进入公共新闻。

不能从留下来的文本比例推断情绪比例。

---

## 10. Privacy boundary

ChinaRen 特别容易诱导考古者去“证明一个班级真的存在过”，然后无意重新公开：

- 姓名；
- 手机；
- QQ；
- 邮箱；
- 家庭地址；
- 婚育状态；
- 照片；
- 私密留言。

本案明确不这样做。

优先保存：

- URL pattern；
- class/member object model；
- 字段名称；
- 页面结构；
- 权限规则；
- 测试/匿名 fixture；
- 用户自己公开发表、并且只截取研究所需最少部分的同期叙述。

2005 年公开报道已经证明校友服务的高可发现性可能转化为非预期个人数据暴露，因此隐私不是今天强加给旧网的道德补丁，而是**当时已经存在的历史问题**。

---

## 11. Contemporary evidence vs nostalgia

### 11.1 同时代使用材料告诉我们的

2005：

- 网上班级用于实习/毕业后协调；
- 也有人担心网上互动不能替代真实班级生活。

2006：

- 老用户确实持续查看谁读书、结婚、生子；
- 身份验证变化也会把毕业用户挡掉。

2008：

- 校内 SNS 已经进入部分大学生的每日时间表；
- 人们可通过关系链重新找到小学甚至幼儿园旧同学。

2009：

- 实名/学校搜索既帮助找师兄，也造成不安全感。

这些材料中的主体验是：

`方便、日常、时间占用、找人、看近况、认证麻烦、隐私`。

### 11.2 后来怀旧材料容易强化的

后来写 ChinaRen 时容易只剩：

- 青春；
- 80 后共同记忆；
- “中国 Facebook 前身”；
- 错失商业机会；
- 平台死亡。

这些并非全错，但会遮住一个更具体的普通生活事实：

> 当年用户真正做的往往只是每周去看看哪个同学换了城市、结婚了没有、班里有没有新照片。

M1 案例必须保留这种不起眼的日常层。

---

## 12. 海外对照只作为边界，不把本仓扩成全球旧网

英国 Friends Reunited 2000 年上线，同样以学校旧关系重连为核心。2009 年《Independent》回顾其起点时，创办动机就是想知道过去的同学后来怎样生活；2005 年 Guardian 报道也展示这类平台同样会出现假资料、骚扰和关系冲突。

来源：

- https://www.independent.co.uk/news/business/analysis-and-features/the-rise-and-fall-of-friends-reunited-1628278.html
- https://www.theguardian.com/technology/2005/jul/20/crime.uknews

本仓只用它来确认：

`school-indexed reconnection`

不是中国平台独有现象。

真正要考古的仍是中文站点自己的：

- URL；
- 编码；
- 页面结构；
- 账号系统；
- 手机/SMS 接口；
- 搜狐矩阵；
- 班级权限；
- 中文 Web 存档缺口。

---

## 13. Evidence ledger

| ID | Date | Source | Grade | Supports | Does not support |
|---|---|---|---|---|---|
| E1 | 2000-09-14 | 搜狐 ChinaRen 收购专题 | A | 收购、平台官方定位 | 注册量独立审计 |
| E2 | 2001-11-19 | 网络报/新浪“超级校友录” | B+ | 普通/付费班级状态、点数升级 | 实际付费转化率 |
| E3 | 2004-06-23 | PChome 教程 | B+ | `alumni.chinaren.com`、账号、学校/班级搜索 | 全国普及率 |
| E4 | 2004-09 | CFC 用户班站 | B+ | 班级创建后可能无人加入 | 普遍活跃率 |
| E5 | 2004-12 | LinuxSir HTML dump | B+/artifact | charset、链接、布局/脚本线索 | 原站完整 response/正常视觉 |
| E6 | 2005-03 | 解放日报 | B+ | 实习、毕业、跨地域使用；线下关系反例 | 全国用户结构 |
| E7 | 2006-09 | 新浪博客 | B+ | 账号可登录但班级认证失败 | 全部账号规则 |
| E8 | 2007-03 | 搜狐产品稿 | A-/B | DIV+CSS/Ajax、相册/动态/隐私/博客互通宣称 | 宣传规模 |
| E9 | 2009-02 | 计世网/新浪 | B+ | ChinaRen 空间、blog feed、widget | 全用户是否使用 |
| E10 | 2009-11 | 现代快报/新浪 | B+ | 实名学校图谱的找人与隐私双重作用 | 普遍风险率 |
| E11 | 2012-02 | 用户公开信 | B/C | 关停时用户的数据/记忆焦虑 | 官方关闭事务细节 |
| E12 | 2022 | MediaChina 专题 | C/research | 旧截图汇总、产品谱系线索 | 代替原始 capture |

---

## 14. 已证实 / 高概率 / 不知道

### 14.1 已证实

1. 2000 年搜狐官方宣布收购 ChinaRen。
2. 2001 年已有普通/超级校友录的服务等级区分。
3. 2004 年 `alumni.chinaren.com` 被同期教程作为校友录入口，支持按小学/中学/大学搜索或创建班级。
4. 2004 年同期论坛 artifact 保留 GB2312、table-heavy、多 host 和登录/移动服务等技术线索。
5. 2005 年有真实班级把校友录用于异地实习和毕业后联系。
6. 2006 年至少一名真实毕业用户遭遇“账号可登录、班级身份无法重新验证”的状态。
7. 2007 年平台公开宣称向 DIV+CSS/Ajax、班级动态、隐私和博客互通演进。
8. 2009 年 ChinaRen 已出现个人空间/feed 化方向。
9. 2012 年已有同时代用户把 ChinaRen 关闭理解为多年共同内容失去保存空间。

### 14.2 高概率但仍要进一步核

1. 2004 legacy alumni shell 与 2007 Web2.0 shell 的 DOM/CSS/JS 差异应当很大。
2. 登录后班级页比公开入口的 archive 覆盖显著更差。
3. QQ 群、校内/人人等承担了相当一部分关系迁移，因此 ChinaRen 页面变冷不等于旧同学失联。
4. 2012 关停对“关系本身”的损失小于对“共同班级 archive”的损失，但还缺用户迁移数据。

### 14.3 不知道

1. 1999 最早校友录的精确页面结构与 launch snapshot。
2. 2000–2003 班级 URL schema 是否有重大迁移。
3. 2004 正常 IE 环境中的精确视觉和 CSS。
4. 2006 学校网络/邮箱认证规则的官方说明和覆盖范围。
5. 2007 Ajax endpoint、参数和返回格式。
6. 2012 官方关停通知的原始页面、提前通知期、导出能力和数据清理事务。
7. 普通用户内容是否有 ArchiveTeam/独立 WARC 抢救项目；尚需系统查重。

---

## 15. Archive attempt in this slice

本轮搜索并尝试定位：

- `alumni.chinaren.com` 2004 前后；
- `chinaren.com` / `www.chinaren.com`；
- 2004 legacy shell；
- 2007 改版；
- 2012 关停。

当前 Web 访问链允许检索历史 URL 和二手引用，但直接构造 Wayback replay URL 时被 provenance 安全规则拒绝；搜索引擎也没有返回可直接跟随的目标 memento。

因此严格记录：

`M1 verified ChinaRen historical Wayback capture: NOT ACHIEVED IN THIS SLICE`。

这不等于：

`Wayback has no capture`。

也不等于：

`historical page did not exist`。

不能把 candidate locator 升级为 capture。

---

## 16. 下一步 M1 验收路线

### Step 1 — 先拿到两个 verified memento

优先：

- 2004 `alumni.chinaren.com` public shell；
- 2007 改版后的 public shell。

每个记录：

- archive source；
- capture URL；
- original URL；
- capture datetime；
- HTTP/replay status；
- charset；
- title；
- DOM/layout；
- script/CSS/image subresource completeness。

### Step 2 — 做 browser comparison

对 2004 capture：

- modern Chromium；
- IE6 级；
- contemporaneous Gecko/Netscape-compatible 环境。

重点观察：

- GB2312；
- table width；
- JS cookie/login；
- broken include；
- image host；
- archive rewrite。

### Step 3 — 匿名化 reconstruction

不要真实登录旧账号。

用假学校、假班级、假成员 fixture 重建：

`school search`
→ `class search`
→ `join request`
→ `membership approved`
→ `class home`
→ `member directory`
→ `post / album`
→ `verification failure`。

### Step 4 — shutdown evidence

寻找：

- 搜狐官方关停通知；
- 用户导出说明；
- 关停后 redirect / tombstone；
- 是否有 ArchiveTeam / WARC 记录。

---

## 17. 对 old-Web 总方法的新贡献

本案新增几个以后研究 SNS/BBS/群体平台都应复用的边界：

1. **`relationship graph != page graph`**：网页链接结构不等于社会关系结构。
2. **`real membership != platform-verifiable membership`**：现实身份和系统可验证身份可分离。
3. **`account survival != community survival`**：账号还能登录不代表原群体空间仍可访问。
4. **`community survival != content survival`**：人还联系不代表旧内容还在。
5. **`findability != consent`**：能搜到不等于有权无限联系或聚合资料。
6. **`private-by-design != historically inactive`**：登录后内容缺失不能当作社区冷清证据。
7. **`platform shutdown != social graph death`**：关系可能迁走，memory home 却可能消失。
8. **`later nostalgia != contemporary primary use`**：关停后的青春叙事不能覆盖当年的日常操作。
9. **`institutional authentication can expire before social belonging`**：学校邮箱和校园网身份会消失，校友身份却不会。
10. **`relationship portability can depend on platform portability`**：人已经跨城市移动，关系图仍可能被困在单一服务商里。

---

## 18. 与 how-people-lived 的交叉结论

从 old-Web 看，ChinaRen 是一个页面、账号、班级和数据迁移问题。

从普通生活史看，它解决的是一个更朴素的问题：

> **毕业以后大家各奔东西，过去的人还找不找得到。**

真正值得两仓共同保留的不是“ChinaRen 曾经很火”，而是状态变化：

```text
shared physical institution
    ↓ graduation / migration
address pointers decay
    ↓
school/class becomes searchable Web index
    ↓
class social graph is hosted by platform
    ↓
person-centered SNS inherits/expands graph
    ↓
mobile messaging keeps graph continuously reachable
    ↓
attention overload leads users to mute/prune visibility
```

旧网考古负责证明每一层当时具体是什么页面、host、编码、认证和保存状态；生活史负责回答这些技术层**到底让哪些人生更容易离开原地点而不必把全部过去留在那里**。

---

*Initial draft AI-assisted. This file deliberately stops short of claiming a verified historical memento until an archive replay is actually opened and inspected under the repository's METHOD contract.*
