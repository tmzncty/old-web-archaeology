# 视聆通：围墙网络里的个人主页与“可见但不在 Internet 上”（1995–2000）

> Status: **bounded research note / hosting-environment probe**, not a complete M1 case.
>
> Scope: 广东“视聆通”（后常与 169 多媒体通信网联系）早期个人主页服务。重点不是写一篇视聆通通史，而是确认一个旧 Web 保存研究容易忽略的边界：**页面存在、用户能访问、甚至形成公共文化影响，并不自动等于该页面当时位于全球 Internet 可路由/可抓取的 Web 上。**

## 0. 为什么现在研究它

仓库 `ROADMAP.md` 的 M1 仍缺完整个人主页/托管案例，M3 还要求解释历史浏览环境。现有研究已经覆盖网易个人主页的免费→收费托管、BlogCN/BlogBus 的平台失踪链、Discuz charset 等，但默认研究对象大多已经处于 Internet HTTP/DNS 世界。

视聆通提供一个更早、也更棘手的状态：

```text
page exists
!= globally Internet-reachable page
!= archive-crawlable page
!= public-Web URL
```

它因此适合补“托管环境”而不是再写一个平台兴衰故事。

---

## 1. 1995-12-29：广州开通视聆通；后来运营方材料称当时即有个人主页服务

广东电信 2018 年回顾材料（由搜狐转载）称：

- 1995-12-29，“视聆通”商用试验网在广州开通；
- 用户通过拨打 `96330` 接入；
- 当时提供家庭教育、娱乐、金融、房产、图书馆数据库等信息服务；
- 同时提供个人主页服务；
- 1998-01-23 又开通视聆通宽带网，并与原窄带网联网。

来源：

- 广东电信回顾材料（2018，搜狐转载）：<https://www.sohu.com/a/273727424_161794>

Evidence:

- grade: **C / institutional retrospective**
- supports:
  - 运营方后来的历史叙述把个人主页列为视聆通早期服务之一；
  - `96330` 是当时接入方式的重要 locator；
  - 1998 年发生过窄带/宽带环境演进。
- does **not** prove:
  - 1995-12-29 当天个人主页功能已经对所有用户正式开放；
  - 主页使用 HTTP、何种 hostname/path；
  - 页面可以从全球 Internet 直接访问；
  - charset、服务器软件或浏览器要求。

这里不能因为来源来自运营方就自动升级为 A：它是 2018 年的机构回顾，不是 1995 年保存下来的原始公告或页面。

---

## 2. 2001 年同期采访：视聆通被实施者描述为 169 多媒体通信网、全中文多媒体服务网络

2001-09-01，《南方都市报》对广东泰信实业总裁孙政权的采访保存了较接近运营侧的说明：

- 视聆通/169 始于 1995 年；
- 1996 年正式开通广东视聆通多媒体网；
- 它被描述为面向计算机用户的、全中文化的多媒体信息服务系统；
- 采访同时说 2000 年前后 163 与 169 已完成合并。

来源：

- 南方都市报，2001-09-01，新浪转载：<https://tech.sina.com.cn/it/m/2001-09-01/82860.shtml>

Evidence:

- grade: **B**（近同时代媒体采访；受访者是项目实施方管理者，但不是原始技术文档）
- supports:
  - 视聆通与 169 多媒体通信网的运营/品牌联系；
  - 它不是单纯一个普通网站，而是一套接入与内容服务环境；
  - 1990 年代末到 2000 年发生了网络环境重组。
- uncertainty:
  - “始于 1995”与“1996 正式开通”的差异可能对应试验网/正式网，需原始公告解决；
  - “163/169 合并”不能直接推出某个具体个人主页 URL 在某天完成迁移。

---

## 3. Carboy / 杨震霆：个人主页真实存在，但参与者明确记得早期视聆通不能出 Internet

杨震霆（Carboy）是早期视聆通个人主页用户。2000-12-14，他以第一人称回顾：

- 1996 年初广东视聆通为用户提供免费个人主页；
- 他是首批申请者之一；
- “完全上网手册”最初即在该环境建立；
- 他当时认为视聆通“不能出 Internet”，因此又寻找其他主页托管环境；
- 广州飞捷随后也提供免费个人主页服务。

来源：

- 杨震霆，《中国最早的“十佳个人主页”流落何处》，2000-12-14，新浪科技：<https://tech.sina.com.cn/r/m/46310.shtml>

Evidence:

- grade: **C / participant retrospective, near-period**
- strong for:
  - 当事人的使用经验；
  - 视聆通个人主页确实进入真实用户实践；
  - 用户感知到“视聆通内部可用”与“Internet 可达”之间存在边界。
