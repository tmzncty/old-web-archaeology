# Discuz! 7.2 的字符集不是一个字段：发行包、数据库、HTTP 头、模板与回放乱码，2009–2012

> 性质：bounded research note / charset-preservation artifact package。  
> 范围：Discuz! 7.2 在 2009–2012 年间的编码发行形态，以及它对中文旧网回放、乱码判断和 M3 浏览环境实验的直接影响。  
> 不是：Discuz! 全史、论坛文化史、漏洞复现教程，也不宣称已经获得并验证全部官方安装包的原始字节。

---

## 0. 为什么这轮选这个对象

仓库的 `ROADMAP.md` / `RESEARCH_PLAN.md` 一直要求完整案例记录 browser / encoding / plugin assumptions，M3 也明确要求比较字符编码差异。

但当前仓库虽然已有大量：

- 平台消失链；
- URL ownership；
- IE / ActiveX / Flash；
- transaction-state gap；

却几乎没有把中文旧站最常见的 **GBK / BIG5 / UTF-8** 做成一个可以落地核验的 artifact model。

本轮先不继续新增一个“页面 != 状态”的领域文件，而选一个非常具体、可验证的历史软件对象：

**Discuz! 7.2（2009-11-19 发布）及其多编码发行包。**

它的价值不在于“Discuz 很流行”这一常识，而在于：同一个论坛版本本身就以不同字符集发行；部署环境中的 Apache charset 规则又可能覆盖页面内声明；管理员迁移 BIG5 → UTF-8 时还会同时碰到程序文件、模板和数据库数据。

因此，旧网考古里看到一页乱码时，不能只问：

> 这个 HTML 是 GBK 还是 UTF-8？

而应先问：

> 到底是哪一层的 charset 与哪一层不一致？

---

## 1. 研究对象与本轮问题

对象：

```text
Discuz! 7.2
release: 2009-11-19
period examined: 2009-11 to 2012-07
```

本轮只回答六个问题：

1. 7.2 是否确实存在多字符集发行，而不是后来下载站重新打包？
2. 这些编码是否只是浏览器显示选项，还是与升级 / 程序包选择绑定？
3. BIG5 → UTF-8 的真实站长迁移会碰到什么？
4. Web server 的 charset 配置能否制造“程序没坏但浏览器乱码”的情况？
5. 对 archive replay 来说，保存 HTML 文本是否足以判断历史编码？
6. 以后 M1 / M3 的 evidence schema 至少需要记录哪些 charset 层？

---

## 2. 时间线

### 2009-11-19 — Discuz! 7.2 发布

至顶网 / ZDNet 软件频道在 2009-11-19 的同期报道中记录 Discuz! 7.2 正式发布，报道来源标为康盛创想，并概述其新增邮箱登录、分类信息检索、版块绑定域名等功能。

来源：

- 至顶网 / ZDNet 软件频道，2009-11-19，《Discuz! 7.2发布 优化产品细节30余项》  
  https://soft.zhiding.cn/software_zone/2009/1119/1516611.shtml

证据等级：**B+（同期行业媒体；内容标示来自康盛创想）**。

本轮只用它锁定 7.2 的发布时间，不用它证明字符集细节。

---

### 2010-01-01 — 同期普通站长材料保留了官方 GBK 包 locator

一篇 2010-01-01 的博客园文章把 Discuz! 7.2 的下载地址直接写为：

```text
http://download.comsenz.com/Discuz/7.2/Discuz_7.2_FULL_SC_GBK.zip
```

同时把 `comsenz.com` 标为官网。

来源：

- 博客园 glc400，2010-01-01，《与大家分享几个开源的网站系统》  
  https://www.cnblogs.com/glc400/archive/2010/01/01/4473757.html

证据等级：**B（同期普通技术博客 / operational locator）**。

它能证明：

- 2010 年初普通用户确实把 `download.comsenz.com/Discuz/7.2/` 当作官方产品下载位置；
- `Discuz_7.2_FULL_SC_GBK.zip` 这个 filename 当时已经在使用。

它不能单独证明：

- 这个 URL 今天仍指向完全相同的字节；
- 文件从未被替换；
- 其他三个编码包在同一天一定同时存在。

---

### 2010-02-02 — BIG5 → UTF-8 的第一人称迁移，显示编码属于“整站栈”而非单页开关

2010-02-02，一名繁体中文 Discuz 管理员记录自己把论坛从 BIG5 转成 UTF-8 的实际操作和失败。

按研究必要最小化，只保留技术事实：

