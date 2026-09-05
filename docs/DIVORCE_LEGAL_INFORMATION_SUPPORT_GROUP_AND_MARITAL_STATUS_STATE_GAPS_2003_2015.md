# DIVORCE_LEGAL_INFORMATION_SUPPORT_GROUP_AND_MARITAL_STATUS_STATE_GAPS_2003_2015

> 适用范围：约 2003–2015 年中文旧网中的离婚法规/办事说明、离婚求助与经验页、QQ/论坛等同状态支持网络的公开痕迹，以及平台自填/虚拟婚姻状态与现实法律状态之间的证据缺口。
>
> 跨仓生活史主文档：
> <https://github.com/tmzncty/how-people-lived/blob/main/topics/marital-exit-post-divorce-household-reconstruction-and-family-reversibility-china-1980-2026.zh-CN.md>
>
> 本文不写“中国离婚史总论”，也不把 `old-web-archaeology` 扩成婚姻家庭史。这里只回答一个旧网考古问题：
>
> **当中文旧网留下“离婚怎么办”“我已离异”“单亲妈妈群”“虚拟结婚/离婚”等页面时，这些 artifact 到底能证明现实婚姻状态转换链的哪一步？**

---

## 0. 与既有文档的边界

本仓已经有：

- `DATING_PROFILES_SEARCH_FILTERS_OFF_PLATFORM_HANDOFF_AND_RELATIONSHIP_OUTCOME_GAPS_2002_2012.md`：婚恋 profile、搜索、匹配、站外联系与关系结果；
- `FORUM_THREAD_GROUP_LIFE_SCRIPT_VISIBILITY_AND_TEMPORAL_STATE_GAPS_1995_2015.md`：论坛/群组中人生脚本的可见性；
- `CONTACT_ENDPOINT_LIFECYCLE_1997_2003.md` 与 `CONTACT_STACK_AND_CHANNEL_HANDOFF_1998_2002.md`：联系方式和通道切换；
- `APPLICATION_STATE_ELIGIBILITY_AND_ROUTE_PORTFOLIO_2003_2015.md`：申请与资格状态；
- `ABANDONED_APPLICATIONS_AND_NEGATIVE_STATE_SURVIVAL_2007_2015.md`：放弃和负状态保存偏差。

本文不重复“怎样找到对象”或一般论坛研究。

新增研究单位是：

> **legal-information state + support-channel state + self-reported marital-status state + real civil-status transition + post-divorce outcome gap**

即：页面里写了什么、用户看到了什么、用户自称什么、现实法律状态是什么、之后生活实际变成什么，全部分开。

---

# 1. 研究单位：不要把一张“离婚页面”当成离婚已经发生

建议把相关链路至少拆成：

```text
real marital relationship
→ conflict / separation / uncertainty
→ information need
→ search / direct navigation / recommendation
→ legal-info or peer-support page encounter
→ rule/version applicability check
→ advice or emotional support received
→ user decision
→ registration or litigation route
→ application accepted
→ statutory waiting / review if applicable
→ legal dissolution
→ civil-registry state updated
→ property / debt / child arrangements
→ support actually performed
→ post-divorce household reconstruction
→ optional self-reported platform status / repartnering
```

建议字段：

```yaml
artifact_type:
platform_or_site:
page_url:
page_publication_date:
claimed_rule_date:
applicable_jurisdiction:
rule_version_verified:
page_visibility:
user_encounter_evidence:
self_reported_marital_status:
legal_status_evidence:
peer_support_channel:
off_platform_private_channel:
registration_or_case_evidence:
post_divorce_outcome_evidence:
archive_capture:
source_grade:
confidence:
privacy_notes:
```

核心边界：

> **page says “divorce procedure” ≠ page reflects current law**

> **page published in 2009 ≠ legal text is valid in 2009**

> **user says “准备离婚” ≠ application filed**

> **user says “已离” ≠ civil registry verified**

> **platform status says “离异” ≠ legal marital status**

> **advice received ≠ advice followed**

> **application accepted ≠ divorce completed**

