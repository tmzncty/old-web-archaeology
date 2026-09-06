# PC DIY 模拟装机、价格库、论坛与真实装配：从网页配置到物理机器的状态缺口（2002—2015）

> Scope：只研究约 2002—2015 年中文 Web 中，DIY / 攒机网站怎样表示配件、价格、参数、兼容性、配置单、跑分预测、论坛意见和商家供给，以及这些网页状态与真实购买、真实装配、首次点亮、长期稳定、升级和二手退出之间的缺口。
>
> 不把本文件扩成中国 PC 工业史或全球 Homebrew computing 史。1990s 前史、相对收入、电脑城日常、2015 年以后的电商/视频化，以及海外 Homebrew / Usenet 对照，进入 companion：`tmzncty/how-people-lived/topics/pc-diy-component-optionality-upgrade-paths-and-hobby-computing-china-1992-2026.zh-CN.md`。

---

## 1. 研究单位：一张配置单不是一台电脑

本题至少包含以下不同对象：

- IT portal / 硬件门户；
- product database / 产品参数库；
- price page / 行情报价页；
- merchant listing / 经销商条目；
- configurator / 模拟攒机系统；
- saved build / 用户配置单；
- expert review / 配置点评；
- benchmark article / 跑分评测；
- forum thread / 求配置、翻车、超频、故障帖；
- driver / BIOS / firmware download；
- secondhand listing / 二手出件；
- off-platform contact / QQ、电话、email；
- physical component / 真实零件；
- physical assembly / 真实装配；
- POST / 第一次点亮；
- OS/driver state / 系统与驱动状态；
- stable workload / 长期稳定使用；
- upgrade / repair / resale / 后续升级、维修、转卖；
- current live legacy page / 今天仍在线的旧内容；
- historical archive capture / 历史档案抓取。

最小状态机：

```text
用户形成用途与预算
→ 查产品 / 行情 / 论坛
→ 建立配置单
→ 配置器判断或暗示兼容
→ 查询商家 / 库存 / 价格
→ 决定购买
→ 到店 / 电话 / 电商 / 邮寄
→ 真实零件到手
→ 装机
→ POST
→ BIOS 设置
→ 安装系统 / 驱动
→ 压力测试 / 跑分
→ 长期使用
→ 故障 / 清灰 / 换件
→ 升级 / 二手出售 / 退役
```

固定边界：

```text
product page exists ≠ product in local stock
quoted price ≠ user paid price
merchant listed ≠ merchant trustworthy
saved build ≠ parts purchased
configurator accepts combination ≠ physical compatibility guaranteed
predicted benchmark ≠ measured benchmark
POST success ≠ long-term stability
benchmark stable ≠ user's application stable
thread solved ≠ author implemented solution
“已出” listing ≠ complete transaction independently verified
old article timestamp ≠ every current module on page belongs to that date
```

---

## 2. 为什么 PC DIY 是旧 Web archaeology 的高价值对象

普通论坛研究常停在：

```text
发帖 → 回复
```

PC DIY Web 同时把网页接到：

```text
产品数据库
→ 实体零件

配置单
→ 真实购买

兼容性判断
→ 真实装配

跑分预测
→ 真机测试

价格页
→ 柜台 / 电商成交

故障帖
→ 真实拆机 / 换件 / BIOS 操作
```

因此即使 HTML 保存完整，也不能仅凭网页证明：

- 用户最终买了哪些部件；
- 当天柜台有没有货；
- 价格是否包含税/散片/盒装/搭售；
- 主板 BIOS 是否支持所选 CPU；
- 电源真实功率是否足够；
- 内存是否在真实机器上稳定；
- 机器是否成功点亮；
- 作者有没有照论坛建议实际换件。

PC DIY 特别需要把 **representation of a machine / 机器的网页表示** 与 **physical machine state / 物理机器状态** 分开。

---

## 3. 2002—2004：门户已经把每日行情、使用技巧、硬件论坛和线下卖场编成一个信息栈

2003 年 1 月，中关村在线的年度 DIY 总结已经把春节装机、配件代际、价格与亲友组机写在同一篇文章里；作者回忆 2002 年为朋友组装约 4000 元电脑。

