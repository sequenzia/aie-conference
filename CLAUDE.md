# AI Engineer World's Fair 2026 — Conference Planning

This repo holds my personalized plan for **AI Engineer World's Fair 2026**
(June 29 – July 2, 2026 · Moscone West, San Francisco · `America/Los_Angeles`).
It exists so an AI assistant (or future me) can pick the plan back up and adjust it
without re-doing discovery or re-running the interview.

> This file is the **portable** copy of my planning profile. A machine-local copy also
> lives in Claude Code's memory store (`~/.claude/projects/.../memory/`), but that does
> not travel with the repo or git — this `CLAUDE.md` does. Keep the two in rough sync.

## Attendee profile (use this to tailor recommendations)

- **Role:** AI/software engineer — a builder who ships product features powered by LLMs/agents.
- **Level:** Advanced (201+). Skip intro/"101" material.
- **Interests, in priority order:**
  1. Agent **harness internals** (context engineering, skills, agent memory, loops)
  2. **Evals / reliability / observability**
  3. **Coding agents & software factories** (AI SDLC)
  4. **Retrieval / memory / graphs**
- **Stack:** Anthropic/Claude (Claude Code, Agent Skills, MCP), OpenAI/Codex, and
  open-source/local models. *Not* focused on cloud-platform managed AI services (AWS/Azure/GCP) —
  deprioritize those vendor sessions.
- **Tie-breaker when two good sessions collide:** prefer **hands-on / apply-it-Monday**
  (code, demos, transferable techniques) over purely frontier/novel. "Frontier" is the
  secondary tie-breaker.
- **Networking:** protect it — keep dedicated expo/lunch blocks even at the cost of a talk.

## Ticket & access constraints

- **Ticket:** Engineering + Workshops.
- **Has access to:** all workshops, all engineering breakout tracks, Main Stage keynotes, expo.
- **NO access to the Leadership track** — sessions physically in the **"Leadership 1 / Leadership 2 /
  Leadership Lounge"** rooms. In the data, that maps to: *AI-Native Enterprises*, *CTO Circle*, and the
  *AI Architects* sub-tracks (Tokenmaxxing / Show My Workflow / AI Factories), plus any stray session
  scheduled in a Leadership room. **Always filter these out** of recommendations (gating is by room, not topic).

## Day → track shape (for fast planning)

- **Day 1 (Mon):** Workshop Day — hands-on across Tracks 1–9. Strategy: one long anchor deep-dive + sharp 1-hr hits.
- **Day 2 (Tue):** Software Factories, Claws & Personal Agents, Search & Retrieval, Forward Deployed Eng. *(secondary interest → lighter, more expo time)*
- **Day 3 (Wed) ⭐:** Context Engineering + Memory & Continual Learning (+ Computer Use, Sandbox). *Strongest day.*
- **Day 4 (Thu) ⭐:** Agentic Engineering + Harness Engineering (+ Local AI, Inference). *Other strongest day.*
- Days 2–4 grid: keynotes 9:00–10:30 · breakouts 10:45–12:25 (20-min talks) · lunch 12:25–1:30 · breakouts 1:30–4:05 · closing keynotes 4:30–5:30.

## Deliverables in this repo

- `aie-wf-2026-schedule.md` — the schedule (picks + backup/alt per slot). **Source of truth for the plan.**
- `aie-wf-2026-schedule.html` — self-contained interactive page (day tabs, reveal backups, check-off
  boxes persisted in `localStorage`, multi-select + export of chosen sessions to Markdown/clipboard or
  `.ics` calendar, Print→PDF). No build step / no network.

The schedule is also mirrored as **45 Google Calendar events** on my primary calendar
(Sequenzia Gmail), in Pacific time, color-coded (keynote=Banana, pick=Blueberry, Day-1 anchor=Tomato,
networking=Basil), with 5-min popup reminders and the backup pick in each event's notes.

## Data source

Conference data comes from the **`aie-worldsfair-2026` MCP server** (configured at the user level):
`get_conference_info`, `get_schedule`, `list_sessions`, `list_speakers`. The full `get_schedule`
payload is large — query it structurally with `jq` rather than reading it linearly.
Some sessions are marked **tentative** (rooms/times may shift) — reconfirm on the official app on the day.

## How to make changes

When asked to adjust the plan:
1. Re-read `aie-wf-2026-schedule.md` for the current state.
2. Apply the change honoring the profile/constraints above (filter Leadership rooms; bias hands-on).
3. **Keep all three in sync:** update the `.md`, the `.html`, and the corresponding Google Calendar
   event(s). Each calendar event's notes already name its backup pick, which makes swaps easy.

## Conventions

- Filenames: kebab-case. Keep the directory structure flat.
- Don't commit or run `git` unless I ask.
