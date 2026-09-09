# Patient record portals, health archives, EHR query/export and cross-institution state gaps · 2002–2015

> Status: research note / evidence contract.
>
> Scope: **中文互联网约 2002–2015 年医疗机构病历、居民电子健康档案、区域卫生信息平台、患者查询页、健康卡 / 就诊卡与 Web 之间的状态关系**。
>
> This is not a history of Chinese medicine, hospital information systems in general, or post-2015 health apps.
>
> Cross-repo life-history note:
> `tmzncty/how-people-lived/topics/from-carrying-medical-record-books-to-portable-clinical-memory-health-records-interoperability-and-care-continuity-china-1976-2026.zh-CN.md`

---

## 0. Why this belongs in old-web-archaeology

旧网仓已经单独研究过：

- 医院预约挂号；
- 就诊卡 / 实名 / SMS / 支付状态；
- 慢病与病友论坛；
- 医疗申诉；
- 校园卡、网银、资格查询等动态事务对象。

但“病历在 Web 上出现”是一类不同的 archaeology problem。

一个 2010 年网页可能只有一个按钮：

> `健康档案查询`

可是这个按钮背后至少可能牵涉：

```text
现实中的人
→ 身份证 / 健康卡 / 就诊卡
→ patient master index
→ 某医院的 MRN
→ 门诊 / 住院电子病历
→ 检验系统 LIS
→ 影像系统 PACS
→ 公共卫生健康档案
→ 区域交换平台
→ Web application
→ session / authorization
→ query result
→ 用户真正看到 / 下载 / 打印
```

因此本篇的第一条硬规则是：

```text
health-record page survives
≠ historical patient database survives
≠ historical record was queryable
≠ historical user was authorized
≠ result page was rendered
≠ record was downloadable
≠ another hospital could consume it
≠ clinician actually used it
```

---

# 1. Scope boundary

## 1.1 In scope

约 2002–2015 中文 Web 中的：

- 居民健康档案查询入口；
- 医院病历 / 报告查询页面；
- 区域卫生信息平台面向居民的 Web surface；
- 健康卡 / 就诊卡作为查询凭证；
- Web 与短信、电话、自助终端的混合接口；
- 门诊病历、电子病历、居民健康档案的术语边界；
- 跨医院记录共享的 Web-visible claims；
- 用户查看、打印、下载、授权、纠错可能对应的状态；
- 历史页面与后端记录之间的 archive gap。

## 1.2 Out of scope

本篇不做：

- 2020s 互联网医院全史；
- 健康码史；
- 医疗建议或疾病诊断；
- 恢复任何私人患者账号；
- 搜索、购买、下载泄露病历；
- 批量保存普通人的真实健康数据；
- 将当前仍可访问的患者门户进行越权测试；
- 把医院 HIS/PACS/LIS 全部写成 old Web 史。

## 1.3 Prehistory boundary

病案管理和医院后台计算机化早于公共 Web。

这部分主要写入 `how-people-lived`；本仓只保留必要边界：

> **Web 没有发明病历，也没有发明医院数据库。Web 改变的是普通患者自己能否远程寻址、查看、打印或维护一部分医疗记录。**

---

# 2. Terminology contract：不要把四个对象都叫“电子病历”

## 2.1 Patient-held outpatient record

纸质门（急）诊病历手册可由患者保管，能够跨机构携带。

它属于物理 artifact，不等于 hospital EMR。

## 2.2 Institutional medical record / case archive

医院保管的病历 / 病案是机构内部记录。

它可以完全没有任何 public-Web surface。

## 2.3 Electronic medical record (EMR)

2010 年卫生部《电子病历基本规范（试行）》与《电子病历系统功能规范（试行）》针对医疗机构在诊疗活动中形成、保存、调用的临床记录。

Sources:

- <https://www.nhc.gov.cn/zwgk/wtwj/201304/a99a0bae95be4a27a8b7d883cd0bc3aa.shtml>
- <https://www.nhc.gov.cn/wjw/gfxwj/201101/a769b5f4b9ca4415a72fa9888bce0bc1.shtml>

## 2.4 Resident health record

