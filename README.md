# 2026 Personal Time Tracker

> A fully deployed, cloud-synced personal time tracker — built without writing a single line of code, using AI (Claude), Supabase, and Netlify.

**Live app →** [your-netlify-url.netlify.app](https://symphonious-valkyrie-fde918.netlify.app)

---

## What It Does

A personal productivity tool to track hours spent across 21 life goals, organised under 6 life pillars. Built to answer one question at the end of every quarter:

> *"How well have I actually spent my time?"*

### Features

- **Log hours** per goal with date — one action, done in seconds
- **By Goal / By Pillar** view toggle with collapsible pillar groups
- **Quarterly breakdown** — total hours + top goals per quarter
- **Yearly overview** — pillar-level bars + all 21 goals ranked by time invested
- **Manage Goals tab** — add, rename, delete, reorder goals from the browser
- **Cross-device sync** — data lives in Supabase, works on phone and laptop
- **Export to CSV** — download all logs to Excel anytime

---

## Life Pillars & Goals

| Pillar | Goals |
|--------|-------|
| 🟢 Deen | 9 goals |
| 🩷 Family | 3 goals |
| 🔵 Career & Finance | 3 goals |
| 🟠 Health | 2 goals |
| 🟣 Education & Knowledge | 2 goals |
| 🟡 Side Quest | 2 goals |

---

## Tech Stack

| Layer | Tool | Cost |
|-------|------|------|
| Frontend | Vanilla HTML/CSS/JS | Free |
| Database | Supabase (PostgreSQL) | Free tier |
| Hosting | Netlify | Free tier |
| Built with | Claude (Anthropic) | — |

No frameworks. No build tools. No npm. A single `index.html` file that talks directly to a Supabase REST API.

---

## How It Was Built

This project was built entirely through conversation with Claude — no manual coding. The process:

1. **Planned goals** using an existing Excel yearly planner
2. **Described the app** to Claude, attached the Excel file → received a complete HTML file
3. **Set up Supabase** — ran a SQL script to create `logs` and `goals` tables
4. **Connected the app** — shared Supabase API keys with Claude → app updated to sync with cloud
5. **Deployed** — dragged a folder to Netlify Drop → live in under 2 minutes
6. **Iterated** — added features (pillar grouping, goal management, sync indicator) through follow-up prompts

Total time: ~2 hours of conversation. Zero prior web development experience required.

The full step-by-step guide is included in this repo as a PowerPoint deck.

---

## Files

```
├── index.html                  # The complete app (single file)
├── how-to-build-your-own.pptx  # 8-slide guide to replicate this project
└── README.md
```

---

## Running Locally

No setup needed. Just open `index.html` in any browser.

Note: The live app connects to a personal Supabase instance. To run your own version with your own data, replace the two constants at the top of the `<script>` tag in `index.html`:

```js
const SUPABASE_URL = 'https://your-project-id.supabase.co';
const SUPABASE_KEY = 'your-anon-public-key';
```

Then run the SQL setup script in your Supabase SQL Editor (see the PowerPoint guide for the full script).

---

## Replicating This Project

The `how-to-build-your-own.pptx` file in this repo walks through all 6 steps with visuals. The short version:

1. Open [claude.ai](https://claude.ai)
2. Describe the app you want + attach your goals document
3. Create a free [Supabase](https://supabase.com) project + run the SQL script Claude gives you
4. Share your Supabase URL + API key with Claude → get an updated HTML file
5. Drag the folder to [app.netlify.com/drop](https://app.netlify.com/drop)
6. Done — you have a live, cross-device synced app

---

## Why I Built This

I'm an MBA candidate at Oxford's Saïd Business School (Class of 2025–26). With heavy coursework, extracurriculars, and personal goals running in parallel, I wanted a way to be intentional about where my time actually goes — not just where I plan for it to go.

This project also served as a personal experiment: *how far can you get with AI tools if you're clear about what you want, without writing code yourself?* The answer, it turns out, is pretty far.

---

*Built by Arief Ramadhan · Oxford MBA 2025–26 · [@arieframadhanm](https://instagram.com/arieframadhanm)*
