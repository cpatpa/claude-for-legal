# AU Localisation Verification Checklist

> [!IMPORTANT]
> **For the reviewing Australian legal practitioner.** This file inventories the AI-generated claims in the AU localisation that require verification against a primary source before the localisation can be relied on. Items are grouped by the source where verification is most efficient. Each row notes the file and line where the claim appears.
>
> AI content was generated against publicly available materials. Even where the content appears accurate, the practitioner should verify before sign-off because:
> 1. Effective dates, thresholds, and penalty caps change.
> 2. Pending reform status can shift between drafting and use.
> 3. AI section number and case citation hallucination is a known failure mode.
>
> When an item is confirmed, replace the `[verify-au]` tag in the source file with `[verified YYYY-MM-DD by [initials] against [source URL or citation]]`. When an item is found wrong, fix the source file in the same commit and note the correction here.

## Verification by source

### Federal Register of Legislation (legislation.gov.au)

Primary source for Commonwealth Acts and consolidated text.

| Claim | File | Status |
|---|---|---|
| Fair Work Act 2009 (Cth) s 117 minimum notice scale (1/2/3/4 weeks + 1 wk if 45+ with 2 yrs service) | employment-legal/CLAUDE.md `## Australian framework`, hiring-review, termination-review | TBV |
| Fair Work Act 2009 (Cth) s 119 redundancy pay scale (4-16 weeks for 1-10+ yrs) | employment-legal/CLAUDE.md | TBV |
| Fair Work Act 2009 (Cth) s 121 small business redundancy exemption | employment-legal/CLAUDE.md | TBV |
| Fair Work Act 2009 (Cth) s 382 unfair dismissal eligibility (6 months / 12 months small business) | employment-legal | TBV |
| Fair Work Act 2009 (Cth) s 394 21-day clock for unfair dismissal application | employment-legal | TBV |
| Fair Work Act 2009 (Cth) s 366 21-day clock for general protections dismissal | employment-legal | TBV |
| Fair Work Act 2009 (Cth) s 387 unfair dismissal criteria | employment-legal/termination-review | TBV |
| Fair Work Act 2009 (Cth) s 389 genuine redundancy defence | employment-legal/termination-review | TBV |
| Fair Work Act 2009 (Cth) s 124 Fair Work Information Statement obligation | employment-legal/hiring-review | TBV |
| Fair Work Act 2009 (Cth) s 125B Casual Employment Information Statement | employment-legal/hiring-review | TBV |
| Fair Work Act 2009 (Cth) s 15A new casual definition (from 26 August 2024) | employment-legal/hiring-review | TBV |
| Fair Work Act 2009 (Cth) s 15AA contractor classification test (from 26 August 2024) | employment-legal/hiring-review | TBV |
| Fair Work Act 2009 (Cth) s 333B-D pay secrecy ban (from 7 December 2022) | employment-legal/hiring-review | TBV |
| Fair Work Act 2009 (Cth) s 357 sham contracting civil penalty | employment-legal/CLAUDE.md | TBV |
| Fair Work Act 2009 (Cth) s 361 reverse burden in general protections | employment-legal/CLAUDE.md | TBV |
| Privacy Act 1988 (Cth) APP 1-13 numbering and substance | privacy-legal/CLAUDE.md | TBV |
| Privacy Act 1988 (Cth) s 6D small business operator exemption (turnover ≤ A$3M) | privacy-legal/CLAUDE.md | TBV |
| Privacy Act 1988 (Cth) s 7B(3) employee records exemption | privacy-legal/CLAUDE.md, dsar-response | TBV |
| Privacy Act 1988 (Cth) s 5B extraterritorial application (post 2024 amendments) | privacy-legal/CLAUDE.md | TBV |
| Privacy Act 1988 (Cth) s 13G civil penalty for serious interference (greater of A$50M / 3x benefit / 30% turnover) | privacy-legal/CLAUDE.md | TBV |
| Privacy Act 1988 (Cth) Part IIIC NDB scheme: 30-day assessment, "as soon as practicable" notification | privacy-legal/CLAUDE.md | TBV |
| Privacy Act 1988 (Cth) s 26WH 30-day assessment window | privacy-legal/CLAUDE.md | TBV |
| Privacy and Other Legislation Amendment Act 2024 (Cth): introduces tort, raises penalties, ADM notice obligations | privacy-legal/CLAUDE.md, ai-governance-legal/CLAUDE.md, product-legal/CLAUDE.md | TBV |
| Statutory tort for serious invasion of privacy commencement date (claimed: 10 June 2025) | privacy-legal/CLAUDE.md:429 | TBV |
| ADM notice obligations commencement (claimed: December 2026) | multiple files | TBV |
| Corporations Act 2001 (Cth) ss 180-184 directors' duties | corporate-legal/CLAUDE.md | TBV |
| Corporations Act 2001 (Cth) s 674 continuous disclosure | corporate-legal/CLAUDE.md | TBV |
| Continuous disclosure penalty (claimed A$525,000 / A$2,625,000 per contravention) | corporate-legal/CLAUDE.md:270 | TBV |
| Corporations Act 2001 (Cth) s 411 schemes of arrangement | corporate-legal/CLAUDE.md | TBV |
| Corporations Act 2001 (Cth) s 142 registered office | corporate-legal/CLAUDE.md, entity-compliance | TBV |
| Corporations Act 2001 (Cth) s 153 quote ACN on documents | corporate-legal/CLAUDE.md | TBV |
| Corporations Act 2001 (Cth) s 588G insolvent trading | corporate-legal/diligence-issue-extraction | TBV |
| Corporations Act 2001 (Cth) s 911A AFSL obligation | corporate-legal/CLAUDE.md | TBV |
| Corporations Act 2001 (Cth) s 912A general obligations | ai-governance-legal/CLAUDE.md | TBV |
| Small proprietary thresholds (2 of 3: < A$50M revenue, < A$25M assets, < 100 employees) | corporate-legal | TBV |
| Patents Act 1990 (Cth) s 120 infringement proceedings forum | ip-legal/CLAUDE.md | TBV |
| Patents Act 1990 (Cth) s 119C experimental use defence | ip-legal/CLAUDE.md | TBV |
| Patents Act 1990 (Cth) s 128 groundless threats | ip-legal/CLAUDE.md, litigation-legal/demand-draft | TBV |
| Patents Act 1990 (Cth) s 163 Crown use | ip-legal/CLAUDE.md | TBV |
| Patents Act 1990 (Cth) s 70 pharmaceutical patent term extension | ip-legal/CLAUDE.md | TBV |
| Trade Marks Act 1995 (Cth) ss 39, 41, 42, 43, 44, 60, 61 examination grounds | ip-legal/clearance | TBV |
| Trade Marks Act 1995 (Cth) s 10 deceptive similarity definition | ip-legal/clearance | TBV |
| Trade Marks Act 1995 (Cth) s 92 removal for non-use (3 years / 5 years) | ip-legal/CLAUDE.md, clearance | TBV |
| Trade Marks Act 1995 (Cth) s 60 well-known marks | ip-legal/CLAUDE.md | TBV |
| Trade Marks Act 1995 (Cth) s 120(3) well-known mark infringement | ip-legal/CLAUDE.md | TBV |
| Trade Marks Act 1995 (Cth) s 129 groundless threats | ip-legal/CLAUDE.md | TBV |
| Trade Marks Act 1995 (Cth) s 185 defensive registrations | ip-legal/clearance | TBV |
| Copyright Act 1968 (Cth) s 35(6) employer ownership in course of employment | ip-legal/CLAUDE.md | TBV |
| Copyright Act 1968 (Cth) s 35(5) commissioned works | ip-legal/CLAUDE.md | TBV |
| Copyright Act 1968 (Cth) Part IX moral rights | ip-legal/CLAUDE.md | TBV |
| Copyright Act 1968 (Cth) ss 116AA-116AJ safe harbour (extended 2018) | ip-legal/CLAUDE.md, takedown | TBV |
| Copyright Act 1968 (Cth) s 115A site-blocking injunctions | ip-legal/CLAUDE.md, takedown | TBV |
| Copyright Act 1968 (Cth) s 115(4) flagrant infringement additional damages | ip-legal/takedown | TBV |
| Copyright Act 1968 (Cth) s 202 groundless threats | ip-legal/CLAUDE.md | TBV |
| Copyright Act 1968 (Cth) ss 116AN-116AS TPM circumvention | ip-legal/CLAUDE.md | TBV |
| Copyright Act 1968 (Cth) Part XIA performers' rights | ip-legal/CLAUDE.md | TBV |
| Designs Act 2003 (Cth) s 77 groundless threats | ip-legal/CLAUDE.md | TBV |
| Designs Act 2003 (Cth) 5-year term renewable to 10 | ip-legal/CLAUDE.md | TBV |
| Competition and Consumer Act 2010 (Cth) Schedule 2 (Australian Consumer Law) | commercial-legal, product-legal | TBV |
| ACL s 18 misleading and deceptive conduct (strict liability) | commercial-legal, product-legal, ip-legal | TBV |
| ACL ss 20-22 unconscionable conduct | commercial-legal, product-legal | TBV |
| ACL ss 23-28 unfair contract terms regime | commercial-legal, product-legal | TBV |
| ACL s 24 unfair contract terms test | commercial-legal | TBV |
| ACL s 25 example list of unfair terms | commercial-legal | TBV |
| ACL s 29 false or misleading representations | product-legal/marketing-claims-review | TBV |
| ACL ss 30-37 specific false representations | product-legal/marketing-claims-review | TBV |
| ACL s 33 misleading conduct as to nature of goods | product-legal/marketing-claims-review | TBV |
| ACL s 34 misleading conduct as to services | product-legal/marketing-claims-review | TBV |
| ACL s 37 false representations in business activities | product-legal/marketing-claims-review | TBV |
| ACL ss 51-59 consumer guarantees | commercial-legal, ip-legal/oss-review | TBV |
| ACL s 64 non-excludable guarantees | commercial-legal | TBV |
| ACL s 131 mandatory reporting of consumer goods causing serious injury (2 days) | product-legal/launch-review | TBV |
| ACL s 232 injunctions | commercial-legal | TBV |
| ACL s 236 damages | commercial-legal | TBV |
| ACL s 237 compensation orders | commercial-legal | TBV |
| ACL s 246 corrective orders | commercial-legal | TBV |
| ACL Part 5-3 country of origin | product-legal/marketing-claims-review | TBV |
| ACL "consumer" definition (under A$100,000 OR personal/household use) | commercial-legal | TBV |
| UCT penalty regime (greater of A$50M / 3x benefit / 30% turnover, from 9 November 2023) | commercial-legal, product-legal | TBV |
| UCT small business threshold (fewer than 100 employees OR turnover < A$10M, from 9 November 2023) | commercial-legal | TBV |
| Spam Act 2003 (Cth) consent, identification, unsubscribe requirements | product-legal/launch-review, marketing-claims-review | TBV |
| Do Not Call Register Act 2006 (Cth) | product-legal/launch-review | TBV |
| Modern Slavery Act 2018 (Cth) reporting threshold A$100M | commercial-legal, corporate-legal | TBV |
| Modern Slavery Act 2018 (NSW) | commercial-legal/CLAUDE.md | TBV |
| Payment Times Reporting Act 2020 (Cth) revenue threshold A$100M | commercial-legal | TBV |
| AML/CTF Act 2006 (Cth) tranche 2 commencement (1 July 2026 claimed) | regulators.md | TBV |
| Online Safety Act 2021 (Cth) | product-legal | TBV |
| Therapeutic Goods Act 1989 (Cth) | product-legal | TBV |
| Federal Court of Australia Act 1976 (Cth) Part IVA class actions | litigation-legal/CLAUDE.md | TBV |
| Supreme Court Act 1986 (Vic) Part 4A group costs orders | litigation-legal/CLAUDE.md | TBV |
| Civil Procedure Act 2005 (NSW) Part 10 class actions | litigation-legal/CLAUDE.md | TBV |
| Federal Court Rules 2011 (Cth) discovery + practice note GPN-DISC | litigation-legal/CLAUDE.md | TBV |
| Federal Court Rules 2011 (Cth) Part 25 offers of compromise | litigation-legal/demand-draft | TBV |
| Evidence Act 1995 (Cth) ss 117-126 privilege | litigation-legal/privilege-log-review | TBV |
| Evidence Act 1995 (Cth) s 131 without prejudice | litigation-legal/CLAUDE.md, demand-draft | TBV |
| UCPR (NSW) Part 20 offers of compromise | litigation-legal | TBV |
| UCPR (NSW) Part 33 subpoenas | litigation-legal/CLAUDE.md | TBV |
| Acts Interpretation Act 1901 (Cth) | law-student/irac-practice | TBV |
| Restraints of Trade Act 1976 (NSW) s 4 read-down power | employment-legal/CLAUDE.md, hiring-review, commercial-legal/nda-review | TBV |
| Privacy Act amendments effective dates: tranche 1 / tranche 2 | privacy-legal/CLAUDE.md | TBV |
| Customs Act 1901 (Cth) Notice of Objection regime | ip-legal/CLAUDE.md | TBV |

