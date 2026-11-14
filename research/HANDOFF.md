# HANDOFF — Cycle 2950 complete → Cycle 2951 (standby/closeout no-op)

**Status:** CLOSEOUT/STANDBY (research-only). Durable handoff: `research/HANDOFF.md`. Research log: `research/SEARCH_LOG.md`. Hypotheses/findings: `research/HYPOTHESES.md`. Initial task message: `research/TASK_CYCLE_2951.md`.

## Completed (Cycle 2950, 2026-11-14T11:16:32Z)
Executed standby/closeout no-op per durable handoff (`research/HANDOFF.md` / `research/TASK_CYCLE_2950.md`). Access sanity checks only (single lightweight probe per endpoint, no data stored, 2026-11-14T11:16:32Z): Binance Futures `fundingRate` (BTCUSDT, limit=1) HTTP 451 (RESTRICTED_LOCATION); Bybit V5 `funding/history` (linear, BTCUSDT, limit=1) HTTP 403 (COUNTRY_BLOCKED); Kraken spot ticker (XBTUSD) HTTP 200 (reachable, sanity check only, not in Cycle 4 spec). Access status unchanged from Cycle 2949. Reviewed `research/HANDOFF.md`, `research/SEARCH_LOG.md`, `research/TASK_CYCLE_2949.md`, `research/TASK_CYCLE_2950.md`, and `research/HYPOTHESES.md`. Artifacts consistent on access labels, cycle numbering, and conclusions. `research/TASK_CYCLE_2949.md` Status confirmed COMPLETE (2026-11-14T10:28:29Z). `research/HYPOTHESES.md` left unmodified (no factual inconsistency found; newest cycle entry Cycle 2211; known bookkeeping-only defects: duplicate "Cycle 346" and out-of-order Cycle 2182/2185 headings — numbering cosmetics, not factual claims). Consolidated `research/SEARCH_LOG.md` running entry updated to Cycles 2842–2950 (109 consecutive standby cycles) with "last checked" 2026-11-14T11:16:32Z; Cycle 2950 closeout bullet added. Activation conditions: (1) no unrestricted network/proxy available to run H1 per Cycle 4 specs (Binance−Bybit, 2024-01-11–2025-03-17, 8h intervals, OOS ≥4 months from 2024-11-10) with full fee/slippage modeling; (2) no user request for a new hypothesis/route beyond the 4 discovered routes. Project remains CLOSEOUT/STANDBY.

## Previous (Cycle 2949, 2026-11-14T10:28:29Z)
Executed standby/closeout no-op per durable handoff (`research/HANDOFF.md` / `research/TASK_CYCLE_2949.md`). Access sanity checks only (single lightweight probe per endpoint, no data stored, 2026-11-14T10:28:29Z): Binance Futures `fundingRate` (BTCUSDT, limit=1) HTTP 451 (RESTRICTED_LOCATION); Bybit V5 `funding/history` (linear, BTCUSDT, limit=1) HTTP 403 (COUNTRY_BLOCKED); Kraken spot ticker (XBTUSD) HTTP 200 (reachable, sanity check only, not in Cycle 4 spec). Access status unchanged from Cycle 2948. Reviewed `research/HANDOFF.md`, `research/SEARCH_LOG.md`, `research/TASK_CYCLE_2948.md`, `research/TASK_CYCLE_2949.md`, and `research/HYPOTHESES.md`. Artifacts consistent on access labels, cycle numbering, and conclusions. `research/TASK_CYCLE_2948.md` Status confirmed COMPLETE (2026-11-14T10:26:39Z). `research/HYPOTHESES.md` left unmodified (no factual inconsistency found; newest cycle entry Cycle 2211; known bookkeeping-only defects: duplicate "Cycle 346" and out-of-order Cycle 2182/2185 headings — numbering cosmetics, not factual claims). Consolidated `research/SEARCH_LOG.md` running entry updated to Cycles 2842–2949 (108 consecutive standby cycles) with "last checked" 2026-11-14T10:28:29Z; Cycle 2949 closeout bullet added. Activation conditions: (1) no unrestricted network/proxy available to run H1 per Cycle 4 specs (Binance−Bybit, 2024-01-11–2025-03-17, 8h intervals, OOS ≥4 months from 2024-11-10) with full fee/slippage modeling; (2) no user request for a new hypothesis/route beyond the 4 discovered routes. Project remains CLOSEOUT/STANDBY.

## Next task (Cycle 2951)
Standby/closeout no-op. Do NOT retry blocked Binance/Bybit endpoints for data collection. Maintain research-only scope. Keep `research/HANDOFF.md`, `research/SEARCH_LOG.md`, `research/TASK_CYCLE_2950.md`, `research/TASK_CYCLE_2951.md`, and `research/HYPOTHESES.md` consistent. See `research/TASK_CYCLE_2951.md` for the full task message and definition of done.

## Context
Project remains in CLOSEOUT/STANDBY. Four literature routes explored (Cycles 1–4); H1 (cross-venue funding spread persistence) and H2 (anchoring-intensity basis premium) synthesized. Original Cycle 4 spec (Binance−Bybit, 2024-01-11–2025-03-17, 8h intervals, OOS ≥4 months from 2024-11-10) is unrunnable from this environment: Binance = RESTRICTED_LOCATION (HTTP 451), Bybit = COUNTRY_BLOCKED (HTTP 403), confirmed across 400+ cycles including recent re-confirmations (last 2026-11-14T11:16:32Z Cycle 2950). Venue-substituted replications (Hyperliquid vs KuCoin for H1; Deribit for H2) falsified both hypotheses for tradability under documented costs. No empirical validation performed on original spec; no trading recommendations made. Neither activation condition occurred.

## Activation conditions (only act if one occurs)
1. An unrestricted network/proxy becomes available → run H1 exactly per Cycle 4 specs (Binance−Bybit, 2024-01-11–2025-03-17, 8h intervals, OOS ≥4 months from 2024-11-10) with full fee/slippage modeling. Document the access method. (Note: this crosses into validation, which is normally out of scope; only do it if the user explicitly authorizes it.)
2. The user explicitly requests a new hypothesis/route beyond the 4 discovered routes.

## Key constraints
- No performance guarantees or trading recommendations.
- No datasets to redistribute.
- Document any venue substitutions if new work is attempted.
- Update all research artifacts after the cycle.

## Access status at handoff (2026-11-14T11:16:32Z, Cycle 2950)
- Binance Futures fundingRate: HTTP 451 (RESTRICTED_LOCATION) — blocked
- Bybit V5 funding/history: HTTP 403 (COUNTRY_BLOCKED) — blocked
- Kraken spot ticker: HTTP 200 (reachable, sanity check only, not in spec)
