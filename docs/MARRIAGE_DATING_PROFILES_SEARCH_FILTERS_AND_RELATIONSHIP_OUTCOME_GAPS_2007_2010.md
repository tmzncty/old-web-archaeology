# 婚恋网站 Profile、搜索筛选与关系结果缺口，2007–2010

> 状态：证据模型 / research note  
> 主研究对象：约 2007–2010 中文婚恋网站的公开 profile、搜索、站内信与线下 handoff  
> 交叉仓：`tmzncty/how-people-lived`  
> 生活史对应：`topics/partner-search-matchmaking-infrastructure-and-marriage-readiness-china-1981-2025.zh-CN.md`

---

## 0. Scope

本文件不写“网络改变中国婚恋”的大叙事。

它只回答一个更窄的旧网考古问题：

> **当 2007–2010 的中文婚恋网站把普通人做成 profile、允许搜索与站内联系时，今天究竟还能证明哪些状态？哪些决定真实关系结果的状态已经天然不可见？**

仓库 scope 保持约 1995–2015 中文互联网。

- 1981 年报纸征婚只作为“陌生人媒介匹配早于 Internet”的前史边界；
- 1980 年代法国 Minitel 等全球比较留给 `how-people-lived`；
- 2019–2025 App、父母在线相亲、“轻相亲”只用于解释后续状态模型，不扩展本文件主时段。

---

## 1. 方法合同

遵守 `docs/METHOD.md`：

```text
platform
≠ site / host
≠ account / profile
≠ page / URL
≠ capture
≠ claim
```

以及：

```text
exists
≠ available
≠ used
≠ popular
≠ caused
```

### 本轮证据强度

本轮拿到的主要是：

- **B：2008 年《中国青年报》对婚恋网站用户搜索操作的同期记录；**
- **B：2009–2011 同期 / 近同期媒体对世纪佳缘产品、收费与数据库商业模式的记录；**
- **C/B：后来对早期平台创办和社会背景的回忆；**
- **D：本文根据这些材料建立的状态机与 archive-gap 模型。**

### 重要限制

本轮**没有可靠恢复 2008 年世纪佳缘搜索结果页或普通用户 profile 的 A 级历史 HTML / WARC capture**。

因此：

- 不声称恢复 2008 年真实页面布局；
- 不声称知道当时具体 DOM、CSS、字符集或 IE 兼容要求；
- 不用现代世纪佳缘页面代替历史页面；
- 不重新公开普通用户已经消失的姓名、联系方式、照片或择偶隐私；
- 不从同期媒体截图推断未显示的 backend 状态。

“缺 A 级 capture”是本轮的明确负结果，不用 reconstruction 补洞。

---

# 第一部分：婚恋网站真正新增的 artifact 是什么

## 2. 2008 同期观察：人被转成可查询字段

2008 年《中国青年报》同期报道记录一名“小周”在世纪佳缘搜索栏输入：

- 年龄；
- 学历；
- 月薪；

随后页面返回几十名符合条件的候选人。他把“自主搜索、随时登录、选择更多”描述为反复使用婚恋网站的原因。

来源：

- 中国青年报 / 中国新闻网，2008-03-03，《逾3成网民网上觅姻缘 网恋将成国人主流婚恋方式》：  
  <https://www.chinanews.com.cn/sh/news/2008/03-03/1179413.shtml>

### Evidence grade

**B：同期媒体对一个真实用户操作和平台界面的观察。**

文章引用的大型在线婚恋调查由行业相关机构执行，不能作为全国人口代表性统计；本文件只用它确认“当时婚恋网站已被当作一个可搜索的专门媒介”，不使用其比例推全民普及。

### 最小 claim

可以写：

> 2008 年同期报道观察到世纪佳缘用户可按年龄、学历、月薪等条件进行候选搜索。

不能写：

> 2008 年中国青年普遍通过数据库条件搜索配偶。

---

## 3. profile 不是“网页上的一个人”，而是一组可变状态

历史婚恋 profile 至少可能包含：

