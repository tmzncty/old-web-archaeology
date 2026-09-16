# 网易个人主页：从免费托管到收费 Personal Space 的服务状态与 URL 谱系（1998—2006）

> 状态：**bounded platform / hosting transition research note；不是 M1 complete case。**  
> 研究对象：网易个人主页托管服务，从 1990 年代末的免费主页，到 2001 年收费托管、2002 年 `Personal Space` / 收费个人主页，再到 2006 年前后的退出线索。  
> 本文优先处理“服务政策、URL 架构、免费/收费状态与退出语义”，不把没有打开核验过的 Wayback 页面写成历史页面证据。

## 0. 为什么现在做这个对象

仓库当前的主要缺口已经不是“再找一个旧网站名字”，而是把 M1 / Phase 2 所需的历史对象做深：

- 同一对象的跨时间变化；
- 页面 / host / 服务政策 / 账号状态不能混写；
- 至少两个独立证据家族；
- 明确哪些结论仍缺实际 capture、charset、DOM、资源依赖与浏览器环境。

现有个人主页研究已经覆盖 Carboy / “完全上网手册”的个体主页 locator，但尚未把一个大型中文个人主页托管平台的**免费 → 收费 → 遗留免费页并存 → 服务退出**过程做成细粒度证据链。

网易适合作为这一缺口的 bounded case，因为本轮获得了：

1. 网易向 SEC 提交的同时代公司原始文件；
2. 1998、2001、2002、2003 年的同期新闻 / 网络转载；
3. 2002 年网易自己公布业绩时出现的 `diy.163.com` 服务 locator；
4. 2002 年普通论坛用户转贴出的具体个人主页 URL；
5. 一处非常值得保留的“停止免费服务”语义冲突。

---

## 1. 先拆对象：不要把“网易个人主页”当成一个永恒不变的网站

本轮至少区分：

```text
operator / company
  NetEase / 网易

service family
  personal homepage hosting

service tier / entitlement
  free homepage storage
  fee-based premium Web page hosting

product label
  Personal Space（2002 后的公司英文披露名称）

service entry / host family
  diy.163.com

individual page locator
  <user>.diy.163.com/<path>

account + billing state
  legacy non-fee / premium / upgraded / discontinued

actual page body + assets
  HTML / images / scripts / downloads / guestbook etc.
```

所以：

> **服务“停止免费” ≠ 所有旧免费页面当日被删除。**

同样：

> **一个历史 URL 被别人引用 ≠ 本轮已经恢复并检查了该历史页面。**

---

## 2. 证据表

| ID | 时间 | 证据 | 等级 | 本轮用途 |
|---|---|---|---|---|
| A1 | 2003-06-27（文件继续以此日为陈述日期） | NetEase Form 20-F/A / SEC：2001-03 收费 Web Page Hosting；2002-03 重新推出并改称 `Personal Space`；免费存储提供到 2001-12；旧免费页获准继续存在；2003-05-31 仍约 27,000 个 non-fee pages、74,000+ premium pages | **A** | 服务政策与免费/收费共存的核心原始证据 |
| B1 | 1998-05-16 | `cn.bbs.comp.software` 同期网络新闻转载：网易重新开放个人主页申请，首日申请超过 3000；称网易以免费个人主页闻名 | **B** | 证明 1998 年免费主页申请服务确在运行；转载来源链未完全恢复 |
| B2 | 2001-03 / 2002-01 回顾 | 《南方都市报》经新浪保存的 2001 年网易拓展轨迹：`3月8日个人主页全面升级` | **B** | 独立支持 2001-03 服务转折 |
| B3 | 2001-03-14 | 《财经时报》经新浪保存：网易已宣布利用个人主页开拓新的收费途径 | **B** | 独立支持收费方向已在 2001-03 同期公开 |
| B4 | 2002-08-05 | 网易第二季度业绩新闻稿经新浪保存：收费服务包含“个人主页服务 `diy.163.com`” | **B（内容源为运营方新闻稿）** | 提供 2002 年服务入口 locator |
| B5 | 2002-08-21 | CFC 中文网历史论坛帖保存具体链接 `http://lichen369.diy.163.com/book/story.htm` | **B** | 提供 `<user>.diy.163.com/...` 的具体同期 user-page locator；本轮未打开该目标历史页 |
| B6 | 2003-01-14 | 赛迪网经新浪保存：称 2002-08-15 网易“全面停止免费个人主页服务”，付费后可继续使用既有 100M，升级每月 15 元 | **B** | 与 A1 对读，限定“停止免费服务”的语义 |
| B7 | 2006-04-12 | 同期 Web2.0/BSP 评述转载：称网易 2006-01-20 关闭“个人空间”，此前公告不再继续发展虚拟主机及域名业务 | **B** | 2006 退出节点的近同时代线索；尚缺原始关闭公告 |
| C1 | 2010 / 2014 | 后来回忆文章重复 2006-01-20 关闭说法 | **C** | 只能增强 locator lead，不能替代原始通知 |
| D1 | 本文 | 对“2001-12 不再提供免费存储”与“2002-08-15 全面停止免费服务”的语义协调 | **D** | 明确提出待验证解释，不当成事实 |

