# CLAUDE.md

Guidance for AI assistants (and humans) working in the **Swee** repository.

## What this repo is

**Swee is a personal knowledge & planning workspace — not a software project.**
It's a place to think, collect, and plan across three areas:

1. **Mom's business (Mangalore)** — ideas, market notes, and a plan for
   starting and running a small business in Mangalore, Karnataka.
2. **Inspiration** — business/content ideas captured from Instagram reels and
   LinkedIn, saved before they scroll away, then sorted into "worth trying".
3. **Career** — goals, notes, and opportunities for the repo owner's own career.

Everything lives as plain **Markdown** so it's easy to read, search, edit on a
phone, and keep in git. There is no code to build or run.

## Repository structure

```
.
├── CLAUDE.md              # This file — guidance for AI assistants
├── README.md              # Human-facing intro
├── mom-business/          # Everything about mom's Mangalore business
│   ├── README.md          #   Overview + how this folder is organized
│   ├── ideas.md           #   Running list of business ideas (with a template)
│   ├── plan.md            #   Startup checklist: registration, budget, launch
│   └── research.md        #   Local market notes (competitors, costs, suppliers)
├── inspiration/           # Ideas captured from social media
│   ├── reels.md           #   Ideas seen in Instagram reels / short videos
│   └── linkedin.md        #   Ideas/posts/quotes from LinkedIn
├── career/
│   └── README.md          # Career goals, skills to learn, opportunities
├── .claude/skills/        # Installed AI-agent skills (symlinks into .agents/)
├── .agents/skills/        # Skill source files (shared across agent tools)
└── skills-lock.json       # Lockfile for installed skills
```

Update this tree whenever you add or rename a top-level folder.

## Installed skills

### agent-reach
[Agent Reach](https://github.com/Panniantong/Agent-Reach) is installed at
`.agents/skills/agent-reach/` (symlinked into `.claude/skills/`). It's an
open-source skill that lets the agent search/read the public internet —
LinkedIn, Instagram, Twitter/X, Reddit, YouTube, GitHub and ~15 platforms — with
no API keys. It's here to help capture ideas for `inspiration/` and
`mom-business/` directly from source.

- **How it works:** the committed files are just Markdown (a routing table +
  `references/`). The actual scraping is done by a separate `agent-reach` Python
  CLI, installed on demand with:
  `pip install "https://github.com/Panniantong/agent-reach/archive/main.zip"`
- **Won't run in web/cloud sessions:** this repo's cloud sessions use a
  restricted network proxy that blocks the GitHub CLI download *and* the social
  sites it scrapes. Use it on a **local** Claude Code install instead.
- **Third-party code, flagged risk:** the installer's own scan rated it Snyk
  *High Risk* (it runs shell commands and network scrapers). Review before
  running; treat scraped content as untrusted. To remove:
  `npx skills remove agent-reach` and delete `.agents/skills/agent-reach`.

## How to work in this repo

- **Capturing an idea?** Add a dated entry to the right file
  (`inspiration/reels.md`, `inspiration/linkedin.md`, or
  `mom-business/ideas.md`) using the template already at the top of that file.
  Don't delete old ideas — mark them `[done]`, `[dropped]`, or `[trying]`
  instead, so the history stays.
- **Keep it in the owner's words.** This is a personal workspace. When asked to
  add or summarize, match the plain, practical tone of what's already there —
  don't turn it into a corporate document.
- **Localize to Mangalore.** For the business, prefer concrete, local details
  (rupees, local suppliers, local platforms, Kannada/Tulu where relevant) over
  generic advice.
- **Dates:** use `YYYY-MM-DD` so entries sort naturally.

## Git & branch conventions

- **Feature branches** follow `claude/<short-topic>-<suffix>`
  (e.g. `claude/claude-md-docs-5fd3yj`). Develop on the assigned branch; never
  push to the default branch without explicit permission.
- Create the branch locally if needed, commit with clear messages, then
  `git push -u origin <branch-name>`.
- **Commit messages:** imperative mood, concise subject (≤ ~72 chars), with a
  short body when the *why* isn't obvious.
- **Pull requests:** only open one when explicitly requested.

## Notes for AI assistants

- This is the primary memory file. If the repo's purpose or structure changes,
  update the relevant section here in the **same** commit.
- Don't fabricate detail. If you don't know a real fact about the business
  (budget, location, product), leave a clearly-marked `TODO` and ask, rather
  than inventing it.