同期来源：

- ZOL，《2002年ZOL硬件DIY总结--年末装机经验谈》，2003-01-29：<https://news.zol.com.cn/2003/0129/54867.shtml>

2004 年新浪硬件频道页面已经同时展示：

- CPU / 内存 / 硬盘当天价格；
- “硬件频道 / 产品评测 / 市场行情 / 使用技巧 / 选购指南 / 硬件论坛”导航；
- 来自 IT168 / ZOL 的行情材料。

例：

- 新浪，《6日硬件行情：CPU内存价格趋稳 硬盘价上涨》，2004-02-06：<https://tech.sina.com.cn/c/2004-02-06/27448.html>

同年中关村在线对太平洋数码电脑城的报道又直接把“DIY 攒机和散户柜台”描述为旧卖场形态之一。

- ZOL，《IT庙会之逛在太平洋数码电脑城》，2004-01-02：<https://nb.zol.com.cn/2004/0102/80737.shtml>

对 old-Web 来说，这不是三个孤立来源，而是一套 **Web-to-market stack / Web—卖场栈**：

```text
网上看每日价格
→ 看评测/配置
→ 进论坛问
→ 再去具体电脑城和柜台买
```

早期门户并没有立即取代电脑城，而是给实体卖场增加了一层购买前信息界面。

---

## 4. 价格页面需要单独建状态：行情不是成交记录

旧硬件站经常留下非常精确的数字，例如：

```text
CPU 某型号 560 元
内存某型号 295 元
硬盘某型号 635 元
```

但至少要区分：

```text
editor observed / received quote
→ page publication
→ user reads page
→ user contacts merchant
→ merchant confirms stock
→ exact SKU/盒装散片/版本确认
→ negotiation / 搭售
→ actual payment
→ component received
```

因此固定：

- `daily price ≠ national price`；
- `北京中关村报价 ≠ 广州/县城报价`；
- `price page timestamp ≠ merchant quote time`；
- `reference price ≠ transaction price`；
- `product name same ≠ PCB/revision same`；
- `low price ≠ stock exists`。

增加 **price-to-purchase gap / 报价—购买缺口** 与 **SKU-revision gap / 型号—硬件修订缺口**。

后一项尤其重要：同一商品名可能跨 PCB revision、显存颗粒、BIOS 或散热器版本变化，今天只剩产品页标题时不能把所有实体样本当同一机器。

---

## 5. 2005 搜狐智能装机：动态数据库第一次成为“虚拟机器”

2005 年 7 月，中关村在线报道搜狐数码天下智能装机系统，并留下精确 historical locator：

```text
http://act.it.sohu.com/jiutian/index.htm
```

报道称系统依赖：

- 上百个数据库表；
- 标准化配件产品库；
- 上万条评测数据库记录；
- 性能模拟算法；
- “输入预算 / 选择用途”；
- 指定配件和偏好；
- 对 3DMark 2001/2003/2005、SYSMark、PCMark 等给出预测值。

同期 B 级来源：

- ZOL，《人人都是DIY高手!搜狐推出智能装机系统》，2005-07-20：<https://news.zol.com.cn/new_news/2005/0720/186845.shtml>

### 5.1 这类系统的 archaeology 不能只找 landing page

一个 configurator 的真实历史行为至少依赖：

```text
landing HTML
→ JS / iframe
→ product database
→ compatibility rules
→ price feed
→ benchmark model
→ session / saved-build state
→ output page / build ID
```

即使 Wayback 保存首页，也可能完全无法重现一次配置。

因此新增 **dynamic-configurator survival gap / 动态装机器存活缺口**。

### 5.2 “性能预测”尤其需要保存 provenance

报道声称系统预测七类 benchmark 的误差可控制在一定范围，但 old-Web archaeology 只能证明**平台当时这样宣称**，不能在没有模型、输入数据库和真实测量集的情况下把它升级为历史事实。

固定：

```text
vendor/site performance claim
≠
independently validated model accuracy
```

---

## 6. 2006 ZOL 模拟攒机：配置单变成用户生成内容

