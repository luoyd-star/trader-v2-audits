# Trader-v2 Daily Health Check — 2026-06-04

_Generated at 2026-06-04 11:30:04 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`2808` last_exit=`(never`
  - uptime/rss: `10:55:44  12992`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`2806` last_exit=`(never`
  - uptime/rss: `10:55:44   8000`

---

## News-agent Freshness

- **latest folder**: `2026-06-04_09-30-10` (age: 1.9h)
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

- **package_id**: `57`
- **generated_at**: `2026-06-04 09:45:31` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#58** (conf=0.46, horizon=3d, 5 symbols incl 1 primary)
  - Claim: Extended AI leadership is vulnerable to mean reversion if follow-through fails today.
  - Falsification: AI leadership broadens with NVDA, AMD, AVGO, TSM and QQQ all showing sustained positive follow-through while breadth improves in the same session.

### Alternative hypotheses (rejected counter-theses)
- Low VIX signals clean broad risk-on continuation.
- Compressed real yields imply liquidity easing and support risk assets.

---

## Planner Thesis Usage (today)

| Agent | Total new plans | With parent_thesis_id | Coverage |
|---|---|---|---|
| Agent_1_Momentum | 1 | 1 | 100% |
| Agent_7_PairsContrarian | 1 | 1 | 100% |

**System total: 2/2 plans linked to a thesis (100% if total else 0).**

---

## Manager Close Reasons (last 7 days)

| close_reason_type | Count | Total PnL |
|---|---|---|
| time_stop | 2 | $428.0 |
| price_invalidation | 1 | $-133.0 |

⚠ **0 closes via thesis_falsified path.** Either no parent_thesis was actually broken in this window (fine), or the LLM never uses this path (concerning if persistent over multiple weeks).
Today's closes: 0 total — none

---

## Reviewer 2x2 (last 7 days)

| outcome_type | adherence | thesis_consistency | Count |
|---|---|---|---|
| FAILURE | FAIL | WARN | 1 |
| FAILURE | PASS | WARN | 1 |
| MIXED | PASS | PASS | 1 |
| MIXED | WARN | WARN | 1 |

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
| 2026-06-04 | $73,538 |
| 2026-06-03 | $73,538 |
| 2026-06-02 | $73,885 |
| 2026-06-01 | $73,495 |
| 2026-05-31 | $73,203 |
| 2026-05-30 | $73,182 |
| 2026-05-29 | $73,179 |
| 2026-05-28 | $73,047 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 812 |
| Other ERROR | 292 |
| Python Traceback | 134 |
2 categories worth attention.

---

_End of snapshot._