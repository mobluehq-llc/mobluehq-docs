---
layout: ../../layouts/DocsLayout.astro
title: Report bugs
description: Use the in-product Report button, then track status on the public MOBLUEHQ status page.
---

## Fast path

1. In forge, open **Report** from the menu or command palette (exact label follows your build).
2. Describe what you saw. Attach logs when the form offers it.
3. Note the reference ID if one is shown.

## Public status

MOBLUEHQ publishes aggregate status derived from the canonical bug registry. Open the [system status page](https://mobluehq-status.pages.dev) for customer-facing incident language without needing GitHub.

## Docs and triage

Documentation updates land on this site. Network triage for verified reports is rolling out on MOBLUEHQ infrastructure; when live, your client will show "Filed as Bug #N" after a successful signed submit.

## Privacy

Do not paste secrets into reports. The form scrubs common key patterns when enabled, but you should rotate anything that leaked.
