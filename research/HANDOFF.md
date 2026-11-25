# HANDOFF — project CLOSED / STANDBY (research-only)

**Last updated:** 2026-11-25T09:07:54Z (handoff refresh: Cycle 4035 COMPLETE → Cycle 4036 next)
**Status:** CLOSED / STANDBY. No automatic cycles. Nothing runs until the user acts.
**Artifacts:** `research/HYPOTHESES.md` (findings), `research/SEARCH_LOG.md` (cycle log), `research/TASK_CYCLE_4036.md` (the single canonical initial task message for the next agent).
**Project type:** literature-driven crypto hypothesis generation. Research-only: no performance guarantees, no trading recommendations, no datasets redistributed.

## What was actually done

- **Cycles 1–4:** four literature routes surveyed; H1 and H2 synthesized with falsification tests, cost models, and a data-acquisition spec. Sources: Inan (2025) funding-rate predictability; Gornall, Rinaldi & Xiao (2024) perpetual vs quarterly basis; Ackerer, Hugonnier & Jermann (2024) perpetual futures pricing. Details in `research/HYPOTHESES.md`.
- **H1** — cross-venue funding spread persistence (Binance − Bybit, 2024-01-11 → 2025-03-17, 8h, OOS ≥ 4 months from 2024-11-10). Original-venue test **never ran**: blocked from this environment. Venue-substituted test (Hyperliquid vs KuCoin, 2025-06-17 → 2025-10-14, 359 obs) found persistence (no-change directional accuracy 0.850, mean |ΔF| ≈ 0.0124%) but gross spread is >5× smaller than conservative round-trip cost (≥0.07%) → **falsified for tradability under published base fees**.
- **H2** — anchoring-intensity basis premium / basis mean reversion (Deribit BTC-PERPETUAL substitution, 3720 obs, 2024-02-29 → 2025-03-17). Mean reversion exists but is extremely fast (half-life ≈0.16 funding intervals), unstable OOS (test β sign flips), and shows no funding-magnitude scaling (corr ≈ −0.004); effect size far below ~7e-4 round-trip cost → **falsified for tradability**.
- **No empirical validation** was ever performed on the original Binance/Bybit H1 spec.

## Access status (last probed 2026-11-03T13:16:19Z — unchanged since Cycle 5; not re-probed since, per the no-probe rule)

| Probe | Endpoint | Result |
|---|---|---|
| Binance Futures | `GET /fapi/v1/fundingRate?symbol=BTCUSDT&limit=1` | HTTP 451 RESTRICTED_LOCATION — blocked |
| Bybit V5 | `GET /v5/market/funding/history?category=linear&symbol=BTCUSDT&limit=1` | HTTP 403 COUNTRY_BLOCKED — blocked |
| Kraken spot | `GET /0/public/Ticker?pair=XBTUSD` | HTTP 200 — reachable, sanity check only (not in spec) |

## Only act if one of these occurs

1. **User explicitly authorizes validation AND an unrestricted network/proxy is supplied.** Then run H1 exactly per the Cycle 4 spec (Binance − Bybit, 2024-01-11 → 2025-03-17, 8h intervals, OOS ≥ 4 months from 2024-11-10, full fee/slippage modeling), document the access method, and record results in `HYPOTHESES.md` + `SEARCH_LOG.md`.
2. **User explicitly requests a new hypothesis or route** beyond the four already explored.

Anything else is a no-op. Do not re-run probes as "progress", do not add another closeout cycle, and do not re-verify these files for their own sake.

## Standing state of the record

- Cycle 3388 (2026-11-19T05:03:25Z) was the last cycle that advanced the standby counter: 547 consecutive no-op standby cycles (2842–3388), zero research output. The chain was terminated there.
- Cycles 3389–4006 were manual handoff messages (user-requested) that re-verified the closed state and changed no conclusion. Only a representative subset is logged in `SEARCH_LOG.md` (through Cycle 3610, which belongs to a divergent parallel chain — see receipt below); the rest are recorded only in the single receipt below.
- This handoff was rewritten at Cycle 3463 to replace ~73 KB of near-duplicate dated blocks with one durable summary, compacted again at Cycle 3492, and compacted again at Cycle 3508 to fold the Cycle 3493–3508 per-handoff receipts into the single receipt below. Prior verbose text remains recoverable in git history and in `research/HANDOFF.md.bak.*`.
- Known cosmetic defects, deliberately not fixed: duplicate "Cycle 346" and out-of-order "Cycle 2182"/"2185" headings in `HYPOTHESES.md`; a few missing historical closeout bullets in `SEARCH_LOG.md` (Cycles 3291, 3317, 3318).

## Receipt (2026-11-25T09:07:54Z) — handoff refresh

- Prior agent task `research/TASK_CYCLE_4035.md` verified COMPLETE (Status = COMPLETE, `## Result` block present at 2026-11-25T09:07:54Z). Confirmed project remains CLOSED / STANDBY; no activation condition triggered. No exchange re-probe performed (no-probe rule). `research/HYPOTHESES.md` and `research/SEARCH_LOG.md` deliberately left unmodified. Project remains CLOSED / STANDBY. Chain remains terminated at Cycle 3388.
- Next canonical initial task message: `research/TASK_CYCLE_4036.md` (Status = PENDING). Clear and complete; no changes needed.
- Corrected record: verified on disk at 2026-11-25T09:07:54Z: `research/HYPOTHESES.md` md5 `38edf583b5d29c652407099c0ba33699` (unchanged); `research/SEARCH_LOG.md` md5 `afcf2710310673d14e7e2184fd27879b` (unchanged); local HEAD = `d42808b4fbab53ccc877d32516c6c4813824ea16` (working tree clean at start of this cycle).

(End of file)
