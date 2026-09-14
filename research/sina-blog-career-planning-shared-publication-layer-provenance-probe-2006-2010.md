# 新浪“职业生涯规划”共享出版层：live-legacy provenance probe（2006—2010）

> 类型：artifact/provenance probe，不是 M1 complete case。  
> 范围：中文旧网约 1995—2015；本文只研究新浪博客当前仍存活的一组 2006—2010 页面怎样被正确解释。  
> 交叉：`tmzncty/how-people-lived` 的 2007—2010 同时代未来想象材料。

## 1. 为什么做这个 probe

`how-people-lived` 已经多次使用新浪博客中 2007—2010 的职业生涯规划文本，作为同时代第一人称未来材料。此前研究已经提醒：

- current live page != historical capture；
- displayed date != independently verified capture datetime；
- course assignment != spontaneous diary；
- author identity 只按页面署名，不外推现实身份。

本轮进一步检查页面谱系后发现，一个更基础的 provenance 问题必须显式拆开：

> **正文作者 != 新浪账号发布者。**

同一 `blog_56c92245...` URL 前缀下存在大量不同学生署名的文章，因此这些页面不能再被口语化地叫成“某学生自己的新浪博客”。

这不是新的“平台状态缺口”概念，而是一个可以直接用于现有 HPL 证据的**具体 artifact 身份修正**。

---

## 2. 当前可核验对象

### 2.1 账号/出版层

当前搜索与 live rendering 显示：

- 数字账号 ID：`1456022085`
- 文章 URL 前缀中的标识：`56c92245`
- 当前博客标题：`职业生涯规划`
- 当前 account URL：`http://blog.sina.com.cn/u/1456022085`

一个仍可访问的文章目录页面：

https://blog.sina.com.cn/s/articlelist_1456022085_8_12.html

当前该页显示分类：

`求职策略（简历与面试等）(823)`

并显示 17 页分页。可见页中连续列出大量 `2006-05-24`、`2006-05-25` 的面试、招聘、企业求职相关文章。

### 证据等级

**A-/B+：当前 live-legacy platform representation。**

它直接证明 2026 年仍能从新浪当前服务层观察到这一账号、分类、文章列表与历史时间字段；它**不证明 2006 年当时的 DOM、模板、文章数量、分类计数和分页结构与今天相同**。

---

## 3. 同一账号下存在多个不同正文署名

以下页面当前都使用相同 `blog_56c92245` 账号前缀，但正文署名不同：

### 3.1 徐宁倩

- 页面：`[原创]我的职业生涯规划：想考上公务员 得提前做好准备`
- 当前显示时间：`2007-12-27 08:24:59`
- 正文署名：`文/徐宁倩（大二 06级 法学）`
- URL：  
  https://blog.sina.com.cn/s/blog_56c9224501007z9x.html

### 3.2 王秋红

- 页面：`[原创]知识是一个人成就大业的基础`
- 当前显示时间：`2008-11-09 06:45:24`
- 正文署名：`文/王秋红（大一 07级对外汉语和英语)`
- URL：  
  https://blog.sina.com.cn/s/blog_56c922450100bcyz.html

### 3.3 李幸

- 页面：`[原创]我的职业生涯规划：决胜未来`
- 当前显示时间：`2008-12-06 09:09:24`
- 正文署名：`文/ 李幸 (07级 大一 汉语言文学）`
- URL：  
  https://blog.sina.com.cn/s/blog_56c922450100bm5l.html

### 3.4 林泉

- 页面：`[原创]在金融危机的当下 为了将来我们应该做些什么`
- 当前显示时间：`2008-12-31 08:50:59`
- 正文署名：`文/ 林泉 (06级大三 国际贸易）`
- URL：  
  https://blog.sina.com.cn/s/blog_56c922450100buz9.html

### 3.5 王璇

- 页面：`[原创]我的职业生涯规划：因为有梦，所以无畏`
- 当前显示时间：`2009-01-28 09:23:21`
- 正文署名：`文/王璇 (07级大二法学）`
- URL：  
  https://blog.sina.com.cn/s/blog_56c922450100c30b.html

### 3.6 田有花

- 页面：`[原创]我的职业生涯规划：我的未来，谁主沉浮`
- 当前显示时间：`2010-12-05 07:15:34`
- 正文署名：`文/ 田有花(大一 09 生物科学）`
- URL：  
  https://blog.sina.com.cn/s/blog_56c922450100ndxb.html

### 已证实

- 当前新浪服务层把这些页面放在同一账号标识下；
- 正文显示多个不同作者署名与不同年级/专业；
- 当前页面保留不同历史显示时间。

### 不能据此确定

- 谁现实运营该账号；
- 账号是否由教师、论坛、课程团队、个人站长或其他主体维护；
- 文本最初是否先发表在大学论坛/BBS/课程系统后再转载；
- 当前 `[原创]` 标签具体表示新浪平台哪一层的原创声明，是否等同于“账号主人本人原创”；
- 显示发布时间是否等于作者完成作业时间。

因此安全表述是：

**shared / curated publication layer（共享/汇编式出版层）**，而不是“学生个人博客”。

这是描述当前可观察结构，不是对现实运营者身份的猜测。

---

## 4. 对旧网 evidence schema 的直接修正

这组页面至少要求把以下字段拆开：

```yaml
platform: sina-blog
platform_account_id: 1456022085
url_account_token: 56c92245
original_url: https://blog.sina.com.cn/s/blog_56c922450100....html
text_author: <正文署名>
account_publisher: unknown
displayed_publication_time: <当前页面显示字段>
composition_time: unknown
submission_time: unknown
historical_capture_datetime: unknown
current_observed_state: live-legacy
```

