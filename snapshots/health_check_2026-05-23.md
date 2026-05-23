# Trader-v2 Daily Health Check — 2026-05-23

_Generated at 2026-05-23 11:30:04 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`1294` last_exit=`(never`
  - uptime/rss: `12:15:54  28496`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`1292` last_exit=`(never`
  - uptime/rss: `12:15:54   9376`

---

## News-agent Freshness

- **latest folder**: `2026-05-22_09-30-08` (age: 26.0h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓

---

## Morning Batch (recent log markers)

Status of morning-batch markers in last ~5MB of log:
- `DAILY STRATEGIST START`: ✓
- `DAILY STRATEGIST END`: ✓
- `DAILY PLANNER START`: ✓
- `DAILY PLANNER END`: ✓
- `DAILY MACRO MANAGER START`: ✓
- `DAILY MACRO MANAGER END`: ✓
- `DAILY REVIEWER START`: ✓
- `DAILY REVIEWER END`: ✓

**Note**: presence in log means it ran *recently*, not necessarily today. Cross-reference with DB sections below for today-specific evidence (Strategist generated_at, plans created_at, etc.).

---

## Strategist Output (latest package)

- **package_id**: `6`
- **generated_at**: `2026-05-23 09:49:22` (age: 1.7h, today's: **YES**)
- **active_theses count**: 2 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#7** (conf=0.55, horizon=2d, 2 symbols incl 1 primary)
  - Claim: Today's FOMC minutes will fail to signal fiscal discipline or credible deficit reduction, sustaining the structurally broken real-yields→gold chain and keeping the gold-bond (GC=F-…
  - Falsification: GC=F-TLT 7d correlation drops below 0.75 within 24 hours of FOMC minutes release AND gold underperforms copper on a risk-adjusted basis during the same window, indicating the fiscal-premium narrative has collapsed and go…
- **#8** (conf=0.45, horizon=3d, 8 symbols incl 1 primary)
  - Claim: Tightening liquidity and late-phase momentum extremes in AI hardware have created asymmetric downside risk for semiconductor momentum longs, and today's FOMC volatility release wil…
  - Falsification: Semiconductor cohort (NVDAUSDT, AMDUSDT, TSMUSDT, AVGOUSDT) posts synchronized new 5-day highs on expanding volume within 48 hours of FOMC minutes AND NVDA-QQQ 7d realized correlation strengthens above 0.95 while implied…

### Alternative hypotheses (rejected counter-theses)
- Oil-bond decoupling (CL=F-TLT z=-2.734) marks the start of a sustained reflationary growth divergence where oil outperforms fixed income independent of rising y
- Broad risk-on continuation powered by resilient AI capex and post-FOMC relief sustains QQQ/SPY breakout trajectories without semiconductor profit-taking.

---

## Planner Thesis Usage (today)

| Agent | Total new plans | With parent_thesis_id | Coverage |
|---|---|---|---|
| Agent_2_MeanReversion | 1 | 1 | 100% |
| Agent_3_Macro | 3 | 3 | 100% |
| Agent_4_Volatility | 2 | 2 | 100% |
| Agent_5_Contrarian | 1 | 1 | 100% |
| Agent_7_PairsContrarian | 1 | 1 | 100% |

**System total: 8/8 plans linked to a thesis (100% if total else 0).**

---

## Manager Close Reasons (last 7 days)

| close_reason_type | Count | Total PnL |
|---|---|---|
| (null) | 6 | $929.0 |
| time_stop | 1 | $-95.0 |

⚠ **0 closes via thesis_falsified path.** Either no parent_thesis was actually broken in this window (fine), or the LLM never uses this path (concerning if persistent over multiple weeks).
Today's closes: 1 total — time_stop:1

---

## Reviewer 2x2 (last 7 days)

| outcome_type | adherence | thesis_consistency | Count |
|---|---|---|---|
| INVALIDATION_EXIT | PASS | CONSISTENT | 1 |
| LOSS | OPENING_PLAN_OBEYED, HOLDING_PLAN_VIOLATED, CLOSING_PLAN_VIOLATED | PARTIAL | 1 |
| NEGATIVE | VIOLATION | VIOLATION | 1 |
| WIN_TIME_STOP_EXIT | PARTIAL | ALIGNED | 1 |
| invalidation_not_respected | partial | unknown | 1 |
| profitable_but_premature | entry_and_hold_ok_exit_violation | intact | 1 |
| scratch_loss | PASS_WITH_NOTES | unknown | 1 |

**Note**: Phase 4's `thesis_validity` / `execution_quality` / `lesson_target` fields
are emitted by the Reviewer LLM but NOT yet persisted as columns in `review_records`.
Until that's wired (TODO), we surface only the legacy adherence/thesis_consistency.

Sanity check: if `outcome_type` is 100% 'SUCCESS', that's the LLM self-flattery red flag.

---

## Open Positions

| Agent | Symbol | Dir | Entry | Margin | Held/Max | % used | parent_thesis_id |
|---|---|---|---|---|---|---|---|
| A5_Contrarian | GEUSDT | LONG | 280.43 | $2000 | 111.6h / 120h | 93% | (legacy) |
| A5_Contrarian | ETHUSDT | LONG | 2129.11 | $2000 | 87.8h / 120h | 73% | (legacy) |
| A7_PairsContrarian | TSMUSDT | LONG | 397.5 | $1409 | 52.3h / 120h | 44% | (legacy) |
| A1_Momentum | NVDAUSDT | LONG | 221.5 | $2487 | 62.8h / 240h | 26% | (legacy) |
| A5_Contrarian | METAUSDT | LONG | 596.53 | $2200 | 27.4h / 120h | 23% | (legacy) |
| A1_Momentum | ARMUSDT | LONG | 265.63 | $2500 | 32.6h / 240h | 14% | (legacy) |

Total open: 6. Pre-Phase-2 legacy (no parent_thesis_id): 6.
⚠ 1 positions ≥80% of max_hold — approaching time stop.

---

## Equity (7-day trend, EOD per day)

| Day | Total equity (EOD) |
|---|---|
| 2026-05-23 | $72,183 |
| 2026-05-22 | $72,498 |
| 2026-05-21 | $71,789 |
| 2026-05-20 | $70,852 |
| 2026-05-19 | $70,706 |
| 2026-05-18 | $70,839 |
| 2026-05-17 | $70,976 |
| 2026-05-16 | $70,750 |
**Today vs yesterday: $-315**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 939 |
| Python Traceback | 359 |
| Other ERROR | 359 |
2 categories worth attention.

---

_End of snapshot._