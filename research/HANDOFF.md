# DURABLE HANDOFF (Cycle 52)

## Status
Project is in **CLOSEOUT/STANDBY** state. All prior cycles (1-51) completed as documented in HANDOFF.md. No empirical validation performed on original Binance/Bybit spec due to persistent access restrictions.

## Current Environment Access (Verified 2026-10-26T17:29Z)
- **Binance Futures** `fapi.binance.com/fapi/v1/fundingRate?symbol=BTCUSDT&limit=5`: HTTP 200 with `{"code":0,"msg":"Service unavailable from a restricted location..."}` → **RESTRICTED_LOCATION** (code 0)
- **Bybit V5** `api.bybit.com/v5/market/funding/history?category=linear&symbol=BTCUSDT&limit=5`: HTTP 403 via CloudFront → **COUNTRY_BLOCKED**
- **Kraken spot** `api.kraken.com/0/public/Ticker?pair=XBTUSD`: Reachable (sanity check only, not in Cycle 4 spec)

## Key Findings (Venue-Substituted Replications)
- **H1 (cross-venue funding spread persistence, Binance−Bybit):** Tested Hyperliquid vs KuCoin (2025-06-17–2025-10-14, 359 obs). Directional accuracy 0.850 on test but mean |ΔF|=1.24e-4 vs roundtrip costs ≥0.07% (taker-mix); fee-aware falsification met. Statistical persistence exists but not tradable under published fees.
- **H2 (basis mean-reversion/funding scaling):** Tested Deribit (BTC-settled/inverse, index_price as spot proxy, interest_8h funding). AR(1) mean reversion unstable OOS (train β positive hl~0.15, test β negative), |funding| correlation with next basis change negligible (-0.004), deviations small vs rt costs (~7e-4). Falsified under costs.

## Artifacts (Consistent)
- `research/HYPOTHESES.md` - H1/H2 with venue substitutions, fee-aware falsification, status
- `research/SEARCH_LOG.md` - Full cycle history (1-51) including blocked attempts and substitutions
- `research/HANDOFF.md` - Complete cycle-by-cycle history

## Next Agent Task (Cycle 52)
**STANDBY/CLOSEOUT** - No further work required unless:
1. **Unrestricted network/proxy becomes available** → Test H1 exactly per Cycle 4 specs (Binance−Bybit, 2024-01-11–2025-03-17, 8h intervals, OOS ≥4 months from 2024-11-10) with full fee/slippage modeling. Document access method.
2. **User explicitly requests new hypothesis/route beyond the 4 discovered** in the original research prompt.

**Do NOT:** Retry blocked Binance/Bybit endpoints from this environment (restrictions confirmed persistent). Make performance guarantees or trading recommendations.

**Scope:** Maintain research-only compliance. Keep HANDOFF/SEARCH_LOG/HYPOTHESES consistent.
