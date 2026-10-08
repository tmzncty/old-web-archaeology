# MSN / Windows Live Spaces 中国区：博客迁移并不等于页面保存（2005–2011）

> 状态：bounded research note；**不是 M1 完整案例**。
>
> 研究重点：平台形态时间线、跨平台迁移的保存边界、账号/关系/内容/URL 的分离，以及关闭过程中的状态变化。

## 1. 为什么选这个对象

仓库已经覆盖多个中文 BSP、个人主页托管、DNS/域名失踪和字符集案例，但默认分支尚无 `MSN Spaces` / `Windows Live Spaces` 专题。README 第一阶段仍要求至少三个完整案例、平台形态时间线以及现代浏览器/旧网页环境研究；MSN Spaces 同时连接 IM、博客、照片、联系人和社交关系，2010–2011 又发生了有明确迁移工具的关闭过程，因此适合研究“平台关闭时究竟什么被迁走、什么被留下”。

本轮不把“搬家成功”当作“原站完整保存”。

## 2. 初步时间线与证据

### 2005-04：Messenger 7.0 中文版强化 Spaces 集成

**等级：B（近同时代新闻）**

北京现代商报经新浪科技保存的 2005-04-12 报道称，MSN Messenger 7.0 中文正式版面向中国用户推出，并“强化了对 MSN Spaces ‘我的共享空间’服务的支持”，同时升级音乐和照片共享。

来源：
- 新浪科技 / 北京现代商报，2005-04-12：`https://tech.sina.com.cn/it/2005-04-12/1658579849.shtml`

可支持：
- Spaces 在中国用户环境中不是孤立 BSP，而与 Messenger 客户端存在产品级联动。

不能支持：
- 不能据此推断某一具体 Spaces 页面的 DOM、charset、浏览器兼容性或 URL pattern。

### 2006-08：MSN Spaces → Windows Live Spaces，并强化社交圈

**等级：B（近同时代新闻）**

2006-08-23 同期报道记录，MSN Spaces 升级为 Windows Live Spaces，中文版同步出现；新服务与 Windows Live Messenger 整合，并增加“朋友的朋友”等社交圈浏览能力。

来源：
- 南方新闻网经新浪科技保存，2006-08-23：`https://tech.sina.com.cn/i/2006-08-23/14491099985.shtml`

这说明平台形态不能只写成“博客”：至少到 2006 年，内容空间、Messenger 联系人/状态和社交发现已经发生耦合。

### 2010-09-28：全球关闭计划与中国区暂缓迁移

**等级：B（同期新闻 + 对当时官方公告的转述）**

2010-09-29《新京报》报道，当时 Live Spaces 首页已出现微软迁移公告：用户可迁往 WordPress.com、下载备份或删除博客；报道还明确指出全球迁移并非完整复制，草稿、页面主题、小工具、访客留言和清单等不会随博客文章一起迁移。MSN 中国区公关负责人同时表示，中国大陆正在准备本地方案，并建议中国用户暂时不要迁移。

来源：
- 新京报经搜狐保存，2010-09-29：`https://news.sohu.com/20100929/n275333792.shtml`
- 北京商报经新浪科技保存，2010-09-29：`https://tech.sina.com.cn/roll/2010-09-29/01591512308.shtml`

关键结论：

`service migration ≠ full platform preservation`

至少应拆成：

`published posts / drafts / comments / theme / widgets / guestbook / lists / photos / profile / contacts / social graph / access controls / URL identity`

这些对象的迁移命运可以不同。

### 2010-11-11～18：中国大陆本地方案转向新浪博客

**等级：A-/B**

2010-11-11 新浪与 MSN 中国联合宣布战略合作，新浪成为中国大陆地区 Windows Live Spaces 官方迁移合作伙伴；同期专题记录迁移后可使用 Windows Live ID 登录新浪博客，并可通过 Messenger Connect 将新浪博客更新重新显示到 Messenger/Windows Live 环境。

11 月 18 日保存的“微软 MSN 官方邮件”文本进一步列出本地迁移工具声称的能力：迁移日志及评论、日志中的照片和视频；保留 Windows Live 个人资料、联系人和 SkyDrive 在线相册；保持 Spaces 访问权限；迁移后仍可使用 Windows Live ID 登录新浪博客，并在 Messenger 中看到日志更新。

