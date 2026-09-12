# 中国劳动力市场网（`www.lm.gov.cn`）历史 artifact probe，2002–2006

> 状态：**artifact probe / 未达到 M1 完整案例门槛**。
>
> 本文件不把“后来的文献还记得这个 URL”写成“历史网页已经恢复”。它只保存本轮能够确认的站点身份、历史原始 URL 线索、同期使用证据，以及尚未取得 verified capture 的负结果。
>
> 与 `docs/ARTIFACT_NEGATIVE_RESULT_LOG_2026-09-12.md` 相同，本文件遵守 `docs/METHOD.md`：candidate locator / historical original URL / verified archive capture 必须分开。

---

## 1. 为什么选这个对象

本轮与 `tmzncty/how-people-lived` 的交叉研究正在完成一个明确 Life Horizons 缺口：

> 1995 与 2005 农民工怎样找工作、住在哪里、怎样联系家里、汇钱和决定返乡。

2005 前后的材料出现一个重要边界：

- 国家级 Web 劳动力市场基础设施已经存在；
- 但国务院研究室农民工调查仍显示，受访农民工主要依靠亲戚、熟人和地缘网络寻找工作。

因此，中国劳动力市场网是一个很合适的 old-Web archaeology 对象：

> **它可以帮助区分“在线岗位信息存在”与“一个普通迁移劳动者已经主要靠 Web 找到工作”。**

这不是要再写一篇“网络招聘 state gap”总论，而是验证一个具体早期公共就业站点究竟留下了什么 artifact。

---

# 2. 研究单位

```yaml
subject: 中国劳动力市场网
research_unit: site/host plus historical page locators; not a verified capture
historical_host: www.lm.gov.cn
period_of_interest: 2002-2006
scope: Chinese public labor-market information / employment information infrastructure
m1_status: NOT ACHIEVED
```

必须区分：

```text
中国劳动力市场网这个站点/品牌存在
!=
某个历史 URL 曾存在
!=
该 URL 被 archive 抓取
!=
本轮实际打开并核验了 capture
!=
普通农民工在当时实际使用该页面找到了工作
```

---

# 3. 已确认：2006 年官方文件明确把 `www.lm.gov.cn` 当作全国网上招聘平台

教育部 2006 年 6 月 22 日的正式网页说明，教育部、人事部、劳动和社会保障部共同举办高校毕业生网上联合招聘活动，由：

- 中国高校毕业生就业服务信息网；
- 人事部人才市场公共信息网；
- **中国劳动力市场网 `www.lm.gov.cn`**；
- 各地就业服务机构网站；

共同承办。

页面进一步说，活动期间三家网站开通统一招聘页面，免费发布招聘信息，供用人单位和毕业生浏览、查询与在线联系。

来源：

- 中华人民共和国教育部，2006-06-22：
  https://www.moe.gov.cn/jyb_xwfb/gzdt_gzdt/moe_1485/tnull_15632.html

证据等级：**A（同期官方网页）**。

它可以直接支持：

- `www.lm.gov.cn` 在 2006 年作为“中国劳动力市场网”公开使用；
- Web 浏览 / 查询 / 在线联系确实是其公共就业信息功能的一部分；
- 它与地方就业服务网站被放在一个公共就业信息体系中。

它不能支持：

- 2002 或 2005 的页面外观；
- 站点 2006 年全部栏目结构；
- 普通农民工使用率；
- 是否必须登录；
- 简历投递究竟完全站内完成还是转交线下 / 邮件；
- charset、DOM、脚本和浏览器环境。

---

# 4. 已确认：2004 年同期报道把该站列为劳动保障部公共服务网络平台

2004 年 12 月中国新闻网的一篇同期报道解释劳动和社会保障部“新职业”发布流程，并明确写道：

- 新职业公示和发布的公共服务网络平台包括：中国劳动力市场网 `www.lm.gov.cn`；
- 另一个平台是国家职业资格工作网。

来源：

- 中国新闻网 / 新浪财经，2004-12-02：
  https://finance.sina.com.cn/MBA/careerdevelop/20041202/22141198359.shtml

证据等级：**B（同期媒体报道，内容描述官方业务）**。

这至少把可证实时间向前推到 2004 年，并说明该站并不只有招聘会功能，还承担劳动市场 / 职业信息公共发布用途。

仍不能由此推断具体页面技术。

---

# 5. 一个很有价值的 historical original URL：2002 数据页

澳大利亚储备银行 2011 年的一篇劳动市场研究在参考文献中保留了劳动和社会保障部门的一条精确 URL：

`http://www.lm.gov.cn/gb/data/2002-09/02/content_3464.htm`

RBA 将其对应到：

> 中国农村劳动力 2000 年就业和流动状况相关材料。

来源：

