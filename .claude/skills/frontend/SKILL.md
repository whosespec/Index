---
name: frontend
description: Conventions for building UI/frontend code in this project.
---
- Match the existing stack and style in `src/`; check `docs/` and CLAUDE.md first.
- Small, single-purpose components; no unused dependencies.
- Accessible by default (labels, semantic elements, keyboard use).
- Handle loading, empty and error states.
- Keep files focused; put shared logic in helpers, not copy-pasted.
