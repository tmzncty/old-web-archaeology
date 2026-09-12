# Pager user-count source scope, failed forecasts, and “online paging” terminology probe（1998—2005）

## 0. Scope guard

本文件**不是新的寻呼 / QQ state-gap 总论**。

仓库已经有：

- `PAGER_WEB_GATEWAY_EMAIL_TO_PAGER_AND_REACHABILITY_STATE_GAPS_1999_2007.md`；
- `docs/PAGER_GATEWAYS_ONLINE_PAGING_AND_CROSS_NETWORK_DELIVERY_GAPS_1998_2002.md`；
- `docs/PAGER_WEB_GATEWAY_OICQ_QQ_PRESENCE_OFFLINE_MESSAGE_AND_MOBILE_HANDOFF_STATE_GAPS_1998_2015.md`；
- `docs/QQ_WEB_PRESENCE_ONLINE_AWAY_INVISIBLE_WATCHER_BADGE_AND_AVAILABILITY_STATE_GAPS_2000_2015.md`。

本 probe 只处理三个方法问题：

1. 同样写作“寻呼用户”的数字为什么不能自动拼成一条序列；
2. 一个后来失败的 1999 年行业预测为什么是重要 old-Web artifact；
3. “寻呼”一词怎样迁移到 OICQ/QQ 等 early Internet 语汇，而不能因此误写成网络层连续。

完整普通生活史和跨国 life-course 比较写回 `tmzncty/how-people-lived`：

`/sources/pager-future-forecast-statistical-universe-and-substitution-hindsight-1998-2005.zh-CN.md`

---

## 1. 第一条证据链：国家统计局的 contemporaneous statistical series

国家统计局《中国统计年鉴 2005》长期表：

- https://www.stats.gov.cn/sj/ndsj/2005/html/P1640C.HTM
- https://www.stats.gov.cn/sj/ndsj/2005/html/P1639C.HTM

以“万户”为单位，给出：

| 年份 | 年末无线寻呼用户 | 年末移动电话用户 |
|---|---:|---:|
| 1998 | 3908.2 | 2386.3 |
| 1999 | 4674.5 | 4329.6 |
| 2000 | 4884.3 | 8453.3 |
| 2001 | 3606.4 | 14522.2 |
| 2002 | 1872.1 | 20600.5 |
| 2003 | 1057.6 | 26995.3 |
| 2004 | 395.2 | 33482.4 |

2005 年 12 月通信行业统计月报：

- https://www.miit.gov.cn/gxsj/tjfx/txy/art/2020/art_b18e780c481745239acd2fc69364e2a3.html

又给出：

- 无线寻呼用户 97.1 万户；
- 移动电话用户 39342.8 万户。

**Evidence grade: A — government statistical tables.**

但这里的 A 只说明“这张表确实这样统计”，不自动说明它覆盖所有后来历史叙述中被叫作“寻呼用户”的对象。

---

## 2. 第二条证据链：later institutional history 给出另一组明显不同的数字

中国电信博物馆 2023 年文章：

- https://museum.chinatelecom.com.cn/yj/txkp/202303/t20230327_73688.html

写道：

- 1998 年国内寻呼机用户“突破 6546 万”；
- 2000 年全国寻呼用户达到 8400 万；
- 2002 年后行业曾尝试以 Internet 为依托的网上寻呼、Web 网页寻呼、网上秘书和电子邮件业务；
- 2007 年多数地区无线寻呼网络退出。

这与 NBS 年鉴同年数字的差距不是普通四舍五入：

```text
1998:
NBS = 3908.2 万
later museum history = 6546 万+

2000:
NBS = 4884.3 万
later museum history = 8400 万
```

本轮没有找到后者 6546 / 8400 的原始统计表或明确 statistical universe。

因此**不得做以下任一动作**：

- 用 later history 覆盖 NBS；
- 反过来把 later history 标成“错误”；
- 把二者平均；
- 选更符合大众记忆的一个；
- 假设一个是设备数、一个是用户数而没有原始定义证据。

永久规则：

> **`same metric label != same reporting universe != directly comparable series`**

需要追查的 scope 变量至少包括：

- reporting body；
- public vs private / dedicated paging systems；
- carrier coverage；
- registered vs active vs paying accounts；
- user account vs terminal / device；
- year-end vs intra-year peak；
- later historical aggregation vs contemporaneous statistical reporting。

