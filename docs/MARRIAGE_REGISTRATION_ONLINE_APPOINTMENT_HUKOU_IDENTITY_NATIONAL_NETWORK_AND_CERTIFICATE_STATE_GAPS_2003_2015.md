# MARRIAGE_REGISTRATION_ONLINE_APPOINTMENT_HUKOU_IDENTITY_NATIONAL_NETWORK_AND_CERTIFICATE_STATE_GAPS_2003_2015

> 适用范围：约 2003–2015 年中文旧网中与结婚登记有关的政务信息页、网上预约、电话/Web 混合服务、身份与户口材料核验、地方婚姻登记业务系统、全国婚姻登记信息联网，以及这些事务在网页档案中的保存缺口。
>
> 跨仓生活史主文档：
> <https://github.com/tmzncty/how-people-lived/blob/main/topics/marriage-registration-locality-documents-and-marital-state-executability-china-1994-2026.zh-CN.md>
>
> 本文不写“中国婚姻史”，不重复婚恋网站如何找对象，也不重复离婚求助/婚姻状态文档。这里只回答一个旧网考古问题：
>
> **当一个旧网页写着“结婚登记网上预约”“在线婚姻登记”“婚姻登记信息全国联网”时，它到底证明了现实法定婚姻状态转换链的哪一步？**

---

## 0. 与既有研究的边界

本仓已经有：

- `DATING_PROFILES_SEARCH_FILTERS_OFF_PLATFORM_HANDOFF_AND_RELATIONSHIP_OUTCOME_GAPS_2002_2012.md`：婚恋 profile、搜索、匹配、站外联系与关系结果；
- `DIVORCE_LEGAL_INFORMATION_SUPPORT_GROUP_AND_MARITAL_STATUS_STATE_GAPS_2003_2015.md`：离婚信息、支持网络、平台自填状态与现实离婚状态；
- `APPLICATION_STATE_ELIGIBILITY_AND_ROUTE_PORTFOLIO_2003_2015.md`：一般申请事务的资格/状态模型；
- `ABANDONED_APPLICATIONS_AND_NEGATIVE_STATE_SURVIVAL_2007_2015.md`：放弃申请和负状态的保存偏差；
- `RESIDENCE_REGISTRATION_TEMPORARY_RESIDENCE_PERMIT_EMPLOYER_WEB_DECLARATION_AND_SERVICE_STATE_GAPS_2002_2015.md`：居住登记、单位申报和线上/线下状态。

本文新增研究单位是：

> **relationship intent + legal eligibility + locality jurisdiction + document state + appointment state + bodily co-presence + registrar decision + registry/database state + certificate delivery**

必须全部分开。

---

# 1. 最小事务状态机：不要把“预约成功”写成“已婚”

结婚登记相关网页至少可能处在下列链条中的不同位置：

```text
legal-information page visible
→ appointment service reachable
→ form loaded
→ applicant enters both parties' information
→ desired date / time slot displayed
→ slot selected
→ reservation submitted
→ reservation accepted
→ appointment slip rendered / printed
→ parties prepare required documents
→ both parties physically appear
→ jurisdiction checked
→ ID / hukou / other documents checked
→ self-declaration signed
→ existing marital status checked
→ registrar approves
→ registry record finalized
→ certificate number / document printed
→ certificates handed to both parties
→ record archived
→ record synchronized / shared with other systems
```

核心边界：

> **page visible ≠ service live**

> **slot displayed ≠ slot reserved**

> **reservation accepted ≠ documents eligible**

> **reservation accepted ≠ both parties appeared**

> **online appointment ≠ online marriage registration**

> **both parties appeared ≠ registrar approved**

> **local record created ≠ national database already synchronized**

> **national database connected ≠ nationwide jurisdiction**

> **national lookup returned no record ≠ person certainly never married**

> **certificate printed ≠ certificate necessarily delivered**

这套状态机应成为以后所有婚姻登记历史页面的默认解释框架。

---

# 2. 2003：政务网页保存的是制度版本，不是一次实际登记结果

