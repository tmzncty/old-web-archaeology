# 2008—2010 消费级账号、社会身份可见性与旧网页人口误判

本文件补充：

- `docs/METHOD.md`；
- `docs/ACCOUNT_PORTABILITY_AND_LOCAL_RESIDUE_1999_2003.md`；
- `docs/AFFILIATION_CREDENTIAL_AND_ACCOUNT_LIFECYCLE_2001_2009.md`；
- `docs/PUBLIC_ACCESS_CONTEXT_1996_2003.md`。

前一份机构资格文档强调：学校邮箱、校园 IP、SSO 等可能给历史账号提供机构归属证据。

本文补一个相反方向的规则：

> **QQ、免费邮箱、博客、论坛昵称、手机 IM 等消费级账号常常没有机构凭证；更重要的是，用户有时正是因为这些账号“不先暴露现实身份”，才把它们当作社会空间。**

因此旧网考古必须区分：

```text
status existence ≠ status visibility ≠ status credential
```

现实中的职业、户籍、阶层、学校和单位身份存在，不代表它们在某个页面或聊天账号上可见；

账号没有显示这些身份，也不代表用户现实中“不属于任何机构”或“不存在社会位置”。

---

## 1. 为什么这一规则必要：2000 年代网民不能默认等于大学生/白领

早期中文互联网保存下来的材料非常容易发生样本偏差。

大学与办公室用户往往留下：

- 学校邮箱；
- 单位邮箱；
- 校园 BBS；
- 校园 SNS；
- 机构主页；
- 组织目录；
- 论文、项目、校友记录。

这些对象的现实身份比较容易被后人重新连接。

但同一时期还有大量年轻人通过：

- 网吧；
- 手机；
- QQ；
- 免费邮箱；
- 论坛昵称；
- QQ 空间；
- 游戏账号；

进入互联网。

他们可能没有任何 `edu.cn`、单位域名或第三方可验证机构字段。

这会造成一个很危险的考古错觉：

> “没有机构字段的人是不是边缘少数？”

同期证据显示答案是否定的。

---

## 2. 深圳 2010：大量基层年轻劳动者已经把“上网”纳入日常生活

深圳市总工会与深圳大学劳动法和社会保障法研究所 2010 年的新生代农民工调查，公开转载版本记录：

- 有效问卷 5000 份；
- 新生代农民工平均年龄约 23.7 岁；
- 52.4% 从事普工或服务员；
- 44.9% 受过高中教育（含中专/中技）；
- 46.8% 居住在公司集体宿舍；
- 57.1% 把上网列入业余生活。

来源：

- 人民网内容经搜狐保存：<https://news.sohu.com/20100715/n273527515.shtml>
- 报告后续部分经新浪保存：<https://news.sina.com.cn/c/2010-07-15/105720684918_2.shtml>

证据等级：**B+：同期调查报告的公开全文转载；未取得原始官方 PDF。**

### 考古含义

一个 2009—2010 年的 QQ 用户、论坛用户、博客用户或网吧用户，不能因为缺少学校/单位字段就被默认成：

- 学生；
- 白领；
- 城市户籍青年；
- 家庭电脑所有者；
- 稳定职业者。

消费级平台的用户社会分布已经足够广，平台存在本身不能承担人口分类功能。

---

## 3. 同期个案证明：账号甚至可能被主动用于“暂时隐藏现实分类”

2010 年《法制周报》同期采访记录了一名在深圳制造业工作的年轻农民工。

报道描述：

- 他长期在外务工；
- 在企业从事模具相关工作；
- 下班后会用手机登录 QQ；
- 他把线上交往的一项价值理解为：别人不会先知道他的“农民工”身份。

来源：

- 《新生代农民工心理调查：渴望更多交流和被认同》，2010-06-04，经新浪保存：<https://news.sina.com.cn/c/sd/2010-06-04/040320407559.shtml>

证据等级：**B/C 混合：同期报道中的同期个人自述。**

这不是用来证明“QQ 人人匿名”。

它证明一个考古上非常重要的可能性：

> **现实身份字段的缺失，有时不是档案缺损，而是当时使用方式本身的一部分。**

用户可能选择昵称、头像、QQ 号，而不主动写：

- 户籍；
- 工种；
- 公司；
- 收入；
- 教育经历。

因此不能把页面上“看不到”直接写成现实生活中“不存在”。

---

## 4. 建议把身份证据拆成五层

以后处理个人主页、QQ 空间、论坛账号、博客或 SNS profile，至少区分：

### 4.1 platform identifier

平台提供的技术标识：

```text
nickname
account id
QQ number
profile URL
email address
```

只证明某个账号/页面的技术身份。

### 4.2 self-declared identity

用户自己写出的现实身份，例如：

