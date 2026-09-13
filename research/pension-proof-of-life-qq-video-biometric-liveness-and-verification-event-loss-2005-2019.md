# 养老金“生存认证”的旧网考古：QQ 视频、生物识别与 verification-event loss（2005–2019）

> Scope：本 note 只讨论约 1995–2015 中文旧网及其延伸接口里，养老金领取资格怎样借助联网软件、网页说明、生物识别和远程通信完成；不把仓库扩展成一般养老金史。
>
> Cross-link：ordinary-life 背景见 `tmzncty/how-people-lived`：`sources/pension-proof-of-life-recurring-eligibility-and-retirement-mobility-china-2004-2026.zh-CN.md`。

## 0. 为什么这是一个 old-Web 问题，而不只是“政务数字化”

资格认证的关键不是“有没有一个网页”，而是：**某个活着的人，在某个时刻，怎样被远处的制度确认仍然活着。**

这类事务特别容易被 Web 考古误读，因为真正决定结果的东西往往不在可保存页面里：

- 本人的身体是否出现在现场或镜头里；
- 摄像头是否实时；
- 指纹/人脸模板是否匹配；
- 经办人员是否认可；
- 另一个部门的数据是否显示近期活动；
- 后台是否把资格状态续到下一周期。

因此本 note 把研究单位从 `page` 扩展到一个更具体的 **verification event / 验证事件**。

核心警告：

```text
historical instruction page recovered
!=
historical liveness verification reconstructed
```

以及：

```text
screenshot of a living person
!=
proof that a contemporaneous liveness event was accepted
```

## 1. 证据合同

### A 级

- 2004 年劳动和社会保障部异地退休人员协助认证通知的官方现存文本；
- 2018 年人社部门取消集中认证的政府发布；
- 2019 年地方政府公开的手机人脸认证操作步骤。

### B 级

- 2005 年太原指纹养老金认证同期报道；
- 2007 年临汾—哈尔滨 QQ 视频认证同期报道；
- 2008 年异地退休人员第一人称/家属认证困难报道；
- 2018–2019 年媒体对视频、刷脸、上门与多通道认证的同期采访。

### 当前没有声称取得的证据

- 没有把任何今天仍在线的 2005–2009 新闻页冒充成当年 capture；
- 没有取得 2007 临汾认证时的 QQ 客户端镜像、聊天日志、截图原件或视频文件；
- 没有取得当年养老金指纹系统的数据库、算法、客户端或供应商手册；
- 没有取得 2019 手机刷脸系统的模型版本、阈值、模板或后端审核记录。

## 2. 2004 的纸面协议：网络化之前，资格状态怎样移动

劳社厅发〔2004〕8号规定，异地居住退休人员原则上每年至少进行一次领取养老金资格协助认证。养老金关系所在地在截止日前 60 天寄出信函与认证表；本人拿身份证、退休证和表格到现居住地街道/乡镇或县区社保机构，当面核验、盖章、签字，再把一份表寄回原参保地；逾期未收到可暂停待遇。

官方现存文本：
https://jlsi.jl.gov.cn/zcfgjjd/qyzgylbx/200701/t20070110_7261898.html

这是后续数字化的基线状态机：

```text
origin agency creates request
→ postal delivery
→ body appears before local verifier
→ documents checked
→ local verifier writes/stamps assertion
→ assertion returns by post
→ origin agency changes pension-eligibility state
```

注意：这里“证明人还活着”的核心 artifact 不是身份证本身，而是**一个近期、带地点和见证机构的 assertion**。

因此后续视频、人脸识别和数据比对，其实是在不断替换这个 assertion 的生产方式。

## 3. 2005 指纹系统：biometric identity 不是 liveness 的完整同义词

2005 年《山西晚报》报道，太原部分地区开始对离退休人员采集双手食指/中指指纹，用养老金身份认证识别系统进行后续认证；首次录入仍要求本人携身份证、户口簿到场。

同期报道：
https://news.sina.com.cn/c/2005-10-19/02247204877s.shtml

对旧系统考古应至少区分：

1. **enrollment**：第一次把某人的法定身份与生物特征模板绑定；
2. **verification**：后来再次采集特征，与模板比较；
3. **eligibility update**：比对结果是否真的让养老金状态继续有效。

