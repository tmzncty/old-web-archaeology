# 留守家庭 QQ / 视频聊天室 / 共享终端与远程照护状态缺口（约 2005–2015）

## Scope

本文件研究约 2005–2015 中文 Web 与即时通信客户端交界上的一个具体对象：

> **学校“亲情电话 / 亲情视频聊天室”、QQ 视频/群聊等数字接口，怎样进入外出务工父母与留守儿童的家庭联系；而今天留下来的网页证据，又能证明到事务链的哪一步。**

它不是中国留守儿童史，也不是全球视频通信史。中国 1995 年以前的通信前史、2015 年后的微信/智能手机家庭生活及海外比较主要放在 `how-people-lived`：

- https://github.com/tmzncty/how-people-lived/blob/main/topics/remote-parenting-left-behind-children-care-bandwidth-and-mediated-copresence-china-1995-2026.zh-CN.md

本文遵守 [`docs/METHOD.md`](docs/METHOD.md)：

- platform / site / page / capture / claim 分开；
- `exists ≠ available ≠ used ≠ outcome`；
- 同期新闻能证明当时报道了某项设施或操作，不能自动证明每个站点实际可用；
- 今天仍在线的 2010/2011 新闻页是 current live page carrying historical-dated content，不是已经验证的 2010/2011 archive capture；
- 搜到一个历史 URL 或 Wayback locator 也不等于已经检查 capture。

本轮 **M1 = NOT ACHIEVED IN THIS SLICE**。没有实际取得并逐资源检查一份满足本仓合同的 2005–2011 QQ 帮助页、学校亲情聊天室页面或相关站点的 verified Wayback/WARC response。

---

## 1. Claim list before narrative

### C1 — 2010 年前后，一些地方把视频通信作为公共/学校照护基础设施提供

2010-09-22 新华社报道，重庆计划到当年底开设 2000 个“亲情视频聊天室”、安装 5000 部“亲情电话”；学校和主城区农民工公寓中已有免费视频联系设施。

Evidence:

- 新华社（搜狐转载），2010-09-22  
  https://news.sohu.com/20100922/n275206482.shtml
- 重庆市教委 / 教育部，2011-01-13，《关爱农村留守儿童行动计划》  
  https://www.moe.gov.cn/jyb_xwfb/s6192/s222/moe_1754/201101/t20110113_114512.html

Grade: **A（政府行动计划） + B（同期新闻）**。

Claim strength:

> 2010–2011 重庆的政策与同期报道明确显示，亲情电话和视频聊天室被纳入留守儿童公共关爱设施。

不能升级成：

> 2010 年底所有 2000 个聊天室均已按同一技术标准建成并稳定运行。

因为“计划数量、建设数量、可用数量、使用数量、成功通话数量”是不同状态。

### C2 — 至少有儿童在学校共享终端上与外出父母完成过视频会话

2010-12-13 同期报道记录：合川草街镇育才小学 9 岁袁晓航坐在学校亲情聊天室，与在浙江务工的母亲视频聊天。

Evidence:

- 华龙网-重庆商报（新浪转载），2010-12-13  
  https://news.sina.com.cn/c/2010-12-13/073221629858.shtml

Grade: **B（同期现场报道）**。

这可以证明至少一个观察到的 `shared terminal → video conversation` 实例，仍不能证明全市平均使用率或效果。

### C3 — 2011 年 QQ 已真实进入一些跨地留守家庭的视频会面

2011-11-07 中新社青田现场报道中，6 岁陈宇洋与在西班牙的母亲视频；记者明确观察到孩子注意 QQ 动画表情，对母亲话语反应有限。

Evidence:

- 中新社/中新网，2011-11-07  
  https://www.chinanews.com.cn/qxcz/2011/11-07/3442352.shtml

Grade: **B（同期现场报道）**。

这支持：

- QQ 客户端/服务至少参与了该次亲子视频场景；
- IM 的界面资源（例如动画表情）本身会进入亲子互动；
- `video stream established ≠ relational familiarity restored`。

它不支持：

- 所有青田留守家庭都用相同 QQ 版本；
- 当次通话使用的 codec、端口、服务器路径、摄像头型号或带宽已知；
- “网络视频聊天是主要机会”可精确量化成使用率。