2009 年国家基本公共卫生服务与卫生信息化文件中的居民健康档案是纵向居民健康管理对象，并可成为区域卫生信息平台的核心。

Sources:

- <https://www.nhc.gov.cn/wjw/gfxwj/200905/f1b689d73db9464483492c2503ecdc87.shtml>
- <https://www.nhc.gov.cn/guihuaxxs/c100133/200906/e6be952491cd4c5fa70247f5f4520f66.shtml>

因此固定：

```text
patient-held booklet
!= institutional chart
!= EMR
!= resident health record
!= patient portal page
```

它们可以连接，但研究单位必须明确。

---

# 3. Evidence grades used here

沿用仓库 METHOD：

- **A**：同时代政府文件、医院官方页面、可验证 historical capture、原始手册；
- **B**：同期新闻、记者实测、操作教程、患者现场采访；
- **C**：多年后机构史、后来的专题回顾；
- **D**：本篇状态机、系统边界和 archive-gap 推断。

特别规则：

> 搜索结果里看到 `www.xmsmjk.com`，只能证明同期材料把它写作厦门市民健康系统入口；没有真正取得历史 memento，就不能声称知道 2009 页面的 DOM、charset、form action、cookie 或 Web 技术栈。

---

# 4. 2002：病历保管规则本身已经说明“患者可见”与“机构持有”不是同一件事

2002 年卫生部《医疗机构病历管理规定》要求医疗机构建立病历管理制度；同期《中国青年报》报道指出，不少医院当时会把病历交患者带到诊室，也存在由医院保管的门急诊病历档案。

Sources:

- 卫生部，2002：<https://www.nhc.gov.cn/zwgkzt/glgf/201306/d7bd030b5a2b4f8f88967c73d3e5c0ca.shtml>
- 中国青年报，2002-08-30：<https://zqb.cyol.com/content/2002-08/30/content_521231.htm>

这里先建立最基本 custody 状态：

```text
RECORD_CREATED
→ PATIENT_HELD
or
→ INSTITUTION_HELD
```

如果是 `PATIENT_HELD`：

```text
patient possesses booklet
→ carries to clinic
→ clinician reads/writes
→ patient retrieves it
```

如果是 `INSTITUTION_HELD`：

```text
record indexed
→ archive stores
→ request locates record
→ authorized staff retrieves
→ record reaches clinic
```

Web 出现以后，两条链都不会自动消失。

---

# 5. 2007–2008：“一本通”是纸质 interoperability，不应被网络史忽略

2007 北京大学首钢医院的官方材料描述统一门诊病历手册的字段与书写要求；2008 年北京全面推行“一本通”，同期患者直接说以后“不用拿那么多本”。

Sources:

- <https://bynews.bjmu.edu.cn/yyzs/2007yy/110863.htm>
- <https://news.sina.com.cn/c/2008-01-01/131514643863.shtml>

这不是 Web 服务，却是理解 Web health-record portal 的必要前史：

```text
one hospital = one booklet
→ one patient-held booklet can cross hospitals
→ regional database can cross hospitals
```

三者解决的是同一个生活问题：

> **下一家医院怎样获得上一家医院留下的记忆？**

但它们的技术与证据结构完全不同。

---

# 6. 2009 厦门：区域共享第一次留下丰富的 Web-visible evidence

## 6.1 What is strongly supported

2009 年多组同期材料显示，“厦门市民健康信息系统”已经在区域内运行：

- 2008 年试运行时覆盖 36 家医疗机构并建立约 93 万份数字健康档案；
- 医生可通过健康卡调用过去病史；
- 检验报告可在机构之间传输；
- 2009 年系统全面启用；
- 同期报道明确称市民可通过网络、手机查看自己的健康档案。

Sources:

- 光明日报，2009-04-06：<https://www.gmw.cn/01gmrb/2009-04/06/content_905629.htm>
- 海峡导报 / 新浪，2009-03-01：<https://news.sina.cn/sa/2009-03-01/detail-ikkntian1360750.d.html>
- 新华网 / 搜狐，2009-01-16：<https://news.sohu.com/20090116/n261792668.shtml>

