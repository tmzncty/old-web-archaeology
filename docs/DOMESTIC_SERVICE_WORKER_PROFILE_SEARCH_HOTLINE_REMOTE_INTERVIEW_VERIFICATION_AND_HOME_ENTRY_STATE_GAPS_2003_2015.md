# 家政服务网站：劳动者档案、搜索、热线、远程面试、核验与入户结果状态差（2003–2015）

## 0. Scope

本 note 研究 **2003–2015 中文互联网中的家政 / 保姆匹配界面**，重点不是写家政行业通史，而是回答：

> 当旧网页说“这里有一位保姆”“可以在线选阿姨”“可以视频面试”“资料已登记/已核验”时，这些页面状态距离现实中一个具体劳动者真正进入一个具体家庭工作，还有多少没有被 Web 保存的步骤？

本对象与 `CLASSIFIED_LISTING_CITY_CATEGORY_CONTACT_RANKING_VERIFICATION_AND_REAL_WORLD_OUTCOME_STATE_GAPS_2005_2015.md` 相邻但不重复。

一般分类信息多为“发布一条需求/供给 → 联系 → 一次交易或招聘”。家政服务则具有额外特征：

- 劳动者本人常成为长期可检索 profile，而不只是某条 listing；
- 服务发生在私人住宅；
- 可能面对婴幼儿、老人、病患和家庭财物；
- 身份、健康、培训、保险、证书等 trust attributes 比普通分类信息更突出；
- 匹配之后需要持续相处，`成交` 不是终点；
- 大量沟通会迅速逃逸到电话、QQ、短信、视频、线下门店和家庭内部。

**仓库主 scope 保持 1995–2015 中文互联网。** 1980s–1990s 家政前史只作为解释 2000s 混合架构的必要背景；海外比较进入 `how-people-lived`，不把本仓扩成全球家政互联网史。

交叉研究：

- `tmzncty/how-people-lived/topics/paid-domestic-service-care-labor-addressability-household-time-outsourcing-and-trust-infrastructure-china-1984-2026.zh-CN.md`

---

## 1. Claim list first

本轮只建立以下可检验 claim：

1. 2006 年杭州已经出现以 QQ / 视频为入口的“网上找保姆”服务，但同期现场报道显示，实际键盘输入由家政机构工作人员代劳，一部分劳动者本人不会使用电脑。
2. 2007 年北京存在“网站查询本地区热线 → 电话联系 → 线下家政匹配”的 Web/telephone hybrid，而不是纯 Web transaction。
3. 2008 年广州 96909 体系把家政劳动者做成带编号的可查询数据库记录，并有快速变化的待业/从业状态、培训和保险信息。
4. 2009 年对“川妹子”家政公司的报道回顾其 2003 年已经尝试网上展示劳动者资料与订单，并用远程面试降低跨城初次筛选成本；但该报道不是 2003 年 historical capture。
5. 对家政类旧网页而言，`profile visible` 与 `worker physically entered household` 之间至少还有 availability、contact、interview、identity/trust check、agreement、travel/home access 等多个不可从公开页面自动推出的状态。
6. 当前没有取得一个按本仓 METHOD 实际打开并检查、同时满足 original URL / capture datetime / replay state / charset / DOM / interaction structure / second time point 的合格早期中文家政网站 M1 capture。

---

## 2. Research units

严格分离以下对象：

### People / legal states

- `worker_person`：现实劳动者；
- `worker_legal_identity`：法定身份；
- `household_employer/person`：现实雇主或家庭联系人；
- `agency_staff`：线下/线上中介工作人员；
- `care_recipient`：婴幼儿、老人、病患等实际服务对象。

### Platform / record states

