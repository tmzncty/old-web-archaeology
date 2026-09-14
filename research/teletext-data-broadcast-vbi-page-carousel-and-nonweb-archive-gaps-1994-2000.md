# Teletext / 图文电视、数据广播、页轮播与 non-Web archive gaps（1994—2000）

> 状态：research / boundary note，不是 M1 complete case。
>
> 仓库 scope 仍是约 1995—2015 中文互联网。本文件不把项目扩成全球广播史；只研究一个直接影响中文旧网解释的问题：1995 年前后，中国已经存在可显示“页”、可向 PC 分发文件、可与早期 Web 并存的广播数据系统，而 HTTP archive 天然不会把这类对象完整保存下来。

---

## 1. 为什么这不是另一个泛化的 `page != backend state`

仓库已经有大量事务型 state-gap note，再增加一个“动态页面有后台状态”没有研究价值。

Teletext / 图文电视提出的是不同问题：

> **历史 representation 甚至根本不是一个被浏览器请求的 URL。**

典型结构更接近：

```text
editorial/data source
        ↓
teletext/data-broadcast encoder
        ↓
television broadcast signal
        ↓
continuously repeated page/file carousel
        ↓
teletext-capable TV / decoder / PC receiver card
        ↓
local page selection / cache / file storage
        ↓
viewer
```

用户输入页号时，通常不是把 query 发回服务端。

因此：

```text
page number selection != HTTP request
broadcast page != Web page
broadcast timestamp != observation timestamp
TV recording != guaranteed teletext capture
current HTML recreation != original broadcast representation
```

这是一种 OWA 很值得保留的“边界对象”：它能防止我们因为 Web archive 很强，就把 1990s 所有数字信息活动都想象成 Web。

---

## 2. 仓库边界：为什么从 1994 写起仍然符合 scope

`README.md` 把本仓主对象限定在约 1995—2015 中文互联网；`docs/METHOD.md` 要求先确定研究单位，并把 capture/original/claim 分开；`ROADMAP.md` 的 M4 未来还要讨论 resource-type-specific archive gaps。

Teletext 的 1980s 技术研发历史主要属于 `how-people-lived`。

本 note 只保留三件与 1995 后中文 Web 直接相关的事：

1. **1994 年中国已经存在实际运行的数据广播/图文电视用途；**
2. **这些内容/系统与 1994—2000 的早期 Internet/Web 可以重叠，而不是严格前后替代；**
3. **Web archive 对这种非 HTTP representation 存在结构性盲区，必须在解释旧网可见性时显式记录。**

---

## 3. Claim list（先列 claim，再列证据）

### C1 — 1994 年中国已有实际使用的图文电视/数据广播，不只是实验室制式

1994-09-27《人民日报》报道，图文电视数据广播把数据信号插入正常电视信号中；中央电视台已经用它向新疆、西藏等地区传新闻稿，经济部门还向全国发送经济信息。

**Evidence:**

- 《人民日报》1994-09-27 第 11 版数字转录，《图文电视广播悄然兴起》
- <https://cn.govopendata.com/renminribao/1994/9/27/11/>

**Grade:** A-（同时代报刊文本；本轮访问的是数字转录，而非重新核验纸版扫描）

**Confidence:** high for the narrow claim that the article reports operational use.

**Do not upgrade to:** public mass use / household penetration.

### C2 — 当时存在 PC receiver card，把电视数据恢复为文件并在本机存储/分析/打印

同一《人民日报》文章描述广电部科研院与企业推出图文电视微机接收卡；PC 卡从视频信号中分离数据、恢复广播文件，并可存储、显示、分析、打印。

**Grade:** A-，same evidence family as C1.

这条 claim 对 OWA 非常重要，因为它说明：

> 1994 年“计算机上的数字文件”不必由 Internet/Web 下载得到，也可能从广播信号接收。

### C3 — 中国全功能 Internet 连接的 1994-04-20 节点仍必须与图文电视分开

CNNIC 互联网大事记记载，1994-04-20 NCFC 64K 国际专线开通，实现与 Internet 的全功能连接；5 月出现早期 Web 服务器。

**Evidence:**

- <https://www3.cnnic.cn/n4/2022/0401/c87-912.html>

