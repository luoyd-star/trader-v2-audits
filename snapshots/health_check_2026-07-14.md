# Trader-v2 Daily Health Check — 2026-07-14

_Generated at 2026-07-14 11:30:00 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`851` last_exit=`(never`
  - uptime/rss: `02-13:23:09  18832`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`844` last_exit=`(never`
  - uptime/rss: `02-13:23:09   5984`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 769.9h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **769.9h old** — news_agent may have stopped producing.

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

- **package_id**: `229`
- **generated_at**: `2026-07-14 09:46:11` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 3 (expected ≥1)

### Active theses (the spine of today's trading)
- **#230** (conf=0.56, horizon=5d, 5 symbols incl 1 primary)
  - Claim: 半导体长期相对强度尚高，但短线回撤与破位意味着领导力暂时失真，未来3至5日偏向选择性下行而非板块追多。
  - Falsification: AMD、MU、ARM和TSM中至少三者的5日收益同步转正，并连续两个日度观察呈现共同的短线趋势修复。

### Alternative hypotheses (rejected counter-theses)
- 半导体回撤只是强势趋势中的短暂整理，板块将迅速恢复广谱上涨。
- 黄金和白银的韧性正在提供可立即交易的贵金属多头信号。
- 高置信度历史类比预示今日应广泛增加风险资产多头。

---

## Planner Thesis Usage (today)

| Agent | Total new plans | With parent_thesis_id | Coverage |
|---|---|---|---|
| Agent_1_Momentum | 2 | 2 | 100% |
| Agent_2_MeanReversion | 3 | 3 | 100% |
| Agent_3_Macro | 3 | 3 | 100% |
| Agent_4_Volatility | 3 | 3 | 100% |
| Agent_5_Contrarian | 4 | 4 | 100% |
| Agent_7_PairsContrarian | 3 | 3 | 100% |

**System total: 18/18 plans linked to a thesis (100% if total else 0).**

---

## Manager Close Reasons (last 7 days)

| close_reason_type | Count | Total PnL |
|---|---|---|
| thesis_falsified | 1 | $-59.0 |

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
| 2026-07-14 | $73,120 |
| 2026-07-13 | $73,120 |
| 2026-07-12 | $73,120 |
| 2026-07-11 | $73,120 |
| 2026-07-10 | $73,120 |
| 2026-07-09 | $73,120 |
| 2026-07-08 | $73,205 |
| 2026-07-07 | $73,334 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 1020 |
| Other ERROR | 55 |
| Python Traceback | 3 |
2 categories worth attention.

---

_End of snapshot._