- Reserve Bank of Australia, *China's Labour Market*, 2011：
  https://www.rba.gov.au/publications/bulletin/2011/sep/4.html

证据等级：**C / locator evidence**。

原因：

- RBA 是可靠的后来研究来源；
- 它保留了精确历史 host + path；
- 但本轮没有实际打开 `lm.gov.cn` 的 2002 原始页面或 archive capture。

所以应记录成：

```yaml
historical_original_url_candidate:
  url: http://www.lm.gov.cn/gb/data/2002-09/02/content_3464.htm
  locator_source: Reserve Bank of Australia reference list, 2011
  original_page_opened: false
  archived_capture_opened: false
  evidence_role: historical URL locator only
```

不能写成：

> “已恢复 2002 年中国劳动力市场网页面。”

---

# 6. URL 形态本身只作为候选技术线索，不升格为技术结论

上面的历史路径包含：

```text
/gb/data/2002-09/02/content_3464.htm
```

后来学术引用还保存过类似的 `lm.gov.cn/gb/...` 路径。

这个 pattern 可以帮助以后搜索 archive，但当前只能写：

- `gb` 路径真实出现在历史引用中；
- 页面使用 `.htm` 扩展名的历史 URL locator 存在。

不能据此推断：

- 后端语言；
- 静态 HTML / 动态生成；
- GB2312 / GBK charset；
- ASP / JSP；
- IIS / Apache；
- IE-only；
- frameset；
- ActiveX。

以上全部保持 **UNKNOWN**。

---

# 7. 本轮 archive probe 结果

本轮对公开 Web 索引进行了针对性搜索，包括：

- `"web.archive.org" "lm.gov.cn" "中国劳动力市场网"`
- `"web.archive.org/web" "www.lm.gov.cn"`
- `"lm.gov.cn" "Wayback"`

结果：

```yaml
archive_locator_found_in_this_run: false
verified_capture_opened: false
failure_class:
  - no_archive_locator_returned_by_current_public_search_index
m1_status: NOT ACHIEVED
```

这里的措辞非常重要。

本轮**没有**证明：

- Internet Archive 没有抓过 `lm.gov.cn`；
- 2002 页面已经永久丢失；
- Common Crawl / ArchiveTeam / 其他档案源没有记录。

只证明：

> **在本轮可用的公开搜索入口中，没有取得可以实际跟入并检查的 archive locator。**

按照 `docs/METHOD.md`，这是一个负的研究结果，不是历史不存在证据。

---

# 8. 当前 artifact 字段状态

```yaml
archive_source: UNKNOWN
capture_url: UNKNOWN
original_url:
  host: http://www.lm.gov.cn/
  exact_candidate: http://www.lm.gov.cn/gb/data/2002-09/02/content_3464.htm
capture_datetime: UNKNOWN
accessed_at: 2026-09-12
replay_status: NOT_OBSERVED
http_status: UNKNOWN
content_type: UNKNOWN
charset: UNKNOWN
page_title: UNKNOWN
redirect_state: UNKNOWN
login_boundary: UNKNOWN
dom_structure: UNKNOWN
forms: UNKNOWN
javascript_dependencies: UNKNOWN
css_subresources: UNKNOWN
image_subresources: UNKNOWN
browser_assumption: UNKNOWN
plugin_assumption: UNKNOWN
archive_rewrite_effects: UNKNOWN
second_verified_timepoint: NONE
```

这意味着该对象距离 M1 仍然很远。

---

# 9. 生活史交叉线：为什么 Web 的存在不能代替实际求职路径证据

国务院研究室 2005 年启动并于 2006 年发布的农民工调查，经新华社同期报道，受访者找工作的主要渠道为：

- 熟人 / 亲戚介绍：60.37%；
- 中介机构介绍：14.20%；
- 自己应聘：12.10%。

来源：

- 新华社 / 新浪，2006-04-16：
  https://news.sina.com.cn/c/2006-04-16/09278708721s.shtml

这和 `www.lm.gov.cn` 的存在并不矛盾。

它们描述的是两个不同层级：

```text
PUBLIC WEB EMPLOYMENT INFRASTRUCTURE EXISTS
!=
MIGRANT WORKER CAN ACCESS IT
!=
MIGRANT WORKER USES IT
!=
IT IS THE DOMINANT SEARCH CHANNEL
!=
A JOB IS ACTUALLY OBTAINED THROUGH IT
```

这也是旧网保存偏差会特别严重的地方。

二十年后：

- 公共网页可能被 archive 保存；
- 政府新闻稿可能仍在；
- URL 可能仍被论文引用；

但以下东西几乎不会留下同等清晰的 Web 证据：

