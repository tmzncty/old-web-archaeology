# “网上寻呼”到底是什么：OICQ、email-to-pager、GSM SMS 网关与历史术语碰撞，1999–2001

> Scope：中文旧网约 1995–2015 范围内，研究 1999–2001 年“网上寻呼 / 网上寻呼机 / 网络寻呼机”这一历史词汇背后至少两套不同技术对象，以及 Web / email / OICQ 与无线寻呼、GSM SMS 之间的跨网事务链。  
> 交叉生活史包：`tmzncty/how-people-lived/sources/pager-public-phone-mobile-addressability-and-network-bridge-china-1984-2007.zh-CN.md`。  
> 本文不是 QQ 怀旧史，不宣称已复原 1999 OICQ 或国信“网上寻呼”网页。当前目标是：**先把 historical identity、术语、跨网依赖、现存 artifact 与 archive gap 拆清楚，避免把完全不同的“寻呼”混成同一个旧网对象。**

---

## 0. 去重：这不是再写一个一般性的 `page != transaction`

本仓已经反复建立：

```text
page != account
page != transaction
locator != verified capture
current live legacy page != historical memento
HTML preserved != server state preserved
```

本轮不再重命名同一问题，而是解决一个更具体的旧网考古风险：

> **历史资料里的同一个词，可能在极短时间内同时指向两套不同系统。**

1999–2001 年的“网上寻呼”就是这样。

如果不先分对象，会产生严重误读：

- 把 CNNIC 的“网上寻呼机 21%”误写成 21% 网民向 BP 机发送 Web 消息；
- 把 OICQ 的“网络寻呼机”定位误写成它天然依赖 126/127/198/199 无线寻呼网；
- 把 1999 腾讯 email-to-pager gateway 误写成 QQ 客户端功能；
- 把 current Tencent historical article 当成 1999 原始网页形态。

---

## 1. 先定义三个不同研究单位

### Subject A — physical pager network 的 Internet gateway

最小结构：

```text
Web / Internet / email
→ gateway / application server
→ paging station
→ 198 / 199 等无线寻呼网络
→ physical pager
```

这类系统的目标终端是真实 BP 机。

### Subject B — OICQ / ICQ 式“网络寻呼机”

最小结构：

```text
Windows client
→ Internet
→ IM server
→ another online identity / client
```

这里“寻呼机”是对即时通信产品的历史命名 / 隐喻，不等于 physical pager network。

### Subject C — mobile OICQ / SMS gateway

最小结构：

```text
GSM SMS / WAP
↔ mobile operator gateway
↔ Tencent OICQ
↔ PC Internet user
```

它又把网络身份和移动电话网络接起来。

三者在 1999–2001 时间上高度重叠，但不能因为都出现“寻呼”两个字就合并。

---

## 2. Artifact family A：信息产业部 1999 汇编证明 physical pager 的“网上寻呼”确实存在

信息产业部综合规划司《通信统计资料汇编（1999）》记载：

- 国信公司无线寻呼用户网络覆盖全国 335 个地市、2022 个县市；
- 198/199 全国联网寻呼拥有广泛覆盖；
- 截至 1999 年底，“网上寻呼”开通到 198、199 全国寻呼网、27 个省及部分市县寻呼网；
- 电子邮件相关业务开通 22 个省市。

这一来源的价值在于：

**即使一个 Web 页面都没有恢复，我们仍有 A 级同期制度 / 业务统计证据，证明“Internet-side paging service → physical paging network”这一服务族当时存在。**

### 证据等级

- **A（同期主管部门统计汇编扫描件）**。

### Source

- 信息产业部综合规划司，《通信统计资料汇编（1999）》。  
  Scan： https://upload.wikimedia.org/wikipedia/commons/a/a2/SSID-12873460_%E9%80%9A%E4%BF%A1%E7%B5%B1%E8%A8%88%E8%B3%87%E6%96%99%E5%8C%AF%E7%B7%A8_1999.pdf

### 它不能证明什么

目前没有由这份汇编直接证明：

