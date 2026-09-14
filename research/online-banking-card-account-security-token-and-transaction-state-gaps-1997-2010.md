# Online banking, card-account access, security tokens and transaction-state gaps, 1997–2010

> Status: research / state-gap note, **not an M1 complete archaeology case**.  
> Primary old-Web scope: Chinese bank Web portals, online-banking authentication, merchant/payment integration, and the client-side/security-token layers that made a historical Web transaction executable.  
> Companion ordinary-life note: `tmzncty/how-people-lived/sources/from-carrying-wages-home-to-networked-money-remittance-bank-cards-and-remote-banking-china-1986-2010.zh-CN.md`.

## 0. Why this belongs in old-web-archaeology without turning the repository into a banking-history project

The companion repository handles postal remittance, ATM/card portability, migrant-worker remittance and branch/time decoupling as ordinary-life financial infrastructure.

This repository takes only the slice where bank-account state acquired a Chinese Web surface:

> **A historical bank page could let a user query or mutate account state, but the transaction depended on off-Web provisioning, physical credentials, browser-specific client software, bank backends and sometimes a second merchant platform.**

That creates an archaeology problem different from a static homepage. Even a complete HTML capture can preserve the public interface while losing nearly everything that made the historical transaction executable.

This note therefore does **not** try to write a general history of Chinese banking. Postal remittance, rural credit outlets, ATM networks and migrant-worker card services are preconditions or comparative boundary evidence only when they explain what the Web layer changed.

---

## 1. Evidence contract and research units

`docs/METHOD.md` applies without exception.

Keep these objects separate:

- **bank / service**: e.g. ICBC personal online banking;
- **site / host**: public bank portal, login host, payment host;
- **page / URL**: product page, login page, help page, merchant-binding guide;
- **customer account**: one bank-account relationship;
- **online-banking provisioning state**: whether the account was enabled for Web use;
- **security credential**: password, certificate, USBKey/U盾, code card or other historical credential;
- **client environment**: browser, ActiveX/control, driver, patch, trusted-site configuration;
- **merchant integration**: e.g. Alipay invoking or relying on bank authentication;
- **transaction request**: one user-submitted operation;
- **bank authorization state**: whether the bank accepted the operation;
- **merchant/application state**: whether a second platform recorded the result;
- **clearing/settlement state**: whether value actually moved and finalized;
- **capture / artifact**: one archived or currently observed representation;
- **claim**: a narrow statement supported by evidence.

Minimum distinction:

```text
login page survives
!= account exists
!= online banking provisioned
!= credential valid
!= client environment executable
!= request submitted
!= bank authorized
!= merchant recorded success
!= funds finally settled
```

The exact internal state machine varies by institution and period. Unless a contemporary manual or protocol document establishes a state, treat the intermediate sequence as a research model, not a recovered implementation.

---

## 2. Historical service identity: website, telephone banking and online banking arrived as overlapping channels

ICBC's institutional history records the following sequence:

- December 1997: ICBC website opened;
- 1999: nationwide unified telephone-banking number `95588` launched;
- 2000-02-01: online banking opened in Beijing, Tianjin, Shanghai and Guangzhou;
- August 2000: personal online banking and Peony Card B2C online-payment functions were introduced;
- 2002: telephone, online and other electronic channels were reorganized under electronic banking;
- 2003-12-18: the `金融@家` electronic-banking brand was launched.

Source:

- ICBC institutional history, `工商银行电子银行引领金融服务走进e时代`  
  https://www.icbc.com.cn/icbc/%E5%8C%97%E4%BA%AC%E5%88%86%E8%A1%8C/%E5%88%86%E8%A1%8C%E5%8A%A8%E6%80%81/%E5%B7%A5%E5%95%86%E9%93%B6%E8%A1%8C%E7%94%B5%E5%AD%90%E9%93%B6%E8%A1%8C%E5%BC%95%E9%A2%86%E9%87%91%E8%9E%8D%E6%9C%8D%E5%8A%A1%E8%B5%B0%E8%BF%9Be%E6%97%B6%E4%BB%A3.htm

