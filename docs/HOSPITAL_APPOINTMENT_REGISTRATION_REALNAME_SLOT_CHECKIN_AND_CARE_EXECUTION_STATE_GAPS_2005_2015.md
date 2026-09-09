# Hospital appointment, registration, real-name, slot, check-in and care-execution state gaps, 2005–2015

> Scope: 中文旧网约 2005–2015。研究医院官网、预约挂号页、统一预约平台、第三方预约入口及其与电话/窗口/短信/医院内部排程系统之间的状态边界。
>
> 不做全球医疗信息化通史，不把 1990s 海外/中国后台排程史无限写进本仓。更长的普通生活史、1960s–1990s 海外计算排程前史、2020s 互联网医院与陪诊变化，写入 `tmzncty/how-people-lived` 的配套专题。

核心问题不是“历史网页上有没有一个预约按钮”，而是：

> **某一历史时点，一个普通患者能否从那个页面真正取得一个属于自己的未来就诊时段？**

医疗预约尤其容易被旧网页误导，因为它横跨：

`公开页面 → 动态号源 → 用户身份 → 医院内部排程 → 短信/电话 → 到院报到 → 医生实际接诊`

archive 通常只保存最外面的一两层。

---

## 0. 本轮结论摘要

本轮可以确认的历史基线：

1. **2009-09-01**，北京三级医院推动预约挂号时，医院预约方式仍高度异构；北京朝阳医院同期已经提供电话、网络、窗口、复诊和社区预约。其网络预约入口位于医院官网 `http://www.bjcyh.com.cn/` 内。同期北京市卫生局材料称该院已有约十三年电话预约经验。
2. **2009-09-30**，卫生部正式发布《关于在公立医院施行预约诊疗服务工作的意见》，明确要求实名预约、更新医务人员出诊信息、逐步提高预约比例。
3. **2009-11** 北京同期统计显示，在预约挂号渠道内部，窗口、电话、网络和其他渠道长期并存，网络预约不是唯一甚至不是主要渠道。
4. **2011-07-28**，北京市统一预约挂号平台上线，公开历史 hostname 为 `www.bjguahao.gov.cn`，与 114 电话平台共享面向公众的统一入口；同期说明存在注册、医院/科室/医生选择、患者资料、短信验证、识别码、取消与现场执行等状态。
5. 2011 平台运行初期已经出现电话等待队列、专家号长时间无余量、实名预约次数限制、爽约规则等状态；“互联网减少物理排队”不能写成“排队消失”。
6. 2009 同期媒体已经记录搜索引擎结果中的假/不规范“网上挂号”入口会要求患者提交姓名、身份证、电话、地址等资料，因此**页面 provenance 本身就是医疗预约可执行性的一部分**。
7. 2014 左右，`guahao.com` 等第三方/合作平台进一步把预约、智能分诊、医生资料和移动端连接起来；但第三方前端显示的医生/号源状态不能直接等同医院 authoritative scheduling state。
8. 本轮没有取得能够逐项核验 DOM、charset、form action、XHR/API、历史 slot payload 和 transaction commit 的合格 Wayback memento。因此 historical replay 仍停在候选层，不能写“已经复原 2011 挂号流程”。

---

## 1. 研究单位：不要把“医院网站”当成一个状态

医疗预约至少包含以下不同对象。

### 1.1 institution

医院或卫生行政机构，例如：

- 北京朝阳医院；
- 北京市卫生局；
- 接入统一平台的某家三级医院。

### 1.2 host / platform

例如：

- `www.bjcyh.com.cn`；
- `www.bjguahao.gov.cn`；
- `guahao.com`；
- 电信 114 呼叫中心。

同一医院可以同时接入多个 host / channel；同一 host 也可能在不同年份更换后台。

### 1.3 public page

可能只是：

- 医院首页；
- 医生介绍；
- 科室页；
- “预约挂号”帮助页；
- 登录/注册壳；
- 日期/医生选择页；
- 预约确认页。

### 1.4 appointment backend

真正管理：

