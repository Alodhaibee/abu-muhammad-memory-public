# PI Governed Agent Kit (Public Safe)

Last updated: 2026-06-11  
Status: **Foundation closed** — governed execution ongoing

---

## Purpose

Public-safe memory for **pi-governed-agent-kit**: a neutral-name governed Pi integration layer where **Cursor supervises and evaluates** while **Pi executes** bounded, repeatable tasks under local-first model routing and owner governance.

This file is a **high-level anchor** only. Detailed operational truth lives in local KnowledgeWiki (`_KnowledgeWiki/projects/pi-governed-agent-kit/`).

---

## What was proven (foundation track — closed 2026-06-11)

- Pi runs reliably under governance with **local Ollama** (primary: `gemma4-64k:latest`).
- **Cursor + Pi role split** works: Pi produces raw output; Cursor evaluates separately.
- **PI-TEST-002** (read-only PI Work documentation handoff) **passed** — validation complete.
- **Micro-testing loop closed** — do not reopen for validation.
- **KnowledgeWiki synced** with validated phase status and governance docs.

---

## Durable rules (public-safe summary)

| Rule | Summary |
|------|---------|
| Local-first | Default to Ollama; escalate to ChatGPT/Codex auth only with evidence |
| API keys | Disabled by default — explicit owner approval only |
| Closed projects | Delivered external projects are out of scope unless owner reopens |
| PI-TEST-001 | **Deprecated** — do not run |
| Output separation | Raw Pi output ≠ Cursor evaluation ≠ durable wiki content |
| Recording | WiseMan order: correct → dedupe → place → record last |
| Launch discipline | Non-blocking launcher; single-flight; wrapper hangs ≠ model failure |

---

## What ChatGPT should remember

- The Pi foundation **validation track is closed**; next work is **real governed execution** (scoped handoffs), not more tests.
- Canonical project status: Phase 3 complete, Phase 4 active for ongoing governed use.
- Do not treat raw lab outputs as organizational truth.
- Do not suggest rerunning PI-TEST-001 or PI-TEST-002 unless owner explicitly reopens validation.

---

## What must remain private

- Full filesystem paths to lab scaffolds and raw output folders (local ops detail).
- Launcher scripts, timing logs, and benchmark artifacts.
- Any auth tokens, model endpoints beyond public policy, or session raw dumps.
- Deprecated external-project test history (PI-TEST-001).

---

## Related safe files

- `04_ACTIVE_PROJECTS.md` — add pi-governed-agent-kit entry when owner updates index
- `01_GLOBAL_RULES.md`
- Local KnowledgeWiki: `projects/pi-governed-agent-kit/` (not copied into this repo)

---

## Public-safe status block

| Item | Status |
|------|--------|
| Foundation track (Phase 0–3 + validation) | **Closed / PASS** |
| Phase 4 governed execution | **Active** — ongoing useful handoffs |
| PI-TEST-002 | **PASS** — closed |
| PI-TEST-001 | **Deprecated** |
| Micro-tests | **Closed** |
| KnowledgeWiki sync | **Complete** (2026-06-11) |
| Public memory record | **Published** (2026-06-11) |

---

## Next-task guidance

Before detailed Pi advice, ask whether the task is:

1. **Governed execution** (scoped read-only handoff — normal path), or  
2. **Kit/promotion change** (needs owner scope + WiseMan review).

Do not recommend validation reruns or external closed-project tests by default.

---

## Boundaries

- This summary does **not** authorize git push, deploy, API keys, or writes to closed external projects.
- Promoting lab scripts to shared `tools/` requires a separate owner-approved session.
- Raw Pi outputs stay in the local lab — never auto-promote to public memory.
