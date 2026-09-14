# CFido 前史边界：live-legacy HTML、nodelist、离线信包与 Web 迁移（1996—2001）

> 状态：prehistory / boundary research note；**不把本仓 scope 改成全球或完整 FidoNet 史，也不是 M1 complete case。**  
> 与 `how-people-lived` 交叉：解释中文旧 Web 为什么不能从“网页出现”才开始理解用户、内容和网络实践。  
> 本轮另重试了上一轮西祠精确 Wayback locator；当前运行环境仍不能完成 replay / CDX 核验，因此西祠状态不升级。

## 1. 为什么 CFido 可以进入 OWA，但只能作为直接必要的前史

本仓主范围仍是约 1995—2015 中文互联网。

CFido 自 1991 年起的 dial-up BBS / FidoNet 历史本身不应把 OWA 无限前移。但 1996—2001 的材料直接触及中文旧 Web 的几个核心问题：

1. **同一批内容可以先在 FidoNet / BBS 信包里传播，再被投影到 Web；**
2. 1997 年 `cfido.com` 已经作为 CFido / 《龙音》的 Internet home；
3. 页面、电子杂志、nodelist 和 BBS 运行状态具有不同保存机制；
4. 一个今天仍可打开的 1990s / 2000-era legacy site，不等同于 Wayback capture；
5. 历史用户的主要读写过程可能发生在离线 reader 里，而不是服务器页面上。

因此这里研究的是：

> **中文旧 Web 从什么既有数字通信系统里长出来，以及哪些前 Web artifact 能帮助解释后来 Web 页面。**

不是：

> “把 old-web-archaeology 变成 FidoNet 历史仓库”。

---

## 2. 研究单位：这里至少有六种不同 artifact

按照 `docs/METHOD.md`，不能把“CFido”混成一个对象。

本轮拆成：

```text
network / protocol system
  CFido / Fidonet Region 65

station / node
  例如 6:657/901 StarStudio BBS

interactive BBS runtime
  用户拨号进入后的菜单、信区、文件区、账号权限、busy/idle 状态

offline packet
  用户下载到本机后离线阅读 / 写回复的信包

periodic network-state artifact
  NODELIST.xxx / diff

Web projection / live-legacy HTML
  cfido.com / 《龙音》 / StarStudio 说明页
```

这些对象的保存率完全不同。

---

## 3. 本轮 artifact 1：1997《龙音》第二期 —— 同时在 CFido 与 Web 发行

当前仍可访问：

- `https://www.cfido.com/deq.htm`

页面正文明确标注：

- 《龙音》第二期；
- 出版日期 `1997-05-09`；
- 1997-05-01 前后 CFido 获得 `cfido.com` 与 Internet 服务器空间；
- 内容基本取材于 CFido 信件；
- 杂志有纯文本、HTML 两种版本在 CFido 上发行，可从站台下载；
- 同时可以从 `http://www.cfido.com` 获得。

这是一条非常强的**跨传输系统 provenance**：

```text
CFido messages
→ edited electronic magazine
├→ plain text / HTML distributed through CFido stations
└→ HTML published through Internet / Web
```

### 对 OWA 的直接影响

不能因为今天最后留下的是 `http://www.cfido.com/...`，就把原内容的“出生地”自动判定成 Web。

这和仓库此前的 `SMS → operator → Web classified listing` 类似，但这里进一步出现：

> **同一份内容在同一时间可以同时属于非-Internet BBS 网络和 Web。**

本文记作：

- `cross-transport publication provenance`
- `legacy-to-Web projection`

---

## 4. 本轮 artifact 2：StarStudio BBS 使用说明 —— Web 页面保存了非 Web runtime 的操作合同

当前可访问：

- `https://www.cfido.com/starstudio/star.htm`

这张 HTML 页面不是历史 BBS runtime 本身，却详细描述了 runtime：

- Echomail / Localmail / PVT / Netmail；
- 约 60 个信区及其名称；
- Blue Wave offline mail；
- 文件服务；
- 新用户 / 正式用户 / 进阶用户级别；
- 每日 10 / 20 / 30 分钟级别的使用额度；
- 加入所需电脑、modem、外线电话和通信软件；
- 账号升级需要填写资料、发自我介绍、学会使用 Blue Wave 等。

### 隐私处理

页面也公开了历史拨号电话号码、个人 ID / 姓名等字段。

