# 中文旧网消费者投诉：提交、转交、回复与现实补救之间的状态缺口（2004–2015）

> Scope: 约 2004–2015 中文 Web 的消费者投诉/维权页面、第三方投诉平台和投诉入口。本文不写完整消费者保护史，也不把 2017 后全国 12315 互联网平台倒灌回旧网时代。

Companion life-history study:  
`tmzncty/how-people-lived/topics/consumer-redress-complaint-routing-evidence-and-remedy-executability-china-1983-2026.zh-CN.md`

Status: research note / state-model companion  
Last research pass: 2026-09-06

## 0. 为什么需要单独建模

旧中文 Web 很容易留下：

- “我要投诉”入口；
- 一条公开投诉正文；
- 商家回复；
- `处理中 / 已回复 / 已解决 / 已完成` 标签；
- 平台自己发布的投诉数量、点击量和解决率。

但真正决定消费者是否得到补救的状态往往在页面之外：

- 发票、订单号、手机号；
- 平台内部审核；
- 转给哪个企业联系人；
- 商家是否真的打过电话；
- 退款是否进银行账户；
- 维修是否完成；
- 赔付承诺是否履行；
- 行政机构是否正式受理；
- 用户后来是否放弃。

因此：

```text
public complaint artifact ≠ complete dispute transaction
```

本文的目标，是防止研究者从“一个公开页面还活着”直接跳到“这次维权成功了”。

---

## 1. 研究对象必须先拆层

### 1.1 经营者自己的售后入口

例如：

```text
在线客服
售后表单
退换货申请
```

这是 seller/platform internal service state。

### 1.2 第三方公开投诉平台

例如 2000s 的“315 消费电子投诉网”等。

典型功能可能包括：

```text
消费者发帖/填表
→ 平台审核
→ 公开展示
→ 联系企业
→ 企业回复
→ 平台修改状态
```

它不是官方 12315，也不是法院。

### 1.3 媒体投诉/曝光入口

2008 年央视 3·15 页面同时提供电话、短信、网络、播客等线索提交方式，并说明会把信息汇总给有关部门寻求解决方案。

Source (A/B, contemporaneous Sina 2008 special page):  
https://finance.sina.com.cn/focus/jj315/index.shtml

媒体收集线索与行政投诉也不是同一状态。

### 1.4 官方行政/消协线上入口

2000s 各地可能存在地方工商/12315 网络系统、信箱或页面，但 2017 年“全国12315互联网平台”才正式上线；2019 年全国平台进一步完成五线整合。

因此禁止：

```text
2008 年一个“网上 315”页面
→ 自动写成今天 www.12315.cn 的历史版本
```

---

## 2. 第三方公开投诉平台最小状态机

以 2000s 消费投诉站为抽象对象：

```text
现实交易发生
→ 用户发现争议
→ 用户取得/保存证据
→ 找到投诉站
→ 注册/识别状态满足
→ 填写投诉
→ 浏览器发送请求
→ 服务端收到
→ durable complaint record 形成
→ moderation / validity check
→ 投诉被接受或拒绝
→ 公开页面生成（若平台公开）
→ 平台选择/识别企业
→ 转交企业联系人
→ 企业真正看到
→ 企业回复平台 / 用户
→ 用户真正看到回复
→ 双方协商
→ 商家承诺补救
→ 退款 / 维修 / 换货 / 履约真正发生
→ 平台修改状态
→ 页面后续保存 / 删除 / 迁移
```

必须保留：

```text
submit clicked ≠ durable complaint record
record exists ≠ accepted as valid
valid ≠ fact independently verified
public ≠ forwarded
forwarded ≠ merchant encountered
merchant replied ≠ consumer saw reply
reply ≠ remedy promised
remedy promised ≠ remedy fulfilled
platform says resolved ≠ independent proof of real-world remedy
```

---

## 3. `valid / invalid` 是平台分类，不是司法事实判断

2008 年新华社/搜狐转载“315 消费电子投诉网”的空调投诉统计：平台称上半年收到 401 宗投诉，其中 28 宗因“投诉内容不实、联系方式虚假等”被判为无效，373 宗有效；截至 7 月 1 日又称 321 宗“得到解决”。

Source (B, contemporaneous media reproducing platform report):  
https://news.sohu.com/20080731/n258506165.shtml

这个 artifact 能证明：

- 平台当时使用了有效/无效分类；
- 平台当时发布了“已解决”的统计标签；
- 第三方媒体在 2008 年公开转载这些数字。

它不能单独证明：

- 每个有效投诉的事实完全真实；
- 28 个无效投诉全是恶意造假；
- 321 个“解决”都发生了退款/维修；
- 该比例代表全国空调售后质量。

