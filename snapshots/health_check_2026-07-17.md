# Trader-v2 Daily Health Check — 2026-07-17

_Generated at 2026-07-17 11:30:03 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`40806` last_exit=`never`
  - uptime/rss: `01-16:06:46   8960`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`40804` last_exit=`never`
  - uptime/rss: `01-16:06:46   6384`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 71.1h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **71.1h old** — news_agent may have stopped producing.

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

- **package_id**: `239`
- **generated_at**: `2026-07-17 09:45:41` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#240** (conf=0.28, horizon=2d, 4 symbols incl 1 primary)
  - Claim: Absent current confirmation and with unreliable semiconductor breadth, tactical QQQ downside is favored over chasing technology longs.
  - Falsification: QQQ, SPY, NVDA, AMD, AVGO, and TSM show coordinated positive breadth while the next structured handoff confirms a risk-on regime for two consecutive sessions.

### Alternative hypotheses (rejected counter-theses)
- Broad technology leadership has repaired and QQQ should be bought.
- Gold should be bought as a structural fiscal-risk hedge.

---

## Planner Thesis Usage (today)

| Agent | Total new plans | With parent_thesis_id | Coverage |
|---|---|---|---|
| Agent_1_Momentum | 1 | 1 | 100% |
| Agent_4_Volatility | 2 | 2 | 100% |
| Agent_7_PairsContrarian | 2 | 2 | 100% |

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
| 2026-07-17 | $73,120 |
| 2026-07-16 | $73,120 |
| 2026-07-15 | $73,120 |
| 2026-07-14 | $73,120 |
| 2026-07-13 | $73,120 |
| 2026-07-12 | $73,120 |
| 2026-07-11 | $73,120 |
| 2026-07-10 | $73,120 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 1025 |
| Other ERROR | 55 |
| Python Traceback | 3 |
2 categories worth attention.

---

_End of snapshot._