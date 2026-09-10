# 异地就医备案、纸质报销、联网结算、待遇计算与真实医疗之间的状态缺口（中国，2005—2015）

> Scope：本文严格服务于 `old-web-archaeology` 的约 1995–2015 中文互联网主范围。
>
> 它不是中国医疗保险制度通史，也不把 2017 以后全国跨省结算平台、医保电子凭证、2020s 国家医保服务平台扩成本文主对象。
>
> 更长的制度前史、2008—2026 普通人异地就医生活史、2019—2026 四种未来比较以及欧洲 EHIC 对照见：
>
> https://github.com/tmzncty/how-people-lived/blob/main/topics/from-carrying-receipts-home-to-direct-cross-region-settlement-medical-insurance-migration-and-care-finance-portability-china-1998-2026.zh-CN.md
>
> 核心考古问题：一张旧医保网页如果写着“异地就医”“异地安置”“联网结算”“持卡结算”“异地定点”“即时结报”，研究者究竟能证明到哪一层？公开办事指南、登记表下载、本人备案成功、医院已接入、社保卡能识别、费用能上传、参保地待遇能计算、患者出院只付自付部分、经办机构之间最后完成清算，并不是同一个对象。

---

## 1. 为什么异地医保是 old-Web 特别容易被误读的对象

它横跨至少四个世界：

### 1.1 Public Web

最容易被 archive 保存：

- 人社/医保部门首页；
- 办事指南；
- “异地就医登记”说明；
- 定点医院名单；
- 下载表格；
- FAQ；
- 政策新闻；
- 网上查询入口；
- “即时结算平台上线”公告。

### 1.2 Authenticated / semi-private service

较难保存：

- 个人社保登录；
- 参保身份匹配；
- 异地安置登记；
- 转诊备案；
- 社保卡状态；
- 本人异地待遇状态；
- 结算明细查询。

### 1.3 Inter-agency / medical backend

公共 archive 通常看不到：

- 医院 HIS；
- 医保前置机；
- 地方医保核心业务系统；
- 省级交换平台；
- 跨地区专线；
- 费用明细上传；
- 医保目录和编码映射；
- 参保地待遇计算；
- 对账与资金清算；
- 错误码与人工回退。

### 1.4 Offline care and reimbursement

真正影响普通人的现实事务：

- 医生是否真的看了这个人；
- 患者实际住院；
- 家庭先拿出多少钱；
- 发票和费用清单是否齐全；
- 家属是否坐车回参保地；
- 经办窗口是否受理；
- 钱什么时候真正回到家庭账户。

因此本文最重要的总边界是：

`public medical-insurance page != executable cross-region entitlement`。

---

## 2. 与仓库已有专题的分工

### 2.1 与社会保险账户专题

已有：

`SOCIAL_INSURANCE_ACCOUNT_QUERY_CONTRIBUTION_RECORD_TRANSFER_AND_BENEFIT_STATE_GAPS_2000_2015.md`

研究：

- 工作是否形成社保记录；
- 缴费是否入账；
- 养老关系怎样转移；
- 长期权益怎样累计。

本文不重复“养老缴费年限可携带”。

本文问：

> 医保关系暂时仍在 A 地时，一笔发生在 B 地的真实医疗费用能否由 A 地待遇现场执行？

### 2.2 与医院预约专题

已有医院预约 state-gap 研究：

`预约成功 != 到院 != 报到 != 接诊`。

本文从医疗发生后继续：

`医院真的接诊 != 异地医保真的能结算`。

### 2.3 与网上银行/汇款专题

医保清算也涉及资金，但不能套用普通银行转账模型。

患者窗口“少付了一笔钱”以后，背后还可能有：

- 医院垫付；
- 就医地经办审核；
- 参保地基金确认；
- 地区间对账；
- 周期性资金清算。

因此：

`patient settlement complete != inter-agency clearing complete`。

---

## 3. 对象模型

### 3.1 Insured person

研究字段：

- 参保地；
- 医保险种；
- 身份证件/社保卡；
- 当期参保状态；
- 异地就医类别；
- 是否备案；
- 是否转诊；
- 是否异地长期居住。

注意：

`有社保卡 != 医保待遇当前有效`。

### 3.2 Insured-region authority

负责或参与：

- 认定参保关系；
- 备案/转诊状态；
- 待遇政策；
- 费用审核；
- 基金支付；
- 手工报销。

### 3.3 Care-region authority

可能负责：

- 接入当地医疗机构；
- 医院协议管理；
- 费用数据接收；
- 异地患者结算服务；
- 对医疗行为进行属地监管；
- 与参保地协调。

### 3.4 Medical institution

不是“医保网站”的附属页，而是独立事务节点。

