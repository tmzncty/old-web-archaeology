# JOB_PORTAL_CITY_FILTERS_RESUME_GEOGRAPHY_REMOTE_APPLICATION_AND_RELOCATION_STATE_GAPS_1999_2015

## Scope

本说明研究约 1999–2015 中文旧网里一类高度影响普通人生，却特别容易被网页档案高估的对象：

**全国招聘网站、城市频道、职位搜索、在线简历与远程申请怎样把“去另一座城市工作”变成可在屏幕上提前搜索的路线。**

本说明不扩展为一般就业史，也不研究 2015 年后的 APP 招聘生态。

它与仓库已有文件有明确边界：

- [`APPLICATION_STATE_ELIGIBILITY_AND_ROUTE_PORTFOLIO_2003_2015.md`](APPLICATION_STATE_ELIGIBILITY_AND_ROUTE_PORTFOLIO_2003_2015.md) 主要研究研究生、公务员等制度性申请中的资格审查与 adjudicated state；
- [`CAMPUS_PARTTIME_BBS_SHORT_GIGS_SCHEDULE_PAYMENT_AND_OUTCOME_GAPS_2005_2009.md`](CAMPUS_PARTTIME_BBS_SHORT_GIGS_SCHEDULE_PAYMENT_AND_OUTCOME_GAPS_2005_2009.md) 研究校园 BBS 短期兼职；
- [`DAY_LABOR_TEMP_JOB_LISTINGS_DISPATCH_SHIFT_AND_SETTLEMENT_STATE_GAPS_2009_2011.md`](DAY_LABOR_TEMP_JOB_LISTINGS_DISPATCH_SHIFT_AND_SETTLEMENT_STATE_GAPS_2009_2011.md) 研究日结/临工派遣；
- 本说明研究的是**全国/跨城市一般招聘门户里，从职位地理字段到现实迁移结果之间的状态断裂。**

生活史解释写回 `tmzncty/how-people-lived`；本仓只处理约 1995–2015 中文 Web 的平台状态、页面状态、动态数据库状态与保存偏差。

---

## 1. 研究单位：一条招聘结果不是“一份工作”

一个在线招聘系统至少可以包含：

```text
public recruitment portal
→ city channel / geographic filter
→ job-search query
→ search-result item
→ job-detail page
→ current vacancy state
→ job-seeker account
→ resume profile/version
→ application submission
→ employer ATS/eHire queue
→ recruiter opens/downloads resume
→ recruiter contacts candidate
→ interview invitation
→ interview channel/location
→ interview completed
→ offer
→ offer accepted
→ relocation
→ arrival
→ onboarding
→ actual work location
```

因此本说明固定以下硬规则：

> **job page exists ≠ vacancy still open**

> **search result visible ≠ applicant eligible**

> **application submitted ≠ recruiter opened it**

> **resume opened ≠ interview invitation**

> **interview invitation ≠ interview completed**

> **offer issued ≠ accepted**

> **offer accepted ≠ person relocated**

> **relocated ≠ onboarding completed**

> **advertised city ≠ actual everyday work location**

公共 Web 最容易保存前半段；真正改变一个人住在哪座城市的状态，几乎都在后半段。

---

## 2. 为什么这一对象属于 old-web archaeology，而不只是就业史？

招聘门户改变了旧 Web 的一个基础关系：

普通文章页主要让人**读一件事**；

招聘门户让用户把现实未来写成查询：

```text
city = Shanghai
job_category = software
salary = ...
keyword = ...
```

然后从动态数据库返回一组未来可能性。

这类页面的历史证据单位不是单纯 HTML。

需要至少区分：

1. search form；
2. query parameters / POST state；
3. dynamic index/database；
4. result ranking；
5. job-detail record；
6. authenticated resume/application state；
7. employer-side private state；
8. offline phone/email/interview state；
9. real relocation outcome。

因此，一个“保存完整”的招聘首页仍可能几乎没有保存真正的招聘系统。

---

## 3. 2004 年 51job SEC 文件：一个少见的 contemporaneous product contract

