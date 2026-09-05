# 1996—2015 中文个人主页：公开自我、访问指标与平台死亡的状态缺口

本文件补充：

- `docs/METHOD.md`；
- `docs/ACCOUNT_PORTABILITY_AND_LOCAL_RESIDUE_1999_2003.md`；
- `docs/AFFILIATION_CREDENTIAL_AND_ACCOUNT_LIFECYCLE_2001_2009.md`；
- `docs/FORUM...` 等论坛/SNS 状态研究。

主研究对象仍严格限定在约 **1995—2015 中文互联网**。GeoCities 只作为海外对照，不把本仓扩成全球旧网史。

对应 `how-people-lived`：

- `topics/personal-homepages-self-publishing-and-platformed-public-identity-china-1980-2026.zh-CN.md`

---

## 0. 为什么要把“个人主页”单独建模

仓库 ROADMAP 的 M1 明确要求至少完成一个“个人主页/主页托管案例”。但个人主页特别容易被后见之明误读，因为今天还能看到的往往只是：

- 一个 HTML 壳；
- 一个昵称；
- 一段“欢迎来到我的主页”；
- 几张幸存图片；
- 一个静态访问计数；
- 一些已经打不开的留言本/聊天室/下载链接。

这远远不足以证明当年的完整体验。

本文的核心规则是：

```text
person
≠ account
≠ homepage namespace
≠ page body
≠ asset set
≠ guestbook database
≠ counter state
≠ audience history
≠ archive capture
≠ current replay
```

个人主页看起来“比论坛帖子更像一个人”，但这种视觉直觉不能替代证据链。

---

# 1. 研究单位必须拆开

个人主页至少可能涉及以下对象：

1. **person / operator**：现实中的作者或维护者；
2. **hosting provider**：ISP、门户、学校、免费主页平台；
3. **account**：用于登录、上传或管理的账号；
4. **namespace / homepage slot**：如 `/~username/`、`/personal/name/`、二级域名；
5. **homepage root URL**；
6. **individual HTML page**；
7. **asset**：图片、音乐、下载文件、CSS、JS；
8. **interactive backend**：留言本、计数器、聊天室、投票；
9. **directory/search listing**：站内目录、排行榜、搜索收录；
10. **archive capture**；
11. **current surviving render**。

不能从：

```text
一个 URL 里有昵称
```

直接推出：

```text
已经确认现实身份
```

也不能从：

```text
主页 HTML 仍存活
```

推出：

```text
留言本、计数器、图片和当年访问行为也存活
```

---

# 2. 1999 同时代材料可以证明：免费个人主页、流量统计、留言本/计数器是真实服务形态

## 2.1 网易服务的同时代/近同时代证据

1999 年 2 月，丁磊在《生活时报》的第一人称文章中回顾网易初创阶段，明确说自己写了个人主页服务系统，包含：

- 计数器；
- 留言本；
- 免费个人主页空间。

来源：

- 丁磊，《我与网易（下）》，《生活时报》，1999-02-21：
  <https://www.gmw.cn/01shsb/1999-02/21/GB/896%5ESH3-2125.htm>

证据等级：**B：近同时代创办者第一人称回顾。**

同年 1 月《生活时报》列出的 CNNIC “十佳网站”说明，当时网易公开服务组合包括：

- 免费个人主页空间；
- 免费流量统计系统；
- 虚拟社区；
- 搜索；
- 免费邮箱等。

来源：

- 《十佳网站评出》，《生活时报》，1999-01-22：
  <https://www.gmw.cn/01shsb/1999-01/22/GB/867%5ESH14-211.htm>

证据等级：**B：同时代媒体。**

因此可以较稳妥写：

> 1999 年前后，国内大型网络服务商已经把“免费主页 + 流量/访问反馈 + 留言”作为真实的个人 Web 服务形态。

不能写：

> 1999 年所有网易个人主页都使用同一套计数器、同一 URL pattern、同一 charset、同一后台实现。

这些仍需要具体 capture / help page / code 证据。