- 医生出诊计划；
- 可预约号源；
- channel quota；
- seat/slot lock；
- cancellation；
- no-show；
- patient identity；
- hospital HIS/PAS mapping。

这个层通常最难被公开 archive 保存。

### 1.5 patient account / identity

包括：

- Web account；
- 姓名；
- 身份证件；
- 手机号；
- 儿童监护人信息；
- 就诊卡/医联码等历史本地标识。

这些不应因为 archive 技术上可能存在就被重新公开。

### 1.6 transaction

一次预约请求不是一个页面，而是一串状态改变。

### 1.7 offline care execution

最终还要经过：

- 到院；
- 取号/报到；
- 核验；
- 候诊；
- 医生接诊。

旧 Web 只能覆盖这条链的前半段，不能从前端成功页推断后半段。

---

## 2. 最小状态机

### 2.1 discovery state

```text
hospital exists
→ official site identified
→ official/authorized booking channel identified
→ department/doctor information found
```

硬边界：

`search result looks official != channel is official`

2009 北京同期调查已经证明搜索“医院 + 网上挂号”可能进入要求真实个人信息的非官方/不规范入口。

### 2.2 schedule-publication state

```text
doctor exists
→ doctor scheduled to practice
→ schedule published to booking system
→ quota assigned to channel
→ slot exposed to current user
```

硬边界：

`doctor profile captured != doctor scheduled that day`

`doctor schedule page captured != bookable inventory existed`

`hospital had inventory != Web channel had inventory`

### 2.3 booking-request state

```text
user registered/logged in
→ patient identity selected/created
→ hospital selected
→ department selected
→ doctor/date selected
→ candidate slot selected
→ patient info submitted
→ SMS/phone verification passed (where required)
→ booking request accepted
```

硬边界：

`form submit != transaction accepted`

### 2.4 reservation-commit state

```text
request accepted
→ authoritative slot lock/commit
→ reservation ID / recognition code created
→ confirmation shown/sent
```

硬边界：

`confirmation-looking page != authoritative hospital ledger committed`

如果平台、医院 HIS、短信网关和电话系统不同步，前端结果不能单独证明最终 reservation state。

### 2.5 cancellation/no-show state

```text
reservation exists
→ patient requests cancellation
→ cancellation accepted
→ slot released/recycled
```

或：

```text
reservation exists
→ appointment time passes
→ no valid check-in
→ no-show recorded
→ possible future booking restriction
```

硬边界：

`cancel button clicked != slot released`

`patient absent != intentionally wasted slot`

旧网页通常保存规则，却几乎不保存患者为什么没来。

### 2.6 check-in / care state

```text
reservation exists
→ patient arrives
→ identity matches
→ check-in/取号 completed
→ patient enters queue
→ doctor actually sees patient
```

硬边界：

`预约成功 != 到院`

`到院 != 报到成功`

`报到成功 != 医生实际接诊`

`医生接诊 != 完成诊断/治疗`

---

## 3. 2009：医院各自为政时期的 Web artifact

### 3.1 北京朝阳医院：电话、Web、窗口、复诊、社区并行

2009-09-07 北京卫生局同期材料说明，北京朝阳医院 9 月 1 日正式开通网上预约挂号，患者可登录医院主页 `http://www.bjcyh.com.cn/`，点击“预约挂号”按提示操作。

同一材料列出：

- 电话预约；
- 网络预约；
- 窗口预约；
- 复诊预约；
- 社区预约。

来源：
- https://news.sina.com.cn/c/2009-09-07/112616254859s.shtml

证据等级：**A/B**（北京市卫生局同期信息，经新浪保存）。

这里最重要的 old-Web 结论不是“2009 有网页”，而是：

> **一个医院品牌同时存在多种预约通道；Web page 只是同一 appointment inventory 的一个入口。**

因此历史复原必须问：

- 电话和 Web 是否共享号源？
- Web 分到多少 quota？
- 页面上的医生列表来自医院 HIS 还是静态维护？
- 预约提交后是实时 commit 还是人工二次确认？

