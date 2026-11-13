# Trader-v2 Daily Health Check — 2026-11-13

_Generated at 2026-11-13 11:30:00 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`1122` last_exit=`(never`
  - uptime/rss: `05-11:32:35  27984`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`1120` last_exit=`(never`
  - uptime/rss: `05-11:32:35   8976`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 2927.1h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **2927.1h old** — news_agent may have stopped producing.

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

- **package_id**: `511`
- **generated_at**: `2026-11-13 09:45:44` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#512** (conf=0.10, horizon=1d, 1 symbols incl 1 primary)
  - Claim: If broad equity weakness emerges without broad technology participation, narrow semiconductor strength will not establish market repair.
  - Falsification: Reject the conditional downside hypothesis if contemporaneous observations show broad equity strength accompanied by sustained participation across both semiconductor and non-semiconductor technology cohorts; absent thos…

### Alternative hypotheses (rejected counter-theses)
- Broad technology recovery supports new equity longs.
- Fiscal concerns support renewed gold strength.

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
| 2026-11-13 | $73,120 |
| 2026-11-12 | $73,120 |
| 2026-11-11 | $73,120 |
| 2026-11-10 | $73,120 |
| 2026-11-09 | $73,120 |
| 2026-11-08 | $73,120 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 1606 |
| Other ERROR | 280 |
| Python Traceback | 25 |
2 categories worth attention.

---

_End of snapshot._