# 2910 — Evercore Interview Prep — AV & IT Support Technician

Preparation dashboard for the interview on **Thursday 29 October 2026, 11:30 am** (Paris time) — Microsoft Teams, ~1 hour, **in English** — with Alex Dyson (AV Support Lead EMEA/APAC), Adeal Hafeez (Desktop Engineer, London) and German Moura (AV Technician). Role: **AV & IT Support Technician**, Evercore Paris (rue de Courcelles). Recruiter: Natalie Bowers.

## Files — ONE single file

- `index.html` — **the entire preparation dashboard, in one autonomous file** (opens directly in a browser, jQuery from CDN, ~360 KB):
  - **Groups 01–11**: the interview trainer (topic-based, ~105 questions, short answer visible directly under every question, one optional Details button, difficulty badges, clickable table of contents, search)
  - **Group 12**: the full technical reference (candidate profile, availability, 92 programming Q&A, glossary, EV0–EV14 deep material) — folded by default, same file
  - **All groups open on page load** — maximum visibility; Details and reference sections stay folded until you click
- `vercel.json` — static deployment config (cleanUrls)
- `.gitignore` — Windows/macOS artefacts, editors, backups

## Structure — 19 sections, ~330 collapsible entries

**Base sections (0–3):**
- **0. 👤 Candidate Profile** — background, three skill sets, recent projects, contact
- **1. 📑 Availability & Practical Details**
- **2. 💻 Programming & Scripting** — 92 Q&A: Python (14), Django (15), Java (15), Spring Boot (15), Angular (15), Core Concepts (18) — each with Definition / Example / Use case
- **3. 📖 Abbreviations Glossary** — 7 categories

**Evercore interview sections (EV0–EV14), English answers + short notes:**
EV0 Introduction & Background (pitch 60/90 s) · EV1 AV Fundamentals · EV2 Crestron · EV3 Q-SYS · EV4 Zoom Rooms & Teams Rooms · EV5 Logitech/Poly/Neat · EV6 Windows & Desktop Support L2 · EV7 Networking (concepts + 8 commands) · EV8 14 troubleshooting scenarios · EV9 Security & Procedures · EV10 APSI Experience & Behavioural · EV11 Questions to Ask · EV12 English Interview Phrases · EV13 Technical References · EV14 Recruiter Check (salary, 5-year plan, physical work, on-call, ITSM, "why you over a Crestron candidate").

Every EV section starts with a **⚡ QUICK ANSWER** — a short, spoken-English answer with keywords.

## Facts policy

- APSI is presented as **a healthcare association** (22 years, ~300 workstations, multisite).
- Real AV example included: board meeting with ~130 people (microphones, batteries, audio levels).
- **No invented experience**: Crestron/Q-SYS/Zoom Rooms/Intune/Autopilot are always presented as "understood, never administered in production". The remaining `PERSONAL EXAMPLE — TO BE COMPLETED` blocks list the facts to fill in before the interview.
- The Evercore source fiches mentioned in the original brief were **not found on disk** — content written from the specification only (transparency block in EV13).

## Removed as too specific to the previous (L'Escalator / Growth Ops) application

- Sections "Échanges et pistes de collaboration", "L'Escalator — écosystème", "Synthèse et référentiel Growth"
- Growth hacking / KPI formulas / Growth frameworks Q&A and the Growth & Marketing glossary
- All mentions of L'Escalator and Joanna

## Revision priorities

1. **EV2 Crestron** and **EV3 Q-SYS** (likely probes from German and Alex)
2. **EV8** — troubleshooting scenarios in English (Symptoms → Checks → Diagnosis → Workaround → Resolution → Documentation → Escalation)
3. **EV0** — 60-second pitch, spoken without notes
4. Then EV4, EV12, and EV14 (salary, five-year plan, notice period — complete the TO BE COMPLETED blocks first)



## Vercel deployment (repo name: everScore_2610_focusSelect)

The project is a static site — no build step required. `index.html` is the entry point: Vercel serves it at the root, and it redirects to `index.html` (the main trainer). `vercel.json` enables clean URLs (`.html` extension removed) — all internal links keep working.

**Deploy steps:**

1. Go to [vercel.com/new](https://vercel.com/new) and import the GitHub repository `LucasTymen/everScore_2610_focusSelect`.
2. Project name: `everScore_2610_focusSelect` (same as the repo).
3. Framework preset: **Other** (static). Root directory: default (`./`). No build command, no output directory.
4. Click **Deploy**. Every push to `main` now redeploys automatically.

Result: `https://everScore-2610-focusselect.vercel.app/` (or the final URL shown by Vercel) serves the interview trainer.
