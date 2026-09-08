# Personal Online Banking, Remittance, Authentication, Clearing, and Funds-Availability State Gaps (China, 1997–2015)

> Scope: Chinese personal online-banking and remote-remittance interfaces, approximately 1997–2015. The archaeological target is **not** a general history of Chinese banking or mobile payment. It is the transaction-state boundary between what a historical Web page appeared to let a person do and when money actually became usable by another person in another place.
>
> Pre-Web postal/bank remittance appears only as necessary boundary context. 2018–2026 examples appear only as afterlife evidence exposing states already created in the 1997–2015 period.

Companion life-history package:

- `tmzncty/how-people-lived/topics/from-carrying-cash-home-to-distance-decoupled-household-liquidity-postal-remittance-bank-cards-online-banking-and-family-money-flows-china-1980-2026.zh-CN.md`

---

## 0. Why this belongs in old-web-archaeology

A surviving old bank page may say:

> `转账成功`

That phrase is archaeologically ambiguous.

It may mean only that:

- the form passed client-side validation;
- the sender authenticated successfully;
- the sender bank accepted an instruction;
- the sender account was debited;
- a clearing message was queued;
- a cross-bank system accepted the item;
- the recipient bank posted the credit;
- the recipient could already withdraw the money;
- or merely that a browser received a success page.

These are not the same state.

The central rule for this note is therefore:

> **visible Web success != final funds availability**

And the complementary old-Web warning is:

> **online banking existed != ordinary users could complete a transfer from any ordinary PC**

Because early personal banking could depend on:

- prior branch enrollment;
- bank card/account status;
- browser support;
- security controls / ActiveX-like components;
- a digital certificate;
- a USB Key/U盾/优KEY;
- a driver;
- password or dynamic-code state;
- transaction limits;
- the recipient bank;
- the interbank clearing rail;
- scheduled maintenance;
- and sometimes a later offline cash-out step in the recipient’s locality.

This is exactly the kind of front-end/back-end state split required by `docs/METHOD.md`.

---

## 1. Core research unit

Do not treat “网上银行” as a single object.

At minimum distinguish:

```text
BANK BRAND
PUBLIC PORTAL HOST
PERSONAL BANK LOGIN HOST
LOGIN PAGE
TRANSFER FORM
AUTHENTICATION COMPONENT
BANK CORE / ACCOUNT SYSTEM
INTERBANK CLEARING SYSTEM
RECIPIENT BANK CORE
RESULT PAGE / RECEIPT
SMS / TELEPHONE NOTIFICATION
```

The same brand may change hosts, application architecture, security controls, certificates, page layout and processing semantics across years.

Likewise:

```text
product launch date
!= host first reachable date
!= feature enabled for all branches
!= user enrolled
!= user authenticated
!= transfer rail available
!= ordinary adoption
```

---

## 2. Pre-Web boundary: remote money movement is older than Web banking

This repository’s main scope stays with 1995–2015 Chinese Web history. The prehistory matters only because otherwise an online-transfer page can be misread as the invention of remittance itself.

A 1980 People’s Bank of China / Ministry of Posts and Telecommunications rule already explicitly governed large personal remittances through banks and post offices.

- 1980-09-06 normative text, public-domain republication:
  <https://zh.wikisource.org/zh-hans/中国人民银行、邮电部关于银行与邮局办理汇兑业务分工办法的补充通知>

Evidence grade: **A for normative rule; current access is a later republication**.

By 2001 China Post was digitizing the transfer of remittance information while customers could still use physical post-office counters. A 2003 contemporary report says the electronic remittance system launched publicly on 2001-07-01 and by early 2002 had replaced physical draft transmission between prefecture/county-level cities; it also records 24-hour and 2-hour services.

- 2003-10-10, Guangming Daily via Sina:
  <https://news.sina.com.cn/c/2003-10-10/1046890772s.shtml>

Evidence grade: **B+ contemporary institutional/press material**.

Archaeological boundary:

> **backend digitization != Web self-service**

A household with no PC could still experience a digitally accelerated remittance.

---

## 3. 1997–2000: online banking appears, but launch chronology is not a historical capture

China Merchants Bank’s current institutional history identifies “一网通” in 1997 as an early personal Internet-banking service. ICBC’s current version-history page records personal Internet-banking pilot deployment on 2000-08-28 in Beijing and Zhejiang and the later 2003 launch of “金融@家”.

