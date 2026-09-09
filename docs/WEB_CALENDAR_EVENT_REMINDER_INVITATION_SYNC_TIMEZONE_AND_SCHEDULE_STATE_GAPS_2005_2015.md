# Web 日历、事件、提醒、邀请、同步、时区与未来状态证据缺口（2005—2015）

## 目的与 scope

本文件补充：

- `docs/METHOD.md`；
- `docs/ONLINE_TIME_SERVICE_NTP_PC_CLOCK_TIMESTAMP_DEADLINE_AND_SERVER_TIME_STATE_GAPS_2001_2015.md`；
- `docs/ONLINE_STORAGE_NETWORK_DISK_UPLOAD_DOWNLOAD_SHARE_SYNC_AND_FILE_CUSTODY_STATE_GAPS_1999_2015.md`；
- `docs/QQ_WEB_PRESENCE_ONLINE_AWAY_INVISIBLE_WATCHER_BADGE_AND_AVAILABILITY_STATE_GAPS_2000_2015.md`。

普通生活史主文档：

- https://github.com/tmzncty/how-people-lived/blob/main/topics/personal-calendars-reminders-shared-schedules-and-machine-addressable-future-china-1990s-2026.zh-CN.md

本文件只研究约 2005—2015 中文旧 Web 中与个人/共享日历直接有关的 artifact 与 state：

- Web calendar landing page；
- 月/周/日视图；
- 登录与账号；
- event / todo / reminder；
- recurring event；
- invitation / attendee；
- shared calendar；
- public/private visibility；
- `.ics` / iCalendar / calendar subscription；
- Web ↔ PC/client ↔ mobile synchronization；
- time-zone conversion；
- reminder delivery；
- event update/cancellation；
- shutdown/export/custody；
- archive replay 中“今天”与历史时间错位。

1998 iCalendar 等海外标准只作为直接技术前史和语义工具，不把本仓扩成全球 calendaring 史。

本仓更不会把 2020s 远程办公和“无会日”写进旧网主体；这些属于 `how-people-lived`。

核心问题：

> **一个 2009 年的 Web 月历截图，到底保存了多少“未来”？**

答案通常远少于看起来。

最重要的边界先写在前面：

```text
calendar landing page survives
!= historical account survives
!= event list survives
!= event payload survives
!= recurrence rule survives
!= reminder configuration survives
!= reminder actually fired
!= invitation reached attendee
!= attendee accepted
!= all synchronized clients converged
!= all clients displayed same local date/time
!= human remembered / attended the event
```

因此：

> **calendar UI != calendar transaction state != lived schedule**

---

# 1. 为什么 Web 日历是特殊的旧网对象：网页展示的不是“过去”，而是当时尚未发生的未来

普通文章页通常表达：

```text
某一时刻已经存在的内容
```

Web 日历却经常表达：

```text
过去某一时刻的人，对更晚时刻的计划
```

例如一个 2009-06-01 创建的事件：

```text
2009-06-01 记录
→ 2009-06-15 面试
→ 2009-06-14 提醒
→ 2009-06-15 修改地点
→ 2009-06-15 参加 / 未参加
```

archive 即使在 2009-06-10 抓到一张月视图，也只保存了整个事务的一帧。

后来如果事件被修改，旧 capture 可能保存一个已经失效的未来。

所以 Web calendar 的 artifact 具有天然的：

**future-state temporality / 未来状态时间性**。

研究时必须写清：

- page capture time；
- event start/end time；
- event creation time（若可见）；
- last-modified / sequence（若可见）；
- reminder trigger time；
- invitation/update time；
- archive fetch time；
- replay time。

这些时间不能混成一个 timestamp。

---

# 2. 研究单位：至少拆成 14 个对象

## 2.1 `platform`

例如：

- 365 日历；
- 中文 Web 门户内的日历服务；
- Google Calendar 的中文用户实践（作为比较/互操作对象）；
- PC/PDA calendar 与 Web 同步入口。

平台存在不等于某一历史功能存在。

---

## 2.2 `calendar_account`

账号是 calendar state 的 owner/container。

```yaml
calendar_account:
  provider: unknown
  identifier_observed: false
  authenticated: false
  creation_time: unknown
  active_at_capture: unknown
```

对私人普通人账号默认不重新发布 identifier。

---

## 2.3 `calendar_container`

一个账号可能有多个 calendar：

- personal；
- work；
- family；
- birthdays；
- shared team；
- subscribed public calendar。

需要区分：

