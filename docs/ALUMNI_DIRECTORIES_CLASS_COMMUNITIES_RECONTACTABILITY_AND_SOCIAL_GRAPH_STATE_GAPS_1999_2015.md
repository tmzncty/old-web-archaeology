# 1999–2015：校友录、网上班级、旧友重连与社会图谱状态缺口

> 研究对象：约 1999–2015 年中文 Web 中，ChinaRen、学校自建校友网、校内/人人以及仍存的旧式“同学录”页面，怎样把学校/班级/毕业年份做成寻找旧人的索引；一张历史或当前可见页面究竟能证明“找到过谁、联系上谁、关系有没有恢复”的哪一步。

生活史对应研究：

- `tmzncty/how-people-lived/topics/from-address-books-to-searchable-pasts-lost-contact-recontactability-and-relationship-addressability-china-1955-2026.zh-CN.md`

本文严格保持本仓约 1995–2015 中文互联网 scope。纸质通讯录、1970s–1980s 电话/邮政条件、2020s 微信联系人清理，以及美国 Classmates.com / 英国 Friends Reunited，只作为边界/比较，不把本仓改成全球社交网络史。

---

## 0. 去重：这不是“ChinaRen 怀旧史”或一般 SNS 平台史

本仓已经有大量关于：

- BBS / 论坛；
- 个人主页；
- 博客/SNS；
- 电话/邮件；
- 搜索；
- 在线求职；
- 公开身份；

的专题。

本文只研究一个状态问题：

> **当现实中的联系方式已经丢失时，中文 Web 怎样让“过去共同上过一所学校/一个班的人”重新变成可检索、可联系的对象？**

因此研究单位不是“网站有多少用户”，而是一条 **recontact transaction**：

```text
学校/组织被平台收录
→ 班级/年级存在
→ 班级由人创建/认领
→ 用户注册
→ 用户声明学校/班级身份
→ 申请加入班级
→ 审核/批准（若有）
→ profile/通讯录可见
→ 另一用户检索/浏览
→ 找到候选人
→ 发消息/留言/IM
→ 对方真正遇到消息
→ 识别发送者
→ 回应/拒绝/忽略
→ 关系转移到电话/QQ/email/线下
→ 后续是否持续
```

核心硬规则：

```text
school listed ≠ school community active
class exists ≠ cohort correctly modeled
account exists ≠ real alumnus
membership requested ≠ membership approved
approved member ≠ currently active user
profile visible ≠ contact details current
search result ≠ correct person
message sent ≠ delivered/encountered
encountered ≠ replied
replied ≠ relationship restored
platform edge ≠ real social relationship
```

---

## 1. 研究单位必须拆开

旧网“同学录”至少有这些不同层级：

- **platform**：ChinaRen、学校校友网、校内/人人等；
- **school entity**：平台里的学校记录；
- **cohort / class entity**：入学年份、年级、班级；
- **class admin state**：谁创建、谁能审核；
- **membership state**：申请/批准/退出/被移除；
- **profile state**：姓名/昵称/学校/联系方式/个人资料；
- **visibility state**：什么字段对谁可见；
- **search state**：检索条件与候选结果；
- **message state**：留言/站内信/IM 的发送与接收；
- **off-platform state**：是否转去电话、QQ、email、线下；
- **relationship state**：现实关系是否真的重新活跃；
- **archive artifact**：今天保存下来的 HTML、报道、截图、current rendering。

不能把这些层级压成一句：

> “通过校友录找到了同学。”

至少要问：**找到了 profile，还是联系到了本人？**

---

## 2. 1999–2001：ChinaRen 同学录是明确存在的中文 Web 产品，但最早原页仍未验收

2001 年新浪科技在 ChinaRen 创始人离职报道中回溯，陈一舟、周云帆、杨宁于 1999 年创办 ChinaRen，其社区和同学录在大学生群体中已有较高知名度。

Source:
- 新浪科技，2001-03-04：https://tech.sina.com.cn/i/c/56262.shtml

Evidence: **B — 同时代行业报道。**

另有 2006 年对创始团队的采访回顾，称 1999 年团队推出 ChinaRen 校友录。

Source:
- 《京华时报》经新浪，2006-02-27：https://tech.sina.com.cn/i/2006-02-27/0717851652.shtml

Evidence: **C/B — 后来的创始经历回顾。**

### 当前可写的窄结论

```text
1999–2001 期间 ChinaRen 已存在“校友录/同学录”产品。
```

### 当前不能写