- `platform/site`；
- `agency account`；
- `worker profile`；
- `worker identifier`；
- `availability status`；
- `skill/certificate record`；
- `training record`；
- `insurance record`；
- `health record`（若当时系统存在）；
- `verification badge/status`；
- `search query`；
- `search result set`；
- `profile detail page`；
- `employer requirement/order`；
- `message/QQ session`；
- `video interview session`；
- `phone hotline/call record`；
- `booking/recommendation record`；
- `contract/agreement`；
- `payment/intermediary fee`；
- `service start/home entry`；
- `service period`；
- `wage due/paid`；
- `review/complaint/blacklist state`；
- `archive capture`。

### Archive states

- original resource；
- Memento/capture；
- replayed main HTML；
- subresources；
- form/action endpoint；
- backend database state；
- telephone/QQ/video handoff；
- later survivor/repost；
- research claim。

这些对象不得相互替代。

---

## 3. Permanent state gaps

### 3.1 人与 profile

```text
real worker
!= legal identity record
!= agency registration
!= web profile
!= currently active profile
!= currently available worker
```

页面里存在一个“保姆档案”只能证明平台在那个状态下表示这个 profile 存在。

不能自动证明：

- 劳动者本人仍在该公司；
- 此刻仍待业；
- 电话仍有效；
- 本人知道页面仍在线；
- 本人同意今天继续公开这些资料。

### 3.2 核验

```text
identity checked
!= skill checked
!= certificate valid/current
!= health suitable for a specific task
!= trustworthy in every context
!= good household fit
```

历史页面中的“已认证”“已登记”“已保险”必须保留其具体对象。

不要把一个 badge 升格为对整个人的总认证。

### 3.3 搜索与结果

```text
query submitted
!= backend index successfully queried
!= result row returned
!= profile currently available
!= contact succeeds
```

尤其是家政 availability 可能按小时改变。2008 年 96909 的同期报道明确说平台按小时更新劳动者信息，这意味着一张 archive search result 即使存在，也只应被理解为某一瞬间的数据库表示。

### 3.4 QQ / 视频与“谁在用电脑”

```text
QQ session exists
!= worker owns QQ account
!= worker typed the text
!= worker can independently operate computer
```

2006 年杭州现场报道中，机构工作人员实际替不会电脑的劳动者打字并转述。

因此网页/新闻所说的“网上和保姆聊”不能未经检查改写为“保姆本人在线聊天”。

### 3.5 联系与现实服务

```text
message sent
!= message received/read
!= phone connected
!= interview happened
!= household accepted worker
!= worker accepted household
!= agreement signed
!= worker travelled/arrived
!= worker entered home
!= service continued
!= wage settled
```

这条链是本研究对象最重要的历史不可见区。

### 3.6 公司、中介与劳动关系

```text
platform/agency introduced worker
!= platform/agency is legal employer
!= platform/agency pays wage
!= platform/agency bears all service liability
```

旧网页上的 logo、公司地址或“推荐”不应被当作劳动关系证明。

---

## 4. Case slice A — “川妹子网上保姆超市”（2003 起的回顾线索）

2009 年新浪科技的一篇企业报道回顾称，“川妹子”家政公司 2003 年开始电子商务尝试，曾把 200 多名劳动者资料放进所谓“网上保姆超市”；雇主可挑选资料、提交订单，公司再回复。报道还以 2002 年上海雇主为面试劳动者支付多人机票成本为例，说明远程 profile / interview 可以降低“先见一面”的跨城成本。

来源：

- 新浪科技，2009-09-13：<https://tech.sina.com.cn/i/2009-09-13/09403433309.shtml>

### Evidence grade

- **B/C, T2**：2009 同期企业报道中的 2003 历史回顾。
- 不是 2003 年原始网页；
- 没有 historical DOM / screenshot / capture；
- 公司自报业务比例不能作为行业 adoption rate。

### What it supports

窄 claim：

> 至迟在 2009 年可核验的公司历史叙述中，该企业把 2003 年视为自己开始用网页展示劳动者资料、接收订单并探索远程面试的阶段。

### What it does NOT support

不得凭此写：

