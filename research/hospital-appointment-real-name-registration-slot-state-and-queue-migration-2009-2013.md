# 医院预约挂号：实名注册、号源状态与排队迁移，2009–2013

> 状态：research note，不构成 M1 完整案例
>
> 范围：2009–2013 年中文 Web 医疗预约挂号及其与电话、医院后台和实名身份链的关系。
>
> 交叉主题：普通生活史中的 `care-slot access / 就医时隙访问`、等待劳动和未来日历化。

## 0. 为什么这是 old-web archaeology，而不只是医疗史

2009–2013 年医院预约挂号把一种原本主要发生在医院窗口和电话线路上的稀缺资源——某天、某科、某位医生的一次门诊机会——逐步做成了 Web 可以查询、预约和确认的状态。

但对考古者来说，网页恰恰只保存了最容易看见的一层。真正决定事务结果的还有：

- 某一时刻的实时号源库存；
- 电话渠道与 Web 渠道是否共享同一库存；
- 某个号是否已经被临时占用；
- 实名身份与手机号是否验证通过；
- 预约是否取消、爽约或兑现；
- 患者最终是否到院就诊。

因此本案例适合把 OWA 的 `page / capture / claim` 方法推进到**动态事务状态**。

---

## 1. 研究单位

本条目至少区分以下对象：

1. **hospital / institution**：医院本身；
2. **platform**：医院自有预约系统、北京市统一预约挂号平台；
3. **web page**：医院列表、科室页、医生页、预约须知、注册页；
4. **user account / identity record**：实名、身份证号、手机号、短信验证状态；
5. **doctor schedule**：医生某日是否出诊；
6. **slot inventory**：某日某医生/科室剩余号源；
7. **reservation order**：一次具体预约记录；
8. **confirmation artifact**：预约序列号、短信等；
9. **phone-channel transaction**：114 等电话渠道产生的预约；
10. **care event**：患者最终是否到院并接受诊疗；
11. **archive capture**：Web archive 保存的页面表示。

这些对象不能互相替代。

尤其：

```text
页面显示“有号”
!=
capture 时后台一定仍有可预约库存

预约记录存在
!=
患者最终接受了诊疗
```

---

## 2. 2009：Web 预约并不是单线替代电话和窗口

2009 年 9 月，北京朝阳医院开通网上预约挂号。同期公开材料显示，该院此前已有约 13 年电话预约经验；新系统上线后，电话、网络、窗口、复诊和社区预约长期并存。网络预约可以 24 小时提交，而电话、窗口仍有自己的服务时段。

来源：

- 北京卫生局 / 新浪转载，2009-09-07：<https://news.sina.com.cn/c/2009-09-07/112616254859s.shtml>

这条材料支持一个窄结论：

> 2009 年部分北京大医院已经把同一个门诊访问问题暴露给多个入口，而不是从“窗口时代”直接切换成“Web 时代”。

证据等级：**A/B，高置信**（官方系统信息由新闻转载保存）。

### 2.1 远程预约可能仍要求先完成线下 enrollment

2009 年 8 月《健康时报》的调查称，北京一些医院的电话预约要先去医院办理预约卡；朝阳医院当时的一种流程要求患者先到挂号处购买并登记“门诊电话预约卡”，之后才能使用电话预约。

来源：

- 健康时报，2009-08-31（新浪转载）：<https://news.sina.com.cn/h/2009-08-31/113318547636.shtml>

因此历史界面研究不能只问“是否有远程入口”，还要问：

**这个入口是不是 first-contact executable？**

也就是，一个第一次来的患者能否不经过此前的线下建档，就完成第一次预约。

---

## 3. 2009：官方制度把实名和预约优先写进公共医院流程

卫生部 2009 年 9 月 30 日《关于在公立医院施行预约诊疗服务工作的意见》要求从 2009 年 11 月起公立三级医院开展预约诊疗，逐步扩展到二级医院；文件要求预约和就诊使用本人身份证等有效证件，并强调预约优先、更新科室和医生出诊信息。

来源：

- 卫生部，2009-09-30：<https://www.nhc.gov.cn/bgt/s9514/200909/d5b3893fff4747cdbf91154f5bf109c8.shtml>

这意味着 old-Web 上的预约页面已经不是普通“信息页”。

它属于一个需要与身份、医生排班、医院业务系统和最终就诊动作联动的**制度事务界面**。

证据等级：**A，高置信**。

---

## 4. 2011：北京统一预约平台把多个医院暴露给同一个入口

