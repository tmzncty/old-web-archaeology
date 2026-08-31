# CITATION.md — 历史网页与档案引用规范

本规范解决一个最常见的问题：**原始 URL、档案 URL、档案时间、页面自身日期与研究访问日期不是同一件事。**

RFC 7089（Memento）把 Original Resource 与其历史 Memento 明确区分，本仓沿用这种区分：

<https://www.rfc-editor.org/rfc/rfc7089.html>

## 1. 最低字段

每条历史网页证据尽量记录：

```yaml
source_id: example-A-001
title: "页面标题"
creator: "机构/作者；不知道则 null"
original_url: "http://example.com/path"
archive_source: "internet-archive"
capture_url: "https://web.archive.org/web/.../http://example.com/path"
capture_datetime: "2006-07-13T07:20:19Z"
page_date: "2006-07-13"       # 页面自己明确标出的日期；没有则 null
accessed_at: "2026-08-31"
evidence_grade: "A"
evidence_type: "archived-page"
verification: "direct"       # direct / locator-only / secondary-quote
notes: "..."
```

## 2. 日期优先级

必须分别保存：

1. `capture_datetime`：archive 表示该 Memento 被保存/归档的时间；
2. `page_date`：页面正文自己标注的发布/更新时间；
3. `event_date`：研究对象实际事件发生日期（若可由证据确定）；
4. `accessed_at`：研究者本次访问证据的日期。

不得把 Wayback URL 中的 timestamp 自动当成文章发布日期。

## 3. 引用格式

### 已直接验证的 archive capture

推荐 Markdown：

```text
机构/作者，《标题》，页面日期（若有）。
Original: <原始 URL>
Archived at Internet Archive, capture YYYY-MM-DD HH:MM:SSZ: <capture URL>
Accessed YYYY-MM-DD. Evidence: A, verification=direct.
```

### 仍在线的同时代官方页面

```text
机构，《标题》，YYYY-MM-DD，<URL>，accessed YYYY-MM-DD。
Evidence: A (contemporaneous primary source).
```

页面今天仍在线，不意味着它今天的 HTML 与当时完全相同。若服务器未提供版本历史，只能把它作为“当前可访问的历史发布材料”，不能据此讨论当年的 CSS/DOM。

### 同期新闻 / 教程

```text
作者/媒体，《标题》，YYYY-MM-DD，<URL>，accessed YYYY-MM-DD。
Evidence: B.
```

若明确为转载，尽量同时记录原稿来源；两个转载 URL 不计作两个独立 evidence family。

### 候选 archive locator

没有直接打开验证时写：

```text
Candidate capture locator only; not counted as verified archived-page evidence.
```

此类 locator 不进入 A 级页面内容结论。

## 4. Original URL 规范化

保留**证据中实际出现的 URL**，不要只保存现代规范化版本。

必要时并列：

- `original_url_observed`：史料实际写法；
- `original_url_normalized`：为比较而规范化的写法。

以下差异在旧网研究中都可能有意义，不能静默抹掉：

- `http` / `https`；
- `www` / 非 `www`；
- 大小写；
- 尾随 `/`；
- percent-encoding；
- 中文路径；
- query string；
- frame 内真实内容 URL；
- 二级域名与用户 path。

## 5. Archive rewrite

Wayback/pywb 等回放系统可能改写：

- HTML 中链接；
- JS/CSS 请求；
- timestamp；
- CSP/header；
- iframe/frame URL。

因此：

- `capture_url` 是档案系统入口；
- 页面内被 rewrite 的 URL 不应自动当成历史原始 URL；
- 能取得 WARC/header 时优先用原始响应 metadata 核对。

## 6. 截图引用

截图只能直接证明截图像素中可见的内容。

必须记录：

- 截图来源；
- 截图日期/估计日期；
- 是否来自 archive replay；
- 浏览器/OS/viewport（知道时）；
- 是否裁剪、缩放、压缩；
- 原页面 URL（知道时）。

截图不能单独证明隐藏 DOM、脚本、请求链、charset 或交互行为。

## 7. 同一 claim 的多证据引用

建议 claim 使用稳定 ID：

```yaml
claim_id: baidu-space-launch-20060713
statement: "百度官方于 2006-07-13 宣布百度空间正式发布。"
supports:
  - BS-A-001
  - BS-B-001
status: verified
```

若多个来源来自同一稿件，增加：

```yaml
evidence_family: baidu-2015-shutdown-announcement
```

避免把转载数量误当作独立核验强度。

## 8. 不可访问 / 失效引用

历史研究不删除失效引用。应改为：

- 保留 original/capture locator；
- 标 `verification=locator-only` 或 `unavailable-on-YYYY-MM-DD`；
- 记录最后一次成功验证（若有）；
- 寻找另一 archive source；
- 降低依赖该证据的 claim confidence。

## 9. 个人内容

普通个人主页/论坛内容只在研究必要范围内引用：

- 优先引用平台级帮助页、新闻、公开技术教程；
- 只为证明 URL pattern 时应抽象账号名；
- 不把 archive 中已删除的联系方式、照片、私人日记复制进仓库；
- citation 能完成证明时，不提交原始内容副本。

## 10. 最低复核问题

提交前逐条问：

- 我记录的是 original URL 还是 archive URL？
- timestamp 是 capture time、page date 还是 event date？
- 我实际打开过这个 capture 吗？
- 这是原始来源还是转载？
- 两个 URL 是否其实来自同一 evidence family？
- archive rewrite 是否改变了我看到的链接？
- 我是否为了证明一个结构性 claim 而不必要地暴露了普通个人内容？
