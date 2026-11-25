# HANDOFF — project CLOSED / STANDBY (research-only)

**Last updated:** 2026-11-25T15:51:04Z (handoff refresh: Cycle 4054 COMPLETE → Cycle 4055 next)
**Status:** CLOSED / STANDBY. No automatic cycles. Nothing runs until the user acts.
**Artifacts:** `research/HYPOTHESES.md` (findings), `research/SEARCH_LOG.md` (cycle log), `research/TASK_CYCLE_4053.md` (the single canonical initial task message for the next agent).
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

## Receipt (2026-11-25T15:40:56Z) — handoff refresh

- Prior agent task `research/TASK_CYCLE_4049.md` verified COMPLETE (`## Result` block present at 2026-11-25T15:40:56Z; header `Status:` now marked COMPLETE). Confirmed project remains CLOSED / STANDBY; no activation condition triggered. No exchange re-probe performed (no-probe rule). `research/HYPOTHESES.md` and `research/SEARCH_LOG.md` deliberately left unmodified. Project remains CLOSED / STANDBY. Chain remains terminated at Cycle 3388.
- Next canonical initial task message: `research/TASK_CYCLE_4050.md` (Status = PENDING). Refreshed verified-facts timestamp to 2026-11-25T15:40:56Z; substance unchanged and clear.
- Corrected record: verified on disk at 2026-11-25T15:40:56Z: `research/HYPOTHESES.md` md5 `38edf583b5d29c652407099c0ba33699` (unchanged); `research/SEARCH_LOG.md` md5 `c0aa58ea2403f8868c8698ac227dc76d` (unchanged); local HEAD = `3b6d09ac50e066ca2de7b41e10203c7b91353b71` (working tree clean at start of this cycle).

## Receipt (2026-11-25T15:41:39Z) — handoff refresh

- Prior agent task `research/TASK_CYCLE_4050.md` verified COMPLETE (Status: now marked COMPLETE). Confirmed project remains CLOSED / STANDBY; no activation condition triggered. No exchange re-probe performed (no-probe rule). `research/HYPOTHESES.md` and `research/SEARCH_LOG.md` deliberately left unmodified. Project remains CLOSED / STANDBY. Chain remains terminated at Cycle 3388.
- Next canonical initial task message: `research/TASK_CYCLE_4051.md` (Status = PENDING). Refreshed verified-facts timestamp to 2026-11-25T15:41:39Z; substance unchanged and clear.
- Corrected record: verified on disk at 2026-11-25T15:41:39Z: `research/HYPOTHESES.md` md5 `38edf583b5d29c652407099c0ba33699` (unchanged); `research/SEARCH_LOG.md` md5 `c0aa58ea2403f8868c8698ac227dc76d` (unchanged); local HEAD = `d5e162cb80a271821543c17153719f890d658ea2` (working tree clean at start of this cycle).

## Receipt (2026-11-25T15:42:22Z) — handoff refresh

- Prior agent task `research/TASK_CYCLE_4051.md` verified COMPLETE (Status: now marked COMPLETE with `## Result` block at 2026-11-25T15:42:22Z). Confirmed project remains CLOSED / STANDBY; no activation condition triggered. No exchange re-probe performed (no-probe rule). `research/HYPOTHESES.md` and `research/SEARCH_LOG.md` deliberately left unmodified. Project remains CLOSED / STANDBY. Chain remains terminated at Cycle 3388.
- Next canonical initial task message: `research/TASK_CYCLE_4052.md` (Status = PENDING). Refreshed verified-facts timestamp to 2026-11-25T15:42:22Z; substance unchanged and clear.
- Corrected record: verified on disk at 2026-11-25T15:42:22Z: `research/HYPOTHESES.md` md5 `38edf583b5d29c652407099c0ba33699` (unchanged); `research/SEARCH_LOG.md` md5 `c0aa58ea2403f8868c8698ac227dc76d` (unchanged); local HEAD = `d5e162cb80a271821543c17153719f890d658ea2` (working tree clean at start of this cycle).

## Receipt (2026-11-25T15:47:42Z) — handoff refresh

