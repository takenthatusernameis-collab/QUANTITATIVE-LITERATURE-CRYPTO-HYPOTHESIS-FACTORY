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

## Cycle 11 — 2026-10-25T16:45:00Z (attempt, blocked)
- Action: Retry Cycle 5/6/7/8/9/10 validation per HANDOFF and Cycle 4 data-acquisition specs (BTC 8h funding + spot/perp for Binance & Bybit), with timestamp alignment/look-ahead prevention/OOS>=~4m/baselines/cost model and H1/H2 falsification tests. No perf/trading recs.
- Attempts:
  - Binance Futures fundingRate (fapi.binance.com/fapi/v1/fundingRate?symbol=BTCUSDT&limit=1): RESTRICTED_LOCATION (code 0/msg Service unavailable from a restricted location...)
  - Bybit V5 funding/history (api.bybit.com/v5/market/funding/history?category=linear&symbol=BTCUSDT&limit=1): COUNTRY_BLOCKED (CloudFront block)
  - Kraken spot Ticker (api.kraken.com/0/public/Ticker?pair=XBTUSD): reachable (sanity check only; not in spec)
- Outcome: No datasets downloaded. No timestamp alignment/OOS/baselines/cost model/falsification tests executed. Hypotheses remain untested. Access labels/gaps/limitations recorded.
- Verdict: Blocked in current environment. Defer to unrestricted network environment or approved proxy/alternative venue with documented justification.

## Cycle 12 — 2026-10-25T17:08:26Z (attempt, blocked)
- Action: Retried validation per HANDOFF (Cycle 12) following Cycle 4 data-acquisition specs exactly from current environment.
- Binance Futures: `GET https://fapi.binance.com/fapi/v1/fundingRate?symbol=BTCUSDT&limit=100` → `{"code":0,"msg":"Service unavailable from a restricted location..."}` (RESTRICTED_LOCATION). No data collected.
- Bybit V5: `HEAD https://api.bybit.com/v5/market/funding/history?category=linear&symbol=BTCUSDT&limit=50` → HTTP/2 403 via CloudFront (COUNTRY_BLOCKED). No data collected.
- Kraken: `GET https://api.kraken.com/0/public/Ticker?pair=XBTUSD` → reachable (sanity check only, not in Cycle 4 spec). No funding/perp series collected.
- Outcome: No datasets downloaded; no timestamp alignment/OOS/baselines/cost model/falsification tests executed. H1/H2 untested. Access gaps recorded.

## Cycle 13 — 2026-10-25T17:08:55Z (attempt, blocked)
- Action: Retried validation per HANDOFF (Cycle 13) following Cycle 4 data-acquisition specs exactly from current environment.
- Binance Futures: `GET https://fapi.binance.com/fapi/v1/fundingRate?symbol=BTCUSDT&limit=100` → RESTRICTED_LOCATION (code 0). No data collected.
- Bybit V5: `HEAD https://api.bybit.com/v5/market/funding/history?category=linear&symbol=BTCUSDT&limit=50` → HTTP 403 via CloudFront (COUNTRY_BLOCKED). No data collected.
- Kraken: `GET https://api.kraken.com/0/public/Ticker?pair=XBTUSD` → reachable (sanity check only, not in Cycle 4 spec). No funding/perp series collected.
- Outcome: No datasets downloaded; no timestamp alignment/OOS/baselines/cost model/falsification tests executed. H1/H2 untested. Access gaps recorded.

## Cycle 14 — 2026-10-25T17:09:03Z (attempt, blocked)
- Action: Retried validation per HANDOFF (Cycle 14) following Cycle 4 data-acquisition specs exactly from current environment.
- Binance Futures: `GET https://fapi.binance.com/fapi/v1/fundingRate?symbol=BTCUSDT&limit=100` → RESTRICTED_LOCATION (code 0, eligibility restriction). No data collected.
- Bybit V5: `HEAD https://api.bybit.com/v5/market/funding/history?category=linear&symbol=BTCUSDT&limit=50` → HTTP 403 via CloudFront (COUNTRY_BLOCKED). No data collected.
- Kraken: `GET https://api.kraken.com/0/public/Ticker?pair=XBTUSD` → reachable (sanity check only, not in Cycle 4 spec). No funding/perp series collected.
- Outcome: No datasets downloaded; no timestamp alignment/OOS/baselines/cost model/falsification tests executed. H1/H2 untested. Access gaps/limitations recorded. Deferred to unrestricted environment or approved proxy/alternative venue.