> **divorce certificate ≠ property / custody / support execution completed**

> **support group exists ≠ private support exchanges are archived**

这套状态机应复用于以后所有离婚求助、婚姻状态字段和相关旧网 case。

---

# 2. 2003：法规版本本身就是旧网页面必须记录的状态

2003 年 10 月 1 日起施行的新《婚姻登记条例》规定，内地居民协议离婚需要提交的主要证件和材料包括户口簿、身份证、结婚证和双方共同签署的离婚协议书。

民政部门当年的公开解释特别指出：新条例取消了此前所在单位、村民委员会或居民委员会出具介绍信的要求。

来源：

- 国家卫生健康委员会保存的《婚姻登记条例》，2003-08-08：
  <https://www.nhc.gov.cn/wjw/flfg/200308/e2813d5724c44fe7bff26cdf9f28945d.shtml>
- 中新网，2003-08-20，《民政部官员称新婚姻登记条例更加保障婚姻自由》：
  <https://www.chinanews.com.cn/n/2003-08-20/26/337148.html>

### 证据等级

- 条例：**A；**
- 同期政策报道：**B，包含民政部门解释。**

### old-Web 结论

从这一节点开始，任何 2003 年以后中文网页如果仍把“单位 / 居委会介绍信”写成现行协议离婚必需材料，都必须首先检查：

1. 页面正文实际写作时间；
2. 页面是否是旧文转载；
3. 页面 publication timestamp 是否只是 CMS 上线/迁移时间；
4. 是否是地方特殊流程，还是错误沿用旧规则；
5. 是否明确标注适用年份。

因此：

> **legal-information page has its own version state。**

不能把网页发布日期直接当法规有效期。

---

# 3. 2006：天涯“虚拟户籍/婚姻”说明平台婚姻状态可以完全脱离现实民政状态

2006 年《重庆商报》经新浪科技保存的同期报道，描述天涯社区内一种由网友运营的“网络户籍”/虚拟民政系统。报道称用户可在虚拟体系中办理“结婚”“离婚”等操作，并由社区内部的“民政部门”修改或注销对应户口状态。

来源：

- 重庆商报 / 新浪科技，2006-07-17，《天涯论坛实施网络户籍管理制 创意缘于版主去世》：
  <https://tech.sina.com.cn/i/2006-07-17/10151040270.shtml>

### 证据等级

**B：同期媒体对平台社区实践的报道。**

### 能写的 claim

> 2006 年天涯已有被媒体观察到的虚拟婚姻/户籍玩法，社区内部状态可以出现“结婚”“离婚”等转换。

### 不能写的 claim

- 这些字段与现实婚姻登记数据库有任何同步；
- 用户填写或社区维护的“已婚/离异”一定对应现实状态；
- 虚拟“离婚”代表现实关系解除；
- 当前还能找到的天涯残页就是当年该系统的原 DOM。

核心规则：

> **platform marital state ≠ civil marital state。**

并且：

> **virtual divorce event ≠ legal divorce event。**

这是以后读取旧 SNS、论坛、婚恋平台“婚姻状态”字段时必须保留的证据边界。

---

# 4. 2009：一个非常有价值的“过时法律页面”反例

110 法律咨询网存在一篇标注 2009-02-13 的《协议离婚须知》页面，且页面注明“文章来源：互联网”；正文仍列出“所在单位、村民委员会或者居民委员会出具的介绍信”等材料要求。

来源：

- 110 法律咨询网，页面标注 2009-02-13，《协议离婚须知》：
  <https://www.110.com/ziliao/article-61187.html>

但 2003 年新《婚姻登记条例》已经取消这一介绍信要求。

### 证据等级

- 页面本身：**B/legacy Web artifact；**
- 2003 条例与同期解释：**A + B，用于判定法律版本。**

### 为什么这一页非常重要

它证明旧网考古里存在一种容易被忽略的风险：

> **stale legal-content hazard——过时法律内容风险。**

页面可以：

