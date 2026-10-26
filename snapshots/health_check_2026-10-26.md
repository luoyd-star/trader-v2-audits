# Trader-v2 Daily Health Check — 2026-10-26

_Generated at 2026-10-26 11:30:04 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`1154` last_exit=`(never`
  - uptime/rss: `16-15:32:52 453216`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`1151` last_exit=`(never`
  - uptime/rss: `16-15:32:52   7776`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 2495.1h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **2495.1h old** — news_agent may have stopped producing.

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

- **package_id**: `475`
- **generated_at**: `2026-10-26 09:45:36` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#476** (conf=0.10, horizon=1d, 1 symbols incl 1 primary)
  - Claim: If semiconductor leadership remains narrow, it will be insufficient to establish a durable broad technology recovery.
  - Falsification: Fresh session-aligned observations establish sustained participation across both semiconductor and non-semiconductor technology cohorts, with broad technology strength persisting beyond isolated semiconductor leaders.

### Alternative hypotheses (rejected counter-theses)
- Broad technology participation has recovered sufficiently to support a durable advance.
- A broad risk-off regime currently supports immediate technology shorts.

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
| 2026-10-26 | $73,120 |
| 2026-10-25 | $73,120 |
| 2026-10-24 | $73,120 |
| 2026-10-23 | $73,120 |
| 2026-10-22 | $73,120 |
| 2026-10-21 | $73,120 |
| 2026-10-20 | $73,120 |
| 2026-10-19 | $73,120 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 1685 |
| Other ERROR | 505 |
| Python Traceback | 105 |
2 categories worth attention.

---

_End of snapshot._