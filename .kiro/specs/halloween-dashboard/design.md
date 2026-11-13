# Design — Haunted Hub

## Overview
Single static `index.html`, no build step, no backend. Dark haunted theme: deep purple-black background, pumpkin orange accents, ghost green highlights. All state that must persist (the EXAONE key) lives in localStorage only.

## Architecture
- `index.html` — everything: markup, CSS, JS in one file so it deploys anywhere (GitHub Pages, Cloudflare Pages, Vercel).
- Data: a `SITES` array in JS (12 real sites). Deals: live fetch from `https://new.xianbao.fun/api/v1/feed?limit=5`, fallback to samples.
- AI: direct browser `fetch` to `https://api.exaone.ai/v1/chat/completions`, model `k-exaone_v2.5`, `Authorization: Bearer <key>`.

## UI
- Header: pumpkins, title, badges (Costume Contest / Kiroween 2026 / Built with Kiro / EXAONE inside), three countdowns.
- Search box filters cards live.
- Cards: name, description, tag, new-tab link.
- EXAONE panel: password key input, prompt textarea, preset buttons, output box, exact-request note for CORS fallback.
- Deals: refresh button, live or sample items.

## Security
- No API key, password or secret is committed. `.gitignore` excludes any local key file. The key field is `type=password` and is only written to localStorage on the user's own machine.
