# ONLINE_RECIPE_FOOD_BLOG_SEARCH_COMMENT_RECIPE_BOX_AND_KITCHEN_EXECUTION_STATE_GAPS_2005_2015

> 中文旧网交叉切片：菜谱网站、美食博客、搜索/收藏/评论与“现实厨房是否真的做成这道菜”的状态缺口。
>
> 主 scope：约 2005—2015 中文互联网。1980s Usenet / 1995 Epicurious 仅作海外前史对照；2018—2025 仅作 earlier-state 的 afterlife 校验，不把本仓扩成全球或移动饮食平台史。
>
> 检索日期：2026-09-08。
>
> life-history companion：`tmzncty/how-people-lived/topics/from-family-taught-cooking-to-searchable-recipes-domestic-skill-portability-and-outsourced-cooking-china-1980-2026.zh-CN.md`

---

## 0. 本切片为什么属于旧网考古

旧网研究很容易把“菜谱页面”当成纯内容页：标题、食材、步骤、图片，似乎能打开就研究完了。

但对普通用户来说，菜谱是一种**事务性知识对象**。页面只在中间：

```text
现实需求（今天要吃什么）
→ 找站点/搜索
→ 找到菜谱
→ 页面/图片/评论加载
→ 用户判断可信/可做
→ 去买或替换食材
→ 在现实厨房执行
→ 成功/失败
→ 可能回站评论、收藏、上传作品
```

所以本切片不把 `recipe page exists` 偷换成 `recipe used`，更不能偷换成 `dish successfully cooked`。

本切片要回答五个旧网问题：

1. 2005—2015 中文 Web 如何把菜谱从编辑内容变成个人博客、搜索库和 UGC；
2. 页面、图片、用户身份、收藏、评论之间有哪些独立状态；
3. 旧浏览器/编码/图片 host/登录状态会怎样影响历史解释；
4. archive 最容易保存“公开成功作品”，却系统性丢失哪些厨房失败和私下求助；
5. 为什么一个今天仍能打开、时间戳写着 2005 的新浪页面，不等于 verified 2005 capture。

---

## 1. 方法合同：先拆 research unit

按 `docs/METHOD.md`，不能把以下对象混成一个“美食网站”：

- **platform**：新浪博客、某菜谱社区；
- **host**：`blog.sina.com.cn`、`eat.sina.com.cn` 等；
- **account/blog**：某位作者的长期个人空间；
- **recipe/article page**：一篇具体做法/随笔；
- **index/search/category page**：用户从“鸡蛋”或“川菜”进入内容的入口；
- **image resource**：成品图、步骤图，可能由独立图片 host 提供；
- **comment/guestbook state**：可能登录后、异步加载或已经迁移；
- **favorite/recipe-box state**：通常账号私有，archive 很难看见；
- **capture**：某 archive 在某 datetime 保存的表示；
- **claim**：研究者关于当时功能/使用/技术的最小陈述。

必须继续区分：

```text
exists
!= available
!= used
!= popular
!= caused
```

以及：

```text
page visible
!= page historically rendered the same way
!= images complete
!= account state intact
!= user actually cooked it
```

---

## 2. 海外前史边界：网络菜谱早于 Web，本仓只把它当比较参照

### 2.1 `alt.gourmand`：电子邮件 + Usenet 的菜谱分发

Google Groups 当前仍提供 `alt.gourmand` 历史消息索引。其中 Brian Reid 的 1989 消息包含对旧说明文档的重发，可见该电子杂志同时通过 electronic mail 与 Usenet 传播，并提供 archive server 获取旧菜谱和文档。

Locator/current archive view:
https://groups.google.com/g/alt.gourmand

Evidence grade: **A-ish archived message**.  
Confidence: **high** for existence of pre-Web networked recipe distribution; Google Groups 现行包装层不应被当成 1989 UI。

RecipeSource 的项目自述称，Jennifer Snider 1993 年从 Usenet 和 Internet mailing lists 收集菜谱，1995 年将约 10,000 条做成 SOAR 可搜索 Web 库。

Source:
https://www.recipesource.com/admin/

Evidence grade: **C official/project retrospective**.

### 2.2 1995 Epicurious：从数据库立即走向论坛、recipe box 与分享

Epicurious 的参与者口述史称，早期站点已有论坛、聊天室、recipe box、email-to-a-friend；Recipe Swap 用户以 `ISO` 等方式向陌生人寻找特定旧配方，地域群体还会发展出线下聚餐。

