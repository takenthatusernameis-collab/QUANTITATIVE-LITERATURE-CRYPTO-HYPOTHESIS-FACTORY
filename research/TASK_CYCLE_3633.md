TASK CYCLE 3633 — Initial task message for the next agent

**Status:** COMPLETE (2026-11-21T13:18:47Z)
**Type:** manual handoff (not a standby cycle; nothing is scheduled)
**Read first:** `research/HANDOFF.md` — it is the single durable summary. This file only tells you what to do (and not do) now.

## Situation in one paragraph

The project is CLOSED / STANDBY and research-only. Four literature routes were surveyed; H1 (Binance−Bybit funding-spread persistence) and H2 (anchoring-intensity basis premium) were synthesized and then falsified **for tradability** under documented costs using venue-substituted data (Hyperliquid/KuCoin for H1; Deribit for H2). H1 was never tested on its original Binance/Bybit spec because both endpoints are geo-blocked from this environment (Binance HTTP 451, Bybit HTTP 403; Kraken spot returns 200 but is not part of the spec). Full detail and numbers: `research/HYPOTHESES.md`.

## Your task

**Default: do nothing new in research.** Read `research/HANDOFF.md`, confirm the closed state, and report it to the user in a few lines. Do not run a standby cycle, do not re-probe exchanges as "progress", and do not edit `HYPOTHESES.md` or `SEARCH_LOG.md` merely to record that nothing changed.

Act **only** if the user does one of these:

1. **Explicitly authorizes validation AND an unrestricted network/proxy is supplied.** Then:
   - Run H1 exactly per the Cycle 4 spec in `research/HYPOTHESES.md`: Binance−Bybit, 2024-01-11 → 2025-03-17, 8h intervals, OOS ≥ 4 months from 2024-11-10, full fee/slippage modeling.
   - Document the access method (proxy/host) in the artifacts.
   - Apply the pre-registered H1 falsification tests; report failure modes, not performance guarantees.
   - Update `research/HYPOTHESES.md` and prepend one bullet to `research/SEARCH_LOG.md`.

2. **Explicitly requests a new hypothesis or a route beyond the four already explored.** Then survey it with the same research-only discipline: sources, mechanism, falsification tests, cost model, data-access spec. No data download unless access is real.

3. **Explicitly asks to retire or restructure the project** (e.g. archive the `TASK_CYCLE_*.md` chain, keep only the canonical task file, or delete the handoff boilerplate). Then do exactly that requested bookkeeping and stop — do not add research content.

If none of these happens, the correct outcome is: no research file changes, no new cycles, a short status report.

## Result (2026-11-21T13:18:47Z) — Cycle 3633 complete

Actions taken: Read `research/HANDOFF.md` and this task file. Confirmed project CLOSED / STANDBY, research-only. Both activation conditions absent: no unrestricted network/proxy supplied, no new hypothesis or route requested, no retirement/restructure requested. Neither Binance (HTTP 451 RESTRICTED_LOCATION) nor Bybit (HTTP 403 COUNTRY_BLOCKED) is accessible; Kraken spot is reachable but not in the Cycle 4 spec. No probes run, no datasets downloaded, no timestamp alignment/OOS/baseline/cost-model/falsification work executed. No research file changes made beyond this task cycle bookkeeping.

Outcome: No activation condition triggered. Correct outcome applied: no research edits, no new research cycles, no new hypotheses, no validation, no trading recommendations. Chain remains terminated at Cycle 3388. Artifacts unchanged (`research/HYPOTHESES.md` md5 `38edf583b5d29c652407099c0ba33699`; `research/SEARCH_LOG.md` md5 `d069e6c08c61ddb89958d7f45c8b0bb0`).

Status: COMPLETE — handoff advanced to `research/TASK_CYCLE_3634.md` as the canonical next-agent task message.
EOF
