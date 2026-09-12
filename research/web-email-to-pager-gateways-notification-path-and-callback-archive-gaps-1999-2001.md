# Web / Email → Pager 网关、通知路径与回呼档案缺口（1999—2001）

> Research checkpoint，不是完整 case。研究对象仍严格服务于本仓约 1995—2015 中文互联网 scope：不是把无线寻呼史整体并入 old-web，而是研究**中文 Web / Email 如何在 1990 年代末成为既有无线寻呼网络的新入口，以及为什么仅保存网页不足以保存一次真实的跨协议消息事务。**

## 0. 为什么这不是另一个 `page != transaction`

本仓已经有：

- [`168-audiotex-ivr-web-bridge-and-voice-interface-archive-gap-1998-2015.md`](168-audiotex-ivr-web-bridge-and-voice-interface-archive-gap-1998-2015.md)：Web / 电话 / IVR / 私有数据库；
- [`ip-telephone-cards-201-campus-phones-public-phone-bars-and-cross-protocol-service-topology-1999-2008.md`](ip-telephone-cards-201-campus-phones-public-phone-bars-and-cross-protocol-service-topology-1999-2008.md)：Web / 零售卡 / PSTN / IVR / 电信网；
- 多个 `page visible != transaction complete` 类状态专题。

如果本文件只写：

> “网页上点发送 ≠ 对方真的收到”

那没有新增价值。

本切片新增的是一种更具体的历史服务拓扑：

```text
Web / email sender
       ↓
Internet-facing gateway
       ↓
paging backend / addressing database
       ↓
radio paging network
       ↓
one-way pager
       ↓
human reads alert
       ↓
finds a telephone
       ↓
PSTN callback
```

这里的发送端、递送端、回复端甚至不在同一种网络上。

本轮暂称：

**cross-protocol endpoint asymmetry / 跨协议端点不对称**。

它的核心不是“网页是不是最终事务”，而是：

> **一次历史通信的发起界面可能是 Web，最终接收界面却根本不是 Web；回复又再次跳到电话网。**

---

## 1. 与 METHOD 的关系

按 `docs/METHOD.md`，本轮必须把下列证据对象分开：

1. 1999 年行业统计公报中对“网上寻呼”“电子邮件到达呼”的描述；
2. 今天仍可读取的新浪 / CNNIC 等历史文本表示；
3. 1999 年“国信网源”真实 Web 页面；
4. pager gateway 的服务端实现；
5. 无线寻呼基站 / 广播链路；
6. 具体 pager 屏幕上是否收到；
7. 用户是否随后找到电话并回拨。

当前只取得 1—2 和普通生活层面的同期报道。

**没有取得**：

- `国信网源` 的已验证 1999 historical capture；
- 原 hostname / URL 的可靠 contemporaneous locator；
- HTML / charset / form field / CGI endpoint；
- Web submit 后的 server response；
- Email-to-pager gateway 协议与字段映射；
- pager delivery log / acknowledgement semantics；
- 同一服务两个历史时点的 capture；
- 原始 pager client（终端）界面 artifact 与同一条消息的端到端 provenance。

因此：

**M1 historical Web-to-pager service artifact: NOT ACHIEVED IN THIS SLICE.**

这是一份 research checkpoint，不升级为 complete case。

---

## 2. 1999 年的强锚点：主管部门公报明确记录 Web / Email 已进入寻呼网

《一九九九年通信业发展统计公报（摘要）》记录，中国联通国信寻呼公司当时：

- 无线寻呼覆盖全国 335 个地市、2022 个县市；
- 280 MHz 198、199 网覆盖 287 个城市，容量 1700 万户；
- 开通“国信网源”网站；
- 截至 1999 年底，**网上寻呼**已经开通到 198、199 全国寻呼网、27 个省网及部分本地网；
- **电子邮件到达呼**已经开通 22 个省网。

来源：信息产业部综合规划司资料，《一九九九年通信业发展统计公报（摘要）(下)》，CCID / 新浪，2000-06-14。  
<https://tech.sina.com.cn/it/2000-06-14/28155.shtml>

### Evidence

- source class: contemporaneous institutional statistical bulletin, preserved via contemporaneous portal republication
- grade: A-/B+
- confidence: high that the service categories and stated coverage existed by end-1999
- does **not** establish original webpage structure, protocols, tariffs, authentication, message length, encoding or end-to-end delivery semantics

### Method boundary

这条证据足够证明：