```text
account
!= calendar
```

以及：

```text
calendar visible
!= calendar editable
```

---

## 2.4 `event_object`

典型字段可能包含：

```yaml
event:
  uid: unknown
  title: redacted
  dtstart: unknown
  dtend: unknown
  timezone: unknown
  all_day: unknown
  location: redacted
  description: redacted
  organizer: redacted
  attendees: redacted
  recurrence_rule: unknown
  sequence: unknown
  visibility: unknown
  status: unknown
```

研究普通生活时，应尽量保留结构而不是重新公布私人内容。

---

## 2.5 `todo_object`

待办和事件不是同一个东西。

```text
VEVENT = 通常绑定时间区间
VTODO = 可以只有截止时间 / 完成状态
```

一个旧 Web 页面写“待办事项”不能直接证明它使用 iCalendar VTODO；具体实现需另证。

---

## 2.6 `reminder_rule`

提醒是附着在 event/todo 上的未来触发规则。

可能包含：

```text
10 minutes before
1 day before
email
SMS
popup
client notification
```

需要单独保存：

```text
event exists
!= reminder exists
```

---

## 2.7 `invitation`

邀请不是“共享一个 URL”这么简单。

至少可能包含：

```text
organizer
attendee
request
response
accepted / declined / tentative
update sequence
cancellation
```

---

## 2.8 `permission_state`

共享日历至少可能有：

```text
private
free_busy_only
read_details
edit_events
manage_sharing
public
unknown
```

今天的权限名不能反投给历史产品。

只有同期 UI/帮助/协议证据才能确定具体状态集合。

---

## 2.9 `sync_client`

可能是：

- 浏览器；
- Thunderbird/Lightning；
- Outlook；
- Palm/PDA；
- Windows client；
- Android/iOS app；
- 桌面 widget。

每个 client 都可能拥有不同步状态。

---

## 2.10 `sync_endpoint`

不能看到“同步”二字就假定协议。

可能是：

- proprietary HTTP API；
- XML feed；
- CalDAV；
- Google-specific provider；
- import/export file；
- periodic polling；
- client-side local bridge。

需要同期证据。

---

## 2.11 `timezone_definition`

一个 event 的时间语义可能来自：

- UTC；
- fixed local time；
- named time zone；
- account default zone；
- device local zone；
- browser locale；
- server default zone。

这几层必须拆开。

---

## 2.12 `reminder_delivery_channel`

例如：

```text
browser popup
email
SMS
mobile push
client-local alarm
```

同一个 event 可能有多条 delivery channel。

---

## 2.13 `web_shell`

HTML/CSS/JS 只是用户看到的一层。

日历尤其依赖：

- AJAX；
- JSON/XML；
- authenticated APIs；
- client-side date calculation；
- browser local time；
- dynamic month navigation；
- server database。

所以：

```text
shell captured
!= event state captured
```

---

## 2.14 `archive_capture`

记录：

```yaml
capture:
  original_url: null
  capture_datetime: null
  http_status: null
  charset: null
  dom_recovered: false
  js_recovered: false
  ajax_routes_recovered: false
  authenticated_state: false
  event_payload_recovered: false
  replay_verified: false
```

没有这些字段时，不应写“复原了某年日历”。

---

# 3. 直接技术前史：RFC 2445 为什么对中文旧网考古有用

1998 年 RFC 2445 定义 iCalendar。

Source:

- RFC 2445, 1998-11: https://www.rfc-editor.org/info/rfc2445/

Evidence grade：**A / original Internet standards document**。

它不是 QQ/365/任何中文网站的实现说明。

不要写：

> 365 日历使用 RFC 2445。

除非拿到同期产品/协议证据。

但 RFC 提供了一套非常适合考古的 state vocabulary：

- event；
- todo；
- alarm；
- organizer；
- attendee；
- UID；
- sequence；
- recurrence；
- timezone；
- free/busy。

更重要的是，它明确区分三类 `DATE-TIME`：

```text
floating local time
UTC
local time + time-zone reference
```

因此以后看到历史页面里的：

```text
2009-02-02 08:00
```

必须继续问：

> **08:00 relative to which clock?**

---

# 4. 中国早期数字日程边界：PDA 的“计划”不能直接写成 Web calendar

2001 年《南方日报》PDA 指南把“通讯录、计划”列为 PDA 个人信息管理功能；部分设备另有浏览/Email 功能。

Source:

- 2001-07-12：https://tech.sina.com.cn/h/n/75588.shtml

