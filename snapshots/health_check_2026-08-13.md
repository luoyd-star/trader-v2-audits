# Trader-v2 Daily Health Check — 2026-08-13

_Generated at 2026-08-13 11:30:05 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`817` last_exit=`(never`
  - uptime/rss: `04-09:54:58 273488`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`812` last_exit=`(never`
  - uptime/rss: `04-09:54:58  10352`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 719.1h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **719.1h old** — news_agent may have stopped producing.

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

- **package_id**: `343`
- **generated_at**: `2026-08-13 09:45:59` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#344** (conf=0.26, horizon=1d, 4 symbols incl 1 primary)
  - Claim: 信息真空叠加科技确认链历史失效，使宽基科技的确认后做空优于追逐多头，但未出现同步弱化时应等待。
  - Falsification: 若科技市场广度、半导体群体与主要大型科技股在同一交易日形成一致且持续的风险偏好修复，则防御性做空逻辑失效。

### Alternative hypotheses (rejected counter-theses)
- 大型科技与半导体正在形成可持续的风险偏好修复，应做多 QQQ。
- 宏观不确定性正在推动黄金与白银形成新的防御性上涨趋势。

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
| 2026-08-13 | $73,120 |
| 2026-08-12 | $73,120 |
| 2026-08-11 | $73,120 |
| 2026-08-10 | $73,120 |
| 2026-08-09 | $73,120 |
| 2026-08-08 | $73,120 |
| 2026-08-07 | $73,120 |
| 2026-08-06 | $73,120 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 1285 |
| Other ERROR | 177 |
| Python Traceback | 76 |
2 categories worth attention.

---

_End of snapshot._