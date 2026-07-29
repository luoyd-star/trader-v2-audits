# Trader-v2 Daily Health Check — 2026-07-29

_Generated at 2026-07-29 11:30:05 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`1181` last_exit=`(never`
  - uptime/rss: `06-08:31:24   5104`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`1177` last_exit=`(never`
  - uptime/rss: `06-08:31:24   2912`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 359.1h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **359.1h old** — news_agent may have stopped producing.

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

- **package_id**: `287`
- **generated_at**: `2026-07-29 09:47:08` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#288** (conf=0.34, horizon=3d, 4 symbols incl 1 primary)
  - Claim: For the next 1-3 sessions, semiconductor weakness is more credible as selective downside than as a broad technology-market signal.
  - Falsification: Invalidate if MU and ARM cease underperforming while NVDA, AVGO, TSM, and ASML show coordinated positive breadth for two consecutive sessions.

### Alternative hypotheses (rejected counter-theses)
- A coordinated semiconductor rebound is repairing broad mega-cap technology leadership.
- The missing upstream evidence itself justifies an immediate broad risk-off position.

---

## Planner Thesis Usage (today)

| Agent | Total new plans | With parent_thesis_id | Coverage |
|---|---|---|---|
| Agent_1_Momentum | 2 | 2 | 100% |
| Agent_4_Volatility | 2 | 2 | 100% |
| Agent_5_Contrarian | 2 | 2 | 100% |
| Agent_7_PairsContrarian | 1 | 1 | 100% |

**System total: 7/7 plans linked to a thesis (100% if total else 0).**

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
| 2026-07-29 | $73,120 |
| 2026-07-28 | $73,120 |
| 2026-07-27 | $73,120 |
| 2026-07-26 | $73,120 |
| 2026-07-25 | $73,120 |
| 2026-07-24 | $73,120 |
| 2026-07-23 | $73,120 |
| 2026-07-22 | $73,120 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 1055 |
| Other ERROR | 179 |
| Python Traceback | 78 |
2 categories worth attention.

---

_End of snapshot._