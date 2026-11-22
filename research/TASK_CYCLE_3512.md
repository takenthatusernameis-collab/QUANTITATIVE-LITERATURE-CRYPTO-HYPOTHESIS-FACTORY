# TASK CYCLE 3512 — Initial task message for the next agent

**Status:** COMPLETE
**Type:** manual handoff (not a standby cycle; nothing is scheduled)
**Read first:** `research/HANDOFF.md` — it is the single durable summary. This file only tells you what to do (and not do) now.

## Situation in one paragraph

The project is CLOSED / STANDBY and research-only. Four literature routes were surveyed; H1 (Binance−Bybit funding-spread persistence) and H2 (anchoring-intensity basis premium) were synthesized and then falsified **for tradability** under documented costs using venue-substituted data (Hyperliquid/KuCoin for H1, Deribit for H2). H1 was never tested on its original Binance/Bybit spec because both endpoints are geo-blocked from this environment (Binance HTTP 451, Bybit HTTP 403, reconfirmed 2026-11-20T11:17:20Z; Kraken spot returns 200 but is not part of the spec, so it proves nothing about H1 feasibility). Full detail and numbers: `research/HYPOTHESES.md`.

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

## Bookkeeping rule (only when the user asks for a handoff refresh)

- Mark the current `TASK_CYCLE_*.md` COMPLETE with a short `## Result` block, write the next `TASK_CYCLE_<n+1>.md`, and edit `research/HANDOFF.md` in place: advance the header timestamp and next-agent pointer and keep exactly one dated receipt.
- `research/HANDOFF.md` must stay compact — one durable summary, never an append-only log of near-identical entries.

## Hard constraints

- No performance guarantees, no trading recommendations, no datasets redistributed.
- Do not present re-verification of a closed project as research progress.
- Do not create `TASK_CYCLE_*.md` files except as the single canonical next-agent task message when a handoff is explicitly requested.

## Current facts you can rely on (verified 2026-11-20T11:17:20Z)

- Binance Futures `fundingRate` (BTCUSDT, limit=1): HTTP 451 (RESTRICTED_LOCATION) — blocked.
- Bybit V5 `funding/history` (linear, BTCUSDT, limit=1): HTTP 403 (COUNTRY_BLOCKED) — blocked.
- Kraken spot ticker (XBTUSD): HTTP 200 (sanity check only; not part of the H1 spec).
- `research/HYPOTHESES.md` md5 `38edf583b5d29c652407099c0ba33699`.
- `research/SEARCH_LOG.md` md5 `5ae5ddfd00639448928a53732beeb3e3`.
- Standby counter frozen at Cycle 3388 (547 consecutive no-op cycles, 2842–3388); Cycles 3389–3511 were handoff bookkeeping only.

## Result

- **Timestamp:** 2026-11-22T02:28:00Z
- **Prior task:** Cycle 3511 read from `research/TASK_CYCLE_3511.md`; already COMPLETE (Result block 2026-11-20T13:21:44Z), so the prior agent's work was verified rather than repeated.
- **Verified on disk:** `research/TASK_CYCLE_3511.md` Status = COMPLETE with a `## Result` block; its canonical next-agent message `research/TASK_CYCLE_3512.md` existed (Status = PENDING) and matched the handoff; `research/HYPOTHESES.md` md5 `38edf583b5d29c652407099c0ba33699` unchanged. `research/SEARCH_LOG.md` md5 is `3286eeb61b649779296ede065f029c17` on disk; no cycle entry was added for it (cycles 3389+ are handoff bookkeeping only, not logged there), so the `5ae5ddfd…` value quoted in earlier task files was stale boilerplate — noted, not treated as drift.
- **Actions:** marked this file (Cycle 3512) COMPLETE; wrote `research/TASK_CYCLE_3513.md` (Status = PENDING) as the canonical next-agent initial task message; updated `research/HANDOFF.md` in place (header timestamp advanced to this receipt, next-agent pointer set to `TASK_CYCLE_3513.md`, single `## Receipt` block replaced). Reconciled one stale header: `research/TASK_CYCLE_3678.md` carried a `## Result` block (2026-11-21T21:34:44Z) but still read Status = PENDING; advanced to COMPLETE to match Cycles 3679–3681.
- **Outcome:** COMPLETE. No activation condition triggered (no unrestricted network/proxy supplied; no new hypothesis or route requested; no validation authorized; no retire/restructure request). No research content added; no probes run. Project remains CLOSED / STANDBY.