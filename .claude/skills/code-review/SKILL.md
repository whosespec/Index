---
name: code-review
description: Checklist for reviewing changes against requirements.
---
Check in order: (1) does it meet every requirement and "done when" criterion; (2) correctness bugs and unhandled edge cases; (3) security (input handling, secrets); (4) tests cover the change; (5) needless complexity or scope creep.
Report only real findings with `file:line`, severity (blocker/should/nit) and a concrete fix. Say `pass` only if there are no blockers.