- 用户端 URL；
- 登录页面布局；
- 是否必须拥有某类 pager 账号；
- 资费；
- 浏览器要求；
- 具体请求 / 回调格式；
- 用户规模。

因此它证明 **service exists**，并不自动证明具体 **Web UI recovered**。

---

## 3. Artifact family B：腾讯 1999 email-to-pager 系统把跨网 transaction 写得更细

腾讯当前官网保存一篇内部日期为 **1999-07-11** 的公司新闻：腾讯与 SINET 合作，将 email 增值服务系统放到深圳电信网络试运行。

页面描述的事务链非常明确：

```text
S0  ISP dial-up user has an email account
↓
S1  incoming email arrives
↓
S2  system extracts sender / subject / content
↓
S3  compare with user-defined rules
↓
S4a send to paging station
S4b send to GSM SMS system
S4c optionally obtain via fax
↓
S5  pager / mobile receives message content
```

用户还能在认证以后设置：

- call barring time period；
- email barring time period；
- character-string filtering；
- 其他筛选规则。

这条来源对于旧网考古很重要，因为它说明一个 1999 的“Internet service”不能只按 Web 页面研究。

真正的执行环境跨越：

```text
web/account configuration
+ mail server
+ filtering application
+ telecom gateway
+ paging station / GSM SMSC
+ wireless radio network
+ physical terminal
```

### Source

- Tencent, “Tencent launched email value-added service system in cooperation with SINET”, historical date 1999-07-11.  
  https://www.tencent.com/en-us/articles/80260.html

### 证据等级

- **A-/B+：current official legacy representation of first-party historical content**。

理由：

- 当前域名和主体可以确认是腾讯；
- 页面明确保留 1999-07-11 的内部历史日期和第一方业务陈述；
- 但本轮没有 verified 1999 capture，不能确认当年的 URL、DOM、模板、语言版本、HTTP headers 或页面是否原样迁移。

所以应该写：

> 腾讯当前官方历史页面保存了一份标注 1999-07-11 的第一方业务陈述。

而不是：

> 我们已经打开了腾讯 1999 年 7 月 11 日的原始网页。

---

## 4. 这是一个典型的“服务比网页更大”的旧网对象

即使以后拿到该产品的完整 HTML，也很可能仍然无法 replay 真正的事务。

原因是有效事务依赖：

```text
email account exists
→ authentication works
→ filtering rules persist
→ mail event arrives
→ gateway routing table exists
→ paging station accepts message
→ pager number is active
→ radio network still transmits
```

其中大多数状态今天已经不存在。

因此本轮不再发明一个泛化的新 `state-loss` 术语，而是把它作为具体的：

**cross-network dependency record**。

未来 reconstruction 应明确标注：

```yaml
web_layer_replayable: unknown
mail_event_replayable: no_original_state
paging_gateway_replayable: not_verified
historic_pager_network_available: no
end_to_end_transaction_replay: not_achieved
```

---

## 5. Artifact family C：OICQ 同期却也被叫“网上寻呼”——词相同，对象已经变了

2000 年 7 月 26 日，《长江日报》在武汉网吧采访中学生时直接写：

> 点击屏幕上的小企鹅，这是 OICQ，时下流行的“网上寻呼”。

报道现场观察到 OICQ 的好友、陌生人、黑名单等结构，并记录一个 17 岁学生同时与多名网友聊天。

这条同期材料确认：

**到 2000 年，“网上寻呼”至少已经被普通媒体用于指 OICQ 式 Internet IM，而不是只指 Web-to-BP gateway。**

### Source

- 《长江日报》经新浪保存，2000-07-26。  
  https://edu.sina.com.cn/edu/2000-07-26/8748.shtml

### 证据等级

- **B+（同期记者现场观察 + 用户采访）**。

### 特别有价值的同场现象

同一篇报道里，学生又会把真实 **BP 机号**给网上认识的人，再在离线以后收到物理传呼。

所以一个 2000 年用户可以同时使用：

```text
OICQ “网上寻呼”
+
physical pager number
+
fixed / home telephone
```

这正是不能按今天产品分类重写历史的理由。

---

## 6. CNNIC 的“网上寻呼机”统计必须做 semantic disambiguation

