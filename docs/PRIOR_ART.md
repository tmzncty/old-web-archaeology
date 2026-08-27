# Prior Art / 已有工作地图

本文件的目的不是列“友情链接”，而是明确哪些基础能力已经有人做得很好，本项目应该复用什么、避免重复什么，以及真正还有空间的地方在哪里。

## 1. Internet Archive / Wayback Machine

- 入口：<https://web.archive.org/>
- 已解决：超大规模网页存档、按 URL + 时间访问历史快照。
- 本项目复用：把 Wayback capture 当作最重要的外部证据源之一。
- 不重复：不自建全球级 Wayback。
- 仍需自己做：中文站点身份确认、页面谱系、同站不同域名/镜像关系、档案缺口解释、浏览器环境复原。

## 2. Webrecorder / pywb

- pywb：<https://github.com/webrecorder/pywb>
- ReplayWeb.page：<https://github.com/webrecorder/replayweb.page>
- Browsertrix Crawler：<https://github.com/webrecorder/browsertrix-crawler>
- ArchiveWeb.page：<https://archiveweb.page/>

### 已解决

- WARC/WACZ 记录与回放；
- 高保真浏览器抓取；
- 浏览器端 archive replay；
- Wayback 风格索引和时间导航；
- 现代动态页面的归档基础设施。

### 本项目决策

若需要本地回放 WARC/WACZ，优先接入这些工具，而不是自己写 URL rewriting / service worker / archive proxy。

我们的价值应在 **case study + evidence model + historical reconstruction**。

## 3. oldweb.today

- 项目：<https://github.com/oldweb-today/oldweb-today>
- 站点：<https://oldweb.today/>

它把旧浏览器模拟器与 Web Archive 连接起来，可在 Netscape、旧 IE 等环境中访问历史网页。

### 启示

“网页快照”与“当年的浏览体验”不是一回事。浏览器、OS、插件、字体、编码、屏幕尺寸都是历史环境的一部分。

### 不重复

不自己维护一套完整旧浏览器模拟器矩阵。需要时直接用 oldweb.today、86Box、PCem、QEMU 等作为复原环境。

## 4. ArchiveTeam

- 项目总览：<https://wiki.archiveteam.org/index.php/Projects>
- Warrior：<https://wiki.archiveteam.org/index.php/ArchiveTeam_Warrior>

ArchiveTeam 长期处理即将关闭、已经关闭或濒危的网站/平台，已经积累大量抢救项目与分布式抓取经验。

### 本项目应该借鉴

- “先抢救再整理”的濒危站点意识；
- 对“完整保存 / 部分保存 / 失败 / 无法公开”做明确状态区分；
- 不把抓下来等同于研究完成。

### 可合作/查重方向

做具体中文平台前，先查 ArchiveTeam 是否已经有对应 project、tracker、WARC 或 Internet Archive collection。

## 5. Common Crawl

- <https://commoncrawl.org/>

Common Crawl 提供长期大规模 WARC/WAT/WET 数据及索引。

### 用途

它更适合：

- 验证某域名/URL 在某时期是否仍被抓到；
- 大规模链接结构和站点生态研究；
- 补充 Wayback 单 URL 浏览模式。

### 限制

Common Crawl 不是专门的历史高保真展示系统；命中也不意味着页面视觉/脚本完整。

## 6. Memento / RFC 7089

- RFC 7089：<https://www.rfc-editor.org/rfc/rfc7089.html>

Memento 通过 datetime negotiation 把“某资源在某个时间的版本”标准化。

### 对本项目的意义

`original URL`、`capture URL`、`observed datetime` 应作为不同字段，不要只保存一条后来会失效的链接。

## 7. Web Design Museum

- <https://www.webdesignmuseum.org/>

它已经系统展示 1990s–2000s 大量网站、软件和视觉设计案例。

### 不重复

不做“全球著名网站截图博物馆”。

### 本项目的差异

重点放在：

- 中文互联网；
- 普通站点而不只是著名公司；
- 站点结构、平台、技术与社区实践；
- 同一站点跨时间的证据链；
- “缺了什么”本身。

## 8. WikiTeam

- <https://github.com/WikiTeam/wikiteam>

专门保存 MediaWiki 等 wiki 站点。若遇到 wiki 类对象，优先检查 WikiTeam 是否已有 dump，不应把“写一个 wiki 爬虫”当成本项目核心成果。

## 当前空缺 / 本仓真正值得做的部分

已有工具很强，但它们通常分别解决：保存、回放、模拟浏览器、展示截图。

本项目可以专注于以下交叉层：

1. **中文互联网站点身份与谱系**：改名、换域名、镜像、收购、平台迁移；
2. **证据可信度模型**：原始快照、截图、新闻、回忆、研究者复原分层；
3. **历史浏览环境说明**：编码、插件、IE-only、Flash、ActiveX 等；
4. **缺失地图**：明确指出 archive gap，而不是只展示幸存者；
5. **平台形态史**：个人主页、论坛、博客、贴吧/SNS 等如何改变写作与关系结构；
6. **可复核案例**：其他人能按 evidence index 找回同一证据。

## 开工前查重清单

每做一个新站点/平台，AI 必须先回答：

- [ ] Wayback 是否已有快照？覆盖哪些年份？
- [ ] ArchiveTeam 是否做过抢救项目？
- [ ] Common Crawl 是否可补链接/文本证据？
- [ ] 是否存在公开 WARC/WACZ/dump？
- [ ] Web Design Museum 或其他博物馆是否已有视觉展览？
- [ ] 是否需要旧浏览器环境才能正确理解？
- [ ] 我们新增的到底是“保存副本”，还是新的历史解释/证据整理？

如果最后一问答不出来，先不要写新抓取器。
