# 家政 / 保姆：网站目录、热线、论坛、O2O 与真实上户之间的状态缺口（2005–2015）

## Scope

本文件只研究约 2005–2015 中文 Web 与家政服务现实流程的交界：

- 家政公司网站上的价格、岗位与联系方式；
- Web 作为热线号码目录；
- 论坛里的“求阿姨 / 拼保姆 / 合雇”帖子；
- 实名家政数据库、在线预约、淘宝生活服务、O2O；
- 页面 / 平台记录与真实面试、进门、住家劳动、口碑之间的缺口；
- 这些页面今天为什么很难单独证明一段家庭劳动真正发生过。

1980s–1990s 的中国家政前史主要属于 `how-people-lived`。这里只在解释 Web 出现以前已有妇联、街道、家政公司、熟人介绍和电话网络时作为边界背景，不把本仓 scope 无限前移。

对应生活史专题：

- `tmzncty/how-people-lived/topics/paid-domestic-service-household-as-workplace-care-transfer-and-platform-matching-china-1983-2026.zh-CN.md`

---

## 1. 研究对象不是“一个家政网站”，而是一条跨媒介事务链

一个页面说“有阿姨”“月薪 600–800”“在线预约”，并不能直接推出家庭里已经有人开始工作。

本案例的最小状态链应写成：

```text
household_need_exists
  ↓
listing / directory / forum_post / search_result visible
  ↓
contact channel acquired (phone / PM / QQ / email / form)
  ↓
worker actually available at required time/place
  ↓
identity / health / skill documents presented
  ↓
intermediary registration or platform profile matched
  ↓
offline interview / trial
  ↓
price + scope + live-in/daytime/hourly schedule negotiated
  ↓
contract / service agreement / informal agreement
  ↓
worker can physically reach residential compound / home
  ↓
actual household entry
  ↓
service starts
  ↓
service outcome / trust / conflict / renewal / termination
  ↓
rating / private reputation / referral / next job
```

Web archive 最容易保存的是上半段：网页、列表、价格、介绍、按钮。

最难保存的是下半段：电话、私信、面试、谈价、住家边界、是否真的来了、家庭内发生了什么、为什么离开、后来是不是靠口碑继续接私单。

因此家政是一个很典型的 **browser-visible control plane / household physical data plane** 案例。

---

## 2. 2005：browser-visible price ≠ negotiated price

### 已证实

2005-01-13《北京现代商报》的同期报道记录：记者查看北京多家知名家政公司网站，页面价格栏仍写普通家政服务月薪约 600–800 元；但记者随后拨电话，得到的回答是春节前已经涨价，具体价格由雇主与服务员协商。

来源：

- https://finance.sina.com.cn/roll/20050113/00001289970.shtml

证据等级：**B，同期媒体操作观察**。

### 可以支持的 claim

> 2005 年北京至少存在家政公司把服务价格发布到 Web 的做法；同期报道显示网页标价可能滞后于电话端的实际议价状态。

### 不可以支持的 claim

- “2005 年北京保姆的统一市场价就是 600–800 元”；
- “网站可以直接完成签约”；
- “报道里看到的所有网站今天仍可恢复”；
- “Web 已成为主要找保姆方式”。

### 新增 gap

`browser-visible-price / negotiated-price gap`

一个历史页面即使完整存活，也可能保存的只是更新不及时的参考价格；真正可成交状态存在于电话和线下谈判中。

---

## 3. 2007：Web 可能只是一张热线拓扑图

### 已证实

2007-01-01《北京晨报》报道，北京家政服务协会与北京市社区服务中心开通 134 条求职热线。市民可以登录：

- `www.jiazhengbj.org`
- `www.bjcs.gov.cn`

查询这些热线号码。报道同时称，上一年春节有 2900 多名京籍家政员通过热线找到工作。

来源：

- https://news.sina.com.cn/c/2007-01-01/023510905731s.shtml
- 近同时代独立报道：https://news.sina.com.cn/s/2006-12-30/064010895476s.shtml

