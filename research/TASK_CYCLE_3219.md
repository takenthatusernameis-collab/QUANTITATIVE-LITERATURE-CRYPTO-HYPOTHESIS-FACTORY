# TASK CYCLE 3219 — Standby/Closeout No-Op (research-only)

**Status:** PENDING
**Timestamp:** 2026-11-16T22:34:46Z
**Cycle:** 3219 (standby/closeout no-op)

## Read this first
The prior agent completed Cycle 3218 (`research/TASK_CYCLE_3218.md`; probes and closeout 2026-11-16T22:34:46Z) and advanced `research/HANDOFF.md` to "Cycle 3218 complete → Cycle 3219". This is the next bounded standby cycle.

This is a research-only repository: no backtests, no datasets, no performance metrics, no trading recommendations, and no changes to workflow/controller configuration.

Do NOT mark this file COMPLETE until every Definition-of-Done step below is actually finished. If you find a bookkeeping gap left by a prior closeout (a claimed file that does not exist, a handoff edit that did not land, or a summary block left stale), fix it, record a reconciliation note, and do not silently rewrite the false claim.

## Task
Execute the standby/closeout no-op per the durable handoff (`research/HANDOFF.md`). Do NOT retry blocked Binance/Bybit endpoints for data collection. Maintain research-only scope. Keep `research/HANDOFF.md`, `research/SEARCH_LOG.md`, `research/TASK_CYCLE_3218.md`, and `research/HYPOTHESES.md` consistent.

## Definition of Done
1. **Access sanity checks** (single lightweight probe per endpoint; record HTTP status only; do not store data):
   - Binance Futures `fundingRate` (BTCUSDT, limit=1) → expect HTTP 451 (RESTRICTED_LOCATION)
   - Bybit V5 `funding/history` (linear, BTCUSDT, limit=1) → expect HTTP 403 (COUNTRY_BLOCKED)
   - Kraken spot ticker (XBTUSD): HTTP 200 (reachable; sanity check only, not in the Cycle 4 spec)
   Run them with a fresh timestamp and record the actual statuses; do not copy the expected values.

2. **Artifact review**: `research/HANDOFF.md`, `research/SEARCH_LOG.md`, `research/TASK_CYCLE_3218.md`, and `research/HYPOTHESES.md`. Confirm consistency on access labels, cycle numbering, and conclusions. Confirm `research/TASK_CYCLE_3218.md` Status = COMPLETE.

3. **`research/HYPOTHESES.md`**: Leave unmodified unless a factual inconsistency is found. Known bookkeeping-only defects (do not fix, do not treat as factual errors): duplicate "Cycle 346" at lines 267/279; out-of-order Cycle 2182/2185 headings at lines 325/332; newest cycle entry is Cycle 2211.

4. **`research/SEARCH_LOG.md`** — this file has THREE summary locations; update ALL of them and verify they agree (grep for every "Last checked"/"Cycles covered"/"Earliest check" occurrence):
   - The consolidated running heading near the top (`## Consolidated standby cycles (...)`): advance to Cycles 2842–3219 (378 consecutive standby cycles) with the new "last checked" timestamp.
   - Prepend a "Cycle 3219 closeout" bullet.
   - The mid-file "Earliest check" / "Last checked" / "Cycles covered" block: set to Cycle 3219 / 2842 through 3219 / 378 consecutive standby cycles.
   - The end-of-file "Earliest check" / "Last checked" / "Cycles covered" block: set to Cycle 3219 / 2842–3219 / 378 cycles.
   - **Coverage-check tip:** match the prefix `- **Cycle N closeout` (not `closeout:**`). Verify all Cycle 3040–3218 closeout bullets are present (pre-existing duplicate bullets are identical redundant entries, not missing coverage).

5. **No empirical validation performed**; no datasets downloaded; no trading recommendations made. State this explicitly.

6. **Activation conditions check**: confirm neither occurred.
   - (a) No unrestricted network/proxy available to run H1 per Cycle 4 specs (Binance−Bybit, 2024-01-11–2025-03-17, 8h intervals, OOS ≥4 months from 2024-11-10) with full fee/slippage modeling.
   - (b) No user request for a new hypothesis/route beyond the 4 discovered routes.

7. **Update `research/HANDOFF.md`**: add a Cycle 3219 completion entry, advance to Cycle 3219 complete → Cycle 3220, and update the access-status timestamp. Re-open the file and confirm it actually carries the new cycle number.

8. **Create `research/TASK_CYCLE_3220.md`** as the next initial task message (Status: PENDING). Then verify it exists with `ls research/TASK_CYCLE_*.md` and re-read it. Mark this file Status = COMPLETE only after steps 1–8 are actually done.

## Bookkeeping traps to avoid
- Update **all three** summary locations in `research/SEARCH_LOG.md` and verify they agree; grep for every "Last checked"/"Cycles covered"/"Earliest check".
- Check bullet coverage with the prefix `- **Cycle N closeout`, not `closeout:**`.
- Verify claimed files actually exist and claimed handoff edits actually landed (`ls research/TASK_CYCLE_*.md`, re-read `research/HANDOFF.md` and `research/SEARCH_LOG.md`). Record a reconciliation note if fixing a prior false claim.

## Context
Project remains CLOSEOUT/STANDBY. Original Cycle 4 spec (Binance−Bybit, 2024-01-11–2025-03-17, 8h intervals, OOS ≥4 months from 2024-11-10) is unrunnable from this environment: Binance = RESTRICTED_LOCATION (HTTP 451), Bybit = COUNTRY_BLOCKED (HTTP 403), confirmed across 400+ cycles including recent re-confirmations (last 2026-11-16T22:34:46Z, Cycle 3218 closeout). Venue-substituted replications (Hyperliquid vs KuCoin for H1; Deribit for H2) falsified both hypotheses for tradability under documented costs.

## Activation Conditions (only act if one occurs)
1. An unrestricted network/proxy becomes available → run H1 exactly per Cycle 4 specs (Binance−Bybit, 2024-01-11–2025-03-17, 8h intervals, OOS ≥4 months from 2024-11-10) with full fee/slippage modeling. Document the access method. (Note: this crosses into validation, which is normally out of scope; only do it if the user explicitly authorizes it.)
2. The user explicitly requests a new hypothesis/route beyond the 4 discovered routes.

## Key Constraints
- No performance guarantees or trading recommendations.
- No datasets to redistribute.
- Document any venue substitutions if new work is attempted.
- Update all research artifacts after the cycle.

## Access Status at Handoff (2026-11-16T22:34:46Z, Cycle 3218)
- Binance Futures fundingRate: HTTP 451 (RESTRICTED_LOCATION) — blocked
- Bybit V5 funding/history: HTTP 403 (COUNTRY_BLOCKED) — blocked
- Kraken spot ticker: HTTP 200 (reachable, sanity check only, not in spec)
