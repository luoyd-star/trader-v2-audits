# Trader-v2 Daily Health Check — 2026-07-25

_Generated at 2026-07-25 11:30:01 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`1181` last_exit=`(never`
  - uptime/rss: `02-08:31:20   5360`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`1177` last_exit=`(never`
  - uptime/rss: `02-08:31:20   3136`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 263.1h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **263.1h old** — news_agent may have stopped producing.

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

- **package_id**: `271`
- **generated_at**: `2026-07-25 09:47:28` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#272** (conf=0.28, horizon=2d, 4 symbols incl 1 primary)
  - Claim: Broad technology upside is unconfirmed; selectively fade QQQ only if the next session again fails to show broad leadership.
  - Falsification: A fresh analyst handoff shows synchronized positive breadth across semiconductors and mega-cap technology for two consecutive completed sessions.

### Alternative hypotheses (rejected counter-theses)
- Broad risk-on participation will resume when markets reopen.
- Semiconductor leadership alone is sufficient to justify new long exposure.

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
| 2026-07-25 | $73,120 |
| 2026-07-24 | $73,120 |
| 2026-07-23 | $73,120 |
| 2026-07-22 | $73,120 |
| 2026-07-21 | $73,120 |
| 2026-07-20 | $73,120 |
| 2026-07-19 | $73,120 |
| 2026-07-18 | $73,120 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 1022 |
| Other ERROR | 183 |
| Python Traceback | 76 |
2 categories worth attention.

---

_End of snapshot._