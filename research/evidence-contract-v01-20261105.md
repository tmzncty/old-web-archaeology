# Evidence contract v0.1 — schema 与边界

本文件对应 ROADMAP M0 的 `schemas/evidence.schema.json` 与三个**合成** fixture。所有 `example.org` URL、日期、声明仅供结构验证，**不是旧网史料**。

## 对象与目的

本轮不是新增一个未核实的旧站故事，而是把仓库已有的 51.net、ChinaRen、263、SMTH、MSN Spaces 等 bounded notes 共同暴露的证据混淆问题固化为机器可检验的最低合同。当前 M0 尚缺 schema，M1 的完整案例、M3 浏览器实测也尚未完成。

- `subject.kind` 区分平台、host、主页、page、capture。
- `evidence[]` 保存 source ID、evidence family、A/B/C/D、verification、original URL、capture URL、日期和浏览器假设；不把 locator-only 自动视为直接验证。
- `claims[]` 把可检验断言与 source ID 分开；同一 family 的转载不自动成为两个独立证据源。
- `reconstruction.is_reconstruction=true` 时必须填写原件、缺失、替代、工具、假设和未决差异。
- `privacy_review` 与 `copyright_review` 保留最小审查状态，禁止把“档案可读”当作“允许再分发”。

## 证据来源与等级

1. **A（技术规范本身）**：Library of Congress, *WARC File Format Published as an International Standard*, **2009-06-04**, https://www.digitalpreservation.gov/news/2009/20090604news_article_warc.html 。具体定位：正文对 WARC 的 HTTP request headers、metadata、record ID、duplicate handling 的说明。可支持“归档对象有请求/响应与元数据层”，**不能**证明某个 2000 年中文网页已经被 WARC 保存。
2. **A（标准文档）**：ISO 28500:2017, *Information and documentation — WARC file format*, **2017-08**, https://www.iso.org/standard/68004.html 。具体定位：Abstract 对 payload/control information、metadata、duplicate detection、record integrity 的定义。2017 标准不应倒填成 1995 年浏览器技术。
3. **A（软件技术文档）**：Wayback CDX Server README, https://github.com/internetarchive/wayback/tree/master/wayback-cdx-server （参考 CDX server README 的 `urlkey,timestamp,original,mimetype,statuscode,digest,length` 字段）。这是索引字段语义，不代表 capture 主体、DOM 或媒体资源已人工核验。
4. **A（本仓既有方法合同）**：`docs/METHOD.md`、`docs/CITATION.md`；它们是本项目规范的直接依据，而非中文互联网历史事件的一手史料。

上述 1–3 是两个以上独立机构的**方法学证据**，不是针对某一历史站点的独立见证。本轮不新增平台历史结论。将此 schema 用于任何站点前，仍须另行取得该站点至少两个独立 evidence family。

## 不得声称

- JSON Schema 校验通过 ≠ 史料为真、source ID 确实存在、支持关系有效、来源独立。
- `evidence_grade=A` + `verification=locator-only` ≠ A 级内容已经核验。
- `capture_datetime` ≠ `page_date` ≠ `event_date`。
- `statuscode=200` ≠ 原始页面完整，也不证明 JS、图片、插件可执行。
- WARC 的 digest 与 CDX 的 digest 不应在未确认算法和数据范围时直接比较。
- `reconstruction=true` ≠ 历史页面；任何视觉复原都必须明显标注。

## 可复原程度与下一步

本轮可复原的是**证据记录结构**，不是历史站点。下一步先用三个真实、经授权的 archive capture 做双 Agent 字段一致性测试，再增加 cross-reference 校验（claim.supports 必须命中 source_id、source_id 唯一、同 family 去重），并把 `datasets/sites.csv` 的字段合同独立定稿。M0 不因有 schema 就全部完成，M1/M3 均保持未完成。

## 隐私与版权

fixture 使用虚构对象与保留域名 `example.org`，不含普通用户隐私、历史 HTML、图片或专有二进制。真实案例只存元数据、少量必要引文和合法可再分发的资源；对已删除个人内容不批量恢复公开。
