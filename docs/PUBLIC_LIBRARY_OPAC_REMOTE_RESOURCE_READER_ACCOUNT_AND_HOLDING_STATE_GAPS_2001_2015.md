# 公共图书馆 OPAC、网络图书馆、读者账户与远程资源状态缺口（约 2001–2015）

Status: research note / state-gap model  
Scope: 中文 Web，约 2001–2015  
Companion: `tmzncty/how-people-lived/topics/public-libraries-access-without-ownership-information-commons-and-life-course-fallback-china-1954-2026.zh-CN.md`  
Last research pass: 2026-09-06

## 0. 为什么这是 old-Web 问题

公共图书馆网页特别容易给后来的研究者制造一种错觉：

> “页面上搜得到这本书/这个数据库，所以当年用户已经可以在线获得它。”

实际上，公共图书馆 Web 同时连接了几套完全不同的状态系统：

- 公共网站内容；
- OPAC / 联机公共目录；
- 具体分馆 holdings；
- 在架/外借/预约状态；
- 读者证与账户；
- 网上续借/预约；
- 数据库授权；
- IP/地域认证；
- 文献传递；
- 馆际互借；
- 电子阅览室共享终端；
- 最终线下取书/还书。

因此本 note 不写“数字图书馆发展史”，而建立可复用的状态边界。

遵循 `docs/METHOD.md`：

> **catalog-visible ≠ holding-exists ≠ currently-available ≠ request-accepted ≠ item-routed ≠ item-picked-up**

以及：

> **database-listed ≠ authenticated ≠ entitled ≠ full-text-returned ≠ user-read/downloaded**

---

## 1. 2004–2009：电子阅览室是共享计算终端，不是“家里多了一台电脑”

文化部 2011 年对公共图书馆 2000s 的统计回顾显示：

- 2009 年全国公共图书馆共有计算机 126207 台；
- 比 2004 年增加 131.8%；
- 2009 年电子阅览室终端 72150 个；
- 比 2004 年增加 167.0%；
- 电子阅览室面积从 2004 年的 14.0 万平方米增至 2009 年 34.4 万平方米。

Source:
- 文化部财务司，2011-01-05，《“十五”以来全国公共图书馆发展情况分析》：
  https://zwgk.mct.gov.cn/zfxxgkml/tjxx/202012/t20201204_906399.html

Evidence:
- A：政府统计。

这能证明公共图书馆在 2000s 快速增加共享计算终端，但不能证明：

- 每台终端都接公网；
- 所有终端权限相同；
- 每个人都可免费使用；
- 终端一直有空位；
- 所有数据库都允许普通 Web 浏览。

2008 年重庆图书馆同期报道提供了一个重要反例：电子阅览室座位已满，一名准备进去查资料的读者无法立即进入；同一空间还有未成年人使用终端玩网络游戏。

Source:
- 重庆商报/新浪，2008-03-17：
  https://news.sina.com.cn/c/2008-03-17/070313583566s.shtml

Evidence:
- B：同期现场报道。

因此需要一条 **shared-terminal state chain**：

```text
library open
→ electronic-reading-room open
→ user eligible
→ card/identity requirement satisfied
→ terminal slot available
→ session opened
→ permitted network/resource reachable
→ task completed
→ session closed
```

`terminal exists ≠ terminal slot available`。

---

## 2. 2009 浙江网络图书馆：一个很好的多状态旧网对象

2009-05-26，浙江网络图书馆上线。开通次日的同期报道给出 original locator：

- `http://www.zjelib.cn/`

并描述首页具有：

- 全文检索；
- 图书；
- 期刊；
- 报纸；
- 学位论文；
- 会议论文；
- 专利；
- 标准；
- 视频；

等查询入口。

同期报道还明确区分：

1. 浙江省范围内上网即可搜索/使用一部分资源；
2. 浙江图书馆、杭州图书馆等持证读者登录后可获得更多功能；
3. 有版权限制的图书可能只提供试读；
4. 无直接全文权限时可发起原文传递；
5. 纸质馆藏可通过馆际互借申请，由图书馆邮寄；
6. 人工咨询/知识导航仍作为独立服务存在。

Source:
- 今日早报/新浪，2009-05-27，《浙江开通“24小时图书馆”》：
  https://news.sina.com.cn/c/2009-05-27/045815690485s.shtml

Evidence:
- B+：上线次日同期现场报道与机构采访。资源规模、速度和“国内首例”等平台参与方主张不能当独立审计。

当前浙江工商大学图书馆的后期介绍也追溯该平台 2009 年 5 月正式上线，并说明其长期依赖统一认证和全省公共图书馆成员体系。

Source:
- 浙江工商大学图书馆，浙江网络图书馆介绍：
  http://www.zjelib.cn/ locator 见
  https://lib.zjgsu.edu.cn/2019/0115/c1027a38201/page.htm

Evidence:
- C/A- mixed：后期机构说明，可确认长期机构定位；不能替代 2009 原页面。

---

## 3. 必须拆开的目录状态

### 3.1 Bibliographic record 不等于馆藏实体

最小状态链：

