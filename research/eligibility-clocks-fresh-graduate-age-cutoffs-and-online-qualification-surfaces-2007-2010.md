# 招聘 Web 的“资格时钟”：应届分类、年龄日期窗与在线资格审查证据边界（2007–2010）

> Status：focused research checkpoint，后续应折回：
>
> - `CIVIL_SERVICE_ONLINE_REGISTRATION_QUALIFICATION_PAYMENT_ADMIT_CARD_AND_HIRING_STATE_GAPS_2004_2015.md`
>
> Cross-repo life-history slice：
>
> - `tmzncty/how-people-lived/sources/eligibility-clocks-fresh-graduate-status-age-cutoffs-and-cohort-gated-opportunities-china-1997-2026.zh-CN.md`
>
> 本文**不是**再写一篇“资格审查通过 ≠ 最终录用”的近义 state-gap。现有 canonical note 已充分覆盖报名、确认、支付、准考证、考试、面试、体检和录用链。本 checkpoint 只补一个旧 Web 方法缺口：**现实人生里的毕业年份、档案位置、是否就业和出生日期，怎样被压成一个在线招考系统可以处理的资格分类；历史公告又能证明到哪一步。**

---

## 1. 为什么这是 Web archaeology，而不只是就业政策史？

早期网上报名把现实中的资格判断接进了 Web 事务。

典型链条不是：

```text
打开页面
→ 填表
→ 报名成功
```

而是：

```text
现实事实
  - 出生日期
  - 毕业年份
  - 学历
  - 户籍 / 生源
  - 档案在哪里
  - 是否落实工作单位
  - 工作经历到哪一天

→ 用户在报名表中声明 / 提交材料
→ 系统保存 candidate record
→ 招录机关按职位规则做资格审查
→ candidate 获得“可继续报名确认”的状态
→ 后续仍可能纸面 / 原件复审
```

这意味着旧网考古如果只保存公开职位表，会遗漏：

- 用户当时如何表达自己的身份；
- 哪些字段来自本人声明；
- 哪些状态要靠学校、档案、人事记录或证件核验；
- 哪些规则由代码执行；
- 哪些规则由人审核。

---

## 2. 2007 深圳：公告已经把“应届”写成多变量 predicate

深圳市 2007 年上半年公务员招考公告明确区分：

- 2006、2007 年毕业，户籍和档案仍留在学校且未落实工作单位者，可按应届毕业生报考；
- 已落实工作单位的 2007 届毕业生在特定条件下仍可进入不同职位池；
- 深圳院校 / 深圳生源又有本地规则；
- 2006 年已分配派遣者以及 2005 年以前毕业者，在相应条件下只能进入社会人员职位；
- 港澳及国外留学归来人员以“毕业不超过一年 / 超过一年”区分应届与社会人员。

同一公告还把一般年龄条件换算成精确出生日期范围，并指定工作经历的统一截止日期。

同期来源：

- 深圳市人民政府，2007-06-29：
  https://www.sz.gov.cn/cn/xxgk/zfxxgj/tzgg/content/post_1614614.html

Evidence：**A-content / contemporaneous government notice**。

### 2.1 新的考古单位：policy predicate

这里需要单独增加一种研究对象：

## policy predicate（政策判定式）

例如：

```text
(graduated in 2006 or 2007)
AND (archive/hukou retained in school)
AND (no job unit implemented)
→ treat as fresh graduate for this recruitment path
```

它和 Web form 不是同一个东西。

### 必须硬分：

```text
policy predicate exists
!= form contains all predicate fields
!= browser validates predicate
!= server automatically validates predicate
!= human reviewer applies predicate correctly
!= later original-document review agrees
```

当前证据只强力证明**规则存在并需要在报名/资格审查流程中被处理**。

没有证据证明 2007 深圳报名后台已经把上述全部条件写成自动规则引擎。

---

## 3. exact date window ≠ verified automated age check

2007 深圳公告把 18–35 岁直接换算为一段出生日期区间；不同职位还可以有 30 岁、25 岁等更窄窗口。

