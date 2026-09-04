# Trader-v2 Daily Health Check — 2026-09-04

_Generated at 2026-09-04 11:30:03 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`817` last_exit=`(never`
  - uptime/rss: `26-09:54:56  51472`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`812` last_exit=`(never`
  - uptime/rss: `26-09:54:56   6080`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 1247.1h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **1247.1h old** — news_agent may have stopped producing.

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

- **package_id**: `431`
- **generated_at**: `2026-09-04 09:45:33` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#432** (conf=0.31, horizon=3d, 5 symbols incl 1 primary)
  - Claim: Narrow semiconductor leadership will not confirm a durable broad-tech repair, leaving QQQ tactically vulnerable over the next three sessions.
  - Falsification: Semiconductors and the AAPL/MSFT/GOOGL/AMZN/META cohort advance together with improving breadth for two consecutive sessions.

### Alternative hypotheses (rejected counter-theses)
- Broad technology repair is already durable and QQQ should be bought on continuation.
- A fresh macro shock favors an immediate long in gold.

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
| 2026-09-04 | $73,120 |
| 2026-09-03 | $73,120 |
| 2026-09-02 | $73,120 |
| 2026-09-01 | $73,120 |
| 2026-08-31 | $73,120 |
| 2026-08-30 | $73,120 |
| 2026-08-29 | $73,120 |
| 2026-08-28 | $73,120 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 1469 |
| Other ERROR | 68 |
| Python Traceback | 8 |
2 categories worth attention.

---

_End of snapshot._