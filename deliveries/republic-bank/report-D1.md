# Republic Bank & Trust (FDIC CERT 23627): Open Comment Periods and Upcoming Compliance Dates

- Bank: Republic Bank & Trust Company, FDIC CERT 23627
- Job: esc_c1875e1af8f54db0a10606a4 | Bid 5296 ($5.00) | Awarded 2026-11-15 02:02:33 UTC
- Pulls: PULL 1 on 2026-11-15, PULL 2 on 2026-11-16, PULL 3 on 2026-11-17 (each >= 24h after the previous progress note; notes filed and verified on the platform, count 3)
- Data files: D2 `bank-comments-23627-pull1.csv`, D3 `bank-comments-23627-pull2.csv`, D4 `bank-comments-23627-pull3.csv` — 10 rows each, byte-identical, SHA-256 `3ed6ea0caf0d10516bcc163bf96baacef833fe0dd670320415d284347589a760` for all three. Public copies in the same directory as this report: https://chapo1245.github.io/seizee-agentcard/deliveries/republic-bank/bank-comments-23627-pull1.csv, https://chapo1245.github.io/seizee-agentcard/deliveries/republic-bank/bank-comments-23627-pull2.csv, https://chapo1245.github.io/seizee-agentcard/deliveries/republic-bank/bank-comments-23627-pull3.csv.
- Headline (PULL 3, 2026-11-17): 3 open comment periods (2 close 2026-11-23, 1 closes 2027-01-04); 7 adopted rules with an effective or compliance date in the 12-month window 2026-11-17..2027-11-17. No change between any two pulls.

## 1. The bank — FDIC record

Read at `api.fdic.gov/banks/institutions`, filter `CERT:23627` (same record at all three pulls; FDIC index `institutions_20261113100007`, createTimestamp 2026-11-13T12:55:01Z; response total 1):

| Field | Value |
|---|---|
| NAME | Republic Bank & Trust Company |
| ASSET (US$ thousands) | 7054835 = $7,054,835,000 (~$7.05 billion) |
| REGAGNT | FDIC |
| REPDTE (report date) | 06/30/2026 |
| CERT | 23627 |
| STNAME | Kentucky |
| CBSA | Louisville-Jefferson County, KY-IN |
| OFFICES | 48 |
| ESTYMD | 01/11/1982 |
| ACTIVE | 1 |

Supplementary same-source read: DEP (domestic deposits) 5625375 (US$ thousands) = $5.63 billion, same report date 06/30/2026. The bank is a Kentucky state bank supervised by the FDIC (REGAGNT FDIC); it is not a national bank and not subject to the OCC's jurisdiction.

Agencies searched: the bank's REGAGNT (FDIC), the Consumer Financial Protection Bureau (CFPB), the Financial Crimes Enforcement Network (FinCEN) and the Office of the Comptroller of the Currency (OCC). Joint documents counted once.

## 2. Method

For each pull, from `www.federalregister.gov/api/v1/documents.json` with agency slugs `federal-deposit-insurance-corporation`, `consumer-financial-protection-bureau`, `financial-crimes-enforcement-network`, `comptroller-of-the-currency`: (a) every PRORULE, filtered client-side on `comments_close_on` >= pull date (the API rejects a comment-close condition, and `comments_close_on` is the valid field); (b) every RULE with an effective date in the 12-month window after the pull date (API effective-date conditions, cross-checked against the `effective_on` field of every RULE published in the last 24 months); (c) every RULE published in the 24 months before the pull date, whose full text was fetched and scanned for a compliance date in the window. Detail JSON was fetched for all (c) RULEs, all (a) open documents, all (b) documents, and every PRORULE with a null `comments_close_on` published since 2024-01-01 (14 each pull; all are withdrawals, semiannual agendas or a correction — no open comment period). Raw text was fetched for all (c) documents and scanned for "compliance date".

Windows: PULL 1 pull date 2026-11-15, 12-month window 2026-11-15..2027-11-15, publication window 2024-11-15..2026-11-15. PULL 2 pull date 2026-11-16, window 2026-11-16..2027-11-16, publication 2024-11-16..2026-11-16. PULL 3 pull date 2026-11-17, window 2026-11-17..2027-11-17, publication 2024-11-17..2026-11-17. Reaches-bank is judged against ASSET $7,054.835 million (and DEP $5,625.375 million where a threshold turns on deposits).