```text
account_id
nickname
age / birth year
sex
location
education
occupation
income band
height
marital status
housing / hukou / family fields（平台不同时期可能不同）
self-description
partner requirements
photo
verification badges
last-active status
membership / VIP status
```

但任何一个字段都需要再问：

- 是用户自填还是系统派生？
- 是否可修改？
- 是否经过平台核验？
- “认证”核验的是身份证本人，还是也核验收入 / 房产 / 婚姻状态？
- 抓取时字段是什么值？
- 历史上此前是否是另一个值？

因此固定：

> **profile field ≠ historical fact about the person**。

最多可以先写：

> 某时刻平台把该字段作为账号的公开 / 半公开表示。

---

# 第二部分：搜索页面比普通文章页面更容易“只剩壳”

## 4. query state machine

婚恋搜索至少有：

```text
user chooses filters
→ request submitted
→ backend interprets filters
→ eligible-account pool calculated
→ ranking / ordering applied
→ result page rendered
→ user opens one profile
```

今天如果只保存搜索表单 HTML，只能证明：

> 某个 capture 时刻存在一套可输入的字段。

它不能证明：

- 2008-03-03 10:15 某次具体查询返回谁；
- 当时有哪些账号处于可搜索状态；
- 结果按什么规则排序；
- 是否有广告 / VIP boost；
- 同一 query 十分钟后结果是否变化。

### 新 gap：search-index snapshot gap

婚恋网站搜索结果依赖持续变化的账号数据库，所以：

> **search UI survived ≠ historical searchable population survived**。

### 新 gap：ranking-state gap

即使我们知道当时 pool，也通常不知道：

- 活跃度；
- 付费权重；
- 推荐算法；
- 站内运营规则；

如何决定了真实排序。

因此：

> **matching feature existed ≠ we can reconstruct who was actually shown to whom**。

---

## 5. candidate-count 是瞬时状态，不是历史人口统计

2008 报道说一次查询返回“几十个”候选。

这个数字不能被延伸成：

- 某地符合条件的真实单身人口；
- 平台真实活跃用户数；
- 可线下约见人数。

原因包括：

- 账号长期不登录；
- 资料未更新；
- 重复账号；
- 已建立关系但未注销；
- 账号只浏览、不回复；
- 资料条件不真实；
- 搜索池被平台规则过滤。

因此固定：

> **returned profile count ≠ active candidate pool ≠ executable relationship pool**。

---

# 第三部分：消息不是一条简单的“联系方式”

## 6. 联系状态机

一个 profile 被打开以后，关系至少还要经过：

```text
profile viewed
→ interest / message attempt
→ message accepted by backend
→ recipient notified
→ recipient can access message
→ message actually read
→ reply attempt
→ mutual conversation
→ off-platform handoff
→ phone / QQ / MSN / SMS contact
→ offline meeting proposed
→ meeting occurs
```

每一步都可能失败。

因此最重要的一组硬边界是：

```text
profile viewed ≠ message sent
message sent ≠ message readable
message readable ≠ message read
message read ≠ reply
reply ≠ identity verified
off-platform contact ≠ meeting
meeting ≠ relationship
relationship ≠ marriage
```

---

## 7. paywall 本身是历史执行状态

2010 年第一财经采访世纪佳缘 CEO 时称，网站自 2008 年开始通过“看信使用电子邮票”等方式向用户收费。

来源：

- 第一财经，2010-08-27，《世纪佳缘CEO龚海燕：婚恋网站熬年头》：  
  <https://www.yicai.com/news/398926.html>

2011 年世纪佳缘 IPO 前后的同期报道进一步解释，在线业务中站内消息阅读与虚拟“邮票”构成收费环节。

来源：

- 北京晨报 / 中新网，2011-04-22，《婚恋网站加入赴美上市大军》：  
  <https://www.chinanews.com.cn/cj/2011/04-22/2990397.shtml>

### Evidence grade

- 2010：**B / 同期 CEO 采访 + 媒体产品描述**；
- 2011：**B / 近同时代 IPO 报道**，用于补状态边界，不把 2011 页面倒投到 2008。

