# Labor-rights portals, hotlines, arbitration guidance, and claim-state gaps, 2003–2015

> Scope: 中文旧网约 1995–2015。
>
> 本文不写中国劳动法通史，也不把 2020s 在线仲裁倒推回旧 Web。研究对象是：2003–2015 年中文 Web 怎样把劳动保障法规、热线、办事指南、仲裁表格、在线咨询、投诉举报和劳动争议程序呈现在页面上，以及 archive 最容易保存哪些壳层、最难保存哪些真实 claim state。
>
> Cross-link: `tmzncty/how-people-lived/topics/from-labor-rights-information-to-claim-executability-workplace-disputes-evidence-and-employment-exit-china-1993-2026.zh-CN.md`

## 1. 为什么这不是 `CONSUMER_COMPLAINT_*` 的重复

消费者投诉模型研究的是：

`商品/服务争议 → 投诉平台 → 企业/监管转办 → remedy`

劳动争议至少还多出几层特殊状态：

- 先判断是否存在劳动关系；
- 区分劳动监察、政策咨询、调解、仲裁、诉讼；
- 识别管辖机构；
- 遵守仲裁时效；
- 提交劳动合同、工资、考勤、工伤、解除通知等证据；
- 可能先仲裁、再法院；
- 离职后企业账号/工作群可能关闭，影响证据取得。

因此不能把一个页面上的“投诉举报”“在线咨询”“劳动仲裁”三个词当成同一个 transaction。

核心边界：

- `legal information exists ≠ individual advice rendered`；
- `online consultation ≠ formal complaint`；
- `complaint accepted ≠ labor arbitration filed`；
- `arbitration form downloadable ≠ arbitration application submitted online`；
- `application submitted ≠ case accepted`；
- `case accepted ≠ hearing held`；
- `award issued ≠ money actually paid`；
- `public case/article exists ≠ authenticated private case state archived`。

---

## 2. 研究单位

按照 `docs/METHOD.md`，本题至少分开：

### platform / service family

- 12333 劳动保障/人力资源社会保障公共服务体系；
- 上海劳动保障服务网 / 上海 12333 portal；
- 地方劳动保障部门页面；
- 劳动法专业信息/咨询站，如 `laodongfa.com`；
- 媒体/论坛里的劳动权利问答与经验帖。

### site / host

同期材料已经可以定位：

- `www.12333sh.gov.cn` — 2008–2010 同期材料明确称为上海劳动保障/人社政府网站；
- `www.12333.gov.cn` — 2005–2006 上海官方年报使用过这个 URL；后来的全国 12333 体系也使用 `12333.gov.cn`，因此**不能把不同年份同一字符串自动视为同一主体/同一后端**；
- `www.laodongfa.com` / `laodongfa.com` — 2006 年已有同时代机构材料证明“劳动法苑”域名在使用。

### page / URL

需要分别找：

- 法规/政策页面；
- 办事指南；
- 仲裁申诉书下载页；
- online Q&A / 嘉宾在线；
- 劳动监察举报入口；
- 仲裁公告；
- 智能咨询；
- 可能的投诉/留言表单；
- 认证后的个人案件页面（若历史上存在）。

### transaction / claim state

即使页面同属一个 host，也必须把：

`read → download → ask → report → apply → accepted → evidence complete → hearing → award → remedy/execution`

作为不同状态。

---

## 3. 2003：12333 首先是电话基础设施，不是 Web 产品

原劳动保障部 2003-05-27 文件明确：全国劳动保障电话咨询服务专用号码为 `12333`，目标是提供统一公共咨询入口，使公众更方便了解政策和办事程序。

### 可证实

- 2003 年全国统一号码制度存在；
- 它首先是电话咨询体系；
- Web、短信、App、小程序是后来叠加的媒介。

### 不能推出

- 2003 年已经存在全国统一 Web 劳动争议立案系统；
- 12333 电话可以直接替代劳动仲裁；
- 全国各地同年部署程度一致。

### Evidence

- A：原劳动保障部《关于开展劳动保障电话咨询服务的通知》，2003-05-27：<https://www.mohrss.gov.cn/xxgk2020/fdzdgknr/zhgl/rlzyshbzxxh/202010/t20201031_394105.html>

---

## 4. 2005–2006 上海：旧 Web 已经是政策/办事入口，但仍是明显 hybrid system

### 4.1 2005 年官方年报留下的页面结构线索

