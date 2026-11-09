# M0 site index contract (draft, 2026-11-09)

This document defines the *index* `datasets/sites.csv`, not the claim-level evidence ledger. It is intentionally empty until records can be traced to evidence files. The absence of rows does **not** mean there are no known sites.

## Row identity and granularity

One row describes one historically bounded **platform, host, site, or public page**. Do not mix a platform with an individual user homepage; split rows if ownership, URL control, or network access changes enough to alter the research unit. `site_id` is a stable lowercase ASCII slug, not an asserted historical identifier. Use UTF-8, RFC 4180 CSV quoting, ISO 8601 dates, and explicit empty cells for unknowns. Never substitute today's DNS response for a historical one.

## Columns

| Column | Meaning and constraint |
|---|---|
| site_id | Unique stable slug; never derived from private user identifiers |
| display_name | Historical public name, with uncertainty in notes |
| unit_type | `platform`, `host`, `site`, `public-page` |
| original_locator | Original historical URL/host *as observed* in evidence; blank if unknown |
| locator_kind | `observed-original`, `reported-original`, `pattern-only`, `unknown` |
| earliest_supported_date | Earliest *evidence-supported* observation, not claimed launch date |
| latest_supported_date | Latest *evidence-supported* observation, not claimed shutdown date |
| date_precision | `day`, `month`, `year`, `mixed`, `unknown` |
| first_evidence_id | Exact ID in evidence ledger; never a guessed Wayback URL |
| second_evidence_id | Second independent family ID where available; blank otherwise |
| independent_family_count | Integer, count of genuinely independent provenance families, not URLs |
| evidence_status | `verified`, `partial`, `candidate`, `unverified` |
| archive_status | `direct-capture-verified`, `locator-only`, `secondary-only`, `not-checked` |
| reconstruction_status | `none`, `proposed`, `experimental`, `verified-differences` |
| privacy_review | `cleared-public-structure`, `restricted`, `pending` |
| notes | Narrow scope, conflicting dates, limitations; no personal data |

## Evidence linkage and date discipline

The index is a **projection**, not a replacement for `evidence.yaml` or `schemas/evidence.schema.json` (currently proposed in PR #19). A historical statement needs its own source, original locator, archive locator if any, event/page/capture/access dates, A/B/C/D grade, verification state, and evidence-family provenance. CSV rows cannot elevate derivative copies into directly verified A-level artifacts.

Never conflate:
- launch, first indexed observation, first capture, last capture, closure announcement, DNS expiry;
- host reachable from one observer versus universally accessible;
- a homepage surviving versus its images/scripts/Flash and interactive runtime surviving;
- an original site versus a migrated, cached, or reconstructed version.

A second citation copied from the same company announcement does not increase `independent_family_count`. If evidence IDs cannot be resolved, leave the row out rather than writing an attractive but uncheckable chronology.

## Privacy and copyright

Index public platform-level locators first. Do not store private user IDs, recovered contact details, deleted diaries, credentials, or proprietary binaries. An archive's public availability is not redistribution permission. Prefer metadata and citations; keep third-party content out of this CSV.

## Acceptance tests before population

1. Parse CSV as UTF-8; assert header order and unique nonempty `site_id`.
2. Validate enumerations and ISO date precision; unknown is empty or the documented enum, never fabricated `1970-01-01`.
3. For every populated evidence ID, resolve it to a real ledger entry and its source family.
4. Verify `independent_family_count` from distinct provenance families rather than citation count.
5. Independently review three actual archive captures and compare index projection across two reviewers; do not mark M0 complete before that test.
6. Do not mark M1 complete merely because the index has three rows: full cases need resource inventories, historical browser/charset assumptions and at least two timepoints.

## Current status

The CSV contains only the header. This is a contract/schema advance, **not** a new historical discovery or an M0/M1 completion claim. Follow-up should connect PR #19's evidence contract, add mechanical validation, and populate only source-verified, privacy-cleared rows.