- China Merchants Bank institutional history:
  <https://www.cmbchina.com/>
- ICBC Internet-banking version history:
  <https://www.icbc.com.cn/icbc/html/wangyin/version/version.html>

Evidence grade: **A for current institutional retrospective chronology**, but **not A historical-capture evidence for 1997/2000 HTML**.

These sources can support narrow claims such as:

```text
institution currently states product X launched in year Y
```

They do **not** support:

```text
1997 page used today’s domain/path
1997 HTML looked like today’s page
all branches/users received identical function
historical transfer form fields
historical HTTP headers/charset/session behavior
```

This distinction is essential because current bank websites often preserve a corporate timeline while replacing every underlying Web artifact.

---

## 4. The transaction model

### 4.1 Enrollment lifecycle

Before a historical user could transfer money online, the actual lifecycle might be:

```text
BANK ACCOUNT EXISTS
-> BANK CARD / ACCOUNT ELIGIBLE
-> USER REQUESTS INTERNET BANKING
-> IDENTITY CHECKED AT BRANCH OR OTHER CHANNEL
-> INTERNET-BANKING CONTRACT CREATED
-> LOGIN ID / CREDENTIAL CREATED
-> SECURITY DEVICE OR CERTIFICATE ISSUED
-> CLIENT SOFTWARE / DRIVER INSTALLED
-> CERTIFICATE ACTIVATED
-> TRANSFER FUNCTION ENABLED
```

Important gaps:

- `bank account exists != online banking enabled`
- `online banking enabled != transfer enabled`
- `login works != high-value transfer allowed`
- `USB Key issued != driver installed`
- `driver installed != browser recognizes component`

### 4.2 Transfer lifecycle

```text
LOGIN PAGE REACHABLE
-> USER AUTHENTICATED
-> TRANSFER PAGE REACHABLE
-> RECIPIENT BANK SELECTED
-> RECIPIENT ACCOUNT ENTERED
-> AMOUNT ENTERED
-> FEE / LIMIT DISCLOSED
-> USER CONFIRMS
-> SECOND FACTOR / CERTIFICATE / U-KEY SIGNATURE
-> BANK ACCEPTS INSTRUCTION
-> SENDER ACCOUNT DEBITED OR FUNDS RESERVED
-> CLEARING MESSAGE GENERATED
-> CLEARING RAIL ACCEPTS
-> RECIPIENT BANK RECEIVES
-> RECIPIENT ACCOUNT CREDITED
-> RECIPIENT CAN WITHDRAW / SPEND
-> RECEIPT / QUERY STATE UPDATED
```

Do not collapse any adjacent pair unless the historical system documentation actually proves atomicity.

### 4.3 Failure branches

```text
wrong account number
recipient-name mismatch / not checked
security component fails
certificate expired
USB device absent
password attempts exceeded
transaction exceeds limit
bank front end accepts but clearing rail unavailable
recipient bank offline
maintenance window
message delayed
credit reversed
browser displays stale/cached result
```

---

## 5. 2005: the Web transfer page becomes inseparable from authentication hardware

A 2005 Xinhua report says ICBC renamed/upgraded its USB client certificate as “U盾”. The described login path required the ordinary Internet-banking username/password plus insertion of a USB device used as a digital certificate before the bank would permit account operations.

- 2005-10-10, Xinhua via Sina:
  <https://tech.sina.com.cn/i/2005-10-10/1619736319.shtml>

Evidence grade: **B contemporary report quoting the bank**.

A dated 2006 ICBC notice still hosted on the bank’s domain lists U盾 prices (60–76 yuan depending on model) and explicitly associates U盾 with 24-hour large-value transfers/remittances.

- 2006-01-24, ICBC preserved notice:
  <https://www.icbc.com.cn/icbc/html/gonggao/2006nian/0124/sy_pop_udunjgtzgg0601241.html>

Evidence grade: **A-current institutional preservation of a dated notice**. It is **not yet a verified 2006 archive capture**.

This produces a key old-Web distinction:

> **page accessibility / transaction authority gap**

A person could open a bank’s public Web pages but still lack the physical credential required to move money.

---

## 6. 2006: “driverless” itself was a product feature, proving that client configuration was part of transaction history

In 2006 China Merchants Bank promoted the “优KEY” mobile digital certificate with “免驱动” as a usability advantage. Contemporary reporting explicitly says earlier USB Keys could fail during driver installation.

