# Remote work / SOHO / mobile office state gaps, 2000–2015

> Scope: 中文 Web 约 2000–2015。这里不写全球远程劳动史，也不把 2020 年后的居家办公倒灌回早期 Web；只研究旧中文 Web 怎样呈现、支持或遮蔽“工作地点与单位地点解绑”的状态。

Companion life-history note: [`tmzncty/how-people-lived/topics/workplace-location-decoupling-telecommuting-remote-work-and-work-boundaries-china-2000-2026.zh-CN.md`](https://github.com/tmzncty/how-people-lived/blob/main/topics/workplace-location-decoupling-telecommuting-remote-work-and-work-boundaries-china-2000-2026.zh-CN.md)

## 1. 为什么这是旧网考古对象

早期中文 Web 里的“SOHO”“网上办公”“移动办公”“电子通勤”很容易被今天压成一个词：remote work。

实际至少有四种不同对象：

1. **自由职业 / SOHO**：没有固定雇主办公室，可能用 email / 论坛 / 网站找客户；
2. **雇员居家办公**：劳动关系不变，雇主临时或长期允许在家工作；
3. **mobile office / 企业移动办公**：员工在家、出差、分公司等地点远程进入企业网、邮件、OA 或 VPN；
4. **共享/临时办公地点**：工作数字化以后，工位、会议室、打印、网络重新作为服务购买。

旧网页上出现“移动办公解决方案”，只能证明一个产品/承诺存在；不能直接证明普通员工真的得到账号、在家登录成功、完成工作，更不能证明企业已经实行 remote-work policy。

因此必须固定：

```text
remote-work marketing exists
≠ employer permits remote work
≠ employee is provisioned
≠ remote authentication succeeds
≠ internal applications are usable
≠ work is actually submitted
≠ coworkers receive/integrate it
≠ employment/pay/performance remain continuous
```

---

## 2. 一个最小状态机

### 2.1 企业雇员远程办公

```text
job / task is remotely executable
→ employer policy permits remote location
→ employee selected / assigned remote state
→ home/remote device available
→ access network available
→ account/credential provisioned
→ dial-up / broadband / VPN session established
→ required client/browser/plugin configured
→ enterprise mail / directory / intranet / OA reachable
→ required file/data reachable
→ task received
→ work produced
→ upload/send/save succeeds
→ colleague/manager encounters current version
→ output accepted into workflow
→ payroll / attendance / performance state continues
```

这些箭头都不能用一个“登录成功”代替。

### 2.2 自由职业 / SOHO

```text
public profile / forum post / listing visible
→ potential client encounters it
→ contact established
→ scope/price agreed
→ file/task delivered
→ client accepts
→ payment obligation created
→ payment actually received
→ next project / reputation / repeat-client state
```

`在家有电脑` 与 `有持续可结算的工作` 之间仍有一整条市场和信任链。

### 2.3 共享办公

```text
workspace listing exists
→ desk/room availability at requested time
→ booking submitted
→ payment recognized
→ access credential / QR / front desk admits user
→ desk/network/electricity actually usable
→ meeting/printing/private-call needs available
→ work session completed
```

一个 2015 年共享空间官网的“自由工位”栏目，不能反推当天一定有工位，更不能证明使用者属于 remote employee。

---

## 3. 2000：SOHO 的公开 Web/媒体语义已经分叉

2000 年《生活时报》一篇同期文章已经明确区分两类居家工作：一类是自由撰稿、律师、设计等自主安排结果交付的人；另一类是会计、技术等在公司允许下居家办公的人，公司为其配联网、专用电话、传真，并继续通过专用电话或网络查询工作状态。

Historical locator / live legacy page:

- original URL currently served by 光明网旧报刊库：
  `https://www.gmw.cn/01shsb/2000-10/25/GB/10%5E1507%5E0%5ESH5-2509.htm`
- publication date stated on page: `2000-10-25`
- evidence: **B / 同期报刊文本的现代在线呈现**

它能证明 2000 年公开话语已经知道“SOHO 自由职业”与“雇主监控的居家办公”不是一回事。

它不能证明：

- 文中所述模式当时的全国采用率；
- 原始 2000 HTTP headers / charset；
- 当前页面 DOM 与 2000 年在线版本是否相同；
- 所述公司的真实远程系统是否被 archive 保存。

---

## 4. 2003 神州数码：非常罕见的“远程工作 transaction narrative”

2003 年 6 月新浪科技保留了一篇同期报道，提供了比一般“移动办公”营销词更细的员工操作链。

Historical original URL / current legacy rendering:

- `https://tech.sina.com.cn/it/m/2003-06-09/1846196226.shtml`
- page-stated publication datetime: `2003-06-09 18:46`
- title: `综述：神州数码“激活”移动商务`
- evidence: **B / 同期媒体；包含员工和企业 IT 人员直接引语**

报道中的员工周永先在 SARS 期间第一次在家办公：

1. 使用公司统一办理的联通 165 账号拨号；
2. 上网后打不开公司网上办公系统 `NOOTS`；
3. 打内部 `7888` IT 服务电话；
4. 按指导下载工具软件；
5. 进入系统通讯录、向媒体发稿；
6. 用电话确认部分记者是否收到；
7. 领导继续通过系统分配新工作。

同篇把企业移动办公描述成三个层次：

- 公司内部动态工位、随员工登录迁移的分机号码；
- 拨号进入企业网、收邮件、访问内部网站；
- VPN 连接全国分支。

它还记录远程办公突然扩大后，IT 帮助台先被大量配置问题冲击，一周后咨询才下降。

### 这条证据真正支持什么

它支持：

```text
public Internet connectivity
≠ enterprise application readiness
```

以及：

```text
account exists
→ dial succeeds
→ enterprise app initially fails
→ support encounter
→ tool installed
→ app succeeds
```

这是一条极其有价值的 **negative-to-recovered state transition**。

### 不能从它推出什么

- `NOOTS` 的准确软件厂商/版本目前未核验；
- 不能从名称猜测协议；
- 不能假定浏览器是 IE6、插件是 ActiveX；
- 不能把“VPN”三个字自动解释成某一种标准或客户端；
- 不能把该 IT 企业的一次应急经验外推成 2003 中国企业普遍状态；
- 报道明确说特殊时期后仍会恢复固定办公，因此不能写成“2003 已经形成常态 WFH”。

---

## 5. Remote access 的页面状态与企业内部状态不能混淆

早期“网上办公 / OA / VPN / 移动办公”通常存在强烈的 **public-product-shell / private-work-state asymmetry**：

档案容易保存：

- 产品首页；
- 功能列表；
- “随时随地办公”的广告语；
- 下载入口；
- 帮助文章；
- 同期媒体评测。

档案不容易、也通常不应该保存：

- 企业真实 VPN 地址；
- 员工用户名、密码、证书；
- 内部通讯录；
- 内部邮件；
- 私有 OA 表单；
- 文档版本；
- 审批记录；
- 考勤；
- 工资、绩效；
- 客户数据。

因此 archived public page 最多能证明“企业/厂商公开提供或宣称某种能力”，而不证明某名普通员工执行到了哪个私有状态。

---

## 6. 早期 Web 的 browser/client dependency 尤其危险

远程工作系统比普通信息页面更容易依赖：

- 特定 Windows 版本；
- IE / 浏览器嗅探；
- ActiveX / Java applet；
- VPN 客户端；
- 证书和本地密钥；
- 私有加密组件；
- Office 文档控件；
- 本地拨号配置；
- 内网 DNS；
- pop/imap/smtp 或 Webmail 的企业配置；
- 防火墙/NAT/代理规则。

所以即使 Wayback 保存了登录页，也不意味着今天能回放 historical task。

必须拆开：

```text
login HTML survives
≠ historical client survives
≠ authentication backend survives
≠ VPN tunnel can be recreated
≠ internal resource was archived
```

现代 Chromium 能展示 2003 年登录壳，也完全不能证明 2003 年真实员工在当时 OS/拨号/VPN 组合下看见同样的交互。

---

## 7. 2008：旧网同时支撑“接活”和“重新找物理办公室”

2008 年《新闻晨报》经新浪保存了上海 SOHO 工作者合租办公室的同期材料：

- 一名自由撰稿人原先在家办公，孩子出生后家庭干扰增大，通过网上“找人合租办公室”帖子找到其他 SOHO 工作者；
- 合租空间提供电话、传真、宽带、打印机和桌椅；
- 一名设计者每天通过 email 承接、交付业务；
- 一名软件开发者通过网络论坛发“求合租”帖子，寻找共同办公者。

Historical locator / current legacy page:

- `https://news.sina.com.cn/c/2008-01-30/023014856800.shtml`
- page-stated publication datetime: `2008-01-30 02:30`
- evidence: **B / 同期媒体**

这条材料揭示旧网的一个重要双重作用：

```text
Internet makes client/work addressable at distance
AND
Internet makes missing physical workspace addressable
```

所以“数字化”并没有简单消灭办公室。恰恰相反，当工作从雇主办公室拆出来以后，Web 又被用来寻找新的共用物理空间。

### Archive caution

报道里提到“论坛发帖”与“网上找合租”，但本轮没有定位到对应原帖，因此：

- 不能确定论坛平台；
- 不能确定原帖 datetime；
- 不能重建回复数；
- 不能验证“十多名应征者”的平台 transaction；
- 媒体转述只能证明受访者/记者当时如此陈述。

---

## 8. 2008 毕业生：`SOHO label ≠ remote-work state`

中新网 2008 年转载《信息时报》的“隐性就业”报道，把多种状态放在同一个 SOHO 标签下：

- 文案策划；
- 网络商铺；
- 自由撰稿；
- 家教；
- 兼职导游；
- 培训机构兼职教师；
- 格子铺。

URL:

- `https://www.chinanews.com.cn/edu/qzjy/news/2008/12-18/1493597.shtml`
- evidence: **B / 同期媒体**

其中不少工作甚至不在家完成。因此旧网考古不能仅凭标题里的 `SOHO` 把个案编码成：

`home-based = true` 或 `remote employment = true`。

至少需要分别记录：

- employment relation；
- work location；
- client acquisition channel；
- delivery channel；
- payment channel；
- contract status。

这是一个 **label/state gap**。

---

## 9. 2009 H1N1：“电子通勤”是雇佣关系内的地点切换

新华社 2009 年报道一名上海杂志编辑在 H1N1 期间申请居家工作；她仍按上司安排完成任务，并通过 email 与上司、同事沟通。报道明确把 `Telecommuter / 电子通勤族` 与 SOHO 区分：前者仍受雇主约束、有工作时间，只是依靠电话、传真、网络等完成远程通勤。

Historical URL currently served by Sohu:

- `https://news.sohu.com/20091204/n268682236.shtml`
- page-stated publication datetime: `2009-12-04 14:36`
- source attribution: 新华网
- evidence: **B / 同期媒体**

这给旧网状态模型增加：

```text
same employee + same employer
physical-office state → temporary-remote state → ?
```

但报道没有提供疫情后该员工是否持续远程，因此最后一个状态必须保持 unknown。

---

## 10. 2010–2015：协同办公产品存在不等于 remote-work norm

随着 OA、企业 Webmail、VPN、即时通信和移动终端增长，越来越多“协同办公”功能可以从 Web 或客户端调用。

但研究必须坚持：

```text
OA product exists
≠ organization purchased it
≠ organization enabled external access
≠ every employee received credentials
≠ employee was allowed to work remotely
≠ employee's job became location-independent
```

尤其不能从今天仍存在的 OA 厂商官网，把当前版本的云、移动端、微信/钉钉集成等特性倒写到 2005 年。

当前现代页面只能作为产品谱系 locator；若要确认历史版本，必须寻找对应年份手册、安装包、帮助页、新闻稿或 archive capture。

---

## 11. 关键 state gaps

### 11.1 policy / capability gap

`技术上可远程 ≠ 雇主允许远程`。

### 11.2 provisioning gap

`员工属于公司 ≠ 已获得远程账号、VPN、证书和设备`。

### 11.3 public-network / enterprise-network gap

`能上 Internet ≠ 能进企业网`。

2003 神州数码员工第一次上网后仍打不开内部系统，是直接证据。

### 11.4 authentication / application gap

`VPN connected ≠ every required OA/mail/file service works`。

### 11.5 send / encounter gap

`email sent ≠ recipient actually received/read`。

2003 员工还需要电话确认记者是否收到邮件。

### 11.6 upload / workflow gap

`file uploaded ≠ manager is looking at current version ≠ output accepted`。

### 11.7 remote-presence / labor gap

`账号在线 ≠ 正在劳动`；反过来 `不在线 ≠ 没有通过电话/离线文件工作`。

### 11.8 temporary / normalized gap

`SARS/H1N1 emergency remote ≠ permanent remote policy`。

### 11.9 SOHO-label / employment-state gap

媒体使用 `SOHO` 可能同时指自由职业、居家雇员、小企业主、兼职甚至只是不坐班。

### 11.10 digital-work / physical-workspace gap

`业务可在线接收交付 ≠ 住宅是合格办公室`。

2008 合租办公室材料正好证明缺口存在。

---

## 12. 保存偏差：企业远程办公比普通公开 Web 更“黑”

这一题有很强的结构性不可见性：

### 容易幸存

- SOHO lifestyle 报道；
- 厂商 OA/VPN 功能页；
- 产品广告；
- 企业危机应对新闻；
- 公共登录壳；
- 下载说明。

### 容易消失 / 不应公开

- 企业 intranet；
- VPN endpoint；
- 员工账号；
- 私有 IM / mail；
- 内部文件；
- 审批与绩效；
- helpdesk ticket；
- 客户数据。

这会制造 **marketing-survival bias / 营销幸存偏差**：后人可能看见很多“随时随地办公”口号，却看不见当天到底有多少人因客户端、带宽、权限、家庭设备或雇主政策失败。

2003 神州数码报道异常有价值，正是因为它保存了一个失败状态：员工已有系统和账号，却仍因本地配置无法使用，必须调用 helpdesk。

---

## 13. Browser / protocol assumptions to record in future captures

未来若取得 M1 级 historical capture，至少记录：

- original URL / host；
- capture datetime；
- Content-Type / charset；
- login form method / action；
- JavaScript / frames / ActiveX / Java dependency；
- cookie/session mechanism；
- client download links；
- browser/OS requirements；
- VPN or dial-up prerequisite if documented；
- public Internet URL vs internal-only hostname；
- attachment/document control dependencies；
- archive rewrite effects。

不要通过尝试真实旧员工凭据验证私有系统。

---

## 14. Historical locators for a future M1 check

### Locator A — Sina 2003 mobile office narrative

- original/live legacy URL: `https://tech.sina.com.cn/it/m/2003-06-09/1846196226.shtml`
- stated datetime: `2003-06-09 18:46`
- value: exact remote-work narrative + system component names
- current status: live page inspected; **no Wayback/WARC capture verified in this research loop**

### Locator B — Sina 2008 SOHO shared office

- original/live legacy URL: `https://news.sina.com.cn/c/2008-01-30/023014856800.shtml`
- stated datetime: `2008-01-30 02:30`
- value: email-based work + forum-mediated workspace search + physical office stack
- current status: live page inspected; **no archive memento verified in this loop**

### Locator C — Sohu/Xinhua 2009 telecommuter

- original/live legacy URL: `https://news.sohu.com/20091204/n268682236.shtml`
- stated datetime: `2009-12-04 14:36`
- value: explicit distinction telecommuter vs SOHO, temporary employer-approved WFH
- current status: live page/search result inspected; **no archive memento verified in this loop**

These are locators, not M1 cases.

---

## 15. Cross-country comparator kept out of repository scope

Global prehistory remains in `how-people-lived`, not here.

Useful comparator facts there include:

- Southern California 1995 employer/commuter survey found telecommuting at 15% of firms with 20+ employees and identified job fit/equipment as obstacles;
- 1998 U.S. household survey found Internet was used by only a minority of telecommuters, so telecommuting should not be treated as synonymous with Web work;
- U.S. GAO in 2001 defined telecommuting as working from remote rather than employer-provided locations and emphasized management/security/suitability barriers.

This note references them only to prevent presentism; it does **not** expand `old-web-archaeology` into a global telework repository.

---

## 16. Evidence grades

| Evidence | Grade | Claim supported | Boundary |
|---|---|---|---|
| 2000《生活时报》SOHO text | B | public distinction between freelance and employer-monitored home work | current online rendering not verified as original historical DOM |
| 2003 Sina mobile-office article | B | concrete employee workflow and company-described remote stack | media narrative; private systems not captured |
| 2008 Sina/新闻晨报 SOHO shared office | B | email delivery + Web/forum workspace discovery + physical workspace needs | original forum transactions absent |
| 2008 Chinanews/信息时报 graduate SOHO | B | `SOHO` label covered multiple employment/location states | not platform transaction evidence |
| 2009 Sohu/Xinhua telecommuter | B | employer-approved temporary remote work and explicit SOHO distinction | post-epidemic state unknown |
| State models in this file | D | research reconstruction of boundaries | never historical original |

---

## 17. Privacy and stop conditions

Do not:

- search for leaked enterprise VPN credentials;
- attempt login to old corporate systems;
- reconstruct a named ordinary employee's private mailbox/files;
- publish employee phone numbers, email addresses or internal hostnames unless indispensable and already institutional/public;
- treat an exposed intranet dump as acceptable historical evidence without privacy review;
- run unknown historical ActiveX/VPN clients on a trusted host merely to “see if they work”。

If private state is inaccessible, record it as inaccessible.

---

## 18. What is established / inferred / unknown

### Established

- Chinese public media by 2000 discussed both freelance SOHO and employer-permitted home work.
- A 2003 contemporaneous case records dial-up, enterprise-network access, a failed first attempt, helpdesk recovery, internal directory/mail and VPN as parts of a real emergency mobile-office system.
- 2008 material records email-mediated client work plus Web/forum-mediated search for shared physical offices.
- 2009 material records a telecommuting employee remaining under employer scheduling and output requirements during H1N1.

### Reasonable inference (D)

- Early remote-work experience depended on a larger private stack than surviving public pages reveal.
- Archive samples will systematically overrepresent products/marketing and underrepresent actual enterprise transaction states.
- `SOHO` should be indexed as a historical label, not used as a normalized employment-state value without additional evidence.

### Unknown

- original historical DOM/HTTP charset for the listed 2000/2003/2008/2009 pages unless an archive capture is later verified;
- exact NOOTS product/version/protocol;
- precise browser/OS/client requirements of the 2003 enterprise system;
- historical VPN implementation;
- helpdesk ticket content/count beyond the published narrative;
- any private employee mailbox/file/approval state;
- whether named emergency remote employees remained remote afterward;
- 2000–2015 representative adoption rates by Chinese industry.

---

## 19. Why this changes old-Web interpretation

A historical page saying “随时随地办公” is not evidence that work had become placeless.

The archaeologically useful question is instead:

> **Which parts of the office had actually crossed the network boundary, which still required a corporate building or private backend, and what hidden authentication, client, support and workflow states stood between a public Web promise and an ordinary employee completing a day of work elsewhere?**

AI-assisted research note. Preserve the A/B/C/D labels and recheck historical mementos before promoting any locator to a complete case.