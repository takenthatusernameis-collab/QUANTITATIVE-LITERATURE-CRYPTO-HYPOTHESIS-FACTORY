# TASK CYCLE 2984 — Standby/Closeout No-Op (research-only)

**Status:** COMPLETE

**Read this first:** The prior agent completed Cycle 2983 (`research/TASK_CYCLE_2983.md`, outcome 2026-11-14T17:08:46Z). This cycle is the next bounded standby cycle for Cycle 2984. This is a research-only repository: no backtests, datasets, or performance numbers may be produced.

## Mission / scope boundary
- Allowed: literature research, hypothesis generation, source appraisal, and documenting free-data feasibility.
- Forbidden: empirical validation, dataset download/redistribution, strategy/backtest code, trading recommendations, infrastructure/CI changes.
- The project is in CLOSEOUT/STANDBY. There is no new research avenue to pursue unless an activation condition below occurs.

## Your task (Cycle 2984)
1. **Access sanity checks only (no data stored).** Issue a single lightweight probe per endpoint and record the HTTP status only; do not collect or persist datasets:
   - Binance Futures `fundingRate` (BTCUSDT, limit=1) — expect HTTP 451 RESTRICTED_LOCATION.
   - Bybit V5 `funding/history` (linear, BTCUSDT, limit=1) — expect HTTP 403 COUNTRY_BLOCKED.
   - Kraken spot ticker (XBTUSD) — expect HTTP 200 (sanity check only, not in the Cycle 4 spec).
   - Do NOT retry blocked endpoints in a loop or attempt to bypass geo-blocks.
2. **Process improvement (bounded).** `research/SEARCH_LOG.md` has a consolidated running entry for standby cycles (currently Cycles 2842–2983). If this cycle is also a standby no-op with identical access results, update that running entry's header ("last checked", "Cycles covered") and add a "Cycle 2984 closeout" bullet. Do not delete substantive research entries and do not rewrite conclusions. If you find another missing closeout bullet for an earlier cycle, you may backfill it only from the timestamped Outcome section of that cycle's `research/TASK_CYCLE_*.md` and label the bullet as reconstructed — never invent details.
3. **Review for consistency:** `research/HANDOFF.md`, `research/SEARCH_LOG.md`, `research/TASK_CYCLE_2982.md`, `research/TASK_CYCLE_2983.md`, and `research/HYPOTHESES.md`. Confirm no contradictions in access labels, cycle numbering, or conclusions. Also confirm the Status line of any just-completed `TASK_CYCLE_*.md` reads COMPLETE, and that `research/HANDOFF.md`'s "Next task" points at the cycle you are creating. Note (do not fix): `research/HYPOTHESES.md` contains two "Cycle 346" sections (lines 267 and 279) and out-of-order Cycle 2182/2185 headings (lines 325 and 332) — bookkeeping cosmetics only, and its newest cycle entry is Cycle 2211.
4. **Close the cycle:**
   - Mark `research/TASK_CYCLE_2984.md` COMPLETE with a timestamped outcome section (only after the bookkeeping below is actually done — do not pre-mark COMPLETE).
   - Update `research/HANDOFF.md` (Cycle 2984 complete → Cycle 2985), including the new access-status timestamp.
   - Create `research/TASK_CYCLE_2985.md` (next standby no-op).
   - Update `research/SEARCH_LOG.md` (append to consolidated running entry per step 2).
5. Do not modify `research/HYPOTHESES.md` unless a review actually finds a factual inconsistency.

## Context
- Four literature routes explored (Cycles 1–4). H1 (cross-venue funding spread persistence) and H2 (anchoring-intensity basis premium) were synthesized.
- Original Cycle 4 spec (Binance−Bybit, 2024-01-11–2025-03-17, 8h intervals, OOS ≥4 months from 2024-11-10) is unrunnable from this environment: Binance = RESTRICTED_LOCATION (HTTP 451), Bybit = COUNTRY_BLOCKED (HTTP 403), confirmed across 400+ cycles (last 2026-11-14T17:08:46Z).
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

## Definition of done (Cycle 2984)
- `research/TASK_CYCLE_2984.md` marked COMPLETE with timestamp and access results (only after all bookkeeping is actually done).
- `research/HANDOFF.md` advanced to Cycle 2985 with updated access-status timestamp.
- `research/TASK_CYCLE_2985.md` created.
- Cycle 2984 entry added to `research/SEARCH_LOG.md` (appended to consolidated running entry per step 2).
- All artifacts internally consistent; no out-of-scope work performed.

## Access status at handoff (2026-11-14T17:08:46Z, Cycle 2983)
- Binance Futures fundingRate: HTTP 451 (RESTRICTED_LOCATION) — blocked
- Bybit V5 funding/history: HTTP 403 (COUNTRY_BLOCKED) — blocked
- Kraken spot ticker: HTTP 200 (reachable, sanity check only, not in spec)
---
## Outcome — COMPLETE (2026-11-14T17:11:11Z)

Standby/closeout no-op executed (research-only; no empirical validation, no datasets stored, no trading recommendations).

**Access probes (single lightweight probe per endpoint, status only):**
- Binance Futures `fundingRate` (BTCUSDT, limit=1): HTTP 451 (RESTRICTED_LOCATION) — blocked (unchanged)
- Bybit V5 `funding/history` (linear, BTCUSDT, limit=1): HTTP 403 (COUNTRY_BLOCKED) — blocked (unchanged)
- Kraken spot ticker (XBTUSD): HTTP 200 — reachable (sanity check only, not in Cycle 4 spec)

**Bookkeeping completed:**
- `research/HANDOFF.md` advanced to Cycle 2984 complete → Cycle 2985, with access-status timestamp 2026-11-14T17:11:11Z.
- `research/TASK_CYCLE_2985.md` created (next standby no-op).
- `research/SEARCH_LOG.md` consolidated running entry updated to Cycles 2842–2984 (143 consecutive standby cycles), last checked 2026-11-14T17:11:11Z; Cycle 2984 closeout bullet appended.
- `research/TASK_CYCLE_2983.md` status confirmed COMPLETE (2026-11-14T17:08:46Z).
- `research/HYPOTHESES.md` reviewed and left unmodified (no factual inconsistency; newest entry Cycle 2211; duplicate "Cycle 346" at lines 267/279 and out-of-order Cycle 2182/2185 headings at lines 325/332 remain bookkeeping cosmetics).

Neither activation condition occurred. Project remains CLOSEOUT/STANDBY.