CNNIC 1999 年 7 月调查的“用户最常使用的网络服务”中：

- “网上寻呼机”约 14.8%；

2000 年 7 月报告的对比表则给出：

- 1999.7：15%
- 2000.7：21%

如果只看到字段名，很容易误解为：

> 21% 网民使用 Web / Internet 向 physical pager 发消息。

但同期《长江日报》已经明确把 OICQ 称作“网上寻呼”；后来的中国电信互联网十年回顾也把这一统计项目括注为 OICQ、ICQ 等。

因此本轮给出一条**方法性纠错**：

```text
historical category label
!=
modern category meaning
```

在取得 CNNIC 原始问卷说明、产品示例或编码手册以前，最安全的表述是：

> 1999–2000 CNNIC online survey respondents 中，选择“网上寻呼机”这一网络服务类别的比例上升；该历史类别很可能至少涵盖 OICQ / ICQ 式 IM，不能直接等同于 physical pager gateway adoption。

### Sources

- **B+/A- 同期报告转载**：1999.7 CNNIC report.  
  https://tech.sina.com.cn/news/it/1999-12-15/13431.shtml
- **B+/A- 同期报告转载**：2000.7 CNNIC report.  
  https://tech.sina.com.cn/internet/china/2000-07-27/31904.shtml
- **A/current official historical report page**：CNNIC 第六次调查。  
  https://www3.cnnic.cn/n4/2022/0401/c88-786.html
- **C/行业回顾，仅辅助解释字段语义**：中国电信互联网十年盘点。  
  https://ad.sina.com.cn/minisite/tianyihd/

### Archive consequence

未来对旧网页做全文检索时，关键词：

```text
网上寻呼
网络寻呼
网上寻呼机
```

不能自动映射到一个 entity type。

应先判定：

```yaml
possible_meaning:
  - physical_pager_gateway
  - internet_instant_messaging
  - generic_network_notification
  - marketing_metaphor
```

---

## 7. 术语碰撞本身就是旧网证据，而不是“写错词”

今天看 OICQ，我们会自然归类为：

```text
instant messaging client
```

但 1999–2000 的用户和媒体并不一定拥有后来稳定下来的产品分类语言。

“网络寻呼机”这个称呼说明当时理解新 Internet 通信工具时，仍借用了已经大众化的 BP 机模型：

- 我有一个号码；
- 别人可以“呼”我；
- 有消息会提醒；
- 可以看谁在线 / 谁找过我；
- 身份跟着账号走，而不是跟着某一台公用电脑走。

因此旧网术语研究不能把今天的 ontology 直接套回去。

本轮把这一具体方法问题记为：

**`terminology collision / 历史术语碰撞`**。

它不是一个新的宏大理论，只是提醒数据集设计：**词是 evidence，不是预先定义好的 entity type。**

---

## 8. 2001 Mobile OICQ：Internet identity 又跨过一次网络边界

2001 年 3 月 6 日新浪科技报道，北京移动已经正式开通“移动 OICQ”，成为第九家开通该服务的移动公司。

报道特别强调：

```text
mobile user
does not need Internet access
and does not need a computer
```

只需通过短信指令开通，就能与 Internet 上的 OICQ 用户通信。

其架构说明为：

```text
GSM SMS / WAP
↔ mobile operator system
↔ Tencent OICQ system
```

功能包括：

- 手机向 OICQ 用户发送消息；
- OICQ 离线时把消息送到已绑定手机；
- 手机查看好友状态；
- 用昵称、email、OICQ 号码查找用户。

### Sources

- **B+（2001 同期产品 / 运营报道）**：新浪科技，2001-03-06。  
  https://tech.sina.com.cn/i/c/56518.shtml
- **B+（2001 同期行业报道）**：南方都市报经新浪保存，2001-06-24。  
  https://tech.sina.com.cn/i/c/72816.shtml

### 证据边界

报道中的“每天 100 万条”“3000 万条”等业务量来自腾讯 / 运营商自报，应作为 platform-reported operational metric，不当作独立人口统计。

---

## 9. 1999 Tencent 还有另一份 mobile email 历史页面，进一步确认这种网关思维

