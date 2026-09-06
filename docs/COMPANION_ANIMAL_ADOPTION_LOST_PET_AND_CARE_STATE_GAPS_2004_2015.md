# Companion-animal adoption / lost-pet / care state gaps, 2004–2015

## Scope

本文严格留在本仓约 1995–2015 中文 Web 的 scope 内。它不是中国宠物史，也不研究 1980s 城市养犬制度本身；前互联网生活史、跨国比较、2015 年后的宠物照护与青年生活变化，放在 companion note：

- `tmzncty/how-people-lived/topics/companion-animal-households-care-obligations-and-pet-infrastructure-china-1983-2026.zh-CN.md`

这里问一个更窄的旧网问题：

> 当一只猫或狗在中文旧 Web 上被写成“待领养”“走失”“找到”“求助”时，页面上可见的状态，与动物此刻真实状态、送养者/主人身份、候选领养者、线下交接和最终结果之间到底隔着多少层？

核心原则沿用 `docs/METHOD.md`：

`platform ≠ page ≠ account ≠ capture ≠ claim`

并增加：

`web-visible animal record ≠ current animal state ≠ real-world outcome`。

---

## 1. 为什么宠物页是一个很好的 old-Web state-gap 样本

宠物领养/寻宠页比普通文章更“时态敏感”。一篇 2007 年文章今天仍能正确表示“2007 年有人这样写过”，但它几乎肯定不能继续表示“这只动物现在仍待领养”。动物状态会在很短时间内变化：

- 被领养；
- 被原主人找回；
- 更换寄养地点；
- 生病/康复；
- 年龄增长；
- 送养条件变化；
- 失踪/找到；
- 页面作者失联；
- 页面没有更新但现实结果已经发生。

因此宠物页要求我们把 **content persistence** 与 **subject-state persistence** 强制分开。

---

## 2. 2004 / 2007 新浪宠物送养页：最小“动物资料包”已经出现

今天仍可访问的新浪同源 legacy 页面中：

- 2004-09-03 有一篇为两只幼猫找新家的页面，正文提供年龄、性别、习惯、城市与领养条件；
- 2007-11-29 “新浪宠物 > 领养中心”有一篇网友为满月小狗寻找领养者的页面。

Original-resource locators：

- <https://bj.sina.com.cn/art/2004-09-03/53479.shtml>
- <https://pet.sina.com.cn/2007-11-29/1732155778.shtml>

证据状态：**same-origin live legacy page，内容带历史日期；本轮没有验证对应 Wayback/WARC memento。** 因此可支持“新浪今天仍保存一份自称 2004/2007 的历史内容”，不能支持“已经恢复了 2004/2007 的原始 HTTP/DOM/浏览器体验”。

页面结构显示，一个现实动物已经可以被压成一个远程匹配对象：

```text
poster
→ animal description
→ age / sex / health-or-habit cues
→ city
→ adoption conditions
→ contact endpoint
→ replies / off-page contact
```

这可以称为 **animal objectification for matching / 为匹配而进行的动物对象化**。

### 2.1 必须保留的 state gaps

```text
listing exists
≠ animal still available
≠ poster still reachable
≠ respondent local enough
≠ respondent suitable
≠ meeting happened
≠ transfer happened
≠ stable adoption
```

这些旧页面尤其不能被今天的搜索引擎当作“仍可领养”的活数据。

### 2.2 privacy note

两篇 legacy 页面可能继续暴露当年的个人联络信息。本仓只保留页面 locator 与状态分析，不复制普通人的旧邮箱、电话、QQ 等字段。**页面仍公开 ≠ 研究仓库应再次扩散。**

这构成一个新的 archive/privacy 问题：**legacy-contact privacy debt / 遗留联系方式隐私债务**。

---

## 3. 2009 成都案例：online self-description 与安全领养之间没有自动信任桥

2009-04-13，《天府早报》报道一起通过网络送养猫的事件。同期报道保存的链条大致是：

1. 原照护者已经收留多只猫，继续照顾能力有限；
2. 在网上发帖寻找领养者；
3. 候选者通过 QQ 联系；
4. 候选者在聊天中表现出对绝育、驱虫、猫粮等知识的熟悉；
5. 双方约定试养和回访；
6. 线下见面并完成动物交付；
7. 原照护者在后续网络沟通中发现描述异常；
8. 猫友、论坛版主与搜索共同帮助识别风险；
9. 再次线下行动，动物被追回。

来源：四川在线-天府早报经搜狐保存，2009-04-13，B 级同期媒体：
<https://news.sohu.com/20090413/n263349275.shtml>

本文不重复案件猎奇细节，只保留它对技术史最重要的反证：