- 原论坛使用 BIG5；
- 管理员希望转 UTF-8，以减少无法表示字符 / 乱码问题；
- 迁移不是简单切换一个前台选项，而涉及重新安装同版本 UTF-8 环境、从 BIG5 版本备份数据再恢复；
- UCenter 编码一致性成为顾虑；
- 直接把旧 7.0 文件覆盖到 7.2 后出现大量乱码，后来确认问题与错误复用旧文件有关。

来源：

- WordPress / 無產劣品小誌，2010-02-02，《Discuz 7.2 更新[暴走狀態]》  
  https://snowheartma.wordpress.com/2010/02/02/discuz-7-2-%E6%9B%B4%E6%96%B0%E6%9A%B4%E8%B5%B0%E7%8B%80%E6%85%8B/

证据等级：**B（同期第一人称站长操作记录）**。

这个来源不能代表所有 Discuz 安装，但足以反驳一个过度简化：

```text
charset migration = 修改一个 meta 标签
```

至少在这个真实 2010 个案里，管理员面对的是：

```text
程序包编码
+ UCenter 编码
+ 数据库备份 / 恢复
+ 旧程序 / 模板文件
```

的组合问题。

---

### 2010-02-07 — 第三方保存了一份同时代 `SC_UTF8` 二进制副本

SourceForge 的 `icandy` 项目文件列表目前仍显示：

```text
Discuz_7.2_FULL_SC_UTF8.zip
modified: 2010-02-07 13:29:15 UTC
size: 4.7 MB
```

来源：

- SourceForge `icandy` files  
  https://sourceforge.net/projects/find-candy/files/

证据等级：**A- / derivative artifact（同时代文件对象，但不是官方托管；官方来源真实性尚未用 hash / signature 证明）**。

这里最重要的边界是：

> “2010 年有一份叫这个名字的 UTF-8 包被第三方保存”

不等于：

> “这份文件已经被证明逐字节等同于 2009/2010 康盛官方下载包”。

在取得官方 checksum、多个独立副本一致 hash、或可信原始介质之前，不升级其 provenance。

---

### 2011-01-28 — 升级教程明确把四种编码当成不同发行选择

2011-01-28 的 Discuz! 7.0 → 7.2 升级教程直接记录官方版下载入口：

```text
http://www.comsenz.com/downloads/install/discuz
```

并列出四种编码：

- 简体中文 GBK；
- 简体中文 UTF-8；
- 繁体中文 BIG5；
- 繁体中文 UTF-8。

教程要求根据原 Discuz! 7.0 的编码选择相应 7.2 程序包，而不是任意混用。

来源：

- 365建站网，2011-01-28，《Discuz!7.0 to Discuz!7.2 升级图文说明》  
  https://www.365jz.com/article/15855

证据等级：**B（近同时代操作教程；保留官方入口与升级路径）**。

这条证据很重要，因为它说明“GBK / UTF-8 / BIG5”至少在发行与升级层面是 **package identity** 的一部分。

不能把它仅仅写成：

```yaml
page_encoding: gbk
```

更接近历史实际的是：

```yaml
software_release:
  product: Discuz! 7.2
  language_variant: simplified_chinese
  package_encoding: gbk
```

---

### 2012-07-17 — 一个 GBK 安装在 Apache `AddDefaultCharset UTF-8` 下实际显示乱码

2012-07-17 的 51CTO 原创技术记录部署：

```text
Discuz_7.2_FULL_SC_GBK.zip
```

首次打开安装页时出现乱码。

作者随后在 Apache `httpd.conf` 中把：

```apache
AddDefaultCharset UTF-8
```

注释掉，重启 Apache 后页面恢复正常显示。

来源：

- 51CTO，smile12321，2012-07-17，《两台web服务器之间轻松实现负载均衡》  
  https://blog.51cto.com/blue3/933400

证据等级：**B+（同期第一人称技术实验 / deployment record）**。

Apache 2.2 官方文档对 `AddDefaultCharset` 的语义说明是：对于 `text/plain` / `text/html` 响应，该指令可以加入默认 charset 参数，并可能覆盖 HTML body 中 `META` 指定的 charset。

来源：

- Apache HTTP Server 2.2 documentation, `AddDefaultCharset`  
  https://httpd.apache.org/docs/2.2/mod/core.html#adddefaultcharset

证据等级：**A（软件版本官方技术文档；用于解释指令语义，不证明某个历史站点一定如此配置）**。

这两条证据组合后，可以确认一个对旧网考古非常重要的具体机制：