### Case law on AustLII (austlii.edu.au)

| Citation | Proposition | File |
|---|---|---|
| *Esso Australia Resources Ltd v Commissioner of Taxation* (1999) 201 CLR 49 | Dominant purpose test for LPP | privilege.md, litigation-legal |
| *Mann v Carnell* (1999) 201 CLR 1 | Waiver of LPP (inconsistency test) | privilege.md, litigation-legal |
| *Waterford v Commonwealth* (1987) 163 CLR 54 | In-house counsel privilege | privilege.md, litigation-legal/privilege-log-review |
| *Calderbank v Calderbank* [1976] Fam 93 | Without prejudice save as to costs offers | litigation-legal/CLAUDE.md, demand-draft |
| *Mabo v Queensland (No 2)* (1992) 175 CLR 1 | AGLC citation example; native title | citation-aglc.md, law-student |
| *Coco v A N Clark (Engineers) Ltd* [1969] RPC 41 | Breach of confidence three elements | privacy-legal, ip-legal/oss-review, commercial-legal/nda-review |
| *Smith Kline & French Laboratories (Aust) Ltd v Secretary, Department of Community Services and Health* (1990) 22 FCR 73 | Breach of confidence adopted | ip-legal/CLAUDE.md |
| *AWB Ltd v Cole (No 5)* (2006) 155 FCR 30 | Privilege over investigations | privilege.md |
| *Voth v Manildra Flour Mills* | Forum non conveniens (clearly inappropriate forum) | terminology.md |
| *BMW Australia Ltd v Brewster* (2019) 269 CLR 574 | Common fund orders | litigation-legal/CLAUDE.md |
| *Knight v FP Special Assets* (1992) 174 CLR 178 | Non-party costs orders | litigation-legal/CLAUDE.md |
| *British American Tobacco Australia Services Ltd v Cowell* (2002) 7 VR 524 | Document preservation | litigation-legal/CLAUDE.md |
| *Palavi v Queensland Newspapers Pty Ltd* [2012] NSWSC 1352 | Document preservation | litigation-legal/CLAUDE.md |
| *Andrews v ANZ Banking Group* (2012) 247 CLR 205 | Penalty doctrine | commercial-legal/review |
| *Paciocco* (2016) 258 CLR 525 | Penalty doctrine | commercial-legal/review |
| *Codelfa Construction Pty Ltd v State Rail Authority of NSW* (1982) 149 CLR 337 | Contract construction, surrounding circumstances | law-student/irac-practice |
| *Toll (FGCT) Pty Ltd v Alphapharm Pty Ltd* (2004) 219 CLR 165 | Objective theory of contract | law-student/irac-practice |
| *CIC Insurance Limited v Bankstown Football Club Ltd* (1997) 187 CLR 384 | Purposive statutory interpretation | law-student/irac-practice |
| *Donoghue v Stevenson* [1932] AC 562 | Negligence | law-student/irac-practice |
| *Hedley Byrne & Co Ltd v Heller & Partners Ltd* [1964] AC 465 | Negligent misstatement | law-student |
| *Caparo Industries Plc v Dickman* [1990] 2 AC 605 | Duty of care | law-student/irac-practice |
| *Sullivan v Moody* (2001) 207 CLR 562 | Novel duty categories in AU | law-student/irac-practice |
| *Carlill v Carbolic Smoke Ball Co* [1893] 1 QB 256 | Unilateral contract | law-student/irac-practice |
| *Walton's Stores (Interstate) Ltd v Maher* (1988) 164 CLR 387 | Unified estoppel | terminology.md, law-student/irac-practice |
| *Frazer v Walker* [1967] 1 AC 569 | Torrens system indefeasibility | law-student/irac-practice |
| *Lange v Australian Broadcasting Corporation* (1997) 189 CLR 520 | Implied freedom of political communication | law-student/irac-practice |
| *Plaintiff S157/2002 v Commonwealth* (2003) 211 CLR 476 | Constitutional judicial review | law-student/irac-practice |
| *Salomon v A Salomon & Co Ltd* [1897] AC 22 | Corporate personality | law-student |
| *In re Queen's University at Kingston*, 820 F.3d 1287 (Fed. Cir. 2016) | Patent agent privilege (US case retained for non-AU users) | ip-legal/CLAUDE.md |

