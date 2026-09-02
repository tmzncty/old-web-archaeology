# RECRUITMENT_PROCESS_STAGE_AND_CHANNEL_SWITCHING_2003_2006.md

## 目的

配套生活史研究：

- <https://github.com/tmzncty/how-people-lived/blob/main/topics/screen-before-travel-and-staged-mobility-online-recruitment-2003-2006.zh-CN.md>

上一份方法文档已经要求把招聘职位页、简历数据库、机构流程和线下录用区分开：

- [RECRUITMENT_LISTING_AND_RESUME_LIFECYCLE_1999_2004.md](RECRUITMENT_LISTING_AND_RESUME_LIFECYCLE_1999_2004.md)

2003—2006 年的同时代材料又暴露了一个新的考古问题：

> **一次历史招聘流程可能跨越多个平台、设备、通信媒介和线下场所。**

例如：

```text
招聘网站看见职位
→ 在线表单投简历
→ 电话通知
→ 浏览器完成在线笔试
→ QQ 语音/视频初面
→ 真实到场终面
→ 线下核验证件 / 签约
```

如果今天只保存到第一张职位网页，我们极容易把“网页”误认为“完整招聘系统”；如果保存到一个招聘平台的产品说明，又可能误认为所有后续步骤都发生在平台内部。

因此本文件新增一个研究单位：

> **recruitment process graph（招聘过程图）**

它不以一个 URL 或一个平台为边界，而以**同一次招聘中每个阶段用了什么渠道、是否要求同步在线、是否要求真实移动**为边界。

---

## 1. 最重要的新禁止：same recruitment case ≠ same platform

2006 年《楚天金报》报道一名准备跳槽去上海的求职者通过 **QQ 视频/语音**与企业总经理面试。

来源：

- 楚天金报 / 新浪，2006-01-18，《网上远程招聘方便求职者 网上笔试视频面试》：<https://news.sina.com.cn/s/2006-01-18/06188013957s.shtml>

证据等级：**B — 同时代新闻 + 同期用户操作描述。**

这条材料只足以证明：

> 某次异地求职中的面试阶段使用了 QQ 视频/语音。

它**不能**证明：

- 职位最初发布在 QQ；
- 简历通过 QQ 提交；
- 招聘网站原生支持视频；
- QQ 保存了完整招聘记录；
- 所有后续面试仍在线进行。

因此旧网考古中必须避免这种错误写法：

> “某招聘网站在 2006 年已经支持视频面试。”

除非有该招聘网站自己的同时代产品证据。

更安全的写法是：

> “同期用户材料显示，一次网络招聘流程中的面试环节可以转入 QQ 视频/语音等外部即时通信工具。”

---

## 2. 用 process stage 代替“网站有 / 没有招聘功能”的二分法

建议把一次招聘至少拆成以下阶段：

```yaml
recruitment_process:
  discovery:
  employer_research:
  application:
  acknowledgement:
  initial_screening:
  test:
  interview_1:
  interview_2:
  credential_verification:
  offer:
  contract:
  medical_exam:
  onboarding:
```

每个阶段再记录：

```yaml
channel:
platform_or_service:
interaction_mode: asynchronous | synchronous | offline | unknown
location_requirement:
travel_required: true | false | unknown
login_required:
identity_requirement:
hardware_requirement:
bandwidth_requirement:
privacy_requirement:
evidence_grade:
confidence:
```

这种设计比单个 `application_channel` 更接近真实历史流程，因为一个人可以在同一次求职中连续切换：

```text
Web → Email → 电话 → QQ → 现场
```

---

## 3. 2003 的反例说明：online stage existence ≠ full-process substitutability

2003 年 SARS 期间，网络招聘被大量尝试，但《中国青年报》在 6 月人才市场恢复后记录：

- 北京两个固定人才市场恢复首日附近共接待近 5000 人；
- 求职者“小白”此前多次网上求职，要么没有合适职位，要么投出的简历没有回复；
- 其他求职者也报告长期网上投递无回应；
- 企业抱怨网络简历匹配度和真实性问题，仍依赖面对面判断。

来源：

- 中国青年报 / 新浪，2003-06-27：<https://news.sina.com.cn/c/2003-06-27/03421231604.shtml>

证据等级：**B。**

因此一个招聘站点即使具备：

```text
职位展示
+
简历投递
```

也不能推断：

```text
筛选
+
面试
+
核验
+
签约
```

已经能够远程完成。

对旧网页的 claim 应始终限制在证据能证明的阶段。

---

## 4. 2005—2006 出现的关键变化：更多后端阶段可以远程，但方式不统一

### 4.1 远程视频面试可以依赖机构共享终端

2005 年 10 月，《湖北日报》记录武汉本地大学生在武汉科技会展中心通过网络视频与浙江宁波企业面试。

来源：