本轮尚不能回答。

### 3.2 2009 预约渠道统计：Web exists != dominant

北京 2009 年 9–10 月预约就诊渠道同期统计：

- 窗口预约 46.44%；
- 电话预约 23.64%；
- 网络预约 3.27%；
- 其他方式 26.65%。

来源：
- https://news.ifeng.com/society/1/200911/1104_343_1420260.shtml

证据等级：**B**。

所以研究一张 2009 网上预约页面时禁止写：

> “患者已经从窗口转向网上挂号。”

最多可以写：

> “Web booking channel 已存在；同期北京预约结构仍然以非 Web 渠道为主。”

### 3.3 2009 fake/unauthorized booking：search-engine provenance gap

同一同期调查中，记者通过搜索引擎输入医院相关关键词，进入一个显示医生姓名、职称、科室和出诊时间，并提供“网上挂号”按钮的页面；表单进一步要求姓名、身份证号码、电话、地址等真实信息。报道将其作为“李鬼”/非正规网络预约问题调查。

这产生一个本仓此前其他事务也可复用的 gap：

### `search-engine provenance gap`

```text
search engine result
≠ official hospital page
≠ authorized booking provider
≠ safe destination for identity data
```

对历史页面来说，“页面长得像医院”毫无证明力。

研究至少需要：

- 当时官方医院页面是否链接到该域名；
- 当时卫生机构是否列其为授权渠道；
- WHOIS/DNS/备案或企业主体能否交叉；
- 是否有同期官方帮助页给出相同 URL。

不能只看页面 UI。

---

## 4. 2009–2011：预约制度把 Web 表单变成身份事务

2009-09-30 卫生部正式文件要求公立医院开展预约诊疗，并强调实名预约与出诊信息更新。

来源：
- https://www.nhc.gov.cn/bgt/s9514/200909/d5b3893fff4747cdbf91154f5bf109c8.shtml

证据等级：**A**。

这意味着从 old-Web 角度看，预约页面不是普通匿名表单。

### 4.1 account != patient

一个登录账户可能：

- 为本人预约；
- 为父母操作；
- 为儿童登记；
- 与手机号绑定；
- 对应多个 historical patient identifiers。

因此：

`Web account == patient` 是错误模型。

### 4.2 real-name field != verified identity

页面中出现“身份证号”字段，只能证明 UI 要求提交该字段；除非有 backend/规则证据，不能推断：

- 是否实时校验；
- 校验哪个数据库；
- 是否只检查格式；
- 是否到院才最终核验。

### 4.3 family proxy != scalper

实名制往往同时面对两种外观相似但社会语义相反的代理行为：

- 合法家庭照护：子女替父母、监护人替儿童；
- 非法/违规倒号：陌生人囤积、转卖稀缺号源。

历史页面如果只留下“同一手机号最多预约 N 人”一类规则，不能自动推断每一种代理关系怎样被区分。

---

## 5. 2011 `bjguahao.gov.cn`：统一入口，但不是单一系统

### 5.1 historical hostname 与上线日期

2011-07-28 北京市统一预约挂号平台试运行，公开网络入口为：

`www.bjguahao.gov.cn`

并与 `(010)114` 电话预约并行。

来源：
- 国家卫生健康委保存的北京平台启动材料：https://www.nhc.gov.cn/tigs/s10008/201107/4a703577b5264f19b49c04f84edd5249.shtml
- 北京日报同期稿：https://news.sina.com.cn/h/cj/2011-07-28/115822893057.shtml
- 北京晚报同期稿：https://news.sina.com.cn/c/2011-07-28/152422894135.shtml

证据等级：**A + B**。

### 5.2 同期公开流程

2011-07-28 北京日报材料保存的 Web 流程可以最小化为：

```text
注册登录
→ 选择医院/科室
→ 选择日期/医生
→ 填写预约信息
→ 短信验证
→ 预约成功
→ 到医院执行
```

电话通道还有：

