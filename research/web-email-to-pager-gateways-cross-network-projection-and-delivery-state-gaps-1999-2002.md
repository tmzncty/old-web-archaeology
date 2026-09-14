# Web / Email → Pager：跨网络投影、网关状态与寻呼投递缺口，1999—2002

> 性质：`old-web-archaeology` research note。  
> 研究对象：1999 年前后中文 Internet / Web / email 与无线寻呼网络之间的 gateway。  
> Scope 说明：本文不把仓库扩大成“无线寻呼史”；只研究**直接进入 1995—2015 中文旧网范围的 Web / Internet 接口、服务语义、历史 URL 与 archive state gap**。  
> 当前状态：**不是 M1 complete case**。已经确认同期服务存在和用户使用，但尚未取得“国信网源 / 网上寻呼”的精确历史 URL 与可打开核验的 historical memento。

---

## 0. 去重与为什么值得单独建 note

本轮先读取：

- 当前 HEAD 与最近提交；
- `ROADMAP.md`；
- `docs/METHOD.md`；
- HPL 的 `METHODOLOGY.zh-CN.md` / life-horizons index / roadmap；
- 已有 `research/`；
- 上一轮 CFido 交叉研究。

仓内检索 `寻呼` / `BB机` / `pager` / `paging` 没有独立案例。

这个对象和已有 email、BBS、mobile Internet、transaction-state gap 并不重复，因为这里出现的是一种非常具体的历史结构：

```text
Web / email 是输入网络
无线寻呼是输出网络
pager 是最终终端
```

因此历史网页不是最终内容目的地，而可能只是**另一套通信网络的控制面**。

---

## 1. Claim list

本 note 只主张以下最小结论：

1. 1999 年中国确实存在把 Internet / Web 与公共无线寻呼网络连接起来的服务；
2. 1999 年底，国信寻呼已在 198/199 全国网、27 个省网及部分本地网开通“网上寻呼”，22 个省网开通“电子邮件到达呼”；
3. 1999 年腾讯 / SINET 的邮件增值系统明确可以把 email 内容路由到 paging station；
4. CNNIC 以 1999-12-31 为截止日的网民调查里，“网上寻呼机”已经作为一项实际网络服务被用户选择；
5. 因而一个历史 Web 页面可能只是 `Internet → paging network` 的入口；
6. 即使历史 form 被完整 archive，也通常不能证明某一条 page 最终通过无线网络成功送达 pager；
7. 当前仍没有足够证据把“国信网源”写成完整 M1 historical Web case。

不主张：

- 1999 年所有寻呼用户都用过 Web 寻呼；
- “网上寻呼”已经大众化到全国人口；
- 当前腾讯页面就是 1999 年原 HTML；
- 搜索到服务名就等于知道历史 URL；
- Web form 可打开就等于 backend、radio network 和 receiver state 都被保存。

---

## 2. A 级同期机构证据：1999 年通信业统计公报

信息产业部综合规划司的 1999 年通信业统计公报（2000 年发布，新浪同期转载）记录：

- 中国联通国信寻呼覆盖 335 个地市、2022 个县市；
- 280MHz 198/199 覆盖全国 287 个城市，容量 1700 万户；
- 国信公司开通“国信网源”网站；
- 截至 1999 年底，“网上寻呼”已经开通 198/199 全国寻呼网、27 个省网和部分本地网；
- “电子邮件到达呼”已经开通 22 个省网；
- 同一公报还说明 VSAT 数据通信被用于全国联网寻呼等业务。

来源：

- 《一九九九年通信业发展统计公报（摘要）（下）》  
  https://tech.sina.com.cn/it/2000-06-14/28155.shtml

Evidence grade：**A（同期官方统计公报，转载 artifact）**。

这个来源证明的是：

> 1999 年底已经存在一套 Internet/Web/email 与 public paging network 相连的服务架构。

它没有告诉我们：

- `国信网源` 的精确 URL；
- Web form 的 HTML；
- 用户字段；
- POST endpoint；
- authentication；
- message length；
- 是否收费；
- sender / pager ID schema；
- actual delivery confirmation。

