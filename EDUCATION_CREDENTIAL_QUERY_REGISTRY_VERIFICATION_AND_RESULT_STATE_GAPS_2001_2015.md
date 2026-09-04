# EDUCATION_CREDENTIAL_QUERY_REGISTRY_VERIFICATION_AND_RESULT_STATE_GAPS_2001_2015

## Scope

本说明研究约 2001–2015 中文 Web 中一类很容易被后来的“学信网一查就知道”叙事压平的对象：

**高等教育学历电子注册、网上查询、学历认证、本人档案与在线验证，怎样把一张纸质学历证书背后的制度事实变成可从 Web 访问的数据库状态。**

本说明严格保持 `old-web-archaeology` 的仓库边界：

- 研究中文旧 Web 的页面、系统、状态和保存问题；
- 2001 以前只作为理解 2001 转折所必需的前史；
- 2015 以后只在“今天为何不能用当前页面倒推旧系统”时作边界说明；
- 普通人为什么考证、学历怎样影响职业未来，写回 `tmzncty/how-people-lived`。

本说明不是学历政策史，也不尝试保存普通人的历史学历记录。

---

## 1. 研究单位：一个“查询结果”至少横跨五种对象

学历查询系统至少包含：

```text
credential event
→ paper certificate / school record
→ issuer-side record
→ provincial registration/review
→ national registry/database
→ public or authenticated Web query
→ query input state
→ backend match
→ result page/report
→ verifier interpretation
→ downstream decision
```

因此必须固定以下规则：

> **paper diploma exists ≠ registry record exists**

> **registry record exists ≠ current public query can retrieve it**

> **query form exists ≠ historical backend still executes**

> **query submitted ≠ backend matched a record**

> **matching record ≠ current user is the credential holder**

> **verification report exists ≠ report remains valid/current**

> **credential verified ≠ credential satisfies this job/exam/school requirement**

> **credential verified ≠ holder has the practical competence implied by readers**

对 old-web archaeology 而言，最危险的跳跃通常发生在：

```text
archived page
→ imagined backend state
→ imagined real person
```

---

## 2. 2001 的关键边界：Web 查询前台并不代表后台已经“全在线”

### A 级来源

教育部 2001 年《高等教育学历证书电子注册管理暂行规定》明确：

- 学历证书注册运用现代信息技术，实行计算机网络管理；
- 各省级教育行政部门审核注册；
- 教育部审核备案后进入全国高等教育学历证书档案库；
- 备案记录供社会网上查询。

来源：

<https://www.moe.gov.cn/s78/A15/xss_left/moe_779/s3263/201006/t20100602_88643.html>

但同年的实施通知同时说明：研究生、成人高等教育相关管理软件当时尚未全部完工，数据先按规定数据库结构**用软盘**向省级教育行政部门申报。

来源：

<https://www.moe.gov.cn/jyb_xxgk/gk_gbgg/moe_0/moe_7/moe_12/tnull_5937.html>

因此本仓必须增加：

## upstream-ingest gap

```text
school has credential data
→ local software exports data
→ physical/digital media transfer
→ provincial intake
→ validation
→ national intake
→ registry publication
```

一张 Web 查询页面只属于这条链最末端。

不能从：

> “2001 已有网上查询”

推出：

> “2001 所有学校到国家库已经是实时网络 API”。

### 考古含义

即使未来获得 2001 查询首页的完整 capture，也仍然可能完全看不到：

- 学校端软件；
- 数据库结构；
- 软盘报送；
- 省级审核工具；
- 纠错/补报流程；
- 从注册到发布的延迟。

这类后台历史需要规章、操作手册、软件介质或机构档案补证，而不是从前台 HTML 猜。

---

## 3. registration state 必须与 certificate state 分开

2001 规章还明确规定，从 2001 年起颁发的毕（结）业证书未经注册，国家不予承认；漏报、错报还存在修正程序。

因此至少应建模：

```yaml
credential:
  issued: true|false|unknown
  issue_date: ...
  issuer: ...

registration:
  submitted: true|false|unknown
  provincial_reviewed: true|false|unknown
  national_recorded: true|false|unknown
  corrected: true|false|unknown
  published_to_query: true|false|unknown
```

