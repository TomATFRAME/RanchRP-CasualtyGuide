# Casualty's Field Guide (Ranch Roleplay) — Handoff / Where I Left Off

_Last updated: 2026-07-26 · Branch: `claude/organize-coding-events-niw91q` (identical to `main`)_

## What this project is

An interactive medical roleplay reference for the State of Monroe (Ranch Roleplay). The **entire app is one file** — `src/App.jsx` — built with Vite + React 18. It renders body-art diagrams with clickable injury zones and quick-reference guides.

## Where it is right now

Working and deployable to Vercel (auto-detects Vite). Last change 2026-04-23. Recent work has been about anatomical accuracy and content:

- Rewrote body-zone coordinates to match the body-art coordinate space; fixed alignment.
- Added back-view labels; "Left/Right Heel" instead of "Toes" on the back view; moved lower abdomen up; tightened face zones.
- Added a **scalping** injury type (locked severe/critical, requires a surgeon).
- Added a **Drugs & Substances Guide** to the Quick Reference.
- Made the dark-mode toggle bigger / more visible.

## What's next

There's no tracked TODO list — pick up from the recent themes:

- Continue refining injury types and their severity/lock rules (the scalping/surgeon pattern is the current model).
- Keep improving body-zone coordinate accuracy against the body art.
- Expand Quick Reference content (the Drugs & Substances guide was the latest addition).

## Set up on a new computer

```bash
git clone https://github.com/TomATFRAME/RanchRP-CasualtyGuide.git
cd RanchRP-CasualtyGuide
npm install
npm run dev        # opens at http://localhost:5173
```

Edit `src/App.jsx` — that's the whole app. Push to GitHub and Vercel auto-deploys. Optional custom domain: Vercel → Settings → Domains, then a `CNAME` at your registrar pointing to `cname.vercel-dns.com`.

⚠️ **Heads up:** this project also lives as a git **submodule inside ResumeForge** (linked from `github.com/dubsarge/casualty-guide`). If you change the guide, be aware ResumeForge pins a specific commit of it.

📌 **Repo note:** `AGENTS.md` warns this is a modified Next-style toolchain in places — read the relevant guide under `node_modules/next/dist/docs/` before assuming standard APIs. (For this app the surface is just Vite/React, but keep it in mind.)
