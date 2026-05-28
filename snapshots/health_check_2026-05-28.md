# Trader-v2 Daily Health Check — 2026-05-28

_Generated at 2026-05-28 11:30:05 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`39320` last_exit=`never`
  - uptime/rss: `01-13:58:56  11008`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`1292` last_exit=`(never`
  - uptime/rss: `05-12:15:54   6432`

---

## News-agent Freshness

- **latest folder**: `2026-05-28_09-30-12` (age: 2.0h)
- **STATE_UPDATE.md**: ✗ MISSING
- **Trader_Handoff.json**: ✗ MISSING
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

- **package_id**: `25`
- **generated_at**: `2026-05-28 09:47:26` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#26** (conf=0.42, horizon=5d, 4 symbols incl 1 primary)
  - Claim: AI-led large-cap momentum remains the only actionable long thesis, but it must be expressed selectively rather than as broad beta.
  - Falsification: NVDA and META both lose leadership while QQQ/SPY breadth fails to expand for two consecutive sessions.

### Alternative hypotheses (rejected counter-theses)
- Gold should remain the primary defensive long.
- Semiconductor exhaustion is ready for outright shorts.

---

## Planner Thesis Usage (today)

| Agent | Total new plans | With parent_thesis_id | Coverage |
|---|---|---|---|
| Agent_1_Momentum | 1 | 1 | 100% |
| Agent_3_Macro | 1 | 1 | 100% |
| Agent_4_Volatility | 1 | 1 | 100% |
| Agent_7_PairsContrarian | 1 | 1 | 100% |

**System total: 4/4 plans linked to a thesis (100% if total else 0).**

---

## Manager Close Reasons (last 7 days)

| close_reason_type | Count | Total PnL |
|---|---|---|
| time_stop | 4 | $649.0 |
| other | 1 | $2185.0 |
| (null) | 1 | $-64.0 |

⚠ **0 closes via thesis_falsified path.** Either no parent_thesis was actually broken in this window (fine), or the LLM never uses this path (concerning if persistent over multiple weeks).
Today's closes: 0 total — none

---

## Reviewer 2x2 (last 7 days)

| outcome_type | adherence | thesis_consistency | Count |
|---|---|---|---|
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
| A5_Contrarian | METAUSDT | LONG | 596.53 | $2200 | 147.4h / 120h | 123% | (legacy) |
| A5_Contrarian | XAUUSDT | LONG | 4515.49 | $1800 | 99.1h / 120h | 83% | 7 |
| A1_Momentum | NVDAUSDT | LONG | 221.5 | $2487 | 182.8h / 240h | 76% | (legacy) |

Total open: 3. Pre-Phase-2 legacy (no parent_thesis_id): 2.
⚠ 2 positions ≥80% of max_hold — approaching time stop.

---

## Equity (7-day trend, EOD per day)

| Day | Total equity (EOD) |
|---|---|
| 2026-05-28 | $73,033 |
| 2026-05-27 | $72,778 |
| 2026-05-26 | $73,032 |
| 2026-05-25 | $73,369 |
| 2026-05-24 | $73,017 |
| 2026-05-23 | $72,248 |
| 2026-05-22 | $72,498 |
| 2026-05-21 | $71,789 |
**Today vs yesterday: +$255**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 854 |
| Other ERROR | 411 |
| Python Traceback | 253 |
2 categories worth attention.

---

_End of snapshot._