# Global Rules (Public Safe)

## Work approach
- Focus on practical execution.
- Keep work phased and organized.
- Reduce confusion with clear outputs.
- Prefer documented decisions.
- Avoid unnecessary questions when context is clear.

## Communication
- Use concise, operational wording.
- Clarify assumptions when needed.
- Keep final outputs easy to review.

## External memory model (public-safe)
- ChatGPT uses lightweight memory and reads this repository as safe index context.
- Cursor maintains the private repository as full long-term memory source.
- If details are sensitive or uncertain, keep them private and do not publish them here.

## Accepted Baseline and Conditional Execution Rules

1. Accepted Baseline Rule
When a project stage, track, commit, or verification result has already been approved and accepted by Abu Muhammad, treat it as the working baseline.
Do not re-check, re-litigate, or reopen previous stages unless there is a new concrete signal such as:
- an actual failure,
- a conflicting file,
- a missing file,
- a changed environment,
- a dirty working tree,
- or Abu Muhammad explicitly asks for verification.

2. No Verification Loops
Verification should protect progress, not consume the working session.
Avoid repeated "verify the verification" workflows.
Use one focused check only when necessary.

3. One Primary Documentation File During Active Work
During active stage work, document in one primary file first.
For Labib, the default active documentation file is:
projects/labib/ACTIVE_CONTEXT.md

Only modify other files when clearly needed:
- TRACKS.md only when a track status changes.
- DECISIONS.md only when a formal decision is approved.
- NEXT_ACTIONS.md only when the next action plan changes.
- projects/LABIB.md only for public-safe summary updates.
- CHANGELOG.md only for public-facing release/history updates.

4. Private vs Public Memory Repositories
Keep a clear distinction between:
- abu-muhammad-memory: private/local memory repository.
- abu-muhammad-memory-public: public-safe GitHub memory repository.

Do not add a GitHub remote to the private repository unless Abu Muhammad explicitly approves it.
Do not push private memory content to GitHub by default.
Public-safe updates should be made only in abu-muhammad-memory-public.

5. Conditional Push and Verify Rule
Any GitHub push prompt must use guarded conditional logic:
- verify the target repository path,
- verify it is a git repository,
- verify the expected remote exists,
- verify the working tree has only the expected changed files,
- commit only the intended files,
- push only after all prechecks pass,
- fetch after push,
- compare local HEAD with origin/current-branch,
- stop with a clear BLOCKED reason if any precondition fails.

Never use unguarded push commands when a guarded one-liner or guarded script can validate, push, and verify in one flow.

6. Stop on BLOCKED
If any prerequisite is missing, stop immediately and print a clear BLOCKED reason.
Do not continue with partial push, remote changes, sync, or extra fixes.

## Codex — officially adopted executor (summary)
- **Codex** is an **official, bounded terminal executor** in the workflow system (CLI installed, exercised, and governed).
- Authoritative **local** rules + skills: **`D:\MyPrograming\CodexSkills`**.
- **Private** GitHub mirror for the skill pack: **`https://github.com/Alodhaibee/CodexSkills`** (details + approved operating rules in **`projects/CODEX_SKILLS.md`**).
- Codex must follow the same **overwrite-only** workspace report rule as other executors (`What_I_Have_Done.md`), and must **not** delete/move/rename, commit/push, use network, or install packages **without explicit instruction**.
- **“أبو محمد”** as vocative only; **`AbuMuhammad`** not a default prefix for new neutral artifacts (see naming rules below).

## Naming approval (durable artifacts)
- Before naming any **new** durable folder, project, tool, skill, or important file, obtain **explicit user approval** for the chosen name.
- **Exception:** names **derived directly** from an already-approved name **without changing meaning** may be reused without re-asking.
- Do **not** use **`AbuMuhammad`** as a **default prefix** for neutral tools or skills; prefer clean names such as **CodexSkills**, **Codex Workflow**, **Project Control Center**.

## Workspace execution report (`What_I_Have_Done.md`)
- After each batch of work, executors (**Cursor**, **Claude Code**, **Codex**, and similar) must write an audit report at **`D:\MyPrograming\What_I_Have_Done.md`** (workspace-level, **outside** this public repo unless explicitly requested otherwise).
- **Overwrite** the file each run so it reflects **only the latest operation** (**never append by default**), unless the user explicitly defines a different reporting scheme.
- Do **not** create `What_I_Have_Done.md` inside repository roots unless explicitly requested.
- Do **not** commit or push `What_I_Have_Done.md` unless explicitly requested.
- When applicable, the report should include: workspace path; goal; files inspected / created / modified / deleted; folders created or deleted; files copied or moved; commands executed; git status before/after; safety scan result; external/network access used (Yes/No); other projects touched (Yes/No); deviations; errors or blocked items; final status.
- Purpose: full traceability so ChatGPT and the user can verify what each executor did and catch mistakes or unauthorized actions.