### Regulator websites and guidance

| Source | Claim | File |
|---|---|---|
| ASIC website | Form 484 28-day deadline | corporate-legal/entity-compliance |
| ASIC website | Form 388 annual lodgement requirements | corporate-legal/entity-compliance |
| ASIC INFO 271 | Algorithmic trading guidance | ai-governance-legal/CLAUDE.md |
| ASIC INFO 230 | Electronic disclosure | ai-governance-legal/CLAUDE.md |
| ASIC Report 720 | AI in financial services | ai-governance-legal/CLAUDE.md |
| ASX Listing Rule 3.1 | Continuous disclosure carve-outs | corporate-legal/CLAUDE.md |
| OAIC APP Guidelines | All 13 APPs interpretation | privacy-legal |
| OAIC Guide to Undertaking Privacy Impact Assessments | Methodology stages | privacy-legal/pia-generation |
| OAIC Guide to securing personal information | APP 11 security guidance | privacy-legal/pia-generation |
| OAIC Children's Online Privacy Code | Status (consultation as of 2025) | multiple files |
| OAIC Privacy (Australian Government Agencies — Governance) APP Code 2017 | Mandatory PIA for high-risk Cth agency projects | privacy-legal/pia-generation |
| ACCC website | Penalty regime (greater of A$50M / 3x benefit / 30% turnover post 2022) | product-legal, commercial-legal |
| ACCC "Making environmental claims" guidance (June 2023) | 8 principles | product-legal/marketing-claims-review |
| AHRC Respect@Work report (2020) | NDA restrictions recommendation | employment-legal/termination-review |
| Sex Discrimination Act 1984 (Cth) s 47C positive duty | In force from 12 December 2023 | regulators.md, employment-legal/CLAUDE.md |
| APRA CPS 230 operational risk | In force 1 July 2025 | ai-governance-legal/CLAUDE.md, regulators.md |
| APRA CPS 234 information security | regulators.md | TBV |
| DISR Voluntary AI Safety Standard (September 2024) 10 Guardrails | ai-governance-legal/CLAUDE.md, aia-generation | TBV |
| DISR proposed Mandatory Guardrails for High-Risk AI consultation (September 2024) | ai-governance-legal/CLAUDE.md | TBV |
| Australia's AI Ethics Principles (8) | ai-governance-legal/CLAUDE.md | TBV |
| ART (Administrative Review Tribunal) commenced 14 October 2024 | regulators.md, courts.md | TBV |
| ASCR Rule 10 (former client) | legal-clinic/client-intake | TBV |
| ASCR Rule 11 (concurrent client) | legal-clinic/client-intake | TBV |
| ASCR Rule 33 (communicating with represented party) | legal-clinic/client-intake | TBV |