### 新 gap：message-entitlement gap

历史 archive 很容易保存：

- “发消息”按钮；
- 收件箱 URL；
- 价格说明；

却很难保存：

- 某用户当时有几张邮票；
- 某封来信是否被付费解锁；
- 解锁后是否真的读取；
- 是否因价格直接放弃。

因此：

> **message exists in backend ≠ recipient had entitlement to read it**。

这是婚恋网站与普通公开论坛完全不同的一层历史状态。

---

# 第四部分：数据库既是平台资产，也制造新的历史不可见性

## 8. 2009：平台自己明确把数据库视为核心资产

2009 年新浪采访世纪佳缘创始人龚海燕，标题直接为“数据库是世纪佳缘最有价值资产”；文章记录截至当年 3 月中旬平台方面宣称拥有大量注册会员，并讨论婚恋网站商业模式与用户付费。

来源：

- 新浪，2009-03-21，《龚海燕：数据库是世纪佳缘最有价值资产》：  
  <https://finance.sina.cn/usstock/hlwgs/2009-03-21/tech-iavxeafs3522739.d.html>

### Evidence grade

**B / 平台创始人同期访谈。**

可以证明：

- 平台在 2009 年如何描述自身商业模式；
- 用户数据库被管理层视为核心资产。

不能自动证明：

- 所有注册账号真实；
- 所有账号当月活跃；
- 平台宣称的成功率；
- 数据库中每一字段都经核验。

### 考古意义

内容网站的公共资产通常是“文章”。

婚恋网站真正高价值、但最不应该被完整公开保存的历史资产却是：

```text
ordinary people profiles
+ search index
+ messages
+ contact graph
+ activity status
+ payment entitlements
```

所以这类旧网存在一个结构性矛盾：

> **最决定真实用户体验的状态，往往也是最应该因为隐私而缺失的状态。**

---

# 第五部分：身份认证不等于“一个人已经被平台证明为真实人生”

## 9. identity-verification gap

婚恋 profile 的信任至少可拆成：

```text
account reachable
identity document matches account holder
photo belongs to account holder
age correct
single / divorced status current
education true
income true
occupation current
housing claims true
relationship intent sincere
```

即使某平台曾提供身份证等认证，也不能把所有后续字段一次性视作已验证。

因此固定：

> **identity verified ≠ biography verified ≠ intent verified**。

### 反例边界

身份欺骗不是 Internet 发明的。

报纸征婚、线下婚介时期同样存在虚假身份与诈骗，因此不能从“网络扩大陌生人池”跳成“网络创造了婚恋欺诈”。

Web 改变的是：

- 陌生人接触规模；
- profile 的复制速度；
- 认证字段；
- 追踪与投诉机制；
- 平台责任接口。

欺骗行为的历史比较需要另立专题，不在此做猎奇案例堆积。

---

# 第六部分：真正的关系通常在 Web archive 边界外完成

## 10. contact-handoff gap

典型婚恋网站执行链很可能在某一步离开网站：

```text
站内 profile
→ 站内信
→ QQ / MSN / 手机 / SMS
→ 咖啡馆 / 公园 / 学校 / 公司附近见面
```

所以：

> **Web artifact can prove discoverability without proving relationship execution.**

### 为什么 archive 很难补

后半段可能发生在：

- 私人即时通信；
- 电话；
- 短信；
- 私人邮件；
- 线下见面。

这些都不属于应被公开 Web archive 批量恢复的材料。

因此 `contact-handoff gap` 很多时候不是技术失败，而是正常的隐私边界。

---

## 11. relationship-outcome gap

一条真实关系可能有：

```text
first meeting
→ no follow-up
```

也可能：

```text
first meeting
→ repeated dates
→ relationship
→ breakup
→ profile reactivated
```

也可能：

```text
relationship
→ marriage
→ account deletion
```

公共旧网通常最容易看到开头：

- profile；
- 搜索；
- “成功会员”宣传页。

最难看到中间的大量普通失败与模糊结果。

