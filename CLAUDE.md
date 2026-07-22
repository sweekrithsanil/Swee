# CLAUDE.md

Guidance for AI assistants (and humans) working in the **Swee** repository.

> **Status: Bootstrap / empty repository.**
> As of the last update this repo contains no application source yet. This file
> documents the conventions that already apply (git workflow, commit style) and
> reserves clearly-marked placeholder sections to fill in as real code lands.
> **When you add code, update the matching section below in the same change** —
> keep this file honest about the *current* state, never aspirational.

## Project overview

_TODO: One paragraph on what Swee is — the problem it solves, who uses it, and
its core purpose. Replace this once the project's direction is set._

- **Name:** Swee
- **Repository:** `sweekrithsanil/Swee`
- **Language / stack:** _TODO — not yet chosen_
- **Status:** pre-initial-commit

## Repository structure

_TODO: Document the directory layout as it forms. Suggested format:_

```
.
├── CLAUDE.md          # This file — AI/developer guidance
├── README.md          # Human-facing project intro
└── .gitignore         # Ignored paths
```

Update this tree whenever you add a top-level directory, and note what each one
is responsible for.

## Development workflow

_TODO: Fill in once tooling exists. Capture the real commands, e.g.:_

- **Install dependencies:** _TODO_
- **Run locally:** _TODO_
- **Build:** _TODO_
- **Test:** _TODO_
- **Lint / format:** _TODO_

Prefer documenting commands that actually exist in the repo (a `Makefile`,
`package.json` scripts, etc.) over generic advice.

## Git & branch conventions

These conventions are already in force:

- **Feature branches** follow the pattern `claude/<short-topic>-<suffix>`
  (e.g. `claude/claude-md-docs-5fd3yj`). Develop on the assigned branch; never
  push directly to the default branch without explicit permission.
- **Create the branch locally** if it doesn't exist, commit your work with
  clear, descriptive messages, then `git push -u origin <branch-name>`.
- **Commit messages:** imperative mood, concise subject line (≤ ~72 chars),
  with a body explaining *why* when the change isn't self-evident.
- **Pull requests:** only open one when explicitly requested. If a PR template
  exists under `.github/`, mirror its structure.

## Coding conventions

_TODO: Record the real conventions once a language is chosen — naming, file
organization, formatting rules, error-handling patterns, and any linters/
formatters that enforce them. Until then, match whatever style the first
committed code establishes, and prefer the project's existing idioms over
personal preference._

## Testing

_TODO: Describe the test framework, where tests live, how to run the full suite
vs. a single test, and the expectation for new code (e.g. "every new module
ships with tests")._

## Notes for AI assistants

- This is the primary memory file. Keep it current: when you change how the
  project is built, run, or structured, update the relevant section here in the
  **same** commit.
- Do not fabricate structure. If a section is still a placeholder, leave the
  `TODO` marker rather than inventing details that aren't in the codebase.
- Follow the git & branch conventions above for every change.
