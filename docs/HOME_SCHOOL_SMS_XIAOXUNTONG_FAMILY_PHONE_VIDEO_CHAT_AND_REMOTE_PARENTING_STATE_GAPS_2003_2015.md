# 家校通 / 校讯通、亲情电话、视频聊天室与远程育儿状态缺口（2003—2015）

> **Scope note**：本文件不是“留守儿童史”，也不把 `old-web-archaeology` 扩展成一般社会史仓库。研究对象仍限定在约 1995—2015 中文互联网 / 电信—Web 混合环境：家校平台、SMS 网关、学校终端、亲情电话、QQ 视频共享终端、账号与事务状态，以及这些状态为何难以被 Web archive 保存。
>
> 普通生活的长时段解释写在 companion：`tmzncty/how-people-lived/topics/remote-parenting-proxy-care-family-presence-and-distributed-care-china-1993-2026.zh-CN.md`。

## 1. 为什么这个对象属于 old-Web

2000 年代的“家校通 / 校讯通”不是今天意义上的单一手机 App，也不能简单叫“短信通知”。同期材料显示，它们往往是一个混合系统：

```text
学校 PC / Web 管理后台
+ 学生 / 家长记录数据库
+ 卡片 / 校园终端 / 刷卡器
+ 短信网关
+ 固话 / 语音热线 / 12580
+ 家长手机
+ 家长 Web 入口
+ 教育资源页面 / 论坛 / 下载区
+ 有时还有小额支付、学籍、考勤和成绩管理
```

它因此很适合检验本仓 METHOD 的基本要求：**页面、账号、一次数据库事务、短信投递和现实中的孩子不能混成一个对象。**

更重要的是，这类平台保存难度很高：今天可能还能找到公开宣传页、新闻稿和历史域名，却很难取得当年某个学生的一次刷卡事件、某条短信是否真正投递、一次家长登录后的动态页面，或 QQ 视频是否真的接通。

---

## 2. 最小 transaction model

### 2.1 家校消息

```text
student record exists
→ guardian phone/account linked
→ teacher/school creates message
→ platform accepts message
→ SMS/voice job generated
→ carrier accepts job
→ target handset receives
→ correct adult sees/hears it
→ adult understands it
→ adult replies or contacts school
→ local action actually occurs
```

### 2.2 “平安短信” / 到校刷卡

```text
card issued
→ card associated with student record
→ card presented to terminal
→ terminal reads card
→ backend stores event
→ rule generates SMS
→ carrier routes SMS
→ guardian handset receives
→ guardian reads
```

任何一段都不能被历史研究者压成一个布尔字段 `student_safe=true`。

### 2.3 共享视频“亲情聊天室”

```text
public/school PC exists
→ child has permission/time to use it
→ Internet route works
→ IM/video software available
→ account credentials available
→ migrant parent has a compatible terminal/account
→ both sides online at same time
→ call connects
→ audio/video usable
→ conversation actually happens
```

因此 `家庭没有电脑` 与 `孩子完全不能视频联系父母` 不是等价命题。

---

## 3. 2003—2006：Web、SMS、语音和实体终端一开始就是编织在一起的

### 3.1 泉州“家校亲情卡”：13 万学生不是 13 万家庭 Web 用户

2005 年 10 月的同期报道记录，泉州已有 300 多所学校、13 万名学生使用“家校亲情卡”。系统可以发送停课通知，学生使用亲情卡，教师可通过承载系统发送通知、成绩和评语，家长/学生还能用账号接入教育资源。

来源：中国教育和科研计算机网，2005-10-14：
https://cernet.edu.cn/xxh/fei/xin_xi_zi_xun/200603/t20060323_144201.shtml

证据等级：**B，同期教育信息化报道。**

关键研究约束：

- `13 万学生在用卡` 不能直接写成 `13 万家庭使用 Web`；
- “家长可以随时掌握”是功能描述，不是每条消息的 delivery proof；
- 教师“可上网实时查询考勤”证明 Web 后台存在某类查询能力，但本轮没有取得原始后台页面。

### 3.2 福建“家校通”：运营商正式材料证明系统边界比 SMS 更大

中国移动 2006 年企业社会责任报告把“家校通”功能列为签到、报平安、亲情通话、家校互联和小额支付；福建业务自 2004 年 1 月启用后，短信报平安注册客户 20 万，家校互联 4 万多。

