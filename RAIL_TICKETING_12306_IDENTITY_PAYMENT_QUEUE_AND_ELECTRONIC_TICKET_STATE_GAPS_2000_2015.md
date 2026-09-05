# 中文旧网铁路购票、12306、实名、支付与票权状态缺口（2000–2015）

## Scope

本稿只研究约 2000–2015 中文 Web 与铁路售票系统交叉的一条窄线：

> **一个旧网页显示“有票”“预订成功”“支付成功”以后，我们还缺哪些状态，才能证明一个历史用户当时真的获得了可以乘车的有效票权？**

这不是中国铁路史，也不是 2020s 12306 产品史。

全球 Minitel/SNCF、铁路票务前史与 2015 以后电子客票/候补的生活史比较放在 `how-people-lived`。

本仓只处理：

- 中文 Web 页面与账号；
- 票额/查询/锁席/订单状态；
- 实名与乘车人记录；
- 浏览器、根证书、验证码；
- 网上银行支付跳转；
- 邮件/SMS通知；
- 纸票交换与身份证直刷之间的边界；
- archive 能保存什么、必然缺什么。

方法依据：`docs/METHOD.md`。

---

## 1. 研究单位必须拆开

至少区分：

- **rail inventory system**：铁路后台客票库存/席位系统；
- **sales channel**：车站窗口、代售点、电话、网站等；
- **Web platform / host**：如 `12306.cn`；
- **account**：注册用户；
- **passenger record / 常用联系人**：账号中保存的乘车人身份；
- **query**：一次出发地/目的地/日期查询；
- **availability representation**：网页返回的余票表示；
- **order request**：用户提交购票请求；
- **seat hold**：临时锁定席位；
- **payment session**：铁路站点向银行/支付渠道转移后的交易状态；
- **payment result**：铁路侧认为支付是否成功；
- **ticket entitlement / electronic ticket record**：有效运输合同/票权记录；
- **paper ticket**：换取的纸质票；
- **identity credential**：身份证等；
- **gate state**：车站检票/自动闸机是否接受；
- **notification**：邮件/SMS；
- **archive capture**：档案保存的一份 Web 表示。

不能把：

> `网页 → 账号 → 查询 → 有票 → 锁席 → 支付 → 出票 → 纸票 → 身份证 → 进站`

压成一个“网上买票成功”。

---

## 2. 最小状态链

```text
train/service exists
→ inventory exists
→ inventory allocated to channel
→ 12306/query endpoint reachable
→ query accepted
→ response rendered
→ user notices target train/seat class
→ booking request submitted
→ server accepts request
→ seat successfully held
→ payment deadline created
→ bank/payment page reachable
→ user authentication/payment succeeds
→ result returns to railway system
→ ticket entitlement issued
→ email/SMS optionally generated
→ paper exchange required OR identity direct-gate path available
→ ticket/identity accepted at station
→ passenger boards
```

因此固定：

> **query says 有票 ≠ order accepted ≠ seat held ≠ payment succeeded ≠ ticket issued ≠ paper exchanged ≠ gate accepted ≠ passenger boarded。**

---

## 3. 2000 左右地方网上售票试验：只能作为前史，不能倒写成全国 12306

2011 年《京华时报》回顾称，北京铁路系统在约 2000 年曾做过“首铁在线”等网络购票尝试；春运、五一等高峰出现服务器压力，后来部分网上/电话售票能力又发生变化。

来源：

- 《铁路网上订票进程历经11年 记者体验网购车票》，京华时报，2011-06-12，搜狐保存：https://news.sohu.com/20110612/n309941949.shtml

Evidence：

- 对 2011 年记者实际体验部分：**Grade B-high contemporaneous**；
- 对约 2000 年历史回顾部分：**Grade C/B-low retrospective**。

### 能证明

- 全国 12306 之前存在过地方性 Web/网络售票试验；
- “铁路内部客票联网”与“公众 Web 购票”并不是同一时点。

### 不能证明

目前没有本轮实际验证的 2000 `首铁在线` historical memento，因此不知道：

- original URL；
- 页面标题；
- charset；
- HTML/frameset；
- 表单 action；
- 支持什么票种；
- 是否实时库存；
- 是否先登记后人工出票；
- 是否有在线支付；
- cookie/session；
- 实际日活/交易量。

所以这个对象只留作 **prehistory locator**，不计 M1 完整案例。

