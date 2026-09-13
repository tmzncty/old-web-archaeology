# 网吧共享终端：接入环境、计费壳、实名 session 与本地状态缺口（约 1998–2012）

> 类型：cross-repo research note / access-environment archaeology  
> HPL companion: `tmzncty/how-people-lived/sources/internet-cafes-public-terminal-access-shared-machines-and-metered-digital-life-china-1996-2026.zh-CN.md`  
> 仓库 scope：只讨论约 1995–2015 中文旧网的用户接入环境与保存问题；全球 Internet café 比较留在 HPL，不把本仓扩成全球网吧史。  
> 本轮状态：取得多条 2002–2006 同期软件/制度证据和一个 2003 仍存活的 17173 产品页，但未取得足以形成 M1 完整案例的 ≥2 时点 historical capture。

## 0. 去重：这不是再写一次“旧网页在现代浏览器里不一样”

本仓已经有：

- IE/ActiveX/银行控件造成的客户端栈资格；
- 登录态和 private account state 的保存缺口；
- 心理论坛的昵称/匿名层；
- 淘宝卖家/市场状态丢失；
- CFido 非 Web operational artifact。

这次补的是一个更靠下的层：

> **用户甚至还没有进入某个网站以前，网吧那台公共电脑已经在通过计费软件、桌面限制、还原工具、营业规则和实名登记塑造可执行的网络生活。**

因此新的研究单位不是 page，而是：

## **`public access session / 公共终端接入 session`**

最小结构至少包括：

```text
physical venue
→ workstation
→ OS / browser / installed client
→ management & billing shell
→ identity-registration state
→ local filesystem / restore policy
→ network connection
→ website/platform account
→ user action
```

如果只复原最后一层网页，就会漏掉大量历史约束。

---

## 1. 一个关键不等式：`historical page replay != historical access replay`

旧网研究通常会问：

- HTML 还在吗？
- CSS/图片在吗？
- IE6 能不能显示？
- charset 是什么？

但对于网吧用户，同一个页面是否可执行还取决于：

- 这台机器上装的是 Windows 98 / 2000 / XP 的哪一个版本；
- IE、QQ、下载工具、输入法、Flash/Java 是否预装；
- 网管软件是否禁用了“运行”、控制面板、复制粘贴或安装程序；
- 一小时多少钱，还剩多少时间；
- 是否必须出示身份证/上网卡；
- 下载文件是否能写入持久分区；
- 重启以后本地文件/新安装程序是否消失；
- 店内是否限制某些程序、端口或网络行为。

因此本轮固定：

## **`access-environment state / 接入环境状态`**

以及保存缺口：

## **`access-environment state loss / 接入环境状态丢失`**

Web archive 保存一个 URL，并不会自动保存当年普通用户到达这个 URL 的整条本地环境。

---

## 2. 2002 同期证据：网管软件和“还原精灵”直接改变用户可以做什么

2002-10-22，《大众网络报》文章《并非无懈可击 网吧网管软件有致命伤》由新浪科技保存。它不是网吧管理软件厂商说明，而是面向当时用户的技术文章；恰恰因为作者在讨论如何绕过限制，反向留下了非常具体的终端环境证据。

页面直接提到：

- 网吧管理软件会屏蔽某些 Windows 操作；
- 《美萍》等管理工具限制用户进程/操作；
- 某些网吧使用《还原精灵》硬盘还原程序；
- 用户收到、下载并安装一个程序后，如果需要重启，重启后新装程序可能消失，因为系统恢复到原状态。

来源：

- 新浪科技 / 《大众网络报》，2002-10-22：  
  https://tech.sina.com.cn/c/2002-10-22/16179.html

**证据等级：B+（同期技术文章）。**

它不能证明所有网吧都安装同一款软件，也不能证明文章里的绕过技巧对所有版本有效；但可以证明一个十分重要的历史用户动作约束已经存在：

```text
我在网页上下载到了文件
!= 这个文件会在本机长期存在

我安装了客户端
!= 重启以后仍然安装着
```

所以 OWA 以后遇到旧站“请下载安装 X 客户端 / 插件”的帮助页时，不能默认公共终端用户能把安装状态持久保存。

这形成：

## **`local-persistence gap / 本地持久状态缺口`**

尤其对：

- 下载器；
- 游戏客户端；
- 输入法；
- 邮件附件；
- 聊天记录；
- 浏览器收藏夹；
- cookie；
- 本地缓存；
- 插件；
- 文档草稿；

