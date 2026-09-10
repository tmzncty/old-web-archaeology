# EMERGENCY HOTLINE / WEB / EMAIL / SMS / LOCATION / DISPATCH STATE GAPS, 1995–2015

## Scope

本文件只处理约 1995–2015 中文互联网及其紧密相邻的电信/数字调度接口，核心对象是：

- 110/119/120/122 等公共紧急入口与后台调度的关系；
- 2001 年前后公安 Web/E-mail 对外入口；
- 2009 年后 12110 短信报警；
- 网站、短信、地图、位置编码和调度系统之间的状态差；
- archive 能看到什么、系统实际执行什么。

它**不是**中国警务史、院前急救史，也不把全球 911/E911 纳入本仓库主体。全球和 1995 年之前的比较放在 `how-people-lived`，这里只有必要的边界说明。

交叉文件：

`tmzncty/how-people-lived/topics/emergency-calling-location-legibility-and-help-seeking-executability-china-1986-2026.zh-CN.md`

---

## 1. Why this is an old-Web problem even when the emergency itself is not “on the Web”

紧急求助是一个很好的反例，可以防止 old-Web archaeology 退化成“保存网页截图”。

普通人可能只做了一件事：拨 110。

但后台可能同时经过：

`PSTN/mobile network`
→ `110/119/120/122 entry point`
→ `call-taking console`
→ `caller/callback number`
→ `address or location representation`
→ `incident/case record`
→ `dispatch rule`
→ `radio/data network`
→ `responder terminal`
→ `physical arrival`

Web 可能只出现在以下位置之一：

- 告知公众号码、范围、使用说明；
- 接受非紧急咨询或 E-mail；
- 提供在线报警/举报入口；
- 在 2000s 后作为短信、地图、账号、实名和后台数据系统的邻接层。

因此：

**`Web page survives != emergency transaction survived`**。

---

## 2. Research objects: do not collapse them

### 2.1 Person / event layer

- physical person needing help
- caller / reporter / witness
- person actually at risk
- incident location
- caller location
- responder destination

这些对象可能不是同一个位置、同一个人。

### 2.2 Communication layer

- fixed telephone
- mobile telephone
- SMS handset
- Web browser
- E-mail client
- WAP/mobile Web endpoint
- later app/WeChat boundary objects（仅作 2015 之后的边界，不在本文展开）

### 2.3 Public entry layer

- `110`
- `119`
- `120`
- `122`
- local non-emergency police hotlines
- `12110` SMS
- public website / mailbox / online report form

### 2.4 Authority layer

- telecom switch/routing
- PSAP-like call-taking desk / 110 command center / 120 dispatch center
- operator console
- case/incident record
- GIS/map/address database
- CAD/dispatch system
- radio/mobile data dispatch
- responder unit
- closure/settlement record

### 2.5 Archive layer

- current official retrospective page
- contemporaneous news report
- historical site capture
- current render of legacy article
- archived HTML shell
- preserved images/scripts/forms
- missing private dispatch records

---

## 3. Minimum state chain

A defensible reconstruction should distinguish at least:

`need for help exists`
→ `reporter decides/tries to report`
→ `call/message submitted`
→ `network accepts`
→ `correct endpoint receives`
→ `operator notices/answers`
→ `caller/message is intelligible`
→ `event type is classified`
→ `location is represented`
→ `location is operationally usable`
→ `incident record created`
→ `dispatch issued`
→ `unit accepts/receives dispatch`
→ `unit moves`
→ `unit finds place/person`
→ `unit arrives`
→ `incident closes`

Never collapse these into “报警成功”.

---

## 4. State gaps to preserve permanently

### G01. number-publicized / locally-routable gap

A webpage or newspaper says a number exists.

This does not establish that every locality, carrier, PBX or handset could route it identically at that time.

### G02. call-attempted / network-connected gap

The user pressed dial.

This does not establish successful network connection.

### G03. connected / operator-answered gap

A call reaches the service network but may queue, busy out, drop or wait.

### G04. caller-number / physical-caller-identity gap

CLI/ANI identifies a line or subscription, not necessarily the person speaking.

### G05. caller-location / incident-location gap

A witness may call from somewhere other than the event.

### G06. fixed-line-address / current-human-location gap

Even a registered fixed address does not prove the person needing help is at that address.