2006 年 ZOL“网友自助装机专家点评”明确说，每天有大量用户用模拟攒机系统建立配置，平台从“网友装机方案库”选择有代表性的方案点评。

同期来源：

- ZOL，《9月攒机要点 2种定位5款网友配置点评》，2006-09-08：<https://diy.zol.com.cn/38/383201.html>
- ZOL，《疯狂游戏型 3款AM2速龙网友配置点评》，2006-09-12：<https://diy.zol.com.cn/38/385268_all.html>

这里需要新增一种 Web object：**saved virtual build / 保存的虚拟配置**。

它可能包含：

- build ID；
- 用户昵称；
- 用途；
- 预算；
- CPU / 主板 / 内存 / 显卡等产品 ID；
- 当时价格；
- 用户备注；
- 专家点评；
- 评论；
- 后续链接。

但配置单的历史字段可能发生时间塌缩：

```text
2006 年保存的 build
+ 当前产品数据库里的停产状态
+ 当前模板
+ 当前相关推荐
+ 后来修订的产品参数
```

因此新增 **saved-build temporal collapse / 配置单时间塌缩**。

若没有历史 capture，不能从今天渲染结果反推 2006 用户当时看到的完整价格和页面布局。

---

## 7. 配置器最危险的推理：网页接受组合 ≠ 真机兼容

真实 PC compatibility 可能取决于：

- socket；
- chipset；
- BIOS revision；
- memory QVL / rank / voltage；
- GPU length / slot width；
- PSU connector / 12V capacity；
- cooler mounting revision；
- case clearance；
- SATA / IDE / NVMe support；
- OS / driver version。

因此至少要拆：

```text
product records coexist in database
→ configurator allows selection
→ rule engine flags no conflict
→ parts actually purchased
→ exact revisions arrive
→ mechanically fit
→ electrically boot
→ BIOS recognizes hardware
→ OS driver works
→ sustained workload stable
```

增加：

- **database-to-physical-compatibility gap**；
- **revision-to-compatibility gap**；
- **POST-to-stability gap**。

一张“模拟攒机成功”的旧图不能证明机器曾经真实存在。

---

## 8. 2006—2008：未来升级被网页显式编码进推荐逻辑

2006 ZOL 的配置点评会直接用“以后升级”评价当前接口选择。例如同价位硬盘中，IDE 虽然现在能用，却因为主板接口趋势被批评不利于未来升级，而 SATA 被推荐为更长期路线。

来源：<https://diy.zol.com.cn/38/385268_all.html>

这说明旧 Web 产品导购不仅表达当前性能，还表达一种 **expected future topology / 预期未来拓扑**：

```text
今天选这个 socket / interface
→ 明年还能不能加东西
→ 下一次是否必须整个平台重换
```

因此 old-Web 页面是研究“当时人怎样想象硬件未来”的一手/近同时代材料之一。

但必须注意：编辑预测接口淘汰速度也可能判断错误。不能因为后来 SATA 胜出，就把当年的推荐写成必然正确。

---

## 9. 2008：页面上的“装机旺季”与现实学生购买仍有一道执行鸿沟

2008 ZOL 秋季分析称 DIY 市场受笔记本和品牌机挤压，但九月学生开学仍会形成装机高峰，平均预算约 4000—5000 元。

- ZOL，《性价比达到最佳 DIY攒机最新攻略大全》，2008-09-11：<https://zdc.zol.com.cn/106/1062657.html>

同期开学导购页面会同时提供“导购 / 评测 / 行情 / 新品 / 知识 / 论坛 / 攒机推荐 / 模拟装机”等入口。

- PConline/新浪，《从七彩虹Intel特惠，谈开学装机五大必知》，2008-09-02：<https://tech.sina.com.cn/h/2008-09-02/1648790663.shtml>

对 archive 来说，这种导航非常有价值，因为它显示当年网站试图把一个用户从：

```text
不知道买什么
→ 学知识
→ 看行情
→ 做配置
→ 去论坛验证
→ 找商品/商家
```

留在一个 portal 内完成。

但 archive 如果只保住文章正文而丢掉导航目标、脚本和数据库，就会留下一个“内容很多、事务能力消失”的壳。

增加 **portal-capability hollowing / 门户能力空心化**。

