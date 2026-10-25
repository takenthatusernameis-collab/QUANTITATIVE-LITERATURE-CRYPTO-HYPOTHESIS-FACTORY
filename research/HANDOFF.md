# DURABLE HANDOFF

## Completed (Cycle 1)
Discovery across 4 routes (funding/basis, liquidation cascades, attention/salience, token unlocks). Results in research/SEARCH_LOG.md. No empirical validation performed.

## Completed (Cycle 2)
Source appraisal + mechanism extraction for Route A on Inan 2025 (DAR funding predictability), Gornall/Rinaldi/Xiao 2024 (perp basis risk), Ackerer/Hugonnier/Jermann 2024 (perp pricing). Recorded citations, access labels, methods, limitations; synthesized 2 falsifiable hypotheses (H1 cross-venue funding spread persistence; H2 anchoring-intensity basis premium). Output: research/HYPOTHESES.md. No empirical validation performed.

## Completed (Cycle 3) — Research-only (scope-compliant)
Scope boundary respected: no datasets downloaded, no backtests/paper trading/performance calculations executed. Produced research-only validation plan for H1 and H2 with free-data feasibility, required fields/timestamps, OOS design, baselines, cost-model requirements, falsification criteria, and failure modes. Added validation-plan section to research/HYPOTHESES.md and logged research-only work in research/SEARCH_LOG.md. No trading recommendations made.

## Completed (Cycle 4) — Research-only (scope-compliant)
Implemented validation plan as concrete data-acquisition specs: exact public endpoints/sources for BTC 8h funding (Binance, Bybit), spot/perp prices/timestamps, fee schedules; documented coverage/history/limits/licensing; timestamp alignment rules; look-ahead prevention; OOS split (>=~4 months holdout) and walk-forward considerations; baseline definitions (no-change); cost model components; explicit falsification tests per H1/H2. No data downloaded, no returns/accuracy/half-lives computed, no backtests run. Updated research/HYPOTHESES.md and research/SEARCH_LOG.md. No trading recommendations made.

## Next agent task
Cycle 5: Independent validator executes the falsification tests per research/HYPOTHESES.md using only free public data (no paid APIs/datasets), strictly following the data-acquisition specs, timestamp alignment, look-ahead prevention, OOS split, baselines, and cost model. Record access labels, coverage, gaps, and limitations. Report failure-mode verdicts only; do NOT make performance guarantees or trading recommendations. Update research/HYPOTHESES.md and research/SEARCH_LOG.md with results/limitations.
