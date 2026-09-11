# 人事档案、人才市场查询、转递与保管状态缺口（中文 Web，1996—2015）

## 0. 研究边界

本 note 研究约 1996—2015 年中文 Web 中与**流动人员人事档案**相关的公开页面、人才市场/毕业生就业网站、查询入口、办事说明和转递状态，而不是写完整的人事档案制度史。

1996 年以前的人才流动与档案托管只作为边界前史，用来解释 2000s 中文 Web 为什么会出现“查档案到没到”“申请接收”“开调档函”等页面；不把 `old-web-archaeology` 的主对象无限前移。

跨时期生活史、制度重返、纸质档案与职业流动的长线比较写在：

- `tmzncty/how-people-lived/topics/from-unit-bound-personnel-files-to-online-dossier-portability-personnel-record-custody-and-administrative-biography-china-1983-2026.zh-CN.md`

本 note 只回答：**当普通人通过中文 Web 处理“档案在哪里、谁保管、能不能接收、是否寄出、有没有到达”时，网页实际证明了什么，又有什么关键状态永远不会由公开 Web 自动证明。**

---

## 1. 先拆对象：一个“查档案”页面背后至少有十五个不同实体

研究时必须分开：

1. **physical person / 现实中的人**；
2. **file subject / 档案主体**；
3. **current employer / 当前雇主**；
4. **former employer / 原单位**；
5. **authorized custodian / 有权保管档案的机构**；
6. **receiving institution / 拟接收机构**；
7. **platform/site/host / 人才市场、毕业生就业或人社网站**；
8. **Web account / 网站账号**；
9. **keyboard operator / 实际操作网页的人**；
10. **query record / 查询结果记录**；
11. **acceptance application / 接收或人才储备申请**；
12. **transfer letter / 调档函、接收函或同类程序性文件**；
13. **dispatch record / 转出记录**；
14. **sealed dossier / 被封装并实际运输的档案本体**；
15. **arrival/index record / 新保管机构的到档、入库、目录状态**；
16. **dossier contents / 档案内部材料**；
17. **downstream use / 后续录用、政审、职称、退休、升学等真实利用结果**。

因此必须长期保留下面的状态差：

`site exists`
`!= institution is authorized custodian`
`!= user registered`
`!= query identity matched the correct person`
`!= query result is current`
`!= receiving application submitted`
`!= receiving institution approved`
`!= transfer/acceptance letter valid`
`!= old custodian audited the dossier`
`!= dossier physically dispatched`
`!= receiver physically received it`
`!= receiving system indexed arrival`
`!= materials are complete`
`!= contents are correct`
`!= downstream institution accepts those records`
`!= downstream life-course transaction succeeds`。

这套拆分与本仓 `docs/METHOD.md` 的原则一致：platform、site、account、page、capture、claim 不得混成一个研究对象。

---

## 2. 1996 是制度边界，不是 Web 起点

1996 年《流动人员人事档案管理暂行规定》明确把辞职、辞退、解除合同、待业大中专毕业生、自费出国留学者，以及外资、乡镇、民营、私营企业中的专业技术与管理人员等纳入流动人员人事档案管理对象。

来源：
- 北京市政府保存文本：https://www.beijing.gov.cn/zhengce/zhengcefagui/qtwj/201208/t20120817_776589.html
- 广州市白云区政府保存文本：https://www.by.gov.cn/zwfw/zdfw/rcfw/xgzc/content/post_5807252.html

**证据等级：A（政府站保存的法规文本）。**

这份规则的重要性在于解释后来网站中的“档案托管/查询/转递”为什么存在：

- 人已经可以离开原单位；
- 新雇主未必有档案保管权；
- 本人又不能把档案当作普通私人文件自行长期持有；
- 因而人才交流/公共人才服务机构成为现实生活与权威记录之间的中介。

这里不把 1996 年写成“网上档案服务开始”。当时的制度对象先于大众 Web；后来中文 Web 只是逐步给这套既有 custody architecture 增加可查询和可申请的界面。

---

## 3. 2007 厦门：非常完整的 `online status + offline papers + physical dossier` 混合事务链

### 3.1 exact historical original hosts

厦门大学学生处 2007 年 5 月 28 日面向应届毕业生发布人才储备办事通知，明确留下两个当时使用的主机：

- `http://www.xmrs.gov.cn/` —— “厦门人事网”，用于毕业生人才储备申请和审批状态查询；
- `http://www.xmrc.com.cn/` —— “厦门人才网”，用于后续查询档案是否到达人才服务中心。

