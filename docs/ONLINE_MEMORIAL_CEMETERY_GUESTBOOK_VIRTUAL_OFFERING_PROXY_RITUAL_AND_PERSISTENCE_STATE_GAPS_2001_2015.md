# ONLINE_MEMORIAL_CEMETERY_GUESTBOOK_VIRTUAL_OFFERING_PROXY_RITUAL_AND_PERSISTENCE_STATE_GAPS_2001_2015

## 0. Scope

本 note 研究约 2001—2015 中文互联网中的一个此前未独立展开的事务对象：**网上纪念馆 / 虚拟墓地 / 网上祭扫页面究竟保存了什么，用户在页面上“建馆、献花、留言、祭扫、付费、分享”分别对应哪些平台状态，以及一个 Web 页面与现实中的死亡事实、亲属授权、墓位维护和长期纪念之间存在什么缺口。**

它不是中国殡葬史，也不评价网络祭祀是否应取代传统仪式。1995 年海外 online cemetery 只作必要的 Web 前史对照；2020—2026 的云祭扫、身份核验、数字遗产只作为 afterlife / state validation，不扩大本仓约 1995—2015 中文旧网 scope。

本轮首先查重 `how-people-lived` 和本仓既有 photo-album、mobile-number、deaf-communication、online-banking、agricultural-information 等专题；未发现 funeral / obituary / memorial / online cemetery 独立 note。

检索日期：2026-09-08。

---

## 1. Claim list before narrative

本轮只把以下窄 claim 写到较高确定度：

1. **B / high**：2001 年《北京晚报》同期资料明确列出至少六个中文网上纪念/虚拟墓地 historical locators，包括 `cn.netor.com`、`www.qingming.com.cn` 等，并描述在线建馆、照片、生平、网上讣告、论坛等功能。
2. **B / high**：2002 年中新社记者实际进入 `CN.NETOR.COM`，观察到用户自建园区、留言、献花、点烛、歌曲等在线纪念行为。
3. **B / high**：2004 年嘉定普通家庭案例显示，纪念页可被亲友反复访问，并容纳照片、生平、文选、历史相册、年谱与虚拟祭品。
4. **B / high**：同为 2004 年，重庆地方调查又发现部分网上纪念服务几乎无人采用，证明 `service exists != ordinary adoption`。
5. **B / high**：2008 年中国青年报调查显示网上墓地已形成建馆费、年费、维护费、虚拟货币/祭品和多种支付方式，同时消费者已经担心“长期付费以后网页会不会消失”。
6. **B / high**：2008 年记者发现一家早期免费网上公墓虽首页仍可见，但搜索失效、内容长期不更新，证明 `site reachable != service operational`。
7. **B / high**：2015 年网店“代客扫墓”说明 Web/QQ/网店事务可以协调真人去墓前清洁、献花并回传视频；`online order != online ritual only`。
8. **D / high as model**：历史研究必须把 `MEMORIAL_CREATED`、`DEATH_VERIFIED`、`KIN_AUTHORIZED`、`PAGE_PUBLIC`、`OFFERING_POSTED`、`PAYMENT_SETTLED`、`PHYSICAL_RITUAL_PERFORMED`、`MEMORIAL_PERSISTENT` 拆开。
9. **D / high as preservation rule**：公开纪念页很容易形成 archive bias；密码馆、私信、QQ、短信、墓前讲话和登录后内容往往不可见。

---

## 2. Prehistory boundary：网上纪念不是“死亡第一次被媒介化”

Internet 以前，死亡通知与追思已经可以通过报刊讣告、书信、电话、广播电视以及亲友网络跨距离传播。物理墓地则把很多长期纪念行为绑定在一个具体地点。

海外的 World Wide Cemetery 当前保存的创办者 1995 年原始构想，正是把 Web 与既有印刷、广播、电视死亡通知作比较，再提出“用一个长期网页保存照片、声音和纪念文字”。

Source:
https://cemetery.org/20-years-word-wide-cemetery-classic-design/

Evidence: **C/A boundary**（现站保存并标为 1995 原始文本；本轮未取得独立 1995 replay）。

本仓只保留这个边界：

