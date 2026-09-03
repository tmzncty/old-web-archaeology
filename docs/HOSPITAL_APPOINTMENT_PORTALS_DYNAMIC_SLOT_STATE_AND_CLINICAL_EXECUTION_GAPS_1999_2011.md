# Hospital appointment portals, dynamic slot state and clinical-execution gaps · 1999–2011

> Status: research note / evidence contract.
>
> Scope: **中文互联网约 1999–2011 年医院预约挂号页面、医院官网、第三方预约入口与北京统一预约平台的 Web archaeology**。
>
> This is **not** a history of Chinese medicine, hospital reform, telemedicine in general, or post-2011 mobile health.
>
> Cross-repo life-history note: `tmzncty/how-people-lived/topics/care-path-addressability-appointmentability-and-navigation-labor-china-1953-2025.zh-CN.md`.

---

## 0. Why this belongs in old-web-archaeology

旧网仓已经处理过：

- job-board application execution gaps；
- housing / roommate listing states；
- dating-profile reciprocal selection；
- online banking transaction state；
- credential-query dynamic databases；
- network-education account / progress state；
- second-hand listing transaction outcomes。

医院预约又是一类非常典型、但此前没有单独建模的 **dynamic transaction-like web object**。

一个静态医院页面可能写：

- 科室；
- 医生；
- 出诊日期；
- “网上预约”；

但普通人真正关心的是：

> **2008 年 8 月某一天、某个账号、某位医生、某个时间段，当时到底还有没有号，以及那次请求最后有没有变成真实就诊。**

这恰恰是公开 Web archive 最难完整保存的部分。

因此本篇的核心规则是：

```text
appointment page survived
≠ historical doctor schedule survived
≠ historical slot inventory survived
≠ booking request succeeded
≠ confirmation reached patient
≠ patient arrived
≠ check-in succeeded
≠ clinical encounter occurred
```

---

# 1. Scope boundary

## 1.1 In scope

约 1999–2011 中文 Web 中的：

- 医院官网预约挂号入口；
- 医生 / 科室排班页；
- 号源与预约表单；
- 预约卡 / 就诊卡与 Web 的混合接口；
- 医院官网到第三方预约站的 handoff；
- Email / SMS / 电话确认与 Web 的边界；
- 北京统一预约挂号平台早期形态；
- 实名预约在网页状态中的体现；
- 预约、取消、爽约规则；
- 与 archive 保存直接有关的浏览器 / session / dynamic backend 问题。

## 1.2 Out of scope

本篇不做：

- 疾病诊断或治疗建议；
- 医生质量排名；
- 患者医疗结果评价；
- 互联网医院 2020s 史；
- 医保全史；
- 医疗 App / 微信全史；
- 恢复任何私人患者账号；
- 搜集泄露病历、预约数据库、手机号或身份证；
- 批量重新公开历史患者敏感信息。

## 1.3 Prehistory boundary

1950s 电话预约和 1993 院内计算机预约对理解 1999 Web 很重要，但它们主要写入 `how-people-lived`。

本仓只把它们作为必要前史边界：

> **Web 没有发明预约；Web 改变的是患者自己远程查询、提交和维护预约状态的能力。**

---

# 2. Evidence grades used here

沿用仓库 A/B/C/D：

- **A**：原始 / 同时代页面、手册、政府原始文件、可定位 capture；
- **B**：同时代或近同时代新闻、记者实测、教程；
- **C**：后来回忆 / 历史专题；
- **D**：本篇的状态机和 archive-gap 推断。

重要限制：

本轮没有取得足够稳定、可逐字段核验的 1999 / 2003 原始 WARC 或 Wayback capture。

因此：

- 不伪造 DOM；
- 不猜字符集；
- 不猜脚本框架；
- 不猜 IE-only / ActiveX；
- 不把报道中描述的流程冒充实际 HTML。

**“历史页面未在本轮取到”是合法结论。**

