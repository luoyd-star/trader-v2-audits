# Trader-v2 Daily Health Check — 2026-07-08

_Generated at 2026-07-08 11:30:01 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`1167` last_exit=`(never`
  - uptime/rss: `07-23:21:05  17872`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`1163` last_exit=`(never`
  - uptime/rss: `07-23:21:05   5504`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 625.9h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **625.9h old** — news_agent may have stopped producing.

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

- **package_id**: `197`
- **generated_at**: `2026-07-08 09:46:46` (age: 1.7h, today's: **YES**)
- **active_theses count**: 3 (expected 1-3)
- **alternative_hypotheses count**: 3 (expected ≥1)

### Active theses (the spine of today's trading)
- **#198** (conf=0.64, horizon=5d, 5 symbols incl 1 primary)
  - Claim: Mixed regime plus AI-capex cooling keeps damaged high-momentum semis vulnerable, with MU the cleanest short expression.
  - Falsification: Semiconductor damage thesis fails if risk_appetite turns risk_on, liquidity stops tightening, and MU/AMD/ARM all show positive short-window momentum in the same report cycle.
- **#199** (conf=0.55, horizon=4d, 4 symbols incl 1 primary)
  - Claim: Crypto repair is selective rather than broad beta, favoring ETH over BTC or DOGE chase while the regime remains mixed.
  - Falsification: Selective ETH thesis fails if ETH stops outperforming BTC while DOGE strength broadens and BTC resumes a stable equity-beta relationship for two report cycles.
- **#200** (conf=0.58, horizon=3d, 4 symbols incl 1 primary)
  - Claim: The equity index tape is range-prone, not a broad expansion signal, so SPY stability should not be extrapolated into QQQ chase.
  - Falsification: Range-prone thesis fails if fragility drops out of Elevated, liquidity no longer tightens, and SPY/QQQ/semiconductor breadth all improve together.

### Alternative hypotheses (rejected counter-theses)
- A clean risk-on expansion has begun across equities and crypto.
- WTI crude has repaired into a sustainable commodity uptrend.
- BTC is the cleanest crypto long because it is strengthening versus equities.

---

## Planner Thesis Usage (today)

| Agent | Total new plans | With parent_thesis_id | Coverage |
|---|---|---|---|
| Agent_1_Momentum | 1 | 1 | 100% |
| Agent_3_Macro | 1 | 1 | 100% |
| Agent_4_Volatility | 2 | 2 | 100% |
| Agent_5_Contrarian | 3 | 3 | 100% |
| Agent_7_PairsContrarian | 1 | 1 | 100% |

**System total: 8/8 plans linked to a thesis (100% if total else 0).**

---

## Manager Close Reasons (last 7 days)

| close_reason_type | Count | Total PnL |
|---|---|---|
| price_invalidation | 1 | $-283.0 |

⚠ **0 closes via thesis_falsified path.** Either no parent_thesis was actually broken in this window (fine), or the LLM never uses this path (concerning if persistent over multiple weeks).
Today's closes: 0 total — none

---

## Reviewer 2x2 (last 7 days)

| outcome_type | adherence | thesis_consistency | Count |
|---|---|---|---|
| FAILURE | WARN | WARN | 1 |

**Note**: Phase 4's `thesis_validity` / `execution_quality` / `lesson_target` fields
are emitted by the Reviewer LLM but NOT yet persisted as columns in `review_records`.
Until that's wired (TODO), we surface only the legacy adherence/thesis_consistency.

Sanity check: if `outcome_type` is 100% 'SUCCESS', that's the LLM self-flattery red flag.

---

## Open Positions

| Agent | Symbol | Dir | Entry | Margin | Held/Max | % used | parent_thesis_id |
|---|---|---|---|---|---|---|---|
| A4_Volatility | MUUSDT | SHORT | 930.4 | $1800 | 8.2h / 144h | 6% | 194 |

Total open: 1. Pre-Phase-2 legacy (no parent_thesis_id): 0.

---

## Equity (7-day trend, EOD per day)

| Day | Total equity (EOD) |
|---|---|
| 2026-07-08 | $73,129 |
| 2026-07-07 | $73,334 |
| 2026-07-06 | $73,179 |
| 2026-07-05 | $73,462 |
| 2026-07-04 | $73,462 |
| 2026-07-03 | $73,462 |
| 2026-07-02 | $73,462 |
| 2026-07-01 | $73,462 |
**Today vs yesterday: $-205**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 984 |
| Other ERROR | 58 |
| Python Traceback | 3 |
2 categories worth attention.

---

_End of snapshot._