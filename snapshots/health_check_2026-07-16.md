# Trader-v2 Daily Health Check — 2026-07-16

_Generated at 2026-07-16 11:30:01 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`40806` last_exit=`never`
  - uptime/rss: `16:06:44  11264`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`40804` last_exit=`never`
  - uptime/rss: `16:06:44   7024`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 47.1h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **47.1h old** — news_agent may have stopped producing.

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

- **package_id**: `234`
- **generated_at**: `2026-07-16 09:45:50` (age: 1.7h, today's: **YES**)
- **active_theses count**: 2 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#235** (conf=0.62, horizon=5d, 4 symbols incl 1 primary)
  - Claim: 风险偏好修复仍集中于少数大型科技股，AAPL等强势股短期继续跑赢宽基科技指数。
  - Falsification: AAPL、META和AMZN连续两个交易日不再共同跑赢QQQ，且科技行业上涨广度同步扩散至半导体和软件弱势组。
- **#236** (conf=0.60, horizon=5d, 4 symbols incl 1 primary)
  - Claim: 高集中与对冲失效使弱势资产更易放大下行，ORCL和EWY可能继续落后于风险偏好修复。
  - Falsification: ORCL和EWY连续两个交易日共同跑赢各自基准，同时因子集中度下降且股债相关性恢复负向对冲状态。

### Alternative hypotheses (rejected counter-theses)
- 风险偏好修复将扩散为SPY和QQQ的全面持续上涨。
- BTC与黄金的结构性同向关系已经形成可交易的BTC多头信号。

---

## Planner Thesis Usage (today)

| Agent | Total new plans | With parent_thesis_id | Coverage |
|---|---|---|---|
| Agent_1_Momentum | 5 | 5 | 100% |
| Agent_3_Macro | 5 | 5 | 100% |
| Agent_4_Volatility | 5 | 5 | 100% |
| Agent_5_Contrarian | 5 | 5 | 100% |
| Agent_7_PairsContrarian | 5 | 5 | 100% |

**System total: 25/25 plans linked to a thesis (100% if total else 0).**

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
| 2026-07-16 | $73,120 |
| 2026-07-15 | $73,120 |
| 2026-07-14 | $73,120 |
| 2026-07-13 | $73,120 |
| 2026-07-12 | $73,120 |
| 2026-07-11 | $73,120 |
| 2026-07-10 | $73,120 |
| 2026-07-09 | $73,120 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 1012 |
| Other ERROR | 55 |
| Python Traceback | 3 |
2 categories worth attention.

---

_End of snapshot._