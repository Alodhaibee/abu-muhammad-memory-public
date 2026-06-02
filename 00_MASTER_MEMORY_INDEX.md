# MASTER MEMORY INDEX (PUBLIC SAFE)

Last updated: 2026-06-02
Status: Active

## Agents Protocol (mandatory — all agents/tools)

**Read `AGENTS_PROTOCOL.md` first** (repository root). It is the **central, versioned operating protocol** for ChatGPT, Cursor, Codex Desktop, Claude, Antigravity, and future agents. It **supersedes** fragile repeated long instructions in prompts when those instructions **duplicate or conflict** with the protocol.

Then read this index file (`00_MASTER_MEMORY_INDEX.md`).

## Codex Desktop (agent instructions)

**Codex Desktop** must follow the permanent operating guide: **`CODEX_DESKTOP_INSTRUCTIONS.md`** (repository root). It defines how Codex integrates with this public memory layer, required reading order, audit reporting, and boundaries alongside ChatGPT, Cursor, and Claude.

## Assistant Rules (Mandatory)
1. Read **`AGENTS_PROTOCOL.md`** before any other file, then this index.
2. Read only the relevant project file for the current task.
3. Do not load all files unless necessary.
4. Treat this repository as public-safe, high-level memory only.
5. Follow **`AGENTS_PROTOCOL.md`** — **Owner-Name Privacy Rule** (neutral labels in recorded files; personal name in private chat only).
6. Never ask the program owner to place secrets in this repository.
7. If a task needs secrets or operational access, ask for a safe summary or use Cursor locally on the private repository.
8. For project-specific tasks, read the matching file under `projects/`.
9. Keep responses Arabic-first unless the task requires English.
10. Respect the program owner's style: practical, phased, documented, low confusion.

## ChatGPT / Abu Saleh memory (three anchors + limit)

**Canonical:** **`06_MEMORY_MAINTENANCE_POLICY.md`** (three lightweight anchors) · **`AS_REF.md`** (target **3** / max **5** limit, externalized pointers, legacy topic router).

Keep ChatGPT memory limited to:

1. **External-first** — durable rules and project detail live externally, not in ChatGPT memory.
2. **Public repo URL** — `https://github.com/Alodhaibee/abu-muhammad-memory-public`
3. **Anti-bloat self-reminder** — start from this repo and this index; export excess durable detail via Cursor/KnowledgeWiki/GitHub, verify, then prune ChatGPT memory.

## Routing by task type
- Central agents protocol (all tools): `AGENTS_PROTOCOL.md`
- General execution rules: `01_GLOBAL_RULES.md`
- Tone and language style: `02_STYLE_AND_RESPONSE_RULES.md`
- Tools/platform overview: `03_TOOLS_AND_ENVIRONMENT.md`
- Active project map: `04_ACTIVE_PROJECTS.md`
- Security boundaries: `05_SECURITY_AND_PRIVACY_RULES.md`
- Memory process policy: `06_MEMORY_MAINTENANCE_POLICY.md`
- Short reference notes: `AS_REF.md`

## Project routing
- LABIB: `projects/LABIB.md`
- ControlCenter (UI: **Control Center** / **Project Dashboard**): `projects/ABU_MUHAMMAD_PROJECT_CONTROL_CENTER.md` — formerly folder `AbuMuhammadControlCenter`; local path `D:\MyPrograming\ControlCenter`
- CodexSkills: `projects/CODEX_SKILLS.md`
- OZZY_OPENCLAW: `projects/OZZY_OPENCLAW.md`
- SECOND_BRAIN: `projects/SECOND_BRAIN.md`
- UQU_OFFICE: `projects/UQU_OFFICE.md`
- SITE_SCOUT: `projects/SITE_SCOUT.md`
- TRADING_AND_PINE: `projects/TRADING_AND_PINE.md`
- N8N: `projects/N8N.md`
- MOLYRA: `projects/MOLYRA.md`
- AOS_EXEC: `projects/AOS_EXEC.md`
- TJJ: `projects/TJJ.md`
- SMART_HOME_IOT: `projects/SMART_HOME_IOT.md`
- SAAS_IDEAS: `projects/SAAS_IDEAS.md`
- Repo Radar (رادار المستودعات): `projects/REPO_RADAR.md` (خطة التطوير اللاحق محليًا: `D:\MyPrograming\RepoRadar\ROADMAP.md`)
- Youtube_TextExtractor (مستخرج نص YouTube — Telegram): `projects/YOUTUBE_TEXT_EXTRACTOR.md` (مسار محلي: `D:\MyPrograming\Youtube_TextExtractor`)
- Telegram Mailman (ساعي تيليجرام — local carrier): `projects/TELEGRAM_MAILMAN.md` (مسار محلي: `D:\MyPrograming\tools\telegram-mailman`)

## Codex / skills / MCP routing
When the task involves **Codex**, local **skills** (`AGENTS.md`, `skills/*/SKILL.md`), or **MCP** wiring plans, read **`projects/CODEX_SKILLS.md`** after this index. **Codex is officially adopted** as a bounded executor. Canonical workstation folder: **`D:\MyPrograming\CodexSkills`**. Private GitHub mirror for the skill pack: **`https://github.com/Alodhaibee/CodexSkills`** (repository **Private**; file bodies not mirrored in this public repo).

## How AI assistants should use this memory
1. After reading **`AGENTS_PROTOCOL.md`**, read this index file.
2. Read only the relevant project file.
3. Do not load all files unless necessary.
4. Use public repo as safe context only.
5. If details are missing, ask Abu Muhammad to have Cursor summarize from the private repo.
6. Never ask Abu Muhammad to publish secrets.
7. For long-term updates, instruct Cursor to update the private repo.

## Compatible AI Assistants
- ChatGPT: lightweight index, public-safe reader; planning, review, prompt shaping, decisions, reading execution reports.
- Claude / Claude Code: technical session advisor and deeper coding executor when used.
- Cursor: private memory librarian and primary IDE-visible code executor.
- Codex: terminal-oriented executor using **`D:\MyPrograming\CodexSkills`** (`AGENTS.md` + skills); future MCP-ready; always scoped safety rules.
- Future agents: must follow this index and all safety rules.

## Recommended first-read order
1. `00_MASTER_MEMORY_INDEX.md`
2. `STATUS_DASHBOARD.md`
3. relevant `projects/*.md`
4. `references/` only if needed
