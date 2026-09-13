# 1999 上海夫妻分居调沪：网上政务后台、居民申报入口与 public-interface gap

> 状态：artifact/provenance research note  
> 建立日期：2026-09-13  
> Scope：1999—2008 中文政务数字化边界；研究“网上办理”在旧网语境中到底证明了什么，不把后来的公开政务门户反投射到 1999 年。

## 1. 为什么写这一条

`old-web-archaeology` 已经有大量“网页 ≠ 最终事务状态”的案例，也刚记录过 legacy page 的 title/body mismatch。

本 note 不再制造一个近义 state-gap，而处理一个更具体、会直接影响 1990s—2000s 中文互联网史解释的问题：

> **一份 1999 年政府文件明确说某项事务已经建立“计算机网上政务服务系统”，这是否足以证明普通居民当时已经能在公开 Web 页面上在线申请？**

答案是：**不能。**

本轮材料反而显示，一项与普通家庭命运直接相关的事务，可以先在政府内部/部门之间网络化，而居民端仍通过单位、街道、区县人事局和纸质材料进入流程。

这里把需要保留的边界称为：

**`networked backoffice != public Web front end`**

这不是抽象理论，而是 1999 上海“解决夫妻两地分居”政策文本本身能够支持的窄结论。

## 2. 研究对象必须拆开

本轮至少涉及四个不同对象，不能把“网上政务服务系统”当成一个模糊网站名：

1. **policy document**：沪人〔1999〕122 号规范性文件；
2. **administrative system**：文件所称“解决夫妻两地分居计算机网上政务服务系统”；
3. **citizen submission channel**：单位申报或个人经街道向区县人事局申报；
4. **current legacy Web representation**：今天上海人社/区政府网站上保存的旧政策正文。

它们的证据问题完全不同。

## 3. 1999 文件到底证明了什么

上海市人事局、上海市公安局 1999-09-15 的通知现由上海市人力资源和社会保障局网站保存。

当前 URL：

https://rsj.sh.gov.cn/tzyjsrygl_17294/20200617/t0035_1390377.html

文件号：`沪人[1999]122号`

### 3.1 居民/单位入口

文件第二条说：

- 在上海的一方提出申请；
- 可以由工作单位申报，也可以个人申报；
- 市直属单位向市人事局申报；
- 其他单位向注册地区县人事局申报；
- 个人申报则通过户籍所在地街道（乡、镇）向区县人事局申报。

因此，从文本直接可见的 ordinary-user path 是：

```text
夫妻/单位
→ 单位或街道
→ 区县/市人事局
→ 行政处理
```

这里**没有**写“申请人登录网站、自行填报”。

### 3.2 网络化处理层

文件第三条则说，本市建立“解决夫妻两地分居计算机网上政务服务系统”；市、区（县）人事局可通过该系统在网上办理调沪手续；承办部门应把在沪一方和调沪人员的基本信息及办理情况输入系统，符合系统内设条件的，可以核发落户证明。

因此文本直接支持：

```text
human submission / institutional submission
→ personnel bureau operator
→ networked administrative system
→ basic-person data + case-processing data entered
→ system condition check / administrative processing
→ settlement proof
→ public-security household-registration step
```

来源：
https://rsj.sh.gov.cn/tzyjsrygl_17294/20200617/t0035_1390377.html

证据等级：**A-content / current legacy representation**。

说明：文件内容本身是 1999 年规范性文件文本；但当前 URL、HTML、DOM、CMS 模板显然是后来的保存层，本轮没有把当前页面冒充 1999 historical Web capture。

## 4. 新增的考古边界：public-interface fallacy

旧网研究很容易出现这样一条错误推理：

```text
1999 文件写“网上办理”
→ 1999 已有公开政务网站
→ 普通居民可以在浏览器里提交申请
```

本轮材料不支持这条链。

更安全的最小 claim 是：

> **1999 年上海该业务已经存在一个供市、区县人事部门使用的计算机联网政务处理系统。**

不能进一步自动推出：

- 系统基于 HTTP/Web；
- 系统暴露于公网 Internet；
- 居民拥有账号；
- 居民自己录入表单；
- 申请材料电子化上传；
- 审批全流程无纸化；
- 当前“一网通办”系统与 1999 系统技术连续。

将上述错误扩张称为：

**`public-interface fallacy / 公众界面谬误`**。