上海市劳动和社会保障局 2005 年政府信息公开年报称，“上海劳动保障服务网”改版后形成：

- 信息服务台；
- 办事大厅；
- 互动社区。

年报还记录：

- 社保网上办事项目；
- 新闻、通知、咨询电话；
- **仲裁公告约 650 条**；
- 12333 电话全天候服务；
- 增设劳动监察网络受理、社会保险查询、网上信访处理等服务。

这足以证明：

> 2005 年上海劳动保障 Web 已经不是纯静态法规陈列页，而是一个包含信息、部分 transaction、互动和公告的混合门户。

但不能把“劳动监察网络受理”写成“劳动争议仲裁网上立案”。监察与仲裁是不同程序。

### Evidence

- A：上海市劳动和社会保障局 2005 年政府信息公开年报：<https://rsj.sh.gov.cn/txxgknb_17198/20200617/t0035_1372757.html>

### 4.2 2006 年：网站出现“维权”资讯、在线解答；真实仲裁仍要求纸面申诉

2006 年年报称网站形成“办事大厅 / 新闻中心 / 资讯服务 / 互动社区”，资讯中明确包含“维权”；同年有在线解答和网上新闻发布会。

但 2006 年同期仲裁办事报道仍写得非常清楚：

- 空白仲裁申诉书可以从上海劳动保障服务网下载打印；
- 也可以去仲裁委员会现场领取；
- 正式申请需提交书面仲裁申诉书及副本；
- 政策咨询另走 12333 或网站。

因此一个历史页面上的“下载申诉书”只能支持：

`form distribution moved partly online`

不能支持：

`formal filing moved online`。

### Evidence

- A：上海 2006 年政府信息公开年报：<https://rsj.sh.gov.cn/txxgknb_17198/20200617/t0035_1372758.html>
- B：新闻晨报 2006-08-26，“社保缴费争议可就近申请仲裁”：<https://news.sina.com.cn/o/2006-08-26/08309852797s.shtml>

---

## 5. `12333.gov.cn` / `12333sh.gov.cn`：同名与迁移本身就是考古问题

本题出现一个值得单独登记的 host-identity risk。

### 同期材料

- 上海 2005、2006 年官方年报把政府网站写作 `http://www.12333.gov.cn`；
- 2008、2009、2010 的上海同期/官方材料则明确使用 `http://www.12333sh.gov.cn`；
- 2020s 全国人社公共服务又使用 `12333.gov.cn` 相关 host。

### 因此禁止

不能看到今天的 `12333.gov.cn`，就直接认为：

- 今天主体 = 2005 上海主体；
- URL ownership 从未变化；
- backend/database 连续；
- 2005 的页面可通过今天路径推回。

### 应建立的 genealogy questions

1. `12333.gov.cn` 2003–2007 的注册/主体/解析记录；
2. 上海何时稳定切换到 `12333sh.gov.cn`；
3. 旧 URL 是否 redirect；
4. redirects 是否被 archive 保存；
5. 两 host 是否共享内容或只是品牌连续；
6. 今天全国 host 取得该域名的时间点；
7. 搜索引擎旧链接在迁移期如何表现。

这正属于本仓的“域名、站点谱系、主体连续性”核心问题，而不是普通政策史。

---

## 6. 2006–2008：专业劳动法站点形成另一类 information layer

上海律师行业的 2006 年同期材料已经把“劳动法苑”直接写成 `laodongfa.com`，说明至少当时该域名/品牌已用于劳动法信息与专业活动传播。

今天 `laodongfa.com` 仍有服务咨询页面，但**今天页面存在不能证明 2006 年的页面结构、导航、咨询机制或内容连续性**。

### 需要区分

- government rights information；
- lawyer/firm-authored legal information；
- public forum/Q&A；
- paid professional consultation；
- formal administrative or arbitral submission。

一个劳动者通过搜索引擎找到律师写的解释，并不等于：

- 他已经获得个案法律意见；
- 仲裁机构接受该解释；
- 该站点能替他提交仲裁。

### Evidence

- B / 同时代行业材料：上海市律师协会，2006-04-13，明确出现“劳动法苑 laodongfa.com”：<https://www.lawyers.org.cn/info/43457beeb37f4231a07bd1be252848d1>
- current locator only：<https://www.laodongfa.com/service.html>

---

## 7. 2008：一个站点可以同时承载“浏览、办事、咨询、评议、投诉”，但这些仍不是一个状态

