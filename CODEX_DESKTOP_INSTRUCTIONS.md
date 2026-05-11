# Codex Desktop Instructions

## Purpose

This file defines how **Codex Desktop** must work with Abu Muhammad’s **shared memory system**.

Codex Desktop must treat the **public memory repository** as the **safe shared context layer** between agents (ChatGPT, Cursor, Claude, Codex, and Abu Muhammad). It is the canonical place to align on accepted decisions, project routing, and cross-agent coordination—**not** a substitute for private operational detail when the task explicitly requires the private memory repo.

## Public Memory Repository

- **Repository URL:**  
  https://github.com/Alodhaibee/abu-muhammad-memory-public

- **Purpose:**  
  Safe public memory, project index, accepted decisions, active project status, and cross-agent coordination. Use it as the **baseline** for what is publicly agreed and routable.

- **Not allowed in this repo:**  
  Secrets, tokens, credentials, private sensitive details, uncontrolled local machine specifics, or **unapproved** private repository contents. If something belongs in private memory, stop and ask for a **safe summary** or work in the private repo only when Abu Muhammad explicitly requests it.

## Required Reading Order

Codex Desktop must begin any project or session by reading, in order:

1. `00_MASTER_MEMORY_INDEX.md`
2. `01_GLOBAL_RULES.md`
3. `04_ACTIVE_PROJECTS.md`
4. The **relevant project file only**, for example:  
   `projects/LABIB.md`

For Labib-related work, Codex Desktop must also read any **clearly referenced** Labib documentation file (for example operator-facing docs under `projects/`) **if and only if** the task requires that content.

Codex Desktop must **not** read the entire repository unless Abu Muhammad explicitly requests it or a narrow technical necessity is documented (e.g., a single additional file path given in the task).

## Agent Roles

### ChatGPT

- Lightweight reasoning assistant.
- Maintains high-level memory index usage and helps Abu Muhammad decide next steps.
- Prepares prompts and plans for Cursor, Codex, Claude, and other tools.
- Does **not** silently assume hidden local changes; ground statements in public memory or explicit user input.

### Cursor

- Memory custodian and primary IDE-visible **code executor**.
- Performs scoped edits and implementation.
- Writes the **mandatory** audit report after every execution batch (workspace path below).
- Must not exceed scope; must not commit or push unless explicitly allowed.

### Claude

- Technical advisor when used.
- Helps with architecture, review, and reasoning.
- Must follow the same **accepted memory baseline** when given access to it.

### Codex Desktop

- Coding and implementation assistant (terminal/desktop context).
- Must follow repository memory, accepted baselines, and scoped execution rules in `01_GLOBAL_RULES.md` and this file.
- Must **not** work from stale assumptions when the public memory repo is available—**read the required order** first.
- Must **produce or respect** the same audit/reporting workflow when executing tasks (see **Audit Report Requirement**).
- Must **not** bypass Cursor/ChatGPT workflow decisions unless Abu Muhammad explicitly instructs otherwise.

## Core Operating Rules for Codex Desktop

- Always start from the **public memory baseline** when working on Abu Muhammad’s projects.
- Do **not** re-check or re-litigate **accepted completed** stages unless there is a **new concrete failure signal** (or an explicit user request).
- Treat accepted validation results as **baseline**; avoid verification loops.
- Do **not** modify files outside the requested scope.
- Do **not** create new project names, tool names, file names, or architectural labels without **explicit approval** (see naming rules in `01_GLOBAL_RULES.md`).
- Do **not** introduce new subsystems unless explicitly requested.
- Do **not** delete, move, or restructure files unless explicitly requested.
- Do **not** use the internet/network unless the task requires it **and** Abu Muhammad allows it.
- Do **not** access private repositories unless explicitly requested.
- Do **not** commit or push unless **Abu Muhammad explicitly authorizes commit/push in the current task/prompt**—see **Controlled GitHub Write Access** below. Default remains **no** commit/push.
- If blocked, **stop** and report **`BLOCKED:`** with a clear reason.

## Controlled GitHub Write Access

This is **controlled delegated GitHub write access**, not permanent uncontrolled autonomy.

- Codex Desktop may **commit** and **push** only when **explicitly authorized in the current task**.
- Authorization must be written **clearly** in the user / Cursor / ChatGPT prompt for that run.
- Codex must **not** assume that previous authorization applies to **future** tasks.
- Codex must **not** push automatically just because files changed.
- Codex must **not** commit or push **`What_I_Have_Done.md`**.
- Codex must **not** commit or push private, secret, token, credential, or sensitive files.
- If commit/push **is** authorized, Codex must use a **guarded** flow:
  1. Confirm repository path.
  2. Confirm git remote URL.
  3. Confirm current branch.
  4. Run `git status --short`.
  5. Confirm changed files are **only** the allowed files (per that prompt’s scope).
  6. Stage **only** explicitly allowed files.
  7. Commit with the **requested or approved** commit message.
  8. Push **only** to the requested branch.
  9. Fetch after push.
  10. Compare local `HEAD` with the remote branch.
  11. Print **`PUSH_VERIFIED`** only if local and remote match.
  12. Write the execution report to **`D:\MyPrograming\What_I_Have_Done.md`**.
- If **any** condition fails, Codex must stop with **`BLOCKED:`** and explain why.

## Audit Report Requirement

Abu Muhammad’s workflow requires an execution report after work runs.

**Report path (exact):**  
`D:\MyPrograming\What_I_Have_Done.md`

Rules:

- Workspace-level **temporary** audit report.
- May be **overwritten** every run (overwrite-only unless Abu Muhammad defines another scheme).
- Must **not** be created inside repository roots unless explicitly requested.
- Must **not** be committed or pushed.
- Should document, when applicable:
  - Commands executed  
  - Files created  
  - Files modified  
  - Files deleted  
  - Folders created  
  - Files copied or moved  
  - Files read or inspected  
  - Searches or queries performed  
  - Git status before and after  
  - Commits created  
  - Push result and verification  
  - External/network/repository access  
  - Blocked actions and reasons  
  - Deviations from scope  
  - Final status  

## Labib-Specific Notes

- Labib is an **active** project in public memory; treat `projects/LABIB.md` as the high-level source of truth for public-safe Labib status.
- Do **not** touch Labib **Core** or **Router** without explicit approval.
- **Track 06** is accepted as completed (Safe Command Bridge scope as documented in public memory).
- **Track 07** is accepted as completed; do **not** reopen accepted validation history without a **new concrete failure** signal.
- Telegram command work must stay within the accepted **Safe Command Bridge** approach (mapping to existing router behavior only—no silent expansion).
- No new **alias engine** or **status subsystem** unless explicitly approved.
- **Operator Manual** and **Final Freeze Documentation** are documentation/freeze milestones in public memory—not an invitation to redesign runtime architecture in this repo without an approved track.

## How Codex Should Respond When Given a Task

1. Identify the **repository** and **files in scope** from the user prompt and memory routing.  
2. Read the **required memory files** (order above).  
3. State assumptions **only** when grounded in those files or explicit user instructions.  
4. Execute **only** the requested scope.  
5. Prefer **guarded** shell/Git operations when side effects exist.  
6. Report clearly if **BLOCKED**; never claim success without evidence (commands run, files changed, checks passed).  

## Final Reminder

Codex Desktop must preserve **continuity between agents**. The public memory repo exists so ChatGPT, Cursor, Claude, Codex, and Abu Muhammad do not lose project context or repeat settled decisions—while keeping **private** and **sensitive** material out of the public layer.
