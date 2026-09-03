# Internet Cafe Public Access: Session Environments, Identity Gates, and Client-State Gaps, 1997–2008

> Scope: 约 1997–2008 的中文互联网公共上网场景。研究对象不是“网吧行业史”，也不是全球 cybercafe 史，而是一个旧网考古问题：**当历史用户通过网吧公共终端进入中文 Web 时，公开网页档案究竟能证明什么，又缺失了哪些决定真实浏览体验的本地/后台状态？**

跨国公共接入前史与普通生活意义写入 `tmzncty/how-people-lived`：

- `topics/internet-cafes-public-access-and-session-based-digital-life-china-1994-2025.zh-CN.md`

本文件遵守 `docs/METHOD.md`：platform / venue / client / account / page / capture / claim 不混写；`exists / available / used / popular / caused` 不互相替代。

---

## 1. 为什么网吧是旧网考古的一个独立对象

传统 Wayback 式研究把重点放在服务器端：

```text
historical URL
→ archived HTML
→ archived subresources
→ replay
```

但一个 2001 年网吧用户实际经历的是：

```text
venue open
→ empty seat
→ billing/session starts
→ local client unlocks
→ browser / launcher / proxy / LAN state
→ Internet route works
→ target site reachable
→ account login succeeds
→ local temporary state accumulates
→ session ends
→ billing closes
→ machine is reused / restored / cleaned
```

这两条链只重叠一部分。

因此：

> `historical page capture ≠ historical public-terminal session`

即使服务器端页面 100% 保存，也可能完全不知道当时公共机器能否进入它、如何进入它、用什么浏览器看到它、哪些账号/插件/下载工具在本地发挥作用。

---

## 2. 研究单位

本题至少必须拆开以下对象：

### venue

一个具体网吧/网络咖啡屋的实体营业地点。

### venue service layer

收费、营业时间、会员/临时卡、包时、身份登记、机位分配。

### client machine

某一台公共 PC，包括：

- OS；
- browser；
- IM/game/download clients；
- fonts / input method；
- plugins；
- local cache；
- restore software；
- proxy / network settings。

### session

一名用户从上机计时到下机的一段临时执行状态。

### network route

网吧出口、ISP、代理、防火墙、DNS、带宽与路由条件。

### web page / platform

用户试图访问的远端 Web 对象。

### personal account

QQ、email、BBS、game、portal 等用户身份。

### archive capture

今天留下的一份服务器端或媒体端历史 artifact。

不能因为某品牌网吧在 2003 年存在，就默认它所有分店、所有机器、所有月份使用同一客户端镜像。

---

## 3. 最小 execution state machine

建议以后凡涉及“某人在网吧打开了某中文旧站”的 claim，至少经过以下状态：

```text
V0 venue exists
V1 venue is open at that date/time
V2 free/usable terminal exists
V3 user is eligible to enter/use the venue
V4 required identity/document/card is accepted
V5 billing/session is opened
V6 terminal is unlocked / assigned
V7 local browser/client starts
V8 network route and DNS work
V9 target host is reachable
V10 page/service renders in that historical client
V11 account authentication, if needed, succeeds
V12 user executes intended action
V13 local/cache/download/session state is created
V14 session ends
V15 billing is settled
V16 local state is cleared, restored, retained, or overwritten
```

因此必须固定：

```text
venue exists != venue open
venue open != seat available
seat available != user eligible
identity recorded != session opened
session opened != Internet works
browser installed != target renders
site reachable != account login succeeds
login succeeds != intended action succeeds
session ended != local state wiped
```

---

## 4. Evidence anchor A/B/C/D

### E1 — 北京 1996–1997 网络咖啡屋：公共终端真实存在并被不同任务使用

2019 年《北京日报》历史版重新展示/整理 1996、1997 年本报旧版，明确给出：

- 1996-11-19 “实华开网络咖啡屋”营业；
- 1997-01 记者探访时有 11 台奔腾电脑；
- 可见用户行为包括 email、查资料、聊天、网络游戏；
- 1996 年网吧上机收费约 30 元/小时。

Sources:

- <https://media.people.com.cn/n1/2019/1017/c40606-31404334.html>
- <https://xinwen.bjd.com.cn/content/s5da7a6cce4b037702ff14b36.html>

Grade: **B/C hybrid**.

Reason: 今天可定位的是 2019 年机构性历史整理，内部明确标出 1996/1997 原报纸版期并展示版面；本轮未将新闻图片下载为“原始历史网页 artifact”，也未把 2019 文本自动升级成 A。

Claims supported:

- public Internet terminals existed in Beijing by 1996–1997;
- at least one contemporaneously observed venue served multiple web/communication tasks;
- access could be explicitly time-priced.

