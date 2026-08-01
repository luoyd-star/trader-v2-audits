# Trader-v2 Daily Health Check — 2026-08-01

_Generated at 2026-08-01 11:30:05 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`1181` last_exit=`(never`
  - uptime/rss: `09-08:31:24   4688`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`1177` last_exit=`(never`
  - uptime/rss: `09-08:31:24   2576`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 431.1h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **431.1h old** — news_agent may have stopped producing.

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

- **package_id**: `299`
- **generated_at**: `2026-08-01 09:47:11` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#300** (conf=0.28, horizon=2d, 4 symbols incl 1 primary)
  - Claim: Until fresh breadth confirms risk appetite, any failed rebound in broad tech should be treated as selective downside rather than chased long.
  - Falsification: The next completed NYSE session shows sustained positive breadth across SPY, QQQ, and the semiconductor cohort through the close, with no late-session reversal.

### Alternative hypotheses (rejected counter-theses)
- Mega-cap technology has already repaired and should be bought on the next session.
- Structural fiscal concerns justify an immediate long in gold.

---

## Planner Thesis Usage (today)

| Agent | Total new plans | With parent_thesis_id | Coverage |
|---|---|---|---|
| Agent_1_Momentum | 1 | 1 | 100% |
| Agent_2_MeanReversion | 1 | 1 | 100% |
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
| 2026-08-01 | $73,120 |
| 2026-07-31 | $73,120 |
| 2026-07-30 | $73,120 |
| 2026-07-29 | $73,120 |
| 2026-07-28 | $73,120 |
| 2026-07-27 | $73,120 |
| 2026-07-26 | $73,120 |
| 2026-07-25 | $73,120 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 1104 |
| Other ERROR | 165 |
| Python Traceback | 76 |
2 categories worth attention.

---

_End of snapshot._