需要区分：

- 医院本身存在；
- 是当地医保定点；
- 是某异地合作定点；
- 已接入交换平台；
- 某类业务已上线；
- 某天系统可正常交易。

### 3.5 Registration / filing record

“异地安置登记”“异地就医备案”“转诊审批”等状态。

可以是：

- 纸质登记表；
- 单位/社区证明；
- 窗口录入；
- 电话/传真；
- 后来的网上申请。

### 3.6 Expense record

医院产生的：

- 总费用；
- 药品；
- 检查；
- 治疗；
- 耗材；
- 自费项目；
- 住院日；
- 病种/诊断。

### 3.7 Reimbursement claim

旧流程里患者/家属把票据等提交参保地。

至少区分：

`materials delivered`
→ `claim accepted`
→ `reviewed`
→ `approved amount calculated`
→ `payment issued`
→ `money received`。

### 3.8 Direct-settlement transaction

新流程中，医院结算端实时/准实时与外地医保规则交互。

至少区分：

`identity match`
→ `eligibility check`
→ `filing/referral match`
→ `expense upload`
→ `benefit calculation`
→ `response received`
→ `patient-side settlement`
→ `later inter-agency clearing`。

### 3.9 Social security card

可以作为：

- 身份凭证；
- 医保结算入口；
- 查询入口；
- 本地/异地持卡凭证。

不能写成：

`一张全国统一卡 = 全国待遇规则统一`。

---

## 4. 基本状态链

### 4.1 传统异地手工报销

`person insured in A`
→ `moves / travels / is referred to B`
→ `care occurs in B`
→ `patient pays first`
→ `hospital emits receipts + itemized list + medical record`
→ `patient/family keeps documents`
→ `documents return to A`
→ `A accepts claim`
→ `A applies its policy`
→ `approval`
→ `payment`
→ `patient finally receives reimbursement`。

### 4.2 委托代办

`care in B`
→ `patient gives paper to local B-side service window`
→ `window batches paper`
→ `staff/agency moves claims to A`
→ `A reviews`
→ `result/funds return`
→ `B-side window / bank delivers outcome`。

这不是“真正联网直接结算”，但已经显著改变患者的跑腿成本。

### 4.3 点对点联网结报

`patient registered for cross-region arrangement`
→ `care in B`
→ `B service point accesses A-related data over dedicated network`
→ `expense/policy data exchanged`
→ `reimbursement calculated locally or cooperatively`
→ `patient completes settlement in B`。

### 4.4 省级异地直接结算

`multiple local systems`
↔ `provincial exchange / centralized platform`
↔ `connected hospitals`
↔ `care transactions`。

### 4.5 全国阶段（仅作为 2015 边界说明）

本文不展开 2017 后全国系统，但必须保留前后边界：

2015 年一些省份已有成熟省内异地平台，不能倒写成当时已经具备后来全国统一跨省能力。

---

## 5. 长期可复用的 state gaps

### 5.1 `public-guidance / personal-eligibility gap`

旧网站有“异地就医办理指南”，只能证明指南公开。

不能证明某个用户：

- 符合异地安置条件；
- 当期参保正常；
- 可以申请；
- 已经申请成功。

### 5.2 `form-download / authoritative-record gap`

archive 保存了一张《异地就医登记表》PDF/Word/HTML 字段，不等于：

`表被填了`
或
`表被经办机构录入`。

### 5.3 `filing-submitted / filing-effective gap`

网上或窗口提交备案，不等于权威系统中的备案已经生效。

尤其历史流程可能有：

- 审核；
- 单位盖章；
- 居住证明；
- 指定医院；
- 次月生效；
- 有效期限。

### 5.4 `referral-approval / settlement-eligibility gap`

医疗上需要转诊，和医保系统认可这次转诊，是两个状态。

### 5.5 `hospital-designated / network-connected gap`

某医院被文件列为异地定点，不能自动证明：

- 接口已上线；
- 前置机运行正常；
- 当天可以实时交易。

2008 四川新农合在京试点就是明确反例：合作存在，但医院与四川网络接口尚未完全连好，患者仍需全额支付后寄票据回家。

### 5.6 `network-connected / transaction-success gap`

系统已经接入，也会：

- 超时；
- 断网；
- 版本不一致；
- 身份匹配失败；
- 数据未上传；
- 规则未同步。

因此历史公告“平台已经联网”不能升级为“每一笔都成功”。

### 5.7 `identity-card / entitlement-match gap`

社保卡能被读出，不等于当前：

- 医保关系有效；
- 异地备案有效；
- 医院有权执行这类待遇。

### 5.8 `care-place-bill / insured-place-benefit gap`

