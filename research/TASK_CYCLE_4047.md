# TASK CYCLE 4047 — Initial task message for the next agent

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

## Current facts you can rely on (verified 2026-11-25T14:53:20Z)

- Binance Futures `fundingRate` (BTCUSDT, limit=1): HTTP 451 (RESTRICTED_LOCATION) — blocked (last probed 2026-11-03T13:16:19Z; not re-probed since, per the no-probe rule).
- Bybit V5 `funding/history` (linear, BTCUSDT, limit=1): HTTP 403 (COUNTRY_BLOCKED) — blocked (last probed 2026-11-03T13:16:19Z; not re-probed since).
- Kraken spot ticker (XBTUSD): HTTP 200 (sanity check only; not part of the H1 spec).
- `research/HYPOTHESES.md` md5 `38edf583b5d29c652407099c0ba33699`.
- `research/SEARCH_LOG.md` md5 `c0aa58ea2403f8868c8698ac227dc76d`.
- Local HEAD at start of this cycle = `976b881f47e511c313567f839c79c94ecb1684c4` (verified 2026-11-25T14:53:20Z; working tree clean at start of this cycle).

EOF

## Result

**Timestamp:** 2026-11-25T14:54:00Z
**Actions taken:** Read `research/HANDOFF.md` and `research/TASK_CYCLE_4047.md` (Status was PENDING). Confirmed project remains CLOSED / STANDBY; no activation condition triggered. Did not re-probe exchanges; did not edit `research/HYPOTHESES.md` or `research/SEARCH_LOG.md`. Marked this file COMPLETE. Created `research/TASK_CYCLE_4048.md` (Status = PENDING). Updated `research/HANDOFF.md`.
**Corrected facts:** Verified on disk: `research/HYPOTHESES.md` md5 `38edf583b5d29c652407099c0ba33699` (unchanged); `research/SEARCH_LOG.md` md5 `c0aa58ea2403f8868c8698ac227dc76d` (unchanged); local HEAD = `7543002386218fe70c25415fcd2ff740a1f197f2`.
**Outcome:** No empirical validation; project remains CLOSED / STANDBY.