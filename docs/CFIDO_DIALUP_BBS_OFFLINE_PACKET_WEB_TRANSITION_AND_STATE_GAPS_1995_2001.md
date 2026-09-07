# CFido 拨号 BBS、离线信包、Web 迁移与状态缺口（1995—2001）

> Scope：本文件只研究约 1995—2001 年中文旧 Web 与 CFido / dial-up BBS 的交界：拨号站台如何被 Web 页面描述、BBS 内容如何迁到 HTML、Internet email / OICQ / 流媒体怎样叠到旧网络外面，以及今天残存的 legacy pages 究竟能证明什么。
>
> 中国 1986—1994 的科研邮件、CFido 1991 起的普通技术生活前史、跨国 FidoNet 比较与“网络存在 ≠ 大众可及”的生活史问题，写入 `tmzncty/how-people-lived/topics/cfido-dialup-bbs-offline-reading-and-network-before-mass-internet-china-1986-2001.zh-CN.md`。本文件不把 `old-web-archaeology` 扩成全球 FidoNet 史。

本题要修正一个很常见的 old-Web 误差：

> **今天能打开一张讲 1990 年代 BBS 的 HTML 页面，不等于我们已经恢复了当年的 BBS；而一份 BBS 信件被 1997 年 HTML 杂志重新发布，也不等于原信区的楼层、转信路径、时间与用户界面仍然存在。**

---

## 1. 研究单位：至少拆成十二层

不要把 `CFido`、`BBS`、`cfido.com` 和一份当前网页当成同一个对象。

至少区分：

1. **FidoNet / CFido network**：节点与转信规则组成的网络；
2. **region / net / node**：例如 Region 65、具体 net 和 node address；
3. **physical BBS station**：一台或多台电脑、modem、电话线；
4. **dial-up telephone number**；
5. **BBS software / mailer / door**；
6. **local user account / level / minutes / credits**；
7. **message area**：Localmail、Echomail、Netmail、PVT 等；
8. **offline packet**：例如 BlueWave 下载 / 上传信包；
9. **inter-node mail route / toss / forward state**；
10. **WWW site / HTML magazine / Internet email**；
11. **current legacy page carrying historical text/code**；
12. **verified historical capture / WARC / original artifact**。

因此固定：

```text
node listed ≠ node reachable
phone answers ≠ BBS session established
BBS login ≠ enough time/permission to read national echoes
downloaded packet ≠ message read
reply written offline ≠ reply uploaded
reply uploaded ≠ remote node received it
historical text visible on current Web ≠ original BBS context survives
current legacy renderer ≠ verified 1997/2000 browser experience
```

---

## 2. 基础状态机：一条 CFido 发言真正抵达远端用户，比“发帖”长得多

StarStudio 当前 legacy page 承载的历史操作说明允许恢复一个最小状态机：

```text
现实用户
→ 有电脑 + modem + 可拨外线电话 + 通讯软件
→ 拨 BBS 电话号
→ modem / line 建链
→ BBS 接听
→ 本地账号认证
→ 用户级别 / 当日分钟数有效
→ 进入 BlueWave door
→ BBS 将订阅信区打包
→ 下载 STUDIO.###
→ 用户挂断
→ 离线阅读 / 写回复
→ 本地生成 STUDIO.NEW
→ 下次拨号
→ 上传 STUDIO.NEW
→ BBS 接收并整理
→ 本地信区可见，或进入 Echomail 转发
→ mailer 按路由向其他节点转信
→ 远端 BBS 接收 / toss
→ 远端用户下一次拨入或下载信包
→ 实际读到
```

来源（current live legacy page；不是本轮验证的历史 capture）：

- <https://www.cfido.com/starstudio/star.htm>

这条状态链说明：

> `message timestamp ≠ recipient-read timestamp`。

对于 store-and-forward 网络，**发送、站台接收、跨节点转发、远端落地和最终阅读本来就是不同时间。**

因此加入 **message-time / delivery-time / read-time gap**。

---

## 3. 单线 BBS 会主动制造“离线优先”的用户界面

StarStudio 页面说明，大多数 Fido BBS 由爱好者在家架设，常见为单线系统；为了节省站台时间资源，站台不鼓励在线读写，而推荐 BlueWave offline reader。