2003 年 10 月 1 日起实施的新《婚姻登记条例》取消单位或村（居）委会婚姻状况证明，不再强制要求婚前医学检查；内地居民结婚仍要求双方共同到一方常住户口所在地的登记机关，并提交户口簿、身份证和签字声明。

来源：

- 上海市民政局保存的 2003《婚姻登记条例》：
  <https://mzj.sh.gov.cn/MZ_zhuzhan255_0-2-8-15-55-239/20200519/MZ_zhuzhan255_7812.html>
- 中国新闻网，2003-08-20，民政部解释新条例：
  <https://www.chinanews.com.cn/n/2003-08-20/26/337148.html>

### 证据等级

- **A**：法规正文、官方解释。

### 对 old-Web 的意义

今天仍能在现代政府 CMS 上看到一篇“2003 年法规”，只证明：

> **旧文本被现代网站保存/迁移了。**

它不能证明：

- 2003 年原始发布页长什么样；
- 原页使用什么 charset；
- 原始 URL 是否相同；
- 当年是否存在在线办事入口；
- 哪些浏览器能正确显示；
- 原站点是否用了 frames / table / JS；
- 用户是否真的从网页得知规则。

因此必须保留：

> **modern-CMS-preserved-text ≠ historical-page capture**

---

# 3. 2007：北京网上预约的原始事务合同非常明确——它只预订窗口时间

2007 年 5 月，海淀区婚姻登记处试行网上预约。同期新华社材料记载：10 个登记窗口中划出两个服务网上预约者，每日网上预约容量约 40 对。

来源：

- 新华社/CCTV，2007-05-16：
  <https://news.cctv.com/china/20070516/100927.shtml>

同年 6 月 28 日，北京市级和大多数区县推广网上预约。同期操作说明已经足够让我们重建**事务逻辑**，但还不足以重建**网页本身**：

1. 登录“北京市婚姻收养登记服务网”、北京民政信息网或首都之窗；
2. 进入“结婚登记网上预约”；
3. 填写男女双方基本信息；
4. 选择登记日期和时间段；
5. 打印预约单；
6. 在约定日期由双方携带预约单和证件到登记机关；
7. 现场完成登记并领取结婚证。

网上预约需要提前两个工作日，受理日期窗口约为未来一个月；不能到场时需要提前取消。

最关键的同时代原话含义是：民政部门**专门提醒网上预约不等于网上结婚登记**。

来源：

- 新华社/CCTV，2007-06-28：
  <https://news.cctv.com/china/20070628/100874.shtml>

### 证据等级

- **B（很强）**：同期新华社操作性报道，引用主管部门负责人和完整流程。

### 现在能证实什么

- 北京 2007 年确有结婚登记网上预约服务；
- 服务至少要求输入双方基本信息和选择日期/时段；
- 有可打印的预约单；
- 预约和现实登记明确是两个事务；
- 双方仍需身体到场；
- 预约目的是压缩等待和现场录入时间。

### 仍不能证实什么

没有 verified historical replay 前，不得声称：

- 表单字段精确名称；
- POST/GET endpoint；
- 是否使用 AJAX；
- 是否依赖 IE；
- charset；
- session/cookie；
- slot 锁定是提交时还是确认时；
- 并发冲突处理；
- 预约单使用 HTML 打印还是 PDF/ActiveX；
- 失败页面文案；
- 用户个人数据在浏览器/URL 中如何传递。

---

# 4. 历史 locator：`bjhysy.bjmzj.gov.cn` 可以定位，但本轮没有 verified capture

2008 年末北京婚姻登记办事提示明确给出两个地址：

- `www.bjmzj.gov.cn` —— 北京民政信息网；
- `bjhysy.bjmzj.gov.cn` —— 北京市婚姻收养登记服务网。

来源：

- 北京晚报，2008-12-25：
  <https://news.sina.com.cn/c/2008-12-25/134016919427.shtml>

