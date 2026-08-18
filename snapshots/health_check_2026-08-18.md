# Trader-v2 Daily Health Check — 2026-08-18

_Generated at 2026-08-18 11:30:02 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`817` last_exit=`(never`
  - uptime/rss: `09-09:54:55 193936`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`812` last_exit=`(never`
  - uptime/rss: `09-09:54:55   9136`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 839.1h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **839.1h old** — news_agent may have stopped producing.

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

- **package_id**: `363`
- **generated_at**: `2026-08-18 09:45:54` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#364** (conf=0.31, horizon=2d, 4 symbols incl 1 primary)
  - Claim: Without broad confirmation, narrow semiconductor leadership is more likely to mean-revert than produce a durable technology-sector advance.
  - Falsification: NVDA, AMD, ARM, ASML, and TSM exhibit synchronized positive breadth with QQQ confirmation across two consecutive sessions and the upstream handoff upgrades the regime to broad risk-on.

### Alternative hypotheses (rejected counter-theses)
- Semiconductor strength is the first leg of a broad mega-cap technology repair.
- Fiscal-risk concerns are reactivating a durable gold-led defensive regime.

---

## Planner Thesis Usage (today)

| Agent | Total new plans | With parent_thesis_id | Coverage |
|---|---|---|---|
| Agent_2_MeanReversion | 1 | 1 | 100% |
| Agent_4_Volatility | 1 | 1 | 100% |
| Agent_5_Contrarian | 1 | 1 | 100% |

**System total: 3/3 plans linked to a thesis (100% if total else 0).**

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
| 2026-08-18 | $73,120 |
| 2026-08-17 | $73,120 |
| 2026-08-16 | $73,120 |
| 2026-08-15 | $73,120 |
| 2026-08-14 | $73,120 |
| 2026-08-13 | $73,120 |
| 2026-08-12 | $73,120 |
| 2026-08-11 | $73,120 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 1320 |
| Other ERROR | 180 |
| Python Traceback | 76 |
2 categories worth attention.

---

_End of snapshot._