# 劳动力市场“信息网”不一定是 Web：后台联网、公共接口与普通求职者终端的语义断层，1998–2002

> 状态：**research / architecture-and-terminology probe；未达到 M1 完整案例门槛。**
>
> 本文件不是重复 [`CHINA_LABOUR_MARKET_NETWORK_ARTIFACT_PROBE_2002_2006.md`](CHINA_LABOUR_MARKET_NETWORK_ARTIFACT_PROBE_2002_2006.md)。后者研究的是 `www.lm.gov.cn` 这个明确公共 Web host 的历史 artifact 线索；本文件向前追一层，问：
>
> **1998–2002 年行政文件里的“劳动力市场信息网”“实时联网”“计算机网络”到底能证明什么？它们什么时候只是就业服务机构内部 / 城市间的数据网络，什么时候才有证据说普通求职者面对的是 WWW 页面？**

---

# 1. 为什么必须单独做这个语义审计

旧网研究非常容易出现一个时代错读：

```text
历史文件写“信息网 / 联网 / 计算机网络”
=> 研究者自动脑补成“网站 / Internet / 浏览器”
```

对 1990s 末中国公共就业服务，这个推断尤其危险。

当时可能同时存在：

- 职介机构内部数据库；
- 同一城市不同就业服务机构之间的局域 / 广域网络；
- 城市向省级中心报送数据的计算机网络；
- 工作人员使用的业务终端；
- 求职者在现场看到的 LED / 电视屏幕；
- 电话热线；
- 报纸、广播、有线电视；
- 国际互联网；
- 后来的公共 Web 网站。

它们可以共享同一批岗位数据，却不是同一个 interface，也不要求同一种用户设备。

因此本文件固定一个旧网考古最低规则：

## **`information network != World Wide Web unless evidence says so`**

---

# 2. 研究单位必须拆开

按照 `docs/METHOD.md`，本轮至少区分六个对象：

```yaml
research_units:
  administrative_program:
    example: 劳动力市场“三化”建设 / 信息网建设
  backend_network:
    example: 城市就业服务机构之间的计算机网络
  provincial_monitoring_network:
    example: 省级监测中心与城市网的数据联接
  public_service_endpoint:
    example: 职介窗口 / 公共终端 / LED / 热线
  public_web_site:
    example: www.lm.gov.cn
  archived_web_capture:
    example: 某 URL 在某 datetime 的 Wayback / WARC artifact
```

这些状态之间不能直接传递：

```text
backend_network exists
!=
public Web site exists
!=
job seeker can access Web site
!=
job seeker personally operates a browser
!=
application is completed online
!=
job is obtained
```

---

# 3. 1998：同期中央文件要求“现代化信息网络”，但列出的普通人接口首先包括电视、广播和职业介绍窗口

1998 年 6 月 9 日，中共中央、国务院《关于切实做好国有企业下岗职工基本生活保障和再就业工作的通知》提出加强劳动力市场建设。

文件写到：

- 各地区、特别是大中城市，应充分利用电视、广播等现代化信息网络；
- 提供求职、招聘、职业指导等信息和咨询；
- 公共职业介绍机构应开设专门服务窗口；
- 街道就业服务也应加强。

来源：

- 《人民日报》1998-06-23 第 1 版保存的同期正式通知：
  https://cn.govopendata.com/renminribao/1998/06/23/1/

Evidence grade: **A（同期正式制度文本；当前通过第三方人民日报历史库访问）**。

这里已经能看到一个重要历史语义：

> **“现代化信息网络”在 1998 的公共就业语境中并不天然意味着浏览器里的 Web。**

电视、广播、窗口、街道服务本身都可以是劳动力市场信息分发系统的一部分。

不能把今天“信息网 = 网站”的直觉倒投回去。

---

# 4. 1998：劳动力市场信息网建设明确是一项“就业服务机构 + 计算机网络”工程

劳动保障系统后来保存的工作回顾称：

- 就业服务信息化在 1980s 末已经从职业介绍、待业保险工作的计算机应用起步；
- 1998 年以后，根据《劳动力市场信息网建设实施纲要》，开始以城市为中心建设劳动力市场信息网络；
- 全国 100 多个地级以上城市依托就业服务与失业保险工作建设计算机网络；
- 各省、自治区、直辖市陆续建设劳动力市场信息网监测中心。

