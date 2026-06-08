# Memory Maintenance Policy

Last updated: 2026-06-08
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
- Suggested blocked status label for this case: `BLOCKED_REMOTE_MISMATCH`.

## Weekly cleanup process
- Refresh public project summaries.
- Remove duplicate or stale high-level wording.
- Confirm safe boundary is still preserved.

## Monthly review process
- Review overall public memory clarity and routing quality.
- Re-validate safety posture for direct ChatGPT reading.

## ChatGPT / Abu Saleh — three lightweight memory anchors (mandatory)

Owner decision (2026-06-01): **ChatGPT memory stays lightweight.** Keep **only** these three anchors:

| # | Anchor | Content |
|---|--------|---------|
| **1** | **External-first principle** | Operational rules, agent rules, project details, workflows, and durable decisions must **not** live mainly in ChatGPT memory. They belong in the **external memory repository** and/or durable **_KnowledgeWiki** references. |
| **2** | **Public memory repo URL** | `https://github.com/Alodhaibee/abu-muhammad-memory-public` |
| **3** | **Self-reminder / anti-bloat rule** | For rules, agents, Cursor, GitHub, KnowledgeWiki, projects, workflows, or memory topics: **start from** this public repo and **`00_MASTER_MEMORY_INDEX.md`**, not from long internal ChatGPT memory. If ChatGPT memory holds durable details beyond these three anchors, route them through Cursor/KnowledgeWiki/GitHub, **verify** external anchoring/publish, then **remove** redundant details from ChatGPT memory. |

**Anchor count (Abu Saleh):** Target **3** active operational anchors; temporary **max 5** only when truly necessary — compact rule in **`AS_REF.md`**.

**Durable operational details belong in external files — not ChatGPT memory.**

### When new durable information appears in ChatGPT memory

1. **Route** it to Cursor / KnowledgeWiki / GitHub at the nearest appropriate opportunity.
2. **Verify** it is saved or published externally (public-safe content only in this repo).
3. **Remove** or request removal from ChatGPT memory after external anchoring is confirmed.

### Public vs private boundary (mandatory)

- Do **not** store sensitive, private, or client-specific details in this public repo.
- Public repo content must be **public-safe** only.
- Private/local details belong in **_KnowledgeWiki** (local operational), private memory, or local project files — **not** here.
- Do **not** rename repository/folder path tokens (e.g. `abu-muhammad-memory-public`) under this policy — separate oversight project.

### Memory categories that should NOT remain in ChatGPT memory

Export these to the correct external layer, then prune ChatGPT memory:

- Detailed Cursor audit reports and long session transcripts
- Commit hashes and push verification details (belong in git history / audit files)
- Telegram Mailman implementation details (belong in project files / KnowledgeWiki)
- Project-specific OWNER_SETTINGS and local config details
- Detailed workflow rules, Skill Bank bodies, and agent operating procedures
- Exact file lists from old sessions
- Long project histories and multi-session execution logs
- Old operational failures, cleanup details, and one-off debugging notes
- Project ideas that belong in KnowledgeWiki registers or `projects/*.md`
- Duplicate copies of rules already in this repo or _KnowledgeWiki
- Secrets, tokens, credentials, client data, or strategic private ideas
- **WiseMan / documentation governance session detail (2026-06-08)** — trials, closeout tables, open-items lists → `_KnowledgeWiki/governance/WiseMan.md`, `skills/wise-governance-review.md`, `standards/project-documentation-standard.md`; prune after `KnowledgeWiki-private` sync verified
- **HomeTalk benefit tables and cleanup prose (B1–B7)** → `_KnowledgeWiki/projects/hometalk.md` and linked guides
- **KnowledgeWiki sync commit hashes and staged-file inventories** → git history + `What_I_Have_Done/cursor.md` audit only
- **Cursor cloud vs Ollama capability matrices** → audit marker `LOCAL_OLLAMA_CURSOR_USAGE_CHECK_COMPLETE`; baseline in `_KnowledgeWiki/tools/owner-windows-ollama-claude-local-baseline.md`

## ChatGPT lightweight memory index policy

**Canonical:** See **three lightweight memory anchors** above. This section adds detail only.

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

## External-first operating boundary (public-safe)
- Detailed operating rules should be stored in external systems, not long-form ChatGPT memory.
- External sources of truth are:
  - local operational KnowledgeWiki
  - this public-safe memory repository (when suitable for public visibility)