---

## 4. 2011-06-11/12：12306 首批网络售票的同时代 Web 状态

### 4.1 银行一手材料证明支付链路存在

中国工商银行同期公告记录：2011-06-11 20:47，一名天津客户在 12306 预订 C2057 北京南—天津车票后，通过工行网上银行完成在线支付；铁路随后通过邮件或短信发送购票信息。

来源：

- ICBC《工行成功办理国内首张网购火车票在线支付》：https://www.icbc.com.cn/icbc/工行风貌/工行快讯/工行成功办理国内首张网购火车票在线支付.htm

Evidence：

- **Grade A**：同期银行官方业务公告。

它可以证明：

```text
12306 reservation
→ online banking payment
→ railway ticket information
→ email/SMS notification
```

至少在首批京津城际试点中真实跑通。

但不能证明所有银行、浏览器、用户、线路都成功。

---

## 5. 一张 2011 同时代截图很重要，但它不是 WARC

2011-06-12《京华时报》记者实际登录 12306，并刊出“记者体验购票网页截屏”。报道逐步记录：

- 首页进入“客运服务”；
- 登录界面；
- 新用户注册；
- 实名、身份证、手机、邮箱；
- “车票预订”；
- “车票查询”；
- 北京南—天津、日期、车次、席别；
- 系统自动分配车厢/座位；
- “席位已成功锁定，请您在15分钟内进行网上支付，否则席位将自动释放给其他旅客”；
- 邮箱/短信通知。

来源：

- https://news.sohu.com/20110612/n309941949.shtml

### Evidence 分层

- 记者文字操作日志：**Grade B-high**；
- 报道中同期页面截图：对截图内**肉眼可见的页面元素**可视为 **Grade A-like visual evidence**；
- 但它不是可检查 HTTP、HTML、JS、CSS、子资源、headers 的 archive capture。

因此禁止：

> `有截图 → 已复原 2011 12306`。

### screenshot / executable page gap

截图最多证明：

- 某时点有这种视觉表示；
- 某些标签/按钮/文字可见；
- 页面曾被真实记者操作到。

不能证明：

- 原 DOM；
- `name=` 字段；
- form method/action；
- JavaScript validation；
- cookies；
- charset；
- hidden inputs；
- CSRF/session tokens；
- AJAX/API endpoint；
- 同日其他用户看到完全相同版本。

---

## 6. query-result / inventory-state gap

记者查询到某车次“一等、二等均有票”，这最多证明：

> **某次查询响应在某个时刻把相应席别表示为可售。**

不能自动证明：

- 查询结果生成时后台仍有同样票额；
- 用户点击预订时仍有；
- 票额没有被别的并发订单占用；
- 该票额没有渠道/区间限制；
- 最后一定锁席成功。

建议字段：

```yaml
query_submitted_at:
query_parameters:
availability_label_observed:
response_rendered_at:
booking_submitted_at:
seat_hold_result:
```

### 新缺口：**display/allocation race gap / 显示—分配竞争缺口**

实时票务里，页面上看到的库存和提交请求时的库存天然可能属于不同毫秒/秒级状态。

这在节假日高并发时尤其关键。

---

## 7. 15 分钟锁席：旧 Web 页面曾控制一个会自动过期的现实权利

2011 报道明确显示：系统成功锁席后生成 15 分钟支付截止时间，逾时席位自动释放。

来源：

- 京华时报：https://news.sohu.com/20110612/n309941949.shtml
- 郑西高铁记者体验：https://news.sina.com.cn/c/2011-09-20/035023182518.shtml
- 燕赵都市报：https://news.sina.com.cn/o/2011-09-30/070023242267.shtml

Evidence：

- **Grade B-high / multiple contemporaneous hands-on reports**。

### 新状态：**expiring entitlement precursor / 会过期的票权前状态**

`seat held` 不是最终 ticket entitlement。

至少还有：

```text
hold_created_at
hold_expires_at
payment_started_at
payment_succeeded_at
payment_callback_received_at
railway_ticket_issued_at
```

任何 archive 截到“席位已成功锁定”都不能写成“用户已经买到票”。

---

## 8. payment-page / railway-result gap

### 8.1 支付是跨站点/跨机构状态机

2011 年记者体验中，铁路页面把用户带到银行网银；用户还可能要安装银行安全插件，再返回铁路系统。

