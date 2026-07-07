# Trader-v2 Daily Health Check — 2026-07-07

_Generated at 2026-07-07 11:30:04 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`1167` last_exit=`(never`
  - uptime/rss: `06-23:21:09  21776`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`1163` last_exit=`(never`
  - uptime/rss: `06-23:21:09   6064`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 601.9h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **601.9h old** — news_agent may have stopped producing.

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

- **package_id**: `192`
- **generated_at**: `2026-07-07 09:45:34` (age: 1.7h, today's: **YES**)
- **active_theses count**: 2 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#193** (conf=0.56, horizon=3d, 4 symbols incl 1 primary)
  - Claim: Mixed Elevated-fragility conditions argue against chasing broad beta; QQQ weakness is the cleanest downside expression.
  - Falsification: Regime_Dashboard shifts from mixed to broad risk-on while fragility exits Elevated and turbulence/absorption warnings disappear for two consecutive daily reports.
- **#194** (conf=0.51, horizon=3d, 4 symbols incl 1 primary)
  - Claim: Semiconductor leadership is unreliable as a broad confirmation signal; avoid long extrapolation and prefer selective downside in MU.
  - Falsification: MU and the broader semiconductor cohort stop showing multi-report pullback behavior while AI semis confirm across NVDA, AMD, ASML, AVGO, and TSM for two consecutive reports.

### Alternative hypotheses (rejected counter-theses)
- Low VIX and normal term structure mean broad risk-on longs should be added today.
- MU relative-strength rank #3 makes MU a long continuation candidate.

---

## Planner Thesis Usage (today)

| Agent | Total new plans | With parent_thesis_id | Coverage |
|---|---|---|---|
| Agent_1_Momentum | 2 | 2 | 100% |
| Agent_2_MeanReversion | 2 | 2 | 100% |
| Agent_3_Macro | 4 | 4 | 100% |
| Agent_4_Volatility | 3 | 3 | 100% |
| Agent_5_Contrarian | 4 | 4 | 100% |
| Agent_7_PairsContrarian | 2 | 2 | 100% |

**System total: 17/17 plans linked to a thesis (100% if total else 0).**

---

## Manager Close Reasons (last 7 days)

| close_reason_type | Count | Total PnL |
|---|---|---|
| price_invalidation | 2 | $-359.0 |

⚠ **0 closes via thesis_falsified path.** Either no parent_thesis was actually broken in this window (fine), or the LLM never uses this path (concerning if persistent over multiple weeks).
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
| 2026-07-07 | $73,179 |
| 2026-07-06 | $73,179 |
| 2026-07-05 | $73,462 |
| 2026-07-04 | $73,462 |
| 2026-07-03 | $73,462 |
| 2026-07-02 | $73,462 |
| 2026-07-01 | $73,462 |
| 2026-06-30 | $73,462 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 1023 |
| Other ERROR | 73 |
| Python Traceback | 4 |
2 categories worth attention.

---

_End of snapshot._