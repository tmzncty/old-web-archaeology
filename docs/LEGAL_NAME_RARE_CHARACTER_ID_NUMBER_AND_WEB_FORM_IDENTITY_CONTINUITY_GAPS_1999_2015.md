# 1999–2015：合法姓名、生僻字、身份证号码与 Web 表单的身份连续性缺口

> 研究对象：约 1999–2015 年中文 Web 中，实名报名、考试、铁路和其他制度型站点怎样把“现实中的同一个人”压成姓名字符串、证件号码和验证状态；当姓名不能被输入/编码/显示、15/18 位号码并存、权威记录与平台记录不一致时，一张历史页面究竟能证明什么。

生活史对应研究：

- `tmzncty/how-people-lived/topics/legal-name-identity-record-continuity-rare-characters-and-machine-legibility-china-1984-2026.zh-CN.md`

本文严格保持本仓约 1995–2015 中文互联网 scope。1980s 身份证制度和 2022 以后字符标准治理只作为理解 Web 状态的边界，不在这里展开一般身份制度史。

---

## 0. 去重：这不是已有“证件门控”或“学历查询”note 的重复

已有文档分别研究：

- `DOCUMENT_GATED_SHARED_ACCESS_AND_IDENTITY_BINDING_2001_2005.md`：网吧/共享终端怎样核验证件；
- `CREDENTIAL_QUERIES_DYNAMIC_DATABASES_AND_PERSONNEL_RECORD_GAPS_2001_2010.md`：学历和人事记录怎样被动态查询；
- `RAILWAY_TICKETING_12306_BROWSER_IDENTITY_QUEUE_PAYMENT_AND_TRIP_STATE_GAPS_2010_2012.md`：12306 的账号、乘车人、证件、订单和出行状态；
- `EDUCATION_CREDENTIAL_QUERY_REGISTRY_VERIFICATION_AND_RESULT_STATE_GAPS_2001_2015.md`：教育资格查询。

这些 note 多数把姓名/证件号码当作已经能够进入系统的字段。

本文研究更底层的 **identity-string continuity**：

```text
现实的人
→ 法律姓名 / 公民身份号码
→ Web 输入字符串
→ 浏览器提交值
→ 服务端解码
→ 数据库保存值
→ 下游系统交换值
→ 权威记录匹配
→ 平台身份状态
→ 现实业务结果
```

核心规则：

```text
legal identity ≠ representable string
representable string ≠ submitted bytes
submitted bytes ≠ durably stored value
stored value ≠ rendered glyph
rendered glyph ≠ authority match
authority match ≠ downstream account link
account link ≠ completed real-world service
```

---

## 1. 研究单位：不要把“姓名字段”当成身份本身

本题至少要区分：

- **physical person**：现实中的自然人；
- **canonical civil record**：公安/户籍系统中的法定姓名与公民身份号码；
- **credential artifact**：身份证、准考证、社保卡等；
- **input method state**：用户设备能否产生目标字符；
- **browser/form state**：表单字段是否允许/保留该字符；
- **wire encoding state**：请求以什么编码传输；
- **server decode state**：服务器如何解释字节；
- **database state**：后台真正保存了什么；
- **rendering/font state**：页面/票据是否有对应字形；
- **verification state**：该字符串是否与权威库/历史账户匹配；
- **service state**：报名、购票、开户等是否真正完成；
- **archive artifact**：今天保存下来的 HTML、截图、帮助页或报道。

因此看到：

```html
<input name="name">
```

只能证明页面设计中存在一个姓名入口，不能证明任何 Unicode/GBK/GB18030 字符都能通过完整链路。

---

## 2. 1999：15→18 位身份证号码是 Web 身份字段必须长期兼容的历史迁移

1999 年公民身份号码改为 18 位，旧身份证在有效期内仍可继续使用。这意味着随后十余年的 Web 系统不能只面对一个“永远固定格式”的身份证字段，而要面对现实中的迁移期。

Contemporary sources:
- 《生活时报》，1999-03-07：https://www.gmw.cn/01shsb/1999-03/07/GB/910%5ESH10-716.htm
- 《生活时报》，1999-09-28：https://www.gmw.cn/01shsb/1999-09/28/GB/shsb%5E1115%5E0%5ESH1-2823.htm

Evidence: **B（同期报刊，解释标准与过渡）**。

考古时至少应编码：

```yaml
identity_number_format:
  accepted_15_digit: true/false/unknown
  accepted_18_digit: true/false/unknown
  x_checksum_case: X/x/unknown
  normalization_rule: unknown
  old_to_new_crosswalk: unknown
```

### `identifier-format coexistence gap`