---

## 10. 论坛与真实排错：成功回复不是成功修复

PC DIY 帖子的现实结果常发生在离开网页以后：

```text
无法点亮 / 噪声 / 蓝屏
→ 发帖
→ 他人建议更新 BIOS / 换槽 / 拔显卡 / 换电源
→ 作者关机拆机
→ 真实硬件状态改变
→ 重启测试
→ 可能回来回帖
```

但作者可能不回来报告结果。

因此：

```text
accepted-looking advice ≠ executed advice
last reply ≠ final machine state
thread stops ≠ problem solved
```

需要新增 **troubleshooting outcome gap / 排错结果缺口**。

这类 gap 与 Stack Overflow 式纯软件问题不同，因为最终状态可能只存在于一台已经报废、卖掉或改装的实体机器里。

---

## 11. 二手与升级：论坛页只保存组件生命史的一部分

DIY 资产可拆分意味着一台电脑可能没有一个明确“死亡日”。

```text
整机 A
→ 换显卡
→ 旧显卡卖给 B
→ 加内存
→ 主板坏掉
→ CPU + 内存迁到另一台
→ 机箱继续用
```

因此 Web 上一个组件可能留下：

- 新品评测；
- 当年报价；
- 用户签名；
- 故障帖；
- 二手 listing；
- 下一位买家的配置。

但这些记录通常没有稳定实体 serial number 可连接。

增加 **component-life provenance gap / 组件生命史来源缺口**。

即使网页都幸存，也通常不能证明“这块具体显卡”跨过了哪些主人和机器。

---

## 12. 页面保存偏差：硬件门户特别容易把多个时点渲染到一起

今天打开 2003—2008 的 ZOL / PConline / 新浪旧文，常能同时看到：

- 历史文章标题与正文日期；
- 当前站点 header / footer；
- 当前产品“停产”状态；
- 当前经销商模块；
- 当前相关推荐；
- 当前 cookie / 广告系统；
- 后来迁移过的图片 CDN。

因此必须记录：

```text
article_content_timestamp
current_render_timestamp
current_host
embedded_product_widget_state
current_price_widget_state
historical_capture_status
```

增加 **hardware-portal legacy-render collapse / 硬件门户遗留渲染时间塌缩**。

不能截整页再标成“2006 年 ZOL 长这样”。

---

## 13. 动态资源与 archive gap 清单

PC DIY 页面特别容易系统性丢失：

- configurator JS；
- iframe；
- product database API；
- dynamic price feed；
- build ID backend；
- compare-list cookie/session；
- benchmark chart data；
- forum attachment；
- driver / BIOS binary；
- external images；
- merchant contact widget；
- old comments；
- pagination。

因此：

```text
article HTML preserved
≠
interactive DIY experience preserved
```

尤其不要用当前产品数据库重新填补历史配置器里已经丢失的 SKU 后，再把结果当 historical original。

---

## 14. 广告、媒体与商家角色歧义

旧硬件门户同时可能扮演：

- 新闻媒体；
- 产品数据库；
- 广告渠道；
- 经销商黄页；
- 导购；
- 论坛；
- 活动组织者；
- 厂商合作推广方。

因此一篇“性价比推荐”不能默认是独立测评。

抽取 claim 时建议记录：

```yaml
content_role:
  value: editorial / sponsored / dealer_quote / user_build / press_release / unclear
source_relationship:
  value: independent / vendor-provided / syndicated / unclear
```

增加 **editorial-commerce role ambiguity / 编辑—商业角色歧义**。

---

## 15. 与海外 pre-Web / Usenet 的边界比较

本仓不展开全球 PC hobby 史，但 companion life-history note 已记录：

- 1975 Homebrew Computer Club newsletter 通过线下会议、纸质通讯、团购和共享知识帮助个人低成本建立家用计算系统；
- 1997 `comp.sys.ibm.pc.hardware.*` FAQ 已经把主板、CPU、价格、购买和硬件问题做成 Usenet 的持续知识层。

这些只作为边界提醒：

> 中国 2000s DIY 门户的“论坛 + 参数库 + 行情 + 配置器”不是 Internet 第一次让爱好者交流硬件，而是中文 Web 在特定电脑城/零售生态里形成的一种高度数据库化版本。

