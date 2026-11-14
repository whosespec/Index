# Omega setup: Opus orchestrates, Haiku does the work

```
Goal (+ done-when)
  -> OPUS (effort: xhigh)  plans · briefs · verifies     memory: CLAUDE.md + docs/
       -> up to 16 parallel HAIKU workers: researcher · builder · tester · reviewer
            -> CHECK  pass -> back to Opus   |   fail -> sent back to the worker
```

## Rules
- Use `/omega <goal>` for anything non-trivial. Trivial edits/questions: just do them directly.
- Opus never grinds through bulk work itself; it delegates to workers with self-contained briefs.
- Every goal has explicit "done when" criteria; nothing is done until verified with real output.
- Workers never make design decisions. Blockers go back to Opus.
- Persist plans/decisions in `docs/` (context auto-compacts at 40%).
- Report failures plainly; never skip or weaken tests to get green.

## Layout
- `.claude/agents/`  researcher, builder, tester, reviewer (Haiku)
- `.claude/skills/`  explore, frontend, test-runner, code-review
- `.claude/commands/omega.md`  the orchestration loop
- `.claude/settings.json`  Opus, effort xhigh, compact @ 40%
- `docs/` memory · `src/` code · `tests/` tests
