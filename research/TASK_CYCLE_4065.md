# TASK CYCLE 4065 — Initial task message for the next agent

**Status:** COMPLETE (2026-11-25T18:45:23Z)
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

## Current facts you can rely on (verified 2026-11-25T18:08:37Z)

- Binance Futures `fundingRate` (BTCUSDT, limit=1): HTTP 451 (RESTRICTED_LOCATION) — blocked (last probed 2026-11-03T13:16:19Z; not re-probed since, per the no-probe rule).
- Bybit V5 `funding/history` (linear, BTCUSDT, limit=1): HTTP 403 (COUNTRY_BLOCKED) — blocked (last probed 2026-11-03T13:16:19Z; not re-probed since).
- Kraken spot ticker (XBTUSD): HTTP 200 (sanity check only; not part of the H1 spec).
- `research/HYPOTHESES.md` md5 `38edf583b5d29c652407099c0ba33699`.
- `research/SEARCH_LOG.md` md5 `6723bd26ec6937524261c9a617b6d24f`.
- Local HEAD at start of this cycle = `b209a95021baf7e6daa3a18c6b168b485de08957` (verified 2026-11-25T18:08:37Z; working tree clean at start of this cycle).

## Result

Read `research/HANDOFF.md` and `research/TASK_CYCLE_4065.md`. Project confirmed CLOSED / STANDBY and research-only. No activation condition occurred: no unrestricted network/proxy supplied, no validation authorized, no new hypothesis or route requested, no retire/restructure request. Per the task's default branch, no research-file changes were made (no standby cycle, no re-probe, no edits to `research/HYPOTHESES.md` or `research/SEARCH_LOG.md` merely to record nothing changed). H1/H2 remain falsified for tradability under documented costs via venue substitution; original Binance/Bybit spec untested due to geo-blocked endpoints. Chain remains terminated at Cycle 3388. Task marked COMPLETE; next-agent pointer advanced to `research/TASK_CYCLE_4066.md` in `research/HANDOFF.md`.

EOF