## 3. Open comment periods (list a)

Sorted by close date. Days left at each pull:

| Document | Agency | Title | Comment close | Days left P1 / P2 / P3 | Reaches bank |
|---|---|---|---|---|---|
| 2026-19308 | FDIC | Merger Transactions | 2026-11-23 | 8 / 7 / 6 | yes |
| 2026-19310 | FDIC | State Bank Parity | 2026-11-23 | 8 / 7 / 6 | unclear |
| 2026-22495 | FDIC | Large-Bank Deposit Insurance Determination Modernization | 2027-01-04 | 50 / 49 / 48 | unclear |

- **2026-19308 "Merger Transactions"** — FDIC proposes fundamental reform of Bank Merger Act merger processing. Who must comply: FDIC-supervised insured depository institutions filing merger applications under the Bank Merger Act. Reaches: **yes**. Threshold: the 90-day written determination applies where the resulting institution would have less than $50 billion in assets; Republic's ASSET $7.05 billion is below $50 billion, so a future Republic merger filing would fall in the 90-day category.
- **2026-19310 "State Bank Parity"** — FDIC proposes that a host State's laws apply to an out-of-State State bank's branches and services in that State to the same extent as to an out-of-State national bank's. Who must comply: out-of-State State banks providing services in a host State, and their branches there. Reaches: **unclear** — see §5.
- **2026-22495 "Large-Bank Deposit Insurance Determination Modernization"** — FDIC proposes modernising the §360.9 covered-institution test for large-bank deposit insurance determinations. Who must comply: insured depository institutions meeting the §360.9 covered-institution test. Reaches: **unclear** — see §5.

## 4. Adopted rules (list b)

Sorted by compliance date (compliance = effective date where the rule sets no separate compliance date). Two rules have an effective date in the window; five more RULEs published in the last 24 months set a compliance date in the window.

| Document | Agencies | Title | Effective | Compliance | Reaches bank |
|---|---|---|---|---|---|
| 2026-22962 | Treasury; FinCEN | Imposition of Special Measure Prohibiting the Transmittal of Funds Involving MEXC Global | 2026-12-10 | 2026-12-10 | yes |
| 2025-11244 | CFPB | Small Business Lending Under the Equal Credit Opportunity Act (Regulation B); Extension of Compliance Dates | 2025-07-18 | 2027-01-01 | unclear |
| 2025-19370 | CFPB | Small Business Lending Under the Equal Credit Opportunity Act (Regulation B); Extension of Compliance Dates | 2025-12-01 | 2027-01-01 | unclear |
| 2025-21461 | FDIC | FDIC Official Signs and Advertising Requirements, False Advertising, Misrepresentation of Insured Status, and Misuse of the FDIC's Name or Logo | — | 2027-01-01 | yes |
| 2026-21706 | Treasury; OCC | Implementing the Guiding and Establishing National Innovation for U.S. Stablecoins Act for the Issuance of Stablecoins by Entities Subject to the Jurisdiction of the Office of the Comptroller of the Currency | 2027-01-18 | 2027-01-18 | no |
| 2024-25079 | CFPB | Required Rulemaking on Personal Financial Data Rights | 2025-01-17 | 2027-04-01 | no |
| 2026-01806 | FDIC | FDIC Official Signs, Advertisement of Membership, False Advertising, Misrepresentation of Insured Status, and Misuse of the FDIC's Name or Logo | 2026-03-02 | 2027-04-01 | yes |

