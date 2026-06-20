# AI OPERATING MODEL

Last updated: 2026-06-21
Status: Active

## Collaboration roles

- Abu Muhammad: owner, decision maker, and execution director.
- ChatGPT / Custom GPTs: lightweight index memory, public-safe memory reader, strategic assistant, and coordinator (handoff to Cursor for file/git work).
- Claude: technical session advisor for focused work sessions.
- Cursor: private memory librarian and primary code/document executor.
- Codex Desktop: bounded terminal executor — see **`CODEX_DESKTOP_INSTRUCTIONS.md`**.

## Repository model

| Layer | Role |
|-------|------|
| **_KnowledgeWiki** (private local) | Full operational brain — Canon, agents operating room, Skill Bank, project registries |
| **This public repo** | Public-safe summarized external memory for GPTs and cross-agent coordination |
| **What_I_Have_Done** (local) | Per-agent session audit reports — evidence, not default durable SoT |

## Core AOS concepts (public-safe)

- **Canon** = official source-of-truth layer (paths, precedence, governance).
- **KnowledgeWiki** = organized long-term memory body (private).
- **Reports** = session evidence of what was done and decided.
- Keep **Canon thin**; avoid duplicating rules across many files.

## Safe collaboration flow

1. Start from **`00_MASTER_MEMORY_INDEX.md`**.
2. Read only the relevant public-safe file for the task.
3. Custom GPTs: follow **`07_GPT_AND_ASSISTANT_SETUP.md`**.
4. Check **`STATUS_DASHBOARD.md`** when project status context is needed.
5. Keep sensitive details private; use Cursor for private-memory updates and safe public summaries.
