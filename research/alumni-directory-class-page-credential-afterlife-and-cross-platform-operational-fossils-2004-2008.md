# 网上同学录：班级页、客户端、跨平台操作化石与历史凭证余生，2004–2008

> Scope：1995–2015 中文旧网范围内的 **ChinaRen / QQ 校友录 / 5460 网上同学录**结构，重点检查 2004–2008 同期技术与普通用户操作材料。  
> 交叉生活史包：`tmzncty/how-people-lived/sources/from-paper-alumni-directories-to-searchable-classes-dormant-tie-reactivation-china-1984-2025.zh-CN.md`。  
> 本文不是 ChinaRen/5460 平台通史，也不宣称 M1 完成。新增价值主要是：恢复“班级怎样被找到、建立和维护”的操作结构；确认 5460 同时存在 Web 与 Windows 客户端入口；记录一类特殊保存风险——**平台本身消失以后，第三方通信档案可能继续暴露当年的账号/初始口令材料。**

---

## 0. 去重与本轮 claim list

仓库已经反复建立以下规则：

```text
page != account
page != transaction
locator != verified capture
current live legacy page != historical memento
platform data persistence != relationship persistence
```

所以本轮不再为这些原则换名字。

本轮只验证六个更具体的 claim：

1. 2004 年至少有多种中文网上同学录以“学校 → 班级 → 账号/成员”为基本导航；
2. 5460 当时不仅有 Web，还存在 Windows 客户端，客户端会从服务器下载个人和班级数据；
3. 普通用户能够按姓名/用户名等字段找人，也能按学校和入学年份找班；
4. 一个班级的上线需要管理员做真实的建班、建号、分发和催促劳动；
5. 邮件/Google Groups 这样的**外部平台**会留下另一个平台的 URL、登录流程和账号结构，因此可以形成 cross-platform operational evidence；
6. 这类外部档案也可能让已经没有现实用途的历史明文凭证继续公开存活，形成新的隐私/安全考古问题。

---

## 1. Artifact A：2004 PChome 教程保存了三套校友录的功能和 historical locator

当前可访问页面：

- https://m.pchome.net/article/content-17875-all.html
- 内部日期：`2004-06-23`
- 标题：`百花争艳网上同学录`
- artifact 类型：`current_live_legacy_tutorial`
- historical capture verified：`false`

### 1.1 ChinaRen

教程给出的 historical locator：

```text
http://alumni.chinaren.com
```

同期操作描述：

- 新用户注册；
- Sohu / ChinaRen 邮件用户可复用已有用户名和密码；
- 可以进入“我的大学 / 我的中学 / 我的小学”；
- 可以搜索或创建班级；
- 班级里有共享文件；
- 管理员可以修改班级宣言，甚至嵌入图片和 MP3。

这里可以支持：

```text
school level + class
```

已经是普通用户可见的信息架构，而不是后来怀旧文章补出的平台定位。

### 1.2 QQ 校友录

historical locator：

```text
http://school.qq.com
```

同期操作描述：

- 以 QQ 号码进入；
- 填写个人名片；
- 创建 / 加入班级；
- 已经存在的“同学”QQ群可以转换为校友录；
- 转换时指定入学年份。

这非常重要，因为它说明：

> 平台关系图不是孤立的。一个既有 IM 群可以被重新编码成校友录里的“班级”。

也就是说，QQ 的即时通信身份与学校/年级身份之间已经可以发生结构转换。

### 1.3 5460 Windows 客户端

教程给出的客户端 locator：

```text
ftp://61.137.93.119/5460/5460.exe
```

**本轮没有实际取得该二进制，因此只能登记为 historical binary locator，不得写成 client recovered。**

教程记录的动作链非常详细：

```text
安装客户端
→ 用用户名查询数字 ID
→ 首次登录
→ 从服务器下载个人数据
→ “我的班级”再次下载班级数据
→ 本地显示班级名与成员列表
→ 手动更新留言数据
→ 查看/发表班级留言
→ 查看/增加相册
```

“我的通讯录”又分：

- 班级同学通讯录；
- 教师通讯录；
- 附加通讯录。

客户端还支持按：

- 用户 ID；
- 用户名；
- 昵称；
- 姓名

搜索好友并实时聊天。

### 证据等级

- **B+**：2004 同期技术/使用教程。它能证明作者当时观察到的入口与操作路径；不能证明所有用户、所有客户端版本或所有服务器节点完全一致。

---

## 2. 对 OWA 的直接修正：旧 SNS/社区不一定是“网页对象”

