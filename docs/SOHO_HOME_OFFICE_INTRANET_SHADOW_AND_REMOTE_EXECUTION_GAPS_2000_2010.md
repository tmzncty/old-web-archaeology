# SOHO、Home Office、内网阴影与远程执行缺口（2000—2010）

> Scope：本文只处理约 2000—2010 年中文旧网中与 SOHO、家庭办公、企业远程协作有关的页面、系统边界和保存偏差。全球 telecommuting 前史与 2020 年后的生活史比较放在 `how-people-lived`，不把本仓扩张成全球远程办公史。

相关生活史研究：

- <https://github.com/tmzncty/how-people-lived/blob/main/topics/workplace-detachment-home-office-and-place-portable-work-china-2000-2024.zh-CN.md>

---

## 1. 为什么远程工作是一个旧网考古问题

2000 年前后的中文门户已经能保存这样的公开叙述：

- 人在家中电脑上写稿；
- 通过 Email 把稿件送到单位；
- 通过网络把内容送到传真机；
- 通过聊天室、在线寻呼、邮件维护客户关系；
- 在家制作网页、插图、程序；
- 通过个人主页和域名展示职业身份。

但真正的劳动状态经常发生在公开 Web 之外：

```text
家中本地文件
→ 拨号 / 宽带接入
→ Email / Webmail / SMTP
→ 附件
→ 单位邮箱 / 内网
→ 电话 / 传真 / IM
→ 人工审核 / 编辑 / 客户反馈
→ 本地文件继续修改
```

因此这一类页面最容易制造一个误解：

> 今天还看得到一篇“SOHO 人如何在家工作”的报道，似乎就等于我们已经保存了当年的远程工作系统。

实际上：

> **public article about remote work ≠ preserved remote-work system state**

本文的主要目标就是把两者拆开。

---

## 2. 证据边界：页面只保存工作流的一小部分

对 2000—2010 的家庭办公，建议至少把 artifact 分成以下层：

| 层 | 典型对象 | 公开 Web 档案可见性 |
|---|---|---|
| public representation | 门户报道、企业新闻、个人主页、招聘/说明页 | 较高 |
| access layer | 拨号账号、宽带、VPN、企业入口 | 部分可见 |
| messaging layer | Email、Webmail、SMTP/POP/IMAP、IM | 很低 |
| transfer layer | 附件、FTP、网络传真、文件服务器 | 很低 |
| enterprise-private layer | OA、内网论坛、项目系统、审批、通讯录 | 极低 |
| local machine layer | Word 文件、PSD、代码、缓存、地址簿 | 几乎不可见 |
| voice / fax layer | 固话、手机、传真机 | Web archive 通常不可见 |
| physical home layer | 房间、桌椅、孩子、噪音、共用设备 | 只能由报道/照片/回忆间接观察 |
| human outcome | 对方是否读到、是否采用、是否付款、是否完成工作 | 极难保存 |

因此对任何“远程执行成功”的 claim，都应继续问：

1. 我们保存的是公开描述还是系统原始记录？
2. 能否证明文件真的被发送？
3. 能否证明接收方真的读到？
4. 能否证明该版本被采用？
5. 能否证明工作关系因此持续？

硬边界：

```text
Email address visible ≠ email sent
email sent ≠ email received
email received ≠ attachment opened
attachment opened ≠ work accepted
work accepted ≠ payment completed
```

---

## 3. 2000 年新浪 SOHO 报道：公开页面如何保存“工作流外壳”

2000 年 9 月 20 日，《北京晚报》经新浪保存的《soho族：在家搭起大平台》提供了一批非常有用的同时代采访：

<https://edu.sina.com.cn/job/2000-09-20/12513.shtml>

报道涉及的工作链包括：

- 家中电脑搜资料、写稿；
- 把文件发到自己的 Email；
- 通过网络向单位传真；
- 自由撰稿人向异地编辑发送稿件；
- 网页/美术工作者在家接项目；
- 使用 Email、聊天室、在线寻呼维持职业联系；
- 个人域名和主页成为职业展示接口。

### 证据等级

**B / A-：同时代媒体报道 + 同期第一人称采访。**

它非常适合证明：

