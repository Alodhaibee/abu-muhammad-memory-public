# Tools And Environment (Public Safe)

## Roles in the current system (high level)
- **ChatGPT:** planning, review, prompt shaping, decisions, reading structured execution reports.
- **Codex:** **officially adopted** strong **terminal-side** executor with **`D:\MyPrograming\CodexSkills`** (`AGENTS.md` + skills: `codex_workflow`, `memory_github_reader`, `safe_project_executor`); **private** GitHub mirror **`https://github.com/Alodhaibee/CodexSkills`** (skills repo); **MCP** may attach later. Guardrails: scoped paths only; **no delete / move / rename** unless explicit; no commit/push/network/package install unless explicit; mandatory **`What_I_Have_Done.md` overwrite** (not append); no report inside project folders unless asked.
- **Cursor:** primary **IDE-visible** executor for repositories and files; typical editing and memory maintenance workflows.
- **Claude Code:** deep programming executor when heavy implementation passes are needed.
- **Control Center (ControlCenter):** local Python GUI dashboard under `D:\MyPrograming\ControlCenter` — lists projects under `D:\MyPrograming`, Git status (Treeview + cache), opens Folder/Cursor/VS Code/PowerShell, prefers audit `D:\MyPrograming\What_I_Have_Done\cursor.md` with fallback to `D:\MyPrograming\What_I_Have_Done.md`, stores notes in `data\project_notes.json`, uses `run.bat` / `run_debug.bat`.
- **GitHub Memory (this repository):** official **public-safe** shared memory for assistants — not a vault for secrets.

## Codex and CodexSkills
- **Codex CLI** installed, run, and tested; **Codex** is **formally approved** as a controlled executor (see **`projects/CODEX_SKILLS.md`**).
- **CodexSkills** (permanent local pack): **`D:\MyPrograming\CodexSkills`** — workstation anchor for `AGENTS.md` + skills.
- **Private GitHub repo** for the skill pack: **`https://github.com/Alodhaibee/CodexSkills`** — baseline **`44811e6f5e88876037423f2ab89ed4077b1cfc27`**, **`PUSH_VERIFIED`** when recorded.
- **`D:\MyPrograming\test_codex`** was a **temporary sandbox**; **removed manually**; **not** canonical.

## Preferred tools and platforms (legacy list + anchors)
- Control Center / ControlCenter (see above)
- Cursor
- ChatGPT
- Codex (+ CodexSkills local pack)
- Claude / Claude Code
- Antigravity
- GitHub
- Docker
- n8n
- Supabase (high-level mention only)
- TradingView
- Raspberry Pi
- Obsidian (knowledge notes and linked thinking)
- MemPalace (memory reinforcement workflow support)
- Graphify (high-level knowledge graph visualization candidate)
- gbrain (high-level graph-assisted knowledge workflow candidate)

## Python on Windows — logon autostart (adopted pattern)

For **long-running** local Python apps (bots, daemons) that should start at **Windows user logon** without a stuck black console:

| Use | Avoid for autostart |
|-----|---------------------|
| `scripts\run_*_hidden.vbs` launched by Scheduled Task via `wscript.exe //B` | Scheduled Task running `cmd.exe` or `scripts\run_*.bat` directly |
| `scripts\setup_autostart.ps1` / `check_autostart.ps1` / `remove_autostart.ps1` | Reading or logging `.env` secrets in setup scripts |
| `scripts\run_*.bat` for **manual** runs only (visible CMD is OK) | `pip` when `uv` is the project standard |
| `uv run` from project root; logs under `logs\` | Server deploy / SSH unless explicitly scoped |

`check_autostart` should report **hidden** vs **legacy visible** launcher. Full local skill: _KnowledgeWiki `skills/python-windows-autostart.md`. Reference project: `D:\MyPrograming\Youtube_TextExtractor` (task `Youtube_TextExtractor_Bot` — hidden launcher, 2026-05-21).

## Youtube Transcript Telegram Bot — deployment note (public-safe)

- **Local:** `D:\MyPrograming\Youtube_TextExtractor` (uv).
- **Remote:** Linux host — project folder `/home/0hani0/Programing/Telgram`; PM2 process **`telgram-bot`**; active script **`youtube_transcript_bot.py`**; legacy **`youtubeToText.py`** not the running entrypoint.
- **Restart (remote):** `pm2 restart telgram-bot`.
- **Secrets:** remain in remote **`config.py`** (unchanged); no `.env` copy from local; no tokens in this repo.
- **Removed on server (2026-05-21):** Supabase, MySQL, DB storage, save prompt — transcript sent as `.txt` only.
- **Server uv:** not installed; **venv/pip** kept for service stability.
- Full SSH/host details: private _KnowledgeWiki only.

## Safety boundary
This file contains tool preferences only and intentionally excludes access credentials, system addresses, or operational secrets.
