# Trader-v2 Daily Health Check — 2026-07-28

_Generated at 2026-07-28 11:30:02 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`1181` last_exit=`(never`
  - uptime/rss: `05-08:31:21   5104`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`1177` last_exit=`(never`
  - uptime/rss: `05-08:31:21   2928`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 335.1h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **335.1h old** — news_agent may have stopped producing.

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

- **package_id**: `283`
- **generated_at**: `2026-07-28 09:47:02` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#284** (conf=0.22, horizon=1d, 3 symbols incl 1 primary)
  - Claim: Absent broad confirmation, semiconductor strength should not be extrapolated into a durable mega-cap technology recovery.
  - Falsification: Semiconductors and non-semiconductor mega-cap technology both show positive breadth and sustained relative strength for two consecutive sessions.

### Alternative hypotheses (rejected counter-theses)
- A broad technology risk-on regime is already underway and semiconductor leadership is valid confirmation.
- A commodity-led inflation or geopolitical regime is the dominant driver today.

---

## Planner Thesis Usage (today)

| Agent | Total new plans | With parent_thesis_id | Coverage |
|---|---|---|---|
| Agent_1_Momentum | 1 | 1 | 100% |
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
| 2026-07-28 | $73,120 |
| 2026-07-27 | $73,120 |
| 2026-07-26 | $73,120 |
| 2026-07-25 | $73,120 |
| 2026-07-24 | $73,120 |
| 2026-07-23 | $73,120 |
| 2026-07-22 | $73,120 |
| 2026-07-21 | $73,120 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 1073 |
| Other ERROR | 182 |
| Python Traceback | 77 |
2 categories worth attention.

---

_End of snapshot._