只把这个名字作为审查提示：当历史材料写“网上”“联网”“电子政务”时，先问**谁在网上**。

## 5. 为什么这会直接改变普通生活史

对 `how-people-lived` 来说，“夫妻两地分居”并不是纯粹的情感或交通问题。1999 上海路径要求：

- 在沪一方；
- 外地配偶属于特定专业技术/管理人员范围；
- 在沪存在接收单位；
- 满足职称、学位、工作年限、分居年限或特殊困难等条件；
- 人事部门处理工作关系；
- 公安环节处理户口。

网络化后台可能改变审批信息怎样在机构之间流动，但普通人的入口仍可能是单位/街道和一叠证明材料。

因此数字化可以先改变：

`institutional latency / data circulation / condition checking`

而暂时不改变：

`citizen-facing interaction surface`。

这是一种此前仓库没有单独写清楚的数字化顺序。

HPL 对应研究包：

`tmzncty/how-people-lived/sources/two-site-households-spouse-separation-commuter-marriage-work-transfer-and-communication-china-1981-2026.zh-CN.md`

## 6. 2000 年中央人事业务进一步证明：“网上办理”首先是行政流程现代化词汇

人事部 2000-10-18 印发的反腐败抓源头实施办法，把“电子政务”与公开、监督联系起来，并要求：

- 公务员考试录用；
- 留学人员回国安置；
- 中央国家机关军转干部接收与安置；
- 国际职员后备人员招考；
- **中央国家机关解决干部夫妻两地分居审批备案**；
- 西部人才开发；

等六项业务在 2000 年 12 月 1 日前逐步实行“网上办理”，实现“服务、办理、监督一体化”。

当前政府保存页：

https://rsj.sh.gov.cn/trlzyhshbzbgz_17256/20200617/t0035_1388302.html

证据等级：**A-content / current legacy representation**。

这证明 2000 年中央人事系统确实把 online handling 当作行政数字化目标。

但它仍然不能单独证明每项业务都有：

`public WWW form + citizen login + electronic attachment upload + end-to-end online approval`。

研究时应把“网上办理”拆成更细的问题：

```text
network exists?
application/database exists?
operator is government staff or citizen?
public Internet or internal network?
browser or dedicated client?
data entry by whom?
attachments digital or paper?
final decision returned how?
```

## 7. 2008 静安材料提供了一个非常重要的用户端反证

静安区政府当前仍保存一份成文/发布于 2008-11-20 的《照顾家庭困难、夫妻分居调沪有关政策》。正文仍然规定：

- 单位申报：向区人事局申报；
- 个人申报：通过户籍所在地街道向区人事局申报；
- 申报材料包括单位报告、本人书面申请、结婚证明、户籍证明、干部调动登记表、外省市商调函、接收证明、身份证号码等；
- 页面列出静安区人事局人才开发科的办公时间、地址、联系人和电话。

当前 URL：

https://www.jingan.gov.cn/govxxgk/JB2/2008-11-20/e33cefe5-9610-4a07-a032-0ab229b88913.html

证据等级：**A-/B+ current legacy representation carrying 2008-dated policy/service content**。

这不能证明 2008 年不存在任何线上居民功能；但它可以反证一种过强叙事：

> “1999 建立网上系统以后，这项事务已经自然演化为普通居民从家中 Web 自助完成。”

至少到这份 2008 服务说明所呈现的路径里，**单位、街道、区人事局、纸质/证明材料和具体办公室仍然是可见的居民接口。**

## 8. 一个很容易误读的当前 UI：legacy content 上方的“立即办理”不是 2008 artifact

当前静安页面顶部可以看到“立即办理”等现代政务站点界面元素。

但正文同时明确保留 2008 年的：

- 成文日期；
- 老机构名称；
- 具体办公室；
- 固定办公时间；
- 联系人；
- 当年纸面材料清单。

因此当前页面至少是：

**`current government portal representation carrying 2008-dated service content`**

而不是：

**`verified 2008 Web service interface`**。

这与上一轮 SASS 的 title/body mismatch 不同：这里不是题名错配，而是**现代服务门户 shell 与历史正文共存**。

所以应记录：

`current action button != historical action capability`

如果自动 agent 只读取页面上今天的“立即办理”，就可能把 2020s 的站点能力投射回 2008。

## 9. 后台规则引擎本身也是一种会消失的历史 artifact

1999 文件有一句非常值得考古：

