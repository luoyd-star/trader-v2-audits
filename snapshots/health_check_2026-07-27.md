# Trader-v2 Daily Health Check — 2026-07-27

_Generated at 2026-07-27 11:30:04 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`1181` last_exit=`(never`
  - uptime/rss: `04-08:31:23   5168`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`1177` last_exit=`(never`
  - uptime/rss: `04-08:31:23   3040`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 311.1h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **311.1h old** — news_agent may have stopped producing.

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

- **package_id**: `279`
- **generated_at**: `2026-07-27 09:46:42` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#280** (conf=0.30, horizon=2d, 4 symbols incl 1 primary)
  - Claim: Stale breadth evidence leaves technology leadership vulnerable to tactical mean reversion, favoring low-conviction QQQ downside.
  - Falsification: A fresh completed-session dataset and structured handoff jointly show QQQ, SPY, and at least four tradable semiconductors strengthening together for two consecutive sessions.

### Alternative hypotheses (rejected counter-theses)
- Broad risk-on continuation is intact despite the missing latest-session data.
- Semiconductors offer a clean selective-short opportunity independent of the broad index.

---

## Planner Thesis Usage (today)

| Agent | Total new plans | With parent_thesis_id | Coverage |
|---|---|---|---|
| Agent_5_Contrarian | 2 | 2 | 100% |

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
| 2026-07-27 | $73,120 |
| 2026-07-26 | $73,120 |
| 2026-07-25 | $73,120 |
| 2026-07-24 | $73,120 |
| 2026-07-23 | $73,120 |
| 2026-07-22 | $73,120 |
| 2026-07-21 | $73,120 |
| 2026-07-20 | $73,120 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 1061 |
| Other ERROR | 183 |
| Python Traceback | 76 |
2 categories worth attention.

---

_End of snapshot._