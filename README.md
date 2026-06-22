<h1>
  <img src="logo.png" alt="QiFlow logo" height="40" valign="middle" />
  &nbsp;QiFlow
</h1>

**A clinician-friendly DMAIC workspace for healthcare QI teams, with an embedded AI coach.**

Live demo: **[qiflow.health](https://qiflow.health)**

## Why QiFlow exists

Healthcare Quality Improvement teams use the DMAIC framework — Define, Measure, Analyze, Improve, Control — to reduce harm, improve care, and meet regulatory targets. In practice, most teams run their projects in a tangle of spreadsheets, Word docs, and Visio diagrams that nobody outside the project can navigate. New team members can't find the aim statement, measure definitions live in someone's email, and "what did we decide about the control plan?" is a question with no good answer.

QiFlow puts the whole DMAIC cycle in one structured workspace where every artifact — problem statement, aim, measures, root-cause analysis, PDSA cycles, control plan — has a clear home and a consistent shape. **QIA**, the embedded AI assistant, sits alongside the workspace and gives phase-aware coaching: it explains DMAIC concepts in plain language, drafts content from project context, and proposes one-click field fills the team can accept or edit.

## Features

**DMAIC workspace**
- **Define** — guided problem statement, aim builder, in/out-of-scope grid
- **Measure** — outcome, process, and balancing measures with operational definitions and baseline values
- **Analyze** — fishbone diagrams, 5 Whys, process maps, impact / effort grids
- **Improve** — PDSA cycle planner with linked tests of change
- **Control** — control plans, monitoring schedules, escalation thresholds, lessons learned

**QIA — the QI assistant**
- Phase-aware agents (each DMAIC phase has its own coaching agent + system prompt)
- Streaming chat with conversation persistence per user, per project
- `FILL_PROPOSAL` flow: QIA proposes values for project fields, user accepts → field is upserted to the database and the UI flashes to confirm
- Membership-gated history: teammates on the same project keep separate threads
- PubMed integration for surfacing relevant clinical literature

**Collaboration**
- Workspaces, projects, role-based invitations
- In-app inbox for invitations and notifications
- Tasks, board view, due dates

## Stack

Next.js 14 (App Router) · TypeScript · Tailwind CSS · Supabase (Postgres + Row-Level Security + Auth) · Anthropic Claude (streaming) · Vercel

## Screenshots

![Dashboard](screenshots/01-dashboard.png)
![Define phase](screenshots/02-define.png)
![QIA panel with field fills](screenshots/03-qia-panel.png)
![QIA fullscreen](screenshots/04-qia-fullscreen.png)

## Status

Phase 1 (DMAIC workspace) and Phase 2 (QIA assistant) are shipped to production. Built solo in collaboration with a Mayo Clinic researcher to align the product with how real QI teams work.

---

*Source code is private. This repo exists to showcase the project.*
