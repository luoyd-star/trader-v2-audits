# Trader-v2 Daily Health Check — 2026-06-19

_Generated at 2026-06-19 11:30:04 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`2179` last_exit=`(never`
  - uptime/rss: `06-16:13:47   9248`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`2176` last_exit=`(never`
  - uptime/rss: `06-16:13:47   3680`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 169.9h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **169.9h old** — news_agent may have stopped producing.

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

- **package_id**: `119`
- **generated_at**: `2026-06-19 09:45:30` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#120** (conf=0.35, horizon=1d, 4 symbols incl 1 primary)
  - Claim: With no fresh US session confirmation, broad equity beta is unreliable and should be treated as a fade-risk regime.
  - Falsification: A fresh structured handoff appears with coherent cross-asset confirmation and at least two independent risk-on cohorts showing aligned leadership.

### Alternative hypotheses (rejected counter-theses)
- Holiday-thin liquidity could squeeze risk assets higher despite missing confirmation.
- Precious metals should be bought as the safest defensive expression today.

---

## Planner Thesis Usage (today)

| Agent | Total new plans | With parent_thesis_id | Coverage |
|---|---|---|---|
| Agent_2_MeanReversion | 1 | 1 | 100% |

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
| 2026-06-19 | $73,538 |
| 2026-06-18 | $73,538 |
| 2026-06-17 | $73,538 |
| 2026-06-16 | $73,538 |
| 2026-06-15 | $73,538 |
| 2026-06-14 | $73,538 |
| 2026-06-13 | $73,538 |
| 2026-06-12 | $73,538 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 811 |
| Other ERROR | 194 |
| Python Traceback | 10 |
2 categories worth attention.

---

_End of snapshot._