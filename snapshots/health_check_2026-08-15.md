# Trader-v2 Daily Health Check — 2026-08-15

_Generated at 2026-08-15 11:30:01 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`817` last_exit=`(never`
  - uptime/rss: `06-09:54:54 266032`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`812` last_exit=`(never`
  - uptime/rss: `06-09:54:54   9248`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 767.1h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **767.1h old** — news_agent may have stopped producing.

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

- **package_id**: `351`
- **generated_at**: `2026-08-15 09:45:30` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#352** (conf=0.31, horizon=3d, 3 symbols incl 1 primary)
  - Claim: Recent failure history favors selective semiconductor downside over extrapolating narrow chip leadership into broad tech strength.
  - Falsification: MU and ARM outperform QQQ for two consecutive completed sessions while leadership broadens across AMD, ASML, NVDA, and TSM.

### Alternative hypotheses (rejected counter-theses)
- Broad mega-cap technology leadership is repairing and QQQ should be bought.
- Persistent fiscal concerns justify an immediate long in gold.

---

## Planner Thesis Usage (today)

| Agent | Total new plans | With parent_thesis_id | Coverage |
|---|---|---|---|
| Agent_1_Momentum | 2 | 2 | 100% |
| Agent_7_PairsContrarian | 2 | 2 | 100% |

**System total: 4/4 plans linked to a thesis (100% if total else 0).**

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
| 2026-08-15 | $73,120 |
| 2026-08-14 | $73,120 |
| 2026-08-13 | $73,120 |
| 2026-08-12 | $73,120 |
| 2026-08-11 | $73,120 |
| 2026-08-10 | $73,120 |
| 2026-08-09 | $73,120 |
| 2026-08-08 | $73,120 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 1319 |
| Other ERROR | 180 |
| Python Traceback | 76 |
2 categories worth attention.

---

_End of snapshot._