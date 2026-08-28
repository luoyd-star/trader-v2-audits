# Trader-v2 Daily Health Check — 2026-08-28

_Generated at 2026-08-28 11:30:05 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`817` last_exit=`(never`
  - uptime/rss: `19-09:54:58  40192`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`812` last_exit=`(never`
  - uptime/rss: `19-09:54:58   8640`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 1079.1h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **1079.1h old** — news_agent may have stopped producing.

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

- **package_id**: `403`
- **generated_at**: `2026-08-28 09:45:45` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#404** (conf=0.28, horizon=1d, 4 symbols incl 1 primary)
  - Claim: 在上游信号缺失且半导体广度历史上不可靠时，ARM反弹失败后的选择性空头优于追逐科技板块多头。
  - Falsification: news_agent恢复有效regime与方向性证据，且ARM、NVDA、AMD、AVGO和TSM中至少四个同步显示持续多头广度确认。

### Alternative hypotheses (rejected counter-theses)
- 大型科技与半导体已进入可持续的广泛风险偏好修复。
- 市场正进入应全面做空股票与加密资产的系统性risk-off阶段。

---

## Planner Thesis Usage (today)

| Agent | Total new plans | With parent_thesis_id | Coverage |
|---|---|---|---|
| Agent_5_Contrarian | 1 | 1 | 100% |

**System total: 1/1 plans linked to a thesis (100% if total else 0).**

---

## Manager Close Reasons (last 7 days)

(no closes in last 7d)

---

## Reviewer 2x2 (last 7 days)

(no reviews in last 7d)

---

## Open Positions

(no open trades)

---

## Equity (7-day trend, EOD per day)

| Day | Total equity (EOD) |
|---|---|
| 2026-08-28 | $73,120 |
| 2026-08-27 | $73,120 |
| 2026-08-26 | $73,120 |
| 2026-08-25 | $73,120 |
| 2026-08-24 | $73,120 |
| 2026-08-23 | $73,120 |
| 2026-08-22 | $73,120 |
| 2026-08-21 | $73,120 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 1473 |
| Other ERROR | 66 |
| Python Traceback | 7 |
2 categories worth attention.

---

_End of snapshot._