```text
query submitted
→ bibliographic record returned
→ one or more holdings associated
→ branch/location known
→ copy status known
→ available now / checked out / missing / processing / non-circulating
→ user decides next action
```

必须固定：

- `search hit ≠ physical copy exists at this branch`
- `holding record ≠ copy currently on shelf`
- `available flag ≠ user physically found it`
- `shelf location ≠ item can be borrowed`

OPAC 截图最多证明系统在某时刻展示了某个状态，不独立证明现实书架状态完全同步。

### 3.2 联合目录不等于统一借阅权

浙江网络图书馆的意义之一是能检索跨馆资源，但：

```text
cross-library discoverability
≠
local borrowing entitlement
≠
interlibrary-loan eligibility
```

用户可能看见另一个馆的书，却仍需要：

- 特定馆读者证；
- 馆际互借申请；
- 费用/邮资；
- 等待调拨；
- 到指定地点取件。

---

## 4. 网上预约/馆际互借必须拆成事务链

如果历史页面出现“预约”“借阅申请”“馆际互借”按钮，不能写成“网上借书完成”。

建议状态模型：

```text
item selected
→ user authenticated
→ eligibility checked
→ request submitted
→ server durably records request
→ lending library accepts / rejects
→ item reserved or retrieved
→ routing / postal handoff
→ destination library or address receives item
→ user notified
→ user actually encounters notice
→ pickup / delivery completed
→ checkout record created
```

其中至少有以下 gap：

- **click / durable-request gap**
- **request / acceptance gap**
- **acceptance / physical-retrieval gap**
- **routed / arrived gap**
- **notice-issued / notice-seen gap**
- **arrived / borrowed gap**

一个 archive 只保存 request confirmation 页，也不能证明物理书最终到达。

---

## 5. 数字资源认证是另一套状态机

数字图书馆尤其容易被今天的“点链接就下载”心智误读。

2009 浙江网络图书馆同期报道已经表明，不同资源存在：

- 地域/IP 条件；
- 是否持读者证；
- 是否有全文权限；
- 试读；
- 文献传递；

等差异。

建议状态链：

```text
resource appears in portal
→ metadata/search result visible
→ access mode identified
→ region/IP condition satisfied (if any)
→ reader account authenticated (if required)
→ license entitlement checked
→ content server session established
→ preview / full text / streaming result returned
→ user actually opens/downloads it
```

固定规则：

- `portal-listed ≠ licensed-to-user`
- `metadata-visible ≠ full-text-readable`
- `reader login success ≠ every database entitlement`
- `institutional IP recognized ≠ home IP recognized`
- `download link rendered ≠ download completed`

### 5.1 authentication type 不能由今天页面反推

old-Web 证据至少要区分：

- IP-based；
- reader-card username/password；
- province/network boundary；
- campus/library proxy；
- certificate/plugin；
- vendor-side secondary login；
- anonymous public access。

如果 historical capture 没有看到 backend/redirect，不得仅因今天服务采用某种统一认证，就写回 2009。

---

## 6. 文献传递：email 是图书馆 Web 的离站 transport

2009 浙江网络图书馆同期报道明确描述：部分无权限直接下载全文的用户可以发起原文传递请求，并提供 email 地址接收文献。

这意味着 Web task 并不止于当前 site：

```text
search result
→ document-delivery form
→ request accepted
→ librarian/system finds source
→ rights/size constraints checked
→ email sent
→ mailbox accepts mail
→ user actually encounters attachment/link
```

因此：

> **request confirmation ≠ document delivered**

并且 archive 通常只可能保存公共表单壳层，几乎不会合法保存真实 email、请求文献和附件交付结果。

这构成：

## **public-search-shell / private-delivery-state asymmetry**

---

## 7. 2010–2011：公共电子阅览室与免费开放增加了一层权限变化

文化部 2010 年宣布公共电子阅览室建设试点，明确准备在北京、天津、辽宁、山东、上海、浙江、广东、安徽、陕西开展试点；2011 年免费开放政策进一步把电子阅览室上网费纳入基本免费项目的取消范围。

Sources:
- 文化部，2010-09-30，《全国公共电子阅览室建设试点工作将展开》：
  https://www.mct.gov.cn/whzx/ldhd/201009/t20100930_696006.htm
- 文化部，2011-02-22，山东免费开放实例：
  https://www.mct.gov.cn/whzx/qgwhxxlb/sd/201111/t20111121_787370.htm

Evidence:
- A：政府同期信息。

但“免费”仍不能抹掉：

- reader-card；
- 押金；
- 身份证；
- 每日时长；
- 内容过滤；
- 未成年人规则；
- 机器数量；
- 开放时间。

例如 2011 年山东省图书馆青少年电子阅览室对未成年人免费开放，但每人每日上网不得超过 2 小时。

Source:
- 文化部/中国文化报，2011-06-07：
  https://www.mct.gov.cn/whzx/qgwhxxlb/sd/201111/t20111121_787400.htm

Evidence:
- A-/B+。

因此：

> **free ≠ unlimited ≠ anonymous ≠ always available**

---

## 8. old-Web 最容易错的 archive inference

