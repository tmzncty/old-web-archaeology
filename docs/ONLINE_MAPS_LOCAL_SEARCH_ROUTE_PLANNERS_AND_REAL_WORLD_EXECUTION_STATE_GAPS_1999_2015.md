# Online maps, local search, route planners, and real-world execution state gaps, 1999–2015

## Scope

This note models a class of Chinese old-web object that is unusually easy to misread in archives: **online maps, local-search maps, bus-route planners, driving-direction pages, POI search and their transition toward mobile navigation**.

Main research object remains the Chinese Web, approximately 1995–2015.

Pre-1995 wayfinding appears only as boundary context. Global services such as MapQuest are comparison material and belong mainly in `how-people-lived`, not as a scope expansion of this repository.

Cross-repository companion note:

- `tmzncty/how-people-lived/topics/searchable-city-routefinding-local-search-and-navigation-china-1983-2026.zh-CN.md`

The central archaeological warning is:

> **An archived map page is not the archived city, not the archived route engine, and not evidence that a traveler reached the destination.**

---

## 1. Why online maps need a separate state model

A forum page can often remain meaningful when its HTML and text survive.

An online map is more distributed. A historical user action may have depended on:

- page HTML;
- CSS and image assets;
- a Java applet, ActiveX control, Flash object or proprietary viewer;
- JavaScript interaction code;
- map image/tile servers;
- a POI database;
- geocoding services;
- bus-route data;
- routing graph/version;
- query parameters;
- backend CGI/ASP requests;
- browser support;
- network speed;
- and a real city whose roads, stops and businesses were changing independently.

An archive can save one layer and lose all the others.

Therefore old-web map archaeology must not use a single boolean such as `page survived`.

---

## 2. Minimum object decomposition

Treat the following as separate units unless evidence proves they were one object.

### 2.1 Map host / portal

Examples:

- Beijing map guide;
- Go2Map;
- Sogou Map;
- 51ditu;
- Mapbar;
- Sina Local Search;
- Youdao Map;
- Baidu Map;
- DDMap.

A portal name is not a stable technical stack across years.

### 2.2 Basemap layer

The road/street geometry or map imagery rendered to the user.

Questions:

- raster or vector?
- pre-generated or dynamically rendered?
- image dimensions / zoom levels?
- update date?
- independent map-data provider?

### 2.3 POI index

Businesses, hospitals, government offices, schools, tourist attractions, residential compounds and other named places.

A POI hit is not the same object as the basemap.

### 2.4 Geocoder / name resolver

Converts a user-entered address, phone number, postcode, compound name or landmark into candidate locations.

### 2.5 Transit dataset

Bus stops, lines, transfer relationships, station names and sometimes schedule assumptions.

### 2.6 Routing engine

Computes a route through road/transit graph data.

Its algorithm and graph version can change without visible page redesign.

### 2.7 UI layer

Zoom, pan, search form, route form, marker popups, printable directions, share links, saved locations.

### 2.8 Capture

A memento of one URL at one time.

This may contain only the UI shell.

### 2.9 Real-world execution

The user physically tries to follow the route and reach a place that is actually present, open and accessible.

This state is normally outside the public web archive.

---

## 3. Core state chain

A route-planning interaction should be modeled as:

```text
public map page exists
→ required browser/plugin can load it
→ map assets load
→ user submits place/address query
→ query reaches backend
→ geocoder resolves candidate(s)
→ POI/location result returned
→ user selects destination
→ route request submitted
→ route engine accepts request
→ route graph/transit dataset queried
→ itinerary returned
→ itinerary displayed/printed/saved/shared
→ user leaves screen
→ user reaches correct starting point
→ roads/stops/services remain usable
→ user follows or adapts route
→ destination still exists and is accessible
→ user arrives
```

None of these arrows is safe to infer automatically.

---

## 4. Evidence anchor: 1999 Chinese online maps already had queryable place layers

A 1999-11-10 *China Reading Weekly / Zhonghua Dushubao* article described several Chinese online-map services.

For the Beijing map guide at `webgis.cei.gov.cn`, it described:

- zooming;
- panning;
- mapped hospitals, restaurants, bookstores and shops;
- searching by name, address, telephone and postcode.