> **Web 没有发明远程追思；它新增的是一个可被链接、搜索、反复访问、更新和平台托管的 memorial object。**

---

## 3. Historical locators：2001 年已经有一批可定位对象

2001-03-26《北京晚报》经新浪科技保存的同期清单非常有价值，因为它直接给出 host 和当时的功能描述：

```text
网同纪念
http://cn.netor.com

华夏宇宙祭奠园
http://www.7054321.com/

清明网
http://www.qingming.com.cn

地球村网上公墓
http://www.ev991.com

中华清明网
http://www.qingming.net/

英特公墓
http://www.inter-cemetery.com
```

Source:
https://tech.sina.com.cn/i/c/59673.shtml

Evidence grade: **B**（同时代媒体产品清单）  
Confidence: **high** for locator/features, **unknown** for actual historical HTTP/HTML.

报道分别描述：

- 在线建馆（免费/有偿）；
- 在线纪念；
- 生活照片保存；
- 名人园/公民园等分类；
- 网上讣告；
- 论坛/“茶室”；
- 纪念文字与资料查询。

这些 locator 不能自动推出：

- 2001 首页 DOM；
- 真实 Content-Type/charset；
- 是否 frameset/table layout；
- 图片/CDN host；
- 登录机制；
- cookie/session；
- 会员数据库；
- 建馆 form action；
- 付费 endpoint；
- IE/Netscape 浏览器要求。

### 3.1 `cn.netor.com` 得到第二个同时代 locator family

2002-04-04 中新社报道明确写出 `CN.NETOR.COM`，并称记者实际登录、看到用户自建园区和留言、鲜花、烛光、歌曲等。

Source:
https://news.sina.com.cn/s/2002-04-04/0605534052.html

Evidence grade: **B**  
Confidence: **high** for host/function existence。

这使 `cn.netor.com` 不只是 2001 清单里的单点 locator。

---

## 4. 研究单位必须拆开：这里至少有八种不同对象

网上纪念特别容易被一句“这个纪念馆存在”混成一个对象。按照本仓 METHOD，至少要拆：

1. **platform / brand**：如 Netor / 网同纪念；
2. **site / host**：如 `cn.netor.com`；
3. **memorial account / hall**：某一个逝者纪念馆；
4. **page / URL**：首页、相册、文选、年谱、留言、祭奠页；
5. **deceased identity record**：平台数据库里关于逝者的姓名、生卒、照片等；
6. **visitor identity/session**：谁能看、谁能留言、是否需要登录；
7. **transaction**：建馆费、维护费、虚拟祭品、支付；
8. **capture / artifact**：Wayback、搜索引擎、媒体截图今天还能留下的版本。

另有一个 Web 之外但和事务直接相关的对象：

9. **physical grave / ashes / ritual location**。

任何研究都不能把 1—9 自动视为同步状态。

---

## 5. State machine A：纪念馆“建成”之前到底发生了什么

最低模型：

```text
USER_DISCOVERS_SERVICE
    ↓
CREATE_FORM_VISIBLE
    ↓
CREATOR_IDENTIFIED? / ANONYMOUS?
    ↓
DECEASED_DATA_ENTERED
    ↓
DEATH_FACT_VERIFIED?
    ↓
KIN_AUTHORITY_VERIFIED?
    ↓
PHOTO / BIO / DATES UPLOADED
    ↓
FREE_OR_PAID_PLAN_SELECTED
    ↓
PAYMENT_REQUIRED?
    ↓
MEMORIAL_RECORD_CREATED
    ↓
PUBLIC / PRIVATE / PASSWORD STATE
    ↓
SHAREABLE_URL_CREATED
```

必须固定以下非等价关系：

```text
FORM_SUBMITTED
!= MEMORIAL_CREATED

MEMORIAL_CREATED
!= DEATH_VERIFIED

DEATH_VERIFIED
!= CREATOR_IS_KIN

CREATOR_IS_KIN
!= ALL_FAMILY_CONSENTS

PAGE_PUBLIC
!= USER_INTENDED_PERMANENT_PUBLICITY
```

