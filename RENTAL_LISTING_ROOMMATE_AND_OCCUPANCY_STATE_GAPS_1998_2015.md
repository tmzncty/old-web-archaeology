# RENTAL LISTING / ROOMMATE / OCCUPANCY STATE GAPS, 1998–2015

Status: research note / state-gap model  
Scope: 约 1998–2015 中文 Web 中住房租赁 listing、分类信息、房源搜索、房东/中介身份、合租/找室友、看房、occupancy 与 archive blind spots；**不把本仓扩展成中国住房史或 2015 年后的租房 App 史**。  
Cross-repo companion: `tmzncty/how-people-lived/topics/from-rental-listings-to-stranger-households-renting-roommates-and-household-assembly-china-1980-2026.zh-CN.md`  
Last research pass: 2026-09-05

---

## 0. Why rental listings are a special old-Web object

租房页面看上去非常“事实化”：

```text
三室一厅
面积 90㎡
月租 1800
某区某路
联系电话
```

它甚至比博客和论坛更容易给研究者一种错觉：既然字段这么具体，我们似乎已经知道历史上的真实住房状态。

实际上，一条 rental listing 背后至少有：

```text
dwelling exists
→ poster has authority to offer it
→ listing created
→ listing admitted to platform
→ listing becomes searchable
→ ranking/paid position
→ user query matches
→ result displayed
→ user notices/clicks
→ contact endpoint works
→ poster responds
→ unit is still vacant
→ quoted price is still valid
→ photos/description match current dwelling
→ viewing happens
→ viewer accepts
→ deposit/payment
→ contract is valid
→ move-in
→ actual roommate/occupancy state
→ landlord does not alter partition/occupancy
→ utilities and shared space work
→ tenancy persists
→ move-out
→ deposit/contract/loan states close
```

公共 Web archive 最容易保存的是：

- listing HTML；
- 标题、价格、面积、地点；
- search form；
- 城市/区域/category 页面；
- 联系方式字符串；
- 帮助页和平台宣传；
- 某些照片；
- 某个页面当时的 capture。

最难保存的是：

- 那一刻房子是否已经租掉；
- 发布者是否真有出租权；
- 价格是不是引流价；
- 同一套房是否重复发布；
- 联系后说了什么；
- 谁实际看了房；
- 谁付了押金；
- 最终住了几个人；
- 房东是否后来加隔断/加床；
- 室友实际身份、作息和相处结果；
- 押金是否退回；
- 租金贷/二房东等后台合同是否关闭。

因此本 note 的核心命题是：

> **listing state survives much better than occupancy state.**

保存了一条“房屋出租”并不等于保存了一段真实居住史。

---

## 1. Evidence contract

遵循 `docs/METHOD.md`。

### 1.1 Research units

至少分别记录：

- `platform`
- `host`
- `city_portal`
- `category`
- `search_form`
- `query`
- `result_page`
- `listing`
- `listing_revision`
- `dwelling`
- `room_or_bed`
- `poster_account`
- `claimed_poster_role`
- `actual_authority_to_lease`
- `contact_endpoint`
- `photo_asset`
- `price_state`
- `availability_state`
- `roommate_request`
- `viewing`
- `deposit_or_payment`
- `contract`
- `occupancy_state`
- `move_out_state`
- `capture`
- `claim`

不得把：

```text
“2008-08-18 某网站仍显示一条月租 900 元的房源”
```

直接写成：

```text
“2008-08-18 这套房可按 900 元租到。”
```

### 1.2 Evidence grades used here

- **A**：verified historical capture/WARC、同期平台 help/产品/技术文档、SEC/监管文件；
- **B**：同期媒体实测、用户操作/投诉、论坛/教程；
- **C**：后来平台史、回忆、现代镜像；
- **D**：根据 URL、截图、后续页面推断历史 DOM/状态。

### 1.3 Privacy boundary

租房页可能同时包含：

- 真实姓名；
- 手机/固定电话；
- QQ/MSN/email；
- 精确住址；
- 性别/年龄/职业；
- 室友偏好；
- 作息；
- 住房内部照片。

对普通个人：

1. 不批量重发历史电话号码；
2. 不用今天仍有效的电话去“验证历史房东”；
3. 不根据精确房号+姓名重新识别历史普通租客；
4. 不把已删除的找室友帖因“研究价值”批量复原公开；
5. 结构研究优先保存字段、URL pattern、匿名化示例和 aggregate state。