```text
正确的 GBK 程序 / 页面字节
+
服务器强加 UTF-8 HTTP charset
→
浏览器可显示乱码
```

也就是说：

> **乱码不自动等于 archive 抓坏了，也不自动等于原 HTML 文件编码错误。**

它可能来自服务器响应头与应用输出编码的冲突。

---

### 2026 当前 — 官方历史版本页仍按四编码保存 7.2 下载入口

当前 `Discuz! 官方站` 的历史版本下载页仍为 Discuz! 7.2 / 7.2 FULL 列出：

- 繁体 UTF-8；
- 繁体 BIG5；
- 简体 UTF-8；
- 简体 GBK。

来源：

- Discuz! 官方站，历史版本下载页（2026 当前访问状态）  
  https://download.discuz.vip/olddz.html

证据等级：**C+ / current official catalog**。

它可用于确认今天官方项目仍把这些历史编码版本作为产品谱系的一部分；不能倒过来代替 2009–2010 同期下载页。

---

## 3. 本轮核心结论：旧中文论坛的 charset 至少是七层对象

结合上述 artifact，可以先提出一个 **D 级研究模型**，以后必须用真实 capture / package bytes 继续验证：

```yaml
encoding_layers:
  package_variant:
    examples: [SC_GBK, SC_UTF8, TC_BIG5, TC_UTF8]

  source_and_template_bytes:
    meaning: PHP / template / language file 的实际字节编码

  database_charset:
    meaning: forum / UCenter 数据库存储及连接编码

  application_output_charset:
    meaning: 应用本身期望输出的编码

  http_header_charset:
    meaning: Content-Type 中服务器实际发送的 charset

  html_meta_charset:
    meaning: 页面 body 内 meta 声明

  client_or_archive_decoding:
    meaning: 历史浏览器、现代浏览器或 archive replay 最终如何解码字节
```

这七层不应该被压成一个 `charset=gbk`。

至少已经有直接证据证明：

- package variant 不唯一；
- 升级时 package encoding 需要与既有安装对应；
- BIG5 → UTF-8 可涉及数据库与程序文件；
- Apache HTTP 层可与 GBK 程序输出发生冲突；
- browser display 最终结果因此不能只从页面可见文字反推。

---

## 4. 对 Web archive 的直接影响

### 4.1 解析后的 Unicode 文本不是原始编码证据

搜索引擎、archive full-text、现代浏览器 DevTools 或研究工具如果只给出已经解码后的 Unicode 文本，可能已经丢失：

- 原始响应字节；
- HTTP `Content-Type`；
- body meta；
- archive 自己采用的解码猜测；
- 原服务器是否额外注入 charset。

所以：

```text
readable Chinese text today
!=
known historical charset
```

反过来：

```text
mojibake today
!=
known historical corruption
```

---

### 4.2 Memento / WARC 取证时必须分开保存 header 与 payload

以后如果找到一个历史 Discuz 页面，最低限度应该分别记录：

```yaml
original_url:
capture_url:
capture_datetime:

response:
  content_type_raw:
  header_charset:

payload:
  raw_bytes_available:
  byte_hash:
  meta_charset:
  detected_encoding:
  detection_method:

replay:
  archive_decoding:
  mojibake_present:
  replay_transform_known:
```

如果 raw bytes 不在手上，不能仅凭 archive 渲染结果写“该站使用 GBK”。

---

### 4.3 同一 URL 在不同服务器配置下甚至可能得到不同显示结果

2012 的部署记录尤其提醒：

同一个 Discuz GBK 程序目录，如果搬到另一台 Apache 上，而后者设置不同的 `AddDefaultCharset`，浏览器显示结果就可能变化。

因此：

```text
site software artifact
!=
served representation
```

对复原实验来说，除了保存应用文件，还要保存 / 明示：

- Web server 类型和版本；
- charset 相关 server config；
- PHP / app 输出 header；
- 浏览器实际接收到的 HTTP header。

否则“离线打开源码看起来正常”不代表当年 HTTP 服务出来也正常。

---

## 5. 对 M3 浏览器实验的意义

Discuz! 7.2 可以提供一个比“换浏览器看看页面长什么样”更严谨的 charset 实验。

以后在隔离环境中可以建立最小矩阵：

```text
A. SC_GBK package + AddDefaultCharset Off
B. SC_GBK package + AddDefaultCharset UTF-8
C. SC_UTF8 package + AddDefaultCharset Off
D. SC_UTF8 package + wrong GBK header
```

再分别比较：