尤其不要再使用一个模糊的 `author:` 同时代表：

- 写文章的人；
- 新浪账号主人；
- 实际点击“发布”的人；
- 课程老师/论坛编辑；
- 当前页面版权主体。

这些角色在旧博客、论坛转载、班级博客、门户专栏和群体账号中可能完全不同。

---

## 5. 时间字段需要至少四层

对于 2008-12-31 的林泉页，当前可以看到一个精确时间：

`2008-12-31 08:50:59`

但旧网考古不能把它直接当成唯一时间轴。建议记录：

1. **composition time**：作者何时完成文本；当前未知；
2. **submission time**：文本何时交给课程/论坛/账号运营者；当前未知；
3. **displayed publication time**：新浪当前 live-legacy 页面显示的 `2008-12-31 08:50:59`；已观察；
4. **archive capture time**：Internet Archive/Common Crawl 等实际抓取时间；本轮尚未取得可核验 capture。

因此：

```text
displayed 2008 timestamp
!= verified 2008 capture
!= proven composition timestamp
```

这条区分对 HPL 的“同时代未来想象”尤其重要：正文内容可以高度符合 2008 年环境，但考古层仍需要独立保存页面 provenance。

---

## 6. live legacy 还暴露出“同一历史内容，多种当前 representation”问题

当前检索还能看到同一账号部分文章通过新浪移动端路径显示：

`https://blog.sina.cn/dpool/blog/s/blog_56c92245....html`

例如同一账号的 2008 年文章现在可以被移动端 renderer 重新呈现，并在页内保留数字账号链接 `u/1456022085`。

这只能证明**今天的平台仍能从同一内容对象生成不同当前 representation**，不能证明 2008 年这些移动端 URL、HTML、CSS、字符集或阅读布局已经以相同形式存在。

所以对 live-legacy 页面必须再区分：

```text
historical content fields survive
!= historical representation survives
```

当前页面最有价值的是帮助恢复：

- exact content URL；
- account ID；
- title；
- displayed timestamp；
- category/tag/byline 等字段；
- 同账号 corpus 关系。

它不能替代 historical memento。

---

## 7. 当前 artifact 状态

```text
platform identity:                   achieved
exact live-legacy account ID:        achieved
exact post URLs:                     achieved
current live-legacy representations: achieved
multiple bylines under one account:  achieved
shared-publication interpretation:   high confidence
real-world account operator:         unknown
original submission workflow:        unknown
verified 2007-2010 archive capture:  NOT achieved
historical HTTP headers:             NOT achieved
historical DOM/charset:               NOT achieved
historical template/CSS/images:       NOT achieved
historical comments/counters:         NOT achieved
second verified historical timepoint: NOT achieved
M1 complete case:                    NOT achieved
```

本轮尝试从精确文章 URL 继续找 Internet Archive/CDX 入口，但当前检索通路没有返回可实际打开并核验的 historical capture。这个负结果只能写成：

**archive replay not obtained in this run**

不能写成：

**Wayback did not preserve it**。

---

## 8. 为什么这对历史解释很重要

如果忽略出版层，一个研究者很容易把：

> “徐宁倩在自己的博客里写下未来规划”

当作自然的个人日记证据。

而当前 artifact 更支持：

> “一篇署名徐宁倩的第一人称职业规划文本，被保存在一个集中刊载职业规划与求职材料的新浪账号里。”

这两个句子的正文内容相同，但历史解释不同：

- 前者暗示自发个人发布；
- 后者提示课程、征集、编辑、论坛或共享出版层可能参与了历史可见性的形成。

于是旧 Web 的保存偏差不仅是“哪些站死了”。还有一层：

> **哪一种文本因为进入了一个持续维护、批量汇编、被搜索引擎反复索引的平台账号，所以比同班没有公开、只存在本地 Word 文件或已经消失的个人空间更容易活到今天。**

这与 HPL 的 `prompt-shaped evidence`、`coherence survival bias` 可以直接交叉。

---

## 9. 海外材料放在哪里

本轮 HPL 同步检查了 2008 年 CivFanatics 的 `Where do you see yourself in 5 year?` 论坛线程作为海外对照：

https://forums.civfanatics.com/threads/where-do-you-see-yourself-in-5-year.273676/

它能帮助比较“课程/共享出版层”与“同侪论坛 prompt”如何产生不同形态的未来陈述。

但该对象属于英文互联网，**不扩写进本仓主研究对象**。OWA 只保留这条交叉链接；全球平台比较主要留在 `how-people-lived`。

---

## 10. 下一步 artifact-first 任务

优先级从高到低：

1. 对上述精确新浪 URL 找 Internet Archive / Common Crawl 历史索引；
2. 若取得 capture，记录 `capture_datetime + original_url + HTTP/replay + DOM + charset`；
3. 优先找 2007-12-27、2008-12-31 两个时点，检查页面模板和账号 chrome 是否相同；
4. 检查历史 article list/category 页，确认多作者汇编结构何时已经出现；
5. 检查评论、转载/收藏字段、标签、分类与链接是否能揭示投稿路径；
6. 检查 ArchiveTeam / 其他新浪博客保存项目是否有 WARC/dump；
7. 不追索作者私人信息，也不批量重发正文；只保存必要 metadata、短摘与 provenance。

如果不能取得 historical capture，本 note 的正式结论也足够明确：

> **当前 live-legacy artifact 足以证明“正文作者层”和“账号出版层”必须拆开，但不足以复原 2007—2010 当时的新浪页面状态。**

这比继续新增第 N 个抽象 `state gap` 更接近仓库当前需要的证据工作。

> 初稿由 AI 辅助整理；事实与页面状态应以可复核来源为准。