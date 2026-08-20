# Trader-v2 Daily Health Check — 2026-08-20

_Generated at 2026-08-20 11:30:03 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`817` last_exit=`(never`
  - uptime/rss: `11-09:54:57 337408`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`812` last_exit=`(never`
  - uptime/rss: `11-09:54:57   9104`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 887.1h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **887.1h old** — news_agent may have stopped producing.

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

- **package_id**: `371`
- **generated_at**: `2026-08-20 09:45:39` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#372** (conf=0.22, horizon=2d, 3 symbols incl 1 primary)
  - Claim: Absent fresh breadth confirmation, narrow semiconductor strength remains unreliable and favors conditional ARM downside over broad tech exposure.
  - Falsification: Semiconductor breadth strengthens across AMD, ASML, AVGO, NVDA, TSM, and ARM for two consecutive sessions while the upstream handoff confirms a broad tech-repair regime.

### Alternative hypotheses (rejected counter-theses)
- Mega-cap technology is entering a broad, durable repair phase.
- The correct response to the information vacuum is a broad defensive long in gold.

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
| 2026-08-20 | $73,120 |
| 2026-08-19 | $73,120 |
| 2026-08-18 | $73,120 |
| 2026-08-17 | $73,120 |
| 2026-08-16 | $73,120 |
| 2026-08-15 | $73,120 |
| 2026-08-14 | $73,120 |
| 2026-08-13 | $73,120 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 1345 |
| Other ERROR | 183 |
| Python Traceback | 78 |
2 categories worth attention.

---

_End of snapshot._