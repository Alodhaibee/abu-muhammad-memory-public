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

## Safety boundary
This file contains tool preferences only and intentionally excludes access credentials, system addresses, or operational secrets.