- 当时某些知识工作者确实把部分或全部任务移到家中；
- 工作流已经跨越本地文件、Internet、Email、传真和单位系统；
- 当时人已经主动讨论“住在哪里是否还重要”。

但它不能证明：

- 所有被描述的 Email / 传真传输都已经留下原始记录；
- 当事人的邮箱、附件、聊天记录还存在；
- 这类工作方式在全国劳动者中普遍；
- 当前页面就是 2000 年抓取的原始 HTML capture。

---

## 4. live legacy page ≠ historical capture

这类新浪旧页今天仍可由现役服务器直接返回。

这是一种很容易被误判的证据类型：

### live legacy page：仍在线的历史页面

它可能保留：

- 原文章标题；
- 正文日期；
- 老式栏目结构；
- 一部分旧导航；
- 旧链接文本。

但当前访问发生在今天。

因此必须把：

- `article_internal_datetime`
- `current_fetch_datetime`
- `archive_capture_datetime`

分开记录。

硬边界：

> **historical body served today ≠ verified historical server response**

即使正文从 2000 年保存至今，我们仍不知道：

- 当年页面是否包含完全相同的模板；
- 后续是否改过编码、导航、广告或 footer；
- 图片、脚本、CSS 是否已经替换；
- 当前 URL 是否经过内部迁移后重新发布。

所以：

> **live legacy page is primary-ish content evidence, but not automatically a capture artifact.**

若有 Wayback/CNWeb 历史 capture，应优先建立两者对照。

---

## 5. 2000 年页面里的“网络传真”是跨网络执行，不是纯 Web 功能

报道中“在家写稿后通过网络发送到单位传真机”的路径尤其值得单独建模。

真实拓扑更接近：

```text
home PC
→ Internet service
→ fax gateway
→ telephone/fax network
→ office fax machine
→ paper / recipient
```

Web 或 Internet 只覆盖其中一部分。

这和仓库已有的 pager gateway 研究属于同一大类，但不是同一个对象：

- pager gateway 的 endpoint 是 pager / SMS / human callback；
- 这里 endpoint 是 office fax / document handoff。

建议共用一个原则：

> **archived interface ≠ archived cross-network delivery**

对于网络传真，还应记录：

```yaml
source_device: home_pc
network_entry: internet
service_type: internet_to_fax
final_network: telephone_fax
final_device: fax_machine
human_handoff_required: true
execution_evidence: unknown | partial | confirmed
```

---

## 6. 2003 SARS：公开新闻能看见应急迁移，看不见多数协作状态

2003 年 6 月 9 日新浪科技保存的神州数码报道写到，公司在 SARS 期间启动多层次移动办公系统，一名市场部员工第一次进入 SOHO 状态：

<https://tech.sina.com.cn/it/m/2003-06-09/1846196226.shtml>

报道非常适合证明：

- 家庭办公对一些员工原本不是常态；
- 危机使企业主动迁移工作地点；
- “办公室网络条件好，所以加班也留在公司”与“回家继续工作”之间存在真实基础设施差异。

但从旧网考古角度，真正关键的是：

> **应急远程工作的大部分 operational state 不在公开页面里。**

我们通常看不到：

- VPN / 拨号日志；
- 内网账号；
- OA 审批；
- 文件服务器；
- 项目状态；
- 员工之间的 Email；
- 电话会议记录；
- 居家电脑上的本地工作文件。

因此公共新闻能证明“系统/实践存在”，却不能重放一个员工当天的真实工作 session。

### remote-work execution gap：远程工作执行缺口

定义：

> 公开 Web 可以保存“有人在远程工作”的叙述或入口，但任务的实际状态转换主要发生在不公开、登录后、站外或本地系统中。

---

## 7. 企业内网是旧网档案里的巨大阴影

2010 年阿里巴巴 SOHO 体验日的同期公开报道记载，近千名员工参与家庭办公，并提到企业内部“阿里味儿”等空间中出现许多员工 SOHO 感受、照片和讨论：

<https://www.cbinews.com/desktop/l9DN34>

这里需要特别严格。

今天能访问的是**公开新闻对企业内网活动的描述**，并不是企业内网本身的历史 capture。

因此：

> **press-reported intranet activity ≠ preserved intranet capture**