- not sufficient for:
  - 精确网络拓扑；
  - 主页服务器 IP、DNS、URL；
  - 所有时期视聆通都不能访问 Internet；
  - 所有视聆通个人主页都永远只在封闭网内。

2005 年，杨震霆再次回忆自己 1995 年通过视聆通上网，并说后来才知道它当时只能在广东省内视聆通站点漫游、不能出 Internet；同文把 1996 年的“完全上网手册”后来地址写为 `carboy.163.net`。

来源：

- 《我的互联网10年故事组——Carboy》，2005-11-11，新浪科技：<https://tech.sina.com.cn/i/2005-11-11/1558763832.shtml>

Evidence:

- grade: **C**
- supports:
  - 同一参与者多年后仍稳定地区分早期视聆通内部环境与 Internet；
  - “完全上网手册”后来存在于 Internet hostname `carboy.163.net`。
- caution:
  - 不能据此把 `carboy.163.net` 倒推成 1996 最初视聆通主页 URL；
  - 这很可能是后续托管/迁移后的 locator。

---

## 4. 一个重要的时间冲突：1995 商用试验 vs 1996 正式开通

当前来源出现两种表述：

```text
1995-12-29  广州“商用试验网”开通（2018 广东电信回顾）
1996        广东视聆通多媒体网“正式开通”（2001 实施方采访）
```

这不应被强行裁成一个日期。

最小解释模型是：

```text
trial/commercial trial launch
!= formal network launch
!= personal-homepage feature launch
!= first user page creation
```

在找到 1995/1996 原始公告、资费表、用户手册或报刊之前，仓库不应声称“视聆通个人主页准确于 1995-12-29 正式上线”。

---

## 5. 对旧 Web 考古最重要的结论：需要增加“网络可达域”字段

常规 Web archaeology 容易把 URL/capture 当作起点：

```text
hostname -> HTTP -> page -> subresources -> replay
```

视聆通说明更早的一层必须被记录：

```text
access network
    ↓
routing / reachability domain
    ↓
name resolution / host locator
    ↓
HTTP or other application service
    ↓
page
```

因此建议未来 `evidence.schema.json` / site dataset 至少考虑：

```text
access_scope:
  - global_internet
  - isp_walled_garden
  - regional_network
  - intranet_like
  - unknown

external_reachability:
  status: verified | reported | unknown
  evidence_grade: A | B | C | D

locator_scope:
  hostname: unknown
  path: unknown
  requires_provider_access: unknown
```

这些只是 schema 建议，不代表当前已经证明视聆通应永久归入某一个固定类型；网络能力会随时间变化。

---

## 6. “完全上网手册”的迁移不能被压成一个 URL

当前可以建立的最保守链条是：

```text
1996 左右：
视聆通内部个人主页（participant-reported）
        ↓
用户因 Internet 可达性限制寻找其他托管
        ↓
后续 Internet-hosted incarnation(s)
        ↓
carboy.163.net（后来的明确 locator）
```

但目前缺：

- 初始视聆通主页 URL/path；
- 是否存在从视聆通到飞捷的完整迁移；
- 哪些文件/页面被复制；
- 是否保留原目录结构；
- `carboy.163.net` 最早出现日期；
- 是否有 redirect，还是人工搬家；
- 图片、下载文件、留言/计数器等动态状态是否一起迁移。

所以不能声称：

> “完全上网手册 1996 年的网址就是 carboy.163.net。”

更准确的是：

> 参与者材料证明作品/站点身份跨越了多个托管环境；现阶段只能确认后期 Internet locator，初始 locator 尚未恢复。

---

## 7. 为什么 Wayback 缺失在这里尤其不能直接解释为“页面没存在过”

如果一个页面只在 ISP/区域封闭网络中可达，则公共 Web crawler 理论上可能根本没有路由条件进入它。

因此：

```text
no public archive capture
!= page did not exist
```

还可能是：

```text
page existed
+ users inside provider network could access it
+ public crawler could not route to it
```

这是 **D 级方法推断**。当前参与者回忆与运营侧材料让它成为合理研究假设，但在找到原始拓扑、用户手册、地址样本或同时代抓取记录前，不能把某一具体视聆通页面的 archive absence 全部归因于网络隔离。

---

## 8. 可复原程度

### 当前可以较可靠复原

- 视聆通是接入网络 + 内容/多媒体服务环境，而不只是一个普通门户页面；
- 1990 年代中期它实际提供过个人主页服务；
- 至少一位重要早期用户把自己的主页实践起点放在视聆通；
- 参与者明确记忆到早期环境存在 Internet 可达性边界；
- 后续出现 169/163 网络重组与主页向 Internet hostname 迁移的历史背景。

