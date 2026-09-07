# 网吧、共享终端、身份登记与公共接入：从“有网页”到“这个人真的能上”的状态缺口（1996—2015）

> Scope：只研究约 1996—2015 年中文 Internet / Web 环境中，网吧、公众电脑屋、共享终端和相关管理页面怎样把普通人接到网站、聊天工具、邮箱、论坛和游戏；重点恢复“到店—登记—分配机位—联网—登录账号—退出 / 重置”的技术与生活状态。
>
> 中国 1994 年以前的科研网络 / email 前史、1996—2026 的普通生活变化、migrant worker / youth 使用、海外 cybercafe / PC bang 对照，主要写入 `tmzncty/how-people-lived/topics/internet-cafes-shared-access-session-local-digital-life-and-public-compute-china-1996-2026.zh-CN.md`。本文件不把 `old-web-archaeology` 扩成全球公共计算史。

本题不是“老网吧怀旧”。它要解决一个旧网考古的基础误差：

> **archive 证明某个网站在 2004 年存在，并不等于一个 2004 年普通用户当时有设备、地点、钱、证件、浏览器、客户端和会话状态去真正使用它。**

---

## 1. 研究单位：不要把 Internet、网页、机器、会话和人压成一个对象

至少区分：

- Internet backbone / ISP；
- public access venue / 网吧 / 公众电脑屋；
- venue operator；
- physical terminal / 机位；
- local OS image；
- browser；
- browser plugins / ActiveX / Java / Flash；
- IM / game / mail client；
- local disk / temporary files；
- restore card / reimage / reboot state；
- venue account / membership card；
- identity document；
- registration database；
- person-to-seat assignment；
- paid session；
- IP / NAT / proxy / filtering state；
- Web account / QQ / email / game identity；
- page / URL；
- server-side session / cookie；
- downloaded file；
- logout / timeout / forced shutdown；
- current legacy page；
- verified historical capture。

因此固定：

```text
Internet connected ≠ venue exists
venue exists ≠ affordable seat available
seat available ≠ user passes identity gate
identity accepted ≠ paid session started
session started ≠ target site reachable
site reachable ≠ browser renders correctly
page renders ≠ user can authenticate
account login ≠ local files survive next visit
historical article exists today ≠ historical terminal environment reconstructed
```

---

## 2. 基础状态机：一个普通人“去网吧上网”至少经过多少层

```text
用户来到现实场所
→ 场所营业 / 有空机
→ 证件 / 年龄 / 会员卡条件满足
→ 服务台建立或查找登记记录
→ 缴费 / 余额有效
→ 分配具体机位
→ 本地 OS / 管理客户端进入可用状态
→ 网络接入成功
→ 浏览器 / QQ / 游戏 / 邮件客户端启动
→ 目标服务可达
→ 用户输入自己的账号 / 密码
→ 服务端认证成功
→ 实际阅读 / 聊天 / 下载 / 游戏 / 提交
→ 本地生成缓存、历史、文件或日志
→ 用户主动退出 / 时间到 / 机器重启
→ 本地状态被保留、清除或还原
→ 下一位用户进入
```

旧 Web archive 通常只保存其中的：

```text
目标网站的一份 HTTP 表示
```

所以从 archive 页面直接写“2005 年用户可以这样操作”经常跨越了十几层未经验证的状态。

---

## 3. 1996—1998 上海：Web 站点已经存在，但“人怎样得到一台联网机器”仍是独立基础设施问题

1998-08-26《中华读书报》同期报道上海网吧时记录：上海 1996 年 5 月出现第一家网吧“威盖特”；到报道时约 400 家网吧 / 公众电脑屋完成登记；上网费从早期约 50 元/小时下降到约 14 元/小时。报道同时给出当时上海家庭计算机普及率约 8% 的地方数字。

同期媒体（B）：

- <https://www.gmw.cn/01ds/1998-08/26/GB/213%5EDS3505.htm>

对 old-Web archaeology 来说，这个对象必须加入 **venue-to-page executability gap / 场所—页面可执行缺口**。

即使我们以后找到 1998 年某站的完整 WARC，也仍需另问：

