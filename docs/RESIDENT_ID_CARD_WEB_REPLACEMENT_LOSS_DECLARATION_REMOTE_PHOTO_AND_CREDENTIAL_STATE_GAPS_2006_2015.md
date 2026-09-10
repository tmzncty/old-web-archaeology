# 2006–2015：居民身份证网上补领、遗失声明、异地传照与凭证连续性状态缺口

> 研究对象：约 2006–2015 年中文 Web 如何进入居民身份证遗失、补领、照片采集、实人核验、费用支付、邮递与异地受理链条。重点不是完整身份证制度史，而是历史网页和同期数字服务究竟能证明“人已经看见入口”“申请已经提交”“公安机关已经受理”“新证已经制作”“旧证已经失效”中的哪一层。

生活史对应研究：

- `tmzncty/how-people-lived/topics/resident-id-loss-replacement-portable-personhood-and-identity-fallback-china-1984-2026.zh-CN.md`

本文严格保持本仓约 1995–2015 中文互联网 scope。1984 身份证制度建立、2017 全国异地受理、2020s App/全程网办只作为理解 2006–2015 边界的前后参照，不把本仓扩展成一般数字身份史。

---

## 0. 去重：这不是“姓名字段”“居住登记”“护照”或“实名制”专题的另一份版本

本仓已经有：

- `docs/LEGAL_NAME_RARE_CHARACTER_ID_NUMBER_AND_WEB_FORM_IDENTITY_CONTINUITY_GAPS_1999_2015.md`：姓名、生僻字、15/18 位身份证号码和 identity-string continuity；
- `docs/RESIDENCE_REGISTRATION_TEMPORARY_RESIDENCE_PERMIT_EMPLOYER_WEB_DECLARATION_AND_SERVICE_STATE_GAPS_2002_2015.md`：人在异地居住时的登记状态；
- `docs/PASSPORT_ONLINE_PREAPPLICATION_APPOINTMENT_BIOMETRICS_ISSUANCE_AND_MOBILITY_STATE_GAPS_2002_2015.md`：护照申请链；
- 铁路、网吧、银行、学历、手机实名等多份依赖身份证的下游 state-gap。

这些文档多数把“本人手里是否有一张可用身份证”当作已有前提。本文补的是 **credential continuity / 凭证连续性**：

```text
现实中的人仍存在
→ 权威人口记录仍存在
→ 身份证号码仍存在
→ 但实体卡可能遗失 / 损坏 / 到期
→ 如何重新得到可被下游机构接受的凭证
```

研究问题因此不是：

> “一个身份证号能否正确输入 Web 表单？”

而是：

> **“当最常用的实体身份证明坏掉以后，历史 Web 到底承担了流程中的哪一步？又有哪些决定性步骤仍在公安后台、邮政、亲友、实体窗口和下游用证单位中？”**

---

## 1. 研究单位：不要把“网上补办身份证”当成一个原子动作

本题至少必须拆开：

- **person**：现实中的自然人；
- **authoritative person record**：公安人口信息系统中的权威个人记录；
- **citizen identity number**：公民身份号码；
- **physical credential**：某一张具体居民身份证；
- **credential status**：有效、到期、挂失/丢失申报、失效等；
- **public information page**：办事说明、政策页、FAQ；
- **application endpoint**：真正接收个人申请的页面/系统；
- **photo artifact**：数码相片及其质量检测结果；
- **identity-proof artifact**：户口簿影印件、历史照片、视频/人脸、指纹等；
- **application record**：申请数据是否进入公安业务系统；
- **authority decision**：户籍地/受理地公安机关是否审核签发；
- **fee state**：工本费、邮费等是否已支付并正确入账；
- **production state**：卡片是否已经制成；
- **postal state**：是否已交 EMS、在途、签收；
- **relying-party state**：银行、铁路、旅馆等是否认可当前凭证/临时证明；
- **archive artifact**：今天能看到的新闻截图、教程、历史页面或 capture。

因此固定：

```text
public guide exists
≠ authenticated user entered service

application form rendered
≠ application submitted

application submitted
≠ authority accepted

authority accepted
≠ card produced

card produced
≠ card delivered

loss declaration submitted
≠ replacement application submitted

loss declaration recorded
≠ every downstream institution rejects old card

physical card machine-readable
≠ authoritative credential status valid
```