## Cycle 15 — 2026-10-25T17:46:29Z (attempt, blocked)
- Action: Retried validation per HANDOFF (Cycle 15) following Cycle 4 data-acquisition specs exactly from current environment.
- Binance Futures: `GET https://fapi.binance.com/fapi/v1/fundingRate?symbol=BTCUSDT&limit=100` → RESTRICTED_LOCATION (code 0, eligibility restriction). No data collected.
- Bybit V5: `GET https://api.bybit.com/v5/market/funding/history?category=linear&symbol=BTCUSDT&limit=50` → HTTP 403 via CloudFront (COUNTRY_BLOCKED). No data collected.
- Kraken: `GET https://api.kraken.com/0/public/Ticker?pair=XBTUSD` → reachable (sanity check only, not in Cycle 4 spec). No funding/perp series collected.
- Outcome: No datasets downloaded; no timestamp alignment/OOS/baselines/cost model/falsification tests executed. H1/H2 untested. Access gaps/limitations recorded. Deferred to unrestricted environment or approved proxy/alternative venue.

## Cycle 16 — 2026-10-25T17:46:47Z (attempt, blocked)
- Action: Retried validation per HANDOFF (Cycle 16) following Cycle 4 data-acquisition specs exactly from current environment.
- Binance Futures: `GET https://fapi.binance.com/fapi/v1/fundingRate?symbol=BTCUSDT&limit=100` → RESTRICTED_LOCATION (code 0, eligibility restriction). No data collected.
- Bybit V5: `GET https://api.bybit.com/v5/market/funding/history?category=linear&symbol=BTCUSDT&limit=50` → HTTP 403 via CloudFront (COUNTRY_BLOCKED). No data collected.
- Kraken: `GET https://api.kraken.com/0/public/Ticker?pair=XBTUSD` → reachable (sanity check only, not in Cycle 4 spec). No funding/perp series collected.
- Outcome: No datasets downloaded; no timestamp alignment/OOS/baselines/cost model/falsification tests executed. H1/H2 untested. Access gaps/limitations recorded. Deferred to unrestricted environment or approved proxy/alternative venue. No trading recommendations.

## Cycle 17 — 2026-10-25T18:02:41Z (Blocked: data access, same env)
- Action: Retried validation per HANDOFF (Cycle 17) following Cycle 4 data-acquisition specs exactly from current environment.
- Binance Futures fundingRate (BTCUSDT, limit=100): HTTP 200 error `{"code":0,"msg":"Service unavailable from a restricted location..."}` (RESTRICTED_LOCATION). No data collected.
- Bybit V5 funding/history (linear BTCUSDT, limit=50): HTTP 403 via CloudFront (COUNTRY_BLOCKED). No data collected.
- Kraken spot ticker (XBTUSD): reachable (sanity check only, not in Cycle 4 spec). No funding/perp series collected.
- Timestamp alignment/OOS split/baselines/cost model/falsification tests: not executed (no datasets).
- Access labels: Binance=RESTRICTED_LOCATION, Bybit=COUNTRY_BLOCKED, Kraken=REACHABLE(not in spec).
- Verdict: Blocked (data access). H1/H2 remain untested; deferred to unrestricted network environment or approved proxy/alternative venue with documented justification. No trading recommendations made.

## Cycle 18 — 2026-10-25T18:05:02Z (Blocked: data access, same env)
- Action: Retried validation per HANDOFF (Cycle 18) following Cycle 4 data-acquisition specs exactly from current environment.
- Binance Futures fundingRate (BTCUSDT, limit=100): HTTP 200 error `{"code":0,"msg":"Service unavailable from a restricted location according to 'b. Eligibility' in https://www.binance.com/en/terms. Please contact customer service if you believe you received this message by mistake."}` (RESTRICTED_LOCATION). No data collected.
- Bybit V5 funding/history (linear BTCUSDT, limit=50): HTTP 403 via CloudFront (COUNTRY_BLOCKED). No data collected.
- Kraken spot ticker (XBTUSD): reachable (sanity check only, not in Cycle 4 spec). No funding/perp series collected.
- Timestamp alignment/OOS split/baselines/cost model/falsification tests: not executed (no datasets).
- Access labels: Binance=RESTRICTED_LOCATION, Bybit=COUNTRY_BLOCKED, Kraken=REACHABLE (not in spec).
- Verdict: Blocked (data access). H1/H2 remain untested; deferred to unrestricted network environment or approved proxy/alternative venue with documented justification. No trading recommendations made.