来源：

- 青岛市人力资源和社会保障局保存的劳动保障部培训就业司 2009 年工作回顾：
  https://hrss.qingdao.gov.cn/zxzx_47/gzdt_47/202206/t20220613_6127566.shtml

Evidence grade: **C/B（后来官方工作回顾；可用于沿革，不是 1998 原始网络技术文档）**。

另外，1998 年 9 月 27–28 日举行过“劳动力市场信息网建设座谈会”，参会者包括 11 个省 / 直辖市和 8 个重点城市劳动就业服务机构的信息网负责人。

现可定位文本：

- 《劳动部关于印发〈劳动力市场信息网建设座谈会纪要〉的通知》，1998-10-09，第三方法规库：
  https://www.055110.com/law/1/30867.html

Evidence grade: **B / locator-quality legal text**。

它们能证明“信息网”作为行政 / 技术工程确实存在；仍不能仅凭词名确定：

- TCP/IP / X.25 / 专线 / 拨号等传输协议；
- 是否与公网 Internet 互联；
- 客户端 OS；
- 软件产品；
- browser 是否参与；
- charset；
- 求职者是否能直接进入系统。

以上当前全部保持 **UNKNOWN**。

---

# 5. 2000：正式文件直接把省级中心定义成“非实时计算机网络系统”的管理中心

2000 年 4 月 13 日，劳动和社会保障部培训就业司发布《关于加强省级劳动力市场信息网监测中心建设的通知》（劳社培就司发〔2000〕8号）。

现存法规文本写明：

> 省级监测中心是联接全省各城市网的**非实时计算机网络系统**的管理中心。

来源：

- 第三方法规库保存的正式文号文本：
  https://www.110.com/fagui/law_154522.html

Evidence grade: **A/B（正式部门文件的第三方保存文本；发布机关、日期、文号明确）**。

这是本轮最重要的技术语义证据。

它说明：

```text
“中国劳动力市场信息网××省监测中心”
```

这个名称里的“网”，至少在这里首先描述的是：

- 省级管理中心；
- 各城市网；
- 数据汇总 / 监测；
- 非实时的计算机联接关系。

因此：

## `named network != public website`

甚至：

## `networked computer service != real-time network`

更不能再跳到：

## `real-time network != Web`

---

# 6. 2001–2002：“市区内实时联网”的统计，也仍然是就业服务系统指标

2001 年劳动和社会保障事业统计公报称：

- 全国建立 17 个省级监测中心；
- 100 个劳动力市场“三化”试点城市中，64 个实现市区内实时联网；
- 就业服务已发展为职业介绍、培训、指导、劳动保险事务代理等“一条龙”服务。

来源：

- 劳动和社会保障部 / 国家统计局，《2001年度劳动和社会保障事业发展统计公报》：
  https://www.stats.gov.cn/sj/tjgb/qttjgb/qgqttjgb/202302/t20230218_1913248.html

2002 年统计公报又称：

- 90 个城市实现市区内实时联网；
- 全国各类职业介绍机构 26,158 所；
- 劳动保障部门办职业介绍机构 18,010 所。

来源：

- 《2002年度劳动和社会保障事业发展统计公报》：
  https://www.stats.gov.cn/sj/tjgb/qttjgb/qgqttjgb/202302/t20230218_1913251.html

Evidence grade: **A（官方年度统计公报）**。

这些数据应解释为：

> 城市公共就业服务的业务 / 信息系统联网程度正在提高。

它们**不能**被改写成：

> “2001 年 64 个城市的求职者已经可以实时在互联网上浏览全部岗位。”

当前没有证据支持后一句。

---

# 7. 舟山 1998–2000：最有价值的是同一批就业信息同时穿过六七种不同接口

《舟山市志（1989—2005）》的劳动力市场条目记录：

- 1997 年开始筹建劳动力市场；
- 1998 年职业介绍、失业保险部门开始窗口式服务；
- 《舟山晚报》和有线电视台推出免费“再就业热线”；
- 1999 年市级劳动力市场正式开业；
- 就业供求信息发布扩展到报纸、广播、电视、电信、国际互联网等媒介；
- 场内使用 LED 电子大屏幕与电视同步显示；
- 2000 年全市职业介绍信息资源共享，职业介绍服务实现计算机管理。