> 人事部门把双方基本信息和办理情况输入系统，“符合系统内设条件的”，即可核发落户证明。

这至少说明系统不是单纯的电子文本传输管道；政策文本声称系统内部存在某种“条件”。

但今天我们不知道：

- 字段 schema；
- 哪些字段必填；
- 学历/职称如何编码；
- 分居年限如何计算；
- 接收单位如何表示；
- “家庭特殊困难”是否能由系统规则表达；
- 条件判断是硬编码、数据库查询还是操作员辅助；
- 是否存在 manual override；
- 错误输入如何退回；
- 不符合条件时系统显示什么；
- 哪一层才做最终人工审批。

于是这里出现一个新的 preservation gap：

**`backend policy-engine survival gap / 后台政策判定引擎保存缺口`**。

旧网档案即使保存了后来公开的政策说明，也可能完全没有保存真正运行过的行政软件。

## 10. 研究时建议增加 actor-surface 字段

对 1990s—2000s “网上办理/联网服务”材料，建议在普通 page/capture 字段之外，加一个很轻量的 actor/interface 记录块：

```yaml
networked_government_service:
  historical_claim_date: 1999-09-15
  service_name: 解决夫妻两地分居计算机网上政务服务系统
  claimed_online: yes
  confirmed_operator:
    - municipal_personnel_bureau
    - district_county_personnel_bureau
  citizen_direct_access: unknown
  employer_direct_access: unknown
  street_office_role: confirmed_submission_intermediary
  public_internet: unknown
  protocol: unknown
  software_client: unknown
  browser_based: unknown
  data_entry_actor: personnel_department_staff
  internal_condition_check: claimed_in_policy_text
  paper_documents_parallel: highly_likely_and_2008_visible
  historical_ui_capture: no
  current_legacy_policy_page: yes
```

目的不是增加 schema 复杂度，而是强迫研究者回答：

> **谁看见了屏幕？谁按下了“提交”？**

## 11. 与 current 一网通办的边界

今天上海“一网通办”中的“解决夫妻两地分居困难调沪”已经明确展示：

- 网上咨询；
- 网上收件；
- 网上预审；
- 网上受理；
- 网上办理；
- 结果信息反馈；
- 受理/审批机构和服务条件。

当前服务页示例：

https://zwdt.sh.gov.cn/govPortals/bsfw/item/9458e55d-e161-4108-9283-676d00bac1fe

另一当前地区页面仍显示实体综合窗口和现场提交材料中的电子签章要求：

https://zwdt.sh.gov.cn/govPortals/bsfw/item/1ca925c4-82a3-45a1-ac9e-c9f0e6dd4715

这些 current pages 只能证明**今天的 hybrid/online service surface**。

绝不能做：

```text
2026 current portal has online receipt
+
1999 policy says 网上政务服务系统
→ same public-facing system continuously existed since 1999
```

中间缺少二十多年 software/platform/protocol/citizen-interface continuity evidence。

## 12. 一条很重要的时间链

目前证据可以安全写成：

### 1999-09

上海规范性文件：

- 居民/单位通过既有行政渠道申报；
- 市、区县人事局使用计算机网上政务服务系统；
- 部门录入个人/案件信息；
- 文件声称系统有“内设条件”。

### 2000-10

人事部：包括中央国家机关夫妻两地分居审批备案在内的六项业务，要逐步网上办理。

### 2008-11

静安区公开服务说明：居民仍可见单位/街道/区人事局申报链、材料清单、实体办公室和电话。

### 2020s current portal

公开“一网通办”已经明确标示网上咨询、收件、预审、受理、办理和结果反馈；部分环节仍可见线下窗口/材料动作。

这是一条**interface ownership transition**的候选链，但本轮不把它写成连续技术谱系，因为 1999/2000 系统 artifact 尚未找到。

## 13. 反例与后见之明风险

### 13.1 “网上”不一定等于 World Wide Web

1999 的“计算机网上政务服务系统”可能是 Web，也可能是内部网络上的专用应用、C/S 软件或其他架构。本轮没有技术手册，保持 `unknown`。

### 13.2 “政府内部联网”不等于居民没有受益

即使居民没有 Web 表单，后台联网仍可能减少重复传递、跨层级等待、手工条件核对和监督成本。

因此不能反过来说“因为不是公众 Web，所以数字化对普通人没有意义”。

### 13.3 2008 的纸面/街道路径不证明后台没有继续在线

完全可能出现：