---

## 2. 前史边界：二代证先是机读凭证，后来 Web 才进入“修复凭证”的链条

2003 年通过、2004 年施行的《居民身份证法》已经明确居民身份证用于证明公民身份，公民身份号码具有唯一、终身不变性质；在申领、换领、补领期间急需使用身份证的，可以申请临时居民身份证。

这说明在本研究窗口开始之前，就已经存在三个不同对象：

```text
权威身份记录
实体居民身份证
临时居民身份证
```

2004 年二代证试点又把非接触 IC 卡、视读与机读能力引入实体凭证。但这仍不能被写成“居民身份证已经变成 Internet 身份”。

本仓只用这一前史解释为什么 2006–2015 的 Web 不是从零制造数字身份，而是在一个已经机读化、已经有公安业务后台的凭证体系上，逐步把 **照片、申请、查询和远程受理** 搬到网络入口。

Evidence family:
- 《中华人民共和国居民身份证法》政府保存文本（A，制度边界）：https://www.miluo.gov.cn/25287/25292/25293/42753/content_1231204.html
- 新华社 2004-03-30 二代证试点同期稿（B）：https://news.sohu.com/2004/03/30/84/news219658493.shtml

---

## 3. 2006 重庆：Web 先替代“照片的身体移动”，不是一次性消灭返乡

2006 年重庆针对大量长期在广东等地务工人员推广异地办理二代身份证的远程照片传输办法。同期报道描述的链条非常典型：

```text
务工地数码照相馆拍摄照片
→ Internet 上传至二代证照片检测系统
→ 合格后打印回执 / 委托书
→ 电子照片传回重庆公安
→ 本人把纸质回执 / 委托书寄给家人
→ 家人带户口簿到户籍地派出所代办
→ 户籍地完成审核、签发和制证
```

报道还记载，梁平县大量人口在深圳、东莞等地务工，试行期间已有数千人通过这种办法办理。

Sources:
- 2006-09-27《华西都市报》同期稿：https://news.sina.com.cn/c/2006-09-27/080010118888s.shtml
- 2006-10-19《重庆晨报》同期稿：https://news.sina.com.cn/c/2006-10-19/030710269283s.shtml

Evidence: **B（同期报刊，包含公安部门对流程的说明）**。

### `remote-photo / authority-presence gap`

远程上传合格证件照只能证明：

```text
photo artifact can travel digitally
```

不能证明：

```text
applicant no longer needs any household-side proxy
or
registered-residence authority no longer controls issuance
```

这是一种非常重要的旧网混合系统：**Web 可以先把一件材料移走几千公里，但制度责任、纸质委托和亲友代跑仍留在原地。**

### `online-information / online-transaction gap`

2006 年 10 月公安部政府网站还组织了二代身份证在线访谈，回答普通用户有关换证、收费、异地情况等问题。

Source:
- 同期转载：https://news.sina.cn/sa/2006-10-19/detail-ikkntiam7926509.d.html

Evidence: **B（同期转载，证明当时有公安部网站在线答疑；原始公安部页面 capture 尚未核）**。

因此：

```text
policy Q&A online
≠ ID application online
```

---

## 4. 2009 湖南：最值得保留的旧网对象，是“遗失声明”和“遗失补领”并存却不相同

2009 年 12 月人民网同期报道记录湖南居民身份证遗失声明网上受理试运行，并明确指出此前已经试点遗失补领网上受理。报道还保存了相关页面截图和候选 host：

- `www.hnga.gov.cn`
- `www.96305.com`
- `www.hnidcard.com`

Source:
- 2009-12-07 人民网同期稿的搜狐保存页：https://news.sohu.com/20091207/n268739057.shtml

Evidence: **B + contemporaneous visual artifact**。

注意：报道中的页面截图可以证明当时媒体观察到某种界面和功能，它**不是原站 archive capture**，不能据此填写完整 HTTP header、charset、DOM 或服务端行为。

### 4.1 两条业务链必须分开

**A. 遗失声明：**

```text
进入声明入口
→ 身份核验
→ 填写遗失信息
→ 提交/付款（若适用）
→ 声明记录/页面生成
```

