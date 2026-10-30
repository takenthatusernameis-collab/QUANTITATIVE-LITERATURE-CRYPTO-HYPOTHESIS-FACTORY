# TASK — Cycle 440

## Context
This is a continuation of the QUANTITATIVE-LITERATURE-CRYPTO-HYPOTHESIS-FACTORY project, currently in a **standby/closeout state**. The full durable handoff is in `research/HANDOFF.md`; the research log is `research/SEARCH_LOG.md`; the hypotheses and findings are `research/HYPOTHESES.md`.

## What has been done (summary)
- **Discovery (Cycles 1–4):** 4 literature routes explored (funding/basis, liquidation cascades, attention/salience, token unlocks). Two falsifiable hypotheses synthesized from Route A sources:
  - **H1** — Cross-venue funding spread persistence (ΔF = funding_Binance − funding_Bybit for BTC 8h).
  - **H2** — Anchoring-intensity basis premium (basis = perp − spot; funding magnitude scales reversion speed).
- **Validation attempts (Cycles 5–439):** Original Cycle 4 spec (Binance & Bybit, 2024-01-11→2025-03-17, 8h, OOS ≥4 months from 2024-11-10) is **unrunnable from this environment** — Binance = RESTRICTED_LOCATION (HTTP 451), Bybit = COUNTRY_BLOCKED (HTTP 403), confirmed across 400+ cycles including Cycle 439 (2026-10-30T15:23:23Z).
- **Venue-substituted replications (Cycles 26–32):**
  - H2 tested on Deribit (BTC-settled/inverse): mean reversion present but unstable OOS, no funding-magnitude scaling, effect size << roundtrip costs (~7e-4) → **falsified for tradability**.
  - H1 tested on Hyperliquid vs KuCoin (359 overlapping 8h obs, 2025-06-17→2025-10-14): no-change persistence directional accuracy 0.850 on test, but mean |ΔF| = 1.24e-4 vs roundtrip costs ≥~0.07% → **fee-aware falsification met**.
- **Conclusion:** Both hypotheses falsified for tradability under documented costs and venue substitutions. All work is research-only; no trading recommendations have been made.
- **Cycle 439 (just completed):** Standby/closeout (no-op). Access restrictions confirmed (Binance RESTRICTED_LOCATION HTTP 451, Bybit COUNTRY_BLOCKED HTTP 403, Kraken HTTP 200 sanity check only). No endpoints retried for data collection. Artifacts (HANDOFF/SEARCH_LOG/HYPOTHESES/TASK_CYCLE_439) reviewed for consistency. Updated research/HANDOFF.md (Cycle 439 completion + Cycle 440 next task + initial task message) and research/SEARCH_LOG.md (Cycle 439 entry). Created research/TASK_CYCLE_440.md.

## Your task (Cycle 440)
**Standby/closeout (no-op).** Do NOT retry blocked Binance/Bybit endpoints from this environment. Maintain research-only scope. Keep `research/HANDOFF.md`, `research/SEARCH_LOG.md`, `research/HYPOTHESES.md`, and `research/TASK_CYCLE_440.md` consistent.

Only act if one of these occurs:
1. An unrestricted network/proxy becomes available → run H1 exactly per Cycle 4 specs (Binance−Bybit, 2024-01-11–2025-03-17, 8h, OOS ≥4 months from 2024-11-10) with full fee/slippage modeling. Document access method.
2. The user explicitly requests a new hypothesis/route beyond the 4 already discovered.

## Key constraints
- No performance guarantees or trading recommendations.
- No datasets to redistribute.
- Document any venue substitutions if new work is attempted.
- Update all research artifacts after any cycle.

## Access status at handoff (2026-10-30T15:23:23Z, Cycle 439)
- Binance Futures fundingRate: HTTP 451 (RESTRICTED_LOCATION) — blocked
- Bybit V5 funding/history: HTTP 403 (COUNTRY_BLOCKED) — blocked
- Kraken spot ticker: HTTP 200 (reachable, sanity check only, not in spec)
- Deribit, Hyperliquid, KuCoin, OKX: reachable (used only for venue-substituted replications; not part of original spec)

## Handoff updated
`research/HANDOFF.md` now records Cycle 439 completion and this Cycle 440 next-agent task. `research/SEARCH_LOG.md` has entries through Cycle 439. `research/HYPOTHESES.md` last updated Cycle 32 final synthesis. No empirical validation performed; no trading recommendations made.
