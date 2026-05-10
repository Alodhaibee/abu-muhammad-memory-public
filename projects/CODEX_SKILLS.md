# CodexSkills (Public Safe)

Last updated: 2026-05-10  
Status: Active / Permanent skills pack (local workstation)

## Canonical local path
`D:\MyPrograming\CodexSkills`

This repository documents **what CodexSkills is** and **how it fits the system**. The skill files themselves (`AGENTS.md`, `skills/*/SKILL.md`) live only on the local machine at the path above and are **not** committed to this public memory repo unless explicitly decided later.

## Purpose
- Permanent home for **Codex** agent rules and reusable **skills** (workflow, memory reader, safe project execution).
- Keeps Codex aligned with the same safety posture as other executors: narrow scope, no silent deletes/moves, explicit permission for network installs/commits, and a mandatory workspace audit report.

## Relationship to the old sandbox
- **`D:\MyPrograming\test_codex`** was a **temporary sandbox** for Codex CLI checks. It is **no longer canonical**.
- After a successful Codex CLI permission test (creating `PERMISSION_TEST.txt` and updating `D:\MyPrograming\What_I_Have_Done.md`), work moved to **CodexSkills** as the durable location.
- The sandbox folder was **removed manually** when no longer needed (do not recreate unless explicitly requested).

## Current skills (folder names)
- `codex_workflow` — default safe workflow, bans, audit report shape, verification expectations.
- `memory_github_reader` — read **public** memory from the local clone whose root contains `00_MASTER_MEMORY_INDEX.md` (see skill text); index-first, single project file afterward.
- `safe_project_executor` — minimal reads, no ground-up rebuild, run user-directed checks, then audit report.

## Operating rules (summary)
- Work only in the **requested workspace/path**.
- **No delete / no move** unless explicitly requested.
- **No `git commit` / `git push`** unless explicitly requested.
- **No network / no package installs** unless explicitly requested.
- Prefer **small, reviewable** changes; verify before claiming success.
- **Mandatory report:** `D:\MyPrograming\What_I_Have_Done.md` — **overwrite per run** (latest operation only), **not** append, unless the user defines another scheme.

## Codex’s role in the ecosystem
- **Codex** is a strong **terminal-side executor**, especially with `AGENTS.md` + skills and **future MCP** hooks.
- It always stays inside the guardrails above; it does **not** replace human approval for naming, pushes, or risky actions.

## How other actors relate (high level)
- **ChatGPT:** planning, review, prompt shaping, decisions, reading execution reports.
- **Codex:** terminal executor using CodexSkills + optional MCP later.
- **Cursor:** usual IDE-visible editing and repo work.
- **Claude Code:** deeper programming passes when needed.
- **Abu Muhammad Project Control Center:** local Python dashboard for projects under `D:\MyPrograming` (Git status, open tools, view `What_I_Have_Done.md`, notes).
- **GitHub Memory (this repo):** official **public-safe** shared memory — not a substitute for private operational detail.

## Naming policy (CodexSkills-related)
- **“أبو محمد”** is primarily a **form of address** for the user; it must **not** auto-prefix every tool/skill/file name.
- Avoid introducing **`AbuMuhammad`** as a default prefix for neutral artifacts; prefer clean names such as **CodexSkills**, **Codex Workflow**, **Project Control Center**.
- Before choosing a **new** durable name for a folder/project/tool/skill/artifact, get **explicit user approval**. Exception: names **directly derived** from an already-approved name without changing meaning may be reused without re-asking.

## Audit report rule (workspace)
All executors should end a batch with a structured overwrite of `D:\MyPrograming\What_I_Have_Done.md`, typically including when applicable:
workspace path, goal, files inspected/created/modified/deleted, folders created/deleted, copies/moves, commands, git status if relevant, safety scan if relevant, external/network access (Yes/No), other projects touched (Yes/No), deviations, errors, final status.

## Related safe files
- `01_GLOBAL_RULES.md` — global naming + audit rules.
- `03_TOOLS_AND_ENVIRONMENT.md` — tools and roles overview.
- `04_ACTIVE_PROJECTS.md` — active map including CodexSkills row.
- `projects/ABU_MUHAMMAD_PROJECT_CONTROL_CENTER.md` — Project Control Center summary.

## Next-task guidance
For Codex-specific execution details, read local `AGENTS.md` and the three skill folders under `D:\MyPrograming\CodexSkills`. For **public-safe** orientation only, stay within this file and the global rules above.