不能把：

```text
手中有一张纸
```

和：

```text
全国登记系统存在对应有效记录
```

合成一个布尔值。

### 新增：registration lag gap

不同时间至少要区分：

```text
qualification completion date
certificate issue date
registration submission date
registry publication date
archive capture date
query execution date
```

同一个人已经拿到证书而网上暂时查不到，在 2010 年以前不是理论状态，而是官方后来明确承认曾长期存在的日常延迟。

---

## 4. 2002 回登：数据库时间范围不是制度诞生日

学信网官方历史说明称：

- 2001 年实施电子注册；
- 2002 年对 1991–2000 年高等教育学历证书信息开展回登；
- 官方学历认证服务自 2002 年起面向社会。

来源：

<https://www.chsi.com.cn/about/200902/20090209/17223140.html>

<https://www.chsi.com.cn/about/ct14.shtml>

因此必须区分：

```text
record year
registry-system creation year
backfill year
query availability year
```

一个 1997 年的学历记录可以在 2002 以后进入全国数据库。

所以：

> **database contains a 1997 record ≠ public online registry existed in 1997.**

这是一类非常典型的**backfill anachronism**（回填造成的时代错觉）。

### 建议字段

```yaml
record_temporality:
  credential_year: 1997
  electronic_registration_original: false|unknown
  later_backfilled: true|unknown
  first_queryable_date: unknown
  evidence_date: ...
```

---

## 5. 2002 的“纸质认证报告 + 网上验证”是混合证明，不是纸→Web 的直接替代

学信网官方介绍称，中心 2002 年开始学历认证：

```text
申请/材料
→ 数据库与其他材料核查
→ 纸质《中国高等教育学历查询报告》
→ 报告电子注册
→ 报告可在网上查询验证
```

来源：

<https://www.chsi.com.cn/about/ct14.shtml>

2012 年官方服务回顾又把服务体系概括为：

- 网上查询；
- 纸质认证；
- 在线验证。

来源：

<https://www.chsi.com.cn/ycnews/201210/20121031/357939990.html>

因此新增：

## report-object / report-validation gap

需要分开：

```text
historical credential
→ certification application
→ certification adjudication
→ report generated
→ report number/code
→ report registered
→ Web validation page
→ verifier checks report
```

Web 上出现“认证报告可验证”，不意味着：

- 原学历本身一定可以直接公开查询；
- 报告生成无需人工审核；
- 任何人都能申请别人的报告；
- 报告没有版本、有效期、隐私限制。

---

## 6. 2004：“唯一网站”意味着 Web authority 本身成为状态对象

教育部 2004 年公告重申 `www.chsi.com.cn` 为高等教育学历证书查询唯一网站，原因之一是当时互联网上已经出现：

- 名称相近的网站；
- 复制官方内容的网站；
- 与假证销售结合的查询页面。

来源：

<https://hudong.moe.gov.cn/jyb_xxgk/gk_gbgg/moe_0/moe_1/moe_366/tnull_4328.html>

因此旧网考古不能只验证：

```text
page resembles official query page
```

还要验证：

```text
host/domain authority at historical datetime
```

新增：

## authority-host gap

```text
page title says “学历查询”
→ host is chsi.com.cn?
→ host historically controlled by authorized institution?
→ page is official product path?
→ query backend belongs to authoritative registry?
```

### 极重要 stop condition

> **fake query success ≠ registry success**

一个制假站完全可以：

- 模仿 logo；
- 模仿字段；
- 返回“查询成功”；
- 展示伪造记录。

所以 old-web 重建“假学历查询网站”时，不能因为页面结果自洽就赋予它权威数据库身份。

---

## 7. 当前保存的 2004 学信网页：是历史文本证据，不是已验证 archive capture

学信网当前存在一页路径：

<https://www.chsi.com.cn/__/200411/20041126/188.html>

页面标注日期 2004-11-26，标题为“学历网上查询－查询系统”。当前文本解析可观察到：

- 若干 input 控件；
- “姓名中不要留空格”；
- 验证码相关提示；
- 系统可查询 2001–2003 多类国家承认高等教育学历；
- 用户输入相应证书信息可核查手中学历证书真伪。