### A1 — SEC / NetEase operator record

- NetEase Form 20-F/A：  
  <https://www.sec.gov/Archives/edgar/data/1110646/000119312504114927/d20fa.htm>

该文件对自己的 Web Page Hosting 服务写得非常具体：

- 2001 年 3 月推出收费 premium Web page hosting；
- 用户可建立、维护 personal homepages；
- 2002 年 3 月以增强功能重新推出，之后改称 `Personal Space`；
- 免费个人主页存储提供到 2001 年 12 月；
- 2001 年 12 月以前建立的免费主页**允许继续存在**，同时鼓励迁往 premium；
- premium 强调更大空间、更快 / 更安全服务器与 24 小时支持；
- 截至 2003-05-31，约有 27,000 个 non-fee personal homepages，与 74,000+ premium personal homepages。

这里的强项是它来自运营者对监管机构提交的同时代公司文件；它仍然是公司自述，不应自动扩张成“所有用户实际体验都如此”。

### B1 — 1998 免费主页申请重新开放

- Google Groups 保存的 `cn.bbs.comp.software` 网络新闻转载，1998-05-16：  
  <https://groups.google.com/g/cn.bbs.comp.software/c/N-CnYVj4n8M>

文本称网易“以提供个人免费主页闻名”，重新开放申请后首日申请超过 3000 人次。

它是同期传播文本，但原始新闻稿 / 页面尚未恢复，因此不升为 A。

### B2 / B3 — 2001 年 3 月从免费优势转向收费路径

- 《南方都市报》经新浪保存的“网易2001拓展轨迹”，2002-01-05：  
  <https://tech.sina.com.cn/i/c/2002-01-05/98289.shtml>
- 《财经时报》经新浪保存，2001-03-14：  
  <https://tech.sina.com.cn/i/c/57790.shtml>

前者把 `3月8日个人主页全面升级` 记入年度轨迹；后者在 3 月 14 日已称网易对外公布将利用个人主页开拓新的收费途径。

这与 A1 的“2001 年 3 月推出 fee-based premium hosting”互相独立地对上。

### B4 — `diy.163.com` 是 2002 年服务 locator

- 网易第二季度业绩新闻稿经新浪保存，2002-08-05：  
  <https://tech.sina.com.cn/i/c/2002-08-05/2028130319.shtml>

文中列举收费服务收入来源时，直接写出：

```text
个人主页服务 diy.163.com
```

这比后来回忆里的模糊“网易主页地址”可靠得多。

但因为我们实际访问的是新浪保存的新闻稿页面，而不是 2002 年 `diy.163.com` 本身，所以它是**locator evidence**，不是该服务页面的 capture evidence。

### B5 — 具体用户页 locator：`<user>.diy.163.com/...`

- CFC 中文网，历史帖时间标为 2002-08-21：  
  <https://bbs.comefromchina.com/threads/28514/>

帖子直接分享：

```text
http://lichen369.diy.163.com/book/story.htm
```

它至少支持：

```text
diy.163.com              = service locator
lichen369.diy.163.com     = user-specific hostname
/book/story.htm           = deeper user-controlled/content path
```

但必须保持边界：

- 本轮没有打开 2002 年该目标页的历史 capture；
- 不知道目标页当时返回的 HTTP 状态、charset、DOM 与资源依赖；
- 不因论坛仍保存这条 URL 就推断目标页仍然存在；
- 不在仓库复制该普通用户页面内容。

---

## 3. 时间线：免费主页不是在某一天简单“消失”

### 1998-05：免费主页仍是网易的重要公开服务

B1 表明网易重新开放免费个人主页申请后，第一天申请量就超过 3000。

可安全声称：

> 到 1998 年 5 月，网易确实在运行面向个人的免费主页申请服务。

不能从这一条推出：

- 具体空间容量；
- URL schema；
- 页面编辑方式；
- FTP / Web editor 是否必需；
- 申请者有多少最终建成活跃站点。

