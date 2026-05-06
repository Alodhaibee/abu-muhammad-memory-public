# Public Memory System Playbook (Safe)

## Purpose
This repository is the safe readable memory index for ChatGPT.

## Operating model
- ChatGPT uses lightweight memory and reads this public repository for safe context.
- Cursor maintains full long-term memory in the private repository.
- Public files contain high-level summaries only.

## How ChatGPT should read memory
1. Read `00_MASTER_MEMORY_INDEX.md` first.
2. Read only files relevant to the current task.
3. For project tasks, read the matching file under `projects/`.
4. If deeper details are required, ask for a safe summary from Cursor.

## Update trigger phrase
- When Abu Muhammad says `حدث الذاكرة` (or similar), Cursor updates private memory first.
- Public summaries are updated only if content is safe for public reading.

## Public safety rule
- No secrets, credentials, direct access details, or operational private data are allowed.
