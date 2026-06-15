---
layout: ../../layouts/DocsLayout.astro
title: Activation and licensing
description: Device activation, offline grace, machine limits, reinstall, and the 30-day license check.
---

MOBLUEHQ products share a **License Authority** pattern: your license is tied to devices you activate, with room to work offline, and a periodic online check that does not upload your case data.

## Activate this device

On first launch, products show **Activate this device** (or **Sign in and activate**).

1. Sign in with the account your onboarding email used, or paste the **license key** if your edition is key-based.
2. The app creates a **device record** — a random device ID and a local license blob signed by the Authority.
3. Keep the license file if the app tells you where it lives; you need it for reinstall on the **same** machine.

Activation proves you are within your seat or machine count. It is not telemetry about what you ran.

## Offline grace

After a successful activation, apps work **offline** for a **grace period** (typically 30 days from the last successful Authority check — exact days show in Settings → License).

During grace:

- Verification and receipts still run on-device
- Mesh features that need routing may degrade or pause
- The UI shows **Offline grace** with the date check is due

Reconnect before grace ends to avoid a hard stop. If you are air-gapped by policy, contact MOBLUEHQ for an offline renewal process — not self-serve in all editions yet.

## Machine limit

Each license allows a fixed number of **activated devices** (your order or onboarding email states the count).

| Situation                     | What to do                                                                               |
| ----------------------------- | ---------------------------------------------------------------------------------------- |
| New laptop                    | Activate; if at limit, deactivate an old device first                                    |
| Replaced drive, same computer | Reactivate; same hardware usually reclaims the slot — if not, see recovery below         |
| Shared VM that respawns       | Avoid — each spawn may count as a new device; use dedicated hardware or talk to MOBLUEHQ |

Deactivate from **Settings → License → Devices** inside any MOBLUEHQ app tied to your account, when that screen is available in your build.

## Reinstall and lost device

**Same machine, reinstall OS:**

1. Install the product again.
2. Choose **Restore license** or sign in — the Authority recognizes the device if the ID survived, or you reactivate once.

**Lost or stolen machine:**

1. Deactivate the old device from another activated machine or ask MOBLUEHQ support to revoke it.
2. Activate your replacement.

**Cannot deactivate (dead machine):**

Email support with your account email and approximate device name. Support can release a slot after verification. See [Support](/getting-started/support).

## Why check once every 30 days?

The License Authority needs a **lightweight online handshake** about once every 30 days to:

- Confirm the license is still valid (payment, trial end, revocation)
- Refresh signed grace metadata your app stores locally
- Enforce machine limits without running a constant phone-home

**What leaves your device on that check:** license ID, device ID, product edition, and a nonce — **not** your prompts, documents, screenings, or chat history.

**The privacy bargain:** you get long offline grace and local execution; MOBLUEHQ gets enough signal to run a honest subscription without watching your work. Case content stays on your machine or in exports **you** choose to store.

If check fails due to network, you keep working until grace expires. Fix firewall allowlists for the hostnames in your onboarding packet.

## Common errors

| Message               | Likely cause          | Fix                       |
| --------------------- | --------------------- | ------------------------- |
| Machine limit reached | Too many activations  | Deactivate another device |
| License expired       | Trial or term ended   | Renew with MOBLUEHQ       |
| Activation required   | No local license blob | Sign in and activate      |
| Check failed          | Network or clock skew | Retry; verify system time |
| Revoked               | Chargeback or policy  | Contact support           |

## Next

- [Offline and privacy](/concepts/offline-and-privacy)
- [Support](/getting-started/support)
- [Quickstart hub](/quickstart)
