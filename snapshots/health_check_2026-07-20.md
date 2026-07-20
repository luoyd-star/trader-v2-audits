# Trader-v2 Daily Health Check — 2026-07-20

_Generated at 2026-07-20 11:30:00 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`40806` last_exit=`never`
  - uptime/rss: `04-16:06:43   8352`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`40804` last_exit=`never`
  - uptime/rss: `04-16:06:43   5680`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 143.1h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **143.1h old** — news_agent may have stopped producing.

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

- **package_id**: `251`
- **generated_at**: `2026-07-20 09:47:06` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#252** (conf=0.31, horizon=1d, 4 symbols incl 1 primary)
  - Claim: Until fresh cross-asset confirmation arrives, broad U.S. risk beta has asymmetric downside from stale-information adverse selection.
  - Falsification: A newly completed U.S. session shows broad SPY and QQQ participation alongside multi-symbol semiconductor confirmation, and a structured handoff identifies coherent risk-on breadth without material broken-chain warnings.

### Alternative hypotheses (rejected counter-theses)
- The stale-data gap conceals a broad risk-on continuation that favors QQQ and semiconductor longs.
- Semiconductors are entering a renewed selective downside-volatility regime led by MU and ARM.

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
| 2026-07-20 | $73,120 |
| 2026-07-19 | $73,120 |
| 2026-07-18 | $73,120 |
| 2026-07-17 | $73,120 |
| 2026-07-16 | $73,120 |
| 2026-07-15 | $73,120 |
| 2026-07-14 | $73,120 |
| 2026-07-13 | $73,120 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 1030 |
| Other ERROR | 55 |
| Python Traceback | 3 |
2 categories worth attention.

---

_End of snapshot._