# 🎃 Zeropuff's Haunted Hub — Kiroween 2026

**Category:** Costume Contest
**Built with:** Kiro (spec-driven) + EXAONE 2.5 (LG AI Research, free API)

A Halloween-themed personal dashboard that collects free tools, domains and daily deals in one place, with a polished spooky UI that actually helps you find things faster.

## What it does

- **Free tools & domains** — searchable cards for the sites the author actually uses: Cloudflare, SEUS, DNSHE, DigitalPlat, KataBump, LXI.be, eu.org, EXAONE, 线报酷, Kiro, GitHub and Kiroween itself.
- **Ask EXAONE** — a built-in panel that calls LG's K-EXAONE 2.5 (`k-exaone_v2.5`, `POST https://api.exaone.ai/v1/chat/completions`, OpenAI-compatible). Presets: summarize today's deals, recommend a free tool, Kiro tips, explain the Public Suffix List.
  - **Your API key stays in your browser only** (localStorage). It is never sent anywhere else and never committed to the repo. There is no key in this repo.
- **Today's deals** — live feed from 线报酷 (Xianbao, public open API, no key). Falls back to sample deals if the browser blocks the live fetch.
- **Countdowns** — credits request closes Dec 1, 12:00 PT; submission closes Dec 4, 14:00 PT; credits expire Dec 31, 23:59 PT.

## Run it

Just open `index.html` in a browser, or deploy the repo to GitHub Pages / Cloudflare Pages / Vercel — it is a single static file, no build step.

To use the EXAONE panel:
1. Get a free key at https://docs.exaone.ai → My profile → API key (no card).
2. Paste it in the dashboard's key box. It is saved only in that browser.
3. Ask a question. If the browser blocks the direct call (CORS), run the same request from curl or your own script — the exact request is shown in the panel.

## Kiroween submission checklist

- [x] New project, created during the submission period (Oct 30 – Dec 4, 2026)
- [x] Built with Kiro — spec in `.kiro/specs/halloween-dashboard/`
- [x] Repo root contains a `.kiro` directory
- [x] Category: Costume Contest
- [ ] Request 4,000 free Kiro credits on the Devpost Resources tab by Dec 1, 12:00 PT (needs Kiro user ID or AWS account ID)
- [ ] Submit on Devpost by Dec 4, 14:00 PT

## Spec

See `.kiro/specs/halloween-dashboard/` — `requirements.md`, `design.md`, `tasks.md`.
