# Reference Notes

## Where to start

Start from **`00_MASTER_MEMORY_INDEX.md`** before using older notes.

Use these public files by purpose:

| Purpose | File |
|---------|------|
| Index and routing | `00_MASTER_MEMORY_INDEX.md` |
| Retention, cleanup, lightweight notes | `06_MEMORY_MAINTENANCE_POLICY.md` |
| Durable operating rules | `AGENTS_PROTOCOL.md`, `01_GLOBAL_RULES.md` |
| Active projects | `04_ACTIVE_PROJECTS.md` and relevant `projects/*.md` |
| MyDoctor maintenance (2026-06-01, public pointer) | `docs/2026-06-01_mydoctor_maintenance_public_pointer.md` |
| Primary Cursor startup rule (2026-06-03) | `docs/2026-06-03_primary_cursor_start_rule.md` |
| Owner Windows Ollama + Claude Code baseline (pointer) | `03_TOOLS_AND_ENVIRONMENT.md` → `_KnowledgeWiki/tools/owner-windows-ollama-claude-local-baseline.md` (includes 2026-06-02 GPU repair + **`qwen3.5-9b-64k` Write-tool success**) |

## Notes discipline

Keep local notes short.

Do not duplicate long operational history.

Move durable rules and stable decisions to the proper external reference listed above.

Keep public files safe for public reading.

Do not place secrets, credentials, private client details, or unnecessary personal labels in public files.

Prefer neutral labels such as owner, program owner, or authorized owner when a role is needed.

## ChatGPT internal memory limit (Abu Saleh — governance)

**One rule:** ChatGPT **internal** memory stays minimal — **target 3** active operational anchors; **temporary max 5** only when truly necessary. Internal memory is **not** an archive. Operational, project, and protocol detail belongs in **external** memory (public repo, KnowledgeWiki, **`AS_REF.md`**, and other approved external references). Any **new durable** operational detail requires **owner approval** before external recording. Temporary or completed reminders **expire or are removed**. **Recovery anchors (do not remove):** see **Reference retention** below.

## Reference retention

**Protected keys (recovery anchors):** Do not remove from lightweight ChatGPT notes:

- Public memory repo: `https://github.com/Alodhaibee/abu-muhammad-memory-public`
- This file: **`AS_REF.md`** (short ChatGPT-facing recovery reference)

When local notes grow beyond the basic anchors, review each additional item first:

| Item type | Action |
|-----------|--------|
| Temporary or completed | Remove from local notes. Do not export. |
| Durable operational information | Ask the **authorized owner** first whether external recording is approved. |
| After approval only | Route with the next suitable execution prompt: record here if the item belongs in short reference notes; otherwise record in the public index, operational wiki, project files, or other appropriate external reference for shared agents, projects, or system-wide rules. |

**Goals:** Prevent loss of important information. Prevent internal note bloat.

## ChatGPT internal memory — externalized pointers (2026-06-02)

Use this block so ChatGPT **internal** memory stays minimal. **Do not** duplicate long history here — read the linked source.

| Area | External source (durable) |
|------|---------------------------|
| Memory limits + recovery anchors | Sections **ChatGPT internal memory limit** and **Reference retention** in this file |
| Abu Saleh identity / naming | Private chat: **أبو محمد**. Transferable files: **owner**, **authorized owner**, **مالك البرنامج**, **المالك** — no personal name unless owner requests. Full rule: **`AGENTS_PROTOCOL.md`** (Owner-Name Privacy Rule), **`01_GLOBAL_RULES.md`** |
| Owner explanations | Prefer plain **Arabic**, owner-readable; explain technical terms simply when needed. Skill Bank Arabic editorial: **`06_MEMORY_MAINTENANCE_POLICY.md`** |
| Agent prompt discipline | Normal prompts only: session name, purpose, owner decision, task, allowed reads/writes, task forbidden, final marker. **Do not** re-teach installed protocol or repeat Working on / audit / rollback / skills rules unless the task changes protocol. Full rule: **`D:\MyPrograming\_KnowledgeWiki\agents\shared.md`** (Compact session prompts); public summary: **`06_MEMORY_MAINTENANCE_POLICY.md`** |
| External-first operational detail | Cursor/protocol/rollback/Working on/skills reporting, Telegram Mailman, MyDoctor pointers, project status → KnowledgeWiki **`agents/`**, **`00_MASTER_MEMORY_INDEX.md`**, **`04_ACTIVE_PROJECTS.md`**, **`projects/*.md`** — not ChatGPT internal archive |

**Legacy topic pointers** (compact — expand only in proper project files when approved):

| Topic | Pointer |
|-------|---------|
| UQU / Arabic-first desktop tools & reporting | `projects/UQU_OFFICE.md` |
| UQU Council PDF → Arabic CSV/Excel extraction | UQU-related; no dedicated public page yet — use `projects/UQU_OFFICE.md` until approved |
| C# WinForms (primary); Python/Streamlit (secondary) | `03_TOOLS_AND_ENVIRONMENT.md`; local repos per task |
| Local Ollama / offline models | `03_TOOLS_AND_ENVIRONMENT.md` → `_KnowledgeWiki/tools/owner-windows-ollama-claude-local-baseline.md` |
| C# WinForms + Ollama chatbot | Local project; no `projects/*.md` yet — owner approval before public detail |
| PDF Genie | Local PDF utility; no `projects/*.md` yet — owner approval before public detail |
| Pine Script / TradingView | `projects/TRADING_AND_PINE.md` |
| YouTube transcript tool | `projects/YOUTUBE_TEXT_EXTRACTOR.md` |
| Telegram messaging / bots | `projects/TELEGRAM_MAILMAN.md`, `projects/LABIB.md` |
| `/to_see_html` visual verification (see-to-believe-lab; single-page + split-view; closeout `TO_SEE_HTML_CLOSEOUT_COMPLETE`) | `04_ACTIVE_PROJECTS.md`; `03_TOOLS_AND_ENVIRONMENT.md`; _KnowledgeWiki `tools/see-to-believe-lab-to-see-html.md` |
| Home Assistant / Alexa automation | `projects/SMART_HOME_IOT.md` |

## Consolidated table (when requested)

When a consolidated memory table is requested:

1. Read the relevant files referenced by the public index and the stated scope.
2. Build **one** consolidated table from those sources.
3. Do not rely on partial recall or stale summaries alone.
4. Keep entries public-safe; omit secrets, credentials, and private client details.
