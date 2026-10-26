# 虎翼网 51.net 免费个人主页：从“主页”到共享虚拟主机的托管边界（2000–2007）

> 状态：bounded research note；不是 M1 完整案例。  
> 研究窗口：约 2000–2007。  
> 核心问题：早期中文互联网所谓“免费个人主页”究竟给用户什么——页面编辑器、账号下的文件树、FTP、次级域名，还是完整虚拟主机？这些托管约束怎样决定今天还能复原什么？

## 1. 为什么选择这个对象

仓库已经覆盖网易/263 等免费主页的收费与关闭链条，但对**主页仍在运行时的实际托管环境**仍缺少足够具体的案例。虎翼网（51.net）提供了一个很好的边界对象：2002–2003 年同期新闻可以确认其“虚拟个人主页/免费个人主页”确实存在；现存官方帮助中心又保留了 FTP、`public_html`、次级域名、UNIX 文件名大小写、免费用户单文件大小限制等操作语义。

这使研究重点从“某免费主页何时关闭”转向：

```text
作者本地文件
  -> 上传工具 / FTP
  -> 托管账户
  -> public_html 文件树
  -> 次级域名
  -> 共享服务器 / 流量与文件限制
  -> 访问者浏览器
```

这条链中的任一层变化，都可能造成“页面看起来消失”或“复原后与当年不一致”。

## 2. 证据等级约定

沿用仓库 A/B/C/D 规范，并在本 note 内额外标明材料时间属性：

- **A**：运营方/系统自身留下的原始材料或 artifact；
- **B**：近同时代新闻、教程等二手材料；
- **C**：参与者后来回忆；
- **D**：本研究根据证据作出的复原/推断。

注意：现存 51.net 帮助页属于运营方原始文档，故可作为 A 类材料证明“该文档当前如此陈述”；但页面未提供可核验的历史发布时间，因此**不能自动当成 2000–2003 年的同时代 A 级快照**。对具体历史配置仍需 archive capture。

## 3. 证据包

### E1 — 2002-01：虎翼网已有“虚拟个人主页”，且托管服务器可以作为独立故障对象

**等级：B（同时代新闻）**

北京晚报 2002-01-12 报道（新浪存档）称，虎翼网因异常访问暂时关闭两台服务器；报道把被访问对象称为虎翼网和网易的“虚拟个人主页”，并引述虎翼网总裁张天山称访问量达到平时约 400–500 倍。

定位：正文开头至对异常访问的描述。

来源：
https://tech.sina.com.cn/i/c/2002-01-12/99314.shtml

**可以支持：**

- 2002-01 时虎翼网确实运营虚拟个人主页托管；
- 承载主页的服务器是可单独受影响/关闭的基础设施对象；
- “域名仍存在”与“托管服务器当前可服务”不是同一状态。

**不能支持：**

- 不能据此确定全部主页由几台服务器承载；
- 不能证明故障期间所有 51.net 子域均不可达；
- 不能证明具体用户页面的数据是否损坏；报道反而称被访问服务器数据不会受损；
- 不复述或保存报道涉及的攻击工具、攻击方法与恶意站点细节，本项目只关心托管可用性。

### E2 — 2003-03：免费个人主页仍在开放注册，并实施按时段/名额的准入

**等级：B（同时代新闻）**

北京晚报 2003-03-08 报道（新浪存档）称，51.net 虎翼网“以免费主页所著称”，当时为了避开白天上网高峰，每日凌晨 3 时开始接受免费个人主页空间注册，达到 1000 人即止。

定位：全文第一段。

来源：
https://news.sina.com.cn/c/2003-03-08/184867462s.shtml

**可以支持：**

- 2003-03 免费个人主页服务仍在提供；
- 免费托管的“可获得性”受平台资源政策控制，不是持续无限注册；
- 平台服务状态至少应拆成 `existing pages served` 与 `new account registration available`。

因此：

```text
hosting service online != registration continuously open
registration closed/full != existing homepage deleted
```

### E3 — 现存 51.net 官方帮助：次级域名、FTP、`public_html` 与本地编辑/再上传模型

**等级：A（运营方原始文档；当前可访问，历史日期未核验）**

51.net 现存“虚拟主机问题”帮助页给出一组非常具体的操作语义：

- 次级域名用户以 `http://***.51.net` 浏览；
- 用户不能直接在服务器上编辑 HTML，应在本地保留备份，修改后重新上传覆盖；
- FTP 示例使用 `wang1.51.net`，登录后进入 `public_html`；
- FrontPage、Dreamweaver、Netscape Composer、CuteFTP、FlashFXP 等均被列入上传路径；
- 页面称服务器使用 UNIX 系统，因此文件名大小写敏感；
- 文件名要求使用英文字母和数字，不允许中文字符；
- 免费用户通过 FTP 上传的单文件大小不得超过 200K；
- 文档还明确区分免费/普及型与更高等级主机能力，免费用户没有 PHP/CGI/ASP 权限。

