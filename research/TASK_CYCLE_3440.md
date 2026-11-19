# TASK CYCLE 3440 — Manual Handoff Message (research-only) — CHAIN TERMINATED

**Status:** COMPLETE (2026-11-19T19:50:40Z)
**Cycle:** 3440 (manual handoff message; not an automatic standby cycle)
**Supersedes:** Cycle 3439 manual handoff message.
**Read first:** `research/HANDOFF.md` (durable handoff), then this file.

## Result
Manual handoff message (not an automatic standby cycle) per `research/TASK_CYCLE_3440.md`. Fresh access probes (2026-11-19T19:50:40Z): Binance Futures `fundingRate` (BTCUSDT, limit=1) HTTP 451 (RESTRICTED_LOCATION); Bybit V5 `funding/history` (linear, BTCUSDT, limit=1) HTTP 403 (COUNTRY_BLOCKED); Kraken spot ticker (XBTUSD) HTTP 200 — unchanged from 2026-11-19T19:48:24Z. Verified on disk: `research/TASK_CYCLE_3439.md` Status = COMPLETE (2026-11-19T19:48:24Z); `research/HANDOFF.md` = "Cycle 3388 complete → CLOSED (chain terminated)"; all three SEARCH_LOG summary locations (consolidated heading line 346; mid-file `Cycles covered` line 351; end-of-file `Cycles covered` line 686) read Cycle 3388 / 2842–3388 / 547 consecutive standby cycles at last checked 2026-11-19T05:03:25Z, in agreement; `research/HYPOTHESES.md` unmodified (md5 38edf583b5d29c652407099c0ba33699). No reconciliation needed. Advanced the next-agent pointer to `research/TASK_CYCLE_3441.md`. No empirical validation performed; no datasets downloaded; no trading recommendations made. Neither activation condition occurred. Chain remains terminated.

## Task
Project is CLOSED/STANDBY. Do NOT run an automatic standby cycle, do NOT create automatic `TASK_CYCLE_*` files beyond the single next manual handoff message, and do NOT retry blocked Binance/Bybit endpoints for data collection. Only act if an activation condition occurs:

1. An unrestricted network/proxy becomes available AND the user explicitly authorizes validation → run H1 exactly per Cycle 4 specs (Binance−Bybit, 2024-01-11–2025-03-17, 8h intervals, OOS ≥4 months from 2024-11-10) with full fee/slippage modeling. Document the access method.
2. The user explicitly requests a new hypothesis/route beyond the 4 discovered routes.

Otherwise do exactly this:
1. Re-run the three lightweight access probes (Binance, Bybit, Kraken) and record HTTP codes with a UTC timestamp.
2. Verify on disk: predecessor task file Status = COMPLETE, `research/HANDOFF.md` header, all three SEARCH_LOG summary locations (the `## Consolidated standby cycles` heading plus the two `- **Cycles covered:**` bullets), and `research/HYPOTHESES.md` md5 (expect `38edf583b5d29c652407099c0ba33699`).
3. Mark this file COMPLETE with the probe timestamp and add a `## Result` block.
4. Append one dated verification entry to `research/HANDOFF.md` (newest first) and advance the next-agent pointer; dedupe verbatim repeats.
5. Prepend one closeout bullet to `research/SEARCH_LOG.md`.
6. Write `research/TASK_CYCLE_3441.md` as the next manual handoff message.
7. Confirm no activation condition occurred and stop.

## Key constraints
- Research-only: no performance guarantees, no trading recommendations, no datasets redistributed.
- Re-verify all three SEARCH_LOG summary locations on disk each cycle rather than trusting prior closeout prose.
- Keep `research/HANDOFF.md` from re-accumulating duplicate blocks; one dated entry per cycle.

## Access status (last verified 2026-11-19T19:48:24Z)
- Binance Futures fundingRate: HTTP 451 (RESTRICTED_LOCATION) — blocked
- Bybit V5 funding/history: HTTP 403 (COUNTRY_BLOCKED) — blocked
- Kraken spot ticker: HTTP 200 (reachable, sanity check only, not in spec)