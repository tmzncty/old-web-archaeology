# 中文健康门户、在线问答、病友论坛与医生主页：健康信息、咨询和线下诊疗状态缺口（2000–2015）

> Scope：本文严格服务于 `old-web-archaeology` 的约 1995–2015 中文互联网主范围。
>
> 对应的前互联网医学科普、病友生活史、疫情后互联网医院、慢性病/罕见病长期照护与海外 BBS/Usenet 对照见：
> https://github.com/tmzncty/how-people-lived/blob/main/topics/from-health-magazine-reader-mail-to-patient-forums-and-internet-followup-illness-information-peer-support-and-care-continuity-china-1983-2026.zh-CN.md
>
> 本文不是“中国互联网医疗通史”。研究对象是旧网中看起来最像“医疗事务”的几类公开对象——健康文章、疾病/药品/医院/医生数据库、患者公开提问、病友论坛、医生主页与咨询入口——以及为什么这些页面**不能直接被当成一次真实诊疗已经发生的证据**。

---

## 0. M1 case status

按 `ROADMAP.md` 与 `docs/METHOD.md`，完整 M1 案例至少需要身份确认、两个历史时点、尽量两个独立 evidence family、资源缺失清单、浏览器/编码条件、“已证实/高概率/不知道”以及历史 capture 的直接检查。

本轮得到：

- **平台/产品身份：强**；
- **时间线：2000 / 2004 / 2007 / 2008 / 2009 / 2010 / 2012 / 2015，多时点强**；
- **独立 evidence family：平台官方发展史 + 同期媒体 + 同期医生自发页面 + 医学/科技媒体，强**；
- **事务状态模型：强**；
- **公开页面与线下临床结果之间的缺口：强**；
- **隐私边界：高敏感，必须主动限制复原范围**；
- **真正可核验 historical archive memento：本轮没有取得一个已经实际打开、能同时检查 original URL / capture datetime / HTTP replay / charset / DOM / interaction endpoint / subresources / second time point 的合格样本。**

因此：

> **M1 verified historical Chinese health portal / patient-Q&A / doctor-profile capture: NOT ACHIEVED IN THIS SLICE.**

这不等于“Wayback 没有保存”。本轮只能说当前检索没有获得符合仓库最低证据合同的已验证 capture。

---

## 1. 研究单位：不要把“网上看到医生”压成一个对象

### 1.1 Physical patient

现实中的患者本人。

需要区分：

- 真实姓名；
- 平台昵称；
- 是否经过实名认证；
- 是否由家属代问；
- 同一个账号是否代表同一个患者；
- 某一帖子是否只描述另一个家庭成员的病情。

### 1.2 Symptom statement

用户自己写出的症状描述。

它是文本对象，不等于医学体征，也不等于正式病历。

```text
user says “发烧/疼痛/皮疹”
!= clinician observed finding
!= diagnosis
```

### 1.3 Claimed diagnosis

患者本人、病友或第三方在帖子里写出的疾病名称。

必须与：

- 医院正式诊断；
- 医生在线推测；
- 搜索引擎标签；
- 群体自称

分开。

### 1.4 Platform account

用户在健康网站上的账号。

可能是：

- 匿名昵称；
- 手机/邮箱注册；
- 后期实名账户；
- 医生账户；
- 机构账户。

### 1.5 Health article

编辑、医生或转载来源形成的健康内容页。

必须记录：

- 原始发布日期；
- 是否后来更新；
- 作者身份；
- 是否转载；
- 当前页面与历史页面是否同版本。

### 1.6 Disease / drug / hospital / doctor database entry

结构化数据库对象。

例如 39 健康网官方发展史记录 2007 年推出疾病、药品、医院/医生等数据库。

这些数据库记录的 `entity exists in catalog` 与现实中的 `service available` 不相同。

### 1.7 Doctor profile

一个公开医生页面可能包含：

- 医院；
- 科室；
- 职称；
- 擅长；
- 文章；
- 患者评价；
- 咨询入口；
- 服务状态。

必须保留：

