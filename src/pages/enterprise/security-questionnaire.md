---
layout: ../../layouts/DocsLayout.astro
title: Security questionnaire — answer template
description: Pre-written answers for standard vendor security questionnaires. Internal use during procurement.
---

<div class="callout callout-internal">

**Internal — not listed in public navigation.** Share with prospects during active procurement conversations. Update this page when controls change; date your export.

</div>

Use this template to respond to common InfoSec and vendor-risk questionnaires. Answers reflect **shipped or in-flight** controls as of publication. Where a control is planned but not complete, the answer says so.

For a public-facing summary, point buyers to the [Trust center](/trust).

---

## Company and scope

| Question | Answer |
| -------- | ------ |
| Legal entity | MOBLUEHQ (single-founder LLC; legal name on order form) |
| Primary products in scope | blueChart, blueForge, blueCheck SDK, and related MOBLUEHQ surfaces under your agreement |
| Data classification handled | Customer-configured; pilot agreements restrict to **synthetic or de-identified** data until a BAA is executed |
| Hosting model | Customer-controlled execution (on-device, customer VPC, or agreed private demo environment). MOBLUEHQ does not operate a multi-tenant SaaS datastore of customer case content |

---

## Data handling

| Question | Answer |
| -------- | ------ |
| What customer data does MOBLUEHQ process? | **License metadata** (license ID, device ID, edition) on periodic activation checks. **Support artifacts** you submit via Report. **No routine upload** of prompts, disclosures, or clinical content to MOBLUEHQ-operated storage in standard editions |
| Where does processing occur? | On the customer device, in the customer VPC (SDK editions), or in a dedicated demo environment named in your agreement |
| Does MOBLUEHQ sell or train on customer content? | **No.** Customer prompts and case facts are not used to train MOBLUEHQ models or resold as a data product |
| Subprocessors | See [Subprocessors](/trust#subprocessors) on the public trust page. Model providers (Anthropic, OpenAI, etc.) are invoked **with your keys** under your vendor agreements when you enable cloud models |
| Cross-border transfer | Depends on your deployment and provider choices. MOBLUEHQ License Authority endpoints are US-based unless your contract specifies otherwise |

---

## Encryption

| Question | Answer |
| -------- | ------ |
| Encryption in transit | TLS 1.2+ for all MOBLUEHQ-operated endpoints (License Authority, status, docs). Customer-to-model-provider traffic uses each vendor's TLS stack |
| Encryption at rest | Customer-controlled disks and VPC storage for case data and exports. MOBLUEHQ-operated systems encrypt provider-managed storage at rest (Cloudflare, GitHub) per those providers' defaults |
| Key management | Signing keys for receipts are generated and held per instance or per customer deployment. MOBLUEHQ does not hold customer content encryption keys for on-prem editions |

---

## Access control

| Question | Answer |
| -------- | ------ |
| Production access | Restricted to founder/engineering principals. No broad contractor access to customer environments |
| Authentication | MOBLUEHQ internal systems use MFA on identity providers. Customer apps use local OS session + product activation; **SSO/SAML is scoped for Phase 2** (see [Enterprise roadmap](/enterprise/roadmap)) |
| Least privilege | Role separation between code, deploy, and support. Customer VPC deployments use your IAM |
| Customer admin console | **Not shipped** in pilot builds; roadmap item |

---

## Audit logging

| Question | Answer |
| -------- | ------ |
| Application audit trail | Products emit **signed receipts** per verification run: inputs fingerprint or redacted summary, outputs or hashes, lanes/models, timestamps, and cryptographic signature |
| Tamper evidence | Receipt chains and internal ops logs use **hash-chained** entries where the product edition supports it; verify offline per [Verification](/concepts/verification) |
| Central SIEM integration | Customer exports receipts to your SIEM. MOBLUEHQ does not ingest customer SIEM streams in standard editions |
| Log retention (MOBLUEHQ ops) | Support tickets and deploy logs retained per internal policy (typically 12 months unless legal hold) |

---

## Vulnerability management and SDLC

| Question | Answer |
| -------- | ------ |
| Secure SDLC | Changes via GitHub PR review; production deploys from tagged releases. No direct-to-prod commits |
| Dependency scanning | `npm audit` / Dependabot on MOBLUEHQ repositories; critical findings triaged before release when feasible |
| SAST/DAST | Linting and type-check in CI; full third-party pen test **not yet completed** — scheduled before SOC 2 Type I observation window |
| Vulnerability disclosure | See [Responsible disclosure](/trust#vulnerability-disclosure) |

---

## Incident response

| Question | Answer |
| -------- | ------ |
| Security contact | security@mobluehq.com |
| Notification timeline | Material incidents affecting MOBLUEHQ-operated services: notice on [status page](https://mobluehq-status.pages.dev) and direct notice to affected customers per agreement |
| IR playbook | Documented runbook (contain → assess → notify → remediate). Tabletop exercise **in progress** as part of SOC 2 prep |
| Customer data breach | Unlikely in standard architecture (no central case datastore). If License Authority or support systems are implicated, we notify per contract and applicable law |

---

## Data retention and deletion

| Question | Answer |
| -------- | ------ |
| Customer case content | Retained **only on customer systems** unless you explicitly export or submit via support |
| License records | Retained for subscription term + reasonable business period for billing disputes |
| Support tickets | Deleted or anonymized on request after ticket closure, subject to legal hold |
| Pilot termination | Per pilot agreement: customer deletes local installs and exports; MOBLUEHQ deletes pilot-specific config within 30 days of written request |

---

## Business continuity and disaster recovery

| Question | Answer |
| -------- | ------ |
| RTO / RPO (MOBLUEHQ services) | License Authority and status: target **24h RTO**, **24h RPO** on managed infra (not yet contractually guaranteed — improving with SOC 2) |
| Customer workloads | On-device and VPC editions continue offline within license grace; see [Licensing](/getting-started/licensing) |
| Backups | Infrastructure config in Git; customer data backup is **customer responsibility** |
| Geographic redundancy | Single-region today for MOBLUEHQ-operated endpoints; multi-region **evaluated for Phase 2** |

---

## Compliance posture

| Question | Answer |
| -------- | ------ |
| SOC 2 | **In progress.** Scoping and gap analysis: [SOC 2 scoping checklist](/enterprise/soc2-scoping). Type I target after auditor engagement (founder-gated) |
| HIPAA / BAA | **Not executed by default.** Pilots use synthetic data only until BAA is signed |
| GDPR | Data processing terms available on request; subprocessors listed publicly |
| PCI | Not in scope — MOBLUEHQ does not process payment cards in product surfaces |

---

## Insurance and organizational risk

| Question | Answer |
| -------- | ------ |
| E&O / cyber liability | **Founder-gated** — engagement with broker in progress; certificate available when bound |
| Bus factor | Single-founder company; escrow or source-access terms negotiable in enterprise agreements |
| Penetration test report | Available under NDA after scheduled assessment |

---

## How to use this document

1. Copy relevant sections into your buyer's questionnaire format.
2. Attach [Offline and privacy](/concepts/offline-and-privacy) and the [Trust center](/trust) for public references.
3. For legal terms, use counsel-reviewed agreements only — the [pilot agreement draft](/enterprise/pilot-agreement) is **not** approved for execution.

**Last updated:** June 2026