燕赵都市报记者记录自己前两次支付均失败，客服建议重试。

来源：

- https://news.sina.com.cn/o/2011-09-30/070023242267.shtml

新闻晚报记者则记录网上退票后退款可能要等待较长银行处理周期。

来源：

- https://news.sina.com.cn/c/2011-09-22/143823199664.shtml

### 必须拆：

```text
bank page rendered
≠ bank accepted credentials
≠ debit succeeded
≠ railway received success callback
≠ ticket issued
≠ refund initiated
≠ refund credited
```

### 新缺口：**cross-domain transaction gap / 跨域交易缺口**

旧 Web archive 即使同时保存 12306 和某银行公共帮助页，通常也不会、也不应该保存真实用户那次登录后的私人交易 session。

因此 transaction outcome 天然处于 archive darkness。

---

## 9. root certificate / browser state：历史页面“今天能打开”不等于当年能买票

2011 年同期记者体验多次提到首次使用需要下载安装“根证书”。

同时《新京报》实际测试：Chrome、Firefox、Safari、Opera 当时不能正常完成 12306 登录购票，而 IE9、360 浏览器可以；铁路客服解释网站基于 IE 标准制作，支持 IE6+。

来源：

- 新京报，2011-06-15：https://news.sina.com.cn/c/2011-06-15/084622643844.shtml
- 2011-09 实测：https://news.sohu.com/20110915/n319446832.shtml

Evidence：

- **Grade B-high contemporaneous technical test**。

### 新状态：**client-capability gate / 客户端能力闸门**

一个 historical URL 的状态至少要再加：

```yaml
browser_family:
browser_version:
root_certificate_installed:
js_runtime_assumption:
online_banking_plugin:
security_warning_state:
```

### old-Web 结论

现代 Chromium 能显示一个重放页面，只能证明：

> “现代环境能渲染 archive rewrite 后的某种表示。”

它绝不能证明：

> “2011 年 Chrome 用户当时也能完成购票。”

这个案例正好满足仓库 M3 所要求的“浏览器环境改变历史解释”类型，但本轮尚未进行旧浏览器重放实验，因此不勾 M3。

---

## 10. email/SMS notification / ticket entitlement gap

2011 年铁路和银行材料都描述支付成功后向用户发送邮件或短信。

因此通知链还要拆：

```text
railway generated notification
→ mail/SMS provider accepted
→ delivered
→ user device/account reachable
→ user noticed
```

通知内容可以包含车次、座位、订单号等，但：

> **收到一封“支付通知”不应单独替代后台 ticket record 作为完整历史证明。**

反过来，没保存邮件也不能证明用户没买票。

这是典型的：

### **private-notification survival gap / 私人通知幸存缺口**

公共 archive 很少合法保留普通人的交易邮件和短信。

---

## 11. electronic-order / paper-ticket gap

2011 年不同线路、车站并不处于同一票制状态。

### 一种状态

京津、京沪部分具备二代身份证检票条件的车站，可以让符合条件用户凭购票身份证直接进出站。

### 另一种状态

石家庄等同期报道明确要求网上购票后到指定窗口/代售点换纸票。

来源：

- 燕赵都市报，2011-09-30：https://news.sina.com.cn/o/2011-09-30/070023242267.shtml
- 工行后续说明：https://www.icbc.com.cn/page/721852349806313473.html

Evidence：

- **A/B-high**。

### 新缺口：**online purchase / gate medium gap / 在线购买—进站介质缺口**

不能因为 Web 里叫“电子客票”就默认：

- 全国无纸；
- 所有车站身份证直刷；
- 所有证件都可机器识读；
- 用户不需要到窗口。

字段应至少有：

```yaml
purchase_channel:
ticket_record_type:
paper_exchange_required:
identity_direct_gate_supported_at_origin:
identity_direct_gate_supported_at_destination:
actual_gate_medium:
```

---

## 12. website service-hours / train-departure gap

早期 12306 并不是天然 24×7 的现代服务。

2011 同期材料写明部分初期网络售票服务时间为约 5:00–24:00，且网上购票/退改签对“距开车还有多久”有明确截止要求。

来源：

- 京华时报 2011-06：https://news.sohu.com/20110612/n309941949.shtml
- 武广等线上售票同期规则可由 2011 铁路/媒体材料交叉。

