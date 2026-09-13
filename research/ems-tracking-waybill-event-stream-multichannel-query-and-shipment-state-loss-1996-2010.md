# EMS tracking：运单号、节点事件、多通道查询与 shipment-state loss（1996–2010）

> 类型：research note / M1 candidate preparation
>
> 仓库 scope：约 1995–2015 中文互联网。本笔记只把 1994 的 EMS 跟踪查询网作为理解后续 Web 的必要前史；不把仓库主对象前移成“中国邮政信息化史”。
>
> cross-link：`tmzncty/how-people-lived/sources/from-postal-parcels-to-trackable-delivery-object-addressability-and-remote-possession-china-1994-2025.zh-CN.md`

## 0. 为什么这是 old-Web archaeology，而不只是物流史

历史 package tracking 很适合检验本仓库的核心原则，因为它把“页面”和“真实事务状态”的区别暴露得极其清楚。

一个 tracking 页面显示：

> 2008-03-24 10:31 到达处理中心

要使这行字出现，至少需要下面几层同时存在：

1. 一个真实物理包裹；
2. 一个稳定的邮件号 / 运单号；
3. 某个处理节点识别这个号码；
4. 节点把事件写入运营数据库；
5. 数据被同步到可查询状态层；
6. Web / SMS / 电话中的某个前端把状态渲染给用户。

因此：

`captured tracking page != preserved shipment`

甚至：

`captured query UI != preserved tracking result`

本笔记的目标是建立一套足够具体的对象模型，使未来取得 1999–2010 historical capture 后，不会把一个 HTML 表单误写成“物流系统已经被复原”。

---

## 1. 1994 前史边界：`网上` 在这里绝不能自动翻译成 `Internet/Web`

后出的 EMS 公司沿革普遍记录：**1994 年 1 月 18 日开通邮政特快专递跟踪查询网，实现快件网上跟踪查询。**

这个日期非常敏感，因为它早于中国通常采用的“1994 年 4 月全功能接入国际互联网”节点。

因此本仓库必须设一条硬规则：

### `historical 网络词汇 != modern Internet semantics`

1990s 文献中的：

- 联网
- 网上
- 查询网
- 计算机网

都必须先问“什么网、谁能接入、用什么终端、面向内部还是公众”，不能看到“网上”二字就写成 World Wide Web。

当前最保守的 reconstruction：

`EMS internal/operational tracking network (1994)`

→ 后续 `185 telephone public query`

→ 后续 `183 / ems.com.cn public Internet representation`

而不是：

`1994 public Web tracking`

当前证据等级：**C+ / B-**（后出企业沿革，多源复述；尚缺 1994 同期技术资料）。

线索：

- <https://wapbaike.baidu.com/item/%E4%B8%AD%E5%9B%BD%E9%82%AE%E6%94%BF%E9%80%9F%E9%80%92%E7%89%A9%E6%B5%81%E8%82%A1%E4%BB%BD%E6%9C%89%E9%99%90%E5%85%AC%E5%8F%B8/6597081>

这条语义警告可复用于仓库里所有“网上银行 / 网上寻呼 / 网上查询 / 网络售票”的早期材料。

---

## 2. 185 电话：public query layer 先于 Web 成为稳定入口

1996 年 9 月 25 日，邮电部发文设立全国 EMS `185` 电话特服专号，并要求各地电信部门保障中继线路。

来源：

- 《邮电部关于设立全国邮政特快专递业务“185”电话特服专号的通知》：<https://zh.wikisource.org/zh-hans/%E9%82%AE%E7%94%B5%E9%83%A8%E5%85%B3%E4%BA%8E%E8%AE%BE%E7%AB%8B%E5%85%A8%E5%9B%BD%E9%82%AE%E6%94%BF%E7%89%B9%E5%BF%AB%E4%B8%93%E9%80%92%E4%B8%9A%E5%8A%A1%E2%80%9C185%E2%80%9D%E7%94%B5%E8%AF%9D%E7%89%B9%E6%9C%8D%E4%B8%93%E5%8F%B7%E7%9A%84%E9%80%9A%E7%9F%A5>

2001 年内蒙古地方志记录，12 个盟市都已开通 185 客服中心，业务包括特快邮件查询、业务咨询、揽收、投诉等；系统具有语音导航、语音播报、电话转接、监听和夜间录音。

- <https://nmgqq.com.cn/shuzishizhi/nianjian/neimengguniajian/nianjianerlinger/jingji/2011-4-14/1702.html>

因此 EMS tracking 的 Web archaeology 不能从网页开始。它的 public interface genealogy 至少包含：

`operator-mediated lookup`

`IVR / voice prompt`

`Web self-service`

`SMS self-service`

