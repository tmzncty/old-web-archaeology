# Home Internet, dial-up, ADSL, broadband provisioning, and state gaps, 1995–2015

> Scope: 中文旧网约 1995–2015。
>
> Cross-link: `tmzncty/how-people-lived/topics/from-dial-up-session-budgeting-to-always-on-household-connectivity-home-internet-provisioning-china-1986-2026.zh-CN.md`
>
> 本文不写中国互联网通史，也不把 1994 年国家网络接入、1995 年公众 Internet 服务、2000s 家庭宽带和 2020s 家庭 Wi-Fi 混成一条“上网越来越快”的线。研究对象是中文旧 Web 怎样呈现拨号/ADSL/宽带的资费、报装、覆盖、账号、自助变更与线路状态，以及 archive 最容易留下什么 public shell、最难留下什么真实 provisioning state。

## 1. 为什么这值得独立建模

旧 Web 通常被研究成“页面在网上”。但一个 2006 年用户要看这些页面，本身先要解决另一套 Web 之前的基础设施问题：

`我住的地址有没有线路`
→ `这个运营商能不能进入楼里`
→ `有无空闲端口`
→ `申请是否受理`
→ `是否生成工单`
→ `技术人员能否布线/同步`
→ `账号是否开通`
→ `资费/时长/速率是什么`
→ `用户电脑能否认证上网`

因此“旧 Web 的用户”不是一个抽象浏览器主体。她还处在一套有地址、铜线、机房端口、用户名、计费策略和营业厅的接入系统中。

本题固定以下边界：

- `ISP/运营商宣传服务存在 ≠ 一个具体地址可装`；
- `小区/区域覆盖 ≠ 当前有空闲端口`；
- `申请被记录 ≠ 生成装机工单`；
- `费用已扣/已缴 ≠ 安装已完成`；
- `ADSL 技术可常在线 ≠ 用户资费允许不限时常在线`；
- `线路标称 2M/4M ≠ 长铜线/共享出口下真实可达速率`；
- `网上营业厅页面存在 ≠ 登录成功 ≠ 后端业务状态真的变更`；
- `在线提交变更 ≠ 立即生效`；
- `宽带账号有效 ≠ 每台家庭设备都可并发使用`；
- `今天同名域名仍在线 ≠ 2000s 主体、页面和 backend 连续`。

---

## 2. 研究单位

按照 `docs/METHOD.md`，本题必须拆开 platform / site / page / transaction / capture。

### 2.1 Service / platform family

至少包括：

- 163 / 169 等拨号 Internet 接入；
- 地方电信/网通 ADSL；
- “北京宽带网 / 宽带北京”一类宽带服务门户；
- 运营商网上营业厅；
- 后期光纤覆盖查询、改造申请和宽带客户端。

它们不是一个连续产品。尤其北京 2000s 固网主体经历品牌/公司重组，不能看到“北京宽带”四个字就假定后台从未变化。

### 2.2 Host / site

本轮同期材料可以定位：

- `www.bbn.com.cn` — 2004–2013 多份同期材料把它称为北京宽带网/宽带北京，并用于 ADSL 账号登录、自助办理以及后来光纤覆盖查询；
- `www.bjtelecom.com.cn` — 2006–2007 北京网通网上营业厅相关材料明确使用；
- `www.169.com` — 2001 ADSL/169 接入宣传材料中的服务 locator；
- `wokuan.bbn.com.cn` — 2013 “沃宽”客户端相关下载/服务 locator。

这些只是 historical locator。域名字符串相同不证明页面形态、主体、认证系统或后端数据库连续。

### 2.3 Page / URL type

后续 archive 检索要分别寻找：

- 拨号号码/接入说明；
- 资费表；
- ADSL 产品说明；
- 覆盖/资源查询；
- 新装申请；
- 安装条件/布线说明；
- 用户登录；
- ADSL 使用时长/速率变更；
- 密码初始化/用户名查询；
- 暂停/恢复/移机/撤机；
- 光纤覆盖查询与改造申请；
- speed test / 客户端 / 故障帮助。

