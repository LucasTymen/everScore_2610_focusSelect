# 2910 — Evercore Interview Prep — AV & IT Support Technician

Preparation dashboard for the interview on **Thursday 29 October 2026, 11:30 am** (Paris time) — Microsoft Teams, ~1 hour, **in English** — with Alex Dyson (AV Support Lead EMEA/APAC), Adeal Hafeez (Desktop Engineer, London) and German Moura (AV Technician). Role: **AV & IT Support Technician**, Evercore Paris (rue de Courcelles). Recruiter: Natalie Bowers.

## Files — ONE single file

- `index.html` — **the entire preparation dashboard, in one autonomous file** (opens directly in a browser, fully self-contained — jQuery embedded inline, no CDN, no internet needed, ~450 KB):
  - **Groups 01–11**: the interview trainer (topic-based, ~105 questions, short answer visible directly under every question, one optional Details button, difficulty badges, clickable table of contents, search)
  - **Group 12**: the full technical reference (candidate profile, availability, 92 programming Q&A, glossary, EV0–EV14 deep material) — folded by default, same file
  - **All groups open on page load** — maximum visibility; Details and reference sections stay folded until you click
- `vercel.json` — static deployment config (cleanUrls)
- `.gitignore` — Windows/macOS artefacts, editors, backups

## Structure — 12 topic groups (all in index.html)

- **01 Introduction & motivation** — pitch, why Evercore, salary/notice (12 Q)
- **02 AV daily operations** — morning checks, room setup per event, microphones/batteries (9 Q)
- **03 AV systems** — Zoom/Teams Rooms, Crestron, Q-SYS, peripherals (11 Q)
- **04 AV troubleshooting** — 11 scenarios in CHECK → TEST → WORKAROUND → INFORM → LOG format
- **05 Windows & desktop** — drivers, sound, docks, sign-in, M365 (13 Q)
- **06 Networking** — one-line definitions (DNS, DHCP, VLAN…) + command sequence (12 Q)
- **07 Security & infrastructure** — malware, suspicious attachments, VMs, ITIL, PowerShell (8 Q)
- **08 APSI experience** — 22 years, GLPI (resolution time), AnyDesk, limited AD exposure, board meeting (8 Q)
- **09 Behavioural** — pressure, seniors, escalation, procedures (9 Q)
- **10 Interview simulation** — expected focus per interviewer (Alex · Adeal · German)
- **11 Quick revision** — 12 flashcard definitions, reflex sentences, numbers to remember, TO-BE-COMPLETED checklist
- **12 Technical reference — full material** (folded): candidate profile, availability, 92 programming Q&A, glossary, EV0–EV14 deep content

Every trainer question: **short answer visible directly** under the question (10–25 words, spoken British English), one optional **Details** button, difficulty badge (Essential/Useful/Advanced). Contents menu + search at the top; all groups open on page load.

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
