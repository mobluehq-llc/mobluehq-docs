---
layout: ../../layouts/DocsLayout.astro
title: Enterprise roadmap — Phase 2 handout
description: Scoped enterprise capabilities for procurement conversations. Honest status — planned, not shipped.
---

<div class="callout callout-internal">

**Internal — not listed in public navigation.** Share with design partners and procurement stakeholders to set expectations. This is a **roadmap**, not a commitment or SLA.

</div>

Use this handout when a buyer asks "what's coming?" after the pilot wedge (blueChart evidence packs). Everything below is **scoped and prioritized** — not built unless marked **Shipped**.

---

## Shipped today (pilot wedge)

| Capability | Status | Notes |
| ---------- | ------ | ----- |
| Signed evidence packs (blueChart) | **Shipped** | Human-in-the-loop; no autonomous denials |
| Offline receipt verification | **Shipped** | See [Verification](/concepts/verification) |
| Device-bound licensing + offline grace | **Shipped** | [Licensing](/getting-started/licensing) |
| Async support + public status | **Shipped** | [Support](/getting-started/support), [Status](https://mobluehq-status.pages.dev) |
| Public trust summary | **Shipped** | [Trust center](/trust) |

---

## Phase 2 — enterprise readiness (scoped, not built)

| Initiative | Target | Honest status | Buyer impact |
| ---------- | ------ | ------------- | ------------ |
| **SSO / SAML** | Post-pilot enterprise agreements | **Not built.** Identity will integrate with customer IdP for admin and activation flows. SCIM **under evaluation** | Removes password sprawl for fleet rollouts |
| **SOC 2 Type I** | After auditor engagement | **In progress** — scoping complete; observation window **not started**. See [SOC 2 scoping](/enterprise/soc2-scoping) | Satisfies standard vendor-risk questionnaires |
| **BAA execution** | Before any PHI pilot | **Template in legal review.** Pilots remain **synthetic-data-only** until signed | Required for HIPAA-regulated workloads |
| **Admin console** | Post-SSO | **Not built.** Fleet device list, license revoke, policy flags | IT ops without emailing support for every seat change |
| **Central audit export API** | Post-admin console | **Not built.** Scheduled receipt/metadata export to customer S3/SIEM | Compliance automation |
| **E&O / cyber insurance certificate** | Broker engagement | **Founder-gated** — not available from this documentation run | Often required at contract signature |
| **Penetration test report** | Pre–Type I observation | **Scheduled** — report under NDA after completion | InfoSec sign-off |

---

## Explicitly not on near-term roadmap

| Item | Why |
| ---- | --- |
| Multi-tenant hosted case datastore | Conflicts with on-device / customer-VPC architecture |
| Autonomous coverage decisions | Product philosophy — evidence for humans only |
| 24/7 phone support | Async-first until scale warrants staffing |
| FedRAMP | Not scoped; evaluate only with funded demand |

---

## Suggested conversation framing

1. **Pilot now** on synthetic data — prove workflow and receipt integrity.
2. **Parallel track** procurement on BAA + SOC 2 timeline if PHI is required.
3. **Production agreement** after pilot success, with SSO and admin console as rollout milestones — not blockers for first value.

For questionnaire answers, attach the [Security questionnaire template](/enterprise/security-questionnaire).

For legal terms, use only **counsel-approved** agreements — not the [pilot agreement draft](/enterprise/pilot-agreement).

**Last updated:** June 2026