```text
1999 年具体某日的首页长什么样
最早 class URL pattern 是什么
最早班级如何创建/审核
最早用户必须填写哪些字段
当时使用什么 charset/cookie/session
```

这些仍需要 verified historical capture。

---

## 3. 2005：同期媒体已经保存“网上班级”进入普通班级日常的行为证据

《解放日报》2005 年报道：

- 复旦大学新闻学院一个硕士班在学生分散到全国实习后，于 ChinaRen 建立网上班级；通知、留言和交流继续在网上进行；
- 武汉大学 1996 级一名毕业生在甘肃工作，称毕业五年来网上同学录帮助全国各地的同学维持联系；
- 报道还观察到 5460、ChinaRen 等平台上大量学校/班级页面。

Source:
- 《解放日报》，2005-03-18，经新浪保存：https://news.sina.com.cn/s/2005-03-18/09105394097s.shtml

Evidence: **B + contemporaneous user quotation。**

平台/班级数量来自页面观察/当时报道口径，不自动当作独立活跃用户数据。

### 这条材料可以证明什么

- 至少部分班级已经把 Web 班级页用于毕业/实习后的持续通知与交流；
- “网上班级”不是纯静态 alumni directory；
- 地理分散以后，班级可能继续拥有一个共享数字地点。

### 不能证明什么

- 所有成员都注册；
- 所有成员都经常登录；
- 留言都被看到；
- 同学关系因为页面而更亲密。

---

## 4. 2005：ChinaRen 与 IM 结合把“找人”推进到即时通信入口，但仍不是结果证据

搜狐同期产品材料介绍搜Q 3.0 与 ChinaRen 校友录结合，UI 中提供“找同学”“找班级”入口；材料还说 ChinaRen 原先部分找同学功能存在手机绑定条件，而搜Q入口调整了该限制。

Source:
- 搜狐，2005-03-01：https://news.sohu.com/20050301/n224481302.shtml

Evidence: **A（participant source）** 对产品自述成立。

这暴露出一个以后考古时必须保存的状态差异：

### `directory-search / IM-reachability gap`

```text
在班级里看到 profile
≠ 该 profile 可直接 IM
≠ IM account 在线
≠ 消息送达
```

并且“手机绑定”本身提示：

```text
account registration
≠ additional verification/binding state
```

未来若取得 2005 原 HTML，需要特别记录：

- 搜索入口是否依赖登录；
- 手机绑定在哪一步检查；
- 搜Q 与 ChinaRen 是否共享 auth/session；
- 搜索结果跳转的是 profile、班级页还是 IM contact object。

目前全部 `unknown`。

---

## 5. 2006–2007：平台自述显示页面技术与关系状态都在加复杂度

2007 年 ChinaRen 的改版材料回顾 2006 年二级产品升级，声称：

- 首页从 table 结构转为 DIV+CSS；
- 大量使用 Ajax；
- 2007 新版增加班级动态；
- 班级相册增容；
- 个人资料可设置隐私；
- 班级/博客等产品互通。

Source:
- ChinaRen/搜狐同期产品稿（当前 Sohu rendering 标注 2007-03-02）：https://www.sohu.com/a/307988831_120136162

Evidence: **A（participant/product source）**。

### 重要限制

同页给出的注册用户、班级数、日访问量属于**平台自报**，本 note 不把它们升级成独立普及率事实。

### 对 M3 的意义

如果以后取得 2005 与 2007 两个历史时点，浏览器环境差异可能非常重要：

```text
pre-Ajax class page
vs
Ajax-enhanced dynamic class state
```

需要检查：

- JS 关闭后能否浏览成员/班级；
- XMLHttpRequest/浏览器兼容；
- charset；
- CSS 布局；
- dynamic URL；
- archive rewrite 是否破坏 Ajax endpoint。

当前没有 verified capture，不能根据产品稿重建 DOM。

---

## 6. 2008 同济校友网：这是目前最清楚的一条“班级 membership state machine”

同济大学校友总会 2008 年给毕业生的公开信明确说明：

1. 登录校友网；
2. 在同学录栏目注册个人信息并查找班级；
3. 班级存在时，提交加入申请；
4. 由班级管理员审核通过；
5. 班级不存在时，先提交班级创建申请，或联系校友总会创建；
6. 班级社区提供班级主页、通讯录、留言、相册、班级管理；
7. 个人应及时更新最新联络方式；
8. 管理员可汇总班级通讯录，再通过 fax/email 提交校友总会。