- 湖北日报 / 新浪，2005-10-22：<https://news.sina.com.cn/c/2005-10-22/07517234530s.shtml>

证据等级：**B。**

2005 年 12 月 CERNET 报道，北京毕业生就业服务机构计划提供可同时供约 1000 名大学生使用的远程面试系统，毕业生在专门计算机房里与外省市单位视频交流。

来源：

- CERNET，2005-12-20：<https://www.edu.cn/xin_xi_zi_xun_1625/20060323/t20060323_155210.shtml>

证据等级：**B / institution-hosted contemporaneous report。**

因此建议额外记录：

```yaml
access_venue:
  home: false/true/unknown
  cybercafe: false/true/unknown
  school_lab: false/true/unknown
  employment_service_center: false/true/unknown
  convention_center: false/true/unknown
  borrowed_device: false/true/unknown
```

不能把“网络视频面试”自动理解成“用户在自己家电脑上视频面试”。

### 4.2 远程筛选可以是长时同步笔试

2006 年同一篇《楚天金报》报道中，一名教师参加天津报社的网络笔试：招聘方从简历中筛出 80 人，要求在指定晚上 18:30—21:00 在线答题，再选 20 人进入面试。

来源：

- <https://news.sina.com.cn/s/2006-01-18/06188013957s.shtml>

证据等级：**B。**

这说明“能打开网页”与“能完成招聘阶段”不能混为一谈。

在线笔试可能要求：

- 长时间稳定连接；
- 固定时段可用；
- 相对安静的环境；
- 能输入长文本；
- 浏览器/脚本兼容；
- 中途不断线。

因此建议增加：

```yaml
session_requirement:
  duration_minutes:
  fixed_start_time: true/false/unknown
  persistent_connection: true/false/unknown
  uninterrupted_session: true/false/unknown
```

共享网吧终端“理论上能打开页面”不能直接证明它适合完成这种考试。

---

## 5. 新证据模型：stage-specific access（阶段特定可及性）

早期网络接入研究常用：

```text
有网 / 没网
```

但招聘过程需要更细的阶梯：

```text
能看职位
→ 能注册账号
→ 能上传/粘贴简历
→ 能保持可联系状态
→ 能接收电话/Email通知
→ 能参加长时在线测试
→ 能语音/视频同步交流
→ 能提交/验证证件
→ 能最终真实到场
```

因此一个历史个案应该记录：

```yaml
stage_access:
  listing_view: confirmed/possible/unknown
  account_registration: confirmed/possible/unknown
  resume_submission: confirmed/possible/unknown
  asynchronous_contact: confirmed/possible/unknown
  synchronous_text: confirmed/possible/unknown
  long_session_test: confirmed/possible/unknown
  audio_interview: confirmed/possible/unknown
  video_interview: confirmed/possible/unknown
  credential_verification: confirmed/possible/unknown
  physical_attendance: confirmed/possible/unknown
```

这比一句“当时已经能网上求职”信息量更高。

---

## 6. 新规则：remote recruitment ≠ remote work

历史材料里的“远程招聘”“网络面试”“网上笔试”很容易被今天的远程工作经验重新解释。

必须分开：

```yaml
recruitment_location_mode: remote | hybrid | onsite | unknown
employment_location_mode: remote | onsite | hybrid | unknown
```

2005—2006 的材料证明的是招聘某些阶段可以远程，不证明录用后允许远程办公。

除非有合同、职位说明、公司制度等独立证据，否则：

> **远程面试绝不能作为远程工作证据。**

---

## 7. 新规则：platform-native feature ≠ externally mediated practice

旧网研究常见一种功能归属错误：

1. 在某招聘网站看到职位；
2. 同期用户后来用 QQ 面试；
3. 研究者把“视频面试”写进招聘网站功能列表。

这是错误的。

建议每个 stage 单独记录：

```yaml
feature_origin:
  platform_native: true/false/unknown
  external_service: true/false/unknown
  institutional_system: true/false/unknown
  ordinary_telephone_network: true/false/unknown
```

例如：

```yaml
interview_1:
  channel: video
  platform_or_service: QQ
  feature_origin:
    platform_native: false
    external_service: true
```

只有招聘网站官方帮助页/产品文档明确显示自身集成视频功能时，才能标 `platform_native: true`。

---

## 8. Archive 的系统性盲点：最容易保存的是流程前端

公共 Web archive 通常更容易保存：

- 招聘首页；
- 职位列表；
- 单个职位页；
- 帮助页；
- 活动专题；
- 公开企业介绍。

更难保存：

- 登录后的简历库；
- 一次性在线笔试；
- 提交成功页；
- 电话邀约；
- SMS；
- QQ 私聊/语音/视频；
- 机构内部视频会议系统；
- 面试后的现场核验；
- 录用决定。

因此：

> **archived front-end completeness ≠ historical process completeness**