51job 在 2004 年 IPO 时向 SEC 提交的 F-1，为早期中国招聘 Web 提供了一个比后来产品回忆更可靠的平台功能截面。

### A 级来源

- 51job, Inc., 2004 F-1：  
  <https://www.sec.gov/Archives/edgar/data/1295484/000114554904000896/u99016fv1.htm>

这是**同期公司正式申报文件**。

它适合证明：

- 公司当时声明哪些产品存在；
- 产品之间如何连接；
- 公司如何定义账号、简历、雇主等统计对象；
- 收入结构和业务结构。

它不能自动证明：

- 所有页面都无故障可用；
- 普通用户体验符合宣传；
- 每个简历都被招聘者查看；
- 每个岗位都真实有效；
- 公司自称的市场领先地位客观成立。

### 3.1 city-by-city 与 nationwide 同时存在

F-1 明确称：

- `www.51job.com` 于 1999 年建立；
- 在线招聘广告以 **city-by-city basis** 提供；
- 网站同时包含全国性的大量招聘广告；
- 公司认为全国网站让雇主接触到 wide geographic area 的候选人。

这意味着城市不是只写在职位正文里。

它已经成为招聘系统的组织维度。

对考古而言，应单独记录：

```yaml
geography_role:
  advertised_job_city: true
  city_channel_or_partition: true
  query_filter_verified: unknown_or_capture_dependent
  candidate_desired_city: capture_dependent
  actual_work_city: unknown_without_outcome_evidence
```

不能因为 `Shanghai` 出现在 URL/频道名里，就把它和现实工作地点合并。

### 3.2 print 与 Web 是同一个招聘系统的两种表面

2004 F-1 还说明：

- `Career Post Weekly` 是 city-specific 周刊；
- 截至 2004-06-30 覆盖 19 个城市；
- 纸质周刊广告同时发布到 `51job.com`；
- 网站另有 online-only advertisements；
- 网站招聘广告通常 hourly update。

公司 2003 年收入里：

- print advertising 62.3%；
- online recruitment services 26.2%。

这些是**公司收入占比，不是用户媒介使用率**。

但它们证明一个重要结构：

> **招聘 Web 不是突然替代报纸，而是在相当长时间里与地方报纸、招聘周刊、招聘会相互复制和导流。**

因此历史页面的 provenance 可能需要追问：

```text
job record originated online?
job record copied from Career Post Weekly?
print ad appeared first?
web version was a basic description or full ad?
```

同一个职位在纸面与 Web 上可能不是同样粒度的 artifact。

---

## 4. “当前职位”也是动态状态，不是页面永久属性

51job F-1 声称求职者可以：

- search and review all current recruitment advertisements；
- 接收与 profile/preferences 匹配的职位 email；
- 直接提交简历；
- organize and track applications；
- 获取招聘会信息。

同时文件说明新在线广告通常几小时内上线，来自纸质周刊的 complimentary postings 通常一至两天上线。

这至少说明平台自身已经存在**时效差异**。

因此建议新增：

## vacancy freshness gap

```text
employer has a vacancy
→ employer submits ad
→ platform accepts/processes
→ database record goes live
→ page/query exposes record
→ position remains open
→ recruiter still reviewing
→ position filled/closed
→ page/index removes or marks it
```

一个 archive capture 只冻结其中一个时点。

如果 2004-05-01 保存下职位页，最多证明：

> 在 capture 可观察状态下，该 URL/内容被档案服务保存。

不能自动证明：

- 当天还有 headcount；
- 招聘者继续收简历；
- 网页状态与企业内部状态同步；
- 该职位不是从纸质广告延迟同步来的。

---

## 5. 搜索结果页是数据库投影，不是职位全集

招聘门户的 search result 至少经过：

```text
query
→ parser
→ geographic/category filters
→ current searchable index
→ ranking/sort
→ pagination
→ user-visible results
```

所以：

> **no result ≠ no job existed in city**

可能原因包括：

- 岗位未进入该平台；
- 岗位只在纸质周刊/人才市场；
- 关键词不匹配；
- 分类错误；
- 城市字段不同；
- 已下线；
- query parameter 丢失；
- archive 没保存动态 response；
- session/cookie 不完整。