5460 这一条要求我们在平台单位里额外记录：

```yaml
platform: 5460
interfaces:
  web: true
  native_client: true
native_client_locator: ftp://61.137.93.119/5460/5460.exe
binary_recovered: false
server_sync_described: true
```

这并不是新造一个抽象 `gap`，而是 M3 浏览环境实验的实质约束：

> **如果历史用户的重要动作发生在 native client 里，仅恢复 Web 页面就算不上恢复平台使用环境。**

尤其是教程明确说客户端从服务器下载个人数据、班级数据和最新留言。

所以历史状态至少跨越：

```text
server state
↕
client synchronization
↕
local client state
```

单独一张网页 capture 不会保存这个同步链。

---

## 3. Artifact B：2008 Google Groups 邮件串保存了一次“班级上线”的操作过程

当前可访问：

- 标题：`5460同学录 —— 多一条思念通道`
- 当前 host：`groups.google.com`
- 首条可见时间：`2008-07-26`
- URL：  
  https://groups.google.com/g/class-1-in-sisu-2007/c/r8zeyNgOUkI
- artifact 类型：`cross_platform_contemporaneous_message_archive`

### 3.1 隐私红线：源页面包含普通个人历史敏感材料

该页面现在仍暴露：

- 普通班级成员真实姓名；
- 部分邮箱；
- 历史 5460 用户名；
- **明文初始口令材料**。

这些字段对于证明研究 claim 并不需要。

因此本仓**明确不复制**：

- 姓名列表；
- 邮箱列表；
- 用户名列表；
- 口令值；
- 任何可用于将这些字段重新拼回具体个人的表格。

保留原始 URL 只是为了 provenance；任何后续公开数据集也应将此 source 标记为：

```yaml
contains_sensitive_legacy_credentials: true
republish_raw_body: false
extract_minimum_only: true
```

这落实 `docs/METHOD.md` 的“研究必要最小化”，而不是因为材料旧就把它当成无风险历史数据。

---

## 4. 2008 同期邮件真正证明了什么？

把敏感字段全部删掉后，仍然有非常丰富的操作证据。

### 4.1 班级 URL 由 classID 寻址

邮件公开的 historical locator 形态为：

```text
http://www.5460.net/gy5460/jsp/liuyan/liuyan.jsp?classID=<numeric-id>
```

后续邮件还出现：

```text
http://class.5460.net/gy5460/jsp/liuyan/liuyan.jsp?classID=<numeric-id>
```

这证明至少在该班级上下文里，班级页不是纯语义 slug，而是 JSP + 数字 `classID` 路由。

### 4.2 直接 URL 不是唯一入口

邮件明确说明，也可以从 5460 首页：

```text
搜索学校
→ 指定入学年份
→ 找到班级
```

这与 2004 教程互相独立加强了 `school + cohort` 搜索结构。

### 4.3 班级上线依赖人工 bootstrap

该班级不是成员逐个自行发现后自然形成的。

同期邮件描述：

```text
观察邻班使用 5460
→ 一名成员创建本班虚拟教室
→ 为其他成员预建账号
→ 通过 email / Google Group 分发入口和说明
→ 成员首次登录后自行管理
→ 管理者继续回答登录问题
```

两天后邮件又报告：24 名成员中已有 16 人完成过登录。

几个月后，同一串邮件再次提醒：部分成员很久没登录，可能已经忘记账号。

这里可以直接支持：

```text
account created
!=
member onboarded
!=
member remembers credential months later
!=
member remains active
```

这不是新的宏大“state gap”，而是一个具体 old-Web community case 的纵向账号状态。

---

## 5. `cross-platform operational fossil`：一个平台的使用流程可能活在另一个平台的档案里

5460 本身今天未必还给我们留下可用的历史班级页面，但 2008 Google Groups 邮件却保留了：

- 5460 班级 URL pattern；
- classID；
- 搜索学校 + 入学年份的导航路径；
- 账号由谁创建；
- 初次登录后的管理逻辑；
- 登录进度；
- 几个月后的遗忘问题。

因此本轮记录一种非常实用的 evidence route：

**`cross-platform operational fossil / 跨平台操作化石`**。

这里“化石”只是一种研究工作标签，不等同于新的正式 schema 类型。

它的含义是：

> 当目标平台本身缺失时，邮件列表、论坛转帖、教程、博客说明等外部系统，可能保存足够多的操作步骤来恢复目标平台的 transaction grammar。