Source:
- 同济大学校友总会，2008：https://www.tongji.edu.cn/info/1032/1899.htm
- historical locator given by source: `http://www.tongjiren.org/class/`

Evidence: **A — 同时代学校官方操作说明。**

这条材料允许建立一个强状态模型：

```text
school platform exists
→ class lookup
→ class found / not found
→ join request / class-create request
→ admin review
→ membership approved
→ member record visible according to permissions
→ contact data periodically updated
```

### 必须保留的 gap

#### `class-found / cohort-authenticity gap`

班级存在不证明创建者正确，也不证明所有成员真实属于该班。

#### `join-request / approved-membership gap`

请求加入不是已加入。

#### `approved-membership / civil-identity gap`

班级管理员审核是一种社区/学校关系确认，不等同公安实名核验。

#### `contact-record / current-reachability gap`

用户主动“更新最新联络方式”的要求本身证明：资料会过期。

#### `member-visible / contact-visible gap`

成员 profile 存在不意味着每项电话/email 对所有人公开。

---

## 7. 2008：数字同学录与纸通讯录仍然并行，不能写替代史

同年，西南交通大学给 5212 名本科毕业生发放纸质《毕业生纪念册》，其中包含“同学录”和“通讯录”板块。

Source:
- 西南交通大学，2008-06-04：https://lixue.swjtu.edu.cn/info/1032/3592.htm

Evidence: **A — 学校同时代记录。**

因此：

```text
online alumni service exists
≠ paper contact redundancy disappeared
```

旧网考古尤其要避免把平台营销话术写成现实渠道替代。

---

## 8. 2008 校内网：学校/工作单位字段变成找人的检索键

2008 年《IT时报》报道陈一舟演示校内网：用记者的工作单位、毕业院校作为筛选条件，找到其一名大学同班同学；报道同时说平台计划继续推出校友录产品。

Source:
- 《IT时报》，2008-04-07，经中国诚通转载：https://www.cctgroup.com.cn/cctgroup/2008-04/08/article_2025052219401374993.html

Evidence: **B + participant demonstration。**

这个单次 demo 不能证明搜索准确率/全量覆盖。

但它明确证明一种 UI/产品逻辑：

### `biographical-anchor search`

```text
unknown current address
+ known school/employer
→ filtered candidate profiles
```

考古时应把搜索字段本身当作社会技术 artifact：

- 学校；
- 入学年份；
- 班级/院系；
- 工作单位；

不是“普通个人资料”而已，而是**把人生经历变成检索索引**。

---

## 9. 2009 北语：同一个 cohort 同时拥有 QQ 群与 ChinaRen class URL

北京语言大学网络教育学院 2009 年一则活动通知同时公开：

- 一个年级 QQ 群；
- 一个具体 ChinaRen 校友录班级 URL。

Source:
- 北京语言大学网络教育学院，2009-05-11：https://www.eblcu.cn/html/2009/xbbxxzx_0511/3823.html
- historical locator in source: `http://class.chinaren.com/class/index.jsp?ename=nec0903`

Evidence: **A — 同时代学校公开通知。**

这条材料对“平台替代史”很重要：

```text
QQ group
+ ChinaRen class
+ offline event
```

可以同时存在。

所以不能写成：

```text
校友录 → QQ 出现 → 校友录立即消失
```

用户会维护**多通道关系 portfolio**。

---

## 10. 当前仍能打开的新浪“同学录”：是高价值 artifact，也是巨大时间陷阱

当前 URL：
- https://edu.sina.com.cn/y/alumni/

当前 rendering 仍能观察到：

- 团体搜索；
- 学校/班级式栏目；
- 论坛标题；
- 一项“毕业之后主要通过什么方式联系同学”的旧式投票，选项包括写信、电话、email、短信、同学录、聊天工具。

Evidence: **A for current rendering only**。

它非常有历史味道，但必须写死：

```text
current legacy rendering
≠ verified 2005/2008 historical page
```

当前页面能证明：

> 今天这个 URL 返回这样一套 legacy shell。

它不能证明：

- 这些文本何时首次上线；
- 历史投票数据是否完整；
- 后台班级数据库现在是否工作；
- 当前 DOM 与 2005 DOM 是否相同；
- iframe/图片/脚本是否来自后续模板；
- 历史用户当时看到同样布局。

这是一个很适合 M1/M3 的候选案例，但本轮没有冒充已完成。

---

## 11. profile-staleness：看到过去的人，不等于今天还能找到人

