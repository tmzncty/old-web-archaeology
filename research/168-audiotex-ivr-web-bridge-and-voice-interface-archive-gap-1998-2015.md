# 168 声讯、IVR—Web 桥与语音界面档案缺口（1998—2015）

> Research checkpoint，不是完整 case。研究对象仍严格服务于本仓 1995—2015 中文互联网 scope：不是把“电话史”无限并入 old-web，而是研究**中文 Web 与同时代电话信息系统如何共存、互相引流和共同完成事务，以及 Web archive 为什么会系统性漏掉其中一半。**

## 0. 为什么这个切片不是另一个 `page != transaction`

仓库已有大量事务状态专题；如果这里只写：

> “网页上有查分页面 ≠ 用户真的查到分数”

那没有新增价值。

本切片的新增点是一个不同的系统边界：

```text
Web / 新闻页 / 帮助页
        ↕
PSTN 电话号码
        ↓
自动声讯 / IVR
        ↓
DTMF 输入 / 语音输出
        ↓
私有数据库 / 计费状态
```

以及另一种更强的跨协议事务：

```text
168 电话计费
→ IVR 念出数字凭证
→ 用户用纸笔抄录
→ 浏览器重新输入
→ Web 账号 / 会员状态改变
```

这里的核心问题不是“页面是不是最终事务”，而是：

**历史服务的关键界面压根不是网页。**

因此即使 Wayback 完美保存了当年的 Web 帮助页，也可能仍然缺失用户真正操作的 IVR 菜单、语音提示、按键分支、电话计费、后台数据库和跨系统同步。

本轮把这种缺失暂称为：

**voice-interface loss / 语音界面损失**

与：

**IVR state-machine loss / IVR 状态机损失**。

---

## 1. 与仓库方法合同的关系

按 `docs/METHOD.md`，必须区分：

- historical Web page；
- 同期媒体对服务的操作说明；
- 电话服务本身；
- 后台数据库；
- 研究者根据操作说明抽象出的状态机。

本文件当前没有取得：

- 一份 1998—2005 运营商 168 历史网页 capture；
- 原始 IVR 录音；
- 原始交换 / CTI / 声讯平台手册；
- 电话计费 CDR；
- 与教育部门成绩库同步的技术协议；
- 同一服务两个时间点的可核验 IVR artifact。

因此：

**M1 historical 168 service artifact: NOT ACHIEVED IN THIS SLICE.**

本文件只形成 research note，不升级为完整 case。

---

## 2. 1998：168 是电信信息基础设施，不应被误写成 Web

国家统计局对 1998 年邮电通信业的总结明确记录：

- 公用数据通信网覆盖地市以上城市、90% 以上县市和部分乡镇；
- 中国公用计算机互联网已通达所有省会城市；
- **168 信息服务台实现全国地市以上城市联网**。

来源：国家统计局，《之十一：邮电通信业突飞猛进》。  
<https://www.stats.gov.cn/zt_18555/ztfx/xzg50nxlfxbg/202303/t20230301_1920449.html>

### Evidence

- grade: A / institutional contemporaneous statistical summary
- confidence: high for nationwide prefecture-level networking claim
- does **not** prove protocol, vendor, interface tree, individual use rate or household penetration

### Method boundary

`networked information service != World Wide Web`

168 可以是高度计算机化、联网的自动信息系统，但用户端仍可能只看到：

- 一个电话号码；
- 一段语音；
- 电话按键。

所以今后看到“168 联网”不能自动填成：

- browser；
- URL；
- TCP/IP end-user session；
- HTTP form；
- Internet user。

---

## 3. 2000 南京中考：可从媒体文字重建一个最小 IVR 事务骨架，但不能冒充原始菜单

2000 年 6 月 27 日《扬子晚报》报道：

- 南京中考文化成绩于次日零点开放；
- 自动台 `16896967`；
- 人工台 `1680`；
- 用户接通后输入考试座位号；
- 系统返回本人成绩；
- 次日仍去学校领取纸面成绩通知单。