来源：
- 厦门大学学生处，2007-05-28，《关于2007届毕业生申报厦门市和福州市人才储备的通知》：https://xsc.xmu.edu.cn/info/1017/41911.htm

**证据等级：A/B+。** 同时代高校官方办事通知，可证明当时通知给毕业生的 URL 和事务流程；不能单独证明两个站点任意一天的页面 DOM、编码、脚本或浏览器兼容条件。

### 3.2 网页能完成什么

按通知，毕业生先进入“厦门人事网”毕业生就业频道：

1. 注册；
2. 填写个人资料；
3. 提交人才储备申请；
4. 若干工作日后再次登录查询审批结果。

如果审批通过，Web 事务仍未闭合。本人或代理人还需要带毕业生推荐表、就业协议书或毕业证/报到证等材料，到厦门市人才服务中心现场审核；审核后取得接收函，再把接收函交给学校，由学校办理后续离校和档案转移。

档案真正到达人才服务中心以后，落户等后续事务才继续；毕业生可以在“厦门人才网”查询档案是否到达。

因此 2007 厦门应写成：

`online identity/profile created`
`→ application submitted`
`→ approval state visible online`
`→ paper credentials checked offline`
`→ receiving letter issued`
`→ university dispatches sealed dossier`
`→ receiving center physically receives dossier`
`→ arrival state becomes queryable`
`→ later hukou/employment procedure continues`。

### 3.3 最重要的考古结论：Web 首先数字化的是状态，不是档案本体

这一案例不能写成“2007 年厦门已经实现电子档案”。从现有证据只能稳妥确认：

- 申请与审批状态可以在 Web 上发生/查询；
- 档案到达状态可以在另一个网站查询；
- 权威档案仍需由学校向人才服务机构转移；
- 后续落户依赖档案真正到达。

因此：

`online approval visible != dossier digitized`

`arrival status visible != dossier contents publicly readable`

`query says arrived != contents complete/correct`。

这类页面更适合称为 **locator/workflow layer**，而不是“个人电子档案全文”。

---

## 4. 2010 东北大学：毕业生首先需要的是“我的档案到底被寄到哪里”

东北大学 2010 年 7 月 26 日发布通知，说明学校已经把 2009、2010 届毕业生档案去向数据导入网站。毕业生可以按学院、学号、姓名等信息查询，结果包含档案寄送方式、是否已经寄出、档案去向等。

来源：
- 东北大学，2010-07-26，《关于学生查询档案去向的通知》：https://dwww.neu.edu.cn/2010/0726/c2230a31365/pagem.htm

**证据等级：A。** 同时代高校官方通知。

对 old-Web 来说，这提供了一个很重要的页面类型：**dossier locator / 档案定位查询**。

它与一般内容页不同：

- 页面可能只有简单表单；
- 真正有价值的是后端一条与身份相匹配的私人状态；
- 搜索爬虫和公共 archive 往往只能保存空表单或帮助文字；
- 历史研究者即便恢复了 HTML，也通常无法合法、可靠地恢复某个普通毕业生当年的后台查询结果。

因此：

`query page captured != query result captured`

`query result captured != result was current`

`“已寄出” != receiver has received`

`destination text != final authorized custodian after later transfers`。

---

## 5. 2007 “死档”新闻：旧网保存个人名单时，历史可见性与隐私会发生冲突

2007 年北京人才档案公共管理服务机构曾通过公开方式寻找长期失联档案的主人。同期报道说，5700 余份长期无人办理手续的档案中，只有 200 余名主人重新取得联系，约 5500 份随后被封存为不能继续正常提供服务的“死档”。

来源：
- 《京华时报》/新浪，2007-12-15，《5500份档案寻主未果今起封存》：https://news.sina.com.cn/c/2007-12-15/024613082329s.shtml

**证据等级：B。** 同期媒体报道，数量采用报道口径，不外推全国。

本仓关心的不是重新建立一张“谁弃档了”的个人名单，而是一个 archive ethics 问题：

> 当年为了公共服务而公开的人名/档案状态，二十年后如果仍被搜索引擎或 archive 保存，研究者是否应该再次聚合、扩散？

答案应当是**不默认这样做**。

### 隐私边界

- 不批量重建普通人的姓名—档案状态名单；
- 不因为旧页面曾公开，就把姓名、身份证号、工作单位等重新做成数据集；
- 研究“死档公告”的页面结构和制度功能时，只保留支持 claim 所需的最少个人信息；
- 若未来获得 archive capture，先做隐私审查，再决定是否截图或引用。

这与 `docs/METHOD.md` 的“已删除/普通个人敏感内容最小化”原则一致。

---

