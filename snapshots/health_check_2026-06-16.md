# Trader-v2 Daily Health Check — 2026-06-16

_Generated at 2026-06-16 11:30:05 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`2179` last_exit=`(never`
  - uptime/rss: `03-16:13:48   8768`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`2176` last_exit=`(never`
  - uptime/rss: `03-16:13:48   5984`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 97.9h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **97.9h old** — news_agent may have stopped producing.

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

- **package_id**: `110`
- **generated_at**: `2026-06-16 09:45:36` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 3 (expected ≥1)

### Active theses (the spine of today's trading)
- **#111** (conf=0.46, horizon=3d, 6 symbols incl 1 primary)
  - Claim: Mixed risk appetite plus QQQ-rate regime break argues against chasing duration-tech beta today.
  - Falsification: QQQ-rate break loses leadership relevance and risk_appetite upgrades from mixed to confirmed broad risk-on across the authoritative Regime_Dashboard for two consecutive sessions.

### Alternative hypotheses (rejected counter-theses)
- A clean risk-on rebound is starting and QQQ should be bought.
- Crypto beta will confirm equity strength via BTC and ETH longs.
- Rotation or cluster migration is the main tradable signal today.

---

## Planner Thesis Usage (today)

| Agent | Total new plans | With parent_thesis_id | Coverage |
|---|---|---|---|
| Agent_1_Momentum | 3 | 3 | 100% |
| Agent_2_MeanReversion | 3 | 3 | 100% |
| Agent_3_Macro | 2 | 2 | 100% |
| Agent_4_Volatility | 4 | 4 | 100% |
| Agent_5_Contrarian | 3 | 3 | 100% |
| Agent_7_PairsContrarian | 2 | 2 | 100% |

**System total: 17/17 plans linked to a thesis (100% if total else 0).**

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
| 2026-06-16 | $73,538 |
| 2026-06-15 | $73,538 |
| 2026-06-14 | $73,538 |
| 2026-06-13 | $73,538 |
| 2026-06-12 | $73,538 |
| 2026-06-11 | $73,538 |
| 2026-06-10 | $73,538 |
| 2026-06-09 | $73,538 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 798 |
| Other ERROR | 241 |
| Python Traceback | 67 |
2 categories worth attention.

---

_End of snapshot._