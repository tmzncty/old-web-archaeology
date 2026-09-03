# 2001–2010：学历查询、动态数据库与人事记录缺口

> Scope：本文件只处理约 2001–2010 中文旧网中“学历网上查询 / 人才网到档查询 / 记录核验页面”作为 Web artifact 时的证据合同。
>
> 更长的普通生活史、1996 流动人员人事档案制度、2020 以后数字化、2023 报到证取消以及美国 Social Security 对照，写在：
> <https://github.com/tmzncty/how-people-lived/blob/main/topics/documentary-portability-personnel-files-and-administrative-shadow-china-1936-2024.zh-CN.md>
>
> 本文件不写“电子政务发展史”，也不把今天还能打开的查询页冒充 2001 年的历史运行状态。目标是回答：**一个旧网页显示“查询学历 / 查询到档”时，今天的档案究竟能证明什么，又系统性看不见什么？**

---

## 1. 为什么这是一个新的旧网研究单位

仓库已经处理过：

- job board 的职位、简历和投递状态；
- 网银与汇款中的认证、清算和 recipient last mile；
- 同学录中的可变 profile、成员表和联系连续性；
- 婚恋、住房、兼职等从 Web 进入现实执行的链条。

学历/人事记录查询与这些都不同。

这里的 Web page 往往不是一个内容页面，也不是单纯交易表单，而是某个**权威数据库的 read surface / status surface**。

研究链条至少要拆成：

```text
public page
→ query form
→ user-supplied identifying fields
→ server-side validation
→ authoritative database lookup
→ result state
→ user interpretation
→ downstream institution accepts / rejects result
```

而“到档查询”还可能是：

```text
physical dossier transfer
→ receiving institution registers arrival
→ web status metadata
→ graduate sees arrival
→ offline filing / hukou / organization procedure
```

因此，本文件的新核心 unit 是：

> **web-visible record state ≠ record payload itself**

---

# 2. 当前 claim list

## C1 — 2001 年全国高等教育学历证书网上查询系统已经公开上线，并要求按证书字段查询

来源：CERNET / 中国教育和科研计算机网，2001-12-20 同期报道：
<https://www.edu.cn/edu/gao_deng/gao_jiao_news/200603/t20060323_21508.shtml>

报道描述当时的操作路径：

- 进入“中国大学生网”；
- 进入“学历文凭查询”；
- 选择普通高校、成人高校、网络教育、自考等类别；
- 输入学历证书号、姓名、出生日期、性别；
- 提交查询后由系统返回结果。

同时还有电话语音查询渠道。

### evidence

**B — 同时代教育网络报道。**

### confidence

**high** for public workflow claim.

### 不能证明

- 今天 `chsi.com.cn` 当前表单与 2001 页面相同；
- 当时所有查询结果页都可公开索引；
- 任何普通网民都能任意枚举别人学历；
- 后端数据库结构可由前端页面推断。

---

## C2 — 2002 年已经出现“真实数据库记录 + 伪造纸证”的身份错配案例

来源：2002-01-03 同期调查报道：
<https://www.edu.cn/edu/gao_deng/gao_jiao_news/200603/t20060323_22337.shtml>

报道记录造假者复制一个真实毕业生的证书编号和个人字段到假证上，再通过刚上线不久的网络查询系统得到真实学历记录。

### evidence

**B — 同期记者调查。**

### confidence

**high for this documented case**。

### 新 evidence rule

查询结果能证明的窄 claim 是：

> `submitted credential tuple matches an authoritative record`

不能直接证明：

> `the physical document or the person presenting it is the true record owner`

因此固定：

```text
database match
≠ claimant identity
≠ physical-document authenticity
```

这类界面必须把 **record verification** 与 **person authentication** 分开。

---

## C3 — 2004 年“哪个网站才是权威入口”本身已经成为安全问题

来源：教育部公告，2004-07-21：
<https://hudong.moe.gov.cn/jyb_xxgk/gk_gbgg/moe_0/moe_1/moe_366/tnull_4328.html>

公告说互联网上出现与教育部学历查询网站名称相似或复制相关内容的网站，因此重申中国高等教育学生信息网是学历证书查询唯一网站。

### evidence

**A — 同时代官方公告。**

### confidence

**high**。

### 新 evidence rule：authoritative endpoint must be proven

一个历史页面看起来像“学历查询”，不够。

