# Trader-v2 Daily Health Check — 2026-06-25

_Generated at 2026-06-25 11:30:05 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`2235` last_exit=`(never`
  - uptime/rss: `20:58:43  11952`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`2231` last_exit=`(never`
  - uptime/rss: `20:58:43   7424`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 313.9h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **313.9h old** — news_agent may have stopped producing.

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

- **package_id**: `139`
- **generated_at**: `2026-06-25 09:45:32` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 3 (expected ≥1)

### Active theses (the spine of today's trading)
- **#140** (conf=0.42, horizon=3d, 5 symbols incl 1 primary)
  - Claim: Liquidity compression makes broad tech/AI momentum vulnerable to failed follow-through rather than clean upside chase.
  - Falsification: Regime_Dashboard confirms clean risk-on and semiconductor leadership broadens across NVDA/AMD/ASML/TSM without liquidity-budget warnings for a full session.

### Alternative hypotheses (rejected counter-theses)
- Low VIX and equity calm signal a clean risk-on regime with room for broad long exposure.
- Semiconductor relative strength is a valid chase signal for fresh longs today.
- Crypto beta should confirm equity risk-on through BTC and ETH upside.

---

## Planner Thesis Usage (today)

| Agent | Total new plans | With parent_thesis_id | Coverage |
|---|---|---|---|
| Agent_1_Momentum | 1 | 1 | 100% |
| Agent_2_MeanReversion | 1 | 1 | 100% |
| Agent_3_Macro | 2 | 2 | 100% |
| Agent_4_Volatility | 2 | 2 | 100% |
| Agent_5_Contrarian | 2 | 2 | 100% |
| Agent_7_PairsContrarian | 3 | 3 | 100% |

**System total: 11/11 plans linked to a thesis (100% if total else 0).**

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
| 2026-06-25 | $73,538 |
| 2026-06-24 | $73,538 |
| 2026-06-23 | $73,538 |
| 2026-06-22 | $73,538 |
| 2026-06-21 | $73,538 |
| 2026-06-20 | $73,538 |
| 2026-06-19 | $73,538 |
| 2026-06-18 | $73,538 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 947 |
| Other ERROR | 142 |
| Python Traceback | 1 |
2 categories worth attention.

---

_End of snapshot._