2008 年上海同期报道把 `www.12333sh.gov.cn` 描述为“一门式网上便民服务”，列出：

- 浏览；
- 查询；
- 办事；
- 咨询；
- 评议；
- 投诉举报。

从 Web archaeology 角度，这类新闻非常容易诱发过度复原：看到“一门式”，就假设所有事务已经共享一个统一账号、统一表单、统一 backend。

正确做法是建立功能矩阵：

| visible label | historical transaction still unknown |
|---|---|
| 浏览 | 静态页还是数据库查询 |
| 查询 | 是否实名、是否动态、查询对象是什么 |
| 办事 | 哪些事项可以完成，哪些只是表格/指南 |
| 咨询 | guestbook、email、实时聊天还是后台工单 |
| 评议 | 是否实名、是否公开 |
| 投诉举报 | 监察举报还是劳动仲裁；是否生成编号 |

### Evidence

- B：新民晚报，2008-10-24：<https://news.sina.com.cn/o/2008-10-24/152514625131s.shtml>

---

## 8. 2009–2010：电话、email、Web 和智能咨询共同增加，仍不能把“信息交互”写成“争议裁决在线化”

上海 2009 年官方年报记录：

- 12333 全年接听近 1800 万来电；
- 受理电子邮件 2 万余封；
- 电话受理劳动监察举报 1 万余件。

2010 年官方年报又记录：

- 12333 继续处理大量电话、email、劳动监察举报；
- 上线“12333在线智能咨询”试验版；
- 编印劳动争议案例汇编。

因此 2010 年前后可以明确观察到：

`phone Q&A + email + web information + intelligent Q&A prototype + offline/formal dispute institutions`

共同存在。

这是一种 **channel accumulation**，不是旧入口被新入口线性替代。

### Evidence

- A：上海 2009 年政府信息公开工作年度报告：<https://www.shanghai.gov.cn/nw24535/20200820/0001-24535_21468.html>
- A：上海 2010 年政府信息公开工作年度报告：<https://www.shanghai.gov.cn/nw25513/20200820/0001-25513_25128.html>

---

## 9. 2012–2013：Web 之外，政务微博又成为“网站延伸”

上海 2012、2013 年政府信息公开年报把“上海12333”政务微博明确称为政府网站的延伸，并记录大量发布与回应。

这意味着旧 Web 末期出现新的 channel handoff：

`government portal → portal + Sina/Tencent/etc. social platforms`

从档案角度必须把两者分开：

- portal page 的 URL 生命周期；
- 微博 post/account 的平台生命周期；
- 评论/问答是否仍公开；
- 微博回答是否只是一般政策信息；
- 是否被截图/转载后脱离原上下文。

不能因为微博回复了一个“劳动仲裁怎么走”的问题，就把它当正式案件 submission。

### Evidence

- A：上海 2012 年政府信息公开工作年度报告：<https://www.shanghai.gov.cn/nw31041/20200820/0001-31041_35103.html>
- A：上海 2013 年政府信息公开工作年度报告：<https://www.shanghai.gov.cn/nw31917/20200820/0001-31917_38306.html>

---

## 10. 本题建议的 state machine

```text
worker experiences a workplace problem
    ↓
problem recognized as possibly rights-related
    ↓
finds information source
    ├─ newspaper / leaflet / union / community
    ├─ 12333 phone
    ├─ government website
    ├─ lawyer / labor-law website
    └─ forum / search engine / social media
    ↓
identifies institution / jurisdiction
    ↓
chooses route
    ├─ policy consultation
    ├─ labor inspection complaint/report
    ├─ mediation
    ├─ labor arbitration
    └─ later court action
    ↓
obtains form / instructions
    ↓
collects identity + employment + claim evidence
    ↓
submission attempt
    ↓
server / email / hotline / counter receives artifact
    ↓
formal acceptance decision
    ↓
case ID / notice / request for supplementation
    ↓
hearing / mediation
    ↓
award / settlement
    ↓
payment / reinstatement / social-insurance correction / other remedy
    ↓
actual closure
```

任何 archive artifact 最多只能证明链条中的一部分。

---

## 11. 必须单独记录的 state gaps

### 11.1 Information-to-procedure gap

能读到法规 ≠ 知道自己属于哪个程序。

### 11.2 Download-to-filing gap

能下载仲裁申诉书 ≠ 能在线提交仲裁。

