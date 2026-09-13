# 配套光盘、离线 Web 客户端与旧网页运行环境：1998—2009 的光介质证据层

## Status

Research note / artifact lead.

**This is not an M1 complete case.**

本轮没有取得满足仓库合同要求的：

- 两个已实际打开并核验的 historical Web capture；
- 原始零售 / 出版母盘的完整 provenance chain；
- 已在历史 OS / 浏览器环境中执行的镜像 replay。

本轮真正新增的是另一类旧网证据对象：**当年的实体配套光盘 / ISO 可能保存了 Web 本身没有保存下来的浏览器、客户端、插件、帮助文件、URL、离线网页工具与版本关系。**

---

## 1. 为什么 old-web archaeology 不应只盯 Wayback

仓库现有方法已经反复强调：

```text
page != platform
capture != transaction
locator != verified capture
```

本轮再增加一条：

```text
historical Web environment != Web archive corpus
```

一个 1999 年网站真正运行所需要的东西可能包括：

- IE / Netscape 的具体版本；
- Acrobat Reader / Java / ActiveX / DirectX / media player；
- OICQ / ICQ / mail / FTP client；
- 字体、输入法、编码支持；
- 离线帮助和安装说明；
- ISP / 软件商提供的辅助客户端；
- 当时用户从杂志光盘取得的补丁。

这些对象常常不是网页，因此 Web crawler 根本不会自然保存它们。

相反，它们可能被当年的 CD-ROM / DVD-ROM 完整带走。

因此可以定义一个新的 artifact family：

## `optical-media runtime fossil / 光介质运行环境化石`

它不是 historical Web capture，却可能是恢复 historical Web execution environment 的一手或近一手材料。

---

## 2. 1998《大众软件》光盘：Internet 内容通过完全离线的介质进入 PC

一个现代保存页面记录的《大众软件》1998 年 8 月配套光盘：

- 镜像大小约 629 MB；
- 当前保存页给出 SHA1 `34FD85265EED198FA521C2A8EB340CC6F70A8814`；
- 目录中出现 Winamp 1.92、WebTwin 1.1a、网络类软件，以及“因特网上的虚拟现实”等文章。

来源：

- https://www.shopmsdn.com/detail-%E5%A4%A7%E4%BC%97%E8%BD%AF%E4%BB%B6%28%E9%85%8D%E5%A5%97%E5%85%89%E7%9B%98%29%281998.08%29%28%E6%80%BB%E7%AC%AC14%E6%9C%9F%29-3238.html

当前页面对 WebTwin 还保留了同期风格的软件说明：

- 可读取 Web HTML；
- 转成 Windows Help 文件；
- 可以承担类似 offline browser 的工作；
- 软件目录为 `\NET\WEBTWIN\WEBTWI.EXE`；
- 给出历史 URL `http://www.webtwin.com`。

这特别重要，因为同一张盘同时保留了：

```text
software binary locator
+ local path
+ historical product URL
+ contemporary functional description
+ neighboring software ecosystem
```

即使 `webtwin.com` 的历史网页最终保存很差，配套盘仍可能留下“这个 Web 软件当时怎样进入用户机器”的另一条证据链。

### Evidence grade

当前只能给 **C / artifact lead**：

- 现代站点提供 ISO 文件名、大小、SHA1 和目录；
- 但本轮没有独立馆藏 / 原始物理盘 hash 交叉确认；
- 也没有下载并挂载该 ISO 做文件级验证。

所以不能写成“已经验证原始 1998 光盘”。

---

## 3. 1999《电脑报》配套盘：可以恢复一套 Web 客户端版本矩阵

保存下来的 1999 年 5 月《电脑报配套光盘》目录列出：

- 中文 IE 5.0；
- Netscape 4.51；
- Acrobat Reader 4.0；
- ICQ 99a Beta；
- DirectX 6.1；
- Windows NT 4 SP4；
- 多个软件升级 / Service Pack；
- 网页图像优化工具等。

来源：

- https://software-archive.tifan.la/%E7%94%B5%E8%84%91%E6%8A%A5/1999/20/99201501.html

这不是一个简单的软件清单。

对 OWA 来说，它可以转化成一个很具体的 **historical client bundle hypothesis**：

```text
May 1999 Chinese PC user
├── IE 5.0 Chinese
├── Netscape 4.51
├── Acrobat Reader 4.0
├── ICQ 99a Beta
├── DirectX 6.1
└── contemporaneous patches / utilities
```

如果未来某个 1999 中文网站只有在特定浏览器 / PDF Reader / plugin 行为下才能正确理解，这类盘可能提供比“随便找一个 Windows 98 ISO + IE6”更接近实际用户环境的组合。