来源：中国移动 2006 企业社会责任报告：
https://www.chinamobile.com/aboutus/res/2006cr_cn/P040102.shtml

证据等级：**A，运营商同时代正式材料。**

这里必须保留 `registered / active-used gap`：注册数不是活跃使用数。

### 3.3 中山“家长留言板”：电话输入，PC 管理，电子屏输出

2005 年 12 月，中山移动开通“家长留言板”：家长拨 12580 留言，内容显示在学校出入口电子屏；学校公布栏由学校通过 PC 输入。

来源：中国教育和科研计算机网，2006-03-29：
https://www.edu.cn/chanpin_xinxi_1709/20060329/t20060329_170194.shtml

证据等级：**B，同期行业报道。**

这是一个很重要的反例：

> **digital service ≠ Web browser service。**

普通家长可以只用电话进入一套背后包含 PC 和数据库的数字系统。

---

## 4. 必须长期保留的 state gaps

### 4.1 student record / actual child gap

数据库中的学生记录可以对应真实儿童，但记录字段、更新时点和现实状态不能自动相等。

### 4.2 guardian contact / actual caregiver gap

平台绑定号码的“家长”可能是父亲、母亲或其他监护联系人；实际每天与孩子同住的人又可能是祖父母或其他亲友。

所以：

```text
platform guardian number
≠ legal guardian
≠ co-resident caregiver
≠ person the child will actually ask for help
```

### 4.3 card assigned / card carried gap

系统里卡已绑定某学生，不证明某天卡实际由该学生携带。

### 4.4 swipe / bodily-presence gap

刷卡只能首先证明 **某张卡在某终端发生了一次事件**。在没有额外证据时，不应把它扩大成“这个孩子整天都安全在校”。

这不是在断言普遍存在代刷，而是一个认识论边界：事务事件与人的完整身体状态不同。

### 4.5 queued / carrier-accepted / delivered / read gap

短信系统至少有：

```text
platform generated
→ gateway queued
→ carrier accepted
→ handset delivered
→ human read
```

今天保存一张“发送成功”的后台截图，也未必说明家长看见了。

### 4.6 read / interpreted / acted gap

即使家长读到“孩子未到校”，仍然需要判断原因、联系学校/本地照护者，并有人完成线下行动。

### 4.7 remote-informed / local-action gap

这是与普通生活史最重要的接口：外出父母可以迅速知道事情，却未必能从几百公里外亲自处理。

### 4.8 home-PC ownership / service-access gap

学校、村微机室、农民工公寓和公共“亲情视频聊天室”可以成为共享终端。因此 household PC ownership 不能作为 Internet 家庭联系的唯一代理变量。

### 4.9 video-connected / meaningful-conversation gap

视频连接成功只能证明媒体通道建立，不证明孩子愿意表达真实问题，也不能证明外出父母能够提供本地照护。

### 4.10 live-service / archived-page gap

公开页面最容易被保存；最关键的实时状态往往来自：

- 登录后的学生记录；
- SMS gateway；
- card terminal；
- carrier delivery report；
- dynamic attendance table；
- private QQ / IM conversation；
- local school database。

这些恰恰最难进入公共 Web archive。

---

## 5. 2009：规模化以后，平台也不能被写成一个全国统一产品

中国移动 2009 年企业社会责任报告称，截至 2009 年 9 月，“校讯通”服务 2,623 万用户，覆盖 67,097 所各类学校；城镇中小学学校覆盖率 30.95%。技术入口包括手机终端、校园信息机和个人电脑，使用短信、语音和 Internet，并提供考勤、学籍、亲情电话和教育网站等能力。

来源：中国移动 2009 企业社会责任报告：
https://www.10086.cn/aboutus/res/2009csr_cn/09/090206.shtml

证据等级：**A，运营商正式材料。**

但这组数字不能被写成：

> 2009 年全国学校都在使用同一个 `xiaoxuntong.com` 式网站。

现实更可能是省级公司、地方教育部门、合作厂商和不同版本并存。产品品牌相同，不证明 host、数据库、登录方式、页面结构和服务合同相同。

因此新增：

> **brand / implementation gap / 品牌—实现缺口。**

后续做站点级考古时，必须先固定城市/省份/运营商/年份，不能以“校讯通”品牌名替代具体技术对象。

---

## 6. 历史 locator：`xxt.cn` 只能被定位到具体时期，不能向前无限回填