`resident offline front door + government online backoffice`

这恰恰是本 note 要保存的混合形态。

### 13.4 当前 legacy page 不等于 historical page

上海人社当前 URL 路径中甚至含 `20200617`；静安当前页面也处于现代门户模板下。

因此只能引用其中保存的 dated policy content，不能从当前 DOM 推 1999/2008 DOM。

## 14. VERIFIED / PROBABLE / UNKNOWN

### VERIFIED

- 1999-09-15 上海文件明确称已经建立夫妻两地分居“计算机网上政务服务系统”；
- 文件明确指定市、区县人事局通过系统办理并录入人员/案件信息；
- 文件同时明确居民入口可以通过单位或街道向人事局申报；
- 2000 人事部文件要求中央国家机关夫妻两地分居审批备案逐步网上办理；
- 2008 静安当前 legacy page 保存的服务正文仍列单位/街道申报、纸面材料、办公地址/时间/电话；
- 今天上海公开政务门户存在更明确的 citizen-facing online service surface。

### PROBABLE / reasonable inference

- 1999 系统至少承担跨行政层级的信息录入/案件处理功能；
- 1999 “系统内设条件”说明软件或数据库层存在某种资格判断支持，而非纯静态信息发布；
- 1999—2008 期间可能长期存在“居民线下入口 + 部门网络化后台”的混合服务结构。

### UNKNOWN

- 1999 系统原软件名/厂商；
- 网络拓扑；
- 是否 TCP/IP；
- 是否浏览器；
- 是否运行在公开 Internet；
- 服务器/数据库；
- 登录/权限模型；
- UI screenshot；
- field schema；
- condition engine 实现；
- 1999 原始公开介绍页 URL；
- 1999—2008 软件是否同一系统；
- current 一网通办与旧系统是否有技术继承关系。

## 15. M1 状态

### 本轮真正取得的

- 两份明确日期、文件号和规则内容的 1999/2000 政策文本 current legacy representations；
- 一份 2008-dated district service-content legacy representation；
- 一个可证伪的 actor/interface 分层；
- 一个 old-Web 研究中容易发生的 public-interface fallacy；
- 一个具体的 backend policy-engine preservation gap。

### 仍未取得

没有得到 1999 “解决夫妻两地分居计算机网上政务服务系统”的：

- historical Web capture；
- 原 UI 截图；
- 客户端安装包；
- 软件手册；
- 系统架构文档；
- 原 hostname/IP；
- browser/protocol 信息；
- 数据字典；
- 两个历史运行时点。

因此：

**`M1 historical Shanghai spouse-separation e-government interface: NOT ACHIEVED IN THIS SLICE`**

并且不能写成“Wayback 没保存”，因为本轮甚至还没有确认该系统是否曾是公开 Web 可抓取对象。

## 16. 下一步最值钱的动作

1. 搜 1999—2001 上海人事局内部刊物、计算机应用会议论文、政府信息化项目采购/验收资料；
2. 搜“夫妻两地分居计算机网上政务服务系统”的完整短语、简称、软件厂商和培训资料；
3. 查 1999—2002 上海人事局历史域名、站点地图和“网上办事”栏目，但只把 URL locator 当 locator；
4. 找区县人事干部操作手册或培训课件，优先恢复 field schema / workflow；
5. 找一个能确认 operator-facing UI 的 screenshot/artifact，再决定是否把它升级为完整 archaeological case；
6. 继续追 2000 年中央人事“六项业务网上办理”究竟使用统一平台还是多个业务系统；
7. 如果最终确认是内联网/专网客户端而非 Web，把它作为中文旧网边界说明，不把 OWA scope 扩张成全国电子政务史。

## 17. 本轮新增价值

这次真正增加的不是“行政审批还有线下材料”这句常识，而是一条会改变旧网史叙述的证据规则：

> **历史材料中的“网上办理”，首先告诉我们某个 actor 使用了网络；它不会自动告诉我们那个 actor 是普通公众。**

1999 年，一个人的婚后生活能不能结束长期两地分居，已经可能由计算机联网的行政系统参与判断和流转；但当事人自己的“界面”，仍可能是一张申请、一个单位、一条街道和一个人事局窗口。

所以研究数字化进入普通生活时，不能只问“这个服务哪年上网”。

还要问：

> **网络究竟先出现在普通人的桌面上，还是先出现在决定普通人命运的那张办公桌后面？**