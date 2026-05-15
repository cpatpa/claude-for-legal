---
name: hiring-review
description: >
  Review an offer letter and any restrictive covenants — jurisdiction check
  included. Substantive rules (covenant enforceability, pay-transparency,
  salary-history limits, exemption criteria) are researched per hire, not
  stored. Use when the user says "review this offer", "can we use a
  non-compete here", "check this offer letter", "hiring in [state]", or
  attaches an offer.
argument-hint: "[offer letter file, or describe the hire]"
---

# /hiring-review

1. Load `~/.claude/plugins/config/claude-for-legal/employment-legal/CLAUDE.md` → jurisdictional footprint, hiring review triggers, restrictive covenant policy.
2. Use the workflow below.
3. Check: jurisdiction, classification, restrictive covenants, background check compliance.
4. Flag anything that hits the jurisdiction-specific escalation table.

---

## Matter context

**Matter context.** Check `## Matter workspaces` in the practice-level CLAUDE.md. If `Enabled` is `✗` (the default for in-house users), skip the rest of this paragraph — skills use practice-level context and the matter machinery is invisible. If enabled and there is no active matter, ask: "Which matter is this for? Run `/employment-legal:matter-workspace switch <slug>` or say `practice-level`." Load the active matter's `matter.md` for matter-specific context and overrides. Write outputs to the matter folder at `~/.claude/plugins/config/claude-for-legal/employment-legal/matters/<matter-slug>/`. Never read another matter's files unless `Cross-matter context` is `on`.

---

## Purpose

Offer letters are mostly boilerplate until they're not. The jurisdiction check
and the restrictive-covenant check are where this skill earns its keep. The
skill does not state the law — every jurisdiction-specific rule is researched
and cited at the time of review.

## Load context

`~/.claude/plugins/config/claude-for-legal/employment-legal/CLAUDE.md` → jurisdictional footprint, hiring review triggers, restrictive
covenant policy, offer letter template location.

## Output header

Prepend the work-product header from `~/.claude/plugins/config/claude-for-legal/employment-legal/CLAUDE.md` → `## Outputs` (it differs by user role — see `## Who's using this`).

## Workflow

### Step 1: Jurisdiction

Where will this person work? Not where HQ is — where *they* are.

If remote: their home state/country governs. If hybrid: usually their home
state, but check the offer letter's choice-of-law clause (may or may not hold
up).

Check the jurisdiction table in `~/.claude/plugins/config/claude-for-legal/employment-legal/CLAUDE.md` for this state/country. If it's
not in the table — new jurisdiction — flag that: "First hire in [state]. The
jurisdiction table doesn't cover this. Research needed before offer goes out."

### Step 2: Classification

Exempt or non-exempt? The offer should say, and the role should support it.

| Test | Check |
|---|---|
| Salary basis | Paid a fixed salary regardless of hours? |
| Salary level | Above the applicable federal and state thresholds? |
| Duties test | Does the role actually involve the exempt duties? |

> **Research before calling exemption.** Identify the currently operative
> salary thresholds (federal and state — several states index annually and
> several have tiered thresholds by employer size) and the applicable duties
> test(s) for the role. Cite primary sources. Verify currency.

If the offer says exempt but the role description does not support the
exempt duties — flag it. Misclassification is expensive.

### Step 3: Restrictive covenants

If the offer includes a non-compete, customer non-solicit, employee
non-solicit, or confidentiality/IP assignment:

> **Research enforceability before advising.** For the employee's jurisdiction,
> identify the currently operative rules on each restrictive covenant in the
> offer. Non-compete enforceability in particular has shifted in multiple
> states in recent years through legislation, agency action, and litigation —
> do not rely on prior memory of which states permit non-competes. Note:
> - The specific type of covenant (non-compete, customer non-solicit, employee
>   non-solicit, confidentiality/trade-secret, IP assignment) — each has its
>   own rules.
> - Any salary or income threshold that conditions enforceability.
> - Any notice, consideration, or garden-leave requirements.
> - Any industry-specific carve-outs (e.g., healthcare, broadcasting).
> - Duration and geographic-scope reasonableness tests.
> - Choice-of-law and choice-of-forum enforceability for out-of-state covenants.
> Cite primary sources. Verify currency.

Per `~/.claude/plugins/config/claude-for-legal/employment-legal/CLAUDE.md` restrictive covenant policy: does this hire even get one?
Some companies use them selectively. Apply the house policy first, then
research overlays from the jurisdiction.

