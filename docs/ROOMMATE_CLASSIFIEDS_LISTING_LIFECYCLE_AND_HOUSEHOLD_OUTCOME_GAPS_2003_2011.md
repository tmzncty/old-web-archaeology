# ROOMMATE_CLASSIFIEDS_LISTING_LIFECYCLE_AND_HOUSEHOLD_OUTCOME_GAPS_2003_2011.md

> 适用范围：约 2003–2011 年中文网站、BBS、论坛、分类信息与媒体记录中的“求租 / 合租 / 找室友 / 转租”等住房匹配 artifact。
>
> 目标：防止把一条幸存的室友广告、求租帖或论坛合集，直接解释成一个真实且持续存在的共同居住家庭。

跨仓生活史主文档：
<https://github.com/tmzncty/how-people-lived/blob/main/topics/residential-seriality-nonkin-households-and-roommate-matching-china-1984-2025.zh-CN.md>

本文件与以下文档互补：

- `RELATIONSHIP_PIPELINE_AND_MATCHMAKING_ARTIFACTS_1998_2005.md`：处理交友 / 婚恋 artifact 与真实关系结果的断裂；本篇处理住房匹配与真实共同居住结果的断裂；
- `LOCATION_COPRESENCE_AND_DISTRIBUTED_HOUSEHOLD_INFERENCE_1999_2015.md`：处理“地点字段 / 婚姻状态”不能推出真实共同居住；本篇处理“合租广告 / 室友帖”不能推出真实 household；
- `CONTACT_STACK_AND_CHANNEL_HANDOFF_1998_2002.md`：解释 Web 如何把后续联系交给电话、Email、QQ 等不可归档渠道；
- `QUOTATION_SURVIVAL_AND_MEDIA_RECONTEXTUALIZATION_2009_2010.md`：处理原帖消失而媒体摘引幸存；本篇进一步增加 listing lifecycle 与 household outcome gap。

本篇新增的研究单位不是“住房”本身，而是：

> **listing artifact → contact / viewing → agreement → move-in → co-residence → exit**

这些阶段不能由一个 URL 自动串起来。

---

## 1. 研究单位：不要把“房源、帖子、室友、家庭”混成一个对象

中文旧网里的住房匹配至少包含以下层级：

- **platform / site**：某门户、地方站、BBS、分类信息平台；
- **board / category**：租房版、房屋信息、合租区、校园 BBS 房屋版；
- **listing page / post**：一条具体“求租 / 出租 / 找室友 / 转租”信息；
- **listing author / account**：发帖账号或匿名联系方式；
- **contact endpoint**：电话、Email、QQ、站内信；
- **reply / public interaction**：可见回帖、追问、补充；
- **private interaction**：电话、私信、Email、QQ 等通常不进入 Web archive；
- **viewing**：实际看房；
- **agreement**：口头约定、租赁合同、分租协议；
- **move-in**：实际入住；
- **co-resident household**：一段真实共同居住关系；
- **exit / replacement**：搬离、换室友、转租、终止；
- **archive capture**：档案服务保存的某个时点呈现。

所以第一条硬规则是：

> **roommate listing ≠ household**

一条帖子最多直接证明：某个账号 / 页面在某个时点表达“有房间可供合租”或“正在寻找室友”。

它不能自动证明：

- 有人真的回复；
- 回复者符合条件；
- 双方见面；
- 看过房；
- 谈妥租金；
- 签过合同；
- 真正搬入；
- 同住了多久；
- 页面里的身份、职业、年龄、性别陈述都真实；
- 最终室友具备广告中偏好的特征。

---

## 2. listing lifecycle：住房广告本身也有生命周期

建议把一条 room / roommate listing 至少拆成：

```text
draft
→ published
→ indexed / visible
→ contacts received
→ candidate screening
→ offline viewing
→ candidate selected
→ agreement
→ filled / move-in
→ occupied
→ exit / replacement
→ expired / withdrawn / deleted / stale / reposted
```

网页 archive 最容易保存的是 `published / visible`。

最重要的后半段：

```text
contact
viewing
selection
agreement
move-in
actual duration
exit
```

通常最难保存。

因此：

> **listing visibility ≠ vacancy persistence**

页面今天还能访问，并不说明该房间今天仍空；历史 capture 里帖子仍存在，也不说明 capture 当日它仍有效。

同样：

> **post timestamp ≠ availability interval**

一条 3 月 1 日发布的信息可能 3 月 2 日已找到室友，却几年后仍可被搜索引擎发现。

---

