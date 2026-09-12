# 留守家庭共享视频：2008 年更早的可操作实例证据 checkpoint

## 目的

这不是新的 state-gap 总论。

仓库已经有 canonical note：

- `LEFT_BEHIND_FAMILY_QQ_VIDEO_CHAT_SHARED_TERMINAL_AND_REMOTE_CARE_STATE_GAPS_2005_2015.md`

该文件已经建立了：

- policy / venue / terminal / network / client / account / presence / session / conversation / downstream care 的状态链；
- `shared terminal`、`local caregiver mediation`、`native-client transaction dark matter` 等问题；
- 2010 重庆“亲情视频聊天室”、2011 青田 QQ 视频、2015 黔东南远教站点培训等证据。

本 checkpoint 只做一件事：

> **把已经观察到的“学校共享终端完成真实亲子视频”的时间下限从 2010 年明确向前推到至少 2008 年，并把两个同期实例登记成可复核 evidence family。**

它以后应折回 canonical note，而不是继续裂变出更多近义文件。

---

## 1. Claim list before narrative

### C1 — 2008-01：重庆丰都至少已有 14 所农村寄宿制学校设置“亲情聊天室”，且存在现场观察到的视频会面

2008-01-03 搜狐所载新华社稿件报道：元旦前夕，丰都县平渡中学初二学生陈代希在“亲情聊天室”的电脑摄像头前，与远在苏州务工的父母进行视频拜年。报道还说，丰都县此前在 2007 年 6 月对农村留守儿童进行调查，近八成受访儿童在“最大的愿望”中选择“想见爸爸、妈妈”；当时已有 14 所农村寄宿制学校建立“亲情聊天室”，700 多名儿童可每周与父母通电话或视频聊天，并有指导老师、心理辅导老师参与。

Evidence:

- 新华社 / 搜狐转载，2008-01-03，《重庆丰都县为农村留守儿童建立“亲情聊天室”》  
  https://news.sohu.com/20080103/n254429527.shtml

Grade: **B（同期新华社现场报道，经搜狐转载）**。

可以支持：

- 2008-01 前后丰都至少存在一批由寄宿制学校提供的共享亲情通信设施；
- 至少有一个被记者描述的 `school computer + camera → child ↔ migrant parents` 视频实例；
- 教师/心理辅导人员属于这套机构化接入的一部分。

不能支持：

- 丰都最早一间聊天室就是 2008 年建成；
- 14 所学校的设备、软件、带宽、开放时段完全一致；
- 700 多名儿童都按“每周一次”稳定完成过成功视频；
- 该会话使用 QQ 或某个具体客户端；
- 当前搜狐页面的 DOM/charset/脚本就是 2008 年版本。

### C2 — 2008-07：宿迁学校电脑教室已经成为某些儿童的主要亲子通信入口

2008-07-09 搜狐所载《中国青年报》稿件记录：11 岁的宿迁蔡集实验小学学生苏啸在周末使用学校电脑教室，与在合肥务工的父亲进行网上视频聊天。父母一年最多回家一两次；报道明确写到，每月一次网上聊天成为他和父亲交流的主要方式。

同一报道把视频终端放进更大的照护基础设施中：宿迁给留守儿童建档、建设寄宿班、“代理家长”、心理咨询室和“留守儿童之家”，并在中小学配置网络视频等亲情通信设施。

Evidence:

- 《中国青年报》 / 搜狐转载，2008-07-09，《宿迁：让学校成为留守儿童温暖的家》  
  https://news.sohu.com/20080709/n258031797.shtml

Grade: **B（同期记者采访，经搜狐转载）**。

可以支持：

- 至少存在一个 `school computer room → monthly video contact → migrant father` 的具体使用实例；
- 共享 Internet 接入与寄宿、代理家长、心理咨询等线下照护体系可以同时存在；
- 一个孩子不拥有家庭电脑，也仍可能成为视频通信的实际使用者。

不能支持：

- “每月一次”是宿迁所有留守儿童的平均频率；
- 该视频必然通过 QQ；
- 学校视频联系能够替代父母一年仅一两次的实体见面；
- 报道里的“600 余部”通信设施等于 600 个同时可用视频机位。

---

## 2. 对 canonical chronology 的实质修正

现有 canonical note 的第一个主要 operational claim 从 2010 重庆计划/实例开始。新材料要求把时间表达改得更谨慎：

```text
observed institutional shared parent-child video in Chinese rural schools
<= 2008-01
```

这里只能写“**至少到 2008 年初已经观察到**”，不能写“2008 年发明/首次出现”。

这是 METHOD 中 multiple clocks 的典型案例：

- 地方试点开始时间；
- 第一次媒体报道时间；
- 设备实际可用时间；
- 儿童完成第一次成功会话时间；
- 市级/省级政策规模化时间；
- 私人家庭终端普及时间；

不应被压成一个“视频聊天进入留守家庭”的年份。

---

## 3. 2008 的拓扑：用户不等于设备所有者

两条材料共同强化一个旧网研究中很容易被忽略的对象关系：

```text
child user
≠ terminal owner
≠ network subscriber
≠ software administrator
≠ account creator
```

可能的机构化拓扑是：