### G07. mobile-number / physical-location gap

A mobile number is portable across space.

### G08. cell-site-location / exact-incident-location gap

Base-station/cell information is a coarse clue, not a room, entrance or exact point.

### G09. device-GPS / dispatcher-visible-location gap

A phone may know its position while the emergency platform has no interface to receive it.

### G10. dispatcher-visible-coordinate / responder-usable-place gap

A coordinate can still correspond to a gated campus, wrong entrance, elevated road, complex building or inaccessible roadside.

### G11. place-name / unique-location gap

“河南大学”“火车站”“人民广场”等名称不一定唯一，也不一定给出入口。

### G12. SMS-sent / SMS-delivered gap

SMS can be delayed or lost.

Contemporaneous 12110 guidance explicitly warned of this limitation.

### G13. SMS-delivered / platform-ingested gap

Carrier delivery does not establish ingestion by the police SMS platform.

### G14. platform-ingested / operator-read gap

Queueing and staffing are separate states.

### G15. operator-read / reply-received gap

The platform may reply while the sender has turned off the phone, lacks signal, cannot safely read a reply, or requested no reply.

### G16. message-readable / incident-locatable gap

Text may omit city, road, vehicle, direction or timing.

### G17. Web-form-submitted / authoritative-case-created gap

A successful HTTP POST is not necessarily a dispatch record.

### G18. e-mail-sent / mailbox-checked gap

Especially important for early public-sector Web.

In 2001 Shanghai’s new police hotline, contemporaneous reporting said E-mail was checked three times a day. That makes it categorically different from 110 emergency telephony.

### G19. website-called-“110” / emergency-110 gap

A domain containing `110` or a page branded “公安热线” does not mean real-time emergency dispatch.

### G20. “网上报警” / physical-emergency-reporting gap

In early Chinese Web sources, “互联网报警/网上报警” may instead mean reporting computer-network intrusion, illegal online content or cyber incidents.

### G21. public-advice / live-service gap

Instructions can survive after the backend service changes or closes.

### G22. incident-record-created / dispatch-issued gap

Logging and dispatch are separate authority states.

### G23. dispatch-issued / responder-received gap

Radio/data delivery can fail or route incorrectly.

### G24. responder-received / responder-en-route gap

An assigned unit may not yet have departed.

### G25. en-route / arrived gap

ETA and motion do not prove arrival.

### G26. arrived-nearby / found-person gap

Especially important where the caller cannot describe an entrance, floor or precise point.

### G27. 110/119/122 “three desks merged” / organizational-homogeneity gap

“三台合一” can mean different degrees of technical and organizational integration. Contemporary 2007 material itself used “不同程度地实现”.

### G28. national-number-standard / local-service-launched gap

12110 was designated a national standard number in 2009, while many local systems were still under construction.

### G29. service-launched / public-awareness gap

A new channel can exist without ordinary people knowing it.

### G30. accessible-in-principle / accessible-in-practice gap

A text channel may improve access for hearing/speech-impaired users while still requiring literacy, signal, handset operation and location description.

---

## 5. Anchor case A: Shanghai 2001 `www.china110.com` — important precisely because it was NOT emergency Web 110

### 5.1 Contemporaneous evidence

On 2001-01-10/11, contemporaneous Xinhua/China News/Shanghai reporting described a new Shanghai “公安热线”.

Public routes included:

- telephone `24023456`;
- Internet site `www.china110.com`;
- E-mail.

The reports explicitly distinguished it from 110: the new hotline/network channel primarily handled **non-emergency consultation and requests**, while 110 remained for emergencies.

One report said incoming E-mail would be opened/checked three times each day.

Evidence grade: **B — contemporaneous secondary report describing an official launch**.

Sources:

- China News Service via Sina, 2001-01-11: https://news.sina.com.cn/s/168507.html
- 解放日报 via Sina, 2001-01-10: https://news.sina.com.cn/c/168046.html

### 5.2 Why this matters methodologically

A future researcher may see:

`china110.com`

and infer:

“Shanghai had Web emergency reporting in 2001.”

The contemporaneous description instead supports a narrower claim:

**The Web/E-mail route was designed partly to divert consultation and non-emergency requests away from the emergency 110 line.**

This is the opposite of “Web replaced the emergency phone.”

### 5.3 State model

