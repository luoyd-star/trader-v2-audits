# Trader-v2 Daily Health Check — 2026-05-29

_Generated at 2026-05-29 11:30:05 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`10251` last_exit=`never`
  - uptime/rss: `09:24:38  25184`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`1292` last_exit=`(never`
  - uptime/rss: `06-12:15:54   5824`

---

## News-agent Freshness

- **latest folder**: `2026-05-29_09-30-07` (age: 1.9h)
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

- **package_id**: `29`
- **generated_at**: `2026-05-29 09:45:31` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#30** (conf=0.56, horizon=5d, 6 symbols incl 1 primary)
  - Claim: AI-led index strength is fragile because extension is high and breadth confirmation is explicitly suspect.
  - Falsification: AI leadership broadens beyond NVDA/second-line semis while liquidity-risk warnings fade and multiple growth symbols show confirmed breadth participation in the same session.

### Alternative hypotheses (rejected counter-theses)
- The NVDA-led AI rally can continue and pull QQQ higher despite narrow breadth.
- Gold and silver should be bought as dollar-debasement hedges.

---

## Planner Thesis Usage (today)

| Agent | Total new plans | With parent_thesis_id | Coverage |
|---|---|---|---|
| Agent_1_Momentum | 1 | 1 | 100% |
| Agent_2_MeanReversion | 1 | 1 | 100% |
| Agent_3_Macro | 2 | 2 | 100% |
| Agent_4_Volatility | 2 | 2 | 100% |
| Agent_7_PairsContrarian | 4 | 4 | 100% |

**System total: 10/10 plans linked to a thesis (100% if total else 0).**

---

## Manager Close Reasons (last 7 days)

| close_reason_type | Count | Total PnL |
|---|---|---|
| time_stop | 5 | $1077.0 |
| price_invalidation | 1 | $-133.0 |
| other | 1 | $2185.0 |
| (null) | 1 | $-64.0 |

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
| invalidation_not_respected | partial | unknown | 1 |
| scratch_loss | PASS_WITH_NOTES | unknown | 1 |

**Note**: Phase 4's `thesis_validity` / `execution_quality` / `lesson_target` fields
are emitted by the Reviewer LLM but NOT yet persisted as columns in `review_records`.
Until that's wired (TODO), we surface only the legacy adherence/thesis_consistency.

Sanity check: if `outcome_type` is 100% 'SUCCESS', that's the LLM self-flattery red flag.

---

## Open Positions

| Agent | Symbol | Dir | Entry | Margin | Held/Max | % used | parent_thesis_id |
|---|---|---|---|---|---|---|---|
| A1_Momentum | NVDAUSDT | LONG | 221.5 | $2487 | 206.8h / 240h | 86% | (legacy) |

Total open: 1. Pre-Phase-2 legacy (no parent_thesis_id): 1.
⚠ 1 positions ≥80% of max_hold — approaching time stop.

---

## Equity (7-day trend, EOD per day)

| Day | Total equity (EOD) |
|---|---|
| 2026-05-29 | $73,129 |
| 2026-05-28 | $73,047 |
| 2026-05-27 | $72,778 |
| 2026-05-26 | $73,032 |
| 2026-05-25 | $73,369 |
| 2026-05-24 | $73,017 |
| 2026-05-23 | $72,248 |
| 2026-05-22 | $72,498 |
**Today vs yesterday: +$82**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 838 |
| Other ERROR | 394 |
| Python Traceback | 236 |
2 categories worth attention.

---

_End of snapshot._