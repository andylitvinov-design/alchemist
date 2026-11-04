# Alchemist AGENTS

## Mandatory cross-project PR economy rule — GLOBAL_PR_ONE_PUBLISH_V1

Before **any** GitHub code change, branch publication or PR in this repository, read the [single global protocol](https://raw.githubusercontent.com/andylitvinov-design/ai-projects-brain/main/systems/pr-one-publish-standard.md). Prepare all related code/tests/docs and perform relevant local checks *before the first remote push* (a branch push can itself trigger CI or a paid preview even without an open PR). Publish one coherent branch HEAD, then open one PR; freeze the published HEAD while required checks run. Only publish a new complete HEAD for an independently verified failure or urgent security/correctness fix, then rerun all required checks. Never create per-file remote commit waves, empty CI wake commits, optional workflows, paid services or bypasses of local repository controls. For work without PR/CI this is N/A. This rule supplements all existing safety, deployment, and privacy instructions.


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
