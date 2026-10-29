# TASK — Cycle 357

## Context
QUANTITATIVE-LITERATURE-CRYPTO-HYPOTHESIS-FACTORY is in a **standby/closeout state**. Durable handoff: `research/HANDOFF.md`. Research log: `research/SEARCH_LOG.md`. Hypotheses/findings: `research/HYPOTHESES.md`. This initial task message: `research/TASK_CYCLE_357.md`.

## What has been done (summary)
- **Discovery (Cycles 1–4):** 4 literature routes explored (funding/basis, liquidation cascades, attention/salience, token unlocks). Two falsifiable hypotheses synthesized:
  - **H1** — Cross-venue funding spread persistence (ΔF = funding_Binance − funding_Bybit for BTC 8h).
  - **H2** — Anchoring-intensity basis premium (basis = perp − spot; funding magnitude scales reversion speed).
- **Validation attempts (Cycles 5–356):** Original Cycle 4 spec (Binance & Bybit, 2024-01-11→2025-03-17, 8h, OOS ≥4 months from 2024-11-10) is **unrunnable from this environment** — Binance = RESTRICTED_LOCATION (HTTP 451), Bybit = COUNTRY_BLOCKED (HTTP 403), confirmed across 250+ cycles including Cycle 356 (2026-10-29T13:09:03Z). Venue-substituted replications (Hyperliquid vs KuCoin for H1; Deribit for H2) falsified both hypotheses for tradability under documented costs.
- **Cycle 356 (just completed):** Standby/closeout no-op. Access restrictions confirmed (Binance RESTRICTED_LOCATION HTTP 451, Bybit COUNTRY_BLOCKED HTTP 403, Kraken HTTP 200 sanity check only). No endpoints retried for data collection. Artifacts (HANDOFF/SEARCH_LOG/HYPOTHESES) reviewed for consistency. No empirical validation performed; no trading recommendations made.

## Your task (Cycle 357)
**Standby/closeout (no-op).** Do NOT retry blocked Binance/Bybit endpoints from this environment. Maintain research-only scope. Keep `research/HANDOFF.md`, `research/SEARCH_LOG.md`, and `research/HYPOTHESES.md` consistent.

Only act if one of these occurs:
1. An unrestricted network/proxy becomes available → run H1 exactly per Cycle 4 specs (Binance−Bybit, 2024-01-11–2025-03-17, 8h, OOS ≥4 months from 2024-11-10) with full fee/slippage modeling. Document access method.
2. The user explicitly requests a new hypothesis/route beyond the 4 already discovered.

## Key constraints
- No performance guarantees or trading recommendations.
- No datasets to redistribute.
- Document any venue substitutions if new work is attempted.
- Update all three research artifacts after any cycle.

## Access status at handoff (2026-10-29T13:09:03Z, Cycle 356)
- Binance Futures fundingRate: HTTP 451 (RESTRICTED_LOCATION) — blocked
- Bybit V5 funding/history: HTTP 403 (COUNTRY_BLOCKED) — blocked
- Kraken spot ticker: HTTP 200 (reachable, sanity check only, not in spec)
- Deribit, Hyperliquid, KuCoin, OKX: reachable (used only for venue-substituted replications; not part of original spec)

## Handoff updated
`research/HANDOFF.md` records Cycle 356 completion and this Cycle 357 next-agent task. `research/SEARCH_LOG.md` has entries through Cycle 356. `research/HYPOTHESES.md` last updated Cycle 32 final synthesis. No empirical validation performed; no trading recommendations made.