- ChatGPT memory should stay pointer-only and lightweight:
  - "Use the external memory system / KnowledgeWiki / public memory repo as the operational source of truth."
- When a current external entrypoint/rule exists, do not rely on long detailed ChatGPT memory copies.
- Agents should start from the current external entrypoint/rules for routing and execution context.

## Primary Cursor startup rule (public-safe — 2026-06-03)

- **Canonical rule name:** **Start Here First — Cursor Working On + Prompt Guard + Skills Review**
- **Status:** Primary and top-priority startup/execution rule for Cursor (see **`docs/2026-06-03_primary_cursor_start_rule.md`**).
- **Controls:** first visible **`## Working on:`** table; mandatory startup file order (`AGENTS_PROTOCOL.md` → `shared.md` → `cursor.md`); **`AGENTS_START_HERE.md`** as router only after those files; **`prompt-style-drift-guard`** before scoped work; central audit **`D:\MyPrograming\What_I_Have_Done\cursor.md`** (full-file overwrite); final **`## 🧠 Skills Summary — Owner Review`** in chat after audit.
- **Governance:** do not bypass; do not add duplicate standalone rules for the same behavior — merge future changes into this rule and aligned local wiki files.

## Cursor audit continuity rule (public-safe summary)
- Cursor canonical audit path remains:
  - `D:\MyPrograming\What_I_Have_Done\cursor.md`
- Legacy/non-default path remains:
  - `D:\MyPrograming\What_I_Have_Done.md` (placeholder only unless explicitly requested)
- Audit/execution reporting is required for every Cursor action, including read-only checks and no-edit tasks.
- **Write method:** **full-file overwrite only** for `cursor.md` (one clean snapshot per run). **Append is forbidden** unless the owner explicitly requests append or history behavior for that run.
- If a prompt says **do not modify any file**, the operational exception is: do not modify any file **except** a **full-file overwrite** of the required audit report at `D:\MyPrograming\What_I_Have_Done\cursor.md` (per **`AGENTS_PROTOCOL.md`** and KnowledgeWiki **`agents/shared.md`**).
- Full Cursor audit sections (token routing, **`## 🧠 Skills Summary — Owner Review`**, etc.): KnowledgeWiki **`agents/cursor.md`** and **`agents/shared.md`**.

## ChatGPT memory pruning against external memory
- When information is already captured in this public memory repository or another approved external memory layer, ChatGPT should not keep long duplicated details in its own memory.
- ChatGPT should retain only a lightweight pointer to the external source of truth.
- If durable information is missing from external memory, record it first in the appropriate external layer, then reduce ChatGPT memory back to lightweight baseline.

## Black Box / Agent Evidence Trail (public-safe)
- For Abu Muhammad's agent workflows, "Black Box" means a reviewable evidence trail of agent work.
- Typical evidence includes: files read, files changed, decisions made, blocked items, audit reports, and push verification.
- This trail supports continuity, accountability, and reconstruction of what happened.
- It is stored in external memory and audit files, not as long duplicated ChatGPT memory.
- Black Box records must not include secrets or sensitive content.
- The concept also covers practical verification of whether an agent worked or failed by reading the evidence/report it produced, including blockers and next-action context.
- Durable useful operating lessons should be externalized to the appropriate memory layer; public-safe lessons may be added to public memory.

## Permanent memory compliance rule
- For Abu Muhammad's operational work, ChatGPT and agents should treat external memory as the source of truth for projects, agents, memory rules, GitHub/KnowledgeWiki operations, audits, skills, and operating policies.
- ChatGPT memory should remain lightweight and pointer-level.
- Before judging durable operational topics, assistants should rely on the public memory repository and/or approved KnowledgeWiki entrypoints rather than long internal memory.
- If useful durable information is missing from external memory, record it in the appropriate external layer first.
- Public-safe and broadly useful lessons may be added to public memory.

## Prompt discipline rule
- For Abu Muhammad's agent workflows, prompts should not repeat long safety/checklist blocks by default.
- Normal prompts should be short and route agents through approved external entrypoint/rules.
- **Do not re-teach** installed protocol in normal task prompts (Working on, audit, rollback, skills rules) unless the task creates/changes/tests protocol — see **`AS_REF.md`** and KnowledgeWiki **`agents/shared.md`** (Compact session prompts).
- Sensitive prompts may add only relevant controls.
- Full checklist prompts should be reserved for new operating rules, public memory updates, high-risk changes, first-time workflow establishment, or suspected drift/noncompliance.

