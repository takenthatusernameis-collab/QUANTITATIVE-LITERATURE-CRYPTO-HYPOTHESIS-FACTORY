# TASK CYCLE 3878 — Initial task message for the next agent

**Status:** COMPLETE
**Type:** manual handoff (not a standby cycle; nothing is scheduled)
**Read first:** `research/HANDOFF.md` — it is the single durable summary. This file only tells you what to do (and not do) now.

## Situation in one paragraph

The project is CLOSED / STANDBY and research-only. Four literature routes were surveyed; H1 (Binance−Bybit funding-spread persistence) and H2 (anchoring-intensity basis premium) were synthesized and then falsified **for tradability** under documented costs using venue-substituted data (Hyperliquid/KuCoin for H1; Deribit for H2). H1 was never tested on its original Binance/Bybit spec because both endpoints are geo-blocked from this environment (Binance HTTP 451, Bybit HTTP 403; Kraken spot returns 200 but is not part of the spec). Full detail and numbers: `research/HYPOTHESES.md`.

## Your task

**Default: do nothing new in research.** Read `research/HANDOFF.md`, confirm the closed state, and report it to the user in a few lines. Do not run a standby cycle, do not re-probe exchanges as "progress", and do not edit `research/HYPOTHESES.md` or `research/SEARCH_LOG.md` merely to record that nothing changed.

Act **only** if the user does one of these:

1. **Explicitly authorizes validation AND an unrestricted network/proxy is supplied.** Then:
   - Run H1 exactly per the Cycle 4 spec in `research/HYPOTHESES.md`: Binance−Bybit, 2024-01-11 → 2025-03-17, 8h intervals, OOS ≥ 4 months from 2024-11-10, full fee/slippage modeling.
   - Document the access method (proxy/host) in the artifacts.
   - Apply the pre-registered H1 falsification tests; report failure modes, not performance guarantees.
   - Update `research/HYPOTHESES.md` and prepend one bullet to `research/SEARCH_LOG.md`.

2. **Explicitly requests a new hypothesis or a route beyond the four already explored.** Then survey it with the same research-only discipline: sources, mechanism, falsification tests, cost model, data-access spec. No data download unless access is real.

3. **Explicitly asks to retire or restructure the project** (e.g. archive the `TASK_CYCLE_*.md` chain, keep only the canonical task file, or delete the handoff boilerplate). Then do exactly that requested bookkeeping and stop — do not add research content.

If none of these happens, the correct outcome is: no research file changes, no new cycles, a short status report.

## Bookkeeping rule (only when the user asks for a handoff refresh)

When the user explicitly asks for a handoff refresh, do exactly this and nothing more:
- Read `research/HANDOFF.md` and the current `research/TASK_CYCLE_NNNN.md` (Status = PENDING).
- Mark the prior task file COMPLETE by adding a `## Result` block with timestamp, actions taken, and outcome.
- Write the next `research/TASK_CYCLE_NNNN.md` (increment cycle number) as the canonical initial task message (Status = PENDING), mirroring this file's structure.
- Update `research/HANDOFF.md` in place: advance the header timestamp, advance the next-agent pointer, replace the single `## Receipt` block with the new one (keep exactly one receipt).
- Do not edit `research/HYPOTHESES.md` or `research/SEARCH_LOG.md`. Do not run probes. Do not add research content.
- Report to the user: project still CLOSED / STANDBY; no activation condition triggered; artifacts unchanged.

## Result

- Timestamp: 2026-11-23T17:28:28Z (Cycle 3878 handoff refresh)
- Actions taken: Read durable handoff `research/HANDOFF.md` and the current task file `research/TASK_CYCLE_3878.md` (Status was PENDING). Confirmed the closed/standby state and its no-op default. Performed no research changes, no exchange probes, and no new cycles.
- Outcome: `research/TASK_CYCLE_3878.md` marked COMPLETE; handoff refresh bookkeeping performed; `research/TASK_CYCLE_3879.md` written as the canonical next-agent initial task message (Status = PENDING); `research/HANDOFF.md` edited in place (header timestamp advanced, next-agent pointer advanced to 3879, single `## Receipt` block replaced).
- Consistency fix: `research/TASK_CYCLE_3875.md` header Status advanced from PENDING to COMPLETE to match its own `## Result` block (it was the only recent file still showing PENDING after completion), so the canonical PENDING task is unambiguous.
- No activation condition triggered: no unrestricted network/proxy supplied, no validation authorized, no new hypothesis/route requested, no retire/restructure request.
- Verified unchanged: `research/HYPOTHESES.md` (md5 `38edf583b5d29c652407099c0ba33699`) and `research/SEARCH_LOG.md` (md5 `3286eeb61b649779296ede065f029c17`).