这类材料必须仍按 B/A 等级分别记录 provenance，不能因为“细节很多”就冒充目标平台自己的 capture。

---

## 6. 更需要警惕的后果：`credential afterlife / 历史凭证余生`

这组邮件暴露出一个此前仓库没有单独强调的隐私风险：

```text
platform account may be dead
platform may be dead
password may be unusable
BUT
credential string survives in another searchable archive
```

本轮称之为：

**`credential afterlife / 历史凭证余生`**。

必须谨慎理解：

- 本轮**没有尝试登录**任何历史账号；
- 不知道这些口令是否后来修改；
- 不知道账号是否仍存在；
- 也不应该测试它们是否仍有效。

研究结论只到：

> **历史身份验证材料可以比原平台的实际可用寿命活得更久。**

这对 old-Web archive 的意义很直接：

**`historical transparency != safe republication`**。

某个页面今天公开可读，不代表研究者应该把其中的凭证再次结构化、索引、引用到 GitHub 或数据集里。

---

## 7. Artifact C：2004 海外中文论坛里的“开班但没人去”反例

当前仍可访问的 CFC 中文网 2004 年线程《开了个校友路!大家有兴趣进来吧!》留下了一条 ChinaRen 班级 locator，并邀请旧同学加入；线程中的回复又提到，自己更早就开过类似校友录，但几乎没人使用。

当前 URL：

- https://bbs.comefromchina.com/threads/278456/
- artifact：`current_live_legacy_forum_thread`
- internal historical date：页面线程显示为 2004 年上下文；本轮未取得同日 archive memento。

### 证据意义

它不是规模证据，却是一条很好的 counterexample：

```text
class space created
!=
class participation achieved
```

这与 2008 “建号 + 发邮件 + 催登录”正好相互校正：平台给了容器，仍然需要人把社会关系搬进去。

### 隐私

本仓不复制该论坛线程里的普通用户名或具体班级个人信息，只保留页面级 provenance 和结构结论。

---

## 8. Artifact D：2005 报刊报道保存“毕业后网上班级”的同时代使用语境

新浪今天仍可打开 2005-03-18《解放日报》报道《“我的大学”虚拟化》：

- 当前 URL：  
  https://news.sina.com.cn/s/2005-03-18/09105394097s.shtml
- 当前 host：`news.sina.com.cn`
- internal date：`2005-03-18`
- body source：`解放日报`
- artifact：`current_live_legacy_news_reprint`
- verified 2005 archive capture：`false`

正文记录：

- 班级成员异地实习后把通知、留言、聊天转到 ChinaRen；
- 毕业后分散到不同地方的班级继续把 online class 当共同空间；
- 记者当时在 5460 / ChinaRen 上观察到多个学校大量线上班级；
- 同时也有学生认为网络参与不能替代线下集体活动。

### 方法价值

它把平台功能和社会使用连接起来，但仍然属于**媒体选择过的案例**。

不能从“某班保持密切联系”推出：

```text
all online alumni classes remained active
```

也不能把记者当时看到的平台 class count 当成去重活跃班级数。

---

## 9. 当前 locator probe：本轮仍没有获得合格 historical memento

针对 2008 邮件里的 5460 class URL，本轮尝试了：

```text
http://www.5460.net/gy5460/jsp/liuyan/liuyan.jsp?classID=...
http://class.5460.net/gy5460/jsp/liuyan/liuyan.jsp?classID=...
```

当前结果：

- 一个当前 URL 可以被请求，但没有得到足以解释历史内容的有效正文；
- 另一个 host 请求超时；
- Web 搜索没有给出一个已经实际打开并核验的 Wayback historical memento；
- 2004 教程中的 FTP 客户端 locator 本轮也没有取得二进制。

因此准确写法是：

```text
historical locator: achieved
period user-operation description: achieved
current target-page body: not usable
historical memento opened/verified: NOT achieved
client binary recovered: NOT achieved
```

绝不能写成：

```text
Wayback did not preserve the class
```

“本轮没取得”不是“不存在”。

---

## 10. 这个案例为什么对 M1 有价值，但现在还不能算 M1

OWA M1 要求一个 forum/BBS/community/platform 类案例至少有：

- 身份确认；
- ≥2 个历史时点；
- 尽可能 ≥2 个独立证据源；
- 缺失资源；
- 浏览器/编码/插件假设；
- 已证实 / 高概率 / 不知道；
- 后来回忆与同时代证据比较。

当前 5460 / 校友录 case 已经有：

### 已有

