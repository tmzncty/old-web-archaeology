# 2001—2005：证件门控的共享接入、场所身份绑定与平台化名

本文件补充：

- `docs/METHOD.md`；
- `docs/AFFILIATION_CREDENTIAL_AND_ACCOUNT_LIFECYCLE_2001_2009.md`；
- `docs/CONTACT_STACK_AND_CHANNEL_HANDOFF_1998_2002.md`。

主研究对象仍是约 1995—2015 年中文互联网。这里不把仓库扩成一般监管史，而是处理旧网页、论坛、QQ/BBS 叙事里很容易发生的一类身份误判：

> **平台上显示昵称，不等于现实接入过程没有身份核验；反过来，网吧柜台核验过身份证，也不等于我们可以把某个昵称、帖子或账号直接绑定到那个现实身份。**

这和已有的 `AFFILIATION_CREDENTIAL_AND_ACCOUNT_LIFECYCLE_2001_2009.md` 处理的是两个不同层级：

- 已有文档：学校邮箱、校园 IP、机构账号如何成为**平台注册资格**；
- 本文档：身份证、学生证、实名上网卡等如何成为**物理/共享接入场所的准入凭证**，以及场所会话记录与平台账号之间的证据边界。

核心规则：

```text
physical-access credential ≠ platform-admission credential
venue identity record ≠ platform account identity
platform pseudonym ≠ anonymous access session
```

---

## 1. 先画完整链条，不从页面昵称直接跳到现实身份

研究一条来自网吧/共享终端的历史帖子，最低模型应当是：

```text
现实中的人
→ 身份证 / 学生证 / 其他有效证件
→ 场所准入
→ 某台终端 / 某个时段
→ Internet 会话
→ 平台登录 / 注册
→ 昵称 / 账号
→ 帖子 / 聊天 / 页面 artifact
```

每一个箭头都需要自己的证据。

例如：

- 一份法规可以证明某时期**要求**核验身份证；
- 一篇现场报道可以证明某家网吧**实际是否核验**；
- 一张登记表可以证明某现实身份与某次场所会话有关；
- 平台日志才可能进一步证明这次会话访问了某个平台账号；
- 单独一条 BBS 帖子通常只能证明某昵称/账号在页面层出现。

除非这些层之间存在可复核的绑定，否则不得跨层补全。

---

## 2. 2001：共享接入已经出现“证件 + 年龄 + 时段”层

2001 年 4 月新华社关于武汉整治网吧的同期报道记载，当地暂行办法要求：

- 顾客出示身份证或其他有效证件；
- 16 岁以下学生可使用学生证；
- 每次上网登记；
- 未成年人还受到工作日、夜间等时段限制。

来源：

- 新华社，《武汉全面整治网吧 上网需出示身份证》，2001-04，经新浪科技保存：<https://tech.sina.com.cn/i/c/61839.shtml>

证据等级：**B：同期新华社报道。** 本轮尚未定位武汉该暂行办法的独立原始公报文本。

同月全国《互联网上网服务营业场所管理办法》要求营业场所记录有关上网信息并保存 60 日，同时对未成年人采取分级时段限制。

来源：

- 《互联网上网服务营业场所管理办法》，2001-04，经新华社/新浪保存：<https://tech.sina.com.cn/i/c/62289.shtml>

证据等级：**A/B 边界：同期规范文本由新华社/门户保存。**

### 考古意义

历史页面如果写“我在网吧上网”，不能只记录：

```yaml
access_channel: internet_cafe
```

还应问：

- 当时当地的年龄规则是什么；
- 哪类证件被接受；
- 是否要求逐次登记；
- 规则是只存在于纸面，还是该场所确实执行。

因为同一个“网吧”标签，在不同年份可能对应完全不同的准入过程。

---

## 3. 2002：规则版本变化会直接改变同一人的合法接入路径

2002 年 9 月公布、11 月施行的《互联网上网服务营业场所管理条例》规定：

- 营业性互联网上网服务场所不得接纳未成年人；
- 营业时间限于每日 8 时至 24 时；
- 经营单位应核对、登记上网消费者身份证等有效证件；
- 记录有关上网信息并保存不少于 60 日。

来源：

- 国务院令第 363 号，2002-09-29；原 2002 年文本数字化版本：<https://zh.wikisource.org/zh-hans/互联网上网服务营业场所管理条例_(2002年)>
- 中国新闻网，2002-11-14 实施报道：<https://www.chinanews.com.cn/2002-11-14/26/243706.html>

证据等级：

