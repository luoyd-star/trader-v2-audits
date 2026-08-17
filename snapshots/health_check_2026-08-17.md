# Trader-v2 Daily Health Check — 2026-08-17

_Generated at 2026-08-17 11:30:00 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`817` last_exit=`(never`
  - uptime/rss: `08-09:54:53 415216`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`812` last_exit=`(never`
  - uptime/rss: `08-09:54:53   9152`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 815.1h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **815.1h old** — news_agent may have stopped producing.

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

- **package_id**: `359`
- **generated_at**: `2026-08-17 09:45:48` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#360** (conf=0.22, horizon=1d, 3 symbols incl 1 primary)
  - Claim: Until breadth and regime data are restored, broad US tech upside lacks confirmation and QQQ downside is the least-specific conditional expression.
  - Falsification: A complete handoff classifies the regime as risk-on and at least two independent breadth, liquidity, or volatility measures confirm broad technology participation for two consecutive sessions.

### Alternative hypotheses (rejected counter-theses)
- The missing upstream evidence is only a pipeline failure while the true market regime remains broadly risk-on.
- Macro uncertainty supports an immediate defensive long in gold.

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
| 2026-08-17 | $73,120 |
| 2026-08-16 | $73,120 |
| 2026-08-15 | $73,120 |
| 2026-08-14 | $73,120 |
| 2026-08-13 | $73,120 |
| 2026-08-12 | $73,120 |
| 2026-08-11 | $73,120 |
| 2026-08-10 | $73,120 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 1309 |
| Other ERROR | 180 |
| Python Traceback | 76 |
2 categories worth attention.

---

_End of snapshot._