都需要单独问：**用户下次换机器或机器重启以后，它还在吗？**

---

## 3. 2003 17173 产品页：计费软件本身就是历史浏览环境的一部分

17173 至今仍保留一篇日期为 2003-02-28 的同期产品页《17173吉胜携手合作 冰点网管今春上架》。页面描述“冰点网管”由既有网管软件演化，用于游戏机房、网吧、培训班、学校机房等，并明确列出功能：

- 管理、监控局域网；
- 对客户端运行进行记录；
- 计费、计时；
- 限制用户使用程序；
- 远程控制计算机。

来源：

- 17173，2003-02-28：  
  https://news.17173.com/content/2003-2-28/n897_813408.html

**证据等级：A-/B+。** 页面本身是至今仍在线的 2003 日期产品报道/宣传材料，可直接证明当时产品这样宣称功能；不能自动证明每个功能在所有部署中可靠生效。

页面还留下两个当年的具体 locator：

```text
http://netbar.17173.com/bdgl1.htm
http://netbar.17173.com/news/content/2003-2-26/n57_973747.html
```

前者是“详细的软件说明”，后者是“详细的购买流程”。当前普通访问已无法获得原内容；本轮也**没有**实际核验到可用 historical memento，因此它们只能登记为：

- historical original-URL locator：已知；
- current original resource：不可正常取得；
- verified archive capture：**not achieved**。

这正符合 `docs/METHOD.md`：搜索/引用中存在历史 URL，不等于我们已经验证 archive capture。

这里新增一个需要进入旧网页复原的环境层：

## **`billing-shell overlay / 计费壳覆盖层`**

当用户面对 IE/QQ/游戏时，桌面上可能还叠着另一套软件状态：

```text
剩余金额
剩余时间
登录/下机
程序白名单/黑名单
远程控制
锁屏/解锁
```

这些元素未必属于网站 DOM，却可能比网站导航更直接地决定一次浏览能持续多久、哪些程序能启动。

---

## 4. 2002–2006：应用昵称制与接入场所实名制可以同时成立

2002 年施行的《互联网上网服务营业场所管理条例》要求网吧等营业场所核对并登记上网消费者的有效身份证件，并记录有关上网信息。

来源：

- 中国新闻网同期报道，新浪，2002-11-14：  
  https://news.sina.com.cn/c/2002-11-14/1655456s.html
- 深圳市政府保存的 2002 年重新审核登记工作方案：  
  https://www.sz.gov.cn/zfgb/2003/gb317/content/post_5020634.html

**证据等级：A-/B+。**

2006 年长沙把这个身份层进一步计算机化。同期报道说，长沙要求新版“网络110”网吧管理软件与计费系统对接，通过键盘录入实名信息或身份证读卡器进行验证。

来源：

- 红网 / 潇湘晨报，新浪，2006-06-17：  
  https://news.sina.com.cn/o/2006-06-17/03439224242s.shtml

合肥同年则从纸质登记簿转为实名登记系统，实名卡可在全市网吧通用并可储值；临时卡由管理员核验身份后登记一次 session。

来源：

- 中国广播网，新浪，2006-11-17：  
  https://news.sina.com.cn/c/2006-11-17/161110529923s.shtml

**证据等级：B+。**

因此对 OWA 的身份研究必须明确至少五层：

```text
person
venue identity record
workstation/session identifier
platform account
public nickname/display identity
```

本轮固定：

## **`access-layer identity / 接入层身份`**

以及：

```text
platform pseudonymity != access-point anonymity
```

这和心理论坛 note 的 `interactional anonymity != archival anonymity` 不是重复概念。

前者问：**当时进入网络的链条上，哪个中间层知道你的现实身份？**  
后者问：**多年后保存和搜索是否扩大了原帖的可识别性？**

一个人完全可以在 BBS 上使用“猫猫123”这样的昵称，同时在网吧前台已经用身份证开启了 24 号机器的 session。

---

## 5. `website account != cybercafe session != local machine state`

为了避免旧网复原把不同 state 混成一个，建议以后对公共终端案例至少拆成：

### 5.1 网站账号状态

- username / UIN / email；
- cookie；
- server-side contacts；
- private messages；
- subscription / paid status。

### 5.2 网吧 session 状态