---

# 3. Pre-Web boundary: appointment existed before the Web

## 3.1 1953 / 1954 / 1993 only as boundary evidence

2020 年《北京日报》根据本报数据库整理预约挂号史，并给出原报日期、版面和标题：

- 1953：北大医院现场预约未来就诊；
- 1954：部分公费医疗单位通过电话向医院预约；
- 1993：同仁医院使用计算机管理系统预约未来科室 / 医生。

Source:

<https://k.sina.cn/article_1893892941_70e2834d02000ryrc.html>

### Evidence grade

- 本轮未直接取得 1953 / 1954 / 1993 原始报纸扫描；
- 对旧网仓只记为 **C/B boundary evidence**；
- 不进入 1995–2015 主体样本。

### Why it matters

它阻止一种错误谱系：

```text
manual queue
→ Web appointment
```

更准确：

```text
future-slot allocation
→ phone mediation
→ institutional computerisation
→ phone/Web self-service
→ unified platform
```

因此 old-Web 研究需要问：

> **哪些状态原本已经在医院后台存在，只是后来通过 Web 暴露给患者？**

---

# 4. 1999 Beijing: card + phone + Web as one hybrid system

## 4.1 What is supported

2006 年同时代回顾报道记载，北京市卫生局 1999 年 9 月推出预约挂号“一卡通”，后有 50 多家医院参加；患者购买卡后可以电话或网上预约。

Source:

<https://finance.sina.com.cn/xiaofei/consume/20060119/07102288409.shtml>

北京日报 2020 年历史资料整理进一步定位到：

- 1999-09-17，北京日报 5 版《网上挂号一卡通》；
- 通过当时“北京卫生信息网”可以预约多家医院；
- 卡既可网上也可电话使用，也可为亲友预约。

Source:

<https://k.sina.cn/article_1893892941_70e2834d02000ryrc.html>

## 4.2 What is NOT yet supported

本轮没有直接恢复：

- 1999 北京卫生信息网的具体 historical URL；
- 页面 capture datetime；
- HTML / DOM；
- 编码；
- 登录字段；
- 预约卡号格式；
- 浏览器要求；
- 后端请求；
- 历史医生列表；
- 当日号源。

因此不能写：

> “1999 页面长这样 / 用这个脚本 / 必须 IE。”

这些目前都是 unknown。

## 4.3 Archaeological model

从已知流程，至少可以确定系统不是纯 Web：

```text
physical card / entitlement
       ↘
phone --- appointment backend --- hospital
       ↗
Web
```

所以即使未来发现首页 capture，也不能把 capture 当成完整系统。

### New gap: entitlement-artifact gap

> **public Web survived ≠ physical appointment-card entitlement survived**

如果历史用户必须先购买 / 持有实体卡，现代研究者打开网页也未必能重现真实预约路径。

---

# 5. 2003 Suzhou: one of the clearest early execution descriptions

## 5.1 Contemporary report

2003-08-02 人民网—江南时报报道苏州大学附属第一医院上线网上预约挂号。

Original domain reported at the time:

`www.sdfyy.cn`

Source:

<https://news.sina.com.cn/o/2003-08-02/1058491035s.shtml>

报道描述：

```text
first registration
→ department information
→ expert list
→ choose department / date / doctor
→ submit
→ backend checks quota
→ receive appointment number
→ on visit day: offline payment / number collection
```

还支持：

- 名额超过上限时提示改时间；
- 可查询已预约记录；
- 可取消预约；
- 当时为提前两天左右的短预约窗口。

## 5.2 Evidence grade

**B — contemporaneous reporting with concrete workflow and original domain.**

没有直接 capture，因此：

- 页面视觉 unknown；
- 表单字段 exact names unknown；
- session / cookie unknown；
- charset unknown；
- browser assumption unknown。

## 5.3 Archaeological significance

这是一个完整的 **hybrid execution boundary**：

