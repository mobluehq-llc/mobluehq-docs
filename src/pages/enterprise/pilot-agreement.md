---
layout: ../../layouts/DocsLayout.astro
title: Pilot agreement (DRAFT)
description: One-page design-partner pilot terms — DRAFT pending attorney review. Do not execute without counsel.
---

<div class="callout callout-draft">

**DRAFT — COUNSEL-GATED**

This document is a **working draft** for internal alignment and procurement conversations. **Do not send for signature, do not rely on these terms in a live pilot, and do not represent them as final** until MOBLUEHQ counsel has reviewed and approved a version for your jurisdiction and use case.

</div>

<div class="callout callout-internal">

**Internal — not listed in public navigation.**

</div>

---

## Pilot services agreement (draft)

**Between:** MOBLUEHQ ("Provider") and **[Customer legal name]** ("Customer")

**Effective date:** **[DATE]**

**Term:** **[90] days** from Effective Date unless terminated earlier. **No auto-renewal.** Any extension requires a new written agreement.

---

### 1. Purpose and scope

Provider will make **blueChart** (or other named MOBLUEHQ product: **[PRODUCT]**) available to Customer for a **limited design-partner / pilot** to evaluate utilization-review evidence workflows. Deliverables are **evidence packs and signed receipts** for human review — not autonomous coverage decisions.

**Out of scope:** production UM adjudication, PHI processing beyond what Section 3 allows, custom SLAs, 24/7 support, or features not shipped in the pilot build.

---

### 2. License grant

Non-exclusive, non-transferable, revocable license to use the pilot software during the Term for internal evaluation only. **No production deployment** without a separate production agreement.

---

### 3. Data and compliance

| Rule | Detail |
| ---- | ------ |
| **Synthetic / de-identified only** | Until a **Business Associate Agreement (BAA)** is fully executed, Customer will **not** load PHI or identifiable patient records into the pilot environment |
| **Customer responsibility** | Customer warrants it has rights to any data entered and will de-identify per its policies |
| **BAA** | If Customer requires HIPAA processing, parties will negotiate a BAA **before** any PHI is permitted. BAA execution is a **Phase 2** milestone — see [Roadmap](/enterprise/roadmap) |
| **DPA** | If required, parties will execute Provider's standard DPA or Customer's reasonable markup, subject to counsel review |

---

### 4. Confidentiality (mutual NDA)

Each party may receive the other's **Confidential Information** during the pilot. The receiving party will: (a) use it only to evaluate the pilot; (b) protect it with reasonable care; (c) disclose only to employees and advisors with a need to know under equivalent obligations. Standard exclusions apply (public domain, independently developed, rightfully received from third parties).

**Term of confidentiality:** three (3) years from disclosure, or longer if trade secret.

---

### 5. Intellectual property

| Item | Owner |
| ---- | ----- |
| Provider software, documentation, and improvements | **MOBLUEHQ** |
| Customer data and exports Customer creates | **Customer** |
| Feedback | Customer grants Provider a perpetual license to use feedback to improve products without attribution or royalty |

No implied license to Provider trademarks beyond identifying the pilot relationship.

---

### 6. Deliverables

Provider delivers:

- Access to the named pilot build
- Async support per [Support expectations](/getting-started/support)
- **Evidence-only outputs** — signed packs Customer exports; not a guarantee of coverage outcome

Customer delivers:

- Timely feedback and bug reports
- Designated technical and clinical contacts
- Compliance with Section 3 data restrictions

---

### 7. Fees

**[Pilot fee: $0 / $X]** as stated on the order. No hidden usage fees during the Term unless separately agreed in writing.

---

### 8. Warranty disclaimer

Pilot software is provided **"AS IS"** for evaluation. Provider disclaims all warranties, express or implied, including merchantability and fitness for a particular purpose.

---

### 9. Limitation of liability

**Cap:** Each party's aggregate liability arising from this agreement is limited to **fees paid in the twelve (12) months** preceding the claim (or **$[AMOUNT]** if no fees were paid).

**Exclusion:** Neither party is liable for indirect, incidental, special, consequential, or punitive damages, or lost profits.

**Carve-outs (typical counsel markup):** cap and exclusion may not apply to gross negligence, willful misconduct, or breach of confidentiality — **subject to attorney review**.

**Zero-to-zero option:** For no-fee pilots, parties may agree **mutual zero liability** except for confidentiality breaches and indemnity for third-party IP claims — **counsel must confirm enforceability**.

---

### 10. Termination

Either party may terminate on **fifteen (15) days'** written notice, or immediately for material breach uncured after **ten (10) days'** notice.

On termination: Customer ceases use, deletes pilot installs per Provider instructions, and certifies deletion on request. Sections on confidentiality, IP, liability, and governing law survive.

---

### 11. Security

Customer will follow Provider's reasonable security guidance. Provider will maintain controls described in the [Security questionnaire template](/enterprise/security-questionnaire) as of the Effective Date. **SOC 2 report** is not yet available; status on [Trust center](/trust).

---

### 12. Governing law

**[State — e.g., Delaware / Wisconsin]** without regard to conflicts principles. Exclusive venue: **[county/state]** unless counsel prefers arbitration.

---

### 13. Entire agreement

This agreement supersedes prior pilot discussions on the same subject. Amendments must be in writing signed by both parties.

---

## Before you use this draft

| Step | Owner |
| ---- | ----- |
| Attorney review of all bracketed fields | MOBLUEHQ counsel + Customer counsel |
| Confirm synthetic-data-only until BAA | Customer compliance |
| Confirm insurance / SOC 2 expectations | Customer procurement (see [SOC 2 scoping](/enterprise/soc2-scoping)) |
| Execute only on approved paper | Both parties |

**Do not substitute this web page for a signed PDF or DocuSign envelope.**
