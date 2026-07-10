# Trader-v2 Daily Health Check — 2026-07-10

_Generated at 2026-07-10 11:30:03 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`1167` last_exit=`(never`
  - uptime/rss: `09-23:21:07   8176`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`1163` last_exit=`(never`
  - uptime/rss: `09-23:21:07   5408`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 673.9h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **673.9h old** — news_agent may have stopped producing.

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

- **package_id**: `211`
- **generated_at**: `2026-07-10 09:45:37` (age: 1.7h, today's: **YES**)
- **active_theses count**: 2 (expected 1-3)
- **alternative_hypotheses count**: 3 (expected ≥1)

### Active theses (the spine of today's trading)
- **#212** (conf=0.48, horizon=3d, 4 symbols incl 1 primary)
  - Claim: Broad US equity beta should be treated as a fade-on-strength environment, not a clean risk-on regime.
  - Falsification: Upstream handoff upgrades to clean risk-on while liquidity-tightening and equity-bond hedge-failure warnings disappear for 2 consecutive daily packages.
- **#213** (conf=0.44, horizon=2d, 5 symbols incl 1 primary)
  - Claim: Semiconductor leadership remains unreliable; high RS names should be treated as selective downside-vol candidates.
  - Falsification: Semiconductor cohort stress disappears when MU, ARM, AMD, NVDA, and TSM all stop showing drawdown/breakdown behavior and leadership breadth improves for 2 sessions.

### Alternative hypotheses (rejected counter-theses)
- Fragility easing means clean risk-on and broad long exposure should be added.
- Crypto beta should confirm equity risk-on through BTC and ETH longs.
- Oil weakness should be repeated as a fresh macro trade.

---

## Planner Thesis Usage (today)

| Agent | Total new plans | With parent_thesis_id | Coverage |
|---|---|---|---|
| Agent_1_Momentum | 1 | 1 | 100% |
| Agent_4_Volatility | 1 | 1 | 100% |

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
| 2026-07-10 | $73,120 |
| 2026-07-09 | $73,120 |
| 2026-07-08 | $73,205 |
| 2026-07-07 | $73,334 |
| 2026-07-06 | $73,179 |
| 2026-07-05 | $73,462 |
| 2026-07-04 | $73,462 |
| 2026-07-03 | $73,462 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 1004 |
| Other ERROR | 55 |
| Python Traceback | 3 |
2 categories worth attention.

---

_End of snapshot._