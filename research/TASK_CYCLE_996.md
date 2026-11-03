## Cycle 996 — Initial Task Message (standby/closeout, research-only)
```
TASK — Cycle 996 (standby/closeout, research-only)

Context: QUANTITATIVE-LITERATURE-CRYPTO-HYPOTHESIS-FACTORY is in CLOSEOUT/STANDBY. Durable handoff: research/HANDOFF.md. Research log: research/SEARCH_LOG.md. Hypotheses/findings: research/HYPOTHESES.md. Initial task message: research/TASK_CYCLE_996.md.

What has been done: 4 literature routes explored (Cycles 1-4); H1 (cross-venue funding spread persistence) and H2 (anchoring-intensity basis premium) synthesized. Original Cycle 4 spec (Binance−Bybit, 2024-01-11–2025-03-17, 8h, OOS ≥4 months from 2024-11-10) is unrunnable from this environment — Binance = RESTRICTED_LOCATION (HTTP 451), Bybit = COUNTRY_BLOCKED (HTTP 403), confirmed across 400+ cycles including Cycles 664-995 (last re-confirmed 2026-11-03T13:12:12Z). Venue-substituted replications (Hyperliquid vs KuCoin for H1; Deribit for H2) falsified both hypotheses for tradability under documented costs. No empirical validation performed on original spec; no trading recommendations made.

Your task (Cycle 996): Completed as standby/closeout no-op per HANDOFF. Did NOT retry blocked Binance/Bybit endpoints for data collection (access restrictions persist unchanged: Binance RESTRICTED_LOCATION HTTP 451, Bybit COUNTRY_BLOCKED HTTP 403). Re-verified access from current environment via direct curl (2026-11-03T13:12:41Z):
  - Binance Futures fundingRate (BTCUSDT): HTTP 451 → RESTRICTED_LOCATION. No data collected.
  - Bybit V5 funding/history (linear BTCUSDT): HTTP 403 → COUNTRY_BLOCKED. No data collected.
  - Kraken spot ticker (XBTUSD): HTTP 200 → reachable (sanity check only, not in spec).
  - Deribit: HTTP 400 (host reachable, malformed request, not in spec).
  - Hyperliquid: HTTP 200 → reachable.
  - KuCoin: HTTP 200 → reachable.
  - OKX: HTTP 200 → reachable.
Reviewed research/HANDOFF.md, research/SEARCH_LOG.md, research/TASK_CYCLE_996.md, and research/HYPOTHESES.md for consistency. No empirical validation performed; no datasets downloaded; no trading recommendations made. Neither activation condition occurred: (a) no unrestricted network/proxy available to run H1 per Cycle 4 specs; (b) no user request for new hypothesis/route beyond the 4 discovered routes. Project remains in closeout state.

Next agent task: Cycle 997 standby/closeout no-op. See research/TASK_CYCLE_997.md.

Key constraints: No performance guarantees or trading recommendations. No datasets to redistribute. Document any venue substitutions if new work is attempted. Update all research artifacts after any cycle.

Access status at handoff (2026-11-03T13:12:41Z, Cycle 996):
- Binance Futures fundingRate: HTTP 451 (RESTRICTED_LOCATION) — blocked
- Bybit V5 funding/history: HTTP 403 (COUNTRY_BLOCKED) — blocked
- Kraken spot ticker: HTTP 200 (reachable, sanity check only, not in spec)
- Deribit, Hyperliquid, KuCoin, OKX: reachable (used only for venue-substituted replications; not part of original spec)
```