---

# 3. CNNIC 1999 调查：个人主页已经是早期网民中的可测量实践，但绝不能外推到总人口

CNNIC 1999 年 7 月统计报告记录：

- 网上联机问卷共有 52,549 份有效答卷；
- 21.6% 受访者把“免费个人主页空间”列为常用网络服务之一；
- 24% 受访者表示拥有个人主页；
- 有主页者中，88% 放在国内网站，12% 放在国外网站。

来源：

- CNNIC，《中国互联网络发展状况统计报告（1999/7）》：
  <https://www.cnnic.cn/NMediaFile/old_attach/P020120612485127164902.pdf>

证据等级：**A：同期机构调查。**

但调查方法本身是：

- 网上问卷；
- 约 30 家国内站点在主页放置调查链接；
- 被调查者已经是当时能够上网并愿意参与调查的人。

所以安全写法是：

> 在 CNNIC 1999 年这批在线调查受访者中，个人主页已经不是不可测的极少数行为。

禁止写成：

> “1999 年中国 24% 的人/青年/网民有个人主页”。

对本仓尤其重要的是：

```text
surveyed user practice
≠ population prevalence
```

---

# 4. 2000 年近同时代回顾揭示：URL、空间、FTP 和平台迁移本身就是主页历史的一部分

杨震霆 2000 年对 1996—2000 中国个人主页的回顾记录了大量具体托管形态：

- GeoCities；
- 广东 ISP “视聆通”；
- 飞捷；
- 湛江个人主页空间；
- 网易等；
- `/personal/...`、`/~username` 等路径；
- FTP 自维护；
- 空间容量差异；
- 留言本、计数器；
- 服务停止、站点迁移、主页长时间不更新。

来源：

- 杨震霆，《中国最早的“十佳个人主页”流落何处》，新浪科技，2000-12-14：
  <https://tech.sina.com.cn/r/m/46310.shtml>

证据等级：**B/C：近同时代个人回顾。**

这份来源非常有价值，但不能单独证明其中所有“第一”“最早”“最大”的判断。

它最可靠的考古价值是：

> **同一个个人站点的内容、URL、hosting provider 和维护状态可以分别迁移。**

因此必须记录：

```text
site identity continuity
URL continuity
content continuity
operator continuity
hosting continuity
```

它们不是同一个布尔值。

---

# 5. 个人主页的完整状态链

最小状态链建议写成：

```text
person exists
→ hosting service exists
→ registration/application available
→ account created
→ homepage namespace assigned
→ author gains upload/edit capability
→ root page published
→ subpages/assets uploaded
→ homepage indexed/listed/discoverable
→ visitor obtains root HTML
→ dependent assets load
→ interactive widgets load
→ counter request executes
→ counter state mutates
→ guestbook/comment backend accepts write
→ author later reads feedback
→ author updates page
→ account remains valid
→ provider keeps service alive
→ namespace/redirect remains valid
→ archive captures some representation
→ modern replay reconstructs some subset
```

任何一个箭头都可能断。

---

# 6. 关键状态缺口

## 6.1 `person / account / homepage gap`

主页署名、昵称、邮箱不能自动变成现实身份确认。

即使昵称和今天公开身份相同，也要另证：

- 作者自述；
- 同时代个人介绍；
- 域名/组织关系；
- 其他独立来源。

隐私上尤其不能为了“确认是谁”去扩大普通个人的现实身份暴露。

---

## 6.2 `namespace assignment gap`

平台允许 `/~username/` 或 `username.example.com`，不代表：

- 用户永久拥有该路径；
- 路径不会回收；
- 账号删除后路径不会重新分配；
- 域名迁移后旧地址继续指向同一个人。

所以历史 URL 不是永久身份证。

---

## 6.3 `default shell / authored body gap`

托管主页经常包含：

- 平台统一 banner；
- 广告；
- 导航；
- 计数器模板；
- 自动页脚；
- “最后更新”组件。

必须分开：

```text
provider-rendered shell
user-authored body
```