**Grade:** B / 后来机构史整理，引用明确历史节点。

因此本 note 绝不使用这样的句子：

> “中国 1994 年以前已经有互联网，因为有图文电视。”

两者是完全不同的网络/媒介架构。

### C4 — 1994-11-28 CCTV “正式播出图文电视”目前只有较晚媒体史锚点，本轮不升级为 A

搜狐 2003《电视百年》写道，中央电视台 1994-11-28 正式播出图文电视；同文列出多个电视台/信息中心，并说特殊接收装置不足使服务难普及。

**Evidence:**

- <https://media.news.sohu.com/77/44/news209404477.shtml>

**Grade:** C / later retrospective media history.

**Unknown:** 1994 年节目报、广电年鉴、CCTV 技术公报能否直接复核这个日期。

### C5 — 海外 teletext archive 已证明：广播数据可以从家用录像带残余信号重新恢复

Teletext Archaeologist 说明，其档案包含大量从普通家庭录像带恢复的 teletext；页面广播后通常在服务端被覆盖，广播机构只保存少量样本，一部分同时代用户则通过 PC decoder card 保存页面。

其 archive highlights 明确列出多个完整 recovered service snapshot，例如 1995 年 BBC1 / BBC2 / Channel 4 等日期化对象。

**Evidence:**

- <https://teletextarchaeologist.org/>
- <https://teletextarchaeologist.org/the-archive/>
- <https://teletextarchaeologist.org/archive-highlights/>
- Rewind 技术说明：<https://rewind.thetvroom.com/39095/features/teletext-recoveries/>

**Grade:** B for modern archival-method claims; recovered artifacts themselves can become A-like historical signal artifacts once a specific recording/date/provenance is individually verified.

本轮没有把某个英国 recovered service 直接当作中国证据。

---

## 4. 新的研究单位：broadcast service snapshot

OWA 的常见层级是：

```text
platform → site/host → account/homepage → page/URL → capture/artifact → claim
```

Teletext 需要一个并列对象：

```text
broadcast system
→ channel/service
→ page number / file identifier
→ broadcast cycle
→ receiver observation
→ recording / decoded recovery artifact
→ claim
```

建议将来若真的发现中国原始图文电视 artifact，不要强行塞进 `original_url` 模型，而增设类似：

```yaml
medium: teletext-data-broadcast
broadcaster: CCTV?
channel: unknown
service_name: unknown
page_number: unknown
broadcast_date: unknown
broadcast_time_window: unknown
recording_carrier: VHS / Betamax / PC capture / broadcaster tape / screenshot
receiver_or_decoder: unknown
recovery_tool: null
recovered_at: null
artifact_hash: null
confidence: low
```

这仍然只是 schema idea，不在本轮修改正式 evidence schema。

---

## 5. `broadcast-page state`：同一个页号也不是一个稳定页面

Web URL 容易让人产生“同一个地址 = 同一个对象”的错觉；teletext 页号同样会产生这种错觉。

实际上：

```text
page 301 at 14:05
!= page 301 at 14:20
!= page 301 tomorrow
```

广播端可以持续改写同一页号的 payload。

因此未来证据不能只写：

> `page=301`

而应该尽量写：

> `page=301 + broadcaster + channel + date/time window + recovered cycle`。

这与 OWA 的“同 URL 不同年月不能默认同一 representation”原则完全平行。

可命名为：

> **`broadcast-page state`**

---

## 6. `carousel-order state` 与 `carousel latency`

Teletext Archaeologist 的 Teletext Player 特意按原广播顺序重放恢复数据；关闭 cache 时，用户必须等待目标页再次在数据流中出现。

来源：

- <https://teletextarchaeologist.org/software/>

这说明完整的历史体验至少包括：

- 页面集合；
- 页面发送顺序；
- 重复频率；
- subpage 顺序；
- 一个完整轮播需要多长时间。

如果只保存最终解码出的静态 PNG/HTML，可能已经丢失：

> **`carousel-order state`**

也丢失：

> **`carousel latency`** —— 用户从输入页号到真正看到页的等待。

因此一个现代“所有页瞬间可点”的 teletext archive 可以非常适合内容研究，却仍不是完整的 historical interaction reconstruction。

---