- 用户有没有自己的 PC？
- 如果没有，附近是否有公众电脑屋？
- 一小时价格相对其工资 / 零花钱是多少？
- 是否排队？
- 机器上是什么浏览器？
- 能不能使用中文输入？
- 是否有 email / chat client？
- 是否允许下载 / 复制文件？

因此历史网站的 `available` 必须拆成至少两个层次：

```text
network-available
person-executable
```

---

## 4. 公共终端制造一种 archive 很难直接保存的“会话型数字生活”

共享机器与家庭 PC 最大的状态差异之一是：

```text
账号可能长期存在
但本地机器并不属于这个人
```

一个用户可能今天使用 37 号机，明天使用另一家店的 12 号机，但仍登录同一个 QQ / 邮箱 / 论坛 / 游戏账号。

这里加入 **terminal-to-account gap / 终端—账号状态缺口**。

### 4.1 服务端连续，不等于本地连续

Web archive 可能保留：

- 论坛账号；
- blog 页面；
- webmail help；
- QQ 产品页；
- 下载站。

却往往无法恢复：

- 某次网吧机器上的 cookie；
- 浏览器 history；
- 本地聊天记录；
- 下载目录；
- 未上传的照片 / 文档；
- 输入法词库；
- 插件版本；
- 游戏补丁；
- USB / floppy handoff；
- 关机前是否真正 logout。

于是一个人的数字生活可以“服务器上很长寿，本地每晚重生”。

这里称为 **session-local state / 会话本地状态**。

---

## 5. 2002 以后：公共接入本身成为一个制度 / 身份 transaction

2002 年国务院令第 363 号《互联网上网服务营业场所管理条例》把“通过计算机等装置向公众提供互联网上网服务的网吧、电脑休闲室等营业性场所”明确纳入管理。

法规范当前官方公开版本（A，制度文本）：

- <https://www.qingdao.gov.cn/zwgk/zdgk/fgwj/zcwj/zfgb/2002_21/202010/t20201025_1750085.shtml>

随后地方同期报道留下不同的身份实现。

### 5.1 天津，2003—2004：身份证 → 实名上网卡 → 机位

2004-04-02 的同期报道说，天津自 2004-04-15 起全面推广实名制：先凭身份证购买上网卡，再凭卡上网；2003-12-20 起已在市内六区 400 余家网吧试运行。报道还提到实名卡同时被经营者用于自动计费。

B：

- <https://news.sohu.com/2004/04/02/34/news219713498.shtml>

可支持：

```text
至少在该地方 / 时点，Internet access 前增加了一层 venue identity + billing state。
```

不能支持：

- 全国同日使用同一技术；
- 卡片数据 schema；
- 后台协议；
- 读卡器厂商 / 软件版本；
- 每一次实际执行都完全符合制度设计。

### 5.2 上海，2004：不同现实身份凭证进入同一公共接入系统

2004-11-25 同期报道说，上海市民使用社保卡，外地人士使用身份证，外籍人士使用护照；报道描述一个覆盖全市 1350 家网吧、约 12 万台终端的经营管理系统。

B：

- <https://news.sohu.com/20041125/n223178578.shtml>

这里新增 **credential-to-session gap / 凭证—会话缺口**：

```text
credential valid ≠ record successfully created
record exists ≠ seat assigned
seat assigned ≠ network session starts
```

### 5.3 北京，2008：现实人 → 照片 + 身份证扫描 → 监管记录 → 以后跨店查找

2008-10-17 新华社报道记录一名外地游客首次进入北京网吧时，被要求拍照并扫描身份证；报道说当时约 1500 家网吧已部署相关设备。另一篇同期转载进一步描述，首次登记后，以后进入已部署系统的网吧可报身份证号并由工作人员核对档案。

B：

- <https://news.sina.com.cn/c/2008-10-17/152816474573.shtml>
- <https://news.sina.com.cn/o/2008-10-17/060614587660s.shtml>

这对旧网身份史很重要，因为它明确形成两层 identity：

```text
现实入口身份：身份证 / 照片 / 机位 / 时间
应用身份：QQ 号 / forum username / email / game handle
```

