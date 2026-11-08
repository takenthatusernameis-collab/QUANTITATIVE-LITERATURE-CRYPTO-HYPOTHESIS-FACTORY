# TASK CYCLE 2002 — Standby/Closeout No-Op (research-only)

**Status:** PENDING.

## Task
Standby/closeout no-op. Do NOT retry blocked Binance/Bybit endpoints for data collection. Maintain research-only scope.

## Required steps
1. Complete prior agent task from durable handoff (Cycle 2001 per `research/HANDOFF.md` / `research/TASK_CYCLE_2001.md`) as standby/closeout no-op.
2. Do NOT retry blocked Binance/Bybit endpoints for data collection.
3. Re-verify access (sanity checks only; no data collected):
   - Binance Futures fundingRate (BTCUSDT, limit=1) → expect HTTP 451 (RESTRICTED_LOCATION)
   - Bybit V5 funding/history (linear, BTCUSDT, limit=1) → expect HTTP 403 (COUNTRY_BLOCKED)
   - Kraken spot ticker (XBTUSD) → expect HTTP 200 (reachable, sanity only, not in spec)
4. Review `research/HANDOFF.md`, `research/SEARCH_LOG.md`, `research/TASK_CYCLE_2001.md`, `research/TASK_CYCLE_2002.md`, and `research/HYPOTHESES.md` for consistency.
5. No empirical validation; no datasets downloaded; no trading recommendations.
6. Check activation conditions; if neither occurs, remain in closeout.
   - (1) Unrestricted network/proxy available → run H1 per Cycle 4 specs.
   - (2) User explicitly requests new hypothesis/route beyond 4 discovered routes.
7. Mark `research/TASK_CYCLE_2002.md` complete, update `research/HANDOFF.md` (Cycle 2002 completion + Cycle 2003 next task), write `research/TASK_CYCLE_2003.md`, and prepend a `research/SEARCH_LOG.md` entry.

## Key constraints
- No performance guarantees or trading recommendations.
- No datasets to redistribute.
- Document any venue substitutions if new work is attempted.
- Update all research artifacts after the cycle.

## Context
Cycle 2001 completed as standby/closeout no-op. Project remains in CLOSEOUT/STANDBY. Four literature routes explored (Cycles 1–4); H1 (cross-venue funding spread persistence) and H2 (anchoring-intensity basis premium) synthesized. Original Cycle 4 spec (Binance−Bybit, 2024-01-11–2025-03-17, 8h, OOS ≥4 months from 2024-11-10) unrunnable from this environment: Binance = RESTRICTED_LOCATION (HTTP 451), Bybit = COUNTRY_BLOCKED (HTTP 403), confirmed across 400+ cycles including Cycles 664–2001. Venue-substituted replications (Hyperliquid vs KuCoin for H1; Deribit for H2) falsified both hypotheses for tradability under documented costs. No empirical validation on original spec; no trading recommendations.