一个历史站点在 2005 年接受 15 位和 18 位，只能证明**输入层兼容两个格式**。

不能证明：

- 后台会把两者自动合并成同一个 person record；
- 同一人以旧号注册的历史账户能被新号自动找回；
- 下游银行、学校或铁路都采用同样的映射规则。

---

## 3. 2007 的现实反证：合法新旧证件存在，不等于下游数据库有 crosswalk

2007 年 CCTV.com 保存的《广州日报》报道记录，湖南耒阳部分居民因历史地址代码纠正而出现新旧身份证号码不同；一名在广州的居民同时持有两张真实证件，银行仍不能把旧号账户和新号本人自动连接。

Source:
- https://news.cctv.com/society/20070824/100579.shtml

Evidence: **B + contemporaneous first-person**。

这条材料不是 Web capture，却是旧网身份模型的重要现实边界：

```text
valid old credential
+ valid new credential
≠ backend same-person bridge
```

因此历史网页中的“身份证号已验证”不能被解释成一种跨时间永久身份状态。

---

## 4. 2008/2009 研究生网报：系统明确允许把合法姓名压成 `?`

2008 年发布的 2009 年考研网报信息说明，把姓名字段写成：字库中不存在的汉字以问号代替；同一说明又同时接受 15 位和 18 位内地身份证号码。

Contemporary copies/republishers:
- 新浪教育（注明来源中国研究生招生信息网），2008-09-10：https://edu.sina.com.cn/kaoyan/2008-09-10/1621163440.shtml
- 陕西招生考试信息网，2008-09-01：https://www.sneac.com/info/1266/12779.htm

Evidence: **B / A- boundary**。这是同时代操作规则的保存/转载，但本轮没有取得当年 `yz.chsi.*` 原始报名表单 memento。

这里必须新增：

### `canonical-name / submitted-name gap`

```text
canonical_name = 张𠮷某
submitted_name = 张?某
```

（示例仅用于说明结构，不对应任何个人。）

### `lossy-substitution-is-protocol gap`

如果同期官方/服务说明要求用户主动使用 `?`，那么 `?` 可能不是乱码，而是业务协议本身的一部分。

因此未来取得历史 HTML 后，不能见到问号就自动写：

```text
archive decoding failed
```

必须先判断：

1. 原始页面说明是否主动要求问号替代；
2. capture 的 HTTP charset 是什么；
3. 原始字节是否仍在；
4. Wayback rewrite 是否改变编码；
5. 问号来自页面正文、用户提交值还是后来的渲染。

---

## 5. 2009 北京中考：有损表示会进入整个后续材料链

2009 年北京中考同期报道说，约 2000 名考生因姓名字符无法通过当时字库/输入法处理而使用拼音替代；相关替代还会进入体检通知、考生卡等后续材料，审核时需要额外确认。

Source:
- CCTV.com / 《京华时报》，2009-03-22：https://news.cctv.com/society/20090322/101677.shtml

Evidence: **B**。

新增：

### `one-form / downstream-document propagation gap`

一次 Web/录入端 compromise 可能不是局部 UI 问题：

```text
initial registration alias
→ exam database
→ medical-exam notice
→ candidate card
→ later admission/checking
```

每一次传播都可能强化那个有损表示。

所以不能把某张后续证件上出现的拼音自动当作“本人法定姓名就是拼音”。

---

## 6. 2010 山东高考：另一条路线是页面提供生僻字复制，而不是把人名压成 `?`

2010 年山东省 2011 年高考远程网报的同期操作说明指出，姓名字符无法由输入法输入时，可在报名网站的“生僻字举例”中找到后复制粘贴。报道同时提醒 JavaScript 关闭会使按钮失效，报名存在 30 分钟时间限制。

Source:
- 大众网—生活日报，2010-11-21：https://sd.dzwww.com/sdnews/201011/t20101121_5990791.html

Evidence: **B, contemporary operational guidance**。

这条证据很适合 M3 浏览环境研究，因为它把几个层级分开：

```text
input-method support
≠ page character availability
≠ clipboard transfer
≠ JS runtime
≠ form submission
≠ server acceptance
```

### `copy-paste palette gap`

即使页面提供了目标字，仍然不知道：

- 该页面以 GB2312、GBK、GB18030、UTF-8 或其他编码提供；
- 浏览器/操作系统字体能否显示；
- 复制后 POST 请求是否保留同一字符；
- 服务端数据库是否原样存储；
- 后续准考证/录取系统是否继续支持。

本轮没有历史 capture，以上全部保持 `unknown`。

---

