# SCREEN READER / WEB ACCESSIBILITY / SEMANTIC NAVIGATION / AUTHENTICATION / TASK-COMPLETION STATE GAPS, 1999–2015

Status: research note / state-gap model  
Scope: 约 1999–2015 中文 Web 中视障用户、读屏软件、键盘导航、网站无障碍、认证与真实任务完成之间的状态；**不把本仓扩展成全球无障碍技术史，也不研究 2015 年以后 App 无障碍的完整历史。**  
Cross-repo companion: `tmzncty/how-people-lived/topics/from-human-readers-to-screen-reader-independence-visual-impairment-assistive-technology-and-interface-executability-china-1953-2026.zh-CN.md`  
Last research pass: 2026-09-05

## 0. Why a page screenshot is almost useless for proving screen-reader usability

旧网页考古通常先问“页面长什么样”。本题必须再问一层：

> **一个当年的视障用户，使用当年的浏览器、读屏软件和输入方式，能不能完成同一个任务？**

视觉截图最多支持视觉布局；它通常不能证明：

- 图片是否有可理解的替代文本；
- 表单字段是否与 label 正确关联；
- Tab/focus 顺序是否合理；
- 图片按钮、Flash、脚本控件能否被读屏识别；
- 动态状态变化是否被辅助技术通知；
- 键盘能否到达并激活全部控件；
- 验证码是否有非视觉替代；
- 提交成功/失败状态是否会被读屏读到；
- 当年具体 screen-reader/browser 组合是否支持页面使用的技术。

因此本 note 的第一条硬规则是：

> **historical rendering ≠ historical accessibility experience.**

## 1. Evidence contract and research units

遵循 `docs/METHOD.md`。

研究时至少区分：

- `site / host`
- `page / URL`
- `historical DOM/resource state`
- `browser / user agent`
- `assistive technology / screen reader`
- `keyboard/focus state`
- `semantic label/alternative-text state`
- `dynamic update state`
- `login state`
- `authentication/challenge state`
- `transaction request`
- `server-side durable state`
- `result/feedback state`
- `user encounter state`
- `archive capture`
- `claim`

不能把：

```text
“2008 年某网站宣布完成无障碍改造”
```

和：

```text
“某位盲人使用某版本 IE + 某版本读屏，在某一天成功完成登录、查询、提交和结果确认”
```

写成同一个状态。

### Evidence grades used here

- **A**：同期标准、协会通知、官方/机构同期页面；
- **B**：同期新闻现场观察、用户采访、实际操作报道；
- **C**：后来机构史；
- **D**：本 note 明确画出的状态机与 archive/browser gap。

### Privacy stop condition

不得为了“验证无障碍”：

- 尝试旧用户账号或密码；
- 根据论坛内容重新识别普通视障用户；
- 收集身份证、银行卡、医疗、求职等私人 transaction；
- 用真实个人信息去测试遗留页面；
- 把历史求助内容重新公开成身份档案。

真实用户的私人任务状态没有进入 archive，很多时候是正确的隐私边界。

## 2. 1999：国际 Web 已经明确把 accessibility 当作页面设计问题

W3C 于 1999-05-05 发布 WCAG 1.0 Recommendation。原始文本明确讨论文本替代、可导航性、不同 user agents、voice browsers 与 screen readers，并指出旧浏览器或辅助技术未必支持所有特性。

Source (A, original standard):  
https://www.w3.org/TR/WCAG10/

这条全球证据只作为技术前史，不改变本仓中文 Web scope。

它给旧网考古一个关键方法提示：

```text
valid HTML
≠ accessible HTML

text visible on screen
≠ text exposed correctly to assistive technology
```

即使我们取得 historical HTML，也不能只用现代 Chromium 的视觉截图判断当时无障碍性。

## 3. 1999–2007：中国读屏用户进入通用 Web，但证据主要保存“使用结果”，不是完整技术栈

2007 年《羊城晚报》报道王永德的经历，记载其在 1999 年末做出读屏软件第一版、2000 年注册；到 2007 年，一些用户已借助读屏上网聊天、搜索信息和接受远程教育。

Source (B+, contemporaneous report with retrospective technical chronology):  
https://news.sina.com.cn/c/2007-06-08/170211985722s.shtml

这能支持：

```text
Chinese screen-reader-mediated Web use existed by the early 2000s
+ Web search/chat/remote-learning use existed among some users
```

不能支持：

```text
all major Chinese sites were accessible
specific browser version was required
specific DOM technique worked
screen-reader market share was known
```

报道把王永德软件称为“国内首个”；本 note 只保存为媒体当时的描述，不把软件优先权升级成独立核验的技术史 claim。

更重要的是，所谓“能上网”必须继续拆开：

```text
browser starts
→ screen reader exposes browser chrome
→ URL/page loads
→ text/navigation is perceivable
→ links can be traversed
→ form controls can be found
→ fields can be entered
→ action can be triggered
→ server accepts request
→ result change is announced
→ user understands final state
```

