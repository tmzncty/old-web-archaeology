# EXAM_RESULT_VOICE_HOTLINE_WEB_QUERY_SMS_AND_OFFICIAL_NOTIFICATION_STATE_GAPS_1997_2015

## Scope

本说明研究约 **1997–2015 中文互联网及其与电话声讯系统的交界**中一个此前没有单独建模的对象：

> **高考、中考、自考、录取等高 stakes result 怎样从机构后台，通过 160/168/960xx 声讯、短信、Web 查询页、学校/招办和纸质通知到达个人；以及“网页能查”“电话能打”“页面显示一个结果”分别能证明什么、不能证明什么。**

主研究对象仍是中文旧网的平台技术、页面/表单、浏览器和 archive gap。

1997 之前的 168 前史只作为边界说明；2015 以后 App/微信/推送的长期变化写入生活史 companion：

- `tmzncty/how-people-lived/topics/from-paid-voice-results-to-web-and-push-information-latency-life-course-interfaces-china-1994-2026.zh-CN.md`

海外 Minitel 比较也主要留在 `how-people-lived`，不把本仓扩成全球 telematics 史。

---

# 1. 研究单位：不要把“成绩公布”当成一个单一 state

至少区分：

1. **scoring complete**：阅卷/审核是否结束；
2. **institutional result record**：机构数据库里是否已有个人成绩/录取状态；
3. **release policy**：机构规定何时公开、向谁公开；
4. **channel dataset loaded**：168/网站/短信后台是否已装载正确数据；
5. **channel open**：电话信箱、网页查询入口是否在当前时刻开放；
6. **front-end reachable**：用户是否能接通电话/加载页面；
7. **authentication executable**：准考证号、身份证后位、查询卡等是否能输入并通过；
8. **query response**：语音/页面是否返回一个值；
9. **display authority**：该值是参考信息还是正式行政状态；
10. **review state**：是否申请复核、复核是否改变结果；
11. **paper / official notification**：成绩单、录取通知书等是否送达；
12. **downstream action**：填志愿、补填、报到等下一状态是否完成。

核心规则：

```text
result exists
≠ result is released
≠ hotline/web backend has correct data
≠ channel is open
≠ user reaches channel
≠ authentication succeeds
≠ page/voice returns a result
≠ result is legally/administratively final
≠ admission/registration is complete
```

因此旧网页上出现“点击查分”按钮，不能直接写成：

> 当时考生已经能够成功查到自己的成绩。

---

# 2. 1990s 边界：Web 不是第一种交互式公共数据库入口

浙江地方志的当前 basic-HTML 版本记录：舟山 1994 年开通自动 168 信息服务台，1997 年该 168 开始提供高考成绩查询，1998 年又开通与全省联网并与 168 相连的 160 人工信息台。

Source:
- 《舟山市志（1989—2005）》上卷，current institutional HTML representation, Page 571：
  https://dfz.zj.gov.cn/zlyz/ossfs/h5/ZS-Z-330900-2005-001-0301/files/basic-html/page571.html

Evidence grade: **B/A-adjacent institutional retrospective compilation**。

### 能证明什么

可以证明：

- 在当地，面向公众的自动电话信息服务早于大众 Web；
- 1997 年高考成绩已经可以成为电话数据库服务的一种内容；
- 168/160 后来扩展到多种生活事务信息。

### 不能证明什么

不能据此复原：

- 1997 年 IVR 的完整提示音；
- DTMF 输入字段；
- 后台数据库 schema；
- 呼叫路由和线路容量；
- 收费规则；
- 哪些家庭真正使用；
- 1997 年所有省份都有相同服务。

### 对本仓 scope 的意义

它只用于说明中文 Web 出现时已经面对一套既有电话信息系统。

不要把 `old-web-archaeology` 改成 1990s 电话网考古仓库。

---

# 3. Web 出现以后不是“替换”，而是 query channels 叠加

## 3.1 四川 2002：网上查询本身可能依赖实体售卡

同期报道记录：四川 2002 年高考查询同时有短信、语音热线和网上查询；网上查询需要先到电信营业厅购买面额 30 元的高考查询卡，再到指定网站输入卡账号/密码。

