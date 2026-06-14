# Trader-v2 Daily Health Check — 2026-06-14

_Generated at 2026-06-14 11:30:03 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`2179` last_exit=`(never`
  - uptime/rss: `01-16:13:46  11328`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`2176` last_exit=`(never`
  - uptime/rss: `01-16:13:46   7584`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 49.9h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **49.9h old** — news_agent may have stopped producing.

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

- **package_id**: `102`
- **generated_at**: `2026-06-14 09:45:27` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#103** (conf=0.32, horizon=1d, 4 symbols incl 1 primary)
  - Claim: Data scarcity makes broad equity downside the only defensible actionable bias if exposure must be expressed today.
  - Falsification: A fresh structured handoff returns with broad risk-on confirmation across macro, index breadth, and at least two major growth cohorts for the same session.

### Alternative hypotheses (rejected counter-theses)
- Risk assets can grind higher because no bad news arrived over the skipped session.
- Gold or silver longs should be the default defensive expression today.

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
| 2026-06-14 | $73,538 |
| 2026-06-13 | $73,538 |
| 2026-06-12 | $73,538 |
| 2026-06-11 | $73,538 |
| 2026-06-10 | $73,538 |
| 2026-06-09 | $73,538 |
| 2026-06-08 | $73,538 |
| 2026-06-07 | $73,538 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 757 |
| Other ERROR | 256 |
| Python Traceback | 81 |
2 categories worth attention.

---

_End of snapshot._