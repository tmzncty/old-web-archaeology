# ONLINE_DATING_PROFILE_SEARCH_MESSAGE_VERIFICATION_MATCH_AND_OFFLINE_RELATIONSHIP_STATE_GAPS_2003_2015

> Scope: 2003—2015 中文婚恋网站/移动 Web 的平台技术、资料页、搜索、消息、认证、排序、线下转化与 archive state gaps。
>
> 本文件不写全球网络婚恋史，也不把 1980s 海外 BBS/Minitel 纳入本仓主对象。全球前 Web 对照与中国生活史前史见 `tmzncty/how-people-lived` 对应专题。

## 1. 研究问题

中文旧网里，“网上找对象”很容易被后来叙事压缩成一句：

> 注册一个婚恋网站，搜索合适的人，发消息，见面，成功就结婚。

从考古角度看，这其实至少包含二十多个不同对象和状态。一个历史首页、一张用户 profile 或一篇成功故事，都不足以证明完整链路。

本 note 的目标是为 2003—2015 中文婚恋网站建立可复用 state model，并回答：

1. 用户看到的资料页究竟证明什么；
2. 搜索结果中的“匹配”与真实可约会对象之间隔着什么；
3. 认证徽章能证明到什么程度；
4. 站内信、虚拟邮票、付费排名等怎样改变用户可见性与联系状态；
5. 用户何时离开公开 Web 转入电话、QQ、短信/微信与线下；
6. archive 为什么会系统性保存“资料存在”，却丢掉“关系有没有发生”。

## 2. 研究单位

严格按 `docs/METHOD.md`，至少区分：

```text
physical person
legal identity
relationship / marital status
platform
site / host
account
profile ID
profile fields
profile essay
photo asset
verification document
verification state / badge
search query
search result set
ranked result row
profile view
message draft
message send event
moderation state
message-delivery state
message-read entitlement
message-read event
reply
block / report event
off-platform contact handoff
QQ / phone / SMS / later WeChat contact
offline meeting
dating relationship
marriage registration
profile relationship-status update
archive capture
research claim
```

这些对象不得互相替代。

## 3. 最小 state machine

### 3.1 从账号到资料

```text
person exists
→ account registration attempted
→ account created
→ profile created
→ profile fields submitted
→ moderation accepted
→ profile public/searchable
→ profile indexed/ranked
```

永久保留：

- `account created != legal identity verified`
- `account created != one unique physical person`
- `profile created != profile searchable`
- `profile searchable != currently active user`
- `profile field != verified fact`
- `verified one field != whole profile true`
- `photo displayed != current/authorized likeness`
- `relationship-status field != legal/current relationship reality`

### 3.2 从搜索到消息

```text
search form rendered
→ query submitted
→ backend query executed
→ candidate result set produced
→ ranking applied
→ result row rendered
→ profile opened
→ message composed
→ message submitted
→ moderation/filtering
→ message delivered/available
→ read entitlement satisfied
→ recipient actually reads
→ reply
```

永久保留：

- `search form exists != query executable`
- `query executable != historical result set recoverable`
- `result row != user still available/single`
- `rank high != objectively better match`
- `rank high != organically relevant`（可能存在付费排名/高级展示）
- `message sent != moderation passed`
- `moderation passed != recipient can read`
- `read entitlement != actual read`
- `message read != reply`
- `reply != mutual romantic intent`

### 3.3 从站内关系到现实关系

```text
reply
→ repeated communication
→ off-platform contact exchange
→ QQ/phone/SMS/WeChat
→ offline meeting arranged
→ offline meeting occurred
→ dating relationship
→ stable partnership
→ marriage registration
```

永久保留：

- `contact info exchanged != offline meeting`
- `offline meeting arranged != meeting occurred`
- `meeting occurred != dating relationship`
- `dating relationship != stable partnership`
- `partnership != marriage`
- `marriage success story != platform causal effect`
- `profile changed to “in a relationship” != legal marriage`
- `legal marriage != platform relationship-status field updated`

## 4. 2008—2011 的同时代证据：平台不是“一个页面”，而是多种交易状态

