# Trader-v2 Daily Health Check — 2026-08-09

_Generated at 2026-08-09 11:30:01 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`817` last_exit=`(never`
  - uptime/rss: `09:54:54 211616`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`812` last_exit=`(never`
  - uptime/rss: `09:54:54  11552`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 623.1h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **623.1h old** — news_agent may have stopped producing.

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

- **package_id**: `327`
- **generated_at**: `2026-08-09 09:45:35` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#328** (conf=0.31, horizon=2d, 4 symbols incl 1 primary)
  - Claim: Until fresh-session breadth confirms risk appetite, broad tech exposure has an asymmetric downside bias and should not be chased long.
  - Falsification: Fresh-session breadth becomes broadly positive across QQQ, SPY, and the semiconductor cohort for two consecutive observations, with leadership extending beyond a small subset of chip names.

### Alternative hypotheses (rejected counter-theses)
- Friday's risk-on structure will resume when markets reopen, making QQQ and semiconductor longs preferable.
- The information gap is best handled with complete neutrality rather than a conditional downside bias.

---

## Planner Thesis Usage (today)

| Agent | Total new plans | With parent_thesis_id | Coverage |
|---|---|---|---|
| Agent_5_Contrarian | 1 | 1 | 100% |

**System total: 1/1 plans linked to a thesis (100% if total else 0).**

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
| 2026-08-09 | $73,120 |
| 2026-08-08 | $73,120 |
| 2026-08-07 | $73,120 |
| 2026-08-06 | $73,120 |
| 2026-08-05 | $73,120 |
| 2026-08-04 | $73,120 |
| 2026-08-03 | $73,120 |
| 2026-08-02 | $73,120 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 1269 |
| Other ERROR | 177 |
| Python Traceback | 76 |
2 categories worth attention.

---

_End of snapshot._