同样：

> **result count ≠ stable historical count**

招聘结果数量高度依赖查询时间和后台 index，不能把一张 screenshot 上的“共 28,531 个职位”当成某城市永久岗位存量。

---

## 6. City field 必须拆成至少四个地理对象

旧招聘页经常给后人一种“地点很精确”的感觉。

实际上至少需要：

```text
candidate_current_location
candidate_desired_location
advertised_job_location
actual_interview_location
actual_work_location
```

还可能有：

- 公司注册地；
- 总部；
- 分公司；
- 培训地；
- 派驻地；
- 项目现场；
- 多地轮岗。

因此：

> **job_location = Beijing**

不能自动推成：

> **this person moved to Beijing and worked daily in Beijing.**

这是招聘 Web 考古与真实迁移史之间最重要的 stop condition 之一。

---

## 7. Resume 不是人：简历数据库有自己的生命周期

51job 2004 F-1 称截至 2004-06-30：

- 自 1999 网站建立以来约有 6.9 million job user accounts established；
- 约 4.6 million resumés posted online。

这些是平台定义的对象。

不能写成：

```text
6.9M accounts = 6.9M unique people
4.6M resumes = 4.6M currently searching people
```

一个人可能：

- 有多个账号；
- 有多个简历版本；
- 更新工作城市；
- 改期望城市；
- 找到工作后忘记删除；
- 长期不登录；
- 允许/禁止招聘者搜索；
- 对不同岗位投不同版本。

因此新增：

## resume-state gap

```text
resume created
→ saved
→ published/searchable?
→ indexed in employer database?
→ current version?
→ candidate still available?
→ employer query matches?
→ employer sees summary?
→ employer downloads/opens?
→ candidate contacted?
```

历史档案通常只会保存 public help/product pages，很难保存一个普通人的私有 resume state。

### 隐私规则

本仓**不需要**为了证明早期简历功能存在而重新公开普通人的历史简历。

优先保存：

- 字段角色；
- UI 说明；
- 产品手册；
- company filing；
- 匿名化截图/结构。

不保存普通用户的：

- 姓名；
- 电话；
- email；
- 家庭住址；
- 身份证件；
- 完整教育/工作轨迹。

---

## 8. application submitted ≠ recruiter read：2008 同期生活材料提供了反证

2008 年末《半月谈》的应届生调查记录：浙江大学城市学院应届生唐莎莎（化名）曾在 20 天里网上投近 500 份简历；同一报道又记录“海投”成为同学间常见策略讨论。

来源：

- **B（同期媒体调查/第一人称）**：  
  <https://www.chinanews.com.cn/edu/qzjy/news/2008/12-30/1508751.shtml>

这类材料最有用的地方不是“500”本身，而是它证明：

**submission throughput 可以远高于 human review throughput。**

因此招聘门户至少应拆成：

```text
apply-button click
→ request accepted
→ application record created
→ attached resume version resolved
→ delivered to employer-side queue
→ visible to recruiter
→ recruiter actually opens
→ recruiter decides
→ contact attempt
```

archive 中即使保存一个“投递成功”模板，也只能证明 UI/可能的成功分支存在。

如果没有用户级后台或日志证据，不得把它升级成：

- 招聘者收到了；
- 招聘者读了；
- 被拒绝；
- 获得面试。

---

## 9. Employer-side eHire / ATS 是公共 Web 看不见的另一半

51job F-1 明确说雇主可以通过 eHire：

- 搜索候选人数据库；
- 下载简历；
- manage / organize / streamline recruitment and hiring process。

这非常重要，因为它证明招聘站不是：

```text
职位页 + 一个邮件地址
```

至少已经存在 private employer-side workflow。

建议模型：

```text
public application
→ employer account
→ candidate inbox/queue
→ recruiter filter
→ resume preview/download
→ internal notes/status
→ phone/email contact
→ interview
```

公共 archive 很可能只保存到第一箭头之前。

于是出现：

## public-opportunity / private-selection gap

> **越接近“这个人会不会真的搬去另一座城市”的状态，越可能退出公共 Web。**