```text
“我在深圳打工”
“某大学学生”
“某公司程序员”
“来自湖南”
```

这属于同期自述，不能自动升级成机构确认。

### 4.3 credentialed affiliation

由学校邮箱、单位域名、校园 IP、SSO 或其他机构制度支持的归属。

这一层应继续按照：

`AFFILIATION_CREDENTIAL_AND_ACCOUNT_LIFECYCLE_2001_2009.md`

处理。

### 4.4 external corroboration

独立材料确认账号与现实身份的连接，例如：

- 同期采访；
- 官方人员目录；
- 机构公告；
- 同期公开简历；
- 可验证的作者页。

### 4.5 intentionally low-visibility identity

当有证据显示用户主动降低现实社会身份可见性时，单独标记。

例如：

```yaml
status_visibility:
  offline_status_known_to_researcher: true
  status_visible_on_platform: false
  low_visibility_intent_observed: true
  evidence_grade: B
  notes: "contemporaneous interview states that online interaction was valued because migrant-worker status was not initially visible"
```

不要把这一层误写成“匿名用户无法确认身份”。

“研究者知道现实身份，但平台互动对象当时未必知道”是完全不同的情形。

---

## 5. 新规则：平台上的缺失字段不能做负人口学推断

若一个历史 QQ 空间没有学校字段：

不能推出：

> “用户没有上过大学。”

若没有单位字段：

不能推出：

> “用户没有工作。”

若没有城市字段：

不能推出：

> “用户没有迁移。”

若只显示昵称：

不能推出：

> “用户现实身份不可知，因此无现实社会位置。”

最安全的写法是：

> capture 中未观察到该字段；现实状态需要其他证据。

也就是：

```text
not observed in artifact ≠ absent in biography
```

这应成为个人账号考古的默认规则。

---

## 6. 手机 QQ 还会打破“一个账号 = 一台电脑 = 一个地点”的旧假设

前面的共享终端研究已经处理：

```text
person ≠ account ≠ terminal
```

2008—2010 年以后还要进一步加入：

```text
account ≠ fixed network location
```

因为手机即时通信开始大量普及。

CNNIC 2008 年底数据记录：

- 中国网民 2.98 亿；
- 手机上网网民约 1.176 亿；
- 手机网民比上年增长约 133%。

来源：

- CNNIC，《第23次中国互联网络发展状况调查统计报告》：<https://www3.cnnic.cn/n4/2022/0401/c88-800.html>

农村互联网报告同时记录：

- 2008 年农村手机上网用户约 4010 万；
- 占农村网民约 47.4%。

来源：

- <https://www2.cnnic.cn/n4/2022/0401/c117-827.html>

这些是总体/农村统计，不是农民工专属统计。

但它们足以提醒旧网页研究：

> 到 2008—2010 年，一个账号的使用环境可能已经在电脑网吧、宿舍电脑和手机之间切换。

因此：

- IP 地理位置不是长期身份地址；
- 一次页面登录环境不代表主要上网环境；
- “手机用户”“网吧用户”“宿舍用户”可能是同一个人不同时间的状态。

---

## 7. 不要把“网友”想象成主要关系对象：同期调查给出了反例

深圳 2010 调查记录：

- 57.1% 新生代农民工把上网列为业余活动；
- 但只有约 3% 把网友列为主要社会交往对象；
- 工友/同事、老乡、亲友、同学仍然是主要关系来源。

来源：

- <https://news.sina.com.cn/c/2010-07-15/105720684918_2.shtml>

所以旧网考古不要默认：

> “一个论坛/QQ 用户的主要社会生活就在平台里。”

历史账号可能只承担：

- 维持已有线下关系；
- 获取信息；
- 娱乐；
- 低风险表达；
- 临时社交；
- 跨地点联络；

而人的核心关系网仍在工厂、宿舍、老乡圈、亲友和现实同学中。

平台材料通常只保存了整个社会关系图的一部分。

---

## 8. 消费级账号可能更适合频繁换工作，但这一点必须按证据强度写

同一深圳调查显示，新生代农民工平均换工作频率高于老一代。

2008 年 Pui-lam Law 与 Yinni Peng 对中国南方农民工移动通信的研究进一步指出：

- 移动通信帮助维持家人/亲属联系；
- 延长工作场所形成的社会网络；
- 零工劳动者可以依靠移动联系组织工作。

来源：

- Pui-lam Law & Yinni Peng, “Mobile Networks: Migrant Workers in Southern China,” 2008：<https://doi.org/10.7551/mitpress/9780262113120.003.0005>

因此可以合理提出：

> **个人手机号/即时通信账号有能力跨越某些雇佣关系结束节点继续保持社会联系。**

但如果某个具体历史账号没有纵向证据，不得自动写：

> “这个 QQ 号陪伴用户跨过了三次换厂。”