## 4. 2008：网站责任第一次进入明确的中文 Web 公共行动

2008-04-01 中国互联网协会发布北京奥运会、残奥会信息无障碍网站行动通知，提出推出相关标准，并推动奥组委、中国残联、政府网站和部分门户进行无障碍改造。

Source (A/B+, contemporaneous association notice):  
https://www.isc.org.cn/article/1521.html

这能证明：

```text
Web accessibility had become an explicit site-design / standardization problem
```

但不能证明：

```text
all named sites completed every planned adaptation
all pages within a site had the same accessibility
all screen readers worked identically
```

因此：

> **campaign target ≠ completed adaptation ≠ user task success.**

## 5. 2008：中国盲人数字图书馆证明专门 Web 空间可做到“读屏 + 键盘 + 内容服务”

2008-10-15《光明日报》报道中国盲人数字图书馆开通。记者现场看到盲人使用读屏软件、键盘和语音提示进入网站，使用电子图书、音频、视频和在线讲座。

Source (B+, contemporaneous observation):  
https://www.gmw.cn/01gmrb/2008-10/15/content_848568.htm

这个案例必须与主流平台分开：

```text
purpose-built accessible library works
≠ bank works
≠ job board works
≠ ecommerce checkout works
≠ school enrollment works
```

因此固定：

> **dedicated-accessibility / mainstream-parity gap.**

它也是 archive 研究的重要偏差：专门无障碍站往往会留下“这是无障碍网站”的明确说明，而普通站点某个具体版本到底能不能被读屏使用，反而很少被系统记录。

## 6. 2008–2013：标准存在不等于历史页面自动符合

全国标准信息公共服务平台记录 YD/T 1761-2012 于 2012-12-28 发布、2013-03-01 实施，代替 YD/T 1761-2008。

Source (A/B+, standards registry):  
https://hbba.sacinfo.org.cn/stdDetail/ccac3842174d800dd0165ba4d77c638b

当前无障碍公共服务平台对标准沿革的说明也明确记录 2012 版替代 2008 版。

Source (B, current standard explanation):  
https://www.wcag.org.cn/yybztx/bzjd/yq/index.html

标准能作为**解释框架**，不能反向用作**站点符合性证据**。

所以：

```text
standard published
≠ site tested
≠ page conforms
≠ screen reader can complete task
```

必须有具体历史页面、测试或同期用户证据才能继续往下写。

## 7. 2009–2010：淘宝视障创业个案把研究从“读页面”推进到“完成经济事务”

2010 年《中国青年报》报道一组视障大学生经营淘宝网店；报道说他们计划分享“淘宝盲用操作攻略”和《视障者淘宝操作手册》，并保存了队长 2009-07-06 的同期日记片段。

Source (B+, contemporaneous report):  
https://news.sohu.com/20100221/n270322328.shtml

这至少证明某些视障用户当时已经在尝试完整电子商务工作流，而不是只浏览网页。

但 archive 不能从“网店真实存在”倒推出淘宝当时所有流程都天然无障碍。真实工作很可能包含：

```text
登录
→ 商品/店铺管理
→ 买家消息
→ 订单状态
→ 支付/结算
→ 地址/物流
→ 售后
→ 页面更新和改版
```

任何一环都可以有独立的 accessibility state。

所以固定：

> **readability ≠ transactional operability.**

以及：

> **one successful user workflow ≠ platform-wide accessibility.**

## 8. 核心状态机 A：公共信息页面

```text
historical URL exists
→ historical page returned
→ encoding/DOM parsed
→ meaningful content exposed to accessibility layer
→ headings/links/forms distinguishable
→ keyboard/focus traversal works
→ target content reached
→ user understands content
```

必须分别记录这些 gap：

### rendered-text / accessibility-tree gap

视觉上有文字，不保证辅助技术取得同样文字与角色信息。

### alternative-text presence / usefulness gap

有 `alt` 属性也不等于内容有意义；`alt="image1"` 与说明按钮用途不是同一件事。

### focus-reachability gap

控件视觉存在不等于键盘焦点能到达。

### focus-order gap

能到达全部控件不等于顺序可理解。

### dynamic-update / announcement gap

AJAX/JS 改变页面不等于读屏用户得到状态通知。

## 9. 核心状态机 B：登录与认证

```text
login page readable
→ username field identifiable
→ password field identifiable
→ values can be entered privately
→ captcha/challenge has accessible route
→ submit control operable
→ request reaches server
→ result/error exposed to user
→ authenticated session established
```

核心 gaps：

- `login-page readable / login-completable gap`
- `visual CAPTCHA / accessible-challenge gap`
- `secure-keyboard / assistive-technology gap`
- `authentication success / user-perceived-success gap`

旧网考古尤其不能看到“登录页看起来正常”就写“盲人可以登录”。

