# DATING_PROFILES_SEARCH_FILTERS_OFF_PLATFORM_HANDOFF_AND_RELATIONSHIP_OUTCOME_GAPS_2002_2012

> 适用范围：约 2002–2012 年中文旧网中的征友/征婚页面、婚恋网站用户资料、搜索与筛选、心理测评/推荐、站内联系、身份认证，以及关系从网站迁移到 QQ/MSN/电话/短信/线下后的证据断裂。
>
> 跨仓生活史主文档：
> <https://github.com/tmzncty/how-people-lived/blob/main/topics/searchable-courtship-partner-search-radius-and-profile-legibility-china-1981-2025.zh-CN.md>
>
> 本文不写“中国婚恋史总论”，也不扩张为 2012 年以后 App / 直播 / 算法婚恋史。这里只回答一个旧网考古问题：
>
> **当一个普通人被旧婚恋网站表示成一个可搜索 profile 时，今天保存下来的 Web artifact 到底能证明关系形成链的哪一步？**

---

## 0. 与既有文档的边界

本仓已经有若干相关但不同的 evidence contract：

- `CONTACT_ENDPOINT_LIFECYCLE_1997_2003.md`：联系方式本身的生命周期；
- `CONTACT_STACK_AND_CHANNEL_HANDOFF_1998_2002.md`：Email、电话、QQ 等通道切换；
- `DOCUMENT_GATED_SHARED_ACCESS_AND_IDENTITY_BINDING_2001_2005.md`：证件、共享终端与身份绑定；
- `AFFILIATION_CREDENTIAL_AND_ACCOUNT_LIFECYCLE_2001_2009.md`：机构身份和账号生命周期；
- `APPLICATION_STATE_ELIGIBILITY_AND_ROUTE_PORTFOLIO_2003_2015.md`：申请状态与资格，不是关系状态；
- `ABANDONED_APPLICATIONS_AND_NEGATIVE_STATE_SURVIVAL_2007_2015.md`：负状态和放弃保存偏差；
- `JOB_BOARD_ADDRESSABILITY_RESUME_DATABASE_GAPS_AND_APPLICATION_ATTENTION_1999_2009.md`：职位/简历数据库和申请事件不可见性。

本文不重复这些。

新增研究单位是：

> **profile representation + bilateral discovery + reciprocal contact + off-platform handoff + relationship outcome**。

婚恋 artifact 的特殊之处在于：

1. 一个 profile 通常同时包含身份 claim、偏好 claim 和自我展示；
2. 搜索结果是双向关系的起点，而不是结果；
3. “匹配”必须经过另一方独立同意；
4. 真正关系极容易从网站迁移到 QQ、MSN、短信、电话与线下；
5. 越接近真实亲密关系，证据越私密，也越不应该被公共 archive 保存。

---

# 1. 研究单位：不要把“征婚页面”当成一段关系

建议把一次网络婚恋流程至少拆成：

```text
platform
→ account
→ profile version
→ profile visibility
→ search / recommendation event
→ profile view
→ expression of interest / message
→ recipient notice
→ reply / reciprocal interest
→ contact handoff
→ first meeting
→ repeated meetings
→ relationship
→ co-residence / marriage / breakup / dormancy
```

建议记录字段：

```yaml
platform:
account_id_status:
profile_url:
profile_version_time:
visibility_scope:
profile_fields:
verification_level:
search_endpoint:
search_query_state:
recommendation_state:
contact_method_on_site:
off_platform_endpoint_type:
meeting_evidence:
relationship_evidence:
outcome_evidence:
archive_capture:
source_grade:
confidence:
privacy_notes:
```

核心边界：

> **profile exists ≠ profile active**

> **profile visible ≠ profile discovered**

> **search result ≠ mutual match**

> **message sent ≠ message read**

> **reply ≠ meeting**

> **meeting ≠ relationship**

> **relationship ≠ marriage**