2008 年 8 月 8 日登记高峰的同期报道也将网上预约指向北京市婚姻收养登记服务网。

所以目前可以把：

```text
subject_host = bjhysy.bjmzj.gov.cn
service_family = marriage/adoption registration service
observed_context = 2008
historical_locator_confidence = high
```

写进候选清单。

但本轮通过当前 Web 访问环境尝试 historical archive/CDX 路径时，没有取得可逐页检查的 2007–2010 replay。

这只是：

> **capture not verified in this slice**

绝不能改写成：

> “Wayback 没有保存这个站。”

按照 `docs/METHOD.md`，candidate locator 和 verified capture 必须保持分离。

---

# 5. 2008-08-08：预约系统暴露了 `slot / eligibility` 两套完全不同的状态

2008 年北京为 8 月 8 日特殊登记高峰开放现场与网上预约。

截至 7 月 16 日，已预约 8000 多对，其中现场约 6000 多、网上约 2000 多；多个区县网上名额已满，网上放号量据主管部门称已经达到平时的 5—10 倍。

来源：

- 北京晚报/中新网，2008-07-16：
  <https://www.chinanews.com.cn/sh/news/2008/07-16/1314478.shtml>

同一材料提供了一个极重要的反例：工作人员对网上预约成功者提前检查材料时，接近 50% 存在证件问题，例如身份证过期、集体户口缺首页、户口记录婚姻状况与实际不一致。

这证明至少需要单独记录：

```text
appointment_status: accepted
slot_status: allocated
identity_document_status: valid / expired / unknown
hukou_document_status: compliant / disputed / incomplete
marital-status-record-match: matched / mismatch / unknown
registration_outcome: unknown until physical review
```

因此：

> **slot acquired ≠ legal eligibility resolved**

对未来 archive case，如果只抓到一个“预约成功”页面，最多只能证明预约层状态，不能把现实婚姻状态写成 completed。

---

# 6. 2008—2009：现场、Web、电话和周末窗口长期并存

北京 2008 年末宣布从 2009 年起周六办理婚姻登记。同期提示同时保留：

- 当日现场直接办理；
- `www.bjmzj.gov.cn` / `bjhysy.bjmzj.gov.cn` 网上预约；
- 96156 咨询；
- 114 查询登记处电话。

来源：

- 北京晚报，2008-12-25：
  <https://news.sina.com.cn/c/2008-12-25/134016919427.shtml>

### old-Web 解释边界

这意味着网站上线不能被写成“办事渠道迁到网上”。

更准确的结构是：

```text
walk-in window
+ online appointment
+ telephone information
+ directory inquiry
+ paper identity/hukou documents
```

即 **channel convergence without channel death**。

对 archive 研究，应该记录页面和电话/窗口如何互相转介，而不是只抓网页。

---

# 7. 2010：行政机关可以决定星期日开放，但预约后台可能仍按工作日日历运行

2010 年 10 月 10 日恰逢星期日，又是特殊数字日期。同期报道显示，北京登记机关因为大量咨询决定特别开放；工作人员同时提醒，网上预约系统在星期日日期上可能存在使用问题，建议需要在当天登记的人现场办理。

本轮尚未取得原始预约应用来验证具体故障机制，因此不能进一步断言“系统硬编码工作日”或“数据库无法接受周日”。

现在只能安全记录状态边界：

> **registry office open ≠ appointment backend guaranteed operable**

这类案例很适合以后 browser/replay 实验，因为它说明“页面能渲染”和“业务日历能完成事务”完全不是一回事。

---

# 8. 2012：全国婚姻数据联网，却仍然不能异地任意登记

2012 年 7 月，民政部宣布婚姻登记信息全国联网：

- 建立中央级婚姻登记数据中心；
- 31 个省级区域建立省级婚姻登记工作网络和数据中心；
- 各地实现在线婚姻登记；
- 可以进行婚姻登记信息全国联网审查。

来源：

- 中国政府网 / 民政部，2012-07-24：
  <https://www.gov.cn/gzdt/2012-07/24/content_2190555.htm>