可以把这种缺口命名为：

### intranet shadow gap：内网阴影缺口

企业 Internet 史越成熟，越可能出现一个悖论：

- 企业越依赖数字化；
- 员工真实工作越进入私有 OA / intranet / messenger；
- 公开 Web 档案反而越难看到日常劳动。

所以一个 2008—2010 高度数字化企业，今天留下的公开网页可能比一个 1998 年个人主页更“漂亮”，但对普通员工实际一天的数字生活反而更不透明。

---

## 8. 2010：家庭基础设施第一次被清楚写成远程办公资格

2010 年报道明确列出参与 SOHO 办公的条件：

- 家中有可宽带上网的电脑；
- 电话、手机能正常使用；
- 能保证正常办公。

这类文字非常值得作为一种 artifact 单独保存：

### remote eligibility artifact：远程资格说明

它可以证明：

- 企业当时认为哪些家庭设备是远程工作的最低输入；
- home broadband / phone / PC 已经不只是消费品，而可以成为劳动资格的一部分。

但不能证明：

- 每个参与者的家庭网络质量相同；
- 所有人拥有独立工作间；
- 家庭成员不会争用设备；
- 远程工作实际产出等于办公室；
- 当天全部内部系统均有历史记录。

推荐 schema：

```yaml
remote_eligibility:
  organization:
  date:
  public_source_url:
  required_device:
    - broadband_pc
    - telephone
    - mobile_phone
  required_home_space: unknown
  required_vpn: unknown
  required_account: implied
  execution_evidence: partial
```

---

## 9. 2008 上海“合租办公室”：媒体描述的论坛帖子不等于帖子已经找回

2008 年 1 月《新闻晨报》经新浪保存的报道写到，多名 SOHO 工作者通过网上“找人合租办公室”的帖子或论坛互相找到，随后实际共同租用办公空间：

<https://news.sina.com.cn/c/2008-01-30/023014856800.shtml>

这和仓库已有 roommate-classified 研究有交叉，但对象不同：

- roommate listing 组装的是共同居住 household；
- co-office listing 组装的是共同工作场所。

这里最重要的 old-web 边界是：

> **media-described forum post ≠ recovered forum post**

公开报道可以证明“受访者说自己通过网络发/看过帖子并由此结识合租者”，但若没有：

- 原论坛名称；
- 原帖 URL；
- 原帖 datetime；
- 回复链；
- archive capture；

就不能把媒体转述升级成 A 级原始论坛证据。

建议状态：

```yaml
listing_recovery_state: described_by_press_not_recovered
```

而不是伪造一个“帖子对象”。

---

## 10. 家庭办公让很多关键 artifact 进入个人电脑，本来就极难归档

SOHO 与传统网站考古一个很大的不同是：

> **工作的核心 artifact 可能从未公开过。**

例如：

- Word / WPS 文稿；
- Photoshop / CorelDRAW 文件；
- 源代码；
- 客户给的附件；
- Email 地址簿；
- ICQ / OICQ / QQ 联系列表；
- 本地聊天记录；
- Outlook Express / Foxmail 邮箱缓存；
- 传真回执；
- 电话本；
- 收款凭证。

这些对象可能只存在于：

- 一块已经报废的硬盘；
- 某个不可访问的邮箱账号；
- 一台公司服务器；
- 一个未公开备份；
- 某个人后来已经清空的本地目录。

因此 old-web 的“缺失地图”若只统计 URL capture，会系统性低估 2000s 数字劳动的消失程度。

建议 M4 以后增加一个非 URL 缺失类型：

```yaml
missing_resource_class: private_operational_artifact
```

---

## 11. Webmail / IM / OA 的登录墙会制造 success-page bias

公开 Web 最容易保存：

- “SOHO 是什么”；
- “某员工今天在家工作”；
- “某公司推出移动办公”；
- “某自由职业者很成功”；
- “某企业的体验活动”；
- 门户编辑挑出的个案。

最难保存：

- 没有完成的稿件；
- 没回的 Email；
- 客户拒绝；
- 延期；
- 居家自律失败；
- 远程绩效下降；
- 工作和育儿同时崩溃的一天；
- 因为设备/网络差根本没能参加 remote 的员工。

