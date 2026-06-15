---
layout: ../../layouts/DocsLayout.astro
title: blueCheck SDK quickstart
description: Embed MOBLUEHQ verification — signed receipts, offline verify, council with judge-and-doer separation.
---

**blueCheck** is the verification engine MOBLUEHQ products embed. The **SDK** lets your application request a verified answer and receive a **signed receipt** you can store, audit, and verify without calling MOBLUEHQ again.

Public package indexes may not list the SDK yet. Use the **install command and registry URL** in your onboarding email or private artifact feed.

## What it is

- **Signed receipts** for each verification run
- **Offline verification** of those receipts after the fact
- **Council** flows with **judge-and-doer separation** where your integration enables them

## Install

1. Add the SDK using the command from onboarding (private npm feed, git tag, or vendored tarball — edition-specific).
2. Configure the **License Authority** endpoint and your **product key** in environment variables or a local config file your security team approves. Keys stay in your infrastructure; the SDK does not send them to MOBLUEHQ chat logs.
3. Install any native verifier CLI if your edition includes one (optional for offline verify).

Example shape only — replace with your edition's names:

```bash
# Example — use the exact command from onboarding
npm install @mobluehq/bluecheck-sdk --registry=https://<your-feed>
```

## First run

1. Initialize the client with your license material and the device activation from [Activation and licensing](/getting-started/licensing).
2. Call the smallest verify API your app needs — for example a single prompt with one model lane.
3. Read the response object: you should get an answer payload and a **receipt** block (signature, algorithm, timestamp, lane metadata).
4. Run the bundled **verify** helper or CLI against the receipt JSON. Offline verify should return valid without a network call if the receipt is intact.

```javascript
// Illustrative — API names follow your SDK version
import { BlueCheckClient } from "@mobluehq/bluecheck-sdk";

const client = new BlueCheckClient({ licensePath: "./bluecheck.license" });
const result = await client.verify({ prompt: "Hello", council: false });
console.log(result.receipt); // store this
```

## Where results and receipts appear

| Output                       | Location                                              |
| ---------------------------- | ----------------------------------------------------- |
| Answer / verification result | Your app — `result` or equivalent field               |
| Signed receipt               | `result.receipt` — persist to your DB or object store |
| Verification status          | SDK `verifyReceipt(receipt)` or CLI — local           |

Wire receipt storage into your audit trail. For field-level receipt anatomy, see [Verification](/concepts/verification) and [Receipt log](/concepts/receipt-log).

## Coming later (not in your SDK yet)

- Public npm without a private feed — **coming**
- Hosted dashboard for receipt search — **coming** for most editions

## Next

- [Offline and privacy](/concepts/offline-and-privacy)
- [Verify receipts](/how-to/verify-receipts)
- [Report bugs](/how-to/report-bugs) from any MOBLUEHQ shell that includes Report