**Evidence grade: B.** This is an institutional retrospective useful for product/service chronology. It is not a verified 1997 or 2000 Web capture.

The safe conclusion is therefore not “Chinese banking moved from branches to the Web in 2000.” The channels overlapped:

```text
branch counter
+ ATM/card network
+ telephone banking
+ Web banking
+ later mobile channels
```

For archaeology, this means a Web page is one interface era inside a larger multi-channel account system.

---

## 3. A live-legacy 2006 path: ICBC UShield + Alipay integration still exposes a historical workflow

A current ICBC server still directly returns the following old path:

`https://www.icbc.com.cn/icbc/html/guanggao/2006nian/0523/images/zfb_060522.html`

The page describes a UShield / Alipay workflow in which:

- the user must first take valid identity documents to an ICBC branch;
- personal online banking must be opened and UShield applied for;
- a UShield driver / relevant patch must be installed on the PC;
- the certificate may be downloaded by a teller or by the user through personal online banking;
- if self-download fails, the user is instructed to return to a branch;
- when the UShield is inserted and its password entered, Alipay recharge, withdrawal and account-management functions become available;
- without the UShield, the described path allows only query-type functions.

Source:

- ICBC current live-legacy page, historical-content path under `2006nian/0523`:  
  https://www.icbc.com.cn/icbc/html/guanggao/2006nian/0523/images/zfb_060522.html

**Evidence grade: A-content / live-legacy artifact, with a major temporal warning.** We can verify the page representation now. The path and content strongly identify a 2006-era document, but this run has **not** verified a 2006 archive capture, original HTTP headers, original DOM, original subresource state, or that the current representation is byte-identical to what users saw in 2006.

Therefore preserve:

```text
current server exposes a historical-content page at a 2006 path
```

separately from:

```text
this exact HTML is a verified 2006 memento
```

The latter is **not achieved**.

---

## 4. State gap 1: `off-Web provisioning state`

The 2006 ICBC page explicitly requires the customer to visit a physical branch with valid identification to open personal online banking and apply for UShield.

That means a future historical login-page capture cannot tell us whether a specific account was actually permitted to use the service.

Minimum distinctions:

```text
public login URL exists
!= customer registered for online banking

customer has bank account
!= online banking enabled

online banking enabled
!= UShield issued
```

This matters because ordinary-life executability begins before the browser session. A Web service can be geographically remote at transaction time while still depending on an earlier face-to-face provisioning event.

Call this:

### `off-Web provisioning state`

For a complete archaeology case, provisioning rules should be reconstructed from contemporary bank manuals / help pages rather than inferred from a modern login screen.

---

## 5. State gap 2: `security-token state`

A historical UShield was not merely a picture of a USB device shown on a Web page. The executable state could include:

- a physical token possessed by the customer;
- a certificate installed or downloaded to the token;
- a binding between credential and customer/account;
- a token password/PIN known to the customer;
- certificate validity and revocation status;
- bank-side trust in that certificate;
- client-side middleware capable of reaching the device.

The 2006 ICBC page directly confirms that driver installation, certificate download and a UShield password were part of the described customer workflow. It also says failed certificate self-download could require a return to the branch.

Therefore:

```text
UShield icon / help page survives
!= historical private key survives
!= certificate was issued
!= certificate was valid
!= certificate was bound to account X
!= user knew the token password
```

### `credential survival != credential executability`

A preserved token photograph, driver package or certificate-control UI can be valuable historical evidence without making any real historical credential executable again.

Privacy/security rule: **do not seek or republish real private keys, account-bound certificates, token PINs or credentials from ordinary users.** Public manuals, demo material and software metadata are sufficient for archaeology.

---

## 6. State gap 3: `client-environment state`

Old online banking made the user's own PC part of the transaction environment.

The 2006 UShield/Alipay page already requires a driver and patch. ICBC also currently preserves an installation guide instructing users to:

- use Internet Explorer;
- download/install ICBC online-banking client controls;
- add ICBC/MyBank hosts to trusted sites;
- enable ActiveX-related settings;
- adjust popup-blocking behavior;
- follow compatibility instructions for IE6/IE7/IE8/IE9.

Source:

- ICBC, `个人网上银行控件安装指南` (current live support artifact):  
  https://www.icbc.com.cn/icbc/html/download/grwangyinanzhuang.htm

**Evidence grade: A for the currently observable support page; historical date uncertain unless separately established.** It demonstrates the kind of client dependency ICBC continued to support, but must not be silently dated to 2006.

For 2006-specific claims, use the UShield/Alipay page itself, which directly says drivers/patches are required.

### Archaeological consequence

A modern Chromium screenshot of a historical banking page cannot be assumed to represent historical executability.

Relevant variables may include:

- IE version;
- Windows version;
- ActiveX/control availability;
- control signing/trust;
- UShield middleware/driver version;
- USB support;
- certificate store behavior;
- JavaScript/browser sniffing;
- popup settings;
- charset;
- TLS/cipher compatibility.

This makes early online banking a strong future M3 browser-environment experiment candidate, but **not** an excuse to recreate or execute real financial transactions.

---

## 7. State gap 4: `cross-site credential projection`

The 2006 ICBC page is especially useful because the same bank-issued physical credential is projected into an external platform workflow: Alipay.

The page describes a path where inserting UShield and entering the UShield password enables recharge, withdrawal and account-management actions associated with the Alipay account.

This yields a new archaeology unit:

### `cross-site credential projection`

```text
bank issues credential
→ bank binds credential to banking identity
→ external platform invokes / relies on bank authentication path
→ one physical credential participates in a second site's transaction workflow
```

A historical Alipay page and a historical ICBC page therefore may represent different surfaces of one transaction.

This is not the same as ordinary hyperlinking.

It also means that a future “platform reconstruction” cannot assume the external platform alone contained all of the authentication state necessary to perform the historical action.

---

## 8. State gap 5: `account-state invisibility`

A public archived bank page may preserve:

- login form labels;
- navigation;
- help text;
- product descriptions;
- screenshots or demo images;
- JavaScript and controls.

It normally will **not** preserve an ordinary customer's authenticated account state, and should not be made to do so.

Potential private state includes:

- account numbers;
- balances;
- transaction history;
- beneficiaries;
- identity details;
- certificate bindings;
- security questions / phone numbers;
- pending transfers.

For this repository:

> **Authenticated ordinary-user bank data is not a desirable archaeology target.**

M1/M3 evidence should prefer public demo accounts, public help pages, training screenshots, manuals, test systems and redacted structural evidence.

### Privacy boundary

Do not republish abandoned authenticated sessions, leaked statements, real beneficiary lists or historical credentials merely because they appear reachable.

The research value lies in reconstructing interface and state structure, not exposing private finances.

---

## 9. State gap 6: `authorization != settlement`

A browser can display a confirmation page without exposing every backend state in the movement of money.

A conservative generic model is:

```text
user enters instruction
→ client authenticates/signs
→ request reaches bank
→ bank validates account / credential / limits
→ bank accepts or rejects instruction
→ merchant/application may receive a result
→ clearing/settlement processes may follow
```

**Evidence grade: D as a generic analytical model unless a period-specific bank protocol/manual confirms the exact state sequence.**

Do not project this exact ordering onto every ICBC transaction.

The archaeological rule is narrower and safe:

```text
visible “success” representation
!= proof that every later financial state completed exactly as assumed
```

When a future capture says “交易成功”, the note must ask what that period's documentation defines as success: request accepted, account debited, merchant credited, or final settlement.

This is the financial equivalent of other dynamic-Web state gaps, but with higher stakes and stronger privacy/security boundaries.

---

## 10. State gap 7: `merchant-bank state divergence`

The UShield/Alipay integration makes a two-system problem visible.

Possible state divergence includes:

```text
bank accepted operation
but merchant page failed to refresh
```

or:

```text
merchant generated payment request
but bank rejected authentication
```

