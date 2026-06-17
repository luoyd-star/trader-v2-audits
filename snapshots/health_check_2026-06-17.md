# Trader-v2 Daily Health Check — 2026-06-17

_Generated at 2026-06-17 11:30:02 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`2179` last_exit=`(never`
  - uptime/rss: `04-16:13:45   6928`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`2176` last_exit=`(never`
  - uptime/rss: `04-16:13:45   4272`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 121.9h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **121.9h old** — news_agent may have stopped producing.

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

- **package_id**: `115`
- **generated_at**: `2026-06-17 09:45:34` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#116** (conf=0.42, horizon=3d, 5 symbols incl 1 primary)
  - Claim: Mixed risk appetite argues against chasing broad tech beta; tactical downside hedges are cleaner than new longs.
  - Falsification: Regime_Dashboard upgrades from mixed risk appetite to confirmed risk-on while breadth and pair-regime confirmations align for two consecutive sessions.

### Alternative hypotheses (rejected counter-theses)
- A broad risk-on continuation is underway and QQQ/SPY longs should be favored.
- Crypto beta should confirm equity risk-on through BTC and ETH longs.

---

## Planner Thesis Usage (today)

| Agent | Total new plans | With parent_thesis_id | Coverage |
|---|---|---|---|
| Agent_2_MeanReversion | 1 | 1 | 100% |
| Agent_5_Contrarian | 1 | 1 | 100% |
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
| 2026-06-17 | $73,538 |
| 2026-06-16 | $73,538 |
| 2026-06-15 | $73,538 |
| 2026-06-14 | $73,538 |
| 2026-06-13 | $73,538 |
| 2026-06-12 | $73,538 |
| 2026-06-11 | $73,538 |
| 2026-06-10 | $73,538 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 787 |
| Other ERROR | 224 |
| Python Traceback | 50 |
2 categories worth attention.

---

_End of snapshot._