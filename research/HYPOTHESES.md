# HYPOTHESES — Cycle 2 (Route A: perpetual funding rate predictability & basis)

Source appraisal and mechanism extraction. No empirical validation performed.

## Source 1 — Inan (2025), "Predictability of Funding Rates"
- Citation: Inan, E. (2025). Predictability of Funding Rates. International Review of Financial Analysis (SSRN 5576424). York University.
- Access: free (SSRN abstract + published page + secondary summaries).
- Method: BTC/USDT perpetual funding rates, Binance & Bybit, 2024-01-11 to 2025-03-17, 8h observations; out-of-sample last 384 obs (from 2024-11-10); one-step-ahead point forecasts from double autoregressive (DAR) models vs no-change benchmark; directional accuracy + forecast error; parameter-estimation-noise adjustment.
- Key findings: DAR outperforms no-change in directional accuracy (Binance 48.70–60.16%, Bybit 49.48–62.5%); raw forecast errors not consistently better; stronger conclusions only after adjustment; predictability time-varying, more unstable on Bybit; cross-exchange spread strategy (short higher expected funding, long other) with $100M, 5x leverage: with modeled fees 6.258% annualized (8 trades) vs benchmark 4.258% (15 trades); without fees benchmark wins 16.652% vs 10.122%.
- Limitations: ~4-month OOS only; single asset/exchanges; fee scenarios stylized; no live execution/slippage; statistical significance hinging on estimation-noise adjustment; time-varying stability means regime risk.

## Source 2 — Gornall, Rinaldi & Xiao (2024/2025), "Perpetual Futures and Basis Risk: Evidence from Cryptocurrency"
- Citation: Gornall, W., Rinaldi, M. & Xiao, Y. (2024). Perpetual Futures and Basis Risk: Evidence from Cryptocurrency. SSRN 5036933 (Nov 2024; rev. May 2025). UBC / CUHK.
- Access: free (SSRN abstract + AEA preliminary + CFTC comment + ResearchGate).
- Method: crypto market as laboratory; empirical comparison of perpetual vs quarterly futures (spreads, volume, liquidations, crisis drawdowns) across Kraken/BitMEX; tractable model of capital-constrained arbitrage (market makers, liquidity traders, hedgers).
- Key findings: perpetuals dominate volume and reduce extreme dislocations; spreads 49–83% tighter than quarterly; perpetual futures decline ~3% more than spot in large moves vs 8–10% for quarterly; perpetual basis-trade drawdowns ~1/3 of quarterly and mean-revert quickly; liquidity advantage larger in volatility; funding payments 8h, small magnitude (-0.004% to 0.01%).
- Limitations: preliminary/incomplete paper; crypto-only, no out-of-sample tradable strategy; model is stylized; crisis events selected; no peer review yet.

## Source 3 — Ackerer, Hugonnier & Jermann (2024), "Perpetual Futures Pricing"
- Citation: Ackerer, D., Hugonnier, J. & Jermann, U. (2024). Perpetual Futures Pricing. NBER WP 32936 (Sep 2024); arXiv:2310.11771; published Mathematical Finance 36(3), 481–499 (2026). EPFL / Wharton.
- Access: free (NBER working paper PDF, arXiv, CEPR DP 19455).
- Method: no-arbitrage pricing of linear, inverse, quanto perpetuals in discrete and continuous time; identifies funding specs guaranteeing futures price = spot; price = risk-neutral expectation of spot sampled at random time reflecting anchoring intensity; replication by dynamic trading.
- Key findings: with appropriate interest term, basis can be zero; otherwise price is discounted expectation at random sampling time; quanto requires convexity correction; perpetuals replicable.
- Limitations: theoretical; assumes no arbitrage, constant rates/params; no empirical validation of pricing residuals; crypto treated as application not testbed.

## Mechanism synthesis
Funding rate persistence (DAR) + contract-design anchoring intensity (AHJ) + capital-constrained arbitrage/basis risk (Gornall) jointly imply: (a) short-horizon funding is weakly predictable and unstable; (b) cross-venue funding spreads are the tradable object, not single-venue levels; (c) basis risk and execution costs dominate gross signal.

## Hypotheses (falsifiable, no empirical validation here)

H1 — Cross-venue funding spread persistence (proxy: ΔF = funding_rate_Binance − funding_rate_Bybit for BTC 8h).
Claim: DAR-type one-step-ahead forecasts of ΔF have directional accuracy > 55% out-of-sample and a fee-aware spread strategy (short higher, long lower, with modeled entry/exit costs) earns positive annualized net return over a 4-month OOS window.
Observable proxies: directional accuracy of ΔF forecast; annualized net return; trade count; max drawdown.
Failure modes: (i) directional accuracy ≤ 50% (no signal); (ii) gross spread < 2× round-trip costs; (iii) stability collapses in high-volatility subsample (Bybit-like instability); (iv) benchmark (no-change) beats DAR net-of-fees.

H2 — Anchoring-intensity / basis premium (proxy: basis = perp_price − spot_price, and funding rate level).
Claim: Periods where realized funding rate exceeds the no-arbitrage-implied funding (from AHJ random-sampling intensity) coincide with larger subsequent basis mean-reversion within 1–3 funding intervals; i.e., mispricing is transient and speed of reversion scales with funding magnitude.
Observable proxies: half-life of basis deviations; correlation of funding magnitude with next-interval basis change; out-of-sample R² of basis-reversion regression.
Failure modes: (i) no significant mean reversion; (ii) reversion slower than 3 intervals (capital not arbitraging); (iii) effect driven only by crisis subsamples (Gornall) and absent in normal periods; (iv) sign flips by exchange/contract type (inverse vs linear).
