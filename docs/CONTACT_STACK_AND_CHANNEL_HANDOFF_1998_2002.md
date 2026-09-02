# CONTACT_STACK_AND_CHANNEL_HANDOFF_1998_2002.md

## 目的与 scope

本文件处理 1998–2002 中文旧网里一个很容易被 Web archive 误读的问题：

> **一个网页上的“联系方式”或一条留言，究竟是完整的在线互动，还是一条电话 / BP 机 / 手机 / Email / OICQ / 线下链路中的某一跳？**

这不会把 `old-web-archaeology` 的研究对象扩展成完整的中国寻呼史。BP 机、电话等非 Web 系统只在它们**直接被中文 Web 页面编码、调用或桥接**时进入本仓。

相关普通生活史主文档：
https://github.com/tmzncty/how-people-lived/blob/main/topics/contact-stacks-channel-handoffs-and-mobile-reachability-china-1998-2002.zh-CN.md

---

## 1. 不要把早期网页想成一个封闭的“线上世界”

1990 年代末到 2000 年代初，一个网页可能只承担：

- 发现某个人；
- 留下一条异步消息；
- 显示 Email / ICQ / OICQ / BP / 电话等联系方式；
- 请求对方改用另一种媒介联系；
- 约定后续的电话或线下见面。

因此：

> **web-mediated interaction ≠ web-contained interaction**

Archive 保存了 Web 页，不等于保存了完整的社会互动。

---

## 2. 同时代 OICQ 教程证明“联系栈”是当时真实存在的用户模型

2000 年 4 月 14 日，《软件世界》在新浪科技发表《中文网络寻呼机--OICQ》。文章开头直接把一个人的通讯录想成多种联系方式并存：

- 电话；
- BP 机；
- 手机；
- E-mail；
- 随后再增加 ICQ。

同文把 Open ICQ / OICQ 描述为中文“虚拟网络寻呼机”，并列出搜索在线用户、实时信息、语音交流和无线寻呼等能力。

来源：
https://tech.sina.com.cn/soft/2000-04-14/133.html

### 可以证明

- 2000 年的产品/教程语境里，电话、BP、手机、Email、ICQ 被理解成可以并存的联系人入口；
- OICQ 当时被描述为可与无线寻呼发生桥接；
- “网络寻呼”不是后来的怀旧命名，而是同期产品语汇。

### 不能证明

- 每个用户都有这五类联系方式；
- 无线寻呼功能被广泛使用；
- 某个具体版本在所有地区支持同一寻呼网络；
- OICQ 出现后 BP 机立即退出。

所以应记录为：

```text
feature exists / contemporary representation exists
≠ widespread use
≠ replacement of old medium
```

---

## 3. 2000 年幸存留言簿：Web → pager 的真实通道切换痕迹

`sickbaby.org` 当前保存一组内部时间戳为 2000 年的旧留言簿页面：

https://www.sickbaby.org/undesay18.htm

其中一条标记 **2000-10-05** 的留言询问朋友是否仍在长沙，并留下寻呼联系方式，请对方看到网页留言后通过 BP 机联系，同时提到共同朋友也想念对方。

本仓不复制原号码、邮箱或其他不必要的普通人身份字段。

这个 artifact 很适合说明：

```text
guestbook page
→ later page visit
→ pager alert / contact
→ likely phone or offline continuation
```

### 证据级别

建议暂标：

```yaml
evidence_grade: A-like
artifact_status: surviving-page-with-contemporary-internal-timestamp
hosting_continuity_verified: false
byte_identity_verified: false
```

也就是说，它是极有价值的同期内容痕迹，但在没有 Wayback/WARC/hash/历史镜像交叉核验前，不应声称当前 HTTP 对象就是未经修改的 2000 年原始字节。

---

## 4. 新研究单位：contact stack

旧网页中的联系人字段不要逐项孤立解释。

建议记录：

```yaml
contact_stack:
  observed_on_page:
    - email
    - icq
    - oicq
    - pager
    - mobile
    - home_phone
    - work_phone
    - homepage
  field_presence_time: unknown
  endpoint_value_preserved_in_research: false
  person_identity_verified: false
```

`contact_stack` 的目标不是收集号码，而是回答：

> **这个页面把一个人建模成拥有多少种可切换的通信入口？**

这会直接连接到平台形态史：个人主页、BBS profile、博客侧栏、SNS 个人资料页都可能拥有不同的联系人 schema。

