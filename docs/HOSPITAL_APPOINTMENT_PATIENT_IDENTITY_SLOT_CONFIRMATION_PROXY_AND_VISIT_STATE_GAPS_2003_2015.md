# Hospital appointment / patient identity / slot / confirmation / proxy / visit state gaps（2003—2015）

## 0. Scope

本 note 研究约 2003—2015 年中文 Web 中医院网上预约、城市统一预约平台和与之相邻的电话/窗口流程，重点不是证明“某医院很早就能网上挂号”，而是回答：**历史网页究竟能证明一次医疗事务的哪一段，哪些关键状态从设计上就不会被公开 Web archive 保存。**

仓库主 scope 仍然是约 1995—2015 中文互联网。本文件不会把 1980s 医院排队史、2020s 手机医疗或全球远程医疗史扩进 old-web 主体；这些只在交叉项目 `how-people-lived` 中作为生活史前史/后史。本文件需要的前史只保留一个边界：预约数字化以前，号源和身份核验主要发生在医院现场，因此 Web 的历史意义必须和线下闭环一起解释。

交叉专题：

- `how-people-lived/topics/from-queueing-for-a-number-to-proxy-booking-hospital-access-care-navigation-and-non-co-resident-caregiving-china-1980s-2026.zh-CN.md`

---

## 1. Research unit：绝不能把这些对象混成一个“挂号页面”

至少拆开：

1. **hospital / institution**：现实医院；
2. **hospital site / host**：医院公开网站，例如 `www.sdfyy.cn`；
3. **department / doctor directory**：科室和医生公开信息；
4. **appointment entry page**：预约入口、帮助页或表单壳；
5. **patient identity**：实际就诊人；
6. **account / registration identity**：平台注册身份；
7. **keyboard / phone operator**：实际操作网页或拨电话的人；
8. **proxy / guardian**：家长、成年子女、亲友、家庭医生等代理人；
9. **slot pool**：真实可预约号源；
10. **query result**：某个时间点返回给用户的号源结果；
11. **booking request**：用户提交的预约请求；
12. **slot lock / successful reservation**：后台真正锁定的号；
13. **confirmation artifact**：预约序列号、识别码、短信等；
14. **on-site pickup / check-in**：就诊当天取号、付费、签到；
15. **actual clinical encounter**：患者真的见到医生；
16. **follow-up transaction**：检查、缴费、取药、报告、复诊。

最低状态链：

`site exists` ≠ `appointment feature exists` ≠ `appointment page reachable` ≠ `patient registered` ≠ `operator is patient` ≠ `live slot visible` ≠ `request submitted` ≠ `slot locked` ≠ `confirmation delivered` ≠ `on-site pickup completed` ≠ `doctor actually saw patient`。

对家庭代理还必须再拆：

`account owner` ≠ `patient` ≠ `parent/guardian` ≠ `person holding the phone` ≠ `person who later appears at hospital`。

---

## 2. Evidence baseline

### A/B/C/D 规则

沿用仓库 `docs/METHOD.md`：

- **A**：历史 capture、同期官方公告/帮助、同时代软件/技术记录；
- **B**：同期媒体、用户教程、技术讨论；
- **C**：后来回忆；
- **D**：研究者推断。

本轮最重要的限制是：找到了若干 **exact historical original host**，但没有取得一份已经实际打开、能够完成 M1 最低检查的 2003—2015 预约交易 capture。因此本文件是 **state-gap research note**，不是完整 case。

### Exact historical hosts / locators

目前由同时代材料直接支持：

- `http://www.sdfyy.cn/` — 2003 年苏州大学附属第一医院网上预约入口所属医院站；
- `http://www.zryhyy.com.cn/` — 2010 年中日友好医院网络预约入口所属医院站；
- `http://www.bjguahao.gov.cn/` — 2011 年起北京统一预约挂号网络入口；
- 2015 年北京 114 微信预约已经出现，但其公众号内页面不是传统公开 Web URL，不能按普通网页 capture 逻辑处理。

这些 URL 是历史 locator，不等于本轮已经验证了对应 archive capture。

---

## 3. 2003：早期网上预约已经是动态事务，而不是静态医院主页

