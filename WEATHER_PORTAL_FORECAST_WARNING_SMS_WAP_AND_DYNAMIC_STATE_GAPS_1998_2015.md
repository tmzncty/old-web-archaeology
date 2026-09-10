# Weather portal / forecast / warning / SMS / WAP / dynamic-state gaps, 1998–2015

## Scope

This note keeps the repository’s main object inside the roughly **1995–2015 Chinese Internet**. Earlier telephone weather services and overseas systems appear only as boundary context needed to understand what the Chinese Web did and did not replace.

The object is not “the history of meteorology.” It is a narrower old-Web archaeology question:

> When a Chinese Web or WAP page said “北京天气预报”, “未来三天天气”, or displayed a warning icon, **what historical state was actually represented, who had authority over that state, how long did it remain valid, and what part of the real service could a Web archive preserve?**

The central warning for archaeology is simple:

```text
archived weather page
!= historical weather state automatically preserved
```

Weather sites are unusually difficult historical objects because their public shell can remain stable while almost every value inside it is time-dependent, frequently revised, loaded from a backend, or rewritten by the current site.

---

## 1. Research units: do not collapse these objects

A weather-service reconstruction should distinguish at least the following units:

1. **observational station / sensor** — a physical source of measured weather;
2. **observation record** — temperature, rain, wind, radar or satellite state at one observation time;
3. **forecast run / guidance** — model or forecaster output generated at a particular issue time;
4. **forecast product** — public forecast derived from guidance;
5. **warning product** — separately issued risk communication with level, area and validity;
6. **forecast revision** — a later version for an overlapping future interval;
7. **city identifier** — the system’s internal mapping between a place name and a forecast object;
8. **public Web URL** — the page address a user opens;
9. **HTML shell** — navigation, labels, template, city selector and static copy;
10. **dynamic data response** — backend values inserted into the shell;
11. **image product** — radar, satellite, typhoon-path or warning image;
12. **WAP page** — a mobile representation that may use a different URL and reduced product set;
13. **SMS subscription product** — scheduled forecast sent to an enrolled phone;
14. **public emergency SMS** — warning pushed regardless of normal paid-subscription status in some jurisdictions;
15. **121/12121 telephone product** — audio/IVR retrieval through the telephone network;
16. **TV/radio bulletin** — scheduled broadcast representation;
17. **electronic display / loudspeaker output** — public-space dissemination;
18. **portal syndication copy** — weather data shown by Sina, Sohu, QQ or other portal rather than the meteorological authority itself;
19. **archive capture** — one preserved representation at one capture datetime;
20. **claim** — the minimum historical statement supported by evidence.

A brand such as “中国天气网” may span many of these layers, but they are not interchangeable evidence.

---

## 2. Pre-Web boundary: on-demand weather did not begin with the Chinese Internet

### 2.1 China: 121 telephone service as a boundary object

A China Weather historical institutional page for Daxinganling states that in **1999** local stations completed a digital upgrade of the “121” automated weather-forecast answering system and offered multiple information boxes such as clothing and comfort indices.

Evidence grade: **B/C institutional retrospective**.

Safe claim:

> In at least this regional system, automated telephone weather retrieval was already an established service object by 1999 and was undergoing digital upgrading.

Unsafe claims:

- “121 started nationwide in 1999”;
- “most Chinese households used it”;
- “Web replaced 121 in 1999.”

Source:

- https://hlj.weather.com.cn/gywm/101050701.shtml

### 2.2 Overseas comparison: the state gap predates the Web

New York’s WEather 6-1212 telephone service began in 1939. Contemporary TIME and New Yorker reports describe a recorded forecast updated from Weather Bureau information; callers could retrieve it on demand.

This matters because an old-Web weather portal inherits an older problem:

```text
source forecast version
!= recording currently on telephone service
!= what a particular caller actually heard
```

The Web did not invent version mismatch. It made versioning faster, more spatially granular and more archive-visible.

Sources:

- https://time.com/archive/6760340/communications-fair-warmer/
- https://www.newyorker.com/magazine/1939/07/15/heavenly-voices

A second boundary example is France’s Minitel weather service, reported at its 2011 shutdown as having roots around 1982. This is another reminder that **online weather information != Web**.

- https://www.01net.com/actualites/le-3615-meteo-fermera-le-30-septembre-539452.html

