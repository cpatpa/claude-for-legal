# Legal Professional Privilege in Australia

> [!CAUTION]
> **AI-generated overview, not verified.** This is a sketch of complex doctrine. Privilege determinations turn on facts. Always check a specific privilege question against current case law and the relevant Evidence Act.

## Why this matters for the repository

The original US-default plugins apply the "ATTORNEY WORK PRODUCT" header and rely on US work product doctrine (FRCP 26(b)(3)) to protect AI-generated analyses. **That doctrine does not exist in Australia.** Applying the header in an Australian context creates a false sense of protection: a regulator with compulsory powers, or an opponent in litigation, can compel production of a document marked "ATTORNEY WORK PRODUCT" if it does not in fact attract Australian legal professional privilege.

## Australian legal professional privilege: structure

Two limbs (often referred to as a single privilege with two heads):

### 1. Legal advice privilege
Confidential communications between a client and a lawyer, made for the **dominant purpose of giving or obtaining legal advice**.

Key features:
- The lawyer must be a qualified legal practitioner. In-house counsel attract advice privilege provided they are sufficiently independent of management and the advice is given in a professional capacity, not as a business participant.
- The communication must be **confidential** at creation.
- The **dominant purpose** test is strict (since *Esso Australia Resources Ltd v Commissioner of Taxation* (1999) 201 CLR 49, replacing the earlier "sole purpose" test). Dominant purpose is determined objectively; ascertaining the dominant purpose involves identifying the purpose of the person responsible for creating or commissioning the document.

### 2. Litigation privilege
Confidential communications made for the **dominant purpose** of use in existing or reasonably anticipated litigation. Covers communications with third parties (witnesses, experts) made for that purpose.

Key features:
- Litigation must be in reasonable prospect (more than a mere possibility).
- The dominant purpose must be litigation use.
- Documents created in the ordinary course of business and only secondarily for possible litigation generally do not attract privilege.

## What is NOT protected (that often surprises US lawyers)

- **Internal analyses for business decisions** (compliance assessments, launch reviews, product reviews, governance memos) are not privileged just because a lawyer was involved. They must be made for the dominant purpose of obtaining or giving legal advice.
- **Investigation reports** are particularly vulnerable. Unless the dominant purpose at the time of creation was legal advice, regulators (ASIC, ACCC, OAIC, AHRC) can compel production even where lawyers conducted the investigation. The case law (e.g. *AWB Ltd v Cole (No 5)* (2006) 155 FCR 30) is unsympathetic to retrospective claims that an investigation was "really" for legal advice.
- **AI prompts and AI outputs**: novel area. The communication of confidential client information to an AI provider may be a disclosure that waives privilege depending on the terms with the provider. Even where no waiver, the dominant purpose at the time of using the AI must be advice or anticipated litigation, not (e.g.) internal training or QA.
- **Drafts of advice prepared in a "deliberative" process**: contrast with Public Interest Immunity (PII) which protects Crown deliberative material. PII is not the same as LPP.
- **Communications with non-legal advisers** (accountants, consultants, PR firms) attract no privilege under LPP, regardless of confidentiality.

## Waiver

Waiver in Australia is largely governed by *Mann v Carnell* (1999) 201 CLR 1: waiver occurs where the conduct of the privilege holder is inconsistent with the maintenance of confidentiality the privilege is intended to protect. Inadvertent disclosure may not waive but consider the inconsistency analysis carefully.

Issue / implied waiver: where a party puts privileged material in issue (e.g. by relying on legal advice as a defence), they may be taken to have waived.

## Regulator compulsion

A document protected by LPP cannot generally be compelled by a regulator using statutory powers. But:

- **ATO and tax**: ATO does not generally seek LPP material, and there is established practice around "accountants' concession" for documents prepared by tax advisers (not statutory privilege, an administrative arrangement).
- **ASIC s 33 / s 19 ASIC Act**: Cannot compel privileged material. Disputes over claims of privilege are common.
- **ACCC s 155 Competition and Consumer Act**: Cannot compel privileged material.
- **OAIC powers**: Cannot compel privileged material.
- **Royal Commissions and equivalent**: Statutory abrogation possible. The *Royal Commissions Act 1902* (Cth) does not abrogate LPP unless expressly stated, but specific Royal Commission Letters Patent may include abrogation. Check the terms.

## Practical implications for AI-assisted work

### Document headers

Replace US "PRIVILEGED & CONFIDENTIAL — ATTORNEY WORK PRODUCT — PREPARED AT THE DIRECTION OF COUNSEL" with one of:

- **For documents created at the direction of, and for the dominant purpose of obtaining advice from, an Australian legal practitioner**:
  `PRIVILEGED AND CONFIDENTIAL: PREPARED AT THE REQUEST OF [AU LEGAL PRACTITIONER] FOR THE DOMINANT PURPOSE OF OBTAINING LEGAL ADVICE`

- **For documents created for the dominant purpose of use in existing or reasonably anticipated litigation**:
  `PRIVILEGED AND CONFIDENTIAL: PREPARED FOR THE DOMINANT PURPOSE OF [EXISTING / ANTICIPATED] LITIGATION`

- **For documents that are not actually privileged (most internal AI analyses)**:
  `CONFIDENTIAL. INTERNAL ANALYSIS. NOT LEGAL ADVICE` (and resist any temptation to assert privilege the document does not in fact attract; a false claim is worse than no claim)

- **For non-lawyer users**:
  `RESEARCH NOTES. NOT LEGAL ADVICE. REVIEW WITH AN AUSTRALIAN LEGAL PRACTITIONER BEFORE ACTING`

### Confidentiality of AI provider

- Confirm the contractual basis on which the AI provider is engaged. Standard consumer terms (training on inputs, no confidentiality of prompts) are likely incompatible with maintaining privilege over client information.
- Enterprise terms (no training, contractual confidentiality, data processing terms) reduce risk. Verify with firm policy.
- Where in doubt, do not input client-identifying information. Redact or use placeholders.

### Investigation work

- Establish dominant purpose **before** beginning the investigation. Engage external counsel to direct the investigation. Document the engagement and purpose.
- Have legal practitioners (in-house counsel with the requisite independence, or external) instruct the AI-assisted work as part of the legal advice workflow.
- Recognise that retrospective claims of privilege rarely succeed where the contemporaneous records show a business purpose.

### Where the user is a non-lawyer

- Outputs labelled with privilege headers are misleading. The privilege requires the involvement of a legal practitioner.
- Default for non-lawyer users in AU practice profiles: no privilege header; explicit "not legal advice" framing.

## Comparative table

| Concept | US (FRCP 26 / common law) | Australia |
|---|---|---|
| Attorney-client privilege | Communications with attorney for legal advice; broader scope in many respects | Legal advice privilege; dominant purpose test |
| Work product doctrine | Materials prepared in anticipation of litigation, ordinary and opinion work product; not requiring dominant purpose | Litigation privilege; requires dominant purpose; **no separate work product doctrine** |
| In-house counsel | Generally privileged | Privileged where counsel is sufficiently independent and acting in legal capacity |
| Common interest | Recognised | Recognised, often described as narrower |
| Joint defence | Recognised | Recognised through common interest doctrine |
| Crime-fraud exception | Recognised | Recognised (improper purpose exception) |
| Waiver | Express, implied, at-issue | *Mann v Carnell* inconsistency test |

## Final practical reminder

Tagging a document with privilege language does not make it privileged. Australian courts and regulators look at the substantive question: what was the document for, who created it, when, and was the dominant purpose advice or litigation. The AI cannot answer that for the user. Skills should surface the question so the reviewing lawyer can answer it.

🤙
