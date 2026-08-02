# Trader-v2 Daily Health Check — 2026-08-02

_Generated at 2026-08-02 11:30:02 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`1181` last_exit=`(never`
  - uptime/rss: `10-08:31:22  11824`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`1177` last_exit=`(never`
  - uptime/rss: `10-08:31:22   2576`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 455.1h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **455.1h old** — news_agent may have stopped producing.

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

- **package_id**: `303`
- **generated_at**: `2026-08-02 09:47:33` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#304** (conf=0.31, horizon=2d, 4 symbols incl 1 primary)
  - Claim: Until fresh breadth data arrives, selective semiconductor downside is preferable to chasing long or making a broad-tech bearish bet.
  - Falsification: A fresh structured handoff shows broad semiconductor participation and improving mega-cap breadth for two consecutive completed sessions.

### Alternative hypotheses (rejected counter-theses)
- The July 31 session began a durable broad risk-on repair led by semiconductors and mega-cap technology.
- Macro uncertainty warrants an immediate broad defensive short across QQQ and SPY.

---

## Planner Thesis Usage (today)

| Agent | Total new plans | With parent_thesis_id | Coverage |
|---|---|---|---|
| Agent_1_Momentum | 2 | 2 | 100% |
| Agent_4_Volatility | 1 | 1 | 100% |
| Agent_5_Contrarian | 1 | 1 | 100% |
| Agent_7_PairsContrarian | 1 | 1 | 100% |

**System total: 5/5 plans linked to a thesis (100% if total else 0).**

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
| 2026-08-02 | $73,120 |
| 2026-08-01 | $73,120 |
| 2026-07-31 | $73,120 |
| 2026-07-30 | $73,120 |
| 2026-07-29 | $73,120 |
| 2026-07-28 | $73,120 |
| 2026-07-27 | $73,120 |
| 2026-07-26 | $73,120 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 1170 |
| Other ERROR | 165 |
| Python Traceback | 76 |
2 categories worth attention.

---

_End of snapshot._