2022—2025 出现“活人被建立网上纪念馆”的法院/媒体案例，已经作为 afterlife 直接证明 `MEMORIAL_CREATED != DEATH_VERIFIED` 不是理论问题。本 note 不把 2020s 内容扩成主 scope，但用它验证早期 state model 的必要性。

Afterlife source:
https://www.chinanews.com.cn/sh/2025/04-05/10394959.shtml

---

## 6. State machine B：“献花/点烛/留言”也不是一个布尔值

一个历史截图上出现“献花”按钮，只能证明按钮/链接可见，不能证明事务成功。

至少拆成：

```text
MEMORIAL_PAGE_RENDERED
    ↓
VISITOR_CAN_ACCESS
    ↓
OFFERING_CONTROL_VISIBLE
    ↓
OFFERING_SELECTED
    ↓
LOGIN_REQUIRED?
    ↓
VIRTUAL_CURRENCY / PAYMENT REQUIRED?
    ↓
REQUEST_SUBMITTED
    ↓
SERVER_ACCEPTED
    ↓
DATABASE_RECORD_WRITTEN
    ↓
COUNTER / GUESTBOOK UPDATED
    ↓
OTHER_VISITORS_CAN_RENDER RESULT
```

所以：

- `button visible != feature operational`
- `click != server accepted`
- `payment deducted != offering persisted`
- `guestbook form visible != message stored`
- `counter increased != unique person`
- `virtual flower rendered != physical grave changed`

2008 年《中国青年报》调查甚至直接记录过“网站可见但搜索引擎已坏”的早期免费网墓。这类 `partial service death` 对 old-Web 考古尤其重要。

---

## 7. 2004：同一年同时出现实际家庭使用与低 adoption，禁止单线普及叙事

### 7.1 嘉定普通家庭实际使用

2004-03-30《嘉定报》记录：安亭镇一名普通企业职工为已故父亲在 Netor 福寿园园区建立纪念堂；记者实际打开网页，看到照片、姓名、生辰、简历、“纪念文选”“历史相册”“活动年谱”等栏目，并记录亲友访问和虚拟送歌/鲜花/酒。

Source:
https://mobile.epaper.routeryun.com/index.php/home/article/index/appkey/49/date/2004-03-30/page/34986/aid/212430.html

Evidence grade: **B**  
Confidence: **high** for this individual use case。

Archaeological implication：

一个纪念馆至少可能包含多个资源类型：

```text
HTML shell
portrait image
biographical text
chronology entries
album images
essay pages
music reference / media file
virtual offering records
visit counters
```

未来 capture 即使保存主 HTML，也可能系统性丢掉其中一半。

### 7.2 重庆低 adoption 反例

2004-03-25《重庆晚报》调查：南山龙园 4000 余具骨灰对应的业务中，只有 12 名普通人建立网络纪念馆；江南殡仪馆 2001 年开过此服务却无人响应，后来取消。

Source:
https://news.sohu.com/2004/03/25/99/news219599967.shtml

Evidence grade: **B**  
Confidence: **high** for local reported uptake。

同一报道同时说功能已有献花、点歌、点烛、上香、祭酒、留言、历史相册。

因此：

```text
FEATURE_COMPLETE
!= CULTURALLY_ACCEPTED
!= LOCAL_ADOPTION
```

不要从一个 2004 功能截图写成“2004 中国人开始普遍网上祭扫”。

---

## 8. 2008 是一个特别好的 old-Web 事务切片：网墓已经同时是 memory service、virtual-goods service 和 long-term hosting contract

中国青年报 2008-04-07 的调查提供了一份极强的 contemporaneous transaction contract。

Source:
https://zqb.cyol.com/content/2008-04/07/content_2132646.htm

Evidence grade: **A/B**（同期报刊记者实际观察 + 消费者采访）  
Confidence: **high**.

报道观察到：

- 建馆/维护按年或多年收费；
- 有 5 年、10 年、20 年维护套餐；
- 虚拟祭品使用平台虚拟货币购买；
- 可通过网银、信用卡、电子支付平台、银行汇款支付；
- 一家早期免费网上公墓虽然网页还在，却已有搜索失效、长期不更新等问题；
- 消费者担心网站无法履行几年乃至十几年的服务承诺。

