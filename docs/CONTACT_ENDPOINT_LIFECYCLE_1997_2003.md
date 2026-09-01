# 1997—2003 联系方式生命周期：旧网页上的 Email 不是永久身份标识

本文件补充：

- `docs/METHOD.md`；
- `docs/PUBLIC_ACCESS_CONTEXT_1996_2003.md`；
- `docs/ACCOUNT_PORTABILITY_AND_LOCAL_RESIDUE_1999_2003.md`。

主研究对象仍是约 1995—2015 年中文互联网。

这里处理一个旧网页考古中非常容易误判的问题：

> **一个历史页面上的联系方式，首先证明“这个页面在当时把该地址作为联系入口”，而不是证明“这个地址永久属于同一个现实人”。**

这一规则尤其适用于：

- E-mail；
- OICQ/QQ；
- ICQ；
- BBS ID；
- BP 机；
- 固定电话；
- 手机号；
- 个人主页 URL。

---

## 1. 为什么 Email 需要单独做生命周期模型

1990 年代末 Webmail 的一个核心能力，是让用户可以从不同联网电脑进入同一个邮箱。

Yahoo! 1997 年发布 Yahoo! Mail 时就明确强调：免费邮件账户可以从世界上任何一台连接 Internet 的电脑访问。

来源：

- Yahoo!, “Yahoo! Expands Community Services With Free E-Mail,” 1997-10-08：<https://www.newmediawire.com/news/yahoo-expands-community-services-with-free-e-mail-3062567>

中国 163 电子邮局的同期报道也明确记录 1999 年用户通过 Web 收发邮件。

来源：

- 《南方周末》，《综述：飞华入不敷出卖掉163》，1999-12-24，经新浪科技保存：<https://tech.sina.com.cn/news/internet/1999-12-24/14105.shtml>

因此 Email 和固定电话不同：

> **它可以跨终端、跨地点继续使用。**

但它又和用户自己控制的域名不同：

> **免费邮箱地址的域名和服务生命周期仍由平台控制。**

这使旧网页上的 Email 同时具有“相对长期”与“可能突然失效”两种性质。

---

## 2. archived page 能证明什么

假设一个 1999 年个人主页写着：

```text
Email: example@163.net
```

一个日期可靠的 archive capture 可以较强支持：

> 在该 capture 对应时期，页面作者公开把 `example@163.net` 作为联系地址。

它**不能自动证明**：

- 该邮箱今天仍有效；
- 2001 年仍由同一个人使用；
- 邮箱地址从未被停用；
- 地址没有被盗用；
- 这个 Email 与页面上其他昵称一定属于同一个现实人；
- 邮箱中的全部历史内容仍然存在；
- 当前同名地址的控制者就是历史页面作者。

因此联系方式应当作为一个**有时间范围的 endpoint observation** 记录。

---

## 3. 163 电子邮局证明：账号“存在过”不等于无限期继续存在

1999 年同期报道记录：163 电子邮局曾清理“三个月无信件往来”的废旧账号。

来源：

- <https://tech.sina.com.cn/news/internet/1999-12-24/14105.shtml>

### 考古含义

如果页面在 1998 年留下某个 `@163.net` 地址，而 2000 年没有后续证据：

不能仅凭旧页面写：

> “该用户 2000 年仍使用此地址。”

安全写法应是：

> “该地址至少在 1998 年这一页面版本中被公开为联系方式；后续有效性未知。”

### 不要进一步偷换

报道中的“收回废旧账号”并不足以单独证明：

- 原地址一定立刻重新分配给别人；
- 所有账号都严格按同一规则处理；
- 每个被回收地址的邮件历史怎样处置。

这些需要另外的产品规则或技术证据。

---

## 4. 2002 年 263 收费证明：平台政策变化可以直接制造“地址迁移事件”

2002 年 263 宣布停止免费邮箱。

同期报道中，一名用户表示自己已经使用该邮箱五年，与国内外朋友保持联系，因此换地址会非常麻烦。

来源：