新浪同期转载：  
<https://edu.sina.com.cn/job/2000-06-27/5390.shtml>

### Evidence

- grade: B / contemporary press operation description
- confidence: high for public workflow

### 最小可支持状态机

可以写：

```text
call number
→ connect
→ submit seat number
→ receive score information
```

不能写：

```text
welcome prompt exact wording
→ press 1 for score
→ press 2 for replay
→ error branch wording
→ timeout seconds
```

因为当前没有原始录音或手册。

### 新方法规则

**workflow inferable != interface text recoverable**

媒体可以让我们知道“用户做了什么”，却未必足以恢复“系统每一步具体说了什么”。

---

## 4. 2004 江苏：一次电话查询包含 terminal capability、身份键、数据库装载和容量状态

2004 年江苏高考查分同期报道比普通“热线号码列表”提供了更深的系统证据：

- `16887799`；
- 查询时要求准考证号 + 考试证号；
- 电话需要处于双音频 / `T` 状态；
- 查询系统按地区提供本地考生成绩；
- 数据输入核对完成后才开放；
- 南京查询线路扩容至可同时容纳约 2000 用户；
- 电信部门实时监控查询话路并调度高峰来电。

来源：《扬子晚报》，新浪教育转载，2004-06-27。  
<https://edu.sina.com.cn/l/2004-06-27/74104.html>

### Evidence

- grade: B
- confidence: high for described operational constraints

### 这里真正的新技术边界

一次“打 168 查分”不能只存成一个电话号码字段。

更接近实际的是：

```text
terminal supports DTMF?
→ local route accepted?
→ line available?
→ DB loaded?
→ identity tuple valid?
→ record found?
→ voice playback completes?
→ billing ends?
```

其中至少一半状态不会出现在历史网页 HTML 里。

### 建议新增 artifact 观察字段（research-level，暂不修改 schema）

```yaml
voice_service:
  access_number: unknown
  endpoint_restriction: unknown
  dtmf_required: unknown
  identity_fields: []
  prompt_tree_source: unknown
  concurrency_claim: unknown
  billing_model: unknown
  backend_data_load_timing: unknown
  manual_fallback: unknown
  original_audio_available: false
```

未知就是 `unknown`，不能从今天的 IVR 习惯倒推。

---

## 5. 2003 江苏：同一公共数据在电话和 SMS 之间迁移，改变的不是“页面皮肤”而是 interaction primitive

2003 年江苏高考查分争议材料记录：

- 2001 年以前，168 是主要较早查分入口；
- 2001 年移动短信进入；
- 2002 年联通短信进入；
- 用户偏好短信的重要原因包括可储存、可转发、可预订；
- 2003 年江苏又主要回到声讯电话，引发成本和拥堵争议。

新浪新闻同期报道：  
<https://news.sina.com.cn/c/2003-07-01/1352300325s.shtml>

新华社后续：  
<https://news.sina.com.cn/c/2003-07-08/0154336684s.shtml>

### Evidence

- grade: B
- evidence family: contemporary press, with several syndications
- do not count multiple mirrors as independent primary sources

### Archaeological implication

电话 → SMS 不是把同一 UI 换颜色。

interaction primitive 发生变化：

| Voice IVR | SMS |
|---|---|
| 必须占用一次会话 | 可异步收取 |
| 结果主要靠听 / 记 | 结果天然可保存 |
| 高峰需要重复拨号 | 可预订后等待推送 |
| 转发依赖重新口述 | 可直接转发文本 |
| 收费按分钟常见 | 可按条 / 服务计费 |

因此平台史不能只研究 browser UI；**一种数据服务迁移到另一种终端时，用户动作原语也会改变。**

---

## 6. 2007 江苏：队列拥塞属于历史界面的一部分，但 archive 几乎看不见

2007 年《中国青年报》采访南京考生计璐：

