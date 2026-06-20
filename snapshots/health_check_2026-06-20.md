# Trader-v2 Daily Health Check — 2026-06-20

_Generated at 2026-06-20 11:30:05 by `scripts/daily_health_check.py`._

_This snapshot is deterministic — all sections are facts queried from DB / log / process state. AI interpretation happens in the remote Claude routine that reads this file._

---

## Process Health

- **com.bull.trader-v2**: state=`running` pid=`2179` last_exit=`(never`
  - uptime/rss: `07-16:13:48   6608`
- **com.bull.trader-v2-dashboard**: state=`running` pid=`2176` last_exit=`(never`
  - uptime/rss: `07-16:13:48   3680`

---

## News-agent Freshness

- **latest folder**: `2026-06-12_09-30-04` (age: 193.9h)
- **STATE_UPDATE.md**: ✓
- **Trader_Handoff.json**: ✓
- **Memory_Pack.yaml**: ✓
⚠ Report is **193.9h old** — news_agent may have stopped producing.

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

- **package_id**: `123`
- **generated_at**: `2026-06-20 09:45:28` (age: 1.7h, today's: **YES**)
- **active_theses count**: 1 (expected 1-3)
- **alternative_hypotheses count**: 2 (expected ≥1)

### Active theses (the spine of today's trading)
- **#124** (conf=0.32, horizon=1d, 4 symbols incl 1 primary)
  - Claim: Fresh directional edge is absent; treat any equity-beta exposure as stale and avoid chasing last-session momentum.
  - Falsification: A fresh structured handoff resumes and shows broad risk-on confirmation across index proxies, megacap tech, and semiconductors in the same session.

### Alternative hypotheses (rejected counter-theses)
- Weekend crypto could provide the only actionable directional read today.
- Hold a risk-on tech thesis from the prior session.

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
| 2026-06-20 | $73,538 |
| 2026-06-19 | $73,538 |
| 2026-06-18 | $73,538 |
| 2026-06-17 | $73,538 |
| 2026-06-16 | $73,538 |
| 2026-06-15 | $73,538 |
| 2026-06-14 | $73,538 |
| 2026-06-13 | $73,538 |
**Today vs yesterday: +$0**

---

## Errors / Red Flags (last 24h)

| Category | Count |
|---|---|
| yfinance (benign noise) | 845 |
| Other ERROR | 185 |
| Python Traceback | 1 |
2 categories worth attention.

---

_End of snapshot._