### success-exit bias

如果一个平台的目标是帮助用户形成稳定关系，那么成功用户可能：

- 停止登录；
- 隐藏 profile；
- 注销；
- 删除照片与自述。

这会产生：

> **success-exit bias（成功退出偏差）**。

历史上“还留在平台的账号”可能系统性偏向：

- 尚未匹配；
- 已废弃但未删除；
- 重返搜索；
- 平台测试 / 异常账号。

因此绝不能用残存 profile 反推历史成功率。

---

# 第七部分：profile 是 mutable state，会发生时间塌缩

## 12. profile-state time collapse

假设一个用户：

```text
2007：上海读研，收入“学生”
2008：北京工作
2009：工资档位上升
2010：准备回老家
```

如果平台 profile 永远只保存当前状态，今天能看到的最后 capture 可能只剩：

```text
location = hometown
occupation = current job
```

它会把整个迁移与职业变化压成最后一个值。

因此新增：

### mutable-profile time collapse

> **later profile state must not be retrojected into an earlier dating episode.**

历史 profile 字段必须和 capture datetime 绑定。

不能写：

> “2008 年此人月薪 X、住在 Y”

如果 X / Y 只来自 2010 capture。

---

## 13. “最后登录”尤其危险

现代 live legacy page 或后期 capture 中如果出现：

- 最后登录；
- 在线 / 离线；
- 会员等级；
- 信件数；
- 访问数；

这些通常都是**当前或后期动态状态**。

必须区分：

```text
profile creation time
field edit time
page capture time
current rendering time
```

如果无法区分，就降低 claim。

---

# 第八部分：搜索与推荐的“当前可重放性”极低

## 14. 浏览器 / 编码 / 动态请求未知项

本轮没有取得 A 级 2008 搜索页面资源，因此以下内容全部保持 **unknown**：

- 页面真实 charset 是 GB2312 / GBK / UTF-8 中哪一种；
- 是否依赖特定 IE 行为；
- 是否有 frames / iframe；
- query 是 GET 还是 POST；
- 结果页是否使用 JS / Ajax；
- 图片 host 是否独立；
- 登录 cookie 与搜索 session 如何绑定；
- 免费 / VIP 的结果是否不同。

这正符合 `METHOD.md` stop condition：

> browser / plugin / account state 足以改变解释而未验证时，不继续把 reconstruction 写得更确定。

---

## 15. 不做“模拟 profile”填历史空白

即使根据 2008 报道我们知道字段大致有：

- 年龄；
- 学历；
- 月薪；

也不能人工生成一个看起来像 2008 世纪佳缘的页面，然后称为“复原”。

可以做的 D 级实验只有：

- generic state diagram；
- 用完全虚构数据演示“filter → result”流程；
- 明确标注 reconstruction / mockup；
- 不使用真实普通用户身份。

---

# 第九部分：与其他旧网对象的比较

## 16. 与招聘网站的相似与不同

相似：

```text
profile / resume
→ structured fields
→ search / filter
→ message / contact
→ offline outcome
```

不同：

- 婚恋 profile 涉及更强私人身份与亲密关系信息；
- “成功”常意味着用户离开平台；
- 双方都是搜索者也是被搜索者；
- mutual interest 是必要状态；
- 家长可能作为非账号本人 search agent 参与。

因此不能把婚恋站简单当普通 classified / job board。

---

## 17. 与同学录 / SNS 的相似与不同

同学录主要通过：

```text
共同过去的学校 / 班级 namespace
→ 找回已认识的人
```

婚恋站主要通过：

```text
结构化条件 / 自述
→ 找此前不认识的人
```

所以：

- alumni roster 研究的是 **relationship continuity**；
- dating profile 研究的是 **relationship origination**。

两者 archive gap 也不同。

---

## 18. 与相亲角的结构同构

2019 人民网观察相亲角时，家长把年龄、学历、户口、收入、工作等写在纸卡上。

来源：

- <https://politics.people.com.cn/n1/2019/1024/c429373-31417696.html>

