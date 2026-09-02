# LOCATION_COPRESENCE_AND_DISTRIBUTED_HOUSEHOLD_INFERENCE_1999_2015.md

> 适用范围：约 1999–2015 年中文旧网中的婚姻/家庭资料页、博客、论坛、新闻转载与“双城 / 异地 / 周末夫妻”等生活叙事。
>
> 目标：避免从一个旧网页里的“所在地、婚姻状态、夫妻、周末、电话、回家”等字段或词语，直接推断一个家庭真实住在哪里、多久见一次、为什么分开。

跨仓生活史主文档：
<https://github.com/tmzncty/how-people-lived/blob/main/topics/reunion-latency-co-presence-stack-and-coordination-by-separation-china-1980-2019.zh-CN.md>

本文件承接：

- `CONTACT_STACK_AND_CHANNEL_HANDOFF_1998_2002.md`：网页只是通信链的一跳；
- `RELATIONSHIP_PIPELINE_AND_MATCHMAKING_ARTIFACTS_1998_2005.md`：关系资料页不等于关系真实生命周期；
- `QUOTATION_SURVIVAL_AND_MEDIA_RECONTEXTUALIZATION_2009_2010.md`：媒体转载不等于原始平台帖子。

本篇新增的研究单位是：**location / residence / co-presence / household topology**。

---

## 1. 核心问题：一个“地点”字段到底表示什么？

旧网里常见：

```text
所在地：北京
籍贯：天津
单位：上海某公司
婚姻状况：已婚
```

这些字段非常诱人，但它们不能自动拼成一个现实家庭。

至少要区分：

- `registered_location`：户籍/登记地；
- `self_reported_location`：账号资料里的自报所在地；
- `work_location`：实际工作地点；
- `sleep_location`：通常过夜地点；
- `partner_location`：伴侣所在地；
- `child_location`：孩子所在地；
- `care_location`：主要育儿/养老劳动发生地点；
- `reunion_location`：家庭周期性团聚地点；
- `hometown`：故乡/籍贯；
- `platform_location_field`：平台字段当前显示的值。

因此：

> **location field ≠ residence**

以及：

> **married status ≠ co-residence**

---

## 2. 1999 年“周末夫妻”：同一个标签已经包含不同空间机制

1999 年 12 月 4 日，新浪转载《扬子晚报》的《都市“周末夫妻”--浪漫还是苦涩》：

<https://news.sina.com.cn/society/1999-12-4/38066.html>

这篇同期媒体材料至少同时描述：

- 一名女性与丈夫**同在一市**，却主动分开居住、按固定频率见面；
- 另一对夫妻因为单位相距较远、日常往返困难而分住，周末团聚。

这已经足以建立一个旧网考古硬规则：

> **term label ≠ verified household geography**

看到：

```text
周末夫妻
异地婚姻
两地分居
双城族
候鸟家庭
```

都不能只靠词语本身编码：

```yaml
cross_city: true
work_caused: true
```

至少要另找：

- 地名；
- 工作地点；
- 通勤/车次；
- 过夜地点；
- 分开原因；
- 团聚频率。

### 证据等级

**B：同期媒体页面。**

它能证明 1999 年公共叙述里这个标签已经存在，并且语义并不单一；不能证明所有被称作“周末夫妻”的人口结构。

---

## 3. same city ≠ daily co-presence

旧网页经常把“异地”理解成不同城市，把“同城”理解成生活在一起。

两者都过度简化。

即使夫妻：

- 同城；
- 同户籍；
- 甚至同一单位；

仍可能因为：

- 夜班 / 对班；
- 超长通勤；
- 驻场；
- 值班；
- 照护老人或孩子；
- 一方长期住单位宿舍；

而几乎没有共同清醒时间。

因此：

> **co-location ≠ co-presence**

旧网研究如果要讨论“家庭是否在一起”，比 `city` 更有用的字段是：

```yaml
sleep_location_overlap: unknown|daily|partial|none
awake_time_overlap: unknown
routine_reunion_frequency: daily|weekly|biweekly|irregular|unknown
```

如果网页没有这些信息，就写 `unknown`。

---

## 4. 2013 新浪博客案例：blog URL ≠ personal diary

新浪博客页面《为了梦想选择双城生活》当前仍可访问：

<https://blog.sina.com.cn/s/blog_49992d2e01018m1c.html>

页面自身显示：

- 博文时间：2013-04-22 19:24:46；
- 正文明确注明：“本文已发表2013年4月21日《今晚报》”；
- 文末再次注明为《今晚报·8090后版》文章。

