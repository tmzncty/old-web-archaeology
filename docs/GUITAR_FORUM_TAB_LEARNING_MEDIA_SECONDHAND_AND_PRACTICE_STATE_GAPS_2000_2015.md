# 吉他论坛、曲谱、教学媒体与练琴：从网页学习对象到身体技能的状态缺口（2000—2015）

> Scope：只研究约 2000—2015 年中文 Web 中，吉他网站/论坛怎样表示曲谱、教程、试听、视频、器材、二手、用户等级与线下活动，以及这些网页状态与真实下载、真实练习、技能形成、演出和成交之间的缺口。
>
> 不把本文件扩成全球吉他史、1980s 中国电视教学史或 2015 年后的 App/短视频史。更早前史、相对收入、工作/婚姻/生育造成的练习中断，以及 Usenet/OLGA 海外比较进入 companion：`tmzncty/how-people-lived/topics/guitar-practice-self-teaching-hobby-reentry-and-amateur-musicianship-china-1986-2026.zh-CN.md`。

本题与现有 Hi-Fi / PC DIY old-Web note 相邻，但研究对象不同：**吉他网页最重要的现实 outcome 不是“拥有一件器材”，而是一个人的手是否真的学会了。**

---

## 1. 研究单位：一篇教程不是一次练习，一张谱也不是一首会弹的歌

至少区分：

- platform / portal；
- host / domain；
- board / subforum；
- thread；
- post / reply；
- article / editorial republication；
- user account；
- mutable rank / points / signature；
- tab / score page；
- inline score image；
- attachment；
- audio demo；
- embedded video / external video；
- lesson series；
- download link；
- secondhand listing；
- PM / QQ / phone / email handoff；
- offline lesson / teacher；
- physical instrument；
- actual practice session；
- embodied skill；
- rehearsal / performance；
- current live legacy page；
- historical archive capture。

最小学习状态机：

```text
用户产生学习目标
→ 找到站点/论坛
→ 搜索曲名/技巧/教材
→ 打开教程/帖子
→ 页面中的谱图/音频/视频成功加载
→ 用户理解内容
→ 可能下载/打印/保存
→ 拿起真实乐器
→ 按内容练习
→ 纠错/反馈
→ 重复数日/数周
→ 技能形成
→ 能完整演奏
→ 技能维持 / 衰退 / 中断
```

最小器材状态机：

```text
论坛看评测/询价
→ 找二手 listing / 商家
→ 联系卖家
→ 离站协商
→ 支付/中介/面交
→ 乐器到手
→ 调整/维护
→ 实际练习
→ 继续持有 / 再出售
```

固定边界：

```text
tutorial page exists ≠ user read it
page text survives ≠ score image/audio/video survives
tab downloaded ≠ tab accurate
tab accurate ≠ user can perform it
reply says “学会了” ≠ skill independently verified
video embed exists ≠ video bytes are archived
user rank ≠ playing level
signature gear list ≠ current ownership
classified listing ≠ sale completed
“已出” ≠ payment / receipt / acceptance independently verified
old post timestamp ≠ current page shell belongs to that year
```

---

## 2. 2000—2001：平台自述可以建立候选谱系，但不能替代历史 capture

吉他中国自己的站史页面称网站于 **2000-10-01** 开通，论坛第一版于 **2001-03-27** 开通，并列出一批当时的专题主页和后续论坛活动。

- 当前平台站史：<https://www.guitarschina.com/article/2005/0701/4.html>

证据等级：**B/C-like platform self-history**。

可以窄地支持：

- 平台今天公开宣称这些起点；
- 2005 页面已经在构建自己的历史叙事；
- 可据此寻找 2000/2001 的 original URL / host / Wayback candidate。

不能直接支持：

- 2000 首页 DOM/charset/视觉；
- 2001 论坛软件和数据库 schema；
- 当时用户量；
- 这些 URL 在每个时点都保持相同路径；
- 当前页面中的后来扩充内容在 2005 原页已经存在。

因此这里只把 `www.GuitarsChina.com`、历史专题路径和 `bbs.GuitarsChina.com` 作为 archive investigation locator。

---

## 3. 2005：论坛内容已经被再编辑成教学文章，产生 provenance 分层

2005-07-30 吉他中国教学页《电吉他教学 第一课 如何读谱 以及 课前准备》标注作者为转帖、来源为“吉他中国论坛”，并明确建议初学者记下或打印资料以供随时参考。