### 方法价值

历史浏览器实验不应只问：

> 这个网页能不能在 IE5 打开？

还应该问：

> **当时普通用户能通过什么渠道取得 IE5、Netscape、Reader 和相关补丁？它们是否真的在同一时期一起被推荐 / 分发？**

配套盘可以回答第二类问题。

---

## 4. `offline acquisition of online capability`

这轮 HPL 交叉研究增加了一个对 OWA 也很重要的机制：

## `offline acquisition of online capability / 在线能力的离线取得`

旧网用户未必通过 Web 下载浏览器和客户端。

真实路径可能是：

```text
报刊亭 / 书店
→ 买杂志 + CD-ROM
→ 安装 IE / Netscape / ICQ / Reader
→ 再拨号上网
```

这会影响 old-Web archaeology 对 download counter、software home page 和 user acquisition 的解释。

例如：

```text
historical download count != historical installed base
```

因为大量安装副本可能通过：

- 杂志配套盘；
- OEM 预装；
- 朋友拷贝；
- 电脑城装机；
- 单位 / 学校共享；
- 盗版 / 合集盘

进入机器，而没有触发原软件站的一次 HTTP download。

因此不能从旧软件下载页面的 archive traffic / counter 单独反推软件的真实普及。

---

## 5. `physical transport as bandwidth`

这组材料还补出一个 old-Web 基础设施层：

## `physical transport as bandwidth / 物理运输充当带宽`

1998—1999 的一张 CD 可以装入数百 MB 软件和内容。

用户获得这些字节的链条可能是：

```text
publisher/editor
→ mastering
→ disc replication
→ newspaper/book distribution
→ local shop/newsstand
→ user walks home
→ CD-ROM drive
```

Web archive 通常只记录链条最后可能出现的 URL，却完全不记录前面这套**离线数据运输网络**。

因此一个网站的软件生态可能在 archive 中显得“下载页资源缺失”，现实历史里却并不代表用户无法取得软件。

这是解释 missing binary 时必须考虑的反例。

---

## 6. 光盘里的 URL 是一种特殊 locator，但绝不是 capture

配套盘目录和 README 往往会留下：

- 软件主页；
- FTP；
- 作者 email；
- GeoCities / personal homepage；
- vendor site；
- update URL。

例如 1998《大众软件》保存页中能看到 WebTwin URL 与若干软件作者地址。

这些数据特别适合用于 old-Web discovery：

```text
CD-ROM metadata / README
→ historical URL candidate
→ archive index probe
→ verified capture
```

但必须坚持：

## `disc URL locator != historical Web capture`

一张 1998 光盘能证明“这个 URL 当时被软件说明引用”，不能证明：

- 该 URL 在光盘发行日一定可访问；
- 页面内容是什么；
- HTTP 状态码是什么；
- charset / DOM / subresources 是什么；
- archive 是否完整保存。

它是一条 A/B/C 级程度取决于原盘 provenance 的 **historical locator evidence**，而不是 Memento。

---

## 7. 配套盘本身也是混合文档：binary + HTML + HLP + text + media

Web archaeology 常以 HTML 页面为天然研究单位。

配套光盘迫使我们改用更宽的对象模型：

```text
Disc image
├── launcher / autorun
├── directory tree
├── executable installers
├── HTML / local mini-sites
├── HLP / CHM / TXT / README
├── images / video / audio
├── URLs / email / FTP references
└── timestamps / file versions
```

因此对一张光盘的最低 archaeology manifest 应至少记录：

- label / volume identifier；
- image size；
- hash；
- filesystem（ISO9660 / Joliet 等）；
- root tree；
- autorun；
- executable names + version evidence；
- HTML / HTM / HLP / CHM count；
- extracted historical URLs；
- embedded browser assumptions；
- file timestamps（但不能简单当发行日期）；
- malware scan / safe execution status；
- source provenance。

---

## 8. “光盘镜像现在网上能下载”不等于 provenance 已经解决

现代软件 / 游戏档案站已经保存不少 1990s—2000s 配套盘镜像，而且常提供 SHA1。

例如现有页面可看到：

- 《大众软件》1998.04 / .06 / .08 / .11 / .12 等多个 ISO；
- 1999 多期双 CD；
- 《电脑迷》2003—2014 大量配套盘集合；
- 《电脑爱好者》2009 合订本双 DVD。

这非常有研究价值，但不能把“有 SHA1”误写成“hash verified original”。

需要至少区分：

