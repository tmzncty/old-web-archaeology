# 校内网 → 人人网：域名迁移证据（2005—2011）

> 状态：bounded research note；不是 M1 complete case。

本轮聚焦 `xiaonei.com` 到 `renren.com` 的品牌与域名迁移，不写“人人网兴衰史”。2011 年 Renren Inc. 向 SEC 提交的 F-1 记录：公司 SNS 前身为 `www.xiaonei.com`，并在 2009 年 8 月更名为 `www.renren.com`；同一文件的知识产权部分同时列出 `renren.com` 与 `xiaonei.com` 为公司注册域名。由此至少可以确认：品牌更名不等于旧域名立即从资产层消失。

2009-08-04 新浪科技报道，千橡宣布校内网更名人人网并启用 `renren.com`，同时称原 `xiaonei.com` 将继续作为跳转网址。2009-08-24《互联网周刊》又把“域名相应更换”具体写在 8 月 14 日凌晨。因此更稳妥的写法是把“更名公告”和“canonical domain cutover”分开，而不是压成一个瞬间。没有直接 HTTP/DNS capture 前，跳转状态码、path/query 是否保留仍然未知。

2007 年同期报道还显示，校内网扩展到高中和白领市场时采用过分区身份规则：例如公司用户需使用相应邮箱后缀注册，而且不同新区不能跨区登录。这说明“实名 SNS”与“所有用户都经过法律身份核验”不是一回事，平台账号存在也不等于拥有所有分区的访问资格。

## 证据等级

- A：Renren Inc. Form F-1（2011-04-15），用于 2011 公司资产状态及正式公司披露。
- B：2006—2009 同期媒体，用于收购、分区规则、更名与域名切换过程。
- C：后来把 2009 更名解释为“衰落转折点”的文章，只作为后见叙事，不作因果证据。
- D：本文提出的 brand / domain / redirect / account / content 分层模型。

## 不能声称已经证明

- 2009-08-04 当天两个域名的实际 DNS/HTTP 状态；
- 旧域名使用何种重定向；
- 深层 URL 是否逐一保留；
- 历史页面 charset、DOM、JS 与浏览器依赖；
- “无缝迁移”是否对所有内容对象成立。

## 下一步

直接核验 2009-08-01..20 的 `xiaonei.com`、`www.xiaonei.com`、`renren.com`、`www.renren.com` capture，记录时间、HTTP/replay 状态、Location、charset 与子资源。优先使用登录/帮助/about 等公开页面，避免普通个人资料页。

## Sources

- SEC F-1: https://www.sec.gov/Archives/edgar/data/1509223/000119312511099693/df1.htm
- 2009-08-04: https://tech.sina.com.cn/i/2009-08-04/14523321884.shtml
- 2009-08-24: https://tech.sina.com.cn/i/2009-08-24/15153378768.shtml
- 2007-11-21: https://tech.sina.com.cn/i/2007-11-21/08491864406.shtml


## 2006 收购：公告、交易完成、技术整合要分开

2006-10-24 的同期报道记录千橡宣布收购校内网并计划整合 5Q 与校内网资产：

- ZDNet China via Sina: https://tech.sina.com.cn/i/2006-10-24/14131200494.shtml

2006-10-26 第一财经日报采访又记录，校内网的网站数据库与用户会在未来数月逐步融合：

- https://tech.sina.com.cn/i/2006-10-26/01471203884.shtml

2011 年 F-1 的审计财务附注则把 completed acquisition 放在 **2006 年 11 月**，并明确写出收购对象包含 domain name、operating platform、login-user list。

因此安全模型是：

```text
deal announced
  → transaction completion
  → platform integration
  → user/data integration
```

2006-10 与 2006-11 不必被处理成“哪个日期是真的”的冲突；它们可以是交易的不同阶段。

这条审计记录还有一个直接的方法价值：旧网平台不是一个不可分割的“网站”。至少在交易记录里，域名、运行平台与用户登录资产可以分别描述。反过来，login-user list 也不能自动等同于完整个人内容、全部关系边或完整数据库镜像。

## 更细的证据 ledger

| ID | 时间 | 等级 | 证据与可支持范围 |
|---|---|---|---|
| P1 | 2011-04-15 | A / A- | Renren F-1：正式公司披露；可支持 2011 资产状态，并提供对 2005/2009 的公司回溯时间线 |
| P2 | 2011-04-15 | A | 审计附注：2006-11 收购对象明确包含 domain、operating platform、login-user list |
| P3 | 2011-04-15 | A | Intellectual Property：`renren.com` 与 `xiaonei.com` 同时仍是注册域名 |
| B1 | 2006-10-24 | B+ | 同期收购公告与整合意图 |
| B2 | 2006-10-26 | B+ | 同期采访显示数据库/用户整合是后续过程 |
| B3 | 2007-11 | B+ | 高中/白领扩张、组织邮箱资格、分区隔离 |
| B4 | 2009-08-04 | B+ | 更名、启用新域名、旧域名继续跳转、资料迁移的运营方口径 |
| B5 | 2009-08-05 | B+ | 财新独立报道 audience repositioning |
| B6 | 2009-08-24 | B+ | 同期行业报道把域名相应更换放在 8 月 14 日凌晨 |
| C1 | 2018 | C | 后来把更名解释为衰落转折点；只能研究后见叙事 |
| D1 | 2026 | D | brand/domain/redirect/account/content/segment 分层模型 |