---

## 3. A/B 交界证据：腾讯保存的 1999-07-11 corporate news

腾讯当前 corporate archive 中有一篇标注 **1999-07-11** 的新闻：Tencent 与 SINET 合作，在深圳电信网络试运行 email value-added service。

页面描述：

- 服务面向 ISP dial-up users；
- email 到达后系统提取 sender address、subject、content；
- 若满足用户自定义规则，内容可送到 paging station 或 GSM SMS system；
- 也可以转到 fax；
- 用户通过 username / password 设置禁止呼叫时段、过滤时段、字符串过滤等规则。

来源：

- Tencent corporate archive：  
  https://www.tencent.com/en-us/articles/80260.html

证据处理必须拆开：

```text
statement date = 1999-07-11
current page artifact = contemporary Tencent corporate website
```

因此：

- 对“腾讯今天以官方身份归档并标注这一 1999 新闻”可以高 confidence；
- 对“1999 年事件/产品说明”可作为强 A/B evidence；
- 但**不能**把今天的 HTML DOM、CSS、URL layout 当成 1999 原页结构。

这正是 OWA METHOD 所要求的：**historical statement != historical page artifact**。

---

## 4. 第二个 evidence family：CNNIC 证明它进入了真实网民服务菜单

CNNIC 于 2000-01-18 发布的《中国互联网络发展状况统计报告》以 1999-12-31 为截止日期。

报告记录：

- 上网计算机 350 万台；
- 上网用户 890 万；
- 在线问卷中，“用户最常使用的网络服务（多选）”里，`网上寻呼机` 为 **13.17%**。

来源（CNNIC 同期报告转载）：

- https://tech.sina.com.cn/news/internet/2000-01-18/15795.shtml

Evidence grade：**A/B（CNNIC 同期统计报告；问卷方法本身具有 selection bias）**。

这条证据非常重要，因为它把：

```text
运营商宣布服务存在
```

推进到：

```text
部分真实 Internet 用户把“网上寻呼机”列为自己常用的网络服务
```

但必须保留 sampling boundary：

- 这是网上联机问卷；
- 是 Internet 用户样本，不是全国人口；
- “13.17%”不是 pager population share；
- 也不能辨认具体服务商。

---

## 5. 新对象模型：`cross-network projection / 跨网络投影`

普通静态网页可以粗略理解成：

```text
HTTP request
→ Web server
→ HTML representation
```

网上寻呼更接近：

```text
browser / email client
→ Web form / mail gateway
→ authentication / filtering rule
→ paging gateway
→ paging station backend
→ radio transmitter network
→ pager ID matching
→ receiver display / beep
→ optional human callback via phone
```

因此历史网页只是整条系统的一个层。

可以定义：

> **`cross-network projection`**：一个网络中的状态、消息或动作被 gateway 转换并投影到另一套通信网络和终端，而不是在原 Web session 内闭环。

在这里：

```text
Internet message state
→ paging delivery request
→ radio-side state
```

三个状态不能合并。

---

## 6. 新 archive gap 一：`gateway-state invisibility / 网关状态不可见`

假设未来取得一个 1999 年“网上寻呼”页面：

```html
[pager id]
[message]
[send]
```

Wayback 能保存这个 form，也仍然可能完全不知道：

- `action=` 指向哪个 CGI / servlet；
- POST body 当时是什么；
- backend 是否要求 session；
- pager number 是否有效；
- gateway 是否接受请求；
- gateway 怎样映射省网 / 全国网；
- 是否进入 message queue；
- 是否因为过滤、资费或权限被拒绝。

因此：

> **`captured form != preserved gateway state`**

这和普通“页面资源缺图”是完全不同的丢失类型。

---

## 7. 新 archive gap 二：`delivery-state invisibility / 投递状态不可见`

即使 gateway 返回：

```text
发送成功
```

也不能自动写成：

```text
pager 已收到
```

可能的状态链至少包括：

