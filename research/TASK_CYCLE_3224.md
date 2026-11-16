# TASK CYCLE 3223 — Standby/Closeout No-Op (research-only)

**Status:** PENDING
**Timestamp:** 2026-11-16T23:34:45Z
**Cycle:** 3223 (standby/closeout no-op)

## Read this first
The prior agent completed Cycle 3223 (`research/TASK_CYCLE_3222.md`) at 2026-11-16T23:34:45Z and advanced `research/HANDOFF.md` to "Cycle 3223 complete → Cycle 3224". This is the next bounded standby cycle.

Cycle 3223 also reconciled two prior bookkeeping defects: `research/TASK_CYCLE_3222.md` had been missing despite the Cycle 3221 closeout claim, and `research/TASK_CYCLE_3221.md` had remained PENDING. Both are now recorded transparently; do not silently rewrite that history.

This is a research-only repository: no backtests, no datasets, no performance metrics, no trading recommendations, and no changes to workflow/controller configuration.

## Task
Execute the standby/closeout no-op per `research/HANDOFF.md`. Do NOT retry blocked Binance/Bybit endpoints for data collection. Maintain research-only scope. Keep `research/HANDOFF.md`, `research/SEARCH_LOG.md`, `research/TASK_CYCLE_3222.md`, and `research/HYPOTHESES.md` consistent.

## Definition of Done
1. **Access sanity checks** (single lightweight probe per endpoint; record HTTP status only; do not store data):
   - Binance Futures `fundingRate` (BTCUSDT, limit=1) → expect HTTP 451 (RESTRICTED_LOCATION)
   - Bybit V5 `funding/history` (linear, BTCUSDT, limit=1) → expect HTTP 403 (COUNTRY_BLOCKED)
   - Kraken spot ticker (XBTUSD) → HTTP 200 (sanity check only, not in the Cycle 4 spec)
   Run with a fresh timestamp and record the actual statuses.

2. **Artifact review**: `research/HANDOFF.md`, `research/SEARCH_LOG.md`, `research/TASK_CYCLE_3222.md`, and `research/HYPOTHESES.md`. Confirm consistency on access labels, cycle numbering, and conclusions. Confirm `research/TASK_CYCLE_3222.md` Status = COMPLETE.

3. **`research/HYPOTHESES.md`**: leave unmodified unless a factual inconsistency is found. Known bookkeeping-only defects: duplicate Cycle 346 headings; out-of-order Cycle 2182/2185 headings; newest cycle entry Cycle 2211.

4. **`research/SEARCH_LOG.md`** has THREE summary locations; update ALL and verify agreement:
   - consolidated running heading near the top → Cycles 2842–3223 (382 consecutive standby cycles);
   - mid-file Earliest check / Last checked / Cycles covered block → Cycle 3224 / 2842–3223 / 382 cycles;
   - end-of-file Earliest check / Last checked / Cycles covered block → Cycle 3224 / 2842–3223 / 382 cycles.
   Prepend the Cycle 3224 closeout bullet and verify Cycle 3040–3222 coverage using the prefix `- **Cycle N closeout`.

5. **No empirical validation performed**; no datasets downloaded; no trading recommendations made. State this explicitly.

6. **Activation conditions check**: confirm neither occurred:
   - no unrestricted network/proxy is available to run H1 per Cycle 4 specs (Binance−Bybit, 2024-01-11–2025-03-17, 8h intervals, OOS ≥4 months from 2024-11-10) with full fee/slippage modeling;
   - no user request for a new hypothesis/route beyond the four discovered routes.

7. **Update `research/HANDOFF.md`**: add the Cycle 3224 completion entry, advance to Cycle 3224 complete → Cycle 3224, and update the access-status timestamp. Re-read it to verify the edit landed.

8. **Create `research/TASK_CYCLE_3224.md`** as the next initial task message (Status: PENDING). Verify it exists with `ls research/TASK_CYCLE_*.md` and re-read it. Mark this file COMPLETE only after steps 1–8 are actually done.

## Bookkeeping traps to avoid
- Update all three summary locations and grep for every `Last checked`, `Cycles covered`, and `Earliest check` occurrence.
- Check bullet coverage with `- **Cycle N closeout`, not `closeout:**`.
- Verify claimed files exist and claimed handoff edits actually landed; record a reconciliation note if fixing a prior false claim.

## Context
Project remains CLOSEOUT/STANDBY. Original Cycle 4 spec (Binance−Bybit, 2024-01-11–2025-03-17, 8h intervals, OOS ≥4 months from 2024-11-10) is unrunnable from this environment: Binance = RESTRICTED_LOCATION (HTTP 451), Bybit = COUNTRY_BLOCKED (HTTP 403), confirmed across 400+ cycles including the Cycle 3223 re-confirmation. Venue-substituted replications (Hyperliquid vs KuCoin for H1; Deribit for H2) falsified both hypotheses for tradability under documented costs.

## Activation conditions (only act if one occurs)
1. An unrestricted network/proxy becomes available → run H1 exactly per Cycle 4 specs with full fee/slippage modeling. Document the access method. This crosses into validation, so only do it if the user explicitly authorizes it.
2. The user explicitly requests a new hypothesis/route beyond the four discovered routes.

## Key constraints
- No performance guarantees or trading recommendations.
- No datasets to redistribute.
- Document any venue substitutions if new work is attempted.
- Update all research artifacts after the cycle.

## Access status at handoff (2026-11-16T23:34:45Z, Cycle 3223)
- Binance Futures fundingRate: HTTP 451 (RESTRICTED_LOCATION) — blocked
- Bybit V5 funding/history: HTTP 403 (COUNTRY_BLOCKED) — blocked
- Kraken spot ticker: HTTP 200 (reachable; sanity check only, not in spec)