### 8.1 新增状态：`HOSTING_CONTRACT` 与 grief 必须分开

历史页面中的“永久”“长期”“20 年维护”不能被考古者当作数据寿命事实。

至少拆：

```text
USER_PAID
!= CONTRACT_VALIDATED
!= SERVER_AVAILABLE_FOR_TERM
!= DOMAIN_AVAILABLE_FOR_TERM
!= MEDIA_BYTES_PRESERVED
!= LOGIN_CREDENTIALS_RECOVERABLE
!= BUSINESS_ENTITY_SURVIVES
```

### 8.2 早期免费网墓是 rare failure-state evidence

记者在 2008 年看到某 2001 年上线的免费网墓时：

- 首页还能打开；
- 可观察到的追思文章主要停留在 2001；
- 墓室搜索引擎无法使用；
- 版权时间等页面元素已经陈旧。

这类证据非常珍贵，因为它证明：

> **一个 old-Web 服务可以在 HTTP 意义上“活着”，在事务意义上已经死了。**

因此未来 M1 capture 不能只记录 `200 OK`。

建议状态：

```text
DOCUMENT_REACHABLE
SUBRESOURCE_REACHABLE
SEARCH_OPERATIONAL
CREATE_OPERATIONAL
LOGIN_OPERATIONAL
PAYMENT_OPERATIONAL
GUESTBOOK_OPERATIONAL
MEDIA_OPERATIONAL
```

分别检查。

---

## 9. 2008 普通人第一人称：为什么 URL 本身是功能，而不仅是页面地址

2008-04-09《南都周刊》采访 27 岁广州人林良英。一年前妹妹因癌症去世，他付费建立纪念馆，一个直接目的就是让外地同学和朋友也能方便参加纪念；第一个清明节，亲友通过页面献歌、点烛、留言。

Source:
https://news.sina.com.cn/c/2008-04-09/164415322655.shtml

Evidence grade: **B**  
Confidence: **high** for individual experience。

Old-Web implication：

`SHAREABLE URL` 本身就是新的事务原语。

过去：

```text
知道墓地在哪
+ 身体能到达
```

Web 增加：

```text
知道 URL
+ 能上网
+ 页面仍然存在
```

于是一个纪念馆可能被：

- email 发给同学；
- QQ 发送；
- BBS/论坛贴链接；
- 写进个人主页；
- 收藏到浏览器 bookmark；
- 后来通过搜索引擎重新找到。

这些 referrer / sharing path 大多不会被纪念馆本身的 archive capture 保存。

---

## 10. 2013—2015：纪念事务开始从专门“网墓网站”溢出到微信和普通网店

### 10.1 2013：微信也能成为哀悼媒介

央视网 2013 清明专题已经记录“微信派上用场”，被用于缅怀故人、寄托哀思。

Source:
https://news.cntv.cn/dujia/coverstory/qingmingyisu/index.shtml

Evidence grade: **B**（同期媒体观察）  
Confidence: medium-high。

这意味着 old-Web 的 platform genealogy 在这里开始发生变化：

```text
special-purpose memorial website
        ↓
blog / forum / SNS / IM / WeChat
```

逝者纪念不再一定拥有一个独立墓园式 site hierarchy，而可能嵌入普通社交平台。

### 10.2 2015：普通电商/QQ 可以调度现实墓地劳动

2015 年人民网转载的记者调查记录网店代客扫墓：客户在线联系/下单，服务者现实中寻找墓位、清洁、献花、鞠躬并录制视频，再把视频发给客户。

Source:
https://culture.people.com.cn/n/2015/0403/c172318-26795505.html

Evidence grade: **B**  
Confidence: **high** for workflow; **low-medium** for market prevalence。

因此 old-Web archaeology 不能把“网络祭扫”全部归入 virtual offering。

第二条事务状态机是：

