# Telegram Mailman — ساعي تيليجرام (public-safe)

Last updated: 2026-05-31  
Status: **Paused / stable** — rollback review complete; final hardening complete; **no rollback required**  
Public-safe: yes (no secrets, no tokens, no chat IDs, no `.env` values)

## Location

- **Private GitHub repo:** `https://github.com/Alodhaibee/telegram-mailman` (private — no secrets in tracked files)
- **Local operational detail:** _KnowledgeWiki `projects/telegram-mailman/` (including `_ACTIVE_PLAN.md` — not a substitute for this public summary)

## What it is

Standalone local **Telegram message carrier**: ingest, route, queue, and gated delivery under documented safety rules. **Offline by default** — no live Bot API calls unless an owner-authorized **Path A** exec session explicitly enables live mode.

## Current state (2026-05-31)

**Stable paused baseline** after message-policy documentation, offline CI verification, and rollback/final-hardening review.

| Area | State |
|------|--------|
| **Runtime** | **Offline** — not running live Telegram |
| **Rollback** | **Not required** — recent repo history reviewed and kept |
| **Message policy** | Documented in repo (`config/OWNER_SETTINGS.md`) — **Path A** (one-off authorized send) in code; **Path B** (pre-authorized notifications) **draft only, not active in code** |
| **Offline unit tests** | **29/29 pass** (local verification) |
| **GitHub Actions** | **Offline tests** workflow on `main` — passing; `unittest` only, `TELEGRAM_MODE=offline`, no secrets in workflow |
| **Documentation** | Bilingual README/CATALOG/X-Ray aligned with paused + policy phase |
| **Prior live** | One owner-authorized dry-run (2026-05-30); **no further live** until new Path A authorization |

**Rule:** No live send, probe, or Telegram API use without explicit owner authorization in a scoped exec session. Path B must not be treated as active until a future owner-approved implementation session.

## Delivered (high level — public-safe)

| Item | Summary |
|------|---------|
| Private code repo | Published on private `main`; selective publish (no `.env`, tokens, or private runtime dumps) |
| Safety hardening | Preflight checks, send ledger, offline test suite |
| Message policy docs | Owner operational policy adopted in repository documentation |
| Offline CI | GitHub Actions runs offline unit tests on push/PR — no Telegram API |
| X-Ray / docs sync | Architecture docs reflect paused + policy phase |
| Rollback + hardening review | Completed — project left stable, no revert |

## Live sending (explicit)

| Item | State |
|------|--------|
| Live sending now | **No** — paused |
| Default mode | **Offline** |
| Path B automatic notifications | **Not implemented** — design draft only |

## Optional next steps (owner-approved only)

- **Path B design / code** — after owner approves draft notification rules (not started)
- **New Path A live session** — explicit authorization only; not the default next action
- **GitHub branch protection** — optionally require the *Offline tests* workflow on `main`
- **Rollback CLI** — optional future tooling (not started)

Do **not** start new features, standing live permission, autostart, or inbound/webhooks without a dedicated approved session.

## Boundaries (for agents)

1. Read **`AGENTS_PROTOCOL.md`** then **`00_MASTER_MEMORY_INDEX.md`** then this file.
2. **Do not** request tokens, chat IDs, or `.env` contents in public memory or agent prompts.
3. **Do not** run live Telegram API, probe, or send without explicit owner authorization in a scoped exec session.
4. **Do not** treat Path B as active in code.
5. Operational detail, evidence JSON, and session audits stay in local _KnowledgeWiki / `What_I_Have_Done` unless separately approved for publish.
6. Telegram Mailman is **separate from Labib** — do not modify Labib for Mailman tasks.

## Phase history (high level)

| Phase | Status |
|-------|--------|
| Offline prototype + route hardening | Done |
| Safety hardening (preflight + ledger + tests) | Done |
| One authorized live dry-run + offline rollback | Done (2026-05-30) |
| Private GitHub repo + safe publish chain | Done |
| Message policy documentation (repo) | Done |
| X-Ray / README / Catalog sync | Done |
| Offline GitHub Actions CI | Done |
| Rollback review + final hardening | Done — no revert |
| Path B in code | Not started |
| Rollback CLI | Not started |