腾讯当前官网另保存一篇内部日期为 **1999-04-07** 的历史公司新闻，描述与深圳联通合作的“Mobile Email”：

- 手机可收 / 发 email；
- 可与 Internet 用户通过 SMS 通信；
- 新邮件可以通知到手机；
- 可从网页设置限制条件；
- 计划支持 QQ-GSM 双向通信。

它说明 1999 腾讯的产品环境本来就在尝试把：

```text
Internet account
email
SMS
pager-like notification
mobile phone
```

接进同一通信栈。

### Source

- **A-/B+ current official legacy historical content**：Tencent, “Tencent launched mobile email service in cooperation with Shenzhen Unicom”, dated 1999-04-07.  
  https://www.tencent.com/en-us/articles/80261.html

同样：这不是 verified 1999 capture。

---

## 10. 2000 的普通网吧用户说明：平台身份可以跨机器，但机器仍是临时的

《长江日报》的 2000 网吧材料与本仓既有 shared-terminal 研究可以直接相连。

学生在网吧使用 OICQ：

```text
temporary rented PC
→ login OICQ account
→ stable friend list / online identity
→ leave café
→ identity remains on server
```

这与 physical pager 非常相似的一点是：

> **通信地址开始属于人，而不是属于那台机器。**

但两种技术的可执行条件完全不同：

| 层 | BP 机 | OICQ 2000 |
|---|---|---|
| 随身终端 | 有 | 通常无，需要 PC / 网吧 |
| 消息接收 | 无线寻呼覆盖 | Internet + OICQ server + client |
| 双向即时文本 | 典型单向机无 | 有 |
| 回复依赖另一设备 | 常依赖固定 / 公用电话 | 依赖当前 PC / Internet session |
| 身份持续 | pager number | OICQ account / number |
| 网络退出后 | pager 仍可继续接收 | PC 端离线；后续可通过 mobile OICQ 补桥 |

这也解释了 2001 mobile OICQ 为什么是重要中间层：它让 Internet identity 开始离开 PC session。

---

## 11. OICQ 早期 artifact：本轮不把 2026 “复活版”冒充 original

2026 年有研究者 / 爱好者公开展示了“复活”1999 第一版 OICQ 的实验。报道声称：

- 找到了多个早期版本；
- 第一版仍可在现代 Windows 运行；
- 但原服务器已经停用；
- 实验者必须自己搭替代服务器才能登录 / 使用。

这对本仓有价值，但证据等级只能是：

**D（modern reconstruction / reverse-engineering evidence）**。

它最多帮助我们形成下一步问题：

- binary 是否真为 1999 original；
- compile timestamp 是否可信；
- server endpoint / protocol 能否从 binary 中恢复；
- modern Windows 的成功运行是否掩盖 Win95/98 下差异；
- substitute server 实现了哪些、遗漏哪些 protocol semantics。

它绝不能被写成：

> “1999 OICQ 已经完整复原。”

### Source（仅作 D 级 lead）

- IT之家，2026-03-30，《技术大神复活 1999 年的 QQ 第一版……》。  
  https://www.ithome.com/0/933/962.htm

### 本轮动作边界

- 没有下载 / 再分发不明版权 binary；
- 没有把第三方 substitute server 当历史原件；
- 没有依据现代 Win11 运行结果推断 1999 historical browser / OS experience。

---

## 12. Historical locator 与 capture probe

### 已确认 historical identity / locator leads

后来的域名史与官方 / 档案材料都指向：

```text
oicq.com
oicq.net
tencent.com
```

1999 第一版 OICQ 通过网络下载站 / 线上渠道传播，但本轮没有取得一个符合 METHOD 要求、能够实际核验：

- capture datetime；
- original URL；
- HTTP replay state；
- page body；
- charset；
- subresources；

的 1999 OICQ 下载页 / 官网 historical memento。

本轮尝试了 OICQ / Tencent 1999 locator 检索，但没有取得可打开核验的合格 archive capture。

所以准确结论是：