这是一种 **statistical-universe gap**，而不是“哪张网页更权威”就能解决的问题。

---

## 3. 第三条证据链：1999 年 live-origin 新闻页保存了一个后来失败的未来

当前仍可访问：

- https://tech.sina.com.cn/news/computer/1999-12-08/12840.shtml

页面标题《寻呼业仍大有可为》，显示日期 1999-12-08，并标明来源《光明日报》。文章采访南京邮电学院通信工程系王世顺。

文本包含非常明确的 future claim：

- 当时估计全国寻呼用户约 7000 万；
- **预计到 2005 年达到 1.3 亿**；
- 同时认为手机用户虽在迅速增长，但受购买力制约，2005 年达到同样 1.3 亿并不容易；
- 未来增长对象包括农村用户、学生和专业用户；
- 技术路线包括更高技术含量的寻呼系统。

**Content evidence grade: B — contemporaneous newspaper interview text surviving at a live origin URL.**

### 3.1 不能把当前页面误写成 verified 1999 Web capture

当前可以观察的是：

```text
old-looking Sina URL
+
1999 display date
+
article body surviving now
```

本轮**没有**取得：

- 1999 capture datetime；
- historical HTTP / replay result；
- historical Content-Type；
- charset；
- DOM；
- original CSS / image resources；
- browser assumptions；
- second historical capture。

因此：

> **`1999 text at live origin in 2026 != verified 1999 interface artifact`**

本轮搜索也没有得到可实际打开并完成 METHOD 合同的 Wayback locator。

这只表示：

`verified historical capture opened = false`

绝不表示：

`Wayback never captured it`。

### 3.2 为什么“错误预测”反而是高价值 artifact

技术史的后来叙述会天然保留赢家：

- 手机用户增长；
- pager 用户下降；
- 网络关闭；
- QQ / 移动 Internet 兴起。

如果只看后来历史，1999 年就会被重写成：

> “大家已经知道 pager 将死，只是在等手机更便宜。”

但 F3 保存了一个 contemporaneous alternative future：

```text
pager continues expanding
+
new rural/student/professional markets
+
higher-tech paging
+
mobile grows in parallel
```

这增加一种 old-Web archive asymmetry：

> **`outcome-survival / failed-future loss asymmetry`**

赢家的结果最容易进入年表；失败的预期往往只有偶然保存的旧新闻、论坛和行业报道才能让我们看到。

所以一个预测即使完全错误，仍是研究当时人时间感的一手对象。

---

## 4. 2000：腾讯保存文本显示“网上寻呼”曾是 early IM 的解释词汇

腾讯当前公司历史页面：

- https://www.tencent.com/zh-cn/articles/80257.html

页面标注 2000-05-27，并说明 2000-05-28《人民日报》转载；文本把同时在线首次突破十万的 QQ 称为：

> “国产免费网上寻呼软件”

这条材料与仓库现有 pager → OICQ/QQ 边界研究相容，但需要进一步细分证据对象。

### 4.1 当前 corporate history page 不是 2000 Web artifact

本轮没有取得 2000 年 Tencent 页面的 historical capture。

所以可以说：

- 腾讯当前历史档案**保存了一段标记为 2000 年、并称被《人民日报》转载的文本**；
- 该文本使用“网上寻呼软件”来描述 QQ。

不能说：

- 当前 DOM 就是 2000 DOM；
- 当前 URL 就是 2000 original URL；
- 当前 CSS / layout / charset 代表 2000；
- 该词一定来自腾讯当时的 first-party product taxonomy，而不是转载文本的媒体表述。

证据等级应拆成：

```text
textual survival: B/C boundary
historical interface: UNKNOWN
historical original URL: UNKNOWN in this probe
```

### 4.2 terminology migration != protocol migration

“网上寻呼”很容易诱发错误技术推断。

必须保留：

```text
word “paging” survives
!=
radio paging infrastructure survives underneath
```

它可能只是用一个普通人已经熟悉的通信概念，解释新 Internet IM：

- 找到某个人；
- 对方在线时即时联系；
- 对方不在线时留下消息；
- 关系地址从地点移动到个人标识。

因此新增规则：