页面列出的用户等级还把每日使用时间写成不同分钟数，例如新用户约 10 分钟、正式用户约 20 分钟、进阶用户约 30 分钟。

来源：

- <https://www.cfido.com/starstudio/star.htm>

这带来一个 old-Web / old-network 都应复用的概念：**scarcity-shaped UI / 稀缺塑造 UI**。

今天保存下来的 HTML 帮助页可以告诉我们“离线阅读存在”，但它仍然不能恢复：

- 当时拨一次需要重拨多少次；
- 热门站占线多久；
- modem 握手失败率；
- 每个用户真实花了多少电话费；
- 20 分钟限制是硬切断、警告还是软规则；
- BlueWave packet 实际编码、压缩与中文显示环境；
- 用户是否真的按照教程离线阅读。

因此：

`help page says workflow exists ≠ workflow executed successfully`。

---

## 4. 当前 StarStudio 页面保存了一个很有价值、但必须谨慎处理的浏览器分支

当前可取到的 StarStudio HTML 页面底部仍暴露一段 JavaScript：它检查 `navigator.userAgent` 是否包含 `MSIE`，如果是则写入 `<bgsound>`，否则写入 `<embed ...>` 来播放 MIDI。

当前 legacy artifact：

- <https://www.cfido.com/starstudio/star.htm>

这对 M3 浏览环境研究很有价值，因为它直接给出一个 **browser-dependent rendering branch / 浏览器依赖渲染分支**：

```text
MSIE branch → bgsound
non-MSIE branch → embed
```

但本轮**不能**写：

> “1997 年 StarStudio 一定就是用这段 JavaScript。”

原因是当前页面本身不是已验证的 1997 capture。我们知道的是：

> **当前 legacy page 保存了一段明显属于旧浏览器时代的 user-agent 分支；其具体历史出现时间仍需 archive capture 或原始介质确认。**

同样，CFido 首页当前还写有“建议 IE4.0 以上、800×600 全屏观看”，并自称最后更新时间 2001-10-17、保留约 2000 年时的样子：

- <https://cfido.com/>

这是一条重要的**site self-description**，不是历史 capture 的替代物。

---

## 5. 1997《龙音》是一个非常清楚的 BBS → Web 再发布链

当前保存的《龙音》第二期把自身日期标为 1997-05-09，并记录：

- 杂志内容基本取材自 CFido 信件；
- 杂志有纯文本和 HTML 两种版本；
- 纯文本 / HTML 可在 CFido 站台发行 / 下载；
- 杂志一度借放在《计算机世界报》主页；
- 1997 年 5 月初取得 `cfido.com` 与服务器空间；
- Internet 用户可通过 Web URL 访问；
- 反馈又可以通过 Internet email 返回。

当前 legacy page carrying dated historical content：

- <https://www.cfido.com/deq.htm>

这里加入 **BBS-to-Web republication chain / BBS—Web 再发布链**：

```text
原始 CFido message
→ 被编辑选中
→ 进入电子杂志
→ 纯文本版本
→ HTML 版本
→ Web host
→ 今天 current legacy page
```

每一次转换都可能丢状态。

### 5.1 `article survives ≠ source message survives`

今天我们可以读到《龙音》的文章，却未必还能恢复：

- 原始 Echomail area；
- 原 message ID；
- 发信 / 转信 / 收信时间；
- 前后回复；
- 原作者本地 BBS 账号状态；
- 编辑删节；
- 该篇从哪个 node 进入编辑流程；
- 纯文本版和 HTML 版之间是否完全一致。

这叫 **republication provenance gap / 再发布来源链缺口**。

### 5.2 Web 让文本更可见，却可能让原网络结构更不可见

一篇信件被抽出信区、变成独立文章后，后来的历史读者更容易阅读正文，却更难知道它原本嵌在怎样的多人对话里。

因此：

> **可读性上升并不等于上下文保存度上升。**

---

## 6. `cfido.com` 的出现不是“CFido 变成网站”，而是多套协议开始叠层

当前“国内消息”页把 `cfido.com` 域名申请日期写为 1997-04-28，并说明由 StarStudio 站长申请虚拟主机，用于向 Internet 用户介绍 CFido。

来源：

- <https://www.cfido.com/gnxx.htm>

《龙音》第二期又描述同一转变：CFido 内容在站台和 WWW 两边同时发行。

到当前保留的旧首页，外围层里又能看到：