Source:
https://www.epicurious.com/about/epicurious-oral-history-article

Evidence grade: **C retrospective oral history**.

对本仓的意义：

> “菜谱页面 → 收藏 → 社区 → 离线做饭/见面”并不是中文互联网特有，但中国 2005—2015 的具体平台、编码、博客文化和移动过渡仍须独立取证。

---

## 3. 中文旧网强锚点 A：2005 新浪美食博客 live legacy artifact

### 3.1 可定位对象

当前新浪博客仍提供：

`https://blog.sina.com.cn/s/blog_5919b50e01000079.html`

页面标题为：

`女人如土豆，男人如面条，做饭如做爱：烹饪男女关系论`

当前页面显示发布时间：

`2005-10-24 09:12:09`

作者“胖星儿”在正文中称自己的页面为“菜博”，并引用自己的“土豆PIZZA”料理记录。

Evidence grade: **A-live-legacy / surviving publisher object**.

### 3.2 这条证据可以证明什么

可以窄写：

> 2026-09-08 访问时，新浪博客仍提供一个内容对象，其页面标示 2005-10-24 的发布时间，正文把作者的博客实践描述为“菜博”并指向具体料理记录。

它支持：

- 美食/菜谱内容与个人博客身份发生结合；
- 当时的作者可以把一道菜与个人随笔、两性叙事放在同一内容对象；
- `blog.sina.com.cn/s/blog_...html` 是当前可定位的 surviving URL pattern。

### 3.3 绝不能从这条证据推出什么

不能写：

- “我们验证了 2005 年新浪博客原始页面”；
- “2005 年浏览器看到的就是现在的布局”；
- “当前 URL 从 2005 起从未变化”；
- “当前 HTML/JS/CSS/图片 host 与 2005 相同”；
- “当前页面所有评论/计数都属于 2005 状态”；
- “新浪博客在 2005 已普遍被普通家庭用于学做饭”。

这是本专题最重要的边界：

**current live legacy page != historical capture != historical browser experience**。

---

## 4. 中文旧网强锚点 B：2005 同期媒体确认“互联网 + 报刊 + 电视”共同传播私房菜

2005-12-30 新浪新闻现存一篇《中国新闻周刊》稿件：

https://news.sina.com.cn/o/2005-12-30/09057857051s.shtml

同期报道观察到：部分都市男女把烹饪重新作为爱好，现象呈年轻化和两性更平均趋势，并通过互联网、报刊、电视共享私房菜；稿件把胖星儿的新浪博客作为具体案例。

Evidence grade: **B contemporaneous secondary**.

这条来源与博客正文是两个 evidence family：

- 原平台个人内容对象；
- 同期媒体对该类实践的观察。

可以据此较有信心地写：

> 至迟 2005 年末，中文旧网中已经存在“个人长期发布家常烹饪内容 + 同期媒体把它识别为新兴都市网络文化”的可核验组合。

仍然不能写全国普及率。

---

## 5. 中文旧网强锚点 C：2006 新浪聊天室让博客操作与自我叙述进一步可见

现存新浪页面：

https://bj.sina.com.cn/danone/art/2006-11-01/174923826.shtml

页面正文标注 `http://eat.sina.com.cn`，记录 2006-11-01 的新浪饮食聊天室实录。王小星在访谈中称自己从前一年 10 月开始做新浪美食博客，每天把给爱人做的菜谱放上去，并描述访问量从早期几十到后来上升。

Evidence grade: **B contemporaneous interview/transcript**.

Historical locator:

- `eat.sina.com.cn`（同期页面正文出现）；
- `blog.sina.com.cn`（当前 surviving blog host）。

这至少提示早期平台关系可能包括：

```text
门户饮食频道
↔ 聊天/活动页
↔ 个人博客
↔ 新闻转载
```

但没有 verified capture 之前，不能推断 2006 年导航、iframe、登录 cookie 或跨域行为。

---

## 6. Recipe publication state machine：一篇“菜谱”至少有这些状态

```text
AUTHOR_HAS_RECIPE
→ DRAFT_CREATED
→ PLATFORM_SUBMISSION_ACCEPTED
→ ARTICLE_OBJECT_CREATED
→ PUBLICATION_VISIBLE
→ INDEX/CATEGORY_UPDATED
→ SEARCH_INDEXED
→ IMAGE_RESOURCES_AVAILABLE
→ READER_LOADS_PAGE
→ READER_CAN_INTERPRET
→ READER_MAY_SAVE/FAVORITE/PRINT/COPY
→ READER_MAY_EXECUTE_OFFLINE
→ READER_MAY_RETURN_WITH_COMMENT/PHOTO
```