## 10. 核心状态机 C：报名、购物、银行、教育等高后果任务

```text
public page accessible
→ account/session accessible
→ required record found
→ form fields understandable
→ required data entered
→ validation error understood
→ submission triggered
→ server durable state created
→ payment/authorization if needed
→ final result returned
→ user recognizes final state
→ real-world entitlement changes
```

因此要固定：

> **accessible shell ≠ accessible transaction.**

某银行首页无障碍，不证明网银密码控件可用；某大学首页无障碍，不证明报名表与支付页可用；某购物列表无障碍，不证明 checkout、退款与客服可用。

## 11. “现代浏览器回放正常”在本题里更加危险

对于普通视觉页面，现代浏览器至少还能给出某种近似视觉呈现；对 screen-reader archaeology，环境错一层就可能改变结论。

应尽量记录：

```text
OS
browser/version
screen reader/version
plugin/ActiveX/Flash state
DOM/markup
encoding
keyboard model
security widget
```

本轮没有这些历史组合的 verified test，因此**不得**写：

- “2008 某站 IE6 + 某读屏一定可用”；
- “某 Flash 一定不可访问”；
- “某页面现代 Chromium 可读，所以当年读屏也可读”。

正确写法是：

> **browser/screen-reader compatibility remains unknown unless historically tested.**

## 12. archive visibility bias：视觉壳层幸存，非视觉交互状态消失

Archive 最容易保存：

- HTML；
- 图片；
- CSS；
- 有时 JavaScript；
- “无障碍版”链接或声明。

最容易丢失：

- 当年 accessibility tree；
- screen reader 实际发声顺序；
- focus state；
- JS runtime event；
- 验证码替代通道；
- 登录后的私有页面；
- 一次真实表单提交；
- 用户是不是实际听见了错误提示；
- 某次改版是否让一个旧 workflow 失效。

因此新建：

> **visual-shell / nonvisual-interaction asymmetry.**

这意味着旧 Web 对视障用户的历史往往比普通视觉用户更难从截图恢复。

## 13. accessibility regression：版本更新可能关闭一条原本可走的路线

旧网研究不能默认：

```text
2005 不可用
→ 2008 改造
→ 以后永远越来越可用
```

真实状态可能是：

```text
v1：简单 HTML，可键盘使用
→ v2：加入图形按钮/脚本，读屏路径变差
→ v3：无障碍改造，重新可用
→ v4：认证组件更换，再次失效
```

这叫：

> **accessibility regression / 无障碍回退。**

要证明 regression，必须拿到同一任务至少两个历史版本的可比证据；本轮没有这样的完整序列，所以目前只把它作为研究模型，不声称某个具体中文站已经被本轮证实存在这种版本回退。

## 14. 历史 locator 与本轮 M1 负结果

本轮取得了强的同期文本与标准证据，但**没有实际取得并打开一份满足仓库 M1 要求的 1999–2015 中文网站 screen-reader task Wayback/WARC capture**。

因此以下仍为 `unknown`：

- 2007 报道所涉普通网站的原 DOM/charset；
- 2008 中国盲人数字图书馆首版原 HTML、脚本与资源；
- 2008 奥运/残奥无障碍行动涉及站点的具体改造前后 DOM diff；
- 2010 淘宝相关页面的历史表单、焦点、脚本和登录状态；
- exact `browser + screen reader + page version` compatibility；
- 当年的验证码/安全控件可访问性；
- 私人登录后的真实 transaction state。

这不是理由去用今天的网站补历史，也不是理由从截图猜 DOM。

下一步最有价值的是：

1. 找到一个 2008–2012 中文无障碍站的 verified memento；
2. 记录 original URL / capture datetime / HTTP/content-type / charset / DOM；
3. 判断页面是否保存足够完整；
4. 如果可以，在合法离线环境中使用历史浏览器/读屏组合进行**明确标记的 reconstruction experiment**；
5. 与同一站普通版或前后版本比较。

## 15. 反例与停止条件

- 标准发布不能证明站点符合；
- 无障碍声明不能证明全部子页面可用；
- 专门盲人站不能证明 mainstream parity；
- 一个熟练用户成功不能证明普通用户容易使用；
- 一个用户失败也不能自动证明所有配置都失败；
- 现代 accessibility audit 不能自动改写历史体验；
- 涉及私人账号、银行、医疗、求职等任务时，不突破隐私边界追 transaction。

## 16. Cross-repo interpretation

`how-people-lived` 关心的是：辅助技术和接口兼容如何改变一个普通人的教育、工作、购物、金融、迁移和独立生活路线。

本仓只负责留下更窄的中文旧网判断：

> **Web 页面存在、视觉上正常、甚至公开宣称“无障碍”，都不足以证明当年的视障用户能够独立完成真实任务。**

真正要保存的是：页面版本、浏览器/辅助技术环境、语义与焦点结构、认证状态、提交反馈，以及我们仍然不知道的地方。