证据等级：**B + B，两个同期媒体 family；核心事实高度一致，但仍可能同源于协会信息发布。**

### 最小机制

```text
historical Web page
  ↓
phone-number list
  ↓
134 local/service hotlines
  ↓
voice contact
  ↓
local matching / company / community node
  ↓
worker
```

这不是“网站取代电话”，而是 **Web directory + telephone transaction**。

### 新增 gaps

- `directory-to-telephone-contact gap`
- `telephone-contact-to-candidate gap`
- `candidate-to-offline-interview gap`
- `hotline-listed-to-hotline-operational gap`

### archive 状态

`www.jiazhengbj.org` 与 `www.bjcs.gov.cn` 是由 2006–2007 同期报道明确给出的 historical locator。

本轮**没有取得并实际检查**满足仓库证据合同的 2006–2007 Wayback/WARC response。因此：

- 当时真实首页 DOM：`unknown`
- charset：`unknown`
- 是否使用 frames / tables / JS：`unknown`
- 是否有在线表单：`unknown`
- 热线名单页面 URL pattern：`unknown`
- 页面是否要求 IE：`unknown`
- 子资源保存情况：`unknown`

正确表述是 **verified capture not obtained in this slice**，不是“Wayback 没有”。

---

## 4. 2008–2011：论坛把“剩余时间”变成可搜索需求，但帖子不是排班系统

### 2008 济南

同期报道记录，一名有 8 个月婴儿的家庭因为自己单独请一个保姆觉得浪费，在网上看到“拼保姆”后，希望由家政公司协调两个家庭共同使用一名保姆。报道采访的家政公司认为这种安排要求家庭地理距离近、工作时间互补。

来源：

- https://news.sina.com.cn/c/2008-12-09/111514852819s.shtml

证据等级：**B，同期媒体；包含雇主与家政员采访。**

### 2009 成都

同期报道直接观察成都网站论坛里的“拼保姆”帖子，例如一个家庭说自己的住家保姆空闲时间较多，希望寻找愿意共同分担工资的邻近家庭；另一条需求只需要工作日晚饭与清洁。实际采访的三户共享案例里，服务员总工资上升、各家庭成本下降，但业内人士提醒晚饭等相同时段会发生排班冲突。

来源：

- https://finance.sina.com.cn/roll/20090310/06452718576.shtml

证据等级：**B；媒体观察了论坛内容 + 线下采访。**

### 2011 南充

同期报道记录一名异地工作的企业主管在网上发“合租保姆”帖，希望与附近住户共享做饭服务。

来源：

- https://news.sina.com.cn/o/2011-02-14/075021949741.shtml

证据等级：**B。**

### 状态链

```text
forum post exists
  ↓
other household sees it
  ↓
reply / PM / phone exchange
  ↓
addresses close enough
  ↓
schedules are complementary
  ↓
worker agrees
  ↓
price-sharing rule agreed
  ↓
actual multi-household route executed
  ↓
arrangement survives schedule collisions
```

### 新增 gaps

- `forum-post / real-arrangement gap`
- `reply / private-contact gap`
- `stated-schedule / actual-availability gap`
- `nearby-on-Web / route-feasible gap`
- `shared-cost-plan / worker-consent gap`
- `shared-nanny / durable-schedule gap`

论坛特别容易制造一种档案错觉：帖子能证明“有人提出这个组合”，不能证明第二天真的有第二户家庭、家政员真的同意、持续了多久。

私信、电话与家庭地址又恰好是最不应/最难被 archive 重放的部分。

---

## 5. 2009：online identity 与线下职业身份并不相同

2009 年成都同期采访里，一名高薪“管家”要求媒体用化名，不愿亲朋好友知道自己做家政；她说在雇主住宅里，访客往往把她当亲戚或公司管理人员。公司本身也使用“管家”而不是“保姆”的岗位名称。

来源：

- https://news.ifeng.com/society/2/200906/0608_344_1192789.shtml

证据等级：**B + contemporaneous self-report**。

对旧 Web 考古的意义：