### State legislation (state legislative registers)

| State | Act | Provision | File |
|---|---|---|---|
| NSW | *Restraints of Trade Act 1976* (NSW) | s 4 read-down power | employment-legal, commercial-legal/nda-review |
| NSW | *Civil Procedure Act 2005* (NSW) | Part 10 class actions | litigation-legal/CLAUDE.md |
| NSW | *Uniform Civil Procedure Rules 2005* (NSW) | Part 20 offers, Part 33 subpoenas | litigation-legal |
| NSW | *Long Service Leave Act 1955* (NSW) | LSL entitlements | employment-legal/CLAUDE.md |
| NSW | *Health Records and Information Privacy Act 2002* (NSW) | Health records | privacy-legal/CLAUDE.md |
| NSW | *Anti-Discrimination Act 1977* (NSW) | State anti-discrim | employment-legal/CLAUDE.md |
| Vic | *Long Service Leave Act 2018* (Vic) | LSL entitlements | employment-legal/CLAUDE.md |
| Vic | *Civil Procedure Act 2010* (Vic) | Procedure | litigation-legal/CLAUDE.md |
| Vic | *Supreme Court Act 1986* (Vic) Part 4A | Class actions + group costs orders | litigation-legal/CLAUDE.md |
| Vic | *Equal Opportunity Act 2010* (Vic) | Anti-discrim | employment-legal/CLAUDE.md |
| Vic | *Occupational Health and Safety Act 2004* (Vic) | WHS | employment-legal/CLAUDE.md |
| Vic | *Health Records Act 2001* (Vic) | Health records | privacy-legal/CLAUDE.md |
| Qld | *Industrial Relations Act 2016* (Qld) | State/local govt | employment-legal/CLAUDE.md |
| Qld | *Public Interest Disclosure Act 2010* (Qld) | Whistleblower | employment-legal/CLAUDE.md |
| Qld | *Civil Proceedings Act 2011* (Qld) Part 13A | Class actions | litigation-legal/CLAUDE.md |
| Qld | *Uniform Civil Procedure Rules 1999* (Qld) | Procedure | litigation-legal/CLAUDE.md |
| WA | *Industrial Relations Act 1979* (WA) | State system | employment-legal/CLAUDE.md |
| WA | *Legal Profession Uniform Law Application Act 2022* (WA) | Effective 1 July 2022 | legal-profession.md |
| WA | *Rules of the Supreme Court 1971* (WA) | Procedure | litigation-legal/CLAUDE.md |
| SA | *Equal Opportunity Act 1984* (SA) | Anti-discrim | employment-legal/CLAUDE.md |
| SA | *Long Service Leave Act 1987* (SA) | LSL | employment-legal/CLAUDE.md |
| SA | *Uniform Civil Rules 2020* (SA) | Procedure | litigation-legal/CLAUDE.md |
| SA | *Legal Practitioners Act 1981* (SA) | Profession | legal-profession.md |
| Tas | *Long Service Leave Act 1976* (Tas) | LSL | employment-legal/CLAUDE.md |
| Tas | *Anti-Discrimination Act 1998* (Tas) | Anti-discrim | employment-legal/CLAUDE.md |
| ACT | *Long Service Leave Act 1976* (ACT) | LSL | employment-legal/CLAUDE.md |
| ACT | *Health Records (Privacy and Access) Act 1997* (ACT) | Health records | privacy-legal/CLAUDE.md |
| NT | *Long Service Leave Act 1981* (NT) | LSL | employment-legal/CLAUDE.md |
| NT | *Anti-Discrimination Act 1992* (NT) | Anti-discrim | employment-legal/CLAUDE.md |