### C4 — 到 2015 年，公共视频站点仍需提供账号与操作培训

2015 年贵州黔东南报道：自 2013 年起在农村远程教育站点建立亲情视频聊天室；到报道时有 1075 个远教站点聊天室和 455 个学校“留守儿童之家”，定时免费开放。报道明确说，因部分家长文化程度较低、不熟悉上网，当地会教他们申请 QQ、学习上网聊天。

Evidence:

- 《中国组织人事报》/人民网，2015-07-27  
  https://dangjian.people.com.cn/n/2015/0727/c397214-27367727.html

Grade: **B（同期机构性报道）**。

它证明“网络存在”之外还有 `account/interface literacy` 层，不证明培训后每个家庭都能完成独立视频会话。

---

## 2. 研究单位必须拆开

这类对象非常容易被一句“学校建了视频聊天室”压扁。

至少要分：

| 层级 | 示例 | 不能自动推出 |
|---|---|---|
| policy / program | “建设 2000 个亲情视频聊天室” | 2000 个全部完成且可用 |
| physical venue | 学校一间电脑室 | 设备安装/联网/开放 |
| terminal | PC + 摄像头 + 麦克风 | 客户端可登录、音视频正常 |
| network | 校园/远教网络 | Internet 可访问 QQ 所需服务 |
| client | QQ / 其他视频客户端 | 双方版本兼容、账号可用 |
| account | QQ 号 | 账号本人、密码仍掌握、未冻结 |
| presence | 对方显示在线 | 对方此刻有时间/愿意接听 |
| session | 视频连接成功 | 音视频质量足以交流 |
| conversation | 实际说了话 | 沟通内容满足照护需要 |
| downstream care | 知道孩子冷/生病/缺钱 | 被子、药、照护者真的到现场 |

旧 Web 考古如果只保存了 program announcement，最多只能证明前一两层。

---

## 3. 一次“亲情视频”的完整可执行链

建议以后所有类似案例按以下状态记录：

```text
A. program announced
  ↓
B. room physically built
  ↓
C. room open at this date/time
  ↓
D. terminal powered and usable
  ↓
E. camera/microphone/audio usable
  ↓
F. network route available
  ↓
G. IM client installed
  ↓
H. client version/service compatible
  ↓
I. child/local caregiver has account credentials
  ↓
J. migrant parent has remote endpoint + credentials
  ↓
K. both parties are simultaneously available
  ↓
L. call/signaling accepted
  ↓
M. audio/video stream established
  ↓
N. conversation actually occurs
  ↓
O. message/need is understood
  ↓
P. local or remote actor performs downstream care action
```

任何网页证据都必须说明自己落在哪些字母上。

---

## 4. 新增状态缺口

### 4.1 announcement-to-equipped-room gap

政策宣布/新闻写“将建”不等于房间已装修、终端已安装。

需找：

- 采购/验收材料；
- 学校照片及日期；
- 设备清单；
- 实际开放通知。

### 4.2 equipped-room-to-open-session gap

有房间不等于孩子想用时就能用。

共享终端可能受：

- 开放时段；
- 排队；
- 教师值守；
- 寄宿/课程表；
- 节假日；
- 电力/网络故障

影响。

2014 年贵州铜仁一所学校的同期报道明确写到，亲情聊天室有 4 台电脑、4 部电话，学生需要预约后与父母联系。这说明 `terminal count` 与 `usable session slots` 应分开。

Evidence:

- 中新网，2014-06-13  
  https://www.chinanews.com/edu/2014/06-13/6277812.shtml

Grade: **B**。

### 4.3 client/version compatibility gap

“装有 QQ”不等于历史任何 QQ 版本都能与远端端点完成音视频。

本轮未知：

- 具体 QQ build/version；
- Windows 版本；
- 摄像头 driver；
- DirectX/音频组件；
- NAT traversal / relay 机制；
- codec；
- 端口和防火墙要求；
- 最低实际带宽；
- 客户端升级策略。

在取得当年 QQ 官方帮助页/安装包/手册或 verified capture 前，全部保持 `unknown`。