### 4.1 2008：三种婚恋平台模式已经明显不同

2008 年《新世纪周刊》同期报道把几种婚恋网站并列比较：

- 百合强调心理/婚恋类型匹配；
- 珍爱强调人工红娘/电话中介；
- 世纪佳缘强调用户自主注册、搜索、发信和约会。

来源：

- 新浪转载《新世纪周刊》，《甜蜜的对抗：婚恋网站的模式之争》，2008-08-19  
  https://news.sina.com.cn/c/2008-08-19/115016140459.shtml

**证据等级：B/T1。**

这提醒我们不能把“婚恋网站”当成单一 technical object。即使两个网站都显示个人资料：

```text
algorithmic compatibility score
!= human matchmaker recommendation
!= user-created search query
```

三者的权威来源、排序逻辑和失败方式不同。

## 5. 2011 SEC F-1：可直接支持的平台状态与收费机制

Jiayuan.com International Ltd. 2011 年 F-1 是本 note 目前最强的 A 级制度/产品证据。

来源：

- https://www.sec.gov/Archives/edgar/data/1511683/000104746911003874/a2203517zf-1.htm

### 5.1 免费注册、资料、浏览与消息并非同一个权限

F-1 明确描述：

- 注册免费；
- 可发布 profile 与图片；
- 可浏览其他用户资料；
- 可保存偏好；
- 可发送初始消息；
- 但要让初始消息“可读”，发送方或接收方需要支付 RMB2 虚拟邮票或拥有相应订阅；
- 第一封读过以后，同一对用户后续站内通信不再按同一方式收费。

因此至少必须拆开：

```text
message compose
!= send
!= recipient entitlement to read
!= actual read
!= subsequent free thread
```

一个 archive 截图里出现“站内信已发送”，不能证明对方当时已经可以打开它。

### 5.2 排序不是自然状态

F-1 还明确列出付费功能：

- improving search ranking；
- priority rankings for sent messages；
- premium display of profile/pictures；
- refined searches；
- last-login visibility；
- profile-viewer visibility。

所以历史研究遇到某日搜索结果页时，必须保留：

> `top result != most compatible / nearest / most popular`。

排序位置可能受商业权重影响。

### 5.3 认证是局部事实，不是整个人“已验证”

F-1 称平台鼓励用户提交年龄、收入、学历等资料证明；提交证明并支付费用后，资料评级提高。平台也限制某些基础字段在未验证情况下向“更好条件”方向修改。

因此：

```text
verification badge
→ proves platform received/accepted some proof under its then-current rules
```

不能自动推出：

```text
legal identity fully verified
marital status verified
income currently accurate
intent sincere
whole profile truthful
```

同时，历史仓库**不应重新公开认证材料原件**。学历证书、身份证明、收入证明属于高隐私对象；研究认证机制时只保留足够支持 claim 的平台规则和 badge 状态。

### 5.4 站内关系设计上就会逃离 Web

F-1 财务说明称，根据公司历史数据，两名用户在站内的平均消息交换约持续 3.5 天；公司据此认为，想继续交往的用户会交换私人联系方式转到站外直接联系。

这只证明公司这样解释其通信数据，但非常适合支持一个结构结论：

> **contact-channel escape 是产品路径本身的一部分。**

因此 crawler 即使完美保存公开站点，也天然很难看到真正关系的后半程。

### 5.5 2010：移动 Web 已经成为桥接层

F-1 记录，自 2010 年 6 月起，部分婚恋服务可经 mobile browser 使用，包括：

- 发送/读取消息；
- 查看/修改 profile；
- 购买部分增值服务。

这意味着 2010—2011 不能简单写成“PC Web → 后来 App”二阶段史。中间至少有 mobile Web / 手机浏览器阶段。

## 6. “验证”无法消灭资料真实性问题

2011 年《每日经济新闻》同期调查婚恋平台诈骗与虚假资料时，世纪佳缘创始人公开表示平台无法保证每一条信息都真实。

来源：

- https://www.nbd.com.cn/articles/2011-06-24/577832.html

**证据等级：B/T1。**

这条证据最适合固定：

> `platform has verification system != every visible profile is verified`。