`platform/profile occupational label ≠ person's socially disclosed identity`

研究普通用户页面时不能从“某个家政员 profile”倒推出她在亲属、邻里、老乡网络中也公开使用同一职业称谓。

还应遵守隐私最小化：普通劳动者旧 profile、电话、身份证等若在 archive 中出现，不因历史研究而重新批量公开。

---

## 6. 2013–2015：从“找号码”到“下单”，但 O2O 没有把 household work 变成纯线上事务

### 2013：Web / App / 微信与传统中介并存

2013 年上海同期报道介绍“云家政”时，明确用“传统中介翻大本子”和“熟人口口相传”作为既有模式对比，并说平台已让数百家机构与数万名实名家政员资料“上网”，同时支持鼠标、App、微信预约。

来源：

- https://news.sina.com.cn/o/2013-07-16/131927683121.shtml

证据等级：**B；其中平台规模数字主要来自平台/协会自报。**

### 2014：在线搜索之后仍然要上门面试

中新网 2014-04-15 报道：上海家庭生活服务发包平台可以在线搜索、匹配和购买服务；家政员之后仍需上门面试，合格后才开始工作；雇主还可以评价，平台追踪服务质量。

来源：

- https://www.chinanews.com/cj/2014/04-15/6067613.shtml

证据等级：**B + platform claims**。

状态链：

```text
profile/database visible
  ↓
search/filter
  ↓
order / appointment
  ↓
worker accepts / platform dispatches
  ↓
offline arrival
  ↓
interview
  ↓
household accepts
  ↓
service begins
  ↓
completion
  ↓
payment / rating / insurance / complaint
```

因此新增：

- `profile-to-person-identity gap`
- `listing-to-current-availability gap`
- `web-match-to-offline-interview gap`
- `interview-to-household-entry gap`
- `order-to-attendance gap`
- `service-completed-to-household-satisfied gap`
- `rating-to-actual-care-outcome gap`

### 2014：淘宝“网购”流程把家政塞进电商状态机

《新民晚报》2014-03-26 报道淘宝“生活家”接入家政服务：消费者在手机淘宝下单、支付到支付宝，服务上门完成后再确认付款，并提供爽约/清洁质量等规则；在沪首批接入约 2000 名钟点工。

来源：

- https://xmwb.xinmin.cn/html/2014-03/26/content_9_3.htm

证据等级：**B + platform claims**。

这意味着旧 Web / 移动 Web 考古必须再分：

`page rendered → order created → escrow paid → dispatch → attendance → service → user confirmation → payment released`

一张历史商品/服务页最多证明 listing 层，不自动证明支付与履约层。

### 2014：native app 开始成为交易入口

同期报道已经把 Web、手机 App、LBS、微信和线下培训混在同一服务栈里。例如 e 家洁的模式是用户在移动端发单，订单按地理位置推给附近阿姨，劳动者在线下培训、线上接单与被评价。

来源：

- https://finance.cnr.cn/gs/201408/t20140821_516275331.shtml
- https://www.sinotf.com/GB/News/1001/2014-09-16/0MMDAwMDE4MDE0MQ.html

这产生 **native-app transition gap**：到 2013–2015，仅做 HTTP/HTML archive 已经越来越无法覆盖完整交易路径。

---

## 7. Web archive 最容易漏掉的：真正的工作发生在私宅里

网页可能保留：

- 公司介绍；
- 阿姨照片 / 年龄 / 籍贯 / 技能；
- 月薪参考；
- 身份/健康/技能认证标签；
- 预约按钮；
- 用户星级；
- 服务规则；
- 门店地址；
- 电话号码。

但以下状态通常在 Web archive 里不可见或只剩二次叙述：

- 面试时谈了什么；
- 雇主最终为何选这个人；
- 实际工资是否和页面相同；
- 是否住家；
- 家政员睡在哪里、什么时候休息；
- 是否允许带手机；
- 老人/婴儿真实照护结果；
- 家庭成员如何评价；
- 私下加薪、红包、额外工作；
- 为什么辞职/被辞；
- 是否绕过平台接“私单”；
- 口碑如何从一户人家传到下一户。