这些号码今天可能重新分配，仓库后续应：

- 保存 `phone field existed`；
- 如需证明 node identity，优先用 station / node address；
- 不在新的结构化数据集里重新大规模发布历史电话号码；
- 普通个人身份只保留支持 claim 所需的最小字段。

---

## 5. `offline-session inversion`：BBS 的大部分“使用”可能发生在断线以后

StarStudio 的 Blue Wave 工作流非常重要：

```text
connect
→ request/download packet
→ disconnect
→ read offline
→ write replies offline
→ pack replies
→ reconnect
→ upload reply packet
```

页面解释这样做可以：

- 节省电话费；
- 节省站台在线时间；
- 让用户有更长时间读写；
- 让其他人更容易拨入。

因此历史 BBS 体验出现一个和 Web 完全不同的保存问题：

> **最值得研究的阅读 / 写作时刻，反而可能没有发生在服务器 session 中。**

即使我们未来拿到：

- 一张完整 BBS 菜单截图；
- 一个 telnet / modem session transcript；

也仍然可能错过用户真正花最多时间的本地 offline reader。

本文暂记：

> **`offline-session inversion`**：网络系统的关键使用行为发生在网络连接之外，服务器端 artifact 对用户时间经验的覆盖反而有限。

---

## 6. `line-state invisibility`：单线 BBS 的关键状态几乎不会进入静态档案

StarStudio 遗留页说许多业余 Fido BBS 因成本是单线系统；这意味着用户实际访问链条包含：

```text
拨号
→ 对方是否占线？
→ modem 是否握手成功？
→ 今天账号还有多少分钟？
→ 登录
→ 下载 / 上传
→ 断线
```

其中最影响普通人体验的状态之一：

```text
line = busy / idle
```

通常不会进入：

- Web capture；
- nodelist；
- 静态截图；
- later homepage。

所以新增：

> **`line-state invisibility`**：历史拨号系统的实时线路竞争，是用户能否进入系统的决定性运行状态，但静态网络档案往往完全看不见。

这和“页面是否保存”是不同的 archive gap。

---

## 7. 本轮 artifact 3：1997 nodelist —— 可以验证周期网络状态，而不是用户 session

`cfido.com` 当前 nodelist index 指向保存仓：

- `https://cfido.com/nodelist/list.html`
- source 标为 `https://github.com/lshw/cfido_nodelist`

目录中可见多期 artifact，例如：

- `NODELIST.234` — 1997-08-22
- `234_304.diff` — 1997-10-31
- `NODELIST.304` — 1997-10-31
- `NODELIST.346` — 1997-12-12
- `NODELIST.002` — 1998-01-02
- 此后还有连续多期 node list / diff。

本轮通过 GitHub 直接检查了两期原始文本：

### 1997-08-22：`NODELIST.234`

文件头写明：

```text
A Zone Nodelist for Friday, August 22, 1997 -- Day number 234
A listing of all the systems within Region 65 of Fidonet
```

在福建段可以确认：

- `Host,657,Fujian_Net,...`
- `StarStudio_BBS` 对应 node `901`；
- station record 还包括 location / sysop / phone / speed / capability flags。

源：

- https://github.com/lshw/cfido_nodelist/blob/master/NODELIST.234

### 1997-10-31：`NODELIST.304`

同一区域两个月后仍可确认 StarStudio `657/901`，但邻近 topology 已变化，例如：

- 福建 hub 编排发生变化；
- 有节点进入 `Hold`；
- 新的 `Pvt` / hub 状态出现。

源：

- https://github.com/lshw/cfido_nodelist/blob/master/NODELIST.304

这已经给出一个真正的 **≥2 historical timepoints** artifact family。

但必须明确：它证明的是 network directory state，不是：

- 那天某个电话一定打得通；
- 某个用户成功登录；
- BBS 菜单长什么样；
- 某个信区当时有哪些帖子；
- 某个账号具有什么权限。

---

## 8. 新 artifact 类型：`protocol-emitted state fossil / 协议周期状态化石`

Web 考古很容易只寻找 HTML / image / CSS。

CFido nodelist 提醒我们：一些网络会定期产生自己的机器可读状态文件。

这些文件不是网页，却可能比网页更可靠地保存：

- node identity；
- region / net / hub 关系；
- station status；
- capability flags；
- 某个时间点网络拓扑。

而 `.diff` 文件又直接编码了“上一版 → 下一版发生了什么”。