因此固定：

> `real-name venue access ≠ real-name Web account`。

---

## 6. 2008—2010：同一个人可能同时处在网吧、家庭、学校和手机四个接入层

CNNIC 2008 青少年报告记录：青少年网民在网吧上网比例为 57.5%，农村青少年网民为 65.4%；同时近五成青少年网民已经使用过手机上网。

A/B（机构调查）：

- <https://www.cnnic.cn/n4/2022/0401/c116-890.html>

2009 年报告记录：手机上网比例升至 74%，网吧比例降至 49.4%；农村青少年手机上网比例为 74.5%。

- <https://www.cnnic.cn/n4/2022/0401/c116-907.html>

2010 年报告继续记录家庭、学校和手机的替代 / 叠加。

- <https://www3.cnnic.cn/n4/2022/0401/c116-841.html>

对 Web archaeology 的直接意义是：

> **不要给一个历史页面假定唯一“典型终端”。**

2009 年同一个论坛帖子可能被用户：

- 家庭台式 PC 浏览；
- 学校机房浏览；
- 网吧 IE 浏览；
- 手机 WAP / mobile Web 浏览；
- 通过转帖 / QQ 链接间接看到。

所以浏览器 / viewport / 登录状态 / 输入能力可能完全不同。

这叫 **multi-access-path divergence / 多接入路径分歧**。

---

## 7. 网吧是 old-Web browser archaeology 不能跳过的一种“历史浏览器容器”

如果未来要做 M3 浏览环境复原，不能只复原“某年的 IE6”。

网吧终端至少还可能包含：

- Windows 版本；
- Internet Explorer 版本；
- Netscape / Firefox / Maxthon 等替代浏览器；
- ActiveX 控件；
- Flash / Java；
- QQ / OICQ / MSN；
- 游戏客户端；
- 下载工具；
- 输入法；
- 网吧管理 / 计费软件；
- 还原卡 / 冰点类环境；
- 代理 / NAT；
- 本地缓存或镜像；
- 机器分辨率和显示器尺寸。

当前网页的 HTML 不能告诉我们这些状态。

因此加入 **historical-terminal environment gap / 历史终端环境缺口**。

在取得当年网吧装机盘、网管手册、软件广告、论坛配置帖或抓包以前，不能写：

```text
“2004 年网吧用户看到的页面就是现代 Wayback 截图这样。”
```

---

## 8. 本地重置可能主动删除最重要的 ordinary-life traces

共享终端通常需要快速恢复给下一位顾客使用。

无论具体店铺采用什么技术，只要存在重启恢复、磁盘还原或定期重装，就会形成一个 old-Web archaeology 特有的悖论：

> **运营上越成功地清除用户本地痕迹，历史上越难恢复一个普通人真实使用过什么。**

这里称为 **machine-reset archive gap / 机器重置档案缺口**。

需要未来用同期技术资料确认的字段：

- local disk 是否可写；
- 哪些分区被还原；
- reboot 是否清除；
- browser cookies 是否持久；
- chat history 保存在哪里；
- downloaded files 是否跨会话；
- USB / floppy 是否可用；
- 是否存在个人网络盘 / server share。

本轮没有取得足够同期技术证据，所以这些全部保持 `unknown`，不能从后来网吧经验反推 2000s 每家店。

---

## 9. Web 页面与现实公共终端之间至少有十类固定 state gap

### 9.1 venue-to-person access gap / 场所—个人可及缺口

```text
site online ≠ person has affordable / reachable terminal
```

### 9.2 identity-to-session gap / 身份—会话缺口

```text
valid ID ≠ session actually starts
```

### 9.3 session-to-page gap / 会话—页面缺口

```text
paid computer time ≠ target URL reachable and renderable
```

### 9.4 account-to-terminal gap / 账号—终端缺口

```text
QQ / email account persists ≠ same machine / cookies / local history persists
```

### 9.5 local-file survival gap / 本地文件存活缺口

```text
download completed ≠ file survives reboot / reimage / next visit
```

### 9.6 credential-log / content asymmetry / 凭证日志—内容不对称

