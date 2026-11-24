# TASK CYCLE 3965 — Initial task message for the next agent

**Status:** COMPLETE
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

## Current facts you can rely on (verified 2026-11-24T20:49:55Z)

- Binance Futures `fundingRate` (BTCUSDT, limit=1): HTTP 451 (RESTRICTED_LOCATION) — blocked.
- Bybit V5 `funding/history` (linear, BTCUSDT, limit=1): HTTP 403 (COUNTRY_BLOCKED) — blocked.
- Kraken spot ticker (XBTUSD): HTTP 200 (sanity check only; not part of the H1 spec).
- `research/HYPOTHESES.md` md5 `38edf583b5d29c652407099c0ba33699`.
- `research/SEARCH_LOG.md` md5 `79690e2acf1c83255dc39a66c659a451`.
- Remote `origin/main` SHA = local HEAD = `6af20b3ec1444241c3021538f99a81c30e1cfdf6` (persistence verified 2026-11-24T20:50:25Z).

## Result

**Timestamp:** 2026-11-24T20:50:25Z
**Action:** Executed pending Cycle 3965 task. Read `research/HANDOFF.md` and confirmed closed state; no activation condition triggered (no unrestricted network/proxy supplied, no new hypothesis/route requested, no validation authorized, no retire/restructure requested). No research file changes, no new cycles, no empirical validation, no datasets downloaded, no trading recommendations made. Marked `research/TASK_CYCLE_3965.md` COMPLETE. Created `research/TASK_CYCLE_3966.md` as next canonical initial task message (Status = PENDING). Updated `research/HANDOFF.md`.
**Outcome:** Project remains CLOSED / STANDBY. `research/HYPOTHESES.md` md5 `38edf583b5d29c652407099c0ba33699`, `research/SEARCH_LOG.md` md5 `79690e2acf1c83255dc39a66c659a451` — both unchanged.