Evidence grade：**B / contemporaneous buyer guide**。

这只能证明：

```text
local electronic schedule management available
```

不能证明：

```text
Web calendar available on same device
```

更不能证明：

```text
server sync / sharing / invitation
```

对 old Web 的边界意义是：

> **不要把“数字日历”与“Web 日历”合并。**

中国 2000s 初的普通人完全可能：

```text
纸本 + PDA local plan + occasional Internet
```

而不是一步跳进 cloud calendar。

---

# 5. 2008 第一人称：Web calendar 与本地客户端之间已经出现明确 handoff

2008-09-20，一名 cnBeta 投稿者记录自己把 Google Calendar 接进 Thunderbird。

Source:

- https://www.cnbeta.com.tw/articles/soft/65181.htm

Evidence grade：**B / contemporaneous first-person technical practice**。

文章给出的链条包括：

```text
Thunderbird
→ install Lightning
→ install Provider
→ open Google Calendar account settings
→ copy XML URL
→ create network calendar in Thunderbird
→ save login credential
→ sync
```

这条材料对于 old Web 非常好，因为它清楚证明：

```text
browser page
!= whole calendar system
```

真实事务跨过：

```text
Web account
→ authenticated feed / endpoint
→ local extension
→ local client cache
→ displayed event
```

Archive 如果只保存 Google Calendar 的设置页，仍无法证明 Thunderbird 当时真正成功收到了哪一个事件。

---

# 6. 365 日历作为 2008—2015 中文 Web/calendar case

## 6.1 证据边界

当前 365 日历产品页自述“从 2008 年到现在”。

Source:

- https://apps.apple.com/cn/app/365%E6%97%A5%E5%8E%86-%E4%B8%87%E5%B9%B4%E5%8E%86/id642101382

Evidence grade：**C for founding-history self-description; current platform page**。

不能仅凭当前页面复原 2008 UI。

但我们有 2012 同期材料。

---

## 6.2 2012 服务条款：平台与 Web 服务在该时点可确认存在

365 日历服务条款顶部明确标注：

> 生效日：2012 年 6 月 20 日。

Source:

- https://www.365rili.com/v4/service.html

Evidence grade：**A for contemporaneous service/terms existence**。

可证明：

- 当时有对应网站服务；
- 服务主体和用户关系有正式条款。

不能证明：

- 某一用户使用；
- 用户量；
- 某一个功能在历史 UI 中如何实现；
- 后端提醒是否可靠。

---

## 6.3 2012 少数派：跨平台、提醒、共享、云端备份已经是可观察产品形态

2012-10-12 少数派文章标题是：

> 《平台可以不同，时间必须一致：365日历》

Source:

- https://sspai.com/post/15191

Evidence grade：**B / contemporaneous third-party product review**。

文章列出：

- 日程提醒；
- 待办；
- 小组日历；
- 日程共享；
- 云端备份；
- Google 同步；
- Web/PC/移动入口。

这至少可以建立 2012 的**产品 claim envelope**。

仍然要坚持：

```text
review says feature available
!= feature used by all users
!= backend semantics recovered
```

---

# 7. 状态机 A：账号与 calendar container

```text
NO_ACCOUNT
→ ACCOUNT_CREATED
→ LOGIN_VALID
→ CALENDAR_CREATED / DEFAULT_CALENDAR_EXISTS
→ EVENTS_ADDED
→ SHARING_OPTIONAL
→ SYNC_CLIENTS_OPTIONAL
→ ACCOUNT_DORMANT
→ ACCOUNT_DISABLED / SERVICE_EXIT / UNKNOWN
```

每个 transition 都需要不同证据。

### archive 常见错觉

登录页存在只证明：

```text
login shell exists
```

不证明：

```text
historical account database still exists
```

更不证明：

```text
ordinary user calendar state survives
```

---

# 8. 状态机 B：event object 生命周期

推荐最小状态：

```text
DRAFT
→ SAVED
→ ACTIVE
→ UPDATED
→ CANCELLED / DELETED
```

若有 sync：

```text
SAVED_SERVER
→ PENDING_SYNC
→ SYNCED_TO_CLIENT_A
→ SYNCED_TO_CLIENT_B
```

问题是：

```text
client_A at sequence=4
client_B at sequence=3
```

此时“同一个事件”已经存在多个现实。

所以：

```text
same UID
!= same revision
```

---

# 9. 状态机 C：reminder 并不是 event 的天然属性