医院账单产生于就医地；医保待遇属于参保地。

直接结算必须在两者之间做规则转换。

因此：

`same bill != same reimbursement`。

### 5.9 `catalog-code / benefit-rule gap`

药品、诊疗项目、耗材在就医地有代码，不等于参保地待遇算法天然认识它。

### 5.10 `receipt-exists / reimbursable-expense gap`

一张发票可以证明患者付过某笔钱，但不能独立证明：

- 费用符合医保范围；
- 材料齐全；
- 参保地最终认可。

### 5.11 `claim-submitted / claim-accepted gap`

患者把票据交给窗口，只证明材料到达。

### 5.12 `claim-approved / funds-received gap`

审核通过和钱进入个人账户之间仍有时间。

### 5.13 `patient-settlement / inter-agency-clearing gap`

患者出院只付自付部分，是前台体验完成。

经办机构与医院、两地基金之间的资金对账可能之后才发生。

### 5.14 `local-platform / national-portability gap`

2011 年一个省已经“省内异地一卡通”，不能写成跨省也一样。

### 5.15 `one-service / all-medical-services gap`

住院可直接结算，不推出：

- 普通门诊；
- 门诊慢病；
- 药店；
- 特殊病种；

也已互通。

### 5.16 `same-province / same-policy gap`

即使同省，各统筹市历史上仍可能有不同规则。

### 5.17 `care-occurs / insurance-transaction gap`

一个患者真正接受了医疗，却完全可能以“自费”完成，后续再报销。

所以医疗记录不能自动证明医保交易同步发生。

### 5.18 `historical-info-page / historical-network-state gap`

今天还能打开的一张旧政策页可能继续调用：

- 当前医院名单；
- 当前电话；
- 当前查询接口；
- 当前统一平台。

这属于：

`current-backend rehydration`

而不是历史网络状态。

---

## 6. 2005—2008：Web 之外的数字系统比普通用户页面更重要

### 6.1 主研究边界

2005—2008 的异地医保考古不能只问：

> “当时有没有网上备案按钮？”

更重要的是：

- 地方医保数据库是否集中；
- 社保卡是否用于医疗结算；
- 医院与经办机构怎样联网；
- 异地合作是纸件代办、专线查询还是实时结算；
- 患者面对的是卡、窗口还是网页。

### 6.2 2008 四川—北京试点：政策合作存在，接口却尚未完成

同期《中国新闻周刊》/国际在线材料记录四川新农合在北京两家医院试点。

22 岁务工者林强在羊坊店医院做阑尾炎手术后，虽然可以按合作安排享受报销比例，但后续报道明确说：医院与四川方面网络系统尚未连接好，仍需患者全额支付并把报销单据寄回四川。

证据等级：**B+ / B（同期调查与后续报道）**。

来源：

- 2008-04-23：
  https://news.sina.com.cn/o/2008-04-23/131613782301s.shtml
- 2008-06-11：
  https://news.sina.com.cn/s/2008-06-11/173114001920s.shtml

这个案例应作为仓库未来判断“平台上线”的标准反例：

`institutional agreement exists`

但

`technical interface ready = false`。

### 6.3 两个月只有 4 人：available 不等于 used，更不等于 popular

同一后续报道记录试点运行两个月仅 4 名患者使用。

按照仓库 METHOD：

- `exists`：可以证明；
- `available to eligible people`：在限定群体/医院中可以证明；
- `used`：有具体患者；
- `popular`：证据反而明显不支持。

不要把“首次跨省试点”标题扩写成“农民工开始普遍异地报销”。

---

## 7. 2008—2010 长三角：非常重要的中间态——“搬砖头”

### 7.1 嘉兴代办窗口

2009 年新华社/《经济参考报》调查记录，嘉兴设置上海医保异地代办窗口；工作人员每周把票据、单据和经费在两地之间搬运，业内称为“搬砖头”。

证据等级：**B+（同期记者调查）**。

来源：

- 浙江在线 / 新华社，2009-04-03：
  https://china.zjol.com.cn/05china/system/2009/04/03/015401763.shtml
- 新浪财经 / 经济参考报，2009-05-04：
  https://finance.sina.com.cn/g/20090504/09276177255.shtml

### 7.2 为什么它对 old-Web 方法特别重要

研究者若只保存当时公共网站，可能看到：

- “异地医保联动”；
- “便民服务窗口”；
- “合作协议”；
- 办理地址。

但真实事务其实仍然：

`paper-based`。

只是：

`paper transport labor`

从患者转移给经办机构。

所以不能把：

`service locally accessible`

误写成：

`transaction digitally interoperable`。

### 7.3 上海—杭州双向联网：专用宽带与窗口前移