因此：

**platform validity state ≠ adjudicated truth state。**

---

## 4. `processed / completed / resolved` 必须记录字段语义

315ts 在其新浪博客 2008 年 8 月发布卖场投诉统计时称，上半年有效投诉 1003 宗，并称截至 8 月 20 日 94.52% “已经处理完毕”。

Source (A/B, contemporaneous platform-authored post on hosted blog):  
https://blog.sina.com.cn/s/blog_50315b110100al1e.html

这类旧页面尤其危险，因为研究者很容易把百分比读成：

```text
94.52% consumers got what they wanted
```

而原文实际上只足够证明平台声称某种“处理完毕”状态。

以后每次遇到状态字段都应问：

- 谁能把它改成 completed？
- 平台员工、企业还是消费者？
- 企业只要回复就算 completed 吗？
- 消费者必须确认吗？
- 无法联系消费者会不会也关闭？
- 部分补救算不算 resolved？
- 关闭后还能 reopen 吗？

在没有当时帮助页/数据库逻辑前，全部保持 `unknown`。

---

## 5. 投诉量没有交易分母：archive 会制造“品牌故障率幻觉”

2008–2009 的媒体经常直接引用投诉站统计某类手机、卖场、空调或通讯购物投诉多少宗。

例如 2009 年《法制晚报》报道 315 消费电子投诉网 5 月收到 15681 件投诉，其中通讯购物投诉 2322 件。

Source (B, contemporaneous media report):  
https://news.sina.com.cn/c/2009-06-10/131915766312s.shtml

但：

```text
complaint count ≠ defect rate
```

至少还缺：

- 销量 / 活跃用户数；
- 使用时长；
- 投诉站在该品牌用户中的知名度；
- 企业是否主动把用户导向该平台；
- 某一事件是否突然引发集中投诉；
- 重复投诉如何去重。

所以不能从 archive 中“某品牌投诉页面很多”直接得到“它是当时最差品牌”。

这叫 **complaint-denominator gap / 投诉分母缺口**。

---

## 6. 公开页面会过度保存危机，而不保存“我懒得投诉”的人

公开投诉站天然选择：

- 问题严重到愿意发帖的人；
- 会用网络的人；
- 知道该网站的人；
- 愿意把纠纷公开的人；
- 还没有完全放弃的人。

它不容易保存：

- 觉得几十元不值得折腾而放弃的人；
- 打电话解决以后从不发帖的人；
- 直接得到商家退款的人；
- 没有电脑或不会填表的人；
- 只在私人 QQ 群讨论的人。

因此 old-Web 会产生 **redress-crisis survival bias / 维权危机幸存偏差**。

旧网留下很多“愤怒、投诉、求助”，不能据此重建成“所有消费都在危机中”。

---

## 7. 公开投诉站既是救济中介，也是有自身激励的平台

2011 年《新京报》报道 315 消费电子投诉网被有关部门关闭，并记录围绕收费、企业会员、投诉隐藏和曝光机制的调查与争议。

Source (B, contemporaneous report, mirrored later; allegations and official enforcement claims must be attributed):  
https://www.doit.com.cn/p/83562.html

这条材料的意义不是让仓库判断每个历史投诉是真是假，而是证明：

**complaint intermediary itself is an actor。**

它可能决定：

- 哪些内容通过审核；
- 哪些内容公开；
- 如何联系企业；
- 什么条件算“处理完成”；
- 哪些企业被突出展示；
- 页面何时隐藏或删除。

所以：

```text
consumer ↔ complaint platform ↔ merchant
```

不是一条透明管道，而是三方系统。

新增 **intermediary-governance gap / 中介治理缺口**。

---

## 8. 平台死亡会把维权证据本身带走

上述 315 消费电子投诉网在 2011 年关闭，意味着此前大量投诉页面、回复、状态标签和外链可能同时失效。

这产生 **redress-platform mortality / 救济平台死亡**：

```text
当年公开过
≠ 今天仍能访问
```

甚至：

```text
当年用户把投诉页当成公开证据
→ 平台后来消失
→ 今天只剩新闻引用、搜索摘要、博客转载或零散 archive
```

因此 old-Web 研究必须把“投诉平台是否活着”与“当年纠纷是否解决”分成两只钟。

---

## 9. 2008 的网络交易增加 `evidence-page / evidence-durability gap`

同期消费者报道已经提醒网购者保留电子交易单据、邮件确认等，因为商品页面可能更新。

Source (B+, contemporaneous Beijing consumer report):  
https://news.sohu.com/20080204/n255066846.shtml

旧网考古时尤其要警惕：

```text
archive captured current product page at T2
≠ consumer saw same representation at purchase time T1
```