### 2001-03：premium hosting 被正式推出

A1：2001 年 3 月推出 fee-based premium Web page hosting。  
B2：2001-03-08 “个人主页全面升级”。  
B3：2001-03-14 同期报道已经把它描述为从个人主页开拓收费途径。

因此这里是一个相当稳的跨来源转折点。

但：

> **收费产品出现 ≠ 免费产品立即消失。**

### 2001-12：公司称不再提供新的免费 storage entitlement

A1 的措辞是：

> Until December 2001, we also offered free computer storage space for personal homepages.

紧接着它又说，那个日期以前建立的免费主页仍被允许存在。

所以更准确的状态模型是：

```text
new free-storage entitlement
  ↓ closes / is no longer offered

legacy free pages
  ↓ may remain

premium hosting
  ↓ actively promoted
```

不能压缩成一句“2001 年 12 月网易把免费主页删了”。

### 2002-03：premium 服务增强并改称 `Personal Space`

A1 明确说 2002 年 3 月 re-launched with enhanced features，之后 renamed `Personal Space`。

这说明至少要区分：

```text
service lineage
!=
product label
!=
individual homepage identity
```

页面的品牌层可以改名，而用户页、账号和内容可能继续延续。

### 2002-06 / 08：`diy.163.com` 已经是收费个人主页服务 locator

B4 在 2002 年第二季度业绩新闻稿里直接给出 `diy.163.com`。

B5 又从普通用户侧保存了一个 2002-08-21 的具体链接：

```text
http://lichen369.diy.163.com/book/story.htm
```

这两条来自不同证据家族，可以互相支持：`diy.163.com` 不只是后来回忆出的名字，而确实进入了运营方服务描述和同期用户传播链。

### 2002-08-15：“全面停止免费个人主页服务”必须谨慎解释

B6 的 2003 年赛迪网年度回顾写道：

- 2002-08-15 网易“全面停止免费个人主页服务”；
- 用户付费后可继续使用；
- 保持以往 100M 空间；
- 升级费 15 元 / 月；
- 新注册用户同等级服务价格更高。

这是很有价值的同期近时材料，但它和 A1 不能被粗暴拼成：

> “2002-08-15 所有免费页被删除”。

因为 A1 又明确说：

- 2001-12 以前建立的免费页被允许继续存在；
- 到 2003-05-31 仍约有 27,000 个 non-fee personal homepages。

### 2003-05-31：legacy non-fee 与 premium 明确共存

A1 的数字尤其关键：

```text
legacy/non-fee personal homepages: ~27,000
premium personal homepages:       >74,000
```

这意味着最晚到 2003 年 5 月，公司的 own reporting 仍把两类页面作为并存状态报告。

---

## 4. “停止免费服务”到底是什么意思？——本轮最重要的证据冲突

### 已证实

A1：

- 免费 storage offered until 2001-12；
- earlier free pages allowed to remain；
- 2003-05 仍有约 27,000 个 non-fee pages。

B6：

- 2003 年近时回顾称 2002-08-15 “全面停止免费个人主页服务”；
- 并称付费后可以继续使用服务。

### 不能直接证明

目前没有足够证据决定 B6 中“全面停止”的精确 operational semantics。

至少存在几种可能：

```text
D1-a  停止新建免费主页 / 新增免费 entitlement
D1-b  停止对 legacy free 用户提供某些维护 / 功能 / SLA
D1-c  开始强力要求某一批用户付费升级，但仍保留部分 grandfathered pages
D1-d  不同产品/账号批次有不同处理规则
```

这些都只是 **D 级待验证解释**。

只有找回：

- 2001-12 的免费服务政策页；
- 2002-08-15 的实际通知；
- 对应 account / upgrade 页面；
- 同一 legacy free page 在前后时点的 capture；

才有资格进一步收敛。

### 方法论结论

本例直接提醒平台谱系研究：

```text
free signup closed
!=
free account deleted
!=
page body deleted
!=
public URL stopped resolving
!=
paid successor created
```

“某服务停止免费”这种新闻标题，不能直接拿来给页面生命史写终止日期。

---

## 5. 2006 退出：目前只能写成 B/C 级节点

本轮找到的近同时代线索：

- 2006-04-12 的 Web2.0 / BSP 评述转载：  
  <https://groups.google.com/g/cn.fan/c/-hZbqvlvM8U>

它称：

- 网易在 2006-01-20 关闭“个人空间”；
- 此前已公告不再继续发展虚拟主机及域名业务。

后来回忆：