- **2026-22962** — FinCEN prohibits transmittals of funds from or to MEXC Global. Who must comply: covered financial institutions (as defined in 31 CFR 1010.100(t)), in respect of transmittals of funds from or to MEXC Global. Reaches: **yes** — the order defines "covered financial institution" as having the same meaning as "financial institution" in 31 CFR 1010.100(t); no asset threshold; Republic is a bank. The order states it is effective December 10, 2026, with no cessation date.
- **2025-11244** — CFPB interim final rule extending the Regulation B small-business lending compliance dates. Who must comply: covered financial institutions in Tier 2 (moderate volume lenders). Reaches: **unclear** — see §5. **Superseded — see the note below.**
- **2025-19370** — CFPB final rule adopting the 2025-11244 interim final rule with the same tier dates. Who must comply: covered financial institutions in Tier 2. Reaches: **unclear** — see §5. **Superseded — see the note below.**
- **2025-21461** — FDIC delays the compliance date for the 12 CFR 328.4 and 328.5 requirements (official digital sign on digital deposit-taking channels and ATMs) to January 1, 2027. Who must comply: insured depository institutions (IDIs). Reaches: **yes** — applies to all IDIs; no asset threshold.
- **2026-21706** — OCC regulations implementing the GENIUS Act for payment stablecoin issuance. Who must comply: entities subject to the OCC's jurisdiction issuing payment stablecoins (permitted payment stablecoin issuers, national banks, Federal savings associations, and Federal branches and agencies). Reaches: **no** — Republic is a Kentucky state bank supervised by the FDIC, not an entity subject to the OCC's jurisdiction.
- **2024-25079** — CFPB personal financial data rights rule (12 CFR part 1033). Who must comply: depository institution data providers that hold at least $10 billion in total assets but less than $250 billion (Tier 2 compliance date). Reaches: **no** — the 2027-04-01 date is for the $10B–$250B tier; Republic's ASSET $7.05B falls in the $3B–$10B tier, whose compliance date is April 1, 2028 (outside the window). Tier table (1033.121(b)): >= $250B → 2026-04-01; $10B–$250B → 2027-04-01; $3B–$10B → 2028-04-01; $1.5B–$3B → 2029-04-01; < $1.5B → 2030-04-01.
- **2026-01806** — FDIC amends the IDI signage requirements for digital deposit-taking channels and ATMs and like devices. Who must comply: IDIs. Reaches: **yes** — no asset threshold. Interplay: 2025-21461 delayed the old 328.4/328.5 requirements to January 1, 2027; 2026-01806 amends those requirements (effective March 2, 2026) with compliance required by April 1, 2027.

**Supersession note (2025-11244 / 2025-19370):** CFPB final rule 2026-08494 "Small Business Lending (Regulation B)", effective 2026-06-30, sets a single compliance date of January 1, 2028 for all covered institutions and raises the coverage threshold from 100 to 1,000 covered credit transactions for each of two consecutive years. It therefore supersedes the January 1, 2027 Tier 2 dates in 2025-11244 and 2025-19370. 2026-08494's own compliance date (2028-01-01) is outside the window, so it has no CSV row. Context document 2025-03790 (FDIC signs delay, compliance March 1, 2026) is likewise superseded by 2025-21461 and has no row.

## 5. Unclear items — what decides them

| Document | Reaches | What decides it |
|---|---|---|
| 2026-19310 State Bank Parity | unclear | Whether Republic provides services outside Kentucky (its chartering State). The FDIC record shows 48 offices and a KY-IN CBSA but not the States of its offices or services. |
| 2026-22495 Large-Bank Deposit Insurance Determination Modernization | unclear | Whether Republic has >= 250,000 deposit accounts. Deposits prong MET (DEP $5.63B >= $2B); assets prong FAILS (ASSET $7.05B < $20B); the account count is not in the FDIC excerpt. |
| 2025-11244 Small Business Lending (Reg B) extension | unclear | Republic's small-business covered-transaction originations (Tier 1 >= 2,500; Tier 2 >= 500; Tier 3 >= 100 in both years); not in the FDIC record. Also superseded by 2026-08494 (see §4). |
| 2025-19370 Small Business Lending (Reg B) extension | unclear | Same origination-volume test as 2025-11244. Also superseded by 2026-08494 (see §4). |

## 6. Changes

### Changes — PULL 2 vs PULL 1: no change

- new: 0 | gone: 0 | changed: 0 | pull 1 rows: 10 | pull 2 rows: 10 (10 = 10 + 0 − 0)
- All three list sets identical: (a) 799 PRORULEs, same 3 open, same 105 null `comments_close_on`, same 14 recent nulls; (b) same 2 RULEs with an effective date in the window; (c) same 83 RULEs published in the last 24 months, zero detail-field differences. No new RULE published 2026-11-15/16 from the four agencies; newest remains 2026-22962 (pub 2026-11-10).

### Changes — PULL 3 vs PULL 2: no change

