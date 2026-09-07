# Housing inventory, online signing, filing and occupancy state gaps (China, 2004–2015)

> Scope: 中文 Web / Web-adjacent 房地产交易基础设施，约 2004–2015。本文不写中国住房制度通史，也不把 1998 年房改扩成 old-web 主体；1998 只作为理解 2000s 商品住房与个人按揭为何需要更强信息/事务基础设施的边界背景。

生活史 companion：

- `tmzncty/how-people-lived/topics/searchable-housing-inventory-online-signing-debt-exit-and-homebuying-executability-china-1998-2026.zh-CN.md`

本篇与已有以下材料分工：

- `RENTAL_LISTING_ROOMMATE_AND_OCCUPANCY_STATE_GAPS_1998_2015.md` / rental docs：处理租赁与合租；
- `docs/CREDIT_APPLICATION_LOAN_PORTALS_INSTALLMENT_ENROLLMENT_AND_REPAYMENT_STATE_GAPS_2005_2008.md`：处理信贷页面、申请和还款；
- 本篇只处理**购买住房本身如何成为 Web / 官方数据库中的可寻址库存，以及网签、纸面签章、备案、登记、交付与实际入住之间的状态缺口**。

---

## 1. 研究问题

中文旧网里“房地产网站存在”太容易被写成一个模糊事实。

更具体的问题是：

1. 2004—2015 的某个页面究竟只是楼盘宣传，还是官方交易数据库？
2. 页面里一套房显示“可售”，是否意味着此刻真能买？
3. `网上签约`、`合同打印`、`双方签字`、`备案`、`产权登记` 是否属于同一个状态？
4. 一个 Web archive 如果保存了项目页，是否保存了动态楼盘表和房源状态？
5. 一个住房条目从数据库里消失，究竟意味着售出、撤销、下架、归档、权限变化还是 capture 缺失？
6. 住房已经买下，能否从 Web artifact 推断购房人已经入住？

本文的核心警告是：

> **housing page ≠ housing state ≠ household outcome**

---

## 2. 研究单位

按照 `docs/METHOD.md`，至少拆为：

- **platform / service**：例如“网上房地产”；
- **host**：例如 `www.fangdi.com.cn`、`www.bjfdc.gov.cn`；
- **project / building record**：楼盘或楼栋数据库对象；
- **unit record**：具体套号对应的数据库记录；
- **listing / entrusted listing**：二手房发布/经纪委托记录；
- **contract transaction**：一份网上签约；
- **filing state**：合同进入行政备案状态；
- **registration state**：权利登记/抵押等另一套行政状态；
- **page / URL**：项目页、楼盘表、查询页、操作说明；
- **capture**：档案在某个 datetime 保存的表示；
- **claim**：对某个历史时点的窄结论。

不能因为这些对象都围绕“同一套房”就把它们合成一个记录。

---

## 3. 2004 上海：从宣传页进入“官方交易库存”

2004 年 7 月 1 日的同期报道记录，上海新建商品房开始全部网上公开销售，长期使用的印刷商品房预销售合同停止使用，转为商品房网上交易系统；当时还计划公开楼盘最高/最低成交价格并规范开盘时点。

来源：

- 浙江在线 / 新浪，2004-07-01：<https://news.sina.com.cn/c/2004-07-01/19352963355s.shtml>

Evidence grade: **B**（同期媒体；不是原交易页 capture）。

这一变化至少支持一个窄 claim：

> 2004 年中，上海的商品房交易监管已经把新房库存、合同与公开 Web 信息进一步绑定，而不只是让开发商拥有自己的宣传网站。

但它不支持：

- 所有用户都在家里上网查房；
- 所有房源状态都实时准确；
- 所有交易步骤均在浏览器内完成；
- archive 今天仍能重放当时动态库存。

### 3.1 新增状态：`market supply / online inventory gap`

```text
physical / legally sellable stock
!= records currently present in Web database
```

原因可以包括：

- 上网滞后；
- 数据录入/同步延迟；
- 规避监管；
- 下架/撤销；
- 后台与公开前台不同步；
- archive 只保存静态壳页面而没有动态查询响应。

---

## 4. 2007 上海二手房：“全面触网”本身就留下数据库覆盖不足的反例

2007 年 1 月 1 日起，上海二手房交易开始全面网上备案。

2007 年 1 月 5 日《文汇报》同期观察：

- `www.fangdi.com.cn` 当时显示二手住宅出售约 14,803 套；
- 普通住宅约 12,019 套；
- 住宅出租约 1,805 套；
- 记者明确写明，网上 1 万多套挂牌房源仍与真实二手房市场供应“相距甚远”。

来源：