- venue；
- workstation number；
- login/start time；
- end time；
- payment/balance；
- identity verification mode；
- management software/session token。

### 5.3 本机临时状态

- downloaded files；
- browser history/cache；
- local chat logs；
- installed programs；
- desktop settings；
- input method dictionaries；
- removable-media mounts。

三者的生命周期可能完全不同：

```text
QQ账号：几年
网吧 session：2小时
本地下载：到重启为止
```

因此：

## **`state-lifetime mismatch / 状态寿命错位`**

是研究网吧时代旧 Web 的一个核心问题。

---

## 6. 一个页面“能打开”，不等于网吧用户能完成同样事务

设想一个 2004 年历史站点要求：

```text
下载插件
→ 安装
→ 重启
→ 再打开浏览器
→ 上传文件
```

今天在 VM 里复原这条流程可能完全可行；但当时网吧用户可能遇到：

- 无管理员权限；
- 网管软件禁止安装；
- C 盘被还原；
- 重启后程序消失；
- 网吧限制下载；
- session 到时；
- 换机器后文件不在；
- 没有可用 U 盘或软盘；
- 前台不允许更改机器设置。

于是应增加不等式：

```text
historical page functional in laboratory
!= historical transaction executable from a public terminal
```

这对本仓 M3 浏览环境实验尤其重要：未来不应只做“IE6 vs Chromium”，还可以加入一层**受管共享终端**配置。

---

## 7. 公共终端的“桌面”本身也是考古对象

未来若取得历史网吧截图、硬盘镜像、网管软件、安装介质或用户手册，建议建立以下字段：

```yaml
access_environment:
  venue_type: cybercafe
  observed_at: 2003-xx-xx
  workstation_os: windows_xp?
  browser: ie6?
  installed_im_clients:
    - qq
  installed_download_tools: unknown
  management_software:
    product: unknown
    version: unknown
  billing:
    unit: hourly?
    price: unknown
    shell_visible: unknown
  identity_layer:
    id_required: unknown
    registration_medium: paper/card/software/unknown
  restore_policy:
    local_disk_reset_on_reboot: unknown
    persistent_partition: unknown
  removable_media:
    floppy: unknown
    usb: unknown
  network:
    bandwidth: unknown
    blocked_ports: unknown
  provenance:
    evidence_grade: B
    source: ...
```

重点是保留 `unknown`，不要从“典型网吧”自动补出配置。

---

## 8. 存档机制为什么系统性漏掉这一层

### 8.1 Web archive 偏向远端 HTTP 资源

Wayback 很擅长回答：

```text
这个 URL 某天返回了什么？
```

它天然不回答：

```text
用户当时在哪台公共机器上？
桌面被什么软件控制？
还有几分钟？
硬盘重启后会不会恢复？
```

### 8.2 公共机器会主动消灭痕迹

系统还原对于网吧运营是维护手段，但对于历史研究意味着：

> **一个用户真实做过的本地操作，本来就可能被设计成在下次重启时消失。**

所以这里的“缺失”不是二十年后的档案机构才造成的。有些 local state 在历史现场就被周期性清除。

本轮将其命名为：

## **`designed ephemerality / 被设计出来的短暂性`**

### 8.3 网管软件页面自身也容易消失

17173 2003 产品页仍然在线，但它当时指向的详细说明和购买流程原 URL 今天已不能作为正常页面取得；而产品页又只提供功能摘要。

这是一种：

## **`documentation-depth collapse / 文档深度塌缩`**

顶层宣传页存活，真正能告诉研究者字段、界面和配置流程的深层文档消失。

---

## 9. 与具体旧网页案例相遇时的检查表

如果一个 1998–2012 中文页面有证据显示大量用户可能从网吧进入，不要只记 browser。

至少问：

1. 这个事务只需要 HTTP 页面，还是需要下载/安装？
2. 是否依赖 QQ/ICQ/OICQ、邮件客户端或游戏客户端？
3. 是否要写本地文件？
4. 是否要重启？
5. 是否要求长期 cookie 或证书？
6. 是否需要上传本地照片/简历/附件？
7. 用户能否用软盘/U盘/邮箱附件把文件带进/带出？
8. 网吧系统是否可能限制安装或系统设置？
9. 用户的 session 是否按时间/余额结束？
10. 接入层是否需要身份证或实名卡？
11. 账号昵称和接入实名是否属于不同数据库？
12. 本次 archive 是否只保存网站，没有保存客户端/桌面？

