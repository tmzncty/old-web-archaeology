# 个人所得税自行申报：Web 填报、身份确认、受理与税款结算状态缺口（2006—2015）

> Scope：只研究约 2006—2015 年中文 Web 上的**个人所得税自行申报/网上办税接口及其状态边界**。1980—2005 的税制史只作为必要前史；2019 年后的“个人所得税”App 与综合所得年度汇算不纳入本仓主对象，只在 companion life-history note 中讨论。
>
> Companion：[`tmzncty/how-people-lived/topics/from-payroll-withholding-to-fiscal-self-administration-personal-tax-filing-and-family-data-china-1980-2026.zh-CN.md`](https://github.com/tmzncty/how-people-lived/blob/main/topics/from-payroll-withholding-to-fiscal-self-administration-personal-tax-filing-and-family-data-china-1980-2026.zh-CN.md)

本题不是“电子政务网站怀旧”。它要回答的是：2007 年一个页面写着“网上申报”，到底能证明到哪一步？

---

## 1. 研究单位与最小 claim

研究单位不是“税务网站”这个品牌，而是一次个人年度自行申报可能穿越的若干对象：

- 公告/帮助页；
- 网上办税入口；
- 个人登记/预登记；
- 身份证明上传或线下确认；
- 密码/凭据；
- 申报表；
- 提交请求；
- 服务器受理状态；
- 受理回执；
- 更正申报；
- 补税/退税结算；
- 税务机关后台记录。

最小 state machine：

```text
法律上属于自行申报人
→ 找到主管税务机关
→ 找到 Web 入口
→ 完成登记/预登记
→ 身份状态可被系统接受
→ 获得/设置登录凭据
→ 进入申报表
→ 填入年度所得和已纳税额
→ 点击提交
→ 服务端实际接受
→ 生成/可下载受理回执
→ 必要时更正
→ 补税/退税完成
→ 后台年度记录最终落定
```

因此固定：

```text
portal exists ≠ taxpayer eligible
form visible ≠ authenticated session
pre-registration ≠ identity confirmed
submit click ≠ server acceptance
accepted declaration ≠ tax settlement
online declaration ≠ fully remote completion
withholding completed ≠ annual self-declaration completed
receipt generated ≠ taxpayer actually saved it
```

---

## 2. 2006—2007：法律上的“自行申报”怎样变成 Web workflow

2006 年国家税务总局《个人所得税自行纳税申报办法（试行）》规定，年所得 12 万元以上，以及两处以上工资薪金、境外所得、无扣缴义务人等情形，需要自行向税务机关申报；总局同年又要求有信息化条件的税务机关完善受理软件，并建议通过网络、邮寄等方式减少直接到办税服务厅的人数。

A 级制度来源：

- 国家税务总局：《个人所得税自行纳税申报办法（试行）》：<https://zhejiang.chinatax.gov.cn/art/2006/11/6/art_8409_16071.html>
- 国家税务总局：《关于做好受理年所得12万元以上纳税人自行纳税申报工作的通知》：<https://zhejiang.chinatax.gov.cn/art/2006/11/6/art_8409_10917.html>

这只能证明**制度要求和系统建设方向**，不能单独证明每个地方的 Web 入口当时都能稳定完成 transaction。

---

## 3. 广东 2007：一个罕见地保存了“预登记—凭据—预申报—线下确认”细节的同期对象

2007 年 1 月 15 日，广东全省统一的个人所得税网上办税应用系统上线。同期报道给出的 historical locator 是：

```text
http://www.gdltax.gov.cn/wsgs
```

报道所保存的流程比一句“可以网上报税”丰富得多：

1. 纳税人进入“个人所得税自行申报”；
2. 可进行预登记；
3. 上传个人身份证明文件；
4. 设置密码；
5. 有扣缴义务人的纳税人，可通过扣缴义务人取得网上查询密码，并在首次申报时修改；
6. 没有扣缴义务人或此前未在税务机关登记的人，要填写个人登记信息、自编密码；
7. 后一类纳税人还需在规定时间到主管税务机关完成首次申报确认；
8. 系统另提供申报查询、缴款查询和历史申报数据查询。

B 级同期来源：

- 《广东省个人所得税网上办税应用系统正式上线运行》，新快报/新浪财经，2007-01-17：<https://finance.sina.com.cn/roll/20070117/09321161258.shtml>
- 《个人网上办税系统开通》，深圳商报/新浪财经，2007-01-17：<https://finance.sina.com.cn/roll/20070117/08311160626.shtml>
- 广州市地税局 2007-02-12 网上申报辅导通知（后由现税务域名保存）：<https://guangdong.chinatax.gov.cn/gdsw/sffggzs/2018-07/05/content_fa05889619224c7cb5064d6831054597.shtml>

### 新状态缺口：credential provenance / 凭据来源缺口

同一个“个人网上申报账号”并不一定完全由本人在线自助创建。同期流程里，凭据可能经过扣缴单位、既有税务登记或线下主管机关。

因此：

```text
personal login ≠ purely personal provisioning
```

这很适合 old-Web 考古，因为今天看到一个登录框，无法从页面外观判断账号究竟如何被发放、由谁初始化、第一次登录前是否已发生线下身份绑定。

---

## 4. 上海 2007—2008：Web 入口存在，但“远程闭环”被明确切断

上海 2006 年底发布的操作意见规定，采用网上申报方式的纳税人，应先在申报期内到主管税务机关办税服务厅办理网上申报申请。采用网上申报的，之后可以从上海税务网站自行下载《年所得12万元以上纳税人网上申报受理回执单》。若填错需要重新申报，要重新全额填表，税务机关以最后一次报送的申报表为准，之前报送的自动作废。

A 级来源：

- 上海税务：《关于本市贯彻落实〈个人所得税自行纳税申报办法（试行）〉的操作意见（暂行）》，2006-12：<https://shanghai.chinatax.gov.cn/zcfw/zcfgk/grsds/200612/t288896.html>

2008 年徐汇区和上海市层面的公告又说明：

- 可选择网上、邮寄、办税服务厅、委托代理；
- 网上申报仍需先到办税服务厅办理申请；
- **不涉及补缴/退还税款**时，可网上或邮寄申报；
- **涉及补缴/退还税款**时，应到主管税务机关办税服务厅办理。

A 级来源：

- 徐汇区税务局，2008-02-28：<https://shanghai.chinatax.gov.cn/xhtax/tzgg/tzl/200802/t351712.html>
- 上海税务，2007-12-27 公告：<https://shanghai.chinatax.gov.cn/xhtax/tzgg/tzl/200801/t351708.html>

这直接建立三个不能合并的状态：

```text
online filing eligibility
≠ online registration completed
≠ online settlement completed
```

一个 archive capture 即使能证明历史页面有“网上申报”入口，也最多先证明 **front-end availability**；不能自动宣称税款结算、身份确认和异常更正都已在 Web 上闭环。

---

## 5. 申报状态不是“一次提交后永远固定”

上海操作意见规定，申报期内若因填写错误需要重新申报，应全额重填，后台以最后一次报送的申报表为准，之前报送的自动作废。

这产生一个容易被 archive 忽略的 **mutable declaration state / 可变申报状态**：

```text
submitted_v1
→ accepted_v1
→ taxpayer detects error
→ submitted_v2
→ accepted_v2
→ v1 invalidated
```

所以历史截图里一张“已申报”回执并不一定是该纳税年度最终状态。研究者如果只找到一份早期回执或帮助页，不能推断最终申报金额与结算结果。

---

## 6. 同期第一人称：页面能打开，不等于普通人理解怎样填写

2009 年成都一名年收入超过 12 万元的机构中层“孙先生”接受同期采访时说，自己的个税每个月已经由单位代扣，仍不理解为什么还要再申报；他查过网上表格后又担心，非财务人员要在短时间内自己算清各类收入、纳税额和应补/应退并不容易。

B 级来源：

- 新华网稿件的搜狐转载，2009-01-13：<https://business.sohu.com/20090113/n261720411.shtml>

这个材料证明的是 **form-availability / form-comprehension gap**，而不是“纳税人普遍不会用互联网”。

```text
field exists
≠ user knows what counts in that field
```

在 old-Web 重建里，文本框的视觉复原尤其容易制造一种假象：仿佛只要所有 input 都显示出来，历史 task 就已被复原。实际上，业务定义、计算规则、单位财务提供的信息和咨询渠道本身也是 transaction stack 的一部分。

---

## 7. 一个更完整的 2007—2015 个税 Web 状态模型

### 7.1 Eligibility state

- `withholding_only`
- `self_declaration_required`
- `self_declaration_optional/other route`
- `unknown`

### 7.2 Authority-routing state

- `主管税务机关 known`
- `主管税务机关 uncertain`
- `wrong authority / redirected`

历史帮助页常把“向主管税务机关申报”写得很简单，但换工作、多收入来源或跨区域居住可能让 routing 本身成为劳动。

### 7.3 Registration / credential state

- `not_registered`
- `pre_registered`
- `identity_material_uploaded`
- `credential issued by withholding agent / authority`
- `password initialized`
- `first-login password changed`
- `offline confirmation still required`
- `active`

### 7.4 Filing state

- `blank`
- `draft/pre-declaration`
- `submit_attempted`
- `server_accepted`
- `receipt_available`
- `corrected/resubmitted`
- `superseded`

### 7.5 Settlement state

- `no additional payment/refund`
- `tax_due`
- `refund_due`
- `offline settlement required`
- `payment initiated`
- `payment cleared`
- `refund initiated`
- `refund received`

### 7.6 Archive-observable state

- `public notice only`
- `help page`
- `login shell`
- `form shell`
- `authenticated transaction unavailable`
- `receipt example only`
- `verified historical transaction capture`

目前本题证据最多推进到前五类中的前几层，**尚未取得最后一类 M1 级 transaction capture**。

---

## 8. 旧网保存偏差：policy-page survival / private fiscal-state darkness

税务网站特别容易形成一种保存不对称：

### 容易留下

- 政策公告；
- 申报期限；
- 表格下载；
- 操作说明；
- 登录入口壳；
- 新闻报道里的 URL；
- 后来迁移到 `chinatax.gov.cn` 的旧文件正文。

### 很难留下，也不应该为了研究重新公开

- 真实身份证明上传件；
- 纳税人密码；
- 真实申报表；
- 收入明细；
- 单位扣缴记录；
- session/cookie；
- 后台审核；
- 补税/退款银行账户；
- 最终年度个人财政状态。

因此命名为：

**public fiscal shell / private settlement state asymmetry——公开财政壳层 / 私人结算状态不对称。**

它会导致一种历史错觉：后人可以非常清楚地看到“网上申报已经上线”，却看不到有多少人卡在预登记、密码、主管机关、首次确认、计算、服务端失败或线下补退税。

---

## 9. 域名迁移也是证据问题

2007 年同期材料给出的原始 locator 包括：

```text
www.gdltax.gov.cn/wsgs
www.tax.sh.gov.cn
www.csj.sh.gov.cn
```

今天很多 2006—2009 的制度文件还能在新的 `chinatax.gov.cn` 省市税务域名下读到。这些页面可以作为**旧文件内容的机构性迁移/再发布来源**，但不能把当前 URL 的 DOM、CSS、HTTPS、charset、JS 或发布时间显示方式倒推成 2007 年原站技术状态。

因此必须分：

```text
historical document content survives
≠ historical page survives
≠ historical transaction endpoint survives
```

---

## 10. Browser / encoding / security unknowns

本轮未取得可验证原始 capture，因此以下全部保持 unknown：

- `gdltax.gov.cn/wsgs` 2007 年真实 HTTP `Content-Type` 与 charset；
- 是否 GB2312 / GBK / UTF-8；
- 表单是普通 HTML POST、frameset、JS 提交还是其他结构；
- 身份证明上传字段的 MIME/大小限制；
- IE 版本要求；
- ActiveX / Java / 客户端证书是否参与某些地区流程；
- cookie/session 生命周期；
- 密码找回流程；
- 服务端 validation error 文案；
- 高峰期 timeout / duplicate-submit 行为；
- 网上缴款真正跳转到什么支付/银行接口；
- 回执是 HTML、可打印页、PDF 还是其他格式。

现代浏览器今天能打开迁移后的政策页，不能填这些空白。

---

## 11. Evidence table

| Claim | Evidence | Grade | Confidence | Boundary |
|---|---|---:|---|---|
| 2007 年起特定个人需要年度自行申报 | 国家税务总局 2006 办法 | A | high | 制度存在不等于每人 Web 自报 |
| 广东 2007-01 有全省统一网上自行申报系统 | 同期媒体 + 广州地税后存文件 | A/B | high | 尚无原 transaction capture |
| 广东流程含预登记、身份材料、密码、部分线下首次确认 | 2007 同期报道 | B | medium-high | 精确 UI / 后台 unknown |
| 上海网上申报需先办理申请 | 上海税务同期制度文件 | A | high | 不证明实际等待时间 |
| 上海部分补退税事务仍需柜台 | 上海税务 2007-12 公告 | A | high | 只适用于该时点/地区规则 |
| 更正申报可使此前申报自动作废 | 上海同期操作意见 | A | high | 后台实现细节 unknown |
| 非财务人员可能理解字段困难 | 2009 同期个人采访 | B | medium | 个案不能外推全体 |

---

## 12. 反例清单

1. **“网站上能报税，所以不用去税务局。”** —— 2007—2008 上海/广东都有明确混合流程反例。
2. **“单位已经扣税，所以个人不用报。”** —— 12 万元以上规则就是反例。
3. **“登录成功就代表身份确认完成。”** —— 预登记、凭据来源、首次确认可分离。
4. **“提交成功就代表税款结清。”** —— 申报和 settlement 是两套状态。
5. **“一份历史回执就是最终申报。”** —— 更正申报可 supersede 旧版本。
6. **“当前官方站保存了旧文件，所以当前页面就是当年页面。”** —— institutionally migrated content 不是 historical DOM。

---

## 13. Privacy stop condition

个税历史 transaction 天然涉及高度私人财政信息。本题不会为了填补 archive gap 去寻找、拼接或重新公开：

- 普通人的身份证号；
- 完整收入明细；
- 真实申报账号；
- 税务密码；
- 银行账户；
- 泄露申报表；
- 未公开后台数据。

即使某个历史缓存或泄露数据可访问，也不构成重新传播的研究必要性。优先使用官方帮助页、匿名化示例、制度文件和同期操作报道。

---

## 14. M1 archive status：负结果

本轮已经定位到 `www.gdltax.gov.cn/wsgs`、`www.tax.sh.gov.cn`、`www.csj.sh.gov.cn` 等 historical locators，并取得多个 2006—2009 同时代 A/B 级制度与新闻来源。

**但本轮没有取得并实际检查一份满足本仓 M1 门槛的 2007—2010 个人网上报税 Wayback/WARC transaction capture。**

因此目前不能声称已经验证：

- 原始 DOM；
- capture datetime；
- 原始 charset；
- form action；
- authenticated flow；
- server acceptance；
- 真实回执；
- payment/refund handoff。

这不是“研究没完成所以随便补”的空白，而是本题的正式 archive gap。

---

## 15. 本轮新增的旧网解释

个人税务 Web 很适合作为“网页存在 ≠ 生活任务已数字化”的强案例。

2007 年一个普通使用者面对的不是单一网站，而是：

```text
单位财务
+ 税务规则
+ 主管机关
+ Web 入口
+ 身份材料
+ 密码
+ 年度收入分类
+ 申报回执
+ 柜台/邮寄 fallback
+ 补退税结算
```

因此对中文旧网的一个新判断是：

> **旧电子政务页面真正要考古的，不只是“按钮长什么样”，而是这个按钮究竟把制度劳动从柜台搬走了多少，又留下了多少必须在网页之外继续完成。**

---

*AI-assisted research note. Historical originals, current institutional migrations, contemporary secondary reporting, inference and unknown transaction states are kept separate.*
