# Memory Maintenance Policy

Last updated: 2026-05-06
Status: Active

## Split model
- Private repository is maintained by Cursor as full memory context.
- Public repository is curated for ChatGPT direct reading.

## Public update policy
- Add only cleaned, reviewed summaries.
- Keep detailed operational notes private.
- Update public files only after safety review.
- Treat public GitHub as reading memory, not operational storage.

## Memory update command (public-safe)
- When Abu Muhammad says `حدث الذاكرة` (or similar), ChatGPT keeps memory lightweight while Cursor maintains full long-term memory in the private repository.
- Update this public repository only with safety-reviewed content suitable for direct reading.
- Public reference repository URL:
  - `https://github.com/Alodhaibee/abu-muhammad-memory-public`
- **Do not** treat memory as updated on GitHub until push is verified on the correct repo; local changes alone are insufficient.
- After an authorized push, confirm `HEAD` matches `origin` on the target branch before reporting success.
- Use selective staging when unrelated local files exist; state outcome as **local only**, **commit only**, or **pushed (verified)**.

## Daily usage workflow (public-safe)
1. Read `00_MASTER_MEMORY_INDEX.md` first.
2. Read only the relevant project file for the active task.
3. Keep ChatGPT internal memory minimal and task-focused.
4. Use this repository as safe context only.

## Public/private update rules
- Cursor updates private repository with complete long-term memory.
- Public repository is updated only with sanitized summaries.
- No sensitive operational details are allowed here.

## Safety scan rule before public commits
- Run safety scan checks before public commits.
- Do not commit if risky sensitive values are detected.

## GitHub safe publish workflow (public updates)
- For commit/push operations, use the `github-safe-publish` workflow from the local Skill Bank.
- Do not proceed when unexplained or unrelated working-tree changes exist; stop and request Abu Muhammad's decision first.
- After push/fetch verification, local `HEAD` must match `origin/<branch>` before reporting success.
- If remote verification is uncertain or mismatched, treat the run as blocked.

## Weekly cleanup process
- Refresh public project summaries.
- Remove duplicate or stale high-level wording.
- Confirm safe boundary is still preserved.

## Monthly review process
- Review overall public memory clarity and routing quality.
- Re-validate safety posture for direct ChatGPT reading.

## ChatGPT lightweight memory index policy
- Main ChatGPT context source is this public memory repository:
  - `https://github.com/Alodhaibee/abu-muhammad-memory-public`
- ChatGPT internal memory must remain a lightweight index only.
- Do not store long session reports, expired reminders, temporary decisions, or detailed project histories in ChatGPT memory.
- When context is needed, read public GitHub memory entrypoints first, then use local KnowledgeWiki/private reports only when provided or needed.
- Canonical Cursor audit path:
  - `D:\MyPrograming\What_I_Have_Done\cursor.md`
- Legacy/non-default audit path:
  - `D:\MyPrograming\What_I_Have_Done.md` (placeholder only; not default)
- No commit or push in memory workflows unless explicitly approved in the current session.
- Skill Bank remains agent-neutral (not Cursor-specific).
- Protect private or strategic ideas before publishing public memory updates.
- Mobile reminders (for example: "remind me when I reach the computer") are temporary holding notes only; once externally recorded and evidenced, they should not stay duplicated in ChatGPT memory.