电话号码会二次放号，房屋会换业主，域名也会换主体。

---

## 2. Physical noticeboard and Web can coexist; do not invent a clean replacement date

2007 年 CCTV/媒体报道配发的同期图片说明，北京某大学校园公告栏仍贴满房屋出租和求租信息。

Source:
- https://news.cctv.com/education/20070716/106193.shtml

Evidence:
- **B+**：同期图文；证明 2007 实体公告栏仍是信息接口，不证明该形态从哪一年开始或全国普及率。

因此不能写：

```text
1998 前：纸
1998 后：Web
```

更合理的是长期 channel portfolio：

```text
friends / classmates / coworkers
+ newspaper/classified
+ physical board / pasted note
+ brokerage storefront
+ campus/work-unit information
+ BBS/forum
+ classified website
+ vertical property portal
+ IM/group
```

用户可以在网上发现房源，再打电话；也可以在校园公告栏看到号码，再用 QQ 继续联系。

对于 old-Web 考古，这意味着一个 online listing 不是完整渠道史，只是一次 contact chain 的一个节点。

---

## 3. Rental page requires three separate clocks: page time, inventory time, occupancy time

增加：

## **listing-time / inventory-time gap**

至少保存：

```text
listing_created_at
listing_updated_at
capture_datetime
claimed_available_from
last_known_vacant_at
contacted_at
rented_at (often unknown)
```

历史 capture 的时间是 archive 保存页面的时间；listing 页面显示的“发布时间”可能是：

- 首次创建；
- 最后刷新；
- 经纪人重新顶帖；
- 平台批量迁移数据时重写；
- 模板生成的相对时间。

不能默认：

```text
capture 2009-06-03
→ unit vacant on 2009-06-03
```

甚至 listing 页面仍在线，也可能只是“已成交后未及时下线”的 stale inventory。

### 3.1 Listing refresh can erase original chronology

若平台允许经纪每日刷新/重发，则：

```text
same dwelling
→ many listing IDs
```

或者：

```text
same listing ID
→ latest timestamp replaces earlier market state
```

因此 old-Web 研究不能只把 URL count 当独立房源 count。

---

## 4. One listing is not one dwelling

增加：

## **listing / dwelling multiplicity gap**

可能存在：

```text
1 dwelling → N agents → N listings
1 dwelling → N prices → N listings
1 dwelling → whole-apartment listing + room listings + bed listings
1 agent → copied listing across N portals
N old listings → same later renovated dwelling
```

也可能：

```text
1 listing → no real dwelling
```

因为它可能是：

- 已租掉的旧房源；
- 假价格引流；
- 假地址；
- 复制别人的照片；
- 经纪虚构；
- 同一套房重复发布；
- “先用漂亮房源引来，再推荐别的房”。

历史页面里最精确的数值，反而可能是商业策略生成的字段，而不是现实市场事实。

---

## 5. SouFun 2010 F-1: a strong A-level proof that online inventory was already ranked, commercial and imperfect

SouFun Holdings 2010 年向 SEC 提交的 F-1 是本专题的核心 A 级来源。

Source:
- SouFun Holdings Limited, Form F-1, filed 2010-09-02：
  https://www.sec.gov/Archives/edgar/data/1294404/000095012310083390/h04135fv1.htm

同期文件明确描述：

- 截至 2010-06-30，数据库约有 **800 万条 secondary and rental residential property listings**；
- 房地产内容/搜索/营销/listing 覆盖 106 个中国城市；
- 用户可以按城市、区域、地铁附近、价格、房型、房间数、面积筛选；
- 页面返回 location、price、room count 和 listing source 等字段。

Evidence:
- **A**：同期监管文件。

注意：

> 800 万是 listing 记录，不是 800 万套独立、同时空置、价格真实的房屋。

### 5.1 Searchable inventory exists ≠ complete market exists

增加：

## **platform-inventory coverage gap**

SouFun 自身都按城市分阶段扩展 full suite；106 城“有内容/搜索/营销/listing coverage”不等于 106 城都具有同样深度、同样房源质量或同样用户习惯。

所以：

```text
platform covers city
≠ all local rental supply indexed
≠ all landlord types represented
≠ informal rooms/bedspaces represented
```

### 5.2 Individual-owner listing and professional listing are not the same visibility class