一项争议可能真正依赖：

- 下单瞬间的商品描述；
- 当时价格；
- 当时承诺的赠品/保修；
- 当时退货规则；
- 登录后订单详情。

Wayback 往往更容易保存公开商品壳层，而不是用户的 authenticated order state。

因此新增：

**public-offer / private-order asymmetry。**

---

## 10. 2010s 前半：电话、Web、媒体和第三方平台长期并存

不要把历史写成：

```text
电话投诉 → 被 Web 替代
```

更常见的是：

```text
12315 电话
+ 来信来访
+ 地方政府/工商网页
+ 企业客服
+ 媒体热线
+ 第三方 315 网站
+ 论坛/博客曝光
```

共同存在。

2013 年工商系统依托 12315 网络处理各类消费者诉求时，官方报道仍把 1999 的 12315 电话作为制度起点。

Source (A/B, People’s Daily report using SAIC statistics, 2014):  
https://politics.people.com.cn/n/2014/0315/c1001-24641803.html

因此早期 Web 更应该被理解为**增加新的 entry points 和 public visibility**，而不是删除电话和窗口。

---

## 11. 与 2017/2019 后全国平台的边界

为了防止 scope creep，本仓只把后期全国平台作为下游边界说明：

- 2017-03-15 全国 12315 互联网平台正式上线；
- 2019-08-31 全国平台完成五线整合。

Sources:  
https://www.cac.gov.cn/2017-03/15/c_1120630167.htm  
https://www.samr.gov.cn/wljys/sjdt/art/2023/art_b3139687c63c4352b474d616c8a37ac6.html

这些时间点反过来说明：

**2004–2010 的“网上投诉”不能默认就是统一全国行政 Web 平台。**

本文件不继续追踪 2017 后 App / 微信小程序 / ODR 技术细节；那部分主要属于 how-people-lived 的长期制度比较。

---

## 12. 两套不同状态机绝不能合并

### 12.1 第三方公开投诉平台

```text
consumer post
→ moderation
→ public page
→ platform forwarding
→ merchant response
→ public status
→ possible remedy
```

### 12.2 行政/消协渠道

```text
complaint submission
→ identity / subject / jurisdiction check
→ acceptance
→ assignment
→ investigation / mediation
→ outcome
→ fulfillment
→ closure
```

一条第三方页面显示“企业已回复”，不能推断行政机关已经立案或调解。

一条行政系统显示“办结”，也不等于历史 Web 上一定存在公开投诉页。

---

## 13. 关键 state gaps

### G-01 — seller-CS / external-escalation gap

经营者客服拒绝或拖延后，消费者是否真的转向外部渠道？

### G-02 — complaint-form / durable-record gap

浏览器提交成功画面不证明后台持久化记录已经形成。

### G-03 — moderation / truth gap

平台判断“有效”不是司法判决，也不等于事实完全核验。

### G-04 — public-page / official-case gap

第三方公开投诉页不等于正式行政案件。

### G-05 — forwarding / merchant-encounter gap

平台标记“已转交”不证明正确企业联系人真正看到。

### G-06 — merchant-reply / remedy gap

公开回复可能只是解释、道歉、要求补材料或否认责任。

### G-07 — promise / fulfillment gap

“同意退款”与银行卡真正到账不是同一个状态。

### G-08 — platform-resolved / user-satisfied gap

平台关闭 ticket 的规则可能和消费者认为“解决”的条件不同。

### G-09 — complaint-count / defect-rate gap

投诉数量没有销售/活跃用户分母时不能解释产品故障率。

### G-10 — screenshot / historical-interaction gap

截图不保存 form action、session、状态变更权限和后台转交。

### G-11 — public-offer / private-order gap

公开商品页可以 archive，真实订单/付款/售后状态通常在认证后。

### G-12 — redress-platform-mortality gap

当初用于公开维权的平台后来可能关闭，页面状态链断裂。

---

## 14. Archive 保存偏差：public complaint shell / private remedy state asymmetry

最容易公开保存的是：

- 标题；
- 消费者叙述；
- 品牌名；
- 平台状态标签；
- 商家公开回复；
- 点击量/评论数。

最不应该公开、也最难保存的是：

- 身份证；
- 完整手机号；
- 地址；
- 银行卡；
- 订单号；
- 发票原件；
- 客服工单；
- 私人邮件/QQ；
- 退款流水；
- 内部审核备注。

因此 archive 常常保存的是**纠纷的公共壳层**，而不是能够证明最后是否退款的**私人补救状态**。

这不是一个应通过泄露数据强行补全的缺口。

---

## 15. Historical locator 与 M1 状态

目前高价值 historical locator：

