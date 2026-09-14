# 共享外设与纸—数往返：照片上传、打印、扫描、传真与浏览器之外的事务状态（2004—2015）

> Scope：本 note 研究约 2004—2015 中文 Web 事务中一个容易被 archive 忽略的层：**网页要求用户离开浏览器，借打印机、扫描仪、数码相机、照相馆、传真机、复印店、单位盖章等完成一次状态转换，然后再回到 Web。**
>
> 1990s 传真/公用数据通信只作为必要前史；普通生活中的长期演化写入 `how-people-lived`。本仓不扩成中国办公自动化史或印刷史。

关联 HPL 研究包：

- <https://github.com/tmzncty/how-people-lived/blob/main/sources/from-copy-shop-and-photo-studio-to-self-service-document-conversion-shared-peripherals-and-paper-digital-braids-china-1992-2026.zh-CN.md>

---

## 0. 去重：为什么已有 state-gap 文件还不够？

本仓已经有：

- `CIVIL_SERVICE_ONLINE_REGISTRATION_QUALIFICATION_PAYMENT_ADMIT_CARD_AND_HIRING_STATE_GAPS_2004_2015.md`
- credential / education verification 相关研究；
- internet-cafe terminal context；
- 各类 appointment / payment / application state-gap note。

其中公务员报名 note 已经很好地拆开：

```text
announcement
→ registration
→ qualification review
→ confirmation
→ photo
→ payment
→ admit card
→ exam
→ downstream hiring
```

本文件不再重写这条业务链。

缺口在另一个方向：

> **同一个 Web transaction 的状态并不都生成在 Web 内。**

例如 `photo uploaded = true` 背后可能是：

```text
实体照片
→ 扫描仪
→ JPG
→ 用户上传
```

也可能是：

```text
用户拿打印出来的照相凭条
→ 指定照相馆
→ 店员拍摄/裁切
→ 店员直接把 JPG 写入报名系统
```

又或者：

```text
纸质低保证明复印件
→ 传真机
→ 考试中心人工审核
→ Web payment-status 被后台改成“确认成功”
```

archive 如果只保存浏览器页面，会把这些路径压成同一个结果字段。

因此本 note 的研究单位不是“一个考试网站”，而是：

## browser ↔ peripheral ↔ intermediary ↔ paper ↔ backend 的跨介质状态转换

---

## 1. 新增证据对象与 gap

### 1.1 off-browser execution layer

定义：一个 Web 流程中，必须或可选地在浏览器外完成、但会改变 Web transaction 可继续性的动作层。

典型动作：

- 打印凭条；
- 扫描纸证件；
- 拍电子照片；
- 由照相馆代传；
- 传真证明；
- 打印表格；
- 手写签名；
- 单位盖章；
- 带纸到现场；
- 之后再回网站查询状态。

### 1.2 peripheral-state invisibility

一张历史页面能够证明：

`页面要求上传 JPG`

通常不能证明：

- 用户是否有扫描仪；
- 用户是否去过照相馆；
- 照片由谁处理；
- 打印任务是否成功；
- 页面输出的 PDF/HTML 是否按要求落纸；
- 传真是否真正到达。

### 1.3 intermediary-operator state

有些中介不是“用户自己不会，所以求助”，而是被制度正式写进流程。

例如 2008 广州人事考试的**指定照相馆**：

```text
print voucher
→ designated studio
→ studio uploads photo directly
→ candidate later checks web state
```

此时 historical transaction 的 actor 不只有：

`user + website`

还包括：

`authorized local operator`。

### 1.4 continuation-key state

跨介质流程通常需要某个 key 让纸、线下动作与 Web account 重新汇合：

- 报名序号；
- 准考证号；
- 照相凭条；
- 条码；
- 身份证号；
- 打印表上的编号；
- 传真件上手写的申请号。

这类 key 往往比页面视觉更接近 transaction 的骨架。

### 1.5 paper-roundtrip state

定义：由 Web 生成的内容落到纸上，经过签字/盖章/粘贴/现场核验后，又影响后续数字或制度状态。

```text
Web form
→ printed form
→ signature / seal / photo
→ physical retention / onsite review
→ downstream eligibility
```

capture 只能保存第一箭头之前的一部分。

### 1.6 local-file provenance gap

历史 `<input type=file>`、上传按钮或照片说明被保存，不代表：