这套状态机必须在以后所有婚恋/征友旧网 case 中复用。

---

# 2. 2002：我们有“网站样本”的同期描述，但没有因此获得原始交友网站 capture

2002 年自由亚洲电台一篇同期评论称，作者各取三份城市报纸和一个名为“交友驿站”的网站各 30 条征婚信息作比较。

作者观察：

- 报纸征婚较常按年龄、学历、经济状况、婚史等固定条件写；
- 网站上的自我描述篇幅通常更长；
- 其网站样本明显偏年轻；
- 作者把这种差异部分归因于 Web 不受纸面版面约束和当时上网条件。

来源：

- 《征婚广告里的中国人（一）》，2002-08-30：
  <https://www.rfa.org/mandarin/pinglun/88525-20020830.html>

### 证据等级

**B：同期二手评论 + 小样本。**

### 目前能写的 claim

> 2002 年已有作者把一个中文征友网站与报纸征婚放在同一分析框架中，并观察到网站样本的篇幅/自述形态与纸媒样本不同。

### 目前不能写的 claim

- `交友驿站` 在 2002 年具体 URL 是什么；
- 它的 profile template 长什么样；
- 是否需要账号登录；
- 字符集、JS、frameset、浏览器要求；
- 这些 30 条样本今天是否仍有 archive capture；
- 作者记录的比例是否代表平台总体。

因此：

> **contemporary description of a site ≠ preserved site artifact**

这一条尤其重要。

以后若找到 archive locator，必须实际打开 capture，再升级为 A；不能把 2002 评论里“网站存在”直接写成已复原页面。

---

# 3. 2006：心理测评 / 智能匹配首先只能作为 product claim

2006 年《中国青年报》同期报道百合网新版时，称该站设计了心理测试与智能匹配系统，并报道其用户规模和创业背景。

来源：

- 中国青年报，2006-01-24，经新浪保存：
  <https://tech.sina.com.cn/i/2006-01-24/1004828139.shtml>

### 证据等级

**B：同期新闻，其中包含平台产品 claim。**

### 证据边界

可以写：

> 当时平台公开把心理测评/智能匹配作为服务功能。

不能写：

> 算法真的提高了关系成功率。

也不能凭新闻页直接推断：

- 历史测试表单具体字段；
- 推荐排序算法；
- 一个用户得到哪些候选人；
- 推荐是否根据完整 profile 实时计算；
- 浏览器/JS 是否影响结果。

因此：

> **matching feature advertised ≠ matching algorithm recovered**

> **recommendation returned ≠ relationship success**

---

# 4. 2008：同期材料第一次把“搜索伴侣”明确呈现成数据库查询动作

2008 年中国青年报稿件的同期转载保存了一名用户操作描述：用户在婚恋网站搜索栏输入年龄、学历、月薪等条件，随后页面返回几十个符合条件的候选档案；他把自主搜索、随时登录和更多选择视为使用理由。

来源：

- 2008-03-03 同期转载：
  <https://www.dzwww.com/xinwen/guoneixinwen/200803/t20080303_3228860.htm>

### 证据等级

**B：同期新闻 + 同期第一人称使用描述。**

### 可确认的交互模型

至少可以确认到：

```text
user specifies structured criteria
→ platform executes search
→ multiple candidate profiles displayed
→ user selects which profiles to inspect/contact
```

这比“网站有征婚页面”强得多。

它证明专业婚恋网站的核心 artifact 已经不只是静态个人页，而包括：

- searchable database；
- search form；
- query parameters；
- result list；
- profile detail；
- login-dependent action。

### 但我们仍未恢复这次具体 query

新闻描述不是 transaction log。

我们不知道：

- 用户到底输入了什么完整值；
- 搜索参数是 GET 还是 POST；
- 结果 URL 是否稳定；
- 哪些候选人当时返回；
- 排序逻辑；
- 用户随后点了谁；
- 谁回复了。