同一 F-1 说明个人业主可免费发布，但这些免费 listings **do not enjoy prime positioning**；free-trial accounts 也比付费订阅获得更不显著的 position/ranking。

增加：

## **paid-position / landlord-type visibility gap**

一名历史用户看到的 SERP/listing order 可能由：

```text
query relevance
+ commercial subscription
+ poster type
+ refresh state
+ local inventory
```

共同决定。

因此不能从今天保存下来的某个 listing 推断“当年普通用户很容易看到它”。

### 5.3 Platform itself recorded false price, false unit and role impersonation

同一 F-1 明确写道，listing monitoring team 会遇到：

- real-estate agent/broker 冒充 individual property owner；
- false properties for sale or rent；
- false sale/rental prices；
- duplicate listings。

文件也明确承认无法验证所有上传信息，只能定期检查 anomalies，并在发现虚假信息后要求整改或移入用户不可访问数据库。

增加：

## **claimed-poster-role / actual-role gap**

```text
页面写“个人房东”
≠ 真是个人房东
```

以及：

## **platform-visible / platform-verified gap**

```text
listing admitted to site
≠ platform verified truth
```

这些不是后来的“租房平台变坏”回忆，而是 2010 年平台自己的同期正式申报已经明确记录的结构问题。

---

## 6. Search fields survive better than market semantics

2010 F-1 能确认 SouFun 当时允许按：

```text
city
district/area
near subway line
price range
property type
number of rooms
size
```

筛选。

但如果未来找到一个 2008/2010 search form capture，仍须区分：

- label text；
- input/select value；
- submitted parameter；
- backend interpretation；
- result corpus；
- default sort；
- paid layer。

增加：

## **filter-label / filter-semantics gap**

一个下拉框写“个人房源”不能自动证明后台只返回真正个人房东；2010 F-1 的 role impersonation 反而说明这种 label 与现实身份之间可能断裂。

同理：

```text
“近地铁”
```

究竟是：

- 平台人工标注；
- 地图距离；
- 经纪自填；
- 某条线路附近行政片区；

必须以同期技术/帮助页确认。

---

## 7. Contact string survives ≠ negotiation survives

增加：

## **contact-endpoint / transaction-dialogue gap**

listing 可能保存：

```text
phone
QQ
MSN
email
platform message
```

但 archive 几乎从不保存：

```text
“这套没了，还有另一套”
“价格其实是 2300”
“先交看房费”
“必须半年付”
“只租女生”
“室友已经换了”
```

所以页面字段只是 advertised state。

不能把历史 listing 上的：

```text
1800/月
```

写成 historical transaction price，除非另有合同、入住者记录或可靠交易数据。

### 7.1 Do not call old phone numbers

旧电话号码可能已经：

- 停机；
- 二次放号；
- 转给新业主/新公司；
- 因号码升位发生变化。

为了“验证 2006 listing”，今天拨号会把历史研究变成对无关现代个人的打扰，而且无法可靠反推历史主体。

---

## 8. Roommate listing is a different object from property listing

“整套房出租”和“找一个人一起住”不是同一层对象。

增加研究单位：

```text
roommate_request
existing_leaseholder
available_room_or_bed
co-renter_wanted
sublease_wanted
roommate_profile
house_rules
```

2008 年海口媒体检查当地网站租屋信息，记录用户公开在网上招募陌生合租者。报道聚焦“异性合租”，存在明显新闻猎奇偏差；本仓只用它证明 **public Web roommate recruitment existed**，不采信其小样本调查为人口代表性结论。

Source:
- 南海网转载于新浪，2008-08-18：
  https://news.sina.com.cn/o/2008-08-18/150914325967s.shtml

Evidence:
- **B**：同期媒体。

### 8.1 roommate profile field ≠ compatibility

增加：

## **profile / co-residence compatibility gap**

历史找室友帖常可能写：

```text
sex/age
job/student
smoking
cleanliness
schedule
long/short stay
pets
budget
```

这些只能证明发布者声明了筛选条件。

不能推断：

- 对方真实满足；
- 实际见过；
- 入住；
- 同住愉快；
- 无安全问题。

### 8.2 Member count / reply count ≠ household assembled

论坛/BBS/分类信息若保存 reply：

```text
“有意”
“已私信”
“加QQ”
```

仍然不等于最终合租。

增加：

