# Trader-v2 Daily Health Check — 2026-06-26

_Generated at 2026-06-26 11:30:04 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`2235` last_exit=`(never`
  - uptime/rss: `01-20:58:42   8944`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`2231` last_exit=`(never`
  - uptime/rss: `01-20:58:43   5936`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 337.9h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **337.9h old** — news_agent may have stopped producing.

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

- **package_id**: `144`
- **generated_at**: `2026-06-26 09:45:30` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#145** (conf=0.42, horizon=3d, 5 symbols incl 1 primary)
  - Claim: Sparse evidence plus repeated failed risk-on chains favors fading broad QQQ risk-on chase today.
  - Falsification: Regime_Dashboard confirms clean risk-on while rotation scorecards show broad T+3 hit rates above 50% and crypto Pair_Regime confirms beta repair.

### Alternative hypotheses (rejected counter-theses)
- Equity calm is a valid clean risk-on signal and supports long beta exposure.
- Crypto should be bought as beta confirmation of equity risk appetite.

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
| 2026-06-26 | $73,538 |
| 2026-06-25 | $73,538 |
| 2026-06-24 | $73,538 |
| 2026-06-23 | $73,538 |
| 2026-06-22 | $73,538 |
| 2026-06-21 | $73,538 |
| 2026-06-20 | $73,538 |
| 2026-06-19 | $73,538 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 938 |
| Other ERROR | 80 |
| Python Traceback | 1 |
2 categories worth attention.

---

_End of snapshot._