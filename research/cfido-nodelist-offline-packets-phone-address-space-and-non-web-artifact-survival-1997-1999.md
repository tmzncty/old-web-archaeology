# CFido nodelist、离线信包、电话号码地址空间与非 Web artifact 存活（1997—1999）

> Research checkpoint，不是完整 case。本仓主对象仍保持约 1995—2015 中文互联网；本文件只把 CFido 放在**直接解释中文 Web/BBS 从哪里长出来**所必需的前史 / 边界位置。它不把 `old-web-archaeology` 改造成全球 FidoNet 史。
>
> 本轮最重要的变化不是再增加一个 `page != transaction`，而是实际检查到一批**有内部日期、节点地址、电话号码、baud/flag 和 message origin 的结构化非 Web 历史 artifact 副本**。这迫使本仓把“旧网 artifact”从 URL / HTML 再向前扩一层。

## 0. 与已有 research note 去重

本仓已经有：

- 拨号 Web 的计费会话与 access-context loss；
- IP 电话、168 IVR、Pager gateway 的跨协议服务拓扑；
- 多个“前台页面 ≠ 后台事务”的状态拆分。

如果本文件只写：

> “CFido 不是 Web。”

没有新增价值。

本轮新增的是四类可以实际编目的考古对象：

```text
Fido node address
telephone dial number
nodelist / diff
message archive / origin line
```

以及一个过渡对象：

```text
Fido nodelist field containing an Internet IP
```

因此研究问题是：

> **当一个数字网络原本不是由 URL、hostname 和 HTTP page 定位时，old-Web archaeology 应该怎样保存它与后来 Web 的接缝？**

---

## 1. Scope boundary：这条前史为什么可以进入 OWA

2024 年 *Isis* 对 CFido 的研究把它的核心历史阶段放在 1991—1998，并指出 dial-up BBS 到 Internet 的转型是 CFido 后期变化的重要背景。

来源：

- Wen-Ching Sung, Chen-Pang Yeang, Zhixiang Cheng, “Demarcating a Pure Land: CFido as a Cyberspace for Computer Amateurs in 1990s China,” *Isis* 115(2), 2024.  
  <https://www.journals.uchicago.edu/doi/10.1086/730229>

本仓不因此向 1991 无限前移。

真正与 1995—2015 中文旧网直接相接的是：

- 1997 年 CFido 自己开始用 `cfido.com` 和 HTML 发行内容；
- Fido 信件与 Internet email / gateway 共存；
- 1998—1999 nodelist 内出现 Internet IP 与电话号码并列；
- 一批后来进入中文 Web / 软件 / IM 环境的人来自这个爱好者网络；
- 同一个《龙音》内容既以 BBS 文本版传播，也以 Web HTML 版传播。

所以这是一份 **boundary archaeology**，不是 scope 重定义。

---

## 2. 本轮实际检查到的 artifact：1996—1999 nodelist 索引

当前 `cfido.com` 仍提供 nodelist 目录：

- <https://www.cfido.com/nodelist/list.html>

目录列出：

- `IMLIST.060`（1996-02-29）；
- 多个 1997 `NODELIST` / diff；
- `MAILRULE.TXT`（目录日期 1998-01-08）；
- 1998 一系列 weekly / periodic nodelist 与 diff；
- `NODELIST.254`（1998-09-11）；
- `NODELIST.099`（1999-04-09）。

目录同时注明 source 为：

- <https://github.com/lshw/cfido_nodelist>

### Evidence classification

这里要拆成三层：

1. **当前目录页**：live legacy Web representation；
2. **GitHub 中的文本文件**：modern preservation copy；
3. **文件内部声称的 1996—1999 operational artifact**：dated historical content。

目前没有原始软盘、原站文件系统镜像、WARC 或签名校验把第 2 层无缝连接回第 3 层。

因此本仓暂定：

- artifact class: `preserved-historical-text-copy`
- evidence grade: **A- candidate / B+**
- confidence: high for “这些文本表示了历史 nodelist/message archive 内容”，lower for byte-identical originality

