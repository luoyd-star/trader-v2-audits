# Trader-v2 Daily Health Check — 2026-08-06

_Generated at 2026-08-06 11:30:01 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`1181` last_exit=`(never`
  - uptime/rss: `14-08:31:20  23456`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`1177` last_exit=`(never`
  - uptime/rss: `14-08:31:20   2544`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 551.1h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **551.1h old** — news_agent may have stopped producing.

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

## Strategist Output (latest package) ⚠ NOT TODAY

- **package_id**: `315`
- **generated_at**: `2026-08-05 09:46:54` (age: 25.7h, today's: **NO — STALE**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#316** (conf=0.34, horizon=2d, 4 symbols incl 1 primary)
  - Claim: Semiconductor leadership remains too narrow and failure-prone to confirm a durable broad-tech advance.
  - Falsification: Semiconductor breadth expands across NVDA, AMD, ARM, ASML, TSM, MU, AVGO and MRVL while both QQQ and SPY confirm strength for two consecutive sessions.

### Alternative hypotheses (rejected counter-theses)
- Broad technology leadership is repairing and should be bought through QQQ.
- Commodity inflation is the dominant trade and warrants long exposure to gold, oil, or copper.

---

## Planner Thesis Usage (today)

| Agent | Total new plans | With parent_thesis_id | Coverage |
|---|---|---|---|
| Agent_1_Momentum | 1 | 1 | 100% |

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
| 2026-08-06 | $73,120 |
| 2026-08-05 | $73,120 |
| 2026-08-04 | $73,120 |
| 2026-08-03 | $73,120 |
| 2026-08-02 | $73,120 |
| 2026-08-01 | $73,120 |
| 2026-07-31 | $73,120 |
| 2026-07-30 | $73,120 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 1252 |
| Other ERROR | 172 |
| Python Traceback | 76 |
2 categories worth attention.

---

_End of snapshot._