因此：

> **reported search event ≠ archived search state**

---

# 5. 搜索结果页比 profile 页更容易产生“state illusion”

历史婚恋站搜索结果通常可能依赖：

- 当前账号；
- 性别/地区/年龄偏好；
- 登录状态；
- profile visibility；
- 当时数据库内容；
- 活跃时间；
- 付费权限；
- 排序/推荐逻辑。

即使今天 archive 到一个搜索 URL，也必须问：

```text
是静态 landing page？
是未登录提示？
是 archive 保存的一次结果？
是回放时重新执行了现代请求？
是错误页面？
是模板壳？
```

所以：

> **search URL survived ≠ historical result set recovered**

如果搜索使用 POST、cookie 或短 session，公共 archive 甚至可能从未保存结果集合。

这类缺失可以命名：

## query-state survival gap：查询状态存续缺口

> 一个动态数据库服务最有历史意义的不是“搜索按钮长什么样”，而是某一时刻数据库里有哪些可发现的人；后者往往比 HTML 壳更难保存。

---

# 6. profile 本身是版本化对象，不是一个永恒的人

婚恋资料可能反复修改：

- 年龄会自然变化；
- 城市会迁移；
- 工作会变化；
- 收入可能重填；
- 照片会更换；
- 自我介绍会优化；
- 择偶范围会收窄/放宽；
- 账号会暂停、注销、重新启用。

因此一张 2008 capture 只能证明：

> **该 capture 所保存的那一版 profile 在该时点以这种形式可见。**

不能把它写成一个人的固定属性。

建议字段：

```yaml
profile_version:
  observed_at:
  capture_datetime:
  field_values:
  visibility:
  status:
  change_relation_to_other_versions:
```

核心边界：

> **profile value at t1 ≠ person attribute for all t**

这也适用于“择偶要求”。

一个人后来修改要求，不能倒推他此前“其实一直这样想”。

---

# 7. 2008 行业调查：只能证明网络婚恋已成为显著服务形态，不能当 Web population census

《2008 中国网民婚恋调查报告》相关页面称：

- 实际答卷 225,343；
- 有效答卷 154,386；
- 45.5% 的有效答卷参与者称使用过婚恋网站为主的网络征婚方式；
- 调查采用线上与线下结合。

来源：

- 中国互联网协会当前保存页：
  <https://www.isc.org.cn/article/12735.html>
- CCTV 同期转载：
  <https://315.cctv.com/20080216/101787.shtml>

### 证据等级

**B：同期行业/协会材料。**

### 不能做的事情

不要用它给 archive dataset 人为加权：

```text
45.5% used dating sites
→ therefore 45.5% of young Chinese had dating profiles
```

这是错误的。

调查本身针对网民/参与者且强烈自选择，婚恋行业机构参与明显。

它只适合支持：

> 到 2008 年，网络婚恋已经有足够规模与公共可见性，形成大规模行业调查、专业网站与稳定产品形态。

---

# 8. profile field 是平台 schema，不是“社会真实”的透明镜子

当一个网站要求：

```text
年龄
学历
收入
身高
地区
职业
婚姻状态
住房
```

这首先告诉我们：

> 平台认为这些字段值得被结构化、筛选或展示。

它不自动证明：

- 所有用户同样重视这些条件；
- 用户填写值真实；
- 没有字段的特征不重要；
- 某字段导致关系成功/失败。

因此旧网考古最好区分：

```yaml
field_exists_in_schema: true
user_value_observed: true/false
value_verified: true/false/unknown
field_used_in_search: true/false/unknown
field_used_in_recommendation: unknown
field_caused_selection: unknown
```

必须坚持：

> **platform schema ≠ user preference distribution**

以及：

> **filterable field ≠ causal selection criterion**

---

# 9. 2011–2012：实名认证出现后，必须拆成 verification ladder