2003 年 8 月的同期报道记录，苏州大学附属第一医院通过 `www.sdfyy.cn` 推出网上预约：首次注册后，患者可查询科室、专家和出诊信息，选择科室、日期与医师；系统返回号数，预约人数超过名额时会提示改选时间；预约成功后可在线查询/取消。

但患者仍必须在就诊当天到医院指定窗口**付费取号**。医院当时实行提前两天预约，并把前五位号留给网上预约者。

来源：
- 江南时报/人民网同期报道（新浪转载），2003-08-02：https://news.sina.com.cn/o/2003-08-02/1058491035s.shtml

**证据等级：B+。**

### 能证明什么

- 2003-08-01 左右，该院对外提供了网上预约功能；
- 同期公开报道给出 exact host `www.sdfyy.cn`；
- 预约涉及注册、动态名额判断、预约号数返回、查询和取消；
- 网上预约并不完成付费与最终现场取号。

### 不能证明什么

- 预约页面的具体 URL pattern；
- 是否使用 GET/POST；
- session/cookie 实现；
- charset；
- HTML/frameset/table 布局；
- 浏览器是否 IE-only；
- JavaScript/ActiveX 是否参与；
- “前五个号”在后台如何保留；
- 某一天某位专家究竟还剩几个号；
- 注册账户和患者现实身份如何校验。

这些全部保持 **UNKNOWN**。

### 首个关键 archive gap

**booking-form survival / live-slot-state loss**

即使未来找到完整 HTML，静态表单也不能重建 2003 年 8 月某天 9:15 的实时号源。号源是后台瞬时状态，不是页面固定内容。

---

## 4. 2009：Web archive 很容易高估 Web，因为当时大规模预约主要不是网络完成

北京 2009 年 9 月开始在 49 家三级医院全面推动预约。北京市卫生部门统计，9—12 月实际预约挂号约 123.4 万个，占实际就诊挂号约 13.05%；预约渠道中：

- 现场窗口约 41.36%；
- 电话约 25.02%；
- 网络约 3.43%；
- 其他方式约 30.19%。

来源：
- 北京市卫生部门：https://wjw.beijing.gov.cn/xwzx_20031/wnxw/201912/t20191214_1175570.html

**证据等级：A。**

因此旧网研究必须建立一个专门的偏差项：

## `Web survival / telephone invisibility asymmetry`

Wayback、Common Crawl 或网页截图会天然留下 Web 入口，却几乎不会留下：

- 114 接线员当时看到的内部界面；
- 患者等待了多久；
- 电话转接了几次；
- 接线员是否成功锁号；
- 医院人工窗口预约；
- 医生诊间直接给患者安排复诊。

如果只依赖 Web artifact，后人会误以为 2009 年“预约挂号数字化”主要发生在浏览器里；同期统计恰恰显示网络只是小渠道之一。

---

## 5. 2010：医院自建 Web 预约与电话预约可以并行，且规则不相同

2010 年 7 月，中日友好医院宣布通过官方站 `www.zryhyy.com.cn` 开通网络预约。同期报道明确：

- 网络预约实名制；
- 范围主要是工作日一周内部分专家号；
- 每天早上 6:00 开始预约下一周相应日期号源；
- 下午 3:00 后停止预约次日号；
- 网络预约费 3 元；
- 同时继续扩展既有 114 电话预约，并增加部分普通号源。

来源：
- 北京晨报同期报道（新浪转载），2010-07-18：https://news.sina.com.cn/o/2010-07-18/015517822351s.shtml

**证据等级：B+。**

这里不能写成“同一医院有一个预约系统”。至少有：

`hospital Web channel` + `114 telephone channel` + `physical hospital workflow`。

它们可能共享部分后台资源，也可能有不同投放规则。若没有后台文档，不能从页面相似性推断同一 slot database。

### Historical-browser warning

今天 `zryhyy.com.cn` 仍存在，当前页面也仍有网络/电话预约说明。但：

**current host continuity != historical page continuity != historical code continuity**。

不得使用 2020s 网站 DOM、TLS、UTF-8、响应式页面或当前浏览器兼容性倒推 2010 年实现。

---

## 6. 2011：统一平台把“医院站点”上移为城市级路由，但事务仍跨系统

北京市 2011 年说明，统一预约平台建设的原因之一，是原先各医院预约号码、网址和流程不统一。平台由 114 电话与网络共同提供服务；2011-07-28 左右 `www.bjguahao.gov.cn` 与电话平台同步试运行。

