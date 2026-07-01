# Trader-v2 Daily Health Check — 2026-07-01

_Generated at 2026-07-01 11:30:05 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`1167` last_exit=`(never`
  - uptime/rss: `23:21:09  23440`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`1163` last_exit=`(never`
  - uptime/rss: `23:21:09   6928`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 457.9h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **457.9h old** — news_agent may have stopped producing.

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

- **package_id**: `165`
- **generated_at**: `2026-07-01 09:45:35` (age: 1.7h, today's: **YES**)
- **active_theses count**: 3 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#166** (conf=0.42, horizon=3d, 3 symbols incl 1 primary)
  - Claim: Mixed regime plus tightening liquidity favors cautious SPY downside rather than broad risk-on expansion.
  - Falsification: Fragility drops from Elevated to Watch, liquidity is no longer tightening, and breadth expands beyond semiconductor leaders for two consecutive reports.
- **#167** (conf=0.58, horizon=3d, 3 symbols incl 1 primary)
  - Claim: Crypto remains an under-confirmed risk asset; BTC weakness is more actionable than equity relief.
  - Falsification: BTC turns positive over the thesis window while its relative_strength_state versus SPY is no longer weakening and ETH also regains confirmation.
- **#168** (conf=0.60, horizon=3d, 3 symbols incl 1 primary)
  - Claim: WTI weakness is idiosyncratic and persistent, so crude downside remains cleaner than equity macro shorts.
  - Falsification: WTI 20-day cumulative residual rises back above the sustained weakness threshold and crude exits the bottom RS cohort for two reports.

### Alternative hypotheses (rejected counter-theses)
- Semiconductor RS leadership can keep driving upside in AMD, INTC, MU and TSM.
- Falling real yields could restart a clean risk-on rally across equities and crypto.

---

## Planner Thesis Usage (today)

| Agent | Total new plans | With parent_thesis_id | Coverage |
|---|---|---|---|
| Agent_1_Momentum | 2 | 2 | 100% |
| Agent_3_Macro | 1 | 1 | 100% |
| Agent_4_Volatility | 2 | 2 | 100% |
| Agent_5_Contrarian | 1 | 1 | 100% |
| Agent_7_PairsContrarian | 1 | 1 | 100% |

**System total: 7/7 plans linked to a thesis (100% if total else 0).**

---

## Manager Close Reasons (last 7 days)

| close_reason_type | Count | Total PnL |
|---|---|---|
| price_invalidation | 1 | $-76.0 |

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
| 2026-07-01 | $73,462 |
| 2026-06-30 | $73,462 |
| 2026-06-29 | $73,532 |
| 2026-06-28 | $73,566 |
| 2026-06-27 | $73,563 |
| 2026-06-26 | $73,538 |
| 2026-06-25 | $73,538 |
| 2026-06-24 | $73,538 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 1044 |
| Other ERROR | 64 |
| Python Traceback | 3 |
2 categories worth attention.

---

_End of snapshot._