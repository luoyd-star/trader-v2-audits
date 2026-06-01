# Trader-v2 Daily Health Check — 2026-06-01

_Generated at 2026-06-01 11:30:02 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`1857` last_exit=`(never`
  - uptime/rss: `18:44:03 165328`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`1853` last_exit=`(never`
  - uptime/rss: `18:44:03   9760`

---

## News-agent Freshness

- **latest folder**: `2026-06-01_09-30-08` (age: 1.9h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓

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

- **package_id**: `41`
- **generated_at**: `2026-06-01 09:45:45` (age: 1.7h, today's: **YES**)
- **active_theses count**: 3 (expected 1-3)
- **alternative_hypotheses count**: 3 (expected ≥1)

### Active theses (the spine of today's trading)
- **#42** (conf=0.64, horizon=5d, 3 symbols incl 1 primary)
  - Claim: Crypto remains the cleanest weak link because equity risk-on is not transmitting into BTC or ETH trend repair.
  - Falsification: BTCUSDT and ETHUSDT both regain short, medium, and long trend references while crypto beta confirms equity risk-on for two consecutive sessions.
- **#43** (conf=0.56, horizon=5d, 3 symbols incl 1 primary)
  - Claim: Broad equity risk-on is compressed rather than healthy, so QQQ strength has asymmetric downside risk into NFP.
  - Falsification: SPY and QQQ VIX correlations normalize back toward negative risk-on behavior while liquidity stops tightening before NFP.
- **#44** (conf=0.58, horizon=7d, 4 symbols incl 1 primary)
  - Claim: AI phase-2 rotation still works, but extension makes fresh second-line longs poor risk before confirmation.
  - Falsification: AI second-line breadth expands for two sessions while extended members cool from overbought readings without losing relative strength.

### Alternative hypotheses (rejected counter-theses)
- MSFT is becoming a new defensive mega-cap leadership leg.
- HOOD, PLTR, ORCL and LLY mark a confirmed behavioral rotation worth following long.
- Low VIX means broad risk-on is healthy and should be bought aggressively.

---

## Planner Thesis Usage (today)

| Agent | Total new plans | With parent_thesis_id | Coverage |
|---|---|---|---|
| Agent_1_Momentum | 6 | 6 | 100% |
| Agent_2_MeanReversion | 4 | 4 | 100% |
| Agent_3_Macro | 8 | 8 | 100% |
| Agent_4_Volatility | 5 | 5 | 100% |
| Agent_5_Contrarian | 4 | 4 | 100% |
| Agent_7_PairsContrarian | 3 | 3 | 100% |

**System total: 30/30 plans linked to a thesis (100% if total else 0).**

---

## Manager Close Reasons (last 7 days)

| close_reason_type | Count | Total PnL |
|---|---|---|
| time_stop | 3 | $1199.0 |
| price_invalidation | 1 | $-133.0 |
| other | 1 | $2185.0 |

⚠ **0 closes via thesis_falsified path.** Either no parent_thesis was actually broken in this window (fine), or the LLM never uses this path (concerning if persistent over multiple weeks).
Today's closes: 0 total — none

---

## Reviewer 2x2 (last 7 days)

| outcome_type | adherence | thesis_consistency | Count |
|---|---|---|---|
| FAILURE | PASS | WARN | 1 |
| MIXED | PASS | PASS | 1 |
| MIXED | PASS | WARN | 1 |
| MIXED | WARN | WARN | 1 |
| SUCCESS | PASS | PASS | 1 |
| SUCCESS | WARN | PASS | 1 |

**Note**: Phase 4's `thesis_validity` / `execution_quality` / `lesson_target` fields
are emitted by the Reviewer LLM but NOT yet persisted as columns in `review_records`.
Until that's wired (TODO), we surface only the legacy adherence/thesis_consistency.

Sanity check: if `outcome_type` is 100% 'SUCCESS', that's the LLM self-flattery red flag.

---

## Open Positions

| Agent | Symbol | Dir | Entry | Margin | Held/Max | % used | parent_thesis_id |
|---|---|---|---|---|---|---|---|
| A1_Momentum | NVDAUSDT | LONG | 221.5 | $2487 | 278.8h / 240h | 116% | (legacy) |

Total open: 1. Pre-Phase-2 legacy (no parent_thesis_id): 1.
⚠ 1 positions ≥80% of max_hold — approaching time stop.

---

## Equity (7-day trend, EOD per day)

| Day | Total equity (EOD) |
|---|---|
| 2026-06-01 | $73,176 |
| 2026-05-31 | $73,203 |
| 2026-05-30 | $73,182 |
| 2026-05-29 | $73,179 |
| 2026-05-28 | $73,047 |
| 2026-05-27 | $72,778 |
| 2026-05-26 | $73,032 |
| 2026-05-25 | $73,369 |
**Today vs yesterday: $-27**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 821 |
| Other ERROR | 345 |
| Python Traceback | 187 |
2 categories worth attention.

---

_End of snapshot._