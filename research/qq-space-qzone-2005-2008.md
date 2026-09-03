# QQ空间 / Qzone 2005–2008：个人空间、浏览器假设与装扮资源链

> 状态：research note；**不是 M1 完整案例**。
>
> 研究对象：2005–2008 年早期 QQ空间（Qzone）的页面入口、QQ 客户端耦合、浏览器使用假设、日志/音乐/装扮功能、静态装扮资源路径，以及 2008 年向 SNS 化页面形态转变的可见证据。
>
> 研究问题：
>
> **早期 QQ空间究竟更接近一个“可自定义个人主页”、一个 QQ 客户端的 Web 延伸，还是已经成熟的 SNS？今天又能从公开残存材料中可靠证明到哪一层？**

---

## 0. 为什么现在研究它

仓库目前已经有百度空间（2006–2015）的 bounded research note，但仍缺一个明显包含：

- 浏览器/客户端耦合；
- 个性化页面布局；
- Flash / 音乐 / 装扮资源；
- 平台托管的静态资源；
- 从个人空间向 SNS 转向；

的中文平台案例。

QQ空间适合作为这个缺口的候选对象，但当前证据仍以官方新闻、同期教程、同期媒体和后来的回忆为主；本轮没有完成可复核的 Wayback/Common Crawl 原始页面 capture 检查，因此不得把它升级为 M1 complete case。

本篇优先推进：

1. 页面入口和 URL ownership；
2. browser / client assumption；
3. Flash 与多媒体作为历史环境条件；
4. 装扮商城和静态资源链；
5. 2006–2008 平台形态变化；
6. 同时代材料与后来回忆之间的边界。

---

## 1. 最小 claim list

| Claim | 当前等级 | 结论强度 |
|---|---|---|
| 2005 年 QQ空间已经作为腾讯 QQ 体系内的个人空间产品上线 | A/C | 已证实“2005 已存在”；精确 6 月 6 日目前主要依赖后来官方纪念/回顾材料 |
| 2006 年同期教程把 `qzone.qq.com` 作为开通/登录入口 | B | 已证实 |
| 2006 年同期教程把 QQ2005 Beta2+ 作为“最佳浏览和使用效果”的客户端条件 | B | 已证实该教程如此要求；不能写成“没有 QQ2005 Beta2 就完全无法使用” |
| 2006 年教程明确让用户在 IE 地址栏输入他人空间地址 | B | 已证实 IE 是教程假设环境；不能据此声称 IE-only |
| 2006 年日志编辑器可插入 Flash、视频、音频链接 | B | 已证实教程所述功能存在 |
| 2006 年页面已有皮肤、漂浮物、挂件、音乐盒等强装扮机制 | A/B | 多来源支持 |
| 2006 年装扮资源至少存在 `imgcache.qq.com/qzone/item/...` 静态资源路径 | B | 已证实同期教程观察到该路径 |
| 2006 年部分用户通过页面模块和 JavaScript 代码绕过/改写装扮效果 | B | 已证实存在这种教程；不是官方支持接口 |
| 2006 年底腾讯称 Qzone 活跃账户达 5700 万 | A | 可证明腾讯当时这样报告；不能当作独立审计后的 MAU 定义 |
| 2008 年腾讯把 Dressing Up、Blog、Photo Album、Music Box、Friends 列为最常用功能 | A | 已证实官方当时如此描述 |
| 2008 年腾讯明确准备加强 SNS 能力并发布 Qzone 5.0 | A | 已证实 |
| 2008 年同期媒体/内部体验稿记录“宽版、透明模块、大标题栏”等自定义变化 | B | 已证实该稿这样记录；其“内部体验”身份仍需独立核验 |
| 后来的“QQ空间最初不是 SNS，而是个人空间/博客产品”回忆与 2008 官方转向 SNS 的材料方向一致 | C + A | 可以写成“相互一致”，不能用后来回忆替代 2005 原始产品定义 |

---

## 2. 2005：上线年份可以确认，但精确起点仍要区分“当时证据”和“后来纪念”