- 连续拨 3 次；
- 前两次进入系统并开始计费，但未得到结果；
- 第三次才完成查询；
- 1 元/分钟，约花五六元；
- 高峰时不少家庭会让亲友同时拨号；
- 声讯结果比学校 / 招办渠道提前约 24 小时。

学信网同期转载：  
<https://gaokao.chsi.com.cn/gkxx/js/200708/20070820/1055474.html>

新浪转载：  
<https://news.sina.com.cn/c/2007-08-20/034913698832.shtml>

### Evidence

- grade: B / contemporaneous interview
- confidence: high for this person and reported observed behavior; not population-representative

### Archive gap

未来研究者如果只保存：

```text
16887799
“高考成绩查询热线”
```

会丢掉真正决定体验的：

- busy signal / queue behavior；
- 进入系统但结果尚不可用时是否收费；
- repeated dial attempts；
- parallel family dialing；
- call duration；
- billing cadence。

这就是：

**queue-state archive gap / 队列状态档案缺口**。

它不是网页加载慢的简单对应物，因为电话服务的失败、等待和计费由交换网、IVR、线路容量与后端数据状态共同产生。

---

## 7. 2002 腾讯：PSTN 是 Web 会员服务的支付与凭证生成器

这轮最直接属于中文旧 Web 的交叉 artifact，是腾讯的 168 Q币路径。

新浪科技 2002 年 4 月同期说明：

- 拨 `16896366`；
- 系统念出一个 12 位数字串；
- 用户最好提前准备纸笔；
- 按 `1` 可以重听；
- 费用 1 元/分钟；
- 累积 Q币后，到腾讯网站会员服务中使用，完成会员注册或续费。

来源：  
<https://tech.sina.com.cn/it2/2002-04-30/113827.shtml>

另一篇 2002 年教程记录北京及其他城市的声讯号码和“取得 12 位串 → 到腾讯网站注册”的操作：  
<https://tech.sina.com.cn/it/t/2002-03-21/107815.shtml>

### Evidence

- grade: B / contemporaneous technical press and tutorial
- confidence: high for publicly advertised user workflow

### 新事务拓扑：human-mediated cross-protocol credential transfer

```text
PSTN call
→ telecom billing
→ IVR generated / delivered token
→ human hears token
→ paper stores token
→ human retypes token into Web
→ Tencent membership state changes
```

这里：

- 电话账单承担支付轨道的一部分；
- 语音承担凭证交付；
- 纸笔承担临时存储；
- 人承担协议转换；
- Web 承担最终账号状态变化。

因此可以正式记录：

**historical Web transaction can depend on an off-Web credential-generation surface.**

这比 `Web form != completed transaction` 更具体，也更适合 old-Web archaeology。

---

## 8. 保存失败模式：一个“网页保存得很好”的服务仍然可能无法复原

### 8.1 voice-interface loss

缺：

- 原始播报音频；
- 菜单层级；
- 语音速度；
- 错误提示；
- 重听 / 返回动作；
- timeout。

### 8.2 IVR state-machine loss

缺：

- 输入长度验证；
- 错误次数限制；
- 无记录分支；
- 数据未装载分支；
- 高峰排队 / 拒接逻辑。

### 8.3 billing-state loss

缺：

- 从哪一秒开始计费；
- 本地话费与信息费怎样叠加；
- 失败呼叫是否计费；
- 运营商 / 内容提供商如何分账。

### 8.4 backend-synchronization loss

缺：

- 教育部门何时导出数据；
- 文件 / 专线 / 数据库如何传送；
- 何时装载；
- 谁核验；
- Web / SMS / IVR 是否共享同一数据副本。

### 8.5 human-transcription loss

腾讯 Q币案例提醒：真正的跨系统接口可能只是**一个人拿纸抄 12 位数**。

Web archive 不会自动保存这一步。

---

## 9. 新方法判断式

本轮建议在此类案例中保持以下不等式：

