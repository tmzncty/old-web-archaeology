# 电大在线不是一张网页：广播、卫星、Web 与学习中心混合远程教育考古——1999–2008

> scope：中文旧网约 1995–2015；本 note 只研究 Internet 进入电大/远程教育以后，Web 如何与卫星、VBI/IP、地方学习中心、电话和线下教学共同组成事务环境。  
> cross-repo：`tmzncty/how-people-lived/sources/from-radio-tv-university-to-online-open-learning-study-without-leaving-work-china-1979-2025.zh-CN.md`  
> status：research note；尚未达到 M1 historical Web case 门槛。

## 0. 去重：不再重复“页面 != 事务”

仓库已经有自学考试网上报名、教育凭证查询、校园一卡通、在线银行、12306 等大量 state-gap 案例。本轮不再新增一个泛化的“在线教育状态丢失”。

这里真正不同的问题是：**历史上的“在线课程”可能从来就不是 Web 单通道产品。**

2000s 初中央广播电视大学的同一门课程/教学活动，可以同时跨越：

```text
纸质教材
广播/电视
数字卫星频道
VBI / satellite IP
地方教学点 LAN
WWW / E-mail / FTP / VOD
在线讨论与答疑
ISDN / H.323 双向视频
电话
短信
面授辅导
```

因此研究对象不能只定义成“网站”。本 note 把它定义为：

**`hybrid delivery system / 混合投递系统`**。

## 1. 研究单位：至少拆成六层

对早期远程教育平台，建议至少记录：

1. **course / course edition**：课程及版本；
2. **resource object**：教材、视频、IP 课件、网页、作业、测试；
3. **delivery path**：电视、卫星 IP、VBI、Web、FTP、地方缓存、实体教材；
4. **interaction channel**：电话、E-mail、BBS/讨论、在线答疑、双向视频、面授；
5. **access point**：家庭、单位、网吧、省校/分校/县级教学点；
6. **learner-specific state**：注册、选课、访问、讨论、作业、测试、成绩。

一个保存完好的 HTML 页面最多只覆盖其中的一部分。

核心不等式：

```text
course Web page preserved
!= complete course preserved
!= learner's actual delivery path known
!= learner interaction preserved
!= learner-specific study state preserved
```

## 2. 1999–2003：历史对象本来就是“天网 + 地网 + 人网”

中央电大 1999 年开始“人才培养模式改革和开放教育试点”。2003 年同期总结记录，系统已把中国教育卫星宽带多媒体传输平台、Internet 与地方电大教学网络结合起来。

截至 2002 年底：

- “电大在线”提供网络教学平台；
- 数字卫星专用频道全天播课程；
- VBI 和 IP 传教学资源/信息；
- 直播课堂与双向视频会议承担互动；
- 网上视频教学可同步卫星电视直播；
- 电视直播课堂也可同步到网上；
- 全国有 867 个 VBI 接收站、约 600 套数字卫星电视接收系统、560 套 IP 接收系统；
- 中央电大网上交互式教学活动 821 场；
- “电大在线”累计注册用户约 40 万、年访问量 757 万人次；
- 卫星 IP 通道全年播发/重播课件 2173 讲。

来源：

- CERNET/中国教育，《教育信息化建设与远程教育》：<https://www.edu.cn/listc_582/20060323/t20060323_158262.shtml> （A/B：教育年鉴式材料的现存 Web 表示）
- CERNET，《信息化推动电大教育跨越式发展》，2003-11-26：<https://www.edu.cn/li_lun_yj_1652/20060323/t20060323_83862.shtml> （B，同时代行业/制度总结）

因此“电大在线”的 archaeology 不能采用：

```text
find homepage capture
→ reconstruct website
→ declare historical course recovered
```

历史课程本来就跨多个网络。

## 3. `delivery-path ambiguity / 投递路径歧义`

同一段教学视频在当时可能通过：

- 卫星电视频道直接播；
- 卫星 IP 下发到地方；
- VBI 数据传输；
- Web VOD；
- 地方学习中心服务器；
- 录像/VCD；

