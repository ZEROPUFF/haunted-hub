# Tasks — Haunted Hub

- [x] 1. Scaffold the static dashboard
  - Single `index.html`, spooky dark theme, header + countdowns
  - Searchable cards for 12 real tools/domains
- [x] 2. Add the EXAONE panel
  - Local-only key input (localStorage), preset prompts
  - POST to api.exaone.ai/v1/chat/completions, model k-exaone_v2.5
  - Error + exact-request fallback for CORS blocks
- [x] 3. Add the deals feed
  - Live fetch from new.xianbao.fun/api/v1/feed, fallback samples
- [x] 4. Add Kiroween compliance files
  - `.kiro/specs/halloween-dashboard/` requirements, design, tasks
  - `README.md` with run + submission checklist
  - `.gitignore` so no key is ever committed
- [ ] 5. Test with a real EXAONE key (needs the user's key, via secure entry — not in chat)
- [ ] 6. Push to a new GitHub repo and submit on Devpost by Dec 4, 14:00 PT