同期调查还记录上海—杭州之间铺设专用宽带，异地参保人可在当地医保服务窗口较快完成结报。

患者仍可能先在医院支付，再到当地医保窗口结算。

因此它是：

`manual hospital payment`
+ `network-assisted local reimbursement`，

而不是后来意义上的：

`hospital discharge direct settlement`。

这是老网页标题里“联网结算”最需要谨慎解释的地方。

### 7.4 2009 陈瑞棠：十分钟完成的是什么？

材料记录杭州参保、上海居住的陈瑞棠老人拿 12 张发票到上海医保事务中心，约 10 分钟完成报销。

这可以证明：

- 当地服务窗口能够办理；
- 事务时间显著缩短；
- 纸质发票仍在流程中。

不能证明：

- 他在医院出院时已经直接结算；
- 医院端实时连接杭州；
- 每名沪杭异地参保人流程完全相同。

---

## 8. 2009—2011：政策目标与 Web 办事页之间还隔着一整个后台

### 8.1 人社部发〔2009〕190号

正式政策提出：

- 重点改善异地安置退休人员等异地就医；
- 减少个人垫付；
- 提高结算服务效率；
- 逐步实现就地就医、持卡结算。

证据等级：**A（正式政策文本）**。

来源：

- 吉林省卫健委保留政策：
  https://wsjkw.jl.gov.cn/zdzt/shylwstzgg/201404/t20140410_7868352.html
- 岳阳市政府保留：
  https://www.yueyang.gov.cn/web/2570/2584/2860/content_472989.html

### 8.2 这份政策不能证明任何一个历史网页事务已经上线

它只能证明国家层面的政策方向。

不能直接推出：

- 2010 全国已有统一平台；
- 所有省都能持卡；
- 网上备案已普及；
- 定点医院系统已实时互通。

### 8.3 2010 辽宁公开规则：同一种“异地”还有不同事务

同期辽宁材料把：

- 短期出差急诊；
- 异地安置；
- 转诊转院；

区别处理。

证据等级：**B+（同期人社部门政策被广播媒体报道）**。

来源：

- 中国广播网 / 新浪，2010-08-17：
  https://news.sina.com.cn/c/2010-08-17/094720914732.shtml

所以 archive 里一个通用导航项“异地就医”，其后可能是多个完全不同的资格和材料状态机。

### 8.4 2011 宜昌异地安置办事页：典型 public guidance artifact

后续保留的 2011 年地方办事说明列出：

- 办理部门；
- 窗口地址；
- 办理时限；
- 长期异地居住退休人员条件；
- 《基本医疗保险异地就医登记表》；
- 身份证/社保卡复印件；
- 居住证明等材料。

证据等级：**A-/B+（地方人社来源被现存政策指南页保留）**。

来源：

https://www.zgdbjz.org.cn/home/guids/article/id/12723.dbjz

这种页面对 old-Web 极有价值，因为它能证明：

- public process description；
- 所需字段/材料；
- offline location；
- eligibility model。

但它不能证明任何特定申请人通过。

---

## 9. 社保卡：全国统一卡面标准与异地交易能力必须分开

### 9.1 1999 首张全国统一规范社保卡不等于全国一卡通已实现

人社部 2015 年回顾称：1999 年 12 月上海发行全国首张社会保障卡，早期即支持职工医保费用结算；2004 年后随着金保工程，各地用卡环境逐步完善；2011 后发卡进入快车道。

证据等级：**C+/A-（2015 人社部官方历史回顾）**。

来源：

https://rst.ln.gov.cn/rst/zxzx/shbz/0ECBA3E2173D4E2382B6E876ADB7E7B8/index.shtml

必须保留：

`nationally standardized card != nationally interoperable medical entitlement`。

### 9.2 2011 宁波：一张卡先解决市内，再逐步扩到省内

同期/近同时期材料记录宁波 2011 年发新社保卡，并计划先实现大市范围异地就医实时结算，再扩到省内部分定点机构。

来源：

https://www.cpic.com.cn/c/2021-05-31/1801813.shtml

这里非常适合说明：

同一张卡的“可用范围”有地理和时间版本。

一张 2011 年社保卡照片本身不能告诉研究者它在 2011 年 9 月、10 月、11 月分别能在哪些医院使用。

这就是：

`card-artifact / acceptance-network gap`。

---

## 10. 2011—2013：后台网络扩张早于统一公众查询界面

2012 年人社信息化工作总结称，到 2011 年末，已有 23 个省份建立省内异地就医结算系统，或通过省级大集中系统形成支持能力。

证据等级：**A/B+（同期全国人社信息化总结）**。

来源：

