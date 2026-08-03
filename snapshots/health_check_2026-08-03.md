# Trader-v2 Daily Health Check — 2026-08-03

_Generated at 2026-08-03 11:30:02 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`1181` last_exit=`(never`
  - uptime/rss: `11-08:31:21   4736`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`1177` last_exit=`(never`
  - uptime/rss: `11-08:31:21   2576`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 479.1h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **479.1h old** — news_agent may have stopped producing.

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

- **package_id**: `307`
- **generated_at**: `2026-08-03 09:47:31` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#308** (conf=0.28, horizon=1d, 4 symbols incl 1 primary)
  - Claim: 在当日宏观与结构化交接缺失时，防御资产相对高贝塔资产更适合作为低置信度风险表达。
  - Falsification: 结构化交接恢复有效regime标签，且股票广度、半导体广度与加密风险偏好在连续两个观察窗口共同确认风险偏好扩张。

### Alternative hypotheses (rejected counter-theses)
- 风险偏好正在全面修复，应做多科技与加密高贝塔资产。
- 半导体已进入可持续的选择性下跌阶段，应直接做空最弱芯片股。

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
| 2026-08-03 | $73,120 |
| 2026-08-02 | $73,120 |
| 2026-08-01 | $73,120 |
| 2026-07-31 | $73,120 |
| 2026-07-30 | $73,120 |
| 2026-07-29 | $73,120 |
| 2026-07-28 | $73,120 |
| 2026-07-27 | $73,120 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 1186 |
| Other ERROR | 168 |
| Python Traceback | 76 |
2 categories worth attention.

---

_End of snapshot._