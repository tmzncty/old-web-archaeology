# SUPPORT_PAGES_DOWNLOAD_ARTIFACTS_REPAIR_REQUESTS_AND_OUTCOME_GAPS_2005_2015.md

Status: methodology / research note  
Scope: Chinese Web support/repair artifacts roughly 2005–2015; vendor support pages, driver/download pages, forums, service-locator/online-repair entry points and the state gaps between public Web evidence and physical repair outcome.  
Companion ordinary-life note: `tmzncty/how-people-lived/topics/repair-time-maintenance-debt-remote-diagnosis-and-household-uptime-china-1987-2025.zh-CN.md`.

## 1. Why repair/support pages need their own archaeology

Old-Web preservation frequently leaves a page saying:

- “download driver”;
- “online repair”;
- “find service center”;
- “read manual”;
- “submit request”;
- “this patch fixes the problem”.

Those phrases can look like complete technical evidence, but in ordinary use they were only entrances to longer state chains.

The archaeological question is not merely:

> Did a support page exist?

It is:

> Could a user with a particular device, hardware revision, operating system, warranty state and location actually move from that page to a working machine?

Therefore the unit of analysis must keep **public support content**, **download artifacts**, **authenticated service state**, **physical logistics** and **repair outcome** separate.

---

## 2. Minimum state model

For a hardware/software repair route, use a chain such as:

```text
product/device exists
→ user identifies model/revision
→ support page found
→ warranty/entitlement known
→ troubleshooting instruction selected
→ driver/manual/firmware or repair request selected
→ artifact actually downloadable / request actually submitted
→ artifact matches device/version OR request accepted
→ local action / technician assignment
→ spare part available
→ repair performed
→ device tested
→ user accepts outcome
→ later reliability observed
```

Do not collapse any adjacent pair.

Hard boundaries:

- `support page exists ≠ linked artifact survives`;
- `download link exists ≠ file downloaded successfully`;
- `file downloaded ≠ file is correct for this device`;
- `forum answer exists ≠ user followed it`;
- `online form submitted ≠ backend ticket accepted`;
- `ticket accepted ≠ technician dispatched`;
- `technician dispatched ≠ technician arrived`;
- `technician arrived ≠ part available`;
- `part replaced ≠ device fixed`;
- `device works at departure ≠ repair remains good`.

---

## 3. 2005–2007: downloadable repair knowledge becomes a Web artifact

Chinese technology media in the mid-2000s routinely linked readers to exact driver/software downloads.

A February 2006 Sina Technology page syndicated from 驱动之家 described a ForceWare beta driver and provided separate download routes for Windows 2000/XP and Windows XP-64 while listing supported GPU identifiers.

Contemporary page:  
<https://tech.sina.com.cn/s/s/2006-02-05/0952832829.shtml>

A December 2006 page discussing NVIDIA's driver architecture also explicitly referred to vendor-side separation of GeForce 8800 and older GeForce/TNT driver downloads.

Contemporary page:  
<https://tech.sina.com.cn/h/2006-12-05/1912179872.shtml>

These pages matter because a Web-era repair path can depend on a **binary artifact**, not just readable prose.

For archaeology, preserve this distinction:

```text
article HTML survived
↓
anchor text says “download”
↓
linked URL known
↓
server response at capture time known
↓
actual binary archived
↓
hash / file identity known
↓
binary corresponds to stated version
```

Most archives stop somewhere in the middle.

This is the **download-artifact gap**.

### Historical claim allowed

A contemporary page can prove that a particular driver/version was being distributed or discussed through Web links.

### Claim not allowed without the artifact

- that the historical download file is preserved;
- that the link returned the claimed binary at the relevant time;
- that the file was unmodified;
- that it actually fixed a specific user's machine.

---

## 4. Version and revision are first-class evidence

Support archaeology must record, when available:

- product family;
- exact model;
- hardware revision;
- serial-range applicability;
- operating system;
- architecture (`x86`, `x64`, etc.);
- firmware/BIOS version;
- driver version;
- release/build date;
- locale/language;
- prerequisite software;
- checksum or file size if historically available.

A surviving “latest driver” page is dangerous historical evidence because **latest is time-relative**.

A 2007 capture and a 2011 capture of the same URL can legitimately point to different binaries.

Therefore:

> `same URL ≠ same repair artifact`.

Call this the **mutable-support-target gap**.

---

## 5. 2007 HP China community: public forum evidence is not the repair backend

A surviving HPE community thread dated 2007-10-11 announced an HP China “online repair” promotion and linked users to online repair routes for Unix servers/storage and industry-standard servers. The post instructed users to read the rules and “how to repair/report” material before participating.

Historical corporate community page:  
<https://community.hpe.com/t5/%E5%B7%A5%E4%B8%9A%E6%A0%87%E5%87%86%E6%9C%8D%E5%8A%A1%E5%99%A8/hp%E7%BD%91%E4%B8%8A%E6%8A%A5%E4%BF%AE%E6%9C%89%E5%A5%96%E6%8E%A8%E5%B9%BF-10-%E6%9C%88%E8%8E%B7%E5%A5%96%E5%90%8D%E5%8D%95%E5%85%AC%E5%B8%83/td-p/1223448>

