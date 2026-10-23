---
name: memory
description: Persistent project memory. Use when the user says "remember", "تذكر", "احفظ", "لا تنسى", asks what you remember, or asks to forget something. Also read it at the start of any task to recall the user's preferences and project decisions.
---

# Memory

Memory lives in `.claude/memory.md` at the project root (create it if missing).
Commit and push it so cloud sessions keep it between sessions.

## Recall
- At the start of a task, read `.claude/memory.md` if it exists and follow what it says.
- When the user asks "what do you remember" / "وش تتذكر", summarize the file.

## Remember
When the user asks you to remember something, or states a lasting preference or decision:
1. Write it as one short line under the right heading:
   - `## Preferences` (language, style, tools)
   - `## Project` (architecture, decisions, conventions)
   - `## People & context`
2. Add the date: `- (2026-10-23) Prefers answers in Gulf Arabic`
3. If an existing line says the opposite, replace it instead of adding a duplicate.
4. Confirm in one line what you saved.

## Forget
When asked to forget something, delete the matching line and confirm.

## Rules
- Never store passwords, API keys, tokens or other secrets.
- Keep lines short and factual; no conversation transcripts.
- Keep the file under ~200 lines; merge or drop stale entries.