- <https://www.guitarschina.com/article/2005/0730/91.html>

证据等级：**A/B（同期平台文章，明确标注来源链）**。

这里至少存在三个不同对象：

```text
更早的原始教材/文章（若有）
→ 论坛中的转帖/讨论
→ 吉他中国文章系统中的编辑再发布
```

因此新增 **republication provenance gap / 再发布来源缺口**：

- 当前文章页存在，不等于原论坛帖仍存在；
- 文章页的图片可能来自另一个 host；
- 编辑可能删节/改格式；
- 原帖回复、纠错和上下文可能全部消失；
- 搜索引擎今天找到“文章”，很容易误认成平台原创或原始发布时间。

后续编目至少应记录：

```yaml
content_origin_claim: forum / repost / original / unknown
editorial_page_date: ...
claimed_original_author: ...
source_thread_url: known / unknown
source_thread_capture: verified / candidate / none-found-in-search
```

---

## 4. 2005 DIY 吉他版：技术、产品展示与交易已经在同一个论坛结构中重叠

2005-05-12 吉他中国公告重新开放 DIY 吉他论坛，并列出讨论范围：DIY 吉他、效果器、音箱、制作技术、产品展示；平台还允许 DIYer 免费展示/交易产品，同时声明商业纠纷由参与者自行承担。

- <https://www.guitarschina.com/news/news/01/20050512/090702.htm>

证据等级：**A（同期平台公告）**。

这说明一个“学习论坛”不只是学习：

```text
电路/制作经验
+ 图片/试听
+ DIYer 身份
+ 产品展示
+ 潜在交易
```

会叠在一个 board 中。

因此用户角色必须分开：

- beginner；
- experienced player；
- teacher；
- moderator；
- DIY maker；
- dealer / commercial participant；
- performer；
- unknown。

不能看到一条“教学/评测”就自动把作者当作无商业关系的普通用户。

---

## 5. 2006：服务器搬迁直接暴露附件是独立保存层

2006-11-22 同期官方公告称论坛从大连搬到北京独立服务器，夜间暂停；公告特别写到此前“失去连接”的附件预计在论坛恢复后恢复。

- <https://www.guitarschina.com/article/2006/1122/1669.html>

2007-03-06 另一次公告又称新闻与论坛服务器搬迁约两天，并明确列出不可访问的：

- `http://bbs.GuitarsChina.com`
- `http://news.GuitarsChina.com`

以及仍正常运行的 shop 和若干兄弟论坛。

- <https://www.guitarschina.com/article/2007/0306/2077.html>

证据等级：**A（同期平台运维公告）**。

这形成一个非常强的 archaeology 机制：**server-migration attachment gap / 服务器迁移附件缺口**。

一条教学帖的存活至少拆成：

```text
thread row in database
→ post body
→ attachment metadata
→ attachment storage path
→ image/audio/video bytes
→ thumbnail
→ permission / login state
→ migrated path mapping
```

即使帖子正文和数据库都迁移成功，附件也可能短期或永久失去连接。

对吉他论坛尤其重要，因为真正用于学习的对象常不是正文，而是：

- 六线谱图片；
- Guitar Pro / MIDI / PDF / 压缩附件；
- 试听 MP3；
- 示范视频；
- DIY 电路图和照片。

因此固定：

**thread survival ≠ learning-object survival。**

---

## 6. 2006：用户目录本身记录了“旧 Web 学习资源发现劳动”

一个当前仍在线的 legacy thread 承载 2006-06-06 的帖子，作者人工汇总“中国吉他网站/曲谱网”，并邀请其他用户补充；页面还保留了若干历史站点、论坛和 QQ 群 locator。

- <https://bbs.guitarschina.com/thread-339349-1-1.html>

证据等级：**B：同时代用户内容，当前 legacy renderer；不是已验证 2006 memento**。

它说明搜索引擎存在以后，**finding where to learn / 找到“去哪学”本身仍是劳动**。用户会手工建：

```text
网站目录
→ 论坛目录
→ 曲谱站
→ QQ 群
```

如果今天只有这份目录幸存，而被链接站点全部死亡，就会产生 **directory-without-destinations gap / 目录存活、目的地消失缺口**。

目录可以证明“当时有人指向这些站”，不能证明每个站点当天可访问，也不能证明其内容质量。

---