The present page is wrapped in a current HPE community interface. The post date and text are useful historical content, but the current rendering is not a 2007 browser experience.

More importantly, the public thread is only evidence that an online-reporting route existed.

The linked historical domains (`e-support.hp.com.cn/...`) were a separate service surface.

The following states must remain distinct:

```text
public forum post
→ linked online-repair URL
→ login/account state
→ eligible product
→ form completed
→ backend request ID issued
→ case accepted
→ engineer/partner assigned
→ repair outcome
```

A public community capture does not reveal the authenticated case database.

This is the **public-support / private-ticket gap**.

---

## 6. 2009 consumer appliance support: Web entry + physical service

A 2009 report on Samsung's refrigerator recall described two consumer routes in China: the company could proactively contact known customers, while users could also register by telephone or through a dedicated “online repair” page on Samsung China's website. Users were expected to provide contact details, address and refrigerator model; a technician would later perform the physical repair.

Contemporary report:  
<https://news.sohu.com/20091109/n268064496.shtml>

A separate March 2009 comparison of flat-panel-TV after-sales policies described Haier's official site as exposing:

- hotline information;
- fee standards;
- an online repair window;
- product manual downloads;
- service-process descriptions.

Contemporary page:  
<https://digi.it.sohu.com/20090311/n262739656_4.shtml>

These sources show that by 2009 a consumer support website could join several previously separate information systems.

But the Web page still did not contain the whole repair.

Recommended state split:

```yaml
public_support:
  support_page_visible:
  fee_schedule_visible:
  manual_locator_visible:
  online_repair_entry_visible:

private_case:
  account_required:
  identity_or_contact_submitted:
  product_model_submitted:
  warranty_state_known:
  request_id_issued:
  appointment_window:

physical_service:
  technician_assigned:
  technician_arrived:
  correct_part_available:
  repair_performed:
  repair_accepted:
```

---

## 7. Support knowledge can outlive the institution responsible for repair

A 2008 Economic Information Daily report on “orphan appliances” described products whose brands or manufacturers had exited or failed, leaving users with devices and warranty cards but no viable original support route.

Contemporary report:  
<https://www.chinanews.com.cn/cj/xfsh/news/2008/05-22/1258691.shtml>

This creates an old-Web problem that differs from ordinary link rot.

A preserved support page may represent an institution that later ceased to be able to provide the promised service.

Therefore distinguish:

- `historical service promise existed`;
- `service organization existed at that date`;
- `service organization still existed when the user's product failed`;
- `required spare part still existed`;
- `some third party later reused the brand/domain`.

Call this the **service-authority lifecycle gap**.

A domain surviving into a later period does not prove continuity of service authority.

---

## 8. Public repair forums preserve advice, not success

Forums and technology communities can preserve very fine-grained failure descriptions:

- exact error message;
- unusual symptom;
- hardware revision;
- workaround;
- unofficial driver;
- attached patch;
- another user's result.

They are valuable because official manuals often omit rare failures.

But forum evidence requires an outcome ladder:

```text
question posted
→ reply posted
→ proposed solution technically plausible
→ attachment/link available
→ original poster tried it
→ original poster reported success
→ success persisted
```

A thread ending with “try this driver” is **not** evidence of repair success.

If the original poster never returns, record `outcome = unknown`.

This is the **forum-outcome gap**.

---

## 9. Attachments are often more fragile than threads

Old technical forums frequently preserve the text shell while losing:

- uploaded images;
- zipped patches;
- BIOS files;
- drivers;
- logs;
- schematics;
- external image-host screenshots;
- FTP links.

For each support thread, separately record:

```yaml
thread_html_survives:
inline_images_survive:
attachments_listed:
attachments_downloadable:
external_links_resolve:
file_hash_known:
file_version_known:
```

A thread with a missing screenshot may become impossible to interpret if replies say only “set it like this”.

A thread with a missing binary may retain explanation but lose executability.

Call this **executable-knowledge loss**.

---

## 10. 2010–2015: support pages become increasingly transactional

During this period, support websites increasingly combined information with account and transaction state:

- warranty lookup;
- serial-number entry;
- repair booking;
- service-center lookup;
- repair-progress query;
- downloadable manuals/drivers;
- community Q&A.

The archaeological consequence is important:

> The more useful the support system became to an individual user, the more important states moved behind forms, cookies, accounts and databases that public Web archives rarely capture.

Public preservation therefore becomes **less representative of actual service execution** even while the public website looks richer.

A screenshot of a polished support home page may preserve less of the user's real repair route than an older static page containing a direct telephone number and downloadable PDF.

---

## 11. Historical browser/environment caution

Support pages are unusually sensitive to runtime assumptions.

Potential dependencies include:

- IE-only form validation;
- ActiveX diagnostic controls;
- Java/Flash upload widgets;
- popup windows;
- vendor download managers;
- login cookies;
- dynamically generated serial-number fields;
- GB2312/GBK form encoding;
- FTP download URLs;
- HTTPS/TLS versions unsupported by old browsers;
- executable installers signed with expired certificates.

