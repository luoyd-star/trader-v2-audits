# Trader-v2 Daily Health Check — 2026-06-15

_Generated at 2026-06-15 11:30:05 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`2179` last_exit=`(never`
  - uptime/rss: `02-16:13:48   9088`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`2176` last_exit=`(never`
  - uptime/rss: `02-16:13:48   6288`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 73.9h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **73.9h old** — news_agent may have stopped producing.

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

- **package_id**: `106`
- **generated_at**: `2026-06-15 09:45:33` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#107** (conf=0.52, horizon=3d, 5 symbols incl 1 primary)
  - Claim: Mixed regime plus low-confidence rotation data argues for fading broad beta rather than chasing risk-on continuation.
  - Falsification: Regime_Dashboard flips from mixed to confirmed risk-on while rotation/cluster signals are supported by independent market snapshot breadth for two consecutive sessions.

### Alternative hypotheses (rejected counter-theses)
- A clean risk-on rotation is underway and should be bought through AI and crypto beta.
- Gold and defensives are the best primary long because fiscal discipline remains absent.

---

## Planner Thesis Usage (today)

| Agent | Total new plans | With parent_thesis_id | Coverage |
|---|---|---|---|
| Agent_2_MeanReversion | 2 | 2 | 100% |
| Agent_3_Macro | 2 | 2 | 100% |
| Agent_5_Contrarian | 1 | 1 | 100% |

**System total: 5/5 plans linked to a thesis (100% if total else 0).**

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
| 2026-06-15 | $73,538 |
| 2026-06-14 | $73,538 |
| 2026-06-13 | $73,538 |
| 2026-06-12 | $73,538 |
| 2026-06-11 | $73,538 |
| 2026-06-10 | $73,538 |
| 2026-06-09 | $73,538 |
| 2026-06-08 | $73,538 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 789 |
| Other ERROR | 256 |
| Python Traceback | 81 |
2 categories worth attention.

---

_End of snapshot._