腾讯当前产品页确认 Qzone 是腾讯长期运营的社交/个人空间产品，并保留日志、博客、照片、音乐盒、个人主页装扮等功能描述：

<https://www.tencent.com/products/qzone/>

### 证据等级

**A（当前官方产品页，用于主体身份与持续性）**。

它能支持：

> Qzone / QQ空间是腾讯产品，核心能力长期包括个人资料、日志/博客、照片、音乐与空间装扮。

它不能直接支持：

> 2005 年上线当天页面就已经具有今天列出的全部功能。

关于精确上线日，2015 年十周年回顾及 2026 年腾讯 QQ 官方周年传播均把 2005-06-06 作为正式上线日期。可用作 chronology lead，但它们属于后来回顾，不是 2005 capture。

2015 回顾转载：

<https://down.lusongsong.com/info/3000.html>

2026 周年报道（转述腾讯 QQ 官方）：

<https://finance.sina.com.cn/stock/t/2026-06-06/doc-iniancxr0753880.shtml>

### 证据等级

**C：后来回顾 / 官方纪念性 chronology。**

因此本轮应写：

> “QQ空间在 2005 年已经上线；后来腾讯官方周年材料将正式上线日记为 2005-06-06。”

而不是把 2005-06-06 直接冒充成已经检查过的 2005 A-level page capture。

---

## 3. 2006-03：页面入口不是独立账号体系，而是 QQ 身份和客户端的 Web 延伸

一份日期为 2006-03-30 的同期教程记录：

- QQ 从 `QQ2005 Beta2` 起增加 QQ空间功能；
- 用户需要 QQ 号码；
- 可以从 QQ 好友面板进入自己的空间；
- 也可以访问 `http://qzone.qq.com`，用 QQ 号码登录后开通/进入空间；
- 教程称安装 `QQ2005 Beta2` 及以上版本可获得“最佳浏览和使用效果”。

来源：

<https://m.qqan.com/c/1038>

### 证据等级

**B：同期教程。**

作者署名不详，页面中的部分图片来自 `soft.yesky.com`，存在转抄或二次整理可能，因此不能把整篇视为官方帮助页。

### 可以支持的窄 claim

> 到 2006 年 3 月，至少有一套同期 QQ空间使用路径把 QQ 客户端、QQ 号码和 Web 空间绑定在同一套身份入口中。

### 不能支持的 claim

- 不能写“QQ空间必须依赖 QQ2005 Beta2 才能打开”；
- 不能写“所有用户都只能从 QQ 客户端进入”；
- 不能写“网页端不存在独立登录路径”。

因为同一教程同时明确给出了 `qzone.qq.com` Web 入口。

### 对平台形态谱系的意义

这里的 URL ownership 与身份 ownership 都明显由平台控制：

```text
QQ number
→ Tencent account identity
→ QQ client navigation
→ qzone.qq.com Web entry
→ platform-hosted personal space
```

它不是 1990s 独立个人主页那种：

```text
user owns/maintains HTML
→ user chooses hosting
→ user manually links pages
```

QQ空间虽然强调“自己的空间”，但“自己的”主要是平台内的可配置呈现，不是站长对服务器、域名和 HTML 文件的所有权。

---

## 4. IE 是同期明确假设，但当前证据不足以写成 IE-only

同一 2006 教程在说明如何查看他人空间时，直接写明让用户：

> 在 IE 地址栏输入对方空间地址。

来源仍为：

<https://m.qqan.com/c/1038>

### 证据等级

**B。**

这至少说明：

- 教程作者默认 Windows + IE 是正常访问环境；
- 浏览器环境应成为本案例 reconstruction 的显式变量。

但它**没有证明**：

- Netscape / Firefox / Opera 一定不能用；
- Qzone 页面依赖 ActiveX；
- Qzone 当时存在浏览器嗅探阻断；
- 只有 IE 才能渲染核心页面。

因此正确写法是：

> **IE-assumed historical workflow ≠ IE-exclusive implementation**

