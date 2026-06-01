# MyDoctor Maintenance — Public-Safe Pointer (2026-06-01)

**Status:** Closed (public-safe summary)  
**Classification:** Public-safe pointer only — full detail in private memory

---

## What happened (summary)

During agent/wiki maintenance work in early June 2026, Cursor behavior drift was investigated (Working on table format, mixed audit report output). The owner paused for diagnosis. A **MyDoctor** maintenance/diagnostic skill was adopted in the local Skill Bank. Private KnowledgeWiki recovery snapshots and a recovery policy were added to the **private** memory repository. Final read-only health check passed.

---

## Public-safe facts

- **MyDoctor** is the first-choice **read-only** diagnostic skill for ecosystem health: memory layers, agent governance, skills, audit integrity, recovery coverage, and behavior drift.
- Default intervention level: **OBSERVE** (no silent fixes).
- **Cursor audit report of record:** per-agent file under `What_I_Have_Done/` (Cursor uses `cursor.md`) — not chat summaries.
- **Public memory repo** holds public-safe content only.
- **Private memory repo** holds internal operational detail and KnowledgeWiki recovery snapshots.
- **ChatGPT** may not access the private GitHub repo from the web; **Cursor** can perform read-only checks from the local environment when asked.

---

## Where to read more

| Need | Where |
|------|-------|
| Public routing | `00_MASTER_MEMORY_INDEX.md`, `AS_REF.md`, `06_MEMORY_MAINTENANCE_POLICY.md` |
| _KnowledgeWiki MyDoctor skill | Local Skill Bank only (not published wholesale) |
| Full incident detail | **Private** memory repo — ask Cursor to summarize `docs/2026-06-01_cursor_mydoctor_maintenance_incident_operational_note.md` |

---

## ChatGPT memory hygiene

After Cursor confirms this pointer and the private note exist, ChatGPT may keep only lightweight anchors: external-first principle, public repo URL, and this pointer — not the full incident narrative.