https://rst.hunan.gov.cn/xxgk/tzgg/201205/t20120509_4225653.html

这对仓库有一个方法论意义：

> 历史 Web 搜不到“统一异地医保门户”，并不能推出当时没有数字异地结算。

因为最关键的系统可能是：

- 专线；
- 省级数据中心；
- 医院前置机；
- 经办机构业务客户端；
- 社保卡读卡环境；

它们本来就不是公共网页。

---

## 11. 2013—2015：省级平台逐渐成为关键中间层

### 11.1 平台必须同时解决政策和代码

地方建设经验表明，异地即时结算不仅需要网络，还需要：

- 全省药品目录/代码映射；
- 诊疗项目；
- 服务设施；
- 疾病编码；
- 医院与经办机构协议；
- 监管机制；
- 费用结算规则。

后来的湖北“十三五”规划对 2011—2015 回顾称，当地建立省级异地就医结算管理信息交换平台，并统一相关目录和编码；2015 年有 6.4 万人次通过省级交换平台即时结算。

证据等级：**C+/A-（政府规划对刚结束阶段的正式回顾）**。

来源：

https://rsj.ezhou.gov.cn/xxgk/fdzdgknr/sswghxx/fzgh/202302/t20230228_524877.html

### 11.2 2015 广东平台上线

深圳医保局现行专题页明确回顾：

- 2015 年 10 月，广东省医疗保险异地就医直接结算平台上线；
- 2015 年 11 月 24 日，深圳龙岗区第二人民医院接入省平台。

证据等级：**C+/A-（后来的官方机构系统史，日期明确；不是 historical capture）**。

来源：

https://hsa.sz.gov.cn/ztzl/ydjyzjjs/

### 11.3 不能把 current retrospective page 当 2015 页面

今天打开上述专题能证明：

- 深圳医保局当前如此记述其系统史。

不能证明：

- 2015 当天专题页长这样；
- 当时 host/DOM/charset/JS 与今天相同；
- 2015 页面已经包含后来的全国跨省栏目。

因此证据类型必须标：

`current official retrospective`

而不是：

`2015 historical Web capture`。

---

## 12. 一个特别重要的语义分裂：就医地目录 / 参保地待遇

异地直接结算经常需要把两套规则同时带入一笔交易。

从 2009—2015 各地实践，到后来全国规则，都能看到类似逻辑：

- 医疗行为发生在就医地；
- 医疗机构和项目首先属于就医地系统；
- 最终报销比例、起付、封顶等又与参保地待遇密切相关。

因此历史页面写：

> “在异地医院可直接结算”

绝不能被理解成：

> “像当地参保人一样按完全相同规则报”。

本文固定：

`care-place catalog / insured-place benefit semantic split`。

未来 reconstruction 若模拟一笔 2014 年异地费用，必须明确：

- 使用哪一年；
- 哪个参保地；
- 哪个就医地；
- 哪套药品/诊疗目录；
- 哪套待遇参数；
- 哪个交易链。

否则只能是现代演示，不是历史事务复原。

---

## 13. Web artifact 分类建议

### Artifact A：政策/新闻页

能证明：

- 某项合作/平台被宣布；
- 当时公开语言；
- 宣称目标；
- 机构名称。

不能证明：

- 后端真的稳定；
- 普通人都能使用。

### Artifact B：办事指南

能证明：

- eligibility；
- required documents；
- office；
- deadline；
- official workflow。

不能证明：

- individual outcome。

### Artifact C：下载表格

能证明：

- institution expected certain fields；
- paper-based bootstrap still existed。

注意记录：

- `.doc` / `.xls` / `.pdf`；
- 文件名；
- MIME；
- 是否 archive 保存附件；
- 中文编码；
- 是否宏/ActiveX/模板依赖。

### Artifact D：公共医院/地区查询页

能证明：

- 用户可搜索当时公开范围（前提是 capture 的数据本身也是历史的）。

风险：

历史 HTML 可能调用当前数据库。

### Artifact E：个人查询/备案入口

必须额外记录：

- 登录主机；
- 身份字段；
- 社保卡号/身份证号；
- 验证码；
- HTTPS；
- iframe；
- ActiveX/证书要求；
- session；
- 是否可匿名访问。

不追求真实普通人账号回放。

### Artifact F：医院端/经办端客户端

通常根本不属于 public Web。

如果只能从：

- 招标文档；
- 软件手册；
- 技术论文；
- 培训截图；

间接了解，必须明确 evidence grade。

---

## 14. 浏览器与技术环境假设

2005—2015 政务/社保网站常见：