- *People's Daily Online*, 2002-03-20：<https://en.people.cn/200203/20/eng20020320_92442.shtml>

另一名北京大学学生则明确表示，需要重新告诉所有朋友旧 263 地址将失效。

来源：

- *China Daily / Business Weekly*, 2002-03-26：<https://www.chinadaily.com.cn/en/bw/2002-03/26/content_113840.htm>

263 在收费过渡期还提供了旧地址自动转发到新地址的功能。

来源：

- 《263今起实施邮件全部收费　收费用户总数已达59万》，原日期 2002-05-23，政府站保存版本：<https://fzggw.cq.gov.cn/zwxx/xwbd/202003/t20200319_5775543.html>

### 这在旧网考古里应当被建模为 lifecycle event

```text
active endpoint
      ↓
provider policy change
      ↓
user choice: pay / abandon / migrate
      ↓
optional forwarding window
      ↓
old endpoint becomes uncertain or dead
```

因此旧网页上 Email 的消失不一定对应：

> “这个人退出互联网。”

它也可能只是：

> “这个人换了服务商，但旧页面没有更新。”

---

## 5. 联系方式必须区分“标识符连续性”与“现实人连续性”

建议使用：

```text
historical person
      ↕  uncertain mapping
contact endpoint
      ↕  provider/account lifecycle
service/platform
```

而不是：

```text
historical person = email address
```

因为以下情况都可能发生：

- 用户换邮箱；
- 用户保留多个邮箱；
- 服务商关闭；
- 免费转收费；
- 长期不活跃账号被回收；
- 地址被盗用；
- 页面多年未更新；
- 联系方式是站点公共邮箱而非个人邮箱；
- 地址属于多人共同维护的组织。

---

## 6. 对个人主页、论坛签名、站长页的建议字段

遇到联系方式时，不要只存：

```yaml
email: example@example.com
```

建议至少记录：

```yaml
contact_endpoint:
  type: email
  value_preserved: false
  domain: 163.net

observed_on_page:
  capture_datetime: "1999-07-01T00:00:00Z"
  original_url: "..."
  archive_url: "..."

role_on_page:
  claimed_as: author-contact
  # author-contact / webmaster / organization / submission-address / unknown

provider_context:
  service: 163-electronic-post-office
  access_model: webmail
  evidence_grade: B

lifecycle:
  known_active_from: unknown
  known_active_to: unknown
  later_policy_event: unknown
  migration_or_forwarding: unknown

identity_linkage:
  real_person_known: false
  confidence: low

privacy_action:
  publish_full_address: false
```

### 为什么默认 `publish_full_address: false`

历史邮箱地址可能：

- 仍在使用；
- 被重新激活；
- 与现实身份直接关联；
- 被垃圾邮件系统收集；
- 成为跨站身份关联线索。

如果完整地址不是论证所必需，应优先：

- 哈希；
- 局部遮蔽；
- 只保留域名；
- 只记录 endpoint 类型。

---

## 7. 联系方式时间线应当允许“空档”

一个个人主页可能依次出现：

```text
1998: school@example.edu.cn
1999: user@163.net
2001: user@263.net
2003: another@example.com
```

不要自动把它写成一条连续迁移链。

只有当页面、用户自述、转发提示或其他证据明确说明“旧地址迁到新地址”时，才能写：

```text
endpoint A → endpoint B
```

否则应记录成：

```text
A observed at T1
B observed at T2
relationship: unknown
```

原因包括：

- 同时多邮箱；
- 专门工作邮箱与私人邮箱；
- 网站投稿邮箱；
- 临时账号；
- 页面编辑者变化。

---

## 8. “地址失效”本身也是网站历史信息

旧站点常见一种情况：

页面仍被 archive 保存，正文也完整，但页面上的：

- Email；
- QQ；
- ICQ；
- 手机；
- 外链主页；

早已失效。

这些不只是“坏链接”。

它们说明一个更大的事实：

> **页面内容的保存寿命，可能长于页面内部社会关系路由的寿命。**