```text
historical domain identity: high-confidence lead
current official historical content: achieved
contemporaneous press evidence: achieved
verified 1999 homepage/download memento: NOT achieved
verified original OICQ binary provenance: NOT achieved
original server/runtime: NOT achieved
```

不能写：

> Wayback 没保存 OICQ。

只能写：

> **本轮没有取得 verified capture。**

---

## 13. 为什么 current Tencent history page 也需要做 provenance 分层

腾讯现在的：

- 1999-04-07 Mobile Email；
- 1999-07-11 email-to-pager；

都是非常好的 source leads。

但它们同时属于一种本仓已经多次遇到的 artifact：

**current live legacy representation**。

研究记录应至少拆成：

```yaml
publisher: Tencent
current_host: tencent.com
internal_historical_date: 1999-07-11
current_access: 2026
historical_capture_verified: false
content_claim: first-party historical statement
historical_page_form: unknown
```

原因很简单：

- 文本可能经过 CMS 迁移；
- URL 很可能不是 1999 原 URL；
- 英文页面可能是后来翻译 / 重排；
- 现代 CSS / template 不代表旧站视觉；
- 内部历史日期不是 Memento-Datetime。

---

## 14. Archive 中最容易消失的是“跨网络执行能力”

对 1999 online paging 来说，最难保存的不是标题和正文，而是整个依赖链：

```text
browser / account configuration
↓
mail server / OICQ server
↓
filtering / routing logic
↓
pager station / SMSC gateway
↓
telecom account / number mapping
↓
radio network
↓
physical pager / GSM phone
```

Web archive 通常更容易保存上端的一张说明页；真正让服务成立的中间层：

- private database；
- telecom routing；
- authentication secrets；
- carrier agreements；
- radio network；
- active subscriber mapping；

几乎不会和页面一起被保存。

所以这个案例特别适合未来 M3 的不是“把网页画回来”，而是建立：

**`end-to-end executability boundary`**。

即：能恢复到哪一层，就在哪一层停下来，不用模拟出来的网关假装 historical original。

---

## 15. 海外比较：late-1990s email / Web ↔ pager convergence 不是中国独有

### 15.1 1996：美国普通家庭也遇到 pager 的 callback dependency

Washington Post 1996 同期采访一对母女：母亲经常在外工作，beeper 让她们终于可以互相叫到，但母亲随后发现路上电话亭不足，难以立即回复，最终增加 cellular phone。

- Washington Post, “Keeping in Touch”, 1996-11-07.  
  https://www.washingtonpost.com/archive/lifestyle/1996/11/08/keeping-in-touch/c191c6b0-26b5-4e2d-994a-b87b605737de/

### 15.2 1997 SkyTel：Web / email 已经可以直接把消息送到 two-way pager

WIRED 1997 的长期使用体验写得非常清楚：SkyTel two-way pager 可以接收来自 email、SkyTel Web 页面和 800 电话的消息，并能直接回复，而不必再找电话。

- WIRED, “Wireless Gets Real”, 1997-10.  
  https://www.wired.com/1997/10/es-wired/

因此：

```text
email / web
→ pager
```

这种跨网融合本身不是中国特有。

中国材料真正需要比较的是：

- physical paging 用户规模大；
- household PC / Internet 仍相对稀少；
- “网上寻呼”同时又变成 Internet IM 的产品语言；
- 2000–2001 运营商 SMS 网关迅速把 OICQ identity 拉进手机网络。

---

## 16. Claim ledger

| Claim | Evidence | Grade | Confidence |
|---|---|---|---|
| 1999 年底国信 paging network 已开通“网上寻呼”到全国/省级寻呼网络 | 信息产业部统计汇编 | A | high |
| 1999 腾讯宣称试运行 email-to-pager / GSM SMS 系统 | Tencent current official historical page | A-/B+ | high for claim, medium for historical page form |
| 2000 同期媒体把 OICQ 称作“网上寻呼” | 长江日报现场报道 | B+ | high |
| CNNIC 1999→2000 “网上寻呼机”使用项从约15%升到21% | CNNIC 同期报告 | A-/B+ | high for reported category |
| CNNIC 的该类别可以直接等同 physical pager gateway | no | — | **unsupported** |
| 2001 mobile OICQ 使手机 SMS 用户可与 PC OICQ 用户互通 | 2001 同期报道 | B+ | high |
| 2026 resurrected OICQ is historical original runtime | modern reconstruction only | D | low / unsupported as original |
| 本轮已取得 1999 OICQ verified archive capture | no | — | **not achieved** |