```text
EVENT_EXISTS
→ REMINDER_CONFIGURED
→ TRIGGER_TIME_REACHED
→ REMINDER_JOB_ENQUEUED
→ CHANNEL_ACCEPTED
→ DELIVERED_TO_DEVICE/MAILBOX
→ DISPLAYED
→ HUMAN_NOTICES
→ HUMAN_ACTS / DISMISSES / SNOOZES
```

Archive 通常最多看到：

- UI 有“提醒”字段；
- 帮助页说可以提醒。

它几乎无法证明：

- 某用户某次提醒真实入队；
- SMTP/SMS/push 成功；
- 用户实际看到。

所以必须固定：

```text
reminder feature exists
!= reminder configured
!= reminder fired
!= reminder delivered
!= reminder noticed
```

---

# 10. 状态机 D：邀请不是一封普通通知

```text
EVENT_CREATED
→ ATTENDEE_ADDED
→ INVITATION_GENERATED
→ SENT
→ DELIVERED
→ OPENED
→ ACCEPTED / DECLINED / TENTATIVE
→ RESPONSE_REACHES_ORGANIZER
→ ORGANIZER_VIEW_UPDATED
```

随后还可能：

```text
EVENT_UPDATED
→ UPDATE_SENT
→ SOME_ATTENDEES_UPDATED
→ OTHERS_STALE
```

以及：

```text
EVENT_CANCELLED
→ CANCEL_SENT
→ CANCEL DELIVERED / LOST
```

因此旧网截图里“Participants: 5”不能直接证明 5 个人都接受。

---

# 11. 状态机 E：共享日历权限

共享不是二值。

研究字段建议：

```yaml
sharing:
  public_listing: unknown
  can_see_free_busy: unknown
  can_read_details: unknown
  can_edit_events: unknown
  can_manage_sharing: unknown
  link_secret_required: unknown
  login_required: unknown
```

历史 UI 可能使用完全不同的权限词。

这里是研究抽象，不是声称 365/Google 当时恰好使用这些 enum。

### 为什么重要

2020 年以后普通用户仍会要求“管理员看全部，其他人只看自己被安排的日程”。

这说明日历内容具有工作与隐私双重属性。

对旧网同样不能把“共享日历”写成“所有内容公开”。

---

# 12. 状态机 F：sync 不是开关，而是分布式状态

```text
LOCAL_CREATE
→ LOCAL_QUEUE
→ NETWORK_REQUEST
→ SERVER_ACCEPTS
→ SERVER_REVISION
→ OTHER_CLIENT_POLLS/PUSHED
→ REMOTE_WRITE
→ LOCAL_APPLIES
```

失败点：

- offline；
- auth expired；
- feed URL changed；
- plugin incompatible；
- conflict；
- clock/timezone mismatch；
- server rejects；
- stale cache；
- partial sync；
- recurrence semantics differ。

因此：

```text
sync enabled
!= sync succeeded
!= all devices converged
```

2008 Thunderbird 第一人称文章尤其适合证明“同步”当时可能依赖：

- 第三方扩展；
- provider plugin；
- XML URL；
- 保存 Web account credential。

只保存浏览器端页面远远不够。

---

# 13. 状态机 G：时区转换

至少拆：

```text
EVENT_SEMANTIC
→ STORED DATETIME
→ ASSOCIATED TIMEZONE
→ SERVER SERIALIZATION
→ CLIENT PARSE
→ CLIENT LOCAL ZONE
→ DISPLAYED WALL TIME
```

这条链里任何一步变化都可能出现：

```text
same event
→ different displayed date
```

2020 年 365 日历 App Store 的用户评论提供了一个后续行为证据：北京时间 2 月 2 日 8am 分享给美国朋友后，对方看到前一日当地时刻，用户认为这对跨国共享造成麻烦。

Source:

- https://apps.apple.com/cn/app/365%E6%97%A5%E5%8E%86-%E4%B8%87%E5%B9%B4%E5%8E%86/id642101382

Evidence grade：**B-/later first-person evidence; used only to identify a semantic hazard, not to back-project a 2010 bug**。

这个 2020 证据不能证明 2012 版本存在同样 bug。

它的作用只是告诉考古者：

> **historical time-zone semantics must be verified, not assumed.**

---

# 14. recurring event：一条规则可以生成无限多个未来对象

这是 archive 最容易低估的部分。

例如：

```text
RRULE:FREQ=WEEKLY;BYDAY=MO
```

可能代表长期重复事件。

一个 2010 年 5 月截图只显示：