## Cycle 19 — Validation attempt (2026-10-25T18:06:13Z, blocked)
- Retried Cycle 4 data-acquisition specs from current environment.
- Binance Futures fundingRate (BTCUSDT, limit=5): RESTRICTED_LOCATION (code 0). No data collected.
- Bybit V5 funding/history (linear BTCUSDT, limit=5): HTTP 403 via CloudFront (COUNTRY_BLOCKED). No data collected.
- Kraken spot ticker (XBTUSD): reachable (sanity check only, not in spec).
- Timestamp alignment/OOS split/baselines/cost model/falsification tests: not executed (no datasets).
- Access labels: Binance=RESTRICTED_LOCATION, Bybit=COUNTRY_BLOCKED, Kraken=REACHABLE (not in spec).
- Verdict: Blocked (data access). H1/H2 remain untested; deferred to unrestricted network environment or approved proxy/alternative venue with documented justification. No trading recommendations made.

## Cycle 21 — 2026-10-25T19:13:13Z (Blocked: data access, same env)
- Action: Retried per HANDOFF (Cycle 21) following Cycle 4 data-acquisition specs exactly from current environment.
- Binance Futures fundingRate (BTCUSDT, limit=5): RESTRICTED_LOCATION (code 0, eligibility restriction).
- Bybit V5 funding/history (linear BTCUSDT, limit=5): HTTP 403 via CloudFront (COUNTRY_BLOCKED).
- Kraken spot ticker (XBTUSD): reachable (sanity check only, not in spec).
- No datasets downloaded; no timestamp alignment/OOS/baselines/cost model/falsification tests executed.
- Access labels: Binance=RESTRICTED_LOCATION, Bybit=COUNTRY_BLOCKED, Kraken=REACHABLE (not in spec).
- Verdict: Blocked (data access). H1/H2 remain untested; deferred to unrestricted network environment or approved proxy/alternative venue with documented justification. No trading recommendations made.

## Cycle 22 — 2026-10-25T19:13:37Z (Blocked: data access, same env)
- Action: Retried per HANDOFF (Cycle 22) following Cycle 4 data-acquisition specs exactly from current environment.
- Binance Futures fundingRate (BTCUSDT, limit=5): RESTRICTED_LOCATION (code 0, eligibility restriction).
- Bybit V5 funding/history (linear BTCUSDT, limit=5): HTTP 403 via CloudFront (COUNTRY_BLOCKED).
- Kraken spot ticker (XBTUSD): reachable (sanity check only, not in spec).
- No datasets downloaded; no timestamp alignment/OOS/baselines/cost model/falsification tests executed.
- Access labels: Binance=RESTRICTED_LOCATION, Bybit=COUNTRY_BLOCKED, Kraken=REACHABLE (not in spec).
- Verdict: Blocked (data access). H1/H2 remain untested; deferred to unrestricted network environment or approved proxy/alternative venue with documented justification. No trading recommendations made.

## Cycle 21 — Blocked (data access, same env)
- Timestamp: 2026-10-25T19:13:13Z
- Binance Futures fundingRate (BTCUSDT, limit=5): RESTRICTED_LOCATION (code 0, eligibility restriction).
- Bybit V5 funding/history (linear BTCUSDT, limit=5): HTTP 403 via CloudFront (COUNTRY_BLOCKED).
- Kraken spot ticker (XBTUSD): reachable (sanity check only, not in spec).
- No datasets downloaded; no timestamp alignment/OOS/baselines/cost model/falsification tests executed.
- Access labels: Binance=RESTRICTED_LOCATION, Bybit=COUNTRY_BLOCKED, Kraken=REACHABLE (not in spec).
- Verdict: Blocked (data access). H1/H2 remain untested; deferred to unrestricted network environment or approved proxy/alternative venue with documented justification. No trading recommendations made.

## Cycle 23 — 2026-10-25T19:22:17Z (Blocked: data access, same env)
- Action: Retried per HANDOFF (Cycle 23) following Cycle 4 data-acquisition specs exactly from current environment.
- Binance Futures fundingRate (BTCUSDT, limit=5): RESTRICTED_LOCATION (code 0, eligibility restriction).
- Bybit V5 funding/history (linear BTCUSDT, limit=5): HTTP 403 via CloudFront (COUNTRY_BLOCKED).
- Kraken spot ticker (XBTUSD): reachable (sanity check only, not in spec).
- No datasets downloaded; no timestamp alignment/OOS/baselines/cost model/falsification tests executed.
- Access labels: Binance=RESTRICTED_LOCATION, Bybit=COUNTRY_BLOCKED, Kraken=REACHABLE (not in spec).
- Verdict: Blocked (data access). H1/H2 remain untested; deferred to unrestricted network environment or approved proxy/alternative venue with documented justification. No trading recommendations made.
