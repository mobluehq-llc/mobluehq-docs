---
layout: ../../layouts/DocsLayout.astro
title: Beta and known issues
description: What to expect in early customer builds, current limitations, and where to check live status.
---

MOBLUEHQ is onboarding **first customers** ahead of broader launch. Expect beta-quality edges. This page deflects repeat questions — check here before you open a ticket.

## What beta means for you

- Features described as **demo** or **private** in [Quickstart](/quickstart) are real but not self-serve public yet
- UI labels and menu names may shift between builds
- Performance varies with mesh load and model providers you attach
- Documentation may lag the build you received — if behavior disagrees with docs, the build wins; file a doc bug via **Report**

## System status (live)

Aggregate health is published on the **[MOBLUEHQ status page](https://mobluehq-status.pages.dev)** — derived from the public bug registry, not a separate manual dashboard.

Check status before assuming your install is broken.

### Area summary (customer-facing)

Status language on the page may show symbols; meanings:

| Area       | Typical meaning                                        |
| ---------- | ------------------------------------------------------ |
| Smith chat | Chat panel in forge-family shells — may be degraded    |
| Dispatch   | Agent runs and tool loops — known pain in active fixes |
| Receipts   | Receipt capture and export — generally stable          |
| Linda      | Customer vertical experiences — may be partial         |

Refresh the status page for current symbols; do not rely on this doc for live color codes.

## Known limitations (shipped)

These are **current** product limits, not a roadmap promise.

### blueForge / Apprentice (forge desktop)

- Apprentice may issue many tool calls without completing writes — tracked as active investigations
- Long coder loops can hit iteration caps and stop with a lane-failed message
- Shell command parsing rejects some valid compound commands after recent hardening
- Child spawn budget can block retries on large sprints

Use receipts to see what actually ran. See [Troubleshooting](/getting-started/troubleshooting).

### blueMoat

- Large disclosures increase run time and mesh queue wait
- Second-opinion lanes depend on mesh availability

### blueChart

- Private demo — templates and criteria packs vary by agreement
- No autonomous denial — by architecture, not a bug

### blueCheck SDK

- Private registry install — public npm **coming**
- Council configuration is edition-specific

### blueGlu and slumberNet

- Demo distribution only
- Unified settings for mesh + chat **coming**

### Licensing

- Air-gapped renewal may require support — not all editions self-serve

## Open issues (registry snapshot)

The status page lists open bugs with IDs. Examples that have been public:

- Tool-heavy dispatches that never write files
- Wrong-path filing suggestions under high confidence
- Spawn budget exceeded on nested retries

Resolved items move to the archive on the status page.

## What we are not fixing in beta

- Requests for autonomous utilization **denial** in blueChart — out of scope by design
- Using one license on unlimited VMs — use [machine limits](/getting-started/licensing) or talk to sales
- Bypassing receipt signing — verification is the product

## Before you report

1. [Status page](https://mobluehq-status.pages.dev)
2. [Troubleshooting](/getting-started/troubleshooting) or product quickstart
3. [Support](/getting-started/support) for how to file with logs

## Next

- [Quickstart](/quickstart)
- [Support expectations](/getting-started/support)
- [Changelog](/changelog)