```text
5/3 meeting
5/10 meeting
5/17 meeting
```

但真正的数据对象可能只是：

```text
DTSTART + RRULE
```

因此：

```text
visible occurrence
!= stored recurrence rule recovered
```

反过来也一样：

```text
RRULE recovered
!= every historical occurrence actually happened
```

用户可能跳过、例外取消、修改某一次。

推荐额外记录：

```yaml
recurrence:
  rrule_seen: false
  rdate_seen: false
  exdate_seen: false
  single_instance_override_seen: false
  expansion_engine_known: false
```

---

# 15. `calendar-present drift / 日历“今天”漂移`

Web calendar 有一个非常特殊的 archive 问题。

页面可能通过 JavaScript 或服务器动态计算：

```text
today
current month
current timezone
current countdown
```

如果 archive 在 2026 年 replay 一份 2010 页面，而脚本在回放环境里重新执行：

```text
HTML capture = 2010
JS computes today = replay/current environment
```

就可能出现：

> **历史页面骨架在 2010，但“今天”却跑到了另一个日期。**

本文件称之为：

**calendar-present drift / 日历“今天”漂移**。

与它相反，archive 也可能把当时的“今天”静态冻住。

于是有两种不同错觉：

### 类型 A：today petrification

2010-05-01 的红框“今天”被永久保存。

后人误以为页面本身就是 5 月 1 日内容，而没有记录 capture 时间。

### 类型 B：today drift

页面 HTML 是 2010，但 JS 重新算 current date。

后人看到完全不可能属于 2010 的“今天”。

因此任何历史 calendar screenshot 都要同时记录：

- capture datetime；
- replay datetime；
- browser/system clock；
- script execution status；
- dynamic date source。

---

# 16. `future-object orphaning / 未来对象孤儿化`

有时 archive 保存：

- 分享 URL；
- 邮件中的 event link；
- `.ics` 下载链接；
- 页面上的 event title；

但后端 event object 已不可访问。

于是出现：

```text
reference survives
→ target future object gone
```

称为：

**future-object orphaning**。

它和旧网图片的 broken image 类似，但语义更复杂：

图片丢失意味着一个媒体对象不见；

日程对象丢失可能意味着：

- 时间；
- 地点；
- 参与者；
- 修改历史；
- 取消状态；
- 提醒；

整套未来承诺一起消失。

---

# 17. Web calendar artifact family

研究一个 2008–2015 中文 Web calendar，至少寻找以下 artifact families。

## 17.1 Public landing

- 产品首页；
- 功能介绍；
- 登录入口；
- 注册入口；
- download/client links。

## 17.2 Calendar shell

- month/week/day tabs；
- today button；
- previous/next；
- add event；
- side mini-calendar；
- timezone display；
- lunar date display（若有）。

## 17.3 Event editor

- title；
- date/time；
- all-day；
- repeat；
- reminder；
- location；
- notes；
- visibility；
- attendees。

## 17.4 Reminder editor

- channel；
- offset；
- snooze；
- repeat alarm。

## 17.5 Sharing / invitation

- email/IM invite；
- public link；
- group calendar；
- permission controls。

## 17.6 Import/export

- `.ics`；
- XML；
- CSV；
- proprietary backup；
- subscription URL。

## 17.7 JS/API resources

- XHR endpoints；
- JSON/XML payload shape；
- date parsing；
- recurrence handling；
- time-zone library；
- auth/session requirements。

## 17.8 Client handoff

- desktop app；
- mobile app；
- Thunderbird/Outlook plugin；
- widget；
- protocol/URL handler。

---

# 18. Claim ladder：Web 日历尤其不能从 `exists` 跳到 `used`

## Exists

可证明服务/页面/功能在某时点存在。

例：2012 服务条款 + 同期产品评论。

## Available

必须继续证明：

- 普通用户可注册；
- 地域可达；
- 浏览器/系统兼容；
- 收费门槛；
- 是否需要特定手机/客户端。

## Used

需要：

- 同期第一人称；
- 用户评论；
- 日记/论坛；
- 可信日志/统计。

2008 cnBeta 投稿可以证明**至少一名中文互联网用户**实际执行过 Google Calendar ↔ Thunderbird 同步。

## Popular

需要独立统计或多源证据。

厂商“千万用户”不能单独完成这一步。

## Caused

“日历让中国人更忙”“共享日历导致加班”都是很强的因果结论。

必须结合：

- 时间使用；
- 职业制度；
- 组织管理；
- 对照材料；