**B. 遗失补领：**

```text
进入补领入口
→ 输入本人身份/户籍字段
→ 提交户口簿影印件等材料
→ 上传照片/完成身份核验
→ 提交申请
→ 缴费
→ 公安审核
→ 制证
→ EMS 投递
→ 本人收到新证
```

所以必须固定：

### `loss-declaration / replacement gap`

```text
loss declaration submitted
≠ replacement application submitted
```

### `loss-declaration / invalid-card gap`

2009 的“遗失声明”不能自动等同于后来全国失效居民身份证信息系统中的权威失效状态，更不能证明所有银行、铁路、旅馆和其他用证单位在同一时刻拒绝旧卡。

### `public-screenshot / historical-capture gap`

新闻截图只能作为视觉二手证据。若以后找到原站 memento，必须重新记录：

- original URL；
- capture URL；
- Memento-Datetime；
- HTTP/回放状态；
- charset / Content-Type；
- DOM 与表单 action；
- 图片/JS/CSS 是否完整；
- 登录与动态 endpoint 是否仍指向历史后端。

---

## 5. 一个可定位但尚未核成 capture 的历史 URL

当前承载于阿里云开发者社区的一篇页面带 `2010-06-12` 时间戳，作者以第一人称说其新办的二代身份证在 EMS 寄送途中遗失，随后搜索到湖南网上补办路径，并转载了当时办理说明。

页面保留了一个很具体的旧 URL：

`http://www.96305.com/framework/hngx/iphfbcol-mbkc-bbnn-keml-kipojgjknlfi.do?isfloat=1&disp_template=templatedefault&fileid=20090720134615750`

Source:
- https://developer.aliyun.com/article/511813

Evidence: **B/C boundary**。

理由：

- 页面以 2010 日期和第一人称语气存在；
- 但当前平台是后来的内容承载页，本轮没有取得原始博客的 2010 memento；
- 因而可用来登记 historical locator 和用户理解，不可用来证明 2010 年服务器此刻返回了什么字节。

### `candidate-locator / verified-capture gap`

必须严格写成：

```yaml
original_url_candidate: http://www.96305.com/framework/...
source_of_locator: later-hosted page carrying 2010 timestamp
verified_memento: false
```

不能因为 URL 看起来完整，就把它当成已核 archive capture。

---

## 6. 2010 湖南：摄像头、网吧、Web、公安后台与 EMS 组成一个完整但高度混合的旧网事务链

2010 年《湖南日报》报道湖南居民身份证遗失补领网上受理正式推出。同期流程写得很具体：

- 可使用带摄像头的电脑；
- 报道明确写“网吧亦可”；
- 可从湖南公安/电子政务相关网站进入；
- 填写身份证号码、姓名、户号；
- 通过摄像头提交视频照片/完成身份确认；
- 填写投递地址；
- 受理后通过邮政速递寄送。

Source:
- 平江县政府保存的《湖南日报》2010-09-16稿：https://www.pingjiang.gov.cn/35048/35055/35056/content_1041601.html

Evidence: **B（同期报纸内容由政府站点保存）**。

### 6.1 这不是“全程无地点”的服务

它依赖：

```text
Internet 接入
+ 有摄像头的 PC
+ 浏览器/页面运行环境
+ 身份/户籍字段可匹配
+ 公安后台
+ 支付/费用处理
+ 实体制证
+ EMS 物流
```

因此更准确的历史描述是：

> **Web 把受理入口从户籍地派出所搬到任何一台满足条件的联网电脑前，但没有把制证、权威审核和最后一公里邮递变成虚拟动作。**

### 6.2 `application-approved / card-delivered gap`

上文第一人称材料恰好提供反例：新证件本身可能在 EMS 阶段遗失。

所以即使：

```text
online application = success
AND
card production = success
```

仍然不等于：

```text
credential possession restored = success
```

这和电商/快递研究有结构相似性，但对象不同：这里物流失败造成的不是普通商品延迟，而是**身份凭证连续性继续中断**。

---

## 7. 2015 的教程保存了一个重要浏览器事实：至少有一条历史路径显式依赖 Flash 摄像头权限