定位：帮助页中“我怎样浏览我的网站”“我怎样修改、编辑我网页的HTML文件”“FTP”“FrontPage/Dreamweaver/Netscape Composer”“上传文件大小”“论坛”等问答。

来源：
https://www.51.net/help/qa_hosting.php

相关 FTP 官方帮助：
https://www.51.net/help/qa_ftp.php

**直接意义：**

这里的“个人主页”至少在这套帮助文档所描述的产品形态里，并非只有一个 Web 表单编辑器，而具有典型共享主机的文件部署语义：作者在本地制作文件，经 FTP/发布工具上传到服务器文件树，再由次级域名映射到该空间。

**历史边界：**

现存页面还自述虎翼网相关服务“自 2000 年 5 月开通以来”，但由于缺少该帮助页自身的历史 capture/版本日期，本 note **不把今天页面中的每一项限制倒填到 2000 年 5 月**。尤其是 200K 单文件限制、各主机等级、PHP/MySQL、流量配额等可能经历过调整。

### E4 — 后来用户回忆：51.net 被记忆为 FTP 空间 + 次级域名

**等级：C（参与者后来回忆）**

2016 年建立的个人站点 VOLNET 回忆，拨号上网年代曾在虎翼网（51.net）申请“ftp 空间”，取得次级域名，并用网页制作工具制作静态 HTML 页面后上线。

定位：首页文章开头“做个人网站大概已经是十几年前……”段。

来源：
https://volnet.github.io/

该回忆与 E3 的官方帮助语义吻合，因此可提高“FTP + 次级域名 + 本地静态 HTML 制作”作为真实用户工作流的可信度；但它没有给出准确年份、账户名或原始 capture，故仍保持 C，不升级为 A/B。

### E5 — 2007 用户案例：免费空间持续存在，但产品状态可能反复变化

**等级：C/B-（2008 年站长经验文转载，接近但非严格同时代官方材料）**

2008-07 的站长经验文称作者 2004 年开始建站，第二个网站使用虎翼网免费空间，并留下 `loveqhai.51.net` 这一 locator；文章称该站为全静态，并提到免费空间状态变化。此材料适合作为 locator 与后续 artifact probe 的线索，不用于证明平台整体配置。

来源：
https://www.aspxhome.com/news/2008/4359.htm

## 4. 一个比“免费主页”更准确的对象模型

基于 E1–E4，可以把至少一类 51.net 免费主页建模为：

```text
[author workstation]
  HTML / images / optional media
          |
          | FTP / publishing tool
          v
[hosting account]
          |
          +-- account credentials
          +-- storage quota
          +-- per-file / feature constraints
          v
[/public_html]
          |
          | hostname mapping
          v
[<name>.51.net]
          |
          v
[shared hosting infrastructure]
          |
          v
[visitor browser]
```

这与后来的博客/SNS 有一个根本差别：内容对象首先是**用户部署的文件**，而不是平台数据库中的“文章记录”。因此复原时需要问：

1. HTML 文件是否保存；
2. 同目录图片/MIDI/SWF 是否保存；
3. 文件名大小写是否保持；
4. 相对路径是否保持；
5. 子域 hostname 是否仍可解析；
6. archive 是否把同一 host 下资源一起抓到；
7. 外链资源是否另有 host；
8. 页面是否依赖历史浏览器/插件。

## 5. 对“缺资源”的新解释

E3 的 UNIX/大小写语义值得特别保留。假设历史 HTML 写：

```html
<img src="Images/Logo.gif">
```

而实际文件是：

```text
images/logo.gif
```

在大小写敏感的托管环境中，它可能历史上就失败；现代研究者如果在大小写不敏感的本地文件系统中重放，反而可能“修好”一个历史错误。

因此：

```text
modern local replay succeeds
    !=
historical hosted page necessarily succeeded
```

反过来，archive replay 中缺图也不能自动归因于 crawler 漏抓：可能是原作者未上传、路径大小写错误、资源超限、资源位于外站，或者后来托管配置改变。

这类差异正适合作为 M3 的一个最小实验变量。

## 6. “页面消失”需要继续分层

结合 E1/E2/E3，可以把免费主页可用性至少拆成：

```text
platform exists
  -> new registration allowed
  -> account active
  -> hostname resolves
  -> hosting server available
  -> account file tree retained
  -> HTTP maps host to account
  -> requested file exists
  -> dependent resources exist
  -> browser can render/execute them
```

因此以下等式均不成立：

```text
registration quota reached != old pages deleted
server temporarily offline != account data deleted
domain exists != user page reachable
HTML captured != page experience preserved
subdomain known != historical DNS mapping proven
```

## 7. 建议写入位置

本轮只提交 research note，不直接改 ROADMAP 勾选项。

后续若 artifact probe 成功，建议：