### 2.4 Provisioning transaction state

建议状态机：

`public product page`
→ `address/line eligibility`
→ `customer identity/account`
→ `application attempt`
→ `server/agent accepted request`
→ `resource/port match`
→ `work order generated`
→ `installer visit`
→ `physical line completed`
→ `DSL/fiber sync`
→ `account authentication`
→ `service active`
→ `billing state active`
→ `plan/speed change request`
→ `change effective`
→ `move/suspend/cancel`

archive 通常只能保存这条链最左边的一部分。

---

## 3. 1999–2001：从拨号页面到 ADSL 页面，改变的不只是下载速度

### 3.1 拨号时代：Web 接入本身有计时状态

1999 年同期材料记录，12 月 1 日起中国电信 163 拨号用户的上网通话费由每 3 分钟 0.18 元降至 0.09 元；169、263 等其他 ISP 并不都共享同样优惠。

这意味着一个旧网页在用户侧至少还隐藏着：

`拨号号码`
+ `电话通话计费`
+ `ISP 网络使用费`
+ `modem/电话线`
+ `连接是否成功`

所以看到 1999 年某站“可访问”不能自动推成某家庭访问它的边际成本很低。

### Evidence

- B / 同时代：北京晚报，1999-11-30，《上网话费明起减半 优惠只限163》：<https://news.sina.com.cn/china/1999-11-30/36695.html>
- B / 同时代：生活时报，2000-06-22，列举北京不同拨号网络/上网卡资费：<https://www.gmw.cn/01shsb/2000-06/22/GB/06%5E1382%5E0%5ESHSB1106.htm>

### 3.2 ADSL 技术上允许“不拨号占线”，但历史产品仍可能按小时计费

2001 年北京 ADSL 同期说明强调，同一铜线可将语音和数据分开，Internet 不再像传统 modem 那样持续占用电话通话；技术上可以保持连接。

但北京 2001 年开放申请时的套餐仍包括：

- 40 小时 / 99 元；
- 100 小时 / 199 元；
- 200 小时 / 380 元；
- 超出套餐继续计费。

因此：

`technical always-on = true`

不能自动翻译为：

`economic unlimited use = true`。

这对旧 Web 的体验复原很重要。如果研究者只根据 ADSL 技术说明写“2001 用户已经可以一直挂在线上”，就会把技术能力和资费行为混掉。

### Evidence

- B / 同时代：《人民日报》2001-09-17，北京 ADSL 技术、申请和市场情况：<https://cn.govopendata.com/renminribao/2001/9/17/12/>
- B / 同时代：北京晨报，2001-08-06，早期 ADSL 40/100/200 小时套餐：<https://tech.sina.com.cn/i/c/2001-08-06/79011.shtml>

---

## 4. 2004–2007：宽带开始用 Web 管理“宽带自己”

这是本题最适合 `old-web-archaeology` 的阶段。

### 4.1 `www.bbn.com.cn`：ADSL 凭据进入 Web portal

2004 年以后多份同期材料把 `www.bbn.com.cn` 描述为“北京宽带网 / 宽带北京”，并要求现有 ADSL 用户使用自己的宽带账号/密码进入服务。

这产生一种有别于普通门户账号的身份层：

`physical access subscription`
↔ `network credential`
↔ `authenticated Web self-service`

也就是说，Web 账户不是只保存“昵称和文章”，还可能直接映射到一条真实住宅线路及其计费状态。

### 4.2 2006：网上可以改时长和速率，但 transaction 有明确后端延迟

2006-05-17 的同期材料写得很具体：北京网通市区用户可以：

