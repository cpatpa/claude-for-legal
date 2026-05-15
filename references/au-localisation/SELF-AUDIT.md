# Self-Audit: Known-Uncertain AU Content

> [!IMPORTANT]
> **From the AI author of the localisation.** This document flags content that I (Claude, the AI) wrote with lower confidence and that the practitioner reviewer should prioritise. It is not a substitute for the full `VERIFICATION-CHECKLIST.md`; it is a smaller, sharper list of "places I am most likely wrong".

## High-uncertainty content

### 1. Specific commencement dates I asserted

I generated the following dates from training data and they may be off by months or by the entire reform:

| Date claim | File | Why uncertain |
|---|---|---|
| Statutory tort for serious invasion of privacy: **commenced 10 June 2025** | privacy-legal/CLAUDE.md:429 | The Privacy and Other Legislation Amendment Act 2024 introduced the tort, but the commencement date depends on regulations and the Governor-General's proclamation. The 10 June 2025 date was my best guess; verify against the Federal Register of Legislation. |
| ADM notice obligation: **from December 2026** | multiple files | The Act sets a delayed commencement; the specific date depends on regulations. Verify before relying. |
| AML/CTF tranche 2: **from 1 July 2026** | regulators.md | Tranche 2 amendments expanding reporting entities (lawyers, accountants, etc.) have a commencement date set by the Act and Regulations. Verify. |
| APRA CPS 230: **in force 1 July 2025** | ai-governance-legal/CLAUDE.md, regulators.md | APRA published CPS 230 with a stated commencement date; verify the in-force date and any transitional provisions. |
| FWA s 15A casual definition + s 15AA contractor test: **from 26 August 2024** | employment-legal/hiring-review | Closing Loopholes No 2 Act 2024 sections commenced on specific dates; verify the actual commencement of each provision. |
| Sex Discrimination Act s 47C positive duty: **in force 12 December 2023** | regulators.md, employment-legal/CLAUDE.md | The Respect at Work amendments staged commencement; verify the AHRC compliance power start date separately. |
| ART replaced AAT: **14 October 2024** | regulators.md, courts.md | I recall this is correct but the exact date should be confirmed. |
| Tax legislation: I assumed superannuation guarantee rate is 11.5% from 1 July 2024 and 12% from 1 July 2025 | employment-legal/hiring-review | ATO publishes the legislated trajectory; verify current and forward rates. |

### 2. Specific section numbers I asserted

I generated section numbers from training data. AI section-number hallucination is a known failure mode. Spot-check these in particular:

| Section | Claim | File |
|---|---|---|
| Privacy Act s 13G | Civil penalty for serious interference | privacy-legal/CLAUDE.md |
| Privacy Act s 26WH | 30-day assessment window for NDB | privacy-legal/CLAUDE.md |
| Privacy Act s 26WK, s 26WL | Notification obligations | privacy-legal/CLAUDE.md |
| Privacy Act s 16C | APP 8 exceptions | privacy-legal/CLAUDE.md |
| FWA s 333B-D | Pay secrecy ban | employment-legal/hiring-review |
| FWA s 66AAB | Casual conversion pathway | employment-legal/hiring-review |
| Corporations Act s 250N | AGM timing | corporate-legal/CLAUDE.md |
| Corporations Act s 250U | Two strikes rule | corporate-legal/CLAUDE.md |
| Corporations Act s 588G | Insolvent trading | corporate-legal/diligence-issue-extraction |
| Corporations Act s 606 | 20% rule for takeovers | corporate-legal/CLAUDE.md |
| Patents Act s 119C | Experimental use defence (in force from April 2012) | ip-legal/CLAUDE.md |
| Trade Marks Act s 120(3) | Well-known mark infringement | ip-legal/CLAUDE.md |
| Trade Marks Act s 185 | Defensive registrations | ip-legal/clearance |
| Copyright Act ss 116AN-116AS | TPM circumvention | ip-legal/CLAUDE.md |
| Customs Act 1901 (Cth) Subdivision C of Division 12 | Employer sanctions Migration Act | employment-legal/hiring-review |
| Migration Act 1958 (Cth) Subdivision C of Division 12 | Employer sanctions | employment-legal/hiring-review |

The above should each be quoted from the Federal Register before relying.

### 3. Specific dollar amounts and thresholds

| Amount | Claim | File | Uncertainty |
|---|---|---|---|
| A$525,000 / A$2,625,000 | Continuous disclosure penalty per contravention | corporate-legal/CLAUDE.md:270 | Penalty units in AU are indexed; the absolute dollar value drifts. I picked figures consistent with my training-era penalty unit value but they should be checked against the current Crimes Act 1914 (Cth) s 4AA penalty unit value. |
| A$175,000 | FWA high income threshold | employment-legal | Indexed annually each 1 July; verify current value. |
| A$3M | Privacy Act small business turnover threshold | privacy-legal/CLAUDE.md | Threshold has historical stability but verify post-tranche 2 status. |
| A$50M | UCT, ACL, Privacy Act penalty cap (alternative limb of greater-of) | multiple | Cap is fixed; verify it has not moved. |
| A$10M | UCT small business turnover threshold | commercial-legal | Verify post-9 November 2023 figure. |
| A$100M | Modern Slavery / Payment Times Reporting threshold | commercial-legal, corporate-legal | Verify both Acts independently. |
| A$525,000 small claim threshold (mentioned as Vic class action threshold?) | (not directly asserted but related claims) | TBV |