- 当时上传文件仍在；
- 文件生成设备已知；
- EXIF/原始文件已保存；
- 用户实际上传的就是今天页面上描述的规格；
- 当前 replay 能安全重放 upload。

研究上尤其不能为了“复原”去搜普通人的真实身份证照片、证明扫描件或报名文件。

---

## 2. 2008 广州：一个几乎为 off-browser archaeology 量身定做的工作流

2008 年广州市人事考试中心经济专业技术资格考试通知保留了一条非常完整的 contemporaneous workflow。

同期转载：

- <https://www.chinaacc.com/new/15/22/48/2008/4/lu113513204413480024876-0.htm>

通知中的历史 Web host 至少包括：

- `中国广州人事网`
- `广州考试信息网`

同年另一份职称外语报名通知明确给出：

- `http://www.gzexam.com.cn`
- `http://www.gzpi.gov.cn/gzexam`

来源：

- <https://www.chinaacc.com/new/15_2_/2008_11_20_lu655912485010211800219908.shtml>

### 2.1 contemporaneous workflow

2008 经济师流程可以重建为：

```text
Internet-connected computer
→ login / personal data
→ select exam
→ PRINT PHOTO VOUCHER
→ leave Web
→ designated photo studio
→ studio takes compliant photo
→ studio directly uploads into registration system
→ candidate waits ~24h
→ candidate returns to Web and checks photo
→ online confirmation
→ online payment
→ PRINT registration/certificate form
→ employer review + seal
→ user stores paper for later certificate handling
→ before exam download + A4 PRINT admit card
→ physical exam gate checks paper card + physical ID
```

### 2.2 这不是普通的 `page != transaction`

这里至少有五类 archive state：

1. **public instruction page**；
2. **authenticated account/application state**；
3. **printed continuation artifact**（照相凭条）；
4. **authorized studio upload state**；
5. **paper-after-Web state**（单位盖章后的登记表、A4 准考证）。

即使 Wayback 把第 1 类和某些静态表格保存得完美，也几乎不会保存 3—5。

### 2.3 photo spec 也是 executable environment 的一部分

该通知还把照片规定到：

- 482×689 px；
- 350 dpi；
- 24-bit RGB；
- JPEG；
- 通常 20–30 KB；
- 白底；
- 头像位置也有像素级约束。

因此 M3 浏览环境复原如果只问“IE6 能不能显示页面”，仍然不够。

真实问题还包括：

> 当时的用户怎样生成一个系统会接受的本地 artifact？

---

## 3. 2008 江西国考：同一个 upload state 有三条生成路径，特殊资格又走传真

江西考区 2009 国家公务员考试报名确认（2008-11）同期说明：

- <https://edu.sina.com.cn/official/2008-11-03/1618173125.shtml>

电子照片可来自：

1. 扫描仪扫描实体照片；
2. 数码相机拍摄；
3. 照相馆拍电子版并由工作人员处理。

这直接证明：

## same server-side field, different historical production paths

后台最终可能都只是：

`photo accepted = true`

但生活史/考古 provenance 完全不同。

### 3.1 困难考生的 cross-medium fallback

对于申请减免考试费的困难家庭考生，说明允许：

```text
upload photo in web system
→ paper proof / low-income certificate
→ photocopy
→ fax to exam center
→ staff review
→ wait 24h
→ return to Web
→ check payment/confirmation state changed
→ bring originals to exam site later
```

传真件上还要求注明：

- 报名序号；
- 姓名；
- 身份证号；
- 联系电话。

这是一种标准的 **out-of-band state mutation**：

> 后台状态改变的触发事件，不发生在浏览器里。

### 3.2 archive implication

如果将来保存到了江西确认系统页面：

- 不能从“确认成功”字段推断用户是网上支付还是困难减免；
- 不能从“照片通过”推断照片来自扫描仪还是照相馆；
- 更不能从 public instruction page 推断某个真实用户走过哪条 fallback。

---

## 4. 2008 山西：浏览器 archaeology 与本地 artifact archaeology 必须同时做

山西考区同期说明：

- <https://edu.sina.com.cn/official/2008-11-03/1522173099.shtml>

明确要求：

- IE 6.0 以上；
- 调整 IE security level；
- 启用 ActiveX 控件和插件；
- 上传 20KB 以下 JPG。

因此一个最低可执行环境不是：

```text
IE6 VM
```

而至少是：

```text
historical browser settings
+ reachable application host
+ local valid JPG
+ file-picker access
+ payment path
+ printer / printed admit-card path
```