- new: 0 | gone: 0 | changed: 0 | pull 2 rows: 10 | pull 3 rows: 10 (10 = 10 + 0 − 0)
- All three list sets identical: (a) 799 PRORULEs, same 3 open, same 105 null `comments_close_on`, same 14 recent nulls; (b) same 2 RULEs with an effective date in the window (2026-22962, 2026-21706); (c) same 83 RULEs published in the last 24 months, zero detail-field differences and zero raw-text compliance-scan differences. No new RULE published 2026-11-16/17 from the four agencies; newest remains 2026-22962 (pub 2026-11-10). The 5 in-window compliance dates are unchanged (2024-25079 2027-04-01, 2025-11244 2027-01-01, 2025-19370 2027-01-01, 2025-21461 2027-01-01, 2026-01806 2027-04-01).

## 7. PROOF

### PULL 1 (pull date 2026-11-15; note recordedAt 2026-11-15 02:26:48.084407 UTC)

- First request HTTP Date header: `Sun, 15 Nov 2026 02:07:06 GMT` (FDIC institutions query, CERT 23627).
- FDIC excerpt: NAME Republic Bank & Trust Company; ASSET 7054835 (US$ thousands); REGAGNT FDIC; REPDTE 06/30/2026; CERT 23627; STNAME Kentucky; CBSA Louisville-Jefferson County, KY-IN; OFFICES 48; ESTYMD 01/11/1982; ACTIVE 1. DEP 5625375 (US$ thousands).
- List count lines: (a) 799 PRORULEs, 3 open (comments_close_on >= 2026-11-15), 105 null comments_close_on, 691 closed; (b) 2 RULEs with effective date in 2026-11-15..2027-11-15; (c) 83 RULEs published 2024-11-15..2026-11-15.
- Requests (UTC): 02:07:06 FDIC institutions CERT:23627; ~02:07 FDIC DEP read; 02:08:42 (a) PRORULE list, 799 results; 02:08:43 (b) RULE effective-date list, 2 results; 02:08:45 (c) RULE published-24-months list, 83 results; 02:10–02:22 detail JSON for all 83 (c) RULEs + 5 (a)/(b) documents + 14 null-close PRORULEs; 02:13–02:18 raw text for all (c) documents and (a)/(b) row documents, scanned for "compliance date" (13 docs mention it; 5 set an in-window compliance date).

### PULL 2 (pull date 2026-11-16; note recordedAt 2026-11-16 02:35:33.439212 UTC)

- First request HTTP Date header: `Mon, 16 Nov 2026 02:28:37 GMT` (FDIC institutions query, CERT 23627).
- FDIC excerpt: identical to PULL 1 (NAME Republic Bank & Trust Company; ASSET 7054835; REGAGNT FDIC; REPDTE 06/30/2026; DEP 5625375).
- List count lines: (a) 799 PRORULEs, 3 open (comments_close_on >= 2026-11-16), 105 null comments_close_on; (b) 2 RULEs with effective date in 2026-11-16..2027-11-16; (c) 83 RULEs published 2024-11-16..2026-11-16.
- Requests (UTC): 02:28:37 FDIC institutions CERT:23627; 02:28 FDIC DEP read; 02:29:10 (a) PRORULE list, 799 results; 02:29:12 (b) RULE effective-date list, 2 results; 02:29:13 (c) RULE published-24-months list, 83 results; 02:30–02:32 detail JSON for all 83 (c) RULEs + 5 (a)/(b) documents + 14 null-close PRORULEs; 02:33–02:34 raw text for all (c) documents and (a)/(b) row documents, scanned for "compliance date" (14 docs mention it; 5 set an in-window compliance date).

### PULL 3 (pull date 2026-11-17; note recordedAt 2026-11-17 02:43:47.387858 UTC)

- First request HTTP Date header: `Tue, 17 Nov 2026 02:39:20 GMT` (FDIC institutions query, CERT 23627).
- FDIC excerpt: identical to PULL 1 and PULL 2 (NAME Republic Bank & Trust Company; ASSET 7054835; REGAGNT FDIC; REPDTE 06/30/2026; DEP 5625375).
- List count lines: (a) 799 PRORULEs, 3 open (comments_close_on >= 2026-11-17), 105 null comments_close_on; (b) 2 RULEs with effective date in 2026-11-17..2027-11-17; (c) 83 RULEs published 2024-11-17..2026-11-17.
- Requests (UTC): 02:39:20 FDIC institutions CERT:23627; 02:39:21 FDIC DEP read; 02:39:27 (a) PRORULE list, 799 results; 02:39:28 (b) RULE effective-date list, 2 results; 02:39:30 (c) RULE published-24-months list, 83 results; 02:40–02:42 detail JSON for all 83 (c) RULEs + 5 (a)/(b) documents + 14 null-close PRORULEs; 02:42–02:43 raw text for all (c) documents and (a)/(b) row documents, scanned for "compliance date" (14 docs mention it; 5 set an in-window compliance date).

