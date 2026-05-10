# CodexSkills (Public Safe)

Last updated: 2026-05-10  
Status: **Officially adopted** — Codex is a **controlled terminal executor** in the workflow system.

## Formal adoption (baseline)
- **Codex CLI** has been **installed, run, and tested** successfully.
- **Codex** is now treated as an **official execution arm** alongside ChatGPT / Cursor / Claude Code, always within written guardrails (see below).

## Canonical locations
| Layer | Location |
|-------|-----------|
| **Local skills pack (authoritative on workstation)** | `D:\MyPrograming\CodexSkills` (`AGENTS.md` + `skills/`) |
| **Private GitHub mirror (skills source of truth in Git)** | `https://github.com/Alodhaibee/CodexSkills` (**Private** repository) |

This **public memory repo** describes CodexSkills **safely**; it does **not** host the skill file contents.

## Git verification snapshot (CodexSkills repo)
- **Last accepted commit:** `44811e6f5e88876037423f2ab89ed4077b1cfc27`
- **Push state:** `PUSH_VERIFIED` (local `HEAD` matched `origin` after push when recorded).

## Current skills (folder names)
- `codex_workflow` — default safe workflow, bans, audit format, verification expectations.
- `memory_github_reader` — read **public** memory from the local clone whose root contains `00_MASTER_MEMORY_INDEX.md`; index-first, single project file afterward.
- `safe_project_executor` — minimal reads, no ground-up rebuild, user-directed checks, then audit report.

## Approved Codex operating rules
1. Work only in a **clearly scoped** workspace/path.
2. **No delete, no move, no rename** unless **explicitly instructed**.
3. **No `git commit` / `git push`** unless **explicitly instructed**.
4. **No network access** unless **explicitly instructed**.
5. **No package installs** unless **explicitly instructed**.
6. After each execution batch, write the audit report at **`D:\MyPrograming\What_I_Have_Done.md`** — **overwrite** (latest run only), **not append**.
7. Do **not** place that report inside individual project folders unless explicitly requested.
8. Obtain **explicit user approval** before naming any **new** durable folder / project / tool / skill / important file / artifact.
9. Do **not** use **`AbuMuhammad`** as a **default prefix** for neutral names; prefer neutral labels such as **CodexSkills**, **Codex Workflow**, **Project Control Center**.
10. The phrase **“أبو محمد”** is primarily **vocative** (addressing the user), not a branding prefix for every artifact.

## Relationship to the old sandbox
- **`D:\MyPrograming\test_codex`** was a **temporary sandbox** for early Codex CLI checks; **not canonical**.
- After validation, work consolidated under **`D:\MyPrograming\CodexSkills`** and the private **`CodexSkills`** GitHub repo.

## Codex’s role in the ecosystem
- Strong **terminal-side** executor with `AGENTS.md` + skills; **MCP** may attach later.
- Does **not** replace explicit human approval for naming, risky changes, or publishing.

## How other actors relate (high level)
- **ChatGPT:** planning, review, prompts, decisions, reading execution reports.
- **Codex:** terminal executor bound to **CodexSkills** rules + skills.
- **Cursor:** IDE-visible editing and typical repo workflows.
- **Claude Code:** deeper coding passes when needed.
- **Abu Muhammad Project Control Center:** local dashboard under `D:\MyPrograming`.
- **GitHub Memory (this repo):** public-safe orientation — **not** a secrets vault.

## Naming policy (reference)
- Same as global rules: approval before **new** durable names; no default **`AbuMuhammad`** prefix; vocative use of **أبو محمد** only.

## Audit report rule (workspace)
Structured overwrite of `D:\MyPrograming\What_I_Have_Done.md` after runs — see **`01_GLOBAL_RULES.md`** for the shared executor baseline.

## Related safe files
- `01_GLOBAL_RULES.md`
- `03_TOOLS_AND_ENVIRONMENT.md`
- `04_ACTIVE_PROJECTS.md`
- `projects/ABU_MUHAMMAD_PROJECT_CONTROL_CENTER.md`

## Next-task guidance
For execution detail, use the **local** pack at `D:\MyPrograming\CodexSkills` and/or the **private** GitHub repo above (with appropriate access). For **public-safe** summaries only, stay within this file.