or:

```text
browser lost connection after submission
while one backend already changed state
```

The 2006 page confirms cross-platform integration, but this run has **not** recovered a contemporary technical document proving the exact failure semantics, retry rules or reconciliation workflow. Those examples therefore remain **D-level failure models**, not claims about a specific ICBC/Alipay transaction.

Future evidence targets:

- bank/merchant help pages describing duplicate payment, timeout or pending states;
- payment-interface manuals;
- contemporary user troubleshooting;
- public demo transaction flows.

---

## 11. New archive mechanism: `live-legacy survival fragmentation`

The current ICBC server produces a useful preservation contrast:

- the 2006 UShield/Alipay path above still opens;
- another old UShield demo path discovered during search currently returns 404;
- a historical code-card page discovered through search currently returns 403.

This should **not** be rewritten as “one was preserved and two were never archived.” It only proves current live-server accessibility differs.

Call this:

### `live-legacy survival fragmentation`

```text
search index knows historical-looking path
!= current server returns it

current server returns it
!= historical Web archive captured it

current 404/403
!= archive absence
```

Long-lived institutional domains can leave a mixed surface where some old objects remain directly served, some are denied, and some are gone from the live site while still potentially existing in external archives.

A complete evidence record must keep `live observed_at` and `archive capture_datetime` separate.

---

## 12. New archive mechanism: `transaction replay impossibility`

For an ordinary static page, archaeology may aim to reproduce rendering closely.

For historical online banking, successful rendering is not equivalent to ethical or technically legitimate replay of the original transaction.

A real transaction could require:

- valid account;
- live bank backend;
- physical token/private key;
- historical security middleware;
- real beneficiary/merchant state;
- current authorization.

Those should **not** be reconstructed with real credentials.

Therefore M3/M1 reconstruction should stop at:

- rendering public pages;
- documenting controls and code paths;
- using mock/fake account data if interaction must be demonstrated;
- clearly labeling reconstructed transaction states;
- never sending a real financial instruction.

### Rule

```text
historical UI replayable
!= historical transaction replayable
```

For this class of site, “cannot safely replay the financial action” is a valid and expected research boundary.

---

## 13. What the Web changed in ordinary institutional labor

This repository does not need to duplicate the companion HPL narrative, but one interpretive link is necessary.

Online banking moved part of the bank employee's procedural work into the household PC:

- navigate menus;
- type beneficiary/account data;
- install security software;
- manage passwords/certificates;
- interpret error messages;
- confirm transaction outcome.

At the same time it could remove a physical branch trip and loosen branch-opening-hour constraints.

So the historical Web did not simply “make banking virtual.” It changed who had to perform the interface labor and where that labor happened.

For old-Web archaeology, those household execution requirements are part of the historical environment, not incidental support details.

---

## 14. Overseas boundary/control: remote banking predates the Web

The companion HPL package uses French Minitel banking as the cross-national control. BNP Paribas' historical archive records Minitel banking tests from 1982 and later home account-management / transfer services.

That comparison belongs mainly in `how-people-lived`. Its relevance here is only a boundary warning:

> **remote banking is not synonymous with Web banking.**

OWA should therefore date and reconstruct the Chinese Web layer specifically rather than treating every electronic remote-banking channel as an “early website.”

---

## 15. Browser-environment implications for M3

Early bank sites are unusually strong candidates for the repository's browser-environment experiment because modern rendering can hide historically decisive dependencies.

A useful future M3 experiment could compare a public historical bank help/demo page under:

- modern Chromium;
- IE6-level Windows environment;
- historical ActiveX/control present vs missing;
- UShield middleware represented only by a harmless mock/stub;
- correct historical charset vs modern forced UTF-8.

Measure at least:

- which controls render;
- whether form submission code loads;
- JS/browser-sniff differences;
- certificate/USB prompts;
- layout differences;
- missing images/scripts;
- archive URL rewriting effects.

No real bank account or credential should be used.

---

## 16. Current archaeology status

### Achieved