否则容易把平台在 2001 年统一改版后插入的 UI 当成用户 1998 年亲手设计的页面。

---

## 6.4 `upload capability / current content gap`

发现 FTP 地址、上传帮助页，只证明编辑路径存在。

不能推出：

- 当前页面确实通过 FTP 上传；
- 所有用户都有同样权限；
- 账号在 capture 当天仍可写；
- 作者仍保存密码。

---

## 6.5 `root HTML / asset survival gap`

主页 root HTML 幸存时，常见丢失包括：

- GIF/JPEG；
- 背景图；
- MIDI；
- ZIP/EXE 下载；
- frame 子页面；
- JS；
- CSS；
- counter GIF；
- guestbook endpoint。

因此“页面可以打开”不能等价于“页面保存完整”。

必须分别记录主文档与子资源。

---

## 6.6 `counter display / audience gap`

一个历史页面显示：

```text
您是第 12345 位访客
```

不能自动解释成：

```text
12,345 个独立的人访问过
```

可能影响计数的包括：

- 同一人重复刷新；
- 是否按 IP/session 去重；
- 图片缓存；
- bot/crawler；
- 计数器重置；
- 站点迁移后重新计数；
- archive replay 是否错误触发或固定历史图像；
- 第三方计数服务是否仍在线。

因此建议字段：

```text
counter_visible_value
counter_backend_known
counter_semantics_known
counter_capture_datetime
counter_reset_evidence
```

本文称为：

**metric-survival / audience-history gap — 指标幸存 / 受众历史缺口。**

---

## 6.7 `guestbook shell / guestbook database gap`

留言本链接存在，不代表：

- backend 存在；
- 数据库被 archive；
- 所有历史留言都可读；
- 写入路径仍可执行；
- 现存留言没有被管理员/作者删除过。

动态留言本往往比静态主页正文更容易整体消失。

所以：

```text
link survives
≠ conversation survives
```

---

## 6.8 `directory inclusion / discoverability gap`

主页可以通过：

- 平台分类目录；
- “十佳主页”；
- 流量排行；
- 友情链接；
- 搜索引擎；
- 报刊推荐；
- 朋友口耳相传；

被发现。

但页面存在不等于当时容易被发现。

本仓必须和 `SEARCH_INDEX_RANKING...` 类研究接起来：

```text
published page
≠ indexed page
≠ highly ranked page
≠ encountered page
```

---

## 6.9 `last-updated label / actual edit-time gap`

个人主页常显示：

- Last Updated；
- 最后更新；
- 当前日期；
- 自动脚本时间。

2000 年杨震霆甚至在回顾某主页时怀疑“最新更新”可能是程序同步显示时间。

因此：

```text
visible date
```

必须先判断究竟是：

- 用户手写日期；
- 文件 mtime；
- 服务端脚本当前日期；
- 浏览器 JS 当前日期；
- archive rewrite 后日期。

否则非常容易把动态“今天”误成历史更新时间。

---

## 6.10 `current shell / historical body gap`

后来的平台、当前镜像或保存站点可能：

- 用新 header 包旧正文；
- 用当前 footer 包历史帖子；
- 重写 URL；
- 将旧内容导入新模板。

所以必须分别标记：

```text
content_time
render_shell_time
capture_time
current_access_time
```

不能给整页一个单一年份。

---

# 7. 从个人主页到 Blog/SNS：研究单位发生变化

## 7.1 2001“个人家园”：多个个人数据服务开始合流

2001 年新浪“个人家园”的同时代报道把：

- 收费邮箱；
- 个人主页；
- 电子相册；
- 名片/日程；

整合成一个个人服务包。

来源：

- 《汪延：个人家园是新浪的重要战略步骤》，2001-08-19：
  <https://tech.sina.com.cn/i/c/2001-08-19/81089.shtml>

证据等级：**B。**

这意味着旧网考古不能只追：

```text
homepage URL
```

还要开始追：

```text
account
→ profile
→ album
→ mailbox
→ calendar/contact state
```

