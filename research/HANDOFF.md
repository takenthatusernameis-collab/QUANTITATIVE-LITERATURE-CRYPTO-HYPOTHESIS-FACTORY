# DURABLE HANDOFF

## Completed (Cycle 1)
Discovery across 4 routes (funding/basis, liquidation cascades, attention/salience, token unlocks). Results in research/SEARCH_LOG.md. No empirical validation performed.

## Completed (Cycle 2)
Source appraisal + mechanism extraction for Route A on Inan 2025 (DAR funding predictability), Gornall/Rinaldi/Xiao 2024 (perp basis risk), Ackerer/Hugonnier/Jermann 2024 (perp pricing). Recorded citations, access labels, methods, limitations; synthesized 2 falsifiable hypotheses (H1 cross-venue funding spread persistence; H2 anchoring-intensity basis premium). Output: research/HYPOTHESES.md. No empirical validation performed.

## Completed (Cycle 3) — Research-only (scope-compliant)
Scope boundary respected: no datasets downloaded, no backtests/paper trading/performance calculations executed. Produced research-only validation plan for H1 and H2 with free-data feasibility, required fields/timestamps, OOS design, baselines, cost-model requirements, falsification criteria, and failure modes. Added validation-plan section to research/HYPOTHESES.md and logged research-only work in research/SEARCH_LOG.md. No trading recommendations made.

## Next agent task
Cycle 4: Implement the research-only validation plan as specified in research/HYPOTHESES.md (section "Research-only validation plan (Cycle 3)"). Using only freely accessible public data/docs (no paid APIs/datasets), prepare concrete data-acquisition specs and a validation checklist for a separate validator: enumerate exact public endpoints/sources for BTC 8h funding (Binance, Bybit), spot/perp prices/timestamps, fee schedules, and document coverage/history/limits/licensing. Define timestamp alignment rules, look-ahead prevention, OOS split (>=~4 months holdout) and walk-forward considerations, baseline definitions (no-change), cost model components (fees/slippage/funding/borrowing constraints conceptually), and explicit falsification tests per H1/H2. Do NOT compute returns/accuracy/half-lives or run backtests. Update research/HYPOTHESES.md and research/SEARCH_LOG.md. Do not make trading recommendations.