因此可定义：

> **`protocol-emitted state fossil`**：由网络运行协议 / 协调流程周期产生、后来可用于重建历史状态的机器可读 artifact。

它和 archive crawler 的 capture 不同：

```text
Wayback capture
= 第三方在某时刻抓到一个 representation

nodelist
= 当时网络自己为了运行而发布的一份状态表示
```

在证据上，两者应分开标 provenance。

---

## 9. `directory state != operational state`

nodelist 再硬，也不能过度解释。

一个节点出现在 `NODELIST.234`，最多证明：

> 在这一版网络目录中，它被列为该身份 / 状态 / capability。

不能自动证明：

```text
published in directory
= line currently answered
= modem handshake worked
= BBS runtime healthy
= user could log in
= content was available
```

所以沿用并强化仓库已有原则：

> **`directory state != operational state != user-session state`**。

这和在线地图的 “map record != route actually executable” 很相似，但这里的运行变量是电话线路、modem、mailer、账号分钟和 station software。

---

## 10. 当前 `cfido.com` 应怎样定级

首页当前写有：

- “网站最后更新时间2001-10-17”；
- “网站保留了2000年时候的样子，不再美化”；
- IE4+ / 800×600 建议。

来源：

- https://cfido.com/

另页称 `cfido.com` 1997-04-28 注册，由 StarStudio 站长申请并托管，用于宣传中国 FidoNet：

- https://www.cfido.com/gnxx.htm

### 本轮建议的 artifact 分类

```yaml
artifact_type: live_legacy_site
current_http_access: achieved
historical_self_claim:
  last_updated: 2001-10-17
  preservation_claim: retains circa-2000 appearance
byte_identity_to_2000: unverified
wayback_capture_required_to_prove_exact_2000_representation: yes
```

证据等级不要简单写一个字母：

- **A**：今天我们实际取得的 HTML / 当前页面内容；
- **A/B**：页面自身带日期的 1997 电子杂志文本，可作为原生 dated artifact 使用，但仍记录今天托管 provenance；
- **B / medium-high**：关于“整个网站保持 2000 年样子”的自我声明；
- **unknown**：今天 HTML 是否逐字节等同 2000 年版本。

---

## 11. 历史浏览环境线索：这里不是“现代网页只是长得旧”

CFido 首页当前明确建议：

```text
IE 4.0+
800×600
```

StarStudio 页面底部还能看到根据 `navigator.userAgent` 判断 MSIE 后选择 `bgsound`，否则使用 `embed` 的脚本逻辑。

因此它很适合进入未来 M3 browser experiment：

- modern Chromium；
- IE4 / IE5 级环境；
- Netscape 级环境；
- MIDI / background sound 支持差异；
- 800×600 viewport；
- 可能的中文 charset / font 差异。

但本轮没有执行旧浏览器实验，所以不能写“已复原历史浏览体验”。

---

## 12. 1997 同期文章把 `nodelist` 的运行用途说得很清楚

《龙音》第二期技术文章解释：

- 站台有 zone:net/node.point 地址；
- 更详细资料放在定期更新的 nodelist；
- nodelist 含站名、电话、站长 ID、位置、modem 速率等；
- mailer 在转信时用这些资料拨叫另一个站台；
- 下游站需要及时更新 nodelist；
- 它把 nodelist 类比为 Internet 域名服务器的一类功能对应物。

来源：

- https://www.cfido.com/deq.htm

这使 1997 nodelist 不只是“后来有人收藏的一堆文本”：

> 同期参与者已经明确说明它是网络运行本身所需的状态目录。

---

## 13. 海外方法对照：FidoNet 的 mail-window artifact

OWA 不扩张到全球旧网，但海外 FidoNet 可以帮助判断哪些 archive 问题是协议共同属性。

FidoNews 1989 年同期刊物中，节点的 network mail 接收被明确限制在专门的 mail-hour window；另一篇同期文章讨论长途电话成本、mail waiting window，以及在 network mail 期间拒绝普通 human caller。

来源：

- https://fidonews.site/1989/v06n01/
- https://www.fidonews.site/1989/v06n22/

所以：

- line contention；
- batch transfer；
- mail windows；
- 电话费用塑造网络时间；

不是中文 CFido 独有。

中文旧网研究真正需要解释的是这些机制如何进入中国电话网、中文软件生态，并怎样在 1997 前后和 Web 同时运行。