虽然这已经超出本文件主时段，但它说明一个重要比较：

```text
paper card
vs.
web profile
```

可能共享同一种字段化逻辑。

因此不能把“把人量化为条件”全部归因于算法推荐。

---

# 第十部分：历史互联网阶段边界

## 19. 不把 1994 前写成“没有网络”，也不把 1994 写成大众婚恋网起点

中央网信办回顾材料指出：

- 1980 年代中国已有国际联网 / 电子邮件前史；
- 1994-04-20 实现与国际互联网全功能连接；
- 此后公共骨干网与公众接入继续扩散。

来源：

- <https://www.cac.gov.cn/2024-04/20/c_1715291120716362.htm>

因此旧网文件只固定：

```text
pre-1994 research/email connectivity exists
1994 full-function Internet connection
later public/commercial access expands
2000s dating sites become a real public artifact class
```

不能写：

> “1994 中国人开始网上相亲。”

也不能写：

> “1994 前中国没有任何数字通信网络。”

---

# 第十一部分：最小状态机

## 20. profile-to-relationship execution state machine

建议把后续证据录入按以下状态拆分：

```text
S0 account absent / unknown
S1 registration started
S2 account created
S3 profile fields entered
S4 profile published / searchable
S5 profile indexed in a query pool
S6 profile returned in result list
S7 profile opened
S8 message / interest attempted
S9 backend accepted message
S10 recipient had entitlement to access
S11 recipient actually read
S12 reply occurred
S13 repeated conversation
S14 off-platform contact exchanged
S15 offline meeting proposed
S16 offline meeting occurred
S17 repeated meetings / relationship
S18 relationship ended / profile reactivated
S19 marriage / durable partnership claim
S20 profile hidden / deleted / abandoned
```

### 不允许跨级推断

- S6 不得推 S8；
- S9 不得推 S11；
- S12 不得推 S16；
- S16 不得推 S17；
- 平台宣传的 S19 需要明确 provenance；
- S20 不得反推 S19。

---

# 第十二部分：archive gaps 总表

## 21. 本专题新增 gaps

### 21.1 profile-state gap

当前 / 后期 profile 值不能恢复早期值。

### 21.2 searchable-population snapshot gap

不知道某时刻哪些账号真实进入 query pool。

### 21.3 ranking-state gap

不知道结果排序、推荐、付费 boost 等内部规则。

### 21.4 active-user gap

profile 存在不等于用户仍在积极找伴侣。

### 21.5 message-entitlement gap

站内信存在不等于收件人当时能免费 / 付费读取。

### 21.6 message-read gap

backend delivered 不等于本人读过。

### 21.7 off-platform handoff gap

QQ / MSN / 手机等私域接触通常不进入 Web archive。

### 21.8 identity-verification gap

认证 badge 不等于整个人生资料都已核验。

### 21.9 offline-meeting gap

双方聊天不等于现实见面。

### 21.10 relationship-outcome gap

见面以后是否继续、分手、结婚通常不可见。

### 21.11 success-exit bias

成功形成关系的用户反而可能注销 / 隐藏，使成功证据退出平台。

### 21.12 mutable-profile time collapse

后期字段覆盖早期字段，压平真实生命历程。

### 21.13 parent-agent gap

账号 / profile 的本人，不一定是实际执行搜索、筛选和初次沟通的人；父母或婚介人员可能代为操作。

---

# 第十三部分：隐私 stop condition

## 22. 婚恋旧网必须采用更严格的数据最小化

普通用户婚恋 profile 可能包含：

- 姓名 / 昵称；
- 照片；
- 年龄；
- 身高；
- 城市；
- 学历；
- 收入；
- 单位；
- 手机 / QQ / MSN；
- 婚史；
- 家庭与住房；
- 私人择偶偏好。

即使某个旧页面仍能被 archive 找到，也不代表仓库应重新分发。

### 默认规则

研究平台机制时：

