# Trader-v2 Daily Health Check — 2026-06-10

_Generated at 2026-06-10 11:30:06 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`1413` last_exit=`(never`
  - uptime/rss: `03-12:26:41   5968`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`1408` last_exit=`(never`
  - uptime/rss: `03-12:26:41   4944`

---

## News-agent Freshness

- **latest folder**: `2026-06-10_09-30-07` (age: 1.9h)
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

- **package_id**: `84`
- **generated_at**: `2026-06-10 09:45:37` (age: 1.7h, today's: **YES**)
- **active_theses count**: 2 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#85** (conf=0.62, horizon=5d, 3 symbols incl 1 primary)
  - Claim: Crypto remains structurally unrepaired, so rallies in BTC/ETH/DOGE should be treated as suspect until broad trend repair occurs.
  - Falsification: BTC, ETH, and DOGE all reclaim ema20, ema60, and ema200 in the same session and hold above them while behavioral flow signals stop conflicting with trend evidence.
- **#86** (conf=0.55, horizon=4d, 3 symbols incl 1 primary)
  - Claim: Equity risk-on is incomplete while vol and credit fail to confirm, so broad beta longs need restraint.
  - Falsification: VIX falls below 18, HYG reclaims ema200, and QQQ/SPY breadth improves together for a full session without leadership narrowing further.

### Alternative hypotheses (rejected counter-theses)
- A soft-risk-on rebound is starting as volatility cools.
- Crypto is bottoming and should be bought ahead of trend confirmation.

---

## Planner Thesis Usage (today)

| Agent | Total new plans | With parent_thesis_id | Coverage |
|---|---|---|---|
| Agent_2_MeanReversion | 3 | 3 | 100% |
| Agent_5_Contrarian | 1 | 1 | 100% |
| Agent_7_PairsContrarian | 4 | 4 | 100% |

**System total: 8/8 plans linked to a thesis (100% if total else 0).**

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
| 2026-06-10 | $73,538 |
| 2026-06-09 | $73,538 |
| 2026-06-08 | $73,538 |
| 2026-06-07 | $73,538 |
| 2026-06-06 | $73,538 |
| 2026-06-05 | $73,538 |
| 2026-06-04 | $73,538 |
| 2026-06-03 | $73,538 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 806 |
| Other ERROR | 257 |
| Python Traceback | 81 |
2 categories worth attention.

---

_End of snapshot._