多通道可能读同一套或部分共享的后台状态。

建议术语：

### `shared backend, heterogeneous interfaces`

同一个运营状态层可以被电话人工、IVR、短信和 Web 分别表示；archive 只存 Web representation 会造成 interface survivorship bias。

---

## 3. 2000–2004：邮政 Web 与电话中心并行，而不是替代

内蒙古地方志记录：

- 2000-11-18：内蒙古邮政 183 网站启动；
- 2000-12-18：电子邮政 183 网站开通；
- Windows 2000 Server + Oracle；
- 各盟市可以通过 163/169 拨号远程登录维护；
- 前台、后台统计、管理维护分层。

这份材料并不能证明该 183 网站的所有业务都与 EMS tracking 数据库直接相连，但它非常适合恢复当时的技术栈和“省级 portal + 地市远程维护”的组织形态。

2004 年新华社报道 `185 → 11185` 与邮政计算机互联网接入码 `183 → 11183` 同时升位，并明确说 11185 提供咨询、查询、受理、投诉。

- <https://news.sina.cn/sa/2004-06-29/detail-ikkntiam0305616.d.html>

同年 EMS 全夜航报道明确给出三种 tracking 入口：

- 短信：邮件号发往 `5185`；
- Web：`www.ems.com.cn`；
- Web：`www.183.com.cn`。

- <https://finance.sina.com.cn/b/20040811/0741939950.shtml>

所以 2004 的用户侧模型至少是：

```text
                    ┌─ phone / 11185 ─ human or IVR representation
physical parcel
      ↓
scan / event DB ────┼─ SMS / 5185 ───── short textual representation
                    │
                    └─ ems.com.cn ───── HTML representation
                       183.com.cn
```

这也是为什么未来恢复一个网页时不能说“恢复了 EMS tracking system”。

---

## 4. 运单号是 old-Web 事务的关键 join key

一般历史网页以 URL 作为对象地址；tracking 页则需要一个来自线下物理世界的 key：**waybill / mail item number**。

这个号码把不同系统连接起来：

- 纸质详情单；
- 包裹标签 / 条码；
- 分拣/处理节点；
- 内部数据库；
- 185/11185；
- SMS；
- Web 查询；
- 后来的淘宝/电商“查看物流”；
- 投诉与赔付。

建议在 artifact schema 中增加：

### `external transaction key`

它不是 account ID，也不是 page ID，而是把 Web representation 连接到一次具体线下事务的外部标识符。

tracking 研究尤其要注意：**真实 historical waybill number 本身可能关联真实姓名、地址、电话和寄递关系。**

仓库不得为了“复现”而收集、批量尝试或重新公开普通人的旧真实运单号。

实验应默认使用：

- 文档中的官方示例号码；或
- 明确无真实事务含义的 synthetic, format-valid number。

---

## 5. 2005：查询页开始与 service-level promise 绑定

2005 年中美等邮政的 EMS 承诺服务报道说明：用户可以通过 11185 或 `ems.com.cn` 查询两地邮编对应的承诺时限，同时查询邮件传递具体信息；因邮政原因超时可以退费。

- 北京晨报，2005-07-26：<https://news.sina.com.cn/o/2005-07-26/03306526163s.shtml>

这使 tracking page 不再只是“where is it”页面，而具有：

- promised-time representation；
- actual event representation；
- delay / breach evidence；
- refund eligibility 的潜在入口。

因此 archive 中若保存了一个“时限查询”表单，却没有保存当时邮编对、服务类型和后端规则，不能恢复用户当时真实看到的承诺。

建议新增：

### `policy-state dependency`

tracking / ETA / commitment 的结果依赖当时业务规则，而不是只依赖 HTML。

---

## 6. 2008 locator：今天能恢复的是入口记忆，不是 historical capture

一篇发布日期为 **2008-03-23** 的 CSDN 博客把：

`http://www.ems.com.cn/ems/index.jsp`

列为“EMS全球快递邮件号查询”。

来源：

- <https://blog.csdn.net/weixin_34101784/article/details/85400363>

这条材料的价值是：

1. 提供 2008 同时期普通网民记录的 locator；
2. 说明 EMS 查询页已经进入“常用在线查询工具”列表；
3. 给 Wayback/CDX 后续 probe 一个具体 path，而不是只搜域名首页。

但严格按 METHOD：

`contemporaneous locator != verified memento`

本轮尝试访问当前 `ems.com.cn`，Web 获取返回 412；并没有取得一个满足以下条件的 2008 capture：

- capture datetime；
- historical HTTP/replay state；
- HTML/DOM；
- declared / detected charset；
- CSS/JS/image subresources；
- form action / query parameter behavior。