- 将一个非敏感 51.net 个人主页升级为 M1“个人主页/主页托管案例”的候选；
- 在未来 `datasets/sites.csv` 增加或确认：`hosting_provider`、`hostname_pattern`、`upload_method`、`server_os_semantics`、`file_constraints`、`runtime_capabilities`；
- 在 M3 实验中加入“大小写敏感路径 + 相对资源 + 现代本地回放”的对照；
- 在 evidence schema 中区分 `service_policy` 与 `observed_artifact_behavior`。

## 8. 下一步 artifact probe

优先顺序：

1. 查 2002–2004 的 51.net 官方帮助页 capture，给 FTP、`public_html`、200K、UNIX/大小写等规则建立时间下界；
2. 以公开、非敏感 locator（例如 E5 留下的站点）寻找至少两个历史时点；
3. 对同一 capture 记录：原始 URL、capture datetime、HTTP headers、HTML charset/meta、资源 URL、资源成功/失败；
4. 检查页面是否含 MIDI、Flash、JavaScript、FrontPage 生成标记等，但不把缺失资源自动补成“原件”；
5. 若找到 2003 注册页 capture，核对“凌晨 3 点 / 1000 人”的准入规则是否能获得 A 级原始页面支持。

## 9. 缺失证据

目前仍缺：

- 2000–2003 虎翼官方帮助页的可核验 archive capture；
- 免费主页的原始服务条款/配额表；
- 一个已经完成两时点资源清单的非敏感用户主页；
- 历史 HTTP headers 与 charset；
- `*.51.net` 子域映射机制的同期技术文档；
- 免费主页页面是否被平台强制插入广告，以及插入方式；
- 免费服务不同年份的空间大小、单文件限制和流量限制演变。

## 10. 可复原程度

### 已证实

- 2002 年虎翼网存在“虚拟个人主页”；
- 2003 年仍提供免费个人主页注册，并有时段/数量准入规则；
- 51.net 官方现存帮助文档描述了次级域名、FTP、`public_html`、本地编辑再上传、UNIX 大小写敏感等共享主机式工作流；
- 后来用户回忆独立吻合“FTP 空间 + 次级域名 + 静态 HTML”的使用方式。

### 高概率但尚待历史 artifact 固定

- 至少部分 2000 年代早期免费主页采用与现存帮助文档相近的共享主机文件树模型；
- FTP/本地网页工具是重要的作者端发布路径；
- 子域名是用户主页的重要 locator 层。

### 不知道

- 2000/2001/2002/2003 各年份具体配额是否相同；
- 200K 单文件限制从何时开始；
- 服务器 OS/文件系统配置在各年份是否一致；
- 是否、何时强制广告；
- 免费主页关闭/重开各阶段的精确时间线；
- 历史 charset、HTTP header 和浏览器兼容要求。

## 11. 不能声称已经证明的内容

本轮不能声称：

- “虎翼网 2000 年起一直使用完全相同的 UNIX 主机配置”；
- “所有免费主页都是纯静态 HTML”；
- “所有免费用户始终只能上传 200K 以下文件”；
- “51.net 子域今天/后来可解析，所以历史上同一 DNS 映射一直存在”；
- “某 archive 缺图就是 Wayback 抓取失败”；
- “现存官方帮助页就是 2000–2003 年原版帮助页”；
- “已经完成一个 M1 个人主页案例”。

## 12. 隐私与版权边界

- 只选公开历史主页，优先作者主动保留、公开回忆或明确用于展示的 locator；
- 不恢复或重新发布账号密码、FTP 凭据、真实姓名、私人邮箱、电话等个人信息；
- 不尝试登录历史账户，不测试仍有效的凭据；
- 用户 HTML/图片/MIDI/SWF 等仍受原作者版权约束：研究记录 URL、hash、metadata、截图必要局部即可，不批量重新托管；
- 对恶意软件/攻击事件只记录其对托管可用性的证据意义，不保存、运行、传播攻击工具；
- 若 archive 中出现后来主动删除的敏感个人内容，以 provenance 记录代替公开再发布。

## 13. 本轮结论

虎翼网提供了一个重要的纠偏：中文旧网的“免费个人主页”不能只按今天的“个人资料页”理解。至少在 51.net 保存下来的产品语义里，它更接近一个受配额和能力限制的共享虚拟主机账户：用户在本地制作文件，经 FTP/发布工具写入 `public_html`，再通过次级域名被访问。

因此旧网考古不能只保存最终 HTML；**作者端工具、上传协议、服务器文件系统语义、账号配额、hostname 映射与浏览器环境共同构成页面的历史运行条件。**

但由于关键官方帮助页尚未取得 2000–2003 的历史 capture，本 note 只把这一结构作为“已有同期存在证据 + 现存运营方技术文档 + 用户回忆互证”的 bounded reconstruction，不把当前帮助页配置倒填为整个早期时期的既定事实。