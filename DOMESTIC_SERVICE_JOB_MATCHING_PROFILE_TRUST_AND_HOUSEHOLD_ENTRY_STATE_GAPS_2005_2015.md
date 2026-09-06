# Domestic-service job matching, profile, trust, and household-entry state gaps, China 2005–2015

## Scope

本笔记研究约 2005–2015 中文 Web 中与家政、保姆、月嫂、钟点工、家庭护理等供需匹配有关的网页与事务状态。

它不是“中国家政行业史”，也不把仓库 scope 扩成全球照护史。目标是回答：

> **当中文 Web 上已经出现“找保姆”“保姆求职”“在线选阿姨”“视频面试”以后，一个 archive capture 离现实中某个劳动者真正走进某户家庭开始服务，还有多少状态没有被保存？**

对应生活史专题：

- `tmzncty/how-people-lived/topics/paid-domestic-service-household-outsourcing-care-chains-and-digital-matching-china-1983-2026.zh-CN.md`

本轮尤其关注：

- 供需 listing；
- 家政协会/社区服务网站；
- 电话热线与 Web 目录的 handoff；
- QQ / 网络视频面试；
- 中介代家政工上网的 proxy digitality；
- 身份、健康、技能与诚信字段；
- 住家/不住家、工种、工资和任务字段；
- 春节供给变化；
- 页面上的库存与现实可派人员之间的差距；
- Web 以后真正成交、试工、入户和服务连续性为何很难被 archive 看到。

---

## 1. 最低证据合同

继续遵守仓库既有方法：

```text
industry / institution
≠ site
≠ page
≠ listing
≠ worker profile
≠ available worker
≠ mutual agreement
≠ physical household entry
≠ successful service
≠ durable employment relation
```

### 1.1 `site exists ≠ matching transaction exists`

家政网站可能只提供：

- 公司介绍；
- 行业新闻；
- 电话；
- 培训；
- 工资行情；
- 求职/招聘信息；
- 门店地址。

即使存在“在线找保姆”栏目，也不能自动推出：

- 需要账号；
- 需要实名；
- 可以站内私信；
- 可以在线支付；
- 可以直接预约；
- 平台掌握实时库存；
- 平台是劳动者雇主。

### 1.2 `listing posted ≠ worker found`

最小状态应拆成：

```text
household has need
→ household finds site/intermediary
→ requirement entered/published
→ page becomes visible
→ worker/intermediary notices it
→ worker is actually available
→ worker accepts basic conditions
→ contact succeeds
→ interview occurs
→ identity/health/skill checked
→ salary/time/rest agreed
→ worker travels to household
→ household admits worker
→ trial work occurs
→ both sides continue
```

2006 年广州已有同期反例：雇主在网站发帖大半个月、同时跑三家线下公司，仍然没有找到保姆。

### 1.3 `worker profile online ≠ worker personally online`

2006 年杭州记者现场验证“QQ/视频找保姆”时，实际网上打字的是中介工作人员，部分家政工本人识字有限、不会用电脑，由工作人员在雇主和劳动者之间口头转述。

因此必须新增字段：

```text
profile_operator:
  worker_self
  intermediary_staff
  family_proxy
  unknown
```

这类现象记为 **proxy digitality / 代理数字化**。

### 1.4 `advertised inventory ≠ deployable inventory`

“有 5000 名阿姨”“一万名保姆不回家”“海量简历”一类页面文案只能先证明：

> 平台/公司当时如此宣称。

现实部署还要检查：

- 是否已经在别家上工；
- 是否愿意接短单；
- 是否住在目标城市；
- 是否春节返乡；
- 工种是否匹配；
- 是否愿意住家；
- 时间是否重叠；
- 工资是否谈妥。

### 1.5 `credential shown ≠ suitability verified`

身份证、健康证、培训证、无犯罪记录、等级证书、评价等可以减少部分信息不对称，但不能自动证明：

- 页面数据仍然有效；
- 原证件真实；
- 平台实际核验过；
- 当前健康状态不变；
- 服务质量一定满足这户家庭；
- 劳动关系正规。

### 1.6 `online contact ≠ online service`