- 2004 技术教程（B+）；
- 2004 普通论坛线程（B）；
- 2005 报刊使用报道（B+）；
- 2008 普通班级邮件（A-/B+）；
- Web URL pattern；
- native client locator；
- client/server sync 操作描述；
- classID、school/year search 描述；
- 一组明确的隐私红线；
- 多时间点“社会证据”。

### 缺失

- ≥2 个**实际打开并核验**的 historical Web capture；
- capture datetime；
- historical HTTP / Content-Type / charset；
- 页面 DOM；
- CSS / 图片 / JS 资源完整性；
- 5460 Windows 客户端二进制；
- 客户端版本信息；
- Windows/IE 依赖；
- 登录后页面的 archive 状态；
- 2004–2008 同一 class/page 的可比较 UI diff。

所以：

**`M1 alumni/community case: NOT ACHIEVED`**。

---

## 11. Browser / client assumptions

### Web 部分

目前不知道：

- 5460 班级页当时的声明 charset；
- 是否存在 IE-specific JS；
- iframe / popup / ActiveX；
- 登录 cookie/session 的具体结构；
- archive rewrite 会不会破坏 JSP query 参数或登录跳转。

### Native client

2004 教程证明客户端存在和大致操作，但尚不知道：

- 具体 Windows 最低版本；
- transport protocol；
- server endpoints；
- 本地文件格式；
- 本地缓存是否含敏感通讯录；
- 客户端是否依赖 IE 组件渲染内部页面；
- 登录密码在本地怎样存储；
- 服务器停运后客户端是否仍能打开本地缓存。

这些都是未来 M3 的实质实验问题。

---

## 12. 一个新的保存层：`class state` 比 page body 更容易消失

这里不需要再创造抽象“page != state”理论，但应把具体 state 列出来。

一个 2008 年班级的真实可用状态至少包括：

```text
classID
class metadata
member roster
account membership
member login status
admin/deputy permissions
messages
albums
address book
teacher directory
friend links
private messages / IM
server-side credential state
client-side downloaded state
```

即使以后取得一张公开班级页 HTML，也很可能只恢复其中一小部分。

所以这个案例的 resource-missing checklist 应把：

**`class-state loss / 班级状态缺失`**

作为具体字段，而不是把“页面截图找到了”误写成“班级恢复了”。

---

## 13. Platform death 与 social-index death

交叉 HPL 研究说明，网上同学录的功能之一，是把：

```text
school + cohort + class + name
```

变成“过去的人可以再次被找回”的索引。

因此平台死亡造成的损失不只是内容：

```text
photos lost
messages lost
```

还可能包括：

```text
relationship lookup graph lost
```

也就是：原本还能按学校/届次找到的人，再次变成只有模糊记忆、没有当前坐标的人。

OWA 以后研究平台关闭时，应该问一个更具体的问题：

> **这个平台是不是同时充当了旧关系的 directory / lookup infrastructure？**

如果是，平台消失就会改变普通人重新进入过去社会关系的可执行性。

---

## 14. 隐私与伦理：这类平台的“完整复原”本身可能是不合适的目标

网上同学录特别容易留下：

- 真实姓名；
- 学校；
- 年级；
- 班级；
- 同学关系；
- 旧邮箱；
- 旧电话；
- 家庭/工作信息；
- 明文初始口令；
- 照片；
- 留言和私密往事。

因此未来即使拿到完整 WARC，也不应该默认：

```text
more complete republication = better archaeology
```

更合适的是：

```text
recover schema
recover navigation
recover field names
recover URL patterns
recover browser/client assumptions
recover aggregate state
MINIMIZE ordinary-person content
```

特别是凭证类材料：

- 不测试；
- 不结构化导出；
- 不全文引用；
- 不创建可搜索用户名/口令数据集；
- 只记录“这种字段曾公开存在于 archive”以及它对证据伦理的意义。

---

## 15. 证据表