后续 M3 浏览环境实验需要实际检查历史 HTML/JS 或旧浏览器回放，才能讨论 IE-only、`document.all`、ActiveX、Trident 私有行为等问题。

---

## 5. Flash 不是“后来回忆里的视觉风格”，而是 2006 同期编辑功能的一部分

2006 教程对日志编辑器的描述明确列出可插入：

- 链接；
- Email 地址；
- 图片；
- **Flash 文件链接**；
- 视频链接；
- 音频链接。

来源：

<https://m.qqan.com/c/1038>

### 证据等级

**B：同期功能说明。**

### 研究意义

这使 Flash 从模糊的“当年很炫”记忆变成一个需要建模的页面依赖。

后续 archive/reconstruction 至少要区分：

```yaml
flash_reference_present: true|false|unknown
swf_url_preserved: true|false|unknown
swf_binary_preserved: true|false|unknown
plugin_required_for_historical_playback: true|false|unknown
modern_replay_uses_raster_fallback: true|false|unknown
ruffle_reconstruction: true|false
```

即使主 HTML capture 完整：

> **HTML survived ≠ Flash experience survived**

如果 SWF、音乐、外链视频或播放器脚本丢失，现代 archive 中“静止的空间页面”可能系统性低估当年的动态体验。

---

## 6. 2006-04：装扮不是抽象功能，而有可观察的静态资源路径

另一份日期为 2006-04-13 的同期教程记录了 QQ空间“装扮空间”中的皮肤资源地址，例如：

```text
http://imgcache.qq.com/qzone/item/pre/13/2029.gif
http://imgcache.qq.com/qzone/item/orig/13/2029.gif
```

教程把前者解释为商城预览资源，把后者解释为实际皮肤图片地址。

来源：

<https://www.qqan.com/article/article_1168_1.html>

### 证据等级

**B：同期用户教程。**

这不是腾讯 API 文档，所以 `pre` / `orig` 的语义只能写成“该教程作者如此观察/解释”，不能自动提升为官方路径合同。

### 重要性

这个 evidence 很适合以后做 archive-gap 调查，因为它把“装扮资源”从一个页面功能拆成独立 resource layer：

```text
Qzone page shell
→ decoration selection
→ imgcache.qq.com/qzone/item/pre/...gif
→ imgcache.qq.com/qzone/item/orig/...gif
→ browser downloads/render asset
```

因此一个用户空间 capture 可能出现：

1. HTML 被保存；
2. 用户文章被保存；
3. 装扮 CSS/JS 被保存；
4. `imgcache.qq.com` 资源没有保存；
5. 最终页面结构仍在，但视觉身份丢失。

这应在 M4 缺失地图中作为独立 resource type 统计，而不是把页面记作简单的“saved / missing”。

---

## 7. 同期“QQ空间代码”说明用户可配置边界曾经比普通主题选择更复杂

同一 2006-04-13 教程还记录了一种用户操作：

- 先从 QQ空间商城/相册取得图片地址；
- 在空间首页“自定义”中新建模块；
- 把带 JavaScript 的 HTML 片段写入模块的“评论”栏；
- 用脚本修改页面背景。

来源：

<https://www.qqan.com/article/article_1168_1.html>

### 证据等级

**B：同期用户实践教程。**

### 必须保留的边界

这只能证明：

> 2006 年存在公开教程教用户通过页面模块字段和脚本片段进行非标准装扮。

它不能证明：

- 腾讯正式支持这种做法；
- 所有账户都允许执行；
- 所有浏览器均执行相同；
- 这种技巧在整个 2006–2008 都有效；
- archive 回放脚本就是历史脚本原样运行。

### 浏览器实验价值

这类页面特别适合 M3：

- 旧 IE 对 `javascript:`、DOM、事件模型的处理；
- archive rewrite 对 JavaScript URL 的改写；
- CSP/现代安全限制；
- 现代浏览器对旧脚本容错；

都可能让同一 capture 出现完全不同结果。

