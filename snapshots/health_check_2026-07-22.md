# Trader-v2 Daily Health Check — 2026-07-22

_Generated at 2026-07-22 11:30:00 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`40806` last_exit=`never`
  - uptime/rss: `06-16:06:43   5056`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`40804` last_exit=`never`
  - uptime/rss: `06-16:06:43   4432`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 191.1h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **191.1h old** — news_agent may have stopped producing.

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

- **package_id**: `259`
- **generated_at**: `2026-07-22 09:46:51` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#260** (conf=0.34, horizon=2d, 4 symbols incl 1 primary)
  - Claim: Narrow semiconductor leadership remains vulnerable to selective downside and should not be treated as broad technology repair.
  - Falsification: Semiconductor breadth broadens across ARM, NVDA, AMD, TSM, ASML, MU and AVGO while QQQ leadership also strengthens for two consecutive sessions.

### Alternative hypotheses (rejected counter-theses)
- Broad mega-cap technology repair supports new QQQ longs.
- Structural fiscal concerns justify a renewed gold long.

---

## Planner Thesis Usage (today)

| Agent | Total new plans | With parent_thesis_id | Coverage |
|---|---|---|---|
| Agent_1_Momentum | 2 | 2 | 100% |
| Agent_4_Volatility | 2 | 2 | 100% |
| Agent_5_Contrarian | 1 | 1 | 100% |
| Agent_7_PairsContrarian | 2 | 2 | 100% |

**System total: 7/7 plans linked to a thesis (100% if total else 0).**

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
| 2026-07-22 | $73,120 |
| 2026-07-21 | $73,120 |
| 2026-07-20 | $73,120 |
| 2026-07-19 | $73,120 |
| 2026-07-18 | $73,120 |
| 2026-07-17 | $73,120 |
| 2026-07-16 | $73,120 |
| 2026-07-15 | $73,120 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 1029 |
| Other ERROR | 54 |
| Python Traceback | 3 |
2 categories worth attention.

---

_End of snapshot._