### 证据定级

本轮定为：

**A-/B+：官方站当前保存的 dated historical page**。

它不是本轮已经独立验证的：

- Wayback memento；
- WARC；
- 2004 原始 HTML 文件；
- 当时浏览器截图。

因此不得据当前页面推断：

```text
original HTML source
original input name
original form method
original form action
original script files
original charset
original CSS
original cookie/session behavior
original HTTP headers
original browser appearance
```

### image-label gap

当前搜索/解析结果显示部分字段标签已经以 `Image` 形式呈现。

如果图像资源未完整保存，后人可能看到：

```text
[Input]
[Input]
[Input]
```

却不知道每个输入框原来对应：

- 姓名？
- 证书编号？
- 验证码？
- 其他字段？

所以：

> **form control survives ≠ field semantics survive.**

必须避免根据今天的查询字段倒填 2004 标签。

---

## 8. query system 的完整状态机

对一个历史学历查询请求，最低模型应为：

```text
1. user reaches correct official host
2. query page loads
3. required assets/labels load
4. user knows required fields
5. inputs pass client/server validation
6. captcha passes
7. request reaches query endpoint
8. backend service is available
9. dataset version at query time contains candidate record
10. input fields match record
11. privacy/access rule permits result
12. backend returns result state
13. result page renders
14. user interprets result
15. verifier accepts result for downstream purpose
```

因此新增以下 gap：

- `host-authority gap`
- `form-semantics gap`
- `captcha gap`
- `query-endpoint gap`
- `backend-availability gap`
- `dataset-version gap`
- `record-match gap`
- `access-policy gap`
- `result-render gap`
- `result-interpretation gap`
- `downstream-acceptance gap`

---

## 9. no-result 不能直接解释成 fake diploma

一个历史查询没有结果，至少可能是：

1. 证书不存在/伪造；
2. 证书存在但未注册；
3. 漏报/错报；
4. 记录后来才回登；
5. 查询年份不在当时系统覆盖范围；
6. 姓名/证书编号输入不匹配；
7. 页面/后台故障；
8. 数据尚未发布；
9. 权限/隐私规则阻止；
10. archive 只保存了表单，没有保存真实查询事务。

所以历史研究中：

> **observed no result ≠ credential false**

必须额外获得制度/学校/认证证据才能提高结论强度。

---

## 10. 2004 数据库规模材料：current database 不是所有页面用户都能搜索的同义词

学信网当前保存的 2004-12-27 页面称，当时全国高等教育学历信息数据库已包括 1991 年以来多类学历信息，截止 2003 年累计入库超过 2500 万人等。

来源：

<https://www.chsi.com.cn/xlrz/ct03.shtml>

即使接受这条官方历史材料，也必须区分：

```text
database has record
≠ public query supports this record class
≠ anonymous query can retrieve it
≠ record fields all publicly visible
≠ all records are equally complete
```

数据库覆盖、公共查询范围、用户身份权限是三个层次。

---

## 11. 2009 “学信档案”：public lookup 与 self-account state 开始分叉

学信网 2012 年官方回顾称，2009 年开通“学信档案”，学生实名注册后可免费查询本人所有学籍学历等信息。

来源：

<https://www.chsi.com.cn/ycnews/201210/20121031/357939990.html>

这使学历 Web 从：

```text
public/third-party query
```

进一步增加：

```text
holder account
→ authenticated personal record view
```

因此新增：

## holder-account gap

```text
credential holder
→ account registration
→ real-name/identity binding
→ login/session
→ account sees record
→ account requests report/verification
```

不能从“学信档案功能存在”推断：

- 某个人当时已经注册；
- 某学历已成功绑定；
- 某次登录成功；
- 某份记录当时已经显示。

同时，公共 archive 对这一层尤其无能为力，因为普通用户登录后的私人页面不应被重新公开。

---

## 12. 2010：credential publication 从 batch lag 进入 near-real-time

教育部 2010 年材料明确称，在此前流程中，毕业生一般取得证书后二至三个月才能在网上查询。

2010 年的在线即时电子注册改为：

