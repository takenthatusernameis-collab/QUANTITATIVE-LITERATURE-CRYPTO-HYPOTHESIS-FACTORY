# TASK CYCLE 3541 — Initial task message for the next agent

**Status:** PENDING
**Type:** manual handoff (not a standby cycle; nothing is scheduled)
**Read first:** `research/HANDOFF.md` — it is the single durable summary. This file only tells you what to do (and not do) now.

## Situation in one paragraph

The project is CLOSED / STANDBY and research-only. Four literature routes were surveyed; H1 (Binance−Bybit funding-spread persistence) and H2 (anchoring-intensity basis premium) were synthesized and then falsified **for tradability** under documented costs using venue-substituted data (Hyperliquid/KuCoin for H1; Deribit for H2). H1 was never tested on its original Binance/Bybit spec because both endpoints are geo-blocked from this environment (Binance HTTP 451, Bybit HTTP 403; Kraken spot returns 200 but is not part of the spec). Full detail and numbers: `research/HYPOTHESES.md`.

Git persistence note (verified 2026-11-22T07:17:13Z): the prior session's bounded remote checkpoint persistence failure has been recovered — local commit `4779aa65c137f1fa4ff3d7144909f4fc7de52150` was pushed to `origin/main` as a clean fast-forward and the remote SHA was verified to match local HEAD. All local commits are preserved; no history was rewritten. The controller will retry persistence of any local-ahead commits after this session; do not claim persistence until the remote SHA matches.

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

When the user explicitly asks for a handoff refresh, do exactly this and nothing more:
- Read `research/HANDOFF.md` and the current `research/TASK_CYCLE_NNNN.md` (Status = PENDING).
- Mark the prior task file COMPLETE by adding a `## Result` block with timestamp, actions taken, and outcome.
- Write the next `research/TASK_CYCLE_NNNN.md` (increment cycle number) as the canonical initial task message (Status = PENDING), mirroring this file's structure.
- Update `research/HANDOFF.md` in place: advance the header timestamp, advance the next-agent pointer, replace the single `## Receipt` block with the new one (keep exactly one receipt).
- Do not edit `research/HYPOTHESES.md` or `research/SEARCH_LOG.md`. Do not run probes. Do not add research content.
- Report to the user: project still CLOSED / STANDBY; no activation condition triggered; artifacts unchanged.

## Hard constraints

- No performance guarantees, no trading recommendations, no datasets redistributed.
- Do not present re-verification of a closed project as research progress.
- Do not create `TASK_CYCLE_*.md` files except as the single canonical next-agent task message when a handoff is explicitly requested.
- When you advance a handoff, verify each prior task file's header Status matches its `## Result` block; fix stale `Status: PENDING` headers that already carry a Result block (this happened at Cycle 3678).
- **Known divergence (do not silently resolve):** the repo also contains a parallel, off-book chain at `research/TASK_CYCLE_3521.md` … `research/TASK_CYCLE_3682.md` (139 COMPLETE + 24 PENDING files, partly logged in `SEARCH_LOG.md` through Cycle 3610) produced by separate checkpoint sessions and NOT referenced by `research/HANDOFF.md`. The authoritative record is `research/HANDOFF.md` + the single canonical task file named there. Treat the high-numbered files as stale unless the user explicitly authorizes a reconciliation/restructure. Do not delete them as part of a routine handoff.
- **Persistence safety:** never claim a checkpoint is persisted until `git ls-remote origin refs/heads/main` returns a SHA equal to local `git rev-parse HEAD`. Do not reset or discard local commits; do not rewrite history unless a confirmed root cause requires it, and then only after preserving a recovery bundle and documenting the rollback plan.

## Current facts you can rely on (verified 2026-11-22T07:17:13Z)

- Binance Futures `fundingRate` (BTCUSDT, limit=1): HTTP 451 (RESTRICTED_LOCATION) — blocked (last probed 2026-11-03T13:16:19Z; not re-probed since, per the no-probe rule).
- Bybit V5 `funding/history` (linear, BTCUSDT, limit=1): HTTP 403 (COUNTRY_BLOCKED) — blocked (last probed 2026-11-03T13:16:19Z; not re-probed since, per the no-probe rule).
- Kraken spot ticker (XBTUSD): HTTP 200 (sanity check only; not part of the H1 spec).
- `research/HYPOTHESES.md` md5 `38edf583b5d29c652407099c0ba33699` (stable since Cycle 3450-era).
- `research/SEARCH_LOG.md` md5 `3286eeb61b649779296ede065f029c17` on disk. The `5ae5ddfd…` value quoted in older task files is stale boilerplate: `SEARCH_LOG.md` was legitimately edited (Cycle 3387 reconciliation) after those files were written, and no cycle entry is added for handoff cycles 3389+. Do not "restore" it.
- Standby counter frozen at Cycle 3388 (547 consecutive no-op cycles, 2842–3388); Cycles 3389–3539 were handoff bookkeeping only.
- Remote `origin/main` SHA = local HEAD = `4779aa65c137f1fa4ff3d7144909f4fc7de52150` (persistence verified).