海外 Friends Reunited 提供了一个非常适合中文旧网解释的对照。2016 年关闭前，创始人公开说大量十多年前注册用户的联系方式已经过期，因此“看到 profile 却无法得到回应”本身成了产品失败点之一。

Sources:
- Sky News, 2016：https://news.sky.com/story/friends-reunited-to-close-after-17-years-10135649
- The Guardian, 2016：https://www.theguardian.com/technology/2016/jan/18/friends-reunited-website-closes-after-15-years

Evidence: **B + participant statement。**

这不是本仓全球案例，只用于建立解释边界：

### `profile-presence / person-reachability gap`

```text
profile still listed
≠ email current
≠ phone current
≠ user remembers password
≠ user still checks site
≠ user wants contact
```

中文校友录同样必须预设这种 gap，而不能把老 profile 当作“关系仍在线”。

---

## 12. 一套可复用的 class/alumni state model

### 12.1 school/class discovery

```text
site loads
→ school index/search loads
→ target school exists
→ target cohort/class exists
→ correct class selected
```

Possible failures:

- 学校重名；
- 合并/改名；
- 校区混淆；
- 入学年/毕业年混用；
- 班级重复创建；
- 用户只知道旧校名。

### 12.2 membership

```text
account created
→ school/class claimed
→ join request
→ admin encounter
→ approve/reject
→ membership durable
```

Unknowns to capture:

- 审核者资格；
- 是否实名；
- 是否允许自动加入；
- 是否会被移除；
- inactive member 如何表示。

### 12.3 profile/contact visibility

```text
member record exists
→ profile fields stored
→ privacy policy/setting
→ requesting user has permission
→ field rendered
```

Never infer hidden phone/email from public profile absence.

### 12.4 recontact transaction

```text
search/browse
→ candidate found
→ identity judged plausible
→ message composed
→ request accepted by server
→ durable message/message queue
→ recipient logs in / notification arrives
→ message encountered
→ recipient recognizes sender
→ reply/no reply
→ optional off-platform exchange
```

### 12.5 relationship outcome

```text
reply
→ one interaction
≠ durable friendship
≠ reunion
≠ mutual aid
≠ renewed closeness
```

平台层到这里就应该停止替现实关系下结论。

---

## 13. 需要固定的 old-Web inference gaps

### `listed-school / real-school gap`

平台有一个学校条目，不保证名称、历史时期、校区和现实机构完全匹配。

### `class-record / real-cohort gap`

一个班级对象可能重复、误建、没人维护。

### `registered-account / alumnus gap`

注册账号不等于真实校友。

### `claimed-membership / approved-membership gap`

声明属于班级与通过管理员/平台审核必须分开。

### `membership / active-use gap`

账号十年前加入班级，不证明十年后仍登录。

### `profile / contact-field gap`

有 profile 不等于有电话/email。

### `contact-field / current-address gap`

有电话/email 不等于仍属于本人。

### `search-hit / identity-match gap`

同名、昵称、学校信息不全都可能产生误判。

### `message-submit / durable-message gap`

点“发送”与服务端 durable state 不是同一状态。

### `durable-message / recipient-encounter gap`

消息在站内存在不等于对方回来查看。

### `encounter / response gap`

看见不等于回复。

### `response / relationship gap`

一次回应不等于关系恢复。

### `platform-social-graph / lived-social-graph gap`

平台好友/同班成员不等于现实好友。

### `current-rendering / historical-interface gap`

今天还活着的 legacy 页面不能替代历史 memento。

---

## 14. 页面结构本身怎样把人生制度化为索引

校友录特别值得考古，因为它把真实人生分段压进 Web IA：

```text
学校
→ 年级
→ 班级
→ 姓名/昵称
```

这不是中性的文件夹。

它假设：

- 学校经历是长期稳定的身份锚点；
- “哪届/哪个班”足以帮助找回一个人；
- 过去共同机构比当前地址更耐久。

校内/人人进一步把：

```text
school + employer + location + friend graph
```

一起变成个人可搜索属性。

所以 old-Web 页面结构本身已经在告诉我们：

> **平台怎样把一个人的生命历程切成可检索字段。**

---

## 15. browser / encoding / dynamic-state 风险

这一类站点非常不适合只靠截图研究。

### 15.1 动态成员列表

成员数、最后登录、班级动态可能来自数据库/JS，不一定写在原 HTML。

### 15.2 Ajax

2007 ChinaRen 产品稿明确称此前已经大量使用 Ajax。

Wayback 主 HTML 成功，不保证：

