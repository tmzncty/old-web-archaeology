# Netscape 4.x 中文运行环境：编码、locale、字体与输入法边界（2000–2002）

## 研究对象与理由

本笔记研究 2000–2002 年 GNU/Linux/X11 环境中 Netscape Communicator 4.72/4.73 的中文运行条件。它不是某个网站的完整案例，而是为 M1 的“浏览器/编码/插件假设”和 M3 浏览环境复原提供一个可复用的环境边界案例。

仓库已有 IE/ActiveX、Flash、Java 等运行时研究，但“charset 声明正确就等于中文页面可以按历史方式显示/输入”的假设仍需拆解。本案例显示，历史中文 Web 的可用性还依赖 locale、X 字体、X resources、输入法启动顺序和浏览器补丁状态。

## 核心结论

在 Netscape 4.x + X11 的历史环境中，至少应区分：

`HTML bytes / HTTP charset / META charset`

`→ process locale`

`→ X locale data / patch state`

`→ X resources (Netscape.ad / fontList)`

`→ installed CJK fonts`

`→ input method (xcin/chinput)`

`→ browser build`

`→ rendered/readable text and form-input capability`

因此：

- `page bytes are GB2312 ≠ Chinese renders correctly`；
- `Chinese renders correctly ≠ Chinese can be entered into forms`；
- `Netscape 4.73 identified ≠ one reproducible runtime`；
- `same HTML capture ≠ same historical experience across locale/font/resource states`。

## 时间点与证据

### 2000-05-30：Netscape 4.72 的 GB2312/Big5 X resources 与输入问题

**证据等级：A（同时代技术邮件/开发维护记录）**

Debian Chinese 邮件列表中 Anthony Fok 记录了针对 Netscape 4.72 的 `Netscape.ad.472.zh_CN.GB2312.Debian` 与 `Netscape.ad.472.zh_TW.Big5.Debian`。邮件同时指出：

- GB2312 中文输入仍缺一个 X locale patch；
- Big5 输入存在异常；
- `libnsfix` 可能导致 Netscape crash；
- 若要输入中文，需要先启动 `xcin` 或 `chinput` 再启动 Netscape，否则 Netscape 可能 crash。

来源：Debian Chinese mailing list, 2000-05-30, message-id `20000530102228.B5994@lovelife.olvc.ab.ca`。

公开定位：<https://lists.debian.org/debian-chinese/2000/05/msg00097.html>

这条材料证明的是 Netscape/X11 中文运行环境的具体依赖关系；它不证明某一个中文网站要求这些组件。

### 2000-07-08：Netscape 4.73 CJK Debian 测试包

**证据等级：A（同时代维护/发布测试记录）**

Anthony Fok 在 Debian Chinese 邮件列表发布 Netscape 4.73 CJK 测试包信息，明确列出：

- `netscape-base-4_4.73-32.1.4_i386.deb`；
- `netscape-base-473_4.73-19.2_i386.deb`；
- `netscape-zh-resource-473_4.73-19.2_all.deb`；
- 简体中文需要相应字体包，繁体中文需要相应字体包；
- 简体环境示例为 `LANG=zh_CN.GB2312`，繁体为 `LANG=zh_TW.Big5`；
- `xcin`/`Chinput` 用于表格中的中文输入。

来源：Debian Chinese mailing list, 2000-07-08, message-id `20000708102651.A25887@lovelife.olvc.ab.ca`。

公开定位：<https://lists.debian.org/debian-chinese/2000/07/msg00080.html>

这提供了一个可复现实验矩阵的历史锚点：browser build、locale、font package、input method 应作为独立变量记录。

### 2002-01-30：错误 fontList 可导致中文异常

**证据等级：A（同时代用户故障排查记录）**

Debian Chinese Big5 邮件列表中一名用户记录：通过 `xrdb -query` 发现 Netscape 的 `fontList` 只有 `iso8859-1 charset`，执行 `xrdb -remove` 后 Netscape 恢复正常。邮件同时提到此前使用 `zh_CN.GB2312/Netscape` resource 配置。

来源：Debian Chinese Big5 mailing list, 2002-01-30, message-id `D139779A9ABFD31184C500508B6FB8A61172510A@CNSVWSHSX0002`。

公开定位：<https://lists.debian.org/debian-chinese-big5/2002/01/msg00184.html>

这条材料很重要，因为它表明即使页面本身和浏览器二进制都没有变化，X resource/font configuration 仍可改变中文显示结果。

### 独立机制背景：网页编码声明与浏览器解释并非同一层

**证据等级：B（近同时代技术教程）**

2004 年赛迪技术文章（新浪转载）逐步演示了 JSP 输出字节、HTTP charset 与 IE 解码之间的关系：同一组字节在错误 charset 下会显示乱码，而手动改变浏览器页面编码可能恢复中文。它不是 Netscape 的直接证据，但独立支持“bytes / server declaration / browser interpretation 必须分层记录”的方法论。