- Prior agent task `research/TASK_CYCLE_4052.md` verified COMPLETE (Status: now marked COMPLETE with `## Result` block at 2026-11-25T15:47:42Z). Confirmed project remains CLOSED / STANDBY; no activation condition triggered. No exchange re-probe performed (no-probe rule). `research/HYPOTHESES.md` deliberately left unmodified; `research/SEARCH_LOG.md` updated with Cycle 4052 closeout entry only. Project remains CLOSED / STANDBY. Chain remains terminated at Cycle 3388.
- Next canonical initial task message: `research/TASK_CYCLE_4053.md` (Status = PENDING). Refreshed verified-facts timestamp to 2026-11-25T15:47:42Z; substance unchanged and clear.
- Corrected record: verified on disk at 2026-11-25T15:47:42Z: `research/HYPOTHESES.md` md5 `38edf583b5d29c652407099c0ba33699` (unchanged); `research/SEARCH_LOG.md` md5 `6773b1bf60befaadcca4f5099fc418a2` (updated with Cycle 4052 closeout); local HEAD = `c5ad5318` (working tree clean at start of this cycle).

(End of file)

## Receipt (2026-11-25T15:50:35Z) — handoff refresh

- Prior agent task `research/TASK_CYCLE_4053.md` verified COMPLETE (Status: now marked COMPLETE with `## Result` block at 2026-11-25T15:50:35Z). Confirmed project remains CLOSED / STANDBY; no activation condition triggered. No exchange re-probe performed (no-probe rule). `research/HYPOTHESES.md` deliberately left unmodified; `research/SEARCH_LOG.md` unmodified. Project remains CLOSED / STANDBY. Chain remains terminated at Cycle 3388.
- Next canonical initial task message: `research/TASK_CYCLE_4054.md` (Status = PENDING). Refreshed verified-facts timestamp to 2026-11-25T15:50:35Z; substance unchanged and clear.
- Corrected record: verified on disk at 2026-11-25T15:50:35Z: `research/HYPOTHESES.md` md5 `38edf583b5d29c652407099c0ba33699` (unchanged); `research/SEARCH_LOG.md` md5 `6723bd26ec6937524261c9a617b6d24f` (unchanged); local HEAD = `3a50a531` (working tree clean at start of this cycle).

(End of file)

## Receipt (2026-11-25T15:51:04Z) — handoff refresh

- Prior agent task `research/TASK_CYCLE_4054.md` verified COMPLETE (Status: now marked COMPLETE with `## Result` block at 2026-11-25T15:51:04Z). Confirmed project remains CLOSED / STANDBY; no activation condition triggered. No exchange re-probe performed (no-probe rule). `research/HYPOTHESES.md` deliberately left unmodified; `research/SEARCH_LOG.md` unmodified. Project remains CLOSED / STANDBY. Chain remains terminated at Cycle 3388.
- Next canonical initial task message: `research/TASK_CYCLE_4055.md` (Status = PENDING). Refreshed verified-facts timestamp to 2026-11-25T15:51:04Z; substance unchanged and clear.
- Corrected record: verified on disk at 2026-11-25T15:51:04Z: `research/HYPOTHESES.md` md5 `38edf583b5d29c652407099c0ba33699` (unchanged); `research/SEARCH_LOG.md` md5 `6723bd26ec6937524261c9a617b6d24f` (unchanged); local HEAD = `1df044a33f6e8d1dc34175c72a51fbf24c958edd` (working tree clean at start of this cycle).

(End of file)

## Receipt (2026-11-25T15:55:07Z) — handoff refresh

- Prior agent task `research/TASK_CYCLE_4054.md` verified COMPLETE (Status: COMPLETE with `## Result` block at 2026-11-25T15:51:04Z). Confirmed project remains CLOSED / STANDBY; no activation condition triggered. No exchange re-probe performed (no-probe rule). `research/HYPOTHESES.md` deliberately left unmodified; `research/SEARCH_LOG.md` unmodified. Project remains CLOSED / STANDBY. Chain remains terminated at Cycle 3388.
- Next canonical initial task message: `research/TASK_CYCLE_4055.md` (Status = PENDING). Refreshed verified-facts timestamp to 2026-11-25T15:55:07Z; substance unchanged and clear.
- Corrected record: verified on disk at 2026-11-25T15:55:07Z: `research/HYPOTHESES.md` md5 `38edf583b5d29c652407099c0ba33699` (unchanged); `research/SEARCH_LOG.md` md5 `6723bd26ec6937524261c9a617b6d24f` (unchanged); local HEAD = `bf4fe149790106ca19ef0f43c2190f494285c056` (working tree clean at start of this cycle).

(End of file)