---

## 10. 远程发现与远程筛选必须分开

2000s 的招聘站很容易让今天的研究者误以为：

> “既然可以网上投简历，所以求职已经不需要去目标城市。”

这是错误的。

2008 的同期毕业生材料同时记录：

- 大量网上投递；
- 大型实体招聘会；
- 多轮线下面试；
- 毕业生跨地区寻找落脚工作。

因此：

## remote-discovery gap

```text
job can be discovered remotely
≠
application can be completed remotely
≠
interview can be completed remotely
≠
job can be performed remotely
```

旧网研究如果只恢复职位搜索页面，会系统性低估**面试旅行成本**。

---

## 11. 2010s：城市字段更加成熟，但不要反投影 UI

后期 51job SEC 年报对在线产品写得更具体，包括求职者可按 city of employment、industry、job function、job title、posting date 等条件搜索。

这些后期文件可以证明：

> 到该年，city 已经明确是可查询条件之一。

但不能反推：

> 2001 年搜索表单一定有完全相同字段、标签、排序和 endpoint。

### 方法规则

若使用 2010s A 级产品文件解释 2000s：

必须写成：

```text
later verified state: city filter existed by YEAR
unknown: exact first appearance and earlier UI/parameter form
```

而不是凭品牌连续性补历史页面。

---

## 12. 海外对照：Monster 证明 geographic search 是跨国在线招聘机制

Monster Worldwide 2003 SEC 文件称：

- Monster 源自 1994 Monster Board；
- 求职者可以按 location、job category、industry、keyword 搜索职位；
- Job Search Agent 可按 industry/location/keywords 周期扫描数据库，并把结果发到 email，用户离线时也可工作；
- 雇主端 Customized Resume Access 支持 geographic searches。

来源：

- **A（同期公司 SEC 文件）**：  
  <https://www.sec.gov/Archives/edgar/data/1020416/000104746903037619/a2121724zs-3a.htm>

本仓不把 Monster 写成研究对象，因为 scope 是中文旧网。

它只提供一个方法学对照：

> **把工作地点和候选人地点变成查询字段，是在线招聘时代的跨国共同结构，并非中国网站特有。**

中国案例更值得考古的是：

- city-by-city 纸质招聘与全国 Web 同步；
- 人才市场、招聘会和网站长期共存；
- 招聘平台与高速城市化/跨城市择业同时扩张。

---

## 13. 2020 以后只作为生活史边界，不扩大本仓 scope

2020 疫情推动在线招聘从“网上报名/简历筛选”进一步进入远程笔试、视频面试。

同期《中国青年报》调查记录 1923 名应届生中：

- 82.4% 的受访者在线投简历；
- 58.2% 参加线上面试；
- 51.5% 参加线上笔试；
- 27.2% 经历线上录取。

来源：

- <https://www.jiemian.com/article/4204203.html>

这组材料在本说明中的用途只有一个：

> **说明 1999–2015 旧网招聘时代的 remote application 不应被后见之明改写成完整 remote hiring。**

2020 后的 Zoom/腾讯会议/招聘 APP 不是本仓主研究对象。

---

## 14. “线上招聘消灭地理限制”的反证：2020 张梦个案

中国青年报 2020 年同期报道中的毕业生张梦（化名）在河南老家收到 3 封上海面试通知后，仍然买机票返回上海，临时租了一间仅剩两周租期的房间，随后跨多个区跑面试，直到租期结束前几天才敲定工作。

来源：

- <https://zqb.cyol.com/html/2020-08/10/nw.D110000zgqnb_20200810_1-06.htm>

这个 2020 个案不写进本仓的旧网页谱系，却是一个很好的**解释边界**：

如果连 2020 都仍可能出现：

```text
email invitation
→ flight
→ temporary rental
→ citywide interviews
```

就更不能仅凭 2004 的“online application”功能把 2000s 求职重构成无地点流程。

---

## 15. 从 Web 到现实迁移：需要一条 relocation execution stack

推荐状态模型：