Source:
- 四川在线，《四川省24日起查高考分 移动电信开通查询“通道”》，2002-07-22：
  https://news.sohu.com/09/70/news202247009.shtml

Evidence grade: **B — 同期媒体。**

这构成一个重要状态链：

```text
Web query advertised
→ user learns physical card requirement
→ travels to telecom storefront
→ pays for query card
→ obtains credentials
→ reaches an Internet terminal
→ loads designated site
→ submits card account/password + candidate data
→ backend accepts/rejects
→ result returned
```

因此新增：

**web-to-offline-credential procurement gap — Web / 线下凭证获取缺口。**

`query page exists` 并不等于 `user can execute query from home with only a browser`。

## 3.2 辽宁 2003：语音、短信、Internet 与行政下发同时存在

2003 年辽宁省招考办的同期说明列出：固定/移动电话语音信箱、短信订制和 Internet 网站三类公开渠道；同时成绩还通过“正常行政渠道逐级下发”。

Source:
- 中国教育在线，《辽宁6月29日零时起可查2003年高考分数》，2003-06-25：
  https://gaokao.eol.cn/news/200603/t20060323_77156.shtml

Evidence grade: **B — 同期招生信息转述。**

因此建议在所有查分 case 中显式记录：

```yaml
channels:
  voice: unknown/known
  sms: unknown/known
  web: unknown/known
  school_or_exam_office: unknown/known
  paper_mail: unknown/known
```

不能看到一个网页以后把其他现实通道从历史里删掉。

---

# 4. 2002 广东测试数据事故：channel response ≠ valid result

2002 年广东出现一条对旧网 state modeling 特别重要的同期报道：高考查分热线尚未正式开放，电信部门调试时挂上往年录取数据作为测试；有考生提前拨打后，系统语音错误地告诉她被一所自己根本没报考的高校录取。负责人随后说明，正式开放以后信息才是真实信息。

Source:
- 中国教育在线，《广东高考查分热线“96040”正式开通才能查分》，2002-07-22：
  https://gaokao.eol.cn/news/200603/t20060323_56363.shtml

Evidence grade: **B — 同期媒体。**

这是一个非常强的反例：

```text
number reachable
+ system prompts work
+ candidate credentials accepted
+ voice returns a university name
```

仍然不能推出：

```text
valid 2002 admission result delivered
```

新增：

**test-data / production-result gap — 测试数据 / 正式结果缺口。**

它同样适用于 Web：即使 archive 能重放一个查询页面或得到 HTTP 200，也不能默认后台数据是当时 production state。

---

# 5. 2004 湖北：同一天里 online result、EMS 与纸质成绩单是不同对象

2004 年湖北同期报道说，考生可登录两个网站或通过 168 查高考成绩；申请 EMS 的考生由速递局寄送；纸质成绩单则向各市州县招考办发放。

Source:
- 《楚天金报》/新浪教育，《湖北省高考评卷结束 今日下午可查成绩》，2004-06-25：
  https://edu.sina.com.cn/l/2004-06-25/73908.html

Evidence grade: **B — 同期媒体。**

因此 archive 研究至少要拆：

```text
web display
≠ voice playback
≠ EMS item
≠ local exam-office paper record
≠ later review result
```

网页只能保存其中一个 surface。

新增：

**online-result / paper-notice divergence — 在线结果 / 纸质通知差异。**

---

# 6. 2006：渠道的“收费属性”会变，不能把号码本身当属性

湖北 2006 年停止 168 收费查询高考成绩，改由成绩信息单和两个网站第一时间免费提供；河北同年保留 168 但免收信息费，并保留网站与正式渠道；山东也把 168、Web 和成绩单设为免费查询。

Sources:
- 新华网/新浪，《湖北停止使用168声讯台收费查询高考成绩》，2006-04-02：
  https://news.sina.com.cn/e/2006-04-02/16108593731s.shtml
- 学信网，《河北：2006年高考成绩查询168不再收信息费》，2006-06-15：
  https://gaokao.chsi.com.cn/gkxx/heb/200606/20060615/513197.html
- 青岛新闻网/新浪，《山东高考成绩25日前公布 3种方式查询全部免费》，2006-06-14：
  https://news.sina.com.cn/c/2006-06-14/14159202969s.shtml