因此 M1 绝不能标 achieved。

---

## 7. tracking page 显示的是 scan-event projection，不是连续“位置”

用户界面常把物流信息理解为“包裹现在在哪”。考古时应改用更窄的模型：

```text
physical motion:  continuous / mostly unobserved
                   ↓ occasional operational event
scan-event log:   E0 accepted
                  E1 processing center A
                  E2 departed A
                  E3 processing center B
                  E4 delivery attempt
                  E5 signed / locker / station
                   ↓
public projection: subset(E0 ... En)
```

因此：

### `latest recorded event != current physical location`

一个 capture 显示“离开处理中心 A”，只证明系统最后公开的事件是 A，不证明截图时包裹仍然在 A。

建议术语：

### `event-stream projection / 事件流投影`

公众 tracking 页面是内部运营事件流的一个经过筛选、延迟、重命名后的 projection。

这比笼统说“page != transaction”更具体，也可以转移到：

- 12306 seat state；
- 银行清算状态；
- 医疗预约 slot；
- 快递运输状态。

---

## 8. shipment-state loss：历史 tracking 最核心的 archive 缺口

即使一个查询页被 Wayback 完整保存，真实历史 shipment state 仍极易消失，原因包括：

1. tracking number 必须由用户输入；crawler 不知道号码；
2. 查询通过 POST / API / 动态脚本完成；
3. 运营方只保留有限期限历史记录；
4. 真实结果涉及隐私，archive 不应主动搜集；
5. status stream 可能来自动态数据库而非静态 HTML；
6. carrier 后续改写 status vocabulary 或接口；
7. 第三方电商只缓存一部分承运商事件。

建议正式定义：

### `shipment-state loss`

**tracking interface 被保存，但构成一次真实寄递事务的事件流没有被保存。**

它与 `reservation-state loss` 不同：

- reservation state 通常是未来资源锁；
- shipment state 是一个物理对象经过空间节点形成的事件流。

---

## 9. “已签收”不是单一事实：末端 status semantics 必须历史化

2019 年国家邮政局调查显示，智能柜、代收点已经大规模参与末端投递；2024 年媒体仍记录“物流详情显示已送达，本人却不知道送到哪里”的用户案例。

- 国家邮政局 2019 Q2 调查：<https://www.gov.cn/xinwen/2019-08/05/content_5418702.htm>
- 人民日报 2024-06-24 调查：<https://paper.people.com.cn/rmrb/html/2024-06/24/nw.D110000renmrb_20240624_1-11.htm>

这提示研究 2000s–2010s tracking UI 时，必须记录 status vocabulary：

- 妥投
- 签收
- 本人收
- 他人收
- 单位收发章
- 门卫/代收
- 投柜
- 驿站
- 投递未果

不同年代的“完成”可能对应不同 physical possession state。

因此：

### `status semantic drift`

同一个“delivered / signed / 妥投”标签的实际生活含义，会随末端基础设施和平台规则变化。

如果只把历史 status 字符串映射成今天的统一枚举，会丢掉这种变化。

---

## 10. 第三方平台带来 status lineage 问题

2009 前后，淘宝等电商与民营快递快速耦合。普通用户越来越可能不去 carrier 官网，而是在订单页点“查看物流”。

这意味着未来 old-Web 研究不能假设：

`platform displayed logistics == carrier original record`

可能链条是：

`carrier event DB → carrier API / scrape / data feed → marketplace normalization → buyer UI`

需要分别记录：

- carrier-originated status；
- marketplace-normalized status；
- platform cache timestamp；
- whether event labels were translated/merged；
- whether missing carrier scans became “暂无物流信息”。

建议术语：

### `status lineage / 状态血缘`

一条物流状态从哪个运营系统产生，经过哪些聚合、缓存、翻译，最后显示在什么用户页面。

这与来源 provenance 完全同构，应该成为 dynamic old-Web 的一个标准字段。

---

## 11. 海外对照：FedEx 证明 Web 只是 public query layer 的一次迁移

FedEx 第一方历史记录：

- 1979：COSMOS 中央计算系统；
- 1986：SuperTracker 手持条码扫描；
- 1994：fedex.com 提供 online package status tracking。

- <https://newsroom.fedex.com/newsroom/global-english/fedex-marks-40th-anniversary-with-community-service-eye-to-the-future>
- <https://www.fedex.com/en-us/about/history.html>

FedEx 2009 年公司材料又说，早期客户可以通过 toll-free call 查询；1995 年 Web 日均 tracking 请求约 9000 次，到 2008-12-23 单日约 980 万次。

- <https://newsroom.fedex.com/newsroom/united-states-english/fedex-refreshes-web-tracking-tools>

