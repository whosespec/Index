---
description: Opus plans, Haiku executes. Run a task through the planner/executor pipeline.
argument-hint: <task description>
---
Task: $ARGUMENTS

Run this pipeline. Do not implement anything yourself.

1. **Plan** – spawn the `planner` subagent with the task above plus any relevant context from this conversation. Show the user the plan briefly.
2. **Execute** – for each step in order, spawn the `executor` subagent with that step's full text (title, files, instructions, done-when). Independent steps may run in parallel. Give the executor nothing else it doesn't need.
3. **Handle failures** – if an executor reports `blocked`, do not retry blindly: send the blocker back to `planner` for a revised step, then re-run that step once. If it blocks again, stop and ask the user.
4. **Verify** – after the last step, run the project's tests/checks yourself (or confirm each step's done-when). Report what was changed and the verification result honestly, including anything not verified.
