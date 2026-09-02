# PRE_WEB_NETWORK_ARTIFACT_MIGRATION_CFIDO_1991_1998.md

## 目的

本文件不是把 `old-web-archaeology` 的主 scope 前移到 1991 年，也不是把仓库改造成全球 BBS/FidoNet 史。

它只处理一个对 **1995–2015 中文旧网考古直接必要** 的边界问题：

> **1990 年代后半的中文 Web 页面里，有多少内容并不是“出生在 Web”，而是从更早的拨号 BBS、FidoNet 信区、纯文本电子杂志、离线文件包迁移过来的？**

CFido / 《龙音》提供了一个非常清楚的案例。

---

## 1. 关键事实：1997 年的 Web artifact 可以拥有 pre-Web origin

中国惠多网电子杂志《龙音》第二期标明 **1997-05-09** 出版。其刊首记录：

- 1997-05-01 为 CFido 申请了 `cfido.com`；
- 杂志曾先借放在《计算机世界报》主页；
- 杂志内容“基本取材自 cfidonet 上的信件”；
- 杂志同时有**纯文本与 HTML 两种版本**；
- 读者可以在 CFido 站台下载，也可以通过 Internet URL 获取。

幸存页面：
https://www.cfido.com/deq.htm

这构成一个明确的 artifact lineage：

```text
CFido / BBS 原始信件
        ↓
编辑选择 / 编排
        ↓
《龙音》电子杂志
        ↓
纯文本版 + HTML 版
        ↓
借放第三方主页 / cfido.com
        ↓
后续幸存页面、镜像或 archive capture
```

因此：

> **archived web page ≠ web-native historical content**

一个 HTML 页面可以是更早网络文化的迁移层，而不是内容的最初发生现场。

---

## 2. 四个时间必须拆开

遇到这种材料时，至少记录：

```yaml
content_origin_time:        # 原始信件/讨论何时产生
editorial_compilation_time: # 何时被选入电子杂志
web_publication_time:       # HTML/Web 版本何时发布
archive_capture_time:       # 档案系统何时抓取当前版本
```

如果只有其中两个时间，不得自动补全另外两个。

### 例子

《龙音》第二期内部有一篇音乐文章署 **1997-04-20 北京**，杂志本期出版日期为 **1997-05-09**，而 `cfido.com` 域名据刊首称在 **1997-05-01** 取得。

所以即使后来 archive 保存的是 `cfido.com/deq.htm`，至少存在三个不同历史时点：

```text
article composition
→ issue compilation/publication
→ web-host publication / later capture
```

不要把 capture datetime 当成文章写作时间，也不要把 HTML 页面存在时间当成信区讨论首次发生时间。

---

## 3. “页面内容”与“原始社区上下文”必须分开

《龙音》自己说明内容基本取自 CFido 信件。

但编辑后的电子杂志与原始信区并不等价。

可能发生：

- 选稿；
- 删除上下文；
- 标题重写；
- 拼写/编码处理；
- 由纯文本转为 HTML；
- 给作者补充 Internet e-mail；
- 添加编辑注；
- 把站内缩写解释给更广泛读者；
- 将原本分散于多站点的讨论重新组织成一期刊物。

因此：

> **edited electronic magazine ≠ raw BBS corpus**

即使内容本身是同时代的，也不能从电子杂志反向恢复整个原始讨论串。

### 推荐证据字段

```yaml
artifact_type: electronic-magazine-html
content_origin_system: cfido
content_origin_type: echomail-or-bbs-letter
editorial_selection: true
raw_thread_available: unknown
web_native: false
transformation_chain:
  - bbs-message
  - magazine-selection
  - text/html-edition
  - web-publication
```

---

## 4. CFido 本身不是 Web，也不要因为后来有网站而改写技术史

《龙音》1997 年技术文章对 CFido 的运行方式有同时代说明：

- 用户通过公共电话网 + modem 拨号进入 BBS；
- 一条电话线通常一次只能服务一个用户；
- 站点间不要求持续互联；
- 各站在特定时间拨号交换信包，文章称一般每日一次；
- echomail 通过各站转信扩散；
- netmail 可以沿网络路由逐级传送；
- 网络拓扑和转信时段明显受电话费用约束。

来源同上：
https://www.cfido.com/deq.htm

因此当后来的 `cfido.com` 页面说“CFido 网络”时，研究对象仍应分成：

```text
CFido protocol / dial-up BBS network
CFido community
Dragon Voice publication
cfido.com web host
later surviving/archive artifact
```

