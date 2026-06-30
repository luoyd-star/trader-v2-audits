# Trader-v2 Daily Health Check — 2026-06-30

_Generated at 2026-06-30 11:30:05 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`1137` last_exit=`(never`
  - uptime/rss: `10:20:00 162816`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`1134` last_exit=`(never`
  - uptime/rss: `10:20:00   8096`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 433.9h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **433.9h old** — news_agent may have stopped producing.

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

- **package_id**: `160`
- **generated_at**: `2026-06-30 09:45:34` (age: 1.7h, today's: **YES**)
- **active_theses count**: 2 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#161** (conf=0.62, horizon=5d, 5 symbols incl 1 primary)
  - Claim: Mixed regime plus elevated fragility favors fading broad equity risk-on rather than adding long beta.
  - Falsification: Regime_Dashboard upgrades from mixed to clean risk-on while fragility leaves Elevated and credit stress components improve for two consecutive reports.
- **#162** (conf=0.56, horizon=4d, 5 symbols incl 1 primary)
  - Claim: Semiconductor relative strength is narrow and should not be extrapolated into broad mega-cap tech repair.
  - Falsification: NVDA, AAPL, AMZN, MSFT, and QQQ all confirm semiconductor leadership with aligned positive breadth and improving regime readings in the same session.

### Alternative hypotheses (rejected counter-theses)
- A clean risk-on breakout is starting and broad equity longs should be bought.
- Semiconductor strength is enough to buy the whole AI and mega-cap complex.

---

## Planner Thesis Usage (today)

| Agent | Total new plans | With parent_thesis_id | Coverage |
|---|---|---|---|
| Agent_1_Momentum | 5 | 5 | 100% |
| Agent_2_MeanReversion | 1 | 1 | 100% |
| Agent_3_Macro | 5 | 5 | 100% |
| Agent_4_Volatility | 4 | 4 | 100% |
| Agent_5_Contrarian | 5 | 5 | 100% |
| Agent_7_PairsContrarian | 3 | 3 | 100% |

**System total: 23/23 plans linked to a thesis (100% if total else 0).**

---

## Manager Close Reasons (last 7 days)

| close_reason_type | Count | Total PnL |
|---|---|---|
| price_invalidation | 1 | $-76.0 |

⚠ **0 closes via thesis_falsified path.** Either no parent_thesis was actually broken in this window (fine), or the LLM never uses this path (concerning if persistent over multiple weeks).
Today's closes: 1 total — price_invalidation:1

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
| 2026-06-30 | $73,462 |
| 2026-06-29 | $73,532 |
| 2026-06-28 | $73,566 |
| 2026-06-27 | $73,563 |
| 2026-06-26 | $73,538 |
| 2026-06-25 | $73,538 |
| 2026-06-24 | $73,538 |
| 2026-06-23 | $73,538 |
**Today vs yesterday: $-70**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 1055 |
| Other ERROR | 64 |
| Python Traceback | 3 |
2 categories worth attention.

---

_End of snapshot._