Evidence grade: **A/B institutional-media chain.**

### 规则

不要建立：

```text
168 => paid
```

而应建立：

```text
(number/service, region, exam, date, carrier, tariff state)
```

同一个 service family 的收费状态会随地区和年份变化。

新增：

**number-to-tariff temporal gap — 号码 / 资费时态缺口。**

旧页面上保存一个 `168xxxxx` 号码，不足以从今天的资费或另一个省的资费推断当年实际费用。

---

# 7. 2007 第一人称：query success 还受线路容量与家庭并行拨号影响

中国青年报 2007 年采访南京考生计璐：她连续拨 168 三次，前两次进入系统但没有得到成绩也已经计费，第三次成功；报道同时说，高峰期线路忙，亲戚朋友会一起拨打。

Source:
- 中国青年报，《部分省市仍继续高考查分收费》，2007-08-20：
  https://news.sina.com.cn/c/2007-08-20/034913698832.shtml

Evidence grade: **B + 同时代第一人称。**

这给 old-web/state archaeology 增加两层：

### 7.1 hotline-connected / result-delivered gap

```text
call connected
≠ candidate result reached
```

如果 archive 只保存资费说明或一个查询号码，它看不到忙音、排队、错误输入、系统中途退出。

### 7.2 public release / household access path gap

现实可能是：

```text
candidate + parents + relatives
→ multiple telephones dial same service
→ one succeeds first
→ result spreads inside household by voice
```

最终知道成绩的人不一定是完成查询的人。

这类家庭内传递几乎不会进入 Web archive。

---

# 8. 2008 上海：168 可以成为 write path，不只是 read path

## 8.1 成人高考：声讯可以补填志愿

上海大学继续教育学院的现存页面标注创建时间 2008-11-18，说明：考生可拨 168 声讯查询录取情况；符合条件者可以通过声讯电话补填志愿；正式录取通知书稍后邮寄。

Source:
- 上海大学继续教育学院，《2008年上海大学成人高考招生录取本科/专升本分数线》：
  https://cce.shu.edu.cn/info/1464/9274.htm

Evidence grade: **A for historical-dated institutional content; current page is not treated as a verified 2008 capture.**

这意味着：

```text
IVR read result
```

和

```text
IVR write preference into admission transaction
```

必须分开。

新增：

**voice-read / voice-write gap — 声讯读 / 写事务缺口。**

## 8.2 普通招生：Web 与声讯并行填额外专业志愿

2008 年上海大学招生政策的同期汇编说明，报考者可选择声讯电话或 Web 填报更多专业志愿。

Source:
- 学信网，《必看：2008年上海各校高考优惠招生政策盘点》，2008-04-29：
  https://gaokao.chsi.com.cn/gkxx/ss/200804/20080429/6140857.html

Evidence grade: **B — 同期招生政策汇编。**

因此某个历史 Web form 不是唯一 transaction surface；即使它完全丢失，也不代表当年的提交能力完全不可恢复研究，可以通过官方说明和并行电话流程建立窄 claim。

---

# 9. 2009 上海：page live ≠ backend usable，尤其在同步发布高峰

2009 年上海中考 18:30 起网站与 168 同时开放；同期记者在 16:30 已感到网站变慢，开放前后明显拥堵。168 不收信息服务费。

Source:
- China Daily，《09上海中考昨起开始查分 分数普遍高于学生预估》，2009-07-07：
  https://www.chinadaily.com.cn/china/2009-07/07/content_8392576.htm

Evidence grade: **B — 同期媒体。**

这要求增加：

**page-live / query-backend-capacity gap — 页面存在 / 查询后端容量缺口。**

一个历史首页可能：

- HTML 能加载；
- 登录表单能显示；
- 静态说明页正常；

但真正查询 POST/API 已因峰值容量不可用。

Archive 往往恰好更容易保存静态 shell，而不是峰值时的 backend behavior。

---

# 10. 2009 大连：服务本身也可能有严格时窗

大连 2009 年中考查分声讯自动信箱只在 7 月 15 日 6:30–8:00 开放，90 分钟后自动关闭；纸质成绩单在当天稍晚凭证件到指定地点领取。