## 3. household outcome gap：广告最容易活，家庭结果最容易消失

这类 artifact 有一个非常强的历史保存不对称：

```text
公开发布“我要找室友”
        ↓  可被搜索 / 抓取
私下电话 / QQ / Email
        ↓  通常不可见
线下看房
        ↓  无 URL
共同入住
        ↓  不一定发帖
几个月后搬走
        ↓  不一定发帖
```

可称为：

> **household outcome gap（共同居住结果缺口）**

因此，一座旧 BBS 保存了 1000 条合租帖，并不等于我们拥有 1000 段合租生活史。

档案更接近记录：

> **attempted household assembly（尝试组装共同居住单元）**

而不是实际 household count。

### 3.1 没有“已租出”标记不能当失败

很多旧帖并没有状态字段；找到室友后，发帖者可能只是停止关注帖子。

所以：

> **no explicit filled marker ≠ not filled**

### 3.2 有回复也不能当成功

公开回帖可能只是：

- 问地址；
- 问价格；
- 顶帖；
- 质疑信息；
- 广告；
- 已过期后的讨论。

所以：

> **reply count ≠ viable candidates ≠ move-ins**

### 3.3 “已找到室友”仍不是完整共同生活史

即便帖子后来明确说“已租出 / 找到人”，也只能证明匹配发生到某一步。

还不知道：

- 对方是否最终搬入；
- 住多久；
- 是否中途退出；
- 是否再次换室友；
- 房租与规则是否按原约定执行。

---

## 4. 2003：先把 Web 放回当时的混合信息环境

2003 年 8 月，《三湘都市报》记录长沙高校宣传栏上的一张合租告示：一名学生已经租下两室一厅，因为经济和安全等考虑希望找人分担另一间卧室；记者观察时，联系电话已经被撕走。

当前存续媒体页：
<https://edu.sina.cn/sa/2003-08-27/detail-ikftpnny8656806.d.html>

证据等级：**B：同期媒体现场观察。**

它不属于本仓 Web artifact 主对象，但非常适合作为边界：

> **Web listing was one channel among noticeboards, newspapers, brokers, acquaintances and campus networks.**

旧网考古若只看幸存网页，会天然看不见同一时期大量发生在纸质公告栏上的匹配。

同年 9 月，中国新闻网 / 搜狐报道海口一些年轻人开始通过当地网站“租屋信息”栏目公开寻找陌生合租者，并把这种方式与过去通过熟人、同学、同事找合租对象作比较。

当前存续媒体页：
<https://news.sohu.com/67/21/news212912167.shtml>

证据等级：**B：同期媒体对网站栏目与帖子内容的观察。**

本轮没有取得该地方网站 2003 年可独立复核的原始 listing capture，因此正确写法是：

```yaml
platform_use_reported_by_contemporary_media: yes
original_listing_capture_verified: no
original_page_structure: unknown
listing_count_method: media_reported
```

不能把媒体摘录反向升级成原始帖子。

---

## 5. 2003—2005：媒体特别爱保存“异性合租”，造成 selection inversion

2003—2005 年的新闻搜索结果中，“异性合租”“孤男寡女”“新同居时代”等标题异常突出。

例如：

- 2003-03-21，中国新闻网，《孤男寡女同居一室不谈爱情 都市流行异性合租》：
  <https://www.chinanews.com.cn/n/2003-03-21/26/285518.html>
- 2005-08-30，羊城晚报 / 新浪，《广州出现新同居时代 男女合租者讲述情感故事》：
  <https://news.sina.cn/sa/2005-08-30/detail-ikkntiam4455671.d.html>

这些材料对“当时有人如何解释自己的合租关系”很有价值，但存在明显的媒体选样机制。

更普通的：

- 两名男同学合租；
- 两名女同事合租；
- 原室友辞职后再找一个同性室友；
- 实习生一起住两个月；

更不具有新闻性，反而可能只留下短命的分类信息帖，甚至完全没有被搜索引擎保存。

因此形成一个重要偏差：

> **media visibility of mixed-gender sharing ≠ prevalence of mixed-gender sharing**

还可以进一步称为：

> **selection inversion（选择反转）**：越“不寻常、可标题化”的共同居住越容易被媒体长期保存，越普通的室友生活越可能只在短期信息流中消失。

这和 `QUOTATION_SURVIVAL_AND_MEDIA_RECONTEXTUALIZATION_2009_2010.md` 的区别是：那篇研究媒体如何让一段论坛引语存活；本篇强调媒体保存机制还会**改变今天可观察的 household type 分布**。

---

