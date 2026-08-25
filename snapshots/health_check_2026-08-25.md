# Trader-v2 Daily Health Check — 2026-08-25

_Generated at 2026-08-25 11:30:04 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`817` last_exit=`(never`
  - uptime/rss: `16-09:54:57 428304`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`812` last_exit=`(never`
  - uptime/rss: `16-09:54:57   8928`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 1007.1h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **1007.1h old** — news_agent may have stopped producing.

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

- **package_id**: `391`
- **generated_at**: `2026-08-25 09:45:40` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#392** (conf=0.25, horizon=1d, 3 symbols incl 1 primary)
  - Claim: 上游证据真空使广泛风险偏好延续缺乏确认；仅在主要指数同步转弱后考虑战术性做空。
  - Falsification: 完整交接恢复并明确标记risk-on，且SPY、QQQ与半导体代表组连续两个交易日同步改善市场广度和相对强度。

### Alternative hypotheses (rejected counter-theses)
- 风险资产可能在缺少新增宏观催化时继续惯性上涨。
- 当前最优判断可能是完全无方向的区间震荡。

---

## Planner Thesis Usage (today)

**No plans created today yet.** Either Planner hasn't run, or it produced 0 plans (correct behavior if no fitting thesis).

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
| 2026-08-25 | $73,120 |
| 2026-08-24 | $73,120 |
| 2026-08-23 | $73,120 |
| 2026-08-22 | $73,120 |
| 2026-08-21 | $73,120 |
| 2026-08-20 | $73,120 |
| 2026-08-19 | $73,120 |
| 2026-08-18 | $73,120 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 1394 |
| Other ERROR | 73 |
| Python Traceback | 15 |
2 categories worth attention.

---

_End of snapshot._