- historical service identity and broad chronology for ICBC website / telephone bank / online bank;
- exact current live-legacy URL for a 2006-era UShield + Alipay workflow page;
- directly observed evidence that branch provisioning, ID, driver/patch installation, certificate download and UShield password were part of that documented workflow;
- evidence model for off-Web provisioning, physical credential state, client environment and cross-site transaction state;
- current observation that old live paths have fragmented survival outcomes (200 response / 403 / 404).

### Not achieved

- a verified 1997–2006 historical Wayback/Common Crawl/WARC capture with capture datetime;
- historical replay/HTTP status;
- original DOM / charset / Content-Type;
- original form actions and script versions;
- complete subresource manifest;
- verified historical UShield control/driver version matched to a captured page;
- a second verified historical Web time point;
- period-specific transaction state machine / timeout/reconciliation semantics;
- M1 complete archaeology case.

Accurate status:

```text
historical service identity: ACHIEVED
exact live-legacy historical-content URL: ACHIEVED
current representation inspected: ACHIEVED
verified historical memento: NOT ACHIEVED
>=2 historical Web timepoints: NOT ACHIEVED
M1 complete case: NOT ACHIEVED
```

---

## 17. Next high-value probes

1. Recover exact 2000–2003 personal-online-banking login/help URLs from contemporary ICBC manuals or press material.
2. Query Wayback/Common Crawl for the exact UShield/Alipay URL and likely login hosts; if a locator is found, **open and inspect it** before upgrading evidence.
3. For any historical capture, record capture datetime, replay/HTTP state, charset, DOM, form action, JS, ActiveX/object tags and subresources.
4. Obtain a second historical time point so changes in login/security architecture can be compared.
5. Locate contemporary public troubleshooting for timeouts, duplicate payments, certificate-download failure and token-driver incompatibility.
6. Find a historical public demo / training account or screenshots that expose the interface without ordinary-user private data.
7. Match any recovered ActiveX/control package to a precise page/date before making browser-environment claims.

---

## 18. Hindsight risks

### Risk 1: “Online bank existed, therefore customers could transact from any computer”

False. Provisioning, physical token possession, driver/control compatibility and trusted browser settings could all matter.

### Risk 2: “Page loads today, therefore this is the 2006 original”

False. The current live-legacy representation has been observed in 2026; historical capture identity remains unverified.

### Risk 3: “UShield survives, therefore historical authentication can be reproduced”

False and unsafe. Hardware appearance and historical private-key/account state are different evidence objects.

### Risk 4: “A success page proves final settlement”

Not unless period-specific documentation defines that state.

### Risk 5: “Web replaced the branch”

The 2006 workflow itself sends the customer back to a branch for initial activation and certain failure recovery.

### Risk 6: “All electronic banking belongs in old-Web history”

No. ATM, phone banking and Minitel-type systems are separate channels. OWA takes them only when they directly explain a Chinese Web interface or shared backend state.

---

## 19. What this adds to old-Web archaeology

The important new point is not “banks also had websites.”

It is that a historical financial webpage can depend on **physical, off-Web and cross-site state** that is unusually difficult—and often inappropriate—to recover:

- a branch-created entitlement;
- a physical security token;
- client drivers and ActiveX controls;
- a certificate/private key;
- a second platform such as Alipay;
- a bank backend whose transaction semantics are invisible in HTML.

That means Web preservation quality must be judged against the whole execution chain, not only against visual fidelity.

A perfect screenshot can preserve the bank's interface while preserving almost none of the historical transaction's executable state.

---

## 20. Saturation judgment

This run is **not** a no-new-mechanism run.

The cross-repository research added a new institutional interface / execution layer:

- money/account portability across place;
- branch/time decoupling;
- credentialized liquidity;
- off-Web provisioning state;
- physical security-token state;
- cross-site credential projection;
- live-legacy survival fragmentation;
- transaction replay impossibility for sensitive dynamic services.

These materially change both the ordinary-life model and the old-Web evidence model.

Therefore the current phase's consecutive no-new-mechanism counter remains **0/3**.
