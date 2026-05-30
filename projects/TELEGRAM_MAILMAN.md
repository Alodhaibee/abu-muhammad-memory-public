# Telegram Mailman — ساعي تيليجرام (public-safe)

Last updated: 2026-05-31  
Status: **Paused — private GitHub repo live; GitHub publish phase closed**  
Public-safe: yes (no secrets, no tokens, no chat IDs, no `.env` values)

## Location

- **Local code:** `D:\MyPrograming\tools\telegram-mailman`
- **Private GitHub repo:** `https://github.com/Alodhaibee/telegram-mailman` (private — no secrets in repo)
- **Local data queue:** `D:\MyPrograming\_KnowledgeWiki\inbox\telegram-mailman\`
- **Local operational plan:** _KnowledgeWiki `projects/telegram-mailman/` (not published to GitHub)

## What it is

Standalone local **Telegram message carrier**: ingest, route, queue, and gated delivery under documented safety rules. **Offline by default** — no live Bot API calls unless an owner-authorized exec session explicitly enables live mode.

## Current milestone (2026-05-31)

**Private GitHub repo created and first safe publish completed** — session `SESSION_TELEGRAM_MAILMAN_CREATE_PRIVATE_REPO_AND_SAFE_FIRST_PUSH_2026-05-31`, closeout `SESSION_TELEGRAM_MAILMAN_GITHUB_CLOSEOUT_2026-05-31`, final status **`GITHUB_PRIVATE_REPO_FIRST_PUSH_COMPLETE`**.

### Delivered (conceptual — no runtime values)

| Item | Summary |
|------|---------|
| **Private code repo** | `Alodhaibee/telegram-mailman` — private; first commit `b6bbae1` on `main` |
| **Publish safety** | Selective staging only; `.env`, tokens, chat IDs, runtime queue/outbox, and private evidence dirs excluded |
| **Preflight + send ledger** | Gated live path with owner authorization checks and persistent send ledger |
| **Offline tests** | **29/29** unit tests pass; no Telegram API in test runs |
| **Documentation** | Bilingual docs + `docs/en/PUBLISH_SAFETY.md`; one prior owner-authorized dry-run verified |

### Live sending status

| Item | State |
|------|--------|
| Live sending | **Paused** — no further live send authorized |
| Default mode | **Offline** |
| Prior live verification | One authorized dry-run completed in a prior session (2026-05-30) |
| GitHub publish / closeout sessions | No API calls; no messages sent |

**Rule:** No future live send should occur until owner explicitly authorizes a new scoped exec session.

## Safe next step

**Local config guide** (`OWNER_SETTINGS.md`) or optional **GitHub CI** for offline tests on push. **Not** a live send session.

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
| Hardening review + pre-dry-run fixes | Done |
| Owner-authorized dry-run + post-dry-run closeout | Done |
| Private GitHub repo + first safe publish | Done |
| GitHub publish closeout | Done |
| Notification policy / rollback CLI / CI | Not started |