这对 M3 有直接方法意义：

## browser completeness fallacy

**旧浏览器成功打开页面，不等于历史工作流已经被复原。**

---

## 5. 纸不是 Web 的“前一个阶段”：它可以是 Web transaction 的中间状态

### 5.1 典型错误模型

```text
paper era
→ web era
→ mobile era
```

### 5.2 contemporaneous evidence 支持的模型

```text
paper identity document
→ scan / photo
→ Web application
→ server-side review
→ print
→ signature / seal
→ physical gate
→ later database state
```

这也是为什么 archive 不能只按 MIME type 统计“HTML 保存率”。

一个制度页面的真正可执行性，还依赖 crawler 通常看不到的：

- local file；
- OS print subsystem；
- physical printer；
- scanner/camera；
- fax network；
- third-party photo studio；
- physical signature/seal；
- in-person clerk。

---

## 6. 1990s 前史边界：传真/传真存储转发解释了为什么 Web 后仍保留 fax fallback

这部分只作必要背景，不把 OWA scope 前推成电信史。

国家统计局历史表记录 1995—1997 全国传真业务量分别约 442.3 万、565.0 万、711.8 万份：

- <https://www.stats.gov.cn/yearbook/1999/o38c.htm>

1999 年国家统计局的五十年通信业回顾又写到，1998 公用数据通信网已经提供“传真存储转发”和“计算机互联网访问”等多种并列业务：

- <https://www.stats.gov.cn/zt_18555/ztfx/xzg50nxlfxbg/202303/t20230301_1920449.html>

所以 2008 年报名系统把 fax 作为 fallback，并不是网页时代突然发明一个奇怪旁路。

更准确地说：

> **Web transaction 把一套更老的远程文件传输基础设施接成自己的异常/辅助路径。**

---

## 7. 对 OWA evidence schema 的新增建议

当目标是事务型页面时，建议 evidence/case note 增加以下字段（命名可后续 schema 化）：

```yaml
execution_context:
  local_file_required: true
  local_file_types:
    - jpeg
  peripheral_dependencies:
    - printer
    - camera_or_scanner
  authorized_intermediary:
    - designated_photo_studio
  printed_artifact_required: true
  physical_signature_or_seal: true
  out_of_band_channels:
    - fax
    - onsite_counter
  continuation_keys:
    - registration_number
    - photo_voucher
  returns_to_web_after_offline_step: true
```

每个字段都应允许：

- `required`
- `optional/fallback`
- `unknown`

而不是二元 present/absent。

### 7.1 为什么这比“页面截图”有用？

它能区分：

```text
一个浏览器里能完整完成的服务
```

和：

```text
页面只是一个 orchestration surface，真正事务散落在浏览器、店铺、纸张和现场之间
```

后者在 2000s 中文 Web 极其常见。

---

## 8. artifact-preservation implications

### 8.1 哪些东西适合保存

优先：

- contemporaneous public instruction pages；
- blank form / template；
- photo specification；
- historical host / URL pattern；
- print-button / file-upload control 的存在；
- browser requirement；
- fallback channel description；
- continuation-key schema；
- blank voucher / redacted sample；
- historical manuals/screenshots with provenance。

### 8.2 哪些东西不应为了“完整”而重新收集

不要批量搜集/公开：

- 普通考生真实身份证照片；
- 身份证扫描件；
- 低保证明；
- 报名序号与身份证号组合；
- 真实准考证；
- 传真中的联系电话和家庭材料；
- 用户提交的原始报名表。

**事务考古的完整性不能以重建普通人的敏感档案为代价。**

### 8.3 可以怎样做 reconstruction

如果未来做 M3：

- 使用 synthetic identity；
- 自制符合历史规格的测试 JPEG；
- 使用 dummy printer / print-to-file 记录页面输出；
- 明确标 `reconstruction`；
- 不向仍然存活的真实考试后台提交测试数据；
- 不把现代页面响应冒充历史 backend state。

---

## 9. 当前 artifact 状态

本轮可以确认：

### 已取得

- 2008 广州考试工作流的同期完整文本；
- historical host：`gzexam.com.cn`、`gzpi.gov.cn/gzexam`；
- 打印照相凭条、指定照相馆直传、24h 后查询、网上支付、打印表格、单位盖章等 workflow；
- 2008 江西的 scanner / digital camera / photo studio 三种 photo-production path；
- 江西困难考生 fax fallback → Web state update；
- 山西 IE6 / ActiveX + local JPG 的环境要求；
- 1990s fax / store-and-forward 的通信前史。

