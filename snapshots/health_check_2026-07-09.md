# Trader-v2 Daily Health Check — 2026-07-09

_Generated at 2026-07-09 11:30:05 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`1167` last_exit=`(never`
  - uptime/rss: `08-23:21:09  10064`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`1163` last_exit=`(never`
  - uptime/rss: `08-23:21:09   5488`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 649.9h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **649.9h old** — news_agent may have stopped producing.

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

- **package_id**: `204`
- **generated_at**: `2026-07-09 09:45:43` (age: 1.7h, today's: **YES**)
- **active_theses count**: 3 (expected 1-3)
- **alternative_hypotheses count**: 3 (expected ≥1)

### Active theses (the spine of today's trading)
- **#205** (conf=0.61, horizon=5d, 4 symbols incl 1 primary)
  - Claim: Tightening liquidity and rising real yields cap broad growth beta despite calm headline volatility.
  - Falsification: Risk_label upgrades from mixed to clean risk-on while liquidity stops tightening and QQQ/mega-cap breadth improves together for 2 sessions.
- **#206** (conf=0.64, horizon=4d, 5 symbols incl 1 primary)
  - Claim: High-RS semiconductor leadership is breaking internally, so weak memory/AI-beta names are fade candidates.
  - Falsification: Semiconductor cohort breadth repairs with MU, AMD, ARM, NVDA, and TSM all showing positive 5d momentum while AI capex status stops cooling.
- **#207** (conf=0.58, horizon=5d, 4 symbols incl 1 primary)
  - Claim: Crypto-linked equity remains weaker than crypto itself, so MSTR is a cleaner short than BTC or ETH.
  - Falsification: Crypto-linked equities begin outperforming BTC and QQQ simultaneously while BTC relative strength improves on both 7d and 30d windows.

### Alternative hypotheses (rejected counter-theses)
- The market is shifting into clean broad risk-on and long index beta should be increased.
- BABA has started a durable trend reversal after its large event-driven rally.
- Precious metals are ready to resume as defensive hedges under elevated fragility.

---

## Planner Thesis Usage (today)

| Agent | Total new plans | With parent_thesis_id | Coverage |
|---|---|---|---|
| Agent_1_Momentum | 3 | 3 | 100% |
| Agent_2_MeanReversion | 4 | 4 | 100% |
| Agent_3_Macro | 2 | 2 | 100% |
| Agent_4_Volatility | 2 | 2 | 100% |
| Agent_5_Contrarian | 2 | 2 | 100% |
| Agent_7_PairsContrarian | 3 | 3 | 100% |

**System total: 16/16 plans linked to a thesis (100% if total else 0).**

---

## Manager Close Reasons (last 7 days)

| close_reason_type | Count | Total PnL |
|---|---|---|
| thesis_falsified | 1 | $-59.0 |
| price_invalidation | 1 | $-283.0 |

✓ thesis_falsified fired 1x — the new path is in use.
Today's closes: 1 total — thesis_falsified:1

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
| 2026-07-09 | $73,120 |
| 2026-07-08 | $73,205 |
| 2026-07-07 | $73,334 |
| 2026-07-06 | $73,179 |
| 2026-07-05 | $73,462 |
| 2026-07-04 | $73,462 |
| 2026-07-03 | $73,462 |
| 2026-07-02 | $73,462 |
**Today vs yesterday: $-85**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 983 |
| Other ERROR | 55 |
| Python Traceback | 3 |
2 categories worth attention.

---

_End of snapshot._