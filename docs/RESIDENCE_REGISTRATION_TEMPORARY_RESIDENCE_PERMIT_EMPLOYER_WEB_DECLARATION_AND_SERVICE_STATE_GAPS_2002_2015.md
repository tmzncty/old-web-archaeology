# 中文旧网居住登记：暂住证、居住证、用人单位 Web 申报与公共服务状态缺口（2002—2015）

## Scope

本文只研究约 **2002—2015 中文网络中与流动人口居住登记、暂住/居住证和相关网上事务直接相关的技术与状态问题**。

重点不是写完整户籍制度史，而是回答：

> **当“一个人住在哪里”逐渐进入计算机数据库、单位 Web 申报、个人网上查询和在线办证系统时，网页上出现的状态究竟能证明什么？**

中国 1995 年以前以及 1990s 的暂住登记，只作为理解 2002—2015 旧网事务的必要前史边界。2016 年以后的移动端、电子居住证和跨城市互认主要放在 `tmzncty/how-people-lived`：

- `topics/from-being-there-to-being-recognized-residence-registration-permits-address-legibility-and-migration-executability-china-1995-2026.zh-CN.md`

本仓不扩成全球居住登记史。瑞典等海外对照也留在 `how-people-lived`。

---

## 一、研究单位：不要把“居住证系统”当成一个网站

至少要区分：

```text
person / 本人身体
actual address / 实际住所
registered address / 已登记地址
registration record / 居住登记记录
permit application / 证件申请
permit card / 实体证件
permit status / 证件状态
service entitlement / 公共服务资格
employer account / 用人单位账号
personal account / 个人账号
page / Web 页面
transaction / 一次事务
backend record / 后台记录
capture / 档案快照
```

尤其禁止直接建立这些等号：

```text
人在地址 A
=
公安数据库记录地址 A
=
当前持有有效居住证
=
拥有某项本地公共服务资格
=
实际已经获得该项服务
```

它们是不同状态。

旧网研究还必须继续区分：

```text
backend computerization
≠
Web service exists
≠
ordinary migrant can access it
≠
ordinary migrant operates it personally
≠
transaction completed online
```

---

## 二、前史边界：暂住登记先于大众 Internet，计算机化也可以先于 Web

1995 年深圳已经有暂住户口、暂住证、蓝印户口和常住户口之间的分层制度。非本市常住户口人员在深圳居留达到规定期限，需要办理暂住证；部分更长期身份又会引用持证年限和暂住记录。[S1]

这对本仓的意义不是把主 scope 拉回 1995，而是建立一个基线：

> **居住地址、持证年限和人口登记在 Web 以前就已经是行政对象。**

所以未来看到“2000s 居住证信息系统”时，不能写成“互联网第一次让城市知道外来人口住在哪里”。

更准确的是：

```text
纸质登记 / 派出所台账 / 单位申报
→ 计算机人口信息系统
→ 部门联网
→ 机构 Web 申报
→ 个人 Web / 移动端
```

而且这些层可能长期并存。

---

## 三、2002 上海：后台已经是信息系统，不等于普通流动人口已经有个人 Web 入口

上海 2002 年的《引进人才实行〈上海市居住证〉制度暂行规定》明确说，居住证信息系统纳入上海社会保障和市民服务信息系统；证件记录持有人的居住地变化，并可用于工作、社保、公积金等事务。[S2]

但这一制度当时主要面向本科以上学历或特殊人才等特定来沪工作创业人员。[S2]

因此至少要拆开两组状态。

### 1. `backend-record / public-Web gap`

2002 年有“居住证信息系统”这一制度事实，只能证明后台信息化存在。

它不能单独证明：

- 普通家庭可从浏览器访问；
- 个人可以在线注册账号；
- 可以远程提交完整申请；
- 当时页面的原始 URL、HTTP、HTML 和浏览器条件。

### 2. `permit-name / population-scope gap`

“上海在 2002 年已经有居住证”也不能写成“2002 年上海全部外来人口已经从暂住证切换到同一套居住证制度”。

同一个证件名称，在不同城市、不同年份可以服务完全不同的人群。

---

## 四、2003：登记事务仍大量依赖单位、房东和户主；取消实体证件也不等于取消后台登记

石家庄 2003 年流动人口管理规定列出了多种代为申报路径：机关、学校、企事业单位可以由指定人员申领，租住房屋可由房主或者本人申领，住常住人口家中可由户主或者本人申领。[S3]