只恢复一张“指纹认证系统”界面截图，无法证明第二、第三步当时怎样运行。

并且：

```text
fingerprint match
!=
full semantic proof of “currently alive”
```

指纹认证能强化“来的人是不是同一个人”，但制度仍需要一个近期发生的采集事件，才把它解释成“此人仍健在”。

## 4. 2007 临汾案例：消费级 QQ 被临时拼装成政务验证通道

2007 年 3 月的同期报道记录：为了确认一名居住哈尔滨的 97 岁退休老人仍健在，山西临汾市企业养老保险管理中心使用 QQ 视频与哈尔滨连线；工作人员要求老人动一动、眨眼，并请两名认识他的老同事参与确认；画面被截取、放大。

同期媒体：
https://news.ifeng.com/society/4/200703/0320_346_90450.shtml

这不是“官方网上养老金系统已经建成”的证据。

更准确的对象是：

**consumer-protocol bricolage / 消费通信协议的制度拼装**。

```text
现成 QQ 账号与视频功能
+ 两端普通 PC/摄像头/Internet
+ 经办人员
+ 认识退休者的旧同事
→ 临时组成可接受的远程见证链
```

这提醒旧网研究者：**重要的网络事务不一定发生在专门政府网站上。**

一个社会流程完全可能借用 IM、邮件、FTP、论坛私信等已有消费通信工具，然后由线下机构赋予它制度效力。

如果只抓 `gov.cn`，会漏掉这种历史。

## 5. verification-event loss：真正决定资格的“事件”几乎没有被保存

2007 报道说工作人员看到了实时老人、让其动作，并留下截图。

但对于 2026 年的考古者，即使未来找到那张截图，也只能证明：

- 某张静态图里出现过一个老人；
- 可能存在某次 QQ 会话；
- 图像可能和报道事件相关。

它**不能自行恢复**：

- 画面是否当时实时传输；
- 谁坐在另一端；
- 经办人员怎样判断动作是实时响应；
- 两位旧同事怎样确认身份；
- 截图是否来自同一次会话；
- 该会话最终是否被写入社保系统并延长资格。

因此新增：

## `verification-event loss / 验证事件丢失`

定义：历史系统的制度意义取决于一个同时发生、由参与者共同确认的事件；后世保存了部分 UI、文本或静态媒体，却没有保存“这个事件当时如何被接受”的完整状态链。

公式：

```text
UI preserved
+ still image preserved
+ policy description preserved
!=
accepted verification event preserved
```

它和 `transaction-state loss` 相近，但更强调**实时身体输入 + 人类/算法判断 + 当时性**。

## 6. “活体”为什么是 Web archive 很难保存的对象

养老金生存认证特别适合提醒我们：浏览器历史并不只由文档构成。

一个远程活体认证至少有这些层：

```text
public instruction page
client software / App
camera / fingerprint sensor
body movement or biometric sample
network session
matching / review backend
institutional decision
eligibility database write
```

Wayback 最容易保存的是第一层。

最难保存的恰恰是后面决定事务是否成立的层。

所以对于这类系统，`Memento` 的对象边界必须写清：保存的是帮助页、下载页、客户端壳、结果页，还是一次真实认证？不能用同一个“网页保存了”覆盖所有层。

## 7. 2008 同期旧新闻页：body burden 已经成为公开争论

2008 年新浪仍在线的《异地领取养老金先要证明自己活着》记录一名 81 岁退休者：每年由女儿陪同打车去办理“健在”证明，再寄回原参保地；当年因社区、派出所和社保部门之间的证明权限衔接不清，老人一度办不下来。

current-live legacy representation：
https://news.sina.com.cn/s/2008-07-01/072914098176s.shtml

该页面今天仍带有典型 2008 新浪导航、Google 搜索入口、短信/播客/通行证等页面壳，但本轮**没有核验其 2008 archive capture**，因此它在本 note 中只能作为：

```text
currently reachable legacy page carrying contemporaneous-dated article body
```

不能据此声称整个 2008 DOM、广告、iframe 和子资源均保持原样。

这类页面很适合作为未来 `current live legacy vs historical capture` diff 候选。

