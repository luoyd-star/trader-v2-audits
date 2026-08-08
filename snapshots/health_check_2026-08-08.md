# Trader-v2 Daily Health Check — 2026-08-08

_Generated at 2026-08-08 11:30:05 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`1181` last_exit=`(never`
  - uptime/rss: `16-08:31:24   4768`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`1177` last_exit=`(never`
  - uptime/rss: `16-08:31:24   2544`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 599.1h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **599.1h old** — news_agent may have stopped producing.

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

- **package_id**: `323`
- **generated_at**: `2026-08-08 09:45:38` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#324** (conf=0.35, horizon=2d, 4 symbols incl 1 primary)
  - Claim: Absent fresh confirmation, broad US technology beta is more vulnerable to repricing than suitable for momentum chasing into Monday.
  - Falsification: A fresh structured handoff identifies a risk-on regime and both semiconductor and mega-cap technology breadth confirm it across two consecutive sessions.

### Alternative hypotheses (rejected counter-theses)
- The missing weekend report is informationally neutral, and Friday's prevailing risk trend will resume unchanged.
- Selective semiconductor weakness is immediately actionable through a MUUSDT short.

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
| 2026-08-08 | $73,120 |
| 2026-08-07 | $73,120 |
| 2026-08-06 | $73,120 |
| 2026-08-05 | $73,120 |
| 2026-08-04 | $73,120 |
| 2026-08-03 | $73,120 |
| 2026-08-02 | $73,120 |
| 2026-08-01 | $73,120 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 1264 |
| Other ERROR | 176 |
| Python Traceback | 76 |
2 categories worth attention.

---

_End of snapshot._