It also described a Shenzhen tourist map that required installation of **Autodesk MapGuide Viewer 3.0** before viewing.

Source:
- https://www.gmw.cn/01ds/1999-11/10/GB/ds%5E274%5E0%5EDS1314.htm

Evidence grade: **B — contemporaneous media observation**.

What this proves:

- queryable Chinese web mapping existed in 1999;
- at least one implementation depended on a proprietary viewer;
- online maps could include searchable local-place metadata.

What it does not prove:

- mass use;
- exact DOM;
- exact charset;
- exact CGI endpoints;
- that the viewer still works in any archived capture;
- route accuracy;
- individual arrival outcomes.

---

## 5. Plugin/viewer gap

The Shenzhen example creates a concrete historical state gap:

```text
HTML capture survives
≠ Autodesk MapGuide Viewer installed
≠ viewer binary/version survives
≠ browser can instantiate viewer
≠ map data endpoint survives
≠ interactive map is reconstructable
```

A modern browser showing a blank rectangle is not evidence that the 1999 page was blank.

Conversely, replacing the missing viewer with a modern map must be labeled reconstruction, not replay.

Required evidence fields for a future capture:

```yaml
page_url:
capture_datetime:
charset:
viewer_or_plugin:
viewer_version_claimed:
plugin_object_or_embed_markup:
external_map_endpoint:
endpoint_capture_status:
modern_browser_result:
historical_browser_hypothesis:
reconstruction_used: false
```

---

## 6. 2000: online-map usefulness was constrained by connection cost and speed

A 2000-08-02 *Zhonghua Dushubao* article explicitly said online electronic maps shared a major problem: slow speed. It also noted that, while Internet access remained expensive, checking a map online could feel costly to ordinary users.

The same article described Go2Map embedding map services into other sites and conducting city data surveys including:

- government offices;
- companies;
- tourist sites;
- office buildings;
- universities;
- hospitals;
- cinemas;
- location/street distribution;
- bus transfer information;
- house numbers.

Source:
- https://www.gmw.cn/01ds/2000-08/02/GB/2000%5E311%5E0%5EDS1704.htm

Evidence grade: **B contemporaneous media**.

Archaeological implication:

> `feature present` and `interaction practically usable on a dial-up/time-priced connection` are different claims.

A historical replay on gigabit broadband silently removes a material part of the original experience.

Suggested reconstruction metadata:

```yaml
connection_assumption:
page_asset_bytes_known:
round_trip_requests_known:
plugin_download_required:
access_pricing_context:
```

Do not fabricate these values when they are unknown.

---

## 7. Embedded-map lineage gap

Go2Map's early business model included embedding or linking map functions into other portals/professional sites.

That means two URLs may present the same underlying geography while having different:

- wrapper HTML;
- branding;
- query parameters;
- upstream host;
- map-data host;
- capture coverage.

A dead embedded map on one portal may still be partially recoverable from another portal using the same map backend.

But this is a **hypothesis for evidence search**, not permission to declare two map experiences identical.

Required distinction:

```text
wrapper site identity
≠ map service provider
≠ map-data provider
≠ routing provider
≠ archive capture source
```

---

## 8. 2005: local search joined map, POI and route planning

SOHU's 2005 acquisition press release filed with the US SEC described Go2Map as a mapping solution provider with POI data across about 200 Chinese cities and delivery through Internet/Intranet platforms, mobile phones, call centers and PDAs.

Source:
- https://www.sec.gov/Archives/edgar/data/1104188/000119312505075385/dex991.htm

Evidence grade: **A for SOHU's formal platform/business claim**.

Do not upgrade this into user-adoption evidence.

A 2005-06-07 first-person test published by Sina is more useful for actual interaction. The tester described:

- draggable map interaction;
- markers with place name, address and telephone;
- nearby ATM search;
- bus transfer and driving-route links;
- using a residential compound/office building instead of knowing the precise bus-stop name;
- route results that sometimes required too many transfers or even went in the wrong direction.

Source:
- https://tech.sina.com.cn/i/2005-06-07/1018628634.shtml

Evidence grade: **B/C — contemporaneous first-person product test on a media platform**.

This produces two separate states that archives frequently collapse:

```text
route engine returns result
≠ route result is sensible
```

and:

```text
POI marker renders
≠ POI coordinate is correct
```

---

## 9. Geocoding gap

The move from exact bus-stop names toward natural place names introduces a hidden resolver state.

Example user input:

```text
"中关村某写字楼"
```

Possible historical states:

1. exact match;
2. alias match;
3. multiple candidate places;
4. fuzzy match;
5. nearby landmark substitution;
6. wrong city;
7. stale name;
8. no match.

An archived route URL may include only a numeric `pid`, coordinate or opaque query token. If the geocoder database has disappeared, the meaning of that token may no longer be recoverable from the HTML alone.

Therefore preserve, when observable:

```yaml
raw_query:
normalized_query:
resolved_label:
resolved_address:
resolved_coordinate:
opaque_place_id:
candidate_count:
```

Do not infer a modern coordinate from a current map and pretend it is the historical resolver output.

---

## 10. 2004/2006: rendering architecture changed performance and archive survivability

A 2006 industry report about Go2Map/Sogou stated that earlier Go2Map access had been slow, and that in 2004 it adopted a **pre-generated map** technical route to reduce server computation and improve access speed. The same report noted the tradeoff that pre-generation made some information-source display less flexible.

Source:
- https://www.taibo.cn/p/1598

Evidence grade: **B — contemporaneous industry report including company technical account**.

This matters archaeologically because a pre-generated raster-map system may leave:

- many small image resources;
- zoom-specific directories;
- server-side coordinate conventions;
- partial captures where HTML survives but tiles do not;
- map images that survive while query/backend services disappear.

Do not assume a modern slippy-map architecture for a 2004 service.

---

## 11. POI freshness gap

The same 2006 report explicitly identified map-data and basemap updating as a major problem and described user marking/correction mechanisms.

A 2008 public travel-forum thread provides a user-facing version of the same problem. A traveler preparing to visit newer Beijing architecture said older tourist-site information was plentiful but information about newer sites was limited, and asked for a site that could locate nearby bus/subway stations. Another participant recommended `51ditu.com`.

Source:
- https://www.backpackers.com.tw/forum/archive/index.php/t-70149.html

Evidence grade: **A/B — public contemporaneous user request and response**.

Core boundary:

```text
POI indexed at capture time
≠ place opened by that date
≠ name/address still current
≠ entrance location correct
≠ nearby transit data current
```

Future case work should record **map-data vintage** independently from page capture datetime wherever possible.

---

## 12. Route-URL survival gap

A 2008 Baidu Zhidao answer to a Beijing→Chengde driving question pasted a `51ditu.com` navigation URL containing encoded route parameters.

Source:
- https://zhidao.baidu.com/question/66478393.html

This is valuable old-web evidence because the answer preserves a route URL even if the route service itself no longer executes.

But a surviving URL proves only:

```text
someone shared this URL in 2008
```

It does not prove:

```text
current URL resolves
historical route output was archived
historical routing graph survives
historical encoded place IDs can be decoded
traveler followed the result
```

A future forensic task should capture:

```yaml
shared_url:
url_encoding:
query_parameter_names:
place_ids:
city_parameters:
transport_mode_parameter:
current_resolution:
wayback_capture_found:
historical_response_found:
```

---

## 13. Human-question / machine-route coexistence

Another 2008 Baidu Zhidao question asked how to travel within Shenyang. Respondents recommended Baidu Map and 51ditu rather than simply supplying a complete route.

Source:
- https://zhidao.baidu.com/question/43012527.html

This matters because a search engine/forum answer and a map system were not separate historical worlds.

A common chain was:

```text
user asks human community
→ respondent supplies local judgment
→ respondent links map tool
→ user moves to map system
```

Archive studies should therefore retain **cross-platform channel switching** instead of assigning a single platform as the complete routefinding system.

---

## 14. Search form success ≠ route success

Recommended state fields:

```yaml
query_submitted:
query_backend_response:
geocode_success:
route_request_created:
route_backend_response:
route_displayed:
route_printed_or_shared:
user_execution_known:
arrival_known:
```

For nearly all public captures, the last two fields should remain `unknown`.

---

## 15. Transit-route dataset gap

