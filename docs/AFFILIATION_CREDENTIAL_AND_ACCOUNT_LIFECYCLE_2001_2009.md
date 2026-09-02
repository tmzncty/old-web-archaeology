# 2001—2009 机构资格、校园邮箱与平台账号生命周期

本文件补充：

- `docs/METHOD.md`；
- `docs/CONTACT_ENDPOINT_LIFECYCLE_1997_2003.md`；
- `docs/ACCOUNT_PORTABILITY_AND_LOCAL_RESIDUE_1999_2003.md`。

主研究对象仍是约 1995—2015 年中文互联网。

这里处理一个旧网考古中很容易发生的身份误判：

> **历史平台曾要求学校邮箱、校园 IP 或机构账号注册，不等于一个多年后的存活账号仍代表当前学生/教职工身份。**

核心规则：

```text
credential lifetime ≠ account lifetime ≠ affiliation lifetime
```

也就是说，要分开记录：

1. 现实中的机构成员资格；
2. 机构发放的数字凭证；
3. 平台在某一时点采用的准入规则；
4. 准入后形成的平台账号；
5. 毕业/离职后的账号持续情况。

---

## 1. Email 在旧网材料里有两种完全不同的角色

前一份联系方式生命周期文档主要把 Email 当作：

> 联系一个人的 endpoint。

但高校/单位邮箱还可能同时承担：

> 机构归属的可机器读取代理。

因此证据结构必须至少区分：

```text
email_as_contact
email_as_affiliation_marker
email_as_registration_credential
```

不要因为三者使用同一个字符串就把它们合并。

---

## 2. 中国高校同期制度证明：学校邮箱域名确实可以承担身份表述

东华大学 2004 年的信息化通知说明：

- 校园邮件系统购置于 2001 年；
- 当时已有约 6500 名学生用户、1500 名教师用户；
- 学校认为教师使用社会免费邮箱时，缺少学校域名，不利于其以本校教职工身份开展教学科研和对外学术交流；
- 教师邮箱与统一身份认证关联；
- 教师离校后保留六个月，之后失效。

来源：

- 东华大学信息化办公室，2004-09-08：<https://inforcenter.dhu.edu.cn/2011/0707/c21353a291594/page.psp>

证据等级：**A：机构同期正式文件。**

### 考古含义

如果历史页面出现一个学校域名邮箱，可以较强支持：

> 该页面在该时点把一个带有该机构域名的地址作为联系入口。

如果同时拥有该校当期发放规则，可以进一步支持：

> 这一类地址通常发给什么群体。

但仍不能机械推出：

- capture 当天现实身份一定仍然有效；
- 该地址没有处在离校缓冲期；
- 当前控制者就是最初申请人；
- 该人已取得某种学历或学位。

机构邮箱不是毕业证。

---

## 3. 机构账号会存在“资格结束后的尾巴”

东华大学的“离校后六个月失效”本身就是一个很好例子：

```text
T0: person leaves institution
T1: mailbox still usable
T2: mailbox expires
```

因此：

> endpoint validity at T1 不足以证明 affiliation validity at T1。

这条规则应推广到：

- 学校邮箱；
- 校园网账号；
- 单位邮箱；
- 校园 BBS 认证；
- VPN/代理权限；
- 学术数据库远程访问；
- 校园 SNS 注册资格。

---

## 4. 校内网把学校邮箱/校园 IP 进一步变成平台注册资格

2007 年《北京青年报》关于校内网向白领扩张的同期报道回顾，校内网早期要求用户：

- 拥有带 `edu.cn` 后缀的电子邮件地址；
- 或在指定大学 IP 地址范围内上网；

才能完成注册。

来源：

- 《北京青年报》，《校内网向白领市场扩张》，2007-12-26，经新浪科技保存：<https://tech.sina.com.cn/i/2007-12-26/10521937375.shtml>

证据等级：**B：同期媒体报道。**

2008 年中国新闻网对校园 SNS 的报道也提到类似机制：学校邮箱和校园网络位置被用于限制注册范围。

来源：

- 中国新闻网，《校内网：毕业了，校内还在》，2008-10-13：<https://www.chinanews.com.cn/edu/dxxy/news/2008/10-13/1409431.shtml>

### 考古意义

一个平台注册页面如果写：

```text
需要 edu.cn 邮箱
```

它证明的是：

> **该版本平台把某类机构数字资源当作准入凭证。**

它不自动证明：

- 每一个账号都确实通过相同方式注册；
- 注册后持续重新验证；
- 多年后的账号持有人仍是学生；
- 邮箱地址与现实人永久一一对应。

必须记录**规则版本和时间点**。

---

## 5. 平台得到的是一个资格快照

旧网考古建议使用下面的时间模型：

```text
T0 institutional credential exists
T1 platform accepts credential
T2 account created
T3 institutional status changes
T4 credential expires / converts / becomes alumni credential
T5 platform account remains active or disappears
```

除非有持续再认证证据，否则：

