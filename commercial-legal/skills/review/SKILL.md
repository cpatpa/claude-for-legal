---
name: review
description: >
  Review a vendor agreement, NDA, or SaaS subscription against your playbook.
  Identifies the agreement structure from titles, routes to the right review skill
  (vendor-agreement-review, nda-review, saas-msa-review), and integrates the output
  into a single memo. Use when the user says "review this contract", "check this
  MSA", "is this NDA okay", "look at this SaaS agreement", or attaches an inbound
  agreement for review.
argument-hint: '[file path | Drive link | [CLM ID] | paste text]'
---

# /review

Reviews an inbound agreement against the playbook in `~/.claude/plugins/config/claude-for-legal/commercial-legal/CLAUDE.md`. Identifies the agreement structure from titles, selects the appropriate skill(s), and — if confirm_routing is enabled — checks with the user before proceeding.

## Instructions

1. **Load `~/.claude/plugins/config/claude-for-legal/commercial-legal/CLAUDE.md`.** If placeholders present, stop and prompt: "Run `/commercial-legal:cold-start-interview` first — I need to learn your playbook before I can review against it."

   Also read `~/.claude/plugins/config/claude-for-legal/commercial-legal/CLAUDE.md` → `## Review preferences` → `confirm_routing`. If the field is missing, treat it as `true`.

2. **Get the agreement:** From file path, Drive link, [CLM ID], or pasted text. If none provided, ask.

3. **Read the document structure — titles first.**

   Before reading the body, extract:
   - The main agreement title (e.g., "Master Services Agreement", "Non-Disclosure Agreement")
   - All exhibit, schedule, addendum, and attachment titles (e.g., "Exhibit A — Data Processing Addendum", "Schedule 1 — Subscription Order Form", "Annex B — Service Level Agreement")

   This is the routing signal. Do not rely on body keywords alone — a 40-page MSA with "confidential" throughout is not an NDA.

4. **Select the skill(s) based on document structure.**

   Map each identified document or section to a skill:

   | Document / section title contains | Skill |
   |---|---|
   | Non-Disclosure, NDA, Confidentiality Agreement (as the *main* agreement) | **nda-review** |
   | Master Services Agreement, Professional Services, Statement of Work, Consulting Agreement | **vendor-agreement-review** |
   | Subscription, SaaS, Cloud Services, Order Form with auto-renewal, Software License with recurring fees | **saas-msa-review** (overlay on vendor-agreement-review) |
   | Data Processing Addendum, DPA, Data Processing Agreement (as exhibit or standalone) | note for **vendor-agreement-review** → data protection section |
   | Service Level Agreement, SLA (as exhibit) | note for **saas-msa-review** → SLA section |

   Multiple skills may apply. Common combinations:
   - MSA + DPA exhibit → vendor-agreement-review, with DPA noted
   - SaaS subscription + Order Form + SLA exhibit → saas-msa-review (covers all three)
   - MSA + Order Form with auto-renewal → vendor-agreement-review + saas-msa-review overlay

   When the structure is genuinely ambiguous after reading titles (e.g., a document titled "Agreement" with no exhibits listed), read the first two pages of the body to resolve it — then stop and route.

5. **Confirm routing if enabled.**

   If `confirm_routing` is `true` in `~/.claude/plugins/config/claude-for-legal/commercial-legal/CLAUDE.md` (or field is absent):

   ```
   I'm going to review this as: [agreement type(s)].

   Documents identified:
   - [Main agreement title] → [skill]
   - [Exhibit A title] → [how it will be handled]
   - [Exhibit B title] → [how it will be handled]

   Sound right? (yes / no — or tell me what I got wrong)
   ```

   Wait for confirmation before proceeding. If the user corrects the routing, apply their instruction and proceed.

   If `confirm_routing` is `false`: proceed silently. Log the routing decision at the top of the review memo so the user can see what was applied.

6. **Run the skill(s).** Follow each skill's workflow fully. If multiple skills apply, run them in sequence and integrate the output into a single memo — don't produce separate memos.