因此 old-Web 研究必须保留：

### `account operator / actual resident gap`

以后即使找到某个单位账号里的申报页面，也不能把页面操作者自动视为证件持有人本人。

### `form submitter / data subject gap`

一个人可以是数据库中的“被申报者”，但不是录入信息的人。

同年沈阳取消《暂住证》，改为免费的暂住登记，仍要求身份证明、照片、现住址、服务处所等信息。[S4]

这证明：

### `physical-certificate / population-registry gap`

**实体证件退出，不代表居住登记退出。**

所以以后研究旧网页时，搜索“暂住证办理网页”找不到，并不能据此推断某地不再记录流动人口。

---

## 五、2008 深圳：最清楚的一份旧网事务合同——Web 首先进入用人单位后台

2008 年深圳公安局和劳动保障局联合启用“深圳市居住证/劳动就业登记网上申报系统”。官方通知直接写给“各用人单位”。[S5]

这份材料是本专题最重要的 A 级技术证据，因为它保留了接近完整的操作序列。

### 1. Web 之前仍有线下账号发放

单位先要到劳动或居住证相关窗口领取系统登录密码和申请材料，然后才能使用网上申报。[S5]

因此：

### `online-establishment / offline-credential-issuance gap`

一个事务有 Web 登录页，并不意味着账号生命周期完全在线。

### 2. 员工先填纸，单位再录电脑

官方流程要求员工填写纸质申请资料，单位再登录网上系统录入个人基本信息、就业信息和居住证信息。[S5]

因此：

### `employee-paper-intent / employer-digital-entry gap`

网页里出现的字段是单位录入的行政记录，并不等于本人直接在网页上逐字段确认。

这也意味着：

```text
paper form says X
≠
employer typed X
≠
backend finally stored X
```

三者理论上都可能发生差异。

### 3. 历史入口不是一个单独站点

官方通知说明，用人单位可以通过：

- “深圳市政府在线”中的“深圳市居住证综合信息网”；
- 深圳市公安局主页；
- 深圳市劳动和社会保障局网上办事大厅；

进入该网上申报系统。[S5]

因此必须区分：

### `entry page / transaction application gap`

几个公开门户可以只是不同入口，真正的事务系统可能是另一个 host、path、frame、redirect 或后台应用。

本轮**没有取得足够证据确认 2008 年事务应用的精确历史 host/path**，所以不应从今天的站点、搜索摘要或后来教程反推。

### 4. “保存”和“上报”是两个不同状态

通知明确把：

```text
信息录入
→ 信息保存
→ 信息上报
```

列成不同步骤。[S5]

因此：

### `saved / submitted gap`

未来即使找到历史截图显示一条记录已经“保存”，也不能推出它已经进入正式申报流程。

### 5. “上报”以后仍然没有办完

网上上报后，单位还要打印劳动就业登记资料或申请居住证人员名单，并带相关材料去线下受理机构/劳动保障窗口办理。[S5]

所以至少存在：

```text
entered
→ saved
→ submitted
→ printed
→ materials carried offline
→ window accepted
→ backend reviewed
→ permit produced / employment registered
```

由此形成：

### `online-submitted / window-accepted gap`

### `window-accepted / permit-produced gap`

### `employment-recorded / residence-permit-issued gap`

所谓“网上申报”在 2008 年并不是端到端无纸化。

---

## 六、2008 的 adoption 边界：服务已经上网，但普通迁移者本人未必是 Web 用户

2008 年同期报道已经把“深圳市居住证综合信息网”作为普通公众查询受理点等信息的入口；同时，制度实施首日的受访劳动者更关心的是证件能否真的提供具体本地事务便利。[S6][S7]

这时至少存在两种完全不同的 Web 用户：

```text
public reader
- 查询政策/受理地点/说明

employer operator
- 登录后台
- 录入员工
- 保存
- 上报
- 打印材料
```

因此：

### `public-information-access / authoritative-transaction-authority gap`

能打开政策页面，不代表拥有申报权限。

### `service-online / migrant-self-service gap`

2008 年“居住证可以网上申报”不能写成“工人已经普遍坐在自己的 PC 前独立办证”。

用人单位 HR、行政人员本身就是数字事务中的代理劳动者。

---

## 七、Web 使就业记录和居住记录发生耦合，但“一个账号里的同一人”仍不等于真实生活完全同步

深圳 2008 系统一次录入同时包含：