## 6. 2005 广州案例：少见的 listing → household outcome 链，但仍是媒体重构

2005 年 8 月的羊城晚报 / 新浪报道保存了一个很完整的个案链条：

```text
一名刚毕业、已在广州工作的年轻人先租到两室一厅
→ 在线发布合租信息
→ 收到多条回复
→ 筛选一个候选室友
→ 双方见面并看房
→ 说明房租、水电及 AA 规则
→ 对方接受
→ 实际共同居住
```

来源：
<https://news.sina.cn/sa/2005-08-30/detail-ikkntiam4455671.d.html>

这条材料很重要，因为它让我们第一次能把：

> **discovery artifact**

和：

> **co-residence outcome**

在同一个同期 evidence family 中接起来。

但它仍然是：

> **journalist-mediated interview**

而不是已经取得：

- 原 listing URL；
- 原回复列表；
- 私信 / 电话；
- 租赁合同；
- move-in record。

因此证据等级仍应写 **B**，不能因为叙事完整就误标为 archive-level A。

同时必须坚持：

> **co-residence ≠ romance ≠ marriage**

同住本身不能恢复出恋爱关系。

这一点与 `RELATIONSHIP_PIPELINE_AND_MATCHMAKING_ARTIFACTS_1998_2005.md` 正好形成镜像：婚恋页面不自动证明共同居住；住房匹配页也不自动证明浪漫关系。

---

## 7. current listing page ≠ historical listing state

即使今天还能打开一条旧帖，也必须拆开多个时间：

```yaml
internal_post_datetime:
archive_capture_datetime:
current_survival_observed_at:
last_edit_datetime:
explicit_listing_status:
```

尤其不能混淆：

> **page visible now ≠ listing active then**

与：

> **page captured then ≠ vacancy still open then**

很多旧平台：

- 不自动删除过期帖；
- 删除后搜索缓存仍存在；
- 用新的模板重新渲染旧数据库内容；
- 合集页把旧帖子再次聚合；
- 移动版 / 当前版页面只保留正文与少量 metadata。

所以“现在还能访问”首先证明的是 **current survival**，不是 historical availability。

---

## 8. 2011 水木《合集》：一个 URL 里面可以有许多 provenance

水木社区当前仍可访问：

<https://m.newsmth.net/article/HouseRent/12633>

页面标题显示为：

> `[合集] 北京五年我的租房记录`

页面把 2011 年的主帖、多个回复、不同作者的租房回忆，以及部分转引材料聚合在一个当前可访问页面里。

它对生活史非常有价值：主帖作者回顾约 2006—2011 年间多次搬家、换室友、失业返乡、返京重新租房、伴侣工作 / 学校地点改变等过程；回复者还留下“已经买房却因为伴侣通勤继续在别处租房”等非标准住房状态。

但从旧网考古角度，它首先是一个非常危险的 artifact。

### 8.1 collection thread provenance collapse

可称为：

> **collection-thread provenance collapse（合集级 provenance 塌缩）**

当前 URL 不能被当成一个作者、一个时间点、一个原帖。

至少应逐 item 记录：

```yaml
collection_url:
item_sequence:
item_author_account:
item_internal_datetime:
item_board_marker:
item_type: original_post | reply | repost | media_quote | unknown
```

否则很容易把另一个网友的回复误写成主帖作者的人生经历。

### 8.2 collection timestamp ≠ component timestamp

合集生成时间、页面内部显示时间、每个帖子原始发表时间可能不同。

所以：

> **collection timestamp ≠ timestamp of every component**

### 8.3 current mobile rendering ≠ 2011 historical UI

`m.newsmth.net` 当前移动页面证明内容仍以某种方式存续，不证明 2011 年用户看到同一 DOM、CSS、字符编码或导航。

因此：

> **surviving current render ≠ verified historical HTML capture**

本轮没有以 Wayback/WARC 逐时点验证 2011 原始页面形态，所以视觉与交互层应写 `unknown`。

### 8.4 encoding corruption duplication risk

当前存续页面的部分历史文本可能出现编码异常、重复片段或合集整理痕迹。

如果未来做机器抽取，必须防止：

> **corrupted / repeated block ≠ independent evidence**

同一段被错误重复两次不能算两个用户、两个案例或两个 evidence family。

---

## 9. repost / mirror / syndication：多个 URL 不等于多套房源

分类信息非常容易被：

- 同一用户重复顶帖；
- 同一房源换标题重发；
- 中介复制到多个板块；
- 聚合站抓取；
- 门户 / 地方站转载；
- 论坛合集再次收录。