### 当前只能部分复原

- 1995/1996 的上线阶段；
- 个人主页申请与发布流程；
- 主页从封闭/区域网络迁往 Internet 的机制。

### 当前不能复原

- 原始主页 URL scheme；
- DNS/host naming；
- HTTP headers/status；
- charset；
- HTML/DOM；
- 浏览器版本要求；
- CGI/留言板/计数器；
- 图片和下载资源树；
- 服务端软件；
- 精确路由拓扑。

因此本 note **不满足 M1 complete case**。

---

## 9. 证据分级表

| 时间 | Claim | 等级 | 来源 | 定位/说明 |
|---|---|---:|---|---|
| 1995/1996（后述） | 视聆通早期提供个人主页服务 | C | 广东电信 2018 回顾 | 1995-12-29 商用试验网段落 |
| 1995–2000（2001 采访） | 视聆通/169 是全中文多媒体服务网络，后经历 163/169 重组 | B | 南方都市报 2001-09-01 | “抓住机会 一举成名”“重塑品牌” |
| 1996（2000 回忆） | Carboy 是早期个人主页用户；当事人感知视聆通不能出 Internet | C | 杨震霆 2000-12-14 | 开头个人主页发展回忆 |
| 1995/1996（2005 回忆） | Carboy 通过视聆通接入，并再次描述只能省内漫游 | C | 新浪 2005-11-11 | “互联网十年故事”第一段 |
| 后期 locator | `carboy.163.net` 是“完全上网手册”的后期地址 | C | 新浪 2005-11-11 | 人物简介段 |
| 未验证 | 公共 crawler 因网络边界无法抓取某具体主页 | D | 本研究推断 | 需原始网络/locator 证据 |

### A 级缺口

本轮 **没有取得 A 级 1995–1998 原始 artifact**。这是结论的一部分，而不是应被掩盖的问题。

优先寻找：

1. 1995-12/1996 视聆通原始开通公告或资费/用户手册；
2. 原始个人主页申请说明；
3. 至少一个历史用户主页 locator；
4. 同时代报刊截图/印刷材料中的 URL 或拨号后菜单；
5. 163/169 合并时的原始迁移公告。

---

## 10. 建议写入位置

当前先保留在：

- `research/shilingtong-walled-garden-homepages-1995-2000.md`

取得 A 级 artifact 后，可进一步用于：

- M1 个人主页/主页托管完整案例；
- `studies/platform-genealogy.md` 的前平台托管阶段；
- `datasets/platforms.csv` 的 access-scope / URL ownership 字段；
- M3 的“历史网络环境不是只有浏览器版本”实验说明。

不建议现在就修改 ROADMAP 勾选 M1。

---

## 11. 下一轮 bounded probe

只做以下工作，避免继续泛搜怀旧材料：

1. 搜索 1995–1997 报刊、邮电系统资料中的视聆通用户手册/资费表/个人主页申请说明；
2. 搜索早期书籍/杂志是否印有视聆通主页 URL；
3. 对 `carboy.163.net` 做最早 capture locator 检查，确定它最迟何时已成为 Internet 地址；
4. 如果能找到一个初始视聆通 locator，先判断它属于 IP、内部 hostname、公共 DNS 还是其他命名体系；
5. 不因 archive absence 自动声称页面被删除。

Stop condition：如果始终只能得到参与者回忆而无原始 locator/页面/手册，则把“原始页面不可从公共 Web archive 直接恢复”作为保存边界，不伪造 reconstruction。

---

## 12. 隐私与版权边界

- 不批量搜集或重新发布普通用户旧个人主页；
- 若发现历史用户目录，只抽取证明托管结构所需的最小 locator/metadata；
- 不通过旧用户名反查现实身份；
- 报刊/书籍/截图只记录 citation 与必要事实，不把整页扫描件提交仓库；
- 如未来找到原始 HTML/图片/程序，只在许可明确时保存内容；否则记录 archive locator、hash、headers 与结构 metadata；
- 已删除的私人内容不因“考古价值”自动获得重新公开的正当性。

---

## 13. 本轮最小结论

> 视聆通提醒我们：中文旧网的早期“个人主页”并不总是从全球 Internet 的 DNS + HTTP 空间开始。至少在 1990 年代中期广东的实际用户经验中，个人主页可以先存在于运营商提供的区域/围墙式网络环境，再随用户和服务演进进入更公开的 Internet 托管空间。

这意味着保存研究必须问的不只是“URL 还在不在”，还要先问：

> **这个 URL/页面在那个时间点，究竟对哪一张网络可见？**
