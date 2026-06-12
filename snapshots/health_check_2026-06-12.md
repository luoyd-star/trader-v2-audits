# Trader-v2 Daily Health Check — 2026-06-12

_Generated at 2026-06-12 11:30:02 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`1013` last_exit=`(never`
  - uptime/rss: `16:39:43  12496`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`1008` last_exit=`(never`
  - uptime/rss: `16:39:43   7760`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 1.9h)
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

- **package_id**: `93`
- **generated_at**: `2026-06-12 09:45:34` (age: 1.7h, today's: **YES**)
- **active_theses count**: 2 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#94** (conf=0.54, horizon=3d, 4 symbols incl 1 primary)
  - Claim: The QQQ rebound is fragile until volatility, credit, liquidity, and breadth confirm risk-on together.
  - Falsification: VIX falls below 18, HYG reclaims ema200, liquidity stops tightening, and market breadth broadens beyond mega-cap AI for 2 sessions.
- **#95** (conf=0.50, horizon=5d, 5 symbols incl 1 primary)
  - Claim: Extended high-beta semiconductor and APAC AI-linked names should be observed, not chased.
  - Falsification: Extended semiconductor and APAC AI-linked cohort cools without distribution, then ASML/EWY/INTC/MRVL regain leadership with broad volume confirmation across 2 sessions.

### Alternative hypotheses (rejected counter-theses)
- The QQQ rebound is a durable risk-on restart.
- Gold should be bought as the clean hedge against real-yield and fiscal stress.

---

## Planner Thesis Usage (today)

| Agent | Total new plans | With parent_thesis_id | Coverage |
|---|---|---|---|
| Agent_1_Momentum | 1 | 1 | 100% |
| Agent_2_MeanReversion | 6 | 6 | 100% |
| Agent_3_Macro | 3 | 3 | 100% |
| Agent_4_Volatility | 2 | 2 | 100% |
| Agent_5_Contrarian | 3 | 3 | 100% |
| Agent_7_PairsContrarian | 2 | 2 | 100% |

**System total: 17/17 plans linked to a thesis (100% if total else 0).**

---

## Manager Close Reasons (last 7 days)

(no closes in last 7d)

---

## Reviewer 2x2 (last 7 days)

(no reviews in last 7d)

---

## Open Positions

(no open trades)

---

## Equity (7-day trend, EOD per day)

| Day | Total equity (EOD) |
|---|---|
| 2026-06-12 | $73,538 |
| 2026-06-11 | $73,538 |
| 2026-06-10 | $73,538 |
| 2026-06-09 | $73,538 |
| 2026-06-08 | $73,538 |
| 2026-06-07 | $73,538 |
| 2026-06-06 | $73,538 |
| 2026-06-05 | $73,538 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 813 |
| Other ERROR | 257 |
| Python Traceback | 81 |
2 categories worth attention.

---

_End of snapshot._