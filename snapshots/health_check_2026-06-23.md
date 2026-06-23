# Trader-v2 Daily Health Check — 2026-06-23

_Generated at 2026-06-23 11:30:05 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`2179` last_exit=`(never`
  - uptime/rss: `10-16:13:48   6368`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`2176` last_exit=`(never`
  - uptime/rss: `10-16:13:48   3632`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 265.9h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **265.9h old** — news_agent may have stopped producing.

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

## Strategist Output (latest package) ⚠ NOT TODAY

- **package_id**: `131`
- **generated_at**: `2026-06-22 09:45:36` (age: 25.7h, today's: **NO — STALE**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#132** (conf=0.62, horizon=1d, 4 symbols incl 1 primary)
  - Claim: Market state is not trade-authoritative today; avoid broad beta chase until Regime_Dashboard and fresh handoff confirm direction.
  - Falsification: Regime_Dashboard, structured handoff, and non-noise scorecard buckets all align on a fresh risk-on regime for one full session.

### Alternative hypotheses (rejected counter-theses)
- A fresh risk-on tape justifies broad QQQ/SPY and crypto beta longs.
- Crypto should lead because equity calm implies abundant liquidity.

---

## Planner Thesis Usage (today)

| Agent | Total new plans | With parent_thesis_id | Coverage |
|---|---|---|---|
| Agent_1_Momentum | 1 | 1 | 100% |
| Agent_5_Contrarian | 1 | 1 | 100% |

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
| 2026-06-23 | $73,538 |
| 2026-06-22 | $73,538 |
| 2026-06-21 | $73,538 |
| 2026-06-20 | $73,538 |
| 2026-06-19 | $73,538 |
| 2026-06-18 | $73,538 |
| 2026-06-17 | $73,538 |
| 2026-06-16 | $73,538 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 944 |
| Other ERROR | 194 |
| Python Traceback | 1 |
2 categories worth attention.

---

_End of snapshot._