页面逐渐成为账号的一个视图，而不再是用户自行组织的全部站点。

---

## 7.2 2008 校内网：个人页进一步成为关系图中的节点

2008 年《中国青年报》报道中的用户操作包括：

- 登录后进入“我的个人主页”；
- 看点击率；
- 看访客；
- 看留言、招呼、评论；
- 通过好友/好友的好友建立关系；
- 搜索旧同学；
- 写日志、分享内容。

来源：

- <https://www.chinanews.com.cn/edu/dxxy/news/2008/10-13/1409431.shtml>

证据等级：**B + 同期个人自述。**

此时研究单位必须扩展为：

```text
profile page
+ social graph
+ visibility metric
+ feed
+ message/comment system
```

而且：

```text
profile network label
≠ current real-world affiliation
```

这与 `AFFILIATION_CREDENTIAL_AND_ACCOUNT_LIFECYCLE_2001_2009.md` 已有结论直接衔接。

---

# 8. 从“站长”到“平台账号”：作者控制权的结构变化

建议平台谱系研究不要写成简单的“越来越先进”，而要比较：

| 维度 | 早期个人主页 | 托管博客 | SNS/个人空间 | 自媒体/内容平台 |
|---|---|---|---|---|
| URL 控制 | 常为 host 下路径 | 平台路径/子域 | 平台 profile ID | 平台 account/channel ID |
| 页面布局 | 用户可较多控制 | 模板化 | 高度平台化 | 高度平台化 |
| 发布技能 | HTML/FTP 可能重要 | Web editor | 表单/上传 | App/editor/视频工具 |
| 发现机制 | 目录/友情链接/搜索 | 标签/评论/搜索 | 社交图/feed | 推荐算法/搜索/feed |
| 反馈 | email/guestbook/counter | 评论/订阅 | 访客/评论/好友 | 点赞/收藏/粉丝/播放 |
| 数据所有权 | 文件可部分自持 | 平台数据库增多 | 平台数据库为主 | 平台数据库为主 |
| 服务死亡风险 | host 路径/资产丢失 | 博客关停/导出 | 账号/平台政策 | 账号、推荐、商业资格 |

关键不是“旧主页自由、新平台不自由”这种价值判断，而是明确：

> **用户从自己维护文件，逐渐转向维护平台里的状态。**

---

# 9. 平台死亡：公开不等于容易保存

## 9.1 个人主页是一种高度集中故障域

当大量用户依赖同一个免费主页 host：

```text
one provider shutdown
→ thousands/millions of personal public selves disappear together
```

这是一种纸质私人档案不一定具有的集中风险。

2000 年的近同时代个人主页回顾已经记录：

- 服务停止申请；
- 公司业务转移；
- 页面“连根砍掉”；
- 只剩零星内容；
- 原主页改域或不再更新。

证据等级仍应保守视为 **B/C**，但它足以证明“托管连续性”本身就是研究对象。

---

## 9.2 GeoCities 是海外对照，不是本仓主对象

FTC 1998 文件证明 GeoCities 当时已形成大量主题社区个人主页托管；Computer History Museum 后来的 `Deleted City` 项目则展示 GeoCities 关闭后大规模网页备份如何成为数字史材料。

来源：

- FTC 1998 complaint：<https://www.ftc.gov/sites/default/files/documents/cases/1998/08/geo-cmpl.htm>
- Computer History Museum：<https://computerhistory.org/exhibits/deleted-city/>

这一海外对照只用于确认一个共同问题：

**hosted-public-self mortality — 托管公开自我的平台死亡。**

中文旧网仍需自己的平台样本来测量这一机制。

---

# 10. Archive 选择偏差：最会公开自己的人，也最容易成为“历史上的普通人”

个人主页档案会制造严重的：

**public-self archive bias — 公开自我档案偏差。**

更容易进入 archive 的人包括：

- 会做网页的人；
- 愿意公开写作的人；
- 主页被目录/友情链接链接的人；
- 流量较高的人；
- 主页活得够久、刚好被 crawler 抓到的人。

