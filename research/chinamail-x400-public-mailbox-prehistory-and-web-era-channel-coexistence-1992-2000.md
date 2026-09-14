# ChinaMail / X.400 公用电子信箱、Web 时代渠道共存与邮箱状态缺口（1992—2000）

> **状态：research / boundary note，不是 M1 complete case。**
>
> **Scope 约束：** 本仓主研究期仍是约 1995—2015 中文 Web。本 note 追溯 1992—1994 只为解释 1995 年以后中文 Web 与更早公用电子信箱/X.400 网络如何重叠；完整的普通生活史写入 `tmzncty/how-people-lived`，不把本仓扩成中国全部数据通信史。

关联：

- `docs/PREHISTORY_BOUNDARY.md`
- `docs/METHOD.md`
- HPL：`sources/public-electronic-mailbox-before-public-internet-china-1992-1997.zh-CN.md`
- HPL：`topics/before-mass-internet-access-ladder-china-france-1980s-1997.zh-CN.md`

---

## 1. 为什么需要这个 note，而不是再写一篇“Internet 前史”

`PREHISTORY_BOUNDARY.md` 已经明确：

```text
网络能力出现
≠ 全功能 Internet 接入
≠ 公共互联网服务出现
≠ 普通家庭可及
≠ 大众互联网生活形成
```

它也已经记录 CANET、CNPAC、科研邮件和 1994 全功能 Internet 边界。

本 note 不重复这些结论，而补一个 OWA 仍缺的**artifact / state 类型**：

> **1995 年中文 Web 出现时，异步数字邮箱并不是只有 Internet SMTP/POP/Webmail 这一种实现。更早的 MHS/X.400/ChinaMail 邮箱仍在运行，同一内容甚至可以同时分发到 Web/Internet 与 ChinaMail。**

这会直接影响旧网页的解释，因为：

1. 一个 Web 页面可能只是多渠道发布中的一个 projection；
2. 页面上的“电子信箱”一词不自动等于今天的 Internet email；
3. 后来的 `@domain` 地址不能无证据倒投到更早的 proprietary / X.400 mailbox identity；
4. Wayback 天然更容易保存 Web representation，而几乎不会保存拨号邮箱、X.400 message store、账号目录、网关状态和用户收件箱。

---

## 2. Claim list

本轮只主张以下窄结论。

### Claim A — 1992 年已有面向用户的公用电子信箱系统

1992-06-28《人民日报》新闻简报记录，北京公用电子信箱系统于 6 月 26 日开通，由电信部门建立并与用户计算机连接；用户可发送信息到他人信箱，也可凭密码取信，开通时已有一百多个用户。

当前证据是历史报纸的数字转录，不是本轮实际核验的原版扫描。

来源：

- <https://cn.govopendata.com/renminribao/1992/06/28/1/>

**Evidence：B+ / contemporaneous-text locator；confidence：high for service existence, medium for exact wording provenance because scan not checked。**

它证明“公用电子信箱服务存在”，不证明“普通家庭普及”。

---

### Claim B — 上海 1992—1995 的电子信箱服务有独立于 Internet 的 X.400/MHS 网络史

上海市政府保存的《上海通志干部读本》记录：

- 1992-06：上海长途电信局电子信箱系统试运行；
- 1993-04：与福州等地联通；
- 1994：与北京以及美国 Telemail、日本 ATI、新加坡 stems、意大利 omega400 的 X.400 网络互联；
- 1995-07：加入全国联网，并称由此形成中国电子信箱系统 ChinaMail；
- 1995 上海 ChinaMail 用户约 0.13 万户。

同一节另列 Internet：

- 1995 年初上海 ChinaNet 节点建成；
- 1995-05-17 开放国际 Internet 业务；
- 1995 用户约 0.11 万户。

来源：

- 上海市政府，《上海通志干部读本》，PDF P321–P322：<https://www.shanghai.gov.cn/shanghai/newshanghai/%E4%B8%8A%E6%B5%B7%E9%80%9A%E5%BF%97.pdf>

**Evidence：B / institutional retrospective compilation；confidence：high for chronology as recorded, medium for user-count denominator until original departmental statistics are recovered。**

这里不能比较出“ChinaMail 比 Internet 更流行”；只能确认两套服务**同城、同年、并存且分别统计**。

---

### Claim C — 1995 年电子出版物可以同时投影到 Internet、图文电视和 ChinaMail

2000 年新浪科技刊载的网络新闻传媒材料回顾：1995-10-20《中国贸易报·电子版》开播后，同时通过：

