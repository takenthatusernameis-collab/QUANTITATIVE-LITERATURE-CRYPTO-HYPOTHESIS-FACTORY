# TASK CYCLE 3568 — Initial task message for the next agent

**Status:** COMPLETE (2026-11-21T02:42:05Z)
**Type:** manual handoff (not a standby cycle; nothing is scheduled)

## Result

Read the durable handoff `research/HANDOFF.md` and confirmed the closed/standby state: project CLOSED / STANDBY, research-only, no automatic cycles, nothing runs until the user acts. Both activation conditions remain untriggered — no unrestricted network/proxy supplied and no new hypothesis or route requested. H1 (Binance−Bybit funding-spread persistence) and H2 (anchoring-intensity basis premium) remain falsified for tradability under documented costs via venue-substituted data (Hyperliquid/KuCoin for H1; Deribit for H2); original Binance/Bybit tests blocked (HTTP 451 / HTTP 403; Kraken spot reachable but out of spec). Verified on disk: `research/HYPOTHESES.md` md5 `38edf583b5d29c652407099c0ba33699` (matches); `research/SEARCH_LOG.md` md5 `d0183d24178d7e9c3621f8157bdebc8f` (differs from the stale Cycle 3566/3567 receipt value `153e40f27378bd54403894258da2d10c` — pre-existing record discrepancy, not changed this cycle). Correct outcome: no research edits, no new cycles beyond the canonical next-agent task message, short status report. Standby counter frozen at Cycle 3388 (547 consecutive no-op cycles, 2842–3388); Cycles 3389–3568 were handoff bookkeeping only.
**Read first:** `research/HANDOFF.md` — it is the single durable summary. This file only tells you what to do (and not do) now.

## Situation in one paragraph

The project is CLOSED / STANDBY and research-only. Four literature routes were surveyed; H1 (Binance−Bybit funding-spread persistence) and H2 (anchoring-intensity basis premium) were synthesized and then falsified **for tradability** under documented costs using venue-substituted data (Hyperliquid/KuCoin for H1, Deribit for H2). H1 was never tested on its original Binance/Bybit spec because both endpoints are geo-blocked from this environment (Binance HTTP 451, Bybit HTTP 403; Kraken spot returns 200 but is not part of the spec). Full detail and numbers: `research/HYPOTHESES.md`.

## Your task

**Default: do nothing new in research.** Read `research/HANDOFF.md`, confirm the closed state, and report it to the user in a few lines. Do not run a standby cycle, do not re-probe exchanges as "progress", and do not edit `HYPOTHESES.md` or `SEARCH_LOG.md` merely to record that nothing changed.

Act **only** if the user does one of these:

1. **Explicitly authorizes validation AND an unrestricted network/proxy is supplied.** Then:
    - Run H1 exactly per the Cycle 4 spec in `research/HYPOTHESES.md`: Binance−Bybit, 2024-01-11 → 2025-03-17, 8h intervals, OOS ≥ 4 months from 2024-11-10, full fee/slippage modeling.
    - Document the access method (proxy/host) in the artifacts.
    - Apply the pre-registered H1 falsification tests; report failure modes, not performance guarantees.
    - Update `research/HYPOTHESES.md` and prepend one bullet to `research/SEARCH_LOG.md`.
2. **Explicitly requests a new hypothesis or a route beyond the four already explored.** Then survey it with the same research-only discipline: sources, mechanism, falsification tests, cost model, data-access spec. No data download unless access is real.
3. **Explicitly asks to retire or restructure the project** (e.g. archive the `TASK_CYCLE_*.md` chain, keep only the canonical task file, or delete the handoff boilerplate). Then do exactly that requested bookkeeping and stop — do not add research content.

If none of these happens, the correct outcome is: no research file changes, no new cycles, a short status report.

## Bookkeeping rule (only when the user asks for a handoff refresh)

- Mark the current `TASK_CYCLE_*.md` COMPLETE with a short `## Result` block, write the next `TASK_CYCLE_<n+1>.md`, and edit `research/HANDOFF.md` in place: advance the header timestamp and next-agent pointer and keep exactly one dated receipt.
- `research/HANDOFF.md` must stay compact — one durable summary, never an append-only log of near-identical entries.

## Hard constraints

- No performance guarantees, no trading recommendations, no datasets redistributed.
- Do not present re-verification of a closed project as research progress.
- Do not create `TASK_CYCLE_*.md` files except as the single canonical next-agent task message when a handoff is explicitly requested.

## Current facts you can rely on (verified 2026-11-21T02:42:05Z)

- Binance Futures `fundingRate` (BTCUSDT, limit=1): HTTP 451 (RESTRICTED_LOCATION) — blocked.
- Bybit V5 `funding/history` (linear, BTCUSDT, limit=1): HTTP 403 (COUNTRY_BLOCKED) — blocked.
- Kraken spot ticker (XBTUSD): HTTP 200 (sanity check only; not part of the H1 spec).
- Access facts last probed 2026-11-20T11:17:20Z; not re-probed during Cycle 3568 (closed-state rule).
- `research/HYPOTHESES.md` md5 `38edf583b5d29c652407099c0ba33699`.
- `research/SEARCH_LOG.md` md5 `d0183d24178d7e9c3621f8157bdebc8f`.
- Standby counter frozen at Cycle 3388 (547 consecutive no-op cycles, 2842–3388); Cycles 3389–3568 were handoff bookkeeping only.
