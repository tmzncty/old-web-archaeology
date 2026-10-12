# QQ 空间 Flash / IE ActiveX 浏览环境边界（2006）

> 状态：bounded research note；**不是 M1 完整案例**。
>
> 目标：补 ROADMAP M1/M3 中仍缺的“浏览器 / 插件假设”，并避免把“页面里有 Flash”与“整个站点依赖 ActiveX”混为一谈。

## 1. 对象与问题

对象：2006 年前后的 QQ 空间（QZone）装扮、Flash 皮肤与自定义页面，以及同一时期 IE6 对 ActiveX/Flash 的执行环境变化。

核心问题：

1. QQ 空间在 2006 年是否实际把 Flash 作为用户空间表现层的一部分？
2. IE6 的 ActiveX 行为变化是否会改变同一 QQ 空间页面的历史体验？
3. 现有证据能证明到哪一层，哪些仍必须等待原始 HTML/SWF/capture？

## 2. 证据分级

### E1 — 2006-11-10 腾讯声明（A-：同期官方文本的媒体转载）

来源：新浪科技转载腾讯声明，《腾讯声明拍拍网会坚守三年免费承诺》，2006-11-10。

定位：https://tech.sina.com.cn/i/2006-11-10/21091232045.shtml

声明明确把 QCC 定义为 QQ 空间提供的 **Flash 皮肤服务**：用户可制作 Flash 皮肤、存储于 QQ 空间、交易，并用它改变空间整体装扮。它还明确区分 QQ 空间的存储/维护与拍拍网的交易平台角色。

可支持：
- 2006 年 QQ 空间确有平台支持的 Flash 皮肤产品，而非只有用户私下嵌入 SWF；
- Flash artifact 可能由 QQ 空间托管，因而“HTML 页面幸存”与“装扮资源幸存”必须分开记录。

不能支持：
- 具体 SWF URL pattern；
- Flash Player 版本；
- `<object>` / `<embed>` 结构；
- QQ 空间整体必须使用 IE/ActiveX。

### E2 — 2006-11-09 QCC 同期报道（B）

来源：新浪科技，《拍拍网联合QQ空间推虚拟物品交易商城》，2006-11-09。

定位：https://tech.sina.com.cn/i/2006-11-09/16351229360.shtml

报道独立记录 QQ 空间提供多款 Flash 皮肤、允许用户交易原创 Flash 作品，并记录平台承担作品存储。

作用：与 E1 形成不同文本来源的同期交叉验证，支持“Flash 是平台化装扮对象”这一事实。

### E3 — 2006-04-11 QQ 空间实际操作教程（B）

来源：太平洋电脑网，经新浪保存，《教你清除QQ空间右上方广告》，2006-04-11。

定位：https://tech.sina.com.cn/s/s/2006-04-11/0957898726.shtml

文章记录的实际操作包括：用 IE 访问 `http://Q-Zone.qq.com/web`、选择“安全模式”、进入“装扮空间”、选择皮肤、使用“自定义 / 个性设置 / 新建模块”等页面操作。

可支持：
- 2006 年存在 `Q-Zone.qq.com/web` 这一用户入口的同期记录；
- QQ 空间页面存在“安全模式”和可配置模块/皮肤的表现层；
- IE 是当时实际使用环境之一。

不能支持：
- “安全模式”等于禁用 Flash/ActiveX；
- 只有 IE 才能访问；
- 教程中的第三方代码在今天仍安全或应被复现。

### E4 — IE6 ActiveX 行为变化（B，独立浏览器环境证据）

来源：太平洋电脑网，经新浪保存，《微软升级IE 看Flash要多点一次鼠标》，2006-03-06。

定位：https://tech.sina.com.cn/s/s/2006-03-06/0807858040.shtml

报道记录微软修改 IE 对 ActiveX 控件的处理方式，影响 Flash 动画和媒体等嵌入内容；适用 Windows XP SP2 / Windows Server 2003 SP1 的 IE6，并延伸到 IE7。

可支持：
- 同一个包含 Flash 的历史页面，在不同补丁状态的 IE6 上可能产生不同交互步骤；
- “浏览器版本”字段不足，至少还应记录 OS/SP 与相关 ActiveX 更新状态。

不能支持：
- QQ 空间在该更新后具体出现了何种提示；
- 某一 QQ 空间 capture 必然受此更新影响。

### E5 — 2010 QQ 空间 Flash 模块操作记录（B，较晚但仍在目标时代内）

来源：多特软件，《悠悠凉爽QQ空间情感FLASH动画模块》，2010-08-23。

定位：https://m.duote.com/tech/3/6066.html

记录“自定义 → 新建模块 → FLASH 动画模块 → 填入 Flash 地址 → 调整尺寸 → 保存”的操作，并保留一个 `.swf` 外链示例。

可支持：
- 至少到 2010 年，QQ 空间仍存在用户可指定外部 SWF locator 的 Flash 模块形态；
- 资源所有权可与页面所有权分离：页面在 QQ 空间，SWF 可在第三方 host。