类似做法在 2009 年国家公务员公告中同样存在：

- 18–35 岁；
- 同时把它翻成具体年月日期范围。

来源：

- 2009 年度中央机关及其直属机构招考公告（2008-10-14，民航局政府镜像）：
  https://www.caac.gov.cn/PHONE/XXGK_17/XXGK/RSXX/201510/t20151029_4383.html

Evidence：**A-content government mirror of contemporaneous announcement**。

这类日期窗对用户体验有直接影响：

> “35 岁以下”不再只是口头类别，而是能被明确映射到生日字段的一条边界。

但旧网复原必须禁止下一步偷跳：

> “公告写了出生日期范围” **不能证明** 历史网页 JavaScript 或服务器已经自动拒绝越界生日。

要证明自动检查，至少需要其中之一：

- 历史 form / HTML / JavaScript；
- 原系统操作手册；
- 同期用户实际报错记录；
- 服务器端接口/软件文档；
- 可复核的历史 capture 显示提交后的错误状态。

本轮均未取得。

---

## 4. 2008–2009：我们能验证“网上确认有先决状态”，但仍不能看见资格引擎

2009 年国家公务员考试多地网上确认说明明确要求：

1. 考生此前已经完成网上报名；
2. 已经通过资格审查；
3. 选择了相应考区；
4. 再进入地方确认系统上传照片、缴费等。

例如：

- 江苏考区确认说明：
  https://edu.sina.com.cn/official/2008-11-03/1555173116.shtml
- 西藏考区确认说明：
  https://edu.sina.com.cn/official/2008-11-03/1610173122.shtml
- 浙江考区确认说明：
  https://edu.sina.com.cn/official/2008-11-03/1600173117.shtml

Evidence：**B+，地方考试机构同期操作说明经媒体保存。**

这能证明一种服务器/业务状态链：

```text
application submitted
→ qualification review passed
→ local confirmation becomes applicable
```

但仍然不知道资格审查具体怎样完成：

- 哪些字段自动比较；
- 哪些由招录机关工作人员看报名表；
- 哪些需要外部材料；
- 是否有批量审核后台；
- 是否存在自动年龄计算；
- “应届”分类是否由用户自选、系统推导，还是审核员改写。

所以本 checkpoint 增加一个长期字段：

```yaml
qualification_execution:
  policy_rule: known/unknown
  user_declared_fields: known/unknown
  client_validation: known/unknown
  server_validation: known/unknown
  human_review: known/unknown
  external_record_dependency: known/unknown
  later_document_recheck: known/unknown
```

未知必须保留 `unknown`。

---

## 5. 2009 江西：线下档案位置仍能决定线上招聘里的“应届”资格

2009 年江西公务员招录同期说明记录：毕业后两年择业期内未落实工作单位，并且户口、档案、组织关系仍保留于学校或指定公共服务机构的毕业生，可按应届高校毕业生对待。

来源：

- 2009-11-24：
  https://edu.sina.com.cn/official/2009-11-24/1329226956.shtml

Evidence：**B+ contemporaneous recruitment-policy reporting**。

这是一个特别适合 old-Web 的边界案例，因为它说明：

```text
Web-visible eligibility state
may depend on
an off-Web archival/personnel state
```

换句话说，报名网站即使完整存活，也不等于历史资格可自动重算。

为了知道某个 2009 年考生当时为什么被按应届处理，研究者可能还需要知道：

- 她当时是否落实单位；
- 档案究竟在哪里；
- 户口在哪里；
- 组织关系如何保存；
- 当年招考单位怎样解释规则。

这些个人状态既往往没有进入公开 archive，也不应为了复原普通个体而重新暴露。

### 新机制：off-Web predicate dependency

**off-Web predicate dependency（站外资格依赖）**：

> 一个 Web 事务的资格结果，依赖网页自身无法独立证明的现实记录。

这和银行卡支付、学历认证、保证金到账等跨系统状态有相似性，但这里的关键不是外部“交易”，而是外部**人生记录**。

---

## 6. 资格页面会制造一种特殊的 archive illusion

