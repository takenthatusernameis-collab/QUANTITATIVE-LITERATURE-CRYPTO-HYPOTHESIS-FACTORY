This is a continuation of the QUANTITATIVE-LITERATURE-CRYPTO-HYPOTHESIS-FACTORY project, currently in a **standby/closeout state**. The full durable handoff is in `research/HANDOFF.md`; the research log is `research/SEARCH_LOG.md`; the hypotheses and findings are `research/HYPOTHESES.md`.

**Your task (Cycle 437):** Standby/closeout no-op. Do NOT retry blocked Binance/Bybit endpoints for data collection. Maintain research-only scope. Keep `research/HANDOFF.md`, `research/SEARCH_LOG.md`, `research/TASK_CYCLE_437.md`, and `research/HYPOTHESES.md` consistent.

**Constraints (must follow):**
- Do NOT retry Binance/Bybit endpoints from this environment (Binance = RESTRICTED_LOCATION HTTP 451, Bybit = COUNTRY_BLOCKED HTTP 403; confirmed persistent across 400+ cycles).
- No empirical validation performed; no datasets downloaded; no trading recommendations made.
- Only act if: (1) unrestricted network/proxy becomes available → run H1 exactly per Cycle 4 specs (Binance−Bybit, 2024-01-11–2025-03-17, 8h, OOS ≥4 months from 2024-11-10) with full fee/slippage modeling and document access method, OR (2) user explicitly requests a new hypothesis/route beyond the 4 already discovered.
- No performance guarantees or trading recommendations. No datasets to redistribute. Document any venue substitutions if new work is attempted. Update all research artifacts after any cycle.

**What has been done (summary):** 4 literature routes explored (Cycles 1-4); H1 (cross-venue funding spread persistence) and H2 (anchoring-intensity basis premium) synthesized. Original Cycle 4 spec unrunnable from this environment. Venue-substituted replications (Hyperliquid vs KuCoin for H1; Deribit for H2) falsified both hypotheses for tradability under documented costs.

**Access status at handoff (2026-10-30T18:07:27Z, Cycle 436):**
- Binance Futures fundingRate: HTTP 451 (RESTRICTED_LOCATION) — blocked
- Bybit V5 funding/history: HTTP 403 (COUNTRY_BLOCKED) — blocked
- Kraken spot ticker: HTTP 200 (reachable, sanity check only, not in spec)
- Deribit, Hyperliquid, KuCoin, OKX: reachable (used only for venue-substituted replications; not part of original spec)