家政是强 physical-terminal 服务：

```text
网页可以远程
视频可以远程
签约可以远程
付款可以远程

但：
清洁 / 做饭 / 抱婴儿 / 扶老人 / 陪床
必须发生在现实地点
```

因此 household-entry state 必须单列。

---

## 2. 前史边界：2005 以前已有中介、熟人和组织化服务，Web 不是“第一匹配器”

本仓不向 1995 以前无限扩张，但为了避免后见之明，需要保存一条边界说明。

1983–1984 北京已经出现组织化家务服务公司，用户通过组织登记寻找家庭服务员；1990s 又有老乡介绍、家政门店和劳务市场。

Source lead:
- 北京日报 2026 档案整理，定位 1983/1984 原报：https://xinwen.bjd.com.cn/content/s6983c4ece4b0687a2890c698.html
- 新民晚报/新浪 2007 对一名 1993–1995 开始跨城做家政工的回忆：https://baby.sina.com.cn/news/2007-07-31/083428142.shtml

Evidence grade:
- **C/B，后来的档案整理和个人回忆。**

这里只用于固定边界：

```text
pre-Web matching already existed
```

不能用它恢复 1980s/1990s 页面。

---

## 3. 2005：供需开始作为公开 Web 文本出现

### 3.1 “中国家政服务网”上的男家政需求

2005 年《新闻晨报》报道，“中国家政服务网”负责人称已有 10 多人上网发帖寻找男保姆，需求包括：

- 搀扶/搬动失能男性老人；
- 擦身等性别敏感护理；
- 家庭重体力劳动；
- 驾驶、维修等组合技能。

Source:
- 新闻晨报/新浪教育，2005-01-04：https://edu.sina.com.cn/j/2005-01-04/96680.html

Evidence grade: **B，同期报道。**

### 可以确认

- 2005 年存在被同期媒体称作“中国家政服务网”的 Web 对象；
- 报道明确把“上网发帖子寻找男保姆”作为用户行为描述；
- Web listing 可以承载非常具体的家庭任务需求。

### 不能确认

本轮尚未恢复：

- historical host；
- 原帖 URL；
- DOM；
- charset；
- 发帖表单；
- 是否注册；
- 是否公开电话；
- 是否有“已找到”状态；
- 是否最终成交。

因此不能从报道里反向发明 UI。

---

## 4. 2006：Web/QQ 出现，但中介仍是协议翻译层

### 4.1 杭州“视频找保姆”：最重要的不是视频，而是代理操作

青年时报 2006 年记者到家政市场实际体验新服务：宣传语是通过 QQ 与保姆聊天、在线挑人；现场却发现：

- 服务人员坐在电脑前；
- 家政工在门口等待；
- 工作人员替家政工打字；
- 再把雇主的话转述给家政工；
- 一名求职者说自己识字不多，不会电脑，觉得还是面对面更方便；
- 一些雇主也认为必须当面见才放心。

Source:
- 青年时报/新浪，2006-02-10：https://news.sina.com.cn/s/2006-02-10/10508171869s.shtml

Evidence grade: **B，同期记者现场观察 + 第一人称。**

### 状态模型

```text
employer opens QQ/video
→ intermediary receives message
→ intermediary speaks to worker
→ worker answers orally
→ intermediary types reply
→ employer sees mediated digital identity
→ physical interview still requested
```

这意味着 archive 若只保存一个“视频找保姆”宣传页面，非常容易产生错误推断：

```text
bad inference:
worker had direct digital profile and direct chat capability
```

实际上当时至少有案例是：

```text
worker represented digitally by intermediary
```

### 新增 preservation bias：`interface-user attribution bias`

历史页面告诉我们“这个界面存在”，却未必告诉我们**真正敲键盘的人是谁**。

这类偏差也可能出现在：

- 农民工网上求职；
- 老年人政务；
- 家属代挂号；
- 网吧代办；
- 中介替用户上传资料。

---

## 5. 2006 广州：成功发布 listing，也可能长期没有可用供给

2006 年 1 月，广州海珠一名雇主在“广州家政服务网”发帖，给出长期聘用、包食宿、独立房间等条件；大半个月后仍没有找到人，并且线下三家家政公司也无人可派。

