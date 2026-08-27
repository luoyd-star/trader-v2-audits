# Trader-v2 Daily Health Check — 2026-08-27

_Generated at 2026-08-27 11:30:05 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`817` last_exit=`(never`
  - uptime/rss: `18-09:54:58 119984`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`812` last_exit=`(never`
  - uptime/rss: `18-09:54:58   8928`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 1055.1h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **1055.1h old** — news_agent may have stopped producing.

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

- **package_id**: `399`
- **generated_at**: `2026-08-27 09:45:42` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#400** (conf=0.27, horizon=1d, 3 symbols incl 1 primary)
  - Claim: The information vacuum makes unconfirmed risk-on breadth fragile; favor conditional QQQ downside only after broad deterioration.
  - Falsification: Mega-cap technology and semiconductor breadth strengthen together for two consecutive sessions while the analyst handoff confirms a risk-on regime.

### Alternative hypotheses (rejected counter-theses)
- Semiconductor strength is beginning a durable broad technology rebound.
- The sparse macro report justifies an immediate defensive XAU long.

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
| 2026-08-27 | $73,120 |
| 2026-08-26 | $73,120 |
| 2026-08-25 | $73,120 |
| 2026-08-24 | $73,120 |
| 2026-08-23 | $73,120 |
| 2026-08-22 | $73,120 |
| 2026-08-21 | $73,120 |
| 2026-08-20 | $73,120 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 1439 |
| Other ERROR | 66 |
| Python Traceback | 7 |
2 categories worth attention.

---

_End of snapshot._