---

## 10. 已证实 / 高概率 / 不知道

### 已证实

- 2002 同期技术文章明确讨论网吧管理软件对用户操作的限制以及硬盘还原程序造成的重启后本地程序消失；
- 2003 17173 同期页面明确宣传网吧管理软件具备客户端记录、计费、计时、程序限制和远程控制能力；
- 2002 制度要求网吧核验登记身份证件并记录上网信息；
- 2006 长沙/合肥同期报道明确出现实名信息与网吧管理/计费软件结合；
- 17173 2003 顶层产品页今天仍在，并保留已失效/未核验的深层原 URL locator。

### 高概率，但本轮不写成事实

- 很多 2000s 网吧桌面可能预装 QQ、游戏客户端、下载工具和输入法；
- 系统还原和受限桌面很可能广泛存在；
- 不同网吧对本地文件、USB 和软件安装的政策差异很大。

这些需要具体站点/网吧/年份 evidence，不能靠集体记忆填充。

### 不知道

- 2003 “冰点网管”对应历史版本的完整 UI、字段和协议；
- 2003 那两个 17173 深层文档的合格 archive capture 是否存在、何时 capture；
- 某具体网吧 2002/2003/2006 的客户端镜像；
- 网管软件、实名系统和公安/文化管理后端之间的具体数据结构；
- 用户下机后本地 state 的清理周期；
- 真实网速、代理/cache、DNS 和端口策略；
- 不同城市实名制度实际执行程度。

---

## 11. 隐私边界

网吧 access log 天然可能包含：

- 身份证信息；
- 姓名；
- workstation number；
- 上下机时间；
- 甚至与访问行为关联的日志。

这些即使未来在某个泄露数据集、旧硬盘或论坛附件里出现，也**不应为了“复原历史”批量重新公开普通个人的身份—访问映射**。

优先保存：

- schema；
- 软件界面；
- 字段名；
- 空白示例；
- 制度说明；
- 聚合数据；
- 已脱敏的技术样本。

这符合 `docs/METHOD.md` 的研究必要最小化。

---

## 12. M1 状态

本轮没有冒充完成 M1。

当前取得：

```text
2002 contemporaneous management/restore behavior article: achieved
2002 contemporaneous policy/access identity layer: achieved
2003 surviving contemporaneous 17173 management-software product page: achieved
2003 deep original-URL locators: achieved
2006 computerized real-name + billing integration descriptions: achieved
```

仍缺：

```text
≥2 verified historical captures of one concrete cybercafe / management interface
capture datetime
historical HTTP / DOM / charset
full management-software UI
second historical timepoint
client OS/browser image or manual sufficient for replay
```

因此准确状态是：

## **`M1 public-terminal access-environment case: NOT ACHIEVED`**

尤其不能把“2003 17173 页面今天仍在线”写成“我们已经复原了 2003 网吧桌面”。

---

## 13. 对 OWA 方法的新增

本轮新增五个可复用机制：

1. **`access-environment state loss`**：网页保存了，公共终端环境没保存；
2. **`billing-shell overlay`**：计时/计费/程序限制层不属于网页 DOM，却决定浏览可执行性；
3. **`access-layer identity`**：网站昵称与场所实名属于不同身份层；
4. **`state-lifetime mismatch`**：网站账号、网吧 session、本地文件具有完全不同的寿命；
5. **`designed ephemerality`**：系统还原主动让历史现场的本地痕迹周期性消失。

因此以后应该把：

```text
page environment
```

扩成：

```text
page + browser + OS + managed-terminal policy + session + identity layer + local persistence
```

才能更接近普通用户真正经历过的旧 Web。

---

## 14. 对 HPL 的回链

HPL companion 将这一技术缺口落回生活史：

- 1996–2002：公共终端让 Internet service access 先于家庭所有权；
- 2008：工地 4–6 台免费电脑、18:00–22:00 的时段把“数字接入”具体变成排队和座位；
- 2018–2019：家庭/手机接入普及以后，公共终端转向高性能和共同娱乐；
- 2026：部分用户再次把昂贵游戏硬件转化为按小时租用。

因此这份 OWA note 不应独立讲“网吧青春”，而应服务一个更窄的考古命题：

> **一个历史网站的真实普通用户，并不一定从一台属于自己的、状态可持久的电脑进入它。**
