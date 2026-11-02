---
description: Advance roadmap one slice (phase order, single issue, gated)
subagent: false
---

Advance roadmap one slice. Arguments: $ARGUMENTS.

Convention: `/roadmap-step #<issue> <title> (epic #<epic> <phase>)`.
- First `#<issue>` = the single target sub-issue to implement now. Read it fully.
- `(epic #<epic>)` = the phase container issue for context only (scope order, checklist). Do not implement the whole epic.
- If no epic is given, infer current phase from the roadmap file and state your assumption.

Rules:
- Phases/epics run in order. Do not jump ahead.
- One prompt = one sub-issue. Never implement a whole epic at once.
- Respect the roadmap cut list / out-of-scope section if one exists.

Before coding:
1. Read the roadmap (first one that exists: roadmap file, wiki/Roadmap.md, plan.md, PROJECT_MAP.md) + the epic issue + the target issue.
2. Check GitHub: resolve repo via `gh repo view --json nameWithOwner`, list linked projects (`gh project list --owner <owner>`), confirm the epic and target issue status on the project board. Use the board state as source of truth for order and done gates.
3. Read linked feature/spec docs for this scope.
4. State scope in 3 lines: goal / done / out-of-scope.

Constraints:
- Match existing architecture, layers, and conventions. Reuse helpers already in repo.
- Smallest diff that closes the issue. No new deps, no adjacent refactors, no speculative features.
- Keep values in the form the platform already gives you.

Done = the target issue's acceptance criteria pass plus the repo gates (typecheck, lint, tests, migration up/down clean where applicable).
Verify with the repo's own commands before finishing.

Out of scope: anything from a later phase. Stop and ask if a breaking change to existing auth/schema/contracts is needed.
