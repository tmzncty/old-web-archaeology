# 图文电视数据广播、PC 接收卡与 signal-layer archive gap（1994—2002）

## 0. Scope：为什么一个 old-Web 仓库要记一条非 Web 数据广播边界

本 note **不把 `old-web-archaeology` 扩成全球 teletext 史**，也不把 1994 年以前的中国广播技术变成仓库主对象。

它只处理一个和 1995—2015 中文 Web 考古直接相关的边界问题：

> **中文 Web 出现时，数字信息并不是第一次进入普通终端。电视数据广播、专用接收卡、有线数据服务等非 Web 数字通道已经存在，并且至少到 2002 年仍与 Modem Internet 并行。若研究者只保存 URL，会把这一层真实数字生活系统性漏掉。**

交叉生活史主文件：

- `how-people-lived/sources/teletext-data-broadcast-pc-cards-and-one-way-digital-information-china-1993-2002.zh-CN.md`

相关但不要重复的本仓专题：

- `docs/ONLINE_SECURITIES_PORTAL_TRADING_CLIENT_ACCOUNT_ORDER_EXECUTION_AND_SETTLEMENT_STATE_GAPS_1997_2015.md`
- `research/dial-up-metered-session-phone-line-contention-and-access-context-loss-1997-2003.md`

本 note 不再讨论证券账户、委托、成交和结算；这里只问：

1. 数据如何在 Web 之外进入 PC/电视；
2. Web 与非 Web 数字入口怎样并存；
3. 为什么普通 Web archive 无法自动保存这种历史使用环境；
4. 将来拿到硬件、驱动、页面或录像时，最低应记录哪些字段。

---

## 1. 去重门禁：这不是另一个 `page != transaction`

现有 saturation audit 要求，新专题必须至少带来一个新的 artifact、事务架构、普通人生活路径、保存机制或跨时点变化。

本轮满足的是**新的保存机制与媒介边界**：

- **signal-layer archive gap / 信号层档案缺口**：历史信息实际存在于电视广播/有线数据流中，但 Web crawler 只会留下后来讨论它的网页；
- **receiver-state dependency / 接收端状态依赖**：真实可读结果依赖接收卡/盒、驱动、软件、信号与频道配置，HTML 并不能复原；
- **return-path split / 返回路径分裂**：信息可以由广播通道进入终端，而用户的查询、回复和事务操作需要另一条线路；
- **upstream/last-mile ambiguity / 上游与最后一公里歧义**：报道说服务商卫星受干扰，不等于每个家庭都用卫星接收；
- **protocol-label ambiguity / 历史标签协议歧义**：不同年代都叫“图文电视/图文数据”，不保证使用同一制式和完全相同协议。

因此本轮不是给既有 state-gap 换名。

---

## 2. Prehistory boundary：1993 已有 `GB/T 14219-1993`，1994 Web 不是中国机器可读数字广播的起点

### 2.1 国家标准提供了非常干净的时间锚

全国标准信息公共服务平台记录：

- `GB/T 14219-1993《中文图文电视广播规范》`；
- 发布：1993-03-06；
- 实施：1993-11-01；
- 主管部门：广电总局。

来源：
- https://openstd.samr.gov.cn/bzgk/std/newGbInfo?hcno=7DF1BA3E5784C639001AB7761394033C

**证据等级：A。**

这比中国 1994-04-20 全功能接入全球 Internet 更早。CNNIC 对后者的官方历史定位见：

- https://www3.cnnic.cn/n4/2022/0401/c87-912.html

因此 old-Web 在写 1994/1995 边界时必须避免：

> “Web/Internet 把中国第一次从模拟信息带进数字信息。”

目前更稳的表述是：

> **Internet/Web 把一种新的通用、可寻址、可交互网络入口带入中国；它不是机器可解码数字信息传送的绝对起点。**

这条 1993 证据只作为主 scope 之前的必要边界，不继续把本仓无限前移。

