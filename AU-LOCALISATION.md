# Australian Localisation

> [!CAUTION]
> **This is an AI-generated localisation in progress.** Every page in this localisation, including this one, was drafted by Claude on the basis of publicly available materials. It has not been verified by an Australian legal practitioner. Treat all content as a research starting point, not as legal advice or a statement of Australian law. A lawyer admitted in the relevant Australian jurisdiction must review, verify, and take professional responsibility for anything that leaves the building.
>
> **Known limitations:**
> - AI hallucination risk on statute names, section numbers, case citations, and procedural timeframes. Always verify against the primary source (Federal Register of Legislation, AustLII, state legislative registers, regulator websites).
> - The law in Australia is federated. Statutes and procedural rules differ between the Commonwealth, the six states, and two territories. Skills that reference "Australian law" need to be checked against the specific jurisdiction in scope.
> - The original repository was built for a United States legal market. Cross-cutting US assumptions (work product privilege, FRCP/FRE, regulator structure, citation format) remain in plugins that have not yet been localised. See the status table below.
> - This localisation does not cover Aboriginal and Torres Strait Islander customary law, which sits alongside Australian state and federal law in specific contexts.
>
> **Report errors:** open an issue against this repository or flag inline with a `[verify-au]` tag in skill output.

This document tracks the Australian localisation of Claude for Legal. The original repository assumes United States law as default. This localisation adds Australian regulatory, statutory, procedural, and terminology content and flags where US-specific framing remains.

## What localisation means here

For each plugin, localisation covers:

1. **Terminology**: US legal terms (attorney, work product, subpoena, discovery, deposition) replaced or supplemented with Australian equivalents (solicitor / barrister / legal practitioner, legal professional privilege, subpoena / summons, disclosure / production, examination).
2. **Statutes and case law**: US statutes (FMLA, Title VII, CCPA, Lanham Act, DMCA) replaced or supplemented with Australian equivalents (Fair Work Act 2009 (Cth), Privacy Act 1988 (Cth), Australian Consumer Law, Trade Marks Act 1995 (Cth), Copyright Act 1968 (Cth)).
3. **Regulators**: US agencies (SEC, FTC, EEOC, USPTO) replaced or supplemented with Australian regulators (ASIC, ACCC, Fair Work Commission, IP Australia). See `references/au-localisation/regulators.md`.
4. **Procedural rules**: FRCP / FRE replaced or supplemented with Federal Court Rules 2011 (Cth) and state court rules, Evidence Act 1995 (Cth) and state evidence acts.
5. **Citation**: Bluebook style replaced with the Australian Guide to Legal Citation (AGLC4). See `references/au-localisation/citation-aglc.md`.
6. **Privilege**: US "attorney work product" doctrine replaced with Australian legal professional privilege analysis. See `references/au-localisation/privilege.md`.
7. **Spelling and units**: en-US replaced with en-AU. USD replaced with AUD. Date format DD/MM/YYYY.
8. **Professional conduct**: ABA Model Rules replaced with Legal Profession Uniform Law (NSW / VIC / WA from 2022) and equivalent state conduct rules. See `references/au-localisation/legal-profession.md`.

## Localisation status

| Plugin | Status | Notes |
|---|---|---|
| `references/au-localisation/` | In progress | Foundation reference materials being built |
| `employment-legal` | Pilot complete (review pending) | Fair Work Act, NES, unfair dismissal, state long service leave added to CLAUDE.md, hiring-review, termination-review |
| `privacy-legal` | Pilot complete (review pending) | Privacy Act 1988 (Cth), 13 APPs, NDB scheme, OAIC enforcement, APP 8 cross-border, APP 12 access added to CLAUDE.md, use-case-triage, dpa-review, dsar-response, pia-generation |
| `ip-legal` | Not started | Needs IP Australia, Patents Act 1990, Copyright Act 1968, Trade Marks Act 1995, no DMCA equivalent |
| `litigation-legal` | Not started | Needs Federal Court Rules, state Supreme Court rules, state Evidence Acts |
| `corporate-legal` | Not started | Needs Corporations Act 2001, ASIC filing calendar, no Delaware analogue |
| `commercial-legal` | Not started | Largely jurisdiction-neutral, needs Australian Consumer Law lens, AU misleading and deceptive conduct doctrine |
| `regulatory-legal` | Not started | Needs ASIC, APRA, ACCC, OAIC, AUSTRAC, ATO feed sources |
| `product-legal` | Not started | Needs Australian Consumer Law, misleading and deceptive conduct, ACCC enforcement posture |
| `ai-governance-legal` | Partial | Multi-jurisdiction table already names Australian AI Ethics Framework; needs Voluntary AI Safety Standard, Privacy Act amendments, ACCC AI enforcement |
| `legal-clinic` | Not started | Needs PLT and supervised practice context, state law society oversight |
| `law-student` | Not started | Needs Australian law school structure, Priestley 11, AGLC citation, PLT pathway |
| `legal-builder-hub` | Not started | Largely jurisdiction-neutral |

## How to use this localisation

1. Read `references/au-localisation/README.md` for the index of foundation materials.
2. When setting up a plugin's cold-start interview, choose "Australia" as the primary jurisdiction and select the relevant state(s).
3. Skills that have been localised will note the localisation in their output header. Skills that have not been localised will continue to apply US-default framing and should be treated with extra scrutiny.
4. The `⚠️ Reviewer note` block above every deliverable is the principal place AU-specific caveats and verification requirements are surfaced.

## Contributing

Localisation contributions follow the same patterns as the rest of the repository (see `CONTRIBUTING.md`). When proposing AU content:

- Cite to the primary source. AustLII or the Federal Register of Legislation for statutes, AustLII for case law.
- Note the state or territory if the rule varies.
- Flag where the rule is unsettled or where there is interstate divergence.
- Do not assume Commonwealth law overrides state law without checking the constitutional power and any state carve-outs.
- Use AGLC4 citation style.

🤙
