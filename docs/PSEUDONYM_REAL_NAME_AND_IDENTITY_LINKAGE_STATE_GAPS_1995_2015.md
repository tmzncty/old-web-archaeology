# Pseudonym / Real-name / Identity-linkage State Gaps, 1995–2015

> 中文旧网里的“网名”“实名”“账号”不是一个字段。本文只研究约 1995–2015 中文互联网中，现实主体、登录凭据、账号 ID、公开昵称和离线身份之间的映射；不扩成全球匿名文化史，也不重新识别普通历史用户。

Companion life-history note:

- `tmzncty/how-people-lived/topics/from-pseudonyms-to-identity-portfolios-online-offline-identity-compartmentalization-china-1980-2026.zh-CN.md`

---

## 1. 为什么这是一个独立的 old-Web 状态问题

本仓已经有：

- `PERSONAL_HOMEPAGE_PUBLIC_SELF_METRICS_AND_PLATFORM_MORTALITY_1996_2015.md`：公开个人页面；
- `ACCOUNT_PORTABILITY_AND_LOCAL_RESIDUE_1999_2003.md`：账号迁移与残留；
- `LEGAL_NAME_RARE_CHARACTER_ID_NUMBER_AND_WEB_FORM_IDENTITY_CONTINUITY_GAPS_1999_2015.md`：法定姓名和证件字符串连续性；
- `ALUMNI_*`：班级身份、成员审核与旧关系重联；
- `DATING_*`：约会 profile 与现实关系 outcome。

本文件只解决一个跨平台的低层问题：

> **一份历史页面里看到的昵称、登录名、账号 ID、实名字段和现实人物之间，究竟能证明什么映射，不能证明什么映射？**

这也是 `ROADMAP.md` M2 已经提出但尚未单独建模的维度：身份到底是匿名昵称、站长身份、实名还是半实名账号。

---

## 2. 不要把“一个账号”想成一个字段

建议把历史身份栈至少拆成：

```text
[real-world person]
        ↓ ?
[legal / credential identity]
        ↓ submitted / verified / unknown
[platform account / numeric ID]
        ↓
[login name]
        ↓
[public nickname / screen name / avatar / bio]
        ↓
[board / group / blog / profile role]
        ↓
[post / comment / message / event]
        ↓
[index / search / cache / quote / archive]
        ↓
[possible cross-platform or offline linkage]
```

其中任意一条箭头都可能：

- 不存在；
- 只在平台私有后台存在；
- 只在特定年份存在；
- 对新账号强制、对老账号 grandfathered；
- 由用户自报而未核验；
- 经手机号/证件/单位/学校等凭据核验；
- 在前台完全不可见。

---

## 3. 必须固定的最小 state gaps

```text
pseudonym ≠ anonymity
```

一个公开昵称可以长期稳定、可搜索、可被熟人识别，甚至后台绑定身份证或手机号，因此“不是法定姓名”不等于“没人知道是谁”。

```text
real-name registration ≠ public real-name display
```

平台要求后台真实身份，不等于前台昵称必须显示身份证姓名。

```text
registration field exists ≠ server verified value
```

历史注册页里存在“真实姓名/身份证”字段，只能证明前台 form 要求过这个字段；不能自动证明后端曾调用权威数据库、人工检查或拒绝假值。

```text
required in help page ≠ historically enforced for every account
```

规则可能只适用于某批新注册、某些角色、某些地区或某次整治阶段。

```text
account ID ≠ login name ≠ display nickname
```

迁移、改名、昵称修改和站内 numeric ID 都会破坏一一对应想象。

```text
same nickname ≠ same human
```

同名昵称可以重复、跨站抢注、被转让或被不同人独立使用。

```text
different nicknames ≠ different humans
```

同一人完全可能维护多个论坛马甲、博客、QQ、校友录或 SNS 账号。

```text
publicly exposed legal identity ≠ research permission to re-identify
```

历史上曾经被媒体、人肉搜索或泄露连接过的普通人，不因此成为今天可以重新拼接私人资料的研究对象。

---

# 4. 1995—2004：公开网名存在，并不能回答后台到底掌握什么

这一时期大量个人主页、BBS、论坛、聊天室和早期博客都把 nickname / handle 作为前台主要身份表面。但仅凭幸存页面通常只能看到：

