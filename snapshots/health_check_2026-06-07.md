# Trader-v2 Daily Health Check — 2026-06-07

_Generated at 2026-06-07 11:30:05 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`1413` last_exit=`(never`
  - uptime/rss: `12:26:40 134656`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`1408` last_exit=`(never`
  - uptime/rss: `12:26:40   7872`

---

## News-agent Freshness

- **latest folder**: `2026-06-05_09-30-09` (age: 49.9h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **49.9h old** — news_agent may have stopped producing.

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

- **package_id**: `71`
- **generated_at**: `2026-06-07 09:45:52` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#72** (conf=0.24, horizon=1d, 4 symbols incl 1 primary)
  - Claim: Information scarcity favors avoiding fresh risk and treating broad-beta downside hedges as the only low-conviction actionable theme.
  - Falsification: A fresh structured handoff returns with confirmed risk-on breadth across index, mega-cap tech, and semiconductors plus no active macro stress warnings.

### Alternative hypotheses (rejected counter-theses)
- Re-enter long gold on deficit and fiscal-discipline concerns.
- Buy semiconductors as the dominant risk-on leadership group.

---

## Planner Thesis Usage (today)

| Agent | Total new plans | With parent_thesis_id | Coverage |
|---|---|---|---|
| Agent_4_Volatility | 2 | 2 | 100% |

**System total: 2/2 plans linked to a thesis (100% if total else 0).**

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
| 2026-06-07 | $73,538 |
| 2026-06-06 | $73,538 |
| 2026-06-05 | $73,538 |
| 2026-06-04 | $73,538 |
| 2026-06-03 | $73,538 |
| 2026-06-02 | $73,885 |
| 2026-06-01 | $73,495 |
| 2026-05-31 | $73,203 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 830 |
| Other ERROR | 257 |
| Python Traceback | 81 |
2 categories worth attention.

---

_End of snapshot._