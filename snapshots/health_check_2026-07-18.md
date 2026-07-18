# Trader-v2 Daily Health Check — 2026-07-18

_Generated at 2026-07-18 11:30:05 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`40806` last_exit=`never`
  - uptime/rss: `02-16:06:48   8784`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`40804` last_exit=`never`
  - uptime/rss: `02-16:06:48   6192`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 95.1h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **95.1h old** — news_agent may have stopped producing.

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

- **package_id**: `243`
- **generated_at**: `2026-07-18 09:47:03` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#244** (conf=0.22, horizon=2d, 3 symbols incl 1 primary)
  - Claim: Narrow semiconductor leadership remains unreliable, favoring selective downside over broad technology continuation.
  - Falsification: MU, ARM, NVDA, TSM, and ASML simultaneously develop improving breadth while QQQ confirms the advance for two consecutive sessions.

### Alternative hypotheses (rejected counter-theses)
- A durable broad mega-cap technology repair is underway.
- Fiscal-risk concerns are reactivating a durable precious-metals breakout.

---

## Planner Thesis Usage (today)

| Agent | Total new plans | With parent_thesis_id | Coverage |
|---|---|---|---|
| Agent_1_Momentum | 1 | 1 | 100% |
| Agent_4_Volatility | 1 | 1 | 100% |
| Agent_7_PairsContrarian | 1 | 1 | 100% |

**System total: 3/3 plans linked to a thesis (100% if total else 0).**

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
| 2026-07-18 | $73,120 |
| 2026-07-17 | $73,120 |
| 2026-07-16 | $73,120 |
| 2026-07-15 | $73,120 |
| 2026-07-14 | $73,120 |
| 2026-07-13 | $73,120 |
| 2026-07-12 | $73,120 |
| 2026-07-11 | $73,120 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 1054 |
| Other ERROR | 55 |
| Python Traceback | 3 |
2 categories worth attention.

---

_End of snapshot._