至少要确认：

- host / domain；
- 当时主管机构；
- 当时官方公告或帮助文档是否指向该 endpoint；
- 页面是否只是镜像、仿冒、转载或静态说明。

因此：

```text
query-looking page
≠ authoritative query endpoint
```

---

## C4 — 2005 年学历数据库已成为现实招聘/资格审查的一部分

来源：教育部 2005-12-19 材料：
<https://www.moe.gov.cn/jyb_xwfb/gzdt_gzdt/moe_1485/tnull_12961.html>

材料记录：

- 2005 年 536.7 万高校毕业生学历证书电子注册并在指定网站发布；
- 1991–2000 年历史学历信息也已大量回登；
- 查询系统已有稳定使用量；
- 机关、企事业单位在招聘、干部任用等工作中越来越多使用学历查询/认证。

### evidence

**A — 官方统计/工作材料。**

### confidence

**high for registration and observed institutional use**。

### 不能证明

- every employer queried every candidate；
- 学历核验等于完整背景调查；
- 每一次查询事件都有可公开存档的 URL。

---

## C5 — 2008 年历史帮助页仍暴露具体浏览器/字符集条件

来源：塔里木大学研究生部门保留的学历查询说明页面：
<https://yjsb.taru.edu.cn/web/xlcx.html>

页面的历史说明包含：

- 查询证书编号等字段；
- 校验码；
- 对较早证书编码规则的说明；
- Windows 98 / Windows Me 与 IE 在字符集支持上的问题，并建议调整编码。

### evidence

**B — 高校服务说明页面。**

### confidence

**medium-high** for historical user-environment clue.

### 为什么重要

学历查询不是抽象 API。

当时用户实际看到什么，还受：

- Windows 版本；
- IE 版本；
- 字符集；
- 验证码；
- 页面脚本；
- 网络连通性。

影响。

因此：

> **modern browser success ≠ historical query usability**

---

## C6 — 2009 年人才网已经能公开“到档状态”，但实体档案仍在线下流转

来源：2009-05-07《新晚报》经新浪保存：
<https://news.sina.com.cn/c/2009-05-07/040315584999s.shtml>

报道说明哈尔滨市人才服务局开通 2009 届毕业生“到档查询”：

- 高校把档案统一转往人才服务局；
- 毕业生可登录哈尔滨人才网查询是否到档；
- 到档后仍需持报到证办理存档、落户、组织关系接收等手续。

### evidence

**B — 同期媒体 / 机构信息。**

### confidence

**high for existence of online arrival query**。

### 新 evidence rule：status surface != payload surface

这个页面能支持的最强 claim 是：

> 某机构公开提供了“档案是否到达”的 Web 查询入口。

不能写成：

> 2009 年毕业生人事档案已经网上转递、网上完整可读。

因此固定：

```text
arrival status online
≠ dossier contents online
≠ dossier transfer online
```

---

## C7 — 2010 年学历注册从“毕业后数月可查”转向在线即时注册

来源：教育部，2010-06-25：
<https://www.moe.gov.cn/jyb_xwfb/gzdt_gzdt/moe_1485/201006/t20100625_90052.html>

教育部说明此前普通高校毕业生学历经过学校上报、省级审核、教育部备案、数据库发布后，通常毕业二至三个月才可网上查询；2010 年开始实施在线即时电子注册。

### evidence

**A — 同期官方说明。**

### confidence

**high**。

### 新研究变量：database publication latency

历史 Web 考古必须问：

> 某人的资格在现实中何时成立？

以及：

> 这个资格何时进入可查询数据库？

两者可能不是同一天。

因此：

```text
credential issued
≠ credential queryable
```

---

# 3. 研究单位必须拆开

对任何历史“查询页面”至少区分以下对象。

## 3.1 authority / custodian

谁是记录的权威保管或发布机构？

不能只看网页 logo。

## 3.2 public landing page

对普通访问者公开的说明页、入口页。

它可能是静态 HTML。

## 3.3 query form

真正提交查询字段的表单。

需要记录：

- GET / POST（能可靠判断时）；
- action endpoint；
- 字段名；
- 验证码；
- session / cookie；
- referrer / browser requirement；
- 编码。

## 3.4 dynamic result

数据库响应。

动态结果很可能：

- 不具有稳定 URL；
- 依赖 POST body；
- 含个人信息；
- 不应被 archive 公开重放。