### Time-sensitive thresholds and rates (verify currency)

These claims involve numbers that change. Verify at the time of use, not just at sign-off.

| Claim | Value claimed | File | Source |
|---|---|---|---|
| Superannuation guarantee rate | 11.5% as at 2024-2025, 12% from 1 July 2025 | employment-legal/hiring-review, corporate-legal/diligence-issue-extraction | ATO website |
| FWA high income threshold | A$175,000 from 1 July 2024 | employment-legal | FWC website |
| Privacy Act small business turnover threshold | A$3M | privacy-legal/CLAUDE.md | OAIC website |
| UCT small business threshold | < 100 employees OR < A$10M turnover (post 9 Nov 2023) | commercial-legal | ACCC website |
| Modern Slavery threshold | A$100M revenue | commercial-legal, corporate-legal | Federal Register |
| Payment Times Reporting threshold | A$100M revenue | commercial-legal | Treasury |
| Penalty cap (Privacy Act s 13G; ACL; UCT) | greater of A$50M / 3x benefit / 30% turnover | privacy-legal, commercial-legal, product-legal | regulator websites |
| Continuous disclosure penalty | A$525,000 individual / A$2,625,000 body corporate | corporate-legal/CLAUDE.md | ASIC website |
| Small proprietary company test | 2 of 3: < A$50M revenue, < A$25M assets, < 100 employees | corporate-legal | ASIC |
| NES annual leave entitlement | 4 weeks (5 weeks shift workers) | employment-legal | Fair Work |
| NES personal/carer's leave | 10 days/year FT | employment-legal | Fair Work |
| Family and domestic violence leave | 10 days paid (from 1 Feb 2023 / 1 Aug 2023 small business) | employment-legal/CLAUDE.md | Fair Work |
| GST rate | 10% | terminology.md | ATO |
| Patents Act standard patent term | 20 years | ip-legal/CLAUDE.md | IP Australia |
| Trade Marks Act registration term | 10 years renewable | ip-legal/CLAUDE.md | IP Australia |
| Copyright term | Life + 70 years (post 2005 FTA reforms) | ip-legal/CLAUDE.md | Federal Register |
| Designs Act term | 5 years renewable to 10 | ip-legal/CLAUDE.md | IP Australia |
| Innovation patent | Abolished for new applications from 26 August 2021 | ip-legal/CLAUDE.md | IP Australia |
| Director ID | Required since November 2022 (initial deadline 5 April 2022 for existing directors) | corporate-legal | ABRS |
| AGM timing | Within 5 months of FY end (s 250N) | corporate-legal/CLAUDE.md | Corporations Act |

