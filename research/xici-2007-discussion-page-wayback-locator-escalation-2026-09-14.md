# 西祠胡同 2007 讨论页：Wayback locator 升级记录（2026-09-14）

> 状态：artifact-locator escalation；**不是** M1 complete case。  
> 关联既有专题：`research/xici-hutong-domain-bbs-lineage-1998-2015.md`。  
> 本文件不新增一套“论坛状态缺口”理论，而是把已有西祠对象向可核验历史 artifact 推进一步。

## 1. 本轮为何做这件事

仓库当前的主要瓶颈已经不是缺少更多平台主题，而是 M1 所需的历史 artifact 深度不足。既有西祠研究已经有 2000–2015 年间的企业/域名/业务沿革、同期媒体对讨论版结构和线下版聚的描述，也已经严格区分“域名资产”“平台身份”和“实际历史页面”。缺的仍是：**真正打开并检查过的历史 BBS 页面 capture**，以及同一对象至少第二个历史时点。

因此本轮不再开新概念专题，而是继续追具体 historical page。

## 2. 新恢复的精确 locator

从后出的参考文献链中恢复到一条精确的西祠讨论页及 Wayback 时间戳：

- 页面题名：`公布亚洲展望２００７城市联赛参赛队员名单`
- 原始 URL：`http://www.xici.net/b373044/d50430566.htm`
- 参考文献所列原始日期：`2007-03-28`
- 精确 archive candidate：`https://web.archive.org/web/20110724135817/http://www.xici.net/b373044/d50430566.htm`
- 参考文献所列 archived date：`2011-07-24`
- 参考文献所列 retrieved date：`2012-08-24`

本轮检索到的直接线索：

- 3rabica 的相关人物条目在参考文献中完整保留了原页面题名、`xici.net`、2007-03-28 日期、上述精确 Wayback URL、2011-07-24 archived date 与 2012-08-24 retrieved date：  
  <https://3rabica.org/%D8%AA%D8%A7%D9%86_%D9%86%D9%8A%D9%86%D8%BA>

这使 locator 从“知道西祠在那个年代存在、知道域名”推进到“知道某一具体帖子和某一个具体 Wayback capture timestamp”。

## 3. 证据等级：只能先算 C 级 locator lead

必须强调：这条证据目前仍然来自**后出的二次参考链**。虽然它给出了完整 Wayback URL，但本轮运行环境未能实际打开该 memento 并检查 replay。

因此当前不能把它升级成 A 级 historical capture evidence，也不能写：

- “已经恢复 2007 年西祠页面”；
- “Wayback 页面显示……”；
- “当时页面 charset 是……”；
- “历史页面的版面/导航/头像/回复结构是……”；
- “子资源完整/缺失”。

当前最准确的记录是：

```yaml
object: xici discussion page
original_url: http://www.xici.net/b373044/d50430566.htm
claimed_original_date: 2007-03-28
capture_candidate: https://web.archive.org/web/20110724135817/http://www.xici.net/b373044/d50430566.htm
capture_timestamp_from_secondary_reference: 2011-07-24T13:58:17Z
opened_capture: false
secondary_reference_retrieval_date: 2012-08-24
status:
  - exact archived URL recovered
  - replay not opened in current runtime
unknowns:
  - replay/historical HTTP status
  - DOM structure
  - charset and encoding behavior
  - board chrome / breadcrumb / navigation
  - author/time/reply metadata actually present in replay
  - image/CSS/JS subresources
  - Wayback replay rewrites
```

## 4. 本轮失败分类

直接访问该 Wayback URL 在当前运行环境中没有成功完成历史 replay 检查；因此这里记为：

**`exact memento locator recovered; replay transport unavailable/unverified in this run`**。

这不是：

- `capture absent`
- `Wayback did not save it`
- `historical page lost`

只有在能实际查询 archive index / replay 并核验后，才有资格判断这些状态。

## 5. 对 M1 的价值

这条 locator 很适合成为 M1 BBS/community 案例的下一跳，因为它满足几个条件：

1. 对象明确：西祠胡同 discussion page；
2. 原始 URL 明确，且不是只有顶级域名；
3. 有具体 post ID / board ID 风格路径：`b373044/d50430566.htm`；
4. 有精确 archive timestamp；
5. 原始内容题名和日期在独立参考链中仍可交叉定位。

但它距离 M1 complete case 仍至少缺：

- 实际打开并记录该 capture；
- 记录 historical/replay HTTP、DOM、charset、missing resources；
- 判断页面壳、帖子正文、回复/导航是否来自同一历史时间；
- 找到西祠同一 board/site 的第二历史时点；
- 最好再找到一个不同证据家族（例如同期截图、缓存、客户端/HTML 保存、机构馆藏）；
- 做至少一次对应历史浏览器/编码假设的 reproduction。

## 6. 海外方法对照：The WELL，不扩张 OWA scope

本轮只把 The WELL 当作方法对照，不把 OWA 改成全球旧网仓库。

1997 年 WIRED 对 The WELL 的同期/近同期长篇报道记录：

- The WELL 1985 年上线时使用 VAX、六个 modem 和六条电话线；
- PicoSpan 把讨论组织成 conferences / topics；
- 1986 年起线下 WELL parties 变成重要社群机制，线上矛盾也会在线下解决；
- 从外地接入在技术上可行，但一名 Austin 用户说，在自己专程去 Bay Area 参加线下 party 之前，发言经常感觉被忽略。

来源：<https://www.wired.com/1997/05/ff-well/>

The WELL 自己 1998 年的公告又说明 Vue conferences 可以由任何 Web 用户阅读，但只有 WELL members 能发帖；即“公开可读投影”和“有权参与的账号状态”并不是一回事。

来源：<https://www.well.com/about-2/pr/well-launches-vue-conferences/>

这个对照只强化已有方法原则：

- BBS/community 的历史对象不只是一张页面；
- public readable projection ≠ posting entitlement；
- 在线关系与线下聚会可以共同构成真实社群；
- 一个 capture 也无法自动恢复会员资格、访问权和线下关系。

这些不是本轮的新机制，不能为了“海外比较”重新命名成新专题。

## 7. 下一步优先级

下一轮若仍能访问同一研究环境，优先顺序应是：

1. 重试精确 memento：  
   `https://web.archive.org/web/20110724135817/http://www.xici.net/b373044/d50430566.htm`
2. 一旦能打开，按 `docs/METHOD.md` 完整记录 capture contract；
3. 从该页面的 board ID、breadcrumb、上一页/下一页或同题名引用反查第二时点；
4. 再考虑把该对象提升为 M1 BBS/community complete case。

在上述步骤完成前，不继续为西祠扩写新的 state-gap 理论文件。

## 8. 饱和判断

本轮取得的是**artifact locator 进展**，不是新的普通生活路径、制度接口、时代时间感、通信转折机制或能实质改变 HPL 结论的一手材料。海外 The WELL 对照也主要确认仓库已有的“线上/线下混合社群”理解。

因此在跨仓研究的饱和计数中，本轮应记为一次 **no-new-mechanism run**；上一轮地图/导航研究确有新的 `route executability`，已把计数重置，所以当前为 **1/3**。