同期报道还说网站首页存在大量“急找保姆”信息，许多没有解决。

Source:
- 信息时报/新浪，2006-01-24：https://news.sina.com.cn/c/2006-01-24/11378068776s.shtml

Evidence grade: **B，同期报道。**

### 5.1 这个案例支持什么

```text
Web requirement publication existed
+ household could publicly specify terms
+ site visibility did not create worker supply
```

### 5.2 不能支持什么

- 不能从“首页大量急聘”推导平台注册量；
- 不能把“未请到”自动归因于网站不好用；
- 同期最明显的外部变量是春节返乡和供给收缩；
- 不能确认每条帖子都是活跃、真实、未过期。

### 新增 gap：`listing-status staleness gap`

旧 archive 即便留下帖子，也可能无法知道：

```text
still open?
filled?
expired?
poster stopped looking?
contact moved offline?
```

---

## 6. 2007 北京：网站更像热线目录，而不是“一键家政”

2007 年北京家政服务协会、北京市社区服务中心联合开通 134 条求职热线，主要面向本地失业人员进入家政业。

同期给出 historical hosts：

```text
www.jiazhengbj.org
www.bjcs.gov.cn
```

用户被告知可先登录两个网站查询热线号码，再通过电话求职。

Sources:
- 北京晨报/新浪，2007-01-01：https://news.sina.com.cn/c/2007-01-01/023510905731s.shtml
- 北京日报/新浪，2006-12-30：https://news.sina.com.cn/s/2006-12-30/064010895476s.shtml

Evidence grade: **B，同期媒体，historical host + described Web→phone workflow。**

### 6.1 可复原的最小 workflow

```text
website
→ hotline list
→ phone call
→ local domestic-service organization
→ screening / job information
→ offline placement
```

所以这里应明确标记：

> **Web directory / telephone transaction handoff**

而不是 `online job placement`。

### 6.2 2009 `bjcs.gov.cn` 仍体现多渠道并存

2009 年北京 96156 已提供：

- 电话咨询；
- 网站查询 `www.bjcs.gov.cn`；
- 短信；
- email。

Source:
- 新京报/新浪，2009-09-01：https://news.sina.com.cn/c/2009-09-01/051016217455s.shtml

Evidence grade: **B。**

这说明中文旧 Web 的一个长期形态是：

```text
site as one addressable layer among phone/SMS/email/counter
```

不能把 browser 看成唯一入口。

---

## 7. 2006 “电子保姆”：trust interface 可能是监控而不是评价

2006 年上海一家家政公司在自己网站宣传所谓“电子保姆”服务：

- 雇主家安装摄像头；
- 手机上查看视频；
- 异常报警；
- 历史视频存储。

Source:
- 中国新闻网/新浪，2006-01-14：https://news.sina.com.cn/o/2006-01-14/09437980806s.shtml

Evidence grade: **B，同期报道，证明服务宣传和争议存在。**

### 对旧网考古的意义

早期“信任技术”不能只追：

- 评分；
- 星级；
- 实名认证。

还需要追：

- 视频监控；
- 摄像头安装说明；
- 手机客户端/网页查看；
- 存储期限；
- 告知和同意；
- 谁能看录像。

### 新增 gap：`trust/surveillance substitution gap`

页面宣传“放心”，实际技术机制可能是把劳动者置于持续监控，而不是建立更平衡的 trust relation。

本轮没有取得该公司原网站 capture，因此：

- 摄像头型号；
- 手机视频协议；
- Web/客户端架构；
- 登录鉴权；
- 视频保存位置；

均为 `unknown`。

---

## 8. 2008：网站之外的春节供给告诉我们“在线库存”为什么特别危险

2008 春节前多地家政供给因返乡显著波动；同期报道反复出现：

- 雇主提前找替工；
- 工人已买返乡车票；
- 短期单价格上涨；
- 住家工和钟点工供给结构不同。

Sources:
- 扬子晚报/新浪，2008-01-18：https://news.sina.com.cn/s/2008-01-18/085113283335s.shtml
- 南方都市报/新浪，2008-01-16：https://news.sina.com.cn/c/2008-01-16/040313266916s.shtml