不能支持：
- 2006 年已经存在完全相同的外链模块机制；
- 示例第三方 SWF 今天仍应抓取或再发布。

## 3. 事实 / 推断分离

### 已证实

- 2006 年 QQ 空间存在平台支持的 Flash 皮肤产品（E1/E2）。
- 平台承担至少部分 Flash 作品的存储与维护（E1/E2）。
- 2006 年同期教程记录 IE、`Q-Zone.qq.com/web`、安全模式、装扮空间和自定义模块操作（E3）。
- 2006 年 IE6 的 ActiveX 处理方式发生过会影响 Flash 等嵌入内容的变化（E4）。
- 2010 年 QQ 空间存在可填写外部 Flash 地址的 Flash 模块操作路径（E5）。

### 高概率但尚未证明（D）

- 2006 年的部分 QQ 空间装扮页面在 IE 中通过 Flash Player ActiveX 实例执行 SWF；这是技术上合理的假设，但本轮没有取得 QQ 空间原始 HTML/object/classid 证据。
- QQ 空间“安全模式”可能用于降低复杂装扮/脚本造成的访问问题；但没有原始帮助文档，不能说明它具体禁用了什么。

### 不知道

- 2006 QZone 的历史 `Content-Type` / charset；
- Flash Player 最低/推荐版本；
- `<object classid>`、`codebase`、`<embed>` 等实际标记；
- SWF 是否跨域加载 XML/图片/音乐；
- IE6 更新前后同一空间的实际交互差异；
- Firefox/Netscape/Opera 当时对相同空间的兼容程度；
- 平台托管 Flash 与用户外链 Flash 的 URL 生命周期差异。

## 4. 对仓库方法的增量

这一对象要求把“插件依赖”至少拆成：

```text
page HTML
→ embed declaration
→ plugin family (ActiveX / NPAPI / other)
→ plugin version
→ browser version
→ OS / service pack / browser patch state
→ SWF artifact
→ SWF secondary network dependencies
```

并把资源所有权拆成：

```text
QZone page owner
≠ QZone-hosted decoration owner/operator
≠ third-party SWF host
≠ browser plugin/runtime provider
```

因此：

`page capture exists ≠ Flash experience preserved`

`SWF file survives ≠ SWF remains executable`

`IE6 identified ≠ historical IE6 behavior fully specified`

`Flash present ≠ site proven IE-only`

## 5. 建议写入位置

当前只建议保留本研究笔记。取得原始 artifact 后再考虑：

- `studies/platform-genealogy.md`：补“页面 URL 与装扮资源 URL/host 分离”；
- M3 实验设计：增加 `OS/SP/browser patch/plugin build` 字段；
- evidence schema：增加 `runtime_dependency`、`embedded_resource_locator`、`execution_status`。

不要仅凭本 note 勾选 M1 或 M3。

## 6. 下一步 artifact probe

优先窗口：2006-03 至 2006-12。

1. 找 `Q-Zone.qq.com/web`、QQ 空间帮助页、装扮页的合法历史 capture；
2. 保存 capture datetime、original URL、HTTP Content-Type、raw HTML/hash；
3. 静态检查 `object`、`embed`、`classid`、`codebase`、`.swf` locator；
4. 对 SWF 只记录 URL、capture、size/hash 和依赖 metadata，不在仓库重新分发；
5. 若存在同一页面在 2006 IE ActiveX 更新前后的 capture，再设计旧 IE 环境对照实验；
6. 单独区分平台 CDN SWF 与第三方外链 SWF。

## 7. 缺失证据与停止条件

当前最关键缺失是 **QQ 空间自己的原始 HTML/帮助文档与 SWF locator**。如果只能继续找到媒体教程和后来回忆，而拿不到 artifact，应停止把结论向“具体执行机制”扩张。

## 8. 隐私、版权与安全边界

- 不为验证插件机制而批量进入普通用户历史空间；优先使用平台首页、帮助页、公开产品页或机构账号。
- 不重新发布普通用户自制 Flash、照片、音乐、评论或个人资料。
- 历史 SWF/ActiveX 只做静态 metadata/hash/provenance；不在日常主机直接执行未知二进制。
- 第三方 SWF URL 仅作为历史 locator 证据，不代表仓库拥有再分发权。
- 不把现代模拟器的输出伪装成历史截图；任何 Ruffle/虚拟机结果必须标 reconstruction/experiment。

## 9. 本轮结论

本轮足以证明：**2006 年 QQ 空间的页面表现层确实包含平台化 Flash 皮肤，而同年 IE6 的 ActiveX 执行行为本身正在变化。** 因此复原 QQ 空间不能只保存 HTML/截图，也不能只写“IE6 + Flash”；需要把浏览器补丁状态、插件家族、SWF artifact 与资源 host 分层记录。

但本轮仍不能声称“2006 QQ 空间整体依赖 ActiveX”或“只有 IE 能正常使用”。这两个说法必须等待 QQ 空间原始页面 artifact 与跨浏览器实验。