- 个人基本信息；
- 就业信息；
- 居住证信息。[S5]

这产生：

### `employment-formality / residence-legibility coupling`

正规单位雇佣可以把一个人更稳定地推入劳动和居住两个行政数据库。

但 old-Web 必须继续拆分：

### `current-employer / current-worker gap`

人可能已经离职，单位记录尚未更新。

### `registered-address / actual-address gap`

人可能已经搬家，后台地址仍是旧地址。

### `permit-valid / entitlement-valid gap`

证件在有效期内，也不意味着每一项依赖居住、社保、积分、家庭条件的具体服务都自动满足。

### `one-card / multiple-backends gap`

一张居住证看起来是一个对象，但其实际功能可能依赖公安、劳动、社保、教育、住房等不同系统。

---

## 八、2015 是 scope 内的重要终点：旧平台更换以后，“同一个居住证网站”不能跨版本处理

2015 年 6 月 1 日，《深圳经济特区居住证条例》实施。同期和稍后的资料显示，新的“深圳经济特区居住证服务平台”接替旧“深圳市居住证综合信息网”，新版流程逐步支持个人账号、网上申办与查询。[S8][S9]

其中，2017 年操作性材料回顾称：

- 2015-06-01 旧“深圳市居住证综合信息网”升级/切换为新平台；
- 新平台使用 `www.szjzz.gov.cn`，后来也见 `szjzz.szga.gov.cn`；
- 页面还保留“原深圳市居住状态查询”等旧数据查询入口。[S8][S9]

这些是 **B/C 级后续操作材料**，只适合用来定位 afterlife 和候选 host。

它们不能单独证明：

- 2008 年旧系统使用同一 host；
- 2015 切换当天的精确 redirect；
- 旧数据库和新数据库怎样迁移；
- 旧证状态如何逐字段映射到新证状态；
- 今天或 2017 页面就是 2015 原始 DOM。

因此新增：

### `same-service-name / same-application gap`

### `same-domain / same-generation gap`

### `legacy-query / migrated-record gap`

一个新平台能查询旧状态，不等于旧系统本身仍然存在，也不等于所有旧字段都完整迁移。

---

## 九、2015 的过渡还证明：系统上线与真实可执行之间存在大量“衔接状态”

2015 年深圳新版居住证上线后的同期舆情材料记录了：

- 居住登记信息查询不到；
- 旧证换新出现障碍；
- 老人、儿童等特殊人群办证困难；
- 新平台发布关于“谁负责登记、怎样登记、申领条件”的说明。[S10]

这类材料不能用来推断“系统整体失败”，但它提醒我们：

### `legacy-record-present / new-platform-visible gap`

旧后台有记录，不等于新前台立即能查到。

### `eligible-in-law / executable-in-transition gap`

条例已经生效，不等于每一个边界案例都能在首日顺利走完新流程。

### `platform-launched / migration-complete gap`

平台发布日不是数据迁移和用户适应的完成日。

---

## 十、状态缺口总表

本专题至少保留以下状态缺口：

```text
physical presence
≠ registered presence

actual address
≠ registered address

registration record
≠ physical certificate

permit held
≠ permit valid

permit valid
≠ service eligible

service eligible
≠ service actually received

resident / data subject
≠ form submitter
≠ account operator

paper form completed
≠ employer entered
≠ backend saved

saved
≠ submitted

submitted online
≠ accepted offline

accepted
≠ permit produced

employment registration
≠ residence-permit issuance

public page accessible
≠ transaction authority granted

backend computerization
≠ public Web

service online
≠ migrant self-service

entry portal
≠ transaction host/path

old platform record exists
≠ new platform displays it

same service name
≠ same application generation

same domain
≠ same backend

announcement survives
≠ application survives

historical locator found
≠ historical capture verified
```

---

## 十一、平台技术与页面形态：目前能证明什么，不能证明什么

### 已能证明

2008 官方制度文本能证明：

- 有 Internet 登录的单位申报系统；
- 登录依赖组织机构代码或工商注册号 + 系统登录密码；
- 账号/密码最初需要线下取得；
- 系统有信息录入、保存、上报、打印等状态；
- 系统把劳动就业与居住证信息放在一个申报工作流里；
- 网上提交以后仍需要线下窗口材料；
- 有多个公共门户可以进入该事务。[S5]

2015 后续材料可以帮助定位新平台和旧查询 afterlife。[S8][S9]

### 仍不知道

