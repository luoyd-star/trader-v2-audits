# Trader-v2 Daily Health Check — 2026-10-25

_Generated at 2026-10-25 11:30:01 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`1154` last_exit=`(never`
  - uptime/rss: `15-15:32:49 423808`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`1151` last_exit=`(never`
  - uptime/rss: `15-15:32:49   7776`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 2471.1h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **2471.1h old** — news_agent may have stopped producing.

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

- **package_id**: `471`
- **generated_at**: `2026-10-24 09:45:31` (age: 25.7h, today's: **NO — STALE**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#472** (conf=0.99, horizon=1d, 1 symbols incl 1 primary)
  - Claim: Fresh directional exposure should remain gated because today's inputs provide no evidence establishing a tradable market regime.
  - Falsification: A fresh completed-session report and current market observations establish a directional regime with corroborating breadth and an independently validated setup.

### Alternative hypotheses (rejected counter-theses)
- Broad equity strength supports initiating long exposure.
- Narrow semiconductor leadership supports selective short exposure.

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
| 2026-10-25 | $73,120 |
| 2026-10-24 | $73,120 |
| 2026-10-23 | $73,120 |
| 2026-10-22 | $73,120 |
| 2026-10-21 | $73,120 |
| 2026-10-20 | $73,120 |
| 2026-10-19 | $73,120 |
| 2026-10-18 | $73,120 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 1667 |
| Other ERROR | 541 |
| Python Traceback | 122 |
2 categories worth attention.

---

_End of snapshot._