# Alipay browser/control boundary, 2007–2008

Status: bounded research note; **not an M1 complete case**.

## Why this object

The repository already has substantial notes on hosting loss, URL/DNS disappearance, charset, and Qzone Flash/IE behavior. M1/M3 still require browser/plugin assumptions backed by historical evidence. Alipay in 2007–2008 provides a unusually explicit case where service reachability was deliberately conditioned on browser engine and availability of a security control, then partially reopened through a different browser-specific control.

This note studies the **browser/runtime access boundary**, not Alipay's general corporate history or payment security.

## Claims and evidence

### 1. 2007-07-31 / 2007-08-15: non-IE access was deliberately restricted

**Claim.** A notice dated 2007-07-31, reproduced by multiple contemporaneous outlets, said that because Firefox and other non-IE-engine browsers could not install Alipay's security control, Alipay would close Firefox/Opera access from 2007-08-15 and suggested IE/MYIE instead.

**Grade: A- (derivative primary text) + B (contemporaneous reporting).** The original Alipay Community URL is named by the reports, but this run did not retrieve the original page artifact itself.

Sources / location:

- PConline report mirrored by Sina, 2007-08-07. It reproduces the Alipay explanation and identifies the original community thread: https://tech.sina.com.cn/i/2007-08-07/14341661578.shtml
- cnBeta, 2007-08-04, explicitly attributes the reproduced notice to 支付宝社区 and preserves the notice date/signature: https://www.cnbeta.com.tw/articles/tech/35663.htm

What this proves: browser support was not merely accidental rendering breakage; access policy was tied to whether the browser could host the security-control path accepted by Alipay.

What it does **not** prove: the exact HTTP status, UA-sniffing implementation, JavaScript logic, ActiveX class ID, or whether every unauthenticated public page was blocked.

### 2. The restriction was part of a wider Chinese payment/browser compatibility boundary

**Claim.** Contemporary discussion connected Alipay's Firefox problem to domestic online-banking compatibility, while Firefox/Mozilla-side commentary in early 2008 still described major Chinese financial sites as having browser-support problems.

**Grade: B.**

Sources:

- Sina/PConline, 2007-08-07: Alipay's supplemental explanation says major domestic online banks were not compatible with Firefox and Linux could not install the Alipay security control. https://tech.sina.com.cn/i/2007-08-07/14341661578.shtml
- CNET/ZDNet-era reporting on Mozilla China, 2008-01-04, preserved by Sina: Mozilla China chairman Gong Li says Chinese users still encounter problems using Firefox with online banking and gives IE as the practical workaround for some banks. https://tech.sina.com.cn/i/2008-01-04/10491954016.shtml

This supports treating the case as a **browser + local security component + downstream bank compatibility** stack rather than as a pure HTML/CSS compatibility issue.

### 3. 2008-09-24: Windows Firefox support arrived through a Firefox-specific security component

**Claim.** On 2008-09-24, contemporaneous reports say Alipay released `AliPay Security Control` as a Firefox add-on, allowing Firefox users to complete Alipay transactions without switching to IE. Reports identify the Mozilla Add-ons locator as `addons.mozilla.org/zh-CN/firefox/addon/6707`.

**Grade: B, with primary-artifact locator but without retrieved add-on artifact.**

Sources:

- cnBeta carrying Sohu IT report, 2008-09-24: https://www.cnbeta.com.tw/articles/soft/65527.htm
- PChome, 2008-09-24: https://article.pchome.net/content-721877.html
- Contemporary blog quoting the Alipay official blog announcement, 2008-09-12: https://dbanotes.net/opensource/alipay_support_firefox.html

Important distinction:

`Firefox supported` did **not** mean `plugin-free / standards-only payment flow`.

The evidence instead indicates a transition from an IE-oriented control boundary to a Firefox-specific control path.

### 4. 2008-10: Linux Firefox support was a separate runtime/package boundary

**Claim.** A 2008-10-23 contemporaneous reproduction of an Alipay blog announcement provides a Linux Firefox package name/workflow and MD5 `02240053d32688ed996e3a4788042801`; installation copied `aliedit.so` and `aliedit.xpt` into `~/.mozilla/plugins`. The same notice said digital certificates were still unsupported in this Linux path.

**Grade: A- derivative primary text.** The original official blog artifact/package was not retrieved in this run, so the hash is a historical claim to verify, not a locally verified digest.

Source:

- cnBeta, 2008-10-23: https://m.cnbeta.com.tw/wap/view/67851.htm
- Independent first-person test on Ubuntu 8.10 / Firefox 3.0.2 was also preserved the same day: https://m.cnbeta.com.tw/wap/view/67860.htm

