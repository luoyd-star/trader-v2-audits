# Trader-v2 Daily Health Check — 2026-08-23

_Generated at 2026-08-23 11:30:03 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`817` last_exit=`(never`
  - uptime/rss: `14-09:54:56 315536`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`812` last_exit=`(never`
  - uptime/rss: `14-09:54:56   8928`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 959.1h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **959.1h old** — news_agent may have stopped producing.

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

- **package_id**: `383`
- **generated_at**: `2026-08-23 09:45:32` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#384** (conf=0.32, horizon=3d, 4 symbols incl 1 primary)
  - Claim: Absent fresh breadth confirmation, narrow semiconductor leadership leaves QQQ vulnerable to selective downside rather than a durable tech advance.
  - Falsification: Semiconductors and non-semiconductor mega-cap constituents both demonstrate broad positive participation for two consecutive completed sessions, with a fresh structured handoff confirming the repair.

### Alternative hypotheses (rejected counter-theses)
- Broad mega-cap technology has repaired and QQQ should be bought on continuation.
- Gold should be bought as a structural fiscal-risk hedge.

---

## Planner Thesis Usage (today)

| Agent | Total new plans | With parent_thesis_id | Coverage |
|---|---|---|---|
| Agent_1_Momentum | 2 | 2 | 100% |
| Agent_2_MeanReversion | 2 | 2 | 100% |
| Agent_4_Volatility | 2 | 2 | 100% |
| Agent_5_Contrarian | 2 | 2 | 100% |
| Agent_7_PairsContrarian | 1 | 1 | 100% |

**System total: 9/9 plans linked to a thesis (100% if total else 0).**

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
| 2026-08-23 | $73,120 |
| 2026-08-22 | $73,120 |
| 2026-08-21 | $73,120 |
| 2026-08-20 | $73,120 |
| 2026-08-19 | $73,120 |
| 2026-08-18 | $73,120 |
| 2026-08-17 | $73,120 |
| 2026-08-16 | $73,120 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 1347 |
| Other ERROR | 147 |
| Python Traceback | 54 |
2 categories worth attention.

---

_End of snapshot._