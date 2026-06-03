# Primary Cursor Startup Rule — Public Record (2026-06-03)

**Status:** Active  
**Classification:** Public-safe operating memory  
**Session:** `RECORD_PRIMARY_CURSOR_START_RULE_IN_PUBLIC_MEMORY_2026-06-03`

---

## Rule name (canonical)

**Start Here First — Cursor Working On + Prompt Guard + Skills Review**

This is the **primary and canonical** startup/execution rule for **Cursor**. It is **top-priority** for Cursor sessions on the program owner's workstation.

---

## Precedence

| Layer | Role |
|-------|------|
| **`AGENTS_PROTOCOL.md`** | First governing protocol for all agents (wins on conflict) |
| **This rule (Cursor tool-local)** | **Primary** Cursor startup/execution behavior — Working on table, startup order, drift guard, central audit, owner skills summary |
| **_KnowledgeWiki** (`agents/shared.md`, `agents/cursor.md`, Skill Bank) | Local operational detail and skills — must **align** with this rule; does **not** replace `AGENTS_PROTOCOL.md` |

If any other Cursor instruction, hook text, compact prompt, or standalone rule **duplicates or conflicts** with this primary rule, **`AGENTS_PROTOCOL.md` wins first**, then this primary Cursor rule, then local wiki detail.

---

## What this rule controls (mandatory)

1. **First visible response** — unfenced **`## Working on:`** Item/Details table (emoji-labeled rows per established format). **No prose before the table.** No agent-initiated reads, searches, commands, edits, MCP, network, Skill Bank pulls, or **active** Superpowers invocation **before** the table.

2. **Mandatory startup file order** (after the table):
   1. `D:\MyPrograming\abu-muhammad-memory-public\AGENTS_PROTOCOL.md`
   2. `D:\MyPrograming\_KnowledgeWiki\agents\shared.md`
   3. `D:\MyPrograming\_KnowledgeWiki\agents\cursor.md`

3. **`AGENTS_START_HERE.md`** — **router/navigation only**, read **after** the three mandatory files. It does **not** replace or precede `AGENTS_PROTOCOL.md`, `shared.md`, or `cursor.md`.

4. **`prompt-style-drift-guard`** — pull and apply `D:\MyPrograming\_KnowledgeWiki\skills\prompt-style-drift-guard.md` **before** any other Skill Bank skill or scoped work. Outcomes: **`PROMPT_STYLE_OK`** or **`PROMPT_STYLE_DRIFT_DETECTED`** (stop; central audit only).

5. **Central audit reporting** — every real Cursor operation ends with **full-file overwrite** (append forbidden unless owner explicitly requests history) to:
   - `D:\MyPrograming\What_I_Have_Done\cursor.md`
   - No scattered task-specific reports unless explicitly listed under **Allowed writes** for that session.

6. **Final owner visibility** — after the central audit is written, the session's final chat response includes **`## 🧠 Skills Summary — Owner Review`** (table matching the audit file), plus the session final marker when specified.

7. **Central audit report** — written **before** claiming the task is done; includes required sections per KnowledgeWiki `agents/cursor.md` and `agents/shared.md` (including **`## Skills usage audit`**, token routing when applicable, and **`## 🧠 Skills Summary — Owner Review`** immediately before **`Final status:`**).

---

## Governance — no duplicate rules

- **Do not bypass** this primary Cursor startup/execution rule.
- **Future changes** to Working on format, startup order, `AGENTS_START_HERE` usage, prompt-style drift guard placement, central audit path, or final Skills Summary behavior must be **merged into this rule** (and aligned local wiki files), **not** added as separate overlapping or conflicting standalone rules.
- **Do not create** duplicate standalone Cursor rules for the same behavior (monitoring table, startup chain, drift guard, audit path, skills summary).
- Hooks and Superpowers remain **subordinate**: passive context may exist before the table; **active** skill/tool use waits until after the table and mandatory operating files (unless `AGENTS_PROTOCOL.md` or an explicit owner override for that run says otherwise).

---

## Where full detail lives (local — not wholesale-published)

| Topic | Local path |
|-------|------------|
| Shared session open sequence | `D:\MyPrograming\_KnowledgeWiki\agents\shared.md` |
| Cursor-specific enforcement | `D:\MyPrograming\_KnowledgeWiki\agents\cursor.md` |
| Prompt style drift guard skill | `D:\MyPrograming\_KnowledgeWiki\skills\prompt-style-drift-guard.md` |
| Wiki router | `D:\MyPrograming\_KnowledgeWiki\AGENTS_START_HERE.md` |

---

## Verification note (2026-06-03)

Compliance tests **`CURSOR_RULES_STARTUP_COMPLIANCE_TEST_2026-06-03`** and **`PROMPT_STYLE_DRIFT_GUARD_TRAP_TEST_2026-06-03`** validated correct behavior (Working on first, startup chain, drift guard trap rejection). Evidence: local `D:\MyPrograming\What_I_Have_Done\cursor.md` for those sessions.

---

## ChatGPT / Abu Saleh pointer

For Cursor startup behavior, use this public record + **`AGENTS_PROTOCOL.md`** — do not re-teach long Working on / audit / drift-guard blocks in normal task prompts.