Bus route planning is especially vulnerable to historical misreading.

A route depends on:

- stop names at that date;
- stop coordinates;
- route direction;
- line extensions/retractions;
- temporary diversions;
- transfer rules;
- service hours;
- possibly fares;
- walking connection assumptions.

The 2005 Sina tester reported routes with excessive transfers or wrong-direction behavior. This is direct evidence that “algorithm returned an answer” must not be treated as “city was correctly modeled”.

When possible, compare a historical route result against independent contemporaneous transit evidence. Do not compare only against today's network.

---

## 16. Dynamic-map capture gap

A static capture may preserve:

- logo;
- search box;
- toolbars;
- textual copyright notice;

while losing:

- map tiles;
- marker overlays;
- drag behavior;
- zoom state;
- backend query response;
- route polyline;
- popup details.

Therefore use at least these distinct statuses:

```text
shell_saved
basemap_saved
interaction_code_saved
backend_response_saved
route_result_saved
```

Do not call `shell_saved` a “complete map capture”.

---

## 17. JavaScript interaction gap

By 2005, contemporaneous tests described draggable maps.

A screenshot can prove visual state but cannot independently prove:

- drag event handling;
- tile request pattern;
- browser compatibility;
- viewport clipping;
- marker hover behavior;
- whether dragging triggered a server request.

If interaction cannot be replayed, report it as:

> **UI behavior described by contemporaneous evidence; not independently replayed in this study.**

Do not recreate a modern draggable map and treat that as recovery.

---

## 18. 2011–2013: the web/mobile boundary becomes part of the object

By 2011–2013, mapping increasingly crossed desktop and phone contexts.

Contemporaneous evidence includes:

- 2011 Nokia web map coverage with PC/mobile synchronization claims;
- rapid growth of mobile-map accounts in 2011–2012 industry measurements;
- 2013 Sogou mobile map integrating bus, driving, walking and real-time traffic;
- 2013 Tencent Map 4.0 supporting WeChat login and synced favorites.

Sources:
- https://www.taibo.cn/p/15119
- https://news.cntv.cn/20120204/101919.shtml
- https://www.taibo.cn/p/25251
- https://news.mydrivers.com/1/286/286235.htm

Archaeological implication:

> **The historical “map page” may no longer contain the user's actual spatial state.**

Favorites, home/work locations and search history may live in authenticated account storage shared across devices.

This introduces:

- account-state gap;
- synchronization gap;
- device-state gap;
- mobile-only feature gap;
- web/mobile version skew.

---

## 19. Account / favorite gap

Possible chain:

```text
user views place anonymously
→ user logs in
→ user favorites place
→ favorite stored server-side
→ mobile client logs into same account
→ favorite syncs
→ user navigates from phone
```

A public Wayback capture normally sees only the first state.

Do not infer private favorites from a public marker or current account UI.

---

## 20. Pre-trip route vs en-route navigation

Old-web research should keep these distinct.

### Pre-trip route planning

Typical states:

- desktop browser;
- start/end form;
- textual itinerary;
- printable result;
- user leaves connection.

### En-route navigation

Typical states:

- device location;
- GPS fix;
- route recalculation;
- voice guidance;
- traffic state;
- device/network availability.

A 2011 article about smartphone GPS emphasized that phone maps could continuously show the user's current location.

Source:
- https://tech.sina.com.cn/s/2011-05-18/09065539245.shtml

Do not retroactively describe a 1999 web map as “navigation” merely because it showed routes.

---

## 21. Real-time traffic gap

Once route advice incorporates traffic, another historical clock appears.

A route result may depend on:

```text
road graph version
+ traffic observation timestamp
+ traffic-data coverage
+ routing algorithm version
+ user request timestamp
```

The page capture datetime alone is not enough.

A 2013 Sogou release claimed real-time traffic-informed route suggestions.

Source:
- https://www.taibo.cn/p/25251

Without the historical traffic feed, a later replay cannot reproduce the original recommendation even if the map and software survive.

---

## 22. Real-world-state gap: 2020 confirms a structural problem visible before 2015

The repository scope ends around 2015, but one later event is useful as a boundary demonstration, not as a scope extension.