- IE6 / IE8；
- 同时代 Firefox；
- modern Chromium；
- archive replay / raw-byte viewer。

记录：

1. HTTP header；
2. meta charset；
3. 浏览器自动检测行为；
4. 页面可见乱码；
5. form 提交后中文字节是否往返一致；
6. 数据库存储是否发生不可逆转换。

### 安全边界

Discuz! 7.2 已停止维护并存在已知漏洞。

若以后真的做 M3：

- 仅离线 / host-only 网络；
- 不暴露公网；
- 不导入真实历史用户数据库；
- 不复现攻击利用；
- 只研究 rendering / encoding / configuration。

---

## 6. Artifact / evidence table

| 对象 | 日期 | Grade | 能证明 | 不能证明 |
|---|---:|---|---|---|
| Discuz! 7.2 发布报道 | 2009-11-19 | B+ | 7.2 同期已发布 | 四编码包当天的精确文件字节 |
| `Discuz_7.2_FULL_SC_GBK.zip` 官方 locator 的普通用户记录 | 2010-01-01 | B | filename + `download.comsenz.com` operational locator | 当前下载文件与当年逐字节相同 |
| BIG5 → UTF-8 迁移第一人称记录 | 2010-02-02 | B | 一个真实管理员经历了 package / DB / file encoding 问题 | 所有 Discuz 用户都必须同样操作 |
| SourceForge `SC_UTF8` 文件对象 | 2010-02-07 | A- derivative | 同时代第三方保存了该 filename 的 4.7 MB 文件 | 它与官方包 hash 一致 |
| 7.0 → 7.2 升级教程 | 2011-01-28 | B | 四种编码发行选择；升级需匹配原编码 | 2009 首发页的全部下载信息 |
| 51CTO GBK + Apache 部署 | 2012-07-17 | B+ | `AddDefaultCharset UTF-8` 与 GBK 安装发生真实乱码冲突 | 每个 Discuz 站都采用该 Apache 配置 |
| Apache 2.2 `AddDefaultCharset` 文档 | version-specific | A | 指令语义 / header 层可覆盖 body meta | 任一具体站点实际配置 |
| 当前 Discuz 历史下载页 | 2026 current | C+ | 当前官方谱系仍列四编码 | 当年页面 UI / 当年文件 hash |

---

## 7. 已证实 / 高概率 / 不知道

### 已证实

- Discuz! 7.2 在 2009-11-19 已发布；
- 2010 年初存在 `Discuz_7.2_FULL_SC_GBK.zip` 这个官方目录 locator 的同期用户记录；
- 2011 的升级材料明确记录 GBK / UTF-8 / BIG5 四种发行选择，并要求匹配原安装编码；
- 2010 的真实站长记录显示 BIG5 → UTF-8 迁移会牵涉程序 / UCenter / 数据恢复 / 文件混用问题；
- 2012 的真实部署记录显示一个 GBK 7.2 安装在 Apache `AddDefaultCharset UTF-8` 下出现乱码，关闭该默认 charset 后恢复；
- Apache 2.2 官方文档说明该指令可给 text/html / text/plain 响应附加 charset，并可能覆盖 body meta；
- 今天 Discuz 官方历史版本页仍把 7.2 保存为四种字符集下载变体。

### 高概率，但本轮不升级

- `SC_GBK / SC_UTF8 / TC_BIG5 / TC_UTF8` 四个包在 7.2 首发期即同时由康盛官方提供；
- 各包内部语言文件 / 模板 / installer 默认 charset 有系统性差异；
- 数据库与 UCenter encoding mismatch 是迁移失败的重要来源。

这些都很合理，也被后续材料支持，但本轮尚未逐个核验 2009 首发下载页和四个原始二进制包。

### 不知道

- 2009-11-19 首发时四个包的 exact filename / byte size / SHA-256；
- 官方包是否在 2009–2012 期间静默替换过；
- SourceForge 2010 副本是否与康盛包逐字节一致；
- 7.2 四编码包里具体哪些文件只是转码，哪些配置值不同；
- 典型真实论坛的 HTTP header charset 与 meta charset 一致率；
- Wayback / Common Crawl 对 GBK Discuz 页面历史上怎样保存 raw header 与 payload；
- 某个具体论坛出现的 mojibake 应归因于 origin server、archive replay 还是后来的 parser。

---

## 8. 可复原到什么程度

### 当前可复原