- **A：法规文本；** 当前使用的是后来数字化呈现，若进入完整 case，应继续与正式公报/法规库互校；
- **B：同期实施报道。**

条例第二条又明确把学校、图书馆等内部为特定对象提供的非营业性上网场所排除在该条例适用范围之外。

因此：

```text
commercial internet-cafe channel closed
```

不能写成：

```text
person disappeared from the Internet
```

他仍可能通过学校机房、图书馆、家庭、朋友设备或其他渠道接入。

> **commercial-channel restriction ≠ total network exclusion**

这是一条旧网人口史必须保留的边界。

---

## 4. credential possession ≠ service eligibility

1985 年居民身份证制度要求年满 16 周岁公民申领居民身份证；2003 年通过、2004 年施行的居民身份证法又规定，未满 16 周岁公民可以自愿申请领取居民身份证。

来源：

- 1985 年《中华人民共和国居民身份证条例》数字化文本：<https://www.muhn.edu.cn/bwb/info/1040/1298.htm>
- 2003 年《中华人民共和国居民身份证法》，上海市政府保存文本：<https://www.shanghai.gov.cn/nw10486/20200813/0001-10486_707.html>

证据等级：**A：法律文本。**

但一个 15 岁少年即使在 2004 年已经持有身份证，也不能因此推出他符合营业网吧的年龄准入条件。

因此必须把：

```text
has acceptable credential?
```

和：

```text
is eligible for this service?
```

分开。

旧网考古遇到学生证、身份证、校园卡、单位证件时都应适用同一原则：

> **证件能证明某种身份属性，不自动产生某项服务资格。**

---

## 5. ID required in rule ≠ ID checked in practice

2002 年条例施行后不久的同期现场报道仍记录：

- 网吧有登记；
- 但登记内容可能虚假；
- 明显未成年人仍能进入。

来源：

- 人民网稿件经中国教育网保存，《未成年人自由出入 “网吧禁令”形同虚设？》，2002-11：<https://www.edu.cn/edu/ji_chu/ji_jiao_news/200603/t20060323_63608.shtml>

2003 年杭州的现场检查更具体：一家网吧入口有“凭有效身份证登记入场”标牌，但一名 16 岁女孩对记者称，营业员没有核验身份证，她自己填写登记后便进入。

来源：

- 《浙江日报》经新浪教育保存，《杭州网吧禁止未成年人入内》，2003-08-22：<https://edu.sina.com.cn/l/2003-08-22/51788.html>

证据等级：**B + embedded contemporary self-report。**

因此证据字段必须拆成：

```yaml
credential_rule_exists: true
identity_check_observed: true/false/unknown
user_admitted: true/false/unknown
```

绝不能仅凭法规把 `identity_check_observed` 自动填为 `true`。

同样：

> **prohibited ≠ absent**

历史上确有违规进入，不等于违规是无成本、普遍或容易的。研究应记录执行差异，而不是把绕过规则浪漫化。

---

## 6. 2003：身份绑定从手写登记向扫描/卡片式会话推进

2003 年北京一篇同期报道记录，一名成年网民第一次去某网吧时必须让机器“扫描”身份证，并因此担心身份证信息会不会被滥用。

来源：

- 《北京娱乐信报》经新浪保存，《杜绝未成年人进入 首次进网吧须“扫”身份证》，2003-11-23：<https://news.sina.com.cn/s/2003-11-23/02181168748s.shtml>

证据等级：**B + 同期个人反应。**

同年辽宁和福建还出现了用身份证办理实名上网卡、进入网吧刷卡认证的试点/推广报道。

来源：

- 新华社经新浪科技，《辽宁省网吧将实行上网实名制 上网持“一卡通”》，2003-03-03：<https://tech.sina.com.cn/i/c/2003-03-03/1047169113.shtml>
- 中国新闻网，《福建网吧年内全采用上网实名制》，2003-08-13：<https://www.chinanews.com.cn/n/2003-08-13/26/334646.html>

证据等级：**B：同期实施报道。**

### 不要把不同技术版本揉成一个“实名制”

至少应区分：

```text
staff visually checks document
→ handwritten register
→ document photocopy / scan
→ local access card
→ regional shared card/database
→ later account / mobile-phone verification
```

这些实现的：

- 数据保存方式；
- 查询能力；
- 单次使用摩擦；
- 隐私感受；
- 与网络会话的绑定强度

都不同。

所以旧网技术史里的 `identity infrastructure` 必须像浏览器、编码和账号规则一样**按版本记录**。

---

## 7. layered identity provenance：身份必须分层追溯