### 2.2 1994 同期报纸说明：数据可以通过电视信号进入 PC 卡并还原成文件

1994-09-27《人民日报》同日报道《图文电视广播悄然兴起》明确描述：

- 数据信号插入正常电视信号；
- 专用图文电视机可显示页面和计算机文件；
- 广电部科研院与北京瑞照科技发展公司推出图文电视微机接收卡；
- 接收卡从视频信号分离数据，将其还原成文件，并可存储、显示、分析和打印。

来源：
- https://cn.govopendata.com/renminribao/1994/9/27/11/

**证据等级：B+。** 同期报纸正文，当前历史文本镜像。

这条材料非常重要，因为它指出一种不依赖 URL 的历史数字对象：

`broadcast stream` → `receiver card` → `local file`。

Web archive 的默认抓取对象则是：

`URL` → `HTTP response` → `HTML/resource graph`。

两者天然不是同一个 artifact universe。

---

## 3. 1995 标准把整个“播出系统—电视网—用户接收机”定义成一条图文电视通道

`GB/T 15771-1995《图文电视通道基本技术参数及测试方法》`：

- 1995-12-08 发布；
- 1996-08-01 实施；
- 广电部广播科学研究院起草；
- 适用于 PAL-D 制电视通道中的图文电视信号。

官方元数据：
- https://std.samr.gov.cn/gb/search/gbDetailed?id=71F772D8268DD3A7E05397BE0A0AB82A

**证据等级：A。**

当前标准文本镜像还把“图文电视通道”定义为从播出系统输出端到用户接收机检波输出端的全过程，并列出电视中心、播控、发射机、电视网、接收机等环节：

- https://www.bzxz.net/bzxz/14651.html

**证据等级：B 文本辅助。**

### 3.1 对 old-Web 方法的含义

如果一个 1997 用户通过电视数据广播收到一组行情或文件，今天可能留下的证据包括：

- 国家/行业标准；
- 运营商宣传；
- 接收卡包装；
- ISA/PCI 卡本体；
- 驱动软盘/CD；
- 客户端软件；
- 用户手册；
- 报纸说明；
- 屏幕照片；
- VHS 录像或 RF/基带信号录制；
- 本地落盘文件。

而可能**完全没有**：

- public URL；
- HTML；
- HTTP header；
- Web server log；
- 可由 Wayback 重放的页面。

因此：

> **`no historical URL found != no digital information service existed`。**

这应该和仓库现有的：

`no capture found != no page existed`

并列，但不能混为同一句话。

---

## 4. 2002：同一台家庭 PC 可以选择 Internet Modem，也可以选择有线图文数据接收卡

2002-01-29 中关村在线面向家庭用户的装机文章《如何配置炒股用电脑？》直接并列：

- “上网方式”：需要稳定 Modem；
- “有线电视网方式”：需要有线图文数据接收卡或外置接收盒。

还进一步区分：

- 职业/短线用户：接收卡 + 盘中即时数据；
- 兼职/中长线用户：Modem 上网，收盘后短时下载数据，同时获得浏览 Internet 和 Email 的能力。

来源：
- https://diy.zol.com.cn/2002/0129/35410.shtml
- 同期新浪转载：https://tech.sina.com.cn/c/2002-02-01/11062.html

**证据等级：B+。** 同期大众电脑媒体操作建议。

### 4.1 一个必须进入 old-Web archaeology 的状态分裂

到 2002 年，一个 PC 用户的数字信息状态至少可以是：

`owns PC`

≠ `has Modem`

≠ `has Internet account/access`

≠ `has cable-TV line`

≠ `has teletext/data receiver card`

≠ `subscribes to specialized real-time feed`

≠ `can browse WWW`

≠ `can receive e-mail`

≠ `can receive real-time one-way broadcast data`。

因此看到“家里有电脑看实时行情”时，不能自动标注为 `Internet user`。