## 7. 2010 的数据库字段标准：`C(24)` 也不等于“姓名最多 24 个 Unicode 字符”

2010 年政法干警招录培养试点的一份同期考生信息标准（人民网内容经中国教育在线保存）列出了 Visual FoxPro 数据库字段：姓名字段 `XM` 为字符型长度 24，字库没有的汉字仍以半角问号代替；证件号码字段长度 18，并继续接受 15/18 位身份证号。

Source:
- 中国教育在线，2010-06-23：https://www.eol.cn/gongwuyuan/gazj/201006/t20100623_488876.shtml

Evidence: **B, contemporaneous technical/data-format description**。

### `field-length semantics gap`

看到 `C(24)` 不能用今天数据库/Unicode 心智直接翻译成“24 个任意字符”。

Visual FoxPro 的 code page、DBF 字段字节数、中文双字节编码、实际客户端写入方式都可能改变解释。

没有原 DBF、code-page metadata 和当年程序时：

```text
field declared length = 24
≠ 24 Unicode scalar values
≠ 24 Chinese characters universally accepted
```

---

## 8. 2011–2015 铁路实名：账号身份、乘车人身份和可输入姓名继续分离

已有铁路 note 已经证明：

```text
account operator / buyer
≠ passenger
≠ identity document holder
```

本专题再补一个字符串层。

2015 年《新京报》采访姓名含“瓛”字的邵先生；报道称其银行存折、车票、社保卡、驾照等多处不能正确显示全名，12306 客服当时给出的解决办法是在线姓名可用拼音替代，但须去车站窗口做身份核验。

Source:
- 人民网 / 《新京报》，2015-03-21：https://travel.people.com.cn/n/2015/0321/c41570-26727955.html

Evidence: **B + contemporaneous first-person + service response**。

状态链至少是：

```text
legal passenger name
→ Web-compatible substitute
→ contact/passenger record
→ verification pending / not completed online
→ physical station document check
→ verified identity state
→ online purchase route potentially usable
```

因此新增：

### `display-name / verification-name gap`

页面显示/保存的拼音替代不一定就是最终用于人工核验的法律姓名。

### `online-entry / offline-trust gap`

Web 可以完成身份记录的一部分，但信任闭环仍在柜台完成。

> **online real-name field ≠ online-complete real-name verification。**

---

## 9. 2014 的“待核验”：不要把状态标签直接解释成 root cause

2014 年人民网/钱江晚报报道一名经常乘火车的用户发现，自己在 12306 的常用联系人状态变为“待核验”，导致不能像以前一样直接选中购票；报道怀疑其姓名生僻字可能有关。

Evidence: **B, contemporaneous report, but causal attribution uncertain**。

本 note 只保留窄结论：

```text
contact row existed
→ historical status could become “待核验”
→ purchase route was blocked until identity state resolved
```

不能升级为：

```text
rare character definitely caused that exact state transition
```

这是典型的 `visible-state / hidden-cause gap`。

---

## 10. 旧 Web 的字符问题至少有七层，不能都叫“乱码”

以后遇到姓名无法正常显示时，先定位失败层：

1. **character repertoire**：标准/字库里有没有该字符；
2. **input method**：用户是否能输入；
3. **font/glyph**：系统是否能画出字形；
4. **client encoding**：浏览器/程序如何编码；
5. **server decoding**：服务端如何解释请求；
6. **database/storage**：后台能否无损保存；
7. **exchange/downstream**：下一套系统是否认同同一编码和同一姓名。

再加一层：

8. **identity matching**：即使字符完整，权威记录是否把它和证件号/账户映射到同一个人。

因此：

```text
input failure ≠ font failure
font failure ≠ encoding failure
encoding failure ≠ database truncation
database success ≠ downstream interoperability
string equality ≠ verified same person
```

---

## 11. GB2312 / GBK / GB18030 / UTF-8：没有 capture 就不要替历史页面猜 charset

1999–2015 中文 Web 横跨多种字符集和浏览器环境。

未来做完整 archaeology case 时至少记录：

```yaml
http_content_type: unknown
http_charset: unknown
html_meta_charset: unknown
raw_bytes_available: false
archive_rewrite_observed: unknown
browser_assumption: unknown
os_font_assumption: unknown
input_method_assumption: unknown
server_decode_assumption: unknown
database_encoding: unknown
```

特别禁止：

- 今天 Chromium 能正常显示一个生僻字，就写“2009 年用户也能看见”；
- 今天页面 UTF-8，就倒推十几年前历史系统也是 UTF-8；
- 转载页能显示汉字，就倒推原报名系统数据库无损保存；
- 看到 `?` 就自动做 mojibake repair；
- 根据后来 GB18030 标准支持范围，推定旧系统已经实施同样能力。