- XHR endpoint 有 capture；
- rewritten JS 可运行；
- 同源策略在 replay 环境下仍成立。

### 15.3 charset / 姓名

校友录天然包含大量中文姓名/学校名；历史 charset、字体和输入法可能影响：

- 姓名搜索；
- 学校名匹配；
- profile rendering。

没有 HTTP/header/HTML capture 时，不猜 GB2312/GBK/UTF-8 的精确版本。

### 15.4 cookie/session

搜索、加入班级、查看联系方式、留言可能依赖登录 session。

公开首页 capture 不能证明认证后的状态。

### 15.5 IM handoff

2005 搜Q/ChinaRen 互通涉及两个产品之间的身份/联系人 handoff；没有客户端和网络材料时，不知道：

- 是否 shared login；
- 是否只是 deep link；
- 是否复制联系人；
- 是否即时读取 ChinaRen database。

全部保持 `unknown`。

---

## 16. archive preservation bias：旧网最容易留下“班级壳”，最难留下真正重逢

### 容易保存

- 学校列表；
- 班级主页；
- 产品介绍；
- 公开论坛/留言；
- 平台宣传“找回同学”；
- 班级相册入口；
- 新闻里的重逢案例。

### 难保存/不应公开

- 真实电话；
- email；
- 私信；
- 谁从未登录；
- unread/read state；
- 管理员拒绝原因；
- 账号找回；
- off-platform 电话/QQ；
- 私人重逢后的关系结果。

所以会产生：

### `public-class-shell / private-recontact-state asymmetry`

我们常能证明：

```text
一个班级页面存在
```

却很难证明：

```text
某个失联十年的普通人真的通过它重新建立了稳定关系
```

这不是研究失败，而是系统本身的隐私边界。

---

## 17. survivorship bias：成功重逢的故事比安静的关系衰减更容易进入档案

媒体和平台喜欢保存：

- 找回失散多年同学；
- 大型聚会；
- “精神家园”；
- 平台用户增长。

但普通关系的常态可能只是：

```text
profile 一直在
→ 偶尔看一眼
→ 多年不留言
→ email 过期
→ 没人特别宣布“关系结束”
```

因此旧网页的高可见故事会系统性高估“重连事件”，低估：

- dormant ties；
- unanswered messages；
- stale profiles；
- mutual indifference；
- quietly ended relationships。

---

## 18. 平台死亡与 contact staleness 是同一研究对象的两种失效

关系可寻址性有两层 uptime：

```text
person/contact record remains valid
AND
platform remains alive
```

任一层失败都会造成：

```text
indexed past
≠ executable recontact
```

所以平台消失不是单纯“怀旧网站关站”，而是：

> **一代人的旧关系索引层可能一起失效。**

这与本仓“内容所有权 / URL ownership / 平台死亡”的主线直接相连。

---

## 19. privacy stop condition

本题特别容易越界，因为旧校友页可能残留：

- 普通人真实姓名；
- 学校/班级；
- 电话；
- email；
- 家庭地址；
- 工作单位。

严格规则：

1. 不批量抓取/重新发布普通校友联系方式；
2. 不把历史姓名 + 学校 + 当前职业拼接做人肉重识别；
3. 不尝试登录/找回旧私人账号；
4. 不用泄露数据库补 membership/私信 state；
5. 引用普通人案例只保留支持机制所需最少信息；
6. archived public contact field 仍按个人敏感信息处理，不因“曾公开”而复制到仓库。

---

## 20. 本轮 archive 检查结果：locator 已经很具体，但 M1 仍未完成

### 已确认 historical/current locators

#### ChinaRen

- host historical locator: `class.chinaren.com`
- 2009 school notice provides specific historical class URL:
  - `http://class.chinaren.com/class/index.jsp?ename=nec0903`
- supporting source: https://www.eblcu.cn/html/2009/xbbxxzx_0511/3823.html

#### 同济校友网

- historical class route from 2008 official source:
  - `http://www.tongjiren.org/class/`
- source: https://www.tongji.edu.cn/info/1032/1899.htm

#### 新浪同学录

- current legacy rendering:
  - https://edu.sina.com.cn/y/alumni/

### 本轮没有做到

**没有实际取得并检查一份满足本仓 M1 最低记录要求的 1999–2010 中文校友录 Wayback/WARC transaction capture。**

因此以下全部仍为 `unknown`：