### 新状态：**service-window / journey-window gap / 网站营业时间—行程时间缺口**

“Web 服务”不自动等于随时可操作。

研究旧票务页时应记录：

```yaml
site_service_hours:
booking_cutoff_before_departure:
refund_change_cutoff:
observed_at:
```

---

## 13. 2012 春运：前台网页只是大规模实时分配系统的一层壳

新华社后来引述 12306 建设者回顾：2012 年春运高峰日售票 119.2 万张、超设计能力约 20%，用户侧表现为余票页面刷新不出、提交卡顿等。

来源：

- 新华网，2018-02-01：https://www.xinhuanet.com/politics/2018-02/01/c_1122350190.htm

Evidence：

- **Grade C-high / institutional retrospective**。

### archive 特别风险：**front-end survivorship / backend-load disappearance**

一份静态 archive capture 很可能保存：

- logo；
- 查询框；
- 登录页；
- 帮助页；

却完全保存不了当时真正决定用户体验的：

- 并发请求量；
- queue depth；
- cache state；
- inventory lock contention；
- database latency；
- payment callback backlog；
- 某用户重复提交了几次。

因此不能用“今天回放很快”反驳“当时系统很卡”。

---

## 14. CAPTCHA / anti-bot state 也是历史页面版本的一部分

2013 起 12306 为对抗抢票程序持续调整验证码；2015 年 3 月进一步改成图片选择验证码。

来源：

- 新华网 2018 回顾：https://www.xinhuanet.com/politics/2018-02/01/c_1122350190.htm
- 京华时报/人民网，2015-03-17：https://politics.people.com.cn/n/2015/0317/c1001-26703227.html

Evidence：

- 2015 页面报道：**Grade B-high contemporaneous**；
- 2013 变迁若仅依赖 2018 回忆：**Grade C-high**。

### 新缺口：**captcha-version gap / 验证码版本缺口**

必须区分：

- 是否有验证码；
- 在登录、查询还是提交订单触发；
- 文本/数字/图片；
- 图库版本；
- 刷新频率；
- 失败后冷却/频控；
- 是否针对异常请求提高验证强度。

一张 2015 登录页截图不能证明 2012 同一 URL 使用同样验证码。

---

## 15. 2014：账号中的“人”本身变成有状态的对象

12306 2014-02-23 官方《铁路互联网购票身份核验须知》规定，自 2014-03-01 起，注册用户和常用联系人要显示身份核验状态。

二代居民身份证可能出现：

- 已通过；
- 待核验；
- 未通过。

部分其他证件还有“请报验”“预通过”等状态。

某些状态必须持原件到车站窗口或代售点处理后才能正常网上购票。

来源：

- 12306 官方历史页面：https://www.12306.cn/mormhweb/weixin/dtzx/wx_zxdt/201402/t20140223_38539.html
- 新华社同期报道：https://politics.people.com.cn/n/2014/0223/c70731-24440092.html

Evidence：

- **Grade A**：官方同时代规则。

### 新状态链

```text
account exists
≠ passenger contact exists
≠ identity submitted
≠ identity verified
≠ identity currently eligible for online purchase
```

### identity-status / real-person gap

页面显示“已通过”只能证明系统在该时点赋予该记录某种可用状态；历史研究仍不能由此过度推断：

- 谁实际控制账号；
- 谁代购；
- 现实乘车人是否最后上车；
- 身份证件是否遗失/被冒用。

---

## 16. 2014：“行程冲突”证明票务数据库开始约束一个人的时间拓扑

2014-12-26 起，12306 宣布不再售卖同一乘车人时间冲突的车票；如果身份信息被冒用导致冲突，用户可以举报后继续购票。

来源：

- 新京报/人民网，2014-12-26：https://politics.people.com.cn/n/2014/1226/c70731-26281781.html

Evidence：

- **Grade B-high contemporaneous report quoting 12306 announcement**。

### 新状态：**itinerary-consistency check / 行程一致性检查**

系统不再只问：

> “这张票有没有？”

还会问：

> “这个身份在这一时间段是否已经绑定另一段不相容行程？”

因此 ticketing database 开始编码一个人的**可移动时间拓扑**。

这对旧网页考古意味着：

> 同样的余票、同样的账号页面，对两个乘车人记录可以返回不同的可购买性。

---

## 17. 2014 用户材料：身份状态会让“看见的票”在手续完成前消失