- 在后来日期被 CMS 重发；
- 从旧稿复制；
- 保留已经失效的法规步骤；
- 在搜索引擎里仍可能继续被发现；
- 页面模板和日期看起来完全“现代”。

所以：

> **page timestamp ≠ legal currency。**

> **search visibility ≠ procedural correctness。**

> **still online ≠ still applicable。**

尤其不能从“2009 网页写了介绍信”反推出“2009 全国办理离婚仍普遍需要介绍信”。

### 目前还不知道

- 这段正文最初写于何年；
- 该页面是否是 2009 新发还是旧文迁移；
- 搜索引擎当年是否实际高排名；
- 有多少用户因此准备了已经不需要的材料；
- 页面是否曾被编辑而 archive 未保留版本链。

这些都应保持 unknown。

---

# 5. 2010：媒体可以证明单亲母亲使用 QQ 群，但不能替我们保存私人群聊

2010 年《北京晚报》/新浪保存的同期采访记录一名离异单亲母亲林颖（化名）。报道说，她离婚后不愿向熟人倾诉、又负担不起持续心理咨询，后来加入单亲妈妈 QQ 群，并把群友之间的倾诉和经验交换描述为自己渡过困难时期的重要支持。

报道同时保留了一个关键反例：她的前夫有时不支付抚养费，群友建议通过法院、执行或其他方式追索，但她本人没有照做。

来源：

- 北京晚报 / 新浪，2010-10-27，《北京单亲母亲生存调查：再婚问题成最大障碍》：
  <https://news.sina.com.cn/c/sd/2010-10-27/174421364056.shtml>

### 证据等级

**B：同期记者采访；个案不可外推。**

### 这份证据能证明什么

> 至少对一名被同期媒体采访的离异女性而言，QQ 群是现实使用的同状态支持通道。

它还能证明：

> **advice received ≠ action executed。**

群友给出法律执行建议，不等于建议被采用，也不等于法院程序开始，更不等于抚养费最终到账。

### 它不能证明什么

媒体报道不能替代：

- 群号；
- 群成员名单；
- 私人聊天记录；
- 精确 QQ 客户端版本；
- 消息存储方式；
- 群里所有人的真实婚姻状态；
- 群规模和活跃度。

因此：

> **reported group use ≠ archived private group corpus。**

而且这里应主动执行隐私 stop condition：

> **研究群组作为生活基础设施，不等于应该寻找、恢复或重新公开私人群聊。**

---

# 6. “离异” profile 字段与既有婚恋网站研究的接口

本仓已有 `DATING_PROFILES_SEARCH_FILTERS_OFF_PLATFORM_HANDOFF_AND_RELATIONSHIP_OUTCOME_GAPS_2002_2012.md`，已经讨论 profile、搜索、消息、站外联系和关系结果。

本文只补一个容易被忽略的边界：

```text
self-reported marital-status field
≠ platform verification
≠ legal registry state
≠ current lived relationship state
```

例如一个旧婚恋 profile 显示：

```text
婚姻状况：离异
```

它至多证明：

> 某个 profile version 在某个时点向访问者呈现了“离异”这一状态。

除非平台当时明确有可核验的认证流程，并且 evidence 足以证明该用户通过了对应认证，否则不能升级为：

> “此人法律上已经完成离婚登记”。

即使法律状态是真的，也不能自动推出：

- 财产已经分清；
- 抚养费已经履行；
- 与前配偶已经完全停止联系；
- 已经形成稳定的新住户；
- 当前正在寻找再婚。

---

# 7. 建议状态机：法律信息、支持和现实状态必须分层

以后相关 case 建议使用三条互相交叉但不可互换的状态轴。

## 7.1 legal-information axis

```text
rule enacted
→ public explanation published
→ Web page created
→ page indexed / linked
→ user encounters page
→ user identifies jurisdiction/version
→ user interprets correctly
→ rule applied to actual procedure
```

核心 gap：

> **rule exists ≠ page current ≠ user sees ≠ user understands ≠ user qualifies。**

## 7.2 support axis

```text
support space exists
→ user discovers it
→ user joins / reads
→ user receives response
→ advice or emotional support is useful
→ user acts / does not act
→ real-world outcome
```