```text
request accepted
→ gateway routed
→ paging station queued
→ transmitter broadcast
→ receiver in coverage
→ receiver matched pager ID
→ receiver displayed / alerted
→ human noticed
```

早期一向 paging 往往没有 end-to-end acknowledgment。

因此需要定义：

> **`delivery-state invisibility`**：Web / gateway 能观察到“提交”或“接受”，档案却无法从页面本身验证物理无线投递和人的接收状态。

如果未来复原 UI，按钮下出现的任何“发送成功”文案，都必须明确它在历史系统中到底意味着哪一级成功。

---

## 8. 新 archive gap 三：`recipient-state loss / 收件端状态丢失`

Web archive 最容易保存发送者一侧，最难保存 pager 一侧。

历史接收端可能具有：

- pager ID / 呼号；
- 数字机或汉字机型号；
- 屏幕字符宽度；
- 本地消息存储上限；
- 滚屏 / 翻页行为；
- 音响 / 振动模式；
- coverage；
- roaming / nationwide paging capability；
- 服务费与套餐状态。

即使 form 与 server response 都保存下来：

> **receiver UI 仍可能完全不可见。**

这意味着真正做历史浏览体验时，研究单位不再只是：

```text
site × browser × time
```

而至少是：

```text
Internet control surface
× gateway semantics
× paging network
× receiver class
× time
```

---

## 9. Web archaeology 中一个容易被忽略的事实：旧 Web 可以控制 Web 之外的世界

如果研究者只看 HTML，会倾向于把早期 Web 当成“阅读网页”的媒介。

1999 年网上寻呼说明，中文 Web 已经能够作为：

> **另一套物理通信基础设施的远程控制面。**

类似对象以后应该主动寻找：

- Web → pager；
- Web → fax；
- email → SMS；
- Web → voice call；
- Web → postal / delivery request；
- Web → bank / booking backend。

它们共同要求 OWA 把研究对象从：

```text
页面长什么样
```

扩大到：

```text
页面连接了什么真实系统
```

但每一条都必须有同期证据，不能从现代 API 结构倒推。

---

## 10. 1999 年的“国信网源”：identity achieved，URL unresolved

当前能 A 级确认：

```text
service/site label = 国信网源
operator = 中国联通国信寻呼（1999 语境）
function includes = 网上寻呼 / email 到达呼
period = at least by end-1999
```

但本轮常规 Web 检索仍没有恢复出：

- exact hostname；
- original URL；
- page URL pattern；
- archive capture；
- historical screenshots。

因此准确状态是：

```text
historical service identity: ACHIEVED
historical operator identity: ACHIEVED
contemporaneous functionality: ACHIEVED
exact historical URL: NOT ACHIEVED
verified historical memento: NOT ACHIEVED
second historical timepoint: NOT ACHIEVED
M1 complete case: NOT ACHIEVED
```

不能写：

> “Wayback 没保存国信网源。”

只能写：

> **本轮仍未恢复 exact historical URL，因此尚未形成可直接检索/核验的 capture locator；capture absence unknown。**

---

## 11. Tencent archive 也不能当作 M1 capture

腾讯当前页面很珍贵，因为它保存了：

- 精确日期；
- 产品工作流；
- pager / GSM / fax 三种输出；
- username/password；
- filter / quiet period；
- paging station 这一 backend component。

但它不能证明：

- 1999 年 Tencent 网站的 DOM；
- 1999 年新闻页 URL；
- 当年 charset；
- 当年 CSS / layout；
- 当年这篇稿件是 HTML、新闻数据库还是其他发布形式；
- 当前页面正文是否经过后续 CMS migration / 翻译。

所以它是一个很强的**historical content provenance**，不是 historical capture。

---

## 12. 海外协议 artifact：SNPP 让“Web / Internet → Pager”不再只是产品宣传

1994 年 1 月 RFC 1568、7 月 RFC 1645 定义 Simple Network Paging Protocol。

RFC 1645 的 abstract 明确说：