### Pending reform status (verify current status before use)

These claims describe proposals or amendments whose status changes. Verify current parliamentary or regulator status.

| Reform | Claim | File |
|---|---|---|
| Non-compete reform | Commonwealth proposals to ban or restrict (2024-2025) | employment-legal/CLAUDE.md, hiring-review |
| Privacy Act tranche 2 reforms | Small business exemption removal, employee records narrowing, mandatory PIA, right to erasure | privacy-legal/CLAUDE.md |
| Statutory tort for serious invasion of privacy | Commenced 10 June 2025 claim | privacy-legal/CLAUDE.md:429 |
| ADM notice obligations | From December 2026 | multiple files |
| OAIC Children's Online Privacy Code | Status as of 2025 | multiple files |
| AML/CTF Act tranche 2 (lawyers, accountants, etc.) | From 1 July 2026 | regulators.md |
| Climate-related Financial Disclosure | Treasury Laws Amendment (Sustainability Reporting) Act | corporate-legal/entity-compliance |
| DISR Mandatory Guardrails for High-Risk AI | Consultation 2024; not enacted | ai-governance-legal/CLAUDE.md, aia-generation |
| Casual Employee post-Closing Loopholes No 2 | FWA s 15A, s 66AAB from 26 August 2024 | employment-legal/hiring-review |
| Contractor classification post-Closing Loopholes No 2 | FWA s 15AA from 26 August 2024 | employment-legal/hiring-review |
| Sex Discrimination Act s 47C positive duty | In force 12 December 2023; AHRC compliance powers | regulators.md, employment-legal/CLAUDE.md |
| ACL UCT penalty regime | Penalties from 9 November 2023 | commercial-legal, product-legal |
| ART replaced AAT | 14 October 2024 | regulators.md, courts.md |