因此存在：

### connected-worker survival bias：联网工作者存续偏差

能够被 2000 年门户采访成“SOHO 族”的人，本来就更可能：

- 有电脑；
- 会上网；
- 从事可数字化任务；
- 有能向媒体讲述的职业身份；
- 能维持较稳定的网络联系。

它们是非常好的“这种活法确实存在”证据，却不是普通劳动者的随机样本。

### success-page bias：成功页面偏差

平台/企业更愿意公开：

- 可工作的案例；
- 体验顺利的员工；
- 新技术带来的效率；
- 有趣的家庭照片。

真正失败的 remote state 往往只存在内部工单、聊天或个人记忆里。

---

## 12. SOHO 的“身份页”也不能等同于实际工作状态

2000 年的自由职业者可能拥有：

- 个人主页；
- 独立域名；
- Email；
- QQ/OICQ；
- 论坛账号；
- 企业注册信息。

这些可以构成一个 `occupational identity stack`。

但必须区分：

```text
personal homepage exists ≠ active client work
portfolio item displayed ≠ commissioned work
company domain exists ≠ company operating normally
email listed ≠ email monitored
online status ≠ working
```

因此 old-web 研究一个 SOHO 个人主页时，至少要把：

- self-description；
- portfolio claim；
- contact endpoint；
- external client evidence；
- contemporaneous media mention；

分别记录。

---

## 13. 当前还不能可靠复原什么

### A. 一名普通 SOHO 工作者完整的一天

即使公开报道描述：

> 上午在家写稿，下午通过 Email 交付。

我们仍通常缺：

- 具体拨号/宽带连接；
- 邮件头；
- 附件版本；
- 对方回复时间；
- 电话沟通；
- 实际收入；
- 当天家庭干扰。

所以不能把媒体叙述转成伪造的“完整工作 session”。

### B. 2003 SARS 企业移动办公后台

公开新闻说明系统存在，不等于 VPN / OA / 内网日志还可获得。

### C. 2010 阿里员工内网讨论

目前只拿到公开报道对内部讨论的同期描述；没有公共 archive 证据时，不应把内网帖标题、用户和内容重新构造出来。

### D. 2008 合租办公室原始帖子

媒体报道证明有帖子/论坛发现过程；原始 URL 尚未恢复。

---

## 14. 证据等级表

| 对象 | 当前材料 | 等级 | 可以写 | 不可以写 |
|---|---|---:|---|---|
| 2000 SOHO 生活 | 新浪存续的同期媒体采访 | B / A- | 当时若干知识工作者的家庭办公工作流、工具、未来想象 | 全国普及率、完整系统状态 |
| 2000 上网条件 | CNNIC 同期统计 | A | 拨号/专线/用户规模边界 | SOHO 劳动人数 |
| 2003 企业移动办公 | 新浪科技同期企业报道 | B | 危机期间企业启动 mobile office；员工第一次 SOHO | 完整 OA/VPN session |
| 2008 SOHO 合租办公室 | 同期媒体采访 | B | 网络发现共同办公者、家庭干扰/孤立/自律等原因 | 原帖已被恢复、所有 SOHO 都如此 |
| 2008 SOHO 毕业生 | 同期媒体采访 | B | 正式就业记录与实际劳动可错位 | 全国“隐性就业”规模（需独立统计） |
| 2010 SOHO 体验日 | 同期公开报道 | B | 家庭宽带 PC + 电话/手机被写成参与条件；员工即时反馈 | 企业内网原帖已经保存 |
| 企业内网讨论 | 公开报道的同期转述 | B-to-D boundary | 可以写“报道描述存在这些内部讨论” | 不得写成已获得 A 级内网 capture |

---

## 15. 建议增加的 evidence fields

未来处理家庭办公 / 企业远程协作 artifact 时，建议记录：

```yaml
artifact_kind:
  - public_article
  - personal_homepage
  - corporate_public_page
  - remote_eligibility_rule
  - forum_listing
  - webmail_interface
  - intranet_reference
  - local_file_reference

visibility:
  public: true|false
  login_required: true|false|unknown
  enterprise_private: true|false|unknown

execution_chain:
  discovery_layer:
  messaging_layer:
  transfer_layer:
  enterprise_private_layer:
  final_human_handoff:

survival_state:
  current_live_page: true|false
  historical_capture: true|false|unknown
  original_thread_recovered: true|false|unknown
  operational_state_recovered: true|false

claim_boundary:
  - represented
  - configured
  - attempted
  - delivered
  - completed
  - human_outcome_unknown
```

