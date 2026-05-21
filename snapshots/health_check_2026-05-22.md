# Trader-v2 Daily Health Check — 2026-05-22

_Generated at 2026-05-22 04:20:32 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`69049` last_exit=`never`
  - uptime/rss: `05:58  80512`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`1899` last_exit=`(never`
  - uptime/rss: `02-06:54:55  10496`

---

## News-agent Freshness

- **latest folder**: `2026-05-21_20-57-01` (age: 7.3h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓

---

## Morning Batch (recent log markers)

Status of morning-batch markers in last ~5MB of log:
- `DAILY STRATEGIST START`: ✗
- `DAILY STRATEGIST END`: ✗
- `DAILY PLANNER START`: ✓
- `DAILY PLANNER END`: ✓
- `DAILY MACRO MANAGER START`: ✓
- `DAILY MACRO MANAGER END`: ✓
- `DAILY REVIEWER START`: ✓
- `DAILY REVIEWER END`: ✓

**Note**: presence in log means it ran *recently*, not necessarily today. Cross-reference with DB sections below for today-specific evidence (Strategist generated_at, plans created_at, etc.).

---

## Strategist Output (today)

**No theses in DB.** Strategist may not have run yet, or persistence failed. P0 issue.

---

## Planner Thesis Usage (today)

**No plans created today yet.** Either Planner hasn't run, or it produced 0 plans (correct behavior if no fitting thesis).

---

## Manager Close Reasons (last 7 days)

| close_reason_type | Count | Total PnL |
|---|---|---|
| (null) | 6 | $929.0 |

⚠ **0 closes via thesis_falsified path.** Either no parent_thesis was actually broken in this window (fine), or the LLM never uses this path (concerning if persistent over multiple weeks).
Today's closes: 1 total — (null):1

---

## Reviewer 2x2 (last 7 days)

| outcome_type | adherence | thesis_consistency | Count |
|---|---|---|---|
| INVALIDATION_EXIT | PASS | CONSISTENT | 1 |
| LOSS | OPENING_PLAN_OBEYED, HOLDING_PLAN_VIOLATED, CLOSING_PLAN_VIOLATED | PARTIAL | 1 |
| NEGATIVE | VIOLATION | VIOLATION | 1 |
| WIN_TIME_STOP_EXIT | PARTIAL | ALIGNED | 1 |
| invalidation_not_respected | partial | unknown | 1 |
| profitable_but_premature | entry_and_hold_ok_exit_violation | intact | 1 |

**Note**: Phase 4's `thesis_validity` / `execution_quality` / `lesson_target` fields
are emitted by the Reviewer LLM but NOT yet persisted as columns in `review_records`.
Until that's wired (TODO), we surface only the legacy adherence/thesis_consistency.

Sanity check: if `outcome_type` is 100% 'SUCCESS', that's the LLM self-flattery red flag.

---

## Open Positions

| Agent | Symbol | Dir | Entry | Margin | Held/Max | % used | parent_thesis_id |
|---|---|---|---|---|---|---|---|
| A5_Contrarian | BABAUSDT | LONG | 132.33 | $1800 | 126.7h / 120h | 106% | (legacy) |
| A5_Contrarian | GEUSDT | LONG | 280.43 | $2000 | 80.5h / 120h | 67% | (legacy) |
| A5_Contrarian | ETHUSDT | LONG | 2129.11 | $2000 | 56.7h / 120h | 47% | (legacy) |
| A7_PairsContrarian | TSMUSDT | LONG | 397.5 | $1409 | 21.1h / 120h | 18% | (legacy) |
| A1_Momentum | NVDAUSDT | LONG | 221.5 | $2487 | 31.6h / 240h | 13% | (legacy) |
| A1_Momentum | ARMUSDT | LONG | 265.63 | $2500 | 1.4h / 240h | 1% | (legacy) |
| A5_Contrarian | METAUSDT | LONG | 596.53 | $2200 | -3.8h / 120h | -3% | (legacy) |

Total open: 7. Pre-Phase-2 legacy (no parent_thesis_id): 7.
⚠ 1 positions ≥80% of max_hold — approaching time stop.

---

## Equity (7-day trend, EOD per day)

| Day | Total equity (EOD) |
|---|---|
| 2026-05-22 | $72,092 |
| 2026-05-21 | $71,789 |
| 2026-05-20 | $70,852 |
| 2026-05-19 | $70,706 |
| 2026-05-18 | $70,839 |
| 2026-05-17 | $70,976 |
| 2026-05-16 | $70,750 |
| 2026-05-15 | $70,996 |
**Today vs yesterday: +$303**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 982 |
| Python Traceback | 384 |
| Other ERROR | 384 |
2 categories worth attention.

---

_End of snapshot._