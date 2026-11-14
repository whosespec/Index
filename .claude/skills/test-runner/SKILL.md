---
name: test-runner
description: How to write and run tests and report results.
---
1. Find the project's test command (package.json, Makefile, CLAUDE.md). If none exists, say so.
2. Put tests in `tests/`, mirroring `src/` paths. Cover the happy path, edge cases and failure cases from the brief.
3. Run the narrowest relevant tests first, then the full suite.
4. Report the exact command and real output. Never claim a pass you didn't see; never skip or weaken a test to get green.