```text
Web owns:
- discovery
- future schedule choice
- quota check
- reservation state
- cancellation

Hospital still owns:
- payment
- physical number collection
- arrival
- clinical encounter
```

因此：

> **online appointment ≠ online outpatient visit**

---

# 6. 2004–2006: existence did not mean default adoption

2006 年报道给出 2004 年北京市各级医院门急诊总量约 5035 万人次、预约挂号约 32.5 万人次。

Source:

<https://finance.sina.com.cn/xiaofei/consume/20060119/07102288409.shtml>

这不是本仓用来计算“精确 Web 渗透率”的数据，因为：

- 预约包括电话 / Web 等多渠道；
- 门急诊与预约统计口径并非完全同构；
- 预约量不是 Web-only numerator。

它能证明的只是：

> **1999 service availability did not make appointment the default hospital access mode by 2004.**

这是 `available ≠ used ≠ popular` 的直接案例。

---

# 7. 2008 Xi'an: contemporaneous reporter walkthrough

## 7.1 A concrete public-to-private-to-offline chain

2008-08-29《西安晚报》记者实际测试网上预约。

Source:

<https://www.chinanews.com.cn/jk/hyxw/news/2008/08-29/1365108.shtml>

报道中的一条成功路径：

```text
hospital website
→ doctor selection
→ time selection
→ name / identity / contact fields
→ submit
→ appointment confirmation number
→ hospital guide desk
→ physical appointment slip
→ cashier
→ department waiting
```

### Privacy note

同期报道公开过一个具体预约号。

本仓**不需要重新复制这个号码**：

- 对研究流程无必要；
- 只保留“系统生成预约编号”这一功能事实。

## 7.2 Same city, different technological topology

同一篇报道中：

- 另一家医院网站记者多次尝试未能顺利打开；
- 该院实际使用电话预约；
- 患者还需先到院凭身份证办理实名会员。

这说明：

```text
Hospital A: Web → offline check-in
Hospital B: offline enrollment → phone
Hospital C: possible walk-up
```

可以同时存在。

### Hard boundary

记者当时“网站打不开”只支持：

> **that access attempt failed**

不支持：

- 网站长期宕机；
- IE / Firefox 不兼容；
- DNS permanently failed；
- server architecture claim。

Browser/runtime cause remains **unknown**。

---

# 8. 2009 policy: appointment becomes an institutional requirement

## 8.1 Primary institutional source

卫生部 2009-09-30《关于在公立医院施行预约诊疗服务工作的意见》要求：

- 2009 年 11 月起所有公立三级医院开展预约诊疗；
- 二级医院逐步开展；
- 定期更新诊疗科目、专业和出诊时间；
- 推广实名预约；
- 推动分时段预约；
- 将预约与连续管理相联系。

Primary source:

<https://www.nhc.gov.cn/bgt/s9514/200909/d5b3893fff4747cdbf91154f5bf109c8.shtml>

Evidence grade: **A (institutional primary source)**.

## 8.2 Why this matters to Web archaeology

政策要求的是“医院预约制度”，不是“必须由 Web 完成”。

因此 2009 以后搜索历史站点时，必须区分：

```text
appointment service exists
vs
online appointment exists
vs
hospital-owned Web appointment exists
vs
third-party Web appointment exists
```

否则很容易把 telephone / window / doctor-workstation appointment 全误算成 Web。

---

# 9. 2009 Beijing: a live taxonomy of incompatible appointment interfaces

## 9.1 Reporter test

2009 年《北京晚报》记者对北京三级医院电话与网络预约做实际体验。

Sources:

<https://news.ifeng.com/mainland/200910/1029_17_1410577.shtml>

<https://news.ifeng.com/mainland/200910/1029_17_1410577_1.shtml>

## 9.2 Confirmed interface types

同期报道中至少能确认以下形态：

### Type A — hospital-owned registration / appointment

记者描述多家医院官网可以注册后预约。

