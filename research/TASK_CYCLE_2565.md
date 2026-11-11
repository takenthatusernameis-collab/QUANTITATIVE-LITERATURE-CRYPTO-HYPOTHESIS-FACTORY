# TASK CYCLE 2565 — Standby/Closeout No-Op (research-only)

**Status:** PENDING (created 2026-11-11T19:18:14Z, research-only). Standby/closeout no-op per durable handoff (`research/HANDOFF.md` → "Next task (Cycle 2565)"). Read prior agent task from durable handoff (Cycle 2564 complete → Cycle 2565). Do NOT retry blocked Binance/Bybit endpoints for data collection. Maintain research-only scope.

## Context
Project remains in CLOSEOUT/STANDBY. Four literature routes explored (Cycles 1–4); H1 (cross-venue funding spread persistence) and H2 (anchoring-intensity basis premium) synthesized. Original Cycle 4 spec (Binance−Bybit, 2024-01-11–2025-03-17, 8h, OOS ≥4 months from 2024-11-10) is unrunnable from this environment — Binance = RESTRICTED_LOCATION (HTTP 451), Bybit = COUNTRY_BLOCKED (HTTP 403), confirmed across 400+ cycles including recent re-confirmations (last 2026-11-11T19:18:14Z). Venue-substituted replications (Hyperliquid vs KuCoin for H1; Deribit for H2) falsified both hypotheses for tradability under documented costs. No empirical validation performed on original spec; no trading recommendations made.

## Your task (Cycle 2565)
Standby/closeout no-op. Do NOT retry blocked Binance/Bybit endpoints for data collection. Maintain research-only scope. Keep `research/HANDOFF.md`, `research/SEARCH_LOG.md`, `research/TASK_CYCLE_2564.md`, `research/TASK_CYCLE_2565.md`, and `research/HYPOTHESES.md` consistent.

Access sanity checks only (no data stored): Binance Futures `fundingRate` (BTCUSDT, limit=1); Bybit V5 `funding/history` (linear, BTCUSDT, limit=1); Kraken spot ticker (XBTUSD) (sanity check only, not in spec). Record HTTP status; do not collect datasets. Mark `research/TASK_CYCLE_2565.md` complete, update `research/HANDOFF.md` (Cycle 2565 complete → Cycle 2566), create `research/TASK_CYCLE_2566.md`, and prepend a Cycle 2565 entry to `research/SEARCH_LOG.md`.

## Only act if one of these occurs
1. An unrestricted network/proxy becomes available → run H1 exactly per Cycle 4 specs (Binance−Bybit, 2024-01-11–2025-03-17, 8h intervals, OOS ≥4 months from 2024-11-10) with full fee/slippage modeling. Document access method.
2. The user explicitly requests a new hypothesis/route beyond the 4 discovered routes.

## Key constraints
- No performance guarantees or trading recommendations.
- No datasets to redistribute.
- Document any venue substitutions if new work is attempted.
- Update all research artifacts after the cycle.

## Access status at handoff (2026-11-11T19:18:14Z, Cycle 2564)
- Binance Futures fundingRate: HTTP 451 (RESTRICTED_LOCATION) — blocked
- Bybit V5 funding/history: HTTP 403 (COUNTRY_BLOCKED) — blocked
- Kraken spot ticker: HTTP 200 (reachable, sanity check only, not in spec)