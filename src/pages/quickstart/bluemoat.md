---
layout: ../../layouts/DocsLayout.astro
title: blueMoat quickstart
description: Prior-art screening with quoted sources, a second opinion, and a tamper-evident receipt.
---

**blueMoat** screens prior art for a disclosure you paste in. Each finding should carry a **validated source quote**, an **independent second opinion**, and a **tamper-evident receipt** you can keep for diligence files.

The customer app is **bluemoat-app** (desktop or web build — your onboarding email names the channel).

## Install

1. Download **bluemoat-app** from the link in your MOBLUEHQ onboarding email, or clone the repo if your agreement is source-based.
2. Install dependencies only if you are on a developer build (`npm install` then `npm run dev` or the command in the repo README).
3. Launch the app and **activate this device** when asked. Your license allows a fixed number of machines; see [Activation and licensing](/getting-started/licensing).

## First run

1. Open **New screening** (or equivalent).
2. Paste a short disclosure or claim text — start with a paragraph, not a full application, to learn the UI.
3. Submit and wait for the run to finish. blueMoat judges on the [Blue](/quickstart/blue) substrate; large inputs take longer.
4. Review the landscape view: each row should show a source quote and confidence or dissent markers where enabled.

## Where results and receipts appear

| Output                   | Location                                                                 |
| ------------------------ | ------------------------------------------------------------------------ |
| Screening report         | In-app results table or landscape view                                   |
| Source quotes            | Per-finding detail drawer                                                |
| Second opinion / dissent | Tagged on findings where council disagreed                               |
| Signed receipt           | **Export receipt** or **Evidence** menu — JSON or PDF depending on build |

Export the receipt before you close the session if your policy requires a permanent record. For export options in other products, see [Export receipts](/how-to/export-receipts).

## If something fails

- **Stuck run** — Check [MOBLUEHQ status](https://mobluehq-status.pages.dev); dispatch issues may affect backend lanes.
- **License error** — [Activation and licensing](/getting-started/licensing)
- **Missing quotes** — Note the finding ID and use in-app **Report**; see [Support](/getting-started/support)

## Next

- [Verify receipts](/how-to/verify-receipts)
- [Beta and known issues](/getting-started/beta-known-issues)