实名系统可能记录“谁、何时、哪台机器”，但并不因此保存：

- 她读了哪篇文章；
- 聊了什么；
- 下载了什么；
- 后来现实生活发生什么。

反过来，Web archive 可能保存一篇页面，却完全不知道当时哪个具体公共终端用户读过它。

### 9.7 public-terminal security-state gap / 公共终端安全状态缺口

archive 不会自动保存本地 keylogger、木马、被修改的浏览器或前一位用户留下的状态。

海外 2003 Kinko's 公共终端键盘记录器案件可作为风险机制对照，但不能类推中国发生率：

- <https://www.cbsnews.com/news/cybercafes-pose-security-problems/>

### 9.8 public-to-private handoff gap / 公共—私人交接缺口

一个用户可能在网吧：

```text
找到号码 / 地址 / 招聘 / 商品
→ 抄到纸上 / 存到 U 盘 / 发给自己的 QQ / 打电话
→ 离开网吧
→ 在线下完成
```

网页只保存最前端，结果发生在场所外。

### 9.9 browser-container gap / 浏览器容器缺口

同一 archive HTML 在：

- IE5 / IE6；
- 不同 Flash；
- 不同 ActiveX；
- 不同字体 / GBK 配置；
- 不同 screen resolution；

可能是完全不同的可执行对象。

### 9.10 venue-function temporal collapse / 场所功能时间塌缩

今天的“电竞馆 / 网咖”网站不能倒推 2004 年网吧的：

- 价格；
- 软件；
- 用户用途；
- 硬件；
- 会员系统；
- 身份登记；
- 浏览器环境。

品牌连续不等于技术系统连续。

---

## 10. 2008 外来工材料：网页考古怎样连接回现实使用，而不越界

2008-04-02《海峡导报》调查厦门翔安一个 industrial-village 周边网吧，报道外来工下班后去网吧的现实路线；受访“小张”明确提到放松、看新闻、了解外部事情。

B，同期个人材料：

- <https://news.sina.com.cn/s/2008-04-02/051613671211s.shtml>

old-Web 侧可以据此增加一种 **person-level usage evidence**：

```text
有同期媒体记录一个具体人 / 场景确实把公共终端用于信息获取。
```

但绝不能把它转换成：

```text
“这个人看过 archive 中的某一个具体网站”
```

除非得到页面 / 浏览历史 / 本人记录等更窄证据。

所以需要把：

- Web-visible content；
- venue capability；
- reported user activity；
- exact visited page；

分成四个不同字段。

---

## 11. 2010s：当家用宽带 / 手机替代“基本接入”以后，网吧页面本身也开始发生意义迁移

2018 年人民网采访网吧经营者和长期用户，回顾 2000 年代早期聊天、语音视频和游戏，并描述后来随着智能手机、微博、微信普及，单纯为了聊天去网吧的行为减少，场所更多转向游戏和社交。

C/B：

- <https://media.people.com.cn/n1/2018/1023/c40606-30356433.html>

对 1996—2015 的旧网研究而言，重要的不是把 2018 回忆当一手技术资料，而是建立一个未来验证问题：

> **同一个“网吧”品牌 / 类别，在不同年份究竟出租的主要稀缺能力是什么？**

候选状态：

```text
Internet connection
→ networked PC
→ game client / performance
→ social co-presence
```

必须用各时期独立材料核验，不能由 2018 访谈一口气回填 1996—2015。

---

## 12. 与已有 old-Web state-gap 专题的交叉

本文件不是重写已有专题，而是提供它们的**person-level access substrate / 个人接入底座**。

### 12.1 Webmail

已有：`WEBMAIL_ACCOUNT_ADDRESS_DELIVERY_AND_SERVICE_CONTINUITY_STATE_GAPS_1998_2015.md`

新增问题：

```text
邮箱存在
+ 网吧终端可用
+ 浏览器兼容
+ 用户记得密码
+ 没有泄漏凭证
→ 才能在共享机器上执行 webmail
```

### 12.2 Pager / email gateway

已有：`PAGER_WEB_GATEWAY_EMAIL_TO_PAGER_AND_REACHABILITY_STATE_GAPS_1999_2007.md`