核心 gap：

> **group exists ≠ user encountered ≠ message read ≠ advice followed ≠ outcome caused。**

## 7.3 marital-status axis

```text
real relationship state
→ user self-description
→ platform field
→ platform verification state
→ civil-registry state
→ public/private document
→ downstream institutional records
```

核心 gap：

> **profile status ≠ verified identity ≠ registry status ≠ all downstream records updated。**

---

# 8. 页面日期与“历史真相”之间至少有五层时间

离婚法规/办事页面尤其容易让人误读日期。

建议每条至少分开：

1. `rule_effective_date`：法规从何日有效；
2. `text_authored_date`：正文何时写成；
3. `page_published_date`：CMS 页面显示何时发布；
4. `archive_capture_datetime`：档案何时抓到；
5. `user_encounter_date`：某个现实用户何时真的看到。

它们可以完全不同。

一个 2009 URL 可以承载 2003 以前的旧文本；一个今天仍在线的政府历史页可以准确保存 2003 法规，但它今天的 HTML/模板并不是 2003 原页面。

所以：

> **content-history time ≠ page-container time。**

这条应当加入以后所有中文旧网法规/办事页的 evidence checklist。

---

# 9. 断裂高可见、普通重建低可见

旧网特别容易留下：

- “我要不要离婚”的求助；
- 离婚程序问答；
- 极端冲突；
- “离异”婚恋 profile；
- 再婚征友；
- 法律纠纷。

但一个人离婚两年以后：

- 正常上班；
- 接送孩子；
- 每月交房租；
- 没有再发求助帖；
- 没有再婚；
- 生活逐渐稳定；

这些最不容易成为可搜索 artifact。

因此：

> **rupture visibility / ordinary-reconstruction darkness——断裂高可见、普通重建黑区。**

也要警惕：

> **crisis-thread survival bias——危机帖幸存偏差。**

只看保存下来的离婚论坛，很容易把 post-divorce life 误写成永久危机。

---

# 10. 公共壳层保存得最好，真正关键的私人状态本来就不应公开

公开 archive 比较可能保存：

- 法规；
- 办事指南；
- 法律咨询页；
- 新闻；
- 公开论坛帖；
- 婚恋 profile 的公开字段；
- 平台帮助页。

通常不会、也不应该公开保存：

- 民政登记数据库；
- 身份证件；
- 离婚协议全文；
- 孩子信息；
- 财产和银行账户；
- 私人 QQ 群聊；
- 抚养费转账；
- 法院执行中的敏感材料；
- 私人心理咨询记录。

因此这里存在：

> **public-advice-shell / private-life-state asymmetry——公共建议壳层 / 私人生活状态不对称。**

档案“缺失”有时是隐私保护的正常结果，不是单纯的 archive failure。

---

# 11. 一张旧网页真正能证明什么：最小 claim 示例

## 可以写

> 2009 年一个今天仍可访问的中文法律咨询页面，其正文仍列出单位/村居委会介绍信作为协议离婚材料，而 2003 年新条例已经取消了这一要求；因此旧网法律页面的显示日期不能直接作为法规有效性证据。

## 不可以写

> 2009 年中国办理离婚仍然需要单位介绍信。

---

## 可以写

> 2010 年同期新闻采访记录一名离异单亲母亲使用单亲妈妈 QQ 群获得同状态支持。

## 不可以写

> 2010 年单亲妈妈普遍依赖 QQ 群。

---

## 可以写

> 2006 年同期报道显示天涯社区存在社区内部“虚拟婚姻/离婚”状态实践。

## 不可以写

> 天涯用户的婚姻状态字段可用于验证现实婚姻。

---

# 12. 证据表