Evidence grade: **B。**

### 保存时应新增字段

```text
listing_date
requested_start_date
requested_end_date
live_in / hourly / temporary
holiday_context
worker_current_city
worker_return-home-plan   # usually unknown
```

否则一个 1 月份的“1000 名阿姨”页面与 3 月份的同一个数字不能被当成同样含义。

---

## 9. 2008–2010：劳动者供给页不能只从雇主视角解释

### 9.1 2008 金融危机：列表背后可能是正在决定“留城还是回乡”的人

2008 年底上海家政市场需求收缩，一名从安徽来的求职者到上海后发现老乡还没找到落脚处，在家政点等待工作，并犹豫继续留城还是回农村。

Source:
- 劳动报/新浪城市，2008-12-08：https://vic.sina.com.cn/20081208/10588436.shtml

Evidence grade: **B，同期现场 + 第一人称。**

这提醒旧网研究者：

> 一个“available worker”不是数据库里静止的一行数据，而是可能明天就离开城市的人。

### 9.2 2010 宜昌：profile 逐渐绑定 credential stack

湖北日报记录宜昌工友家政体系：

- 家政网站定期发布供需；
- 外地公司、客户、家政工可网络视频直接交流；
- 报名时要身份证、无犯罪记录证明；
- 家属签字；
- 统一体检/健康证；
- 培训、理论与操作考试；
- 资格证书；
- 再向京沪粤推荐。

Source:
- 湖北日报/新浪，2010-04-06：https://news.sina.com.cn/o/2010-04-06/055017327959s.shtml

Evidence grade: **B，同期机构运作报道。**

### 可能的 Web state model

```text
training applicant
→ identity checked offline
→ health checked offline
→ exam passed
→ credential issued
→ worker enters website supply pool
→ remote company/client sees worker
→ video interview
→ employment/placement agreement
→ worker travels to destination city
→ final household match
```

注意：媒体能证明这类流程被实际描述，不能证明网站内部真的有每个字段的结构化 database。

---

## 10. 2011–2015：从“信息撮合”向平台化过渡，但不要倒推今天的交易模型

2010s 初，家政网站、分类信息平台、社区服务网、公司官网越来越多；2014 年以后又出现更移动化的到家服务平台。

但对 2005–2015 的研究，必须避免拿今天的产品页倒灌：

```text
current app has:
profile + order + payment + rating

therefore 2008 site had same stack
```

这是错误推断。

旧 Web 里至少存在几种不同架构：

### A. Web directory → phone

例：2007 北京热线目录。

### B. listing board → direct/offline contact

例：2005/2006 招聘、求职帖子。

### C. intermediary-operated chat/video

例：2006 杭州 QQ。

### D. credential/training organization → Web/video → cross-city placement

例：2010 宜昌。

### E. classified platform → company/worker contact

后期分类信息网站逐渐承载大量家政广告，但仍可能在电话后完全离开平台。

### F. later app/platform order flow

接近 2014–2015 才逐渐出现更完整的下单、派单、评价、支付与售后模式；必须逐站验证，不做整行业推断。

---

## 11. 一个推荐的 transaction state machine

今后发现具体家政站点/capture 时，至少按以下链记录：

```text
landing page
→ category selection
→ household or worker role selected
→ account/identity state
→ requirement/profile form
→ photo/document upload
→ listing/profile publication
→ search/filter/recommendation
→ profile view
→ contact reveal / message / QQ / phone
→ intermediary intervention
→ interview/video
→ identity/health/skill verification
→ salary/time/rest negotiation
→ booking / placement request
→ mutual acceptance
→ physical travel
→ household entry
→ trial work
→ continuing service
→ payment
→ rating/complaint
→ termination/replacement
```

不是每个平台都有全部状态。

对每个 capture 应标：

```text
observed state
inferred next state
unknown private state
```

---

## 12. 重点 state gaps

### 12.1 `listing-to-live-supply gap`

帖子存在不代表劳动者/岗位还可用。

### 12.2 `profile-to-person gap`

网页上的姓名、年龄、技能、照片可能：

