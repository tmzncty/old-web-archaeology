# 263 免费个人主页停止服务与百度快照“抢救”链（2000–2002）

> 状态：bounded research note；**不是 M1 完整案例**。  
> 研究对象：263 首都在线免费个人主页，重点考察 2000 年可确认的托管/治理状态、2002 年停止免费服务、收费替代，以及百度搜索快照作为派生保存层的出现。  
> 时间范围：2000-02 至 2002-04；必要背景延伸至 1999–2000 的 263 门户/ISP 环境。  
> 目的：补 ROADMAP M1 的个人主页/主页托管案例与“资源/URL/内容失踪链”，并为 M4 的 archive-gap 模型提供 `origin disappearance != derivative copy disappearance` 的案例。

## 1. 为什么选这个对象

仓库已经有网易个人主页、视聆通/Carboy、BlogCN、BlogBus、Baidu Space、Qzone 等研究。继续写泛泛的“免费主页兴衰”会重复。

263 的缺口不同：这里存在一条罕见且可被同时代报道交叉定位的链：

1. 2000 年，263 明确托管普通用户个人主页，并因用户上传内容卷入侵权争议；
2. 263 对托管内容存在程序过滤与对高排名主页的人工检查；
3. 2002-03-29 24:00，263 停止免费个人主页服务并推出收费替代；
4. 同期报道明确称未付费用户的免费主页内容“不再被 263 保留”；
5. 百度针对这一事件进行个人主页“挽救行动”，声称已经制作约 11 万个 263 个人主页网页快照。

因此它不是普通的“网站关了”案例，而是：

```text
origin-hosted user page
  -> platform moderation / ranking visibility
  -> free-hosting entitlement ends
  -> origin retention ends (for unpaid pages, according to contemporary report)
  -> paid hosting successor offered
  -> independent search-engine snapshot layer exists for part of corpus
```

关键方法问题是：**原托管平台停止保留页面，不等于所有页面内容在同一时刻从整个 Web 证据生态中消失。**

---

## 2. 证据等级

沿用仓库 A/B/C/D：

- **A**：原始/同时代一手 artifact（平台公告、历史 HTML、HTTP 响应、原始用户手册、原始快照等）；
- **B**：近同时代二手报道、采访、技术报道；
- **C**：后来回忆；
- **D**：研究者复原/推断。

本轮没有取得 263 原始 2000/2002 HTML、服务条款或关闭公告，因此**不能把媒体报道中的平台行为升级成 A**。媒体对 263/百度的直接采访或当时现场描述仍按 B 使用；其中的企业自述保留为“operator/company claim”。

---

## 3. 证据表

| 时间 | 证据 | 等级 | 可以支持 | 不能支持 |
|---|---|---:|---|---|
| 2000-02-12 | 《北京晚报》经新浪保存：《263被告侵权引发诸多疑问》 | B | 263 当时提供免费个人主页；普通注册用户可以上传内容；平台使用程序过滤特定词汇，并对排名前列主页做定期人工检查 | 不能推出所有主页都被人工审核；不能确定主页 URL schema、空间配额、charset 或服务器软件 |
| 2000-11-23 | iThome：263 成立网络集团，同时经营 ISP/ICP/IDC | B | 263 当时是综合 ISP/ICP/IDC，说明个人主页服务处在更大的接入+内容+托管业务环境中 | 不能证明个人主页具体运行在何种 IDC 架构或服务器上 |
| 2002-04-02（报道 2002-03-29 截止） | 《北京青年报》经新浪保存：《263免费服务相继死亡 搜狐21cn誓不跟风》 | B | 报道明确称 3 月 29 日 24:00 停止免费个人主页服务；未付费用户内容不再由 263 保留；同时推出 30/70/100MB 收费个人主页，年费 300/700/1160 元 | 不能证明所有旧 URL 在 00:00 同时返回 404；不能证明后台/备份在同刻物理删除 |
| 2002-04-02 | 同一报道对 263 市场部刘先生的采访 | B（operator statement embedded in B source） | 263 将个人主页业务描述为 IDC 业务中的小部分，并称收费主页调整与邮箱收费“恰巧相继” | 不能独立验证公司的动机或实际成本结构 |
| 2002-04-02 | 同一报道记录百度“263个人主页挽救行动” | B（Baidu claim embedded in B source） | 百度称工程师已利用搜索技术制作 263 个人主页网页快照；截至发稿称约 11 万页 | 不能证明 11 万页全部完整；不能证明图片/CSS/JS/下载资源被保存；不能证明快照长期可访问 |
| 1999-07 | CNNIC 1999/7 统计报告 | A/B boundary: institutional contemporary report | `www.263.net` 是受访用户常设浏览器首页中的高频站点之一（1644 票），可作为 263 当时门户可见性的背景 | 不支持个人主页数量、主页 URL 或 2002 关闭事件 |