- 文汇报 / 新浪，2007-01-05：<https://finance.sina.com.cn/roll/20070105/07441137088.shtml>

Evidence grade: **B**（同期平台观察）。

2007 年 1 月 3 日另一份同期报道同样指出，网上挂牌仍少于实际市场供应，并记录一名中介对备案系统调试阶段的负面体验。

来源：

- 解放日报 / 新浪，2007-01-03：<https://news.sina.com.cn/o/2007-01-03/090010916268s.shtml>

Evidence grade: **B**。

### 4.1 为什么这条负证据特别重要

它阻止一种常见考古错误：

```text
archived database count
→ 被当成当时市场总量
```

即使未来取得 2007-01-05 的完整页面 capture，也最多先证明：

> 该系统在该时刻对该查询公开了这些记录。

它不能自动证明：

> 上海当时只有这些房子在出售。

这就是 **database coverage gap**。

---

## 5. 2007：备案号开始成为房源在多个媒介之间的事务键

2007 年 1 月 23 日的同期报道记载，上海房地管理部门酝酿要求经纪机构在报纸等媒体发布房源时标注网上备案号；截至报道前一日：

- 2,247 家房地产经纪机构通过网上资格认证；
- 3,176 家分支机构；
- 10,795 名经纪人；
- 经纪委托合同网上备案 64,943 份；
- 累计发布房源 34,304 套；
- 网上签订房地产交易合同 10,632 套。

来源：

- 解放日报 / 新浪，2007-01-23：<https://finance.sina.com.cn/roll/20070123/09001173390.shtml>

Evidence grade: **B**。

这里出现的是 **cross-medium transaction key（跨媒介事务键）**：

```text
报纸/媒体广告
      ↓ 备案号
官方在线记录
      ↓
经纪委托 / 房源 / 交易合同
```

旧网考古以后应主动寻找：

- 页面上的备案号字段；
- 报纸广告中的相同号码；
- 经纪机构页面中的号码；
- 是否能由多个 artifact 交叉确认同一套房源。

但涉及普通个人联系方式、业主姓名等时必须遵守最小化原则，不为了“拼完整交易”重新公开私人信息。

---

## 6. 2008 北京：一个官方流程明确证明 `online signing != paperless completion`

北京市住房和城乡建设部门 2008 年 4 月 29 日发布通知，自 2008 年 6 月 1 日起实行商品房预售合同网上联机备案。

官方流程明确是：

```text
买卖双方确认条款
→ 在交易权属管理系统网上签约
→ 开发企业网上打印合同
→ 买卖双方在纸上签字、盖章
→ 开发企业网上联机备案
→ 打印备案表交购房人
→ 用户凭签约密码查询备案情况
```

来源：

- 北京市住房和城乡建设委员会，2008-04-29：<https://zjw.beijing.gov.cn/bjjs/fdcjy/wqht/spfysxswqlc/743809748/index.shtml>

Evidence grade: **A**（同期官方制度与操作说明）。

同一官方通知还规定：

- 解除合同需要相关原件与身份证明等材料；
- 部分继承、遗赠、离婚、夫妻更名等变更仍需到房管部门办理；
- 已办理期房抵押登记的住房解除合同前可能先要处理抵押注销。

这证明早期“网签”至少包含一条明显的 **paper–digital braid（纸—网编织）**。

### 6.1 新增 gap

`online-sign / paper-execution gap`

```text
网上已生成/确认合同
!= 纸面签字盖章已完成
```

`paper-execution / filing gap`

```text
纸质合同双方已经签完
!= 开发企业已经完成网上备案
```

`filed / registered-right gap`

```text
预售合同已备案
!= 最终产权/转移登记已完成
```

`filed / mortgage-state gap`

```text
合同已备案
!= 贷款已审批 / 已放款 / 抵押登记已完成
```

`purchase / occupancy gap`

```text
合同与贷款都已生效
!= 房屋已交付
!= 家庭已经入住
```

---

## 7. 一套住房应被当成多状态对象，而不是一个 URL

建议 future evidence schema 为住房案例保留以下状态字段（不要求每个城市/年份都有全部状态）：

```text
project_visible
unit_visible
unit_marked_available
listing_authorized
broker_authorized
viewing_contact_available
reservation_created
online_contract_created
paper_contract_signed
filing_submitted
filing_confirmed
mortgage_applied
mortgage_approved
mortgage_funded
mortgage_registered
transfer_registered
construction_complete
delivered
occupied
contract_cancelled
listing_withdrawn
```

特别是预售住房，`contract_date` 与 `occupancy_date` 可能相隔很久。

因此历史叙述不要写：

> “某人 2006 年买房，所以 2006 年开始住在这里。”

除非另有交付/入住证据。

---

## 8. Page / backend / real-world state matrix

