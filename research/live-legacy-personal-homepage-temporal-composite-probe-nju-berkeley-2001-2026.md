# Live-legacy 个人主页的时间复合：南京大学 / Berkeley 实物核验（2001—2026）

> 性质：artifact evidence upgrade。  
> 本文件**不新增**一个新的 `STATE_GAPS` 理论专题；它用当前仍在线的页面，验证本仓既有 `last-updated label / actual edit-time gap`，并给后续 M1/M2 取证规定更严格的时间字段。
>
> 主研究对象仍是中文旧网。Berkeley 仅作为海外对照，不扩展仓库 scope。

## 1. 去重与研究问题

本仓已有：

- `docs/PERSONAL_HOMEPAGE_PUBLIC_SELF_METRICS_AND_PLATFORM_MORTALITY_1996_2015.md`
- `research/artifact-probe-carboy-163-net-personal-homepage-1996-2000.md`

前者已经明确提出：

```text
visible "Last updated"
!= actual edit time of the whole representation
```

所以本轮不再发明“旧主页时间戳失真”这一概念。问题改成：

> 能否找到一个仍在线、可直接核验的中文个人主页，使页面内部出现**晚于页脚 Last updated 很多年的内容**，从而把方法警告从推论提升为可复核 artifact evidence？

答案是：可以。

---

## 2. 中国对象：南京大学李宣东个人主页

### 2.1 当前可访问 artifact

URL：

- https://cs.nju.edu.cn/lixuandong/

本轮直接打开当前页面，可以观察到：

- 页面仍是南京大学个人学术主页；
- `Teaching` 中出现 `Formal Languages and Automata, Fall 2019`；
- `Research Projects` 中出现 2016—2019、2017—2021 等项目时间；
- 但页面底部同时显示：`Last updated: Nov. 10, 2001`。

因此，至少对**当前这一 representation**，下面这个命题已经被页面内部证据直接否定：

```text
footer Last updated = 整个页面最后一次内容修改时间
```

更准确地说：

```text
page observed in 2026
contains internal dates reaching 2021
while footer exposes 2001
```

这是一份非常干净的 **temporal composite / 时间复合页面**。

### 2.2 证据等级

本轮可确认：

```text
current live URL                         = ACHIEVED
current body/footer contradiction       = ACHIEVED
Chinese institutional hosting context   = ACHIEVED
historical 2001 capture opened          = NOT ACHIEVED
historical 2019/2021 capture opened     = NOT ACHIEVED
same-page change-over-time              = NOT ACHIEVED
M1 complete historical case             = NOT ACHIEVED
```

所以它是**当前 live-legacy artifact**，不是 2001 年 Wayback capture，更不能把今天打开的页面当成“2001 年网页原样存活”。

---

## 3. 海外对照：UC Berkeley John R. Steel 个人主页

URL：

- https://math.berkeley.edu/~steel/

当前搜索/页面表示中可同时观察到：

- 页面仍保留个人学术主页式结构；
- 正文含 `Spring Semester 2020` 的 office-hours 信息；
- 页脚却显示 `Last modified: Mon Jan 5 10:58:16 PDT 2001`。

这与南京大学对象形成独立对照：

```text
late internal content
+
very old visible footer timestamp
```

因此这种现象不应解释成“中国某个站点的特例”。更保守的跨国判断是：

> 在长期存在的机构主页空间中，旧模板、手工页脚、局部 include、局部更新或其他维护方式，可以让一个页面同时暴露多个时间层。

但这仍不是“所有大学个人主页都这样”的普遍率结论。

---

## 4. 对 old-web archaeology 的直接方法后果

### 4.1 `Last updated` 只能是字段，不能是 capture date

以后个人主页 / 静态 HTML case 至少应分开记录：

```text
observed_at
archive_capture_datetime
HTTP Last-Modified (if any)
visible_footer_date
latest_internal_date
oldest_internal_date
file/path continuity evidence
host continuity evidence
```

禁止把：

```text
Last updated: 2001
```

直接写成：

```text
this is a 2001 page
```

### 4.2 live legacy page 不是 frozen historical page

一个 URL 从旧网时代延续到今天时，至少存在四种可能：

1. 文件从未变过；
2. 正文持续改动，但页脚日期没改；
3. 页框/模板很旧，局部内容由 include / script / CMS 更新；
4. namespace 延续，但底层文件经历迁移或替换。

只有第 1 种才接近“冻结页面”。单凭视觉古旧、旧 footer 或老 URL pattern，无法区分四者。

因此：

```text
URL continuity
!= byte continuity
!= representation continuity
!= historical capture
```

### 4.3 对 M1 / M2 的影响

如果把 live-legacy page 纳入案例，只能作为：

- historical locator lead；
- namespace / institutional-host survival evidence；
- current artifact；
- later endpoint for change-over-time。

它不能替代：

- 至少一个真正历史 capture；
- capture timestamp；
- historical HTTP / replay；
- DOM / charset / subresource 状态；
- 第二历史时点。

---

## 5. 反例与替代解释

本轮证据只证明两个具体页面存在明显时间复合，不证明所有旧主页都存在错误 footer。

可能的替代解释包括：

- footer 是作者忘记手改的纯文本；
- 部分正文来自 server-side include；
- 不同区块由不同维护流程更新；
- 站点迁移时保留了旧模板；
- 搜索引擎当前摘要与页面最终 HTML 之间有缓存差异。

因此，后续若要做 M1/M2，仍应保存原始 HTML、响应头、DOM、资源请求，而不是只截图。

---

## 6. 它改变了什么，又没有改变什么

### 改变

它把本仓已有的 `last-updated label / actual edit-time gap` 从纯方法警告升级成**可复核的中外 artifact 对照**。

它也进一步说明：

> live-legacy 页面保存的是一个仍在继续生长或被局部维护的对象；历史研究者面对的是时间层叠，不是自动获得了一张过去的快照。

### 没有改变

它没有新增：

- 新生活路径类别；
- 新制度接口；
- 新 Internet 转折机制；
- 新的 archive gap 概念。

因此它不应被用来继续扩张 `STATE_GAPS` 文件数量。

---

## 7. 下一步 artifact-first 任务

优先级：

1. 为 `https://cs.nju.edu.cn/lixuandong/` 获取真正历史 capture；
2. 若能打开，记录 capture datetime、HTTP/replay、DOM、charset、assets；
3. 再取第二历史时点，对比正文与 footer 是否同步变化；
4. 若历史 capture 不可达，继续寻找同 namespace 的旧课程页、目录页、外链引用或镜像；
5. 对 Carboy / 西祠等已有精确 locator 继续做 artifact escalation，而不是重新发明主页/论坛机制。

---

## 8. 来源

### 中国 artifact

- 南京大学李宣东个人主页：
  https://cs.nju.edu.cn/lixuandong/

### 海外对照

- UC Berkeley, John R. Steel personal homepage：
  https://math.berkeley.edu/~steel/

### 仓内方法基础

- `docs/PERSONAL_HOMEPAGE_PUBLIC_SELF_METRICS_AND_PLATFORM_MORTALITY_1996_2015.md`
- `research/artifact-probe-carboy-163-net-personal-homepage-1996-2000.md`
- `docs/METHOD.md`
- `docs/RESEARCH_SATURATION_DEDUP_AND_ARTIFACT_PRIORITY_AUDIT_2026-09-12.md`