这组不可见部分可以称为：

**private-household transaction dark matter / 私宅事务暗物质**。

家政旧网研究的一个重要结论不是“Web 保存了多少”，而是明确写出：**家庭服务的核心结果天然发生在 archive acquisition surface 之外。**

---

## 8. 证件与信任：certificate-display ≠ verified capability

2000s 后家政越来越职业化，网页/门店会展示身份证、健康证、培训证、母婴护理等级等。但至少需要分开：

```text
certificate displayed
  ↓
certificate issuer identifiable
  ↓
certificate authentic
  ↓
standard comparable across issuers
  ↓
skill actually present
  ↓
skill relevant to this household
  ↓
trust established
```

2019 年以后出现更系统的信用查询，但这已经超出本文件核心 old-Web 时间窗，只作为后续谱系提示。

老网页若只有一个“金牌 / 高级 / 持证”badge，不能让研究者倒推出统一国家资格或已验证技能。

新增：

- `certificate-display / validity gap`
- `issuer / cross-issuer-comparability gap`
- `credential / performed-skill gap`

---

## 9. “人找到了”仍不是“今天能上户”——后续阶段压力测试

2020 年上海疫情材料虽然超出本仓主时段，但作为 state-machine pressure test 很有价值：一名家政员即使持身份证、复工证、健康证、健康码和 14 天行动轨迹，也可能被不同小区门岗拒绝；有雇主因接人流程过于麻烦暂停下一单。

来源：

- https://news.sina.cn/gn/2020-03-20/detail-iimxyqwa1935609.d.html

它验证了 2005–2015 框架里一直存在但不容易被网页看到的最后一层：

`matched worker ≠ physically executable household entry`

所以即便未来取得完整 O2O 订单页面，也必须留有 `contract/order-to-household-entry gap`。

---

## 10. Platformization 的反例：线下与熟人网络没有自然消失

2023 年“阿姨来了”平台自身的样本调查称，其受访家政员找工作渠道里，线下家政公司约占 51%，熟人介绍约 35%，互联网平台约 13%。这是平台样本，不是全国统计，但恰好构成反例：平台成熟后，熟人与线下公司仍然重要。

来源：

- https://news.bjd.com.cn/2024/03/20/10725966.shtml

所以历史谱系不能写成：

`街道/熟人 → 网站 → App → 线下消失`

更像：

```text
熟人 / 老乡 / 妇联 / 街道 / 家政公司
        ↘ 电话
           ↘ Web 目录 / 论坛
              ↘ 实名数据库 / O2O / App / 微信
                 ↘ 评价 / 信用记录

这些层长期并存，并会在具体家庭、工种和城市里重新组合。
```

---

## 11. Evidence ledger

| 日期 | 事实单位 | 等级 | 可以证明 | 不能证明 |
|---|---|---:|---|---|
| 2005-01 | 家政公司网站价格 + 电话核实 | B | Web 已用于价格/服务信息；页面价格可滞后 | 北京统一市场价、成交结果 |
| 2006-12 / 2007-01 | 两个 Web locator + 134 热线 | B/B | Web 可做热线目录；热线是匹配事务层 | 原页面 DOM、热线实时在线率 |
| 2008-12 | 济南网上看到“拼保姆” | B | Internet 信息进入照护时段共享 | 论坛原帖已恢复、安排长期成功 |
| 2009-03 | 成都论坛“拼保姆” + 线下案例 | B | 论坛发现需求与现实共享可发生 | 所有论坛帖都落地 |
| 2009-06 | 高薪“管家”隐藏职业身份 | B/同时性自述 | 职业标签与社会身份可分离 | 家政行业整体污名程度 |
| 2011-02 | 网上“合租保姆”发帖 | B | 共享照护需求仍经 Web 协调 | 排班长期可执行 |
| 2013-07 | 云家政 Web/App/微信资料 | B/platform | 多入口和实名资料平台化已出现 | 全国采用、平台规模独立验证 |
| 2014-03 | 淘宝生活家家政下单 | B/platform | 电商 escrow/确认流程进入家政 | 每单履约、评价真实性 |
| 2014-04 | 云家政在线匹配 + 线下面试 | B/platform | online match 与 offline interview 共存 | “找阿姨难”已解决 |
| 2014-08/09 | LBS/App/O2O | B | 原生移动入口成为家政控制面 | Web archive 可覆盖完整事务 |