- 登录 `www.bjtelecom.com.cn` 网上营业厅的 ADSL 自服务区；
- 或登录 `www.bbn.com.cn`；
- 使用 ADSL 用户名和密码；
- 在线申请修改 ADSL 使用时长和速率；
- 申请从**次月**生效；
- 当月多次修改时，以最后一次为准。

所以必须拆成：

`self-service page exists`
→ `credential accepted`
→ `change request accepted`
→ `pending until billing boundary`
→ `new plan effective`

而不是把“按钮点下去”写成线路当场完成提速。

### Evidence

- B / 同时代：北京晚报，2006-05-17：<https://tech.sina.com.cn/t/2006-05-17/1712942299.shtml>
- B / 同时代：人民邮电报，2006-05-17：<https://tech.sina.com.cn/t/2006-05-17/1755942442.shtml>

### 4.3 2007：一次 portal 改版就足以改变账号与 transaction 路径

IT168 2007-03-16 的同期操作文章记录：

- 此前用户已经可以在线改 ADSL 包月信息/时长/带宽；
- 2007 年 2 月起网上营业厅升级；
- 用户需要先在 `www.bjtelecom.com.cn` 注册门户账号；
- 再把自己的 ADSL 账号添加进“我的账户”；
- 然后进入业务受理栏目修改时长/速率。

文章还保存一个非常具体的 historical page locator：

`http://www.bjtelecom.com.cn/cnc/general/ywsl/xieyibook/xieyibook11.jsp`

这说明同一个“网上改 ADSL”的产品叙述，至少存在两种身份结构：

`ADSL credential → self-service`

和后来：

`portal account → bind ADSL credential → self-service`。

### Evidence

- B / 同时代操作文：IT168，2007-03-16：<https://wireless.it168.com/a2007/0316/792/000000792454.shtml>

### Archive implication

如果只恢复到 2007 改版后的 login shell，就不能拿它替代 2006 的账户模型；如果只找到动态 JSP URL，也不能断言其 POST、session 或 binding backend 被 archive 保存。

---

## 5. 2007–2009：计时宽带并没有立刻消失

2007 年北京网通把 512K 计时后付费客户自动提到 1M，但原 `0.05 元/分钟` 计费保持不变，并继续提供 20/40/50 小时等限时包月。

2009 年北京联通把部分计时产品提到 2M，资费仍是 `0.05 元/分钟`，用户仍可通过 `www.bbn.com.cn` 自助服务或营业厅/客服办理。

这证明 ADSL/宽带页面的历史版本必须保留**资费状态**：

`1M page`

可能对应：

- 计时后付费；
- 限时包月；
- 不限时包月；
- 融合套餐。

页面上一个“2M”标题本身并不足以告诉我们用户是否会长期保持连接。

### Evidence

- B / 同时代：中国新闻网/北京日报，2007-01-05：<https://news.sina.com.cn/o/2007-01-05/142810932345s.shtml>
- B / 同时代：C114，2009-12-01：<https://m.c114.com.cn/w80-463752.html>

---

## 6. 2008：最关键的反例——钱付了、申请受理了，仍可能没有端口

2008 年广州棠东一名企业用户向两家运营商申请 2M 宽带。同期报道记录：

- 运营商先受理申请；
- 包年费用已经被预扣；
- 几天后申请又被退回；
- 原因是当地 ADSL 接入口已满；
- 最终尝试从更远的交接箱牵线；
- 因铜线距离，先只能按 512K 报装，并被告知可能不稳定。

报道还直接描述运营商内部的 provisioning workflow：

`customer application`
→ `customer record`
→ `resource system matches line/port`
→ `resource exists → work order`
→ `installer executes`

这是一条极重要的 state-gap 证据，因为它证明：

- `payment state ≠ service state`；
- `application accepted by front desk ≠ resource allocated`；
- `city marketed as broadband-covered ≠ specific address serviceable at requested rate`；
- `nominal product speed ≠ physical copper-loop attainable speed`。

### Evidence

