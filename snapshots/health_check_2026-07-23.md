# Trader-v2 Daily Health Check — 2026-07-23

_Generated at 2026-07-23 11:30:05 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`1181` last_exit=`(never`
  - uptime/rss: `08:31:24 195264`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`1177` last_exit=`(never`
  - uptime/rss: `08:31:24   8768`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 215.1h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **215.1h old** — news_agent may have stopped producing.

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

- **package_id**: `263`
- **generated_at**: `2026-07-23 09:47:43` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#264** (conf=0.28, horizon=2d, 4 symbols incl 1 primary)
  - Claim: 在缺乏当日广泛修复证据时，半导体内部脆弱标的的选择性下行风险高于板块整体延续上涨的可信度。
  - Falsification: 若 MU、AMD、NVDA、ARM 与 QQQ 在同一交易日形成广泛同步强势，且后续一日仍保持板块扩散，则选择性半导体下行假设失效。

### Alternative hypotheses (rejected counter-theses)
- 科技与半导体正在形成可持续的广泛风险偏好修复。
- 宏观信息真空意味着所有方向性交易都应完全暂停。

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
| 2026-07-23 | $73,120 |
| 2026-07-22 | $73,120 |
| 2026-07-21 | $73,120 |
| 2026-07-20 | $73,120 |
| 2026-07-19 | $73,120 |
| 2026-07-18 | $73,120 |
| 2026-07-17 | $73,120 |
| 2026-07-16 | $73,120 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 1031 |
| Other ERROR | 183 |
| Python Traceback | 76 |
2 categories worth attention.

---

_End of snapshot._