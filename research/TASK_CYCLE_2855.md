# TASK CYCLE 2855 — Standby/Closeout No-Op (research-only)

**Status:** PENDING (handoff written 2026-11-13T16:36:58Z).

**Read this first:** The prior agent completed Cycle 2854 (`research/TASK_CYCLE_2854.md`). Your job is to perform the same bounded standby cycle for Cycle 2855 and then advance the handoff to Cycle 2856. This is a research-only repository: do NOT run backtests, download datasets, or produce performance numbers.

## Mission / scope boundary
- Allowed: literature research, hypothesis generation, source appraisal, and documenting free-data feasibility.
- Forbidden: empirical validation, dataset download/redistribution, strategy/backtest code, trading recommendations, infrastructure/CI changes.
- The project is in CLOSEOUT/STANDBY. There is no new research avenue to pursue unless an activation condition below occurs.

## Your task (Cycle 2855)
1. **Access sanity checks only (no data stored).** Issue a single lightweight probe per endpoint and record the HTTP status only; do not collect or persist datasets:
   - Binance Futures `fundingRate` (BTCUSDT, limit=1) — expect HTTP 451 RESTRICTED_LOCATION.
   - Bybit V5 `funding/history` (linear, BTCUSDT, limit=1) — expect HTTP 403 COUNTRY_BLOCKED.
   - Kraken spot ticker (XBTUSD) — expect HTTP 200 (sanity check only, not in the Cycle 4 spec).
   - Do NOT retry blocked endpoints in a loop or attempt to bypass geo-blocks.
2. **Review for consistency:** `research/HANDOFF.md`, `research/SEARCH_LOG.md`, `research/TASK_CYCLE_2854.md`, `research/TASK_CYCLE_2855.md`, and `research/HYPOTHESES.md`. Confirm no contradictions in access labels, cycle numbering, or conclusions. Also confirm the Status line of any just-completed `TASK_CYCLE_*.md` reads COMPLETE.
3. **Close the cycle:**
   - Mark `research/TASK_CYCLE_2855.md` COMPLETE with a timestamped outcome section.
   - Update `research/HANDOFF.md` (Cycle 2855 complete → Cycle 2856), including the new access-status timestamp.
   - Create `research/TASK_CYCLE_2856.md` (next standby no-op).
   - Prepend a Cycle 2855 entry to `research/SEARCH_LOG.md`.
4. Do not modify `research/HYPOTHESES.md` unless a review actually finds a factual inconsistency (recent standby cycles have not needed to).

## Context
- Four literature routes explored (Cycles 1–4). H1 (cross-venue funding spread persistence) and H2 (anchoring-intensity basis premium) were synthesized.
- Original Cycle 4 spec (Binance−Bybit, 2024-01-11–2025-03-17, 8h intervals, OOS ≥4 months from 2024-11-10) is unrunnable from this environment: Binance = RESTRICTED_LOCATION (HTTP 451), Bybit = COUNTRY_BLOCKED (HTTP 403), confirmed across 400+ cycles including recent re-confirmations (last 2026-11-13T16:36:58Z Cycle 2854).
- Venue-substituted replications (Hyperliquid vs KuCoin for H1; Deribit for H2) falsified both hypotheses for tradability under documented costs.
- No empirical validation has ever been performed on the original spec. No trading recommendations have been made.

## Only act if one of these occurs
1. An unrestricted network/proxy becomes available → run H1 exactly per Cycle 4 specs (Binance−Bybit, 2024-01-11–2025-03-17, 8h intervals, OOS ≥4 months from 2024-11-10) with full fee/slippage modeling. Document the access method. (Note: this crosses into validation, which is normally out of scope; only do it if the user explicitly authorizes it.)
2. The user explicitly requests a new hypothesis/route beyond the 4 discovered routes.

## Key constraints
- No performance guarantees or trading recommendations.
- No datasets to redistribute.
- Document any venue substitutions if new work is attempted.
- Update all research artifacts after the cycle.

## Definition of done (Cycle 2855)
- `research/TASK_CYCLE_2855.md` marked COMPLETE with timestamp and access results.
- `research/HANDOFF.md` advanced to Cycle 2856 with updated access-status timestamp.
- `research/TASK_CYCLE_2856.md` created.
- Cycle 2855 entry prepended to `research/SEARCH_LOG.md`.
- All artifacts internally consistent; no out-of-scope work performed.

## Access status at handoff (2026-11-13T16:36:58Z, Cycle 2854)
- Binance Futures fundingRate: HTTP 451 (RESTRICTED_LOCATION) — blocked
- Bybit V5 funding/history: HTTP 403 (COUNTRY_BLOCKED) — blocked
- Kraken spot ticker: HTTP 200 (reachable, sanity check only, not in spec)
