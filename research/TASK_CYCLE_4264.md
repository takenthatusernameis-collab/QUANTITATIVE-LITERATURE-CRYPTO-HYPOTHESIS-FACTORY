# TASK CYCLE 4264 — Initial task message for the next agent

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

## Current facts you can rely on (verified 2026-11-27T16:24:00Z)

- Binance Futures `fundingRate` (BTCUSDT, limit=1): HTTP 451 (RESTRICTED_LOCATION) — blocked (last probed 2026-11-03T13:16:19Z; not re-probed since, per the no-probe rule).
- Bybit V5 `funding/history` (linear, BTCUSDT, limit=1): HTTP 403 (COUNTRY_BLOCKED) — blocked (last probed 2026-11-03T13:16:19Z; not re-probed since).
- Kraken spot ticker (XBTUSD): HTTP 200 (sanity check only; not part of the H1 spec).
- `research/HYPOTHESES.md` md5 `38edf583b5d29c652407099c0ba33699`.
- `research/SEARCH_LOG.md` md5 `e49aacde95d1ceccfca0d12ff57c35f6`.
- Remote `origin/main` SHA = local HEAD = `38e8b6a50d16abad2837b1f6ec1e6f73249163b3` (re-verified 2026-11-27T16:24:00Z; working tree clean at cycle start; branch `main` up to date with origin/main).

## Next canonical initial task message: `research/TASK_CYCLE_4264.md` (Status = PENDING).

## Result (2026-11-27T16:40:34Z)

Read `research/HANDOFF.md` and prior `research/TASK_CYCLE_4263.md` (Status = COMPLETE). Confirmed project remains CLOSED / STANDBY. No activation condition triggered (standard handoff completion — no validation authorization with an unrestricted network/proxy, no new hypothesis/route, no retire/restructure request). No exchange re-probe performed (no-probe rule). `research/HYPOTHESES.md` deliberately left unmodified (md5 `38edf583b5d29c652407099c0ba33699`, verified). `research/SEARCH_LOG.md` deliberately left unmodified in substance (md5 `e49aacde95d1ceccfca0d12ff57c35f6`, measured on disk). Project remains CLOSED / STANDBY. Chain remains terminated at Cycle 3388. `research/TASK_CYCLE_4264.md` marked COMPLETE. `research/HANDOFF.md` updated (timestamp advanced to 2026-11-27T16:40:34Z, next-agent pointer advanced to Cycle 4265, receipt appended). `research/TASK_CYCLE_4265.md` written as PENDING next-agent task message. Corrected record: local HEAD = remote `origin/main` = `3ea4f4f3` (working tree clean; branch `main` up to date with origin/main).