```text
Web/email origin → paging network
```

但还不足以证明：

```text
specific historical form → specific CGI → successful radio delivery → human saw it
```

因此严禁把行业公报中的服务名称画成一个“已复原网站截图”。

---

## 3. 1998 年基线：无线寻呼不是边缘设备，因此 Web gateway 连接的是一个真实的大众基础设施

国家统计局 1999 年总结 1998 年通信业时记录：

- 无线寻呼用户 3908 万户；
- 280 MHz 高速寻呼网已在 22 个省会以上城市联网运行；
- 126、127、198、199 等系统基本形成全国范围无线寻呼服务网络；
- 同期中国公用计算机互联网已通达全部省会城市。

来源：国家统计局，《之十一：邮电通信业突飞猛进》。  
<https://www.stats.gov.cn/zt_18555/ztfx/xzg50nxlfxbg/202303/t20230301_1920449.html>

CNNIC 第三次统计报告则记录，截至 1998-12-31，中国上网用户为 210 万。

来源：CNNIC，《第三次中国互联网络发展状况调查统计报告》。  
<https://www3.cnnic.cn/n4/2022/0401/c88-812.html>

### 为什么这对 old-Web 考古重要

Web-to-pager 不是一个“互联网用户之间的边缘插件”。

它可能把一个规模仍明显更窄的 Internet 发送端，接到了规模大得多的无线寻呼接收端。

因此研究 1999 中文 Web 时，必须允许出现：

```text
sender is a Web user
recipient is not a Web user
transaction nevertheless crosses the Internet boundary
```

这叫：

**recipient-side Internet invisibility / 收件人侧 Internet 不可见**。

如果只按“谁上网”统计 Internet 的社会作用，会漏掉这种网关型外溢。

---

## 4. 2000 CNNIC：“网上寻呼机”已经成为公开统计中的网络服务类别

CNNIC 2000 年 7 月报告中，“用户最常使用的网络服务（多选）”包括：

- Email 87.65%；
- BBS 21.17%；
- **网上寻呼机 20.72%**；
- 网上炒股 14.64%；
- 网络电话 9.63%。

报告还给出 1999.7 与 2000.7 比较，网上寻呼机由约 15% 上升到约 21%。

来源：CNNIC，《中国互联网络发展状况统计报告(2000/7)》，新浪保存版本。  
<https://tech.sina.com.cn/internet/china/2000-07-27/31904.shtml>

### Sample caveat

报告说明当次采用网上联机调查与抽样调查等方法，联机调查有效答卷 573,902 份，抽样调查有效答卷 3,679 份。

因此：

```text
20.72% != 20.72% of Chinese population
```

本仓只使用它证明两件事：

1. “网上寻呼机”在 2000 年已是 CNNIC 能够独立列出的网络服务类别；
2. Web / Internet 与寻呼在当时人的服务分类中确实发生了交叉。

当前**不能**仅凭该分类判断它对应：

- 国信网源；
- OICQ；
- 某个门户的寻呼服务；
- 多种产品之和。

因此：

**survey category != identified historical product.**

---

## 5. 一次 Web-to-pager 事务至少有五个独立状态

如果未来取得一张历史“网上寻呼”页面，本仓不应只记录 `form works / form broken`。

最低状态链应拆成：

```text
S0  sender sees historical page
S1  sender supplies recipient pager identity / message
S2  Web frontend accepts submission
S3  gateway accepts / transforms message
S4  paging backend schedules radio delivery
S5  pager radio endpoint receives / displays message
S6  human notices / understands message
S7  if reply required, human finds another terminal
S8  callback reaches sender or intended third party
```

这产生几个不能合并的不等式：

```text
form submission != gateway acceptance
```

```text
gateway acceptance != radio transmission
```

```text
radio transmission != pager reception
```

```text
pager reception != human attention
```

```text
human attention != callback completion
```

这些不是为了制造更多 state-gap 文件，而是为了防止考古者把**跨协议事务**误缩成一个 HTTP request。

---

## 6. `notification-path archive gap / 通知路径档案缺口`

普通 Web archive 擅长保存：

- HTML；
- 图片；
- CSS；
- 部分 JavaScript；
- 可抓取链接。

但一次 1999 网上寻呼真正决定用户体验的层，可能包括：