广州日报 2014 年报道一名邓女士：家人的身份证信息未通过核验，原本看到的两张潮汕—深圳车票因为需要先处理身份核验而错失。

来源：

- https://travel.people.com.cn/n/2014/0415/c41570-24896860.html

Evidence：

- **Grade B / contemporaneous first-person report**。

### 新缺口：**visible-inventory / credential-readiness gap / 票额可见—身份就绪缺口**

有票 + 有钱 + 有网 + 有账号仍可能不够。

如果 passenger state 不是可购买状态，库存会在制度手续完成前改变。

---

## 18. 2015 图片验证码：页面可访问仍不等于操作可完成

2015-03-16 后，12306 登录/购票验证改为根据提示点击图片。同期报道记录 8 张图的选择界面；用户抱怨模糊和反复失败。

来源：

- 京华时报/人民网，2015-03-17：https://politics.people.com.cn/n/2015/0317/c1001-26703227.html
- 京华时报/人民网，2015-12-11：https://finance.people.com.cn/n/2015/1211/c66323-27916267.html

Evidence：

- **Grade B-high contemporaneous screenshot/reporting**。

### page-load / task-completion gap

一个 archive 能重放验证码区域，不代表：

- 图片资源全部保存；
- 当年的题目集合保存；
- 验证 endpoint 仍存在；
- challenge/session 绑定可重放；
- 现代用户能完成历史验证；
- 当时所有用户都见过相同题目。

因此 CAPTCHA 是典型的**动态私人状态不可回放对象**。

---

## 19. old-Web 票务的核心时间轴不是一个时间戳

至少要记录：

```text
train_departure_time
presale_open_time
query_time
availability_response_time
booking_submit_time
seat_hold_time
hold_expiry_time
payment_start_time
payment_success_time
railway_callback_time
ticket_issue_time
notification_time
paper_exchange_time
gate_time
archive_capture_time
```

### 为什么重要

在高并发票务里，几秒就可能改变解释。

例如：

- 10:00:01 页面显示有票；
- 10:00:03 用户点击提交；
- 10:00:04 库存被其他订单锁定；
- 10:00:06 返回无票。

archive 如果只保存 10:00 左右一个 HTML，无法还原整条 transaction。

---

## 20. inventory allocation / channel equality gap

即使多个渠道接到同一全国客票系统，也不能不经证据就写：

> “所有渠道始终看到完全一样的票额。”

需要单独查：

- 不同时期是否有渠道票额分配；
- 学生/团体票预留；
- 车站/代售/电话/网络是否共享实时库存；
- 区间票额如何释放；
- 春运临客/新增列车何时进入系统。

2001、2011 的材料都提示“票源分配”本身是问题，但本轮没有足够原始配置文件，因此：

### `channel_inventory_policy = unknown unless sourced`

不从页面表现倒推后台分票算法。

---

## 21. page state / user attention gap

即使 archive 恰好保存了：

- 有票；
- 截止时间；
- 支付按钮；
- 换票提示；

也不知道历史用户是否：

- 看见；
- 理解；
- 点击；
- 在倒计时结束前完成；
- 因为浏览器错误放弃；
- 转去车站窗口。

所以一个旧票务页面的意义不能只从 UI 推到行为。

建议证据组合：

- 页面/截图；
- 同期用户操作报道；
- 官方规则；
- 交易/规模统计；
- 后来回忆只做补充。

---

## 22. 公共 archive 天然保存不了最关键的票务状态

### 容易保存

- 首页；
- 公共查询框；
- 注册/登录壳；
- 帮助页；
- 购票须知；
- 浏览器提示；
- 公告；
- 静态验证码外观截图。

### 很难/不应公开保存

- 真实姓名；
- 身份证号；
- 常用联系人；
- 真实订单；
- seat hold token；
- 银行支付 session；
- 手机/邮箱；
- 实时库存快照；
- 实际排队位置；
- 身份核验后台结果细节；
- 某个人最终是否过闸。

### 新机制：**public-shell / private-allocation asymmetry / 公共外壳—私人分配状态不对称**

一个票务网站保存得越像“完整网站”，越容易让后人误以为真实交易也被保存了。

实际上最关键的：

> “那一秒到底有没有把那张票分给这个人？”

通常正是最不可归档的状态。

---

## 23. privacy stop condition