- 目标是从 Internet 侧向 radio paging terminals 发送 numeric / alphanumeric one-way pages；
- 支持该协议以及 SMTP 的 gateways 已经实际用于 nationwide paging and messaging；
- Unix / Windows 的 email filters 与 SNPP client software 已经存在。

来源（原始协议文档，A 级）：

- https://www.rfc-editor.org/info/rfc1568/
- https://www.rfc-editor.org/rfc/rfc1645.html

这说明：

> Internet-to-pager gateway 是 1990 年代通信史中的真实跨网络架构，不是中国运营商自己发明出来的营销说法。

美国 1995 年《Washington Post》又说明，当时约 3000 万 pager 用户最常见的普通用法仍然是收到 callback number；two-way pager 的新意义之一就是能直接回简短消息，不再需要找电话。

来源：

- https://www.washingtonpost.com/archive/business/1995/12/04/how-it-works/8f72080b-8e47-4b43-804e-1c52f4e94c7a/
- https://www.washingtonpost.com/archive/business/1995/10/02/paging-takes-a-new-direction/777e5512-f023-45fa-8b8e-f3052041dc25/

海外比较的用途是解释对象结构，不把 OWA scope 变成全球 paging archive。

---

## 13. 一个特别重要的时间性警告：不要用 2007 的结局清洗 1999 的页面语义

1999 年存在：

- 全国寻呼网络扩张；
- 网上寻呼；
- email-to-pager；
- Internet 用户实际使用“网上寻呼机”；
- 同期媒体预测 pager 用户还会继续增加。

1999-12-08《光明日报》甚至采访到通信专家，预测 2005 年中国寻呼用户可能达到 1.3 亿。

来源：

- https://tech.sina.com.cn/news/computer/1999-12-08/12840.shtml

但 MIIT 2005 年 12 月统计表只剩 **97.1 万无线寻呼用户**：

- https://www.miit.gov.cn/gxsj/tjfx/txy/art/2020/art_b18e780c481745239acd2fc69364e2a3.html

2007 年联通又申请关闭除上海外大部分公共寻呼服务：

- https://business.sohu.com/20070305/n248504668.shtml

因此未来如果找到 1999 `网上寻呼` 页面，不能把它解释成：

> “一个已经快淘汰的旧技术勉强加上 Web。”

因为对 1999 同时代参与者而言，它完全可能被理解为：

> “成熟无线消息网络正在获得 Internet 输入端。”

这是历史页面语义的一部分。

---

## 14. 对 M1/M3 的直接影响

### M1：如果未来找到 capture

至少记录：

```yaml
platform: 国信网源 / relevant paging service
page_type: online paging control surface
original_url: unknown until recovered
capture_datetime: required
input_fields:
  - pager_id
  - message
  - region_or_network?
  - auth?
submission_method: GET/POST/unknown
backend_endpoint: record if visible
response_semantics: accepted / queued / delivered / unknown
charset: required if observable
subresources: list separately
```

必须另外加：

```yaml
external_system:
  type: radio_paging_network
  backend_state_preserved: false/unknown
  delivery_state_preserved: false/unknown
  receiver_state_preserved: false/unknown
```

### M3：浏览环境复原

即使 IE5/IE6 能完整显示 form，仍不能把“点击发送”真的连向历史号码或真实第三方系统。

安全、隐私与研究伦理要求：

- 不试探真实旧寻呼号；
- 不发送真实消息；
- 使用 synthetic pager ID；
- backend mock 必须标记 `reconstruction`；
- “发送成功”只能模拟 UI 分支，不得假装重建真实 1999 delivery。

---

## 15. 隐私边界

历史 pager ID / 号码可能和真实个人身份、电话、单位相关。

因此如果未来取得：

- 用户目录；
- 示例 pager number；
- 旧个人主页上的呼号；

默认做 research-minimization：

1. 平台结构优先；
2. 普通个人号码 redacted；
3. 不批量重新公开 private/contact data；
4. 不用活跃网络测试旧号码；
5. demo / synthetic fixture 与 historical evidence 分开。

---

## 16. 与 HPL 的交叉解释