### 来源定位

1. 新浪科技保存《北京晚报》2000-02-12：  
   `https://tech.sina.com.cn/news/internet/2000-02-12/17274.shtml`  
   关键定位：第二、三段；“263免费提供的个人主页”；后文“程序过滤”“对排名前列的主页采用定期人工检查”。

2. iThome 2000-11-23：  
   `https://www.ithome.com.tw/news/10391`  
   关键定位：标题与首段；263 同时经营 ISP、ICP、IDC。

3. 新浪科技保存《北京青年报》2002-04-02：  
   `https://tech.sina.com.cn/i/c/2002-04-02/109503.shtml`  
   关键定位：首段（3 月 29 日 24:00、免费内容不再保留、收费档位）；“业务调整调掉免费主页”；“百度伸手挽救行动”（约 11 万个网页快照）。

4. CNNIC 1999 年 7 月《中国互联网络发展状况统计报告》：  
   `https://www.cac.gov.cn/files/pdf/hlwtjbg/hlwlfzzkdctjbg004.pdf`  
   关键定位：用户填写的浏览器首页，`www.263.net` 1644 票。

---

## 4. 2000：主页存在，而且平台已经介入内容治理

2000-02-12 的同期报道不是平台产品介绍，而是一次侵权争议。报道明确说，有人使用 263 免费提供的个人主页上传《考研胜经》部分内容，263 又无法通过注册材料找到上传者。

这一材料至少证明：

- 263 免费个人主页在 2000 年已经是实际运行服务；
- 用户拥有上传/发布能力；
- 注册身份可能不足以可靠映射到现实身份；
- 平台已经实施自动词汇过滤；
- 平台对“排名前列”的主页实施人工抽查。

这对旧网考古很重要，因为“免费主页”不能被默认建模成纯静态 FTP 空间。至少在 263 这里，平台层还包括：

```text
account / registration
  -> upload/publishing
  -> hosted page
  -> ranking / visibility
  -> automated filtering
  -> selective human moderation
```

但本轮**没有证据**说明上传协议是 FTP、Web form 还是专有工具，也没有原始页面证明其模板、计数器、留言本或 CGI 能力。

---

## 5. 2002-03-29：停止免费资格与“内容不再保留”必须分层

2002-04-02 的《北京青年报》报道把 3 月 29 日 24:00 作为停止免费个人主页服务的节点，并明确写到：如果免费个人主页用户没有付费，原免费主页内容将不再由 263 保留。

同一报道给出的收费替代为：

- 30 MB：300 元/年；
- 70 MB：700 元/年；
- 100 MB：1160 元/年。

因此可以确认一个商业/托管状态转移：

```text
free hosting entitlement
  -> cutoff
  -> paid hosting successor available
```

但不能把它偷换成：

```text
2002-03-29 24:00
  -> every URL instantly returns 404
  -> every file instantly physically erased
  -> every backup erased
  -> every search copy erased
```

目前这些都没有 A 级 artifact 支持。

建议在未来 disappearance schema 中至少拆开：

- `free_entitlement_end`；
- `origin_content_retention_end`；
- `origin_url_http_end`；
- `dns_end`；
- `paid_successor_available`；
- `derivative_cache_available`；
- `derivative_cache_expiry`。