不能写成：

> “这是从 1998 硬盘原封不动提取的原件。”

---

## 3. `NODELIST.254`：1998-09-11 的地址世界首先由电话号码组成

本轮通过 GitHub connector 实际读取：

- `lshw/cfido_nodelist/NODELIST.254`

文件头内部标明：

```text
A Zone Nodelist for Friday, September 11, 1998
```

并列出 Zone 6 / Region 65 的 CFido 节点。

条目中可观察字段包括：

- `Host` / `Hub` / 普通 node / `Pvt`；
- net / node number；
- station name；
- city；
- sysop；
- telephone number 或 `-Unpublished-`；
- nominal speed / modem flags。

北京、上海、深圳、广州、珠海、杭州等地大量节点的“如何找到这个数字空间”首先是：

```text
Fido address + dial telephone number
```

而不是：

```text
hostname + URL
```

### 新研究单位：`network address surface`

OWA 原有研究单位偏：

- platform；
- site / host；
- account；
- page / URL；
- capture。

CFido 边界要求再增加一种更抽象的历史研究单位：

**`network address surface / 网络寻址表面`**。

可能的 historical locator 包括：

- telephone number；
- Fido `zone:net/node.point`；
- IP；
- hostname；
- URL；
- service code；
- pager number。

不能把 URL 误当成所有数字网络天然的基本单位。

---

## 4. 同一份 nodelist 内已经出现“这不是电话号码，是 Internet IP”

`NODELIST.254` 的广州部分包含 `Electronic_Space` 节点，通常写电话号码的位置出现：

```text
202-116-78-254
```

并附有说明，指出它不是电话号码，而是 Internet IP。

1999-04-09 的 `NODELIST.099` 保存副本中，这一条仍可见。

### 这条 artifact 为什么比一句“CFido 后来接上 Internet”更强

它直接保留了旧数据结构面对新 transport 时的尴尬：

**一个原本主要容纳 dial number 的地址字段，开始被塞入 IP。**

这说明协议转型可以先表现为：

```text
old directory schema
+
new transport locator
```

而不是立刻出现一个全新的 Web database。

本轮暂称：

**`address-space overlap / 地址空间重叠`**。

方法上应记录：

```text
field semantic in old system
!=
value type actually found in late-period artifact
```

这类异常值可能正是平台迁移最有价值的证据。

---

## 5. `MAILRULE.TXT`：message dump 能保存 Web archive 很难保存的运行语境

本轮还实际读取了：

- `lshw/cfido_nodelist/MAILRULE.TXT.utf-8`

其中有多条内部日期为 1997—1998 的 CFido 信区规则 / message records。

例如保存副本中的 1998-01-08 总则 message 带有类似 Fido message header、node address 和 origin 信息；origin 还包含站台电话号码、开放时间窗和 modem speed。

某条 origin 明确呈现：

```text
telephone number
<23:00-07:00 33600bps>
Fido node address
```

这比单独知道“某 BBS 存在”多恢复了三种历史条件：

1. **什么时候可以打进去**；
2. **通过什么电话入口**；
3. **预期连接速度 / modem 能力**。

同一 archive 中 HAM.CHINA 的规则 message 又同时出现 Internet email / HTTP 信息和 `Fido Echomail <--> Internet Gateway` 的 origin 描述，并对 GB 中文 / ASCII 等字符使用做出规则。

### 新 archive 结论：`message metadata is infrastructure evidence`

普通论坛帖的 header 往往被当成“格式噪声”。

但在这种系统里，header / origin 可能直接保存：

- node identity；
- route context；
- phone number；
- availability window；
- baud；
- software chain；
- gateway status；
- charset norm。

所以：

**历史消息的 envelope 也是基础设施史料，不只是正文附件。**

---

## 6. StarStudio：今天的 live page 保存旧操作说明，但不是 historical capture

当前页面：

