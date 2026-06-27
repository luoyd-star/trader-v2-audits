# Trader-v2 Daily Health Check — 2026-06-27

_Generated at 2026-06-27 11:30:05 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`2235` last_exit=`(never`
  - uptime/rss: `02-20:58:43  20224`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`2231` last_exit=`(never`
  - uptime/rss: `02-20:58:43   5936`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 361.9h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **361.9h old** — news_agent may have stopped producing.

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

- **package_id**: `148`
- **generated_at**: `2026-06-27 09:45:30` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#149** (conf=0.42, horizon=2d, 4 symbols incl 1 primary)
  - Claim: With no fresh handoff on a non-US session, the only actionable thesis is controlled continuation of existing QQQ downside exposure.
  - Falsification: A fresh structured handoff or next liquid US session shows broad risk-on confirmation across QQQ/SPY/semis while the existing QQQ short re-enters its prior compression zone.

### Alternative hypotheses (rejected counter-theses)
- The skipped report means all directional theses should be removed today.
- Use the lack of negative news to pivot risk-on into QQQ or semis.

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

| Agent | Symbol | Dir | Entry | Margin | Held/Max | % used | parent_thesis_id |
|---|---|---|---|---|---|---|---|
| A4_Volatility | QQQUSDT | SHORT | 713.34 | $1800 | -0.7h / 144h | -0% | 136 |

Total open: 1. Pre-Phase-2 legacy (no parent_thesis_id): 0.

---

## Equity (7-day trend, EOD per day)

| Day | Total equity (EOD) |
|---|---|
| 2026-06-27 | $73,564 |
| 2026-06-26 | $73,538 |
| 2026-06-25 | $73,538 |
| 2026-06-24 | $73,538 |
| 2026-06-23 | $73,538 |
| 2026-06-22 | $73,538 |
| 2026-06-21 | $73,538 |
| 2026-06-20 | $73,538 |
**Today vs yesterday: +$26**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 969 |
| Other ERROR | 41 |
| Python Traceback | 1 |
2 categories worth attention.

---

_End of snapshot._