- B / 同时代：南方都市报转载，中关村在线，2008-07-08：<https://net.zol.com.cn/98/987730.html>
- B / 同时代同稿：C114，2008-07-09：<https://www.c114.com.cn/market/183/a328684.html>

注意：以上两个 URL 基本属于同一报道 family，不能算两个真正独立证据源。

---

## 7. 楼宇、端口与运营商准入：Internet 也有物理地址

### 7.1 北京郊区：端口耗尽可以持续多年

2008-12-29 京华时报记录，北京通州、昌平、朝阳部分偏远地区居民因网通端口不足无法安装固话/宽带；一名居民称自己居住五年仍未装上，营业厅长期回复“没有线路资源、端口都被占用，只能等待扩容”。扩容还牵涉机房、电杆和电缆建设。

所以“北京已有大规模宽带”与“北京每一个住宅都能安装宽带”完全不是同一个 claim。

### Evidence

- B / 同时代：京华时报/中新网，2008-12-29：<https://www.chinanews.com.cn/it/txxw/news/2008/12-29/1506181.shtml>

### 7.2 运营商覆盖差异会把搬家变成 access migration

2007 年一名北京 ADSL 用户在价格争议中称，自己想换其他宽带运营商，但其他运营商对其居住区域/电话线路不能提供相同服务。

2008 广州报道也记录楼宇独占/排他接入争议。

因此研究家庭宽带必须建立：

`person identity`
+ `postal address/building`
+ `telephone/physical line`
+ `operator footprint`
+ `live port inventory`

的组合，而不能把 broadband subscription 当成像 email 一样随人天然携带的账户。

### Evidence

- B / 同时代：市场报相关报道，2007-06-20：<https://news.sohu.com/20070620/n250686008.shtml>
- B / 同时代：南方都市报转载，2008-07-08：<https://net.zol.com.cn/98/987730.html>

---

## 8. 一条线路能给多少人用：家庭网络在旧 Web 时代也有 policy state

2008 年广东电信针对“一拖N”共享上网引发争议。同期报道记录，其合同/控制规则把同一家庭内少量电脑与更多机器共享甚至经营性转售区分开，并出现超过限定设备数后被断网提示的情况。

从考古角度，这提示后续不能只复原 modem/路由器教程，还应找：

- 服务协议历史版本；
- 对路由器/NAT/多终端的规则；
- 同时在线设备限制；
- 断网/告警页面；
- 家庭与出租屋/企业的套餐分类。

### Evidence

- B / 同时代：南方都市报，2008-01-08：<https://tech.sina.com.cn/t/2008-01-08/09231959797.shtml>

### Hard boundary

`一条宽带物理上可通过路由器共享`

不能直接推出：

`合同允许任意数量设备/住户共享`。

---

## 9. 2013：光纤覆盖查询把“这个地址能不能升级”重新做成 Web 对象

2013 年北京联通提速材料记录：

- 用户可以登录 `www.bbn.com.cn` 查询小区光纤覆盖；
- 光纤已覆盖时，可通过客户端申请光纤改造；
- 未覆盖时可以申请“光改团购”；
- 满足一定人数/比例并且资料准确、没有第三方限制时，运营商承诺在限定工作日内推进覆盖；
- 客户仍可通过网上营业厅和 10010 申请宽带安装。

这里产生一个新的旧 Web / client transaction：

`address/building query`
→ `coverage response`
→ `individual conversion request / group demand aggregation`
→ `physical project`
→ `in-home conversion`

它仍然不是“地图上显示覆盖 = 当场装好”。同期规则甚至明确列出线路不具备入户条件、第三方限制等例外。

### Evidence

- B / 同时代：北京联通提速说明，2013-07-03：<https://www.bbtnews.com.cn/2013/0703/73960.shtml>
- B / 同期活动材料：新浪“沃宽”专题，含 `bbn.com.cn`/客户端和覆盖查询说明：<https://client.sina.com.cn/zt/wokuan/>