因此：

> **multiple listing URLs ≠ multiple vacancies**

也不能简单用页面数量估计租赁市场规模。

建议添加：

```yaml
repost_relation: original | same_author_repost | mirror | syndication | likely_duplicate | unknown
provenance_family:
canonical_listing_candidate:
```

判断 duplicate 时只能用可观察字段：

- 时间；
- 区域；
- 户型；
- 房租；
- 联系方式模式；
- 文字高度重合；

仍要允许 `unknown`，不能因为相似就强行合并不同普通人的住房信息。

---

## 10. listed rent ≠ paid rent；roommate preference ≠ actual roommate

旧帖常包含：

```text
800 元 / 月
押一付三
限女生
希望 IT 从业者
不吸烟
爱干净
```

这些首先是 **advertised terms / desired traits**。

不能自动写成：

```yaml
actual_monthly_rent: 800
actual_roommate_gender: female
actual_roommate_job: IT
actual_roommate_smoking: false
```

因为现实结果可能发生：

- 议价；
- 分摊比例调整；
- 房东临时加价；
- 水电另算；
- 最终接受不符合原偏好的人；
- 帖子从未匹配成功。

硬规则：

> **listed rent ≠ paid rent**
>
> **roommate preference field ≠ actual roommate trait**

这对以后做结构化 extraction 尤其重要。

---

## 11. location precision：为了研究住房，也不要重新暴露普通人的旧地址

合租帖往往比一般论坛帖子包含更多可识别信息：

- 小区 / 楼栋；
- 单位 / 学校；
- 电话；
- Email；
- QQ；
- 性别 / 年龄；
- 职业；
- 作息；
- 预算；
- 与谁同住。

这使它既有研究价值，也有更高隐私风险。

本仓遵循 `AGENTS.md` 和 `METHOD.md` 的研究必要最小化原则：

- 不批量重新公开旧电话号码；
- 不在仓库建立普通用户姓名—手机号索引；
- 不为了“复原现场”重新拼出精确门牌；
- 研究页面字段时优先抽象 schema / pattern；
- 需要引用个案时，只保留证明 claim 所需的最少生活信息；
- 个人今天已经成年或公开活跃，也不构成重新扩散其旧住房资料的充分理由。

建议：

```yaml
location_precision: city | district | neighborhood | exact_address_present_redacted | unknown
contact_channels: phone | email | qq | private_message | other
contact_value_preserved: false
privacy_redactions:
```

---

## 12. online discovery ≠ end-to-end online housing transaction

2003—2011 的住房匹配中，Web 可以承担：

- 发布；
- 搜索；
- 初步筛选；
- 留联系方式；
- 公开问答。

但通常仍需要：

```text
phone / QQ / Email
→ 约时间
→ 到现场看房
→ 检查钥匙 / 水电 / 室友
→ 谈押金
→ 签纸质合同或口头约定
→ 搬运行李
→ 实际共同生活
```

因此：

> **online discovery ≠ online transaction ≠ digital household**

这与本仓现有 transactional archaeology 一致：页面只是流程的一部分，运行态和线下执行不能从表单页面反推。

---

## 13. 建议的 roommate-listing artifact schema

以后若为房屋 / 合租站点建 evidence fixture，可以使用：

```yaml
platform:
site_host:
board_or_category:
listing_url:
listing_id:
listing_type: room_offered | room_wanted | roommate_wanted | teamup | sublet | unknown

author_account:
internal_post_datetime:
internal_edit_datetime:
archive_capture_datetime:
current_survival_observed_at:

city:
location_precision:
room_type:
listed_rent:
listed_deposit:
listed_utilities_terms:
roommate_preferences:

contact_channels:
contact_values_redacted: true
public_reply_visibility:
private_contact_likely:

explicit_listing_status: available | filled | withdrawn | expired | unknown
fill_evidence:
offline_viewing_evidence:
agreement_evidence:
move_in_evidence:
co_residence_evidence:
exit_evidence:

source_layer: original_listing | archive_capture | current_survival | contemporary_media | later_recollection | reconstruction
source_speaker:
evidence_grade: A | B | C | D
confidence:

repost_relation:
provenance_family:
encoding_state:
browser_assumption:
privacy_redactions:
notes:
```

尤其不要把 `listed_*` 字段重命名成 `actual_*`，除非另有结果证据。

---

## 14. 已知 / 高概率 / 不知道

### 已知