### Type B — hospital page → third-party appointment provider

报道提到部分医院通过爱康等第三方完成预约。

Historical third-party URL named in the report:

`www.Ikang.com`

### Type C — separate inquiry / appointment site

报道提及：

`http://iask.mtzyy.com.cn/`

需注册、提交，等待管理员回复确认。

### Type D — hospital website + institutional email handoff

报道提及北京博爱医院历史网站：

`www.crrc.com.cn`

患者把预约所需信息发送到机构公开 Email，再等待邮件确认。

本仓不需要在正文复制具体患者信息，也不建议主动测试历史邮箱。

### Type E — offline card first, phone later

26 家医院表示首次电话预约需要先到医院办理预约卡。

### Type F — mobile-number verification

部分系统要求实名信息、患者 ID / 就诊卡和特定手机验证。

---

# 10. The appointment state machine

从 1999–2011 的证据可以建立最小状态机。

```text
1. institution exists
2. department listed
3. doctor listed
4. schedule published
5. slot inventory exposed
6. user has entitlement/account/card
7. user authenticated / identified
8. booking request submitted
9. backend accepts or rejects
10. confirmation delivered
11. user may cancel / reschedule
12. user travels
13. user checks in / exchanges token
14. payment succeeds
15. patient enters consultation queue
16. clinical encounter occurs
17. tests / prescription / follow-up may occur
18. future rebooking may be created
```

旧 Web archive 通常只能较好覆盖 1–4。

5–18 的保存率会迅速下降。

---

# 11. New gap model

## 11.1 schedule-version gap

医生页面保存下来，不等于某个历史日期的出诊表保存下来。

```text
current doctor profile
≠ historical schedule
```

尤其当页面永远渲染“当前排班”时，archive 可能发生 time collapse。

---

## 11.2 slot-state gap

这是本篇最核心的新 gap。

```text
schedule says doctor works Friday
≠ Friday had an available slot at 08:03 on Tuesday
```

号源是后台动态库存。

同一个 URL 在不同秒钟可能返回：

- 有号；
- 已满；
- 尚未放号；
- 已取消；
- 暂停预约。

archive 若只抓一次，不能代表整日状态。

---

## 11.3 release-time contention gap

2009 广州报道描述某热门专家网上号源在极短时间内被预约完。

Source:

<https://news.ifeng.com/society/2/200910/1012_344_1384067.shtml>

这意味着：

> **a static snapshot cannot reconstruct contention.**

即使 archive 在当天中午抓到“已满”，也不知道：

- 什么时候放号；
- 满用了几秒 / 几分钟；
- 有多少用户同时请求；
- 是否有 retry；
- 是否有 later cancellations。

---

## 11.4 account / entitlement gap

1999 一卡通、2008 实名会员、2009 就诊卡 / 患者 ID 都说明：

```text
public form reachable
≠ historical user was entitled to submit
```

账号状态通常是 private backend state。

---

## 11.5 identity-binding gap

实名预约会绑定：

- 姓名；
- 有效证件；
- 手机；
- 就诊卡 / patient ID。

这些数据不应该出现在公开 archive。

因此：

> **absence of historical booking records is often a correct privacy outcome, not an archival failure to “repair”.**

---

## 11.6 confirmation-channel gap

Web 请求以后，确认可能通过：

- 页面提示；
- Email；
- SMS；
- 电话；
- 管理员人工回复。

公开网页只保存 request surface，不保存 private confirmation。

所以：

```text
form submitted
≠ booking confirmed
```

---

## 11.7 third-party handoff gap

医院官网可能只承担：

```text
hospital page
→ link to third party
```

archive 可能只保存一边。

因此至少记录：

```yaml
origin_site: hospital
handoff_site: third-party
handoff_type: hyperlink | iframe | redirect | unknown
transaction_owner: third-party | hospital | unknown
```

不要因为医院 URL 幸存，就说预约 backend 也由医院所有。

---

