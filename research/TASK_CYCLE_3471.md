# TASK CYCLE 3471 — Initial task message for the next agent

**Status:** PENDING
**Type:** manual handoff (not a standby cycle; nothing is scheduled)
**Read first:** `research/HANDOFF.md` — it is the single durable summary. This file only tells you what to do (and not do) now.

## Situation in one paragraph

The project is CLOSED / STANDBY and research-only. Four literature routes were surveyed; H1 (Binance−Bybit funding-spread persistence) and H2 (anchoring-intensity basis premium) were synthesized and then falsified **for tradability** under documented costs using venue-substituted data (Hyperliquid/KuCoin for H1, Deribit for H2). H1 was never tested on its original Binance/Bybit spec because both endpoints are geo-blocked from this environment (Binance HTTP 451, Bybit HTTP 403, both re-confirmed 2026-11-20T00:51:54Z; Kraken spot returns 200 but is not part of the spec). Full detail and numbers: `research/HYPOTHESES.md`.

## Your task

**Default: do nothing.** Verify nothing needs doing, report the closed status to the user, and stop. Do not run a standby cycle, do not create another `TASK_CYCLE_*.md`, do not re-probe exchanges for the sake of it, and do not rewrite the research artifacts to record that nothing changed.

Act **only** if the user does one of these:

1. **Explicitly authorizes validation and supplies an unrestricted network/proxy.** Then:
    - Run H1 exactly per the Cycle 4 spec in `research/HYPOTHESES.md`: Binance−Bybit, 2024-01-11 → 2025-03-17, 8h intervals, OOS ≥ 4 months from 2024-11-10, full fee/slippage modeling.
    - Document the access method (proxy/host) in the artifacts.
    - Apply the pre-registered H1 falsification tests; report failure modes, not performance guarantees.
    - Update `research/HYPOTHESES.md` and prepend one bullet to `research/SEARCH_LOG.md`.
2. **Explicitly requests a new hypothesis or a route beyond the four already explored.** Then survey it with the same research-only discipline: sources, mechanism, falsification tests, cost model, data-access spec. No data download unless access is real.

If neither happens, the correct outcome is: no file changes, no new cycles, a short status report.

## Hard constraints

- No performance guarantees, no trading recommendations, no datasets redistributed.
- Do not present re-verification of a closed project as research progress.
- `research/HANDOFF.md` must stay compact: one durable summary, not an append-only log of near-identical entries. If you do meaningfully change state, edit it in place and add at most one dated receipt line.

## Current facts you can rely on (verified 2026-11-20T00:51:54Z)

- Binance Futures `fundingRate`: HTTP 451 (RESTRICTED_LOCATION) — blocked.
- Bybit V5 `funding/history`: HTTP 403 (COUNTRY_BLOCKED) — blocked.
- Kraken spot ticker: HTTP 200 (sanity check only).
- `research/HYPOTHESES.md` md5 `38edf583b5d29c652407099c0ba33699`.
- Standby counter frozen at Cycle 3388 (547 consecutive no-op cycles, 2842–3388); Cycles 3389–3470 were handoff bookkeeping only.

## Result
(pending)