### 4. Specific case citations and ratios

Cases I cited from training data. AI case-citation hallucination is also a known failure mode. Spot-check:

| Case | What I asserted | File |
|---|---|---|
| *AWB Ltd v Cole (No 5)* (2006) 155 FCR 30 | Investigation privilege | privilege.md |
| *British American Tobacco Australia Services Ltd v Cowell* (2002) 7 VR 524 | Document preservation | litigation-legal/CLAUDE.md |
| *Palavi v Queensland Newspapers Pty Ltd* [2012] NSWSC 1352 | Document preservation | litigation-legal/CLAUDE.md |
| *Voth v Manildra Flour Mills* | Forum non conveniens test | terminology.md |
| *BMW Australia Ltd v Brewster* (2019) 269 CLR 574 | Common fund orders | litigation-legal/CLAUDE.md |
| *Knight v FP Special Assets* (1992) 174 CLR 178 | Non-party costs | litigation-legal/CLAUDE.md |
| *Sullivan v Moody* (2001) 207 CLR 562 | AU diverging from UK on duty of care | law-student/irac-practice |

I'm reasonably confident on *Esso* (1999), *Mann v Carnell* (1999), *Mabo (No 2)* (1992), *Calderbank*, *Donoghue v Stevenson*, *Codelfa*, *Toll v Alphapharm*, *Walton's Stores*, *CIC Insurance* — these are well-known and frequently cited. Even so, verify the year and reporter against the case.

### 5. Things I deliberately didn't include because confidence was low

To flag what's missing:

- I did not write detailed jurisdiction-by-jurisdiction state Long Service Leave entitlement tables (entitlement structure varies and I would have hallucinated).
- I did not produce specific dollar amounts for state payroll tax thresholds.
- I did not address Aboriginal and Torres Strait Islander legal questions (native title, customary law); the localisation defers to specialist practitioners.
- I did not produce a full list of modern awards or pinpoint specific award classifications.
- I did not address tax-specific calculations (PAYG, FBT, CGT, GST mechanics) beyond signposting.
- I did not produce detailed corporate transaction documents (sample SPAs, schemes documents); the localisation describes the regime without drafting.

### 6. Areas where I am most uncertain at a conceptual level

- **Privilege over AI prompts and outputs**: this is novel. My characterisation (`references/au-localisation/privilege.md`) reflects general principles but no specific Australian case law squarely on point yet (as of my training cutoff). A practitioner reviewing should consider whether current case law has emerged.
- **AML/CTF tranche 2 application to lawyers**: the substance of the obligations on legal practitioners is being developed through subordinate legislation; my account is general.
- **Children's privacy code content**: in development; my description is at the proposed-content level only.
- **Class action funder regulation**: rapidly evolving; particularly around MIS classification post-Litigation Funding Schemes regulations.

## What I am NOT uncertain about

Some of the content is well-grounded and should not need detailed audit:

- The general structure of the Priestley 11 (law-student/CLAUDE.md).
- The general AGLC4 citation conventions (citation-aglc.md).
- The split between solicitors and barristers in AU practice (legal-profession.md).
- The general framework that Privacy Act has APPs, that the ACL has consumer guarantees, that the Corporations Act regulates AU companies. Sections may be off; the framework is right.
- The general statement that AU has no work product doctrine equivalent and uses dominant purpose for LPP.

## Recommended audit sequence

1. **Highest leverage**: practitioner reviews `references/au-localisation/regulators.md`, `courts.md`, `legal-profession.md`, `privilege.md` against current websites. ~2 hours.
2. **Time-sensitive**: spot-check the 10 items in `VERIFICATION-CHECKLIST.md` → "Highest-risk claims" section. ~1 hour.
3. **Section number spot-check**: pull 10 random rows from `VERIFICATION-CHECKLIST.md` → "Federal Register of Legislation". Verify each against legislation.gov.au. ~30 minutes. If 8/10 pass, sample more; if multiple fail, expand audit.
4. **Case citation spot-check**: 5 cases from the case law table. ~30 minutes.
5. **Plugin-by-plugin walkthrough**: read each plugin's CLAUDE.md AU framework section end-to-end. ~30 minutes per plugin. Focus first on the practice areas you actually use.
6. **Per-skill walkthrough**: read the AU framework block in each pilot-localised skill. ~10 minutes per skill.

Total practitioner time for a thorough first-pass review: roughly 12-18 hours. The verification checklist exists so the practitioner can prioritise.

🤙