- 2003 页面一定使用 tables/frames；
- charset 一定是 GB2312/GBK；
- 必须 IE6；
- profile 有哪些精确字段；
- 订单表单的 POST/GET endpoint；
- 当年页面真实流量；
- 当年成交比例。

---

## 5. Case slice B — 杭州 QQ / 视频找保姆（2006）

青年时报 2006 年现场报道：杭州某家政市场推出通过 QQ 和视频找保姆的服务。记者到现场后发现，与雇主在线交流的主要是家政机构服务人员；劳动者本人站在旁边，由工作人员代打字、转述。一位劳动者说自己识字不多，更不会电脑，仍偏好直接见雇主。

来源：

- 青年时报 / 新浪，2006-02-10：<https://news.sina.com.cn/s/2006-02-10/10508171869s.shtml>

### Evidence grade

- **B, T1**：同时代现场报道。

### State model

```text
employer computer
→ QQ/video channel
→ agency staff account/interface
→ staff reads/types
→ worker hears/responds orally
→ staff relays response
```

而不是默认：

```text
employer ↔ worker's own QQ account
```

### New archive warning: `proxy-input / apparent-user gap`

未来若只剩 QQ 截图、网站宣传或“在线咨询”按钮，研究者很容易把文本界面中的 speaker 当成劳动者本人。

这个案例说明：**界面里出现“阿姨回复”并不能自动证明阿姨本人操作了界面。**

必须寻找：

- 账号归属；
- 操作设备；
- 工作人员是否代理；
- 文字是否为转述；
- 视频是否 worker direct / staff mediated。

---

## 6. Case slice C — 北京家政就业热线 + Web directory（2007）

2007 年北京晨报报道，北京家政服务相关机构开通多部本地家政就业热线；公众可以通过 `www.jiazhengbj.org` 或 `www.bjcs.gov.cn` 查询热线列表，再通过电话进入匹配。

来源：

- 北京晨报 / 新浪，2007-01-01：<https://news.sina.com.cn/c/2007-01-01/023510905731s.shtml>

### Evidence grade

- **B, T1**。

### Architecture claim

这是典型：

```text
Web discovery / directory
→ telephone hotline
→ human operator
→ local matching
→ offline service
```

不是：

```text
Web page
→ fully online hiring transaction
```

### New archive warning: `web-entry / phone-handoff gap`

即使今天完整拿到当年网站 HTML，也最多可能恢复：

- 某区县热线号码；
- 服务说明；
- 组织结构；
- 入口文字。

真正的劳动匹配记录已经离开 Web，进入电话和人工业务系统。

因此：

`website recovered != service transaction recovered`

---

## 7. Case slice D — 广州 96909 劳动者登记数据库（2008）

2008 年南方日报、羊城晚报同期报道，广州 96909 体系上线家政服务人员资料登记系统，3000 多名从业人员资料进入数据库；劳动者有编号，雇主可到 `www.96909.com.cn` 查询。报道还提及：

- 近六成登记人员当时处于待业状态；
- 平台按小时更新人员信息；
- 信息涉及从业、培训、保险；
- 编号与身份核验流程相连；
- 雇主也可以拨打 96909 获取帮助。

来源：

- 南方日报 / 新浪，2008-07-29：<https://news.sina.com.cn/c/2008-07-29/024414231312s.shtml>
- 羊城晚报 / 新浪，2008-07-29：<https://news.sina.com.cn/c/2008-07-29/140014235251s.shtml>

### Evidence grade

- **B, T1**，两个媒体文本应检查是否部分共享协会通稿；不能机械算两个完全独立 evidence family。

### State model

```text
worker registered
→ identifier assigned
→ profile record
→ availability flag/status
→ search by identifier
→ employer gets information
→ phone / agency contact
→ real interview / hiring
```

### `availability-state ephemerality`

由于报道明确说劳动者状态按小时更新：

`profile captured at 10:00 != availability at 14:00`

