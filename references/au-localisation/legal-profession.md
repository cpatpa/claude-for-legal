# Australian Legal Profession Regulation

> [!CAUTION]
> **AI-generated, not verified.** Conduct rules, AI guidance, and trust account requirements change. Verify with the relevant law society, bar association, or designated local regulatory authority before relying on a specific rule. The author of this file is not your designated local regulatory authority.

## Regulatory framework

Australia does not have a single national legal profession statute. The Legal Profession Uniform Law (LPUL) operates in NSW, Victoria, and Western Australia (WA joined 1 July 2022). Other states and territories each have their own Act.

| Jurisdiction | Governing Act | Designated local regulatory authority (DLRA) |
|---|---|---|
| NSW | *Legal Profession Uniform Law (NSW) No 16a* | Law Society of NSW (solicitors), NSW Bar Association (barristers) |
| VIC | *Legal Profession Uniform Law Application Act 2014* (Vic) | Victorian Legal Services Board + Commissioner (VLSB+C), Law Institute of Victoria, Victorian Bar |
| WA | *Legal Profession Uniform Law Application Act 2022* (WA) | Legal Practice Board of WA, Law Society of WA, WA Bar Association |
| QLD | *Legal Profession Act 2007* (Qld) | Queensland Law Society, Bar Association of Queensland, Legal Services Commission |
| SA | *Legal Practitioners Act 1981* (SA) | Law Society of SA, SA Bar Association, Legal Practitioners Conduct Board |
| TAS | *Legal Profession Act 2007* (Tas) | Law Society of Tasmania, Tasmanian Bar |
| ACT | *Legal Profession Act 2006* (ACT) | ACT Law Society, ACT Bar Association |
| NT | *Legal Profession Act 2006* (NT) | Law Society NT, NT Bar Association |

## Solicitors and barristers

The Australian profession is divided in most jurisdictions. Solicitors and barristers are admitted as legal practitioners but practise differently:

- **Solicitors**: Provide legal advice, conduct transactions, instruct barristers. Hold a practising certificate from the solicitors' regulator. May appear in court but in higher courts typically brief a barrister.
- **Barristers**: Specialist advocates and opinion writers. Hold a practising certificate from the bar. In most states, barristers practise as sole practitioners and accept work via the cab-rank rule. Direct access (briefing a barrister without a solicitor) is permitted in limited circumstances.

The fused / split distinction varies:
- **Fused** (in form, though practice often splits anyway): SA, NT.
- **Split** (separate admission practising certificates and roles): NSW, VIC, QLD, WA. Tasmania and ACT have practical separation but a single admission.

## Conduct rules

### Solicitors' Conduct Rules
- **Australian Solicitors' Conduct Rules (ASCR)** adopted in most jurisdictions. Maintained by the Law Council of Australia. Key rules:
  - Rule 4: Other fundamental ethical duties (honesty, integrity, candour, courtesy).
  - Rule 9: Confidentiality.
  - Rule 11: Conflicts (concurrent client interests).
  - Rule 10: Conflicts (former client).
  - Rule 19-25: Duty to the court.
  - Rule 17: Independence.
  - Rule 7: Communication with represented parties.
- Note: Victoria has its own *Legal Profession Uniform Law Australian Solicitors' Conduct Rules 2015* (the Uniform Solicitors' Conduct Rules), substantially aligned with the ASCR but technically a separate instrument.