对应 HPL 研究包：

`how-people-lived/sources/from-pager-to-mobile-phone-reachable-without-callability-and-split-communication-loop-china-1984-2007.zh-CN.md`

HPL 侧新增的生活机制包括：

- `reachable-without-callability`；
- `split communication loop`；
- `borrowed return channel`；
- `callback avoidance`；
- `cross-network notification`；
- `branching technical future`。

OWA 负责解释其中 Web 可见的部分为什么不能代表整个通信系统。

最核心的对应关系：

```text
HPL: Internet 信息怎样追上一个没有持续上网的人？

OWA: 历史页面保存以后，我们还缺失了哪几层 gateway / radio / receiver state？
```

---

## 17. 证据矩阵

| Claim | Evidence | Grade | Confidence | Limitation |
|---|---|---:|---:|---|
| 1999 国信存在“网上寻呼” | MII 1999 bulletin | A | high | exact URL unknown |
| 22 省网有 email 到达呼 | MII 1999 bulletin | A | high | workflow details absent |
| Tencent email 可送 paging station | Tencent archived corporate news dated 1999-07-11 | A/B | high for content provenance | current HTML not 1999 capture |
| 网民实际使用“网上寻呼机” | CNNIC 1999-12-31 survey | A/B | high for sampled users | self-selected online survey |
| Internet→pager gateway 是全球 1990s 架构 | RFC 1568/1645 | A | high | not Chinese implementation proof |
| form capture ≠ pager delivery | system-state inference | D | high | needs future concrete capture to instantiate |
| 1999 页面不能按“即将淘汰”解释 | contemporaneous forecast + later collapse | B/A | high | interpretation, not UI fact |

---

## 18. 已证实 / 高概率 / 不知道

### 已证实

- 1999 年中国有网上寻呼和 email 到达呼；
- 国信有名为“国信网源”的网站；
- 腾讯 1999 邮件增值系统把 email 内容路由到 paging station；
- CNNIC 的 1999 年末调查把“网上寻呼机”列为实际使用的网络服务；
- Internet-to-pager gateway 在 1994 RFC 中已有标准化尝试；
- 2005 年公共无线寻呼用户已经大幅萎缩。

### 高概率

- 1999 的网上寻呼使用了 server-side form / gateway，而不是单纯静态页面；
- 不同省网可能存在服务能力、号码格式和 message length 差异；
- historical capture 即使存在，也很可能只保存 control surface 而不是 backend transaction state。

### 不知道

- “国信网源” exact URL；
- 是否仍有 Wayback / Common Crawl / WARC capture；
- exact field schema；
- HTTP method；
- backend endpoint；
- charset / browser requirement；
- historical send success semantics；
- receiver display behavior；
- 同一服务第二历史时点。

---

## 19. 下一步 artifact-first 路线

优先级不是再写“寻呼机怀旧史”，而是：

1. 从 1998—2001 中文网址目录、报刊广告、ISP 导航页里恢复 `国信网源` exact hostname；
2. 查 `网上寻呼` / `电子邮件到达呼` 的用户教程，争取拿到 URL pattern / field names；
3. 一旦 exact URL 出现，进入 Wayback / Common Crawl locator probe；
4. 若能打开，按 `docs/METHOD.md` 记录：capture datetime、HTTP/replay、DOM、charset、subresources；
5. 查找第二历史时点，判断 gateway UI / operator / branding 是否变化；
6. 不对真实号码执行历史 form；任何 transaction path reconstruction 均使用 synthetic fixture。

---

## 20. 本轮结论

旧 Web 不只是一个“信息页面世界”。

1999 年一名用户可以在拨号 Internet 上收到 email，或者让另一个 Web 用户提交消息，然后真正响起来的却不是浏览器——而是一个挂在某人腰间、运行在完全不同无线网络上的寻呼机。

所以：

> **页面的边界，不是系统的边界。**

对于这种对象，Web archive 最可能保存的是控制面；真正消失的，恰恰是 gateway 后面的 operational state、无线投递和最终收件端。