- IE 优先；
- 表格布局；
- GB2312/GBK；
- iframe；
- JS 表单校验；
- 下载 Office 文档；
- 控件/证书；
- 图片按钮；
- 动态 JSP/ASP/ASPX；
- 个人系统与公开网站分 host。

因此现代 Chromium 成功打开一张 archive 页面，只能证明：

`modern replay yields a representation`。

不能直接证明：

`2010 用户的 IE6/IE8 实际操作路径完全相同`。

尤其个人服务如果依赖：

- ActiveX；
- 客户端证书；
- 旧版 TLS；
- 本地读卡器；

现代回放可能天然失真。

---

## 15. Archive preservation gaps

### 15.1 `transaction-survival gap`

公共页面可能保存，真实事务几乎不会。

### 15.2 `authenticated-state gap`

登录后的备案、待遇和费用明细因隐私/robots/session 等不应成为普通公共 archive 目标。

### 15.3 `backend-API gap`

页面壳还在，但历史异地结算 API、JSP endpoint、专线服务早已下线。

### 15.4 `hospital-side gap`

患者真正交易的医保终端/HIS 前置机不在公开 Web。

### 15.5 `attachment gap`

办事页还在，Word/Excel 登记表附件丢失。

### 15.6 `list temporal drift`

旧页面标题写“联网医院查询”，实际加载的是今天的医院名单。

### 15.7 `policy temporal drift`

旧 URL 被 CMS 迁移后正文可能是后来的政策解释，不能仅凭 URL 年份判断内容时间。

### 15.8 `administrative-success / paper-survival inversion`

这是本轮新增的保存反转。

旧手工报销会在个人手里留下：

- 发票；
- 清单；
- 复印病历；
- 报销受理单；
- 车票；
- 汇款/到账痕迹。

而直接结算改革的目标恰恰是让患者不再搬这些纸。

因此：

> 正常、成功、无摩擦的联网事务，未来反而可能比失败后转手工报销的事务更少留下私人纸质痕迹。

这不是证据缺陷，而是系统成功本身改变了证据生产。

### 15.9 `manual-fallback visibility bias`

系统失败以后：

- 患者投诉；
- 媒体报道；
- 纸件增多；
- 人工窗口记录增加。

所以历史材料可能系统性高估失败/麻烦事务的可见度。

必须区分：

`more surviving failure evidence`

与

`higher historical failure rate`。

---

## 16. 对“第一人”“首例”“上线”的词汇约束

旧网材料常见：

- “全省首例”；
- “首个跨省结算”；
- “平台正式上线”；
- “一卡通”；
- “无障碍”；
- “即时结算”。

这些词必须降解成可检验 claim。

例如：

### “首例”

最多证明媒体/机构如此定位某一事件。

需确认：

- 首个什么保险类型？
- 首个什么地理范围？
- 首个何种结算方式？
- 是住院还是门诊？

### “一卡通”

不能默认：

`one card works everywhere for every service`。

### “即时”

必须问即时到哪一步：

- 患者窗口？
- 经办审批？
- 医院回款？
- 地区间基金清算？

### “联网”

必须问连接了：

- 哪些市；
- 哪些医院；
- 哪些险种；
- 哪些业务；
- 哪个版本。

---

## 17. 2015 这个范围边界怎样写

`old-web-archaeology` 主对象不能因为这个专题被拖到 2026。

因此本文以 2015 为主体结束：

- 2000s：地方医保 Web/经办系统、纸件与点对点合作；
- 2008—2010：代办、专网、异地结报探索；
- 2011—2013：社保卡、省级大集中、省内结算系统扩张；
- 2014—2015：省级交换平台成熟度提高，一些省份实现较大范围即时结算。

2016 后全国跨省结算只作为：

`later state transition`

用于说明 2015 系统边界，详细生活史交给 `how-people-lived`。

---

## 18. 本轮 historical capture 尝试

### 18.1 候选 host

本轮根据同期/近同时期材料重点关注了：

- `www.12333sh.gov.cn` —— 上海劳动保障/人社公共服务历史 host；
- 上海历史医保相关 host（后来的材料常见 `www.shyb.gov.cn`）；
- 各省市人社/医保政府站中的异地就医指南；
- 2015 广东/深圳省内异地结算相关政府站点。

这些 host / URL 线索只是 **candidate locators**。

### 18.2 Wayback/CDX replay 本轮未升级为 verified capture

本轮尝试直接打开构造的 Wayback replay / CDX URL，例如：

- `https://web.archive.org/web/20100501000000/http://www.12333sh.gov.cn/`
- 针对 `www.12333sh.gov.cn/*` 的 2008—2015 CDX 查询；
- 针对 2015 深圳/广东相关 host 的候选 replay。

当前 Web 工具链明确拒绝未经搜索结果建立 provenance 的构造 archive URL。