建议以后遇到“实名 / 匿名 / 半实名”这类词时，先拆成至少四层：

### A. physical-person layer

现实中的自然人。

### B. access-venue layer

网吧、学校、单位、图书馆等是否知道或记录使用者身份。

### C. network/session layer

是否存在终端、时间、卡号、账号、IP 等会话级标识。

### D. platform-presentation layer

QQ 号、BBS ID、聊天室昵称、博客署名、SNS 资料如何向其他用户显示。

因此完全可能出现：

```text
A/B/C 层高度可追踪
D 层仍显示化名
```

也可能出现：

```text
D 层资料声称是真名
但 A↔D 没有独立绑定证据
```

所以：

> **real-name looking profile ≠ verified physical identity**

> **pseudonymous profile ≠ unrecorded physical access**

---

## 8. 旧网页本身通常看不见“进门以前”发生的事

Wayback、Common Crawl 或保存下来的 BBS dump 比较容易留下：

- 帖子；
- 账号页；
- 站点帮助；
- 网吧广告/价格页；
- 门户新闻；
- 论坛上对规则的讨论。

它们通常不会留下：

- 柜台手写登记簿；
- 60 日后按规则销毁/覆盖的会话记录；
- 一次刷卡失败；
- 一个忘带证件后转身离开的普通用户；
- 一个未成年人被店员拒绝的平常下午。

我把这种保存偏差称为 **access-layer invisibility（接入层不可见性）**。

这意味着今天研究旧网时，最容易看到的是：

> “已经成功进入网络的人留下了什么。”

却不容易看到：

> “谁在终端前就被筛掉了。”

因此：

```text
archived user population ≠ eligible population ≠ attempted-access population
```

更不能把 archive 里留下来的用户样本直接当成当年“想上网的人”的总体。

---

## 9. record-retention rule ≠ archival survival

2001/2002 规则中的“保存 60 日”首先是当时运营/管理要求，不是历史档案制度。

因此：

```text
log required in 2002
```

不意味着：

```text
log should still exist in 2026
```

旧网考古不应因为今天找不到这些日志，就怀疑它们当年从未存在；也不应主动寻找、汇总或重新公开包含普通个人身份信息的历史登记记录。

### 隐私边界

即使偶然遇到幸存的：

- 身份证号；
- 真实姓名 + 会话时段；
- 上网卡号；
- 电话；
- 详细地址；

本仓也应执行研究必要最小化，只记录支持结构性 claim 所需要的字段，不重新发布可重识别信息。

这里的研究对象是**身份基础设施怎样工作**，不是“找出某条历史帖子是谁发的”。

---

## 10. 海外校准：公共终端的证件门控不是中国独有

2005 年意大利的公共 Internet/通信终端也出现了用户身份证明要求。

同期规范文本要求经营者在提供服务前核验用户身份证件，并保存相关身份/使用记录。

来源：

- 意大利内政部 2005-08-16 decree（Wikisource 转录）：<https://it.wikisource.org/wiki/D.M._16_agosto_2005_-_Decreto_Pisanu>

同期《卫报》报道中，威尼斯一名经营者称当天已有多名顾客因没带证件无法使用；罗马一家服务大量移民顾客的 internet point 则称有部分顾客拒绝提供身份证明后离开。

来源：

- *The Guardian*, “Passport to surf”, 2005-09-29：<https://www.theguardian.com/news/blog/2005/sep/29/passporttosur>

证据等级：

- **A：同期规范文本；**
- **B：同期现场报道。**

这个对照只用于校准机制：

> **共享终端可以从“钱 + 空位”变成“钱 + 空位 + 可接受证件”。**

它不意味着两国制度原因、执行方式或网络文化相同，也不改变本仓中文旧网的 scope。

---

## 11. 与机构数字凭证文档的边界

`AFFILIATION_CREDENTIAL_AND_ACCOUNT_LIFECYCLE_2001_2009.md` 已经讨论：

```text
学校邮箱 / 校园 IP
→ 第三方平台接受该凭证
→ 平台账号建立
```

本文讨论：

```text
身份证 / 学生证 / 场所卡
→ 共享终端准入
→ 网络会话
→ 之后才可能进入平台
```

两个系统可能在同一个人身上叠加：

```text
身份证进入网吧
→ 打开校内网
→ edu.cn 邮箱完成平台注册
→ 用昵称发布内容
```

但四个身份层不能合并。

这一点对 2000s 中文旧网尤其重要，因为：

