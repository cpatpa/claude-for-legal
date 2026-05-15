# Australian Localisation Reference Materials

> [!CAUTION]
> **AI-generated content, not verified by an Australian legal practitioner.** Every file in this folder was drafted by Claude on the basis of publicly available materials. Treat as a research starting point, not as legal advice. Section numbers, deadlines, and procedural rules change. Always verify against the primary source before relying on anything here.
>
> Primary sources to verify against:
> - [Federal Register of Legislation](https://www.legislation.gov.au) for Commonwealth statutes
> - State and territory legislative registers (NSW, VIC, QLD, WA, SA, TAS, ACT, NT)
> - [AustLII](https://www.austlii.edu.au) for case law and unconsolidated statutes
> - Regulator websites (ASIC, ACCC, OAIC, Fair Work Commission, IP Australia, APRA, AUSTRAC, ATO, AFCA)

This folder holds the cross-cutting reference materials that every Australian-localised plugin can read from. It is the AU counterpart to the US-default content already baked into the plugins.

## Contents

| File | What's in it |
|---|---|
| `regulators.md` | Map of Australian federal and state regulators (ASIC, ACCC, OAIC, AHRC, APRA, AUSTRAC, ATO, AFCA, IP Australia, Fair Work Commission, state Fair Trading offices, state EPAs) with scope, enforcement powers, and key reporting obligations |
| `courts.md` | Australian court structure: High Court, Federal Court, Federal Circuit and Family Court, state Supreme Courts, District / County Courts, Magistrates / Local Courts, specialist tribunals (AAT, FWC, VCAT, NCAT, QCAT, SACAT, ART) |
| `citation-aglc.md` | Quick reference to AGLC4 (Australian Guide to Legal Citation, 4th edition) for cases, statutes, secondary sources |
| `terminology.md` | US to AU legal terminology mapping (attorney to solicitor / barrister / legal practitioner, work product to legal professional privilege, subpoena to subpoena / summons, discovery to disclosure, etc.) |
| `legal-profession.md` | Legal Profession Uniform Law (NSW, VIC, WA), state legal profession acts, conduct rules (ASCR), trust accounts, costs disclosure, advertising rules, AI use guidance from Law Society / Law Institute |
| `privilege.md` | Legal professional privilege in Australia: advice privilege and litigation privilege, dominant purpose test, waiver, no work product doctrine, compulsory regulator powers that can pierce LPP |
| `dates-currency-spelling.md` | DD/MM/YYYY date format, AUD currency, en-AU spelling conventions, metric units |

## How plugins use this

Each plugin's `CLAUDE.md` template references the files in this folder under a `## Jurisdiction: Australia` section. When the user's practice profile selects Australia as the primary jurisdiction, skills load the relevant AU reference and apply it instead of (or alongside) the US default.

Where a plugin has not yet been localised, the cold-start interview will still let the user choose Australia, but the skill output will carry a `[verify-au]` flag on every jurisdiction-specific claim. The user is expected to verify against the primary source.

## What this is NOT

- Not legal advice.
- Not a substitute for an Australian legal practitioner.
- Not a comprehensive treatise. Each file is a working reference for the AI agent and the reviewing lawyer, not a textbook.
- Not stable. Australian law changes. Recent examples relevant to this repository: Privacy Act amendments (tranche 1 passed 2024, tranche 2 in progress), Voluntary AI Safety Standard (2024), respect at work amendments to the Fair Work Act, Legal Profession Uniform Law extension to WA (2022).

## Verification workflow

When a skill output relies on something in this folder:

1. The output should cite the specific file and section (e.g. `regulators.md#asic`).
2. The reviewing lawyer should treat the cite as `[model knowledge — verify]` until checked against the primary source.
3. If the primary source contradicts what is in this folder, the file should be updated and the contradiction logged in commit history.

🤙