| Artifact | 最多直接证明什么 | 不能自动证明什么 |
|---|---|---|
| 楼盘宣传页 | 项目被这样宣传 | 房源真实可售、价格真实、用户实际看过 |
| 官方楼盘表 | 某时点系统公开某种 unit state | 市场全部库存、后台实时无延迟 |
| 二手挂牌 | 有一条公开 listing | 业主仍愿出售、委托仍有效、最终成交 |
| 网签查询结果 | 系统返回一份签约/备案状态 | 纸合同全部有效、贷款已放款、产权已登记 |
| 合同备案页 | 一项行政备案存在 | 家庭已入住、交易没有后续解除 |
| 新闻报道中的统计数 | 当时媒体/机构报告该数量 | 原数据库 query 的完整参数与页面形态 |
| 房贷产品页 | 当时产品规则/宣传 | 某位购房人的贷款审批和实际放款 |
| archive capture | 该 archive 在 capture_datetime 保存某表示 | 原站所有动态子资源、用户当年看到完全相同结果 |

---

## 9. `visible / available / executable` 必须拆开

对住房数据库至少使用以下阶梯：

### exists

某个项目/房源记录存在。

### visible

普通 Web 用户在某一界面能看到。

### available

该房源在当时制度和市场条件下仍可出售/出租。

### reachable

用户能联系到发布者、中介或开发商。

### eligible

购买人满足当地购房、贷款等资格。

### executable

首付、签约、身份材料、贷款、备案等都能走通。

### completed

交易和权利状态最终完成。

### occupied

房屋真正进入家庭日常生活。

这几级不能互相替换。

---

## 10. 历史 locator

本轮可以确认至少有以下历史 locator 出现在同期材料：

- `www.fangdi.com.cn` — 2007 上海“网上房地产”同期报道明确引用；
- `www.bjfdc.gov.cn` — 2008 北京同期报道/交易管理说明出现的房地产交易管理网历史 host。

这些 locator 现在只能作为**历史地址线索**。

不能因为今天域名/网站仍存在或被迁移，就推断：

- 2004、2007、2008 的 URL path 没变；
- 页面模板没变；
- 数据库 API 没变；
- 当时同样支持 HTTPS；
- 原动态结果已经被 archive 保存。

---

## 11. Archive / M1 status

### M1: NOT ACHIEVED IN THIS SLICE

本轮获得了：

- 2004 上海网上交易的同期媒体证据；
- 2007 上海二手房网上备案、库存覆盖不足、经纪机构资格和合同数据的同期报道；
- 2008 北京住建部门保存的明确网签/打印/签章/备案官方流程；
- 历史 host locator。

但本轮**没有实际取得并检查一份满足仓库 METHOD 的 2004—2010 历史 Wayback/WARC replay response**。

因此以下内容保持 `unknown`：

- 2004 `fangdi.com.cn` 的原始 HTTP headers；
- historical charset（GB2312 / GBK / UTF-8 等）；
- 原始 DOM / frameset / table layout；
- JS / form action / query parameter；
- session / cookie；
- 房源颜色图例当年具体 HTML/CSS 实现；
- 动态楼盘表是否由 archive 捕获；
- 后端库存刷新频率的实际实现；
- 中介/开发商登录后台界面；
- 浏览器最低版本/IE-only 条件；
- TLS/非 TLS 状态；
- 撤销、下架、修改房源在原系统里的历史呈现；
- 查询失败、超时、数据库维护等负状态页面。

正确结论是：

> **本轮尚未验证 historical capture。**

不能写成：

> **Wayback 没有。**

搜索 locator 也不等于已经验证 capture。

---

## 12. Browser / environment assumptions

在取得原始 capture 前，禁止默认：

- modern Chromium 可正确表示当年页面；
- 当前页面的 UTF-8 能代表 2004 页面编码；
- 当前 CSS/JS 与当时一致；
- 动态楼盘表在 archive replay 中会继续工作；
- 现代 HTTPS 跳转与历史 HTTP 原站相同；
- 页面上今天看到的颜色/图例就是 2000s 原设计。

如果未来拿到 artifact，优先记录：

1. `Content-Type` / charset；
2. table / frameset / script 依赖；
3. IE browser sniffing；
4. 动态查询是 GET、POST 还是 iframe/JS；
5. 图片/图例是否缺失；
6. archive rewrite 是否破坏 query；
7. unit record 是否拥有稳定 URL。

---

## 13. Historical visibility asymmetry

住房交易系统会制造大量官方记录，却仍然只保存生活的一部分。

### 更容易留档

- 项目/楼栋；
- 房源字段；
- 备案号；
- 经纪机构资格；
- 网上签约/备案；
- 成交价格统计；
- 操作通知；
- 贷款/登记制度规则。

