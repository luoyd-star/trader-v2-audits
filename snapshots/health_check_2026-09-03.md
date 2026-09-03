# Trader-v2 Daily Health Check — 2026-09-03

_Generated at 2026-09-03 11:30:06 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`817` last_exit=`(never`
  - uptime/rss: `25-09:54:59 533792`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`812` last_exit=`(never`
  - uptime/rss: `25-09:54:59   6112`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 1223.1h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **1223.1h old** — news_agent may have stopped producing.

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

- **package_id**: `427`
- **generated_at**: `2026-09-03 09:45:31` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#428** (conf=0.28, horizon=2d, 4 symbols incl 1 primary)
  - Claim: Until breadth confirms, fade extended QQQ upside rather than extrapolating narrow semiconductor leadership.
  - Falsification: Semiconductors and at least four non-semiconductor mega-cap technology names show aligned positive breadth and persistence for two consecutive sessions.

### Alternative hypotheses (rejected counter-theses)
- A durable broad risk-on regime is beginning, led by semiconductors and mega-cap technology.
- Macro stress justifies an immediate broad-market short without waiting for confirmation.

---

## Planner Thesis Usage (today)

| Agent | Total new plans | With parent_thesis_id | Coverage |
|---|---|---|---|
| Agent_2_MeanReversion | 1 | 1 | 100% |
| Agent_7_PairsContrarian | 1 | 1 | 100% |

**System total: 2/2 plans linked to a thesis (100% if total else 0).**

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
| 2026-09-03 | $73,120 |
| 2026-09-02 | $73,120 |
| 2026-09-01 | $73,120 |
| 2026-08-31 | $73,120 |
| 2026-08-30 | $73,120 |
| 2026-08-29 | $73,120 |
| 2026-08-28 | $73,120 |
| 2026-08-27 | $73,120 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 1464 |
| Other ERROR | 71 |
| Python Traceback | 8 |
2 categories worth attention.

---

_End of snapshot._