```text
account active at T5
```

不能推出：

```text
credential still valid at T5
```

也不能推出：

```text
person still has original affiliation at T5
```

---

## 6. 2008 年近同时代材料直接证明：毕业用户会继续留在校园 SNS

中国新闻网 2008 年报道记录了一名中国人民大学毕业生的案例：

- 已经毕业并开始工作；
- 仍频繁打开校内网；
- 继续查看消息、同学动态；
- 曾在平台上写日志调侃自己工作以后仍离不开校内；
- 后续仍继续使用。

来源：

- <https://www.chinanews.com.cn/edu/dxxy/news/2008/10-13/1409431.shtml>

证据等级：**B/C 混合：同期报道嵌入近同时代个人平台自述。**

### 这对 archived profile 的解释非常重要

如果我们在 2008 年 capture 里看到一个账号属于“某大学网络”，安全写法是：

> 该账号在平台中与该大学网络存在历史关联；若平台注册曾要求学校资格，则这种关联可能源于较早的注册资格。账号持有人在 capture 当时是否仍为学生，需要另证。

不要写：

> “2008 年某大学在校生 X”。

除非有 2008 年独立学籍/自述证据。

---

## 7. 平台扩张本身也可能是用户生命历程逼出来的

2007 年关于校内网向白领扩张的报道明确提到：

> 早期大学用户中已经有一部分毕业并进入白领职场。

这意味着平台 scope 变化不能只从公司战略解释。

它还可能是：

```text
cohort ages
↓
users graduate
↓
existing social graph crosses institution boundary
↓
platform must decide whether to exclude, retain, or redesign for them
```

这是一种 **life-course pressure on platform design（生命历程对平台设计的压力）**。

旧网平台谱系研究以后应增加这一维度：

- 平台最初服务什么人生阶段？
- 用户年龄增长以后怎么办？
- 平台是否跟着用户进入下一阶段？
- 是否创建校友/职场/家庭等新分类？
- 还是让原社区逐渐老化、迁移或死亡？

---

## 8. 海外对照：TheFacebook 也曾把大学邮箱用作校园社会图的准入条件

2004 年 Brown University 的同期学生报纸介绍 TheFacebook 时明确说明：

- 当时服务已覆盖数十所大学；
- 拥有相应学校有效 Email 地址的用户可以创建个人资料；
- 新生用它在线认识未来同学，并发展到线下见面。

来源：

- *The Brown Daily Herald*, “Thefacebook.com e-unites first-years,” 2004-09-02：<https://www.browndailyherald.com/article/2004/09/thefacebook-com-e-unites-first-years>

证据等级：**B：同期校园报纸。**

这用于校准机制：

> 机构 Email 被第三方社交平台当作准入凭证，并不是中文互联网独有。

本仓库不因此扩成 Facebook 史。

中国案例的具体解释仍应优先追踪：

- `edu.cn`；
- 校园 IP；
- 校园网和宿舍接入；
- 校内网/5Q/占座等本地平台；
- 网吧/公共终端与校园身份的交叉。

---

## 9. 校友邮箱证明：机构资格可以被重新编码，而不是简单失效

浙江大学官方材料记录：自 2007 年起，毕业生可以保留/转换校友邮箱，后来说明中明确把这一安排作为毕业离校过程的一部分。

来源：

- 浙江大学，2015 年邮件系统发展时间线：<https://www.zju.edu.cn/2015/1203/c32861a1520413/pagem.htm>
- 浙江大学信息技术中心，校友邮箱说明：<https://its.zju.edu.cn/_t2014/2020/0410/c49623a2051388/page.psp>

海外同期对照中，*The Harvard Crimson* 2003 年报道 Harvard 自 1998 年起提供 `post.harvard.edu` 校友地址，最初主要作为转发地址，让毕业生在使用其他邮箱服务商的同时保留 Harvard 关联地址。

来源：

- *The Harvard Crimson*, 2003-10-14：<https://www.thecrimson.com/article/2003/10/14/e-mail-filter-blocks-more-than-spam/>

### 考古含义

`@university-domain` 不能自动解释为：

> current student / current employee

还可能是：

> alumnus / forwarding alias / legacy account / transition period

必须先查机构自己的账号制度。

---

## 10. 建议把“机构归属凭证”单独建模

旧网页、SNS 案例遇到学校/单位邮箱时，不要只沿用 contact endpoint 字段。

建议增加：

```yaml
affiliation_credential:
  type: institutional_email  # institutional_email / campus_ip / SSO / other
  issuer: unknown
  credential_value_preserved: false
  institutional_domain: example.edu.cn

credential_policy:
  observed_at: null
  eligible_population: unknown
  issue_rule_evidence: []
  expiry_rule: unknown
  post_exit_grace_period: unknown
  alumni_conversion: unknown

platform_admission:
  platform: unknown
  rule_observed_at: null
  required_credential: unknown
  continuous_revalidation: unknown

platform_account:
  first_observed: null
  last_observed: null
  institutional_network_label: unknown

affiliation_status_at_capture:
  value: unknown
  evidence: []
  confidence: low
```