因此这个 artifact 最适合说明：

> **container platform ≠ content origin**

虽然 URL 在 `blog.sina.com.cn`，内容 provenance 不是普通用户“2013 年 4 月 22 日写了一篇生活日记”，而是**报刊内容进入博客容器后的再发布**。

建议记录：

```yaml
container_platform: Sina Blog
container_page_timestamp: 2013-04-22T19:24:46+08:00
content_origin_claimed: 今晚报·8090后版
content_origin_date_claimed: 2013-04-21
speaker_type: journalist-mediated_interview
personal_diary: false
```

### 为什么这很重要

如果以后批量搜索“新浪博客 + 双城生活 + 第一人称”，很容易把报道中的受访者引语误收为“博客作者本人第一人称”。

于是：

> **first-person quotation on a blog page ≠ blogger first-person testimony**

需要继续追 `source_speaker` 和 `content_origin`。

---

## 5. 2013 案例还说明：train-time field ≠ household distance

同一篇文章记录一对京津夫妻：列车运行约半小时，但受访丈夫表示地铁、进站检票和加班使每日返家不可行，实际通常每周团聚一次。

旧网文章里经常会出现：

```text
北京到天津只需 30 分钟
上海到无锡 42 分钟
```

若研究对象是家庭生活，不能直接编码为：

```yaml
reunion_latency_minutes: 30
```

应拆成：

```yaml
scheduled_vehicle_time:
first_mile_time:
station_process_time:
waiting_time:
last_mile_time:
work_schedule_constraint:
actual_reunion_cadence:
```

核心规则：

> **published travel time ≠ door-to-door reunion latency**

网页能证明时刻表或报道里的列车时间，不自动证明当事人“离家只有半小时”。

---

## 6. 网页保存了“每天通电话”，也不能升级成 physical togetherness

本仓已有 `CONTACT_STACK_AND_CHANNEL_HANDOFF_1998_2002.md` 指出：Web archive 经常只保存通信链的一跳。

在多地家庭里还要再加一条：

> **communication presence ≠ physical presence**

一个页面说夫妻：

- 每天电话；
- 每晚 QQ；
- 一直短信；
- 开着视频吃饭；

可以支持 `communication_frequency` 或 `remote_co-presence_claim`，但不能支持：

```yaml
cohabiting: true
care_work_shared_physically: true
```

反过来，页面没有提到配偶也不能推出：

```yaml
single: true
separated: true
relationship_absent: true
```

这类负推断在个人博客尤其危险，因为“今天没写家人”只是内容选择。

---

## 7. 2018–2019 媒体页说明家庭拓扑可能包含三代人和多个城市

虽然 `old-web-archaeology` 的主 scope 到约 2015，后续材料可以作为**边界验证**，用于说明为什么 1995–2015 的旧网页不能简单按“账号所在地”重建家庭。

2018 年《中国青年报》记录一名退休老人离开青岛丈夫，去北京燕郊为儿子一家照顾孙辈；她一天的大量时间用于买菜、做饭、清洁、接孩子，到深夜才给丈夫打电话：

<https://zqb.cyol.com/html/2018-02/09/nw.D110000zgqnb_20180209_2-06.htm>

2019 年《都市快报》杭州东站采访又记录一户京杭家庭：妻子从北京到杭州工作，两个孩子随她迁移，外祖母也从北京到杭州帮忙照护，丈夫继续在北京工作并约每两周来杭州团聚：

<https://hznews.hangzhou.com.cn/shehui/content/2019-04/08/content_7173338.htm>

这些后界材料不写成本仓的主研究对象，而是验证一个推理边界：

> **one account / one location field cannot encode a household topology.**

一个家庭同时可能拥有：

```text
partner A work/sleep city
partner B work/sleep city
children city
grandparent care city
hometown
registered household location
reunion route
```

如果旧平台只给一个“所在地”下拉框，它本身就会把现实生活压扁。

---

## 8. 新研究单位：household topology

如果一个旧页确实提供足够证据，建议把家庭空间结构单独建模，而不是把地点塞进 account metadata。

```yaml
household_topology:
  evidence_scope: article|blog|forum-post|profile
  legal_relationship_claim: married
  member_nodes:
    - role: spouse_a
      work_location: Beijing
      sleep_location: Beijing
    - role: spouse_b
      work_location: Tianjin
      sleep_location: Tianjin
  reunion:
    cadence: weekly
    usual_location: Tianjin
    transport: intercity_rail
  remote_contact:
    channels:
      - phone
    frequency_claim: daily
  care_distribution:
    child_location: Tianjin
    primary_caregiver: unknown
  confidence: medium
```