---

## 6. 百度“挽救行动”：搜索快照是派生保存层，不是原站存续

同一 2002 报道记录了一个非常值得进入仓库方法论的动作：百度得知 263 免费个人主页将停止后，针对这些页面制作网页快照，并称截至发稿已完成约 11 万个主页快照。

这意味着 2002 年的中文 Web 已经出现一种与今天 archive capture 很相似、但制度目的完全不同的派生保存层：**搜索引擎缓存/快照可能在 origin 停止保留后继续让正文可见。**

应严格区分：

```text
origin page
!= search-engine index record
!= search-engine cached HTML snapshot
!= archival capture
```

尤其不能从“百度快照存在”推出：

- 原 263 页面仍然在线；
- 页面全部子资源完整；
- 快照具有长期保存承诺；
- 快照是法律/档案意义上的永久存档；
- 11 万条快照等于 11 万个唯一用户；
- 11 万条快照覆盖了 263 全部免费个人主页。

这里的“11 万”只是**百度当时向记者声称的快照任务数量**，不是本轮独立复算结果。

---

## 7. 一个更准确的失踪链

263 案例至少需要如下状态图：

```text
account exists
  -> free-hosting entitlement active
  -> origin page hosted
  -> page may be ranked / moderated
  -> search engine discovers page
  -> search engine may hold cached snapshot

2002 cutoff:
  free entitlement ends
  -> unpaid origin content no longer retained (reported policy)
  -> paid successor can preserve/continue some hosting
  -> cached derivative may remain independently visible
```

所以：

```text
platform stops free hosting
!= page bytes instantly vanish everywhere

origin content no longer retained
!= derivative cache absent

cached HTML survives
!= original site survives

cached HTML survives
!= complete page experience survives
```

这应当成为后续 M1/M4 对“页面死亡”的标准警告。

---

## 8. 与现有仓库案例的非重复关系

### 与网易个人主页案例

网易研究重点是免费资格、收费 Web hosting / Personal Space 的并存与 grandfathering；263 的新贡献是**明确停止免费主页 + 未付费内容不再保留 + 第三方搜索快照抢救**。

### 与 BlogBus

BlogBus 重点是 DNS/name resolution 与 URL 迁移；263 的核心是**origin retention 与 derivative cache 分离**。

### 与 BlogCN/MSN Spaces

这些对象强调平台迁移/导出；263 则显示第三方搜索引擎可以在没有用户主动迁移的情况下形成派生副本，但其完整性和寿命未知。

### 与 Carboy/视聆通

视聆通强调 access-network reachability；263 是公开门户环境下的 hosting entitlement / retention / cache 问题。

---

## 9. 建议写入位置

当前先写：

- `research/263-free-homepage-baidu-cache-disappearance-chain-2000-2002.md`

拿到 artifact 后可考虑：

- M1 个人主页案例候选的一部分；
- `studies/platform-genealogy.md`：免费托管 -> 收费托管；
- 未来 archive-gap schema：`origin_retention` 与 `derivative_cache` 分离；
- `datasets/sites.csv`：263 个人主页的历史 locator 与 capture 时点；
- `docs/METHOD.md`：搜索缓存只能作为 derivative artifact，不等于 origin capture。

本轮不直接改 METHOD/ROADMAP，避免在没有原始 artifact 的情况下把 bounded case 提升为全局规范。

---

## 10. 下一步 artifact probe

优先级按可证伪性排序：

1. **找到至少一个非敏感 263 免费个人主页原始 locator**（机构页、软件作者页、公开项目页优先，不以普通私人日记为首选）；
2. 查 2000–2002 Wayback/CDX/Common Crawl 是否保存该 locator；
3. 找 2002-03-29 前、后同一 locator 的 HTTP/capture 状态；
4. 找 263 原始“停止免费个人主页服务”公告或帮助页；
5. 找百度 2002 年“263 个人主页挽救行动”的原始公告/产品页；
6. 若能找到历史百度快照 artifact，记录它保存的是 HTML、文本摘要还是完整资源，并检查图片/CSS/JS 的来源；
7. 记录原始 `Content-Type`、charset、HTML meta、frame/object/embed/script/image locators；
8. 只在隔离环境中静态检查未知脚本/二进制，不执行未知 ActiveX/Java/下载文件。

