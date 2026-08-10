# Trader-v2 Daily Health Check — 2026-08-10

_Generated at 2026-08-10 11:30:00 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`817` last_exit=`(never`
  - uptime/rss: `01-09:54:53 329328`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`812` last_exit=`(never`
  - uptime/rss: `01-09:54:53  10464`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 647.1h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **647.1h old** — news_agent may have stopped producing.

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

- **package_id**: `331`
- **generated_at**: `2026-08-10 09:45:45` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#332** (conf=0.31, horizon=2d, 3 symbols incl 1 primary)
  - Claim: Absent fresh breadth confirmation, broad technology downside is cleaner than chasing semiconductor-led upside over the next two sessions.
  - Falsification: A populated analyst handoff identifies a constructive regime and both semiconductor and mega-cap technology cohorts show broad, internally consistent participation for two consecutive sessions.

### Alternative hypotheses (rejected counter-theses)
- The correct stance is fully neutral because the upstream data package contains no usable market evidence.
- Semiconductor leadership is beginning a durable broad technology risk-on phase.

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
| 2026-08-10 | $73,120 |
| 2026-08-09 | $73,120 |
| 2026-08-08 | $73,120 |
| 2026-08-07 | $73,120 |
| 2026-08-06 | $73,120 |
| 2026-08-05 | $73,120 |
| 2026-08-04 | $73,120 |
| 2026-08-03 | $73,120 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 1261 |
| Other ERROR | 177 |
| Python Traceback | 76 |
2 categories worth attention.

---

_End of snapshot._