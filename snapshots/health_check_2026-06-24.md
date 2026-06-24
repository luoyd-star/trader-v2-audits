# Trader-v2 Daily Health Check — 2026-06-24

_Generated at 2026-06-24 11:30:03 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`2179` last_exit=`(never`
  - uptime/rss: `11-16:13:46   6224`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`2176` last_exit=`(never`
  - uptime/rss: `11-16:13:46   3552`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 289.9h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **289.9h old** — news_agent may have stopped producing.

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

- **package_id**: `135`
- **generated_at**: `2026-06-24 09:45:31` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#136** (conf=0.31, horizon=3d, 4 symbols incl 1 primary)
  - Claim: Broad risk-on confirmation is not validated, so index beta longs should be treated as fragile rather than chased.
  - Falsification: Regime_Dashboard confirms broad risk-on while RS, Driver_Residual, and Pair_Regime all align for risk appetite for two sessions.

### Alternative hypotheses (rejected counter-theses)
- A clean risk-on regime is active and should be bought through QQQ and AI leaders.
- Crypto beta should lead if equities stabilize.

---

## Planner Thesis Usage (today)

| Agent | Total new plans | With parent_thesis_id | Coverage |
|---|---|---|---|
| Agent_2_MeanReversion | 2 | 2 | 100% |
| Agent_4_Volatility | 2 | 2 | 100% |

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
| 2026-06-24 | $73,538 |
| 2026-06-23 | $73,538 |
| 2026-06-22 | $73,538 |
| 2026-06-21 | $73,538 |
| 2026-06-20 | $73,538 |
| 2026-06-19 | $73,538 |
| 2026-06-18 | $73,538 |
| 2026-06-17 | $73,538 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 932 |
| Other ERROR | 194 |
| Python Traceback | 1 |
2 categories worth attention.

---

_End of snapshot._