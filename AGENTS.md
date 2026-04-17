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