## 11.8 offline-enrollment gap

有些系统必须：

```text
先去医院办卡
→ 回家打电话 / 上网
```

如果只研究 Web，会完全漏掉 eligibility step。

因此：

> **online execution can depend on a prior offline ceremony.**

---

## 11.9 check-in / token-exchange gap

2003 苏州、2008 西安都显示：

预约成功后还需到院：

- 取号；
- 换票；
- 缴费；
- 签到。

所以：

```text
reservation token
≠ final queue position
≠ consultation
```

---

## 11.10 no-show / cancellation gap

Web 可以保存“可取消预约”功能说明，但某个人：

- 是否取消；
- 是否爽约；
- 是否被列入限制；

属于 private account state。

因此历史爽约率必须使用机构统计或同时代研究，不能从 archive 单页推断。

---

## 11.11 clinical-execution privacy gap

真正的诊疗结果通常包括：

- 病历；
- 检查；
- 处方；
- 诊断；
- 后续安排。

这类内容天然敏感。

本仓明确停止于：

```text
public service interface
→ appointment execution boundary
```

不以“考古完整”为理由寻找私人医疗记录。

---

# 12. 2009: scarce capacity vs broken interface

研究旧预约网站时必须区分三种失败：

## A. interface failure

例如：

- 页面打不开；
- 表单错误；
- 请求失败。

## B. entitlement failure

例如：

- 没有预约卡；
- 未实名；
- 手机不匹配。

## C. capacity failure

例如：

- 页面正常；
- 账号正常；
- 但没有号。

三者在用户体验上都可能是“挂不上”。

但历史解释完全不同。

因此：

> **“挂不上” ≠ “网站坏了”**

---

# 13. 2010: appointment confirmation can change intercity movement

2010 年报道记录，一名天津患者中午到北京后凭已预约凭证取得专家号。

Source:

<https://news.sohu.com/20100118/n269657328.shtml>

old-Web 侧不研究这名患者的疾病。

我们只记录一个 execution fact：

> **remote confirmation could precede intercity travel.**

这意味着预约页面是 mobility infrastructure 的一部分。

但 archive 通常只会留下“预约网站”，不会留下：

- 用户之后是否买票；
- 何时抵达；
- 是否住店；
- 是否真正看诊。

可命名：

## mobility-outcome gap

```text
booking success
≠ travel occurred
```

---

# 14. 2011 Beijing unified platform: platform genealogy boundary

## 14.1 Why unification happened

北京市卫生部门 2011 年说明：此前各医院的预约电话、网址不同，给用户记忆和使用造成困难，因此建设面向全体患者的统一预约平台，统一电话和网络入口并统筹号源数据。

Source:

<https://wjw.beijing.gov.cn/xwzx_20031/wnxw/201912/t20191214_1174492.html>

同期报道：

<https://news.sina.com.cn/c/2011-07-27/151122886816.shtml>

Historical domain reported:

`www.bjguahao.gov.cn`

## 14.2 Archaeological transition

这不是简单“新网站替代旧网站”。

更像：

```text
many hospital-specific front doors
        ↓
unified city-level discovery / booking front door
        ↓
hospital-specific clinical backends remain
```

因此统一平台形成一个新的 **platform genealogy**：

- 用户入口所有权；
- 号源数据来源；
- 医院自身网站；
- 电话入口；
- 后台临床系统

不再是同一个 ownership layer。

---

# 15. URL / host inventory from this round

> 仅列同时代报道明确点名的公开机构 / 服务 URL；不保证当前仍存在，不主动测试私人账号。