## 7. `receiver-state gap`：同一广播信号，不同终端可能产生不同可见世界

1994《人民日报》同时提到两类接收端：

1. 专用图文电视机；
2. 微机接收卡。

2003 搜狐回顾也明确说需要特殊接收装置。

因此 future case 至少应记录：

- receiver 是否支持对应制式；
- 字符集/中文支持；
- 是否缓存页面；
- 是否支持 subpage；
- PC 卡是否能保存原始文件还是只保存渲染结果；
- 分辨率/字体/字符发生器；
- 是否能打印；
- 接收信号质量与误码。

可命名：

> **`receiver-state gap`**

同一广播服务的历史 artifact，不等于每户电视当时看到同一个结果。

---

## 8. `broadcast-time / observation-time gap`

对 Wayback，至少会记录 `Memento-Datetime`。

对 teletext，真实时间可能有：

1. 编辑者修改页面；
2. encoder 将新页放入轮播；
3. 广播发射；
4. 某台接收机捕获；
5. 本地 cache 更新；
6. 用户查看；
7. VHS/VCR 记录下包含数据的信号；
8. 数十年后 recovery tool 从磁带重新解码。

所以 recovery artifact 的 `recovered_at=2026` 完全不等于 `broadcast_at=2026`。

未来应显式拆：

```text
broadcast_datetime
recording_datetime
recovery_datetime
research_accessed_at
```

不能只保留一个 `date` 字段。

---

## 9. `signal-survival gap`：节目录像存在，不等于隐藏数据还存在

Teletext Archaeologist 明确提醒：

- 第一代录像带最好；
- 多次复制会模糊 teletext 信号；
- 某些 time-base corrector 会用自己的信号覆盖原 teletext data；
- 很多历史页面只能从保存状况足够好的家用录像恢复。

来源：

- <https://teletextarchaeologist.org/about/>
- <https://teletextarchaeologist.org/>

所以未来如果得到一盘 1996 年 CCTV VHS：

```text
video programme is visually replayable
```

也不能直接推导：

```text
teletext/data layer is recoverable
```

这可记作：

> **`signal-survival gap`**

与 Web 的“HTML 在、图片 404”类似，但发生在模拟信号层。

---

## 10. `decoded-representation gap`：恢复出来的 HTML 不是历史 Web 页

现代 teletext archive 常把恢复数据渲染成 HTML，方便搜索、浏览和比较。

这个 HTML 很有研究价值，但必须标记：

```text
modern HTML viewer != historical HTTP resource
```

更准确的 provenance 是：

```text
historical broadcast signal
→ videotape/PC capture
→ modern recovery software
→ decoded packet/page data
→ modern HTML renderer
```

所以如果将来把海外 teletext recovered HTML 与中文 Web 页面放在同一数据集，必须避免 `evidence_type=archived-page` 产生误解。

建议至少写：

```yaml
evidence_type: recovered-broadcast-page
reconstruction: true-or-derived
historical_transport: broadcast
modern_render_transport: http
```

这里的 `reconstruction/derived` 语义还需要与仓库正式 schema 讨论，本轮不直接定规范。

---

## 11. `content-provenance crossover`：同一内容可能跨广播、专网、Web 投影

1994《人民日报》已经说明，新闻稿和经济信息可通过图文电视发送。

而仓库上一轮 ChinaMail note 已经建立另一个并行渠道：X.400/MHS/ChinaMail 的电子信箱与 Web/Internet 在 1995 前后可以同时存在。

因此 1995—2000 中文旧网的内容 provenance 不应默认是：

```text
newsroom → Web CMS → web page
```

可能还有：

```text
newsroom/database
├─→ teletext/data broadcast
├─→ proprietary mailbox / ChinaMail
├─→ fax / wire feed
└─→ Web
```

如果未来在 Web archive 中找到一份和电视数据页文字高度相同的稿件，不能仅凭相同正文推定“网页是原件、teletext 转抄网页”。

方向可能相反，也可能两者来自同一上游编辑系统。

可命名：

> **`content-provenance crossover`**

---

## 12. 海外 control：Ceefax 说明“同一架构”可以有完全不同的社会分布

Ofcom 的 2024 历史回顾记录：Ceefax 页面有页号，用户用遥控器进入；服务高峰达到约 2200 万周用户，体育比分是典型日常用途。