新增问题：Web gateway 可用不代表发送者拥有私人机器；公共终端可能是发送侧的一部分。

### 12.3 Online banking / remittance

已有：

- `ONLINE_BANKING_REMITTANCE_AND_PAYMENT_STATE_GAPS_1997_2015.md`
- `ONLINE_BANKING_POSTAL_REMITTANCE_AND_MONEY_TRANSFER_STATE_GAPS_2005_2015.md`

新增问题：在公共机器执行敏感金融事务的安全状态与家庭 PC 不同；不能只按服务端页面考古。

### 12.4 Resume / recruiter / job search

已有：`RESUME_CHRONOLOGY_CAREER_GAPS_REENTRY_AND_PRIVATE_RECRUITER_STATE_GAPS_1999_2015.md`

本轮尚未找到足够的一手链条证明普通 migrant worker 普遍通过网吧投简历，因此只建立接口，不补因果故事。

### 12.5 Search / directory

已有：`SEARCH_DIRECTORY_QUERY_RANKING_AND_INDEX_STATE_GAPS_1997_2015.md`

新增问题：历史搜索结果页面可被 capture，但输入查询的公共终端状态、缓存和后续行动通常没有保存。

---

## 13. Archive strategy：公共终端研究需要的不只是 Wayback

未来的证据包应主动寻找不同 artifact family：

### A. Web / archive

- 网吧官网 / 门店页面；
- 网吧管理软件官网 / 帮助；
- 计费系统产品页；
- 实名登记系统说明；
- 当时 ISP / 网吧行业页面；
- Wayback / WARC / Common Crawl。

### B. Software / hardware

- 网管软件安装包；
- 还原卡说明书；
- 上网卡 / 读卡器手册；
- 网吧装机镜像 / 软件清单；
- 浏览器 / QQ / 游戏客户端版本资料；
- 网吧路由 / proxy / NAT 设备手册。

### C. Visual / material evidence

- 同期网吧照片；
- 收费牌；
- 会员卡；
- 机位号；
- 读卡器 / 摄像登记终端；
- 软盘 / U 盘 / 打印服务广告。

### D. Life evidence

- 同期用户帖子；
- 日记 / 博客；
- migrant worker / student 采访；
- 店主日志；
- “第一次上网”同期记录。

这些 evidence family 合起来，才可能恢复“页面如何真正进入普通人的手”。

---

## 14. M1 状态：NOT ACHIEVED IN THIS SLICE

本轮实际取得并检查的是：

- 当前仍在线的 1998 同期新闻页面；
- 当前官方公开的 2002 法规范文本；
- 当前仍在线的 2004 / 2008 同期新闻页面；
- 当前 CNNIC 保存的 2008—2010 调查报告页面；
- 当前仍在线的同期 / 后来用户与行业采访。

本轮**没有实际取得并检查**一份满足 M1 的 1996—2010 中文网吧 / 管理软件 / 门店网站 verified Wayback/WARC capture。

因此以下内容全部保持 `unknown`：

- 某一家 1998 / 2004 网吧网站的 historical DOM / CSS；
- 原始 charset / Content-Type；
- 当时网吧终端常见浏览器版本的可核验证据；
- ActiveX / Flash / Java 具体配置；
- 实名卡后台 protocol / schema；
- 身份登记数据库字段；
- 机位—身份—时间的实际日志结构；
- 还原卡 / 本地磁盘保留策略；
- cookie / local file persistence；
- QQ / 游戏 / webmail 客户端实际版本组合。

固定写法：

```text
M1 NOT ACHIEVED IN THIS SLICE
```

而不是：

```text
Wayback 没有这些东西
```

搜索未完成不能作为历史不存在的负证据。

---

## 15. 后见之明 / 复原风险