但同一时期民政部仍说要“探索打破在户籍地办理婚姻登记的限制”。地方记者也明确得到答复：**联网不等于已经允许异地登记。**

来源：

- 西安晚报，2012-07-25：
  <https://news.sina.com.cn/o/2012-07-25/054024839028.shtml>
- 华商晨报，2012-07-26：
  <https://news.sina.com.cn/o/2012-07-26/085924848327.shtml>

这必须写成 old-Web 的一个核心状态缺口：

### `backend-networked / public-jurisdiction gap`

```text
registrar can query remote marital-state records
≠ couple can choose any remote registry office
```

这是非常典型的数字化多时钟：

1. 地方业务计算机化；
2. 省级联网；
3. 全国信息联网；
4. 对公众异地办理的管辖权改革；
5. 面向个人的预约/查询；
6. 后续部门数据联动。

绝不能压成一个“2012 年婚姻登记全国联网，所以婚姻登记全国化了”的句子。

---

# 9. 2012：全国数据库本身也有 `legacy-ingest` 状态

北京民政局 2012 年工作总结记载：

- 2010 年涉外、华侨、港澳台婚姻登记与全国联网；
- 2011 年北京婚姻登记系统与全国婚姻登记数据中心对接；
- 从档案部门共享婚姻登记历史档案电子数据 377.8 万条；
- 继续开展婚姻登记历史档案的数据化补录。

来源：

- 北京市民政局，2012-10-11：
  <https://mzj.beijing.gov.cn/art/2012/10/11/art_5550_1192.html>

所以全国联网系统至少还要区分：

```text
local-current-record
legacy-paper-record
legacy-digitized-record
legacy-record-imported
record-matched-to-current-identity
record-available-for-network-review
```

这意味着：

> **network query negative ≠ historical marital state definitively negative**

特别是处理姓名、身份证号码变化、老证件、早期纸档案时，不得把数据库空结果当成完备历史证明。

---

# 10. 2012 的隐私边界：婚姻信息联网不等于公众可搜索的“婚史数据库”

全国联网新闻发布后，社会上很快出现“是否可以查别人的婚姻状况”的疑问。

民政部门公开解释的方向是：婚姻登记信息查询有严格权限，并不是互联网公众查询服务。

因此 future archive work 必须避免一个危险误读：

> **nationally queryable by authorized registrars ≠ publicly searchable on the Web**

本仓不会为了“考古完整”主动寻找、复制或重新公开普通人的婚姻记录、身份证号、户籍地址、历史结婚/离婚信息。

建议归档重点放在：

- 空白表单；
- 公开办事说明；
- 字段 schema；
- 预约事务状态；
- 历史 URL；
- 公开技术文档；
- 匿名化后的错误类型。

而不是普通人的真实婚姻数据。

---

# 11. 2018 afterlife 反例：联网以后，地方文件格式仍可能阻断现实登记

虽然本文主 scope 到 2015，但 2018 的一份政府留言非常适合作为早期系统的 afterlife 反证。

广西网民描述：自己和吉林籍男友携带真实户口簿、身份证和照片办理登记，却因为两省户口簿盖章方式不同被当地窗口拒绝。另一个在北京打工的河北网民也描述了和黑龙江女友遭遇类似问题，并强调两人都在外打拼、请假回家困难。

民政部后续答复确认，只要户口簿首页盖有户口专用章，即使常住人口登记卡没有同样公章，也不影响效力。

来源：

- 湖南省民政厅保存的中国政府网留言与答复：
  <https://mzt.hunan.gov.cn/hdjl/zxts/cjwt/201901/t20190122_5264863.html>

这不是 2003–2015 页面本身，因此不能拿来倒填旧网实现。

它作为 afterlife 能证明的是：

> **database connected ≠ local document interpretation standardized**

以及：

> **document valid ≠ frontline recognizability**

以后研究 2010s 政务事务时，不能只研究“后台有没有联网”，还要保存地方窗口如何解释纸质证件。