### 4.4 web-page-to-native-client gap

这是本专题对 old Web 最重要的技术边界之一。

一份学校网页或新闻页可以告诉用户：

> “这里可以视频聊天。”

但实际事务可能发生在原生 QQ 客户端，而不是浏览器页面。

因此：

```text
historical Web page survives
≠ historical video transaction survives
```

甚至 Web 页面可能保存得非常好，而真正的：

- 好友列表；
- 在线状态；
- 通话请求；
- 通话失败码；
- 音视频流；
- 本地聊天数据库；
- 账号验证

全部不在 Web archive 的采集面内。

这可以称为：

**native-client transaction dark matter / 原生客户端事务暗物质**。

### 4.5 account-to-person identity gap

一个 QQ 号不必然等于一个稳定的个人身份。

共享终端环境尤其可能出现：

- 教师代注册；
- 家庭共用账号；
- 孩子使用祖父母/亲属账号；
- 密码写在纸上；
- 账号被回收/冻结；
- 昵称变化。

当前材料只证明某些家庭使用 QQ，不足以恢复 account ownership model。

### 4.6 local-caregiver mediation gap

孩子越小，越可能需要祖父母、老师或其他照护者：

- 开机；
- 找到联系人；
- 输入账号密码；
- 调整摄像头；
- 转述父母的话；
- 解释孩子状态；
- 结束/重新连接通话。

所以看似 `parent ↔ child` 的数字会话，实际拓扑可能是：

```text
migrant parent
      ↕
   IM/video
      ↕
teacher/grandparent ── child
```

后来的研究也明确指出，祖父母在视频亲职中会成为中介和“脚手架”。但对 2005–2015 的具体中文旧网案例，仍需同时期第一手操作材料来恢复这种劳动。

### 4.7 online-presence-to-attention gap

对方“在线”只说明账号/客户端达到某种 presence state。

不等于：

- 对方没在上班；
- 能开摄像头；
- 能长聊；
- 有安静空间；
- 正在看屏幕；
- 愿意讨论孩子此刻想谈的话。

这是即时通信平台保存最差、但生活史最重要的一层。

### 4.8 call-connected-to-meaningful-conversation gap

2011 青田案例直接展示：视频通话已经连接，儿童却主要注意 QQ 动画表情，对母亲回应很少。

因此不能把 `video call success` 作为 `relationship restored` 的 proxy。

### 4.9 remote-advice-to-local-action gap

父母可以通过视频知道孩子需要什么，但真正的照护动作可能仍需：

- 祖父母；
- 老师；
- 亲属；
- 快递/电商；
- 医疗机构；
- 本人返乡。

例如“知道孩子冷”与“有人把被子送到学校”是两个状态。

这个 outcome 通常完全位于 Web/IM 记录之外。

### 4.10 call-log-to-content gap

即使后来能得到某种账号级日志，最多可能证明：

- 某时间呼叫；
- 时长；
- 对端账号；
- 成功/失败。

它不能自动告诉我们谈了：

- 学习；
- 钱；
- 健康；
- 情绪；
- 是否回家；
- 谁先挂断。

通信 metadata 和家庭意义必须分开。

### 4.11 shared-terminal privacy/history gap

学校共享电脑为了安全和下一名使用者，可能：

- 清理历史；
- 退出账号；
- 还原系统；
- 禁止本地保存；
- 由教师统一管理。

这些做法对运营可能是正确的，但会系统性消除普通用户的历史痕迹。

因此：

> **a well-maintained shared terminal can be an intentionally bad personal archive.**

这一点与网吧案例的 `machine-reset archive gap` 同源，但亲情聊天室还增加了儿童隐私和机构代管账号的问题。

### 4.12 media-resource survival gap

QQ 视频/表情/头像和 Web 新闻页可能依赖不同 host、协议和缓存。

今天一篇 2011 新闻正文能打开，不代表：

- 当年的 QQ 动画表情资源；
- 头像；
- 视频流；
- client UI；
- 摄像头截图；
- 下载链接

还能恢复。

甚至“孩子盯着某个动画表情”这种同期观察可能留下文字描述，而那个具体动画对象本身已经消失。

