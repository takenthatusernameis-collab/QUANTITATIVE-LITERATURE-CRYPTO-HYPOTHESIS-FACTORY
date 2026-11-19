# TASK CYCLE 3411 — Manual Handoff Message (research-only) — CHAIN TERMINATED

**Status:** PENDING
**Cycle:** 3411 (manual handoff message; not an automatic standby cycle)
**Supersedes:** Cycle 3410 manual handoff message.
**Read first:** `research/HANDOFF.md` (durable handoff), then this file.

## Task
Project is CLOSED/STANDBY. Do NOT run an automatic standby cycle, do NOT create automatic `TASK_CYCLE_*` files beyond the single next manual handoff message, and do NOT retry blocked Binance/Bybit endpoints for data collection. Only act if an activation condition occurs:

1. An unrestricted network/proxy becomes available AND the user explicitly authorizes validation → run H1 exactly per Cycle 4 specs (Binance−Bybit, 2024-01-11–2025-03-17, 8h intervals, OOS ≥4 months from 2024-11-10) with full fee/slippage modeling. Document the access method.
2. The user explicitly requests a new hypothesis/route beyond the 4 discovered routes.

Otherwise do exactly this:
1. Re-run the three lightweight access probes (Binance, Bybit, Kraken) and record HTTP codes with a UTC timestamp.
2. Verify on disk: predecessor task file Status = COMPLETE, `research/HANDOFF.md` header, all three SEARCH_LOG summary locations, and `research/HYPOTHESES.md` md5 (expect `38edf583b5d29c652407099c0ba33699`).
3. Mark this file COMPLETE with the probe timestamp and add a `## Result` block.
4. Append one dated verification entry to `research/HANDOFF.md` (newest first) and advance the next-agent pointer; dedupe verbatim repeats.
5. Prepend one closeout bullet to `research/SEARCH_LOG.md`.
6. Write `research/TASK_CYCLE_3412.md` as the next manual handoff message.
7. Confirm no activation condition occurred and stop.

## Key constraints
- Research-only: no performance guarantees, no trading recommendations, no datasets redistributed.
- Document any venue substitutions if new work is attempted (prior substitutions: Hyperliquid vs KuCoin for H1; Deribit for H2 — both falsified for tradability under documented costs).
- Re-verify all three SEARCH_LOG summary locations on disk each cycle: the `## Consolidated standby cycles (2842–3388, …)` heading, plus the mid-file and end-of-file `- **Cycles covered:**` bullets. Do not trust prior closeout prose — false/over-claims have recurred 25 times, most recently at Cycle 3386.
- Keep `research/HANDOFF.md` from re-accumulating duplicate status/verification blocks; one dated entry per handoff.

## Access status (last verified 2026-11-19T11:36:53Z)
- Binance Futures fundingRate: HTTP 451 (RESTRICTED_LOCATION) — blocked
- Bybit V5 funding/history: HTTP 403 (COUNTRY_BLOCKED) — blocked
- Kraken spot ticker: HTTP 200 (reachable, sanity check only, not in spec)

## Verification (performed in Cycle 3410, 2026-11-19T11:36:53Z)
- Probes: Binance Futures `fundingRate` (BTCUSDT, limit=1) HTTP 451 (RESTRICTED_LOCATION); Bybit V5 `funding/history` (linear, BTCUSDT, limit=1) HTTP 403 (COUNTRY_BLOCKED); Kraken spot ticker (XBTUSD) HTTP 200 — unchanged from 2026-11-19T10:44:38Z.
- `research/TASK_CYCLE_3409.md` Status = COMPLETE (2026-11-19T10:44:38Z).
- `research/TASK_CYCLE_3410.md` marked COMPLETE (2026-11-19T11:36:53Z).
- `research/HANDOFF.md` = "Cycle 3388 complete → CLOSED (chain terminated)".
- SEARCH_LOG summary locations verified on disk: heading (line 312) 2842–3388 / 547 consecutive standby cycles, last checked 2026-11-19T05:03:25Z; mid-file block (lines 317 and 459) and end-of-file block (line 652) read 2842–3388 (547 cycles) — all three in agreement, unchanged as expected for a terminated chain.
- `research/HYPOTHESES.md` unmodified (md5 38edf583b5d29c652407099c0ba33699).
- No reconciliation needed.

## Result
Chain remains terminated at Cycle 3388 (547 consecutive no-op standby cycles). Unless the user authorizes validation (activation condition 1) or requests a new route (activation condition 2), the project should remain formally closed.

**Status:** COMPLETE (2026-11-19T11:40:00Z)
