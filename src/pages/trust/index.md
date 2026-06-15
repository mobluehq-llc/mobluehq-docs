---
layout: ../../layouts/DocsLayout.astro
title: Trust center
description: Security contact, vulnerability disclosure, subprocessors, and data-handling summary for MOBLUEHQ products.
---

MOBLUEHQ builds verification software for regulated workflows. This page is the **public** trust summary for procurement and InfoSec reviewers. Deep legal artifacts (pilot agreements, questionnaire exports) are shared during active sales conversations — not published here.

## System status

Live service health and customer-visible incidents:

**[MOBLUEHQ status page →](https://mobluehq-status.pages.dev)**

For beta expectations and known limits, see [Beta and known issues](/getting-started/beta-known-issues).

---

## Security contact

| Channel | Detail |
| ------- | ------ |
| **Email** | [security@mobluehq.com](mailto:security@mobluehq.com) |
| **Scope** | Vulnerabilities in MOBLUEHQ-operated services, product security questions, coordinated disclosure |
| **Response** | Acknowledgment within **5 business days**; critical issues prioritized |

**Do not** paste exploits, PHI, or live credentials in public bug reports. Use the security contact or in-product **Report** with redacted logs. See [Report bugs](/how-to/report-bugs).

---

## Vulnerability disclosure {#vulnerability-disclosure}

We support **coordinated disclosure**:

1. Report to [security@mobluehq.com](mailto:security@mobluehq.com) with reproduction steps and impact assessment.
2. Allow reasonable time to remediate before public disclosure (typically **90 days**, shorter for active exploitation).
3. We will confirm receipt, keep you informed of status, and credit researchers in release notes when desired.

We do not pursue legal action against good-faith research that respects customer data and avoids service disruption.

---

## Subprocessors {#subprocessors}

MOBLUEHQ uses the following categories of subprocessors to operate **our** infrastructure (not your model inference, which uses **your** provider keys):

| Subprocessor | Purpose | Location |
| ------------ | ------- | -------- |
| **Cloudflare** | Docs hosting, CDN, Pages deploy | US / global edge |
| **GitHub** | Source control, CI artifacts | US |
| **Email provider** (transactional) | Support and onboarding email | US |

**Model providers** (Anthropic, OpenAI, Google, others) are invoked **directly by your deployment** with credentials you configure. They are your subprocessors under your agreements when you enable cloud models. MOBLUEHQ does not route prompts through a shared multi-tenant inference pool in standard editions.

For a DPA or updated subprocessor notification, contact your MOBLUEHQ onboarding channel.

---

## Data handling summary

| Topic | Summary |
| ----- | ------- |
| **Architecture** | Customer content runs on-device, in your VPC, or in a dedicated demo environment — not in a MOBLUEHQ multi-tenant case database |
| **What we may see** | License checks (license ID, device ID, edition), support tickets you submit, aggregated status — not routine access to case content |
| **Receipts** | Cryptographically signed records of verification runs; you control export and retention |
| **Training** | We do not train on customer prompts or clinical content |
| **HIPAA** | BAA required before PHI; pilots use synthetic or de-identified data only until BAA is executed |
| **SOC 2** | Type I **in progress** — not yet available for distribution |

Full detail: [Offline and privacy](/concepts/offline-and-privacy) · [Licensing](/getting-started/licensing) · [Verification](/concepts/verification)

---

## Compliance artifacts

| Artifact | Availability |
| -------- | ------------ |
| Public trust summary | This page |
| Security questionnaire answers | On request during procurement |
| SOC 2 report | **Not yet issued** — notify list via security contact |
| BAA / DPA | Counsel-reviewed versions on request |
| Penetration test summary | Under NDA after completion |

---

## Related

- [Offline and privacy](/concepts/offline-and-privacy)
- [Support](/getting-started/support)
- [System status](https://mobluehq-status.pages.dev)