- 发帖昵称；
- 头像；
- 注册时间；
- 等级/积分；
- 公开个人资料；
- email/QQ 等用户自愿填写字段。

最难保存的却是：

- 当年注册 form 的完整字段；
- 真实姓名字段是否必填；
- 是否验证；
- 管理员能看到什么；
- 是否有 IP/电话/证件内部映射；
- 旧账号后来是否被迁移到新的实名要求下。

因此，本阶段看到“满屏网名”最多证明：

> **public-facing identity was pseudonymous-looking.**

不能直接证明：

> **platform possessed no real-world identifying data.**

本轮没有找到足够高质量、可代表 1995—2004 中文平台总体的后台身份采集比例；保持 unknown。

---

# 5. 2005：角色级 credentialing 不能被写成全民实名

2005 年《南方日报》同期报道，深圳在相关互联网治理行动中要求论坛/BBS 版主、聊天室管理者和部分 QQ 群创建者进行真实身份登记。

来源：

- <https://news.sina.com.cn/o/2005-07-26/09026530230s.shtml>

证据等级：**B，同时代媒体。**

能证明：

```text
some managerial roles
→ extra real-identity registration requirement
```

不能证明：

```text
all readers / posters / QQ users
→ mandatory public legal-name display
```

这提示旧网考古必须保存 **role scope**：普通用户、版主、群创建者、企业认证账号可能处在完全不同的 identity state。

---

# 6. 2006：博客实名争论证明“政策想象”存在，但不能当作执行事实

2006 年同期媒体报道，中国互联网协会正在研究博客实名制度，平台和媒体围绕实名、匿名、责任和隐私展开公开争论。

来源：

- <https://news.sina.com.cn/c/2006-10-20/145310285373s.shtml>

证据等级：**B，同时代媒体。**

这类材料可以证明：

- 某种制度正在被讨论；
- 当时参与者如何理解匿名/实名；
- 部分平台公开表态。

它不能自动证明：

- 注册页面已经改变；
- 后端已经部署身份核验；
- 旧账号被强制补录；
- 实际用户因此公开使用法定姓名。

需要固定：

```text
policy proposal ≠ product deployment ≠ enforcement ≠ user completion
```

---

# 7. 2008：公开昵称可能被历史媒体连接到现实人物，但 archive 不应重复做这种连接

《中国青年报》2008 年关于“Die豹”事件的同期报道记录，一名大学生的网络昵称在争议和人肉搜索中被连接到现实学校与个人生活，并造成严重线下后果。

来源：

- <https://zqb.cyol.com/content/2008-06/18/content_2227616.htm>

证据等级：**B，同时代调查报道。**

这能证明一个重要状态：

```text
stable public handle
→ cross-source linkage
→ offline identification
→ real-world consequence
```

但本仓的研究动作必须停在这里。不要：

- 用旧昵称继续搜索她今天的账号；
- 拼接学校、家庭、住址、手机号；
- 把当年的 doxxing 结果再整理成一个现代身份 dossier。

### 方法结论

**identity-linkage evidence 与 identity-linkage reproduction 是两回事。**

研究者可以证明“这类穿透曾发生”，不需要再次执行穿透。

---

# 8. 2009：法规、网站声明和真实执行仍需要分开

2009 年杭州关于互联网实名管理的同期报道可以看到明显的 implementation gap：公开规则、地方要求与具体网站是否已经落实之间并不总是一致。

候选来源：

- <https://news.sina.com.cn/c/2009-05-05/082517747986.shtml>
- <https://news.sina.com.cn/c/2009-05-06/092717755354.shtml>

证据等级：**B，同时代媒体。**

本轮没有为这些站点取得可复核的历史注册 transaction，因此只把它们用于提醒：

```text
law / regulation exists
≠
site UI changed that day
≠
backend verification active
≠
all users complied
```

---

# 9. 2011：官方材料明确给出“后台实名 / 前台自愿”的双层状态

北京市政府 2011 年关于微博用户管理的政策问答说明：

- 注册并发布信息的用户要向网站提交真实身份信息；
- 浏览行为不受同样注册条件限制；
- 对外使用的服务名称仍可由用户自主选择。

来源：

- 北京市政府，2011-12-17：<https://www.beijing.gov.cn/zhengce/zcjd/201905/t20190523_77079.html>

证据等级：**A，同时代官方解释。**

这给出了一个可复用的历史状态模型：