```text
school graduation review
→ upload credential data
→ online review
→ online publication
```

并宣传“即传即审即上网”“零时差”。

来源：

<https://www.moe.gov.cn/jyb_xwfb/gzdt_gzdt/moe_1485/201006/t20100625_90052.html>

<https://www.moe.gov.cn/jyb_xwfb/gzdt_gzdt/moe_1485/201008/t20100816_93954.html>

新增：

## publication-latency gap

一个 2007 年毕业证页面与 2011 年毕业证页面不能默认使用同样的“证书签发→可查询”延迟模型。

如果个人博客写：

> “毕业证已经拿到了，但网上还查不到”

在 2008 和 2012 的制度背景含义可能不同。

---

## 13. “即时”也不是绝对事务一致性

“零时差”是制度/服务目标和同期官方表述。

考古上不能因此写：

```text
certificate print timestamp == registry commit timestamp == globally queryable timestamp
```

仍需区分：

- 学校审核完成；
- 数据上传；
- 省/中央审核状态；
- 数据库提交；
- 查询索引更新；
- public endpoint 读取；
- 缓存；
- 页面结果。

没有事务日志时，archive 不能证明秒级一致性。

---

## 14. verification report 是一个有生命周期的 Web object

2012 年学信网已把“在线验证”列为三种验证模式之一。

当前系统中又存在：

- 《教育部学历证书电子注册备案表》；
- 《教育部学籍在线验证报告》；
- 验证码/在线验证入口。

对 2009–2015 旧网研究，建议建立：

```text
holder requests verification report
→ report generated
→ report code / URL exists
→ validity interval
→ verifier opens verification endpoint
→ backend validates code
→ report displayed
→ holder may extend/re-request
```

新增：

## report-validity gap

一张历史截图显示“验证报告”不等于：

- 验证码在截图之后仍有效；
- 报告未被延长/替换；
- 当前系统仍能查相同 code；
- 截图没有被伪造。

因此不建议仓库保存普通个人的完整验证码、证件号和报告细节。

---

## 15. identity match 是查询系统的独立状态

学历记录通常包含：

- 姓名；
- 身份证件；
- 出生信息；
- 学校；
- 专业；
- 层次；
- 入学/毕业时间；
- 证书编号；
- 图像等。

来源：

<https://www.chsi.com.cn/about/200902/20090209/17223140.html>

因此：

```text
record exists
```

和：

```text
current person can be automatically matched to record
```

必须分开。

建议：

```yaml
identity_binding:
  historical_name: unknown
  current_name_match: unknown
  historical_id_type: unknown
  current_id_match: unknown
  photo_match: unknown
  manual_evidence_required: unknown
```

### 隐私边界

本仓研究的是字段角色和系统状态，不建立普通毕业生学历数据库。

不得为了验证历史页面：

- 批量输入普通人的姓名/证书编号；
- 搜索并重新公开身份证号；
- 保存可用于身份盗用的完整历史学历报告；
- 利用今天的查询系统追查历史个人主页作者的真实学历。

---

## 16. old-record tail：今天“需要人工认证”不能倒推旧记录曾经不存在

2018 年以后制度继续把已经进入数据库的学历推向电子认证，但较早记录、数据库中没有的特殊记录仍可能需要人工认证。

这个现象虽超出本仓主年代，其作用是提醒如何解释 2001–2015 页面：

> 某类旧证书今天还需要认证，说明 registry coverage 是分层历史产物。

不能写：

```text
“2001 年系统开通，所以所有 1990s 学历从那天起都天然处于相同查询状态。”
```

2002 回登、后续补录、人工查档都说明覆盖是历史形成的。

---

## 17. archive 的最大错觉：保存了“查询入口”，却没有保存“查询事实”

Web archive 很可能保存：

- 首页；
- 帮助页；
- 查询表单；
- 字段说明；
- FAQ；
- 官方公告。

却通常不会、也不应该保存：

- 某普通人的真实查询输入；
- CAPTCHA 成功事务；
- 后端数据库快照；
- 身份验证；
- 私人学历结果；
- 企业核验日志；
- 下游招聘决定。