因此未来复原时要把：

> **historical script behavior**

和：

> **archive-rewritten modern behavior**

分开记录。

---

## 8. 2006 年底：腾讯已经把 Qzone 当成大规模“Online Life”组件

腾讯 2007-04-10 的官方品牌战略新闻写到，公司在 2005 年明确“Online Life”战略，并称到 2006 年底拥有：

- 超过 2.30 亿活跃 QQ IM 账户；
- **5700 万活跃 Qzone 账户**。

来源：

<https://www.tencent.com/en-us/articles/80174.html>

### 证据等级

**A：同期官方公司材料。**

### Claim 边界

可写：

> 腾讯在 2007 年官方材料中把 2006 年底的 Qzone 活跃账户数报告为 5700 万，并把它纳入“Online Life”业务组合。

不能直接写：

> 2006 年底有 5700 万独立自然人稳定使用 QQ空间。

原因：

- “active account” 是平台统计口径；
- 可能与自然人一对多；
- 本轮没有独立审计或第三方同口径数据。

---

## 9. 2008-03：官方描述已经明确出现“个人空间 → SNS 网络”的方向

腾讯 2008-03-19 的官方新闻称：

- Qzone 单月活跃用户超过 1 亿；
- 常用功能包括 **Dressing Up、Blog、Photo Album、Music Box、Friends**；
- 产品团队计划在 2008 年进一步部署 SNS network；
- 年中将提供 Qzone 5.0，强化 social networking capacity 与 user experience。

来源：

<https://www.tencent.com/en-us/articles/80148.html>

### 证据等级

**A：同期官方公司材料。**

### 平台谱系意义

这是一条很有价值的“平台自我描述变化”证据：

```text
personal expression / decoration / blog
+ QQ identity and friend graph
→ stronger SNS network
→ central online community platform
```

它支持一个窄结论：

> 到 2008 年，腾讯已经明确把 Qzone 的产品方向描述为强化 SNS 网络，而不是仅维护一组独立个人空间。

它不能单独确定“转型完成于哪一天”。

---

## 10. 2008-07：同期体验稿记录 Qzone 5.0 仍把页面可塑性当作核心产品层

2008-07-15 的驱动中国文章记录了 Qzone 5.0 “自由之夏”的内部测试体验，包括：

- “小窝”“全屏”之外新增“宽版”；
- 首页模块可选半透明/全透明；
- 新增大标题栏；
- 皮肤和模块继续可自由组合；
- 文章还称本次开发强调加载速度、兼容性和扩展性。

来源：

<https://site.qudong.com/2008/0715/17060.shtml>

### 证据等级

**B：同期媒体/体验稿。**

作者声称从腾讯公司内网获得内测入口，但本轮未独立核验作者身份，因此不能把它升级为腾讯内部原始文档。

### 为什么重要

即便 2008 官方已经在强调 SNS，页面“空间感”仍没有立刻消失。

Qzone 5.0 的可见演化更像：

```text
platform-controlled personal homepage
+ dense visual customization
+ QQ friend graph
+ blog/photo/music modules
→ wider/socialized navigation and feed-like aggregation
```

而不是：

```text
personal homepage abruptly replaced by SNS
```

这提醒后续 `platform-genealogy.md` 不要把阶段做成过于整齐的互斥分类。

---

## 11. 后来回忆与同时代材料：哪些可以互相印证，哪些不能

2015 年十周年回顾把 Qzone 的开端描述为：

- 2005 年 4 月内部“小窝”测试；
- 2005-06-06 正式上线；
- 起初参照博客/个人空间产品，而不是成熟 SNS；
- 后续逐步把关系链和社会化能力做重。

来源：

<https://down.lusongsong.com/info/3000.html>

### 证据等级

**C：十年后回顾。**

### 与 A/B 证据的比较

这份回忆的“大方向”与 2008 腾讯官方材料一致：

- 2006 教程强调个人空间、装扮、日志、相册、音乐盒；
- 2008 腾讯官方开始明确强调 SNS network；
- 2008 5.0 体验稿仍保留高度个性化页面布局。