---

## 5. 新研究单位：channel handoff

当内容明确要求“改用另一种媒介联系”时，建议单独建模：

```yaml
channel_handoff:
  discovery_medium: web-guestbook
  initial_message: asynchronous-web-message
  next_endpoint_type: pager
  reply_medium: unknown
  offline_followup: unknown
  captured_stages:
    - web-message
    - pager-endpoint-mentioned
  missing_stages:
    - pager-delivery
    - callback
    - conversation
    - offline-meeting
  endpoint_redacted: true
```

常见历史链可能包括：

```text
Web → Email
Web → BP → phone
BBS → OICQ
homepage → ICQ
Email → pager
OICQ → wireless paging
Web → phone → offline meeting
```

但**只记录证据实际支持的跳数**。不要因为一种链“很合理”就补齐缺失段。

---

## 6. 必须把“联系方式字段”拆成至少五个不同 claim

一个旧 profile 出现 `BP机` 字段时，至少有以下五层：

1. `field_exists`：页面/schema 有这个字段；
2. `field_filled`：这个账号填了值；
3. `endpoint_valid_at_time`：该端点当时真实有效；
4. `endpoint_owned_or_controlled_by_account_holder`：确实由此人控制；
5. `endpoint_used_for_observed_interaction`：我们有证据看到它真的参与了一次联系。

因此：

> **field exists ≠ field filled ≠ endpoint valid ≠ identity verified ≠ endpoint used**

这条规则尤其重要，因为旧网页经常把大量字段默认渲染出来，即使用户从未填写。

---

## 7. 一个重要的 schema dating 陷阱

一些今天仍然可访问的早期中文个人主页/个人档案页面，会同时显示：

- 一个很早的“注册日期”；
- 当前页面模板里的 ICQ / OICQ / 手机 / BP / 电话等字段。

这很容易诱导研究者写：

> “该平台在注册日期当年就已经有 BP 机字段。”

这是不成立的。

当前渲染模板可能多年后改过，而账号注册时间只是账户元数据。

所以：

> **account registration date ≠ profile-schema date**

若要证明某平台在 2002 年就提供某字段，需要：

- 2002 年 archive capture；
- 同期帮助页/注册表单；
- 同期用户教程或截图；
- 其他可定位的 schema 证据。

不能只靠今天幸存页面中“注册于 2002”+“现在显示 BP 字段”的组合。

---

## 8. 联系方式字段的功能角色也要分开

同一种页面可以同时包含不同角色的端点：

### discovery

让陌生人第一次找到你：

- 主页 URL；
- BBS 帐号；
- 搜索结果；
- 公开 Email。

### alert / interrupt

把“有人找你”送到移动中的人：

- BP 机；
- 手机短信；
- 部分网络寻呼。

### conversation

适合持续交换信息：

- 电话；
- ICQ/OICQ；
- chat room；
- Email（异步）。

### persistent identity

让关系跨地点/终端继续：

- Email address；
- ICQ/OICQ number；
- stable username。

### offline coordination

把网络互动导向现实地点：

- 电话确认；
- BP 回呼；
- 时间/地点留言。

因此看到多个联系人字段时，不要把它们当作完全同质的“联系方式”。

---

## 9. Archive asymmetry：Web archive 天然只保存通信链的一边

一个 archive capture 可能完整保存：

- “请呼我”；
- “给我打电话”；
- “发邮件给我”；
- “晚上上 QQ”；
- 一个 profile 的联系方式框。

但通常无法保存：

- BP 系统实际投递记录；
- 电话回拨；
- 手机短信；
- 私人 ICQ/OICQ 会话；
- 约定后的见面；
- 后来换号通知；
- 从未进入 Web 的关系。

因此：

> **archived front-end contact surface ≠ complete social relation**

这和本仓已有两条规则直接相连：

- `platform-mediated tie ≠ platform-originated tie`；
- `archived web page ≠ web-native historical content`。

现在还要增加：

> **archived web message ≠ complete communication chain**。

---

## 10. 隐私：研究 contact schema，不重新出版 contact database

历史联系方式极容易被“旧网考古”不必要地重新公开。

默认规则：

