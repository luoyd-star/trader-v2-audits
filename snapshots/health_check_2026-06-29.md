# Trader-v2 Daily Health Check — 2026-06-29

_Generated at 2026-06-29 11:30:05 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`2235` last_exit=`(never`
  - uptime/rss: `04-20:58:43  18912`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`2231` last_exit=`(never`
  - uptime/rss: `04-20:58:43   5872`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 409.9h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **409.9h old** — news_agent may have stopped producing.

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

- **package_id**: `156`
- **generated_at**: `2026-06-29 09:45:29` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#157** (conf=0.46, horizon=5d, 5 symbols incl 1 primary)
  - Claim: Elevated stress plus unreliable risk-on chains favors keeping index exposure defensive rather than chasing longs.
  - Falsification: Stress leaves the Elevated/Stress zone and news_agent provides a dated risk-on regime with broad breadth confirmation for two consecutive sessions.

### Alternative hypotheses (rejected counter-theses)
- Broad equity risk-on should be bought after the recent calm tape.
- Energy stabilization should support crude and oil-equity longs.

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

| Agent | Symbol | Dir | Entry | Margin | Held/Max | % used | parent_thesis_id |
|---|---|---|---|---|---|---|---|
| A4_Volatility | QQQUSDT | SHORT | 713.34 | $1800 | 47.3h / 144h | 33% | 136 |

Total open: 1. Pre-Phase-2 legacy (no parent_thesis_id): 0.

---

## Equity (7-day trend, EOD per day)

| Day | Total equity (EOD) |
|---|---|
| 2026-06-29 | $73,545 |
| 2026-06-28 | $73,566 |
| 2026-06-27 | $73,563 |
| 2026-06-26 | $73,538 |
| 2026-06-25 | $73,538 |
| 2026-06-24 | $73,538 |
| 2026-06-23 | $73,538 |
| 2026-06-22 | $73,538 |
**Today vs yesterday: $-21**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 1057 |
| Other ERROR | 59 |
| Python Traceback | 1 |
2 categories worth attention.

---

_End of snapshot._