- OICQ；
- RealPlayer 网络直播；
- WWW 外链；
- 网上商店 / 信息港等 Web 对象。

来源：

- <https://cfido.com/oldindex.htm>

所以旧网谱系不要写成：

```text
BBS died
→ Web replaced it
```

更可靠的是：

```text
拨号 BBS / Fido mail
→ + Internet email
→ + WWW / HTML magazine
→ + OICQ
→ + streaming media / Web services
```

这里加入 **protocol-layer overlap / 协议层重叠**。

一个 1998—2000 左右的使用者可能同时属于多个层，而不是“从旧时代整个人迁入新时代”。

---

## 7. nodelist 是非常强的拓扑证据，也有很明确的 state gap

当前 `cfido.com` nodelist index 列出一系列历史文件，例如：

- `NODELIST.234` — 1997-08-22；
- `NODELIST.304` — 1997-10-31；
- 1998 年多份连续周度 nodelist / diff；
- `MAILRULE.TXT` — 1998-01-08。

来源：

- <https://www.cfido.com/nodelist/list.html>
- 后来保存来源：<https://github.com/lshw/cfido_nodelist>

`NODELIST.304` 的文件头自标为 1997-10-31，并列出 Region 65 / Mainland China 下多个 net、hub、node、电话号、modem flags 与 sysop 名。

这类 artifact 适合支持：

- 节点地址结构确实存在；
- 网络具有明确的地域 / 拨号拓扑；
- 电话号码和 modem capability 是路由 / 可达性的一部分；
- 节点列表会按日期更新。

但不能直接支持：

```text
listed on that date = actually dialable at every moment
listed node = ordinary users successfully logged in
phone number = same physical machine throughout period
nodelist copy today = bit-identical original distribution artifact
```

因此加入 **nodelist-to-live-node gap / 节点表—实际在线节点缺口**。

当前 GitHub 副本属于后来保存的历史文件；其 provenance 需要继续记录，不能冒充本轮从 1997 介质取得的原始盘片或 archive capture。

---

## 8. 一个拨号号码在 archive 中消失，会让整个生活流程一起消失

Web archaeology 常优先看 URL，但 CFido 提醒我们：1990s 网络对象的核心 locator 可能首先是**电话号码**。

当年用户入口可以写成：

```text
0599-5832832
```

而不是：

```text
https://...
```

因此 old-Web 的前史 / 边界说明需要允许这些 locator：

- telephone number；
- Fido address，如 `6:657/901`；
- nodelist entry；
- BBS name；
- Echomail area；
- packet filename；
- later Web URL。

这里加入 **locator-regime transition / 定位符制度转换**：

> 从电话号码 / node address 找人和服务，逐步转向 URL / email / IM account。

如果只搜索历史 URL，研究者会系统性漏掉 Web 之前以及 Web 早期仍依赖 dial-up locator 的活动。

---

## 9. 身份状态：local BBS account、Fido persona 和 Web identity 不能压成一个 username

StarStudio 页面显示：新用户通过本地 BBS 注册，升级要求资料较完整、包括中文名，并使用 ID 参与不同信区。

这至少存在：

```text
现实人
→ 本地注册资料
→ local BBS account / ID
→ user level / daily minutes
→ local / national message areas
→ 可能出现 email address
→ 可能进入 Web / OICQ identity
```

因此加入 **local-account-to-network-persona gap / 本地账号—网络人格缺口**。

我们目前不知道：

- 同一 ID 在不同站是否唯一；
- 注册资料是否可被其他站验证；
- node 间转信是否总能稳定保留 persona；
- 后来的 Web email / OICQ 是否与旧 BBS ID 对应；
- 当前页面显示的人名 / 邮箱在何时第一次出现。

不要把今天常见的“一个平台账号贯穿所有服务”模型投射回去。

---

## 10. old-Web archaeology 需要新增的核心 state gaps

### 10.1 line-availability gap

`电话号码存在 ≠ 拨得通`。单线站台可能正在服务别人，线路可能忙、断、停机或在 mail hour 中服务节点转信。

### 10.2 handshake-to-session gap

`modem 接通 ≠ BBS session 成功`。调制解调器能力、线路质量、终端设置和 BBS 软件都可能失败。

### 10.3 session-to-permission gap

`登录成功 ≠ 能读全国信区`。用户级别、当日分钟、信用点和规则会限制能力。