## 7. 2007—2010：曲谱、视听、教程和线下演出已经形成平台内不同状态

当前吉他中国论坛仍有电吉他曲谱区，今天的列表能看到部分帖子携带 2007、2008 等旧日期；例如当前列表页仍显示 2007 年的曲谱主题，民谣吉他板块的深页仍列出 2008 年的用户弹唱、比赛等主题。

- 当前曲谱版：<https://bbs.guitarschina.com/forum-58-1.html>
- 当前民谣吉他历史列表例：<https://bbs.guitarschina.com/forum.php?fid=2&filter=typeid&mobile=no&mod=forumdisplay&orderby=dateline&page=270&typeid=12>

这些对象只能标为：

**current live forum indexes carrying historical thread timestamps**。

不能写成：

> “这是 2008 年论坛首页。”

因为当前 renderer 可能叠加：

- 2020s 导航；
- 当前版主；
- 当前主题/回复计数；
- 当前分页；
- 当前用户积分；
- 当前推荐/公告；
- 迁移后的附件 URL。

新增 **legacy-render temporal collapse / 遗留渲染时间塌缩**。

---

## 8. 2009 第一人称“攒钱买琴”：网页保存的是未来预算话语，不是实际交易

当前 legacy thread 承载 2009-01-13 的帖子，作者明确标明内容为个人虚构/参考，再用个人经验估算学生兼职多久才能买一把 Gibson Les Paul Standard。

- <https://bbs.guitarschina.com/thread-751524-1-1.html>

对 old-Web 来说，它是很好的 **future-planning discourse artifact / 未来规划话语对象**，却不是：

- 工资统计；
- 真实兼职记录；
- 真实购买订单；
- 真实 Gibson 成交价数据库。

因此固定：

```text
forum calculation
≠ market statistic
≠ enacted plan
≠ completed purchase
```

同时当前页面上的账号等级、积分、注册信息可能在后续年份变化，不能自动当作 2009 时点 snapshot。

---

## 9. 曲谱是旧 Web 特别脆弱的对象：HTML 保存不代表“谱还在”

吉他论坛里的学习对象可能有至少六种表现：

1. 纯文本和弦；
2. ASCII tab；
3. inline score image；
4. JPG/PNG 扫描谱；
5. Guitar Pro / MIDI / PDF / ZIP attachment；
6. 外链曲谱站 / 网盘 / 视频。

对应保存状态至少拆成：

```text
thread HTML preserved?
→ attachment name preserved?
→ attachment ID preserved?
→ bytes archived?
→ login required?
→ original filename/extension preserved?
→ file still parseable?
→ embedded image original or thumbnail?
→ external host captured?
```

新增 **tab/score object survival gap / 曲谱对象存活缺口**。

如果帖子只有“谢谢，好谱”回复，而谱图/附件已经丢失，历史学家甚至不知道大家在感谢哪一版谱。

---

## 10. 音频与视频进一步增加“播放器壳存活、媒体字节消失”的风险

吉他学习越来越依赖“看动作”和“听声音”。旧 Web 上媒体可能经过：

- Flash player；
- RealMedia / Windows Media；
- 外链优酷等视频站；
- forum attachment；
- MP3 链接；
- 后来的 HTML5 重嵌入。

一个今天显示视频标题/播放器位置的页面，不足以证明历史媒体对象仍能取得。

新增：

- **player-to-media gap**；
- **embed-to-origin gap**；
- **video-account continuity gap**。

特别是平台迁移后，当前页面可能把旧帖子正文保留，却已经通过现代方式重渲染或完全丢失原播放器。

---

## 11. 用户等级不能当技能等级：论坛身份与身体能力天然分离

当前吉他中国 legacy pages 往往显示“吉他行者 / 吉他英雄 / 吉他之神”等等级、积分、注册时间、总帖数。

这些字段是平台 participation state，不是 performance credential。

固定：

```text
high forum rank
≠ high guitar skill

low post count
≠ beginner

old registration date
≠ continuous practice
```

一个专业演奏者可以很少发帖，一个高积分用户也可能主要参与闲聊、交易或器材讨论。

建议以后抽取：

```yaml
platform_rank:
  observed_on_current_renderer: ...
playing_skill_claim:
  explicit_self_claim: ...
  third_party_evidence: ...
relationship: unknown
```

这可称为 **account-skill identity gap / 账号—技能身份缺口**。

---

