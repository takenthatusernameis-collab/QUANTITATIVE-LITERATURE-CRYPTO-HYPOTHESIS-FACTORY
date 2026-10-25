# SEARCH LOG

Cycle 1 — 2026-10-25. Scope: 4 discovery routes, web search only (no paid access). No empirical validation performed.

## Route A — Perpetual funding rate predictability & basis
- Query themes: "perpetual futures funding rate predictability", "basis premium academic paper", "funding rate predict price change"
- Sources: SSRN (Inan 2025; Gornall/Rinaldi/Xiao 2024), arXiv (Ackerer/Hugonnier/Jermann 2024; BitMex funding 2019), Aalto thesis (Helminen 2022), ctfassets note, Korean journal (Kim, perp futures as Bitcoin volatility predictors)
- Useful: funding rates embed positioning imbalance; predictability is real but weak at short horizons, stronger at longer horizons and cross-sectionally; DAR models beat no-change (Inan) but stability is time-varying.
- Dead ends: none material. Caveat: several are student theses / practitioner notes, not peer-reviewed.

## Route B — Liquidation cascades & liquidity spirals
- Query themes: "liquidation cascades", "forced deleveraging price impact", "Brunnermeier Pedersen liquidity spiral"
- Sources: arXiv (branching cascade paper 2026; Cheng 2021 optimal margin), SSRN (Lim 2025 Oct-10 crash; Faulkner 2026 forensic analysis), permissionless.fi chapter, Coindesk/Cryptoslate, JFDA (Nguyen two-regime recovery), Springer (Pindza et al. 2026 venue uncertainty), LSE SSRN (Vayanos constrained arbitrage), NBER/Princeton (Brunnermeier-Pedersen 2008)
- Useful: cascades are derivatives-led, mark-price undershoot is a crypto-specific amplifier, impact-spread spikes ×3-9× are universal, two-regime recovery (spread recovers, depth contracts persistently), long-bias in liquidations (65%).
- Dead ends: none. Caveat: several cascade papers are very recent (2025-2026) and lightly vetted; treat as leads.

## Route C — Attention, salience, behavioural finance
- Query themes: "salience theory cryptocurrency", "investor attention bitcoin prediction", "retail vs institutional attention"
- Sources: IRFA (Chen/Lepori/Tai/Sung 2022 salience), PLOS One (Zhu et al. 2021 attention), Smales (UWA, investor attention & uncertainty), SSRN (Koch/Dimpfl 2022 attention & herding), IREF/Ozdamar et al. (2022 retail vs institutional), FRL (Wang et al. 2022 LSTM attention)
- Useful: attention Granger-causes returns & volatility; salience predicts next-week reversal in micro-caps; retail attention negative for returns, institutional positive; effects accentuated in COVID.
- Dead ends: attention alone does not beat buy-and-hold out-of-sample in most years (Suardi et al.).

## Route D — Token unlocks / vesting schedules
- Query themes: "token unlock price impact", "optimal vesting schedule", "vesting cliff"
- Sources: Keyrock (16k unlocks), 6th Man Ventures (5k unlocks), Animoca Brands Research (35k unlocks, 89 tokens), Chainforce, Stratos.xyz, Unlocks Calendar, Fundstrat
- Useful: unlocks >1% of circulating supply move price (−0.3% wk before, −0.3% wk after); anticipation dominates; cliffs worst; "mostly vested" tokens outperform; daily unlocks neutral.
- Dead ends: none. Caveat: industry analytics, not peer-reviewed; causal claims are correlational and self-stated.

## Coverage limits
- No paywalled sources used. All access was free abstract/full text via public pages, arXiv, SSRN, university repositories, journal open pages, and practitioner research notes.
- Search was not exhaustive; no backward/forward citation chasing was performed this cycle (deferred to Cycle 2 if it changes a ranking).
Cycle 2 — 2026-10-25. Route A source appraisal + mechanism extraction; synthesized H1/H2. No empirical validation performed.

Cycle 4 — 2026-10-25. Implemented research-only validation plan as concrete data-acquisition specs: public endpoints for BTC 8h funding (Binance/Bybit), spot/perp prices, fee schedules; timestamp alignment rules, look-ahead prevention, OOS split >=~4 months holdout, walk-forward, baseline definitions, cost model components, falsification tests per H1/H2, licensing/limits. No data downloaded, no backtests/computations. No trading recommendations. Updated research/HYPOTHESES.md.

Cycle 5 — 2026-10-25. Independent validator attempt blocked: Binance/Bybit free public APIs geographically restricted in this environment; no data collected; no falsification tests run; no computations. Kraken spot ticker sanity check only (not spec source). Hypotheses untested; deferred to unrestricted environment. No trading recommendations.

Cycle 6 — 2026-10-25. Retried per HANDOFF following Cycle 4 specs. Binance Futures fundingRate endpoint returns location restriction error (RESTRICTED_LOCATION); Bybit V5 funding/history returns CloudFront country block (COUNTRY_BLOCKED). Kraken spot ticker reachable but not in spec; no funding/perp data collected. No datasets downloaded, no alignment/OOS/baselines/costs/tests executed. Access labels recorded; gaps documented; hypotheses remain untested. No trading recommendations.

Cycle 7 — 2026-10-25. Retried per HANDOFF. Binance Futures = RESTRICTED_LOCATION; Bybit V5 = COUNTRY_BLOCKED; Kraken reachable (not in spec). No data downloaded; no alignment/OOS/baselines/costs/tests executed. Hypotheses remain untested. No trading recommendations.

Cycle 8 — 2026-10-25. Retried per HANDOFF. Binance Futures = RESTRICTED_LOCATION; Bybit V5 = COUNTRY_BLOCKED; Kraken reachable (not in spec). No data downloaded; no alignment/OOS/baselines/costs/tests executed. Hypotheses remain untested. No trading recommendations.

Cycle 9 — 2026-10-25. Retried per HANDOFF. Binance Futures = RESTRICTED_LOCATION; Bybit V5 = COUNTRY_BLOCKED; Kraken reachable (not in spec). No data downloaded; no alignment/OOS/baselines/costs/tests executed. Hypotheses remain untested. No trading recommendations.

Cycle 10 — 2026-10-25. Retried per HANDOFF. Binance Futures = RESTRICTED_LOCATION; Bybit V5 = COUNTRY_BLOCKED; Kraken reachable (not in spec). No data downloaded; no alignment/OOS/baselines/costs/tests executed. Hypotheses remain untested. No trading recommendations.