- 由本人填写；
- 由中介代填；
- 已过期；
- 经过营销改写。

### 12.3 `interface-user attribution gap`

真正使用网页/QQ 的可能不是 profile 对应劳动者本人。

### 12.4 `contact-to-interview gap`

看到电话/QQ 不代表联系成功。

### 12.5 `interview-to-mutual-acceptance gap`

家政是双向选择，雇主可以拒绝，劳动者也可以拒绝。

### 12.6 `acceptance-to-household-entry gap`

还要经过：

- 交通；
- 搬迁；
- 门禁；
- 实际开始日期；
- 可能的临时反悔。

### 12.7 `entry-to-continuity gap`

试工一天不等于稳定服务半年。

### 12.8 `advertised-inventory-to-deployable-inventory gap`

公司宣传的阿姨总量与某天能派给某户家庭的人数不同。

### 12.9 `credential-to-current-trust gap`

证件可见不等于适配、服务质量或劳动关系已经验证。

### 12.10 `platform-to-employer gap`

平台/中介未必是劳动者法律意义上的雇主。

### 12.11 `online-to-offline-payment gap`

老站即使在网页找到人，工资很可能直接由家庭现金/转账支付，平台没有 settlement record。

### 12.12 `holiday-calendar gap`

春节前后的“可用人力”会因返乡行为突然变化；snapshot datetime 对解释特别重要。

---

## 13. Archive 最容易保存什么，最难保存什么

### 容易保存

- 首页；
- 分类目录；
- 工资行情；
- 服务介绍；
- 招聘标题；
- 部分公开 profile；
- 培训公告；
- 热线列表；
- 公司宣传语；
- “在线选保姆”“视频招聘”按钮；
- FAQ。

### 难保存

- 登录后候选列表；
- QQ 对话；
- 电话通话；
- 中介人员口头转述；
- 身份证/健康证后台；
- 当前真实库存；
- 谁已经在别人家上工；
- 工人春节返乡计划；
- 面试后拒绝原因；
- 工资议价；
- 试工；
- 雇主住宅入户；
- 现金工资；
- 私下解约；
- 家庭满意/不满意但未公开投诉；
- 劳动者自己家庭的照护代价。

因此这里存在强烈的：

## **public-listing / private-household-state asymmetry**

archive 最容易留下“我要找人”和“我想找工作”，最难留下真正决定生活的“她最后来了没有、做了多久、为什么走”。

---

## 14. 额外保存偏差

### 14.1 successful-placement bias

家政公司和媒体更爱发布：

- “金牌月嫂”；
- 高薪；
- 成功就业；
- 好雇主/好阿姨故事。

大量没配成、试工失败、做三天离职的情况更少留下网页。

### 14.2 employer-view bias

家政页面通常面向付费家庭，容易把劳动者压成：

```text
age / hometown / skill / wage / photo
```

但劳动者自己的：

- 孩子；
- 老人；
- 春节；
- 住房；
- 城市迁移；
- 社保；

往往不在 profile 中。

### 14.3 worker-self-selection invisibility

劳动者拒绝某个家庭通常不会留下“拒单日志”在公开 Web 上。

### 14.4 seasonal snapshot bias

春节前采样与节后采样会得到完全不同的供需图。

### 14.5 proxy-digitality bias

一个看起来“在线”的劳动者可能只是被中介数字化表示。

### 14.6 trust-technology bias

现代研究者看到“实名/视频/监控”容易把它解释成信任提升；实际上也可能代表更强的劳动监控。

### 14.7 stale-profile survivorship

长期被 archive 保存的 profile 可能恰好是已经失效但未删除的页面，而活跃动态列表反而没抓到。

---

## 15. Browser / encoding / technical questions

一旦取得 2005–2010 capture，应重点记录：

- GB2312 / GBK / UTF-8；
- table layout；
- frameset；
- ASP / JSP / PHP 动态路径；
- form method / action；
- GET search query；
- page number / sorting；
- session cookie；
- login requirement；
- phone number 是否直接在 HTML；
- QQ 号是否通过图片/JS/点击显示；
- profile photo 子资源；
- ActiveX / Java / Flash；
- “视频面试”是否调用 QQ 外部客户端；
- 是否使用 `tencent://` 一类 URI；
- 是否依赖 IE-only 控件；
- 上传身份证/健康证是否在公开 Internet front end；
- 是否有 robots/login 导致 archive 只能看壳。