```text
www.315ts.net
```

2008 年平台自己的新浪博客明确把该域名写为“315 消费电子投诉网”网址：

https://blog.sina.com.cn/s/blog_50315b110100al1e.html

但本轮**没有实际取得并检查一份满足 M1 门槛的 historical Wayback/WARC transaction capture**。

因此以下全部保持 `unknown`：

- 2008 主站真实 charset；
- HTML / frames / table / JS 结构；
- 注册是否必需；
- 投诉表单 field names；
- form action / POST target；
- CAPTCHA；
- cookie / session；
- 投诉 ID 生成方式；
- “有效/无效”后台字段；
- “处理完毕/解决”谁能修改；
- 企业是否有专门登录后台；
- 企业回复是 API、后台、邮件还是人工录入；
- 投诉内容删除/隐藏规则；
- 原站关闭前后的 URL redirect / archive behavior。

Candidate locator ≠ verified capture。

---

## 16. 浏览器与编码边界

在没有历史 capture 以前，不推断：

- IE6-only；
- ActiveX；
- GB2312 / GBK / UTF-8；
- JavaScript validation；
- iframe / frameset；
- 上传附件的技术限制。

即使新浪博客和今天的新闻页面能在现代 Chromium 正常显示，也不能证明 `www.315ts.net` 当年的浏览体验。

---

## 17. 隐私 stop conditions

旧投诉页极易包含普通人的敏感生活信息。研究中禁止：

- 重建或批量公开完整手机号、地址、身份证、订单号；
- 用用户名 + 品牌 + 城市反向识别投诉者；
- 搜索泄露数据库补后台状态；
- 登录遗留账号；
- 用现在仍有效的联系方式联系历史投诉者；
- 为了证明退款而搜集私人银行流水或客服工单。

需要研究状态结构时，优先抽象字段和流程，不保存个人识别值。

---

## 18. 后见之明风险

### 风险 A：把所有“315”当官方

品牌名带 `315`、页面写“维权”，并不证明它属于工商/市场监管行政系统。

### 风险 B：把 modern 12315 状态机倒灌回 2008

2017 全国互联网平台、2019 五线整合是后来的制度层。

### 风险 C：把平台自报解决率当第三方审计

平台有自己的分类、关闭规则和商业激励。

### 风险 D：只因为公开帖能搜索到，就以为当时消费者主要通过公开 Web 维权

电话、来信、窗口、企业客服和私人关系一直并存。

### 风险 E：从投诉 archive 重建“消费者情绪总体”

最平静、最快解决、最早放弃的纠纷最不容易留下公开页面。

---

## 19. 已证实 / 高概率 / 不知道

### 已证实

- 2008 年 `www.315ts.net` 作为第三方消费投诉平台名称/域名出现在同期平台自述与媒体材料中；
- 平台使用“有效/无效”“处理完毕/解决”等状态词并发布统计；
- 2000s 电话、媒体、第三方 Web 投诉入口共存；
- 2011 年该平台被关闭，历史页面生命周期中断；
- 2017 全国 12315 互联网平台才正式上线，不能倒灌到 2008。

### 高概率但未做 transaction verification

- 普通投诉页面至少需要服务端持久化和某种状态更新逻辑；
- 企业回复需要平台与企业之间某种转交通道；
- 公开展示字段必然只是完整后台 dispute state 的子集。

### 不知道

- 2008 原 DOM、浏览器/编码；
- 用户和企业权限模型；
- attachment / CAPTCHA / session 技术；
- `resolved` 的精确定义；
- 真实退款与平台状态的逐案一致程度。

---

## 20. 下一步最值钱的证据

优先级不是再找更多“某品牌被投诉多少次”的新闻，而是：

1. 一份 2006–2010 `www.315ts.net` 实际 archive capture；
2. 同期帮助页/投诉指南，解释状态字段和用户操作；
3. 一份同时代企业侧说明，证明投诉如何被转交和回复；
4. 同一个公开投诉在两个时点的 capture，用来观察状态从 `pending → replied/resolved` 是否发生变化；
5. 如果能合法获得，比较主页面与无登录/已登录状态的差异，但不接触私人账号。

达到这些条件以后，才值得把本研究升级成 M1 级完整旧网案例的一部分。

## 21. 本轮结论

旧中文 Web 让消费纠纷第一次更容易变成**可搜索、可公开、可聚合同类问题的页面对象**，但页面对象不是现实补救本身。

对旧网考古最重要的边界是：

> **一条投诉页可以证明“这个争议曾以这种形式进入公共 Web”，却不能独自证明它怎样进入企业/监管后台，更不能仅凭一个绿色的“已解决”标签断言钱已经回到消费者手里。**