因此学历查询系统是一种典型的：

## control-surface survival / state-loss pattern

```text
control surface survives
backend historical state does not
```

后人会看到一个看似完整的“学历查询”按钮，误以为可以重放 2004 年的制度状态。

实际上按钮背后的：

- registry version；
- query service；
- captcha service；
- identity policy；
- access rules；
- result schema；

都可能早已变化。

---

## 18. current live page 不能替代 historical capture

当前教育部政务服务/学信网页面已经要求或展示：

- 证书编号；
- 姓名；
- 证件号码；
- 手机号码；
- 图形验证码；
- 短信验证码；
- 权属人同意等规则。

这些是**当前状态**。

不能把它们倒推到：

- 2004；
- 2007；
- 2009。

特别是当前页面明确要求权属人同意，不代表 2004 的匿名/零散查询已经使用同样的 consent model。

所以本仓应保留：

## interface-version gap

```text
historical query UI
≠ current query UI
```

每个字段都必须有对应时点的证据才能写入复原。

---

## 19. fake-site archaeology 的特殊规范

学历查询假站涉及：

- 诈骗；
- 个人身份信息；
- 伪造证件；
- 历史域名可能换手。

因此若未来研究 2004 前后仿冒站，应优先保存：

- 当时教育部/公安公告中的域名或描述；
- archive metadata；
- 页面结构摘要；
- logo/标题模仿方式；
- authority confusion 机制；

不要：

- 重新上线可工作的假学历查询器；
- 恢复真实个人假证数据；
- 测试今天复用后的域名是否仍能收集身份字段；
- 把 archive 中的个人证件号重新公开。

---

## 20. browser / charset / asset 状态：当前仍然 unknown 的部分

本轮没有获得一份已打开并验证的 2001–2004 WARC/Wayback capture。

因此以下保持 **unknown**：

```yaml
browser_assumption:
  ie_required: unknown
  netscape_compatible: unknown
  javascript_required: unknown
  cookies_required: unknown
  frameset: unknown

encoding:
  original_charset: unknown
  gb2312_or_gbk: unknown

form:
  method: unknown
  action: unknown
  field_names: unknown
  captcha_endpoint: unknown
  result_endpoint: unknown

assets:
  historical_label_images: unknown
  css: unknown
  js: unknown
```

当前官方历史页的文字存在，不足以补全这些字段。

---

## 21. 证据表

| Claim | Evidence | Grade | What it proves | What it does not prove |
|---|---|---:|---|---|
| 2001 实施学历电子注册、供社会网上查询 | 教育部教学〔2001〕4号 | A | 制度与管理链存在 | 普通用户体验/页面结构 |
| 2001 部分数据仍可用软盘申报 | 教育部教学厅〔2001〕2号 | A | 后台仍是混合数据流 | 每省具体执行完全相同 |
| 2002 回登 1991–2000 信息 | 学信网官方制度史 | B+ | backfill 存在 | 每条记录首次上网日期 |
| 2002 开展学历认证 | 教育部/学信网 | A/B+ | 认证服务与纸质报告链存在 | 某个人实际办理结果 |
| 2004 CHSI 是唯一官方学历查询网站 | 教育部公告 | A | authority host 规则 | 具体假站技术实现 |
| 2004 查询页支持证书信息核查 | 学信网当前保存的 2004 dated page | A-/B+ | 官方历史文本/功能表述 | 原 DOM/charset/backend |
| 2009 开通学信档案 | 学信网 2012 官方回顾 | B+ | holder account 功能时间线 | 2009 原界面技术细节 |
| 2010 即时注册、减少 2–3 月延迟 | 教育部同期材料 | A/B+ | publication latency 的制度转折 | 秒级事务一致性 |

---

## 22. 与 `how-people-lived` 的交叉链接

生活史对应专题：

`tmzncty/how-people-lived/topics/from-paper-credential-to-searchable-proof-education-verification-and-credential-stacking-china-1993-2026.zh-CN.md`

本仓只保留以下可复用结论：

