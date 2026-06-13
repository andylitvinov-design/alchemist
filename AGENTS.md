# Alchemist AGENTS

## Scope

- Applies to `/Users/andriilitvinov/projects/MYPROJECTS/alchemist`.
- This repo is the canonical Codex project directory for Alchemist-specific HTML tools.

## Rules

- Keep this repo separate from other Alchemy folders so Cloud Codex sees only Alchemist context.
- Keep `README.md` and `STATE.md` current enough to resume safely.
- Treat generated output as disposable unless explicitly promoted to a durable artifact.

## Git

- `main` is production-ready only.
- Do not push directly to `main`.
- Use branch -> PR -> merge for production-facing changes.
- Autosave/checkpoint branches may be created by the workspace preservation flow.
---

## Agent Command Registry

### /delivery

`/delivery` is sufficient by itself. No extra delegation language is required.

When the user invokes `/delivery`, read and follow `.claude/commands/delivery.md`.

Stop only with `STATUS: SUCCESS` or `STATUS: BLOCKED`.

**Project adapter:**

- Repository: `andylitvinov-design/alchemist`
- Default branch: `codex/bootstrap-alchemist`
- Target branch: `codex/bootstrap-alchemist`
- Package manager: none (static HTML)
- Framework: static HTML
- Build: none (static files, open in browser)
- CI: none confirmed
- Deployment: Vercel (vercel.json present)
- Primary live URL: **needs verification** — SUCCESS cannot be claimed without confirmed URL

**Live URL blocker:** Before any /delivery run can reach SUCCESS, confirm the Vercel URL
for this project in the Vercel dashboard and update this file.
