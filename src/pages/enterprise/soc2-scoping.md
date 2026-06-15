---
layout: ../../layouts/DocsLayout.astro
title: SOC 2 Type I — scoping checklist
description: Controls in place vs gaps, and steps to engage an auditor. Founder-gated engagement.
---

<div class="callout callout-internal">

**Internal — not listed in public navigation.** For founder and advisor use when engaging a SOC 2 auditor. **No documentation run can substitute for an audit engagement or issue a SOC 2 report.**

</div>

This checklist maps MOBLUEHQ's **current control posture** against a typical SOC 2 Type I (Security trust services criteria) readiness review. Use it to enter an auditor conversation with eyes open on gaps, cost, and timeline.

Public status: [Trust center](/trust) · Questionnaire template: [Security questionnaire](/enterprise/security-questionnaire)

---

## Engagement prerequisites (founder-gated)

| Prerequisite | Status | Notes |
| ------------ | ------ | ----- |
| Auditor selected (AICPA firm) | **Not engaged** | Budget $15k–$40k for Type I readiness + report depending on scope and firm |
| Trust services criteria | **Security (common criteria)** | Availability and confidentiality add-ons optional for Type I |
| System description boundary | **Draft** | License Authority, status page, docs site, support ticketing — **not** customer on-prem installs |
| E&O / cyber insurance | **In progress** | Often requested alongside SOC 2; separate broker engagement |
| Penetration test | **Scheduled** | Usually required before or during observation window |

---

## Control matrix — in place vs gap

| Control area | In place today | Gap / remediation |
| ------------ | -------------- | ----------------- |
| **Access management** | MFA on GitHub, Cloudflare, email; no shared root passwords | Formal access review log; offboarding checklist documented |
| **Encryption** | TLS on all MOBLUEHQ endpoints; provider at-rest encryption | Document customer-side encryption responsibility in system description |
| **Change management** | PR-based deploys; tagged releases | Written change policy; emergency change procedure |
| **Vulnerability management** | Dependabot / npm audit in CI | SLA for critical CVEs; annual third-party pen test |
| **Logging & monitoring** | Cloudflare analytics; GitHub audit log | Centralized log retention policy; alerting runbooks |
| **Incident response** | Status page process; security@ contact | Formal IR plan + tabletop exercise with dated minutes |
| **Vendor management** | Subprocessor list public | Annual vendor review cadence documented |
| **BCP/DR** | Git-backed infra; manual restore tested informally | Written BCP/DR plan with RTO/RPO targets |
| **SDLC** | Code review, CI build | Secure coding training record; branch protection evidence export |
| **Background checks** | Founder-only today | Policy scales when hires join |
| **Physical security** | N/A — no MOBLUEHQ datacenter | Rely on Cloudflare / SaaS provider SOC reports |
| **Risk assessment** | Informal | Annual risk assessment document for auditor file |
| **Policies** | Scattered in docs | Policy pack: InfoSec, Acceptable Use, Data Retention, IR |

---

## Hash-chained audit logging (product)

| Layer | Status |
| ----- | ------ |
| Receipt signatures per run | **Shipped** in product editions |
| Hash-chained receipt / ops logs | **Shipped or shipping** per edition — document exact edition in system description |
| MOBLUEHQ central SIEM of customer receipts | **Out of scope** — customer exports |

Auditors will distinguish **MOBLUEHQ corporate systems** from **customer-deployed software**. The system description should draw that boundary clearly.

---

## Recommended steps to Type I

| Step | Owner | Est. effort |
| ---- | ----- | ----------- |
| 1. Freeze system description boundary | Founder + advisor | 1–2 days |
| 2. Select auditor; sign engagement letter | Founder (budget approval) | 1–2 weeks |
| 3. Gap remediation from matrix above | Engineering | 2–6 weeks |
| 4. Policy pack draft + approval | Founder + counsel | 1–2 weeks |
| 5. Penetration test | Third party | 1–2 weeks + remediation |
| 6. Observation window (if required by firm) | Operations | 2–4 weeks typical for Type I |
| 7. Auditor report issuance | Auditor | 2–4 weeks after fieldwork |

**Total calendar time (typical):** 8–16 weeks from engagement, assuming no critical pen-test findings.

---

## Cost ranges (planning only — not quotes)

| Item | Range (USD) |
| ---- | ----------- |
| SOC 2 Type I audit (Security only) | $15,000 – $35,000 |
| Readiness / virtual CISO advisor | $5,000 – $15,000 |
| Penetration test | $5,000 – $15,000 |
| GRC tooling (optional) | $3,000 – $12,000 / year |
| Policy templates + counsel review | $2,000 – $8,000 |

Add **Availability** or **Confidentiality** criteria: typically +30–50% on audit fees.

---

## What this run does **not** produce

- SOC 2 Type I or Type II report
- Auditor management letter
- E&O or cyber insurance certificate
- Signed BAA or DPA

Those require **founder-initiated** engagements with auditors, brokers, and counsel.

---

## After Type I

| Next | Purpose |
| ---- | ------- |
| Type II observation (6–12 months) | Prove controls operated effectively over time |
| Continuous monitoring | Vanta / Drata / similar — evaluate at hire scale |
| Customer-facing trust pack | SOC report under NDA + updated [Trust center](/trust) |

**Last updated:** June 2026
