# TASK CYCLE 3408 — Manual Handoff Message (research-only) — CHAIN TERMINATED

**Status:** PENDING
**Cycle:** 3408 (manual handoff message; not an automatic standby cycle)
**Supersedes:** Cycle 3407 manual handoff message.

## Task
Project is CLOSED/STANDBY. Do NOT run an automatic standby cycle. Only act if an activation condition occurs:

1. An unrestricted network/proxy becomes available AND the user explicitly authorizes validation → run H1 exactly per Cycle 4 specs (Binance−Bybit, 2024-01-11–2025-03-17, 8h intervals, OOS ≥4 months from 2024-11-10) with full fee/slippage modeling. Document the access method.
2. The user explicitly requests a new hypothesis/route beyond the 4 discovered routes.

Otherwise: re-verify the closed state from the filesystem (access probes + on-disk artifacts), confirm no activation condition occurred, leave artifacts consistent, and write the next manual handoff message. Do NOT retry blocked Binance/Bybit endpoints for data collection. Maintain research-only scope.

## Key constraints
- No performance guarantees or trading recommendations.
- No datasets to redistribute.
- Document any venue substitutions if new work is attempted.
- Update all research artifacts after any cycle.
- Re-verify all three SEARCH_LOG summary locations on disk each cycle: the `## Consolidated standby cycles (2842–3388, …)` heading, plus the mid-file and end-of-file `- **Cycles covered:**` bullets. Do not trust prior closeout prose.
- Keep `research/HANDOFF.md` from re-accumulating duplicate status/verification blocks; append one dated verification entry per handoff and dedupe verbatim repeats.

## Access status (last verified 2026-11-19T10:35:57Z)
- Binance Futures fundingRate: HTTP 451 (RESTRICTED_LOCATION) — blocked
- Bybit V5 funding/history: HTTP 403 (COUNTRY_BLOCKED) — blocked
- Kraken spot ticker: HTTP 200 (reachable, sanity check only, not in spec)

## Verification (performed in Cycle 3407)
- Access probes (2026-11-19T10:35:57Z): Binance Futures `fundingRate` (BTCUSDT, limit=1) HTTP 451 (RESTRICTED_LOCATION); Bybit V5 `funding/history` (linear, BTCUSDT, limit=1) HTTP 403 (COUNTRY_BLOCKED); Kraken spot ticker (XBTUSD) HTTP 200 — unchanged from 2026-11-19T09:43:20Z.
- `research/TASK_CYCLE_3406.md` Status = COMPLETE (2026-11-19T09:43:20Z).
- `research/TASK_CYCLE_3407.md` Status = COMPLETE (2026-11-19T10:35:57Z).
- `research/HANDOFF.md` = "Cycle 3388 complete → CLOSED (chain terminated)".
- All three SEARCH_LOG summary locations verified on disk: heading reads 2842–3388 / 547 consecutive standby cycles, last checked 2026-11-19T05:03:25Z; mid-file and end-of-file `- **Cycles covered:**` bullets read 2842–3388 (547 cycles) — all three in agreement, unchanged as expected for a terminated chain.
- `research/HYPOTHESES.md` unmodified (md5 38edf583b5d29c652407099c0ba33699).
- Note: `research/TASK_CYCLE_3407.md` did not exist on disk despite being claimed as written by Cycle 3406; it was created and marked COMPLETE in this cycle. Do not assume prior closeout prose reflects on-disk reality — verify before trusting.

## Result
Chain remains terminated at Cycle 3388. Unless the user authorizes validation (activation condition 1) or requests a new route (activation condition 2), the project should remain formally closed. Do NOT create automatic cycles. No empirical validation performed; no datasets downloaded; no trading recommendations made.

**Status:** PENDING — awaiting the next agent to execute (or the user to trigger an activation condition).