以及：

> `some field verified != current relationship intent verified`。

## 7. Search schema 本身就是历史材料

婚恋搜索表单应当作为重要页面形态保存，因为它把当时平台认为“可用于筛选伴侣”的特征明确结构化。

未来遇到 M1 capture 时，至少记录：

- 性别/寻找对象类型；
- 年龄区间；
- 地区；
- 学历；
- 收入；
- 身高；
- 婚史/婚姻状态；
- 是否有照片；
- 认证状态；
- 最后登录；
- 排序选项；
- 其他高级筛选；
- 字段默认值；
- 哪些筛选为付费功能。

不要只截“漂亮首页”。

搜索字段能回答一个很有生活史意义的问题：

> **2008/2011 的平台到底把哪些人生条件认为是机器可比较的？**

## 8. Profile page 的证据边界

一张历史 profile 页面可以证明：

- 某 URL/capture 在某时刻展示了某些字段；
- 平台界面如何组织用户自述；
- 某些照片/图标/认证 badge 是否被显示；
- 页面是否提供发信、收藏、查看资料等入口。

它不能单独证明：

- 页面字段真实；
- 页面对应唯一真人；
- 此人当时仍单身；
- 此人当时仍登录；
- 此人看到过某个访问者；
- 此人后来见过任何站内用户；
- 此人后来建立关系或结婚。

隐私上，普通个人历史 profile 应实行研究必要最小化：优先抽象字段、URL pattern 与 interface state，不批量重新公开已经消失的头像、姓名、联系方式和自我介绍全文。

## 9. 2019 之后的生活史材料为什么也能反推旧网 state gap

2019 年《中国青年报》同期采访显示，平台用户常见路径不是“平台→结婚”，而是：

```text
平台搜索/测试
→ 加微信
→ 偶尔聊天
→ 可能长期不见面
```

另一批受访者又同时使用：

- 父母/亲友介绍；
- 单位同事；
- 婚恋平台；
- 公众号/线下活动。

来源：

- https://zqb.cyol.com/html/2019-09/19/nw.D110000zgqnb_20190919_1-08.htm

这不是 2003—2015 old-Web 的直接页面证据，但它提醒我们：**任何旧 profile/database 都不应该被误读成封闭、完整的婚恋市场。** 现实关系长期是多渠道并行的。

## 10. Archive bias 1：profile-page survival / relationship-state loss asymmetry

最容易被 archive 保存的是：

- 首页；
- 注册页；
- 帮助页；
- 搜索表单；
- 公开 profile；
- 平台成功案例；
- 新闻稿。

最容易消失的是：

- 某一天真实搜索结果；
- 私信；
- 消息是否可读；
- 回复；
- QQ/手机号交换；
- 线下见面；
- 关系开始/结束；
- 未成功匹配。

所以 archive 会系统性制造：

> **页面上“人很多”，现实关系过程却异常安静。**

## 11. Archive bias 2：public-profile / private-message inversion

公开 profile 的历史保存价值高，但与“关系是否发生”的因果距离很远。

真正更接近关系形成的证据——私信、电话、QQ/微信——恰恰更私密，也更不应该被恢复/再公开。

因此本仓明确接受：

> **隐私最小化会故意让某些关系史保持不可完全复原。**

这不是研究失败。

## 12. Archive bias 3：search-form survival / ranking-state loss

即使搜索表单完整保存，也不代表能重建当时返回结果。

需要区分：

```text
search-form HTML
query parameters
backend index snapshot
ranking model
paid boost state
user activity state
moderation state
result-set rendering
```

后五项往往完全不在静态 capture 中。

因此：

> `historical search UI recovered != historical search result recoverable`。

## 13. Archive bias 4：verification-badge / underlying-document loss

如果 profile 页面保存了“学历已认证/身份已认证”等 badge，最多能证明：

- 平台在该 capture 中显示了这个认证状态。

不要尝试寻找、恢复或公开背后的私人证件。

真正应研究的是：

- 当时认证规则；
- badge 文案；
- 哪些字段可认证；
- 平台如何说明认证边界；
- 认证状态是否改变排序/可见性。