需要固定的 state gaps：

- `article exists != indexed by platform search`
- `indexed != discoverable by external search engine`
- `HTML loaded != step images loaded`
- `thumbnail loaded != original image loaded`
- `ingredients text visible != full procedure visible`
- `page public != comments public`
- `favorite button visible != favorite persisted`
- `comment submitted != comment approved/visible`
- `recipe saved != recipe ever cooked`
- `recipe cooked != result uploaded`

旧网考古如果只保存最终 HTML，最多只覆盖这条链的一部分。

---

## 7. Kitchen execution state machine：Web 事务的另一半发生在网络外

```text
NEED_MEAL
→ RECIPE_DISCOVERED
→ USER_JUDGES_FEASIBLE
→ INGREDIENTS_ACQUIRED
→ TOOLS/FUEL AVAILABLE
→ PREP_STARTED
→ HEAT/TIME EXECUTED
→ DISH_FINISHED
→ DISH_EATEN
→ OUTCOME_JUDGED
→ OPTIONAL_FEEDBACK_TO_WEB
```

因此：

- `search query success != household meal success`
- `recipe complete != ingredients locally available`
- `ingredient locally available != user can afford it`
- `recipe says oven != renter owns oven`
- `recipe says “适量” != novice knows quantity`
- `photo looks successful != first attempt succeeded`
- `positive comment != representative user outcome`

这类 gap 是 old-Web 与 how-people-lived 最关键的交叉点：

> 网页可以精确保存文字，但真正决定普通人生活的是页面之外的锅、火、钱、时间和技能。

---

## 8. 账号/身份状态：菜谱从匿名文本变成“这个人会做什么”

个人博客与后来的菜谱社区把内容绑到账户：

```text
ACCOUNT_CREATED
→ PROFILE_EXISTS
→ RECIPE/POST_PUBLISHED
→ TAG/CATEGORY_ASSOCIATED
→ FOLLOW/COMMENT RELATION
→ FAVORITE/COLLECTION STATE
→ USER_REPUTATION/IDENTITY ACCUMULATES
```

历史解释中必须区分：

- `author display name != verified offline identity`
- `account exists != account continuously controlled by same person`
- `post author field != original offline inventor of recipe`
- `follower count now != follower count then`
- `current profile metadata != historical account state`

食谱尤其容易发生来源漂移：家庭口传、书本、报刊、论坛转帖和个人改配方可能在一篇博客里重新混合。没有原作者声明/引用链时，不要把平台“作者”自动写成配方发明者。

---

## 9. 2009 同期材料：Web 让做饭身份可见，但不能解决家庭劳动

2009 年《中国青年报》相关报道（搜狐现存页面）记录大学生男性在 QQ 心情写“在家学做家庭煮男”，以及上海 80 后男性在网上晒给妻子做的菜。

Locators:
- https://news.sohu.com/20090828/n266289034.shtml
- https://www.chinanews.com/life/news/2009/11-04/1945652.shtml

Evidence grade: **B contemporaneous media profiles**.

旧网层面能证明的是：

- QQ 状态/个人网络表达可承载“我在学做饭”的身份陈述；
- 菜品照片/晒菜可成为网络自我呈现；
- 同期媒体把这些线上痕迹当人物材料。

不能自动证明：

- QQ 好友真正看见了这条状态；
- 晒出的饭菜反映日常每顿；
- 网络导致男性承担家务。

2010 年关于 80 后家务分工的调查仍显示做饭、洗碗等可产生家庭冲突。

Locator:
https://news.sohu.com/20100810/n274099783.shtml

这正是：

**online visibility of cooking != redistribution of domestic labor**。

---

## 10. 从 desktop Web 到 mobile：2011 的精确历史 UI 仍不能由 2018 回忆代替

2018 年《中国青年报》对“下厨房”创始人王旭升的采访现存于人民网：

http://media.people.com.cn/n1/2018/0227/c40606-29835941.html

他回忆 2011 年与女友都是烹饪新手、在网上找菜谱，随后创办产品；2018 年报道又把 App 描写为年轻人做年夜饭时的“移动教科书”。

Evidence grade:
- **B** for 2018 interviews/observations;
- **C/B boundary** for 2011 retrospective founder narrative.