```text
拨 114
→ 实名预约
→ 若等待新号源则进入电话等待队列
→ 预约成功后短信/电话确认
→ 获得 8 位识别码
→ 必要时提前取消
```

来源：
- China Daily 保存北京日报流程：https://www.chinadaily.com.cn/dfpd/bj/2011-07/28/content_13000741_2.htm

证据等级：**B — 同时代官方/媒体操作说明。**

这足以建立状态机，但**仍不足以复原历史 DOM 或 backend**。

### 5.3 one public entry != one inventory state

官方材料强调电话和网站统一对外，但医院的：

- 内部 HIS；
- 医生工作站预约；
- 复诊预约；
- 社区转诊；
- 窗口余号；
- 统一平台 quota

可能同时存在。

因此：

> `统一入口` 不应被考古写成 `全北京只有一个 authoritative slot database`，除非有更强技术文档证明。

本轮只能确认统一平台承担面向公众的统一电话/Web 服务和号源数据管理目标。

### 5.4 slot snapshot ephemerality

号源比普通网页内容更短命。

一张 capture 上的：

`某医生 8 月 5 日 有号`

最多只能证明 archive 取得页面时页面**展示**了这种状态，不能证明：

- 页面生成时 slot 仍可锁定；
- capture datetime 与 database query datetime 完全相同；
- 另一用户没有已经抢先提交；
- archive replay 时的显示不是缓存或重写结果。

因此新定义：

### `slot snapshot ephemerality`

**历史号源状态是极短时状态，页面 capture 的时间粒度往往不足以证明一次可执行机会。**

### 5.5 inventory-display / lock gap

```text
slot listed
→ user clicks
→ request reaches backend
→ backend rechecks inventory
→ lock acquired
→ reservation committed
```

任一阶段都可能失败。

所以：

`slot listed != slot locked`

这是预约挂号和普通静态目录最关键的差异之一。

---

## 6. 排队并没有消失，只是进入不同层

### 6.1 phone queue

2011 平台初期报道记录，用户拨 114 后可能先听数分钟等待音乐，热线再进入预约专席；甚至有人凌晨保持电话等待当天早晨放号。

来源：
- 京华时报/新浪，2011-08-04：https://news.sina.com.cn/c/sd/2011-08-04/033422930416.shtml

证据等级：**B**。

### 6.2 Web release-time race

2010 杭州同期报道记录某些热门专家号在线放号后迅速约满，并建议用户提前打开目标专家页、在固定时间点击。

来源：
- 杭州网，2010-11-24：https://hznews.hangzhou.com.cn/kejiao/content/2010-11/24/content_3528841.htm

证据等级：**B**。

### 6.3 server queue / backend contention

旧 Web capture 若只显示普通页面，几乎不会保留：

- 同时在线人数；
- request queue；
- timeout；
- lock contention；
- retry；
- booking service degradation。

因此：

> **“历史页面能正常回放”与“当年高峰时这个服务能正常完成事务”是完全不同的问题。**

---

## 7. 取消、爽约与“患者信用”状态

2011 北京统一预约平台同期规则提出：

- 实名预约次数限制；
- 预约后应提前取消；
- 多次无故爽约可能在一段时间内限制继续使用电话/网络预约。

来源：
- 新华网稿，凤凰保存，2011-06-29：https://health.ifeng.com/news/detail_2011_06/29/7335350_0.shtml
- 同期平台规则：https://news.sina.com.cn/o/2011-07-29/034722896541.shtml

证据等级：**B**。

这产生几个 archive gap。

### 7.1 no-show reason invisibility

历史系统可能保存：

`no-show = true`

却不保存普通生活原因：

- 病情突然恶化去了急诊；
- 症状消失；
- 工作无法请假；
- 火车延误；
- 老人临时无法出门；
- 家属无法陪同。

所以不能把 backend 状态直接道德化为“浪费医疗资源”。

### 7.2 cancellation-release gap

患者取消成功以后：

- 号源是否立刻重新放出？
- 哪个渠道先看到？
- 是否进入人工重新分配？