- 接入地点经常是公共/共享终端；
- 平台又可能依赖校园邮箱、手机号、邀请关系等另一套资格系统；
- 页面最终只显示昵称或 profile。

如果不拆层，很容易把“半实名”写成一个毫无解释力的总标签。

---

## 12. 建议字段

旧网案例涉及网吧、机房、图书馆或其他共享终端时，建议增加：

```yaml
access_context:
  venue_type: unknown  # commercial_cafe / school_lab / library / workplace / other
  observed_at: null
  age_rule: unknown
  business_hour_rule: unknown

physical_credential:
  required_by_rule: unknown
  accepted_types: []
  possessed_by_user: unknown
  checked_in_practice: unknown

identity_implementation:
  type: unknown  # visual_check / handwritten_register / id_scan / access_card / other
  session_binding: unknown
  record_retention_rule: unknown
  record_survival: unknown

network_session:
  terminal_id_observed: false
  session_time_observed: false
  ip_observed: false

platform_identity:
  platform: unknown
  visible_handle: unknown
  real_name_rule: unknown
  affiliation_credential_rule: unknown

venue_to_platform_binding:
  evidence: []
  confidence: none
```

### 默认值应当保守

尤其：

```yaml
physical_credential.checked_in_practice: unknown
venue_to_platform_binding.confidence: none
```

除非有独立证据，不因法规存在或昵称样式而自动升级。

---

## 反例与后见之明风险

### 反例 1：有身份证仍可能不符合服务资格

未成年人可能拥有身份证，但营业网吧仍禁止接纳未成年人。

因此：

```text
credential possession ≠ admission eligibility
```

### 反例 2：法规禁止不等于历史实践完全消失

同期现场报道记录过未成年人仍被放入网吧。

因此：

```text
prohibited ≠ absent
```

### 反例 3：看见昵称不等于匿名进入

平台只显示昵称时，接入场所仍可能知道现实身份。

因此：

```text
pseudonymous display ≠ anonymous access
```

### 反例 4：知道现实身份不等于知道发帖账号

即使保存了一次身份证登记，只要缺少会话/平台绑定，就不能把某个帖子归到那个现实人。

因此：

```text
venue record ≠ authorship proof
```

### 后见之明风险：把后来的实名体系倒灌到 2001—2003

手写登记、身份证扫描、区域上网卡、手机号码验证、平台实名账号，是不同年代、不同技术层和不同数据模型。

不要用后来的“互联网实名制”一个词抹平这些差异。

---

## 已证实 / 高概率 / 不知道

### 已证实

- 2001 年全国网吧管理办法已经要求保存上网信息，并对未成年人采用分级准入/时段规则。
- 2001 年武汉同期报道记录了身份证/学生证登记的地方实践。
- 2002 年全国条例明确要求营业网吧核验有效身份证件、保存上网记录，并禁止接纳未成年人。
- 同期现场材料证明规则执行并非完全一致。
- 2003 年部分地区已经出现身份证扫描、实名上网卡等更结构化的身份—会话绑定实现。

### 高概率

- 对依赖共享终端的用户，忘带证件、年龄不符合、场所执行严格等会成为真实接入摩擦。
- “网吧实名 + 平台昵称”在 2000s 可以同时成立，因此简单的“实名/匿名”二元分类不足。
- Web Archive 对成功发帖的可见性远强于对进场失败、柜台核验和短期会话日志的可见性。

### 不知道

- 1998—2001 各城市网吧证件规则的精确扩散时序；
- 不同网吧实际核验率；
- 忘带证件/拒绝登记导致放弃上网的普通用户比例；
- 具体网吧登记系统与特定 QQ/BBS 账号之间是否存在合法公开、可复核的历史绑定证据；
- 大量手写登记或早期上网卡数据是否仍有合规、非敏感的档案性保存。

---

## 下一步

以后若做具体 1999—2005 网吧、BBS 或平台案例，优先找：

1. 某城市原始网吧管理办法与规则版本；
2. 网吧自己的同时代入场说明、价格页、会员/上网卡说明；
3. 用户同期关于忘带证件、办卡、登记、被拒或转去别处的叙述；
4. 学校机房/图书馆与商业网吧之间的渠道切换；
5. 在不重识别个人的前提下，验证“场所层身份”与“平台层身份”到底有没有技术绑定。

如果只能找到法规，不应补写具体用户体验；如果只能找到帖子，不应补写现实入口身份。

---

*本方法包由 AI 辅助整理。重点是建立可复核的身份层级与 archive bias 边界，不重新公开普通个人的历史身份记录。*