| 对象 | 日期 | 当前形态 | 可证明 | 不能证明 | 等级 |
|---|---:|---|---|---|---|
| PChome《百花争艳网上同学录》 | 2004-06-23 | current live legacy tutorial | ChinaRen/QQ/5460 功能、URL/FTP locator、客户端动作 | 普遍使用率、当前二进制存在、历史页面 DOM | B+ |
| CFC 中文论坛校友录线程 | 2004 | current live legacy forum | 普通用户创建/邀请加入班级；存在低参与反例 | ChinaRen 班级实际活跃统计 | B |
| 解放日报/新浪《“我的大学”虚拟化》 | 2005-03-18 | current live legacy news | 异地实习/毕业班级用 online class 维持联系 | 全体大学生代表性 | B+ |
| Google Groups 5460 班级邮件 | 2008-07 起 | contemporaneous cross-platform message archive | class URL、学校+年份检索、人工建号/分发、登录进度、账号遗忘 | 5460 页面 UI、账号今天是否有效 | A-/B+ |
| 5460 class locator current probe | 2026 检查 | empty/unusable body / timeout | locator 当前解析尝试状态 | 历史 capture 是否存在 | D-level research observation |

---

## 16. 已证实 / 高概率 / 不知道

### 已证实

- 2004 年 ChinaRen/QQ/5460 都存在面向班级/校友关系的入口；
- 5460 当时存在 Windows 客户端 locator 和 server-data-download 操作描述；
- 2008 年一个具体班级通过邮件把成员引导到 5460 班级；
- 该班级可按学校 + 入学年份在 5460 中查找；
- 账号建立之后还会出现“不登录 / 忘账号”的状态；
- Google Groups 当前保存的邮件正文包含普通个人历史凭证材料；
- 本仓没有必要复制这些材料来证明上述 claim。

### 高概率，但仍需 artifact 验证

- 2004 教程中的 Windows 客户端真实连接 5460 服务端并同步所述班级数据；
- JSP classID URL 在 2008 当时可公开访问到相应班级页面；
- Web 与 native client 共享部分账号/班级后台状态。

这些目前由同期教程/用户操作相互支持，但没有 binary / packet / historical page capture 验证。

### 不知道

- historical page 的 DOM/charset/JS；
- FTP binary 是否还存在于任何 archive；
- 当前空/超时 locator 与历史 5460 服务之间的具体迁移链；
- Google Groups 中历史初始凭证是否后来修改；
- 任何历史账号今天是否存在或可用（也不应尝试）；
- 班级页面是公开可读、登录可读还是字段分级可读的完整规则；
- 5460 的删除、隐私、注销和数据导出机制。

---

## 17. 后见之明风险

### 风险 A：把 5460 写成“微信群之前的微信群”

不成立。它有 Web 班级、通讯录、相册、留言和独立客户端，账号/内容/同步模型都不同。

### 风险 B：把 Windows 客户端 locator 当作已保存软件

教程里的 FTP 地址只能证明当时作者给出了这个下载位置；本轮没有拿到 binary。

### 风险 C：把 Google Groups 页面当作 5460 capture

它只能证明邮件里怎样描述和使用 5460；不是目标站页面原件。

### 风险 D：因为现在看得到旧用户名/密码，就去测试

绝对不应该。研究上不需要，而且会跨越明显的伦理与安全边界。

### 风险 E：把 current live legacy 新闻页当作原始 2005 新浪 DOM

当前页面保存历史正文，不等于已经恢复当时的 CSS/JS/导航和评论状态。

---

## 18. 对 OWA 方法的实质新增

本轮真正值得写回方法意识的不是再一个 `state gap`，而是三件很具体的事：

### 18.1 历史平台可能跨 Web / native client 两套交互层

M3 不能默认“浏览器复原 = 平台复原”。

### 18.2 一个死平台的操作语法可能活在另一个平台的 archive 里

教程、邮件列表、BBS 可以提供 target platform locator、字段、步骤和失败状态。

### 18.3 历史凭证可以比平台活得更久

archive researcher 的责任不只是“尽量找到更多”，还包括：**找到以后决定什么不应该再次公开。**

---

## 19. 下一步

1. 继续查 `alumni.chinaren.com`、`school.qq.com`、`www.5460.net`、`class.5460.net` 的 Wayback / Common Crawl / ArchiveTeam locator；
2. 目标不是多找新闻，而是至少取得两个可以实际打开、记录 `capture_datetime` 的 5460/ChinaRen historical capture；
3. 查找 5460 Windows 客户端的可信软件档案或镜像，只登记 hash/metadata，不随意重新分发；
4. 若取得 binary，在隔离环境做静态分析，先确认 OS/API/endpoint 假设，再决定是否进入 M3；
5. 不恢复、测试或传播普通用户历史凭证；
6. 对现有 Google Groups 证据在未来 schema 中加入 `sensitive_artifact` / `credential_material_present` 之类的保护字段；
7. 若 M1 选用这一 community case，至少取得两个时点的真实 capture 后再升级，不因现有材料丰富而提前宣称完成。