只填 evidence 明确支持的字段。

不要为了让图“完整”而推断未出现的家庭成员、地址或真实姓名。

---

## 9. 再加一个研究单位：co-presence stack

对关系/家庭 artifact，可以把“在一起”拆成层级：

```yaml
co_presence_stack:
  legal_relationship: observed|claimed|unknown
  registered_same_place: yes|no|unknown
  shared_budget: yes|no|unknown
  digitally_reachable: yes|no|unknown
  routine_remote_contact: yes|no|unknown
  recurring_physical_reunion: yes|no|unknown
  daily_co_residence: yes|no|unknown
  embodied_care_shared: yes|no|unknown
```

它防止出现两种相反误判：

1. `每天 QQ / 电话 → 实际生活在一起`；
2. `分处两城 → 已经不是一个家庭经济/照护单位`。

---

## 10. 资料页地点字段至少有六种 dating 风险

旧平台 profile 常出现：

```text
所在地
故乡
单位
婚姻状态
最后登录
注册时间
```

研究时必须防止：

1. **account date ≠ field value date**：2003 注册，2008 修改所在地；
2. **capture date ≠ move date**：2008 capture 只能给变化设上/下界；
3. **schema date ≠ account date**：今天幸存模板的“所在地”字段不证明 2003 年已有；
4. **hometown ≠ residence**；
5. **workplace city ≠ sleep city**；
6. **stale profile ≠ current location**：用户迁移后可能从不更新。

因此建议：

```yaml
location_claim:
  value_republished: false
  field_label: 所在地
  observed_on_capture: true
  capture_datetime:
  claimed_effective_date: unknown
  semantic_role: unknown
  corroborated_by_body_text: false
```

普通个人的精确旧地址默认不重新公开。

---

## 11. Archive asymmetry：家庭“接口”比家庭“拓扑”更容易存活

Web archive 较容易保存：

- “我在北京”；
- “老公周末回来”；
- “每天电话”；
- “孩子跟我住”；
- 一个城市字段；
- 一篇“异地夫妻”咨询帖。

却经常保存不了：

- 对方真实居住页；
- 私聊；
- 电话内容；
- 谁每天做饭/接孩子；
- 一趟未被写进博客的普通返家；
- 后来什么时候真正合居；
- 一次地点更新是否只是资料维护。

所以：

> **archived household interface ≠ complete household topology**

与本仓已有的 `surviving quotation ≠ surviving original post` 类似，家庭史还会遭遇另一种缺失：**关系链的节点分散在不同媒介和不同人的生活里，而 archive 往往只抓到其中一个人的公开表面。**

---

## 12. 搜索可见性偏差：冲突型异地家庭更容易留下网页

“夫妻长期不见”“双城婚姻风险”“为了梦想两地跑”很适合成为：

- 报纸专题；
- 心理咨询；
- 情感博客；
- 门户转载；
- 论坛热帖。

反过来，一户家庭如果只是：

> 每周五坐车回家，周日回来，十年没发生戏剧性事件。

它可能完全没有公开网页。

因此：

> **search-visible distributed households ≠ representative distributed households**

本仓不应从“搜索结果里异地婚姻多为冲突故事”推出“异地婚姻历史上主要以冲突形式存在”。

这与 `QUOTATION_SURVIVAL_AND_MEDIA_RECONTEXTUALIZATION_2009_2010.md` 的 preservation filter 相连：媒体选择本身就是历史可见性过滤器。

---

## 13. 2013 新浪博客案例的 provenance 模板

建议按以下方式编目，而不是写“2013 新浪博主分享双城夫妻生活”：

```yaml
artifact:
  platform: Sina Blog
  url: https://blog.sina.com.cn/s/blog_49992d2e01018m1c.html
  observed_page_title: 为了梦想选择双城生活
  internal_page_timestamp: 2013-04-22T19:24:46+08:00

provenance:
  content_origin_claimed: 今晚报·8090后版
  origin_publication_date_claimed: 2013-04-21
  original_newspaper_page_verified_in_this_pass: false
  container_copy_verified: true

content_type:
  journalist_report: true
  blogger_personal_diary: false
  interview_quotes_present: true

claims:
  - claim: one described couple used weekly Beijing-Tianjin reunion despite short scheduled rail time
    grade: B
    confidence: medium-high
  - claim: daily phone contact existed for that described couple
    grade: B
    confidence: medium-high
  - claim: this pattern was representative of all 80/90s couples
    grade: unsupported
```