Source:
- 半岛晨报/新浪教育，《辽宁省15日早6点半开始查询09年中考成绩》，2009-07-14：
  https://edu.sina.com.cn/zhongkao/2009-07-14/1443209902.shtml

Evidence grade: **B — 同期媒体。**

新增：

**service-window / stored-data gap — 服务时窗 / 数据存在缺口。**

后台有数据，不代表号码任何时刻都开放。

对于 Web archaeology，同样不要看到一个查询 URL 后默认它是长期 always-on endpoint。

---

# 11. 2009 全国渠道矩阵：地区差异必须进入数据模型

湖南省教育厅当前保留一篇标注 2009-06-18 的全国高考查分方式汇总，地区组合包括：

- 考试院/教育网；
- 县区招办；
- 纸质成绩单；
- 短信；
- 168 声讯；
- 118114 等电话服务；
- 不同地区的免费/收费差异。

Source:
- 湖南省教育厅，《2009年高考全国各地成绩查询时间及查询方式汇总》：
  https://jyt.hunan.gov.cn/sjyt/xxgk/gzdt/tpxw/201701/t20170121_3954970.html

Evidence grade: **A/B institutional current page carrying a contemporaneous-dated compilation.**

### 规则

不要写：

> “2009 中国高考通过 X 查询。”

应写：

```text
province/city + exam + year + channel
```

新增：

**national-label / regional-channel gap — 全国标签 / 地区渠道缺口。**

---

# 12. 2010 自考：成熟 Web 旁边仍可以有昂贵声讯和短信

2010 年 1 月自学考试成绩查询汇总显示，北京已经有考试院 Web 查询，同时仍可自愿使用固定电话声讯（信息费 3 元/分钟）、移动声讯和收费短信；天津也保留网站、收费热线与短信等渠道。

Source:
- 自考365，《2010年1月高等教育自学考试成绩查询》，2010-04-30：
  https://www.zikao365.com/new/1_41/2010_4_30_li6078954903401023438.shtml

Evidence grade: **B — 同期教育服务汇编，不是考试院原始页面。**

这说明旧 Web 研究中：

> **某一 transaction 已经有 Web 入口，并不证明并行收费电话已经退出。**

也不能反过来从电话继续存在推断 Web 使用不重要。

---

# 13. Query result 的 authority 需要单独编码

中国材料常同时存在：

```text
电话/网站即时显示
→ 纸质成绩单
→ 成绩复核
→ 录取状态
→ 正式录取通知书
```

河北 2006 年明确称，高考录取结果仍以院校录取通知书为准；上海大学 2008 年也把声讯查询和稍后寄出的书面录取通知分开。

Source:
- 学信网，《河北：2006年高考成绩查询168不再收信息费》：
  https://gaokao.chsi.com.cn/gkxx/heb/200606/20060615/513197.html
- 上海大学继续教育学院 2008 页面：
  https://cce.shu.edu.cn/info/1464/9274.htm

因此新增：

**displayed-result / authoritative-notice gap — 显示结果 / 权威通知缺口。**

建议 evidence schema 将：

```yaml
result_surface:
result_authority:
review_available:
official_notice_medium:
```

拆开，而不是一个 `result=true`。

---

# 14. Old-Web 页面尤其容易造成“查询服务仍存在”的假象

当前仍在线的历史日期页面可能保留：

- “点击查询”；
- 查询电话号码；
- 当年开放时间；
- 一个表单 shell；
- 一张查询卡说明；
- JavaScript 校验；
- 当年的 FAQ。

但真正完成 transaction 还可能需要已经消失的：

- CGI/ASP/JSP backend；
- 数据库连接；
- 运营商 IVR；
- SMS gateway；
- 查询卡认证数据库；
- 省招考后台接口；
- session/cookie；
- 动态验证码；
- 高峰时线路/服务器容量。

因此固定：

```text
historic instructions survive
≠ historic interactive service survives
```

新增：

**instruction-page / transaction-backend survival gap — 说明页 / 事务后端存活缺口。**

---

# 15. Archive 特有的几个状态缺口

## 15.1 result-exists / channel-open gap

机构已经生成结果，但查询渠道尚未到规定开放时间。