---

## 10. Old-Web state model

### 10.1 拨号时代

```text
ISP/service advertised
→ user obtains dial number/account/card
→ local phone line available
→ modem configured
→ dial attempt
→ access server answers or busy/fails
→ authentication
→ online session starts
→ billed time accumulates
→ disconnect
→ phone line returns to ordinary voice use
```

档案里看到拨号号码与资费表，不能证明任何具体一次 session 成功。

### 10.2 ADSL 新装

```text
product page
→ address/line/application submitted
→ customer record created
→ resource/port lookup
→ port allocated
→ work order
→ installer/physical wiring
→ modem sync
→ account provisioned
→ authentication
→ billing activated
→ service usable
```

### 10.3 在线套餐/速率变更

```text
public portal
→ login
→ bind/resolve ADSL account
→ choose plan/speed
→ submit
→ backend accepts request
→ pending
→ billing-cycle boundary
→ new state effective
```

### 10.4 光纤改造

```text
address/building coverage query
→ coverage response
→ request
→ eligibility/third-party constraints
→ project/resource allocation
→ in-building/in-home wiring
→ ONT/line activation
→ account/billing migration
→ service active
```

这些 transaction 不应被一个“网上营业厅”标签压成同一状态。

---

## 11. Archive 保存偏差

### 11.1 Public-service-shell / private-provisioning-state asymmetry

最容易保存：

- 产品名称；
- 速率；
- 资费；
- 营销页；
- 帮助页；
- 登录框；
- “在线申请/自助变更”按钮；
- 覆盖查询入口；
- 客服号码。

最难保存、且很多本来就不应公开：

- 用户真实姓名/身份证；
- 电话号码；
- ADSL 用户名/密码；
- 住宅精确地址；
- 实时端口库存；
- 资源系统匹配结果；
- POST payload；
- session/cookie；
- 工单；
- 技术员记录；
- DSL sync/线路衰减参数；
- 账务 backend；
- 实际装通/退单/移机结果。

因此 archive 很可能保存“北京有 2M ADSL 页面”，却保存不了“某栋楼这一天下午有没有最后一个空闲端口”。

### 11.2 Successful-installation bias

运营商新闻和用户教程天然更容易留下：

`推出业务`
`提速`
`完成覆盖`
`在线申请`

而：

`端口满`
`无法入楼`
`申请后退单`
`铜线太远降速`
`安装失败`
`移机失败`

更依赖投诉、媒体调查或论坛负面经验。

所以旧网基础设施史必须主动保存 failure state，而不能只读运营商产品页。

### 11.3 Tariff/version mutability gap

资费页是高变动资源。同一个 URL 在不同 capture datetime 可能代表：

- 512K / 1M / 2M；
- 计时；
- 限时包月；
- 不限时；
- 促销期；
- 普通价；
- 老用户/新用户不同政策。

因此引用必须绑定 capture datetime，不能以今天转载的一个价格覆盖整个年份。

### 11.4 Portal/backend gap

即使 `www.bjtelecom.com.cn` 或 `www.bbn.com.cn` 的 public HTML 被完整保存，也不能推出：

- 登录服务被保存；
- 用户绑定流程仍工作；
- backend API/数据库被保存；
- 套餐变更会在回放环境里得到真实 acceptance；
- coverage query 还能访问当年的资源数据库。

### 11.5 Domain/organizational continuity gap

北京固网品牌/主体在 2000s 有重组；域名、品牌词和服务入口可能继续存在或迁移。

因此要单独建立：

- registrant/主体时间线；
- redirect 时间线；
- 页面 title/branding 时间线；
- 账号体系迁移；
- 是否同一 backend。

品牌连续 ≠ 技术系统连续。

### 11.6 Browser/client gap

本轮同期材料能证明部分服务后来需要门户注册、账号绑定，2013 又出现“沃宽”客户端。