本轮没有取得并逐页检查符合仓库 METHOD 合同的 2002—2015 historical replay，因此以下全部保持 `unknown`：

- 2008 事务应用精确 original host/path；
- HTTP status / headers；
- charset；
- 原始 HTML / frameset / table / CSS；
- JavaScript；
- 是否 IE-only；
- 是否依赖 ActiveX、客户端证书或特定安全控件；
- session/cookie；
- 登录失败/密码过期页面；
- 地址编码查询控件；
- “保存”和“上报”的具体 endpoint；
- 后台如何同步公安与劳动系统；
- 打印页面的 HTML/插件实现；
- 提交后 receipt/流水号；
- 旧证数据到 2015 新平台的字段迁移机制；
- 2015 切换当天的 redirect / DNS / server 行为。

因此：

> **M1 — NOT ACHIEVED IN THIS SLICE.**

这一轮取得的是 historical locator、官方事务合同和 afterlife 线索，不是已经完成的 historical page reconstruction。

按照 `docs/METHOD.md`：

> **locator ≠ verified capture。**

也不能把“本轮没有实际取得可检查 replay”写成“Wayback 没保存”。

---

## 十二、Archive preservation：旧网最容易留下的是政策文本，最容易消失的是决定普通人状态的事务后台

这个专题对历史可见性尤其典型。

今天深圳政府网站仍能打开 2008 年公报文本。[S5]

这能证明：

- 通知正文；
- 当年制度名称；
- 工作流；
- 当时列出的入口名称。

但今天的响应式政府 CMS 页面不能证明 2008 年原始网页长什么样。

### `modern-CMS-preserved-text / historical-page gap`

更容易消失的恰恰是：

- 登录页；
- 单位账号首页；
- 员工列表；
- 草稿；
- 保存状态；
- 上报状态；
- 打印预览；
- 错误码；
- 地址库；
- 受理回执；
- 旧证迁移失败；
- 数据同步延迟。

因此，未来只看公开幸存网页，会产生明显偏差：

> **我们更容易保存“制度说应该怎样办”，却更难保存“一个具体人那天到底办到哪一步”。**

---

## 十三、浏览器与字符集假设

在没有 historical capture 以前，不应根据 2008 年“网上办事大厅”四个字自动填：

```text
IE6-only
GB2312
frameset
ActiveX
```

这些在同期政务站点中都很常见，但对本系统目前只能属于候选 hypothesis。

正确写法是：

```text
charset: unknown
browser dependency: unknown
ActiveX/client control: unknown
session implementation: unknown
```

等取得原始 capture、帮助文档、安装包或同期兼容性说明以后再升级证据等级。

---

## 十四、隐私与再发布边界

居住登记是 old-Web 中隐私风险最高的一类事务之一。

历史系统理论上可能包含：

- 姓名；
- 身份证号码；
- 手机；
- 精确住址；
- 房东/户主；
- 工作单位；
- 就业状态；
- 家庭成员；
- 子女；
- 证件状态。

即使未来在 Web Archive、泄漏数据库、论坛截图或第三方缓存里找到真实记录，也不应为了“考古完整”重新公开普通人的完整个人信息。

优先保存：

- 公开帮助页；
- 空白表单；
- schema/字段名；
- URL pattern；
- 状态机；
- 匿名化截图；
- 错误页；
- 公开政策说明；
- 无个人数据的客户端/浏览器依赖证据。

`capture exists` 不自动创造再发布权。

---

## 十五、证据台账

### A 级 / 原始或同期制度材料

**[S1] 深圳市人民政府，1995**
《深圳市户籍制度改革暂行规定》。用于 pre-Web 边界，不作为本仓主对象。

**[S2] 上海市人民政府，2002**
《引进人才实行〈上海市居住证〉制度暂行规定》。证明居住证信息系统及早期对象边界。

**[S3] 石家庄市人民政府，2003**
《石家庄市流动人口管理办法》。证明单位/房东/户主等代理登记路径。

**[S5] 深圳市公安局、深圳市劳动和社会保障局，2008**
《关于启用深圳市居住证/劳动就业登记网上申报系统的通知》。本专题核心 A 级事务合同。

**[S11] 国务院，2015**
《居住证暂行条例》。用于 scope 末端制度边界。

### B 级 / 同期或近同时期媒体、机构二次材料

**[S4] 2003 沈阳取消暂住证报道**：证明“取消实体证件但继续登记”的分支。