这条材料**不能**用于宣称：

- 2011 站点的确切首页结构；
- 2011 是否优先 desktop Web / mobile Web / app；
- 当年的 URL pattern；
- 浏览器/系统兼容要求；
- 当年 search/collection/comment 具体状态机。

这些仍需要 2011—2012 capture、同期教程或帮助页。

因此本专题把“mobile co-presence in kitchen”作为 afterlife 解释，而不拿后来的产品成熟状态覆盖早期 Web。

---

## 11. Search state machine：搜索框存在，不等于这个人能找到可做的菜

一个 recipe search 至少有：

```text
QUERY_ENTERED
→ QUERY_NORMALIZED
→ INDEX_MATCHES
→ RESULT_LIST_RENDERED
→ RESULT_CLICKED
→ RECIPE_LOADED
→ USER_FILTERS_FOR_INGREDIENT/TIME/TOOLS
→ EXECUTABLE_CHOICE_FOUND
```

历史页面若只保存搜索首页，不能证明：

- 后端索引仍可用；
- 2008 年索引内容与今天相同；
- 动态 search endpoint 被 archive 保存；
- 中文分词/编码正常；
- POST/GET 参数能被 replay；
- 登录用户与匿名用户结果一致。

这类功能尤其容易出现 **shell survives, service dies**：搜索框还在，后端索引/接口已经不存在。

---

## 12. Image state machine：菜谱网站的“最有用部分”可能比正文更容易丢

对新手来说，步骤图往往承担文字无法表达的判断：

- 面团应该多湿；
- 糖色到什么颜色；
- 菜切多大；
- 成品应该多稠。

但图片可能来自：

- 独立图片域；
- 用户相册服务；
- CDN；
- 动态缩略图；
- 防盗链 endpoint；
- 后来迁移的 object storage。

状态必须拆：

```text
IMG_TAG_SURVIVES
!= IMAGE_URL_RESOLVES
!= THUMBNAIL_SURVIVES
!= ORIGINAL_SURVIVES
!= SAME_BYTES_AS_HISTORICAL
```

所以“菜谱 HTML 被保存”并不自动意味着用户还能按它学习。

---

## 13. Comment / feedback state machine：archive 最容易丢失失败经验

```text
USER_LOGGED_IN
→ COMMENT_FORM_AVAILABLE
→ SUBMISSION_ACCEPTED
→ MODERATION/PERSISTENCE
→ COMMENT_RENDERED
→ AUTHOR/OTHERS SEE IT
→ OPTIONAL REPLY
```

最有历史价值的反馈往往是：

- “我没有这个原料，可以换什么？”
- “为什么我做出来是生的？”
- “家里只有电饭煲能不能做？”
- “一人份应该减多少？”

但这些比公开正文更容易因登录、异步接口、分页、删除和平台迁移消失。

因此 archive survivor bias 可能让后人看到一个**比真实使用更顺利的厨房**：

> 正文和漂亮成品图留下了，失败、追问、作者纠错和私聊没有留下。

---

## 14. “作品/晒菜”也是选择偏差，不是 household adoption census

后来的菜谱社区会鼓励用户上传“跟做作品”。即使在早期博客/论坛，作者也会晒菜。

历史研究必须区分：

```text
RECIPE_VIEW
→ ATTEMPT
→ SUCCESS/FAILURE
→ PHOTO_TAKEN
→ PHOTO_SELECTED
→ PHOTO_UPLOADED
→ PUBLICLY_VISIBLE
```

真正 archive 可见的通常是最后一步。

因此：

**historian-visible cooking != all cooking attempts**。

尤其不能从大量漂亮 UGC 图片推出普通用户“都很会做”。

---

## 15. 2019 / 2020 afterlife 用来验证 earlier-state，而不是扩大仓库 scope

### 15.1 2019：菜谱信息足够以后，瓶颈转向时间与前处理

界面新闻 2019 年报道显示，一部分 95 后消费者偏好半成品、汤料包、净菜和配送；报道直接把“做饭”的定义讨论为可拆分流程。

Source:
https://www.jiemian.com/article/3645981.html

这验证 old-web 的一个后果：

> 当“怎么做”越来越容易取得，信息并不必然继续是最大瓶颈。洗、切、买、等、洗锅等现实步骤会变得更显眼。

### 15.2 2020：App 和亲友视频可以同时成为知识源