```text
profile / chat performance
≠ care competence
≠ benign intent
```

以及：

```text
public adoption post
→ private QQ conversation
→ physical handoff
→ private follow-up
→ cross-forum search
→ offline recovery
```

真正决定安全的环节大量发生在 archive 最难保存的私人/线下状态里。

### 新增 gap：off-platform screening gap

旧论坛可以留下“送养帖”和“有人回复”，但领养筛选往往转向 QQ、电话、见面、看居住环境、试养、回访。于是：

`public thread evidence ≠ full adoption transaction evidence`。

---

## 4. 2010：两万浏览不等于二十个可执行家庭

2010-04-10《新京报》报道，一名志愿者为三只流浪狗寻找家庭。她同时使用网站发帖、社区纸质广告等渠道。报道说，新浪宠物频道相关博客不到一周有两万多点击，但真正联系领养的人不超过 20 个，并且部分联系者身在外地。

来源：新京报经新浪保存，2010-04-10，B：
<https://news.sina.com.cn/o/2010-04-10/011717348865s.shtml>

这是旧网研究里罕见的同页 **funnel evidence / 漏斗证据**：

```text
page exposure: >20,000
→ actual contact: <20
→ geographically executable contact: smaller
→ screened adopter: unknown
→ completed stable adoption: not derivable from page views
```

因此以后看到宠物论坛“浏览量/点击量”时，必须明确：

**attention count is not care capacity**。

同理，评论中的“好可爱”“支持领养”不能计入潜在领养家庭。

---

## 5. 平台谱系候选：论坛、门户领养中心与宠物社区

本轮找到的候选平台/locator 包括：

### 5.1 新浪宠物 / 新浪生活领养内容

2004 与 2007 页面是目前最具体的 original-resource locator。它们体现的是门户频道 + 用户投稿/内容页模式，而不是结构化 shelter database。

### 5.2 四川之家“宠物之家”论坛

2009 同期报道明确提到相关风险帖曾转载自“四川之家‘宠物之家’论坛”。本轮没有取得可验证的原线程 URL/capture，因此只能登记平台名与媒体 locator，不能复原论坛 DOM 或 thread tree。

### 5.3 狗民网 / `goumin.com`

一个仍在线的 2009 蜂鸟摄影论坛帖子留下了外链痕迹，指向 `bbs.goumin.com/viewthread.php...=viewapplylist`，说明当时至少存在一个狗民网论坛/报名型页面 locator family。当前搜索结果把中间 query 参数截断，**不能**据此制造完整 URL。

同期外链页：
<https://bbs.fengniao.com/forum/1250741.html>

当前 WHOIS 显示 `goumin.com` 注册日期为 2006-07-28；WHOIS 只能支持域名注册时间，不证明网站在某日的具体功能：
<https://www.whois.com/whois/goumin.com>

### 5.4 重庆 E 宠网

易宠科技当前公司历史页回顾称“重庆 E 宠网”2008 年在重庆大学上线，2009 年成为城市宠物社区，并随后转向商城。

来源：平台当前 retrospective self-history，C，不是 2008 historical capture：
<https://www.epetbar.com/>

它适合作为后续平台谱系 candidate，不足以单独重建 2008 论坛页面。

---

## 6. 两条应该分别建模的状态机

### 6.1 Adoption / rehoming

```text
animal exists
→ current carer decides to rehome
→ listing authored
→ listing indexed / linked
→ viewer encounters
→ viewer expresses interest
→ off-platform contact
→ location / housing / experience screening
→ identity / intent judgment
→ physical meeting
→ trial / transfer
→ follow-up
→ stable care OR return / rehome again
→ listing closed / left stale
```

### 6.2 Lost / found pet

```text
animal missing
→ owner notices
→ time/location/photo description created
→ notice posted
→ search/index/share
→ viewer sees possible match
→ sighting/contact
→ owner judges identity
→ physical search/retrieval
→ animal recovered OR remains missing
→ notice marked found / removed / left stale
```

这两条链都包含大量“现实结果不回写网页”的可能。

---

## 7. 新增 old-Web state gaps

### 7.1 listing-status staleness gap

`page remains online ≠ listing remains active`。

这是宠物页面比普通新闻更严重的语义老化问题。一个 2007 “找妈妈”的标题在 2026 搜索结果里仍像行动号召，但真实 animal state 早已不可由页面推断。

### 7.2 image-dependency gap

宠物识别高度依赖照片、花色、伤痕、体型等视觉线索。若 archive 只保住 HTML 文字、图片 404，页面可能仍“可读”却已经失去最关键的匹配能力。

因此：

`HTML survived ≠ identification affordance survived`。