如果 archive 只抓到一张静态页面，它保存的是某一版数据库投影，不是劳动者长期固定属性。

### `verification-badge / underlying-evidence gap`

即使历史 profile 显示“身份核验”“培训”“保险”，也应分别问：

- 谁核验？
- 核验对象是什么字段？
- 数据在何时有效？
- 后台证明材料是否属于敏感信息？
- archive 是否只留下前台 badge，而没有后台证据？

隐私原则要求：**不要为了证明旧网页真实性而重新公开劳动者身份证号、健康材料或详细住址。**

---

## 8. 不是所有“在线家政”都由劳动者本人在线完成

2006 QQ 案例说明一个容易被 Web archaeology 忽略的角色：**digital proxy**。

数字系统的使用者可能是：

- 雇主本人；
- 家政机构工作人员；
- 劳动者的亲属；
- 社区服务点人员；
- 劳动者本人。

因此建议在 future evidence schema 加一个概念字段（本 note 暂不改 schema）：

```yaml
interface_operator:
  type: [worker, employer, agency_staff, relative, unknown]
  evidence: ...
```

否则“谁点了按钮”会被错误地与“页面中描述的是谁”合并。

---

## 9. 旧网页最容易留下什么，最容易丢掉什么？

### 9.1 `profile-shell survival / household-fit loss asymmetry`

最容易保存：

- 姓名/昵称（若公开）；
- 年龄；
- 籍贯；
- 工种；
- 工作经验；
- 工资要求；
- 证书 badge；
- “立即联系/预约”按钮。

最难保存：

- 雇主是否真正打电话；
- 双方是否喜欢对方；
- 家庭成员边界是否冲突；
- 婴儿/老人是否适应；
- 劳动者是否觉得工作条件合理；
- 干了三天、三个月还是三年；
- 为什么离开。

因此 archive 天然高估 **profile legibility**，低估 **relationship durability**。

### 9.2 `worker-profile survival / labor-rights loss asymmetry`

公开 profile 可能留下技能和工资报价，却不会留下：

- 实际工时；
- 夜间起身次数；
- 是否有独立房间；
- 是否休息；
- 是否拖欠工资；
- 是否临时加任务；
- 谁承担保险；
- 是否存在书面劳动/服务协议。

这会让未来研究者看到一个“非常可搜索的劳动者”，却看不到她的工作生活。

### 9.3 `web-entry / private-channel escape`

Web 页面经常只是第一跳：

```text
Web → phone
Web → QQ
Web → SMS
Web → video
Web → physical agency
```

真正关系会主动离开 crawler 最能保存的公开页面。

### 9.4 `availability-state loss`

待业/在岗、可约/不可约是高频变化状态。

archive 即使能保存 profile，也可能根本没抓到异步后台数据、AJAX 返回或某一小时的 availability flag。

### 9.5 `public-profile / private-proof inversion`

最容易公开保存的是前台“已认证”；最能证明认证过程的身份证件、背景信息、健康资料却最私密、最不应该被重新公开。

因此证据完整度必须主动服从隐私最小化。

---

## 10. 反例：HTML 完整也不等于现实事务完整

对这个研究对象，即使未来拿到一个 **100% 完整的 2008 页面 replay**，仍然无法仅凭网页证明：

- 劳动者是否在网页抓取后一小时被雇走；
- 电话是否接通；
- 雇主和劳动者是否见面；
- 劳动者是否从外地真正抵达；
- 是否进入家庭；
- 是否完成一整月服务；
- 工资是否支付；
- 关系为何结束。

因此 old-web archaeology 的结论必须停在 Web 可证明的边界。

---

## 11. Browser / charset / implementation assumptions

本轮 **没有**取得合格 historical capture，因此以下一律不推断：

- IE-only；
- IE6；
- ActiveX；
- Flash；
- table layout；
- frameset；
- GB2312 / GBK / UTF-8；
- Java Applet；
- 页面分辨率；
- 表单 GET / POST；
- 是否 Java/JSP/ASP/PHP；
- 数据库类型；
- QQ/video 具体嵌入方式。