### 8.1 搜索框幸存，不等于数据库幸存

OPAC/数字图书馆页面往往是：

```text
static shell
→ CGI/JSP/ASP/search endpoint
→ live database
```

Wayback 可能保存表单和样式，却没有：

- POST response；
- session；
- catalog backend；
- vendor database；
- current holding states。

因此一个能打开的“检索首页”不能自动算完整 transaction capture。

### 8.2 archive 保存的 search result 可能是 URL-query artifact

GET 参数型 OPAC 结果有时可能被保存，但需要检查：

- capture datetime；
- query 参数是否被 archive rewrite；
- 是否只是错误页/超时页；
- 结果是否来自原站还是现代重定向；
- charset 是否正确；
- 搜索结果页中的 availability 是否动态二次加载。

### 8.3 当前 OPAC 不能证明 2009 OPAC

今天仍在运行的 `opac.*` 页面可以证明“当前系统怎样工作”，不能证明：

- 2009 使用同一 vendor；
- 同一数据库 schema；
- 同一字段命名；
- 同一 JS；
- 同一编码；
- 同一 reader-account contract。

### 8.4 modern browser success ≠ historical browser success

2000s 图书馆系统可能依赖：

- IE；
- frames；
- GB2312/GBK；
- JavaScript；
- vendor popups；
- 下载控件/阅读器；
- 第三方数据库插件。

没有 M3 验证时，现代 Chromium 回放不能写成“当年读者体验”。

---

## 9. 平台可观察事实与私人状态分层

### Publicly observable

可能进入 archive：

- 首页；
- 搜索框；
- 书目结果；
- 数据库目录；
- 读者服务说明；
- 开放时间；
- 费用；
- 办证规则；
- 帮助页面。

### Authenticated/private

通常不应进入公开 archive：

- 读者姓名/证件号；
- 借阅历史；
- 当前在借；
- 预约队列；
- 罚款；
- email；
- 文献传递请求；
- 真实下载历史；
- 登录 cookie/session。

因此存在：

## **public-catalog-shell / private-reader-state asymmetry**

历史研究最容易看到“图书馆承诺提供什么”，最难看到“一个具体普通人最终拿到了什么”。

---

## 10. 与普通生活史连接时的禁止推断

不得直接写：

```text
OPAC existed
→ everyone knew the item existed
```

不得写：

```text
network library launched
→ home access became universal
```

不得写：

```text
electronic reading room existed
→ ordinary household Internet access existed
```

不得写：

```text
free opening
→ zero access cost
```

不得写：

```text
catalog says available
→ person borrowed/read it
```

允许的窄结论是：

> 某年、某平台公开提供某种 catalog/resource/request interface；同期材料证明至少有读者实际使用；进一步的 authentication、backend transaction 和现实取得状态仍需独立证据。

---

## 11. M1 candidate locators 与本轮负结果

### Candidate A — 浙江网络图书馆

Historical original locator from 2009 contemporary report:

- `http://www.zjelib.cn/`

Research value:

- portal + unified search；
- reader-card login；
- rights-dependent digital access；
- document delivery；
- interlibrary loan；
- public/private state split。

### Candidate B — 重庆数字图书馆

2009 contemporary locator:

- `www.cqelib.cn`

Source:
- 中国新闻网/搜狐，2009-09-27：
  https://news.sohu.com/20090927/n267035714.shtml

Research value:

- reader-card-derived digital access；
- databases / books / exam resources；
- useful cross-city comparison against Zhejiang。

### Negative result

本轮**没有取得并实际打开一份满足本仓 M1 最低门槛的 2008–2010 中文公共图书馆完整 Wayback/WARC transaction capture**。

因此以下内容继续保持 `unknown`：

- `zjelib.cn` 2009 原始 DOM；
- HTTP charset / Content-Type；
- query endpoint；
- GET/POST 形式；
- cookie/session；
- 读者证认证协议；
- 地域/IP 判定实现；
- 第三方数据库 handoff；
- 文献传递后台；
- 馆际互借 durable state；
- historical browser requirement。

新闻里出现 URL 只登记为 **historical locator**，不冒充 verified memento。

---

## 12. 隐私 stop condition

不要为了重建 reader state：

- 使用泄露的图书馆账户；
- 搜集普通人借阅历史；
- 重放真实身份证/读者证号；
- 公开文献传递 email；
- 把私人预约/罚款/阅读历史重新拼回个人身份。

本题真正需要复原的是**系统状态模型与公共界面**，不是某位普通读者的私人借书档案。

---

## 13. 下一步

优先：

1. 对 `zjelib.cn` 做 Wayback CDX/capture 日期调查；
2. 寻找 2009–2010 的帮助页、登录说明、馆际互借说明；
3. 找到至少一份历史 OPAC search-result capture，而不只首页；
4. 对比浙江/重庆/上海/深圳的 reader-card authentication；
5. 记录 browser/charset/vendor；
6. 若找到完整 capture，再把本 note 升级为 M1 case 候选。

在此之前维持：

> **platform service existence = supported**
>
> **historical original transaction = not yet verified**