铁路购票涉及极高密度个人信息。

本仓禁止为了补历史状态而：

- 寻找泄露的真实身份证号；
- 尝试登录历史普通用户账号；
- 复用旧密码；
- 收集私人订单截图中不必要的姓名、身份证、手机号；
- 测试当前 12306 是否接受历史用户数据；
- 批量重新发布历史订单/行程。

研究平台结构时优先：

- 公告；
- 官方帮助页；
- 同期记者自己的体验账号；
- 已公开的教学截图；
- 去标识的流程状态。

这符合 `docs/METHOD.md` 的隐私最小化要求。

---

## 24. 本轮实际取得的最强 historical visual evidence

### 对象

2011-06-11/12 京津城际网络售票首日附近的 12306 页面。

### 证据

《京华时报》2011-06-12 报道所刊“记者体验购票网页截屏” + 逐步骤记者操作日志。

### 证据等级

```yaml
source_type: contemporaneous newspaper report + screenshot
page_visual_elements: A-like
interaction_report: B-high
verified_warc: false
verified_wayback_memento: false
html_dom: unknown
charset: unknown
subresources: unknown
http_headers: unknown
cookies: unknown
js_endpoints: unknown
```

### 为什么不能升 M1 capture

仓库 `docs/METHOD.md` 要求 archive capture 最少能区分 original resource / memento，并记录 capture URL、original URL、capture datetime、回放状态、主文档与子资源、charset 等。

本轮没有取得满足这些字段的一份 2011 12306 verified memento。

所以：

> **同期截图很强，但仍然不是 Web archive capture。**

---

## 25. 本轮 archive 负结果

本轮主动寻找过：

- 2000 前后地方网上售票试验；
- 2011 初版 `www.12306.cn`；
- 早期客运服务/车票预订页面；
- 2014 身份核验页面；
- 2015 图片验证码页面。

当前公开 Web 搜索可以定位大量同期报道、官方说明和截图，也能找到今天仍保存的部分旧公告；但本轮**没有取得并实际打开、检查一份满足 M1 最低字段的 2011–2015 交易流程 Wayback/WARC memento**。

因此保留 unknown：

- original query URL pattern；
- 2011 charset；
- DOM/frames；
- form action；
- AJAX endpoint；
- session/cookie 名；
- root certificate 技术细节；
- 银行跳转 POST 字段；
- 余票 response schema；
- 2012 排队/频控内部字段；
- captcha challenge endpoint；
- 历史 inventory API。

“没有找到/没有验证”不写成“当时不存在”。

---

## 26. 与 `how-people-lived` 的交叉链接

配套生活史专题：

`topics/from-ticket-window-to-virtual-waitlist-rail-ticketing-and-mobility-executability-china-1980-2026.zh-CN.md`

两仓边界：

### `how-people-lived`

研究：

- 窗口排队；
- 返乡；
- 学生/务工者；
- 多路线替代；
- 法国 Minitel 对照；
- 2019 候补；
- 2020 电子客票；
- 2024 多方案候补；
- 普通人如何把旅行变成可执行行为。

### `old-web-archaeology`

研究：

- 2011–2015 中文 Web 状态；
- 页面/账号/乘车人/库存/锁席/支付；
- IE/根证书/验证码；
- 实名核验；
- 纸票交换；
- archive 缺失与隐私边界。

不把全球票务史和 2020s 12306 功能无限搬进本仓。

---

## 27. 建议状态模型

```yaml
rail_ticket_web_state:
  platform:
  host:
  observed_at:
  evidence_grade:

  client:
    browser:
    version:
    root_certificate_required:
    plugin_required:

  account:
    login_possible:
    passenger_record_present:
    identity_verification_state:

  query:
    origin:
    destination:
    travel_date:
    train:
    seat_class:
    availability_label:
    response_time:

  booking:
    request_submitted:
    seat_hold_created:
    hold_expires_at:

  payment:
    channel:
    redirected_to_bank:
    payment_result:
    callback_observed:

  ticket:
    entitlement_issued:
    notification_sent:
    paper_exchange_required:
    identity_direct_gate_supported:

  archive:
    archive_source:
    capture_url:
    original_url:
    capture_datetime:
    replay_status:
    charset:
    subresource_completeness:
```

每个字段允许 `unknown`，禁止为了“完整”而猜。

---

## 28. 新增 state gaps 清单