- 7.2 的发布时间；
- 多编码发行模型；
- 至少一个同期官方 GBK 下载 locator；
- 一个同期 UTF-8 derivative artifact locator；
- 一个 BIG5 → UTF-8 真实迁移路径；
- 一个 GBK 应用与 Apache UTF-8 header 冲突导致乱码的真实部署案例；
- charset 多层证据模型。

### 当前不能复原

- 2009 官方下载页原貌；
- 四个首发包的 authoritative hash；
- 任一真实 2009–2012 Discuz 论坛的完整 header + raw bytes + DB + browser session；
- “所有 Discuz 7.2 页面默认都是 GBK”或任何类似泛化；
- 某个 archive capture 的乱码原因，除非 raw bytes / header / replay transform 都能检查。

因此：

**M1 complete case: NOT ACHIEVED**。

但这轮已经补上了一个此前明显欠缺的 **charset preservation mechanism**。

---

## 9. 哪些内容不能声称已经证明

禁止从本轮证据写出：

- “Discuz! 7.2 默认就是 GBK，所以看到的老论坛都是 GBK”；
- “乱码一定是浏览器兼容性”；
- “Wayback 把中文抓坏了”；
- “页面里有 `<meta charset>` 就能知道历史响应编码”；
- “今天官方历史下载页的 zip 一定就是 2009 原始包”；
- “SourceForge 的 2010 zip 已证明为官方原件”；
- “BIG5 → UTF-8 只需数据库转码”或相反“必须完全重装”；
- “Apache `AddDefaultCharset` 是 Discuz 普遍乱码的主要原因”。

这些都超出现有证据。

---

## 10. 隐私与版权边界

这个对象主要是软件 / 配置层，个人隐私风险低于论坛帖子考古，但版权边界仍要明确。

### 可以保存

- 历史下载 URL；
- filename；
- timestamp；
- file size；
- cryptographic hash（若以后合法取得文件）；
- 公开 release / install 文档中的必要技术事实；
- 少量 configuration key / charset metadata；
- 自己离线实验产生的 diff / screenshot。

### 不应直接提交到仓库

- 完整 Discuz! 7.2 安装包；
- 大量受版权保护源码；
- 第三方论坛完整数据库；
- 真实用户帖子 / 私信 / 账号数据；
- 漏洞利用 payload 或可直接用于攻击仍在线旧站的步骤。

如果以后必须验证二进制，只提交：

```yaml
filename:
source_locator:
retrieved_at:
size:
sha256:
provenance_status:
```

以及为 charset claim 所需的最小片段 / metadata。

---

## 11. 下一步最值钱的 bounded artifact work

1. **取得四个 7.2 历史包的可验证副本**：优先官方当前历史下载页与至少一个独立旧镜像；只下载用于本地 hash / metadata，不提交二进制。
2. 计算 SHA-256，并比较多个来源是否同 hash；若不一致，记录 package replacement / repackaging，而不是挑一个当“真”。
3. 离线解包，不执行，比较：
   - installer charset；
   - `config.inc.php` / UCenter charset 相关字段；
   - template / language file bytes；
   - HTML meta / PHP header 输出；
   - SQL schema / connection charset。
4. 搜索 2009-11-19 至 2010-02 的 Comsenz 官方下载页 historical capture，恢复四包 exact locator。
5. 找一个 2009–2012 的公开 Discuz 论坛 historical capture，要求能够取得：
   - original URL；
   - capture datetime；
   - raw `Content-Type`；
   - raw payload 或至少 byte-preserving artifact；
   - body meta；
   - replay 可见状态。
6. 若 raw bytes 与 replay 文本不一致，优先记录 **archive decoding divergence**，不要擅自“修复”后当历史原件。
7. M3 实验只在离线环境做 GBK / UTF-8 × Apache header × historical browser 矩阵。

---

## 12. 方法结论

这个案例对中文旧网最有用的提醒不是“以前常用 GBK”。

而是：

> **历史字符编码是一条从软件发行包、数据库、应用输出、HTTP header、HTML body 到浏览器 / archive replay 的链；任何一层错位都可能在今天表现成同一种“乱码”。**

因此以后遇到 mojibake，最小正确姿势不是先猜编码，而是留下：

```text
bytes
+ header
+ meta
+ package / app context
+ replay transform
```

如果这五样里缺了三四样，研究结论应该写“未知”，而不是把现代浏览器的自动解码结果当作历史事实。

---

## AI-assisted research note

本研究笔记由 AI 辅助整理。所有历史断言均按 contemporaneous operational evidence、later/current official catalog 与 researcher inference 分层；未执行历史 Discuz 代码、未访问私人论坛数据、未复制历史安装包进仓库。