1. **remote verifiability 依赖一整条 registry/query chain，而不是一个网页。**
2. **数据库回填会制造时间错觉。**
3. **前台 Web 可以在线，后台仍可能依赖软盘/人工审核。**
4. **“无结果”有多个解释，不等于证书必假。**
5. **权威域名本身是学历真实性链的一部分。**
6. **公共 archive 容易保存 control surface，难保存真实个人 query/result state。**

---

## 23. 本轮新增的 state gaps

正式记录以下术语：

- `upstream-ingest gap`
- `certificate/registration gap`
- `registration-lag gap`
- `backfill-anachronism gap`
- `report-object/report-validation gap`
- `authority-host gap`
- `form-semantics gap`
- `captcha gap`
- `query-endpoint gap`
- `backend-availability gap`
- `dataset-version gap`
- `record-match gap`
- `holder-account gap`
- `publication-latency gap`
- `report-validity gap`
- `identity-binding gap`
- `interface-version gap`
- `control-surface/state-loss gap`

---

## 24. Stop conditions

以下情况停止增加确定性：

- 只有当前学信网页，没有历史 capture；
- current host 上的 dated page 无法证明 original DOM；
- 搜索引擎出现 Wayback locator，但未实际打开；
- 查询字段标签只剩图片且图片未保存；
- 无法确认一个学历记录在哪个日期首次进入数据库；
- 涉及普通人的完整证书号、身份证号、照片；
- 需要真实提交今天的查询系统才能“验证历史个人”；
- 假站域名已复用，无法确定历史主体；
- 只能通过今天的接口行为猜 2004 后台。

“我们确认 2004 有学历查询功能，但不能可靠复原 2004 查询事务”本身就是有效结论。

---

## 25. 下一步

最高价值证据不是另一篇“学信网发展史”，而是：

### A. 2001–2004 可验证的 historical capture

最好取得：

```text
original URL
capture URL
capture datetime
HTTP status
Content-Type / charset
HTML source
form method/action
input names
label images
JS/CSS
captcha behavior
result URL pattern
```

### B. 同时找到一份同期用户操作说明

用于比较：

```text
official help says X
user actually does Y
```

### C. 保留一个 negative reconstruction

如果历史主 HTML 存在但 query backend 不可能重放，应明确写：

> **historical control surface preserved; historical transaction state unrecoverable.**

而不是模拟一个“2004 查询成功”结果冒充历史系统。

---

## Sources

### A / official contemporaneous

- 教育部，2001，《高等教育学历证书电子注册管理暂行规定》：<https://www.moe.gov.cn/s78/A15/xss_left/moe_779/s3263/201006/t20100602_88643.html>
- 教育部办公厅，2001，《关于做好2001年高等教育学历证书管理工作的通知》：<https://www.moe.gov.cn/jyb_xxgk/gk_gbgg/moe_0/moe_7/moe_12/tnull_5937.html>
- 教育部，2004，《关于重申中国高等教育学生信息网是学历证书查询唯一网站的公告》：<https://hudong.moe.gov.cn/jyb_xxgk/gk_gbgg/moe_0/moe_1/moe_366/tnull_4328.html>
- 教育部，2010，《普通高等教育学历证书实施在线即时电子注册》：<https://www.moe.gov.cn/jyb_xwfb/gzdt_gzdt/moe_1485/201006/t20100625_90052.html>
- 教育部，2010，《普通高等教育学历证书即时注册实现“零时差”查询》：<https://www.moe.gov.cn/jyb_xwfb/gzdt_gzdt/moe_1485/201008/t20100816_93954.html>

### Official historical pages / later institutional reconstruction

- 学信网，2004-11-26，“学历网上查询－查询系统”：<https://www.chsi.com.cn/__/200411/20041126/188.html>
- 学信网，2004-12-27，“全国高等教育学历信息数据库”：<https://www.chsi.com.cn/xlrz/ct03.shtml>
- 学信网，“学历电子注册制度”：<https://www.chsi.com.cn/about/200902/20090209/17223140.html>
- 学信网，“学历认证”：<https://www.chsi.com.cn/about/ct14.shtml>
- 学信网，2012，“学信网建立功能完善的学籍学历查询验证服务体系”：<https://www.chsi.com.cn/ycnews/201210/20121031/357939990.html>