```text
REMOTE_CUSTOMER
→ SHOP / QQ / PHONE CONTACT
→ ORDER TERMS
→ GRAVE LOCATION PROVIDED
→ PAYMENT / AGREEMENT
→ WORKER ACCEPTS
→ WORKER PHYSICALLY REACHES CEMETERY
→ GRAVE IDENTIFIED
→ CLEANING / FLOWERS / BOWING
→ PHOTO / VIDEO CAPTURED
→ MEDIA SENT BACK
→ CUSTOMER CONFIRMS
```

关键边界：

```text
ORDER_PLACED
!= GRAVE_FOUND
!= RITUAL_PERFORMED
!= VIDEO_RECEIVED
!= FAMILY_SATISFIED
```

这是一种典型的 **Web-mediated offline labor**，和本仓招聘/家政/农业成交专题可交叉比较。

---

## 11. 一个必须永久保留的 identity gap：纪念页不是死亡证明

本轮主 scope 结束于 2015，但 2022—2025 的 afterlife 已经提供直接反证：某网络祭祀平台由于没有核实逝者身份，让一名仍在世女性被建立纪念馆多年。

Source:
https://www.chinanews.com.cn/sh/2025/04-05/10394959.shtml

这验证了早期站点研究必须保留：

```text
DECEASED_NAME_ENTERED
!= PERSON_MATCHED
!= DEATH_VERIFIED
!= CREATOR_AUTHORIZED
```

如果未来找到 2003 年某普通人网上纪念馆，不得因为页面写着：

```text
姓名 / 生卒年 / 死因 / 照片
```

就自动把全部字段当作经过平台或官方核实的 historical fact。

研究者最多能先写：

> “该 memorial page 在当时这样陈述。”

再寻找独立来源确认。

---

## 12. Persistence state machine：网上纪念最特殊之处，是用户的时间期望可能远长于普通网站

普通论坛帖子消失会造成历史损失；网上纪念馆消失还可能破坏一个家庭持续多年的私人纪念实践。

因此至少增加：

```text
MEMORIAL_CREATED
    ↓
DOMAIN_ACTIVE
    ↓
APP/SITE ACTIVE
    ↓
HTML RECORD RETAINED
    ↓
IMAGES RETAINED
    ↓
AUDIO / VIDEO RETAINED
    ↓
GUESTBOOK RETAINED
    ↓
VIRTUAL OFFERING HISTORY RETAINED
    ↓
CREATOR CAN STILL AUTHENTICATE
    ↓
SUCCESSOR CAN TAKE OVER?
    ↓
EXPORT AVAILABLE?
    ↓
POST-SHUTDOWN RETRIEVABLE?
```

不能写：

- `main page survived -> album survived`
- `thumbnail survived -> original survived`
- `memorial visible -> manager login still works`
- `domain still exists -> old database is continuous`
- `same brand -> same backend`
- `current Netor page -> 2002 page structure unchanged`

当前 Netor 仍可检索到一些早期建立的纪念馆或旧 URL 结构的后代页面，这只能作为 **current afterlife observable evidence**，不能证明中间二十多年没有迁移、重写或数据结构变化。

Current example / afterlife locator:
https://link.netor.net/link/mem_96091.html

---

## 13. Browser / encoding / plugin questions that remain open

本轮还没有 verified historical capture，所以以下全部保持 `unknown`：

### `cn.netor.com`, 2001—2008

- HTTP `Content-Type`；
- GB2312 / GBK / UTF-8；
- 是否 frameset；
- table layout；
- JavaScript browser sniffing；
- IE-only 控件；
- session/cookie；
- memorial ID 和 BoardID 的 server-side route 语义；
- 上传照片 MIME / size 限制；
- 音乐是 `<embed>` / ActiveX / Flash / third-party URL 还是 server asset；
- 相册原图和缩略图 host；
- guestbook pagination；
- 虚拟祭品是即时数据库记录还是预生成 HTML；
- payment callback；
- free / paid memorial 的访问区别；
- password-protected memorial 的实现。

### 其他 2001 locators

同样全部未知：

- `www.7054321.com`
- `www.qingming.com.cn`
- `www.ev991.com`
- `www.qingming.net`
- `www.inter-cemetery.com`

现代站点、域名停放页或域名复用绝不能填补这些 unknown。

---

## 14. Historical capture attempt：M1 本轮仍 NOT ACHIEVED