## **reply / roommate-outcome gap**

真正 outcome 往往在：

- 电话；
- QQ/MSN；
- 私信；
- 线下看房；
- 合同；

中发生，公共 Web 看不到。

---

## 9. Viewing is not a stable snapshot of occupancy

2008 年扬子晚报记录大学生吴冉看过一套合租房、交定金后，入住时发现房东又把大房间和客厅调整/增加居住人数，最后六人共同使用卫生间。

Source:
- https://news.sina.com.cn/c/2008-08-11/035214293436s.shtml

Evidence:
- **B+**：同期投诉与媒体采访。

增加：

## **viewing-state / move-in-state gap**

```text
viewing at t1
≠ physical layout at t2
≠ occupancy at t2
```

住房和一般商品不同：

- partition 可加；
- 床位可加；
- 室友可换；
- 房东可住入；
- 水电/家具可被搬走；
- 周边施工/噪声可变化。

因此即便 archive 能保存 t1 的真实照片，也不能把它当整个租期的状态。

---

## 10. Image survival is particularly deceptive in rental archaeology

增加：

## **photo-time / dwelling-time gap**

一组 2009 listing photos 可能：

- 是更早拍摄；
- 拍摄于上一任租客入住前；
- 来自同小区样板房；
- 被多个 listing 复制；
- 只拍好看的角度；
- 不包含窗外、楼道、卫生间、隔断；
- archive 丢失 EXIF/原始 filename。

若图片子资源保存，应记录：

```text
image_url
capture_datetime
claimed listing association
image dimensions
archive rewrite
whether same hash appears in other listings
```

如果同一图片 hash 出现在多个地址/房型 listing，这本身可能成为 duplication/stock-photo 证据，但不能自动判断哪一条真实。

---

## 11. Rental price needs advertised / negotiated / paid separation

增加三个字段：

```text
advertised_rent
negotiated_rent
paid_rent
```

再加：

```text
deposit
agency_fee
utilities
property_fee
internet_fee
payment_frequency
loan_or_installment_state
```

一个页面写：

```text
1500 元/月
```

不能自动计算普通人月住房成本。

2008–2010s 市场还可能出现：

- 押一付三；
- 中介费；
- 短租加价；
- 房间/床位与整套不同计价；
- 后来的租金贷。

若 archive 只保存 headline price，历史研究应明确写成 **advertised rent**。

---

## 12. Whole apartment / room / bed are different inventory units

增加：

## **rental-unit granularity gap**

一个物理 apartment 可以被市场表示为：

```text
whole unit
→ bedroom A
→ bedroom B
→ partitioned room C
→ bed 1 / bed 2 / bed 3
```

因此：

```text
number_of_listings
```

必须先知道 listing unit 是：

- dwelling；
- room；
- bed；
- roommate vacancy。

否则跨时期比较会把“房源变多”与“同一住房被切成更小付费单元”混在一起。

这对 2000s–2010s 群租/床位房尤其重要。

---

## 13. Search result is a temporary market surface, not the market itself

一条历史 SERP 需要记录：

```text
query
city
filters
sort order
page number
capture datetime
visible listing IDs
paid/sponsored markings
pagination
```

增加：

## **SERP / local-market gap**

同一天：

```text
platform A results
≠ platform B results
≠ broker storefront inventory
≠ campus board
≠ private QQ group
≠ landlord word-of-mouth inventory
```

历史研究若只保存一个大型平台，会系统性漏掉：

- 不会发布网络广告的老年房东；
- 小区内部转租；
- 学校/单位内部资源；
- 低价床位和非正规出租；
- 熟人转介绍；
- 已经从公开 Web 转进 IM 群的房源。

---

## 14. 2019–2021 evidence confirms the long-running page/reality gap, but stays outside this repo's primary scope

本仓 scope 以约 2015 为主。后来的材料只作为验证状态模型是否具有解释力的外部 check，不扩成 2020s 平台研究。

2019《中国青年报》调查/采访仍记录“房屋信息与宣传不符”、室友冲突等问题；2021 同类调查仍记录大量受访者认为虚假房源多。

Sources:
- 2019-06-28：
  https://news.cctv.com/2019/06/28/ARTInCmd8pYKTb6YTXRnfivZ190628.shtml
- 2021-08-12：
  https://zqb.cyol.com/html/2021-08/12/nw.D110000zgqnb_20210812_3-10.htm