## 3.5 backend record

权威数据库里的记录本身。

Web 页面不能自动证明数据库 schema。

## 3.6 physical dossier

对人事档案案例，还要单独建模实体材料。

它可能通过：

- 机要；
- 专人；
- 后期符合规范的邮政渠道；

转递，而网页只提供状态。

---

# 4. 动态数据库页面的四类 archive gap

## 4.1 query-state survival gap

Web Archive 可能保存查询框，却没有保存历史用户提交了什么字段。

因此：

> **form survived ≠ historical query survived**

## 4.2 result-state survival gap

即使提交动作可复原，历史结果可能依赖：

- 当时数据库状态；
- 当时权限；
- 当时验证码；
- 当时请求来源。

今天用同样字段查询得到的 current state，不能冒充 2005 result。

因此：

> **current database answer ≠ historical database answer**

## 4.3 privacy-preserving absence

学历、姓名、出生日期、人事档案状态等都可能涉及普通人的个人信息。

这类结果不应该因为“技术上可能抓到”就批量重新公开。

因此：

> **archive absence may be ethically desirable, not merely a technical failure**

## 4.4 backend-shadow gap

真正决定结果的是数据库和机构业务系统。

公开 Web archive 通常看不见：

- 数据库更新事务；
- 审核队列；
- 机构内部修改历史；
- 到档登记；
- 转递回执；
- 线下补材料。

所以：

> **archived front end ≠ archived administrative system**

---

# 5. “学历查询”与“人事档案查询”不能合并

## 5.1 学历查询

查询对象更接近：

```text
credential record
```

典型 claim：

- 此证书信息是否对应注册学历；
- 何时可查；
- 哪个网站权威。

## 5.2 人事档案到档查询

查询对象更接近：

```text
custody / arrival state of dossier
```

典型 claim：

- 档案是否已到机构；
- 当前存放地；
- 后续该去哪里办理。

因此：

```text
credential verification service
≠ personnel-file service
```

更不能把“学信网能查学历”写成“个人档案已经电子化”。

---

# 6. “查询成功”究竟证明哪一层？

建议为每个 query case 标注 `verified_claim_type`。

可选值：

- `credential-existence`
- `credential-field-match`
- `record-arrival`
- `record-custody-location`
- `application-status`
- `identity-authentication`
- `document-authenticity`
- `person-to-record-binding`

通常一个页面只能证明其中一两层。

例如 2001 学历查询更接近：

```text
credential-field-match
```

而不能自动提升成：

```text
person-to-record-binding
```

2009 到档查询更接近：

```text
record-arrival
```

而不是：

```text
record-contents-authenticated
```

---

# 7. 域名与权威性必须做 temporal validation

2001 报道使用“中国大学生网”及当时域名；2004 教育部又明确重申 `chsi.com.cn` 为唯一学历查询网站。

因此历史研究不能把“今天的学信网 URL”无条件回填到 2001。

至少记录：

```yaml
service_brand:
historical_host:
claim_date:
authority_source:
current_host:
redirect_observed:
```

并固定：

> **same service lineage ≠ same historical endpoint**

域名迁移本身也是证据。

---

# 8. 浏览器、编码与验证码属于查询系统的一部分

如果历史说明页提到 Windows 98、Windows Me、IE、编码自动选择、验证码等，不能把这些当装饰信息删掉。

它们影响：

- 用户能不能看到字段；
- 中文姓名是否正常显示；
- 表单是否能提交；
- 自动化抓取是否可能；
- archive replay 是否与当年一致。

最低记录：

```yaml
browser_assumption:
os_assumption:
charset:
captcha_present:
client_script_required:
query_method:
```

没有验证时写 `unknown`。

---

# 9. 到档查询是一种“行政物流 tracking”，不是网页内容史

2009 案例说明一个很值得复用的形态：

```text
physical object moves
→ institution records state
→ web exposes state metadata
```

这和包裹 tracking、申请进度查询、证件办理状态页非常接近。

因此以后遇到旧网行政查询页，要问：

1. payload 是什么？
2. payload 是否在线？
3. Web 只显示哪几个状态字段？
4. 状态是谁录入？
5. 状态更新延迟多久？
6. 查询成功后是否仍需到柜台？

### 硬边界

```text
tracking page
≠ dematerialized workflow
```

---