```text
doctor profile exists
!= doctor identity independently verified
!= current hospital affiliation verified
!= doctor currently active online
!= doctor accepts this patient's condition
```

### 1.8 Patient question

公开或半公开提交给平台的问题。

问题本身至少有：

- draft；
- submitted；
- accepted/moderated；
- publicly visible；
- routed to doctor；
- answered；
- closed/deleted

等不同状态。

### 1.9 Doctor answer

医生或平台标注为医生的人留下的回复。

必须区分：

- 科普回答；
- 就医建议；
- 鉴别诊断提示；
- 正式复诊意见；
- 处方。

2000s–early 2010s 旧网里的绝大多数公开问答不能自动升级成后来的“互联网医院正式诊疗”。

### 1.10 Patient forum / group

病友论坛、BBS、QQ群、博客评论等社群对象。

群体可以产生：

- 情绪支持；
- 经验知识；
- 就医路线；
- 疾病解释；
- 偏方；
- 谣言；
- 线下病友关系。

归档时不能只因为多人重复某说法，就提高其医学证据等级。

### 1.11 Consultation request

患者请求医生回复的一次事务。

可能还包含：

- 付费；
- 服务包；
- 次数；
- 等待队列；
- 图片/报告上传；
- 电话回拨；
- 预约转诊。

### 1.12 Off-platform contact

医生和患者可能迅速转向：

- 电话；
- 短信；
- QQ；
- 后来的微信；
- 医院挂号；
- 线下面诊。

这形成典型 **`contact-channel escape / 联络链逃逸`**。

### 1.13 Offline clinical encounter

现实门诊/住院才是另一权威域。

必须与网页对象分开：

```text
online question
→ maybe online answer
→ maybe appointment/referral
→ maybe offline attendance
→ examination
→ diagnosis
→ prescription/treatment
```

archive 往往只能看到前两步。

### 1.14 Prescription / medicine purchase

尤其不能从“医生回复某药名”直接推断：

- 形成正式处方；
- 患者购买；
- 患者服用；
- 治疗有效。

### 1.15 Follow-up relation

一个医生和患者持续数月/数年的咨询关系。

它可能跨越：

- 网站；
- 电话；
- 医院；
- QQ/微信；
- 病历系统。

单一网页只能看见其中很小一部分。

### 1.16 Archive capture

最后才是历史档案系统保存的一份表示。

必须和以上所有现实对象分开。

---

## 2. 时间线：健康网站从内容页走向查询、问答与医生互动

### 2.1 2000-03-09：39健康网官方历史记录正式开通

39健康网当前官方发展历程将正式开通时间记为 2000 年 3 月 9 日。

来源：

- https://corp.39.net/info/develop/
- https://corp.39.net/info/

证据等级：**A（平台当前官方历史陈述）**。

能证明：

- 平台今天把自身起点定位于 2000-03-09；
- `www.39.net` 是其核心品牌/host。

不能单独证明：

- 2000 年首页 DOM；
- 当时字符集；
- 当时具体栏目结构；
- 当年真实访问量；
- 普通网民采用率。

### 2.2 2004-12：官方历史称推出“39健康搜”

39 官方发展史称，2004 年 12 月与雅虎中国合作推出“39健康搜”。

来源同上。

证据等级：**A（平台历史陈述）**。

这个节点的 old-Web 意义是：健康内容开始从门户栏目进一步成为**查询对象**。

但必须保留：

```text
search product exists
!= health result complete
!= ranking medically authoritative
!= target page still available
```

### 2.3 2007-09：疾病/药品/医院/医生数据库

官方发展史称 2007 年 9 月推出七大健康数据库，包括疾病、药品、医院/医生库。

来源：

- https://corp.39.net/info/develop/

这使信息架构从：

```text
频道 → 文章
```

进一步转向：

```text
疾病 entity
药品 entity
医院 entity
医生 entity
→ structured lookup
```

但当前没有历史 capture 验证当时字段、URL pattern 和查询表单。

### 2.4 2008-08：健康问答成为平台显式产品