Evidence grade：**B contemporaneous**，其中光明日报包含记者现场观察与患者同期发言。

## 6.2 Historical hostname evidence

2010 年卫生部统计信息中心关于“中国卫生信息技术交流大会”的官方通知给出大会官网：

`www.xmsmjk.com/health/`

Source:

- <https://www.nhc.gov.cn/mohwsbwstjxxzx/s8553/201011/23d14466d4264c4db49cb457434c26ca.shtml>

2011 年厦门第三医院同期页面又明确告诉患者：

- 登录“市民健康网” `www.xmsmjk.com`；
- 使用医保卡号或市民健康正式卡号为账号；
- 以保险号为密码；
- 然后进入网络预约界面。

Source:

- <https://www.xmdsyy.com/info/311271.jspx>

这个证据可以支持：

```text
xmsmjk.com existed as a contemporaneously referenced service host
```

但不能支持：

```text
2009 health-record query used exactly the same login fields
```

预约与健康档案查询是否共用同一认证、同一 session、同一应用，在没有原始页面前仍是 unknown。

---

# 7. Xiamen state model：同一张健康卡背后至少有四套状态

## 7.1 Identity state

```text
REAL_PERSON
→ ID / social-security / health-card identity
→ patient master identity
→ local institution MRN(s)
```

硬边界：

```text
one card scans successfully
!= all historical MRNs merged correctly
```

## 7.2 Record-ingest state

```text
ENCOUNTER_OCCURRED
→ clinician writes record
→ source system commits
→ interface exports event
→ regional platform receives
→ patient longitudinal record updates
```

硬边界：

```text
encounter occurred
!= regional record updated
```

## 7.3 Clinician-view state

```text
patient presents identity
→ clinician authenticated
→ clinical relationship established
→ regional lookup succeeds
→ prior record list appears
→ clinician opens item
→ clinician interprets / uses it
```

硬边界：

```text
record discoverable
!= clinician opened it
!= clinician relied on it
```

## 7.4 Patient-Web-view state

```text
user opens portal
→ login page served
→ identifier supplied
→ authentication accepted
→ account mapped to resident
→ authorization checked
→ query executed
→ result rendered
→ user actually sees record
```

这与医院内部医生查看完全不是同一事务。

---

# 8. 2009–2010：国家 health-record platform 与 hospital EMR 同时推进，但不是同一后端

2009 年卫生部先后发布：

- 健康档案基本架构与数据标准；
- 基于健康档案的区域卫生信息平台建设指南；
- 区域卫生信息平台技术解决方案。

Sources:

- <https://www.nhc.gov.cn/wjw/gfxwj/200905/f1b689d73db9464483492c2503ecdc87.shtml>
- <https://www.nhc.gov.cn/guihuaxxs/c100133/200906/e6be952491cd4c5fa70247f5f4520f66.shtml>
- <https://www.nhc.gov.cn/mohwsbwstjxxzx/s8553/200912/45413.shtml>

2010 年又发布电子病历规范。

这一历史重叠特别容易让后来研究者误写成：

```text
2009: EHR nationwide launched
→ hospital EMRs became one national database
```

证据不支持这种叙述。

更准确的模型：

```text
hospital clinical systems
     ↘
regional exchange / health-record platform
     ↗
community public-health systems
```

不同地方的实现程度、字段、身份匹配、实时性和用户入口都可能不同。

---

# 9. 2010 武汉：明确出现“居民自己在 Web 查询完整健康档案”的政策记录

武汉市政府 2011 年总结 2010 年社区卫生信息化时明确称：

- 以居民健康档案为主线；
- 通过网络实现大医院与社区双向转诊与远程诊疗；
- 探索居民在网上通过健康档案信息查询系统，自行查询自己家庭和个人的完整健康档案；
- 截至 2010-10-31，社区卫生服务系统保存电子健康档案 252.47 万份。

Source:

- <https://www.nhc.gov.cn/jws/s6462/201103/7676a2b9199d4d978220fc2cf6c4e18a.shtml>

Evidence grade：**A/B official retrospective-on-previous-year operations**。