2011 年 7 月 28 日，北京市预约挂号统一平台开始试运行。官方和同期报道给出的入口包括：

- 电话：`114`；
- Web：`www.bjguahao.gov.cn`。

首批接入医院通过统一入口提供普通号、专科号和专家号预约，多数医院可预约未来约三个月的号源。

来源：

- 卫生部，2011-07-29：<https://www.nhc.gov.cn/tigs/s10008/201107/4a703577b5264f19b49c04f84edd5249.shtml>
- 北京卫生局历史页面，2011-06-21：<https://wjw.beijing.gov.cn/xwzx_20031/wnxw/201912/t20191214_1174492.html>
- 北京晚报，2011-07-28（新浪保存）：<https://news.sina.com.cn/c/2011-07-28/152422894135.shtml>

### 4.1 已确认的历史 locator

2011 年三博脑科医院的一份官方新闻仍保留了当时的具体 URL：

- `http://www.bjguahao.gov.cn/comm/index.php`
- `http://www.bjguahao.gov.cn/comm/yyxz.php?hpid=124`

来源：

- 三博脑科医院，2011-09-19：<https://www.sbnk.cn/Html/News/Articles/100938.html>

这些 URL 目前只能记为 **historical locator**。

本轮没有取得已经实际打开并核验过 `capture_datetime / historical HTTP / DOM / charset / subresources` 的 2011 memento，因此不能称为 historical capture。

---

## 5. 同一个“排队”开始从大厅迁到电话和 Web

2011 年统一平台上线后的同期体验报道显示，热门专家号仍可能迅速约满；有用户从凌晨开始等待电话系统到放号时刻，也有老人反复拨打 114。

来源：

- 京华时报，2011-08-04（新浪保存）：<https://news.sina.com.cn/c/sd/2011-08-04/033422930416.shtml>

所以平台考古不能把：

```text
医院大厅里没有一条长队
```

等同于：

```text
排队已经消失
```

更准确的模型是：

**`queue migration / 排队迁移`**

```text
窗口前的身体队列
→ 电话占线 / 呼叫队列
→ 固定放号时刻
→ 浏览器刷新 / Web 提交竞争
```

这类等待通常不会被 Web archive 直接保存。

一个页面即使被完整 capture，也不会告诉我们：

- 当时电话线路有多少人在等；
- 某个专家号在几秒前是否已经被另一渠道占走；
- 用户提交以后后台返回了什么瞬时状态。

---

## 6. `slot-state invisibility / 号源状态不可见于静态档案`

门诊号源是一个典型的**高频变化服务器端状态**。

可以把它抽象成：

```text
future doctor schedule
→ slots generated
→ slots allocated to channels
→ visible availability
→ reservation attempt
→ success / failure
→ cancellation / release
→ no-show / attendance
```

静态 HTML/WARC 最多可能保存其中某个时刻的表示。

因此：

**`captured availability representation != preserved inventory state`**

即使 archive 保存了一页写着“可预约”，也不能直接证明 capture 时这张号仍然能被真实用户成功提交；页面可能存在缓存、archive rewrite、异步接口失效或后端状态已经变化。

本条目把这一考古缺口命名为：

**`slot-state invisibility`**。

它比泛泛的 `page != transaction` 更具体，因为可以明确列出未来需要恢复的状态机。

---

## 7. `channel-converged inventory / 多渠道汇入同一稀缺库存`

北京统一平台从设计上同时暴露 114 和 Web；部分医院又保留自身窗口、复诊和社区渠道。

这带来一个重要方法问题：

**一个前端的 capture 不能代表整个号源系统。**

研究时至少要问：

- Web 与 114 是否使用同一号源池；
- 医院是否给不同渠道分配固定比例；
- 某些复诊/社区号源是否根本不向 Web 暴露；
- 取消后号源是否重新进入所有渠道；
- 平台显示的“满”是全院无号，还是仅该渠道无号。

这可以称为：

**`channel-converged inventory / 多渠道汇入同一稀缺库存`**。

它提醒考古者：前端页面数量和真实可访问容量之间没有简单一一对应关系。

---

## 8. 2013 技术论文留下了实名注册链的字段级证据

2013 年，中国联通系统研究人员发表 *A Two Factor User Authentication Scheme for Medical Registration Platform*，描述北京医疗预约平台的注册/认证流程。

论文称，首次使用时用户需要提供包括：

- real name；
- gender；
- age；
- mobile phone number；
- ID card number；

并使用发送至手机号的短信验证码完成注册确认。

