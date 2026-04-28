---
layout: ../../layouts/DocsLayout.astro
title: Install blueForge
description: Clone or download blueForge, install dependencies, and run the desktop app locally.
---

## Before you start

You need a Mac or Linux machine with permission to install desktop software. Windows support follows the same Rust plus web shell layout where applicable.

## From source (developers)

1. Clone the `blueforge-desktop` repository from GitHub (MOBLUEHQ source repo).
2. Install Node.js LTS and Rust toolchain (`rustup`) plus platform prerequisites for Tauri.
3. Install JavaScript dependencies:

```bash
npm install
```

4. Run the development shell:

```bash
npm run tauri dev
```

On first launch, forge asks which model providers you want to enable. You can change providers later under Settings.

## Verify the install

Open the chat panel (Smith). Send a short message. If you see a reply and no credential errors in the receipt strip, the install is healthy.

## Next

Continue to [First dispatch](/getting-started/first-dispatch) or [Set up providers](/how-to/set-up-providers).