2012 年同期报道记录，百合网在 2011 年底开始推进后台实名认证，并设置过渡期；平台设计强调前台仍可使用昵称，而后台完成身份核验。

来源：

- 第一财经日报，2012-02-03，经搜狐保存：
  <https://business.sohu.com/20120203/n333580998.shtml>
- 中国妇女报，2012-01-18，经中新网保存：
  <https://www.chinanews.com.cn/sh/2012/01-18/3613977.shtml>

同年多篇调查又记录：行业对实名效果存在争论，仅姓名/身份证号匹配可能被冒用；平台之间对“实名”本身也互相质疑。

来源：

- 新闻晚报，2012-07-23，经新浪保存：
  <https://news.sina.com.cn/o/2012-07-23/125924827239.shtml>
- 中新社，2012-07-12：
  <https://www.chinanews.com.cn/cul/2012/07-12/4028373.shtml>
- 中国广播网，2012-08-13：
  <https://finance.cnr.cn/gundong/201208/t20120813_510575384.shtml>

### 新 evidence model

不要只写：

```yaml
real_name: true
```

改为：

```yaml
verification:
  phone_bound: unknown
  legal_name_submitted: true/false/unknown
  id_number_submitted: true/false/unknown
  id_name_match: true/false/unknown
  face_or_photo_match: true/false/unknown
  education_verified: true/false/unknown
  occupation_verified: true/false/unknown
  marital_status_verified: true/false/unknown
  income_verified: true/false/unknown
  verification_visible_to_others: true/false/unknown
```

核心规则：

> **identity verification ≠ attribute verification**

> **verified badge ≠ verified intention**

即使身份证真实，也不能由此证明：

- 职业收入真实；
- 婚姻状态真实；
- 照片是当前本人；
- 使用者没有欺诈意图；
- 线下见面安全。

---

# 10. “后台实名、前台昵称”是一种值得单独保存的身份架构

2012 年资料特别有意义的一点，是平台试图让：

```text
legal identity known to platform
≠
legal identity shown to every user
```

共存。

这不是简单的“实名 / 匿名”二选一。

建议以后给旧网身份增加：

```yaml
identity_layers:
  public_display_name:
  platform_known_legal_identity:
  counterparty_visible_identity:
  verification_badge:
  public_contact_details:
```

它能避免把“后台实名”错误描述成“网站上人人公开真名”。

---

# 11. 婚恋站最关键的历史动作往往会离开站点

2019 的下游同期材料虽然超出本文件主体时间范围，却能帮助验证一个 2000s 即已存在的结构问题：平台认识的人常常加微信后继续联系，真正见面的关系甚至可能主要来自别的渠道。

对于 2002–2012，我们应预期并主动验证类似 handoff：

```text
dating-site message
→ QQ / MSN
→ email / SMS / phone
→ offline meeting
```

但注意：`预期` 不等于 `已证实`。

只有找到同期页面/教程/用户材料时才能给具体平台升级证据等级。

此处只是规定考古模型。

### 新 gap：off-platform relationship execution gap

> 旧婚恋网站越成功地让两个人互换联系方式，它自己越可能失去后续关系的可见性。

因此 archive 即使完整保存网站，也可能看不见真正关系。

核心边界：

> **contact handoff ≠ relationship outcome**

> **platform disappearance from evidence ≠ relationship ended**

两个人从网站消失，可能是：

- 去 QQ 聊；
- 换电话；
- 见面；
- 开始恋爱；
- 同时注销账号；
- 也可能只是放弃平台。

没有后续证据时必须写“不知道”。

---

# 12. 双边系统比求职网站多一层“对方也在选择”

招聘网站的申请链通常是：

```text
candidate → employer
```

婚恋网站则是：

```text
A evaluates B
AND
B evaluates A
```

即使算法说 `match`，也只代表平台计算结果；双方仍然要分别决定。

建议使用：