- 只记录字段名；
- 用媒体已公开的匿名 / 化名案例；
- 不保存普通用户联系电话；
- 不批量列真实账号 ID；
- 不复制已删除 profile 照片；
- 不尝试破解登录或恢复私人站内信；
- 不购买泄露数据库；
- 不把公开 archive 当作重新暴露个人婚恋史的许可证。

这一点优先于“考古完整度”。

---

# 第十四部分：已证实 / 高概率 / 不知道

## 23. 已证实

- 2008 年同期媒体观察到中文婚恋网站可按年龄、学历、月薪等字段查询候选；
- 2008–2010 世纪佳缘已经存在在线付费 / 看信类商业机制的同期材料；
- 2009 平台创始人明确把用户数据库视作重要资产；
- 线上 profile 与站内联系之后仍存在大量不可见的私域 / 线下执行步骤；
- 旧网方法上必须把 account、profile page、capture、backend state 与 claim 分开。

## 24. 高概率，但本轮不升格为确定事实

- 历史搜索结果受账号活跃、付费与内部排序影响；
- 大量关系建立以后会离开站内通信；
- 成功用户更可能离开平台，从而产生成功退出偏差。

这些需要更多官方产品说明、历史 capture 或用户操作文档补强。

## 25. 不知道

- 2008 世纪佳缘搜索页准确 HTML / CSS / charset / browser requirements；
- 2008 年某个普通账号的历史 profile 字段变更序列；
- 同一 query 在同一天不同时间的结果差异；
- 站内信后台是否保存已删除用户的完整历史状态；
- 搜索 ranking 是否包含付费权重以及具体规则；
- 普通用户从站内信转到 QQ / 手机的比例；
- 一次搜索返回的几十个 profile 中多少当时真实活跃；
- 大量“没有结果”的关系尝试如何留痕。

---

# 第十五部分：下一步

## 26. 最高价值任务

寻找一个**不暴露敏感个人信息**的 2007–2010 原生多时点案例：

```text
T1：一个历史 search / help / tutorial capture
T2：同站关于 profile / message / paywall 的同期产品说明
T3：同期普通用户公开写下“联系 → 转 QQ / 手机 → 见面 / 没见面”的最小片段
T4：数月后的公开 follow-up（若有）
```

最理想的不是“成功结婚故事”，而是能把状态链真正钉住的普通案例。

### 如果找不到

保留负结果：

- 哪些 archive 搜过；
- 哪些 URL pattern 无 capture；
- 哪些页面要求登录；
- 哪些个人信息因隐私不应追；
- 哪些 browser / backend 状态不可恢复。

不要为了完整叙事去补造 profile 或私信。

---

## Sources

1. 中国青年报 / 中国新闻网，2008-03-03，《逾3成网民网上觅姻缘 网恋将成国人主流婚恋方式》  
   <https://www.chinanews.com.cn/sh/news/2008/03-03/1179413.shtml>
2. 新浪，2009-03-21，《龚海燕：数据库是世纪佳缘最有价值资产》  
   <https://finance.sina.cn/usstock/hlwgs/2009-03-21/tech-iavxeafs3522739.d.html>
3. 第一财经，2010-08-27，《世纪佳缘CEO龚海燕：婚恋网站熬年头》  
   <https://www.yicai.com/news/398926.html>
4. 北京晨报 / 中新网，2011-04-22，《婚恋网站加入赴美上市大军》  
   <https://www.chinanews.com.cn/cj/2011/04-22/2990397.shtml>
5. 人民网，2019-10-24，《中国为什么会有“相亲角”？》  
   <https://politics.people.com.cn/n1/2019/1024/c429373-31417696.html>
6. 中央网信办，2024-04-20，《中国全功能接入国际互联网30周年述评》  
   <https://www.cac.gov.cn/2024-04/20/c_1715291120716362.htm>

---

## Cross-repository boundary

婚恋如何进入住房、工作、迁移、户口、父母支持、单身生活可持续性和四阶段未来时间感，由 `how-people-lived` 处理。

本仓只保留：

> **中文旧网怎样把人变成 profile / query / result / message，以及这些 artifact 为什么无法直接告诉我们现实关系到底发生了什么。**