真正拿到同一页面的 `263 origin capture + Baidu derivative snapshot`，这个案例才有机会从 bounded note 升级为 M1 的强案例。

---

## 11. 缺失证据

当前缺：

- 263 原始 2002 关闭公告；
- 263 免费主页的稳定 URL schema；
- 任一已核验的 2000–2002 263 用户主页历史 capture；
- 关闭前后同一 URL 的 HTTP 状态；
- 原始 `Content-Type` / charset / DOM；
- 图片、CSS、JS、CGI/留言本等子资源清单；
- 付费后旧 URL 是否原样延续；
- 未付费内容实际删除的执行批次与时间；
- 百度 11 万快照的 corpus 清单；
- 百度快照的保存完整率、寿命、删除策略；
- 263 主页数量的独立统计。

---

## 12. 可复原程度

### 已可复原（中等置信度）

- 2000 年 263 存在免费个人主页托管；
- 平台对托管内容存在自动过滤与选择性人工检查；
- 2002-03-29 24:00 被报道为免费个人主页停止节点；
- 同期存在收费主页替代；
- 同期报道明确称未付费免费主页内容不再由 263 保留；
- 百度同期声称对约 11 万个 263 个人主页制作网页快照。

### 仅部分可复原

- 免费主页 -> 收费主页的用户迁移比例；
- URL continuity；
- 原始页面的实际页面形态；
- 搜索快照与 origin 的内容一致性。

### 当前不可复原

- 精确 DOM/视觉布局；
- 历史浏览器兼容性；
- charset；
- 动态组件；
- 关闭瞬间的真实 HTTP 行为；
- 百度快照 corpus 的完整性与后续寿命。

---

## 13. 不能声称已经证明的内容

本轮**不能**声称：

- 263 在 2002-03-29 24:00 删除了所有免费主页文件；
- 所有免费主页 URL 当时立即失效；
- 263 的 DNS/主站同时关闭；
- 百度完整保存了全部 263 免费主页；
- “11 万”是唯一用户数或完整站点数；
- 百度快照保存了图片、脚本、样式和下载资源；
- 百度快照今天仍可恢复；
- 263 免费主页使用某个确定 charset、模板系统或上传协议；
- 付费用户一定保留原 URL；
- 2002 的收费调整是 263 个人主页最终永久终止的日期。

---

## 14. 隐私与版权边界

263 个人主页属于典型用户生成内容。即使历史搜索缓存或 archive 仍能访问，也不应默认重新发布普通用户已删除的私人照片、联系方式、日记或可识别个人信息。

研究优先级：

1. 平台公告、帮助页、公开产品页；
2. 机构/项目/软件作者主动公开的非敏感主页；
3. 普通用户页面只记录最小必要 metadata（locator、capture datetime、HTTP/charset/resource facts）；
4. 不把已删除私人内容全文复制进仓库；
5. 百度/263 的专有页面、图片或二进制只记录 provenance、hash、尺寸、MIME 与 archive locator，不重新分发；
6. 涉及争议/侵权内容的 2000 案件，只引用新闻对平台机制的描述，不复刻被指侵权的正文。

---

## 15. 结论

263 免费个人主页提供了一个非常清楚但仍未完成的 disappearance-chain 案例。当前最可靠的结论不是“263 在 2002 年把 11 万个主页删掉了”，而是：

> 同期报道显示，263 在 2002-03-29 停止免费个人主页服务，并对未付费用户停止内容保留；与此同时，百度声称已经为约 11 万个 263 个人主页制作搜索快照。由此可见，旧 Web 的“页面死亡”至少必须区分 origin hosting/retention 与第三方 derivative cache 两层。

下一轮如果拿不到同一 URL 的原始 capture 或百度快照 artifact，应停止扩写叙事，记录 negative result，而不是继续用更多后来回忆填空。
