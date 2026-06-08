# Trader-v2 Daily Health Check — 2026-06-08

_Generated at 2026-06-08 11:30:05 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`1413` last_exit=`(never`
  - uptime/rss: `01-12:26:40  28384`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`1408` last_exit=`(never`
  - uptime/rss: `01-12:26:40   5024`

---

## News-agent Freshness

- **latest folder**: `2026-06-08_09-30-09` (age: 1.9h)
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

- **package_id**: `75`
- **generated_at**: `2026-06-08 09:45:29` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 3 (expected ≥1)

### Active theses (the spine of today's trading)
- **#76** (conf=0.46, horizon=3d, 5 symbols incl 1 primary)
  - Claim: Cross-asset stress favors a conservative short-risk bias over buying the dip today.
  - Falsification: QQQ/SPY, crypto beta, and semiconductor cohort all shift from stress to synchronized risk-on behavior for one full session.

### Alternative hypotheses (rejected counter-theses)
- AI semiconductors are only pausing before another leadership leg higher.
- Gold or silver should be the primary hedge against renewed macro stress.
- Energy or copper demand signals should drive today's primary thesis.

---

## Planner Thesis Usage (today)

| Agent | Total new plans | With parent_thesis_id | Coverage |
|---|---|---|---|
| Agent_2_MeanReversion | 2 | 2 | 100% |
| Agent_3_Macro | 3 | 3 | 100% |
| Agent_4_Volatility | 1 | 1 | 100% |
| Agent_5_Contrarian | 1 | 1 | 100% |
| Agent_7_PairsContrarian | 1 | 1 | 100% |

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
| 2026-06-08 | $73,538 |
| 2026-06-07 | $73,538 |
| 2026-06-06 | $73,538 |
| 2026-06-05 | $73,538 |
| 2026-06-04 | $73,538 |
| 2026-06-03 | $73,538 |
| 2026-06-02 | $73,885 |
| 2026-06-01 | $73,495 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 833 |
| Other ERROR | 257 |
| Python Traceback | 81 |
2 categories worth attention.

---

_End of snapshot._