Evidence:
- **B**：later boundary evidence only。

它们不证明 2005 的具体假房源比例，但支持这样一个方法判断：

> listing-to-dwelling state gap 不是只在某一年短暂存在，因此历史 capture 更不能被直接当“现实库存快照”。

---

## 15. Archive-specific gaps

### 15.1 login / private-message gap

找室友和租房沟通很容易转进：

```text
platform PM
QQ
MSN
email
phone
```

public crawler 无法保存后续。

### 15.2 dynamic search gap

历史租房搜索可能依赖：

- GET/POST query；
- session；
- JS；
- city cookie；
- dynamically generated result IDs；
- backend database no longer available。

一个 search form capture 存在，不等于历史 query 可重放。

### 15.3 pagination gap

archive 可能只保存第一页。

因此不能从：

```text
page 1 has 20 listings
```

推算完整市场或 category 总量，除非历史页面明确给出可信 total 并解释计算方式。

### 15.4 contact redaction / rewrite gap

平台可能今天对旧页：

- 隐藏号码；
- 替换成虚拟号；
- 要求登录；
- 删除 QQ/email；
- 把号码改成图片；

当前 live 页面不是历史 contact state。

### 15.5 deleted-after-rented gap

如果平台在租出后自动删除/隐藏 listing，则成功成交的房源反而可能比无人问津的 stale page 更难被长期抓到。

增加：

## **successful-delisting bias——成功下架偏差**

这和 dating site 的 “successful disappearance bias” 类似，但机制不同：

- dating：成功关系可能离开平台；
- rental：成功出租可能直接让 listing 消失。

因此 archive 中长期幸存的 listing 可能偏向：

- stale；
- 无人租；
- 模板页；
- 被平台长期保留的 SEO 页面。

### 15.6 occupancy outcome darkness

最终最重要的状态：

```text
who actually lived there?
for how long?
under what contract?
with whom?
why did they leave?
```

通常完全不在 public Web。

本 note 称为：

## **occupancy-outcome darkness——入住结果黑区**

---

## 16. Overseas comparator: Craigslist shows the same general mechanism, not a uniquely Chinese one

本仓不扩展为全球旧网仓库；以下仅用于比较结构。

Craigslist 当前保存的同期/近同时代媒体资料显示：

- 1995 起源于旧金山本地 mailing list/community bulletin board；
- 2000 同期报道已提到 apartments for rent；
- 2001 同期报道把 jobs、items、rooms for rent 列为核心 bulletin-board postings；
- 2002 个案有人通过同一平台找到 apartment、roommate、job 等生活资源。

Sources:
- https://www.craigslist.org/about/press/craigsonlinelistofstuff
- https://www.craigslist.org/about/press/dotorgssurviving
- https://www.craigslist.org/about/press/esquire
- https://www.craigslist.org/about/expansion

Evidence:
- **B+**：同期媒体现由 Craigslist 重托管，不是 verified original Web captures。

比较意义：

> **把本地住房和陌生室友放进可更新的 online classified corpus，是跨国 Web 时代的共同机制。**

中国更需要单独研究的，是它与：

- 快速住房制度转型；
- 大规模高校毕业生迁城；
- 城中村/群租/单位宿舍；
- QQ/电话等站外闭环；
- 房地产 vertical portals 与经纪商业排序

怎样叠加。

### 16.1 pre-Web overseas check: stranger roommate matching predates the Web

UNT Digital Library 的 1984 *Dallas Voice* 原版 classified page 已有 `DWELLINGS & ROOMMATES` 类目。

Source:
- https://digital.library.unt.edu/ark:/67531/metapth615777/m1/19/

Evidence:
- **A**：同期报纸原页。

因此：

```text
stranger roommate discovery
```

不能定义成 Web 原生行为。Web 的转折更可能是：

```text
posting latency ↓
searchability ↑
listing refresh rate ↑
geographic reach ↑
number of candidates ↑
platform-mediated ranking ↑
```

同时 fraud/identity/duplication state 也进入平台数据库层。

---

## 17. Minimum state model for one rental-history claim

如果未来要声称：

> “2009 年某毕业生可以通过某中文房产网站按地铁线找到一间 1500 元/月的合租房并入住。”

至少需要分别证明：