来源：

- <https://www.ofcom.org.uk/tv-radio-and-on-demand/bbc/marking-50-years-since-ceefax-the-horse-drawn-internet-was-launched>

Guardian 的回顾补充，1974 年刚开播时只有约 6000 户有兼容电视，而后设备普及才推动用户增长。

来源：

- <https://www.theguardian.com/tv-and-radio/2022/oct/20/ceefax-is-dead-long-live-ceefax-meet-the-fans-resurrecting-the-ingenious-service>

这个 control 的作用不是“外国更先进”的线性比较，而是证明：

> **技术架构存在不能告诉我们实际社会规模。receiver distribution 才是关键变量。**

当前中国证据更强地证明 institutional/data-distribution use 和 receiver development；还没有同等级的 household penetration 数据。

---

## 13. 海外 artifact：Jobfinder 把 broadcast page 直接接到就业机会

Rewind 的电视档案记录 Central Television 1986 年 Jobfinder：正常节目结束后，以 teletext/in-vision 形式播出工作信息；档案页面提供 1986-09-30 的具体播出对象。

来源：

- <https://rewind.thetvroom.com/24367/channel-presentation/central-closedown-30th-september-1986/>

这告诉我们，如果研究问题是“Web 招聘出现以前，数字/电子信息怎么进入找工作”，teletext 是真实可比较对象。

但目前没有取得中国普通求职者用图文电视找工作的同时代材料，所以本 note 不把 Jobfinder 的用途投影到中国。

---

## 14. Archive bias：为什么 Web 会在后来显得比当时更大

Web archive 的基本抓取对象是 HTTP/URL。

Teletext 的典型对象不是 URL。

因此今天的研究者会面对一个结构性偏差：

| 1990s 实际信息渠道 | 今天常见保存入口 |
|---|---|
| Web | Wayback/Common Crawl/站长备份，较高可见性 |
| BBS/论坛 | 部分页面、数据库备份、转载，碎片化 |
| proprietary mailbox | 极低；账号与消息通常私有 |
| teletext/data broadcast | 极低；需要录像/VBI/PC capture 等特殊残存 |
| fax | 个体纸张/机构档案，难集中检索 |
| pager | 后台与空中消息几乎不留公开档案 |

因此不能从：

> “1997 年我今天能找到很多网页，却很少找到 teletext 页面”

推出：

> “1997 年普通人的数字信息主要发生在 Web。”

这属于：

> **`archive-medium selection bias`**

---

## 15. 对 M4 archive-gap model 的潜在字段

如果未来 M4 做资源类型缺失模型，可以考虑新增：

```yaml
historical_transport:
  - http
  - telnet
  - dialup-bbs
  - proprietary-mailbox
  - teletext-broadcast
  - tv-data-broadcast
  - fax
  - pager

original_representation:
  - html
  - terminal-stream
  - teletext-packet
  - broadcast-file
  - raster-video
  - paper

survival_carrier:
  - archive-capture
  - server-backup
  - user-local-file
  - screenshot
  - videotape
  - broadcaster-master
  - printout
  - later-transcription
```

这只是研究 note 中的建议，不代表本仓 schema 已接受这些 enum。

---

## 16. 中国 artifact 当前状态

本轮准确状态：

```text
historical Chinese technical/service identity: achieved
1994 contemporaneous operational-use evidence: achieved
PC receiver-card workflow evidence: achieved
1994-04-20 Internet boundary: achieved
later 1994-11-28 launch locator: achieved, retrospective only
exact Chinese teletext page artifact: NOT achieved
exact page number / carousel snapshot: NOT achieved
raw broadcast/VBI packet capture: NOT achieved
historical receiver manual: NOT achieved
verified 1995-2000 Chinese teletext recording: NOT achieved
M1 complete case: NOT applicable / NOT achieved
```

特别注意：本轮没有找到一份可以实际解码和校验的 1994—2000 中国图文电视原始页面。

所以不能写：

> “我们已经复原了 1994 年 CCTV 图文电视。”

只能写：

> “我们已经确认 1994 年存在实际运行的服务/用途，并建立了以后遇到 artifact 时的证据模型。”

---