更难看见：

- 只浏览不发布的人；
- 只用邮件/聊天的人；
- 没被外部链接的主页；
- 很快删除的页面；
- robots/login 后的空间；
- 普通家庭、低收入用户、非技术用户未数字化的生活；
- 用户主动撤回的私人内容。

因此：

> **Archive 里的“个人互联网史”不是网民的随机样本，而是被发布意愿、技术能力、链接结构、平台寿命和 crawler 行为多轮筛选后的样本。**

---

# 11. “访问历史黑区”：网页幸存，遭遇史消失

即使一个个人主页被完美保存，我们仍然通常不知道：

- 1998 年谁第一次从报纸地址输入它；
- 谁从友情链接点进来；
- 谁看了三十秒就走；
- 谁保存了书签；
- 谁因为主页写信给作者；
- 谁受它影响去学 HTML、换工作、买电脑；
- 哪些访问来自搜索引擎；
- 哪些只是 crawler。

因此定义：

**encounter-history darkness — 遭遇史黑区。**

主页正文保存越完整，研究者越容易误以为“历史场景也完整”。实际上最关键的人际后果往往根本不在 HTML 里。

---

# 12. 访问指标不只是技术字段，也会改变行为

2008 校内网同期材料已经显示：

- 用户主动查看主页点击率；
- 点击率上涨带来满足感；
- 有人为了增加点击而逐个访问别人主页；
- 留言、评论是否出现会改变用户的情绪和登录习惯。

这意味着 counter / page views 不只是要被“正确解析”的技术对象，它们本身已经参与塑造用户行为。

因此建议旧网案例同时记录：

```text
metric implementation evidence
metric displayed value
user interpretation evidence
behavioral consequence evidence
```

不能只保存一个 `counter=918`。

---

# 13. 2015 以后不扩 scope，但要说明边界

本仓主研究止在约 2015 年，因此：

- 2019 自媒体职业化；
- 2022 校园博主；
- 2025 “电子搬家”；

不作为本仓继续扩展的平台史对象。

它们只在 `how-people-lived` 中承担长期生活史比较。

本仓要回答的是它们的旧网前提：

> **个人 URL、主页、博客、个人空间、访问指标、评论、好友网络和托管平台，怎样在 1996—2015 之间逐步建立了“公开自我可被平台化管理”的技术条件。**

---

# 14. 一个个人主页案例应怎样编目

建议未来 M1 个人主页完整案例至少记录：

```yaml
object_type: personal_homepage
operator_identity:
  status: confirmed|probable|unknown|minimized_for_privacy
hosting_provider:
homepage_root_url:
namespace_pattern:
active_period:
captures:
  - archive_source:
    capture_url:
    original_url:
    capture_datetime:
    http_or_replay_state:
    charset:
    main_document_saved:
    subresources_sampled:
browser_assumptions:
  ie:
  netscape:
  frameset:
  javascript:
  java_activex_flash:
features:
  counter:
  guestbook:
  downloads:
  music:
  forms:
  chat:
  outbound_links:
state_unknowns:
privacy_notes:
copyright_notes:
```

尤其不要遗漏：

- 原 URL；
- capture datetime；
- 当前访问时间；
- 主页正文与平台 shell 的时代是否相同；
- counter 是否静态图/动态服务；
- guestbook 是否实际恢复；
- 资源缺失清单；
- 是否出现现实联系方式。

---

# 15. 浏览器/编码条件

1996—2005 个人主页尤其容易遇到：

- GB2312 / GBK / Big5；
- `<frameset>`；
- table layout；
- `document.all`；
- 浏览器嗅探；
- Java Applet；
- ActiveX；
- Flash；
- MIDI/BGSOUND；
- 第三方计数器图片；
- 站外图片 hotlink；
- 固定 640×480 / 800×600 设计；
- 字体缺失。

所以现代 Chromium “能打开”只说明现代环境得到一种结果。

完整案例必须至少记录：