## Session finality check (public-safe)
- Agents must **not** claim **PASS**, **COMPLETE**, or that a session can **close cleanly** while **unresolved items** remain for the stated goal.
- Use **PARTIAL**, **NEEDS_REVIEW**, or **BLOCKED** and list open items unless Abu Muhammad explicitly accepts them in the current thread.
- Pair with local **workflow-audit** skill and **evidence-before-completion** rules in KnowledgeWiki `agents/shared.md`.

## Repeatable prompt patterns → skills (public-safe)
- Repeated long prompt blocks (Mode, startup paths, safety checklists) should become **compact session wrappers** or **Skill Bank** skills — not re-pasted every session.
- Local skills: **compact-session-prompt**, **skill-authoring**, **skill-opportunity-review** (KnowledgeWiki `skills/` — bodies local only).
- **Prompt discipline** and **compact prompts** are operational rules in KnowledgeWiki `AGENTS_START_HERE.md` and `agents/shared.md`.

## Skill Bank governance — anti-bloat (public-safe, 2026-05-29)
- **Before** a new skill or global rule: verify an existing Skill Bank skill or shared operating rule does not already cover the pattern (**skill-discovery** first).
- **Prefer:** improve an existing skill, anchor in **`agents/shared.md`**, or use a template/tool — **not** a duplicate `skills/*.md` file.
- **Lifecycle (names only, local bodies):** **skill-discovery** → **skill-opportunity-review** (when a pattern repeats) → **skill-authoring** (only after review + owner approval). Also route long-running work via **project-continuity-plan** and end sessions with **workflow-audit**.
- **ChatGPT / Abu Saleh** should remind the owner when an idea belongs in these mechanisms instead of a new parallel rule.
- **Not** for one-time ideas or session excitement. See **`01_GLOBAL_RULES.md`** (Skill Bank governance).

## Owner-facing Arabic editorial policy (public-safe)
- **Abu Saleh** owns **editorial Arabic wording** for owner-facing Skill Bank catalog and similar summaries.
- Agents (including Cursor) may **apply** Arabic text supplied in an approved session; they must **not invent** literal Arabic translations for owner-facing titles or explanations without Abu Saleh review.
- English skill filenames remain the agent execution source; Arabic catalog is for owner navigation (`skills/_00_SKILLS_CATALOG.ar.md` — local).

## Agent-neutral pattern adoption (public-safe)
- Useful agent behaviors — including patterns observed from **Cursor Superpowers** or other tools — may be **distilled** into **agent-neutral** Skill Bank skills or shared operating rules when they improve results across agents.
- Do **not** copy proprietary plugin formats, hook names, or tool-specific packaging verbatim into Skill Bank.
- Tool-specific execution stays in per-agent operating files; Skill Bank stays agent-neutral.

## Skill Bank — personal monitoring and compact prompts (public-safe, 2026-05-29)
- **personal-monitoring:** Owner-visible **rendered pre-action table** before meaningful steps; levels **light / normal / strict / approval-gated**; **`strict`** recommended default in compact prompts (continue after table unless sensitive); **`approval-gated`** for Git/secrets/live/delete/publish. Full skill local only.
- **compact-session-prompt:** Short prompts with `Use standard KnowledgeWiki startup` instead of repeating boilerplate; pairs with personal-monitoring when `Monitoring:` is set. Full skill local only.
- **Registry:** KnowledgeWiki `skills/README.md` is the live list; public memory records names and purpose only — not full skill bodies.

## Memory publish verification (public-safe, 2026-05-29)
- Do **not** describe public memory as **published on GitHub** unless **commit + push + verify** (`git fetch`; local `HEAD` = `origin/master` on the correct repo).
- **Three layers** agents must not confuse: **LOCAL_UPDATED** (disk only) · **READY_NOT_PUSHED** (prepared or committed locally, not verified on GitHub) · **PUBLISHED_AND_VERIFIED** (push verified).
- Local edits under `abu-muhammad-memory-public` alone are **not** publish. Full procedures: KnowledgeWiki `skills/memory-update-safe.md`, `skills/github-safe-publish.md`, `skills/workflow-audit.md` (local only).
