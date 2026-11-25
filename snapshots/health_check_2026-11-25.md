# Trader-v2 Daily Health Check — 2026-11-25

_Generated at 2026-11-25 11:30:05 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`1122` last_exit=`(never`
  - uptime/rss: `17-11:32:40   9424`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`1120` last_exit=`(never`
  - uptime/rss: `17-11:32:40   5760`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 3215.1h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **3215.1h old** — news_agent may have stopped producing.

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

- **package_id**: `559`
- **generated_at**: `2026-11-25 09:45:41` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#560** (conf=0.10, horizon=1d, 1 symbols incl 1 primary)
  - Claim: If semiconductor strength remains isolated while broad technology weakens, semiconductor leadership will not confirm a broad-tech recovery.
  - Falsification: After activation, invalidate if technology participation broadens beyond semiconductors and the broader technology cohort confirms sustained recovery across consecutive sessions. Missing observations do not constitute co…

### Alternative hypotheses (rejected counter-theses)
- Broad technology is undergoing a durable recovery.
- Fiscal concerns are sustaining a bullish gold regime.

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
| 2026-11-25 | $73,120 |
| 2026-11-24 | $73,120 |
| 2026-11-23 | $73,120 |
| 2026-11-22 | $73,120 |
| 2026-11-21 | $73,120 |
| 2026-11-20 | $73,120 |
| 2026-11-19 | $73,120 |
| 2026-11-18 | $73,120 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 1593 |
| Other ERROR | 42 |
| Python Traceback | 14 |
2 categories worth attention.

---

_End of snapshot._