---

## 14. 对上一轮西祠 locator 的实际重试结果

上一轮精确 candidate：

```text
original:
http://www.xici.net/b373044/d50430566.htm

candidate memento:
https://web.archive.org/web/20110724135817/http://www.xici.net/b373044/d50430566.htm
```

本轮再次尝试：

- Web replay direct open；
- exact URL / title search；
- Wayback / archive locator search；
- runtime direct request / CDX 路径。

结果仍未取得可检查 replay：当前工具链对嵌套 `http://` URL / Wayback replay 有 safe-URL / transport 限制，而容器侧又无法解析 `web.archive.org` DNS。

因此状态只能继续写：

```yaml
exact_memento_locator: known
opened_capture: false
capture_absent: unknown
wayback_saved_it: unknown
transport_in_current_runtime: failed_or_unavailable
```

**不能**写：

- “Wayback 没保存”；
- “页面已丢失”；
- “已经恢复西祠 2007 页面”。

这次重试是负结果，不新增概念文件。

---

## 15. 当前“已证实 / 高概率 / 不知道”

### 已证实

- 1997-05-09《龙音》页面当前可访问，正文明确给出日期和 CFido / Internet 双通道发行说明；
- StarStudio 遗留页当前可访问，并保存 Blue Wave、信区、账号分钟与加入条件说明；
- `NODELIST.234`（1997-08-22）和 `NODELIST.304`（1997-10-31）可以直接读取；
- 两期 nodelist 都列出福建 net 与 StarStudio `657/901`，且同一 net 内节点状态会随版本变化；
- `cfido.com` 当前首页自述最后更新于 2001-10-17，并称保留约 2000 年样式。

### 高概率

- 当前 live-legacy 站保留了相当多 1997—2001 真实历史内容和 HTML 结构；
- nodelist / diff 是后续重建 CFido 网络时点最有价值的第一手 artifact family 之一；
- 1997 `cfido.com` 是非-Internet BBS 社群向 Web 投影的直接过渡对象。

### 不知道

- 当前 `cfido.com` 各文件是否与原 1997 / 2000 字节完全一致；
- 原服务器 / 后续迁移是否改过 charset、headers、timestamps；
- 1997 用户真实看到的页面是否和今天 modern Chromium 渲染一致；
- BBS interactive runtime 的菜单、ANSI / terminal 表现、busy state、session log；
- Blue Wave 历史 packet fixture 是否仍可安全取得并验证；
- 西祠 exact memento 的 replay / DOM / charset / subresources。

---

## 16. M1 / M3 价值与下一跳

CFido 本轮不替代 M1 三案例，但它提供了一个比“继续找更多旧站介绍”更硬的 artifact-first 路线。

下一步优先级：

1. 对 `cfido.com` 选一个具体 dated page，查询 Wayback / Common Crawl 的独立时间点，与 live-legacy HTML 做字节 / DOM / link 对照；
2. 对 `NODELIST.234 → NODELIST.304` 做机器 diff，验证 topology change，而不是手工印象；
3. 找一个可公开、非敏感的 Blue Wave sample packet / reader 文档，记录离线格式，不触碰普通人的私信；
4. 在隔离旧浏览器环境中重放 `cfido.com` 的 IE4 / Netscape 分支，记录 MIDI / layout / charset 差异；
5. 西祠 replay 通道一旦可用，立即回到 exact memento，避免主题漂移。

---

## 17. 本轮方法结论

这次最重要的考古校正是：

> **历史数字网络不总是以“历史网页”的形式留下自己。**

对 CFido 来说，可能保存得最好的反而是：

- 周期 nodelist；
- nodelist diff；
- 电子杂志；
- Web 上保存的操作说明；
- 离线 reader / packet 格式。

而最难留下的是：

- 某一刻电话线是不是忙；
- 用户拨了几次才接通；
- 当天还剩几分钟；
- 本地离线读了多久；
- 回复在哪一轮 mail batch 才到另一个城市；
- 交互 BBS 屏幕在某个具体 session 里到底是什么样。

所以一个真正的中文旧网考古对象，有时必须从：

```text
HTML archaeology
```

扩大成：

```text
HTML
+ protocol state files
+ client/offline formats
+ network timing rules
+ runtime/session gaps
```

同时仍保持 OWA 的 1995—2015 中文互联网主 scope，不把前史无限扩张。