This is useful because it demonstrates that `browser family support` and `OS support` were separate axes.

## Browser-environment model suggested by the evidence

For this class of Chinese Web application, preservation/replay should record at least:

```text
OS / architecture
→ browser family + version
→ rendering engine
→ plugin/control mechanism
→ security-control build/package
→ certificate capability
→ downstream bank compatibility
→ site-side access policy / UA gate
→ HTML/payment application
```

Useful non-equivalences:

```text
page renders ≠ user can authenticate/pay
browser supported ≠ browser works without a local control
Firefox supported ≠ Linux supported
Linux Firefox supported ≠ certificate workflow supported
service reachable ≠ all transaction paths usable
IE-compatible browser ≠ historically identical IE runtime
```

## Timeline

| Date | Event | Grade |
|---|---|---|
| 2007-07-31 | Alipay notice dated: Firefox/Opera restriction announced because security control could not be installed | A- derivative |
| 2007-08-15 | stated effective date for non-IE access restriction | A- derivative |
| 2008-01-04 | Mozilla China commentary still describes Chinese online-banking browser compatibility as a practical constraint | B |
| 2008-09-24 | Firefox security-control/add-on support publicly released | B |
| 2008-10-23 | Linux Firefox security-control test package/installation details preserved; certificate limitation stated | A- derivative + B first-person test |

## Suggested repository integration

Primary location: this note under `research/` until original artifacts are recovered.

Later candidates:

- M1/M3 browser-assumption fields: add `browser_engine`, `browser_version`, `os`, `plugin_or_control`, `control_version/hash`, `certificate_support`, `access_gate`, and `transaction_capability` as distinct observations rather than one `works_in_IE` boolean.
- `studies/platform-genealogy.md`: only after the browser/runtime evidence is connected to an actual archived Alipay page.

## Missing evidence / next bounded probe

1. Original 2007-07-31 Alipay Community notice capture (`club.alipay.com/show_thread-19---6044452-.htm` as cited by contemporaneous reporting).
2. 2007-08-15 before/after captures of login/payment entry points, including raw HTML and HTTP behavior.
3. Historical Alipay security-control installer metadata: filename, signature, version, hash, ActiveX/COM identifiers where applicable.
4. Mozilla Add-ons artifact/metadata for add-on 6707, including compatible Firefox versions and package type.
5. Original 2008 Alipay blog announcement and Linux package; verify the reported MD5 without redistributing the binary.
6. A safe static inspection of archived HTML for `object`, `classid`, plugin detection, UA gating, and download locators. Do **not** execute historical controls on a normal workstation.

## Reconstruction potential

**Medium for access-policy/runtime history; low-to-medium for executable replay today.** The policy transition is unusually well documented. Faithful replay requires the exact historical page, control build, browser/OS state, certificate behavior, and possibly bank-side endpoints that no longer exist.

A safe reconstruction can probably reproduce the *decision boundary* (supported/unsupported environment and explanatory UI) before it can reproduce a real payment transaction.

## What we cannot claim

- We have not proved that all 2007 Alipay pages were IE-only.
- We have not proved the exact ActiveX CLSID or control implementation from original HTML.
- We have not proved that the 2007 restriction was enforced solely by HTTP User-Agent sniffing.
- We have not proved that Firefox support in September 2008 was standards-only or plugin-free; evidence points the other way.
- We have not verified the Linux package MD5 against recovered original bytes.
- We have not proved that Firefox/Linux users could use every certificate, bank, recharge, and payment path after the new control appeared.

## Privacy, security, and copyright boundary

- Do not capture or republish account pages, transaction records, payment credentials, certificates, cookies, or user-identifying data.
- Historical controls/installers should be handled as potentially unsafe executable code. Prefer metadata, hashes, signatures, static strings, and sandboxed/offline analysis; do not run unknown ActiveX/plugin binaries on an ordinary host.
- Do not commit proprietary installers or add-on binaries unless redistribution rights are established. Record locators, hashes, sizes, signatures, and provenance instead.
- Public help pages, corporate notices, and press reports may be cited and minimally excerpted; preserve only what is necessary to substantiate claims.

## Research conclusion

The important archaeological object is not simply “Alipay once preferred IE.” The evidence shows a moving **capability boundary**: in 2007 Alipay deliberately denied non-IE browser access because its accepted security-control path was unavailable there; in 2008 it restored Firefox access by shipping a Firefox-specific control, then separately exposed a Linux Firefox package with remaining certificate limitations.

For old-Web reconstruction, this means a visually intact page can still be functionally dead if the historical local control, browser/OS combination, certificate path, or downstream bank integration is absent. That boundary should be preserved as evidence rather than flattened into a generic `IE-only` label.