### 11.3 Consultation-to-case gap

online Q&A / 12333 回复 ≠ 正式案件已经成立。

### 11.4 Complaint-route gap

“劳动监察举报”与“劳动争议仲裁”不能合并成一个“投诉”。

### 11.5 Submission-to-acceptance gap

email/form/留言成功发送 ≠ 仲裁机构依法受理。

### 11.6 Public-guide/private-evidence gap

公开网页可能完整保存办事指南，但真正案件依赖：

- 劳动合同；
- 工资单；
- 考勤；
- 身份证；
- 工伤材料；
- 解除通知；
- 企业内部记录。

这些大多在认证/线下/私人环境中，不会进入 public archive。

### 11.7 Award-to-remedy gap

公开仲裁公告或案例摘要 ≠ 当事人最终收到钱。

### 11.8 Domain-identity gap

`12333.gov.cn` 同一个 hostname 字符串跨年份不必然对应同一个网站主体或技术系统。

### 11.9 Social-media-answer gap

2012–2013 以后政务微博问答 ≠ 正式法律意见/案件受理。

---

## 12. 保存偏差

### 12.1 Public-rights-shell / private-claim-state asymmetry

最容易保存：

- 法规；
- FAQ；
- 办事指南；
- 电话号码；
- 表格下载；
- 仲裁公告；
- 政策新闻；
- 一般性 online Q&A。

最难保存：

- 身份验证；
- 真实仲裁申诉书；
- 附件上传；
- 劳动合同/工资/考勤；
- 私人 email；
- hotline call content；
- backend routing；
- 是否补材料；
- hearing scheduling；
- 最终付款。

这会让后来的研究者误以为旧劳动保障 Web “信息很多，所以办事也一定很完整”。

### 12.2 Success-case visibility bias

政府/媒体更容易留下：

- 成功调解；
- 追回工资；
- 典型胜诉；
- 新平台上线。

更难留下：

- 问了以后没继续；
- 过了时效；
- 管辖搞错；
- 材料不足；
- 中途放弃；
- 裁决后仍未执行。

### 12.3 Static-policy survivorship bias

法规、通知、年度报告作为静态文档非常容易迁站后继续存活；真正的动态办事页、表单、数据库查询和认证后页面更容易消失。

因此：

`current official page carrying 2006 text ≠ 2006 original web presentation`。

### 12.4 Hotline invisibility

12333 对普通生活可能比网页更重要，但电话通话天然比 Web 页面更难被公共 archive 保存。

只做网页考古会系统性低估电话在 2000s 劳动权利基础设施里的份量。

---

## 13. Browser / encoding / transaction questions for future M1 work

如果以后取得 2005–2010 `12333sh.gov.cn` 或相关站点 capture，至少检查：

### HTTP / character encoding

- `Content-Type`；
- GB2312 / GBK / UTF-8；
- archive rewrite 是否改变 charset；
- 中文表格字段是否乱码。

### Page structure

- frameset / table layout；
- 左侧栏目树；
- 动态 ASP/JSP/PHP endpoint；
- query string；
- downloadable DOC/PDF/XLS 是否单独存档。

### Forms

- `method=GET/POST`；
- action URL；
- 是否依赖 JavaScript；
- captcha；
- 身份证/单位字段；
- 电话/email；
- 是否上传附件；
- submit 后是否有 receipt / case number。

### Sessions

- cookie；
- login requirement；
- session expiration；
- 是否跳到统一认证或不同 host。

### Dynamic result state

- `success` page 是否只是前端提示；
- 是否能证明 backend 接收；
- 是否生成 claim ID；
- 是否能查询处理进度；
- 查询需要哪些 credentials。

### Email / phone handoff

旧 Web 很可能不是 transaction terminal，而只是：

`page → download/phone/email → human handling`

必须保留这种 hybrid route，而不是为了叙事整齐把它强行改写成纯 Web workflow。

---

## 14. M1 检查：本轮仍是负结果

本轮明确定位了：

- `www.12333sh.gov.cn`；
- 早期官方材料中的 `www.12333.gov.cn`；
- `laodongfa.com`；
- 2005–2010 上海网站功能、电话、email、online Q&A 的同期官方记录。

并尝试搜索/打开 2006–2008 的 Wayback locator，但**没有在本轮实际取得并检查一份满足 M1 要求的历史 transaction capture**。