不能由功能表推出。

---

# 19. 2012 365 日历厂商规模数字如何处理

2012 年有厂商/推广材料声称大量用户、同步和提醒次数。

这类数字即使同期，也只能记作：

```yaml
source_type: vendor_claim
independent_verification: absent
use_for: scale_claim_as_claim
not_for: population_estimate
```

不要写：

> “2012 年中国已有 X 千万普通人日常使用云日历。”

除非有独立调查。

这是 `popular` claim ladder 的典型案例。

---

# 20. Browser / charset / client environment

Web calendar 比静态网页更依赖执行环境。

记录：

```yaml
client_environment:
  browser: unknown
  browser_version: unknown
  os: unknown
  charset_header: unknown
  meta_charset: unknown
  javascript_required: unknown
  cookies_required: unknown
  local_storage_required: unknown
  timezone_source: unknown
  plugin_required: unknown
```

2008 Thunderbird 同步又需要独立记录：

```yaml
external_client:
  product: Thunderbird
  extension: Lightning
  provider_extension: present
  remote_calendar_url: redacted
  credential_storage: reported
```

不要把浏览器和客户端混成一个 artifact。

---

# 21. Charset 与日期格式不是小问题

中文日历可能同时出现：

- `2008-09-20`；
- `2008年9月20日`；
- `9/20`；
- 星期；
- 农历；
- 节气；
- 全天事项；
- 12/24 小时制。

若编码错误、脚本丢失、locale 改变，可能导致：

- 标题乱码；
- 星期错位；
- 月份数字歧义；
- 日期 parser 错误；
- 农历字段无法复现。

因此旧网日历不是“抓到文字就算成功”。

---

# 22. Browser page time 与 server event time 必须分开

与授时专题交叉时，要记录：

```text
server clock
browser clock
account timezone
calendar timezone
event timezone
archive capture time
replay machine time
```

不能从：

```text
页面显示 20:00
```

直接推出：

```text
server stored 20:00 local
```

更不能推出：

```text
human intended 20:00 in that zone
```

---

# 23. Preservation levels：C0–C7

为 Web calendar 定义单独 preservation ladder。

## C0 — locator / mention only

只有：

- URL；
- 新闻；
- 产品名称；
- 搜索结果。

不能描述页面结构。

## C1 — public landing shell

保存：

- 产品首页；
- 登录/注册入口；
- 功能说明。

可证明服务界面存在。

## C2 — calendar UI structure

保存：

- 月/周/日视图；
- navigation；
- event editor shell；
- reminder/share controls。

可以描述 artifact，但不能声称真实事务成功。

## C3 — executable public client resources

保存：

- JS/CSS；
- API route references；
- date/time parsing；
- event form submission shape；
- charset/browser dependencies。

仍不要求真实私人账号。

## C4 — synthetic transaction reconstruction

在合法、安全、非生产隐私环境里，以 synthetic event 验证：

```text
create
edit
repeat
remind
share
cancel
```

必须标：

**RECONSTRUCTION / not historical live account**。

## C5 — sync/import/export semantics

至少确认：

- import/export format；
- subscription；
- client sync relation；
- known versioning/conflict semantics。

## C6 — time semantics

确认：

- account/event timezone；
- floating vs absolute（若适用）；
- recurrence；
- all-day；
- daylight/locale handling。

## C7 — privacy-preserving transaction evidence model

最高等级并不要求取得真实普通用户日历。

它要求能说明：

- 哪些 backend state 存在；
- 哪些状态 archive 永远看不到；
- 哪些私人数据不应收集；
- 哪些行为只能保持 unknown。

因此：

> **C7 does not mean “publish a person’s calendar.”**

它意味着对系统边界和不可见性有完整认识。

---

# 24. 本轮 archive 尝试

本轮尝试寻找：

- `365rili.com` 约 2008–2010 的历史入口；
- Web calendar 早期 UI；
- 可核验的 Wayback replay / CDX 结果。

当前工具访问链中，直接构造历史 Wayback/CDX URL 被 URL 安全限制拒绝；公开普通 Web 搜索没有在本轮返回一份能够完整核验以下字段的历史 memento：

```text
capture_datetime
original_url
HTTP status
charset
DOM
JS
AJAX endpoint
historical calendar shell
historical event editor
```

因此严格记录：

```text
M1 verified historical Web-calendar capture:
NOT ACHIEVED IN THIS SLICE
```

这**不等于**：

```text
Wayback did not preserve 365rili.com
```