1. **不要把 1994 国家全功能接入当成普通用户终端状态。**
2. **不要把今天“网咖”界面倒投回 2000s。** 当前高性能 / 电竞品牌不是早期页面形态证据。
3. **不要把 current legacy news page 当 historical capture。** 搜狐 / 新浪今天能显示 2004 / 2008 正文，只证明当前 host 承载历史日期内容。
4. **不要把实名入口当网站实名。** venue identity 与 service account 必须分层。
5. **不要从站点 archive 推断用户浏览器。** 同时要恢复 public-terminal environment。
6. **不要把用户说“去网吧上网”自动翻译成“浏览 Web”。** 可能主要是 QQ、聊天室、语音视频、游戏或下载客户端。
7. **不要把网吧使用率当成没有家庭 Internet 的比例。** 同一用户可能多地接入。
8. **不要把“文件下载成功”推断成文件长期保存。** 公共终端的重启 / 还原可能形成主动丢失。
9. **不要把监管日志存在推断成内容日志存在。** 两者保存语义不同。
10. **不要用 2018 / 2026 怀旧采访单独确定 2000 年价格、软件版本或页面。** 回忆材料只能承担 C 级角色。

---

## 16. 已证实 / 高概率 / 不知道

### 已证实

- 1998 上海同期媒体已经把网吧 / 公众电脑屋作为商业公众 Internet 接入层报道；
- 同一报道明确显示公共场所增长与低家庭计算机普及率可以并存；
- 2002 国家法规范把网吧等营业性公众上网服务场所独立定义；
- 2004 天津 / 上海、2008 北京同期报道存在身份凭证与公共机位之间的登记流程；
- CNNIC 2008—2010 青少年调查显示网吧、家庭、学校、手机入口在转型期同时存在；
- 同期 2008 migrant-worker 报道提供至少一个现实使用公共终端获取新闻 / 信息的个人锚点。

### 高概率但仍需技术 artifact 验证

- 共享终端上的本地状态与长期账号状态经常不同步；
- 网吧管理 / 恢复机制会显著影响 cookie、下载文件、聊天记录等可持续性；
- 不同网吧 OS / browser / plugin 配置会改变 old-Web 页面实际可执行性。

这些是工程上合理的机制，但要写成某年某店的事实，必须找到具体软件 / 装机 / 机器证据。

### 不知道

- 1996—2000 早期中国网吧最典型的 browser stack；
- 特定历史网吧是否保存用户本地文件；
- 2004 实名系统具体数据库 schema 和协议；
- 普通用户在共享终端上完成 webmail / banking / job application 的实际比例；
- 哪些历史门店 / 管理软件存在完整可检验 archive captures。

---

## 17. 下一步最值钱的考古对象

优先找一个能把 **Web + software + physical terminal** 三层真正连起来的 bounded case，而不是再找十篇怀旧文章。

候选：

- 1999—2005 某一家有 archived 官网 / 价格 / 软件说明的网吧；
- 一套 2000s 网吧计费 / 管理软件及其官网、安装手册、客户端截图；
- 一套实名上网卡系统的产品手册与城市部署新闻；
- 一份带明确日期的网吧装机软件清单；
- 一个 public terminal + webmail / QQ / forum 的完整操作记录；
- 一个“下载到软盘 / U 盘 / 打印”的旧网 handoff case。

如果能取得 verified capture，再按 M1 最低字段记录：

```text
archive_source
capture_url
original_url
capture_datetime
HTTP/replay state
main resource
subresources
charset / Content-Type
browser assumptions
missing artifacts
confidence
```

---

## 18. 这项考古为什么会改变我们理解旧 Web 的方式

传统 old-Web archaeology 很容易问：

> “这个页面 2003 年长什么样？”

网吧把问题再往现实里推进一层：

> **“2003 年的哪一种人，在哪一台不属于自己的机器上，花多少钱、拿什么证件、用什么浏览器，才能真正把这个页面变成一次生活行为？”**

如果这一层不恢复，我们保存的可能只是服务器历史，而不是普通人的 Internet 历史。

公共终端最有价值的地方就在于，它让旧网研究看到一个被“家庭 PC 普及率”隐藏的人群：

```text
没有自己的电脑
但有自己的 QQ 号
没有自己的硬盘
但有自己的邮箱
每次换一台机器
却在网上维持一个连续的自己
```

这也是为什么页面 archive、账号连续性、本地会话和现实身份必须被当成四种不同的历史对象。
