# Trader-v2 Daily Health Check — 2026-05-26

_Generated at 2026-05-26 11:30:04 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`39976` last_exit=`never`
  - uptime/rss: `19:03:07  27376`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`1292` last_exit=`(never`
  - uptime/rss: `03-12:15:53   8000`

---

## News-agent Freshness

- **latest folder**: `2026-05-26_09-30-07` (age: 1.9h)
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

- **package_id**: `15`
- **generated_at**: `2026-05-26 09:45:41` (age: 1.7h, today's: **YES**)
- **active_theses count**: 2 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#16** (conf=0.66, horizon=7d, 4 symbols incl 1 primary)
  - Claim: Fiscal-dominance metals-duration convergence can persist through the catalyst-distant window.
  - Falsification: GC=F correlations with TLT, SHY, LQD, and HYG all drop below elevated convergence status while GC=F-VIX correlation turns positive for two sessions.
- **#17** (conf=0.58, horizon=5d, 5 symbols incl 1 primary)
  - Claim: AI leadership remains intact but narrow, favoring quality semiconductor exposure over broad beta.
  - Falsification: AI leaders lose relative strength together while QQQ breadth fails to broaden and semiconductor cohort leadership stops confirming for two consecutive sessions.

### Alternative hypotheses (rejected counter-theses)
- Broad risk-on melt-up lifts equities, crypto, and commodities together.
- Gold safe-haven identity is re-emerging after the weekend gap.

---

## Planner Thesis Usage (today)

| Agent | Total new plans | With parent_thesis_id | Coverage |
|---|---|---|---|
| Agent_3_Macro | 2 | 2 | 100% |

**System total: 2/2 plans linked to a thesis (100% if total else 0).**

---

## Manager Close Reasons (last 7 days)

| close_reason_type | Count | Total PnL |
|---|---|---|
| (null) | 4 | $625.0 |
| time_stop | 3 | $389.0 |

⚠ **0 closes via thesis_falsified path.** Either no parent_thesis was actually broken in this window (fine), or the LLM never uses this path (concerning if persistent over multiple weeks).
Today's closes: 0 total — none

---

## Reviewer 2x2 (last 7 days)

| outcome_type | adherence | thesis_consistency | Count |
|---|---|---|---|
| INVALIDATION_EXIT | PASS | CONSISTENT | 1 |
| MIXED | PASS | WARN | 1 |
| NEGATIVE | VIOLATION | VIOLATION | 1 |
| SUCCESS | WARN | PASS | 1 |
| invalidation_not_respected | partial | unknown | 1 |
| profitable_but_premature | entry_and_hold_ok_exit_violation | intact | 1 |
| scratch_loss | PASS_WITH_NOTES | unknown | 1 |

**Note**: Phase 4's `thesis_validity` / `execution_quality` / `lesson_target` fields
are emitted by the Reviewer LLM but NOT yet persisted as columns in `review_records`.
Until that's wired (TODO), we surface only the legacy adherence/thesis_consistency.

Sanity check: if `outcome_type` is 100% 'SUCCESS', that's the LLM self-flattery red flag.

---

## Open Positions

| Agent | Symbol | Dir | Entry | Margin | Held/Max | % used | parent_thesis_id |
|---|---|---|---|---|---|---|---|
| A7_PairsContrarian | TSMUSDT | LONG | 397.5 | $845 | 124.3h / 120h | 104% | (legacy) |
| A5_Contrarian | METAUSDT | LONG | 596.53 | $2200 | 99.4h / 120h | 83% | (legacy) |
| A1_Momentum | NVDAUSDT | LONG | 221.5 | $2487 | 134.8h / 240h | 56% | (legacy) |
| A1_Momentum | ARMUSDT | LONG | 265.63 | $313 | 104.6h / 240h | 44% | (legacy) |
| A5_Contrarian | XAUUSDT | LONG | 4515.49 | $1800 | 51.1h / 120h | 43% | 7 |

Total open: 5. Pre-Phase-2 legacy (no parent_thesis_id): 4.
⚠ 2 positions ≥80% of max_hold — approaching time stop.

---

## Equity (7-day trend, EOD per day)

| Day | Total equity (EOD) |
|---|---|
| 2026-05-26 | $73,093 |
| 2026-05-25 | $73,369 |
| 2026-05-24 | $73,017 |
| 2026-05-23 | $72,248 |
| 2026-05-22 | $72,498 |
| 2026-05-21 | $71,789 |
| 2026-05-20 | $70,852 |
| 2026-05-19 | $70,706 |
**Today vs yesterday: $-276**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 874 |
| Other ERROR | 440 |
| Python Traceback | 287 |
2 categories worth attention.

---

_End of snapshot._