```text
[real identity submitted / checked at backend]
                  ↓
         [platform account]
                  ↓
       [public user-chosen name]
```

本文称为：

**credential-bound pseudonymity — 凭据绑定化名性。**

所以 old-Web capture 上看到一个网名，不能据此判断后台是否实名；反过来看到“实名注册”的公告，也不能据此把历史前台截图中的昵称当成假身份或违规状态。

---

# 10. 2015：账号名称规范继续证明“账号主体”和“公开名称”要分层记录

国家互联网信息办公室 2015 年发布《互联网用户账号名称管理规定》，要求服务提供者落实真实身份信息认证，同时规范账号名称、头像和简介等前台信息。

来源：

- <https://www.cac.gov.cn/2015-02/04/c_1114246561.htm>

证据等级：**A，官方原始文件。**

对于历史数据库/schema 设计，这至少需要分开：

```yaml
account_internal_id: unknown
login_identifier: unknown
credential_real_identity_required: yes/no/unknown
credential_verification_method: unknown
public_display_name: observed string
public_real_name_required: yes/no/role-scoped/unknown
observed_at: datetime
```

不要再用一个 `username` 字段承载全部含义。

---

# 11. 一个值得继续追的混合设计：实名可验证，但不把法定姓名直接公开

2010 年宁波出现过“东方诚信网络”一类同期报道对象：公开描述的思路包括把手机号与网络昵称绑定，并通过中介号码转接联系，希望在可追责与不直接公开现实信息之间形成折中。

候选来源：

- 同期媒体索引/报道（本轮只作为 locator；需后续复核原页面与产品文档）。

本轮没有取得满足本仓门槛的原站 capture，因此不进一步确定：

- 注册字段；
- 手机核验方法；
- 转接系统；
- nickname uniqueness；
- 实际用户规模；
- 服务持续时间。

这条候选只保留为下一轮 artifact target，不提升到已证实技术实现。

---

# 12. 公开页面与私人凭据天然存在保存不对称

本文把它称为：

**public-handle / private-credential asymmetry — 公开昵称 / 私人凭据保存不对称。**

Archive 很容易留下：

- nickname；
- avatar；
- public profile；
- post；
- comment；
- page title；
- 公开“认证”图标；
- 帮助页里的实名说明。

Archive 很难、也通常不应该留下：

- 身份证号码；
- 完整手机号；
- 后台审核记录；
- 账号与实名映射表；
- credential verification API response；
- 内部风控标记；
- password/session；
- 管理员查看页。

因此历史研究存在一个非常强的视觉错觉：

> **前台留下满屏网名，看起来像一个完全匿名的互联网；后台身份层恰好是最难被公共档案保存的部分。**

反过来也成立：一篇今天仍可读的实名政策公告，可能保存得比当时真正运行的注册/验证接口完整得多。

---

# 13. 历史 capture 应怎样编目身份字段

如果未来取得一个 BBS/博客/SNS 注册或 profile capture，建议至少记录：

## 13.1 Registration shell

- original URL；
- capture URL；
- capture datetime；
- HTTP status；
- charset；
- browser assumption；
- 是否要求 JS/ActiveX/plugin；
- 表单 method/action；
- 可观察字段 label；
- 哪些字段标 required。

## 13.2 Credential layer

只记录 schema 和规则，不记录普通人的敏感值：

- real name field exists?；
- ID-card field exists?；
- phone field exists?；
- email verification?；
- school/work affiliation?；
- verification claimed by help page?；
- verification response actually observed?；
- old-account migration rule?。

## 13.3 Public identity layer

- login name 是否公开；
- nickname 是否可修改；
- public numeric ID；
- avatar/bio；
- 是否显示“认证/实名”标识；
- 是否允许不同 board / group / blog 使用不同 display identity。

## 13.4 Linkage evidence

只记录：

- 平台自己是否提供 cross-profile links；
- 同一 numeric ID 改昵称后是否仍可追踪；
- 公共页面是否显示曾用名；
- 新闻/官方材料是否明确记录某类 linkage mechanism。

**不要把普通账号跨站 re-identification 变成研究任务。**

---

# 14. Browser / encoding / migration 也会制造“身份变化”假象

昵称字段尤其容易被旧网页环境破坏：