## 15.2 channel-open / access-success gap

渠道开放，但电话忙音、Web 拥堵、终端或凭证条件使个人没有成功接入。

## 15.3 hotline-connected / result-delivered gap

电话接通并开始计费，不代表已经听到自己的成绩。

## 15.4 web-page-live / query-backend-live gap

静态页面能加载，不代表动态查询后端工作。

## 15.5 authentication-form / authentication-service gap

能看到准考证号/身份证输入框，不代表历史认证数据库能回放。

## 15.6 test-data / production-result gap

2002 广东热线事故证明，一个技术上工作的查询服务可能仍装载错误/测试数据。

## 15.7 displayed-result / official-notice gap

即时显示或语音结果和正式成绩单/录取通知书不是同一 artifact。

## 15.8 score / admission gap

成绩查询成功不等于录取状态已形成。

## 15.9 query-time / publication-time gap

页面文章发布日期、查询开放日期、本人实际查询时间是三只钟。

## 15.10 number-to-tariff temporal gap

168/160/960xx 号码本身不能证明某年某地的收费状态。

## 15.11 public-thread-or-news / private-result gap

媒体和论坛可以保存“大家今晚查分”的公共事件，但个人分数本身通常是私有数据，不应因考古重新公开。

## 15.12 billing-trail / content-trail asymmetry

电信系统可能留下通话计费记录，却未留下用户当时听到的完整 IVR 内容；Web archive 则可能保存说明页，却不保存运营商计费链。

---

# 16. Browser / encoding / terminal assumptions

本轮没有历史 capture，因此以下全部保持 `unknown`，不得由今天页面反推：

- 2002–2009 查询站点真实 Content-Type / charset；
- 是否 GB2312/GBK；
- IE-only、ActiveX、Java、Flash 是否参与；
- form method/action；
- client-side JS validation；
- cookie/session；
- query-card credential transport；
- captcha；
- peak-time backend timeout behavior；
- mobile/WAP variant；
- 网吧/家庭 PC/学校机房的具体浏览器环境。

### 特别提醒

一个 2008 页面今天在 Chromium 中可读，只能证明：

> 当前服务器/当前渲染链能把历史日期内容送给现代浏览器。

不能证明：

> 2008 年考生就是以今天看到的 DOM、CSS、导航和账号状态使用它。

---

# 17. Voice archaeology 比 Web archaeology 多丢了什么？

160/168 等系统通常不会自然进入 Wayback。

需要另外寻找：

- 当年电信业务手册；
- 报刊广告；
- 资费表；
- IVR 流程图；
- 软件/交换机厂商手册；
- 用户录音（若来源/隐私/版权允许）；
- 招生机构公告；
- 电信企业年鉴/地方志；
- 同期用户操作说明。

而且必须区分：

```text
number existed
≠ menu path known
≠ result database connected
≠ call succeeded
≠ user heard correct value
```

这是一种 **non-Web transactional dark matter / 非 Web 事务暗物质**：

普通人的很多数字事务已经发生，却很少留下可由网页档案直接回放的 artifact。

---

# 18. 证据等级与 provenance

| 对象 | 证据 | 等级 | 本轮用途 |
|---|---|---:|---|
| 舟山 168 前史 | 地方志 current HTML | B/A-adjacent | 前 Web 电话信息服务边界 |
| 四川 2002 | 同期地方媒体 | B | Web 查询卡、短信/语音/Web 并行 |
| 广东 2002 | 同期媒体 | B | 测试数据/正式结果 gap |
| 辽宁 2003 | 招生信息同期转述 | B | 固话/移动/短信/Web 并行 |
| 湖北 2004 | 同期媒体 | B | Web/168/EMS/纸单并行 |
| 湖北/河北/山东 2006 | 官方/媒体链 | A/B | 资费状态变化，168 不等于收费 |
| 南京 2007 | 中国青年报 + 第一人称 | B | 线路忙、重复拨号、亲友并行 |
| 上海大学 2008 | 当前官方页承载历史日期内容 | A-content / capture unverified | 168 查询 + 补填志愿 |
| 上海 2009 | 同期媒体 | B | Web 高峰拥堵、168 免费并行 |
| 大连 2009 | 同期媒体 | B | 90 分钟 service window |
| 全国 2009 | 省教育厅 current page 承载同期汇编 | A/B | 地区 channel heterogeneity |
| 自考 2010 | 同期教育服务汇编 | B | Web + 有偿声讯/短信继续并存 |