| Claim | Evidence | Grade | Confidence | Boundary |
|---|---|---:|---:|---|
| 2003 新条例取消单位/村居委会离婚介绍信 | 2003 条例 + 民政部同期解释 | A + B | high | 不等于所有地方执行摩擦当天消失 |
| 2006 天涯有虚拟婚姻/离婚状态实践 | 重庆商报 / 新浪科技同期报道 | B | medium-high | 未验证原系统 DOM/数据库 |
| 2009 某法律页仍展示旧介绍信要求 | 110 legacy page + 2003 法规对照 | B + A | high for contradiction | 页面正文原始写作时间 unknown；页面自称文章来源为互联网 |
| 2010 单亲母亲使用 QQ 群获得支持 | 北京晚报 / 新浪采访 | B | medium-high for individual case | 不代表总体；无私人群聊 corpus |
| profile “离异”不能自动证明民政状态 | 状态模型 + 既有 dating research | D supported by system distinction | high as methodological rule | 具体平台验证能力须逐案检查 |

---

# 13. 浏览器、编码和动态状态：本轮仍然没有 M1 级 historical capture

本轮获得的是：

- 今天仍可访问的历史法规页面；
- legacy 法律咨询页面；
- 同期新闻对天涯/QQ 使用的描述；
- 既有 dating-profile 研究的状态边界。

**本轮没有实际取得并检查一份满足 M1 的 2003–2015 中文“离婚求助 / 办理 / 支持群组”历史 Wayback/WARC transaction capture。**

因此以下内容全部继续标记为 `unknown`：

- 2003–2010 某原始离婚办事页的 historical original URL；
- capture datetime；
- HTTP headers；
- charset；
- 原 DOM / frameset / JS；
- historical form action；
- cookie/session；
- QQ 群客户端具体 UI 与消息持久化；
- 天涯虚拟户籍系统的真实数据库 schema；
- 一个用户看到过哪一版法规页面；
- 一个现实离婚登记 transaction 的后台状态。

不能把今天仍在线的 legacy page 冒充成当年的 DOM，也不能因为媒体描述“QQ 群”就复原一个私人群组。

---

# 14. 隐私 stop condition

这一题比普通旧网页更需要主动停止。

禁止为了“完整历史”去：

- 搜集普通人的身份证、离婚证、协议书；
- 批量恢复已经删除的婚姻求助帖；
- 寻找泄露的婚姻登记数据库；
- 重新公开孩子姓名、学校、住址；
- 进入或测试仍存在的私人支持群；
- 将匿名/化名人物反向识别。

优先保存：

- URL；
- 页面日期；
- 法规版本；
- 页面结构/字段类型；
- 公开 claim；
- archive metadata；
- 状态缺口分析。

---

# 15. 下一步最值钱的旧网 artifact

不是更多“离婚率新闻”，而是以下任一对象：

1. 一份 **2003–2006 官方婚姻登记办事页的 verified capture**，能直接比较法规更新前后页面内容；
2. 一个 **2005–2012 公开离婚/单亲支持论坛 thread 的 verified capture**，同时有 original URL、capture time、分页/编辑/删除状态；
3. 一份 **历史婚恋平台婚姻状态字段的官方帮助页或认证说明**，用于区分 self-report 和 verification；
4. 一条同一法律咨询 URL 的多个历史 capture，用来研究旧法规内容何时被更新、迁移或继续错误保留。

如果找到以上 artifact，优先回答：

> **Web 是怎样把婚姻退出变得“更容易知道怎么办”的，而不是把“知道怎么办”误写成“现实里已经办完、分完、养育安排也稳定”。**

---

# 16. 对 old-Web 考古方法的新增贡献

这一题最终增加了五条可复用的方法规则：

1. **page timestamp ≠ legal currency**；
2. **platform marital state ≠ civil marital state**；
3. **reported support-channel use ≠ archived private conversation**；
4. **advice encountered ≠ advice acted upon ≠ outcome**；
5. **public rupture artifact survives better than ordinary reconstruction**。

它们不只适用于离婚。

以后研究：

- 社保政策；
- 招生规则；
- 户籍办事；
- 劳动法规；
- 房产交易；
- 医疗资格；

都必须问同一个问题：

> **这个旧网页保存的是一条当时有效、被现实用户正确应用的制度接口，还是一段后来仍漂在 Web 上的旧说明？**