---

## 17. “已证实 / 高概率 / 不知道”

### 已证实

- 1999 主管部门统计中确实存在 physical pager network 的“网上寻呼”服务表述。
- Tencent current official historical content 记录了 1999 email-to-pager / GSM gateway 方案。
- 2000 同期新闻明确把 OICQ 称作“网上寻呼”。
- CNNIC 报告中确实存在“网上寻呼机”统计项。
- 2001 mobile OICQ 已实现 GSM SMS ↔ OICQ 的跨网通信。

### 高概率

- 1999–2000 的“网上寻呼机”统计类别至少与 OICQ / ICQ 式 IM 高度相关，而不是单指 physical pager gateway。
- “pager”这一已熟悉的社会技术范畴为 OICQ 的早期产品命名和用户理解提供了现成隐喻。

### 不知道

- 国信网上寻呼的用户端原始 URL、UI、HTML、浏览器要求。
- CNNIC 原始问卷题项是否列出示例产品，以及 15% / 21% 的精确编码边界。
- 1999 Tencent email-to-pager 的真实用户量、成功率、资费。
- 1999 OICQ 首版官网 / 下载页两个可核验 historical timepoints。
- 原 OICQ server protocol 和全部在线功能状态。

---

## 18. 隐私、版权与复原边界

本轮没有复制：

- 普通用户 OICQ 号码；
- 普通用户 pager number；
- 私人聊天内容；
- 第三方 OICQ binary；
- 现代“复活版”服务器代码。

对 2000 学生现场材料只抽取支持技术 / 生活 claim 的最少行为信息，不将未成年人的历史个人信息进一步结构化扩散。

未来若找到原始 OICQ binary：

- 先记录 hash / filename / provenance / source；
- 版权不明时不直接提交 binary；
- runtime reconstruction 必须标 D；
- 自建替代 server 不能伪装成 historical server。

---

## 19. 对 M1 / M3 的实际推进价值

本轮没有完成 M1，但给出一个非常具体的候选实验族。

### M1 所需仍缺

```text
[ ] 1999/2000 OICQ or online-paging verified memento #1
[ ] second historical timepoint
[ ] original/candidate binary with provenance
[ ] resource missing list from actual capture
[ ] contemporary screenshot/manual independent source
```

### M3 可以测试

若以后取得 OICQ 1999 binary：

```text
Win98/Win95 environment
vs
modern Windows
```

至少测试：

- executable launches；
- hard-coded server / DNS；
- login behavior without historical backend；
- character encoding；
- sound assets；
- network failure mode；
- server substitute 所需最小协议；
- modern compatibility 是否掩盖 historical networking differences。

若取得 physical online-paging Web page：

重点不是视觉，而是：

- login/auth；
- pager number input；
- message length；
- carrier/network selection；
- fee / quota；
- delivery acknowledgement；
- IE/JS/charset；
- server-side gateway dependency。

---

## 20. 本轮状态

```text
subject identity disambiguation: achieved
physical online-paging institutional evidence: achieved
1999 email-to-pager transaction description: achieved
OICQ terminology collision evidence: achieved
2001 SMS↔OICQ bridge evidence: achieved
international comparator: achieved
verified 1999 historical Web memento: NOT achieved
verified original OICQ runtime: NOT achieved
M1 complete case: NOT achieved
```

本轮的实质推进不是“又发现一个旧网站”，而是纠正一个会污染后续数据集的分类错误：

> **1999–2000 的“网上寻呼”不是一个单义词。**

同一个时代里，它既可以指 Internet 到 physical pager network 的网关，也可以指 OICQ / ICQ 这样的 Internet 即时通信。

如果把这两者混起来，用户比例、平台谱系、页面 locator、技术栈和生活史解释都会一起错位。