---

## 12. M1 status

**M1 NOT ACHIEVED IN THIS SLICE.**

原因不是对象不重要，而是本轮没有得到满足 `docs/METHOD.md` 合同的 historical capture bundle。

目前有：

- 2005–2014 多份同期数字报刊/新闻页面；
- 明确的 historical locators（如 `www.jiazhengbj.org`、`www.bjcs.gov.cn`）；
- 同期媒体对论坛、家政网站、O2O 页面和用户操作的观察；
- 多个独立 evidence family 支持“Web/电话/论坛/O2O 逐渐进入匹配链”。

但仍缺：

- 一份实际打开并核验的 2005–2010 家政站点 Wayback/WARC capture；
- 原始 HTTP headers；
- charset；
- 当时 DOM/CSS/JS；
- IE/ActiveX/Flash/browser assumptions；
- 价格页版本历史；
- 论坛原 thread capture 与回复链；
- PM/QQ/电话后的现实结果；
- 2013–2015 App/API/backend 历史 artifact。

因此禁止写：

- “北京家政网 2007 年页面长这样”；
- “某论坛帖子最终促成了共享保姆”；
- “2014 O2O 下单即履约”；
- “今天能访问的媒体截图就是当时用户看到的原始家政平台”。

---

## 13. 后见之明与隐私风险

1. **不能因今天 O2O 熟悉，就把 2007 网站理解成现代平台。** 当年的 Web 很可能只是号码、介绍和静态信息控制面。
2. **不能把帖子当 outcome。** 求职帖、求阿姨帖、拼保姆帖只证明意向和可观察协调。
3. **不能从公开 profile 重新公开普通人的敏感资料。** 电话、身份证、健康信息、住址应最小化。
4. **不能把“实名数据库”写成完全解决信任。** 数据真实性、更新周期、技能与家庭适配仍是另外状态。
5. **不能把平台评级写成客观护理质量。** 评分本身也有平台选择、沉默和交易外口碑。
6. **不能把 App 时代自动纳入 Web archive。** 2013–2015 后，native client、API、推送和支付后台已经越来越重要。

---

## 14. 下一步真正高价值的考古动作

优先级从高到低：

1. 实际取得并核验 `www.jiazhengbj.org` 或同期家政公司 2005–2010 至少两个历史时点的 capture；
2. 找到一个 2008–2011 “拼保姆/求阿姨”论坛原 thread 的可验证 capture，记录 thread URL、回复、附件与 archive gap；
3. 找一份 2013–2015 云家政/淘宝生活家/e家洁 的原始帮助页、FAQ、订单状态说明或手机客户端手册；
4. 对一个历史站点实际验证 GB2312/GBK、IE compatibility 与表单行为；
5. 若能取得 App artifact，只记录 package/version/API locator 与界面证据，不把现代安装/模拟重建冒充历史原件。

---

## 本轮对旧网考古最重要的结论

> **家政旧网不是“保姆网站史”，而是一次非常典型的跨媒介事务考古。**
>
> 2005 年页面上的工资还要打电话重谈；2007 年网站主要告诉你该拨哪一条热线；2009 年论坛能让两个家庭发现彼此，但排班和同意仍发生在线下；2014 年平台已经能搜索、预约、支付、评价，真正的面试、进门和照护却依旧发生在住宅里。
>
> 因此，网页越完整，也越要问它没有保存什么：**真正把一个陌生人变成“每天早上会拿钥匙走进你家的人”的那条链，恰恰最容易消失在 Web archive 之外。**