新闻里说“可以上网查”只证明功能叙述，不证明页面实现。

---

## 12. Archive search status

本轮围绕以下对象进行了历史 capture locator 搜索：

- “川妹子网上保姆超市”及企业网站线索；
- `www.jiazhengbj.org`；
- `www.bjcs.gov.cn` 相关家政热线页；
- `www.96909.com.cn`；
- 2006 杭州 QQ / 视频找保姆服务。

取得的是：

- 同时代新闻；
- 后来企业历史报道；
- original URL / host 线索；
- 功能描述。

没有取得一份已实际打开并检查、同时满足以下项目的 M1 capture：

- exact `original_url`；
- `capture_url`；
- `capture_datetime`；
- replay / HTTP 状态；
- historical charset；
- DOM / form / profile structure；
- subresource state；
- interaction endpoint；
- 第二历史时点。

因此严格记录：

> **M1 verified historical Chinese domestic-service worker-profile / search / remote-interview capture: NOT ACHIEVED IN THIS SLICE.**

这不是“Wayback 没保存”的结论。

`not found in current search` 不能升级为 `archive has no capture`。

---

## 13. Privacy boundary

家政 profile 比一般商品 listing 更容易包含今天不应重新聚合的普通人信息，例如：

- 本名；
- 头像；
- 年龄；
- 籍贯；
- 手机；
- 身份编号；
- 婚育情况；
- 健康情况；
- 培训证件；
- 过往雇主评价；
- 住家/非住家偏好。

即使 archive 中存在：

- 本仓优先研究字段结构、页面状态与平台机制；
- 不批量再发布普通劳动者 profile；
- 不建立可搜索的历史身份证/手机号集合；
- 引用个人案例只保留支持 claim 所需的最少信息；
- 对健康、犯罪背景、住址等高敏感信息坚持更高阈值。

`historically public != ethically necessary to republish now`。

---

## 14. 与 generic classifieds 的区别

| 状态 | 普通分类信息 | 家政 profile / service |
|---|---|---|
| 基本对象 | 一条商品/工作/租房 listing | 一个持续存在的劳动者 profile + household requirement |
| 时间状态 | listing 是否有效 | 劳动者是否待业、可否住家、档期 |
| 信任 | 发布者真实性、货/岗真实性 | 身份 + 技能 + 健康/培训/保险 + 私宅边界 |
| 事务终点 | 成交/招聘 | 入户只是开始，长期 household fit 才决定持续 |
| Web 外逃 | 电话/私信/见面 | 电话/QQ/视频/门店/家庭内部持续关系 |
| 隐私风险 | 联系方式、地址 | 额外包含劳动者身份、健康、家庭/履历等 |
| archive 偏差 | listing 留下、成交消失 | profile 留下、真实照护关系和劳动条件消失 |

因此本 note 不应合并回 generic classifieds 文件。

---

## 15. What is established / probable / unknown

### 已证实

- 2006 杭州存在由家政机构工作人员代理 QQ/视频输入的线上找保姆服务；
- 2007 北京至少存在“网站查热线 → 电话匹配”的混合入口；
- 2008 广州 96909 同期报道描述了劳动者资料数据库、编号查询和按小时更新；
- 2000s 的在线入口与电话、人工中介、线下面试长期共存；
- 身份/培训/保险等信息已经逐渐进入数字匹配界面。

### 高概率 / 可合理推断

- 中文早期家政网站的最大生活影响之一，是降低跨城初次筛选和信息搜索成本；
- Web 只是整个事务链的一层，大量关键状态进入电话/QQ/线下后不可见；
- 劳动者数字能力与服务数字化程度可能严重不对称；
- 家政 profile 的 archive survival 会系统性高估我们对真实劳动关系的了解。

### 不知道