These overseas objects do **not** expand this repository into global old-Web history. They only define the technical prehistory against which Chinese Web weather services should be interpreted.

---

## 3. Chinese public weather information before and around mass Web adoption

A later China Meteorological News retrospective dates public broadcast/newspaper weather information to 1956-07-01, and a People’s Daily publication-history page shows weather appearing in the newspaper header for long periods.

For this repository, the point is only the media transition:

```text
scheduled publication/broadcast
→ on-demand telephone retrieval
→ Internet portal / WAP retrieval
→ SMS and later app push
```

Do not write this as replacement. Evidence from 2007 onward shows all these channels overlapping.

Boundary sources:

- https://news.weather.com.cn/2019/09/3242518.shtml
- https://dangshi.people.com.cn/n/2015/0210/c85037-26538880.html

---

## 4. 2007 multi-channel evidence: Web was one channel in a larger dissemination fabric

### 4.1 Shanghai mobile/WAP weather, SMS, TV, radio and displays

A 2007 contemporary Shanghai report describes a “mobile weather station” that could expose satellite imagery, radar, wind/rain and warnings through mobile Internet/WAP. The same report also describes weather SMS, large amounts of TV/radio weather programming and electronic displays.

Evidence grade: **B contemporary media**, likely including official/provider claims that require care on scale numbers.

Minimum supported claim:

> By early 2007, Shanghai weather information could move through mobile/WAP and SMS while broadcast and public-display channels remained active.

This establishes a crucial old-Web interpretation rule:

**a weather portal capture is not the whole public weather service of that day.**

Source:

- https://tech.sina.com.cn/t/2007-01-12/08271332058.shtml

### 4.2 Public-warning SMS vs paid routine forecast SMS

Contemporary 2007 reporting distinguishes emergency/disaster warning SMS from routine personalized weather-SMS subscription products. Some public discussion explicitly argued that disaster warnings should not depend on paid subscription.

This creates separate research units:

```text
routine forecast subscription
!= public emergency warning dissemination
```

A phone could receive one without being subscribed to the other, depending on place, operator and policy.

Useful contemporary leads:

- https://news.sina.com.cn/c/2007-08-13/155812376368s.shtml
- https://news.sina.com.cn/c/2007-08-27/063613749726.shtml

### 4.3 SMS can be a trigger, telephone/Web can be the continuation channel

A 2007 Guangdong emergency-message case instructed recipients to call **12121** for updated weather. This is a hybrid information architecture:

```text
push layer: SMS tells you to pay attention
pull layer: telephone/Web/WAP provides continued updates
```

When reconstructing “what information was available,” researchers should therefore look for cross-channel handoffs, not one page alone.

---

## 5. 2008 launch of China Weather: what is actually proven

### 5.1 Contemporary launch evidence

