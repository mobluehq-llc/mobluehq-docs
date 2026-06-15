---
layout: ../../layouts/DocsLayout.astro
title: Support and response expectations
description: Async support, the 48–72 hour window, and how to file bugs from inside a product.
---

MOBLUEHQ support is **async-first**. We read every report; we do not staff a 24/7 chat desk during early customer onboarding.

## Response window

| Channel                        | Expectation                                                                               |
| ------------------------------ | ----------------------------------------------------------------------------------------- |
| In-product **Report**          | First human reply within **48–72 hours** on business days (US Central bias)               |
| License or activation blockers | Same window; mark **urgent — cannot activate** in the subject or description              |
| Security issues                | Use the security contact in your onboarding packet — do not paste exploits in public bugs |

Weekends and US holidays may extend the window. Critical outages appear on the [status page](https://mobluehq-status.pages.dev) without waiting for individual replies.

## How to file from inside a product

Most MOBLUEHQ shells include **Report** in the menu or command palette.

1. Reproduce or note the last step before the failure.
2. Open **Report** (wording may be **Send feedback** in some builds).
3. Describe expected vs actual behavior in plain language.
4. Attach logs when the form offers them — they stay with the ticket, not in public docs.
5. Copy the **reference ID** if shown; include it in any follow-up email.

Step-by-step for forge: [Report bugs](/how-to/report-bugs).

### What to include

- Product name and build version (About box)
- OS and hardware class if performance-related
- Receipt export or last successful step for dispatch issues
- Whether you are on offline grace ([licensing](/getting-started/licensing))

### What not to include

- API keys, license keys, or patient/PII
- Full disclosure text unless your agreement explicitly allows it in tickets

## What happens after you file

1. Ticket enters the MOBLUEHQ bug registry (customer-visible IDs may appear on the status page when triaged).
2. Engineering reproduces using your logs and receipts when possible.
3. You receive email or in-app notice on status changes — not every intermediate commit.

Network triage with signed submit ("Filed as Bug #N") rolls out per product; until then, email confirmation is the source of truth.

## Self-serve before waiting

| Topic                 | Doc                                                         |
| --------------------- | ----------------------------------------------------------- |
| Install and first run | [Quickstart](/quickstart)                                   |
| License errors        | [Activation and licensing](/getting-started/licensing)      |
| Live incidents        | [Status page](https://mobluehq-status.pages.dev)            |
| Known beta limits     | [Beta and known issues](/getting-started/beta-known-issues) |
| Privacy questions     | [Offline and privacy](/concepts/offline-and-privacy)        |

## Sales, billing, and seat changes

Licensing and seat count changes go through the same contact as onboarding — not the Report form. Reference your account email and company name.

## Next

- [Report bugs](/how-to/report-bugs)
- [Beta and known issues](/getting-started/beta-known-issues)