2015 年新浪保存的一篇图文教程演示湖南异地/网上身份证办理时，页面明确提示允许 **Adobe Flash Player** 使用摄像头；教程还要求输入户号，并记录作者本人因为户号有误，需要家人回当地核实/重新打印信息。

Source:
- 2015 图文教程：https://jx.sina.com.cn/news/m/2015-11-21/detail-ifxkxfvn8931390.shtml （同类异地办理人物材料）
- 湖南网上办理图文操作页：https://news.sina.com.cn/ （本轮使用的具体检索 artifact 需后续在 capture ledger 中补全 exact article URL）

本轮可稳定使用的现有检索证据表明：2015 相关 `hnidcard.com` 路径出现 Flash 摄像头许可和户号字段。

Evidence: **B/C boundary（同期/近同期教程）**。

### `browser-capability / identity-proof gap`

这是一个非常适合旧网考古的浏览器依赖：

```text
page HTML survives
≠ Flash runtime survives

Flash permission dialog visible
≠ webcam successfully captured image

webcam captured image
≠ server accepted evidence

server accepted evidence
≠ authoritative household record matched
```

### `household-number-entered / authority-match gap`

教程中的户号错误反例尤其重要。表单允许用户输入一个字符串，不等于公安权威户籍记录会接受它。

```text
browser value syntactically valid
≠ authoritative person/household join succeeds
```

### 浏览器环境目前的止步线

本轮不能把 2015 Flash 依赖倒推到 2009：

- 2009 页面是否同样用 Flash：**unknown**；
- 2009 页面 charset：**unknown**；
- 是否 IE-only：**unknown**；
- 是否 ActiveX：**unknown**；
- 是否 table layout / frameset：**unknown**。

在拿到历史 HTML/capture 以前，不补画“典型 IE6 页面”。

---

## 8. 2015：Web 入口与“人在何处受理”开始继续分化

2015 年公安机关推进居民身份证异地受理试点。一名 22 岁湖南籍青年在湖北办理时，现场登记、身份核验、照片/指纹采集后得到取证回执，约十分钟完成前台手续。

Source:
- 《人民日报》2015-12-18：https://finance.people.com.cn/n1/2015/1218/c1004-27944218.html

Evidence: **B + contemporaneous person**。

对本仓最重要的不是 2017 后来的全国节点，而是看到 2015 时 state machine 已经开始改变：

```text
本人所在地受理
→ 户籍地/权威人口信息核验
→ 制证/签发
→ 结果回到本人所在地
```

这与 2006 的：

```text
人在外地
→ 照片数字回传
→ 纸委托寄回
→ 家人到户籍地代跑
```

不是同一种“网上办证”。

### `remote-artifact / remote-authority gap`

2006 主要让材料远程；2015 开始让**受理责任本身跨地域协作**。研究中文政务 Web 时不能只数“某年有网页”，要问网页后面的行政拓扑有没有变。

---

## 9. 可复用 state gaps

本案例建议加入本仓长期词汇表：

### 9.1 `public-service-shell / authenticated-person gap`

公开办事页存在，不证明普通用户已经进入需要实名状态的事务系统。

### 9.2 `identity-number / credential-state gap`

知道身份证号码，不等于手中持有有效证件。

### 9.3 `loss-declaration / invalid-card gap`

做过遗失声明，不等于旧卡已在所有权威/下游系统中不可用。

### 9.4 `loss-declaration / replacement gap`

声明遗失与申请新证是两个事务。

### 9.5 `replacement-submit / authoritative-acceptance gap`

Web 显示提交成功，不等于公安业务系统已经正式受理或签发。

### 9.6 `remote-photo-upload / identity-verification gap`

照片上传成功不等于照片合格，更不等于它已被可靠绑定到正确自然人。

### 9.7 `photo-compliance / person-match gap`

符合证件照技术标准不等于身份核验完成。

### 9.8 `webcam-permission / video-proof gap`

浏览器/Flash 得到摄像头权限，不等于视频证据达到服务端要求。

### 9.9 `browser-form / police-ledger gap`

表单里的姓名、身份证号、户号只是用户提交值；公安权威记录是否匹配是另一状态。