## How to use this checklist

1. **Foundation first**: review `references/au-localisation/` files (regulators, courts, AGLC4, terminology, legal-profession, privilege, dates-currency-spelling). Everything else hangs off these.
2. **Statute and case spot-check**: pick a sample of 10-15 statute references and 5-8 case citations from the tables above. Verify each against the primary source. If the sample passes, sample more. If it fails, expand the audit.
3. **Time-sensitive thresholds**: confirm each is current as at the verification date. Tag with verification date.
4. **Pending reform status**: confirm whether each reform is in force, in consultation, or has progressed. Update the localisation files accordingly.
5. **State-by-state references**: if your practice profile narrows to one state, prioritise that state's verification.

## Highest-risk claims (sample for first-pass audit)

If short on time, start here:

1. **Privacy Act statutory tort commencement date** (claimed 10 June 2025): privacy-legal/CLAUDE.md:429. Wrong date here would mislead an entire workflow.
2. **ADM notice obligation effective date** (claimed December 2026): multiple files. Same downstream impact.
3. **FWA high income threshold** (claimed A$175,000 from 1 July 2024): employment-legal. This is indexed annually; check current value at the FWC website.
4. **Superannuation guarantee rate trajectory** (11.5% → 12% on 1 July 2025): employment-legal/hiring-review. Verify ATO published rate.
5. **Continuous disclosure penalty** (A$525,000 / A$2,625,000): corporate-legal/CLAUDE.md:270. These look low; confirm against current Corporations Act / ASIC penalty unit values.
6. **Privacy Act small business turnover threshold** (A$3M): privacy-legal/CLAUDE.md. Foundational; many other claims depend on this.
7. **UCT small business definition** (post 9 Nov 2023): commercial-legal. Threshold drives whether the regime applies.
8. **Closing Loopholes No 2 effective dates** (claimed 26 August 2024 for casual and contractor definitions): employment-legal/hiring-review. Cross-check FWA s 15A and s 15AA.
9. **AGLC4 citation conventions**: references/au-localisation/citation-aglc.md. Sample 10 citations against the published AGLC.
10. **All groundless threats provisions** (Patents s 128, TM s 129, Copyright s 202, Designs s 77): ip-legal/CLAUDE.md and litigation-legal/demand-draft. Wrong section numbers would mislead C&D drafting.

🤙