1. 国际互联网；
2. 中央电视台图文电视；
3. 全国电子信箱信息服务系统 ChinaMail

三条渠道传播。

来源：

- <https://tech.sina.com.cn/news/it/2000-04-19/23203.shtml>

**Evidence：B / near-contemporaneous retrospective；confidence：medium-high for channel coexistence, not sufficient for exact message format or historical URL。**

这是一条 OWA 很重要的边界证据：

> **同一“电子版”内容不是天然只有一个 Web original。Web 只是它的若干 contemporaneous representations 之一。**

---

## 3. 新的研究单位：不要把“电子信箱”当成一个 page field

研究早期中文页面时，看到：

```text
电子信箱：xxxx
```

必须先问它究竟指什么。

至少可能是：

```text
Internet RFC822/SMTP address
X.400 / MHS address
ChinaMail service account
BBS internal mailbox
commercial online-service mailbox
gateway alias
later retrospective rewrite
```

因此，本仓以后遇到 1995—2000 `电子信箱 / E-Mail / Mailbox` 字段，建议额外记录：

| 字段 | 问题 |
|---|---|
| `mailbox_system` | Internet mail / X.400 / MHS / ChinaMail / BBS internal / unknown |
| `address_as_displayed` | 历史页面实际显示什么，不补全 |
| `address_namespace` | 是否是 `local@domain`、X.400 structured address、numeric/service ID 等 |
| `gateway_claim` | 是否有证据与 Internet/其他邮件网互通 |
| `gateway_evidence_date` | 网关能力在哪一天/年份得到证据支持 |
| `client_context` | terminal / proprietary client / dial-up / Webmail / unknown |
| `mailbox_host` | 邮箱所在服务或 message store，若可确认 |
| `representation_channel` | Web / email / ChinaMail / teletext / print / multiple |
| `identity_continuity` | 后来的 Internet alias 是否确证继承同一旧账号 |

最重要的规则：

> **不要把今天熟悉的 `@domain` 结构自动补给一个只写“电子信箱”的历史页面。**

---

## 4. `service-identity / Internet-identity gap`

这是本轮最重要的 state gap。

一个用户可以已经拥有：

- mailbox；
- password；
- persistent message store；
- service-internal identity；

但仍然没有：

- globally routable Internet email address；
- SMTP/POP account；
- Webmail URL；
- full TCP/IP Internet access。

因此：

```text
mailbox exists
!= Internet address exists
!= Internet gateway exists
!= Webmail exists
```

这一点不能从后来页面反推。

如果某旧服务后来给原账号增加 Internet alias，必须记录 alias 的**首次可证日期**；不能把 1998 的 alias 写回 1993。

---

## 5. `gateway-time boundary`：用户界面没变，可达世界却可能突然变了

邮件系统和 Web 页面有一个不同点：

> **真正决定“你能寄给谁”的关键变化，可能发生在网关，而不是 UI。**

例如一个 proprietary mailbox：

```text
T0：只能寄同服务内部账号
T1：可通过 X.400 gateway 寄到另一城市/国家
T2：加入 Internet mail gateway
T3：获得 RFC822-style alias
T4：出现 Webmail front-end
```

用户可能多年看到近似的“写信 / 收信”界面，但地址宇宙已经改变数次。

这意味着旧网考古需要把：

- `UI chronology`
- `gateway chronology`
- `address chronology`

分开。

### 海外 control：CompuServe

1989-07-17《Washington Post》报道，CompuServe/The Source 自 1979 起已经让个人电脑用户经电话线接入并收发电子邮件；1989 年 CompuServe 宣称用户超过 50 万。

来源：

- <https://www.washingtonpost.com/archive/business/1989/07/17/information-services-companies-develop-new-improved-products/689795d6-b914-4e63-a597-f0a35ec54682/>

后出的 CompuServe/AOL 历史资料把 1989 标为 proprietary email 与 Internet email gateway 打通的重要时期。

来源：

- <https://www.compuserve.com/home/about.jsp>
- <https://www.aol.com/news/compuserve-earns-state-historical-recognition-110140253.html>

CompuServe 的意义不是给中国找“模板”，而是证明：

> **邮箱服务内部通信 → 外部网关 → Internet addressability**

是一种跨国都可能出现的技术序列，并不等于“电子邮件从一开始就是开放 Internet 服务”。

---

## 6. `channel-equivalence fallacy`：同一内容 ≠ 同一历史 artifact

《中国贸易报·电子版》的三渠道分发提示一个常见错误。

即使文字内容源相同：

```text
Web HTML
ChinaMail message
teletext page
```

也不是同一 artifact。

它们可能具有不同：