- <https://cfido.com/starstudio/star.htm>

页面仍说明：

- StarStudio BBS 的 Fido address；
- 上站电话号码；
- BlueWave door / offline reader；
- 下载 packet、断线阅读写作、再上传 reply packet；
- 用户每日 10 / 20 / 30 分钟等级；
- 用户需电脑、modem、外线电话和通讯软件。

它对恢复普通用户 workflow 极有价值。

但必须固定：

```text
current live legacy page
!=
verified historical capture of that page
```

当前能观察到的 HTML、服务器、HTTP header、DOM、charset、JS、resource URL 都不能自动倒推为 1990 年代状态。

页面内容可以证明“今天仍有一份自称保存旧制度的操作说明”，并与 nodelist / message artifact / 1997 刊物互证其制度结构；它本身仍不是 archive memento。

---

## 7. 《龙音》第二期：同一内容同时属于 BBS artifact 与 early Web artifact

当前 `cfido.com/deq.htm` 保存《龙音》第二期，页内明确标为 **1997 年 5 月 9 日出版**。

来源：

- <https://www.cfido.com/deq.htm>

刊物说明：

- 内容主要来自 CFido 信件；
- 有纯文本版和 HTML 版；
- 文本可在 CFido 站台下载；
- HTML 可在 Internet Web 上访问；
- 编辑已使用 Internet email。

因此同一文化对象拥有至少两条传播路径：

```text
CFido message ecosystem
→ text magazine file
→ BBS download
```

和：

```text
same editorial object
→ HTML
→ Web hosting
```

### 新机制：`artifact bifurcation / 作品载体分叉`

早期 Web 内容并不一定“出生在 Web”。

它可能先是：

- 信区 message；
- 文本包；
- 电子杂志；
- BBS 下载文件；

随后才获得 HTML 表示。

如果只保存 HTML，会丢掉它在旧网络中的原始分发链；如果只保存 TXT，又会丢掉它进入 Web 后的浏览环境。

---

## 8. `cfido.com` 的精确 1997 日期目前存在内部冲突

`cfido.com` 当前“国内消息”页写：

- 域名申请于 **1997-04-28**。

来源：

- <https://www.cfido.com/gnxx.htm>

但《龙音》1997-05-09 第二期的同期文本说：

- **1997-05-01**，编辑为 CFido 申请域名并租用美国服务器空间。

来源：

- <https://www.cfido.com/deq.htm>

这两个日期可能分别指：

- registration / application；
- 实际操作 / hosting；
- 文章作者的近似记忆；

目前不能确定。

因此 checkpoint 固定为：

```text
cfido.com existed as a Web boundary object by early May 1997: high confidence
exact application/registration date: unresolved (1997-04-28 vs 1997-05-01 descriptions)
```

这比为了时间线漂亮强行选一个日期更符合 METHOD。

---

## 9. “中国第一个 BBS”是一个 scope-sensitive claim

CERNET 机构史称 1995 年 8 月水木清华为“中国大陆第一个 BBS 站点”或“第一个大型 BBS 站点”。

来源：

- <https://www.cernet.edu.cn/cernet_fu_wu/cernet_news/zui_xin_bo_bao/200603/t20060323_113803.shtml>
- <https://cernet.edu.cn/info/zt/cernet20/talent/cxcy/201411/t20141105_1198982.shtml>

与此同时，CFido 的 dial-up BBS 站台显然在 1995 年以前已经存在。

因此本仓以后遇到“first BBS”必须问：

- first dial-up BBS？
- first Fido node？
- first Internet-connected BBS？
- first CERNET BBS？
- first large public campus BBS？

本轮固定：

**`firstness requires protocol scope / 第一必须绑定协议范围`**。

不要为了一个“第一”把不同网络系统压成同一种对象。

---

## 10. 海外对照：Fido 的成本与 store-and-forward 是全球共同结构