### 10.4 packet-download-to-reading gap

`STUDIO.### 下载成功 ≠ 用户实际读完`。

### 10.5 offline-reply-to-network gap

`本地写好回复 ≠ 上传 ≠ 本地站接受 ≠ 全国转信成功`。

### 10.6 message-time / delivery-time / read-time gap

store-and-forward 不能用一个帖子时间戳替代整个传播时间链。

### 10.7 nodelist-to-live-node gap

节点表是拓扑声明，不是 uptime 日志。

### 10.8 BBS-message-to-Web-article gap

HTML 杂志可能保存正文，却丢掉原信区、回复、message ID 和转信路径。

### 10.9 current-legacy-code-to-historical-code gap

今天页面里残存的 IE / `<bgsound>` / `<embed>` 分支很有价值，但没有 capture 就不能自动定年。

### 10.10 dialup-locator-to-Web-locator gap

电话号、Fido address、email、URL、OICQ 号会在同一社群中接续 / 并存。

---

## 11. Browser / encoding / media assumptions

本轮可以直接观察到的 current legacy artifacts 包括：

- `cfido.com` 自述推荐 IE4.0+、800×600；
- StarStudio current page 残存 MSIE user-agent 分支；
- MIDI 背景音乐使用 `<bgsound>` / `<embed>` 不同路径；
- `oldindex.htm` 仍保存 RealPlayer `pnm://.../live.rm` 形式的直播 locator；
- 页面存在大量已经属于历史 Web 生态的外链。

这些信息提示未来 M3 至少应测试：

- IE4 / IE5 / IE6 级环境；
- Netscape / 非 MSIE 分支；
- MIDI playback；
- `<bgsound>` 与 `<embed>` 行为；
- 800×600 viewport；
- GB2312 / GBK / 当前服务器实际 charset；
- RealPlayer / `pnm://` 协议不可用时页面怎样退化。

但现在仍不能说“2000 年用户一定看到当前呈现”。

---

## 12. Evidence ledger

| Claim | Evidence | Grade / confidence | 限制 |
|---|---|---|---|
| CFido 1991 起活动、1991—1998 是关键时期 | 2024 *Isis* 研究 | B / high | 后来学术重构，不是当时页面 |
| 1994-04-20 全功能 Internet，1995/1996 公用服务扩展 | CNNIC 历史整理 | B / high | 机构后期整理 |
| StarStudio 需要电脑/modem/电话/通信软件 | current StarStudio legacy page | A-content? / medium-high | 当前容器，不是 verified historical capture |
| BlueWave 用离线信包节省电话费 / 上站时间 | 同上 | A-content? / high for page claim | 实际用户执行率未知 |
| 不同用户等级对应分钟数 | 同上 | A-content? / high for page claim | 历史时点仍待 archive 定年 |
| 《龙音》第二期标 1997-05-09，并同时通过 CFido + WWW / email 分发 | current `deq.htm` carrying dated text | A-content? / medium-high | 原始 1997 HTTP capture 未验证 |
| `cfido.com` 域名 / Web host 进入社群 | `deq.htm` + `gnxx.htm` | two related platform evidence items / medium-high | 同一 evidence family，非完全独立 |
| 1997/1998 nodelists 有明确日期与节点结构 | current index + recovered GitHub files | recovered primary artifact / medium-high | 原始分发介质 / hash provenance 未闭合 |
| 国际 FidoNet 同样受电话费 / 合作节点影响 | 1993 *Washington Post* + FidoNet standards | B + A / high | 不直接代表中国成本与用户结构 |

注：`A-content?` 是本文件的提醒标记，不改变 `docs/METHOD.md` 的正式 A/B/C/D 合同；它表示“页面承载的文本看起来是历史操作说明 / 同期文本，但当前 HTTP 容器并非已验证历史 capture”。正式数据 schema 实现时应拆成 `content_provenance` 与 `capture_provenance`，而不是新增模糊等级。

---

## 13. 反例与后见之明风险

### 13.1 不要写“1994 年前中国没有网络”

有科研邮件、专线、CFido 等前史。

### 13.2 也不要写“1994 年前中国人已经普遍上网”

CFido 和科研通信都具有很高设备 / 技能 / 组织门槛；全功能 Internet、大众商业服务和家庭普及是不同状态。