**[S6][S7] 2008 深圳同期报道**：证明公众信息入口和当事人对证件功能的同期理解。

**[S10] 2015 深圳新旧平台切换初期舆情**：证明迁移期出现记录查询、换证等执行摩擦。

### C 级 / 后来操作材料

**[S8][S9] 2017 操作指南/用户教程**：只用于定位 2015 新平台 afterlife、候选 URL 和旧状态查询，不反推 2008 原始技术实现。

### D 级 / 本文重建与概念

- `service-online / migrant-self-service gap`
- `account operator / actual resident gap`
- `employee-paper-intent / employer-digital-entry gap`
- `saved / submitted gap`
- `legacy-record-present / new-platform-visible gap`
- `modern-CMS-preserved-text / historical-page gap`

这些术语不是历史行动者原词。

---

## 十六、这改变了我们怎样理解中文旧网？

过去写“2008 年深圳居住证网上申报”，很容易只留下一个网站名。

实际上，当时的普通生活动作更像：

```text
工人住进出租屋
→ 单位/房东/本人形成登记责任
→ 员工在纸上填资料
→ 单位行政人员取得网页登录密码
→ HR 进入 Web
→ 录入员工资料
→ 保存
→ 上报
→ 打印
→ 拿纸去线下窗口
→ 后台继续处理
→ 证件最终成为另一些公共事务的入口
```

**Internet 没有突然把一个迁移者变成“线上居民”。它先把单位、公安、劳动部门之间的一部分中间劳动搬上了 Web。**

而今天真正最难考古的，恰恰不是“深圳当年有一个居住证网站”这句话，而是：

> 某个普通人搬了家以后，那一条地址记录有没有及时改变；某个 HR 点击“保存”以后有没有再点“上报”；旧系统里已经存在的一年居住时间，在 2015 年新平台里究竟有没有完整出现。

这些数据库状态对人的真实生活比首页配色更重要，却比首页更容易从历史中消失。

---

## Sources

### [S1]
深圳市人民政府：《深圳市人民政府关于印发〈深圳市户籍制度改革暂行规定〉的通知》，1995。
https://www.sz.gov.cn/zfgb/1995/gb82/content/post_10057342.html

### [S2]
上海市人民政府：《引进人才实行〈上海市居住证〉制度暂行规定》，2002。
https://www.shanghai.gov.cn/nw4644/20200905/0001-4644_304.html

### [S3]
石家庄市人民政府：《石家庄市流动人口管理办法》，2003；司法部法规库镜像。
https://www.moj.gov.cn/pub/sfbgw/flfggz/flfggzdfzwgz/200411/t20041112_135062.html

### [S4]
新华网/中广网：《沈阳取消暂住证 在全国率先推出申报暂住登记制》，2003-07-22；新浪历史镜像。
https://news.sina.cn/sa/2003-07-22/detail-ikknscsi0834263.d.html

### [S5]
深圳市公安局、深圳市劳动和社会保障局：《关于启用深圳市居住证/劳动就业登记网上申报系统的通知》，深公（指）字〔2008〕289号，2008-06-30。
https://www.sz.gov.cn/zfgb/2008/gb604/content/post_4985042.html

### [S6]
新华社：《深圳正式实施居住证制度》，2008-08-02；新浪历史镜像。
https://news.sina.com.cn/c/2008-08-02/083814256077s.shtml

### [S7]
《深圳商报》：《持居住证9月有望赴港游》，2008-08-02；新浪历史镜像。
https://news.sina.com.cn/c/2008-08-02/045514254951s.shtml

### [S8]
百度经验：《深圳市居住证状态查询》，2017-03-11。后续操作材料，只作 afterlife / locator 证据。
https://jingyan.baidu.com/article/925f8cb8f88d2cc0dde056a3.html

### [S9]
深圳本地宝：《深圳居住证办理网站》，2017-05-22。后续服务指南，只作 afterlife / locator 证据。
https://m.bendibao.com/bsy613844.html

### [S10]
深圳新闻网：《8月份深圳市网络舆情应对能力排行榜》，2015-09-22，其中梳理新版居住证上线初期执行问题。
https://www.sznews.com/zhuanti/content/mb/2015-09/22/content_16895848_13.htm

### [S11]
国务院：《居住证暂行条例》，国务院令第663号，2015-11-26 公布，2016-01-01 施行；教育部政府门户镜像。
https://www.moe.gov.cn/jyb_xxgk/moe_1777/moe_1778/201612/t20161213_291799.html
