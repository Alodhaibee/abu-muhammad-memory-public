# Tools And Environment (Public Safe)

## Roles in the current system (high level)
- **ChatGPT:** planning, review, prompt shaping, decisions, reading structured execution reports.
- **Codex:** strong **terminal-side** executor with **`D:\MyPrograming\CodexSkills`** (`AGENTS.md` + skills: `codex_workflow`, `memory_github_reader`, `safe_project_executor`); **MCP** may attach later. Operates under tight guardrails (scoped paths, no delete/move by default, no commit/push/network/install unless explicitly allowed, mandatory `What_I_Have_Done.md` overwrite).
- **Cursor:** primary **IDE-visible** executor for repositories and files; typical editing and memory maintenance workflows.
- **Claude Code:** deep programming executor when heavy implementation passes are needed.
- **Abu Muhammad Project Control Center:** local Python GUI dashboard under `D:\MyPrograming\AbuMuhammadControlCenter` — lists projects under `D:\MyPrograming`, Git status, opens Folder/Cursor/VS Code/PowerShell, shows `D:\MyPrograming\What_I_Have_Done.md`, stores notes in `data\project_notes.json`, uses `run.bat` / `run_debug.bat`.
- **GitHub Memory (this repository):** official **public-safe** shared memory for assistants — not a vault for secrets.

## Codex and CodexSkills
- **CodexSkills** (permanent local pack): **`D:\MyPrograming\CodexSkills`** — active reference for Codex rules and skills (see **`projects/CODEX_SKILLS.md`** in this repo for public-safe summary).
- **`D:\MyPrograming\test_codex`** was a **temporary sandbox** for Codex CLI experiments; it was **removed manually** after migration and is **not** canonical.
- **Codex CLI** permission-style check succeeded in that sandbox (e.g. creating `PERMISSION_TEST.txt` and writing `What_I_Have_Done.md`) before adopting CodexSkills as the durable location.

## Preferred tools and platforms (legacy list + anchors)
- Abu Muhammad Project Control Center (see above)
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

## Safety boundary
This file contains tool preferences only and intentionally excludes access credentials, system addresses, or operational secrets.