```text
job discovered
→ job detail read
→ applicant decides destination acceptable
→ application submitted
→ recruiter sees application
→ contact succeeds
→ interview invited
→ interview channel chosen
→ interview completed
→ offer issued
→ offer accepted
→ travel booked
→ temporary housing available
→ body arrives
→ employment paperwork completed
→ onboarding starts
→ actual work begins
```

另有并行制度链：

```text
personnel file / credential / hukou / residence / social-insurance state
```

这些链不能合并成一个 `hired=true`。

### 新概念：relocation outcome darkness

公共网页能非常精确地保存：

- 公司名；
- 岗位名；
- 城市；
- 工资区间（若当年显示）；
- 发布时间。

却通常完全看不见：

- 最后录了谁；
- 谁拒绝；
- 谁买了票；
- 谁搬家；
- 谁到岗三天后离职。

因此招聘 Web 具有一种特殊的历史偏差：

> **opportunities are public; realized life courses are private.**

---

## 16. 建议固定的 state gaps

### 16.1 `job-page / vacancy-state gap`

职位页存在，不等于内部 headcount 仍开放。

### 16.2 `posting-time / index-time gap`

雇主提交、平台处理、搜索可见、archive capture 是不同时间。

### 16.3 `print / web synchronization gap`

纸质招聘广告与 Web 副本可能有一至数日或其他同步差。

### 16.4 `city-label / actual-work-location gap`

页面城市字段不等于实际每日工作地点。

### 16.5 `query / searchable-index gap`

一个查询结果只反映特定时点、特定参数下的 index 投影。

### 16.6 `search-ranking gap`

搜索可见并不等于所有职位获得相同曝光；后期平台可能存在付费排序、广告位等商业机制。

### 16.7 `account / person gap`

registered account 不是 unique person。

### 16.8 `resume / current-job-seeker gap`

一份历史简历不等于该主体当时仍在求职。

### 16.9 `resume-version gap`

下载/投递的具体版本可能不是今天残留页面看到的版本。

### 16.10 `resume-searchability gap`

“已创建简历”不等于“雇主数据库中可搜索”。

### 16.11 `application / recruiter-delivery gap`

前端成功不等于企业侧队列成功生成记录。

### 16.12 `delivered / opened gap`

招聘者收到不等于打开。

### 16.13 `opened / contact gap`

打开不等于发出电话/email。

### 16.14 `contact / interview gap`

联系成功不等于面试发生。

### 16.15 `remote-discovery / remote-interview gap`

远程找到岗位不等于远程完成面试。

### 16.16 `offer / acceptance gap`

offer 是公司提出的未来，不是求职者已经选择的未来。

### 16.17 `acceptance / relocation gap`

接受 offer 不等于身体真正迁移。

### 16.18 `relocation / onboarding gap`

到了城市不等于最终入职。

### 16.19 `public-page / private-ATS gap`

公共 archive 通常无法保存 eHire/ATS 内部流程。

### 16.20 `web-state / institutional-record gap`

招聘站不会自动告诉我们人事档案、户籍、资格、社保等制度状态。

---

## 17. Archive capture：本轮没有把 locator 冒充验证结果

本轮取得了：

- 51job 2004 SEC 的同期正式产品描述；
- 2003–2004 51job 自身媒体/内容页及同期媒体报道入口；
- 2008 同期求职者在线投递和线下招聘体验；
- 海外 Monster 2003 SEC 对照。

但本轮**没有取得并实际验证一份足以复原 1999–2004 `www.51job.com` 搜索流程的历史 Wayback capture**。

因此以下字段保持 unknown：

```yaml
validated_capture_1999_2004: false
historical_homepage_dom: unknown
historical_search_form_dom: unknown
historical_charset: unknown
historical_query_method_get_or_post: unknown
historical_city_parameter_name: unknown
historical_result_url_pattern: unknown
historical_login_cookie_structure: unknown
historical_resume_submit_endpoint: unknown
historical_application_success_template: unknown
historical_javascript_requirements: unknown
historical_browser_requirement: unknown
```

即使搜索引擎今天能找到旧域名、旧媒体页或 Wayback locator，也不满足 `docs/METHOD.md` 对 verified capture 的要求。