```text
historical browser assumption
modern replay result
known missing behavior
```

---

# 16. 隐私边界

个人主页比门户首页更容易含有：

- 姓名；
- 生日；
- 学校/单位；
- 邮箱；
- 电话；
- 家庭地址；
- 照片；
- 朋友姓名；
- 情感/健康/家庭叙述。

因此遵守 `docs/METHOD.md`：

1. 研究平台结构时，优先抽象 URL pattern，不批量重新公开普通用户 ID；
2. 不因为历史页面公开过，就批量再发布今天已经难以发现的个人敏感内容；
3. 不通过今天仍有效的电话/邮箱去“确认历史作者”；
4. 普通个人页截图只保留支持 claim 所需最小范围；
5. 涉及未成年人页面尤其提高门槛；
6. 页面已主动删除而只在 archive 存在时，避免把删除本身当作“邀请重新公开”。

---

# 17. 版权边界

个人主页中的：

- 照片；
- 绘图；
- 音乐；
- 软件；
- 长篇文章；

版权通常不能因为 archive 可访问就重新分发。

优先保存：

- URL；
- capture metadata；
- 文件类型/尺寸/hash（合法取得时）；
- 结构描述；
- 自己的测量；
- 必要的极短摘录。

不要为了“还原氛围”把整站原资源重新打包进仓库。

---

# 18. 本轮负结果：仍没有一份达到 M1 门槛的 verified 1996—2000 中文个人主页 capture

本轮能够定位：

- 1999 同时代/近同时代平台描述；
- CNNIC 1999 使用调查；
- 2000 个人站长近同时代回顾；
- 一条后来文章提供的 1999 `163.com` Wayback locator。

但本轮**没有成功实际打开并检查一份足以作为完整个人主页案例基础的 1996—2000 中文个人主页 Wayback/WARC memento**。

按照 `docs/METHOD.md`：

> 搜索结果出现 Wayback 链接，不等于 capture 已验证。

因此以下内容全部继续保持 unknown：

- 某个具体 1998 网易个人主页的原始 DOM；
- charset header；
- 当时的完整 URL namespace 规则；
- FTP/管理入口的具体页面；
- 计数器 CGI endpoint；
- 留言本 backend；
- cookie/session；
- frameset/subresource 完整性；
- IE/Netscape 的真实差异。

这不是失败；它是明确的 archive gap。

---

# 19. 下一步：把 M1 的“个人主页案例”从抽象模型推进为可复核案例

优先对象可以从现有证据丰富的 1997—2000 中文个人主页生态中选择，但必须先满足：

1. 至少两个历史时点的实际 capture；
2. 原 URL 可确认；
3. 主 HTML 与若干子资源能实际检查；
4. 至少一个独立同时代来源；
5. 现实个人隐私风险可控；
6. 能列清“已证实 / 高概率 / 不知道”。

最值得恢复的不是“漂亮截图”，而是：

```text
URL namespace
charset
HTML/frame structure
asset graph
counter behavior
留言本是否动态
outbound link graph
last-update semantics
host migration
capture gap
```

---

# 20. 核心结论

中文个人主页考古最危险的错觉是：

> **页面看起来越像一个人的“家”，研究者越容易把页面、账号、作者、访问者和真实人生混成同一个对象。**

真正可靠的模型应该始终保持：

```text
公开页面是某人某时点的展示层
≠ 完整的人

counter 是某个系统显示的状态
≠ 独立读者人数

guestbook link 是一个交互入口
≠ 留言历史完整幸存

homepage root survives
≠ asset/backend survives

URL remains resolvable
≠ original operator remains

archive capture survives
≠ historical audience encounter survives
```

这也解释了个人主页为什么是 `how-people-lived` 与 `old-web-archaeology` 特别好的交叉对象：

> 它一方面让普通人第一次大规模拥有“自己可以编辑的公共地址”；另一方面又用托管、URL、计数器、后台、平台寿命和 archive 选择，把谁能成为后人眼中的“普通网民”重新筛选了一遍。