## 8. 2018 的转折：interface success 可以表现为“界面消失”

2018 年人社部全面取消集中资格认证，目标不是停止资格核实，而是更多依靠信息比对、社会化服务、远程认证与上门服务。

官方/政府转载：
https://rst.ln.gov.cn/rst/zxzx/zfhy/7BC52398F5CA46D68847BB2C358B17AA/index.shtml

人民日报同期报道还记录，有退休人员被要求录制手持身份证、眨眼、说话的视频，有异地老人每年返回原工作地办理，也有老人因窗口系统维护白跑。

同期报道：
https://politics.people.com.cn/n1/2018/0619/c1001-30065547.html

这里出现一个对 old-Web 很重要的反直觉：

## `successful interface disappearance / 成功的界面消失`

在传统 Web 史里，功能越来越成熟似乎应该留下更多页面。

但“寓认证于无形”的目标恰好相反：

```text
过去：用户主动打开/到达某个认证界面
未来：其他数据库已经足够证明近期状态
→ 用户不需要操作
```

因此：

**absence of user-facing page can be the designed success state of the service.**

如果未来只统计“有多少公开办事页面”，会低估真正后台数字化程度。

## 9. 2019 手机刷脸：一个短流程背后是多个不可见状态

重庆潼南 2019 年政府说明把手机认证写成四步：

1. 下载注册“重庆掌上12333”；
2. 手机号 + 身份证实名认证；
3. 签领电子社保卡；
4. 进入养老金资格认证，对镜头眨眼。

官方页面：
https://www.cqtn.gov.cn/zwgk_184/zcjd/wzjd_tnqzf/201905/t20190529_5868021_wap.html

表面上它像一个很简单的 UI flow，实际至少涉及：

```text
phone-number account
→ legal-identity binding
→ e-social-security-card state
→ camera permission
→ face template / identity source
→ liveness prompt
→ biometric decision
→ pension eligibility write
```

所以新增方法警告：

```text
frontend flow recovered
!=
biometric decision system recovered
```

需要分别记录：

- App/版本；
- OS 要求；
- 是否允许借他人设备；
- 摄像头权限；
- 人脸底库来源；
- 活体动作提示；
- 失败码；
- retry / fallback；
- 最终资格状态；
- 是否需要人工复核。

2019 哈尔滨材料明确说，使用老年机或非安卓手机者可借亲友/社区工作人员的安卓设备认证。这证明 **device identity != legal identity**：设备可以不是本人的，而人脸和身份证状态必须指向本人。

来源：
https://chinajob.mohrss.gov.cn/h5/c/2019-10-23/132958.shtml

## 10. `body-as-ephemeral-input / 身体作为瞬时输入`

对于普通网页，输入可以是文本字段。

养老金远程认证里，人的身体本身变成输入设备的一部分：

- 眨眼；
- 转头；
- 指纹；
- 实时视频动作；
- 人脸图像。

这些输入的意义高度依赖采集时刻。

因此：

```text
body sample copied later
!=
body present then
```

这也是为什么“把一张历史刷脸页面复原出来”几乎不能复原历史事务。

复原页面最多告诉我们：系统当时要求什么。

不能告诉我们：某个退休者当时是否通过，以及为什么通过。

## 11. `witness migration / 见证者迁移`

从 2004 到 2019，可以看到“谁替制度作证”不断变化：

```text
街道/乡镇工作人员面对面核对
→ 指纹模板
→ 旧同事 + QQ 实时视频
→ 社区人员拍视频
→ App 活体算法
→ 多部门数据比对
```

这里没有简单的“人工 → 自动”直线。

人类见证、设备、算法和数据库长期混合存在。

因此 old-Web case 应记录的是：

**哪一个 actor 在这个时点承担了“我相信这个人仍健在”的责任。**

## 12. 隐私边界：不要为了考古重新公开生物识别材料

如果未来真的找到：

- 2007 QQ 视频截图；
- 指纹采集界面截图；
- 老人的身份证照片；
- 人脸认证失败日志；
- 带姓名、身份证号的认证表；

默认不应把原始个人敏感材料直接重新公开。

按照本仓 METHOD：