现代回放和历史执行环境必须分开。

---

## 12. 一个专门的 archive trap：`?` 可能有四种完全不同的 provenance

历史姓名/页面里看到 `?` 时，至少有四种解释：

```text
A. 当年业务规则要求用户主动输入 ?
B. 浏览器提交时发生有损转码
C. 服务端/数据库写入时发生 replacement
D. archive / 现代解码把未知字节显示成 ?
```

A–D 的历史含义完全不同。

如果不能取得 raw bytes、HTTP header 或同期规则，就应该标：

```yaml
question_mark_origin: unknown
```

而不是“修复”成一个研究者猜测的汉字。

这类 reconstruction 一旦把猜测字形写回页面，会直接伪造个人姓名，属于本仓应避免的高风险复原。

---

## 13. `same person` 也可能因为号码变化而被误拆成两个 Web 用户

旧站数据如果同时出现：

```text
name = 王某
id = 15-digit-A
```

和多年后：

```text
name = 王某
id = 18-digit-B
```

不得仅凭姓名相同就合并，也不得仅凭号码不同就断言是两个人。

需要独立 crosswalk evidence。

### `historical-identifier / account-identity gap`

尤其在：

- 招生系统；
- 银行账户；
- 社保；
- 早期实名铁路；
- 政务查询

中，一个历史 15 位号码可能只是当时合法的 account key。

出于隐私，本仓不应收集普通人的完整身份证号来做批量拼接。研究规则应该优先保留：

```yaml
id_format: 15_digit
id_value: redacted/not_collected
```

除非号码本身是公开规范示例且与普通个人无关。

---

## 14. 页面可观察事实与真实身份结果必须拆开

建议以后对这类 artifact 用如下状态：

```yaml
page:
  name_field_present: true/false/unknown
  rare_character_help_present: true/false/unknown
  id_15_accepted: true/false/unknown
  id_18_accepted: true/false/unknown
  substitution_rule: question_mark/pinyin/copy_palette/unknown

client:
  input_character_possible: true/false/unknown
  rendered_correctly: true/false/unknown
  js_required: true/false/unknown

transaction:
  request_sent: true/false/unknown
  server_accepted: true/false/unknown
  durable_record_created: true/false/unknown
  canonical_name_preserved: true/false/unknown

verification:
  authority_lookup_attempted: true/false/unknown
  match_succeeded: true/false/unknown
  manual_review_required: true/false/unknown

outcome:
  registration_complete: true/false/unknown
  credential_issued: true/false/unknown
  offline_fallback_used: true/false/unknown
```

这比“网站支持实名”可靠得多。

---

## 15. 保存偏差：公开帮助页很亮，真正的 identity crosswalk 很暗

archive 最容易留下：

- 报名须知；
- 字段列表；
- FAQ；
- 登录页；
- 生僻字示例表；
- “待核验”帮助；
- 浏览器提示。

最难留下、也本来就不应该公开的是：

- 普通用户完整身份证号；
- 公安权威库返回值；
- 旧号→新号映射；
- 真实姓名替代值；
- 银行/学校人工核验工单；
- 数据库修复 SQL / 个人记录；
- 柜台看到的证件扫描件。

我把它称为：

### **public-form-shell / private-identity-crosswalk asymmetry**

于是后人很容易知道“页面要求姓名和身份证”，却不知道一个合法姓名在后台失败以后究竟怎样被修好。

这不是 archive 不够努力而已，其中相当一部分是正确的隐私黑区。

---

## 16. 与现有 old-Web notes 的交叉规则

### 与铁路票务 note

```text
passenger identity
→ name representation
→ verification state
→ order/ticket state
→ station execution
```

本文只负责前两到三步的字符串/记录连续性，铁路 note 负责后续订单和现实乘车。

### 与教育 credential note

```text
legal person
→报名/学籍 identity row
→ credential record
→ online query
```

本文不把姓名可录入直接写成学历存在。

### 与网吧证件门控 note

网吧柜台核验身份证证明的是 access venue 层；不能因此把平台昵称与身份证姓名自动绑定。

### 与档案/学历动态数据库 note

数据库查询可以返回一个资格记录，不代表查询者或当前账号已经与该记录主人完成 same-person 绑定。

---

## 17. Evidence ledger