Claims NOT supported:

- exact client OS/browser/plugin stack;
- default homepage;
- session cleanup policy;
- citywide user share;
- national representativeness.

### E2 — 飞宇 1998：价格改变实际 repeat use

新华社 2001 年报道回溯飞宇开业：25 台电脑，前三天免费时排队坐满；随后 20 元/小时，有时一天仅七八名顾客。

Source:

- <https://tech.sina.com.cn/i/c/2001-08-31/82744.shtml>

Grade: **B**（近同时代媒体 + 当事人叙述）。

Useful claim:

> service availability and technical capacity did not guarantee economically sustainable repeat access.

Archive relevance:

一个网页 capture 不能证明“普通用户当时实际上负担得起在该终端打开它”。

### E3 — 沈阳 2003：身份卡进入 session gate

同期报道描述统一安装实名制网吧管理系统；用户以身份证办上网卡，扫描确认后才能打开网页。

Source:

- <https://news.sina.com.cn/c/2003-07-10/08441313128.html>

Grade: **B**.

Useful claim:

```text
physical terminal present
```

之后又新增：

```text
identity/document/card/backend state
```

这一执行层不会被 target website 的 archive 保存。

### E4 — 合肥 2006：实名管理与临时 session 的具体流程

同期央广网报道：市区 95% 以上网吧已安装实名登记系统；有效证件可办实名卡；临时上网也需由管理人员登记，临时卡打开具体机器/session。

Source:

- <https://news.sina.cn/sa/2006-11-14/detail-ikknscsk1272371.d.html>

Grade: **B**.

This supports a state distinction between:

```text
person identity
registration-card identity
temporary session token
terminal session
```

这些对象不能简化成一个“实名账号”。

### E5 — 2006 enforcement counterexample

新华社记者在天津、南京、兰州部分网吧暗访时发现，多家并不实际要求实名卡；南京同期报道也称不少场所弃用系统。

Sources:

- <https://news.sina.com.cn/o/2006-05-24/14509014461s.shtml>
- <https://news.sohu.com/20061111/n246321432.shtml>

Grade: **B**.

Hard rule:

```text
policy exists != software installed != local enforcement != every observed session compliant
```

因此 archive 看到一份“实名制说明页”不能重构某位用户当晚实际上怎样进机。

### E6 — CNNIC 2008：public access was still behaviorally large while home access was already dominant

CNNIC 第 22 次统计报告（2008 年中）记录：

- home access: 74.1%;
- Internet-café access: 39.2%;
- café users: about 99.18 million;
- 24 and under: 70.7% of café users.

Source:

- <https://www3.cnnic.cn/NMediaFile/2022/0830/MAIN1661848787213RHRPZ27GU2.pdf>

Grade: **A**（当期机构调查报告；今天由 CNNIC 官方站保存）。

注意：“上网地点”是可并存的行为类别，不可将 74.1% 与 39.2% 当作互斥人口。

CNNIC 青少年调查还记录 2008 年青少年网民中 57.5% 过去半年曾在网吧上网，农村青少年网民为 65.4%。

Source:

- <https://www.cnnic.cn/n4/2022/0401/c116-890.html>

Grade: **A**.

This supports:

> public-terminal access remained a major execution environment even after home access became widespread.

It does NOT support:

> every young user depended on cafés as their primary access location.

---

## 5. Why a server-side WARC is insufficient

### 5.1 Client-image gap

历史网页可能依赖：

- IE-specific rendering;
- ActiveX;
- Java;
- Flash;
- Chinese fonts/input methods;
- download managers;
- media codecs;
- browser sniffing;
- local certificates;
- particular screen resolution.

但公共 PC 不是某位用户长期维护的个人电脑。经营者可能批量：

- reinstall;
- ghost/restore;
- patch;
- lock desktop;
- change homepage;
- deploy game clients;
- add/remove browser plugins.

因此同一家网吧 2002-03 与 2002-11 可能已经不是同一个 execution environment。

本轮**没有获得任何可核验的 1997–2008 中国网吧原始 client disk image / Ghost image / VM image**。

所以禁止写：

> “某 2001 网吧用户使用 IE6 打开该页”

除非有具体机房/机器/时点证据。

### 5.2 Billing-state gap

一次 session 是否开始，可能依赖：

- 人工纸条；
- 前台计时；
- 会员账户；
- 卡号；
- 临时卡；
- 计费软件；
- 预充值余额。

远端网页 archive 完全不知道：

- 是否还有余额；
- 用户已经用了多久；
- 是否即将被强制下机；
- 是否续费；
- 是否包夜。