不要把它们合成一个模糊的“网站”。

---

## 5. 这正好解释为什么 1994 边界需要谨慎

CNNIC/CERNET 的中国互联网发展大事记保存了另一个必要的边界：

- 1987：CANET 已实现国际电子邮件；
- 1988–1993：存在 X.25、X.400、DECnet、科研网、部分国际邮件/专线；
- 1993：数百名科研人员可通过高能所链路使用电子邮件；
- 1994-04-20：NCFC 实现全功能 Internet 国际连接；
- 1995-01：开始通过电话网、DDN、X.25 等方式向社会提供 Internet 接入；
- 1996-01：CHINANET 全国骨干网正式开通。

来源：
https://www.cernet.edu.cn/ke_yan_yu_fa_zhan/gai_kuang/xin_wen_gong_gao/200603/t20060323_78013.shtml

所以旧网研究里至少不要写：

> “1994 年以前中国没有网络。”

但本仓也不应该据此把 1980s 科研网络全面纳入主 scope。

正确边界是：

> **当 1995–2015 中文 Web artifact 的技术、社区或内容来源明显继承自 1995 年以前的系统时，允许写必要的 prehistory note；完整的全球/中国互联网前史仍属于其他研究项目。**

相关生活史主文档：
https://github.com/tmzncty/how-people-lived/blob/main/topics/layered-network-access-and-batch-sociality-china-1987-1997.zh-CN.md

---

## 6. 一个新的考古问题：migration layer

以后看到旧网页时，除了问“这个页面什么时候上线”，还要问：

> **它是不是某种更早媒介的迁移层？**

候选来源包括：

- FidoNet / CFido echomail；
- 单站 BBS 帖子；
- Usenet / mailing list；
- 纯文本电子杂志；
- FTP 文件说明；
- 软件 README / FILE_ID.DIZ；
- 光盘/磁盘电子出版物；
- 报纸和纸质杂志转贴；
- 校园网内部资料；
- 电话/BP 机联系人目录的 Web 重排。

### 推荐字段

```yaml
migration_layer:
  is_migrated: true
  origin_medium: dialup-bbs
  origin_platform: cfido
  origin_date: unknown
  web_publication_date: 1997-05
  transformation: editorial-compilation-and-html
  raw_origin_preserved: unknown
```

---

## 7. 为什么这种迁移会制造 archive bias

Web archive 更容易保存：

- HTML 版电子杂志；
- 首页、目录和经过编辑的文章；
- 有固定 URL 的作品；
- 被后来网站继续托管的精选内容。

它更难保存：

- 原始 BBS 的完整信区；
- 未被编辑选中的普通帖子；
- 私人 netmail；
- 本地站台短期内容；
- 拨号过程、离线阅读包和本地用户数据库；
- 没有迁移到 Web 的失败、闲聊与普通日常。

因此：

> **web survival can overrepresent what was selected for migration.**

一个电子杂志留存了恋爱、技术、音乐、软件等文章，并不能证明这些主题就是原始 CFido 讨论的比例结构。

我们只知道：编辑认为它们值得在某一期被选出来并继续传播。

---

## 8. “幸存原件”也要记录 hosting continuity

当前 `cfido.com` 自述网站保留了早期页面风格，同时目录中仍能看到 1996–1999 的 nodelist / mailrule 文件：

https://www.cfido.com/nodelist/list.html

但当前可访问 ≠ 已证明从 1990s 到今天 URL、文件、字节内容完全连续。

在没有 Wayback/WARC/hash 比较前，建议记录：

```yaml
surviving_copy: true
historical_internal_date: 1997-05-09
current_host: cfido.com
hosting_continuity_verified: false
byte_identity_verified: false
```

这可以避免把“当前站点保存了一份老材料”错误升级成“这是未经迁移的原始 1997 HTTP 对象”。

---

## 9. nodelist 是另一种 artifact，不要按网页逻辑解读

当前 CFido 站点索引列出：

- `IMLIST.060` — 1996-02-29；
- `NODELIST.234` — 1997-08-22；
- 多份 1997–1998 `NODELIST.*` 与 diff；
- `MAILRULE.TXT` — 1998-01-08。

索引：
https://www.cfido.com/nodelist/list.html

这些文件如果后续完成内容验证，可以用于：

- 节点地址；
- 系统名；
- 地理位置；
- 电话/modem 标记；
- 网络拓扑；
- 节点新增/删除；
- 技术规则。

但它们不能直接证明：

