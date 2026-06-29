# /delivery

`/delivery` is sufficient by itself. The user does not need to add extra delegation phrases.
The command means full safe release-owner delegation:

```
task → acceptance criteria → implementation → result quality gate → local checks
→ PR → PR health → merge if permitted → deploy → live proof → final report
```

## Project Adapter

- Repository: `andylitvinov-design/alchemist`
- Default branch: `codex/bootstrap-alchemist`
- Target branch: `codex/bootstrap-alchemist`
- Package manager: none (static HTML)
- Framework: static HTML
- Build command: none (static files)
- Check command: open index.html in browser
- CI: none confirmed
- Deployment: Vercel (vercel.json present)
- Primary live URL: needs verification ← SUCCESS cannot be claimed without confirmed live URL

**Live URL blocker**: The production Vercel URL for this repo has not been confirmed.
Before any `/delivery` run can reach SUCCESS, verify the live URL:
1. Check Vercel dashboard for project `alchemist` or related name.
2. Record the URL in this file and in AGENTS.md.
3. Rerun `/delivery` after the URL is confirmed.

## Safety Rules

- Do not change env vars, secrets, or Vercel credentials.
- Preserve existing HTML tool functionality (Bach cards, stage checker modules).
- Do not run migrations or data changes.

## Protocol

Act as release owner for this project.

1. Extract acceptance criteria from the original task before coding.
2. Implement the minimum required change.
3. Open modified HTML files in browser to verify visually.
4. Create a PR to `codex/bootstrap-alchemist`.
5. Verify Vercel deployment for the merge (if live URL confirmed).
6. Return STATUS: SUCCESS or STATUS: BLOCKED.

Input format:

Task:
$ARGUMENTS

## Result Quality Gate

| Requirement | Status | Evidence | Verification method |
|---|---|---|---|

Allowed statuses: `PASS`, `PARTIAL`, `FAIL`, `NOT VERIFIED`.
`PARTIAL`, `FAIL`, or `NOT VERIFIED` block STATUS: SUCCESS.

## Stop States

### STATUS: SUCCESS

```txt
LIVE PROOF:
- Live URL:
- Checked route/page:
- Final deployed commit:
- Expected live behavior:
- Actual live behavior:
- Evidence:
```

### STATUS: BLOCKED

```txt
- Where the loop stopped:
- What is complete:
- What is not complete:
- Exact blocker:
- Evidence:
- Required user action:
- Next prompt to run after unblocking:
```

## Rules

- Never claim SUCCESS without confirmed live URL and live proof.
- Stop after 3 failed fix attempts — return STATUS: BLOCKED.
- Never touch env vars or secrets without explicit user approval.