> **No silent supplement.** If a research query to the configured legal research tool returns few or no results for the jurisdiction's exemption thresholds, restrictive-covenant rules, pay-transparency law, or any other item you're researching, report what was found and stop. Do NOT fill the gap from web search or model knowledge without asking. Say: "The search returned [N] results from [tool]. Coverage appears thin for [jurisdiction / topic]. Options: (1) broaden the search query, (2) try a different research tool, (3) search the web — results will be tagged `[web search — verify]` and should be checked against a primary source before relying, or (4) flag as unverified and stop. Which would you like?" A lawyer decides whether to accept lower-confidence sources.
>
> **Source attribution.** Tag every citation in the review with where it came from: `[Westlaw]`, `[CourtListener]`, or the MCP tool name for citations retrieved from a legal research connector; `[web search — verify]` for web-search citations; `[model knowledge — verify]` for citations recalled from training data; `[user provided]` for citations the user supplied. Citations tagged `verify` carry higher fabrication risk and should be checked first. Never strip or collapse the tags.

### Step 4: Jurisdiction-specific requirements

Check the `~/.claude/plugins/config/claude-for-legal/employment-legal/CLAUDE.md` table for this jurisdiction. Common categories to
research for each hire:

- **Pay transparency** — does the jurisdiction require a salary range in the
  posting? If so, is this offer within the posted range? Research the current
  rule (including any recent amendments or new enforcement guidance).
- **Ban-the-box** — does the jurisdiction or locality restrict the timing or
  scope of criminal-history inquiries?
- **Salary-history limits** — is the jurisdiction one that restricts asking
  about or relying on prior salary? Research current rules and recent
  amendments.
- **Required offer-letter or onboarding notices** — some jurisdictions require
  specific notices at offer or hire (wage-notice statutes, sick-leave notices,
  etc.). Research what is currently required and whether a template exists.

Cite primary sources. Verify currency.

### Step 5: Offer letter content

Read the letter. Check:

**Employment-at-will is US-only.** "At-will" means either party can terminate without cause or notice (subject to statutory exceptions). This concept does not exist outside the US:

- **US (most states):** At-will is the default. Offer letters often include "at-will" language to defeat implied-contract arguments. Check that it's present if US.
- **Montana:** Not at-will. Wrongful Discharge from Employment Act requires cause after probation.
- **UK:** No at-will. Employees have statutory protections from day 1 (unfair dismissal after 2 years of service, automatic unfair dismissal for protected reasons from day 1). The offer letter must contain the written statement of particulars (ERA 1996 s.1): pay, hours, notice period, holidays, pension, disciplinary/grievance procedures.
- **EU:** No at-will. Termination requires cause, notice, and often works council consultation or collective redundancy procedures. The offer letter requirements vary by member state but notice periods and written particulars are standard.
- **Australia:** No at-will. See the Australian framework below.
- **Canada:** No at-will. Common law reasonable notice (can be months), ESA minimums, wrongful dismissal exposure.
- **Singapore, other APAC:** No at-will. Employment Act and contract-based protections.

---

### Australian framework for hiring review

> When the work jurisdiction identified in Step 1 is in Australia, apply this framework in addition to the steps above. This block is AI-generated and must be reviewed by an Australian legal practitioner before acting on it. Tag every Australian-specific claim `[verify-au]` until checked against the primary source (Fair Work Act, modern award, state Act, IP Australia / ASIC register, etc.).

**Source stack to check (in order):**

1. **Fair Work Act 2009 (Cth)** and the National Employment Standards. Identify whether the employee will be in the national system (almost all private sector employers are; state and local government employees in some states are not).
2. **Modern award or enterprise agreement** that covers the role and industry. Coverage is determined by the industry and the role's classification, not by what the employer or employee prefers. The role must be classified within the applicable award's classification structure. Check whether the proposed remuneration meets or exceeds the award rate including loadings, allowances, and penalty rates.
3. **State long service leave Act** in the relevant state or territory.
4. **State anti-discrimination Act** in the relevant state or territory (overlaying Commonwealth Acts).
5. **Common law restraint of trade** and (NSW only) the *Restraints of Trade Act 1976* (NSW).

**Required content of an Australian offer / employment contract:**