如果研究者只根据 Wayback，会系统性地看到“职位发布”，却看不见“这个职位后来怎样变成一次电话、一场 QQ 面试、一次坐火车的真实移动”。

这不是普通资源缺失，而是一种**流程阶段型保存偏差（process-stage preservation bias）**。

建议在招聘案例中加入：

```yaml
preservation_bias:
  discovery_stage_well_preserved: true/false/unknown
  application_stage_preserved: true/false/unknown
  private_contact_stage_preserved: true/false/unknown
  synchronous_interview_stage_preserved: true/false/unknown
  offline_outcome_preserved: true/false/unknown
```

---

## 9. “没有留下 QQ / 电话记录”不能反推流程没发生

如果一份 2006 年招聘页被 Wayback 保存，而没有保存对应 QQ 聊天记录：

不能写：

> “该招聘流程没有在线面试。”

最多只能写：

> “目前保存的公开 Web artifacts 没有证明该次招聘存在在线面试。”

私人即时通信、电话和机构内部系统原本就具有较低公共档案可见性。

这和本仓已有规则一致：

> `not observed in artifact ≠ absent in biography`

在招聘研究中应进一步具体化为：

> `not observed in public web archive ≠ absent from the recruitment process`

---

## 10. 同一次招聘需要建立 channel-switching graph

推荐最小结构：

```yaml
case_id: example-2006-001

stages:
  - stage: discovery
    channel: web
    service: recruitment-site
    evidence_grade: A/B/C/D

  - stage: application
    channel: web-form
    service: recruitment-site
    evidence_grade: A/B/C/D

  - stage: acknowledgement
    channel: telephone
    service: pstn/mobile
    evidence_grade: A/B/C/D

  - stage: test
    channel: web
    service: unknown
    synchronous: true
    travel_required: false
    evidence_grade: B

  - stage: interview_1
    channel: video-voice
    service: QQ
    synchronous: true
    travel_required: false
    evidence_grade: B

  - stage: interview_2
    channel: physical
    service: onsite
    travel_required: true
    evidence_grade: unknown
```

关键不是把未知项补齐，而是把**未知阶段显式留空**。

---

## 11. 生活史上的意义不能从网页本身直接推出

同时代新闻把远程招聘描述为省时、省力、减少舟车劳顿，但本仓仍应把这些分层：

### 可以由具体流程直接支持

- 某次面试双方没有跨城到同一地点；
- 某次笔试通过互联网在指定时间完成；
- 某个机构提供共享远程面试终端。

### 可以合理推断

- 这些步骤减少了该阶段的跨城到场需求；
- 对没有私人视频设备的人，机构共享终端提高了服务可及性。

### 不能仅凭网页/新闻推出

- 平均每个求职者节省多少钱；
- 远程招聘普及率；
- 视频面试提高录用概率；
- 网络招聘造成全国职业流动率上升；
- 远程招聘意味着工作本身远程化。

生活史上的更大解释应交给 `how-people-lived`，旧网仓主要保存**技术/平台/流程证据合同**。

---

## 12. 海外对照给出的一个方法提醒：招聘数字化本来就按阶段不均匀推进

美国劳工统计局对 2001 年互联网求职者的统计显示：

- 92.2% 看在线广告/职位；
- 68.5% 研究潜在雇主；
- 37.4% 在职位服务中发布简历。

来源：

- U.S. Bureau of Labor Statistics, 2002-11-21：<https://www.bls.gov/opub/ted/2002/nov/wk3/art04.htm>

到 2003 年，BLS 记录：

- 92.6% 看在线职位；
- 70.2% 研究雇主；
- 57.0% 在线提交简历/申请；
- 41.0% 在职位服务发布简历。

来源：

- U.S. Bureau of Labor Statistics, 2005-08-16：<https://www.bls.gov/opub/ted/2005/aug/wk3/art02.htm>

这些美国数字不能直接用于推断中国，但它们提供一个跨国可复用的考古框架：

> **不要问“招聘什么时候上网”，而要问“招聘的哪一个阶段、对哪一群人、在什么设备和网络条件下上网”。**

---

## 13. 对 2003—2006 中文招聘旧网页的推荐字段

```yaml
object_type: recruitment_process
subject:
period:

platforms_involved:
external_services_involved:
offline_venues_involved:

stages:
  discovery:
    channel:
    platform:
    synchronous:
    travel_required:
    access_venue:
    evidence_grade:
  application:
    channel:
    platform:
    evidence_grade:
  screening:
    channel:
    platform:
    evidence_grade:
  test:
    channel:
    platform:
    duration_minutes:
    fixed_time:
    travel_required:
    evidence_grade:
  interview:
    channel:
    platform:
    audio_required:
    video_required:
    travel_required:
    access_venue:
    evidence_grade:
  verification:
    channel:
    physical_documents_required:
    evidence_grade:
  offer:
    channel:
    evidence_grade:
  onboarding:
    location:
    travel_required:
    evidence_grade:

remote_recruitment: true/false/partial/unknown
remote_employment: true/false/unknown

archive_visibility:
  public_pages:
  authenticated_pages:
  private_messages:
  synchronous_sessions:
  offline_outcome:

unknowns:
privacy_risk:
hindsight_risk:
```

