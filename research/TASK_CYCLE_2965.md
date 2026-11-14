# TASK CYCLE 2965 — Standby/Closeout No-Op (research-only)

**Status:** PENDING

**Read this first:** The prior agent completed Cycle 2964 (`research/TASK_CYCLE_2964.md`, 2026-11-14T13:29:39Z). This cycle is the next bounded standby cycle for Cycle 2965. This is a research-only repository: no backtests, datasets, or performance numbers may be produced.

## Mission / scope boundary
- Allowed: literature research, hypothesis generation, source appraisal, and documenting free-data feasibility.
- Forbidden: empirical validation, dataset download/redistribution, strategy/backtest code, trading recommendations, infrastructure/CI changes.
- The project is in CLOSEOUT/STANDBY. There is no new research avenue to pursue unless an activation condition below occurs.

## Your task (Cycle 2965)
1. **Access sanity checks only (no data stored).** Issue a single lightweight probe per endpoint and record the HTTP status only; do not collect or persist datasets:
   - Binance Futures `fundingRate` (BTCUSDT, limit=1) — expect HTTP 451 RESTRICTED_LOCATION.
   - Bybit V5 `funding/history` (linear, BTCUSDT, limit=1) — expect HTTP 403 COUNTRY_BLOCKED.
   - Kraken spot ticker (XBTUSD) — expect HTTP 200 (sanity check only, not in the Cycle 4 spec).
   - Do NOT retry blocked endpoints in a loop or attempt to bypass geo-blocks.
2. **Process improvement (bounded).** `research/SEARCH_LOG.md` has a consolidated running entry for standby cycles (currently Cycles 2842–2964). If this cycle is also a standby no-op with identical access results, update that running entry's header ("last checked", "Cycles covered") and add a "Cycle 2965 closeout" bullet. Do not delete substantive research entries and do not rewrite conclusions. If you find another missing closeout bullet for an earlier cycle, you may backfill it only from the timestamped Outcome section of that cycle's `research/TASK_CYCLE_*.md` and label the bullet as reconstructed — never invent details.
3. **Review for consistency:** `research/HANDOFF.md`, `research/SEARCH_LOG.md`, `research/TASK_CYCLE_2964.md`, `research/TASK_CYCLE_2965.md`, and `research/HYPOTHESES.md`. Confirm no contradictions in access labels, cycle numbering, or conclusions. Also confirm the Status line of any just-completed `TASK_CYCLE_*.md` reads COMPLETE, and that `research/HANDOFF.md`'s "Next task" points at the cycle you are creating. Note (do not fix): `research/HYPOTHESES.md` contains two "Cycle 346" sections and out-of-order Cycle 2182/2185 headings — bookkeeping cosmetics only, and its newest cycle entry is Cycle 2211.
4. **Close the cycle:**
   - Mark `research/TASK_CYCLE_2965.md` COMPLETE with a timestamped outcome section (only after the bookkeeping below is actually done — do not pre-mark COMPLETE).
   - Update `research/HANDOFF.md` (Cycle 2965 complete → Cycle 2966), including the new access-status timestamp.
   - Create `research/TASK_CYCLE_2966.md` (next standby no-op).
   - Update `research/SEARCH_LOG.md` (append to consolidated running entry per step 2).
5. Do not modify `research/HYPOTHESES.md` unless a review actually finds a factual inconsistency.

## Context
- Four literature routes explored (Cycles 1–4). H1 (cross-venue funding spread persistence) and H2 (anchoring-intensity basis premium) were synthesized.
- Original Cycle 4 spec (Binance−Bybit, 2024-01-11–2025-03-17, 8h intervals, OOS ≥4 months from 2024-11-10) is unrunnable from this environment: Binance = RESTRICTED_LOCATION (HTTP 451), Bybit = COUNTRY_BLOCKED (HTTP 403), confirmed across 400+ cycles (last 2026-11-14T13:29:39Z Cycle 2964).
- Venue-substituted replications (Hyperliquid vs KuCoin for H1; Deribit for H2) falsified both hypotheses for tradability under documented costs.
- No empirical validation has ever been performed on the original spec. No trading recommendations have been made.

## Only act if one of these occurs
1. An unrestricted network/proxy becomes available → run H1 exactly per Cycle 4 specs (Binance−Bybit, 2024-01-11–2025-03-17, 8h intervals, OOS ≥4 months from 2024-11-10) with full fee/slippage modeling. Document the access method. (Only if user explicitly authorizes; validation is normally out of scope.)
2. The user explicitly requests a new hypothesis/route beyond the 4 discovered routes.

## Key constraints
- No performance guarantees or trading recommendations.
- No datasets to redistribute.
- Document any venue substitutions if new work is attempted.
- Update all research artifacts after the cycle.

## Definition of done (Cycle 2965)
- `research/TASK_CYCLE_2965.md` marked COMPLETE with timestamp and access results (only after all bookkeeping is actually done).
- `research/HANDOFF.md` advanced to Cycle 2966 with updated access-status timestamp.
- `research/TASK_CYCLE_2966.md` created.
- Cycle 2965 entry added to `research/SEARCH_LOG.md` (appended to consolidated running entry per step 2).
- All artifacts internally consistent; no out-of-scope work performed.

## Access status at handoff (2026-11-14T13:29:39Z, Cycle 2964)
- Binance Futures fundingRate: HTTP 451 (RESTRICTED_LOCATION) — blocked
- Bybit V5 funding/history: HTTP 403 (COUNTRY_BLOCKED) — blocked
- Kraken spot ticker: HTTP 200 (reachable, sanity check only, not in spec)