7. **Check for escalations:** If any issue exceeds the reviewer's authority per the `~/.claude/plugins/config/claude-for-legal/commercial-legal/CLAUDE.md` matrix, invoke **escalation-flagger** to route and draft the ask.

8. **Offer follow-ups:**
   - Stakeholder summary for the business owner
   - Redline .docx with tracked changes
   - [CLM] record creation (if connected)
   - Add to renewal register (if auto-renewal found)

## Configuring confirm_routing

Add to `~/.claude/plugins/config/claude-for-legal/commercial-legal/CLAUDE.md` → `## Review preferences`:

```markdown
## Review preferences

confirm_routing: true   # Set to false to skip routing confirmation and proceed automatically
```

The cold-start interview should ask about this preference. Default is `true` — confirmation on. As trust builds, the user can set it to `false`.

## Examples

```
/commercial-legal:review vendor-msa.pdf
```

```
/commercial-legal:review https://drive.google.com/file/d/ABC123
```

```
/commercial-legal:review
[paste agreement text]
```

## Australian framework (if AU is the relevant jurisdiction)

> AI-generated. Verify against the Australian Consumer Law and current ACCC guidance.

When reviewing an AU contract, apply these overlays in addition to the playbook:

- **Non-excludable ACL consumer guarantees** (ss 51-59, 64): apply to goods/services supplied to "consumers" (under A$100,000 OR personal use). Contract clauses purporting to exclude or modify these are void; attempting to do so is itself a contravention (s 29(1)(m)). Flag any "AS IS" or "to the fullest extent permitted by law" wording in consumer-facing supply.
- **Unfair contract terms (ACL s 23-28)**: applies to standard form contracts with consumers OR small businesses (fewer than 100 employees OR annual turnover < A$10M, applied to the counterparty). Penalty for using an unfair term (from 9 November 2023): greater of A$50M / 3x benefit / 30% adjusted turnover. Scan for the s 25 example list: one-sided termination, unilateral variation, automatic renewal traps, liability cap disproportionate to risk, jurisdiction restrictions.
- **Misleading and deceptive conduct (ACL s 18)**: pre-contractual statements, marketing material, conduct during negotiation. Strict liability. Survives "entire agreement" clauses to a significant degree (the entire-agreement clause does not exclude s 18 claims).
- **Unconscionable conduct (ss 20-22)**: section 20 (common law equivalent) high threshold; section 21 (statutory) broader, applies to business transactions.
- **Privacy and security**: for contracts involving personal information, ensure APP 8 (cross-border accountability), APP 11 (security), and NDB scheme assistance obligations are addressed. AU has no statutory "DPA" requirement; this is contractual.
- **Penalty doctrine**: AU penalty doctrine narrower than the historical US position; *Andrews v ANZ Banking Group* (2012) 247 CLR 205 and *Paciocco* (2016) 258 CLR 525 set the test. Genuine pre-estimate of loss permitted; punitive liquidated damages not.
- **Modern Slavery Statement**: if either party has revenue > A$100M, supply chain due diligence and reporting obligations apply.
- **Payment Times Reporting Act 2020 (Cth)**: entities with revenue > A$100M must report payment practices to small business suppliers twice yearly.
- **Governing law / dispute resolution**: NSW, Victoria, WA are common AU governing-law defaults. Foreign governing law on AU consumer contracts may not exclude ACL.
- **Spelling, dates, currency**: AUD, DD/MM/YYYY, en-AU spelling.
- **"AS IS" disclaimers** do not override ACL non-excludable guarantees; the supplier remains liable. Flag aggressively in AU consumer-facing contracts.

Tag every AU-specific claim `[verify-au]` until checked.

---

## Output

Full review memo per the skill's format. Routing decision logged at the top. Deviation-by-deviation, specific redline language, named approver. Saved where `~/.claude/plugins/config/claude-for-legal/commercial-legal/CLAUDE.md` → House style says work product goes.
