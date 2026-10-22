# 水木清华 BBS：2005 年校内访问边界与“站点仍在但公网消失”

> 状态：bounded research note；**不是 M1 完整案例**。
>
> 研究对象：BBS 水木清华站（`smth.edu.cn`），重点限定在 2005-03-16 前后从开放型 BBS 转为校内型后的可达性变化。

## 为什么研究这个对象

仓库已经覆盖 DNS 失效、托管关闭、平台迁移、围墙网个人主页、搜索快照等多种“消失”。但仍缺一个反方向的、证据较强的案例：**同一个服务和内容库可能继续运行，而访问资格在网络边界上收缩，使公网用户突然失去访问能力。**

这对 M1 的 BBS/社区案例、M2 平台谱系和 M4 缺失地图都有直接价值。

核心区分：

```text
site/service exists
!= globally routable/reachable
!= reachable from a given network origin
!= account may authenticate
!= user may register
!= user may read/post
!= public archive crawler can capture
```

## 证据等级说明

沿用仓库 A/B/C/D：

- **A**：原始/同时代 artifact 或原始文本；
- **B**：近同时代独立报道；
- **C**：后来参与者/机构回忆；
- **D**：研究者复原或推断。

本笔记中，2005-03-16 站务公开信目前来自 2005-03-22 的同时代转贴，并非直接从 `smth.edu.cn` 原始 capture 取得，因此记为 **A-（derivative primary text）**，不能冒充已验证的原始页面 artifact。

## 时间线

### 2005-03-16：由开放型转为校内型

**证据：A- / B**

2005-03-22 的个人博客保存了《BBS 水木清华站站务委员会致全站用户的一封公开信》的同时代转贴，署名日期为 2005-03-16。该转贴同时保存了《京华时报》2005-03-19 第 04 版报道。

报道记录：

- 3 月 16 日，水木清华站由开放型转为校内型；
- 页面显示“限制校外 IP 访问”；
- 当日下午 3:40，站务委员会发布公开信；
- 校外用户将不能访问；
- 次日下午记者仍观察到新 ID 注册受限。

来源：

- Rooster, `水木BBS调整为校内型`, 2005-03-22，保存站务公开信与《京华时报》2005-03-19 报道：
  https://steature.wordpress.com/2005/03/22/%E6%B0%B4%E6%9C%A8bbs%E8%B0%83%E6%95%B4%E4%B8%BA%E6%A0%A1%E5%86%85%E5%9E%8B/
- CyberJos, `水木清華之死`, 2005-03-21；独立的近同时代观察，记录校内 IP 边界与校外用户失去服务：
  https://cyberjos.blog/press/internet/%E6%B0%B4%E6%9C%A8%E6%B8%85%E8%8F%AF%E4%B9%8B%E6%AD%BB/

### 可直接证明什么

目前可以较有把握地说：

1. 2005-03-16 前后，水木清华的访问政策从开放型收缩为校内型；
2. 限制是按校内/校外网络来源实施，而不只是把首页换成关站公告；
3. 校外用户因此失去正常访问能力；
4. 服务本身并未在 3 月 16 日简单“关站”。

### 不能直接证明什么

当前材料**不能**证明：

- 所有校外 ASN/IP 在同一秒被统一丢弃；
- 限制具体发生在路由、ACL、防火墙、反向代理还是应用层；
- Telnet 与 WWW 两条入口采用完全相同的过滤机制；
- DNS 在校外停止解析；
- origin server 停机；
- 数据库或历史文章被删除；
- Wayback 没有 capture 就是因为该限制；
- 任何具体用户的数据在此时丢失。

“物理上屏蔽路由”等更具体的机制说法主要见于后来整理材料；在取得网络配置、traceroute、原始技术公告或同时代多点测量前，不升级为 A/B 事实。

## 新的 preservation 模型：observer-relative reachability

旧网“可达”必须带观察点：

```text
artifact exists at origin
  -> DNS answer from observer
  -> network route from observer
  -> transport connection
  -> protocol service (WWW/Telnet)
  -> application authorization
  -> account capability
  -> content capability (read/post/register)
```

因此更准确的字段不是简单 `reachable: true/false`，而应类似：

```yaml
observation:
  datetime: 2005-03-16Txx:xx:xx+08:00
  observer_network: outside_tsinghua   # if independently known
  service: www|telnet
  dns: unknown
  route: unknown
  transport: unknown
  application_response: access_restricted
  registration: restricted
  evidence_grade: B
```

**同一时刻，从清华校内和校外观察，站点可能具有不同的“存在状态”。**

这与此前视聆通案例互补：视聆通强调一个服务从一开始就可能位于区域/围墙网络；水木清华则证明一个原本公网可访问的社区可以在不删除内容库的情况下把可达域收缩回机构网络。

## BBS 形态的额外价值

水木清华还提醒我们：历史 BBS 不应只按“网页”保存。

至少要分别检查：

- WWW 入口；
- Telnet 入口；
- guest/read capability；
- 注册；
- 登录；
- 发帖；
- 站内信/好友等登录后对象；
- 精华区/版面内容；
- 校内与校外网络来源。