反过来，看到一个家庭已经拨号上网，也不能推断它不会继续使用股票卡/有线数据卡。

### 4.2 Web 出现以后，旧数字媒介不一定只是“落后 fallback”

同期文章甚至给专用实时流一个明确用途优势：对于需要盘中持续跟踪的人，专用数据接收仍被推荐；而 Modem 的优势在于成本、通用 Web、Email 和收盘后下载。

所以更准确的媒介替代模型是：

`specialized broadcast real-time lane` **vs** `general interactive Internet lane`

在一段时间内按需求并存，而不是：

`旧媒介失败 → Web 接管全部功能`。

---

## 5. 2002 广州故障：保存了真实 household endpoint，却留下了网络拓扑歧义

2002-03-16《新快报》/搜狐报道日凌干扰造成广州部分图文数据服务中断：

- 约两万使用“家庭服务器”的股民未能正常收到股市信息（报道估计口径）；
- 王先生在家炒股，家里安装设备接收股市信息；
- 开盘后无数据，服务公司热线拥堵；
- 服务公司称其使用的卫星链路受到日凌影响；
- 本次中断约 25 分钟。

来源：
- https://news.sohu.com/07/39/news148173907.shtml

**证据等级：B+。** 同期用户投诉 + 记者现场 + 服务商说明。

### 5.1 `upstream medium != household last mile`

这类历史报道极易被后来的技术史写错。

文章说的是：

`传播公司使用的卫星受到干扰`

它没有证明：

`每户家庭都安装卫星天线直接下行`。

结合 2002 ZOL 的“有线电视网 + 图文数据接收卡/接收盒”，完全可能存在：

`卫星/其他上游 feed → provider/headend → cable/other local distribution → household receiver`

但这是**工程重建候选**，不是本轮已证实拓扑。

所以写入方法规则：

> **`upstream transport evidence != last-mile transport evidence`。**

任何未来重建都要单独找：

- 服务商头端结构；
- 城市有线网接口；
- 家庭安装说明；
- 接收卡输入端；
- 是否需要独立天线/机顶盒；
- 本地频道/频点配置。

### 5.2 “家庭服务器”也不能按今天的 server 概念硬译

报道使用“家庭服务器”一词，但本轮没有型号、说明书、照片文字细节或厂商资料。

因此当前只保留历史原称，不推断：

- 它是否真正运行 server process；
- 是 PC 内置卡还是外置盒；
- 操作系统；
- 协议；
- 数据格式；
- 是否带缓存；
- 是否需要账号/加密卡。

---

## 6. `return-path split`：接收实时数字信息与执行事务可以是两套基础设施

现有证券专题已经说明 Internet 网上委托、电话委托、专用拨号网络、券商 gateway 和交易所状态必须拆开。

图文数据材料再补一层：

`real-time quote/data reception channel` 与 `order/response channel` 本身也可能不同。

因此对于历史证券终端：

`data card receives quotes` ≠ `same card can submit orders`。

对于更一般的图文电视：

`PC receives file` ≠ `PC can reply to publisher over same path`。

这构成：

> **`return-path split / 返回路径分裂`**。

这对 Web 史很有解释力：Web/Internet 后来的重要变化之一，是把原来分散在不同媒介上的“获取—查询—回复—提交”逐渐收敛进同一通用网络，而不是第一次让机器显示远程文本。

---

## 7. 新的 archive failure mode：`signal-layer archive gap`

### 7.1 Web archive 更容易留下“谈论信号的网页”，而不是信号本身

今天我们还能打开：

- 1994《人民日报》对图文电视的描述；
- 2002 ZOL 的接收卡装机建议；
- 2002 搜狐保存的故障新闻。

这会制造一种错觉：历史对象是这些网页。

实际上，用户当年真正依赖的是：

- 某一时刻的 RF/有线/基带数据流；
- 某个频点/频道；
- 接收卡；
- 驱动；
- 客户端；
- 实时数据内容；
- 本地缓存/文件。