本轮找到的较可靠 locator 是河南校讯通的 `www.xxt.cn`。

2013 年一份高校来源的招聘公告转载明确称，河南校信通教育科技有限公司主营“校讯通家校沟通信息平台（www.xxt.cn）”。

来源：2013-12-17 招聘公告存留：
https://www.ynpxrz.com/n495187c1277.aspx

证据等级：**B，2013 年同期招聘/机构介绍。**

后来的 WHOIS 汇总还显示 `xxt.cn` 注册时间为 2005-04-02，但这是现代第三方数据库结果，只能作为 locator 辅助，不能证明 2005 年当天就已经运行同一平台或拥有 2013 年页面结构。

来源（D/辅助定位）：
https://webrate.org/site/xxt.cn/

因此允许的 claim 是：

> **2013 年已有同时代材料把 `www.xxt.cn` 指认为河南校讯通家校沟通信息平台。**

不允许的 claim 是：

> **2005—2015 全国“校讯通”的网址就是 `xxt.cn`。**

广东 2014 年用户社区材料则把 `edu.gd.chinamobile.com` 指向广东移动“校讯通”详情页，进一步说明同品牌存在地方 host。

来源：广州妈妈网，2014：
https://www.gzmama.com/thread-4040446-1-1.html

证据等级：**B/C，2014 用户社区里的同期产品活动帖，可作 locator，不足以替代官方页面 capture。**

---

## 7. 2010—2012：共享视频终端揭示“网页可及”和“家庭拥有电脑”之间的差异

2010 年新华社报道，重庆计划为留守儿童及家长开设 2,000 个“亲情视频聊天室”、安装 5,000 部“亲情电话”；终端布置在农村学校和主城区农民工公寓，使两端可以免费进行视频联系。

来源：新华社，2010-09-22（搜狐存留）：
https://news.sohu.com/20100922/n275206482.shtml

证据等级：**B。计划数不能当完成数。**

2012 年教育部转载《光明日报》材料记录，贵州修文县村级免费“绿色网吧”供 60 多名留守儿童使用，孩子通过 QQ 视频与外出父母联系；报道同时指出当地家庭计算机普及有限。

来源：教育部，2012-06-25：
https://www.moe.gov.cn/jyb_xwfb/s5148/201206/t20120625_138217.html

证据等级：**B。**

对 old-Web 考古而言，这要求我们扩大“访问环境”字段：

- 家庭 PC；
- 网吧；
- 学校微机室；
- 村公共电脑；
- 农民工公寓终端；
- 单位电脑；
- 手机；
- 亲友代操作。

一个页面的典型用户不一定坐在自己的卧室里。

---

## 8. 从短信遥测到摄像头：2015 后的连续性边界

2015 是本仓主 scope 的上缘，因此这里只记录边界，不把研究扩成智能家居史。

到 2018 年，媒体已经出现外出父母在老家安装摄像头、通过语音与画面“陪”孩子和祖父母的案例。

来源：中国青年报，2018-04-17（人民网）：
https://gongyi.people.com.cn/n1/2018/0417/c151132-29930199.html

这与 2000s 家校通有一个结构连续性：

```text
早期：学校把离散事件（到校 / 成绩 / 通知）推给远程家长
后来：家庭摄像头把家庭空间本身变成持续可观察对象
```

但 old-Web 只需记录这条边界，不继续展开 2018 以后平台史。

---

## 9. “connected ≠ emotionally informed”：事务系统不能替代关系研究

中国农业大学 2006—2008 年调查的同期报道显示，打电话已是留守儿童与外出父母维系关系的主要方式；95.4% 的外出父母通话时会询问学习，但报道同时指出情感交流不足。另有 61.5% 的儿童不愿向父母诉说烦恼。

来源：中国青年报 2009-01-06，央视网存留：
https://news.cctv.com/china/20090106/102098.shtml

证据等级：**B。**

这对于 old-Web 有一个重要方法提醒：

> `messages sent per month`、`login count`、`call connected` 等日志，是关系的 transaction trace，不是关系质量本身。

平台日志适合证明通信动作，不能单独证明“亲情改善”“教育效果提高”或“监护问题解决”。运营商宣传里出现这类效果措辞时，只能写“平台当时这样宣称”。

---

## 10. 海外比较只放在 companion，不改仓库 scope