```text
A. platform / interface
1. host 在 2009 存在
2. historical capture 可定位
3. city portal 存在
4. search/filter 可用
5. subway criterion 的语义可确认

B. listing
6. listing 在目标时点存在
7. listing 的发布时间/更新时间可区分
8. 1500 是 advertised rent
9. listing unit 是 whole/room/bed/roommate vacancy
10. source/poster role 可观察

C. real dwelling
11. 地址/小区对应真实住房
12. 房源当时仍可租
13. 照片/面积/房型未被证明是复制或错误

D. human transaction
14. 用户实际看到 listing
15. 联系成功
16. 实际看房或可信代理看房
17. negotiated terms 可知
18. contract/payment 成立
19. move-in 可确认

E. occupancy
20. 实际室友人数/关系可知
21. 入住后 layout 未立即改变，或变化有记录
22. 租住持续时间可知
23. move-out 与 deposit closure 可知
```

绝大多数 archive-only 研究只能覆盖 1–10 的一部分。

这不是失败，而是 evidence boundary。

---

## 18. Verified / probable / unknown in this pass

### 已证实

- 2007 中国高校环境仍存在实体出租/求租公告栏；
- 2008 同期中文媒体记录公开 Web 找陌生室友；
- 2008 同期个案证明看房后的 occupancy/layout 可以在入住前被房东改变；
- SouFun 2010 F-1 证明其拥有大规模二手/租赁 listing 数据库、按多字段搜索、商业排序/prime positioning，并明确记录虚假出租、虚假价格、重复 listing 和经纪冒充个人房东；
- 海外纸质 classified 在 1984 已有 roommate 类目，Web 没有发明陌生合住；
- Craigslist 2000–2002 同期媒体已经把 housing/rooms 与其他城市生活分类信息放在同一 online community infrastructure 中。

### 高概率但本轮不升格

- 1998–2005 中文租房 Web 已经经历从门户/分类信息到更结构化 vertical search 的持续变化；
- QQ/电话很可能承担大量 listing 之后的实际谈判；
- 许多“已出租”状态没有进入公共 archive。

这些需要 verified captures / help pages / user instructions 才能继续收紧。

### 不知道

- 1998–2001 主要中文租房站点的原始 DOM、charset、form method/action；
- 某个 2000s query 在具体 datetime 的真实 result ranking；
- paid position 与自然 relevance 在历史 SERP 上怎样视觉区分；
- 个人房源字段后台如何验证身份；
- 页面价格与实际成交价差多少；
- stale listing 平均多久下线；
- 合租 listing 中到底多少真的形成共同住户；
- archive 里的幸存 listing 相对真实历史市场存在多大 selection bias。

---

## 19. Negative result: no verified 1998–2005 Chinese rental-search capture in this pass

本轮找到了：

- 2010 同期正式平台产品/风险说明；
- 2007–2008 同期用户/媒体材料；
- later live/archive locators 和图像线索。

但**没有取得并实际打开、检查一份足以复原 1998–2005 核心中文租房搜索流程的 Wayback/WARC memento**。

因此本 note 不猜：

- early SouFun/搜房原 DOM；
- GB2312/GBK/UTF-8；
- frameset；
- search `GET`/`POST`；
- city cookie；
- `input name`；
- listing ID pattern；
- pagination；
- QQ/phone masking；
- IE-only JS/ActiveX；
- historical SERP ranking。

搜索结果里的截图、现代镜像、当前公司史只能作为 locator/secondary evidence。

按照 `docs/METHOD.md`：

> **Wayback locator not opened and checked ≠ verified historical capture.**

---

## 20. Next evidence package

最有价值的下一步不是再找“某平台有几百万房源”，而是拿下一份 **2000–2005 verified Chinese rental/classified flow**：

```text
original URL
capture datetime
HTTP/replay state
charset
city/category navigation
search form
query parameters
listing card fields
price/unit semantics
poster-role label
contact representation
pagination
images/subresources
browser assumptions
archive rewrite
which backends are dead
```

然后选一条普通 listing 做最窄的 longitudinal trace：

```text
t0: listing appears
t1: refresh/change price
t2: phone/QQ/contact evidence if public and ethical
t3: page removed / stale
t4: later cached/quoted version
```

必须接受最终很可能只能得到：

> “我们知道这间房曾经被网页描述为可租；不知道最终谁住进去。”

而这一句本身就是本对象最重要的 old-Web 考古结论之一。