本轮新增/固定：

1. `backend-inventory / public-web gap`
2. `query-result / current-inventory gap`
3. `display / allocation-race gap`
4. `booking-request / seat-hold gap`
5. `seat-hold / final-ticket gap`
6. `hold-created / hold-expired gap`
7. `payment-page / bank-success gap`
8. `bank-success / railway-callback gap`
9. `payment-success / ticket-issued gap`
10. `email-sent / user-noticed gap`
11. `online-purchase / paper-exchange gap`
12. `paper-ticket / identity-direct-gate gap`
13. `browser-render / task-completion gap`
14. `root-certificate / modern-replay gap`
15. `captcha-shell / captcha-session gap`
16. `account / passenger-record gap`
17. `passenger-record / identity-verified gap`
18. `identity-verified / purchase-eligible gap`
19. `visible-inventory / credential-readiness gap`
20. `single-ticket / itinerary-consistency gap`
21. `public-shell / private-allocation asymmetry`
22. `archive-page-time / transaction-time gap`
23. `channel-availability / channel-inventory-policy gap`
24. `website-service-hours / train-departure gap`
25. `screenshot / executable-page gap`
26. `front-end-survival / backend-load gap`

---

## 29. 它改变 old-Web 考古的哪一点理解

### 29.1 Web 页面可以直接成为现实移动权的控制面

论坛、博客主要改变信息和社交；票务页则直接连接：

> 一个具体身份是否能在一个具体时间进入一趟现实列车。

这使页面状态的历史含义更高风险。

### 29.2 动态系统最重要的事实恰好最难被静态 archive 保存

对票务系统，真正关键的不是 logo，而是：

- 那一秒的库存；
- 那个身份状态；
- 那次锁席是否还有效；
- 那笔支付是否回调；
- 那个车站是否接受身份证直刷。

这些多数不会进入公共 archive。

### 29.3 “旧网页能回放”与“旧服务能重演”距离特别远

就算把 HTML/CSS/JS 全保存下来，没有：

- 实时客票后台；
- 身份核验；
- 银行支付；
- 短信/邮件；
- 车站闸机；

也不能真正“复活 2011 12306”。

所以历史复原若做到这一类网站，必须显式区分：

> **UI reconstruction** 与 **service reconstruction**。

后者几乎必然只能模拟，不应伪装成历史 original。

---

## 30. 已证实 / 高概率 / 不知道

### 已证实

- 2011 京津城际首批 12306 网络售票真实形成实名注册、查询、锁席、15 分钟支付、邮件/SMS通知链；
- 同期页面/流程依赖特定浏览器环境、根证书和网上银行；
- 某些线路可二代身份证直接检票，另一些站仍要求换纸票；
- 2014 网站把乘车人身份核验状态变成在线购票能力条件；
- 2014 行程冲突检查把同一身份的多个票权放入时间一致性约束；
- 2015 图片验证码直接进入登录/购票操作路径。

### 高概率

- 高峰期真实用户体验越来越由“公共页面 + 私人状态 + 后台实时负载”共同决定；
- 现代 archive 对这类系统存在特别强的静态壳保存偏差；
- 真实 transaction replay 在隐私、支付和失效后台方面存在结构性不可复原性。

### 不知道

- 2011 初版页面完整 DOM/charset/HTTP；
- 原始查询/提交 endpoint 与参数；
- 历史库存接口 schema；
- 2012 server queue 的具体实现；
- 不同售票渠道的票额分配策略细节；
- 2011 某一截图页面在不同浏览器中的像素级差异；
- 早期地方网上售票试验与全国客票系统的技术连接方式。

---

## 31. 下一步

最高价值不是继续收集“12306 十年发展史”，而是：

1. 找到一份 **2011–2012 verified Wayback/WARC memento**；
2. 实际打开并记录：
   - archive source；
   - capture URL；
   - original URL；
   - capture datetime；
   - charset；
   - 页面层级；
   - 主/子资源；
   - 登录/查询是否只是壳；
3. 如果能取得合法历史客户端环境，再做一个最小 IE6/IE8 vs modern Chromium 回放比较；
4. 只复原公共页面，不碰真实私人账号/订单；
5. 将 2011 报纸截图与 memento 做版式/控件交叉确认。

在拿到 verified memento 以前，本文件保持 **state-gap research note**，不宣称 M1 完整考古案例。