菲律宾跨国家庭从书信、盒式录音带到移动电话的研究说明，远程育儿并非中文互联网独有；移动通信让迁移母亲更容易参与孩子生活，但孩子对远程父母角色的体验可能更复杂。

参考：
- https://journals.sagepub.com/doi/10.5367/sear.2011.0043
- https://journals.sagepub.com/doi/10.1177/1461444810393903

这些海外材料用于 `how-people-lived` 比较，不纳入本仓平台谱系样本。

---

## 11. Archive / browser / protocol gap

### M1 status

**NOT ACHIEVED IN THIS SLICE.**

本轮已经得到：

- 2005 泉州家校亲情卡的同期功能描述；
- 2006 中国移动正式 CSR；
- 2009 中国移动正式 CSR 与规模数据；
- 2013 `www.xxt.cn` 同期 locator；
- 2014 广东移动 `edu.gd.chinamobile.com` locator；
- 2010—2012 公共视频终端的同期材料。

但本轮**没有实际取得并逐项检查一份满足 `docs/METHOD.md` 合同的 2003—2015 Wayback/WARC replay**。

尝试直接访问 Wayback CDX 的历史查询 URL 时，当前 Web 访问工具的安全限制阻止了直接打开；普通搜索也没有返回可验证的 capture。这个结果只能写成：

> **本轮未验证历史 capture。**

不能写成：

> **Wayback 没保存。**

仍未知：

- 原始 HTTP headers；
- charset（GB2312 / GBK / UTF-8 的具体时点）；
- 原始 DOM / frameset / table layout；
- IE-only / ActiveX / Java / Flash 条件；
- login/session/cookie 方案；
- parent/student account 的 URL pattern；
- SMS gateway 与 Web backend 的接口；
- card reader 协议和上传重试逻辑；
- carrier delivery report 是否回写平台；
- dynamic attendance / grade pages 是否被 archive 捕获；
- 历史站点的登出、失败、停机和欠费页面；
- `xxt.cn` 2005—2013 精确的 host / 主体 / 页面变迁。

### Candidate next capture work

以后 M1/M4 可优先查：

1. `www.xxt.cn` 2005—2015 的 exact capture timeline；
2. `edu.gd.chinamobile.com` 2010—2015；
3. 泉州电信“家校亲情卡 / 家校通”同期官方 host；
4. 地方教育局 / 学校帮助页里保存的登录 URL、截图和客户端要求；
5. 同期用户教程是否保存了登录、成绩、考勤和短信设置页面；
6. 手机运营商套餐、退订和跨网限制。

---

## 12. 隐私与未成年人边界

这一类 old-Web 对象比普通门户站更敏感，因为原始数据可能包含：

- 未成年人姓名；
- 学号 / 学籍；
- 家长手机号；
- 到离校时间；
- 成绩和教师评语；
- 家庭关系；
- 私人留言；
- 照片和视频。

即使未来 archive 技术上能够取得登录后缓存、旧截图或泄露数据库，也不应为了“考古完整”重新公开普通儿童的个人记录。

研究优先级应是：

1. 保存公开产品帮助页、字段 schema 和页面结构；
2. 保存 URL / capture metadata；
3. 对私人数据只记录支持 claim 所需的最少抽象；
4. 优先使用官方 demo、媒体截图、空白表单和公开教程；
5. 不批量重发儿童姓名、号码、成绩、出勤和家庭留言。

---

## 13. 本轮新增的 old-Web 结论

此前可以把家校系统理解为“学校给家长发短信”。

现在更准确的是：

> **它是一套把孩子的一小部分线下生活转换成数据库事件，再通过 SMS、电话、Web 和共享终端传给远程成年人的事务系统。**

这改变了历史可见性：

- 过去学校门口等孩子、家长会和老师口头转述很难留下机器记录；
- 2000s 以后，到校刷卡、成绩、通知和家长号码越来越容易形成 transaction trace；
- 可是一次“短信发送成功”仍然无法告诉未来研究者家长有没有看到，更无法告诉我们远在城市的父亲知道孩子没到校以后，最后是谁骑车去找他。

因此这类系统最值得保存的不是一句“信息化促进家校沟通”，而是那一长串中间状态：

```text
observed
→ encoded
→ stored
→ routed
→ delivered
→ read
→ interpreted
→ acted upon
```

旧网考古真正要做的，是阻止后来的研究者把这八个状态重新压回一个绿色的“成功”按钮。