On 2020-01-25, reports that Beijing expressways were closed circulated online. A contemporaneous New Beijing News verification found that some map/navigation displays indicating closure did not match on-site information from checkpoints, which remained open.

Source:
- https://news.sina.cn/gn/2020-01-25/detail-iihnzhha4608266.d.html

This later case clarifies a state gap already present throughout old-web mapping:

```text
routing/map database state
≠ legal traffic state
≠ physical road state
≠ on-site enforcement state
```

The 2020 example should not be written as a 1999 fact; it demonstrates why earlier route results also require caution.

---

## 23. Map page survival can create false spatial certainty

An archived result often looks authoritative:

- precise marker;
- street name;
- numbered route steps;
- distance;
- estimated path.

This precision can be misleading.

The archive may not preserve:

- uncertainty in geocoding;
- alternative candidate addresses;
- stale POIs;
- route-graph age;
- temporary closure;
- whether the place entrance was elsewhere;
- whether a user trusted/followed the result.

Therefore add a standard warning to any reconstructed route case:

> **Rendered precision is not evidence of historical ground-truth accuracy.**

---

## 24. Proposed gap taxonomy

### 24.1 `plugin/viewer gap`

HTML survives; required viewer/runtime does not.

### 24.2 `basemap-asset gap`

Page shell survives; map images/tiles do not.

### 24.3 `geocoder gap`

Search form survives; address/name resolution backend does not.

### 24.4 `POI freshness gap`

A point exists in database but may already have moved/closed/renamed.

### 24.5 `place-ID semantic gap`

Opaque historical IDs survive in URLs without recoverable meaning.

### 24.6 `route-engine gap`

UI and endpoints survive, but routing graph/algorithm cannot be reconstructed.

### 24.7 `transit-version gap`

Bus/rail network shown cannot be tied to a precise service date.

### 24.8 `real-time-feed gap`

Historical traffic/weather/closure feed is absent.

### 24.9 `interactive-state gap`

Screenshot/HTML survives; pan/zoom/hover/selection state does not.

### 24.10 `cross-device state gap`

Public web capture lacks account favorites/sync/mobile state.

### 24.11 `route-share gap`

A shared URL survives, but generated itinerary does not.

### 24.12 `real-world execution gap`

Route result survives; actual trip outcome is unknown.

### 24.13 `destination-status gap`

POI survives; physical business/institution availability is unknown.

### 24.14 `map-data vintage gap`

Capture date is known but underlying basemap/POI dataset date is not.

---

## 25. Evidence grading used in this note

| Evidence | Date | Grade | Strongest supported claim |
|---|---:|---|---|
| Zhonghua Dushubao online-map guide | 1999 | B | queryable maps and MapGuide dependency existed |
| Zhonghua Dushubao digital-map article | 2000 | B | speed/access-cost limits and Go2Map embedded service model |
| SOHU SEC filing/press release | 2005 | A (company claim) | Go2Map formal business/data capabilities |
| Sina first-person local-search test | 2005 | B/C | actual UI behavior and route errors observed by tester |
| Go2Map/Sogou industry report | 2006 | B | pre-generation technique and update problem described |
| Backpackers Beijing thread | 2008 | A/B | contemporaneous traveler demand and 51ditu recommendation |
| Baidu Zhidao route questions | 2008 | A/B | users publicly shared/recommended map-route services |
| Nokia/Sogou/Tencent mobile-map reports | 2011–13 | B/A platform claims | web/mobile sync, mobile route and traffic features |
| 2020 road-state verification | 2020 | B, boundary example | map state and on-site state can diverge |

No source in this table establishes population-level adoption by itself.

---

## 26. Archive search performed this round

Search work attempted:

- public web search for Go2Map 1999–2001 historical captures;
- public references to Wayback captures;
- contemporaneous media references preserving historical URLs.

Result:

- contemporaneous URLs and functional descriptions were found;
- no **independently verified, replayed 1999–2001 Go2Map/Beijing-map capture** was obtained in this run;
- a direct Wayback CDX open attempt was not usable through the current web-access path.

Therefore this note does **not** claim:

- exact historical Go2Map DOM;
- exact charset;
- CGI/ASP action URLs;
- MapGuide object markup for the Shenzhen service;
- preserved route-query responses;
- preserved tile sets.