来源：

- 浙江地方志公开 HTML 转换，第 380 页：
  https://dfz.zj.gov.cn/zlyz/ossfs/h5/ZS-Z-330900-2005-001-0303/files/basic-html/page380.html

Evidence grade: **C/B（后来地方志整理；不是 1998–2000 原始站点 artifact）**。

这一段特别适合 old-Web archaeology，因为它防止一个常见错误：

```text
internet channel exists
=> all other channels become obsolete
```

真实状态可能是：

```text
one job database / one employment-service organization
-> staff window
-> newspaper
-> radio
-> cable TV
-> telephone hotline
-> LED / TV in hall
-> Internet
```

因此，**“Web 到来”并没有把旧接口一次性替掉，而是给同一服务栈增加了一个出口。**

---

# 8. 这和已有 `www.lm.gov.cn` artifact probe 怎样衔接

仓库已有：

- [`docs/CHINA_LABOUR_MARKET_NETWORK_ARTIFACT_PROBE_2002_2006.md`](CHINA_LABOUR_MARKET_NETWORK_ARTIFACT_PROBE_2002_2006.md)

该 probe 已经确认：

- 2004 年同期报道把 `www.lm.gov.cn` 列为劳动保障部公共服务网络平台；
- 2006 年教育部正式网页把“中国劳动力市场网 `www.lm.gov.cn`”作为全国网上联合招聘平台；
- 一份 2011 年澳大利亚储备银行研究保留了 `lm.gov.cn` 的 2002 精确 original URL locator；
- 但尚未取得满足 METHOD 的 verified historical capture。

这两个文件应按以下顺序阅读：

```text
1998–2002：employment-service computerization / backend information network
                     ↓
          public dissemination through multiple endpoints
                     ↓
2002–2006：明确可定位的 public WWW host / www.lm.gov.cn
```

这个箭头表示**研究问题的层级关系**，不是已经证明的单一系统技术迁移链。

当前仍不知道：

- 早期城市 / 省级业务网络是否、何时与 `lm.gov.cn` 共用数据库；
- 数据上传是自动、批处理还是人工；
- 哪些城市最早将本地职位同步到 Internet；
- 后台 client 与 Web publishing stack 是否由同一供应商 / 系统承担。

---

# 9. 新增的 old-Web 证据规则：数字化的“终端位置”必须单独记录

建议以后凡遇到公共服务“信息化”对象，都增加一个字段：

```yaml
digitization_locus:
  data_entry_by: UNKNOWN | clerk | employer | user
  database_location: UNKNOWN | office LAN | city WAN | provincial center | public Internet
  user_endpoint: UNKNOWN | staffed counter | public terminal | telephone | TV/LED | web browser
  user_owns_terminal: UNKNOWN | yes | no | not_required
  direct_user_query: UNKNOWN | yes | no
  direct_user_submission: UNKNOWN | yes | no
```

为什么要这么做？

因为下面四种体验在普通人生活里完全不同：

### A. 柜台代理

```text
求职者说需求
-> 职介员操作电脑
-> 电脑返回岗位
-> 职介员口头 / 纸面告诉求职者
```

### B. 公共终端

```text
求职者到劳动市场
-> 自己操作现场终端
-> 查询数据库
```

### C. 家庭 / 单位 Web

```text
求职者自己有电脑 + Internet
-> 浏览网站
-> 查询 / 投递
```

### D. 多媒介广播

```text
后台职位数据
-> 报纸 / 电视 / LED / 热线发布
-> 求职者再线下联系
```

“后台已经电子化”只证明这些路线中的前半段可能改变，并不能告诉我们 ordinary user 的最后一公里是哪一种。

---

# 10. 一个新的保存偏差：public-Web hindsight / 公共 Web 后见偏差

二十多年后，研究者最容易重新找到的是：

- 后来的政府网站；
- `www.lm.gov.cn` 这样的域名；
- 在线招聘活动公告；
- 门户转载；
- 被论文引用的 URL。

反而最难重新看到的是：