## 12. 2014/2015 前的二手论坛：器材退出原因可以被保存，但真实成交常在 Web 之外

当前 legacy thread 承载 2014 年一台小功率吉他音箱的二手 listing。卖家写明工作调动、不想继续折腾，并在回复中引导买家去 QQ 等渠道细聊。

- <https://bbs.guitarschina.com/thread-1714649-1-1.html>

这可以支持：

- 当时公开 listing 会记录价格、所在地、成色、用途叙述、退出原因；
- 在线帖子可把双方导向私聊。

不能支持：

- 设备最后成交；
- 买家就是某一回复者；
- 实际支付价；
- 物流/验收结果。

因此继续沿用并细化：

**public listing / private transaction asymmetry**。

吉他二手尤其可能经历：

```text
forum listing
→ reply
→ QQ / phone
→ courier / face-to-face
→ inspect neck/electronics/frets
→ payment
→ dispute / accept
```

archive 大多只保存最前面的公开壳。

---

## 13. “练会了没有”是本题最大的现实状态盲区

即使网页、谱、视频、附件全部完整，archive 仍然无法直接知道：

- 用户下载后有没有拿起琴；
- 一周练几次；
- 动作是否正确；
- 手指是否疼到退出；
- 节奏是否稳定；
- 三个月后是否还能弹；
- 是否给家人/朋友演奏；
- 是否进了乐队；
- 是否多年后放弃。

因此增加 **instruction-to-practice gap / 教学—练习缺口** 与 **practice-to-skill gap / 练习—技能缺口**。

这个缺口比“页面有没有保存”更根本：Web archaeology 可以恢复学习环境，却不能把学习环境自动解释成学习结果。

---

## 14. 与海外 OLGA 的比较只作为保存机制对照，不改变本仓 scope

1998 年 Washington Post / WIRED 的同期报道显示，美国/全球吉他学习者已经通过 Usenet 与 OLGA 分享 tablature；OLGA 1992 年从 Usenet 社群发展成专门 archive，后来因版权争议关闭主服务、依赖镜像继续存活。

- <https://www.washingtonpost.com/archive/business/1998/07/20/no-music-for-site-readers/935b2669-2849-4c41-9294-59c7c5d31103/>
- <https://www.wired.com/1998/06/they-used-to-write-the-songs/>

这里只提取一个可比较机制：

```text
社区帖子
→ 被整理成专门学习档案
→ 法律/治理变化
→ 主档案关闭
→ 镜像/私人副本成为存续路径
```

它不能证明中文曲谱站经历相同的法律史，也不能把 1990s 美国 Usenet 使用环境写成当时中国普通家庭环境。

对于本仓，海外材料只提醒我们继续检查：中文曲谱/教程消失究竟因为服务器、附件、域名、版权、平台迁移还是用户删除，不要把所有 loss 归为“技术坏了”。

---

## 15. 候选 archive / original locator

本轮可继续追的历史对象：

```text
www.GuitarsChina.com
bbs.GuitarsChina.com
news.GuitarsChina.com
enews.GuitarsChina.com
历史 Guitar China article paths
论坛 list.asp?boardid=79（2005 DIY board locator）
2005 article /article/2005/0730/91.html
2006/2007 server-migration notices
```

还应根据 2006 用户“吉他网站全收集”帖中的历史目录，只抽取必要的 host/path 做 Wayback / Common Crawl 可得性调查，不批量复制普通用户联系方式。

隐私边界：

- 当前 legacy thread 中仍暴露的个人电话/QQ 不复制进仓库；
- 研究二手交易只保留状态机和必要时间/平台信息；
- 不因为 archive 可访问而重新公开普通用户已删除的私人练习视频、联系方式或照片。

---

## 16. M1 状态：本轮未达到 verified historical capture 门槛

本轮已经有：

- 精确历史 host / URL locator；
- 2005—2007 同期官方平台公告；
- 当前仍在线、承载 2006/2009/2014 等时间戳的 legacy pages；
- 平台内部明确的 forum → article provenance；
- 服务器迁移与附件断链的同期直接证据。

但**没有在本轮实际打开并检查一份满足本仓 M1 要求的 2000—2010 吉他中国历史 Wayback/WARC capture**，因此以下仍为 unknown：