这一 source 能证明功能被政府正式描述为已经探索实现，但本轮仍缺：

- original public URL；
- login screenshot；
- DOM；
- charset；
- account-registration process；
- family-member authorization model；
- whether “完整健康档案” meant all source systems or only community-health subset；
- whether historical data were downloadable or only viewable。

因此不能从政策叙述推断具体 UI。

---

# 10. Browser/page archaeology：一个 health-record portal 的 HTML 只是最外层

如果未来取得 2009–2011 历史 capture，至少需要检查：

## 10.1 Public shell

- title；
- host / path；
- charset；
- frameset / table layout；
- login form；
- form action；
- JS；
- captcha；
- IE-only / ActiveX；
- HTTPS / HTTP；
- cookie behavior。

## 10.2 Authenticated surface

- login success redirect；
- patient dashboard；
- record list；
- report detail；
- print / download；
- family-member switch；
- error state；
- timeout / logout。

## 10.3 Backend objects that archive probably does not preserve

- patient master index；
- health-card binding；
- encounter tables；
- LIS / PACS records；
- regional exchange queue；
- role-based permissions；
- audit log；
- clinician authorization；
- patient consent state。

所以：

> **captured HTML is evidence of a surface, not evidence of a historical patient transaction.**

---

# 11. Query / export state machine

把“网上能查病历”拆成：

```text
P0 PORTAL_EXISTS
P1 LOGIN_PAGE_REACHABLE
P2 ACCOUNT_AUTHENTICATED
P3 ACCOUNT_LINKED_TO_PATIENT_IDENTITY
P4 RECORD_INDEX_RETURNED
P5 RECORD_DETAIL_RETURNED
P6 HUMAN_READABLE
P7 PRINTABLE
P8 DOWNLOADABLE
P9 MACHINE_READABLE_EXPORT_AVAILABLE
P10 USER_CAN_CARRY_EXPORT_TO_ANOTHER_PROVIDER
P11 EXTERNAL_PROVIDER_CAN_IMPORT / INTERPRET
P12 CLINICIAN_ACTUALLY_USES_IT
```

必须禁止以下跳跃：

```text
P0 ≠ P4
P4 ≠ P8
P8 ≠ P11
P11 ≠ P12
```

尤其：

**Web viewability ≠ interoperability。**

一张 HTML 表格即使能看，也可能完全无法被另一家医院的系统直接消费。

---

# 12. 2013：病历标识与身份证明开始被正式要求建立检索关联

《医疗机构病历管理规定（2013年版）》明确：已经建立电子病历的医疗机构，应把病历标识号码与患者身份证明编号相关联，使用两者均能检索病历；同时规定门急诊病历原则上由患者保管，医疗机构建立门诊电子病历或病历档案室后，在患者同意情况下也可以由机构保管。

Source:

- <https://www.nhc.gov.cn/zwgk/wtwj/201312/a84f3666d1be49f7a959d7912a978db7.shtml>

这给 old-Web transaction 研究一个特别重要的身份层：

```text
web account identifier
!= national identity number
!= health-card number
!= hospital MRN
!= regional master-patient index
```

它们可能映射到同一个人，但不能默认字段相等。

---

# 13. Same person / different record：identity resolution gap

跨医院共享最难的问题之一，不一定是“网页打不开”，而是系统到底知道两个记录是不是同一个人。

最小模型：

```text
Hospital A MRN 00123
Hospital B card 77890
community health record ID X
national ID Y
web account Z
```

要形成纵向档案，需要 mapping：

```text
00123 ↔ 77890 ↔ X ↔ Y ↔ Z
```

因此：

```text
same name != same person
same ID number != every legacy MRN already merged
same health card != every historical encounter present
```

历史 archive 几乎不可能保存这些后台 mapping。

---

# 14. Same data / different meaning：semantic interoperability gap

即使两个系统真的把数据传过去，也不能直接写“病历已经共享”。

至少还要问：

- 日期是否一致；
- 检验单位与参考范围是否保留；
- 原始影像还是只有报告；
- 诊断是初步、出院还是疑似；
- 药品名称是否标准化；
- 记录版本是否完整；
- 修改 / 追加记录是否同步；
- 医生看到的是摘要还是原始病历。