- pager number / account database；
- Web-to-pager gateway；
- 字符截断 / 编码转换；
- message queue；
- provincial vs national paging route；
- 无线频点与覆盖；
- pager battery / 开机状态；
- 数字机还是汉显机；
- 接收后用户附近有没有电话；
- 公话是否排队；
- 回拨话费；
- 最终 callback 是否接通。

其中多数不会进入 WARC。

因此本轮固定：

**notification-path archive gap / 通知路径档案缺口**。

即：

> Web archive 可能保存“发送寻呼”的入口，却几乎必然不完整保存从 Web submit 到无线接收再到人类回呼的全路径。

---

## 7. 一个特别危险的误判：`recipient endpoint == browser`

现代研究者看到历史网页上的“给他留言”“发消息”“寻呼”按钮，很容易默认：

> 对方也是打开网页收消息。

1999 国信公报明确告诉我们，至少存在另一种 topology：

```text
browser / email
     ↓
paging gateway
     ↓
radio pager
```

所以未来任何 1998—2001 中文站点出现下列词语时：

- 网上寻呼；
- 网络寻呼机；
- 呼机留言；
- BP 机留言；
- Email 到达呼；
- 无线寻呼；

都应该先问：

> **recipient endpoint 到底是什么？**

可能是：

- browser；
- desktop IM client；
- pager；
- mobile phone；
- email inbox；
- operator console；
- several endpoints at once。

不能只根据 sender UI 推断 recipient UI。

---

## 8. 回呼意味着事务真正延伸到了 Web archive 之外的物理城市

2000 年《北京晚报》对北京西站公用电话乱收费的同期调查，记录一名旅客在公用电话处：

1. 打了一个传呼；
2. 接了回电；
3. 为这组动作被摊主收费。

电信投诉热线给出的标准中，一次寻呼与接回电分别都有费用 / 手续费项目。

来源：《北京西站一公用电话亭真黑 长途电话4分钟开价96元》，2000-10-26。  
<https://news.sina.com.cn/society/2000-10-26/138549.html>

### Archaeological meaning

即使一条 page 是从 Web 发出的，真实的“完成”仍可能需要：

- 收件人看见 BP 机；
- 改变行走路线；
- 找到公用电话；
- 排队；
- 付费；
- 回拨。

因此：

**historical message delivery had a physical last mile.**

本仓在重建老网页交互时，应避免把“数字事务”理解成完全在屏幕中闭合。

---

## 9. 数字机 / 汉显机差异意味着同一网页消息可能到达不同能力的终端

2025 年玉屏地方文史回顾记录：

- 多数数字 BP 机主要显示回拨电话号码；
- 汉显机可以显示文字留言；
- 汉显服务费明显更高；
- 当地 1995 年开通数汉兼容与 127 自动寻呼。

来源：杨显政，《感受通信工具的变化》，玉屏网。  
<https://www.yp.gov.cn/contents/2025/03/17/receive-1764843f-1b66-4998-ac9b-01927ef7a29b.html>

### Evidence caveat

- 后期地方文史，不是 1999 原始产品说明；
- 用于建立“endpoint capability varied”的问题意识；
- 不用来推断国信网上寻呼具体如何向不同机型编码。

### 新的 artifact 字段

以后若取得 Web-to-pager 页面，应至少记录：

```yaml
recipient_endpoint:
  pager_network: unknown
  pager_number_format: unknown
  pager_type: unknown   # numeric / alphanumeric / mixed
  message_character_limit: unknown
  message_encoding: unknown
  truncation_behavior: unknown
  callback_number_field: unknown
  delivery_receipt_visible_to_sender: unknown
```

这些字段不能从今天的常识补猜。

---

## 10. 海外比较只作为边界校验：1997 SkyTel 已明确实现 Web / Email → pager

WIRED 1997 年对美国无线数据服务的实测记录，SkyTel 双向 pager 可以：

- 从 Email 收消息；
- 从 SkyTel Web site 收消息；
- 从 800 电话收消息；
- 在 pager 本机直接回复，而不再需要找电话。

来源：Simson Garfinkel, “Wireless Gets Real,” *WIRED*, 1997-10。  
<https://www.wired.com/1997/10/es-wired/>

这对本仓只有两个比较用途：

1. `Web / email → pager` 并不是中国独有的网络融合方向；
2. two-way pager 恰好说明 one-way pager 的关键缺口就是“回复仍依赖另一个终端”。

OWA scope 仍然是中文旧网，不在此扩写全球 pager 史。

---

## 11. OICQ / “网络寻呼机”只作为高价值 locator，不在本轮升级为核心证据

