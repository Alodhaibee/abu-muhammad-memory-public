# Agents Protocol

Protocol-Version: 2026-05-12.1  
Status: Active  
Owner: Abu Muhammad  
Repository: https://github.com/Alodhaibee/abu-muhammad-memory-public

## Purpose

- This file is the **central operating protocol** for Abu Muhammad’s AI agents and tools.
- It exists so **ChatGPT**, **Cursor**, **Codex Desktop**, **Claude**, **Antigravity**, and **future agents** share the same **memory baseline** and **workflow rules** without relying on fragile, repeated long instructions in every prompt.
- **If any agent’s local understanding conflicts with this file, this file wins.**
- Any agent that **does not read** this protocol **must not execute** project changes (stop with **BLOCKED** or ask for a read scope that includes this file).

## Required Startup Rule

Every agent must start project work by reading:

1. **`AGENTS_PROTOCOL.md`** (this file)
2. **`00_MASTER_MEMORY_INDEX.md`**
3. **`01_GLOBAL_RULES.md`**
4. **`04_ACTIVE_PROJECTS.md`**
5. The **relevant project file only**, for example:  
   `projects/LABIB.md`

**Tool-specific instructions (additional reads):**

- **Codex Desktop** must also read **`CODEX_DESKTOP_INSTRUCTIONS.md`**.
- Future tool-specific instruction files may be added and referenced from this protocol.

Agents must **not** read the entire repository unless explicitly requested or technically necessary.

## Tool-Local Startup Instructions

- Each supported tool or agent should store a **permanent local** startup or settings instruction when the tool supports it.
- The startup instruction should tell the tool to **read and follow**:  
  `D:\MyPrograming\abu-muhammad-memory-public\AGENTS_PROTOCOL.md`
- This reduces repeated long prompts and keeps all agents aligned to **one central protocol**.
- Tool-local instructions must remain **short** and must **not** duplicate the full protocol.
- If tool-local instructions conflict with **`AGENTS_PROTOCOL.md`**, **`AGENTS_PROTOCOL.md` wins**.
- Tool-local instructions do **not** grant commit/push permission.
- Commit/push still requires **explicit current-prompt authorization**.
- Each agent must still write **only** to its **assigned audit report file** (see **Audit Report System**).

## Protocol Version Rule

Every execution report must include:

- **Protocol version** read (e.g. `2026-05-11.1`).
- **Whether the protocol was read successfully** (Yes/No).
- If the agent **cannot** read the current protocol, it must **stop** with **BLOCKED**.
- If the **task instructions conflict** with this protocol, the agent must **stop** and **report the conflict** unless Abu Muhammad **explicitly overrides** the protocol for that run.

## Agent Roles

### ChatGPT

- Lightweight reasoning assistant and memory index.
- Helps Abu Muhammad decide next steps.
- Prepares **scoped** prompts for Cursor, Codex Desktop, Claude, Antigravity, and other tools.
- Does **not** silently assume local file changes.
- Reviews audit reports from agents.

### Cursor

- Memory custodian and scoped **code/document** executor.
- Performs controlled edits and implementation.
- Must produce an **audit report** after every run (see **Audit Report System**).
- Must not exceed scope.
- Must not commit or push unless explicitly authorized.

### Codex Desktop

- Coding and implementation assistant.
- Must follow public memory, accepted baselines, and scoped execution rules.
- May commit/push **only** when explicitly authorized **in the current prompt**.
- Must use **guarded** and **verified** Git flow when push is allowed.

### Claude

- Technical advisor.
- Helps with architecture, review, reasoning, and technical critique.
- Must follow the same memory baseline when given access.
- Must **not** create competing project truth outside this memory protocol.

### Antigravity

- Implementation / build / design assistant when used.
- Must follow this protocol before working on Abu Muhammad’s projects.
- Must **not** assume it can rename, restructure, redesign, deploy, or publish unless explicitly authorized.
- Must write **only** to its own audit report file.
- Must **not** override decisions already accepted in public memory.

### Future Agents