网页只是今天留下来的**旁证壳**。

所以新增：

> **`signal-layer archive gap / 信号层档案缺口`**：
> 公共 Web 档案可以很好地保存描述广播数据服务的网页，却可能完全没有保存用户当时真正接收的数据流。

### 7.2 `historical article survives != historical signal survives`

最低状态必须拆：

`article says service existed`

≠ `original broadcast signal preserved`

≠ `raw data frames preserved`

≠ `receiver hardware preserved`

≠ `driver/software preserved`

≠ `receiver can still decode stream`

≠ `historical user-visible page/file can be reconstructed`。

### 7.3 这也是“Web hindsight bias”的一个新来源

研究者能够搜索到 URL，于是自然更容易研究 Web；无法输入 URL 的信号层服务就像从未存在。

这会导致：

> **数字信息史被 URL 可检索性反向塑形。**

old-Web archaeology 因此需要主动记住：中文 Web 的同时代竞争者和邻接媒介，有些从一开始就不属于 crawler-friendly artifact universe。

---

## 8. `receiver-state dependency`：网页完整保存也无法替代历史接收端

图文数据服务的历史“可用性”依赖至少这些对象：

1. 当地是否有信号；
2. 频道/频点/线路是否正确；
3. 接收卡或外置盒是否存在；
4. 硬件接口是否与 PC 兼容；
5. 驱动是否可安装；
6. 客户端软件是否存在；
7. 数据格式/协议是否匹配；
8. 字符集和字体是否可用；
9. 服务是否需要订阅/授权；
10. 上游 feed 是否正常；
11. 本地软件能否存储、显示、分析或打印。

因此新增：

> **`receiver-state dependency / 接收端状态依赖`**。

它和现有 Web archaeology 的 browser/charset assumption 类似，但更硬：没有历史卡和驱动，连“服务器重放”这一层都未必存在。

---

## 9. protocol-label ambiguity：不要把所有“图文电视”强行画成一条单协议谱系

当前证据包括：

- 1993 `GB/T 14219-1993` 中文图文电视广播规范；
- 1994《人民日报》的图文电视微机接收卡；
- 1995 `GB/T 15771-1995` 图文电视通道；
- 2002 ZOL 的“有线图文数据接收卡”；
- 2002 广州“图文电视数据传播有限公司”家庭股市数据服务。

这些名称明显相关，但当前还缺：

- 产品手册；
- 数据帧格式；
- 驱动；
- 接收频率；
- 服务商协议；
- 是否严格采用 CCST；
- 是否有私有扩展。

因此：

> **`terminology continuity != protocol identity`。**

未来任何谱系图都应把“同名/近名”与“技术兼容”分成两条证据。

---

## 10. 海外 comparison boundary：Ceefax 只用来证明机制可比较，不写进本仓主体

英国 Science Museum Group 的 BBC Heritage 藏品记录，Ceefax 1974 年启动，通过电视信号 vertical blanking interval 发送数据，可提供最新新闻和字幕：

- https://collection.sciencemuseumgroup.org.uk/objects/co8356079/ceefax-clock

BBC 后来的历史回顾记载，1980 年代数百万英国家庭购买支持 teletext 的电视，1990 年代周使用者达到约 2000 万，内容包括股价、食谱等：

- https://unvis.it/www.bbc.co.uk/news/uk-20032882

2009 年 Teletext 新闻业务关闭时，运营方把 online use 增长列为传统电视文字业务衰退因素之一：

- https://www.theguardian.com/media/2009/jul/16/teletext-to-be-pulled-tv

这只支持一个跨国机制：

`broadcast digital information before mass Internet` 并非中国特例。

本仓不继续写英国 teletext 历史，也不把中国的 CCST 与 BBC Ceefax 视为同一协议。

---

## 11. 给未来 artifact probe 的 `broadcast_data_context` 最小记录块

如果以后得到接收卡、截图、说明书、视频或信号记录，建议附：