`public reads site/news`
→ `sends e-mail / uses network contact`
→ `mail reaches mailbox`
→ `staff opens mailbox at scheduled interval`
→ `classifies request`
→ `routes/answers`

This workflow is not equivalent to:

`dial 110`
→ `real-time call-taking`
→ `incident dispatch`.

### 5.4 Historical capture status

A verified M1 capture for `www.china110.com` was **NOT ACHIEVED IN THIS SLICE**.

A web search for indexed historical captures did not provide a capture that could be checked for all required METHOD fields. A direct CDX request could not be evaluated in the current research interface.

Therefore we do **not** claim:

- Wayback had no copy;
- the site used any particular charset;
- a specific form action existed;
- a particular browser/ActiveX requirement existed;
- the 2001 HTML looked like later screenshots or current descendants.

Required next evidence:

`original URL + capture URL + capture datetime + HTTP status + raw/decoded bytes + charset evidence + DOM + form/mail link + subresources + second time point`.

---

## 6. Semantic trap: 2002 “互联网报警处置中心” does not mean ordinary emergency Web reporting

A 2002 China News report described Nantong establishing Jiangsu’s first “互联网报警处置中心”. Users could call 110 or use a website when computers were attacked.

Evidence grade: **B — contemporaneous secondary report**.

Source: https://tech.sina.com.cn/i/c/2002-09-03/1318136321.shtml

The center’s described scope focused on computer viruses, intrusions, network security and information-system incidents.

Therefore the phrase “互联网报警” has at least two historically distinct senses:

1. **using the Internet as the reporting channel**;
2. **reporting an Internet/computer-security incident**.

A search-result snippet alone can easily collapse them.

Permanent rule:

**Never code “网上110 / 互联网报警” as a public physical-emergency Web interface until the article/manual says what object is being reported and how it reaches dispatch.**

---

## 7. Anchor case B: 2009 `12110` — national identifier, locally uneven service

### 7.1 National number standardization

A 2009 report relaying Ministry of Public Security information said `12110` had been set as the nationwide public SMS alarm number.

At that moment:

- Shanghai, Tianjin, Zhejiang were reported as having service across their jurisdictions;
- 44 prefecture-level cities and 15 county-level cities had also launched;
- other places were still studying/building systems.

Evidence grade: **B — contemporaneous official-information report**.

Source: https://www.npc.gov.cn/WZWSREL25wYy9jMi9jMTg4L2MyMTkvMjAxOTA1L3QyMDE5MDUyMl8xNzA3OTMuaHRtbA%3D%3D

### 7.2 Accessibility is central, not incidental

The same material explicitly identified hearing/speech-impaired people and situations in which voice calling was unsafe or impractical as key use cases.

A 2009 Henan report preserves contemporaneous user demand:

- a long-distance coach passenger wanted a silent reporting channel because speaking could expose him;
- a migrant worker described seeing theft on a crowded bus but remaining silent because he felt threatened;
- other interviewees worried about SMS delay/loss and whether police could locate a sender.

Evidence grade: **B-personal — contemporaneous media interviews, not representative population evidence**.

Source: https://news.sina.com.cn/c/2009-01-13/071115024341s.shtml

### 7.3 The national number is not the service state

Preserve:

`12110 nationally designated`
≠ `province configured`
≠ `city configured`
≠ `carrier routes correctly`
≠ `SMS delivered`
≠ `police platform ingests`
≠ `operator reads`
≠ `sender receives confirmation`
≠ `location actionable`
≠ `dispatch occurs`.

This is a canonical example of why a nationally standardized identifier must not be equated with nationwide operational availability.

---

## 8. 2012 physical location codes: a non-Web interface to a digital dispatch map

A 2012 Chengde government report described two local additions:

- `12110` SMS alarm service;
- numbered street-light poles that callers could report to 110, allowing the command center to map the code to a precise location.

Source: https://www.chengde.gov.cn/art/2012/1/11/art_360_72899.html

Evidence grade: **B — contemporaneous local-government report**.

This is particularly valuable for old-Web archaeology because it shows a hybrid interface:

`physical pole label`
→ `human reads numeric code`
→ `voice/SMS transmits code`
→ `digital database resolves location`
→ `dispatcher sends unit`.

There may be **no public Web transaction at all**, yet the life-world is being reorganized by a digital spatial index.

Call this:

### public-physical-key / private-digital-map split

The durable public artifact is a number painted on physical infrastructure. The authoritative mapping from number to dispatchable coordinates lives inside a private system.

---

## 9. Back-end digitization evidence inside the scope window

A 2007 contemporaneous report on Anshan 110 described an integrated command center using:

- SMS mass messaging;
- electronic maps;
- GPS satellite positioning;
- large-screen displays;
- video monitoring;
- wired/wireless communications.

Evidence grade: **B — contemporaneous local press report**.

Source: https://news.sina.com.cn/o/2007-01-11/073310971652s.shtml

This matters because it prevents a false Web-centric chronology:

**A citizen may still only dial a three-digit voice number while the institutional side has already become a networked computer workflow.**

The public interface can remain extremely old while the dispatch substrate changes radically.

---

## 10. Boundary after 2015: why later video alarm systems matter to interpretation but not to this file’s object range

2018 Yantai `@110` and later 5G video alarm systems show where the old state gaps eventually moved:

- voice-only description → video/visual evidence;
- manual landmark description → device/map location;
- telephone number → account/real-name layer;
- call recording → multimodal evidence record.

But those systems are post-2015 and belong mainly in `how-people-lived` or a future post-old-Web project.

They may be used here only as **boundary evidence** showing that the 1995–2015 problems of location and modality did not disappear automatically.

---

## 11. Archive asymmetries

### 11.1 public-interface survival / dispatch-state loss asymmetry

Likely to survive publicly:

- hotline number;
- official service description;
- FAQ/instructions;
- news story announcing a launch;
- domain name;
- public e-mail address;
- screenshot of a public form.

Systematically less likely to survive publicly:

- actual call queue state;
- call audio;
- caller number;
- exact live location;
- operator notes;
- incident classification;
- CAD event ID;
- dispatch messages;
- radio traffic;
- unit GPS;
- actual arrival time;
- closure details.

This is not simply “archive missingness”. Much of the strongest transaction evidence is private by design.

### 11.2 static-instruction / live-routing loss asymmetry

A 2009 page can say “send to 12110”.

That page cannot by itself tell us whether, at 23:17 on a particular date:

- the sender’s carrier routed it;
- the local SMS gateway was healthy;
- the message queued;
- an operator saw it;
- the reply arrived.

### 11.3 hotline-name survival / organizational-state loss asymmetry

The same number can survive across major reorganizations of:

- call centers;
- geographic boundaries;
- dispatch responsibility;
- 110/119/122 integration;
- staffing;
- software.

A persistent number should not be mistaken for a persistent backend.

### 11.4 public-location / private-location-authority inversion

Historical public pages may tell users to provide an address or pole code.

The actual authority that resolves that text/code into a dispatcher map may be an inaccessible private database. The public artifact documents the expected interface, not the live geospatial state.

---

## 12. Capture contract for an emergency-service old-Web case

A future M1 case should record:

1. exact original URL;
2. exact capture URL;
3. capture datetime;
4. HTTP result and redirect chain;
5. bytes/encoding/charset evidence;
6. visible text and DOM structure;
7. form method/action, `mailto:` or linked endpoint if present;
8. whether submission endpoint was captured separately;
9. scripts/frames/images/subresources;
10. browser/plugin requirements only if evidenced;
11. whether the interface was emergency, non-emergency, cyber-incident, complaint or information-only;
12. stated service hours / mailbox checking rhythm;
13. whether a successful submit had any stated dispatch semantics;
14. second historical time point;
15. privacy review before retaining any personally identifying report content.

---

## 13. Privacy boundary

Emergency communication generates exceptionally sensitive records.

Do not seek, republish or reconstruct ordinary persons’:

- phone numbers;
- home addresses;
- medical details;
- call recordings;
- exact incident locations tied to private individuals;
- account identifiers;
- private SMS contents;
- dispatch histories;
- victim/witness identities beyond what is necessary for already-public historical reporting.

For archaeology, **service/interface metadata is usually sufficient**.

This creates a deliberate evidence ceiling:

**The project may be able to prove that a channel existed and how it was supposed to work while intentionally refusing to prove the full path of a private person’s real emergency.**

That is a correct boundary, not a research failure.

---

## 14. Evidence ledger