### 尚未取得

- 一个实际打开核验的 2008 `gzexam.com.cn` application memento；
- capture datetime；
- historical HTTP/replay status；
- registration DOM；
- charset；
- JS/ActiveX 资源；
- photo upload endpoint；
- print CSS / actual voucher HTML；
- designated studio operator interface；
- 第二个历史时点。

因此当前准确状态是：

```text
historical service identity: achieved
historical host/locator: achieved
contemporaneous workflow evidence: achieved
browser/peripheral dependency model: achieved
verified historical transaction capture: NOT achieved
second verified historical timepoint: NOT achieved
M1 complete case: NOT achieved
```

搜索不到或当前环境打不开 archive 不能写成“当时没有页面”或“Wayback 没保存”。

---

## 10. 与现有公务员 note 的关系

现有公务员 note 的核心单位是：

> **application lifecycle**

本 note 的核心单位是：

> **state 如何跨 browser / local artifact / peripheral / human intermediary / paper / backend 迁移**

两者的关系类似：

```text
业务状态机
×
媒介转换状态机
```

以后处理：

- 学历认证；
- 招聘简历；
- 医院材料；
- 签证；
- 网上银行证书；
- 房产/贷款申请；
- 政务表单；

都可以复用这个二维模型，而无需为每个场景重新发明 `page != transaction`。

---

## 11. 海外比较：Kinko's 提醒我们不要把“家庭没有设备”写成“用户无法执行数字/办公任务”

1995 年 WIRED 同期报道 Kinko's 时，门店已经把：

- state-of-the-art photocopiers；
- computers rented by the hour；
- LaserWriter output；
- desktop publishing；
- photo processing；
- videoconferencing

组合成一种共享信息机器服务。

来源：

- <https://www.wired.com/1995/06/kinkos/>

这说明 `peripheral access without ownership` 不是中国特例。

对 OWA 更直接的方法启示是：

> **历史 Web 用户环境不只由“家里那台电脑”构成。**
>
> 一个用户完全可能在 copy shop / campus lab / internet cafe / office 完成 local-file preparation、printing 和 submission。

因此 M3 的 `access context` 字段应允许：

- home PC；
- work/school PC；
- internet café；
- copy/print shop；
- photo studio；
- public/service counter；
- unknown。

---

## 12. Known / probable / unknown

### 已证实

- 2008 多个中国考试 Web 流程明确依赖浏览器外的照片、扫描、打印、传真或现场动作；
- 一些照相馆是制度指定的直接上传节点；
- fax 可以触发人工审核并让 Web 状态随后变化；
- 某些报名系统明确要求 IE6/ActiveX，同时又要求本地 JPEG；
- 纸质输出仍可能是进入考试现场的最终 gate artifact。

### 高概率但仍需更多 artifact

- 打字复印店/照相馆应当是早期 Web transaction 的重要 access-support layer；
- 同一个 public form 在家庭、网吧、文印店和单位电脑上具有不同的实际可执行成本；
- 很多 archive “页面缺失”研究其实还漏了一类问题：**页面保存了，但 off-browser execution context 永远没有进入 crawler。**

### 不知道

- `gzexam.com.cn` 2008 报名页面的真实 DOM 与 capture 状态；
- 指定照相馆使用的 operator-side client/UI；
- photo voucher 上实际有哪些 continuation key；
- fax review 如何写回后台；
- 用户本地打印失败/照片规格失败的真实发生率；
- 各类共享外设路径的使用比例。

---

## 13. 对 old-web archaeology 的最小结论

本轮最需要保留下来的不是“2008 年网上报名还要打印”。

而是：

> **历史 Web 页面可能只是一个跨媒介流程的控制面。**

用户真正完成一件事时，状态会离开 HTML：

```text
browser
→ printer
→ paper voucher
→ photo studio
→ local/remote JPEG
→ backend
→ browser
→ print form
→ signature/seal
→ physical gate
```

所以：

## archived page != archived execution environment

而且这里的 “environment” 不应只理解为 IE6、Flash、GBK 或屏幕分辨率。

它还包括：

> **街角那台打印机、照相馆的相机、办公室的复印机、传真线路、单位公章，以及把这些东西和报名序号连接起来的人。**