- 优先保存 schema、字段、流程、软件名、版本、时间和错误类型；
- 对普通人的姓名/证件号/生物图像执行研究必要最小化；
- 已删除或未公开的生物识别数据不因为“历史研究”就获得再发布许可。

这里尤其应该保存**系统怎样要求人的身体出现**，而不是保存某个普通人的身体数据本身。

## 13. 与海外 proof-of-life 的可比性

英国目前仍对部分海外 State Pension 领取者发送 life certificate，需要合格见证人签字，未返回可能暂停支付：
https://www.gov.uk/state-pension-if-you-retire-abroad/report-a-change-in-your-circumstances

法国海外养老金领取者也需要周期性 proof of life；现有在线系统可上传证明，更新的手机方案开始使用证件 + 短视频：
https://www.lassuranceretraite.fr/portail-info/hors-menu/traductions/english/proof-of-life.html

这说明：

- “养老金系统不知道海外领取者是否死亡”是跨国共同问题；
- witness、纸证、视频、App、自动数据交换都是不同的解决方案；
- 中国 2007 QQ 案例值得研究的不是“中国特别奇怪”，而是**正式接口缺位时，现成通信软件如何临时承担 institutional transport**。

## 14. 已证实 / 高概率 / 不知道

### 已证实

- 2004 年异地退休人员协助认证存在规范化纸面—邮政流程；
- 2005 年太原至少有地区开始养老金指纹认证；
- 2007 年临汾确有使用 QQ 视频确认异地高龄退休者健在的同期报道；
- 2008 年异地退休人员仍可能依赖社区/社保盖章 + 邮寄；
- 2018 年全国政策转向取消集中认证；
- 2019 年部分地区已经公开使用手机 App + 电子社保卡 + 人脸/活体动作认证。

### 高概率，但需要进一步 artifact

- 2005–2012 不同城市使用了多个并不完全兼容的生物识别/退管系统；
- 远程视频、指纹和纸面认证长期并行，而不是整齐替代；
- 初次人脸/指纹 enrollment 与后续日常 verification 在客户端上存在明显不同流程。

### 不知道

- 2007 临汾 QQ 使用的准确 QQ 版本、OS、摄像头、编码与网络条件；
- 当时是否保存视频，还是只保存截图/人工记录；
- 该次事件最终写入哪个社保数据库字段；
- 指纹系统的供应商、数据格式、模板迁移情况；
- 2019 人脸认证具体算法/阈值/失败码/人工复核比例；
- 哪些系统的历史安装包、帮助页或截图仍有合格 archive capture。

## 15. Artifact probe 状态

本轮实际取得：

1. 2008 新浪 legacy article 当前仍可访问；
2. 2004 规范的地方社保局现存 official representation；
3. 2019 地方政府手机认证步骤页面；
4. 多个同期新闻作为 B 级 evidence family。

本轮没有取得：

- ≥2 个已打开核验的 2005–2010 历史 memento；
- 当年 QQ/社保客户端页面的历史 DOM/安装包；
- 指纹或人脸系统的 period manual；
- historical runtime replay。

因此：

```text
policy/process identity: achieved
contemporaneous event descriptions: achieved
current-live legacy pages: achieved
verified historical application capture: NOT achieved
runtime reconstruction: NOT achieved
```

这不是 M1 候选的完成状态，也不声称 archive 不存在。

## 16. 下一步最值得追的窄问题

1. 找 2005–2012 “离退休人员指纹身份认证系统 / 退管系统 / 生存认证系统”供应商与软件手册。
2. 以 2007 临汾 QQ 案为 locator，找当年转载页面、截图或地方社保年报，确认这是孤立 improvisation 还是随后形成过视频认证路径。
3. 检索 2010s 初期各地“异地退管系统”公开帮助页，比较字段：姓名、身份证、退休证、照片、指纹、认证时间、状态码。
4. 对 2008 新浪 legacy page 做历史 capture 对照，区分今天页面壳与当年实际 DOM/iframe/charset。
5. 如果找到生物识别软件镜像，优先记录输入/输出 schema 和失败状态，不收集真实退休人员生物数据。

---

初稿由 AI 辅助整理；此 note 的价值主要是提出可验证的 artifact / event 区分，而不是宣称已经复原任何历史生存认证系统。