```text
recommended
→ A interested
→ B noticed
→ B interested
→ reciprocal channel opened
```

而不是把平台用词“匹配成功”自动当作 relationship success。

因此：

> **algorithmic match ≠ reciprocal match**

> **reciprocal match ≠ durable relationship**

这是 dating artifact 与 job-board artifact 的关键差异。

---

# 13. 推荐系统会产生 impression history，但这种历史几乎不可公开保存

一个普通用户一天可能看到几十个 profile。

真实系统可能产生：

- impression；
- click；
- dwell time；
- ignore；
- interest；
- message；
- block；
- hide；
- shortlist。

这些行为对理解“一个人实际上看过多少条关系可能性”极其重要。

但它们通常位于：

- 登录后；
- 数据库；
- session；
- JS / AJAX；
- 私人日志；
- 推荐后台。

所以新增：

## impression-history gap：曝光历史缺口

> **a preserved profile tells us who could be viewed, not who was actually shown to whom.**

这意味着公开 archive 会系统性高估静态 profile 的重要性、低估 recommendation/query state 的重要性。

---

# 14. 被忽略、被拒绝和短暂聊天尤其容易消失

婚恋网站的负状态至少包括：

```text
no view
viewed, no interest
interest sent, no reply
chat started, stopped
contact exchanged, no meeting
meeting occurred, no second meeting
relationship formed, later ended
```

真正最容易留下公开记录的反而是：

- 平台首页；
- “成功牵手”案例；
- 婚礼故事；
- 媒体宣传；
- 重大诈骗新闻。

因此出现：

## relationship-outcome survival bias：关系结果存续偏差

以及：

## success-story curation bias：成功故事精选偏差

平台公开展示的成功案例证明：

> 某些成功关系被平台挑选出来讲述。

它不能证明：

- 成功率；
- 典型使用路径；
- 平均聊天时长；
- 多数人的结果。

尤其不能用几十篇成功故事除以注册用户数计算成功率，因为分子与分母完全不对应。

---

# 15. 当前 live profile / current platform page 不是 2000s artifact

婚恋平台如果今天仍在线，会形成很强的 `live legacy page` 诱惑。

必须分开：

```yaml
historical_claim_date:
current_page_access_date:
current_template_date:
archive_capture_datetime:
original_resource_date:
```

一个今天仍写着“创办于 2003”的页面，可以支持机构沿革 claim，却不能告诉我们：

- 2003 首页长什么样；
- 2003 是否已有这个字段；
- 当年 profile URL pattern；
- 当年编码；
- 当年搜索接口；
- 当年会员看到的 UI。

因此：

> **current corporate history ≠ historical capture**

与本仓其它 legacy platform 的规则一致。

---

# 16. profile URL 可能稳定，profile meaning 却不稳定

即使同一个用户 ID URL 存活多年，也需要确认：

- 是否仍是同一账户；
- 页面是否已注销；
- 是否被平台复用；
- 是否改成登录页；
- 是否只剩模板；
- 是否由 archive rewrite 造成伪稳定；
- profile 内容属于哪个时间点。

所以：

> **stable URL ≠ stable identity state**

尤其婚恋账号很可能在进入关系后停用、隐藏或删除。

账号消失本身不能被自动解释为“找到对象”。

> **profile removed ≠ relationship formed**

---

# 17. 动态推荐和搜索页应优先记录请求方法、cookie 与登录依赖

若未来找到原始 capture，应至少测：

```yaml
request:
  method: GET/POST/unknown
  query_parameters:
  cookie_required:
  authenticated_session_required:
  referer_dependency:
  javascript_required:
  frame_dependency:
  charset:
  pagination_pattern:
  result_count_visible:
```

对于 2000s 中文婚恋站尤其要检查：

- GB2312 / GBK / UTF-8；
- IE-only JS；
- table layout；
- iframe / frameset；
- 图片服务器是否独立域名；
- 登录 cookie；
- 验证码；
- profile photo 是否 robots/权限阻断；
- 站内信是否完全不可 archive。