来源：
- 北京市卫生部门，2011-06-21：https://wjw.beijing.gov.cn/xwzx_20031/wnxw/201912/t20191214_1174492.html
- 法制晚报同期报道（新浪转载），2011-07-27：https://news.sina.com.cn/c/2011-07-27/151122886816.shtml

**证据等级：A/B+。**

### 统一入口不等于统一后台

统一平台至少连接：

`city platform` → `hospital` → `department/doctor` → `hospital slot source` → `patient identity` → `booking confirmation` → `hospital on-site pickup`。

“一个网站能搜很多医院”只能证明入口聚合，不自动证明所有医院的号源系统、身份系统、付费系统和现场 HIS 已经完全统一。

### 电话基础设施也是平台的一部分

旧网考古应避免只画一张 Web sitemap。统一预约的真实服务层还包括 114 话务、短信、医院现场窗口和医院自己的卡/就诊系统。对患者而言，这是一个跨媒介事务，而不是一个网页产品。

---

## 7. Patient identity / operator identity：医疗站点特别容易产生身份错位

2011 年北京儿童医院的 114 预约流程要求家长提供：

- 患儿姓名；
- 家长身份证号；
- 联系电话；
- 预约成功后的短信；
- 到院后按要求取号。

来源：
- 北京儿童医院/北京市卫生部门：https://wjw.beijing.gov.cn/xwzx_20031/jcdt/201912/t20191215_1231789.html

**证据等级：A。**

因此平台层至少有：

`patient = child`

`proxy/guardian = parent`

`identity credential may belong to guardian`

`contact phone may belong to guardian`

`operator = whoever made the call`

这直接禁止一种常见推断：

> “这个手机号/账号预约了儿科，所以手机号/账号主人就是患者。”

医疗、教育、社保等家庭事务都必须保留 **subject / account / operator / guardian** 分离。

---

## 8. 2014—2015：数字预约形成账户信誉、识别码和多渠道稀缺队列

### 8.1 先注册，再抢号

2014 年同期挂号攻略已经建议患者提前完成 114 平台身份注册，否则在新号源释放时才注册会错过号源。部分医院还存在额外院内卡/银行卡要求。

来源：
- 健康时报，2014-08-21：https://www.jksb.com.cn/html/2014/newspaper_0821/88140.html

**证据等级：B。**

这说明到这一步，**account readiness 本身已经成为 appointment executability 的一部分。**

`slot available at release time != user ready to claim slot`。

### 8.2 2015 微信版：公开页面进一步进入半封闭账号空间

2015 年北京 114 微信预约内测，用户需要注册真实就诊人姓名、有效证件信息；成功后系统发送短信和 8 位识别码；到院取号仍要核验患者本人证件。平台还设每日/七日/三个月预约上限与爽约限制。

来源：
- 京华时报/人民网，2015-02-03：https://politics.people.com.cn/n/2015/0203/c70731-26495015.html

**证据等级：B+。**

这里出现三个旧网保存难题：

1. **WeChat enclosure**：事务页位于公众号/账号环境，不是普通公开 URL；
2. **private identity state**：姓名、证件、手机号不应被公共 archive 保存；
3. **reputation state**：爽约次数和临时预约资格是账户私有状态。

因此传统 Wayback 方法对 2015 之后的“网页医疗”会越来越不完整。

### 8.3 预约成功仍可能需要数小时数字排队

2015 年北京青年报/新华网记录，一些热门科室的 114 电话预约需要从凌晨 4 点进入队列，等到下午放号；一名用户晒出的最长通话接近 11 小时。记者实际从 4:15 进入儿童医院口腔科队列，到 14:00 放号后才预约到三个月后的号。

来源：
- 新华网，2015-09-24：https://www.xinhuanet.com/politics/2015-09/24/c_128261318.htm

**证据等级：A-/B+。** 同期用户材料 + 记者复现实测。

所以：

`digital queue exists != waiting eliminated`；

`appointment platform exists != physician capacity increased`。

这也是为何 Web 页面上简单的“可预约/已满”不能被解释成一个静态技术功能：它背后是高度时间敏感的稀缺资源分配。

---

## 9. Archive bias map