### 更容易消失

- 用户搜索了什么却没有点击；
- 看过哪些房最后没买；
- 售楼处口头说了什么；
- 私下谈价；
- 父母如何决定出首付；
- 贷款被拒的真实理由；
- 为什么取消认购；
- 交付延期对婚期、工作地点的影响；
- 房子最后由谁长期居住。

因此存在：

> **archived housing record / lived household gap**。

Web 可能保存一套房，却完全没有保存“这个家后来怎么过”。

---

## 14. 负状态尤其值得保存

未来如果取得历史 artifact，应主动寻找：

- `已售 / 不可售 / 已签 / 已备案`；
- `撤销`；
- `合同解除`；
- `挂牌失效`；
- `重复房源`；
- `无查询结果`；
- `系统维护`；
- `数据库同步延迟`；
- `备案失败`；
- `权限不足`；
- `密码错误`；
- `项目停售`。

只保存“成功页面”会把旧网重建成一种过度顺滑的世界。

---

## 15. 证据表

| Claim | Evidence family | Grade | Confidence | Boundary |
|---|---|---:|---|---|
| 2004 上海新建商品房进入网上公开销售/交易系统 | 同期浙江在线/新浪 | B | high | 没有原页面 capture |
| 2007 上海二手房全面网上备案 | 同期文汇报/解放日报 | B | high | 城市制度，不外推全国 |
| 2007 初网上挂牌明显少于实际市场供应 | 同期记者观察 | B | high | 只证明早期覆盖 gap |
| 2007 经纪资格、委托、房源、合同均进入网上事务链 | 同期解放日报 | B | high | 数量为报道时点快照 |
| 2008 北京网签后仍需打印纸合同、签字盖章再网上备案 | 北京住建委官方通知 | A | high | 流程存在不等于每笔顺利完成 |
| 合同解除/部分变更仍可能需要线下原件 | 北京住建委官方通知 | A | high | 只针对该制度/时期 |
| 原历史页面 DOM/charset/browser 形态 | 未验证 capture | — | unknown | 不推断 |

---

## 16. Counterexamples / hindsight risks

### 不要写“2004 以后上海买房就透明了”

同期材料已经出现平台覆盖不足和市场参与者规避/适应系统的问题。

### 不要写“2008 北京已经电子合同无纸化”

官方流程明确要求打印、签字、盖章。

### 不要把官方数据库计数当成市场普查

2007 的同期材料直接证明 online inventory 可以少于实际供应。

### 不要把一套房的备案日期当入住日期

预售住房尤其危险：购房人可能已经开始还贷一年以上，却仍未交付。

### 不要用今天仍在线的政府旧通知页面代替历史 UI

当前政府站保留的是**内容/制度文本**，不是 2008 年浏览器、URL、HTML、CSS 和 backend 的原始 artifact。

---

## 17. 下一步最值得做的 archive work

1. 对 `www.fangdi.com.cn` 枚举 2004、2007 两个窄时间窗的 verified captures；
2. 先检查静态首页/帮助页，再尝试动态楼盘表，而不是直接假定 query 可回放；
3. 对 `www.bjfdc.gov.cn` 查 2008-06 前后帮助页和楼盘表 capture；
4. 记录每个 candidate capture 的 `original_url / capture_datetime / HTTP replay state / charset / subresource loss`；
5. 若动态房源不可复原，明确记录 `backend dark matter`，不要用现代站点补画；
6. 寻找 2007—2010 BBS/博客里普通购房人怎样使用“网上房地产”、备案密码、楼盘表和网签查询；
7. 比较媒体中的“可售/已售/备案颜色”描述与实际 capture；
8. 只在取得合格 capture 后，才考虑把该对象升级成 M1 完整案例。

---

## 18. 本轮增加的 old-Web 理解

旧中文 Web 不只是“房地产广告搬到了网上”。

更重要的一步是：

> **现实中的一套房开始拥有一个可查询的数字状态，而这个状态逐渐成为签约、备案、监管和媒体发布之间的共同接口。**

但这也制造了新的考古陷阱。

未来研究者可能看到一个极其整齐的楼盘表，以为 2007 年的市场也像数据库一样完整；看到“网签”，以为那天纸已经消失；看到合同备案，以为家庭已经搬进去。

实际链路更像：

```text
房子存在
→ 进入数据库
→ 被普通用户看见
→ 仍然可售
→ 现场看房
→ 家庭筹资
→ 网上签约
→ 纸面签章
→ 网上备案
→ 贷款/抵押
→ 登记
→ 交付
→ 入住
```

**旧网真正保存下来的，只是这条链里比较容易被系统记录的几个状态。**
