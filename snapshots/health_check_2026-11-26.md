# Trader-v2 Daily Health Check — 2026-11-26

_Generated at 2026-11-26 11:30:02 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`1266` last_exit=`(never`
  - uptime/rss: `10:17:46  51824`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`1264` last_exit=`(never`
  - uptime/rss: `10:17:46   9808`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 3239.1h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **3239.1h old** — news_agent may have stopped producing.

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

- **package_id**: `563`
- **generated_at**: `2026-11-26 09:45:34` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#564** (conf=0.10, horizon=1d, 1 symbols incl 1 primary)
  - Claim: Broad technology upside is unconfirmed; selective semiconductor weakness is a conditional downside hypothesis only.
  - Falsification: Reject this conditional downside hypothesis if fresh observations establish sustained semiconductor participation alongside broad mega-cap technology strength; missing observations do not count as confirmation.

### Alternative hypotheses (rejected counter-theses)
- Semiconductor leadership supports a broad technology advance.
- A confirmed risk-off regime supports immediate semiconductor shorts.

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
| 2026-11-26 | $73,120 |
| 2026-11-25 | $73,120 |
| 2026-11-24 | $73,120 |
| 2026-11-23 | $73,120 |
| 2026-11-22 | $73,120 |
| 2026-11-21 | $73,120 |
| 2026-11-20 | $73,120 |
| 2026-11-19 | $73,120 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 1495 |
| Other ERROR | 1009 |
| Python Traceback | 505 |
2 categories worth attention.

---

_End of snapshot._