## 6. 2014—2015：保管成为免费公共服务，Web 入口与 custody authority 仍不能混写

2014 年末，中组部、人社部、发改委、财政部、国家档案局发布通知，明确自 2015 年 1 月 1 日起取消流动人员人事关系及档案保管费、查阅费、证明费、转递费等，由公共就业和人才服务机构提供基本公共服务。

来源：
- 人力资源和社会保障部，2014-12-10：https://www.mohrss.gov.cn/SYrlzyhshbzb/jiuye/zcwj/gaoxiaobiyesheng/201412/t20141215_146304.html

**证据等级：A。** 中央部门政策文件。

旧网页考古时尤其要避免一个错误：

`某人才网提供档案查询/代办页面`

不自动等于：

`这个网站运营主体具有法定档案保管权限`。

研究单位应至少拆成：

`Web service provider`
`!= legal custodian`
`!= actual warehouse/档案库`
`!= downstream institution that uses dossier`。

在某些时期，同一事业单位可能同时承担网站运营和档案保管；但需要证据确认，不能从品牌名相似直接推断。

---

## 7. 2015 之后的新界面不属于本仓主范围，但它反向说明 2000s Web 做到哪一步

2019 年北京人才档案公共管理服务已经能让个人在线申请部分档案服务；2020 年疫情期间，北京此前完成的数百万卷档案数字化又支撑了查询、证明、调档函、退休预约等“不见面”服务；2021—2022 年新规继续要求档案由授权机构管理，严禁个人自带转递，同时推进数字档案和全国数据共享。

这些后续发展属于 `how-people-lived` 的长时段比较，不在本仓扩写。但它们对 old-Web 有一个方法学意义：

2003—2015 中文人才/毕业生网站中的“档案查询”，很可能只覆盖数字化成熟链条中的前两层：

1. **locator digitization** —— 在哪里、到没到、寄到哪；
2. **workflow digitization** —— 申请、审批、开函、预约。

不能从它们倒推当时已经存在：

3. **full image digitization** —— 整卷材料已扫描可内部调用；
4. **cross-system interoperability** —— 多机构自动共享和核验完整状态。

---

## 8. 需要长期保留的 archive asymmetries

### 8.1 `locator-page survival / dossier-content invisibility`

“档案查询”入口很可能被保存，档案内容本身从设计上就不应进入公共 Web archive。

因此历史研究中常出现一种倒置：最容易看到的是“请输入姓名/学号查询”，最看不到的是这个查询为什么对某个人的未来重要。

### 8.2 `public-guidance / private-state asymmetry`

办事指南、转递说明、收费标准、咨询电话易保存；

真实个人状态——是否接收、是否寄出、是否到档、缺什么材料、谁正在保管——通常要求身份验证或属于后台数据库。

### 8.3 `query-result freshness ambiguity`

即便获得一张历史截图，上面写“已寄出/已到达”也只能证明**该查询时点系统显示如此**。

不能自动证明：

- 后续没有退回；
- 没有再次转递；
- 物理档案和数据库记录同步无误；
- 若干年后的保管机构仍相同。

### 8.4 `custodian-state / physical-artifact gap`

数据库可能先写“转出”，纸档案可能仍在运输；

也可能纸件已经到达，新机构尚未完成拆封、审核、目录录入。

因此：

`dispatch database state != physical transit state != receiving catalog state`。

### 8.5 `identity-query privacy`

很多查询以姓名、身份证号、学号、毕业学校、年份等为键。这类页面即使可技术复原，也不等于应该大规模重放真实查询或重新公开结果。

### 8.6 `dead-file-publicity survival bias`

失联、异常、无人认领的档案因为需要公告，反而更可能留下公开网页；正常完成转递的人通常不会产生同等公开痕迹。

因此旧网样本可能**系统性高估异常案例**。

### 8.7 `digital-front-end / paper-backend asymmetry`

网页看起来越来越现代，不代表档案本体已经变成网络文件。2007 厦门案例尤其说明：

`web application` + `online status`

可以和：

`paper credentials` + `sealed institutional transfer`

长期共存。

### 8.8 `successful-query survivorship`

论坛/帮助帖最容易留下两类人：

- 顺利查到结果，分享教程；
- 遇到异常，公开求助。

完全不知道需要查档案、没有上网、没有留下文字的人不可见。不能从旧网讨论密度估算真实档案关注度。

---

## 9. 平台、账号、档案主体与操作人必须继续分离

未来若找到人才网 archive capture，应至少记录：