现代二手资料普遍把 1999 OICQ 描述成“网络寻呼”软件，部分文章进一步声称早期版本可向 BP 机留言。

本轮没有取得：

- 1999 OICQ 原始帮助文件中对无线 pager gateway 的说明；
- 对应服务端协议；
- 同期广告 / 手册对 BP 机互通的明确操作步骤；
- 可验证的在线服务 capture。

因此本轮不把：

```text
OICQ == proven BP-pager gateway
```

写入 confirmed layer。

但它是下一轮很高价值的 artifact 方向：

- 原始 99a 安装包；
- help/resource string；
- 菜单 / dialog；
- 同期软件评测；
- 服务端 locator；
- `oicq.com` / `oicq.net` 历史 capture。

这正符合仓库“artifact first, memory later”的推进方式。

---

## 12. 当前可确认 / 可推断 / 未知

### Confirmed

1. 1998 年中国无线寻呼已形成千万级用户和全国性网络。
2. 1999 年底，国信寻呼已开通“网上寻呼”和“电子邮件到达呼”。
3. 2000 CNNIC 报告把“网上寻呼机”列成独立网络服务类别。
4. 现实寻呼事务可与公用电话 / 回电形成完整生活工作流。
5. 海外同期存在明确 Web / Email → pager 服务，说明这种跨协议网关在技术史上并非孤例。

### Probable / strong inference

1. 中文 Web 在 1999—2000 已存在多个把 Internet sender 接到非-Web recipient 的通信场景。
2. 一部分“网络寻呼”用户体验由 Web frontend、私有 gateway、无线网络和电话回呼共同组成。
3. 只保存 sender page 会系统性高估 Web 作为完整事务环境的自足性。

### Unknown

1. “国信网源”原 URL / hostname；
2. 原页面布局、charset、JS、form action；
3. 是否需要登录、pager network selection、收费；
4. message encoding / length；
5. Email 到达呼具体传递内容；
6. delivery receipt / error state；
7. radio backend protocol；
8. pager model compatibility；
9. callback 是否能与 Web sender identity 自动绑定；
10. 同一服务第二个历史 capture 时点。

---

## 13. M1 artifact probe 状态

本轮进行了 locator 搜索：

- `国信网源`；
- `网上寻呼 198 199`；
- `电子邮件到达呼`；
- 1999 行业统计公报；
- OICQ / 网络寻呼相关二手线索。

取得了：

- 1999 行业统计公报的同期 Web 转存；
- 2000 CNNIC 完整统计报告的同期 Web 表示；
- 2000 北京西站寻呼 / 回电现场报道；
- 后期地方文史的 pager endpoint 行为说明；
- 1997 美国 Web / Email → pager 比较材料。

**没有取得一份满足 M1 的 1999 中文网上寻呼原服务 capture。**

所以必须写：

> `M1 historical Web-to-pager service capture: NOT ACHIEVED IN THIS SLICE.`

而不是：

> “Wayback 没有保存”

也不是：

> “国信网源页面已经复原”。

---

## 14. 下一轮最值钱的 artifact 搜索顺序

1. 从同期报刊 / 软件杂志 / 电话黄页定位“国信网源” hostname；
2. 用确定 hostname 做 Wayback / other archive capture search；
3. 找 1999—2001 网上寻呼业务使用说明 / 资费单；
4. 找 Email 到达呼说明；
5. 找 198 / 199 用户手册与 pager 编号格式；
6. 找 OICQ 99a 原始安装包、help、resource string；
7. 若取得页面，按 `docs/METHOD.md` 做两个时点、HTTP/replay、charset、子资源、表单/action、missing resources、browser assumptions；
8. 把 sender UI 与 recipient endpoint 分开记录，不因为同一服务名而强行合并。

---

## 15. 对 old-Web archaeology 的新增方法结论

本轮可以固定四条以后可复用的边界：

```text
sender interface != recipient interface
```

```text
Web submission != radio delivery
```

```text
historical Web page captured != historical notification path captured
```

```text
Internet-mediated communication != both humans were Internet users
```

以及一个研究提醒：

> **老 Web 并不总是一个自足世界。很多网页只是进入其他通信基础设施的入口；收件人可能活在另一种终端、另一种协议、另一套资费和另一条物理最后一公里里。**

这也是本轮对仓库 scope 的价值：它没有把研究对象扩大成“全球无线史”，而是把 1999—2001 中文 Web 的真实系统边界画得更准确。