公开页面往往不解释。

### 7.3 rule-page / enforcement gap

帮助页写“爽约三次限制预约”只证明规则存在，不证明：

- 所有医院执行完全一致；
- backend 在整个时期没有变更；
- 每次 no-show 都被准确记入同一患者。

---

## 8. 2011–2015 第三方平台：front-end aggregation != hospital authority

2011 以后第三方预约平台和医院合作越来越常见。2014 年同期材料描述挂号网/“微医院”可提供：

- 预约挂号；
- 智能分诊；
- 科室医生信息；
- 医院导航；
- 移动端入口。

并称部分合作医院早在 2011 年已开放通过 `guahao.com` 预约。

来源：
- 2014-09-02 同期报道：https://finance.sina.cn/usstock/mtszx/2014-09-02/detail-iawrnsfu1672536.d.html

证据等级：**B — 同时代商业/媒体材料；用户规模和效果类宣传不得直接当独立事实。**

这里新增：

### `aggregator authority gap`

```text
third-party doctor page
≠ hospital doctor schedule

third-party displayed slot
≠ hospital authoritative slot

third-party confirmation
≠ hospital accepted appointment
```

只有确认平台与医院后台的接口关系，才能提升事务结论。

### `normalization gap`

第三方平台可能把不同医院的：

- 科室名称；
- 医生职称；
- 时间段；
- 可约状态；
- 取消规则

统一成自己的字段。

archive 保存的是平台 normalized representation，不一定是医院原始 schema。

---

## 9. 医疗预约特有的“分诊前置”状态

铁路购票可以让用户自己知道目的地；医疗预约未必。

2014 左右移动医疗产品已把“智能分诊”列为预约入口功能之一。2019（超出本仓主时段、只作后续边界）医院又出现病历上传/精准预约等更强分诊机制。

因此 2005–2015 Web 考古需要单独记录：

```text
symptom known to patient
→ patient chooses department
→ platform suggests department (optional)
→ doctor chosen
→ appointment booked
→ clinician later judges whether this was the correct service
```

硬边界：

`platform department recommendation != clinical diagnosis`

`appointment in a department != medically appropriate routing`

如果 archive 只保存最终预约科室，我们不知道患者此前是否曾：

- 搜错科；
- 重新预约；
- 被客服/分诊台改科；
- 先挂普通门诊后转专家。

这是一种重要的 **pre-visit classification invisibility**。

---

## 10. Old-Web artifact preservation levels

建议把历史预约对象分为以下 preservation level。

### H0 — brand/reference only

只知道某时期有“网上预约”服务或 hostname。

### H1 — public shell

保存了医院/平台首页和“预约挂号”入口。

### H2 — help / workflow

保存注册、预约、取消、实名规则或公开操作说明。

### H3 — doctor / department directory

保存科室、医生、出诊信息的历史 representation。

### H4 — interactive form shell

保存选择医院、科室、日期、医生、患者字段的 DOM/form。

### H5 — dynamic inventory representation

保存某时点实际号源/可约状态及相关 payload。

### H6 — transaction protocol

能证明 form action / XHR/API、request fields、session/CSRF 等历史事务接口。

### H7 — controlled historical replay

在不使用真实患者身份和不消耗真实医疗资源的隔离/仿真条件下，可以解释历史 transaction state machine。

### H8 — care-side linkage

有机构级文档能把预约状态和到院报到/就诊状态连接起来。

**最高等级不要求、也不允许以重新公开真实普通患者私人挂号历史作为验收条件。**

---

## 11. Archive capture 需要额外记录的字段

除了 `docs/METHOD.md` 的基本字段，医疗预约建议增加：

```yaml
artifact_role: help|directory|booking_form|slot_result|confirmation|cancel|login|error
institution:
host:
original_url:
capture_url:
capture_datetime:
page_generated_time:
charset_declared:
charset_observed:
login_required:
patient_identity_required:
sms_required:
form_action:
xhr_endpoints:
channel: web|phone_help|hospital_window_reference|third_party
inventory_authority: hospital|municipal_platform|third_party|unknown
slot_timestamp_visible:
appointment_date_visible:
transaction_commit_observable:
subresources_missing:
privacy_risk:
confidence:
```