## 17. Evidence table

| ID | Evidence | Grade | Supports | Does not support |
|---|---|---|---|---|
| E1 | 《人民日报》1994-09-27 | A- | operational data-broadcast use; PC receiver workflow | household popularity |
| E2 | CNNIC Internet timeline | B | 1994-04-20 full Internet connection boundary | consumer adoption |
| E3 | 搜狐《电视百年》2003 | C | retrospective 1994-11-28 launch/date claim; receiver bottleneck | exact contemporaneous service state |
| E4 | Ofcom Ceefax history | C/B institutional retrospective | UK page-number UX and scale | China scale |
| E5 | Teletext Archaeologist archive/method | B + derived artifacts | VHS recovery path, incomplete broadcaster preservation | any specific Chinese page |
| E6 | Rewind 1986 Jobfinder catalog | B / archival catalog | job information as teletext use | Chinese use |

---

## 18. 已证实 / 高概率 / 不知道

### 已证实

- 1994-09 中国同时代报刊报道实际图文电视数据广播用途；
- CCTV 被报道用于新闻稿、经济信息分发；
- PC receiver card 可把广播数据恢复成文件并存储/显示/分析/打印；
- 这种服务不是 Internet，1994-04-20 全功能 Internet 节点必须独立记录；
- 海外 teletext 可以从录像带残留信号恢复，且现代 archive 已有大量日期化服务快照。

### 高概率但仍需更强原始证据

- 1994-11-28 是 CCTV 正式图文电视节目开播节点；
- 1990s 中国若存在家用录像保留相关广播，部分隐藏数据可能在适当录制/保存条件下仍可恢复；
- 1995—2000 一些新闻/经济内容可能跨 teletext、专有电子信箱与 Web 共用上游内容源。

### 不知道

- 1994—2000 中国具体服务页号与页数；
- carousel 周期、subpage 和更新时间；
- receiver 字符集和兼容差异；
- 用户规模与家庭渗透率；
- 是否已有任何公开的中国原始 VBI/teletext packet dump；
- 哪些 VHS/Betamax/广播机构母带还能恢复数据；
- 图文电视内容与早期中文 Web 具体页面之间是否有可证明的内容继承链。

---

## 19. Privacy / copyright / reconstruction boundary

- 不需要也不应恢复私人账号数据；teletext 本身主要是广播内容，但版权仍归原内容权利人；
- 若获得录像带，仓库优先保存 metadata、hash、技术测量和必要的小型研究截图，不默认重新分发整段节目；
- 从 VHS 恢复出的 page 必须标注 `recovered/derived`，不能称为“原始 HTML”；
- 若现代工具修复坏字符、补页或合成完整轮播，必须明确标 reconstruction；
- 任何海外 artifact 不能冒充中国 artifact。

---

## 20. 下一步：真正值得做的 artifact work

优先级：

1. 查《中国广播电视年鉴》1994—2000 的图文电视条目，找具体台站、设备、页数、用户/接收机数据；
2. 查 1994—1998 电视机/图文解码器/PC 接收卡说明书、广告、价目表；
3. 找中国同时代页面照片、页码表、演示录像；
4. 调查是否有国内电视史/录像收藏者保留 PAL 录像原带，确认 VBI 是否仍可读取；
5. 若得到录像，先建立 provenance + hash + recording chain，不直接做“漂亮复原”；
6. 对 1995—2000 同一新闻事件，尝试建立 `teletext → ChinaMail/proprietary service → Web` 的同内容多渠道 evidence chain；
7. 若没有原 artifact，停止在 research note，不人为制造一个“1994 CCTV teletext screenshot”。

---

## 21. 本轮结论

对中文旧网考古最重要的不是把 teletext 纳入“互联网家谱”，而是接受一个更麻烦的事实：

> **1995 年前后的数字信息世界并不都长成 URL。**

一个人可能在电视/PC 卡上选择编号页面、等待广播轮播、保存文件；另一个人拨 BBS；第三个人用 ChinaMail；第四个人已经打开了 Web。

今天 Wayback 最容易让第四种生活留下证据。

如果不主动建模这些 non-Web representation，旧网考古会在无意中把“最容易被 Web archive 保存的生活”误写成“当时最主要的数字生活”。