所以：

> **transport interoperability != semantic continuity。**

这类差异往往不会出现在宣传首页，却会决定数据能不能真的用于诊疗。

---

# 15. Preservation levels for historical health portals

建议以后对旧健康档案 portal 使用 H0–H6：

### H0 — locator only

只有历史 URL、新闻或 Wayback candidate locator。

### H1 — public shell survives

首页 / 登录页有 verified capture。

### H2 — application resources partly survive

CSS / JS / image / form structure 可检查。

### H3 — authenticated workflow documented contemporaneously

没有真实患者 session，但有官方手册 / 同期教程足以确认字段与流程。

### H4 — non-sensitive synthetic / public demo result survives

有不含真实个人健康数据的 demo、training screenshot、test account artifact。

### H5 — transaction semantics can be reconstructed

能确认 identity mapping、query action、result type、print/download capability。

### H6 — backend interoperability evidence exists

能通过官方技术文档、接口标准或系统手册确认跨机构交换对象与状态。

注意：

**H6 不要求、也不应该要求公开真实患者病历。**

医疗 Web archaeology 的高质量证据目标应是架构与状态，而不是隐私内容。

---

# 16. Archive gap：为什么健康档案 portal 比普通静态网页更难保存

## 16.1 Login wall

真实记录通常必须登录，因此 crawler 只能保存 public shell。

## 16.2 Dynamic query

记录列表按 account、身份和时间动态生成；memento 保存首页不保存 query result。

## 16.3 Separate clinical systems

检验、影像、病历常来自不同内网系统，公开 Web 只做 gateway。

## 16.4 Session / cookie dependency

认证后页面需要 session，archive replay 时原 session 已失效。

## 16.5 Image and report subresources

医学影像可能通过独立 PACS viewer、Java / ActiveX / proprietary plugin 返回；报告可能通过 PDF/stream/download endpoint 生成。

## 16.6 Privacy is a feature, not a preservation failure

真实病历没有被公共 crawler 保存，往往正是正常安全边界的结果。

因此必须固定：

> **archive absence of patient data should not be treated as evidence that the historical system lacked patient data.**

---

# 17. Negative evidence from this slice

本轮对 `www.xmsmjk.com` 做了 historical-replay 探索。

已获得的同期 locator / hostname evidence：

- 2010 卫生部官方会议通知：`www.xmsmjk.com/health/`；
- 2011 厦门第三医院：`www.xmsmjk.com` 作为市民健康网 / 预约入口，并描述账号字段。

本轮尝试直接请求类似：

`https://web.archive.org/web/20100101000000/http://www.xmsmjk.com/`

当前访问链因 URL 安全限制未能打开构造的 Wayback replay。

因此当前状态严格记录为：

```text
historical hostname: supported
candidate archive exploration: attempted
verified memento: NOT ACHIEVED IN THIS SLICE
historical DOM/charset/form action: UNKNOWN
historical health-record result page: UNKNOWN
```

不得写：

> `Wayback 没有保存 xmsmjk.com`。

我们只知道本轮没有取得可核验 memento。

---

# 18. Evidence / claim table

| Claim | Grade | Confidence | Limit |
|---|---:|---:|---|
| 2002 已有国家级病历保管规范 | A | high | 不等于各院执行完全一致 |
| 2007–2008 北京推统一纸质门诊“一本通” | A/B | high | 不等于全国采用 |
| 2009 厦门已有区域健康信息共享运行案例 | B | high | 先行城市，不可外推全国 |
| 同期材料称厦门居民可通过网络/手机查健康档案 | B | medium-high | 本轮未复原原始查询 UI |
| 2010 武汉官方总结称居民可在网上查询本人/家庭健康档案 | A/B | high for stated service | 原始 URL 与认证流程 unknown |
| 2010 国家发布电子病历规范 | A | high | 规范发布 ≠ 全国医院全部达到 |
| 2013 规定要求电子病历标识与身份证明关联检索 | A | high | legacy mapping 实施效果未知 |
| Web portal capture 能证明后台历史病历仍存在 | — | **unsupported** | 禁止该推断 |
| archived login page 能证明某患者曾成功查询 | — | **unsupported** | 禁止该推断 |