- 一个老乡口头告诉另一个人“厂里还招人”；
- 两个人一起坐火车去广东；
- 到劳动力市场现场排队；
- 工厂门口直接报名；
- 亲友替新来者安排第一晚住宿。

因此：

## **Web survival / interpersonal-infrastructure invisibility bias**

公共就业站点在 archive 中的可见性，不能直接用来估计它在普通农民工实际求职中的相对份量。

---

# 10. 这和“Internet 前史 / 大众化”边界怎样连接

这个对象还帮助防止另一种错误时间线：

> “1994 正式接入 Internet → 2000s 大家已经主要在线找工作”。

实际证据更像：

```text
劳动力跨省移动早已大规模发生
↓
熟人、亲属、劳务输出、现场职业介绍构成主要信息网络
↓
公共部门逐步建立国家 / 地方 Web 劳动力市场页面
↓
Web 成为新增的岗位信息与公共服务入口
↓
不同群体以不同速度把在线信息真正整合进求职行动
```

因此 Internet 的影响不能只按“网站上线日”分期。

至少要再问：

- 谁能上网？
- 在哪里上网？
- 她知道这个网站吗？
- 网站上的岗位和她的技能 / 地域匹配吗？
- 联系招聘方后，后续是否仍然线下进行？
- 一个亲友介绍是否比 Web 信息更可信、还顺带提供住宿和同行？

---

# 11. 已证实 / 高概率 / 不知道

## 已证实

- `www.lm.gov.cn` 在 2004 年同期报道中已作为劳动保障公共服务网络平台出现。
- 2006 年教育部正式网页明确把 `www.lm.gov.cn` 称为中国劳动力市场网，并用于全国网上联合招聘。
- 后来高质量研究保留了精确的 2002 historical original URL：`http://www.lm.gov.cn/gb/data/2002-09/02/content_3464.htm`。
- 2005 前后农民工求职仍高度依赖亲友 / 熟人网络；网站存在不能等同于主导使用渠道。

## 高概率，但本轮不升格为 verified artifact claim

- `www.lm.gov.cn` 在 2002 前后已经承载农村劳动力就业 / 流动统计或政策材料。
- `/gb/.../content_####.htm` 是当时站点真实使用过的 URL 路径模式之一。

## 不知道

- 2002 页面的历史 HTML；
- 2002 / 2004 / 2005 / 2006 首页布局；
- charset；
- DOM；
- CSS / 图片 / JS 子资源；
- 是否 frameset；
- 浏览器兼容要求；
- 求职者 / 单位账户模型；
- 站内职位搜索字段；
- 站内申请是否存在；
- 联系是否跳转电子邮件 / 电话 / 地方职业介绍机构；
- archive 是否有多个可用时间点；
- 页面在不同年份怎样变化。

---

# 12. 下一次 artifact verification 的优先顺序

1. 直接用 Internet Archive CDX / Wayback URL 查询 `www.lm.gov.cn` 和精确 2002 path，而不是只依赖通用搜索引擎。
2. 查询至少以下 URL：
   - `http://www.lm.gov.cn/`
   - `http://www.lm.gov.cn/gb/`
   - `http://www.lm.gov.cn/gb/data/2002-09/02/content_3464.htm`
3. 若找到 candidate capture，实际打开主文档并记录：
   - capture URL；
   - original URL；
   - capture datetime；
   - replay / HTTP 状态；
   - title；
   - Content-Type / charset（能可靠观察时）；
   - 重定向 / 错误 / robots / login 状态。
4. 单独列主 HTML 与 CSS / 图片 / JS 子资源的 survival。
5. 至少再找一个 2004–2006 时点，以满足跨时点比较需要。
6. 找同期用户教程 / 截图作为第二 evidence family。
7. 在没有旧浏览器验证前，不写 IE-only / ActiveX / GBK 等结论。
8. 不碰普通个人求职账号或隐私数据；研究站点公共结构即可。

---

# 13. 对 M1 的结论

这次**没有完成**一个 M1 case。

它推进的是更小但可复核的一步：

```text
site identity partially confirmed
+
historical host confirmed
+
exact historical original URL candidate recovered
+
contemporaneous official use confirmed
+
archive search negative result recorded
+
all technical fields kept UNKNOWN where capture is absent
```

当前最准确的总结是：

> **中国劳动力市场网在 2000s 前半确实属于公共就业 Web 基础设施；本轮已恢复若干历史 URL 与同期官方使用证据，但没有实际核验历史 archive capture。**

而对 ordinary-life 项目最重要的一点是：

> **网站已经存在，与一个迁移劳动者实际依靠什么找到下一份工作，是两个不同的问题。**

---

*研究记录由 OpenAI GPT-5.6 Sol 辅助整理；未取得的历史 artifact 明确保留为 UNKNOWN，不以年代刻板印象补齐。*