特别是 2006 “QQ 视频找保姆”不能假定视频发生在网站 DOM 内。

---

## 16. Historical locator ledger

### 已有 B 级 historical locators

#### `www.jiazhengbj.org`

2006-12 / 2007-01 同期报道明确称“北京家政网”，用于查询 134 条家政求职热线。

Evidence family:
- https://news.sina.com.cn/c/2007-01-01/023510905731s.shtml
- https://news.sina.com.cn/s/2006-12-30/064010895476s.shtml

Status:
- **historical host confirmed by contemporary secondary sources**
- **no verified archive capture this run**

#### `www.bjcs.gov.cn`

同期称“北京市社区服务信息网”，用于查询家政热线；2009 年还作为 96156 多渠道服务中的网站入口。

Evidence family:
- https://news.sina.com.cn/c/2007-01-01/023510905731s.shtml
- https://news.sina.com.cn/c/2009-09-01/051016217455s.shtml

Status:
- **historical host confirmed**
- **no verified M1 capture this run**

### 未解析 host 的对象

- 2005 “中国家政服务网”；
- 2006 “广州家政服务网”；
- 2006 杭州提供 QQ/视频找保姆的家政市场/介绍所站点；
- 2010 宜昌工友家政服务网站。

目前只能保留媒体中的对象名和 workflow 描述，不能猜域名。

---

## 17. 本轮 archive 尝试与负结果

本轮针对：

- `www.jiazhengbj.org`
- `www.bjcs.gov.cn`

尝试搜索 Internet Archive / Wayback locator。

结果：

- 普通搜索没有返回可直接验证的 historical memento；
- 尝试直接打开 CDX 查询 URL 时，当前 Web 工具因 URL 安全/重写限制未能实际取得 CDX 响应；
- 因此没有获得可检查 response body、headers、DOM、charset、form action、cookie/session 和子资源的 capture。

按照 `docs/METHOD.md`：

> **candidate locator / archive search attempt ≠ verified capture**

所以本轮明确记录：

```text
M1 verified transaction capture = NOT ACHIEVED
```

这不等于：

```text
Wayback has no copies
```

也不等于：

```text
site did not exist
```

后续可用 Internet Archive 官方界面、CDX API 的可控环境、Common Crawl index 或 Webrecorder 工具继续查。

---

## 18. 已证实 / 高概率 / 不知道

### 已证实

1. 2005 同期媒体记录中文 Web 上已有个人发帖寻找特定类型家政人员；
2. 2006 广州家庭确实用家政网站发布找保姆需求，但大半个月未找到；
3. 2006 杭州至少一个“QQ/视频找保姆”服务由中介人员替家政工进行数字交互；
4. 2006 上海至少有家政公司在网站宣传手机视频监控型“电子保姆”；
5. 2007 `www.jiazhengbj.org` 与 `www.bjcs.gov.cn` 被同期媒体明确用作热线查询入口；
6. 2010 宜昌家政体系被同期媒体描述为网站发布供需 + 网络视频 + 线下身份/健康/培训认证 + 跨城输送。

### 高概率但需要 capture 验证

1. 这些站点至少部分使用传统动态 Web 技术和表单/查询；
2. 电话/QQ/email 是重要的 off-platform handoff；
3. 早期家政 profile/招聘页大量使用 GB2312/GBK 和 table layout；
4. 部分页面可能仅在 IE-era 环境完整工作。

这些都不能在取得原 capture 前写成事实。

### 不知道

1. 2005 “中国家政服务网”准确历史域名和技术栈；
2. 2006 “广州家政服务网”准确 URL；
3. 2006 杭州 QQ 服务是网站内入口、QQ 客户端还是人工电脑端；
4. 2007 两个北京 host 的历史 DOM/charset；
5. 招聘表单 GET/POST；
6. 是否存在登录账号；
7. 是否支持 profile 更新/删除；
8. 是否有“已上岗/已成交”状态；
9. 真实 conversion rate；
10. 2010 视频匹配是否由网站内嵌视频、QQ 或其他客户端完成；
11. 身份证/健康证等是否以结构化字段进入 Web backend；
12. 2011–2015 分类平台上的家政广告何时开始形成完整订单状态。