### 9.10 `household-number-entered / household-number-authoritative gap`

输入一个格式正确的户号，不等于当前权威户籍库中它属于本人。

### 9.11 `payment / application-posting gap`

支付/汇费成功不应自动升级成补证业务权威记录已更新。

### 9.12 `application-approved / card-produced gap`

审核签发与实体制证是两个步骤。

### 9.13 `card-produced / EMS-delivered gap`

制成新卡不等于本人已经拿到；邮递可以失败。

### 9.14 `physical-card-readable / authoritative-validity gap`

一张旧卡的芯片仍能被读出，不等于权威系统仍把它当有效凭证。

### 9.15 `provincial-web-service / national-portability gap`

湖南某一时点的网上补领不能写成全国普通人的可用能力。

### 9.16 `service-exists / migrant-adoption gap`

报道、截图和教程能证明服务存在/有人使用，不能推算外出务工群体整体采用率。

### 9.17 `public-screenshot / historical-capture gap`

同期新闻截图不是 memento。

### 9.18 `current-host / historical-backend gap`

今天某 host 存活或重定向，不证明它连接的是 2009 年同一公安业务后端。

---

## 10. Artifact / evidence ledger

| artifact | date | proves | grade | does not prove |
|---|---:|---|---|---|
| 重庆外出务工人员网络传照报道 | 2006 | 数码照、Internet 传输、回执/委托、亲友代办的混合链存在 | B | 当地所有务工者可用；户籍地审核已取消 |
| 公安部网站在线访谈同期转载 | 2006 | Web 已进入政策问答层 | B | 办证事务已可在线完成 |
| 人民网湖南遗失声明/补领报道与截图 | 2009 | 两类业务存在；候选 host 与界面可观察 | B + visual | 原站 HTML/HTTP/charset；全国普及 |
| 后来承载的 2010 时间戳用户页 | 2010 | 一名用户把网上补领当现实补救；保存旧 URL locator | B/C boundary | 原始博客字节、后台结果、代表性 |
| 湖南日报政府保存稿 | 2010 | 摄像头、网吧、Web 字段、邮递链存在 | B | 所有浏览器环境；每次申请结果 |
| 2015 图文教程 | 2015 | 至少一条路线涉及摄像头/Flash、户号等字段 | B/C boundary | 2009 同样依赖 Flash；权威后端成功 |
| 异地受理同期人物报道 | 2015 | 人可在户籍地以外完成受理前台 | B | 全国全面可用；Web 本身完成异地审核 |

---

## 11. Archive 状态：本轮没有达到 verified historical Memento

本轮针对以下候选对象进行了 archive locator / replay 尝试：

- `www.hnidcard.com`
- `www.96305.com`
- `www.hnga.gov.cn`
- 2009 报道/用户页中出现的具体 `96305.com/framework/...do?...fileid=...` locator

当前访问链没有取得一份能够逐项核验以下字段的合格 historical memento：

```yaml
archive_source: ?
capture_url: ?
original_url: ?
capture_datetime: ?
http_status: ?
content_type: ?
charset: ?
html_dom: ?
form_action: ?
script_dependencies: ?
subresources_complete: ?
```

因此本轮结论只能写：

> **M1 verified historical Hunan resident-ID Web capture: NOT ACHIEVED IN THIS SLICE.**

不能写：

- “Wayback 没保存”；
- “页面已经彻底不存在”；
- “2009 页面就是 IE6 + GB2312 + Flash”；
- “今天找到的新闻截图等同于网页原件”。

这遵守 `docs/METHOD.md` 的负证据合同：locator 未实际核验只能登记为 candidate，`没有找到` 不能升级为 `当时不存在`。

---

## 12. 浏览器 / 字符集 /插件假设

当前已证实：

- 2015 相关教程至少显示过 **Adobe Flash Player 摄像头权限**；
- 2010 同期报道明确要求带摄像头的联网电脑，甚至可用网吧；
- 2009 媒体保存的页面截图证明有 Web UI，但不是 HTML artifact。

当前不知道：