- Any future agent must be **added to this protocol** (roles + audit path) before being trusted with project execution.
- Future agents must receive their **own** audit report file path under `D:\MyPrograming\What_I_Have_Done\`.

## Public Memory Repository

- **Repository URL:**  
  https://github.com/Alodhaibee/abu-muhammad-memory-public

- **Purpose:**  
  Safe public memory, project index, accepted decisions, active project status, and cross-agent coordination.

- **Not allowed:**  
  Secrets, tokens, credentials, private sensitive details, uncontrolled local machine details, or unapproved private repository contents.

## Baseline and Verification Rules

- Do **not** re-check accepted baselines unless there is a **new concrete failure signal**.
- Treat accepted validation results as **baseline**.
- Do **not** enter verification loops.
- If a new failure appears, investigate from the **new failure signal only**.
- Do **not** re-open old stages just because of uncertainty.
- Do **not** modify **Core**, **Router**, or **frozen** project areas without explicit approval.

## Naming and Structure Rules

- Do **not** create new project names, folder names, tool names, file names, or architectural labels without Abu Muhammad’s approval.
- Do **not** introduce new subsystems unless explicitly requested.
- Do **not** delete, move, or restructure files unless explicitly requested.
- If naming is required, **propose** names and wait for approval unless the name was **already approved**.

## Git and GitHub Rules

- **No** agent may commit or push unless **explicitly authorized in the current prompt**.
- **Previous authorization does not carry forward.**
- Any push must be **guarded**, **conditional**, and **verified** after push.

**Guarded push checklist:**

1. Confirm repository path.  
2. Confirm remote URL.  
3. Confirm current branch.  
4. Run `git status --short`.  
5. Confirm changed files are **only** approved files.  
6. Stage **only** approved files.  
7. Commit with **approved** message.  
8. Push **only** to approved branch.  
9. Fetch after push.  
10. Compare local `HEAD` with remote branch.  
11. Print **`PUSH_VERIFIED`** only if local and remote match.  

- If **any** condition fails, stop with **BLOCKED**.  
- **Never** commit/push audit reports unless explicitly requested.  
- **Never** commit/push secrets, credentials, tokens, private repo contents, or files outside approved scope.

## Audit Report System

**Official audit folder:**  
`D:\MyPrograming\What_I_Have_Done\`

Each agent must write **only** to its own file:

| Agent / tool | Audit file |
|--------------|------------|
| **Cursor** | `D:\MyPrograming\What_I_Have_Done\cursor.md` |
| **Codex Desktop** | `D:\MyPrograming\What_I_Have_Done\codex.md` |
| **Claude** | `D:\MyPrograming\What_I_Have_Done\claude.md` |
| **Antigravity** | `D:\MyPrograming\What_I_Have_Done\antigravity.md` |
| **ChatGPT handoff** | `D:\MyPrograming\What_I_Have_Done\chatgpt_handoff.md` |

**Rules:**

- Each agent must write its report as a **full-file overwrite** on **every** run (replace the entire file contents in **one** write operation).  
- **Append** mode is **forbidden** for audit reports.  
- **Partial** overwrites that leave **old tail content** from a previous version are **forbidden**.  
- **Stale** content from previous runs must **not** remain in an agent’s report file.  
- **No** agent may **inspect**, **modify**, **delete**, **rename**, or **overwrite** **another** agent’s report file unless Abu Muhammad **explicitly authorizes** that access for the path and run.  
- **No** agent may delete and recreate the audit **folder**.  
- Audit files are **local temporary** reports.  
- Audit files must **not** be committed or pushed unless **explicitly requested**.  
- The old single file **`D:\MyPrograming\What_I_Have_Done.md`** is **legacy** and must **not** be used for **new** agent reports.  
- **Integrity recovery:** If an agent detects **stale** content, **duplicated** report blocks/sections, or **more than one** `Final status:` line in **its own** report file, it must **fully rewrite** its own report file as a **clean** snapshot **before** finishing the task.

**Final status line (mandatory format):**

- Every report must include **exactly one** line of the form `Final status: <VALUE>` (no duplicate `Final status:` lines).  
- That `Final status:` line must be the **last non-empty** line in the file (no report body after it).

**Every report must include:**

- **Report timestamp** with **timezone** (when the report was written)  
- Agent/tool name  
- Protocol version read  
- Execution mode: **READ_ONLY**, **DOC_EDIT**, **CODE_EDIT**, **COMMIT_PUSH**, **DESIGN_EDIT**, **BLOCKED**, or **ERROR**  
- Scope  
- Commands executed  
- Files created  
- Files modified  
- Files deleted  
- Folders created  
- Files copied or moved  
- Files read or inspected  
- Searches or queries performed  
- Git status before and after  
- Staged files (if git was used)  
- Commit hash (if created)  
- Push result and verification (if push was allowed)  
- External/network/repository access  
- Blocked actions and reasons  
- Deviations from scope  
- **Final status** (the single mandatory `Final status:` line is defined under **Final status line** above)  

## Network and External Access Rules

- Do **not** use internet/network unless the task requires it **and** the user allows it.  
- If external access is used, report the **exact reason** and **target**.  
- **Private repositories** must not be accessed unless explicitly authorized.

## Labib-Specific Baseline

- Labib is an **active** project.  
- **Track 06** is accepted as completed.  
- **Track 07** is accepted as completed.  
- Accepted validation results must **not** be rechecked without a **new concrete failure**.  
- Telegram command work must stay within the accepted **Safe Command Bridge** approach.  
- **No** new alias engine or status subsystem unless explicitly approved.  
- **Operator Manual** and **Final Freeze** are documentation/freeze phases—not an invitation to redesign.  
- Do **not** touch Labib **Core** or **Router** without explicit approval.

## What To Do When Instructions Conflict

- If the **user prompt** conflicts with **`AGENTS_PROTOCOL.md`**, stop and report the conflict unless Abu Muhammad **explicitly overrides** the protocol.  
- If repository **files** conflict with memory/context, the **current repository memory files** win.  
- If a task is **ambiguous** and could modify persistent structure, **ask for approval** before naming or restructuring.

## Minimal Prompt Pattern for Future Agents

Use this pattern when delegating work:

```text
Read and follow:
D:\MyPrograming\abu-muhammad-memory-public\AGENTS_PROTOCOL.md

Then perform this task:
[task]

Write your audit report only to your assigned file.
Do not commit or push unless explicitly authorized.
```