| Approx. date | Reported URL / host | Role | Evidence | Current reconstruction status |
|---|---|---|---|---|
| 2003 | `www.sdfyy.cn` | 苏大附一院网站 / 网上预约入口 | B contemporaneous report | historical capture not retrieved this round |
| 2009 | `www.Ikang.com` | third-party reservation handoff in reporter test | B | exact historical booking path not reconstructed |
| 2009 | `iask.mtzyy.com.cn` | registration + administrator confirmation flow | B | dynamic account state unavailable |
| 2009 | `www.crrc.com.cn` | hospital site; email-based appointment instructions reported | B | exact page capture not retrieved |
| 2011 | `www.bjguahao.gov.cn` | Beijing unified appointment platform | A/B institutional + contemporaneous media | historical platform capture not retrieved this round |

### Important

Do not infer from host survival today that:

- ownership is unchanged；
- same service is running；
- same URL path exists；
- historical data survived。

---

# 16. Browser / runtime contract

## 16.1 What we know

本轮证据明确说明：

- 2008 有记者遇到医院网站多次无法打开；
- 2003 / 2009 流程包含动态注册、提交和查询；
- 预约后台必然依赖 server-side state。

## 16.2 What we do NOT know

本轮没有足够 capture / manual 支持以下具体说法：

- IE5 / IE6 required；
- ActiveX required；
- Java applet required；
- GB2312 / GBK exact charset；
- frameset；
- ASP / JSP / PHP implementation；
- cookie names；
- HTTP method；
- CAPTCHA technology。

因此这些全部保持 **unknown**。

## 16.3 Minimal future experiment

如果以后找到 2003 / 2009 capture，建议记录：

```yaml
capture_url:
original_url:
capture_datetime:
status_code:
charset_declared:
charset_observed:
form_action:
method:
script_dependencies:
external_hosts:
cookie_dependency:
login_required:
missing_assets:
modern_chromium_result:
legacy_browser_assumption:
```

不要为了“能点”而生成假的后端响应。

---

# 17. Historical result-page contract

预约网站特别容易发生一种误读：

> 页面上有“医生 A 周五出诊”，研究者就以为周五可以约医生 A。

实际上至少要拆：

```text
doctor exists
→ doctor scheduled
→ schedule published
→ quota allocated to this channel
→ quota released
→ slot still available
→ user eligible
→ request accepted
```

因此任何 archive note 最少要明确：

```yaml
claim_type: doctor-listing | schedule | slot-availability | booking-success
observed_at:
channel:
confidence:
```

不要把不同 claim_type 合并。

---

# 18. Evidence table

## A-level

### A1. 2009 Ministry of Health appointment policy

<https://www.nhc.gov.cn/bgt/s9514/200909/d5b3893fff4747cdbf91154f5bf109c8.shtml>

Supports:

- appointment service institutionalisation；
- schedule updating；
- real-name / timed appointment policy direction。

Does NOT prove:

- a specific hospital Web implementation；
- a specific historical slot。

### A2. 2011 Beijing health authority platform statement

<https://wjw.beijing.gov.cn/xwzx_20031/wnxw/201912/t20191214_1174492.html>

Supports:

- hospital-specific URL/phone fragmentation as a stated problem；
- unified platform intent and 114 role。

---

## B-level

### B1. 2003 Suzhou online appointment workflow

<https://news.sina.com.cn/o/2003-08-02/1058491035s.shtml>

### B2. 2006 Beijing appointment retrospective with 2004 volumes

<https://finance.sina.com.cn/xiaofei/consume/20060119/07102288409.shtml>

### B3. 2008 Xi'an reporter execution test

<https://www.chinanews.com.cn/jk/hyxw/news/2008/08-29/1365108.shtml>

### B4. 2009 Beijing multi-hospital reporter test

<https://news.ifeng.com/mainland/200910/1029_17_1410577.shtml>

<https://news.ifeng.com/mainland/200910/1029_17_1410577_1.shtml>

### B5. 2009 Guangzhou slot contention

<https://news.ifeng.com/society/2/200910/1012_344_1384067.shtml>

### B6. 2010 patient appointment / intercity execution

<https://news.sohu.com/20100118/n269657328.shtml>

### B7. 2011 unified-platform launch reporting

