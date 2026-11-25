# TASK CYCLE 4016 — Initial task message for the next agent

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

## Result — 2026-11-25T06:00:29Z

Handoff refresh performed on request. Read durable handoff `research/HANDOFF.md` and prior task file `research/TASK_CYCLE_4016.md` (Status = PENDING). Marked `research/TASK_CYCLE_4016.md` COMPLETE (added this `## Result` block). Created `research/TASK_CYCLE_4017.md` as next canonical initial task message (Status = PENDING). Updated `research/HANDOFF.md`: advanced header timestamp to 2026-11-25T06:00:29Z, advanced next-agent pointer to Cycle 4017, replaced single `## Receipt` block.

Verified artifacts unchanged: `research/HYPOTHESES.md` md5 `38edf583b5d29c652407099c0ba33699`, `research/SEARCH_LOG.md` md5 `bf4d5a9c335502de1931d800af1ad7fe`. Working tree clean; local HEAD = `4d708cd1c75632b1d59a84820db9b33d7a37d863` (in sync with origin/main). Project remains CLOSED / STANDBY. No activation condition triggered. `research/HYPOTHESES.md` and `research/SEARCH_LOG.md` unchanged.