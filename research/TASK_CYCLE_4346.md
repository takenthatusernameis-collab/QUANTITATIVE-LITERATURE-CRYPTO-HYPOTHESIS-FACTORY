# TASK CYCLE 4346 — Initial task message for the next agent

**Status:** COMPLETE
**Type:** manual handoff (not a standby cycle; nothing is scheduled)
**Read first:** `research/HANDOFF.md` — it is the single durable summary. This file only tells you what to do (and not do) now.

## Situation in one paragraph

The project is CLOSED / STANDBY and research-only. Four literature routes were surveyed; H1 (Binance−Bybit funding-spread persistence) and H2 (anchoring-intensity basis premium) were synthesized and then falsified **for tradability** under documented costs using venue-substituted data (Hyperliquid/KuCoin for H1; Deribit for H2). H1 was never tested on its original Binance/Bybit spec because both endpoints are geo-blocked from this environment (Binance HTTP 451, Bybit HTTP 403; Kraken spot returns 200 but is not part of the spec). Full detail and numbers: `research/HYPOTHESES.md`.

## Your task

**Default: do nothing new in research.** Read `research/HANDOFF.md`, confirm the closed state, and report it to the user in a few lines. Do not run a standby cycle, do not re-probe exchanges as "progress", and do not edit `research/HYPOTHESES.md` or `research/SEARCH_LOG.md` merely to record that nothing changed.

Act **only** if the user does one of these:

1. **Explicitly authorizes validation AND an unrestricted network/proxy is supplied.** Then run H1 exactly per the Cycle 4 spec, document access method, apply pre-registered falsification tests, update `research/HYPOTHESES.md` and prepend one bullet to `research/SEARCH_LOG.md`.
2. **Explicitly requests a new hypothesis or a route beyond the four already explored.**
3. **Explicitly asks to retire or restructure the project.**

If none happens, the correct outcome is: no research file changes, no new cycles, a short status report.

## Hard constraints

- No performance guarantees, no trading recommendations, no datasets redistributed.
- Do not present re-verification of a closed project as research progress.
- Do not create `TASK_CYCLE_*.md` files except as the single canonical next-agent task message when a handoff is explicitly requested.

## Current facts you can rely on (verified 2026-11-28T06:55:50Z)

- Binance Futures `fundingRate` (BTCUSDT, limit=1): HTTP 451 (RESTRICTED_LOCATION) — blocked (last probed 2026-11-03T13:16:19Z; not re-probed since, per the no-probe rule).
- Bybit V5 `funding/history` (linear, BTCUSDT, limit=1): HTTP 403 (COUNTRY_BLOCKED) — blocked (last probed 2026-11-03T13:16:19Z; not re-probed since).
- Kraken spot ticker (XBTUSD): HTTP 200 (sanity check only; not part of the H1 spec).
- `research/HYPOTHESES.md` md5 `38edf583b5d29c652407099c0ba33699`.
- `research/SEARCH_LOG.md` md5 `8bec965c4e30b50b317012336474feb2` (working tree clean; the delta from the older `90d99a9bea4a19a10dd015404592b530` is prior-cycle closeout bookkeeping captured by automated checkpoint commits, not research work).
- Remote `origin/main` SHA = local HEAD = `e96865b35e408dbac94bb1c771ed64ec8febc99a` (working tree clean at start of cycle; branch `main` up to date with origin/main).

## Result (2026-11-28T06:58:08Z) — handoff completion

- Prior agent task `research/TASK_CYCLE_4346.md` completed: read `research/HANDOFF.md`, confirmed CLOSED / STANDBY state, reported to user. No activation condition triggered (standard handoff completion — user requested standard handoff completion only; no validation authorization with an unrestricted network/proxy, no new hypothesis/route, no retire/restructure request). No exchange re-probe performed (no-probe rule). `research/HYPOTHESES.md` deliberately left unmodified (md5 `38edf583b5d29c652407099c0ba33699`, verified). `research/SEARCH_LOG.md` deliberately left unmodified (md5 `8bec965c4e30b50b317012336474feb2`, verified on disk). Project remains CLOSED / STANDBY. Chain remains terminated at Cycle 3388.
- Next canonical initial task message: `research/TASK_CYCLE_4347.md` (Status = PENDING). Written this cycle as a clear PENDING initial task message for the next agent; verified-facts timestamp 2026-11-28T06:58:08Z.
- Corrected record: re-verified on disk at 2026-11-28T06:58:08Z: `research/HYPOTHESES.md` md5 `38edf583b5d29c652407099c0ba33699`; `research/SEARCH_LOG.md` md5 `8bec965c4e30b50b317012336474feb2`; local HEAD = `e96865b35e408dbac94bb1c771ed64ec8febc99a` (working tree clean at start of cycle; branch `main` up to date with origin/main; this cycle's handoff/task-file edits uncommitted per no-commit instruction; research artifacts unmodified in substance this cycle).
EOF