这能阻止一个常见错误：

> 因为门户报道说“员工通过网络办公”，就把系统状态一口气从 `represented` 写成 `completed`。

---

## 16. 与已有 old-web 研究的关系

这篇文档复用但不重复以下已有框架：

- `DIALUP_ACCESS_CONTEXT_1995_1998.md`：解释早期网络接入背景；
- `CONTACT_STACK_AND_CHANNEL_HANDOFF_1998_2002.md`：解释 Email / pager / phone 等多通道交接；
- `PAGER_GATEWAYS_ONLINE_PAGING_AND_CROSS_NETWORK_DELIVERY_GAPS_1998_2002.md`：共用“接口 ≠ 跨网投递”原则；
- `JOB_BOARD_ADDRESSABILITY_RESUME_DATABASE_GAPS_AND_APPLICATION_ATTENTION_1999_2009.md`：就业发现层；
- `PART_TIME_JOB_POSTS_BBS_MEDIATION_AND_OFFLINE_EXECUTION_2006_2009.md`：线上发现、线下执行的短工；
- `ROOMMATE_CLASSIFIEDS_LISTING_LIFECYCLE_AND_HOUSEHOLD_OUTCOME_GAPS_2003_2011.md`：帖子到现实共同生活之间的 outcome gap。

本篇新增的是：

> **当 Web/Internet 不再只是“发现工作”，而是开始承载工作执行本身时，真正的劳动反而大量进入公开 Web 档案看不到的私有数字层。**

这是与 job-board archaeology 最关键的区别。

---

## 17. 后见之明风险

### 不要把 2000 SOHO 写成“今天数字游民的起点”

2000 年当事人确实已经想象居住地点松动，但其设备、任务、收入与组织环境不同。

### 不要把 2003 SARS 写成 2020 的缩小版

两次危机都触发 home office，但 2003 的网络普及、云服务、视频会议和组织经验完全不同。

### 不要从“在家办公”推断“家庭生活更轻松”

2008 的采访反而直接显示孩子、孤独和自律问题会使人重新租办公室。

### 不要把“公开 Web 缺少证据”写成“当时没有数字工作”

企业内网、Email、IM、本地文件本来就比公开主页更难留下 archive。

---

## 18. 本轮新结论：数字化越深入，普通劳动反而可能越不可见

1990s 个人主页把大量私人表达公开在 URL 上。

而 2000s 后的实际工作越来越进入：

- 私人邮箱；
- 企业内网；
- 登录后的 OA；
- IM；
- 本地硬盘；
- 电话；
- 私有附件。

于是出现一个值得长期追踪的考古悖论：

> **digitalization ≠ archivability**

甚至在某些劳动场景里：

> **more digital work can mean less publicly archivable work.**

对“普通人到底怎样活着”的研究尤其重要，因为正式企业的公开首页可能保存几十年，而一个普通员工真正占据 8 小时的数字劳动却可能完全没有一个公开 URL。

---

## 19. 下一步

高价值对象不再是更多门户 SOHO 新闻，而是尽量恢复至少一条原生执行链：

1. 2000—2004 普通自由职业者个人主页 + 同期客户/作品更新 + 可验证邮件/论坛痕迹；
2. 2003 企业公开移动办公页与可公开合法访问的员工同期论坛/个人日志交叉；
3. 2007—2010 “找人合租办公室”原始 BBS 帖 → 后续实际共租结果；
4. 同一人从 `home office → shared office → fixed office / continued freelance` 的多时点页面；
5. 对一个仍在线的 2000 年门户页面寻找 ≥2 个 Wayback 时点，比较正文、导航、编码、图片和链接，验证 `live legacy page` 与历史 capture 的漂移。

如果原始私有 Email、内网或删除帖子客观不可访问，应按仓库 stop condition 正式记录“无法可靠复原”，而不是用后来回忆或生成内容填空。