《中国青年报》2020-03-12 调查中，72.2% 受访者称使用厨艺 App 学习，50.4% 向亲友远程求助；具体受访者既照图文 App，又通过视频向家人请教。

Source:
https://zqb.cyol.com/html/2020-03/12/nw.D110000zgqnb_20200312_4-08.htm

这反过来说明：

**digital recipe did not replace kin knowledge; it became another layer in the stack**。

本仓只用它来检验早期 Web “外置知识”机制的后续，不把 2020 App 当作 2005 页面证据。

---

## 16. Historical visibility：哪些生活会被保存，哪些会消失

### 更容易留下

- 新闻/门户编辑菜谱；
- 公开博客文章；
- 首页/频道页；
- 流量大的作者；
- 成品照片；
- 平台宣传成功故事；
- 可被搜索引擎索引的公开评论。

### 更容易消失

- 家庭 QQ/短信里问“盐放多少”；
- 朋友电话口述；
- 只登录可见的收藏夹；
- 搜索历史；
- 做失败后没有上传的尝试；
- 已删除的普通用户博客；
- 评论分页/API；
- 用户相册图片；
- 打印出来贴在冰箱上的网页；
- 从网页手抄到纸本后的私人改动。

因此：

**historian-visible recipe culture != ordinary domestic knowledge system**。

最公开、最漂亮、最成功的人，可能被保存得最好；真正大量的日常“问一下家里人”“看完没做”“做坏了不发”则几乎不可见。

---

## 17. Browser / encoding / runtime assumptions：当前仍不知道的技术条件

本轮没有取得可验证的 2005—2011 historical capture，因此以下均保持 unknown：

- 新浪博客/饮食频道具体历史 `Content-Type` / charset；
- 是否 GB2312/GBK/UTF-8 及何时切换；
- 老页面是否依赖 IE-specific JS；
- 图片是否通过独立 album/CDN host；
- 评论是否 iframe / JS / server-side render；
- 收藏/登录 cookie 域；
- 搜索参数是否 GET/POST；
- 是否存在 ActiveX/Flash 上传器；
- 800×600 / 1024×768 等 viewport 对导航/图片的影响。

现代 Chromium 能打开 surviving 新浪内容，只能证明**现代环境得到某种当前呈现**。

不得写成：

`IE6 user in 2005 saw exactly this`。

---

## 18. Archive attempt / M1 status

### 本轮实际做了什么

1. 以当前 surviving URL、`blog.sina.com.cn`、`eat.sina.com.cn`、相关 2005—2006 标题为 locator 搜索；
2. 尝试构造 Internet Archive historical replay URL；
3. 当前检索链未返回可实际打开并检查的 Wayback capture；直接构造的 replay URL 被当前 Web 工具的 URL 安全限制拒绝；
4. 对 Wayback 域名的搜索查询也未得到可验证 capture 结果。

### 正确结论

**M1: NOT ACHIEVED IN THIS SLICE**。

只能写：

> 本轮未验证到一份符合 `docs/METHOD.md` 最低合同的 historical capture。

不能写：

> “Wayback 没保存新浪美食博客/菜谱页面。”

工具访问限制、搜索索引缺失、robots、历史 URL 变体、动态路径都仍是替代解释。

### 如果下一轮拿到 capture，最低记录

```yaml
archive_source:
capture_url:
original_url:
capture_datetime:
accessed_at:
http_status:
content_type:
charset:
redirect_state:
main_document_saved:
image_subresources_saved:
comment_state_observable:
login_required:
browser_assumption:
evidence_grade:
confidence:
```

---

## 19. Claim matrix

| Claim | Evidence | Grade | Confidence | Boundary |
|---|---|---|---|---|
| 2005 有可定位的新浪美食博客内容对象 | 新浪 surviving blog page | A-live-legacy | high | 非 historical capture |
| 2005 同期媒体观察到都市男女通过互联网分享私房菜 | 中国新闻周刊同期稿 | B | high | 无全国普及率 |
| 2006 新浪饮食聊天室采访该博主 | 新浪现存 transcript | B | high | 当前页面不等于 2006 DOM |
| 1980s 海外已有邮件/Usenet 菜谱传播 | Google Groups `alt.gourmand` | A-ish | high | 仅海外比较 |
| 1995 RecipeSource/Epicurious 已有搜索/社区式菜谱系统 | 项目史/口述史 | C | medium-high | 回顾材料 |
| 2011 下厨房源于创始人和伴侣找在线菜谱的需求 | 2018 创始人采访 | C/B boundary | medium-high | 不证明 2011 UI |
| 2019 年用户做饭流程已可大量模块化 | 同期界面报道 | B | medium | 数据源有人群选择偏差 |
| 2020 App 与亲友远程求助并存 | 中青报调查/人物 | B | high | 特殊居家情境 |

