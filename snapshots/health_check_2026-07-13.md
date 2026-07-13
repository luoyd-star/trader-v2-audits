# Trader-v2 Daily Health Check — 2026-07-13

_Generated at 2026-07-13 11:30:03 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`851` last_exit=`(never`
  - uptime/rss: `01-13:23:12  21728`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`844` last_exit=`(never`
  - uptime/rss: `01-13:23:12   7680`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 745.9h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **745.9h old** — news_agent may have stopped producing.

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

- **package_id**: `225`
- **generated_at**: `2026-07-13 09:45:38` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#226** (conf=0.42, horizon=3d, 3 symbols incl 1 primary)
  - Claim: Fragile, concentrated equity risk should favor a cautious QQQ downside bias over new broad technology longs.
  - Falsification: Fragility exits Watch, equity-bond hedging normalizes, and factor concentration declines while broad equity participation improves for two consecutive sessions.

### Alternative hypotheses (rejected counter-theses)
- Low volatility could signal a durable broad risk-on expansion rather than a fragile concentrated advance.
- Semiconductor leadership could support a renewed broad mega-cap technology long.

---

## Planner Thesis Usage (today)

| Agent | Total new plans | With parent_thesis_id | Coverage |
|---|---|---|---|
| Agent_1_Momentum | 1 | 1 | 100% |
| Agent_3_Macro | 1 | 1 | 100% |

**System total: 2/2 plans linked to a thesis (100% if total else 0).**

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
| 2026-07-13 | $73,120 |
| 2026-07-12 | $73,120 |
| 2026-07-11 | $73,120 |
| 2026-07-10 | $73,120 |
| 2026-07-09 | $73,120 |
| 2026-07-08 | $73,205 |
| 2026-07-07 | $73,334 |
| 2026-07-06 | $73,179 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 990 |
| Other ERROR | 55 |
| Python Traceback | 3 |
2 categories worth attention.

---

_End of snapshot._