---

# 12. 历史 URL / host 候选

本轮能够从同期材料中确认或较强定位的候选：

```yaml
- host: www.bjmzj.gov.cn
  label: 北京民政信息网
  observed_in: 2008
  role: information + marriage-registration appointment entry
  capture_verified_this_slice: false

- host: bjhysy.bjmzj.gov.cn
  label: 北京市婚姻收养登记服务网
  observed_in: 2008
  role: marriage/adoption information + marriage-registration appointment
  capture_verified_this_slice: false

- host: www.beijing.gov.cn
  label: 首都之窗
  observed_in: 2007 reports as appointment entry
  role: portal/entry
  historical_transaction_capture_verified_this_slice: false
```

注意：上述角色来自同期新闻/办事提示，不代表这些 host 在整个 2007–2015 期间始终承担相同功能。

### 必须继续查的谱系问题

- `bjhysy.bjmzj.gov.cn` 何时上线、何时下线或迁移？
- 预约应用是否实际托管在另一个 application host/path？
- `www.bjmzj.gov.cn` 是直接执行预约，还是只链接/iframe 到业务系统？
- 首都之窗入口是 redirect、form proxy 还是说明页？
- 2010/2011 北京业务系统与全国中心对接后，前端 host 是否变化？
- 后续现代北京婚姻预约入口与旧 host 是否有直接技术继承关系？

这些在没有 capture/WARC 前全部保持 `unknown`。

---

# 13. 一个建议的 evidence schema

```yaml
artifact_type: marriage-registration-page
city_or_province:
site_label:
host:
original_url:
capture_url:
capture_datetime:
observed_datetime:
source_grade: A|B|C|D

page_role:
  - legal-info
  - material-checklist
  - appointment-entry
  - appointment-form
  - appointment-result
  - appointment-cancel
  - office-directory
  - status-query
  - help

jurisdiction_rule:
required_documents:
physical_co_presence_required:
appointment_required_or_optional:
appointment_window:
slot_state_observed:
submission_state_observed:
identity_validation_observed:
hukou_validation_observed:
marital_status_network_check_observed:
registrar_decision_observed:
certificate_state_observed:

browser_assumption:
charset:
frames:
js_dependencies:
session_cookie:
print_dependency:
external_resources:
missing_resources:

personal_data_present:
privacy_action:
notes:
confidence:
```

---

# 14. 事务 gap 字典

以后遇到相关页面，至少检查下列 gap：

### 14.1 `information / transaction`

有办事说明 ≠ 有在线事务能力。

### 14.2 `transaction page / live backend`

历史 HTML 可以回放 ≠ 后台日期、时段或验证 API 仍可回放。

### 14.3 `slot shown / slot locked`

页面显示时段 ≠ 并发提交后仍然属于此用户。

### 14.4 `reserved / eligible`

预约成功 ≠ 证件和法律条件合格。

2008 北京接近一半预约者材料问题是直接证据。

### 14.5 `online actor / legal parties`

一个人可以在电脑上为两人填写预约，但结婚登记要求两位法律当事人共同到场。

### 14.6 `identity document / hukou document / marital-state record`

身份证有效、户口簿有效、婚姻数据库状态一致，是三个独立检查。

### 14.7 `national network / national jurisdiction`

2012 是经典反例：后台全国联网，但公众登记仍受户籍地管辖。

### 14.8 `record exists / record synchronized`

地方登记完成 ≠ 全国中心已经同步。

### 14.9 `no network record / legally unmarried`

历史档案补录不完整时不能反推。

### 14.10 `certificate rendered / certificate delivered`

未来若发现打印队列、证书编号或模板页面，仍不能直接证明证书已交付。

### 14.11 `current CMS copy / historical page`

今天政府网站保存 2003/2008 文本 ≠ 当年网页结构仍在。

### 14.12 `appointment traffic / total registration behavior`

特殊日期的预约流量不能代表普通工作日，更不能代表一代人的婚姻意愿。

---