也不等于：

```text
no historical capture exists
```

只是本轮访问链没有验证成功。

符合 `docs/METHOD.md`：

> archive locator / search hint != verified capture。

---

# 25. Negative evidence：什么能写，什么不能写

可以写：

> 本轮未验证到 2008–2010 365 日历历史 replay。

不能写：

> 365 日历 2008–2010 没有被 archive 保存。

可以写：

> 当前公开页面无法证明某历史提醒真实投递。

不能写：

> 当时提醒系统经常失败。

可以写：

> 私人 event state 通常不会进入公开 archive。

不能写：

> 用户当年没有使用这个功能。

---

# 26. Privacy：calendar archaeology 不应变成生活轨迹曝光

私人日历可能直接包含：

- 姓名；
- 邮箱；
- 手机；
- 住址；
- 医院；
- 疾病；
- 面试公司；
- 宗教活动；
- 政治活动；
- 性/亲密关系；
- 儿童学校；
- 家庭成员；
- 财务截止；
- 旅行计划。

因此默认策略：

```text
public product docs > public help > public demo > synthetic reconstruction
```

而不是：

```text
hunt private calendar dump
```

即使 archive 意外保存 authenticated/private material，也不应因为“历史价值”就重新传播普通人的完整轨迹。

---

# 27. Screenshot trap：一张月视图最多证明什么

截图可以证明：

- 某 UI layout；
- 当时显示的 visible cells；
- 某些可见 event labels（若合法公开）；
- today marker；
- buttons/icons。

它不能证明：

- event database 完整内容；
- reminder backend；
- attendees 的 acceptance；
- sync status；
- hidden calendars；
- future modifications；
- event actually happened。

因此：

```text
screenshot = representation evidence
not transaction ground truth
```

---

# 28. `.ics` survives != historical account survives

如果 archive 保存一个 `.ics` 文件，它可能提供非常强的对象证据：

- UID；
- DTSTART；
- DTEND；
- RRULE；
- timezone；
- organizer；
- sequence。

但仍要注意：

```text
export snapshot
!= live account state
```

文件可能：

- 是旧版本；
- 后来 event 被取消；
- attendee 状态已变；
- private field 被删；
- client import 后产生另一份副本。

因此 `.ics` 是**event serialization evidence**，不是整个平台事务真相。

---

# 29. `free/busy` 是一个重要但容易忽略的隐私中间层

完整公开日历不是唯一共享方式。

Internet calendaring 很早就有 free/busy 概念：

```text
别人只知道你这段时间忙
→ 不知道你为什么忙
```

这是：

**coordination without full disclosure**。

对中文旧 Web 若发现类似功能，应特别记录。

因为它直接连接今天的防守问题：

> **组织可以协调时间，不代表必须知道私人事件内容。**

---

# 30. `calendarization` 不应被误写成“所有人的生活都精确到分钟”

旧 Web 研究容易过度选择：

- IT 用户；
- 白领；
- 高校；
- 互联网公司；

因为这些群体的日历教程和网页最容易留下。

而 2008 年大量普通生活仍可能依靠：

- 纸日历；
- 手机闹钟；
- 短信；
- QQ 消息；
- 单位通知；
- 家人提醒；
- 记忆。

因此：

```text
archive-visible calendar users
!= representative population
```

尤其不要把早期技术社区的 Google Calendar/Thunderbird 同步经验写成全国普通家庭基线。

---

# 31. 与“未来想象”的交叉：产品功能本身只能提供弱证据

2012 年“平台可以不同，时间必须一致”可以作为同期技术愿望的一条文本证据。

它显示一种扩张式期待：

> **人可以换平台，但计划最好持续。**

但它不能单独证明：

- 用户相信未来更乐观；
- 用户一定更想跳槽/迁移；
- 中国青年普遍拥有长期计划。

这类大结论必须回到 `how-people-lived`，结合：

- 第一人称未来计划；
- 就业/住房/婚姻材料；
- 统计；
- 生命史。

old-web 只提供基础设施与 artifact 边界。

---

# 32. 一个可复用的 Web calendar capture 记录模板