因此可以写：

> 后来的“从个人空间/博客向 SNS 演化”的叙述，与 2006–2008 同时代可见功能和腾讯 2008 年自我描述方向一致。

但不能写：

> 因为 2015 回顾说了，所以 2005 内测流程、内部代号、竞品判断、团队动机都已经得到 A 级证明。

这些内部起源细节仍需要 2005–2006 原始腾讯页面、员工同期记录或可验证 archive capture。

---

## 12. 一个很有价值但只能算 D/C 的恢复线索：QZone Museum

2026 年的非官方项目 **QZone Museum** 声称整理了 2005–2009 年的 5,851 个 QQ空间装饰元素，包括：

- skins；
- pendants；
- floaties；
- cursors；
- title bars；
- Flash music players。

项目说明称其工作从 Internet Archive Wayback Machine 的 CDX index 开始，并发现许多原始装饰资源 URL 长期仍有响应。

来源：

<https://viola.city/projects/qzone-museum/>

### 证据等级

**D/C：现代数字考古项目 / 研究者复原线索。**

它很有价值，但本仓不能把项目整理结果直接当成历史原件。正确用法是：

1. 把它当作 resource locator source；
2. 回到 Internet Archive / original URL 核验；
3. 记录具体 capture datetime、原始 MIME、hash、是否重定向；
4. 再决定是否能把某个资源升级为 A。

它也不能证明 5,851 个资源在同一时间对所有用户可见或可购买。

---

## 13. 页面与资源存续模型

本案例建议至少拆成以下层：

```yaml
platform:
  name: QQ空间 / Qzone
  owner: Tencent

identity_layer:
  qq_number:
  qq_client_entry:
  web_login_entry:

page_layer:
  homepage_shell:
  blog_module:
  photo_album:
  music_box:
  guestbook:
  friend_navigation:

customization_layer:
  skin:
  pendant:
  float_item:
  title_bar:
  custom_module:
  user_script_fragment:

resource_layer:
  imgcache_asset:
  photoimg_asset:
  swf:
  audio:
  video_link:
  external_image:

runtime_layer:
  browser:
  qq_client_version:
  javascript_behavior:
  flash_plugin:
  charset:

archive_layer:
  main_html_capture:
  subresource_capture:
  redirect_capture:
  login_wall:
  rewrite_effect:
```

以后不要再把“某个空间页面保存了”记成单个布尔值。

---

## 14. 浏览器 / 编码 / 插件：当前能说到什么程度

### 已知

- 2006 同期教程显式假设 IE；
- 同期资料要求 QQ2005 Beta2+ 以获得最佳使用效果；
- 日志可嵌入 Flash 文件链接；
- 音乐盒、视频、音频和脚本装扮都可能引入外部运行依赖；
- 2008 5.0 体验稿把兼容性作为重构目标之一。

### 未知

- 具体 IE 最低版本；
- 是否依赖 ActiveX；
- 2005/2006 各页面 Content-Type / charset；
- 是否为 GB2312、GBK 或 UTF-8；
- 浏览器嗅探代码；
- `document.all` / `attachEvent` 等 Trident 私有 API 是否为关键路径；
- Flash Player 最低版本；
- 用户脚本技巧在哪些版本有效；
- Wayback rewrite 是否破坏原脚本。

因此本轮**不能**把“IE、Flash 很典型”写成完成的浏览环境复原。

---

## 15. 建议的 archive 取证顺序

下一轮若要把本对象推进到 M1 complete case，应按下列顺序做 bounded capture verification：

### A. 官方帮助页

候选 original URL：

```text
http://qzone.qq.com/helpcenter/index.html
```

二手引用反复指出一个 2008-12-21 Wayback locator；本轮未能直接打开检查，因此目前只能记为：

> **candidate capture locator, not verified A evidence**

需要实际检查：

- capture datetime；
- HTTP 状态；
- 主 HTML；
- frame/iframe；
- CSS/JS；
- charset；
- 是否登录跳转；
- 子资源缺失率。

