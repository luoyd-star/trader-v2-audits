# Trader-v2 Daily Health Check — 2026-08-26

_Generated at 2026-08-26 11:30:02 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`817` last_exit=`(never`
  - uptime/rss: `17-09:54:55  41856`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`812` last_exit=`(never`
  - uptime/rss: `17-09:54:55   8928`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 1031.1h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **1031.1h old** — news_agent may have stopped producing.

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

- **package_id**: `395`
- **generated_at**: `2026-08-26 09:45:42` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#396** (conf=0.28, horizon=3d, 4 symbols incl 1 primary)
  - Claim: Without fresh breadth or catalyst confirmation, high-beta semiconductors remain more vulnerable to selective downside than broad upside continuation.
  - Falsification: Semiconductor breadth broadens across ARM, MU, NVDA, TSM, ASML, and AVGO for two consecutive sessions while a fresh analyst handoff identifies a common positive catalyst.

### Alternative hypotheses (rejected counter-theses)
- A broad mega-cap technology repair is beginning and semiconductor leadership will expand into QQQ.
- Fiscal concerns are re-establishing a durable long-gold regime.

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
| 2026-08-26 | $73,120 |
| 2026-08-25 | $73,120 |
| 2026-08-24 | $73,120 |
| 2026-08-23 | $73,120 |
| 2026-08-22 | $73,120 |
| 2026-08-21 | $73,120 |
| 2026-08-20 | $73,120 |
| 2026-08-19 | $73,120 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 1390 |
| Other ERROR | 56 |
| Python Traceback | 6 |
2 categories worth attention.

---

_End of snapshot._