因此建议完整案例增加：

### Contact survival

- 页面文本是否保存；
- 联系入口是否仍可验证存在；
- 服务商是否仍存在；
- 地址是否曾发生收费/关闭/迁移；
- 是否有替代 endpoint；
- 是否只能证明历史存在，不能证明当前控制权。

---

## 9. Webmail 提醒我们：平台消失不是单纯“内容丢了”

当一个免费主页托管平台关闭时，可能丢失的是：

- 页面；
- 图片；
- URL；
- 友情链接。

当一个邮箱平台停止服务时，可能丢失的是：

- 邮件内容；
- 通讯录；
- 旧地址的可达性；
- 别人多年记住的联系方式；
- 旧网页、名片、简历里仍然指向该地址的社会路由。

所以旧网考古以后讨论“平台死亡”时，应至少区分：

```text
content death
URL death
account death
contact-endpoint death
relationship-routing death
```

这些不是同一个事件。

---

## 10. 海外对照怎样使用

Yahoo! Mail、Hotmail 的同期资料证明：

> Webmail 把同一邮箱从固定终端上拆下来，是全球性产品机制。

但本仓库不因此扩成全球邮件史。

海外材料只用来校准：

- “跨终端访问”不是中文互联网独有；
- 中国案例的特殊性应继续从网吧密度、家庭接入、拨号环境、中文门户竞争、价格和本地用户习惯中寻找。

中文旧网主体证据仍优先使用：

- 163；
- 263；
- 新浪/搜狐/21CN/网易等同时代服务；
- 中文个人主页；
- 论坛签名；
- 同期教程与用户材料。

---

## 11. 常见误判

### 误判 A：旧页面有 Email，所以这个人今天仍可通过它联系

错误。

只能证明历史页面当时公开过该地址。

### 误判 B：同一个 Email 出现在多年页面里，所以现实人身份已经确认

不一定。

还要排除：

- 页面镜像；
- 复制；
- 组织公共地址；
- 控制权变化。

### 误判 C：用户换了邮箱，所以网络身份“断了”

也不一定。

他可能通过：

- 转发；
- 新主页公告；
- QQ/ICQ；
- 同一 BBS ID；
- 线下联系人；

保持社会连续性。

### 误判 D：平台还活着，所以历史地址一定还活着

错误。

账号可能因为：

- 长期未使用；
- 收费；
- 违规；
- 用户主动放弃；

提前失效。

---

## 12. 本文件的证据边界

### 已证实

- 1997 年海外主流 Webmail 已明确以跨联网电脑访问为产品特征；
- 1999 年中国 163 用户已使用 Web 页面收发邮件；
- 163 存在清理长期无往来账号的机制；
- 263 在 2002 年免费转收费时发生了大规模用户迁移问题；
- 263 曾提供短期自动转发，以降低旧地址失效造成的联系中断。

### 合理推断

- 个人 Webmail 可以降低换终端、换地点造成的联系地址迁移成本；
- 网吧/学校机房环境使这种跨终端能力尤其重要；
- 一个公开时间很长的邮箱会积累“社会地址迁移债务”。

### 尚未证明

- 某个具体历史邮箱是否后来被重新分配；
- 某个旧页面作者是否实际迁移到某个新地址；
- 历史邮箱中的联系人和内容保存方式；
- 不同免费邮件系统逐版本的账号回收规则。

---

## 13. 与 M2 平台谱系的关系

`ROADMAP.md` 的 M2 已经要求研究：

- 谁拥有 URL；
- 内容生命周期由谁决定；
- 平台死亡时用户能否迁走内容。

联系方式应该加入同一组问题：

> **谁拥有“别人找到我”的入口？平台死亡时，这个入口能不能迁走？**

因此未来的平台比较不应只有：

```text
content portability
URL portability
```

还应增加：

```text
identity portability
contact-endpoint portability
relationship-routing portability
```

这会把“旧网站长什么样”进一步推进到：

> **一个旧平台消失时，它从普通人的社会生活里带走了什么。**