到达学习者。

如果 archive 今天保存一个课程目录，它最多证明该 Web representation 存在，不能自动证明具体学习者当年从 Web 观看该视频。

因此新增一个具体 provenance 字段建议：

```yaml
delivery_path:
  observed: false
  candidates:
    - broadcast_tv
    - satellite_ip
    - vbi
    - web_vod
    - local_study_centre
    - physical_media
```

只有用户手册、访问日志、用户自述或具体操作证据能进一步收窄。

## 4. 2001–2002 陕西：所谓“网络学习”可能发生在教学点的公共电脑上

2003 年发表的《西部远程教育的网络学习环境调查与分析》使用 2001–2002 年陕西电大自评、问卷和学习者座谈。它记录：

- `WWW.SXRTVU.EDU` 提供 WWW/E-mail/FTP/VOD；
- 引入“电大在线”平台，具有资源管理、在线讨论、答疑、视频直播、网上测试；
- 地市分校建设 LAN、VBI/IP 接收、多媒体网络教室和数字卫星接收；
- 10 个地市分校中，2 个使用 128 Kbps DDN、8 个使用 512 Kbps 以上 ADSL；
- 地方分校共有 730 台计算机，其中 610 台可浏览 Internet；
- 有宽带条件者可个别上网，否则学习者可集中到教学点。

来源：

- 冀鼎全、张亚斌、王中锋，《西部远程教育的网络学习环境调查与分析》，2003-06-19：<https://www.edu.cn/jiao_xue_153/20060323/t20060323_76896.shtml> （B/A，含 2001–2002 调查与自评资料）

学习者座谈还明确指出，一部分人无力购买电脑或承担联网成本，只能到远程教学辅导中心上网。

因此新增：

### `access-point ambiguity / 接入地点歧义`

```text
registered online learner
!= home Internet user
```

未来数据集应该允许记录：

- home；
- workplace；
- Internet cafe；
- provincial TVU；
- branch / county study centre；
- unknown。

否则“网络教育普及”很容易被误写成“家庭网络学习普及”。

## 5. 2000–2004：浏览器只是更大实时通信栈的一层

CERNET 对“电大在线”技术人员的采访记录：

- 2000 年：8 个教学点以双线 ISDN 进行 256 Kbps Internet 视频试验；
- ISDN 受到电信局域/区域拨号限制，跨区域成为障碍；
- 2001 年：在北京、太原等 8 点开始 H.323 IP 视频试验；
- 2002 年：扩到 48 点同时观看 768 Kbps 视频；
- 2004 年：开始考虑让学习者从家、单位或网吧参与视频互动，而此前主要需要到教学点。

来源：

- CERNET，《远程教育被谁束缚》：<https://cernet.edu.cn/xxh/fei/jcyy/jx/yc/200603/t20060323_157316.shtml> （B，行业采访）

这提醒 M3 浏览器复原：即使历史网页本身在 IE 环境下成功加载，也未必恢复了当时的实时教学。

至少还要问：

```text
ISDN available?
regional dialing allowed?
H.323 endpoint available?
video codec available?
MCU/server alive?
bandwidth sufficient?
multicast / firewall assumptions?
```

因此：

**`browser replay success != synchronous class replay success`**。

## 6. `multi-network course state / 多网络课程状态`

这个案例真正值得写入 OWA 的不是又一个“state loss”，而是**状态同时存在于不同网络里**。

例如同一堂课可能有：

```text
broadcast schedule state
satellite transmission state
Web resource publication state
local-cache state
live-room state
student registration state
discussion/Q&A state
assignment/test state
```

这些状态的时间戳未必完全相同。

一个课程资源也可能：

- 已经在卫星下发；
- 地方服务器已经缓存；
- Web 目录还未更新；
- 某学习中心仍能访问；
- 家庭拨号用户无法观看；

所以 archive 中一次网页 capture 不足以确定“这一时刻课程是否对所有学习者可得”。