```yaml
case_id: CAL-YYYY-NNN
platform:
  name: null
  service_start_claim: null
site:
  hostname: null
  url: null
capture:
  archive: null
  capture_datetime: null
  original_url: null
  http_status: null
  replay_verified: false
  charset: null
browser_environment:
  browser: unknown
  javascript: unknown
  cookies: unknown
  system_timezone: unknown
page:
  type: unknown
  month_view: false
  week_view: false
  day_view: false
  event_editor: false
  reminder_ui: false
  sharing_ui: false
account:
  authenticated: false
  identity_redacted: true
event:
  synthetic: null
  uid_seen: false
  timezone_seen: false
  recurrence_seen: false
  reminder_seen: false
  attendee_seen: false
sync:
  endpoint_seen: false
  protocol_identified: false
  client_identified: false
preservation_level: C0
claims:
  exists: unknown
  available: unknown
  used: unknown
  popular: unknown
  caused: unknown
privacy:
  private_user_data_republished: false
notes: null
```

---

# 33. 本轮最重要的新旧网认识论结论

### 33.1 `visible future != executable future`

页面写着“明天 9:00”，不证明提醒、邀请或现实行动会成功。

### 33.2 `event object != occurrence`

重复规则会生成多个 occurrence；截图只看到其中一部分。

### 33.3 `same UID != same revision`

多端同步会出现 stale copy。

### 33.4 `same event != same local date`

时区转换可能跨日。

### 33.5 `today is an executable value`

“今天”可能来自脚本、server 或 browser clock；archive replay 会漂移或石化。

### 33.6 `future object is private history`

一个人的旧日历不是普通“网页内容”，而是高度敏感的生活轨迹。

---

# 34. 反例与尚未确定

## 反例 A：日历 UI 可以完全静态

不是所有历史日历页都依赖复杂 JS/backend。

某些只是公共节假日/万年历页面。

不能把所有“日历”都按私人 Web calendar 建模。

## 反例 B：提醒可以完全本地执行

事件可能从 Web 同步一次，此后 alarm 在本机触发。

所以 server 没有 reminder job 不等于用户没有提醒。

## 反例 C：分享链接可以是公开只读页面

不一定有 organizer/attendee RSVP。

“共享”与“邀请”必须分开。

## 反例 D：sync 也可能只是手动 export/import

不能因为两端都有同一事件就推断实时同步。

### 尚未确定

1. 365 日历 2008–2011 Web UI 的可验证 historical capture；
2. 当时是否以及何时支持 `.ics` / XML / proprietary feed，各版本需逐年查证；
3. 早期中文个人门户/邮箱 calendar 的服务谱系；
4. 2005–2010 中国普通用户 calendar 使用率；
5. Web 日历 reminder 中 Email/SMS 的真实 delivery semantics；
6. 农历 recurring birthday 的历史实现；
7. 2010s 初不同 Android/iOS/PC clients 的 conflict resolution；
8. platform shutdown/export 是否造成 calendar-memory loss。

---

# 35. 与相邻 old-web 专题的分界

## 与授时专题

授时回答：

```text
机器现在几点？
```

本篇回答：

```text
机器怎样保存“未来几点要做什么”？
```

## 与 online storage

存储专题回答：

```text
文件对象是否持久、同步、可导出？
```

本篇回答：

```text
未来事件是否持久、同步、可解释？
```

## 与 QQ presence

presence 专题回答：

```text
某一刻人是否可见/可联系？
```

本篇回答：

```text
还没到的某一刻是否已经被预先占用/提醒？
```

---

# 36. 建议下一步可做的 bounded archaeology

优先顺序：

1. 搜索 2008–2010 `365rili.com` 历史公开 landing/login/help capture；
2. 验证一个明确 capture 的 `capture_datetime / HTTP / charset / DOM / JS`；
3. 查当时公开帮助页中的 event/reminder/share 字段；
4. 找一个同期公开 synthetic/demo calendar，而不是私人账号；
5. 搜索 `.ics` / XML / calendar subscription 的公开 sample；
6. 若拿到安全公开样本，建立 event state fixture；
7. 验证 `today` 是 server-rendered 还是 JS-computed；
8. 对 archive replay 记录系统时间与 capture 时间，检查 calendar-present drift。

完成第 2 步以前，不升级 M1。

---

# 37. 一句结论

> **旧 Web 日历最容易骗研究者的地方，是它看起来像一张静态月历。实际上，一个真正能改变生活的网络日历是一套分布式未来状态：服务器保存事件，客户端保存副本，时区决定显示，重复规则生成尚未发生的实例，邀请和取消在多人之间传播，提醒还要等未来某一刻才触发。Archive 往往只冻住最外面那一层网格。研究的任务不是把网格截图得更漂亮，而是明确指出：哪些未来状态真的被保存了，哪些在后端、设备、时间和私人生活里已经不可见。**