- 历史 Content-Type / charset（GB2312/GBK/UTF-8）；
- 2001/2005 论坛软件精确版本；
- 历史 DOM / frames / table layout；
- login / cookie / session 行为；
- attachment upload/download URL schema；
- 历史图片/音频/视频子资源完整性；
- 原始帖子和文章系统之间是否保存跳转/引用字段；
- 当时浏览器要求；
- 历史用户 rank 与今天 current renderer 的字段差异。

所以本轮状态必须写：

> **M1 NOT ACHIEVED IN THIS SLICE. Historical locators and contemporary platform evidence exist; verified historical Web representation remains pending.**

不能写“Wayback 没有”，也不能把今天还能打开的论坛页截图当成 2009 原界面。

---

## 17. 新增状态缺口汇总

本题对 old-Web 方法新增/强化以下可复用 gap：

1. **republication provenance gap** — 论坛转文章后，原帖上下文/纠错可能消失；
2. **server-migration attachment gap** — 数据库正文和附件存储可以分开断裂；
3. **directory-without-destinations gap** — 用户网站目录存活，但目标站点死亡；
4. **legacy-render temporal collapse** — 老帖正文与当前模板/账号状态叠在同一页面；
5. **tab/score object survival gap** — HTML 存活但谱图/GP/PDF/ZIP 不在；
6. **player-to-media gap** — 播放器壳/标题在，但真实音视频字节丢失；
7. **account-skill identity gap** — 论坛等级不是演奏能力；
8. **instruction-to-practice gap** — 教程被访问不等于用户练了；
9. **practice-to-skill gap** — 练习声明不等于可验证技能；
10. **public listing / private transaction asymmetry** — 二手真实成交退到 QQ/电话/面交；
11. **future-plan / enacted-outcome gap** — 论坛预算和目标不等于计划执行。

---

## 18. 已证实 / 高概率 / 不知道

### 已证实

- 2005 吉他中国文章系统存在明确“来源：吉他中国论坛”的教学再发布；
- 2005 平台有独立 DIY board，并把技术交流、图片/试听、产品展示和潜在交易放在同一社区；
- 2006 平台服务器搬迁公告直接提到附件失去连接及恢复；
- 2007 再次存在新闻/论坛 host 分离的服务器迁移；
- 今天平台仍可见承载 2000s/2010s 时间戳的 legacy content。

### 高概率但需 capture 核验

- 2000s 吉他论坛是一套强依赖附件、图片、外链媒体的学习基础设施；
- 服务器/论坛版本迁移可能改变 URL、附件路径和当前渲染；
- 大量真实练习和交易 outcome 在公开 Web 之外发生。

### 不知道

- 2001—2007 各版论坛的真实历史 DOM、编码、软件版本和 attachment schema；
- 当前旧帖中的哪些账户字段来自历史时点、哪些来自后来数据库状态；
- 丢失附件当年是否全部恢复；
- 曲谱版历史附件的保存率；
- 用户下载教程以后真实练习/掌握比例；
- 多少二手 listing 最终成交。

---

## 19. 后见之明风险

- 不把“论坛有大量教程”写成“普通人已经不需要老师”；
- 不把“今天还能访问老帖”写成“旧 Web 保存完好”；
- 不把平台自报会员/帖子数当独立规模统计；
- 不把当前 forum rank、帖子总数、最后登录当历史 snapshot；
- 不把音乐学习成功故事当大多数人的路径；
- 不把 2020s 短视频/App 使用习惯投射回 2005；
- 不把 OLGA 的版权史机械套在中文论坛上。

---

## 20. 下一步最值钱的考古动作

1. 对 `bbs.GuitarsChina.com` 2001/2005/2008 做少量、可复核 Wayback/CDX 调查，优先找 board index + thread + attachment 三件套。
2. 检查 2005 `list.asp?boardid=79` 的 forum software、charset、分页和附件 pattern。
3. 对 `/article/2005/0730/91.html` 找历史 capture，比较 current article renderer 与历史正文/图片路径。
4. 从 2006 服务器搬迁前后各取一个相同 thread locator，检验 host/path/attachment 是否变化。
5. 找一个有曲谱图片或 Guitar Pro 附件的 2007—2010 thread，专门做 `thread HTML vs learning object` 保存率案例。
6. 若只取得 current legacy page，不升级为 M1；把 current render、post timestamp 和 historical capture 三个时点分别记录。

---

本文件为 AI-assisted research note。未复制普通用户联系方式或受版权保护的曲谱/音视频，只保存支持平台结构与状态缺口所需的最小事实、URL 与分析。