官方发展史将“39健康问答”推出时间记为 2008 年 8 月，并将其描述为网民与医生直接交流的产品。

来源：

- https://corp.39.net/info/develop/

证据等级：**A（平台陈述）**。

此处最重要的不是平台宣传中的“直接交流”，而是 old-Web 研究必须立刻追问：

```text
question written
→ submitted
→ platform accepted
→ public page created
→ routed
→ doctor read
→ doctor answered
→ user read answer
→ real-world action
```

这不是一个状态。

### 2.5 2009-08：专家博客成为健康门户的一部分

官方历史称，到 2009 年 8 月健康博客中已有大量专家博主。

来源：

- https://corp.39.net/info/develop/

这意味着医生在旧网里的角色不仅是数据库条目，也可以成为持续发布文章、形成个人内容地址的作者。

### 2.6 2009-09-07：好大夫医生同期自发页面保存“虚拟诊室”的实际使用动机

湘雅医院医生闵晓珊在好大夫在线自己的页面写道，随着患者越来越多，越来越多人要求留个人电话号码；私人电话不断侵入休息以后，她决定不再留个人号码，并把网站虚拟诊室视为解决渠道边界的办法。

来源：

- https://www.haodf.com/neirong/wenzhang/83957.html

证据等级：**A/T0：同期、具名医生、平台原生内容当前仍可读。**

这条材料能直接证明：

- 当时至少有医生把好大夫页面作为患者院外提问入口；
- 平台与个人电话之间存在功能替代/边界管理关系。

不能证明：

- 所有问题都会回复；
- 回复具有正式诊断效力；
- 网站取代线下就医。

值得特别注意：当前页面今天附带的“仅供健康科普、不能作为诊断治疗依据”等现代平台提示，**不能自动当作 2009 年原始 DOM 中已经存在的同一句提示**，除非取得历史 capture。

### 2.7 2010：纸媒“柯大夫信箱”被明确延伸为在线问答

2010 年凤凰健康报道“家庭医生在线”新版首页时，明确写到《家庭医生》的“柯大夫信箱”在网站中延伸为“柯大夫知道”，由医生团队回答网民健康问题。

来源：

- https://health.ifeng.com/news/qy/detail_2010_07/21/1810677_0.shtml

证据等级：**B（同期媒体/平台活动报道）**。

这个节点非常有旧网谱系意义：

```text
纸质读者来信
→ 编辑筛选
→ 专家回答
→ 期刊刊发
```

被重新映射为：

```text
网页提问
→ 平台路由/筛选
→ 医生回答
→ 在线持久页面
```

数字化改变了延迟、可检索性和规模，但“提问者—编辑/平台—专家—公众读者”这一基础结构具有连续性。

### 2.8 2010：好大夫经营者明确划出“互联网无法完成诊断/处方”的边界

2010 年《科学时报》采访好大夫在线 CEO 王航时，他明确把网站定位为帮助患者找到合适医生、与医生沟通的平台，并表示，在未见到患者、只根据叙述和部分检查结果的条件下，互联网不应被理解为完成准确诊断和开具处方。

来源：

- https://news.sciencenet.cn/sbhtmlnews/2010/7/234713.html

证据等级：**B（同期科技媒体采访；平台经营者观点）**。

报道同时给出医生数据库、实名交流医生和日交流量等平台口径；这些数据可用于理解规模，不当作独立审计统计。

### 2.9 2012：好大夫在线形成“医生发现 + 医患互动 + 预约转诊”组合

2012 年《理财周报》同期报道描述好大夫在线收录 3000 多家公立医院和近 30 万医生，并提供医生推荐、医患互动、预约转诊等服务。

来源：

- https://finance.sina.cn/sa/2012-04-09/detail-ikftssan7199992.d.html

证据等级：**B（同期商业媒体 + 平台口径）**。

这个组合说明“医生 profile”与“医疗事务”之间出现更多中间状态：

```text
profile viewed
→ consultation
→ recommendation
→ referral request
→ appointment
→ offline visit
```