- GB2312 / GBK / Big5 / UTF-8 解码不同；
- HTML entity / replacement character；
- 字体缺字；
- archive rewrite；
- profile migration；
- URL 中 username 编码变化；
- 昵称允许改名但缓存标题没更新；
- 平台换 numeric ID / slug。

所以：

```text
rendered nickname changed
≠
person changed
```

也不能反过来：

```text
rendered nickname identical
≠
same account/person proven
```

需要 account ID、URL、时间和平台规则共同判断。

---

# 15. 与 life-history 研究的交叉意义

旧网身份结构会直接改变普通生活：

- 一个学生能否在论坛里讨论兴趣而不立即被学校角色吞没；
- 一个职员能否保留不面向客户/同事的公开表达面；
- 一个创作者是否为了可发现性主动把网名和现实身份连接；
- 一个争议网名被 doxxing 后是否产生学校/工作后果；
- 一个家庭成员是否因为进入同一 SNS 而触发 context collapse；
- 用户是否需要开小号、换平台或清理旧内容来重新建立边界。

这里不做 2015 以后的平台史；后续身份分舱、朋友圈分组、三天可见、2023—2026 选择性前台实名与新身份认证架构，放在 companion `how-people-lived` note 里。

---

# 16. 反例与后见之明风险

1. **不要写“早期网络天然匿名”。** 海外 WELL 等早期社区就是明显反例；中文平台也可能在后台保存现实线索。
2. **不要写“实名制后网名消失”。** 2011 官方材料已经明确区分后台真实身份与前台自选名称。
3. **不要写“昵称就是假身份”。** 昵称可能是长期稳定、所有现实熟人都知道的公开身份。
4. **不要写“实名一定降低所有风险”。** 这超出本仓证据，也忽略身份泄露和跨语境联结风险。
5. **不要从政策日期直接推站点部署日期。** 必须找具体页面/capture/帮助文档。
6. **不要从一个注册 form 推后端验证。** server-side state 需要另外证据。
7. **不要从新闻中的一次 doxxing 重演 doxxing。** 研究 linkage mechanism，而不是建立个人 dossier。
8. **不要从今天的账号状态回填 2008。** 昵称、实名、认证标识和 numeric ID 都可能经过迁移。

---

# 17. 本轮 M1 / archive 负结果

本轮获得了多组具体 historical locator 与同时代制度材料，包括：

- 2005 深圳关于特定管理角色真实身份登记的报道；
- 2006 博客实名讨论；
- 2008 网络昵称被连接至线下身份的同期案例；
- 2009 杭州规则/执行争议；
- 2011 北京“后台实名、前台自愿”的官方解释；
- 2015 全国账号名称规定。

但本轮 **没有取得并实际检查一份满足 M1 门槛的 2005—2011 中文 BBS/博客/SNS 注册流程 Wayback/WARC transaction capture**。

因此以下内容继续保持 `unknown`：

- 某一目标站当年完整注册 DOM；
- 原 HTTP charset；
- form action / method；
- ID-card/real-name 字段是否真正送达服务器；
- 服务端是否核验、怎样核验；
- cookie/session；
- 旧账号迁移与 grandfathering；
- nickname change history；
- 实名状态是否在前台暴露；
- 注册成功/失败的真实 response。

这不是“当时不存在”的证据，只是：**本轮没有得到可复核 transaction artifact。**

---

# 18. 下一步最值得做的 artifact target

优先级不是继续堆实名政策新闻，而是找一个真正能看见字段分层的历史对象：

1. 2005—2010 某中文 BBS / 博客注册帮助页 + registration capture；
2. 同平台至少两个历史时点，观察 nickname / real-name / phone / email 字段变化；
3. 如果可得，再找同期用户教程或站长文档作为第二 evidence family；
4. 只记录 schema，不提交真实普通用户的身份证、手机号或账号实名映射。

如果只能找到公开 profile、找不到 registration/backend，就明确停在：

```text
public nickname observed
backend credential state unknown
```

---

## 结论

中文旧网身份史不能写成：

```text
匿名网名
→
实名制
```

更适合的考古模型是：

```text
real person
↕（可能未知）
credential identity
↕（提交 / 核验 / 未知）
platform account
↕
login identifier
↕
public nickname
↕
content + search + archive
↕
possible offline linkage
```

旧网最容易保存最后几层，最难保存中间的私有 credential state。正因为如此，**“页面看起来匿名”与“系统实际上完全不知道你是谁”之间存在一个结构性的 archive gap。**