- 月光博客 / Google Groups 2010：  
  <https://groups.google.com/g/williamlong/c/-IwCBydOvKA/m/FsPsEaFmcMQJ>
- 央广网 2014 的互联网回忆文章：  
  <https://tech.cnr.cn/techhlw/20141028/t20141028_516677679.shtml>

当前最谨慎写法：

> **有近同时代 B 级材料和后来 C 级回忆共同指向 2006-01-20 的“个人空间”关闭节点，但本轮尚未恢复网易原始关闭通知，因此不升为 A。**

也不能从“关闭个人空间”进一步自动推出：

- 当日所有 `*.diy.163.com` 页面同时停止解析；
- 所有数据同日删除；
- 域名同日失效；
- 用户没有迁移期；
- “博客兴起”是唯一或已证明的因果解释。

---

## 6. URL / host 谱系：本轮能证明到哪里

### 较强：2002 `diy.163.com`

B4：运营方新闻稿经新浪保存，明确写出 `diy.163.com`。  
B5：同期普通用户帖出现 `lichen369.diy.163.com/book/story.htm`。

因此可以较稳地记：

```yaml
service_host_2002: diy.163.com
user_host_pattern_observed:
  - <user>.diy.163.com
example_path_observed:
  - /book/story.htm
```

注意这里只是**observed locator pattern**，不是全站 schema。

### 仍未知：1998 免费主页的 canonical host/path

本轮没有足够 A/B 级 artifact 把 1998 免费主页的 URL schema 固定下来。

后来的回忆 / 转载里会出现不同 `163` host 写法，但在 archive capture 核验之前，不应把它们自动拼成一条无缝迁移链。

### 仍未知：2006 关闭后的 redirect / tombstone / DNS 行为

缺：

- `diy.163.com` 2005/2006 HTTP 行为；
- 用户 subdomain 是否统一 redirect；
- 404 / parking / NXDOMAIN / product notice 的发生顺序；
- 域名继续存在但 content identity 改变的可能。

因此目前不能声称已经完成“页面与域名失踪链条”。

---

## 7. 托管环境：能说服务等级，不能猜服务器拓扑

A1 允许我们说 premium service 被运营方宣传为：

- greater storage space；
- more secure and faster server；
- 24-hour customer support；
- more reliable platform。

这证明了**服务层级 / hosting promise** 的变化。

它不证明：

- 实际物理机型号；
- 操作系统；
- Web server 软件；
- 机房；
- 是否从 shared hosting 迁往某一种特定虚拟主机架构；
- legacy free pages 与 premium pages 是否物理隔离。

所以本文不把“更快服务器”扩写成未经证实的基础设施故事。

---

## 8. 浏览器、字符集与编辑工具：本轮仍为空，不用常识补

即使 1998—2002 年中国 Web 常见 IE、GB2312/GBK、FTP 工具或 FrontPage，本轮也没有从已打开的网易历史主页 artifact 中验证：

- `Content-Type`；
- HTML `<meta charset>`；
- 页面实际字节编码；
- FTP 上传；
- Web editor；
- FrontPage extensions；
- JavaScript requirements；
- frames；
- ActiveX / Java / Flash；
- browser-specific layout。

因此一律记为 **unknown**。

这是 M1 仍未完成的重要原因。

---

## 9. 可复原程度

### 当前可以较可靠复原

1. 1998 年网易仍在运营免费个人主页申请；
2. 2001 年 3 月出现明确的收费 premium homepage hosting 转折；
3. 公司称免费存储提供到 2001 年 12 月，但旧免费页并非立即全部消失；
4. 2002 年 3 月 premium service 增强并使用 `Personal Space` 名称；
5. 2002 年 `diy.163.com` 与 `<user>.diy.163.com/...` locator 确实进入同期材料；
6. 2003 年 5 月 legacy non-fee 与 premium pages 仍同时存在；
7. 2006 年 1 月关闭节点有 B/C 级支持，但尚缺 A 级原始通知。

### 当前只能高概率 / 有线索

- 2002-08-15 可能代表免费服务权利进一步收紧 / 转付费阶段；
- 2006-01-20 是个人空间服务正式关闭日；
- 关闭与博客产品兴起之间存在业务替代关系。

以上不能全部写成已证实因果事实。

### 当前不知道

- 1998 免费主页 URL pattern；
- 2001/2002 产品入口的完整 DOM；
- 历史 charset；
- 上传 / 编辑工具链；
- 用户页模板结构；
- guestbook / counter / comments 等动态后端状态；
- 2002-08-15 对不同 legacy 用户到底执行了什么；
- 2006 关闭时的迁移 / 导出政策；
- `diy.163.com` 与用户 subdomain 的逐日失效过程；
- 图片、下载和脚本子资源保存率。