```text
broadcast_data_context:
  observed_date:
  provider_or_station:
  service_name:
  city_or_coverage:
  terminology_used_by_source:
  claimed_standard:
  standard_evidence:
  upstream_transport:
  last_mile_transport:
  channel_or_frequency:
  receiver_hardware:
  receiver_interface:
  driver_version:
  client_software:
  os_requirement:
  character_set_or_font:
  subscription_or_auth:
  return_path:
  content_type:
  real_time_or_delayed:
  raw_signal_preserved:
  decoded_data_preserved:
  screenshot_or_video_preserved:
  user_manual_preserved:
  uncertainty:
```

### 11.1 字段约束

- `upstream_transport` 和 `last_mile_transport` 必须分开；
- `claimed_standard` 不能根据年代猜；
- `return_path` 若没有证据就填 `unknown`，不能因为 PC 有 Modem 就推断同一服务双向；
- `raw_signal_preserved=false` 时，不应把截图当作完整协议复原；
- `terminology_used_by_source` 保留历史原词，以防今天术语覆盖当年实现差异。

---

## 12. Artifact search outcome：本轮取得的是强边界证据，不是 M1 页面复原

本轮实际取得：

- 1993/1995 官方国家标准 locator；
- 1994 同期《人民日报》完整技术描述；
- 2002 同期消费者装机说明；
- 2002 同期广州家庭故障事件；
- 真实公司名 `广州三立经纬图文电视数据传播有限公司`；
- 真实历史设备类别：图文电视微机接收卡、有线图文数据接收卡、外置接收盒、家庭服务器。

本轮**没有**取得：

- 北京瑞照 1994 PC 卡原始手册/驱动；
- 广州三立经纬原始网站；
- 2002 家庭服务器型号和安装文档；
- 原始图文数据 raw capture；
- 一套可运行的接收端软件/驱动；
- 同一服务两个历史时点的 Web 页面 capture。

因此：

**M1 Web artifact claim: NOT ACHIEVED / NOT THE PRIMARY ARTIFACT TYPE IN THIS SLICE。**

尤其不能把 2002 搜狐新闻页面说成“复原了 2002 图文数据服务”。它只复原了关于该服务的一条同期媒体记录。

---

## 13. 与现有证券专题的接口

本轮不修改 `ONLINE_SECURITIES...STATE_GAPS` 的主链，但给它增加一个解释边界：

在 1990s—2000s 初，“在家看实时行情”不等于“通过 Internet 看实时行情”。

未来证券 artifact 遇到以下词汇时应额外查 transport：

- 股票卡；
- 行情卡；
- 图文数据；
- 有线数据；
- 卫星行情；
- 家庭服务器；
- 实时接收软件。

最低需要问：

`quote feed transport?`

而不是只问：

`broker website URL?`

交易执行仍按既有专题拆成账户、权限、客户端、gateway、exchange、fill、settlement。

---

## 14. 本轮新结论

这条线给 old-Web archaeology 增加了一种此前没有明确命名的历史不可见性：

> **Web archive 的缺口不只发生在“网页曾经存在但没抓到”。有些数字生活从一开始就不属于 Web。**

1990 年代中国一部分机器可读信息可以沿电视广播/有线网络进入接收卡；2002 年 Internet 已经成熟到可以被家庭用 Modem 浏览和收邮件时，专用图文数据接收仍真实存在。

所以以后看到 1995—2005 的数字信息史，必须同时防两种后见偏差：

1. **Internet hindsight**：把所有数字信息服务都倒写成 Internet 的前身或早期形态；
2. **URL survival bias**：因为今天只能搜索网页，就误以为当年的数字生活也主要发生在网页里。

本轮更准确的边界是：

> **Web 不是数字信息的起点；它是后来越来越强的一种通用交互层。**

而理解中文旧网真正取代、吸收或绕过了什么，必须把这些没有 URL 的邻接基础设施也留在视野里。