- 每个节点当日实际在线；
- 普通用户数量；
- 某个信区的活跃程度；
- 某个人真实拨号访问过该节点。

即：

> **listed node ≠ reachable node ≠ active community ≠ observed user visit**

后续如果纳入正式 case，应逐文件检查 provenance，而不是只引用目录页。

---

## 10. 海外对照：FidoNet 的成本结构是共同机制

1993 年 *Washington Post* 同时代报道把美国 FidoNet 描述为由 BBS 爱好者合作维护的低成本网络，当时节点数已超过 25,000；地区节点共同承担长途电话成本，一些 BBS 免费，另一些收较低年费。

https://www.washingtonpost.com/archive/business/1993/07/19/fidonet-enthusiasts-share-a-low-cost-way-to-communicate/eaf20b43-5c52-4663-82c4-c22c48ba5ca8/

1989 年 FidoNews 同时代文章直接把 message size、baud rate 与长途电话费放在同一成本模型中：
https://www.fidonews.site/1989/v06n22/

这说明：

- 批量转信；
- 固定 mail hour；
- 压缩；
- 离线读写；
- 分层路由；

都不是中国特有现象。

中国案例要另外解释的是电话/PC 可及性、中文系统、区域电信条件以及 1994–1998 与公共 Internet 快速重叠的具体历史环境。

---

## 11. 证据等级

### A — 同时代历史材料

**《龙音》第二期（1997-05-09）**

用途：

- 证明刊物当时如何自我描述发行方式；
- 证明 CFido 技术文章对拨号、转信、电话成本、echomail/netmail 的同期理解；
- 证明 BBS 信件被编辑后迁移为 text/HTML/Web；
- 证明部分内容主题超出纯技术。

限制：

- 当前 host continuity 尚未独立验证；
- 编辑选刊不能代表原始信区总体分布；
- 文章对 FidoNet 全球早史中的细节仍应与独立技术史料交叉。

**FidoNews 1989**

用途：全球 FidoNet 电话成本/baud-rate 约束的同时代佐证。

### B — 近同时代二手证据

**Washington Post 1993**：海外 FidoNet 使用与成本结构。

### B+ — 后来机构历史汇编

**CNNIC/CERNET 2003 大事记**：1987–1996 中国机构网络、全功能连接、公共接入时间线。

### Scholarly reconstruction

Sung, Yeang, Cheng, *Isis* 2024：CFido 1991–1998 的研究史定位。
https://www.journals.uchicago.edu/doi/10.1086/730229

---

## 12. 后见之明与复原风险

### 风险 A：把 CFido 写成“中国早期网站”

错误。CFido 核心是电话线拨号 BBS / FidoNet 式转信网络；后来出现 Web host 是迁移阶段。

### 风险 B：把 1997 HTML 当成原始讨论线程

错误。电子杂志已经经过编辑选择和媒介转换。

### 风险 C：因为后来参与者成名而只保存“名人史”

这会把普通站友、无名用户和未迁移内容再次抹除。

### 风险 D：把 archive 的时间戳当作内容产生时间

必须拆 `origin / compilation / publication / capture`。

### 风险 E：把 1994 之前写成空白

这会看不懂为什么一些 1995–1997 Web 站点一上线就已经拥有现成社群、昵称、文本库、技术习惯和关系网络。

---

## 13. 它改变了旧网考古的哪一点？

此前一个默认模型可能是：

```text
site created
→ users arrive
→ content accumulates
→ archive captures site
```

CFido 案例要求增加另一条：

```text
pre-web community exists
→ messages/files/social norms accumulate elsewhere
→ selected artifacts migrate into web
→ web site appears already carrying history
→ archive captures only the migrated layer
```

所以：

> **a site's first web capture may be the middle of a community history, not its beginning.**

这条规则对 1995–2000 的中文 BBS、软件站、电子杂志、个人主页、校园网络和门户早期栏目尤其重要。

---

## 14. 尚未确定

- `cfido.com/deq.htm` 当前文件与 1997/2000 历史 HTTP 文件是否字节一致；
- 《龙音》纯文本版是否还能从独立 archive 找到；
- 第二期各文章对应的原始 CFido 信区/信件是否仍可定位；
- 当前 nodelist 文件的原始来源、完整性和转码过程；
- 有多少 1995–2000 中文 Web 站点具有类似“BBS/FTP/电子杂志 → Web”的迁移谱系。

在这些问题解决以前，保持 `surviving-copy / migrated-artifact / provenance-partial` 标记比写一个无缝连续的“站史”更可靠。