1993 年 *Washington Post* 的同期报道描述美国 FidoNet：早期设计会在夜间较低电话费时拨号交换消息；节点由爱好者协作承担费用；direct netmail 更快但可能需要承担长途费，routed mail 更慢但便宜。

来源：

- <https://www.washingtonpost.com/archive/business/1993/07/19/fidonet-enthusiasts-share-a-low-cost-way-to-communicate/eaf20b43-5c52-4663-82c4-c22c48ba5ca8/>

Internet Hall of Fame 对 Karen Banks 的资料则记录，1990—1997 年 GreenNet 的 GnFido gateway 使用 FidoNet / UUCP store-and-forward，连接非洲、南亚和东欧 60 多个伙伴，在很多地点成为 NGO、研究者和机构获得低成本电子通信的重要手段。

来源：

- <https://www.internethalloffame.org/inductee/karen-banks/>

所以：

**store-and-forward、间歇拨号和成本感知路由并非中国特殊。**

中国 OWA 更值得记录的是这些全球机制进入中文编码、国内电话区号、国产软件/爱好者文化以后形成的具体 artifact。

---

## 11. 新的 archive failure / survival 模型

### 11.1 `URL-centric archive bias / URL 中心的档案偏差`

如果研究工具只会问：

> “这个 URL 在 Wayback 里有没有？”

那么 1990 年代早期数字网络会被系统性低估。

因为历史入口可能是：

```text
0599-5832832
6:657/901
CHAT.CHINA
STUDIO.###
```

它们都不是 URL。

### 11.2 `non-Web operational artifact survival / 非 Web 运行 artifact 存活`

一个网络可能没有保存下来的网页，却留下：

- nodelist；
- weekly diff；
- message dump；
- origin line；
- offline mail packet；
- BBS software / mailer config；
- modem / dial instructions。

这些 artifact 对“系统怎样实际工作”甚至可能比宣传首页更强。

### 11.3 `replicated-text survivorship / 复制型文本的幸存优势`

Fido 的 nodelist、echomail、mail rules 天生就是要被复制到多个节点的文本对象。

研究假说：

> **本来为了分布式运行而反复复制的结构化文本，可能比依赖单一早期 Web host 的页面拥有更高的后世幸存概率。**

当前只有 CFido 一个案例，尚不能当成普遍定律；以后可与 Usenet spool、mailing-list archives、FTP mirrors 比较。

### 11.4 `preservation copy != original transport artifact`

现代 GitHub 中的 `NODELIST.254` 即使内容可信，也不能证明：

- 文件 byte-for-byte 未变化；
- newline / encoding 未转换；
- 时间戳来自原文件系统；
- 它就是某一具体站台当时实际载入的副本。

因此 provenance 必须保留“现代保存层”。

---

## 12. 对 evidence schema 的建议字段：支持非 Web 网络 artifact

不改主 METHOD，只在本 checkpoint 提供可复用字段建议：

```yaml
artifact_kind: nodelist | message-dump | mail-packet | bbs-manual | web-page
artifact_internal_date: 1998-09-11
preservation_copy_observed_at: 2026-09-13
preservation_host: github
historical_network: CFido
network_address: "6:655/403"
dial_number: "..."
ip_locator: null
baud_or_speed: "33600bps"
availability_window: "23:00-07:00"
transport: pstn-modem | internet-ip | unknown
encoding_rule: GB/ASCII | unknown
gateway_to: internet | null
original_media_provenance: unknown
byte_identity_verified: false
```

目的不是把所有 artifact 塞进网页 schema，而是防止非 Web 证据在 catalog 时被迫伪装成 URL。

---

## 13. 本轮“已证实 / 高概率 / 不知道”

### 已证实 / strong

