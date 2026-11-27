# TASK CYCLE 4221 — Initial task message for the next agent

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

## Current facts you can rely on (verified 2026-11-27T06:00:34Z)

- Binance Futures `fundingRate` (BTCUSDT, limit=1): HTTP 451 (RESTRICTED_LOCATION) — blocked (last probed 2026-11-03T13:16:19Z; not re-probed since, per the no-probe rule).
- Bybit V5 `funding/history` (linear, BTCUSDT, limit=1): HTTP 403 (COUNTRY_BLOCKED) — blocked (last probed 2026-11-03T13:16:19Z; not re-probed since).
- Kraken spot ticker (XBTUSD): HTTP 200 (sanity check only; not part of the H1 spec).
- `research/HYPOTHESES.md` md5 `38edf583b5d29c652407099c0ba33699`.
- `research/SEARCH_LOG.md` md5 `17a7c298e6f91b293b9b0fdfceb5c816`.
- Remote `origin/main` SHA = local HEAD = `f362aa55cbc9f97c42d36957d6fc5cb789af6295` (verified 2026-11-27T06:00:34Z; working tree clean; branch `main` up to date with origin/main).

## Next canonical initial task message: `research/TASK_CYCLE_4221.md` (Status = PENDING).

## Result (2026-11-27T06:04:31Z)

Read `research/HANDOFF.md`, confirmed project remains CLOSED / STANDBY. Verified on disk: `research/HYPOTHESES.md` md5 `38edf583b5d29c652407099c0ba33699`; `research/SEARCH_LOG.md` md5 `0f6a66fda98c67ebf3fb46071be5c7cb`; local HEAD = `7f32c1e17689707b554bf324456901c76d230532` = remote `origin/main` (working tree clean). No activation condition triggered (standard handoff refresh — no unrestricted network/proxy supplied, no new hypothesis/route requested, no validation authorized, no retire/restructure request). No exchange re-probe performed (no-probe rule). Research artifacts deliberately left unmodified. Record correction: the prior 06:00:34Z receipt listed `research/SEARCH_LOG.md` md5 `17a7c298e6f91b293b9b0fdfceb5c816`, but the Cycle 4220 closeout bullet was committed in `7f32c1e1` (06:03:48Z), so the on-disk md5 at this cycle's start is `0f6a66fda98c67ebf3fb46071be5c7cb` (content-only change: one prepended closeout bullet; no research substance altered). Updated `research/HANDOFF.md` with receipt timestamp 2026-11-27T06:04:31Z and advanced next-agent pointer to Cycle 4222. Status → COMPLETE.