这不是要求每个案例都填满，而是防止研究者把一个保存良好的职位页误当成完整流程。

---

## 14. 证据等级与可写 claim

### B 级可以支持的窄 claim

> 2005 年同期媒体记录了武汉本地大学生通过网络视频与浙江企业进行跨地区面试。

> 2006 年同期报道中，一名计划跳槽去上海的求职者通过 QQ 视频/语音与企业负责人进行了远程面试。

> 2006 年同期报道中，一名求职者在远程完成了指定时段的互联网笔试。

### 不应扩张为

> 2005 年中国网络招聘已经普遍实现全流程线上化。

> 2006 年招聘网站普遍内置视频面试。

> 2006 年异地工作已经不需要跨城。

---

## 15. 隐私与再发布

招聘流程经常涉及：

- 姓名；
- 手机；
- Email；
- QQ 号；
- 学校；
- 单位；
- 工作经历；
- 求职意向；
- 录用结果。

即使旧新闻或 archive 曾公开这些内容，本仓也只保留支持历史机制所必需的最少信息。

尤其不要：

- 收集并重新发布普通求职者历史 QQ 号码；
- 重建历史简历数据库；
- 公开旧手机号/住址；
- 为了“还原招聘流程”尝试联系当年普通用户；
- 把私人 QQ/Email 残片拼成可搜索个人档案。

本文件使用同期报道中的化名/称呼时，仅用于说明流程机制，不扩展身份识别。

---

## 16. 后见之明风险

### 风险 A：把 2020 年 Zoom/腾讯会议式云招聘倒投到 2005 年

2005 年远程面试可能依赖专门机房、会展中心、QQ、桌面摄像头和机构网络。设备与场地本身就是历史条件。

### 风险 B：把 Web archive 当成完整通信档案

招聘后端很容易转到电话、短信、QQ 和现场，这些本来就不在公共网页存档的优势范围内。

### 风险 C：把一次创新案例当成普及

远程视频面试被新闻报道，可能正因为它稀少、新奇。`exists` 不能跳到 `popular`。

### 风险 D：把渠道能力写成使用效果

“能视频面试”只证明技术和流程可行，不证明求职者因此获得工作。

---

## 17. 本规则改变旧网考古的哪一点

过去很容易把一个历史网站作为完整研究单位：

```text
这个网站有什么页面？
这个网站有什么功能？
```

招聘材料说明，对普通人的真实网络生活，更重要的问题有时是：

```text
这个人为了完成一件事
先后穿过了哪些网站、账号、通信网络和现实场所？
```

因此，旧网考古除了 **site archaeology**，还需要在合适对象上做：

> **workflow archaeology（工作流考古）**。

对于招聘，它尤其意味着：

> **网页保存了机会的入口，却往往没有保存一个普通人怎样从那个入口一步步走到真实工作。**

这段缺失不能用想象补齐；但可以通过同期新闻、帮助文档、教程、机构流程说明和用户自述，谨慎地重新建立阶段图，并把每一步证据等级分别标出。

---

## 来源

1. 中国青年报 / 新浪，2003-06-27，《非典难撼现场招聘霸主地位 网上招聘要跨的门槛还很多》：<https://news.sina.com.cn/c/2003-06-27/03421231604.shtml>
2. 湖北日报 / 新浪，2005-10-22，《图文：本地大学生借助网络视频参加浙江面试》：<https://news.sina.com.cn/c/2005-10-22/07517234530s.shtml>
3. CERNET，2005-12-20，《网络面试拓宽就业渠道 视频业务又添新用途》：<https://www.edu.cn/xin_xi_zi_xun_1625/20060323/t20060323_155210.shtml>
4. 楚天金报 / 新浪，2006-01-18，《网上远程招聘方便求职者 网上笔试视频面试》：<https://news.sina.com.cn/s/2006-01-18/06188013957s.shtml>
5. U.S. Bureau of Labor Statistics, 2002-11-21, *Job-search methods on-line*: <https://www.bls.gov/opub/ted/2002/nov/wk3/art04.htm>
6. U.S. Bureau of Labor Statistics, 2005-08-16, *Methods of Internet job searching*: <https://www.bls.gov/opub/ted/2005/aug/wk3/art02.htm>

---

*本规则初稿由 AI 辅助整理。任何具体平台 case 仍应优先寻找 A 级历史页面/帮助文档，并按 `docs/METHOD.md` 逐 claim 复核。*