建议新增证据字段：

```yaml
network_layer:
  - public_web
  - satellite_broadcast
  - satellite_ip
  - vbi
  - institutional_lan
  - realtime_video
  - telecom_voice_sms
state_scope:
  - national
  - provincial
  - branch
  - learner_specific
```

## 7. 2005 湖南：同一场会议同时给出 Web 登录法与卫星收视法

湖南开放大学今天仍保留一份 2005-11-09 的通知，安排 2006 年春季招生工作会议。附件一要求访问：

- `http://www.open.edu.cn/`
- `http://www.openedu.com.cn/`

进入教师频道“网上会议室”，输入会议密码、单位名称、真实姓名、职务职称参加网上会议。

同一通知的附件二又给出中国教育卫星宽带传输网的接收方法，包括卫星、Ku 波段、下行频率、符号率和电视频道调谐步骤。

来源：

- 湖南开放大学，《关于召开2006年春季开放教育试点招生工作会议的通知》，2005-11-09：<https://www.hnou.edu.cn/html/840/2005-11-17/content-3169.html> （A/B：官方当前 live legacy page，内部日期 2005；本轮未核验 2005 archive capture）

这是一条非常好的 `hybrid delivery` 证据：**同一个制度活动已经同时把 Web room 和卫星 TV 当作合法入口。**

同时也要保持 archive discipline：今天能打开的官方旧正文只能证明当前 live legacy representation 保存了 2005 字段，不能自动还原 2005 年页面模板、DOM、charset、子资源或登录室运行状态。

## 8. `interaction-state loss / 学习互动状态丢失` 的具体内容

2002 年已有 821 场中央级网上交互教学活动，平台功能包括在线讨论、答疑、测试和视频直播。

如果未来只恢复公共课程页，真正消失的很可能是：

- 谁注册了课程；
- 哪些讨论帖属于哪一届；
- 教师答过什么问题；
- 学生是否参加直播；
- 测试提交与反馈；
- 访问时间；
- 课程中断后是否回来；
- 地方平台与中央平台之间的同步状态。

这些内容通常位于登录后数据库，且包含普通个人资料，既难 archive，也不一定适合重新公开。

所以即使技术上找到数据库 dump，也必须服从 METHOD 的隐私最小化原则。

## 9. 一个重要的 Web 前史边界：1999 之前不要硬塞进 OWA 主体

广播电视大学 1979 起的广播/电视/教材体系对理解 1999 后“电大在线”非常重要，但 OWA 不应因此扩成 1979–2015 中国远程教育史。

本仓只需要保留最小前史说明：

```text
pre-Internet course delivery already existed
→ Internet enters an existing distance-education system
→ Web changes interaction/addressability and resource access
→ older channels remain in parallel
```

1979–1998 的普通学习生活、广播节目表、电视/收音机实际可及和跨国 Open University 比较，放在 `how-people-lived`。

## 10. 海外对照只作为方法参照，不扩大仓库 scope

英国 Open University 1971 已通过广播电视、邮寄教材和学习中心组织远程教育；1972 年数字档案保存的 `Open Forum 45` 专门讨论学习中心中的电视/广播录音带。1989 年 Robin Mason 的论文又研究 OU 第一批大规模 computer conferencing；到 2002 年，OU 已有 Web course + computer conferencing 扩展到 12,000 多名学生的研究。

来源：

- OU Digital Archive, `Open Forum 45 (1972)`：<https://www.open.ac.uk/library/digital-archive/program/audio%3A574708b56768d>
- Robin Mason (1989)：<https://oro.open.ac.uk/56447/>
- Weller & Robinson (2002)：<https://oro.open.ac.uk/1064/>

这里只用于证明一个考古方法上的共同点：**Internet 进入远程教育时，经常是往已有多媒介体系上加一层，而不是从零建立整个制度。**

## 11. Historical locator / artifact probe

本轮取得并交叉确认的历史 locator：