---

# 19. Counterexamples

## 19.1 电子记录存在，但患者不能拿走

医院内部 EMR 可以非常成熟，却没有 patient-facing download。

所以：

```text
institution digital
!= patient portable
```

## 19.2 患者能在页面上看，但另一家医院不能导入

HTML / PDF 可读不等于 structured exchange。

## 19.3 跨院共享成功，但医生仍需要重检

结果可能太旧、方法不同、病情变化或临床安全需要确认。

因此：

```text
shared != reusable in every clinical decision
```

## 19.4 纸病历并非只有“落后”

患者直接持有纸本，反而有明显 custody：不依赖网站存活、密码、接口和平台账户。

数字 portal 增加了可检索性，也增加了账号与平台依赖。

---

# 20. Privacy contract for this topic

本专题的研究对象是**系统结构**，不是普通人的具体疾病。

禁止：

- 搜索泄露病历；
- 保存真实患者诊断截图；
- 公开身份证 / 健康卡 / 病历号；
- 用 Wayback 或搜索缓存重新暴露已经撤下的敏感医疗资料；
- 用真实患者身份尝试历史登录。

优先证据：

- 政府规范；
- 医院公开手册；
- 同期记者现场流程；
- 系统技术文档；
- 不含个人敏感数据的截图；
- synthetic / training artifacts。

这与仓库 METHOD 的 privacy-minimization 原则一致。

---

# 21. Hindsight risks

## Risk A — 把今天的 EHR 词义倒灌给 2009

必须按同期文本区分健康档案、电子病历、市民健康系统、数字医院。

## Risk B — 把宣传中的“全生命周期”当作数据完整性审计

平台可以宣称“记录一生”；这只能证明当时的目标 / 产品叙述，不能证明每个居民从出生以来数据无缺失。

## Risk C — 把页面按钮当作 transaction evidence

`健康档案查询` 四个字不证明某次查询成功。

## Risk D — 把 regional pilot 当 nationwide norm

厦门、武汉、上海先行案例证明 possibility，不证明 ordinary national availability。

## Risk E — 把“共享”写成“任何医生都能看”

真实系统应存在角色、机构、诊疗关系、授权和审计边界。

---

# 22. What remains unknown / next archaeology targets

1. 取得 2008–2011 `xmsmjk.com` 至少两个 verified mementos；
2. 确认厦门“健康档案查询”与预约是否同一 host / application；
3. 取得武汉 2010 健康档案查询系统的 historical URL；
4. 找一份 2009–2011 patient-facing 操作手册，明确登录字段、家庭成员切换、打印 / 下载；
5. 找同期公开技术文档，明确 regional master-patient-index 的键；
6. 检查是否存在 IE-only、ActiveX、Java/PACS viewer 等 runtime requirement；
7. 找不含真实个人数据的 historical screenshot 或 demo；
8. 区分报告 HTML、PDF、原始影像与结构化交换的不同保存率；
9. 研究系统改版 / 域名迁移时患者如何继续访问旧记录；
10. 研究旧平台关停以后，“病历在后台仍有法定保存义务”和“原患者 Web 账号还能不能访问”是否分离。

---

# 23. Cross-repo interpretation

旧 Web 角度最容易看到的是：

```text
登录框
查询按钮
报告列表
打印按钮
```

生活史真正关心的是：

> **一个带着十年慢病史的人换了城市、换了医院以后，是否还需要从头重新讲一次自己是谁。**

因此本专题给两仓建立一个共同判断：

```text
record exists
≠ record addressable
≠ record visible
≠ record portable
≠ record interoperable
≠ record clinically reused
```

中文旧网把越来越多医疗信息第一次放到普通人的浏览器前面，但这只是长链条中的一层。

真正改变生活的，不是“医院网页上多了一个健康档案栏目”，而是那一层 Web surface 是否真的接到了一个能把人的过去带到下一次就诊的记忆系统。