后续做 Wayback case 时必须对子资源单独记 capture 状态。

### 7.3 same-animal identity gap

宠物没有天然稳定的 Web identifier。同一动物可能：

- 被不同人用不同名字发帖；
- 年龄/体型随时间变化；
- 照片角度不同；
- 在论坛、博客、QQ 群被重复转发；
- 领养后改名。

因此不能仅凭“同城 + 相似花色 + 名字相近”自动合并历史记录。

### 7.4 public-shell / private-care-state asymmetry

公开 Web 容易留下：

- 标题；
- 动物描述；
- 照片（若幸存）；
- 浏览量；
- 评论；
- “求领养/求寻找”。

最难留下：

- QQ/电话筛选；
- 住址核验；
- 试养；
- 领养协议；
- 线下交付；
- 后续回访；
- 退养；
- 实际找回时间。

因此 archive 会系统性高估“公开匹配对象”，低估“关系真正完成需要的私人劳动”。

### 7.5 audience-geography gap

2010 材料明确显示，一篇页面可以获得巨大跨地域曝光，但动物的实际转移常受同城、运输和后续回访限制。

`global / national visibility ≠ local executability`。

### 7.6 success-story bias

“成功领养”“主人找回”“网友合力救回”更容易被媒体二次报道；无人联系、长期寄养、最终放弃、帖子沉底等负状态更难形成可检索报道。

未来应主动搜：`无人领养 / 求领养半年 / 已送出又退回 / 找不到 / 失联 / 帖子失效 / 图片挂了`。

---

## 8. 浏览器、编码与技术环境：目前知道得很少

对 2004/2007 新浪 legacy page，本轮**没有**验证：

- 历史 HTTP `Content-Type` / charset；
- 当年 DOM 是否与今天返回版本一致；
- 图片是否原始路径或后来迁移；
- 评论是否为 iframe / 独立 host；
- 表单是否存在；
- 登录/cookie 要求；
- 当年 IE/插件依赖；
- 页面是否经历模板批量重写。

对 2009 四川之家、狗民网、E宠网同样没有完整 historical transaction。

现代 Chromium 今天“能打开”只证明当前服务器返回某个可渲染结果。

---

## 9. M1 capture status：本轮仍是明确负结果

本轮针对以下对象进行了历史 locator 搜索：

- `bj.sina.com.cn/art/2004-09-03/53479.shtml`
- `pet.sina.com.cn/2007-11-29/1732155778.shtml`
- `bbs.goumin.com` 2009-era forum family
- `goumin.com` 2008–2009

结果：**没有实际打开并检查到一份满足本仓 M1 最低要求的 2004–2010 中文宠物领养/寻宠 Wayback/WARC memento。** 搜索引擎未给出可直接验证的对应 capture；这不能写成“Wayback 没有”，只能记为“本轮没有验证成功”。

因此以下字段全部继续是 `unknown`：

- historical DOM；
- capture datetime；
- historical charset；
- image subresource completeness；
- original comment endpoint；
- login/session；
- submit / reply transaction；
- post-edit / close status；
- QQ/phone handoff；
- outcome write-back。

达到 M1 前，本文保持 **research note / state-gap model**，不升格为完整平台 case。

---

## 10. 隐私 stop condition

宠物送养/寻宠页很容易包含普通人的旧邮箱、电话、QQ、居住片区，以及可由照片推断的家庭环境。本项目研究页面状态，不需要重新定位这些人。

规则：

1. 不在仓库正文重复普通用户旧联系方式；
2. 不为了确认“后来有没有领养成功”去拼接普通人的跨平台身份；
3. 不把旧 QQ/邮箱拿去搜索今天的实名身份；
4. 只在确有研究必要时保留普通用户名，而且优先用“送养者/发帖者/领养者”抽象化；
5. 动物照片同样不批量镜像，版权与人物/住宅背景隐私不明时只保留 locator。

---

## 11. 这一轮对中文旧网理解的新增

宠物页提醒我们：**旧 Web 保存的是一个时刻的请求，不是一个永久有效的现实状态。**

对于普通文章，页面老旧主要意味着观点和版式过时；对于“求领养/寻宠”页面，页面越长寿，反而越可能与真实世界脱节。于是 old-Web archaeology 需要多一个字段：

`subject_state_at_capture` 与 `subject_state_now/afterward` 必须分开，后者不知道时就写 `unknown`。

这也解释了为什么 Internet 对普通生活的改变不能用页面数量衡量。它确实把一只需要新家的猫、一只走失的狗变成了跨空间可发现的对象；但**真正的生活变化发生在页面之外：有人筛选、有人坐车、有人开门、有人把动物接回家，并在第二天继续喂它。**