### B. 2006 入口页

```text
http://qzone.qq.com/
```

建议抽样：

- 2006-03；
- 2006-04；
- 2006-07；
- 2008-03；
- 2008-07。

目标不是连续抓取，而是比较页面形态断点。

### C. 装扮静态资源

从同期教程给出的 pattern 开始：

```text
http://imgcache.qq.com/qzone/item/pre/...gif
http://imgcache.qq.com/qzone/item/orig/...gif
```

先查 CDX / capture metadata，不批量下载资源。

记录：

- URL；
- capture datetime；
- MIME；
- size；
- digest/hash（档案可得时）；
- 是否仍指向同一内容；
- 是否存在 pre/orig 对应关系。

### D. 页面地址 pattern

同期教程明确说明存在按 QQ 号码直达他人空间的方式，但当前页面文本中的地址写法存在渲染/转写异常（显示为类似 `http://QQ号码.QQ空间.qq.com`）。

在没有历史 capture / DNS / 同期独立材料核验前，不应凭现代常识自动修正成某个确定 hostname pattern。

---

## 16. 可以复原到什么程度

### 当前可做

可以做一个**结构性 reconstruction spec**：

- QQ identity 与空间入口关系；
- 页面模块列表；
- 皮肤/挂件/音乐盒等装扮层；
- Flash / 外链媒体依赖；
- 平台静态资源 host 的存在；
- 2008 版式变化方向。

### 当前不能做

不能制作并声称为“历史原貌”的：

- 2005 首页精确像素级复原；
- 2006 某普通用户完整空间；
- 2006 装扮商城完整资源库；
- 2008 Qzone 5.0 最终正式版页面；
- 当年 Flash/音乐实际播放体验；
- IE 独占行为演示。

原因是尚缺：

- 可验证的历史 HTML/CSS/JS；
- capture-level 子资源清单；
- charset；
- 插件版本；
- 浏览器版本；
- 用户账号状态；
- 外链媒体存续情况。

---

## 17. “已证实 / 高概率 / 不知道”

### 已证实

- 2005 年 Qzone 已作为腾讯产品存在；
- 2006 年已有 `qzone.qq.com` Web 入口；
- QQ 号码和 QQ 客户端与空间访问深度耦合；
- 2006 年同期教程假设 IE，并推荐 QQ2005 Beta2+；
- 2006 年页面支持日志、相册、音乐盒、装扮、Flash/多媒体链接；
- 同期教程观察到 `imgcache.qq.com/qzone/item/...` 装扮资源路径；
- 2008 年腾讯明确把 Qzone 继续向 SNS network 推进；
- 2008 Qzone 5.0 的同期体验材料仍以高度自定义页面为核心体验之一。

### 高概率，但不能升级为确定历史原件

- 2005-06-06 是正式上线日；
- 2005 年内部曾有“小窝”测试阶段；
- 早期 Qzone 主要参照博客/个人空间而非成熟 SNS；
- `pre` / `orig` 是系统化的预览/原图资源层约定。

这些结论目前分别依赖后来官方纪念、后来回顾或用户教程解释。

### 不知道

- 2005 上线当天 HTML 结构；
- 2005/2006 精确 charset；
- IE 最低版本；
- ActiveX 是否为核心依赖；
- Flash Player 最低版本；
- 页面地址 hostname 的准确历史 pattern；
- 某一具体装扮资源在何时上架/下架；
- 普通用户与黄钻用户当时所有权限差异；
- 2008 5.0 内测稿与最终上线版本的完整差异。

---

## 18. 隐私与版权边界

### 隐私

- 不提交普通用户 QQ 号码、空间日志、照片、留言或联系方式；
- URL pattern 用占位符描述，不把随机个人空间作为公开 fixture；
- 若未来必须验证一个用户空间，只记录支持技术 claim 所需的最少字段；
- 不重新公开已经删除的个人内容。

### 版权