因此严格记录：

**M1 verified historical cross-region-medical-insurance Web capture: NOT ACHIEVED IN THIS SLICE.**

这只表示：

`本轮没有实际打开并检查到合格的 memento`。

绝不能写成：

- “Wayback 没保存”；
- “这些网站当年不存在”；
- “archive 中不存在相关页面”；
- “当时没有网上服务”。

### 18.3 若以后成功 replay，最低记录字段

必须按 `docs/METHOD.md` 记录：

- `archive_source`；
- `capture_url`；
- `original_url`；
- `capture_datetime`；
- HTTP/回放状态；
- redirect/login/error/robots；
- Content-Type；
- charset；
- 主文档/附件；
- iframe；
- JS/form action；
- historical endpoint 是否仍然历史化；
- browser assumption；
- evidence grade。

---

## 19. 一个可复用的证据矩阵

| Claim | 最好证据 | 只靠什么不够 |
|---|---|---|
| 某地存在异地就医政策 | 同期正式政策 | 后来回忆 |
| 某网站公开异地指南 | verified historical capture + 同期官方说明 | 今天同 URL |
| 某表格当时可下载 | capture of page + attachment | 搜索摘要 |
| 某医院当时被列为异地定点 | 同期名单/政策 | 今天医院宣传 |
| 某医院系统已完成联网 | 同期官方上线记录 + 技术/使用证据 | “签约合作”新闻 |
| 某人确实使用 | 同期患者事务/一手材料 | 平台宣传 |
| 某次完成直接结算 | 医院/经办记录或可靠同期报道 | “持卡就医”帮助页 |
| 某次最终基金支付 | 权威结算/权益记录 | 前端成功页 |
| 某模式已经普及 | 规模统计 | “首例”“首家” |

---

## 20. 关键证据包

### E1 — 2008 四川新农合北京试点

事实：

- 两家北京医院成为四川新农合在京定点试点；
- 有真实务工者使用；
- 后续网络接口尚未完成；
- 患者仍需全额支付并寄票据回四川；
- 两个月仅少量患者使用。

Grade：**B+/B**。

意义：

`agreement != interface != direct settlement != adoption`。

### E2 — 2009 上海—嘉兴/杭州

事实：

- 嘉兴设上海医保代办窗口；
- 纸票据由工作人员跨地搬运；
- 上海—杭州铺设专用宽带，服务窗口前移；
- 有具体异地参保老人 10 分钟完成本地报销案例。

Grade：**B+**。

意义：

把“人工物流替代患者旅行”和“联网”分开。

### E3 — 人社部发〔2009〕190号

事实：

- 政策明确减少垫资、改进异地结算；
- 逐步实现就地就医、持卡结算。

Grade：**A**。

意义：

证明当时问题定义，不证明全国技术完成。

### E4 — 2011—2012 人社信息化

事实：

- 多省已有省内异地就医系统或省级大集中支持；
- 社保卡扩张。

Grade：**A/B+**。

意义：

证明后台数字网络早于统一公众 Web。

### E5 — 2015 广东平台

事实：

- 2015 年 10 月广东省异地直接结算平台上线；
- 11 月深圳接入。

Grade：**C+/A-（后来官方回顾）**。

意义：

作为主 scope 尾端的省级平台锚点。

---

## 21. 反例

### 21.1 “有医保就能异地报”——错误

参保只是必要条件之一。

### 21.2 “异地定点 = 当场刷卡”——错误

2008 四川—北京试点直接反证。

### 21.3 “联网 = 全数字无纸”——错误

2009 长三角可以联网辅助，却仍由患者/窗口持发票结报。

### 21.4 “社保卡全国统一 = 待遇全国统一”——错误

卡标准、数据互通和待遇政策是不同层。

### 21.5 “省内已经通 = 跨省也通”——错误

历史上两者差距可以很大。

### 21.6 “医院公告上线 = 每天稳定”——错误

任何 transaction system 都需要故障证据和 uptime 才能讨论稳定性。

### 21.7 “旧网页没有个人事务 = 当时没有个人事务”——错误

最关键的状态本就受登录和隐私保护。

---

## 22. 后见之明风险

### Risk A：把国家医保服务平台倒投到 2010

2010 的真实入口更可能是：

- 窗口；
- 纸表；
- 单位；
- 电话；
- 地方人社网站；
- 医院/经办专网。

### Risk B：把“异地医保”当一个统一产品名

不同地区、险种、时期可能是完全不同系统。

### Risk C：把 current official history 当 historical page

今天深圳医保专题回顾 2015 系统史是可靠的机构史证据，但不是 2015 DOM。