必须另外证明账号在多个时期持续由同一人使用。

---

## 9. 建议增加 `social_status_evidence` 字段

个人账号案例可以使用：

```yaml
social_status_evidence:
  platform_identifier:
    type: qq_account
    value_preserved: false
  self_declared:
    occupation: unknown
    location: unknown
    education: unknown
  credentialed_affiliation:
    observed: false
  external_corroboration:
    observed: true
    evidence_type: contemporaneous_interview
    evidence_grade: B
  status_visibility:
    occupation_visible_on_platform: unknown
    hukou_visible_on_platform: false
    institution_visible_on_platform: false
    low_visibility_intent_observed: true
```

### 解释原则

- `credentialed_affiliation.observed: false` 只表示未观察到凭证；
- 不表示现实中没有机构关系；
- `status_visibility.*: false` 表示页面/互动界面不显示；
- 不表示现实状态不存在；
- `low_visibility_intent_observed` 只有在同期自述或可靠材料明确支持时才填 `true`。

---

## 10. 对旧网页人口学分析的直接影响

### 错误写法

> “该 QQ 空间没有学校信息，因此用户大概是非学生青年。”

> “该论坛用户经常用手机发帖，因此属于城市白领。”

> “早期博客作者写作频繁，应有自己的家庭电脑。”

> “这个账号没有实名资料，所以无法研究其社会位置。”

### 更安全的写法

> “该 capture 未观察到学校/单位归属字段。同期消费级账号已被不同职业与户籍群体广泛使用，因此不能由账号形式推断其社会身份。”

如果有采访或独立来源：

> “同期报道将该账号/网名与一名深圳制造业劳动者关联；该身份连接来自报道，而不是平台页面本身。”

这样可以把：

```text
what the platform shows
```

与：

```text
what we know about the person from elsewhere
```

彻底分开。

---

## 11. 历史可见性不平等：数字痕迹多，不代表身份更容易恢复

消费级账号产生了一个重要悖论。

某个普通用户可能留下大量：

- 日志；
- 签名；
- 评论；
- QQ 空间内容；
- 论坛帖子；
- 游戏记录；

但这些内容没有稳定现实姓名、单位或学校连接。

反过来，一个大学教师可能只留下几页机构目录，却非常容易被机构邮箱和实名记录确认。

所以旧网考古必须区分：

```text
content density
identity legibility
institutional legibility
```

三者不是一回事。

这也意味着：

> **互联网并没有简单消除“哪些人生更容易进入历史”的差异，而是创造了新的可见性结构。**

有的人留下很少文字但身份清晰；

有的人留下大量文字却现实位置模糊。

---

## 12. 隐私边界：不要为了证明“非机构身份”反向肉搜普通用户

本仓研究的目标不是把一个匿名/昵称账号重新实名化。

即使研究者理论上可以利用：

- QQ 号；
- 邮箱；
- 老论坛签名；
- 手机号；
- 旧个人主页；

拼接出现实身份，也必须先问：

> 这个现实姓名对平台史/生活史结论是否必要？

如果只是为了证明：

> “2009 年存在年轻制造业劳动者使用手机 QQ”

应优先引用已经公开、同期采访过的个案和聚合调查，而不是重新识别一个普通历史账号。

继续执行 `docs/METHOD.md` 的 privacy minimization。

---

## 13. 海外机制校准，不扩大本仓 scope

2009 年 Eric C. Thompson 对新加坡外籍家政和建筑劳动者的研究显示，手机既帮助受空间/劳动约束的移民维持跨国社群，也可能在当地社会中成为“外来劳动者”的身份标记。

来源：

- <https://doi.org/10.1111/j.1471-0374.2009.00258.x>

这只用于校准一个机制：

> **通信技术不会天然让身份更隐形或更平等；它改变的是身份如何被显示、隐藏和重新标记。**

本仓仍只研究中文旧网约 1995—2015 的证据问题，不扩展为全球移动通信史。

---

## 14. 当前最小规则

以后遇到历史个人账号，默认执行：

```text
1. account proves account, not biography.
2. missing status field proves non-observation, not status absence.
3. institutional credential and consumer identifier must be separate fields.
4. contemporaneous self-description and external corroboration must be graded separately.
5. pseudonymous use can be an intended social affordance, not merely missing data.
6. mobile / shared-terminal use breaks the assumption that one account maps to one machine or place.
7. do not infer class, occupation, hukou, education, or household equipment from platform presence alone.
8. do not re-identify ordinary users unless identity is necessary to the historical claim.
```

这个规则应与：

```text
credential lifetime ≠ account lifetime ≠ affiliation lifetime
```

一起使用。

合起来就是：

> **历史账号首先是平台对象；现实人生必须另外建立证据链。**
