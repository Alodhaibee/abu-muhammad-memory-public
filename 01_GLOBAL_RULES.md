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
- ChatGPT / Abu Saleh memory keeps **only three lightweight anchors** — see **`06_MEMORY_MAINTENANCE_POLICY.md`** (**three lightweight memory anchors**).
- ChatGPT reads this repository as safe index context; Cursor maintains private/full memory locally.
- If details are sensitive or uncertain, keep them private and do not publish them here.

### _KnowledgeWiki (local — not public)
- Do **not** publish **_KnowledgeWiki** contents publicly. Only **public-safe summaries** may be added to this repository.
- **Private/strategic ideas**, **raw/inbox** contents, **evidence**, **scripts**, **configs**, **credentials**, **local paths**, and **sensitive project internals** remain **local/private**.

## Central agents protocol (mandatory)

- **`AGENTS_PROTOCOL.md`** (repository root of **`abu-muhammad-memory-public`**) is the **single official** operating protocol for all AI agents/tools in this workflow.
- **Every agent** must **read it before executing project changes** and must **report the protocol version** read in its own per-agent audit file (see **`AGENTS_PROTOCOL.md`** and **Workspace execution reports** below).
- Per-agent audit reports live only under **`D:\MyPrograming\What_I_Have_Done\`**. The legacy single file **`D:\MyPrograming\What_I_Have_Done.md`** must **not** be used for **new** agent reports.
- **Commit/push** remains **explicitly authorized in the current prompt only**, must be **guarded** and **verified** when allowed, and is further specified in **`AGENTS_PROTOCOL.md`**.

### Tool-local startup pointers (optional but recommended)

- Agents and tools should use **permanent local** startup or settings instructions **where the tool supports them**, pointing first to **`AGENTS_PROTOCOL.md`** (see **`AGENTS_PROTOCOL.md`** — **Tool-Local Startup Instructions**).
- Those local settings are **only pointers** to the central protocol, **not** replacements for reading it.
- **`AGENTS_PROTOCOL.md`** remains the **source of truth**.
- Local startup settings do **not** authorize commit/push or **expanded scope** beyond what the current prompt and protocol allow.

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
- Codex must follow the same **per-agent overwrite-only** workspace audit rule as other executors (see **Workspace execution reports** below), and must **not** delete/move/rename, commit/push, use network, or install packages **without explicit instruction**.
- **“أبو محمد”** as vocative only; **`AbuMuhammad`** not a default prefix for new neutral artifacts (see naming rules below).

## Codex Desktop — public memory integration (mandatory)

- **Codex Desktop** must follow **`CODEX_DESKTOP_INSTRUCTIONS.md`** (repository root of **`abu-muhammad-memory-public`**) when working on Abu Muhammad’s projects so its behavior matches the shared-memory workflow.
- Codex Desktop must use this **public memory repo** as the **safe shared baseline** for routing, accepted stages, and coordination with ChatGPT, Cursor, and Claude—**not** for secrets or unapproved private content.
- Codex Desktop must respect the **workspace-level** audit rule: write only to **`D:\MyPrograming\What_I_Have_Done\codex.md`** per **`CODEX_DESKTOP_INSTRUCTIONS.md`** and the **Workspace execution reports** section below.

**Controlled delegated GitHub write:** Codex Desktop has controlled delegated GitHub write access **only** when Abu Muhammad **explicitly authorizes commit/push in the current prompt**. Any Codex commit/push must be **scoped**, **guarded**, **verified after push**, and **documented** in **`D:\MyPrograming\What_I_Have_Done\codex.md`** (Codex’s own audit file). Codex must **never** commit/push audit reports (including any file under `What_I_Have_Done\`), secrets, credentials, private repository contents, or files outside the approved scope.

## Naming approval (durable artifacts)
- Before naming any **new** durable folder, project, tool, skill, or important file, obtain **explicit user approval** for the chosen name.
- **Exception:** names **derived directly** from an already-approved name **without changing meaning** may be reused without re-asking.
- Do **not** use **`AbuMuhammad`** as a **default prefix** for neutral tools or skills; prefer clean names such as **CodexSkills**, **Codex Workflow**, **Project Control Center**.

## Owner-Name Privacy Rule (mandatory)

Owner decision (2026-06-01). Full protocol: **`AGENTS_PROTOCOL.md`** — **Owner-Name Privacy Rule**.

| Context | Rule |
|---------|------|
| **Private chat** | Owner's chosen personal label/name is **allowed** (including conversation with Abu Saleh). |
| **Recorded / transferable content** | Do **not** use the personal name/label in program files, docs, configs, templates, code comments, reports, operational wiki files, or client-transferable content — **unless** the owner explicitly requests it for that specific file/purpose. |
| **Default labels** | **owner**, **program owner**, **authorized owner**; **المالك**, **مالك البرنامج**, **المالك المصرّح** |
| **Violations** | Privacy/portability **defects** — fix when editing; no bulk historical rewrites |
| **Path tokens** | Do **not** rename repos/folders (e.g. `abu-muhammad-memory-public`) under this rule — separate oversight project |

**Related (existing):** vocative **"أبو محمد"** in live chat only; **`AbuMuhammad`** not a default prefix for neutral artifacts (Codex summary above).

## Workspace execution reports (`What_I_Have_Done/`)

Official audit layout (workspace-level, **outside** this public repo unless Abu Muhammad requests otherwise):

| Agent / role | Audit file (write **only** this file for that agent) |
|--------------|--------------------------------------------------------|
| **Cursor** | `D:\MyPrograming\What_I_Have_Done\cursor.md` |
| **Codex Desktop** (and terminal Codex when used as that executor) | `D:\MyPrograming\What_I_Have_Done\codex.md` |
| **Claude** | `D:\MyPrograming\What_I_Have_Done\claude.md` |
| **Antigravity** | `D:\MyPrograming\What_I_Have_Done\antigravity.md` |
| **ChatGPT handoff** (when represented locally) | `D:\MyPrograming\What_I_Have_Done\chatgpt_handoff.md` |

**Safety rules (multi-agent):**

- Each agent writes **only** to its own file above.
- **No** agent may delete, overwrite, rename, or modify **another** agent’s report file.
- **No** agent may delete or recreate the **`D:\MyPrograming\What_I_Have_Done`** folder.
- Audit files are **local temporary** reports; **do not** commit or push them unless explicitly requested.
- Each agent may **overwrite only its own** file each run (**overwrite-only** for that file, **never append by default** unless Abu Muhammad defines another scheme).
- **Per-agent audit reports are snapshot reports, not append logs:** every run must **replace** that agent’s own report file **completely** (full-file overwrite). Append mode is forbidden; leaving stale tail content from a prior run is forbidden.
- Each report must include a **report timestamp with timezone** and **exactly one** `Final status:` line, and that line must be the **last non-empty** line in the file (see **`AGENTS_PROTOCOL.md`**).
- **Stale** content, **duplicated** report blocks, or **multiple** `Final status:` lines make the report **invalid**; the agent must **rewrite its own file cleanly** before finishing if it detects any of these in its own audit path.
- Do **not** create these audit files inside repository roots unless explicitly requested.
- Each report should include, when applicable: **report timestamp with timezone**; **agent name**; **protocol version read** and **whether the protocol was read successfully** (per **`AGENTS_PROTOCOL.md`**); **execution mode**; scope; commands; files inspected / created / modified / deleted; folders created or deleted; files copied or moved; git status before/after; staged files if git was used; commit hash if created; push result if allowed; external/network access; blocked items; deviations; the single terminal **`Final status:`** line.

**Legacy:** The older single file `D:\MyPrograming\What_I_Have_Done.md` is **deprecated** for routine multi-agent reporting (one writer could clobber another). Prefer the **`What_I_Have_Done\`** folder and per-agent files above.

**Purpose:** Full traceability without agents overwriting each other’s audits.

### Agent report review and token honesty (public-safe)

- When reviewing agent execution reports, use a **score out of 5** with a **brief reason**; add a **short improvement note** when useful.
- Reports that involved model or API processing should include a **Token Routing / Saving Report** section (internal vs external usage, routing summary when known).
- If exact token counts or costs are **not available**, state **Unknown** and explain why — **do not fabricate** token numbers.
- Estimates, when used, must be labeled **Estimated** with the measurement source noted.

### Skill Bank (local bodies — public-safe summary, 2026-05-29)

- Local **_KnowledgeWiki** Skill Bank (`skills/`) holds **agent-neutral** procedures; **`skills/README.md`** is the **live registry** (agent quick tables are shortcuts only).
- **Stabilized 2026-05-23** (session `SESSION_SKILL_BANK_BACKBONE_AND_PROJECT_MANIFEST_DRY_TEST_2026-05-23`): **workflow-audit**, **memory-update-safe**, **agent-report-review**, **project-manifest**, **skill-discovery**, **skill-opportunity-review**.
- **Expanded 2026-05-29 (public-safe names only):** **personal-monitoring**, **compact-session-prompt**, **memory-update-safe** / **github-safe-publish** (publish verification layers), **skill-authoring**, plus **learned operating practices** in local `agents/shared.md` (evidence, skill discovery, design before build, agent-neutral distillation).
- **Session finality:** Do not claim **PASS** / session closed while unresolved items remain — use **PARTIAL** / **NEEDS_REVIEW** / **BLOCKED** (see **06_MEMORY_MAINTENANCE_POLICY.md**).
- **Owner-facing Arabic:** Abu Saleh editorial review for catalog wording; agents apply approved Arabic — do not invent literal owner-facing Arabic.
- **project-manifest** had a practical **dry test** on a private voice-kit project — **PASS** locally; do **not** publish full manifests or long audit bodies here.
- **Cursor audit hygiene:** long accumulated `cursor.md` content may be copied to **`What_I_Have_Done/archive/`** (dated archive); active **`cursor.md`** remains append per run unless owner requests overwrite.

### Skill Bank governance — avoid duplicate skills and rules (public-safe, 2026-05-29)

**Operating preference (owner-approved):** Before proposing a **new rule**, **decision record**, or **Skill Bank skill**, check whether an **existing Skill Bank skill** or **shared operating rule** already covers it.

| Default | Action |
|---------|--------|
| Pattern already covered (~80%+) | **Improve or anchor** the existing skill or rule — do **not** add a near-duplicate |
| Repeated useful pattern | Route through **skill-discovery** → **skill-opportunity-review** → **skill-authoring** (authoring **only after** review + approval) |
| Long / multi-session project work | Use **project-continuity-plan** decision gate when applicable |
| Session accountability | **workflow-audit** and local **`agents/shared.md`** learned practices |

**Do not** create skills from **one-time use** or session **excitement**. Prefer **improving existing mechanisms** over skill bloat.

**ChatGPT / Abu Saleh:** Proactively remind Abu Muhammad when a new idea should be routed into existing mechanisms (names above) instead of inventing a parallel rule or skill. Full skill bodies stay in local **_KnowledgeWiki** only.

### Controlled agent self-development (public-safe)

Adopt a **controlled self-development workflow** for agents:

- Agents **must not** modify themselves or implement self-development changes **directly**.
- Any agent may **record improvement ideas** in a **dedicated ideas register** (local, not published here in full).
- When an idea matures or is adopted, record it in a **dedicated evolution/history register** (local detail stays private unless approved for public summary).
- **Any real implementation** requires **explicit review and approval** by the program owner (user/supervisor) **before** execution.
- The workflow must stay **agent-neutral** and **reusable** across current and future agents — not tied to one tool.
- Agents may **later** propose development ideas from references, communities, or GitHub — **as suggestions only**, never as automatic implementation.