### Risk D：把新闻标题“无障碍”当真实无摩擦

必须进入正文看：

- 是否仍垫资；
- 是否仍拿发票；
- 是否只能某几家医院；
- 是否需提前备案。

### Risk E：把没有公开 capture 当没有后台

医保联网本来就大量发生在 public Web 之外。

---

## 23. 隐私与伦理边界

### 不追求

- 真实普通人的医保账户登录；
- 真实身份证号/社保卡号；
- 原始住院费用明细的批量再公开；
- 病种与身份的可识别关联；
- 私人报销材料镜像；
- 任何能重新识别历史患者的交易日志。

### 优先保存

- 公共政策；
- 空白表格；
- 页面结构；
- 字段 schema；
- 定点机构列表的历史快照；
- 软件/系统说明；
- 匿名化 transaction model；
- 已公开报道中的必要最小个人事实。

### 历史患者材料

同期新闻中的林强、陈瑞棠等个案只保留支撑研究机制所需的最少信息，不扩展搜索其私人生活。

---

## 24. Reconstruction 如果以后要做，应该复原什么

不应该伪造一名真实患者 2010 年的医保账户。

更安全、更有研究价值的是复原**事务壳**：

### Fixture A — 纸质异地安置

虚构身份：

`退休人员 / 参保地 A / 长期居住地 B`

展示：

- 空白登记表；
- 需要哪些证明；
- 如何指定医院；
- 哪些状态仍 offline。

### Fixture B — 2009 代办窗口

展示：

`医院付款`
→ `收集发票`
→ `B 地代办窗口`
→ `纸件物理移动`
→ `A 地审核`
→ `结果返回`。

### Fixture C — 2012 省内持卡

展示：

`card read`
→ `provincial eligibility lookup`
→ `expense upload`
→ `settlement response`。

所有数据必须 synthetic，并明显标 `reconstruction`。

---

## 25. 可加入未来 schema 的字段

```yaml
object_type: cross_region_medical_settlement
service_year:
insured_region:
care_region:
insurance_scheme:
care_type:
filing_required:
filing_channel:
referral_required:
provider_designation:
provider_network_status:
identity_medium:
public_web_url:
authenticated_host:
backend_topology_known:
expense_catalog_rule:
benefit_rule_region:
patient_advance_required:
settlement_mode:
  - manual_reimbursement
  - delegated_reimbursement
  - point_to_point_network
  - provincial_direct_settlement
  - unknown
paper_artifacts:
public_artifacts:
private_artifacts:
archive_capture_verified:
browser_assumption:
evidence_grade:
known_gaps:
```

这比一个简单的：

`has_online_settlement: true`

更符合历史现实。

---

## 26. 尚未确定

1. 2005—2007 最早一批地方异地医保专线/平台的精确技术拓扑仍缺统一清单。
2. 早期新农合跨省试点中，医院使用的软件、传输协议、数据库接口需要更强技术文档。
3. 2008—2010 上海/嘉兴/杭州代办与专网的具体历史 Web URL、charset、附件结构尚未取得 verified capture。
4. 2011—2013 各省“异地就医系统”中有多少属于 Web application、C/S 客户端、专线服务或核心系统模块，目前不能混写。
5. 2015 广东省平台的历史技术资料、接口标准和当时页面仍需进一步定位。
6. “即时结算”的医院端响应时延与后端资金清算周期不能从便民新闻直接推断。
7. 早期定点医院名单如何动态更新、旧页面是否调用当前数据库，需要 capture 级检查。
8. 患者个人纸质档案的 survival bias 尚缺系统样本，本文的 `administrative-success / paper-survival inversion` 目前是研究假设与机制判断，不是定量结论。

---

## 27. 本轮如何改变 old-Web 的解释框架

以前很容易把“政府网站出现一个办事入口”看成数字化的主要历史节点。

异地医保说明，真正影响普通人生活的变化经常不在 public Web 里：

- 2008 年两地政策已经合作，接口还没通；
- 2009 年专用宽带已经铺好，患者仍拿着发票；
- 2011 年省级平台已经开始支持持卡结算，普通人未必需要打开浏览器；
- 2015 年省级交换平台越来越成熟，但全国统一跨省系统还没有形成。

所以旧网考古以后研究这类公共服务时，不应只问：

> “这个页面长什么样？”

还应再问：

> **这个页面到底只是解释了一件线下事务，还是启动了一件私人事务；它启动以后，哪一步离开了 Web，进入地方数据库、专线、医院终端、纸件、电话和人工窗口；最终又在哪个系统里才真正算完成？**

异地医保尤其提醒我们：

**HTML 往往是最可见的一层，却可能是整个制度事务中最不决定结果的一层。**