- 1999 年职介员电脑里实际跑的客户端；
- 城市局域 / 广域网的具体协议；
- 柜台工作流；
- 打印出的岗位单；
- LED 大屏当日显示内容；
- 一次街道工作人员帮下岗职工查岗位的操作过程。

于是 archive 很容易把历史压成：

```text
“以前没有网上找工作”
->
“后来出现就业网站”
```

而真实过程可能更像：

```text
manual employment office
-> office computerization
-> inter-office data network
-> screen / hotline / newspaper / TV outputs
-> public terminals
-> public Web site
-> direct online application
```

这里新增一个 archive-bias 标签：

## `public-Web hindsight bias`

> **因为公共网页比内部客户端、柜台流程和短命业务系统更容易留下可搜索 URL，后来研究者会系统性高估“Web 页”在数字化过程中的起点位置。**

---

# 11. 第二个保存偏差：backend invisibility / 后台不可见偏差

旧网研究通常以 URL 为索引单位。

但大量真正改变普通人生活的早期数字系统可能根本没有 public URL：

- 社保经办终端；
- 职介数据库；
- 银行柜台系统；
- 票务专网；
- 单位内部局域网；
- 电话坐席后端。

它们可能比 public Web 更早决定：

- 查询速度；
- 跨区信息能否共享；
- 柜台能否看到另一区岗位；
- 一份记录要不要重新录入；
- 一个普通人要跑几个地点。

所以：

## `no public URL != no digital infrastructure`

这条规则对中文旧网尤其重要，因为 1990s–2000s 大量社会数字化并不是从浏览器开始。

---

# 12. 本轮 artifact 状态

本轮没有把行政 / 地方志文本冒充成历史网站 capture。

当前只确认：

```yaml
1998_information_network_program:
  exists: true
  evidence: policy / later official retrospective
  exact_technical_stack: UNKNOWN

2000_provincial_monitoring_network:
  exists: true
  topology_claim: connects city networks; described as non-real-time computer network system
  protocol: UNKNOWN
  client_software: UNKNOWN
  public_web_interface: UNKNOWN

2001_city_realtime_networking:
  official_count: 64 of 100 pilot cities
  direct_public_browser_access: UNKNOWN

2002_city_realtime_networking:
  official_count: 90 cities
  direct_public_browser_access: UNKNOWN

public_www_lm_gov_cn:
  handled_in: docs/CHINA_LABOUR_MARKET_NETWORK_ARTIFACT_PROBE_2002_2006.md
  verified_historical_capture: not achieved in that probe
```

本轮也**没有取得**一份 1998–2002 劳动力市场后台系统的：

- 原始安装手册；
- 历史客户端截图；
- 软件介质；
- 抓包；
- 可核验 WARC / Web capture；
- 浏览器要求；
- charset / DOM / script 证据。

所以：

## **M1 status: NOT ACHIEVED**

更严格地说，本对象目前首先是 **non-Web / pre-public-Web digital infrastructure research note**，并不适合作为 M1 的“历史 Web 页面”完整案例。

---

# 13. 当前不能写的东西

不得写：

> “1998 年中国劳动力市场网已经是一个全国网站。”

证据不足。

不得写：

> “2000 年下岗职工可以直接在线实时查全国岗位。”

证据不足。

不得写：

> “市区实时联网”就是 Internet 实时联网。

术语不等价。

不得根据 `/gb/` 路径、`.htm` 扩展名或后来网站猜：

- GB2312 / GBK；
- ASP / JSP；
- IIS；
- IE-only；
- frameset；
- ActiveX。

这些在没有 artifact 前全部是 **UNKNOWN**。

不得把地方志 1999 年提到“国际互联网”改写成：

> “Internet 已经是当地主要就业渠道。”

地方志只证明它进入发布媒介组合。

---

# 14. 和普通生活史的交叉解释

本轮与 `tmzncty/how-people-lived` 的交叉研究新增一个非常具体的普通生活状态：

## `institution-mediated digitization / 机构中介数字化`

一个 1998–2002 年的求职者完全可能经历：

```text
本人没有联网电脑
-> 去街道 / 职介中心
-> 工作人员使用已经联网的就业系统
-> 得到岗位信息
-> 本人再打电话 / 去现场 / 参加招聘会
```