### 9.1 `public-shell / private-patient-state asymmetry`

最容易保存：

- 医院首页；
- 专家介绍；
- “预约挂号”按钮；
- 用户须知；
- 放号时间；
- 帮助页。

最不应该、也最难公开保存：

- 患者真实姓名/证件；
- 联系方式；
- 疾病和科室选择；
- 历史订单；
- 爽约记录；
- 医保/就诊卡信息；
- 检查和诊断结果。

因此 public Web 的完整保存也不等于 transaction history 可恢复。

### 9.2 `booking-form / backend-slot-state asymmetry`

HTML 可能显示一个日期下拉框，却无法告诉我们：

- 这个日期当时还有几个号；
- 哪一分钟被谁锁走；
- hospital backend 是否同步；
- 某位专家是否临时停诊；
- 是否存在只投给电话/窗口的独立号池。

### 9.3 `confirmation-artifact loss`

早期系统频繁依赖：

- 预约序列号；
- 短信；
- 8 位识别码；
- 打印/手写预约条。

这些通常不会进入公开 archive。页面说“预约成功后发送短信”只能证明设计流程，不能证明某位用户实际收到短信。

### 9.4 `Web / telephone / window asymmetry`

2009 官方统计已经证明，网络只占预约中的小部分。Web archaeology 若只保存网站，会系统性低估电话与窗口。

应在 evidence record 里明确：

`web-visible channel != total service channel distribution`。

### 9.5 `account / patient / operator / proxy ambiguity`

医疗事务天然存在：

- 家长替儿童预约；
- 成年子女替父母预约；
- 医院人员/家庭医生协助预约；
- 一个手机号码维护多个家庭成员。

所以日志里的账号、手机号、IP 或 browser session 不应直接当作 patient identity。

### 9.6 `appointment / attendance / treatment gap`

即便 archive 保存了一个“预约成功”页面，它也不能证明：

- 患者按时到院；
- 完成取号；
- 医生正常出诊；
- 患者实际接诊；
- 后续检查/治疗发生。

旧网页能恢复的是**某一事务状态**，不是完整医疗事实。

---

## 10. Candidate evidence map

| 时间 | 对象 | 同时代证据 | 可支持 claim | 等级 |
| --- | --- | --- | --- | --- |
| 2003-08 | 苏大附一院 `www.sdfyy.cn` | 江南时报/人民网同期报道 | 注册、动态名额、预约/取消、现场付费取号 | B+ |
| 2009-09~12 | 北京 49 家三级医院 | 北京市卫生部门统计 | 网络/电话/现场预约渠道分布 | A |
| 2010-07 | 中日医院 `www.zryhyy.com.cn` | 北京晨报同期报道 | 实名 Web 预约、时间窗、费用、与 114 并存 | B+ |
| 2011-04 | 北京儿童医院/114 | 医院/卫生部门公告 | guardian identity + child patient + SMS + 现场取号 | A |
| 2011-06~07 | 北京统一平台 `www.bjguahao.gov.cn` | 卫生部门公告 + 同期媒体 | 统一电话与 Web 入口、城市级聚合 | A/B+ |
| 2014 | 114 平台 | 同期健康媒体操作体验 | account readiness、放号时点 | B |
| 2015-02 | 114 微信预约 | 京华时报/人民网 | 实名、识别码、预约上限、爽约规则 | B+ |
| 2015-09 | 114 热门号源 | 北青报/新华网实测 | 电话长队、三个月号源、稀缺未消失 | A-/B+ |

---

## 11. M1 capture status

### Exact candidate originals obtained

- `http://www.sdfyy.cn/` — 2003；
- `http://www.zryhyy.com.cn/` — 2010；
- `http://www.bjguahao.gov.cn/` — 2011—2015。

### 本轮没有达到 M1

**`M1 verified historical Chinese hospital appointment capture: NOT ACHIEVED IN THIS SLICE`**

原因不是“已证明 Wayback 没存”。本轮通过公开检索和 exact host 线索继续定位，但没有得到一份能够实际打开并同时核验以下字段的历史预约 capture：

- `archive_source`；
- `capture_url`；
- `original_url`；
- `capture_datetime`；
- replay / HTTP state；
- Content-Type / charset；
- DOM / form action；
- login/session boundary；
- scripts/subresources；
- 动态号源请求；
- 第二个独立历史时点。