- 研究字段类型时只记录 `pager / phone / email / OICQ`，不复制值；
- 普通用户的历史 BP 机号、手机、家庭电话、Email 不进入公开数据集，除非具体数字本身对关键 claim 不可替代；
- 引用留言时尽量摘要，不把号码再次转录；
- 不尝试拨打、添加、验证仍可能属于个人的旧号码/帐号；
- 不通过多个旧页面拼出普通人的现实身份；
- 不把联系人表做成可检索的历史个人数据库。

推荐：

```yaml
contact_endpoint_type: pager
endpoint_value_observed: true
endpoint_value_republished: false
privacy_action: redacted
```

---

## 11. 海外比较只用于确认机制，不扩张本仓 scope

1998 年美国 BellSouth Wireless Data 的 Interactive Paging Service 已让 RIM Inter@ctive Pager 950 收发 paging 和 E-mail；同年 *Wired* 报道 Fujitsu ByeDesk 可以把 Email 和 Web 页面更新转发到手机/pager，并把移动设备消息经服务器送回 Internet。

来源：
https://www.wirelessdesignonline.com/doc/bellsouth-launches-interactive-paging-service-0001

https://www.wired.com/1998/09/email-email-everywhere/

它们说明“Internet 与寻呼/移动设备互相桥接”不是中国独有。

但这些材料只承担**比较机制**：本仓不会因此开始系统研究美国 pager / BlackBerry 前史；完整跨国生活史应写在 `how-people-lived`。

---

## 12. 建议加入 case/evidence 的字段

```yaml
contact_surface:
  page_type: profile|guestbook|homepage|forum-post|help-page
  observed_contact_fields:
    - email
    - pager
    - oicq
  schema_date_verified: false

channel_handoff:
  source_medium: web
  destination_medium: pager
  explicit_handoff: true
  followup_observed: false

endpoint_evidence:
  endpoint_type: pager
  value_observed: true
  value_republished: false
  validity_at_observed_time: unknown
  identity_linkage: unverified

archive_limits:
  captures_web_message: true
  captures_pager_delivery: false
  captures_callback: false
  captures_offline_followup: false
```

---

## 13. Evidence grades

### A-like — surviving contemporaneous-content artifact

**sickbaby.org，内部日期 2000-10-05**

用途：

- Web 留言明确请求转向 pager；
- 证明一次跨媒介 handoff 至少在幸存同期内容中出现。

限制：

- hosting continuity 未证；
- 当前页面可能是后来整理/迁移后的 surviving copy；
- 不重新发布 endpoint 值。

### B — 同时代产品/教程证据

**《软件世界》/新浪科技，2000-04-14，《中文网络寻呼机--OICQ》**

用途：

- 同时出现电话、BP、手机、Email、ICQ 的 contact-stack representation；
- OICQ 无线寻呼 feature claim。

限制：

- 不能证明使用率；
- 不能自动推出每版/每地能力一致。

### B — 海外同时代比较

**BellSouth 1998；Wired/Fujitsu 1998**

用途：Internet/pager convergence 的独立跨国比较。

限制：产品、用户群和网络结构与中国不同。

---

## 14. 尚未确定

- 中文个人主页/BBS/SNS 各平台最早何时增加、何时删除 `BP机` 字段；
- OICQ→无线寻呼的具体协议、合作寻呼台和覆盖；
- guestbook → pager → phone 这种 handoff 的频率；
- 哪些 Web profile 字段只是模板遗留、已经无人使用；
- pager 字段消失与手机/QQ 普及之间的精确时间关系；
- archive 是否系统性高估“公开联系方式多”的用户，并低估纯线下/电话关系；
- 平台改版是否会把新 contact schema 套到老帐号页面，从而制造 false historical UI。

这些问题以后适合通过 1998–2005 的 Wayback profile/register/help captures 做版本级 schema archaeology。

---

## 15. 这条规则改变了什么？

以后看到一张 2000 年个人主页，不再把它理解成一个自足的“网络身份页面”。

更稳妥的模型是：

> **旧网页可能只是一个人的社会路由器面板。**

它告诉访客：

- 从哪里发现我；
- 怎样叫到我；
- 怎样和我长聊；
- 如果这个入口失效，还可以换哪一条路。

而历史档案通常只保存了这个面板，没有保存面板后面的电话网、寻呼网、聊天服务和真实见面。

这就是为什么旧网考古必须把 **page archaeology** 再向外扩一层，做 **communication-path archaeology**，但仍严格保留本仓 1995–2015 中文 Web 的 scope 边界。