但本轮**没有足够证据**确认 2004–2010 具体 self-service 页面是否依赖：

- IE-only；
- ActiveX；
- 特定 JS；
- Java；
- 特定 charset；
- 特定 cookie/security setting。

这些全部保持 unknown，不根据“那个年代运营商网站常用 IE”进行类推。

---

## 12. M1 archive status：本轮仍是明确负结果

本轮针对以下 locator 做了定向检索：

- `www.bjtelecom.com.cn`；
- `www.bbn.com.cn`；
- `www.169.com`；
- `www.bjtelecom.com.cn/cnc/general/ywsl/xieyibook/xieyibook11.jsp`。

也使用了带 `site:web.archive.org/web/...` 的搜索查询寻找 2001、2004、2006 前后可直接检查的 Wayback locator。

### 结果

**本轮没有实际打开并验证一份满足本仓 M1 门槛的 2001–2010 中文家庭宽带报装/自助办理 transaction capture。**

这不是：

> “Wayback 没有这些页面”。

只能写成：

> “本轮没有取得并检查可用 historical memento”。

因此以下项目继续为 unknown：

- historical DOM；
- HTTP charset / Content-Type；
- form action；
- GET/POST method；
- cookie/session；
- portal→ADSL account binding；
- captcha；
- coverage/address database response；
- live port response；
- service-change acknowledgement；
- billing backend handoff；
- actual work-order state；
- browser/plugin requirement。

candidate historical URL 不得升级成 verified capture。

---

## 13. Privacy / copyright

家庭宽带 provisioning 很容易碰到：

- 精确住宅地址；
- 固话号码；
- ADSL 账号；
- 工单编号；
- 身份证/机主信息；
- 旧 forum/投诉中的普通人联系方式。

本仓只保留证明技术结构所需的最低信息：

- 城市/区域；
- 抽象 URL pattern；
- 产品/运营商；
- transaction state。

不因历史页面仍可访问就重新公开普通用户的账号、电话或精确住址。

---

## 14. 与 `how-people-lived` 的交叉结论

这份 old-Web note 改变的并不是“ADSL 网页长什么样”，而是旧网研究的用户模型。

研究 2001–2010 中文互联网时，用户不应被抽象成：

`browser → website`

更现实的链条是：

`household/building`
→ `telephone/copper/fiber infrastructure`
→ `operator footprint`
→ `port/resource state`
→ `subscription/account`
→ `billing/time policy`
→ `modem/router/client`
→ `browser`
→ `website`

所以：

> **一个历史网页“存在于 Internet 上”，与一个具体普通家庭“在这个晚上能够低成本、稳定、持续地打开它”，之间仍隔着一整套住宅接入基础设施。**

这一点应成为以后所有中文旧 Web 大众化叙事的默认校验。

---

## 15. 下一步

1. 对 `www.bbn.com.cn`、`www.bjtelecom.com.cn` 做 host genealogy，不默认品牌/主体连续；
2. 继续寻找 2004–2007 的 public product/help/registration capture；
3. 优先找 2007 `xieyibook11.jsp` 的 historical memento 和相邻静态资源；
4. 若找到 capture，记录 charset、form、JS、session 边界，但不尝试重放真实用户账号；
5. 搜索 163/169 同期 ISP 接入手册、Windows 95/98 拨号配置页；
6. 找一份带“端口查询/覆盖查询”的历史 capture，把 public lookup 与 live resource database 分开；
7. 建立失败状态样本：端口满、铜线过长、不能移机、楼宇排他、装机取消；
8. 以后做浏览环境实验时，把运营商 self-service 页面纳入候选，但只有拿到可靠 capture 后才进入 M3。

---

## AI-assisted research note

初稿由 AI 辅助检索与整理。本文没有把 today-live host 当 historical capture，没有用运营商产品宣传替代具体地址的可装性，也没有尝试登录、枚举或重新公开普通用户的历史宽带账号。