A contemporary 2008-07-28 report states that **www.weather.com.cn** formally launched that day as a public meteorological service portal. It describes weather forecast, disaster warning, information, climate, tourism and science channels; it says the portal exposed weather information for 2,913 domestic and overseas cities and had a mobile service through **wap.weather.com.cn/wap/** with three-day forecasts/trends for roughly 3,000 cities.

Evidence grade: **B contemporary report based heavily on official launch claims**.

Source:

- https://news.sina.com.cn/s/2008-07-28/144214229855s.shtml

Official/near-official later confirmation:

- https://www.weather.com.cn/index/lssj/11/374248_4.shtml
- https://www.weather.com.cn/zt/syds/1684476.shtml

Safe claims:

- the public portal existed and was formally launched by 2008-07-28;
- a WAP endpoint was advertised at launch;
- city forecasts/warnings and Olympic-specific products were part of the stated service;
- Web and WAP were intentionally parallel interfaces.

Do not infer without capture evidence:

- exact 2008 DOM structure for every city page;
- exact charset or HTTP headers;
- whether every advertised city endpoint worked at every moment;
- browser compatibility;
- whether a current `weather.com.cn/weather/<cityid>.shtml` pattern existed in the same form at launch;
- whether the WAP URL was archived with its dynamic data;
- actual user counts from page availability alone.

### 5.2 The launch date itself contains a useful same-day artifact

Current China Weather historical pages preserve articles dated **2008-07-28** about Typhoon Fung-wong, including images and exact forecast issue times.

Example current legacy URLs:

- https://zj.weather.com.cn/alarm/lssj/07/23384.shtml
- https://www.weather.com.cn/zt/tqzt/fh808/07/59012.shtml

These are useful **surviving official legacy pages**, but they are not automatically equivalent to a verified 2008 archive capture. The current HTTP response, template, navigation and footer may have changed after publication.

Therefore record separately:

```text
article publication datetime
!= current retrieval datetime
!= original 2008 rendered shell
!= archived 2008 capture
```

---

## 6. Weather pages are versioned future objects, not static facts

A weather forecast has at least two time axes:

1. **issue time** — when this forecast version was produced/published;
2. **valid time** — the future interval it predicts.

A third axis often matters:

3. **capture time** — when an archive captured a representation.

For archaeology, always prefer fields such as:

```yaml
forecast_issue_time:
forecast_valid_from:
forecast_valid_to:
warning_issue_time:
warning_level:
warning_area:
warning_cancel_time:
page_publication_time:
archive_capture_time:
retrieval_time:
```

Do not collapse them into one `date`.

### Example

A page captured at 15:00 may contain a forecast issued 11:00 and valid 20:00–08:00 tomorrow. A current re-render of a legacy URL in 2026 may carry modern navigation/footer but preserve an old article timestamp. Those are different historical statements.

---

## 7. State-gap catalogue

### 7.1 Observation / forecast gaps

1. `sensor-observation / public-observation gap`
   - station measured a value;
   - public page may show a delayed, rounded or selected representation.

2. `model-run / public-forecast gap`
   - backend guidance exists;
   - human/automated public product can differ.

3. `forecast-generated / forecast-published gap`
   - a product may exist internally before public release.

4. `forecast-issued / forecast-current gap`
   - a later update can supersede the version a user saw earlier.

5. `forecast-horizon / certainty-horizon gap`
   - a 15-day page exists;
   - confidence is not uniform across all 15 days.

6. `city-name / city-id gap`
   - visible place label can map to an internal ID whose historical mapping must be verified.

7. `administrative-area / meteorological-area gap`
   - warning coverage may not align perfectly with what a user infers from a city label.

### 7.2 Warning gaps

8. `hazard-detected / warning-issued gap`

9. `warning-issued / Web-page-updated gap`

10. `warning-issued / SMS-dispatched gap`

11. `SMS-dispatched / carrier-accepted gap`

12. `carrier-accepted / handset-delivered gap`

13. `handset-delivered / human-noticed gap`

14. `human-noticed / human-understood gap`

15. `human-understood / human-believed-actionable gap`

16. `warning-level / institution-response gap`
   - red warning can exist without school/work/transport stopping at exactly the same moment.

17. `warning-issued / warning-cancelled gap`
   - archive may preserve issue page but not cancellation.

18. `warning-area / actual-user-location gap`
   - subscriber number/handset association does not guarantee the person is physically inside the warned area.

### 7.3 Web/WAP gaps

19. `HTML-shell / live-data gap`

20. `city-page / data-endpoint gap`

21. `data-endpoint / exact-forecast-version gap`

22. `desktop-page / WAP-page gap`

23. `WAP-advertised / device-compatible gap`

24. `URL-resolves-today / URL-had-same-meaning-historically gap`

25. `page-publication-timestamp / original-render gap`

26. `legacy-page-survival / legacy-template-survival gap`

27. `current-footer / historical-footer gap`

28. `city-list-count / executable-city-endpoint gap`

29. `portal-copy / meteorological-authority-source gap`
   - a portal may cache/reformat an official product.

30. `portal-update-time / source-update-time gap`

### 7.4 SMS / telephone gaps

31. `routine-SMS-subscriber / emergency-warning-recipient gap`

32. `SMS-subscription-active / daily-message-delivered gap`

33. `12121-number-advertised / IVR-operational gap`

34. `IVR-operational / local-call-accessible gap`

35. `telephone-recording / latest-forecast gap`
   - recording update may lag source product.

36. `SMS-text / full-warning-product gap`
   - character limits may compress detail.

### 7.5 User-action gaps

37. `forecast-viewed / decision-changed gap`

38. `warning-received / plan-cancelled gap`

39. `warning-understood / institution-permits-exit gap`

40. `rain-icon / umbrella-carried gap`

41. `warning / harm-avoided gap`
   - causal claim requires far more evidence than delivery.

---

## 8. 2014 redesign is a useful versioning checkpoint

China Weather’s surviving 2014 redesign announcement states that the new site extended forecast display to 15 days, added three-hour forecasts for the next three days, scenic-area forecasts and air-quality observations. The same announcement explicitly warns users that forecasts are uncertain and that longer lead times are less certain; products are continually revised.

Evidence grade: **A/B official product announcement surviving on current official site**.

Source:

- https://www.weather.com.cn/wzfw/gbgg.shtml

This is unusually useful for archaeology because the provider itself states a rule historians must preserve:

> **a forecast is a revisable future estimate, not a timeless fact stored behind a URL.**

A capture of `Tuesday: rain` and another capture hours later of `Tuesday: cloudy` are not necessarily contradictions or archive corruption. They may be legitimate forecast revisions.

---

## 9. Old-Web preservation biases specific to weather

### 9.1 `page-shell survival / forecast-state loss asymmetry`

The navigation, city name, “7天天气”, footer and help copy can survive while the historically correct forecast payload disappears.

A crawler may therefore preserve the *shape of consulting the future* while losing the future that users actually saw.

### 9.2 `static-article survival / live-widget loss asymmetry`

A typhoon news article with text and a static JPEG can remain highly legible decades later. A city homepage whose temperature, icons and hourly data came from live backend calls may replay as blank, error, or present-day values.

This systematically overrepresents editorial weather articles relative to routine daily checking.

### 9.3 `warning-issue survival / warning-cancel loss asymmetry`

High-impact warning pages are more likely to be linked and archived than routine cancellation/expiry state. A historical reconstruction can therefore accidentally make danger appear to last longer than the operational warning did.

### 9.4 `public-Web survival / private-delivery loss asymmetry`

The official warning page may survive. The decisive user-side states usually do not:

- was a given phone included in the target audience?
- did the carrier deliver it?
- did the user open/notice it?
- did they understand it?
- did a school or employer release them?

These are not only hard to archive; some are private data and should not be reconstructed at individual level without research necessity.

### 9.5 `current-legacy-render / historical-render confusion`

China Weather still serves pages carrying 2008–2013 publication timestamps. Their survival is valuable, but current navigation, footer, CSS, service telephone numbers or related links can be newer than the article body.

Never label a screenshot of the page fetched today “what the site looked like in 2008” unless a 2008 capture verifies it.

### 9.6 `forecast-popularity / disaster-visibility bias`

Archives and news search overpreserve typhoons, floods, “forecast failed” stories and severe warnings. The overwhelmingly ordinary act—checking tomorrow’s temperature before dressing—may leave fewer durable traces.

This means disaster-heavy source collections can distort the social history of weather use.

---

## 10. Contemporary user evidence and what it can establish

### 10.1 2008 forecast-SMS complaints

A 2008 contemporary news report records users complaining when a subscribed weather forecast predicted rain or temperature changes that did not match their later local experience.

Source:

- https://news.sina.com.cn/c/2008-05-09/201113854723s.shtml

For old-Web archaeology this does **not** prove the exact SMS content unless the message itself is preserved. It proves a narrower state:

> Some users had integrated forecast SMS into clothing/umbrella decisions strongly enough to compare forecast and outcome and complain about mismatch.

### 10.2 2018/2019 App Store reviews as later boundary evidence

Current Apple App Store pages expose old reviews dated 2018 and 2019 describing routine weather checking before going out or during travel.

Source:

- https://apps.apple.com/cn/app/%E5%A2%A8%E8%BF%B9%E5%A4%A9%E6%B0%94-%E8%AE%A9%E6%9C%AA%E7%9F%A5%E5%8F%AF%E5%85%88%E7%9F%A5/id434209233?platform=iphone&see-all=reviews

These are **not** in repository scope as a 2018+ technical old-Web case, but they are useful endpoint evidence for the transition being traced: city-specific pull-based Web/WAP weather had become persistent location-aware mobile routine.

Archive warning:

```text
review original date
!= current review-page rendering date
```

The page can support the existence of dated review content; it cannot reconstruct the 2018 App Store UI without an appropriate historical capture.

---

## 11. 2021 Zhengzhou as a state-machine stress test outside main scope

The 2021 Zhengzhou flood lies outside this repository’s main time range but is useful as an endpoint test of the state model.

Contemporary reporting and the later State Council investigation show that multiple red warnings existed and large numbers of SMS messages were sent, yet important institutional and individual responses did not occur in time. One interviewed resident said she received a red-warning SMS but did not understand rainfall quantities as a reason to change her next-day routine.

Sources:

- https://news.sina.cn/gn/2021-07-25/detail-ikqciyzk7561257.d.html
- https://www.eeo.com.cn/2021/0724/496084.shtml
- https://www.chinanews.com/sh/2021/07-30/9532105.shtml
- https://www.mem.gov.cn/xw/bndt/202201/t20220121_407135.shtml

This later case validates why an archaeologist must never treat:

```text
“warning page existed”
```

as equivalent to:

```text
“ordinary residents had an executable warning.”
```

---

## 12. Browser, encoding and runtime questions still unknown

For a complete 2008–2010 China Weather M1 case, do **not** infer the following from generic Chinese-Web memory:

- GB2312/GBK/UTF-8 encoding for a particular URL;
- IE-only behavior;
- Flash requirements;
- JavaScript data-loader implementation;
- iframe source;
- AJAX/API hostname;
- exact CSS/table layout;
- screen-resolution assumptions;
- whether the WAP page used WML, XHTML-MP or ordinary HTML at a specific date;
- caching/CDN behavior;
- original redirect chain between `weather.com.cn`, provincial subdomains and mobile hosts.

These require capture-level evidence.

The current live pages frequently contain iframes, dynamic widgets and modern footers. They are leads, not substitutes for 2008 technical evidence.

---

## 13. M1 capture attempt in this slice

Searches in this slice included combinations of:

- `weather.com.cn` + 2008 + Internet Archive/Wayback;
- China Weather launch-era URLs;
- 12121 / WAP weather historical leads;
- current surviving legacy pages dated 2008;
- contemporary external news reports that preserve the advertised WAP endpoint.

A search-engine result did **not** yield a capture that could be opened and checked through this research environment with all minimum fields:

- `archive_source`;
- `capture_url`;
- `original_url`;
- `capture_datetime`;
- response/replay state;
- charset/Content-Type if observable;
- DOM/template;
- dynamic weather-data dependency;
- subresources;
- WAP/desktop relationship.

Therefore:

> **M1 verified historical China Weather city/WAP capture: NOT ACHIEVED IN THIS SLICE.**

This statement means only “not verified in this research slice.” It does **not** mean “Wayback did not archive China Weather” or “the page did not exist.”

The strongest current technical anchor remains the contemporary launch report advertising both `www.weather.com.cn` and `wap.weather.com.cn/wap/`, plus surviving official legacy pages.

---

## 14. Candidate M1 reconstruction plan

A strong future M1 case should select **one city + one high-impact weather period + two capture dates**, rather than trying to reconstruct the entire portal.

Recommended candidate:

**Beijing or a Fujian/Zhejiang city during Typhoon Fung-wong, 2008-07-28 to 2008-07-30.**

Required evidence bundle:

1. one verified desktop city-page capture before/near the event;
2. one second historical capture after forecast revision;
3. original `Content-Type`/charset if retrievable;
4. HTML source and script/iframe references;
5. one static warning/article page whose issue time can be independently dated;
6. advertised WAP URL and, ideally, a WAP capture;
7. one contemporaneous portal/news copy to compare content propagation;
8. record of whether warning issue and cancellation pages both survive;
9. explicit missing-resource list;
10. browser/reconstruction assumptions.

The goal should be to demonstrate at least one real historical transition such as:

```text
forecast v1 → forecast v2
or
no warning → warning issued → warning cancelled
```

and then test what the archive actually retained.

---

## 15. Evidence ledger

| ID | Date | Object | Source type | Grade | Minimal claim | Key limitation |
|---|---:|---|---|---|---|---|
| WX01 | 1939 | WEather 6-1212 | contemporary TIME/New Yorker | A/B | on-demand recorded weather by telephone existed | overseas boundary only |
| WX02 | c.1982 | 3615 Météo | 2011 shutdown report | C/B | pre-Web French online weather service existed | retrospective start date |
| WX03 | 1999 | Daxinganling 121 | institutional historical page | B/C | local automated phone service digitally upgraded | not national launch date |
| WX04 | 2007 | Shanghai mobile/WAP weather | contemporary news | B | WAP/SMS coexisted with broadcast/display channels | scale partly provider claims |
| WX05 | 2007 | warning SMS + 12121 | contemporary news | B | push and pull channels were linked | implementation varies by locality |
| WX06 | 2008-07-28 | China Weather launch | contemporary launch report | B | portal and WAP endpoint advertised; city/weather channels existed | no capture-level DOM validation |
| WX07 | 2008 | weather SMS users | contemporary interviews | B | users acted on forecasts and evaluated mismatch | not accuracy statistics |
| WX08 | 2008-present | legacy weather.com.cn articles | surviving official pages | A/B current artifact | pages with 2008 publication timestamps survive | current rendering may differ |
| WX09 | 2014 | China Weather redesign | official product announcement | A/B | forecast horizon/products changed; provider states rolling revision and uncertainty | current retrieval, not necessarily historical capture |
| WX10 | 2018/2019 | weather-app reviews | dated user content on current platform | A/B | individual users integrated weather lookup into daily planning | self-selected; current render |
| WX11 | 2021 | Zhengzhou warning chain | contemporary media + official investigation | B/A | warning issuance/delivery did not guarantee actionable response | endpoint stress-test outside main scope |

---

## 16. Claims now safe to add to the repository

### Confirmed / high confidence

- Chinese public weather information before the mass Web included broadcast/newspaper and telephone retrieval.
- At least one regional 121 automated answering service was being digitally upgraded by 1999.
- Shanghai had SMS and mobile/WAP weather channels by 2007 while TV/radio/display channels remained active.
- China Weather formally launched in July 2008 and publicly advertised desktop plus WAP weather access.
- China Weather’s own 2014 documentation explicitly treats longer-horizon forecasts as more uncertain and subject to rolling revision.
- Current official sites preserve legacy pages carrying old publication timestamps, but those current renders are not historical captures by themselves.
- A weather service is a multi-channel, versioned state machine; a Web archive can preserve only part of it.

### High probability but not yet capture-verified

- Launch-era city pages depended on data and template layers whose archival survival differed.
- WAP and desktop representations likely had different resource constraints and may have archived differently.
- Routine city forecast pages are probably underrepresented relative to typhoon/disaster editorial pages in surviving link graphs.

### Unknown in this slice

- exact 2008 city URL patterns across all provinces;
- original charset/HTTP headers for selected launch pages;
- original JS/API/iframe dependencies;
- exact WAP markup type and handset compatibility;
- whether a verified Memento can preserve both shell and historically correct forecast payload;
- how cancellation/expiry of warnings was represented in early portal pages.

---

## 17. Privacy and copyright boundary

Weather pages are mostly public, but warning-delivery research can drift into private data.

Do not reconstruct or republish:

- individual phone numbers;
- SMS delivery logs linked to persons;
- precise historical user location when unnecessary;
- private subscription/account data;
- personal movement inferred from warning targeting.

Prefer aggregate delivery statistics and voluntary public testimony.

For archive assets, link to captures and record metadata rather than copying proprietary radar imagery, maps or complete site mirrors when rights are unclear.

---

## 18. What this changes about Chinese old-Web archaeology

Weather pages reveal a particularly dangerous assumption in Web history: **that a surviving page preserves the state users saw.**

For a blog post, the body may remain relatively stable. For a weather page, the most important content is designed to expire. The HTML can survive while the forecast changes; a warning can be issued and later cancelled; the city label can survive while the backend data endpoint dies; a 2008 article can still load in 2026 inside a modern template.

This creates a characteristic archival asymmetry:

> **The old Web may preserve the interface by which people looked into the future while losing the particular future they were shown.**

That matters for ordinary-life history. A historian may know that a person *could* open a weather page in 2008, but still not know what forecast appeared before that person left home, which revision they saw, whether a warning reached their phone, or whether their school or employer allowed them to respond.

The Web artifact is therefore evidence of one layer of everyday infrastructure, not the final authority on the lived event.

---

## 19. Cross-repository link

Companion life-history note:

- `tmzncty/how-people-lived/topics/weather-forecast-warning-reachability-and-micro-future-planning-china-1956-2026.zh-CN.md`

The companion note carries the long chronology, overseas prehistory and 2005–2026 life-horizon interpretation. This repository should remain focused on Chinese Web/WAP architecture, page/state distinctions, browser/runtime assumptions and preservation failure.