绝不能把它们合成“网上看了医生”。

### 2.10 2015：研究边界开始逼近移动社交与更正式的互联网医疗

到 2015 左右，健康门户、医生平台、移动 App、微信/QQ 医患沟通和后来互联网医院的边界开始相互接近。

本文在 2015 截止，不向后扩成互联网医院史。后续正式复诊、处方、医保和配送的生活史由 `how-people-lived` 处理。

---

## 3. 事务状态机：一条公开健康问答到底证明什么

建议对任何健康 Q&A 页面使用以下状态链：

```text
physical person has symptom
→ user/account exists
→ question drafted
→ question submitted
→ platform receives request
→ moderation/triage
→ public question page exists
→ doctor/answerer assigned
→ answer written
→ answer published
→ patient reads answer
→ patient chooses action
→ appointment/referral requested
→ offline attendance
→ clinical examination
→ diagnosis
→ treatment/prescription
→ follow-up
→ outcome
```

历史网页通常只能证明中间的一小段。

### 永久状态差 1

```text
question page exists
!= patient identity verified
```

### 永久状态差 2

```text
patient says “我得了X病”
!= X is medically confirmed
```

### 永久状态差 3

```text
question submitted
!= platform accepted
!= doctor viewed
```

### 永久状态差 4

```text
answer published
!= target patient read it
```

### 永久状态差 5

```text
doctor response
!= formal clinical diagnosis
```

### 永久状态差 6

```text
doctor mentioned a medicine
!= prescription issued
!= medicine purchased
!= medicine taken
```

### 永久状态差 7

```text
referral / appointment request
!= appointment confirmed
!= patient attended
```

### 永久状态差 8

```text
public Q&A resolved on site
!= real disease resolved
```

### 永久状态差 9

```text
same patient nickname appears again
!= same legal person
```

### 永久状态差 10

```text
same doctor name appears in database
!= same affiliation at every historical date
```

---

## 4. 病友论坛：最需要同时保存“经验价值”与“临床边界”的旧网对象

### 4.1 病友群可以承担现实医院很难承担的生活知识交换

论坛/QQ群里的患者常交换：

- 检查实际流程；
- 哪座城市/医院有某专科；
- 药物日常副作用；
- 住院需要准备什么；
- 如何向家人解释疾病；
- 工作/上学时怎样处理症状；
- 情绪支持。

这些信息的价值不能因为它不是随机对照试验就被抹掉。

### 4.2 但群体一致意见不能自动升级成医学事实

2009 年中新网/大河网报道的“未知病毒”群体是一个极重要的历史反例：网名“求败”的男子六年间几乎每晚进入 QQ 病友群，群体成员互相交流相似症状，但多次医学检测没有支持他们坚持的疾病解释。

来源：

- https://www.chinanews.com/jk/jk-ysbb/news/2009/10-27/1931974.shtml

证据等级：**B/T1**。

研究的结论不是“患者是错的所以不值得研究”，而是：

> **数字社群既能减少孤独，也能把一种解释框架稳定成群体身份。**

因此：

```text
many matching narratives
!= epidemiological confirmation
```

### 4.3 “刘太医”案例显示网站、书籍、患者证言和汇款可以形成跨媒介反馈回路

2009 年中国新闻周刊相关报道记录，“刘太医”通过书籍、网站及患者口碑传播夸大治疗主张，调查后来发现其资质和药物存在严重问题；甚至在骗局已经受到揭露后，仍有部分接受者希望继续为其理论辩护。

来源：

- 中国新闻网稿凤凰转载，2009-07-22：
  https://news.ifeng.com/society/5/200907/0722_2579_1263481.shtml
- 2009-08-02 同期报道：
  https://news.sina.com.cn/c/2009-08-02/005916051205s.shtml

证据等级：**B**。

这提醒旧网考古不能只复原页面视觉，还要辨认：

```text
credential image shown
!= credential authentic

testimonial posted
!= treatment effective

forum repetition
!= independent evidence
```

---

## 5. 医生 profile 的权威不是一个 Boolean

