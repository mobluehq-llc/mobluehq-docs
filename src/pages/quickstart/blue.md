---
layout: ../../layouts/DocsLayout.astro
title: Blue quickstart
description: The verification substrate every MOBLUEHQ product runs on.
---

**Blue** is the private inference mesh underneath the MOBLUEHQ portfolio. Product apps (blueMoat, blueChart, blueGlu, and others) call into Blue for model work. The scheduler routes jobs; your prompts and documents are not stored on MOBLUEHQ servers as part of normal operation. Every answer that matters ships with a **signed receipt** you can verify offline.

You usually do not install Blue by itself. You install a product app that rides Blue. This page orients you when onboarding mentions "the substrate" or "the mesh."

## What you get

- Sealed, signed results attached to each run
- Council-style checks where products enable them (independent models, judge separated from doer)
- A consistent receipt format across products — see [Offline and privacy](/concepts/offline-and-privacy)

## Install

1. Use the installer or access link from your MOBLUEHQ onboarding email for the **product** you bought (for example blueMoat or blueChart).
2. On first launch, complete **Activate this device** when prompted. That ties your license to this machine. See [Activation and licensing](/getting-started/licensing).
3. If you are a developer using **blueForge** (the desktop forge), follow [Install blueForge](/getting-started/install) instead — forge is the local dev shell that also produces receipts.

## First run

1. Open your product app and confirm the status strip shows **licensed** or **offline grace** (wording varies by build).
2. Run the smallest task the product offers (one screening, one evidence pack, one chat turn).
3. Open the **receipt** or **evidence** panel for that run. You should see timing, model or lane labels, and a signature block or export action.

If the run fails, check [Beta and known issues](/getting-started/beta-known-issues) and the [status page](https://mobluehq-status.pages.dev).

## Where results appear

| What                   | Where to look                                                                                                         |
| ---------------------- | --------------------------------------------------------------------------------------------------------------------- |
| Human-readable summary | Main product UI (report view, chat panel, pack viewer)                                                                |
| Signed receipt         | Receipt panel, export JSON, or "Download evidence" depending on product                                               |
| Verification           | [Verify receipts](/how-to/verify-receipts) for hash and field checks; full cryptographic verify flows vary by edition |

## Next

- [blueMoat quickstart](/quickstart/bluemoat) if you screen prior art
- [Offline and privacy](/concepts/offline-and-privacy) for the data-leaves-the-device map
- [slumberNet](/concepts/slumbernet) if your edition participates in the volunteer mesh