> **`terminology continuity != transport continuity != service-state continuity`**

---

## 5. 海外 sanity check：late-1990s 美国行业也把未来押在 two-way paging 上

这部分不扩展仓库 scope，只用于检验“寻呼升级而不是死亡”的未来是不是中国特有。

RCR Wireless 同期行业材料：

- 1998-03-23: https://www.rcrwireless.com/19980323/archived-articles/two-way-to-bring-more-users-and-money-to-industry
- 1998-08-17: https://www.rcrwireless.com/19980817/archived-articles/carriers-approach-two-way-with-different-strategies
- 1998-08-31: https://www.rcrwireless.com/19980831/archived-articles/bellsouth-tackles-two-way-market

这些文章明确把 two-way paging 写成下一阶段增长路线，并介绍：

- 双向文字；
- e-mail；
- nationwide roaming；
- delivery / read acknowledgement；
- 更小的 wearable terminal。

2004 年 Washington Post 的后来回顾则称，美国 paging 用户从 1998 年约 4500 万峰值下降到约 1200 万，而 cellular users 已超过 1.57 亿：

- https://www.washingtonpost.com/archive/business/2004/03/30/pager-firms-will-merge/f369f409-2455-45c9-bd14-a66c5a3f3aa8/

所以：

`failed pager-upgrade future` 不是中国特有现象。

这也警告我们，不要把后来的 smartphone / cellular convergence 倒写成 1998 年唯一可见的技术终局。

---

## 6. Archive / source rules added by this probe

### 6.1 Statistical-universe gap

```text
same noun in two tables
!=
same counted object
```

尤其面对：

- 用户；
- 账户；
- 终端；
- 在线用户；
- 注册用户；
- 付费用户；
- 业务用户；
- 全国 / 某运营体系用户。

### 6.2 Forecast-survival / outcome-hindsight gap

```text
later outcome known
!=
earlier outcome predictable
```

错误预测可以是高质量 historical evidence，因为它保存 contemporaneous option set。

### 6.3 Live-origin content / historical-interface gap

```text
old article survives on original/current publisher domain
!=
1999 HTML survives unchanged
```

内容史与界面史必须拆开。

### 6.4 Terminology / transport gap

```text
“网上寻呼”
!=
traditional paging network transported the message
```

术语可以跨技术栈迁移。

---

## 7. Counterexamples and hindsight risks

- 1999 新浪/光明日报文章开头本身就记录了“寻呼命运岌岌可危”的另一派判断；因此不能制造“当时所有人都看多 pager”的假共识。
- NBS 序列里 1999 mobile users 已非常接近 pager users，2000 已显著反超；手机替代风险并非不可见。
- later museum history 的 8400 万不能因为与“大众记忆中的鼎盛期”一致就自动优先于 contemporaneous NBS 表。
- current live Tencent / Sina pages 的内容生存不能证明原始页面技术生存。
- US two-way paging 是比较对象，不是中国 OICQ / pager 的实现证据。

---

## 8. Unknowns / next artifact work

1. 找出 6546 万 / 8400 万的第一手统计来源和统计定义；
2. 找到 1999 新浪文章的可打开 historical capture，并按 `docs/METHOD.md` 记录 capture datetime、charset、DOM 与子资源；
3. 找到《人民日报》2000-05-28 QQ 转载的原始版面或数字化报纸 artifact；
4. 找到 1999—2002 中国“网上寻呼”产品页 / 帮助页的 verified captures；
5. 对比至少两个 historical timepoints，观察“网上寻呼”词汇何时让位于“即时通信 / IM / QQ”；
6. 不把统计口径问题提前解释掉，直到拿到 source metadata。

---

## 9. M1 status

本 probe 新增了：

- 一条 official statistical series；
- 一条后来机构史的冲突 series；
- 一个 1999 live-origin contemporaneous failed-future text；
- 一个 2000 corporate-history textual-survival lead；
- 一组海外 two-way paging sanity checks。

但本轮没有打开满足最低合同的 historical archive capture。

因此：

> **M1 verified historical pager / online-paging Web capture: NOT ACHIEVED IN THIS SLICE.**

这份文件的价值是先把 source universe、forecast artifact 和 terminology migration 分开，避免下一次 artifact reconstruction 在错误的统计和技术前提上继续扩张。