- 2006-06-20, Sina Finance:
  <https://finance.sina.com.cn/money/bank/bank_operation/20060620/19162667064.shtml>

Evidence grade: **B contemporary product report**.

That single fact is archaeologically important. It means a bank transfer cannot be reconstructed only from server HTML.

The user environment may have included:

```text
Windows version
browser engine
USB stack
bank driver
certificate middleware
security control
local permissions
anti-virus interaction
```

Therefore:

> **historical browser replay without security middleware may reproduce a page but not reproduce transaction executability.**

This is a stronger state than the repository’s general “modern Chromium may render differently” warning: here the missing client component could prevent the transaction entirely.

---

## 7. 2006 historical locator: ICBC personal banking login can be narrowed without pretending we have a capture

A 2006 contemporary anti-phishing report compared a fake URL with what it identified as the genuine ICBC personal-banking address:

```text
https://mybank.icbc.com.cn/icbc/perbank/index.jsp
```

- 2006-12-06 contemporary report:
  <https://www.cnbeta.com.tw/articles/19028.htm>

ICBC’s present FAQ continues to identify `https://mybank.icbc.com.cn` as the personal Internet-banking host.

- current ICBC FAQ:
  <https://www.icbc.com.cn/icbc/en/frequentlyaskedquestions/faqs/others/WhatistheICBCwebsiteaddr.htm>

Evidence grade:

- **B** for the 2006 contemporary report’s locator;
- **A-current** for present host identity;
- **not a verified 2006 capture**.

This supports a candidate historical locator only.

Do **not** infer:

- the 2006 page still exists at that exact path;
- current TLS/HTTP behavior matches 2006;
- current page HTML is historical;
- historical certificates remain valid;
- archive replay can complete login.

---

## 8. Security controls introduce hidden state into what otherwise looks like a simple form

Third-party payment/help pages preserved from the later old-Web period document multiple ICBC user classes:

```text
static-password user
one-time/dynamic code-card user
U盾 user
```

Some instructions note different payment/transfer limits and the need to visit a branch to obtain an electronic password card or U盾.

Examples:

- historical-style payment-gateway help:
  <https://pay.fuiou.com/help/0801020000.html>
- later help preserving the same distinction:
  <https://www.yirendai.com/support/others/wyfw/2013080293.html>

Evidence grade: **B/C depending on the exact page date; useful for state vocabulary, not sufficient to date every rule**.

Required distinction:

```text
AUTHENTICATED_USER
!= USER_WITH_HIGH_VALUE_AUTHORITY
```

The transfer amount itself can change what authentication route is required.

This matters for ordinary life because a user who could pay a small online purchase might still be unable to send a month’s salary home.

---

## 9. 2005 policy boundary: electronic-payment limits were tied to authentication strength

Contemporary reporting on the People’s Bank of China’s 2005 electronic-payment guidance described limits for personal online payment where digital certificates/electronic signatures were not used: single transactions up to 1,000 yuan and daily cumulative value up to 5,000 yuan.

- 2005 contemporary reporting:
  <https://news.sina.com.cn/c/2005-10-31/08157313717s.shtml>
- PBC English Q&A on the E-Payment Guidance:
  <https://www.pbc.gov.cn/english/130721/2025080815102544674/index.html>

Evidence grade: **A/B family: central-bank rule/Q&A plus contemporary press**.

Archaeological value:

```text
same Web channel
+ stronger credential
-> different executable transaction ceiling
```

So a screenshot of a transfer form does not prove all visible amounts were legally/technically executable for every logged-in user.

---

## 10. 2007–2009: old-Web remittance becomes ordinary enough to enter newspaper service journalism

A 2007 Shanghai reader letter gives a useful non-Web counterexample: a migrant restaurant worker with more than 20,000 yuan saved still weighed carrying cash home against postal remittance because rural notification could take days.

- 2007-02-15, Wenhui Bao via Sina:
  <https://news.sina.com.cn/c/2007-02-15/082011247995s.shtml>

Evidence grade: **B, contemporary first-person letter + reporter follow-up**.

By 2009, another contemporary article describes a Shanghai worker repeatedly using online banking to send money to parents in Shenyang; the interviewed user says a 20,000-yuan remittance could be completed online in about two minutes, with lower fees than the counter route.

- 2009-06-15, Licai Zhoubao via Sina:
  <https://finance.sina.cn/sa/2009-06-15/detail-ikftssap0008222.d.html>

Evidence grade: **B contemporary first-person interview**.

