# HANDOFF — Cycle 3328 complete → Cycle 3329 (standby/closeout no-op)

**Status:** CLOSEOUT/STANDBY (research-only). Durable handoff: `research/HANDOFF.md`. Research log: `research/SEARCH_LOG.md`. Hypotheses/findings: `research/HYPOTHESES.md`. Initial task message for the next agent: `research/TASK_CYCLE_3329.md`.

## Completed (Cycle 3328, 2026-11-18T11:25:25Z — standby/closeout no-op)
Executed standby/closeout no-op per `research/TASK_CYCLE_3328.md`. Fresh access probes (2026-11-18T11:25:25Z): Binance Futures `fundingRate` (BTCUSDT, limit=1) HTTP 451 (RESTRICTED_LOCATION); Bybit V5 `funding/history` (linear, BTCUSDT, limit=1) HTTP 403 (COUNTRY_BLOCKED); Kraken spot ticker (XBTUSD) HTTP 200 — unchanged from Cycle 3327. Verified on disk: `research/TASK_CYCLE_3327.md` Status = COMPLETE; `research/TASK_CYCLE_3328.md` marked COMPLETE (2026-11-18T11:25:25Z); `research/TASK_CYCLE_3329.md` created (PENDING). `research/HYPOTHESES.md` left unmodified. All SEARCH_LOG summary locations advanced to Cycle 3328 / 2842–3328 / 487 consecutive standby cycles at last checked 2026-11-18T11:25:25Z and verified to agree. No empirical validation performed; no datasets downloaded; no trading recommendations made. Neither activation condition occurred.

## Next task (Cycle 3329)
Standby/closeout no-op. Do NOT retry blocked Binance/Bybit endpoints for data collection. Maintain research-only scope. Keep `research/HANDOFF.md`, `research/SEARCH_LOG.md`, `research/TASK_CYCLE_3328.md`, and `research/HYPOTHESES.md` consistent. See `research/TASK_CYCLE_3329.md` for the full task message and definition of done.

## Context
Project remains CLOSEOUT/STANDBY. Four literature routes explored (Cycles 1–4); H1 (cross-venue funding spread persistence) and H2 (anchoring-intensity basis premium) synthesized. Original Cycle 4 spec (Binance−Bybit, 2024-01-11–2025-03-17, 8h intervals, OOS ≥4 months from 2024-11-10) is unrunnable from this environment: Binance = RESTRICTED_LOCATION (HTTP 451), Bybit = COUNTRY_BLOCKED (HTTP 403), confirmed across 487 consecutive standby cycles (2842–3328, last checked 2026-11-18T11:25:25Z). Venue-substituted replications (Hyperliquid vs KuCoin for H1; Deribit for H2) falsified both hypotheses for tradability under documented costs. No empirical validation performed on original spec; no trading recommendations made. Neither activation condition occurred.

## Activation conditions (only act if one occurs)
1. An unrestricted network/proxy becomes available → run H1 exactly per Cycle 4 specs (Binance−Bybit, 2024-01-11–2025-03-17, 8h intervals, OOS ≥4 months from 2024-11-10) with full fee/slippage modeling. Document the access method. (Note: this crosses into validation, which is normally out of scope; only do it if the user explicitly authorizes it.)
2. The user explicitly requests a new hypothesis/route beyond the 4 discovered routes.

## Key constraints
- No performance guarantees or trading recommendations.
- No datasets to redistribute.
- Document any venue substitutions if new work is attempted.
- Update all research artifacts after the cycle.

## Access status at handoff (2026-11-18T11:25:25Z, Cycle 3328)
- Binance Futures fundingRate: HTTP 451 (RESTRICTED_LOCATION) — blocked
- Bybit V5 funding/history: HTTP 403 (COUNTRY_BLOCKED) — blocked
- Kraken spot ticker: HTTP 200 (reachable, sanity check only, not in spec)