```text
A. 原始出版方 / 图书馆 / 实体盘成像
B. 两份独立实体盘成像 hash 一致
C. 单一社区镜像 + 清单 / 图片可对照
D. 只有文件名 / 网盘转载 / 无来源镜像
```

本轮接触到的主要是 **C 级 artifact leads**。

后续只有在 provenance 提升后，才适合把镜像正式放进 reproducible browser lab。

---

## 9. 2007—2009：宽带增长没有让光盘立即退出

一个简单的“拨号 → ADSL → 光盘死亡”叙事并不成立。

### 2007

现存《开天辟地学电脑—全面掌握 Windows XP》配套光盘把：

- IE6；
- MSN / Messenger；
- 拨号上网；
- 防火墙；
- 家庭 / 办公网络；
- 远程桌面；

做成面向电脑初、中级用户和培训班的本地多媒体教程。

当前保存页：

- https://www.shopmsdn.com/detail-%E6%B4%AA%E6%81%A9-%E5%BC%80%E5%A4%A9%E8%BE%9F%E5%9C%B0%E5%AD%A6%E7%94%B5%E8%84%91-%E6%96%B0%E7%BC%96%E5%85%A8%E9%9D%A2%E6%8E%8C%E6%8F%A1WindowsXP%28%E9%85%8D%E5%A5%97%E5%85%89%E7%9B%98%29%282007%29-4343.html

### 2008

北京网通推出 8 Mbps ADSL 时，同期报道已经把速度解释成“约 10 分钟下载一张 650 MB 光盘内容”；但这一档包月 498 元，同时市场上还有明显更低速的 4M / 2M / 1M / 512K 层级。

- https://tech.sina.com.cn/t/2008-05-17/07162201056.shtml

### 2009

《电脑爱好者》合订本仍用两张约 4 GB 的 DVD 提供：

- 2008—2009 期刊全文检索；
- 电子书；
- 技巧 / 故障资料。

- https://www.shopmsdn.com/detail-Oracle8PersonalEdition%288.0.4%29%28NT/95/detail-%E7%94%B5%E8%84%91%E7%88%B1%E5%A5%BD%E8%80%85-2009%E5%90%88%E8%AE%A2%E6%9C%AC%E9%85%8D%E5%A5%97%E5%85%89%E7%9B%98%28%E4%B8%8A%29%28%E4%B8%8B%29%282DVD%29-3013.html

所以 archive 设计也不能预设“2005 以后 optical media 不重要”。

旧 Web 的历史运行环境至少到 2000s 后期仍和 DVD / ISO / virtual drive 生态交错。

---

## 10. ISO 进一步把“物理光盘”变成了网络文件

2009 年的同期软件页面仍大量介绍 DAEMON Tools 等虚拟光驱工具，明确支持 ISO / CUE / CCD / MDS 等镜像格式。

这产生一个很有意思的循环：

```text
physical software distribution
→ disc image format
→ Internet download
→ virtual optical drive
→ old installer sees “disc” again
```

因此 optical-disc archaeology 不能只等同于“收藏塑料圆片”。

**光盘作为逻辑介质，可以在实体盘衰退后继续活在 ISO 和虚拟光驱中。**

同期来源：

- cnBeta, 2009-04-25, DAEMON Tools 4.30.4。
  - https://m.cnbeta.com.tw/view/82722.htm
- MyDrivers / 快科技, 2009-08-07, DAEMON Tools Pro 4.35。
  - https://news.mydrivers.com/1/141/141528.htm

Evidence: **B， samtidiga software-release pages / mirrors.**

---

## 11. 海外对照：CD-ROM 不是中国 Internet 落后的偶发现象

Pew / Times Mirror Center 在 1995 年对美国 4005 名受访者的调查发现：

- online service 订户约近 1200 万；
- 约 200 万人直接 Internet 连接；
- 调查中的家庭电脑用户约 48% 已有 CD-ROM drive；
- 52% CD-ROM 用户至少每周使用一次；
- 受访者对 CD-ROM 的依赖评价高于 online services。

来源：

- https://www.pewresearch.org/politics/1995/10/16/americans-going-online-explosive-growth-uncertain-destinations/

这意味着：

> “数字内容先本地化，再逐渐联网更新”是 1990s 家庭计算的一条跨国共同路径，而不是“中国因为 Internet 慢所以才用光盘”的特殊失败史。

对 OWA 而言，海外 PC magazine cover discs、AOL / ISP CDs、shareware CDs 也应作为比较性的 runtime artifact family，而不是只比较 Wayback coverage。

---

## 12. 新的保存机制：`artifact inversion`