```text
historical help page captured
!= historical voice service captured
```

```text
access number known
!= IVR tree known
```

```text
IVR tree known
!= backend database state known
```

```text
query succeeded in report
!= population-level reliability known
```

```text
Web membership page captured
!= payment / credential origin was Web
```

```text
same result data on Web + SMS + voice
!= same interface, same cost, same latency or same executability
```

---

## 10. 与 Web 大众化的直接交叉：电话没有在网页出现时退出

### 2006 安徽

高考成绩同时提供 168 与 Web 查询。  
<https://gaokao.eol.cn/an_hui/200606/t20060624_185451.shtml>

### 2008 广西及多省

当年仍广泛存在：

- Web；
- 168 声讯；
- SMS；
- 号码百事通 / 其他热线；
- 招办现场。

汇总入口：  
<https://zsb.jxvct.edu.cn/news/2011/03/0321G2011.html>

### 2015 甘肃

Web 已经是明确正式查询入口，但 168、12580、1161148 与县区招办仍并存。  
<https://gaokao.eol.cn/gan_su/dongtai/201506/t20150621_1277776.shtml>

### 解释

这说明 old-Web 的研究对象不能默认是：

> Web 把旧渠道全部替换。

更常见的历史形态可能是：

> **同一制度数据库在多个终端上暴露不同接口。**

因此网页考古必须把“页面所处的渠道组合”也当成上下文。

---

## 11. 海外比较：France-Examen 2005 的 Minitel + Web + voice + SMS

法国 2005 年考试结果服务是很好的反例：即使 Web 已经成熟，同一结果仍同时通过 Minitel、网站、语音电话和 SMS 发布。

01net 2005 年采访 France-Examen 负责人时记录：

- Web 峰值约 46,000 simultaneous sessions；
- voice 峰值约 300,000 simultaneous calls；
- 整个周期预计约 1.2m Minitel calls；
- 800k voice calls；
- 500k SMS。

来源：  
<https://www.01net.com/actualites/loic-jauson-france-examen-nous-diffusons-plus-de-2-25-millions-de-resultats-scolaires-284467.html>

1999 年《La Dépêche》还报道 Minitel 和移动电话已经减少部分学生守在学校公告板前等待结果的行为：  
<https://www.ladepeche.fr/article/1999/07/06/204049-la-ruee-vers-demain.html>

### 比较价值

它支持一个跨国方法结论：

**multi-channel persistence is normal; Web arrival does not define a clean media replacement date.**

但不要把法国 Minitel 与中国 168 当成同一系统：

- Minitel 是屏幕式双向终端；
- 168 是电话语音 / DTMF 服务家族；
- 终端普及、计费、运营制度、协议栈不同。

比较的是“多渠道制度信息接口”，不是品牌等价。

---

## 12. 当前 evidence register

| Claim | Source | Grade | Confidence | Missing |
|---|---|---:|---:|---|
| 1998 168 已实现全国地市以上城市联网 | 国家统计局 | A | high | protocol/vendor/use-rate |
| 2000 南京中考可输入座位号电话查分，早于纸面条 | 扬子晚报 / 新浪 | B | high | original IVR/audio/manual |
| 2003 江苏 voice/SMS 渠道竞争及收费拥堵 | contemporaneous press | B | high | original contracts + IVR logs |
| 2004 江苏要求双音频、双身份键、本地库、扩容 | 扬子晚报 / 新浪 | B | high | platform manual/backend architecture |
| 2007 个体发生重复拨号、计费、亲友并行查询 | 中国青年报 | B | medium-high | population distribution/CDR |
| 2002 168 生成 Q币数字串后到 Web 使用 | 新浪科技同期教程 | B | high | Tencent / carrier primary backend docs |
| 2006—2015 Web 与 voice/SMS/线下长期并存 | education portals / admissions-derived notices | B | high | province-by-province systematic dataset |
| France 2005 Minitel/Web/voice/SMS coexist | 01net interview | B | high | provider raw traffic logs |