没有 capture 时这些全部是待验证项，不能从同年代其它网站类推。

---

# 18. 隐私规则：不要因为旧 profile 公开过，就把普通人的亲密资料重新做成 searchable corpus

婚恋 profile 经常包含：

- 真实或半真实姓名；
- 年龄 / 出生年月；
- 地区；
- 工作；
- 收入；
- 婚史；
- 身高体重；
- 照片；
- 联系方式；
- 对伴侣的私人要求；
- 对性格、家庭和感情经历的自述。

即使 archive 今天技术上仍能访问，仓库也应实行**研究必要最小化**。

默认做法：

- 不批量重新发布普通用户旧 profile；
- 不建立“历史征婚用户姓名数据库”；
- 不复制联系方式；
- 不为了证明字段存在而暴露普通人完整资料；
- 优先保存字段 schema、URL pattern、页面结构、匿名化摘要和 evidence metadata；
- 个案只保留支撑 claim 的最少信息。

这比普通论坛昵称更敏感。

---

# 19. 一个 dating-profile evidence contract

以后若发现历史 profile，可按下面模板记录：

```yaml
artifact_type: dating_profile
platform:
original_url:
capture_url:
capture_datetime:
page_internal_datetime:
accessed_at:
source_grade: A/B/C/D

account:
  public_name_type: nickname/realname/unknown
  account_status: active/dormant/removed/unknown

profile:
  version_time: unknown
  fields_visible:
    - age
    - location
    - education
  narrative_bio_present: true/false/unknown
  partner_requirements_present: true/false/unknown
  photo_present: true/false/unknown

verification:
  public_badge: none/phone/id/other/unknown
  backend_identity_known: true/false/unknown
  attributes_verified: []

interaction:
  searchability: true/false/unknown
  message_action_visible: true/false/unknown
  off_platform_contact_visible: true/false/unknown

outcome:
  reciprocal_contact: unknown
  meeting: unknown
  relationship: unknown
  marriage: unknown

privacy:
  ordinary_person: true
  reproduce_contact_info: false
  reproduce_full_profile: false

missing:
  - private_messages
  - search_impressions
  - backend_verification
  - off_platform_chat
  - relationship_outcome
```

---

# 20. “已证实 / 高概率 / 不知道”示例

假设某 2008 capture 里有一个 profile，页面上有“已认证”图标与“发信”按钮。

## 已证实

- capture 时该页面呈现这些字段；
- 页面显示“已认证”标记；
- 页面模板提供发信入口。

## 高概率但仍需证据

- 账号当时属于可参与站内匹配的用户；
- 认证标记对应平台某个后台认证流程。

## 不知道

- 用户本人当日是否仍在使用；
- 认证核验了哪些属性；
- 是否有人发过信；
- 是否回复；
- 是否转到 QQ / 电话；
- 是否见面；
- 是否恋爱或结婚。

这正是本专题最需要防止的“从 profile 跳到 biography”。

---

# 21. 与生活史仓的交叉结论

旧网资料最容易让研究者产生错觉：

> 有多少 profile，就有多少可恢复的关系史。

实际上 profile 只恢复了“候选人变得可寻址”的一层。

普通人的真实关系路径更像：

```text
profile / post
→ discoverability
→ bilateral attention
→ communication
→ handoff
→ meeting
→ repeated embodied interaction
→ relationship negotiation
→ possible household / marriage
```

旧网通常越往后越看不见。

因此应将：

## relationship-outcome gap

正式加入中文旧网 archive-gap 体系。

它与 job-board 的 application-event gap、roommate listing 的 household-outcome gap 同构，但婚恋关系有更强的：

- 双边同意；
- 私密性；
- 跨平台迁移；
- 删除动机；
- 身份敏感性。

---

# 22. 本轮 source register