- 2003 年纸质校园公告栏仍在承担室友匹配；
- 同期媒体已经观察到地方网站“租屋信息”栏目用于陌生人合租匹配；
- 2005 年媒体采访至少保存一条“网上发帖 → 回复 → 见面 / 看房 → 共同居住”的完整个案链；
- 2011 年水木当前存续《合集》保存了长达数年的租房 / 换室友 / 搬家叙事及多名回复者材料；
- BBS / Web 只能直接证明它所保存的页面状态，不能自动证明真实共同居住结果。

### 高概率但仍需更强原始 artifact

- 2000s 初期中文校园 BBS、地方论坛和门户租房栏目已经存在大量普通的同性 / 同学 / 同事合租信息；
- 找到候选人后，大量实际筛选转移到电话、QQ、Email 和线下看房；
- 许多“成功找到室友”的结果不会被原帖明确回写。

### 不知道

本轮尚未解决：

- 2003 海口报道所指地方网站的精确原始 URL 与可核验 archive capture；
- 2005 广州个案的原 listing URL 与回复记录；
- 2011 水木《合集》各组成帖在 2011 年的原始 HTML / capture 是否完整可得；
- 早期平台是否普遍具有“已租出 / 关闭”结构化状态；
- 不同平台普通 roommate listing 的成功率、平均存续时间和平均同住时长；
- 同性室友、异性室友、同学 / 同事 / 陌生人合租在总体中的真实比例。

这些都不能靠今天搜索到多少页面来补。

---

## 15. 对 archive gap model 的新增：listing survival ≠ household survival

本篇为以后 M4 / Phase 5 的 archive-gap 模型增加四个字段方向：

### A. listing survival

是否保存：

- 列表页；
- 具体 listing；
- 图片；
- 作者资料；
- 回帖。

### B. state survival

是否能知道：

- 帖子是否仍有效；
- 已租出；
- 已撤回；
- 过期；
- 后来编辑。

### C. interaction survival

是否保存：

- 公开回复；
- 私信；
- 电话 / Email / QQ handoff 的存在证据。

### D. outcome survival

是否保存：

- 看房；
- 签约；
- move-in；
- 实际 co-residence；
- 搬离 / 换室友。

四者通常高度不对称。

最重要的结论是：

> **archived housing market ≠ historical housing life.**

档案可能非常擅长保存“人当时想怎样找房”，却非常不擅长保存“最后和谁住、住了多久、为什么又搬走”。

---

## 16. 对生活史的交叉意义

旧网住房页不是生活史的直接数据库，但可以帮助回答：

- 某时期一个人是否可以跨出原有熟人圈寻找室友；
- 合租条件如何被写成结构化偏好；
- 房租、通勤、性别、安全、职业和作息如何进入筛选；
- 一条迁移 / 实习 / 恋爱团聚路线是否有短期住房模块可接；
- 线上自我陈述如何暂时成为“能不能一起住”的现实筛选接口。

同时，它必须不断提醒生活史研究者：

> **一个幸存的房源广告，是一个可能的生活路径入口，不是已经完成的生活。**

因此与 how-people-lived 的分工是：

- 本仓保存 / 分析 listing、页面结构、状态、provenance、archive gap；
- `how-people-lived` 分析居住串行性、非亲属 household、工作 / 关系 / 迁移 / 通勤与住房如何共同组成实际生命历程；
- 全球 Usenet / Craigslist 等海外对照留在 how-people-lived，不扩张本仓全球 scope。

---

## 17. 下一步最有价值的旧网证据

1. 找到 1998—2004 中文 BBS / 地方站中**同一 listing 的多个时间状态**，尤其是“求租 → 已找到 / 撤帖”；
2. 找到一个可复核的校园 BBS 房屋版 archive capture，记录列表页、帖子 URL pattern、回帖与编码 / 浏览器环境；
3. 对水木 2011《合集》逐 item 建 provenance map，区分主帖、回复、转载、重复 / 编码异常；
4. 如果取得可合法分析的历史 WARC / dump，再测量“公开 listing 有多少具有明确 filled/withdrawn 状态”，不要用当前 Web 搜索结果估成功率；
5. 与 `LOCATION_COPRESENCE_AND_DISTRIBUTED_HOUSEHOLD_INFERENCE_1999_2015.md` 联合制定 `listing evidence → co-residence claim` 的最低升级门槛。

在取得这些证据前，最稳妥的正式结论仍然是：

> **中文旧网确实已经成为陌生室友发现和住房搜索的一层基础设施，但公开可保存的 listing 与真实 household outcome 之间存在系统性、且很难从 Web archive 自动填平的断裂。**