如果今天保存到一张 2009 年报名首页，上面写：

> “应届高校毕业生可报考”

它只能证明：

`policy category was presented`

不能证明：

- 任意声称自己是应届的人都能提交；
- 系统怎样判断“应届”；
- 档案位置是否在线可查；
- 资格审核员是否接受；
- 后续原件复审是否一致。

因此新增一条方法规则：

## category-visible ≠ category-computable

**页面显示某个资格类别，不等于历史 Web 系统拥有足够数据自行计算这个类别。**

还有一条：

## structured field ≠ automated decision

表单把生日、毕业年月做成结构化字段，也不能自动推出服务器按代码执行了年龄/届次判定。

这两条规则应该和 canonical 公务员事务链中的：

- application / confirmation gap；
- payment / reconciliation gap；
- qualification / attendance gap；

并列，而不是替代它们。

---

## 7. 当前页面保存的是旧文本，不是旧事务界面

本轮重要证据之一来自深圳市政府今天仍可访问的 2007 年公告页。

这类资源可以强力证明：

- 公告文本；
- 发布日期；
- 当年公开的资格规则；
- 某些历史 locator。

但它不能自动证明：

- 当前 DOM 是 2007 年 DOM；
- 当前字符集是当年字符集；
- 当前模板 / CSS / JS 属于 2007 年；
- 2007 年报名系统仍在；
- 历史 session / candidate backend 仍可访问。

因此应登记为：

**current government page carrying contemporaneous-dated content**

而不是：

**verified 2007 Web capture**。

---

## 8. historical locator / artifact status

本轮再次检索了下列早期招考 locator / host 线索：

- `www.mop.gov.cn/2005gwy/default.asp`
- `gwy2006.mop.gov.cn`
- `www.cpta.com.cn`
- 深圳人事 / 考试相关历史 host

搜索未取得一份能够按 `docs/METHOD.md` 最低合同实际检查的历史 capture：

- capture datetime；
- original URL；
- historical HTTP / replay state；
- charset / Content-Type；
- form fields；
- JS validation；
- form action / backend locator；
- 子资源；
- 第二历史时点。

因此：

## M1 historical qualification-interface capture: NOT ACHIEVED IN THIS SLICE

这只表示**本轮没有成功打开并核验 artifact**。

不能写成：

- “Wayback 没保存”；
- “当年页面不存在”；
- “资格审查完全人工”；
- “年龄一定由前端 JS 检查”。

---

## 9. 下一步最值钱的不是再找公告，而是找“判定发生在哪里”

优先级：

1. 2006–2010 国家 / 地方公务员原始报名表截图或教程；
2. 报名系统字段说明 / 操作手册；
3. 同期出现“年龄不符合”“非应届不能报此职位”等具体报错的用户材料；
4. 招录机关资格审查后台说明；
5. 两个实际历史 capture，比较职位表 / 报名入口随年度变化；
6. 若能取得历史 HTML，检查：
   - `select` / radio 中的身份类别；
   - birth date control；
   - graduation date；
   - hidden fields；
   - JS validation；
   - form action；
   - charset；
   - 是否 frame / IE-only。

只有做到这些，才能开始回答：

> **2007 年一个人的年龄与毕业届次，究竟是在浏览器、服务器、审核员桌面，还是纸质原件复审环节真正变成“可 / 不可报考”。**

---

## 10. 它改变了旧网考古哪一点？

事务型旧网研究很容易把用户想象成一组已经存在于数据库里的字段。

现实恰恰可能相反：

> **数据库字段是在努力把一个复杂人生临时压成可审查状态。**

“应届生”不是一个稳定字符串；它可能需要毕业年、档案、户口、工作状态和地方规则共同解释。

“35 岁以下”也不是只要页面上有一句话就已经完成自动验证。

因此，对旧招聘 Web 最重要的考古问题之一不再只是：

> 这个页面有没有保存？

还应该问：

> **网页到底拥有多少足够的信息，能够自己判断这个人是谁、现在属于哪类、今天还来不来得及。**