- `www.96909.com.cn` 在 2008 年的精确 DOM / CSS / charset / query 参数；
- 劳动者详情是否有静态 permalink；
- availability 数据是否 server-rendered、独立接口或页面内字段；
- 早期“川妹子网上保姆超市”的原始 URL pattern；
- 2006 杭州 QQ 服务使用个人 QQ、企业账号还是其他终端组织方式；
- archive 是否保存了可重放的搜索结果与 profile pair；
- 历史 profile 是否在页面关闭后仍被搜索引擎缓存；
- 服务完成/离职等结果状态是否曾回写平台。

---

## 16. 下一步 M1 证据任务

只有拿到实际 capture 后再推进页面形态：

1. 为 `www.96909.com.cn` 建 original URL 候选列表：主页、search、worker detail、help；
2. 检查 2008-07、2008-08、2009 至少两个时点；
3. 记录 HTTP/replay、charset、DOM、form action、worker ID query pattern；
4. 单独检查 CSS/JS/image 是否保存；
5. 判断劳动者状态是 HTML 固化还是动态后台；
6. 对普通人 profile 只记录字段 schema，不批量镜像个人内容；
7. 若 96909 不满足 M1，再转 `jiazhengbj.org` 或可核验的早期企业家政站；
8. 至少用一个同期教程/媒体操作说明作为独立 evidence family。

在上述步骤完成前，本 note 保持 research state-gap document，不宣称页面复原完成。

---

## Sources

### 同时代 / 近同时代中国材料

- 青年时报 / 新浪，2006，“视频找保姆其实还靠二传手”：<https://news.sina.com.cn/s/2006-02-10/10508171869s.shtml>
- 北京晨报 / 新浪，2007，家政就业热线：<https://news.sina.com.cn/c/2007-01-01/023510905731s.shtml>
- 南方都市报 / 新浪，2008，96909 与家政公司联盟：<https://news.sina.com.cn/c/2008-01-16/040313266916s.shtml>
- 南方日报 / 新浪，2008，96909 人员登记数据库：<https://news.sina.com.cn/c/2008-07-29/024414231312s.shtml>
- 羊城晚报 / 新浪，2008，登记信息与保险：<https://news.sina.com.cn/c/2008-07-29/140014235251s.shtml>
- 新浪科技，2009，“川妹子”互联网家政回顾：<https://tech.sina.com.cn/i/2009-09-13/09403433309.shtml>
- 东方早报 / 搜狐上海，2010，家政匹配渠道调查：<https://sh.sohu.com/20100317/n270882034.shtml>

### 后续边界材料（不用于扩大本仓时间 scope）

用于确认 2000s 已出现的 trust / profile 问题后来怎样制度化，不作为 1995–2015 页面形态证据：

- 商务部，2019，家政信用信息平台：<https://fms.mofcom.gov.cn/jmshfw/fgzc/art/2019/art_091a5aa915aa4317af3f6fffc94661a4.html>
- 商务部，2020，防疫健康信息：<https://fms.mofcom.gov.cn/jmshfw/fgzc/art/2020/art_fbc22dc52b67423099f1e3ec7df7f685.html>

---

## 17. Core archaeological insight

旧网很容易让后人产生一种错觉：

> “只要 profile 页面还在，这个人当年的工作状态就被保存下来了。”

家政恰好证明相反。

一个页面可以把某人的年龄、籍贯、技能和“当前待业”保存得非常完整，却完全没有保存：她有没有接到那通电话、愿不愿意去那个家庭、有没有赶到另一座城市、雇主是否改变条件、婴儿是否适应、工资有没有结清、三天后为什么离开。

因此家政网站的历史价值不只是“早期生活服务网站长什么样”，而是让我们看见 Web 保存能力的边界：

> **网页最擅长保存一个陌生人变得可搜索的时刻；最不擅长保存这个陌生人真正进入另一个人的生活以后发生了什么。**