# 10. 当前历史可见性模型

对 2001–2010 资格/档案查询页面，可以使用以下 funnel：

```text
service announced
→ public landing page exists
→ query form reachable
→ historical client can submit
→ backend accepts fields
→ authoritative record exists
→ result returned
→ user understands result
→ downstream institution accepts result
→ real-world procedure completes
```

Web archive 通常最容易证明前 2–3 层。

越接近真实个人记录和业务结果，越难、也越不应该被公开 archive 完整保存。

因此：

> **the most consequential state may be the least publicly archiveable state**

这是本仓此前 `private-transaction survival inversion` 在行政记录领域的对应现象。

---

# 11. Evidence ledger

| Claim | Source | Grade | Confidence | Gap |
|---|---|---:|---:|---|
| 2001 学历网上查询系统公开上线 | CERNET 同期报道 | B | High | 未拿到原始 query page capture |
| 2001 查询依赖证书号、姓名、出生日期、性别 | 同上 | B | High | 后续版本字段可能变化 |
| 2002 真实数据库记录可被假证借用的个案 | CERNET 同期调查 | B | High for case | 单一个案 |
| 2004 教育部指定唯一权威查询网站 | 教育部公告 | A | High | 证明当时权威性，不证明全部镜像状态 |
| 2005 学历查询进入招聘/资格审查实践 | 教育部材料 | A | High | 无 individual query logs |
| 2008 历史服务说明存在 IE/编码条件 | 高校说明页 | B | Medium-high | 页面具体创建/更新时点仍需更细 provenance |
| 2009 哈尔滨人才网开通到档查询 | 同期新闻 | B | High | 原始动态 result 未取回 |
| 2010 学历注册从二三个月滞后改为即时 | 教育部说明 | A | High | 只针对学历注册 |

---

# 12. Privacy stop conditions

这类研究尤其容易越过普通人隐私边界。

以下内容默认不做批量采集或重新公开：

- 普通人的姓名 + 出生日期 + 学历证书编号组合；
- 可用于再次查询的完整 credential tuple；
- 人事档案存放地与身份证号组合；
- 动态结果页中的普通人敏感字段；
- 可直接绑定现实身份的历史 query result。

优先保存：

- 表单字段 schema；
- 官方帮助页；
- 查询流程；
- 状态枚举；
- 公开机构统计；
- 去标识化错误类型；
- 截止在支持 claim 所需的最小个案信息。

如果某 capture 的研究价值主要来自暴露普通人敏感数据，**停止复原**。

---

# 13. Negative evidence protocol

如果没有找到 2001/2004/2009 原始动态查询页，不写：

> 当年页面不存在。

只写：

> 当前未验证到可可靠回放的原始 query/result capture。

需要继续检查：

- Wayback URL variants；
- 历史域名迁移；
- GET / POST 差异；
- robots；
- session；
- captcha；
- JSP/ASP 动态 URL；
- archive 未保存 POST body；
- 结果页因个人数据策略未被抓取。

---

# 14. 下一步最高价值证据

最有价值的不是再找到十篇“网上查询很方便”的新闻，而是以下任一项：

1. **2001–2004 原始学历查询入口 capture**：能确认历史 host、字段、编码、提交方式；
2. **2006–2010 人才网原始到档查询 capture**：哪怕没有个人结果，也能确认 query schema 和状态枚举；
3. **同一服务跨年份版本链**：观察字段、验证码、域名、认证和隐私提示怎样变化；
4. **同时代用户故障帖**：例如“查不到学历”“档案明明寄了但网页没到档”“IE/编码/验证码失败”；
5. **后台与前台更新延迟证据**：能量化 `record event → database-visible state` 的 latency。

如果能拿到第 4 或第 5 类证据，就可以把本文件从“页面/制度 evidence contract”推进到真正的 **administrative latency archaeology（行政延迟考古）**。

---

# 15. 本轮新增的硬规则

```text
query page exists
≠ authoritative endpoint

form survives
≠ historical query survives

database match
≠ claimant identity

credential query success
≠ full personnel record verified

arrival status visible
≠ dossier contents online

current database answer
≠ historical database answer

modern browser can open page
≠ historical client could complete query

more digitized
≠ more appropriate to archive personal results
```

这些规则应当用于后续所有旧网中的政府、教育、人才、考试、资格、证书和申请状态查询页面。