一个历史医生页可能同时有多层权威：

1. 平台收录该姓名；
2. 平台声称已确认身份；
3. 医生实际控制该页面；
4. 医院/科室关系在该日期仍有效；
5. 医生有某领域专业资质；
6. 医生愿意线上回答；
7. 医生对当前患者有足够信息；
8. 回答属于科普、咨询或正式医疗行为。

所以建议未来 evidence schema 支持：

```yaml
doctor_profile:
  listed: true
  identity_verification: unknown
  account_control: supported_by_contemporary_post
  institution_affiliation_at_date: partially_verified
  consultation_mode: public_text
  clinical_transaction_status: unknown
```

而不是一个简单字段：

```yaml
verified_doctor: true
```

---

## 6. 旧健康网页最典型的 archive 偏差

### 6.1 `article survival / advice-context loss`

健康文章正文容易被 crawler 保存。

但以下内容更容易消失：

- 当时首页如何把它推荐给用户；
- 同页警示语；
- 作者认证状态；
- 评论；
- 关联疾病数据库；
- 当时广告；
- 是否后来更新过。

于是今天看到的文章可能保留“建议”，却丢掉它在当时界面里的风险边界。

### 6.2 `question-text survival / clinical-outcome loss`

公开提问可能长期留下：

> “我这种情况怎么办？”

但几乎永远不知道：

- 后来去了哪家医院；
- 正式诊断是什么；
- 是否按回复做了；
- 五年后病情怎样。

这会导致 **`public-question / private-outcome asymmetry`**。

### 6.3 `doctor-profile survival / availability loss`

医生页可以保存很多年，但：

```text
profile visible in archive
!= doctor accepting consultations at that moment
```

服务开关、排队状态、付费档位、响应时间和号源常由动态后台生成，最容易消失。

### 6.4 `forum-post survival / social-graph loss`

病友论坛正文可能留下；真正把人联结起来的：

- 私信；
- QQ 群号变化；
- 电话；
- 线下病友会；
- 管理员踢人/封号；
- 谁后来不再出现

却通常无法恢复。

### 6.5 `current disclaimer / historical disclaimer gap`

当前健康平台页面常附有：

> 内容仅供科普参考，不能作为诊断治疗依据。

如果当前页面的正文发布时间是 2009 年，**也不能因此推断这句免责声明在 2009 年的原始 DOM 中已经以相同位置、文字和视觉权重存在。**

必须有 historical capture 才能做这个页面层面的 claim。

### 6.6 `same URL / changed medical guidance gap`

医学知识会变化。

同一个疾病 URL 今天还存在，并不代表：

- 2006 年正文相同；
- 旧治疗方案仍被认可；
- 原作者仍署名；
- 页面没有被覆盖更新。

旧网研究应尽量记录内容时点，而不是只保存永久 URL。

---

## 7. 健康页面的动态资源尤其容易让现代回放产生误导

未来获得历史 capture 后，至少需要检查：

- charset / Content-Type；
- HTML form action；
- JS 是否负责提交问题；
- 登录态；
- iframe；
- doctor/profile 数据是否服务器端渲染；
- 图片 host；
- 广告脚本；
- 分页；
- 搜索 query 参数；
- 动态推荐接口；
- 评论/回复是否另一个 endpoint；
- Flash/ActiveX 是否出现；
- WAP 与桌面版是否共享账号/内容。

在没有历史 capture 的情况下，本轮**不猜** 39.net、好大夫或家庭医生在线具体年份所使用的：

- GB2312 / GBK / UTF-8；
- IE-only 技术；
- table / frameset；
- ASP/PHP/JSP；
- AJAX；
- 某个具体 URL pattern。

这些必须由历史 artifact 支持。

---

## 8. 证据登记