Together these sources establish **used**, not merely **exists**, for at least some households.

They still do not establish population prevalence.

---

## 11. 2008 third-party tutorials are part of the archaeological object

Bank transaction history is not preserved only on bank domains. E-commerce, travel, payment gateways and local service sites often wrote step-by-step bank tutorials because users needed help crossing from merchant site to bank site.

Examples include:

- Shenzhen local guide to Bank of Communications online banking (2008-11-28), identifying `www.95559.com.cn` and describing a mobile-SMS authentication path:
  <https://m.bendibao.com/bsy500.html>
- Tuniu help preserving bank-specific online-banking enrollment/payment guidance:
  <https://tuniu.com/help/help_bank_06.shtml>

Evidence grade: **B**.

These third-party pages may preserve:

- hostnames;
- terminology;
- enrollment assumptions;
- login variants;
- screenshots;
- SMS verification steps;
- product distinctions such as “大众版 / 专业版”.

They must not be treated as authoritative for bank backend semantics, but they are valuable **user-execution evidence**.

---

## 12. A bank brand can expose multiple “online banking” modes with different powers

China Merchants Bank third-party instructions from the old-Web period distinguish:

```text
个人银行大众版
个人银行专业版
```

with professional-version enrollment involving branch identity verification and a certificate/authorization process.

Examples:

- old payment-help page:
  <https://st.shengpay.com/html/shengpayHelper/help_new/help_page/index_zs.htm>
- Tuniu bank-help page:
  <https://tuniu.com/help/help_bank_06.shtml>

Evidence grade: **B**.

Thus:

> `user can log in to CMB Web banking != user has professional-version transfer authority`

A reconstruction that renders a public “个人银行” button but cannot tell which banking mode it entered is incomplete.

---

## 13. 2010: “super online banking” shows that the Web form and the money rail are separate historical systems

The People’s Bank of China states that the Online Payment Interbank Clearing System began trial operation on 2010-08-30 and completed national rollout on 2011-01-24. It supported cross-bank payments, account information queries and online contract/signing functions using real-time transmission/response.

- PBC Guizhou branch explanation:
  <https://guiyang.pbc.gov.cn/guiyang/113337/2164373/2197562/index.html>
- PBC, China Payment System Development Report (2010):
  <https://www.pbc.gov.cn/eportal/fileDir/image_public/UserFiles/goutongjiaoliu/upload/File/中国支付体系发展报告2010.pdf>

Evidence grade: **A**.

The 2010 report says 64 banking financial-institution legal entities had connected by year end.

This is a critical architecture boundary:

```text
BROWSER
-> BANK A WEB FRONT END
-> BANK A CORE
-> ONLINE PAYMENT INTERBANK CLEARING SYSTEM
-> BANK B CORE
-> RECIPIENT BALANCE
```

The browser is only the first visible layer.

---

## 14. `system launched != every bank/customer immediately available`

Contemporary launch reporting in 2010 described banks still testing/rolling out customer-facing features even as the central interbank system went online.

- 2010-08-31 contemporary reporting:
  <https://news.sina.com.cn/o/2010-08-31/051018043272s.shtml>

Evidence grade: **B**.

So timeline claims should preserve at least three dates:

```text
central infrastructure online
bank connected
specific retail customer feature available
```

Do not assign the first date to the third state.

---

## 15. 2013 maintenance is a rare state-gap probe: front-end availability does not guarantee clearing availability

During a 2013 payment-system upgrade, contemporary notices warned that some interbank counter remittance and Internet-banking cross-bank transfer services would be suspended while relevant clearing systems were stopped, even while ATM and some third-party payment paths could continue through other rails.

- 2013-09-27, People.cn:
  <https://www.people.com.cn/24hour/n/2013/0927/c25408-23053674.html>

Evidence grade: **B contemporary authoritative media based on PBC schedule**.

This provides unusually strong support for:

> **front-end reachable / downstream rail unavailable gap**

A historical screenshot showing that a user could still reach `mybank.icbc.com.cn` during such a window would not prove a cross-bank remittance was executable.

---

## 16. Funds-availability state must include the recipient’s locality

A 2005 People’s Bank of China pilot for migrant-worker bank cards demonstrates why recipient-side cash access is not a trivial final step.

The official design:

```text
migrant worker deposits money to UnionPay card at work location
-> card network carries value state
-> rural credit cooperative in home region accepts card
-> cash can be withdrawn locally
```