| Claim | Evidence | Grade | What it proves | What it does not prove |
|---|---|---:|---|---|
| 1999 后 15/18 位号码在过渡期共存 | 同期《生活时报》 | B | 格式迁移与旧证继续有效 | 各 Web 系统如何 crosswalk |
| 2007 下游银行可能无法把新旧号码认成同一人 | CCTV/广州日报个案 | B | same-person / same-record gap 存在 | 全国普遍率 |
| 2008/09 研招网报允许姓名用 `?` 替代 | 同期报名说明转载/保存 | B/A- | 业务协议存在有损姓名表示 | 当年原 DOM / POST / DB charset |
| 2009 北京中考拼音替代会进入后续材料 | 同期媒体 | B | 有损表示可继续传播 | 每位考生最终结果 |
| 2010 山东高考站点提供生僻字复制路线 | 同期操作报道 | B | Web 前端 workaround 存在 | 原页面 charset / server storage |
| 2010 招录数据格式含姓名/ID 长度与替代规则 | 同期数据标准转载 | B | historical field contract | 原系统代码和 DB code page |
| 2015 12306 对部分生僻字使用拼音+窗口核验 fallback | 人民网/新京报 | B | hybrid identity fallback | 所有生僻字、所有车站一致实现 |

---

## 18. 本轮 verified / high-probability / unknown

### 已证实（在当前证据强度范围内）

- 1999 后存在 15/18 位身份证号码格式迁移和共存期；
- 2008/09 研招网报说明明确允许对无法表示的姓名汉字使用问号替代；
- 2009 北京中考存在拼音替代姓名并继续进入后续材料的同期报道；
- 2010 山东高考网报存在页面提供生僻字复制粘贴的操作路线；
- 2015 铁路实名 Web/线下之间存在拼音替代 + 物理窗口核验的 fallback 证据。

### 高概率但仍需原 artifact 验证

- 同一时期不同报名系统采用了不同字符集、输入控件和数据库编码；
- 有损替代在部分后台会造成后续人工核验劳动；
- 15/18 位格式兼容并不意味着所有历史账户自动完成 same-person merge。

### 不知道

- 2008/09 研招原始页面实际 HTTP charset、DOM、form action、POST bytes；
- `?` 在后台是否原样存储或被另一个字段映射回法律姓名；
- 2010 山东“生僻字举例”页面的原字符集、字体和脚本实现；
- 2010 DBF 文件实际 code page 与生产数据库实现；
- 2014 具体用户“待核验”的 root cause；
- 2015 12306 各类生僻字的完整输入/核验规则矩阵。

---

## 19. M1 / archive 状态：本轮不虚假升级

本轮得到的是很强的 contemporary service documentation、媒体操作描述和 historical locators，但**没有实际打开并检查一份满足 M1 标准的 2008–2010 实名报名 transaction Wayback/WARC capture**。

高价值 locator 包括：

- 中国研究生招生信息网历史报名服务（同期文档指向 `yz.chsi.*` 体系）；
- 山东高考报名 `wsbm.sdzk.gov.cn`；
- 12306 `www.12306.cn`。

它们当前只能登记为 locator/context，不算 verified capture。

下一次若取得 memento，必须实际记录：

- original URL；
- capture URL；
- capture datetime；
- HTTP status；
- Content-Type / charset；
- raw HTML；
- JS / stylesheet / font 子资源缺失；
- form action 是否被 archive rewrite；
- 页面中的 `?` 是 literal text 还是解码结果；
- modern Chromium 与历史浏览环境差异。

---

## 20. 隐私 stop conditions

本题尤其容易滑向不必要的人肉拼接，明确禁止：

- 收集普通用户完整身份证号；
- 用姓名 + 学校 + 手机 + 身份证片段重新识别报道中的普通人；
- 尝试登录旧实名账户；
- 使用泄露银行/教育/铁路数据库补 crosswalk；
- 把已经脱敏的政府咨询案例重新反查真实身份；
- 为了修复乱码而猜测并重新公开普通人的真实姓名。

如果历史 artifact 的研究价值主要依赖暴露普通人的完整身份字段，应停止，而不是“为了考古完整性”继续。

---

## 21. 这份 note 改变了什么

旧网考古过去很容易把实名表单写成：

```text
姓名 + 身份证号 → 实名用户
```

现在必须改成：

```text
法定姓名 / 历史号码
→ 客户端能否表示
→ Web 是否允许输入
→ 请求是否无损
→ 后台是否保存
→ 权威记录是否匹配
→ 历史旧号/新号是否 crosswalk
→ 是否需要人工例外
→ 现实业务是否完成
```

因此一张旧网页上出现“姓名”“身份证号”两个输入框，最多证明**那个时代已经试图把现实身份结构化**。

它不自动证明：

> **所有合法的人都能完整进入这个结构，也不证明系统认出的那个字符串，已经可靠地对应回现实中的同一个人。**