### 为什么 `affiliation_status_at_capture` 必须独立

因为：

- 注册资格可能只检查一次；
- 邮箱可能有离校宽限期；
- 邮箱可能转换成校友地址；
- 平台账号可能永久保留；
- 用户可能毕业多年仍属于原校园网络分类。

---

## 11. 平台案例应当保存“准入规则版本”

平台规则会变。

例如一个平台可能经历：

```text
Phase A: only selected universities
Phase B: all university email / campus IP
Phase C: alumni / white-collar expansion
Phase D: open registration
```

如果只引用后期帮助页面去解释早期账号，就会产生严重后见之明。

所以 M1/M2 案例以后应尽量记录：

```yaml
admission_rule_observation:
  capture_datetime: ...
  platform_version_period: ...
  accepted_credentials:
    - edu-email
    - campus-ip
  source: ...
  confidence: ...
```

---

## 12. 不要从域名变化自动构造人生迁移

历史个人主页可能出现：

```text
2003: user@university.edu.cn
2006: user@publicmail.com
2008: user@company.com
```

这很诱人，会让人写成：

```text
student → graduate → employed
```

但如果没有额外证据，这仍然是不安全的。

可能情况包括：

- 三个邮箱同时使用；
- 第一个是实验室公共邮箱；
- 公司邮箱用于业务、私人邮箱继续存在；
- 页面维护者变化；
- 页面复制/镜像；
- 校友继续保留学校邮箱。

安全写法仍是：

```text
endpoint A observed at T1
endpoint B observed at T2
endpoint C observed at T3
life-course linkage: unproven
```

只有当自述、简历、学校名录、单位页面或迁移提示提供独立证据时，才能建立人生节点关系。

---

## 13. 机构数字身份会制造档案偏差

大学生、教师、大型机构职员更可能留下：

- 有机构域名的邮箱；
- 校园 BBS 账号；
- 公开主页；
- 学术/单位目录；
- 可按年份追踪的成员记录。

没有进入这些制度化路径的人，可能主要留下：

- 免费邮箱；
- QQ；
- 匿名论坛名；
- 网吧使用痕迹；
- 手机/BP 机；
- 极少数零散页面。

因此旧网资料中的“身份可验证程度”本身就有阶层/制度路径选择偏差。

不要把：

> 更容易验证的人

误写成：

> 更典型的网民。

---

## 14. 与平台谱系 M2 的连接

现有 M2 关注：

- 谁拥有 URL；
- 谁决定布局；
- 身份是匿名还是实名/半实名；
- 内容生命周期由谁决定；
- 平台死亡时能否迁走内容。

建议以后再加一个维度：

> **谁决定你有资格进入这个平台？这种资格在人生阶段变化后是否继续有效？**

平台可以按：

- 机构域名；
- 校园 IP；
- 邀请码；
- 手机号；
- 身份证；
- 现实关系；

构造不同的社会边界。

这会直接影响平台里“谁被保存下来”。

---

## 15. 隐私边界

历史学校邮箱尤其容易与真实姓名、学院、毕业年份直接关联。

因此：

- 不为证明一般机制而批量公开个人邮箱；
- 默认只保留域名和类型；
- 只有研究对象本身是公开机构/公众人物且地址确有论证必要时，才考虑保留完整历史 endpoint；
- 不通过当前邮箱是否可收信来“验证”历史人身份；
- 不主动向历史地址发送邮件做考古探针。

机构归属研究不需要重新打扰现实中的人。

---

## 16. 本文件带来的新审查问题

以后处理校园站、校园 SNS、个人主页、站长资料时，至少问：

1. 这个 Email 在页面上只是联系方式，还是也被平台/机构用作资格凭证？
2. 当期机构发放规则是什么？
3. 当期平台注册规则是什么？
4. 是只在注册时验证，还是持续验证？
5. capture 时现实机构身份是否有独立证据？
6. 离校/离职后账号有无宽限期？
7. 是否存在 alumni conversion / forwarding？
8. 平台账号是否穿过毕业/离职继续存在？
9. 当前 archive 保存的是机构身份、平台身份，还是二者不同步后的残留？

如果这些问题不能回答，允许写：

> **unknown。**

比把一个旧 `edu.cn` 地址直接解释成“当时在校生”可靠得多。

---

## 17. 与 `how-people-lived` 的分工

本文件只处理中文旧网考古里的证据解释规则。

跨国生命历程与普通生活问题，见 `how-people-lived`：

- `topics/institutional-email-as-affiliation-credential-and-life-stage-1998-2009.zh-CN.md`

那里关注的是：

> 学校/单位数字账号如何进入毕业、就业、校友身份和长期社会关系。

这里关注的是：

> **面对一个历史页面、账号或平台规则，研究者到底可以安全声称什么。**
