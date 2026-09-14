# 西祠 2007 页面：Wayback capture 打开后的质量检查（2026-09-14）

> 性质：artifact verification note；不是新的 state-gap 理论，也不是 M1 complete case。  
> 关联：`research/xici-2007-discussion-page-wayback-locator-escalation-2026-09-14.md`。

## 1. 为什么再次检查同一个对象

前两轮已经把对象收窄到一个精确历史页面与精确 Wayback locator：

- 原始 URL：`http://www.xici.net/b373044/d50430566.htm`
- 后出参考链给出的题名：`公布亚洲展望２００７城市联赛参赛队员名单`
- 后出参考链给出的原始日期：`2007-03-28`
- candidate memento：`https://web.archive.org/web/20110724135817/http://www.xici.net/b373044/d50430566.htm`

此前状态一直是 `locator known / replay not opened`。本轮不换题，直接再次核验这个 capture。

## 2. 本轮实际打开了 Wayback memento shell

本轮通过后出参考页中的 archive 链接进入 Wayback，成功取得该 memento 的回放外壳。Wayback 当前显示：

- 此 URL 有 `6 captures`；
- 可见时间范围为 `2011-07-16` 至 `2021-05-03`；
- 当前定位到的时间戳为 `2011-07-24 13:58:17`。

来源：

- 后出 locator 链：<https://3rabica.org/%D8%AA%D8%A7%D9%86_%D9%86%D9%8A%D9%86%D8%BA>
- memento：<https://web.archive.org/web/20110724135817/http://www.xici.net/b373044/d50430566.htm>

这使证据状态从“只有二手 locator”推进到：**该 memento 确实可被 Wayback 当前回放系统打开并识别为一个 capture。**

## 3. 但 target post body 仍没有恢复

继续打开 Wayback 的 inner iframe 后，返回的是一个极短的中文文本 representation；当前回放/解析链把其字符错误显示成 mojibake，且没有出现预期的帖子题名、正文、board chrome、回复结构或帖子元数据。

因此本轮**不能**把它写成“2007 西祠帖子已恢复”。更准确的状态是：

```yaml
object: xici discussion page
original_url: http://www.xici.net/b373044/d50430566.htm
memento_timestamp: 2011-07-24T13:58:17Z
wayback_shell_opened: true
capture_count_visible_in_wayback_ui: 6
capture_range_visible_in_wayback_ui:
  first: 2011-07-16
  last: 2021-05-03
inner_replay_opened: true
expected_post_body_recovered: false
inner_representation:
  type: short_text_or_error_like_html
  exact_chinese_wording_decoded: false
  mojibake_present: true
historical_content_type: unknown
historical_charset: unknown
board_chrome_recovered: false
reply_structure_recovered: false
subresources_checked: false
second_historical_timepoint_opened: false
m1_status: NOT ACHIEVED
```

注意：这里使用 `error_like` 只描述**当前可见 representation 与目标帖子内容不符**，不推断它在历史服务器侧究竟是维护页、应用错误页、限流页还是其他短状态页。由于 charset / 原始字节未取得，不能凭 mojibake 猜原文。

## 4. 这条结果改变了什么

它改变的是 artifact 状态，不改变 ordinary-life 结论：

1. `exact locator` 不再只是后出参考链里的字符串；该 Wayback memento 当前确实能打开。
2. “capture 存在”仍然**不等于**“目标历史内容被保存”。
3. 这个案例具体演示了 `docs/METHOD.md` 已经要求检查的事项：一个 archive locator 必须继续判断是否是目标页面、错误页、登录页、重定向或其他非目标 representation。
4. 当前 capture 无法提供 2007 年西祠 DOM、charset、论坛壳、作者/时间/回复结构，也没有形成第二历史时点，所以仍不满足 M1。

因此这是一条有价值的 A 级 **capture-quality evidence**，但不是一个会改变 HPL 生活史解释的新机制或新生活路径。

## 5. 并行 derivative-artifact 检查：Carboy

本轮继续检查 `完全上网手册 / Carboy` 是否存在公开可访问的整站镜像、离线包或公开 derivative corpus。检索仍能稳定找到 2000 年刘韧的近同时代报道与杨震霆相关材料，其中明确记录：1997 年王峻涛曾把“完全上网手册”整站下载到本机学习；也能确认历史路径 `business.gznet.com/carboy/` 以及后来被删除、只剩零星内容的叙述。

目前没有取得一个可验证为 1997 年用户侧副本的公开镜像/磁盘包，因此状态仍是：

```text
historical local-copy behavior: evidenced by near-contemporaneous report
publicly recoverable 1997 derivative artifact: not obtained
private-copy existence today: unknown and not pursued
```

不能因为“当年有人下载过”推断那份副本今天仍然存在。

## 6. 海外 preservation 对照

本轮再次核查 GeoCities 的 2009 抢救作为海外对照，而不扩张本仓 scope。Archive Team 记录，GeoCities 宣布关闭后，协调抓取从 2009 年 4 月持续到 10 月关闭前；Internet Archive 同期进行了 deep crawl，不同抢救项目保留的子集并不完全相同。

来源：

- <https://wiki.archiveteam.org/index.php/GeoCities_Project>
- <https://wiki.archiveteam.org/index.php/Geocities>
- <https://internetarchive.wordpress.com/2009/08/25/geocities-preserved/>

这个对照仍然只强化既有结论：今天旧网的可见性高度依赖关闭前的抢救生态、用户副本与档案策略；它没有产生新的中国生活路径或新的互联网转折机制。

## 7. 跨仓饱和判断

与前两轮相比，本轮确实把西祠从 `opened_capture=false` 推进到 `wayback_shell_opened=true / inner_replay_opened=true`，但取得的是**非目标/不可可靠解码的 representation**，没有恢复帖子本体，也没有得到第二历史时点。

同时：

- 没有发现新的生活路径类别；
- 没有发现新的制度接口；
- 没有发现新的时代时间感机制；
- 没有发现新的通信 / Internet 转折机制；
- Carboy 仍是既有 preservation mechanism 的具体 lead；
- GeoCities 仍是已有 rescue-ecology 判断的海外确认；
- 本轮 artifact 进展不足以实质改写 HPL 的现有生活史结论。

因此按跨仓既定规则，本轮是连续第三次 `no-new-mechanism / no-conclusion-changing-evidence` 运行，应进入阶段性 closure，而不是继续扩张 state-gap 专题。

## 8. 若未来重启这个对象

只在出现以下任一触发时继续：

1. 能取得该 capture 的原始字节、WARC/CDX metadata 或可靠 charset，从而判断 short representation 的真实内容；
2. 能打开 6 个 captures 中另一个历史时点，并恢复目标帖子或论坛壳；
3. 找到同一 board/site 的独立历史 artifact（HTML、截图、客户端缓存、公开镜像等）；
4. 得到能改变西祠页面结构、访问权、保存偏差或普通用户实践解释的一手证据。

否则不再仅凭更多 locator、后来回忆或同义 state-gap 文件继续扩张。