- 标题截断；
- 字符编码；
- 字数限制；
- 分页；
- 发布时间；
- 图片支持；
- 超链接；
- MIME/message envelope；
- 发送者/收件者字段；
- 阅读顺序；
- 保存机制。

因此若未来恢复 1995《中国贸易报》Web 页面，不得写：

> “这就是 ChinaMail 用户当时看到的电子报。”

除非另有 ChinaMail message artifact 证明 rendering/content parity。

建议字段：

```yaml
content_work: 中国贸易报电子版某期
representation:
  channel: web | chinamail | teletext
  observed_artifact: true/false
  timestamp: ...
  encoding: ...
  transformation_known: true/false
```

---

## 7. Web archive 对非-Web 邮箱存在结构性失明

Wayback 等 Web archive 主要保存 HTTP resources。

即使一个 1996 页面完整保留了“ChinaMail”“电子信箱”链接或地址，也可能完全没有保存：

- X.400 directory；
- message store；
- account provisioning；
- dial-up access number；
- terminal client；
- mailbox password flow；
- gateway routing table；
- unread/read/deleted state；
- 真实 message payload；
- 用户个人 address book；
- 发送失败 / 延迟 / bounce 记录。

因此新增：

### `mailbox-state invisibility`

历史 Web capture 看见的是**服务的公开表面**，不是历史 mailbox state。

### `gateway-state invisibility`

网页说“可发送国际邮件”最多证明一种 contemporaneous claim；除非有日志/手册/测试记录，不能恢复某一时刻网关实际可达哪些网络。

### `address-directory loss`

邮件系统的可寻址空间可能依赖动态 directory；directory 丢失后，单条旧地址很难证明当时可发现性。

### `non-Web survival bias`

1990 年代中期同时存在的 Web 与非-Web 数字服务，今天保存概率极不对称。

这会制造错误印象：

```text
今天能看到的 1995 Web 很多
→ 1995 的数字生活主要就是 Web
```

这个推理不成立。

---

## 8. `later-email-address backprojection` 风险

个人主页、单位介绍、论文元数据里经常可以看到后来留下的 Internet email 地址。

如果某机构 1993 年已有 MHS/ChinaMail 服务、1996 年又有 Internet 域名，很容易出现一种诱人的叙事：

> “该人/单位从 1993 年起就使用 `name@domain.cn`。”

除非有 1993 artifact 明确显示这个地址，否则不能这么写。

必须允许以下情况：

```text
1993: X.400 / service ID A
1995: gateway alias B
1996: Internet mailbox C
1998: Web page displays C
```

甚至 A、B、C 是否同一个人的连续账号都可能未知。

所以：

> **identity continuity is a claim, not a default.**

---

## 9. 1995 不是“旧邮件系统停止、新 Web 开始”的边界

上海地方志本身就把 1995 年 ChinaMail 和 Internet 分别列项；《中国贸易报》材料又显示同一电子出版物通过 Internet 和 ChinaMail 同时传播。

因此 OWA 中更准确的过渡模型是：

```text
pre-Web digital services
        │
        ├── continue independently
        ├── gain gateways
        ├── coexist with Web
        ├── project some content to Web
        └── later disappear / merge / become invisible
```

而不是：

```text
1995: Web arrives → everything before it becomes obsolete
```

这条边界说明对于 1995—1998 中文站点尤其重要，因为站点作者/机构可能同时仍在：

- ChinaMail；
- X.400；
- 传真；
- BBS；
- 电话信息服务；
- Internet email；
- Web

之间工作。

---

## 10. Evidence ledger

| ID | Evidence | Grade | Supports | Does not support |
|---|---|---|---|---|
| E1 | 1992《人民日报》北京公用电子信箱新闻的数字转录 | B+ locator | public mailbox service existed; password retrieval; 100+ users | original scan appearance, household adoption, address format |
| E2 | 《上海通志》1992—1995 增值电信条目 | B institutional | Shanghai MHS/X.400 chronology; ChinaMail network; 1995 user counts; Internet separately listed | exact original operational logs, daily availability, user composition |
| E3 | 2000 新浪刊载的网络新闻传媒材料 | B | 1995 trade newspaper remembered as Internet + teletext + ChinaMail parallel distribution | exact 1995 message bytes, HTML, timestamps, UI |
| E4 | 1989 Washington Post CompuServe report | A/B contemporaneous media | consumer proprietary online email existed at scale; PC/modem/time-priced access | exact gateway internals |
| E5 | later CompuServe/AOL history | C / corporate retrospective | gateway chronology lead | must not replace 1989 primary/contemporaneous evidence |

