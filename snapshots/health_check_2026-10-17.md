# Trader-v2 Daily Health Check — 2026-10-17

_Generated at 2026-10-17 11:30:02 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`1154` last_exit=`(never`
  - uptime/rss: `07-15:32:50 274864`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`1151` last_exit=`(never`
  - uptime/rss: `07-15:32:50   7776`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 2279.1h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **2279.1h old** — news_agent may have stopped producing.

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

- **package_id**: `443`
- **generated_at**: `2026-10-17 09:45:30` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#444** (conf=0.00, horizon=1d, 1 symbols incl 1 primary)
  - Claim: Broad-equity upside continuation is an unconfirmed hypothesis pending fresh evidence of participation and macro support.
  - Falsification: On receipt of fresh session data, broad-equity participation contracts while macro conditions tighten; this joint observation rejects the upside-continuation hypothesis. Missing observations do not count as confirmation …

### Alternative hypotheses (rejected counter-theses)
- Semiconductor leadership supports a broad technology rally.
- Broad risk aversion favors equity shorts.

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
| 2026-10-17 | $73,120 |
| 2026-10-16 | $73,120 |
| 2026-10-15 | $73,120 |
| 2026-10-14 | $73,120 |
| 2026-10-13 | $73,120 |
| 2026-10-12 | $73,120 |
| 2026-10-11 | $73,120 |
| 2026-10-10 | $73,120 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 1533 |
| Other ERROR | 810 |
| Python Traceback | 254 |
2 categories worth attention.

---

_End of snapshot._