| Claim | Source | Grade | 能证明 | 不能证明 |
|---|---|---|---|---|
| 39.net 官方把上线时间记为 2000-03-09 | `corp.39.net` 发展史 | A/platform | 平台当前历史叙述 | 2000 首页 DOM/访问量 |
| 2004 年官方历史称推出 39 健康搜 | `corp.39.net` | A/platform | 产品节点 | 历史界面/排名算法 |
| 2007 年官方历史称推出疾病/药品/医院医生数据库 | `corp.39.net` | A/platform | 数据库产品节点 | 字段和 URL schema |
| 2008 年官方历史称健康问答推出 | `corp.39.net` | A/platform | 问答产品存在 | 每个问题均由医生回答 |
| 2009 医生把好大夫虚拟诊室用于替代私人电话 | `haodf.com` 同期医生文章 | A/T0 | 实际使用动机 | 正式诊断/处方发生 |
| 2010 “柯大夫信箱”延伸为网络问答 | 凤凰健康同期报道 | B | 纸媒→Web 产品谱系 | 完整事务状态 |
| 2010 好大夫经营者称互联网沟通不能替代完整诊断/处方 | 《科学时报》 | B | 当时平台自我边界 | 全行业规则 |
| 2012 好大夫有医生数据库、互动、预约转诊 | 《理财周报》 | B | 服务组合存在 | 全国患者使用比例 |
| 2009 “未知病毒”病友群存在长期同伴确认 | 中新网/大河网 | B/T1 | 群体经验与医学检测之间冲突 | 对个体症状的临床解释 |
| 2009 “刘太医”网站/书籍/口碑形成传播链 | 同期新闻 | B | 传播与资质造假调查 | 每个网络用户受影响程度 |

---

## 9. 隐私：健康 old-Web 是本仓最需要“故意不完整”的对象之一

### 9.1 历史公开不等于今天应重新公开

一个 2008 年病友论坛用户可能公开写过：

- HIV 状态；
- 精神疾病；
- 生殖健康；
- 性经历；
- 家庭冲突；
- 儿童病史；
- 真实姓名或手机号。

这些内容即使被 archive 保存，也不代表本仓需要重新建立姓名索引或批量镜像。

### 9.2 研究平台机制优先于恢复个人隐私内容

优先保存：

- URL pattern；
- forum/category structure；
- form fields；
- moderation rules；
- doctor verification model；
- public/private state boundaries；
- aggregate behavior。

仅在必要时引用最小化、匿名化的个人材料。

### 9.3 删除和消失本身可能是合理隐私结果

对于医疗史，archive gap 不总是“应当修复的损失”。

一个患者后来删除自己多年前的公开病史，可能正是她应拥有的退出权。

因此：

> **historical completeness 与 personal privacy 在本案中存在真实冲突。**

不应默认“能恢复多少就恢复多少”。

---

## 10. 本轮 archive 检索与负结果

本轮搜索了：

- `39.net` / `www.39.net` 的历史页面线索；
- 2004 健康搜索节点；
- 2008 健康问答节点；
- `haodf.com` 2009 医生主页/虚拟诊室；
- 2010 家庭医生在线/柯大夫知道；
- Wayback 相关索引线索。

当前可用搜索结果提供了平台官方历史、同期媒体和今天仍可访问的旧文章，但没有形成一份满足 `docs/METHOD.md` 第 4 节的 verified archive capture。

因此只能记录：

> **M1 verified historical Chinese health portal / patient-Q&A capture: NOT ACHIEVED IN THIS SLICE.**

不能写：

> “Wayback 没保存 39.net。”

因为这次没有完成足以支持这种负命题的系统性 archive 查询与 replay 检查。

### 下一轮可优先验证的 capture 目标

只列已由来源确认的 host / product family，不猜具体历史 endpoint：

1. `www.39.net`：2000、2004、2007、2008、2010 多时点；
2. 39 健康搜索相关公开入口：先从同期新闻/帮助页反推 exact URL；
3. 39 健康问答：先从 2008 同期页面取得 exact original URL；
4. `haodf.com`：2009 医生虚拟诊室及医生主页；
5. 家庭医生在线 2010 “柯大夫知道”入口。

每个 verified capture 都要记录：