---

## 11. 已证实 / 高概率 / 不知道

### 已证实（按当前证据强度）

- 1992 北京已有公用电子信箱服务，并有 100+ 用户的同期报道；
- 上海 1992 起运行电子信箱系统；
- 上海 1994 记录到多个 X.400 国际互联；
- 上海 1995 ChinaMail 与 Internet 被作为不同业务分别记录；
- 1995 后中国早期 Web 与 ChinaMail 并非必然互斥；
- 海外商业联机服务也存在“proprietary mailbox 先于 Internet gateway”的路径。

### 高概率但仍需原始技术材料加强

- ChinaMail 用户使用专用/标准兼容客户端或拨号路径访问 mailbox；
- 部分后来 Internet mail identity 可能由旧服务经 gateway/alias 迁移；
- 1995—1997 一些内容提供者维护了多套并行发布工作流。

### 不知道

- 1992 北京系统精确软件/硬件产品；
- 早期用户个人/单位构成；
- 资费；
- 精确拨号号码与登录流程；
- ChinaMail historical account/address syntax；
- 1995《中国贸易报》ChinaMail message 的原始 envelope/body；
- ChinaMail → Internet SMTP gateway 的精确上线日；
- 是否有任何公开可核验的 ChinaMail historical client screenshot / installer / manual；
- 某一 ChinaMail mailbox 的真实历史 message state。

---

## 12. Archive / reconstruction stop condition

这个对象不能按普通网站去追一个“主页截图”就算完成。

如果未来只能找到：

- ChinaMail 名称；
- 服务号码列表；
- 后来回忆；
- 1995 Web 页面提到“电子信箱”；

但没有：

- 原始操作手册；
- 客户端软件/截图；
- historical address example；
- message artifact；
- gateway technical document；

那么必须停在 research note。

尤其禁止：

1. 用现代 email UI 重建 ChinaMail 并标成历史原貌；
2. 根据“电子信箱”四字生成一个 `user@chinamail...` 地址；
3. 把 Web archive 的网页时间当作邮件发送时间；
4. 把当前还能看到的后出文章当作 1995 Web original；
5. 为了“完整复原”寻找或公开普通人的历史私人邮件。

隐私优先：平台/协议研究不需要恢复个人私人 mailbox 内容。

---

## 13. 对 M1 的状态

本轮**没有完成 M1 case**。

当前状态：

```text
historical service identity: ACHIEVED
1992 public-mailbox existence: ACHIEVED (transcribed contemporaneous newspaper)
1992—1995 Shanghai X.400/ChinaMail chronology: ACHIEVED (institutional retrospective)
1995 Web-era channel coexistence: ACHIEVED as B-grade claim
exact ChinaMail historical UI: NOT ACHIEVED
exact public hostname/URL: NOT APPLICABLE / UNKNOWN for non-Web service
historical client artifact: NOT ACHIEVED
historical message artifact: NOT ACHIEVED
Internet gateway exact date/config: NOT ACHIEVED
verified historical Web memento tied to ChinaMail: NOT ACHIEVED
M1 complete case: NOT ACHIEVED
```

这正是边界 note 的价值：它让后续 M1 研究者知道，**不能把 Web capture 当成 1990 年代全部数字通信环境。**

---

## 14. 下一步最值钱的 artifact

优先级从高到低：

1. 1992—1996 ChinaMail / MHS 用户手册或开户指南；
2. 同期电信资费表；
3. 客户端软件、安装盘、屏幕截图或操作教材；
4. 1641 等接入号码的同期官方号码表（不要依赖现代号码聚合站）；
5. X.400 address examples 和 gateway technical manual；
6. 《中国贸易报·电子版》同一期 Web 与 ChinaMail 双 artifact；
7. 1995—1997 站点中明确同时列出 X.400 与 Internet email 的页面；
8. 第二个城市的用户统计，检验上海是不是特例。

如果拿到第 6 类，尤其值得做：

```text
same content work
→ Web representation
→ ChinaMail representation
```

的逐字段比较，这会比继续添加新的 `STATE_GAPS` 名称更有考古价值。

---

## 15. 本轮最小结论

> **早期中文 Web 不是从“数字通信空白”里突然长出来的。它进入的是一个已经存在公共电子信箱、X.400、分组数据网、传真、BBS 和其他数字服务的环境。**

对 OWA 来说，更重要的不是把这些前史都纳入主 scope，而是记住：

> **一个 1995 Web 页面可能只是某项服务的一个新界面、一个新渠道或一个投影；Web archive 保存了这个投影，并不等于保存了当时整个数字系统。**