来源：
- 中国广播网经新浪保存，2010-11-12：`https://news.sina.com.cn/o/2010-11-12/073321459742.shtml`
- 新浪科技合作专题：`https://tech.sina.com.cn/z/MsnSina/`
- cnBeta 保存的官方邮件文本，2010-11-18：`https://www.cnbeta.com.tw/articles/tech/127360.htm`

证据分级说明：
- 联合宣布合作的同期报道记 B；
- 被保存的官方邮件内容具有原始通信文本性质，但当前 locator 是第三方转载而非微软原始邮件/服务器 artifact，因此暂记 **A-（derivative primary text）**，待取得原始邮件或微软页面 capture 后再升级。

这里尤其不能把“保留 Windows Live 个人资料、联系人、SkyDrive”理解成“这些数据迁入新浪数据库”。官方邮件的措辞更接近：博客搬走，但这些 Windows Live 服务继续留在微软侧。

因此更合适的模型是：

`Spaces blog content -> Sina Blog`

同时：

`Windows Live ID / profile / contacts / SkyDrive -> remain in Windows Live ecosystem`

再通过：

`Messenger Connect -> cross-platform identity/activity linkage`

这是一种**拆分迁移（split migration）**，不是站点镜像。

### 2010-11：实际搬家并非“无损”已经有同期异议

**等级：B（同期记者观察与用户反馈）**

2010-11-19《东方早报》报道中国大陆专属迁移方案上线，并记录部分用户认为搬家并不顺利。2010-11-22《法制晚报》进一步记录：国内多个第三方搬家工具出现图片不兼容、博文丢失等问题；新浪方面则声称官方合作迁移可以保存文字、图片等，并列举标题、正文、博文图片、评论、空间权限、头像、昵称等项目。

来源：
- 东方早报经新浪保存，2010-11-19：`https://news.sina.com.cn/o/2010-11-19/092218383216s.shtml`
- 法制晚报经新浪科技保存，2010-11-22：`https://tech.sina.com.cn/i/2010-11-22/15144893834.shtml`

注意：平台/合作方对“不会遗失”的承诺是 operator claim，不等于逐对象、逐博客独立验证。

### 2011-03-17：服务正式关闭

**等级：B（机构行业信息 + 同期报道）**

中国互联网协会 2011-03-10 转述 Windows Live 中国团队最后提醒：Spaces 从 3 月 17 日起正式关闭，用户可以迁往新浪博客或下载日志到本地；迁移后仍可用 Windows Live ID 登录新浪博客，并可通过 Messenger Connect 维持更新展示。

3 月 18 日的同期报道记录服务已经在 3 月 17 日正式关闭。

来源：
- 中国互联网协会，2011-03-10：`https://www.isc.org.cn/article/11654.html`
- 至顶网/驱动之家，2011-03-18：`https://soft.zhiding.cn/software_zone/2011/0318/2022893.shtml`

## 3. 本轮得到的核心方法结论

Windows Live Spaces 中国区迁移至少要求把“平台连续性”拆成以下维度：

1. **内容连续性**：已发布博文、评论、图片/视频是否复制；
2. **编辑状态连续性**：草稿是否迁移；
3. **表现层连续性**：主题、布局、小工具是否迁移；
4. **互动对象连续性**：访客留言、清单、评论是否迁移；
5. **媒体对象连续性**：日志内媒体与独立在线相册不是同一个对象；
6. **身份连续性**：Windows Live ID 能否继续作为登录凭据；
7. **关系连续性**：联系人是否继续存在，以及是否真的复制到目标平台；
8. **活动流连续性**：新博客更新能否重新进入 Messenger 好友动态；
9. **权限连续性**：原 Spaces 访问权限能否映射；
10. **URL 连续性**：旧 Spaces URL 是否跳转、是否保留 deep link/path——本轮尚未取得 artifact 证据；
11. **原平台可执行性**：迁移完成后旧页面的脚本、模块和浏览器体验是否还能复现——本轮未知。

因此不能把“官方提供一键搬家”写成“网站被完整保存”。

## 4. 建议写入位置

本轮建议先保留在 `research/`，不立即勾选 M1。

后续如果取得原始 capture，可拆入：
- `cases/windows-live-spaces-cn/README.md`
- `cases/windows-live-spaces-cn/evidence.yaml`
- `cases/windows-live-spaces-cn/timeline.md`
- `cases/windows-live-spaces-cn/reconstruction.md`

平台形态时间线可引用：

`Messenger-linked personal space/blog (2005) -> socially integrated Windows Live Spaces (2006) -> split migration into Sina Blog + retained Windows Live identity/services (2010–2011)`