后续只有实际打开 capture、确认不是错误页/重定向/robots 占位，并检查主文档与子资源后，才能升级。

---

## 18. 如果未来拿到 capture，应该怎么验？

### 18.1 页面级

记录：

```yaml
original_url:
capture_url:
capture_datetime:
archive_source:
http_or_replay_state:
charset:
content_type:
page_title:
city_context:
login_required:
```

### 18.2 查询级

记录：

```yaml
query_form_present:
method:
action:
city_field_name:
keyword_field_name:
category_field_name:
salary_field_if_any:
query_string_preserved:
result_count_present:
pagination_present:
sort_options:
```

### 18.3 动态资源

检查：

- JS 是否 archive-rewritten；
- result URL 是否可回放；
- 搜索结果是否来自当年保存 response 还是今天 live backend；
- 图片/CSS 是否完整；
- session 是否必要；
- login redirect 是否阻断；
- form submit 是否只是向已死 endpoint 发请求。

### 18.4 Browser assumption

早期中文招聘页可能受：

- IE 行为；
- GB2312/GBK；
- table layout；
- popup；
- frame/iframe；
- JS validation；

影响。

没有实际 capture 时不猜。

---

## 19. 一个高风险误读：旧招聘网页会制造“全国市场一直在那里”的错觉

今天检索老网页时，研究者可能看到：

- 北京频道；
- 上海频道；
- 广州频道；
- 数以万计岗位；
- 简历库规模；
- 全国覆盖宣传。

于是容易写成：

> “2004 年求职者已经可以在一个成熟全国劳动力市场里自由移动。”

这至少漏了五个层面：

1. 谁家里/学校/网吧有可用 Internet；
2. 谁属于招聘门户偏爱的职业/教育用户群；
3. 一条职位是否真的开放；
4. 是否还必须跨城参加实体面试；
5. 找到岗位后是否有钱、住房和制度条件真正搬过去。

因此推荐固定一句：

> **A searchable labor market is not the same thing as an executable labor market.**

---

## 20. 与 how-people-lived 的交叉链接

生活史侧应重点读取：

`tmzncty/how-people-lived/topics/moving-city-as-career-strategy-job-search-relocation-and-reversible-mobility-china-1980-2026.zh-CN.md`

那里研究：

- move-first search vs search-first move；
- relocation commitment point；
- 人事档案与身体迁移；
- 2008 “海投”与“先落脚”；
- 2019 城市的阶段性选择；
- 2020 远程面试；
- 2023–2026 可逆迁移和临时住宿缓冲。

本仓不把这些 2016–2026 生活史材料扩展为旧网主 scope。

---

## 21. Evidence matrix

| Claim | Evidence | Grade | What it proves | What it does not prove |
|---|---|---:|---|---|
| 51job website established in 1999 | 2004 SEC F-1 | A | company contemporaneously declared launch and product history | exact 1999 DOM/capture |
| Online ads organized city-by-city | 2004 SEC F-1 | A | city was a product organization dimension | exact search field UI in every year |
| Print ads and Web were coordinated | 2004 SEC F-1 | A | hybrid media pipeline existed | every record synced perfectly |
| Website updated ads hourly | 2004 SEC F-1 | A | company-declared operational cadence | every user saw a fresh vacancy |
| Job seekers could search, receive matching emails, apply, track | 2004 SEC F-1 | A | feature contract | successful hiring outcome |
| Employers used eHire resume tools | 2004 SEC F-1 | A | private employer workflow existed | contents of any ordinary user's case |
| 2008 graduates could send hundreds of online applications | contemporary press interview | B | lived use and submission abundance existed | representative average |
| Physical recruitment fairs remained important | contemporary press | B | hybrid online/offline job search | share of all job search |
| Geographic resume/job search also existed abroad | Monster 2003 SEC | A | cross-national structural comparison | Chinese adoption level |
| Exact 1999–2004 51job search DOM/charset/endpoints | no verified capture this run | unknown | — | must not reconstruct |

---

## 22. 已证实 / 高概率 / 不知道

### 已证实