---

## 13. Archive / artifact probe 状态

### 本轮取得

- 当前仍可访问的同期新闻文本；
- 号码、用户步骤、资费、身份字段、容量描述；
- 多年份跨渠道服务说明；
- 一个明确的电话 → Web 凭证桥案例。

### 本轮未取得

- 1998—2005 运营商 168 原始历史站点 capture；
- 2000 南京 168 原始 IVR audio；
- 2004 江苏 168 菜单树 / CTI 配置；
- 2002 腾讯 168 Q币的运营商原始帮助页 / 后台规范；
- 可验证 `capture_datetime + original_url + HTTP/replay + charset + DOM + subresources` 的两时点 168 Web artifact pair。

因此继续保持：

**M1 NOT ACHIEVED.**

尤其不能写：

> “Wayback 没保存 168。”

本轮只证明：**本轮尚未取得并验证满足 METHOD 合同的 capture。**

---

## 14. 后见之明风险

### 风险 A：URL bias

今天能搜索到的是新浪、学信网、教育在线等 Web 页面，因此很容易把历史服务理解成“网页发布了一串电话号码”。

对当时用户来说，真正操作的系统可能从始至终没有 URL。

### 风险 B：smartphone IVR projection

不要用今天 10086 / 银行客服的菜单结构倒推 2000 年 168 菜单。

### 风险 C：digital = Internet

自动声讯很可能高度数字化，但 end-user Internet 与电信自动信息服务必须分开。

### 风险 D：service name continuity

“168”是接入号码家族 / 信息服务品牌，不足以证明全国各地同一厂商、同一后端或同一菜单。

### 风险 E：reported number = original interface artifact

新闻里的 `16887799` 证明号码当时被公开报道；它不等于原始电信帮助页被保存。

---

## 15. 这改变了 OWA 的哪一点理解

此前很多旧网研究天然以：

```text
URL → page → form → backend
```

作为服务模型。

本轮要求补一个同样真实的 1995—2015 中文数字服务模型：

```text
telephone number → IVR prompt → DTMF → private DB → spoken result
```

以及两者的桥：

```text
telephone number → billed voice token → paper note → Web field → account state
```

这意味着中文旧 Web 的边界环境不仅包括：

- 浏览器；
- Flash；
- ActiveX；
- charset；
- modem；

还包括**同时代电话网提供的交互信息面**。

不是因为本仓要改成“电信史仓库”，而是因为一些 Web 服务在历史上根本无法只靠 Web 完成。

---

## 16. 下一步最高价值 artifact

按收益排序：

1. 中国电信 / 地方电信 1990s—2000s `168` 原始用户指南或业务手册；
2. 电话簿 / 黄页中自动信息台的分类和子号码；
3. 168 CTI / audiotex 平台厂商手册；
4. 原始 IVR 录音或录音转写，带日期和来源；
5. 2002 腾讯 168 Q币原始腾讯帮助页历史 capture；
6. 2000—2004 高考查分运营商原始帮助页；
7. 教育成绩数据库 → 运营商声讯 / SMS / Web 的同步协议或招标文件；
8. 同一省份 2000、2005、2010 两到三个历史时点的渠道拓扑，形成真正可比较 timeline。

如果拿不到这些，保留“voice interface unrecoverable”本身就是正式考古结论，不补造菜单。

---

## 17. HPL 交叉链接

普通生活史的对应切片：

- `sources/telephone-audiotex-168-exam-results-and-interactive-information-before-mass-web-china-1998-2015.zh-CN.md`

那里重点解释：

- 为什么早知道一天有生活价值；
- 家庭如何在拥堵时并行拨号；
- 电话查询怎样位于广播与 Web 之间；
- 同一人生状态怎样通过 voice / SMS / Web / school 多渠道获得。

本仓只保留与中文旧 Web 技术、交互和保存边界直接相关的部分。