```text
school / boarding school
  ├─ room
  ├─ PC
  ├─ camera + audio
  ├─ Internet connection
  ├─ teacher / counsellor
  └─ schedule / access rule
           ↓
         child
           ↕
     native video client (?)
           ↕
   migrant parent endpoint
```

这对 Web 史尤其重要，因为后来研究者若只查“家庭电脑拥有率”或“家庭宽带普及率”，会漏掉一类真实用户：

> **个人没有终端所有权，但借学校/单位/网吧/社区的制度化共享终端完成了数字事务。**

可称为：

**institution-mediated user state / 制度中介型用户状态**。

它不是新平台类型，而是 adoption 状态的一种拆分。

---

## 4. 两个 2008 页面今天能打开，不等于已经拿到 2008 Web artifact

本轮可以直接访问的两个 URL 都仍在搜狐域名下，并带有 2008 日期与同期稿件正文：

- `https://news.sohu.com/20080103/n254429527.shtml`
- `https://news.sohu.com/20080709/n258031797.shtml`

但按 `docs/METHOD.md`，它们在本轮只能作为：

> **current live origin/portal pages carrying contemporaneous-dated reports**

不能自动升级成：

> **verified 2008 archived webpage interface**

本轮没有取得并逐项核验：

- archive source；
- capture datetime；
- historical HTTP status；
- historical Content-Type；
- charset；
- DOM；
- iframe/脚本在 2008 年的真实结构；
- 图片、CSS、JS 等子资源；
- 第二历史时点。

搜索过程中也没有得到能够实际打开检查的 Wayback locator。因此：

**M1 verified historical capture: NOT ACHIEVED IN THIS SLICE.**

`没有在本轮找到可验证 capture` 不得写成 `Internet Archive 当年没有保存`。

---

## 5. Source family：同一个门户 host 不等于同一个证据来源

这两条 material 都保存在 `news.sohu.com`，但稿源不同：

- 2008-01：新华社；
- 2008-07：《中国青年报》。

因此判断 evidence family 时，不能只按 host 去重。

反过来，同一新华社稿件如果被搜狐、新浪、网易分别转载，也不能因为有三个 URL 就计成三个独立观察。

这里建议保持：

```text
portal URL count != evidence family count
```

本 checkpoint 当前至少有两个不同的 contemporaneous reporting families，但它们仍都属于新闻证据 B，而不是 archived-page A。

---

## 6. 一个值得带回 how-people-lived 的生活史含义

2008 材料最值得跨仓带回去的，并不是“某学校很早就有摄像头”。

更重要的是：

> **数字通信进入普通家庭生活，并不总是沿着“家庭购买电脑 → 家庭装宽带 → 家庭成员自己上网”的私人消费路径。**

它也可能沿着：

```text
学校先联网
→ 学校先拥有终端与摄像头
→ 教师管理时间与设备
→ 儿童以学生身份获得会话机会
→ 家庭关系因此短暂进入网络
```

这是一种制度基础设施把 Internet 临时“借给家庭”的模式。

它与网吧、单位机房、公共图书馆、远程教育站点等共享接入场景可以进行更广泛比较，但本文件不扩展成全球共享终端史。

---

## 7. 已证实 / 高概率 / 不知道

### 已证实（在当前证据强度下）

- 2008-01 同期新华社报道明确记载丰都学校亲情聊天室中的实际视频会面；
- 2008-07 同期《中国青年报》报道明确记载宿迁儿童使用学校电脑教室与外地父亲视频；
- 两个案例都说明儿童的 Internet 使用可以由学校共享终端中介，而不要求家庭私有设备；
- 这些报道早于 canonical note 目前突出使用的 2010 重庆扩张节点。

### 高概率但仍需更好证据

- 2007 年已经存在一批实际投入使用的相关设施，因为 2008-01 报道称项目和调查在此前已经展开；
- 教师在实际会话中承担设备、预约或组织劳动，但本轮没有操作手册或排班表证明每次会话的具体劳动分工。

### 不知道

- 两地最早一次亲情视频的日期；
- 客户端品牌与版本；
- 操作系统；
- 摄像头、声卡、耳麦型号；
- 带宽与资费；
- NAT/relay/codec；
- 登录账号由谁申请和保管；
- 会话失败率；
- 是否留下本地聊天记录；
- 是否存在可验证的 2008 Wayback/WARC 主文档与子资源集合。

---

## 8. 下一步

优先级高于继续增加同类新闻个案的是：

1. 将这两个 2008 实例折回 `LEFT_BEHIND_FAMILY_QQ_VIDEO_CHAT_SHARED_TERMINAL_AND_REMOTE_CARE_STATE_GAPS_2005_2015.md` 的 chronology；
2. 针对精确 URL 做 Wayback / Common Crawl / 其他 archive locator 检查；
3. 找丰都/宿迁学校或教育部门当年的设备采购、操作说明、开放时段、预约表或计算机教室配置；
4. 找 2007–2009 QQ/视频客户端的官方帮助、安装说明或软件包，才能讨论实际 client/browser/OS 环境；
5. 若能取得两个可验证历史时点，再把这一对象升级为 M1 case 候选。

在此之前，不应该再新增第三篇“留守儿童视频 state gap”总论。