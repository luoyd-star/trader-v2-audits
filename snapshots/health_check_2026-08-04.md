# Trader-v2 Daily Health Check — 2026-08-04

_Generated at 2026-08-04 11:30:03 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`1181` last_exit=`(never`
  - uptime/rss: `12-08:31:22   6864`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`1177` last_exit=`(never`
  - uptime/rss: `12-08:31:22   2560`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 503.1h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **503.1h old** — news_agent may have stopped producing.

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

- **package_id**: `311`
- **generated_at**: `2026-08-04 09:47:37` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#312** (conf=0.30, horizon=1d, 5 symbols incl 1 primary)
  - Claim: Without corroborated breadth, tech beta is more vulnerable to failed continuation than to a clean upside trend.
  - Falsification: Broad semiconductor participation and mega-cap breadth jointly confirm risk-on conditions for two consecutive sessions, supported by a structured analyst handoff.

### Alternative hypotheses (rejected counter-theses)
- Broad technology and semiconductor leadership is beginning a durable risk-on continuation.
- Fiscal uncertainty is sufficient to support an immediate XAU long thesis.

---

## Planner Thesis Usage (today)

| Agent | Total new plans | With parent_thesis_id | Coverage |
|---|---|---|---|
| Agent_1_Momentum | 1 | 1 | 100% |
| Agent_4_Volatility | 1 | 1 | 100% |

**System total: 2/2 plans linked to a thesis (100% if total else 0).**

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
| 2026-08-04 | $73,120 |
| 2026-08-03 | $73,120 |
| 2026-08-02 | $73,120 |
| 2026-08-01 | $73,120 |
| 2026-07-31 | $73,120 |
| 2026-07-30 | $73,120 |
| 2026-07-29 | $73,120 |
| 2026-07-28 | $73,120 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 1185 |
| Other ERROR | 168 |
| Python Traceback | 76 |
2 categories worth attention.

---

_End of snapshot._