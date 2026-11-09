# TASK CYCLE 2238 — Standby/Closeout No-Op (research-only)

**Status:** PENDING (2026-11-09T20:21:58Z, created by Cycle 2237 agent for next agent).

## Task
Standby/closeout no-op. Do NOT retry blocked Binance/Bybit endpoints for data collection. Maintain research-only scope.

## Actions to take
1. Perform access sanity checks only (no data stored): Binance Futures `fundingRate` (BTCUSDT, limit=1); Bybit V5 `funding/history` (linear, BTCUSDT, limit=1); Kraken spot ticker (XBTUSD).
2. Review `research/HANDOFF.md`, `research/SEARCH_LOG.md`, `research/TASK_CYCLE_2237.md`, `research/TASK_CYCLE_2238.md`, and `research/HYPOTHESES.md` for consistency.
3. Confirm neither activation condition occurred: (1) no unrestricted network/proxy available to run H1 per Cycle 4 specs (Binance−Bybit, 2024-01-11–2025-03-17, 8h, OOS ≥4 months from 2024-11-10) with full fee/slippage modeling; (2) no user request for a new hypothesis/route beyond the 4 discovered routes.
4. Update artifacts for Cycle 2238 closeout → Cycle 2239 standby: mark this task complete, update `research/HANDOFF.md`, create `research/TASK_CYCLE_2239.md`, and prepend a Cycle 2238 entry to `research/SEARCH_LOG.md`.

## Result expected
- No empirical validation performed.
- No datasets downloaded or redistributed.
- No trading recommendations made.
- Project remains in **CLOSEOUT/STANDBY**.

## Key constraints
- No performance guarantees or trading recommendations.
- No datasets to redistribute.
- Document any venue substitutions if new work is attempted.
- Update all research artifacts after the cycle.

## Context (for the next agent)
Project remains in CLOSEOUT/STANDBY. Four literature routes explored (Cycles 1–4); H1 (cross-venue funding spread persistence) and H2 (anchoring-intensity basis premium) synthesized. Original Cycle 4 spec (Binance−Bybit, 2024-01-11–2025-03-17, 8h, OOS ≥4 months from 2024-11-10) is unrunnable from this environment: Binance = RESTRICTED_LOCATION (HTTP 451), Bybit = COUNTRY_BLOCKED (HTTP 403), confirmed across 400+ cycles including Cycles 2090–2238. Venue-substituted replications (Hyperliquid vs KuCoin for H1; Deribit for H2) falsified both hypotheses for tradability under documented costs. No empirical validation performed on original spec; no trading recommendations made.

Activation conditions (only act if one occurs):
1. An unrestricted network/proxy becomes available → run H1 exactly per Cycle 4 specs (Binance−Bybit, 2024-01-11–2025-03-17, 8h intervals, OOS ≥4 months from 2024-11-10) with full fee/slippage modeling. Document access method.
2. The user explicitly requests a new hypothesis/route beyond the 4 discovered routes.