来源：赛迪网/新浪科技，2004-11-15：
<https://tech.sina.com.cn/s/s/2004-11-15/1403459387.shtml>

## 事实、回忆与推断边界

### 已证实

1. 2000 年 Debian 社区确实为 Netscape 4.72/4.73 维护 GB2312/Big5 相关 X resources 与 CJK 测试包。
2. 在该环境中，locale、字体、输入法和部分 patch/resource 状态会影响中文显示或输入。
3. 2000-05 的维护记录明确报告启动输入法与 Netscape 的先后顺序可能关系到 crash。
4. 2002-01 的实际故障记录显示 `fontList` 被限制为 ISO-8859-1 时会造成中文问题，移除相关 X resource 后恢复。

### 高概率但尚未对具体旧站证明

1. 对 1999–2002 中文网页做 Netscape 级复原时，仅设置页面 charset 不足以定义历史运行环境。
2. 某些历史表单“今天无法输入中文”可能来自输入法/XIM/X resource 环境，而非站点后端或 HTML 本身。
3. 同一 capture 在现代 Chromium、Windows IE 和 Linux Netscape 4.x 中可能出现不同的中文可读性和表单输入能力。

### 不知道 / 不能声称已经证明

1. 不能据此声称 2000 年中国大陆普通用户普遍使用 Linux Netscape；本案例是运行环境边界，不是市场份额研究。
2. 不能据此声称任何具体中文站点要求 Netscape 4.73、xcin 或这些 Debian patches。
3. 尚未获得一个具体历史中文页面 artifact，并在严格复原的 Netscape 4.73 环境中完成对照实验。
4. 尚不能量化 GB2312、GBK、Big5、UTF-8 在 2000–2002 中文 Web 的实际占比。
5. 邮件中的 crash/输入行为是当时具体软件组合的观察，不能外推到所有 Unix/X11 或所有 Netscape 4.x build。

## 对 M1 / M3 的建议字段

建议浏览环境记录至少加入：

- browser family / exact build；
- OS / distribution / architecture；
- process locale (`LANG`, `LC_*`)；
- HTTP `Content-Type` charset；
- HTML META charset；
- detected/forced browser encoding；
- installed CJK fonts；
- X resources / browser resource files；
- input method and startup order；
- relevant locale patches / compatibility libraries；
- `render_readable` 与 `form_input_working` 分开记录。

这能防止把“网页显示正常”和“网页交互可用”压成一个布尔值。

## 建议写入位置

当前先保留为 `research/` bounded note。后续可将方法结论写入：

- `docs/METHOD.md`：浏览环境证据字段；
- M3 实验方案：增加 `locale/font/input-method/resource-state` 变量；
- 未来 `schemas/evidence.schema.json`：把页面编码声明与运行环境编码状态拆开。

在没有具体页面 artifact 和复现实验之前，不修改 ROADMAP 完成状态。

## 下一步 artifact probe

优先选择一个 2000–2002 的公开、非敏感中文技术/门户静态页面，要求能取得原始 HTML bytes 或可信 archive capture。对同一 artifact 记录：

1. HTTP charset 与 META charset 是否一致；
2. modern Chromium 解码结果；
3. Netscape 4.73 + `zh_CN.GB2312` + 对应字体环境；
4. 改变/移除 `Netscape.ad` 或 fontList 后的差异；
5. 页面含表单时，分别测试“显示中文”和“输入中文”；
6. 不执行来源不明的插件、Java applet 或下载二进制。

目标不是证明“旧浏览器更真实”，而是至少列出五项由浏览环境导致的解释差异，以直接推进 M3 验收。

## 隐私与版权边界

- 本研究只引用公开技术邮件与公开技术文章，不采集私人邮件、账号数据或普通用户已删除页面。
- 邮件列表内容只保留必要技术事实、日期和 message-id，不在仓库镜像整封邮件。
- Netscape、字体包、兼容库等历史二进制不直接提交仓库；若后续合法取得，只记录来源、版本、hash 和许可状态。
- 对未来用户主页 artifact，优先选择机构/技术/公开示例页；普通个人主页仅记录最低必要 metadata，不重新发布个人内容。

## 证据分级摘要

| 时间 | 证据 | 等级 | 能证明什么 |
|---|---|---|---|
| 2000-05-30 | Debian Chinese Netscape.ad / patch / input-method 维护邮件 | A | Netscape 4.72 中文环境存在具体 locale/resource/input 依赖 |
| 2000-07-08 | Debian Chinese Netscape 4.73 CJK 测试包邮件 | A | 4.73 的 CJK 包、字体、locale 与输入法组合 |
| 2002-01-30 | Debian Chinese Big5 实际 fontList 故障排查 | A | X resource/fontList 可独立改变中文显示结果 |
| 2004-11-15 | 赛迪/新浪 JSP 编码教程 | B | bytes、HTTP charset 与浏览器解码应分层记录 |
| 本笔记提出的复原矩阵 | 研究者模型 | D | 待具体页面实验验证 |
