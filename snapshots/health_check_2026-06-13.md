# Trader-v2 Daily Health Check — 2026-06-13

_Generated at 2026-06-13 11:30:05 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`2179` last_exit=`(never`
  - uptime/rss: `16:13:48  13536`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`2176` last_exit=`(never`
  - uptime/rss: `16:13:48   7936`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 25.9h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓

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

- **package_id**: `98`
- **generated_at**: `2026-06-13 09:45:29` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#99** (conf=0.42, horizon=1d, 5 symbols incl 1 primary)
  - Claim: Signal scarcity makes new broad-risk longs lower quality until fresh cross-asset confirmation returns.
  - Falsification: A fresh structured handoff returns with broad risk-on confirmation across indices, semis, mega-cap tech, and crypto breadth in the same session.

### Alternative hypotheses (rejected counter-theses)
- Weekend crypto could provide the only actionable momentum signal today.
- Precious metals could remain the best defensive long if macro uncertainty persists.

---

## Planner Thesis Usage (today)

| Agent | Total new plans | With parent_thesis_id | Coverage |
|---|---|---|---|
| Agent_1_Momentum | 1 | 1 | 100% |
| Agent_4_Volatility | 2 | 2 | 100% |

**System total: 3/3 plans linked to a thesis (100% if total else 0).**

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
| 2026-06-13 | $73,538 |
| 2026-06-12 | $73,538 |
| 2026-06-11 | $73,538 |
| 2026-06-10 | $73,538 |
| 2026-06-09 | $73,538 |
| 2026-06-08 | $73,538 |
| 2026-06-07 | $73,538 |
| 2026-06-06 | $73,538 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 773 |
| Other ERROR | 257 |
| Python Traceback | 81 |
2 categories worth attention.

---

_End of snapshot._