---

## 10. 为什么这仍不是 M1 complete case

按 `RESEARCH_PLAN.md`，本轮仍缺：

- [x] entity / service identity confirmation；
- [x] 多个历史时间点的政策 / locator 证据；
- [x] 至少两个独立证据家族；
- [x] later recollection vs contemporaneous evidence comparison；
- [ ] 一个实际打开、按 capture contract 编目的历史 `diy.163.com` 页面；
- [ ] 第二个实际打开的历史页面时点；
- [ ] `evidence.yaml`；
- [ ] `timeline.md`（独立 case 结构）；
- [ ] `reconstruction.md`；
- [ ] DOM / charset；
- [ ] main document vs subresource loss inventory；
- [ ] browser/plugin assumptions grounded in artifact；
- [ ] 2002-08-15 policy page / notice；
- [ ] 2006 closure notice / tombstone。

结果：

**`M1 NetEase personal-homepage case: NOT ACHIEVED IN THIS RUN.`**

---

## 11. 下一轮限定取证顺序

不要继续写更多“个人主页为何衰落”的概念文章；优先找 artifact：

1. **2001-03-08** 前后的网易个人主页入口 / 升级公告；
2. **2001-12** 免费 storage 截止相关 policy / help；
3. **2002-03** `Personal Space` relaunch 入口 / pricing / help；
4. **2002-06~08** `diy.163.com` 首页与一个非敏感代表用户页 capture；
5. **2002-08-15** “停止免费个人主页服务”原始公告；
6. **2003-05** legacy free 与 premium page 的可见差异；
7. **2006-01-20** 关闭通知 / tombstone；
8. 对每个打开的 capture 记录：
   - original URL；
   - capture URL + timestamp；
   - replay / HTTP state；
   - `Content-Type`；
   - charset；
   - DOM / frames；
   - CSS / image / JS / download 子资源；
   - redirect；
   - privacy risk。

如果 Internet Archive replay 仍不可访问，只保存 locator 与失败分类，不写“Wayback 没有保存”。

---

## 12. 建议写入位置

本文件作为 evidence package / research note 保留。

后续取得 artifact 后可进入：

- `cases/`：个人主页 / hosting complete case；
- `studies/platform-genealogy.md`：免费个人主页 → premium hosting / Personal Space → later blog/SNS 的**非线性**关系；
- `datasets/sites.csv`：`diy.163.com` 与 representative user host；
- archive-gap model：host survives / page disappears / policy changes / dynamic state missing 等。

在 capture 验证前，不勾选 Phase 2 complete case。

---

## 13. 隐私与版权边界

个人主页尤其容易把“技术史取证”变成对普通人的重新曝光。

本对象后续必须遵守：

- 不批量枚举 `*.diy.163.com` 用户；
- 不为了证明 URL pattern 而重新公开普通人的姓名、邮箱、电话、住址或私人照片；
- 只选支持平台结构 claim 所需的最小代表样本；
- 对已经删除的用户页面，优先记录 metadata / URL pattern / resource status，而不是整页转载；
- 不把 archive 可访问等同于允许在仓库重新分发；
- 不提交版权不明的历史图片、音乐、下载文件或二进制；
- 若必须引用个人页正文，只摘取与技术结构直接相关的最小片段，并考虑去标识化。

B5 的具体 URL 只因为它已经在一个公开的 2002 年同期帖子中作为普通 Web 链接存在、且用于证明 URL architecture；本仓不复制其目标页正文。

---

## 14. 本轮结论

这次真正新增的不是“网易以前有个人主页”这条常识，而是一个可检验的状态链：

```text
1998 free homepage application active
        ↓
2001-03 premium paid hosting introduced
        ↓
2001-12 new free storage no longer offered
        ↓
legacy free pages remain
        +
2002-03 premium service relaunched as Personal Space
        ↓
2002 `diy.163.com` / <user>.diy.163.com/... observed
        ↓
2002-08 press says “stop free homepage service”
        ↓
2003-05 operator still reports ~27k non-fee pages
        ↓
2006 closure lead (B/C; original notice not yet recovered)
```

因此最重要的研究约束是：

> **不要给平台服务寻找一个虚假的单一“死亡日”。账号资格、免费 entitlement、付费产品、页面公开性、URL、内容和域名可能在不同日期改变。**

而这正是下一步历史 capture 应当检验的对象。