来源：

- Atlantis Press：<https://www.atlantis-press.com/proceedings/iccsee-13/4763>
- DOI：<https://doi.org/10.2991/iccsee.2013.332>

论文还指出当时认证流程存在不足，并提出更强的 SMS-OTP 双因素方案。

证据等级：**B，中高置信**。

理由：它是同时代技术论文，作者机构与电信系统相关，可以很好地证明作者观察/描述的字段和认证问题；但它不是平台官方生产系统完整手册，所以不把所有实现细节升级为 A 级。

### 8.1 `identity-binding state / 身份绑定状态`

这组材料说明一个预约订单不是匿名购物车。

它至少涉及：

```text
person identity
+ ID number
+ mobile number
+ verification code
+ hospital / department / doctor
+ appointment date
+ reservation order
```

因此历史页面中的“注册成功”“预约成功”依赖大量 archive 通常不会保存的后台身份状态。

出于隐私原则，本仓若未来取得普通患者页面/邮件/短信遗留物，应优先记录**字段类型和流程**，而不是重新公开真实身份证号、手机号或预约序列号。

---

## 9. `appointment-state != care-event`

即使以后取得真实历史预约确认页，它能证明的也只是：

> 某个系统曾表示一次预约成立。

它不能单独证明：

- 患者真的去了医院；
- 医生当天没有停诊；
- 患者按时取号；
- 最终见到了该医生；
- 完成了诊疗。

因此本案例必须把 `reservation order` 与 `care event` 分开。

这是医疗类 old-Web artifact 和普通静态内容页最根本的差异之一。

---

## 10. 浏览器与运行环境：现在能证明什么，不能证明什么

本轮材料足以确认 2009–2013 有 Web 预约、实名注册、短信确认和多渠道号源。

但本轮**没有得到足够证据**去断言：

- `bjguahao.gov.cn` 必须使用 IE6/IE7；
- 是否依赖 ActiveX；
- 当时主页面 charset；
- JS 框架；
- 预约提交是否使用 AJAX；
- 登录 cookie/session 机制；
- 短信接口协议；
- 与医院 HIS 的具体 API。

因此不写“典型 IE-only 政务站”之类凭时代印象作出的推断。

后续 M3 如要做浏览器复原，应先取得真实 historical capture 或同时代技术文档，再决定 IE / Firefox / charset 实验。

---

## 11. artifact probe：本轮得到和没得到什么

### 已得到

- 2009 卫生部预约诊疗官方制度原文；
- 2009 北京医院多渠道预约的同期流程描述；
- 2011 统一平台官方上线资料；
- `bjguahao.gov.cn` 历史域名；
- 两个 2011 具体 URL locator；
- 2011 同期用户/记者对电话等待和热门号源稀缺的观察；
- 2013 同时代技术论文的注册字段和短信确认描述。

### 本轮没有得到

- 一个已经实际打开并核验的 2009–2013 Wayback/Memento capture；
- capture datetime；
- historical HTTP/replay state；
- 原始 DOM / CSS / JS；
- charset；
- 子资源完整性；
- 页面在历史浏览器中的实际表现；
- 服务器端号源库存记录；
- 原始短信网关或 HIS 接口文档。

本轮曾继续搜索 `bjguahao.gov.cn` 和具体路径的 archive locator，但没有取得可以实际打开核验的 memento；在本轮运行环境中进一步尝试 archive CDX 路径时也遇到访问/DNS限制。

因此这里只能写：

**`no verified historical capture obtained in this run`**

不能写：

**`Wayback did not preserve the site`**。

后者是没有证据的负结论。

---

## 12. OWA 方法上的新增点

### 12.1 页面保存成功，最关键的历史状态仍可能全部丢失

医疗预约的真正稀缺物不是 HTML，而是某个未来时刻的 slot。

即使页面、CSS、logo、医生简介全部保存，也可能完全不知道当时：

- 还有几张号；
- 谁正在提交；
- 电话端是否刚拿走最后一个；
- 订单是否成功；
- 之后是否取消。

### 12.2 “数字化”会改变 archive 的可见偏差

窗口时代的等待通常只能从新闻、日记、照片恢复；Web 时代留下更多页面，却可能让研究者误以为 Web 本身就是完整制度。

实际上真正的服务仍横跨：

```text
Web
+ call centre
+ SMS
+ hospital backend
+ ID database
+ physical clinic
```

### 12.3 越成功的事务越可能越难被公开 archive 保存