- host / platform；
- 页面类型（公开指南、登录页、查询页、结果页、咨询页）；
- 是否需要注册；
- 查询键是什么；
- 操作人是否必须与档案主体相同；
- 是否允许单位经办人/学校/代理人操作；
- 结果是公开页面还是登录态；
- URL 是否包含个人标识；
- 是否缓存或泄漏敏感参数。

尤其不能从“某账号提交了调档申请”推断：

`account owner == dossier subject == physical operator == receiving institution contact`。

2007 厦门通知本身就允许“本人或代理人”办理部分线下环节；未来获得 Web 端证据时同样必须检查代理角色。

---

## 10. 历史技术条件：目前哪些仍是 UNKNOWN

本轮恢复了 `www.xmrs.gov.cn`、`www.xmrc.com.cn` 等同时代 original hosts，但没有取得一份已经实际打开、可复核的 2007 historical capture。

因此以下全部保持 **UNKNOWN**：

- 页面当时使用 GB2312、GBK 还是 UTF-8；
- ASP/JSP/PHP 等服务端技术；
- 是否依赖 IE 专属脚本或 ActiveX；
- 表单 action；
- session/cookie 机制；
- 查询结果 URL 是否带个人参数；
- JS/CSS/图片是否由独立子域提供；
- 2007 与后续版本是否同一套代码；
- modern Chromium 回放是否等于历史浏览体验。

不因为“2007 年中国政务网站通常……”就补写这些内容。

---

## 11. M1 archive 状态

本轮以以下 historical original hosts / locator 为入口继续尝试公开 archive 定位：

- `http://www.xmrs.gov.cn/`
- `http://www.xmrc.com.cn/`
- 东北大学 2010 档案去向查询通知中的校内查询路径线索。

目前没有取得一份**实际打开后**能够同时核验下列字段的合格 capture：

- `archive_source`
- `capture_url`
- `original_url`
- `capture_datetime`
- replay / HTTP state
- Content-Type / charset
- DOM / form action
- login/session boundary
- scripts/subresources
- 一份查询入口之外的第二历史时点

因此记录：

> **M1 verified historical Chinese personnel-dossier/talent-market query capture: NOT ACHIEVED IN THIS SLICE.**

这不等于“Wayback 没保存”，也不等于历史站点不可恢复。它只表示本轮没有拿到达到本仓最低证据合同的 verified capture。搜索结果、现存办事通知和 historical original URL 只能作为 candidate locator / A-B 级事务证据，不能伪装成已经检查过的 Memento。

---

## 12. 已证实 / 高概率 / 不知道

### 已证实

- 1996 年制度已经把多种脱离传统单位的人生状态纳入流动人员人事档案管理。
- 2007 年厦门毕业生可以通过“厦门人事网”提交人才储备申请并查询审批，再通过人才服务中心/学校完成纸质材料与档案转移；“厦门人才网”可用于查询档案是否到达。
- 2010 年东北大学公开通知毕业生可在线查询档案寄送与去向状态。
- 2015 年起流动人员基本档案保管、查阅、证明和转递服务取消收费。

### 高概率但仍需更强页面级证据

- 2000s 人才/毕业生 Web 的核心价值之一是把原本需要电话/现场反复询问的“审批、去向、到达”状态变成远程可见。
- “查询层”通常先于整卷档案影像化和跨机构数据互操作成熟。
- 人才服务站点的实际用户可能包含本人、学校经办人、单位人员和代理人，而不只是档案主体本人。

### 不知道

- 2007 厦门两个历史站点具体页面布局、charset、浏览器要求与后台框架；
- 真实查询结果页是否被公共 archive 保存；
- 查询页面与档案库后台是实时同步、批量同步还是人工更新；
- 2003—2010 各地人才市场网上查询覆盖率；
- 普通私企员工实际多久会主动查询一次档案；
- 某个历史查询结果与纸档案真实位置之间的误差率。

---

## 13. 对中文旧网史的修正

人事档案网站提醒我们，中文旧网不能只按“内容平台”来写。

2000s 的 Web 里还有大量今天不那么显眼的**状态型页面**：

- 录取状态；
- 志愿提交状态；
- 社保缴费状态；
- 户籍/居住证办理状态；
- 医院预约状态；
- 档案审批、寄出、到达状态。

它们往往页面并不华丽，却可能直接决定一个人的下一份工作、落户、读研或回到某种制度轨道。

而这类页面又恰好最难考古：**公开壳容易留下，私人状态最容易消失。**

所以 old-Web 的历史可见性不能只问“页面有没有保存”，还要问：

> **真正改变这个人未来的那一行后台状态，当年是否只存在于一个登录后的数据库结果里；今天即使页面壳还活着，我们是不是已经再也看不见它。**