- 2005-12-29 PBC release via Sina:
  <https://finance.sina.com.cn/g/20051229/1801472429.shtml>
- PBC 2005 Guizhou regional financial report:
  <https://www.pbc.gov.cn/eportal/fileDir/history_file/files/att_12716_1.pdf>

Evidence grade: **A**.

This shows why Web archaeology should not end at `RECIPIENT_ACCOUNT_CREDITED`.

For a rural household:

```text
credit posted
!= convenient nearby cash availability
```

The user-facing Internet can be perfect while the final kilometer of financial infrastructure remains the binding constraint.

---

## 17. Transaction receipts and “success pages” need an explicit evidence contract

If a historical capture of a transfer result is ever found, catalog at least:

```yaml
page_claimed_state: unknown|submitted|accepted|debited|processing|completed
sender_bank: ...
recipient_bank: ...
within_bank_or_interbank: ...
visible_reference_number: redacted/hash-only
visible_timestamp: ...
amount: redact unless historically necessary
recipient_identity: never republish ordinary-person data
archive_source: ...
capture_datetime: ...
original_url: ...
http_status: ...
charset: ...
browser_assumption: ...
private_dynamic_state: yes
confidence: ...
```

Privacy rule:

> Do not republish an ordinary person’s bank account number, balance, transfer amount, beneficiary name, security code or transaction reference merely because an archive accidentally captured it.

For this object class, **schema/state preservation is more valuable than personal transaction disclosure**.

---

## 18. Required state distinctions

### Identity / authority

- `bank customer != online-banking customer`
- `online-banking login != transfer authority`
- `password accepted != U-Key/certificate accepted`
- `certificate present != certificate valid`
- `account owner != current keyboard operator`

### Browser / client

- `public page renders != banking control installed`
- `driver installed != USB device detected`
- `security component loaded != transaction signed`
- `modern replay renders != historical client executable`

### Transfer

- `form completed != submitted`
- `submitted != accepted`
- `accepted != sender debited`
- `sender debited != clearing complete`
- `clearing complete != recipient credited`
- `recipient credited != recipient notified`
- `recipient notified != locally withdrawable`

### Interbank

- `bank A online != clearing rail online`
- `clearing rail online != bank B online`
- `system national rollout != every bank feature enabled`

### Historical evidence

- `dated bank notice on current server != verified historical Web capture`
- `contemporary article gives URL != capture opened and checked`
- `search-engine result != historical artifact`
- `current host identity != unchanged historical application`

---

## 19. Browser/technology questions that remain open

For each historical bank target, try to establish rather than assume:

- OS requirement;
- IE version requirement;
- whether Netscape/Firefox worked;
- ActiveX or proprietary security controls;
- executable download / CAB / DLL dependencies;
- USB Key middleware;
- certificate store location;
- TLS/cipher compatibility;
- GB2312 / GBK / UTF-8;
- frameset / table layout;
- JavaScript dependence;
- cookie/session mechanism;
- timeout behavior;
- anti-phishing image / reserved message;
- popup/window dependencies;
- print-receipt implementation;
- whether transfer result came from synchronous response or later query.

Without these, a visual reconstruction must remain explicitly incomplete.

---

## 20. Candidate historical locators from this slice

### ICBC

Contemporary 2006 evidence gives:

```text
portal: http://www.icbc.com.cn
personal bank candidate:
https://mybank.icbc.com.cn/icbc/perbank/index.jsp
```

Current bank documentation gives the personal-banking host:

```text
https://mybank.icbc.com.cn
```

### Bank of Communications

2008 user guide gives:

```text
www.95559.com.cn
```

and identifies separate personal-bank paths under the `pbank.95559.com.cn` family in later surviving documentation.

### China Merchants Bank

Contemporary and current institutional material repeatedly anchors:

```text
www.cmbchina.com
```

and “一网通 / 个人银行大众版 / 个人银行专业版” as distinct user-facing concepts.

These are **locators**, not verified capture claims.

---

## 21. Archive attempt and M1 status

This slice attempted to move from the 2006 ICBC locator toward an Internet Archive CDX query for:

```text
mybank.icbc.com.cn/icbc/perbank/index.jsp
```

and separately toward early `www.cmbchina.com` captures.

The current Web access path rejected direct constructed CDX URLs before a qualifying result could be opened and inspected.

Therefore:

> **M1 historical-capture verification: NOT ACHIEVED IN THIS SLICE.**