`page_generated_time` 和 `capture_datetime` 必须分开；历史号源页尤其不能把 archive 时间直接当 backend snapshot 时间。

---

## 12. 浏览器、编码、脚本与 transaction replay

预约系统很可能比普通内容页更依赖：

- 登录 cookie；
- session；
- JS；
- AJAX/XHR；
- 动态 select；
- 短信验证码；
- Captcha；
- 跨域/第三方支付或通信服务；
- server-generated token。

因此现代 Wayback “看起来能点”也不意味着历史事务可重演。

### 12.1 charset

2005–2011 中文医院站可能使用 GB2312/GBK/UTF-8 中的任意一种，必须以具体 capture header/meta 为准，不能凭年份猜。

### 12.2 JavaScript

若历史页面的医院/科室/医生级联菜单由 JS 生成：

`static HTML survives != choices survive`

### 12.3 AJAX slot payload

如果号源通过 XHR 读取：

`booking shell survives != inventory survives`

### 12.4 SMS verification

短信是 archive 外的第二信道：

`Web form captured != verification channel captured`

### 12.5 live-backend contamination

最危险的情况是一个旧 URL 今天仍能打开，却已经连接到：

- 新平台；
- 新医生库；
- 新实名系统；
- 当前 2026 backend。

这种结果只能叫：

> **current-backend rehydration**

绝不能写成 historical transaction replay。

---

## 13. 隐私与伦理边界

医疗预约天然涉及高敏感信息。

禁止把以下内容作为“复原完整度”的目标：

- 普通个人姓名 + 身份证号；
- 手机号；
- 具体疾病 + 可识别个人；
- 私人预约历史；
- 短信验证码；
- 就诊卡号；
- 医保凭证；
- 私人病历/检查资料。

优先使用：

- 官方帮助页；
- 测试/demo 账号（若合法公开）；
- 同期新闻中已经匿名化的用户经历；
- 公开医生/科室页面；
- institution-level workflow；
- schema/state reconstruction。

本研究的目标是恢复**系统如何工作**，不是恢复某个普通人的病史。

---

## 14. 历史可见性偏差

### 14.1 booking-success survival bias

媒体、帮助页和平台案例更容易保存“预约成功”。

真正失败的：

- 电话永远占线；
- 页面超时；
- 点到专家后号没了；
- SMS 没收到；
- 到院身份不匹配；
- 临时停诊

更容易无痕消失。

### 14.2 slot terminal-state bias

最终“已约满”截图会把此前几小时的：

- 有号；
- 退号；
- 重新放号；
- 锁定未支付/未确认（若有）

全部压扁成一个终态。

### 14.3 public-shell bias

公开首页和医生介绍最容易被 archive 抓到；用户登录后的预约表单和事务结果最难保存。

### 14.4 successful-filter bias

实名制/反黄牛越成功，很多被系统拒绝的异常请求越不会留下公开 Web artifact。

### 14.5 offline-completion gap

真正的医疗结果发生在线下：患者最终有没有被医生看、诊断是什么、是否转科，archive 通常不知道。

---

## 15. 本轮 historical replay 尝试

### 15.1 `www.bjguahao.gov.cn`, 2011

本轮根据 2011 同期官方/媒体资料确认 historical hostname，并尝试直接打开一个约 2011 年的 Wayback replay URL。

当前研究客户端拒绝了未经已有搜索结果 provenance 建立的构造 `web.archive.org` URL，返回 safe-URL 限制，因而未取得真实 memento 内容。

结论：

> **M1 verified 2011 `www.bjguahao.gov.cn` historical capture: NOT ACHIEVED IN THIS SLICE.**

这只说明本轮没有实际核验成功，**不等于 Internet Archive 没有保存该站点。**

### 15.2 `www.bjcyh.com.cn`, 2009