- 51job 在 2004 同期 SEC 文件中把 1999 作为网站建立年份。
- 2004 前后其招聘业务明确是 city-specific print + city-by-city online + nationwide website 的混合结构。
- 求职者已有搜索、匹配邮件、直接投简历、申请信息管理等在线功能。
- 雇主已有 eHire 搜索/下载简历和管理招聘流程的私有 Web 工具。
- 2008 同期个人材料证明网上海投与实体招聘会可以同时成为同一个人的求职日常。
- Monster 2003 同期材料证明 location/geographic search 是国际在线招聘共同技术结构。

### 高概率但需 capture 加强

- 2000s 中期普通 51job 用户已经在具体 UI 中频繁把城市作为职位筛选条件。
- 搜索结果和职位详情存在动态 index/version 差异。
- 登录、简历、投递状态的大部分历史记录因认证和数据库后端而没有进入公共 archive。

### 不知道

- 51job 1999–2004 各年份精确 DOM、charset 和 query parameter。
- 城市筛选首次出现的准确日期和 UI 变化。
- 2004 普通用户一次投递后招聘者侧的真实状态机字段。
- 某个公开历史职位最终由谁获得、是否跨城搬迁、是否到岗。
- 一条 Web 广告从 employer submit 到 public index 的真实逐条延迟分布。

---

## 23. 后见之明风险

1. **不要把 2020 视频面试体验倒推到 2004。**
2. **不要把 2010s 搜索字段倒推成 1999 完全相同 UI。**
3. **不要把注册账号数写成独立活跃求职人数。**
4. **不要把 posted resume 写成当时仍求职。**
5. **不要把“在线职位很多”写成普通人现实可获得机会很多。**
6. **不要把页面城市写成最终迁居城市。**
7. **不要把线上申请当成招聘流程已完整在线。**
8. **不要把一个品牌跨十几年视为同一后台系统。**
9. **不要因为页面在 archive 中活着，就假定 dynamic database / ATS 也被保存。**
10. **不要为了复原用户简历而重新公开普通人的敏感历史资料。**

---

## 24. 下一步最值钱的 old-web artifact

优先目标不是再找“前程无忧成立于哪年”的文章，而是实际验证一份约 1999–2005 的中文招聘 portal capture，最好能取得：

```text
homepage
→ city channel
→ search form
→ one preserved query/result
→ one job detail
→ login/application boundary
```

逐项恢复：

- original URL；
- capture datetime；
- charset；
- form method/action；
- city field；
- keyword/category field；
- result URL pattern；
- dynamic asset loss；
- login/session boundary；
- browser assumption。

如果最后只能恢复 public result 而无法恢复 application backend，也应明确写出：

> **我们保存了“这座城市看起来有哪些未来”，但没有保存这些未来后来落到谁身上。**

这本身就是一条重要的旧网考古结论。

---

## Sources

### Primary / contemporaneous platform evidence

- 51job, Inc. 2004 F-1, SEC:  
  <https://www.sec.gov/Archives/edgar/data/1295484/000114554904000896/u99016fv1.htm>
- 51job 2003 corporate media page, useful as a contemporaneous product-context artifact but not a full recruitment-flow capture:  
  <https://media.51job.com/2003/0601.htm>
- Monster Worldwide 2003 SEC filing, overseas comparison only:  
  <https://www.sec.gov/Archives/edgar/data/1020416/000104746903037619/a2121724zs-3a.htm>

### Contemporary lived-use evidence

- 2008-12-30，《展望2009：百名应届大学毕业生择业生态调查》：  
  <https://www.chinanews.com.cn/edu/qzjy/news/2008/12-30/1508751.shtml>

### Later boundary checks, not old-Web product evidence

- 2020-04-02，《“解锁”线上求职 应届生准备好了吗》：  
  <https://www.jiemian.com/article/4204203.html>
- 2020-08-10，《就业季突围》：  
  <https://zqb.cyol.com/html/2020-08/10/nw.D110000zgqnb_20200810_1-06.htm>

---

*Initial research synthesis was AI-assisted. No ordinary user's private resume, account or application record was republished. No unverified archive locator is treated as a historical capture.*