---

## 20. 反例与可替代解释

### 反例 A：网站很多，不等于做饭更多

外卖、食堂、餐馆、便利店同样扩张。菜谱信息供给增加可以和家庭烹饪频率下降同时发生。

### 反例 B：博客内容多，不等于普通读者是新手

美食博客可能主要吸引已有兴趣和厨具的人。

### 反例 C：UGC 增加不等于家庭技能更平均

愿意拍照上传的人本身就是高度选择样本。

### 反例 D：移动菜谱出现不等于亲属知识消失

2020 同期材料明确显示 App 与家庭视频求助可以同时存在。

### 反例 E：不会做饭不一定是信息问题

真正限制可能是：

- 合租厨房太差；
- 无冰箱/抽油烟机；
- 工作太晚；
- 食堂更便宜；
- 单人份食材难买；
- 家庭成员愿意做；
- 本人更愿购买服务。

---

## 21. 与 life-history companion 的交叉链接应该怎样使用

old-web 文件只负责：

- 平台/host/page/account；
- 内容和事务状态；
- browser/encoding/runtime；
- archive gap；
- 保存偏差；
- evidence level。

普通生活长时段则放在 how-people-lived：

- 离家/迁移后技能是否可携带；
- 婚姻中的家务分工；
- 2009 独立生活想象；
- 2019 时间拥堵与半成品；
- 2020 应急再学习；
- 2025 meal-prep / 私厨；
- 海外 pre-Web 长史。

这能避免把 old-web scope 无限前移或无限延后。

---

## 22. 下一步最值钱的 old-Web 证据

1. **真正拿到 2005—2007 新浪博客 historical capture**：至少两个时点，检查 HTML、charset、图片 host、评论与导航；
2. 找 2004—2006 独立中文菜谱站/美食论坛的同期帮助页或教程，确认搜索、投稿、收藏、评论路径；
3. 找 2008—2010 用户教程，确认普通人是打印、抄写还是把电脑/手机带进厨房；
4. 找同一菜谱页面 `main HTML survives / step image missing` 的真实 archive 例子；
5. 若有历史站点依赖 Flash/ActiveX 上传照片，单独记录 browser assumption；
6. 建一个最小 recipe evidence fixture，把 `article page / image / comment / account / offline execution` 分开，防止以后研究重新混成“网页存在=生活发生”。

---

## 23. 本轮对 old-Web 解释新增了什么

以前很容易把旧网“生活服务”理解成：论坛聊天、博客写作、SNS 关系、电子商务交易。

菜谱提醒我们，还有一种很重要的 Web 对象：**它的真正终点不在网页里。**

一篇菜谱的服务器请求可以全部成功，用户却在厨房里把菜炒糊；一张今天还在的成品图也可能只是作者几十次做饭里最值得上传的一次。反过来，一个用户可能 2007 年看完网页、抄在纸上，从此做了十几年，却从未评论、收藏或留下任何平台痕迹。

因此旧网考古不能只问“这个页面当时能不能打开”，还必须问：

> **这个页面试图把什么行动送到屏幕外？它成功到哪一步，而历史档案又最多能看见哪一步？**

在菜谱案例里，这个屏幕外的最后一跳，就是一顿真的被做出来、被吃掉、随后几乎不留数字记录的饭。

---

## Research saturation checkpoint

本轮新增 old-Web 状态机制：

- `recipe publication != kitchen execution`；
- `live legacy page != historical capture`；
- `recipe HTML != instructional completeness`；
- `UGC outcome archive != all attempts`；
- `digital recipe != replacement of kin knowledge`；
- `search/index/comment/favorite/image` 各自独立状态。

并取得：

- 2005 新浪美食博客 surviving primary content object；
- 2005/2006 两个独立同期 evidence family；
- pre-Web `alt.gourmand` 海外对照；
- 2018/2020 afterlife 对 earlier mechanism 的校验。

因此本轮属于实质新增，连续“无实质新增”计数仍为 **0 / 3**。不触发 closure。

---

Initial research note prepared with AI assistance under the repository evidence contract; no historical binary assets were copied into the repository.