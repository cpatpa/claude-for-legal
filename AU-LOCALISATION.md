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

## For the reviewing practitioner

Two documents support the practitioner review:

- **[`references/au-localisation/VERIFICATION-CHECKLIST.md`](references/au-localisation/VERIFICATION-CHECKLIST.md)** — every `[verify-au]` claim grouped by primary source needed (Federal Register of Legislation, AustLII case law, regulator websites, state legislation, time-sensitive thresholds, pending reforms). Use as a structured audit sweep.
- **[`references/au-localisation/SELF-AUDIT.md`](references/au-localisation/SELF-AUDIT.md)** — the AI author's own list of "places I am most likely wrong": specific commencement dates, section numbers, dollar amounts, and case citations that warrant priority spot-checking. AI hallucination on these is the failure mode this document is designed to surface.

A first-pass review using these documents takes roughly 12-18 hours; the checklist exists to make that time efficient.

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
| `references/au-localisation/` | Foundation complete (review pending) | 8 reference files: regulators, courts, AGLC4, terminology, legal profession, privilege, dates/currency/spelling |
| `employment-legal` | Pilot complete (review pending) | Fair Work Act, NES, unfair dismissal, general protections, state long service leave; CLAUDE.md, hiring-review, termination-review |
| `privacy-legal` | Pilot complete (review pending) | Privacy Act 1988 (Cth), 13 APPs, NDB scheme, OAIC enforcement, APP 8 cross-border, APP 12 access; CLAUDE.md, use-case-triage, dpa-review, dsar-response, pia-generation |
| `ip-legal` | Pilot complete (review pending) | Patents Act 1990, Copyright Act 1968, Trade Marks Act 1995, IP Australia, no DMCA equivalent, groundless threats; CLAUDE.md, takedown, clearance, oss-review |
| `litigation-legal` | Pilot complete (review pending) | Federal Court Rules 2011, state Supreme Court rules, uniform Evidence Acts, LPP dominant purpose, Calderbank offers, Part IVA class actions, costs follow event; CLAUDE.md, demand-draft, privilege-log-review |
| `corporate-legal` | Pilot complete (review pending) | Corporations Act 2001 (Cth), ASIC filings (Form 484, 388), directors' duties, continuous disclosure, schemes of arrangement, FIRB, no Delaware analogue; CLAUDE.md, entity-compliance, diligence-issue-extraction |
| `commercial-legal` | Pilot complete (review pending) | Australian Consumer Law, non-excludable consumer guarantees, UCT regime with penalties, misleading and deceptive conduct (s 18), unconscionable conduct, Modern Slavery Act; CLAUDE.md, review, nda-review |
| `regulatory-legal` | Pilot complete (review pending) | AU regulator feed sources (ASIC, ACCC, OAIC, APRA, AUSTRAC, ATO, AFCA, eSafety, ACMA), parliamentary process, no NPRM regime; CLAUDE.md, reg-feed-watcher |
| `product-legal` | Pilot complete (review pending) | ACL marketing claims (s 18, 29, 33), substantiation, country of origin (Pt 5-3), Spam Act, mandatory product safety, ACCC enforcement; CLAUDE.md, launch-review, marketing-claims-review |
| `ai-governance-legal` | Pilot complete (review pending) | Voluntary AI Safety Standard 2024 (10 Guardrails), AI Ethics Principles, proposed Mandatory Guardrails, Privacy Act ADM (Dec 2026), sectoral overlays; CLAUDE.md, aia-generation |
| `legal-clinic` | Pilot complete (review pending) | Clinical legal education context, Legal Profession Uniform Law and state Acts, ASCR, reserved legal work, common practice areas; CLAUDE.md, client-intake |
| `law-student` | Pilot complete (review pending) | Priestley 11, PLT pathway, AGLC4, no single bar exam, AU assessment formats, AI use policies; CLAUDE.md, case-brief, irac-practice |
| `legal-builder-hub` | Pilot complete (review pending) | AU QA checks for community skills, AU-compatible starter packs, US-default flagging; CLAUDE.md |

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
