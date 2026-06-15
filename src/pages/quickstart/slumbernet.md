---
layout: ../../layouts/DocsLayout.astro
title: slumberNet quickstart
description: Donate idle compute to the verified AI mesh; yields when you return.
---

**slumberNet** lets a capable machine **donate idle time** to the MOBLUEHQ mesh. While you are away, it helps run verified AI work for the network. When you come back, it **yields immediately** so your own apps stay responsive.

Status today: **demo available** by request. For the signing concepts behind slumberNet payloads, see [slumberNet concept](/concepts/slumbernet).

## What it is

- A background agent on your machine, not a separate chat product
- Uses your hardware only when idle (CPU/GPU thresholds vary by build)
- Signs work with your instance keypair so the mesh can trust payloads from your node

## Install

1. Get the slumberNet installer from your MOBLUEHQ demo or fleet onboarding email.
2. Install and grant the permissions the installer requests (notifications, background compute — platform-specific).
3. Activate the device under your license; mesh nodes count toward your **machine limit** like other products.

## First run

1. Open slumberNet settings and set **idle threshold** (for example 15 minutes after last input) and **yield policy** (pause when any local MOBLUEHQ app is foreground).
2. Enable **mesh participation** if it is off by default in your edition.
3. Leave the machine idle past the threshold. The status icon should move to **Contributing** or similar.
4. Use the machine again — contribution should stop within seconds.

## Where results and receipts appear

| Output              | Location                                                               |
| ------------------- | ---------------------------------------------------------------------- |
| Contribution status | Menu bar or system tray icon                                           |
| Session log         | slumberNet **Activity** window — jobs accepted, completed, yielded     |
| Signed job receipts | Activity detail per job — export when your build includes audit export |

You do not read customer-facing screening or chart results here; those stay in blueMoat, blueChart, and other apps. slumberNet only shows **your node's** mesh work.

## Privacy

- Jobs are verified workloads, not your personal files
- Your instance keypair signs outbound work; see [Offline and privacy](/concepts/offline-and-privacy)
- Opt out anytime by disabling mesh participation or quitting the agent

## Shipped limitations

- Demo / invite-only install
- Fleet policy console (**blueFleet**) — **coming** for org-wide rollout
- Earnings or credits display — **not shipped** in current demo

## Next

- [slumberNet concept](/concepts/slumbernet)
- [Activation and licensing](/getting-started/licensing)
- [Support](/getting-started/support)