关键的独立来源组合是：

- SEC 审计/公司披露；
- 2006 同期商业与科技媒体；
- 2007 分区产品报道；
- 2009 发布会报道与独立行业分析。

同一发布会的多篇转述不能机械计算成多份独立技术证据。

## 2009 的“更名”至少包含四个可能错开的状态

目前最稳妥的拆法是：

```text
brand announcement
  ↓
new domain made available
  ↓
canonical/default host cutover
  ↓
legacy-domain redirect period
```

2009-08-04 新浪科技足以证明更名与新域名启用被公开宣布，也足以证明运营方当时声明旧域名会继续作为跳转入口。

2009-08-24《互联网周刊》把“域名相应更换”放在 8 月 14 日凌晨。没有 HTTP/DNS artifact 前，本仓不把这两个日期压成一个时间点，也不推断 8 月 4 日至 14 日之间的具体 redirect / canonical 策略。

这个边界对其他旧网平台也可复用：

```text
rename date
  != DNS cutover date
  != HTTP redirect date
  != deep-link migration completion date
```

## “无缝转移”必须保持为 operator claim

2009-08-04 的同期报道记录运营方称用户资料会“无缝转移”。这条是重要的同时代证据，但它证明的是**平台当时这样承诺/描述迁移**，不是独立迁移审计。

在没有前后 artifact、导出文件或独立用户对照之前，不能把“无缝”自动扩展为：

- 所有历史内容都保留；
- 所有关系都保留；
- 所有隐私设置都保留；
- 所有深层 URL 都有等价 redirect；
- 所有时间戳与评论层级都保持原样。

这也是本案对 M2 “内容所有权与 URL 所有权变化”最直接的贡献之一：内容连续性与 URL 连续性应分别验证。

## 2011：域名资产与用户可见状态仍不能混写

F-1 在 2011 年仍同时列出 `xiaonei.com` 和 `renren.com`。这足以证明旧域名没有随着“校内网”品牌退场而立即从公司域名资产层消失。

但必须继续保留：

```text
domain owned
  != DNS resolves
  != HTTP responds
  != redirects
  != redirects preserve path/query
  != old and new deep links are content-equivalent
```

因此后续 archive 工作应给域名迁移至少记录：

- owner/asset evidence；
- DNS/host evidence；
- HTTP response；
- redirect target；
- path/query preservation；
- content equivalence。

## 已证实 / 高概率 / 不知道

### 已证实

1. 2011 SEC 文件把 SNS 前身记为 `www.xiaonei.com`，并把 2009-08 作为更名为 `www.renren.com` 的月份。
2. 2006-10 千橡公开宣布收购校内网。
3. 审计附注把 2006-11 completed acquisition 的资产明确拆成 domain、operating platform、login-user list。
4. 2006 同期报道表明数据库/用户整合是未来数月的过程。
5. 2007 高中/白领扩张时存在组织邮箱资格和分区隔离。
6. 2009-08-04 公开宣布更名与新域名启用。
7. 当时运营方公开称 `xiaonei.com` 将继续作为跳转网址，并称资料“无缝转移”。
8. 2009-08-24 同期报道把域名“相应更换”放在 8 月 14 日凌晨。
9. 2011 `xiaonei.com` 与 `renren.com` 同时仍被列为公司注册域名资产。

### 高概率但未核验

1. 2009 更名期间两个域名存在一段并行窗口。
2. `xiaonei.com` 在更名后承担过 legacy redirect。
3. 首页级迁移可能比 deep-link continuity 更完整。
4. 2007 的分区身份模型在 2009 泛化后经历过调整。

### 不知道

1. 2005 原始 launch page 与精确公开上线日。
2. 2005—2009 页面 charset、DOM、JS 和浏览器依赖。
3. 2006 收购记录中的 login-user list 到底包含哪些字段。
4. 5Q 与校内网的技术整合方式。
5. 2007 各分区实际 URL/host。
6. 2009-08-04 两域实际 DNS/HTTP 状态。
7. 2009-08-14 canonical cutover 的具体动作。
8. legacy redirect 的 status 与 path/query preservation。
9. “无缝迁移”对不同内容对象的逐项真实性。

## 隐私与版权边界

本案不需要批量恢复普通用户资料即可完成平台结构研究。后续优先使用登录页、帮助页、about/product page 等公共结构页面；不以个人页面、私人照片、好友关系或已删除留言作为批量样本。

版权不明的历史资源只保留 URL、capture metadata、摘要与测量结果，不把整页、图片或平台素材镜像进仓库。

## 补充来源

- 2006-10-24 收购公告：https://tech.sina.com.cn/i/2006-10-24/14131200494.shtml
- 2006-10-26 第一财经采访：https://tech.sina.com.cn/i/2006-10-26/01471203884.shtml
- 2007-11-27 高中/白领扩张：https://tech.sina.com.cn/roll/2007-11-27/2344501202.shtml
- 中国互联网协会 2009-08-04：https://www.isc.org.cn/article/10515.html
- 财新 2009-08-05：https://companies.caixin.com/m/2009-08-05/100052893.html
- 后来回顾，仅作 C 级：https://finance.sina.com.cn/stock/jhzx/2018-11-14/doc-ihmutuec0220882.shtml