<https://news.sina.com.cn/c/2011-07-27/151122886816.shtml>

---

## C / B boundary source

北京日报 2020 历史专题，引用本报 1953 / 1954 / 1993 / 1999 原始报道定位：

<https://k.sina.cn/article_1893892941_70e2834d02000ryrc.html>

Use only as prehistory / archive lead until original pages are retrieved.

---

# 19. Counterexamples

## 19.1 A page can work while no slot exists

因此：

> “预约失败”不能自动记为 website failure。

## 19.2 A slot can be reserved while visit never happens

可能：

- cancel；
- no-show；
- wrong identity；
- travel disruption；
- doctor schedule change。

## 19.3 A hospital can offer appointment without Web

电话、现场、诊间都属于预约渠道。

## 19.4 A hospital can have a Web page but delegate transaction elsewhere

因此：

> `page ownership ≠ transaction ownership`。

## 19.5 Unified platform does not imply unified clinical backend

统一入口可以存在，而医院内部：

- payment；
- EMR；
- check-in；
- tests

仍各自运行。

---

# 20. Privacy stop conditions

医院预约考古必须比普通商业页面更严格。

Stop immediately if reconstruction would require：

- patient account credentials；
- leaked appointment database；
- historical ID numbers；
- private SMS / email obtained without clear consent；
- medical records；
- diagnosis or test results of ordinary individuals；
- resurrecting deleted patient posts unnecessarily。

Allowed / preferred：

- institutional manuals；
- public service guides；
- public screenshots with no sensitive data；
- contemporaneous newspaper walkthroughs；
- policy documents；
- archive metadata；
- anonymised aggregate statistics。

---

# 21. Hindsight risks

## 21.1 Do not project WeChat/App logic backward

2003 Web flow may have had none of today’s：

- QR login；
- mobile payment；
- push notification；
- persistent app identity。

Do not describe it with current UI metaphors unless quoting contemporaneous language.

## 21.2 Do not treat “网上预约” as end-to-end online care

2003 / 2008 evidence clearly shows offline payment / token exchange / hospital waiting remained.

## 21.3 Do not treat 1999 as mass household use

Online appointment existed, but Internet household access and service adoption were still limited.

## 21.4 Do not infer historical availability from a doctor profile surviving today

Profiles and schedules are mutable.

## 21.5 Do not infer browser requirements without capture/manual evidence

A reporter’s failed page load is not enough.

---

# 22. What this changes in the repository’s archive-gap model

Before this case, many transaction-like notes focused on：

```text
listing / form
→ private handoff
→ outcome disappears
```

Hospital appointment adds something sharper：

> **the public result itself is a rapidly changing inventory state.**

For classifieds, the listing may survive for hours/days.

For appointment systems, the historically meaningful state may last seconds.

So archive missingness is not just “private transaction after public page”. It is also：

```text
public page
+ private account
+ high-frequency mutable inventory
+ anti-abuse state
+ offline execution
```

This should eventually become a reusable `dynamic-inventory` gap class for：

- appointments；
- tickets；
- reservations；
- application quotas；
- limited registration slots。

---

# 23. Confirmed / probable / unknown

## Confirmed

- 1999 Beijing hybrid card + phone/Web appointment system existed;
- 2003 Suzhou online reservation supported doctor/date selection and offline payment/collection;
- 2008 Xi'an reporter successfully executed a Web-to-offline appointment path;
- 2009 hospitals used materially different Web/phone/card/email workflows;
- 2009 national policy pushed appointment service across tertiary public hospitals;
- 2011 Beijing unified phone/Web entry was launched to reduce fragmented interfaces.

## Probable but not fully reconstructed

- historical Web pages depended on session/backend state beyond what static capture could preserve;
- many doctor/schedule pages were dynamically generated or database-backed;
- later captures may time-collapse historical schedules.

## Unknown