本轮提出一个值得后续检验的保存现象：

## `artifact inversion / 保存倒置`

一个历史软件可能出现：

```text
website → dead / poorly archived
binary → survives on magazine CD image
README → survives locally
historical URL → survives inside README
browser that accessed site → survives on same disc
```

结果是：

**原本作为“网站附件”的软件和说明，反而比网站主体活得更久。**

这会改变 old-web discovery 顺序。

过去常见：

```text
known URL → Wayback → missing assets
```

未来可以增加：

```text
known software / magazine
→ preserved ISO
→ extract README / URL / version
→ archive probe
→ browser reproduction
```

---

## 13. 对 M1 / M3 的具体影响

### M1

配套盘本身不能替代 M1 对 historical captures 的要求。

即使盘里写着：

`http://www.webtwin.com`

也只能增加：

- historical locator；
- software identity；
- contemporaneous distribution evidence。

仍需独立取得并打开 Web captures。

### M3

配套盘对 M3 浏览器复现价值更高。

如果 provenance 足够强，可以用来构建：

- 1998 Chinese consumer software bundle；
- 1999 browser / Reader / ICQ matrix；
- companion documentation；
- plugin / helper-app inventory。

这样 M3 不再只靠“我们认为那个年代大概用 IE5/6”的后见猜测。

---

## 14. Privacy / security

老光盘可能包含：

- 旧邮箱；
- 作者姓名 / 地址；
- 注册码；
- 序列号；
- 论坛用户名；
- 恶意软件 / 宏 / exploit；
- 自动运行程序。

因此：

1. 默认只在隔离 VM / offline environment 挂载；
2. 不执行未知 autorun；
3. 先做静态清单和 hash；
4. 普通个人邮箱只在研究必要时最小化引用；
5. serial / credential 不重新公开结构化整理；
6. 研究旧恶意内容只做防御性 / 保存性分析。

---

## 15. Current evidence table

| Evidence | Current status | Grade | What it supports | What it does NOT support |
|---|---|---:|---|---|
| 1996/1997 electronic-publication rules | confirmed text | A | physical digital media was formal publication category | ordinary household adoption |
| 1998 People’s Daily industry statistics | contemporaneous report | A/B | rapid CD-ROM publishing growth | household usage distribution |
| 1998 PopSoft disc catalog | current archive record | C | software/content bundle + historical locators | verified original-disc provenance |
| 1999 Computer News cover-disc list | preserved catalog | B/C | IE5/Netscape/ICQ/Reader contemporaneous bundle | exact bytes unless ISO verified |
| 2007 Windows XP training disc | archive record | C | continued offline Internet training path | scale of use |
| 2008 ADSL report | contemporaneous | B | broadband speed/cost transition | nationwide affordability |
| 2009 Computer Fan DVD record | archive record | C | optical corpus persisted in broadband era | usage frequency |
| 1995 Pew US survey | contemporaneous survey | A/B | overseas mass CD-ROM use before online dominance | China-specific adoption |

---

## 16. Archive probe result / stop condition

本轮没有把现代镜像站“有 ISO”写成 artifact verified。

当前准确状态：

```text
historical optical-media identity: ACHIEVED
contemporaneous cover-disc contents: ACHIEVED for several catalog records
historical software/version/URL leads: ACHIEVED
modern ISO hash leads: ACHIEVED
independent original-media hash verification: NOT ACHIEVED
isolated mount + file manifest: NOT ACHIEVED
verified historical Web memento derived from disc URL: NOT ACHIEVED
M1 complete case: NOT ACHIEVED
```

### 下一步 stop / go 判据

值得继续投入的条件：

1. 能取得一张来源明确的 1998—2000 实体盘镜像；或
2. 两个独立镜像源给出一致 hash；或
3. 盘内 URL 能导向一个此前未发现、且可以实际打开核验的 historical Web capture；或
4. 盘内浏览器 / plugin 对一个已有 M1 候选 case 的显示结果产生实质差异。

如果只是继续找到更多“某期杂志也有光盘”的目录，不再增加新机制，就应停止扩张该专题。

---

## 17. 本轮方法结论

旧 Web 不只生活在服务器上。

一部分旧 Web 的客户端环境、软件入口和 URL 线索，当年是被**压进一张光盘，装进杂志袋子，再通过报刊发行网带到用户电脑旁边**的。

因此 old-web archaeology 需要同时保存：

```text
server-side captures
+ client-side runtime
+ distribution media
+ documentation / URLs
```

否则我们可能成功复原了一张 HTML，却仍然没有复原那个普通用户当年真正拥有的 Web。