但这只是该平台的形态变化，不代表整个中文互联网的单线演化。

## 5. 缺失证据 / 下一刀

优先寻找以下 artifact，而不是继续收集怀旧文章：

1. 2005–2006 中国用户实际 Spaces 页面的历史 capture：URL pattern、HTML、charset、脚本、图片和 Messenger 集成痕迹；
2. 2010-09-28 微软原始迁移公告 capture；
3. 2010-11 中国大陆官方迁移工具页面及帮助页 capture；
4. 同一非敏感/机构型测试博客在 Spaces 与新浪迁移后的成对页面，用于字段级 diff；
5. 2011-03-17 前后旧 Spaces URL 的 HTTP/redirect/tombstone 行为；
6. 迁移导出文件格式或公开帮助文档，用于区分“可下载备份”和“可导入迁移”的数据范围。

## 6. 可复原程度

当前：**中等偏低**。

已经可以较稳复原：
- 中国区产品时间线；
- Messenger / Spaces / Windows Live ID / 新浪博客之间的产品关系；
- 关闭与迁移政策；
- 迁移对象存在明确的选择性边界。

尚不能复原：
- 具体历史页面视觉/DOM；
- charset 与 HTTP header；
- 浏览器/脚本依赖；
- 旧 URL 的 redirect 行为；
- 任一用户博客的实际字段级迁移完整率；
- 所有用户是否在同一时点失去写入或读取能力。

## 7. 不能声称已经证明的内容

- 不能声称“中国区 Spaces 已被新浪完整保存”；
- 不能声称“Windows Live 联系人全部复制到了新浪”；
- 不能把 Windows Live ID 可登录新浪等同于账号数据库整体迁移；
- 不能把 Messenger 中仍能看到更新等同于旧社交图完整迁移；
- 不能声称 2011-03-17 当天所有旧 URL 同时返回相同状态；
- 不能声称旧主题、小工具、访客留言等已迁移；同期全球迁移材料反而明确提示若干对象不会迁移；
- 不能根据现代页面或后来的博客副本倒推出旧 Spaces 的 DOM、charset 或浏览器行为。

## 8. 隐私与版权边界

- 不批量重新公开普通用户的旧博客、照片、评论、联系人或访客留言；
- 后续成对迁移验证优先使用机构账号、公开测试账号或明确授权样本；
- 普通用户页面只记录支持平台结构 claim 所必需的最小 locator/metadata，避免正文再发布；
- 不把第三方保存的官方邮件全文复制进仓库；只记录与迁移边界有关的最小事实和 locator；
- 若取得历史导出包，只做结构、字段和 hash/metadata 分析，不提交私人内容。

## 9. 证据表

| 时间 | 主张 | 等级 | 定位 |
|---|---|---|---|
| 2005-04-12 | Messenger 7.0 中文版强化 MSN Spaces 集成 | B | 新浪科技保存的北京现代商报报道 |
| 2006-08-23 | Windows Live Spaces 中文版上线并强化 Messenger/社交圈整合 | B | 新浪科技保存的南方新闻网报道 |
| 2010-09-28/29 | 全球关闭计划；中国区暂缓并寻找本地方案；迁移并非覆盖所有平台对象 | B | 新京报/北京商报同期报道及对公告的转述 |
| 2010-11-11 | 新浪成为中国大陆官方迁移合作伙伴，Messenger Connect 连接两平台 | B | 中国广播网报道、新浪合作专题 |
| 2010-11-18 | 官方邮件列出本地迁移与保留对象 | A- | cnBeta 保存的“微软 MSN 官方邮件”文本，待原始 artifact 核验 |
| 2010-11-19/22 | 本地搬家实际运行；存在用户失败/不完整反馈与合作方完整性承诺 | B | 东方早报、法制晚报 |
| 2011-03-17 | Windows Live Spaces 正式关闭 | B | 中国互联网协会 + 3/18 同期报道 |

## 10. 研究者推断（D）

以下仅作为后续验证框架：

- 中国区方案表现为“博客内容迁往新浪 + Windows Live 身份/联系人/相册留在微软侧 + Messenger Connect 重建跨平台活动连接”的拆分迁移；
- 即使文章和评论全部复制成功，旧平台仍可能因为主题、小工具、URL、访问模型和关系呈现不同而不可等价复原；
- “关系迁移”需要进一步区分复制 social graph、保留原 graph、建立 federated/link bridge 三种机制。现有证据更接近后两者的组合，但必须等待原始技术文档验证。