全球材料不写入本仓主线。

---

## 16. M1 archive 验证状态

本轮已取得并实际阅读多个**当前仍可访问、带历史正文日期的 legacy pages**，包括：

- `news.zol.com.cn/2003/0129/54867.shtml`（2003 正文）；
- `diy.zol.com.cn/38/383201.html`（2006 正文）；
- `diy.zol.com.cn/38/385268_all.html`（2006 正文）；
- `zdc.zol.com.cn/106/1062657.html`（2008 正文）；
- 新浪保存的 2004/2008 同期转载页面。

同时定位了 2005 搜狐智能装机 original locator：

```text
http://act.it.sohu.com/jiutian/index.htm
```

但本轮**没有取得并检查一份满足 M1 门槛的 2002—2010 中文 PC DIY configurator/forum 的 verified Wayback/WARC capture**。

因此以下历史状态保持 `unknown`：

- 搜狐装机器原 HTML/charset；
- JS / iframe；
- product DB 请求；
- compatibility rule implementation；
- benchmark prediction backend；
- session/cookie；
- saved build URL pattern；
- ZOL 2006 模拟攒机原 transaction 页面；
- 用户配置单历史 DOM；
- 当时论坛附件/图片；
- 历史商家库存和真实成交。

结论必须写成：

**M1 NOT ACHIEVED IN THIS SLICE**。

不能写成“Wayback 没有”或“系统无法复原”，除非后续按 METHOD 记录过明确 archive 搜索范围并验证失败。

---

## 17. 已证实 / 高概率 / 不知道

### 已证实

- 2003—2004 中文 IT Web 已将行情、评测、论坛和实体 DIY 市场连接；
- 2005 搜狐被同期媒体报道推出数据库化智能装机系统，并留下 original URL；
- 2006 ZOL 明确存在模拟攒机、用户配置库和周期性专家点评；
- 2008 DIY 门户仍把学生开学视为重要装机时点，同时承认笔记本/品牌机挤压；
- 今天仍有多个 legacy pages 承载这些年份的正文。

### 高概率但待 capture 复核

- 模拟装机的 transaction 层依赖服务器数据库和 session，而非纯静态 HTML；
- 许多历史配置单今天即使还能渲染，也可能混入后来的产品状态与页面模板；
- 当前旧文章中的动态价格/商家/推荐模块不能自动视为历史值。

### 不知道

- 2005 搜狐 configurator 当年的具体浏览器兼容要求；
- 是否使用 GB2312/GBK、何种 JS/iframe 架构；
- 推荐算法与兼容规则的真实实现；
- 性能预测误差是否被独立验证；
- 2006 ZOL saved-build 的原 URL/schema；
- 论坛用户实际购买率、点亮率和长期稳定率。

---

## 18. 后见之明风险

不要写：

- “2000s 用户已经像今天一样网购散件”——早期 Web 长期与实体电脑城、电话、柜台共存；
- “配置器解决了兼容问题”——它最多降低部分信息摩擦；
- “IDE 用户当时显然应该买 SATA”——当时价格、主板接口和现有设备都影响判断；
- “笔记本兴起后 DIY 结束”——它后来继续作为高性能、游戏、工作站、审美与小型化路线存在；
- “旧文还能打开，所以旧网站保存完好”——current live legacy render 可能跨越二十年模板和数据库迁移。

---

## 19. 它改变了我们对中文旧 Web 的哪一点理解

PC DIY 说明，2000s 中文门户并不只是“网页上有很多文章”。它们曾试图成为一种**购买前计算环境**：用户可以在真实零件还没到手以前，把预算、用途、参数、价格、接口、未来升级和跑分先组成一台虚拟机器。

这也是一种很容易被 archive 误判的旧 Web：

> 今天剩下的往往是文章和参数页，看起来资料极其丰富；真正最能改变普通人行为的动态配置器、价格 feed、session、用户 build、商家库存和离站购买过程却可能已经消失。

所以旧 Web 的“内容保存率很高”，完全可能与它的**事务能力和决策能力保存率很低**同时成立。