因此不能写：

- “2003 页面是 GB2312”；
- “必须 IE6”；
- “用了 ASP/JSP”；
- “表单 endpoint 是某 URL”；
- “后台每次实时 AJAX 查询”；
- “2011 北京统一平台继承了某医院代码”。

这些全部保持 **UNKNOWN**。

---

## 12. Browser / encoding / plugin assumptions

当前：**UNKNOWN unless a future capture proves otherwise**。

不能根据年代默认：

- IE6；
- ActiveX；
- Java Applet；
- GB2312/GBK；
- frameset；
- table layout；
- 1024×768；
- Windows XP。

这些在 2000s 中文站点中常见，但“常见”不是本项目的 historical evidence。

未来取得 capture 后，至少检查：

1. response headers / meta charset；
2. form target 与 method；
3. JS 是否被 archive rewrite；
4. 登录/预约是否 iframe/跳转到其他 host；
5. 是否依赖 cookie；
6. 现代 Chromium 回放与历史 IE 环境是否有解释差异；
7. 医院公开页面和真正交易 endpoint 是否属于同一域名。

---

## 13. Privacy boundary

医疗预约比一般旧网页具有更高隐私风险。

即使未来 archive、论坛截图、教程或泄漏日志中出现普通人的：

- 姓名；
- 身份证号；
- 手机号；
- 就诊科室；
- 疾病；
- 医保号；
- 预约历史；
- 检查结果；

也不得因为“网上能找到”就批量重新公开。

本仓应优先保存：

- URL pattern；
- 流程；
- 字段类型；
- 页面结构；
- 规则；
- 公开演示账号/官方截图；
- 匿名化后的状态模型。

研究普通用户时只保留支持 claim 所需的最小信息。

---

## 14. 已证实 / 高概率 / 不知道

### 已证实

- 2003 年 `www.sdfyy.cn` 所属医院已公开提供网上预约，且事务仍要到院付费取号。
- 2009 年北京预约改革中，网络渠道远少于现场和电话渠道。
- 2010 年中日医院官方 Web 预约与 114 电话预约并存。
- 2011 年北京统一预约平台同时由电话和 Web 组成。
- 儿科流程中 patient 与 guardian/operator 从设计上就可能不是同一人。
- 2015 年预约平台已经存在实名、识别码、频次限制和爽约惩罚等账户状态。
- 热门专家号在数字平台下仍可能形成长时间远程队列。

### 高概率但仍需 capture/technical evidence

- 医院网站公开壳与真正预约交易 endpoint 很可能存在多 host / backend integration；具体结构未知。
- 2011 城市平台需要与不同医院 HIS/号源系统交换数据，但每家医院的接口形态与同步机制不能由宏观公告推断。
- 2003/2010 页面很可能受到当时浏览器环境影响，但具体影响未知。

### 不知道

- 2003 `sdfyy.cn` 预约页 exact URL；
- 历史 charset；
- 服务器技术栈；
- 身份校验字段；
- 某时点 live slot payload；
- 预约成功页外观；
- 2011 `bjguahao.gov.cn` 首版 DOM 与浏览器兼容性；
- 114 内部 operator UI；
- 电话与 Web 是否在所有医院实时共享完全同一号池；
- 2015 微信预约 transaction 页面能否从任何合规公开档案恢复。

---

## 15. 对中文旧网史的意义

医院预约是一个特别好的反例，提醒本仓不要把中文互联网史写成“页面越来越丰富、用户越来越多”。

一个 2003 年极其朴素的预约表单，可能已经和现实医院的**稀缺号源、实名身份、付费窗口、医生排班和患者身体移动**发生了直接耦合。反过来，一张 2015 年保存精美的挂号页面，如果没有动态号源、电话渠道和现场取号证据，也可能只恢复了现实事务的最薄一层。

因此对 transactional old Web，应增加一个总原则：

> **页面不是事务，事务也不是现实结果。**

对于医院预约尤其如此：

`HTML survived` 并不意味着 `slot state survived`；

`booking succeeded` 并不意味着 `visit happened`；

`account acted` 并不意味着 `patient acted`。

这三个 gap 应成为以后研究网上银行、招生、政务、票务、社保和其他早期事务型中文 Web 的共同方法。