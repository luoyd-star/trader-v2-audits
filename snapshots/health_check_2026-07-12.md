# Trader-v2 Daily Health Check — 2026-07-12

_Generated at 2026-07-12 11:30:00 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`851` last_exit=`(never`
  - uptime/rss: `13:23:09 138736`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`844` last_exit=`(never`
  - uptime/rss: `13:23:09   7888`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 721.9h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **721.9h old** — news_agent may have stopped producing.

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

- **package_id**: `221`
- **generated_at**: `2026-07-12 09:45:35` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#222** (conf=0.30, horizon=1d, 4 symbols incl 1 primary)
  - Claim: Fresh US-risk exposure has poor information-adjusted asymmetry until the next validated daily pipeline restores market confirmation.
  - Falsification: A fresh structured handoff identifies a coherent catalyst and the next session confirms it through aligned SPY, QQQ, and broad semiconductor participation rather than isolated leadership.

### Alternative hypotheses (rejected counter-theses)
- Weekend crypto strength is the start of a durable risk-on breakout led by BTC and ETH.
- Semiconductors have repaired into broad leadership and should be bought aggressively.

---

## Planner Thesis Usage (today)

**No plans created today yet.** Either Planner hasn't run, or it produced 0 plans (correct behavior if no fitting thesis).

---

## Manager Close Reasons (last 7 days)

| close_reason_type | Count | Total PnL |
|---|---|---|
| thesis_falsified | 1 | $-59.0 |
| price_invalidation | 1 | $-283.0 |

✓ thesis_falsified fired 1x — the new path is in use.
Today's closes: 0 total — none

---

## Reviewer 2x2 (last 7 days)

| outcome_type | adherence | thesis_consistency | Count |
|---|---|---|---|
| FAILURE | FAIL | WARN | 1 |
| FAILURE | WARN | WARN | 1 |

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
| 2026-07-12 | $73,120 |
| 2026-07-11 | $73,120 |
| 2026-07-10 | $73,120 |
| 2026-07-09 | $73,120 |
| 2026-07-08 | $73,205 |
| 2026-07-07 | $73,334 |
| 2026-07-06 | $73,179 |
| 2026-07-05 | $73,462 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 1026 |
| Other ERROR | 55 |
| Python Traceback | 3 |
2 categories worth attention.

---

_End of snapshot._