- 2009/2010 exact browser support matrix；
- IE6/IE7 是否为硬性要求；
- 是否使用 ActiveX；
- 是否使用 Flash webcam，还是其他本地组件；
- GB2312 / GBK / UTF-8；
- 是否 frameset/table-heavy；
- form action 是否指向同 host；
- 摄像头照片是否经客户端压缩/插件编码；
- session/cookie 机制；
- 后台是否依赖公安专网而非公网页面直接连接核心库。

这些必须等待 verified capture、教程全文或软件环境证据，不做 D 级“想当然复原”。

---

## 13. 历史可见性：越权威的身份事务，越不应该进入公共 archive

本案例有非常强的 **public-guidance / private-authority inversion**。

公开旧网可以合理保存：

- 办事指南；
- 费用/时限；
- 候选 host；
- 通用字段名；
- 页面布局；
- 浏览器依赖；
- 示例截图；
- 新闻中的流程描述。

真正能证明某个具体人“补领成功”的材料却包括：

- 身份证号码；
- 户号；
- 户口簿影印件；
- 证件照、视频人像；
- 指纹；
- 家庭住址；
- 投递地址；
- 公安后台审核状态；
- 具体证件签发/失效时间；
- 某个下游用证单位的核验记录。

这些恰恰应该受隐私保护，不应因为“考古完整性”被重新公开。

因此：

> **公共 Web 最容易保存“一个普通人当年理论上可以怎么补证”，最不应该保存“这个普通人究竟是哪一个人、交了哪些生物信息、住在哪里、后台如何处理”。**

这不是 archive 失败，而是研究伦理的必要边界。

---

## 14. 为什么“旧卡还能被读出来”不能当作“旧卡仍有效”

后来建立的失效居民身份证信息系统进一步暴露了一个早期旧网研究中容易忽略的事实：实体卡的可读状态和权威凭证状态可以分离。

2016 后相关制度要求社会用证单位联网核查失效信息；2019 同期法治报道仍记录部分使用部门未充分接入，身份冒用个案因此继续发生。

Sources（作为 2015 scope 之后的边界说明，不作为本文主体）：
- 公安部 2016 失效居民身份证信息系统报道：https://www.gov.cn/xinwen/2016-10/06/content_5115529.htm
- 2019《法制日报》/人民网：https://legal.people.com.cn/n1/2019/0319/c42510-30983427.html

这个后续节点说明为什么研究 2009 “遗失声明”时更不能写成：

```text
user clicked declare-lost
→ old physical card universally stopped working
```

真正状态应该至少拆成：

```text
loss report/declaration
→ authority record changes (if it does)
→ invalid-card data becomes queryable
→ relying party actually queries
→ transaction rejects old credential
```

---

## 15. 对中文旧网史的修正：历史“政务上网”不只是网页，还是材料和身体重新分配

这个对象能纠正两种相反的误读。

### 误读 A：2000s 网上办事只是“看看说明，真正都线下”

不对。2009–2010 湖南的身份证遗失补领已经把真实身份材料、摄像头验证、申请和投递地址放进 Web 事务链，能实质减少本人返乡。

### 误读 B：一旦出现“网上补领”，整个办证就已经虚拟化

也不对。它仍可能依赖：

- 户籍权威记录；
- 家人/原籍核实；
- 摄像头、Flash/浏览器；
- 公安内部业务系统；
- 工本费/邮费；
- 实体制证；
- EMS 送达；
- 下游用证机构自己的核验能力。

旧网真正改变的是 **where the person must be**：

> 从“本人必须回户籍地”开始，逐步变成“照片先走、纸和亲友代走、申请在 Web 走、权威数据后台走、最后实体卡再通过邮政回来”。

这比“某政府网站 2009 年上线某功能”更接近普通人的实际变化。

---

## 16. 反例与后见之明风险

### 16.1 不把湖南地方服务写成全国服务

2009–2010 的网上补领具有明确地域和资格条件。

### 16.2 不把新闻截图写成 historical capture

截图可作 B 级视觉证据，不自动拥有 Memento metadata。

### 16.3 不把“带摄像头 PC”写成“智能手机时代的网页版”

2010 的设备世界包括网吧、PC、摄像头、浏览器、可能的插件和 EMS；它的执行环境与今天手机 App 完全不同。

### 16.4 不把 2015 Flash 依赖倒推到 2009

实现可能在六年间多次重写。