### 13.3 不要把 CFido 只写成后来互联网名人的青春史

著名人物因为后来容易被记录，会制造 survivorship bias。old-Web archaeology 更应保存普通用户、普通站台、失败的拨号、附件、规则和没有“成功故事”的页面。

### 13.4 不要把 current legacy page 当作 frozen 2000 snapshot

页面自己说“保留 2000 年样子”只是平台自述。它可能经历服务器迁移、编码调整、链接修补、静态化或资源替换。

### 13.5 不要把 Web republication 当成原帖

《龙音》文章可见，只证明编辑后的表示仍可见；原 message thread / route / reply chain 仍可能失去。

---

## 14. M1 状态：NOT ACHIEVED IN THIS SLICE

本轮取得并实际检查了：

- current `cfido.com` legacy pages；
- current StarStudio page；
- current 《龙音》第二期页面；
- current nodelist index；
- 后来保存的 1997/1998 nodelist 文件；
- 高质量学术史与国际同期 FidoNet 报道 / 标准。

但是本轮**没有取得并实际打开检查一份 1995—2001 `cfido.com` / StarStudio / 中文 CFido BBS 的 verified Wayback/WARC capture**。

因此以下仍为 `unknown`：

- 1997 / 1998 / 2000 某一确切日期的 HTTP response headers；
- 当时真实 Content-Type / charset；
- 原始 HTML 是否与当前 legacy page bit-identical；
- 当时图片、MIDI、JS 等子资源是否完整；
- 当前 MSIE 分支何时加入；
- 历史服务器软件与目录结构；
- 原拨号 BBS 的 DOS / ANSI / 中文终端真实画面；
- BlueWave packet 的原始样本与中文编码；
- 站台实际在线 / busy / downtime 日志。

所以不能宣称“CFido Web case 已完成复原”。

同时也不能写“Wayback 没有”。正确结论只是：

> **本轮尚未验证到满足 M1 合同的历史 capture。**

---

## 15. 下一步最值钱的考古动作

1. 针对 `cfido.com`、`www.cfido.com/starstudio/star.htm`、`deq.htm` 搜索并实际验证 1997—2001 captures；
2. 对每个 capture 分别记录 original URL、capture datetime、HTTP / replay 状态、charset 与子资源；
3. 比较当前 legacy HTML 与历史 capture 的 DOM / links / JS；
4. 获取至少一个原始 BlueWave packet 或 BBS 软件 fixture，在隔离环境里检查编码与工作流；
5. 对 `NODELIST.304` 等 recovered artifact 补 provenance：最早保存来源、文件 hash、与其他副本比对；
6. 若能得到旧浏览器环境，复现 MSIE `<bgsound>` 与非 IE `<embed>` 分支；
7. 专门采样普通站点，而不是只追踪后来著名站长。

---

## 16. 对中文旧网谱系的修正

现有平台谱系常写：

```text
个人主页
→ 独立论坛 / BBS
→ 托管博客
→ 平台社区
→ SNS
```

CFido 提醒我们，在“论坛 / BBS”之前和旁边还要保留另一条**通信拓扑谱系**：

```text
电话号 + modem
→ local BBS
→ Fido node address / Echomail
→ offline packet
→ Internet email / Web mirror
→ Web account / IM
```

这不是要求仓库把 scope 前移到 1980s，而是为了正确解释 1995—2001 中文 Web 为什么会继承：

- BBS 话语习惯；
- nickname / ID；
- 版区 / 信区；
- 下载区；
- 站长文化；
- 字符终端与中文编码约束；
- 业余维护与服务器自建；
- “先在线发现、再离线处理”的低带宽行为。

因此中国 1995 年以前的 CFido 只作为必要前史；本仓主研究对象仍然是约 1995—2015 中文旧 Web。

---

## 17. 本轮新增结论

这个 companion 的实质新增不在“CFido 很早”这一事实，而在于把历史可见性拆成新的状态模型：

> **一条 1997 年的网络消息，可能先存在于某台家用 BBS 的磁盘里，经电话线和离线信包穿过几个节点，再被编辑选进电子杂志，最后变成今天浏览器还能打开的一张 HTML。我们今天保存下来的，往往只是这条生命链最后的一层。**

因此，后续只要研究 dial-up BBS / early Web overlap，就必须明确：`Web-visible artifact ≠ original network state`。