# Trader-v2 Daily Health Check — 2026-07-03

_Generated at 2026-07-03 11:30:02 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`1167` last_exit=`(never`
  - uptime/rss: `02-23:21:06  10864`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`1163` last_exit=`(never`
  - uptime/rss: `02-23:21:06   6208`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 505.9h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **505.9h old** — news_agent may have stopped producing.

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

- **package_id**: `175`
- **generated_at**: `2026-07-03 09:45:34` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#176** (conf=0.32, horizon=1d, 4 symbols incl 1 primary)
  - Claim: Skipped macro pipeline and no handoff make fresh risk-on chasing unjustified today.
  - Falsification: A fresh structured handoff or next full cash-session report shows broad risk-on confirmation across index breadth, semis, and mega-cap tech with no macro risk deterioration.

### Alternative hypotheses (rejected counter-theses)
- Holiday-thin liquidity could still melt up in mega-cap tech.
- Gold should be the primary defensive expression today.

---

## Planner Thesis Usage (today)

| Agent | Total new plans | With parent_thesis_id | Coverage |
|---|---|---|---|
| Agent_4_Volatility | 1 | 1 | 100% |

**System total: 1/1 plans linked to a thesis (100% if total else 0).**

---

## Manager Close Reasons (last 7 days)

| close_reason_type | Count | Total PnL |
|---|---|---|
| price_invalidation | 1 | $-76.0 |

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
| 2026-07-03 | $73,462 |
| 2026-07-02 | $73,462 |
| 2026-07-01 | $73,462 |
| 2026-06-30 | $73,462 |
| 2026-06-29 | $73,532 |
| 2026-06-28 | $73,566 |
| 2026-06-27 | $73,563 |
| 2026-06-26 | $73,538 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 1018 |
| Other ERROR | 64 |
| Python Traceback | 3 |
2 categories worth attention.

---

_End of snapshot._