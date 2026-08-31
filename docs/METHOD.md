# METHOD.md — 中文旧网考古证据与复原方法

本文件定义本仓的最低证据合同。目标不是让所有案例写成同一种叙事，而是让不同研究者/Agent 对同一历史对象留下可比较、可复核、可否证的记录。

## 1. 研究单位

每个结论必须先指定研究单位，不把“站点”“平台”“页面”“账号”“域名”“一次 capture”混成一个对象。

常用层级：

- **platform**：例如某博客/SNS 产品；
- **site / host**：例如 `hi.baidu.com`；
- **account / homepage**：平台内一个用户空间；
- **page / URL**：具体文章、栏目、帮助页；
- **capture / artifact**：某档案服务在某时刻保存的一份表示；
- **claim**：研究者依据若干 evidence 作出的最小可检验陈述。

同一个 host 的不同年月不能默认视为同一页面形态；同一个品牌名也不能默认对应同一个技术系统。

## 2. A/B/C/D 证据等级

### A — 原始 / 同时代证据

满足以下一类即可进入 A，但仍须记录 provenance：

- 可定位的历史网页快照、WARC/WACZ、原始 HTML/CSS/JS；
- 当时发布的官方公告、产品页、帮助页、开发文档、软件手册；
- 当时产生的 DNS/WHOIS/证书/软件包/安装介质等技术记录；
- 同时代截图或抓包，且来源、日期与对象可核验。

A 不等于“绝对真实”。平台自己的新闻稿可以证明“平台当时这样宣称”，不能自动证明用户规模、效果或因果解释。

### B — 近同时代二手证据

包括同期或接近事件发生时间的新闻报道、教程、媒体评测、论坛技术讨论、站长文章、用户操作说明等。

B 可以补足 URL 形态、功能存在、用户操作路径等，但若只是转抄同一公告，不算真正独立来源。

### C — 后来回忆

包括多年后的采访、怀旧文章、个人回忆、二次整理。

C 适合研究记忆与经验，不应单独用于确定精确日期、页面结构、浏览器要求或资源是否真实存在。

### D — 研究者复原 / 推断

包括根据残存资源补出页面结构、推断域名迁移关系、根据截图猜测 CSS/脚本行为、用模拟环境重建浏览体验等。

任何 D 级内容必须显式写明：

1. 推断依据；
2. 推断步骤；
3. 缺失证据；
4. 可替代解释；
5. 哪些部分由现代工具或人工补全。

D 不得伪装成 historical original。

## 3. “独立来源”判定

两个 URL 不必然是两个独立来源。若两篇新闻逐字转抄同一稿件，只计一个 evidence family。

优先组合：

- 平台官方页面 + 同期独立媒体；
- Wayback capture + Common Crawl/WARC；
- 官方帮助页 + 同期用户教程；
- 同时代页面 + 后来的回忆（用于比较，而不是互相“投票”）。

每条关键 claim 尽量至少有两个 evidence family；只有一个来源时必须降低措辞强度。

## 4. Archive capture 的最低记录

档案证据必须区分 Original Resource 与 Memento。RFC 7089 对 Original Resource、Memento 及 Memento-Datetime 的区分可作为本仓字段设计的基础：

<https://www.rfc-editor.org/rfc/rfc7089.html>

每个 capture 最少记录：

- `archive_source`；
- `capture_url`；
- `original_url`；
- `capture_datetime`（若档案明确给出）；
- `accessed_at`；
- HTTP/回放状态（若可观察）；
- 页面是否为重定向、错误页、登录页或 robots 占位；
- 主文档与子资源是否分别保存；
- 字符集/Content-Type（能可靠取得时）；
- evidence grade 与 confidence。

**搜索结果里出现一个 Wayback 链接，不等于已经验证该 capture。** 未实际打开并检查的 locator 只能登记为“candidate capture”。

## 5. Claim 的最小化写法

优先写可以被证据直接支持的窄结论：

- 好：`2006-07-13 百度官方新闻稿宣布百度空间正式发布。`
- 差：`2006 年百度空间成为中国年轻人的网络家园。`

必须区分：

- **exists**：某功能/页面被证据证明存在；
- **available**：普通用户当时能否获得；
- **used**：是否有使用证据；
- **popular**：是否有可靠规模数据；
- **caused**：是否有因果证据。

不能从 exists 直接跳到 popular，更不能从时间先后直接跳到 caused。

## 6. 页面与浏览器环境

现代浏览器成功回放只证明“现代环境可以得到某种呈现”，不证明当年用户看到同样结果。

涉及以下内容时必须记录 browser assumption：

- IE-only / ActiveX；
- Java Applet；
- Flash；
- document.all / 浏览器嗅探；
- GB2312 / GBK / Big5 / UTF-8；
- frameset / table layout；
- 字体、viewport、屏幕尺寸；
- 被 archive rewrite 改写的 URL/JS。

没有旧浏览器验证时，不得把现代回放截图写成“历史浏览体验”。

## 7. Reconstruction 标识

任何复原页面、重建截图、手工补链、模拟器输出都必须在文件与展示层同时带 `reconstruction` 标识。

复原说明至少列：

- historical originals；
- missing artifacts；
- substituted artifacts；
- modern tooling；
- assumptions；
- unresolved differences。

不得使用生成式内容填补历史缺失资源后冒充原件。

## 8. 负证据与缺失

`没有找到` 不能写成 `当时不存在`。

应记录搜索范围，例如：

- 查询了哪些 archive；
- 检查了哪些年份/URL 变体；
- 是否可能受 robots、登录、动态 URL、JS、域名复用影响；
- 是否只缺子资源而主 HTML 存在。

“无法可靠复原”是允许且有价值的结论。

## 9. 隐私与版权

### 隐私

- 对普通个人主页、论坛账号、联系方式实行研究必要最小化；
- 不批量重新公开已经删除的个人敏感内容；
- 研究平台结构时优先抽象 URL pattern，而不是复制普通用户 ID；
- 必须引用个人页面时，只保留支持 claim 所需的最少信息。

### 版权

archive 可访问不等于仓库可重新分发。

版权/许可不明时优先提交：

- URL；
- capture metadata；
- 摘要与分析；
- 自己生成的测量结果；

而不是原始图片、音乐、Flash、整页镜像或大段文本。

## 10. 每次研究循环

1. 读当前仓库与最近提交；
2. 选一个足够具体的缺口；
3. 建 claim list，再找证据，不先写故事；
4. 至少寻找两个 evidence family；
5. 标 A/B/C/D 与 confidence；
6. 明确 archive gap、浏览器/编码条件；
7. 写“已证实 / 高概率 / 不知道”；
8. 做隐私/版权检查；
9. 只有证据达到门槛时进入完整 case；否则保留 research note；
10. checkpoint 后再扩展。

## 11. Stop conditions

出现以下情况时停止把结论写得更确定：

- 只剩后来回忆，无法找到同时代证据；
- archive locator 无法实际检查；
- 来源之间明显互相转抄；
- 域名已复用且无法确认历史主体；
- 浏览器/插件条件足以改变解释但尚未验证；
- 涉及不应重新公开的个人内容；
- 版权状态不足以支持复制原资源；
- reconstruction 与 original 无法可靠区分。

此时应保存负结果、缺失项与下一步，而不是补全叙事。