- 当前 `cfido.com` nodelist index 暴露 1996—1999 dated list/diff filenames，并指向现代 GitHub preservation repo；
- 本轮实际读取到内部日期 1998-09-11 的 `NODELIST.254` 和 1999-04-09 的 `NODELIST.099` preserved copies；
- preserved nodelist 中大量节点以电话号码作为 locator，并同时携带 Fido node address；
- 广州 `Electronic_Space` 条目以 Internet IP 出现在通常承载电话号码的字段，并明确说明是 IP；
- `MAILRULE` preserved copy 内有 1997—1998 message metadata、Fido origin、站台开放时段 / baud 等运行痕迹；
- 1997《龙音》明确把同一刊物作为 CFido 文本版和 Internet HTML 版发行；
- 当前 StarStudio legacy page 明确描述 BlueWave offline packet workflow。

### 高概率 / inference

- 1997—1999 CFido 正处在“电话/Fido address 与 Internet/IP/Web address 重叠”的过渡带；
- 结构化 nodelist/message metadata 对复原运行拓扑比单纯截图具有更高价值；
- 很多 early-Web 人物和内容的 Web 形态之前存在 BBS/text-file 前身。

### 不知道

- GitHub preservation copy 与最初发布文件是否 byte-identical；
- `NODELIST.254` 中每个电话号码在 1998-09-11 是否实际可拨通；
- `Electronic_Space` 的 IP transport 具体使用何种 Fido-over-IP 软件/协议；
- StarStudio 当前页面与 1997/1998 原 HTML 的 DOM / charset / script 差异；
- `cfido.com` 1997-04-28 与 1997-05-01 日期差异的准确解释；
- earliest `cfido.com` historical capture 是否能达到 METHOD 的 capture contract；
- BlueWave packet 原文件是否仍有带来源链的保存副本。

---

## 14. M1 状态：这次拿到了更像“artifact”的东西，但仍不是完整 Web case

过去多轮研究常见状态是：

> contemporaneous description exists, historical interface artifact not obtained.

本轮不同：

**实际检查到了 dated structured operational-artifact copies。**

这是证据质量上的实质推进。

但 M1 的完整 case 要求仍包括：

- 明确对象身份；
- ≥2 historical time points；
- 尽可能 ≥2 independent evidence sources；
- 资源缺失；
- browser / encoding assumptions；
- historical page / capture provenance；
- recollection vs contemporaneous comparison。

当前仍没有把 `cfido.com` / StarStudio 做成合格的 historical Web capture case。

因此严格记录：

**`M1 historical CFido Web case: NOT ACHIEVED IN THIS SLICE.`**

同时另记：

**`dated non-Web operational artifacts: ACHIEVED AS PRESERVATION COPIES, provenance chain incomplete.`**

---

## 15. 下一步最值钱的不是再写一篇回忆史

优先级：

1. 找到并实际打开 `cfido.com` 1997—2000 至少两个 historical Web captures；
2. 记录 original URL、capture datetime、HTTP/replay、charset、DOM、图片/MIDI/链接缺失；
3. 找 StarStudio 旧 capture，与今天 live legacy page 做逐字段差分；
4. 获取一份有明确 provenance 的 BlueWave packet（如 `.###` / reply packet）并只做 metadata / format 研究；
5. 找 Fido ↔ Internet gateway 的当年软件、配置或手册；
6. 查 `Electronic_Space` IP 节点的具体 transport；
7. 为 nodelist / message-dump 设计 evidence fixture，验证非 Web artifact 是否应进入正式 schema；
8. 与 Usenet spool / mailing-list archive 做一个跨国 artifact-survival 比较。

---

## 16. 与 how-people-lived 的交叉链接

普通生活侧详细讨论：

- offline-first networked sociality；
- daily minute quota；
- shared-line time commons；
- tariff-shaped network geography；
- 1997 同期使用者怎样同时使用 CFido 和 Internet；
- BBS 与 Internet BBS 的边界。

见：

- `tmzncty/how-people-lived/sources/cfido-offline-first-bbs-store-and-forward-and-scarce-online-minutes-china-1991-1999.zh-CN.md`

本仓只保留与 **artifact、address surface、保存偏差、协议接缝和 historical Web boundary** 直接有关的部分。
