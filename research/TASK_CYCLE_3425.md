# TASK CYCLE 3425 — Manual Handoff Message (research-only) — CHAIN TERMINATED

**Status:** PENDING
**Cycle:** 3425 (manual handoff message; not an automatic standby cycle)
**Supersedes:** Cycle 3424 manual handoff message.
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
6. Write `research/TASK_CYCLE_3426.md` as the next manual handoff message.
7. Confirm no activation condition occurred and stop.

## Key constraints
- Research-only: no performance guarantees, no trading recommendations, no datasets redistributed.
- Re-verify all three SEARCH_LOG summary locations on disk each cycle.

## Access status (last verified 2026-11-19T13:49:07Z)
- Binance Futures fundingRate: HTTP 451 (RESTRICTED_LOCATION) — blocked
- Bybit V5 funding/history: HTTP 403 (COUNTRY_BLOCKED) — blocked
- Kraken spot ticker: HTTP 200 (reachable, sanity check only, not in spec)