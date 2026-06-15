---
layout: ../../layouts/DocsLayout.astro
title: Offline and privacy
description: What runs on your device, what may leave it, and how signed receipts work.
---

MOBLUEHQ products are built for regulated and sensitive work. This page states the **shipped** privacy model in plain language. Product-specific nuance appears in each [quickstart](/quickstart).

## What runs on your device

| Stays local            | Examples                                                                            |
| ---------------------- | ----------------------------------------------------------------------------------- |
| Your files and prompts | Disclosure text, chart facts, chat messages — processed in the app or local runtime |
| API keys you configure | Provider keys in blueForge Settings never pass through MOBLUEHQ                     |
| License blob           | Signed grace metadata after activation                                              |
| Receipt generation     | Structured record of each run, signed on device or in your VPC for SDK editions     |
| Offline inference      | blueGlu offline mode; degraded mesh when disconnected                               |

## What may leave your device

| May leave               | When                                   | What exactly                                                                                                                                                |
| ----------------------- | -------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------- |
| License Authority check | ~Every 30 days or on activate          | License ID, device ID, edition — not case content. See [Activation and licensing](/getting-started/licensing)                                               |
| Model provider calls    | When you use cloud models              | Prompts to **your** vendor (Anthropic, OpenAI, etc.) under their terms — MOBLUEHQ does not substitute as the model host unless your contract says otherwise |
| Mesh job payloads       | slumberNet or mesh-enabled products    | Verified job packages — not your personal document library                                                                                                  |
| Bug reports             | When you click **Report**              | Logs and description you submit — scrub secrets first                                                                                                       |
| Signed exports you send | When **you** email or upload a receipt | Entirely your choice                                                                                                                                        |

MOBLUEHQ does **not** sell a background feed of customer prompts. If a feature would upload content, the UI labels it (for example "cloud screening") in shipped builds.

## What is a signed receipt?

A **receipt** is a structured record of one verification run:

- Inputs fingerprint or redacted summary (edition-dependent)
- Outputs or hashes
- Lanes, models, or tools involved
- Timestamps
- A **cryptographic signature** from the signing key for that run or instance

Receipts let a third party answer: **did this output come from this run at this time?** without trusting a screenshot.

## How to verify a receipt

1. Export receipt JSON from the product (receipt panel, export menu, or SDK field).
2. Use the verifier shipped with your edition — in-app **Verify**, blueCheck SDK `verifyReceipt`, or CLI if provided.
3. Confirm **signature valid** and compare hashes to files on disk if your policy requires it.

Advanced cross-machine hash workflows may be behind feature flags; see [Verify receipts](/how-to/verify-receipts).

Offline verification means: once you have the receipt and the public key material (bundled in the app or SDK), **no network** is required to validate the signature.

## slumberNet and instance keys

[slumberNet](/concepts/slumbernet) adds an **instance keypair**. Payloads your machine signs prove they originated from your install. That is identity of the **node**, not surveillance of your folders.

## blueForge and providers

In blueForge, you connect providers directly. Keys stay on your machine. See [Set up providers](/how-to/set-up-providers).

## If you need a data map for procurement

Gather:

- This page
- Your order's edition (on-prem, VPC SDK, demo)
- [Activation and licensing](/getting-started/licensing) for Authority traffic
- Product quickstart for export paths

Contact MOBLUEHQ support for a DPA or subprocessors list if your process requires it.

## Next

- [Quickstart](/quickstart)
- [Verification concept](/concepts/verification)
- [Report bugs](/how-to/report-bugs) without pasting secrets
