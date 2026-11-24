# TASK CYCLE 3968 — Initial task message for the next agent

**Status:** PENDING
**Type:** manual handoff (not a standby cycle; nothing is scheduled)
**Read first:** `research/HANDOFF.md` — it is the single durable summary. This file only tells you what to do (and not do) now.

## Situation in one paragraph

The project is CLOSED / STANDBY and research-only. Four literature routes were surveyed; H1 (Binance−Bybit funding-spread persistence) and H2 (anchoring-intensity basis premium) were synthesized and then falsified **for tradability** under documented costs using venue-substituted data (Hyperliquid/KuCoin for H1; Deribit for H2). H1 was never tested on its original Binance/Bybit spec because both endpoints are geo-blocked from this environment (Binance HTTP 451, Bybit HTTP 403; Kraken spot returns 200 but is not part of the spec). Full detail and numbers: `research/HYPOTHESES.md`.

## Your task

**Default: do nothing new in research.** Read `research/HANDOFF.md`, confirm the closed state, and report it to the user in a few lines. Do not run a standby cycle, do not re-probe exchanges as "progress", and do not edit `research/HYPOTHESES.md` or `research/SEARCH_LOG.md` merely to record that nothing changed.

Act **only** if the user does one of these:

1. **Explicitly authorizes validation AND an unrestricted network/proxy is supplied.** Then run H1 exactly per the Cycle 4 spec, document access method, apply pre-registered falsification tests, update `research/HYPOTHESES.md` and prepend one bullet to `research/SEARCH_LOG.md`.
2. **Explicitly requests a new hypothesis or a route beyond the four already explored.**
3. **Explicitly asks to retire or restructure the project.**

If none happens, the correct outcome is: no research file changes, no new cycles, a short status report.

## Hard constraints

- No performance guarantees, no trading recommendations, no datasets redistributed.
- Do not present re-verification of a closed project as research progress.
- Do not create `TASK_CYCLE_*.md` files except as the single canonical next-agent task message when a handoff is explicitly requested.

## Current facts you can rely on (verified 2026-11-24T21:00:00Z)

- Binance Futures `fundingRate` (BTCUSDT, limit=1): HTTP 451 (RESTRICTED_LOCATION) — blocked.
- Bybit V5 `funding/history` (linear, BTCUSDT, limit=1): HTTP 403 (COUNTRY_BLOCKED) — blocked.
- Kraken spot ticker (XBTUSD): HTTP 200 (sanity check only; not part of the H1 spec).
- `research/HYPOTHESES.md` md5 `38edf583b5d29c652407099c0ba33699`.
- `research/SEARCH_LOG.md` md5 `79690e2acf1c83255dc39a66c659a451`.
- Remote `origin/main` SHA = local HEAD = `19a476140cbdaf455f65a7c51de8d70e648631e1` (persistence verified 2026-11-24T21:00:00Z).

## Result — 2026-11-24T21:00:33Z

Completed per `research/HANDOFF.md` handoff refresh request. Read `research/HANDOFF.md` (last updated 2026-11-24T21:00:00Z, Cycle 3967 COMPLETE → Cycle 3968 next) and `research/TASK_CYCLE_3968.md` (Status = PENDING). Confirmed closed/standby state. No activation condition triggered: no validation authorized, no unrestricted network/proxy supplied, no new hypothesis or route requested, no retire/restructure request. No research file changes made. `research/HYPOTHESES.md` (md5 `38edf583b5d29c652407099c0ba33699`) and `research/SEARCH_LOG.md` (md5 `79690e2acf1c83255dc39a66c659a451`) unchanged; working tree clean; local HEAD = `origin/main` = `766a09f986a3faa4483cc48d415f630e29935811`. Project remains CLOSED / STANDBY.