## 14. Archive bias 5：success-story selection

婚恋网站会主动保存/宣传“牵手成功”“登记结婚”的故事，因为它们既是品牌宣传，又能证明服务价值。

失败路径则通常没有公开页面：

```text
发了十封没人回
→ 加微信后沉默
→ 见一面没继续
→ 半年后注销
```

因此未来任何 success-story collection 都必须标记 selection bias，不能直接估算平台成功率。

## 15. Archive bias 6：database snapshot / living availability gap

一张 profile 页可能在 archive 里永久“活着”，但现实中的人可能早已：

- 结婚；
- 进入其他关系；
- 停止使用；
- 换账号；
- 要求删除；
- 去世。

所以：

> `archived profile still renders != person was available at capture replay time`。

尤其要区分 original historical capture datetime 与今天 replay 的时间。

## 16. 移动端与跨端边界

2010 起已存在 mobile browser 婚恋功能，因此 2003—2015 至少应区分：

- desktop Web；
- mobile Web/WAP-like browser access；
- later native app；
- SMS/phone relay；
- QQ/微信外部通信；
- offline events/VIP matchmaker。

同一账号是否在多端共享：

- session；
- message state；
- profile fields；
- payment entitlement；
- block/report；

不能凭品牌一致默认。

## 17. 浏览器/编码/页面环境：目前不知道什么

在没有合格 historical capture 前，**不得**因为“2000s 中文网站”就默认：

- GB2312 / GBK；
- IE6 only；
- table layout；
- frameset；
- Flash；
- ActiveX；
- 某固定 viewport；
- 某 JS popup/message mechanism。

这些都必须等具体 capture / 同期技术文档支持。

## 18. M1 historical capture 状态

本轮实际检索：

- `jiayuan.com` / 世纪佳缘 2000s historical capture locator；
- `love21cn.com` 早期品牌/域名 locator；
- `baihe.com` 2008 前后 historical capture locator；
- 公开搜索可发现的 Wayback 索引线索。

在本轮可用检索接口里，**没有获得一份已经实际打开并能同时核验以下字段的合格 M1 capture**：

- exact `original_url`；
- `capture_url`；
- `capture_datetime`；
- HTTP/replay 状态；
- charset/content-type；
- DOM/search form/profile structure；
- 图片/脚本等 subresources；
- 第二历史时点。

因此本轮状态严格记录为：

> **M1 verified historical Chinese online-dating profile/search/message capture: NOT ACHIEVED IN THIS SLICE.**

这不等于“Wayback 没保存”，也不等于“当时页面不存在”。只表示本轮没有达到 `docs/METHOD.md` 的 capture 验证门槛。

## 19. 目前可确认 / 高概率 / 不知道

### 已确认

- 2008 同期媒体已经记录多个中国婚恋网站采用明显不同的匹配/中介模式。
- 2011 SEC F-1 可确认 Jiayuan 当时存在 profile、browse/search、站内消息、虚拟邮票可读权限、付费排序/展示、资料证明、移动浏览器入口、线下活动和 VIP 搜索等制度设计。
- 2011 同期调查/采访可确认平台无法保证所有用户资料完全真实。
- 站内消息链设计本身会很快转入私人联系方式。

### 高概率但仍需 capture 验证

- 不同年份 profile/search page 的字段与默认筛选发生过变化；
- 登录、付费状态和 JS/dynamic backend 会显著影响页面可见内容；
- 图片/CDN/动态搜索结果比静态新闻/帮助页更难完整保存。

### 目前不知道

- 2003—2005 早期具体搜索表单的 DOM、charset 与 browser requirement；
- 2008 某一日期实际搜索结果页的排序逻辑与付费 boost 状态；
- 一个历史 profile badge 在没有当时规则文档时到底覆盖了哪些字段；
- 早期 mobile Web 与 desktop Web 的 session/message consistency；
- 普通用户在站内转 QQ/电话后真实关系结果的总体分布。

## 20. 后见之明风险

### 20.1 不要用今天的 App 逻辑倒推旧 Web

