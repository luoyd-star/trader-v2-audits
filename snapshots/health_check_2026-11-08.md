# Trader-v2 Daily Health Check — 2026-11-08

_Generated at 2026-11-08 11:30:05 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`1122` last_exit=`(never`
  - uptime/rss: `11:32:40 276112`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`1120` last_exit=`(never`
  - uptime/rss: `11:32:40   9760`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 2807.1h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **2807.1h old** — news_agent may have stopped producing.

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

- **package_id**: `491`
- **generated_at**: `2026-11-08 09:45:42` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#492** (conf=0.90, horizon=1d, 2 symbols incl 1 primary)
  - Claim: Broad equity upside remains unconfirmed; isolated semiconductor strength cannot establish a market-wide recovery.
  - Falsification: A fresh completed-session report establishes positive broad-index performance, advancing breadth, and participation across semiconductor and non-technology sectors, replacing the current absence of broad confirmation.

### Alternative hypotheses (rejected counter-theses)
- Semiconductor leadership is driving a durable broad-market advance.
- A broad risk-off reversal favors immediate equity shorts.

---

## Planner Thesis Usage (today)

**No plans created today yet.** Either Planner hasn't run, or it produced 0 plans (correct behavior if no fitting thesis).

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
| 2026-11-08 | $73,120 |

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 1677 |
| Other ERROR | 385 |
| Python Traceback | 45 |
2 categories worth attention.

---

_End of snapshot._