---

## 5. 三种不同的“共享终端”不能混成一个平台

### 5.1 学校亲情聊天室

特点可能包括：

- 学校空间；
- 儿童端共享；
- 教师/管理员值守；
- 固定开放时段；
- 与学校心理/关爱项目结合。

### 5.2 农村远程教育站点

2015 黔东南材料表明，已有农村远教站点被再利用为亲情视频基础设施。

这是一种 **infrastructure repurposing / 基础设施再用途化**：

原本为教育/党员远教等目的部署的 PC、网络和空间，后来可以承担家庭通信。

### 5.3 农民工公寓/城市端共享空间

重庆 2010 报道提到，主城区一些农民工公寓也设免费视频聊天室。

这很重要，因为视频事务需要两端执行。只给农村孩子一台电脑并不够；远端父母也必须有：

- 终端；
- 网络；
- 时间；
- 账号；
- 可用空间。

因此“数字鸿沟”至少是双端的。

---

## 6. 页面考古：今天能打开的同期新闻证明什么

本轮检查的 2010–2015 新闻和机构页面，大多今天仍可以 live retrieval。

正确描述：

> current live page carrying historical-dated content

不能写：

> verified 2010 historical page / capture

因为当前页面可能叠加：

- 新模板；
- 新导航；
- 新统计脚本；
- HTTPS/CDN；
- 新编码；
- 新分享按钮；
- 已替换的图片 host；
- 后来的响应式布局。

除非实际检查档案 capture 的：

- original URL；
- archive URL；
- capture datetime；
- HTTP/回放状态；
- HTML；
- charset；
- 子资源；
- redirect；
- 浏览器条件，

否则不能把当前呈现当作当年浏览体验。

---

## 7. 本轮证据账本

| claim | source | grade | can prove | cannot prove |
|---|---|---:|---|---|
| 重庆计划大规模建亲情视频聊天室/电话 | 教育部转载重庆行动计划，2011 | A | 政策目标、设施类别、数量目标 | 全部实际验收/稳定使用 |
| 2010 已有学校/农民工公寓亲情视频场景 | 新华社 2010-09-22 | B | 同期报道存在这些设施/场景 | 全市覆盖率、技术栈 |
| 9 岁儿童在学校与浙江母亲视频 | 重庆商报 2010-12-13 | B | 至少一个观察实例 | 普遍效果 |
| 2011 青田儿童通过 QQ 视频见海外母亲 | 中新社 2011-11-07 | B | QQ 进入具体亲子视频场景、界面资源进入互动 | QQ 版本/codec/服务端细节 |
| 2015 黔东南利用远教站点建聊天室并培训家长申请 QQ | 中国组织人事报 2015 | B | 公共终端 + 账号/技能培训并存 | 1075 点每次 session 成功率 |
| 2014 贵州某校 4 台电脑+4 电话、预约联系 | 中新社 2014 | B | terminal count 与预约制实例 | 历史配置完整技术清单 |

没有 A 级 historical Web capture，所以本轮不升级为 M1 完整案例。

---

## 8. 同期第一人称材料与“平台可观察事实”必须分层

### 平台/设施可观察事实

- 政府要求建设亲情视频聊天室；
- 某校有 4 台电脑、4 部电话；
- 报道明确出现 QQ 动画表情；
- 远教站点教家长申请 QQ。

### 同时性自述/现场言语

- 2010 小学生通过视频告诉母亲自己在学校很好；
- 2011 青田儿童在现场对“妈妈叫什么名字”回答“不知道”。

### 二次解释

- “视频聊天室能缓解亲情焦虑”；
- “网络拉近亲情距离”。

这些多是报道者/机构的解释，不能和用户 outcome 混为同一证据等级。

### 后来学术重构

2018–2023 的民族志研究可以帮助我们提出“祖父母中介”“远程照护”“视频矛盾性”等机制，但不能反向证明 2010 某一学校具体怎么操作 QQ。

---

## 9. 反例

### 9.1 没有私人家庭电脑，也可能完成视频

学校/远教站点说明 `household ownership ≠ service access`。

### 9.2 有视频，也可能关系陌生

