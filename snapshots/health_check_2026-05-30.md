# Trader-v2 Daily Health Check — 2026-05-30

_Generated at 2026-05-30 11:30:04 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`10251` last_exit=`never`
  - uptime/rss: `01-09:24:37  10496`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`1292` last_exit=`(never`
  - uptime/rss: `07-12:15:53   5824`

---

## News-agent Freshness

- **latest folder**: `2026-05-29_09-30-07` (age: 25.9h)
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

- **package_id**: `33`
- **generated_at**: `2026-05-30 09:45:31` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#34** (conf=0.42, horizon=2d, 5 symbols incl 1 primary)
  - Claim: With no fresh handoff today, the only defensible live thesis is risk-managed continuation of the existing NVDA long.
  - Falsification: A fresh structured handoff resumes and contradicts AI/growth leadership, or NVDA's cohort support from QQQ/AMD/AVGO fails broadly in the same session.

### Alternative hypotheses (rejected counter-theses)
- Treat the skipped-pipeline day as a clean risk-off signal and short high beta.
- Add fresh AI or QQQ longs because the current NVDA position is profitable momentum.

---

## Planner Thesis Usage (today)

**No plans created today yet.** Either Planner hasn't run, or it produced 0 plans (correct behavior if no fitting thesis).

---

## Manager Close Reasons (last 7 days)

| close_reason_type | Count | Total PnL |
|---|---|---|
| time_stop | 5 | $1077.0 |
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
| scratch_loss | PASS_WITH_NOTES | unknown | 1 |

**Note**: Phase 4's `thesis_validity` / `execution_quality` / `lesson_target` fields
are emitted by the Reviewer LLM but NOT yet persisted as columns in `review_records`.
Until that's wired (TODO), we surface only the legacy adherence/thesis_consistency.

Sanity check: if `outcome_type` is 100% 'SUCCESS', that's the LLM self-flattery red flag.

---

## Open Positions

| Agent | Symbol | Dir | Entry | Margin | Held/Max | % used | parent_thesis_id |
|---|---|---|---|---|---|---|---|
| A1_Momentum | NVDAUSDT | LONG | 221.5 | $2487 | 230.8h / 240h | 96% | (legacy) |

Total open: 1. Pre-Phase-2 legacy (no parent_thesis_id): 1.
⚠ 1 positions ≥80% of max_hold — approaching time stop.

---

## Equity (7-day trend, EOD per day)

| Day | Total equity (EOD) |
|---|---|
| 2026-05-30 | $73,070 |
| 2026-05-29 | $73,179 |
| 2026-05-28 | $73,047 |
| 2026-05-27 | $72,778 |
| 2026-05-26 | $73,032 |
| 2026-05-25 | $73,369 |
| 2026-05-24 | $73,017 |
| 2026-05-23 | $72,248 |
**Today vs yesterday: $-109**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 824 |
| Other ERROR | 379 |
| Python Traceback | 221 |
2 categories worth attention.

---

_End of snapshot._