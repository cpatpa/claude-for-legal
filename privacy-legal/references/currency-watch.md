# Privacy Currency Watch

**Last verified: 2026-05-10.**

> **⚠️ Staleness check.** If the last-verified date above is more than 90 days old, treat this file as stale and verify each entry before relying on it. A stale watch list is worse than no watch list — it looks current while being wrong. When a skill reads this file, check the last-verified date first. If stale, say: "The currency watch was last verified [date] — [N] months ago. I'm using it as a checklist of areas to search, not as a source of current status." When you update any entry, also update the last-verified date at the top.

Privacy law moves. Before relying on an effective date, threshold, or obligation, verify it. These are the areas most likely to have moved since model training:

## COPPA (16 CFR Part 312)

- **2025 Amendments — compliance deadline April 22, 2026.** Major changes: biometric identifiers and government IDs are now "personal information"; separate verifiable parental consent required for third-party disclosure tied to targeted advertising; written information security program mandatory; indefinite retention prohibited.
- A plugin that knows pre-2025 COPPA looks competent while being stale. Verify at [FTC COPPA page](https://www.ftc.gov/legal-library/browse/rules/childrens-online-privacy-protection-rule-coppa).

## State privacy laws (comprehensive)

The map grows every year. As of May 2026, comprehensive privacy laws in force or imminent: CA (CCPA/CPRA), VA, CO, CT, UT, IA, IN, TN, MT, OR, TX, FL, DE, NH, NJ, KY, MD, MN, NE, RI. Check the IAPP state law tracker for current effective dates and the most recent additions.

## Cross-border transfers

- **EU-US DPF** in force since July 2023. Subject to Schrems III litigation — verify it's still valid before relying.
- **UK-US Data Bridge** in force since October 2023.
- **Swiss-US DPF** in force since September 2024.
- For any transfer that relies on an adequacy decision, check the EU Commission's current adequacy list.

## FTC enforcement trends

- **FTC v. Humor Rainbow/OkCupid (March 2026):** Undisclosed sharing of user data with a third party for AI training as a §5 violation. Flag for any DPA or privacy policy review involving AI training pathways.
- Health data: FTC's expansive reading of the Health Breach Notification Rule (GoodRx, BetterHelp, Premom settlements). Verify current scope.
- Dark patterns: FTC's pattern of treating confusing consent flows as deceptive. Verify current enforcement posture.

## DSAR response timelines

CCPA: 45 days + 45-day extension with notice. GDPR: 1 month + 2-month extension. Other states vary — verify the specific state's window. The plugin defaults may be out of date for the newest states.

## Australia (AI-generated; verify against OAIC, AustLII, Federal Register of Legislation)

> All items in this AU section carry `[verify-au]` status. AU privacy law is in active reform.

### Tranche 1 reforms (Privacy and Other Legislation Amendment Act 2024)

- **Statutory tort for serious invasion of privacy**: commenced 10 June 2025 `[verify-au]`. Limited to intentional or reckless invasions; serious; without consent or other justification; balanced against public interest.
- **Civil penalty cap raised**: serious or repeated interference now greater of A$50M / 3x benefit / 30% adjusted turnover. New tiered penalties for less serious contraventions.
- **Extraterritorial application broadened**: s 5B amended to remove the "collect or hold in Australia" requirement.
- **ADM (automated decision-making) notice obligations**: from December 2026 `[verify-au]`. APP entities must include in APP 5 collection notices and APP 1 privacy policies information about substantially automated decisions significantly affecting individuals.
- **Children's Online Privacy Code**: OAIC code in development as of 2025 `[verify-au]`.

### Tranche 2 reforms (proposed, not yet enacted)

- **Small business operator exemption** (s 6D, < A$3M turnover): proposal to remove. Status: not enacted `[verify-au]`.
- **Employee records exemption** (s 7B(3)): proposal to narrow. Status: not enacted `[verify-au]`.
- **Mandatory PIA for high privacy risk activities**: proposal. Status: not enacted `[verify-au]`.
- **Right to erasure**: proposal. Status: not enacted `[verify-au]`.
- **Direct right of action**: proposal. Status: not enacted `[verify-au]`.

### NDB scheme

- 30-day assessment window (s 26WH). "As soon as practicable" notification after determining eligible breach. Verify if any reform tightens.

### Cross-border (APP 8)

- No SCCs / adequacy. AU continues accountability framework. Watch for any reform aligning with international transfer mechanisms.

### Consumer Data Right (CDR)

- Banking live 2020, energy live 2022. Telecommunications expansion proposed `[verify-au]`. Action initiation framework in development.

### State health records

- *Health Records Act 2001* (Vic), *Health Records and Information Privacy Act 2002* (NSW), *Health Records (Privacy and Access) Act 1997* (ACT) overlay the Privacy Act. Watch for state amendments.

### Verify-at sources (AU)

- OAIC: oaic.gov.au/news-and-publications
- Federal Register of Legislation: legislation.gov.au
- Treasury Privacy Act review: treasury.gov.au/consultation
- AustLII Federal Court daily: austlii.edu.au

---

## How to use this file

When a skill cites a privacy rule, effective date, or threshold, it should note: "Privacy law is moving — this may have changed since my training. Verify at [source]. See `references/currency-watch.md`."

**This file goes stale.** Current as of May 2026. Update when you notice drift.