- 不把 QZone Museum、Wayback 或仍可访问的腾讯装扮图片批量复制进仓库；
- 不提交历史音乐、视频、Flash、皮肤二进制；
- 优先记录 URL、capture metadata、MIME、hash、尺寸与研究摘要；
- 截图若以后作为论证材料使用，需明确来源、日期与合理使用范围。

---

## 19. 建议写入位置

当前建议保留本文件：

```text
research/qq-space-qzone-2005-2008.md
```

只有在完成至少两个可直接检查的历史 capture、一个浏览器/资源依赖表和一个缺失清单后，再考虑提升为：

```text
studies/qq-space-qzone-2005-2008.md
```

并计入 M1 “博客/SNS/平台案例”。

后续可从本篇抽取到：

- `studies/platform-genealogy.md`：URL ownership、QQ identity、个人空间→SNS；
- `datasets/platforms.csv`：Qzone 2005/2006/2008 时点；
- M3 浏览器实验：IE/modern browser + Flash missing；
- M4 缺失地图：`imgcache.qq.com` / SWF / music / external assets。

---

## 20. 本轮来源表

| ID | 日期 | 来源 | 等级 | 用途 |
|---|---:|---|---|---|
| QZ-A1 | 2007-04-10 | Tencent, “Tencent Launches New Brand Strategy and Ad Campaign” — <https://www.tencent.com/en-us/articles/80174.html> | A | 2006 年底 Qzone 活跃账户、Online Life 定位 |
| QZ-A2 | 2008-03-19 | Tencent, “Active Qzone Users Top 100 Million” — <https://www.tencent.com/en-us/articles/80148.html> | A | 功能使用、SNS 方向、Qzone 5.0 计划 |
| QZ-A3 | current | Tencent Qzone product page — <https://www.tencent.com/products/qzone/> | A（当前） | 产品主体、长期功能描述；不能反推 2005 页面 |
| QZ-B1 | 2006-03-30 | 腾牛，“QQ空间新手学堂 带你步入QZone网络生活” — <https://m.qqan.com/c/1038> | B | QQ2005Beta2、qzone 入口、IE、Flash、模块 |
| QZ-B2 | 2006-04-13 | 腾牛，“用QQ相册打造免费QQ空间皮肤和挂件” — <https://www.qqan.com/article/article_1168_1.html> | B | imgcache 资源路径、用户脚本装扮实践 |
| QZ-B3 | 2008-07-15 | 驱动中国，“自由之夏—QQ空间5.0腾讯公司内测启动” — <https://site.qudong.com/2008/0715/17060.shtml> | B | 5.0 宽版、透明模块、标题栏、兼容性/扩展性 |
| QZ-C1 | 2015-06-05 | 十周年回顾转载 — <https://down.lusongsong.com/info/3000.html> | C | 2005 起源叙事、个人空间→SNS 回忆 |
| QZ-C2 | 2026-06-06 | 新浪财经转述腾讯 QQ 21 周年材料 — <https://finance.sina.com.cn/stock/t/2026-06-06/doc-iniancxr0753880.shtml> | C | 官方纪念性 2005 上线 chronology |
| QZ-D1 | 2026 | QZone Museum — <https://viola.city/projects/qzone-museum/> | D/C | 现代资源恢复项目与 CDX 取证线索 |

---

## 21. Stop conditions / 下一步门槛

在以下任一项未完成前，不把本研究 note 宣称为“QQ空间早期完整复原”：

- 至少两个历史 capture 被直接打开并检查；
- 至少一个 capture 的主 HTML + 子资源关系得到记录；
- charset 被直接观察；
- Flash / script / music 中至少一种依赖得到 capture-level 验证；
- 页面 hostname pattern 得到同期独立证据核验；
- 2008 Qzone 5.0 正式上线版本与内测稿完成区分。

如果 archive 最终只能保存 shell、静态图片和帮助页，而登录后个人状态、音乐、Flash 和动态脚本不可恢复，应把这一“不完整性”写成正式考古结论，而不是用现代资源补齐历史页面。