于是早期网页中的“用户停留时间”不能从页面本身复原。

### 5.3 Seat-availability gap

CNNIC 可以证明大量人使用网吧，但不能告诉我们一个具体周五晚 20:00：

- 这家店有没有空机；
- 是否要排队；
- 是否只有某种低配置机位；
- 是否因维修关闭部分机器。

因此：

```text
venue capacity != instantaneous available capacity
```

### 5.4 Network-route gap

公共 terminal 的真实可达性还依赖：

- ISP upstream;
- DNS;
- local router/proxy;
- filtering;
- congestion;
- international bandwidth;
- transient outage.

Wayback capture 能证明服务器/档案在某时刻保存某资源，不能证明某家中国网吧同日能稳定取得它。

### 5.5 Account-entitlement gap

QQ、email、BBS、game、portal 登录都可能继续把用户引出公开 Web。

```text
login page survived != historical credentials survived
credentials existed != user remembered them
account existed != account was not locked
```

研究者不应为了补 execution chain 去搜集/复用旧账号密码。

---

## 6. Public terminal as a privacy-sensitive archaeological environment

共享机器最危险的“历史残留”恰恰可能是最不应该保存的部分：

- browser history;
- cookies;
- saved usernames/passwords;
- chat logs;
- email caches;
- downloaded personal documents;
- identity-card numbers;
- session records;
- payment/member records.

这些可能在旧硬盘、二手机器、磁盘镜像或泄露数据库中残存。

本仓固定原则：

> **credential/session residue is not a recovery target.**

即使 artifact 技术上可读，也应优先抽象其存在形式，而不是重新公开普通用户内容。

因此这里存在一个 **desirable archive gap**：

> 某些 session 没有被永久保存，是正确的隐私结果，而不是需要修补的历史失败。

---

## 7. Public-Web / private-client asymmetry

网吧留下的公共网页很可能是：

- 品牌介绍；
- 加盟广告；
- 营业地址；
- 促销价；
- 游戏活动；
- 政策/实名登记说明；
- 新闻报道。

但真实使用发生在：

- local client;
- IM/game native application;
- private account;
- member database;
- billing software;
- LAN;
- off-web phone/SMS arrangements.

这是一种典型的 **public-shell / private-execution asymmetry**。

可以类比本仓已有：

- online banking form vs settlement state;
- recruitment listing vs recruiter backend;
- dating profile vs relationship outcome;
- hospital appointment page vs actual slot state。

网吧场景的独特之处是：**连“浏览网页的那台电脑”本身也属于不可见执行层。**

---

## 8. Archive gaps to record explicitly

### G1 — venue-topology gap

不知道当日：

- 多少台机器；
- 机器如何分区；
- 是否有吸烟/无烟区；
- 是否有包间；
- 哪些终端停机。

### G2 — machine-inventory gap

广告说“100 台电脑”不等于当日 100 台可用。

### G3 — client-image gap

缺 OS/browser/plugins/fonts/codec/IME/patch level 的可验证镜像。

### G4 — billing-state gap

缺 user session start/end/balance/续时状态。

### G5 — identity-gate gap

知道实名系统存在，不知道某 session 是否真正执行、卡/证件是否被接受。

### G6 — enforcement gap

法规与现实执行之间可能不一致。

### G7 — startup-state gap

缺默认首页、桌面快捷方式、开机 launcher、锁屏工具。

### G8 — network-route gap

缺该 venue / hour 的 ISP、DNS、proxy、packet path、bandwidth/congestion 状态。

### G9 — local-software ecosystem gap

旧网用户可能主要通过 QQ、游戏客户端、FTP、下载器等 native software 行动；Web archive 不保存完整客户端行为。

### G10 — session-cleanup gap

不知道下机后：

- 自动还原；
- 仅清浏览器；
- 什么都不清；
- 重启后恢复；
- 定期 Ghost 重装。

### G11 — price-time gap

可能存在：

- 标准小时价；
- 学生价；
- 会员价；
- 夜间价；
- 包夜；
- 促销免费时段。

一个静态广告页不能自动恢复每个时点的 executable price。

### G12 — closure/venue-death gap

品牌新闻和旧网页可以继续存在，而具体门店已经搬迁、停业、换老板或重新装机。

---

## 9. Browser reconstruction rules for Internet-café cases

如果未来找到一个具体 2000–2006 网吧 client artifact，必须单独记录：

```yaml
venue:
observed_date:
client_machine_scope: single-machine | image-family | venue-wide-claim
os:
browser:
browser_version:
encoding_support:
fonts:
plugins:
ime:
launcher_or_shell:
restore_software:
network_proxy:
startup_homepage:
evidence_grade:
provenance:
```