| Claim | Grade | Source | Limits |
|---|---|---|---|
| Shanghai launched `www.china110.com` / E-mail police hotline in Jan 2001 for mainly non-emergency consultation/help | B | China News/解放日报 contemporaneous reports | no verified historical capture yet |
| E-mail was reportedly checked three times daily | B | China News via Sina, 2001 | reported workflow, not server log |
| Nantong 2002 “互联网报警处置中心” dealt with computer/network security incidents | B | China News, 2002 | demonstrates semantic ambiguity, not general emergency Web reporting |
| By end-2006, 1743 of 2087 target county/city public-security organs had achieved “three desks in one” to varying degrees | B | MPS press-conference report, 2007 | “不同程度” must be preserved |
| `12110` was designated national public SMS alarm number in 2009 while local deployment remained uneven | B | MPS information relayed by legal media/NPC site | designation != local launch |
| Contemporaneous users described situations in which speaking aloud was unsafe and wanted SMS | B-personal | 大河报, 2009 | individual path evidence only |
| Police guidance warned SMS could delay or be lost | B | 2009/2012 reporting | channel limitation, not quantified reliability |
| Chengde used street-light pole codes as a location aid in 2012 | B | Chengde government, 2012 | one locality |
| Anshan 110 used electronic maps/GPS/video and other digital systems in 2007 | B | local press, 2007 | system description, not per-incident proof |

---

## 15. Sources

1. 上海开通网上“公安热线”, 中新社 via Sina, 2001-01-11.  
   https://news.sina.com.cn/s/168507.html

2. 上海市公安局开通热线24023456密切警民联系, 解放日报 via Sina, 2001-01-10.  
   https://news.sina.com.cn/c/168046.html

3. 江苏加强网络监督成立首家互联网报警中心, 中国新闻网 via Sina, 2002-09-03.  
   https://tech.sina.com.cn/i/c/2002-09-03/1318136321.shtml

4. 公安部通报全国公安机关“三台合一”建设情况, 2007-01-09.  
   https://news.sohu.com/20070109/n247504535.shtml

5. 打110，海、台、岫全知道——鞍山“三台合一”, 北方晨报 via Sina, 2007-01-11.  
   https://news.sina.com.cn/o/2007-01-11/073310971652s.shtml

6. 公安部：全国统一短信报警号“12110”上海天津等开通, 2009-01-12.  
   https://www.npc.gov.cn/WZWSREL25wYy9jMi9jMTg4L2MyMTkvMjAxOTA1L3QyMDE5MDUyMl8xNzA3OTMuaHRtbA%3D%3D

7. 报警“动手不动口”无声胜有声, 大河报 via Sina, 2009-01-13.  
   https://news.sina.com.cn/c/2009-01-13/071115024341s.shtml

8. “110”出新招——“路灯杆编码”和“12110短信”可报警, 承德市政府, 2012-01-11.  
   https://www.chengde.gov.cn/art/2012/1/11/art_360_72899.html

9. Boundary reference only: 烟台市公安局“@110”, 2018.  
   https://www.yantai.gov.cn/art/2018/4/16/art_12307_958319.html

---

## 16. M1 status

**M1 verified historical Chinese emergency/police Web capture: NOT ACHIEVED IN THIS SLICE.**

Specific leads now worth a future capture pass:

- `www.china110.com`, especially Jan 2001–2003;
- any contemporaneous Shanghai police page explaining `24023456` + Web/E-mail division of labor;
- early 12110 public instruction pages, ideally 2009–2012;
- early local “网上110” pages whose scope can be proven to be physical-emergency, non-emergency, cybercrime, or complaint service rather than inferred from the name.

Do not upgrade a locator/search hit into M1 without the METHOD metadata.

---

## 17. What this adds to old-Web archaeology

The key result is not “police went online.”

It is the opposite correction:

**The Web often sat beside, around, or behind the authoritative emergency transaction rather than replacing it.**

A 2001 E-mail page could deliberately divert non-emergency traffic away from 110. A 2009 SMS number could provide a silent interface while still depending on telecom delivery, local deployment, human reading and location description. A street-light number could be a physical key into a private digital map. A 110 call could look unchanged to the citizen while its institutional backend moved from paper and radio toward networked computer dispatch.

For this domain, the most historically important state is often exactly the one a Web crawler cannot see:

**the moment a vague human message becomes a dispatchable place.**