- 1999 Beijing page DOM and original URL in this run;
- exact browser/OS requirements for 1999/2003 systems;
- exact charset/script stack;
- exact historical slot API or backend schema;
- how much of each old service was captured by Internet Archive/Common Crawl;
- whether any complete authenticated transaction can be ethically reconstructed without private data.

---

# 24. Next high-value artifact work

Priority is not another newspaper quote.

The strongest next slice would be one **publicly archived, privacy-safe appointment interface across at least two timestamps**, ideally：

```text
2003–2005 hospital homepage
→ doctor/schedule page
→ appointment form or instruction page
→ later revision
```

For each capture, record：

- original URL；
- capture datetime；
- links；
- form action if preserved；
- static vs dynamic elements；
- charset；
- missing scripts/images；
- whether the form can be rendered without submitting；
- whether the historical backend is gone；
- what state cannot be recovered。

Candidate leads from contemporaneous reports：

- `www.sdfyy.cn`；
- `iask.mtzyy.com.cn`；
- `www.crrc.com.cn`；
- `www.bjguahao.gov.cn`。

Do **not** log in or attempt to resurrect historical patient accounts.

---

# 25. Saturation note

This slice adds a genuinely new archive mechanism：

1. **slot-state gap**；
2. **release-time contention gap**；
3. **entitlement-artifact gap**；
4. **confirmation-channel gap**；
5. **offline-enrollment gap**；
6. **check-in/token-exchange gap**；
7. **clinical-execution privacy gap**；
8. **dynamic inventory as a high-frequency public-but-ephemeral state**。

Therefore this is **not** a no-new-evidence run and does not contribute to the 3-run saturation counter.

---

# Sources

## Chinese appointment / old-Web evidence

- 北京日报历史资料整理（1953 / 1954 / 1993 / 1999）：<https://k.sina.cn/article_1893892941_70e2834d02000ryrc.html>
- 北京预约一卡通 / 2004 appointment volume：<https://finance.sina.com.cn/xiaofei/consume/20060119/07102288409.shtml>
- 2003 苏州网上预约：<https://news.sina.com.cn/o/2003-08-02/1058491035s.shtml>
- 2008 西安记者实际预约：<https://www.chinanews.com.cn/jk/hyxw/news/2008/08-29/1365108.shtml>
- 2009 卫生部预约诊疗政策：<https://www.nhc.gov.cn/bgt/s9514/200909/d5b3893fff4747cdbf91154f5bf109c8.shtml>
- 2009 北京多医院电话 / Web 实测：<https://news.ifeng.com/mainland/200910/1029_17_1410577.shtml>
- 2009 北京实测续页：<https://news.ifeng.com/mainland/200910/1029_17_1410577_1.shtml>
- 2009 广州专家号网上竞争：<https://news.ifeng.com/society/2/200910/1012_344_1384067.shtml>
- 2010 北京预约挂号患者执行：<https://news.sohu.com/20100118/n269657328.shtml>
- 2011 北京统一平台说明：<https://wjw.beijing.gov.cn/xwzx_20031/wnxw/201912/t20191214_1174492.html>
- 2011 统一平台启动同期报道：<https://news.sina.com.cn/c/2011-07-27/151122886816.shtml>

## Cross-repo overseas comparison (kept mainly in how-people-lived)

- 1987 France Minitel / SANTAL health information：<https://www.lemonde.fr/archives/article/1987/03/26/la-sante-par-l-ecran-le-service-telematique-de-chambery-permet-aux-hemophiles-de-traiter-a-domicile-leur-maladie_4052128_1819218.html>
- 1999 NHS Direct telephone → Web expansion：<https://www.independent.co.uk/news/selfhelp-nhs-care-on-the-net-expanded-1131037.html>
- NHS Direct historical / academic overview：<https://www.cambridge.org/core/journals/psychiatric-bulletin/article/nhs-direct-a-telephone-helpline-for-england-and-wales/65028FFC4E4AC232DA509F3FFE83FE3F>
