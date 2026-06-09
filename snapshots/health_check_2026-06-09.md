# Trader-v2 Daily Health Check — 2026-06-09

_Generated at 2026-06-09 11:30:04 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`1413` last_exit=`(never`
  - uptime/rss: `02-12:26:39  23024`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`1408` last_exit=`(never`
  - uptime/rss: `02-12:26:39   5008`

---

## News-agent Freshness

- **latest folder**: `2026-06-09_09-30-07` (age: 1.9h)
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

- **package_id**: `80`
- **generated_at**: `2026-06-09 09:45:34` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#81** (conf=0.58, horizon=3d, 4 symbols incl 1 primary)
  - Claim: Crypto strength is a relief bounce, not trend repair, while BTC, ETH, and DOGE remain below ema20/ema60/ema200.
  - Falsification: BTCUSDT, ETHUSDT, and DOGEUSDT all reclaim ema20/ema60/ema200 and hold above them for the same full session.

### Alternative hypotheses (rejected counter-theses)
- The VIX dip below 20 means risk-on conditions are confirmed across equities.
- Behavioral flow and rotation hypotheses are confirmed fund flows that justify directional trades.

---

## Planner Thesis Usage (today)

| Agent | Total new plans | With parent_thesis_id | Coverage |
|---|---|---|---|
| Agent_1_Momentum | 3 | 3 | 100% |
| Agent_3_Macro | 3 | 3 | 100% |
| Agent_4_Volatility | 3 | 3 | 100% |
| Agent_5_Contrarian | 3 | 3 | 100% |
| Agent_7_PairsContrarian | 1 | 1 | 100% |

**System total: 13/13 plans linked to a thesis (100% if total else 0).**

---

## Manager Close Reasons (last 7 days)

| close_reason_type | Count | Total PnL |
|---|---|---|
| time_stop | 1 | $0.0 |

⚠ **0 closes via thesis_falsified path.** Either no parent_thesis was actually broken in this window (fine), or the LLM never uses this path (concerning if persistent over multiple weeks).
Today's closes: 0 total — none

---

## Reviewer 2x2 (last 7 days)

| outcome_type | adherence | thesis_consistency | Count |
|---|---|---|---|
| FAILURE | FAIL | WARN | 1 |

**Note**: Phase 4's `thesis_validity` / `execution_quality` / `lesson_target` fields
are emitted by the Reviewer LLM but NOT yet persisted as columns in `review_records`.
Until that's wired (TODO), we surface only the legacy adherence/thesis_consistency.

Sanity check: if `outcome_type` is 100% 'SUCCESS', that's the LLM self-flattery red flag.

---

## Open Positions

(no open trades)

---

## Equity (7-day trend, EOD per day)

| Day | Total equity (EOD) |
|---|---|
| 2026-06-09 | $73,538 |
| 2026-06-08 | $73,538 |
| 2026-06-07 | $73,538 |
| 2026-06-06 | $73,538 |
| 2026-06-05 | $73,538 |
| 2026-06-04 | $73,538 |
| 2026-06-03 | $73,538 |
| 2026-06-02 | $73,885 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 794 |
| Other ERROR | 257 |
| Python Traceback | 81 |
2 categories worth attention.

---

_End of snapshot._