- original URL；
- capture URL；
- capture datetime；
- access date；
- HTTP/replay state；
- redirect/login/error 状态；
- charset/Content-Type；
- 主文档和子资源；
- form/link endpoint；
- browser assumption；
- 第二历史时点。

---

## 11. old-Web 与生活史之间最重要的交叉结论

### 11.1 “网页里有疾病”与“现实里有人得到照护”之间隔着很多系统

旧网最容易保存：

```text
病名
文章
医生名字
一个问题
一个回答
```

现实生活真正依赖：

```text
能不能找到医生
能不能挂号
能不能去医院
检查做不做得起
诊断是否明确
药有没有
医保能不能报
几个月后还能不能继续复诊
```

因此 health Web archaeology 如果只恢复页面，会系统性高估“信息”而低估“执行”。

### 11.2 Internet 的确增加了患者的行动空间，但不是单向“民主化医疗”

它同时增加：

- 可搜索知识；
- 病友支持；
- 医生可达性；

以及：

- 错误信息；
- 过度自我诊断；
- 医生注意力压力；
- 隐私泄露；
- 平台认证和商业排序的新不透明性。

### 11.3 最值得保存的也许不是一个“医学结论”，而是当时人怎样组织不确定性

一个 2008 年患者页面的历史价值，常常不是判断她最后得了什么病，而是看到：

- 她当时知道哪些病名；
- 她为什么来网上问；
- 她相信什么来源；
- 她怎样描述身体；
- 其他患者如何回应；
- 医生如何划定在线回答的边界。

这比把旧论坛错误地改造成“历史病例库”更符合本仓的研究目标。

---

## 12. 已证实 / 高概率 / 不知道

### 已证实

- 39 健康网官方历史把正式开通时间记为 2000-03-09；
- 官方历史记录 2004 健康搜索、2007 多类健康数据库、2008 健康问答、2009 专家博客、2010 WAP 等节点；
- 2009 至少有医生公开把好大夫虚拟诊室作为院外沟通渠道，并明确用于减少私人电话侵扰；
- 2010 同期报道明确把纸媒“柯大夫信箱”与在线“柯大夫知道”连接起来；
- 2010 好大夫经营者公开强调在线交流不能简单等同完整诊断/处方；
- 2009 同期报道证明 QQ 病友群既能形成长期互助，也可能形成未经临床证实的共同疾病解释。

### 高概率，但仍需 historical capture 细化

- 2000s 中后期健康门户已经把疾病、药品、医院、医生、文章、问答和论坛放进一个相互链接的信息架构；
- 问答和医生主页的动态事务状态远比今天静态 survivor 页面显示的复杂；
- WAP/移动入口在 2010 前后开始改变健康信息访问地点和频率。

### 不知道

- 2000、2004、2008 各时点 39.net 具体 DOM、编码与浏览器表现；
- 39 健康问答最初版 exact URL、form action、审核和医生路由实现；
- 2009 好大夫医生页在当年页面上具体有哪些 disclaimer、按钮和咨询状态；
- 当时患者从公开问答转化为线下就诊的比例；
- 早期病友论坛中有多少真实关系转移到 QQ/电话/线下；
- 被 archive 保存的公开患者文字相对于全部真实用户有多强的选择偏差。

---

## 13. 本研究包改变了 old-Web 的哪一点理解

健康旧网尤其提醒我们：**“网页保存下来”与“事务保存下来”不是一回事。**

在普通门户新闻里，一篇正文保存完整可能已经恢复了主要内容；但在健康问答里，最关键的现实过程恰恰发生在页面之外：患者有没有去医院、医生到底诊断了什么、药是否拿到、疾病后来如何。

于是，一个保存得异常完整的旧健康网站，仍然可能只恢复了医疗生活最公开、最容易被 crawler 看见的一层。

最准确的考古目标不是把它重新做成一个“还能使用的网上医院”，而是保留这些边界：

> **2008 年这个人确实能在网页上提出问题；但我们不能因为问题和回复今天还在，就替她补写一个从未被档案保存下来的诊断、治疗和结局。**