所以跨国上更合理的谱系是：

`operational event capture → centralized tracking DB → call-center access → Web self-service → push/mobile`

而不是：

`Web invented package tracking`

这与中国 EMS 的 1994 tracking network → 185 → Web/SMS 路线形成很好的结构性对照。

---

## 12. 可进入 artifact schema 的字段

未来若取得 historical capture，建议为 tracking 类页面记录：

```yaml
artifact_type: shipment_tracking_ui
carrier: EMS
capture_datetime:
historical_url:
page_identity:
charset_declared:
charset_detected:
form_method:
form_action:
tracking_number_field:
validation_pattern:
captcha_present:
client_side_js_required:
result_delivery:
  - same_page
  - popup
  - new_page
  - frame
  - api_async
status_fields:
  - event_time
  - event_location
  - status_text
  - signer
  - delivery_office
external_transaction_key: waybill_number
backend_state_preserved: false
real_shipment_replay_attempted: false
privacy_note: do_not_probe_live_or_historical_real_people_waybills
```

如果只能恢复查询 UI：

```yaml
claim_level: interface_only
```

绝不写：

```yaml
claim_level: historical_shipment_recovered
```

---

## 13. 隐私与安全规则

tracking 页面比普通新闻页敏感得多，因为历史 result 可能包含：

- 姓名；
- 手机/固定电话；
- 详细地址；
- 工作单位；
- 寄件人与收件人的关系；
- 时间和空间轨迹。

因此：

1. 不批量搜索真实历史运单号；
2. 不尝试“猜”仍可查询的旧号码；
3. 不把搜索结果中的普通人号码重新结构化提交仓库；
4. screenshot 若含普通人 PII，应裁切/打码或只记录 schema；
5. runtime reconstruction 只使用官方 demo / synthetic data；
6. archive capture 本身公开 ≠ 可以无条件再传播其中 PII。

这一规则与仓库已有 credential-afterlife 研究一致。

---

## 14. M1 当前准确状态

本轮已完成：

- [x] 历史服务 identity：EMS tracking / 185 / 11185 / 183 / ems.com.cn；
- [x] 1996 以后电话公共查询制度证据；
- [x] 2000–2001 183/185 地方部署证据；
- [x] 2004 Web + SMS + phone 多通道同期证据；
- [x] 2008 `ems/index.jsp` contemporaneous locator；
- [x] transaction/event-stream model；
- [x] privacy boundary；
- [x] overseas comparison。

仍未完成：

- [ ] 一个实际打开、核验过的 1999–2010 `ems.com.cn` historical memento；
- [ ] capture datetime + HTTP/replay metadata；
- [ ] 原 HTML / DOM / charset；
- [ ] CSS/JS/images/subresources；
- [ ] 第二个历史时点；
- [ ] 合法、安全的 result-state replay；
- [ ] 2000s 原始客户端/扫描设备运行环境。

因此：

**M1 complete case: NOT ACHIEVED.**

尤其不能写“Wayback 没保存”；本轮只能写“没有取得并实际核验满足仓库证据合同的 historical memento”。

---

## 15. 下一步 artifact hunt

优先搜索 locator：

1. `http://www.ems.com.cn/ems/index.jsp`（2008 contemporaneous locator）；
2. `http://www.ems.com.cn/`；
3. `http://www.183.com.cn/`；
4. 2004 新闻中可能链接的查询页；
5. 地方 `183` 电子邮政站点；
6. 2005 “承诺时限查询”相关 path。

取得 capture 后先做：

`capture identity → HTTP → charset → form/action → subresources → no-submit replay`

不要先输入任何真实历史运单号。

可继续找的非 Web artifact：

- 185/11185 操作手册；
- EMS 旧详情单；
- 条码规范；
- 扫描设备说明；
- 状态码/状态词表；
- 2000s 邮政信息化技术论文；
- 淘宝早期“查看物流”帮助文档。

---

## 16. 本轮对 OWA 方法的实质增量

这次不是再写一遍 `page != transaction`，而是把动态 tracking 具体拆成：

1. **pre-Internet backend networkization**：内部联网早于 public Web；
2. **external transaction key**：线下运单号是 Web 事务 join key；
3. **event-stream projection**：Web 展示是运营事件流的投影；
4. **shipment-state loss**：查询 UI 保存不等于历史寄递状态保存；
5. **status semantic drift**：“妥投/签收”的生活意义会变；
6. **status lineage**：承运商事件经过第三方平台聚合后需要来源血缘；
7. **shared backend, heterogeneous interfaces**：电话/SMS/Web 可能只是同一后台的不同窗口。

这些规则可迁移到本仓库其他动态事务型旧网对象，而不需要扩张仓库 scope。