### 16.5 不把服务报道中的成功用户外推为普通迁移人口总体体验

报道天然偏向能找到入口、成功完成流程或具有新闻价值的人。

### 16.6 不把“挂失/声明”写成旧卡物理失效

卡片、权威状态和下游核验是三个对象。

### 16.7 不把“异地受理”写成户籍责任完全消失

很多时期只是本人不用身体返回，权威审核仍通过后台回到户籍地。

---

## 17. M1 候选价值与下一步

这个对象值得进入后续 M1/平台环境验证，因为它同时包含：

- 明确年代：2006、2009、2010、2015；
- 多个 contemporaneous evidence family；
- 具体候选 host/URL；
- 动态表单；
- 摄像头/Flash 这种浏览环境依赖；
- 公安后台 + Web + EMS 的 hybrid transaction；
- 一条直接影响普通迁移者工作和返乡成本的现实执行链。

下一步优先级：

1. 用可验证的 archive source 取得 `hnidcard.com` / `96305.com` 2009–2010 memento；
2. 若 Wayback locator 不可核，检查 Common Crawl、国家/地方档案馆或同期电子报附件；
3. 取得 2015 Flash 教程 exact URL、截图和页面时间字段；
4. 若拿到 capture，记录 charset、HTML、form action、cookie/session、Flash object/embed、JS 与子资源；
5. 尽量确认 2006 重庆照片检测中心历史 host，而不是根据机构名猜 URL；
6. 不追求恢复真实普通用户的身份证号、照片、户口簿和申请记录。

当前状态：**research package strong; M1 verified capture incomplete**。

---

## 18. 本轮对 old-Web archaeology 的新增理解

这条线最重要的不是又发现一个 2000s 政府网站，而是确认旧 Web 已经开始承担一种非常具体的“人生故障修复”。

如果一个外出务工者丢失身份证，传统故障恢复需要本人回户籍地；2006 的系统先让照片走网络、本人少走一段；2009–2010 湖南进一步让申请、摄像头验证和邮寄进入 Web；2015 后异地受理又让权威数据在后台替本人往返。

因此中文旧网不能只按“网页内容”和“网民文化”来考古。某些动态表单真正改变的是：

> **一个人为了让制度重新认出自己，到底需要移动多少公里、请几天假、借谁的电脑、找不找家人代跑，以及新证还没到手的那几周能不能继续正常生活。**

而 archive 恰好最难保存这条事务的权威内部状态。所以本案例再次证明：页面保存得再完整，也不能自动推出真实人生结果；但只要把 Web、公安后台、家庭代理、邮政和下游核验一起建模，残存页面仍足以帮助我们恢复普通人当年“怎样把自己重新接回制度”的一部分现实。

---

## Sources / evidence ledger

- 《中华人民共和国居民身份证法》政府保存文本（A）：https://www.miluo.gov.cn/25287/25292/25293/42753/content_1231204.html
- 新华社 2004 二代证试点同期稿（B）：https://news.sohu.com/2004/03/30/84/news219658493.shtml
- 2006 重庆外出务工人员网络传照/亲友代办（B）：https://news.sina.com.cn/c/2006-09-27/080010118888s.shtml
- 2006 重庆扩大远程照片传输（B）：https://news.sina.com.cn/c/2006-10-19/030710269283s.shtml
- 2006 公安部网站二代证在线访谈同期转载（B）：https://news.sina.cn/sa/2006-10-19/detail-ikkntiam7926509.d.html
- 2009 湖南网上遗失声明/补领同期报道与截图（B + visual）：https://news.sohu.com/20091207/n268739057.shtml
- 2010 用户第一人称页面、保留 `96305.com` 历史 URL（B/C boundary）：https://developer.aliyun.com/article/511813
- 2010《湖南日报》网上补领、摄像头/网吧/邮递链（B）：https://www.pingjiang.gov.cn/35048/35055/35056/content_1041601.html
- 2015 跨省异地受理普通人案例（B）：https://finance.people.com.cn/n1/2015/1218/c1004-27944218.html
- 2019 失效身份证信息联网边界（scope 之后的机制说明，B）：https://legal.people.com.cn/n1/2019/0319/c42510-30983427.html