| source | date | grade | support | limitation |
|---|---:|---|---|---|
| RFA《征婚广告里的中国人（一）》 | 2002-08-30 | B | 网站/纸媒征婚同时存在；篇幅/格式观察 | 只有作者小样本，不是原站 capture |
| 中国青年报百合网报道 | 2006-01-24 | B | 心理测评/智能匹配作为 product claim | 算法、UI、效果未恢复 |
| 中国青年报 2008 用户搜索稿转载 | 2008-03-03 | B | 字段搜索、结果返回、用户使用动机 | 无具体 query log/capture |
| 2008 网民婚恋调查 | 2008 | B | 网络婚恋形成大规模服务/调查 | 强自选择，不代表人口总体 |
| 第一财经/妇女报实名制报道 | 2012 | B | 后台实名、过渡期、身份层设计 | 平台 claim 与真实执行需区分 |
| 新闻晚报/中新社实名争议 | 2012 | B | 认证漏洞、欺诈、行业争论 | 个案不能估计总体欺诈率 |

访问日期：2026-09-03。

---

# 23. 反例与后见之明风险

## 反例 A：Web 并不一定让自我介绍更短、更数据化

2002 同期样本恰恰观察到网站自述比报纸长。

因此不能写线性故事：

```text
paper = narrative
web = fields
```

真正变化取决于平台形态。

## 反例 B：实名不等于透明

后台可以知道真实身份，前台仍显示昵称。

因此匿名/实名不是二值变量。

## 反例 C：平台消失不等于关系失败

成功 handoff 到站外以后，平台恰恰可能再也看不到两个人。

## 风险 A：用今天平台 UI 复原 2008

禁止。

## 风险 B：把行业宣传中的“成功匹配”当真实关系结果

禁止。

## 风险 C：把一个 verified badge 解释为全部字段经过验证

禁止。

## 风险 D：为了研究旧网重新公开普通人的婚恋隐私

禁止。

---

# 24. 下一步最有价值的证据

优先级最高的不是再搜一百篇“婚恋网站市场规模”报道，而是：

### A. 找真正的 2002–2008 profile/search capture

候选对象：

- 交友驿站；
- 世纪佳缘早期页面；
- 百合网 2005–2008；
- 新浪/搜狐/网易等门户交友栏目；
- 高校 BBS 鹊桥/征友版。

需要同时验证：

- original URL；
- capture datetime；
- charset；
- profile schema；
- search parameters；
- login requirement；
- photos/subresources；
- browser assumptions。

### B. 找同一账号的多时点 profile

例如：

```text
2006 profile A
→ 2007 修改城市/工作/要求
→ 2008 隐藏/注销
```

这样可以第一次研究 profile revision，而不是把一个页面当永恒身份。

### C. 找公开、非敏感的 relationship revision chain

最好是普通用户自己公开记录：

```text
发征友帖
→ 更新“收到很多信”
→ 更新“已经见面”
→ 更新“暂停征友”
```

但只在隐私风险可控、资料本来就面向公开研究且无需重新曝光敏感身份时使用。

---

# 25. 本轮结论

这一轮没有把旧网婚恋写成“互联网改变爱情”。

得到的是一个更窄、但可以长期复用的考古结论：

> **中文旧网把一部分潜在伴侣从熟人关系中的“某个人”，变成了数据库里可被搜索、过滤和联系的 profile；但公开 Web 最容易保存的恰恰只是这条关系链的前半段。**

越往真实关系推进：

```text
站内私信
→ QQ / MSN / 电话
→ 线下见面
→ 恋爱
→ 共同生活
```

越容易离开 archive。

所以以后所有婚恋类旧网研究都应坚持：

> **searchable profile ≠ searchable biography**

以及：

> **historical partner visibility ≠ historical relationship outcome**

这正是平台化以后普通人生“看起来数据更多、实际生命历程却仍大量不可见”的一个典型案例。