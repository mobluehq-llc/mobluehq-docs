---
layout: ../../layouts/DocsLayout.astro
title: blueGlu quickstart
description: On-device Blue chat with citations, mesh access online, and visible uncertainty.
---

**blueGlu** is the MOBLUEHQ chat surface for general use: works **offline on your device**, uses the **Blue mesh** when online, shows **where each answer came from**, and surfaces **uncertainty and disagreement** instead of guessing.

Status today: **demo available** by request — not a public store listing yet.

## Install

1. Request demo access through your MOBLUEHQ contact if you do not already have a build.
2. Install the blueGlu app for your platform (macOS or Linux in current demos; Windows follows the same shell pattern where available).
3. **Activate this device** on first launch. See [Activation and licensing](/getting-started/licensing).

## First run

1. Open blueGlu and confirm the header shows **Offline**, **Online**, or **Mesh** mode.
2. In **offline** mode, ask a factual question you can check locally. Answers run on-device; citations point to bundled or local sources.
3. Switch to **online** or **mesh** when licensed and ask the same question. Compare citations — mesh mode may show which lane contributed.
4. If models disagree, blueGlu should show a **disagreement** or **low confidence** strip rather than blending silently.

## Where results and receipts appear

| Output              | Location                                              |
| ------------------- | ----------------------------------------------------- |
| Chat answer         | Main panel                                            |
| Citations / sources | Inline chips or side panel per turn                   |
| Disagreement        | Banner or council block on that turn                  |
| Receipt             | **Receipt** icon on the turn — export JSON for audits |

Receipt export matches other Blue products; see [Export receipts](/how-to/export-receipts).

## Shipped limitations

- Demo distribution only — no self-serve download on this docs site yet
- Model catalog depends on your demo build
- Full mesh participation may require separate [slumberNet](/quickstart/slumbernet) opt-in — **coming** in unified settings

## Next

- [Blue quickstart](/quickstart/blue) for substrate context
- [Beta and known issues](/getting-started/beta-known-issues)
- [Support](/getting-started/support)