- exact original HTML；
- capture datetime；
- HTTP Content-Type/charset；
- CSS/JS completeness；
- historical cookie/session；
- class creation POST；
- join approval backend；
- search query endpoint；
- private-message persistence；
- phone/email visibility rules；
- 2005→2007 exact DOM diff。

搜索结果、新闻里的 URL、今天仍活的 legacy page 都只是 locator/artifact，**不等于 verified memento**。

---

## 21. 推荐的下一个 M1 切片

优先顺序：

### A. ChinaRen 2005 / 2007 两时点

目标：验证：

- class URL pattern；
- school/class navigation；
- member list；
- pre/post Ajax 页面差异；
- encoding；
- privacy controls；
- missing subresources。

### B. 同济 2008 class route

学校官方流程足够详细，适合把 historical page 与文档状态机逐项对照。

### C. 新浪 legacy 同学录

先把**current rendering**做完整 provenance，然后再找至少两个历史 memento，专门验证：

```text
今天看到的旧页面
到底哪些真是旧结构
哪些是后来模板遗留/重渲染
```

---

## 22. 已证实 / 高概率 / 不知道

### 已证实

1. 1999–2001 ChinaRen 已有明确“同学录/校友录”产品。
2. 2005 年至少部分高校班级在地理分散后使用网上班级维持通知/互动。
3. 2005 ChinaRen/搜Q 产品材料明确存在找同学/找班级入口和绑定状态差异。
4. 2007 平台材料明确宣称 ChinaRen 使用 DIV+CSS、Ajax，并增加班级动态/隐私等能力。
5. 2008 同济校友网正式存在“查班级—申请加入—管理员审核—通讯录/留言/相册—更新联系方式”的流程。
6. 2009 北语 cohort 同时使用 QQ 群和 ChinaRen 班级。
7. 当前新浪仍返回一个 legacy 同学录页面壳层。

### 高概率 / 可合理推断

1. 学校/年级/班级构成比“当前住址”更耐久的生平锚点索引。
2. online class directory 降低一部分毕业/迁移后的偶然失联成本。
3. 资料长期不更新会把“可检索”退化为“只有过期 profile”。
4. 从 class-centric alumni directory 到 person-centric SNS 是重要关系索引模型变化。

### 不知道

1. 最早 ChinaRen 的精确班级 schema。
2. 班级管理员实际怎样核验身份。
3. 消息 delivered/read state 是否存在、怎样实现。
4. 公开/私密联系方式默认策略的历史版本。
5. 多少真实重连是平台造成，而不是电话/QQ/共同朋友本来也能完成。
6. 平台关闭/迁移时，旧关系图究竟保存/导出了多少。

---

## 23. 对 `how-people-lived` 的回写

这组旧网状态缺口改变生活史解释的地方不是“网站很先进”，而是：

```text
过去共同机构
→ 被编码为稳定检索锚点
→ dormant relationship 获得重新寻址机会
```

但最终必须停在：

```text
recontactability ≠ relationship persistence
```

一个班级页可以比班级关系活得久；一个 profile 也可以比它所指向的联系方式活得久。

因此普通人多出来的一种“活法”不是**永远保持所有旧关系**，而是：

> **离开一段人生以后，不一定必须当天决定这段关系是永久结束还是永久维持；它可以先休眠，而未来仍有重新寻找的可能。**

---

## Source ledger

| Source | Date | Grade | Supports | Does not prove |
|---|---:|---|---|---|
| 新浪科技 ChinaRen 创始团队报道 | 2001 | B | ChinaRen/同学录产品存在 | 最早 DOM/用户普及率 |
| 《解放日报》网上班级 | 2005 | B | geographically dispersed class usage | all members active |
| 搜狐搜Q+ChinaRen | 2005 | A participant | find-class/find-person product flow | message outcome |
| ChinaRen 改版稿 | 2007 | A participant | DIV+CSS/Ajax/features claimed | self-reported scale accuracy |
| 同济校友总会 | 2008 | A | class membership/approval/update workflow | backend implementation |
| 西南交大纪念册 | 2008 | A | paper + web coexistence | nationwide practice |
| IT时报校内网演示 | 2008 | B | school/employer filtering | general search accuracy |
| 北语网院通知 | 2009 | A | specific ChinaRen class locator + QQ coexistence | private class contents |
| 新浪同学录 current URL | current | A-current only | current legacy rendering | historical rendering |
| Friends Reunited closure | 2016 | B | comparative profile staleness/platform mortality | China-specific state |

*Initial research note was AI-assisted; uncertain/private states are deliberately left unresolved.*