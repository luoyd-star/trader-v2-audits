# Trader-v2 Daily Health Check — 2026-08-14

_Generated at 2026-08-14 11:30:03 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`817` last_exit=`(never`
  - uptime/rss: `05-09:54:56 292576`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`812` last_exit=`(never`
  - uptime/rss: `05-09:54:56  10320`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 743.1h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **743.1h old** — news_agent may have stopped producing.

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

- **package_id**: `347`
- **generated_at**: `2026-08-14 09:45:41` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#348** (conf=0.25, horizon=1d, 3 symbols incl 1 primary)
  - Claim: Absent fresh regime evidence, narrow semiconductor strength is fragile and favors selective downside over broad directional exposure.
  - Falsification: Semiconductor breadth becomes broad and persistent while the refreshed handoff confirms a risk-on regime across multiple mega-cap technology groups.

### Alternative hypotheses (rejected counter-theses)
- Broad mega-cap technology is entering a durable risk-on expansion led by semiconductors.
- The missing upstream evidence is merely an ingestion failure and markets should remain neutral.

---

## Planner Thesis Usage (today)

| Agent | Total new plans | With parent_thesis_id | Coverage |
|---|---|---|---|
| Agent_4_Volatility | 1 | 1 | 100% |
| Agent_5_Contrarian | 1 | 1 | 100% |

**System total: 2/2 plans linked to a thesis (100% if total else 0).**

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
| 2026-08-14 | $73,120 |
| 2026-08-13 | $73,120 |
| 2026-08-12 | $73,120 |
| 2026-08-11 | $73,120 |
| 2026-08-10 | $73,120 |
| 2026-08-09 | $73,120 |
| 2026-08-08 | $73,120 |
| 2026-08-07 | $73,120 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 1309 |
| Other ERROR | 180 |
| Python Traceback | 76 |
2 categories worth attention.

---

_End of snapshot._