2008/2011 的核心机制包括网页搜索、站内信、虚拟邮票、电话/VIP 红娘与 mobile browser，不应被今天“左右滑”式 App 叙事覆盖。

### 20.2 不要把实名/认证写成“真人已验证”

认证对象与认证范围必须逐项说明。

### 20.3 不要把用户量写成活跃单身人口

`registered account` 与 `active account` 在 2011 F-1 中本身就有不同定义；两者都不能直接等同唯一真人或当前可约会人数。

### 20.4 不要把“成功结婚”写成算法成功

一次婚姻结果可能同时受：

- 家庭；
- 住房；
- 城市；
- 工作；
- 线下沟通；
- 用户自己的选择；

影响。平台只提供初始接触或筛选，不能从时间顺序直接推出因果。

## 21. 对 `old-web-archaeology` 平台谱系的意义

婚恋网站是连接“旧论坛/个人主页”与“平台化数据库身份”的好案例，因为它同时表现出：

- 用户依然有个人 profile URL/页面；
- 但页面字段高度平台化；
- 搜索/排名决定可见性；
- 私信受权限/付费/审核控制；
- 身份认证被平台状态化；
- 真实关系很快逃到站外；
- 平台又重新组织线下活动。

它不是简单的“个人主页升级版”，而是：

> **平台把一个人的部分人生条件结构化，然后用数据库查询与消息权限重新组织陌生人之间的可达性。**

## 22. 下一步 M1 任务

优先寻找并实际打开至少两个时间点的：

1. Jiayuan 注册/搜索/公开 profile；
2. Baihe 兼容性/测试结果入口；
3. Zhenai 用户注册与红娘中介页面；
4. 2010 左右 mobile browser 页面；
5. 官方 help / FAQ 中关于认证、消息、注销和 relationship status 的说明。

每个 capture 必须登记：

```yaml
archive_source:
capture_url:
original_url:
capture_datetime:
accessed_at:
http_replay_state:
content_type:
charset:
login_required:
subresource_state:
evidence_grade:
confidence:
```

达到两个历史时点以后，再做页面结构、字段和浏览器环境的真实比较。

## 23. 来源清单

### A 级 / 同时代平台制度证据

- Jiayuan.com International Ltd. Form F-1, filed 2011-04-20  
  https://www.sec.gov/Archives/edgar/data/1511683/000104746911003874/a2203517zf-1.htm

### B/T1 同时代中文媒体

- 《甜蜜的对抗：婚恋网站的模式之争》，《新世纪周刊》/新浪转载，2008-08-19  
  https://news.sina.com.cn/c/2008-08-19/115016140459.shtml
- 《世纪佳缘会员频“受伤” 婚恋网站商业模式监管存空白》，每日经济新闻，2011-06-24  
  https://www.nbd.com.cn/articles/2011-06-24/577832.html

### 用于后续生活史/状态边界校验（超出本仓主时间范围，不作为 2003—2015 页面证据）

- 中国青年报，2019，《78.8%受访单身青年在婚恋交友平台注册过》  
  https://zqb.cyol.com/html/2019-09/19/nw.D110000zgqnb_20190919_1-08.htm
- 中国青年报，2019，《73.0%受访单身青年担心婚恋交友平台泄露用户信息》  
  https://zqb.cyol.com/html/2019-09/19/nw.D110000zgqnb_20190919_4-08.htm

## 24. 结论

中文旧网里的婚恋平台特别适合提醒本仓：

> **最容易保存下来的“人”，其实只是数据库里一张公开资料页。**

这张页面可以有头像、年龄、学历、收入、城市、婚恋状态、认证标记和“给 TA 写信”按钮，看起来比很多普通个人主页更像一个完整的人；但真正的关系恰恰从这里开始迅速消失于 archive：消息有没有被解锁、有没有回复、有没有换 QQ、有没有见面、见面后有没有继续、几年后有没有结婚，绝大多数都不再属于公开网页。

所以 old-Web 考古不能把保存得最完整的对象误当成历史上最重要的对象。**资料页证明某种平台化身份曾被展示；它并不证明那个人当时怎样爱过、拒绝过、犹豫过或最后和谁生活。**