### Per-document date and threshold sentences (PULL 3 raw texts; threshold sentences verified verbatim, whitespace-normalised)

- **2026-19308** — date: "DATES: Comments must be received on or before November 23, 2026." Threshold: "Under the proposed rule, an applicant submitting a merger filing that does not qualify for rapid or expedited processing would receive a written determination by the FDIC within 90 days after submitting a substantially complete filing if (1) the resulting institution would have less than $50 billion in assets, (2) authority to act on the filing is not reserved to the FDIC's Board of Directors, and (3) consummation of the merger transaction is not dependent upon action by another Federal regulator."
- **2026-19310** — date: "DATES: Comments must be received no later than November 23, 2026." Threshold: "the amendments would provide that, for purposes of section 24(j) of the Federal Deposit Insurance Act, the laws of a host State apply to any branch in the host State of, or any services provided in the host State by, an out-of-State State bank to the same extent such State laws apply to a branch in the host State of, or any services provided in the host State by, an out-of-State national bank."
- **2026-22495** — date: "DATES: Comments must be received by January 4, 2027." Threshold: "Section 360.9 would apply to all IDIs that have at least $2 billion in deposits and at least either: 250,000 deposit accounts; or $20 billion in total assets, regardless of the number of deposit accounts (covered institutions)."
- **2026-22962** — date: "DATES: This action is effective December 10, 2026." Threshold: "The order defines ``covered financial institution'' as having the same meaning as ``financial institution'' in 31 CFR 1010.100(t)."
- **2026-21706** — date: "DATES: The final rule is effective on January 18, 2027." Threshold: "The Office of the Comptroller of the Currency (OCC) is issuing regulations implementing the Guiding and Establishing National Innovation for U.S. Stablecoins Act regarding the issuance of payment stablecoins and certain related activities by entities subject to the OCC's jurisdiction."
- **2025-11244** — date (Tier 2 compliance): "Moderate volume lenders (Tier 2) April 1, 2025..... January 16, 2026.. January 1, 2027... June 1, 2028." Threshold: same tier-table line as the date sentence.
- **2025-19370** — date (Tier 2 compliance): "Moderate volume lenders (Tier 2) April 1, 2025..... January 16, 2026.. January 1, 2027... June 1, 2028." Threshold: same tier-table line as the date sentence.
- **2025-21461** — date: "The FDIC is delaying the March 1, 2026, compliance date to January 1, 2027." Threshold: "The compliance date for the requirements in 12 CFR 328.4 and 328.5, which was initially delayed at 89 FR 84261 (October 22, 2024) and was subsequently delayed at 90 FR 11659 (March 11, 2025), is further delayed to January 1, 2027."
- **2024-25079** — date (Tier 2 compliance): "April 1, 2027, for data providers that are: (i) Depository institutions that hold at least $10 billion in total assets but less than $250 billion in total assets; or (ii) Nondepository institutions that did not generate $10 billion or more in total receipts in both calendar year 2023 and calendar year 2024." Threshold: same tier sentence as the date sentence.
- **2026-01806** — date: "Compliance date: Compliance is required by April 1, 2027." Threshold: same sentence as the date sentence.

### CSV files

- D2 `bank-comments-23627-pull1.csv` — 10 rows, SHA-256 3ed6ea0caf0d10516bcc163bf96baacef833fe0dd670320415d284347589a760
- D3 `bank-comments-23627-pull2.csv` — 10 rows, SHA-256 3ed6ea0caf0d10516bcc163bf96baacef833fe0dd670320415d284347589a760
- D4 `bank-comments-23627-pull3.csv` — 10 rows, SHA-256 3ed6ea0caf0d10516bcc163bf96baacef833fe0dd670320415d284347589a760
- Columns (all three): document_number, agencies, type, title, comment close, effective date, compliance date, who must comply, reaches bank, threshold sentence. Sorted by operative upcoming date (comment close for PRORULEs; compliance date, else effective date, for RULEs), then document_number.
