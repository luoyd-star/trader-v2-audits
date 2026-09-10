# Trader-v2 Daily Health Check — 2026-09-10

_Generated at 2026-09-10 11:30:04 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`817` last_exit=`(never`
  - uptime/rss: `32-09:54:57  61968`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`812` last_exit=`(never`
  - uptime/rss: `32-09:54:57   5984`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 1391.1h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **1391.1h old** — news_agent may have stopped producing.

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

## Strategist Output (latest package) ⚠ NOT TODAY

- **package_id**: `435`
- **generated_at**: `2026-09-05 09:45:43` (age: 121.7h, today's: **NO — STALE**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#436** (conf=0.34, horizon=3d, 4 symbols incl 1 primary)
  - Claim: Absent fresh breadth confirmation, narrow semiconductor leadership remains vulnerable, with ARM the cleanest selective short expression.
  - Falsification: A fresh analyst handoff shows ARM, NVDA, AMD, ASML, and MU participating in broad semiconductor strength alongside QQQ for two consecutive completed sessions.

### Alternative hypotheses (rejected counter-theses)
- Mega-cap technology has repaired and broad semiconductor strength now supports renewed QQQ upside.
- Structural fiscal concerns have restored gold as the cleanest defensive long.

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
| 2026-09-10 | $73,120 |
| 2026-09-09 | $73,120 |
| 2026-09-08 | $73,120 |
| 2026-09-07 | $73,120 |
| 2026-09-06 | $73,120 |
| 2026-09-05 | $73,120 |
| 2026-09-04 | $73,120 |
| 2026-09-03 | $73,120 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 1528 |
| Other ERROR | 247 |
| Python Traceback | 7 |
2 categories worth attention.

---

_End of snapshot._