青田案例说明 `visual presence ≠ intimacy`。

### 9.3 有终端，也可能不会申请/操作账号

2015 培训材料说明 `terminal available ≠ interface executable`。

### 9.4 有 Web 页面，也可能真正的事务完全发生在客户端

这是 Web archive 对 native IM 历史的结构性盲点。

### 9.5 有远程联系，也不能替代现场照护

视频/QQ 最多扩展 care coordination；孩子身边仍需要祖父母、教师或其他人处理身体性任务。

---

## 10. 后见之明风险

1. 不要把微信时代“扫二维码就能视频”的习惯倒灌进 2010 QQ。
2. 不要假定每所“亲情聊天室”使用相同软件；有些可能用 QQ，有些可能用其他视频工具。
3. 不要从 2011 青田 QQ 个案外推全国平台份额。
4. 不要把今天还能打开的中新网/新浪/搜狐页叫作 2010 capture。
5. 不要从“2000 个计划”写成“2000 个完成并稳定运行”。
6. 不要从“有摄像头”推导“音视频质量足够”。
7. 不要把共享终端用户账号和个人实名身份自动对应。
8. 不要把“孩子与父母视频过”写成“亲子关系得到改善”。

---

## 11. 本轮未知项

### 技术未知

- 2010 重庆具体学校使用的 IM 产品与版本；
- QQ 具体 build、协议、codec；
- Windows 版本；
- 摄像头/麦克风型号与 driver；
- 客户端升级方式；
- 带宽和网络拓扑；
- 防火墙/NAT；
- 失败提示；
- 本地聊天记录默认保存策略；
- 公共机是否使用还原卡/统一镜像；
- 登录账号由谁创建和保管；
- 音视频 session metadata 保留多久。

### 历史页面未知

- 2005–2011 QQ 官方视频帮助页原始 URL pattern；
- 相关 help page 的历史 DOM/charset；
- 学校/远教站点是否有独立预约网页；
- 是否有 IE-only / ActiveX / plugin 依赖；
- 页面上的客户端下载安装链；
- 图片/Flash/视频资源子 host。

### 生活 outcome 未知

- 平均每名儿童多久能预约一次；
- 父母端成功接通率；
- session 时长；
- 因上班错过的比例；
- 有多少通话由教师/祖父母协助；
- 通话以后有多少现实照护动作真正被执行。

---

## 12. 下一步 archive 侦察目标

优先寻找而不是猜：

1. 2008–2011 腾讯 QQ 官方帮助/下载页中“视频聊天 / 摄像头 / 语音视频”文档的 verified captures；
2. 重庆/贵州学校或远教站点 2010–2015 “亲情聊天室”页面的历史 URL 与 capture；
3. 当年电脑教室设备采购、验收或使用管理办法；
4. QQ 老版本安装包/README/软件手册，验证 OS、camera、network 假设；
5. 同期用户教程，确认普通使用者真实的 camera setup / NAT / login failure；
6. 如果能取得一份完整 historical capture，再按 M1 合同记录主 HTML、子资源、charset、浏览器条件和缺失列表。

在这些证据出现以前，正确结论是：

> **“本轮尚未验证技术细节”，而不是“当时没有这些技术细节”。**

---

## 13. 对中文旧网考古的新增理解

这类案例迫使 old-web-archaeology 承认一个重要边界：

> **Web 只是旧数字生活的一个可见层。**

2010 年的一篇新闻网页可能完整活到今天，却只留下“学校有亲情聊天室”这句话。真正的一次家庭会面发生在：

- 一间今天可能已改作别用的教室；
- 一台早已报废的 PC；
- 一个不能再登录的 QQ 号；
- 一个当时的 Windows/摄像头/客户端组合；
- 父母下班后短暂的同时在线窗口；
- 一次没有公开存档的音视频流；
- 通话以后祖母、教师或父母做出的现实行动。

因此：

**page survives ≠ client survives ≠ session survives ≠ care outcome survives。**

旧 Web 的历史可见性在这里出现了系统偏差：最容易留下的是政策页面和新闻正文；最接近日常家庭关系的那几十分钟会话，反而最容易彻底消失。