---

## 19. 隐私与版权边界

家政页面可能含有高度个人化内容：

- 姓名；
- 照片；
- 手机；
- QQ；
- 籍贯；
- 年龄；
- 身份证；
- 健康信息；
- 雇主家庭地址；
- 婴儿/老人病情；
- 住家条件。

后续取得 archive capture 时：

- 优先保存 URL pattern、字段结构、截图局部或 metadata；
- 不重新批量公开普通劳动者手机号、身份证和家庭地址；
- 不因为旧页面公开过就复制整个人员数据库；
- 做 transaction archaeology 时应优先选机构/帮助页或已经匿名化的页面。

---

## 20. 与海外比较时该比较什么

全球前史主要留在 `how-people-lived`，本仓只保留有助于界定中文 Web 的方法结论。

1988 法国 Minitel 已能让临时工和用工企业按行业、地区筛选劳务机构；美国 1990s 也存在报纸 + 中介的跨地区家庭照护匹配；2001 以后又出现 Sittercity 一类在线照护市场。

这些对象说明：

> **Web 的共同机制是扩大陌生人劳务的可搜索性和可联系性，而不是第一次创造陌生家庭服务。**

对中文旧网真正值得比的是：

- profile 由谁创建；
- 联系方式是否公开；
- background/health/skill 如何验证；
- 中介是否仍居中；
- 是否保留电话；
- transaction 是否离站；
- 谁承担实际雇佣责任。

---

## 21. 下一步 M1 research plan

优先顺序：

### A. `www.jiazhengbj.org`, 2006–2009

找：

- 首页；
- 热线列表；
- 招聘/求职栏目；
- 页脚主体；
- charset；
- 是否有表单；
- 联系方式结构。

### B. `www.bjcs.gov.cn`, 2006–2010

找：

- 96156 服务入口；
- 社区家政/养老服务目录；
- 是否存在 district 子站；
- 站内查询；
- Web→phone handoff。

### C. 解析 2006 “广州家政服务网” host

从同期转载、搜索结果、ICP备案线索、新闻正文引用路径寻找原域名，不猜。

### D. 解析 2005 “中国家政服务网” host

目标是定位一个不涉及个人敏感资料的栏目/帮助页。

### E. 2010 宜昌工友家政

找同年工会、培训基地、家政网站的官方 URL 或缓存引用，核验“网络视频”真正使用什么协议/客户端。

### M1 最低成功标准

至少取得一个 2005–2010 页面：

- actual memento opened；
- original URL 明确；
- Memento-Datetime 明确；
- response body 可检查；
- charset 可判断；
- 主文档/子资源状态记录；
- 不涉及不应重新公开的个人敏感内容。

若仍然只有新闻 locator，就保持 research note，不升级为完整 case。

---

## 22. 本轮最重要的旧网结论

如果只看 surviving page，很容易得到：

```text
2006: 家政已经“网上找人”
```

但同时代 evidence 迫使我们把它拆开：

```text
Web 上能写“我要找人”
≠ 有人可用

Web 上能看到“阿姨”
≠ 阿姨本人会用电脑

QQ/视频能沟通
≠ 双方不需要中介

profile 能展示
≠ 身份和技能已经核验

宣传有很多人
≠ 某天能派给某户家庭

线上匹配完成
≠ 人已经走进住宅

人走进住宅
≠ 这段照护能够持续
```

因此家政网站特别适合作为中文旧 Web 的一个考古对象：

> **它把非常私人、非常身体化、非常依赖信任的一段家庭劳动放到公开信息层上，却又把最关键的结果留在电话、QQ、中介柜台、火车、住宅门口和家庭内部。archive 保存的是“可见的供需壳”，真正决定普通人生活有没有被接住的 household state，恰恰是最容易消失的部分。**
