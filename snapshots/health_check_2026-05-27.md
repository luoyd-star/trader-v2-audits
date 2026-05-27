# Trader-v2 Daily Health Check — 2026-05-27

_Generated at 2026-05-27 11:30:05 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`39320` last_exit=`never`
  - uptime/rss: `13:58:57  26096`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`1292` last_exit=`(never`
  - uptime/rss: `04-12:15:55   9408`

---

## News-agent Freshness

- **latest folder**: `2026-05-27_09-30-09` (age: 2.0h)
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

- **package_id**: `20`
- **generated_at**: `2026-05-27 09:45:39` (age: 1.7h, today's: **YES**)
- **active_theses count**: 2 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#21** (conf=0.43, horizon=3d, 4 symbols incl 1 primary)
  - Claim: Narrow AI-led strength is mature, so fresh exposure should favor hedging/fading extended beta rather than chasing longs.
  - Falsification: Fresh structured handoff confirms broadening market breadth while NVDA, TSM, META, and QQQ all show synchronized positive follow-through without defensive asset demand.
- **#22** (conf=0.46, horizon=5d, 3 symbols incl 1 primary)
  - Claim: Gold longs remain acceptable as a hedge, but should not be treated as confirmation for broader risk-on exposure.
  - Falsification: Gold loses defensive sponsorship while equity breadth broadens and the documented real-yield/gold chain remains unstable for two consecutive sessions.

### Alternative hypotheses (rejected counter-theses)
- AI momentum may continue and reward holding or adding NVDA/TSM longs.
- A broad risk-on rally may be starting across equities and crypto.

---

## Planner Thesis Usage (today)

| Agent | Total new plans | With parent_thesis_id | Coverage |
|---|---|---|---|
| Agent_1_Momentum | 1 | 1 | 100% |
| Agent_2_MeanReversion | 1 | 1 | 100% |
| Agent_3_Macro | 3 | 3 | 100% |
| Agent_4_Volatility | 1 | 1 | 100% |
| Agent_5_Contrarian | 1 | 1 | 100% |
| Agent_7_PairsContrarian | 1 | 1 | 100% |

**System total: 8/8 plans linked to a thesis (100% if total else 0).**

---

## Manager Close Reasons (last 7 days)

| close_reason_type | Count | Total PnL |
|---|---|---|
| time_stop | 3 | $389.0 |
| (null) | 2 | $-122.0 |
| other | 1 | $2185.0 |

⚠ **0 closes via thesis_falsified path.** Either no parent_thesis was actually broken in this window (fine), or the LLM never uses this path (concerning if persistent over multiple weeks).
Today's closes: 1 total — other:1

---

## Reviewer 2x2 (last 7 days)

| outcome_type | adherence | thesis_consistency | Count |
|---|---|---|---|
| INVALIDATION_EXIT | PASS | CONSISTENT | 1 |
| MIXED | PASS | WARN | 1 |
| NEGATIVE | VIOLATION | VIOLATION | 1 |
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
| A7_PairsContrarian | TSMUSDT | LONG | 397.5 | $845 | 148.3h / 120h | 124% | (legacy) |
| A5_Contrarian | METAUSDT | LONG | 596.53 | $2200 | 123.4h / 120h | 103% | (legacy) |
| A1_Momentum | NVDAUSDT | LONG | 221.5 | $2487 | 158.8h / 240h | 66% | (legacy) |
| A5_Contrarian | XAUUSDT | LONG | 4515.49 | $1800 | 75.1h / 120h | 63% | 7 |

Total open: 4. Pre-Phase-2 legacy (no parent_thesis_id): 3.
⚠ 2 positions ≥80% of max_hold — approaching time stop.

---

## Equity (7-day trend, EOD per day)

| Day | Total equity (EOD) |
|---|---|
| 2026-05-27 | $72,906 |
| 2026-05-26 | $73,032 |
| 2026-05-25 | $73,369 |
| 2026-05-24 | $73,017 |
| 2026-05-23 | $72,248 |
| 2026-05-22 | $72,498 |
| 2026-05-21 | $71,789 |
| 2026-05-20 | $70,852 |
**Today vs yesterday: $-126**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 868 |
| Other ERROR | 427 |
| Python Traceback | 269 |
2 categories worth attention.

---

_End of snapshot._