因此以下内容一律保持 `unknown`：

- 2005/2006 原始首页 DOM；
- historical charset；
- “劳动监察网络受理”具体 form action；
- 仲裁公告 URL pattern；
- online Q&A backend；
- captcha；
- cookie/session；
- 申诉书下载实际文件；
- 是否生成投诉编号；
- authenticated case status；
- 数据库/人工转办 handoff。

**正确结论是“本轮未验证成功”，不是“Wayback 没有”。**

搜索引擎没有返回 archive result、以及直接构造 Wayback URL 未能作为可核验 memento 打开，都不足以作为 capture 不存在的证据。

---

## 15. Privacy boundary

劳动争议材料往往同时包含：

- 身份证信息；
- 手机号；
- 家庭住址；
- 健康状况；
- 工资；
- 公司内部沟通；
- 普通劳动者姓名与账号。

因此未来即使找到旧论坛、投诉或仲裁相关页面：

- 优先抽象 URL pattern；
- 不重新扩散普通人的联系方式；
- 不批量恢复已删除个人案件；
- 技术结构可以研究，私人证据不因 archive 可访问就自动适合重新公开。

---

## 16. 与 `how-people-lived` 的交叉结论

这条旧 Web 证据链改变了一个很容易被现代 UI 误导的判断。

不能写：

> “有了劳动保障网站以后，劳动者可以网上维权。”

应该拆成：

> **2000s 中文 Web 首先大幅提高了法律、办事指南、仲裁表格、机构地址与咨询入口的可寻址性；电话和 Web 一起减少‘我到底该问谁’的成本。但一个真实劳动争议仍然要跨过管辖、证据、纸面提交、受理、开庭、裁决和实际履行等多个状态。旧网页最容易留下的是权利的公开壳层，恰恰最难留下普通劳动者有没有真正把一份坏工作结清。**

这也是为什么 `how-people-lived` 需要把“能换工作”进一步拆成“能离开工作场所”与“能结清旧劳动关系”。

---

## 17. Evidence inventory

| Claim | Evidence | Grade | Confidence |
|---|---|---:|---:|
| 12333 2003 年作为全国统一电话咨询号码启用 | 原劳动保障部文件 | A | high |
| 2005 上海劳动保障网已有办事/互动、仲裁公告等 | 2005 官方年报 | A | high |
| 2005 上海已有劳动监察网络受理等服务 | 2005 官方年报 | A | high for official claim/existence |
| 2006 网站有维权资讯、在线解答 | 2006 官方年报 | A | high |
| 2006 仲裁申诉表可网上下载但正式申请仍为书面提交 | 同期新闻操作说明 | B | medium-high |
| 2008 `12333sh.gov.cn` 被描述为一门式服务入口 | 同期新民晚报 | B | high for advertised capability |
| 2009 电话、email、劳动监察举报并存 | 官方年报 | A | high |
| 2010 有在线智能咨询试验版 | 官方年报 | A | high |
| 2012–2013 政务微博被作为网站延伸 | 官方年报 | A | high |
| 2006 `laodongfa.com` 已作为劳动法苑域名使用 | 上海律协同期材料 | B/A-like institutional contemporaneous | high for locator |
| 任一 2005–2010 劳动争议 Web transaction 已被本轮 archive capture 验证 | none | — | **not established** |

---

## 18. 下一步优先级

1. 找 `12333sh.gov.cn` 2005–2010 capture index，而不是只搜今天迁站后的年度报告；
2. 核对 `12333.gov.cn` → `12333sh.gov.cn` 的 host ownership / redirect genealogy；
3. 找一个真实“表格下载 → 线下仲裁”的历史页面和附件文件；
4. 找一个 online Q&A page，确认是否 static archive、guestbook、ASP/JSP dynamic page；
5. 找一条“劳动监察网络受理”的真实 form capture；
6. 检查 `laodongfa.com` 2006–2010 的首页、栏目、论坛/咨询入口及 charset；
7. 主动寻找失败状态：dead link、submit error、过期表格、旧电话号码、迁站后的 broken deep link；
8. 若取得 authenticated/private-like artifact，先做隐私审查，再决定是否只记录 metadata。

---

## AI-assisted research note

初稿由 AI 辅助检索与整理。没有把当前 live page 当 historical capture，也没有把新闻中的“网上办事/维权”概括为“全流程网上仲裁”。本轮 archive transaction 仍是明确负结果。
