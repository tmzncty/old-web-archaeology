# M3 最小浏览环境差异实验协议（设计稿，尚未执行）

日期：2026-11-12。状态：**protocol only / no historical capture verified / no M3 acceptance claimed**。

## 研究缺口与边界

ROADMAP M3 要求对同一历史页面比较 modern Chromium、IE5/6 级、可行时 Netscape 级环境，以及 Flash/Ruffle 或插件缺失，最终列出至少五个**经实验观察**的解释差异。现有 #12（QQ 空间 Flash）、#13（支付宝控件）、#17（Netscape 中文环境）为对象/机制研究，不能替代同一 artifact 的受控实验。此协议不重复其历史事实。

## 工具证据（不是中文网站的历史证据）

- **A / contemporary primary documentation of present tooling**：OldWeb.today 项目自述可将模拟 Netscape/IE 浏览器连接 Web archive，浏览器镜像内可能预装 Flash/Java；其 IE6 镜像注明 Win98 + Flash 9。<https://github.com/oldweb-today/oldweb-today>（2026-11-12 查阅）。这只能说明模拟器作者对当前工具的描述，**不能证明某中文网站当年用过这些配置**。
- **A / contemporary primary documentation of present tooling**：ReplayWeb.page 官方说明支持 WARC/WACZ，使用现代浏览器的 replay frontend，并集成 Ruffle；WARC 需索引，WACZ 可按需加载。<https://replayweb.page/docs/formats/>；<https://webrecorder.net/replaywebpage/>（2026-11-12 查阅）。
- **D / methodological inference**：工具的 archive rewrite、浏览器模拟、Flash 运行时及资源覆盖差异都是混杂变量；跨工具截图差异不能直接归因于浏览器引擎。

以上两个项目是独立的软件/文档来源，但不是两个独立的历史中文站点 evidence families。后者仍须另找。

## Artifact 入选门槛

只选择公开的、非敏感的 1995–2015 中文页面，优先 2000–2004 年官方帮助/产品页。需有：（1）原始 URL 和精确 capture datetime；（2）能实际读取的原始响应 bytes 或 WARC（不仅 Wayback locator）；（3）主文档及关键子资源的逐项清单；（4）HTTP Content-Type、charset/meta、hash；（5）至少两个独立历史 evidence families（例如原始 capture + 同期独立教程/报道），避免两个镜像转载冒充互证。若缺原始 bytes，标 candidate，不进入实验。

## 预注册实验矩阵

| 条件 | 浏览器/运行时 | 输入 |
|---|---|---|
| E0 | 原始 bytes 静态解析（无执行） | 同一主 HTML、headers、子资源清单 |
| E1 | 现代 Chromium + archive replay | 固定 capture 与 viewport |
| E2 | OldWeb.today Win98 IE6（记录实际镜像与插件版本） | 同一 capture |
| E3 | OldWeb.today Netscape 4（记录 OS/镜像） | 同一 capture |
| E4 | 现代 Chromium + Ruffle 与禁用 Ruffle 两次 | 同一 capture，限已许可 SWF |
| E5 | 仅当合法且可控时：历史 charset/字体/locale 的单变量变化 | 相同 bytes |

对每次运行记录：UTC 执行时间、capture URL、原始 URL、capture timestamp、工具版本/commit、OS、浏览器版本、插件版本、viewport、网络请求与缺失清单、编码判定、控制台/JS 错误、截图 hash、观察者、是否启用 live fallback。不得静默补取当前网站资源。

## 五类待检验假设（不是五个已证实差异）

1. HTTP charset / META / 自动探测的优先级是否使相同中文字节显示不同；
2. 表格/frameset 布局在固定 viewport 下是否发生可测几何变化；
3. document.all / 浏览器嗅探 JS 是否使导航或表单功能不同；
4. SWF 在插件缺失、旧 Flash 和 Ruffle 下是否有不同呈现或交互；
5. 字体缺失、CJK glyph、图片资源及大小写路径是否影响可见内容。

每项结果必须同时记录原始观察和**至少一个竞争解释**（例如缺图可能来自 archive 未抓取而非浏览器）；不成立也保留 negative result。至少五项必须在一个案例上观察并复核，才满足 M3 验收。

## 运行安全与复原边界

不在联网生产机器运行历史 ActiveX、未知 SWF、Java Applet 或专有插件。优先静态检查；需要动态运行时使用隔离 VM/模拟器、禁用访问私人网络及外部副作用。不要提交普通用户主页全文、联系方式、私密帖子、专有二进制或受版权保护的媒体。只提交 locator、metadata、hash、经许可的最小截图与自写分析。

## 建议后续文件与停止条件

- 实验前：在 `research/m3-artifact-selection.md` 登记候选、独立来源家族、实际验证状态与被排除理由；
- 实验后：在 `experiments/browser-matrix/<case-id>/` 保存 `manifest.yaml`、`observations.csv`、`missing-resources.md` 和 `interpretation.md`；
- 如无合格原始 bytes、无许可或无法隔离执行：停止动态实验，保留 negative result；不得勾 ROADMAP M3。