A modern browser successfully displaying archived text does not prove a historical user could complete the original support transaction.

Record **browser assumption** and **transaction assumption** separately.

---

## 12. Repair-progress pages are especially hard to archive

A repair-status page may expose states such as:

```text
received
→ diagnosing
→ waiting for part
→ repairing
→ testing
→ ready for pickup / dispatch
→ closed
```

But these are usually authenticated and tied to serial numbers, phone numbers, case IDs or customer accounts.

Do not seek or republish historical personal repair records merely to fill the archive gap.

The absence of such pages in public archives is partly an appropriate privacy boundary.

Call this the **authenticated-repair-ledger gap**.

---

## 13. Physical outcome remains off-Web

Even a perfectly preserved repair ticket usually cannot prove:

- technician actually entered the home;
- correct part was installed;
- old part was returned;
- machine passed a realistic workload test;
- consumer accepted the bill;
- repair remained stable for weeks/months;
- user later replaced the product anyway.

Therefore the final nodes remain ordinary-life evidence, not pure Web evidence.

The Old-Web repository can document the **interface and state claims**. `how-people-lived` should document what those states meant for the household day.

---

## 14. Overseas comparison: CompuServe shows remote support predates the Web

A 1990 CompuServe new-member magazine described a layered help route using guides, online help, questions-and-answers databases, forum managers and Customer Service.

Contemporary source locator:  
<https://vtda.org/pubs/CompuServe_Magazine/CompuServe_Magazine_1990-NewMember.pdf>

A 1987 Borland Turbo C manual, quoted in a later historical discussion, directed users first to Borland's CompuServe forum (`GO BOR`) for support, with letter and telephone routes also available.

Locator / later discussion:  
<https://retrocomputing.stackexchange.com/questions/1818/how-were-bugs-reported-for-compilers-that-were-shipped-on-floppy-disks>

The comparison matters methodologically:

- remote technical support is older than the Web;
- public network support can coexist with phone and postal channels;
- forum archives preserve shared troubleshooting better than one-to-one calls;
- moving from proprietary online service to Web can itself break historical continuity.

Do not insert CompuServe into this repository's Chinese-old-Web object corpus; use it only as comparative method in the companion life-history analysis.

---

## 15. Evidence grading for this slice

### A / strong historical artifact

- surviving HPE corporate-community post dated 2007 showing online-repair campaign and historical e-support links.
- 1995 Chinese national three-guarantees normative text as an official institutional source for what repair records, parts and responsibility were supposed to exist.

### B / contemporary secondary evidence

- 2005–2009 technology-media pages describing driver/download routes, support functions, consumer repair cases and online repair interfaces.
- contemporary recall reporting describing phone/Web registration followed by physical service.

### C / later retrospective lead

- current sites describing their own long history or old support-database size without independently preserved historical captures.

### D / reconstruction

- any inferred historical form fields, DOM, CSS, browser requirements, database schema, attachment identity or backend workflow that is not directly evidenced.

---

## 16. Negative result in this round

This round did **not** verify a complete 2005–2010 Chinese consumer support session that preserves all of the following together:

1. public product/support page;
2. exact device/revision selection;
3. authenticated online-repair form;
4. issued case ID;
5. repair-progress states;
6. final physical outcome.

It also did not verify a historical archived copy of the original binary behind the selected Driver Home download links.

Therefore this note does not reconstruct historical DOM, CSS, charset, account fields, ticket schema, executable hashes or real individual repair outcomes.

---

## 17. Reusable evidence schema extension

Suggested fields:

```yaml
support_object:
  vendor:
  product_family:
  exact_model:
  hardware_revision:
  serial_range_known: false

web_artifact:
  original_url:
  capture_url:
  capture_datetime:
  charset:
  browser_assumption:

support_role:
  type: manual|driver|firmware|forum|service-locator|repair-form|status-page

version_state:
  os:
  architecture:
  driver_version:
  firmware_version:
  build_or_release_date:

linked_artifact:
  url:
  archived: false
  downloadable_now: false
  hash_known: false

repair_request:
  authenticated: unknown
  submitted: unknown
  accepted: unknown
  case_id_issued: unknown

physical_state:
  technician_assigned: unknown
  part_available: unknown
  repaired: unknown
  user_accepted: unknown
  long_term_outcome: unknown

claim_supported:
claim_not_supported:
unknowns:
```

---

## 18. What this adds to old-Web archaeology

Repair/support pages expose a broader rule for dynamic historical systems:

> **A public Web page can preserve the instruction to change reality without preserving whether reality changed.**

For support history this means:

- the page says a driver exists, but the binary may be gone;
- the form says a repair can be requested, but the private ticket is invisible;
- the status system says a part is waiting, but the physical warehouse is outside the Web;
- the forum says “try this”, but the user may never report back.

This is not an archival failure to be papered over with guesses. It is part of the historical object.

The durable research question is therefore not merely “what support website existed?” but:

> **Which portions of repair knowledge, entitlement, transaction state and physical outcome were actually Web-visible, and which disappeared behind binaries, authentication, logistics or private household space?**