这里最重要的是：**把 artifact provenance 和生活史 claim 分开。**

---

## 14. 证据等级建议

### B — 1999 新浪 / 扬子晚报“周末夫妻”

可用于：

- 证明标签在同期存在；
- 证明标签当时已包含同城主动分居和工作距离分居等不同机制。

不可用于：

- 总体比例；
- 把所有“周末夫妻”定义成跨城双职工。

### B — 2013 新浪博客中的《今晚报》再发布

可用于：

- 同期媒体呈现的京津双城夫妻与通勤路径；
- 证明博客容器可能托管报刊内容；
- 证明报道中的“列车 30 分钟”与实际每周团聚可以同时成立。

不可用于：

- 把页面当普通博客作者原生日记；
- 把所有“双城族”写成高铁造成；
- 从新闻人物推总体频率。

### B — 2018/2019 后界比较

只用于验证 household topology 推理模型，不扩张本仓主 scope。

---

## 15. 建议新增字段

```yaml
relationship_location_evidence:
  page_type: profile|blog|forum|news-copy|help-page
  container_platform:
  content_origin:
  content_origin_verified: false

  relationship_status_claim:
  registered_location_claim:
  self_reported_location_claim:
  work_location_claim:
  sleep_location_claim:
  partner_location_claim:
  child_location_claim:
  care_location_claim:

  reunion:
    cadence_claim:
    route_claim:
    scheduled_vehicle_time:
    door_to_door_time:

  remote_contact:
    channels: []
    frequency_claim:

  inference_limits:
    cohabitation_verified: false
    migration_date_verified: false
    cause_of_separation_verified: false
    household_topology_complete: false

  privacy:
    exact_address_republished: false
    personal_endpoints_republished: false
```

---

## 16. 与 old-web scope 的边界

本文件不把 `old-web-archaeology` 改造成婚姻社会学或全球家庭史仓库。

在本仓中，只研究：

- 中文 Web 如何编码“所在地 / 婚姻 / 家庭”；
- 博客 / 论坛 / 门户转载如何保存两地生活叙事；
- 这些页面怎样制造 location inference 风险；
- 页面 provenance 与真实生活 topology 为什么不能混为一谈。

1980 年代的夫妻分居制度史、2018–2019 的家庭空间重组和海外 commuter marriage 比较，放在 `how-people-lived`。

跨仓主文档：
<https://github.com/tmzncty/how-people-lived/blob/main/topics/reunion-latency-co-presence-stack-and-coordination-by-separation-china-1980-2019.zh-CN.md>

---

## 17. 已证实 / 高概率 / 不知道

### 已证实

- 1999 新浪同期转载页面中，“周末夫妻”至少同时指向不同的空间/婚姻机制；
- 2013 新浪博客幸存页面明确自述内容原发表于前一日《今晚报》，所以博客 URL 不能被当成原生个人日记 provenance；
- 该 2013 页面中的受访夫妻确实被报道为“短列车运行时间 + 实际每周团聚 + 每日电话”的组合；
- 中文 Web artifact 可以保存关系的一个 location/contact 表面，而非完整家庭空间结构。

### 高概率但仍需更多证据

- 1995–2015 许多平台的单一“所在地”字段系统性压缩了多地点生活；
- 情感咨询、门户和新闻转载比普通低冲突家庭日志更容易长期存活并进入今天的搜索结果。

### 不知道

- 1999–2015 各主要中文平台在具体版本里怎样定义“所在地 / 家乡 / 居住地”；
- 多少用户会及时更新地点字段；
- 一个 profile 地址变化与真实迁移之间的平均滞后；
- 原生 BBS/博客里低冲突、长期双城家庭的留存比例；
- 是否能找到同一普通用户跨多年地点字段变化、同时又不触及隐私边界的可公开案例。

---

## 18. 下一步

最值得继续做的不是再搜“异地婚姻故事”，而是选择一个具体中文平台版本，做**location-field archaeology**：

1. 找同期注册/个人资料帮助页；
2. 确定“所在地 / 家乡 / 单位”等字段在什么版本存在；
3. 检查字段是自由文本还是行政区下拉；
4. 检查是否允许多个地点；
5. 比较个人主页 → 博客 → SNS 后，平台是否越来越强制把一个人压缩成单一 location；
6. 只研究 schema 和匿名化样本，不重新公开普通人的旧地址。

如果这一层能做出来，就可以把“家庭实际有多个地点”与“平台只能显示一个地点”之间的差距，变成可复核的旧网结构史，而不是只停留在概念提醒。