This negative result is part of the archaeological record, not a reason to invent reconstruction details.

---

## 27. Browser/environment hypotheses for future testing

These are **questions, not findings**:

- Did the 1999 Beijing map guide depend on JavaScript features specific to IE/Netscape versions?
- Was GB2312 declared in HTTP headers, META, or both?
- Did the Shenzhen MapGuide page use `<OBJECT>`, `<EMBED>`, ActiveX classid or Netscape-style plugin detection?
- Did later Go2Map/Sogou use pre-generated raster images with server-side coordinates or early Ajax/slippy-map interaction?
- Were route results generated server-side as HTML, client-side from structured data, or hybrid?

Do not answer these from present-day service behavior.

---

## 28. Privacy and copyright boundary

Map research is usually less privacy-sensitive than old personal pages, but it can still expose:

- home addresses in shared route URLs;
- personally saved places;
- account favorites;
- historical search logs;
- movement traces.

Do not republish private route histories or authenticated account data merely because a leaked/archive endpoint exists.

For copyrighted map imagery:

- prefer citation and metadata;
- use tiny excerpts only when legally justified;
- do not commit bulk tiles or commercial basemap archives without permission.

---

## 29. Reconstruction rules for one future complete case

A reconstruction of a historical map query must say exactly which layer is original.

Example:

```yaml
historical_html: archived
historical_css: archived
historical_map_images: partial
historical_javascript: missing
historical_plugin: missing
historical_query_response: missing
historical_route_graph: missing
modern_basemap_substitution: none
researcher_reconstruction: only annotated screenshots of surviving state
```

If a modern basemap is used to explain geography, label it **modern reference**, never historical replay.

---

## 30. Cross-repository interpretation

For `how-people-lived`, the historical implication is not “maps got better”.

It is that ordinary people gradually gained **pre-arrival legibility of unfamiliar cities**:

- places became searchable;
- route computation became externalized;
- navigation moved from pre-trip planning to continuous in-trip guidance;
- commute time could become a variable in housing/career planning.

For this repository, the complementary conclusion is:

> **The more useful a map service became in ordinary life, the more of its decisive state tended to live outside the archivist's visible HTML — in databases, routing engines, authenticated accounts, live feeds and the physical city itself.**

---

## 31. Next high-value evidence target

Do not broaden immediately into “all Chinese maps”.

The highest-value next slice is one **1999–2005 historical map interaction** with a real capture and enough dependencies to answer:

1. original URL;
2. capture datetime;
3. charset;
4. browser assumptions;
5. plugin/runtime requirement;
6. basemap asset URLs;
7. search form fields;
8. route/geocode endpoint;
9. one query response;
10. missing dependencies;
11. whether interaction can be replayed in period-appropriate browser conditions.

Priority candidates:

- `webgis.cei.gov.cn` Beijing map guide;
- early Go2Map;
- 51ditu route output;
- early Sogou Map beta.

A formally documented failure to recover the backend is an acceptable outcome.

---

## 32. Current conclusion

### Confirmed

- queryable Chinese web maps existed by 1999;
- proprietary viewer dependence existed in at least one 1999 Chinese map service;
- speed/access cost constrained early online-map practicality;
- by 2005, local search could combine POIs, address/telephone metadata, bus transfers and driving routes;
- contemporaneous testing already found route-quality errors;
- map-data freshness was an acknowledged problem;
- by 2008 users publicly linked route URLs and recommended electronic-map sites in ordinary questions;
- by 2011–2013 map state increasingly crossed web/mobile/accounts and incorporated location/traffic.

### Strong inference

- public archives systematically preserve map **presentation layers** better than private/runtime/backend/real-world execution states;
- route-result pages are especially vulnerable to false certainty because they visually encode precision even when underlying data vintage is unknown.

### Unknown

- exact 1999–2003 DOM/charset/request architecture for the priority sites;
- completeness of surviving map images/tiles;
- historical geocoder and route-engine versions;
- exact relationship among wrapper portals and shared Go2Map backends at specific dates;
- user arrival outcomes for almost all preserved public route requests.

This uncertainty should remain visible until capture-level evidence resolves it.