- `www.crtvu.edu.cn` — 中央广播电视大学站点（2003 同期资料明确记录）；
- `www.open.edu.cn` — 电大在线学习网（2003 同期资料与 2005 官方通知明确记录）；
- `www.openedu.com.cn` — 公网镜像/电大在线相关站点（2003 同期资料、2005 通知记录）；
- `www.sxrtvu.edu` / `WWW.SXRTVU.EDU` — 陕西电大网络（2001–2002 调查记录）。

本轮也尝试搜索 `open.edu.cn`、`openedu.com.cn` 的 Wayback/CDX candidate，但执行环境没有取得一个可以实际打开并核验 `capture_datetime + historical HTTP/replay + DOM + charset + subresources` 的 1999–2005 memento。

因此只能写：

```text
historical locator identified: YES
verified historical memento in this run: NO
```

不能写：

```text
Wayback did not preserve the site
```

## 12. 浏览器/插件/协议假设清单

未来若拿到 capture，M3 至少应验证：

- IE 版本与 JavaScript / frameset / table layout；
- GB2312 / GBK / UTF-8；
- ASF/WMV/RealMedia 等历史流媒体格式；
- Windows Media / RealPlayer / ActiveX 依赖；
- H.323 / ISDN / MCU 不属于普通浏览器回放的部分；
- Web VOD URL 是否指向已丢失流媒体服务器；
- 地方缓存/代理是否使当时教学点能访问今天 archive 没保存的资源；
- 服务器端登录、讨论、测试是否完全不可复原。

尤其要防止：

```text
modern browser can render old HTML
→ falsely infer that historical learner could complete the course in-browser
```

## 13. 已证实 / 高概率 / 不知道

### 已证实

- 2000s 初中央电大远程教学是卫星 + Internet + 地方教学点等多网络系统；
- `open.edu.cn`、`openedu.com.cn` 确为当时使用的历史 locator；
- “电大在线”具有在线讨论、答疑、视频、测试等功能；
- 2001–2002 西部部分“网络远程学习者”实际上依赖地方教学点电脑；
- Internet 视频最初存在 ISDN/H.323/带宽/教学点约束。

### 高概率但未完成 artifact 验证

- 早期站点存在 frames/旧媒体插件/字符集等 M3 风险；
- 公共首页与登录后的课程/讨论空间保存概率和保存质量显著不同；
- 同一资源的地方缓存版本与中央站点版本可能存在时间差。

### 不知道

- 1999–2005 `open.edu.cn` 当前可验证的具体 capture 序列；
- 2002 一个普通学习者登录后的真实课程页 DOM；
- 讨论区、答疑、测试数据库是否存在可合法研究的历史导出；
- 各地方平台的版本、定制程度和同步机制；
- 真实 ASF/流媒体文件的历史 URL 与 codec 栈是否还能恢复。

## 14. M1 状态

这轮证据足以形成一个具体 research note，但**不满足 M1 完整案例**。

当前：

```text
historical entity identity: achieved
historical locator candidates: achieved
contemporaneous hybrid-infrastructure evidence: achieved
ordinary-access evidence: achieved
browser/protocol hypotheses: achieved
verified historical capture #1: NOT achieved
verified historical capture #2: NOT achieved
resource-missing inventory from real captures: NOT achieved
runtime replay: NOT achieved
```

所以：

**`M1 open-distance-learning platform case: NOT ACHIEVED`**。

## 15. 本轮对 old-Web archaeology 的真正贡献

这次最重要的不是再说一次“网页不是整个事务”，而是要求考古者先问：

**历史对象究竟有没有完整地生活在 Web 里？**

“电大在线”说明答案可能是否定的。

一门 2002 年的课程可以同时存在于卫星电视、VBI/IP、地方服务器、网页、实时视频、电话答疑和纸质教材里。未来即使把网站恢复得非常漂亮，也可能只恢复了整个学习系统的一张切片。

因此最合适的结论是：

**`historical Web representation != historical delivery system`**。