# 15. 浏览器与页面复原问题：当前全部 unknown 的部分

在未取得历史 replay 前，下列内容不能猜：

- 页面编码：GB2312 / GBK / UTF-8？
- table / frameset / DIV+CSS？
- IE-only 条件？
- ActiveX / Java applet / 浏览器证书？
- 客户端 JS 验证哪些字段？
- 日期选择器是 JS 还是服务器渲染？
- 时段余量是页面生成时写入还是异步请求？
- 是否有验证码？
- session 是否绑定 IP / cookie？
- 打印预约单需要什么浏览器设置？
- 网上预约成功页是否含身份证等敏感字段？
- 页面刷新是否可能重复提交？
- 取消预约是否需要 reservation id / 身份证号 / 密码？
- HTTPS 是否存在、证书如何部署？
- 错误页面和超时页面长什么样？

这些问题非常适合未来 Phase 2 / Phase 4 的完整 case + browser environment experiment。

---

# 16. Archive gap：婚姻登记网页特别容易留下“外壳”，丢掉“事务状态”

预约类政务系统对网页档案不友好。

最容易被保存的是：

- 首页；
- 办事说明；
- 新闻公告；
- 预约入口链接；
- 静态材料清单。

最容易缺失的是：

- 登录/session 后页面；
- 实时可选日期；
- 某一时刻的 slot inventory；
- POST 结果；
- 动态校验；
- 打印页；
- 取消预约状态；
- 身份/婚姻状态后台审查；
- 同步队列；
- 失败、放弃与证件不合格状态。

因此 archive surviving set 会天然偏向：

> **制度声称如何运作**

而不是：

> **某个普通人到底在哪一步失败。**

这应和 `ABANDONED_APPLICATIONS_AND_NEGATIVE_STATE_SURVIVAL_2007_2015.md` 交叉使用。

---

# 17. 隐私与伦理边界

婚姻登记数据涉及高度敏感的个人状态。

即使未来 archive、缓存或意外暴露页面能够访问，本仓也不应重新公开普通人的：

- 身份证号；
- 户籍地址；
- 真实出生日期；
- 手机号；
- 婚姻史；
- 预约编号；
- 结婚/离婚双方可关联身份；
- 未公开的登记失败原因。

研究优先级应是：

```text
schema / workflow / empty form / public help / historical URL / anonymized error class
>
ordinary person's identifiable transaction record
```

后者除非有非常强的研究必要性和合法公开依据，否则不应复制到仓库。

---

# 18. 与中国旧网 scope 的边界

本文主对象严格保持在约 2003–2015 中文政务 Web / 数字后台。

2003 以前的单位证明、纸质登记只作为理解 Web 事务的必要前史；2018、2021、2025 只作为 afterlife，用于解释早期系统哪些边界后来暴露或被制度改革改变。

全球比较不在本仓展开。

法国 Minitel 等 pre-Web 民事状态远程事务，应写入 `how-people-lived` 的跨国普通生活比较，而不是把 `old-web-archaeology` 扩展成全球行政信息化史。

---

# 19. M1 状态

## `M1 = NOT ACHIEVED IN THIS SLICE`

本轮取得了：

- 明确历史 host locator；
- 2007 同期预约操作合同；
- 2008 特殊日期事务容量与证件预审反例；
- 2008/2009 Web + 电话 + 现场混合渠道；
- 2012 全国婚姻登记数据联网的官方架构级说明；
- 2012 历史档案电子数据补录证据；
- 2018 afterlife 的跨省证件格式反例。

但**没有**取得并逐页检查满足 `docs/METHOD.md` 合同的 2007–2015 Wayback/WARC historical replay。

当前 Web 访问环境下尝试 archive/CDX 路径没有获得可验证 replay。这只能记录为访问/验证未完成，不能声称 archive 中不存在 capture。

因此以下仍为 `unknown`：