同期官方材料已经确认 2009-09 的网站主体与“主页 → 预约挂号”路径，但本轮没有取得可核验：

- capture datetime；
- historical HTTP status；
- charset；
- DOM；
- form action；
- JS；
- booking result payload。

结论：

> **M1 verified 2009 Beijing Chaoyang Hospital booking-page capture: NOT ACHIEVED IN THIS SLICE.**

### 15.3 `guahao.com`, 2011–2014

本轮取得 2014 同期合作/产品描述，但未验证对应历史页面 capture 与具体 backend contract。

结论：

> **platform feature evidence achieved; verified historical transaction capture not achieved.**

---

## 16. 已证实 / 高概率 / 不知道

### 已证实

- 2009 北京多家三级医院已经同时存在电话、窗口、网络等预约方式。
- 北京朝阳医院 2009 年通过自身网站提供预约入口。
- 2009 国家层面明确推动公立三级医院实名预约诊疗。
- 2011 `www.bjguahao.gov.cn` 与 114 构成北京统一预约挂号的公众入口。
- 2011 同期资料明确存在注册、医院/科室/医生选择、实名患者信息、短信/电话确认、取消与预约限制。
- 同一时期热门专家号仍高度稀缺，电话/Web 都存在新的等待与争抢。
- 2009 已存在搜索结果导向非官方/不规范预约入口的同期风险证据。

### 高概率但本轮不提升为确定技术事实

- 统一平台与医院内部系统之间存在某种号源数据同步/接口层。
- Web 与电话在部分情况下读取同一总体号源池，但具体 quota、lock 与一致性机制可能因医院/时期不同。
- 2009–2015 越来越多平台把号源查询做成 AJAX/动态事务，而不是纯静态 HTML。

### 不知道

- 2009 朝阳医院预约页面的准确历史 endpoint 与 DOM。
- 2011 统一平台的历史 charset、JS stack、XHR endpoint、session/token 设计。
- 某个具体 capture 中显示的号源是否在那一瞬间仍可真正锁定。
- Web/114/医院内部各渠道在每个时期的 authoritative ownership 与冲突处理规则。
- 一次历史“预约成功”页面背后是否已经完成医院 HIS/PAS commit。

---

## 17. 下一步最值得做的三项 bounded work

### A. Verified `bjguahao.gov.cn` memento

目标只做到：

- 1 个 2011–2012 首页/帮助页 capture；
- 1 个预约流程相关 capture；
- 记录 original/capture URL、datetime、HTTP、charset、DOM、缺失子资源；
- 不登录、不提交真实患者信息。

### B. Beijing Chaoyang 2009 page genealogy

查：

`homepage → appointment entry → form/help → confirmation semantics`

优先找：

- Wayback；
- 同期新闻截图；
- 医院/卫生局旧页面；
- 2009 用户教程。

### C. Phone/Web inventory asymmetry

找一个 2010–2012 医院，使用同期材料核验：

- 电话能约但 Web 不能约；
- Web 有号电话无号；
- 不同渠道 quota；
- cancellation 后哪个渠道先看到。

这比再收集十张“预约挂号首页”更能改变结论。

---

## 18. 对跨仓生活史的贡献

这个对象把 old-Web archaeology 与普通生活史接得非常紧：

- 历史 Web 页面把**未来医疗机会**变成了屏幕上的状态；
- 实名制度把机会与一个具体制度身份绑定；
- 电话/Web 把一部分身体等待搬成远程请求；
- 但专业稀缺、科室分类和现实就诊仍然存在；
- 家庭成员开始能够远程替老人/儿童维护预约状态；
- archive 最容易保存的是“预约功能存在”，最难保存的却是一个普通人当时为什么最终没能看上病。

因此以后看到历史医院页上的“预约挂号”四个字，最低正确反应应该不是：

> “当时已经可以网上看病了。”

而是继续问：

> **这个页面当时到底连接了哪个号源系统、要求什么身份、能否真正提交、如何确认、失败时怎么办，以及成功以后还要完成多少线下步骤？**