所以：

```text
WWW unavailable != BBS wholly unavailable
Telnet unavailable != WWW unavailable
guest readable != account usable
account exists != user can reach login endpoint
content still on disk != former user can retrieve it
```

## 与“站点死亡”的区别

建议后续研究统一使用如下状态词，而不要全部写成“关闭”：

- `service_shutdown`：服务实际停止；
- `network_scope_restricted`：网络来源范围收缩；
- `registration_closed`：停止注册；
- `read_only`：只读；
- `account_auth_unavailable`：已有账号无法登录；
- `locator_dead`：URL/host 不再工作；
- `content_deleted`：内容对象被删除；
- `archive_observer_excluded`：档案爬虫所在网络无法进入。

本案当前最强结论属于 `network_scope_restricted`，不能替换成 `service_shutdown` 或 `content_deleted`。

## 与后人回忆/整理材料的比较

后来的百科式整理通常把 2005-03-16 概括成“封禁校外 IP”“物理上对校外路由屏蔽”，并进一步叙述随后新水木的建立、数据备份和用户迁移。

这些材料对寻找线索有用，但本轮不把其中的具体网络机制、用户数据复制过程或比例数字直接提升为事实。相比之下，2005-03-19《京华时报》报道能够直接支持的范围更窄但更可靠：**页面明确宣布限制校外 IP，记者观察到访问/注册状态变化。**

这正好满足 M1 所要求的“后人回忆与同时代证据比较”：后来叙事往往把一个复杂的权限/网络变化压缩成“封站”或“316 事件”，而同期证据允许把状态拆得更细。

## 建议写入位置

当前先保留本文件：

- `research/smth-access-boundary-2005.md`

取得 artifact 后可进一步进入：

- 一个正式的 BBS/community M1 case；
- `studies/platform-genealogy.md`：开放校园 BBS -> 校内交流平台 / 公网社区分叉；
- future `datasets/sites.csv`：加入 observer/network-scope 字段；
- future archive-gap model：区分 crawler exclusion 与 content absence。

## 下一步 artifact probe

优先级：

1. 找到 2005-03-15/16/17/18 的 `smth.edu.cn` WWW capture；
2. 找到 3 月 16 日站务公开信原始 locator/capture；
3. 找到 WWW 进站画面中“限制校外 IP”原始 capture；
4. 找到 Telnet 进站画面 artifact（截图需保留 provenance）；
5. 分别记录 WWW/Telnet 的 hostname、port、response；
6. 若有合法的历史网络测量，只记录校内/校外观察点，不尝试绕过历史或现有访问控制；
7. 检查 3 月 16 日前后公共 archive 的 capture discontinuity，但**不能从 capture gap 单独推导过滤机制**。

## 可复原程度

| 层 | 当前状态 |
|---|---|
| 平台身份 | 高 |
| 2005-03-16 政策变化 | 高 |
| 校外访问受限 | 高 |
| WWW 具体 HTML | 低，待原始 capture |
| Telnet 具体进站画面 | 低，待原始 artifact |
| DNS 行为 | 未知 |
| 网络过滤实现 | 未知 |
| charset | 未知 |
| 浏览器依赖 | 未知 |
| BBS server software/version | 未知 |
| 内容库连续性 | 中低；“服务未整体关停”不等于逐对象连续性 |
| 公共 archive 可抓取性 | 未知，需逐时点验证 |

## 不能声称已经证明的内容

- “2005-03-16 水木清华关站”；
- “2005-03-16 所有数据被删除”；
- “校外访问限制一定由路由器 ACL 实现”；
- “Wayback 的缺口一定由校内化导致”；
- “新水木是旧水木的完整字节级镜像”；
- “所有旧账号、私信、好友关系均被迁移”；
- “后来水木社区与原站在法律、组织或数据意义上完全连续”。

## 隐私与版权边界

这是社区数据案例，风险高于普通企业首页。

- 不为证明迁移完整性而抓取或公开普通用户私信、好友关系、邮箱、真实姓名等个人数据；
- 不把已删除普通用户帖子重新批量发布；
- 优先使用站务公告、公开进站画面、媒体报道、帮助页和非敏感公共版面；
- 历史截图只保存研究所需的最小片段和 provenance；
- 如需比较文章 continuity，优先选择站务公告或明确允许公开传播的制度性文本；
- 不绕过现有访问控制，不利用遗留账号进入非公开内容；
- 版权不明的历史资源只记录 URL、hash、metadata 和 archive locator，不默认重新分发。

## 本轮结论

本案的新贡献不是再次叙述“316 事件”，而是把它转成可复核的旧网保存问题：

> **一个站点可以继续存在、服务器可以继续工作、内容也可能仍在，但因为访问网络域收缩，它会从某些用户和公共档案爬虫的观察世界里突然消失。**

因此旧网考古中的“存在/消失”必须记录 observer 与 network scope；否则很容易把 `network_scope_restricted` 错写成 `service_shutdown` 或 `content_deleted`。