从机构史看：就业服务已经数字化。

从家庭互联网史看：这个人可能仍然没有上网。

两句话可以同时成立。

这也是为什么 old-Web archaeology 不能只用“家庭网民规模”和“网站上线日期”来解释数字基础设施如何改变普通生活。

---

# 15. 与海外对照的边界

跨仓研究同时检查了法国 ANPE / Minitel：1990s 的法国已经存在求职者直接操作 Minitel 查询并提交岗位申请的全国服务。

海外材料主要写入 `how-people-lived`，本仓不把研究 scope 扩成全球旧网史。

在这里只保留一个比较变量：

> **同样叫 employment-service digitization，可以是 worker-facing terminal，也可以是 clerk-facing backend。**

这有助于以后描述中国对象时避免“数字化”这个词过度抽象。

---

# 16. 证据等级表

| Claim | Evidence | Grade | 当前能证明什么 |
|---|---|---:|---|
| 1998 中央文件要求劳动力市场现代化信息服务，并列电视、广播、职业介绍窗口 | 1998-06-09 中央通知 | A | 多渠道公共服务设计存在 |
| 1998 后开始以城市为中心建设劳动力市场计算机网络 | 2009 劳动保障部门回顾 | C/B | 官方沿革叙述，需原始技术文档继续核对 |
| 2000 省级监测中心被定义为连接城市网的非实时计算机网络系统管理中心 | 劳社培就司发〔2000〕8号 | A/B | “信息网”至少有后台 / 行政网络含义 |
| 2001 64/100 试点城市实现市区内实时联网 | 2001 统计公报 | A | 公共就业业务系统联网范围扩大 |
| 2002 90 城市实现市区内实时联网 | 2002 统计公报 | A | 同上 |
| 舟山 1999 就业信息同时通过报纸、广播、电视、电信、Internet、LED 等发布 | 后来地方志 | C/B | 多接口并存；不能证明各接口使用比例 |
| `www.lm.gov.cn` 在 2002–2006 有明确公共 Web 证据 | 既有 artifact probe | 见原文件 | public-Web 层后来明确存在，但历史 capture 尚未核验 |

---

# 17. 下一步 artifact 优先级

1. 查《劳动力市场信息网建设实施纲要》原始全文，找是否包含网络拓扑、通信协议、终端类型或数据交换方式。
2. 查 1998–2002 各城市“三化”建设验收材料，优先找：系统结构图、软件名、服务器 / 客户端、局域 / 广域网说明。
3. 查当年职业介绍中心培训教材、操作手册、政府采购 / 招标资料。
4. 找“求职者查询终端”与“职介员业务终端”的同期照片或使用说明，严格区分两者。
5. 继续追 `www.lm.gov.cn` historical capture，但不要假定它就是 1998 后台网络的直接 Web 化版本。
6. 若找到历史 Web capture，再记录 Content-Type、charset、DOM、forms、JS、浏览器假设与第二时点；当前不要猜。
7. 若后台系统没有公开 URL，考虑以软件手册 / 截图 /采购文件作为 non-Web digital artifact，而不是强迫它进入 Wayback 框架。

---

# 18. 这一轮真正新增的 old-Web 认识

此前可以问：

> “中国劳动力市场网什么时候上线？”

本轮把问题改成了三层：

```text
什么时候岗位记录开始被计算机管理？
什么时候就业服务机构之间开始联网共享？
什么时候普通求职者开始直接面对 Web / 远程终端？
```

这三个时间点不必相同。

对普通人来说，第一、第二层甚至可以在本人完全没有 Internet 的情况下，已经改变“去一个职介所能查到多少地方的岗位”“工作人员多久能找到信息”“同一份信息能否出现在 LED、电视、热线和网站上”。

因此，研究中文旧网时，最容易漏掉的一类基础设施可能恰恰是：

> **它已经数字化了生活，却还没有长成一个我们今天能输入 URL 打开的网页。**

---

*本研究 note 由 OpenAI GPT-5.6 Sol 辅助整理。未取得的协议、客户端、浏览器、编码与 historical capture 均保留 UNKNOWN；不把“信息网”按今天语义自动改写成 Internet / WWW。*