- historical capture datetime；
- 原始 HTTP headers；
- charset；
- DOM / frames / CSS；
- JS；
- browser sniffing；
- session/cookie；
- appointment endpoint；
- slot API / lock semantics；
- 打印实现；
- 历史错误页；
- 全国联网后的前端/后台请求边界；
- legacy record lookup 的具体协议；
- 2007→2015 host/path 迁移谱系。

所以本文件是**研究包 / transaction-state companion**，不是 Phase 2 的完整 historical Web case。

---

# 20. 下一步最值钱的验证

1. 对 `bjhysy.bjmzj.gov.cn` 做 Wayback/ArchiveTeam/Common Crawl locator survey，并记录准确 capture datetime，而不是只靠搜索引擎转述。
2. 找至少两个 2007–2009 时点的预约入口 capture，比较 host/path 与表单变化。
3. 检查 2008-08-08 前后的页面是否保存特殊日历/容量提示。
4. 如能获得表单页，记录 charset、method/action、字段名、JS、打印路径，不提交任何真实个人数据。
5. 对 2010-10-10 星期日问题，寻找原始公告/页面并核验究竟是预约日历限制、运维安排还是报道中的预防性建议。
6. 找 2011 北京系统与全国数据中心对接后的本地软件/培训材料，区分 public Web 与 registrar-only backend。
7. 对 2012 全国中心开展“public Web / registrar intranet / private network”边界调查；不要仅凭“在线婚姻登记”四字推断互联网公众入口。
8. 如果抓到动态页面，优先用 pywb/ReplayWeb.page/oldweb.today，而不是自研回放器。

---

# 21. 这一轮新增的解释

中文旧网里的“网上结婚登记”特别容易被今天的人误读成一种很早的端到端数字政务。

现有同时代证据反而呈现一条更复杂的路线：

```text
现实窗口排队
→ Web 预订未来窗口时间
→ 现场纸证件核验
→ 地方计算机登记
→ 地方历史档案数字化
→ 全国后台联网审查
→ （多年以后）登记管辖权才逐步脱离户籍地
```

所以这次新增的真正历史解释是：

> **中国婚姻登记的“网络化”先发生在时间预约和后台记录之间，而不是先发生在两位普通人可以远程完成婚姻这件事上。**

页面可以先让人少排几个小时，数据库可以先跨过省界，而两个人的身体仍然必须回到法律指定的地方。

这正是 old-Web 应保存的东西：不是“某网站当年很先进”的怀旧印象，而是网页、数据库、纸证件、窗口和人的身体在同一事务里究竟各负责哪一步。

---

## 主要来源

### A：官方 / 原始规范和机构材料

- 2003《婚姻登记条例》：
  <https://mzj.sh.gov.cn/MZ_zhuzhan255_0-2-8-15-55-239/20200519/MZ_zhuzhan255_7812.html>
- 2012 民政部婚姻登记信息全国联网发布会：
  <https://www.gov.cn/gzdt/2012-07/24/content_2190555.htm>
- 2012 北京市民政局婚姻登记信息化总结：
  <https://mzj.beijing.gov.cn/art/2012/10/11/art_5550_1192.html>
- 2018 网民留言与民政部答复（官方保存）：
  <https://mzt.hunan.gov.cn/hdjl/zxts/cjwt/201901/t20190122_5264863.html>

### B：同期操作性新闻

- 2007 海淀网上预约试点：
  <https://news.cctv.com/china/20070516/100927.shtml>
- 2007 北京推广网上预约：
  <https://news.cctv.com/china/20070628/100874.shtml>
- 2008 8月8日预约容量与证件预审：
  <https://www.chinanews.com.cn/sh/news/2008/07-16/1314478.shtml>
- 2008/2009 北京周六服务、网站与热线：
  <https://news.sina.com.cn/c/2008-12-25/134016919427.shtml>
- 2012 “联网但异地登记仍需等待”：
  <https://news.sina.com.cn/o/2012-07-25/054024839028.shtml>

---

> Initial research and synthesis were AI-assisted. This note deliberately separates historical locator evidence from verified captures, and it does not reproduce identifiable private marriage-registration data.