本轮实际尝试从以下两个历史 locator 向 Internet Archive CDX 查询推进：

```text
cn.netor.com
www.qingming.com.cn
```

当前 Web 工具对直接构造的 CDX 查询 URL 返回安全访问限制；随后以搜索引擎查询 `site:web.archive.org` 的 2002/2004 capture 也没有获得可实际打开并检查的 replay。

因此本轮结论必须写成：

> **未在本轮访问路径中验证到合格 historical capture。**

不能写：

> “Wayback 没保存。”

按照 `docs/METHOD.md`，本轮 M1 状态为：

**NOT ACHIEVED IN THIS SLICE**

已经获得的是 strong historical locators + contemporary transaction descriptions，不是 archive replay。

下一步真正达到 M1 需要至少实际检查：

- capture datetime；
- original URL；
- status / redirect；
- headers / charset；
- DOM / frames；
- image/media subresources；
- form / link action；
- browser/plugin assumptions；
- 至少第二个独立 archive/evidence family。

---

## 15. Preservation bias：网上纪念页面会系统性制造一种“看起来更公开的 grief history”

### 比较容易幸存

- public memorial landing page；
- 逝者姓名、生卒年；
- 公开 biography；
- static HTML；
- guestbook 的一部分；
- 网站 logo、栏目名；
- 付费规则、帮助页；
- 新闻媒体截图；
- 搜索引擎索引过的公开 URL。

### 系统性容易消失

- 密码保护纪念馆；
- 私人账号后台；
- QQ/短信通知；
- 用户是从谁那里拿到 URL；
- 真实墓前讲话；
- 不公开的家庭照片；
- third-party music；
- Flash/ActiveX 动画；
- 支付流水；
- 被删除或未续费纪念馆；
- 用户下载走但没有重新公开的档案；
- 一家人内部关于“网祭算不算”的争论。

所以必须固定：

```text
PUBLIC_WEB_GRIEF
!= TOTAL_GRIEF

ARCHIVED_MEMORIAL
!= REPRESENTATIVE_MEMORIAL
```

尤其不能因为公开纪念馆更好抓，就把“愿意公开写中文纪念页的人”当成全部丧亲者。

---

## 16. Privacy boundary

这个对象比普通旧主页更敏感。

仓库如果未来进入具体 memorial case，应遵守：

1. 不为了“完整复原”批量重新公开普通逝者/家属的私人照片；
2. 已经密码保护的纪念馆不绕过访问限制；
3. 已被删除的普通个人纪念内容，不因为 archive 能访问就大规模镜像；
4. 优先研究页面结构、状态机、URL pattern、公开帮助页和平台事务；
5. 需要举普通个人案例时，只保留支持 claim 的最少身份信息；
6. 不把未经独立确认的“死因”“亲属关系”当作平台外真实事实。

---

## 17. 与 `how-people-lived` 的交叉边界

本仓保留：

- 2001—2015 中文虚拟墓地/网上纪念站点；
- historical locators；
- memorial URL / account / page state；
- HTML、浏览器、charset、media、guestbook、payment、session；
- 站点停滞/关站与 archive gap；
- 专门纪念网站向微信/普通网店迁移的中文旧网形态；
- online order 与 offline proxy ritual 的事务缺口。

`how-people-lived` 负责：

- 亲属为何需要纪念；
- 迁移、上学、工作、海外生活和返乡成本；
- 2005—2012 / 2015—2019 / 2020—2022 / 2023—2026 时间感；
- 家庭是否接受网上纪念；
- 继续关系、数字遗产和死后记忆治理；
- 1995 海外 online cemetery 与长期跨国比较。

---

## 18. 已证实 / 高概率 / 不知道

### 已证实

- 2001 多个中文虚拟墓地 host/name 同时存在；
- `cn.netor.com` 至少在 2001、2002 同期来源中出现；
- 在线建馆、照片、纪念文章、留言、虚拟献花/点烛等功能至少被同期媒体观察/描述；
- 2004 有普通家庭实际使用案例；
- 2004 也有极低 adoption 的地方反例；
- 2008 已形成付费、维护期、虚拟货币/祭品和多种支付方式；
- 2008 已观察到“页面仍在但服务部分失效”的旧站；
- 2013 微信开始被当作纪念媒介之一；
- 2015 普通网店/QQ 可协调代客扫墓现实劳动。

