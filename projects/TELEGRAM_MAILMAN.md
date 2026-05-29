# Telegram Mailman — ساعي تيليجرام (public-safe)

Last updated: 2026-05-30  
Status: **Paused — safety hardening implemented; live sending stopped**  
Public-safe: yes (no secrets, no tokens, no chat IDs, no `.env` values)

## Location

- **Local code:** `D:\MyPrograming\tools\telegram-mailman`
- **Local data queue:** `D:\MyPrograming\_KnowledgeWiki\inbox\telegram-mailman\`
- **Local operational plan:** _KnowledgeWiki `projects/telegram-mailman/` (not published to GitHub)

## What it is

Standalone local **Telegram message carrier**: ingest, route, queue, and gated delivery under documented safety rules. **Offline by default** — no live Bot API calls unless an owner-authorized exec session explicitly enables live mode.

## Current milestone (2026-05-30)

**Safety hardening implementation completed** — session `SESSION_TELEGRAM_MAILMAN_SAFETY_HARDENING_IMPLEMENT_2026-05-30`, final status **`PASS_SAFETY_HARDENING_IMPLEMENTED`**.

### Delivered (conceptual — no runtime values)

| Item | Summary |
|------|---------|
| **Preflight checks** | Offline CLI command to verify readiness before any future live send (owner authorization, routes, ledger state) |
| **Send ledger** | Persistent local file recording intended/completed send identities to help prevent cross-session duplicate sends |
| **Offline tests** | **26/26** unit tests pass; no Telegram API in test runs |
| **Documentation** | Bilingual docs synced; one prior live dry-run verified in prior authorized session |

### Live sending status

| Item | State |
|------|--------|
| Live sending | **Paused** — work stopped for now |
| Default mode | **Offline** |
| Prior live verification | One authorized dry-run completed in a prior session (2026-05-30) |
| This hardening session | No API calls; no messages sent |

**Rule:** No future live send should occur until **`SESSION_TELEGRAM_MAILMAN_HARDENING_REVIEW_2026-05-30`** (read-only review) passes and owner explicitly authorizes a new exec session.

## Remaining risks (public-safe summary)

- Send ledger not auto-seeded from prior canonical live evidence — review needed before second live send.
- Per-process send guard still exists alongside persistent ledger — review may consolidate.
- Hardening review not yet performed.

## Safe next step

**Read-only hardening review** — `SESSION_TELEGRAM_MAILMAN_HARDENING_REVIEW_2026-05-30`. **Not** a live send session.

## Boundaries (for agents)

1. Read **`AGENTS_PROTOCOL.md`** then **`00_MASTER_MEMORY_INDEX.md`** then this file.
2. **Do not** request tokens, chat IDs, or `.env` contents in public memory or agent prompts.
3. **Do not** run live Telegram API, probe, or send without explicit owner authorization in a scoped exec session.
4. Operational detail, evidence JSON, and `_ACTIVE_PLAN.md` stay in local _KnowledgeWiki / private audit paths unless separately approved for publish.
5. Telegram Mailman is **separate from Labib** — do not modify Labib Core/Router for Mailman tasks.

## Phase history (high level)

| Phase | Status |
|-------|--------|
| Offline prototype + route hardening | Done |
| First live dry-run (one message, authorized) | Done (prior session) |
| Post-live offline rollback | Done |
| Safety hardening (preflight + ledger + tests) | Done |
| Work pause + public memory record | Done (this update) |
| Hardening review | Not started |
| Category expansion / inbound / autostart | Not started |
