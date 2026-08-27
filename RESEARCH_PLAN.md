# RESEARCH_PLAN.md — Old Web Archaeology

## Phase 0 — Method contract

- [ ] `docs/METHOD.md`：A/B/C/D 证据等级细则；
- [ ] `docs/CITATION.md`：archive URL、original URL、capture datetime、访问日期；
- [ ] `schemas/evidence.schema.json`；
- [ ] `datasets/sites.csv` 字段；
- [ ] reconstruction 标识规则；
- [ ] 个人隐私/已删除内容再发布边界；
- [ ] 3 个 evidence fixture 验证 schema。

验收：同一 capture 由两个 agent 编目时关键字段基本一致。

## Phase 1 — Candidate survey

列出约 15 个 1995–2010 中文旧网站/平台候选，覆盖个人主页、论坛/BBS、博客/SNS。逐一记录：

- 已知 URL/域名；
- 活跃时期；
- Wayback/ArchiveTeam/Common Crawl 等可得性；
- 是否有多个时点；
- 是否涉及明显隐私/版权风险；
- 研究价值；
- 证据断裂点。

只调查，不做大规模抓取。

## Phase 2 — Three complete cases

选择三类不同对象。每个 case 至少：

- identity confirmation；
- ≥2 历史时点；
- 尽可能 ≥2 独立证据源；
- `evidence.yaml`；
- `timeline.md`；
- `reconstruction.md`；
- 资源缺失清单；
- browser/encoding/plugin assumptions；
- 已证实/高概率/不知道；
- 至少一处“后来回忆 vs 同时代证据”比较。

## Phase 3 — Platform genealogy

产出：

- [ ] `studies/platform-genealogy.md`；
- [ ] `datasets/platforms.csv`；
- [ ] ≥20 个平台/站点时点证据；
- [ ] URL ownership / content ownership / identity / link model 比较。

主线可从个人主页 → 论坛/BBS → 托管博客 → 平台社区 → SNS/信息流，但证据不支持时不得硬凑线性进化。

## Phase 4 — Browser environment experiment

设计并执行一个最小可复现实验，比较：modern Chromium、IE5/IE6 级环境、条件允许时 Netscape、Flash/Ruffle/插件缺失。

记录 CSS/布局、编码、JS、ActiveX/Java/Flash、字体、图片、viewport 差异。

验收：一个案例至少列出 5 个环境导致的解释差异。

## Phase 5 — Archive gap model

成熟后再扩大样本：

- [ ] gap 数据模型；
- [ ] 100 个样本站点；
- [ ] 年份/resource/platform 缺失统计；
- [ ] robots/login/JS/dynamic URL 等系统性保存偏差；
- [ ] sampling bias 说明。

## Phase 6 — Optional public presentation

只有方法和案例稳定后才考虑 Pages/可视化。展示必须让 provenance、证据等级、缺失和 reconstruction 标记比视觉复原更显眼。

## 每阶段门禁

- 证据可定位；
- 日期与 URL 清楚；
- inference 显式；
- 隐私/版权自查；
- 不自动补历史空白；
- 负结果/缺失也保存；
- checkpoint 后继续。