### 重要 provenance 说明

“上海大学 2008 页面现在还在线”和“湖南省教育厅现在还展示 2009 日期内容”不是历史 capture 证明。

本轮只把它们用于：

> **当前 live institutional artifact carries historical-dated content.**

历史 DOM/HTTP/浏览器状态另行验证。

---

# 19. 反例

### 反例 A：Web 不必然免费

四川 2002 网上查分要线下购买查询卡。

### 反例 B：声讯不必然收费

河北/山东 2006 和上海 2009 都有免信息费声讯例子。

### 反例 C：电话服务不只读取数据

上海 2008 的 168 还可以写入志愿。

### 反例 D：HTTP 页面存在不代表 transaction 可用

同步发布高峰可以让真正查询后端拥堵。

### 反例 E：系统返回内容不代表内容有效

广东 2002 调试期间的测试数据造成错误录取结果。

### 反例 F：Web 普及不等于旧声讯马上退出

本 companion 截止 2015；长期生活史 companion 另记录 2023 甘肃仍正式提供电信 16887801 高考查分入口。该事实只作为 post-scope boundary，不把本文件扩到 2020s。

---

# 20. 后见之明风险

## 风险 1：把声讯台写成“Internet 出现前的笨办法”

在家庭 PC 和 Internet 接入并不普通的时期，一部固定电话/公话可能比 Web 更可执行。

## 风险 2：把旧网查分页面写成完整 digitalization

页面可能只是一个 shell；认证、数据、IVR、短信、纸质通知和复核都在页面之外。

## 风险 3：把一个省推广成全国

查询渠道和资费高度地区化。

## 风险 4：把“成绩”与“录取”压成同一状态

两者之间还有志愿、投档、资格线、补填、复核等状态。

## 风险 5：把 current legacy renderer 当历史页面

今天页面上的导航、二维码、统计、移动适配、HTTPS/CDN 都可能是后来层。

---

# 21. M1 状态

## M1 NOT ACHIEVED IN THIS SLICE

本轮**没有取得并实际检查**一份满足仓库 M1 合同的 1997–2010 中文查分网站 verified Wayback/WARC capture。

因此本轮没有验证：

- historical HTTP headers；
- original Content-Type / charset；
- historical DOM/CSS/JS；
- form action；
- query backend；
- query-card auth flow；
- cookie/session；
- server-side error pages；
- busy/timeout response；
- WAP/mobile variant；
- historical subresource survival；
- IVR audio/menu。

正确结论是：

> **本轮尚未获得可按 M1 编目的 capture。**

而不是：

> “Wayback 没有保存。”

搜索结果、今天还能打开的历史日期页面、以及媒体中的旧 URL 都只能先登记为 locator / live legacy artifact。

---

# 22. 下一步具体考古任务

1. 选一个 2002–2006 招考网站，枚举历史 hostname/path/query 变体，再实际打开 archive captures；
2. 优先寻找查询说明页与真正 `form action` 是否分域/分 host；
3. 找四川 2002 查询卡的原始页面、卡面说明或用户教程，验证账号/密码字段和后端；
4. 找上海 2008 `info.shu.*` 志愿页面历史 capture，并和 168 并行流程互证；
5. 找 2009 上海“招考热线”中考查询入口历史 capture，区分静态入口与结果 backend；
6. 搜集 160/168 原始资费和 IVR 技术文档，不能只靠新闻描述；
7. 建 `channel-state` fixture，把 `open/reachable/authenticated/result-delivered/official` 分成独立字段；
8. 对至少一个 case 做现代浏览器 vs IE6 级环境差异验证；
9. 若能拿到历史 query form，严禁用真实普通人的准考证/身份证数据测试；只做无个人信息的页面/协议考古。

---

## Research note

Initial draft prepared with AI assistance. It intentionally preserves the distinction between historical content, current live legacy pages, archive captures, private result data, and reconstructed transaction logic.