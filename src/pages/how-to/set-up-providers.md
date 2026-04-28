---
layout: ../../layouts/DocsLayout.astro
title: Set up providers
description: Connect Anthropic, OpenAI, Google, or local models using keys that stay on your machine.
---

## Why this page exists

Most questions we hear are some version of "which key goes where." Providers are configured inside blueForge so your keys never pass through MOBLUEHQ servers.

## Steps

1. Open **Settings** from the forge shell.
2. Choose **Providers** (wording may say Models or API keys depending on build).
3. For each vendor you use, paste the API key from that vendor's console.
4. Save. Forge validates keys with a lightweight check when possible.

## Tips

- Start with one provider, confirm chat works, then add alternates.
- Use separate keys for personal and work machines when vendors allow multiple keys.
- If a provider shows red, open the vendor status page in your browser; also check [MOBLUEHQ status](https://mobluehq-status.pages.dev).

## Local models

Point **OLLAMA** or the local endpoint field at your LAN URL (for example `http://127.0.0.1:11434`). There is no cloud hop for local inference.

## Next

Move to [First dispatch](/getting-started/first-dispatch) or [Use council mode](/how-to/use-council-mode).