### 禁止推断

不得仅根据“那个年代常见”写：

- “肯定 IE6”；
- “肯定 Windows 98”；
- “默认打开 3721/hao123”；
- “一定安装 QQ”；
- “一定用还原卡”；
- “一定支持 Flash”。

这些都必须落到具体 venue + date + evidence。

---

## 10. A useful negative result from this run

本轮进行了公开 Web 与仓库内检索，获得：

- 1996–1998 公共上网场所的近同时代媒体证据；
- 2003–2006 实名 session gate 的同期媒体证据；
- 2008 CNNIC 公共上网地点的 A 级调查证据；
- 2006 “制度存在但执行不一致”的同期反证。

但**没有可靠获得**：

1. 1997–2008 中国具体网吧的一份原始 client disk/Ghost image；
2. 对应机器的可验证浏览器、插件、字体、输入法完整清单；
3. 某一用户 session 的合法、非敏感完整状态链；
4. 某网吧计费系统原始数据库（且普通用户 session DB 本身也不应成为公开复原目标）；
5. 足以证明“某远端旧站在某具体网吧、某天、某机位成功渲染”的 packet/screenshot + provenance 组合。

因此本轮**不做历史 client reconstruction**。

“服务器端页面可保存，但公共终端执行环境无法可靠复原”本身就是正式结论。

---

## 11. Cross-era interpretation, kept outside repo scope

全球 cybercafe / Minitel / public terminal 比较不应把本仓扩成全球旧网史。

仅记录与中文旧网解释直接有关的边界：

- 1994 London Cyberia contemporaneous reporting shows public Internet terminals, NCSA Mosaic and staff assistance existed outside China before Chinese mass access;
- therefore “public access before household ownership” is not uniquely Chinese;
- Chinese-specific archaeology should remain focused on local venue/client/identity/software conditions and Chinese Web/platform usage.

海外生活史与跨国比较写入 `how-people-lived` counterpart，而不扩张本仓主体范围。

---

## 12. Claims table

| Claim | Grade | Confidence | Boundary |
|---|---|---:|---|
| Beijing had an observed public network-café environment by 1996–1997 | B/C | high | later newspaper archive reproduces/locates original issues |
| high hourly price could suppress repeat café use in 1998 Feiyu case | B | medium-high | near-contemporary retrospective within media report |
| some 2003 public-access sessions were designed to require ID-card-based gate | B | high | implementation claim, not proof of every session |
| 2006 systems could distinguish registered card / temporary card / terminal session | B | high | city-specific |
| real-name policy/system presence did not imply consistent enforcement | B | high | multiple-city contemporary reporting |
| café use remained large in 2008 while home use was already widespread | A | high | CNNIC survey; categories can overlap |
| rural youth café use was higher than average in CNNIC 2008 youth sample | A | high | survey definition/timeframe must be retained |
| exact 1997–2008 Chinese café client image is reconstructed here | — | **false / not attempted** | evidence absent |
| archived target website proves café user could render it | — | **unsupported** | requires client + route evidence |

---

## 13. Hindsight risks

1. 不把 1994 full Internet connection 当成 household mass access；
2. 不把“网吧存在”写成“所有青年都去网吧”；
3. 不把今天怀旧中的典型 CRT/QQ/游戏画面自动套给所有年份；
4. 不用今天的 Chromium 回放代替历史公共 PC 体验；
5. 不因为实名系统报道存在，就假定每家门店严格执行；
6. 不因为某用户在网吧登录过账号，就搜集其旧 cookie/chat/password 以“补历史”；
7. 不把 venue website 当作 venue client image；
8. 不把行业规模或机位数当成瞬时 seat availability。

---

## 14. Next high-value evidence

最高价值下一步不是继续找“网吧数量”，而是寻找一个**合法可研究的公共 client environment**：

- 历史网吧安装光盘；
- 公开发布的计费软件 manual / demo；
- 可验证来源的无个人数据 Ghost image；
- 同期网管技术文章，能定位 OS/browser/restore/proxy；
- 历史截图，能同时定位 venue/date/client shell；
- 两个以上时点，观察 client image 如何更新。

如果能获得这样的 artifact，才值得进入 M3 browser-environment experiment：

```text
same historical page
× historical café client assumption
× IE5/IE6-class VM
× modern Chromium replay
```

并明确列出至少五个解释差异。

在此之前，正确的考古结论仍是：

> **中文旧网的公共访问史不能只从服务器端 archive 重建。那一小时真正发生在一台临时租来的机器上，而那台机器的状态通常比网页本身消失得更彻底。**
