# Memory Maintenance Policy

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

## Weekly cleanup process
- Refresh public project summaries.
- Remove duplicate or stale high-level wording.
- Confirm safe boundary is still preserved.

## Monthly review process
- Review overall public memory clarity and routing quality.
- Re-validate safety posture for direct ChatGPT reading.