### Barristers' Conduct Rules
- **Legal Profession Uniform Conduct (Barristers) Rules 2015** in NSW, VIC, WA.
- State equivalents in other jurisdictions (e.g. *Bar Association of Queensland Barristers' Conduct Rules*).
- Includes the cab-rank rule and rules on direct access briefing.

## Continuing professional development

- Annual CPD requirement: 10 units per year in most jurisdictions (some require minimum allocation across categories: ethics, practice management, professional skills, substantive law).
- CPD year typically 1 April to 31 March.
- Logged through the law society or bar.

## Trust accounts and costs

- **Trust accounts**: Strict regulation under the LPUL or state Act. Annual external examination. Designated trust account; controlled money account; transit money. Breaches are serious and frequently disciplinary.
- **Costs disclosure**: Required at engagement. Statutory limits on costs without compliant disclosure. LPUL ss 174-185.
- **Costs agreements**: Generally required to be in writing for amounts above the statutory threshold.
- **Contingency fees (damages-based)**: Generally prohibited, except in Victoria for class actions under Part 4A of the *Supreme Court Act 1986* (Vic) (Group Costs Orders permitted, in force since 2020).
- **Conditional costs agreements (no-win-no-fee)** are permitted with uplift up to 25%.

## AI use guidance

Several state regulators and the Law Council have issued AI-use guidance for the profession. Practitioners must verify the current statement of position with their DLRA. Themes across the guidance as of 2024-2025:

- **Competence and supervision**: A lawyer remains responsible for AI-assisted work and must verify outputs.
- **Confidentiality**: Client information must not be input to AI tools that retain or train on the data without informed client consent and a permitted basis.
- **Privilege**: Disclosure of privileged material to a third-party AI service may waive privilege if the service is not appropriately bound by confidentiality.
- **Candour to the court**: Practitioners must not file AI-hallucinated citations. Multiple Australian courts have issued practice notes or warnings (e.g. Supreme Court of NSW, Federal Court, Supreme Court of Victoria) following well-publicised hallucinated-citation incidents in the US and elsewhere.
- **Costs disclosure**: AI-assisted work that is charged at conventional rates may attract proportionality challenges; some firms have begun disclosing AI use in costs disclosure.
- **Practising certificate conditions**: Some DLRAs are considering conditions requiring training in AI use.

Specific guidance to check against the primary source:

- Law Society of NSW: AI guidance for solicitors (ongoing updates).
- Law Institute of Victoria: Guidelines on the use of generative AI by lawyers.
- Queensland Law Society: AI in legal practice guidance.
- Federal Court of Australia: Practice Note on the use of generative AI in litigation (verify current edition).
- Supreme Court of New South Wales: Practice Note on Use of Generative Artificial Intelligence (SC Gen 23) (verify current edition).

## Admission and reserved areas

- **Admission**: Holder of an accredited law degree + Practical Legal Training (PLT) (e.g. College of Law, ANU Legal Workshop, Leo Cussen) + supervised practice period for solicitors (typically 2 years restricted practising certificate). Barristers complete the Bar Practice Course / Readers Course after admission.
- **Reserved legal work**: Engaging in legal practice without holding a practising certificate is an offence. Reserved areas include drawing or preparing a document for fee or reward affecting legal rights, appearing as advocate before a court (with exceptions for self-represented and McKenzie friend support).
- **In-house counsel**: Hold an in-house or corporate practising certificate (depending on state). May not advise external parties; advice scope is to the corporate employer.

## Implications for AI-assisted legal work in this repository

When skills in this repository are used by an Australian legal practitioner:

1. **The user remains responsible** for the AI output. Skills must surface what is uncertain so the user can verify.
2. **Confidentiality and privilege must be preserved.** Skills must not assume that uploading client documents to a model is permissible without checking the user's firm policy and the client's consent. See `privilege.md`.
3. **Citations from AI must be verified.** Default behaviour: tag AI-generated citations `[verify]` and treat all citations as unverified until checked against a primary source.
4. **Output must not assert "work product" protection** in AU contexts. See `privilege.md` for the correct framing.
5. **The user is the lawyer; the AI is not.** No output is legal advice. The work-product header for AU outputs uses `CONFIDENTIAL. LEGAL ANALYSIS FOR THE USER'S REVIEW. NOT LEGAL ADVICE`, or `PRIVILEGED AND CONFIDENTIAL: PREPARED FOR THE PURPOSE OF OBTAINING LEGAL ADVICE` (if the output is being prepared at the direction of, or for the use of, an Australian legal practitioner). See `privilege.md` for the formulation.
6. **Non-lawyer users** should be reminded that providing legal advice without a practising certificate is an offence. Skills should not output content that purports to be legal advice when used by a non-lawyer.

🤙