### 高概率但仍需 capture 验证

- Netor 早期纪念馆存在 server-side memorial ID/BoardID 路由；
- 相册、guestbook、祭品、文选可能是不同 endpoint；
- 早期页面很可能针对 IE-era 浏览器环境设计；
- 音乐/动画资源的 preservation rate 很可能低于主 HTML。

以上都不得写成“已证实技术栈”。

### 不知道

- 2001/2002 Netor 首页和个馆页真实 charset/DOM；
- 是否要求特定浏览器或插件；
- memorial 创建时是否有任何死亡/亲属核验；
- 免费馆与付费馆数据库生命周期；
- 纪念馆管理权如何继承；
- 支付后虚拟祭品的真实数据库状态；
- guestbook moderation；
- 旧图片/音乐 host；
- 关站/迁移时是否有 export；
- 各站点真实 unique-user 分母。

---

## 19. Hindsight risks

### 风险一：把 2001 的网站清单写成“网上祭扫已经普及”

禁止。2004 重庆材料直接否定这种写法。

### 风险二：把平台自报访问量当 population adoption

禁止。站点 traffic、祭奠 clicks、纪念馆数量和真实家庭数量不是同一 denominator。

### 风险三：把页面上的逝者资料当官方死亡记录

禁止。afterlife 已经证明可能存在错误/恶意建馆。

### 风险四：把“献花按钮”当完成一次真实事务

禁止。必须验证 backend/state 或只写 UI exists。

### 风险五：把 2020s “云祭扫”体验倒灌回 2000s

禁止。2000s 是 PC Web、网银/汇款、低宽带/家庭接入不均、不同 browser 环境；不能用今天小程序体验补历史界面。

### 风险六：把现代 Netor 页当 2001 原版

禁止。同品牌延续不等于同 DOM/backend。

### 风险七：为追求完整复原重新公开家庭私人 grief

禁止。研究平台结构优先于恢复普通人私密内容。

---

## 20. 下一步最值得做什么

1. 取得 `cn.netor.com` 2001—2004 至少两个 verified capture；
2. 实际检查一个 memorial 首页 + guestbook + 相册子页的 resource survival；
3. 对比 `www.qingming.com.cn` / `www.qingming.net` 是否属于不同主体，避免同名误合并；
4. 搜同时代 Netor 帮助/付款/建馆教程，定位 form 与 payment state；
5. 寻找 2000s 用户教程/论坛帖，恢复创建和管理路径；
6. 调查历史 charset、IE/Flash/音乐嵌入；
7. 找一个已经死亡/停运的虚拟墓地案例，与持续运行 Netor 做 platform mortality 对照；
8. 若进入完整 case，优先使用公共人物/机构园区或取得许可的普通案例，避免隐私复原；
9. 与 `PERSONAL_ONLINE_PHOTO_ALBUM...` companion 比较“普通照片托管”与“纪念照片托管”在永久性期望上的差异。

---

## 21. 这一 slice 对旧网考古的真正新增

这个对象迫使仓库再加一层此前很容易忽略的时间问题：

> **有些网站的用户并不只期待“今年能打开”，而是期待在自己、父母甚至下一代还活着的时候都能继续打开。**

网上墓地看起来只是另一种 old-Web 页面，实际上它把 `HTTP service lifetime` 和 `family memory lifetime` 绑在了一起。

因此一个 2008 消费者问“付了钱以后网页突然没了怎么办”，并不是普通电子商务里的售后抱怨。它已经触及中文旧网保存问题最深的一层：

**如果一个家庭把唯一的一部分纪念材料交给某个站点，那么站点死亡也可能成为第二次记忆丢失。**

这使 online memorial 成为 `old-web-archaeology` 和 `how-people-lived` 特别合适的交叉对象。

本轮获得强 historical locators、事务合同、普通家庭使用/拒绝反例和后续 state validation，但尚无 verified replay，因此不宣称 M1 完成。