实名预约确认页通常需要登录，并且含个人敏感状态；archive 本来就不应完整公开保存这类内容。

因此“没有公开用户订单页”不能简单解释为平台没有真实使用。

这一点和公开个人主页的 archive 逻辑完全不同。

---

## 13. Evidence table

| Claim | Source | Family | Grade | Confidence | Limits |
|---|---|---|---|---|---|
| 2009 朝阳医院已有约 13 年电话预约并新增 Web 渠道 | 北京卫生局/新浪 | official/reprint | A/B | high | 不能推断全北京使用率 |
| 2009 公立三级医院应开展预约并实名 | 卫生部文件 | official | A | high | 不证明各院实际成熟度 |
| 2011 北京统一平台由 114 + Web 提供预约 | 卫生部/北京市卫生系统 | official | A | high | 不证明所有渠道库存完全一致 |
| `bjguahao.gov.cn/comm/...` URL 当时被医院使用 | 三博脑科医院 2011 新闻 | official hospital | A/B | high | locator，不是 capture |
| 热门号源上线后仍出现电话等待和迅速约满 | 京华时报同期体验 | contemporaneous media | B | high | 不能外推全部医院 |
| 2013 注册含实名、身份证、手机号、短信确认 | ICCSEE 技术论文 | contemporaneous technical paper | B | medium-high | 非官方完整生产手册 |
| 当前已取得 2011 historical memento | 本轮 probe | — | — | **NO** | 未实际打开核验 |

---

## 14. 已证实 / 高概率 / 不知道

### 已证实

- 2009–2011 北京医院预约入口从医院自有电话/Web进一步进入统一 114 + Web 平台；
- 实名身份是预约制度的重要组成；
- 2011 有明确的 `bjguahao.gov.cn` 历史 URL；
- 多渠道长期并存；
- 热门专家号源稀缺没有因 Web 出现而自动消失；
- 2013 同时代技术材料描述了实名、身份证、手机号和短信确认链。

### 高概率但仍需更多技术证据

- Web 与 114 在平台层面至少共享部分统一调度的号源资源；
- 平台前端依赖医院侧动态排班/号源同步；
- 大部分最重要的实时状态属于服务器端，普通 archive capture 很难完整保存。

### 不知道

- 2011 网站真实 DOM、charset 和浏览器兼容矩阵；
- 每家医院如何把号源比例具体分给 Web / 114 / 窗口 / 社区；
- 预约提交是否有临时锁、锁多久；
- SMS、统一平台和 HIS 的生产接口协议；
- 目前 archives 是否其实存在可用 memento，只是本轮访问路径没有取得；
- 两个以上可以完整比较的历史 capture 时点。

---

## 15. 与 how-people-lived 的交叉

对应 HPL：

`sources/from-overnight-queue-to-real-name-appointment-care-slot-access-and-waiting-labor-china-1996-2026.zh-CN.md`

HPL 关心的是：

- 一个患者怎样取得一次未来门诊机会；
- 排队劳动怎样从身体搬到电话/Web/App；
- 异地患者如何把医疗安排进火车、请假和家庭照护日历；
- 老年人怎样依赖人工/电话/家属代理 fallback。

OWA 关心的则是：

- 这些生活动作在 Web 上留下了什么；
- 哪些关键服务器端状态没有被 capture；
- 身份、短信和电话渠道怎样越过单一页面边界；
- 怎样避免把“历史页面被保存”写成“历史事务被保存”。

---

## 16. M1 与饱和判断

这一案例目前状态：

```text
historical entity identity: achieved
historical domain/URL locators: achieved
contemporaneous workflow evidence: achieved
identity-field evidence: achieved
multi-channel model: achieved
verified historical memento: NOT achieved
second verified historical timepoint: NOT achieved
historical browser/runtime verification: NOT achieved
```

因此：

**M1 hospital-appointment case: NOT ACHIEVED**。

这轮并不是给已有 `page != transaction` 换名字。`slot-state invisibility`、`channel-converged inventory` 和 `queue migration` 给出了可以以后用真实 capture、历史接口文档和浏览器实验检验的具体状态模型。

同时 HPL 侧也新增了独立的制度接口：疾病发生以后如何取得、锁定并兑现一个未来 care slot。

因此本轮不计入连续无实质新增，阶段饱和计数保持 **0/3**。

---

*初稿由 AI 辅助整理。涉及普通患者个人身份材料时遵守研究必要最小化，不重新公开身份证号、手机号、预约序列号等历史敏感字段。*
