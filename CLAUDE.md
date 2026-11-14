# Workflow: Opus plans, Haiku executes

Goal: spend expensive reasoning only on planning; do the bulk of the work on the cheap model.

- Non-trivial tasks (more than a trivial one-file edit): use `/omega <task>` or follow the same flow manually: `planner` subagent (Opus) -> `executor` subagent (Haiku) once per plan step -> verify.
- Trivial tasks (typo, one-line change, a question): just do them directly.
- The executor never makes design decisions; if it is blocked, the problem goes back to the planner.
- Always verify at the end by running the real checks, and report failures plainly.

Config: `.claude/settings.json` sets `opusplan` (Opus in plan mode, cheap model otherwise); agents live in `.claude/agents/`, the pipeline in `.claude/commands/omega.md`.