This means only:

- no qualifying replay was verified in this run.

It does **not** mean:

- Wayback has no capture;
- the historical page was never archived;
- Common Crawl/other collections lack it;
- the host was absent.

Per `docs/METHOD.md`, candidate locators must remain candidate locators until an actual replay/artifact is opened and inspected.

---

## 22. What is established / probable / unknown

### Established with current evidence

1. Personal online banking existed in China before mass smartphone payment.
2. ICBC and CMB institutional histories place major personal online-banking deployments in the late 1990s/early 2000s.
3. By 2005–2006, USB digital certificates were explicitly part of retail online-banking security and transfer authority.
4. Driver installation and certificate middleware were real user-execution issues.
5. A contemporary 2006 source identifies `mybank.icbc.com.cn/icbc/perbank/index.jsp` as the genuine ICBC personal-bank login locator in an anti-phishing comparison.
6. By 2009 at least some ordinary users were using personal online banking for repeated long-distance transfers to parents.
7. The PBC’s 2010 online interbank clearing system demonstrates that cross-bank Web transfers depended on a separate national clearing layer.
8. The 2013 maintenance window demonstrates that a bank Web front end and downstream transfer rail can have different availability states.
9. Rural recipient cash-out remained a separate infrastructure problem even when electronic account/card rails existed.

### Probable but not yet capture-verified

1. IE/security-control dependencies materially affected many early retail bank transaction paths.
2. The historical ICBC personal banking application used the candidate path family identified in 2006 for at least part of the period.
3. Public bank portals and authenticated transaction applications were often separate hosts or application contexts.
4. Receipt/result pages were highly dynamic and therefore systematically under-preserved relative to public help pages.

### Unknown

1. Exact HTML/DOM/CSS of 1997–2001 CMB personal banking.
2. Exact HTTP headers and charset of the 2006 ICBC login/application.
3. Exact client security control filenames/versions at each date.
4. Whether historical archive replay can load dependent scripts/components.
5. Session/cookie structure.
6. Transfer endpoint method/URL.
7. Recipient-name validation semantics.
8. Whether `success` was synchronous finality or instruction acceptance for each bank/version.
9. How cross-bank failures were represented in the UI.
10. Whether a transfer result page could later update asynchronously.
11. Real-world browser failure rates.
12. Real-world adoption by income, age, region and rural/urban status.

---

## 23. Archaeological preservation bias

The most survivable artifacts are likely to be:

- marketing pages;
- fee tables;
- public security notices;
- tutorials;
- anti-phishing alerts;
- product launch articles;
- screenshots in merchant help pages;
- maintenance notices.

The least survivable artifacts are likely to be:

- authenticated transaction forms;
- POST bodies;
- dynamic recipient lists;
- security-device handshakes;
- account balances;
- transfer status queries;
- error codes;
- clearing acknowledgements;
- actual recipient credit timestamps.

So a future history built only from surviving pages will systematically over-document **promised capability** and under-document **transaction failure**.

That bias must be stated, not silently filled with modern assumptions.

---

## 24. Why this changes old-Web interpretation

A bank website is not simply a page collection.

It is a distributed transaction boundary:

```text
public Web
<-> authenticated session
<-> local security hardware
<-> bank core
<-> central clearing
<-> another bank
<-> recipient’s local access infrastructure
```

The historical Web page is only the visible edge.

For ordinary-life history, however, the outcome occurs at the far end:

> **Can the person in another city actually use the money now?**

That is why `转账成功` is not a complete historical claim.

---

## 25. Next archaeological tasks

1. Obtain verified 2005–2009 captures for `mybank.icbc.com.cn` and record exact capture datetime, status, charset and page type.
2. Search archive indexes for early `cmbchina.com` “一网通” public/help pages before attempting authenticated-application reconstruction.
3. Find contemporary bank manuals or software CDs documenting security controls, USB-Key middleware and browser requirements.
4. Preserve third-party merchant tutorials as independent evidence of how ordinary users actually crossed between merchant and bank pages.
5. Find a dated historical transfer receipt/error screenshot with all private data redacted at source or suitable for schema-only analysis.
6. Compare within-bank, cross-city same-bank and cross-bank state semantics rather than assuming one transfer model.
7. Locate maintenance/error pages, because failures are more informative for transaction-state archaeology than another marketing homepage.

---

*AI-assisted research note. No private banking records, credentials, transaction identifiers or deleted personal financial material are reproduced.*