- Position title and classification under any applicable modern award.
- Start date.
- Status: permanent (full-time / part-time), maximum-term / fixed-term, or casual. Casual employee definition is set in the Fair Work Act and the role must in substance be casual; the contract label alone is not determinative.
- Remuneration: base salary, superannuation (currently 11.5% of OTE, scheduled to reach 12% on 1 July 2025 `[verify-au]`), any allowances, any annualised salary arrangement that absorbs award entitlements (must comply with the applicable award's annualised wage clause).
- Hours of work.
- Notice period (must meet NES s 117 minimum on each side).
- Probation period if any (probation does not displace unfair dismissal protections; the minimum employment period under s 382(a) FWA is the relevant gate, not the contractual probation).
- Annual leave, personal/carer's leave, parental leave references (NES floor).
- Confidentiality, IP assignment.
- Restrictive covenants (see below).
- Termination provisions consistent with NES.
- Mandatory provision of the **Fair Work Information Statement** to all new employees (s 124 FWA). Casual employees must additionally receive the **Casual Employment Information Statement** (s 125B FWA).

**No at-will in Australia.** Do not include "employment at will" language in an Australian offer. Replace with the agreed notice period each way (must meet NES minimum on the employer side; the employee side may match or differ).

**Restrictive covenants in AU:**

- Default position: an enforceable post-employment restraint requires (a) a legitimate interest to protect (confidential information, customer connection, staff stability), and (b) a restraint that is reasonable in scope (duration, geography, activity).
- **NSW**: courts can read down an unreasonable restraint under s 4 *Restraints of Trade Act 1976* (NSW). This makes broader cascading clauses survive in NSW that would not in other states.
- **Other states**: blue-pencil severance only. Courts will not rewrite an unreasonable clause; they may sever a complete sub-clause.
- **Consideration**: a restraint introduced mid-employment requires fresh consideration (a payment or a clear benefit) beyond continued employment.
- **2024-2025 reform alert**: the Commonwealth has announced proposals to ban or restrict non-compete clauses below an income threshold. Verify current status before drafting or advising. `[verify-au]`
- For executive hires: check whether the contract is below the FWA "high income threshold" (currently A$175,000 from 1 July 2024 `[verify-au]`). High-income employees not covered by an award have unfair dismissal access only if under the threshold.

**Classification and award coverage:**

- The award classification is a question of fact (what does the role actually do?), not preference.
- "Set-off" or annualised salary arrangements can absorb award entitlements only if the contract is clear and the salary in fact exceeds what the award would require taking into account loadings, allowances, and penalty rates. Underpayment risk is acute; multi-million dollar back-pay liabilities and civil penalties have been imposed on major employers.
- Casual classification: the *Fair Work Legislation Amendment (Closing Loopholes No. 2) Act 2024* (Cth) introduced a new definition of casual employee (s 15A) and a casual conversion pathway (s 66AAB) effective from 26 August 2024. `[verify-au]`
- Independent contractor classification: s 15AA FWA (effective 26 August 2024) sets a multi-factor "real substance, practical reality, and true nature" test. ATO superannuation tests apply separately under the *Superannuation Guarantee (Administration) Act 1992* (Cth).

**Background checks and right to work:**

- Right to work: VEVO check via Department of Home Affairs for non-citizens. Employer sanctions for knowingly employing unlawful non-citizens under the *Migration Act 1958* (Cth) Subdivision C of Division 12.
- Police checks: nationally coordinated criminal history check via accredited bodies. State-by-state spent convictions schemes (e.g. *Criminal Records Act 1991* (NSW)) prevent reliance on certain old convictions.
- Working with Children Check: state-by-state schemes (e.g. WWCC in NSW, WWC Check in Vic). Mandatory for child-related work.
- Privacy Act 1988 (Cth) APP 3 limits collection of personal information to what is reasonably necessary for the employer's functions. Employee records exemption (s 7B(3)) applies to current and former employees but NOT to job candidates.

**Pay transparency / pay equity:**

- *Workplace Gender Equality Act 2012* (Cth) gender pay gap reporting for employers with 100+ employees (WGEA). Public disclosure of employer-level gender pay gaps commenced February 2024.
- *Sex Discrimination Act 1984* (Cth) and *Fair Work Act 2009* (Cth) prohibit pay secrecy clauses (FWA ss 333B-D from 7 December 2022): employees have a workplace right to disclose or not disclose their remuneration.

**Output additions for AU hires (in addition to the standard output structure):**

- Note the **applicable modern award (or "award-free, above high income threshold")** and the classification under that award.
- Note **superannuation rate** applied and confirm super fund stapling has been considered.
- Note any **restraint of trade** clause and the enforceability analysis under the work state's doctrine, including the 2024-2025 reform status if a non-compete is included.
- Note **state long service leave** Act applicable and any portability scheme.
- Confirm **Fair Work Information Statement** (and Casual Employment Information Statement, if applicable) will be provided.

---

**Check for at-will language ONLY if the jurisdiction is US.** For non-US jurisdictions, check instead for: notice period (and whether it meets statutory minimum), the written-statement particulars the jurisdiction requires, probation period terms, and any jurisdiction-specific mandatory clauses.

**Never recommend adding at-will language to a non-US offer letter.** It's legally meaningless, it can conflict with mandatory statutory terms, and it signals to the employee's lawyer that the employer didn't understand the jurisdiction.

- At-will language present and not undermined elsewhere (US only, see above)
- Contingencies clear (background check, reference, I-9 if US, VEVO right-to-work check if Australia, equivalent right-to-work check for the applicable jurisdiction)
- Start date, title, salary, reporting structure stated
- Equity terms (if any) consistent with the plan
- Integration clause so the letter is the whole deal
- For non-US: notice period meets statutory minimum, jurisdiction's required written-statement particulars included, probation period compliant with local rules
- For Australia: modern award coverage identified and remuneration meets award floor; Fair Work Information Statement to be provided; superannuation rate compliant; restraint enforceable under work state's doctrine

## Output

> **Jurisdiction assumption.** This review applies the rules of the employee's work jurisdiction identified in Step 1. Enforceability of restrictive covenants, exemption thresholds, pay-transparency obligations, salary-history limits, and required notices vary materially by state and locality, and several have shifted recently. If the candidate's work location changes, or the role spans jurisdictions, this review may not apply as written.

```markdown
[WORK-PRODUCT HEADER — per plugin config ## Outputs — differs by role; see `## Who's using this`]

## Hiring Review: [Candidate] — [Role] — [Jurisdiction]

**Overall:** [Clear to send | Changes needed | Escalate]

### Jurisdiction: [State/Country]
[Jurisdiction table entry. Any auto-escalate triggers that fire.]

### Classification
[Exempt/non-exempt call, grounded in researched thresholds and duties test.
Any flags.]

### Restrictive covenants
[If any. Enforceability call per researched jurisdiction rules, with pinpoint
cites and currency note. Suggested changes.]

### Jurisdiction-specific requirements
[Pay transparency, notices, salary-history rules, etc. — each researched and
cited, or flagged as needing research.]

### Offer letter
[Any issues with the letter itself]

### Action items
- [ ] [specific change needed before sending]
```

## Consequential-action gate (make an offer)

**Before producing a "Clear to send" recommendation or a final offer letter for signature:** Read `## Who's using this` in `~/.claude/plugins/config/claude-for-legal/employment-legal/CLAUDE.md`. If the Role is **Non-lawyer**:

> Making an offer has legal consequences — the letter is a contract, and restrictive covenants, classification, and jurisdiction-specific terms are difficult to reset once sent. Have you reviewed this offer with an attorney? If yes, proceed. If no, here's a brief to bring to them:
>
> - Candidate, role, jurisdiction (where they'll actually work)
> - Classification call (exempt/non-exempt) and why
> - Restrictive covenants in the offer and the enforceability analysis
> - Jurisdiction-specific requirements that apply (pay transparency, wage notices, salary-history rules)
> - Open questions and what's unresolved
> - What could go wrong (misclassification liability, unenforceable non-compete, missing required notice, conflicting at-will language)
> - What to ask the attorney (is this the right form for this jurisdiction; can we use our standard non-compete here; what notices need to go with the letter)
>
> If you need to find an attorney, solicitor, barrister, or other authorised legal professional: contact your professional regulator (state bar in the US, SRA/Bar Standards Board in England & Wales, Law Society in Scotland/NI/Ireland/Canada, Law Society of [state] or Bar Association of [state] in Australia, or your jurisdiction's equivalent) for a referral service. In Australia, the Law Society of NSW, Law Institute of Victoria, Queensland Law Society, Law Society of WA, Law Society of SA, Law Society of Tasmania, ACT Law Society, and Law Society NT each run a Find-a-Lawyer or referral service.

Do not produce a "Clear to send" output past this gate without an explicit yes. A marked-DRAFT flagged for attorney review is fine.

---

## Close with the next-steps decision tree

End with the next-steps decision tree per CLAUDE.md `## Outputs`. Customize the options to what this skill just produced — the five default branches (draft the X, escalate, get more facts, watch and wait, something else) are a starting point, not a lock-in. The tree is the output; the lawyer picks.

## What this skill does not do

- Draft the offer letter — reviews it.
- Make the hire decision — checks the paperwork.
- State restrictive-covenant or exemption rules from memory — every
  jurisdiction-specific call is based on researched, cited sources verified
  for currency.
- Research a new jurisdiction in depth on its own — flags that research is
  needed, and uses `wage-hour-qa` or outside counsel to fill in.
